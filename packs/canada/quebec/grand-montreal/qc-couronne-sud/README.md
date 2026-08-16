# Couronne Sud (Montérégie)

Pack `qc-couronne-sud` · version 1.2.1 · grille 200 m · Canada › Québec › Grand Montréal

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 62 493 |
| dont restreintes (aéroport, militaire, prison) | 160 |
| Cellules retirées par le masque d'eau | 2 064 |
| Villes | 30 |
| Arrondissements et quartiers | 0 |
| Îles | 0 |
| Parcs | 587 |

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

## Villes (30)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Parcs |
|---|---:|---:|---:|---:|---:|---:|
| Varennes | 4 852 | 53 | 4 799 | 0 | **4 799** | 22 |
| Verchères | 3 725 | 0 | 3 725 | 0 | **3 725** | 10 |
| Saint-Jean-Baptiste | 3 702 | 17 | 3 685 | 0 | **3 685** | 4 |
| Beauharnois | 3 422 | 5 | 3 417 | 0 | **3 417** | 20 |
| Contrecœur | 3 345 | 2 | 3 343 | 0 | **3 343** | 23 |
| Carignan | 3 168 | 0 | 3 168 | 0 | **3 168** | 23 |
| Saint-Philippe | 3 127 | 0 | 3 127 | 0 | **3 127** | 6 |
| Saint-Constant | 2 881 | 2 | 2 879 | 0 | **2 879** | 29 |
| Saint-Isidore | 2 631 | 0 | 2 631 | 0 | **2 631** | 5 |
| Kahnawake | 3 136 | 611 | 2 525 | 0 | **2 525** | 12 |
| Sainte-Julie | 2 446 | 0 | 2 446 | 126 | **2 320** | 35 |
| Saint-Mathias-sur-Richelieu | 2 409 | 0 | 2 409 | 5 | **2 404** | 4 |
| Mercier | 2 323 | 5 | 2 318 | 0 | **2 318** | 9 |
| La Prairie | 2 225 | 1 | 2 224 | 0 | **2 224** | 39 |
| Mont-Saint-Hilaire | 2 243 | 19 | 2 224 | 0 | **2 224** | 27 |
| Saint-Mathieu-de-Beloeil | 2 011 | 0 | 2 011 | 15 | **1 996** | 5 |
| Saint-Amable | 1 884 | 0 | 1 884 | 0 | **1 884** | 18 |
| Saint-Basile-le-Grand | 1 834 | 0 | 1 834 | 14 | **1 820** | 24 |
| Châteauguay | 2 848 | 1 033 | 1 815 | 0 | **1 815** | 63 |
| Calixa-Lavallée | 1 683 | 0 | 1 683 | 0 | **1 683** | 2 |
| Saint-Mathieu | 1 590 | 0 | 1 590 | 0 | **1 590** | 4 |
| Richelieu | 1 572 | 0 | 1 572 | 0 | **1 572** | 9 |
| Chambly | 1 261 | 0 | 1 261 | 0 | **1 261** | 48 |
| Beloeil | 1 237 | 0 | 1 237 | 0 | **1 237** | 52 |
| Candiac | 977 | 100 | 877 | 0 | **877** | 22 |
| Léry | 518 | 0 | 518 | 0 | **518** | 5 |
| Sainte-Catherine | 693 | 216 | 477 | 0 | **477** | 25 |
| Delson | 389 | 0 | 389 | 0 | **389** | 14 |
| Otterburn Park | 269 | 0 | 269 | 0 | **269** | 14 |
| McMasterville | 156 | 0 | 156 | 0 | **156** | 8 |

