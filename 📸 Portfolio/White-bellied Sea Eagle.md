---
type: portfolio
id: portfolio-white-bellied-sea-eagle
title: White-bellied Sea Eagle
species: White-bellied Sea Eagle
featured: true
photos:
  - file: "📖 Field Journal/2026/2026-08-09 Kuala Selangor Eagle Feeding/WBSE_001.jpg"
    trip_id: 2026-08-09-kuala-selangor-eagle-feeding
    date: 2026-08-09
    rating: 5
    caption: "Adult banking over mangrove after a near-miss stoop"
    focal_length_mm: 500
    settings: "1/2500, f/7.1, ISO 800"
  - file: "📖 Field Journal/2026/2026-08-09 Kuala Selangor Eagle Feeding/WBSE_002.jpg"
    trip_id: 2026-08-09-kuala-selangor-eagle-feeding
    date: 2026-08-09
    rating: 4
    caption: "Juvenile circling — useful ID reference frame"
    focal_length_mm: 400
    settings: "1/2000, f/7.1, ISO 1000"
tags:
  - portfolio
  - raptor
created: 2026-08-09
updated: 2026-08-09
---

# White-bellied Sea Eagle — Portfolio

Featured frames of **White-bellied Sea Eagle**.

## Species note

```dataview
LIST
FROM "🐦 Species"
WHERE type = "species" AND common_name = this.species
```

## Selected frames

<!-- Embed after JPEGs are exported into the trip folder -->
<!-- ![[📖 Field Journal/2026/2026-08-09 Kuala Selangor Eagle Feeding/WBSE_001.jpg]] -->
<!-- ![[📖 Field Journal/2026/2026-08-09 Kuala Selangor Eagle Feeding/WBSE_002.jpg]] -->

| File | Date | Rating | Caption |
|---|---|---|---|
| WBSE_001.jpg | 2026-08-09 | 5 | Adult banking over mangrove |
| WBSE_002.jpg | 2026-08-09 | 4 | Juvenile circling |

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

- Why these frames made the cut: clean wing shape, readable eye, mangrove context
- Gaps / shots still wanted: fish-in-talons moment, eye-level perch portrait
