---
type: species
id: blue-tailed-bee-eater
common_name: Blue-tailed Bee Eater
scientific_name: Merops philippinus
family: Meropidae
order: Coraciiformes
iucn_status: Least Concern
malaysia_status: Migrant / winter visitor
aliases:
  - BTBE
  - Blue-tailed Bee-eater
  - 蓝尾佛法僧
  - 蓝尾蜂虎

life_list: true
target: false
wishlist: false
best_photo: "📖 Field Journal/2023/2023-02-18 Kota Kemuning Wetland/DSC00668.jpg"
tags:
  - species
  - bee-eater
created: 2026-08-06
updated: 2026-08-06
---

# Blue-tailed Bee Eater

*Merops philippinus*

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

Head & Face: Green crown and nape with a broad black mask through the eyes; yellow chin directly above a rich chestnut/rufous throat patch.

Body & Tail: Rich green mantle and wings with a bright blue rump and a long, bright blue tail; central tail feathers extend into narrow streamers.

Underparts: Pale green breast shading to a blue-tinted lower belly and vent.

Bill & Eyes: Long, slender, down-curved black bill paired with deep red eyes.

#### vs. Lookalikes:

vs. Blue-throated Bee-eater: Blue-throated has a rich chestnut-red crown and nape, a royal blue throat (no yellow chin or chestnut patch), and a dark blue tail.

vs. Green Bee-eater: Green Bee-eater is noticeably smaller, has a bright green throat with a narrow black collar line (gorget), a reddish-bronze tinge to the crown, and a green tail.

vs. Chestnut-headed Bee-eater: Chestnut-headed has a bright chestnut head, nape, and upper back, a bright yellow throat framed by a red/black border, and lacks the long central tail streamers.

#### Immature:

Duller overall: Paler olive-green body with a muted, washed-out yellow throat and little to no chestnut color.

Tail features: Rump and tail are duller blue, and central tail streamers are short or absent.

## Behaviour I've seen

- Single bird perched in open wetland edge habitat 

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
