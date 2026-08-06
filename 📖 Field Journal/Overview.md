# Field Journal

Trip folders live under year directories:

`📖 Field Journal/YYYY/YYYY-MM-DD Title/{Journal.md, *.jpg, GPS.gpx?}`

## All trips

```dataview
TABLE WITHOUT ID
  link(file.path, title) AS Trip,
  date AS Date,
  year AS Year,
  locations AS Locations,
  length(species_observed) AS "# Species",
  rating AS Rating
FROM "📖 Field Journal"
WHERE type = "trip"
SORT date DESC
```

## Years

- [[📖 Field Journal/2026/Overview|2026]]
- [[📖 Field Journal/2027/Overview|2027]]
- [[📖 Field Journal/2028/Overview|2028]]
