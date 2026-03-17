<h1 align="center">Tutorial 6: Beskrivende Statistik</h1>

Efter denne tutorial vil du kunne:

*   Forstå forskellen mellem population og stikprøve.
*   Klassificere data som kvalitativ eller kvantitativ (diskret eller kontinuert).
*   Oprette og fortolke frekvensfordelinger, histogrammer og ogive-diagrammer.
*   Beregne og fortolke centralmål: middelværdi, median og typetal.
*   Beregne og fortolke spredningsmål: variationsbredde, varians, standardafvigelse og interkvartilbredde.
*   Anvende den empiriske regel til normalfordelte data.
*   Identificere outliers ved hjælp af IQR-metoden.
*   Oprette og fortolke boxplots.
*   Forstå og identificere skævhed i datafordelinger.

## 1. Introduktion til Beskrivende Statistik

Beskrivende statistik handler om at organisere, præsentere og opsummere data på en meningsfuld måde. I softwareudvikling arbejder vi konstant med data: performance metrics, responstider, fejlrater osv. Beskrivende statistik giver os værktøjer til at forstå disse data uden at skulle se på hver enkelt værdi.

#### Population vs. Stikprøve

**Population:** Det komplette sæt af alle mulige observationer eller målinger i en given undersøgelse.

**Stikprøve:** En delmængde af populationen som vi faktisk observerer eller måler.

**Eksempel:** Hvis vi vil analysere responstider for en webapplikation der betjener millioner af brugere dagligt, ville **populationen** være alle mulige responstider. På grund af praktiske begrænsninger måler vi kun responstiderne for en **stikprøve** af 10.000 requests per dag.

#### Typer af Data

**Kvalitative data** (kategoriske data): Ikke-numerisk information der kan kategoriseres.

*   **Eksempler:** Programmeringssprog (Python, Java, C++), bug severity (kritisk, høj, medium, lav)

**Kvantitative data:** Numeriske målinger der kan ordnes og underkastes matematiske operationer.

*   **Diskret:** Tællelige værdier (antal bugs, linjer kode, commits per dag)
*   **Kontinuert:** Målbare værdier der kan antage enhver værdi inden for et område (responstid i ms, CPU-forbrug i %, hukommelsesbrug i MB)

## 2. Frekvensfordelinger og Visualisering

#### Frekvensfordeling

En **frekvensfordeling** viser hvor ofte hver værdi eller klasse af værdier forekommer i et datasæt.

*   **Absolut frekvens:** Det faktiske antal forekomster
*   **Relativ frekvens:** Andelen af det totale antal observationer
*   **Kumuleret relativ frekvens:** Den løbende sum af relative frekvenser

**Eksempel:** Antal fejl fundet per dag i 10 dage: {2, 3, 2, 2, 3, 2, 4, 3, 2, 3}

| Antal fejl | Frekvens | Relativ frekvens | Kumuleret relativ frekvens |
|------------|----------|------------------|----------------------------|
| 2          | 5        | 5/10 = 0.50      | 0.50                       |
| 3          | 4        | 4/10 = 0.40      | 0.90                       |
| 4          | 1        | 1/10 = 0.10      | 1.00                       |

#### Histogrammer

Et **histogram** er en grafisk repræsentation af frekvensfordelingen for grupperede data. Når data har mange forskellige værdier, grupperes de i **bins** (klasseintervaller).

**Vigtige punkter:**

*   Søjlerne i et histogram er placeret direkte ved siden af hinanden (til forskel fra et søjlediagram)
*   Højden af hver søjle repræsenterer frekvensen eller den relative frekvens
*   Typisk bruges 5-10 bins
*   Vi bruger **venstre-inklusion konvention**: Intervallet [700, 800) indeholder værdier $x$ hvor $700 \leq x < 800$

#### Ogive (Kumuleret Frekvenskurve)

Et **ogive** viser den kumulerede relative frekvens. Fra et ogive kan man nemt aflæse:

