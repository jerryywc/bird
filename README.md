# Bird — Obsidian Field Journal Vault

Trip-first vault for bird photography: every outing lives in its own folder; species and location pages summarise experience and **auto-reference** trips via Dataview.

## Open in Obsidian

1. Obsidian → **Open folder as vault** → select this `Bird` folder
2. Install community plugin **Dataview** (required for Home, Lists, Species, Location queries)
3. Optional: **Templater** (or enable core **Templates**) → template folder = `🧩 Templates`
4. Set startup note to `🏠 Home` if desired

## Workflow

1. Create `📖 Field Journal/YYYY/YYYY-MM-DD Title/`
2. Copy `🧩 Templates/Trip.md` → `Journal.md` in that folder
3. Export keeper JPEGs into the same folder (optional `GPS.gpx`)
4. Set `species_observed` and `locations` to **exact note titles** (strings)
5. Create Species / Location notes from templates when you meet something new
6. Curate Portfolio pages for published keepers

## Naming contracts (important)

| Field | Must match |
|---|---|
| Trip `species_observed` items | `🐦 Species` note `common_name` / filename |
| Trip `locations` items | `📍 Locations` note `name` / filename |
| Portfolio `species` | Species `common_name` |

These plain strings (not wikilinks in YAML) keep Dataview simple and stay portable for a future web app.

## Folder map

```
Bird/
├── 🏠 Home.md
├── 📖 Field Journal/YYYY/<date> Title/{Journal.md, *.jpg, GPS.gpx?}
├── 🐦 Species/
├── 📍 Locations/
├── 📸 Portfolio/
├── 📋 Lists/
├── 🧩 Templates/
├── ⚙️ Assets/
└── DATA_MODEL.md    ← schema for later app migration
```

## Sample data included

- Trips: `2026-08-09 Kuala Selangor Eagle Feeding`, `2026-08-16 KSNP`
- Species: WBSE, Brahminy Kite, Lesser Adjutant, Mangrove Pitta (target), Oriental Darter (wishlist)
- Locations: Eagle Feeding Spot, KSNP, Pantai Jeram (unvisited)
- Portfolio stubs for WBSE and Lesser Adjutant

Drop real JPEGs into the sample trip folders using the filenames referenced in each `Journal.md`.
