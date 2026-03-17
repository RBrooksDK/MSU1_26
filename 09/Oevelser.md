<h1 align="center">Øvelser 9:<br>Matrix algebra og invertible matricer</h1>

I skal lave øvelserne inden timerne torsdag. I kan med fordel lave dem i grupper og diskutere dem indbyrdes. Det er vigtigt, at I forstår opgaverne og kan forklare dem til hinanden. På torsdag diskuterer vi opgaverne, og I skal være klar til at præsentere dem for klassen.

<style>
body[data-md-color-scheme] .md-content ol       { list-style-type: lower-alpha; }
body[data-md-color-scheme] .md-content ol li    { padding-left: 10px; }
</style>

**[Python]** Betyder at du anbefales at bruge Python til at løse øvelsen. Du kan finde Python-løsningerne [her](https://github.com/RBrooksDK/MSE1_25/blob/main/09/Python_solutions_for_exercises_09.ipynb) eller download dem [her](../Python_solutions_for_exercises_09.ipynb)

#### Øvelse 1
1. Bestem ved inspektion om følgende vektormængder er lineært uafhængige eller afhængige. Begrund hvert svar.
{ .annotate }

    i. $\left[\begin{array}{l}5 \\ 1\end{array}\right],\left[\begin{array}{l}2 \\ 8\end{array}\right],\left[\begin{array}{l}1 \\ 3\end{array}\right],\left[\begin{array}{r}-1 \\ 7\end{array}\right]$ (1)
    { .annotate }

    1. Afhængig

    ii. $\left[\begin{array}{r}2 \\ -4 \\ 8\end{array}\right],\left[\begin{array}{r}-3 \\ 6 \\ -12\end{array}\right]$  (1)
    { .annotate }

    1. Afhængig

    iii. $\left[\begin{array}{r}5 \\ -3 \\ -1\end{array}\right],\left[\begin{array}{l}0 \\ 0 \\ 0\end{array}\right],\left[\begin{array}{r}-7 \\ 2 \\ 4\end{array}\right]$  (1)
    { .annotate }

    1. Afhængig

    iv. $\left[\begin{array}{l}3 \\ 4\end{array}\right],\left[\begin{array}{r}-1 \\ 5\end{array}\right],\left[\begin{array}{l}3 \\ 5\end{array}\right],\left[\begin{array}{l}7 \\ 1\end{array}\right]$  (1)
    { .annotate }

    1. Afhængig

    v. $\left[\begin{array}{r}-8 \\ 12 \\ -4\end{array}\right],\left[\begin{array}{r}2 \\ -3 \\ -1\end{array}\right]$  (1)
    { .annotate }

    1. Uafhængig

    vi. $\left[\begin{array}{r}1 \\ 4 \\ -7\end{array}\right],\left[\begin{array}{r}-2 \\ 5 \\ 3\end{array}\right],\left[\begin{array}{l}0 \\ 0 \\ 0\end{array}\right]$  (1)
    { .annotate }

    1. Afhængig

2. Lad $A = \left[\begin{array}{cccccc}1 & -4 & -2 & 0 & 3 & -5 \\ 0 & 0 & 1 & 0 & 0 & -1 \\ 0 & 0 & 0 & 0 & 1 & -4 \\ 0 & 0 & 0 & 0 & 0 & 0\end{array}\right]$.

    Beskriv alle løsninger til $A \mathbf{x}=\mathbf{0}$ i parameterform.

    ??? answer "&nbsp;"

        Løsningen i parameterform er:

        $$
        \mathbf{x} = \left[\begin{array}{c}
        x_1 \\
        x_2 \\
        x_3 \\
        x_4 \\
        x_5 \\
        x_6
        \end{array}\right] = x_2 \left[\begin{array}{c}
        4 \\
        1 \\
        0 \\
        0 \\
        0 \\
        0
        \end{array}\right] + x_4 \left[\begin{array}{c}
        0 \\
        0 \\
        0 \\
        1 \\
        0 \\
        0
        \end{array}\right] + x_6 \left[\begin{array}{c}
        -5 \\
        0 \\
        1 \\
        0 \\
        4 \\
        1
        \end{array}\right]
        $$

        hvor $x_2$, $x_4$ og $x_6$ er frie variable.

3. **[Python]** Brug så mange søjler af $A$ som muligt til at konstruere en matrix $B$ med egenskaben, at ligningen $B \mathbf{x}=\mathbf{0}$ kun har den trivielle løsning. Løs $B \mathbf{x}=\mathbf{0}$ for at verificere dit arbejde.

$A=\left[\begin{array}{rrrrr}3 & -4 & 10 & 7 & -4 \\ -5 & -3 & -7 & -11 & 15 \\ 4 & 3 & 5 & 2 & 1 \\ 8 & -7 & 23 & 4 & 15\end{array}\right]$

??? answer "&nbsp;"

    $\left[\begin{array}{ccc}3 & -4 & 7 \\ -5 & -3 & -11 \\ 4 & 3 & 2 \\ 8 & -7 & 4\end{array}\right]$

#### Øvelse 2

I (a) og (b) beregn hver matrixsum eller produkt hvis den er defineret. Hvis et udtryk ikke er defineret, forklar hvorfor. Lad

$$
\begin{aligned}
& A=\left[\begin{array}{rrr}
2 & 0 & -1 \\
4 & -5 & 2
\end{array}\right], \quad B=\left[\begin{array}{rrr}
7 & -5 & 1 \\
1 & -4 & -3
\end{array}\right], \\
& C=\left[\begin{array}{rr}
1 & 2 \\
-2 & 1
\end{array}\right], \quad D=\left[\begin{array}{rr}
3 & 5 \\
-1 & 4
\end{array}\right], \quad E=\left[\begin{array}{r}
-5 \\
3
\end{array}\right]
\end{aligned}
$$

1. $-2 A, \; B-2 A, \; A C, \; C D$

    ??? answer "&nbsp;"

        $$-2 A=\left[\begin{array}{rrr}-4 & 0 & 2 \\ -8 & 10 & -4\end{array}\right]$$

        $$B-2 A=\left[\begin{array}{rrr}
        3 & -5 & 3 \\
        -7 & 6 & -7
        \end{array}\right]$$

        $A C$ er ikke defineret.

        $$C D=\left[\begin{array}{rr}1 & 13 \\ -7 & -6\end{array}\right]$$

2. **[Python]** $A+3 B, \; 2 C-3 E, \; D B, \; E C$

    ??? answer "&nbsp;"

        $$A+3 B=\left[\begin{array}{rrr}
        23 & -15 & 2 \\
        7 & -17 & -7
        \end{array}\right]$$

        $2 C-3 E$ er ikke defineret.

        $$D B=\left[\begin{array}{rrr}
        26 & -35 & -12 \\
        -3 & -11 & -13
        \end{array}\right]$$

        $E C$ er ikke defineret.

3. **[Python]** Lad $A=\left[\begin{array}{rr}3 & -6 \\ -1 & 2\end{array}\right], B=\left[\begin{array}{rr}-1 & 1 \\ 3 & 4\end{array}\right]$, og $C= \left[\begin{array}{rr}-3 & -5 \\ 2 & 1\end{array}\right]$. Verificer at $A B=A C$ og alligevel $B \neq C$.

    ??? answer "&nbsp;"

        Da \( AB = \left[\begin{array}{rr} -21 & -21 \\ 7 & 7 \end{array}\right] = AC \), følger \( AB = AC \).

        Dermed er \( AB = AC \) men \( B \neq C \).

4. **[Python]** Hvis $A=\left[\begin{array}{rr}1 & -3 \\ -3 & 5\end{array}\right]$ og $A B=\left[\begin{array}{rr}-3 & -11 \\ 1 & 17\end{array}\right]$, bestem matricen $B$.

    ??? answer "&nbsp;"

        $B=\left[\begin{array}{ll}3 & 1 \\ 2 & 4\end{array}\right]$

#### Øvelse 3

1. Find inverterne af $\begin{array}{cc}{\left[\begin{array}{l}8 \\ 5\end{array}\right.} & \left.\begin{array}{c}6 \\ 4\end{array}\right]\end{array}$ og $\begin{array}{cc}{\left[\begin{array}{l}3 \\ 8\end{array}\right.} & \left.\begin{array}{c}2 \\ 5\end{array}\right]\end{array}$.

    ??? answer "&nbsp;"

        $\left[\begin{array}{ll}8 & 6 \\ 5 & 4\end{array}\right]^{-1}=\frac{1}{32-30}\left[\begin{array}{rr}4 & -6 \\ -5 & 8\end{array}\right]=\left[\begin{array}{cr}2 & -3 \\ -5/2 & 4\end{array}\right]$
        
        $\left[\begin{array}{ll}3 & 2 \\ 8 & 5\end{array}\right]^{-1}=\frac{1}{15-16}\left[\begin{array}{rr}5 & -2 \\ -8 & 3\end{array}\right]=\left[\begin{array}{cc}-5 & 2 \\ 8 & -3\end{array}\right]$

2. **[Python]** Brug inversen fundet i Øvelse 3.a til at løse systemet

    $\begin{aligned}
    & 8 x_1+6 x_2=2 \\
    & 5 x_1+4 x_2=-1
    \end{aligned}$

    ??? answer "&nbsp;"
        Løsning: $x_1=7$ og $x_2=-9$.

3. **[Python]** Find inversen af matricen. Brug algoritmen for at finde inversen af en $n \times n$ matrix.

    $\left[\begin{array}{rrr}
    1 & 0 & -2 \\
    -3 & 1 & 4 \\
    2 & -3 & 4
    \end{array}\right]$

    ??? answer "&nbsp;"

        $$\left[\begin{array}{ccc}
        8 & 3 & 1 \\
        10 & 4 & 1 \\
        7/2 & 3/2 & 1/2
        \end{array}\right]
        $$

#### Øvelse 4

I denne øvelse er matricerne alle $n \times n$. Hvert delspørgsmål er en implikation af formen "Hvis (udsagn 1), så (udsagn 2)". Markér en implikation som Sandt hvis sandheden af (udsagn 2) altid følger når (udsagn 1) er sand. En implikation er Falsk hvis der findes en instans hvor (udsagn 2) er falsk mens (udsagn 1) er sand. Begrund hvert answer.

1. Hvis ligningen $A \mathbf{x}=\mathbf{0}$ kun har den trivielle løsning, så er $A$ rækkeekvivalent med $n \times n$ identitetsmatricen. (1)
{ .annotate }

    1. Sandt

2. Hvis søjlerne i $A$ spænder over $\mathbb{R}^n$, så er søjlerne lineært uafhængige.  (1)
{ .annotate }

    1. Sandt

3. Hvis $A$ er en $n \times n$ matrix, så har ligningen $A \mathbf{x}=\mathbf{b}$ mindst én løsning for hvert $\mathbf{b}$ i $\mathbb{R}^n$. (1)
{ .annotate }

    1. Falsk

4. Hvis ligningen $A \mathbf{x}=\mathbf{0}$ har en ikke-triviel løsning, så har $A$ færre end $n$ pivotpositioner. (1)
{ .annotate }

    1. Sandt

5. Hvis $A^T$ ikke er invertibel, så er $A$ ikke invertibel. (1)
{ .annotate }

    1. Sandt

#### Øvelse 5
**[Python]** Givet

$A=\left[\begin{array}{ccc}1 & 0 & 0 \\ 0 & 3 & 0 \\ 0 & 0 & -3\end{array}\right]$ og $B=\left[\begin{array}{ccc}1 & 1 & 1 \\ 1 & 1 & 1 \\ 1 & 1 & 1\end{array}\right]$.

Løs matrixligningen $X+A=2(X-B)$.

??? answer "&nbsp;"

    $X=\left[\begin{array}{ccc}3 & 2 & 2 \\ 2 & 5 & 2 \\ 2 & 2 & -1\end{array}\right]$

#### Øvelse 6

**[Python]** Lad matricen $A$ være givet ved

$A=\left[\begin{array}{cc}
3-2 q & 1 \\
4 & 3+2 q
\end{array}\right]$

hvor $q$ er en skalar. Beregn $q$ så

$A^2=\left[\begin{array}{cc}
29 & 6 \\
24 & 125
\end{array}\right]$

??? answer "&nbsp;"

    $q=4$
