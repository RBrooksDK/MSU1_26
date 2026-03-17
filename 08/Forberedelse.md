<h1 align="center">M1: Forberedelse før den første undervisning - Vektorer og matricer</h1>

At forberede sig betyder ikke nødvendigvis at læse alt materiale fra start til slut. Det handler i stedet om at identificere og fokusere på det indhold, der er mest relevant for dig og din forberedelse til undervisningen. Jeg forventer dog, at du har gennemgået og forstået materialet fra tutorials og/eller videoerne. Du kan teste din viden i quizzen, hvor en forståelse anses som tilstrækkelig, hvis du kan svare korrekt på mindst 7 ud af 10 spørgsmål.


<hr>

### Læsemateriale:

Brooks: [Kapitel 8](https://docs.google.com/viewer?url=https://raw.githubusercontent.com/RBrooksDK/MSE_book_v2/master/main.pdf).


<hr>

### Ressourcer

[Noter fra videomateriale](https://drive.google.com/file/d/1pgvezM1CDloxEbb2C7SieGaUPD8DLv9E/view?usp=sharing)

[Andre materialer](https://viaucdk-my.sharepoint.com/:f:/g/personal/rib_viauc_dk/Ep-kuPOC2r5NsJOp-SzZ1U8BsPWE1ZL0SEZTvJ8NXxrsHQ?e=y455Od)


<hr>

### Videomateriale

#### 8.1. Linearkombinationer

<div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%; overflow: hidden;">
    <iframe 
        src="https://drive.google.com/file/d/1THASrpG_1SGrFDRQVseeEuJY-eeZsOVG/preview" 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
        allow="autoplay; encrypted-media" 
        allowfullscreen>
    </iframe>
</div>



#### 8.2. Vektorligninger

<div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%; overflow: hidden;">
    <iframe 
        src="https://drive.google.com/file/d/16f2m9YpRobN1l6ZUzwV5uq3zTul4NFTF/preview" 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
        allow="autoplay; encrypted-media" 
        allowfullscreen>
    </iframe>
</div>

#### 8.3. Matrixligninger

<div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%; overflow: hidden;">
    <iframe 
        src="https://drive.google.com/file/d/1Gqz-mOhviCSJI454ngNdrxoS-Eb6aQcT/preview" 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
        allow="autoplay; encrypted-media" 
        allowfullscreen>
    </iframe>
</div>

#### 8.4. Løsningsmængder til lineære ligningssystemer

<div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%; overflow: hidden;">
    <iframe 
        src="https://drive.google.com/file/d/1c7cxZfs-hveel77-krmctBuLyeyNjIFq/preview" 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
        allow="autoplay; encrypted-media" 
        allowfullscreen>
    </iframe>
</div>

#### 8.5. Lineær uafhængighed

<div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%; overflow: hidden;">
    <iframe 
        src="https://drive.google.com/file/d/1yQOPSC6Tdh809U4OZFwqO6AZu2NopQeO/preview" 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
        allow="autoplay; encrypted-media" 
        allowfullscreen>
    </iframe>
</div>

<hr>

### Quiz
Når du har været igennem videoerne og/eller læst materialet i dette modul, kan du teste din viden i quizzen. Quizzen indeholder 10 spørgsmål, og en forståelse anses som tilstrækkelig, hvis du kan svare korrekt på mindst 7 ud af 10 spørgsmål. Du kan se din samlede score nederst på siden, og du kan også se din score for hvert spørgsmål. Du kan tage quizzen så mange gange, og dine resulter bliver hverken gemt eller vurderet. Quizzen er kun til din egen skyld, så du kan se, hvor godt du har forstået materialet.

<?quiz?>
question: Hvad er en vektor i matematisk forstand?
answer: En vektor er et tal
answer: En vektor er en ordnet liste af tal
answer-correct: En vektor er en matrix med kun én søjle eller én række
answer: En vektor er en funktion
answer: En vektor er en ligning
content:
<p><strong>Forklaring:</strong> En vektor er en matrix med kun én søjle (kolonnevektor) eller én række (rækkevektor), der kan repræsentere positioner, retninger eller data.</p>
<?/quiz?>

---

<?quiz?>
question: Hvilken operation kan IKKE udføres på vektorer af samme dimension?
answer: Addition
answer: Subtraktion
answer: Skalarmultiplikation
answer-correct: Multiplikation af to vektorer
answer: Lineære kombinationer
content:
<p><strong>Forklaring:</strong> To vektorer kan ikke multipliceres direkte med hinanden. Derimod kan de adderes, subtraheres, multipliceres med skalarer og kombineres lineært.</p>
<?/quiz?>

---

<?quiz?>
question: Hvad er en vektorligning?
answer: En ligning med kun vektorer
answer-correct: En ligning af formen $x_1\mathbf{a}_1 + x_2\mathbf{a}_2 + \cdots + x_n\mathbf{a}_n = \mathbf{b}$
answer: En ligning med kun skalarer
answer: En ligning med kun matricer
answer: En ligning med kun funktioner
content:
<p><strong>Forklaring:</strong> En vektorligning er af formen $x_1\mathbf{a}_1 + x_2\mathbf{a}_2 + \cdots + x_n\mathbf{a}_n = \mathbf{b}$, hvor $\mathbf{a}_i$ er søjlevektorer og $\mathbf{b}$ er konstantvektoren.</p>
<?/quiz?>

---

<?quiz?>
question: Hvilken af følgende repræsenterer et lineært ligningssystem?
answer-correct: $A\mathbf{x} = \mathbf{b}$
answer: $A + B = C$
answer: $\mathbf{x} \cdot \mathbf{y} = 0$
answer: $A^2 = B$
answer: $\mathbf{x} + \mathbf{y} = \mathbf{z}$
content:
<p><strong>Forklaring:</strong> Et lineært ligningssystem kan skrives som $A\mathbf{x} = \mathbf{b}$, hvor $A$ er koefficientmatricen, $\mathbf{x}$ er variabelvektoren og $\mathbf{b}$ er konstantvektoren.</p>
<?/quiz?>

---

<?quiz?>
question: Hvad er en lineær kombination af vektorer?
answer: Summen af to vektorer
answer-correct: Et udtryk af formen $c_1\mathbf{v}_1 + c_2\mathbf{v}_2 + \cdots + c_k\mathbf{v}_k$
answer: Produktet af to vektorer
answer: Differensen mellem to vektorer
answer: En vektor ganget med en skalar
content:
<p><strong>Forklaring:</strong> En lineær kombination er et udtryk af formen $c_1\mathbf{v}_1 + c_2\mathbf{v}_2 + \cdots + c_k\mathbf{v}_k$, hvor $c_i$ er skalarer og $\mathbf{v}_i$ er vektorer.</p>
<?/quiz?>

---

<?quiz?>
question: Hvad betyder det, når et lineært system har frie variable?
answer: Systemet har ingen løsning
answer: Systemet har præcis én løsning
answer-correct: Systemet har uendeligt mange løsninger
answer: Systemet er inkonsistent
answer: Systemet er overbestemt
content:
<p><strong>Forklaring:</strong> Frie variable betyder, at systemet har uendeligt mange løsninger, da de frie variable kan antage vilkårlige værdier.</p>
<?/quiz?>

---

<?quiz?>
question: Hvad er en homogen ligning?
answer: En ligning med kun positive koefficienter
answer: En ligning med kun negative koefficienter
answer-correct: En ligning af formen $A\mathbf{x} = \mathbf{0}$
answer: En ligning med kun hele tal
answer: En ligning med kun brøker
content:
<p><strong>Forklaring:</strong> En homogen ligning er af formen $A\mathbf{x} = \mathbf{0}$, hvor højresiden er nulvektoren.</p>
<?/quiz?>

---

<?quiz?>
question: Hvad betyder det, at vektorer er lineært uafhængige?
answer: De kan ikke adderes
answer: De kan ikke multipliceres
answer-correct: Ligningen $c_1\mathbf{v}_1 + c_2\mathbf{v}_2 + \cdots + c_k\mathbf{v}_k = \mathbf{0}$ kun har den trivielle løsning
answer: De har samme længde
answer: De peger i samme retning
content:
<p><strong>Forklaring:</strong> Vektorer er lineært uafhængige, hvis ligningen $c_1\mathbf{v}_1 + c_2\mathbf{v}_2 + \cdots + c_k\mathbf{v}_k = \mathbf{0}$ kun har den trivielle løsning $c_1 = c_2 = \cdots = c_k = 0$.</p>
<?/quiz?>

---

<?quiz?>
question: Hvad er parametrisk vektorform?
answer-correct: En måde at skrive løsninger med frie variable som $\mathbf{x} = \mathbf{p} + t_1\mathbf{v}_1 + t_2\mathbf{v}_2 + \cdots$
answer: En måde at skrive vektorer som tal
answer: En måde at multiplicere matricer
answer: En måde at addere vektorer
answer: En måde at beregne determinanter
content:
<p><strong>Forklaring:</strong> Parametrisk vektorform er en måde at skrive løsninger med frie variable som $\mathbf{x} = \mathbf{p} + t_1\mathbf{v}_1 + t_2\mathbf{v}_2 + \cdots$, hvor $\mathbf{p}$ er en partikulær løsning og $t_i$ er parametre.</p>
<?/quiz?>

---

<?quiz?>
question: Hvad er en matrix-vektor multiplikation?
answer: En måde at addere to vektorer
answer: En måde at multiplicere to vektorer
answer-correct: En operation der kombinerer en matrix med en vektor for at producere en ny vektor
answer: En måde at beregne determinanten af en matrix
answer: En måde at finde inverse af en matrix
content:
<p><strong>Forklaring:</strong> Matrix-vektor multiplikation er operationen $A\mathbf{x}$, hvor hver række i $A$ multipliceres med $\mathbf{x}$ for at producere en ny vektor. Det er grundlæggende for at løse lineære ligningssystemer.</p>
<?/quiz?>



