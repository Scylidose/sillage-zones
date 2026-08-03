# Grand Montréal

Pack `qc-montreal` · version 1.0.1 · grille 200 m · Canada › Québec

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 140 402 |
| dont restreintes (aéroport, militaire, prison) | 2 322 |
| Cellules écartées comme eau | 1 299 |
| Villes | 54 |
| Arrondissements et quartiers | 44 |
| Îles | 3 |
| Parcs | 86 |

Une cellule appartenant à plusieurs zones (un arrondissement *et* sa ville) n'est comptée qu'une fois dans le total du territoire, mais apparaît dans chacune des zones ci-dessous.

« Écartées comme eau » ne compte que les cellules d'eau tombant dans un polygone de zone : les frontières sont rognées sur la rive, donc l'essentiel du fleuve n'a jamais appartenu à personne.

### Lire les colonnes

| Colonne | Ce que c'est |
|---|---|
| **Brut** | cellules dans le polygone, avant toute exclusion |
| **Eau** | parmi elles, écartées comme plan d'eau — elles n'appartiennent à aucune zone |
| **Sans eau** | ce que publie `cell-totals.json` |
| **Restr.** | parmi elles, dans un aéroport, une zone militaire ou une prison |
| **Comptées** | le dénominateur réel de l'app : sans eau − restreintes |

## Îles

| Île | Cellules | Composition |
|---|---:|---|
| Île de Montréal | 25 368 | somme de 15 villes |
| Île Perrot | 2 112 | somme de 4 villes |
| Parc Jean-Drapeau | 110 | polygone propre |

Une île *composite* n'a pas de cellules à elle : sa progression est la somme de ses villes, et ses cellules ne lui sont jamais rattachées directement — elles compteraient deux fois.

## Villes (54)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Parcs |
|---|---:|---:|---:|---:|---:|---:|
| Mirabel | 24 772 | 0 | 24 772 | 1 018 | **23 754** |  |
| Montreal | 18 582 | 0 | 18 582 | 243 | **18 339** | 36 |
| Laval | 12 495 | 0 | 12 495 | 24 | **12 471** | 3 |
| Terrebonne | 7 978 | 0 | 7 978 | 25 | **7 953** | 3 |
| Longueuil | 5 897 | 0 | 5 897 | 218 | **5 679** | 2 |
| Mascouche | 5 489 | 0 | 5 489 | 0 | **5 489** |  |
| Sainte-Anne-des-Plaines | 4 840 | 1 | 4 839 | 91 | **4 748** | 1 |
| Varennes | 4 799 | 0 | 4 799 | 0 | **4 799** | 3 |
| Saint-Jérôme | 4 670 | 1 | 4 669 | 0 | **4 669** | 2 |
| Vaudreuil-Dorion | 3 694 | 0 | 3 694 | 0 | **3 694** | 2 |
| Boucherville | 3 588 | 0 | 3 588 | 0 | **3 588** | 2 |
| Saint-Eustache | 3 584 | 0 | 3 584 | 0 | **3 584** |  |
| Repentigny | 3 104 | 0 | 3 104 | 0 | **3 104** | 1 |
| Oka | 2 899 | 0 | 2 899 | 0 | **2 899** |  |
| Saint-Constant | 2 879 | 0 | 2 879 | 0 | **2 879** | 1 |
| Blainville | 2 807 | 0 | 2 807 | 248 | **2 559** | 1 |
| Kahnawake | 2 525 | 0 | 2 525 | 0 | **2 525** |  |
| Brossard | 2 300 | 0 | 2 300 | 0 | **2 300** | 2 |
| La Prairie | 2 225 | 1 | 2 224 | 0 | **2 224** | 2 |
| Saint-Bruno-de-Montarville | 2 166 | 0 | 2 166 | 87 | **2 079** | 1 |
| Saint-Joseph-du-Lac | 2 105 | 0 | 2 105 | 0 | **2 105** |  |
| Châteauguay | 1 815 | 0 | 1 815 | 0 | **1 815** |  |
| Boisbriand | 1 441 | 0 | 1 441 | 0 | **1 441** |  |
| Notre-Dame-de-l'Île-Perrot | 1 418 | 0 | 1 418 | 0 | **1 418** | 1 |
| Dorval | 1 068 | 0 | 1 068 | 368 | **700** | 1 |
| Pointe-Claire | 961 | 0 | 961 | 0 | **961** | 1 |
| Candiac | 877 | 0 | 877 | 0 | **877** | 1 |
| Dollard-Des-Ormeaux | 757 | 0 | 757 | 0 | **757** | 1 |
| Montréal-Est | 634 | 0 | 634 | 0 | **634** |  |
| Beaconsfield | 560 | 0 | 560 | 0 | **560** |  |
| Rosemère | 555 | 0 | 555 | 0 | **555** |  |
| Sainte-Anne-de-Bellevue | 534 | 0 | 534 | 0 | **534** |  |
| Kirkland | 491 | 0 | 491 | 0 | **491** | 1 |
| Sainte-Thérèse | 479 | 0 | 479 | 0 | **479** |  |
| Sainte-Catherine | 477 | 0 | 477 | 0 | **477** | 1 |
| Sainte-Marthe-sur-le-Lac | 432 | 0 | 432 | 0 | **432** |  |
| Mont-Royal | 390 | 0 | 390 | 0 | **390** |  |
| Delson | 389 | 0 | 389 | 0 | **389** |  |
| Saint-Lambert | 381 | 0 | 381 | 0 | **381** | 1 |
| Senneville | 370 | 0 | 370 | 0 | **370** |  |
| Pincourt | 363 | 0 | 363 | 0 | **363** |  |
| Côte-Saint-Luc | 352 | 0 | 352 | 0 | **352** |  |
| Deux-Montagnes | 315 | 0 | 315 | 0 | **315** |  |
| Lorraine | 307 | 0 | 307 | 0 | **307** |  |
| Baie-D'Urfé | 304 | 0 | 304 | 0 | **304** | 1 |
| Ville de l'Île-Perrot | 275 | 0 | 275 | 0 | **275** |  |
| Pointe-Calumet | 237 | 0 | 237 | 0 | **237** |  |
| Bois-des-Filion | 231 | 0 | 231 | 0 | **231** |  |
| Westmount | 202 | 0 | 202 | 0 | **202** |  |
| Charlemagne | 107 | 0 | 107 | 0 | **107** |  |
| Hampstead | 92 | 0 | 92 | 0 | **92** |  |
| Montréal-Ouest | 71 | 0 | 71 | 0 | **71** |  |
| Vaudreuil-sur-le-Lac | 67 | 0 | 67 | 0 | **67** |  |
| Terrasse-Vaudreuil | 56 | 0 | 56 | 0 | **56** |  |

