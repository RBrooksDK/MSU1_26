<h1 align="center">Tutorial 7: Lineær Algebra og Ligningssystemer</h1>

Efter denne tutorial vil du kunne:

*   Forstå og arbejde med matricer og deres operationer.
*   Identificere echelon form og reduceret echelon form af matricer.
*   Udføre elementære rækkeoperationer korrekt.
*   Løse systemer af lineære ligninger ved hjælp af række-reduktion.
*   Fortolke løsninger til lineære systemer (unik løsning, uendeligt mange løsninger, ingen løsning).
*   Anvende lineær algebra til praktiske problemer i softwareudvikling.
*   Arbejde med augmenterede matricer og pivot-positioner.

## 1. Introduktion til Lineær Algebra

Lineær algebra er fundamentet for moderne datavidenskab og softwareudvikling. Fra machine learning algoritmer til grafiske transformationer i spil og 3D-modellering - lineær algebra er overalt i softwareudvikling.

#### Hvad er et System af Lineære Ligninger?

Et **system af lineære ligninger** er en samling af ligninger hvor hver ligning er lineær (ingen variable er opløftet til potenser højere end 1).

**Eksempel:**

$$
\begin{aligned}
2x_1 - 3x_2 + x_3 &= 5 \\
x_1 + 2x_2 - x_3 &= 1 \\
-2x_1 + x_2 + 3x_3 &= 0
\end{aligned}
$$

#### Matricer og Augmenterede Matricer

En **matrix** er en rektangulær arrangement af tal organiseret i rækker og kolonner.

**Koefficientmatrix** indeholder kun koefficienterne:

$$\begin{bmatrix} 2 & -3 & 1 \\ 1 & 2 & -1 \\ -2 & 1 & 3 \end{bmatrix}$$

**Augmenteret matrix** inkluderer også højre side af ligningerne:

$$\begin{bmatrix} 2 & -3 & 1 & 5 \\ 1 & 2 & -1 & 1 \\ -2 & 1 & 3 & 0 \end{bmatrix}$$

## 2. Elementære Rækkeoperationer

Elementære rækkeoperationer er de grundlæggende operationer vi kan udføre på en matrix uden at ændre løsningssættet til det tilsvarende ligningssystem.

#### De Tre Elementære Rækkeoperationer

**1. Swap (Ombytning):** Byt om på to rækker

$$r_i \leftrightarrow r_j$$

**2. Scaling (Skalering):** Gang en række med en konstant (ikke nul)

$$r_i \rightarrow c \cdot r_i \quad \text{hvor } c \neq 0$$

**3. Replacement (Erstatning):** Læg et multiplum af en række til en anden række

$$r_i \rightarrow r_i + c \cdot r_j$$

#### Eksempel: Rækkeoperationer

Start med matrixen:

$$\begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9 \end{bmatrix}$$

**Swap:** $r_1 \leftrightarrow r_3$

$$\begin{bmatrix} 7 & 8 & 9 \\ 4 & 5 & 6 \\ 1 & 2 & 3 \end{bmatrix}$$

**Scaling:** $r_2 \rightarrow 2 \cdot r_2$

$$\begin{bmatrix} 7 & 8 & 9 \\ 8 & 10 & 12 \\ 1 & 2 & 3 \end{bmatrix}$$

**Replacement:** $r_3 \rightarrow r_3 - 2r_1$

$$\begin{bmatrix} 7 & 8 & 9 \\ 8 & 10 & 12 \\ -13 & -14 & -15 \end{bmatrix}$$

## 3. Echelon Form og Reduceret Echelon Form

#### Echelon Form (Række-Echelon Form)

En matrix er i **echelon form** hvis:

1. Alle rækker med kun nuller er nederst
2. Den første ikke-nul element (pivot) i hver række er til højre for pivots i rækkerne ovenfor
3. Pivots behøver ikke at være 1

**Eksempel på echelon form:**

$$\begin{bmatrix} 2 & -1 & 3 & 1 \\ 0 & 3 & -2 & 4 \\ 0 & 0 & 1 & 2 \end{bmatrix}$$

#### Reduceret Echelon Form (RREF)

En matrix er i **reduceret echelon form** hvis:

1. Den er i echelon form
2. Alle pivots er 1
3. Der er kun nuller over og under hver pivot

**Eksempel på reduceret echelon form:**

$$\begin{bmatrix} 1 & 0 & 0 & 2 \\ 0 & 1 & 0 & 1 \\ 0 & 0 & 1 & 2 \end{bmatrix}$$

#### Identifikation af Matrixformer

**Eksempel:** Bestem hvilken form følgende matricer er i:

1. $\begin{bmatrix} 1 & 0 & 2 \\ 0 & 1 & -1 \\ 0 & 0 & 0 \end{bmatrix}$ → **Reduceret echelon form**

