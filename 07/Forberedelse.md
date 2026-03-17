<h1 align="center">M1: Forberedelse før den første undervisning - Introduktion til lineær algebra</h1>

At forberede sig betyder ikke nødvendigvis at læse alt materiale fra start til slut. Det handler i stedet om at identificere og fokusere på det indhold, der er mest relevant for dig og din forberedelse til undervisningen. Jeg forventer dog, at du har gennemgået og forstået materialet fra tutorials og/eller videoerne. Du kan teste din viden i quizzen, hvor en forståelse anses som tilstrækkelig, hvis du kan svare korrekt på mindst 7 ud af 10 spørgsmål.


<hr>

### Læsemateriale:

Brooks: [Kapitel 7](https://docs.google.com/viewer?url=https://raw.githubusercontent.com/RBrooksDK/MSE_book_v2/master/main.pdf).


<hr>

### Ressourcer

[Noter fra videomateriale](https://drive.google.com/file/d/1U0fPEaOrso99t3N2jdi1tb_6-u73QGd-/view?usp=sharing)

[Andre materialer](https://viaucdk-my.sharepoint.com/:f:/g/personal/rib_viauc_dk/EkjUOJhNa7lFscFUs9rWtwsB_2p-THcKaRcRj3M3LYR99g?e=av1cs5)


<hr>

### Videomateriale

#### 7.1. Lineære ligningssystemer

<div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%; overflow: hidden;">
    <iframe 
        src="https://drive.google.com/file/d/1uRWzqqKZHXwc9dZjAOaJ_UCrG3h74S2N/preview" 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
        allow="autoplay; encrypted-media" 
        allowfullscreen>
    </iframe>
</div>

#### 7.2. The Matrix

<div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%; overflow: hidden;">
    <iframe 
        src="https://drive.google.com/file/d/1mk-n7buSRbaiESQvBVeXQOIC6HFPiuoo/preview" 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
        allow="autoplay; encrypted-media" 
        allowfullscreen>
    </iframe>
</div>

#### 7.3. Elementære rækkeoperationer

<div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%; overflow: hidden;">
    <iframe 
        src="https://drive.google.com/file/d/1sBybIL3lIL1dXakBGS6H13J8b7cRWMQy/preview" 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
        allow="autoplay; encrypted-media" 
        allowfullscreen>
    </iframe>
</div>

#### 7.4. Echelon former

<div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%; overflow: hidden;">
    <iframe 
        src="https://drive.google.com/file/d/1TxR8bX70nIgH_Fovh_yHpX3YR1vb_dBD/preview" 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
        allow="autoplay; encrypted-media" 
        allowfullscreen>
    </iframe>
</div>

<hr>

### Quiz
Når du har været igennem videoerne og/eller læst materialet i dette modul, kan du teste din viden i quizzen. Quizzen indeholder 10 spørgsmål, og en forståelse anses som tilstrækkelig, hvis du kan svare korrekt på mindst 7 ud af 10 spørgsmål. Du kan se din samlede score nederst på siden, og du kan også se din score for hvert spørgsmål. Du kan tage quizzen så mange gange, og dine resulter bliver hverken gemt eller vurderet. Quizzen er kun til din egen skyld, så du kan se, hvor godt du har forstået materialet.

<?quiz?>
question: Hvad er en lineær ligning?
answer: En ligning med kun variable
answer-correct: En ligning af formen $a_1x_1 + a_2x_2 + \cdots + a_nx_n = b$ hvor $a_i$ og $b$ er konstanter
answer: En ligning med kun konstanter
answer: En ligning med kun brøker
answer: En ligning med kun potenser
content:
<p><strong>Forklaring:</strong> En lineær ligning er af formen $a_1x_1 + a_2x_2 + \cdots + a_nx_n = b$ hvor $a_1, a_2, \ldots, a_n$ og $b$ er konstanter.</p>
<?/quiz?>

---

<?quiz?>
question: Hvad er en augmenteret matrix?
answer: En matrix med kun koefficienter
answer: En matrix med kun konstanter
answer-correct: En matrix der indeholder både koefficienter og konstanter fra højresiden af ligningerne
answer: En matrix med kun variable
answer: En matrix med kun nuller
content:
<p><strong>Forklaring:</strong> En augmenteret matrix indeholder koefficienterne fra ligningssystemet plus en ekstra søjle med konstanterne fra højresiden.</p>
<?/quiz?>

---

<?quiz?>
question: Hvilke tre typer elementære rækkeoperationer findes der?
answer: Addition, subtraktion og multiplikation
answer: Division, potensopløftning og kvadratrod
answer-correct: Erstatning, ombytning og skalering
answer: Integration, differentiering og grænseværdi
answer: Logaritme, eksponential og trigonometri
content:
<p><strong>Forklaring:</strong> De tre elementære rækkeoperationer er: 1) Erstatning (erstat en række med summen af sig selv og et multiplum af en anden række), 2) Ombytning (bytte to rækker), 3) Skalering (multiplicer alle elementer i en række med en konstant).</p>
<?/quiz?>

