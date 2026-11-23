# SimpleCal

**TL;DR:** A single-file, mobile-first meal checklist for a young football player (target ~4000 kcal/day, zone 3500–4500). Tap what was eaten, see the day total, week average and days-in-zone. No backend, no build step. Data lives in `localStorage` with JSON export/import.

## Design principles

- **Under 10 seconds per day.** One tap per meal item; no typing unless adding a custom "Annet" kcal entry.
- **Big targets.** Two-column card grid, 92px tall cards, thumb-reach bottom nav.
- **Zone, not perfection.** The goal is 3500–4500 kcal over time, shown as a green band, not a pass/fail score.
- **Dad edits the menu, son only ticks.** All meals, kcal values and goals live in the `CONFIG` block at the top of the script in `index.html`.

## Features (v1)

| Area | What it does |
|---|---|
| Day view | Date navigation, total vs. goal bar with zone band, 5 meal sections + boosters |
| Portions | Tap a checked card's chip to cycle ×1 → ×1.5 → ×2 → ×0.5 |
| Custom | "Annet": add any kcal amount to the day |
| Week view | Avg kcal/day, days in zone, bar per day (tap to open), avg per meal |
| Backup | Export / import JSON (merge by date) |

## Data model

```json
{ "days": { "2026-11-23": { "items": { "b1": 1, "d3": 1.5 }, "extra": [300] } } }
```

Item ids map to the `SECTIONS` config. kcal is computed at read time, so changing a kcal value in the config also changes history.

## Deploy (GitHub Pages)

1. Create the repo `simplecal`, add `index.html` + `README.md`, push to `main`.
2. Repo → Settings → Pages → Source: `main` / root.
3. Open `https://<user>.github.io/simplecal/` on the phone → Share → **Add to Home Screen**.

## Roadmap ideas

- PWA manifest + service worker (offline, proper app icon)
- Weight/energy/sleep quick-rating per day
- Editable menu in the UI instead of the config block
- Optional protein estimate per item
- Shared sync between son's and dad's phone (e.g. Cloudflare KV)
