# Laval

Pack `qc-laval` · version 1.0.0 · grille 200 m · Canada › Québec › Grand Montréal

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 12 495 |
| dont restreintes (aéroport, militaire, prison) | 24 |
| Cellules retirées par le masque d'eau | 1 000 |
| Villes | 1 |
| Arrondissements et quartiers | 14 |
| Îles | 0 |
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

## Villes (1)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Parcs |
|---|---:|---:|---:|---:|---:|---:|
| Laval | 13 495 | 1 000 | 12 495 | 24 | **12 471** | 10 |

## Arrondissements et quartiers (14)

| Zone | Ville | Brut | Eau | Sans eau | Restr. | Comptées | Parcs |
|---|---|---:|---:|---:|---:|---:|---:|
| Duvernay | laval | 2 464 | 155 | 2 309 | 0 | **2 309** | 2 |
| Chomedey | laval | 2 096 | 56 | 2 040 | 0 | **2 040** | 1 |
| Saint-François | laval | 2 072 | 249 | 1 823 | 12 | **1 811** |  |
| Auteuil | laval | 1 328 | 77 | 1 251 | 0 | **1 251** |  |
| Sainte-Dorothée | laval | 1 184 | 74 | 1 110 | 0 | **1 110** | 1 |
| Fabreville | laval | 1 182 | 122 | 1 060 | 0 | **1 060** | 2 |
| Sainte-Rose | laval | 890 | 48 | 842 | 0 | **842** | 1 |
| Vimont | laval | 711 | 2 | 709 | 0 | **709** | 1 |
| Laval-des-Rapides | laval | 492 | 38 | 454 | 0 | **454** | 1 |
| Saint-Vincent-de-Paul | laval | 402 | 0 | 402 | 12 | **390** | 1 |
| Laval-Ouest | laval | 259 | 54 | 205 | 0 | **205** |  |
| Pont-Viau | laval | 181 | 16 | 165 | 0 | **165** |  |
| Laval-sur-le-Lac | laval | 129 | 31 | 98 | 0 | **98** |  |
| Îles-Laval | laval | 56 | 28 | 28 | 0 | **28** |  |

## Parcs (10)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Les défis « parc » demandent au moins 10 cellules.

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Bois Duvernay | Laval › Duvernay | 152 |
| Le Boisé Sainte-Dorothée | Laval › Sainte-Dorothée | 143 |
| Bois de l'Équerre | Laval › Sainte-Rose | 111 |
| Bois Papineau | Laval › Duvernay | 53 |
| Bois de la Source | Laval › Fabreville | 22 |
| Centre de la nature | Laval › Saint-Vincent-de-Paul | 20 |
| Parc Bernard-Landry | Laval › Laval-des-Rapides | 15 |
| Parc de Lausanne | Laval › Vimont | 10 |
| Réserve naturelle de l'Île Locas ⚠️ | Laval › Fabreville | 6 |
| Le Boutillier Park ⚠️ | Laval › Chomedey | 5 |

⚠️ 2 parc(s) sous le seuil de 10 cellules : ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| airport | 12 |
| prison | 12 |
| military | 0 |
| **Total déclaré** | **24** |
| dont dans une zone de ce territoire | 24 |


### Zones concernées

| Zone | Cellules exclues |
|---|---:|
| Laval | 24 |
| Saint-Vincent-de-Paul | 12 |
| Saint-François | 12 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
