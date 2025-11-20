# Radnje: Izjave, izrazi, operatori, funkcije i metode

Osnovna namjena programiranje je reći računalu što da *radi*. Ono što
nam je posebno zanimljivo u definiciji sastavnih dijelova programskog
kôda je vrlo svrsishodna podjela na radnje i podatke.

Programi se, slobodno govoreći, sastoje od *radnji* i od *podataka*.
Zapravo, obzirom da je program zapisan na računalo, cijeli zapis program
se sastoji od podataka pa na nekim razinama ova distinkcija ne
funkcionira. Dapače, velik napredak u povijesti računarstva je prelazak
na "programe pohranjene kao podatke". Ipak, ova podjela nam je vrlo
korisna za učenje i razumijevanje suvremenog programiranja. Radnje se
provode putem posebnih riječi koje tvore osnovu programskog jezika,
*operatora* te putem *funkcija* i *metoda*.

Većina radnji ovisi o vrsti podataka. Koje radnje možemo obavljati s
kojim podacima? Radnja `print` je univerzalna, bilo koju vrstu podataka
možemo ispisati na ekran iako katkad taj ispis korisniku neće imati
smisla. Programi su sami po sebi tekst, pa se sve može pretvoriti u
tekst. Što je s ostalim radnjama? Jasno je da možemo zbrojiti dva broja,
ali da li možemo zbrajati tekst? A tekst i broj? Probajte u IDLE-u
izvršiti sljedeće izraze: `16 + 26`, `'a' + 'b'` i `'z' + 42`. Da li su
se svi izrazi uspješno izvršili? Zašto?

Važno je dakle uočiti da radnje koje možemo provesti s nekim podacima
ovise o *vrsti tih podataka*. Upravo je u poglavljima
<a href="#podaci_vrste" data-reference-type="ref"
data-reference="podaci_vrste">[podaci_vrste]</a> i
<a href="#podaci_tekst" data-reference-type="ref"
data-reference="podaci_tekst">[podaci_tekst]</a> riječ o osnovnim
vrstama podataka i radnjama s njima jer bez tog znanja ne možemo
smisleno pristupiti programiranju. Ipak, prije no što krenemo na to,
upoznajmo se s osnovnim načinima zadavanja radnji računalu putem
programskog jezika Python. Vrijedi znati i da se ti načini mogu
generalizirati i na mnoge druge programske jezike, pa vrijede općenito
za programiranje iako se detalji među jezicima razlikuju.

## Izjave i izrazi

Najosnovniji element imperativnih jezika je *izjava* (eng. *statement*).
Izjava služi zadavanju onoga što smatramo jednom naredbom za provođenje
neke radnje. Ta naredba može biti i kompleksna, odnosno može se
sastojati od više podređenih radnji. Neke izjave su posebne riječi
propisane programskim jezikom, a neke su *izrazi*. Izraz (eng.
*expression*) je kombinacija radnji i podataka iz koje možemo izračunati
neku vrijednost. Programerski žargon ovdje kopira matematički pa se kaže
da se izrazi *evaluiraju* čime se izračunava vrijednost izraza. Izrazi
se u načelu sastoje od operatora i operanada, ali sadrže i druge
koncepte kao sastavne dijelove što je to funkcija. Pogledajmo primjere:

``` python
>>> 17 + 25 42 >>> n = 17 + 25 >>> if n print(’broj je paran’) else: print(’broj je neparan’)broj je paran >>> x = round(3.14)
```

U retku 1 vidimo jedan izraz, `17 + 25`. Ovaj izraz se sastoji od
operatora `+` te dva cijela broja kao operanada, `17` i `25`. Ovaj izraz
također tvori i jednu izjavu koju u engleskom programskom žargonu
nazivamo *expression statement*. Redak 2 je rezultat evaluacije ovog
izraza.

U retku 3 nalazi se jedna jednostavna izjava, ova izjava sadrži izraz
`17 + 25` te dodjelu rezultata ovog izraza varijabli `n`. U ovoj izjavi
prvo se evaluira izraz te se zatim rezultat izraza dodjeljuje varijabli
`n`. Dakle, nakon evaluacije izraza s desne strane, izvršava se
`n = 42`. Dodjela varijabli se ne smatra izrazom jer nema rezultat, to
je jednostavno dodjela "imena" rezultatu izraza, odnosno pridruživanje
rezultata izraza varijabli `n`.

