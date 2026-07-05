# Garage — FH6 Coverage Tracker

A single-file, offline-first companion app for **Forza Horizon 6** — track which cars you own for every Race Type × Class combination, keep tabs on your Super Wheelspin collection, and never again wonder "do I actually have a car for S1 Touge?"

No build step, no backend, no account. Open `index.html` in a browser and it works.

![version](https://img.shields.io/badge/version-1.13f2-2DE2D6?style=flat-square)

---

## Features

### 🚗 Garage
Add cars with their class, race type, and an optional note. Edit or delete any entry inline. Start typing a car's name and it autocompletes against a live-fetched Forza Horizon 6 car list, auto-filling the class for you.

### 📊 Dashboard
An animated, car-dashboard-styled overview:
- A central gauge showing overall coverage %, with a toggle for a per-race-type breakdown
- RPM and Fuel dials that idle, sweep, and animate on a working **ignition button**
- OIL / TEMP / BATT / BELT / BRAKE telltale lights that do a real bulb-check on startup, then settle into their resting state

### 🗺️ Coverage
A Race Type × Class grid, colour-coded by how many cars you have for each combination. Click any cell to see exactly which cars fill it.

### 🏜️ Dirt Routes
Static reference info on FH6's Horizon Open dirt/asphalt route mixes.

### 🎡 Super Wheelspins
A checklist of every Super Wheelspin-exclusive car, grouped by brand. Search, filter by Collected/Remaining, and use Check All / Uncheck All on the currently visible set.

### 💾 Import / Export
- **Export** your garage to a portable `.txt` (JSON) setup file
- **Import** a setup file from a friend — if it also contains Super Wheelspin data, you're asked before it overwrites your own (since that's account-specific)
- A setup can also be opened via a `#setup=...` share link

---

## Getting started

1. Download `index.html`.
2. Open it in any modern browser (Chrome, Firefox, Edge, Safari).
3. That's it — your data saves automatically to that browser's local storage.

To host it as a real site (so you have a stable link instead of a local file), drag-and-drop it onto [Netlify Drop](https://app.netlify.com/drop), or push it to a GitHub repo and enable **GitHub Pages** in Settings.

## A note on data

This app stores everything in your browser's `localStorage` — there is no server and no shared database. That means:

- Your garage is private to **your browser on your device**. Nobody else sees it, and you don't see anyone else's.
- If you and your friends deploy this together, each person gets their own empty garage — you share progress by sending each other exported setup files, not by looking at the same live data.
- Clearing your browser's site data will clear your garage. Export a backup occasionally if you've put real time into it.

## Tech

Plain HTML, CSS, and vanilla JavaScript — no framework, no build tools, no dependencies to install. Car name/class suggestions are fetched live from the [Forza Wiki](https://forza.fandom.com/wiki/Forza_Horizon_6/Cars); everything else works fully offline.

## Versioning

The build tag next to the title (e.g. `v1.13f2`) tracks changes made to this file:
- **Major** (`v1` → `v2`) — a significant rework
- **Minor** (`v1.13` → `v1.14`) — a new feature or meaningful addition
- **Fix** (`v1.13` → `v1.13f1` → `v1.13f2`) — bug fixes or cleanup with no new features; resets when the minor version bumps
