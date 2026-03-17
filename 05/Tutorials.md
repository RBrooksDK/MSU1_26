<h1 align="center">Tutorial 5: Betingede sandsynligheder og Bayes' Teorem</h1>

Efter denne tutorial vil du kunne:

*   Forstå og beregne betingede sandsynligheder.
*   Anvende loven om total sandsynlighed til at løse komplekse sandsynlighedsproblemer.
*   Forstå og anvende Bayes' teorem til at opdatere sandsynligheder baseret på nye informationer.
*   Skelne mellem uafhængige og afhængige hændelser.
*   Arbejde med kontingenstabeller til at organisere og analysere sandsynlighedsdata.
*   Anvende betingede sandsynligheder og Bayes' teorem til at løse problemer i softwareudvikling.

## 1. Betinget Sandsynlighed

Betinget sandsynlighed måler sandsynligheden for en hændelse, givet at en anden hændelse allerede er indtruffet. Dette er fundamentalt for at forstå, hvordan information påvirker vores sandsynlighedsberegninger.

#### Definition af Betinget Sandsynlighed

For to hændelser $A$ og $B$ med $P(B) > 0$, er den betingede sandsynlighed for $A$ givet $B$ defineret som:

$$P(A|B) = \frac{P(A \cap B)}{P(B)}$$

#### Vigtige Egenskaber

*   $P(A|B) \geq 0$ for alle hændelser $A$ og $B$
*   $P(S|B) = 1$ hvor $S$ er udfaldsrummet
*   Hvis $A_1, A_2, \ldots$ er disjunkte hændelser, så er $P(\bigcup_{i=1}^{\infty} A_i | B) = \sum_{i=1}^{\infty} P(A_i | B)$

#### Eksempel: Betinget Sandsynlighed

Antag at vi kaster to terninger. Hvad er sandsynligheden for at summen er 7, givet at den første terning viser 4?

**Løsning:**

Lad $A$ = "summen er 7" og $B$ = "første terning viser 4"

Vi skal finde $P(A|B) = \frac{P(A \cap B)}{P(B)}$

**Trin 1:** Find $P(B)$ - sandsynligheden for at første terning viser 4: $P(B) = \frac{1}{6}$

**Trin 2:** Find $P(A \cap B)$ - sandsynligheden for at summen er 7 OG første terning viser 4
For at summen skal være 7 når første terning viser 4, skal anden terning vise 3.
Der er kun ét gunstig udfald: (4,3): $P(A \cap B) = \frac{1}{36}$

**Trin 3:** Beregn den betingede sandsynlighed

$$P(A|B) = \frac{P(A \cap B)}{P(B)} = \frac{\frac{1}{36}}{\frac{1}{6}} = \frac{1}{36} \cdot \frac{6}{1} = \frac{6}{36} = \frac{1}{6}$$

**Resultat:** Sandsynligheden for at summen er 7, givet at første terning viser 4, er $\frac{1}{6}$.

## 2. Loven om Total Sandsynlighed

Loven om total sandsynlighed er et kraftfuldt værktøj til at beregne sandsynligheden for en hændelse, når vi kender de betingede sandsynligheder givet forskellige disjunkte hændelser.

#### Sætning: Loven om Total Sandsynlighed

Lad $B_1, B_2, \ldots, B_n$ være en partition af udfaldsrummet $S$ (dvs. ${B_1, \ldots, B_n}$ er en disjunkt og komplet opdeling af $S$). For enhver hændelse $A$:

$$P(A) = \sum_{i=1}^{n} P(A|B_i) \cdot P(B_i)$$

#### Eksempel 1: Loven om Total Sandsynlighed

En fabrik producerer chips på tre maskiner. Maskine 1 producerer 50% af chipsene med 2% defekte. Maskine 2 producerer 30% med 3% defekte. Maskine 3 producerer 20% med 1% defekte. Hvad er sandsynligheden for at en tilfældig chip er defekt?

**Løsning:**

Lad $D$ = "chip er defekt" og $M_i$ = "chip kommer fra maskine $i$"

Vi har:

*   $P(M_1) = 0.5$, $P(D|M_1) = 0.02$
*   $P(M_2) = 0.3$, $P(D|M_2) = 0.03$
*   $P(M_3) = 0.2$, $P(D|M_3) = 0.01$

Ved loven om total sandsynlighed:

$$P(D) = P(D|M_1) \cdot P(M_1) + P(D|M_2) \cdot P(M_2) + P(D|M_3) \cdot P(M_3)$$

$$P(D) = 0.02 \cdot 0.5 + 0.03 \cdot 0.3 + 0.01 \cdot 0.2 = 0.01 + 0.009 + 0.002 = 0.021$$

#### Eksempel 2: Loven om Total Sandsynlighed med Studerende

Antag at vi har en gruppe studerende hvor 60% er mænd og 40% er kvinder. Af mændene studerer 70% datalogi, mens 50% af kvinderne studerer datalogi. Hvad er sandsynligheden for at en tilfældig studerende studerer datalogi?

