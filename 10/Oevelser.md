<h1 align="center">Øvelser</h1>

<style>
body[data-md-color-scheme] .md-content ol       { list-style-type: lower-alpha; }
body[data-md-color-scheme] .md-content ol li    { padding-left: 10px; }
</style>


I opgave 6 skal du anvende matrixmultiplikation til at kombinere to rotationer. Vi har primært arbejdet med matrixmultiplikation i SymPy, hvor man blot kan skrive `A*B` for at multiplicere to matricer. I NumPy foregår det på følgende måde:

```python
import numpy as np

# Definer to 3x3 matricer
A = np.array([[1, 2, 3],
              [4, 5, 6],
              [7, 8, 9]])

B = np.array([[9, 8, 7],
              [6, 5, 4],
              [3, 2, 1]])

# Udfør matrixmultiplikation ved hjælp af np.dot
resultat = np.dot(A, B)

# Alternativt kan '@'-operatoren bruges (Python 3.5+)
resultat_alt = A @ B

# Vis resultater
print("Matrix A:")
print(A)

print("\nMatrix B:")
print(B)

print("\nResultat af matrixmultiplikation (A * B):")
print(resultat)

print("\nResultat af matrixmultiplikation ved hjælp af '@' operatoren (A @ B):")
print(resultat_alt)
```

<style type="text/css">
    ol { list-style-type: lower-alpha; }
</style>

---

#### Øvelse 1

Alle nedenstående er i 3D-rummet.

 1. Konstruér en matrix til at rotere \( -22^{\circ} \) omkring \( x \)-aksen.  
 2. Konstruér en matrix til at rotere \( 30^{\circ} \) omkring \( y \)-aksen.  
 3. Konstruér en matrix til at rotere \( -15^{\circ} \) omkring aksen \( [0.267,-0.535,0.802] \).  

??? answer "Se svaret"

    1. $\left[\begin{array}{ccc}1 & 0 & 0 \\ 0 & \cos \left(-22^{\circ}\right) & \sin \left(-22^{\circ}\right) \\ 0 & -\sin \left(-22^{\circ}\right) & \cos \left(-22^{\circ}\right)\end{array}\right]=\left[\begin{array}{ccc}1.000 & 0.000 & 0.000 \\ 0.000 & 0.927 & -0.375 \\ 0.000 & 0.375 & 0.927\end{array}\right]$
    2. $\begin{aligned} & {\left[\begin{array}{ccc}\cos 30^{\circ} & 0 & -\sin 30^{\circ} \\ 0 & 1 & 0 \\ \sin 30^{\circ} & 0 & \cos 30^{\circ}\end{array}\right]=\left[\begin{array}{ccc}0.866 & 0.000 & -0.500 \\ 0.000 & 1.000 & 0.000 \\ 0.500 & 0.000 & 0.866\end{array}\right]}\end{aligned}$
    3. $\left[\begin{array}{ccc}0.968 & -0.212 & -0.131 \\ 0.203 & 0.976 & -0.084 \\ 0.146 & 0.054 & 0.988\end{array}\right]$


---

#### Øvelse 2

Konstruér en matrix, der fordobler højden, bredden og længden af et objekt i 3D.

??? answer "Se svaret"
    $\left[\begin{array}{lll}2 & 0 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 2\end{array}\right]$

---

#### Øvelse 3

Konstruér en $4 \times 4$ matrix til at flytte ved $[4,2,3]$. Husk at bogen bruger rækkevektorer, så flytningen skal være i den sidste række.

??? answer "Se svaret"
    $\left[\begin{array}{llll}1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 0 \\ 4 & 2 & 3 & 1\end{array}\right]$


---

#### Øvelse 4

Konstruér en $4 \times 4$ matrix til at rotere $20^{\circ}$ omkring $x$-aksen og derefter flytte ved $[4,2,3]$.

??? answer "Se svaret"
    $\begin{aligned} \mathbf{R}_x\left(20^{\circ}\right) \mathbf{T}([4,2,3]) & =\left[\begin{array}{cccc}1.000 & 0.000 & 0.000 & 0.000 \\ 0.000 & 0.940 & 0.342 & 0.000 \\ 0.000 & -0.342 & 0.940 & 0.000 \\ 0.000 & 0.000 & 0.000 & 1.000\end{array}\right]\left[\begin{array}{llll}1.000 & 0.000 & 0.000 & 0.000 \\ 0.000 & 1.000 & 0.000 & 0.000 \\ 0.000 & 0.000 & 1.000 & 0.000 \\ 4.000 & 2.000 & 3.000 & 1.000\end{array}\right] \\ & =\left[\begin{array}{cccc}1.000 & 0.000 & 0.000 & 0.000 \\ 0.000 & 0.940 & 0.342 & 0.000 \\ 0.000 & -0.342 & 0.940 & 0.000 \\ 4.000 & 2.000 & 3.000 & 1.000\end{array}\right]\end{aligned}$

