---
tags:
    - Sandsynlighed
    - Betinget Sandsynlighed
    - Bayes' Teorem
    - Afhængige Hændelser
    - Uafhængige Hændelser
    - Kontingenstabeller
    - Skæring af Hændelser
    - Stokastiske Processer
---

<h1 align="center">Øvelser 1:<br>Betingede sandsynligheder og Bayes' teorem</h1>

I skal lave øvelserne inden timerne torsdag. I kan med fordel lave dem i grupper og diskutere dem indbyrdes. Det er vigtigt, at I forstår opgaverne og kan forklare dem til hinanden. På torsdag diskuterer vi opgaverne, og I skal være klar til at præsentere dem for klassen.

<style>
body[data-md-color-scheme] .md-content ol       { list-style-type: lower-alpha; }
body[data-md-color-scheme] .md-content ol li    { padding-left: 10px; }
</style>

#### Øvelse 1: Repetition

Lad $A$ og $B$ være to hændelser sådan at:

$$
P(A)=0.3, \quad P(B)=0.2, \quad P(A \cap B)=0.1
$$

Find sandsynlighederne nedenfor. Angiv dine svar korrekte til én decimal.

1. Find $P(A^c)$. (1)
{ .annotate }

    1. $P(A^c)=0.7$.

2. Find $P\left(A \cup B\right)$. (1)
{ .annotate }

    1. $P\left(A \cup B\right)=0.4$.

3. Find $P\left(A^c \cap B\right)$. (1)
{ .annotate }

    1. $P\left(A^c \cap B\right)=0.1$

4. Find $P\left(A \cap B^c\right)$. (1)
{ .annotate }

    1. $P\left(A \cap B^c\right)=0.2$.

5. Find $P\left((A \cup B)^c\right)$. (1)
{ .annotate }

    1. $P\left((A \cup B)^c\right)=0.6$.

6. Find $P\left(A^c \cup B\right)$. (1)
{ .annotate }

    1. $P\left(A^c \cup B\right)=0.8$.

#### Øvelse 2: Kast med fair terning

Jeg kaster en fair terning to gange og får to tal: $X_1=$ resultatet af første kast, $X_2=$ resultatet af andet kast.

1. Find sandsynligheden for at $X_2=4$. (1)
{ .annotate }

    1. $\dfrac{1}{6}$

2. Find sandsynligheden for at $X_1+X_2=7$. (1)
{ .annotate }

    1. $\dfrac{1}{6}$

3. Find sandsynligheden for at $X_1 \neq 2$ og $X_2 \geq 4$. (1)
{ .annotate }

    1. $\dfrac{5}{12}$

#### Øvelse 3: Venn og sandsynlighed

Lad $A, B$ og $C$ være tre hændelser med sandsynligheder givet:

<img src="../src/venn1.png" width = "200">

Find sandsynlighederne nedenfor. Angiv dine svar som uforkortelige brøker.

1. $P(A \mid B)$ (1)
{ .annotate }

    1. $\dfrac{4}{7}$

2. $P(C \mid B)$ (1)
{ .annotate }

    1. $\dfrac{3}{7}$

3. $P(B \mid A \cup C)$ (1)
{ .annotate }

    1. $\dfrac{5}{14}$

4. $P(B \mid (A, C))$ (1)
{ .annotate }

    1. $\dfrac{1}{2}$

#### Øvelse 4: Flere fly
Sandsynligheden for at et regelmæssigt planlagt fly afgår til tiden er $0.83$; sandsynligheden for at det ankommer til tiden er $0.82$; og sandsynligheden for at det afgår og ankommer til tiden er $0.78$. Find sandsynligheden for at et fly (angiv dine svar korrekte til fire decimaler):

1. Ankommer til tiden, givet at det afgik til tiden (1)
{ .annotate }

    1. 0.9398

1. Afgik til tiden, givet at det har ankommet til tiden (1)
{ .annotate }

    1. 0.9512

1. Ankommer til tiden, givet at det ikke afgik til tiden (1)
{ .annotate }

    1. 0.2353