---

<?quiz?>
question: Hvad er echelon form?
answer: En matrix hvor alle elementer er 1
answer-correct: En matrix hvor alle nulrækker er nederst og hver ledende indgang er til højre for den ovenstående
answer: En matrix hvor alle elementer er 0
answer: En matrix hvor alle elementer er lige
answer: En matrix hvor alle elementer er ulige
content:
<p><strong>Forklaring:</strong> En matrix er i echelon form hvis: 1) Alle nulrækker er nederst, 2) Hver ledende indgang er i en søjle til højre for den ovenstående, 3) Alle elementer under en ledende indgang er nuller.</p>
<?/quiz?>

---

<?quiz?>
question: Hvad er reduceret echelon form (RREF)?
answer: En matrix hvor alle elementer er 1
answer: En matrix hvor alle elementer er 0
answer-correct: En echelon matrix hvor hver ledende indgang er 1 og den eneste ikke-nul indgang i sin søjle
answer: En matrix hvor alle elementer er lige
answer: En matrix hvor alle elementer er ulige
content:
<p><strong>Forklaring:</strong> RREF er en echelon form hvor: 1) Hver ledende indgang er 1, 2) Hver ledende 1 er den eneste ikke-nul indgang i sin søjle.</p>
<?/quiz?>

---

<?quiz?>
question: Hvornår er et lineært system konsistent?
answer: Når det har præcis én løsning
answer: Når det har uendeligt mange løsninger
answer-correct: Når det har enten én eller uendeligt mange løsninger
answer: Når det har ingen løsninger
answer: Når det har negative løsninger
content:
<p><strong>Forklaring:</strong> Et system er konsistent hvis det har mindst én løsning (enten én unik løsning eller uendeligt mange løsninger). Det er inkonsistent hvis det har ingen løsninger.</p>
<?/quiz?>

---

<?quiz?>
question: Hvad er en pivot position?
answer: En position hvor alle elementer er 0
answer-correct: En position i en matrix der svarer til en ledende 1 i den reducerede echelon form
answer: En position hvor alle elementer er 1
answer: En position hvor alle elementer er negative
answer: En position hvor alle elementer er brøker
content:
<p><strong>Forklaring:</strong> En pivot position er en position i en matrix $A$ der svarer til en ledende 1 i den reducerede echelon form af $A$.</p>
<?/quiz?>

---

<?quiz?>
question: Hvad er forskellen mellem basiske og frie variable?
answer: Der er ingen forskel
answer: Basiske variable er altid 0
answer-correct: Basiske variable svarer til pivot søjler, frie variable svarer til ikke-pivot søjler
answer: Frie variable er altid 1
answer: Basiske variable er altid negative
content:
<p><strong>Forklaring:</strong> Basiske variable svarer til pivot søjler i den augmenterede matrix, mens frie variable svarer til ikke-pivot søjler og kan antage vilkårlige værdier.</p>
<?/quiz?>

---

<?quiz?>
question: Hvad er row reduction algoritmen?
answer: En algoritme til at addere matricer
answer: En algoritme til at multiplicere matricer
answer-correct: En algoritme til at omdanne en matrix til echelon form eller reduceret echelon form
answer: En algoritme til at finde determinanten
answer: En algoritme til at finde inverse matricer
content:
<p><strong>Forklaring:</strong> Row reduction algoritmen er en systematisk metode til at omdanne en matrix til echelon form eller reduceret echelon form ved hjælp af elementære rækkeoperationer.</p>
<?/quiz?>

---

<?quiz?>
question: Hvad betyder det, når en augmenteret matrix har en række af formen $[0 \ldots 0 \mid b]$ hvor $b \neq 0$?
answer: Systemet har en unik løsning
answer: Systemet har uendeligt mange løsninger
answer-correct: Systemet er inkonsistent og har ingen løsning
answer: Systemet har negative løsninger
answer: Systemet har komplekse løsninger
content:
<p><strong>Forklaring:</strong> En række af formen $[0 \ldots 0 \mid b]$ hvor $b \neq 0$ svarer til ligningen $0 = b$, hvilket er en modsigelse og betyder at systemet er inkonsistent.</p>
<?/quiz?>



