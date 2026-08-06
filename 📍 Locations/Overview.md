# Locations

Places you shoot. Visits auto-link when trip `locations` matches `name`.

```dataview
TABLE WITHOUT ID
  link(file.link, name) AS Location,
  region AS Region,
  visited AS Visited,
  rating AS Rating,
  last_visit AS "Last visit"
FROM "📍 Locations"
WHERE type = "location"
SORT visited DESC, name ASC
```

New note → template [[🧩 Templates/Location]].
