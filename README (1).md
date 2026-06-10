# Smashville Hockey Ops — Analytics Suite

An interactive hockey-operations analytics tool built around the Nashville Predators' real situation heading into the 2026 NHL Draft: the #10 overall pick, a cap sheet carrying several underwater contracts, and a draft-first mandate under new GM Chris MacFarland.

**[▶ Live demo](https://benmccurry.github.io/preds-analytics-suite/)** · click **"Take a tour"** in the top bar for a 2-minute guided walkthrough.

---

## What it is

A single, self-contained web app (one HTML file, no install) with eleven linked modules that move the way a front office actually works: **define an identity → evaluate players → run the draft → forecast the roster five years out.**

### Highlights
- **Roster & Cap** — contract-efficiency ledger ranking every deal by surplus value (production vs. pay).
- **Player Value model** — an undervaluation engine surfacing buy-low targets.
- **Scouting Tree** — a live projection workbench: drag attribute sliders and the outcome tiers, comps, risk, and confidence band recompute instantly.
- **Mock Draft** — the real 2026 prospect board with a GM-definable "Smashville Way" fit engine, a full 7-round draft simulator, and **1,000-run Monte Carlo** pick-availability modeling.
- **Model Lab** — the projection engine made transparent: feature contributions, calibration, Bayesian updating, and development curves. Every number can show its own formula.
- **Future Lineup** — a drag-and-drop depth chart with five-year tabs; contracts expire and prospects arrive on schedule.
- **The Brief** — a printable one-page summary.

## Design principle

Every projection is shown as a **range with explicit confidence**, never a lone number. We can't be certain — but we can quantify how confident we are, and the model sharpens as data accrues. Hover any **ⓘ** icon to see exactly how a metric is calculated.

## Data & honesty note

Player names, positions, cap hits, contract terms, the farm system, and the 2026 draft order are **real** (per public sources as of early 2026). Advanced metrics (Value Scores, fit, projections) and the calibration data are **modeled/synthetic** to demonstrate the architecture — in a production deployment these weights are fit on real historical outcomes, and the interface doesn't change. This is disclosed throughout the app.

## Tech

Plain HTML, CSS, and vanilla JavaScript in a single file. No build step, no dependencies to install. Visualizations are hand-built SVG; PNG export uses [html2canvas](https://html2canvas.hertzen.com/).

> Note: the optional "AI Architect" module calls a live language-model API and only functions in an environment with that access configured; it is inert on a static host.

## Run it locally

Download `preds-analytics-suite.html` and double-click it — it opens in any modern browser. That's the whole setup.

---

*Built as an independent analytics portfolio project. Not affiliated with or endorsed by the Nashville Predators or the NHL.*
