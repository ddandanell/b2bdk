# Assets — How We Store and Name

All images, logos, screenshots, PDFs, and downloadable files live under
`/system/assets/` with a strict naming convention. **No exceptions.**

## Folder structure

```
/system/assets/
  brand/             — logo, wordmark, favicon, brand color swatches
  og/                — Open Graph 1200×630 social-share cards
  hero/              — hero shots per area page
  ui/                — UI element exports (icons, illustrations)
  photos/            — real photos (member-approved, model-released)
    _releases/       — signed model-release PDFs (one per photo)
  screenshots/       — competitor + our own, for research
  pdf/               — downloadable PDFs (terms, member welcome pack)
```

## Naming convention

```
{area-code}-{persona-code}-{purpose}-{dimensions}.{ext}
```

Examples:
- `a1-p1-hero-1200x630.jpg` — A1 scooter area, P1 Lukas persona, hero, OG size
- `a0-p5-membership-cta-800x600.jpg` — homepage, James persona
- `brand-wordmark-512x128.svg`
- `og-homepage-1200x630.jpg`
- `screenshot-balipremiumtrip-pricing-2026-05.png`

Rules:
- Lowercase. Hyphens only. **No spaces. No underscores** (except `_releases`).
- Always include dimensions for raster images.
- SVG for logos and icons.
- JPG for photos (80% quality), PNG only when transparency is required.
- WebP versions auto-generated next to JPG/PNG via build step (future).

## Image size budgets

| Type | Max KB |
| --- | --- |
| Hero JPG | 120 |
| OG card JPG | 80 |
| UI icon SVG | 5 |
| Body photo JPG | 60 |
| Anything else | **200 (requires approval)** |

## Approval

Any photo of a real person needs a signed model release stored in
`/system/assets/photos/_releases/` **before** it goes on a public page.

## Forbidden

- Stock photos of "diverse smiling expats holding laptops on a beach"
- Stock photos of Bali sunsets used as decoration
- AI-generated faces (we don't fake testimonials)
- Anything we don't have rights to use
- Watermarks from preview-tier stock sites

## When the web-designer agent uses an asset

The agent must:
1. Confirm the file exists in `/system/assets/`
2. Reference it by relative path from the page being built
3. Include the dimensions in the HTML `width`/`height` attributes
4. Never inline base64 images larger than 2 KB

## When the researcher agent saves a screenshot

Format: `screenshot-{competitor-or-source}-{topic}-{YYYY-MM}.png`

Drop into `/system/assets/screenshots/`. Reference it from the matching
research file in `/system/research/`.
