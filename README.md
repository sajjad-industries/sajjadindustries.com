# sajjadindustries.com

The Sajjad Industries holding page, served by GitHub Pages at `https://sajjadindustries.com/`
(custom domain, see `CNAME`). Static files only, no server. The brand images used by email live in
a separate repository, `sajjad-industries/www`, at `https://assets.sajjadindustries.com/`.

`index.html` is one file: styles inline with the values from the brand tokens, the lockup and font
loaded from this repository, no scripts, no form, nothing requested from another origin (a
Content-Security-Policy meta tag enforces it). It follows the reader's light or dark setting. All
paths in it are relative, so it also opens from a local web server:
`python3 -m http.server --bind 127.0.0.1` in this folder.

The accent colour is set once, by `--si-accent` and `--si-accent-ink` at the top of the styles.

| Path | Source in the company repository |
|---|---|
| `brand/lockup-horizontal-black.svg`, `brand/lockup-horizontal-white.svg` | `brand/logo/` (same names) |
| `favicon.ico`, `favicon.svg`, `favicon-16.png`, `favicon-32.png`, `apple-touch-icon.png`, `icon-192.png`, `icon-512.png`, `site.webmanifest` | `brand/exports/favicon/` |
| `fonts/IBMPlexSans-Variable.woff2` | `brand/fonts/IBMPlexSans[wdth,wght].ttf`, the whole font compressed to WOFF2 with `fonttools ttLib.woff2 compress`, not subset or renamed (the licence reserves the name "Plex" for unmodified copies) |
| `fonts/LICENSE-OFL.txt` | `brand/fonts/LICENSE-OFL.txt` |
| `og-image.png` | `brand/logo/lockup-stacked-white.svg` at 4 px per unit, centred on black, 1200 x 630 |

Never edit the copied files here: change the source, rebuild, and copy the result over.

`robots.txt` allows crawling and points to `sitemap.xml`, which lists the one page.

This repository is public. Nothing private goes in it, in any commit.
