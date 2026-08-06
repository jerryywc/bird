# Data model (migration-ready)

Canonical record types used across this vault. All notes carry YAML frontmatter; relationships use **plain string titles** that match note names. A future web app can ingest the same Markdown + sidecar JPEGs without Obsidian-specific link syntax in metadata.

## Entity: `trip`

| Field | Type | Notes |
|---|---|---|
| `type` | `"trip"` | Discriminator |
| `id` | string | Stable slug, e.g. `2026-08-09-kuala-selangor-eagle-feeding` |
| `title` | string | Display title |
| `date` | date | ISO `YYYY-MM-DD` |
| `end_date` | date | Same as `date` for day trips |
| `year` | number | Folder convenience |
| `locations` | string[] | Exact `location.name` values |
| `species_observed` | string[] | Exact `species.common_name` values |
| `companions` | string[] | Optional |
| `weather` | string | Free text |
| `tide` | string | Free text |
| `light` | string | Free text |
| `conditions` | string | Free text |
| `gear` | string[] | Kit list |
| `rating` | number \| null | 1–5 |
| `photos_exported` | number | Count of JPEGs in folder |
| `has_gpx` | boolean | `GPS.gpx` present |
| `cover_image` | string | Filename relative to trip folder |
| `status` | `"draft"` \| `"published"` | |
| `tags` | string[] | |
| `created` / `updated` | date | |

**Files:** `📖 Field Journal/{year}/{date} {title}/Journal.md` plus `*.jpg` / optional `GPS.gpx`.

## Entity: `species`

| Field | Type | Notes |
|---|---|---|
| `type` | `"species"` | |
| `id` | string | Slug |
| `common_name` | string | Primary key for joins |
| `scientific_name` | string | |
| `family` / `order` | string | |
| `iucn_status` | string | |
| `malaysia_status` | string | |
| `aliases` | string[] | Filename codes e.g. `WBSE` |
| `life_list` | boolean | |
| `target` | boolean | |
| `wishlist` | boolean | |
| `first_seen` | date \| null | |
| `best_photo` | string | Vault-relative path |
| `tags` | string[] | |

**Derived:** trips where `contains(species_observed, common_name)`.

## Entity: `location`

| Field | Type | Notes |
|---|---|---|
| `type` | `"location"` | |
| `id` | string | Slug |
| `name` | string | Primary key for joins |
| `region` / `country` | string | |
| `coordinates.lat` / `.lon` | number \| null | WGS84 |
| `habitat` | string[] | |
| `access` | string | |
| `best_season` / `best_tide` | string | |
| `visited` | boolean | |
| `first_visit` / `last_visit` | date \| null | |
| `rating` | number \| null | |
| `tags` | string[] | |

**Derived:** trips where `contains(locations, name)`.

## Entity: `portfolio`

| Field | Type | Notes |
|---|---|---|
| `type` | `"portfolio"` | |
| `id` | string | |
| `title` | string | Usually equals species |
| `species` | string | `common_name` join key |
| `featured` | boolean | Home dashboard |
| `photos` | object[] | See below |
| `tags` | string[] | |

### `photos[]` item

| Field | Type |
|---|---|
| `file` | string (vault-relative path) |
| `trip_id` | string |
| `date` | date |
| `rating` | number |
| `caption` | string |
| `focal_length_mm` | number |
| `settings` | string |

## Entity: `list` / `home`

Dashboard and list notes are query surfaces only (`type: list` | `home`). They should not own canonical data.

## Join rules

```
trip.species_observed[]  ==  species.common_name
trip.locations[]         ==  location.name
portfolio.species        ==  species.common_name
portfolio.photos[].trip_id == trip.id
```

## Suggested web app mapping

| Vault | App |
|---|---|
| Trip folder | `Trip` + `Asset` rows |
| `Journal.md` body | `Trip.notesMarkdown` |
| Species / Location / Portfolio notes | Tables keyed by `id` |
| Dataview blocks | API queries / SQL views |
| JPEG sidecars | Object storage; keep relative paths |

Prefer preserving `id`, ISO dates, and string join keys unchanged during import.
