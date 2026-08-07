---
type: species
id: red-wattled-lapwing
common_name: Red-wattled Lapwing
scientific_name: Vanellus indicus
family: Charadriidae
order: Charadriiformes
iucn_status: Least Concern
malaysia_status: Resident
aliases:
  - RWL
  - Burung Duit-Duit
  - 肉垂麦鸡
life_list: true
target: false
wishlist: false
best_photo: ""
tags:
  - species
created: 2026-08-06
updated: 2026-08-06
---

# 

*`= this.scientific_name`*

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

Red wattle & bill: Bright red fleshy facial wattle right in front of the eyes, paired with a red bill featuring a sharp black tip and a red eye-ring.

Black & white head pattern: Solid black crown, face, throat, and breast bib; bold white stripe starting behind the eye and running down the side of the neck to the white underparts.

Body & Legs: Light bronze-brown back and wing coverts, contrasting with a pure white belly and long, bright yellow legs.

In Flight: Striking broad white wing-bar across black flight feathers, and a white tail with a black band near the tip. Highly vocal in flight ("did-he-do-it!").

#### vs. Lookalikes:

vs. Yellow-wattled Lapwing: Yellow-wattled has bright yellow facial wattles (instead of red), a sandy-brown neck, and lacks the solid black throat and chest bib.

vs. River Lapwing: River Lapwing features a black crest, a greyish neck, and a brown breast band, lacking the bold red wattle.

vs. Masked Lapwing: Masked Lapwing has massive yellow fleshy wattles covering the face and a white neck (lacks the black bib and red facial wattle).

#### Immature:

Duller markings: Black on the head and breast is duller brown or mixed with white patches; chin and throat are white.

Smaller wattle: The red facial wattle is much smaller, pale, or undeveloped.

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
