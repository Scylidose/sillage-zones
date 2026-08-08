# Montréal (île)

Pack `qc-montreal-ile` · version 1.1.0 · grille 200 m · Canada › Québec › Grand Montréal

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

## Îles

| Île | Cellules | Composition |
|---|---:|---|
| Île de Montréal | 25 367 | somme de 15 villes |
| Parc Jean-Drapeau | 110 | polygone propre |

Une île *composite* n'a pas de cellules à elle : sa progression est la somme de ses villes, et ses cellules ne lui sont jamais rattachées directement — elles compteraient deux fois.

## Villes (16)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Parcs |
|---|---:|---:|---:|---:|---:|---:|
| Montreal | 22 453 | 3 872 | 18 581 | 243 | **18 338** | 472 |
| Dorval | 1 453 | 385 | 1 068 | 368 | **700** | 12 |
| Pointe-Claire | 1 790 | 829 | 961 | 0 | **961** | 25 |
| Dollard-Des-Ormeaux | 764 | 7 | 757 | 0 | **757** | 20 |
| Montréal-Est | 712 | 78 | 634 | 0 | **634** | 2 |
| Beaconsfield | 1 095 | 535 | 560 | 0 | **560** | 16 |
| Sainte-Anne-de-Bellevue | 563 | 29 | 534 | 0 | **534** | 6 |
| Kirkland | 492 | 1 | 491 | 0 | **491** | 11 |
| Mont-Royal | 390 | 0 | 390 | 0 | **390** | 14 |
| Senneville | 928 | 558 | 370 | 0 | **370** | 1 |
| Côte-Saint-Luc | 352 | 0 | 352 | 0 | **352** | 10 |
| Baie-D'Urfé | 383 | 79 | 304 | 0 | **304** | 7 |
| Westmount | 202 | 0 | 202 | 0 | **202** | 7 |
| Hampstead | 92 | 0 | 92 | 0 | **92** | 4 |
| Montréal-Ouest | 71 | 0 | 71 | 0 | **71** | 1 |
| L'Île-Dorval | 8 | 0 | 8 | 0 | **8** |  |

## Arrondissements et quartiers (19)

| Zone | Ville | Brut | Eau | Sans eau | Restr. | Comptées | Parcs |
|---|---|---:|---:|---:|---:|---:|---:|
| Saint-Laurent | montreal | 2 190 | 4 | 2 186 | 194 | **1 992** | 32 |
| Pointe-aux-Trembles-Rivieres-des-Prairies | montreal | 2 520 | 339 | 2 181 | 6 | **2 175** | 58 |
| Pierrefonds--Roxboro | montreal | 1 668 | 287 | 1 381 | 0 | **1 381** | 34 |
| Mercier-Hochelaga-Maisonneuve | montreal | 1 396 | 98 | 1 298 | 47 | **1 251** | 46 |
| Ahuntsic-Cartierville | montreal | 1 239 | 1 | 1 238 | 0 | **1 238** | 43 |
| L'Ile-Bizard--Sainte-Genevieve | montreal | 1 812 | 618 | 1 194 | 0 | **1 194** | 13 |
| Cote-des-Neiges--Notre-Dame-de-Grace | montreal | 1 084 | 0 | 1 084 | 0 | **1 084** | 23 |
| Lachine | montreal | 1 125 | 218 | 907 | 0 | **907** | 12 |
| Villeray-Saint-Michel-Parc-Extension | montreal | 839 | 8 | 831 | 0 | **831** | 14 |
| LaSalle | montreal | 1 250 | 423 | 827 | 0 | **827** | 25 |
| Rosemont--La-Petite-Patrie | montreal | 810 | 0 | 810 | 0 | **810** | 29 |
| Ville-Marie | montreal | 1 094 | 294 | 800 | 0 | **800** | 31 |
| Sud-Ouest | montreal | 915 | 117 | 798 | 0 | **798** | 33 |
| Anjou | montreal | 705 | 3 | 702 | 0 | **702** | 11 |
| St-Leonard | montreal | 691 | 0 | 691 | 0 | **691** | 15 |
| Montreal-Nord | montreal | 638 | 75 | 563 | 0 | **563** | 14 |
| Verdun--Ile-des-Soeurs | montreal | 1 071 | 589 | 482 | 0 | **482** | 19 |
| Plateau-Mont-Royal | montreal | 416 | 3 | 413 | 0 | **413** | 13 |
| Outremont | montreal | 198 | 1 | 197 | 0 | **197** | 7 |

## Îles à polygone propre

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Parcs |
|---|---:|---:|---:|---:|---:|---:|
| Parc Jean-Drapeau | 135 | 25 | 110 | 0 | **110** | 2 |

