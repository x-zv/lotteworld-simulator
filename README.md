# Lotte World Simulator

A browser-based 3D blockout of the visible exterior environment of Lotte World, built as an expandable simulation prototype.

## Current build

- Lotte World Adventure main building mass and glass-dome silhouette
- Front entrance plaza, portico, side wings, and approach roads
- Magic Island landform, surrounding Seokchon Lake, and Magic Castle silhouette
- Placeholder silhouettes for major outdoor ride structures
- Orbit camera controls, zoom, pan, reset view, and landmark labels
- Procedural geometry; no external 3D model assets required

## Run

Open `index.html` in a modern browser with an internet connection. Three.js is loaded from jsDelivr CDN.

For a local server:

```bash
python3 -m http.server 8000
```

Then visit http://localhost:8000.

## Roadmap

1. Verify the overall site plan and building proportions against current official maps and reference photography.
2. Add accurate paths, entrances, facades, roofs, bridges, and terrain.
3. Replace placeholder ride silhouettes with individual ride models.
4. Add interior floors, guest navigation, queues, ride operation, and simulation systems.

## Accuracy note

This is an early visual blockout, not a surveyed or dimensionally accurate reconstruction. Dimensions and positions are intentionally approximate and will be refined as reliable references are added. This is an unofficial fan-made project and is not affiliated with or endorsed by Lotte World or Lotte Corporation.
