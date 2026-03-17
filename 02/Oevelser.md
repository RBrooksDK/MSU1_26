<h1 align="center">Øvelser 2:<br>Talsystemer</h1>

I skal lave øvelserne inden timerne torsdag. I kan med fordel lave dem i grupper og diskutere dem indbyrdes. Det er vigtigt, at I forstår opgaverne og kan forklare dem til hinanden. På torsdag diskuterer vi opgaverne, og I skal være klar til at præsentere dem for klassen.

<style>
body[data-md-color-scheme] .md-content ol       { list-style-type: lower-alpha; }
body[data-md-color-scheme] .md-content ol li    { padding-left: 10px; }
</style>

#### Øvelse 1: Binær til Decimal

Konverter følgende binære tal til decimale tal.

1. $110$ (1)
{ .annotate }

    1. $6_{10}$

2. $1110111100_2$(1)
{ .annotate }

    1. $956_{10}$

3. $1001101110110_2$(1)
{ .annotate }

    1. $4982_{10}$

#### Øvelse 2: Decimal til Binær
Angiv den binære udvidelse af følgende værdier og angiv derefter tallet i binær. 

1. $49_{10}$

    ??? answer "&nbsp;"
        $1\cdot2^5 + 1\cdot2^4 + 0\cdot2^3 + 0\cdot 2^2 + 0\cdot 2^1 + 1\cdot2^0$

        $110001$

2. $212_{10}$

    ??? answer "&nbsp;"
        $1\cdot 2^7 + 1\cdot 2^6 + 1 \cdot 2^4 + 1 \cdot 2^2$

        $11010100_2$

#### Øvelse 3: Konverter til Decimal
Angiv den hexadecimale udvidelse af følgende værdier og angiv derefter tallet i decimal. 

1. $37D_{16}$

    ??? answer "&nbsp;"

        $3 \cdot 16^2 + 7 \cdot 16^1 + 13 \cdot 16^0$

        $893_{10}$

2. $1A9_{16}$

    ??? answer "&nbsp;"

        $1 \cdot 16^2 + 10 \cdot 16^1 + 9 \cdot 16^0$

        $425$

#### Øvelse 4: Hex og Binær

Løs "crossbins" nedenfor. Hintsene er i hexadecimal, og svarene skal være i binær.  
**Bemærk**: Hvis dit tal er for kort, tilføj nuller foran!

<img src="../src/crossbin1.png" alt="Crossbin 1" width="400"/>

??? answer "&nbsp;"
    <img src="../src/crossbin1sol-1.jpg" alt="Crossbin 1" width="400"/>

<img src="../src/crossbin2.png" alt="Crossbin 2" width="350"/>

??? answer "&nbsp;"
    <img src="../src/crossbinsol-1%201.jpg" alt="Crossbin 2" width="350"/>

#### Øvelse 5: Hex og Binær

Lad $S$ være mængden af alle binære tal med 7 tegn, og lad $f$ være en funktion fra $S$ til $\mathbb{Z}$ givet ved $f(x_2) = x_{10}$.

1. Bestem $f(111010)$.(1)
{ .annotate }

    1. 58

2. Ordenen af en mængde er antallet af elementer i en mængde. For eksempel er ordenen af ${1, 5, 7, 19, 27, 39}$ lig med 6. Bestem ordenen af mængden $S$. (1)
{ .annotate }

    1. 128

#### Øvelse 6: Binær Addition

Udfør følgende binære additionsoperationer. Vis dit arbejde ved at overføre som nødvendigt.

1. $1011_2 + 1101_2$ (1)
{ .annotate }

    1. $11000_2$ (hvilket svarer til $24_{10}$)

2. $10110101_2 + 1101110_2$ (1)
{ .annotate }

    1. $100100011_2$ (hvilket svarer til $291_{10}$)

#### Øvelse 7: Binær Multiplikation

Udfør følgende binære multiplikationsoperationer. Vis dit arbejde ved hjælp af standard multiplikationsalgoritmen.

1. $101_2 \times 11_2$ (1)
{ .annotate }

    1. $1111_2$ (hvilket svarer til $15_{10}$)

2. $1101_2 \times 110_2$ (1)
{ .annotate }

    1. $1001110_2$ (hvilket svarer til $78_{10}$)

3. $10111_2 \times 1011_2$ (1)
{ .annotate }

    1. $11111101_2$ (hvilket svarer til $253_{10}$)

#### Øvelse 8: Oktal

I hver underopgave skal du udføre den første konvertering og betegne resultatet som x. Derefter skal du konvertere x yderligere til det ønskede talsystem.

1. $(1101011)_2 \longrightarrow x_8 \longrightarrow x_{10}$

    ??? answer "&nbsp;"

        $(153)_8$ = $107_{10}$