2. $\begin{bmatrix} 2 & 1 & 3 \\ 0 & 3 & -2 \\ 0 & 0 & 4 \end{bmatrix}$ → **Echelon form**

3. $\begin{bmatrix} 1 & 2 & 3 \\ 0 & 0 & 1 \\ 0 & 1 & 0 \end{bmatrix}$ → **Hverken** (pivot i række 3 er til venstre for pivot i række 2)

## 4. Række-Reduktion Algoritmen

#### Fremgangsmåde for at Få RREF

1. **Start med den første kolonne** og find den første ikke-nul element
2. **Ombyt rækker** hvis nødvendigt for at få pivot øverst
3. **Skaler** for at få pivot = 1
4. **Eliminer** alle elementer under pivots ved at bruge erstatning
5. **Gentag** for næste kolonne

#### Eksempel: Række-Reduktion

Lad os reducere følgende matrix til RREF:

$$\begin{bmatrix} 2 & -4 & 6 & 2 \\ 1 & 0 & 1 & 3 \\ -2 & 2 & 0 & 2 \end{bmatrix}$$

**Trin 1:** Ombyt rækker for at få pivot øverst

$$\begin{bmatrix} 1 & 0 & 1 & 3 \\ 2 & -4 & 6 & 2 \\ -2 & 2 & 0 & 2 \end{bmatrix}$$

**Trin 2:** Eliminer under første pivot

$$r_2 \rightarrow r_2 - 2r_1: \begin{bmatrix} 1 & 0 & 1 & 3 \\ 0 & -4 & 4 & -4 \\ -2 & 2 & 0 & 2 \end{bmatrix}$$

$$r_3 \rightarrow r_3 + 2r_1: \begin{bmatrix} 1 & 0 & 1 & 3 \\ 0 & -4 & 4 & -4 \\ 0 & 2 & 2 & 8 \end{bmatrix}$$

**Trin 3:** Arbejd med anden kolonne

$$r_2 \rightarrow -\frac{1}{4}r_2: \begin{bmatrix} 1 & 0 & 1 & 3 \\ 0 & 1 & -1 & 1 \\ 0 & 2 & 2 & 8 \end{bmatrix}$$

$$r_3 \rightarrow r_3 - 2r_2: \begin{bmatrix} 1 & 0 & 1 & 3 \\ 0 & 1 & -1 & 1 \\ 0 & 0 & 4 & 6 \end{bmatrix}$$

**Trin 4:** Arbejd med tredje kolonne

$$r_3 \rightarrow \frac{1}{4}r_3: \begin{bmatrix} 1 & 0 & 1 & 3 \\ 0 & 1 & -1 & 1 \\ 0 & 0 & 1 & 1.5 \end{bmatrix}$$

**Trin 5:** Eliminer over pivots

$$r_1 \rightarrow r_1 - r_3: \begin{bmatrix} 1 & 0 & 0 & 1.5 \\ 0 & 1 & -1 & 1 \\ 0 & 0 & 1 & 1.5 \end{bmatrix}$$

$$r_2 \rightarrow r_2 + r_3: \begin{bmatrix} 1 & 0 & 0 & 1.5 \\ 0 & 1 & 0 & 2.5 \\ 0 & 0 & 1 & 1.5 \end{bmatrix}$$

**Resultat:** Matrixen er nu i RREF med løsningen $x_1 = 1.5$, $x_2 = 2.5$, $x_3 = 1.5$.

## 5. Fortolkning af Løsninger

#### Tre Typer af Løsninger

**1. Unik Løsning**

- Der er en pivot i hver kolonne af koefficientdelen
- RREF ligner: $\begin{bmatrix} 1 & 0 & 0 & a \\ 0 & 1 & 0 & b \\ 0 & 0 & 1 & c \end{bmatrix}$

**2. Uendeligt Mange Løsninger**

- Der er mindre pivots end variabler
- Nogle variable er "frie" (kan vælges frit)
- RREF ligner: $\begin{bmatrix} 1 & 0 & 2 & a \\ 0 & 1 & -1 & b \\ 0 & 0 & 0 & 0 \end{bmatrix}$

**3. Ingen Løsning (Inkonsistent)**

- Der er en pivot i højre side af den augmenterede matrix
- RREF ligner: $\begin{bmatrix} 1 & 0 & 0 & a \\ 0 & 1 & 0 & b \\ 0 & 0 & 0 & 1 \end{bmatrix}$

#### Eksempel: Fortolkning af Løsninger

**Unik løsning:**

$$\begin{bmatrix} 1 & 0 & 0 & 2 \\ 0 & 1 & 0 & 3 \\ 0 & 0 & 1 & 1 \end{bmatrix} \Rightarrow \begin{cases} x_1 = 2 \\ x_2 = 3 \\ x_3 = 1 \end{cases}$$

