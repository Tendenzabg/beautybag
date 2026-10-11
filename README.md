# BeautyBag Bulgaria — tema Shopify (beautybag.bg)

Tema **Horizon** personalizzato: palette "Premium Botanical & French Luxury", titoli Prata, testo Inter.

## Struttura
- `assets/ blocks/ config/ layout/ locales/ sections/ snippets/ templates/` → file del tema (radice del repo, così Shopify lo collega direttamente)
- `docs/` → design system, catalogo, logistica, strategia
- `brand/` → logo
- `CHANGELOG.md` → storico delle versioni

## Versioni
Ogni modifica = un commit + una versione (tag `vX.Y`) e una voce nel `CHANGELOG.md`.
Per tornare a una versione precedente: `git checkout vX.Y` oppure ripubblicare il tema da quel tag.

## Collegare il tema a Shopify
Shopify admin → Negozio online → Temi → Aggiungi tema → **Connetti da GitHub** → repo `Tendenzabg/beautybag`, ramo `main`.
Da quel momento ogni push su `main` aggiorna il tema collegato.
