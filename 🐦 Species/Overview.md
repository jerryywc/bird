# Species

Personal species notes. Trips auto-link when `species_observed` matches `common_name`.

```dataview
TABLE WITHOUT ID
  link(file.link, common_name) AS Species,
  scientific_name AS Scientific,
  life_list AS Life,
  target AS Target,
  wishlist AS Wish,
  first_seen AS "First seen"
FROM "🐦 Species"
WHERE type = "species"
SORT common_name ASC
```

New note → template [[🧩 Templates/Species]].
