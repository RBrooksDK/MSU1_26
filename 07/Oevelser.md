---
tags:
    - Lineær Algebra
    - Rækkereduktion
    - Echelon Form
    - Reduceret Echelon Form
    - Rækkeoperationer
    - System af Lineære Ligninger
---

<h1 align="center">Øvelser 7:<br>Lineære ligninger i lineær algebra</h1>

I skal lave øvelserne inden timerne torsdag. I kan med fordel lave dem i grupper og diskutere dem indbyrdes. Det er vigtigt, at I forstår opgaverne og kan forklare dem til hinanden. På torsdag diskuterer vi opgaverne, og I skal være klar til at præsentere dem for klassen.

<style>
body[data-md-color-scheme] .md-content ol       { list-style-type: lower-alpha; }
body[data-md-color-scheme] .md-content ol li    { padding-left: 10px; }
</style>

### Øvelser

#### Øvelse 1: Echelon og reduceret echelon form
Bestem hvorvidt følgende matricer er i reduceret echelon form, echelon form eller hverken.

a. $\begin{bmatrix} 1 & 0 & 2 & 1\\ 
                0 & 1 & -3 & 0\end{bmatrix}$

b.
$\begin{bmatrix} 1 & 2 & -2 & 5\\
                0 & 1 &  0 & -1\\
                0 & 0 &  1 & 3 \\ 
                0 & 0 &  0 & 1\end{bmatrix}$

c.
$\begin{bmatrix} -1 & 0\\
                0 & 4\\
                0 & 0 \end{bmatrix}$

d.
$\begin{bmatrix} 1 & 0 & 1 & 0 & -1\\
                0 & 1 & 1 & 0 & 0\\
                0 & 0 & 0 & 0 & 0\\
                0 & 0 & 0 & 1 & -1\end{bmatrix}$

e.
$\begin{bmatrix} 0 & 3 & 0 & 4\\
                0 & 0 & -2 & -2\\
                0 & 0 & 0 & 7\end{bmatrix}$

f.
$\begin{bmatrix} 1 & 0 & 0 & 1\\
                0 & 0 & 1 & -2\\
                0 & 0 & 0 & 1\end{bmatrix}$

??? answer "&nbsp;"
    a. reduceret echelon form 

    b. echelon form

    c. echelon form

    d. hverken

    e. echelon form

    f. echelon form



#### Øvelse 2: Rækkeoperationer
Forklar hvilke rækkeoperationer der bruges i beregningerne nedenfor.

a.
$\begin{bmatrix}
    4 & -3 & 1 & 2 \\
    3 & 1 & -5 & 6 \\
    1 & 1 & 2 & 4 \\
    \end{bmatrix}
    \sim
\begin{bmatrix}
    1 & 1 & 2 & 4 \\
    3 & 1 & -5 & 6 \\
    4 & -3 & 1 & 2 \\
    \end{bmatrix}$

??? answer "&nbsp;"
    Swap: $r_1 \leftrightarrow r_3$

b. $\begin{bmatrix}
    1 & 1 & 2 & 4 \\
    3 & 1 & -5 & 6 \\
    4 & -3 & 1 & 2 \\
    \end{bmatrix}
    \sim
    \begin{bmatrix}
    1 & 1 & 2 & 4 \\
    0 & -2 & -11 & -6 \\
    4 & -3 & 1 & 2 \\
    \end{bmatrix}$

??? answer "&nbsp;"
    Erstatning: $r_2 \rightarrow r_2 - 3r_1$
c. $\begin{bmatrix}
    1 & 1 & 2 & 4 \\
    0 & -2 & -11 & -6 \\
    4 & -3 & 1 & 2 \\
    \end{bmatrix}
    \sim
    \begin{bmatrix}
    1 & 1 & 2 & 4 \\
    0 & -2 & -11 & -6 \\
    0 & -7 & -7 & -14 \\
    \end{bmatrix}$

??? answer "&nbsp;"
    Erstatning: $r_3 \rightarrow r_3 - 4r_1$

d. $\begin{bmatrix}
    1 & 1 & 2 & 4 \\
    0 & -2 & -11 & -6 \\
    0 & -7 & -7 & -14 \\
    \end{bmatrix}
    \sim
    \begin{bmatrix}
    1 & 1 & 2 & 4 \\
    0 & -2 & -11 & -6 \\
    0 & 1 & 1 & 2 \\
    \end{bmatrix}$

??? answer "&nbsp;"

    Skalering: $r_3 \rightarrow -\frac{1}{7}r_3$

e. $\begin{bmatrix}
    1 & 1 & 2 & 4 \\
    0 & -2 & -11 & -6 \\
    0 & 1 & 1 & 2 \\
    \end{bmatrix}
    \sim
    \begin{bmatrix}
    1 & 1 & 2 & 4 \\
    0 & 1 & 1 & 2 \\
    0 & -2 & -11 & -6 \\
    \end{bmatrix}$

??? answer "&nbsp;"
    Swap: $r_2 \leftrightarrow r_3$

f. $\begin{bmatrix}
    1 & 1 & 2 & 4 \\
    0 & 1 & 1 & 2 \\
    0 & -2 & -11 & -6 \\
    \end{bmatrix}
    \sim
    \begin{bmatrix}
    1 & 1 & 2 & 4 \\
    0 & 1 & 1 & 2 \\
    0 & 0 & -9 & -2 \\
    \end{bmatrix}$

??? answer "&nbsp;"
    Erstatning: $r_3 \rightarrow r_3 + 2r_2$

