<h1 align="center">Øvelser 8:<br>Vektorer og matricer</h1>

I skal lave øvelserne inden timerne torsdag. I kan med fordel lave dem i grupper og diskutere dem indbyrdes. Det er vigtigt, at I forstår opgaverne og kan forklare dem til hinanden. På torsdag diskuterer vi opgaverne, og I skal være klar til at præsentere dem for klassen.

<style>
body[data-md-color-scheme] .md-content ol       { list-style-type: lower-alpha; }
body[data-md-color-scheme] .md-content ol li    { padding-left: 10px; }
</style>

#### Øvelse 1: Genopfriskning

Du får den augmenterede matrix

$A =\begin{bmatrix}
    1 &  -2 &  0 &  -1 & 1\\
    -4 &  8 &  2 &  4 & -8\\
    -2 &  4 &  0 &  1 &  -2
\end{bmatrix}$​

1. Hvad er størrelsen af matrixen? (1)
{ .annotate }

    1. $3\times5$

2. Reducer matrixen til echelonform (enten manuelt eller ved at udføre separate rækkeoperationer i Python)

    ??? answer "&nbsp;"

        Bemærk. Der er mange måder at reducere matrixen til echelonform på. Her er en måde at gøre det på.

        $\begin{bmatrix}
            1 &  -2 &  0 &  -1 & 1 \\
            0 &  0 &  2 &  0 & -4 \\
            0 &  0 &  0 &  -1 &  0
        \end{bmatrix}$

3. Brug echelonformen til at finde de basale variable og frie variable

    ??? answer "&nbsp;"

        De basale variable er $x_1$, $x_3$ og $x_4$ og den frie variabel er $x_2$

4. Find den generelle løsning til systemet og skriv de basale variable i forhold til de frie variable

    ??? answer "&nbsp;"
        Udtryk $x_1, x_3$, og $x_4$ i forhold til den frie variabel $x_2$ :
        1. Fra Række 1: $x_1-2 x_2=1 \Rightarrow x_1=2 x_2+1$
        2. Fra Række 2: $x_3=-2$
        3. Fra Række 3: $x_4=0$

5. Markér hver af følgende udsagn som SAND eller FALSK

    (i)  Matrix A beskriver et system af fem ligninger og tre variable (1)
    { .annotate }

    1. FALSK

    (ii)  Matrix A beskriver et konsistent system af ligninger (1)
    { .annotate }

    1. SAND

    (iii)  En 3x5 augmenteret matrix kan ikke have en unik løsning (1)
    { .annotate }

    1. SAND

    (iv)  En 3x5 augmenteret matrix vil altid være konsistent (1)
    { .annotate }

    1. FALSK

#### Øvelse 2: Matrix- og vektorligninger

For hvert af følgende systemer af lineære ligninger, skriv det som (i) en augmenteret matrix (ii) en vektorligning og (iii) en matrixligning.

1. $\begin{cases}
    2x_1 +3x_2 - 4x_3 =8\\
    -x_2 +x_3 + 2x_4 = -2\\
    -x_1 + 2x_4 = 3
    \end{cases}$

    ??? answer "&nbsp;"

        (i) Augmenteret matrix:
        $\begin{bmatrix}
            2 & 3 & -4 & 0 &  8\\
            0 & -1&  1 & 2 & -2\\
            -1& 0 & 0 & 2 & 3 
        \end{bmatrix}$

        (ii) Vektorligning:
        $x_1\begin{bmatrix}2\\\ 0\\\ -1\end{bmatrix} + x_2\begin{bmatrix}3\\\ -1\\\ 0\end{bmatrix}+ x_3\begin{bmatrix}-4\\\ 1\\\ 0\end{bmatrix}+ x_4\begin{bmatrix}0\\\ 2\\\ 2\end{bmatrix}=\begin{bmatrix}8\\\ -2\\\ 3\end{bmatrix}$

        (iii) Matrixligning:
        $\begin{bmatrix}
            2 & 3 & -4 & 0 \\
            0 & -1&  1 & 2 \\
            -1& 0 & 0 & 2 
        \end{bmatrix}
        \begin{bmatrix}
            x_1\\x_2\\x_3\\x_4
        \end{bmatrix}
        =
        \begin{bmatrix}
            8\\-2\\3
        \end{bmatrix}$

