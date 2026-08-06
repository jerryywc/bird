---
type: list
title: Wish List
updated: 2026-08-06
tags:
  - list
  - wishlist
---

# Wish List

Species I want to see someday (`wishlist: true`) — not yet active field targets.

```dataview
TABLE WITHOUT ID
  link(file.link, common_name) AS Species,
  scientific_name AS "Scientific name",
  malaysia_status AS Status
FROM "🐦 Species"
WHERE type = "species" AND wishlist = true
SORT common_name ASC
```
