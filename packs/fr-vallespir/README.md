# Vallespir

Pack `fr-vallespir` · version 1.0.0 · grille 200 m · France › Occitanie

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 4 804 |
| dont restreintes (aéroport, militaire, prison) | 0 |
| Cellules écartées comme eau | 0 |
| Villes | 4 |
| Arrondissements et quartiers | 0 |
| Îles | 0 |
| Parcs | 13 |

Une cellule appartenant à plusieurs zones (un arrondissement *et* sa ville) n'est comptée qu'une fois dans le total du territoire, mais apparaît dans chacune des zones ci-dessous.

« Écartées comme eau » ne compte que les cellules d'eau tombant dans un polygone de zone : les frontières sont rognées sur la rive, donc l'essentiel du fleuve n'a jamais appartenu à personne.

### Lire les colonnes

| Colonne | Ce que c'est |
|---|---|
| **Brut** | cellules dans le polygone, avant toute exclusion |
| **Eau** | parmi elles, écartées comme plan d'eau — elles n'appartiennent à aucune zone |
| **Sans eau** | ce que publie `cell-totals.json` |
| **Restr.** | parmi elles, dans un aéroport, une zone militaire ou une prison |
| **Comptées** | le dénominateur réel de l'app : sans eau − restreintes |

## Villes (4)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Parcs |
|---|---:|---:|---:|---:|---:|---:|
| Maureillas-las-Illas | 1 946 | 0 | 1 946 | 0 | **1 946** | 5 |
| Céret | 1 736 | 0 | 1 736 | 0 | **1 736** |  |
| Le Boulou | 646 | 0 | 646 | 0 | **646** |  |
| Saint-Jean-Pla-de-Corts | 476 | 0 | 476 | 0 | **476** |  |

## Parcs (13)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Les défis « parc » demandent au moins 10 cellules.

| Parc | Cellules |
|---|---:|
| Forêt de Maureillas-las-Illas (6) | 193 |
| Forêt de Maureillas-las-Illas (5) | 181 |
| Forêt de Céret | 111 |
| Forêt de Céret (2) | 108 |
| Forêt de Maureillas-las-Illas (7) | 89 |
| Forêt de Maureillas-las-Illas (4) | 75 |
| Forêt de Maureillas-las-Illas (2) | 74 |
| Forêt de Maureillas-las-Illas (3) | 61 |
| Forêt de Maureillas-las-Illas (9) | 29 |
| Forêt de Céret (3) | 29 |
| Forêt du Boulou | 28 |
| Forêt de Maureillas-las-Illas | 21 |
| Forêt de Maureillas-las-Illas (8) | 21 |

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| airport | 0 |
| military | 0 |
| prison | 0 |
| **Total déclaré** | **0** |
| dont dans une zone de ce territoire | 0 |


---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
