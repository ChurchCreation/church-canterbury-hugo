# Canterbury — a free church website template for Hugo

A free website template for Anglican, Episcopal and Catholic parishes. It knows the church year: the season is computed from the date and colours the page, and the movable feasts are worked out rather than typed in, so the calendar is never out of date. Pages for services, music, the church year, and weddings, baptisms and funerals. Self-hosted typefaces, dark mode, and no external requests.

**[Live demo](https://churchcreation.com/demo/canterbury/)** · **[About this template](https://churchcreation.com/templates/canterbury/)** · 8 pages · MIT

![Home page](https://raw.githubusercontent.com/ChurchCreation/church-canterbury-hugo/main/images/preview.jpg)

| Dark mode | On a phone |
|---|---|
| ![The same page in dark mode](https://raw.githubusercontent.com/ChurchCreation/church-canterbury-hugo/main/images/preview-dark.jpg) | ![The same page on a phone](https://raw.githubusercontent.com/ChurchCreation/church-canterbury-hugo/main/images/preview-mobile.jpg) |

## Getting started

Needs Hugo 0.150+ (extended not required).

```bash
git submodule add https://github.com/ChurchCreation/church-canterbury-hugo.git themes/church-canterbury-hugo
```

Then set the theme in your site's configuration:

```toml
theme = 'church-canterbury-hugo'
uglyURLs = true          # the runtime resolves paths from a flat .html URL

[security]
  allowContent = ['^text/html$', '^text/markdown$']
```

To see it with this parish's pages, run the bundled example site:

```bash
cd exampleSite && hugo server --themesDir ../..
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

MIT — see [LICENSE.md](LICENSE.md). Use it for your church, for a client, commercially, whatever. Attribution appreciated, not required. Bundled typefaces are SIL OFL 1.1; see `core/fonts/FONTS.md`.

Photography in the live demo is from Unsplash and is credited in `CREDITS.md`; the download ships neutral placeholders instead.

---

One of ten [free church website templates](https://churchcreation.com/templates/) from ChurchCreation. Built for [Hugo](https://gohugo.io/).
