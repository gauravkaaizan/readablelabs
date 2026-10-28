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

- Each page is a single self-contained HTML file (inline CSS/JS): `index.html` (home), `ecommerce/index.html` (original e-commerce audit page), `thanks/index.html` (form thank-you, noindex)
- No external JS libraries; use vanilla JS only
- Google Fonts is the only external dependency allowed
- Use `&#8209;` (non-breaking hyphen) in "E-commerce" headings to prevent mid-word line breaks
- Primary CTA: the free growth check form (`#check`, Netlify Forms, name `growth-check`). Secondary CTA (book a call): `https://calendly.com/yugashree107/ai-content-clarity-discovery-call`
- SEO files: `sitemap.xml`, `robots.txt`, `og-image.png`, LocalBusiness/ProfessionalService JSON-LD in the home page head, Google Search Console verification meta tag (do not remove)
- LinkedIn link: `https://www.linkedin.com/in/yugashree-kotkar/`
- Domain: `readablelabs.io`

---

## Brand

- Company: Readable Labs
- Founder: Yugashree Kotkar
- Location: Redmond, WA
- Service (since 2026-10-27): growth for small businesses and makers (Google, Instagram, Facebook, WhatsApp, website, reviews). Entry offer: free growth check (3 fixes in 24 hours). The original AI Content Clarity Audit lives at /ecommerce/
- AI systems referenced: ChatGPT, Claude, Gemini (not Perplexity)
- SKU threshold (e-commerce audit page only): 10+ SKUs

## Colors

| Name | Hex |
|------|-----|
| Navy | `#1E2D3D` |
| Blue | `#2D7DD2` |
| Green (CTA) | `#27AE60` |
| Background | `#F7F6F2` |
| Text | `#4A5568` |
| White | `#FFFFFF` |

---

## Deploying

Netlify site `readablelabs` (id `a863ca50-c19b-478f-bb4e-d24cfc0eb0b3`) on the Kaaizan Netlify account. Form detection is ON; new form submissions email yugashree107@gmail.com.

```bash
netlify deploy --site a863ca50-c19b-478f-bb4e-d24cfc0eb0b3 --dir . --prod
```

Never deploy without showing Yugashree a preview and getting an explicit go.
