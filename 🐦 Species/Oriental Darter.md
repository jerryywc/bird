---
type: species
id: oriental-darter
common_name: Oriental Darter
scientific_name: Anhinga melanogaster
family: Anhingidae
order: Suliformes
iucn_status: Near Threatened
malaysia_status: Resident
aliases:
  - Snakebird
life_list: false
target: false
wishlist: true
first_seen: 
best_photo: ""
tags:
  - species
  - wishlist
created: 2026-08-06
updated: 2026-08-06
---

# Oriental Darter

*Anhinga melanogaster*

## Personal summary

Wish-list bird — want a clean perched “snakebird” silhouette with wet wings spread. Likely at larger wetlands beyond my usual KS loop.

## Identification tips (personal)

- Long thin neck; dagger bill
- Often swims low with only neck above water

## Behaviour I've seen

- *(none yet)*

## Best conditions / approach

- Still water for reflections; late afternoon side light

## Trip log

```dataview
TABLE WITHOUT ID
  link(file.path, title) AS Trip,
  date AS Date,
  locations AS Locations,
  rating AS Rating
FROM "📖 Field Journal"
WHERE type = "trip" AND contains(species_observed, this.common_name)
SORT date DESC
```

## Sighting count

```dataview
TABLE WITHOUT ID
  length(rows) AS "Trips with this species"
FROM "📖 Field Journal"
WHERE type = "trip" AND contains(species_observed, this.common_name)
GROUP BY true
```

## Portfolio

```dataview
LIST
FROM "📸 Portfolio"
WHERE type = "portfolio" AND species = this.common_name
```
