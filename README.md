# ArugaLife Design System

The shared brand + UI foundation for **ArugaLife** and its flagship product **Evera**.
Link one stylesheet (`styles.css`), use the tokens and components, and follow the voice
and visual rules below.

## One company, two voices

This system has two surfaces. Pick the right one for the job.

| | **ArugaLife** (master brand) | **Evera** (product) |
|---|---|---|
| **Used for** | Marketing site, brand moments, outreach | The logged-in PRA senior-benefits app |
| **Feeling** | Warm, empathetic, Filipino warmth open to the world | Institutional, trustworthy, clear |
| **Palette** | Sage green · cream · terracotta · gold | Navy · orange · neutral grays |
| **Type** | Plus Jakarta Sans + Caveat (handwritten accent) | Source Sans 3 + Libre Baskerville |
| **Icons** | Brand SVGs (`assets/`) | Lucide (CDN) |

Evera is a retirement benefits plan offered in partnership with the
**Philippine Retirement Authority (PRA)**.

## Who we serve

ArugaLife is Filipino at heart but not Filipino-only. Our community spans
local families and a fast-growing base of members from around the world —
including retirees from the **United States, China, Japan, Korea, and India**
who choose the Philippines for their next chapter (a natural fit with PRA's
SRRV program). Keep the copy welcoming and global: lead with *aruga* (Filipino
care) as the **differentiator**, never as a barrier to entry. Prefer "everyone,"
"every family," "here and around the world" over "every Filipino."

## Quick start

Link the single entry stylesheet — it `@import`s every token and font:

```html
<link rel="stylesheet" href="styles.css">
```

Then use the CSS variables and React components. Prefer the **semantic aliases**
(`--surface-page`, `--text-heading`, `--action-primary`, …) over raw palette tokens
so UI tracks the right brand automatically.

## Visual foundations

### Color

**ArugaLife brand** — `--al-cream` `#F7F3E9` (page), `--al-cream-deep` `#EFE7D3` (alt),
`--al-sage` `#DDE7D3` and `--al-sage-mid` `#A9C29D` (surfaces/borders),
`--al-green` `#5E8062` and `--al-green-deep` `#2E4636` (brand + headings),
`--al-terra` `#D26B3C` (primary action), `--al-gold` `#E8A53C` (highlight/numerals),
`--al-ink` `#2B3A30` (body), `--al-muted` `#5D6B5E` (secondary).

**Evera product** — `--ev-navy` `#0A2540` (surface), `--ev-orange` `#E8730A` (action),
`--ev-green` `#1A7A4A` (success), `--ev-red` `#C0392B` (error), plus a gray scale
(`--gray-50` … `--gray-700`).

Reach for the semantic aliases at the bottom of `tokens/colors.css` in real UI.

### Type

- **ArugaLife:** `--font-display` (Plus Jakarta Sans) for UI and headings, with
  `--font-hand` (Caveat) as a sparing handwritten accent.
- **Evera:** `--font-ui` (Source Sans 3) for UI, `--font-serif` (Libre Baskerville)
  for formal headings.
- Fluid display scale: `--fs-hero`, `--fs-h1`–`--fs-h3`, `--fs-lead`, `--fs-body`,
  `--fs-sm`, `--fs-xs`. Weights `--fw-regular` (400) … `--fw-black` (800).

### Spacing, radii & shadows

In `tokens/spacing.css` — use these tokens rather than magic numbers.

## Components

React primitives in `components/` (namespace `window.ArugaLifeDesignSystem_233caa`):

- **Core** — `Button`, `Badge`, `Card`, `Avatar`, `Eyebrow`
- **Forms** — `Input`, `Select`

Each has a `.d.ts` (API), a `.jsx` (source), and a `.prompt.md` (usage notes).

## Assets

In `assets/`: `logo-mark.svg`, `logo-lockup.svg`, `logo-lockup-dark.svg`, the brand
value icons (`icon-malasakit`, `icon-bayanihan`, `icon-gabay`, `icon-tapat`), and
`sampaguita-flower.jpg`. Copy what you need into your own files — don't hot-link.

## Templates

Ready-to-copy starting points live in `templates/`:

- **ArugaLife Landing** (`templates/arugalife-landing`) — the marketing landing page.

The reference recreations in `ui_kits/` (`arugalife-web`, `evera-app`) show the system
in full context.

## Repository layout

| Path | What it is |
|------|------------|
| `styles.css` | Single entry stylesheet — `@import`s all tokens + fonts |
| `tokens/` | Colors, typography, spacing/radii/shadows, fonts |
| `components/` | React primitives (core + forms) |
| `assets/` | Logos and brand SVG icons |
| `templates/` | Copy-ready starting points |
| `ui_kits/` | Full-context recreations (ArugaLife web, Evera app) |
| `foundations/` | Visual specimen cards |
| `export/` | Built, self-contained marketing site (`index.html`) for deploy |

## Building with the system

- **Visual artifacts** (slides, mocks, prototypes): copy assets out, link `styles.css`
  for tokens, reuse the SVGs in `assets/`, and follow the voice + visual rules above.
- **Evera app work:** Lucide icons + the navy/orange theme.
- **ArugaLife brand work:** the warm sage/cream/terracotta palette + the brand SVGs.
- Respect `prefers-reduced-motion` — disable decorative animation when it's set.
