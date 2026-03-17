<h1 align="center">M1: Forberedelse før den første undervisning - Kombinatorik og sandsynlighedsteori</h1>

At forberede sig betyder ikke nødvendigvis at læse alt materiale fra start til slut. Det handler i stedet om at identificere og fokusere på det indhold, der er mest relevant for dig og din forberedelse til undervisningen. Jeg forventer dog, at du har gennemgået og forstået materialet fra tutorials og/eller videoerne. Du kan teste din viden i quizzen, hvor en forståelse anses som tilstrækkelig, hvis du kan svare korrekt på mindst 7 ud af 10 spørgsmål.


<hr>

### Læsemateriale:

Brooks: [Kapitel 4](https://docs.google.com/viewer?url=https://raw.githubusercontent.com/RBrooksDK/MSE_book_v2/master/main.pdf).


<hr>

### Ressourcer

[Noter fra videomateriale](https://drive.google.com/file/d/1zKyM3CnrKBoLwOabxI1NSx4PnUQ291A1/view?usp=sharing)

[Andre materialer](https://viaucdk-my.sharepoint.com/:f:/g/personal/rib_viauc_dk/EsJDXlP48H5Nnak20uj9FMYBWN_47BOjpk_K1Lso5NxBoA?e=ooXo2d)


<hr>

### Videomateriale

#### 4.1. Udfaldsrum og hændelser

<div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%; overflow: hidden;">
    <iframe 
        src="https://drive.google.com/file/d/1UOf9RqyH2exKC-IH7JFMUcHKSAPJRfUJ/preview" 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
        allow="autoplay; encrypted-media" 
        allowfullscreen>
    </iframe>
</div>

#### 4.2. Tælleteknikker

<div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%; overflow: hidden;">
    <iframe 
        src="https://drive.google.com/file/d/1NajfuFf7PhnrkFm7eQ3DtNXkBCGTKIzc/preview" 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
        allow="autoplay; encrypted-media" 
        allowfullscreen>
    </iframe>
</div>

#### 4.3. Permutationer og kombinationer

<div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%; overflow: hidden;">
    <iframe 
        src="https://drive.google.com/file/d/1-mpao9UsCyMZCPj7OqPeJaFnPRufZ3Sl/preview" 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
        allow="autoplay; encrypted-media" 
        allowfullscreen>
    </iframe>
</div>

#### 4.4. Sandsynligheder

<div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%; overflow: hidden;">
    <iframe 
        src="https://drive.google.com/file/d/1dU89-ePN1O3jkaxmRzHxjZik7wq-c2sg/preview" 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
        allow="autoplay; encrypted-media" 
        allowfullscreen>
    </iframe>
</div>

<hr>

### Quiz
Når du har været igennem videoerne og/eller læst materialet i dette modul, kan du teste din viden i quizzen. Quizzen indeholder 10 spørgsmål, og en forståelse anses som tilstrækkelig, hvis du kan svare korrekt på mindst 7 ud af 10 spørgsmål. Du kan se din samlede score nederst på siden, og du kan også se din score for hvert spørgsmål. Du kan tage quizzen så mange gange, og dine resulter bliver hverken gemt eller vurderet. Quizzen er kun til din egen skyld, så du kan se, hvor godt du har forstået materialet.

<?quiz?>
question: Hvilken af følgende beskriver bedst multiplikationsprincippet?
answer: Antallet af måder at udføre en opgave på er summen af alle mulige måder
answer-correct: Antallet af måder at udføre en opgave på er produktet af antal måder for hvert trin
answer: Multiplikationsprincippet gælder kun for permutationer
answer: Multiplikationsprincippet gælder kun for kombinationer
answer: Multiplikationsprincippet bruges kun til at beregne sandsynligheder
content:
<p><strong>Forklaring:</strong> Multiplikationsprincippet siger, at hvis en opgave kan opdeles i k trin, hvor hvert trin kan udføres på n_i måder, så kan hele opgaven udføres på n_1 · n_2 · ... · n_k måder.</p>
<?/quiz?>

---

<?quiz?>
question: Hvad er forskellen mellem permutationer og kombinationer?
answer: Der er ingen forskel - de betyder det samme
answer: Permutationer bruges kun til sandsynlighedsberegninger
answer-correct: Permutationer tager højde for rækkefølge, kombinationer gør ikke
answer: Kombinationer tager højde for rækkefølge, permutationer gør ikke
answer: Permutationer bruges kun for uendelige mængder
content:
<p><strong>Forklaring:</strong> En permutation er et ordnet arrangement af elementer, mens en kombination er et uordnet udvalg. Rækkefølgen betyder noget for permutationer, men ikke for kombinationer.</p>
<?/quiz?>

---

<?quiz?>
question: Hvilken af følgende formler bruges til at beregne antallet af kombinationer af r elementer valgt fra n elementer?
answer: $\frac{n!}{(n-r)!}$
answer: $n^r$
answer-correct: $\frac{n!}{r!(n-r)!}$
answer: $\frac{r!}{n!(r-n)!}$
answer: $n \cdot r$
content:
<p><strong>Forklaring:</strong> Antallet af kombinationer er givet ved binomialkoefficienten $\binom{n}{r} = \frac{n!}{r!(n-r)!}$. Dette tager højde for, at rækkefølgen ikke betyder noget.</p>
<?/quiz?>

---

<?quiz?>
question: Hvad er sandsynligheden for en hændelse E i et udfaldsrum S med lige sandsynlige udfald?
answer: $P(E) = \frac{|S|}{|E|}$
answer-correct: $P(E) = \frac{|E|}{|S|}$
answer: $P(E) = |E| \cdot |S|$
answer: $P(E) = |E| - |S|$
answer: $P(E) = |E| + |S|$
content:
<p><strong>Forklaring:</strong> For lige sandsynlige udfald er sandsynligheden for hændelse E lig med antallet af gunstige udfald (|E|) divideret med antallet af mulige udfald (|S|).</p>
<?/quiz?>

---

<?quiz?>
question: Hvilken af følgende er komplementreglen for sandsynlighed?
answer: $P(E^c) = P(E)$
answer: $P(E^c) = 0$
answer-correct: $P(E^c) = 1 - P(E)$
answer: $P(E^c) = P(E) - 1$
answer: $P(E^c) = \frac{1}{P(E)}$
content:
<p><strong>Forklaring:</strong> Komplementreglen siger, at sandsynligheden for komplementet til en hændelse E er lig med 1 minus sandsynligheden for E. Dette gælder fordi E og E^c tilsammen udgør hele udfaldsrummet.</p>
<?/quiz?>

---

<?quiz?>
question: Hvornår er to hændelser E1 og E2 uafhængige?
answer: Når de ikke kan ske samtidigt
answer: Når de har samme sandsynlighed
answer-correct: Når P(E1 ∩ E2) = P(E1) · P(E2)
answer: Når P(E1 ∪ E2) = P(E1) + P(E2)
answer: Når de er disjunkte
content:
<p><strong>Forklaring:</strong> To hændelser er uafhængige, hvis sandsynligheden for deres fællesmængde er lig med produktet af deres individuelle sandsynligheder. Dette betyder, at forekomsten af den ene hændelse ikke påvirker sandsynligheden for den anden.</p>
<?/quiz?>

---

<?quiz?>
question: Hvad er betinget sandsynlighed P(E2|E1)?
answer: Sandsynligheden for E1 givet E2
answer-correct: Sandsynligheden for E2 givet E1
answer: Sandsynligheden for E1 eller E2
answer: Sandsynligheden for E1 og E2
answer: Sandsynligheden for E1 minus E2
content:
<p><strong>Forklaring:</strong> Betinget sandsynlighed P(E2|E1) er sandsynligheden for at hændelse E2 indtræffer, givet at hændelse E1 allerede er indtruffet. Den beregnes som P(E1 ∩ E2) / P(E1).</p>
<?/quiz?>

---

<?quiz?>
question: Hvilken af følgende beskriver bedst additionsprincippet?
answer-correct: Antallet af måder at udføre en opgave på er summen af antal måder for hver uafhængig metode
answer: Antallet af måder at udføre en opgave på er produktet af antal måder for hver metode
answer: Additionsprincippet bruges kun til permutationer
answer: Additionsprincippet bruges kun til kombinationer
answer: Additionsprincippet gælder kun for uafhængige hændelser
content:
<p><strong>Forklaring:</strong> Additionsprincippet siger, at hvis en opgave kan udføres på k forskellige måder, hvor hver måde er uafhængig af de andre, så kan opgaven udføres på n_1 + n_2 + ... + n_k måder i alt.</p>
<?/quiz?>

---

<?quiz?>
question: Hvad er forskellen mellem "med tilbagelægning" og "uden tilbagelægning"?
answer: Der er ingen forskel - de betyder det samme
answer-correct: Med tilbagelægning betyder at elementer kan gentages, uden tilbagelægning betyder at de ikke kan
answer: Uden tilbagelægning betyder at elementer kan gentages, med tilbagelægning betyder at de ikke kan
answer: Det afhænger af om det er permutationer eller kombinationer
answer: Det afhænger af om det er sandsynlighedsberegninger eller tælleproblemer
content:
<p><strong>Forklaring:</strong> "Med tilbagelægning" betyder, at et element kan vælges flere gange (gentages), mens "uden tilbagelægning" betyder, at hvert element kun kan vælges én gang. Dette påvirker både tælleformler og sandsynlighedsberegninger.</p>
<?/quiz?>

---

<?quiz?>
question: Hvilken af følgende formler bruges til at beregne antallet af permutationer af r elementer valgt fra n elementer?
answer: $\frac{n!}{r!(n-r)!}$
answer-correct: $\frac{n!}{(n-r)!}$
answer: $n^r$
answer: $\frac{r!}{n!(r-n)!}$
answer: $n \cdot r$
content:
<p><strong>Forklaring:</strong> Antallet af permutationer er givet ved P(n,r) = $\frac{n!}{(n-r)!}$. Dette tager højde for, at rækkefølgen betyder noget, og at der ikke er tilbagelægning.</p>
<?/quiz?>



