# Agglomération de Québec

Pack `qc-quebec-agglo` · version 1.0.1 · grille 200 m · Canada › Québec › Grand Québec

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 29 348 |
| dont restreintes (aéroport, militaire, prison) | 792 |
| dont sans chemin (aucune voie à moins de 60 m) | 8 223 |
| Cellules retirées par le masque d'eau | 2 703 |
| Villes | 3 |
| Arrondissements et quartiers | 6 |
| Îles | 0 |
| Parcs | 478 |

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

## Villes (3)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Sans chemin | Parcs |
|---|---:|---:|---:|---:|---:|---:|---:|
| Québec | 25 909 | 1 667 | 24 242 | 792 | **23 450** | 5 731 (24 %) | 441 |
| Saint-Augustin-de-Desmaures | 5 607 | 1 036 | 4 571 | 0 | **4 571** | 2 483 (54 %) | 21 |
| L'Ancienne-Lorette | 409 | 0 | 409 | 0 | **409** | 5 (1 %) | 12 |

## Arrondissements et quartiers (6)

| Zone | Ville | Brut | Eau | Sans eau | Restr. | Comptées | Sans chemin | Parcs |
|---|---|---:|---:|---:|---:|---:|---:|---:|
| La Haute-Saint-Charles | quebec | 8 257 | 241 | 8 016 | 497 | **7 519** | 2 928 (39 %) | 70 |
| Sainte-Foy–Sillery–Cap-Rouge | quebec | 5 157 | 89 | 5 068 | 286 | **4 782** | 1 401 (29 %) | 106 |
| Beauport | quebec | 4 490 | 531 | 3 959 | 0 | **3 959** | 778 (20 %) | 57 |
| Charlesbourg | quebec | 3 576 | 29 | 3 547 | 1 | **3 546** | 531 (15 %) | 37 |
| Les Rivières | quebec | 2 597 | 25 | 2 572 | 0 | **2 572** | 85 (3 %) | 65 |
| La Cité-Limoilou | quebec | 1 277 | 72 | 1 205 | 8 | **1 197** | 12 (1 %) | 107 |

