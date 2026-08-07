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
best_photo: "📖 Field Journal/2026/2026-08-09 Kuala Selangor Eagle Feeding/WBSE_001.jpg"
tags:
  - species
  - raptor
created: 2026-08-06
updated: 2026-08-06
---

# White-bellied Sea Eagle

*Haliaeetus leucogaster*

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

Head & Body: Pristine white head, neck, chest, belly, and underwing coverts; striking contrast with slate-grey upperparts, wings, and mantle.

In Flight (V-shape soar): Holds broad wings in a distinct shallow "V" shape (dihedral) when soaring; underneath shows white front wing halves contrasting sharply with blackish-grey flight feathers and a wedge-shaped tail with a pure white tip.

Bill & Bare Parts: Massive, heavy lead-grey to bluish-horn bill with a dark hook; pale yellow to greyish unfeathered legs with powerful talons.

#### vs. Lookalikes:

vs. Brahminy Kite: Brahminy Kite is much smaller with a rich chestnut/reddish-brown body and mantle (only head and chest are white), and flies on flat wings rather than in a V-dihedral.

vs. Grey-headed Fish Eagle: Grey-headed has a grey head and upper breast, brown body and wings, and a white belly/tail with a broad black terminal tail band.

vs. Osprey: Osprey is smaller with a prominent dark eye-stripe (eyemask), brown upperparts, and a brown breast band, flying with bent "M-shaped" wings.

#### Immature:

Mottled Brown: Take up to 5 years to gain full adult plumage; juvenile is overall warm brown with pale buff streaks on the head and underparts.

Flight Profile: Still shows the broad wings, short wedge tail, and V-shaped soaring posture, but underwings display a pale translucent patch at the base of the primary feathers.

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
