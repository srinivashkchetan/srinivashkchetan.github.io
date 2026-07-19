# Atelier — made-to-measure prototype

A single-page clickable prototype. Fabric photos are loaded at runtime from the
`assets/fabrics/` folder, so you can change any fabric's cloth by replacing an
image file in the repo (no code edits).

## Structure

```
index.html            the prototype (references the image folder below)
assets/fabrics/       one photo per fabric (see table)
```

## Fabric library

Tops (12) and bottoms (8). Each fabric's `id` in `index.html` maps to a file in
`assets/fabrics/`. Filenames keep spaces (referenced URL-encoded in the code).

| Group  | Fabric              | File                          |
|--------|---------------------|-------------------------------|
| Top    | Indigo Dabu         | `Another indigo.jpeg`         |
| Top    | Yellow Floral       | `Flower in yellow.jpeg`       |
| Top    | Indigo Ikat         | `Indigo - 2.jpeg`             |
| Top    | Indigo Leaf Stripe  | `Indigo with leaves.jpeg`     |
| Top    | Indigo Buti         | `Indigo.jpeg`                 |
| Top    | Mural Print         | `Mural.jpeg`                  |
| Top    | Orange Buti         | `Orange.jpeg`                 |
| Top    | Blue Floral Buti    | `Pattern.jpeg`                |
| Top    | Pink Buti           | `Pink gawd.jpeg`              |
| Top    | Black Triangle Buti | `Triangle on black.jpeg`      |
| Top    | Turquoise Buti      | `Turq.jpeg`                   |
| Top    | Yellow Marigold     | `Yellow with orng flwr.jpeg`  |
| Bottom | Black Ikat          | `Black ikkat.jpeg`            |
| Bottom | Green Check         | `Greensquares.jpeg`           |
| Bottom | Pink Check Lungi    | `Red sq lungi.jpeg`           |
| Bottom | Mustard Ikat        | `Sanyasi.jpeg`                |
| Bottom | Ivory Stripe        | `White bands.jpeg`            |
| Bottom | Pink Windowpane     | `White lungi pink square.jpeg`|
| Bottom | Yellow Gingham      | `Yellow check.jpeg`           |
| Bottom | Black Check         | `black chq.jpeg`              |

- **To change a fabric's photo:** replace its file in `assets/fabrics/` (keep the
  same filename). The images here are already cropped to the cloth and resized for web.
- **To add / rename / re-map a fabric:** edit the `FAB` catalog and the `PHOTOS`
  map near the top of the `<script>` in `index.html`.

Each photo appears in three places automatically: the swatch tile, the garment
preview, and the review screen.

## Run / host

- **Locally:** run `python3 -m http.server` in this folder, then open
  http://localhost:8000.
- **GitHub Pages:** repo Settings → Pages → deploy from `main` (root). Served at
  `https://<username>.github.io/<repo>/`.
