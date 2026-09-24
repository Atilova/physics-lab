# Interactive physics

Self-contained HTML pages for exploring school physics by dragging things around. There is no build step and no dependency: open a file in a browser, or visit the published site.

## Pages

| Page | What it does |
|---|---|
| [`index.html`](index.html) | Landing page listing everything below |
| [`optics-bench.html`](optics-bench.html) | Optics bench: concave, convex and plane mirrors; converging and diverging lenses. Drag the object, image, F and C; obstacles; zoom and pan; English and Russian |

## Publishing

Every push to `master` runs [`.github/workflows/pages.yml`](.github/workflows/pages.yml), which publishes the repository root to GitHub Pages.

One-time setup after creating the repository: **Settings → Pages → Build and deployment → Source: GitHub Actions**. The repository must be public unless the account has a paid plan, because GitHub Pages is not available for private repositories on the free plan. Re-run the workflow from the Actions tab after enabling Pages.

## Adding a page

Put a new HTML file at the repository root and add a card for it in `index.html`. Keep pages self-contained (inline CSS and JavaScript) so they keep working when opened as plain files.

## Local preview

Open `index.html` directly in a browser, or serve the folder:

```sh
python3 -m http.server 8000
```
