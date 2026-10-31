# Paris

Pack `fr-paris` · version 1.0.0 · grille 200 m · France › Île-de-France

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 5 915 |
| dont restreintes (aéroport, militaire, prison) | 31 |
| dont sans chemin (aucune voie à moins de 60 m) | 0 |
| dont en forêt, sans chemin non plus | 1 |
| dont traversées par un cours d'eau, sans chemin non plus | 0 |
| Cellules retirées par le masque d'eau | 166 |
| Villes | 1 |
| Arrondissements et quartiers | 20 |
| Îles | 0 |
| Parcs | 1 805 |

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
| Paris | 6 081 | 166 | 5 915 | 31 | **5 884** |  | 1783 |

## Arrondissements et quartiers (20)

| Zone | Ville | Brut | Eau | Sans eau | Restr. | Comptées | Sans chemin | Parcs |
|---|---|---:|---:|---:|---:|---:|---:|---:|
| 12e arrondissement de Paris | paris-75 | 946 | 30 | 916 | 11 | **905** |  | 384 |
| 16e arrondissement de Paris | paris-75 | 944 | 47 | 897 | 0 | **897** |  | 643 |
| 15e arrondissement de Paris | paris-75 | 488 | 14 | 474 | 9 | **465** |  | 71 |
| 13e arrondissement de Paris | paris-75 | 412 | 12 | 400 | 0 | **400** |  | 80 |
| 19e arrondissement de Paris | paris-75 | 390 | 9 | 381 | 0 | **381** |  | 94 |
| 20e arrondissement de Paris | paris-75 | 349 | 1 | 348 | 3 | **345** |  | 69 |
| 18e arrondissement de Paris | paris-75 | 348 | 0 | 348 | 0 | **348** |  | 69 |
| 17e arrondissement de Paris | paris-75 | 327 | 1 | 326 | 0 | **326** |  | 61 |
| 14e arrondissement de Paris | paris-75 | 322 | 0 | 322 | 0 | **322** |  | 67 |
| 7e arrondissement de Paris | paris-75 | 239 | 18 | 221 | 8 | **213** |  | 29 |
| 8e arrondissement de Paris | paris-75 | 220 | 1 | 219 | 0 | **219** |  | 31 |
| 11e arrondissement de Paris | paris-75 | 213 | 2 | 211 | 0 | **211** |  | 26 |
| 10e arrondissement de Paris | paris-75 | 160 | 3 | 157 | 0 | **157** |  | 19 |
| 5e arrondissement de Paris | paris-75 | 146 | 4 | 142 | 0 | **142** |  | 42 |
| 9e arrondissement de Paris | paris-75 | 129 | 0 | 129 | 0 | **129** |  | 6 |
| 6e arrondissement de Paris | paris-75 | 125 | 2 | 123 | 0 | **123** |  | 40 |
| 1er arrondissement de Paris | paris-75 | 106 | 8 | 98 | 0 | **98** |  | 6 |
| 4e arrondissement de Paris | paris-75 | 91 | 14 | 77 | 0 | **77** |  | 22 |
| 3e arrondissement de Paris | paris-75 | 69 | 0 | 69 | 0 | **69** |  | 23 |
| 2e arrondissement de Paris | paris-75 | 59 | 0 | 59 | 0 | **59** |  | 1 |