#### Øvelse 5: Uafhængighed og kontingenstabeller
En undersøgelse blev gennemført for at bestemme beskæftigelsesgraden for nyligt dimitterede ingeniørstuderende. Undersøgelsen blev gennemført ét år efter dimission og blev lavet for ICT-ingeniører, Bygningsingeniører, Maskiningeniører og Global Business Engineers. De dimitterede blev klassificeret i en af to beskæftigelseskategorier: (1) beskæftiget/studerende og (2) arbejdsløs. 40% af respondenterne havde studeret ICT-ingeniør og af disse var 85% beskæftiget/studerende. Af alle respondenterne var 20% arbejdsløse. Af de 100 tidligere bygningsingeniørstuderende, der deltog i undersøgelsen, var 20% arbejdsløse. Andelen af arbejdsløse maskin- og bygningsingeniørstuderende var den samme, og undersøgelsen inkluderede præcis 9 arbejdsløse maskiningeniørstuderende. 300 studerende deltog i undersøgelsen.

1. Baseret på disse oplysninger, konstruer en 2 x 4 kontingenstabel for undersøgelsesresultaterne.

    ??? answer "&nbsp;"
        <img src="../src/contingency.png" width = "300">

        Teknisk set er summerne og totalerne ikke en del af kontingenstabellerne. De tilføjes for at gøre det nemmere at beregne sandsynlighederne.


2. Hvad er sandsynligheden for at en arbejdsløs respondent er en tidligere ICT-studerende? Angiv dit svar som en uforkortelig brøk. (1)
{ .annotate }

    1. $\dfrac{3}{10}$

3. Hvis en respondent er arbejdsløs, hvad er sandsynligheden for at respondenten var en GBE-studerende? Angiv dit svar som en uforkortelig brøk. (1)
{ .annotate }

    1. $\dfrac{13}{60}$

4. Er det at være arbejdsløs uafhængigt af at være en tidligere ICT-studerende?

    ??? answer "&nbsp;"
        Du kan sammenligne enhver a priori sandsynlighed med den tilsvarende a posteriori sandsynlighed. F.eks. fandt du en a posteriori sandsynlighed på $\dfrac{3}{10}$ i (b). Den a priori sandsynlighed er $\dfrac{2}{5}$. Da de to sandsynligheder ikke er lige store, er de to hændelser afhængige:

        $P(\text{ICT} \mid \text{Arbejdsløs}) = \dfrac{3}{10} \neq \dfrac{2}{5} = P(\text{ICT})$

#### Øvelse 6: Bayes' teorem
Sygdom $A$ forekommer med sandsynlighed 0.1, og sygdom $B$ forekommer med sandsynlighed 0.2. Det er ikke muligt at have begge sygdomme. Du har en enkelt test. Denne test rapporterer positiv med sandsynlighed 0.8 for en patient med sygdom $A$, med sandsynlighed 0.5 for en patient med sygdom $B$, og med sandsynlighed 0.01 for en patient uden sygdom - kald sidstnævnte hændelse $W$. Ved at angive dit svar korrekt til fire decimaler, hvis testen kommer tilbage positiv, hvad er sandsynligheden for at du har enten:

1. Sygdom $A$ (1)
{ .annotate }

    1. $0.4278$

2. Sygdom $B$ (1)
{ .annotate }

    1. $0.5348$

3. Ingen sygdom (1)
{ .annotate }

    1. $0.0374$

### Udfordringsøvelser

#### Udfordringsøvelse 1

Brug kun tid på denne øvelse, hvis du har tid tilbage efter at have fuldført de andre øvelser, og du fandt dem for nemme. Problemet er taget fra eksamen i Stokastisk Modellering og Processer (IT-SMP1) på 6./7. semester.

Du vælger et punkt $(A, B)$ ensartet tilfældigt i enhedskvadraten $\{(x, y): 0 \leq x, y \leq 1\}$.

<p align="center">
    <img src="../src/challenge.png" width="200">