Pod jednostavne izjave smatramo one koje se logički pišu u jedan
redak[^1]. Pored jednog ili više izraza, te izjave mogu sadržavati i
posebne konstrukte poput pridruživanja vrijednosti varijabli te drugih
izjava zadanih posebnim riječima koje propisuje Python. Ovih riječi nema
puno, rijetko se mijenjaju i u Pythonu 3 uključuju: `assert`, `pass`,
`del`, `return`, `yield`, `raise`, `break`, `continue`, `import`,
`global` i `nonlocal`. Obzirom da se radi o specijaliziranim
"naredbama", s većinom ovih izjava ćemo se upoznavati kasnije u tekstu
kada nam teme i znanje dozvole da ih kvalitetno obradimo.

U retku 4 započinje složena izjava `if` koja završava u retku 7.
Rezultat izvršavanja ove izjave možemo vidjeti u retku 10. Ovu izjavu
možemo pročitati na sljedeći način: ako je n paran broj, tada na ekran
ispiši tekst "broj je paran", a ako nije, tada ne ekran ispiši tekst
"broj je neparan". U retku 4, prvo se evaluira izraz `n \% 2`. Kao što
je opisano u pregledu aritmetičkih operatora, operator `%` vraća ostatak
cjelobrojnog dijeljenja. Nakon toga se evaluira izraz koji provjerava da
li je rezultat jednak nuli, odnosno u ovom slučaju `0 == 0`. Evaluacija
tog izraza je vrijednost `True` što rezultira time da se izvršava redak
5, a ne redak 7. Sve navedeno tvori jedan kondicional što je pobliže
opisano u poglavlju <a href="#kondicionali" data-reference-type="ref"
data-reference="kondicionali">[kondicionali]</a>.

Složene izjave sadrže više komponenata i logički se pišu u više redaka.
Tako, na primjer, izjava `if` sadrži i komponentu `else`. U Pythonu,
složenih izjava ima još manje nego jednostavnih te one služe kontroli
toka (`if`, `while`, `for` i `try`), definiciji vlastitih funkcija i
klasa (`def` i `class`) te radu s korutinama `async`. Kontrola toka se
obrađuje u poglavlju <a href="#kontrola_toka" data-reference-type="ref"
data-reference="kontrola_toka">[kontrola_toka]</a>, definicija funkcija
i klasa u dijelu <a href="#abstrakcija" data-reference-type="ref"
data-reference="abstrakcija">[abstrakcija]</a>, a korutine nisu obrađene
u ovoj knjizi.

Vrijedi i napomenuti da je složene izjave relativno nepraktično
izvršavati u komandnoj liniji pa ćemo ih rijetko viđati u primjerima
koji se koriste komandnom linijom.

U retku 11 primjera
<a href="#listing:statements_expression" data-reference-type="ref"
data-reference="listing:statements_expression">[listing:statements_expression]</a>
vidimo izjavu koja se sastoji od poziva na funkciju `round` putem oblih
zagrada unutar kojih se nalaze parametri za tu funkciju. U ovom slučaju,
funkcija prima jedan parametar, broj `3.14`. Poziv na tu funkciju čini
jedan izraz, a rezultat se pridružuje varijabli `x`.

Sada kad razumijemo osnovne koncepte u zadavanju naredbi u programskim
jezicima, odnosno izjave i izraze, pogledajmo pobliže detalje korištenja
operatora i funkcija jer su oni najosnovniji elementi provođenja radnji
putem programskih jezika.

## Operatori

Operatori su najjednostavniji način provođenja radnji u programiranju, a
mnogi su nam poznati iz matematike (npr. `+` i `-`) čak i ako nemamo
iskustva s programiranjem. Operatora ima relativno mali broj i možemo ih
svrstati u nekoliko skupina koje su opisane u nastavku. Oni su tipično
neki simbol, ali mogu biti i više simbola (poput `!=`) ili pak riječi
(poput `in` ili `and`). Uvijek su kratki za zapisati, ali ono što ih
čini operatorima je stil njihova korištenja, a ne dužina u broju
znakova. Također, operatora postoji relativno mali broj i svi mogući
operatori su unaprijed određeni samim propisom programskog jezika.
Drugim riječima, nije moguće definirati vlastite operatore.

Operatori se pišu između dvije vrijednosti ili varijable s kojima će se
provoditi radnja kao, na primjer, u izrazu `x + y`. U tom izrazu znak
`+` je operator, a varijable `x` i `y` su operandi, odnosno vrijednosti
s kojima se izvršava radnja naznačena operatorom.

