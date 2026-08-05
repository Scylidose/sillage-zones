# Agglomération de Longueuil

Pack `qc-longueuil` · version 1.0.0 · grille 200 m · Canada › Québec › Grand Montréal

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 14 331 |
| dont restreintes (aéroport, militaire, prison) | 305 |
| Cellules retirées par le masque d'eau | 1 109 |
| Villes | 5 |
| Arrondissements et quartiers | 11 |
| Îles | 0 |
| Parcs | 12 |

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

## Villes (5)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Parcs |
|---|---:|---:|---:|---:|---:|---:|
| Longueuil | 6 238 | 341 | 5 897 | 218 | **5 679** | 3 |
| Boucherville | 4 182 | 594 | 3 588 | 0 | **3 588** | 2 |
| Brossard | 2 300 | 1 | 2 299 | 0 | **2 299** | 3 |
| Saint-Bruno-de-Montarville | 2 216 | 50 | 2 166 | 87 | **2 079** | 1 |
| Saint-Lambert | 504 | 123 | 381 | 0 | **381** | 2 |

## Arrondissements et quartiers (11)

| Zone | Ville | Brut | Eau | Sans eau | Restr. | Comptées | Parcs |
|---|---|---:|---:|---:|---:|---:|---:|
| Saint-Hubert | longueuil | 3 371 | 4 | 3 367 | 218 | **3 149** | 1 |
| Le Vieux-Longueuil | longueuil | 2 621 | 337 | 2 284 | 0 | **2 284** | 2 |
| Greenfield Park | longueuil | 246 | 0 | 246 | 0 | **246** |  |
| Secteur L | brossard | 192 | 1 | 191 | 0 | **191** |  |
| Secteur R | brossard | 147 | 2 | 145 | 0 | **145** |  |
| Secteur M | brossard | 87 | 0 | 87 | 0 | **87** |  |
| Secteur O | brossard | 79 | 0 | 79 | 0 | **79** |  |
| Secteur J | brossard | 61 | 0 | 61 | 0 | **61** |  |
| Secteur N | brossard | 59 | 0 | 59 | 0 | **59** |  |
| Secteur I | brossard | 55 | 1 | 54 | 0 | **54** |  |
| Secteur E | brossard | 19 | 0 | 19 | 0 | **19** |  |

## Parcs (12)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Les défis « parc » demandent au moins 10 cellules.

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Réserve naturelle du Bois-de-Brossard | Brossard | 119 |
| Parc Michel Chartrand | Longueuil › Le Vieux-Longueuil | 86 |
| Parc Jean-Drapeau | — | 84 |
| Parc de la Cité | Longueuil › Saint-Hubert | 53 |
| Parc Marie-Victorin | Saint-Bruno-de-Montarville | 23 |
| Parc de la Voie maritime | Saint-Lambert | 10 |
| Parc Pierre-Laporte ⚠️ | Boucherville | 9 |
| Refuge d'oiseaux migrateurs des Îles-de-la-Couvée ⚠️ | Saint-Lambert | 9 |
| Parc du Boisé-Du-Pays-Brûlé ⚠️ | Boucherville | 7 |
| Parc Marie-Victorin (2) ⚠️ | Longueuil › Le Vieux-Longueuil | 7 |
| Parc de la Terre ⚠️ | Brossard | 6 |
| Grand Parc Urbain ⚠️ | Brossard | 5 |

⚠️ 6 parc(s) sous le seuil de 10 cellules : ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| airport | 218 |
| military | 87 |
| prison | 0 |
| **Total déclaré** | **305** |
| dont dans une zone de ce territoire | 305 |


### Zones concernées

| Zone | Cellules exclues |
|---|---:|
| Saint-Hubert | 218 |
| Longueuil | 218 |
| Saint-Bruno-de-Montarville | 87 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
