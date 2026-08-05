# Grand Montréal

Pack `qc-montreal` · version 1.1.0 · grille 200 m · Canada › Québec

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 202 425 |
| dont restreintes (aéroport, militaire, prison) | 2 508 |
| Cellules retirées par le masque d'eau | 17 211 |
| Villes | 84 |
| Arrondissements et quartiers | 44 |
| Îles | 3 |
| Parcs | 136 |

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
| Île Perrot | 2 112 | somme de 4 villes |
| Parc Jean-Drapeau | 110 | polygone propre |

Une île *composite* n'a pas de cellules à elle : sa progression est la somme de ses villes, et ses cellules ne lui sont jamais rattachées directement — elles compteraient deux fois.

## Villes (84)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Parcs |
|---|---:|---:|---:|---:|---:|---:|
| Mirabel | 24 772 | 1 | 24 771 | 1 018 | **23 753** | 3 |
| Montreal | 22 453 | 3 872 | 18 581 | 243 | **18 338** | 52 |
| Laval | 13 495 | 1 000 | 12 495 | 24 | **12 471** | 10 |
| Terrebonne | 8 232 | 254 | 7 978 | 25 | **7 953** | 4 |
| Longueuil | 6 238 | 341 | 5 897 | 218 | **5 679** | 3 |
| Mascouche | 5 528 | 39 | 5 489 | 0 | **5 489** | 1 |
| L'Assomption | 5 099 | 4 | 5 095 | 0 | **5 095** | 1 |
| Sainte-Anne-des-Plaines | 4 840 | 1 | 4 839 | 91 | **4 748** | 1 |
| Varennes | 4 852 | 53 | 4 799 | 0 | **4 799** | 3 |
| Saint-Jérôme | 4 670 | 1 | 4 669 | 0 | **4 669** | 3 |
| Les Cèdres | 3 919 | 0 | 3 919 | 21 | **3 898** |  |
| Verchères | 3 725 | 0 | 3 725 | 0 | **3 725** |  |
| Vaudreuil-Dorion | 4 682 | 988 | 3 694 | 0 | **3 694** | 4 |
| Saint-Jean-Baptiste | 3 702 | 17 | 3 685 | 0 | **3 685** |  |
| Boucherville | 4 182 | 594 | 3 588 | 0 | **3 588** | 2 |
| Saint-Eustache | 3 710 | 126 | 3 584 | 0 | **3 584** | 1 |
| Beauharnois | 3 422 | 5 | 3 417 | 0 | **3 417** | 2 |
| Saint-Lazare | 3 386 | 0 | 3 386 | 5 | **3 381** | 2 |
| Contrecœur | 3 345 | 2 | 3 343 | 0 | **3 343** | 3 |
| Carignan | 3 168 | 0 | 3 168 | 0 | **3 168** | 1 |
| Saint-Philippe | 3 127 | 0 | 3 127 | 0 | **3 127** |  |
| Repentigny | 3 656 | 552 | 3 104 | 0 | **3 104** | 1 |
| Oka | 4 413 | 1 514 | 2 899 | 0 | **2 899** |  |
| Saint-Constant | 2 881 | 2 | 2 879 | 0 | **2 879** | 1 |
| Blainville | 2 842 | 35 | 2 807 | 248 | **2 559** | 2 |
| Saint-Isidore | 2 631 | 0 | 2 631 | 0 | **2 631** |  |
| Kahnawake | 3 136 | 611 | 2 525 | 0 | **2 525** |  |
| Sainte-Julie | 2 446 | 0 | 2 446 | 126 | **2 320** | 2 |
| Saint-Mathias-sur-Richelieu | 2 409 | 0 | 2 409 | 5 | **2 404** |  |
| Mercier | 2 323 | 5 | 2 318 | 0 | **2 318** |  |
| Brossard | 2 300 | 1 | 2 299 | 0 | **2 299** | 3 |
| La Prairie | 2 225 | 1 | 2 224 | 0 | **2 224** | 2 |
| Mont-Saint-Hilaire | 2 243 | 19 | 2 224 | 0 | **2 224** | 1 |
| Saint-Bruno-de-Montarville | 2 216 | 50 | 2 166 | 87 | **2 079** | 1 |
| Saint-Joseph-du-Lac | 2 120 | 15 | 2 105 | 0 | **2 105** |  |
| Saint-Mathieu-de-Beloeil | 2 011 | 0 | 2 011 | 15 | **1 996** |  |
| Saint-Amable | 1 884 | 0 | 1 884 | 0 | **1 884** | 1 |
| Saint-Sulpice | 1 863 | 0 | 1 863 | 0 | **1 863** |  |
| Saint-Basile-le-Grand | 1 834 | 0 | 1 834 | 14 | **1 820** | 1 |
| Châteauguay | 2 848 | 1 033 | 1 815 | 0 | **1 815** | 2 |
| Calixa-Lavallée | 1 683 | 0 | 1 683 | 0 | **1 683** |  |
| Saint-Mathieu | 1 590 | 0 | 1 590 | 0 | **1 590** |  |
| Richelieu | 1 572 | 0 | 1 572 | 0 | **1 572** |  |
| Boisbriand | 1 525 | 84 | 1 441 | 0 | **1 441** | 1 |
| Notre-Dame-de-l'Île-Perrot | 3 517 | 2 099 | 1 418 | 0 | **1 418** | 1 |
| Chambly | 1 261 | 0 | 1 261 | 0 | **1 261** | 2 |
| Beloeil | 1 237 | 0 | 1 237 | 0 | **1 237** |  |
| Hudson | 1 097 | 0 | 1 097 | 0 | **1 097** | 2 |
| Dorval | 1 453 | 385 | 1 068 | 368 | **700** | 1 |
| Pointe-Claire | 1 790 | 829 | 961 | 0 | **961** | 1 |
| Candiac | 977 | 100 | 877 | 0 | **877** | 1 |
| Dollard-Des-Ormeaux | 764 | 7 | 757 | 0 | **757** | 1 |
| Montréal-Est | 712 | 78 | 634 | 0 | **634** |  |
| Beaconsfield | 1 095 | 535 | 560 | 0 | **560** |  |
| Rosemère | 624 | 69 | 555 | 0 | **555** | 2 |
| Sainte-Anne-de-Bellevue | 563 | 29 | 534 | 0 | **534** | 2 |
| Léry | 518 | 0 | 518 | 0 | **518** |  |
| Kirkland | 492 | 1 | 491 | 0 | **491** |  |
| Sainte-Thérèse | 479 | 0 | 479 | 0 | **479** |  |
| Sainte-Catherine | 693 | 216 | 477 | 0 | **477** | 2 |
| Sainte-Marthe-sur-le-Lac | 432 | 1 | 431 | 0 | **431** |  |
| Mont-Royal | 390 | 0 | 390 | 0 | **390** |  |
| Delson | 389 | 0 | 389 | 0 | **389** |  |
| Saint-Lambert | 504 | 123 | 381 | 0 | **381** | 2 |
| Senneville | 928 | 558 | 370 | 0 | **370** | 1 |
| Pincourt | 483 | 120 | 363 | 0 | **363** |  |
| Côte-Saint-Luc | 352 | 0 | 352 | 0 | **352** |  |
| Deux-Montagnes | 368 | 53 | 315 | 0 | **315** | 1 |
| Lorraine | 311 | 4 | 307 | 0 | **307** |  |
| Baie-D'Urfé | 383 | 79 | 304 | 0 | **304** | 1 |
| Ville de l'Île-Perrot | 487 | 212 | 275 | 0 | **275** |  |
| Otterburn Park | 269 | 0 | 269 | 0 | **269** |  |
| Pointe-Calumet | 593 | 356 | 237 | 0 | **237** |  |
| Bois-des-Filion | 251 | 20 | 231 | 0 | **231** | 1 |
| Westmount | 202 | 0 | 202 | 0 | **202** |  |
| McMasterville | 156 | 0 | 156 | 0 | **156** |  |
| Pointe-des-Cascades | 131 | 0 | 131 | 0 | **131** | 1 |
| Charlemagne | 116 | 9 | 107 | 0 | **107** |  |
| Hampstead | 92 | 0 | 92 | 0 | **92** |  |
| Montréal-Ouest | 71 | 0 | 71 | 0 | **71** |  |
| Vaudreuil-sur-le-Lac | 144 | 77 | 67 | 0 | **67** |  |
| Terrasse-Vaudreuil | 62 | 6 | 56 | 0 | **56** |  |
| L'Île-Cadieux | 28 | 0 | 28 | 0 | **28** |  |
| L'Île-Dorval | 8 | 0 | 8 | 0 | **8** |  |