Operande najčešće odvajamo razmacima od operatora. Striktno govoreći,
korištenje razmaka nije nužno u slučajevima kada je operator neki
poseban simboli opcionalno (na primjer, `x * y` i `x*y` su ekvivalentni
izrazi), ali kada je operator riječ, isto ne vrijedi jer se tada isti ne
može razlikovati od imena varijable. Na primjer, `a and b` je validan
izraz, ali `aandb` nije već se referira na jednu varijablu koja se zove
"aandb". Kao dobar stil pisanja kôda, dakle, preporuča se uvijek
stavljati razmake prije i poslije operatora čak i kada sintaksa to ne
zahtijeva.

Slijedi pregled najčešćih operatora u Pythonu. Svrha ovog dijela je dati
pregled operatora, ne podrobno objasniti korištenje svakog. Većina ovih
operatora će se detaljnije objasniti kasnije u tekstu tamo gdje to
najviše odgovara gradivu, a na ove tablice se uvijek možete vratiti kao
referencu.

### Pridruživanje vrijednosti varijabli

Daleko najčešći operator koji ćemo koristiti u kôdu je *operator za
pridruživanje vrijednosti varijabli*. To je operator `=`. Važno je
zapamtiti da ovaj operator ne provjerava jednakost (tome služi operator
`==`), već dodjeljuje vrijednosti nekoj varijabli. U Pythonu stoji i
ideja da ovime dodjeljujemo imena različitim vrijednostima kako bi se na
njih kasnije mogli referirati. To će često biti vrijednosti koje ne
znamo za vrijeme pisanja programa kao što je to slučaj kada korisnika
zatražimo unos funkcijom `input`.

``` python
>>> x = 16 # pridruži vrijednost 16 novoj varijabli x >>> y = 26 # pridruži vrijednost 26 novoj varijabli y >>> x + y # rezultat ovog izračuna nismo pridružili niti jednoj varijabli 42 >>> z = x + y # definiraj novu varijablu z kako bi se kasnije mogao pozvati na rezultat >>> print(z) # pozovi se na vrijednost varijable z 42 >>> z = y - x # pridruži novu vrijednost varijabli z >>> print(z) # pozovi se na vrijednost varijable z 10>>> text = input("Upiši neki tekst: ") # pridruži korisnički unos varijabli "text" Upiši neki tekst: neću >>> print(text) # varijabla text se sada referira na što god da je korisnik upisao ’neću’
```

Važno je primijetiti da su nam varijable nužne kako bi programirali.
Egzaktne vrijednosti vrlo često nisu poznate za vrijeme pisanja
programa. Na primjer, varijabla `text` se referira na rezultat
izvršavanja funkcije `input`, odnosno na koji god tekst da je korisnik
upisao. Bez korištenja te varijable ne bismo imali načina da se pozovemo
na korisnički unos koji može biti bilo što.

### Aritmetički operatori

Operatori koji su nam najpoznatiji su operatori iz osnova matematike. To
su aritmetički operatori i najčešće se koriste s brojevima, ali neki se
mogu koristiti i s drugim vrstama vrijednosti, kao što ćemo vidjeti u
idućem poglavlju. Pregled je vidljiv u tablici
<a href="#tab:operatori-aritmetika" data-reference-type="ref"
data-reference="tab:operatori-aritmetika">1</a>.

<div class="center">

<div id="tab:operatori-aritmetika">

| **operator** | **operacija** | **primjer** | **rezultat** |
|:---|:---|:---|:---|
| $`\boldsymbol{+}`$ | zbrajanje | $`7\:+\:2`$ | 9 |
| $`\boldsymbol{-}`$ | oduzimanje | $`7\:-\:2`$ | 5 |
| $`\boldsymbol{*}`$ | množenje | $`7\:*\:2`$ | 14 |
| $`\boldsymbol{**}`$ | potenciranje | $`7\:**\:2`$ | 49 |
| $`\boldsymbol{/}`$ | dijeljenje | $`7\:/\:2`$ | 3.5 |
| $`\boldsymbol{//}`$ | cjelobrojno dijeljenje | $`7\://\:2`$ | 2 |
| $`\boldsymbol{\%}`$ | ostatak cjelobrojnog dijeljenja | $`7\:\%\:2`$ | 1 |

Aritmetički operatori

</div>

</div>