2. $(782)_{10} \longrightarrow x_8 \longrightarrow x_2$

    ??? answer "&nbsp;"
    
        $(1416)_8$ = $1100001110_2$

3. $\left(5B7\right)_{16} \rightarrow x_2 \rightarrow x_8$

    ??? answer "&nbsp;"

        $(10110110111)_2$ = $(2667)_8$

### Udfordringsøvelser

#### Udfordringsøvelse 1: Binære brøker

1. I et binært tal repræsenterer cifrene til venstre for decimalpunktet $(1,2,4,8, \ldots)-\left(2^0, 2^1, 2^2, 2^3, \ldots\right)$. Hvad tror du cifrene til højre for decimalpunktet repræsenterer? Beregn værdierne svarende til de første 4 cifre.

    ??? answer "&nbsp;"

        $\frac{1}{2}-0.5 ; \quad \frac{1}{4}-0.25 ; \quad \frac{1}{8}-0.125 ; \quad \frac{1}{16}-0.0625$

2. Konverter 0.75 til binær.

    ??? answer "&nbsp;"

        $0.11_2$

3. Konverter 14.6875 til binær.

    ??? answer "&nbsp;"

        $1110.1011_2$

#### Udfordringsøvelse 2: Base32

I nogle sammenhænge er det en fordel at bruge endnu flere end 16 symboler til at repræsentere tal - for eksempel tillader dette at generere kortere web-adresser. Et valg er base32, hvor den mest populære kodning (RFC 4648) er som vist i tabellen nedenfor (bemærk, at symbolerne "0" og "1" ikke bruges. Dette skyldes deres lighed med bogstaverne "O" og "I"):

| 0 | A | 8 | I | 16 | Q | 24 | Y |
| :--- | :--- | ---: | :--- | :--- | :--- | :--- | :--- |
| 1 | B | 9 | J | 17 | R | 25 | Z |
| 2 | C | 10 | K | 18 | S | 26 | 2 |
| 3 | D | 11 | L | 19 | T | 27 | 3 |
| 4 | E | 12 | M | 20 | U | 28 | 4 |
| 5 | F | 13 | N | 21 | V | 29 | 5 |
| 6 | G | 14 | O | 22 | W | 30 | 6 |
| 7 | H | 15 | P | 23 | X | 31 | 7 |

1. Konverter tallet $L 5 T_{32}$ til decimal.

    ??? answer "&nbsp;"

        $12211$

2. Konverter tallet 93678 til base32.

    ??? answer "&nbsp;"

        $C3PO_{32}$

3. Konvertering mellem binær og hexadecimal er let, fordi hver ciffer i hexadecimal svarer til præcis fire cifre i binær. Er der en lignende symmetri mellem binær og base32?

    ??? answer "&nbsp;"

        Hver ciffer i base32 svarer til fem cifre i binær.

4. Konverter $1001011011_2$ til base32.

    ??? answer "&nbsp;"

        $S3_{32}$

5. Konverter $BATMAN_{32}$ til binær.

    ??? answer "&nbsp;"

        $0000100000010011011000000001101_2$

#### Udfordringsøvelse 3: Shannons Entropi

I informationsteori er Shannons entropi et mål for usikkerheden i et sæt af mulige udfald. Den er defineret som:

$$H(X) = -\sum_{i=1}^{n} p(x_i) \log_2 p(x_i)$$

hvor $H(X)$ er entropien af den tilfældige variabel $X$, $p(x_i)$ er sandsynligheden for udfald $x_i$, og summen tages over alle mulige udfald. Bemærk, at på grund af base 2 i logaritmen vil svaret være i bits, men du kan også beregne det i andre enheder.

Du kan også tænke på det som et mål for den gennemsnitlige mængde information produceret af en stokastisk datakilde.

Bemærk: Når vi taler om flere kast eller andre hændelser i træk, antages det altid, at disse hændelser er uafhængige, medmindre andet er angivet.

1. Beregn entropien af et fair møntkast. (2 lige sandsynlige udfald, 50% chance for krone, 50% chance for plat)

    ??? answer "&nbsp;"
    
        1 bit

2. Beregn entropien af et biased 70:30 møntkast med en præcision på 4 decimaler. (2 udfald, 70% chance for krone, 30% chance for plat)

    ??? answer "&nbsp;"

        0.8813 bits

3. Beregn entropien af at rulle en fair sekssidet terning. (6 lige sandsynlige udfald, hver med 1/6 chance)

    ??? answer "&nbsp;"

        2.5850 bits

4. Beregn den samlede entropi af 100 biased 1:99 møntkast. (1% chance for krone, 99% chance for plat)

    ??? answer "&nbsp;"

        ca. 8 bits (8.0793)

