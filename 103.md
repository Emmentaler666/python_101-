# Podaci: Vrijednosti i njihove vrste

Računalo može provoditi radnje samo s *podacima*. Broj 42 je podatak,
kao i 3.14. Tekst "Život, svemir i sve!" je podatak. Ove podatke ne
percipiramo kao zbirke podataka pa ih uobičajeno jednostavno zovemo
*vrijednosti*. Ne treba puno razmišljati kako bi shvatili da postoji
beskonačno različitih vrijednosti. Također, sjetimo se sljedećeg
programa:

``` python
Nepoznati podatak za vrijeme izvršavanja programalisting:nepoznati_podatak text = input("Unesi tekst i pritisni <enter>: ") print(text) input("Pritisni <enter> za kraj")
```

U programu prikazanom u primjeru
<a href="#listing:nepoznati_podatak" data-reference-type="ref"
data-reference="listing:nepoznati_podatak">[listing:nepoznati_podatak]</a>,
vrijednost varijable `text` je prilikom pisanja programa nepoznata. To
je što god da je korisnik koji je pokrenuo program unio kad ga je
računalo to zatražilo. Drugim riječima, ne samo da postoji beskonačno
različitih vrijednosti već iste najčešće nisu poznate prilikom pisanja
programa. Ovo mora biti tako: kada bi sve vrijednosti bile unaprijed
zapisane u neki program, taj program bi uvijek radio istu stvar!

U uvodu smo već uočili da postoje različite vrste vrijednosti. Čak i
izvan sfere programiranja razlikujemo "brojke i slova". Osnovne vrste
vrijednosti u kontekstu programiranja su **cijeli** i **decimalni
brojevi**, **tekst**, **booleove vrijednosti** i vrijednost
**None**[^1]. Ostale vrste vrijednosti možemo stvoriti koristeći se ovim
osnovnim vrstama i strukturama podataka (o kojima će biti riječ
kasnije). Na primjer, datum se sastoji od tri cijela broja, a možemo ga
ljepše prikazati ukoliko ga pretvorimo u tekst sa znakovima ".", "-" ili
"/" između znamenki. Ali čak i u tom slučaju, datum je tri broja koji
ima posebna pravila prikaza kao tekst i posebna pravila za zbrajanje i
oduzimanje na razini brojeva. Sve vrste vrijednosti koje nam dakle
trebaju za rad s datumima su cijeli brojevi i tekst za potrebe prikaza.
Osnovne vrste vrijednosti su dakle temeljne za programiranje i zapis
strukturiranih podataka kao i stvaranje kompleksnijih vrsta vrijednost
pa krenimo s upoznavanjem istih.

U ovom dijelu ćemo objasniti atomske vrijednosti, odnosno cijele i
decimalne brojeve, booleove vrijednosti i vrijednost `None`. To su one
vrijednosti koje ne možemo raščlaniti na sastavne dijelove. Booleove
vrijednosti (`True` i `False`) i vrijednost `None` su uistinu
jednostavne vrijednosti i neće nam trebati puno da opišemo rad s njima.
Brojevi su znatno kompleksnija tema, ali rad s njima nam je već bar
donekle poznat iz matematike. S druge strane, tekst je vrlo važno
podrobnije objasniti jer je znatno kompleksnija tvorevina od ostalih
osnovnih vrsta vrijednosti. Također, rad s računalnim tekstom nam nije
toliko poznat iz drugih područja i specifičan je za programiranje. Za
razliku od brojeva, tekst slijedi druga pravila na papiru i na računalu
(što uključuje i rad u softveru koji imitira papir, kao što je npr.
*Microsoft Word*) pa su nam pristup radu i mogućnosti manje poznate.
Naravno, tekst je od vrlo velikog značaja za programiranje, World Wide
Web i razmjenu podataka. Radi svega navedenog, tekstu će se posvetiti
zasebno poglavlje.

## Brojevi