## Parcs (587)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Réserve Naturelle Gault ⚠️ | Mont-Saint-Hilaire | 494 |
| Réserve naturelle du Bois-de-Brossard | La Prairie | 119 |
| Refuge faunique Marguerite d'Youville | Châteauguay | 95 |
| Parc régional des Grêves - Secteur de la Colonie des Grèves de Contrecoeur | Contrecœur | 80 |
| Refuge d'oiseaux migrateurs de l'Île-aux-Hérons | Sainte-Catherine | 75 |
| Parc Le Rocher | Saint-Amable | 58 |
| Centre ecologique Fernand-Seguin | Châteauguay | 47 |
| Parc régional des Grèves | Contrecœur | 47 |
| Réserve naturelle du Piémont-du-Mont-Saint-Hilaire | Mont-Saint-Hilaire | 41 |
| Bois Robert | Beauharnois | 33 |
| Récré-O-Parc de Sainte-Catherine | Sainte-Catherine | 27 |
| Parc naturel des Ruisseaux | Chambly | 27 |
| Parc des Étangs Antoine-Charlebois | Sainte-Julie | 24 |
| Parc Saint-Charles (4) | Varennes | 22 |
| Parc de conservation Barbe-Denys-De La Trinité | Contrecœur | 22 |
| Parc multifonctionnel | Saint-Constant | 22 |
| Réserve naturelle du Ruisseau-Robert | Carignan | 20 |
| Parc Saint-Charles (5) | Varennes | 12 |
| Parc des Écluses | Beauharnois | 10 |
| Parc Champlain (5) ⚠️ | Candiac | 8 |
| Parc Lucie-F.-Roussel ⚠️ | La Prairie | 7 |
| Parc Robert-Lebel ⚠️ | Chambly | 7 |
| Parc de la Commune ⚠️ | Châteauguay | 6 |
| Parc de la Commune (2) ⚠️ | Varennes | 6 |
| Parc de la Commune (5) ⚠️ | Varennes | 6 |
| Parc Armand-Frappier ⚠️ | Sainte-Julie | 6 |
| Parc du Pré-Vert ⚠️ | Varennes | 5 |
| Parc Lorne-Worsley ⚠️ | Beloeil | 5 |
| Parc Émilie-Gamelin (2) ⚠️ | La Prairie | 5 |
| Parc Roger-Bélisle ⚠️ | Saint-Mathias-sur-Richelieu | 5 |
| Recreation Park ⚠️ | Kahnawake | 5 |
| Parc Saint-François-Xavier ⚠️ | Candiac | 5 |
| Parc du Ruisseau (7) ⚠️ | Saint-Basile-le-Grand | 5 |
| Parc de Chambly (5) ⚠️ | Chambly | 5 |
| Parc des Patriotes (5) ⚠️ | Chambly | 5 |
| Parc Edmour-J.-Harvey ⚠️ | Sainte-Julie | 5 |
| Parc du Bassin de La Prairie ⚠️ | La Prairie | 4 |
| Billings ⚠️ | Châteauguay | 4 |
| Parc du Carrousel ⚠️ | Varennes | 4 |
| Parc Antoine-Pécaudy ⚠️ | Contrecœur | 4 |
| Parc de Beauharnois ⚠️ | Beauharnois | 4 |
| Parc des Goélands ⚠️ | La Prairie | 4 |
| Parc Fleur-de-Lys ⚠️ | Sainte-Catherine | 4 |
| Parc des Pionniers ⚠️ | Verchères | 4 |
| Parc Chevaliers de Colomb ⚠️ | Sainte-Catherine | 4 |
| Aire de conservation ⚠️ | Mont-Saint-Hilaire | 4 |
| Réserve naturelle du Boisé-Virginia ⚠️ | Beauharnois | 4 |
| Parc de la Coulée (3) ⚠️ | Sainte-Julie | 4 |
| Parc Desrochers ⚠️ | Sainte-Julie | 4 |
| Parc André-J.-Côté ⚠️ | Candiac | 3 |
| Parc Gilles Plante ⚠️ | McMasterville | 3 |
| Parc du Portageur ⚠️ | Varennes | 3 |
| Parc Jules-Choquet ⚠️ | Sainte-Julie | 3 |
| Parc des Loisirs (2) ⚠️ | Saint-Jean-Baptiste | 3 |
| Fort-Chambly ⚠️ | Chambly | 3 |
| Parc du Tisserand ⚠️ | Chambly | 3 |
| Parc Multisportif Ozias-Leduc ⚠️ | Mont-Saint-Hilaire | 3 |
| Parc N.-P.-Lapierre ⚠️ | Sainte-Julie | 3 |
| Parc des Tuleries ⚠️ | Sainte-Julie | 3 |
| Parc du Petit Bonheur ⚠️ | Saint-Constant | 3 |
| Parc des Éperviers (2) ⚠️ | Sainte-Catherine | 3 |
| Parc Deauville ⚠️ | Candiac | 3 |
| Parc Honoré-Mercier ⚠️ | Châteauguay | 3 |
| Parc du Centenaire (3) ⚠️ | Delson | 3 |
| Parc Lafarge ⚠️ | Saint-Constant | 3 |
| Halte Au Fil de l'Eau ⚠️ | Beauharnois | 3 |
| Parc de Mercier (2) ⚠️ | Mercier | 2 |
| Parc Boardman ⚠️ | Delson | 2 |
| Parc du Vallon ⚠️ | Varennes | 2 |
| Parc des Trinitaires ⚠️ | Saint-Basile-le-Grand | 2 |
| Parc de la Seigneurie (2) ⚠️ | Saint-Basile-le-Grand | 2 |
| Parc François-Williams ⚠️ | Saint-Amable | 2 |
| Parc Sharron ⚠️ | Otterburn Park | 2 |
| Parc Gérard-Laframboise ⚠️ | Saint-Philippe | 2 |
| Parc Scheffer ⚠️ | Chambly | 2 |
| Parc Laurent-Blanchard ⚠️ | Chambly | 2 |
| Parc Florence-Viens ⚠️ | Richelieu | 2 |
| Parc des Jardins ⚠️ | Saint-Constant | 2 |
| Parc Leblanc ⚠️ | Saint-Constant | 2 |
| Parc Arthur-Trudeau ⚠️ | Delson | 2 |
| Parc de La Tortue ⚠️ | Delson | 2 |
| Parc de la Voie Maritimne ⚠️ | Sainte-Catherine | 2 |
| Parc de Saint-Constant ⚠️ | Saint-Constant | 2 |
| Parc de la Mairie (2) ⚠️ | Carignan | 2 |
| Parc des Citoyens ⚠️ | Saint-Constant | 2 |
| Parc de Mont-Saint-Hilaire (7) ⚠️ | Mont-Saint-Hilaire | 2 |
| Parc du Petit-Rapide ⚠️ | Beloeil | 2 |
| Parc Aurèle-Dubois ⚠️ | Beloeil | 2 |
| Parc de McMasterville (2) ⚠️ | McMasterville | 2 |
| Parc du Ruisseau-Bernard ⚠️ | McMasterville | 2 |
| Parc Bissonnette ⚠️ | Beauharnois | 2 |
| Parc de la Coulée François-Jarret ⚠️ | Verchères | 2 |
| Parc Haendel (2) ⚠️ | Candiac | 2 |
| Centre Municipal ⚠️ | Saint-Constant | 2 |
| Parc de Sardaigne ⚠️ | Candiac | 2 |
| Parc d'Auteuil - Espace vert Gravel-Guérin ⚠️ | Sainte-Catherine | 2 |
| Parc du centre culturel Claude Hébert ⚠️ | Saint-Constant | 2 |
| Parc de Montpellier (2) ⚠️ | Saint-Basile-le-Grand | 2 |
| Parc du Moulin (2) ⚠️ | Sainte-Julie | 2 |
| Parc de Mont-Saint-Hilaire (9) ⚠️ | Mont-Saint-Hilaire | 2 |
| Parc des Scouts ⚠️ | Varennes | 2 |
| Parc de La Prairie (2) ⚠️ | La Prairie | 2 |
| Parc Fernand-Séguin ⚠️ | Candiac | 2 |
| Parc Yvan-Franco ⚠️ | Châteauguay | 2 |
| Parc Oliver ⚠️ | Châteauguay | 2 |
| Parc de Châteauguay (11) ⚠️ | Châteauguay | 2 |
| Parc Philippe-Bonneau ⚠️ | Châteauguay | 2 |
| Parc Josaphat-Pitre ⚠️ | Châteauguay | 1 |
| Parc de Mercier ⚠️ | Mercier | 1 |
| Parc Jules-Léger ⚠️ | Châteauguay | 1 |
| Parc Garand ⚠️ | Châteauguay | 1 |
| Parc Vincent ⚠️ | Châteauguay | 1 |
| Parc des Acadiens ⚠️ | Châteauguay | 1 |
| Parc Sutterlin ⚠️ | Châteauguay | 1 |
| Des Sorbiers ⚠️ | Mercier | 1 |
| Parc de La Prairie ⚠️ | La Prairie | 1 |
| Parc des Véterans ⚠️ | Carignan | 1 |
| Parc Léo-Rouillier ⚠️ | La Prairie | 1 |
| Parc de Châteauguay ⚠️ | Châteauguay | 1 |
| Parc de Châteauguay (3) ⚠️ | Châteauguay | 1 |
| Park Langlois ⚠️ | Châteauguay | 1 |
| Parc Pierre-Raffeix ⚠️ | La Prairie | 1 |
| Parc du Rempart ⚠️ | La Prairie | 1 |
| Parc Pierre-Boucher ⚠️ | Varennes | 1 |
| Parc des Ancêtres ⚠️ | Varennes | 1 |
| Parc Georges-Pépin ⚠️ | Chambly | 1 |
| Parc Noël Lareau ⚠️ | Chambly | 1 |
| Parc Duvernay ⚠️ | Chambly | 1 |
| Parc Ringuet ⚠️ | Sainte-Julie | 1 |
| Parc de l'Érablière ⚠️ | Sainte-Julie | 1 |
| Parc Arthur Gauthier ⚠️ | Sainte-Julie | 1 |
| Parc du Pont-de-Pruche ⚠️ | Saint-Basile-le-Grand | 1 |
| Parc des Cheminots ⚠️ | Saint-Basile-le-Grand | 1 |
| Parc-école Marie-Victorin ⚠️ | Varennes | 1 |
| Parc Bel-Air ⚠️ | Saint-Amable | 1 |
| Parc Albine-Gadbois ⚠️ | Beloeil | 1 |
| Parc Helen ⚠️ | Otterburn Park | 1 |
| Centre sportif Edmond-Auclair ⚠️ | Otterburn Park | 1 |
| Parc Duncan-Campbell ⚠️ | Otterburn Park | 1 |
| Parc de Mont-Saint-Hilaire (2) ⚠️ | Mont-Saint-Hilaire | 1 |
| Parc Champlain (2) ⚠️ | Mont-Saint-Hilaire | 1 |
| Parc Jean-Baptiste Allard ⚠️ | Beloeil | 1 |
| Boisé dans les Bourgs de la Capital ⚠️ | Beloeil | 1 |
| Parc de la Baronne ⚠️ | Beloeil | 1 |
| Parc des Loisirs ⚠️ | Saint-Mathieu-de-Beloeil | 1 |
| Parc de Mont-Saint-Hilaire (3) ⚠️ | Mont-Saint-Hilaire | 1 |
| Parc de la Petite-Patrie ⚠️ | Varennes | 1 |
| Parc Ki-Ri ⚠️ | Varennes | 1 |
| Parc Jean-Marie Moreau ⚠️ | Verchères | 1 |
| Parc Cartier-Richard ⚠️ | Contrecœur | 1 |
| Parc Optimiste-Paul-Godin ⚠️ | La Prairie | 1 |
| Parc Gilles-Villeneuve ⚠️ | Chambly | 1 |
| Parc du Domaine ⚠️ | Carignan | 1 |
| Parc Bourcier ⚠️ | Beauharnois | 1 |
| Parc Roméo-Bourcier ⚠️ | Châteauguay | 1 |
| Parc de Concord ⚠️ | Châteauguay | 1 |
| Parc Joseph-Laberge ⚠️ | Châteauguay | 1 |
| Parc Jean-de-la-Mennais ⚠️ | La Prairie | 1 |
| Parc du Frère Ulysse-Baron ⚠️ | La Prairie | 1 |
| Parc Le gaspésien ⚠️ | Saint-Constant | 1 |
| Parc de Mercier (3) ⚠️ | Mercier | 1 |
| Parc de Saint-Isidore ⚠️ | Saint-Isidore | 1 |
| Parc des Hirondelles (3) ⚠️ | Mercier | 1 |
| Parc Montcalm (3) ⚠️ | Candiac | 1 |
| Parc Roméo-V.-Patenaude ⚠️ | Candiac | 1 |
| Parc de Vienne ⚠️ | Sainte-Julie | 1 |
| Parc du Bois-Franc ⚠️ | Sainte-Julie | 1 |
| Parc de Chambly ⚠️ | Chambly | 1 |
| Parc Joséphte-Chatelain ⚠️ | Chambly | 1 |
| Parc Breux ⚠️ | Chambly | 1 |
| Parc Albini Gemme ⚠️ | Saint-Amable | 1 |
| Parc de Saint-Basile-le-Grand (3) ⚠️ | Saint-Basile-le-Grand | 1 |
| Parc de la Gare (2) ⚠️ | Mont-Saint-Hilaire | 1 |
| Parc Georges-Étienne-Cartier ⚠️ | Châteauguay | 1 |
| Place Raymond-Laisné ⚠️ | Beloeil | 1 |
| Place Nicole-Tremblay ⚠️ | Beloeil | 1 |
| Parc Gédéon-Coursolles ⚠️ | Beloeil | 1 |
| Parc du Luxembourg ⚠️ | Sainte-Julie | 1 |
| Parc des Moussaillons ⚠️ | Varennes | 1 |
| Parc-école De La Source ⚠️ | Varennes | 1 |
| Parc de l'Arrondissement ⚠️ | La Prairie | 1 |
| Parc des Cèdres (3) ⚠️ | Beauharnois | 1 |
| Parc de la Commune (3) ⚠️ | Chambly | 1 |
| Parc Roland-Pigeon ⚠️ | Verchères | 1 |
| Parc Fortier ⚠️ | Richelieu | 1 |
| Parc de la Jemmerais ⚠️ | Beloeil | 1 |
| Parc Sainte-Anne (2) ⚠️ | Saint-Isidore | 1 |
| Parc Roussillon (2) ⚠️ | Saint-Constant | 1 |
| Parc Levasseur ⚠️ | Saint-Constant | 1 |
| Parc Montcalm (5) ⚠️ | Sainte-Catherine | 1 |
| Parc Miron ⚠️ | Delson | 1 |
| Parc Raymond-Pitre ⚠️ | Mercier | 1 |
| Parc Henriette ⚠️ | Carignan | 1 |
| Parc de Conservation Jeanne-Cartier ⚠️ | Contrecœur | 1 |
| Parc de La Rocque ⚠️ | Mont-Saint-Hilaire | 1 |
| Orville Standup Memorial Park ⚠️ | Kahnawake | 1 |
| Parc Copping ⚠️ | Otterburn Park | 1 |
| Parc de Otterburn Park ⚠️ | Otterburn Park | 1 |
| Parc Boileau ⚠️ | Chambly | 1 |
| Parc de Saint-Mathieu (3) ⚠️ | Saint-Mathieu | 1 |
| Parc Arthur Bouvier ⚠️ | Calixa-Lavallée | 1 |
| Parc Fréchette (2) ⚠️ | Mont-Saint-Hilaire | 1 |
| Parc des Ancêtres (3) ⚠️ | Saint-Constant | 1 |
| Parc d'Auteuil ⚠️ | Sainte-Catherine | 1 |
| Sentier Richelieu ⚠️ | La Prairie | 1 |
| Parc Magellan ⚠️ | Sainte-Catherine | 1 |
| Parc de La Prairie (3) ⚠️ | La Prairie | 1 |
| Parc MacDonald (2) ⚠️ | Beauharnois | 1 |
| Parc de Cherbourg ⚠️ | Candiac | 1 |
| Parc Picardie ⚠️ | Candiac | 1 |
| Parc Ovide-Asselin ⚠️ | Léry | 1 |
| Parc Ricard ⚠️ | Châteauguay | 1 |
| Parc Isabelle (2) ⚠️ | Châteauguay | 1 |
| Parc Albert-Einstein ⚠️ | Châteauguay | 1 |
| Parc de Châteauguay (14) ⚠️ | Châteauguay | 1 |
| Parc Chevrefils ⚠️ | Châteauguay | 1 |
| Parc Moïse-Prégent ⚠️ | Châteauguay | 1 |
| Parc Martineau (2) ⚠️ | Châteauguay | 1 |
| Parc de Saint-Mathias-sur-Richelieu (2) ⚠️ | Saint-Mathias-sur-Richelieu | 1 |
| Parc des Voiles ⚠️ | Saint-Mathias-sur-Richelieu | 1 |
| Parc du Verger-Tétreault ⚠️ | Otterburn Park | 1 |
| Parc Joseph-Véronneau ⚠️ | Sainte-Julie | 1 |
| Parc Jordi-Bonet ⚠️ | Sainte-Julie | 1 |
| Parc Adam ⚠️ | Chambly | 1 |
| Parc de Saint-Constant (7) ⚠️ | Saint-Constant | 1 |
| Parc de Ronsard ⚠️ | Saint-Constant | 1 |
| Parc de Beloeil (7) ⚠️ | Beloeil | 1 |
| Parc de Saint-Constant (8) ⚠️ | Saint-Constant | 1 |
| Parc des Peupliers (2) ⚠️ | Carignan | 1 |
| Parc Victor-Brillon ⚠️ | Beloeil | 1 |
| Parc de Candiac (5) ⚠️ | Candiac | 1 |
| Parc de Carignan (3) ⚠️ | Carignan | 1 |
| Parc Duclos ⚠️ | Otterburn Park | 1 |
| Parc de la Pointe-Valaine ⚠️ | Otterburn Park | 1 |
| Parc Clifton ⚠️ | Otterburn Park | 1 |
| Parc de l'Île-aux-Tortues ⚠️ | Beloeil | 1 |
| Marsh & Linear Pond ⚠️ | Kahnawake | 1 |
| Turtle Nesting Grounds ⚠️ | Kahnawake | 1 |
| Parc Louis-Philippe-Paré ⚠️ | Châteauguay | 1 |
| Parc les Marguerite ⚠️ | Varennes | 1 |
| Parc-école La Roseraie ⚠️ | Varennes | 1 |
| Parc-école de l'Envolée ⚠️ | Saint-Amable | 1 |
| Parc Comtois (2) ⚠️ | Sainte-Julie | 1 |
| Parc de Carignan (4) ⚠️ | Carignan | 1 |
| Parc de Carignan (5) ⚠️ | Carignan | 1 |
| Parc des Ateliers ⚠️ | Chambly | 1 |
| Parc de Chambly (8) ⚠️ | Chambly | 1 |
| Parc de la Chanterelle ⚠️ | Saint-Basile-le-Grand | 1 |
| Parc Optimiste (2) ⚠️ | Sainte-Catherine | 1 |
| Parc Fernand-Lapalme ⚠️ | Delson | 1 |
| Parc Thomas-Auguste-Brisson ⚠️ | La Prairie | 1 |
| Parc Georges-Soyez ⚠️ | Châteauguay | 1 |
| Parc Roger-Déziel ⚠️ | Châteauguay | 1 |
| Parc de Cambray ⚠️ | Châteauguay | 1 |
| Parc Marcel-Seers ⚠️ | Châteauguay | 1 |
| Espace vert Saint-Jean-Union ⚠️ | Sainte-Catherine | 1 |
| Parc des Rapides (2) ⚠️ | Chambly | 1 |
| Place du Centennaire ⚠️ | Beloeil | 1 |

329 parc(s) plus petits qu'une cellule ne sont pas listés : la carte les dessine, mais ils n'offrent aucune cellule.

⚠️ 569 parc(s) hors de la fenêtre 10–125 cellules (568 trop petit(s), 1 trop grand(s)) : affichés sur la carte, mais ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| military | 140 |
| airport | 20 |
| prison | 0 |
| **Total déclaré** | **160** |
| dont dans une zone de ce territoire | 160 |


### Zones concernées

| Zone | Cellules exclues |
|---|---:|
| Sainte-Julie | 126 |
| Saint-Mathieu-de-Beloeil | 15 |
| Saint-Basile-le-Grand | 14 |
| Saint-Mathias-sur-Richelieu | 5 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
