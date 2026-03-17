<h1 align="center">Tutorial 1: Vektorer og Matricer</h1>

Efter denne tutorial vil du kunne:

*   Forstå og arbejde med vektorer og matricer.
*   Konvertere mellem forskellige repræsentationer af lineære ligningssystemer.
*   Beregne lineære kombinationer af vektorer.
*   Skrive løsninger i parametrisk vektorform.
*   Løse homogene ligningssystemer.
*   Bestemme lineær uafhængighed af vektorer.
*   Anvende vektorer og matricer i praktiske sammenhænge.

## 1. Grundlæggende Vektoroperationer

En vektor er en ordnet liste af tal, der kan repræsentere positioner, retninger eller data. I denne tutorial fokuserer vi på kolonnevektorer.

**Definition af vektorer:**

$$\mathbf{v} = \begin{bmatrix}v_1\\v_2\\\vdots\\v_n\end{bmatrix}$$

**Grundlæggende operationer:**

*   **Skalarmultiplikation:** $c\mathbf{v} = \begin{bmatrix}cv_1\\cv_2\\\vdots\\cv_n\end{bmatrix}$
*   **Vektoraddition:** $\mathbf{u} + \mathbf{v} = \begin{bmatrix}u_1+v_1\\u_2+v_2\\\vdots\\u_n+v_n\end{bmatrix}$
*   **Vektorsubtraktion:** $\mathbf{u} - \mathbf{v} = \begin{bmatrix}u_1-v_1\\u_2-v_2\\\vdots\\u_n-v_n\end{bmatrix}$

**Eksempel på vektoroperationer:**

Lad $\mathbf{v}_1 = \begin{bmatrix}1\\-2\\4\end{bmatrix}$ og $\mathbf{v}_2 = \begin{bmatrix}3\\0\\2\end{bmatrix}$.

Beregn $2\mathbf{v}_1 + 3\mathbf{v}_2$:

**Løsning:**

$$2\mathbf{v}_1 + 3\mathbf{v}_2 = 2\begin{bmatrix}1\\-2\\4\end{bmatrix} + 3\begin{bmatrix}3\\0\\2\end{bmatrix} = \begin{bmatrix}2\\-4\\8\end{bmatrix} + \begin{bmatrix}9\\0\\6\end{bmatrix} = \begin{bmatrix}11\\-4\\14\end{bmatrix}$$

## 2. Matricer og Matrixoperationer

En matrix er et rektangulært array af tal organiseret i rækker og søjler.

**Matrixnotation:**

$$A = \begin{bmatrix}a_{11} & a_{12} & \cdots & a_{1n}\\a_{21} & a_{22} & \cdots & a_{2n}\\\vdots & \vdots & \ddots & \vdots\\a_{m1} & a_{m2} & \cdots & a_{mn}\end{bmatrix}$$

**Matrix-vektor multiplikation:**

$$A\mathbf{x} = \begin{bmatrix}a_{11} & a_{12} & \cdots & a_{1n}\\a_{21} & a_{22} & \cdots & a_{2n}\\\vdots & \vdots & \ddots & \vdots\\a_{m1} & a_{m2} & \cdots & a_{mn}\end{bmatrix}\begin{bmatrix}x_1\\x_2\\\vdots\\x_n\end{bmatrix} = \begin{bmatrix}a_{11}x_1 + a_{12}x_2 + \cdots + a_{1n}x_n\\a_{21}x_1 + a_{22}x_2 + \cdots + a_{2n}x_n\\\vdots\\a_{m1}x_1 + a_{m2}x_2 + \cdots + a_{mn}x_n\end{bmatrix}$$

**Eksempel på matrix-vektor multiplikation:**

Lad $A = \begin{bmatrix}2 & 3\\-1 & 4\end{bmatrix}$ og $\mathbf{x} = \begin{bmatrix}1\\-2\end{bmatrix}$.

Beregn $A\mathbf{x}$:

**Løsning:**

$$A\mathbf{x} = \begin{bmatrix}2 & 3\\-1 & 4\end{bmatrix}\begin{bmatrix}1\\-2\end{bmatrix} = \begin{bmatrix}2 \cdot 1 + 3 \cdot (-2)\\-1 \cdot 1 + 4 \cdot (-2)\end{bmatrix} = \begin{bmatrix}2 - 6\\-1 - 8\end{bmatrix} = \begin{bmatrix}-4\\-9\end{bmatrix}$$

## 3. Repræsentationer af Lineære Ligningssystemer

Et lineært ligningssystem kan repræsenteres på tre ækvivalente måder:

### 3.1 System af Ligninger

$$\begin{cases}
a_{11}x_1 + a_{12}x_2 + \cdots + a_{1n}x_n = b_1\\
a_{21}x_1 + a_{22}x_2 + \cdots + a_{2n}x_n = b_2\\
\vdots\\
a_{m1}x_1 + a_{m2}x_2 + \cdots + a_{mn}x_n = b_m
\end{cases}$$

