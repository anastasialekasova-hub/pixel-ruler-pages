# Pixel Ruler — pages

Welcome, uninstall and privacy pages for the Pixel Ruler Chrome extension,
served via GitHub Pages.

- `welcome/` opens once on install (`chrome.runtime.onInstalled`, reason `install`)
- `uninstall/` opens when the extension is removed (`chrome.runtime.setUninstallURL`)
- `privacy/` is the privacy policy linked from the Chrome Web Store listing

The repository must stay **public** — GitHub Pages does not serve private repos
on the free plan.

## Screenshots on the welcome page

The browser frames on `welcome/` are drawn in HTML and CSS rather than captured,
so they are already free of tabs, other extensions and personal data, and stay
sharp on any display. If you prefer real captures later, replace the two
`.frame` blocks with `<img>` tags — keep the red arrows and the numbers.

## Uninstall feedback

`uninstall/index.html` posts to a Google Form. Fill in `FORM_ID`,
`ENTRY_REASON` and `ENTRY_DETAILS` at the bottom of the file from the form's
pre-filled link. Until they are filled the form still shows the thank-you
state, it just sends nothing.

## Publishing

1. Create a **public** repository named `pixel-ruler-pages` under the same
   GitHub account as the extension.
2. Push this folder to it and enable Pages (Settings → Pages → Deploy from a
   branch → `main` / root).
3. The extension already points at
   `https://anastasialekasova-hub.github.io/pixel-ruler-pages/welcome/` and
   `/uninstall/` — if the account or repository name differs, change the single
   `PAGES` constant in `src/background/service-worker.js`.
4. Link `privacy/` from the Chrome Web Store listing's privacy policy field.

### Own domain (module 3)

The methodology's domain rule — at most one word longer than five letters —
is satisfied by the product name itself: `pixel` (5) + `ruler` (5), so
**pixelruler.com** qualifies. Registering it early is worth it: the domain's
age matters later, and the pages can move there without touching the extension
beyond the `PAGES` constant.
