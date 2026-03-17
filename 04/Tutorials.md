<h1 align="center">Tutorial 4: Kombinatorik og Sandsynlighed</h1>

Efter denne tutorial vil du kunne:

*   Forstå og anvende multiplikationsreglen og additionsreglen til at tælle udfald.
*   Beregne permutationer og kombinationer både med og uden gentagelse.
*   Arbejde med grundlæggende sandsynlighedsbegreber som forsøg, udfaldsrum og hændelser.
*   Beregne sandsynligheder for hændelser, komplementer, foreninger og forskelle mellem hændelser.
*   Forstå forskellen mellem uafhængige og afhængige hændelser.
*   Anvende kombinatorik og sandsynlighed til praktiske problemer i softwareudvikling.

## 1. Grundlæggende Tælleprincipper

#### Multiplikationsreglen

Hvis en opgave kan opdeles i $k$ trin, hvor det første trin kan udføres på $n_1$ måder, det andet trin på $n_2$ måder, osv., så kan hele opgaven udføres på $n_1 \cdot n_2 \cdot \ldots \cdot n_k$ måder.

**Eksempel:** En digital enhed kan specificeres med:

- 5 hukommelsesstørrelser
- 3 skærmtyper  
- 4 lagerstørrelser
- 2 muligheder for pen (med eller uden)

Antal forskellige systemer: $5 \cdot 3 \cdot 4 \cdot 2 = 120$

#### Additionsreglen

Hvis en opgave kan udføres på $k$ forskellige måder, hvor hver mulighed er gensidigt udelukkende, og der er $n_1$ måder at udføre den første på, $n_2$ måder at udføre den anden på, osv., så kan opgaven udføres på $n_1 + n_2 + \ldots + n_k$ måder i alt.

**Eksempel:** En studerende kan vælge mellem:

- 3 matematikkurser
- 4 programmeringskurser
- 2 designkurser

Antal forskellige kurser: $3 + 4 + 2 = 9$

Som det fremgår, er additionsreglen ret triviel.

## 2. Permutationer

#### Permutationer uden gentagelse

En **permutation** er en ordnet arrangement af elementer. Der er to hovedtyper:

**1. Arrangement af alle n elementer:**
Antallet af måder at arrangere alle $n$ elementer i rækkefølge er:

$$n! = n \cdot (n-1) \cdot (n-2) \cdot \ldots \cdot 2 \cdot 1$$

**Eksempel:** Hvor mange måder kan 4 personer sidde omkring et bord?

$$4! = 4 \cdot 3 \cdot 2 \cdot 1 = 24$$

**2. Arrangement af r elementer valgt fra n elementer:**
Antallet af permutationer af $r$ elementer valgt fra $n$ elementer er:

$$P(n,r) = P^n_r = \frac{n!}{(n-r)!}$$

Bemærk at $P(n,n) = \frac{n!}{0!} = n!$ (da $0! = 1$).

**Eksempel:** Hvor mange måder kan man vælge og arrangere 3 forskellige elektroniske komponenter (fx modstand, kondensator, diode) i rækkefølge fra en kasse med 15 forskellige komponenter?

$$P(15,3) = \frac{15!}{12!} = 15 \cdot 14 \cdot 13 = 2730$$

#### Permutationer med gentagelse

Når elementer kan vælges flere gange, er antallet af permutationer:

$$n^r$$

**Eksempel:** En pinkode med 4 cifre, hvor hvert ciffer kan være 0-9:

$$10^4 = 10,000 \text{ mulige koder}$$

#### Permutationer med ens elementer

Hvis der er $n$ elementer hvor $n_1$ er ens af type 1, $n_2$ er ens af type 2, osv., så er antallet af forskellige permutationer:

$$\frac{n!}{n_1! \cdot n_2! \cdot \ldots \cdot n_k!}$$

## 3. Kombinationer

#### Kombinationer uden gentagelse

En **kombination** er en uordnet udvælgelse af elementer. Antallet af kombinationer af $r$ elementer valgt fra $n$ elementer er:

$$C(n,r) = C^n_r = \binom{n}{r} = \frac{n!}{r!(n-r)!}$$

**Specielle tilfælde:**

- $\binom{n}{0} = 1$ (vælg ingen elementer)
- $\binom{n}{n} = 1$ (vælg alle elementer)
- $\binom{n}{1} = n$ (vælg ét element)

**Eksempel:** Hvor mange måder kan 3 børn vælges (uden rækkefølge) fra en klasse på 15 børn?

$$\binom{15}{3} = \frac{15 \cdot 14 \cdot 13}{3 \cdot 2 \cdot 1} = 455$$

#### Kombinationer med gentagelse

Når elementer kan gentages, er antallet af kombinationer:

$$\binom{n+r-1}{r}$$

