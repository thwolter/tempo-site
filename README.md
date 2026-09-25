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

## macOS launch checklist

- Replace the bracketed operator name, postal address, working contact email, and hosting-provider details in all four legal pages. Verify that the privacy wording matches the actual host and domain setup. A domain registration alone does not provide a working mailbox.
- Add the live Mac App Store listing link to both landing pages after the listing is approved. Until then, the pages correctly say that the macOS release is in preparation. Windows and Linux are described as later plans.
- Check the final screenshots against the released macOS build. The two-image interruption sequence shows the paused original task and the separate interruption; a third screenshot showing the original task returned paused would complete the sequence. Review the example data before a connected screenshot story is published.
- Verify the rendered German and English pages at desktop and mobile widths on the chosen host, including all legal links and the App Store link when added.

The landing pages use locally stored screenshot assets and do not load third-party images. The outbound Slint link is an ordinary link; the desktop app contains Slint's About widget for attribution.