*   Medianen (ved 0.50)
*   Kvartiler (ved 0.25 og 0.75)
*   Percentiler (ved hvilken som helst værdi mellem 0 og 1)

## 3. Centralmål

Centralmål beskriver den "typiske" eller "centrale" værdi i et datasæt.

#### Middelværdi (Gennemsnit)

For et datasæt med $n$ værdier $x_1, x_2, \ldots, x_n$ er **stikprøvemiddelværdien**:

$$\bar{x} = \frac{1}{n}\sum_{i=1}^{n} x_i = \frac{x_1 + x_2 + \cdots + x_n}{n}$$

**Eksempel:** Responstider (ms): {120, 150, 180, 200, 220}

$$\bar{x} = \frac{120 + 150 + 180 + 200 + 220}{5} = \frac{870}{5} = 174 \text{ ms}$$

**Egenskaber:**

*   Tager højde for alle værdier
*   Følsom overfor outliers
*   Bedst for symmetriske fordelinger uden ekstreme værdier

#### Median

**Medianen** er den midterste værdi når data er sorteret i stigende rækkefølge.

For $n$ sorterede værdier:

$$\text{Median} = \begin{cases}
x_{\frac{n+1}{2}} & \text{hvis } n \text{ er ulige} \\
\frac{x_{\frac{n}{2}} + x_{\frac{n}{2}+1}}{2} & \text{hvis } n \text{ er lige}
\end{cases}$$

**Eksempel:** For {120, 150, 180, 200, 220} (n = 5, ulige):

$$\text{Median} = x_3 = 180 \text{ ms}$$

**Eksempel:** For {120, 150, 180, 200, 220, 250} (n = 6, lige):

$$\text{Median} = \frac{x_3 + x_4}{2} = \frac{180 + 200}{2} = 190 \text{ ms}$$

**Egenskaber:**

*   Robust overfor outliers
*   Repræsenterer midtpunktet i dataene (50% under, 50% over)
*   Bedst for skæve fordelinger eller data med outliers

#### Typetal (Modus)

**Typetallet** er den værdi der forekommer hyppigst i datasættet.

*   **Ingen modus:** Alle værdier forekommer lige ofte
*   **Unimodal:** Én værdi forekommer hyppigst
*   **Bimodal:** To værdier deler den højeste frekvens
*   **Multimodal:** Flere værdier deler den højeste frekvens

**Eksempel:** {High, Medium, Low, High, Critical, Medium, High, Low, High, Medium}

Frekvenser: High: 4, Medium: 3, Low: 2, Critical: 1

**Typetal:** High (forekommer 4 gange)

**Egenskaber:**

*   Særligt nyttigt for kategoriske data
*   Kan bruges til diskret kvantitativ data
*   Kan være ikke-eksisterende eller ikke-unik

## 4. Spredningsmål

Spredningsmål beskriver hvor spredte dataene er.

#### Variationsbredde (Range)

**Variationsbredden** er forskellen mellem den største og mindste værdi:

$$\text{Variationsbredde} = x_{\max} - x_{\min}$$

**Eksempel:** For {120, 150, 180, 200, 350}:

$$\text{Variationsbredde} = 350 - 120 = 230 \text{ ms}$$

**Egenskaber:**

*   Simpel at beregne
*   Meget følsom overfor outliers
*   Giver ingen information om fordelingen mellem ekstremerne

#### Varians og Standardafvigelse

**Stikprøvevariansen** måler den gennemsnitlige kvadrerede afvigelse fra middelværdien:

$$s^2 = \frac{1}{n-1}\sum_{i=1}^{n}(x_i - \bar{x})^2$$

**Stikprøvestandardafvigelsen** er kvadratroden af variansen:

$$s = \sqrt{s^2} = \sqrt{\frac{1}{n-1}\sum_{i=1}^{n}(x_i - \bar{x})^2}$$

