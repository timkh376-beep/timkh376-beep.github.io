# LUMA

A café website — coffee, food and wine in Vienna. Static site, English and German.

**Live:** https://timkh376-beep.github.io/

> **LUMA is a conceptual project.** The café does not exist. The address, phone
> number and email are invented, and the reservation form does not send anything.

## What's here

| Page | English | German |
|---|---|---|
| Home | [/en/](https://timkh376-beep.github.io/en/) | [/de/](https://timkh376-beep.github.io/de/) |
| Menu | [/en/menu/](https://timkh376-beep.github.io/en/menu/) | [/de/menu/](https://timkh376-beep.github.io/de/menu/) |
| Desserts | [/en/desserts/](https://timkh376-beep.github.io/en/desserts/) | [/de/desserts/](https://timkh376-beep.github.io/de/desserts/) |
| Wine | [/en/wine/](https://timkh376-beep.github.io/en/wine/) | [/de/wine/](https://timkh376-beep.github.io/de/wine/) |
| Story | [/en/story/](https://timkh376-beep.github.io/en/story/) | [/de/story/](https://timkh376-beep.github.io/de/story/) |

Fifteen dishes, ten desserts, eleven wines, a scroll-driven video sequence,
a filterable menu, a tasting calendar and a dessert carousel.

## Running it locally

The pages load their own assets, which a browser refuses to do from `file://`,
so they need a server — any server will do:

```sh
python3 -m http.server 8765
```

Then open http://localhost:8765/en/

## How it's built

A pre-built [Next.js](https://nextjs.org) static export, committed as plain
files and served straight from the repository root by GitHub Pages. There is no
build step in this repository and no dependencies to install.

`.nojekyll` matters: without it GitHub Pages runs Jekyll, which skips
directories beginning with an underscore — and every script, stylesheet and font
lives in `_next/`. The page would load blank.

## Fonts and media

Fonts are self-hosted in `_next/static/media/`; nothing is fetched from a CDN,
so the site works with no third-party requests at all.
