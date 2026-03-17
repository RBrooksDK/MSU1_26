<h1 align="center">Tutorial 2: Talsystemer</h1>

Efter denne tutorial vil du kunne:

*   Forstå hvordan forskellige talsystemer (binær, decimal, hexadecimal) fungerer
*   Konvertere mellem binære tal og decimale tal i begge retninger
*   Konvertere mellem hexadecimale tal og decimale tal i begge retninger
*   Konvertere mellem binære og hexadecimale tal
*   Udføre simple regneoperationer med binære tal (addition og multiplikation)
*   Forstå sammenhængen mellem forskellige talsystemer og deres anvendelse i programmering

## 1. Grundlæggende om Talsystemer

Et **talsystem** er en måde at repræsentere tal på ved hjælp af cifre. Det talsystem vi bruger til daglig er **decimalsystemet** (grundtal 10), som bruger cifrene 0-9.

**Grundtal (base)** angiver hvor mange forskellige cifre der bruges i systemet:

  - **Decimalsystemet** (base 10): Bruger cifrene 0, 1, 2, 3, 4, 5, 6, 7, 8, 9
  - **Binærsystemet** (base 2): Bruger kun cifrene 0 og 1
  - **Hexadecimalsystemet** (base 16): Bruger cifrene 0-9 og bogstaverne A-F (hvor $A=10, B=11, C=12, D=13, E=14, F=15$)

## 2. Positionsværdi og Udvidelse

I alle talsystemer har hver position en bestemt værdi baseret på grundtallet opløftet til en potens.

**Decimalsystemet:** Tallet $1234_{10}$ kan skrives som:

$$1 \cdot 10^3 + 2 \cdot 10^2 + 3 \cdot 10^1 + 4 \cdot 10^0 = 1000 + 200 + 30 + 4 = 1234$$

**Binærsystemet:** Tallet $1101_2$ kan skrives som:

$$1 \cdot 2^3 + 1 \cdot 2^2 + 0 \cdot 2^1 + 1 \cdot 2^0 = 8 + 4 + 0 + 1 = 13_{10}$$

**Hexadecimalsystemet:** Tallet $2A3_{16}$ kan skrives som:

$$2 \cdot 16^2 + 10 \cdot 16^1 + 3 \cdot 16^0 = 512 + 160 + 3 = 675_{10}$$

## 3. Konvertering fra Binær til Decimal

**Metode:** Brug positionsværdi-udvidelsen

**Eksempel:** Konverter $1011_2$ til decimal

  1. Identificer positionerne fra højre: $2^0, 2^1, 2^2, 2^3$
  2. Multiplicer hvert ciffer med dets positionsværdi:
   $1 \cdot 2^3 + 0 \cdot 2^2 + 1 \cdot 2^1 + 1 \cdot 2^0$
  3. Beregn: $8 + 0 + 2 + 1 = 11_{10}$

**Trinvis fremgangsmåde:**

  1. Skriv positionsværdierne under hvert ciffer (fra højre: $2^0, 2^1, 2^2, \dots$)
  2. Multiplicer hvert ciffer med dets positionsværdi
  3. Læg alle produkter sammen

## 4. Konvertering fra Decimal til Binær

**Metode:** Gentagen division med 2

**Eksempel:** Konverter $13_{10}$ til binær

  1. Divider med 2 og noter resten:
     - $13 \div 2 = 6 \text{ rest } 1$
     - $6 \div 2 = 3 \text{ rest } 0$
     - $3 \div 2 = 1 \text{ rest } 1$
     - $1 \div 2 = 0 \text{ rest } 1$
  2. Læs resterne bagfra: $1101_2$

**Alternativ metode:** Find den største potens af 2

  1. Find den største potens af 2 der er $\le$ tallet
  2. Træk denne potens fra
  3. Gentag indtil der ikke er noget tilbage
  4. Marker positionerne for de anvendte potenser med 1, resten med 0

**Eksempel:** $49_{10}$ til binær

  - $49 \ge 32 = 2^5$ ✓ $\rightarrow 49 - 32 = 17$
  - $17 \ge 16 = 2^4$ ✓ $\rightarrow 17 - 16 = 1$
  - $1 < 8 = 2^3$ ✗
  - $1 < 4 = 2^2$ ✗
  - $1 < 2 = 2^1$ ✗
  - $1 \ge 1 = 2^0$ ✓ $\rightarrow 1 - 1 = 0$

Resultat: $110001_2$ (positioner: $2^5, 2^4, 2^0$)

## 5. Konvertering mellem Hexadecimal og Decimal

**Fra Hexadecimal til Decimal:**

Brug positionsværdi-udvidelsen med grundtal 16

**Eksempel:** $2F_{16}$ til decimal

$$2 \cdot 16^1 + 15 \cdot 16^0 = 32 + 15 = 47_{10}$$

**Fra Decimal til Hexadecimal:**

Gentagen division med 16

**Eksempel:** $255_{10}$ til hexadecimal

  - $255 \div 16 = 15 \text{ rest } 15 \text{ (F)}$
  - $15 \div 16 = 0 \text{ rest } 15 \text{ (F)}$

Resultat: $FF_{16}$

## 6. Konvertering mellem Binær og Hexadecimal

