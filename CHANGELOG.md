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
- Sticky compact total bar, so the day total stays visible while scrolling
- Meal block stays open while picking (it used to jump to the next meal after the first tap)
- "Frokostblanding + varmt vann" (he uses hot water, not milk): 200/300/450 kcal
- "Ferdig ✓" button closes a meal and opens the next one
- Undo: "Angre" toast after every change
- Removed kcal ranges from untouched cards (kcal shows once a chip is picked)
- Favourites: within each meal, the foods he logged most in the previous 30 days come first (ties keep menu order; today's own taps never reorder the list)
- Menu trimmed to 5 meals: removed Før trening, Etter trening, Drikke and Boostere; added Etter skole (matboks, wrap, toast, egg, nøtter). "Annet" stays
- Portion guide: size hints under Liten/Vanlig/Stor (≈ 50/75/100 g dry oats, plate rule for dinner) and a "weigh your own bowls once" guide in the Meg tab
- Havregrøt matches the family's real bowls: Liten skål = 55 g dry oats (~300 kcal), Stor skål = 150 g (~650 kcal), oats go raw from the bag with hot water + jam; no middle size. Skolelunsj oats + nuts: 475 / 850
- Frokostblanding and yoghurt use the same two bowls (provisional gram/dl values); yoghurt split into "vanlig" and "Gresk"
- Design pass (from a UX critique): closed meals show what was logged ("Egg (3) · Havregrøt (Stor)"); status wording now follows the goal (Mer! / Nesten / Mål nådd at the goal, the ±500 zone is only the green band); week card counts days at/above the goal; plate guide shown once per meal; solid sticky bar with fade; "I dag" capitalisation fixed; bigger chip kcal text; nav active state no longer the same as "selected"; "1 dag logget"; empty-week hint; collapsible porsjonsguide
- Progress-ring app icon (SVG favicon + 180/512 PNG, maskable) and 6 themes in the Meg tab: Mørk, Lys, Matchday, Slate, Rød, Auto (follows the phone)
- Storage key changed to `simplecal.v2` (v1 data is not migrated; the menu ids changed)

## v1 — initial release

- Day view: date navigation, total vs. goal bar with zone band, 5 meal sections + boosters
- Portions: tap a checked card's chip to cycle ×1 → ×1.5 → ×2 → ×0.5
- Custom "Annet" kcal entries
- Week view: avg kcal/day, days in zone, bar per day, avg per meal
- Export / import JSON backup (merge by date)