2. $\begin{cases}
    x_1 + x_2 = 2\\
    x_1 -x_2 = 4
    \end{cases}$

    ??? answer "&nbsp;"

        (i) Augmenteret matrix:
        $\begin{bmatrix}
            1 & 1 & 2\\
            1 & -1& 4
        \end{bmatrix}$

        (ii) Vektorligning:
        $x_1\begin{bmatrix}1\\1\end{bmatrix}+ x_2\begin{bmatrix}1\\-1\end{bmatrix}=\begin{bmatrix}2\\4\end{bmatrix}$

        (iii) Matrixligning:
        $\begin{bmatrix}
            1 & 1 \\
            1 & -1
        \end{bmatrix}
        \begin{bmatrix}
            x_1\\x_2
        \end{bmatrix}
        =
        \begin{bmatrix}
            2\\4
        \end{bmatrix}$


3. $\begin{cases}
    x_1 = 4\\
    x_2 = -1\\
    x_3 = 10
    \end{cases}$

    ??? answer "&nbsp;"

        (i) Augmenteret matrix:
        $\begin{bmatrix}
            1 & 0 & 0 & 4\\
            0 & 1 & 0 & -1\\
            0 & 0 & 1 & 10
        \end{bmatrix}$

        (ii) Vektorligning:
        $x_1\begin{bmatrix}1\\0\\0\end{bmatrix}+ x_2\begin{bmatrix}0\\1\\0\end{bmatrix}+x_3\begin{bmatrix}0\\0\\1\end{bmatrix}=\begin{bmatrix}4\\-1\\10\end{bmatrix}$

        (iii) Matrixligning:
        $\begin{bmatrix}
            1 & 0 & 0 \\
            0 & 1 & 0\\
            0 & 0 & 1
        \end{bmatrix}
        \begin{bmatrix}
            x_1\\x_2\\x_3
        \end{bmatrix}
        =
        \begin{bmatrix}
            4\\-1\\10
        \end{bmatrix}$

#### Øvelse 3: Lineære kombinationer
Lad

$\mathbf{v}_1=\begin{bmatrix}1\\ -2\\ 4\end{bmatrix}$, $\mathbf{v}_2=\begin{bmatrix}3\\ 0\\ 2\end{bmatrix}$ og $\mathbf{v}_3=\begin{bmatrix}-1\\ 5\\ 1\end{bmatrix}$.

Beregn de lineære kombinationer nedenfor.

1. $2\mathbf{v}_1+3\mathbf{v}_2+\mathbf{v}_3$


    ??? answer "&nbsp;"

        $\begin{bmatrix}10\\1\\15\end{bmatrix}$

2. $\mathbf{v}_1-\mathbf{v}_3$

    ??? answer "&nbsp;"

        $\begin{bmatrix}2\\-7\\3\end{bmatrix}$

3. $\frac{1}{2}\mathbf{v}_1+\frac{3}{2}\mathbf{v}_2+\mathbf{v}_3$

    ??? answer "&nbsp;"

        $\begin{bmatrix}4\\4\\6\end{bmatrix}$

4. Find løsningen til det lineære system beskrevet af den augmenterede matrix

    \[
    \begin{bmatrix}
        1 & 3 & -1 & 10 \\
        -2 & 0 & 5 & 1 \\
        4 & 2 & 1 & 15
    \end{bmatrix}
    \]

    ??? answer "&nbsp;"

        $\begin{cases}
        x_1 = 2\\
        x_2 = 3\\
        x_3 = 1
        \end{cases}$


#### Øvelse 4: Parametrisk vektorform
I følgende øvelser er løsningen til et sæt lineære ligninger allerede fundet. Din opgave
er at skrive løsningen på parametrisk vektorform.

1. Et system er fundet at have løsningen

    $$
    \begin{aligned}
    x_1 &= 4 - x_2 \\
    x_2 &= x_2 \\
    x_3 &= -1 + 3x_2
    \end{aligned}
    $$

    hvor $x_2$ er en fri variabel. Skriv løsningen i parametrisk vektorform.

    ??? answer "&nbsp;"
        $\left[\begin{array}{l}
        x_1 \\
        x_2 \\
        x_3
        \end{array}\right]=\left[\begin{array}{c}
        4 \\
        0 \\
        -1
        \end{array}\right]+x_2\left[\begin{array}{c}
        -1 \\
        1 \\
        3
        \end{array}\right]$

