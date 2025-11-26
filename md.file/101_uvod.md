# Uvod u programiranje

Kada bi pisanim jezikom znali zadavati naredbe računalu, mogli bi mu
naređivati da kontinuirano izvršava naše \"recepte\". Mogli bi
automatizirati razne zadatke! To je programiranje: zadavanje naredbi
računalu putem jezika koji je osmišljen baš za tu svrhu. Obzirom da su
računala vrlo efikasna u obavljanju dosadnih i repetitivnih radnji i da
to rade brzo i precizno, to je vrlo korisna vještina.

Programiranje je, međutim, puno više od samo automatizacije poznatih nam
procesa. Takvim razmišljanjem stvaramo i uvjete za nove ideje i
mogućnosti. Možemo osmisliti potpuno nove pristupe raznim problemima. Na
ovaj način je, na primjer, nastao softver s grafičkim sučeljem koji nam
omogućuje zadavanje naredbi računalu kroz vizualne metafore radije nego
kroz tekstualne naredbe. Danas nam gotovo više nije moguće zamisliti rad
sa računalima bez ove inovacije, ali u početku to nije bila nimalo
jednostavna zamisao. Također, ovako su nastali Internet i World Wide
Web, precizniji medicinski aparati, računalne igre, algoritmi koji uče,
umjetna inteligencija, mogućnost programiranja satelita u svemiru i
robota koji istražuju Mars te mnogi drugi sustavi koji nas danas
okružuju te nam pomažu i zabavljaju nas. Ovako su nastali i računalni
virusi i ostali maliciozni softver, kontrola i krađa informacija,
utjecaj na ljudske odluke i opredjeljenja na daleko većoj i suptilnijoj
razini no ikad prije, kibernetičko ratovanje te kojekakve druge
opasnosti i nepoznatosti. Ovako su nastali Google, Facebook, Amazon i
druge gigantske web korporacije koje donose mnoge korisne usluge, ali i
počinju kontrolirati sve veću količinu informacija. Ovako nastaje sve
što su ljudi sposobni osmisliti, a može se provesti putem zadavanja
naredbi umreženim računalima\...

Ipak, ovaj tekst se ne tiče šireg utjecaja korištenja računala na gotovo
sve sfere ljudske djelatnosti već na osnove upravljanja računalom putem
programskih jezika pa ćemo se fokusirati samo na to. Važno je samo
držati na umu koliko toga je moguće postići programiranjem jer se
prilikom učenja osnova na tu činjenicu može lako zaboraviti. Za
usporedbu nam može poslužiti matematika. Dok tek učimo osnovne
aritmetičke račune lako je propustiti koliki značaj matematika ima u
arhitekturi, fizici, glazbi i mnogim drugim sferama ljudske djelatnosti.

U svakom slučaju, danas smo do te mjere okruženi raznim grafičkim
sučeljima da je često teško zamisliti što možemo s programiranjem izvan
konteksta razvoja takvog softvera. Programiranje je drugi način
komunikacije koji se temelji na formalnim jezicima i formiranju procesa
koji računalo na zahtjev može izvršiti bilo koji broj puta. Kao
praktična vještina, programiranje nam omogućuje automatizaciju
kojekakvih radnih zadataka, a izrada aplikacija s grafičkim sučeljem je
samo jedan vid korištenja ove vještine. Kao teorijsko znanje,
programiranje nam omogućava bolji uvid u rad računala i suvremenih
informacijskih sustava, ali i u formalne načine upravljanja putem
strukturiranih podataka.

O terminologiji ćemo kasnije, ali recimo za sada da zapis naredbi
izrečenih nekim programskim jezikom, odnosno skup programskih
instrukcija, nazivamo \"programskim kôdom\" što se često jednostavno
skraćuje u \"kôd\"[^1]. Kako bismo počeli programirati, moramo odabrati
neki programski jezik koji propisuje *sintaksu* za pisanje kôda. Taj
jezik nam omogućuje da razgovaramo s računalom. Sintaksa je skup pravila
koji propisuje kako ispravno formirati neki prirodni ili umjetan jezik,
odnosno koje rečenice izrečene jezikom su ispravne, a koje nisu.

Za potrebe ovog teksta odabran je programski jezik **Python**, ali
većina prikazanih koncepata i mehanizama tvore osnovu razumijevanja
programiranja koja je primjenjiva u gotovo bilo kojem suvremenom
programskom jeziku. Kada se nauči jedan programski jezik, mnogi osnovni
koncepti ostaju isti i u drugima.

Python je popularan programski jezik vrlo *visoke razine*[^2] i
*općenite namjene* koji je dostupan za sve danas popularne operativne
sustave. Neke prednosti ovog programskog jezika i razlozi radi kojih se
često uči kao prvi programski jezik su sljedeći:

-   **Brzo postizanje rezultata i brzo usvajanje jezika**: napisati
    program koji radi nešto korisno zahtijeva manje posla nego u većini
    drugih jezika. Također, Python se brzo uči i često navodi kao
    izvrstan jezik za prvi susret s programiranjem. Ipak, za razliku od
    mnogih drugih \"početničkih\" jezika, Python je koristan i
    profesionalcima.

-   **Čitljiv kôd**: sintaksa je dizajnirana s naglaskom na čitljivost.
    Python kôd je sličan engleskom jeziku te sadrži manje posebnih
    znakova (poput vitičastih zagrada i točka-zareza) od većine drugih
    jezika.

-   **Više-paradigmatski pristup**: Python dopušta proceduralno,
    objektno i funkcijsko programiranje. U njemu možemo napisati
    jednostavnu skriptu, ali i kompleksan program s grafičkim sučeljem
    ili web aplikaciju.

-   **Baterije uključene**: Python dolazi s velikom zbirkom *standardnih
    modula* koji proširuju jezik s vrlo korisnim i često potrebnim
    mogućnostima (na primjer čitanje i zapis posebnih formata, rad s
    datotekama i operativnim sustavom, slanje elektroničke pošte, rad s
    WWW tehnologijama \...). Drugim riječima, mnoge programski
    naprednije radnje su već uključene u samu instalaciju ovog
    programskog jezika.

-   **Aktivna zajednica**: Python je vrlo popularan i za mnogo toga se
    aktivno koristi. Radi toga postoji velik broj kvalitetnih proširenja
    mogućnosti ovog programskog jezika (i.e. modula) koji se aktivno
    razvijaju. Drugim riječima, u posebnim slučajevima (poput rada sa
    slikama i drugom multimedijom ili statističkim podacima) postoji već
    velik broj kvalitetnih proširenja koji nam olakšavaju rad. Također,
    lako je pronaći pomoć i dobiti podršku za česte probleme.

## Instalacija Pythona

Python programski kôd možemo pisati na papiru pa čak i na zidu pećine i
to bi još uvijek bio jezik Python. Ipak, kako bismo kôd pisan u Pythonu
*izvršili* potrebno ga je zapisati kao računalni tekst. Taj tekst se
zatim putem posebnog programa prevodi u drugu vrstu kôda koji je
računalu moguće direktno provesti, a ljudima nije čitljiv. O detaljima
ćemo kasnije, ali recimo za sada da je taj poseban program koji prevodi
Python u instrukcije izvršive računalu sama *implementacija* programskog
jezika i da ga je potrebno instalirati kako bismo mogli izvršavati
naredbe napisane u tom programskom jeziku.

Obzirom da je implementacija Pythona računalni program, a i sama
definicija jezika se razvija dodavanjem i zastarijevanjem koncepata,
Python razvojem dobiva različite verzije. Minimalna pretpostavljena
verzija Pythona za potrebe ovog teksta je 3.3., a preporuča se
instalirati zadnju 3.x verziju.

Koristite Python 3 Ova skripta nije namijenjena za Python 2.x i mnogi
primjeri u toj verziji neće raditi ili će raditi pogrešno.

U trenutku pisanja ovog teksta, Python 2 još uvijek na nekim operativnim
sustavima (MacOS te razne Linux distribucije) dolazi unaprijed
instaliran, ali se može smatrati zastarjelim i ta verzija Pythona se
koristi samo kako bi se održala kompatibilnost sa starijim sustavima
koji još nisu prerađeni u noviju verziju. Provjerite dakle da je Python
koji pokrećete Python 3, a ne 2.

