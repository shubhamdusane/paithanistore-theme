# Paithani Store — Shopify Theme

**Live store:** paithanistore.com | **Base:** Dawn theme | **Updated:** March 2026

## Branch Strategy
| Branch | Purpose | Shopify |
|--------|---------|---------|
| `main` | Live store | Published theme |
| `staging` | Test before going live | Unpublished theme |

**Rule:** Push to `staging` first → preview in Shopify → merge to `main`

## Key Changes Made

### Bug Fixes
- **404 fix:** Removed `search.avada-seo.liquid` and `page.autoketing-*.liquid` (app templates causing routing conflict)
- **404 fix:** Disabled app blocks in settings_data.json for uninstalled apps
- **OG image fix:** Changed `http:` to `https:` (WhatsApp/Facebook shares now show images)
- **Speed fix:** Removed duplicate booster speed script

### SEO
- Organization + WebSite + LocalBusiness schema
- Product schema → https://schema.org + BreadcrumbList
- Collection SEO schema on all collection pages
- Twitter:image meta tag added
- robots.txt allows AI crawlers (GPTBot, Claude, Perplexity, OAI-SearchBot)

### Brand & UX
- Google Fonts: Cormorant Garamond (headings) + Lato (body)
- WhatsApp button: fixed, bottom 90px, z-index 99999 (above Shopify Inbox)
- Cart type: drawer (was notification)
- Cart note enabled for blouse sizes
- Theme-color: #812c2d (brand maroon)
- Improved 404 page with search + links

### New Files
- `snippets/paithani-trust-badges.liquid`
- `snippets/paithani-internal-links.liquid`
- `snippets/collection-seo-schema.liquid`
- `templates/collection.narayan-peth-saree.json`
- `templates/collection.paithani-shela.json`
- `templates/collection.wedding-paithani-saree.json`
- `templates/collection.nauvari-saree-online.json`
- `templates/collection.paithani-accessories.json`
- `templates/collection.designer-dupatta.json`
- `templates/robots.txt.liquid`

### Reference Docs (assets/)
- `SEO-META-TITLES-ALL-PAGES.md` — copy-paste titles for every page
- `blog-post-1,2,3` — 3 blog posts ready to publish
- `SEO-COMPETITOR-ANALYSIS-MARCH2026.md`

## Setup GitHub Secrets (for auto-deploy)
In repo Settings → Secrets → Actions, add:
- `SHOPIFY_STORE_URL` = `paithanistore.myshopify.com`
- `SHOPIFY_TOKEN` = your Shopify custom app token
- `SHOPIFY_LIVE_THEME_ID` = your live theme ID
- `SHOPIFY_STAGING_THEME_ID` = your staging theme ID
