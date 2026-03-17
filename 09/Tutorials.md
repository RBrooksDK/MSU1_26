<h1 align="center">Tutorial 1: Matrix Algebra</h1>

Efter denne tutorial vil du kunne:

*   Udføre grundlæggende matrix-aritmetik, herunder addition, subtraktion og skalarmultiplikation.
*   Forstå og anvende matrixmultiplikation korrekt.
*   Arbejde med matrixpotenser og den transponerede af en matrix.
*   Bestemme, om en matrix er invertibel.
*   Find den inverse af en 2x2 og en n x n matrix.
*   Anvende matrixinverser til at løse lineære ligningssystemer.
*   Forstå og anvende "The Invertible Matrix Theorem".

## 1. Matrix-aritmetik

Matrix-aritmetik dækker over de grundlæggende operationer som addition, subtraktion, skalarmultiplikation og matrixmultiplikation. Disse operationer er fundamentale for at kunne manipulere og kombinere matricer i mere komplekse sammenhænge, såsom løsning af ligningssystemer.

### 1.1 Addition og Skalarmultiplikation

**Matrixaddition:**

Summen af to matricer, A og B, af samme dimension (m x n), er en ny m x n matrix, hvor hvert element er summen af de korresponderende elementer i A og B.

$$
A+B=\begin{bmatrix}
a_{11}+b_{11} & \cdots & a_{1n}+b_{1n} \\
\vdots & \ddots & \vdots \\
a_{m1}+b_{m1} & \cdots & a_{mn}+b_{mn}
\end{bmatrix}
$$

**Skalarmultiplikation:**

Produktet af en skalar *c* og en matrix A er en ny matrix, hvor hvert element i A er multipliceret med *c*.

$$
cA=\begin{bmatrix}
ca_{11} & \cdots & ca_{1n} \\
\vdots & \ddots & \vdots \\
ca_{m1} & \cdots & ca_{mn}
\end{bmatrix}
$$

**Eksempel på matrixaddition og skalarmultiplikation:**

Lad $A = \begin{bmatrix}-5 & 2 & 0 \\ 7 & -3 & 4 \\ -1 & 3 & 2\end{bmatrix}$ og $B = \begin{bmatrix}0 & -1 & 8 \\ 6 & -14 & 2 \\ 9 & 5 & 1\end{bmatrix}$.

Beregn $A+B$ og $3A$:

**Løsning:**

$$
A+B = \begin{bmatrix}-5+0 & 2+(-1) & 0+8 \\ 7+6 & -3+(-14) & 4+2 \\ -1+9 & 3+5 & 2+1\end{bmatrix} = \begin{bmatrix}-5 & 1 & 8 \\ 13 & -17 & 6 \\ 8 & 8 & 3\end{bmatrix}
$$

$$
3A = \begin{bmatrix}3(-5) & 3(2) & 3(0) \\ 3(7) & 3(-3) & 3(4) \\ 3(-1) & 3(3) & 3(2)\end{bmatrix} = \begin{bmatrix}-15 & 6 & 0 \\ 21 & -9 & 12 \\ -3 & 9 & 6\end{bmatrix}
$$

### 1.2 Matrixmultiplikation

Matrixmultiplikation er mere komplekst. Produktet AB af to matricer A og B er kun defineret, hvis antallet af søjler i A er lig med antallet af rækker i B.

**Definition af matrixmultiplikation:**

Hvis A er en m x n matrix og B er en n x p matrix, så er produktet AB en m x p matrix. Hver indgang (i, j) i AB er prikproduktet af den i'te række i A og den j'te søjle i B.

**Eksempel på matrixmultiplikation:**

Lad $A = \begin{bmatrix}1 & 2 & -2 \\ 1 & 1 & -3\end{bmatrix}$ og $B = \begin{bmatrix}-4 & 2 & 4 & -4 \\ -1 & -5 & -3 & 3 \\ -4 & -4 & -3 & -1\end{bmatrix}$.

Beregn $AB$:

**Løsning:**

A er en 2x3 matrix og B er en 3x4 matrix. Antallet af søjler i A (3) er lig med antallet af rækker i B (3), så produktet er defineret. Resultatet vil være en 2x4 matrix.

