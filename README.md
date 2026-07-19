# Atelier — made-to-measure prototype

A single-page clickable prototype. Fabric photos are **not** embedded in the HTML —
they are loaded at runtime from the `assets/fabrics/` folder, so you can change any
fabric's cloth by just replacing an image file in the repo (no code edits).

## Structure

```
index.html                 the prototype (references the image folder below)
assets/
  fabrics/
    poplin.jpg   linen.jpg   oxford.jpg   khadi.jpg   chambray.jpg  silk.jpg   ← tops
    twill.jpg    linenb.jpg  wool.jpg     cord.jpg    denim.jpg     gab.jpg    ← bottoms
```

## How the images are picked up

`index.html` maps each fabric id to `assets/fabrics/<id>.jpg`:

| Fabric (shown in app) | id / file          |
|-----------------------|--------------------|
| Cotton Poplin         | `poplin.jpg`       |
| Pure Linen            | `linen.jpg`        |
| Oxford                | `oxford.jpg`       |
| Handspun Khadi        | `khadi.jpg`        |
| Chambray              | `chambray.jpg`     |
| Silk Blend            | `silk.jpg`         |
| Cotton Twill          | `twill.jpg`        |
| Linen Blend           | `linenb.jpg`       |
| Wool Blend            | `wool.jpg`         |
| Fine Corduroy         | `cord.jpg`         |
| Raw Denim             | `denim.jpg`        |
| Gabardine             | `gab.jpg`          |

- **To change a fabric's photo:** replace `assets/fabrics/<id>.jpg` with your own image
  (keep the same filename). Square-ish, well-lit close-ups of the cloth work best.
- **To make a fabric use the generated woven texture instead of a photo:** delete that
  fabric's line from the `PHOTOS = { ... }` map near the top of the `<script>` in `index.html`.

Each photo shows up in three places automatically: the swatch tile, the garment preview,
and the review screen.

## Run / host

- **Locally:** open `index.html` in a browser, or run `python3 -m http.server` in this
  folder and visit http://localhost:8000.
- **GitHub Pages:** in the repo, Settings → Pages → deploy from the `main` branch (root).
  The site will be at `https://<username>.github.io/<repo>/`.
