# Garage — FH6 Coverage Tracker

A single-file, offline-first companion app for **Forza Horizon 6**. It helps you track which cars you own for every Race Type × Class combination, and keep tabs on your Super Wheelspin collection — so you're not stuck guessing whether you actually have a car ready for, say, S1 Touge.

No build step, no backend, no account. Open `index.html` in a browser and it works.

## Getting started

1. Download `index.html`.
2. Open it in any modern browser.
3. That's it — your data saves automatically to that browser's local storage.

To host it as a real site (so you have a stable link instead of a local file), drag-and-drop it onto [Netlify Drop](https://app.netlify.com/drop), or push it to a GitHub repo and enable **GitHub Pages** in Settings.

## A note on data

This app stores everything in your browser's `localStorage` — there is no server and no shared database. That means:

- Your garage is private to **your browser on your device**. Nobody else sees it, and you don't see anyone else's.
- If you and your friends deploy this together, each person gets their own empty garage — you share progress by sending each other exported setup files, not by looking at the same live data.
- Clearing your browser's site data will clear your garage. Export a backup occasionally if you've put real time into it.

## Tech

Plain HTML, CSS, and vanilla JavaScript — no framework, no build tools, no dependencies to install. Car name/class suggestions are fetched live from the Forza Wiki; everything else works fully offline.
