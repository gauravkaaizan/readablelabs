# CLAUDE.md — Readable Labs Website

Rules and conventions for AI assistants working on this project.

---

## Writing Style

### No Em Dashes
Never use em dashes in any visible website copy. This includes:
- The `—` character (U+2014)
- The `&mdash;` HTML entity
- The `&#8212;` HTML entity

Em dashes make copy feel AI-generated. Replace them with a period, a comma, a colon, or rewrite the sentence so the dash isn't needed.

**Wrong:**
> AI fills gaps with assumptions — often wrong ones.

**Right:**
> AI fills gaps with assumptions. Often wrong ones.

**Wrong:**
> Not just what's wrong — why AI misreads your content.

**Right:**
> Not just what's wrong. I dig into why AI misreads your content.

---

### Humanize All Copy
Website text should sound like a real person wrote it, not an AI. Avoid patterns that signal AI-generated content:

- No em dashes (see above)
- No overly symmetrical sentence structures ("Not only X, but also Y")
- No generic filler phrases ("comprehensive", "robust", "seamlessly", "leverage", "utilize")
- Prefer short, direct sentences over long compound ones
- It's fine to start sentences with "And", "But", or "So"
- Contractions are good (don't, it's, you're, I've)
- Write in first person where Yugashree is speaking

---

## Technical Conventions

- All HTML, CSS, and JS live in a single `index.html` file — no separate files
- No external JS libraries; use vanilla JS only
- Google Fonts is the only external dependency allowed
- Use `&#8209;` (non-breaking hyphen) in "E-commerce" headings to prevent mid-word line breaks
- All CTA buttons link to: `https://calendly.com/yugashree107/ai-content-clarity-discovery-call`
- LinkedIn link: `https://www.linkedin.com/in/yugashree-kotkar/`
- Domain: `readablelabs.io`

---

## Brand

- Company: Readable Labs
- Founder: Yugashree Kotkar
- Location: Seattle, WA
- Service: AI Content Clarity Audits for e-commerce brands
- AI systems referenced: ChatGPT, Claude, Gemini (not Perplexity)
- SKU threshold: 10+ SKUs for good fit, fewer than 10 is not a fit

## Colors

| Name | Hex |
|------|-----|
| Navy | `#1E2D3D` |
| Blue | `#2D7DD2` |
| Green (CTA) | `#27AE60` |
| Background | `#F7F6F2` |
| Text | `#4A5568` |
| White | `#FFFFFF` |