$$
AB = \begin{bmatrix}
(1)(-4)+(2)(-1)+(-2)(-4) & (1)(2)+(2)(-5)+(-2)(-4) & (1)(4)+(2)(-3)+(-2)(-3) & (1)(-4)+(2)(3)+(-2)(-1) \\
(1)(-4)+(1)(-1)+(-3)(-4) & (1)(2)+(1)(-5)+(-3)(-4) & (1)(4)+(1)(-3)+(-3)(-3) & (1)(-4)+(1)(3)+(-3)(-1)
\end{bmatrix}
$$

$$
AB = \begin{bmatrix}2 & 0 & 4 & 4 \\ 7 & 9 & 10 & 2\end{bmatrix}
$$

Bemærk at produktet $BA$ ikke er defineret, da antallet af søjler i B (4) ikke er lig med antallet af rækker i A (2).

## 2. Matrixpotenser og Transponering

**Matrixpotens:**

For en kvadratisk matrix A (n x n) defineres den k'te potens af A som produktet af A med sig selv k gange.

$$
A^k = \underbrace{A \cdot A \cdot \ldots \cdot A}_{k \text{ gange}}
$$

**Transponering:**

Den transponerede af en m x n matrix A, betegnet $A^T$, er en n x m matrix, hvor rækkerne i A bliver til søjlerne i $A^T$.

**Eksempel på transponering:**

Lad $A = \begin{bmatrix}-2 & 1 & 0 \\ 3 & -1 & -3\end{bmatrix}$.

**Løsning:**

$$
A^T = \begin{bmatrix}-2 & 3 \\ 1 & -1 \\ 0 & -3\end{bmatrix}
$$

En vigtig egenskab ved transponering er $(AB)^T = B^T A^T$.

## 3. Invertible Matricer

En n x n matrix A kaldes invertibel (eller ikke-singulær), hvis der findes en n x n matrix C, således at $AC = CA = I_n$, hvor $I_n$ er identitetsmatricen. C kaldes den inverse af A og betegnes $A^{-1}$.

### 3.1 Inversen af en 2x2 Matrix

For en 2x2 matrix $A = \begin{bmatrix}a & b \\ c & d\end{bmatrix}$ er den inverse givet ved:

$$
A^{-1} = \frac{1}{ad-bc} \begin{bmatrix}d & -b \\ -c & a\end{bmatrix}
$$

Dette er kun muligt, hvis determinanten af A, `det(A) = ad-bc`, ikke er nul.

**Eksempel på inversen af en 2x2 matrix:**

Find inversen af $A = \begin{bmatrix}1 & 2 \\ 3 & 4\end{bmatrix}$.

**Løsning:**

Determinanten er `det(A) = (1)(4) - (2)(3) = 4 - 6 = -2`.

$$
A^{-1} = \frac{1}{-2} \begin{bmatrix}4 & -2 \\ -3 & 1\end{bmatrix} = \begin{bmatrix}-2 & 1 \\ \frac{3}{2} & -\frac{1}{2}\end{bmatrix}
$$

### 3.2 Inversen af en n x n Matrix

For at finde inversen af en større kvadratisk matrix A, kan man benytte følgende algoritme:

1.  Opstil den udvidede matrix $[A | I_n]$.
2.  Anvend rækkeoperationer for at reducere A til $I_n$.
3.  Den resulterende matrix til højre vil være $A^{-1}$, altså $[I_n | A^{-1}]$.

**Eksempel på inversen af en 3x3 matrix:**

Find inversen af $A = \begin{bmatrix}1 & 0 & -2 \\ -3 & 1 & 4 \\ 2 & -3 & 4\end{bmatrix}$.

**Løsning:**

Opstil den udvidede matrix og rækkereducer:

$$
\left[\begin{array}{ccc|ccc}
1 & 0 & -2 & 1 & 0 & 0 \\
-3 & 1 & 4 & 0 & 1 & 0 \\
2 & -3 & 4 & 0 & 0 & 1
\end{array}\right] \sim \left[\begin{array}{ccc|ccc}
1 & 0 & 0 & 8 & 6 & 2 \\
0 & 1 & 0 & 20 & 8 & 2 \\
0 & 0 & 1 & \frac{7}{2} & \frac{3}{2} & \frac{1}{2}
\end{array}\right]
$$