## Arrondissements et quartiers (44)

| Zone | Ville | Brut | Eau | Sans eau | Restr. | Comptées | Parcs |
|---|---|---:|---:|---:|---:|---:|---:|
| Saint-Hubert | longueuil | 3 371 | 4 | 3 367 | 218 | **3 149** | 1 |
| Duvernay | laval | 2 464 | 155 | 2 309 | 0 | **2 309** | 2 |
| Le Vieux-Longueuil | longueuil | 2 621 | 337 | 2 284 | 0 | **2 284** | 2 |
| Saint-Laurent | montreal | 2 190 | 4 | 2 186 | 194 | **1 992** | 4 |
| Pointe-aux-Trembles-Rivieres-des-Prairies | montreal | 2 520 | 339 | 2 181 | 6 | **2 175** | 5 |
| Chomedey | laval | 2 096 | 56 | 2 040 | 0 | **2 040** | 1 |
| Saint-François | laval | 2 072 | 249 | 1 823 | 12 | **1 811** |  |
| Pierrefonds--Roxboro | montreal | 1 668 | 287 | 1 381 | 0 | **1 381** | 2 |
| Mercier-Hochelaga-Maisonneuve | montreal | 1 396 | 98 | 1 298 | 47 | **1 251** | 4 |
| Auteuil | laval | 1 328 | 77 | 1 251 | 0 | **1 251** |  |
| Ahuntsic-Cartierville | montreal | 1 239 | 1 | 1 238 | 0 | **1 238** | 6 |
| L'Ile-Bizard--Sainte-Genevieve | montreal | 1 812 | 618 | 1 194 | 0 | **1 194** | 2 |
| Sainte-Dorothée | laval | 1 184 | 74 | 1 110 | 0 | **1 110** | 1 |
| Cote-des-Neiges--Notre-Dame-de-Grace | montreal | 1 084 | 0 | 1 084 | 0 | **1 084** | 1 |
| Fabreville | laval | 1 182 | 122 | 1 060 | 0 | **1 060** | 2 |
| Lachine | montreal | 1 125 | 218 | 907 | 0 | **907** | 2 |
| Sainte-Rose | laval | 890 | 48 | 842 | 0 | **842** | 1 |
| Villeray-Saint-Michel-Parc-Extension | montreal | 839 | 8 | 831 | 0 | **831** | 2 |
| LaSalle | montreal | 1 250 | 423 | 827 | 0 | **827** | 3 |
| Rosemont--La-Petite-Patrie | montreal | 810 | 0 | 810 | 0 | **810** | 4 |
| Ville-Marie | montreal | 1 094 | 294 | 800 | 0 | **800** | 4 |
| Sud-Ouest | montreal | 915 | 117 | 798 | 0 | **798** | 3 |
| Vimont | laval | 711 | 2 | 709 | 0 | **709** | 1 |
| Anjou | montreal | 705 | 3 | 702 | 0 | **702** | 2 |
| St-Leonard | montreal | 691 | 0 | 691 | 0 | **691** | 1 |
| Montreal-Nord | montreal | 638 | 75 | 563 | 0 | **563** |  |
| Verdun--Ile-des-Soeurs | montreal | 1 071 | 589 | 482 | 0 | **482** | 5 |
| Laval-des-Rapides | laval | 492 | 38 | 454 | 0 | **454** | 1 |
| Plateau-Mont-Royal | montreal | 416 | 3 | 413 | 0 | **413** | 3 |
| Saint-Vincent-de-Paul | laval | 402 | 0 | 402 | 12 | **390** | 1 |
| Greenfield Park | longueuil | 246 | 0 | 246 | 0 | **246** |  |
| Laval-Ouest | laval | 259 | 54 | 205 | 0 | **205** |  |
| Outremont | montreal | 198 | 1 | 197 | 0 | **197** |  |
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
| Parc Jean-Drapeau | 135 | 25 | 110 | 0 | **110** | 1 |

