# Vaudreuil-Soulanges (Montérégie)

Pack `qc-vaudreuil-soulanges` · version 1.2.1 · grille 200 m · Canada › Québec › Grand Montréal

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
| Parcs | 175 |

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
| Les Cèdres | 3 919 | 0 | 3 919 | 21 | **3 898** | 16 |
| Vaudreuil-Dorion | 4 682 | 988 | 3 694 | 0 | **3 694** | 69 |
| Saint-Lazare | 3 386 | 0 | 3 386 | 5 | **3 381** | 22 |
| Notre-Dame-de-l'Île-Perrot | 3 517 | 2 099 | 1 418 | 0 | **1 418** | 19 |
| Hudson | 1 097 | 0 | 1 097 | 0 | **1 097** | 11 |
| Pincourt | 483 | 120 | 363 | 0 | **363** | 17 |
| Ville de l'Île-Perrot | 487 | 212 | 275 | 0 | **275** | 11 |
| Pointe-des-Cascades | 131 | 0 | 131 | 0 | **131** | 5 |
| Vaudreuil-sur-le-Lac | 144 | 77 | 67 | 0 | **67** | 1 |
| Terrasse-Vaudreuil | 62 | 6 | 56 | 0 | **56** | 1 |
| L'Île-Cadieux | 28 | 0 | 28 | 0 | **28** |  |

