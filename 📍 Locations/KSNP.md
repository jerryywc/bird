---
type: location
id: ksnp
name: KSNP
region: Selangor
country: Malaysia
coordinates:
  lat: 3.3380
  lon: 101.3040
habitat:
  - mangrove
  - mudflat
  - boardwalk
access: public
best_season: Year-round (migrant boost Aug–Apr)
best_tide: Low tide for mudflat waders and storks
visited: true
first_visit: 2026-08-16
last_visit: 2026-08-16
rating: 4
tags:
  - location
  - mangrove
aliases:
  - Kuala Selangor Nature Park
created: 2026-08-16
updated: 2026-08-16
---

# KSNP

**Kuala Selangor Nature Park**

## Overview

Mangrove boardwalks, hide, and coastal mudflats. Quieter than the eagle boats — better for storks, pittas (target), and habitat storytelling shots.

## Habitat & access

| | |
|---|---|
| **Region** | Selangor |
| **Habitat** | Mangrove / mudflat |
| **Access** | Public (park entry) |
| **Best season** | Year-round; migrants Aug–Apr |
| **Best tide** | Low tide |

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

- Walk slowly on boardwalks — pitta country
- Check mudflats from the coastal edge at low tide
- Mosquitoes after rain; bring repellent

## Photography notes

- Lower ISO in dense canopy; watch for mottled light
- Bring a beanbag for hide rails