## Parcs (136)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Les défis « parc » demandent au moins 10 cellules.

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Grand Parc de l'Ouest | Montreal › Pierrefonds--Roxboro | 187 |
| Parc-nature du Bois-de-l'Île-Bizard | Montreal › L'Ile-Bizard--Sainte-Genevieve | 156 |
| Bois Duvernay | Laval › Duvernay | 152 |
| Parc nature les Forestiers-de-Saint-Lazare | Saint-Lazare | 148 |
| Le Boisé Sainte-Dorothée | Laval › Sainte-Dorothée | 143 |
| Parc du Domaine Vert | Mirabel | 138 |
| Arboretum Morgan | Sainte-Anne-de-Bellevue | 134 |
| Parc-nature de la Pointe-aux-Prairies | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 132 |
| Réserve naturelle du Bois-de-Brossard | Brossard | 119 |
| Bois de l'Équerre | Laval › Sainte-Rose | 111 |
| Parc du Domaine Vert (2) | Mirabel | 99 |
| Parc du Mont-Royal | Montreal › Ville-Marie | 96 |
| Refuge faunique Marguerite d'Youville | Châteauguay | 95 |
| Parc agricole du Bois-de-la-Roche | Senneville | 90 |
| Parc régional Bois de Belle-Rivière | Mirabel | 88 |
| Parc-nature du Bois-de-Liesse | Montreal › Saint-Laurent | 87 |
| Parc Michel Chartrand | Longueuil › Le Vieux-Longueuil | 86 |
| Parc Jean-Drapeau | Montreal › Ville-Marie › Parc Jean-Drapeau | 84 |
| Parc régional des Grêves - Secteur de la Colonie des Grèves de Contrecoeur | Contrecœur | 80 |
| Parc Faunique Domaine du Parc (Ruisseau de Feu) | Terrebonne | 75 |
| Refuge d'oiseaux migrateurs de l'Île-aux-Hérons | Sainte-Catherine › LaSalle | 75 |
| Parc du Grand-Coteau | Mascouche | 64 |
| Parc régional de la Rivière-du-Nord | Saint-Jérôme | 62 |
| Parc nature Saint-Eustache | Saint-Eustache | 61 |
| Parc Le Rocher | Saint-Amable | 58 |
| Parc de la Cité | Longueuil › Saint-Hubert | 53 |
| Bois Papineau | Laval › Duvernay | 53 |
| Centre ecologique Fernand-Seguin | Châteauguay | 47 |
| Parc régional des Grèves | Contrecœur | 47 |
| Parc-nature du Bois-de-Saraguay | Montreal › Ahuntsic-Cartierville | 43 |
| Parc Angrignon | Montreal › Sud-Ouest | 42 |
| Jardin botanique de Montréal | Montreal › Rosemont--La-Petite-Patrie | 41 |
| Réserve naturelle du Piémont-du-Mont-Saint-Hilaire | Mont-Saint-Hilaire | 41 |
| Bois Robert | Beauharnois | 33 |
| Parc Frédéric-Back | Montreal › Villeray-Saint-Michel-Parc-Extension | 33 |
| Parc du Canal-de-Lachine | Montreal › Sud-Ouest | 32 |
| Parc Maisonneuve | Montreal › Rosemont--La-Petite-Patrie | 31 |
| Parc de Blainville | Blainville | 30 |
| Récré-O-Parc de Sainte-Catherine | Sainte-Catherine | 27 |
| Parc naturel des Ruisseaux | Chambly | 27 |
| Parc des Étangs Antoine-Charlebois | Sainte-Julie | 24 |
| Parc nature de Pointe-des-Cascades | Pointe-des-Cascades | 24 |
| Parc olympique | Montreal › Mercier-Hochelaga-Maisonneuve | 23 |
| Parc Marie-Victorin | Saint-Bruno-de-Montarville | 23 |
| Bois de la Source | Laval › Fabreville | 22 |
| Parc Saint-Charles | Varennes | 22 |
| Parc-nature des Rapides-du-Cheval-Blanc | Montreal › Pierrefonds--Roxboro | 22 |
| Parc écologique des Sources | Montreal › Saint-Laurent | 22 |
| Parc de conservation Barbe-Denys-De La Trinité | Contrecœur | 22 |
| Parc multifonctionnel | Saint-Constant | 22 |
| Parc de Terrebonne | Terrebonne | 21 |
| Parc Terra Cotta | Pointe-Claire | 20 |
| Centre de la nature | Laval › Saint-Vincent-de-Paul | 20 |
| Réserve naturelle du Ruisseau-Robert | Carignan | 20 |
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
| Parc de Vaudreuil-Dorion | Vaudreuil-Dorion | 15 |
| Parc Bernard-Landry | Laval › Laval-des-Rapides | 15 |
| Parc-nature de l'Île-de-la-Visitation | Montreal › Ahuntsic-Cartierville | 15 |
| Parc Marais Tylee | Rosemère | 14 |
| Parc-Nature Harwood | Vaudreuil-Dorion | 13 |
| Parc de l'Île-Lebel | Repentigny | 12 |
| Parc Saint-Charles (2) | Varennes | 12 |
| Parc de la Rivière-des-Mille-Îles | Boisbriand | 12 |
| Domaine Saint-Paul | Montreal › Verdun--Ile-des-Soeurs | 12 |
| Parc Marcelin-Wilson | Montreal › Ahuntsic-Cartierville | 12 |
| Parc Sandy Beach | Hudson | 11 |
| Parc Tiohtià:ke Otsira'kéhne | Montreal › Cote-des-Neiges--Notre-Dame-de-Grace | 11 |
| Parc Équestre | Blainville | 11 |
| Parc des Rapides | Montreal › LaSalle | 11 |
| Parc Arthur-Therrien | Montreal › Verdun--Ile-des-Soeurs | 10 |
| Parc de Lausanne | Laval › Vimont | 10 |
| Parc des Écluses | Beauharnois | 10 |
| Parc de la Voie maritime | Saint-Lambert | 10 |
| Parc de l'Aqueduc | Montreal › Verdun--Ile-des-Soeurs | 10 |
| Parc du Père-Marquette ⚠️ | Montreal › Rosemont--La-Petite-Patrie | 9 |
| Parc Pierre-Laporte ⚠️ | Boucherville | 9 |
| Parc de Montreal ⚠️ | Montreal › Ville-Marie | 9 |
| Parc nature de la Tourbière-du-Bordelais ⚠️ | Saint-Lazare | 9 |
| Réserve écologique de l'Île-Garth ⚠️ | Bois-des-Filion | 9 |
| Réserve écologique des Îles-Avelle-Wight-et-Hiam ⚠️ | Vaudreuil-Dorion | 9 |
| Réserve naturelle du Marécage-des-Chenaux-de-Vaudreuil ⚠️ | Vaudreuil-Dorion | 9 |
| Refuge d'oiseaux migrateurs des Îles-de-la-Couvée ⚠️ | Saint-Lambert | 9 |
| Parc des Hirondelles ⚠️ | Montreal › Ahuntsic-Cartierville | 8 |
| Parc Jeanne-Mance ⚠️ | Montreal › Plateau-Mont-Royal | 8 |
| Parc Thomas-Chapais ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 8 |
| Parc Pasquale-Gattuso ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 8 |
| Parc Fritz ⚠️ | Baie-D'Urfé | 8 |
| Parc écologique de l'Assomption ⚠️ | L'Assomption | 8 |
| Parc Philippe-Laheurte ⚠️ | Montreal › Saint-Laurent | 8 |
| McGill Bird Observatory ⚠️ | Sainte-Anne-de-Bellevue | 8 |
| Réserve naturelle du Boisé-Roger-Lemoine ⚠️ | Deux-Montagnes | 8 |
| Parc Champlain ⚠️ | Candiac | 8 |
| Parc de la Traversée ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 8 |
| Parc Lucie-F.-Roussel ⚠️ | La Prairie | 7 |
| Terrains du centre communautaire Sarto-Desnoyers ⚠️ | Dorval | 7 |
| Parc Henri-Julien ⚠️ | Montreal › Ahuntsic-Cartierville | 7 |
| Parc Angora ⚠️ | Terrebonne | 7 |
| Parc René-Lévesque ⚠️ | Montreal › Lachine | 7 |
| Parc Robert-Lebel ⚠️ | Chambly | 7 |
| Parc du Boisé-Du-Pays-Brûlé ⚠️ | Boucherville | 7 |
| Réserve naturelle de l'Île des Juifs ⚠️ | Rosemère | 7 |
| Parc Marie-Victorin (2) ⚠️ | Longueuil › Le Vieux-Longueuil | 7 |
| Parc LaSalle ⚠️ | Montreal › Lachine | 7 |
| Parc d'Anjou-sur-le-Lac ⚠️ | Montreal › Anjou | 7 |
| Parc Sir-Wilfrid-Laurier ⚠️ | Montreal › Plateau-Mont-Royal | 6 |
| Parc de la Terre ⚠️ | Brossard | 6 |
| Parc Félix-Leclerc ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 6 |
| Parc Ahuntsic ⚠️ | Montreal › Ahuntsic-Cartierville | 6 |
| Parc Eugène-Dostie ⚠️ | Montreal › L'Ile-Bizard--Sainte-Genevieve | 6 |
| Parc historique Pointe-du-Moulin ⚠️ | Notre-Dame-de-l'Île-Perrot | 6 |
| Parc Delorme ⚠️ | Montreal › St-Leonard | 6 |
| Parc Ignace-Bourget ⚠️ | Montreal › Sud-Ouest | 6 |
| Parc des Méandres ⚠️ | Sainte-Anne-des-Plaines | 6 |
| Parc de la Commune ⚠️ | Varennes | 6 |
| Réserve naturelle de l'Île Locas ⚠️ | Laval › Fabreville | 6 |
| Parc de Hudson ⚠️ | Hudson | 6 |
| Parc Jacques-Locas ⚠️ | Saint-Jérôme | 6 |
| Parc Vaillant ⚠️ | Terrebonne | 5 |
| Parc Émilie-Gamelin ⚠️ | La Prairie | 5 |
| Parc Maynard-Ferguson ⚠️ | Montreal › Verdun--Ile-des-Soeurs | 5 |
| Le Boutillier Park ⚠️ | Laval › Chomedey | 5 |
| Parc du Ruisseau ⚠️ | Saint-Basile-le-Grand | 5 |
| Parc naturel de Rivière-à-Gagnon ⚠️ | Saint-Jérôme | 5 |
| Parc de Montreal (2) ⚠️ | Montreal › LaSalle | 5 |
| Grand Parc Urbain ⚠️ | Brossard | 5 |
| Parc Étienne-Desmarteau ⚠️ | Montreal › Rosemont--La-Petite-Patrie | 4 |
| Parc de la Coulée ⚠️ | Sainte-Julie | 4 |

⚠️ 53 parc(s) sous le seuil de 10 cellules : ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| military | 13 416 |
| airport | 5 987 |
| prison | 292 |
| **Total déclaré** | **19 695** |
| dont dans une zone de ce territoire | 2 508 |

Le jeu de données couvre plus large que le territoire — il est produit à une échelle supérieure. Seules les cellules tombant dans une zone d'ici pèsent sur un pourcentage.

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
| Sainte-Julie | 126 |
| Sainte-Anne-des-Plaines | 91 |
| Saint-Bruno-de-Montarville | 87 |
| Mercier-Hochelaga-Maisonneuve | 47 |
| Terrebonne | 25 |
| Laval | 24 |
| Les Cèdres | 21 |
| Saint-Mathieu-de-Beloeil | 15 |
| Saint-Basile-le-Grand | 14 |
| Saint-Vincent-de-Paul | 12 |
| Saint-François | 12 |
| Pointe-aux-Trembles-Rivieres-des-Prairies | 6 |
| Saint-Lazare | 5 |
| Saint-Mathias-sur-Richelieu | 5 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
