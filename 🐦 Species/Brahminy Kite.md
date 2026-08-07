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

## Identification tips

#### Adult:

Contrasting plumage: Distinctive snow-white head, neck, and breast with fine dark streaks; rich chestnut-red to reddish-brown mantle, back, wings, and belly.

In Flight: Broad, rounded wings with black wingtips (primaries); short, pale, rounded tail. Soars on flat or slightly drooped wings (unlike the V-shape of sea eagles).

Bill & Bare Parts: Pale yellow-grey hooked bill; yellow ceres and short yellow legs.

#### vs. Lookalikes:

vs. White-bellied Sea Eagle (Adult): Sea eagle is much larger, has a pure white belly, grey back and wings, and soars in a distinct V-shape (dihedral).

vs. White-bellied Sea Eagle (Immature): Immature sea eagles are mottled brown, lack the chestnut tone, and are significantly larger with wedge-shaped tails.

vs. Osprey: Osprey has a dark brown eye-stripe/mask, white underparts with a brown chest band, and dark brown upperparts; flies with bent wings in an "M" profile.

#### Immature:

Overall appearance: Mottled dark brown and buff overall, looking similar to young eagles/kites; lacks the bold white and chestnut contrast of adults.

Key cues: Pale panel under the primary flight feathers in flight; noticeably rounded tail and medium size help separate it from juvenile sea eagles.

## Behaviour I've seen

- Dives aggressively on tossed food
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
