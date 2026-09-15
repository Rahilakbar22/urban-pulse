# Urban Pulse

An interactive dashboard exploring how a fictional city — **Meridian Bay** — grows district by district. Built as a single self-contained page: vanilla HTML, CSS and JavaScript, no frameworks, no build step.

**Live demo** — enable GitHub Pages on this repo (Settings → Pages → Deploy from branch `main` / `root`) and the link goes here.

## What it does

- **Population growth chart** — an SVG line/area chart of Meridian Bay's population from 2016–2026, with a hover crosshair and tooltip on every year.
- **District map** — a 6×4 grid of 24 districts, each colored by type (residential, commercial, park & green, transit hub, mixed-use). Click any block to see its population, walkability score, and green coverage, plus a short fact about that kind of urban space.
- **Filters** — filter the map by district type without losing the rest of the map for context (non-matching blocks dim rather than disappear).
- **Summary stat tiles** — total population, average walkability, green coverage, and 10-year growth, computed live from the district data.
- **Light / dark mode** — a manual toggle that respects the system default on first load and remembers your choice.

## Why it's built this way

- **No dependencies to install.** Open `index.html` in a browser and it works — nothing to `npm install`, no bundler.
- **Data-viz best practices.** The categorical palette (five district types) and the chart's single blue series are both checked for colorblind-safe contrast — legends are always paired with visible labels, never color alone.
- **Accessible by default.** District blocks and filters are real buttons (keyboard-operable, with `aria-pressed` / `aria-label`), and the chart has a text alternative via `aria-label`.

## Run it locally

No build step — just open the file:

```bash
git clone https://github.com/Rahilakbar22/urban-pulse.git
cd urban-pulse
open index.html   # or just double-click it
```

## Tech

HTML5, CSS custom properties (for the light/dark theme), and vanilla JavaScript. Font: Inter via Google Fonts.

## Notes

Meridian Bay and all of its district names and figures are fictional — built to demonstrate the interaction design, not to represent a real place.

## License

MIT — see [LICENSE](./LICENSE).

