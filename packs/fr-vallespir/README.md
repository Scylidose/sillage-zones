# Vallespir

Pack `fr-vallespir` · version 1.3.0 · grille 200 m · France › Occitanie

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
| Parcs | 75 |

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
| Maureillas-las-Illas | 1 947 | 1 | 1 946 | 0 | **1 946** | 15 |
| Céret | 1 745 | 9 | 1 736 | 0 | **1 736** | 17 |
| Reynès | 1 274 | 0 | 1 274 | 0 | **1 274** | 3 |
| L'Albère | 748 | 0 | 748 | 0 | **748** | 8 |
| Le Boulou | 671 | 24 | 647 | 0 | **647** | 8 |
| Vivès | 521 | 0 | 521 | 0 | **521** | 6 |
| Saint-Jean-Pla-de-Corts | 491 | 15 | 476 | 0 | **476** | 10 |
| Taillet | 463 | 0 | 463 | 0 | **463** | 2 |
| Les Cluses | 404 | 0 | 404 | 0 | **404** |  |
| Le Perthus | 195 | 0 | 195 | 0 | **195** | 5 |

## Parcs (75)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Forêt de Maureillas-las-Illas (5) ⚠️ | Maureillas-las-Illas | 2 674 |
| Forêt de l'Albère (4) ⚠️ | L'Albère | 872 |
| Forêt de Taillet ⚠️ | Taillet | 714 |
| Forêt de Maureillas-las-Illas (4) ⚠️ | Maureillas-las-Illas | 181 |
| Forêt de Vivès (5) ⚠️ | Vivès | 171 |
| Forêt du Perthus (3) ⚠️ | Le Perthus | 165 |
| Forêt de Céret | Céret | 108 |
| Forêt de Maureillas-las-Illas (3) | Maureillas-las-Illas | 75 |
| Forêt de Maureillas-las-Illas (2) | Maureillas-las-Illas | 61 |
| Forêt de Vivès | Vivès | 59 |
| Forêt de Maureillas-las-Illas (8) | Maureillas-las-Illas | 36 |
| Forêt de Reynès | Reynès | 33 |
| Forêt du Perthus | Le Perthus | 27 |
| Forêt de Maureillas-las-Illas (7) | Maureillas-las-Illas | 23 |
| Forêt de Maureillas-las-Illas | Maureillas-las-Illas | 21 |
| Forêt de Maureillas-las-Illas (9) | Maureillas-las-Illas | 21 |
| Forêt de Vivès (2) | Vivès | 18 |
| Bois de Saint-Jean-Pla-de-Corts | Saint-Jean-Pla-de-Corts | 12 |
| Forêt de l'Albère (7) | L'Albère | 12 |
| Forêt de Céret (2) | Céret | 10 |
| Forêt de Reynès (2) | Reynès | 10 |
| Forêt du Boulou ⚠️ | Le Boulou | 9 |
| Bois de Saint-Jean-Pla-de-Corts (6) ⚠️ | Saint-Jean-Pla-de-Corts | 6 |
| Bois de Céret (8) ⚠️ | Céret | 6 |
| Forêt de l'Albère (3) ⚠️ | L'Albère | 6 |
| Forêt du Perthus (4) ⚠️ | Le Perthus | 6 |
| Forêt de l'Albère ⚠️ | L'Albère | 5 |
| Bois de Céret ⚠️ | Céret | 5 |
| Forêt de l'Albère (2) ⚠️ | L'Albère | 4 |
| Bois de Céret (3) ⚠️ | Céret | 4 |
| Forêt de Vivès (6) ⚠️ | Vivès | 4 |
| Parc du château d'Aubiry ⚠️ | Céret | 3 |
| Forêt de Vivès (3) ⚠️ | Vivès | 3 |
| Bois de Saint-Jean-Pla-de-Corts (2) ⚠️ | Saint-Jean-Pla-de-Corts | 3 |
| Bois de Céret (4) ⚠️ | Céret | 3 |
| Forêt de Maureillas-las-Illas (12) ⚠️ | Maureillas-las-Illas | 3 |
| Forêt de l'Albère (8) ⚠️ | L'Albère | 3 |
| Aire de Loisirs du Prat de la Farga ⚠️ | Maureillas-las-Illas | 2 |
| Bois de Saint-Jean-Pla-de-Corts (3) ⚠️ | Saint-Jean-Pla-de-Corts | 2 |
| Bois de Céret (2) ⚠️ | Céret | 2 |
| Bois de Maureillas-las-Illas ⚠️ | Maureillas-las-Illas | 2 |
| Bois de Saint-Jean-Pla-de-Corts (4) ⚠️ | Saint-Jean-Pla-de-Corts | 1 |
| Bois de Saint-Jean-Pla-de-Corts (5) ⚠️ | Céret | 1 |
| Bois de Saint-Jean-Pla-de-Corts (7) ⚠️ | Saint-Jean-Pla-de-Corts | 1 |
| Bois de Céret (5) ⚠️ | Céret | 1 |
| Bois de Céret (6) ⚠️ | Céret | 1 |
| Bois de Céret (7) ⚠️ | Céret | 1 |
| Forêt de Vivès (4) ⚠️ | Vivès | 1 |

27 parc(s) plus petits qu'une cellule ne sont pas listés : la carte les dessine, mais ils n'offrent aucune cellule.

⚠️ 60 parc(s) hors de la fenêtre 10–125 cellules (54 trop petit(s), 6 trop grand(s)) : affichés sur la carte, mais ils ne peuvent pas servir de cible à un défi.

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
