---
type: species
id: little-egret
common_name: Little Egret
scientific_name: Egretta garzetta
family: Ardeidae
order: Pelecaniformes
iucn_status: Least Concern
malaysia_status: Resident & Winter Visitor
aliases:
  - LE
  - Burung Pucong Kapur
  - 白鹭
life_list: false
target: false
wishlist: false
best_photo: ""
tags:
  - species
  - egret
created: 2026-08-06
updated: 2026-08-06
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

"Golden Slippers" (Diagnostic): Solid black legs contrasting dramatically with bright yellow feet and toes (very obvious in flight).

Bill & Face: Long, very slender all-black bill with pale yellowish-grey bare facial skin (lores) between the bill and eye (turns pinkish/reddish briefly at peak breeding).

Plumage: Pure brilliant white overall. In breeding plumage, displays two long, lanceolate nape plumes and fine wispy plumes on the breast and back.

#### vs. Lookalikes:

vs. Intermediate Egret & Great Egret: Both are much larger with yellow bills (non-breeding) or black bills (breeding), but critically have all-black legs and feet (no bright yellow slippers).

vs. Cattle Egret: Shorter, stockier build with a thick yellow bill (in non-breeding), dark or yellowish legs, a shorter neck, and lacks yellow feet.

vs. Chinese Egret (Vulnerable): Chinese Egret has a bright yellow bill in breeding season, or a dark bill with a pinkish base in non-breeding, along with a shaggy crest (rather than two long nape plumes).

vs. Pacific Reef Heron (White Morph): Pacific Reef Heron has shorter, stockier greenish-yellow legs and a heavier, dull brownish-yellow bill.

#### Immature:

Similar to non-breeding adults, but the yellow on the feet may extend slightly higher up the back of the tarsus (lower leg), and lores are dull greyish-yellow.

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
