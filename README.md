# SimpleCal

**TL;DR:** A single-file, mobile-first meal checklist for a young football player (target ~4000 kcal/day, zone 3500–4500). Tap what was eaten, see the day total, week average and days-in-zone. No backend, no build step. Data lives in `localStorage` with JSON export/import.

## Design principles

- **Under 10 seconds per day.** One tap per food; no typing unless adding a custom "Annet" kcal entry.
- **Big targets.** Full-width cards with 48px chips, thumb-reach bottom nav.
- **Zone, not perfection.** The goal is 3500–4500 kcal over time, shown as a green band, not a pass/fail score.
- **Dad edits the menu, son only ticks.** All meals and kcal values live in the `CONFIG` block at the top of the script in `index.html`.

## Features

| Area | What it does |
|---|---|
| Day view | Date navigation, total vs. goal bar, 8 collapsible meal blocks in day order |
| Portions | Chips on each card: numbers (`2 3 4 5`) for countable foods, `Liten / Vanlig / Stor` for plate meals. Tap again to remove |
| Shortcuts | Most-logged foods float to the top of each meal; "↻ Som i går" copies yesterday's choices for a meal; "Annet" adds any kcal |
| Status | Mer! / Nesten / Mål nådd, plus "Mangler ca X kcal" |
| Week view | Avg kcal/day, days with goal reached, bar per day (tap to open), avg per meal |
| Profile | Name and daily goal (zone = goal ±500) |
| Backup | Export / import JSON (merge by date), wipe all data |
| Offline | Service worker + manifest + iPhone home-screen icon |

## Data model

```json
{ "profile": { "name": "", "goal": 4000 },
  "days": { "2026-11-23": { "items": { "b_brod": "4", "d_kyl": "Stor" }, "extra": [300] } } }
```

Item ids map to the `SECTIONS` config; the value is the chip label that was picked. kcal is computed at read time, so changing a kcal value in the config also changes history. Data stays in the browser's `localStorage` (key `simplecal.v2`) — no account, no server.

## Deploy (GitHub Pages)

1. Push all files (`index.html`, `sw.js`, `manifest.webmanifest`, icons) to `main`.
2. Repo → Settings → Pages → Source: `main` / root.
3. Open `https://<user>.github.io/simplecal/` on the phone → Share → **Add to Home Screen**.

## Planning

See [ROADMAP.md](ROADMAP.md) (someday ideas), [BACKLOG.md](BACKLOG.md) (active todo) and [CHANGELOG.md](CHANGELOG.md) (history).

## License

All rights reserved © 2026 nobody174. Free to use the app; please don't copy, modify or redistribute the code without asking.
