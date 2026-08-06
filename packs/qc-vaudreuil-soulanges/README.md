# Vaudreuil-Soulanges (Montérégie)

Pack `qc-vaudreuil-soulanges` · version 1.0.1 · grille 200 m · Canada › Québec › Grand Montréal

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 14 434 |
| dont restreintes (aéroport, militaire, prison) | 26 |
| Cellules retirées par le masque d'eau | 3 502 |
| Villes | 11 |
| Arrondissements et quartiers | 0 |
| Îles | 1 |
| Parcs | 10 |

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

## Îles

| Île | Cellules | Composition |
|---|---:|---|
| Île Perrot | 2 112 | somme de 4 villes |

Une île *composite* n'a pas de cellules à elle : sa progression est la somme de ses villes, et ses cellules ne lui sont jamais rattachées directement — elles compteraient deux fois.

## Villes (11)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Parcs |
|---|---:|---:|---:|---:|---:|---:|
| Les Cèdres | 3 919 | 0 | 3 919 | 21 | **3 898** |  |
| Vaudreuil-Dorion | 4 682 | 988 | 3 694 | 0 | **3 694** | 4 |
| Saint-Lazare | 3 386 | 0 | 3 386 | 5 | **3 381** | 2 |
| Notre-Dame-de-l'Île-Perrot | 3 517 | 2 099 | 1 418 | 0 | **1 418** | 1 |
| Hudson | 1 097 | 0 | 1 097 | 0 | **1 097** | 2 |
| Pincourt | 483 | 120 | 363 | 0 | **363** |  |
| Ville de l'Île-Perrot | 487 | 212 | 275 | 0 | **275** |  |
| Pointe-des-Cascades | 131 | 0 | 131 | 0 | **131** | 1 |
| Vaudreuil-sur-le-Lac | 144 | 77 | 67 | 0 | **67** |  |
| Terrasse-Vaudreuil | 62 | 6 | 56 | 0 | **56** |  |
| L'Île-Cadieux | 28 | 0 | 28 | 0 | **28** |  |

## Parcs (10)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Les défis « parc » demandent au moins 10 cellules.

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Parc nature les Forestiers-de-Saint-Lazare | Saint-Lazare | 148 |
| Parc nature de Pointe-des-Cascades | Pointe-des-Cascades | 24 |
| Parc de Vaudreuil-Dorion | Vaudreuil-Dorion | 15 |
| Parc-Nature Harwood | Vaudreuil-Dorion | 13 |
| Parc Sandy Beach | Hudson | 11 |
| Parc nature de la Tourbière-du-Bordelais ⚠️ | Saint-Lazare | 9 |
| Réserve écologique des Îles-Avelle-Wight-et-Hiam ⚠️ | Vaudreuil-Dorion | 9 |
| Réserve naturelle du Marécage-des-Chenaux-de-Vaudreuil ⚠️ | Vaudreuil-Dorion | 9 |
| Parc historique Pointe-du-Moulin ⚠️ | Notre-Dame-de-l'Île-Perrot | 6 |
| Parc de Hudson ⚠️ | Hudson | 6 |

⚠️ 5 parc(s) sous le seuil de 10 cellules : ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| airport | 26 |
| military | 0 |
| prison | 0 |
| **Total déclaré** | **26** |
| dont dans une zone de ce territoire | 26 |


### Zones concernées

| Zone | Cellules exclues |
|---|---:|
| Les Cèdres | 21 |
| Saint-Lazare | 5 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
