# Lotte World Simulator

A browser-based, walkable 3D theme-park reconstruction prototype inspired by public photographs and official guide-map references for Lotte World Adventure and Magic Island.

## Current build

- Elliptical half-dome roof with repeated metal ribs and horizontal glazing bands
- Photo-inspired Adventure entrance facade with an inset arch, clock face, tiled stone palette, signage, columns, and side wings
- Multi-level exterior facade mullions, structural piers, and gallery rail details
- Magic Island landform, Seokchon Lake, stone approach bridge, and pastel Magic Castle with blue conical turrets, arched windows, trim, and finials
- Distinct procedural geometry for recognizable attraction families: carousel, pirate ship, gyro rides, coaster loops, water rides, balloon flight, teacups, bumper cars, children’s rides, themed dark-ride facades, and more
- Restaurant and shop storefronts with separate wall palettes, glazing, awnings, tables, and illuminated-style sign panels
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

The catalog and 3D models are still a photo-matched approximation, not a surveyed or CAD-accurate replica. Representative structures now have distinct silhouettes and palettes, while less-photographed attractions use theme-specific procedural models. Exact dimensions, track centerlines, support placement, interior architecture, shopfront branding, and facility coordinates still need validation against close-up photographs or measured drawings. Facility placement is approximate rather than surveyed.

## Parade behavior

The simulator uses a ten-minute real-time interval measured from page load. Each parade procession lasts about 110 seconds and has a manual preview button. This interval is intentionally a simulator rule, not a recreation of the park's published show timetable. The current winter theme is based on Lotte World's 2026 winter season announcement; the parade floats are original generic winter-themed placeholders rather than exact character or float replicas.

Season themes are selected automatically from the local calendar month. Winter, spring, summer, and autumn currently have separate color palettes and parade decorations; the winter theme is the most developed in this build.

## Reference material

- Lotte World official winter-season announcement: https://www.youtube.com/watch?v=BgzsANrByC8
- 2026 winter parade report and seasonal details: https://www.kmib.co.kr/article/20261125502043

## Visual reference notes

Public reference photos were used to guide the visual language of the Adventure entrance clock-and-arch facade, the blue-ribbed glass dome, Magic Castle's pale masonry and blue roofs, the French Revolution indoor loop, the Magic Island coaster/gyro rides, the Spanish Pirate Ship, Pharaoh's Fury entrance, and the balloon attraction.

- Adventure entrance: https://ak-d.tripcdn.com/images/1mi0j224x98xf99dq6B37.jpg
- Magic Castle: https://cf.creatrip.com/original/spot/14619/0e2ync2pv1vojzfzowgy8ip5blg225kl.jpg
- French Revolution: https://shaunchng.com/photos/_data/i/upload/2023/05/21/20230521013551-2e51b3e3-me.jpg
- Spanish Pirate Ship: https://imagel.sekainavi.com/images/templates/SEOUL/1009385/dd8f89dd5eba2907_S.jpg
- Balloon Flight: https://res.klook.com/image/upload/fl_lossy.progressive/q_auto/f_auto/c_fill/blogen/5a165c5f-Lotte-World-Seoul-Theme-Park.jpg
- Official 2025 guide map: https://adventure.lotteworld.com/cmm/download.do?subPath=2025_Guidemap_eng.pdf

## Roadmap

1. Refine each remaining attraction using close-up, front/side/rear reference photographs.
2. Replace approximate footprints and coordinates with measured site-plan geometry where reliable measurements are available.
3. Build detailed interiors, themed facades, bridges, signage, landscaping, and lighting.
4. Expand ride-specific motion, queue logic, operating status, and guest simulation.

## Accuracy note

This is an early visual blockout, not a surveyed or dimensionally accurate reconstruction. Dimensions and positions are intentionally approximate and will be refined as reliable references are added. This is an unofficial fan-made project and is not affiliated with or endorsed by Lotte World or Lotte Corporation.
