# SimpleCal — Changelog

Authoritative history of what has shipped.

## v2 — chips redesign

- Replaced the ×1/×1.5/×2 portion cycling with chips on every card: number chips (`2 3 4 5`) for countable foods, `Liten / Vanlig / Stor` for plate meals
- New menu: 8 blocks in day order (Frokost, Skolelunsj, Før trening, Etter trening, Middag, Kveldsmat, Drikke, Boostere), no banana/orange
- Collapsible meal blocks (first empty one opens automatically), kcal + tick per block
- "↻ Som i går" per meal, and "Nullstill" per meal
- Simple status: Mer! / Nesten / Mål nådd, plus "Mangler ca X kcal"
- Local profile (name, daily goal); zone = goal ±500
- Backup (export/import/wipe) moved to the "Meg" tab
- Offline support (service worker) + web manifest + iPhone home-screen icon
- Storage key changed to `simplecal.v2` (v1 data is not migrated; the menu ids changed)

## v1 — initial release

- Day view: date navigation, total vs. goal bar with zone band, 5 meal sections + boosters
- Portions: tap a checked card's chip to cycle ×1 → ×1.5 → ×2 → ×0.5
- Custom "Annet" kcal entries
- Week view: avg kcal/day, days in zone, bar per day, avg per meal
- Export / import JSON backup (merge by date)
