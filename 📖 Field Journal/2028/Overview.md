# 2028 Field Journal

```dataview
TABLE WITHOUT ID
  link(file.path, title) AS Trip,
  date AS Date,
  locations AS Locations,
  length(species_observed) AS "# Species",
  rating AS Rating
FROM "📖 Field Journal/2028"
WHERE type = "trip"
SORT date DESC
```

*No trips yet — create `YYYY-MM-DD Title/Journal.md` from [[🧩 Templates/Trip]].*
