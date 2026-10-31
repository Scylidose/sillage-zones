# Hauts-de-Seine

Pack `fr-hauts-de-seine` · version 1.0.0 · grille 200 m · France › Île-de-France

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 9 848 |
| dont restreintes (aéroport, militaire, prison) | 42 |
| dont sans chemin (aucune voie à moins de 60 m) | 12 |
| dont en forêt, sans chemin non plus | 3 |
| dont traversées par un cours d'eau, sans chemin non plus | 0 |
| Cellules retirées par le masque d'eau | 292 |
| Villes | 36 |
| Arrondissements et quartiers | 0 |
| Îles | 4 |
| Parcs | 1 492 |

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
| Boucle Nord de Seine (Hauts-de-Seine) | 1 778 | somme de 6 villes |
| Grand Paris Seine Ouest | 2 033 | somme de 8 villes |
| Paris Ouest La Défense | 3 321 | somme de 11 villes |
| Vallée Sud Grand Paris | 2 717 | somme de 11 villes |

Une île *composite* n'a pas de cellules à elle : sa progression est la somme de ses villes, et ses cellules ne lui sont jamais rattachées directement — elles compteraient deux fois.

## Villes (36)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Sans chemin | Parcs |
|---|---:|---:|---:|---:|---:|---:|---:|
| Rueil-Malmaison | 838 | 11 | 827 | 0 | **827** | 2 (0 %) | 133 |
| Nanterre | 705 | 17 | 688 | 7 | **681** |  | 77 |
| Gennevilliers | 674 | 57 | 617 | 0 | **617** |  | 73 |
| Meudon | 569 | 9 | 560 | 8 | **552** |  | 75 |
| Antony | 550 | 4 | 546 | 0 | **546** |  | 72 |
| Clamart | 504 | 1 | 503 | 5 | **498** |  | 30 |
| Colombes | 455 | 15 | 440 | 0 | **440** |  | 60 |
| Saint-Cloud | 435 | 14 | 421 | 0 | **421** | 3 (1 %) | 99 |
| Châtenay-Malabry | 363 | 2 | 361 | 0 | **361** |  | 50 |
| Boulogne-Billancourt | 355 | 38 | 317 | 0 | **317** |  | 66 |
| Asnières-sur-Seine | 281 | 10 | 271 | 0 | **271** |  | 22 |
| Bagneux | 243 | 0 | 243 | 0 | **243** |  | 27 |
| Courbevoie | 242 | 10 | 232 | 0 | **232** |  | 54 |
| Issy-les-Moulineaux | 245 | 13 | 232 | 3 | **229** |  | 72 |
| Sèvres | 230 | 7 | 223 | 0 | **223** |  | 28 |
| Ville-d'Avray | 217 | 2 | 215 | 0 | **215** |  | 17 |
| Suresnes | 215 | 8 | 207 | 11 | **196** |  | 54 |
| Sceaux | 208 | 2 | 206 | 0 | **206** |  | 29 |
| Neuilly-sur-Seine | 216 | 13 | 203 | 0 | **203** |  | 26 |
| Chaville | 202 | 0 | 202 | 0 | **202** |  | 8 |
| Le Plessis-Robinson | 198 | 2 | 196 | 0 | **196** |  | 23 |
| Marnes-la-Coquette | 197 | 4 | 193 | 0 | **193** | 1 (1 %) | 21 |
| Vaucresson | 179 | 0 | 179 | 0 | **179** | 5 (3 %) | 44 |
| Villeneuve-la-Garenne | 185 | 11 | 174 | 0 | **174** |  | 48 |
| Châtillon | 171 | 0 | 171 | 0 | **171** | 1 (1 %) | 22 |
| Puteaux | 189 | 20 | 169 | 0 | **169** |  | 43 |
| Clichy | 180 | 14 | 166 | 0 | **166** |  | 31 |
| Garches | 161 | 0 | 161 | 0 | **161** |  | 10 |
| Fontenay-aux-Roses | 143 | 0 | 143 | 0 | **143** |  | 9 |
| Levallois-Perret | 138 | 7 | 131 | 0 | **131** |  | 24 |
| Montrouge | 122 | 0 | 122 | 0 | **122** |  | 40 |
| Malakoff | 119 | 0 | 119 | 8 | **111** |  | 21 |
| Bois-Colombes | 111 | 1 | 110 | 0 | **110** |  | 17 |
| Bourg-la-Reine | 107 | 0 | 107 | 0 | **107** |  | 7 |
| La Garenne-Colombes | 103 | 0 | 103 | 0 | **103** |  | 11 |
| Vanves | 91 | 0 | 91 | 0 | **91** |  | 34 |

