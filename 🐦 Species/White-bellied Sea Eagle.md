---
type: species
id: white-bellied-sea-eagle
common_name: White-bellied Sea Eagle
scientific_name: Haliaeetus leucogaster
family: Accipitridae
order: Accipitriformes
iucn_status: Least Concern
malaysia_status: Resident
aliases:
  - WBSE
  - White-bellied Sea-Eagle
life_list: true
target: false
wishlist: false
first_seen: 2026-08-09
best_photo: "📖 Field Journal/2026/2026-08-09 Kuala Selangor Eagle Feeding/WBSE_001.jpg"
tags:
  - species
  - raptor
created: 2026-08-09
updated: 2026-08-09
---

# White-bellied Sea Eagle

*Haliaeetus leucogaster*

## Personal summary

Large coastal raptor — my most reliable subject at the Kuala Selangor eagle feeding. Adults show clean white head/belly against grey wings; juveniles are mottled brown and easy to underexpose against bright sky.

## Identification tips (personal)

- Adult: white head + belly, grey upperwing — unmistakable at distance once known
- Juvenile: brown overall; wait for the white to come in over years
- In flight: broad wings, short wedge-ish tail vs. longer-tailed kites

## Behaviour I've seen

- Circles with Brahminy Kites during feeding boats
- Stoops for fish tossed from boats; often loses contests to aggressive kites
- Perches on dead mangroves between passes

## Best conditions / approach

- Morning sessions at feeding spot — side light on undersides
- Continuous AF, high shutter (≥1/2000) when birds bank overhead
- Leave headroom; they fill the frame fast at 500mm

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
