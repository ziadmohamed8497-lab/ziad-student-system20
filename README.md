# CODINGـSystems — static HTML website

Plain HTML + CSS + JavaScript. Black & gold theme. No server, no database, no build step, no Node needed.

## Open / host it
- **Locally:** double-click `index.html` (or run `python3 -m http.server` in this folder).
- **Hosting:** upload the whole folder to any static host (Netlify, Vercel, Cloudflare Pages, GitHub Pages, cPanel/FTP).

## Edit settings — `assets/config.js`
- WhatsApp / TikTok / Instagram links (already set to the official accounts).
- `email`: empty = every email element stays hidden. Fill it to show it.
- `logoLight` / `logoDark`: put your official logo in `assets/img/` and write its path (e.g. `assets/img/logo.svg`). Until then a text wordmark is shown. Proportions are preserved.
- `formEndpoint` (optional): a form service URL (Formspree, Getform, Web3Forms…) that accepts a JSON POST. If set, the forms show a "Send request" button, and success is shown **only** if that service answers OK.

## How requests reach you (no server)
The forms open **WhatsApp with a prefilled message** to +20 127 891 0793. Nothing is sent until the visitor presses send in WhatsApp (the site says so). There are no customer accounts, no fake reference numbers, and no stored data. Attachments are not possible on a static site — visitors attach them in WhatsApp.

## Not included (needs a server)
Admin dashboard, database, login, request references, file uploads, editing portfolio from a panel. To change content, edit the HTML (or `_tools/data.json` + run `python3 _tools/build.py`, which regenerates all pages).

## Languages
EN / AR switch (RTL), remembered in the browser (`localStorage`, language only). Every page contains both languages.

## Before launch
Upload the logo, set the email, review `privacy.html` and `terms.html` with a lawyer, replace the 3 **Concept** projects with real ones, and set `SITE_URL` in `_tools/build.py` then rebuild if you want a `sitemap.xml`.

## Important: extract the ZIP first
Unzip the whole folder before opening any page (do not open files from inside the ZIP viewer). The pages need the `assets/` folder next to them for scripts, fonts and images. Basic styling is embedded in every page, but the forms, language switch and menu need `assets/`.