Standardafvigelsen har samme enhed som data og repræsenterer den typiske afstand fra middelværdien.

**Eksempel:** For {5, 6, 7, 8, 9} med $\bar{x} = 7$:

$$s^2 = \frac{1}{4}[(5-7)^2 + (6-7)^2 + (7-7)^2 + (8-7)^2 + (9-7)^2]$$

$$s^2 = \frac{1}{4}[4 + 1 + 0 + 1 + 4] = \frac{10}{4} = 2.5$$

$$s = \sqrt{2.5} \approx 1.58$$

**Beregningsformel (alternativ):** 

$$s^2 = \frac{1}{n-1}\left(\sum_{i=1}^n x_i^2 - \frac{(\sum_{i=1}^n x_i)^2}{n}\right)$$

Denne formel er ofte nemmere at bruge ved håndberegning.

#### Kvartiler og Interkvartilbredde

**Kvartiler** opdeler sorterede data i fire lige store dele:

*   **Q1 (Første kvartil):** 25. percentil - 25% af data er mindre
*   **Q2 (Anden kvartil):** 50. percentil - dette er medianen
*   **Q3 (Tredje kvartil):** 75. percentil - 75% af data er mindre

**Interkvartilbredden (IQR)** måler spredningen af de midterste 50% af data:

$$\text{IQR} = Q_3 - Q_1$$

**Eksempel:** For {120, 150, 180, 200, 220, 250, 280, 300, 350, 400}:

*   Nedre halvdel: {120, 150, 180, 200, 220} → Q1 = 180 (median af nedre halvdel)
*   Øvre halvdel: {250, 280, 300, 350, 400} → Q3 = 300 (median af øvre halvdel)
*   IQR = 300 - 180 = 120 ms

**Egenskaber:**

*   Robust overfor outliers
*   Beskriver spredningen af den centrale del af dataene

## 5. Den Empiriske Regel (68-95-99.7 Reglen)

For **cirka normalfordelte data** gælder den empiriske regel:

*   Cirka **68.3%** af observationerne ligger inden for $\bar{x} \pm s$
*   Cirka **95.4%** af observationerne ligger inden for $\bar{x} \pm 2s$
*   Cirka **99.7%** af observationerne ligger inden for $\bar{x} \pm 3s$

**Eksempel:** Et system har middelværdi = 200 ms og standardafvigelse = 30 ms.

*   68.3% ligger i [200 - 30, 200 + 30] = [170, 230] ms
*   95.4% ligger i [200 - 60, 200 + 60] = [140, 260] ms
*   99.7% ligger i [200 - 90, 200 + 90] = [110, 290] ms

En responstid på 290 ms ligger 3 standardafvigelser fra middelværdien og er derfor usædvanlig.

## 6. Outlier-detektion

**Outliers** er datapunkter der er markant forskellige fra resten af dataene.

#### 1.5 × IQR Metoden

*   **Milde outliers:** Værdier mindre end $Q_1 - 1.5 \times \text{IQR}$ eller større end $Q_3 + 1.5 \times \text{IQR}$
*   **Ekstreme outliers:** Værdier mindre end $Q_1 - 3 \times \text{IQR}$ eller større end $Q_3 + 3 \times \text{IQR}$

**Eksempel:** Med Q1 = 180, Q3 = 300, IQR = 120:

*   Nedre grænse for milde outliers: 180 - 1.5(120) = 0
*   Øvre grænse for milde outliers: 300 + 1.5(120) = 480
*   Værdier > 480 eller < 0 er milde outliers

**Vigtigt:** Outliers kan være:

*   Målefejl eller datainputfejl → skal muligvis fjernes
*   Ægte usædvanlige hændelser → kan være de vigtigste datapunkter at analysere
*   I softwareudvikling kan outliers indikere performance-problemer, bugs eller sikkerhedsbrud

## 7. Boxplots

Et **boxplot** (kassediagram) giver et visuelt resumé af datafordelingen:

