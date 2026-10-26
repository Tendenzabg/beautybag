# Changelog

## v1.28 — 2026-10-26
- Scheda prodotto: il selettore «Формат» ora mostra anche la ricarica 15 ml nelle schede 70 ml e 30 ml, quando esiste ed è pubblicata (letta dai «Допълващи продукти» del prodotto; i prodotti in bozza non compaiono). Formati ordinati dal più piccolo, il corrente evidenziato. Stessa cosa nel pannello «Купи сега» delle card in collezione (nuovo snippet `product-card-format-pill`, `product-card-formats` riscritto). Fix: dalla scheda 15 ml restano visibili anche 30 e 70 ml (il formato collegato viene seguito su due livelli). Il codice della scheda è passato dal blocco `bb_format` di `templates/product.json` ai nuovi snippet `product-format-selector` e `product-format-selector-button`.

## v1.27 — 2026-10-15
- Lingue: tutte le scritte rimaste in inglese nella versione bulgara ora sono in bulgaro (pagina 404, carrello «Количка», «Може да ви хареса и», «Колекции», pulsante del modulo contatti, «Абонирай се» nel footer, pagina password, «100% Произведено в Италия», «Унисекс и лукс колекция»). I link delle tre collezioni nella home ora puntano agli handle latini.
- Scheda prodotto: i blocchi Liquid con testi fissi (selettore formato, descrizione Extrait de Parfum) ora seguono la lingua (`request.locale`); rimosse "на достъпна цена" e "12+ часа" da questi blocchi.
- In Shopify (non nei file del tema): menu e pagina Contatti in bulgaro; traduzioni inglesi registrate per tema, menu, collezioni, pagine, policy e prodotti attivi.

## v1.26 — 2026-10-15
- Selettore lingua con bandierine (BG, EN; pronte anche IT, DE, RO) nell'header e nel menu mobile. Nuovo snippet `language-flags` (funziona anche senza JavaScript: ogni bandierina invia il modulo di localizzazione). Nuova impostazione header `language_selector_style` (`flags` predefinito, `dropdown` per il vecchio menu a tendina), con chiavi in `locales/en.default.schema.json`.
- Il selettore con le bandierine è un menu a discesa: bottone con la bandierina della lingua attiva che apre l'elenco (bandierina + nome). Nuovo snippet `language-flag-icon`; nuovo componente `language-flags-component` in `assets/localization.js` (chiude il menu con clic fuori e Esc). Nel menu mobile l'elenco si apre dentro il pannello.
- In Shopify: inglese collegato al mercato Bulgaria (`beautybag.bg/en/`). Il selettore compare solo se il negozio ha più di una lingua attiva. I testi di prodotti e collezioni in inglese non sono ancora tradotti (restano in bulgaro).
- Caricato sul tema live spingendo il branch `claude/theme-v1.25` (collegato al tema). Primo invio con i filtri Liquid dentro i parametri del tag `form`: Shopify ha rifiutato lo snippet e per alcuni minuti l'header mostrava un errore Liquid; corretto assegnando prima le variabili. Theme Check non disponibile: verificato sul sito pubblico.

## v1.25 — 2026-10-15
- SEO: `snippets/meta-tags.liquid` — `og:price:amount` ora con punto decimale e due decimali (es. 18.00, prima 18,00) indipendente dalla lingua; `og:image` ora con `https:` (prima `http:`).
- Handle (URL) di collezioni e prodotti traslitterati in latino con reindirizzamenti 301 dai vecchi indirizzi in cirillico (es. `/collections/damski-parfyumi`). La sezione collezione della home ora punta a `bestselari`.
- Testi delle 4 collezioni principali, titolo SEO e meta description della home impostati in Shopify (non fanno parte dei file del tema). Testi alternativi (alt) aggiunti a 5 immagini della home.
- Salvato lo stato del tema live v1.24 con queste modifiche. Theme Check non disponibile: verificato solo sul sito pubblico.

## v1.24 — 2026-10-12
- Corretto un errore della v1.23: l'impostazione `free_shipping_threshold` aveva troppi passi (290 con step 1; Shopify ne accetta max 101), quindi Shopify rifiutava `settings_schema.json` e lo svuotava, scomponendo la home. Ora step 5 (58 passi). Tutti i range del tema verificati.

