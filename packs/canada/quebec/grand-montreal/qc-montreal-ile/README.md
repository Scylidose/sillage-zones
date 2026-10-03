# Montréal (île)

Pack `qc-montreal-ile` · version 1.2.4 · grille 200 m · Canada › Québec › Grand Montréal

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 25 367 |
| dont restreintes (aéroport, militaire, prison) | 611 |
| dont sans chemin (aucune voie à moins de 60 m) | 401 |
| dont en forêt, sans chemin non plus | 216 |
| dont traversées par un cours d'eau, sans chemin non plus | 11 |
| Cellules retirées par le masque d'eau | 6 398 |
| Villes | 16 |
| Arrondissements et quartiers | 19 |
| Îles | 2 |
| Parcs | 1 552 |

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

## Îles

| Île | Cellules | Composition |
|---|---:|---|
| Île de Montréal | 25 367 | somme de 15 villes |
| Parc Jean-Drapeau | 110 | polygone propre |

Une île *composite* n'a pas de cellules à elle : sa progression est la somme de ses villes, et ses cellules ne lui sont jamais rattachées directement — elles compteraient deux fois.

## Villes (16)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Sans chemin | Parcs |
|---|---:|---:|---:|---:|---:|---:|---:|
| Montréal | 22 453 | 3 872 | 18 581 | 243 | **18 338** | 222 (1 %) | 1212 |
| Dorval | 1 453 | 385 | 1 068 | 368 | **700** | 1 (0 %) | 26 |
| Pointe-Claire | 1 790 | 829 | 961 | 0 | **961** |  | 57 |
| Dollard-des-Ormeaux | 764 | 7 | 757 | 0 | **757** |  | 35 |
| Montréal-Est | 712 | 78 | 634 | 0 | **634** | 154 (24 %) | 6 |
| Beaconsfield | 1 095 | 535 | 560 | 0 | **560** |  | 41 |
| Sainte-Anne-de-Bellevue | 563 | 29 | 534 | 0 | **534** | 9 (2 %) | 19 |
| Kirkland | 492 | 1 | 491 | 0 | **491** | 1 (0 %) | 28 |
| Mont-Royal | 390 | 0 | 390 | 0 | **390** |  | 32 |
| Senneville | 928 | 558 | 370 | 0 | **370** | 4 (1 %) | 4 |
| Côte-Saint-Luc | 352 | 0 | 352 | 0 | **352** | 10 (3 %) | 27 |
| Baie-D'Urfé | 383 | 79 | 304 | 0 | **304** |  | 17 |
| Westmount | 202 | 0 | 202 | 0 | **202** |  | 18 |
| Hampstead | 92 | 0 | 92 | 0 | **92** |  | 13 |
| Montréal-Ouest | 71 | 0 | 71 | 0 | **71** |  | 12 |
| L'Île-Dorval | 8 | 0 | 8 | 0 | **8** |  |  |

## Arrondissements et quartiers (19)

| Zone | Ville | Brut | Eau | Sans eau | Restr. | Comptées | Sans chemin | Parcs |
|---|---|---:|---:|---:|---:|---:|---:|---:|
| Saint-Laurent | montreal | 2 190 | 4 | 2 186 | 194 | **1 992** |  | 70 |
| Rivière-des-Prairies–Pointe-aux-Trembles | montreal | 2 520 | 339 | 2 181 | 6 | **2 175** |  | 115 |
| Pierrefonds-Roxboro | montreal | 1 668 | 287 | 1 381 | 0 | **1 381** |  | 80 |
| Mercier–Hochelaga-Maisonneuve | montreal | 1 396 | 98 | 1 298 | 47 | **1 251** |  | 91 |
| Ahuntsic-Cartierville | montreal | 1 239 | 1 | 1 238 | 0 | **1 238** |  | 67 |
| L'Île-Bizard–Sainte-Geneviève | montreal | 1 812 | 618 | 1 194 | 0 | **1 194** |  | 47 |
| Côte-des-Neiges–Notre-Dame-de-Grâce | montreal | 1 084 | 0 | 1 084 | 0 | **1 084** |  | 55 |
| Lachine | montreal | 1 125 | 218 | 907 | 0 | **907** |  | 41 |
| Villeray–Saint-Michel–Parc-Extension | montreal | 839 | 8 | 831 | 0 | **831** |  | 54 |
| LaSalle | montreal | 1 250 | 423 | 827 | 0 | **827** |  | 50 |
| Rosemont–La Petite-Patrie | montreal | 810 | 0 | 810 | 0 | **810** |  | 67 |
| Ville-Marie | montreal | 1 094 | 294 | 800 | 0 | **800** |  | 148 |
| Le Sud-Ouest | montreal | 915 | 117 | 798 | 0 | **798** |  | 106 |
| Anjou | montreal | 705 | 3 | 702 | 0 | **702** |  | 26 |
| Saint-Léonard | montreal | 691 | 0 | 691 | 0 | **691** |  | 32 |
| Montréal-Nord | montreal | 638 | 75 | 563 | 0 | **563** |  | 34 |
| Verdun | montreal | 1 071 | 589 | 482 | 0 | **482** |  | 56 |
| Le Plateau-Mont-Royal | montreal | 416 | 3 | 413 | 0 | **413** |  | 57 |
| Outremont | montreal | 198 | 1 | 197 | 0 | **197** |  | 16 |

## Îles à polygone propre

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Sans chemin | Parcs |
|---|---:|---:|---:|---:|---:|---:|---:|
| Parc Jean-Drapeau | 135 | 25 | 110 | 0 | **110** |  | 2 |

