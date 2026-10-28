# MSU1_26 – Matematik for Spiludviklere

Dansk kursusside for MSU1 (2. semester). Siden hedder "Matematik for Spiludviklere" og følger i sessionerne 01–09 samme emner som MSE1 (aritmetik og funktioner, talsystemer, mængdelære, kombinatorik og sandsynlighed, Bayes, beskrivende statistik, lineær algebra, vektorer og matricer, matrixalgebra). Session 10 er lineære transformationer og transformationsmatricer; 11–12 er projektarbejde.

## Struktur

- Sessionsmapperne hedder kun `01` til `12`. Hver har `README.md`, `Forberedelse.md`, `Oevelser.md` og `Tutorials.md`, og alle fire står i nav. En ny session skal have alle fire filer og nav-indgange.
- Figurer ligger i sessionens `src/` samt i `billeder/` og `figures/`.
- Litteratur: kapitler fra MSE-bogen (`MSE_book_v2`), linket via `raw.githubusercontent.com/.../master/main.pdf`. MSE_book_v2's branch hedder `main`; tjek linket, hvis det skal ændres.
- Sprog: dansk (`language: da`, quiz `lang: da`).

## Konfiguration, der afviger fra den globale opsætning

- `site_dir: ../site`, dvs. `C:\GitHub\site`, som deles med ALI1_26 og STA_26. Byg til en anden mappe (`mkdocs build --strict -d <mappe>`), hvis flere sites bygges efter hinanden.
- Ingen `mkdocs-jupyter`.
- Ingen `.gitignore`. Pas på ikke at committe `.venv/`, `.vscode/` eller byggeoutput.
- Den lokale `.venv` er i stykker (dens launcher peger på `OneDrive - ViaUC\Arbejde\GitHub\MSE1_DK_25\.venv`). Byg med den globale `mkdocs`, indtil den er genskabt.
