<h1 align="center">Øvelser 3: Mængdelære<br></h1>

I skal lave øvelserne inden timerne torsdag. I kan med fordel lave dem i grupper og diskutere dem indbyrdes. Det er vigtigt, at I forstår opgaverne og kan forklare dem til hinanden. På torsdag diskuterer vi opgaverne, og I skal være klar til at præsentere dem for klassen.

<style>
body[data-md-color-scheme] .md-content ol       { list-style-type: lower-alpha; }
body[data-md-color-scheme] .md-content ol li    { padding-left: 10px; }
</style>

#### Øvelse 1: Roster vs. Set-Builder (ækvivalens)

For hvert par, beslut om de to notationer definerer **den samme** mængde.

1. \(A=\{2,4,6,8\}\) og \(A=\{\,x\in\mathbb Z\mid 1\le x\le 8,\; x\text{ lige}\,\}\). (1)
{ .annotate }

    1. Samme.

2. \(B=\{a,e,i,o,u\}\) og \(B=\{\,l\mid l\text{ er en vokal på engelsk}\,\}\). (1)
{ .annotate }

    1. Samme.

3. \(C=\{x\in\mathbb Z\mid x^2<10\}\) og \(C=\{-3,-2,-1,0,1,2,3\}\). (1)
{ .annotate }

    1. Samme.

#### Øvelse 2: Mængdeoperationer og Kardinalitet

Betragt mængderne $A=\{e, f, g\}$ og $B=\{a, e, g, h\}$. Bestem hver mængde og dens kardinalitet:

1. $A \cup B$ og $|A \cup B|$ (1)
{ .annotate }

    1. $\{a, e, f, g, h\}$ og $5$.

2. $A \cap B$ og $|A \cap B|$ (1)
{ .annotate }

    1. $\{e, g\}$ og $2$.

3. $B-A$ og $|B-A|$ (1)
{ .annotate }

    1. $\{a, h\}$ og $2$.

4. $A-B$ og $|A-B|$ (1)
{ .annotate }

    1. $\{f\}$ og $1$.

#### Øvelse 3: Grundlæggende mængdeoperationer (beregn eksplicit)

Lad \(U=\{1,2,\dots,10\}\), \(A=\{1,3,4,8,10\}\), \(B=\{2,3,7,8\}\).

1. \(A\cup B\) (1)
{ .annotate }

    1. \(\{1,2,3,4,7,8,10\}\).

2. \(A\cap B\) (1)
{ .annotate }

    1. \(\{3,8\}\).

3. \(A\setminus B\) og \(B\setminus A\) (1)
{ .annotate }

    1. \(A\setminus B=\{1,4,10\}\), \(B\setminus A=\{2,7\}\).

4. \(A^\mathrm c\) (komplement i \(U\)) (1)
{ .annotate }

    1. \(\{2,5,6,7,9\}\).

5. \(A\oplus B\) (symmetrisk forskel) (1)
{ .annotate }

    1. \(\{1,2,4,7,10\}\).

#### Øvelse 4: Medlemskab \(\in\) / \(\notin\)

Lad \(U=\mathbb Z\), \(E=\{x\in\mathbb Z\mid x\equiv 0\pmod 2\}\), \(O=U\setminus E\).

1. Beslut: \( -7\in E\ ?\) (1)
{ .annotate }

    1. Nej, \(-7\in O\).

2. Beslut: \(0\in E\ ?\) (1)
{ .annotate }

    1. Ja.

3. Beslut: \( \pi\in U\ ?\) (1)
{ .annotate }

    1. Nej, \(\pi\notin\mathbb Z\).

#### Øvelse 5: Delmængde vs. Egentlig Delmængde

Lad \(A=\{1,2\}\), \(B=\{1,2,3\}\), \(C=\{1,2\}\).

1. Er \(A\subseteq B\)? Er \(A\subset B\)? (1)
{ .annotate }

    1. Ja; Ja (egentlig).

2. Er \(A\subseteq C\)? Er \(A\subset C\)? (1)
{ .annotate }

    1. Ja; Nej (lige, ikke egentlig).

