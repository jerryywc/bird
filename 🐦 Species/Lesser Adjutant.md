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
first_seen: 2026-08-16
best_photo: ""
tags:
  - species
  - stork
created: 2026-08-16
updated: 2026-08-16
---

# Lesser Adjutant

*Leptoptilos javanicus*

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
- Avoid sudden movement — they flush early

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
