# nexa-motion-website

Static design prototypes of the Nexa Motion site, published with GitHub Pages.

- `index.html` — home page that links to every version
- `versions.json` — the list of versions the home page shows
- `versions/<slug>/` — one self-contained prototype per folder (`index.html`, its runtime in `support.js` and `vendor/`, and images in `assets/`)
- GitHub Pages publishes the root of `main` directly; `.nojekyll` tells it to serve the files as-is

## Adding a version

1. Unzip the export into `versions/<slug>/` and rename its `*.dc.html` file to `index.html`.
2. Add an entry to `versions.json` (`slug`, `title`, `note`, `added`, and a `thumbnail` path relative to the version folder).

## Local preview

```bash
python3 -m http.server 8765
```

Then open http://localhost:8765. The page does not load over `file://`.
