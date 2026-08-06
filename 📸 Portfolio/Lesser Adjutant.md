---
type: portfolio
id: portfolio-lesser-adjutant
title: Lesser Adjutant
species: Lesser Adjutant
featured: true
photos: []
tags:
  - portfolio
  - stork
created: 2026-08-16
updated: 2026-08-16
---

# Lesser Adjutant — Portfolio

Featured frames of **Lesser Adjutant**.

## Species note

```dataview
LIST
FROM "🐦 Species"
WHERE type = "species" AND common_name = this.species
```

## Selected frames

*Awaiting export from [[📖 Field Journal/2026/2026-08-16 KSNP/Journal|2026-08-16 KSNP]].*

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

- Why these frames made the cut: —
- Gaps / shots still wanted: closer foraging sequence, flight departure
