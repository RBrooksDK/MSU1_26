<h1 align="center">Øvelser</h1>

Øvelserne skal laves i løbet af undervisningen, men I må gerne kigge på dem derhjemme

<style>
body[data-md-color-scheme] .md-content ol       { list-style-type: lower-alpha; }
body[data-md-color-scheme] .md-content ol li    { padding-left: 10px; }
</style>

#### Øvelse 1:

Løs følgende ligninger:

1. $\ 2-\frac{4 x+3}{x+x^2}=\frac{2 x}{x+1}-\frac{5}{x}$
2. $\ -2+2 \ln 3 x=17$
3. $\ \ln (x+1)^2=2$
4. $\ \ln \left(x^2+1\right)=8$
5. $\ 5^{3 x+2}=25^{x-1}$
6. $\ 2^{x+1}=4^{x-2}$

??? answer "&nbsp;"

    1. $x = -\frac{2}{3}$
    2. $x = \frac{e^{\frac{19}{2}}}{3}$
    3. $x = -1 \pm e$
    4. $x = \pm \sqrt{e^8 - 1}$
    5. $x = -4$
    6. $x = 5$

#### Øvelse 2:

Ifølge Einsteins relativitetsteori gives massen af en partikel ved:

$$
m=\frac{m_0}{\sqrt{1-\left(\frac{v}{c}\right)^2}}
$$

hvor
$m_0$ er massen af partiklen i hvile,
$v$ er partiklens hastighed, og
$c$ er lysets hastighed i vakuum.

1. Gør $v$ til subjektet i formlen givet $v>0$.

    ??? answer "&nbsp;"

        $v=c \cdot \sqrt{1-\left(\frac{m_0}{m}\right)^2}$

2. Find den hastighed, der er nødvendig for at øge massen af en partikel til tre gange dens hvilemasse. Giv værdien for $v$ som en brøkdel af $c$ (eller som en decimal).

    ??? answer "&nbsp;"

        $v=0.943 c$

#### Øvelse 3
Bestem definitionsmængden og værdimængden for hver af de reelle funktioner nedenfor. Det er en god idé at plotte funktionerne ved hjælp af software (f.eks. Geogebra, WolframAlpha osv.):

1. $\ f(x)=\frac{1}{x-7}$

    ??? answer "&nbsp;"

        Definitionsmængde: $\mathbb{R} \backslash\{7\}$;

        Værdimængde: $\mathbb{R} \backslash\{0\}$

2. $\ f(x)=\sqrt{x+3}$

    ??? answer "&nbsp;"

        Definitionsmængde: $\mathbb{R}_ {\geq-3}$;

        Værdimængde: $\mathbb{R}_ {\geq 0}$

#### Øvelse 4
Find hver af de følgende sammensatte funktioner:

1. $\ g \circ f$ når $f(x)=3 x+1$ og $g(x)=x^2$.

    ??? answer "&nbsp;"

        $(g \circ f)(x)=9 x^2+1+6 x$

2. $f \circ g$ når $f(x)=x^2+1$ og $g(x)=\frac{1}{x}$.

    ??? answer "&nbsp;"

        $(f \circ g)(x)=\frac{1}{x^2}+1$

3. $\ g \circ f$ når $f$ og $g$ er defineret som i øvelse (2).

    ??? answer "&nbsp;"

        $(g \circ f)(x)=\frac{1}{x^2+1}$

#### Øvelse 5
Find den inverse funktion:

1. $\ f(x)=\frac{6}{5-x}$

    ??? answer "&nbsp;"

        $f^{-1}(x)=5-\frac{6}{x}$

2. $\ f(x)=-\ln (1-2 x)+1$

    ??? answer "&nbsp;"

        $f^{-1}(x)=\left(1-e^{1-x}\right) / 2$

3. $\ f(x)=2 \cdot 10^{3 x}-1$

    ??? answer "&nbsp;"

        $f^{-1}(x)=\frac{\log \left(\frac{x+1}{2}\right)}{3}$

#### Øvelse 6

En bakteriekultur starter med 1000 bakterier ved tiden $t=0$, og antallet fordobles hver 40. minut.

1. Find et funktionelt udtryk for antallet af bakterier ved tiden $t$ (målt i minutter).

    ??? answer "&nbsp;"

        $f(t)=1000 \cdot 2^{t / 40}$

2. Find antallet af bakterier efter en time.

    ??? answer "&nbsp;"

        $f(60) \approx 2828$

3. Efter hvor mange minutter vil der være 50000 bakterier?

    ??? answer "&nbsp;"

        ca. 225.75 minutter

#### Øvelse 7

Bestem, om den givne funktion er inverterbar ved at kontrollere, om den er injektiv (en-til-en) og surjektiv (på). Hvis du konkluderer, at funktionen er inverterbar, bestem dens inverse funktion.

1. $f: R \backslash\{1\} \rightarrow R \backslash\{0\}, f(x)=\frac{2}{x-1}$

    ??? answer "&nbsp;"

        Funktionen er inverterbar.

        $f^{-1}(x)=\frac{2}{x}+1$

2. $f: R \backslash\{3\} \rightarrow R, f(x)=\frac{x+1}{x-3}$

    ??? answer "&nbsp;"

        Funktionen er ikke surjektiv, derfor er den ikke inverterbar.

3. $f: R \rightarrow R, f(x)=x^3-3 x$

    ??? answer "&nbsp;"

        Funktionen er ikke injektiv, derfor er den ikke inverterbar.

### Udfordringsøvelser

Nogle andengradspolynomier har ikke nogen rødder blandt de reelle tal. For eksempel opfylder ingen reel værdi af $x$ ligningen $x^2+1=0$. Men hvis vi definerer det imaginære tal $i=\sqrt{-1}$, ser vi, at ligningen er sand for $x= \pm i$ :

$$
i^2+1=-1+1=0 \quad \text { og } \quad(-i)^2+1=-1+1=0
$$

#### Udfordringsøvelse 1

Løs ligningerne nedenfor (en andengradsligning med imaginære rødder løses på samme måde som en almindelig andengradsligning.):

1. $9 x^2+64=0$

    ??? answer "&nbsp;"

        $x= \pm \frac{8}{3} i$

2. $x^2+10 x+169=0$

    ??? answer "&nbsp;"

        $x=-5 \pm 12 i$

3. $6 x^2+13 ix-2=0$

    ??? answer "&nbsp;"

        $x=-\frac{1}{6} i$ eller $x=-2 i$

#### Udfordringsøvelse 2

Vis, at værdien af hvert af udtrykkene nedenfor er reel (dvs. indeholder ikke $i$ ):

1. $(1+i)(1-i)$

    ??? answer "&nbsp;"

        $(1+i)(1-i)=2$

2. $(a+b i)(a-b i)$

    ??? answer "&nbsp;"

        $(a+b i)(a-b i)=a^2-b^2 i^2=a^2+b^2$

#### Udfordringsøvelse 3

Beregn eller reducer hvert af udtrykkene nedenfor:

1. $i^{2017}$

    ??? answer "&nbsp;"

        $i$

2. $\frac{1}{2+3 i}+\frac{1}{2-3 i}$

    ??? answer "&nbsp;"

        $\frac{4}{13}$

3. $\frac{1+i}{1-i}$

    ??? answer "&nbsp;"

        $i$
