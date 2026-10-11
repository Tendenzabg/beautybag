# Changelog

## v1.8 — 2026-10-11
- Scheda prodotto: ripristinata la riga accordion "Олфактивна пирамида" (prima riga) con i metafield Върхови нотки, Сърдечни нотки, Базови нотки (ogni riga appare solo se compilata).

## v1.7 — 2026-10-11
- Nuova palette ispirata a chogangroupspa.com: sfondo #FFFFFF, testo #1D1D1D, viola #6A61A7 (pulsanti/accenti), lilla chiaro #EDEBF5 (riquadri/linee). Badge "esaurito" rosa #F6C6E2.
- Font: Instrument Sans per titoli, sottotitoli e testo (prima Prata + Inter). Dimensioni titoli leggermente ridotte.
- Stile: pulsanti, campi e selettori a pillola; schede prodotto e popup con angoli 16 px; larghezza pagina "wide".
- Icone dei blocchi "Icona" (homepage e scheda prodotto): viola con cerchio lilla dietro, seguono la palette (regola in snippets/icon-or-image.liquid).

## v1.6 — 2026-10-11
- Slideshow hero: nuova impostazione "Immagine mobile" (<750px, formato verticale 4:5) sul blocco slide.
- Homepage: banner mobile 928x1152 (bianco e nero) collegati alle due slide.

## v1.5 — 2026-10-11
- Sfondo del sito bianco (#FFFFFF) con riquadri/linee color #F3EFE8 (variante "Prova A").
- Scheda prodotto: nuova riga accordion "Олфактивна пирамида" (note di testa/cuore/fondo dai metafield), mostrata solo se presenti.
- Rimossa la dicitura "на достъпна цена" dal testo introduttivo della scheda prodotto e dalla homepage.

## v1.4 — 2026-10-11
- Scheda prodotto: selettore "Формат" con i due formati collegati (70 ml ↔ 30 ml, 50 ml ↔ 15 ml ricarica) in base al metafield `other_format`; mostra misura e prezzo, il formato corrente è evidenziato in verde salvia.
- Fix: la dicitura "(зареждане)" nell'intro ora usa correttamente il metafield booleano `is_refill`.

## v1.3 — 2026-10-11
- Scheda prodotto: nascosto il pulsante di acquisto rapido "Купете със Shop" (nuova opzione nel blocco accelerated-checkout, ora disattivata).

## v1.2 — 2026-10-11
- Scheda prodotto: rimosso il sottotitolo "Олфактивно вдъхновение: marca - modello" sotto il prezzo (il disclaimer legale nell'accordion resta).

## v1.1 — 2026-10-11
- Hero: slideshow con 2 immagini (flacone nero con splash dorato, flacone bianco con splash di latte), autoplay 6 s, pulsante in basso a sinistra.
- Titolo H1, sottotitolo e 2 pulsanti spostati nella nuova sezione `intro_bb` sotto l'hero.

## v1.0 — 2026-10-11
- Primo salvataggio del tema "Horizon - BeautyBag Botanical Fonts".
- Palette Premium Botanical & French Luxury (avorio #FAF7F0, tortora #5E554C, lino #E8E0D0, salvia #55634A, oro opaco #BFA06A).
- Font: titoli Prata, testo e pulsanti Inter; prezzi/menu in Inter, nomi profumi in Prata.
- Homepage (annunci, hero, 4 punti di fiducia, 3 collezioni, bestseller, storia, FAQ) e scheda prodotto (sottotitolo da metafield, trust, accordion con disclaimer).
- Logo BeautyBag.
- Aggiunti `docs/` con design system, catalogo, logistica e strategia.