(De mellemliggende rækkeoperationer er udeladt for korthedens skyld)

Den inverse er:

$$
A^{-1} = \begin{bmatrix}8 & 6 & 2 \\ 20 & 8 & 2 \\ \frac{7}{2} & \frac{3}{2} & \frac{1}{2}\end{bmatrix}
$$

## 4. Løsning af Matrixligninger med Inverser

Hvis A er en invertibel matrix, har ligningen $A\mathbf{x} = \mathbf{b}$ en unik løsning givet ved $\mathbf{x} = A^{-1}\mathbf{b}$.

**Eksempel på løsning af ligningssystem:**

Løs systemet:
$8x_1 + 6x_2 = 2$
$5x_1 + 4x_2 = -1$

**Løsning:**

Systemet kan skrives som $A\mathbf{x} = \mathbf{b}$, hvor $A = \begin{bmatrix}8 & 6 \\ 5 & 4\end{bmatrix}$, $\mathbf{x} = \begin{bmatrix}x_1 \\ x_2\end{bmatrix}$ og $\mathbf{b} = \begin{bmatrix}2 \\ -1\end{bmatrix}$.

Find først $A^{-1}$:
`det(A) = (8)(4) - (6)(5) = 32 - 30 = 2`.

$$
A^{-1} = \frac{1}{2} \begin{bmatrix}4 & -6 \\ -5 & 8\end{bmatrix} = \begin{bmatrix}2 & -3 \\ -\frac{5}{2} & 4\end{bmatrix}
$$

Løsningen er $\mathbf{x} = A^{-1}\mathbf{b}$:

$$
\mathbf{x} = \begin{bmatrix}2 & -3 \\ -\frac{5}{2} & 4\end{bmatrix} \begin{bmatrix}2 \\ -1\end{bmatrix} = \begin{bmatrix}(2)(2)+(-3)(-1) \\ (-\frac{5}{2})(2)+(4)(-1)\end{bmatrix} = \begin{bmatrix}7 \\ -9\end{bmatrix}
$$

Så $x_1 = 7$ og $x_2 = -9$.

## 5. The Invertible Matrix Theorem

Dette teorem samler en række ækvivalente udsagn for en kvadratisk matrix. Hvis ét af udsagnene er sandt, er de alle sande.

**The Invertible Matrix Theorem (uddrag):**

For en n x n matrix A er følgende udsagn ækvivalente:

*   A er en invertibel matrix.
*   A er rækkeækvivalent med $I_n$.
*   A har n pivotpositioner.
*   Ligningen $A\mathbf{x} = \mathbf{0}$ har kun den trivielle løsning.
*   Søjlerne i A er lineært uafhængige.
*   Ligningen $A\mathbf{x} = \mathbf{b}$ har mindst én løsning for ethvert $\mathbf{b}$ i $\mathbb{R}^n$.
*   $A^T$ er en invertibel matrix.

## Opsummering

Denne tutorial har introduceret de centrale begreber inden for matrix algebra:

*   **Matrix-aritmetik:** Addition, subtraktion, skalarmultiplikation og matrixmultiplikation.
*   **Matrixpotenser og transponering:** Potenser af kvadratiske matricer og den transponerede af en matrix.
*   **Invertible matricer:** Definition, egenskaber og metoder til at finde den inverse.
*   **Løsning af ligningssystemer:** Anvendelse af matrixinverser til at finde unikke løsninger.
*   **The Invertible Matrix Theorem:** En samling af ækvivalente betingelser for invertibilitet.

Disse værktøjer er essentielle for at kunne arbejde effektivt med komplekse lineære systemer.

## Almindelige Faldgruber

*   **Dimensioner ved multiplikation:** Husk at antallet af søjler i den første matrix skal matche antallet af rækker i den anden.
*   **Rækkefølgen af matrixmultiplikation:** Generelt er $AB \neq BA$.
*   **Invers af produkt:** Husk reglen $(AB)^{-1} = B^{-1}A^{-1}$.
*   **Ikke-kvadratiske matricer:** Kun kvadratiske matricer kan have en invers.
*   **Singulære matricer:** En matrix med en determinant på nul er ikke invertibel.