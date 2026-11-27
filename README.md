# Lotte World Simulator

A browser-based, walkable 3D reconstruction prototype of Lotte World Adventure and Magic Island, rebuilt from user-supplied interior photographs and publicly available guide-map references.

## Current build

- Long barrel-vault glass roof with repeated transverse steel arches, longitudinal purlins, glass panes, side aprons, and tall structural columns
- Multi-level oval atrium galleries, inner and outer railings, balusters, support piers, and broad circulation promenade
- Central 30 × 60 m ice-rink footprint, ice surface, perimeter boards, railings, and suspended circular lighting rig
- Photo-inspired themed village facades: grand European-style palace frontage, half-timber houses, colored roofs, arched shop windows, rockwork backdrop, palm trees, and balloon-shaped lanterns
- Magic Island landform, Seokchon Lake, stone approach bridge, and pastel Magic Castle with blue conical turrets, arched windows, trim, and finials
- Separate procedural attraction models and animated motion for carousel, pirate ship, gyro rides, coaster loops, water rides, balloon flight, teacups, bumper cars, children’s rides, and themed dark rides
- Explicit track geometry and path-following vehicles for Atlantis, French Revolution, World Monorail, and water-ride routes
- 63 anonymous animated guest figures across the rink, promenades, and galleries, including walkers, idle spectators, phone-photo gestures, and skaters; the player avatar is also a rigged multi-part human figure
- Restaurant and shop storefronts with separate wall palettes, glazing, awnings, tables, and sign panels
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

The scene is a photo-matched approximation rather than a surveyed or CAD-accurate replica. The four user-supplied photographs establish the interior roof, central ice rink, circular galleries, themed village, tropical details, and crowd scale. Public guide-map information confirms facility names and general floor groupings. The published isometric map is used to trace relative placement, not to claim exact building coordinates or walkway widths. Exact coordinates, clearances, structural dimensions, and every ride's track centerline require measured plans or additional multi-angle reference views. Guest figures are anonymous animated visitors, not copied identities of people in the photographs.


## Map coordinates and ride motion

The current attraction catalog follows the 2026 Korean guide-map names and floor groupings. The relative positions are manually traced from publicly available isometric guide-map artwork and anchored around the entrance, bridge, island shoreline, and 30 × 60 m ice rink. These are local simulation coordinates, not surveyed metre coordinates, GPS positions, or CAD measurements. A measured architectural floor plan is still required to claim exact clearances and facility coordinates.

Ride values currently shown in the simulator:
- **Atlantis:** 670 m track, 75 km/h maximum, 22 m height, 72° steep section, 8-seat boat, and approximately 108 seconds from the cited coaster database references. Its 3D route is a photo/map-informed approximation; the vehicle follows that route using a 670 m display-distance profile.
- **French Revolution:** approximately 630 m, 70 km/h maximum, 28 m height, one 360° inversion, and 105 seconds from Coaster.cloud. Its modeled path contains a chain lift, vertical loop, and a 540° horizontal helix; exact track centerline and intermediate speed trace are not publicly measured.
- **Gyro Swing:** 27 m attraction height, 32 m top height, 96° maximum swing angle, 83 km/h listed maximum, 40 riders, and about 100 seconds from a secondary published reference. Its amplitude envelope and time-by-time speed are simulated approximations.
- **Gyro Drop:** 70 m tower and 100 km/h listed maximum from the official guide map. The cycle length and acceleration profile are simulator estimates, not a published operating telemetry trace.

Boarding clones the facility vehicle, places the visitor in its seat area, moves the vehicle along the modeled track or ride motion, follows it with the camera, and displays current speed, progress, and elapsed time. For rides without published speed/duration data, the card explicitly identifies their motion as a simulation estimate.

## Parade behavior

The simulator uses a ten-minute real-time interval measured from page load. Each parade procession lasts about 110 seconds and has a manual preview button. This interval is intentionally a simulator rule, not a recreation of the park's published show timetable. The current winter theme is based on Lotte World's 2026 winter season announcement; the parade floats are original generic winter-themed placeholders rather than exact character or float replicas.

Season themes are selected automatically from the local calendar month. Winter, spring, summer, and autumn currently have separate color palettes and parade decorations; the winter theme is the most developed in this build.

## Reference material

- Lotte World official winter-season announcement: https://www.youtube.com/watch?v=BgzsANrByC8
- 2026 winter parade report and seasonal details: https://www.kmib.co.kr/article/20261125502043

## Visual reference notes

The four supplied interior photographs were used as the primary references for the long glazed barrel roof, repeating arch frames, central ice rink, oval gallery railings, pastel village facades, palm trees, balloon lanterns, and guest density. Additional public references were used for ride families and the official guide-map facility groupings.

- Adventure entrance: https://ak-d.tripcdn.com/images/1mi0j224x98xf99dq6B37.jpg
- Magic Castle: https://cf.creatrip.com/original/spot/14619/0e2ync2pv1vojzfzowgy8ip5blg225kl.jpg
- French Revolution: https://shaunchng.com/photos/_data/i/upload/2023/05/21/20230521013551-2e51b3e3-me.jpg
- Spanish Pirate Ship: https://imagel.sekainavi.com/images/templates/SEOUL/1009385/dd8f89dd5eba2907_S.jpg
- Balloon Flight: https://res.klook.com/image/upload/fl_lossy.progressive/q_auto/f_auto/c_fill/blogen/5a165c5f-Lotte-World-Seoul-Theme-Park.jpg
- Official 2025 guide map: https://adventure.lotteworld.com/cmm/download.do?subPath=2025_Guidemap_eng.pdf
- 2026 Korean guide-map listing: https://www.scribd.com/document/1072853286/2026-%EB%A1%AF%EB%8D%B0%EC%9B%94%EB%93%9C-%EA%B0%80%EC%9D%B4%EB%93%9C%EB%A7%B5-%EA%B5%AD%EB%AC%B8
- Published isometric map artwork used only for relative placement tracing: https://javamilk.com/img/kr-lotte-world-adventure-guide-map.pdf
- Atlantis ride data: https://coasterpedia.net/wiki/Atlantis_Adventure
- French Revolution ride data: https://data.coaster.cloud/en/attractions/49eeee89-french-revolution-hulenchilebollusyeon

## Roadmap

1. Replace approximate facility coordinates with measured floor-plan positions and verify walkway widths and clearances.
2. Trace each remaining ride's full track centerline, elevation profile, bank angle, supports, station, and vehicle direction from multi-angle references.
3. Refine building proportions, storefront ornament, interior materials, roof panel dimensions, and gallery balustrades.
4. Expand guest behavior with collision avoidance, groups, queues, ice-skating paths, and attraction-specific boarding/exit choreography.

## Accuracy note

This is an early visual blockout, not a surveyed or dimensionally accurate reconstruction. Dimensions and positions are intentionally approximate and will be refined as reliable references are added. This is an unofficial fan-made project and is not affiliated with or endorsed by Lotte World or Lotte Corporation.