## Arrondissements et quartiers (44)

| Zone | Ville | Brut | Eau | Sans eau | Restr. | Comptées | Parcs |
|---|---|---:|---:|---:|---:|---:|---:|
| Saint-Hubert | longueuil | 3 372 | 4 | 3 368 | 218 | **3 150** | 1 |
| Duvernay | laval | 2 464 | 155 | 2 309 | 0 | **2 309** |  |
| Le Vieux-Longueuil | longueuil | 2 623 | 337 | 2 286 | 0 | **2 286** | 2 |
| Saint-Laurent | montreal | 2 186 | 0 | 2 186 | 194 | **1 992** | 3 |
| Pointe-aux-Trembles-Rivieres-des-Prairies | montreal | 2 181 | 0 | 2 181 | 6 | **2 175** | 2 |
| Chomedey | laval | 2 096 | 56 | 2 040 | 0 | **2 040** | 1 |
| Saint-François | laval | 2 072 | 249 | 1 823 | 12 | **1 811** |  |
| Pierrefonds--Roxboro | montreal | 1 381 | 0 | 1 381 | 0 | **1 381** |  |
| Mercier-Hochelaga-Maisonneuve | montreal | 1 298 | 0 | 1 298 | 47 | **1 251** | 3 |
| Auteuil | laval | 1 328 | 77 | 1 251 | 0 | **1 251** |  |
| Ahuntsic-Cartierville | montreal | 1 239 | 1 | 1 238 | 0 | **1 238** | 4 |
| L'Ile-Bizard--Sainte-Genevieve | montreal | 1 194 | 0 | 1 194 | 0 | **1 194** | 1 |
| Sainte-Dorothée | laval | 1 184 | 74 | 1 110 | 0 | **1 110** |  |
| Cote-des-Neiges--Notre-Dame-de-Grace | montreal | 1 084 | 0 | 1 084 | 0 | **1 084** |  |
| Fabreville | laval | 1 181 | 122 | 1 059 | 0 | **1 059** |  |
| Lachine | montreal | 907 | 0 | 907 | 0 | **907** | 2 |
| Sainte-Rose | laval | 890 | 48 | 842 | 0 | **842** |  |
| Villeray-Saint-Michel-Parc-Extension | montreal | 831 | 0 | 831 | 0 | **831** | 2 |
| LaSalle | montreal | 827 | 0 | 827 | 0 | **827** | 2 |
| Rosemont--La-Petite-Patrie | montreal | 810 | 0 | 810 | 0 | **810** | 4 |
| Ville-Marie | montreal | 800 | 0 | 800 | 0 | **800** | 2 |
| Sud-Ouest | montreal | 798 | 0 | 798 | 0 | **798** | 4 |
| Vimont | laval | 710 | 2 | 708 | 0 | **708** | 1 |
| Anjou | montreal | 702 | 0 | 702 | 0 | **702** | 1 |
| St-Leonard | montreal | 691 | 0 | 691 | 0 | **691** | 1 |
| Montreal-Nord | montreal | 563 | 0 | 563 | 0 | **563** |  |
| Verdun--Ile-des-Soeurs | montreal | 482 | 0 | 482 | 0 | **482** | 2 |
| Laval-des-Rapides | laval | 492 | 38 | 454 | 0 | **454** | 1 |
| Plateau-Mont-Royal | montreal | 413 | 0 | 413 | 0 | **413** | 3 |
| Saint-Vincent-de-Paul | laval | 401 | 0 | 401 | 12 | **389** | 1 |
| Greenfield Park | longueuil | 246 | 0 | 246 | 0 | **246** |  |
| Laval-Ouest | laval | 259 | 54 | 205 | 0 | **205** |  |
| Outremont | montreal | 197 | 0 | 197 | 0 | **197** |  |
| Secteur L | brossard | 192 | 1 | 191 | 0 | **191** |  |
| Pont-Viau | laval | 181 | 16 | 165 | 0 | **165** |  |
| Secteur R | brossard | 147 | 2 | 145 | 0 | **145** |  |
| Laval-sur-le-Lac | laval | 129 | 31 | 98 | 0 | **98** |  |
| Secteur M | brossard | 87 | 0 | 87 | 0 | **87** |  |
| Secteur O | brossard | 79 | 0 | 79 | 0 | **79** |  |
| Secteur J | brossard | 61 | 0 | 61 | 0 | **61** |  |
| Secteur N | brossard | 59 | 0 | 59 | 0 | **59** |  |
| Secteur I | brossard | 55 | 1 | 54 | 0 | **54** |  |
| Îles-Laval | laval | 56 | 28 | 28 | 0 | **28** |  |
| Secteur E | brossard | 19 | 0 | 19 | 0 | **19** |  |

