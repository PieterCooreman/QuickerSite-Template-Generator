# QuickerSite Template Builder

**Live version:** [https://pietercooreman.github.io/QuickerSite-Template-Generator/](https://pietercooreman.github.io/QuickerSite-Template-Generator/)

A single-file HTML application that generates random, responsive website templates for [QuickerSite](https://quickersite.com), an ASP/VBScript CMS for Windows Servers.

## What it does

Open `index.html` in a browser. Click **Suggest Random Template** to generate a complete QuickerSite-compatible `page.html` template. Each generation randomizes colors, fonts, layout, header images, and structure. You can also fine-tune every setting manually -- changes are applied instantly in the live preview.

Download the result or copy the source to your clipboard, then import it into QuickerSite.

## Features

- **Fully randomized templates** -- 16 color schemes, 15+ heading/body font pairings, 5 header styles, 4 hero styles, 23 Unsplash header images, sidebar/banner/footer variations
- **Live preview** with desktop and mobile views, plus a source code viewer
- **Auto-regeneration** on every control change (no need to click a button)
- **Pure CSS mobile menu** using a checkbox hack -- no JavaScript dependency, works reliably with QuickerSite's jQuery environment
- **Bootstrap 3 menu compatibility** -- targets the exact `ul.nav.navbar-nav` / `.dropdown` / `.dropdown-menu` class structure that `[QS_BOOTSTRAPMENU_3]` outputs

## QuickerSite variables included

Every generated template contains these standard QuickerSite placeholders:

### Head section
| Variable | Purpose |
|---|---|
| `[TITLETAG]` | Page title |
| `[METATAG_AUTHOR]` | Author meta |
| `[METATAG_COPYRIGHT]` | Copyright meta |
| `[METATAG_KEYWORDS]` | Keywords meta |
| `[METATAG_DESCRIPTION]` | Description meta |
| `[C_DIRECTORY_QUICKERSITE]` | Path to QS css directory |
| `[METATAG_REFRESH]` | Meta refresh (if any) |
| `[RSSLINK]` | RSS link element |
| `[FAVICON_LINK]` | Favicon link |
| `[JAVASCRIPT]` | QS JavaScript includes |
| `[GOOGLEANALYTICS]` | Analytics code (optional) |
| `[PAGEHEADER]` | Additional head content |

### Body section
| Variable | Purpose |
|---|---|
| `[SITENAME]` | Site name (header, hero, footer) |
| `[SITESLOGAN]` | Site slogan |
| `[QS_BOOTSTRAPMENU_3]` | Bootstrap 3 horizontal navigation |
| `[PAGETITLE]` | Current page title |
| `[PAGEBODY]` | Page body content |
| `[PAGELIST]` | List content |
| `[PAGEFORM]` | Form content |
| `[PAGECATALOG]` | Catalog content |
| `[PAGEFEED]` | Feed content |
| `[PAGEAPPLICATION]` | Application content |
| `[PAGETHEME]` | Theme/forum content |
| `[PAGEBREADCRUMBS]` | Breadcrumb navigation |
| `[QSHIGHLIGHTSLABEL]` | Highlights banner title |
| `[QSHIGHLIGHTS]` | Highlights banner content |
| `[QSCONTACTINFOLABEL]` | Contact info banner title |
| `[BANNER]` | Contact info banner content |
| `[QSSITEFOOTER]` | Footer text |
| `[RSSLINKART]` | RSS icon link (optional) |
| `[PAGERENDERTIME]` | Page render time |

### Search form
The standard QS search form block is included with `<!-- START SEARCHFORM -->` / `<!-- END SEARCHFORM -->` markers and uses `[SF_ACTIONURL]`, `[SF_HIDDENFIELD]`, and `[SF_TEXTVALUE]`.

## Template quality

Generated templates include:

- **Google Fonts** loaded via `<link>` with `preconnect` hints (not `@import`)
- **`<meta name="theme-color">`** set to the primary color
- **Skip-to-content** accessibility link
- **Visually-hidden labels** on search inputs for screen readers
- **Single `<h1>`** per page (logo downgrades to `<div>` when hero is present)
- **Print stylesheet** that hides navigation/sidebar/footer and shows content full-width
- **Link color contrast** automatically adjusted if too close to text or background color
- **Responsive** at 768px breakpoint -- single-column layout, CSS-only hamburger menu with flat submenu display

## How to use with QuickerSite

1. Open `index.html` in your browser
2. Click **Suggest Random Template** until you find a design you like (or adjust settings manually)
3. Click **Copy source** or save as `page.html`
4. In QuickerSite backsite, go to **Setup > Templates > New template**
5. Paste the html code
6. Activate the template

## Requirements

- A modern browser to run the builder (Chrome, Firefox, Edge, Safari)
- QuickerSite v4.x to use the generated templates

## Credits

- Header background images from [Unsplash](https://unsplash.com)
- Fonts from [Google Fonts](https://fonts.google.com)
- Built for [QuickerSite CMS](https://quickersite.com) by Pieter Cooreman