Postoje više vrsta brojeva, a one koje daleko najčešće koristimo su
cijeli i decimalni brojevi. Ove vrste vrijednosti se u Pythonu nazivaju
`int` i `float` što su relativno standardni nazivi za ove vrste
vrijednosti u programiranju i bazama podataka. Riječ `int` je skraćeni
oblik engleske riječi *integer* koja doslovno znači cijeli broj. Riječ
`float` dolazi od engleskog izraza *floating point number* i ovaj
koncept je malo problematičniji jer se ponešto razlikuje od decimalnih
brojeva koji su nam poznati iz matematike s ploče u školi. Takve brojeve
možemo shvatiti kao računalnu aproksimaciju decimalnih brojeva koji
omogućuju varijaciju između raspona i preciznosti. Ipak, u daleko
najvećem broju problema koje rješavamo programiranjem, `float` brojeve
možemo shvatiti kao decimalne, a razlika nam je jedino važna ukoliko
zahtijevamo preciznost na jako velikom broju decimala. Također, za
razliku od jezika niže razine i baza podataka, Python nema više vrsta
cijelih i decimalnih brojeva koje podržavaju različite minimalne i
maksimalne veličine ili broj decimala pa u ovu temu nećemo ulaziti jer
je nepotrebna za osnove programiranja i većinu programa napisanih u
Pythonu[^2].

S brojevima se najčešće radi putem aritmetičkih operatora. Slijede neki
primjeri iz interaktivnog rada s Pythonom s kojima smo se već upoznali
kod objašnjenja operatora, ali vrijedi ponoviti. Obzirom da su brojevi i
operacije s brojevima došle "s papira", najčešće radnje s brojevima
provodimo upravo kroz operatore jer nam je tako najprirodnije i najkraće
pisati.

``` python
>>> 12 + 8 20 >>> 12 - 8 4 >>> 12 * 8 96 >>> 12 ** 8 # potenciranje, 12 na 8 429981696 >>> 12 / 8 1.5 >>> 12 // 8 # cjelobrojno dijeljenje 1 >>> 12 4
```

Operatore nećemo podrobnije ovdje opisivati jer su detaljnije prikazani
u poglavlju <a href="#radnje" data-reference-type="ref"
data-reference="radnje">[radnje]</a>. Osim standardnih matematičkih
operacija s operatorima, Python ima ugrađene dodatne matematičke
funkcije i konstante mnoge od kojih su dostupne kroz *standardan modul*
`math`. "Modul" je proširenje mogućnosti Pythona i možemo ga jednostavno
shvatiti kao *plug-in*. "Standardan" modul znači da se radi o modulu
koji dolazi s Pythonom i uvijek je dostupan, odnosno koji ne zahtijeva
dodatan korak instalacije modula. U primjeru
<a href="#listing:brojevi_operacije2" data-reference-type="ref"
data-reference="listing:brojevi_operacije2">[listing:brojevi_operacije2]</a>
koristimo dodatne funkcije koje donosi modul `math`, a zadržimo se za
sada na brojevima, dok će o modulima biti riječ u poglavlju
<a href="#moduli" data-reference-type="ref"
data-reference="moduli">[moduli]</a>:

``` python
>>> round(3.1416) # funkcija za zaokruživanje je ugrađena u Python 3 >>> round(3.1416, 2) 3.14 >>> import math # koristiti ćemo modul math pa ga moramo uključiti >>> math.ceil(3.1416) # zaokruži na prvi viši cijeli broj, obratno je "floor" 4 >>> math.sqrt(625) # drugi korijen 25.0 >>> math.sin(45) # sinus; uključene su i ostale trigonometrijske funkcije 0.8509035245341184 >>> math.pi 3.141592653589793 # konstanta \pi
```

Modul `math` donosi i mnoge druge mogućnosti, a postoje i kompleksna
proširenja Pythona orijentirana na rad s brojevima bilo da se radi o
naprednijoj matematici ili specijalizacijama poput statistike. Obzirom
da se ovdje u načelu radi ili o poznatim nam matematičkim postupcima i
funkcijama (u slučaju modula `math`, to su mogućnosti poput korjenovanja
i trigonometrijskih funkcija) ili pak o naprednim područjima nevezanim
za osnove programiranja (npr. statistika, strojno učenje) no o novim
konceptima ovdje možemo stati s prikazom rada s brojevima i prikazati
druge vrste vrijednosti koje su specifičnije za programiranje.

## Booleove vrijednosti

Različitih brojeva i tekstualnih nizova ima beskonačno, ali samo su
dvije booleove vrijednosti i označavaju "da" i "ne", odnosno istinu i
neistinu, postoji i ne postoji, ima struje i nema struje, 1 i 0 ... Ove
dvije vrijednosti su neobično važne za računarstvo jer su to binarne
znamenke koje u kontekstu suvremenih digitalnih elektroničkih računala
tvore binarni brojevni sustav putem kojeg kodiramo bilo koje podatke za
potrebe interakcije s računalnim hardverom odnosno za potrebe pohrane u
memoriju i izvršavanje instrukcija. U programiranju, ove dvije
vrijednosti imaju i širu logičku upotrebu, kao što ćemo uskoro vidjeti u
primjerima. U Pythonu ih nazivamo `True` i `False`.

