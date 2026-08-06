---
type: list
title: Locations Visited
updated: 2026-08-06
tags:
  - list
  - locations
---

# Locations Visited

Sites marked `visited: true`, with auto-counted trips.

```dataview
TABLE WITHOUT ID
  link(file.link, name) AS Location,
  region AS Region,
  rating AS Rating,
  first_visit AS "First visit",
  last_visit AS "Last visit"
FROM "📍 Locations"
WHERE type = "location" AND visited = true
SORT last_visit DESC, name ASC
```

## All locations (including unvisited)

```dataview
TABLE WITHOUT ID
  link(file.link, name) AS Location,
  region AS Region,
  visited AS Visited,
  habitat AS Habitat
FROM "📍 Locations"
WHERE type = "location"
SORT visited DESC, name ASC
```
