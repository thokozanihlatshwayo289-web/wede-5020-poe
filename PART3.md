Part 3 — Interactive Features, SEO, Forms, and Deployment
Date: 2026-06-19

Summary
- Implemented interactive UI: accordions, tabs, modals, lightbox gallery.
- Added Leaflet interactive map and sample marker.
- Implemented dynamic product/service cards and search/filter.
- Added client-side validation, AJAX simulation, and Netlify Forms support for `Contact us` and `enquiry` forms.
- Added SEO improvements: meta descriptions, canonical links, Open Graph tags, JSON-LD, `robots.txt`, and `sitemap.xml`.
- Added performance optimizations: minified CSS/JS, deferred scripts, lazy-loading images, and extra CSS to reduce layout shift.
- Added Netlify configuration and GitHub Actions workflow for CI deploys, and created `gh-pages` branch for GitHub Pages deployment.
- Added `thanks.html` for form submission confirmation.

Key files added or updated for Part 3
- `index.html` — homepage interactive section, SEO tags
- `Contact us.html` — Netlify form enabled, validation
- `enquiry.html` — Netlify form enabled
- `js/main.js`, `js/main.min.js` — interactive handlers
- `style.min.css`, `style.extra.css` — minified and extra styles
- `robots.txt`, `sitemap.xml`
- `netlify.toml`, `.github/workflows/deploy_netlify.yml`, `NETLIFY.md`
- `thanks.html`
- `PART3.md` (this file)

How to verify
1. Open `index.html`, `Contact us.html`, `enquiry.html` locally to review interactive features.
2. Deploy to Netlify (or check GitHub Pages): forms will be captured by Netlify Forms when deployed and configured.

Notes
- Form submissions are simulated via AJAX to httpbin when the "Send via AJAX (simulated)" checkbox is selected. Without AJAX, forms will submit to Netlify (if deployed and connected) or use mailto fallback on the contact form.
