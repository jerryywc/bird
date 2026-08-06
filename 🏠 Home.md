---
type: home
title: Bird Photography Dashboard
updated: 2026-08-06
tags:
  - dashboard
  - home
---

# 🏠 Bird Photography

Personal field journal, species notes, locations, and portfolio — trip-first.

## Quick links

| | | |
|---|---|---|
| [[📋 Lists/Life List\|Life List]] | [[📋 Lists/Target Species\|Targets]] | [[📋 Lists/Wish List\|Wish List]] |
| [[📋 Lists/Locations Visited\|Locations Visited]] | [[🐦 Species/Overview\|Species]] | [[📍 Locations/Overview\|Locations]] |
| [[📖 Field Journal/Overview\|Field Journal]] | [[📸 Portfolio/Overview\|Portfolio]] | [[🧩 Templates]] |

---

## Recent trips

```dataview
TABLE WITHOUT ID
  link(file.path, title) AS Trip,
  date AS Date,
  locations AS Locations,
  length(species_observed) AS Species,
  rating AS Rating
FROM "📖 Field Journal"
WHERE type = "trip"
SORT date DESC
LIMIT 10
```

---

## Stats

```dataview
TABLE WITHOUT ID
  length(rows) AS "Trips logged"
FROM "📖 Field Journal"
WHERE type = "trip"
GROUP BY true
```

```dataview
TABLE WITHOUT ID
  length(rows) AS "Species on life list"
FROM "🐦 Species"
WHERE type = "species" AND life_list = true
GROUP BY true
```

```dataview
TABLE WITHOUT ID
  length(rows) AS "Locations visited"
FROM "📍 Locations"
WHERE type = "location" AND visited = true
GROUP BY true
```

---

## Target species

```dataview
TABLE WITHOUT ID
  link(file.link, common_name) AS Species,
  scientific_name AS "Scientific name",
  malaysia_status AS Status
FROM "🐦 Species"
WHERE type = "species" AND target = true
SORT common_name ASC
```

---

## Wish list

```dataview
TABLE WITHOUT ID
  link(file.link, common_name) AS Species,
  scientific_name AS "Scientific name"
FROM "🐦 Species"
WHERE type = "species" AND wishlist = true
SORT common_name ASC
```

---

## Featured portfolio

```dataview
TABLE WITHOUT ID
  link(file.link, title) AS Portfolio,
  species AS Species,
  featured AS Featured
FROM "📸 Portfolio"
WHERE type = "portfolio" AND featured = true
SORT title ASC
```

---

## How this vault works

1. **Every outing starts as a trip folder** under `📖 Field Journal/YYYY/YYYY-MM-DD Title/`
2. Drop exported JPEGs next to `Journal.md` (optional `GPS.gpx`)
3. Fill `species_observed` and `locations` in trip frontmatter using exact note titles
4. Species and Location pages **auto-pull** matching trips via Dataview
5. Curate keepers on Portfolio pages; Lists stay query-driven

> New note? Use templates in `🧩 Templates/` (Templater / core Templates).
