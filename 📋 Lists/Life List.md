---
type: list
title: Life List
updated: 2026-08-06
tags:
  - list
  - life-list
---

# Life List

Species I've personally observed and logged (`life_list: true`).

```dataview
TABLE WITHOUT ID
  link(file.link, common_name) AS Species,
  scientific_name AS "Scientific name",
  first_seen AS "First seen",
  malaysia_status AS Status
FROM "🐦 Species"
WHERE type = "species" AND life_list = true
SORT first_seen ASC, common_name ASC
```

## Count

```dataview
TABLE WITHOUT ID
  length(rows) AS "Life list total"
FROM "🐦 Species"
WHERE type = "species" AND life_list = true
GROUP BY true
```
