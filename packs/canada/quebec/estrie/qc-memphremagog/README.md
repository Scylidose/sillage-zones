# Memphrémagog (Estrie)

Pack `qc-memphremagog` · version 1.0.0 · grille 200 m · Canada › Québec › Estrie

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 66 301 |
| dont restreintes (aéroport, militaire, prison) | 37 |
| dont sans chemin (aucune voie à moins de 60 m) | 4 205 |
| dont en forêt, sans chemin non plus | 28 153 |
| dont traversées par un cours d'eau, sans chemin non plus | 1 108 |
| Cellules retirées par le masque d'eau | 6 404 |
| Villes | 17 |
| Arrondissements et quartiers | 0 |
| Îles | 0 |
| Parcs | 106 |

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

## Villes (17)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Sans chemin | Parcs |
|---|---:|---:|---:|---:|---:|---:|---:|
| Potton | 13 910 | 872 | 13 038 | 0 | **13 038** | 634 (5 %) | 8 |
| Magog | 8 424 | 1 154 | 7 270 | 0 | **7 270** | 395 (5 %) | 37 |
| Orford | 7 474 | 553 | 6 921 | 37 | **6 884** | 172 (2 %) | 6 |
| Stanstead (Canton) | 6 800 | 1 113 | 5 687 | 0 | **5 687** | 396 (7 %) | 2 |
| Sainte-Catherine-de-Hatley | 4 991 | 639 | 4 352 | 0 | **4 352** | 460 (11 %) | 6 |
| Bolton-Est | 4 078 | 124 | 3 954 | 0 | **3 954** | 70 (2 %) | 3 |
| Ogden | 4 188 | 455 | 3 733 | 0 | **3 733** | 528 (14 %) | 1 |
| Austin | 4 332 | 612 | 3 720 | 0 | **3 720** | 178 (5 %) | 4 |
| Eastman | 3 889 | 198 | 3 691 | 0 | **3 691** | 38 (1 %) | 9 |
| Hatley (Canton) | 3 750 | 123 | 3 627 | 0 | **3 627** | 293 (8 %) | 1 |
| Stukely-Sud | 3 207 | 17 | 3 190 | 0 | **3 190** | 195 (6 %) | 1 |
| Hatley | 3 324 | 284 | 3 040 | 0 | **3 040** | 712 (23 %) | 1 |
| Saint-Étienne-de-Bolton | 2 471 | 54 | 2 417 | 0 | **2 417** | 33 (1 %) | 1 |
| Stanstead (Ville) | 1 124 | 16 | 1 108 | 0 | **1 108** | 79 (7 %) | 8 |
| Ayer's Cliff | 389 | 111 | 278 | 0 | **278** | 13 (5 %) | 7 |
| North Hatley | 227 | 63 | 164 | 0 | **164** | 1 (1 %) | 6 |
| Saint-Benoît-du-Lac | 127 | 16 | 111 | 0 | **111** | 8 (7 %) |  |