**Komponenter:**

*   **Boks:** Strækker sig fra Q1 til Q3 (indeholder de midterste 50% af data)
*   **Median-linje:** En linje inde i boksen ved medianen
*   **Whiskers (antenner):** Linjer fra boksen til minimum og maksimum (ekskl. outliers)
*   **Outliers:** Punkter uden for whiskers (> Q3 + 1.5 × IQR eller < Q1 - 1.5 × IQR)

**Fortolkning af boxplot:**

*   **Længden af boksen** (IQR): Viser spredningen af de centrale data
*   **Position af medianlinje:** Viser symmetri/skævhed
*   **Længde af whiskers:** Viser spredningen af ekstreme værdier
*   **Outliers:** Identificerer usædvanlige observationer

## 8. Skævhed i Datafordelinger

#### Symmetrisk Fordeling

I en **symmetrisk fordeling** er data jævnt fordelt omkring centrum:

*   Middelværdi ≈ Median ≈ Typetal
*   Whiskers i boxplot er ca. lige lange
*   Histogram ser symmetrisk ud

#### Højreskæv Fordeling (Positiv Skævhed)

En **højreskæv fordeling** har en lang højre hale:

*   Middelværdi > Median > Typetal
*   Højre whisker er længere end venstre
*   Histogram har en lang højre hale
*   Eksempel: Indkomster, responstider (nogle få meget høje værdier)

#### Venstreskæv Fordeling (Negativ Skævhed)

En **venstreskæv fordeling** har en lang venstre hale:

*   Typetal > Median > Middelværdi
*   Venstre whisker er længere end højre
*   Histogram har en lang venstre hale
*   Eksempel: Alder ved pensionering (de fleste går på pension omkring samme alder, men nogle få går meget tidligere)

**Vigtig pointe:** I skæve fordelinger er medianen ofte et bedre centralmål end middelværdien, da medianen ikke påvirkes af ekstreme værdier.

## 9. Normalfordeling

En **normalfordeling** (også kaldet Gauss-fordeling eller klokke-kurve) er en symmetrisk, klokkeformet fordeling hvor:

*   Middelværdi = Median = Typetal
*   Cirka 68% af data ligger inden for ±1 standardafvigelse fra middelværdien
*   Cirka 95% ligger inden for ±2 standardafvigelser
*   Cirka 99.7% ligger inden for ±3 standardafvigelser

Mange data i naturen og i softwareudvikling tilnærmer normalfordelingen, hvilket gør den meget nyttig til analyse og modellering.

## Opsummering

I denne tutorial har du lært de grundlæggende værktøjer til beskrivende statistik:

*   **Datatyper:** Kvalitativ vs. kvantitativ (diskret/kontinuert)
*   **Visualisering:** Frekvensfordelinger, histogrammer, ogives, boxplots
*   **Centralmål:** Middelværdi, median, typetal
*   **Spredningsmål:** Variationsbredde, varians, standardafvigelse, IQR
*   **Analyse:** Den empiriske regel, outlier-detektion, skævhed

Disse værktøjer er fundamentale for at forstå og analysere data i softwareudvikling, fra performance metrics til brugeradfærd.

## Almindelige Faldgruber

*   **Forveksling af population og stikprøve:** Husk at konklusioner fra en stikprøve kun er valide hvis stikprøven er repræsentativ.
*   **Brug af middelværdi ved skæve fordelinger:** Brug median når data har outliers eller er skæve.
*   **Glemme enheder:** Varians har kvadrerede enheder, standardafvigelse har samme enheder som data.
*   **Forkert fortolkning af percentiler:** 75. percentil betyder at 75% af data er **mindre end eller lig** denne værdi.
*   **Automatisk fjernelse af outliers:** Outliers kan indikere vigtige problemer og bør undersøges før de fjernes.
*   **Antagelse om normalfordeling:** Ikke alle data er normalfordelte - tjek altid før du anvender den empiriske regel.
