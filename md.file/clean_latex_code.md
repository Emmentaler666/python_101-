-- clean_latex_code.lua -- Filter za čišćenje LaTeX rukopisa pri
konverziji u Markdown (GFM). -- Rješava: -- \*

::: python
...
:::

           -> ```python code block

-- \*
\begin{python}{...}{...} ... \end{python}
-\>
\`\``python code block --   * \mintinline{python}{...}                  ->`...`--   * \lstinline{...}                           ->`...\`
-- \* `\index{...}`{=tex} -\> briše se -- \*

  --------------------------------------------------------------
  -- Ideja: očistiti dijelove koje pandoc ne zna sam prevesti,
  -- a sve ostalo prepustiti pandocu.
  --------------------------------------------------------------

  ---------------------
  -- Pomoćne funkcije
  ---------------------

local function has_class(el, class) if not el.classes then return false
end for \_, c in ipairs(el.classes) do if c == class then return true
end end return false end

-- trim početne i završne whitespace znakove local function trim(s)
return (s:gsub("\^%s+", ""):gsub("%s+\$","")) end

  ------------------------------------------------------------
  -- Div: hvata
  ------------------------------------------------------------
  function Div(el) if has_class(el, "python") then -- 1) Ako u
  Div-u postoji CodeBlock, iskoristi njegov tekst local code =
  nil

  for \_, blk in ipairs(el.content) do if blk.t == "CodeBlock"
  then code = blk.text break end end

  -- 2) Ako nema CodeBlock-a, stringify cijeli sadržaj if not
  code then code = pandoc.utils.stringify(el.content) end

  -- 3) Odreži sve prije prvog Python prompta "\>\>\>" local
  pos = code:find("\>\>\>", 1, true) if pos then code =
  code:sub(pos) end

  code = trim(code)

  -- Ako je ipak ostalo prazno, neka pandan odluči if code ==
  "" then return nil end

  -- Vrati pravi fenced code-block s jezikom python return
  pandoc.CodeBlock(code, pandoc.Attr("", {"python"}, {})) end

  return nil end
  ------------------------------------------------------------

## -- RawBlock: slučaj kad pandoc ostavi LaTeX okoline kakve jesu

function RawBlock(el) if el.format \~= "latex" then return nil end

local text = el.text

-- 0) comment okolina -- kompletno je brišemo if
text:match("\\begin{comment}") then return {} end

-- 1)
\begin{python}{Naslov}{label} ... \end{python}

do local body = text:match("\\begin{python}{.-}{.-}(.-)\\end{python}")
if body then -- odreži sve prije prvog "\>\>\>", ako postoji local pos =
body:find("\>\>\>", 1, true) if pos then body = body:sub(pos) end body =
trim(body) return pandoc.CodeBlock(body, pandoc.Attr("", {"python"},
{})) end end

-- (po potrebi ovdje možeš dodati i lstlisting, important itd.)

return nil end

  ----------------------------------------------------
  -- RawInline: inline LaTeX → inline code ili briši
  ----------------------------------------------------

function RawInline(el) if el.format \~= "latex" then return nil end

local t = el.text

-- 1) `\mintinline{python}{...}`{=tex} -\> `...` do local lang, body =
t:match("\\mintinline%{(.-)%}(%b{})") if lang == "python" and body then
local code = body:sub(2, -2) -- makni vanjske {} return
pandoc.Code(code) end end

-- 2) `\lstinline{...}`{=tex} -\> `...` do local body2 =
t:match("\\lstinline(%b{})") if body2 then local code = body2:sub(2, -2)
return pandoc.Code(code) end end

-- 3) `\index{...}`{=tex} -\> brišemo (indeks za tiskanu knjigu) if
t:match("\^\\index%b{}\$") then return {} end

return nil end
