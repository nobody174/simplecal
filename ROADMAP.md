# SimpleCal — Roadmap

Future and unscoped ideas ("someday"), plus locked design decisions. Active work lives in [BACKLOG.md](BACKLOG.md); shipped work in [CHANGELOG.md](CHANGELOG.md).

## Someday ideas

- PWA manifest + service worker (offline, proper app icon)
- Weight/energy/sleep quick-rating per day
- Editable menu in the UI instead of the config block
- Optional protein estimate per item
- Shared sync between son's and dad's phone (e.g. Cloudflare KV)

## Locked design decisions

- Single `index.html`, no backend, no build step.
- Data in `localStorage` with JSON export/import (merge by date).
- Zone (3500–4500 kcal), not pass/fail.
- Dad edits the menu via the `CONFIG` block; son only ticks.
- kcal computed at read time (editing config kcal changes history).
