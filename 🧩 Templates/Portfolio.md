---
type: portfolio
id: 
title: 
species: 
featured: false
photos: []
# photos:
#   - file: "📖 Field Journal/2026/2026-08-09 Kuala Selangor Eagle Feeding/WBSE_001.jpg"
#     trip_id: "2026-08-09-kuala-selangor-eagle-feeding"
#     date: 2026-08-09
#     rating: 5
#     caption: "Adult banking over mangrove"
#     focal_length_mm: 500
#     settings: "1/2000, f/7.1, ISO 800"
tags:
  - portfolio
created: {{date}}
updated: {{date}}
---

#  — Portfolio

> Set `title` and `species` to the species **common_name** (exact).

## Species note

```dataview
LIST
FROM "🐦 Species"
WHERE type = "species" AND common_name = this.species
```

## Selected frames

<!-- ![[📖 Field Journal/2026/.../WBSE_001.jpg]] -->

| File | Date | Rating | Caption |
|---|---|---|---|
| | | | |

## All trips with this species

```dataview
TABLE WITHOUT ID
  link(file.path, title) AS Trip,
  date AS Date,
  locations AS Locations,
  rating AS Rating
FROM "📖 Field Journal"
WHERE type = "trip" AND contains(species_observed, this.species)
SORT date DESC
```

## Curation notes

- Gaps / shots still wanted:
