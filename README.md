# David Hosking – personal academic website

Static single-page site served by GitHub Pages at https://dhosking16.github.io.
Plain HTML and CSS with no build step. Type is set in Playfair Display and Libre Caslon Text, loaded from Google Fonts.

## Layout

| Path | What it is |
| --- | --- |
| `index.html` | All content: masthead, About, Research, PhD opportunities, Publications, Teaching, footer |
| `assets/css/style.css` | All styling; colours and fonts are variables at the top |
| `images/` | Headshot, figures, the link-preview image (`og-image.jpg`) and `logos/` (institution crests) |
| `documents/cv.pdf` | The public version of the CV |
| `favicon.*`, `apple-touch-icon.png` | Site icons |

## Editing

- Publications use the `.ledger` list: copy an `<li class="ledger__item">` block to add an entry. Each entry has authors, title and venue lines.
- To add a section, copy a `<section class="section">` block and add a matching link in the masthead nav; the side menu copies the nav automatically.
- After changing `style.css`, bump the `?v=` number on its `<link>` in `index.html` so browsers fetch the new file. Do the same for the icon links after changing an icon.
- Only ever put the public CV in `documents/`.

## Preview locally

```bash
python3 -m http.server 8765 --bind 127.0.0.1
```

Then open http://127.0.0.1:8765.

## Deploy

Push to `main`. GitHub Pages serves the repository root; changes appear within a minute or two.

## Crest attribution

The crests in `images/logos/` are from Wikimedia Commons:

- Oxford: [Oxford-University-Circlet.svg](https://commons.wikimedia.org/wiki/File:Oxford-University-Circlet.svg), public domain.
- Princeton: [Princeton University Shield.svg](https://commons.wikimedia.org/wiki/File:Princeton_University_Shield.svg), public domain.
- Cambridge: [Coat of Arms of the University of Cambridge.svg](https://commons.wikimedia.org/wiki/File:Coat_of_Arms_of_the_University_of_Cambridge.svg), CC BY-SA 3.0, derived from Cambridge University Crest.svg by Massive.
- Edinburgh: [University of Edinburgh arms.svg](https://commons.wikimedia.org/wiki/File:University_of_Edinburgh_arms.svg) by Hogweard, public domain.

The arms themselves are the property of the respective universities.
