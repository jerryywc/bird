# 2026 Field Journal

```dataview
TABLE WITHOUT ID
  link(file.path, title) AS Trip,
  date AS Date,
  locations AS Locations,
  length(species_observed) AS "# Species",
  rating AS Rating,
  status AS Status
FROM "📖 Field Journal/2026"
WHERE type = "trip"
SORT date DESC
```