Kada se Python instalira kroz standardni postupak (tj. registrira se u
operativnom sustavu), Python datoteke postaju *izvršive*, odnosno mogu
se direktno pokretati kao programi. Na primjer, \"duplim klikom\" ili u
sistemskoj komandnoj liniji. Python datoteke prepoznajemo po tome što im
je nastavak \".py\", ali su te datoteke zapravo obične tekstualne
datoteke i tipičan nastavak bi im bio \".txt\". Nastavak \".py\"
jednostavno naznačuje da se u njima ne nalazi slobodan tekst već tekst
napisan u jeziku Python. Također, uz instalaciju Pythona dolaze i
popratne komponente poput programa za interaktivno izvršavanje
programskih naredbi, dokumentacije i raznih dodatnih proširenja
mogućnosti ovog jezika.

Operativni sustav (OS) Windows ne uključuje instalaciju Pythona već ga
je potrebno dodatno instalirati. Opis instalacije za Windows OS je u
nastavku. Što se tiče raznih Linux distribucija i MacOS-a, Python je
često unaprijed instaliran, ali treba provjeriti verziju te instalirati
Python 3.x ukoliko je potrebno. Upute za instalaciju za MacOS i Linux
distribucije možete pronaći na [python.org](http://www.python.org).

### Instalacija na Windows OS-u

Standardna instalacija na Windows OS-u se obavlja putem \"instalera\"
referentne implementacije Pythona s [python.org](http://www.python.org).
Python instaliran na ovaj način dolazi sa svim standardnim dijelovima
jezika i jednostavno ga je instalirati putem uobičajenog grafičkog
sučelja za instalaciju *desktop* aplikacija. Na slici
[1](#fig:wininstall){reference-type="ref" reference="fig:wininstall"}
vidimo kako izgleda pokretanje instalacije novijih verzija Pythona.

![Instalacija Pythona na Windows OS-u](windows_install){#fig:wininstall
width="\\textwidth"}

Dok klik na \"Install Now\" obavlja većinu posla, ipak je korisno
primijetiti neke detalje i uključiti dodatne mogućnosti. Python će se po
zadanim postavkama instalirati u korisnički direktorij (na slici je
instalacija za korisnika koji se zove Z) i to u pod-direktorij
\"AppData\\Local\\Programs\\Python\". Ovo je zgodno zapamtiti jer katkad
treba pronaći instalaciju Pythona na disku. Glavni razlog za to je
instalacija proširenja (koja se u Pythonu nazivaju \"moduli\") za ovaj
programski jezik. U ovom smislu je vrlo korisna i mogućnost **Add Python
3.x to PATH** koja po zadanim postavkama nije uključena, ali dobro ju je
uključiti. Tada nakon instalacije možemo Python alate koristiti iz bilo
kojeg direktorija, što je posebno korisno za instalaciju dodatnih
modula, odnosno proširenja mogućnosti ovog programskog jezika.

## Pisanje i izvršavanje Python kôda

Kao što smo već rekli, manji Python program nije ništa drugo nego jedna
obična tekstualna datoteka s instrukcijama napisanim u jeziku Python i s
ekstenzijom \".py\" radije nego \".txt\". Ovo više manje stoji za sve
programske jezike, osim što drugi koriste vlastite ekstenzije. Python
datoteke s nastavkom .py može izvršavati direktno bez dodatnih
korisničkih koraka. Drugim riječima, .py datoteke možemo jednostavno
pokrenuti klikom miša ili unosom u komandnu liniju. Kod drugih vrsta
jezika moramo prvo automatski prevesti tekstualne datoteke koje sadrže
instrukcije u binarne datoteke koje su izvršive (kao što su to .exe
datoteke).

Drugi način izvršavanja Python kôda je unosom u Python komandnu liniju.
Ova komandna linija nije isto što i komandna linija operativnog sustava
jer izvršava Python kôd radije no sistemske naredbe. Python komandna
linija je vrlo korisna za učenje i testiranje kôda, a iskusni programeri
je koriste i za jednostavnije administrativne ili analitičke zadatke.
Nije međutim podobna za pisanje programa koje planiramo izvršiti veći
broj puta ili obavljanje kompleksnijih radnji. Ova mogućnost nije toliko
univerzalna među programskim jezicima kao što je to zapis programa u
tekstualne datoteke. Ipak, ova komandna linija nam **omogućava direktnu
eksperimentaciju** i jedna od prednosti Pythona i to posebno za potrebe
učenja programiranja. Ovu mogućnost valja, dakle, često koristiti!

Standardna instalacija Pythona dolazi s programom \"IDLE\" koji pruža
jednostavno grafičko sučelje za direktno izvršavanje kôda. Nakon što smo
instalirali Python, pokrenimo program IDLE kako bismo krenuli izvršavati
programske naredbe jer je ovo u početku vrlo korisno za upoznavanje
koncepata i eksperimentaciju s mogućnostima. IDLE se ponaša kao i većina
aplikacija s grafičkim sučeljem, odnosno moguće ju je pokrenuti kroz
*Start menu* ili ekvivalente u drugim operativnim sustavima.

![Izvršavanje Python kôda putem sučelja IDLE](idle){#fig:idle
width="\\textwidth"}

Kada pokrenemo IDLE, dočekati će nas glavno sučelje ovog programa koje
je prikazano na slici [2](#fig:idle){reference-type="ref"
reference="fig:idle"}. U glavnom prozoru IDLE-a naredbe se upisuju nakon
redaka koje počinju s \"$>>>$\", a izvršavaju pritiskom na tipku *enter*
odnosno *return*. U ovom slučaju smo izvršili jednostavan *izraz*
`1 + 1`{.python}. Kada se taj izraz evaluira pritiskom na tipku *enter*,
rezultat se ispisuje u idućem retku koja ne započinje s \"$>>>$\" kako
bi bilo jasno da se radi o rezultatu, a ne o naredbi. Obzirom da još
nismo spomenuli niti jednu posebnu naredbu za programske jezike,
probajte izvesti nekoliko osnovnih matematičkih radnji. IDLE je sam po
sebi sjajan kao kalkulator, a dobiti ćete dojam kako ovakvo sučelje
funkcionira. Nemojte se uplašiti ukoliko vam se ne ekran ispišu crvena
slova koja javljaju grešku, to je normalno.

Osim same komandne linije, IDLE funkcionira i kao program za izradu
tekstualnih datoteka odnosno omogućuje i standardan pristup
programiranju. Ako iz padajućeg izbornika odaberemo mogućnost
\"File-\>New File\", otvoriti će nam se nova tekstualna datoteka kao što
je vidljivo na slici [3](#fig:idle_text){reference-type="ref"
reference="fig:idle_text"}. Datoteka sadrži tipičan program za prvi
susret s programiranjem koji ćemo kasnije podrobnije analizirati.

![IDLE i pisanje tekstualnih datoteka](idle_text){#fig:idle_text
width="\\textwidth"}

Novi prozor koji nam se otvorio je jednostavan program za pisanje
tekstualnih datoteka (poput Notepada i sličnog softvera), a ne komandna
linija kao glavni prozor IDLE-a. U novonastalu datoteku možemo upisati
bilo koji program i zatim ga izvršiti putem mogućnosti iz padajućeg
izbornika \"Run-\>Run Module\" ili pritiskom na tipku \"F5\". Jedini
zahtjev je da prvo sačuvamo datoteku na disk pri čemu je dobro paziti da
joj dodijelimo ekstenziju .py. IDLE kao softver je, naime, dosta
asketske prirode pa neke verzije ne paze na to umjesto nas. Rezultat ove
radnje je vidljiv na slici [4](#fig:idle_text_run){reference-type="ref"
reference="fig:idle_text_run"}.

![IDLE i rezultat izvršavanja
programa](idle_text_run){#fig:idle_text_run width="\\textwidth"}

Upravo smo izvršili računalni program! Ovu datoteku nismo morali
pokretati kroz IDLE, mogli smo je i jednostavno pokrenuti direktno iz
operativnog sustava. Ipak, prije no što se bacimo na samo programiranje
recimo nešto o primjerima u ovom tekstu jer ih ubuduće nećemo više
prikazivati kroz slike softvera s grafičkim sučeljem već kao programski
kôd.

## Primjeri

Obzirom da se radi o programiranju, ovaj tekst je prepun primjera.
Primjeri su posebno označeni kako bi bilo jasno da se radi o kôdu,
radije nego o slobodnom tekstu. Na primjer:

Ovakvi primjeri su najčešći i prikazuju dio Python koda kakav bi se
nalazio u nekoj .py datoteci. Ove datoteke je najbolje za početak pisati
u softveru koji nam je jednostavno koristiti pa kasnije potencijalno
preći na profesionalniji softver za programiranje. Za upoznavanje s
ovakvim softverom i odabir aplikacije za pisanje kôda vidi poglavlje
[1.6](#softver){reference-type="ref" reference="softver"}, a za sada se
zadržimo na primjerima u ovom tekstu.

Primjeri U ovoj tekstu primjeri su neobično važni jer se upravo unutar
primjera često prenose novi koncepti i mogućnosti tako da ih je vrlo
važno sve pročitati i dobro razumjeti jer kasniji primjeri zahtijevaju
da su raniji koncepti već usvojeni.

Osim spomenute vrste primjera, postoji još jedna:

Primjeri u kojima neki reci počinju s \"$>>>$\" su česti u Python
literaturi i označavaju da se radi o interaktivnom izvršavanju kôda
kojeg je korisnik unio u komandnu liniju kao što smo prikazali ranije.
Na ovaj način se često prikazuju osnovni koncepti, a pojava ovakvog
primjera naznačuje da s prikazanim treba eksperimentirati u Python
komandnoj liniji (npr. IDLE-u) kako bi bolje usvojili prikazane koncepte
i mehanizme.

Riječ je o mogućnosti Pythona da se kôd upisuje i izvršava redak po
redak što je izvrsno za učenje jezika jer omogućava direktnu
eksperimentaciju. Reci koji počinju s \"$>>>$\" su oni koje mi upisujemo
u Python komandnu liniju, a reci bez tih znakova se mogu pojaviti samo
nakon redaka s početnim \"$>>>$\" i prikazuju rezultat izvršavanja
prijašnjeg retka, ako postoji. Naravno, znakovi \"$>>>$\" nisu dio kôda
već jednostavno naznaka gdje se nalazi početak linije koja se izvršila.
Drugim riječima, njih ne prepisujemo kada želimo isprobati kôd!

U svakom slučaju, ovakva mogućnost direktnog izvršavanja kôda je izvrsna
za učenje programiranja i eksperimentiranje pa je topla preporuka
koristiti ju čim više. Kada god niste sigurni kako nešto funkcionira i
koji je rezultat ili vrsta rezultata određenog izraza, eksperimentirajte
s time u Python komandnoj liniji.

Vrijedi napomenuti i da primjeri iz komandne linije prikazuju kôd koji
nije nužno međusobno povezan među recima, dok je to kod primjera iz
datoteka uvijek slučaj.

## Moj prvi program

Rekli smo već da se s Pythonom brzo postižu rezultati pa umjesto teorije
krenimo s implementacijom tradicionalnog programa za prvi susret s
programiranjem, a obzirom da radimo u vrlo čitljivom i produktivnom
programskom jeziku, odvesti ćemo ovaj program i korak dalje! Svi
spomenuti koncepti u ovom poglavlju su pobliže objašnjeni kasnije u
skripti.

Napravite novu tekstualnu datoteku s nazivom \"pozdrav_svijetu.py\".
Jedan način za ovo je odabir mogućnosti \"File \> New File\" u programu
IDLE. Pa zatim \"File \> Save\" u novom prozoru kada ispunimo datoteku.
Sadržaj datoteke treba biti sljedeći:

Ova datoteka je *računalni program* koji ispisuje \"Pozdrav, svijete!\"
na ekran. Prikazani program nije posebno uzbudljiv, ali ga možemo
smatrati kompletnom aplikacijom[^3]. Ekstenzija \".py\" označava da se
radi o Python kôdu. Ako je Python instaliran na sustavu, ova datoteka se
može pokrenuti kao *izvršiva* datoteka. Drugim riječima, dupli klik na
ovu datoteku (ili unos u komandnu liniju) i ovaj program će ispisati
\"Pozdrav, svijete!\" na ekran i završiti izvršavanje programa. Ako se
sustav umjesto toga požali na nepoznatu ekstenziju, znači da Python nije
pravilno instaliran odnosno da nije registriran u operativnom sustavu.

Ako pak na pokretanje datoteke samo neki prozor bljesne na ekranu i
odmah se zatvori ili se naoko ništa ne dogodi, šanse su da se program
ispravno izvršio. Naime, početnicima je čest problem vidjeti rezultate
ovog programa jer se rezultat ispisuje u komandnu liniju, a taj prozor
se uglavnom zatvori čim program završi. Za ovo je kriv operativni sustav
koji komandnu liniju zatvori čim je program gotov s izvršavanjem. Jedan
od načina na koji možemo riješiti problem je da dodamo još jednu naredbu
u naš program koja računalu govori da pričeka neki naš unos prije no što
se završi izvršavanje.

Otvorite \"pozdrav_svijetu.py\" i promijenite sadržaj u:

Probajmo sada pokrenuti \"pozdrav_svijetu.py\" duplim klikom na
datoteku. Vježba je uspješna ako vidimo ekran na kojem su ispisana dva
retka teksta (\"Pozdrav, svijete!\" i \"Pritisni \<enter\> za kraj\")
koji se se zatvara (ili vraća u komandnu liniju) kad pritisnemo tipku
*enter*. Sad smo već i doradili naš program kako bi zaobišli određene
osebujnosti operativnog sustava. Ako program još uvijek ne radi, šanse
su da smo negdje učinili pogrešku u sintaksi pa provjerite da su zagrade
i navodnici ispravno zatvoreni.

Općenito rečeno, računalni program je sustav *računalu izvršivih
naredbi*. Te naredbe rade na temelju specificiranih podataka jer
**računalo može raditi samo s podacima**. Posljedice slanja tih podataka
određenom hardveru (ekstremniji primjeri bi bili nuklearna elektrana ili
satelit u svemiru) mogu itekako imati utjecaja na stvarni svijet, ali
računalni programi interno rade samo s podacima. Možemo pojednostavljeno
reći da se računalni programi sastoje od *radnji* i od *podataka*.
Zapravo i sam zapis programa možemo smatrati podacima[^4], ali biti će
nam lakše početi programirati ako razlikujemo dijelova kôda koji
*prenose instrukcije* odnosno koje *reprezentiraju radnje* i dijelove
kôda koji *prenose informacije*, odnosno koji jednostavno
*reprezentiraju podatke*.

Pogledajmo kako to funkcionira u programu koji smo upravo napisali. U
našem programu, prva naredba se sastoji od poziva na *funkciju*
`print`{.python} s vrijednošću `'Pozdrav, svijete!'`{.python} kao
*parametrom* što zajedno tvori jedan *izraz*:
`ispiši 'Pozdrav, svijete!' na ekran`{.python}. Ovaj izraz se sastoji od
poziva na jednu radnju i svih podataka potrebnih za izvršavanje te
radnje. Ti podaci su u ovom slučaju jednostavno tekst koji treba
ispisati, a radnja se provodi pozivom na funkciju. Druga naredba se, na
isti način, sastoji od poziva na funkciju `input`{.python} s vrijednošću
`'Pritisni <enter> za kraj'`{.python}. Funkciju ovdje možemo shvatiti
kao \"naredbu računalu\" radije no u striktno matematičkom smislu, a
*poziv na funkciju* je naredba da se funkcija izvrši. Funkcija je jedan
od temeljnih načina na koji u suvremenim programskim jezicima zadajemo
radnje koje računalo treba izvršiti. Možemo reći da osnovne radnje
\"pakiramo\" u funkcije što nam omogućuje da izvršavamo kompleksnije
radnje kroz jednu naredbu. `print`{.python} je najosnovnija funkcija za
izvještavanje korisnika o rezultatima programa ili o važnim
informacijama za vrijeme izvršavanja programa, a `input`{.python} je
najosnovnija funkcija koja korisniku omogućuje unos vrijednosti u
program. Drugim riječima, `input`{.python} i `print`{.python} su osnovne
*input/output* naredbe u Pythonu. Obje funkcioniraju kroz komandnu
liniju jer bilo kakvo grafičko sučelje unosi dodatne komplikacije u
program i zahtjeve za operativni sustav. Programiranje grafičkog sučelja
za ovaj program bi, na primjer, bilo znatno kompleksnije za izvesti od
onoga što program već radi.

U našem programu, funkciju `input`{.python} koristimo samo za zadršku
programa od zatvaranja prije no što smo stigli pročitati informacije
koje nam je program ispisao. Ovo je zapravo trik koji koristimo kako nam
operativni sustav ne bi zatvorio prozor prije no što pročitamo rezultate
programa. U idućoj vježbi je prikazano kako se `input`{.python}
uobičajeno koristi.

Otvorite \"pozdrav_svijetu.py\" i promijenite sadržaj u kôd prikazan u
primjeru [\[listing:pozdrav3\]](#listing:pozdrav3){reference-type="ref"
reference="listing:pozdrav3"}, a zatim pokrenite program i pratite upute
na ekranu.

U ovom zadatku, pojavljuju se novi koncepti, *komentar* i *varijabla*.

Komentari se naznačuju znakom `#`{.python} i sav tekst nakon tog znaka
se smatra slobodnim tekstom koji se ne izvršava, a ne programskim kôdom.
Znak `#`{.python} se može pojaviti bilo na početku ili unutar retka.
Komentari služe pružanju dodatnih informacija o kôdu i vrlo su korisni
za poboljšanje čitljivosti i planiranje programa. U kompleksnom kôdu, na
primjer, korisno je napisati riječima što se u nekom dijelu odvija kako
bi se olakšao razvoj i kasnije preinake. Prilikom razvoja, često je
korisno i prvo slobodnim jezikom napisati što se sve mora gdje odvijati
pa tek zatim, kad struktura i logika programa postane jasna,
isprogramirati sam programski kôd.

Komentari Kôd je korisno komentirati i preporuča se bogato korištenje
komentara. Na taj način se mogu pružiti dodatna objašnjenja koja služe
boljem razumijevanju kôda. Također, vrlo su korisni kada čitamo tuđi kôd
ili se vratimo na vlastiti kôd koji smo napisali ranije pa zatim nismo
neko vrijeme radili na njemu.

U ovom tekstu komentari u primjerima su vrlo važni jer objašnjavaju kôd,
podsjećaju na ranije spoznaje pa čak i uvode nove koncepte.

Obratite, dakle, pažnju na komentare u primjerima jer se njima skreće
pažnja na važne ili nove koncepte. Kraći komentari koji se odnose na
jedan redak kôda se pišu u istom retku nakon samog kôda. Duži komentari
se najčešće pišu u redak iznad samog kôda te se nakon njih ne ostavlja
prazan redak. Ukoliko je komentar predugačak za redak kôda[^5], tada se
komentar može podijeliti u više redaka, a svaku je potrebno započeti
znakom `#`{.python}.

Komentarlisting:komentar print(\"jao meni\") \# komentar za ovaj redak

\# komentar za retke kôda koje slijede print(\"aha, aha\")

\# komentar koji se ne odnosi na neki poseban kôd

\# komentar koji je predugačak da bi stao u jedan redak kôda se može \#
prelomiti u dva ili više redaka, a u ovom slučaju se odnosi \# na kôd
odmah nakon komentara print(\"avaj\")

Varijable možemo shvatiti kao nazive koji stoje za druge vrijednosti. Te
vrijednosti su programeru najčešće nepoznate u trenutku pisanja kôda i
mogu se promijeniti za vrijeme izvršavanja programa. Varijable su nam
nužno potrebne kako bi se mogli referirati na razne podatke koji su
rezultati radnji u programu, koje si unijeli korisnici ili koji su pak
dohvaćeni iz vanjskih datoteka, baza podataka ili raznih *online*
usluga. U primjeru
[\[listing:pozdrav3\]](#listing:pozdrav3){reference-type="ref"
reference="listing:pozdrav3"}, `text`{.python} je varijabla. To možemo
prepoznati ponajprije zato zato jer joj se u retku
`text = input("Unesi tekst i pritisni <enter>: ")`{.python} *pridružuje*
vrijednost. Naime, znak `=`{.python} je *operator* za pridruživanje
vrijednosti varijabli. Uz funkcije, operatori (npr. `+`{.python} i
`-`{.python}) su drugi osnovan način zadavanja specifičnih radnji s
podacima. Pridruživanje vrijednost varijablama te izvršavanje radnji
putem funkcija i operatora je podrobnije opisano u idućem poglavlju, kao
i njihova povezanost sa širim konceptima *izjava* i *izraza*. Ono što
vrijedi spomenuti odmah su pravila imenovanja varijabli, funkcija i
ostalih elemenata koji imaju specifična imena.

Tekst `'Unesi tekst i pritisni <enter>: '`{.python} ili broj
`1`{.python} su vrijednosti, ne stoje za nešto drugo već jesu upravo taj
niz znakova odnosno taj broj. Varijabla `text`{.python} je drugačija,
ona ne stoji za niz od četiri slova `'text'`{.python} već je naziv za
što god je korisnik unio u program putem funkcije `input`{.python}.

Nazivi i pravila imenovanja Nazivi (npr. varijabli i funkcija) u Pythonu
i većini drugih programskih jezika se smiju sastojati samo od slova,
brojki i donje crte (\_) i ne smiju počinjati s brojem. Ne smiju, dakle,
sadržavati razmake i interpunkcijske znakove. Također, ne smiju biti
rezervirane riječi kao što su to riječi `if`{.python}, `and`{.python},
`while`{.python} i slične.

Što se funkcija tiče, kao prvi susret možemo proučiti kako radi funkcija
`input`{.python}. Ta funkcija:

1.  prima tekst za prikaz korisniku (koji mu tipično daje upute) kao
    ulazni podatak

2.  ispisuje taj tekst na ekranu te čeka da korisnik upiše nešto i
    potvrdi unos tako što stisne *enter*

3.  kao rezultat funkcije vraća tekst koji je korisnik napisao prije no
    što je stisnuo *enter*

Vrijednost varijable `text`{.python} je dakle varijabilna i točnu
vrijednost uopće ne moramo znati prilikom pisanja programa: ona je što
god da je korisnik unio putem funkcije `input`{.python} *za vrijeme
izvršavanja* programa. U naredbi
`text = input('Unesi tekst i pritisni <enter>')`{.python}, prvo se
izvršava izraz koji se sastoji od poziva funkcije `input`{.python} s
jednom vrijednosti kao parametrom. Taj izraz vraća vrijednost koju je
korisnik unio i ta vrijednost se pridružuje varijabli `text`{.python}. U
ostatku programa, kada se želimo referirati na koju god vrijednost da je
korisnik unio možemo to činiti putem varijable `text`{.python} kao u
naredbi `print(text)`{.python}. Dapače, moramo tako jer ne možemo
unaprijed znati koju će vrijednost korisnik unijeti! Općenitije, opis
funkcije `input`{.python} prikazuje kako radi tipična funkcija: primi
parametre, na osnovu njih provede neke radnje pa vrati rezultat. Taj
rezultat često pridružujemo nekoj varijabli kako bi se na njega mogli
kasnije referirati.

### Moja prva pogreška

Prije no što krenemo dalje, recimo nešto i o pogreškama u kôdu. One će
nam se često dešavati i to nije ništa neobično. Dapače, događaju se i
iskusnim programerima, a najveća razlika je što će iskusan programer
brže prepoznati o čemu se radi i ispraviti grešku. Drugim riječima, kada
vidimo crvena slova na ekranu to nas ne treba nimalo obeshrabriti.
Najčešće pogreške u početku su greška u sintaksi pisanja. Ovo se
najčešće događa kada zaboravimo zatvoriti zagradu, navodnike ili dodati
zarez gdje je potrebno.

Kada pokrenemo ovaj program, sustav će javiti sljedeću grešku:

Problem je što smo u retku 2 zaboravili zatvoriti zagradu. Obzirom da se
naredbe mogu pisati u više redaka, Python je pogrešku uočio tek u retku
3 pa nam to i javlja. Kada vidimo pogrešku vrste `SyntaxError`{.python}
to znači da nešto ne valja u retku koji nam javlja sustav ili u retku
prije toga. U ovom slučaju, greška je u retku 2. Kod pogreška je važno
zapamtiti sljedeće:

Pogreške Pogreške će nam se često dešavati, posebno u početku. To je
normalno i znači da smo radili i pokušavali. Bez obzira na koliko je
tekst pogreške dugačak, poruka koju ju opisuje je u zadnjem retku pa nju
valja pročitati prvu. Reci prije toga služe kako bi lakše pronašli
pogrešku u kôdu. S vremenom ćemo naučiti vrste pogrešaka i biti će nam
ih sve lakše ispravljati.

Pogledajmo za sada još jednu čestu pogreško, a kasnije ćemo se njima
baviti podrobnije.

Obzirom da je sada sintaksa ispravna, program će se početi izvršavati,
ali će se u retku 3 dogoditi sljedeća pogreška:

Kada nam se pojavi pogreška vrste `NameError`{.python} to znači da smo
se negdje referirali na naziv (npr. varijable ili funkcije) koji ne
postoji. U ovom slučaju smo varijablu u retku 2 nazvali `text`{.python},
a u retku 3 se referiramo na naziv `tekst`{.python} koji u ovom programu
nije definiran. Ovo će nam također biti česta pogreška i vrlo često se
javlja uslijed tipfelera. Na primjer kada napišemo \"prnit\" umjesto
\"print\".

Sada kada se više ne bojimo pogrešaka, možemo iskoristiti prikazane
koncepte, dodati jedan novi za kontrolu toka programa i možemo
isprogramirati mali računalni upitnik. Ovaj program je vidljiv u
primjeru [\[listing:kviz\]](#listing:kviz){reference-type="ref"
reference="listing:kviz"}.

Unesimo taj primjer u tekstualnu datoteku i pokrenimo. Kao što vidimo,
igraču je omogućen odabir odgovora kroz vrijednost koju unosi u komandnu
liniju. Neko grafičko sučelje bilo bi samo proširenje ovog programa koja
bi tu vrijednost unijela kroz igračev pritisak na gumb ili što slično te
omogućilo korištenje multimedije.

Nakon što je igrač unio odabir, tok programa se nastavlja u odnosu na
taj odabir. Konkretnije, prikazani kôd uključuje *kondicional* koji
odlučuje koji dio kôda će se izvršiti. Kad bismo ga pročitali normalnim
jezikom, taj kondicional bi mogao zvučati ovako: \"Ako je igrač unio
malo slovo \"a\", tada ispiši tekst vezan za odabir \"a\". Ako je pak
igrač unio malo slovo \"b\", tada ispiši tekst vezan za odabir \"b\".
Ako je pak igrač unio malo slovo \"c\", tada ispiši tekst vezan za
odabir \"c\". A ako je igrač unio bilo što drugo, tada ispiši tekst
vezan za nepoznati odabir.\" Većina riječi u prikazanom kôdu nam je sama
po sebi razumljiva, a riječ `elif`{.python} u Python kôdu je jednostavno
skraćeni oblik engleskog izraza *else if* odnosno "osim ako".

Naš kondicional se ovdje sastoji od četiri *uvjeta*. Kôd pisan uvučeno
ispod uvjeta (nakon redaka koji počinju s `if`{.python}, `elif`{.python}
ili `else`{.python}), izvršava se samo ako je uvjet zadovoljen. U
Pythonu se uvlačenjem kôda naznačava koji reci kôda se izvršavaju u
odnosu na koji uvjet. Ako je, na primjer,
`if player_choice == "c":`{.python} uvjet zadovoljen, tada se izvršavaju
reci 16 i 17. Sve retke koji se izvršavaju na ovaj način zajedno
nazivamo *blok* kôda. Dvotočka nam naznačava da se nakon retka koji
njome završava očekuje novi blok kôda odnosno da ćemo uvući retke koje
se izvršavaju u odnosu na redak koja završava s \":\".

Navedeno ćemo kasnije detaljnije objasniti, ali za sada je važno
zapamtiti da je uvlačenje u Pythonu značajno te da označava koji reci se
izvršavaju zajedno i pod što pripadaju! Također, ovdje se radi o
osebujnosti Pythona koja zgraža mnoge puriste. U drugim jezicima,
uvlačenje je uglavnom stvar stila, a blok kôda se često naznačuje
vitičastim zagradama (\"{\" i \"}\"). Ipak, bilo koji programer koji
drži do sebe će i u drugim programskim jezicima kôd uvući kako je
prikazano jer ga je tako puno ugodnije za čitati.

Primijetimo i dvostruki znak jednakosti, odnosno `==`{.python}. Ovo je
jednostavno operator za provjeru jednakosti. `a == b`{.python} čitano
normalnim jezikom je: \"Da li je a jednako b?\" i rezultat može biti
`True`{.python} ili `False`{.python}. Sjetimo se, znak `=`{.python} u
Pythonu (i mnogim drugim jezicima), služi pridruživanju vrijednosti
varijablama, a ne provjeri jednakosti! Drugim riječima `a = 1`{.python}
bi čitali \"varijabli `a`{.python} pridruži vrijednost `1`{.python}\", a
ne \"je li vrijednost pridružena varijabli `a`{.python} jednaka broju
`1`{.python}\".

U svakom slučaju, naš prvi program je sada dovoljno dorađen da smo
dobili neki dojam o programiranju i sada možemo dublje ući u teme koje
smo upravo otvorili. U ovom dijelu teksta programiranje je prikazano od
programa prema korištenim konceptima kako bi se dobio uvid u osnove
pisanja programa te se u neke koncepte nije dublje ulazilo. Kako bi
mogli programirati potrebno je biti dobro upoznat s osnovnim programskim
konceptima te o mogućnostima koje neki specifičan jezik pruža. Zato su u
nastavku cjeline razrađene obratno, od terminologije i najosnovnijih
koncepata prema specifičnim temama koje ćemo obraditi u sljedećem
redoslijedu:

1.  **Radnje:** izjave, izrazi, operatori, funkcije i metode

2.  **Podaci:** osnovne vrste vrijednosti (brojevi, booleove vrijednosti
    i vrijednost `None`{.python})

3.  **Proširenja mogućnosti:** rad s modulima

4.  **Kontrola toka:** kondicionali, petlje i pokušaji

5.  **Tekst:** osnove razumijevanja računalnog teksta i programski rad s
    istim

6.  **Putanje i datoteke:** rad s tekstualnim datotekama, putanjama i
    datotečnim sustavom

7.  **Strukture podataka:** popisi, rječnici i skupovi

8.  **Definicija funkcija:** kreiranje vlastitih radnji

9.  **Definicija modula:** kreiranje vlastitih proširenja

10. **Definicija klasa:** kreiranje vlastitih vrsta vrijednost i vezanih
    radnji

Svaka od navedenih tema biti će popraćena bogato komentiranim primjerima
kako bismo naučili koristiti prikazane teme u praksi. Ipak, prije no što
krenemo dublje u sve ovo, krenimo od općenitijeg pregleda nekih osnovnih
koncepata i pojmova.

## Osnovni koncepti i pojmovi

Kao što ste već vjerojatno uočili, tema programiranja prožeta je
vlastitom specijaliziranom terminologijom. Mnoge termine upoznat ćemo
kroz rad s vezanim konceptima. Ipak, prije no što se bacimo na samo
\"štrikanje\" kôda, korisno se upoznati s nekim osnovnim pojmovima.

### Što je to \"programski jezik\"?

Već smo rekli da je Python *programski jezik* koji je *visoke razine* i
*općenite namjene*. Što je to \"programski jezik\"? Jednostavno rečeno,
to je formalan jezik koji je namijenjen za davanje instrukcija računalu.
Tekstualan zapis ovih instrukcija nazivamo *programski kôd* ili često
samo *kôd*. Ali što je \"formalan jezik\"? Za naše potrebe možemo reći
da je to umjetan jezik koji zadovoljava strogo definiranu sintaksu i ima
strogu specifikaciju. Formalni jezici izbjegavaju pojave višeznačnosti i
istoznačnosti koje se pojavljuju u prirodnim jezicima. Cilj je postići
da kad napišemo nešto formalnim jezikom, za razliku od prirodnog jezika,
postoji samo jedna moguća ispravna interpretacija napisanog.

\"Programski jezik\" je u svojoj srži *specifikacija* formalnog jezika s
posebnom namjenom. Kôd pišemo prema toj specifikaciji i možemo ga pisati
na bilo koji medij koji podržava tekst. Recimo da čitamo ovaj tekst u
tiskanom izdanju. Python programi preneseni kroz primjere nisu ništa
manje \"Python programi\" zato jer su na papiru. Bili bi programi i da
su zapisani ugljenom na zid pećine. Međutim, da bi ih računalo moglo
*izvršiti*, moramo 1) pohraniti kôd kao računalni tekst i 2) izvršiti
taj kôd putem posebnog programa koji ga zna prevesti u instrukcije koje
računalo može provesti. Taj poseban program je *implementacija*
programskog jezika. Kada smo ranije \"instalirali Python\" zapravo smo
instalirali njegovu referentnu implementaciju. Implementaciju možemo
promatrati kao realizaciju specifikacije, a na računalima se ta
realizacija provodi kroz softver.

Implementacija programskog jezika Specifikacija programskog jezika se
implementira aplikacijom koju je potrebno instalirati kako bi se taj
programski jezik mogao izvršavati.

Perceptivniji dio publike primijetit će ovdje potencijalan problem:
programski jezik implementiran je aplikacijom koja je, po svojoj
prirodi, implementirana nekim programskim jezikom. Programski jezici se,
prema tome, implementiraju programskim jezicima! U najčešćem slučaju,
programski jezici *više razine* se implementiraju u programskim jezicima
*niže razine*. Standardna implementacija Pythona, koja je dostupna s
[python.org](http://www.python.org), zove se CPython (kada ju je
potrebno diferencirati od drugih implementacija Pythona) i, kako ime
kaže, implementirana je u programskom jeziku C. Kada netko kaže
\"instaliraj si pajton\", šanse su da misli na CPython.[^6]

### Razine programskih jezika i izvršavanje kôda

Kod programskih jezika, pridjev \"visoke razine\" znači da je jezik
visoko apstrahiran u odnosu na način na koji računala hardverski primaju
instrukcije, odnosno da koristi jednostavnu sintaksu i konstrukte nalik
prirodnom jeziku kako bi se povećala produktivnost u pisanju programa te
poboljšala čitljivost i razumijevanje napisanog kôda. Pri tome način na
koji računalo izvršava instrukcije ne utječe (jako) na sam dizajn
jezika.

Računalo pak razumije samo nule i jedinice. Nema struje, ima struje. Čim
je jezik niže razine, tim je bliži hardverskoj logici rada računala.
Danas se jezici poput C-a katkad spominju kao jezici niže razine, ali
preciznije rečeno C je sistemski jezik visoke razine. Konstrukti koje
stvaramo u C-u ne odgovaraju direktno logici računala, ali C je
orijentiran na efikasnost i dopušta upravljanje hardverom (na primjer,
upravljanje zauzećem memorije) što jezici visoke razine danas obavljaju
automatski. U Pythonu, na primjer, ne možemo direktno upravljati
zauzećem memorije jer mu to jednostavno nije namjena i u praksi upravo
radi toga može postići već reklamiranu brzinu i jednostavnost pisanja
kôda. Ono što se, naravno, gubi tim pristupom je *efikasnost izvedbe*,
ali danas nam je u mnogim slučajevima važnija *efikasnost pisanja* kôda
jer, obzirom na brzinu današnjih računala, za mnoge zadatke efikasnost
izvedbe jednostavno više nije problem.

Programski jezici najniže razine su potpuno ovisni o arhitekturi
računala i najčešće ih nazivamo *assembly* jezicima. Instrukcije koje
dajemo putem ovakvih jezika imaju otprilike jedan na jedan odnos prema
radnjama koje računalo zapravo obavlja. U ranim danima programiranja,
odnosno u prvom razdoblju u kojem su se računala počela programirati
pohranjenim programima radije nego hardverskim promjenama, bilo je
moguće programirati samo u ovakvim jezicima. Također, ovakvi programi su
daleko najefikasniji za izvedbu jer uglavnom direktno odgovaraju
hardverskim radnjama. S rastom računalne snage ovo prestaje biti problem
za mnoge aplikacije, a aplikacije koje su namijenjene za maksimalnu
efikasnost (operativni sustavi, sustavi koji funkcioniraju u stvarnom
vremenu, računalne igre \... ) se sve češće programiraju u tzv.
sistemskim jezicima poput C-a i već dugo je to standard. Pisati složene
sustave u *assembly* jezicima bilo bi problematično. Drugi razlog
korištenju *assembly* jezika je bio što jednostavno nisu postojale druge
paradigme u programiranju. Razvoj programskih jezika je uvelike razvoj
logičkih konstrukata i metafora podobnih za programiranje ljudima, a
koji se mogu prevesti u direktne instrukcije računalima.

U svakom slučaju, na najnižoj razini je *strojni kôd*: instrukcije
zapisane u binarnom kôdu koji računalo može direktno izvršavati putem
svog hardvera. Računalu, naravno, sve o čemu smo da sada pričali treba
prevesti u nule i jedinice koje direktno prenose određene instrukcije
hardveru. Skup tih instrukcija je propisan samim procesorom koji
koristimo, a kôd napisan u bilo kojem jeziku se na ovaj ili onaj način
prevodi u skup ovakvih instrukcija koje su direktno hardverski izvršive.
Izvršavanje kôda, dakle uvijek zahtijeva prevođenje u izvršivu verziju
koja više nije ljudski čitljiva.

U ovom smislu možemo razlikovati interpretirane i kompajlirane jezike.
Kod interpretiranih jezika naredbe je moguće izvršavati direktno, bez
posebnog procesa prevođenja u izvršivu datoteku. Python je ovakav jezik
(iz korisničke perspektive), što i omogućuje interaktivno izvršavanje
naredbi u komandnoj liniji. Jezici poput C-a, C++-a, Jave i C\#-a su pak
kompajlirani jezici. Kako bi se kôd napisan u ovakvim jezicima mogao
izvršiti, potrebno ga je prvo prevesti u izvršivu datoteku i taj proces
se naziva kompajliranje.

Prednost interpretacije je mogućnost direktnog izvršavanja kôda, a
manjak to što se za vrijeme izvršavanja programa (eng. *runtime*) mogu
dogoditi greške koje su je bilo moguće pronaći u procesu kompajliranja
kao i manja efikasnost izvršavanja kôda. Prednosti i mane kompajliranja
su upravo obratno.

### Namjena programskih jezika

Već smo spomenuli da je Python jezik \"općenite namjene\". Takav opis
programskog jezika znači da nema neku posebnu namjenu već široku paletu
upotreba (npr. matematičke operacije, rad s datotekama, administracija
sustava, izrada softvera s grafičkim sučelja, obrada podataka, izrada
web-stranica, itd.). Postoje i jezici s definiranom primarnom namjenom
koji se koriste u nekoj specifičnoj domeni. Na primjer, programski jezik
R je namijenjen za statističke postupke što ga čini izvrsnim za provedbu
istih nad podacima i upravljanje podacima u te svrhe, ali nije podoban
za druge radnje (npr. obrada teksta, izrada web-stranica ili aplikacija
s grafičkim sučeljem).

Uz navedeno, mnogi jezici koji su općenite namjene u praksi postanu
popularni za određene svrhe. C je, na primjer, praktički *lingua franca*
operativnih sustava. JavaScript i PHP se koriste gotovo isključivo za
programiranje web aplikacija odnosno web stranica. Python se pak
etablirao kao dobar jezik za učenje programiranja, ali i u području
analitičke obrade podataka, strojnog učenja i tzv. znanstvenog
računarstva.

### Softver, programi, aplikacije, skripte \...

Raščistili smo neke apstraktne pojmove vezane uz prirodu i izvedbu
programskih jezika. Pogledajmo još neke pojmove vezane uz ciljeve
programiranja. Programiranje, složit ćemo se, primarno služi izradi
*računalnih programa*. Računalni programi vrsta su *softvera* odnosno
sačinjavaju ih instrukcije računalu. Neki programi su *aplikacije*, neki
*skripte*, a neki pak sistemski softver poput *operativnih sustava*.

Aplikacije su programi s nekom specifičnom namjenom i koje zahtijevaju
operativni sustav za funkcioniranje. Aplikacija je softver koji je
namijenjen za diseminaciju krajnjim korisnicima, odnosno onima koji nisu
sudjelovali u implementaciji iste. Ovakav softver vrlo često ima i
grafičko sučelje.

Skripta je program koji je, često vrlo brzo[^7], napisan s nekom vrlo
specifičnom namjenom (npr. \"kopiraj sve slike koje zadovoljavaju uvjet
u neki direktorij i promjeni im rezoluciju\" ili \"preuzmi podatke iz
baze podataka, spoji ih s vanjskim podacima i zapiši ih u XML\") i kojeg
ima smisla izvršavati samo u tu usku svrhu. Skripte se katkad pokreću i
samo jednom te ih nakon toga više nema razloga pokretati jer su obavile
za što su namijenjene. Skripte vrlo često nisu namijenjene diseminaciji
krajnjim korisnicima te ih koriste samo oni koji su ih napisali ili se
ugrađuju kao automatski izvršavani elementi raznih sustava poput web
usluga. Skripte nemaju grafičko sučelje.

### Sastavni dijelovi programskog kôda

Način na koji možemo podijeliti osnovne sastavne dijelove kôda uvelike
ovisi o vrsti jezika odnosno o paradigmama unutar kojih je jezik
dizajniran. Te paradigme su široka tema koju ćemo uglavnom zaobići jer
nam za sada nisu potrebne[^8], ali recimo samo da je Python
*imperativan* jezik što znači da u njemu formalno zapisujem naredbe koje
računalu govore *što da napravi*. Ovo je najlakše objasniti u kontrastu
s *deklarativnim* jezicima u kojima formalno zapisujemo *što želimo
dobiti kao rezultat*. Primjer deklarativnog jezika specifične namjene je
SQL (*Structured Query Language*) koji služi radu s relacijskim bazama
podataka.

Najosnovniji sintaktički element imperativnih jezika je *izjava* (eng.
*statement*) koja služi zadavanju onoga što smatramo jednom radnjom. Ta
radnja može biti i složena, odnosno može se sastojati od više podređenih
radnji. Neke izjave su posebne naredbe propisane programskim jezikom, a
neke su *izrazi*. Izraz je kombinacija podataka i radnji iz koje možemo
izračunati neku vrijednost. Programerski žargon ovdje kopira matematički
pa se kaže da se izrazi *evaluiraju* čime se izračunava vrijednost.
Izrazi se u načelu sastoje od operatora i operanada, ali sadrže i druge
koncepte kao što je to funkcija. O detaljima ovoga je riječ u sljedećem
poglavlju ([\[radnje\]](#radnje){reference-type="ref"
reference="radnje"}) koje se upravo podrobnije bavi radnjama.

Obzirom na razinu pisanja, možemo spomenuti *retke* i *blokove* kôda.
Redak teksta je prirodan način podjele kôda nekog programa, pa reci
često odgovaraju individualnim izjavama. Blok kôda je skupina redaka
koji se izvršavaju kao jedna cjelina. Koncept \"bloka\" je važniji no
što se možda na prvi pogled čini. U primjeru
[\[listing:kviz\]](#listing:kviz){reference-type="ref"
reference="listing:kviz"} smo već vidjeli kondicional gdje svaki
`if`{.python}, `elif`{.python} ili `else`{.python} dio očekuje blok kôda
u nastavku koji se smije sastojati od minimalno jednog retka, ali često
ih ima i više.

Organizacija kôda se dalje dijeli s jedne strane u datoteke (gdje
različiti programski jezici imaju različitu logiku spajanja različitih
datoteka), a s druge generalizira putem definiranja vlastitih funkcija i
vrsta podataka odnosno objektnog programiranja. Ove razine su nam za
sada previše jer za razliku od do sada opisanog nisu nužno potrebne u
svakom Python programu pa ćemo o njima kasnije, kada usvojimo osnove.

## *Notepad* na stereoidima! ili U čemu pisati Python kôd? {#softver}

Python programi su dakle obične tekstualne datoteke. Ipak, pisati ih u
aplikacijama za običan tekst koji dolaze instalirani s operativnim
sustavima (poput Notepada i sličnog softvera) je pomalo naporno. Korak
iznad su naprednije verzije aplikacija za običan tekst koje omogućavaju
lakši rad sa strukturiranim tekstom poput HTML-a ili raznih programskih
jezika. Ovakve aplikacije, između ostaloga, posebno označavaju različite
dijelove kôda koristeći se bojama i vrstom slova (podebljana i kurziv),
kao što je slučaj i u primjerima u ovom tekstu. Primjer ove vrste
softvera je [Notepad++](https://notepad-plus-plus.org/).

Ovakav softver je napredak u odnosu na najobičnije urednike teksta i
može nam poslužiti za pisanje, ali svejedno nije direktno usmjeren prema
pisanju programskog kôda. Jednu aplikaciju usmjerenu prema pisanju i
izvršavanju kôda smo upravo ukratko predstavili i riječ je o programu
IDLE koji dolazi uključen u standardnu instalaciju Pythona. Prednost
ovog programa je Python komandna linija koja je vrlo korisna za učenje i
isprobavanje. Komponenta za pisati tekst, međutim, i nije neki veliki
napredak u odnosu na Notepad budući da je IDLE kao aplikacija za pisanje
tekstualnih datoteka dosta jednostavna [^9] i ne donosi mnoge mogućnosti
koje srodan softver često posjeduje.

Na razini iznad običnih urednika teksta je softver posebno dizajniran za
pisanje kôda s kompleksnim mogućnostima koje se po potrebi mogu
uključiti, ali i ne moraju. Kao preporučene predstavnike možemo
spomenuti [Atom](https://atom.io), [VS
Code](https://code.visualstudio.com) i [Sublime
Text](https://www.sublimetext.com)[^10].

Na najkompleksnijoj razini, postoje posebna \"softverska okruženja\" za
pisanje kôda. Ovakav softver zove se ***I**ntegrated **D**evelopment
**E**nvironment* (odnosno IDE softver) i uključuje mnoge dodatne
mogućnosti poput pronalaženja najčešćih grešaka i analize kôda, pomoć
pri spajanju različitih razina (e.g. programski kôd, baze podataka i web
tehnologije), automatskog preimenovanja i preseljenja dijelova kôda i
sličnih korisnih mogućnosti. Kod IDE softvera možemo razlikovati softver
orijentiran prema više jezika i softver specijaliziran za jedan jezik.

Što se pisanja Pythona tiče, ovdje ćemo izdvojiti dva IDE rješenja. Prvo
se zove [Thonny](http://thonny.org) i posebno nam je zanimljivo jer se
radi o softveru namijenjenom za početnike koje skriva kompleksnost
tipičnu za ovu vrstu softvera. Za profesionalan razvoj, pak, može se
preporučiti [PyCharm](https://www.jetbrains.com/pycharm) IDE. Ova
aplikacija dolazi u više varijanti: edukacijska verzija, verzija za
zajednicu i profesionalna verzija. Jedino profesionalna verzija se
plaća, a za potrebe ove skripte nije potrebna jer su njene dodatne
mogućnosti uglavnom vezane za izradu weba i komunikaciju s bazama
podataka radije nego za općenito Python programiranje. Edukacijska
verzija je pojednostavljena pa čak i uključuje neke Python vježbe što ju
čini zanimljivom za početnike, ali dobro je zapamtiti da je ta verzija
namijenjena za prijelaz u profesionalnije varijante ovog softvera.

Neki popularni IDE-i za više jezika uključuju
[Eclipse](https://www.eclipse.org) i [Visual
Studio](https://www.visualstudio.com). Najproduktivnije pisanje kôda
može se ostvariti upravo kroz IDE softver. To postaje posebno značajno
za veće projekte i kada često pišemo kôd, ali ovakav softver u početku
pretpostavlja od korisnika znanje o programiranju te visoku razinu
računalne pismenosti.

Obzirom na sve ovo, u čemu pisati Python kôd? Za prve susrete je
svejedno, najbolje u poznatom vam softveru koji ne zahtijeva
prepoznavanje novih mogućnosti poput IDLE-a[^11] ili
[Notepad++](https://notepad-plus-plus.org/). Zatim se vrlo brzo dobro
prebaciti na [Thonny](http://thonny.org). Dapače, nije loše ni krenuti
iz ovog softvera jer je isti namijenjen upravo za početnike. A ako tko
krene raditi kompleksnije projekte, korisno se upoznati s punim PyCharm
IDE-om ili sličnim okruženjem.

## Možda vrijedi znati i \...

U nastavku su ukratko opisane neobavezne teme koje možda nekome pomognu.
Riječ je o softveru za programiranje, o distribucijama Pythona
usmjerenim na tzv. znanstveno računarstvo i rad s podacima te o
razlikama između Pythona 2 i Pythona 3.

### Neke korisne distribucije za Windows OS

Python se vrlo često koristi u analitičkom radu i ima velik broj
dodatnih proširenja upravo za rad s podacima. Instalirati sva proširenja
može biti naporno, posebno na Windows OS-u, pa postoje posebne
instalacije Pythona koje dolaze s dodatnim komponentama.

Pored standardne instalacije, vrlo korisna distribucija Pythona za
operativni sustav Windows je [WinPython](http://winpython.github.io).
Ova *distribucija* donosi portabilnu verziju Pythona s velikim brojem
korisnih dodatnih modula primarno usmjerenih na korištenje Pythona za
rad s podacima. Ali što je *distribucija*? To je jednostavno softverski
paket koji se sastoji od same implementacije programskog jezika (bez
koje, kao što smo već rekli, kôd nije izvršiv), dodatnih modula i
popratnog softvera poput alata za pisanje i provjeru kôda. Obzirom da se
Python vrlo često koristi u obradi podataka pa tako i znanosti, česte su
tzv. znanstvene distribucije među kojima je i WinPython, a svakako treba
spomenuti i
[Anacondu](http://https://www.continuum.io/anaconda-overview).

WinPython je namijenjen da bude portabilan pa se ne registrira u sustavu
sam od sebe, ali dolazi s konfiguracijskim alatom (WinPython control
panel) s kojim je moguće tu instalaciju registrirati u sustavu (u
glavnom izborniku: *Advanced -\> Register distribution*). Kada se
provede ta naredba, WinPython se ponaša kao da je instaliran putem
standardnog Python instalera.

### Python 2 i 3

U nastavku su ukratko opisane glavne razlike između Pythona 2 i Pythona
3 za slučaj da netko planira koristiti stariju literaturu, baš mora
programirati u Pythonu 2 ili ih jednostavno zanimaju razlike. Ako ništa
od navedenog nije slučaj, slobodno preskočite ovaj dio!

Python se kao jezik i kao softver kontinuirano razvija, te postoje
starije i novije verzije. Python kôd napisan za starije verzije je u
načelu kompatibilan s novima budući da nove verzije najčešće donose nove
alate, mogućnosti i ispravke, a ne promjene starijih mogućnosti. Jedna
od iznimaka od ovog pravila je prijelaz iz Pythona 2.x u Python 3.x.
Python 3 donosi neke promjene radi kojih kôd pisan za Python 2 često
nije validan u Pythonu 3.

U trenutku pisanja, Python 3 možemo smatrati standardom i ovaj tekst je
orijentiran na Python 3. Ipak, radi se o relativno recentnoj promjeni i
Python 2 .x (zadnja verzija je python 2.7.x) je još uvijek donekle
relevantan. Razlog sporom prelasku s 2 na 3 je primarno bio u
prebacivanju velikih Python modula na Python 3, ali danas su gotovo svi
relevantni moduli već prilagođeni za trojku. Glavni razlog spominjanju
ove razlike je u korištenju starije literature (obzirom da se radi o
programskom jeziku koji se aktivno razvija, \"starija\" literatura je
izdana prije svega nekoliko godina!) koja uglavnom donosi još uvijek
relevantne teme. Također, knjige pisane relativno nedavno će često
napominjati da je \"Python 2 još uvijek standard\" što danas možemo
ignorirati.

Kako bi čitali štivo napisano za Python 2 i adaptirali ga za Python 3,
postoji nekoliko razlika koje trebamo držati na umu:

1.  Naredba `print`{.python} je promijenila ponašanje: Python 2 izjava
    `print`{.python}  \
    `'Hello, world!'`{.python} je u Pythonu 3 postala funkcija i piše se
    `print('Hello, world!')`{.python}. Glavna razlika u sintaksi su
    zagrade, što znači da je u velikom broju print naredbi pisanih za
    Python 2 samo potrebno dodati zagrade kod riječi \"print\" (kako je
    upravo prikazano) i dobit ćemo validan Python 3.

2.  U Pythonu 3 je lakše raditi s **unicode tekstom**. Otvaranje
    tekstualnih datoteka i rad s tekstom koji sadržava ne-ASCII znakove
    (a danas bi svaki tekst trebali tretirati na ovaj način) je bolje
    usvajati kroz štivo koje se temelji na Pythonu 3.

3.  U Pythonu 2, **dijeljenje cijelih brojeva** se ponaša prema logici
    računala i programskih jezika, pa, na primjer, rezultat operacije
    `5 / 2`{.python} je 2! Po logici računala, dijeljenje dva broja će
    vratiti broj iste vrste kao i dva ulazna broja, što nije intuitivno.
    U Pythonu 3, ovaj izraz se ponaša po \"standardnoj\" matematičkoj
    logici, odnosno rezultat operacije `5 / 2`{.python} je 2.5 kako
    bismo i očekivali. Drugim riječima, u Pythonu 3 ovaj problem više
    nije relevantan i u starom štivu se može ignorirati sve dok smo
    sigurni da programiramo u Pythonu 3.

4.  Python 2 funkcija `input`{.python} je izbačena iz jezika, a Python 2
    funkcija `raw\_input`{.python} je postala nova `input`{.python}
    funkcija za Python 3. Drugim riječima, funkcija `input`{.python} se
    jednostavno ne ponaša više kao u Pythonu 2, a stara `input`{.python}
    funkcija više ne postoji.

Ostale razlike između Pythona 2 i 3 su suptilnije i početniku
nepotrebne. Za par godina i ovaj cijeli dio teksta će biti moguće
izbaciti.

[^1]: Kôd se često piše i bez naglaska, odnosno jednostavno \"kod\". U
    ovom tekstu se naglasak koristi kako bi se riječ lako razlikovala od
    čestog prijedloga \"kod\" u rečenicama poput \"Kod prikazanog kôda
    možemo uočiti \...\". Također, kôd je zbirna imenica koja označava
    skup znakova za zapis programa. Množina \"kodovi\" se ne koristi u
    ovom značenju već bi značila isto što i riječ \"šifre\" ili
    \"identifikatori\".

[^2]: Razine ćemo objasniti kasnije, ali za sada vrijedi spomenuti da
    visoka razina načelno znači da je jednostavniji za korištenje od
    jezika niske razine.

[^3]: Usput rečeno, radi se o tradicionalnom primjeru za prvi susret s
    programiranjem koji je poznatiji u svojoj engleskoj inačici *Hello,
    world!*.

[^4]: Dapače, ovo je vrlo važan napredak u povijesti razvoja suvremenih
    računala. Računala su se prije toga programirala hardverski, odnosno
    prespajanjem žica i mehaničkim sklopkama.

[^5]: Koji se najčešće skraćuje na 80 ili 120 znakova po retku.

[^6]: Ostale implementaciju uključuju, na primjer, Jython (Java
    implementacija), IronPython (.net implementacija) i PyPy
    (alternativa CPythonu orijentirana na efikasnost), ali ove nisu
    relevantne za potrebe ove skripte.

[^7]: Odnosno u znatno kraćem vremeno no što to pretpostavlja razvoj
    neke aplikacije.

[^8]: Ako koga zanima više, s osnovama se može upoznati putem [ovog
    Wikipedia
    članka](https://en.wikipedia.org/wiki/Comparison_of_programming_paradigms)

[^9]: namijenjen je da bude sastavni dio instalacije pa je tako u naravi
    minimalističan

[^10]: Od spomenute tri aplikacije, jedino se Sublime naplaćuje za
    kontinuirano korištenje, ali za testiranje je dostupan bez
    ograničenja

[^11]: IDLE = IDE + Eric Idle