Zanimljivost kod aritmetičkih operatora je da se svi mogu spojiti s
operatorom za pridruživanje vrijednosti varijabli (tj. `=`) kako bi se
skratilo pisanje izraza poput `x = x + 1` u `x += 1`. Drugim riječima,
možemo u isto vrijeme odraditi aritmetičku operaciju i rezultat
pridružiti varijabli. Ovo je najlakše objasniti primjerom
<a href="#listing:dodjeljivanje_aritmetika" data-reference-type="ref"
data-reference="listing:dodjeljivanje_aritmetika">[listing:dodjeljivanje_aritmetika]</a>.

``` python
>>> x = 1 >>> x = x + 2 # zbroji x i 2 pa pridruži novu vrijednost varijabli x >>> print(x) # x sada ima novu vrijednost, nije više 1 3 >>> x += 2 # isto što i x = x + 2 samo kraće za pisati >>> print(x) 5 >>> x *= 2 # isto što i x = x * 2 samo kraće za pisati >>> print(x) 10 >>> x /= 2 # isto što i x = x / 2 >>> print(x) 5.0
```

### Operatori za usporedbu

Osim aritmetičkih operacija, vrijednosti često uspoređujemo. Sve
vrijednosti možemo međusobno provjeriti da su jednake koristeći se
operatorom `==` ili nejednake koristeći se operatorom `!=`. Kod
vrijednosti koje podržavaju sortiranje možemo još i provjeravati da li
su veće ili manje od drugih vrijednosti. Operatore za usporedbu možemo
vidjeti na tablici
<a href="#tab:operatori-usporedba" data-reference-type="ref"
data-reference="tab:operatori-usporedba">2</a>.

<div class="center">

<div id="tab:operatori-usporedba">

| **operator**          | **operacija**     | **primjer**    | **rezultat** |
|:----------------------|:------------------|:---------------|:-------------|
| $`\boldsymbol{==}`$   | jednako           | $`7\:==\:2`$   | False        |
| $`\boldsymbol{!\!=}`$ | nejednako         | $`7\:!\!=\:2`$ | True         |
| $`\boldsymbol{<}`$    | manje             | $`7\:<\:2`$    | True         |
| $`\boldsymbol{<\!=}`$ | manje ili jednako | $`7\:<\!=\:2`$ | True         |
| $`\boldsymbol{>}`$    | veće              | $`7\:>\:2`$    | False        |
| $`\boldsymbol{>\!=}`$ | veće ili jednako  | $`7\:>\!=\:2`$ | False        |

Operatori za usporedbu

</div>

</div>

### Logički operatori

Različite operacije je često potrebno i logički povezivati. Na primjer
provjeravati da je više uvjeta zadovoljeno ili da je barem jedan od
uvjeta zadovoljen. Tome služe logički operatori `and`, `or` i `not`
prikazani na tablici
<a href="#tab:operatori-bool" data-reference-type="ref"
data-reference="tab:operatori-bool">3</a>. Ovi operatori zajedno s
operatorima za usporedbu imaju posebno značajnu ulogu kod kondicionala,
odnosno *if ... then ... else* konstrukcija.

<div class="center">

<div id="tab:operatori-bool">

| **operator** | **operacija**     | **primjer**              | **rezultat** |
|:-------------|:------------------|:-------------------------|:-------------|
| **and**      | logičko i         | $`7 > 2`$ and $`7 < 10`$ | True         |
| **or**       | logičko ili       | $`7 < 2`$ or $`7 < 10`$  | True         |
| **not**      | logička inverzija | not $`7\:>\:2`$          | False        |

Logički operatori

</div>

</div>

### Operatori za provjeru članstva

Često su korisni i operatori za provjeru članstva. Ovo su dva operatora
koja nam govore da li neki tekst ili struktura podataka sadrži određeni
element. Uloga ovih operatora će nam postati puno jasnija kada naučimo
strukture podataka, ali za sada primjere možemo pokazati koristeći se
tekstom. Operatori za provjeru članstva su prikazani na tablici
<a href="#tab:operatori-clanstvo" data-reference-type="ref"
data-reference="tab:operatori-clanstvo">4</a>.

<div class="center">

<div id="tab:operatori-clanstvo">

| **operator** | **operacija** | **primjer**      | **rezultat** |
|:-------------|:--------------|:-----------------|:-------------|
| **in**       | sadrži        | "a" in "abc"     | True         |
| **not in**   | ne sadrži     | "a" not in "abc" | False        |

Operatori za provjeru članstva

</div>

</div>

### Operatori za provjeru identiteta

