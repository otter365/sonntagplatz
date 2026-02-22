# Sonntagplatz

Sonntagplatz is a small, static website built as a long-term writing system and a hands-on learning project.

It is structured into four verticals:

- **AberSonntag** — Torah, ethics, and foundational frameworks  
- **DochSonntag** — world systems, institutions, and incentives  
- **UndSonntag** — product strategy, technical architecture, and execution  
- **NurSonntag** — craft: photography, culinary notes, and daily curiosities

Live site: https://sonntagplatz.com

---

## Why this exists

- To publish concise essays across four domains without diluting the identity of each section.
- To keep the implementation simple (hand-written HTML/CSS) while applying disciplined SEO basics.
- To evolve gradually into a scalable content system once publishing cadence justifies it.

---

## Architecture

This is a static site (no framework, no server-side rendering).

Current structure:
- `index.html` — portal / navigation to the four sections  
- `aber.html`, `doch.html`, `und.html`, `nur.html` — section hubs  
- `style.css` — global styling  
- `images/` — OG images and icons  
- `site.webmanifest` — PWA metadata

Planned (manual, tidy):
- `/<section>/<slug>.html` — one file per article
- section hub pages list and link to articles

---

## SEO baseline

The goal is consistent metadata and crawlability without heavy tooling.

Implemented / tracked:
- canonical URLs
- Open Graph + Twitter cards
- `robots.txt`
- `sitemap.xml`
- JSON-LD (structured data)

Quality rule of thumb:
- page headline, title tag, description, and social previews should all describe the same page.

---

## Deployment

Development is local in VS Code and deployed through GitHub → Cloudflare Pages CI/CD.

---

## Roadmap (short)

- Fix remaining OG image path / MIME inconsistencies
- Standardize favicon + manifest paths
- Add article template for manual posting (`/templates/post-template.html`)
- Add section hubs with internal linking between clusters