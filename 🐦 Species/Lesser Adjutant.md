---
type: species
id: lesser-adjutant
common_name: Lesser Adjutant
scientific_name: Leptoptilos javanicus
family: Ciconiidae
order: Ciconiiformes
iucn_status: Near Threatened
malaysia_status: Resident
aliases:
  - LA
life_list: true
target: false
wishlist: false
best_photo: ""
tags:
  - species
  - stork
created: 2026-08-06
updated: 2026-08-06
---

# Lesser Adjutant

*Leptoptilos javanicus*

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

Tall, dark stork with a bare head — uncommon enough that every sighting feels like a win. Seen stalking mudflats at Pantai Jeram; prefers distance and quiet approach.

## Identification tips

#### Adult:

Head & Neck: Largely bare, scaly head and neck with a yellowish or pale skin tone, sparse hair-like down, and a pale red crown patch.

Massive Bill: Very thick, straight, wedge-shaped horn-colored bill with a straight culmen (ridge).

Upperparts & Wings: Glossy dark slate-black to dark greenish-black back, wings, and tail; clean white belly, vent, and underparts.

No Neck Pouch: Lacks a dangling inflatable neck pouch; has a tight, clean neck profile at rest.

#### vs. Lookalikes:

vs. Greater Adjutant: Greater is noticeably larger with a massive, thicker bill with a curved culmen; possesses a prominent dangling, inflatable gular neck pouch and a pale grey band across the wings (lesser has solid dark wings).

vs. Milky Stork: Milky Stork is predominantly white with black flight feathers, a yellow slightly curved bill, and a bare pink/red facial mask (unlike the all-dark back and bare yellow head of the Lesser Adjutant).

vs. Painted Stork: Painted Stork features heavy black breast bands, pink tail/wing coverts, and a yellow downward-curved bill.

#### Immature:

Duller & Hairy: Head and neck are covered in much thicker brown downy feathers, giving it a scruffier, hairier appearance.

Plumage: Dark upperparts are duller and lack the glossy greenish sheen seen in adults.

## Behaviour I've seen

- Solitary or loose pairs on open mud
- Slow deliberate walk while foraging

## Best conditions / approach

- Low tide mudflats; long lens essential

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