Uz provjeravanje jednakosti postoje i operatori za provjeru identiteta
koji su vidljivi na tablici
<a href="#tab:operatori-identitet" data-reference-type="ref"
data-reference="tab:operatori-identitet">5</a>. Važno je primijetiti da
ovi operatori nisu isto što i provjera jednakosti. Provjera jednakosti
provjerava da li se dvije vrijednosti mogu smatrati ekvivalentnima
odnosno “istima”, a provjera identiteta provjerava da li se radi o istoj
vrijednosti u memoriji računala.

<div class="center">

<div id="tab:operatori-identitet">

| **operator** | **operacija**       | **primjer**   | **rezultat** |
|:-------------|:--------------------|:--------------|:-------------|
| **is**       | je isti objekt      | True is 1     | False        |
| **is not**   | ne nije isti objekt | True is not 1 | True         |

Operatori za provjeru identiteta

</div>

</div>

Ovo će početi imati više smisla kada dođemo do objektnog programiranja,
ali za sada možemo upotrebu prikazati sljedećim primjerom:

``` python
>>> True == 1 # True se može smatrati jednakom vrijednosti 1 True >>> True is 1 # True nije posve ista vrijednost u memoriji kao i 1 False
```

### Prioritet izvršavanja operacija

U ranijim primjerima prikazivali smo samo izraze koji se koriste jednim
operatorom. Što se međutim zbiva kada u istom izrazu koristimo više
operatora? Na primjer, koliko je `2 + 2 * 3`? Kako bismo izračunali taj
izraz potreban nam je koncept prioriteta operatora. Pogledajmo primjer.

``` python
>>> 2 + 2 * 3 # prvo se množi a onda zbraja 8 >>> (2 + 2) * 3 # prvo se evaluira operacija u zagradama, a tek onda množi 12
```

Kao što znamo iz matematike, postoji zadani redoslijed izvršavanja
operatora. Operacije prema prioritetu operatora. U prethodnom primjeru,
operator `*` ima veći prioritet od operatora `+` pa je prva operacija
koja se izvršava operacija `2 * 3`. Ukoliko želimo promijeniti taj
redoslijed, moramo koristiti zagrade oko jedne operacije (dakle jednog
operatora i njegovih operanada). Vrijedi zapamtiti da zagrade nisu nikad
greška. Izraz `2 + 2 * 3` isti je kao i izraz `2 + (2 * 3)`. Drugim
riječima, kada nismo sigurni u zadani prioritet operatora, uvijek možemo
koristiti zagrade kako bi se osigurali u redoslijed izvršavanja
operacija.

Dok se prikazani primjer koristi konceptima koji su nam najvjerojatnije
poznati iz matematike, u programskim jezicima to često nije tako
jednostavno. Prvi razlog je zato što se radnje ne moraju ponašati po
pravilima iz matematike (iako je to najčešći slučaj), a drugi to što u
programskim jezicima postoje operatori koji nam nisu poznati iz
matematike.

U svakom slučaju, za Python vrijedi kako je navedeno u sljedećem popisu.
Operatori zapisani na vrhu popisa imaju najveći prioritet.

1.  izrazi u zagradama

2.  izvršavanje funkcija

3.  potenciranje (`**`)

4.  pretvaranje brojeva u negativne (`-x`)

5.  množenje, dijeljenje, cjelobrojno dijeljenje, ostatak
    (`*, /, //, %`)

6.  zbrajanje i oduzimanje (`+, -`)

7.  provjera članstva, provjera identiteta i
    usporedbe(`in, not in, is, is not, <, <=, >, >=, !=, ==`)

8.  booleovi operatori (`not, and, or`)

