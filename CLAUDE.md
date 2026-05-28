# Mr C — maniflair

## Project Overview

Single-page marketing/e-commerce landing page for **Mr C** (brand: `manity_flair`), a men's clothing education brand based in India. The brand philosophy centers on teaching men to understand fabric, construction, and garment provenance rather than buying on price or trend.

**Tagline:** "Dress Better. Buy Better."  
**Instagram:** [@manity_flair](https://instagram.com/manity_flair)  
**Copyright:** © 2026 Mr C — manity_flair

---

## Tech Stack

- **Pure HTML/CSS/JS** — no framework, no build tool, no dependencies
- Single file: `index.html`
- Google Fonts: `Cormorant Garamond` (serif) + `Jost` (sans-serif)
- Scroll reveal via native `IntersectionObserver`

---

## Design System

### Color Palette (CSS custom properties)

| Variable       | Value              | Usage                        |
|----------------|--------------------|------------------------------|
| `--cream`      | `#f5f0e8`          | Page background              |
| `--parchment`  | `#ede8df`          | Alternate section background |
| `--ink`        | `#1a1714`          | Primary text / dark bg       |
| `--ink-soft`   | `#3d3830`          | Secondary text               |
| `--warm-mid`   | `#8c7b6b`          | Muted/label text             |
| `--accent`     | `#6b3a2a`          | Brand red-brown accent       |
| `--gold`       | `#b89c6e`          | Decorative gold              |
| `--border`     | `rgba(26,23,20,0.12)` | Subtle borders            |

### Typography

- **Serif** (`--ff-serif`): Cormorant Garamond — headings, prices, quotes, large display text
- **Sans** (`--ff-sans`): Jost — body, nav links, buttons, labels
- Body: 15px / weight 300 / line-height 1.7

### Spacing Convention

- Desktop sections use `padding: 6–7rem 8rem`
- Mobile breakpoint: `max-width: 900px`, padding collapses to `1.5rem`

---

## Page Structure

| Section        | ID/Class        | Description                                              |
|----------------|-----------------|----------------------------------------------------------|
| Nav            | `nav`           | Fixed top bar — logo, links (Products/Journal/About), Instagram link |
| Hero           | `.hero`         | Two-column grid: copy left, campaign image placeholder right |
| Manifesto      | `.manifesto`    | Brand belief statement — "read selvage edges, inspect welt construction" |
| Pillars        | `.pillars`      | 3-column grid: Material Truth / Construction Over Trend / Informed Choice |
| Products       | `#products`     | 3-column product grid — "The Edit"                       |
| Quote          | `.quote-section`| Centred pull quote                                       |
| Reels/Journal  | `#reels`        | 4-column reel card grid linking to Instagram             |
| Footer         | `footer#about`  | 3-column: brand tagline / navigation / social links      |

---

## Current Products (Placeholders)

All product images are placeholders (no real images yet).

| Product                     | Material                        | Price   |
|-----------------------------|---------------------------------|---------|
| Burgundy Selvedge Bomber    | 14oz Japanese Denim · Sizes 44–60 | ₹8,500 |
| Chore Coat in Moleskin      | French Cotton Moleskin · Natural | ₹6,200  |
| Oxford Weave Shirt          | 120/2 Egyptian Cotton · RTW     | ₹3,800  |

---

## Journal Reels (Placeholder content)

Four reel cards, all linking to Instagram:

1. **Construction** — Real vs Fake Leather — How to Know in 30 Seconds
2. **History** — Japanese Selvedge Denim — Why It Survived the Machine Age
3. **Shoes** — Goodyear Welt vs Cemented Sole — The Construction That Changes Everything
4. **Fabric** — The Burgundy Jacket — A Story That Began With a Childhood Tree

---

## Animations

- Hero elements: staggered `fadeUp` keyframe (0.2s–0.8s delay)
- Scroll sections: `.reveal` class toggled to `.reveal.visible` via `IntersectionObserver` at `threshold: 0.12`
- Hover: product cards lift (`translateY(-4px)`), reel cards scale (`1.02`), overlays fade in

---

## Known Gaps / TODOs

- All product and campaign images are placeholders (`.hero-img-icon` with "M" monogram)
- No real links — "View all pieces", Size Guide, Enquiries all point to `#`
- No cart / checkout functionality
- No backend or CMS
- Mobile nav links hidden (`display: none`) — no hamburger menu implemented