## Îles à polygone propre

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Parcs |
|---|---:|---:|---:|---:|---:|---:|
| Parc Jean-Drapeau | 110 | 0 | 110 | 0 | **110** | 1 |

## Parcs (86)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Les défis « parc » demandent au moins 10 cellules.

| Parc | Cellules |
|---|---:|
| Parc Michel Chartrand | 86 |
| Parc Jean-Drapeau | 84 |
| Parc de la Cité | 53 |
| Parc Angrignon | 42 |
| Jardin botanique de Montréal | 41 |
| Parc Le Rocher | 37 |
| Parc du Canal-de-Lachine | 33 |
| Parc Frédéric-Back | 33 |
| Parc Maisonneuve | 31 |
| Récré-O-Parc de Sainte-Catherine | 27 |
| Parc naturel des Ruisseaux | 27 |
| Parc récréotouristique de Saint-Lin-Laurentides | 24 |
| Parc olympique | 23 |
| Parc Marie-Victorin | 23 |
| Parc Saint-Charles | 22 |
| Parc multifonctionnel | 22 |
| Parc | 21 |
| Parc Terra Cotta | 20 |
| Centre de la nature | 20 |
| Parc Jarry | 19 |
| Parc Marcel-Laurin | 18 |
| Parc du Centenaire | 17 |
| Parc de l'Honorable-George-O'Reilly | 16 |
| Parc La Fontaine | 15 |
| Parc de la Promenade-Bellerive | 15 |
| Vieux-Port | 15 |
| Parc | 15 |
| Parc Bernard-Landry | 15 |
| Parc-Nature Harwood | 13 |
| Parc de l'Île-Lebel | 12 |
| Parc | 12 |
| Parc du Boisé de la Volière | 12 |
| Parc Marcelin-Wilson | 12 |
| Parc Sandy Beach | 11 |
| Parc Équestre | 11 |
| Parc des Rapides | 11 |
| Parc Arthur-Therrien | 10 |
| Parc de Lausanne | 10 |
| Parc des Écluses | 10 |
| Parc de la Voie maritime | 10 |
| Parc de l'Aqueduc | 10 |
| Parc du Père-Marquette ⚠️ | 9 |
| Parc Pierre-Laporte ⚠️ | 9 |
| Parc ⚠️ | 9 |
| Parc des Hirondelles ⚠️ | 8 |
| Parc Jeanne-Mance ⚠️ | 8 |
| Parc Thomas-Chapais ⚠️ | 8 |
| Parc Pasquale-Gattuso ⚠️ | 8 |
| Parc Fritz ⚠️ | 8 |
| Parc Philippe-Laheurte ⚠️ | 8 |
| Parc Champlain ⚠️ | 8 |
| Parc de la Traversée ⚠️ | 8 |
| Parc Lucie-F.-Roussel ⚠️ | 7 |
| Terrains du centre communautaire Sarto-Desnoyers ⚠️ | 7 |
| Parc Henri-Julien ⚠️ | 7 |
| Parc Angora ⚠️ | 7 |
| Parc René-Lévesque ⚠️ | 7 |
| Parc du Boisé-Du-Pays-Brûlé ⚠️ | 7 |
| Parc Marie-Victorin ⚠️ | 7 |
| Parc LaSalle ⚠️ | 7 |
| Parc d'Anjou-sur-le-Lac ⚠️ | 7 |
| Parc Sir-Wilfrid-Laurier ⚠️ | 6 |
| Parc de la Terre ⚠️ | 6 |
| Parc Félix-Leclerc ⚠️ | 6 |
| Parc Ahuntsic ⚠️ | 6 |
| Parc Eugène-Dostie ⚠️ | 6 |
| Parc historique Pointe-du-Moulin ⚠️ | 6 |
| Parc Delorme ⚠️ | 6 |
| Parc Ignace-Bourget ⚠️ | 6 |
| Parc du Bois-Franc ⚠️ | 6 |
| Parc des Méandres ⚠️ | 6 |
| Parc de la Commune ⚠️ | 6 |
| Parc ⚠️ | 6 |
| Parc des Bénévoles ⚠️ | 6 |
| Parc Jacques-Locas ⚠️ | 6 |
| Parc Esther-Blondin ⚠️ | 5 |
| Parc Émilie-Gamelin ⚠️ | 5 |
| Parc Maynard-Ferguson ⚠️ | 5 |
| Le Boutillier Park ⚠️ | 5 |
| Parc du Ruisseau ⚠️ | 5 |
| Parc naturel de Rivière-à-Gagnon ⚠️ | 5 |
| Parc ⚠️ | 5 |
| Grand Parc Urbain ⚠️ | 5 |
| Parc Edmour-J.-Harvey ⚠️ | 5 |
| Parc Étienne-Desmarteau ⚠️ | 4 |
| Parc de la Coulée ⚠️ | 4 |

⚠️ 45 parc(s) sous le seuil de 10 cellules : ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| military | 13 416 |
| airport | 5 987 |
| prison | 292 |
| **Total déclaré** | **19 695** |
| dont dans une zone de ce territoire | 2 322 |

Le jeu de données couvre plus large que le territoire — il est produit à l'échelle de la province. Seules les cellules tombant dans une zone d'ici pèsent sur un pourcentage.

### Zones concernées

| Zone | Cellules exclues |
|---|---:|
| Mirabel | 1 018 |
| Dorval | 368 |
| Blainville | 248 |
| Montreal | 243 |
| Saint-Hubert | 218 |
| Longueuil | 218 |
| Saint-Laurent | 194 |
| Sainte-Anne-des-Plaines | 91 |
| Saint-Bruno-de-Montarville | 87 |
| Mercier-Hochelaga-Maisonneuve | 47 |
| Terrebonne | 25 |
| Laval | 24 |
| Saint-Vincent-de-Paul | 12 |
| Saint-François | 12 |
| Pointe-aux-Trembles-Rivieres-des-Prairies | 6 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
