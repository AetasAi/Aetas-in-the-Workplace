# Aetas in the Workplace

Financial wellbeing consultancy site for SMEs, mid-sized businesses, charities, and not-for-profits.

**Live site:** https://itw.aetaspartners.com

---

## What the site covers

Aetas in the Workplace is a consultancy-led financial wellbeing service. The site presents the service to two primary audiences, each with a dedicated page:

- **Limited companies** — SMEs and mid-sized businesses where financial stress has a direct cost to productivity and retention
- **Charities and not-for-profits** — Organisations that need to support their people within tighter budget constraints, with additional governance and income opportunity angles

---

## Site structure

| File | Description |
|------|-------------|
| `index.html` | Homepage — overview of the service and both audience tracks |
| `limited-companies.html` | Audience page for SMEs and mid-sized businesses |
| `charities.html` | Audience page for charities and not-for-profits |
| `diagnostic.html` | 12-question self-assessment diagnostic tool |
| `insights.html` | Insights and articles |
| `faqs.html` | Frequently asked questions |
| `privacy.html` | Privacy policy |
| `CNAME` | Custom domain configuration (`itw.aetaspartners.com`) |
| `manifest.webmanifest` | PWA manifest for mobile and browser branding |
| `robots.txt` | Search engine and AI crawler instructions |
| `sitemap.xml` | Sitemap for search engines |
| `schema.json` | Structured data reference (also embedded as ld+json in each page) |
| `llms.txt` | AI crawler guidance |

---

## Design system

- Pure static HTML, CSS, and vanilla JavaScript — no build tools, frameworks, or Jekyll
- Custom design system using CSS variables (`--navy`, `--gold`, `--cream`, etc.)
- Typography: Cormorant Garamond (headings) and Jost (body text), loaded via Google Fonts
- Colour palette: `--navy: #1a2744`, `--gold: #b89a5a`, `--cream: #f8f4ee`
- Fully responsive; navigation collapses at 940px
- Deployed automatically via GitHub Pages on every push to `main`

---

## Updating the site

**To edit a page:** open the relevant `.html` file, make your changes, and commit to `main`. GitHub Pages redeploys automatically within about a minute.

**To update the navigation across all pages:** the nav block is duplicated in every `.html` file. If a nav link changes, update all pages. The `class="active"` attribute on each page's nav link indicates the current page.

**Primary CTA booking link (used across all pages):**
```
https://links.aetas-partners.com/widget/booking/IacdM2cW2bnLm0pK7Jty
```

**Webinar/event booking link:**
```
https://links.aetas-partners.com/widget/booking/4q95PzVyRtNPdzPavQzV
```

---

## Head tag requirements (all pages)

Every page must include the following in `<head>`. Adjust `og:title`, `og:description`, `og:url`, and `canonical` per page:

```html
<!-- Favicon -->
<link rel="icon" type="image/png" sizes="32x32" href="/icons/favicon-32.png" />
<link rel="icon" type="image/png" sizes="16x16" href="/icons/favicon-16.png" />
<link rel="apple-touch-icon" sizes="180x180" href="/icons/apple-touch-icon.png" />

<!-- PWA manifest and theme -->
<link rel="manifest" href="/manifest.webmanifest" />
<meta name="theme-color" content="#1a2744" />

<!-- Canonical -->
<link rel="canonical" href="https://itw.aetaspartners.com/[page-url]" />

<!-- Open Graph -->
<meta property="og:title" content="[Page title]" />
<meta property="og:description" content="[Page description]" />
<meta property="og:url" content="https://itw.aetaspartners.com/[page-url]" />
<meta property="og:type" content="website" />
<meta property="og:image" content="https://itw.aetaspartners.com/og-image.png" />
<meta property="og:image:width" content="1200" />
<meta property="og:image:height" content="630" />
<meta name="twitter:card" content="summary_large_image" />
```

---

## Contact

Matthew Steiner — [matthew.steiner@aetas-partners.com](mailto:matthew.steiner@aetas-partners.com) · 020 3633 0579

Financial wellbeing education and consultancy services do not constitute regulated financial advice. Where regulated advice is required, this is provided by Aetas Wealth, a trading style of Insight Financial Associates Limited, authorised and regulated by the FCA (registration 458421).
