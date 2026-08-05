# Montréal (île)

Pack `qc-montreal-ile` · version 1.0.0 · grille 200 m · Canada › Québec › Grand Montréal

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 25 367 |
| dont restreintes (aéroport, militaire, prison) | 611 |
| Cellules retirées par le masque d'eau | 6 398 |
| Villes | 16 |
| Arrondissements et quartiers | 19 |
| Îles | 2 |
| Parcs | 60 |

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
| Île de Montréal | 25 367 | somme de 15 villes |
| Parc Jean-Drapeau | 110 | polygone propre |

Une île *composite* n'a pas de cellules à elle : sa progression est la somme de ses villes, et ses cellules ne lui sont jamais rattachées directement — elles compteraient deux fois.

## Villes (16)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Parcs |
|---|---:|---:|---:|---:|---:|---:|
| Montreal | 22 453 | 3 872 | 18 581 | 243 | **18 338** | 53 |
| Dorval | 1 453 | 385 | 1 068 | 368 | **700** | 1 |
| Pointe-Claire | 1 790 | 829 | 961 | 0 | **961** | 1 |
| Dollard-Des-Ormeaux | 764 | 7 | 757 | 0 | **757** | 1 |
| Montréal-Est | 712 | 78 | 634 | 0 | **634** |  |
| Beaconsfield | 1 095 | 535 | 560 | 0 | **560** |  |
| Sainte-Anne-de-Bellevue | 563 | 29 | 534 | 0 | **534** | 2 |
| Kirkland | 492 | 1 | 491 | 0 | **491** |  |
| Mont-Royal | 390 | 0 | 390 | 0 | **390** |  |
| Senneville | 928 | 558 | 370 | 0 | **370** | 1 |
| Côte-Saint-Luc | 352 | 0 | 352 | 0 | **352** |  |
| Baie-D'Urfé | 383 | 79 | 304 | 0 | **304** | 1 |
| Westmount | 202 | 0 | 202 | 0 | **202** |  |
| Hampstead | 92 | 0 | 92 | 0 | **92** |  |
| Montréal-Ouest | 71 | 0 | 71 | 0 | **71** |  |
| L'Île-Dorval | 8 | 0 | 8 | 0 | **8** |  |

## Arrondissements et quartiers (19)

| Zone | Ville | Brut | Eau | Sans eau | Restr. | Comptées | Parcs |
|---|---|---:|---:|---:|---:|---:|---:|
| Saint-Laurent | montreal | 2 190 | 4 | 2 186 | 194 | **1 992** | 4 |
| Pointe-aux-Trembles-Rivieres-des-Prairies | montreal | 2 520 | 339 | 2 181 | 6 | **2 175** | 5 |
| Pierrefonds--Roxboro | montreal | 1 668 | 287 | 1 381 | 0 | **1 381** | 2 |
| Mercier-Hochelaga-Maisonneuve | montreal | 1 396 | 98 | 1 298 | 47 | **1 251** | 4 |
| Ahuntsic-Cartierville | montreal | 1 239 | 1 | 1 238 | 0 | **1 238** | 6 |
| L'Ile-Bizard--Sainte-Genevieve | montreal | 1 812 | 618 | 1 194 | 0 | **1 194** | 2 |
| Cote-des-Neiges--Notre-Dame-de-Grace | montreal | 1 084 | 0 | 1 084 | 0 | **1 084** | 1 |
| Lachine | montreal | 1 125 | 218 | 907 | 0 | **907** | 2 |
| Villeray-Saint-Michel-Parc-Extension | montreal | 839 | 8 | 831 | 0 | **831** | 2 |
| LaSalle | montreal | 1 250 | 423 | 827 | 0 | **827** | 3 |
| Rosemont--La-Petite-Patrie | montreal | 810 | 0 | 810 | 0 | **810** | 4 |
| Ville-Marie | montreal | 1 094 | 294 | 800 | 0 | **800** | 4 |
| Sud-Ouest | montreal | 915 | 117 | 798 | 0 | **798** | 3 |
| Anjou | montreal | 705 | 3 | 702 | 0 | **702** | 2 |
| St-Leonard | montreal | 691 | 0 | 691 | 0 | **691** | 1 |
| Montreal-Nord | montreal | 638 | 75 | 563 | 0 | **563** |  |
| Verdun--Ile-des-Soeurs | montreal | 1 071 | 589 | 482 | 0 | **482** | 5 |
| Plateau-Mont-Royal | montreal | 416 | 3 | 413 | 0 | **413** | 3 |
| Outremont | montreal | 198 | 1 | 197 | 0 | **197** |  |

## Îles à polygone propre

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Parcs |
|---|---:|---:|---:|---:|---:|---:|
| Parc Jean-Drapeau | 135 | 25 | 110 | 0 | **110** | 1 |