**Løsning:**

Lad $M$ = "studerende er mand" og $D$ = "studerende studerer datalogi"

Vi har:

*   $P(M) = 0.6$
*   $P(M^c) = 0.4$ (kvinde)
*   $P(D|M) = 0.7$
*   $P(D|M^c) = 0.5$

Vi skal finde $P(D)$ ved hjælp af loven om total sandsynlighed:

$$P(D) = P(D|M) \cdot P(M) + P(D|M^c) \cdot P(M^c)$$

$$P(D) = 0.7 \cdot 0.6 + 0.5 \cdot 0.4 = 0.42 + 0.20 = 0.62$$

**Resultat:** Sandsynligheden for at en tilfældig studerende studerer datalogi er 62%.

## 3. Bayes' Teorem

Bayes' teorem giver os mulighed for at "vende" betingede sandsynligheder - at opdatere vores tro på en hændelse baseret på nye beviser.

#### Sætning: Bayes' Teorem

For to hændelser $A$ og $B$ med $P(B) > 0$:

$$P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)}$$

Hvis vi har en partition $B_1, B_2, \ldots, B_n$ af udfaldsrummet, kan vi skrive:

$$P(B_i|A) = \frac{P(A|B_i) \cdot P(B_i)}{\sum_{j=1}^{n} P(A|B_j) \cdot P(B_j)}$$

#### Eksempel: Bayes' Teorem - Medicinsk Test

En medicinsk test for en sygdom har følgende egenskaber:

*   Sandsynligheden for positiv test givet sygdom: 95%
*   Sandsynligheden for positiv test givet ingen sygdom: 2%
*   Forekomst af sygdommen i befolkningen: 1%

Hvad er sandsynligheden for at en person har sygdommen, givet at testen er positiv?

**Løsning:**

Lad $S$ = "person har sygdommen" og $T^+$ = "test er positiv"

Vi har:

*   $P(S) = 0.01$ (a priori sandsynlighed - sandsynligheden før vi har nogen information)
*   $P(T^+|S) = 0.95$ (sensitivitet)
*   $P(T^+|S^c) = 0.02$ (falsk positiv-rate)

Vi skal finde $P(S|T^+)$ (a posteriori sandsynlighed - sandsynligheden efter vi har fået information om testresultatet).

Først finder vi $P(T^+)$ ved loven om total sandsynlighed:

$$P(T^+) = P(T^+|S) \cdot P(S) + P(T^+|S^c) \cdot P(S^c)$$

$$P(T^+) = 0.95 \cdot 0.01 + 0.02 \cdot 0.99 = 0.0095 + 0.0198 = 0.0293$$

Nu anvender vi Bayes' teorem:

$$P(S|T^+) = \frac{P(T^+|S) \cdot P(S)}{P(T^+)} = \frac{0.95 \cdot 0.01}{0.0293} \approx 0.3239$$

Dette betyder, at selv med en positiv test, er der kun 32.39% sandsynlighed for at personen faktisk har sygdommen!

## 4. Uafhængighed af Hændelser

To hændelser er uafhængige, hvis forekomsten af den ene ikke påvirker sandsynligheden for den anden.

#### Definition af Uafhængighed

To hændelser $A$ og $B$ er uafhængige hvis og kun hvis:

$$P(A \cap B) = P(A) \cdot P(B)$$

Dette er ækvivalent med:

*   $P(A|B) = P(A)$ (hvis $P(B) > 0$)
*   $P(B|A) = P(B)$ (hvis $P(A) > 0$)

#### Eksempel: Test for Uafhængighed

Antag at vi kaster to terninger. Lad $A$ = "første terning viser 6" og $B$ = "summen er 7". Er $A$ og $B$ uafhængige?

**Løsning:**

*   $P(A) = \frac{1}{6}$
*   $P(B) = \frac{6}{36} = \frac{1}{6}$ (der er 6 måder at få sum 7 på)
*   $P(A \cap B) = \frac{1}{36}$ (kun (6,1) giver både første terning = 6 og sum = 7)

Vi tjekker: $P(A) \cdot P(B) = \frac{1}{6} \cdot \frac{1}{6} = \frac{1}{36} = P(A \cap B)$

Da $P(A \cap B) = P(A) \cdot P(B)$, er $A$ og $B$ uafhængige.

## 5. Kontingenstabeller

Kontingenstabeller er en effektiv måde at organisere og analysere data med to kategoriske variable.

#### Struktur af Kontingenstabeller

En kontingenstabel har følgende struktur:

|           | Kategori B₁ | Kategori B₂ | ... | Total |
|-----------|-------------|-------------|-----|-------|
| Kategori A₁ | n₁₁        | n₁₂         | ... | n₁₊   |
| Kategori A₂ | n₂₁        | n₂₂         | ... | n₂₊   |
| ...       | ...         | ...         | ... | ...   |
| Total     | n₊₁         | n₊₂         | ... | n     |