3. Giv et eksempel på to **disjunkte** ikke-tomme delmængder af \(\{1,2,3,4\}\). (1)
{ .annotate }

    1. \(\{1,3\}\) og \(\{2,4\}\).

#### Øvelse 6: Kardinalitet og Potensmængde

1. Beregn \(|\mathcal P(\{a,b,c\})|\) og list \(\mathcal P\).

    ??? answer "&nbsp;"

        \(2^3=8\). \(\{\emptyset,\{a\},\{b\},\{c\},\{a,b\},\{a,c\},\{b,c\},\{a,b,c\}\}\).

2. For \(S=\{1,2,3,4,5\}\), hvor mange delmængder indeholder elementet \(1\)?

    ??? answer "&nbsp;"

        \(2^{4}=16\) (vælg frit blandt de andre 4).

#### Øvelse 7: Intervalnotation (oversættelse)

Oversæt mellem set-builder og intervalnotation i \(\mathbb R\).

1. \(\{x\in\mathbb R\mid -2\le x<3\}\) (1)
{ .annotate }

    1. \([-2,3)\).

2. \((-∞,0]\cup(5,∞)\) i builder-form. (1)
{ .annotate }

    1. \(\{x\in\mathbb R\mid x\le 0\ \text{eller}\ x>5\}\).


#### Øvelse 8: Mængdeidentiteter

1. Bevise at \(A \cup (A \cap B) = A\) ved hjælp af fundamentale mængdeidentiteter.

    ??? answer "&nbsp;"

        \[
        \begin{aligned}
        A \cup (A \cap B)
          &= (A \cup A)\,\cap\,(A \cup B) && \text{distributivitet}\\
          &= A \cap (A \cup B)            && \text{idempotens}\\
          &= A                             && \text{absorption.}
        \end{aligned}
        \]

2. Bevise at \(\left(A \cap A^{c}\right) \cup (A \cap B) \cup \left(A^{c} \cap B\right) = B\) ved hjælp af mængdeidentiteter.

    ??? answer "&nbsp;"

        \[
        \begin{aligned}
        (A \cap A^c) \cup (A \cap B) \cup (A^c \cap B)
          &= \varnothing \cup \big[(A \cap B) \cup (A^c \cap B)\big] && A \cap A^c=\varnothing \\
          &= B \cap (A \cup A^c)                                    && \text{distributivitet}\\
          &= B \cap U                                               && \text{komplementlov}\\
          &= B.                                                     && \text{identitet}
        \end{aligned}
        \]

3. Bevise at \(\big((A^c \cup B)^c\big) \cup A = A\) ved hjælp af mængdeidentiteter.

    ??? answer "&nbsp;"

        \[
        \begin{aligned}
        \big((A^c \cup B)^c\big) \cup A
          &= \big((A^c)^c \cap B^c\big) \cup A && \text{De Morgan}\\
          &= (A \cap B^c) \cup A               && \text{dobbelt komplement}\\
          &= A \cup (A \cap B^c)               \\
          &= A.                                 && \text{absorption}
        \end{aligned}
        \]

4. Bestem om \((A \oplus B) \cup A = A \cup B\) ved hjælp af mængdeidentiteter.

    ??? answer "&nbsp;"

        \[
        \begin{aligned}
        (A \oplus B) \cup A
          &= \big((A \cap B^c) \cup (A^c \cap B)\big) \cup A && \text{def.\ af }\oplus\\
          &= \big(A \cap B^c\big) \cup A \cup \big(A^c \cap B\big)\\
          &= A \cup \big(A^c \cap B\big)                    && A \cup (A \cap X)=A\\
          &= (A \cup A^c)\cap (A \cup B)                    && \text{distributivitet}\\
          &= U \cap (A \cup B)\\
          &= A \cup B.
        \end{aligned}
        \]

### Udfordringsøvelser

#### Udfordringsøvelse 1: Uendelige mængder og tællelighed
I mængdeteori skelner vi mellem endelige, tælleligt uendelige og utælleligt uendelige mængder.  
En mængde er **tælleligt uendelig** hvis dens elementer kan sættes i en-til-en korrespondance med \(\mathbb{N}=\{0,1,2,\dots\}\).