## Parcs (175)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Parc nature les Forestiers-de-Saint-Lazare ⚠️ | Saint-Lazare | 148 |
| Parc nature de Pointe-des-Cascades | Pointe-des-Cascades | 24 |
| Parc de Vaudreuil-Dorion (11) | Vaudreuil-Dorion | 15 |
| Parc-Nature Harwood | Vaudreuil-Dorion | 13 |
| Parc Sandy Beach | Hudson | 11 |
| Parc nature de la Tourbière-du-Bordelais ⚠️ | Saint-Lazare | 9 |
| Réserve écologique des Îles-Avelle-Wight-et-Hiam ⚠️ | Vaudreuil-Dorion | 9 |
| Réserve naturelle du Marécage-des-Chenaux-de-Vaudreuil ⚠️ | Vaudreuil-Dorion | 9 |
| Parc historique Pointe-du-Moulin ⚠️ | Notre-Dame-de-l'Île-Perrot › Île Perrot | 6 |
| Parc de Hudson (3) ⚠️ | Hudson | 6 |
| Parc de Dorion-Gardens ⚠️ | Vaudreuil-Dorion | 4 |
| Parc Olympique ⚠️ | Pincourt › Île Perrot | 4 |
| Parc Saint-Robert ⚠️ | Saint-Lazare | 4 |
| Parc Michel-Martin ⚠️ | Ville de l'Île-Perrot › Île Perrot | 3 |
| Parc des Hirondelles (2) ⚠️ | Notre-Dame-de-l'Île-Perrot › Île Perrot | 3 |
| Parc des Éperviers ⚠️ | Notre-Dame-de-l'Île-Perrot › Île Perrot | 3 |
| Parc nature de l'Île-aux-Tourtes ⚠️ | Vaudreuil-Dorion | 3 |
| Parc Thompson ⚠️ | Hudson | 3 |
| Parc de la Famille ⚠️ | Ville de l'Île-Perrot › Île Perrot | 2 |
| Parc Shamrock ⚠️ | Pincourt › Île Perrot | 2 |
| Parc Donat-Bouthillier ⚠️ | Terrasse-Vaudreuil › Île Perrot | 2 |
| Parc Bédard ⚠️ | Saint-Lazare | 2 |
| Parc des Cèdres (2) ⚠️ | Les Cèdres | 2 |
| Parc de Pointe-des-Cascades ⚠️ | Pointe-des-Cascades | 2 |
| Parc Saint-Thomas ⚠️ | Hudson | 2 |
| Parc des Mésanges (3) ⚠️ | Notre-Dame-de-l'Île-Perrot › Île Perrot | 2 |
| Parc Paul-Gérin-Lajoie ⚠️ | Vaudreuil-Dorion | 2 |
| Parc de l'Île-Bray ⚠️ | Vaudreuil-Dorion | 2 |
| Parc Saint-Pierre (5) ⚠️ | Pointe-des-Cascades | 2 |
| Parc de la Maison-Valois ⚠️ | Vaudreuil-Dorion | 2 |
| Parc des Cèdres ⚠️ | Les Cèdres | 1 |
| Parc Trudeau ⚠️ | Vaudreuil-Dorion | 1 |
| Parc Sainte-Trinité ⚠️ | Vaudreuil-Dorion | 1 |
| Parc de Vaudreuil-Dorion ⚠️ | Vaudreuil-Dorion | 1 |
| Parc Esther-Blondin ⚠️ | Vaudreuil-Dorion | 1 |
| Parc de la Seigneurie (3) ⚠️ | Vaudreuil-Dorion | 1 |
| Parc du Grand-Pré ⚠️ | Saint-Lazare | 1 |
| Parc de la Vallée-Chaline ⚠️ | Saint-Lazare | 1 |
| Parc Benson ⚠️ | Hudson | 1 |
| Parc Taillon ⚠️ | Pincourt › Île Perrot | 1 |
| Parc Castonguay ⚠️ | Vaudreuil-Dorion | 1 |
| Parc de Cedarbrook ⚠️ | Saint-Lazare | 1 |
| Parc de Saddlebrook ⚠️ | Saint-Lazare | 1 |
| Parc Carrefour Notre-Dame ⚠️ | Notre-Dame-de-l'Île-Perrot › Île Perrot | 1 |
| Parc Saint-Jean-Baptiste (2) ⚠️ | Vaudreuil-Dorion | 1 |
| Parc de la Belle-Plage ⚠️ | Vaudreuil-Dorion | 1 |
| Parc 22e Avenue ⚠️ | Ville de l'Île-Perrot › Île Perrot | 1 |
| Parc Saint-Michel (2) ⚠️ | Vaudreuil-Dorion | 1 |
| Parc Lorne-Worsley (2) ⚠️ | Vaudreuil-Dorion | 1 |
| Parc du Ruisselet ⚠️ | Vaudreuil-Dorion | 1 |
| Parc des Narcisses ⚠️ | Vaudreuil-Dorion | 1 |
| Parc Marier ⚠️ | Vaudreuil-Dorion | 1 |
| Parc des Pins (4) ⚠️ | Saint-Lazare | 1 |
| Parc Champlain (4) ⚠️ | Les Cèdres | 1 |
| Parc des Fauvettes ⚠️ | Notre-Dame-de-l'Île-Perrot › Île Perrot | 1 |
| Parc de Vaudreuil-sur-le-Lac ⚠️ | Vaudreuil-sur-le-Lac | 1 |
| Parc des Cèdres (4) ⚠️ | Les Cèdres | 1 |
| Parc des Martins-Pêcheurs ⚠️ | Notre-Dame-de-l'Île-Perrot › Île Perrot | 1 |
| Parc des Mouettes ⚠️ | Notre-Dame-de-l'Île-Perrot › Île Perrot | 1 |
| Parc des Tourterelles ⚠️ | Notre-Dame-de-l'Île-Perrot › Île Perrot | 1 |
| Parc des Citoyens (2) ⚠️ | Ville de l'Île-Perrot › Île Perrot | 1 |
| Parc des Colibris ⚠️ | Ville de l'Île-Perrot › Île Perrot | 1 |
| Parc Bellevue ⚠️ | Pincourt › Île Perrot | 1 |
| Parc Rousseau ⚠️ | Pincourt › Île Perrot | 1 |
| Parc de Pincourt (3) ⚠️ | Pincourt › Île Perrot | 1 |
| Parc de la Rhapsodie ⚠️ | Saint-Lazare | 1 |
| Parc de Vaudreuil-Dorion (3) ⚠️ | Vaudreuil-Dorion | 1 |
| Parc de Bel-Air ⚠️ | Vaudreuil-Dorion | 1 |
| Parc Quinchien ⚠️ | Vaudreuil-Dorion | 1 |
| Parc de Vaudreuil-Dorion (5) ⚠️ | Vaudreuil-Dorion | 1 |
| Parc de Vaudreuil-Dorion (6) ⚠️ | Vaudreuil-Dorion | 1 |
| Parc Mozart ⚠️ | Vaudreuil-Dorion | 1 |
| Parc Vivaldi ⚠️ | Vaudreuil-Dorion | 1 |
| Parc de la Canardière ⚠️ | Vaudreuil-Dorion | 1 |
| Parc Jack Layton ⚠️ | Hudson | 1 |
| Royal Oak Tennis Club ⚠️ | Hudson | 1 |
| Parc de Hudson ⚠️ | Hudson | 1 |
| Parc Saint-Féréol ⚠️ | Les Cèdres | 1 |
| Parc du Suroît ⚠️ | Pincourt › Île Perrot | 1 |
| Parc Daoust ⚠️ | Les Cèdres | 1 |

95 parc(s) plus petits qu'une cellule ne sont pas listés : la carte les dessine, mais ils n'offrent aucune cellule.

⚠️ 171 parc(s) hors de la fenêtre 10–125 cellules (170 trop petit(s), 1 trop grand(s)) : affichés sur la carte, mais ils ne peuvent pas servir de cible à un défi.

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