#### Sandsynlighedsberegninger fra Kontingenstabeller

Fra en kontingenstabel kan vi beregne:

*   **Marginale sandsynligheder**: $P(A_i) = \frac{n_{i+}}{n}$, $P(B_j) = \frac{n_{+j}}{n}$
*   **Fælles sandsynligheder**: $P(A_i \cap B_j) = \frac{n_{ij}}{n}$
*   **Betingede sandsynligheder**: $P(A_i|B_j) = \frac{n_{ij}}{n_{+j}}$, $P(B_j|A_i) = \frac{n_{ij}}{n_{i+}}$

#### Eksempel: Kontingenstabel

En undersøgelse af 200 studerende gav følgende resultater:

|           | Datalogi | Ingeniør | Økonomi | Total |
|-----------|----------|----------|---------|-------|
| Mand      | 30       | 40       | 20      | 90    |
| Kvinde    | 25       | 35       | 50      | 110   |
| Total     | 55       | 75       | 70      | 200   |

Find sandsynligheden for at en tilfældig studerende er kvinde, givet at de studerer økonomi.

**Løsning:**

$P(\text{Kvinde}|\text{Økonomi}) = \frac{50}{70} = \frac{5}{7} \approx 0.714$

## 6. Anvendelser i Softwareudvikling

Betingede sandsynligheder og Bayes' teorem har mange praktiske anvendelser i softwareudvikling:

#### Machine Learning og Klassifikation

*   **Naive Bayes klassifikatorer** bruger Bayes' teorem til at klassificere data
*   **Spam-filtrering** anvender betingede sandsynligheder til at vurdere om en email er spam
*   **Anbefalingssystemer** bruger betingede sandsynligheder til at forudsige brugerpræferencer

#### Fejlfinding og Debugging

*   **Fejlanalyse** kan bruge Bayes' teorem til at identificere mest sandsynlige fejlkilder
*   **Performance monitoring** anvender betingede sandsynligheder til at forudsige systemfejl

#### Sikkerhed og Risikovurdering

*   **Intrusion detection** bruger betingede sandsynligheder til at identificere mistænkelig aktivitet
*   **Risk assessment** anvender Bayes' teorem til at opdatere risikovurderinger baseret på nye data

#### Eksempel: Spam-filtrering

En spam-filter analyserer emails baseret på nøgleord. Antag:

*   10% af alle emails er spam
*   Hvis en email er spam, indeholder den ordet "gratis" med sandsynlighed 60%
*   Hvis en email ikke er spam, indeholder den ordet "gratis" med sandsynlighed 5%

Hvad er sandsynligheden for at en email er spam, givet at den indeholder ordet "gratis"?

**Løsning:**

Lad $S$ = "email er spam" og $G$ = "email indeholder 'gratis'"

Vi har:

*   $P(S) = 0.1$
*   $P(G|S) = 0.6$
*   $P(G|S^c) = 0.05$

Ved loven om total sandsynlighed:

$$P(G) = P(G|S) \cdot P(S) + P(G|\overline{S}) \cdot P(\overline{S}) = 0.6 \cdot 0.1 + 0.05 \cdot 0.9 = 0.06 + 0.045 = 0.105$$

Ved Bayes' teorem:

$$P(S|G) = \frac{P(G|S) \cdot P(S)}{P(G)} = \frac{0.6 \cdot 0.1}{0.105} \approx 0.5714$$

Der er 57.14% sandsynlighed for at emailen er spam, givet at den indeholder ordet "gratis".

## Opsummering

I denne tutorial har vi udforsket de fundamentale koncepter inden for betingede sandsynligheder og Bayes' teorem:

*   **Betinget sandsynlighed** måler sandsynligheden for en hændelse givet information om en anden hændelse
*   **Loven om total sandsynlighed** giver os mulighed for at beregne sandsynligheder ved at opdele problemet i disjunkte tilfælde
*   **Bayes' teorem** tillader os at opdatere vores tro baseret på nye beviser
*   **Uafhængighed** af hændelser er vigtig for at forstå, hvornår information ikke påvirker sandsynligheder
*   **Kontingenstabeller** er et praktisk værktøj til at organisere og analysere sandsynlighedsdata

Disse koncepter er afgørende for moderne softwareudvikling, især inden for machine learning, dataanalyse og risikovurdering.

## Almindelige Faldgruber

*   **Forveksling af $P(A|B)$ og $P(B|A)$**: Husk at rækkefølgen betyder noget i betingede sandsynligheder
*   **Glemme at tjekke uafhængighed**: Antag ikke automatisk at hændelser er uafhængige
*   **Fejl i loven om total sandsynlighed**: Sørg for at partitionen dækker hele udfaldsrummet
*   **Forkert anvendelse af Bayes' teorem**: Husk at beregne $P(B)$ korrekt først
*   **Fortolkning af a posteriori sandsynligheder**: Forstå forskellen mellem a priori og a posteriori sandsynligheder