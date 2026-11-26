# Lotte World Simulator

A browser-based 3D blockout of the visible exterior environment of Lotte World, built as an expandable simulation prototype.

## Current build

- Lotte World Adventure main building mass and glass-dome silhouette
- Front entrance plaza, portico, side wings, and approach roads
- Magic Island landform, surrounding Seokchon Lake, and Magic Castle silhouette
- Placeholder silhouettes for major outdoor ride structures
- Orbit camera controls, zoom, pan, reset view, and landmark labels
- Seasonal parade system with three animated floats following a looped route inside the Adventure building
- Season theme selected from the local calendar month; the current November 2026 build selects the winter `해피 크리스마스 퍼레이드` theme
- Parade auto-starts every 10 minutes after the page is opened; `퍼레이드 미리보기` starts one immediately for testing
- Procedural geometry; no external 3D model assets required

## Run

Open `index.html` in a modern browser with an internet connection. Three.js is loaded from jsDelivr CDN.

For a local server:

```bash
python3 -m http.server 8000
```

Then visit http://localhost:8000.


## Walkable park and interactions

The scene now has stacked walkable levels for B1F and 1F–4F, plus a pedestrian bridge to the Magic Island blockout. Visitors can move with WASD or the arrow keys on desktop and with the on-screen direction pad on touch devices. The nearest facility shows an interaction prompt; press E on desktop or tap the action button on mobile.

The initial facility catalog contains:
- 42 attraction entries across B1F, 1F, 2F–4F, and Magic Island
- 26 dining entries
- 15 shop entries
- 28 guest-service and vertical-circulation entries, including elevators, escalators, stairs, restrooms, lockers, first aid, guest relations, and other amenities

Interaction behavior:
- **Attractions:** open a ride card and start a short animated boarding sequence.
- **Elevators:** choose B1F or 1F–4F; a lift cabin moves with the visitor between floors.
- **Escalators and stairs:** move to the adjacent floor.
- **Restaurants:** choose a sample menu category and play a short meal simulation.
- **Shops and services:** open a facility-specific information or browsing panel.

The catalog and the 3D models are an expandable first-pass blockout. Each entry has a visible sign and a category-specific model, but exact footprint, ride geometry, routes, interiors, menu items, and current operation status still need to be refined using verified references. Facility placement is approximate rather than surveyed.

## Parade behavior

The simulator uses a ten-minute real-time interval measured from page load. Each parade procession lasts about 110 seconds and has a manual preview button. This interval is intentionally a simulator rule, not a recreation of the park's published show timetable. The current winter theme is based on Lotte World's 2026 winter season announcement; the parade floats are original generic winter-themed placeholders rather than exact character or float replicas.

Season themes are selected automatically from the local calendar month. Winter, spring, summer, and autumn currently have separate color palettes and parade decorations; the winter theme is the most developed in this build.

## Reference material

- Lotte World official winter-season announcement: https://www.youtube.com/watch?v=BgzsANrByC8
- 2026 winter parade report and seasonal details: https://www.kmib.co.kr/article/20261125502043

## Roadmap

1. Verify the overall site plan and building proportions against current official maps and reference photography.
2. Add accurate paths, entrances, facades, roofs, bridges, and terrain.
3. Replace placeholder ride silhouettes with individual ride models.
4. Add interior floors, guest navigation, queues, ride operation, and simulation systems.

## Accuracy note

This is an early visual blockout, not a surveyed or dimensionally accurate reconstruction. Dimensions and positions are intentionally approximate and will be refined as reliable references are added. This is an unofficial fan-made project and is not affiliated with or endorsed by Lotte World or Lotte Corporation.
