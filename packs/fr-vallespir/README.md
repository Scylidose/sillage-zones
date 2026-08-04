# Vallespir

Pack `fr-vallespir` · version 1.1.0 · grille 200 m · France › Occitanie

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 8 409 |
| dont restreintes (aéroport, militaire, prison) | 0 |
| Cellules retirées par le masque d'eau | 49 |
| Villes | 10 |
| Arrondissements et quartiers | 0 |
| Îles | 0 |
| Parcs | 18 |

Une cellule appartenant à plusieurs zones (un arrondissement *et* sa ville) n'est comptée qu'une fois dans le total du territoire, mais apparaît dans chacune des zones ci-dessous.

« Retirées par le masque d'eau » est mesuré au moment du rognage, par `build_water_mask.py`. Il ne peut pas être recalculé depuis le pack : les frontières y sont déjà découpées sur la rive, donc ces cellules sont hors des polygones et un recomptage les trouverait toutes à zéro — ce qui se lirait, à tort, comme « pas d'eau ici ».

### Lire les colonnes

| Colonne | Ce que c'est |
|---|---|
| **Brut** | cellules du polygone d'origine, avant toute exclusion |
| **Eau** | parmi elles, retirées par le masque d'eau — elles n'appartiennent à aucune zone |
| **Sans eau** | ce que publie `cell-totals.json` |
| **Restr.** | parmi elles, dans un aéroport, une zone militaire ou une prison |
| **Comptées** | le dénominateur réel de l'app : sans eau − restreintes |

## Villes (10)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Parcs |
|---|---:|---:|---:|---:|---:|---:|
| Maureillas-las-Illas | 1 947 | 1 | 1 946 | 0 | **1 946** | 5 |
| Céret | 1 745 | 9 | 1 736 | 0 | **1 736** |  |
| Reynès | 1 274 | 0 | 1 274 | 0 | **1 274** | 2 |
| L'Albère | 748 | 0 | 748 | 0 | **748** |  |
| Le Boulou | 671 | 24 | 647 | 0 | **647** |  |
| Vivès | 521 | 0 | 521 | 0 | **521** | 2 |
| Saint-Jean-Pla-de-Corts | 491 | 15 | 476 | 0 | **476** |  |
| Taillet | 463 | 0 | 463 | 0 | **463** |  |
| Les Cluses | 404 | 0 | 404 | 0 | **404** | 1 |
| Le Perthus | 195 | 0 | 195 | 0 | **195** | 1 |

## Parcs (18)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Les défis « parc » demandent au moins 10 cellules.

| Parc | Cellules |
|---|---:|
| Forêt de l'Albère (3) | 226 |
| Forêt du Perthus (2) | 193 |
| Forêt de Maureillas-las-Illas (4) | 181 |
| Forêt de Vivès | 111 |
| Forêt de Céret | 108 |
| Forêt de Maureillas-las-Illas (5) | 89 |
| Forêt de l'Albère (2) | 78 |
| Forêt de Maureillas-las-Illas (3) | 75 |
| Forêt du Perthus | 74 |
| Forêt de Maureillas-las-Illas (2) | 61 |
| Forêt de Reynès | 33 |
| Forêt de Maureillas-las-Illas (7) | 29 |
| Forêt de Céret (2) | 29 |
| Forêt du Boulou | 28 |
| Forêt de l'Albère | 22 |
| Forêt de Maureillas-las-Illas | 21 |
| Forêt de Maureillas-las-Illas (6) | 21 |
| Forêt de Vivès (2) | 18 |

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
