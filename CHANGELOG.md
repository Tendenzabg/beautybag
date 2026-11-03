# Changelog

## v1.36 — 2026-11-04
- Footer ripristinato: `sections/footer-group.json` non veniva caricato da Shopify (FILE_VALIDATION_ERROR: `pixel_height` del logo = 44 non è un multiplo dello step 8). Impostato 48 → il file viene accettato e il footer torna visibile.
- Theme Check non disponibile: nessun controllo automatico eseguito.

## v1.31 — 2026-11-03
- Footer Soft Violet (v1.29) applicato sopra il tema live salvato (v1.30): conservate le modifiche manuali dell'editor (blocchi app, collezione).
- Social del footer (blocco `social`): Facebook «Beauty Bag Парфюми», Instagram @beautybag.bg, TikTok @beautybag.bg — gli URL reali impostati a mano sul footer live. YouTube e X restano vuoti (nel live erano solo link generici).
- Theme Check non disponibile: nessun controllo automatico eseguito.

## v1.30 — 2026-11-03
- Salvataggio del tema LIVE (MAIN) «beautybag/claude/theme-v-cart-no-persist» con le modifiche fatte a mano nell'editor tra il 31/10 e il 3/11 (ultimo commit Shopify bc0462e).
- `config/settings_data.json`: blocchi app attivi nel tema — Google & YouTube (widget in basso a sinistra), Forms, Microsoft Clarity — e Pigeon Express «shipping-widget-script» (presente ma disattivato).
- `templates/collection.json`: modifiche alla pagina collezione fatte nell'editor. `sections/footer-group.json`: piccoli ritocchi manuali al footer.
- Questo snapshot parte dalla linea del tema live (v1.24 + cart no-persist): NON include il lavoro v1.25–v1.29 (footer Soft Violet, branch `claude/theme-v1.29`), che resta separato.
- Theme Check non disponibile: nessun controllo automatico eseguito.

## v1.29 — 2026-10-31
- Nuovo footer in stile Soft Violet: fondo lilla (color2), 5 blocchi (brand con logo/slogan/contatti, menu «Магазин», menu «Помощ», «Доставка и плащане», bollettino a tutta larghezza) + barra inferiore con copyright, policy e icone di pagamento. Menu Shopify creati: `footer-shop`, `footer-help`. Social rimossi finché non ci sono gli URL reali.

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

## v1.32 — Traduzione EN del tema (su base v1.31)
- Nuovo snippet `snippets/bb-tr.liquid`: dizionario BG→EN (note olfattive, genere, tipo) usato solo con locale `en`.
- Filtri collezione (`list-filter`, `filter-remove-buttons`) tradotti.
- `templates/product.json`: etichette note, disclaimer marchi e pulsante scheda tecnica in EN.
- Theme Check non disponibile: non eseguito.

## v1.33 — Traduzione EN completa (su v1.32)
- `list-filter.liquid`: etichette valori filtro tradotte anche nel checkbox e nel riepilogo filtro attivo.
- `templates/product.json`: blocco «Формат» (ml/refill) e testo intro (concentrazione, volume, benefici) in EN.
- Traduzioni contenuti tema (home, FAQ, annunci, trust, accordion) registrate in Shopify per il tema live (50 chiavi, translationsRegister).
- Theme Check non disponibile: non eseguito.

## v1.34 — Bandierine BG/UK nel selettore lingua (su v1.33)
- Ripristinati da v1.26: `snippets/language-flags.liquid`, `snippets/language-flag-icon.liquid`, componente `LanguageFlagsComponent` in `assets/localization.js`, impostazione `language_selector_style` (default «flags») in `sections/header.liquid`, menu mobile in `snippets/header-drawer.liquid`, voci in `locales/en.default.schema.json`.
- Theme Check non disponibile: non eseguito.

## v1.35 — Bandierine attive di default (condizione `!= dropdown`, impostazione assente nel JSON del gruppo header). Theme Check non disponibile.
