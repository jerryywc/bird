---
type: species
id: mangrove-pitta
common_name: Mangrove Pitta
scientific_name: Pitta megarhyncha
family: Pittidae
order: Passeriformes
iucn_status: Near Threatened
malaysia_status: Resident
aliases:
  - MP
life_list: false
target: true
wishlist: false
first_seen: 
best_photo: ""
tags:
  - species
  - pitta
  - target
created: 2026-08-06
updated: 2026-08-06
---

# Mangrove Pitta

*Pitta megarhyncha*

## Personal summary

Not yet on the life list — priority target for mangrove mornings. Known from KSNP boardwalk areas; listen for the call before chasing silhouettes.

## Identification tips (personal)

- Classic pitta shape; green upperparts, buff underparts, darker crown
- Skulking on muddy mangrove floor

## Behaviour I've seen

- *(none yet)*

## Best conditions / approach

- Early morning, quiet boardwalk, call playback only where ethical/permitted
- Low angle, patience over pursuit

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
