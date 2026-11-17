# Polaris – Policy-minded professionals

Sito statico di Polaris, pubblicato con GitHub Pages su **https://polarisprofessionals.it**.

Nessuna dipendenza né build: è HTML e CSS puro. Modifichi un file, fai commit su `main` e il sito si aggiorna in un paio di minuti.

## Struttura

```
index.html            la pagina del sito
brand/index.html      guida all'identità visiva (palette, caratteri, art direction)
assets/css/style.css  tutti gli stili; i colori sono variabili in cima al file
assets/img/           logo e stella
assets/membri/        foto dei membri (vedi sotto)
favicon.svg
CNAME                 dominio personalizzato per GitHub Pages
```

## Foto dei membri

Finché manca la foto, il sito mostra le iniziali. Per aggiungerla basta caricare un file con il nome esatto in `assets/membri/`:

| Membro | File |
|---|---|
| Francesco Armillei | `armillei-francesco.jpg` |
| Elia Bidut | `bidut-elia.jpg` |
| Lorenzo Borga | `borga-lorenzo.jpg` |
| Claudio Buongiorno Sottoriva | `buongiorno-sottoriva-claudio.jpg` |
| Andrea Cerrato | `cerrato-andrea.jpg` |
| Maddalena Conte | `conte-maddalena.jpg` |
| Francesco Filippucci | `filippucci-francesco.jpg` |
| Matteo Gallone | `gallone-matteo.jpg` |
| Giulia Gitti | `gitti-giulia.jpg` |
| Andrea Gorga | `gorga-andrea.jpg` |
| Nicola Lipari | `lipari-nicola.jpg` |
| Francesco Olivanti | `olivanti-francesco.jpg` |
| Marco Palladino | `palladino-marco.jpg` |
| Lorenzo Ruffino | `ruffino-lorenzo.jpg` |
| Matteo Sartori | `sartori-matteo.jpg` |
| Andrea Silvagni | `silvagni-andrea.jpg` |
| Alessandro Zhou | `zhou-alessandro.jpg` |

Indicazioni: foto quadrata, almeno 400×400 px, viso centrato, formato `.jpg`. Il colore non conta: il sito le rende tutte monocrome nel tono del marchio (a colori al passaggio del mouse).

## Aggiungere o modificare un membro

In `index.html` ogni membro è un blocco `<li class="membro">`. Copia un blocco, cambia iniziali, nome, affiliazione, bio e nome del file della foto. Per il profilo LinkedIn aggiungi, dopo la bio, un link `<a class="membro-link" href="…">` come quelli già presenti. Aggiorna anche il numero nel titolo della sezione ("17 professionisti").

## Dominio

Il file `CNAME` contiene `www.polarisprofessionals.it` (dominio principale; GitHub reindirizza `polarisprofessionals.it` su www). Nella zona DNS del dominio (Netsons) servono:

| Tipo | Nome | Valore |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | `elbid.github.io.` |

Poi in **Settings → Pages** del repository: sorgente `main` / root, dominio `www.polarisprofessionals.it`, e quando il certificato è pronto spunta **Enforce HTTPS**.