**Uendeligt mange løsninger:**

$$\begin{bmatrix} 1 & 2 & 0 & 4 \\ 0 & 0 & 1 & 2 \\ 0 & 0 & 0 & 0 \end{bmatrix} \Rightarrow \begin{cases} x_1 = 4 - 2x_2 \\ x_2 \text{ fri} \\ x_3 = 2 \end{cases}$$

**Ingen løsning:**

$$\begin{bmatrix} 1 & 0 & 0 & 2 \\ 0 & 1 & 0 & 3 \\ 0 & 0 & 0 & 1 \end{bmatrix} \Rightarrow \text{Inkonsistent (0 = 1 er umuligt)}$$

## 6. Praktiske Anvendelser

#### Kostplanlægning

En softwareudvikler vil planlægge sin kost med smør, æbler og havre. Næringsværdier per 100g:

| Næringsværdier | Smør | Æble | Havre |
|----------------|------|------|-------|
| Protein (g)    | 0.2  | 0.3  | 14.0  |
| Fedt (g)       | 82.5 | 0.2  | 6.9   |
| Kulhydrater (g)| 0.0  | 12.1 | 57.0  |

**System af ligninger:**

$$
\begin{cases}
0.2x_1 + 0.3x_2 + 14.0x_3 = 50 \quad \text{(protein)} \\
82.5x_1 + 0.2x_2 + 6.9x_3 = 70 \quad \text{(fedt)} \\
0.0x_1 + 12.1x_2 + 57.0x_3 = 260 \quad \text{(kulhydrater)}
\end{cases}
$$

Dette kan løses ved række-reduktion for at finde de optimale mængder.

#### Software Performance Optimering

I softwareudvikling bruges lineære systemer til:

- **Load balancing:** Fordele requests mellem servere
- **Resource allocation:** Optimere CPU, hukommelse og disk forbrug
- **Network routing:** Finde optimale ruter i netværk
- **Machine learning:** Lineære regression og klassifikation
- **Computer graphics:** 3D transformationer og rendering

## 7. Almindelige Fejl og Faldgruber

#### Række-Reduktion Fejl

**Fejl 1:** Glemmer at skifte fortegn ved subtraktion

- **Forkert:** $r_2 \rightarrow r_2 - 3r_1$ hvor $r_1 = [1, 2, 3]$ giver $r_2 = [4, 5, 6] - [3, 6, 9] = [1, -1, -3]$
- **Korrekt:** $r_2 = [4, 5, 6] - [3, 6, 9] = [1, -1, -3]$ ✓

**Fejl 2:** Blander række- og kolonne-operationer

- **Forkert:** At bytte kolonner (ændrer løsningssættet)
- **Korrekt:** Kun række-operationer bevarer løsningssættet

**Fejl 3:** Glemmer at tjekke for inkonsistens

- **Forkert:** Fortsætter række-reduktion selv når der er pivot i højre side
- **Korrekt:** Stop når du ser en række som $[0, 0, 0, 1]$ (inkonsistent)

#### Fortolkning af Løsninger

**Fejl 4:** Forveksler frie variable

- **Forkert:** At tro at alle variable har unikke værdier
- **Korrekt:** Identificer pivots for at finde basale vs. frie variable

**Fejl 5:** Forkert identifikation af matrixformer

- **Forkert:** At tro at en matrix med pivots = 1 automatisk er RREF
- **Korrekt:** Tjek også at der kun er nuller over og under pivots

## Opsummering

I denne tutorial har du lært de grundlæggende koncepter i lineær algebra:

*   **Matricer og augmenterede matricer** - Repræsentation af lineære systemer
*   **Elementære rækkeoperationer** - Swap, scaling, replacement
*   **Echelon former** - Identifikation af matrixformer
*   **Række-reduktion** - Systematisk fremgangsmåde til RREF
*   **Løsningsfortolkning** - Unik, uendeligt mange, eller ingen løsninger
*   **Praktiske anvendelser** - Fra kostplanlægning til software optimering

Disse værktøjer er fundamentale for at forstå og løse komplekse problemer i softwareudvikling, machine learning og datavidenskab.

## Almindelige Faldgruber

*   **Række-operationer:** Blander række- og kolonne-operationer eller glemmer fortegnsregler.
*   **Matrixformer:** Forveksler echelon form med reduceret echelon form.
*   **Løsningsfortolkning:** Glemmer at identificere frie variable eller inkonsistente systemer.
*   **Pivot-identifikation:** Ikke korrekt at identificere pivot-positioner og deres betydning.
*   **Række-reduktion:** Ikke systematisk fremgangsmåde eller glemmer at tjekke for inkonsistens.
*   **Praktisk anvendelse:** Ikke at oversætte praktiske problemer til lineære systemer korrekt.