---
type: portfolio
id: portfolio-blue-tailed-bee-eater
title: Blue-tailed Bee Eater
species: Blue-tailed Bee Eater
featured: false
photos:
  - file: "📖 Field Journal/2023/2023-02-18 Kota Kemuning Wetland/DSC00668.jpg"
    trip_id: 2023-02-18-kota-kemuning-wetland
    date: 2023-02-18
    rating: 5
    caption: "Perched at wetland edge — first record"
tags:
  - portfolio
  - bee-eater
created: 2023-02-18
updated: 2026-08-06
---

# Blue-tailed Bee Eater — Portfolio

## Species note

```dataview
LIST
FROM "🐦 Species"
WHERE type = "species" AND common_name = this.species
```

## Selected frames

![[📖 Field Journal/2023/2023-02-18 Kota Kemuning Wetland/DSC00668.jpg]]

| File | Date | Rating | Caption |
|---|---|---|---|
| DSC00668.jpg | 2023-02-18 | 5 | Perched at wetland edge — first record |

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

- Gaps / shots still wanted: flight with blue tail showing, insect sally, closer portrait, side-by-side with Blue-throated Bee-eater for ID reference
