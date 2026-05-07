# Lake & Lederman Cost Segregation — Marketing Site

Single-page marketing site for Lake & Lederman PLLC.
Static HTML with Tailwind CSS + Alpine.js (CDN-loaded). No build step.

## Files

| File | What it is |
|---|---|
| `index.html` | The entire site. Open in any browser to preview locally. |
| `netlify.toml` | Netlify build/header config. |
| `robots.txt` | Tells search engines they may crawl the site. |
| `sitemap.xml` | One-URL sitemap for SEO. |
| `_redirects` | Netlify redirect rules (single-page fallback). |
| `assets/` | Reserved for future images/logos. |

## Local preview

Just double-click `index.html`, or run a tiny local server:

```bash
cd lake-lederman-website
python3 -m http.server 8000
# then open http://localhost:8000 in your browser
```

## Deploying to Netlify

See **Netlify_Deployment_Guide.pdf** in the parent folder.
Two-minute version:

1. Create a free GitHub account; create a new repo named `lake-lederman-website`.
2. Drag this entire folder into the GitHub web upload page; commit.
3. Go to netlify.com → "Add new site" → "Import from GitHub" → pick the repo.
4. Click Deploy. Netlify gives you a free `*.netlify.app` URL within ~30 seconds.
5. (Optional) Buy a domain (e.g. lakeledermancostseg.com) and connect it under
   Site settings → Domain management.

## Editing content

Most of the page text and case-study data lives directly in `index.html`.
Search for `[PLACEHOLDER]` to find every spot that needs your real content
(bios, license numbers, phone, email, address). Replace and re-deploy.

The interactive checklist data lives near the bottom of `index.html`,
inside the `dashboard()` function. Add/remove items in the `seed = [ ... ]`
array.
