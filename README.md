# BeSpoke by The Indian Motif — clickable prototype

A single, self-contained clickable prototype (research build).

## Files
- `index.html` — the whole prototype, including the logo (embedded). Nothing
  else is required for it to render.
- `.nojekyll` — tells GitHub Pages to serve files as-is.

## Deploy on GitHub Pages
1. Commit `index.html` (and `.nojekyll`) to your repo — repo root is simplest.
2. Repo → Settings → Pages → Source: your branch, folder `/ (root)`.
3. Open the published URL. The logo is baked into the page, so there is no
   separate image file to misplace and nothing to 404.

The logo is embedded as a data URL, so the page works identically when opened
locally (double-click), served over HTTP, or hosted on GitHub Pages.