## Parcs (1492)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Forêt domaniale de Meudon (2) ⚠️ | Meudon › Grand Paris Seine Ouest | 451 |
| Forêt de Fausses-Reposes ⚠️ | Ville-d'Avray › Grand Paris Seine Ouest | 224 |
| Domaine national de Saint-Cloud ⚠️ | Saint-Cloud › Paris Ouest La Défense | 202 |
| Forêt domaniale de la Malmaison | Rueil-Malmaison › Paris Ouest La Défense | 114 |
| Parc de Sceaux (3) | Sceaux › Vallée Sud Grand Paris | 93 |
| Forêt de Verrières (2) | Châtenay-Malabry › Vallée Sud Grand Paris | 58 |
| Parc des Chanteraines | Villeneuve-la-Garenne › Boucle Nord de Seine (Hauts-de-Seine) | 37 |
| Domaine Départemental de la Vallée-aux-Loups | Châtenay-Malabry › Vallée Sud Grand Paris | 35 |
| Forêt de Saint-Cloud (77) | Saint-Cloud › Paris Ouest La Défense | 32 |
| Bois de Clamart (3) | Clamart › Vallée Sud Grand Paris | 23 |
| Parc Boisé du Parc de la Vallée-aux-Loups | Châtenay-Malabry › Vallée Sud Grand Paris | 22 |
| Forêt de Châtenay-Malabry (17) | Châtenay-Malabry › Vallée Sud Grand Paris | 21 |
| Les Quatre-Cèdres | Marnes-la-Coquette › Grand Paris Seine Ouest | 19 |
| Parc Pierre-Lagravère | Colombes › Boucle Nord de Seine (Hauts-de-Seine) | 18 |
| Coulée verte du sud parisien | Antony › Vallée Sud Grand Paris | 18 |
| Parc Henri Sellier | Le Plessis-Robinson › Vallée Sud Grand Paris | 15 |
| Parc André Malraux | Nanterre › Paris Ouest La Défense | 13 |
| Forêt de Rueil-Malmaison (34) | Rueil-Malmaison › Paris Ouest La Défense | 13 |
| Forêt de Clamart (8) | Clamart › Vallée Sud Grand Paris | 12 |
| Parc de l'île Saint-Germain | Issy-les-Moulineaux › Grand Paris Seine Ouest | 11 |
| Le Bouquet de Verrières | Châtenay-Malabry › Vallée Sud Grand Paris | 10 |
| Parc du Chemin de l'île | Nanterre › Paris Ouest La Défense | 10 |
| Parc de Bois-Préau ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 9 |
| Forêt de Saint-Cloud (78) ⚠️ | Saint-Cloud › Paris Ouest La Défense | 9 |
| Bois de Clamart (4) ⚠️ | Clamart › Vallée Sud Grand Paris | 9 |
| Forêt de Clamart (7) ⚠️ | Clamart › Vallée Sud Grand Paris | 9 |
| Forêt de Sceaux ⚠️ | Sceaux › Vallée Sud Grand Paris | 8 |
| Forêt de Saint-Cloud (9) ⚠️ | Saint-Cloud › Paris Ouest La Défense | 8 |
| Forêt de Saint-Cloud (15) ⚠️ | Saint-Cloud › Paris Ouest La Défense | 8 |
| Parc Heller ⚠️ | Antony › Vallée Sud Grand Paris | 7 |
| Parc de Boulogne - Edmond de Rothschild ⚠️ | Boulogne-Billancourt › Grand Paris Seine Ouest | 7 |
| Parc des Sévines ⚠️ | Gennevilliers › Boucle Nord de Seine (Hauts-de-Seine) | 6 |
| Forêt de Saint-Cloud (7) ⚠️ | Saint-Cloud › Paris Ouest La Défense | 6 |
| Forêt de Saint-Cloud (8) ⚠️ | Saint-Cloud › Paris Ouest La Défense | 6 |
| Parc de Villeneuve l'Étang ⚠️ | Marnes-la-Coquette › Grand Paris Seine Ouest | 6 |
| Parc Naturel des Gallicourts ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 6 |
| Forêt de Saint-Cloud (80) ⚠️ | Saint-Cloud › Paris Ouest La Défense | 6 |
| Forêt de Sceaux (2) ⚠️ | Sceaux › Vallée Sud Grand Paris | 5 |
| Forêt de Sceaux (4) ⚠️ | Sceaux › Vallée Sud Grand Paris | 5 |
| Forêt de Sceaux (6) ⚠️ | Sceaux › Vallée Sud Grand Paris | 5 |
| Forêt de Saint-Cloud (5) ⚠️ | Saint-Cloud › Paris Ouest La Défense | 5 |
| Bois de la Garenne ⚠️ | Le Plessis-Robinson › Vallée Sud Grand Paris | 5 |
| Forêt de Saint-Cloud (79) ⚠️ | Saint-Cloud › Paris Ouest La Défense | 5 |
| Parc des Bords de Seine ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 4 |
| Parc Boisé ⚠️ | Châtenay-Malabry › Vallée Sud Grand Paris | 4 |
| Parc Leclerc ⚠️ | Villeneuve-la-Garenne › Boucle Nord de Seine (Hauts-de-Seine) | 4 |
| Parc Nautique de l'Île de Monsieur ⚠️ | Sèvres › Grand Paris Seine Ouest | 4 |
| Plaine des Closeaux ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 4 |
| Forêt de Saint-Cloud (24) ⚠️ | Saint-Cloud › Paris Ouest La Défense | 4 |
| Parc de Nanterre (9) ⚠️ | Nanterre › Paris Ouest La Défense | 4 |
| Parc de l'Observatoire ⚠️ | Meudon › Grand Paris Seine Ouest | 4 |
| Parc des étangs de Corot ⚠️ | Ville-d'Avray › Grand Paris Seine Ouest | 4 |
| Bois de Colombes (2) ⚠️ | Colombes › Boucle Nord de Seine (Hauts-de-Seine) | 4 |
| Forêt de Châtenay-Malabry (13) ⚠️ | Châtenay-Malabry › Vallée Sud Grand Paris | 4 |
| Parc de la Roseraie ⚠️ | Châtenay-Malabry › Vallée Sud Grand Paris | 4 |
| Forêt de Marnes-la-Coquette (14) ⚠️ | Marnes-la-Coquette › Grand Paris Seine Ouest | 4 |
| Parc Frédéric Pic ⚠️ | Vanves › Grand Paris Seine Ouest | 3 |
| Forêt de Antony ⚠️ | Antony › Vallée Sud Grand Paris | 3 |
| Parc du Château ⚠️ | Suresnes › Paris Ouest La Défense | 3 |
| promenade de la couverture de l'autoroute ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 3 |
| Forêt de Saint-Cloud (10) ⚠️ | Saint-Cloud › Paris Ouest La Défense | 3 |
| Parc des Impressionnistes (2) ⚠️ | Clichy › Boucle Nord de Seine (Hauts-de-Seine) | 3 |
| Parc Départemental des Chanteraines - Louvresses ⚠️ | Gennevilliers › Boucle Nord de Seine (Hauts-de-Seine) | 3 |
| Parc de Sèvres ⚠️ | Sèvres › Grand Paris Seine Ouest | 3 |
| Forêt de Saint-Cloud (14) ⚠️ | Saint-Cloud › Paris Ouest La Défense | 3 |
| Forêt de Saint-Cloud (16) ⚠️ | Saint-Cloud › Paris Ouest La Défense | 3 |
| Forêt de Saint-Cloud (25) ⚠️ | Saint-Cloud › Paris Ouest La Défense | 3 |
| Domaine national de la Malmaison ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 3 |
| Forêt de Garches (2) ⚠️ | Garches › Paris Ouest La Défense | 3 |
| Forêt de Gennevilliers (11) ⚠️ | Gennevilliers › Boucle Nord de Seine (Hauts-de-Seine) | 3 |
| Forêt de Rueil-Malmaison (29) ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 3 |
| Parc de Nanterre (10) ⚠️ | Nanterre › Paris Ouest La Défense | 3 |
| Bois de Sèvres (3) ⚠️ | Sèvres › Grand Paris Seine Ouest | 3 |
| Forêt de Sceaux (18) ⚠️ | Sceaux › Vallée Sud Grand Paris | 3 |
| Parc du Lycée Michelet ⚠️ | Vanves › Grand Paris Seine Ouest | 3 |
| Forêt de Rueil-Malmaison (33) ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 3 |
| Forêt de Suresnes (36) ⚠️ | Suresnes › Paris Ouest La Défense | 3 |
| Forêt de Châtenay-Malabry (19) ⚠️ | Châtenay-Malabry › Vallée Sud Grand Paris | 3 |
| Forêt de Rueil-Malmaison (35) ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 3 |
| Bois de Antony (18) ⚠️ | Antony › Vallée Sud Grand Paris | 3 |
| Parc de Suresnes ⚠️ | Suresnes › Paris Ouest La Défense | 2 |
| Parc Henri Barbusse ⚠️ | Issy-les-Moulineaux › Grand Paris Seine Ouest | 2 |
| Forêt de Sceaux (5) ⚠️ | Sceaux › Vallée Sud Grand Paris | 2 |
| Bois de Verrières ⚠️ | Clamart › Vallée Sud Grand Paris | 2 |
| Parc André Malraux (2) ⚠️ | Châtillon › Vallée Sud Grand Paris | 2 |
| Parc des Sports ⚠️ | Gennevilliers › Boucle Nord de Seine (Hauts-de-Seine) | 2 |
| Parc Robinson ⚠️ | Asnières-sur-Seine › Boucle Nord de Seine (Hauts-de-Seine) | 2 |
| Parc des Pleïades ⚠️ | Courbevoie › Paris Ouest La Défense | 2 |
| Jardin de la Ménagerie ⚠️ | Sceaux › Vallée Sud Grand Paris | 2 |
| Parc des Couronnes ⚠️ | Courbevoie › Paris Ouest La Défense | 2 |
| Parc de la Noisette ⚠️ | Antony › Vallée Sud Grand Paris | 2 |
| Forêt de Saint-Cloud (6) ⚠️ | Saint-Cloud › Paris Ouest La Défense | 2 |
| Parc Départemental des Chanteraines - Garennes ⚠️ | Villeneuve-la-Garenne › Boucle Nord de Seine (Hauts-de-Seine) | 2 |
| Parc Départemental des Chanteraines - Vallon de Seine ⚠️ | Gennevilliers › Boucle Nord de Seine (Hauts-de-Seine) | 2 |
| Promenade de la couverture de l'autoroute ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 2 |
| Jardin Albert Kahn ⚠️ | Boulogne-Billancourt › Grand Paris Seine Ouest | 2 |
| Forêt de Saint-Cloud (11) ⚠️ | Saint-Cloud › Paris Ouest La Défense | 2 |
| Forêt domaniale de Meudon ⚠️ | Sèvres › Grand Paris Seine Ouest | 2 |
| Parc forestier du Tronchet ⚠️ | Meudon › Grand Paris Seine Ouest | 2 |
| Forêt de Rueil-Malmaison (10) ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 2 |
| Forêt de Saint-Cloud (12) ⚠️ | Saint-Cloud › Paris Ouest La Défense | 2 |
| Forêt de Saint-Cloud (13) ⚠️ | Saint-Cloud › Paris Ouest La Défense | 2 |
| Plaine de la Sibérie (2) ⚠️ | Sceaux › Vallée Sud Grand Paris | 2 |
| Parc Paumier ⚠️ | Meudon › Grand Paris Seine Ouest | 2 |
| Bois de la Solitude ⚠️ | Le Plessis-Robinson › Vallée Sud Grand Paris | 2 |
| La coulée verte ⚠️ | Colombes › Boucle Nord de Seine (Hauts-de-Seine) | 2 |
| Parc Richelieu ⚠️ | Bagneux › Vallée Sud Grand Paris | 2 |
| Parc de Nanterre (3) ⚠️ | Nanterre › Paris Ouest La Défense | 2 |
| Parc de Rueil-Malmaison (10) ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 2 |
| Jardin des Tourneroches ⚠️ | Saint-Cloud › Paris Ouest La Défense | 2 |
| Domaine de Vert-Mont ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 2 |
| Forêt de Rueil-Malmaison (17) ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 2 |
| Parc François Mitterrand (2) ⚠️ | Bagneux › Vallée Sud Grand Paris | 2 |
| Parc Casimir Davaine ⚠️ | Garches › Paris Ouest La Défense | 2 |
| Bois de Sceaux ⚠️ | Sceaux › Vallée Sud Grand Paris | 2 |
| Forêt de Garches ⚠️ | Garches › Paris Ouest La Défense | 2 |
| Parc du Mont-Valérien ⚠️ | Suresnes › Paris Ouest La Défense | 2 |
| Parc de Châtenay-Malabry (2) ⚠️ | Châtenay-Malabry › Vallée Sud Grand Paris | 2 |
| Parc du Docteur Bazennerye ⚠️ | Ville-d'Avray › Grand Paris Seine Ouest | 2 |
| Forêt de Vaucresson (11) ⚠️ | Vaucresson › Paris Ouest La Défense | 2 |
| Bois de Châtenay-Malabry (8) ⚠️ | Châtenay-Malabry › Vallée Sud Grand Paris | 2 |
| Forêt de Antony (11) ⚠️ | Antony › Vallée Sud Grand Paris | 2 |
| Forêt de Villeneuve-la-Garenne (20) ⚠️ | Villeneuve-la-Garenne › Boucle Nord de Seine (Hauts-de-Seine) | 2 |
| Parc du Cardinal ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 2 |
| Forêt de Sceaux (14) ⚠️ | Sceaux › Vallée Sud Grand Paris | 2 |
| Forêt de Ville-d'Avray (3) ⚠️ | Ville-d'Avray › Grand Paris Seine Ouest | 2 |
| Le Petit Bois ⚠️ | Bagneux › Vallée Sud Grand Paris | 2 |
| Parc de Châtenay-Malabry (6) ⚠️ | Châtenay-Malabry › Vallée Sud Grand Paris | 2 |
| Parc de Meudon (9) ⚠️ | Meudon › Grand Paris Seine Ouest | 2 |
| Forêt du Plessis-Robinson ⚠️ | Le Plessis-Robinson › Vallée Sud Grand Paris | 2 |
| Bois de Sèvres (6) ⚠️ | Sèvres › Grand Paris Seine Ouest | 2 |
| Parc Rodin ⚠️ | Issy-les-Moulineaux › Grand Paris Seine Ouest | 1 |
| Parc de l'Île de la Jatte ⚠️ | Levallois-Perret › Paris Ouest La Défense | 1 |
| Forêt de Sceaux (3) ⚠️ | Sceaux › Vallée Sud Grand Paris | 1 |
| Forêt de Antony (2) ⚠️ | Antony › Vallée Sud Grand Paris | 1 |
| Parc des Bruyères ⚠️ | Bois-Colombes › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Parc de Clichy ⚠️ | Clichy › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Parc Départemental des Chanteraines - Les Mariniers ⚠️ | Gennevilliers › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Parc du Moulin ⚠️ | Puteaux › Paris Ouest La Défense | 1 |
| Parc Léon Salagnac ⚠️ | Malakoff › Vallée Sud Grand Paris | 1 |
| Parc Raymond Sibille Arboretum ⚠️ | Antony › Vallée Sud Grand Paris | 1 |
| Square Chaptal ⚠️ | Levallois-Perret › Paris Ouest La Défense | 1 |
| Parc Henri Matisse ⚠️ | Châtillon › Vallée Sud Grand Paris | 1 |
| Parc des Sarments ⚠️ | Châtillon › Vallée Sud Grand Paris | 1 |
| Potager du Dauphin ⚠️ | Meudon › Grand Paris Seine Ouest | 1 |
| Parc de la Planchette ⚠️ | Levallois-Perret › Paris Ouest La Défense | 1 |
| Parc de la Mairie ⚠️ | Garches › Paris Ouest La Défense | 1 |
| Parc Lebaudy ⚠️ | Puteaux › Paris Ouest La Défense | 1 |
| Parc Roger Salengro ⚠️ | Clichy › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Vergers de Buzenval ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 1 |
| Parc de la Maison Blanche ⚠️ | Clamart › Vallée Sud Grand Paris | 1 |
| Parc Chenard et Walcker ⚠️ | Gennevilliers › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Square Gabriel Fauré ⚠️ | Antony › Vallée Sud Grand Paris | 1 |
| Parc des Anciennes Mairies ⚠️ | Nanterre › Paris Ouest La Défense | 1 |
| Parc Offenbach ⚠️ | Puteaux › Paris Ouest La Défense | 1 |
| Parc Communal Caillebotte ⚠️ | Colombes › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Parc Diderot ⚠️ | Courbevoie › Paris Ouest La Défense | 1 |
| Forêt de Saint-Cloud (3) ⚠️ | Saint-Cloud › Paris Ouest La Défense | 1 |
| Jardin des Acacias ⚠️ | Nanterre › Paris Ouest La Défense | 1 |
| Prairie du Moulin Joly ⚠️ | Colombes › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Parc Théodore Monod ⚠️ | Clichy › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Terrasse du Fecheray ⚠️ | Suresnes › Paris Ouest La Défense | 1 |
| Coulée verte ⚠️ | Villeneuve-la-Garenne › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Forêt de Gennevilliers (2) ⚠️ | Gennevilliers › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Square Capitaine Dronne ⚠️ | Antony › Vallée Sud Grand Paris | 1 |
| Parc de Gennevilliers (2) ⚠️ | Gennevilliers › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Parc de Boulogne-Billancourt ⚠️ | Boulogne-Billancourt › Grand Paris Seine Ouest | 1 |
| Square André Meunier ⚠️ | Bourg-la-Reine › Vallée Sud Grand Paris | 1 |
| Parc des Tourelles ⚠️ | Bois-Colombes › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Parc de Billancourt ⚠️ | Boulogne-Billancourt › Grand Paris Seine Ouest | 1 |
| Solarium et pelouse de la piscine ⚠️ | Boulogne-Billancourt › Grand Paris Seine Ouest | 1 |
| Parc des Glacières ⚠️ | Boulogne-Billancourt › Grand Paris Seine Ouest | 1 |
| Square Silvain ⚠️ | Asnières-sur-Seine › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Mail du Maréchal Juin (2) ⚠️ | Boulogne-Billancourt › Grand Paris Seine Ouest | 1 |
| Jardin des serres d’Auteuil ⚠️ | Boulogne-Billancourt › Grand Paris Seine Ouest | 1 |
| Parc de la Folie Saint-James ⚠️ | Neuilly-sur-Seine › Paris Ouest La Défense | 1 |
| Square Guy Môquet ⚠️ | La Garenne-Colombes › Paris Ouest La Défense | 1 |
| Parc de Bécon ⚠️ | Courbevoie › Paris Ouest La Défense | 1 |
| Parc de la Résistance ⚠️ | Issy-les-Moulineaux › Grand Paris Seine Ouest | 1 |
| Jardin des Tournelles ⚠️ | Courbevoie › Paris Ouest La Défense | 1 |
| Parc de Antony ⚠️ | Antony › Vallée Sud Grand Paris | 1 |
| Square du Maréchal Joffre ⚠️ | Asnières-sur-Seine › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Bois de l'Aurore ⚠️ | Antony › Vallée Sud Grand Paris | 1 |
| Parc de Lesser ⚠️ | Ville-d'Avray › Grand Paris Seine Ouest | 1 |
| Jardin Japonais ⚠️ | Boulogne-Billancourt › Grand Paris Seine Ouest | 1 |
| Parc de Rueil-Malmaison ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 1 |
| Forêt de Rueil-Malmaison (3) ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 1 |
| Forêt de Rueil-Malmaison (7) ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 1 |
| Parc de Rueil-Malmaison (2) ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 1 |
| Forêt de Rueil-Malmaison (14) ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 1 |
| Parc Nelson Mandela ⚠️ | Courbevoie › Paris Ouest La Défense | 1 |
| Forêt de Saint-Cloud (18) ⚠️ | Saint-Cloud › Paris Ouest La Défense | 1 |
| Forêt de Saint-Cloud (19) ⚠️ | Saint-Cloud › Paris Ouest La Défense | 1 |
| Forêt de Saint-Cloud (20) ⚠️ | Saint-Cloud › Paris Ouest La Défense | 1 |
| Forêt de Saint-Cloud (22) ⚠️ | Saint-Cloud › Paris Ouest La Défense | 1 |
| Promenade des quatre forêts ⚠️ | Clamart › Vallée Sud Grand Paris | 1 |
| Jardin de la Roseraie ⚠️ | Montrouge › Vallée Sud Grand Paris | 1 |
| Parc Alsace ⚠️ | Levallois-Perret › Paris Ouest La Défense | 1 |
| Forêt de Nanterre (4) ⚠️ | Nanterre › Paris Ouest La Défense | 1 |
| Parc des Chenevreux ⚠️ | Nanterre › Paris Ouest La Défense | 1 |
| Parc de Nanterre (4) ⚠️ | Nanterre › Paris Ouest La Défense | 1 |
| Parc des Alisiers (2) ⚠️ | Antony › Vallée Sud Grand Paris | 1 |
| Parc de Suresnes (4) ⚠️ | Suresnes › Paris Ouest La Défense | 1 |
| Parc de l'Amitié ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 1 |
| Forêt de Bagneux ⚠️ | Bagneux › Vallée Sud Grand Paris | 1 |
| Parc Youri Gagarine ⚠️ | Levallois-Perret › Paris Ouest La Défense | 1 |
| Bois du Carreau ⚠️ | Châtenay-Malabry › Vallée Sud Grand Paris | 1 |
| Bois du Carreau (2) ⚠️ | Châtenay-Malabry › Vallée Sud Grand Paris | 1 |
| Forêt de Nanterre (19) ⚠️ | Nanterre › Paris Ouest La Défense | 1 |
| Square Eugène Varlin ⚠️ | Gennevilliers › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Park Nelson Mandela ⚠️ | Bagneux › Vallée Sud Grand Paris | 1 |
| Parc de Nanterre (5) ⚠️ | Nanterre › Paris Ouest La Défense | 1 |
| Parc de Clamart (2) ⚠️ | Clamart › Vallée Sud Grand Paris | 1 |
| Parc Marcel Bich ⚠️ | Clichy › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Parc Charles Lorilleux ⚠️ | Puteaux › Paris Ouest La Défense | 1 |
| Forêt de Antony (3) ⚠️ | Antony › Vallée Sud Grand Paris | 1 |
| Forêt de Sceaux (8) ⚠️ | Sceaux › Vallée Sud Grand Paris | 1 |
| Forêt de Antony (5) ⚠️ | Antony › Vallée Sud Grand Paris | 1 |
| Square Florence Arthaud ⚠️ | Colombes › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Forêt de Boulogne-Billancourt (2) ⚠️ | Boulogne-Billancourt › Grand Paris Seine Ouest | 1 |
| Square de l'Abbé Derry ⚠️ | Issy-les-Moulineaux › Grand Paris Seine Ouest | 1 |
| Forêt de Issy-les-Moulineaux (2) ⚠️ | Issy-les-Moulineaux › Grand Paris Seine Ouest | 1 |
| Forêt de Puteaux (2) ⚠️ | Puteaux › Paris Ouest La Défense | 1 |
| Parc de Malakoff ⚠️ | Malakoff › Vallée Sud Grand Paris | 1 |
| Bois de Antony (2) ⚠️ | Antony › Vallée Sud Grand Paris | 1 |
| Parc de la Maison des Arts ⚠️ | Châtillon › Vallée Sud Grand Paris | 1 |
| Parc des Pierrettes ⚠️ | Châtillon › Vallée Sud Grand Paris | 1 |
| Parc des Pierrelais ⚠️ | Châtillon › Vallée Sud Grand Paris | 1 |
| Forêt de Clichy ⚠️ | Clichy › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Forêt de Clichy (2) ⚠️ | Clichy › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Berges de la Seine ⚠️ | Courbevoie › Paris Ouest La Défense | 1 |
| Jardin Toscan ⚠️ | Montrouge › Vallée Sud Grand Paris | 1 |
| Parc Sainte-Barbe ⚠️ | Fontenay-aux-Roses › Vallée Sud Grand Paris | 1 |
| Square de l'Hôtel de Ville ⚠️ | Courbevoie › Paris Ouest La Défense | 1 |
| Bois de Meudon (2) ⚠️ | Meudon › Grand Paris Seine Ouest | 1 |
| Jardin de la Pointe ⚠️ | Boulogne-Billancourt › Grand Paris Seine Ouest | 1 |
| Square du Souvenir Français (2) ⚠️ | Asnières-sur-Seine › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Parc Robert Auzelle ⚠️ | Clamart › Vallée Sud Grand Paris | 1 |
| Parc de Courbevoie (10) ⚠️ | Courbevoie › Paris Ouest La Défense | 1 |
| Forêt de Meudon ⚠️ | Meudon › Grand Paris Seine Ouest | 1 |
| Parc de Meudon (4) ⚠️ | Meudon › Grand Paris Seine Ouest | 1 |
| Square Maréchal Leclerc ⚠️ | Asnières-sur-Seine › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Jardin Bellini ⚠️ | Boulogne-Billancourt › Grand Paris Seine Ouest | 1 |
| Square du 8 mai 1945 ⚠️ | Asnières-sur-Seine › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Parc Georges Levillain ⚠️ | Clichy › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Bois de Antony (3) ⚠️ | Antony › Vallée Sud Grand Paris | 1 |
| Parc du Souvenir Français ⚠️ | Châtenay-Malabry › Vallée Sud Grand Paris | 1 |
| Bois de Saint-Cloud ⚠️ | Saint-Cloud › Paris Ouest La Défense | 1 |
| Forêt de Issy-les-Moulineaux (12) ⚠️ | Issy-les-Moulineaux › Grand Paris Seine Ouest | 1 |
| Forêt de Issy-les-Moulineaux (18) ⚠️ | Issy-les-Moulineaux › Grand Paris Seine Ouest | 1 |
| Jardins de l'Hôtel de Ville ⚠️ | Levallois-Perret › Paris Ouest La Défense | 1 |
| Forêt de Marnes-la-Coquette (2) ⚠️ | Marnes-la-Coquette › Grand Paris Seine Ouest | 1 |
| Forêt de Rueil-Malmaison (20) ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 1 |
| Parc du Mont-Valérien (2) ⚠️ | Suresnes › Paris Ouest La Défense | 1 |
| Square Médéric (2) ⚠️ | Colombes › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Parc Marguerite Yourcenar ⚠️ | Asnières-sur-Seine › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Parc de Montrouge (2) ⚠️ | Montrouge › Vallée Sud Grand Paris | 1 |
| Forêt de Montrouge (8) ⚠️ | Montrouge › Vallée Sud Grand Paris | 1 |
| Forêt de Gennevilliers (8) ⚠️ | Gennevilliers › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Forêt de Villeneuve-la-Garenne ⚠️ | Villeneuve-la-Garenne › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Forêt de Villeneuve-la-Garenne (8) ⚠️ | Villeneuve-la-Garenne › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Forêt de Villeneuve-la-Garenne (15) ⚠️ | Villeneuve-la-Garenne › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Bois de Antony (4) ⚠️ | Antony › Vallée Sud Grand Paris | 1 |
| Résidence Séverine (2) ⚠️ | Issy-les-Moulineaux › Grand Paris Seine Ouest | 1 |
| Forêt de Antony (9) ⚠️ | Antony › Vallée Sud Grand Paris | 1 |
| Square des États-Unis ⚠️ | Montrouge › Vallée Sud Grand Paris | 1 |
| Parc de Meudon (7) ⚠️ | Meudon › Grand Paris Seine Ouest | 1 |
| Jardin de la Cour d'Honneur ⚠️ | Issy-les-Moulineaux › Grand Paris Seine Ouest | 1 |
| Passage des glycines ⚠️ | Puteaux › Paris Ouest La Défense | 1 |
| Forêt de Issy-les-Moulineaux (29) ⚠️ | Issy-les-Moulineaux › Grand Paris Seine Ouest | 1 |
| Square de la Liberté ⚠️ | Le Plessis-Robinson › Vallée Sud Grand Paris | 1 |
| Forêt de Saint-Cloud (29) ⚠️ | Saint-Cloud › Paris Ouest La Défense | 1 |
| Bois de Meudon (6) ⚠️ | Meudon › Grand Paris Seine Ouest | 1 |
| Bois de Issy-les-Moulineaux ⚠️ | Issy-les-Moulineaux › Grand Paris Seine Ouest | 1 |
| Bois de Meudon (9) ⚠️ | Meudon › Grand Paris Seine Ouest | 1 |
| Parc de Ville-d'Avray ⚠️ | Ville-d'Avray › Grand Paris Seine Ouest | 1 |
| Parc de Châtillon (5) ⚠️ | Châtillon › Vallée Sud Grand Paris | 1 |
| Jardin des délices ⚠️ | Puteaux › Paris Ouest La Défense | 1 |
| Parc de Ville-d'Avray (2) ⚠️ | Ville-d'Avray › Grand Paris Seine Ouest | 1 |
| Forêt de Meudon (9) ⚠️ | Meudon › Grand Paris Seine Ouest | 1 |
| Square Daniel Rops ⚠️ | Neuilly-sur-Seine › Paris Ouest La Défense | 1 |
| Forêt de Vanves (16) ⚠️ | Vanves › Grand Paris Seine Ouest | 1 |
| Forêt de Vanves (17) ⚠️ | Vanves › Grand Paris Seine Ouest | 1 |
| Forêt de Issy-les-Moulineaux (34) ⚠️ | Issy-les-Moulineaux › Grand Paris Seine Ouest | 1 |
| Bois de Colombes (4) ⚠️ | Colombes › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Bois de Colombes (6) ⚠️ | Colombes › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Bois de Gennevilliers (5) ⚠️ | Gennevilliers › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Bois de Colombes (8) ⚠️ | Colombes › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Bois de Gennevilliers (15) ⚠️ | Gennevilliers › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Bois de Villeneuve-la-Garenne ⚠️ | Villeneuve-la-Garenne › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Bois de Villeneuve-la-Garenne (7) ⚠️ | Villeneuve-la-Garenne › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Bois de Antony (8) ⚠️ | Antony › Vallée Sud Grand Paris | 1 |
| Parc de Issy-les-Moulineaux (4) ⚠️ | Issy-les-Moulineaux › Grand Paris Seine Ouest | 1 |
| Forêt de Saint-Cloud (37) ⚠️ | Saint-Cloud › Paris Ouest La Défense | 1 |
| Forêt de Marnes-la-Coquette (4) ⚠️ | Marnes-la-Coquette › Grand Paris Seine Ouest | 1 |
| Forêt de Meudon (13) ⚠️ | Meudon › Grand Paris Seine Ouest | 1 |
| Forêt de Saint-Cloud (43) ⚠️ | Saint-Cloud › Paris Ouest La Défense | 1 |
| Forêt de Saint-Cloud (44) ⚠️ | Saint-Cloud › Paris Ouest La Défense | 1 |
| Forêt de Saint-Cloud (64) ⚠️ | Saint-Cloud › Paris Ouest La Défense | 1 |
| Jardin des Avelines ⚠️ | Saint-Cloud › Paris Ouest La Défense | 1 |
| Bois de Châtenay-Malabry (9) ⚠️ | Châtenay-Malabry › Vallée Sud Grand Paris | 1 |
| Forêt de Antony (10) ⚠️ | Antony › Vallée Sud Grand Paris | 1 |
| Forêt de Antony (12) ⚠️ | Antony › Vallée Sud Grand Paris | 1 |
| Parc de Meudon (8) ⚠️ | Meudon › Grand Paris Seine Ouest | 1 |
| Forêt de Villeneuve-la-Garenne (19) ⚠️ | Villeneuve-la-Garenne › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Forêt de Fontenay-aux-Roses ⚠️ | Fontenay-aux-Roses › Vallée Sud Grand Paris | 1 |
| Bois de Antony (13) ⚠️ | Antony › Vallée Sud Grand Paris | 1 |
| Parc de Villeneuve-la-Garenne (2) ⚠️ | Villeneuve-la-Garenne › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Forêt de Boulogne-Billancourt (16) ⚠️ | Boulogne-Billancourt › Grand Paris Seine Ouest | 1 |
| Forêt de Rueil-Malmaison (30) ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 1 |
| Forêt de Sceaux (16) ⚠️ | Sceaux › Vallée Sud Grand Paris | 1 |
| Jardins du Grand Échiquier ⚠️ | Asnières-sur-Seine › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Parc Maxime Vachier-Lagrave ⚠️ | Asnières-sur-Seine › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Bois de Rueil-Malmaison (9) ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 1 |
| Bois de Rueil-Malmaison (15) ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 1 |
| Bois de Rueil-Malmaison (16) ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 1 |
| Bois de Rueil-Malmaison (17) ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 1 |
| Bois de Vaucresson (18) ⚠️ | Vaucresson › Paris Ouest La Défense | 1 |
| Bois de Vaucresson (19) ⚠️ | Vaucresson › Paris Ouest La Défense | 1 |
| Bois de Rueil-Malmaison (31) ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 1 |
| Bois de Rueil-Malmaison (34) ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 1 |
| Parc de Colombes (2) ⚠️ | Colombes › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Parc de Villeneuve-la-Garenne (3) ⚠️ | Villeneuve-la-Garenne › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Parc de Gennevilliers (11) ⚠️ | Gennevilliers › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Bois de Villeneuve-la-Garenne (11) ⚠️ | Villeneuve-la-Garenne › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Bois de Villeneuve-la-Garenne (12) ⚠️ | Villeneuve-la-Garenne › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Bois de Gennevilliers (25) ⚠️ | Gennevilliers › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Bois de Gennevilliers (28) ⚠️ | Gennevilliers › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Forêt de Châtenay-Malabry (14) ⚠️ | Châtenay-Malabry › Vallée Sud Grand Paris | 1 |
| Bois de Gennevilliers (29) ⚠️ | Gennevilliers › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Parc des Cinq Continents - Jacques Chirac ⚠️ | Levallois-Perret › Paris Ouest La Défense | 1 |
| Parc de Clamart (3) ⚠️ | Clamart › Vallée Sud Grand Paris | 1 |
| Mail René Rousseau ⚠️ | Bagneux › Vallée Sud Grand Paris | 1 |
| Forêt de Clamart (5) ⚠️ | Clamart › Vallée Sud Grand Paris | 1 |
| Mini-Forêt Miyawaki ⚠️ | Montrouge › Vallée Sud Grand Paris | 1 |
| Bois du Plessis-Robinson (3) ⚠️ | Le Plessis-Robinson › Vallée Sud Grand Paris | 1 |
| Bois du Plessis-Robinson (4) ⚠️ | Le Plessis-Robinson › Vallée Sud Grand Paris | 1 |
| Bois du Plessis-Robinson (6) ⚠️ | Le Plessis-Robinson › Vallée Sud Grand Paris | 1 |
| Bois du Plessis-Robinson (7) ⚠️ | Le Plessis-Robinson › Vallée Sud Grand Paris | 1 |
| Parc de Puteaux (5) ⚠️ | Puteaux › Paris Ouest La Défense | 1 |
| Parc de Nanterre (20) ⚠️ | Nanterre › Paris Ouest La Défense | 1 |
| Parc de Puteaux (7) ⚠️ | Puteaux › Paris Ouest La Défense | 1 |
| Parc départemental Gauthier-Mougin ⚠️ | Boulogne-Billancourt › Grand Paris Seine Ouest | 1 |
| Bois de Saint-Cloud (4) ⚠️ | Saint-Cloud › Paris Ouest La Défense | 1 |
| Parc Thieulin ⚠️ | Bourg-la-Reine › Vallée Sud Grand Paris | 1 |
| Parc de Bagneux (3) ⚠️ | Bagneux › Vallée Sud Grand Paris | 1 |
| Parc de Puteaux (9) ⚠️ | Puteaux › Paris Ouest La Défense | 1 |
| Forêt de Suresnes (35) ⚠️ | Suresnes › Paris Ouest La Défense | 1 |
| Bois de Antony (16) ⚠️ | Antony › Vallée Sud Grand Paris | 1 |
| Bois des Fonds Maréchaux ⚠️ | Vaucresson › Paris Ouest La Défense | 1 |
| Parc Camille Ronce ⚠️ | Gennevilliers › Boucle Nord de Seine (Hauts-de-Seine) | 1 |
| Parc Jacques Chirac ⚠️ | Rueil-Malmaison › Paris Ouest La Défense | 1 |
| Forêt de Sceaux (20) ⚠️ | Sceaux › Vallée Sud Grand Paris | 1 |
| Forêt de Sceaux (21) ⚠️ | Sceaux › Vallée Sud Grand Paris | 1 |
| Bois de Boulogne ⚠️ | Neuilly-sur-Seine › Paris Ouest La Défense | 1 |
| Parc de Sèvres (5) ⚠️ | Sèvres › Grand Paris Seine Ouest | 1 |
| Bois de Antony (17) ⚠️ | Antony › Vallée Sud Grand Paris | 1 |

1 135 parc(s) plus petits qu'une cellule ne sont pas listés : la carte les dessine, mais ils n'offrent aucune cellule.

⚠️ 1473 parc(s) hors de la fenêtre 10–125 cellules (1470 trop petit(s), 3 trop grand(s)) : affichés sur la carte, mais ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| military | 39 |
| prison | 3 |
| airport | 0 |
| **Total déclaré** | **42** |
| dont dans une zone de ce territoire | 42 |


### Zones concernées

| Zone | Cellules exclues |
|---|---:|
| Suresnes | 11 |
| Meudon | 8 |
| Malakoff | 8 |
| Nanterre | 7 |
| Clamart | 5 |
| Issy-les-Moulineaux | 3 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
