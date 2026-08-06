---
type: species
id: black-naped-oriole
common_name: Black-naped Oriole
scientific_name: Oriolus chinensis
family: Oriolidae
order: Passeriformes
iucn_status: Least Concern
malaysia_status: Resident
aliases: [BNO, Burung Kunyit Besar, 黑枕黄鹂]
life_list: false
target: false
wishlist: false
best_photo: "📖 Field Journal/2020/2020-10-03 Bukit Rimau/DSC_3081.jpg"
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

Bright golden-yellow overall: Unmistakable vivid canary-yellow body, chest, mantle, and rump.

Broad black nape mask: A wide, continuous black band running straight through the eyes and wrapping right around the back of the head (the nape).

Striking wing & tail contrast: Mostly black wings with yellow spots on the flight feather tips; black tail feathers with bright yellow outer edges.

Heavy pink bill: Robust, conical, deep-pink to pinkish-red bill; dark reddish-brown eyes.

#### vs. Lookalikes:

vs. Eurasian Golden Oriole: Eurasian only has a short black eye-stripe that does not wrap around the back of the head/nape, and has less yellow on the wings.

vs. Slender-billed Oriole: Slender-billed has a distinctly narrower black nape band and a noticeably thinner, slighter bill.

vs. Black-hooded Oriole: Black-hooded has a complete black hood covering the entire head and throat, rather than just a eye/nape mask.

#### Immature:

Duller & streaked: Olive-greenish mantle with a pale off-white belly covered in dark vertical streaks.

Faint mask: Black eye-mask is smudged, incomplete, or dark gray; bill is dull brown or pale pink.

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