Situacija je zapravo nešto kompleksnija, ali ovdje se navode samo
koncepti s kojima smo već upoznati. Potpunu tablicu koja definira
redoslijed izvršavanja možete pronaći u službenoj
[dokumentaciji](https://docs.python.org/3/reference/expressions.html#operator-precedence).

## Funkcije i metode

*Funkcije* su jedan od osnovnih građevnih blokova u suvremenom
programiranju i služe provođenju onoga što percipiramo kao "jednu
radnju" (iako ta radnja može interno prilično kompleksna).

Operatora, dakle, ima relativno mali broj i obavljaju neke osnovne
radnje. Drugi način provođenja radnji u programiranju je funkcijama.
Funkcija ima vrlo velik broj i obavljaju najrazličitije radnje koje su
najčešće znantno kompleksnije od onih koje obavljaju operatori. Već smo
vidjeli funkciju koja ispisuje tekst na ekran (`print`) i koja pita
korisnika za unos (`input`). Postoje i mnoge druge funkcije, za
sortiranje, zbrajanje svih brojeva u nekom popisu, pristup tekstualnim
datotekama, kopiranje i brisanje datoteka, slanje elektroničke pošte i
tako dalje. Python s verzijom 3.8 ima 69 ugrađenih funkcija vrlo
različitih namjena. Ugrađene funkcije su one koje dolaze kao sastavni
dio samog jezika i s mnogima od njih ćemo se upoznati kasnije u ovom
tekstu, a cijeli popis možete pronaći u službenoj
[dokumentaciji](https://docs.python.org/3/library/functions.html).

Uz ugrađene funkcije, Python dolazi s velikom "knjižnicom" proširenja
(eng. *add-on* ili *plugin*). Ta proširenja u Pythonu nazivamo
*modulima* i detaljnije se obrađuju u poglavlju
<a href="#moduli" data-reference-type="ref"
data-reference="moduli">[moduli]</a>. Za sada nam je važno da moduli
donose mnoge dodatne funkcije za matematiku, za rad s različitim vrstama
podataka, datotekama, sustavom ili pak slanje elektroničke pošte, da
spomenemo samo neke mogućnosti. Osim modula koji dolaze s Pythonom,
možemo i preuzeti velik broj modula koje je razvila zajednica. Također,
ne samo da možemo definirati vlastite funkcije[^2] nego bez toga nećemo
daleko dogurati s programiranjem. Funkcija dakle teoretski ima
beskonačno.

Za sada nam je važno naučiti neke temeljne koncepte vezane uz funkcije,
a kroz ovaj tekst ćemo se s mnogima i pobliže upoznati gdje to bude
svrsishodno. Kada se upoznamo s osnovama, naučiti ćemo i definirati
vlastite funkcije.

Svaka funkcija:

1.  Prima 0 ili više ulaznih vrijednosti, odnosno parametara (koji se
    često nazivaju i argumenti).

2.  Provodi neke radnje (na temelju ulaznih vrijednosti ako postoje).

3.  Vraća neku vrijednost. Ako rezultat nije relevantan vraća vrijednost
    `None`[^3]

Što je dakle funkcija u programskim jezicima? Ulazne vrijednosti za
funkciju zovemo *parametri* ili *argumenti*. Python interno koristi
engleski izraz *argument*, ali mi ćemo koristiti hrvatski izraz
*parametar* jer nam je jeziku prirodniji.

Funkcija može i ne mora primiti parametre, zatim se u funkciji dešavaju
određene radnje (npr. zbrajaju se ulazni parametri ili se ispisuju na
ekran) i na kraju funkcija vraća neku vrijednost. Funkcija koja zbraja
ulazne parametre vraća njihov zbroj kao rezultat. Kod te funkcije, kao i
kod većine, rezultat je relevantan i uopće razlog izvršavanja funkcije.
Kod funkcije `print`, funkcija ispisuje na ekran, a vraća vrijednost
`None`. Funkcije čija povratna vrijednost nije relevantna vraćaju
vrijednost `None`. U svakom slučaju, funkcije u Pythonu uvijek imaju
povratnu vrijednost.

Parametri se pišu u oble zagrade koje kod funkcija i metoda imaju
posebno značenje i označavaju naredbu[^4] za izvršavanje funkcije. Čak i
kada funkcija ne prima nikakve parametre, oble zagrade su potrebne kako
bi se funkcija izvršila. U engleskom žargonu često kažemo i da se
funkcija "poziva" (eng. *call*), a to rješenje koristi i Python pa ćemo
često naići na jezično rješenje da treba "pozvati funkciju", odnosno u
engleskoj literaturi "*call a function*", što znači isto što i "izvršiti
funkciju". Pogledajmo primjer
<a href="#listing:funkcija_izvrsavanje" data-reference-type="ref"
data-reference="listing:funkcija_izvrsavanje">[listing:funkcija_izvrsavanje]</a>.

Kao što vidimo u zadnjem slučaju, kada pokušamo oblim zagradama izvršiti
nešto što nije funkcija dobivamo grešku
`TypeError: 'int' object is not callable`. U slobodnom prijevodu, greška
u vrsti podataka: objekt vrste cijeli broj se ne može pozvati, odnosno
nije izvršiv. Navedena greška demonstrira upotrebu ranije opisane
terminologije.

<div class="important">

Izvršavanje funkcija Funkcije se pozivaju oblim zagradama. Oble zagrade
nakon riječi naznačuju da se neki kôd poziva. Na primjer, `print` se
jednostavno referira na tu funkciju i ne izvršava je. `print()` izvršava
tu funkciju.

</div>

### Pozivanje i parametri

Funkcije i metode, dakle, provode radnje na temelju ulaznih parametara.
Ponekad primaju i nula parametara, ali to je rjeđi i najjednostavniji
slučaj. Kako se parametri šalju funkcijama kad ih je više od jedan?
Postoje dva načina: pozicijski ili po imenu. Do sad smo koristili samo
pozicijski pristup i slali samo jedan parametar. Pogledajmo funkciju
`round` koja zaokružuje broj na cijeli ili na određen broj decimala kao
primjer funkcije s dva parametra.

``` python
>>> pi = 3.1416 >>> round(pi) # obavezan parametar, što se zaokružuje, bez toga radnja nema smisla 3 >>> round(pi, 2) # drugi parametar je opcionalan, na koliko decimala 3.14
```

Funkcija `round`, dakle, uzima jedan obvezan i jedan opcionalan
parametar. U primjeru
<a href="#listing:parametri_obveznost" data-reference-type="ref"
data-reference="listing:parametri_obveznost">[listing:parametri_obveznost]</a>
smo parametre definirali pozicijski. Prvi parametar je broj koji se
zaokružuje, a drugi broj decimala na koji će se zakruživati. Različite
funkcije imaju posve različite parametre i njihov broj ovisi o tome što
funkcija radi. Kako saznati parametre neke funkcije? Možemo čitati
*online* dokumentaciju ili pak iskoristiti ugrađenu funkciju `help`.

### Interna dokumentacija i funkcija help

Ukoliko u Pythonu potražimo pomoć za funkciju `round` dobit ćemo
sljedeći ispis:

``` python
>>> help(round) """ Help on built-in function round in module builtins:round(number, ndigits=None) Round a number to a given precision in decimal digits.The return value is an integer if ndigits is omitted or None. Otherwise the return value has the same type as the number. ndigits may be negative. """
```

Primijetite razliku između `help(round)` i `help(round())`. U prvom
slučaju ne izvršavamo funkciju `round` već se na nju referiramo pa ju
funkcija `help` prima kao parametar. U drugom slučaju izvršavamo
funkciju `round` pa će funkcija `help` primiti rezultat izvršavanja te
funkcije kao parametar, što nije ono što želimo postići.

Redak teksta koji nam opisuje koje parametre prima ova funkcija je
`round(number, ndigits=None)`. Nju valja čitati ovako: "Funkcija round
prima jedan obavezan parametar koji se zove `number` te jedan opcionalan
parametar `ndigits`". Parametar `ndigits` je opcionalan zato jer mu je
već pridružena vrijednost `None`. Svi parametri kojima je već pridružena
neka vrijednost su opcionalni i moramo ih definirati samo ukoliko želimo
promijeniti unaprijed zadanu vrijednost.

Parametre možemo jednostavno poslati pozicijski u ovu metodu, na prvom
mjestu nalazi se *number*, a na drugom, opcionalno, *ndigits*. Vidimo da
svaki parametar uz poziciju ima i svoje ime. Ta imena možemo koristiti
prilikom pozivanja funkcije kako bi parametre definirali putem imena, a
ne pozicije. Pogledajmo primjer:

``` python
>>> n = 3.142 >>> round(number=n) # bilo koji parametar možemo i imenovati 3 >>> round(number=n, ndigits=2) # sintaksa je ista pridruživanju vrijednosti varijabli 3.14 >>> round(ndigits=2, number=n) # kada su parametri imenovani, pozicija je nebitna 3.14
```

Imenovani parametri su korisni kad želimo preskočiti neki opcionalan
parametar i kad funkcije koje koristimo imaju velik broj parametara i
želimo osigurati da im nismo zamijenili redoslijed. Korištenje
imenovanih parametara često i poboljšava čitljivost kôda, pogotovo kod
funkcija koje primaju velik broj ulaznih vrijednosti. Postoje i funkcije
koje primaju varijabilan broj parametara i kod kojih moramo koristiti
imenovane parametre kako bi postigli određenu funkcionalnost. Kao
kompleksniji primjer možemo prikazati naredbu `print` koju smo do sada
koristili samo u najosnovnijem obliku.

``` python
>>> help(print) Help on built-in function print in module builtins:print(...) print(value, ..., sep=’ ’, end=’’, file=sys.stdout, flush=False)Prints the values to a stream, or to sys.stdout by default. Optional keyword arguments: file: a file-like object (stream); defaults to the current sys.stdout. sep: string inserted between values, default a space. end: string appended after the last value, default a newline. flush: whether to forcibly flush the stream.
```

Usredotočimo se za sada samo na parametre funkcije `print`. Vidimo novi
koncept. Prvi parametar se zove `value`, a nakon njega dolazi `...`. To
znači da možemo poslati bilo koji broj vrijednosti kao parametre za
`value`. Sve ove vrijednosti će se ispisati na ekran razdvojene
razmakom, osim ako nismo naredili drugačije. Pogledajmo primjer:

``` python
>>> print(’a’, ’b’, ’c’) a b c
```

Funkcija `print` je u liniji 1 primila tri vrijednosti koje će ispisati,
`'a', 'b'` i `'c'`. Sve tri vrijednosti su ispisane razdvojene razmakom,
a na kraju je ispisan znak za prelazak u novi redak. Ove mogućnosti
možemo kontrolirati parametrom `sep`, koji definira znak koji razdvaja
vrijednosti, i parametrom `end` koji definira znak koji s kojim se
završava ispis. Obzirom da se sve vrijednosti koje pošaljemo pozicijski
ispisuju razdvojene znakovima koje definira `sep` i završavaju znakovima
koje definira `end`, kako poslati te parametre? Koristeći se imenima.
Pogledajmo primjer.

``` python
>>> print(’a’, ’b’, ’c’, sep=’ - ’, end=’ ...’) a - b - c ... >>> print(’a’, ’b’, ’c’, sep=’’) a b c
```

U prikazanom primjeru, `'\n'` se referira na znak za novi redak, što je
pobliže opisano u poglavlju o tekstu. Redak 1 prikazuje naredbu koja
ispisuje tri vrijednosti i spaja ih sa znakovima razmak, crtica, razmak,
a završava ispis sa znakovima razmak, tri točkice i novim retkom. Redak
3 prikazuje naredbu koja koristi znak za novi redak kao `sep` pa se
svaka vrijednost ispisuje u novom retku.

### Metode

*Metode* su posebna vrsta funkcija. To su funkcije vezane za vrste
vrijednosti i uvijek rade nešto s vrijednošću za koju su vezane.
Pogledajmo razliku između funkcije `print`, i metode `upper` koju
posjeduju vrijednosti vrste tekst, odnosno u Python terminima `str`, i
koja pretvara sva mala slova u velika.

U načelu, ugrađene funkcije implementiraju radnje koje se mogu provoditi
s više vrsta vrijednosti. Na primjer `print(t)` ispisuje tekstualni
prikaz varijable `t` bez obzira na vrstu vrijednosti koja je toj
varijabli pridružena. Hipotetska funkcija `upper(t)` bi dozvoljavala
varijabli `t` da bude samo tekst pa ju je logičnije vezati uz samu
vrijednost: `t.upper()`. `t.upper(t)` bi bilo u ovom slučaju redundantno
pisati pa se pretpostavlja da metoda prima vrijednost prije točke kao
prvi parametar. Na taj način je funkcija `upper` dostupna samo kroz
tekstualne vrijednosti što pogoduje organizaciji kôda jer ju smješta u
jedini kontekst u kojem je iskoristiva. Poziv `x.upper()` javlja grešku
`AttributeError: 'int' object has no attribute 'upper'` jer objekti
vrste `int` nemaju "mogućnost" odnosno metodu `upper`: to kod brojeva
jednostavno nema smisla jer se veže uz koncept promjene veličine slova.

<div class="important">

Metode Metode su funkcije koje su vezane uz određenu vrstu vrijednosti i
implicitno primaju tu vrijednost kao prvi parametar.

</div>

[^1]: Termin "logički pišu" se koristi zato jer je jedan redak moguće
    podijeliti u više koristeći se posebnom sintaksom, kao i više redaka
    spojiti u jedan. Ovo se međutim smatra lošom praksom u pisanju kôda.

[^2]: Kao i vrste podataka, metode i module, ali ne i operatore.

[^3]: Dok prve dvije točke stoje za sve programske jezike, treća nije
    univerzalna.

[^4]: koja je tehnički gledano operator
