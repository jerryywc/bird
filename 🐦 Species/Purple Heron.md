---
type: species
id: purple-heron
common_name: Purple Heron
scientific_name: Ardea purpurea
family: Ardeidae
order: Pelecaniformes
iucn_status: Least Concern
malaysia_status: Resident
aliases:
  - PH
  - Burung Pucong Seriap
  - 紫鹭
life_list: true
target: false
wishlist: false
best_photo: ""
tags:
  - species
  - heron
created:
  "{ date }":
updated:
  "{ date }":
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

#### Adult:

Slender rufous neck: Long, snake-like chestnut/rufous neck marked with distinct black vertical stripes running down the sides.

Dark purplish plumage: Slate-grey upperparts with a dark purplish-chestnut tinge; deep chestnut chest, belly, and thighs; dark crown with black nape plumes.

Bill & feet: Very sharp, slender yellowish dagger-like bill; unusually large yellowish-brown feet built for stepping over wetland vegetation.

#### vs. Lookalikes:

vs. Grey Heron: Grey Heron has a white head and neck with a black crest, a light pearl-grey body, and white underparts (completely lacks the rich chestnut/rufous tones and neck striping of the Purple Heron).

vs. Great-billed Heron: Great-billed is significantly larger and heavier, with uniform dull brownish-grey plumage and a massive, thick bill.

#### Immature:

Buff-brown plumage: Paler, sandy-brown overall with buff edges on wing coverts and less distinct dark striping on the neck.

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