## Parcs (478)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Parc naturel du mont Bélair ⚠️ | Québec › La Haute-Saint-Charles | 362 |
| Base de plein air de Sainte-Foy | Québec › Sainte-Foy–Sillery–Cap-Rouge | 62 |
| Parc Chauveau | Québec › Les Rivières | 58 |
| Parc des Champs-de-Bataille | Québec › La Cité-Limoilou | 45 |
| Parc de Montchâtel | Québec › La Haute-Saint-Charles | 45 |
| Parc linéaire de la rivière Saint-Charles | Québec › La Cité-Limoilou | 41 |
| Réserve naturelle des Capteuses-de-Rêve | Québec › La Haute-Saint-Charles | 31 |
| Parc des Saules | Québec › Les Rivières | 26 |
| Réserve naturelle des Marais-du-Nord | Québec › La Haute-Saint-Charles | 24 |
| Parc de la Rivière | L'Ancienne-Lorette | 23 |
| Parc riverain du lac Saint-Augustin | Saint-Augustin-de-Desmaures | 19 |
| Parc de la Chute-Montmorency | Québec › Beauport | 16 |
| Domaine de Maizerets | Québec › La Cité-Limoilou | 15 |
| Parc du Bois-de-Coulonge | Québec › Sainte-Foy–Sillery–Cap-Rouge | 11 |
| Parc de Duberger | Québec › Les Rivières | 10 |
| Parc de la Famille | Québec › Beauport | 10 |
| Parc Victoria ⚠️ | Québec › La Cité-Limoilou | 9 |
| Réserve naturelle des Battures-de-Saint-Augustin-de-Desmaures ⚠️ | Saint-Augustin-de-Desmaures | 9 |
| Parc de Québec (42) ⚠️ | Québec › Charlesbourg | 8 |
| Parc de Québec (44) ⚠️ | Québec › Charlesbourg | 8 |
| Parc de la Montagne-des-Roches ⚠️ | Québec › Charlesbourg | 8 |
| Réserve naturelle du Marais-Léon-Provancher ⚠️ | Saint-Augustin-de-Desmaures | 7 |
| Réserve naturelle de la Station-Agronomique-de-l'Université-Laval ⚠️ | Saint-Augustin-de-Desmaures | 7 |
| Parc de la Pointe-aux-Lièvres ⚠️ | Québec › La Cité-Limoilou | 6 |
| Parc linéaire du coteau Sainte-Geneviève ⚠️ | Québec › La Cité-Limoilou | 5 |
| Parc Saint-Viateur ⚠️ | Québec › Charlesbourg | 5 |
| Parc Saint-David ⚠️ | Québec › Beauport | 5 |
| Parc de la Rivière-Beauport ⚠️ | Québec › Beauport | 5 |
| Parc du Périgord ⚠️ | Québec › Charlesbourg | 5 |
| Parc linéaire de la Rivière-des-Roches ⚠️ | Québec › Charlesbourg | 5 |
| Parc Cartier-Brébeuf ⚠️ | Québec › La Cité-Limoilou | 5 |
| Parc Henri-Casault ⚠️ | Québec › Charlesbourg | 4 |
| Parc de la Carrière ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 4 |
| Parc de l'Escarpement ⚠️ | Québec › Les Rivières | 4 |
| Parc de la Falaise ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 4 |
| Parc Delphis-Marois ⚠️ | Saint-Augustin-de-Desmaures | 4 |
| Parc de Québec ⚠️ | Québec › Beauport | 3 |
| Parc Jean-Marc-Gauthier ⚠️ | Québec › Les Rivières | 3 |
| Parc de Québec (2) ⚠️ | Québec › La Cité-Limoilou | 3 |
| Parc Bardy ⚠️ | Québec › La Cité-Limoilou | 3 |
| Parc de la Terrasse-du-Bon-Air ⚠️ | Québec › Charlesbourg | 3 |
| Parc Saint-Jérôme-de-l'Auvergne ⚠️ | Québec › Charlesbourg | 3 |
| Parc Saint-Yves ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 3 |
| Parc des Primevères ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 3 |
| Parc du Plateau ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 3 |
| Parc de Québec (35) ⚠️ | Québec › Les Rivières | 3 |
| Parc des Brumes ⚠️ | Québec › Les Rivières | 3 |
| Parc Victorin-Beaucage ⚠️ | Québec › Les Rivières | 3 |
| Parc de la Grande-Oasis ⚠️ | Québec › La Haute-Saint-Charles | 3 |
| Parc Bon-Pasteur ⚠️ | Québec › Charlesbourg | 3 |
| Parc Saint-Denys ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 3 |
| Parc Gilles-Lamontagne ⚠️ | Québec › La Cité-Limoilou | 3 |
| Parc de la Colline ⚠️ | Québec › Les Rivières | 2 |
| Parc de l'Apprenti-Sage ⚠️ | Québec › Les Rivières | 2 |
| Parc des Braves ⚠️ | Québec › La Cité-Limoilou | 2 |
| Parc Dollard-Des-Ormeaux ⚠️ | Québec › La Cité-Limoilou | 2 |
| Parc Savio ⚠️ | Québec › Beauport | 2 |
| Parc de l'Échouerie ⚠️ | Québec › Beauport | 2 |
| Parc Saint-Sacrement ⚠️ | Québec › La Cité-Limoilou | 2 |
| Parc Jules Émond ⚠️ | Québec › La Haute-Saint-Charles | 2 |
| Parc Raymond-De Rosa ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 2 |
| Parc des Verveines ⚠️ | Québec › Charlesbourg | 2 |
| Parc du Bastion-de-la-Reine ⚠️ | Québec › La Cité-Limoilou | 2 |
| Parc de Québec (31) ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 2 |
| Parc Saint-Jean-Baptiste de La Salle ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 2 |
| Parc du Verger ⚠️ | Saint-Augustin-de-Desmaures | 2 |
| Parc de Champigny ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 2 |
| Parc Kiwanis ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 2 |
| Parc Saint-Mathieu ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 2 |
| Parc de Québec (33) ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 2 |
| Parc Antoine-Masson ⚠️ | Québec › Les Rivières | 2 |
| Parc du Marais ⚠️ | Québec › Les Rivières | 2 |
| Parc Jean-Marie Beaulieu ⚠️ | Québec › La Haute-Saint-Charles | 2 |
| Parc Véga ⚠️ | Québec › La Haute-Saint-Charles | 2 |
| Parc Le Bivouac ⚠️ | Saint-Augustin-de-Desmaures | 2 |
| Parc Guillaume-Mathieu (2) ⚠️ | Québec › Charlesbourg | 2 |
| Parc du Petit-Village ⚠️ | Québec › Beauport | 2 |
| Parc Fargy ⚠️ | Québec › Beauport | 2 |
| Parc Maurice-Dorion ⚠️ | Québec › Charlesbourg | 2 |
| Parc de l’Oise ⚠️ | Québec › Charlesbourg | 2 |
| Parc Maurice-Lortie ⚠️ | Québec › Charlesbourg | 2 |
| Parc de la Ribambelle ⚠️ | Québec › Beauport | 2 |
| Parc Cambert ⚠️ | Québec › Beauport | 2 |
| Parc des Eaux-Fraîches ⚠️ | Québec › La Haute-Saint-Charles | 2 |
| Parc Bourg-Royal ⚠️ | Québec › Charlesbourg | 2 |
| Parc Gaby-Pléau ⚠️ | Québec › La Haute-Saint-Charles | 2 |
| Parc aux Quatre-Vents ⚠️ | Québec › La Haute-Saint-Charles | 2 |
| Parc de la Chanterelle ⚠️ | Québec › La Haute-Saint-Charles | 2 |
| Parc de la Chaudière ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 2 |
| Parc de la Belle-Eau ⚠️ | Québec › La Haute-Saint-Charles | 2 |
| Parc Étienne-Parent ⚠️ | Québec › Beauport | 2 |
| Parc Réal-Cloutier ⚠️ | Québec › La Haute-Saint-Charles | 1 |
| Parc de la Joie-de-Vivre ⚠️ | Québec › La Haute-Saint-Charles | 1 |
| Parc Robert-Légaré ⚠️ | Québec › Les Rivières | 1 |
| Parc de Québec (4) ⚠️ | Québec › La Haute-Saint-Charles | 1 |
| Parc de l'Artillerie ⚠️ | Québec › La Cité-Limoilou | 1 |
| Parc de Québec (5) ⚠️ | Québec › La Haute-Saint-Charles | 1 |
| Parc Notre-Dame de la Garde ⚠️ | Québec › La Cité-Limoilou | 1 |
| Parc de Québec (10) ⚠️ | Québec › La Cité-Limoilou | 1 |
| Place des Canotiers ⚠️ | Québec › La Cité-Limoilou | 1 |
| Parc du Cachemire ⚠️ | Québec › La Haute-Saint-Charles | 1 |
| Parc du Millénaire ⚠️ | Saint-Augustin-de-Desmaures | 1 |
| Parc Saint-Michel ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| Parc Noël-Langlois ⚠️ | Québec › Beauport | 1 |
| Parc Expo-Cité ⚠️ | Québec › La Cité-Limoilou | 1 |
| Parc de Québec (16) ⚠️ | Québec › Beauport | 1 |
| Parc Saint-Ignace ⚠️ | Québec › Beauport | 1 |
| Parc Chevalier ⚠️ | Québec › Beauport | 1 |
| Parc Vachon ⚠️ | Québec › Beauport | 1 |
| Parc Sainte-Anne ⚠️ | Québec › La Haute-Saint-Charles | 1 |
| Parc des Écores ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| Parc de Bélair ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| Parc Notre-Dame de Foy ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| Parc Clérin ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| Parc Saint-Raphaël ⚠️ | Québec › La Haute-Saint-Charles | 1 |
| Parc Maria-Goretti ⚠️ | Québec › Charlesbourg | 1 |
| Parc de l'Orme ⚠️ | Québec › La Haute-Saint-Charles | 1 |
| Parc Ross ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| Parc Louis-Latulippe ⚠️ | Québec › Les Rivières | 1 |
| Parc de Québec (17) ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| Parc Sainte-Geneviève ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| Parc Chauray ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| Parc du Lyonnais ⚠️ | Québec › Charlesbourg | 1 |
| Parc de la Meule ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| Parc Paul-Émile-Beaulieu ⚠️ | Québec › La Haute-Saint-Charles | 1 |
| Parc de Québec (19) ⚠️ | Québec › Charlesbourg | 1 |
| Parc de Québec (20) ⚠️ | Québec › Charlesbourg | 1 |
| Parc Saint-Pierre ⚠️ | Québec › Charlesbourg | 1 |
| Parc Chabot ⚠️ | Québec › Charlesbourg | 1 |
| Jardins de l'hôtel de ville ⚠️ | Québec › La Cité-Limoilou | 1 |
| Parc de l'Esplanade ⚠️ | Québec › La Cité-Limoilou | 1 |
| Parc de Québec (24) ⚠️ | Québec › La Cité-Limoilou | 1 |
| Parc de la Francophonie ⚠️ | Québec › La Cité-Limoilou | 1 |
| Parc de Québec (27) ⚠️ | Québec › La Haute-Saint-Charles | 1 |
| Parc de Québec (29) ⚠️ | Québec › La Cité-Limoilou | 1 |
| Parc des Bernaches ⚠️ | Saint-Augustin-de-Desmaures | 1 |
| Parc Senneterre ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| Parc de Québec (32) ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| Parc Jean-Roger Durand ⚠️ | Québec › La Haute-Saint-Charles | 1 |
| Parc Anet-Gomin ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| Parc Saint-François-Xavier ⚠️ | Québec › Les Rivières | 1 |
| Parc du Père-Frédéric ⚠️ | Québec › Les Rivières | 1 |
| Parc de la Petite-Rivière ⚠️ | Québec › Les Rivières | 1 |
| Place de la Famille ⚠️ | L'Ancienne-Lorette | 1 |
| Parc des Hauts Clochers ⚠️ | L'Ancienne-Lorette | 1 |
| Parc de la Fenaison ⚠️ | Québec › Beauport | 1 |
| Parc Saint-Luc ⚠️ | Québec › La Haute-Saint-Charles | 1 |
| Parc des Seigneuries ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| Parc du Bon Pasteur ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| Parc Guillaume-Mathieu ⚠️ | Québec › Charlesbourg | 1 |
| Parc Gérard-Marchand ⚠️ | Québec › La Cité-Limoilou | 1 |
| Parc Lockwell ⚠️ | Québec › La Cité-Limoilou | 1 |
| Parc Saint-Benoît ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| Parc de Norvège ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| Parc de Québec (34) ⚠️ | Québec › La Cité-Limoilou | 1 |
| Parc Montpellier ⚠️ | Québec › Beauport | 1 |
| Parc de la Commune ⚠️ | Québec › Charlesbourg | 1 |
| Parc de Québec (36) ⚠️ | Québec › Les Rivières | 1 |
| Parc des Franciscains ⚠️ | Québec › La Cité-Limoilou | 1 |
| Parc de Québec (37) ⚠️ | Québec › Beauport | 1 |
| Parc Saint-Matthew ⚠️ | Québec › La Cité-Limoilou | 1 |
| Parc du Bois-Enchanté ⚠️ | Québec › La Haute-Saint-Charles | 1 |
| Réserve naturelle de l’Échappée-Belle ⚠️ | Québec › La Haute-Saint-Charles | 1 |
| Centre de glisse Myrand ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| parc Joseph-Giffard ⚠️ | Québec › Beauport | 1 |
| Bassin de l'Opale ⚠️ | Québec › Charlesbourg | 1 |
| Parc du Millénaire (2) ⚠️ | Québec › La Haute-Saint-Charles | 1 |
| Parc de Chantelle ⚠️ | Québec › Charlesbourg | 1 |
| Parc Jean Guyon ⚠️ | Québec › Beauport | 1 |
| Parc des Émereaudes ⚠️ | Québec › Charlesbourg | 1 |
| Parc de Mexico ⚠️ | Québec › Les Rivières | 1 |
| Parc de Québec (45) ⚠️ | Québec › La Haute-Saint-Charles | 1 |
| Parc Denise-Pelletier ⚠️ | Québec › La Haute-Saint-Charles | 1 |
| Parc Marguerite-Bourgeoys ⚠️ | Québec › La Haute-Saint-Charles | 1 |
| Parc des Capucins ⚠️ | Québec › La Haute-Saint-Charles | 1 |
| Parc Joseph-Tardif ⚠️ | Québec › Les Rivières | 1 |
| Parc Destor ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| Parc Bibiane-Robitaille ⚠️ | Québec › Les Rivières | 1 |
| Parc Richard Gosselin ⚠️ | Saint-Augustin-de-Desmaures | 1 |
| Parc Alain ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| Parc Noirefontaine ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| École Saint-Paul-Apôtre ⚠️ | Québec › La Cité-Limoilou | 1 |
| Parc Groenland ⚠️ | Québec › La Haute-Saint-Charles | 1 |
| Parc de Québec (63) ⚠️ | Québec › Les Rivières | 1 |
| Parc de Québec (66) ⚠️ | Québec › Les Rivières | 1 |
| Parc du Petit-Bois (2) ⚠️ | Québec › Les Rivières | 1 |
| Parc Sainte-Odile ⚠️ | Québec › La Cité-Limoilou | 1 |
| Parc de la Pommeraie ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| Parc Provancher ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| Parc des Compagnons ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| Parc Bégon ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| Parc Antoine-Martin ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| Parc des Meuniers ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| Parc de Québec (78) ⚠️ | Québec › La Haute-Saint-Charles | 1 |
| Parc de Québec (79) ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| Parc de Québec (80) ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| Sainte Famille ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| Parc Sainte-Monique ⚠️ | Québec › Les Rivières | 1 |
| Parc Sainte-Isabelle ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| Parc de Québec (85) ⚠️ | Québec › Charlesbourg | 1 |
| Parc de l'Ancienne-Lorette (4) ⚠️ | L'Ancienne-Lorette | 1 |
| Parc de la Futaie ⚠️ | Saint-Augustin-de-Desmaures | 1 |
| Parc Malraux ⚠️ | Québec › Sainte-Foy–Sillery–Cap-Rouge | 1 |
| Parc de Québec (86) ⚠️ | Québec › La Cité-Limoilou | 1 |
| Parc de la Comtoise ⚠️ | Québec › Les Rivières | 1 |
| Parc du Musée ⚠️ | Québec › La Cité-Limoilou | 1 |
| Parc du Boisé-Saint-Félix ⚠️ | Saint-Augustin-de-Desmaures | 1 |
| Parc de Beaumont ⚠️ | Québec › Les Rivières | 1 |
| Sentier Place Montaigne ⚠️ | Québec › Charlesbourg | 1 |
| Parc de Québec (88) ⚠️ | Québec › Les Rivières | 1 |
| Parc ibert ⚠️ | Québec › Les Rivières | 1 |
| Parc naturel du Marais-Bellevue ⚠️ | Québec › La Haute-Saint-Charles | 1 |
| Parc Éden ⚠️ | Québec › La Haute-Saint-Charles | 1 |
| Parc d'Évora ⚠️ | Québec › Les Rivières | 1 |
| Parc Ferland ⚠️ | Québec › La Cité-Limoilou | 1 |
| Parc Langelier (2) ⚠️ | Québec › La Cité-Limoilou | 1 |
| Parc D'Iberville ⚠️ | Québec › La Cité-Limoilou | 1 |
| Parc de l'Amérique-Latine ⚠️ | Québec › La Cité-Limoilou | 1 |
| Jardin Jean-Paul-L'Allier ⚠️ | Québec › La Cité-Limoilou | 1 |
| Parc Place Portneuf ⚠️ | Saint-Augustin-de-Desmaures | 1 |
| Parc de la côte Sauvageau ⚠️ | Québec › La Cité-Limoilou | 1 |

257 parc(s) plus petits qu'une cellule ne sont pas listés : la carte les dessine, mais ils n'offrent aucune cellule.

⚠️ 463 parc(s) hors de la fenêtre 10–125 cellules (462 trop petit(s), 1 trop grand(s)) : affichés sur la carte, mais ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| military | 497 |
| airport | 286 |
| prison | 9 |
| **Total déclaré** | **792** |
| dont dans une zone de ce territoire | 792 |


### Zones concernées

| Zone | Cellules exclues |
|---|---:|
| Québec | 792 |
| La Haute-Saint-Charles | 497 |
| Sainte-Foy–Sillery–Cap-Rouge | 286 |
| La Cité-Limoilou | 8 |
| Charlesbourg | 1 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