## Parcs (60)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Les défis « parc » demandent au moins 10 cellules.

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Grand Parc de l'Ouest | Montreal › Pierrefonds--Roxboro | 187 |
| Parc-nature du Bois-de-l'Île-Bizard | Montreal › L'Ile-Bizard--Sainte-Genevieve | 156 |
| Arboretum Morgan | Sainte-Anne-de-Bellevue | 134 |
| Parc-nature de la Pointe-aux-Prairies | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 132 |
| Parc du Mont-Royal | Montreal › Ville-Marie | 96 |
| Parc agricole du Bois-de-la-Roche | Senneville | 90 |
| Parc-nature du Bois-de-Liesse | Montreal › Saint-Laurent | 87 |
| Parc Jean-Drapeau | Montreal › Ville-Marie › Parc Jean-Drapeau | 84 |
| Refuge d'oiseaux migrateurs de l'Île-aux-Hérons | Montreal › LaSalle | 75 |
| Parc-nature du Bois-de-Saraguay | Montreal › Ahuntsic-Cartierville | 43 |
| Parc Angrignon | Montreal › Sud-Ouest | 42 |
| Jardin botanique de Montréal | Montreal › Rosemont--La-Petite-Patrie | 41 |
| Parc Frédéric-Back | Montreal › Villeray-Saint-Michel-Parc-Extension | 33 |
| Parc du Canal-de-Lachine | Montreal › Sud-Ouest | 32 |
| Parc Maisonneuve | Montreal › Rosemont--La-Petite-Patrie | 31 |
| Parc olympique | Montreal › Mercier-Hochelaga-Maisonneuve | 23 |
| Parc-nature des Rapides-du-Cheval-Blanc | Montreal › Pierrefonds--Roxboro | 22 |
| Parc écologique des Sources | Montreal › Saint-Laurent | 22 |
| Parc Terra Cotta | Pointe-Claire | 20 |
| Parc-nature du Bois-d'Anjou | Montreal › Anjou | 20 |
| Parc Jarry | Montreal › Villeray-Saint-Michel-Parc-Extension | 19 |
| Parc de la Coulée-Grou | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 19 |
| Parc Marcel-Laurin | Montreal › Saint-Laurent | 18 |
| Parc du Centenaire | Dollard-Des-Ormeaux | 17 |
| Parc de l'Honorable-George-O'Reilly | Montreal › Verdun--Ile-des-Soeurs | 16 |
| Parc-nature du Ruisseau-De-Montigny | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 16 |
| Parc La Fontaine | Montreal › Plateau-Mont-Royal | 15 |
| Parc de la Promenade-Bellerive | Montreal › Mercier-Hochelaga-Maisonneuve | 15 |
| Vieux-Port | Montreal › Ville-Marie | 15 |
| Parc-nature de l'Île-de-la-Visitation | Montreal › Ahuntsic-Cartierville | 15 |
| Domaine Saint-Paul | Montreal › Verdun--Ile-des-Soeurs | 12 |
| Parc Marcelin-Wilson | Montreal › Ahuntsic-Cartierville | 12 |
| Parc Tiohtià:ke Otsira'kéhne | Montreal › Cote-des-Neiges--Notre-Dame-de-Grace | 11 |
| Parc des Rapides | Montreal › LaSalle | 11 |
| Parc Arthur-Therrien | Montreal › Verdun--Ile-des-Soeurs | 10 |
| Parc de l'Aqueduc | Montreal › Verdun--Ile-des-Soeurs | 10 |
| Parc du Père-Marquette ⚠️ | Montreal › Rosemont--La-Petite-Patrie | 9 |
| Parc de Montreal ⚠️ | Montreal › Ville-Marie | 9 |
| Parc des Hirondelles ⚠️ | Montreal › Ahuntsic-Cartierville | 8 |
| Parc Jeanne-Mance ⚠️ | Montreal › Plateau-Mont-Royal | 8 |
| Parc Thomas-Chapais ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 8 |
| Parc Pasquale-Gattuso ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 8 |
| Parc Fritz ⚠️ | Baie-D'Urfé | 8 |
| Parc Philippe-Laheurte ⚠️ | Montreal › Saint-Laurent | 8 |
| McGill Bird Observatory ⚠️ | Sainte-Anne-de-Bellevue | 8 |
| Parc de la Traversée ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 8 |
| Terrains du centre communautaire Sarto-Desnoyers ⚠️ | Dorval | 7 |
| Parc Henri-Julien ⚠️ | Montreal › Ahuntsic-Cartierville | 7 |
| Parc René-Lévesque ⚠️ | Montreal › Lachine | 7 |
| Parc LaSalle ⚠️ | Montreal › Lachine | 7 |
| Parc d'Anjou-sur-le-Lac ⚠️ | Montreal › Anjou | 7 |
| Parc Sir-Wilfrid-Laurier ⚠️ | Montreal › Plateau-Mont-Royal | 6 |
| Parc Félix-Leclerc ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 6 |
| Parc Ahuntsic ⚠️ | Montreal › Ahuntsic-Cartierville | 6 |
| Parc Eugène-Dostie ⚠️ | Montreal › L'Ile-Bizard--Sainte-Genevieve | 6 |
| Parc Delorme ⚠️ | Montreal › St-Leonard | 6 |
| Parc Ignace-Bourget ⚠️ | Montreal › Sud-Ouest | 6 |
| Parc Maynard-Ferguson ⚠️ | Montreal › Verdun--Ile-des-Soeurs | 5 |
| Parc de Montreal (2) ⚠️ | Montreal › LaSalle | 5 |
| Parc Étienne-Desmarteau ⚠️ | Montreal › Rosemont--La-Petite-Patrie | 4 |

⚠️ 24 parc(s) sous le seuil de 10 cellules : ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| airport | 558 |
| military | 47 |
| prison | 6 |
| **Total déclaré** | **611** |
| dont dans une zone de ce territoire | 611 |


### Zones concernées

| Zone | Cellules exclues |
|---|---:|
| Dorval | 368 |
| Montreal | 243 |
| Saint-Laurent | 194 |
| Mercier-Hochelaga-Maisonneuve | 47 |
| Pointe-aux-Trembles-Rivieres-des-Prairies | 6 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
