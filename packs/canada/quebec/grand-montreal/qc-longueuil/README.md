# Agglomération de Longueuil

Pack `qc-longueuil` · version 1.2.1 · grille 200 m · Canada › Québec › Grand Montréal

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 14 331 |
| dont restreintes (aéroport, militaire, prison) | 305 |
| dont sans chemin (aucune voie à moins de 60 m) | 2 526 |
| Cellules retirées par le masque d'eau | 1 109 |
| Villes | 5 |
| Arrondissements et quartiers | 11 |
| Îles | 0 |
| Parcs | 522 |

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
| **Sans chemin** | parmi les comptées, celles qu'aucune voie n'approche à moins de 60 m — l'utilisateur peut les marquer inaccessibles zone par zone, elles restent comptées tant qu'il ne le fait pas |

## Villes (5)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Sans chemin | Parcs |
|---|---:|---:|---:|---:|---:|---:|---:|
| Longueuil | 6 238 | 341 | 5 897 | 218 | **5 679** | 798 (14 %) | 229 |
| Boucherville | 4 182 | 594 | 3 588 | 0 | **3 588** | 999 (28 %) | 86 |
| Brossard | 2 300 | 1 | 2 299 | 0 | **2 299** | 337 (15 %) | 128 |
| Saint-Bruno-de-Montarville | 2 216 | 50 | 2 166 | 87 | **2 079** | 390 (19 %) | 37 |
| Saint-Lambert | 504 | 123 | 381 | 0 | **381** | 2 (1 %) | 39 |

## Arrondissements et quartiers (11)

| Zone | Ville | Brut | Eau | Sans eau | Restr. | Comptées | Sans chemin | Parcs |
|---|---|---:|---:|---:|---:|---:|---:|---:|
| Saint-Hubert | longueuil | 3 371 | 4 | 3 367 | 218 | **3 149** | 716 (23 %) | 81 |
| Le Vieux-Longueuil | longueuil | 2 621 | 337 | 2 284 | 0 | **2 284** | 82 (4 %) | 132 |
| Greenfield Park | longueuil | 246 | 0 | 246 | 0 | **246** |  | 16 |
| Secteur L | brossard | 192 | 1 | 191 | 0 | **191** |  | 24 |
| Secteur R | brossard | 147 | 2 | 145 | 0 | **145** |  | 6 |
| Secteur M | brossard | 87 | 0 | 87 | 0 | **87** |  | 16 |
| Secteur O | brossard | 79 | 0 | 79 | 0 | **79** |  | 13 |
| Secteur J | brossard | 61 | 0 | 61 | 0 | **61** | 8 (13 %) |  |
| Secteur N | brossard | 59 | 0 | 59 | 0 | **59** |  | 6 |
| Secteur I | brossard | 55 | 1 | 54 | 0 | **54** |  | 1 |
| Secteur E | brossard | 19 | 0 | 19 | 0 | **19** |  | 1 |