## Parcs (1805)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Parc de Paris (98) ⚠️ | Paris › 12e arrondissement de Paris | 543 |
| Bois de Vincennes ⚠️ | Paris › 12e arrondissement de Paris | 543 |
| Bois de Boulogne ⚠️ | Paris › 16e arrondissement de Paris | 446 |
| Forêt de Paris (888) | Paris › 16e arrondissement de Paris | 27 |
| Forêt de Paris (889) | Paris › 12e arrondissement de Paris | 26 |
| Forêt de Paris (890) | Paris › 16e arrondissement de Paris | 25 |
| Bois de Paris (172) | Paris › 16e arrondissement de Paris | 25 |
| Parc de la Villette | Paris › 19e arrondissement de Paris | 18 |
| Parc Floral de Paris | Paris › 12e arrondissement de Paris | 17 |
| Forêt de Paris (899) | Paris › 16e arrondissement de Paris | 17 |
| Cité Universitaire - Parc Est | Paris › 14e arrondissement de Paris | 16 |
| Champ de Mars | Paris › 7e arrondissement de Paris | 15 |
| Parc des Buttes-Chaumont | Paris › 19e arrondissement de Paris | 15 |
| Parc de Bagatelle | Paris › 16e arrondissement de Paris | 15 |
| Forêt de Paris (140) | Paris › 16e arrondissement de Paris | 14 |
| Jardin des Plantes | Paris › 5e arrondissement de Paris | 13 |
| Bois de Paris (177) | Paris › 16e arrondissement de Paris | 13 |
| Jardin des Tuileries | Paris › 1er arrondissement de Paris | 12 |
| Jardin du Luxembourg | Paris › 6e arrondissement de Paris | 12 |
| Parc Suzanne Lenglen | Paris › 15e arrondissement de Paris | 10 |
| Forêt de Paris (217) | Paris › 16e arrondissement de Paris | 10 |
| Forêt de Paris (137) ⚠️ | Paris › 12e arrondissement de Paris | 9 |
| Forêt de Paris (153) ⚠️ | Paris › 12e arrondissement de Paris | 9 |
| Forêt de Paris (176) ⚠️ | Paris › 12e arrondissement de Paris | 9 |
| Forêt de Paris (148) ⚠️ | Paris › 16e arrondissement de Paris | 8 |
| Parc Montsouris ⚠️ | Paris › 14e arrondissement de Paris | 8 |
| Jardins du Trocadéro ⚠️ | Paris › 16e arrondissement de Paris | 8 |
| Forêt de Paris (13) ⚠️ | Paris › 12e arrondissement de Paris | 7 |
| Arboretum de Paris ⚠️ | Paris › 12e arrondissement de Paris | 7 |
| Forêt de Paris (192) ⚠️ | Paris › 12e arrondissement de Paris | 7 |
| Parc de Bercy ⚠️ | Paris › 12e arrondissement de Paris | 6 |
| Pelouse de Reuilly ⚠️ | Paris › 12e arrondissement de Paris | 6 |
| Forêt de Paris (65) ⚠️ | Paris › 12e arrondissement de Paris | 6 |
| Forêt de Paris (136) ⚠️ | Paris › 12e arrondissement de Paris | 6 |
| Forêt de Paris (147) ⚠️ | Paris › 16e arrondissement de Paris | 6 |
| Forêt de Paris (150) ⚠️ | Paris › 16e arrondissement de Paris | 6 |
| Forêt de Paris (152) ⚠️ | Paris › 16e arrondissement de Paris | 6 |
| Bois de Paris (21) ⚠️ | Paris › 16e arrondissement de Paris | 6 |
| Parc André Citroën ⚠️ | Paris › 15e arrondissement de Paris | 6 |
| Forêt de Paris (178) ⚠️ | Paris › 12e arrondissement de Paris | 6 |
| Forêt de Paris (258) ⚠️ | Paris › 16e arrondissement de Paris | 6 |
| Parc Clichy-Batignolles Martin Luther King ⚠️ | Paris › 17e arrondissement de Paris | 6 |
| Forêt de Paris (16) ⚠️ | Paris › 12e arrondissement de Paris | 5 |
| Forêt de Paris (80) ⚠️ | Paris › 12e arrondissement de Paris | 5 |
| Forêt de Paris (82) ⚠️ | Paris › 12e arrondissement de Paris | 5 |
| Forêt de Paris (180) ⚠️ | Paris › 12e arrondissement de Paris | 5 |
| Jardin du Ranelagh ⚠️ | Paris › 16e arrondissement de Paris | 5 |
| Parc Monceau ⚠️ | Paris › 8e arrondissement de Paris | 5 |
| Forêt de Paris (895) ⚠️ | Paris › 16e arrondissement de Paris | 5 |
| Forêt de Paris (898) ⚠️ | Paris › 12e arrondissement de Paris | 5 |
| Forêt de Paris (901) ⚠️ | Paris › 16e arrondissement de Paris | 5 |
| Forêt de Paris (10) ⚠️ | Paris › 12e arrondissement de Paris | 4 |
| Jardin Tino Rossi - Musée de la Sculpture en Plein Air ⚠️ | Paris › 5e arrondissement de Paris | 4 |
| Forêt de Paris (17) ⚠️ | Paris › 12e arrondissement de Paris | 4 |
| Forêt de Paris (18) ⚠️ | Paris › 12e arrondissement de Paris | 4 |
| Forêt de Paris (21) ⚠️ | Paris › 12e arrondissement de Paris | 4 |
| Enclos N°189 ⚠️ | Paris › 12e arrondissement de Paris | 4 |
| Forêt de Paris (108) ⚠️ | Paris › 12e arrondissement de Paris | 4 |
| Parc Georges Brassens ⚠️ | Paris › 15e arrondissement de Paris | 4 |
| Forêt de Paris (175) ⚠️ | Paris › 12e arrondissement de Paris | 4 |
| Cité Universitaire - Parc Ouest ⚠️ | Paris › 14e arrondissement de Paris | 4 |
| Forêt de Paris (218) ⚠️ | Paris › 16e arrondissement de Paris | 4 |
| Parc de la Butte du Chapeau Rouge ⚠️ | Paris › 19e arrondissement de Paris | 3 |
| Parc Kellermann ⚠️ | Paris › 13e arrondissement de Paris | 3 |
| Forêt de Paris (15) ⚠️ | Paris › 12e arrondissement de Paris | 3 |
| Réserve Forestière ⚠️ | Paris › 12e arrondissement de Paris | 3 |
| Parc de Choisy ⚠️ | Paris › 13e arrondissement de Paris | 3 |
| Forêt de Paris (84) ⚠️ | Paris › 12e arrondissement de Paris | 3 |
| Forêt de Paris (89) ⚠️ | Paris › 12e arrondissement de Paris | 3 |
| Forêt de Paris (95) ⚠️ | Paris › 12e arrondissement de Paris | 3 |
| Forêt de Paris (118) ⚠️ | Paris › 12e arrondissement de Paris | 3 |
| Forêt de Paris (122) ⚠️ | Paris › 12e arrondissement de Paris | 3 |
| Forêt de Paris (138) ⚠️ | Paris › 12e arrondissement de Paris | 3 |
| Forêt de Paris (139) ⚠️ | Paris › 12e arrondissement de Paris | 3 |
| Jardin des serres d’Auteuil ⚠️ | Paris › 16e arrondissement de Paris | 3 |
| Forêt de Paris (157) ⚠️ | Paris › 12e arrondissement de Paris | 3 |
| Jardin Nelson Mandela ⚠️ | Paris › 1er arrondissement de Paris | 3 |
| Forêt de Paris (164) ⚠️ | Paris › 12e arrondissement de Paris | 3 |
| Forêt de Paris (177) ⚠️ | Paris › 12e arrondissement de Paris | 3 |
| Forêt de Paris (267) ⚠️ | Paris › 16e arrondissement de Paris | 3 |
| Forêt de Paris (834) ⚠️ | Paris › 12e arrondissement de Paris | 3 |
| Bois de Paris (93) ⚠️ | Paris › 12e arrondissement de Paris | 3 |
| Jardins de l'Avenue Foch ⚠️ | Paris › 16e arrondissement de Paris | 3 |
| Les Jardins d'Éole ⚠️ | Paris › 18e arrondissement de Paris | 3 |
| Île Nord ⚠️ | Paris › 12e arrondissement de Paris | 2 |
| Forêt de Paris (7) ⚠️ | Paris › 12e arrondissement de Paris | 2 |
| Square Sarah Bernhardt ⚠️ | Paris › 20e arrondissement de Paris | 2 |
| Forêt de Paris (19) ⚠️ | Paris › 12e arrondissement de Paris | 2 |
| Square de la Marseillaise ⚠️ | Paris › 19e arrondissement de Paris | 2 |
| Forêt de Paris (39) ⚠️ | Paris › 12e arrondissement de Paris | 2 |
| Forêt de Paris (40) ⚠️ | Paris › 12e arrondissement de Paris | 2 |
| Forêt de Paris (42) ⚠️ | Paris › 12e arrondissement de Paris | 2 |
| Forêt de Paris (47) ⚠️ | Paris › 12e arrondissement de Paris | 2 |
| Forêt de Paris (83) ⚠️ | Paris › 12e arrondissement de Paris | 2 |
| Forêt de Paris (86) ⚠️ | Paris › 12e arrondissement de Paris | 2 |
| Forêt de Paris (98) ⚠️ | Paris › 12e arrondissement de Paris | 2 |
| Forêt de Paris (99) ⚠️ | Paris › 12e arrondissement de Paris | 2 |
| Forêt de Paris (110) ⚠️ | Paris › 12e arrondissement de Paris | 2 |
| Forêt de Paris (117) ⚠️ | Paris › 12e arrondissement de Paris | 2 |
| Forêt de Paris (119) ⚠️ | Paris › 12e arrondissement de Paris | 2 |
| Forêt de Paris (125) ⚠️ | Paris › 12e arrondissement de Paris | 2 |
| Forêt de Paris (133) ⚠️ | Paris › 12e arrondissement de Paris | 2 |
| Forêt de Paris (135) ⚠️ | Paris › 12e arrondissement de Paris | 2 |
| Square Louise Michel ⚠️ | Paris › 18e arrondissement de Paris | 2 |
| Square du Serment de Koufra ⚠️ | Paris › 14e arrondissement de Paris | 2 |
| Forêt de Paris (182) ⚠️ | Paris › 12e arrondissement de Paris | 2 |
| La Petite Ceinture du 15e ⚠️ | Paris › 15e arrondissement de Paris | 2 |
| La Petite Ceinture du 14e ⚠️ | Paris › 14e arrondissement de Paris | 2 |
| Forêt de Paris (216) ⚠️ | Paris › 16e arrondissement de Paris | 2 |
| Forêt de Paris (242) ⚠️ | Paris › 16e arrondissement de Paris | 2 |
| Forêt de Paris (424) ⚠️ | Paris › 16e arrondissement de Paris | 2 |
| Forêt de Paris (786) ⚠️ | Paris › 16e arrondissement de Paris | 2 |
| Parc Aretha Franklin ⚠️ | Paris › 20e arrondissement de Paris | 2 |
| Le Pré Catelan ⚠️ | Paris › 16e arrondissement de Paris | 2 |
| Forêt de Paris (891) ⚠️ | Paris › 16e arrondissement de Paris | 2 |
| Parc Chapelle-Charbon ⚠️ | Paris › 18e arrondissement de Paris | 2 |
| Jardins des Champs-Élysées ⚠️ | Paris › 8e arrondissement de Paris | 2 |
| Square Alexandre et René-Parodi ⚠️ | Paris › 16e arrondissement de Paris | 2 |
| Île du Belvédère ⚠️ | Paris › 19e arrondissement de Paris | 1 |
| Jardin du Palais Royal ⚠️ | Paris › 1er arrondissement de Paris | 1 |
| Square Violet ⚠️ | Paris › 15e arrondissement de Paris | 1 |
| Jardin Caroline Aigle ⚠️ | Paris › 15e arrondissement de Paris | 1 |
| Square Frédéric Bazille ⚠️ | Paris › 14e arrondissement de Paris | 1 |
| Square Pablo Casals ⚠️ | Paris › 15e arrondissement de Paris | 1 |
| Square des Missions Étrangères ⚠️ | Paris › 7e arrondissement de Paris | 1 |
| Jardin Villemin - Mahsa Jîna Amini ⚠️ | Paris › 10e arrondissement de Paris | 1 |
| Jardin Atlantique ⚠️ | Paris › 15e arrondissement de Paris | 1 |
| Esplanade Gaston Monnerville ⚠️ | Paris › 6e arrondissement de Paris | 1 |
| Square René Le Gall ⚠️ | Paris › 13e arrondissement de Paris | 1 |
| Jardin des Grands-Explorateurs Marco Polo et Robert Cavelier-de-la-Salle ⚠️ | Paris › 6e arrondissement de Paris | 1 |
| Forêt de Paris ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (2) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (3) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (4) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (9) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Jardin du Moulin de la Vierge - Carole Roussopoulos ⚠️ | Paris › 14e arrondissement de Paris | 1 |
| Square Julia Bartet ⚠️ | Paris › 14e arrondissement de Paris | 1 |
| Forêt de Paris (11) ⚠️ | Paris › 13e arrondissement de Paris | 1 |
| Jardin Henri-Sauvage ⚠️ | Paris › 18e arrondissement de Paris | 1 |
| Square Carlo Sarabezolles ⚠️ | Paris › 15e arrondissement de Paris | 1 |
| Forêt de Paris (14) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (20) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (23) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Jardin Claire Motte ⚠️ | Paris › 17e arrondissement de Paris | 1 |
| Square Emmanuel Fleury ⚠️ | Paris › 20e arrondissement de Paris | 1 |
| Square Séverine ⚠️ | Paris › 20e arrondissement de Paris | 1 |
| Jardin de la Gare de Charonne ⚠️ | Paris › 20e arrondissement de Paris | 1 |
| Jardin de l'Hospice Debrousse ⚠️ | Paris › 20e arrondissement de Paris | 1 |
| Square Sergent Aurélie Salel ⚠️ | Paris › 20e arrondissement de Paris | 1 |
| Square Marcel Sembat ⚠️ | Paris › 18e arrondissement de Paris | 1 |
| Jardin Yacine-Kateb ⚠️ | Paris › 13e arrondissement de Paris | 1 |
| Forêt de Paris (25) ⚠️ | Paris › 19e arrondissement de Paris | 1 |
| Forêt de Paris (29) ⚠️ | Paris › 19e arrondissement de Paris | 1 |
| Square Léon-Frapié ⚠️ | Paris › 20e arrondissement de Paris | 1 |
| Forêt de Paris (30) ⚠️ | Paris › 19e arrondissement de Paris | 1 |
| Forêt de Paris (38) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (48) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (51) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (55) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (56) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (57) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (60) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (62) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (63) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (68) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (69) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (77) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (78) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (79) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (85) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (88) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (90) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (92) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (93) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (94) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Square Léon-Serpollet ⚠️ | Paris › 18e arrondissement de Paris | 1 |
| Forêt de Paris (96) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (103) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (104) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (106) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (109) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (111) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (114) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (116) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Square des Saint-Simoniens ⚠️ | Paris › 20e arrondissement de Paris | 1 |
| Jardin de la Gare de Reuilly - Julien Lauprêtre ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (123) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (126) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (131) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Jardin Ilan-Halimi ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Place des Vins de France ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Square Ernest Gouin ⚠️ | Paris › 17e arrondissement de Paris | 1 |
| Square du Vert Galant ⚠️ | Paris › 1er arrondissement de Paris | 1 |
| Square Charles Victor Langlois ⚠️ | Paris › 4e arrondissement de Paris | 1 |
| Jardin Serge Gainsbourg ⚠️ | Paris › 19e arrondissement de Paris | 1 |
| Jardin de l’Hôtel Salomon de Rothschild ⚠️ | Paris › 8e arrondissement de Paris | 1 |
| Square Frédérick Lemaître ⚠️ | Paris › 10e arrondissement de Paris | 1 |
| Square Henri Collet ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Square Henry Bataille ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Parc de Paris (53) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Parc de Paris (54) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Square Jérôme Bellat ⚠️ | Paris › 17e arrondissement de Paris | 1 |
| Jardin public de l'Observatoire de Paris ⚠️ | Paris › 14e arrondissement de Paris | 1 |
| Parc de Paris (69) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Square du Tchad ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Square des Deux Nèthes ⚠️ | Paris › 18e arrondissement de Paris | 1 |
| Square Henri-Karcher ⚠️ | Paris › 20e arrondissement de Paris | 1 |
| Square de la Roquette ⚠️ | Paris › 11e arrondissement de Paris | 1 |
| Square Raoul Nordling ⚠️ | Paris › 11e arrondissement de Paris | 1 |
| Jardin Émile Gallé ⚠️ | Paris › 11e arrondissement de Paris | 1 |
| Île Sud ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Square des Chamaillards ⚠️ | Paris › 13e arrondissement de Paris | 1 |
| Jardin Solange Faladé ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Square Émile Cohl ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (149) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Forêt de Paris (154) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Forêt de Paris (156) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Jardin Biopark ⚠️ | Paris › 13e arrondissement de Paris | 1 |
| Square Marcel-Bleustein-Blanchet ⚠️ | Paris › 18e arrondissement de Paris | 1 |
| Forêt de Paris (159) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Parc de Belleville ⚠️ | Paris › 20e arrondissement de Paris | 1 |
| Coulée verte René-Dumont ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Square d'Alleray La Quintinie ⚠️ | Paris › 15e arrondissement de Paris | 1 |
| Forêt de Paris (167) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (168) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (170) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Jardin René Binet ⚠️ | Paris › 18e arrondissement de Paris | 1 |
| Square des Batignolles ⚠️ | Paris › 17e arrondissement de Paris | 1 |
| Petite Ceinture du 16e ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Jardin Eugénie Djendi ⚠️ | Paris › 15e arrondissement de Paris | 1 |
| Square du Docteur Variot ⚠️ | Paris › 20e arrondissement de Paris | 1 |
| Forêt de Paris (174) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (179) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Jardin Luc-Hoffmann ⚠️ | Paris › 19e arrondissement de Paris | 1 |
| Forêt de Paris (181) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (184) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Square Carpeaux ⚠️ | Paris › 18e arrondissement de Paris | 1 |
| Bois de Paris (29) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Bois de Paris (31) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Parc de Paris (117) ⚠️ | Paris › 13e arrondissement de Paris | 1 |
| Jardins Rosa Luxemburg ⚠️ | Paris › 18e arrondissement de Paris | 1 |
| Bois de Paris (35) ⚠️ | Paris › 19e arrondissement de Paris | 1 |
| Promenade Amália Rodrigues ⚠️ | Paris › 19e arrondissement de Paris | 1 |
| Parc de Paris (120) ⚠️ | Paris › 8e arrondissement de Paris | 1 |
| Square Henri Huchard ⚠️ | Paris › 18e arrondissement de Paris | 1 |
| Jardin Lucien Fontanarosa ⚠️ | Paris › 17e arrondissement de Paris | 1 |
| Jardin des Archives-Nationales ⚠️ | Paris › 3e arrondissement de Paris | 1 |
| Forêt de Paris (199) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Parc de Paris (125) ⚠️ | Paris › 14e arrondissement de Paris | 1 |
| Forêt de Paris (204) ⚠️ | Paris › 5e arrondissement de Paris | 1 |
| Forêt de Paris (207) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Jardin de la maison des orphelins apprentis d'Auteuil ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Forêt de Paris (214) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Jardin promenade Cesária Évora ⚠️ | Paris › 19e arrondissement de Paris | 1 |
| Jardin Federica Montseny ⚠️ | Paris › 13e arrondissement de Paris | 1 |
| Forêt de Paris (219) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Forêt de Paris (220) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Forêt de Paris (222) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Forêt de Paris (224) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Jardin Mélinée Manouchian ⚠️ | Paris › 20e arrondissement de Paris | 1 |
| Jardin Saïda ⚠️ | Paris › 15e arrondissement de Paris | 1 |
| Forêt de Paris (239) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Forêt de Paris (257) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Forêt de Paris (264) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Forêt de Paris (266) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Forêt de Paris (276) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Forêt de Paris (296) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Forêt de Paris (297) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Jardin du Père-Armand-David ⚠️ | Paris › 6e arrondissement de Paris | 1 |
| Forêt de Paris (302) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Forêt de Paris (313) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Jardin Hans et Sophie Scholl ⚠️ | Paris › 17e arrondissement de Paris | 1 |
| Forêt de Paris (316) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Forêt de Paris (320) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Forêt de Paris (328) ⚠️ | Paris › 19e arrondissement de Paris | 1 |
| Forêt de Paris (329) ⚠️ | Paris › 19e arrondissement de Paris | 1 |
| Forêt de Paris (331) ⚠️ | Paris › 19e arrondissement de Paris | 1 |
| Forêt de Paris (341) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Forêt de Paris (354) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Forêt de Paris (426) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Forêt de Paris (429) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Parc de Paris (137) ⚠️ | Paris › 14e arrondissement de Paris | 1 |
| Forêt de Paris (456) ⚠️ | Paris › 19e arrondissement de Paris | 1 |
| Forêt de Paris (459) ⚠️ | Paris › 19e arrondissement de Paris | 1 |
| Forêt de Paris (462) ⚠️ | Paris › 19e arrondissement de Paris | 1 |
| Forêt de Paris (463) ⚠️ | Paris › 19e arrondissement de Paris | 1 |
| Jardin Albert-Schweitzer ⚠️ | Paris › 4e arrondissement de Paris | 1 |
| Parc Sainte-Périne ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Parc de Paris (142) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt linéaire ⚠️ | Paris › 19e arrondissement de Paris | 1 |
| Jardin d'immeubles Albert-Bartholomé ⚠️ | Paris › 15e arrondissement de Paris | 1 |
| Forêt de Paris (495) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Forêt de Paris (525) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Forêt de Paris (531) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Forêt de Paris (622) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Forêt de Paris (634) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Jardin Élisabeth Boselli ⚠️ | Paris › 15e arrondissement de Paris | 1 |
| Forêt de Paris (658) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (770) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Forêt de Paris (783) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Forêt de Paris (785) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Forêt de Paris (795) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Jardin Laure Albin Guillot ⚠️ | Paris › 13e arrondissement de Paris | 1 |
| Forêt de Paris (815) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Jardin Paule Minck ⚠️ | Paris › 20e arrondissement de Paris | 1 |
| Parc de Paris (155) ⚠️ | Paris › 13e arrondissement de Paris | 1 |
| Promenade Jean-Jacques Sempé ⚠️ | Paris › 6e arrondissement de Paris | 1 |
| Parc de Paris (156) ⚠️ | Paris › 17e arrondissement de Paris | 1 |
| Promenade Bernard Lafray ⚠️ | Paris › 17e arrondissement de Paris | 1 |
| Forêt de Paris (828) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Bois de Paris (84) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Bois de Paris (85) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Bois de Paris (89) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Bois de Paris (91) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Square du Chanoine Viollet ⚠️ | Paris › 14e arrondissement de Paris | 1 |
| Forêt de Paris (843) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Jardin Lily Laskine ⚠️ | Paris › 17e arrondissement de Paris | 1 |
| Bois de Paris (106) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Bois de Paris (134) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Bois de Paris (137) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Bois de Paris (138) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Boisement du grand labyrinthe ⚠️ | Paris › 5e arrondissement de Paris | 1 |
| Forêt urbaine ⚠️ | Paris › 14e arrondissement de Paris | 1 |
| Bois de Paris (158) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Forêt de Paris (881) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Petite Ceinture du 18e ⚠️ | Paris › 18e arrondissement de Paris | 1 |
| Forêt de Paris (884) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Forêt de Paris (886) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Forêt de Paris (887) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Parc de Paris (166) ⚠️ | Paris › 8e arrondissement de Paris | 1 |
| Square Roger-Coquoin ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Square de l'Abbé Migne ⚠️ | Paris › 14e arrondissement de Paris | 1 |
| Square Henri Galli ⚠️ | Paris › 4e arrondissement de Paris | 1 |
| Square Charles Péguy ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Square Boucicaut ⚠️ | Paris › 7e arrondissement de Paris | 1 |
| Parc de Paris (168) ⚠️ | Paris › 16e arrondissement de Paris | 1 |
| Forêt de Paris (892) ⚠️ | Paris › 7e arrondissement de Paris | 1 |
| Square de la Place de la Réunion ⚠️ | Paris › 20e arrondissement de Paris | 1 |
| Square de la Porte de la Villette ⚠️ | Paris › 19e arrondissement de Paris | 1 |
| Promenade Jane et Paulette Nardal ⚠️ | Paris › 14e arrondissement de Paris | 1 |
| Forêt de Paris (897) ⚠️ | Paris › 12e arrondissement de Paris | 1 |
| Jardin Arnaud Beltrame ⚠️ | Paris › 3e arrondissement de Paris | 1 |
| Jardin Nicole Maestracci ⚠️ | Paris › 20e arrondissement de Paris | 1 |

1 462 parc(s) plus petits qu'une cellule ne sont pas listés : la carte les dessine, mais ils n'offrent aucune cellule.

⚠️ 1787 parc(s) hors de la fenêtre 10–125 cellules (1784 trop petit(s), 3 trop grand(s)) : affichés sur la carte, mais ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| military | 31 |
| airport | 0 |
| prison | 0 |
| **Total déclaré** | **31** |
| dont dans une zone de ce territoire | 31 |


### Zones concernées

| Zone | Cellules exclues |
|---|---:|
| Paris | 31 |
| 12e arrondissement de Paris | 11 |
| 15e arrondissement de Paris | 9 |
| 7e arrondissement de Paris | 8 |
| 20e arrondissement de Paris | 3 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
