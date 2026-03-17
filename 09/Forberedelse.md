<h1 align="center">M1: Forberedelse før den første undervisning - Matrix algebra og invertible matricer</h1>

At forberede sig betyder ikke nødvendigvis at læse alt materiale fra start til slut. Det handler i stedet om at identificere og fokusere på det indhold, der er mest relevant for dig og din forberedelse til undervisningen. Jeg forventer dog, at du har gennemgået og forstået materialet fra tutorials og/eller videoerne. Du kan teste din viden i quizzen, hvor en forståelse anses som tilstrækkelig, hvis du kan svare korrekt på mindst 7 ud af 10 spørgsmål.


<hr>

### Læsemateriale:

Brooks: [Kapitel 9](https://docs.google.com/viewer?url=https://raw.githubusercontent.com/RBrooksDK/MSE_book_v2/master/main.pdf).


<hr>

### Ressourcer

[Noter fra videomateriale](https://drive.google.com/file/d/14d3mLRa3KcwYXhO-MUCzcKkV9730vk_o/view?usp=sharing)

[Andre materialer](https://viaucdk-my.sharepoint.com/:f:/g/personal/rib_viauc_dk/EpGNNUp8hjpPn6niIxD8hT4BdSOLqNwtdY91GTRCdj7D_g?e=xE3Dfj)


<hr>

### Videomateriale

#### 9.1. Addition og skalarmultiplikation

<div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%; overflow: hidden;">
    <iframe 
        src="https://drive.google.com/file/d/13Zdx2Y_p9EH4DadiAQuzNddx4EwBW5vF/preview" 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
        allow="autoplay; encrypted-media" 
        allowfullscreen>
    </iframe>
</div>



#### 9.2. Matrixmultiplikation

<div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%; overflow: hidden;">
    <iframe 
        src="https://drive.google.com/file/d/1XMaut9NZReXgzf3ZwusSwynyHBnrIN5U/preview" 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
        allow="autoplay; encrypted-media" 
        allowfullscreen>
    </iframe>
</div>

#### 9.3. Den transponerede

<div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%; overflow: hidden;">
    <iframe 
        src="https://drive.google.com/file/d/1fy8lLScQAyOUI3orXltM038p5UZbvaIw/preview" 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
        allow="autoplay; encrypted-media" 
        allowfullscreen>
    </iframe>
</div>

#### 9.4. Invertible matricer

<div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%; overflow: hidden;">
    <iframe 
        src="https://drive.google.com/file/d/1xm3tjvzSVHQBCMbNQ04JP2l-u7VGpkO-/preview" 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
        allow="autoplay; encrypted-media" 
        allowfullscreen>
    </iframe>
</div>

#### 9.5. Teoremet om invertible matricer

<div style="position: relative; width: 100%; height: 0; padding-bottom: 56.25%; overflow: hidden;">
    <iframe 
        src="https://drive.google.com/file/d/1L_7CjSz4p59eI0UpF6aoFgLKSli3LOXg/preview" 
        style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;" 
        allow="autoplay; encrypted-media" 
        allowfullscreen>
    </iframe>
</div>


<hr>

### Quiz
Når du har været igennem videoerne og/eller læst materialet i dette modul, kan du teste din viden i quizzen. Quizzen indeholder 10 spørgsmål, og en forståelse anses som tilstrækkelig, hvis du kan svare korrekt på mindst 7 ud af 10 spørgsmål. Du kan se din samlede score nederst på siden, og du kan også se din score for hvert spørgsmål. Du kan tage quizzen så mange gange, og dine resulter bliver hverken gemt eller vurderet. Quizzen er kun til din egen skyld, så du kan se, hvor godt du har forstået materialet.

<?quiz?>
question: Hvad er den afgørende betingelse for, at matrixproduktet AB er defineret?
answer: A og B skal have samme dimensioner.
answer-correct: Antallet af søjler i A skal være lig med antallet af rækker i B.
answer: Antallet af rækker i A skal være lig med antallet af søjler i B.
answer: A og B skal begge være kvadratiske matricer.
answer: A og B skal være symmetriske.
content:
<p><strong>Forklaring:</strong> For at matrixproduktet AB skal være defineret, skal dimensionerne "matche" således, at antallet af søjler i den første matrix (A) er identisk med antallet af rækker i den anden matrix (B).</p>
<?/quiz?>

---

<?quiz?>
question: Hvilket udsagn om matrixmultiplikation er generelt sandt?
answer: Matrixmultiplikation er altid kommutativ, dvs. AB = BA.
answer: AB er kun defineret, hvis BA også er defineret.
answer-correct: Matrixmultiplikation er ikke kommutativ, dvs. AB ≠ BA i de fleste tilfælde.
answer: Resultatet af AB har altid samme dimension som A.
answer: Matrixmultiplikation er kun defineret for invertible matricer.
content:
<p><strong>Forklaring:</strong> I modsætning til almindelig talmultiplikation er rækkefølgen afgørende for matricer. I de fleste tilfælde vil AB og BA ikke give det samme resultat, og det er endda muligt, at kun ét af produkterne er defineret.</p>
<?/quiz?>

---

<?quiz?>
question: Hvad er en identitetsmatrix' rolle i matrix algebra?
answer: Den består udelukkende af nuller.
answer: Den bruges til at fordoble alle elementer i en matrix.
answer-correct: Den fungerer som det neutrale element for multiplikation, ligesom tallet 1 i almindelig aritmetik.
answer: Enhver matrix multipliceret med identitetsmatricen giver nulmatricen.
answer: Den kan kun multipliceres med sig selv.
content:
<p><strong>Forklaring:</strong> Identitetsmatricen, I, er en kvadratisk matrix med 1-taller i diagonalen og 0-taller alle andre steder. For enhver matrix A, hvor multiplikationen er defineret, gælder det, at AI = A og IA = A.</p>
<?/quiz?>

---

<?quiz?>
question: Hvad kendetegner den transponerede af en matrix, $A^T$?
answer: Alle elementer i A bliver negative.
answer: Rækkefølgen af søjlerne i A bliver omvendt.
answer: Det er det samme som den inverse af A.
answer-correct: Rækkerne i A bliver til søjlerne i $A^T$.
answer: Den transponerede kan kun findes for matricer med en determinant på 0.
content:
<p><strong>Forklaring:</strong> Transponering er en operation, hvor man "vender" matricen om dens diagonal. Den i'te række i A bliver til den i'te søjle i $A^T$.</p>
<?/quiz?>

---

<?quiz?>
question: Hvornår siges en kvadratisk matrix A at være invertibel?
answer: Hvis dens determinant er lig med 0.
answer: Hvis alle dens elementer er forskellige fra nul.
answer-correct: Hvis der eksisterer en matrix $A^{-1}$, så $AA^{-1} = A^{-1}A = I$.
answer: Hvis den er rækkeækvivalent med nulmatricen.
answer: Hvis den kun indeholder positive tal.
content:
<p><strong>Forklaring:</strong> En matrix er invertibel, hvis den har en invers, $A^{-1}$, som, når den multipliceres med A, resulterer i identitetsmatricen I. Dette er analogt med at finde den reciprokke værdi af et tal.</p>
<?/quiz?>

---

<?quiz?>
question: For en 2x2 matrix, hvad fortæller determinanten os om matrixens invertibilitet?
answer: Hvis determinanten er positiv, er matricen invertibel.
answer-correct: Hvis determinanten er forskellig fra nul, er matricen invertibel.
answer: Hvis determinanten er 1, er matricen ikke invertibel.
answer: Determinanten har ingen betydning for invertibilitet.
answer: Kun matricer med en determinant på 0 er invertible.
content:
<p><strong>Forklaring:</strong> Determinanten er en skalarværdi, der kan beregnes fra en kvadratisk matrix. En afgørende egenskab er, at matricen kun har en invers, hvis og kun hvis dens determinant er forskellig fra nul.</p>
<?/quiz?>

---

<?quiz?>
question: Hvad er den korrekte formel for den inverse af et produkt af to invertible matricer, A og B?
answer: $(AB)^{-1} = A^{-1}B^{-1}$
answer: $(AB)^{-1} = (BA)^{-1}$
answer: $(AB)^{-1} = A^{-1} + B^{-1}$
answer-correct: $(AB)^{-1} = B^{-1}A^{-1}$
answer: $(AB)^{-1} = (A^T B^T)^{-1}$
content:
<p><strong>Forklaring:</strong> Når man tager den inverse af et produkt af matricer, bytter man om på rækkefølgen og tager den inverse af hver enkelt. Dette kaldes "socks-shoes property".</p>
<?/quiz?>

---

<?quiz?>
question: Hvis en n x n matrix A er invertibel, hvad er den unikke løsning til matrixligningen $A\mathbf{x} = \mathbf{b}$?
answer: $\mathbf{x} = \mathbf{b}A^{-1}$
answer: $\mathbf{x} = A\mathbf{b}$
answer: Ligningen har ingen løsning.
answer-correct: $\mathbf{x} = A^{-1}\mathbf{b}$
answer: $\mathbf{x} = \mathbf{b}$
content:
<p><strong>Forklaring:</strong> Ved at multiplicere med $A^{-1}$ fra venstre på begge sider af ligningen ($A^{-1}A\mathbf{x} = A^{-1}\mathbf{b}$) kan man isolere $\mathbf{x}$, da $A^{-1}A = I$. Dette giver den unikke løsning $\mathbf{x} = A^{-1}\mathbf{b}$.</p>
<?/quiz?>

---

<?quiz?>
question: Ifølge "The Invertible Matrix Theorem", hvilket af følgende udsagn er IKKE ækvivalent med, at en n x n matrix A er invertibel?
answer: A er rækkeækvivalent med identitetsmatricen $I_n$.
answer-correct: Ligningen $A\mathbf{x} = \mathbf{0}$ har uendeligt mange løsninger.
answer: A har n pivotpositioner.
answer: Søjlerne i A er lineært uafhængige.
answer: $A^T$ er invertibel.
content:
<p><strong>Forklaring:</strong> "The Invertible Matrix Theorem" fastslår, at hvis A er invertibel, så har den homogene ligning $A\mathbf{x} = \mathbf{0}$ kun den trivielle løsning ($\mathbf{x} = \mathbf{0}$). Hvis den har uendeligt mange løsninger, er A netop *ikke* invertibel.</p>
<?/quiz?>

---

<?quiz?>
question: Hvad er en forudsætning for at kunne beregne potensen af en matrix, $A^k$?
answer: A skal være invertibel.
answer: A må kun indeholde positive tal.
answer-correct: A skal være en kvadratisk matrix.
answer: k skal være et lige tal.
answer: A skal være en rækkevektor.
content:
<p><strong>Forklaring:</strong> Matrixpotenser, $A^k = A \cdot A \cdot \ldots \cdot A$, er defineret ved at multiplicere matricen med sig selv. Da matrixmultiplikation kræver, at antallet af søjler i den første matrix matcher antallet af rækker i den anden, kan A kun multipliceres med sig selv, hvis den har lige mange rækker og søjler, dvs. er kvadratisk.</p>
<?/quiz?>