### 3.2 Augmenteret Matrix

$$\begin{bmatrix}a_{11} & a_{12} & \cdots & a_{1n} & b_1\\a_{21} & a_{22} & \cdots & a_{2n} & b_2\\\vdots & \vdots & \ddots & \vdots & \vdots\\a_{m1} & a_{m2} & \cdots & a_{mn} & b_m\end{bmatrix}$$

### 3.3 Vektorligning

$$x_1\mathbf{a}_1 + x_2\mathbf{a}_2 + \cdots + x_n\mathbf{a}_n = \mathbf{b}$$

hvor $\mathbf{a}_j$ er $j$-te søjle i koefficientmatricen.

### 3.4 Matrixligning

$$A\mathbf{x} = \mathbf{b}$$

**Eksempel på konvertering:**

Konverter systemet:

$$\begin{cases}
2x_1 + 3x_2 - 4x_3 = 8\\
-x_2 + x_3 + 2x_4 = -2\\
-x_1 + 2x_4 = 3
\end{cases}$$

**Løsning:**

**(i) Augmenteret matrix:**

$$\begin{bmatrix}
2 & 3 & -4 & 0 & 8\\
0 & -1 & 1 & 2 & -2\\
-1 & 0 & 0 & 2 & 3
\end{bmatrix}$$

**(ii) Vektorligning:**

$$x_1\begin{bmatrix}2\\0\\-1\end{bmatrix} + x_2\begin{bmatrix}3\\-1\\0\end{bmatrix} + x_3\begin{bmatrix}-4\\1\\0\end{bmatrix} + x_4\begin{bmatrix}0\\2\\2\end{bmatrix} = \begin{bmatrix}8\\-2\\3\end{bmatrix}$$

**(iii) Matrixligning:**

$$\begin{bmatrix}
2 & 3 & -4 & 0\\
0 & -1 & 1 & 2\\
-1 & 0 & 0 & 2
\end{bmatrix}\begin{bmatrix}x_1\\x_2\\x_3\\x_4\end{bmatrix} = \begin{bmatrix}8\\-2\\3\end{bmatrix}$$

## 4. Lineære Kombinationer

En lineær kombination af vektorer $\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_k$ er et udtryk af formen:

$$c_1\mathbf{v}_1 + c_2\mathbf{v}_2 + \cdots + c_k\mathbf{v}_k$$

hvor $c_1, c_2, \ldots, c_k$ er skalarer.

**Eksempel på lineære kombinationer:**

Lad $\mathbf{v}_1 = \begin{bmatrix}1\\-2\\4\end{bmatrix}$, $\mathbf{v}_2 = \begin{bmatrix}3\\0\\2\end{bmatrix}$ og $\mathbf{v}_3 = \begin{bmatrix}-1\\5\\1\end{bmatrix}$.

Beregn $2\mathbf{v}_1 + 3\mathbf{v}_2 + \mathbf{v}_3$:

**Løsning:**

$$2\begin{bmatrix}1\\-2\\4\end{bmatrix} + 3\begin{bmatrix}3\\0\\2\end{bmatrix} + \begin{bmatrix}-1\\5\\1\end{bmatrix} = \begin{bmatrix}2\\-4\\8\end{bmatrix} + \begin{bmatrix}9\\0\\6\end{bmatrix} + \begin{bmatrix}-1\\5\\1\end{bmatrix} = \begin{bmatrix}10\\1\\15\end{bmatrix}$$

## 5. Parametrisk Vektorform

Når et lineært system har frie variable, kan løsningen skrives i parametrisk vektorform som:

$$\mathbf{x} = \mathbf{p} + t_1\mathbf{v}_1 + t_2\mathbf{v}_2 + \cdots + t_k\mathbf{v}_k$$

hvor:

- $\mathbf{p}$ er en partikulær løsning
- $t_1, t_2, \ldots, t_k$ er parametre (frie variable)
- $\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_k$ er retningsvektorer

**Eksempel på parametrisk vektorform:**

Et system har løsningen:

$$\begin{aligned}
x_1 &= 4 - x_2\\
x_2 &= x_2\\
x_3 &= -1 + 3x_2
\end{aligned}$$

hvor $x_2$ er en fri variabel.

**Parametrisk vektorform:**

$$\begin{bmatrix}x_1\\x_2\\x_3\end{bmatrix} = \begin{bmatrix}4\\0\\-1\end{bmatrix} + x_2\begin{bmatrix}-1\\1\\3\end{bmatrix}$$

**Forklaring:** Løsningen består af en "partikulær løsning" $\begin{bmatrix}4\\0\\-1\end{bmatrix}$ plus alle mulige lineære kombinationer af "retningsvektoren" $\begin{bmatrix}-1\\1\\3\end{bmatrix}$ ganget med den frie parameter $x_2$.

