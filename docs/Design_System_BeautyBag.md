# Design System BeautyBag — "Premium Botanical & French Luxury" (ottobre 2026)

Sostituisce la palette precedente (Midnight Charcoal / Champagne Gold / Pearl White / Deep Charcoal).

## Palette (regola 60/30/10)
| Ruolo | Colore | HEX | Uso |
|---|---|---|---|
| 60% dominante | Bianco latte / avorio | #FAF7F0 | sfondi sito, schede prodotto, spazi vuoti (token `background`) |
| 30% secondario | Grigio tortora / lino caldo | #5E554C | testi, menu, sottotitoli (token `foreground`) |
| Neutro di supporto | Lino chiaro | #E8E0D0 | bordi, divisori, sfondo hero e card (token `color2`) |
| Accento 1 | Oro champagne opaco | #BFA06A | icone certificazione, etichette "Novità", dettagli di brand (hardcoded, solo accenti) |
| Accento 2 / CTA | Verde salvia scuro | #55634A | pulsanti "Aggiungi al carrello", CTA, sezioni in evidenza (token `color1`) |

Testo su verde salvia: avorio (#FAF7F0). Non usare più nero #111111 né oro #D4AF37.

## Font (ottobre 2026)
- **Titoli (H1–H4):** Prata (serif elegante, supporta il cirillico → bulgaro corretto). Handle tema: `prata_n4`. Alternativa scelta dall'utente: Cinzel (tutto maiuscolo) — NON adatta ai testi bulgari perché senza cirillico (fallback).
- **Testo, sottotitoli (H5–H6) e pulsanti:** Inter (alternativa: Open Sans). Handle: `inter_n4` corpo, `inter_n5` sottotitoli, `inter_n7` accent.
- Dimensioni titoli nel tema: H1 44, H2 36, H3 28, H4 24; paragrafo 14.
- Playfair Display / Cormorant Garamond non più usati.

### Regole d'oro font (BG + EN)
1. Ogni font scelto deve avere i set "Latin" **e** "Cyrillic".
2. Il bulgaro ha parole più lunghe (es. "Купи сега" vs "Buy now"): i pulsanti verde salvia devono mantenere padding interno sufficiente, senza rompere il layout; testare i testi bulgari più lunghi.
3. Gerarchia: font titoli (Prata) per nomi dei profumi, titoli dei blocchi in homepage e grandi promozioni; font corpo (Inter) per prezzi, menu di navigazione e recensioni clienti.

### Applicazione nel tema (copia "Horizon - BeautyBag Botanical Fonts")
- Nome prodotto (scheda e card) = preset h4/h3 (Prata); titoli sezioni home = h1–h3 (Prata).
- Prezzi = preset h6 nelle card, h5 nella scheda prodotto (Inter). Menu, azioni header e selettore paese/lingua = `body` (Inter). Annunci = subheading (Inter).
- Titoli trust ("100% Made in Italy" ecc.) e accordion = h5/h6 (Inter).

## Tema Shopify (Horizon)
- `config/settings_data.json` → `color_palette`: background #FAF7F0, foreground #5E554C, color1 #55634A, color2 #E8E0D0. Pulsanti primari e variante selezionata usano `color1`. `type_heading_font` = prata_n4.
- Nei template (`index.json`, `product.json`) usare i token `{{ settings.color_palette.* }}`; hardcoded solo l'oro #BFA06A per le icone.

## Regole operative
- Il tema pubblicato NON è modificabile via API: duplicare il tema, modificare la copia, far pubblicare all'utente (non pubblicare prima del via).
- Foto prodotto: accostare i flaconi a elementi reali (foglie di salvia, alambicco, texture di latte).
