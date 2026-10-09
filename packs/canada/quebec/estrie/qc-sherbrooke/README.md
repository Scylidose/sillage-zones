# Sherbrooke

Pack `qc-sherbrooke` · version 1.0.0 · grille 200 m · Canada › Québec › Estrie

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 17 893 |
| dont restreintes (aéroport, militaire, prison) | 0 |
| dont sans chemin (aucune voie à moins de 60 m) | 1 351 |
| dont en forêt, sans chemin non plus | 3 047 |
| dont traversées par un cours d'eau, sans chemin non plus | 327 |
| Cellules retirées par le masque d'eau | 693 |
| Villes | 1 |
| Arrondissements et quartiers | 6 |
| Îles | 0 |
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
| **Sans chemin** | parmi les comptées, celles qu'aucune voie n'approche à moins de 60 m, hors bois et hors cours d'eau — l'utilisateur peut les marquer inaccessibles zone par zone, elles restent comptées tant qu'il ne le fait pas |

Les cellules boisées et celles que traverse un cours d'eau forment deux autres catégories, marquables de la même façon et comptées dans le résumé ci-dessus. Toutes trois exigent la même chose — aucune voie à moins de 60 m — et sont disjointes : une cellule desservie par un sentier reste accessible, quoi qu'elle contienne.

## Villes (1)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Sans chemin | Parcs |
|---|---:|---:|---:|---:|---:|---:|---:|
| Sherbrooke | 18 586 | 693 | 17 893 | 0 | **17 893** | 1 351 (8 %) | 173 |

## Arrondissements et quartiers (6)

| Zone | Ville | Brut | Eau | Sans eau | Restr. | Comptées | Sans chemin | Parcs |
|---|---|---:|---:|---:|---:|---:|---:|---:|
| Rock Forest–Saint-Élie–Deauville | sherbrooke | 7 892 | 387 | 7 505 | 0 | **7 505** | 533 (7 %) | 30 |
| Brompton | sherbrooke | 4 058 | 99 | 3 959 | 0 | **3 959** | 648 (16 %) | 10 |
| Fleurimont | sherbrooke | 2 179 | 39 | 2 140 | 0 | **2 140** | 56 (3 %) | 50 |
| Jacques-Cartier | sherbrooke | 1 551 | 42 | 1 509 | 0 | **1 509** | 12 (1 %) | 31 |
| Le Mont-Bellevue | sherbrooke | 1 444 | 50 | 1 394 | 0 | **1 394** | 11 (1 %) | 41 |
| Lennoxville | sherbrooke | 1 462 | 76 | 1 386 | 0 | **1 386** | 91 (7 %) | 11 |

