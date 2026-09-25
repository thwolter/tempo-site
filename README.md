# Tempo website

The bilingual product website for Tempo. It is plain HTML and CSS, with no build step or package dependencies.

## Layout

- `site/` is the deployable document root. `index.html` is the German landing page and `en.html` is the English version.
- `site/styles.css` contains the shared site styles; `site/assets/` contains the images used by the pages.
- The German and English legal pages are `impressum.html` / `legal-notice.html` and `datenschutz.html` / `privacy.html`.
- `design/palette.html` is a standalone preview of Tempo's application palette. It is not part of the website.

## Preview locally

From the repository root, run:

```sh
python3 -m http.server 8000 --directory site
```

Open `http://localhost:8000/` for German or `http://localhost:8000/en.html` for English. Open `design/palette.html` directly to inspect the palette preview.

## Publishing and changes

No host or deployment process has been selected. When one is chosen, configure its document root as `site/`; deploy the contents of that directory, not the entire repository. Keep relative links between the pages, stylesheet, and assets working from that root.

Small interactions can use browser-native JavaScript modules in `site/` without a build step. Introduce a build tool only if a feature actually needs one.

Before publishing, replace the bracketed operator, contact, and hosting-provider placeholders in all four legal pages and review the statements against the selected hosting arrangement.