#### Udfordringsøvelse 4: Entropi anvendelse

Almindelige nemme-at-implementere strategier for at lagre en serie af hændelsesresultater inkluderer at lagre et tal, der repræsenterer resultatet af hændelsen for hver hændelse, eller at lagre en liste af bits, der repræsenterer de mulige udfald med kun det endelige udfaldsbit sat til 1. Som du ved nu, er disse strategier måske ikke de mest effektive måder at lagre information på, især når udfaldene af hændelserne ikke er lige sandsynlige. I denne øvelse skal du prøve at tænke på kreative løsninger til at optimere sådanne problemer.

1. Hvis du havde 128 møntkast, og alle ville resultere i krone, undtagen præcis ét, der ville resultere i plat, hvad er den mindste mængde plads i bits, som du kunne lagre resultatet af alle kast i? (rækkefølge betyder noget)

    ??? answer "&nbsp;"

        7 bits

2. Hvad er nogle strategier, der bruger så lidt plads som muligt, når du lagrer udfaldene? Sigte efter at opnå det teoretiske minimum eller i det mindste så lidt som muligt.

    ??? answer "&nbsp;"

        For eksempel at lagre kun positionen af platten som et 7-bit tal (1-128). På denne måde kan vi rekonstruere alle 128 kastresultater ved for eksempel at gå fra 1 til 128 og tjekke, om positionen matcher det lagrede tal. Hvis ja, kan vi udskrive plat, ellers krone.

3. Gentag det samme for kun 100 møntkast, hvad er den mindste mængde plads i bits, som du kunne lagre resultatet af alle kast i? (rækkefølge betyder noget)

    ??? answer "&nbsp;"

        6.6439 bits

4. De fleste digitale systemer i det virkelige liv bruger binære tal til at lagre information. For hver ciffer er der 2 mulige tilstande. Kan informationen om de 100 kast nævnt tidligere lagres med perfekt effektivitet i binær? (Hint: tænk på antallet af udfald, din lagring kan repræsentere, og hvad det betyder at være effektiv i disse termer)

    ??? answer "&nbsp;"

        Nej. Vi kan kun bruge et naturligt antal bits, og enten kan vi repræsentere flere eller færre end 100 udfald. At være effektiv i dette tilfælde betyder at kunne repræsentere præcis 100 udfald uden spildt plads.

5. Hvilket talsystem kunne du bruge i stedet for at lagre informationen mere effektivt? (Hint: prøv at ændre base af logaritmen, når du beregner entropien, søg efter hele tal resultater)

    ??? answer "&nbsp;"

        Base 10 og base 100 opnår begge den samme perfekte effektivitet i dette tilfælde. Begge kan repræsentere 100 udfald med et helt antal cifre (ingen rest betyder ingen spildt plads). Bemærk, at blandede baser også kan bruges til at opnå denne effektivitet, og for at finde alle mulige baser skal du blot finde alle divisorer af 100. (undtagen unary, som ikke rigtig ville være egnet til dette)

#### Udfordringsøvelse 5: Entropi Avanceret

I den sidste øvelse var det garanteret at få præcis ét plat i serien af møntkast. Nu dropper vi den garanti og beregner i stedet entropien af en serie af 100 biased møntkast (99% chance for krone, 1% chance for plat).

1. Beregn entropien af en serie af 100 biased møntkast.

    ??? answer "&nbsp;"

        ca. 8 bits (8.0793)

2. Forestil dig, at vi ville fortsætte med at kaste mønten for evigt. Kan du bruge en lignende strategi til at lagre disse udfald sammenlignet med den tidligere øvelse? Ville det have den samme effektivitet?

    ??? answer "&nbsp;"

        Ja, så længe du tager højde for, at vi må fortsætte med at tilføje til denne lagring. Et eksempel på en strategi ville være at lagre tallene i 9-bit blokke, der repræsenterer, hvor mange krone der er kastet mellem platene. Hvis tallet er for stort, fylder vi blot blokken med 1'er og afslutter den i den næste blok på 9 bits.

        Effektiviteten ville nærme sig at være den samme, husk at entropien handler om gennemsnit, og over tid ville vi nærme os det teoretiske minimum eller potentialet af vores strategi, men vi kan ikke garantere, at de næste par kast ikke bare er plat, hvilket hæmmer vores pladsbesparende strategier.

3. Prøv at lave et par af disse uretfærdige kast i en tilfældig talgenerator og prøv at bruge din strategi. Ville du spare plads sammenlignet med fx. at lagre hvert kast som én bit? (hvis ikke, prøv at fortsætte og se, om det forbedres)