### Usporedba brojeva

Do bool vrijednosti u programima često dolazimo posebnim operatorima i
metodama za usporedbu. Ovakvi operatori i metode služe provjeri
istinitosti neke tvrdnje odnosno odgovaraju na da-ne pitanja. Pogledajmo
prvo najčešće operatore za usporedbu brojeva:

``` python
>>> x = 2 # ovo je pridruživanje varijabli, a ne provjera jednakosti >>> y = 3 >>> x < y # x je manje od y True >>> x >= y # x je veće ili jednako y False >>> x == y # x je jednako y False >>> x != y # x je različit od y True >>> x + y == 5 # rezultat izraza "x + y" iznosi 5 True >>> x + (y == 5) # što se ovdje dogodilo ??? 2
```

Neke detalje smo spomenuli već u uvodu i podrobnije objasnili u
poglavlju <a href="#radnje" data-reference-type="ref"
data-reference="radnje">[radnje]</a>, ali vrijedi ponoviti. Primijetimo
operator `==` u izrazu `x == y`. Rekli smo da operator `=` znači
pridruživanje vrijednosti varijabli. Bilo bi višeznačno koristiti isti
znak za operator koji provjerava jednakost pa za to postoji poseban
operator: `==`.

Na primjer, u matematici:

``` python
Znak "=" u matematicilisting:bool2 x = 1 # (pridruživanje: neka x bude 1) x + 1 = 2 # (tvrdnja jednakosti: x + 1 je jednako 2)
```

U Pythonu:

``` python
>>> x = 1 # pridruživanje: "neka x bude 1", ovo nije izraz pa nema rezultata >>> x + 1 == 2 # provjera jednakosti: "da li se izraz "x + 1" evaluira u 2" True
```

A kako to da je izraz `x + y == 5` različit od izraza `x + (y == 5)`?
Prvi dio odgovora leži u redoslijedu izvršavanja operacija. Kao što je
opisano u poglavlju <a href="#radnje" data-reference-type="ref"
data-reference="radnje">[radnje]</a>, prvo se provode aritmetičke
operacije pa zatim operacije usporedbe. U izrazu `x + y == 5` prvo se
provodi zbrajanje pa tek zatim usporedba. Taj izraz je, dakle, isto što
i `(x + y) == 5`. U izrazu `x + (y == 5)` smo zagradama promijenili
redoslijed izvršavanja operacija: prvo se provodi usporedba `y == 5`
koja vraća rezultat `False`. Zatim se provodi zbrajanje, a u ovom
slučaju to je izraz `x + False`. False je ekvivalentan vrijednosti 0 pa
je taj izraz isto što i `x + 0` te iznosi vrijednosti varijable `x`,
odnosno `2`. Za redoslijed izvršavanja operatora znamo kako iz
prijašnjeg poglavlja tako i iz osnova matematike. Za vrijednosti True i
False vrijedi zapamtiti da su ekvivalentne vrijednostima `1` i `0` i da
mnogi jezici dopuštaju aritmetičke operacije s njima. Navedeno je
pobliže prikazano u primjeru
<a href="#listing:bool_je_broj" data-reference-type="ref"
data-reference="listing:bool_je_broj">[listing:bool_je_broj]</a>.

``` python
>>> n = 42 >>> n + True # True je jednak 1 43 >>> n - True 41 >>> n + False # False je jednak 0 42 >>> n * False 0 >>> True == 1 True >>> True is 1 # ali True je u memoriji različita vrijednost od 1 False >>> True is not 1 True
```

### Usporedba drugih vrsta vrijednosti

Situacije koje provjeravamo s očekivanim odgovorima "da" i "ne" ovise
najviše o vrstama vrijednosti. Za brojeve se odnose na matematičke
koncepte (veće, manje, jednako ), ali što je na primjer s tekstom? Tekst
podržava mnoštvo tvrdnji koje možemo provjeravati, pogledajmo neke od
njih:

``` python
>>> a = ’nešto’ >>> b = ’nešto drugo’ >>> a == b # većina osnovnih vrsti podataka dopušta provjeru jednakosti False >>> ’d’ in a # da li se znak ’d’ nalazi u tekstu a False >>> ’dr’ in b # da li se znakovi ’drugo’ nalaze u tekstu b True >>> b.startswith(a) # posebne provjere se često provode posebnim metodama za vrste vrijednosti True >>> s = ’122’ >>> s.isdigit() # da li se tekst sastoji samo od brojeva? True >>> s = ’abc’ # da li se tekst sastoji samo od slova? >>> s.isalpha() True >>> s = ’abc4’ >>> s.isalpha() False
```

