# AUTOFACTORY — 3D Car Factory Line

A single-page Three.js visualization of a car factory line, from raw materials to finished cars driving off the end.

**Live site:** https://earino.github.io/car-factory-3d/

## What it shows

One continuous conveyor line, left to right:

1. **Raw materials** — steel coils, panel stacks, crates and barrels staged beside the line
2. **FRAME** gantry — bare body shell enters the line
3. **BODY** gantry — welded silver body
4. **PAINT** shop — translucent enclosure with spray mist; cars transition from silver to their bright color
5. **ASSEMBLY** gantry — wheels scale in and headlights brighten
6. **CHECK** gantry — final inspection glow, then the car drives off onto an elevated road

A roof-mounted crane slides back and forth over the line; dust drifts through the hall; a live counter tracks produced cars.

## Controls

- Drag to orbit · scroll (or pinch) to zoom — auto-orbit resumes on reset view
- Play / pause button freezes the line
- Speed slider: 0.25×–3×
- Reset view restores the default camera angle

## Tech

Single `index.html` (inline CSS/JS) + Three.js vendored in `vendor/` — no build step, no dependencies to install. Served as static files from GitHub Pages.

## Run locally

```sh
python3 -m http.server 8765
# open http://localhost:8765/index.html
```

Note: the page uses ES modules, so it must be served over HTTP(S) — opening `index.html` directly from disk will not work.