## Parcs (522)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Parc national du Mont-Saint-Bruno ⚠️ | Saint-Bruno-de-Montarville | 423 |
| Parc national des Îles-de-Boucherville ⚠️ | Boucherville | 339 |
| Réserve naturelle du Bois-de-Brossard | Brossard | 119 |
| Parc Michel Chartrand | Longueuil › Le Vieux-Longueuil | 86 |
| Parc Jean-Drapeau | — | 84 |
| Parc de la Cité | Longueuil › Saint-Hubert | 53 |
| Parc Marie-Victorin (3) | Saint-Bruno-de-Montarville | 23 |
| Parc de la Voie maritime | Saint-Lambert | 10 |
| Parc Pierre-Laporte (2) ⚠️ | Boucherville | 9 |
| Refuge d'oiseaux migrateurs des Îles-de-la-Couvée ⚠️ | Saint-Lambert | 9 |
| Parc du Boisé-Du-Pays-Brûlé ⚠️ | Boucherville | 7 |
| Parc Marie-Victorin (4) ⚠️ | Longueuil › Le Vieux-Longueuil | 7 |
| Parc de la Terre ⚠️ | Brossard | 6 |
| Parc de la Pointe-du-Marigot ⚠️ | Longueuil › Le Vieux-Longueuil | 6 |
| Parc de l’Île Charron ⚠️ | Longueuil › Le Vieux-Longueuil | 5 |
| Grand Parc Urbain ⚠️ | Brossard | 5 |
| Parc Edmour-J.-Harvey ⚠️ | Saint-Bruno-de-Montarville | 5 |
| Parc Illinois ⚠️ | Brossard › Secteur I | 4 |
| Parc Poly-Aréna ⚠️ | Brossard › Secteur N | 4 |
| Parc Sorbonne ⚠️ | Brossard | 4 |
| Parc de Mortagne ⚠️ | Boucherville | 4 |
| Parc des Tilleuls (2) ⚠️ | Saint-Bruno-de-Montarville | 4 |
| Parc de la Mairie ⚠️ | Boucherville | 4 |
| Parc Rosanne-Laflamme (2) ⚠️ | Longueuil › Saint-Hubert | 4 |
| Centennial Park ⚠️ | Longueuil › Greenfield Park | 4 |
| Parc Léon-Gravel ⚠️ | Brossard › Secteur R | 3 |
| Parc Pierre-Laporte ⚠️ | Longueuil › Saint-Hubert | 3 |
| Parc Paul-Pratt ⚠️ | Longueuil › Le Vieux-Longueuil | 3 |
| Parc Laurier ⚠️ | Longueuil › Le Vieux-Longueuil | 3 |
| Parc Lecavalier ⚠️ | Longueuil › Le Vieux-Longueuil | 3 |
| Parc Thomas-Dubuc ⚠️ | Longueuil › Le Vieux-Longueuil | 3 |
| Parc René-Veillet ⚠️ | Longueuil › Greenfield Park | 3 |
| Parc de Normandie ⚠️ | Boucherville | 3 |
| Parc de Picardie ⚠️ | Boucherville | 3 |
| Parc Vincent d'Indy ⚠️ | Boucherville | 3 |
| Parc Bois-de-Brouage ⚠️ | Boucherville | 3 |
| Parc Rabastalière ⚠️ | Saint-Bruno-de-Montarville | 3 |
| Parc Duquesne ⚠️ | Saint-Bruno-de-Montarville | 3 |
| Parc De La Rivière-aux-pins ⚠️ | Boucherville | 3 |
| Parc Empire ⚠️ | Longueuil › Greenfield Park | 3 |
| Parc Immaculée-Conception ⚠️ | Longueuil › Saint-Hubert | 3 |
| Parc Anne-Marie-Lemay ⚠️ | Boucherville | 3 |
| Parc Gentilly Ouest ⚠️ | Longueuil › Le Vieux-Longueuil | 3 |
| Parc de Boucherville (12) ⚠️ | Boucherville | 3 |
| Parc Chevrier ⚠️ | Brossard | 3 |
| Parc Des Gouverneurs ⚠️ | Boucherville | 3 |
| Parc Radisson ⚠️ | Brossard › Secteur R | 2 |
| Parc Roger ⚠️ | Brossard › Secteur R | 2 |
| Parc écologique des Sansonnets ⚠️ | Brossard | 2 |
| Parc Balzac ⚠️ | Brossard | 2 |
| Parc Campbell ⚠️ | Longueuil › Saint-Hubert | 2 |
| Parc Marie-Victorin ⚠️ | Brossard | 2 |
| Park Parc Vanier ⚠️ | Brossard | 2 |
| Parc Lautrec ⚠️ | Brossard › Secteur L | 2 |
| Parc Olympia ⚠️ | Brossard › Secteur O | 2 |
| Parc Leckie ⚠️ | Longueuil › Saint-Hubert | 2 |
| Parc Lionel-Groulx ⚠️ | Longueuil › Le Vieux-Longueuil | 2 |
| Parc Christ-Roi ⚠️ | Longueuil › Le Vieux-Longueuil | 2 |
| Parc Racine ⚠️ | Longueuil › Le Vieux-Longueuil | 2 |
| Parc Des Hirondelles ⚠️ | Longueuil › Le Vieux-Longueuil | 2 |
| Parc Daniel-Johnson ⚠️ | Longueuil › Saint-Hubert | 2 |
| Parc Champvert ⚠️ | Longueuil › Le Vieux-Longueuil | 2 |
| Parc Pierre-Boucher (2) ⚠️ | Boucherville | 2 |
| Parc Jean-Jacques-Bertrand ⚠️ | Longueuil › Saint-Hubert | 2 |
| Parc Joseph-de-Sérigny ⚠️ | Longueuil › Le Vieux-Longueuil | 2 |
| Parc de Boucherville ⚠️ | Boucherville | 2 |
| Parc de la Coulée ⚠️ | Saint-Bruno-de-Montarville | 2 |
| Place de la Paix (2) ⚠️ | Boucherville | 2 |
| Parc des Explorateurs ⚠️ | Boucherville | 2 |
| Parc Laflamme ⚠️ | Longueuil › Le Vieux-Longueuil | 2 |
| Parc Marquette ⚠️ | Longueuil › Le Vieux-Longueuil | 2 |
| Parc des vétérans (2) ⚠️ | Longueuil › Saint-Hubert | 2 |
| Parc de Longueuil (17) ⚠️ | Longueuil › Saint-Hubert | 2 |
| Park Parc Raymond-Brassard ⚠️ | Longueuil › Saint-Hubert | 2 |
| Parc Gérard-Philipps ⚠️ | Longueuil › Saint-Hubert | 2 |
| Parc Préville ⚠️ | Saint-Lambert | 2 |
| Parc des vélos ⚠️ | Brossard | 2 |
| Parc Belcourt ⚠️ | Longueuil › Le Vieux-Longueuil | 2 |
| Parc Arthur- Dumouchel ⚠️ | Boucherville | 2 |
| Parc Baudelaire ⚠️ | Brossard | 2 |
| Parc des Glaïeuls ⚠️ | Longueuil › Saint-Hubert | 2 |
| Parc de Longueuil (23) ⚠️ | Longueuil › Saint-Hubert | 2 |
| Parc de l'Union ⚠️ | Saint-Lambert | 2 |
| Parc Central (2) ⚠️ | Longueuil › Le Vieux-Longueuil | 2 |
| Parc de Brixton ⚠️ | Saint-Lambert | 2 |
| Parc Champlain (3) ⚠️ | Brossard | 2 |
| Parc Alain-Forget ⚠️ | Longueuil › Saint-Hubert | 2 |
| Parc Saint-Alphonse ⚠️ | Brossard | 2 |
| Parc des Semis ⚠️ | Longueuil › Le Vieux-Longueuil | 2 |
| Parc de Boucherville (13) ⚠️ | Boucherville | 2 |
| Parc Jacques-de-Noyon ⚠️ | Boucherville | 2 |
| Parc de Boucherville (19) ⚠️ | Boucherville | 2 |
| Parc de Longueuil (47) ⚠️ | Longueuil › Saint-Hubert | 2 |
| Parc Marcel-Simard ⚠️ | Longueuil › Saint-Hubert | 2 |
| Parc Nicole Lemaire ⚠️ | Boucherville | 2 |
| Parc Sainte-Marie ⚠️ | Brossard › Secteur O | 1 |
| Parc de Brossard ⚠️ | Brossard › Secteur L | 1 |
| Parc Océanie ⚠️ | Brossard › Secteur O | 1 |
| Parc Briand ⚠️ | Brossard | 1 |
| Parc de Brossard (8) ⚠️ | Brossard › Secteur M | 1 |
| Parc Montpetit ⚠️ | Brossard › Secteur M | 1 |
| Parc Bernini ⚠️ | Brossard | 1 |
| Parc Vallerand ⚠️ | Brossard | 1 |
| Parc de Brossard (21) ⚠️ | Brossard | 1 |
| Parc de Brossard (24) ⚠️ | Brossard › Secteur O | 1 |
| Parc Pellan ⚠️ | Brossard | 1 |
| Parc Santerre ⚠️ | Brossard | 1 |
| Parc Malo ⚠️ | Brossard › Secteur M | 1 |
| Parc Perras ⚠️ | Longueuil › Saint-Hubert | 1 |
| Parc Saint-Judes ⚠️ | Longueuil › Greenfield Park | 1 |
| Parc Gentilly Est ⚠️ | Longueuil › Le Vieux-Longueuil | 1 |
| Parc Beaune ⚠️ | Brossard | 1 |
| Parc Béliveau ⚠️ | Brossard | 1 |
| Parc Marie-Josée-Vandette ⚠️ | Longueuil › Saint-Hubert | 1 |
| Parc de Longueuil (4) ⚠️ | Longueuil › Saint-Hubert | 1 |
| Parc Gabrielle-Roy ⚠️ | Saint-Bruno-de-Montarville | 1 |
| Parc Jolliet ⚠️ | Saint-Bruno-de-Montarville | 1 |
| Parc Albert-Schweitzer ⚠️ | Saint-Bruno-de-Montarville | 1 |
| Marguerite-A.-Tessier ⚠️ | Boucherville | 1 |
| Park Parc Louis-Brosseau ⚠️ | Longueuil › Saint-Hubert | 1 |
| Parc Jean-Pierre-Côté ⚠️ | Longueuil › Le Vieux-Longueuil | 1 |
| Parc Saint-Charles (2) ⚠️ | Longueuil › Le Vieux-Longueuil | 1 |
| Parc Gardenville ⚠️ | Longueuil › Le Vieux-Longueuil | 1 |
| Parc Jean-De-Lalande ⚠️ | Longueuil › Le Vieux-Longueuil | 1 |
| Parc Bréboeuf ⚠️ | Longueuil › Le Vieux-Longueuil | 1 |
| Parc Le Moyne ⚠️ | Longueuil › Le Vieux-Longueuil | 1 |
| Parc Champlain ⚠️ | Longueuil › Le Vieux-Longueuil | 1 |
| Parc DuBuisson ⚠️ | Longueuil › Le Vieux-Longueuil | 1 |
| Parc Bellerive ⚠️ | Longueuil › Le Vieux-Longueuil | 1 |
| Parc Marquis-De-Montcalm ⚠️ | Longueuil › Le Vieux-Longueuil | 1 |
| Parc Jardins Des Pinsons ⚠️ | Longueuil › Le Vieux-Longueuil | 1 |
| Parc Jean-Louis ⚠️ | Longueuil › Le Vieux-Longueuil | 1 |
| Parc Sacré-Coeur ⚠️ | Longueuil › Le Vieux-Longueuil | 1 |
| Parc Villion ⚠️ | Brossard | 1 |
| Parc Jean-Gareau ⚠️ | Boucherville | 1 |
| Parc Perron (2) ⚠️ | Longueuil › Le Vieux-Longueuil | 1 |
| Parc Fernand-Bouffard ⚠️ | Longueuil › Le Vieux-Longueuil | 1 |
| Parc Roméo-Vachon ⚠️ | Longueuil › Saint-Hubert | 1 |
| Parc Fonrouge ⚠️ | Longueuil › Le Vieux-Longueuil | 1 |
| Parc Gordon ⚠️ | Saint-Lambert | 1 |
| Parc Carillon ⚠️ | Longueuil › Le Vieux-Longueuil | 1 |
| Parc Franchère ⚠️ | Longueuil › Le Vieux-Longueuil | 1 |
| Parc St-Nazaire ⚠️ | Longueuil › Saint-Hubert | 1 |
| Parc Raymond ⚠️ | Longueuil › Le Vieux-Longueuil | 1 |
| Parc de Longueuil (13) ⚠️ | Longueuil › Le Vieux-Longueuil | 1 |
| Parc Sabrevois ⚠️ | Boucherville | 1 |
| Parc D'Iberville ⚠️ | Boucherville | 1 |
| Parc Joseph-Huet ⚠️ | Boucherville | 1 |
| Parc Adoncour ⚠️ | Longueuil › Le Vieux-Longueuil | 1 |
| Parc de Longueuil (14) ⚠️ | Longueuil › Le Vieux-Longueuil | 1 |
| Parc Bariteau ⚠️ | Longueuil › Le Vieux-Longueuil | 1 |
| Parc Bisaillon ⚠️ | Saint-Bruno-de-Montarville | 1 |
| Parc Pontbriand ⚠️ | Saint-Bruno-de-Montarville | 1 |
| Parc Monseigneur-Gilles-Gervais ⚠️ | Saint-Bruno-de-Montarville | 1 |
| Parc Sommet-Trinité ⚠️ | Saint-Bruno-de-Montarville | 1 |
| Parc de Saint-Bruno-de-Montarville (2) ⚠️ | Saint-Bruno-de-Montarville | 1 |
| Parc Charles-Desmarteau-Père ⚠️ | Boucherville | 1 |
| Parc Antoine-Girouard ⚠️ | Boucherville | 1 |
| Parc Boisvert ⚠️ | Longueuil › Saint-Hubert | 1 |
| Parc Houde (2) ⚠️ | Saint-Lambert | 1 |
| Parc De L'Église ⚠️ | Longueuil › Le Vieux-Longueuil | 1 |
| Parc de Boucherville (2) ⚠️ | Boucherville | 1 |
| Parc des Pâquerettes ⚠️ | Longueuil › Saint-Hubert | 1 |
| Parc Raymond-Comeau ⚠️ | Longueuil › Saint-Hubert | 1 |
| Parc Jardins De Lorraine ⚠️ | Longueuil › Le Vieux-Longueuil | 1 |
| Jardin Du Cerf ⚠️ | Longueuil › Le Vieux-Longueuil | 1 |
| Parc Alexandra ⚠️ | Saint-Lambert | 1 |
| Parc Upper-Edison ⚠️ | Saint-Lambert | 1 |
| Parc École Rabeau ⚠️ | Saint-Lambert | 1 |
| Parc Lespérance ⚠️ | Saint-Lambert | 1 |
| Parc de Brossard (44) ⚠️ | Brossard › Secteur L | 1 |
| Parc du Ruisseau (4) ⚠️ | Saint-Bruno-de-Montarville | 1 |
| Parc du Boisé (2) ⚠️ | Boucherville | 1 |
| Parc Pierre-Mercure ⚠️ | Boucherville | 1 |
| Parc Michel-Sarrazin ⚠️ | Saint-Bruno-de-Montarville | 1 |
| Parc des Pins (5) ⚠️ | Saint-Bruno-de-Montarville | 1 |
| Parc de Brossard (52) ⚠️ | Brossard | 1 |
| Parc de Brossard (53) ⚠️ | Brossard | 1 |
| Parc Allée des Sorbiers ⚠️ | Longueuil › Saint-Hubert | 1 |
| Parc de Longueuil (24) ⚠️ | Longueuil › Saint-Hubert | 1 |
| Parc Davidson/Lavoie ⚠️ | Longueuil › Saint-Hubert | 1 |
| Parc Lunan ⚠️ | Brossard › Secteur L | 1 |
| Parc D.E. Joyal ⚠️ | Longueuil › Saint-Hubert | 1 |
| Parc du Havre (2) ⚠️ | Brossard | 1 |
| Parc Quincy-Sous-Sénart ⚠️ | Saint-Bruno-de-Montarville | 1 |
| Réseau vert bleu Harmonie (2) ⚠️ | Boucherville | 1 |
| Parc Baker ⚠️ | Brossard | 1 |
| Parc Jubilee ⚠️ | Longueuil › Greenfield Park | 1 |
| Parc Marquis-De Tracy ⚠️ | Boucherville | 1 |
| Parc De Caumont ⚠️ | Boucherville | 1 |
| Réserve naturelle du Boisé-Du Tremblay ⚠️ | Boucherville | 1 |
| Parc du Golf ⚠️ | Saint-Lambert | 1 |
| Parc Aumont (2) ⚠️ | Brossard | 1 |
| Parc Stephen-Olynyk ⚠️ | Longueuil › Greenfield Park | 1 |
| Parc Bertrand-Lesage ⚠️ | Boucherville | 1 |
| Parc de Boucherville (18) ⚠️ | Boucherville | 1 |
| Parc de Brossard (56) ⚠️ | Brossard | 1 |
| Parc de Bretagne ⚠️ | Saint-Lambert | 1 |
| Centre de Plein Air Brossard ⚠️ | Brossard | 1 |
| Parc du Patriote-Joseph-Vincent ⚠️ | Longueuil › Saint-Hubert | 1 |
| Parc du Soldat-Simon-Longtin ⚠️ | Longueuil › Saint-Hubert | 1 |
| Parc de Boucherville (23) ⚠️ | Boucherville | 1 |
| Héritage Champlain (2) ⚠️ | Brossard | 1 |
| Parc de Liège ⚠️ | Brossard › Secteur L | 1 |
| Parc linéaire Desaulniers (5) ⚠️ | Longueuil › Le Vieux-Longueuil | 1 |
| Parc de Saint-Bruno-de-Montarville (4) ⚠️ | Saint-Bruno-de-Montarville | 1 |
| Esplanade Alarie-Simoneau ⚠️ | Boucherville | 1 |
| Parc Jacques-Rousseau ⚠️ | Saint-Bruno-de-Montarville | 1 |

314 parc(s) plus petits qu'une cellule ne sont pas listés : la carte les dessine, mais ils n'offrent aucune cellule.

⚠️ 516 parc(s) hors de la fenêtre 10–125 cellules (514 trop petit(s), 2 trop grand(s)) : affichés sur la carte, mais ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| airport | 218 |
| military | 87 |
| prison | 0 |
| **Total déclaré** | **305** |
| dont dans une zone de ce territoire | 305 |


### Zones concernées

| Zone | Cellules exclues |
|---|---:|
| Saint-Hubert | 218 |
| Longueuil | 218 |
| Saint-Bruno-de-Montarville | 87 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
