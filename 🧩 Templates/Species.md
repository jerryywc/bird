---
type: species
id: 
common_name: 
scientific_name: ""
family: ""
order: ""
iucn_status: ""
malaysia_status: ""
aliases: []
life_list: false
target: false
wishlist: false
best_photo: ""
tags:
  - species
created: {{date}}
updated: {{date}}
---

# 

*`= this.scientific_name`*

> Fill `common_name` to match this note’s title exactly (join key for trips).

## First seen

```dataview
TABLE WITHOUT ID
  date AS Date,
  link(file.path, title) AS Trip
FROM "📖 Field Journal"
WHERE type = "trip" AND contains(species_observed, this.common_name)
SORT date ASC
LIMIT 1
```

## Last seen

```dataview
TABLE WITHOUT ID
  date AS Date,
  link(file.path, title) AS Trip
FROM "📖 Field Journal"
WHERE type = "trip" AND contains(species_observed, this.common_name)
SORT date DESC
LIMIT 1
```

## Best photo

```dataviewjs
const photo = dv.current().best_photo;
if (photo) {
  dv.paragraph(`![[${photo}|400]]`);
} else {
  dv.paragraph("*No best photo set yet.*");
}
```

## Personal summary

-

## Identification tips

-

## Behaviour I've seen

-

## Best conditions / approach

-

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

## Links

- Life list: `= this.life_list`
- Target: `= this.target`
- Wish list: `= this.wishlist`
