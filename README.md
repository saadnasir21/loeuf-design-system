# loeuf — Design System

A brand & UI design system for **[loeuf.pk](https://loeuf.pk/)** ([@loeuf.pk](https://www.instagram.com/loeuf.pk/)) — a contemporary Pakistani fashion label. Minimal, editorial, and warm, anchored on the signature **Mist `#EAEAEA`**.

## Files
| File | Purpose |
|------|---------|
| `index.html` | Visual style guide — open in a browser to see colors, type, components, voice. |
| `instagram.html` | Instagram posting system — feed grid, post/story templates, captions, cadence. |
| `tokens.css` | CSS custom properties — the source of truth for product code. |
| `tokens.json` | Same tokens as JSON for design tools / build pipelines. |

## Foundations at a glance

**Color** — Cool-neutral backbone, one accent.
- **Page background `#EAEAEA` (Mist) + cards `#FFFFFF` (White)** · Noir `#161616` (ink)
- Rose `#C97F75` — dusty-rose accent for **badges, sale & tags**, used sparingly (~2% of any view)
- Yolk `#DDA63A` — optional secondary accent · Almond `#E7DECF` — warm tint
- Rough usage ratio: **90% neutral / 8% ink / 2% accent**

**Type** — Two families.
- **Fraunces** (serif) — display headings, product names, italic accent words
- **Gotham** (geometric sans) — body, nav, eyebrows, buttons, forms. *Licensed font; use **Montserrat** as the free web fallback.*

**System** — 4px spacing grid · near-sharp corners (radius 0–4px) · whisper-soft shadows; borders do the structural work.

**Voice** — Warm, understated, assured. *"Crafted for the way you move."* Short, sensory, never salesy.

## Using the tokens
```html
<link rel="stylesheet" href="tokens.css">
```
```css
body { background: var(--bg-page); }   /* #EAEAEA Mist */
.card { background: var(--bg-surface); } /* #FFFFFF White */

.button {
  background: var(--c-noir);
  color: var(--c-white);
  font-family: var(--font-sans);
  padding: var(--space-3) var(--space-6);
  border-radius: var(--radius-none);
}
```

Fonts:
- **Fraunces** — free, via Google Fonts (ital, 300–600).
- **Gotham** — licensed (Typography.com); self-host the webfont. Use **Montserrat** (Google Fonts, 300–600) as the free fallback.

---
*v1.0 — 2026. A living document; evolve it as the brand grows.*
