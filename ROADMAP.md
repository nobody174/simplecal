# SimpleCal — Roadmap

Future and unscoped ideas ("someday"), plus locked design decisions. Active work lives in [BACKLOG.md](BACKLOG.md); shipped work in [CHANGELOG.md](CHANGELOG.md).

## Someday ideas

- Weight/energy/sleep quick-rating per day
- Editable menu in the UI instead of the config block
- Optional protein estimate per item
- Cross-device sync / login so data follows the user to a laptop (Supabase or Firebase; sync-code or email login). Adults only, GDPR note + delete-account needed. Decided 2026-11-23: local-first for v1.

## Locked design decisions

- Single `index.html` (+ small sw.js/manifest), no backend, no build step.
- Data in `localStorage` with JSON export/import (merge by date).
- Zone (3500–4500 kcal), not pass/fail.
- Dad edits the menu via the `CONFIG` block; son only ticks.
- Portions are chips, not multipliers (numbers for countables, Liten/Vanlig/Stor for plates).
- No banana, no orange (allergy).
- kcal computed at read time (editing config kcal changes history).
