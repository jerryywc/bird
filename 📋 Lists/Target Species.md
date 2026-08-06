---
type: list
title: Target Species
updated: 2026-08-06
tags:
  - list
  - targets
---

# Target Species

Active photography targets (`target: true`).

```dataview
TABLE WITHOUT ID
  link(file.link, common_name) AS Species,
  scientific_name AS "Scientific name",
  malaysia_status AS Status,
  iucn_status AS IUCN
FROM "🐦 Species"
WHERE type = "species" AND target = true
SORT common_name ASC
```
