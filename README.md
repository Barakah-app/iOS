# Barakah — Public Website

This repository hosts the public website for **Barakah**, a private baby and family care tracking app for iOS.

The site is published via GitHub Pages at:  
**https://Barakah-app.github.io/iOS**

## Pages

| File | URL | Purpose |
|------|-----|---------|
| `index.html` | `/` | Landing page |
| `privacy.html` | `/privacy.html` | Privacy Policy |
| `support.html` | `/support.html` | Support & FAQ |

Each page also ships in `ar`/`es`/`fr`/`tr` (e.g. `index.ar.html`), linked via `hreflang` tags.

## Editing

The checked-in `.html` files are **generated** — don't hand-edit them directly, edits will be
overwritten. Shared boilerplate (head/meta/nav/footer/hreflang, per-language nav/footer strings)
lives in `build/generate.py`; translated page copy lives in `build/content/{page}.{lang}.html`.
Each page type's CSS lives once in `build/css/{page}.css` (identical across all 5 languages of
that page).

- **Change shared UI text** (nav labels, footer/copyright, lang-switcher) → edit the `UI` dict in
  `build/generate.py`.
- **Change a page's title/meta description** → edit `PAGE_META` in `build/generate.py`.
- **Change a page's actual content** for one language → edit `build/content/{page}.{lang}.html`.
- **Change styling** for a page type → edit `build/css/{page}.css`.

Then regenerate and commit the output:

```sh
python3 build/generate.py
```

## About Barakah

Barakah helps parents log feedings, sleep, diapers, growth measurements, medications, and milestones. Data syncs privately through iCloud — no account required, no third-party servers.

**Contact:** barakah-app@proton.me  
**© 2026 BARAKAH TECHNOLOGIES, INC.**
