# Atelier — made-to-measure prototype

A single-page clickable prototype. Fabric photos are loaded at runtime from the
`assets/fabrics/` folder, so you can change any fabric's cloth by replacing an
image file in the repo (no code edits).

Filenames are lowercase with no spaces — required for case-sensitive hosts like
GitHub Pages.

## Structure

```
index.html            the prototype (references the image folder below)
assets/fabrics/       one photo per fabric, named <id>.jpg (see table)
```

## Fabric library

| Group  | Fabric              | File                    |
|--------|---------------------|-------------------------|
| Top    | Indigo Dabu         | `indigodabu.jpg`        |
| Top    | Yellow Floral       | `yellowfloral.jpg`      |
| Top    | Indigo Ikat         | `indigoikat.jpg`        |
| Top    | Indigo Leaf Stripe  | `indigoleaf.jpg`        |
| Top    | Indigo Buti         | `indigobuti.jpg`        |
| Top    | Mural Print         | `mural.jpg`             |
| Top    | Orange Buti         | `orangebuti.jpg`        |
| Top    | Blue Floral Buti    | `bluebuti.jpg`          |
| Top    | Pink Buti           | `pinkbuti.jpg`          |
| Top    | Black Triangle Buti | `blacktriangle.jpg`     |
| Top    | Turquoise Buti      | `turqbuti.jpg`          |
| Top    | Yellow Marigold     | `marigold.jpg`          |
| Bottom | Black Ikat          | `blackikat.jpg`         |
| Bottom | Green Check         | `greencheck.jpg`        |
| Bottom | Pink Check Lungi    | `pinkcheck.jpg`         |
| Bottom | Mustard Ikat        | `mustardikat.jpg`       |
| Bottom | Ivory Stripe        | `ivorystripe.jpg`       |
| Bottom | Pink Windowpane     | `pinkwindow.jpg`        |
| Bottom | Yellow Gingham      | `yellowgingham.jpg`     |
| Bottom | Black Check         | `blackcheck.jpg`        |

- **To change a fabric's photo:** replace its `<id>.jpg` in `assets/fabrics/`
  (keep the same filename). Images here are already cropped to the cloth and
  resized for web.
- **To add / rename / re-map a fabric:** edit the `FAB` catalog and the `PHOTOS`
  map near the top of the `<script>` in `index.html`.

## Run / host

- **Locally:** run `python3 -m http.server` in this folder, then open
  http://localhost:8000.
- **GitHub Pages:** repo Settings → Pages → deploy from `main` (root). Served at
  `https://<username>.github.io/<repo>/`.