</p>

Hvad er sandsynligheden for at ligningen

$$
A X^2+X+B=0
$$

har reelle løsninger?

[Løsning](Solution7.pdf)

#### Udfordringsøvelse 2: Binomisk Sætning

Binomisk udvidelsesformel:

$$
(a+b)^n=\sum_{k=0}^n\binom{n}{k} a^{n-k} b^k
$$


$$
(a+b)^n=\binom{n}{0} a^n+\binom{n}{1} a^{n-1} b+\binom{n}{2} a^{n-2} b^2+\ldots+\binom{n}{n} b^n,
$$

hvor $\binom{n}{k}=\frac{n!}{k!(n-k)!}$ er den binomiske koefficient
Den generelle term i den binomiske udvidelse:

$$
T_{k+1}=\binom{n}{k} a^{n-k} b^k, \quad k=0,1,2 \ldots, n
$$

Vigtig egenskab: Antallet af termer i den binomiske udvidelse af $(a+b)^n$ er $n+1$.

1. Skriv den binomiske udvidelse af $(a+2 b)^4$. Hint: Du kan bruge Pascals trekant til nemt at skrive de binomiske koefficienter ned.

    ??? answer "&nbsp;"

        1. $a^4+8 a^3 b+24 a^2 b^2+32 a b^3+16 b^4$

2. Find den 5. term i udvidelsen af $(\sqrt{x}+x)^{10}$

    ??? answer "&nbsp;"

        1. $210 x^7$

3. Bestem termen, der indeholder $x^6$ i udvidelsen af $\left(x+\frac{1}{2} y\right)^9$.

    ??? answer "&nbsp;"

        1. $\frac{21}{2} x^{6} y^{3}$

#### Udfordringsøvelse 3: Monty Hall Problemet

Monty Hall problemet er et berømt sandsynlighedspuslespil baseret på et spilshow-scenarie. Sådan fungerer det:

1. Du præsenteres for tre døre: bag en dør er en bil (præmien, du ønsker), og bag de to andre døre er geder (som du ikke ønsker).
2. Du vælger en dør (sig, Dør 1).
3. Værten, som ved, hvad der er bag hver dør, åbner en anden dør (sig, Dør 3), som har en ged bag sig.
4. Du får derefter valget mellem at holde fast ved dit oprindelige valg (Dør 1) eller skifte til den resterende uåbnede dør (Dør 2).

Spørgsmålet er: Skal du holde fast ved dit oprindelige valg, skifte til den anden dør, eller betyder det ikke noget?
For at løse dette problem kan vi analysere sandsynlighederne for at vinde bilen baseret på din strategi (at holde fast eller skifte).

1. Hvad er sandsynligheden for at vinde bilen, hvis du holder fast ved dit oprindelige valg? (1)
{ .annotate }

    1. \(\dfrac{1}{3}\)

2. Hvad er sandsynligheden for at vinde bilen, hvis du skifter til den anden dør? (1)
{ .annotate }

    1. \(\dfrac{2}{3}\)

3. Hvad ville sandsynligheden for at vinde være, hvis der var 100 døre, med 1 bil og 99 geder, og efter du vælger en dør, åbner værten 98 døre med geder bag dem? (1)
{ .annotate }

    1. \(\dfrac{99}{100}\)

Sjov Fakta: Dette problem førte til meget debat om sandsynlighed og beslutningstagning. Problemet blev populært af Marilyn vos Savant i hendes "Ask Marilyn" kolonne i Parade magasin i 1990, hvilket førte til udbredt diskussion og analyse. 

[(YT 3 min) Monty Hall Problem - AsapSCIENCE](https://www.youtube.com/watch?v=9vRUxbzJZ9Y)

[(YT 5 min) Monty Hall Problem - Numberphile](https://www.youtube.com/watch?v=4Lb-6rxZxx0)

[(YT 15 min) Monty Hall Problem - VSauce](https://www.youtube.com/watch?v=TVq2ivVpZgQ)