#### Vigtige egenskaber ved binomialkoefficienter

- $\binom{n}{0} = 1$ og $\binom{n}{n} = 1$
- $\binom{n}{r} = \binom{n}{n-r}$ (symmetri)
- $\binom{n}{r} = \binom{n-1}{r-1} + \binom{n-1}{r}$ (Pascals trekant)

## 4. Grundlæggende Sandsynlighedsbegreber

#### Forsøg og Udfaldsrum

Et **forsøg** er en proces der frembringer et udfald. **Udfaldsrummet** $S$ er mængden af alle mulige udfald.

**Eksempel:** Kast med en terning

- Udfaldsrum: $S = \{1, 2, 3, 4, 5, 6\}$

#### Hændelser

En **hændelse** $E$ er en delmængde af udfaldsrummet $S$.

**Eksempel:** For terningkast

- $A = \{2, 4, 6\}$ (lige tal)
- $B = \{1, 3, 5\}$ (ulige tal)

#### Sandsynlighed

For lige sandsynlige udfald er sandsynligheden for hændelse $E$:

$$P(E) = \frac{|E|}{|S|} = \frac{\text{antal gunstige udfald}}{\text{antal mulige udfald}}$$

**Eksempel:** Sandsynligheden for at få et lige tal ved terningkast:

$$P(A) = \frac{3}{6} = \frac{1}{2}$$

## 5. Sandsynlighedsregler

#### Grundlæggende egenskaber

1. **Ikke-negativitet:** $0 \leq P(E) \leq 1$ for enhver hændelse $E$
2. **Normalisering:** $P(S) = 1$
3. **Additivitet:** For disjunkte hændelser $E_1$ og $E_2$: $P(E_1 \cup E_2) = P(E_1) + P(E_2)$

#### Komplementreglen

$$P(E^c) = 1 - P(E)$$

hvor $E^c$ er komplementet til $E$.

**Eksempel:** Sandsynligheden for ikke at få et lige tal:

$$P(A^c) = 1 - \frac{1}{2} = \frac{1}{2}$$

#### Forening af hændelser

For to hændelser $E_1$ og $E_2$:

$$P(E_1 \cup E_2) = P(E_1) + P(E_2) - P(E_1 \cap E_2)$$

**Eksempel:** Lad $E_1$ = "få mindst 4" og $E_2$ = "få et lige tal" ved terningkast.

- $E_1 = \{4, 5, 6\}$, $P(E_1) = \frac{3}{6} = \frac{1}{2}$
- $E_2 = \{2, 4, 6\}$, $P(E_2) = \frac{3}{6} = \frac{1}{2}$
- $E_1 \cap E_2 = \{4, 6\}$, $P(E_1 \cap E_2) = \frac{2}{6} = \frac{1}{3}$

$$P(E_1 \cup E_2) = \frac{2}{3}$$

## 6. Uafhængige og Afhængige Hændelser

#### Uafhængige hændelser

To hændelser $E_1$ og $E_2$ er **uafhængige** hvis:

$$P(E_1 \cap E_2) = P(E_1) \cdot P(E_2)$$

**Eksempel:** Kast med to terninger

- $E_1$ = "første terning viser 6"
- $E_2$ = "anden terning viser 6"

$$P(E_1) = P(E_2) = \frac{1}{6}$$
$$P(E_1 \cap E_2) = \frac{1}{36} = \frac{1}{6} \cdot \frac{1}{6}$$

Derfor er $E_1$ og $E_2$ uafhængige.

#### Afhængige hændelser

Hvis $P(E_1 \cap E_2) \neq P(E_1) \cdot P(E_2)$, så er hændelserne afhængige.

**Eksempel:** Træk to kort fra et kortspil uden tilbagelægning

- $E_1$ = "første kort er spar"
- $E_2$ = "andet kort er spar"

$$P(E_1) = \frac{13}{52} = \frac{1}{4}$$

$$P(E_2|E_1) = \frac{12}{51}$$

$$P(E_1 \cap E_2) = \frac{1}{4} \cdot \frac{12}{51} = \frac{12}{204}$$

## 7. Betinget Sandsynlighed

#### Definition

Den betingede sandsynlighed for $E_2$ givet $E_1$ er:

$$P(E_2|E_1) = \frac{P(E_1 \cap E_2)}{P(E_1)}$$

**Eksempel:** En urne indeholder 5 røde og 7 blå kugler. Træk to kugler uden tilbagelægning.

Hvad er sandsynligheden for at den anden kugle er rød, givet at den første kugle var rød?

**Løsning:**

Lad $E_1$ = "første kugle er rød" og $E_2$ = "anden kugle er rød"

- $P(E_1) = \frac{5}{12}$ (5 røde ud af 12 kugler)
- $P(E_1 \cap E_2) = \frac{5}{12} \cdot \frac{4}{11} = \frac{20}{132}$ (begge røde)