## Parcs (1552)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Grand Parc de l'Ouest ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 462 |
| Refuge d'oiseaux migrateurs de Senneville ⚠️ | Sainte-Anne-de-Bellevue › Île de Montréal | 279 |
| Grand Parc de l'Ouest (2) ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 187 |
| Parc-nature du Bois-de-l'Île-Bizard ⚠️ | Montréal › L'Île-Bizard–Sainte-Geneviève › Île de Montréal | 156 |
| Arboretum Morgan ⚠️ | Sainte-Anne-de-Bellevue › Île de Montréal | 134 |
| Parc-nature de la Pointe-aux-Prairies ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 132 |
| Parc du Mont-Royal | Montréal › Ville-Marie › Île de Montréal | 96 |
| Parc agricole du Bois-de-la-Roche | Senneville › Île de Montréal | 90 |
| Parc-nature du Bois-de-Liesse | Montréal › Saint-Laurent › Île de Montréal | 87 |
| Parc Jean-Drapeau | Montréal › Ville-Marie › Parc Jean-Drapeau | 84 |
| Refuge d'oiseaux migrateurs de l'Île-aux-Hérons | Montréal › LaSalle › Île de Montréal | 75 |
| Parc-nature du Bois-de-Saraguay | Montréal › Ahuntsic-Cartierville › Île de Montréal | 43 |
| Parc Angrignon | Montréal › Le Sud-Ouest › Île de Montréal | 42 |
| Jardin botanique de Montréal | Montréal › Rosemont–La Petite-Patrie › Île de Montréal | 41 |
| Parc Frédéric-Back | Montréal › Villeray–Saint-Michel–Parc-Extension › Île de Montréal | 33 |
| Parc du Canal-de-Lachine | Montréal › Le Sud-Ouest › Île de Montréal | 32 |
| Parc Maisonneuve | Montréal › Rosemont–La Petite-Patrie › Île de Montréal | 31 |
| Parc olympique | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 23 |
| Parc-nature des Rapides-du-Cheval-Blanc | Montréal › Pierrefonds-Roxboro › Île de Montréal | 22 |
| Parc écologique des Sources | Montréal › Saint-Laurent › Île de Montréal | 22 |
| Parc Terra Cotta | Pointe-Claire › Île de Montréal | 20 |
| Parc-nature du Bois-d'Anjou | Montréal › Anjou › Île de Montréal | 20 |
| Parc Jarry | Montréal › Villeray–Saint-Michel–Parc-Extension › Île de Montréal | 19 |
| Parc de la Coulée-Grou (2) | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 19 |
| Parc Marcel-Laurin | Montréal › Saint-Laurent › Île de Montréal | 18 |
| Parc du Centenaire | Dollard-des-Ormeaux › Île de Montréal | 17 |
| Parc de l'Honorable-George-O'Reilly | Montréal › Verdun › Île de Montréal | 16 |
| Parc-nature du Ruisseau-De-Montigny | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 16 |
| Parc La Fontaine | Montréal › Le Plateau-Mont-Royal › Île de Montréal | 15 |
| Parc de la Promenade-Bellerive | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 15 |
| Vieux-Port | Montréal › Ville-Marie › Île de Montréal | 15 |
| Parc-nature de l'Île-de-la-Visitation | Montréal › Ahuntsic-Cartierville › Île de Montréal | 15 |
| Domaine Saint-Paul | Montréal › Verdun › Île de Montréal | 12 |
| Parc Marcelin-Wilson | Montréal › Ahuntsic-Cartierville › Île de Montréal | 12 |
| Parc Tiohtià:ke Otsira'kéhne | Montréal › Côte-des-Neiges–Notre-Dame-de-Grâce › Île de Montréal | 11 |
| Parc des Rapides | Montréal › LaSalle › Île de Montréal | 11 |
| Parc Arthur-Therrien | Montréal › Verdun › Île de Montréal | 10 |
| Parc de l'Aqueduc | Montréal › Verdun › Île de Montréal | 10 |
| Parc du Père-Marquette ⚠️ | Montréal › Rosemont–La Petite-Patrie › Île de Montréal | 9 |
| Parc de Montreal (54) ⚠️ | Montréal › Ville-Marie › Île de Montréal | 9 |
| Parc des Hirondelles ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 8 |
| Parc Jeanne-Mance ⚠️ | Montréal › Le Plateau-Mont-Royal › Île de Montréal | 8 |
| Parc Thomas-Chapais ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 8 |
| Parc Pasquale-Gattuso ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 8 |
| Parc Fritz ⚠️ | Baie-D'Urfé › Île de Montréal | 8 |
| Parc Philippe-Laheurte ⚠️ | Montréal › Saint-Laurent › Île de Montréal | 8 |
| McGill Bird Observatory ⚠️ | Sainte-Anne-de-Bellevue › Île de Montréal | 8 |
| Parc de la Traversée ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 8 |
| Terrains du centre communautaire Sarto-Desnoyers ⚠️ | Dorval › Île de Montréal | 7 |
| Parc Henri-Julien ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 7 |
| Parc René-Lévesque ⚠️ | Montréal › Lachine › Île de Montréal | 7 |
| Parc LaSalle ⚠️ | Montréal › Lachine › Île de Montréal | 7 |
| Parc d'Anjou-sur-le-Lac ⚠️ | Montréal › Anjou › Île de Montréal | 7 |
| Parc Sir-Wilfrid-Laurier ⚠️ | Montréal › Le Plateau-Mont-Royal › Île de Montréal | 6 |
| Parc Félix-Leclerc ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 6 |
| Parc Ahuntsic ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 6 |
| Parc Eugène-Dostie ⚠️ | Montréal › L'Île-Bizard–Sainte-Geneviève › Île de Montréal | 6 |
| Parc Delorme ⚠️ | Montréal › Saint-Léonard › Île de Montréal | 6 |
| Parc Ignace-Bourget ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 6 |
| Parc du Bois-Franc (2) ⚠️ | Montréal › Saint-Laurent › Île de Montréal | 6 |
| Parc Pierre Elliott Trudeau ⚠️ | Côte-Saint-Luc › Île de Montréal | 6 |
| Parc Adrien-D.-Archambault ⚠️ | Montréal › Verdun › Île de Montréal | 6 |
| Parc des Bénévoles (2) ⚠️ | Kirkland › Île de Montréal | 6 |
| Parc Monseigneur J.-A.-Richard ⚠️ | Montréal › Verdun › Île de Montréal | 5 |
| Parc Grier ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 5 |
| Parc Clémentine-De la Rousselière ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 5 |
| Parc Armand-Bombardier ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 5 |
| Parc Maynard-Ferguson ⚠️ | Montréal › Verdun › Île de Montréal | 5 |
| Parc Martin-Luther-King ⚠️ | Montréal › Côte-des-Neiges–Notre-Dame-de-Grâce › Île de Montréal | 5 |
| Parc de Montreal (143) ⚠️ | Montréal › LaSalle › Île de Montréal | 5 |
| Parc Duval ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 5 |
| Parc Cedar Park Heights ⚠️ | Pointe-Claire › Île de Montréal | 4 |
| Parc André-Lavallée ⚠️ | Montréal › Rosemont–La Petite-Patrie › Île de Montréal | 4 |
| Parc de la Louisiane ⚠️ | Montréal › Rosemont–La Petite-Patrie › Île de Montréal | 4 |
| Parc Sainte-Bernadette ⚠️ | Montréal › Rosemont–La Petite-Patrie › Île de Montréal | 4 |
| Parc Étienne-Desmarteau ⚠️ | Montréal › Rosemont–La Petite-Patrie › Île de Montréal | 4 |
| King George Park ⚠️ | Westmount › Île de Montréal | 4 |
| Parc Saint-Laurent ⚠️ | Montréal › Saint-Laurent › Île de Montréal | 4 |
| Parc Le Ber ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 4 |
| Parc Daniel-Johnson (2) ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 4 |
| Parc de Montreal (15) ⚠️ | Montréal › Ville-Marie › Parc Jean-Drapeau | 4 |
| Parc Louis-Riel ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 4 |
| Parc Riverside ⚠️ | Montréal › LaSalle › Île de Montréal | 4 |
| Parc Lake Road ⚠️ | Dollard-des-Ormeaux › Île de Montréal | 4 |
| Parc Edward Janiszewski ⚠️ | Dollard-des-Ormeaux › Île de Montréal | 4 |
| Parc des Cageux ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 4 |
| Parc de Montreal (53) ⚠️ | Montréal › Ville-Marie › Île de Montréal | 4 |
| Parc Giuseppe-Garibaldi ⚠️ | Montréal › Saint-Léonard › Île de Montréal | 4 |
| Parc Lucie-Bruneau ⚠️ | Montréal › Anjou › Île de Montréal | 4 |
| Parc Villeray ⚠️ | Montréal › Villeray–Saint-Michel–Parc-Extension › Île de Montréal | 4 |
| Parc Don-Bosco ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 4 |
| Parc George-Springate ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 4 |
| Parc de l'école secondaire de la Pointe-aux-Trembles ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 4 |
| Parc de Beaconsfield (9) ⚠️ | Beaconsfield › Île de Montréal | 4 |
| Parc Ladauversière ⚠️ | Montréal › Saint-Léonard › Île de Montréal | 4 |
| Parc Westmount ⚠️ | Westmount › Île de Montréal | 4 |
| Parc Hampstead ⚠️ | Hampstead › Île de Montréal | 4 |
| Parc Pie-XII ⚠️ | Montréal › Saint-Léonard › Île de Montréal | 4 |
| Parc Hébert (2) ⚠️ | Montréal › Saint-Léonard › Île de Montréal | 4 |
| Parc Sunnyside ⚠️ | Pointe-Claire › Île de Montréal | 3 |
| Parc du Pélican ⚠️ | Montréal › Rosemont–La Petite-Patrie › Île de Montréal | 3 |
| Parc Danyluk ⚠️ | Mont-Royal › Île de Montréal | 3 |
| Parc City Lane ⚠️ | Beaconsfield › Île de Montréal | 3 |
| Parc Surrey ⚠️ | Dorval › Île de Montréal | 3 |
| Parc Saint-Charles ⚠️ | Dorval › Île de Montréal | 3 |
| Parc du Boisé-de-Saint-Sulpice ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 3 |
| Parc Marguerite-Bourgeoys ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 3 |
| Parc Sauvé ⚠️ | Montréal › Montréal-Nord › Île de Montréal | 3 |
| Parc Coubertin ⚠️ | Montréal › Saint-Léonard › Île de Montréal | 3 |
| Parc Westminster ⚠️ | Dollard-des-Ormeaux › Île de Montréal | 3 |
| Parc Frederick T. Wilson ⚠️ | Dollard-des-Ormeaux › Île de Montréal | 3 |
| Parc de Beauséjour ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 3 |
| Lieu historique national du Canal-de-Lachine ⚠️ | Montréal › Lachine › Île de Montréal | 3 |
| Parc Pierre-Bédard ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 3 |
| Parc de Louisbourg ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 3 |
| Parc Valois ⚠️ | Pointe-Claire › Île de Montréal | 3 |
| Parc Raymond (2) ⚠️ | Montréal › LaSalle › Île de Montréal | 3 |
| Parc Benny ⚠️ | Montréal › Côte-des-Neiges–Notre-Dame-de-Grâce › Île de Montréal | 3 |
| Parc Brook ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 3 |
| Parc Carlos d'Alcantara ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 3 |
| Parc du Boisé Jean-Milot ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 3 |
| Parc Roger-Rousseau ⚠️ | Montréal › Anjou › Île de Montréal | 3 |
| Parc de Montreal (60) ⚠️ | Montréal › Ville-Marie › Île de Montréal | 3 |
| Parc Sainte-Marthe ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 3 |
| Parc Campbell Ouest ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 3 |
| Parc de Stewart Hall ⚠️ | Pointe-Claire › Île de Montréal | 3 |
| Parc Bertold ⚠️ | Baie-D'Urfé › Île de Montréal | 3 |
| Parc Yuile ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 3 |
| Parc de Montreal (82) ⚠️ | Montréal › Montréal-Nord › Île de Montréal | 3 |
| Parc Cité-Jardin ⚠️ | Montréal › Rosemont–La Petite-Patrie › Île de Montréal | 3 |
| Parc des Arbres ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 3 |
| Parc Ferland ⚠️ | Montréal › Saint-Léonard › Île de Montréal | 3 |
| Parc J.-Albert-Gariépy ⚠️ | Montréal › Verdun › Île de Montréal | 3 |
| Parc Mackenzie-King ⚠️ | Montréal › Côte-des-Neiges–Notre-Dame-de-Grâce › Île de Montréal | 3 |
| Parc Maurice-Richard (2) ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 3 |
| Parc Westwood (2) ⚠️ | Dollard-des-Ormeaux › Île de Montréal | 3 |
| Parc Spring Garden ⚠️ | Dollard-des-Ormeaux › Île de Montréal | 3 |
| Parc Sainte-Odile ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 3 |
| parc des Bateliers ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 3 |
| Parc de la Merci ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 3 |
| Parc Lefebvre (2) ⚠️ | Montréal › LaSalle › Île de Montréal | 3 |
| Parc Trenholme ⚠️ | Montréal › Côte-des-Neiges–Notre-Dame-de-Grâce › Île de Montréal | 3 |
| Parc Loyola ⚠️ | Montréal › Côte-des-Neiges–Notre-Dame-de-Grâce › Île de Montréal | 3 |
| Parc Stoney Point ⚠️ | Montréal › Lachine › Île de Montréal | 3 |
| Parc Ermanno-La Riccia ⚠️ | Montréal › Saint-Léonard › Île de Montréal | 3 |
| Bassin de la Brunante ⚠️ | Montréal › Saint-Laurent › Île de Montréal | 3 |
| Parc Gouin (4) ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 3 |
| Parc de Montreal (163) ⚠️ | Montréal › Rosemont–La Petite-Patrie › Île de Montréal | 3 |
| Parc Honoré-Mercier (2) ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 3 |
| Parc de West Vancouver ⚠️ | Montréal › Verdun › Île de Montréal | 3 |
| Parc Dollard-des-Ormeaux ⚠️ | Dollard-des-Ormeaux › Île de Montréal | 3 |
| Parc Lacharité ⚠️ | Montréal › LaSalle › Île de Montréal | 3 |
| Parc Alexandre-Bourgeau ⚠️ | Pointe-Claire › Île de Montréal | 2 |
| Parc Hermitage ⚠️ | Pointe-Claire › Île de Montréal | 2 |
| Parc Northview ⚠️ | Pointe-Claire › Île de Montréal | 2 |
| Parc Arthur-E.-Séguin ⚠️ | Pointe-Claire › Île de Montréal | 2 |
| Parc Centennial ⚠️ | Beaconsfield › Île de Montréal | 2 |
| Parc Windsor ⚠️ | Dorval › Île de Montréal | 2 |
| Parc du Millénaire ⚠️ | Dorval › Île de Montréal | 2 |
| Parc Jean-Martucci ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 2 |
| Parc Jean-Amyot ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 2 |
| Parc Saint-Donat ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 2 |
| Parc de l'Ancienne-Pépinière ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 2 |
| Parc Beaubien (2) ⚠️ | Montréal › Rosemont–La Petite-Patrie › Île de Montréal | 2 |
| Parc de l'Hôtel-de-Ville ⚠️ | Montréal-Est › Île de Montréal | 2 |
| Parc Saint-Simon-Apôtre ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 2 |
| Parc François-Perrault ⚠️ | Montréal › Villeray–Saint-Michel–Parc-Extension › Île de Montréal | 2 |
| Parc Pierre-Bernard ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 2 |
| Parc Terry Fox ⚠️ | Dollard-des-Ormeaux › Île de Montréal | 2 |
| Parc Champêtre ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 2 |
| Parc Jean-Duceppe ⚠️ | Montréal › Rosemont–La Petite-Patrie › Île de Montréal | 2 |
| Parc Aimé-Caron ⚠️ | Montréal › Saint-Laurent › Île de Montréal | 2 |
| Parc Cousineau ⚠️ | Montréal › Saint-Laurent › Île de Montréal | 2 |
| Parc Noël-Sud ⚠️ | Montréal › Saint-Laurent › Île de Montréal | 2 |
| Parc Noël-Nord ⚠️ | Montréal › Saint-Laurent › Île de Montréal | 2 |
| Parc de la Reine-Élisabeth ⚠️ | Montréal › Verdun › Île de Montréal | 2 |
| Parc Alexis-Nihon ⚠️ | Montréal › Saint-Laurent › Île de Montréal | 2 |
| Parc Pilon ⚠️ | Montréal › Montréal-Nord › Île de Montréal | 2 |
| Parc Gabriel-Lalemant ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 2 |
| Parc Aimé-Léonard ⚠️ | Montréal › Montréal-Nord › Île de Montréal | 2 |
| Parc Henri-Bourassa ⚠️ | Montréal › Montréal-Nord › Île de Montréal | 2 |
| Parc Pierre-Tétrault ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 2 |
| Parc Champdoré ⚠️ | Montréal › Villeray–Saint-Michel–Parc-Extension › Île de Montréal | 2 |
| Parc Joyce ⚠️ | Montréal › Outremont › Île de Montréal | 2 |
| Parc du Boisé-Roxboro ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 2 |
| Parc Lalancette ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 2 |
| Parc Elm ⚠️ | Dollard-des-Ormeaux › Île de Montréal | 2 |
| Parc Dan-Hanganu ⚠️ | Montréal › Verdun › Île de Montréal | 2 |
| Parc Baldwin ⚠️ | Montréal › Le Plateau-Mont-Royal › Île de Montréal | 2 |
| Parc Baldwin (2) ⚠️ | Montréal › Le Plateau-Mont-Royal › Île de Montréal | 2 |
| Parc Van Horne ⚠️ | Montréal › Côte-des-Neiges–Notre-Dame-de-Grâce › Île de Montréal | 2 |
| Parc Joseph-Paré (2) ⚠️ | Montréal › Rosemont–La Petite-Patrie › Île de Montréal | 2 |
| Parc Edward J. Kirwan ⚠️ | Côte-Saint-Luc › Île de Montréal | 2 |
| Parc Cavelier-De LaSalle ⚠️ | Montréal › LaSalle › Île de Montréal | 2 |
| Parc-école Laurier-Macdonald ⚠️ | Montréal › Saint-Léonard › Île de Montréal | 2 |
| Parc Leroux ⚠️ | Montréal › LaSalle › Île de Montréal | 2 |
| Parc Graham ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 2 |
| Parc Fairview ⚠️ | Dollard-des-Ormeaux › Île de Montréal | 2 |
| Parc de la Savane ⚠️ | Montréal › Côte-des-Neiges–Notre-Dame-de-Grâce › Île de Montréal | 2 |
| Parc Nelson-Mandela ⚠️ | Montréal › Côte-des-Neiges–Notre-Dame-de-Grâce › Île de Montréal | 2 |
| Parc Dollard-Morin ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 2 |
| Parc de Montreal (33) ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 2 |
| Parc du Château-Pierrefonds ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 2 |
| Parc de Montreal (37) ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 2 |
| Parc Saint-Joseph (2) ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 2 |
| Parc André-Laurendeau ⚠️ | Montréal › Anjou › Île de Montréal | 2 |
| Parc Goncourt ⚠️ | Montréal › Anjou › Île de Montréal | 2 |
| Parc Carignan (2) ⚠️ | Montréal › Lachine › Île de Montréal | 2 |
| Parc Herb-Trawick ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 2 |
| Parc de Montreal (66) ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 2 |
| Parc Francine-Léger ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 2 |
| Parc Liébert ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 2 |
| Parc Chénier-Beaugrand ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 2 |
| Parc Francesca-Cabrini ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 2 |
| Parc Luigi-Pirandello ⚠️ | Montréal › Saint-Léonard › Île de Montréal | 2 |
| Parc René-Goupil ⚠️ | Montréal › Villeray–Saint-Michel–Parc-Extension › Île de Montréal | 2 |
| Parc de Montreal (71) ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 2 |
| Parc Summerlea ⚠️ | Montréal › Lachine › Île de Montréal | 2 |
| Parc Sunnybrooke ⚠️ | Dollard-des-Ormeaux › Île de Montréal | 2 |
| Parc Héritage-sur-le-Lac ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 2 |
| Port de Plaisance de Pierrefonds ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 2 |
| Parc Moulin-du-Rapide ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 2 |
| Parc Marie-Cardinal ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 2 |
| Parc Atholstan ⚠️ | Mont-Royal › Île de Montréal | 2 |
| Parc Léon-Brisebois ⚠️ | Montréal › L'Île-Bizard–Sainte-Geneviève › Île de Montréal | 2 |
| Parc Allan's Hill ⚠️ | Baie-D'Urfé › Île de Montréal | 2 |
| Parc Clément-Jetté Nord ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 2 |
| Parc des Roseraies ⚠️ | Montréal › Anjou › Île de Montréal | 2 |
| Parc de Montreal (97) ⚠️ | Montréal › Saint-Laurent › Île de Montréal | 2 |
| Parc Saint-Benoît ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 2 |
| Parc d'A-Ma-Baie ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 2 |
| Parc Rhian-Wilkinson ⚠️ | Baie-D'Urfé › Île de Montréal | 2 |
| Parc Pine Beach ⚠️ | Dorval › Île de Montréal | 2 |
| Parc Simone-Dénéchaud ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 2 |
| Place des Montréalaises ⚠️ | Montréal › Ville-Marie › Île de Montréal | 2 |
| Parc de Dollard-Des-Ormeaux (5) ⚠️ | Dollard-des-Ormeaux › Île de Montréal | 2 |
| Parc de Dollard-Des-Ormeaux (6) ⚠️ | Dollard-des-Ormeaux › Île de Montréal | 2 |
| Parc Meades ⚠️ | Kirkland › Île de Montréal | 2 |
| Parc Grovehill ⚠️ | Montréal › Lachine › Île de Montréal | 2 |
| Hayward Park ⚠️ | Montréal › LaSalle › Île de Montréal | 2 |
| Parc de Montreal (132) ⚠️ | Montréal › LaSalle › Île de Montréal | 2 |
| Parc Ranger ⚠️ | Montréal › LaSalle › Île de Montréal | 2 |
| Parc de la Vérendrye ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 2 |
| Parc Félix-Leclerc (6) ⚠️ | Montréal › LaSalle › Île de Montréal | 2 |
| Parc Notre-Dame-de-Grâce ⚠️ | Montréal › Côte-des-Neiges–Notre-Dame-de-Grâce › Île de Montréal | 2 |
| Parc Georges-Saint-Pierre ⚠️ | Montréal › Côte-des-Neiges–Notre-Dame-de-Grâce › Île de Montréal | 2 |
| Parc Pehr-Kalm ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 2 |
| Parc Saint-Alphonse (2) ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 2 |
| Parc de Montreal (158) ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 2 |
| Parc Dalbé-Viau ⚠️ | Montréal › Lachine › Île de Montréal | 2 |
| Parc Windermere ⚠️ | Beaconsfield › Île de Montréal | 2 |
| Parc de la Rivière-Disparue ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 2 |
| Parc des Vannes de l'Aqueduc ⚠️ | Montréal › LaSalle › Île de Montréal | 2 |
| Parc Morgan (2) ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 2 |
| Parc Hartenstein ⚠️ | Montréal › Saint-Laurent › Île de Montréal | 2 |
| Parc de la Confédération ⚠️ | Montréal › Côte-des-Neiges–Notre-Dame-de-Grâce › Île de Montréal | 2 |
| Parc Jean-Jacques Rouseau ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 2 |
| Parc George-Vernot ⚠️ | Montréal › Villeray–Saint-Michel–Parc-Extension › Île de Montréal | 2 |
| Parc linéaire du Premier-Chemin-de-Fer ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 2 |
| Parc Wilfrid-Bastien ⚠️ | Montréal › Saint-Léonard › Île de Montréal | 2 |
| Parc Clearpoint ⚠️ | Pointe-Claire › Île de Montréal | 1 |
| Parc Saint-Viateur ⚠️ | Montréal › Outremont › Île de Montréal | 1 |
| Parc Beaubien ⚠️ | Montréal › Outremont › Île de Montréal | 1 |
| Parc Seigniory ⚠️ | Pointe-Claire › Île de Montréal | 1 |
| Newton Square ⚠️ | Pointe-Claire › Île de Montréal | 1 |
| Parc Maple ⚠️ | Pointe-Claire › Île de Montréal | 1 |
| Parc Jack-Robinson ⚠️ | Pointe-Claire › Île de Montréal | 1 |
| Parc Marsh & Stockwell ⚠️ | Pointe-Claire › Île de Montréal | 1 |
| Parc D.W. Beck ⚠️ | Pointe-Claire › Île de Montréal | 1 |
| Parc de Pointe-Claire (6) ⚠️ | Pointe-Claire › Île de Montréal | 1 |
| Lower Field ⚠️ | Montréal › Ville-Marie › Île de Montréal | 1 |
| Parc J.-Arthur-Champagne ⚠️ | Montréal › Rosemont–La Petite-Patrie › Île de Montréal | 1 |
| Parc Joseph-N.-Drapeau ⚠️ | Montréal › Rosemont–La Petite-Patrie › Île de Montréal | 1 |
| Parc Saint-Émile ⚠️ | Montréal › Rosemont–La Petite-Patrie › Île de Montréal | 1 |
| Parc de Normanville ⚠️ | Montréal › Villeray–Saint-Michel–Parc-Extension › Île de Montréal | 1 |
| Parc Le Prévost ⚠️ | Montréal › Villeray–Saint-Michel–Parc-Extension › Île de Montréal | 1 |
| Parc Mohawk ⚠️ | Mont-Royal › Île de Montréal | 1 |
| Parc de Beaconsfield ⚠️ | Beaconsfield › Île de Montréal | 1 |
| Brookside Park ⚠️ | Beaconsfield › Île de Montréal | 1 |
| Parc de Beaconsfield (2) ⚠️ | Beaconsfield › Île de Montréal | 1 |
| Parc Shannon ⚠️ | Beaconsfield › Île de Montréal | 1 |
| Parc Royal ⚠️ | Beaconsfield › Île de Montréal | 1 |
| Parc Beaconsfield Heights ⚠️ | Beaconsfield › Île de Montréal | 1 |
| Parc Beacon Hill ⚠️ | Beaconsfield › Île de Montréal | 1 |
| Parc Paiement ⚠️ | Kirkland › Île de Montréal | 1 |
| Parc Kirkland ⚠️ | Kirkland › Île de Montréal | 1 |
| Place De La Dauversière ⚠️ | Montréal › Ville-Marie › Île de Montréal | 1 |
| Parc Héritage ⚠️ | Kirkland › Île de Montréal | 1 |
| Parc Houde ⚠️ | Kirkland › Île de Montréal | 1 |
| Square Dorchester ⚠️ | Montréal › Ville-Marie › Île de Montréal | 1 |
| Parc Ecclestone ⚠️ | Kirkland › Île de Montréal | 1 |
| Parc Rutherford ⚠️ | Montréal › Ville-Marie › Île de Montréal | 1 |
| Parc Aumais ⚠️ | Sainte-Anne-de-Bellevue › Île de Montréal | 1 |
| Parc William-Bowie ⚠️ | Montréal › Côte-des-Neiges–Notre-Dame-de-Grâce › Île de Montréal | 1 |
| Parc du Voyageur ⚠️ | Pointe-Claire › Île de Montréal | 1 |
| Parc Westwood ⚠️ | Dorval › Île de Montréal | 1 |
| Parc Courtland ⚠️ | Dorval › Île de Montréal | 1 |
| Parc Dorval ⚠️ | Dorval › Île de Montréal | 1 |
| Parc Ballantyne ⚠️ | Dorval › Île de Montréal | 1 |
| Parc Tolhurst ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 1 |
| Parc De Lotbinière ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 1 |
| Parc Willibrord ⚠️ | Montréal › Verdun › Île de Montréal | 1 |
| Parc Beurling ⚠️ | Montréal › Verdun › Île de Montréal | 1 |
| Parc de l'Ukraine ⚠️ | Montréal › Rosemont–La Petite-Patrie › Île de Montréal | 1 |
| Parc Jeanotte ⚠️ | Montréal › LaSalle › Île de Montréal | 1 |
| Parc Saint-Jean-Baptiste ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc de Montréal-Est ⚠️ | Montréal-Est › Île de Montréal | 1 |
| Parc Émilie-Gamelin ⚠️ | Montréal › Ville-Marie › Île de Montréal | 1 |
| Parc Alphonse-Télesphore-Lépine ⚠️ | Montréal › Le Plateau-Mont-Royal › Île de Montréal | 1 |
| Parc Garneau ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 1 |
| Parc Oscar-Peterson ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 1 |
| Parc Saint-Victor ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 1 |
| Parc Connaught ⚠️ | Mont-Royal › Île de Montréal | 1 |
| Parc Jos-Montferrand ⚠️ | Montréal › Ville-Marie › Île de Montréal | 1 |
| Parc du Mail ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 1 |
| Parc Sir-George-Étienne-Cartier ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 1 |
| Parc Hamilton ⚠️ | Mont-Royal › Île de Montréal | 1 |
| Parc Maynard-Metcalf ⚠️ | Mont-Royal › Île de Montréal | 1 |
| Parc Berthe-Louard ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 1 |
| Parc de Westmount ⚠️ | Westmount › Île de Montréal | 1 |
| Parc Gohier ⚠️ | Montréal › Saint-Laurent › Île de Montréal | 1 |
| Parc Beaulac ⚠️ | Montréal › Saint-Laurent › Île de Montréal | 1 |
| Parc Dr-Bernard-Paquet ⚠️ | Montréal › Saint-Laurent › Île de Montréal | 1 |
| Parc Isaac-Abrabanel ⚠️ | Montréal › Saint-Laurent › Île de Montréal | 1 |
| Parc Marlborough ⚠️ | Montréal › Saint-Laurent › Île de Montréal | 1 |
| Parc Poirier ⚠️ | Montréal › Saint-Laurent › Île de Montréal | 1 |
| Parc de Montreal (6) ⚠️ | Montréal › Saint-Laurent › Île de Montréal | 1 |
| Parc Gold ⚠️ | Montréal › Saint-Laurent › Île de Montréal | 1 |
| Parc Chamberland ⚠️ | Montréal › Saint-Laurent › Île de Montréal | 1 |
| Parc Dakin ⚠️ | Mont-Royal › Île de Montréal | 1 |
| Parc Ottawa ⚠️ | Montréal › Montréal-Nord › Île de Montréal | 1 |
| Parc Prieur ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 1 |
| Parc J. J. Gagnier ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 1 |
| Parc Lacordaire ⚠️ | Montréal › Montréal-Nord › Île de Montréal | 1 |
| Parc Saint-Laurent (3) ⚠️ | Montréal › Montréal-Nord › Île de Montréal | 1 |
| Parc Le Carignan ⚠️ | Montréal › Montréal-Nord › Île de Montréal | 1 |
| Parc Molson ⚠️ | Montréal › Rosemont–La Petite-Patrie › Île de Montréal | 1 |
| Parc Applewood ⚠️ | Hampstead › Île de Montréal | 1 |
| Parc Aldred ⚠️ | Hampstead › Île de Montréal | 1 |
| Parc L.-O.-Taillon ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 1 |
| Place Henri-Dunant ⚠️ | Montréal › Ville-Marie › Île de Montréal | 1 |
| Parc Beauclerk ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 1 |
| Parc Théodore ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 1 |
| Parc François-Vaillancourt ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc de Montreal (11) ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc Saint-Georges ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc Joseph-Avila-Proulx ⚠️ | Montréal › L'Île-Bizard–Sainte-Geneviève › Île de Montréal | 1 |
| Place de la Paix ⚠️ | Montréal › Ville-Marie › Île de Montréal | 1 |
| Parc de la Coulée-Grou ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc Ouellette ⚠️ | Montréal › LaSalle › Île de Montréal | 1 |
| Parc Hochelaga ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 1 |
| Parc Wolfred-Nelson ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 1 |
| Parc Ovila-Pelletier ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 1 |
| Parc Édouard-Raymond-Fabre ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 1 |
| Square Dézéry ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 1 |
| Place de la Grande-Paix-de-Montréal ⚠️ | Montréal › Ville-Marie › Île de Montréal | 1 |
| Parc Coolbrooke ⚠️ | Dollard-des-Ormeaux › Île de Montréal | 1 |
| Parc Saint-Aloysius ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 1 |
| Parc Dunkerque ⚠️ | Montréal › Côte-des-Neiges–Notre-Dame-de-Grâce › Île de Montréal | 1 |
| Parc Desmarest ⚠️ | Montréal › L'Île-Bizard–Sainte-Geneviève › Île de Montréal | 1 |
| Parc Jonathan-Wilson ⚠️ | Montréal › L'Île-Bizard–Sainte-Geneviève › Île de Montréal | 1 |
| Parc Nesbitt ⚠️ | Montréal › Rosemont–La Petite-Patrie › Île de Montréal | 1 |
| Parc Alouette ⚠️ | Dollard-des-Ormeaux › Île de Montréal | 1 |
| Parc Ambassador ⚠️ | Pointe-Claire › Île de Montréal | 1 |
| Parc de la Fontaine ⚠️ | Montréal › Verdun › Île de Montréal | 1 |
| Parc du Pied-du-Courant ⚠️ | Montréal › Ville-Marie › Île de Montréal | 1 |
| Parc des Éclusiers ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 1 |
| Parc Saint-Pierre-Claver ⚠️ | Montréal › Le Plateau-Mont-Royal › Île de Montréal | 1 |
| Parc des Compagnons-de-Saint-Laurent ⚠️ | Montréal › Le Plateau-Mont-Royal › Île de Montréal | 1 |
| Parc Olivier-Robert ⚠️ | Montréal › Ville-Marie › Île de Montréal | 1 |
| Parc Saint-Louis ⚠️ | Montréal › Lachine › Île de Montréal | 1 |
| Parc MacDonald ⚠️ | Montréal › Côte-des-Neiges–Notre-Dame-de-Grâce › Île de Montréal | 1 |
| Parc Desmarchais ⚠️ | Montréal › Verdun › Île de Montréal | 1 |
| Parc Saint-Gabriel ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 1 |
| Parc Raimbault ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 1 |
| Parc des Locomotives ⚠️ | Montréal › Rosemont–La Petite-Patrie › Île de Montréal | 1 |
| Parc des Carrières ⚠️ | Montréal › Rosemont–La Petite-Patrie › Île de Montréal | 1 |
| Parc Nicolas-Tillemont ⚠️ | Montréal › Villeray–Saint-Michel–Parc-Extension › Île de Montréal | 1 |
| Parc Julie-Hamelin ⚠️ | Montréal › Villeray–Saint-Michel–Parc-Extension › Île de Montréal | 1 |
| Parc Yitzchak Rabin ⚠️ | Côte-Saint-Luc › Île de Montréal | 1 |
| Champ des Possibles ⚠️ | Montréal › Le Plateau-Mont-Royal › Île de Montréal | 1 |
| Parc De Lorimier ⚠️ | Montréal › Le Plateau-Mont-Royal › Île de Montréal | 1 |
| Carré d'Hibernia ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 1 |
| Parc Médéric-Martin (2) ⚠️ | Montréal › Ville-Marie › Île de Montréal | 1 |
| Parc Raymond-Préfontaine ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 1 |
| Carré Viger ⚠️ | Montréal › Ville-Marie › Île de Montréal | 1 |
| Parc Prudence-Heward ⚠️ | Montréal › Ville-Marie › Île de Montréal | 1 |
| Parc des Royaux ⚠️ | Montréal › Ville-Marie › Île de Montréal | 1 |
| Parc Jacques-Viger ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 1 |
| Parc des Faubourgs ⚠️ | Montréal › Ville-Marie › Île de Montréal | 1 |
| Parc du Bois-des-Trottier ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 1 |
| Parc Anderson ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 1 |
| Parc de Montreal (30) ⚠️ | Montréal › Ville-Marie › Île de Montréal | 1 |
| Parc George-Legault ⚠️ | Montréal › L'Île-Bizard–Sainte-Geneviève › Île de Montréal | 1 |
| Parc Alexander ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 1 |
| Parc Irma-Le Vasseur ⚠️ | Montréal › Outremont › Île de Montréal | 1 |
| Parc Robert-Sauvé ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 1 |
| Parc Villeret ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 1 |
| Parc Saint-Clément ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 1 |
| Parc Gilbert-Layton ⚠️ | Montréal › Côte-des-Neiges–Notre-Dame-de-Grâce › Île de Montréal | 1 |
| Parc Somerled ⚠️ | Montréal › Côte-des-Neiges–Notre-Dame-de-Grâce › Île de Montréal | 1 |
| Parc Joseph-Thibaudeau ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 1 |
| Parc Conrad-Poirier ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc Cécile-Bérubé ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc Pierre-Blanchet ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc du Molise ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc Outremont ⚠️ | Montréal › Outremont › Île de Montréal | 1 |
| Parc Léon-Provancher ⚠️ | Montréal › Rosemont–La Petite-Patrie › Île de Montréal | 1 |
| Parc Idola-Saint-Jean ⚠️ | Montréal › Rosemont–La Petite-Patrie › Île de Montréal | 1 |
| Parc Jean-Louis-Beaudry ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 1 |
| Parc Joseph-Octave-Villeneuve ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 1 |
| Parc des Botanistes ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc Joe-Beef ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 1 |
| Parc Montcalm (4) ⚠️ | Montréal › Rosemont–La Petite-Patrie › Île de Montréal | 1 |
| Parc Persillier-Lachapelle ⚠️ | Montréal › Ville-Marie › Île de Montréal | 1 |
| Parc Yves-Thériault ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc Saint-Charles (3) ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 1 |
| Parc Empress ⚠️ | Pointe-Claire › Île de Montréal | 1 |
| Parc de Montreal (39) ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 1 |
| Parc de Montreal (40) ⚠️ | Montréal › L'Île-Bizard–Sainte-Geneviève › Île de Montréal | 1 |
| Parc du Bassin-à-Gravier ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 1 |
| Place Urbain-Baudreau-Graveline ⚠️ | Montréal › Le Plateau-Mont-Royal › Île de Montréal | 1 |
| Parc Gray (2) ⚠️ | Baie-D'Urfé › Île de Montréal | 1 |
| Parc Belmont ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 1 |
| Parc du Bout-de-l'Île ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc Pierre-Payet ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc Saint-Valérien ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Jardins Queen-Elizabeth ⚠️ | Westmount › Île de Montréal | 1 |
| Parc de Westmount (3) ⚠️ | Westmount › Île de Montréal | 1 |
| Parc de la Ferme-Brodie ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 1 |
| Parc de Montreal (64) ⚠️ | Montréal › Rosemont–La Petite-Patrie › Île de Montréal | 1 |
| Parc de la Bruère ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 1 |
| Parc Marie-LeFranc ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc McLearon ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc de Montreal (67) ⚠️ | Montréal › Saint-Léonard › Île de Montréal | 1 |
| Parc de Montreal (69) ⚠️ | Montréal › Rosemont–La Petite-Patrie › Île de Montréal | 1 |
| Parc Jerry-Shears ⚠️ | Montréal › Saint-Laurent › Île de Montréal | 1 |
| Parc Roman-Zytynsky ⚠️ | Montréal › Saint-Laurent › Île de Montréal | 1 |
| Parc Robert-Stephenson ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc Claudine-Vallerand ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc André-Corbeil-Dit-Tranchemontagne ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc Louis-Hébert ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 1 |
| Parc de Montreal (72) ⚠️ | Montréal › LaSalle › Île de Montréal | 1 |
| Parc Rembrandt ⚠️ | Côte-Saint-Luc › Île de Montréal | 1 |
| Parc Nathan-Shuster ⚠️ | Côte-Saint-Luc › Île de Montréal | 1 |
| Parc Mitchell Brownstein ⚠️ | Côte-Saint-Luc › Île de Montréal | 1 |
| Fletcher Park ⚠️ | Côte-Saint-Luc › Île de Montréal | 1 |
| Parc de Côte-Saint-Luc ⚠️ | Côte-Saint-Luc › Île de Montréal | 1 |
| Parc de Côte-Saint-Luc (3) ⚠️ | Côte-Saint-Luc › Île de Montréal | 1 |
| Parc Saint-Jean-de-Matha ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 1 |
| Parc John-Fisher ⚠️ | Pointe-Claire › Île de Montréal | 1 |
| Parc de Dorval (3) ⚠️ | Dorval › Île de Montréal | 1 |
| Parc de Montreal (74) ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 1 |
| Parc de Kirkland ⚠️ | Kirkland › Île de Montréal | 1 |
| Parc Gibson ⚠️ | Kirkland › Île de Montréal | 1 |
| Parc de Beaconsfield (6) ⚠️ | Beaconsfield › Île de Montréal | 1 |
| Parc Henri-Jarry ⚠️ | Beaconsfield › Île de Montréal | 1 |
| Parc de Beaconsfield (7) ⚠️ | Beaconsfield › Île de Montréal | 1 |
| Parc Godin ⚠️ | Sainte-Anne-de-Bellevue › Île de Montréal | 1 |
| Parc Denis-Benjamin-Viger ⚠️ | Montréal › L'Île-Bizard–Sainte-Geneviève › Île de Montréal | 1 |
| Parc Aragon ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 1 |
| Parc des Bénévoles ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 1 |
| Parc Jean-Brillant ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 1 |
| Parc Raoul-Laurin ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 1 |
| Parc Marie-Claire-Daveluy ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc Gerry-Roufs ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc Pierre Dagenais-dit-Lépine ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc Zotique-Saint-Jean ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc Samuel-Morse ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc Hans-Selye ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc Francesco-Lacurto ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc Marcel-Léger ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc Richelieu (2) ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc du Cheval-Blanc ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc de Montreal (78) ⚠️ | Montréal › Montréal-Nord › Île de Montréal | 1 |
| Parc de Montreal (85) ⚠️ | Montréal › Montréal-Nord › Île de Montréal | 1 |
| Parc Primeau ⚠️ | Montréal › Montréal-Nord › Île de Montréal | 1 |
| Parc Charleroi ⚠️ | Montréal › Montréal-Nord › Île de Montréal | 1 |
| Parc Sainte-Lucie ⚠️ | Montréal › Villeray–Saint-Michel–Parc-Extension › Île de Montréal | 1 |
| Parc du Bois-Franc (3) ⚠️ | Montréal › Saint-Laurent › Île de Montréal | 1 |
| Parc Jean-J.-et-Marc-Thibodeau ⚠️ | Mont-Royal › Île de Montréal | 1 |
| Parc E.-B.-Jubien ⚠️ | Mont-Royal › Île de Montréal | 1 |
| Parc Godfroy-Langlois ⚠️ | Mont-Royal › Île de Montréal | 1 |
| Parc de la Paix (2) ⚠️ | Mont-Royal › Île de Montréal | 1 |
| Parc Kindersley ⚠️ | Mont-Royal › Île de Montréal | 1 |
| Parc Emerald ⚠️ | Mont-Royal › Île de Montréal | 1 |
| Parc Monsignor Harold-J.-Doran ⚠️ | Mont-Royal › Île de Montréal | 1 |
| Parc de Montreal (89) ⚠️ | Montréal › Côte-des-Neiges–Notre-Dame-de-Grâce › Île de Montréal | 1 |
| Miniparc Grandbois ⚠️ | Montréal › Saint-Léonard › Île de Montréal | 1 |
| Miniparc de Ségur ⚠️ | Montréal › Saint-Léonard › Île de Montréal | 1 |
| Parc de Montreal (90) ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 1 |
| Parc de la Métairie ⚠️ | Montréal › Verdun › Île de Montréal | 1 |
| Parc de l'esplanade de la Pointe-Nord ⚠️ | Montréal › Verdun › Île de Montréal | 1 |
| Place Iona-Monahan ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 1 |
| Aire de repos Île-Mercier ⚠️ | Montréal › L'Île-Bizard–Sainte-Geneviève › Île de Montréal | 1 |
| Parc Julie-Dauth ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 1 |
| Parc Riviera ⚠️ | Montréal › L'Île-Bizard–Sainte-Geneviève › Île de Montréal | 1 |
| Parc Cardinal (2) ⚠️ | Montréal › L'Île-Bizard–Sainte-Geneviève › Île de Montréal | 1 |
| Parc Shakespeare ⚠️ | Dollard-des-Ormeaux › Île de Montréal | 1 |
| Parc Langhorne ⚠️ | Hampstead › Île de Montréal | 1 |
| Parc Dorset ⚠️ | Baie-D'Urfé › Île de Montréal | 1 |
| Parc Fritz (2) ⚠️ | Baie-D'Urfé › Île de Montréal | 1 |
| Parc Saint-Marcel ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc Verdelles ⚠️ | Montréal › Anjou › Île de Montréal | 1 |
| Parc Clément-Jetté Sud ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 1 |
| Parc du Bocage ⚠️ | Montréal › Anjou › Île de Montréal | 1 |
| Parc des Vétérans ⚠️ | Côte-Saint-Luc › Île de Montréal | 1 |
| Parc de Montreal (94) ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 1 |
| Parc Belvédère Terry-Fox ⚠️ | Montréal › Côte-des-Neiges–Notre-Dame-de-Grâce › Île de Montréal | 1 |
| Parc de la Malva ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 1 |
| City Hall Park ⚠️ | Montréal › LaSalle › Île de Montréal | 1 |
| Parc Maria-Goretti ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc Sutherland-Sackville-Bain ⚠️ | Montréal › Verdun › Île de Montréal | 1 |
| Parc-école Notre Dame ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc du Ruisseau-du-Pont-à-l’Avoine ⚠️ | Montréal › Villeray–Saint-Michel–Parc-Extension › Île de Montréal | 1 |
| Parc Highridge ⚠️ | Beaconsfield › Île de Montréal | 1 |
| Parc Guglielmo-Marconi ⚠️ | Montréal › Rosemont–La Petite-Patrie › Île de Montréal | 1 |
| Parc Pierre-Dansereau ⚠️ | Montréal › Outremont › Île de Montréal | 1 |
| Parc Coolbrook ⚠️ | Dollard-des-Ormeaux › Île de Montréal | 1 |
| Parc de Montreal (110) ⚠️ | Montréal › LaSalle › Île de Montréal | 1 |
| Plage de l'Est ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Place au Soleil Mullins ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 1 |
| Parc Victor Gray ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 1 |
| Parc de Montreal (114) ⚠️ | Montréal › Anjou › Île de Montréal | 1 |
| Parc de Montreal (115) ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 1 |
| Promenade de l'Aqueduc ⚠️ | Montréal › LaSalle › Île de Montréal | 1 |
| Parc Julia-Drummond ⚠️ | Montréal › Ville-Marie › Île de Montréal | 1 |
| Parc Juliette-Huot ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 1 |
| Parc François-La Bernarde ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc Marie-Claire-Kirkland-Casgrain ⚠️ | Montréal › LaSalle › Île de Montréal | 1 |
| Parc d'Argenson (2) ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 1 |
| Parc Gadbois ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 1 |
| Parc de la Grande-Anse (2) ⚠️ | Pointe-Claire › Île de Montréal | 1 |
| Parc Bayview ⚠️ | Pointe-Claire › Île de Montréal | 1 |
| Parc Neptune ⚠️ | Dorval › Île de Montréal | 1 |
| Parc Félix-Leclerc (4) ⚠️ | Montréal › Anjou › Île de Montréal | 1 |
| Parc des Gorilles ⚠️ | Montréal › Rosemont–La Petite-Patrie › Île de Montréal | 1 |
| Parc Saint-André-Apôtre ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 1 |
| Parc Roland-Giguère ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 1 |
| Parc Basile-Routhier ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 1 |
| Parc Robillard ⚠️ | Sainte-Anne-de-Bellevue › Île de Montréal | 1 |
| Parc de Mésy ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 1 |
| Parc D'Auteuil ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 1 |
| Parc de Deauville ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 1 |
| Parc Cyril-W.-MacDonald ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 1 |
| Parc de Dollard-Des-Ormeaux (4) ⚠️ | Dollard-des-Ormeaux › Île de Montréal | 1 |
| Parc Holleuffer ⚠️ | Kirkland › Île de Montréal | 1 |
| Parc de Bordeaux ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 1 |
| Parc Nicolas-Viel ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 1 |
| Parc Dixie ⚠️ | Montréal › Lachine › Île de Montréal | 1 |
| Parc Dollier-de-Casson ⚠️ | Montréal › LaSalle › Île de Montréal | 1 |
| Musée de Lachine ⚠️ | Montréal › Lachine › Île de Montréal | 1 |
| Parc Commémoratif (2) ⚠️ | Montréal-Ouest › Île de Montréal | 1 |
| Parc Clifford ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 1 |
| Parc Grovehill (2) ⚠️ | Montréal › Côte-des-Neiges–Notre-Dame-de-Grâce › Île de Montréal | 1 |
| Parc de Montreal (135) ⚠️ | Montréal › Rosemont–La Petite-Patrie › Île de Montréal | 1 |
| Parc Coffee ⚠️ | Montréal › Côte-des-Neiges–Notre-Dame-de-Grâce › Île de Montréal | 1 |
| Parc Houde (3) ⚠️ | Montréal › Saint-Laurent › Île de Montréal | 1 |
| Parc Decelles ⚠️ | Montréal › Saint-Laurent › Île de Montréal | 1 |
| Parc Zotique-Racicot ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 1 |
| Parc De Salaberry ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 1 |
| Parc de Montreal (136) ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 1 |
| Parc Albert-Malouf ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 1 |
| Parc de Montreal (138) ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 1 |
| Parc de Montreal (139) ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 1 |
| Parc de Montreal (140) ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 1 |
| Parc du Bassin-Bonsecours ⚠️ | Montréal › Ville-Marie › Île de Montréal | 1 |
| Parc des Fondatrices-de-Saint-Léonard ⚠️ | Montréal › Saint-Léonard › Île de Montréal | 1 |
| Terrain d'athlétisme de Westmount ⚠️ | Westmount › Île de Montréal | 1 |
| Parc Suzanne-Beaudoin-Dumouchel ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 1 |
| Parc Saint-Paul-de-la-Croix ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 1 |
| Parc de Montreal (153) ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 1 |
| Parc de Dollard-Des-Ormeaux (7) ⚠️ | Dollard-des-Ormeaux › Île de Montréal | 1 |
| Parc de Montreal (154) ⚠️ | Montréal › L'Île-Bizard–Sainte-Geneviève › Île de Montréal | 1 |
| Square Cabot ⚠️ | Montréal › Ville-Marie › Île de Montréal | 1 |
| Parc Garon–Amos ⚠️ | Montréal › Montréal-Nord › Île de Montréal | 1 |
| Jardins du Petit-Laurier ⚠️ | Montréal › Le Plateau-Mont-Royal › Île de Montréal | 1 |
| Parc Percy-Walters ⚠️ | Montréal › Ville-Marie › Île de Montréal | 1 |
| Parc de Montreal (160) ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 1 |
| Baseball court (Seigniory Park) ⚠️ | Pointe-Claire › Île de Montréal | 1 |
| Carré du Nordet ⚠️ | Montréal › Saint-Laurent › Île de Montréal | 1 |
| Parc Parent ⚠️ | Montréal › LaSalle › Île de Montréal | 1 |
| Parc de Montreal (174) ⚠️ | Montréal › Mercier–Hochelaga-Maisonneuve › Île de Montréal | 1 |
| Parc Smiley ⚠️ | Kirkland › Île de Montréal | 1 |
| Parc de Montreal (175) ⚠️ | Montréal › Ville-Marie › Île de Montréal | 1 |
| Parc de la Rive-Boisée ⚠️ | Montréal › Pierrefonds-Roxboro › Île de Montréal | 1 |
| Parc Urgel-Archambault ⚠️ | Montréal › Saint-Laurent › Île de Montréal | 1 |
| Parc Edgewater ⚠️ | Pointe-Claire › Île de Montréal | 1 |
| Parc Saint-James ⚠️ | Beaconsfield › Île de Montréal | 1 |
| Parc Ernest-Rouleau ⚠️ | Montréal › Rivière-des-Prairies–Pointe-aux-Trembles › Île de Montréal | 1 |
| Parc Highlands ⚠️ | Montréal › LaSalle › Île de Montréal | 1 |
| Parc des Saints-Anges ⚠️ | Montréal › LaSalle › Île de Montréal | 1 |
| Esplanade Jean-Doré ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 1 |
| Parc Woodland ⚠️ | Montréal › Verdun › Île de Montréal | 1 |
| Parc Jean-Brillant (2) ⚠️ | Montréal › Côte-des-Neiges–Notre-Dame-de-Grâce › Île de Montréal | 1 |
| Parc des Amériques ⚠️ | Montréal › Le Plateau-Mont-Royal › Île de Montréal | 1 |
| Parc Mahatma Gandhi ⚠️ | Montréal › Côte-des-Neiges–Notre-Dame-de-Grâce › Île de Montréal | 1 |
| Parc Pratt ⚠️ | Montréal › Outremont › Île de Montréal | 1 |
| Parc de Westmount (7) ⚠️ | Westmount › Île de Montréal | 1 |
| Parc de Montreal (179) ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 1 |
| Ovila-Légaré ⚠️ | Montréal › Villeray–Saint-Michel–Parc-Extension › Île de Montréal | 1 |
| Parc Sault-au-Recollet ⚠️ | Montréal › Ahuntsic-Cartierville › Île de Montréal | 1 |
| Parc Kirkland (2) ⚠️ | Montréal › Lachine › Île de Montréal | 1 |
| Parc Guillaume-Bruneau ⚠️ | Montréal › Saint-Laurent › Île de Montréal | 1 |
| Parc Raymond-Lagacé ⚠️ | Montréal › Saint-Laurent › Île de Montréal | 1 |
| Parc Vinet ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 1 |
| Parc Sammy-Hill ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 1 |
| Woonerf Saint-Pierre ⚠️ | Montréal › Le Sud-Ouest › Île de Montréal | 1 |

944 parc(s) plus petits qu'une cellule ne sont pas listés : la carte les dessine, mais ils n'offrent aucune cellule.

⚠️ 1520 parc(s) hors de la fenêtre 10–125 cellules (1514 trop petit(s), 6 trop grand(s)) : affichés sur la carte, mais ils ne peuvent pas servir de cible à un défi.

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
| Montréal | 243 |
| Saint-Laurent | 194 |
| Mercier–Hochelaga-Maisonneuve | 47 |
| Rivière-des-Prairies–Pointe-aux-Trembles | 6 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