2. Et system af ligninger er fundet at have løsningen

    $$
    \begin{aligned}
    x_1 &= 5 + 4x_4 \\
    x_2 &= 2 \\
    x_3 &= x_3 \\
    x_4 &= x_4 \\
    x_5 &= -8 + x_3 - 7x_4
    \end{aligned}
    $$

    hvor $x_3$ og $x_4$ er frie variable. Skriv løsningen i parametrisk vektorform.

    ??? answer "&nbsp;"
        $\left[\begin{array}{l}
        x_1 \\
        x_2 \\
        x_3 \\
        x_4 \\
        x_5
        \end{array}\right]=\left[\begin{array}{c}
        5 \\
        2 \\
        0 \\
        0 \\
        -8
        \end{array}\right]+x_3\left[\begin{array}{l}
        0 \\
        0 \\
        1 \\
        0 \\
        1
        \end{array}\right]+x_4\left[\begin{array}{c}
        4 \\
        0 \\
        0 \\
        1 \\
        -7
        \end{array}\right]$


#### Øvelse 5: Homogen ligning
Løs den homogene ligning $A\mathbf{x}=\mathbf{0}$ for følgende matricer. Skriv løsningen i parametrisk vektorform.

1. $\begin{bmatrix}
    4 & -8\\
    -3 & 6\end{bmatrix}$

    ??? answer "&nbsp;"
        $\mathbf{x}=x_2\left[\begin{array}{l}2 \\ 1\end{array}\right]$

2. $\begin{bmatrix}
    4 & -9 & 1 \\
    2 & -5 & 1 \\
    -3 & 1 & 5 \end{bmatrix}$

    ??? answer "&nbsp;"
        $\mathbf{x}=x_3\left[\begin{array}{l}2 \\ 1 \\ 1\end{array}\right]$

3. $\begin{bmatrix}
    2 & -10 & 6 \\
    1 & -5 & 3
    \end{bmatrix}$

    ??? answer "&nbsp;"
        $\mathbf{x}=x_2\left[\begin{array}{l}5 \\ 1 \\ 0\end{array}\right]+x_3\left[\begin{array}{c}-3 \\ 0 \\ 1\end{array}\right]$

        $\mathbf{x}=x_2\left[\begin{array}{l}5 \\\ 1 \\\ 0\end{array}\right]+x_3\left[\begin{array}{c}-3 \\\ 0 \\\ 1\end{array}\right]$

4. For øvelserne a)-c) giv en geometrisk fortolkning af løsningsmængden.

    ??? answer "&nbsp;"
        a) Løsningsmængden er en linje i $\mathbb{R}^2$, da den har én fri variabel, hvilket repræsenterer et endimensionalt underrum.  
        b) Løsningsmængden er en linje i $\mathbb{R}^3$, da den har én fri variabel, hvilket repræsenterer et endimensionalt underrum.  
        c) Løsningsmængden er et plan i $\mathbb{R}^3$, da den har to frie variable, hvilket repræsenterer et todimensionalt underrum.
        
#### Øvelse 6: Lineær uafhængighed

1. For $\mathbf{a}_1 = 
    \begin{bmatrix}
        2 \\
        3 \\
        0
    \end{bmatrix}$,
    $\mathbf{a}_2 = 
    \begin{bmatrix}
        1\\
        2\\
        -5
    \end{bmatrix}$,
    $\mathbf{a}_3 = 
    \begin{bmatrix}
        4\\
        1\\
        2
    \end{bmatrix}$, og
    $\mathbf{b} = 
    \begin{bmatrix}
        8\\
        6\\
        12
    \end{bmatrix}$ 
    bestem om $\mathbf{b}$ er en lineær kombination af $\mathbf{a}_1,\mathbf{a}_2$ og $\mathbf{a}_3$.

    ??? answer "&nbsp;"
        Ja, da $\mathbf{b}=3\mathbf{a}_1-2\mathbf{a}_2+\mathbf{a}_3$

2. Lad $A = \begin{bmatrix}1 & -2 & 4 \\
                0 & 4 & -5 \\
                -3 & 6 & -12 \end{bmatrix}$ og
    $\mathbf{b}=\begin{bmatrix}1 \\ -4 \\ -1\end{bmatrix}$ være givet.
    Bestem hvorvidt $\mathbf{b}$ er en lineær kombination af søjlerne i $A$.

    ??? answer "&nbsp;"
        Nej, $\mathbf{b}$ er ikke en lineær kombination af søjlerne i $A$

3. For $A = \begin{bmatrix}2 & -6 & 5 \\
            1 & -5 & 1 \\
            -2 & 6 & p \end{bmatrix}$ og
    $\mathbf{b}= \begin{bmatrix}3 \\ 0 \\ q\end{bmatrix}$ 
    bestem værdierne af $p$ og $q$ således at $\mathbf{b}$ ikke er en lineær kombination af søjlerne i $A$.

    ??? answer "&nbsp;"
        $p=-5$ og $q\neq-3$