Den betingede sandsynlighed er:

$$P(E_2|E_1) = \frac{P(E_1 \cap E_2)}{P(E_1)} = \frac{\frac{20}{132}}{\frac{5}{12}} = \frac{20}{132} \cdot \frac{12}{5} = \frac{4}{11}$$

Dette giver mening, fordi efter at have trukket en rød kugle, er der 4 røde kugler tilbage ud af 11 kugler i alt.

## 8. Fødselsdagsparadokset

Hvor mange personer skal være i et rum, så sandsynligheden for at mindst to har samme fødselsdag overstiger 0.5?

**Løsning:**  

$$P(\text{mindst to ens}) = 1 - P(\text{alle forskellige})$$

$$P(\text{alle forskellige}) = \frac{365 \cdot 364 \cdot \ldots \cdot (365-n+1)}{365^n}$$

For $n = 23$: $P \approx 0.507$

## 9. Anvendelse i Softwareudvikling

#### Algoritmisk kompleksitet

- **Permutationer:** Bruges til at vurdere hvor mange mulige ordnede arrangementer en algoritme skal gennemløbe, fx ved brute-force søgning i et kodeordssystem eller ved generering af alle mulige ruter i et ruteplanlægningsproblem.  
- **Kombinationer:** Hjælper med at beregne antallet af mulige valg i optimeringsproblemer, fx hvor mange forskellige sæt af funktioner der kan vælges til en softwarekonfiguration.

#### Datastrukturer

- **Hash-tabeller:** Sandsynligheden for kollisioner i hash-funktioner kan modelleres med sandsynlighedsteori og fødselsdagsparadokset. Det giver indsigt i hvor stor en tabel skal være for at minimere risikoen for kollisioner.  
- **B-træer og andre søgetræer:** Forventet søgetid og balance kan analyseres ud fra sandsynlighedsfordelinger af inddata, hvilket hjælper med at vælge den rette datastruktur til opgaven.

#### Kryptografi og sikkerhed

- **Adgangskoder:** Kombinatorik bruges til at beregne styrken af adgangskoder (antal mulige kombinationer). Jo flere muligheder, jo sværere er det at gætte en adgangskode ved brute-force.  
- **Kryptografiske hash-funktioner:** Sandsynligheden for at to forskellige inddata giver samme hash (kollision) kan estimeres med sandsynlighedsteori, hvilket er vigtigt for sikkerhedsvurdering.  
- **Nøglelængder i kryptering:** Antallet af mulige nøgler vokser eksponentielt med nøglelængden, hvilket kan forklares med multiplikationsreglen.

#### Test og kvalitetssikring

- **Kombinatorisk test:** Bruges til at sikre, at alle vigtige kombinationer af input-parametre bliver testet, fx når en funktion skal virke på tværs af forskellige browsere, styresystemer og hardwarekonfigurationer.  
- **Monte Carlo test:** Sandsynlighedsbaserede metoder anvendes til at simulere tusindvis af tilfældige scenarier og dermed opdage fejl, som deterministiske tests måske overser.

#### Maskinlæring og dataanalyse

- **Bayesiansk inferens:** Baseret på betinget sandsynlighed, anvendes til at opdatere sandsynligheder for hypoteser, når nye data observeres.  
- **Klassifikation:** Mange klassifikationsalgoritmer (fx Naive Bayes) bygger direkte på sandsynlighedsteori.  
- **Overfitting og generalisering:** Sandsynlighedsbegreber bruges til at forstå og modellere usikkerheden i træning og test af modeller.  
- **Stokastiske algoritmer:** Mange ML-metoder (fx stochastic gradient descent) anvender sandsynlighed for at gøre optimering effektiv på store datamængder.

## Opsummering

I denne tutorial har du lært:

1. **Tælleprincipper** (multiplikation og addition) til at beregne antal muligheder
2. **Permutationer** og **kombinationer** til at tælle ordnede og uordnede valg
3. **Sandsynlighed** til at kvantificere usikkerhed
4. **Uafhængighed** og **betinget sandsynlighed** som nøglebegreber
5. **Praktiske anvendelser** i softwareudvikling og datalogi

## Almindelige Faldgruber

*   **Permutation vs. kombination:** Permutation tager rækkefølge i betragtning, kombination gør ikke
*   **Glemsomhed om gentagelse:** Vær præcis med om elementer kan gentages
*   **Fejl i sandsynlighedsregning:** Sandsynligheder skal altid ligge mellem 0 og 1
*   **Uafhængig vs. disjunkt:** Uafhængige hændelser kan overlappe, disjunkte kan ikke
*   **Manglende fuldstændighed:** Husk at udfaldsrummet skal dække alle muligheder