### Koje vrijednosti postoje?

Također, bilo koju vrijednost možemo reducirati na bool vrijednost
odnosno na "postoji/ne-postoji". Velika većina vrijednosti se
procjenjuje kao `True` jer se odnosi na vrijednost koju smatramo
"postojećom". Kod brojeva je ovdje očito o čemu se priča, 0 se
procjenjuje kao `False`, a svi ostali brojevi kao `True`. Dapače, već
smo vidjeli su vrijednosti `True` i `False` ekvivalentne brojevima 1 i 0
te da je čak s njima i moguće provoditi aritmetičke operacije. Kod
ostalih vrijednosti, međutim, također postoje "prazne vrijednosti" koje
se smatraju `False`. Riječ je u načelu o praznim "zbirkama": tekst od 0
znakova, popis s 0 elemenata itd. S mnogim zbirkama, odnosno
*strukturama podataka*, ćemo se sresti u idućim poglavljima jer su
strukture podataka nezaobilazna tema za programiranje.

``` python
>>> bool(42) True >>> bool(0) False >>> bool(None) # vrijednost None je opisana u nastavku ovog poglavlja False >>> bool(’neki tekst’) # tekst koji sadrži barem jedan znak True >>> bool(”) # prazan tekstovni niz, tekst od nula znakova False >>> bool([]) # prazan popis, više o popisima kasnije False # ali zapamtimo da se prazne zbirke procjenjuju kao False
```

### Booleovi operatori

Također, booleove vrijednosti se mogu kombinirati booleovim operatorima
`and` i `or`. Bool vrijednost se može i negirati, odnosno pretvoriti u
suprotnu bool vrijednost pomoću operatora `not` koji prethodi varijabli,
odnosno vrijednosti. Na primjer:

``` python
>>> True and False False >>> True or False True >>> not False True >>> True and not False True# shodno gore navedenom: >>> x = 1 >>> y = 2 >>> x + y == 3 and x == 1 True >>> x + y == 1000 and x == 1 False >>> x + y == 1000 or y == 2 True >>> not x == 1 False>>> a = ’nešto’ >>> b = ’nešto drugo’ >>> a.startswith(’n’) and b.startswith(’n’) True >>> a.startswith(’n’) and b.startswith(’x’) False >>> a.startswith(’n’) or b.startswith(’x’) True >>> a.startswith(’n’) and not b.startswith(’x’) True
```

## None

`None` je jedinstvena vrijednost koja označava nepostojanje vrijednosti.
Drugim riječima, postoji samo jedna moguća vrijednost čija vrsta je
`None` i ta vrijednost je `None`. Možda zvuči čudno, ali ova vrijednost
je vrlo korisna kada je potrebno eksplicitno zapisati da neka varijabla
"nema vrijednost".

Promotrimo, na primjer, razliku između vrijednosti `None` i vrijednosti
`0`.

``` python
Čemu služi vrijednost None?listing:none broj_knjiga = 0 broj_knjiga = None
```

U slučaju `broj_knjiga = 0` znači poznatu informaciju: "nula knjiga".
Kada bi se ovaj podatak koristio, na primjer, za broj posuđenih knjiga,
vrijednost 0 bi značila da nema posuđenih knjiga. S druge strane,
vrijednost `None` kod `broj_knjiga = None`, pak, znači: "broj knjiga je
nepoznat". Vrijednost `None` posebno je korisna za rad s podacima i
dizajn vlastitih funkcija (što je prikazano kasnije). U drugim jezicima
i bazama podataka, vrijednost `None` se često naziva `null`.

Za razliku od brojeva, teksta i booleovih vrijednosti, s vrijednosti
`None` nemamo posebne radnje jer za ovu vrstu vrijednosti nemaju smisla.

[^1]: Koja se u mnogim drugim jezicima i bazama podataka često zove
    `null`.

[^2]: Ako pak krenete programirati, na primjer, rakete i svemirske
    brodove, informirajte se. Barem je jedna već pala radi pogrešnih
    konverzija iz jedne vrste broja u drugi, vidi na primjer [Ariane
    5](https://en.wikipedia.org/wiki/Ariane_5#Notable_launches).
