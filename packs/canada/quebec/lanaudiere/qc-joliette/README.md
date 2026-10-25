# Joliette (Lanaudière)

Pack `qc-joliette` · version 1.0.0 · grille 200 m · Canada › Québec › Lanaudière

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 21 731 |
| dont restreintes (aéroport, militaire, prison) | 37 |
| dont sans chemin (aucune voie à moins de 60 m) | 7 628 |
| dont en forêt, sans chemin non plus | 4 513 |
| dont traversées par un cours d'eau, sans chemin non plus | 1 624 |
| Cellules retirées par le masque d'eau | 286 |
| Villes | 10 |
| Arrondissements et quartiers | 0 |
| Îles | 0 |
| Parcs | 95 |

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

## Villes (10)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Sans chemin | Parcs |
|---|---:|---:|---:|---:|---:|---:|---:|
| Saint-Thomas | 4 927 | 7 | 4 920 | 0 | **4 920** | 2 176 (44 %) | 2 |
| Sainte-Mélanie | 4 081 | 74 | 4 007 | 0 | **4 007** | 951 (24 %) | 3 |
| Saint-Ambroise-de-Kildare | 3 511 | 6 | 3 505 | 9 | **3 496** | 1 704 (49 %) | 6 |
| Saint-Paul | 2 575 | 45 | 2 530 | 0 | **2 530** | 719 (28 %) | 13 |
| Notre-Dame-de-Lourdes | 1 869 | 16 | 1 853 | 28 | **1 825** | 806 (44 %) | 3 |
| Crabtree | 1 354 | 36 | 1 318 | 0 | **1 318** | 464 (35 %) | 6 |
| Joliette | 1 233 | 42 | 1 191 | 0 | **1 191** | 111 (9 %) | 22 |
| Saint-Charles-Borromée | 978 | 25 | 953 | 0 | **953** | 231 (24 %) | 12 |
| Notre-Dame-des-Prairies | 968 | 22 | 946 | 0 | **946** | 241 (25 %) | 25 |
| Saint-Pierre | 521 | 13 | 508 | 0 | **508** | 225 (44 %) | 1 |

## Parcs (95)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Parc régional des Chutes-Monte-à-Peine-et-des-Dalles | Sainte-Mélanie | 74 |
| Parc du Bois-Brûlé ⚠️ | Saint-Charles-Borromée | 9 |
| Parc Saint-Jean-Bosco ⚠️ | Saint-Charles-Borromée | 6 |
| Parc Casavant-Desrochers ⚠️ | Saint-Charles-Borromée | 5 |
| Parc Denis-Laporte ⚠️ | Crabtree | 5 |
| Parc Amphithéâtre Fernand-Lindsay ⚠️ | Joliette | 5 |
| Parc Louis-Querbes ⚠️ | Joliette | 4 |
| Parc Pierre-Charbonneau ⚠️ | Joliette | 4 |
| Parc de l'Érablière ⚠️ | Crabtree | 4 |
| Parc Antonio-Barrette ⚠️ | Joliette | 3 |
| Parc des Dalles ⚠️ | Joliette | 3 |
| Parc Georges-Rondeau ⚠️ | Joliette | 3 |
| Parc des Berges ⚠️ | Saint-Paul | 3 |
| Parc Maria-Goretti ⚠️ | Saint-Charles-Borromée | 3 |
| Terrain des loisirs ⚠️ | Saint-Thomas | 2 |
| Parc Armand Desrochers ⚠️ | Crabtree | 2 |
| Parc Bélair ⚠️ | Joliette | 2 |
| Parc Réal-Laurin ⚠️ | Joliette | 2 |
| Parc du Chalet des loisirs ⚠️ | Saint-Ambroise-de-Kildare | 2 |
| Parc du Bourg-Boisé ⚠️ | Saint-Paul | 2 |
| Parc de Joliette ⚠️ | Joliette | 1 |
| Parc Émile-Prévost ⚠️ | Joliette | 1 |
| Parc Hervé-Champoux ⚠️ | Joliette | 1 |
| Parc Arthur-Robillard ⚠️ | Joliette | 1 |
| Parc Saint-Jean-Baptiste ⚠️ | Joliette | 1 |
| Parc Amyot ⚠️ | Saint-Paul | 1 |
| Parc Arthur-Normand ⚠️ | Joliette | 1 |
| Parc Amable-Chalut ⚠️ | Notre-Dame-des-Prairies | 1 |
| Parc Jean-Livernoche ⚠️ | Saint-Charles-Borromée | 1 |
| Parc Lajoie ⚠️ | Joliette | 1 |
| Parc du Centre communautaire Jeannette-Laviolette ⚠️ | Saint-Paul | 1 |
| parc des Jonquilles ⚠️ | Notre-Dame-des-Prairies | 1 |
| Parc Colette-Robillard ⚠️ | Notre-Dame-des-Prairies | 1 |
| Parc Paul-Émile-Robillard ⚠️ | Notre-Dame-des-Prairies | 1 |
| Parc Robert-Quenneville ⚠️ | Joliette | 1 |
| Parc des Champs-Élysées ⚠️ | Notre-Dame-des-Prairies | 1 |
| Parc des Sables ⚠️ | Sainte-Mélanie | 1 |
| Parc Paul-Émile-Asselin ⚠️ | Notre-Dame-de-Lourdes | 1 |
| Parc de la rue Ducharme ⚠️ | Saint-Ambroise-de-Kildare | 1 |
| Parc Maxime-Beauséjour ⚠️ | Saint-Ambroise-de-Kildare | 1 |
| Parc de Bellefeuille ⚠️ | Saint-Charles-Borromée | 1 |
| Parc du Docteur-Yvon-Gauthier ⚠️ | Saint-Charles-Borromée | 1 |
| Parc de Joliette (4) ⚠️ | Joliette | 1 |
| Parc des Tourelles ⚠️ | Saint-Paul | 1 |
| Parc Royal ⚠️ | Saint-Paul | 1 |

50 parc(s) plus petits qu'une cellule ne sont pas listés : la carte les dessine, mais ils n'offrent aucune cellule.

⚠️ 94 parc(s) hors de la fenêtre 10–125 cellules (94 trop petit(s), 0 trop grand(s)) : affichés sur la carte, mais ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| airport | 38 |
| military | 0 |
| prison | 0 |
| **Total déclaré** | **38** |
| dont dans une zone de ce territoire | 37 |

Le jeu de données couvre plus large que le territoire — il est produit à une échelle supérieure. Seules les cellules tombant dans une zone d'ici pèsent sur un pourcentage.

### Zones concernées

| Zone | Cellules exclues |
|---|---:|
| Notre-Dame-de-Lourdes | 28 |
| Saint-Ambroise-de-Kildare | 9 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
