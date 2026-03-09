# Lobito-korridoren: Scrollytelling Map

Interactive scrollytelling story about the Lobito Corridor and the geopolitics of critical minerals in Central Africa. Built with [MapLibre GL JS](https://maplibre.org/) and [Scrollama](https://github.com/russellsamora/scrollama).

## Quick start

The app is a static HTML page that fetches GeoJSON data via `fetch()`, so it needs a local HTTP server (opening `index.html` directly via `file://` won't work due to CORS).

**Python (simplest):**

```bash
cd scrollama
python3 -m http.server 8000
```

Then open [http://localhost:8000](http://localhost:8000).

**Node:**

```bash
npx serve scrollama
```

**VS Code:** Right-click `index.html` → "Open with Live Server" (requires the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension).

## Project structure

```
scrollama/
├── index.html              # Single-page app (HTML + CSS + JS)
└── data/
    ├── cities.geojson
    ├── copper_tracts.geojson
    ├── corridor_line.geojson
    ├── countries.geojson
    ├── european_destinations.geojson
    ├── facilities_ownership.geojson
    ├── maus_polygons.geojson
    ├── railway.geojson
    └── supply_chains.geojson
```

## Data sources

- **Mine polygons:** Maus et al. (2022) Global Mining Polygons
- **Facilities & ownership:** USGS Africa Mineral Industries Geodatabase
- **Copper tracts:** USGS mineral resource assessments
- **Railway:** USGS Africa GIS Transport layer
- **Cities:** Natural Earth 10m Populated Places
- **Supply chains & European destinations:** Manually compiled from known trade routes
