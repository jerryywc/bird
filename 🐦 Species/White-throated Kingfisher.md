---
type: species
id: white-throated-kingfisher
common_name: White-throated Kingfisher
scientific_name: Halcyon smyrnensis
family: Alcedinidae
order: Coraciiformes
iucn_status: Least Concern
malaysia_status: Resident
aliases:
  - WTKF
  - White-breasted Kingfisher
  - Pekaka Dada Putih
  - 白胸翡翠
life_list: true
target: false
wishlist: false
best_photo: ""
tags:
  - species
  - kingfisher
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

Snow-white throat & breast: A large, bright white patch covering the throat and central breast (looks like a clean white bib).

Deep chocolate-brown head & belly: Head, neck, lower breast, belly, and shoulders are a rich, dark chocolate brown.

Electric blue back & wings: Bright cyan to electric-blue back, rump, and tail; in flight, displays a prominent white wing-patch on black flight feathers.

Heavy red bill & legs: Large, dagger-like coral-red bill and bright red legs/feet.

#### vs. Lookalikes:

vs. Stork-billed Kingfisher: Much larger with an enormous red bill; features a yellow/buff neck, head, and underparts rather than chocolate-brown and white.

vs. Black-capped Kingfisher: Has a solid black cap/head, a broad white collar around the neck, and a purple-blue back rather than electric cyan.

vs. Collared Kingfisher: Completely greenish-blue upperparts with a white collar, pure white underparts, and a dark black upper bill (lacks chocolate-brown plumage).

#### Immature:

Duller plumage: Brown feathers on the head and belly are paler with fine dark scaling or scalloping on the breast.

Darker bill: Bill is dark brownish-horn with a dull reddish base rather than bright red.

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
