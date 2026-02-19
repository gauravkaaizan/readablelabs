# Readable Labs — Marketing Website

Single-page marketing website for **Readable Labs**, an AI Content Clarity Auditing service for e-commerce brands.

**Live domain:** readablelabs.io
**Location:** Seattle, WA
**Calendly:** https://calendly.com/yugashree107/ai-content-clarity-discovery-call
**LinkedIn:** https://www.linkedin.com/in/yugashree-kotkar/

---

## Project Structure

```
readablelabs/
├── index.html    # Single file — all HTML, CSS, and JS inline
├── README.md     # This file
└── CLAUDE.md     # AI assistant rules for this project
```

## Running Locally

No build step required. Open directly in a browser:

```bash
open index.html
```

Or serve with any static file server:

```bash
# Python
python3 -m http.server 8080

# Node (npx)
npx serve .
```

Then visit `http://localhost:8080`.

---

## Sections

| # | Section | Notes |
|---|---------|-------|
| 1 | Nav | Sticky, blur backdrop, green CTA |
| 2 | Hero | Left-aligned, scroll-animated, pulsing dot eyebrow |
| 3 | Problem | Two-column: copy left, issue card panel right |
| 4 | Solution | 6-card grid (3-col) + meta row |
| 5 | How It Works | 2x2 step cards + italic callout note |
| 6 | About | Two-column sidebar layout, sticky sidebar |
| 7 | Who It's For | Fit / not-fit card comparison |
| 8 | Final CTA | Navy bg, large green button |
| 9 | Footer | Dark navy, email + LinkedIn + CTA, copyright |

---

## Design System

| Token | Value |
|-------|-------|
| Navy | `#1E2D3D` |
| Blue | `#2D7DD2` |
| Green (CTA) | `#27AE60` |
| Background | `#F7F6F2` |
| Text | `#4A5568` |
| White | `#FFFFFF` |

**Fonts:** DM Serif Display (headings) + DM Sans (body) via Google Fonts
**Breakpoints:** 900px (about section stacks), 768px (all grids collapse to single column)

---

## Tech Notes

- Zero external dependencies beyond Google Fonts
- Scroll animations via `IntersectionObserver` (no library)
- Sticky nav with `backdrop-filter: blur()`
- Staggered card animations using JS-applied `transition-delay`
- Non-breaking hyphen (`&#8209;`) used in "E-commerce" headings to prevent mid-word line breaks
- All CTAs link to Calendly

---

## Content Rules

See `CLAUDE.md` for full guidelines. Key rule: **no em dashes anywhere in visible copy.**

---

© 2025 Readable Labs. All Rights Reserved.
