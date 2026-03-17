<h1 align="center">M1: Forberedelse før den første undervisning - Betingede sandsynligheder og Bayes' Teorem</h1>

At forberede sig betyder ikke nødvendigvis at læse alt materiale fra start til slut. Det handler i stedet om at identificere og fokusere på det indhold, der er mest relevant for dig og din forberedelse til undervisningen. Jeg forventer dog, at du har gennemgået og forstået materialet fra tutorials og/eller videoerne. Du kan teste din viden i quizzen, hvor en forståelse anses som tilstrækkelig, hvis du kan svare korrekt på mindst 7 ud af 10 spørgsmål.


<hr>

### Læsemateriale:

Brooks: [Kapitel 5](https://docs.google.com/viewer?url=https://raw.githubusercontent.com/RBrooksDK/MSE_book_v2/master/main.pdf).


<hr>

### Ressourcer

[Noter fra videomateriale](https://drive.google.com/file/d/1kF-E_UrK0OiCLxFTKKqHDkQqRuaymUJ_/view?usp=sharing)

[Andre materialer](https://viaucdk-my.sharepoint.com/:f:/g/personal/rib_viauc_dk/El6TyZ3UNqZDmv4WaAnaxdQBqhXftjEPeBzsfKRGOU6lDg?e=Q3XR6s)


<hr>

### Videomateriale

#### 5.1. Betinget sandsynlighed
<div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%; overflow: hidden;">
    <iframe 
        src="https://drive.google.com/file/d/1ITfcN5gn0yYwDf6Vs5h9tjMEBqMH9zt9/preview" 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
        allow="autoplay; encrypted-media" 
        allowfullscreen>
    </iframe>
</div>

#### 5.2. Uafhængige hændelser
<div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%; overflow: hidden;">
    <iframe 
        src="https://drive.google.com/file/d/14hCe6IKcVX70a8aVr4vE4GM9kLLNzL6D/preview" 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
        allow="autoplay; encrypted-media" 
        allowfullscreen>
    </iframe>
</div>

#### 5.3. Loven om total sandsynlighed
<div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%; overflow: hidden;">
    <iframe 
        src="https://drive.google.com/file/d/1122ymGfyhdAS0X1O5SzQUsN6N8gfMlh1/preview" 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
        allow="autoplay; encrypted-media" 
        allowfullscreen>
    </iframe>
</div>

#### 5.4. Kontingenstabeller
<div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%; overflow: hidden;">
    <iframe 
        src="https://drive.google.com/file/d/14BLwa1I_6kGxgzGKOjytV49AURygGrVy/preview" 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
        allow="autoplay; encrypted-media" 
        allowfullscreen>
    </iframe>
</div>

#### 5.5. Bayes' teorem
<div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%; overflow: hidden;">
    <iframe 
        src="https://drive.google.com/file/d/1d2b8K1K483WTycyuxm57MBwHQFItdpxN/preview" 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
        allow="autoplay; encrypted-media" 
        allowfullscreen>
    </iframe>
</div>


<hr>

### Quiz
Når du har været igennem videoerne og/eller læst materialet i dette modul, kan du teste din viden i quizzen. Quizzen indeholder 10 spørgsmål, og en forståelse anses som tilstrækkelig, hvis du kan svare korrekt på mindst 7 ud af 10 spørgsmål. Du kan se din samlede score nederst på siden, og du kan også se din score for hvert spørgsmål. Du kan tage quizzen så mange gange, og dine resulter bliver hverken gemt eller vurderet. Quizzen er kun til din egen skyld, så du kan se, hvor godt du har forstået materialet.

<?quiz?>
question: Hvad er definitionen af betinget sandsynlighed P(A|B)?
answer: P(A|B) = P(A) + P(B)
answer: P(A|B) = P(A) · P(B)
answer-correct: P(A|B) = P(A ∩ B) / P(B)
answer: P(A|B) = P(A ∪ B) / P(B)
answer: P(A|B) = P(A) - P(B)
content:
<p><strong>Forklaring:</strong> Betinget sandsynlighed er defineret som P(A|B) = P(A ∩ B) / P(B), hvor P(B) > 0.</p>
<?/quiz?>

---

<?quiz?>
question: Hvilken af følgende formler repræsenterer loven om total sandsynlighed?
answer: P(A) = P(A|B) · P(B)
answer-correct: P(A) = Σ P(A|B_i) · P(B_i)
answer: P(A) = P(A ∩ B) / P(B)
answer: P(A) = P(A ∪ B) - P(B)
answer: P(A) = P(A) · P(B)
content:
<p><strong>Forklaring:</strong> Loven om total sandsynlighed siger, at P(A) = Σ P(A|B_i) · P(B_i) hvor {B_i} er en partition af udfaldsrummet.</p>
<?/quiz?>

---

<?quiz?>
question: Hvad er Bayes' teorem?
answer: P(A|B) = P(B|A) · P(A)
answer-correct: P(A|B) = P(B|A) · P(A) / P(B)
answer: P(A|B) = P(A ∩ B) / P(A)
answer: P(A|B) = P(A) + P(B) - P(A ∩ B)
answer: P(A|B) = P(A) · P(B)
content:
<p><strong>Forklaring:</strong> Bayes' teorem er P(A|B) = P(B|A) · P(A) / P(B), som giver os mulighed for at "vende" betingede sandsynligheder.</p>
<?/quiz?>

---

<?quiz?>
question: Hvornår er to hændelser A og B uafhængige?
answer: Når P(A|B) = P(B|A)
answer: Når P(A) = P(B)
answer-correct: Når P(A ∩ B) = P(A) · P(B)
answer: Når P(A ∪ B) = P(A) + P(B)
answer: Når P(A|B) = 0
content:
<p><strong>Forklaring:</strong> To hændelser er uafhængige hvis og kun hvis P(A ∩ B) = P(A) · P(B).</p>
<?/quiz?>

---

<?quiz?>
question: Hvad er forskellen mellem a priori og a posteriori sandsynlighed?
answer: Der er ingen forskel - de betyder det samme
answer-correct: A priori er sandsynligheden før information, a posteriori er sandsynligheden efter information
answer: A priori er sandsynligheden efter information, a posteriori er sandsynligheden før information
answer: A priori er altid større end a posteriori
answer: A priori er altid mindre end a posteriori
content:
<p><strong>Forklaring:</strong> A priori sandsynlighed er sandsynligheden før vi har nogen information, mens a posteriori sandsynlighed er sandsynligheden efter vi har fået ny information.</p>
<?/quiz?>

---

<?quiz?>
question: Hvad er en partition af et udfaldsrum S?
answer: En mængde af overlappende hændelser
answer-correct: En disjunkt og komplet opdeling af S
answer: En mængde af uafhængige hændelser
answer: En mængde af lige sandsynlige hændelser
answer: En mængde af komplementære hændelser
content:
<p><strong>Forklaring:</strong> En partition er en disjunkt og komplet opdeling af udfaldsrummet S, dvs. hændelserne er disjunkte og deres forening er S.</p>
<?/quiz?>

---

<?quiz?>
question: Hvad er sandsynligheden for unionen P(A ∪ B) hvis A og B er to hændelser?
answer: P(A ∪ B) = P(A) + P(B)
answer-correct: P(A ∪ B) = P(A) + P(B) - P(A ∩ B)
answer: P(A ∪ B) = P(A) · P(B)
answer: P(A ∪ B) = P(A) - P(B)
answer: P(A ∪ B) = P(A ∩ B)
content:
<p><strong>Forklaring:</strong> Sandsynligheden for unionen af to hændelser er P(A ∪ B) = P(A) + P(B) - P(A ∩ B). Vi trækker P(A ∩ B) fra for at undgå at tælle fællesmængden dobbelt.</p>
<?/quiz?>

---

<?quiz?>
question: Hvad er komplementreglen for sandsynlighed?
answer: P(A^c) = P(A)
answer: P(A^c) = 0
answer-correct: P(A^c) = 1 - P(A)
answer: P(A^c) = P(A) - 1
answer: P(A^c) = 1 / P(A)
content:
<p><strong>Forklaring:</strong> Komplementreglen siger, at P(A^c) = 1 - P(A), da A og A^c tilsammen udgør hele udfaldsrummet.</p>
<?/quiz?>

---

<?quiz?>
question: Hvordan beregner man marginale sandsynligheder fra en kontingenstabel?
answer: Ved at dividere fællesfrekvenser med totalen
answer-correct: Ved at dividere række- eller søjlesummer med totalen
answer: Ved at multiplicere fællesfrekvenser med totalen
answer: Ved at addere alle fællesfrekvenser
answer: Ved at subtrahere fællesfrekvenser fra totalen
content:
<p><strong>Forklaring:</strong> Marginale sandsynligheder beregnes som P(A_i) = n_{i+}/n og P(B_j) = n_{+j}/n, hvor n_{i+} og n_{+j} er række- og søjlesummer.</p>
<?/quiz?>

---

<?quiz?>
question: Hvad er sandsynligheden for unionen P(A ∪ B) hvis A og B er hændelser?
answer: P(A ∪ B) = P(A) + P(B)
answer-correct: P(A ∪ B) = P(A) + P(B) - P(A ∩ B)
answer: P(A ∪ B) = P(A) · P(B)
answer: P(A ∪ B) = P(A) - P(B)
answer: P(A ∪ B) = P(A ∩ B)
content:
<p><strong>Forklaring:</strong> Sandsynligheden for unionen af to hændelser er P(A ∪ B) = P(A) + P(B) - P(A ∩ B). Vi trækker P(A ∩ B) fra for at undgå at tælle fællesmængden dobbelt.</p>
<?/quiz?>



