# Portfolio

Curated keepers by species. Source files stay in trip folders.

```dataview
TABLE WITHOUT ID
  link(file.link, title) AS Portfolio,
  species AS Species,
  featured AS Featured,
  length(photos) AS Frames
FROM "📸 Portfolio"
WHERE type = "portfolio"
SORT featured DESC, title ASC
```

New note → template [[🧩 Templates/Portfolio]].
