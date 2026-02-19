# Readable Labs — Marketing Website

Single-page marketing website for **Readable Labs**, an AI Content Clarity Auditing service for e-commerce brands.

**Live site:** https://readablelabs.netlify.app
**Domain:** readablelabs.io
**Location:** Seattle, WA
**Calendly:** https://calendly.com/yugashree107/ai-content-clarity-discovery-call
**LinkedIn:** https://www.linkedin.com/in/yugashree-kotkar/

---

## Project Structure

```
readablelabs/
├── index.html       # Single file — all HTML, CSS, and JS inline
├── yugashree.jpg    # Founder headshot (About section)
├── README.md        # This file
└── CLAUDE.md        # AI assistant rules for this project
```

---

## Running Locally

No build step required. Open directly in a browser:

```bash
open index.html
```

Or serve with any static file server for proper `http://` context:

```bash
# Python
python3 -m http.server 8080

# Node (npx)
npx serve .
```

Then visit `http://localhost:8080`.

---

## Deploying to Netlify

### Option 1 — Drag and Drop (simplest)

1. Go to [app.netlify.com](https://app.netlify.com)
2. Click **Add new site → Deploy manually**
3. Drag the entire `readablelabs/` folder onto the upload area
4. Netlify gives you a live URL instantly

### Option 2 — Netlify CLI

```bash
# Install CLI (if not already installed)
npm install -g netlify-cli

# Log in
netlify login

# Deploy to production from inside this folder
netlify deploy --prod --dir .
```

### Option 3 — Netlify API (no interactive CLI needed)

```bash
# 1. Create the site (once)
curl -X POST "https://api.netlify.com/api/v1/sites" \
  -H "Authorization: Bearer YOUR_NETLIFY_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"name": "readablelabs"}'

# 2. Zip the files
zip -r deploy.zip index.html yugashree.jpg

# 3. Deploy
curl -X POST "https://api.netlify.com/api/v1/sites/YOUR_SITE_ID/deploys" \
  -H "Authorization: Bearer YOUR_NETLIFY_TOKEN" \
  -H "Content-Type: application/zip" \
  --data-binary @deploy.zip
```

Get your token at: https://app.netlify.com/user/applications#personal-access-tokens

### Option 4 — Connect GitHub repo

1. Go to [app.netlify.com](https://app.netlify.com) → **Add new site → Import from Git**
2. Connect the GitHub repo: `https://github.com/gauravkaaizan/readablelabs`
3. Set **Publish directory** to `.` (the root, since there's no build step)
4. Click **Deploy** — every push to `main` will auto-deploy

---

## Custom Domain Setup (Namecheap + Netlify)

### Step 1 — Add the domain in Netlify

1. Go to [app.netlify.com](https://app.netlify.com) and open the **readablelabs** site
2. Click **Site settings → Domain management → Add a domain**
3. Type `readablelabs.io` and click **Verify → Add domain**

### Step 2 — Add DNS records in Namecheap

1. Log in to [namecheap.com](https://namecheap.com)
2. Go to **Domain List → Manage** next to `readablelabs.io`
3. Click the **Advanced DNS** tab
4. Delete any existing default `A` or `CNAME` records
5. Add these two records:

| Type | Host | Value | TTL |
|------|------|-------|-----|
| `A` | `@` | `75.2.60.5` | Automatic |
| `CNAME` | `www` | `readablelabs.netlify.app` | Automatic |

> **Note:** Make sure Nameservers in Namecheap is set to **Namecheap BasicDNS** (not custom nameservers), otherwise the Advanced DNS tab won't control your records.

### Step 3 — Wait for DNS propagation

DNS changes take anywhere from a few minutes to 24 hours. Check progress at [dnschecker.org](https://dnschecker.org) — enter `readablelabs.io` and watch for the `A` record to show `75.2.60.5` worldwide.

### Step 4 — SSL (fully automatic, no action needed)

Once Netlify detects the DNS is pointing correctly, it provisions a free SSL certificate automatically via Let's Encrypt. You will get an email from Netlify when it's ready. The site will then be live and secured at:

- `https://readablelabs.io`
- `https://www.readablelabs.io`

---

## Sections

| # | Section | Notes |
|---|---------|-------|
| 1 | Nav | Sticky, blur backdrop, green CTA |
| 2 | Hero | Left-aligned, scroll-animated, pulsing dot eyebrow |
| 3 | Problem | Two-column: copy left, issue card panel right |
| 4 | Solution | 6-card grid (3-col) + meta row |
| 5 | How It Works | 2x2 step cards + italic callout note |
| 6 | About | Two-column sidebar layout, real headshot |
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
- Non-breaking hyphen (`&#8209;`) used in "E&#8209;commerce" headings to prevent mid-word line breaks
- All CTAs link to Calendly

---

## Content Rules

See `CLAUDE.md` for full guidelines. Key rules: no em dashes in copy, all text must be humanized.

---

© 2025 Readable Labs. All Rights Reserved.