## v1.23 — 2026-10-12
- Barra «consegna gratuita» nel carrello e nel drawer: mostra quanto manca per superare 70 € (testi bulgari in `locales/bg.json`) e, raggiunta la soglia, il messaggio di conferma. Nuove impostazioni tema (Carrello): `free_shipping_bar_enabled`, `free_shipping_threshold` (70). Nuovo snippet `free-shipping-bar`, richiamato da `cart-products`. La soglia deve coincidere con la tariffa impostata nelle spedizioni di Shopify.

## v1.22 — 2026-10-12
- Pulsanti primari con sfumatura verticale viola-magenta (#924A87 → #6A61A7). Nuove impostazioni tema: `button_gradient_enabled`, `button_gradient_start`, `button_gradient_end`. Pulsanti secondari e «Купи сега» trasparenti invariati; al hover leggermente più scuri.

## v1.21 — 2026-10-12
- Logo mobile ancora più grande: altezza da 38 a 50 px (`logo_height_mobile`).
- Incluse le modifiche fatte nell'editor sul tema v1.20 (home).

## v1.20 — 2026-10-12
- Salvate le modifiche dall'editor sul tema live (v1.18): nuove immagini mobile dell'hero (senza logo), immagine di sfondo "luxury" nella sezione collezione, fondi lilla semitrasparenti sui testi e pulsante con viola semitrasparente. Mantenuto il logo mobile a 38 px.

## v1.19 — 2026-10-12
- Logo più grande su mobile: altezza da 28 a 38 px (`logo_height_mobile`).

## v1.18 — 2026-10-12
- Salvate le modifiche dall'editor sul tema live (v1.17): footer con bollettino in bulgaro e impostazioni complete dei blocchi; home con overlay a gradiente viola/rosa sulle sezioni, immagini di sfondo nelle sezioni collezioni e testi con fondo semitrasparente.

## v1.17 — 2026-10-12
- Etichetta "Изчерпано" (e tutti i badge) quadrata: `badge_corner_radius` da 100 a 0.
- Schede tecniche PDF (BGR) collegate via metafield ai 94 prodotti della collezione Бестселъри (dati, non tema).

## v1.16 — 2026-10-11
- Scheda prodotto: nuovo blocco sotto gli accordion con il pulsante "Изтегли техническата карта (PDF)", mostrato solo se il prodotto ha il metafield `custom.tech_sheet` (file). Primo prodotto con scheda: 002M.

## v1.15 — 2026-10-11
- Salvate le modifiche fatte nell'editor sul tema live: transizioni di pagina attive (anche verso il prodotto principale), carrello laterale che si apre dopo l'aggiunta, acquisto rapido su mobile attivo, collezione "бестселъри" per lo stato vuoto, sfondo pulsante primario #6A61A7DE (leggermente trasparente), testo spedizione nell'accordion prodotto aggiornato (Pigeon al posto dell'automat 24/7).

## v1.14 — 2026-10-11
- Salvata la modifica fatta nell'editor al testo "Правна забележка" nella scheda prodotto (accordion): ora non cita più marca e modello nella frase iniziale.

## v1.13 — 2026-10-11
- Salvate le modifiche fatte nell'editor sul tema live (v1.12): pulsanti hero della home trasparenti con bordo e testo marrone (#6A4A43 / #6B5748), larghezza personalizzata 25% desktop / 50% mobile.

## v1.12 — 2026-10-11
- Pulsanti quadrati senza arrotondamenti: raggio 0 per pulsanti primari, secondari e selettori di variante (anche pillole formato e "Купи сега" nelle card).

## v1.11 — 2026-10-11
- Pulsante "Купи сега" nelle card delle collezioni: ora trasparente con bordo (pieno al passaggio del mouse), sia su desktop sia su mobile.

## v1.10 — 2026-10-11
- Schede prodotto nelle collezioni: su mobile/touch (senza hover) i formati 30/70 ml e "Купи сега" appaiono sotto il prezzo; su desktop resta il pannello al passaggio del mouse (snippet `product-card-formats`, parametro `layout`).

## v1.9 — 2026-10-11
- Pagina collezioni: al passaggio del mouse sulla foto della card compare un pannello con i formati (es. 30 ml / 70 ml, dal metafield `other_format`) e il pulsante "Купи сега" che aggiunge il formato scelto e va direttamente al checkout. Solo su dispositivi con mouse; appare solo se il prodotto (o l'altro formato) è disponibile. Nuovo snippet `product-card-formats`, chiavi locale `content.product_card_*`.

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