## Parcs (175)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Parc du Mont-Bellevue | Sherbrooke › Le Mont-Bellevue | 96 |
| Parc du Bois-Beckett | Sherbrooke › Jacques-Cartier | 70 |
| Base de plein air André-Nadeau | Sherbrooke › Rock Forest–Saint-Élie–Deauville | 26 |
| Parc Armand-Duplessis | Sherbrooke › Fleurimont | 24 |
| Parc Marais Réal-D.-Carbonneau | Sherbrooke › Fleurimont | 21 |
| Parc Central | Sherbrooke › Rock Forest–Saint-Élie–Deauville | 19 |
| Parc des Deux-Ruisseaux | Sherbrooke › Le Mont-Bellevue | 18 |
| Parc Victoria | Sherbrooke › Fleurimont | 15 |
| Parc Jacques-Cartier | Sherbrooke › Jacques-Cartier | 12 |
| Parc Sylvie-Daigle | Sherbrooke › Fleurimont | 12 |
| boisé Lucien-Blanchard ⚠️ | Sherbrooke › Le Mont-Bellevue | 9 |
| Parc André-Viger ⚠️ | Sherbrooke › Jacques-Cartier | 9 |
| Parc Quintal ⚠️ | Sherbrooke › Fleurimont | 8 |
| Parc Belvédère ⚠️ | Sherbrooke › Le Mont-Bellevue | 6 |
| Parc Lucien-Blanchard ⚠️ | Sherbrooke › Le Mont-Bellevue | 6 |
| Parc Atto-Beaver ⚠️ | Sherbrooke › Lennoxville | 6 |
| Parc Walter-Camden ⚠️ | Sherbrooke › Fleurimont | 5 |
| Parc Andrew-Sangster ⚠️ | Sherbrooke › Le Mont-Bellevue | 4 |
| Parc du Marquis-de-Montcalm ⚠️ | Sherbrooke › Jacques-Cartier | 4 |
| Parc Paul-Marin ⚠️ | Sherbrooke › Le Mont-Bellevue | 3 |
| Parc Bureau ⚠️ | Sherbrooke › Fleurimont | 3 |
| Parc du Mi-Vallon ⚠️ | Sherbrooke › Rock Forest–Saint-Élie–Deauville | 3 |
| Parc Nault ⚠️ | Sherbrooke › Brompton | 3 |
| Parc de la Plage-Municipale ⚠️ | Sherbrooke › Rock Forest–Saint-Élie–Deauville | 3 |
| Parc de la Kruger ⚠️ | Sherbrooke › Brompton | 3 |
| Parc du Barrage ⚠️ | Sherbrooke › Le Mont-Bellevue | 3 |
| Boisé de la Sauvagine ⚠️ | Sherbrooke › Jacques-Cartier | 3 |
| Parc de Saint-Alphonse-de-Liguori ⚠️ | Sherbrooke › Jacques-Cartier | 2 |
| Parc de Sherbrooke ⚠️ | Sherbrooke › Le Mont-Bellevue | 2 |
| Parc Gilles-Charland ⚠️ | Sherbrooke › Fleurimont | 2 |
| Parc Maillé ⚠️ | Sherbrooke › Fleurimont | 2 |
| Parc de Saint-Charles-Garnier ⚠️ | Sherbrooke › Jacques-Cartier | 2 |
| Parc de Marie-Médiatrice ⚠️ | Sherbrooke › Le Mont-Bellevue | 2 |
| Parc du Domaine-Howard ⚠️ | Sherbrooke › Jacques-Cartier | 2 |
| Parc des Jardins-Fleuris ⚠️ | Sherbrooke › Fleurimont | 2 |
| Parc Couturier ⚠️ | Sherbrooke › Fleurimont | 2 |
| Parc Desranleau ⚠️ | Sherbrooke › Fleurimont | 2 |
| Parc du Mena'Sen ⚠️ | Sherbrooke › Fleurimont | 2 |
| Parc Centennial ⚠️ | Sherbrooke › Lennoxville | 2 |
| Parc des Quatre-Pins ⚠️ | Sherbrooke › Jacques-Cartier | 2 |
| Parc Thérèse-Lecompte ⚠️ | Sherbrooke › Rock Forest–Saint-Élie–Deauville | 2 |
| Parc Dorilas-Gagnon ⚠️ | Sherbrooke › Brompton | 2 |
| Parc de la Butte-aux-Bouleaux ⚠️ | Sherbrooke › Rock Forest–Saint-Élie–Deauville | 2 |
| Parc de Liège ⚠️ | Sherbrooke › Jacques-Cartier | 1 |
| Parc de Saint-Boniface ⚠️ | Sherbrooke › Jacques-Cartier | 1 |
| Boisé du Champ des Buttes ⚠️ | Sherbrooke › Le Mont-Bellevue | 1 |
| Parc de Sherbrooke (2) ⚠️ | Sherbrooke › Le Mont-Bellevue | 1 |
| Parc du Frère-Théode ⚠️ | Sherbrooke › Le Mont-Bellevue | 1 |
| Parc Adrien-Cambron ⚠️ | Sherbrooke › Fleurimont | 1 |
| Parc des Optimistes ⚠️ | Sherbrooke › Fleurimont | 1 |
| Parc de Notre-Dame-du-Rosaire ⚠️ | Sherbrooke › Le Mont-Bellevue | 1 |
| Parc Arsène-Goyette ⚠️ | Sherbrooke › Le Mont-Bellevue | 1 |
| Parc de Marie-Reine-du-Monde ⚠️ | Sherbrooke › Fleurimont | 1 |
| Parc Philippe-Desranleau ⚠️ | Sherbrooke › Fleurimont | 1 |
| Parc des Pyrénées ⚠️ | Sherbrooke › Fleurimont | 1 |
| Parc du Villageois ⚠️ | Sherbrooke › Rock Forest–Saint-Élie–Deauville | 1 |
| Parc Normand-Dusseault ⚠️ | Sherbrooke › Fleurimont | 1 |
| Parc de Sherbrooke (10) ⚠️ | Sherbrooke › Le Mont-Bellevue | 1 |
| Parc de l'Escarpe ⚠️ | Sherbrooke › Le Mont-Bellevue | 1 |
| Parc Judes-O.-Camirand ⚠️ | Sherbrooke › Le Mont-Bellevue | 1 |
| Parc de la Laurentie ⚠️ | Sherbrooke › Jacques-Cartier | 1 |
| Parc Hélène-Boullé ⚠️ | Sherbrooke › Jacques-Cartier | 1 |
| Parc de l'Ancienne-Prison ⚠️ | Sherbrooke › Jacques-Cartier | 1 |
| Parc Lennoxville Optimist ⚠️ | Sherbrooke › Lennoxville | 1 |
| Parc Olivier-Chauveau ⚠️ | Sherbrooke › Jacques-Cartier | 1 |
| Parc Jules-Richard ⚠️ | Sherbrooke › Rock Forest–Saint-Élie–Deauville | 1 |
| Boisé du Portage ⚠️ | Sherbrooke › Rock Forest–Saint-Élie–Deauville | 1 |
| Parc Charles-Émile-Gadbois ⚠️ | Sherbrooke › Rock Forest–Saint-Élie–Deauville | 1 |
| Parc Beaulieu ⚠️ | Sherbrooke › Rock Forest–Saint-Élie–Deauville | 1 |
| Parc Yousuf-Karsh ⚠️ | Sherbrooke › Rock Forest–Saint-Élie–Deauville | 1 |
| Parc Ernest-Bergeron ⚠️ | Sherbrooke › Brompton | 1 |
| Parc de la Rive ⚠️ | Sherbrooke › Brompton | 1 |
| Parc du Plateau ⚠️ | Sherbrooke › Rock Forest–Saint-Élie–Deauville | 1 |
| Parc Alfred-Élie-Dufresne ⚠️ | Sherbrooke › Le Mont-Bellevue | 1 |

101 parc(s) plus petits qu'une cellule ne sont pas listés : la carte les dessine, mais ils n'offrent aucune cellule.

⚠️ 165 parc(s) hors de la fenêtre 10–125 cellules (165 trop petit(s), 0 trop grand(s)) : affichés sur la carte, mais ils ne peuvent pas servir de cible à un défi.

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