---

#### Øvelse 5

Konstruér en $4 \times 4$ matrix til at flytte ved $[4,2,3]$ og derefter rotere $20^{\circ}$ omkring $x$-aksen.


??? answer "Se svaret"
    $\begin{aligned} \mathbf{T}([4,2,3]) \mathbf{R}_x\left(20^{\circ}\right) & =\left[\begin{array}{cccc}1.000 & 0.000 & 0.000 & 0.000 \\ 0.000 & 1.000 & 0.000 & 0.000 \\ 0.000 & 0.000 & 1.000 & 0.000 \\ 4.000 & 2.000 & 3.000 & 1.000\end{array}\right]\left[\begin{array}{cccc}1.000 & 0.000 & 0.000 & 0.000 \\ 0.000 & 0.940 & 0.342 & 0.000 \\ 0.000 & -0.342 & 0.940 & 0.000 \\ 0.000 & 0.000 & 0.000 & 1.000\end{array}\right] \\ & =\left[\begin{array}{cccc}1.000 & 0.000 & 0.000 & 0.000 \\ 0.000 & 0.940 & 0.342 & 0.000 \\ 0.000 & -0.342 & 0.940 & 0.000 \\ 4.000 & 0.853 & 3.503 & 1.000\end{array}\right]\end{aligned}$
 

---

#### Øvelse 6

Et objekt havde oprindeligt sine akser og origo sammenfaldende med world space akser og origo. Det blev derefter roteret \( 30^{\circ} \) omkring \( y \)-aksen og derefter \( -22^{\circ} \) omkring \( x \)-aksen. Husk at rækkevektorer multipliceres fra venstre og kolonnevektorer fra højre.

 1. Hvad er matricen, der kan bruges til at transformere rækkevektorer fra objekt space til world space? *Hint*: du kan bruge rotationsmatricerne fra øvelse 1.
 2. Hvad med matricen til at transformere vektorer fra verdensrummet til objektets rum? *Hint*: Det er ret meget relateret til (6a) og transponering.
 3. Udtryk objektets \( z \)-akse ved hjælp af opretstående koordinater (upright space fra sidste session).

??? answer "Se svaret"
    1. $\begin{aligned} \mathbf{M}_{\mathrm{obj} \rightarrow \text { wld }}=\mathbf{R}_y\left(30^{\circ}\right) \mathbf{R}_x\left(-22^{\circ}\right) & =\left[\begin{array}{ccc}0.866 & 0.000 & -0.500 \\ 0.000 & 1.000 & 0.000 \\ 0.500 & 0.000 & 0.866\end{array}\right]\left[\begin{array}{ccc}1.000 & 0.000 & 0.000 \\ 0.000 & 0.927 & -0.375 \\ 0.000 & 0.375 & 0.927\end{array}\right] \\ & =\left[\begin{array}{ccc}0.866 & -0.187 & -0.464 \\ 0.000 & 0.927 & -0.375 \\ 0.500 & 0.324 & 0.803\end{array}\right]\end{aligned}$
    2. Her skal vi tage de modsatte rotationer i den modsatte rækkefølge.

        \[
        \begin{aligned}
        \mathbf{M}_{\mathrm{wld} \rightarrow \mathrm{obj}}=\mathbf{R}_x\left(22^{\circ}\right) \mathbf{R}_y\left(-30^{\circ}\right) & =\left[\begin{array}{ccc}
        1.000 & 0.000 & 0.000 \\
        0.000 & 0.927 & 0.375 \\
        0.000 & -0.375 & 0.927
        \end{array}\right]\left[\begin{array}{ccc}
        0.866 & 0.000 & 0.500 \\
        0.000 & 1.000 & 0.000 \\
        -0.500 & 0.000 & 0.866
        \end{array}\right] \\
        & =\left[\begin{array}{ccc}
        0.866 & 0.000 & 0.500 \\
        -0.187 & 0.927 & 0.324 \\
        -0.464 & -0.375 & 0.803
        \end{array}\right]
        \end{aligned}
        \]

        Eller, måske vidste du allerede, at resultatet blot ville være transponeret af svaret fra det forrige problem. Hvis ja, godt for dig.
    3. Konverter \( z \)-aksen fra objektets rum til opretstående rum:

        \[
        \left[\begin{array}{lll}
        0 & 0 & 1
        \end{array}\right]\left[\begin{array}{ccc}
        0.866 & -0.187 & -0.464 \\
        0.000 & 0.927 & -0.375 \\
        0.500 & 0.324 & 0.803
        \end{array}\right]=\left[\begin{array}{lll}
        0.500 & 0.324 & 0.803
        \end{array}\right]
        \]

        Dette er selvfølgelig blot det samme som at udtrække den sidste række af matricen.


---