## Parcs (1552)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Grand Parc de l'Ouest ⚠️ | Montreal › Pierrefonds--Roxboro | 462 |
| Refuge d'oiseaux migrateurs de Senneville ⚠️ | Sainte-Anne-de-Bellevue | 279 |
| Grand Parc de l'Ouest (2) ⚠️ | Montreal › Pierrefonds--Roxboro | 187 |
| Parc-nature du Bois-de-l'Île-Bizard ⚠️ | Montreal › L'Ile-Bizard--Sainte-Genevieve | 156 |
| Arboretum Morgan ⚠️ | Sainte-Anne-de-Bellevue | 134 |
| Parc-nature de la Pointe-aux-Prairies ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 132 |
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
| Parc de la Coulée-Grou (2) | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 19 |
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
| Parc de Montreal (54) ⚠️ | Montreal › Ville-Marie | 9 |
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
| Parc du Bois-Franc (2) ⚠️ | Montreal › Saint-Laurent | 6 |
| Parc Pierre Elliott Trudeau ⚠️ | Côte-Saint-Luc | 6 |
| Parc Adrien-D.-Archambault ⚠️ | Montreal › Verdun--Ile-des-Soeurs | 6 |
| Parc des Bénévoles (2) ⚠️ | Kirkland | 6 |
| Parc Monseigneur J.-A.-Richard ⚠️ | Montreal › Verdun--Ile-des-Soeurs | 5 |
| Parc Grier ⚠️ | Montreal › Pierrefonds--Roxboro | 5 |
| Parc Clémentine-De la Rousselière ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 5 |
| Parc Armand-Bombardier ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 5 |
| Parc Maynard-Ferguson ⚠️ | Montreal › Verdun--Ile-des-Soeurs | 5 |
| Parc Martin-Luther-King ⚠️ | Montreal › Cote-des-Neiges--Notre-Dame-de-Grace | 5 |
| Parc de Montreal (143) ⚠️ | Montreal › LaSalle | 5 |
| Parc Duval ⚠️ | Montreal › Pierrefonds--Roxboro | 5 |
| Parc Cedar Park Heights ⚠️ | Pointe-Claire | 4 |
| Parc André-Lavallée ⚠️ | Montreal › Rosemont--La-Petite-Patrie | 4 |
| Parc de la Louisiane ⚠️ | Montreal › Rosemont--La-Petite-Patrie | 4 |
| Parc Sainte-Bernadette ⚠️ | Montreal › Rosemont--La-Petite-Patrie | 4 |
| Parc Étienne-Desmarteau ⚠️ | Montreal › Rosemont--La-Petite-Patrie | 4 |
| King George Park ⚠️ | Westmount | 4 |
| Parc Saint-Laurent ⚠️ | Montreal › Saint-Laurent | 4 |
| Parc Le Ber ⚠️ | Montreal › Sud-Ouest | 4 |
| Parc Daniel-Johnson (2) ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 4 |
| Parc de Montreal (15) ⚠️ | Montreal › Ville-Marie › Parc Jean-Drapeau | 4 |
| Parc Louis-Riel ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 4 |
| Parc Riverside ⚠️ | Montreal › LaSalle | 4 |
| Parc Lake Road ⚠️ | Dollard-Des-Ormeaux | 4 |
| Parc Edward Janiszewski ⚠️ | Dollard-Des-Ormeaux | 4 |
| Parc des Cageux ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 4 |
| Parc de Montreal (53) ⚠️ | Montreal › Ville-Marie | 4 |
| Parc Giuseppe-Garibaldi ⚠️ | Montreal › St-Leonard | 4 |
| Parc Lucie-Bruneau ⚠️ | Montreal › Anjou | 4 |
| Parc Villeray ⚠️ | Montreal › Villeray-Saint-Michel-Parc-Extension | 4 |
| Parc Don-Bosco ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 4 |
| Parc George-Springate ⚠️ | Montreal › Pierrefonds--Roxboro | 4 |
| Parc de l'école secondaire de la Pointe-aux-Trembles ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 4 |
| Parc de Beaconsfield (9) ⚠️ | Beaconsfield | 4 |
| Parc Ladauversière ⚠️ | Montreal › St-Leonard | 4 |
| Parc Westmount ⚠️ | Westmount | 4 |
| Parc Hampstead ⚠️ | Hampstead | 4 |
| Parc Pie-XII ⚠️ | Montreal › St-Leonard | 4 |
| Parc Hébert (2) ⚠️ | Montreal › St-Leonard | 4 |
| Parc Sunnyside ⚠️ | Pointe-Claire | 3 |
| Parc du Pélican ⚠️ | Montreal › Rosemont--La-Petite-Patrie | 3 |
| Parc Danyluk ⚠️ | Mont-Royal | 3 |
| Parc City Lane ⚠️ | Beaconsfield | 3 |
| Parc Surrey ⚠️ | Dorval | 3 |
| Parc Saint-Charles ⚠️ | Dorval | 3 |
| Parc du Boisé-de-Saint-Sulpice ⚠️ | Montreal › Ahuntsic-Cartierville | 3 |
| Parc Marguerite-Bourgeoys ⚠️ | Montreal › Sud-Ouest | 3 |
| Parc Sauvé ⚠️ | Montreal › Montreal-Nord | 3 |
| Parc Coubertin ⚠️ | Montreal › St-Leonard | 3 |
| Parc Westminster ⚠️ | Dollard-Des-Ormeaux | 3 |
| Parc Frederick T. Wilson ⚠️ | Dollard-Des-Ormeaux | 3 |
| Parc de Beauséjour ⚠️ | Montreal › Ahuntsic-Cartierville | 3 |
| Lieu historique national du Canal-de-Lachine ⚠️ | Montreal › Lachine | 3 |
| Parc Pierre-Bédard ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 3 |
| Parc de Louisbourg ⚠️ | Montreal › Ahuntsic-Cartierville | 3 |
| Parc Valois ⚠️ | Pointe-Claire | 3 |
| Parc Raymond (2) ⚠️ | Montreal › LaSalle | 3 |
| Parc Benny ⚠️ | Montreal › Cote-des-Neiges--Notre-Dame-de-Grace | 3 |
| Parc Brook ⚠️ | Montreal › Pierrefonds--Roxboro | 3 |
| Parc Carlos d'Alcantara ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 3 |
| Parc du Boisé Jean-Milot ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 3 |
| Parc Roger-Rousseau ⚠️ | Montreal › Anjou | 3 |
| Parc de Montreal (60) ⚠️ | Montreal › Ville-Marie | 3 |
| Parc Sainte-Marthe ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 3 |
| Parc Campbell Ouest ⚠️ | Montreal › Sud-Ouest | 3 |
| Parc de Stewart Hall ⚠️ | Pointe-Claire | 3 |
| Parc Bertold ⚠️ | Baie-D'Urfé | 3 |
| Parc Yuile ⚠️ | Montreal › Pierrefonds--Roxboro | 3 |
| Parc de Montreal (82) ⚠️ | Montreal › Montreal-Nord | 3 |
| Parc Cité-Jardin ⚠️ | Montreal › Rosemont--La-Petite-Patrie | 3 |
| Parc des Arbres ⚠️ | Montreal › Pierrefonds--Roxboro | 3 |
| Parc Ferland ⚠️ | Montreal › St-Leonard | 3 |
| Parc J.-Albert-Gariépy ⚠️ | Montreal › Verdun--Ile-des-Soeurs | 3 |
| Parc Mackenzie-King ⚠️ | Montreal › Cote-des-Neiges--Notre-Dame-de-Grace | 3 |
| Parc Maurice-Richard (2) ⚠️ | Montreal › Ahuntsic-Cartierville | 3 |
| Parc Westwood (2) ⚠️ | Dollard-Des-Ormeaux | 3 |
| Parc Spring Garden ⚠️ | Dollard-Des-Ormeaux | 3 |
| Parc Sainte-Odile ⚠️ | Montreal › Ahuntsic-Cartierville | 3 |
| parc des Bateliers ⚠️ | Montreal › Ahuntsic-Cartierville | 3 |
| Parc de la Merci ⚠️ | Montreal › Ahuntsic-Cartierville | 3 |
| Parc Lefebvre (2) ⚠️ | Montreal › LaSalle | 3 |
| Parc Trenholme ⚠️ | Montreal › Cote-des-Neiges--Notre-Dame-de-Grace | 3 |
| Parc Loyola ⚠️ | Montreal › Cote-des-Neiges--Notre-Dame-de-Grace | 3 |
| Parc Stoney Point ⚠️ | Montreal › Lachine | 3 |
| Parc Ermanno-La Riccia ⚠️ | Montreal › St-Leonard | 3 |
| Bassin de la Brunante ⚠️ | Montreal › Saint-Laurent | 3 |
| Parc Gouin (4) ⚠️ | Montreal › Ahuntsic-Cartierville | 3 |
| Parc de Montreal (163) ⚠️ | Montreal › Rosemont--La-Petite-Patrie | 3 |
| Parc Honoré-Mercier (2) ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 3 |
| Parc de West Vancouver ⚠️ | Montreal › Verdun--Ile-des-Soeurs | 3 |
| Parc Dollard-des-Ormeaux ⚠️ | Dollard-Des-Ormeaux | 3 |
| Parc Lacharité ⚠️ | Montreal › LaSalle | 3 |
| Parc Alexandre-Bourgeau ⚠️ | Pointe-Claire | 2 |
| Parc Hermitage ⚠️ | Pointe-Claire | 2 |
| Parc Northview ⚠️ | Pointe-Claire | 2 |
| Parc Arthur-E.-Séguin ⚠️ | Pointe-Claire | 2 |
| Parc Centennial ⚠️ | Beaconsfield | 2 |
| Parc Windsor ⚠️ | Dorval | 2 |
| Parc du Millénaire ⚠️ | Dorval | 2 |
| Parc Jean-Martucci ⚠️ | Montreal › Ahuntsic-Cartierville | 2 |
| Parc Jean-Amyot ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 2 |
| Parc Saint-Donat ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 2 |
| Parc de l'Ancienne-Pépinière ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 2 |
| Parc Beaubien (2) ⚠️ | Montreal › Rosemont--La-Petite-Patrie | 2 |
| Parc de l'Hôtel-de-Ville ⚠️ | Montréal-Est | 2 |
| Parc Saint-Simon-Apôtre ⚠️ | Montreal › Ahuntsic-Cartierville | 2 |
| Parc François-Perrault ⚠️ | Montreal › Villeray-Saint-Michel-Parc-Extension | 2 |
| Parc Pierre-Bernard ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 2 |
| Parc Terry Fox ⚠️ | Dollard-Des-Ormeaux | 2 |
| Parc Champêtre ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 2 |
| Parc Jean-Duceppe ⚠️ | Montreal › Rosemont--La-Petite-Patrie | 2 |
| Parc Aimé-Caron ⚠️ | Montreal › Saint-Laurent | 2 |
| Parc Cousineau ⚠️ | Montreal › Saint-Laurent | 2 |
| Parc Noël-Sud ⚠️ | Montreal › Saint-Laurent | 2 |
| Parc Noël-Nord ⚠️ | Montreal › Saint-Laurent | 2 |
| Parc de la Reine-Élisabeth ⚠️ | Montreal › Verdun--Ile-des-Soeurs | 2 |
| Parc Alexis-Nihon ⚠️ | Montreal › Saint-Laurent | 2 |
| Parc Pilon ⚠️ | Montreal › Montreal-Nord | 2 |
| Parc Gabriel-Lalemant ⚠️ | Montreal › Ahuntsic-Cartierville | 2 |
| Parc Aimé-Léonard ⚠️ | Montreal › Montreal-Nord | 2 |
| Parc Henri-Bourassa ⚠️ | Montreal › Montreal-Nord | 2 |
| Parc Pierre-Tétrault ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 2 |
| Parc Champdoré ⚠️ | Montreal › Villeray-Saint-Michel-Parc-Extension | 2 |
| Parc Joyce ⚠️ | Montreal › Outremont | 2 |
| Parc du Boisé-Roxboro ⚠️ | Montreal › Pierrefonds--Roxboro | 2 |
| Parc Lalancette ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 2 |
| Parc Elm ⚠️ | Dollard-Des-Ormeaux | 2 |
| Parc Dan-Hanganu ⚠️ | Montreal › Verdun--Ile-des-Soeurs | 2 |
| Parc Baldwin ⚠️ | Montreal › Plateau-Mont-Royal | 2 |
| Parc Baldwin (2) ⚠️ | Montreal › Plateau-Mont-Royal | 2 |
| Parc Van Horne ⚠️ | Montreal › Cote-des-Neiges--Notre-Dame-de-Grace | 2 |
| Parc Joseph-Paré (2) ⚠️ | Montreal › Rosemont--La-Petite-Patrie | 2 |
| Parc Edward J. Kirwan ⚠️ | Côte-Saint-Luc | 2 |
| Parc Cavelier-De LaSalle ⚠️ | Montreal › LaSalle | 2 |
| Parc-école Laurier-Macdonald ⚠️ | Montreal › St-Leonard | 2 |
| Parc Leroux ⚠️ | Montreal › LaSalle | 2 |
| Parc Graham ⚠️ | Montreal › Pierrefonds--Roxboro | 2 |
| Parc Fairview ⚠️ | Dollard-Des-Ormeaux | 2 |
| Parc de la Savane ⚠️ | Montreal › Cote-des-Neiges--Notre-Dame-de-Grace | 2 |
| Parc Nelson-Mandela ⚠️ | Montreal › Cote-des-Neiges--Notre-Dame-de-Grace | 2 |
| Parc Dollard-Morin ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 2 |
| Parc de Montreal (33) ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 2 |
| Parc du Château-Pierrefonds ⚠️ | Montreal › Pierrefonds--Roxboro | 2 |
| Parc de Montreal (37) ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 2 |
| Parc Saint-Joseph (2) ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 2 |
| Parc André-Laurendeau ⚠️ | Montreal › Anjou | 2 |
| Parc Goncourt ⚠️ | Montreal › Anjou | 2 |
| Parc Carignan (2) ⚠️ | Montreal › Lachine | 2 |
| Parc Herb-Trawick ⚠️ | Montreal › Sud-Ouest | 2 |
| Parc de Montreal (66) ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 2 |
| Parc Francine-Léger ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 2 |
| Parc Liébert ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 2 |
| Parc Chénier-Beaugrand ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 2 |
| Parc Francesca-Cabrini ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 2 |
| Parc Luigi-Pirandello ⚠️ | Montreal › St-Leonard | 2 |
| Parc René-Goupil ⚠️ | Montreal › Villeray-Saint-Michel-Parc-Extension | 2 |
| Parc de Montreal (71) ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 2 |
| Parc Summerlea ⚠️ | Montreal › Lachine | 2 |
| Parc Sunnybrooke ⚠️ | Dollard-Des-Ormeaux | 2 |
| Parc Héritage-sur-le-Lac ⚠️ | Montreal › Pierrefonds--Roxboro | 2 |
| Port de Plaisance de Pierrefonds ⚠️ | Montreal › Pierrefonds--Roxboro | 2 |
| Parc Moulin-du-Rapide ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 2 |
| Parc Marie-Cardinal ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 2 |
| Parc Atholstan ⚠️ | Mont-Royal | 2 |
| Parc Léon-Brisebois ⚠️ | Montreal › L'Ile-Bizard--Sainte-Genevieve | 2 |
| Parc Allan's Hill ⚠️ | Baie-D'Urfé | 2 |
| Parc Clément-Jetté Nord ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 2 |
| Parc des Roseraies ⚠️ | Montreal › Anjou | 2 |
| Parc de Montreal (97) ⚠️ | Montreal › Saint-Laurent | 2 |
| Parc Saint-Benoît ⚠️ | Montreal › Ahuntsic-Cartierville | 2 |
| Parc d'A-Ma-Baie ⚠️ | Montreal › Pierrefonds--Roxboro | 2 |
| Parc Rhian-Wilkinson ⚠️ | Baie-D'Urfé | 2 |
| Parc Pine Beach ⚠️ | Dorval | 2 |
| Parc Simone-Dénéchaud ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 2 |
| Place des Montréalaises ⚠️ | Montreal › Ville-Marie | 2 |
| Parc de Dollard-Des-Ormeaux (5) ⚠️ | Dollard-Des-Ormeaux | 2 |
| Parc de Dollard-Des-Ormeaux (6) ⚠️ | Dollard-Des-Ormeaux | 2 |
| Parc Meades ⚠️ | Kirkland | 2 |
| Parc Grovehill ⚠️ | Montreal › Lachine | 2 |
| Hayward Park ⚠️ | Montreal › LaSalle | 2 |
| Parc de Montreal (132) ⚠️ | Montreal › LaSalle | 2 |
| Parc Ranger ⚠️ | Montreal › LaSalle | 2 |
| Parc de la Vérendrye ⚠️ | Montreal › Sud-Ouest | 2 |
| Parc Félix-Leclerc (6) ⚠️ | Montreal › LaSalle | 2 |
| Parc Notre-Dame-de-Grâce ⚠️ | Montreal › Cote-des-Neiges--Notre-Dame-de-Grace | 2 |
| Parc Georges-Saint-Pierre ⚠️ | Montreal › Cote-des-Neiges--Notre-Dame-de-Grace | 2 |
| Parc Pehr-Kalm ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 2 |
| Parc Saint-Alphonse (2) ⚠️ | Montreal › Ahuntsic-Cartierville | 2 |
| Parc de Montreal (158) ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 2 |
| Parc Dalbé-Viau ⚠️ | Montreal › Lachine | 2 |
| Parc Windermere ⚠️ | Beaconsfield | 2 |
| Parc de la Rivière-Disparue ⚠️ | Montreal › Sud-Ouest | 2 |
| Parc des Vannes de l'Aqueduc ⚠️ | Montreal › LaSalle | 2 |
| Parc Morgan (2) ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 2 |
| Parc Hartenstein ⚠️ | Montreal › Saint-Laurent | 2 |
| Parc de la Confédération ⚠️ | Montreal › Cote-des-Neiges--Notre-Dame-de-Grace | 2 |
| Parc Jean-Jacques Rouseau ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 2 |
| Parc George-Vernot ⚠️ | Montreal › Villeray-Saint-Michel-Parc-Extension | 2 |
| Parc linéaire du Premier-Chemin-de-Fer ⚠️ | Montreal › Sud-Ouest | 2 |
| Parc Wilfrid-Bastien ⚠️ | Montreal › St-Leonard | 2 |
| Parc Clearpoint ⚠️ | Pointe-Claire | 1 |
| Parc Saint-Viateur ⚠️ | Montreal › Outremont | 1 |
| Parc Beaubien ⚠️ | Montreal › Outremont | 1 |
| Parc Seigniory ⚠️ | Pointe-Claire | 1 |
| Newton Square ⚠️ | Pointe-Claire | 1 |
| Parc Maple ⚠️ | Pointe-Claire | 1 |
| Parc Jack-Robinson ⚠️ | Pointe-Claire | 1 |
| Parc Marsh & Stockwell ⚠️ | Pointe-Claire | 1 |
| Parc D.W. Beck ⚠️ | Pointe-Claire | 1 |
| Parc de Pointe-Claire (6) ⚠️ | Pointe-Claire | 1 |
| Lower Field ⚠️ | Montreal › Ville-Marie | 1 |
| Parc J.-Arthur-Champagne ⚠️ | Montreal › Rosemont--La-Petite-Patrie | 1 |
| Parc Joseph-N.-Drapeau ⚠️ | Montreal › Rosemont--La-Petite-Patrie | 1 |
| Parc Saint-Émile ⚠️ | Montreal › Rosemont--La-Petite-Patrie | 1 |
| Parc de Normanville ⚠️ | Montreal › Villeray-Saint-Michel-Parc-Extension | 1 |
| Parc Le Prévost ⚠️ | Montreal › Villeray-Saint-Michel-Parc-Extension | 1 |
| Parc Mohawk ⚠️ | Mont-Royal | 1 |
| Parc de Beaconsfield ⚠️ | Beaconsfield | 1 |
| Brookside Park ⚠️ | Beaconsfield | 1 |
| Parc de Beaconsfield (2) ⚠️ | Beaconsfield | 1 |
| Parc Shannon ⚠️ | Beaconsfield | 1 |
| Parc Royal ⚠️ | Beaconsfield | 1 |
| Parc Beaconsfield Heights ⚠️ | Beaconsfield | 1 |
| Parc Beacon Hill ⚠️ | Beaconsfield | 1 |
| Parc Paiement ⚠️ | Kirkland | 1 |
| Parc Kirkland ⚠️ | Kirkland | 1 |
| Place De La Dauversière ⚠️ | Montreal › Ville-Marie | 1 |
| Parc Héritage ⚠️ | Kirkland | 1 |
| Parc Houde ⚠️ | Kirkland | 1 |
| Square Dorchester ⚠️ | Montreal › Ville-Marie | 1 |
| Parc Ecclestone ⚠️ | Kirkland | 1 |
| Parc Rutherford ⚠️ | Montreal › Ville-Marie | 1 |
| Parc Aumais ⚠️ | Sainte-Anne-de-Bellevue | 1 |
| Parc William-Bowie ⚠️ | Montreal › Cote-des-Neiges--Notre-Dame-de-Grace | 1 |
| Parc du Voyageur ⚠️ | Pointe-Claire | 1 |
| Parc Westwood ⚠️ | Dorval | 1 |
| Parc Courtland ⚠️ | Dorval | 1 |
| Parc Dorval ⚠️ | Dorval | 1 |
| Parc Ballantyne ⚠️ | Dorval | 1 |
| Parc Tolhurst ⚠️ | Montreal › Ahuntsic-Cartierville | 1 |
| Parc De Lotbinière ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 1 |
| Parc Willibrord ⚠️ | Montreal › Verdun--Ile-des-Soeurs | 1 |
| Parc Beurling ⚠️ | Montreal › Verdun--Ile-des-Soeurs | 1 |
| Parc de l'Ukraine ⚠️ | Montreal › Rosemont--La-Petite-Patrie | 1 |
| Parc Jeanotte ⚠️ | Montreal › LaSalle | 1 |
| Parc Saint-Jean-Baptiste ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc de Montréal-Est ⚠️ | Montréal-Est | 1 |
| Parc Émilie-Gamelin ⚠️ | Montreal › Ville-Marie | 1 |
| Parc Alphonse-Télesphore-Lépine ⚠️ | Montreal › Plateau-Mont-Royal | 1 |
| Parc Garneau ⚠️ | Montreal › Sud-Ouest | 1 |
| Parc Oscar-Peterson ⚠️ | Montreal › Sud-Ouest | 1 |
| Parc Saint-Victor ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 1 |
| Parc Connaught ⚠️ | Mont-Royal | 1 |
| Parc Jos-Montferrand ⚠️ | Montreal › Ville-Marie | 1 |
| Parc du Mail ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 1 |
| Parc Sir-George-Étienne-Cartier ⚠️ | Montreal › Sud-Ouest | 1 |
| Parc Hamilton ⚠️ | Mont-Royal | 1 |
| Parc Maynard-Metcalf ⚠️ | Mont-Royal | 1 |
| Parc Berthe-Louard ⚠️ | Montreal › Ahuntsic-Cartierville | 1 |
| Parc de Westmount ⚠️ | Westmount | 1 |
| Parc Gohier ⚠️ | Montreal › Saint-Laurent | 1 |
| Parc Beaulac ⚠️ | Montreal › Saint-Laurent | 1 |
| Parc Dr-Bernard-Paquet ⚠️ | Montreal › Saint-Laurent | 1 |
| Parc Isaac-Abrabanel ⚠️ | Montreal › Saint-Laurent | 1 |
| Parc Marlborough ⚠️ | Montreal › Saint-Laurent | 1 |
| Parc Poirier ⚠️ | Montreal › Saint-Laurent | 1 |
| Parc de Montreal (6) ⚠️ | Montreal › Saint-Laurent | 1 |
| Parc Gold ⚠️ | Montreal › Saint-Laurent | 1 |
| Parc Chamberland ⚠️ | Montreal › Saint-Laurent | 1 |
| Parc Dakin ⚠️ | Mont-Royal | 1 |
| Parc Ottawa ⚠️ | Montreal › Montreal-Nord | 1 |
| Parc Prieur ⚠️ | Montreal › Ahuntsic-Cartierville | 1 |
| Parc J. J. Gagnier ⚠️ | Montreal › Ahuntsic-Cartierville | 1 |
| Parc Lacordaire ⚠️ | Montreal › Montreal-Nord | 1 |
| Parc Saint-Laurent (3) ⚠️ | Montreal › Montreal-Nord | 1 |
| Parc Le Carignan ⚠️ | Montreal › Montreal-Nord | 1 |
| Parc Molson ⚠️ | Montreal › Rosemont--La-Petite-Patrie | 1 |
| Parc Applewood ⚠️ | Hampstead | 1 |
| Parc Aldred ⚠️ | Hampstead | 1 |
| Parc L.-O.-Taillon ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 1 |
| Place Henri-Dunant ⚠️ | Montreal › Ville-Marie | 1 |
| Parc Beauclerk ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 1 |
| Parc Théodore ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 1 |
| Parc François-Vaillancourt ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc de Montreal (11) ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc Saint-Georges ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc Joseph-Avila-Proulx ⚠️ | Montreal › L'Ile-Bizard--Sainte-Genevieve | 1 |
| Place de la Paix ⚠️ | Montreal › Ville-Marie | 1 |
| Parc de la Coulée-Grou ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc Ouellette ⚠️ | Montreal › LaSalle | 1 |
| Parc Hochelaga ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 1 |
| Parc Wolfred-Nelson ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 1 |
| Parc Ovila-Pelletier ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 1 |
| Parc Édouard-Raymond-Fabre ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 1 |
| Square Dézéry ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 1 |
| Place de la Grande-Paix-de-Montréal ⚠️ | Montreal › Ville-Marie | 1 |
| Parc Coolbrooke ⚠️ | Dollard-Des-Ormeaux | 1 |
| Parc Saint-Aloysius ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 1 |
| Parc Dunkerque ⚠️ | Montreal › Cote-des-Neiges--Notre-Dame-de-Grace | 1 |
| Parc Desmarest ⚠️ | Montreal › L'Ile-Bizard--Sainte-Genevieve | 1 |
| Parc Jonathan-Wilson ⚠️ | Montreal › L'Ile-Bizard--Sainte-Genevieve | 1 |
| Parc Nesbitt ⚠️ | Montreal › Rosemont--La-Petite-Patrie | 1 |
| Parc Alouette ⚠️ | Dollard-Des-Ormeaux | 1 |
| Parc Ambassador ⚠️ | Pointe-Claire | 1 |
| Parc de la Fontaine ⚠️ | Montreal › Verdun--Ile-des-Soeurs | 1 |
| Parc du Pied-du-Courant ⚠️ | Montreal › Ville-Marie | 1 |
| Parc des Éclusiers ⚠️ | Montreal › Sud-Ouest | 1 |
| Parc Saint-Pierre-Claver ⚠️ | Montreal › Plateau-Mont-Royal | 1 |
| Parc des Compagnons-de-Saint-Laurent ⚠️ | Montreal › Plateau-Mont-Royal | 1 |
| Parc Olivier-Robert ⚠️ | Montreal › Ville-Marie | 1 |
| Parc Saint-Louis ⚠️ | Montreal › Lachine | 1 |
| Parc MacDonald ⚠️ | Montreal › Cote-des-Neiges--Notre-Dame-de-Grace | 1 |
| Parc Desmarchais ⚠️ | Montreal › Verdun--Ile-des-Soeurs | 1 |
| Parc Saint-Gabriel ⚠️ | Montreal › Sud-Ouest | 1 |
| Parc Raimbault ⚠️ | Montreal › Ahuntsic-Cartierville | 1 |
| Parc des Locomotives ⚠️ | Montreal › Rosemont--La-Petite-Patrie | 1 |
| Parc des Carrières ⚠️ | Montreal › Rosemont--La-Petite-Patrie | 1 |
| Parc Nicolas-Tillemont ⚠️ | Montreal › Villeray-Saint-Michel-Parc-Extension | 1 |
| Parc Julie-Hamelin ⚠️ | Montreal › Villeray-Saint-Michel-Parc-Extension | 1 |
| Parc Yitzchak Rabin ⚠️ | Côte-Saint-Luc | 1 |
| Champ des Possibles ⚠️ | Montreal › Plateau-Mont-Royal | 1 |
| Parc De Lorimier ⚠️ | Montreal › Plateau-Mont-Royal | 1 |
| Carré d'Hibernia ⚠️ | Montreal › Sud-Ouest | 1 |
| Parc Médéric-Martin (2) ⚠️ | Montreal › Ville-Marie | 1 |
| Parc Raymond-Préfontaine ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 1 |
| Carré Viger ⚠️ | Montreal › Ville-Marie | 1 |
| Parc Prudence-Heward ⚠️ | Montreal › Ville-Marie | 1 |
| Parc des Royaux ⚠️ | Montreal › Ville-Marie | 1 |
| Parc Jacques-Viger ⚠️ | Montreal › Sud-Ouest | 1 |
| Parc des Faubourgs ⚠️ | Montreal › Ville-Marie | 1 |
| Parc du Bois-des-Trottier ⚠️ | Montreal › Pierrefonds--Roxboro | 1 |
| Parc Anderson ⚠️ | Montreal › Pierrefonds--Roxboro | 1 |
| Parc de Montreal (30) ⚠️ | Montreal › Ville-Marie | 1 |
| Parc George-Legault ⚠️ | Montreal › L'Ile-Bizard--Sainte-Genevieve | 1 |
| Parc Alexander ⚠️ | Montreal › Pierrefonds--Roxboro | 1 |
| Parc Irma-Le Vasseur ⚠️ | Montreal › Outremont | 1 |
| Parc Robert-Sauvé ⚠️ | Montreal › Pierrefonds--Roxboro | 1 |
| Parc Villeret ⚠️ | Montreal › Pierrefonds--Roxboro | 1 |
| Parc Saint-Clément ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 1 |
| Parc Gilbert-Layton ⚠️ | Montreal › Cote-des-Neiges--Notre-Dame-de-Grace | 1 |
| Parc Somerled ⚠️ | Montreal › Cote-des-Neiges--Notre-Dame-de-Grace | 1 |
| Parc Joseph-Thibaudeau ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 1 |
| Parc Conrad-Poirier ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc Cécile-Bérubé ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc Pierre-Blanchet ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc du Molise ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc Outremont ⚠️ | Montreal › Outremont | 1 |
| Parc Léon-Provancher ⚠️ | Montreal › Rosemont--La-Petite-Patrie | 1 |
| Parc Idola-Saint-Jean ⚠️ | Montreal › Rosemont--La-Petite-Patrie | 1 |
| Parc Jean-Louis-Beaudry ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 1 |
| Parc Joseph-Octave-Villeneuve ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 1 |
| Parc des Botanistes ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc Joe-Beef ⚠️ | Montreal › Sud-Ouest | 1 |
| Parc Montcalm (4) ⚠️ | Montreal › Rosemont--La-Petite-Patrie | 1 |
| Parc Persillier-Lachapelle ⚠️ | Montreal › Ville-Marie | 1 |
| Parc Yves-Thériault ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc Saint-Charles (3) ⚠️ | Montreal › Pierrefonds--Roxboro | 1 |
| Parc Empress ⚠️ | Pointe-Claire | 1 |
| Parc de Montreal (39) ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 1 |
| Parc de Montreal (40) ⚠️ | Montreal › L'Ile-Bizard--Sainte-Genevieve | 1 |
| Parc du Bassin-à-Gravier ⚠️ | Montreal › Sud-Ouest | 1 |
| Place Urbain-Baudreau-Graveline ⚠️ | Montreal › Plateau-Mont-Royal | 1 |
| Parc Gray (2) ⚠️ | Baie-D'Urfé | 1 |
| Parc Belmont ⚠️ | Montreal › Ahuntsic-Cartierville | 1 |
| Parc du Bout-de-l'Île ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc Pierre-Payet ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc Saint-Valérien ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Jardins Queen-Elizabeth ⚠️ | Westmount | 1 |
| Parc de Westmount (3) ⚠️ | Westmount | 1 |
| Parc de la Ferme-Brodie ⚠️ | Montreal › Sud-Ouest | 1 |
| Parc de Montreal (64) ⚠️ | Montreal › Rosemont--La-Petite-Patrie | 1 |
| Parc de la Bruère ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 1 |
| Parc Marie-LeFranc ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc McLearon ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc de Montreal (67) ⚠️ | Montreal › St-Leonard | 1 |
| Parc de Montreal (69) ⚠️ | Montreal › Rosemont--La-Petite-Patrie | 1 |
| Parc Jerry-Shears ⚠️ | Montreal › Saint-Laurent | 1 |
| Parc Roman-Zytynsky ⚠️ | Montreal › Saint-Laurent | 1 |
| Parc Robert-Stephenson ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc Claudine-Vallerand ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc André-Corbeil-Dit-Tranchemontagne ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc Louis-Hébert ⚠️ | Montreal › Ahuntsic-Cartierville | 1 |
| Parc de Montreal (72) ⚠️ | Montreal › LaSalle | 1 |
| Parc Rembrandt ⚠️ | Côte-Saint-Luc | 1 |
| Parc Nathan-Shuster ⚠️ | Côte-Saint-Luc | 1 |
| Parc Mitchell Brownstein ⚠️ | Côte-Saint-Luc | 1 |
| Fletcher Park ⚠️ | Côte-Saint-Luc | 1 |
| Parc de Côte-Saint-Luc ⚠️ | Côte-Saint-Luc | 1 |
| Parc de Côte-Saint-Luc (3) ⚠️ | Côte-Saint-Luc | 1 |
| Parc Saint-Jean-de-Matha ⚠️ | Montreal › Sud-Ouest | 1 |
| Parc John-Fisher ⚠️ | Pointe-Claire | 1 |
| Parc de Dorval (3) ⚠️ | Dorval | 1 |
| Parc de Montreal (74) ⚠️ | Montreal › Pierrefonds--Roxboro | 1 |
| Parc de Kirkland ⚠️ | Kirkland | 1 |
| Parc Gibson ⚠️ | Kirkland | 1 |
| Parc de Beaconsfield (6) ⚠️ | Beaconsfield | 1 |
| Parc Henri-Jarry ⚠️ | Beaconsfield | 1 |
| Parc de Beaconsfield (7) ⚠️ | Beaconsfield | 1 |
| Parc Godin ⚠️ | Sainte-Anne-de-Bellevue | 1 |
| Parc Denis-Benjamin-Viger ⚠️ | Montreal › L'Ile-Bizard--Sainte-Genevieve | 1 |
| Parc Aragon ⚠️ | Montreal › Pierrefonds--Roxboro | 1 |
| Parc des Bénévoles ⚠️ | Montreal › Pierrefonds--Roxboro | 1 |
| Parc Jean-Brillant ⚠️ | Montreal › Pierrefonds--Roxboro | 1 |
| Parc Raoul-Laurin ⚠️ | Montreal › Pierrefonds--Roxboro | 1 |
| Parc Marie-Claire-Daveluy ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc Gerry-Roufs ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc Pierre Dagenais-dit-Lépine ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc Zotique-Saint-Jean ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc Samuel-Morse ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc Hans-Selye ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc Francesco-Lacurto ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc Marcel-Léger ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc Richelieu (2) ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc du Cheval-Blanc ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc de Montreal (78) ⚠️ | Montreal › Montreal-Nord | 1 |
| Parc de Montreal (85) ⚠️ | Montreal › Montreal-Nord | 1 |
| Parc Primeau ⚠️ | Montreal › Montreal-Nord | 1 |
| Parc Charleroi ⚠️ | Montreal › Montreal-Nord | 1 |
| Parc Sainte-Lucie ⚠️ | Montreal › Villeray-Saint-Michel-Parc-Extension | 1 |
| Parc du Bois-Franc (3) ⚠️ | Montreal › Saint-Laurent | 1 |
| Parc Jean-J.-et-Marc-Thibodeau ⚠️ | Mont-Royal | 1 |
| Parc E.-B.-Jubien ⚠️ | Mont-Royal | 1 |
| Parc Godfroy-Langlois ⚠️ | Mont-Royal | 1 |
| Parc de la Paix (2) ⚠️ | Mont-Royal | 1 |
| Parc Kindersley ⚠️ | Mont-Royal | 1 |
| Parc Emerald ⚠️ | Mont-Royal | 1 |
| Parc Monsignor Harold-J.-Doran ⚠️ | Mont-Royal | 1 |
| Parc de Montreal (89) ⚠️ | Montreal › Cote-des-Neiges--Notre-Dame-de-Grace | 1 |
| Miniparc Grandbois ⚠️ | Montreal › St-Leonard | 1 |
| Miniparc de Ségur ⚠️ | Montreal › St-Leonard | 1 |
| Parc de Montreal (90) ⚠️ | Montreal › Pierrefonds--Roxboro | 1 |
| Parc de la Métairie ⚠️ | Montreal › Verdun--Ile-des-Soeurs | 1 |
| Parc de l'esplanade de la Pointe-Nord ⚠️ | Montreal › Verdun--Ile-des-Soeurs | 1 |
| Place Iona-Monahan ⚠️ | Montreal › Ahuntsic-Cartierville | 1 |
| Aire de repos Île-Mercier ⚠️ | Montreal › L'Ile-Bizard--Sainte-Genevieve | 1 |
| Parc Julie-Dauth ⚠️ | Montreal › Pierrefonds--Roxboro | 1 |
| Parc Riviera ⚠️ | Montreal › L'Ile-Bizard--Sainte-Genevieve | 1 |
| Parc Cardinal (2) ⚠️ | Montreal › L'Ile-Bizard--Sainte-Genevieve | 1 |
| Parc Shakespeare ⚠️ | Dollard-Des-Ormeaux | 1 |
| Parc Langhorne ⚠️ | Hampstead | 1 |
| Parc Dorset ⚠️ | Baie-D'Urfé | 1 |
| Parc Fritz (2) ⚠️ | Baie-D'Urfé | 1 |
| Parc Saint-Marcel ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc Verdelles ⚠️ | Montreal › Anjou | 1 |
| Parc Clément-Jetté Sud ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 1 |
| Parc du Bocage ⚠️ | Montreal › Anjou | 1 |
| Parc des Vétérans ⚠️ | Côte-Saint-Luc | 1 |
| Parc de Montreal (94) ⚠️ | Montreal › Pierrefonds--Roxboro | 1 |
| Parc Belvédère Terry-Fox ⚠️ | Montreal › Cote-des-Neiges--Notre-Dame-de-Grace | 1 |
| Parc de la Malva ⚠️ | Montreal › Pierrefonds--Roxboro | 1 |
| City Hall Park ⚠️ | Montreal › LaSalle | 1 |
| Parc Maria-Goretti ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc Sutherland-Sackville-Bain ⚠️ | Montreal › Verdun--Ile-des-Soeurs | 1 |
| Parc-école Notre Dame ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc du Ruisseau-du-Pont-à-l’Avoine ⚠️ | Montreal › Villeray-Saint-Michel-Parc-Extension | 1 |
| Parc Highridge ⚠️ | Beaconsfield | 1 |
| Parc Guglielmo-Marconi ⚠️ | Montreal › Rosemont--La-Petite-Patrie | 1 |
| Parc Pierre-Dansereau ⚠️ | Montreal › Outremont | 1 |
| Parc Coolbrook ⚠️ | Dollard-Des-Ormeaux | 1 |
| Parc de Montreal (110) ⚠️ | Montreal › LaSalle | 1 |
| Plage de l'Est ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Place au Soleil Mullins ⚠️ | Montreal › Sud-Ouest | 1 |
| Parc Victor Gray ⚠️ | Montreal › Pierrefonds--Roxboro | 1 |
| Parc de Montreal (114) ⚠️ | Montreal › Anjou | 1 |
| Parc de Montreal (115) ⚠️ | Montreal › Ahuntsic-Cartierville | 1 |
| Promenade de l'Aqueduc ⚠️ | Montreal › LaSalle | 1 |
| Parc Julia-Drummond ⚠️ | Montreal › Ville-Marie | 1 |
| Parc Juliette-Huot ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 1 |
| Parc François-La Bernarde ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc Marie-Claire-Kirkland-Casgrain ⚠️ | Montreal › LaSalle | 1 |
| Parc d'Argenson (2) ⚠️ | Montreal › Sud-Ouest | 1 |
| Parc Gadbois ⚠️ | Montreal › Sud-Ouest | 1 |
| Parc de la Grande-Anse (2) ⚠️ | Pointe-Claire | 1 |
| Parc Bayview ⚠️ | Pointe-Claire | 1 |
| Parc Neptune ⚠️ | Dorval | 1 |
| Parc Félix-Leclerc (4) ⚠️ | Montreal › Anjou | 1 |
| Parc des Gorilles ⚠️ | Montreal › Rosemont--La-Petite-Patrie | 1 |
| Parc Saint-André-Apôtre ⚠️ | Montreal › Ahuntsic-Cartierville | 1 |
| Parc Roland-Giguère ⚠️ | Montreal › Ahuntsic-Cartierville | 1 |
| Parc Basile-Routhier ⚠️ | Montreal › Ahuntsic-Cartierville | 1 |
| Parc Robillard ⚠️ | Sainte-Anne-de-Bellevue | 1 |
| Parc de Mésy ⚠️ | Montreal › Ahuntsic-Cartierville | 1 |
| Parc D'Auteuil ⚠️ | Montreal › Ahuntsic-Cartierville | 1 |
| Parc de Deauville ⚠️ | Montreal › Pierrefonds--Roxboro | 1 |
| Parc Cyril-W.-MacDonald ⚠️ | Montreal › Pierrefonds--Roxboro | 1 |
| Parc de Dollard-Des-Ormeaux (4) ⚠️ | Dollard-Des-Ormeaux | 1 |
| Parc Holleuffer ⚠️ | Kirkland | 1 |
| Parc de Bordeaux ⚠️ | Montreal › Ahuntsic-Cartierville | 1 |
| Parc Nicolas-Viel ⚠️ | Montreal › Ahuntsic-Cartierville | 1 |
| Parc Dixie ⚠️ | Montreal › Lachine | 1 |
| Parc Dollier-de-Casson ⚠️ | Montreal › LaSalle | 1 |
| Musée de Lachine ⚠️ | Montreal › Lachine | 1 |
| Parc Commémoratif (2) ⚠️ | Montréal-Ouest | 1 |
| Parc Clifford ⚠️ | Montreal › Sud-Ouest | 1 |
| Parc Grovehill (2) ⚠️ | Montreal › Cote-des-Neiges--Notre-Dame-de-Grace | 1 |
| Parc de Montreal (135) ⚠️ | Montreal › Rosemont--La-Petite-Patrie | 1 |
| Parc Coffee ⚠️ | Montreal › Cote-des-Neiges--Notre-Dame-de-Grace | 1 |
| Parc Houde (3) ⚠️ | Montreal › Saint-Laurent | 1 |
| Parc Decelles ⚠️ | Montreal › Saint-Laurent | 1 |
| Parc Zotique-Racicot ⚠️ | Montreal › Ahuntsic-Cartierville | 1 |
| Parc De Salaberry ⚠️ | Montreal › Ahuntsic-Cartierville | 1 |
| Parc de Montreal (136) ⚠️ | Montreal › Ahuntsic-Cartierville | 1 |
| Parc Albert-Malouf ⚠️ | Montreal › Ahuntsic-Cartierville | 1 |
| Parc de Montreal (138) ⚠️ | Montreal › Sud-Ouest | 1 |
| Parc de Montreal (139) ⚠️ | Montreal › Sud-Ouest | 1 |
| Parc de Montreal (140) ⚠️ | Montreal › Sud-Ouest | 1 |
| Parc du Bassin-Bonsecours ⚠️ | Montreal › Ville-Marie | 1 |
| Parc des Fondatrices-de-Saint-Léonard ⚠️ | Montreal › St-Leonard | 1 |
| Terrain d'athlétisme de Westmount ⚠️ | Westmount | 1 |
| Parc Suzanne-Beaudoin-Dumouchel ⚠️ | Montreal › Ahuntsic-Cartierville | 1 |
| Parc Saint-Paul-de-la-Croix ⚠️ | Montreal › Ahuntsic-Cartierville | 1 |
| Parc de Montreal (153) ⚠️ | Montreal › Ahuntsic-Cartierville | 1 |
| Parc de Dollard-Des-Ormeaux (7) ⚠️ | Dollard-Des-Ormeaux | 1 |
| Parc de Montreal (154) ⚠️ | Montreal › L'Ile-Bizard--Sainte-Genevieve | 1 |
| Square Cabot ⚠️ | Montreal › Ville-Marie | 1 |
| Parc Garon–Amos ⚠️ | Montreal › Montreal-Nord | 1 |
| Jardins du Petit-Laurier ⚠️ | Montreal › Plateau-Mont-Royal | 1 |
| Parc Percy-Walters ⚠️ | Montreal › Ville-Marie | 1 |
| Parc de Montreal (160) ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 1 |
| Baseball court (Seigniory Park) ⚠️ | Pointe-Claire | 1 |
| Carré du Nordet ⚠️ | Montreal › Saint-Laurent | 1 |
| Parc Parent ⚠️ | Montreal › LaSalle | 1 |
| Parc de Montreal (174) ⚠️ | Montreal › Mercier-Hochelaga-Maisonneuve | 1 |
| Parc Smiley ⚠️ | Kirkland | 1 |
| Parc de Montreal (175) ⚠️ | Montreal › Ville-Marie | 1 |
| Parc de la Rive-Boisée ⚠️ | Montreal › Pierrefonds--Roxboro | 1 |
| Parc Urgel-Archambault ⚠️ | Montreal › Saint-Laurent | 1 |
| Parc Edgewater ⚠️ | Pointe-Claire | 1 |
| Parc Saint-James ⚠️ | Beaconsfield | 1 |
| Parc Ernest-Rouleau ⚠️ | Montreal › Pointe-aux-Trembles-Rivieres-des-Prairies | 1 |
| Parc Highlands ⚠️ | Montreal › LaSalle | 1 |
| Parc des Saints-Anges ⚠️ | Montreal › LaSalle | 1 |
| Esplanade Jean-Doré ⚠️ | Montreal › Sud-Ouest | 1 |
| Parc Woodland ⚠️ | Montreal › Verdun--Ile-des-Soeurs | 1 |
| Parc Jean-Brillant (2) ⚠️ | Montreal › Cote-des-Neiges--Notre-Dame-de-Grace | 1 |
| Parc des Amériques ⚠️ | Montreal › Plateau-Mont-Royal | 1 |
| Parc Mahatma Gandhi ⚠️ | Montreal › Cote-des-Neiges--Notre-Dame-de-Grace | 1 |
| Parc Pratt ⚠️ | Montreal › Outremont | 1 |
| Parc de Westmount (7) ⚠️ | Westmount | 1 |
| Parc de Montreal (179) ⚠️ | Montreal › Sud-Ouest | 1 |
| Ovila-Légaré ⚠️ | Montreal › Villeray-Saint-Michel-Parc-Extension | 1 |
| Parc Sault-au-Recollet ⚠️ | Montreal › Ahuntsic-Cartierville | 1 |
| Parc Kirkland (2) ⚠️ | Montreal › Lachine | 1 |
| Parc Guillaume-Bruneau ⚠️ | Montreal › Saint-Laurent | 1 |
| Parc Raymond-Lagacé ⚠️ | Montreal › Saint-Laurent | 1 |
| Parc Vinet ⚠️ | Montreal › Sud-Ouest | 1 |
| Parc Sammy-Hill ⚠️ | Montreal › Sud-Ouest | 1 |
| Woonerf Saint-Pierre ⚠️ | Montreal › Sud-Ouest | 1 |

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
| Montreal | 243 |
| Saint-Laurent | 194 |
| Mercier-Hochelaga-Maisonneuve | 47 |
| Pointe-aux-Trembles-Rivieres-des-Prairies | 6 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
