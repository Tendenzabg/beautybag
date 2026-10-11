# BeautyBag Bulgaria — tema Shopify (beautybag.bg)

Tema **Horizon** personalizzato: palette "Premium Botanical & French Luxury", titoli Prata, testo Inter.

## Struttura
- `assets/ blocks/ config/ layout/ locales/ sections/ snippets/ templates/` → file del tema (radice del repo, così Shopify lo collega direttamente)
- `docs/` → design system, catalogo, logistica, strategia
- `brand/` → logo
- `CHANGELOG.md` → storico delle versioni

## Versioni
- Ramo di lavoro (quello collegato a Shopify): `claude/theme-live`.
- Ogni modifica = un commit su `claude/theme-live` + uno snapshot di versione `claude/theme-vX.Y` + una voce nel `CHANGELOG.md`.
- Per tornare indietro: ricollegare il tema al ramo `claude/theme-vX.Y` desiderato (o fare un nuovo commit che ripristina quei file).

Nota: nelle sessioni Claude si può scrivere solo su rami `claude/*`, per questo non si usano `main` e i tag.

## Collegare il tema a Shopify
Shopify admin → Negozio online → Temi → Aggiungi tema → **Connetti da GitHub** → repo `Tendenzabg/beautybag`, ramo `claude/theme-live`.
Da quel momento ogni push su quel ramo aggiorna il tema collegato.
