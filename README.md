# Canterbury — a free church website template for Hugo

Parish Eucharist at 10, Choral Evensong at 6, and a church open every day from nine until dusk. Service times, the church year, weddings, baptisms and funerals.

**[Live demo](https://churchcreation.com/demo/canterbury/)** · **[About this template](https://churchcreation.com/templates/canterbury/)** · 8 pages · MIT

## Getting started

Needs Hugo 0.150+ (extended not required).

```bash
hugo server
```

Then build:

```bash
hugo          # writes public/
```

## Making it your church's

Almost everything a church needs to change lives in one file — **`static/church.config.json`**: name, address, phone, service times, giving link, social accounts. Edit that and the header, footer, contact page, map link and structured data all update together, so they cannot drift apart.

The rest:

| Where | What |
|---|---|
| `layouts/baseof.html` | the shared layout — header, footer, `<head>` |
| `content/*.html` | one file per page; the front matter carries its title and description |
| `data/nav.json` | the navigation, rendered by the layout with `aria-current` on the current page |

## What's included

8 pages: St Botolph's, Barwick, About, Contact, Weddings, baptisms and funerals, Music, Services, Plan a visit, The church year.

Self-contained: the typefaces are bundled and self-hosted, the CSS and JS ship with the template, and there are no external requests, no build step for the assets, and no tracking. Dark mode is included and respects the system setting.

## URLs are flat on purpose

Pages build to `about.html` rather than `/about/`. The template's own runtime depends on it: `core/js/ui.js` marks the current nav link by comparing the last path segment, and `core/js/config.js` fetches `church.config.json` by a relative path. Pretty URLs break both. If you would rather have them, change the two accordingly.

## Licence

MIT — use it for your church, for a client, commercially, whatever. Attribution appreciated, not required. Bundled typefaces are SIL OFL 1.1; see `core/fonts/FONTS.md`.

Photography in the live demo is from Unsplash and is credited in `CREDITS.md`; the download ships neutral placeholders instead.

---

One of ten [free church website templates](https://churchcreation.com/templates/) from ChurchCreation. Built for [Hugo](https://gohugo.io/).