g. Den reducerede matrix fra (f) er den augmenterede matrix for et system af lineære ligninger. Har dette system ingen løsning, en unik løsning eller uendeligt mange løsninger?

??? answer "&nbsp;"
    Systemet har en unik løsning, da der er en pivot i hver kolonne af koefficientdelen af den reducerede matrix.

#### Øvelse 3: System af lineære ligninger
Givet følgende system af lineære ligninger:

$$
\begin{aligned}
2x_1 - 4x_2 + 6x_3 &= 2 \\
x_1 + x_3 &= 3 \\
-4x_1 + 2x_2 &= 2
\end{aligned}
$$

a. Skriv den augmenterede matrix for systemet.

??? answer "&nbsp;"
    $\begin{bmatrix}
    2 & -4 & 6 & 2\\
    1 & 0  & 1 & 3\\
    -4& 2  & 0 & 2
    \end{bmatrix}$

b. Brug rækkeoperationer til at få den reducerede række-echelon form af matrixen og skriv løsningen ned.

??? answer "&nbsp;"
    RREF:
    $\begin{bmatrix}
    1 & 0 & 0 & 1\\
    0 & 1 & 0 & 3\\
    0 & 0 & 1 & 2
    \end{bmatrix}$

    Løsning:
    $\begin{cases}
        x_1 = 1\\
        x_2 = 3\\
        x_3 = 2
    \end{cases}$

#### Øvelse 4: Rækkereduktion
Løs systemerne hvis augmenterede matricer er givet nedenfor. Skriv den generelle løsning ned, dvs. skriv de basale variable i forhold til de frie variable. 

a. $\begin{bmatrix} 1 & 2 & 3 & 4\\
                    4 & 8 & 9 & 4\end{bmatrix}$

??? answer "&nbsp;"
    $\begin{cases}
        x_1 = -8-2x_2\\
        x_2 \text{ fri}\\
        x_3 = 4
    \end{cases}$

b. $\begin{bmatrix} 1 & -1 & -2 & 3\\
                    4 & -2 & -8 & 2\end{bmatrix}$

??? answer "&nbsp;"
    $\begin{cases}
        x_1 = -2+2x_3\\
        x_2 = -5\\
        x_3 \text{ fri}
    \end{cases}$

c. $\begin{bmatrix} -2 & 4 & -3 & 0\\
                    4 & -8 & 6& 0\\
                    -6& 12& -9 & 0\end{bmatrix}$

??? answer "&nbsp;"
    $\begin{cases}
        x_1 = 2x_2 - \frac{3}{2}x_3\\
        x_2 \text{ fri}\\
        x_3 \text{ fri}
    \end{cases}$

#### Øvelse 5: Konsistens af systemet
Hvilke af de augmenterede matricer nedenfor repræsenterer et inkonsistent system af ligninger?

a. $\begin{bmatrix}
    0 & 3 & -2 & 1\\
    0 & 0  & -1 & 4\\
    0 & 0  & 0 & 0 \end{bmatrix}$

b. $\begin{bmatrix}
    -1 & 3 & 1 \\
    0 & 5  & 3 \\
    0 & 0  & 6 \end{bmatrix}$

c. $\begin{bmatrix}
    7 & 1 & 1 \\
    0 & 2  & 2 \\
    0 & 0  & 3 \\
    0 & 0  & 0
\end{bmatrix}$

d. $\begin{bmatrix}
    1 & 0 \\
    0 & 1 
\end{bmatrix}$

e. $\begin{bmatrix}
    -3 & 0 & 0 & 9\\
    0 & 1  & 0 & 0\\
    0 & 0  & 4 & 0
\end{bmatrix}$

f. $\begin{bmatrix}
    0 & 0 & 6 & 3
\end{bmatrix}$

??? answer "&nbsp;"
    inkonsistent: b, c, d

    konsistent: a, e, f


g. For de konsistente systemer, find den generelle løsning.

??? answer "&nbsp;"
    a. $\begin{cases}
        x_1 \text{ fri}\\
        x_2 = -\frac{7}{3}\\
        x_3 = -4
    \end{cases}$

    e. $\begin{cases}
        x_1 = - 3\\
        x_2 = 0\\
        x_3 = 0
    \end{cases}$

    f. $\begin{cases}
        x_1 \text{ fri}\\
        x_2 \text{ fri}\\
        x_3 = \frac{1}{2}
    \end{cases}$


#### Øvelse 6: Planlæg en kost
Brug Python til at løse denne øvelse. 

I en uge beslutter du at spise kun smør, æbler og havre.

|Næringsværdier per 100 g|  Smør  |  Æble  |  Havre  | Rugbrød|
|----------------------------|---------:|--------:|-------:|---------:|
|Protein       (g)           |    0.2   |   0.3   | 14.0   |    6.4   |
|Fedt           (g)           |   82.5   |   0.2   |  6.9   |    4.7   |
|Kulhydrater (g)           |    0.0   |   12.1  | 57.0   |   32.0   |

a. Hvor meget smør, æble og havre skal du spise for at få 50 g protein, 70 g fedt og 260 g kulhydrater per dag?

??? answer "&nbsp;"
    $\begin{cases}  54.7 \text{ g smør}\\
                522.8\text{ g æble}\\
                345.2 \text{ g havre}\end{cases}$


Næste uge beslutter du at erstatte æbler med rugbrød.

b. Er det muligt at planlægge en kost af smør, rugbrød og havre for stadig at få 50 g protein, 70 g fedt og 260 g kulhydrat per dag?

??? answer "&nbsp;"
    Nej, systemet af lineære ligninger har en unik løsning. Dog indeholder løsningen en negativ mængde havre, hvilket ikke giver mening.
