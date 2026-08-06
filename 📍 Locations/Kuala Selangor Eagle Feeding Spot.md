---
type: location
id: kuala-selangor-eagle-feeding-spot
name: Kuala Selangor Eagle Feeding Spot
region: Selangor
country: Malaysia
coordinates:
  lat: 3.3405
  lon: 101.2512
habitat:
  - estuary
  - mangrove
  - open water
access: public
best_season: Year-round
best_tide: Rising / mid — boats usually run on schedule
visited: true
first_visit: 2026-08-09
last_visit: 2026-08-09
rating: 5
tags:
  - location
  - raptors
created: 2026-08-09
updated: 2026-08-09
---

# Kuala Selangor Eagle Feeding Spot

## Overview

Boat-based feeding sessions for White-bellied Sea Eagles and Brahminy Kites. Action is dense and predictable — ideal for flight practice and keeper frames.

## Habitat & access

| | |
|---|---|
| **Region** | Selangor |
| **Habitat** | Estuary / mangrove edge |
| **Access** | Public (boat operators) |
| **Best season** | Year-round |
| **Best tide** | Check operator schedule |

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

- Arrive early for check-in and lens setup on the jetty
- Protect gear from spray; keep a dry cloth handy
- Pick a shooting lane and commit — don't chase every bird

## Photography notes

- Back-button AF + high continuous burst
- Expose for whites on adult WBSE undersides
- Occasional otters near banks — worth a second body or quick flip to wider zoom
