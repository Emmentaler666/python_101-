# Kontrola toka: Kondicionali, petlje i pokušaji {#kontrola_toka}

U programiranju ne bismo daleko dogurali kada bismo jedino mogli po redu izvršavati jedinične radnje. S jedne strane moramo moći prema određenim uvjetima odabrati koje naredbe će se izvršiti, a koje ne. Ovo postižemo *kondicionalima*. S druge strane moramo moći ponavljati iste naredbe. Ovo postižemo *petljama*. U nastavku ćemo se upoznati s detaljima i riječ je o standardnim komponentama gotovo svih programskih jezika. U mnogim jezicima visoke razine postoji i treći koncept u kontroli toka, a to je *pokušaj* provođenja određenih naredbi s jasno definiranim kôdom koji će se izvršiti ako neka od naredbi ne uspije.

## Kondicionali: Ako \... onda \... {#kondicionali}

Kondicionali služe *odabiru* kôda koji će se izvršiti. Kada su neke linije ovisne o kondicionalu, tada se neće izvršavati uvijek već samo kada su određeni uvjeti zadovoljeni. Time dobivamo mogućnosti poput: \"ako se neki izraz evaluira kao True, napravi nešto; a ako ne, napravi nešto posve drugo\". Na taj način možemo reći stvari poput:

-   Ako direktorij ne postoji, stvori ga.
-   Ako datoteka postoji pitaj korisnika da li ju želi prepisati novom
    datotekom.
-   Ako korisničko ime već postoji, javi da je zauzeto, a ako korisničko
    ime ne postoji, stvori novog korisnika.
-   Ako je korisnik upisao odgovor \"a\", javi da je odgovor točan, a
    ako je korisnik upisao \"b\", \"c\" ili \"d\" javi da je odgovor
    netočan, a u svim ostalim slučajevima javi da odgovor nije
    prepoznat.

Kondicionali služe uvjetnom izvršavanju kôda. Oni prema određenim uvjetima odabiru koji će se reci izvršiti, a koji ne.

Kondicionale u programskim jezicima tipično reprezentiramo sa složenom izjavom `if`{.python}, a minimalan oblik te izjave u Pythonu je:

Najjednostavniji oblik kondicionala

listing:kondicional1 if \<izraz\>:
neka radnja

\"Neka radnja\" se izvršava samo ako izraz rezultira vrijednošću koja se procjenjuje kao `True`{.python} (vidi poglavlje o booleovim vrijednostima za detalje). Ova radnja se mora sastojati od barem jedne linije kôda, ali može se sastojati i od više njih. Konkretnije, ispod svake `if`{.python} izjave se očekuje uvučeni blok kôda. Taj blok koda, kao što je već rečeno, se naznačuje tako što su sve linije u bloku jednako uvučene i izvršava se samo ako je uvjet zadovoljen, a u suprotnom se preskače.

Što se uvlačenja kôda tiče, u Pythonu se uvijek uvlači nakon dvotočke koja se, između ostalog, koristi u kondicionalima i petljama. Općenito je pravilo da Python nakon retka koji završava s dvotočkom očekuje barem jednu uvučen redak kôda odnosno minimalan blok kôda.

Standard u Pythonu je kôd uvlačiti sa četiri razmaka koji se u prilagođenom softveru dobivaju pritiskom na tipku \"tabulator\" odnosno \"tab\". Ovaj koncept se naziva \"mekanim tabulatorom\" (eng. *soft tab*) jer služi istome čemu služi i sam znak tabulator, ali izbjegava taj znak (što ima i smisla jer je tabulator po definiciji razmak varijabilne dužine). Moguće je koristiti i znak tabulator, ali se treba pobrinuti da se ne miješaju tabulatori i razmaci. Navedeno zvuči kompleksnije no što je slučaj u praksi jer se za ujednačenost uglavnom pobrine softver u kojem programiramo.

Moguće je napisati i kondicional koji će uvijek izvršiti neki kôd tako što ga proširimo s komponentom `else`{.python} koja znači \"u svim ostalim slučajevima\".

Kondicional koji će uvijek izvršiti radnjulisting:kondicional3 if \<izraz\>: neka radnja else: \# u svim ostalim slučajevima neka druga radnja

U ovom obliku, \"neka radnja\" se izvršava kao i u prošlom, ali ako se ne izvrši, tada će se izvršiti \"neka druga radnja\". Drugim riječima ovakav kondicional će, za razliku od prošlog oblika, uvijek izvršiti neke naredbe. Pogledajmo neke konkretne primjere:

Primjer prikazuje tri kondicionala. Prvi kondicional radi nešto samo ako je uvjet zadovoljen. Druga dva kondicionala uvijek rade nešto jer imaju komponentu `else`{.python} čiji kôd se izvršava kada niti jedan drugi uvjet nije zadovoljen. Izvršavanje prikazanog koda, dakle, ispisati će dvije ili tri rečenice jer prvi prikazani kondicional nema komponentu `else`{.python} dok druga dva imaju. Koje su to?

[\[listing:kondicional4\]](#listing:kondicional4){reference-type="ref" reference="listing:kondicional4"} x je veće ili jednako y x + y je manje od 10

U prijašnjem primjeru svi izrazi koji se pojavljuju kao uvjeti se evaluiraju u booleove vrijednosti. Kad želimo vidjeti rezultat određenog izraza najjednostavnije je to probati u Python komandnoj liniji.

Što bi se dogodilo da smo koristili izraze koji se ne evaluiraju u booleovu vrijednost poput `x + y`{.python}? U Pythonu je za potrebe kondicionala moguće i implicitno pretvoriti bilo koju vrijednosti u booleovu vrijednost. Drugim riječima, izjava `if vrijednost:`{.python} se izvršava kao da smo pisali `if bool(vrijednost):`{.python}. Sjetimo se, izraz se uvijek evaluira u vrijednost pa ranije napisano ujedno znači i `if bool(izraz)`{.python}. Pogledajmo primjer:

[\[listing:kondicional5\]](#listing:kondicional5){reference-type="ref" reference="listing:kondicional5"} bool(b) se evaluira u True bool(x + y) se evaluira u True

Kako možemo napisati kondicional koji ima više od jednog eksplicitnog uvjeta (ne računajući `else`{.python})? U kondicionalima se često koriste dodatne komponente *else if* koje služe upravo ovome. Python te riječi skraćuje u riječ `elif`{.python}. Kondicional sa svim dozvoljenim komponentama izgleda ovako:

Kondicional sa svim komponentamalisting:kondicional6 if \<izraz1\>: radnja 1 elif \<izraz2\>: radnja 2 elif \<izraz3\>: radnja 3 \... else: radnja n

A evo i konkretnog primjera kondicionala sa svim komponentama:

[\[listing:kondicional6\]](#listing:kondicional6){reference-type="ref" reference="listing:kondicional6"} slučaj \"x je 3\"

Drugim riječima, svaki kondicional ima nužno jedan `if`{.python} slučaj, a može imati i bilo koji broj `elif`{.python} slučajeva i jedan `else`{.python} slučaj. Ovakav kondicional smo već vidjeli u primjeru [\[listing:kviz\]](#listing:kviz){reference-type="ref" reference="listing:kviz"}, a u idućim poglavljima ćemo za vježbu isprogramirati nešto konkretnije i iskoristiti kondicionale. Upoznajmo se ipak prije toga i s petljama i pokušajima kako bismo zaokružili koncept \"kontrole toka\".