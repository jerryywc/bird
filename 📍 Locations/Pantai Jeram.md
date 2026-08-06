---
type: location
id: pantai-jeram
name: Pantai Jeram
region: Selangor
country: Malaysia
coordinates:
  lat: 3.2240
  lon: 101.3050
habitat:
  - beach
  - coastal
  - mudflat
access: public
best_season: Migration season for shorebirds
best_tide: Low to mid tide
visited: false
first_visit: 
last_visit: 
rating: 
tags:
  - location
  - shorebirds
created: 2026-08-06
updated: 2026-08-06
---

# Pantai Jeram

## Overview

Coastal stretch west of KL — on the radar for shorebirds and coastal raptors. Not yet visited; placeholder for planning.

## Habitat & access

| | |
|---|---|
| **Region** | Selangor |
| **Habitat** | Beach / coastal mud |
| **Access** | Public |
| **Best season** | Migration |
| **Best tide** | Low–mid |

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

- Scout parking and walk-in paths before peak heat
- Watch heat haze on long lenses midday

## Photography notes

-
