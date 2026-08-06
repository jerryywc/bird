---
type: species
id: lesser-adjutant
common_name: Lesser Adjutant
scientific_name: Leptoptilos javanicus
family: Ciconiidae
order: Ciconiiformes
iucn_status: Near Threatened
malaysia_status: Resident
aliases:
  - LA
life_list: true
target: false
wishlist: false
best_photo: ""
tags:
  - species
  - stork
created: 2026-08-06
updated: 2026-08-06
---

# Lesser Adjutant

*Leptoptilos javanicus*

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

Tall, dark stork with a bare head — uncommon enough that every sighting feels like a win. Seen stalking mudflats at KSNP; prefers distance and quiet approach.

## Identification tips (personal)

- Large stork silhouette; bare yellowish head/neck
- Dark upperparts; pale belly in good light
- Flight: slow, deep wingbeats; neck retracted like a heron

## Behaviour I've seen

- Solitary or loose pairs on open mud
- Slow deliberate walk while foraging

## Best conditions / approach

- Low tide mudflats; long lens essential

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