## 6. Homogene Ligningssystemer

Et homogent system er et system af formen $A\mathbf{x} = \mathbf{0}$.

**Vigtige egenskaber:**

- $\mathbf{x} = \mathbf{0}$ er altid en løsning (trivial løsning)
- Hvis der er ikke-trivielle løsninger, er der uendeligt mange løsninger
- Løsningsmængden er et underrum

**Eksempel på homogen ligning:**

Løs $A\mathbf{x} = \mathbf{0}$ for $A = \begin{bmatrix}4 & -8\\-3 & 6\end{bmatrix}$.

**Løsning:**

1. **Række-reduktion af $[A|\mathbf{0}]$:**

$$\begin{bmatrix}4 & -8 & 0\\-3 & 6 & 0\end{bmatrix} \sim \begin{bmatrix}1 & -2 & 0\\0 & 0 & 0\end{bmatrix}$$

2. **Løsning:**

$$\mathbf{x} = x_2\begin{bmatrix}2\\1\end{bmatrix}$$

**Forklaring:** Da $x_1 = 2x_2$ og $x_2$ er fri, kan alle løsninger skrives som multipla af vektoren $\begin{bmatrix}2\\1\end{bmatrix}$.

## 7. Lineær Uafhængighed

Vektorer $\mathbf{v}_1, \mathbf{v}_2, \ldots, \mathbf{v}_k$ er lineært uafhængige, hvis ligningen:

$$c_1\mathbf{v}_1 + c_2\mathbf{v}_2 + \cdots + c_k\mathbf{v}_k = \mathbf{0}$$

kun har den trivielle løsning $c_1 = c_2 = \cdots = c_k = 0$.

**Test for lineær uafhængighed:**

- Sæt vektorerne som søjler i en matrix $A$
- Løs $A\mathbf{x} = \mathbf{0}$
- Hvis der kun er den trivielle løsning, er vektorerne lineært uafhængige
- Hvis der er frie variable, er vektorerne lineært afhængige

**Eksempel på lineær uafhængighed:**

Bestem om $\mathbf{b} = \begin{bmatrix}8\\6\\12\end{bmatrix}$ er en lineær kombination af:
$$\mathbf{a}_1 = \begin{bmatrix}2\\3\\0\end{bmatrix}, \quad \mathbf{a}_2 = \begin{bmatrix}1\\2\\-5\end{bmatrix}, \quad \mathbf{a}_3 = \begin{bmatrix}4\\1\\2\end{bmatrix}$$

**Løsning:**

Løs systemet $x_1\mathbf{a}_1 + x_2\mathbf{a}_2 + x_3\mathbf{a}_3 = \mathbf{b}$:

**Augmenteret matrix:**

$$\begin{bmatrix}2 & 1 & 4 & 8\\3 & 2 & 1 & 6\\0 & -5 & 2 & 12\end{bmatrix}$$

**RREF:**

$$\begin{bmatrix}1 & 0 & 0 & 3\\0 & 1 & 0 & -2\\0 & 0 & 1 & 1\end{bmatrix}$$

**Løsning:** Ja, $\mathbf{b} = 3\mathbf{a}_1 - 2\mathbf{a}_2 + \mathbf{a}_3$

## Opsummering

I denne tutorial har du lært de grundlæggende koncepter inden for vektorer og matricer:

*   **Vektoroperationer:** Addition, subtraktion, skalarmultiplikation
*   **Matrix-vektor multiplikation:** Hvordan man beregner $A\mathbf{x}$
*   **Repræsentationer:** System af ligninger, augmenteret matrix, vektorligning, matrixligning
*   **Lineære kombinationer:** Hvordan man kombinerer vektorer
*   **Parametrisk vektorform:** Hvordan man skriver løsninger med frie variable
*   **Homogene systemer:** Særlige egenskaber ved $A\mathbf{x} = \mathbf{0}$
*   **Lineær uafhængighed:** Hvordan man tester om vektorer er uafhængige
*   **Praktiske anvendelser:** Computer graphics, dataanalyse, machine learning

Disse koncepter er fundamentale for forståelsen af lineær algebra og har mange praktiske anvendelser i softwareudvikling og datavidenskab.

## Almindelige Faldgruber

*   **Matrix dimensioner:** Sørg for at matrix-vektor multiplikation er defineret (antal søjler i matrix = antal rækker i vektor)
*   **Vektor notation:** Husk at arbejde med kolonnevektorer i matrixligninger
*   **Frie variable:** Når der er frie variable, er der uendeligt mange løsninger
*   **Trivial løsning:** Homogene systemer har altid $\mathbf{x} = \mathbf{0}$ som løsning
*   **Lineær uafhængighed:** Test ved at løse $A\mathbf{x} = \mathbf{0}$ - kun trivial løsning betyder uafhængighed