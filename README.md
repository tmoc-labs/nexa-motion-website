# nexa-motion-website

Static design prototypes of the Nexa Motion site, published with GitHub Pages.

- `site/index.html` — home page that links to every version
- `site/versions.json` — the list of versions the home page shows
- `site/versions/<slug>/` — one self-contained prototype per folder (`index.html`, its runtime in `support.js` and `vendor/`, and images in `assets/`)
- `.github/workflows/pages.yml` — deploys `site/` to GitHub Pages on every push to `main`

## Adding a version

1. Unzip the export into `site/versions/<slug>/` and rename its `*.dc.html` file to `index.html`.
2. Add an entry to `site/versions.json` (`slug`, `title`, `note`, `added`, and a `thumbnail` path relative to the version folder).

## Local preview

```bash
python3 -m http.server 8765 --directory site
```

Then open http://localhost:8765. The page does not load over `file://`.