**Nøgleprincip:** 4 binære cifre = 1 hexadecimalt ciffer

**Konverteringstabel:**

| Binær | Hex | Decimal |
|-------|-----|---------|
| 0000  | 0   | 0       |
| 0001  | 1   | 1       |
| 0010  | 2   | 2       |
| 0011  | 3   | 3       |
| 0100  | 4   | 4       |
| 0101  | 5   | 5       |
| 0110  | 6   | 6       |
| 0111  | 7   | 7       |
| 1000  | 8   | 8       |
| 1001  | 9   | 9       |
| 1010  | A   | 10      |
| 1011  | B   | 11      |
| 1100  | C   | 12      |
| 1101  | D   | 13      |
| 1110  | E   | 14      |
| 1111  | F   | 15      |

**Fra Binær til Hexadecimal:**

  1. Gruppér binære cifre i grupper af 4 (fra højre)
  2. Tilføj foranstillede nuller hvis nødvendigt
  3. Konverter hver gruppe til det tilsvarende hexadecimale ciffer

**Eksempel:** $11010111_2$ til hexadecimal

  - Gruppér: $1101|0111$
  - Konverter: $1101_2 = D_{16}$, $0111_2 = 7_{16}$
  - Resultat: $D7_{16}$

**Fra Hexadecimal til Binær:**

  1. Konverter hvert hexadecimalt ciffer til 4 binære cifre
  2. Sammensæt resultaterne

**Eksempel:** $A3_{16}$ til binær

  - $A_{16} = 1010_2$
  - $3_{16} = 0011_2$
  - Resultat: $10100011_2$

## 7. Binær Addition

Binær addition følger simple regler:

  - $0 + 0 = 0$
  - $0 + 1 = 1$
  - $1 + 0 = 1$
  - $1 + 1 = 10_2$ (0 med transport af 1)

**Eksempel:** $1011_2 + 1101_2$

$$
\begin{array}{rr}
  & 1011 \\
+ & 1101 \\
\hline
& 11000 \\
\end{array}
$$

Trinvis:

  1. $1 + 1 = 10_2 \rightarrow \text{skriv 0, transport 1}$
  2. $1 + 0 + (\text{transport}) 1 = 10_2 \rightarrow \text{skriv 0, transport 1}$
  3. $0 + 1 + (\text{transport}) 1 = 10_2 \rightarrow \text{skriv 0, transport 1}$
  4. $1 + 1 + (\text{transport}) 1 = 11_2 \rightarrow \text{skriv 11}$

## 8. Binær Multiplikation

Binær multiplikation følger reglerne:
  
  - $0 \times 0 = 0$
  - $0 \times 1 = 0$
  - $1 \times 0 = 0$
  - $1 \times 1 = 1$

**Eksempel:** $101_2 \times 11_2$

$$
\begin{array}{r}
101 \\
\times \quad 11 \\
\hline
101 \\
1010 \\
\hline
1111 \\
\end{array}
$$

## 9. Praktiske Tips

**Hurtige konverteringer:**

- **Potenser af 2:** $2^0=1, 2^1=2, 2^2=4, 2^3=8, 2^4=16, 2^5=32, 2^6=64, 2^7=128, 2^8=256$

- **Hexadecimal bogstaver:** Husk $A=10, B=11, C=12, D=13, E=14, F=15$

**Fejlkontrol:**

  - Tjek altid om dit resultat giver mening i størrelsesorden
  - Ved konvertering til binær: er antallet af cifre rimeligt?
  - Ved hexadecimal: er cifrene gyldige (0-9, A-F)?

## 10. Anvendelse i Programmering

**Hvorfor er dette vigtigt for softwareudvikling?**

  - **Binær:** Computere arbejder internt med binære tal
  - **Hexadecimal:** Bruges til at repræsentere binære data kompakt (f.eks. farver: `#FF0000`)
  - **Bit-operationer:** Manipulation af individuelle bits i programmering
  - **Hukommelsesadresser:** Ofte vist i hexadecimal
  - **Debugging:** Forståelse af hvordan data gemmes og manipuleres

## Opsummering

I denne tutorial har du lært de grundlæggende principper for talsystemer og konvertering mellem dem. Husk følgende nøglepunkter:

  1. **Positionsværdi** er fundamentet for alle talsystemer
  2. **Gentagen division** er den sikre metode til konvertering fra decimal
  3. **4 binære cifre = 1 hexadecimalt ciffer** - denne sammenhæng er guld værd
  4. **Øv dig** i at genkende almindelige mønstre og potenser af 2

Disse færdigheder er essentielle for forståelse af hvordan computere behandler data og vil hjælpe dig gennem hele din uddannelse som softwareingeniør.

## Almindelige Faldgruber

  *   **Positionsrækkefølge:** Husk at potenserne starter fra højre med potens 0
  *   **Hexadecimale bogstaver:** A-F repræsenterer 10-15, ikke 1-6
  *   **Foranstillede nuller:** Ved binær til hex gruppering, tilføj nuller til venstre om nødvendigt
  *   **Transport ved addition:** Glem ikke at overføre 1 til næste position ved $1+1$
  *   **Ciffer-validering:** Sørg for kun at bruge gyldige cifre for det pågældende talsystem