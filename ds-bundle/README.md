# loeuf — design system (conventions)

A calm, editorial fashion system for **loeuf.pk**. Build on-brand by using these exact tokens and classes — do not invent new color names, fonts, or class vocabulary.

## Setup
Every design imports **`styles.css`** (tokens + fonts + base + component classes). Page background is **Mist `#EAEAEA`**; content sits on **White `#FFFFFF`** cards. Load the fonts (Google Fonts) — **Fraunces** (display serif) and **Montserrat** (the free stand-in for the licensed **Gotham**, which is the real brand sans).

## Styling idiom — CSS custom properties + `ds-` utility classes
Style with the `var(--*)` tokens from `styles.css`. Never hard-code hex values.

| Token | Value | Use |
|---|---|---|
| `--bg-page` / `--c-mist` | `#EAEAEA` | page background |
| `--bg-surface` / `--c-white` | `#FFFFFF` | cards, panels, inputs |
| `--c-noir` | `#161616` | primary text, inverse surfaces |
| `--c-graphite` | `#555555` | secondary text |
| `--c-rose` | `#C97F75` | **the accent** — badges, sale, CTAs (sparing, ~2%) |
| `--c-rose-deep` | `#B0685E` | accent hover |
| `--c-almond` | `#E7DECF` | warm tint surface |
| `--font-display` | Fraunces | headings, product names, italic accents |
| `--font-sans` | Gotham → Montserrat | body, nav, labels, buttons |
| `--space-1…9` | 4 → 96px | 4px-base spacing |
| `--radius-none/sm/md/pill` | 0/2/4/999px | near-sharp corners |
| `--egg` | `50% 50% 50% 50% / 62% 62% 38% 38%` | the œuf oval — photo crops, frames, the wordmark “o” |

Component classes (see `styles.css`): `.ds-wordmark` (egg-dot mark), `.ds-btn` (+ `--ghost` `--accent` `--link`), `.ds-badge` (+ `--noir` `--soft` `--out` `--stock`), `.ds-input`, `.ds-card`, `.ds-egg` (oval crop), `.ds-eyebrow`, `.ds-display`.

## Idiomatic snippet
```html
<div class="ds-card" style="padding:var(--space-6); background:var(--bg-surface)">
  <span class="ds-badge">New in</span>
  <h3 style="font-family:var(--font-display); margin:var(--space-3) 0">Camila</h3>
  <div class="ds-egg" style="aspect-ratio:4/5; background:var(--c-mist)"></div>
  <button class="ds-btn ds-btn--accent" style="margin-top:var(--space-4)">Add to cart</button>
</div>
```

## Where the truth lives
`styles.css` (tokens + classes) is authoritative. Each component’s preview card is in `components/<Group>/<Name>/<Name>.html`. Voice: warm, short, sensory — *"Crafted for the way you move."* Never more than one accent per view.
