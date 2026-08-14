# sillage-zones

Official-zone packs for [Sillage](https://github.com/Scylidose/WorldExplorer), an
Android exploration app that tracks which 200 m cells of the world you have
walked through.

A **pack** is one territory, self-contained: the boundaries of its cities and
subdivisions, the water bodies to exclude, the restricted areas (airports,
military zones, prisons), its parks, and the precomputed cell counts each zone
is measured against. The app downloads packs from here, so a boundary
correction — or a whole new city — reaches users without an app release.

## Layout

| Path | What it is |
|---|---|
| `index.json` | The catalogue the app reads. Everything the download screen shows comes from it, so a pack can be listed, sized and located without downloading anything. |
| `packs/<country>/<region>/<id>/` | The pack files, in clear, nested under the group path its `pack.json` declares. A boundary correction is a readable diff here. The nesting is for browsing only: the app reads `index.json` and the absolute URL of each entry, never these paths, so they can be reorganised without breaking any installed version. |
| Releases | `pack.zip` per version — what the app actually downloads. |

## Pack format

| File | Contents |
|---|---|
| `pack.json` | id, version, grid size, group path (country → region), bbox, checksums |
| `zones.geojson` | cities and arrondissements. Arrondissements come first: the app walks the list in order and tags a cell with every zone it falls in |
| `islands.geojson` | island outlines. `members` means the island is the sum of those cities rather than a shape cells are tested against |
| `water.geojson` | cells whose centre falls in here belong to no zone |
| `restricted-zones.geojson` | drawn on the map as hatched areas |
| `parks.geojson` | used by the park challenges |
| `cell-totals.json` | cells per zone — the denominator of every percentage |
| `restricted-cells.json` | restricted cell ids, subtracted from those denominators |

Two invariants matter, and the app enforces both by refusing to load a pack that
breaks them:

- **`cellSizeM` must match the app's grid** (200 m). The totals are counts of
  cells; counted on a different grid they would put wrong denominators behind
  every percentage — silently.
- **`formatVersion` must be one the app knows.** Guessing at an unknown format
  corrupts boundaries rather than failing.

## Contributing a correction

Edit the GeoJSON under the pack's directory, bump `version` in its `pack.json`, and
open a pull request. Note that `cell-totals.json` and `restricted-cells.json`
are *derived* from the geometry: changing a boundary without regenerating them
leaves the zone measured against the old shape. The generator scripts live in
the app repository under `apps/android/scripts/`.

## Licence

Derived from OpenStreetMap and public open-data sources, and distributed under
the **ODbL** — see [ATTRIBUTION.md](ATTRIBUTION.md).