## Parcs (106)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Parc national du Mont-Orford ⚠️ | Orford | 3 400 |
| Réserve naturelle des Montagnes-Vertes ⚠️ | Potton | 1 889 |
| Réserve naturelle du Mont-Éléphant | Potton | 122 |
| Réserve naturelle des Collines-de-Bolton-Est | Bolton-Est | 91 |
| Marais de la Rivière aux Cerises | Magog | 66 |
| Réserve écologique de la Vallée-du-Ruiter | Potton | 64 |
| Réserve naturelle Maurice-Bessette | Orford | 23 |
| Parc du Cercle des Pierres ⚠️ | Stanstead (Ville) | 8 |
| Parc de la rivière Missisquoi Nord ⚠️ | Potton | 5 |
| Parc de l'Est ⚠️ | Magog | 5 |
| Site de la SACS ⚠️ | Ayer's Cliff | 5 |
| Club Aramis ⚠️ | Magog | 4 |
| Parc d'Omerville ⚠️ | Magog | 4 |
| Parc de la Pointe-Merry ⚠️ | Magog | 4 |
| Parc de la Plage des Cantons ⚠️ | Magog | 3 |
| Parc le Montagnais ⚠️ | Orford | 2 |
| Parc des Loisirs ⚠️ | Austin | 2 |
| Beebe Memorial Park ⚠️ | Stanstead (Ville) | 2 |
| Parc des Générations ⚠️ | Stanstead (Ville) | 2 |
| Halte de la Rivière aux Cerises ⚠️ | Orford | 2 |
| parc de la Baie-de-Magog ⚠️ | Magog | 2 |
| APS ⚠️ | Magog | 2 |
| Parc de Eastman (4) ⚠️ | Eastman | 2 |
| Parc Banting Holmes ⚠️ | Stanstead (Ville) | 1 |
| Parc Horan ⚠️ | Magog | 1 |
| Parc Honoré-Langlois ⚠️ | Sainte-Catherine-de-Hatley | 1 |
| Parc no 2 ⚠️ | Magog | 1 |
| Marina no 1 ⚠️ | Magog | 1 |
| Parc de Stanstead (Canton) (2) ⚠️ | Stanstead (Canton) | 1 |
| Parc Gaston-Giguère ⚠️ | Hatley | 1 |
| Parc des pionniers ⚠️ | Ayer's Cliff | 1 |
| Parc Jonathan-Martel ⚠️ | Sainte-Catherine-de-Hatley | 1 |
| Parc des Vétérans (2) ⚠️ | North Hatley | 1 |
| Parc de la Plage ⚠️ | North Hatley | 1 |
| Parc De La Rivière ⚠️ | North Hatley | 1 |
| Parc de Bolton-Est ⚠️ | Bolton-Est | 1 |
| Parc Weir ⚠️ | Ogden | 1 |
| Parc Terrio ⚠️ | Bolton-Est | 1 |
| Parc Monseigneur-Vel ⚠️ | Sainte-Catherine-de-Hatley | 1 |
| Parc Wilfrid-Lareau ⚠️ | Sainte-Catherine-de-Hatley | 1 |
| Parc de la plage Massawippi ⚠️ | Ayer's Cliff | 1 |
| Parc Scowen ⚠️ | North Hatley | 1 |
| Parc Maurice-Théroux ⚠️ | Magog | 1 |
| Parc Yvon-Laramée ⚠️ | Eastman | 1 |
| Parc des Pionniers ⚠️ | Magog | 1 |
| Parc de Ayer's Cliff (2) ⚠️ | Ayer's Cliff | 1 |
| Parc de la Grève ⚠️ | Eastman | 1 |
| Parc Shappie Trough ⚠️ | Austin | 1 |
| Parc Chaumière ⚠️ | Hatley (Canton) | 1 |
| Réserve écologique de la Mine-aux-Pipistrelles ⚠️ | Potton | 1 |
| Parc du Ruisseau ⚠️ | Magog | 1 |
| Parc des Patriotes ⚠️ | Magog | 1 |
| Parc General-Vanier ⚠️ | Magog | 1 |
| Parc des Cerisiers ⚠️ | Magog | 1 |
| APPL ⚠️ | Magog | 1 |
| APS (3) ⚠️ | Magog | 1 |
| Parc Municipal ⚠️ | Saint-Étienne-de-Bolton | 1 |

49 parc(s) plus petits qu'une cellule ne sont pas listés : la carte les dessine, mais ils n'offrent aucune cellule.

⚠️ 101 parc(s) hors de la fenêtre 10–125 cellules (99 trop petit(s), 2 trop grand(s)) : affichés sur la carte, mais ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| military | 37 |
| airport | 0 |
| prison | 0 |
| **Total déclaré** | **37** |
| dont dans une zone de ce territoire | 37 |


### Zones concernées

| Zone | Cellules exclues |
|---|---:|
| Orford | 37 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
