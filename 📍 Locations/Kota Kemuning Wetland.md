---
type: location
id: kkwetland
name: Kota Kemuning Wetland
region: "Selangor"
country: Malaysia
coordinates:
  lat: 
  lon: 
habitat: [wetland]
access: "public"
best_season: "Year-round"
best_tide: ""
visited: true
first_visit: 
last_visit: 
rating: 3
tags:
  - wetland
created: {{date}}
updated: {{date}}
---

# 

> Fill `name` to match this note’s title exactly (join key for trips).

## Overview

5 minutes drive from home. Tightly connected to housing area.

## Habitat & access

| | |
|---|---|
| **Region** | `= this.region` |
| **Habitat** | `= this.habitat` |
| **Access** | `= this.access` |
| **Best season** | `= this.best_season` |
| **Best tide** | `= this.best_tide` |

## Coordinates

- Lat: `= this.coordinates.lat`
- Lon: `= this.coordinates.lon`

## Species typically seen here

```dataview
TABLE WITHOUT ID
  rows.species_observed AS Species
FROM "📖 Field Journal"
WHERE type = "trip" AND contains(locations, this.name)
FLATTEN species_observed
GROUP BY true
```

## Visits

```dataview
TABLE WITHOUT ID
  link(file.path, title) AS Trip,
  date AS Date,
  species_observed AS Species,
  rating AS Rating,
  weather AS Weather
FROM "📖 Field Journal"
WHERE type = "trip" AND contains(locations, this.name)
SORT date DESC
```

## Visit count

```dataview
TABLE WITHOUT ID
  length(rows) AS Visits
FROM "📖 Field Journal"
WHERE type = "trip" AND contains(locations, this.name)
GROUP BY true
```

## Field tips

-

## Photography notes

-