1. Bevise at mængden af lige heltal \(E=\{2n \mid n\in\mathbb{Z}\}\) er tælleligt uendelig.  

    ??? answer "&nbsp;"
        Definer bijektion \(f:\mathbb{Z}\to E\), \(f(n)=2n\). Derfor \(|E|=|\mathbb{Z}|\).

2. Vis at mængden af rationale tal \(\mathbb{Q}\) er tælleligt uendelig.  

    ??? answer "&nbsp;"
        Arranger brøker \(\tfrac{p}{q}\) i et gitter, traversér diagonalt (Cantor zig-zag), og udelad duplikater. Dette lister alle rationale tal.

3. Argumenter hvorfor mængden af reelle tal \(\mathbb{R}\) er **utællelig**.  

    ??? answer "&nbsp;"
        Cantor’s diagonal: givet enhver opregning af decimaler, konstruer et tal der adskiller sig i den \(i\)-te ciffer fra den \(i\)-te indgang. Modsigelse → utællelig.

#### Udfordringsøvelse 2: Paradoxer og potensmængden
For enhver mængde \(S\), har dens potensmængde \(\mathcal{P}(S)\) strengt større kardinalitet end \(S\).  

1. Bevise at ingen funktion \(f:S\to\mathcal{P}(S)\) kan være surjektiv.  

    ??? answer "&nbsp;"
        Antag \(f\) surjektiv. Definer \(T=\{x\in S\mid x\notin f(x)\}\). Så \(T\in\mathcal{P}(S)\).  
        Hvis \(T=f(y)\), modsigelse: \(y\in T\iff y\notin f(y)=T\). Umuligt.  

2. Fortolk hvorfor dette indebærer at der er **ingen største uendelighed**.  

    ??? answer "&nbsp;"
        Hvis \(|\mathcal{P}(S)|>|S|\), så starter vi med \(\mathbb{N}\), får et hierarki: \(\mathcal{P}(\mathbb{N}), \mathcal{P}(\mathcal{P}(\mathbb{N}))\), osv. Derfor danner uendeligheder en endeløs stige.

3. Reflekter: hvad sker der hvis vi forsøger at anvende denne idé på “mængden af alle mængder”?  

    ??? answer "&nbsp;"
        Leder til **Russell’s paradoks**: “mængden af alle mængder der ikke indeholder sig selv” giver modsigelse. Undgås i ZFC-aksiomer.

#### Udfordringsøvelse 3: Kodning af mængder som tal
Enhver endelig delmængde af \(\mathbb{N}\) kan unikt repræsenteres af et naturligt tal. En standardmetode bruger **binær ekspansion**:  
For \(A \subseteq \{0,1,2,\dots,n-1\}\), definer $\operatorname{code}(A)=\sum_{i \in A} 2^i$

1. Kode \(A=\{0,3,4\}\) som et tal.  

    ??? answer "&nbsp;"
        \(2^0+2^3+2^4=1+8+16=25\).  

2. Dekode tallet \(45\) til dets tilsvarende delmængde af \(\{0,1,2,3,4,5\}\).  

    ??? answer "&nbsp;"
        \(45=32+8+4+1=2^5+2^3+2^2+2^0\). Delmængde: \(\{0,2,3,5\}\).  

3. Forklar hvorfor denne kodning giver en bijektion mellem \(\mathcal{P}(\{0,1,\dots,n-1\})\) og heltalene \(0,1,\dots,2^n-1\).  

    ??? answer "&nbsp;"
        Hver delmængde har en unik binær maske, og hver binær streng svarer til præcis én delmængde. Derfor bijektion.

4. Hvordan forbinder denne idé sig til datalogi (bitsets, databaser, logik)?  

    ??? answer "&nbsp;"
        Det er grundlaget for bitsets, tilladelsesflag og sandhedstabeller: delmængder lagret som heltal muliggør effektiv beregning.
