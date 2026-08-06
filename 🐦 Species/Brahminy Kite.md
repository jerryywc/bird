---
type: species
id: brahminy-kite
common_name: Brahminy Kite
scientific_name: Haliastur indus
family: Accipitridae
order: Accipitriformes
iucn_status: Least Concern
malaysia_status: Resident
aliases:
  - BK
  - Red-backed Sea Eagle
life_list: true
target: false
wishlist: false
best_photo: "📖 Field Journal/2026/2026-08-09 Kuala Selangor Eagle Feeding/BK_001.jpg"
tags:
  - species
  - raptor
created: 2026-08-06
updated: 2026-08-06
---

# Brahminy Kite

*Haliastur indus*

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

The acrobat of the feeding — chestnut body, white head/breast, constantly jostling White-bellied Sea Eagles for fish. Smaller and more manoeuvrable; often the more photogenic subject when light is harsh.

## Identification tips (personal)

- Adult: white head/breast + chestnut body — clean two-tone
- Immature: browner, streakier; easy to confuse with other kites at distance

## Behaviour I've seen

- Dives aggressively on tossed fish
- Mid-air tussles and food piracy
- Roosts on nearby poles and mangroves

## Best conditions / approach

- Track one bird through a dive rather than spraying the flock
- Watch for wing-spread catch moments just above the water

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
