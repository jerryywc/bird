---
type: species
id: asian-openbill
common_name: Asian Openbill
scientific_name: Anastomus oscitans
family: Ciconiidae
order: Ciconiiformes
iucn_status: Least Concern
malaysia_status: Migrant
aliases:
  - Asian Openbill Stork
  - Botak Asia
  - Upih Paruh Sepit
  - 钳嘴鹳
life_list: false
target: false
wishlist: false
best_photo: ""
tags:
  - species
  - stork
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

## Identification tips (personal)

#### Adult:

Diagnostic "open" bill: Massive, dull horn-gray to yellow-gray bill with a distinct gap between the arched upper mandible and recurved lower mandible (only touching at the tip).

Plumage: Pale greyish-white body with contrasting glossy black flight feathers and tail. Turns starker white during breeding season and more muted grey in non-breeding plumage.

Bare parts: Long pinkish-grey to dull reddish legs and feet; bare grey patch around the eyes and lores.

In Flight: Flies with broad wings and neck fully outstretched (classic stork profile), showing strong black-and-white wing contrast beneath.

#### vs. Lookalikes:

vs. White Stork / Oriental Stork: Both are much larger with pure black primaries/secondaries; critically, their bills meet completely along the entire edge without any gap.

vs. Milky Stork: Milky Stork has a bright yellow, slightly decurved solid bill with no gap, a bare reddish/pink face mask, and is significantly larger.

vs. Egrets (e.g., Great/Intermediate Egret): Egrets fold their necks into an "S" shape in flight, whereas the Openbill flies with its neck straight out. Egrets also lack black flight feathers and gap-bills.

#### Immature:

Plumage: Brownish-grey overall, looking noticeably dirtier and duller than adults, with darker brownish streaking on the neck and mantle.

Bill shape: The gap between upper and lower mandibles is very small or absent in young birds, developing as they mature.

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
