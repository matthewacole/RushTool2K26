# TIFF 26 Planner

A single-file, no-build, offline-capable web app for planning a trip to the Toronto
International Film Festival (TIFF) 2026 (Sep 10–20). Everything lives in one HTML file —
open `index.html` in a browser or deploy it to GitHub Pages as-is.

Forked from the original TIFF 2026 Rush Scheduler (CSV + PowerShell generator) into a
modern single-file web app.

## Features

- Browse all 244 films, mark favorites (♥), and filter by category/search
- Build a per-day screening schedule with conflict detection
- Projected **rush (walk-up) odds %** for every public screening, with a plain-English
  factor breakdown, per-tier advice, and same-venue alternates later in the day
- Weather forecast per screening time (Open-Meteo; falls back to last-year/typical data)
- Export/import favorites as JSON
- Fully responsive (desktop / tablet / mobile)

## Rush model

`pct = clamp(53 + Σ factors, 5, 95)` where factors include premiere status, Cannes
selection, niche-program boosts, live interest, star power, awards-contender status,
number/later-index of public showings, venue rush-seat pool, evening screening,
non-English dialogue, and weather.

## Deploy

This is a static site — point GitHub Pages at the `main` branch of this repo and it
serves `index.html`. No build step required.
