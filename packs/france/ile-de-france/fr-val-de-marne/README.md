# Val-de-Marne

Pack `fr-val-de-marne` · version 1.0.1 · grille 200 m · France › Île-de-France

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 13 751 |
| dont restreintes (aéroport, militaire, prison) | 364 |
| dont sans chemin (aucune voie à moins de 60 m) | 152 |
| dont en forêt, sans chemin non plus | 38 |
| dont traversées par un cours d'eau, sans chemin non plus | 12 |
| Cellules retirées par le masque d'eau | 326 |
| Villes | 47 |
| Arrondissements et quartiers | 0 |
| Îles | 3 |
| Parcs | 2 003 |

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
| Grand Paris Sud Est Avenir | 5 661 | somme de 16 villes |
| Grand-Orly Seine Bièvre (Val-de-Marne) | 4 938 | somme de 18 villes |
| Paris-Est-Marne et Bois | 3 152 | somme de 13 villes |

Une île *composite* n'a pas de cellules à elle : sa progression est la somme de ses villes, et ses cellules ne lui sont jamais rattachées directement — elles compteraient deux fois.

## Villes (47)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Sans chemin | Parcs |
|---|---:|---:|---:|---:|---:|---:|---:|
| Vitry-sur-Seine | 672 | 18 | 654 | 0 | **654** | 2 (0 %) | 90 |
| Champigny-sur-Marne | 655 | 11 | 644 | 0 | **644** |  | 128 |
| Saint-Maur-des-Fossés | 646 | 14 | 632 | 0 | **632** |  | 48 |
| Créteil | 661 | 31 | 630 | 0 | **630** |  | 135 |
| Sucy-en-Brie | 602 | 3 | 599 | 0 | **599** | 1 (0 %) | 41 |
| Santeny | 569 | 2 | 567 | 0 | **567** | 39 (7 %) | 42 |
| La Queue-en-Brie | 545 | 2 | 543 | 0 | **543** | 4 (1 %) | 37 |
| Boissy-Saint-Léger | 516 | 4 | 512 | 0 | **512** | 6 (1 %) | 33 |
| Villeneuve-le-Roi | 482 | 24 | 458 | 154 | **304** | 1 (0 %) | 45 |
| Villeneuve-Saint-Georges | 462 | 20 | 442 | 6 | **436** | 9 (2 %) | 49 |
| Limeil-Brévannes | 396 | 0 | 396 | 4 | **392** | 1 (0 %) | 39 |
| Orly | 387 | 8 | 379 | 141 | **238** |  | 57 |
| Thiais | 369 | 1 | 368 | 0 | **368** |  | 88 |
| Ivry-sur-Seine | 355 | 10 | 345 | 6 | **339** |  | 56 |
| Fontenay-sous-Bois | 322 | 0 | 322 | 8 | **314** |  | 47 |
| Villecresnes | 321 | 1 | 320 | 0 | **320** | 10 (3 %) | 35 |
| Villejuif | 304 | 0 | 304 | 0 | **304** |  | 50 |
| Chennevières-sur-Marne | 303 | 6 | 297 | 0 | **297** | 1 (0 %) | 38 |
| Maisons-Alfort | 308 | 13 | 295 | 15 | **280** |  | 89 |
| Valenton | 309 | 16 | 293 | 2 | **291** | 8 (3 %) | 47 |
| Bonneuil-sur-Marne | 317 | 28 | 289 | 0 | **289** |  | 30 |
| Choisy-le-Roi | 308 | 34 | 274 | 0 | **274** | 2 (1 %) | 43 |
| Marolles-en-Brie | 265 | 2 | 263 | 0 | **263** | 3 (1 %) | 13 |
| Noiseau | 262 | 3 | 259 | 0 | **259** | 30 (12 %) | 7 |
| Le Plessis-Trévise | 251 | 0 | 251 | 0 | **251** | 6 (2 %) | 15 |
| Rungis | 243 | 0 | 243 | 0 | **243** |  | 55 |
| Villiers-sur-Marne | 243 | 0 | 243 | 0 | **243** |  | 38 |
| Chevilly-Larue | 241 | 0 | 241 | 0 | **241** |  | 46 |
| L'Haÿ-les-Roses | 227 | 0 | 227 | 0 | **227** |  | 35 |
| Le Perreux-sur-Marne | 226 | 2 | 224 | 0 | **224** |  | 7 |
| Fresnes | 205 | 0 | 205 | 7 | **198** |  | 43 |
| Alfortville | 215 | 21 | 194 | 0 | **194** |  | 19 |
| Ormesson-sur-Marne | 194 | 0 | 194 | 0 | **194** | 8 (4 %) | 10 |
| Mandres-les-Roses | 192 | 2 | 190 | 0 | **190** | 7 (4 %) | 40 |
| Bry-sur-Marne | 196 | 13 | 183 | 0 | **183** |  | 68 |
| Cachan | 159 | 0 | 159 | 0 | **159** |  | 31 |
| Périgny | 158 | 1 | 157 | 0 | **157** | 14 (9 %) | 31 |
| Nogent-sur-Marne | 160 | 5 | 155 | 0 | **155** |  | 39 |
| Arcueil | 132 | 0 | 132 | 11 | **121** |  | 41 |
| Joinville-le-Pont | 129 | 15 | 114 | 0 | **114** |  | 30 |
| Vincennes | 111 | 0 | 111 | 0 | **111** |  | 20 |
| Charenton-le-Pont | 105 | 6 | 99 | 0 | **99** |  | 23 |
| Le Kremlin-Bicêtre | 88 | 0 | 88 | 7 | **81** |  | 10 |
| Saint-Maurice | 78 | 3 | 75 | 0 | **75** |  | 30 |
| Gentilly | 67 | 0 | 67 | 0 | **67** |  | 24 |
| Ablon-sur-Seine | 66 | 7 | 59 | 0 | **59** |  | 25 |
| Saint-Mandé | 55 | 0 | 55 | 3 | **52** |  | 6 |

## Parcs (2003)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Forêt domaniale de Notre-Dame ⚠️ | Santeny › Grand Paris Sud Est Avenir | 836 |
| Forêt régionale de Gros Bois | Boissy-Saint-Léger › Grand Paris Sud Est Avenir | 113 |
| Forêt de Limeil-Brévannes (4) | Limeil-Brévannes › Grand Paris Sud Est Avenir | 89 |
| Forêt de Boissy-Saint-Léger (2) | Boissy-Saint-Léger › Grand Paris Sud Est Avenir | 85 |
| Forêt de Limeil-Brévannes (2) | Limeil-Brévannes › Grand Paris Sud Est Avenir | 59 |
| Parc départemental des Lilas | Vitry-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 56 |
| Bois du Petit-Val | Boissy-Saint-Léger › Grand Paris Sud Est Avenir | 54 |
| Parc Interdépartemental des Sports - Plaine Sud | Choisy-le-Roi › Grand-Orly Seine Bièvre (Val-de-Marne) | 44 |
| Parc de Détente et de Loisirs du Tremblay | Champigny-sur-Marne › Paris-Est-Marne et Bois | 37 |
| Forêt de Noiseau | Noiseau › Grand Paris Sud Est Avenir | 29 |
| Île de Loisirs de Créteil | Créteil › Grand Paris Sud Est Avenir | 27 |
| Forêt régionale du Plessis Saint-Antoine | Le Plessis-Trévise › Grand Paris Sud Est Avenir | 19 |
| Parc départemental de la Plage Bleue | Valenton › Grand-Orly Seine Bièvre (Val-de-Marne) | 15 |
| Forêt de Villecresnes (27) | Villecresnes › Grand Paris Sud Est Avenir | 15 |
| Forêt de Villecresnes (28) | Villecresnes › Grand Paris Sud Est Avenir | 13 |
| Parc de Choisy-le-Roi (2) | Choisy-le-Roi › Grand-Orly Seine Bièvre (Val-de-Marne) | 12 |
| Parc Départemental des Hautes Bruyères | Villejuif › Grand-Orly Seine Bièvre (Val-de-Marne) | 11 |
| Parc départemental du Morbras | Ormesson-sur-Marne › Grand Paris Sud Est Avenir | 10 |
| Cité Verte | Sucy-en-Brie › Grand Paris Sud Est Avenir | 10 |
| Forêt de Villeneuve-Saint-Georges | Villeneuve-Saint-Georges › Grand-Orly Seine Bièvre (Val-de-Marne) | 10 |
| Forêt de Orly (2) | Orly › Grand-Orly Seine Bièvre (Val-de-Marne) | 10 |
| Parc départemental de la Roseraie ⚠️ | L'Haÿ-les-Roses › Grand-Orly Seine Bièvre (Val-de-Marne) | 8 |
| Parc du Château de Retz ⚠️ | Chennevières-sur-Marne › Grand Paris Sud Est Avenir | 8 |
| Bois de Chennevières-sur-Marne (17) ⚠️ | Chennevières-sur-Marne › Grand Paris Sud Est Avenir | 8 |
| Forêt de Limeil-Brévannes ⚠️ | Limeil-Brévannes › Grand Paris Sud Est Avenir | 8 |
| Forêt de Villecresnes (29) ⚠️ | Villecresnes › Grand Paris Sud Est Avenir | 8 |
| Parc départemental Saussaie-Pidoux ⚠️ | Villeneuve-Saint-Georges › Grand-Orly Seine Bièvre (Val-de-Marne) | 7 |
| Parc Hôpital Émile Roux ⚠️ | Limeil-Brévannes › Grand Paris Sud Est Avenir | 7 |
| Parc Départemental du Plateau (3) ⚠️ | Champigny-sur-Marne › Paris-Est-Marne et Bois | 7 |
| Parc intercommunal des Sports du Grand Godet ⚠️ | Villeneuve-le-Roi › Grand-Orly Seine Bièvre (Val-de-Marne) | 6 |
| Espace Naturel de la Pierre-Fitte ⚠️ | Villeneuve-le-Roi › Grand-Orly Seine Bièvre (Val-de-Marne) | 6 |
| Bois Lacroix ⚠️ | La Queue-en-Brie › Grand Paris Sud Est Avenir | 6 |
| Bois de l'Haÿ-les-Roses ⚠️ | L'Haÿ-les-Roses › Grand-Orly Seine Bièvre (Val-de-Marne) | 6 |
| Forêt de Santeny (13) ⚠️ | Santeny › Grand Paris Sud Est Avenir | 6 |
| Forêt de Bonneuil-sur-Marne (9) ⚠️ | Bonneuil-sur-Marne › Grand Paris Sud Est Avenir | 6 |
| Forêt de Sucy-en-Brie (11) ⚠️ | Sucy-en-Brie › Grand Paris Sud Est Avenir | 6 |
| Parc des Artistes ⚠️ | Nogent-sur-Marne › Paris-Est-Marne et Bois | 5 |
| Parc départemental du Petit-le-Roy ⚠️ | Chevilly-Larue › Grand-Orly Seine Bièvre (Val-de-Marne) | 5 |
| Forêt de Santeny (5) ⚠️ | Santeny › Grand Paris Sud Est Avenir | 5 |
| Parc départemental de la Plaine des Bordes ⚠️ | Chennevières-sur-Marne › Grand Paris Sud Est Avenir | 5 |
| Parc des Saules ⚠️ | Orly › Grand-Orly Seine Bièvre (Val-de-Marne) | 5 |
| Bois de Villecresnes (2) ⚠️ | Villecresnes › Grand Paris Sud Est Avenir | 5 |
| bois du Luzard ⚠️ | Le Plessis-Trévise › Grand Paris Sud Est Avenir | 5 |
| Île des Loups ⚠️ | Le Perreux-sur-Marne › Paris-Est-Marne et Bois | 4 |
| Parc départemental du Champ Saint-Julien ⚠️ | Valenton › Grand-Orly Seine Bièvre (Val-de-Marne) | 4 |
| Bois de Marolles-en-Brie ⚠️ | Marolles-en-Brie › Grand Paris Sud Est Avenir | 4 |
| Parc du Coteau de Bièvre ⚠️ | Arcueil › Grand-Orly Seine Bièvre (Val-de-Marne) | 4 |
| Forêt de Périgny (31) ⚠️ | Périgny › Grand Paris Sud Est Avenir | 4 |
| Parc départemental des Cormailles ⚠️ | Ivry-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 4 |
| Forêt de Sucy-en-Brie (2) ⚠️ | Sucy-en-Brie › Grand Paris Sud Est Avenir | 3 |
| Forêt de Santeny ⚠️ | Santeny › Grand Paris Sud Est Avenir | 3 |
| Forêt de La Queue-en-Brie (6) ⚠️ | La Queue-en-Brie › Grand Paris Sud Est Avenir | 3 |
| Parc de la Garennière ⚠️ | Sucy-en-Brie › Grand Paris Sud Est Avenir | 3 |
| Parc départemental du Rancy ⚠️ | Bonneuil-sur-Marne › Grand Paris Sud Est Avenir | 3 |
| Forêt de Chennevières-sur-Marne (2) ⚠️ | Chennevières-sur-Marne › Grand Paris Sud Est Avenir | 3 |
| Parc de Saint-Maurice ⚠️ | Saint-Maurice › Paris-Est-Marne et Bois | 3 |
| Parc de la Bièvre (2) ⚠️ | L'Haÿ-les-Roses › Grand-Orly Seine Bièvre (Val-de-Marne) | 3 |
| Bois de Chevilly-Larue (2) ⚠️ | Chevilly-Larue › Grand-Orly Seine Bièvre (Val-de-Marne) | 3 |
| Parc des Coudrais ⚠️ | Bry-sur-Marne › Paris-Est-Marne et Bois | 3 |
| Bois grignon ⚠️ | Orly › Grand-Orly Seine Bièvre (Val-de-Marne) | 3 |
| Forêt de Santeny (14) ⚠️ | Santeny › Grand Paris Sud Est Avenir | 3 |
| Forêt de Santeny (16) ⚠️ | Santeny › Grand Paris Sud Est Avenir | 3 |
| Bois de Bry-sur-Marne (23) ⚠️ | Bry-sur-Marne › Paris-Est-Marne et Bois | 3 |
| Bois de Vitry-sur-Seine (2) ⚠️ | Vitry-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 3 |
| Forêt de Limeil-Brévannes (3) ⚠️ | Limeil-Brévannes › Grand Paris Sud Est Avenir | 3 |
| Parc Georges Méliès ⚠️ | Orly › Grand-Orly Seine Bièvre (Val-de-Marne) | 2 |
| Parc Mélinée et Missak Manouchian ⚠️ | Bonneuil-sur-Marne › Grand Paris Sud Est Avenir | 2 |
| Forêt de Chennevières-sur-Marne ⚠️ | Chennevières-sur-Marne › Grand Paris Sud Est Avenir | 2 |
| Parc Maurice Thorez ⚠️ | Choisy-le-Roi › Grand-Orly Seine Bièvre (Val-de-Marne) | 2 |
| Parc de Noiseau ⚠️ | Noiseau › Grand Paris Sud Est Avenir | 2 |
| Forêt de Santeny (2) ⚠️ | Santeny › Grand Paris Sud Est Avenir | 2 |
| Forêt de La Queue-en-Brie (7) ⚠️ | La Queue-en-Brie › Grand Paris Sud Est Avenir | 2 |
| Parc des Sports ⚠️ | Fresnes › Grand-Orly Seine Bièvre (Val-de-Marne) | 2 |
| Parc Frédéric Joliot Curie ⚠️ | Vitry-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 2 |
| Forêt de Rungis ⚠️ | Rungis › Grand-Orly Seine Bièvre (Val-de-Marne) | 2 |
| Parc Jacques Chirac ⚠️ | Valenton › Grand-Orly Seine Bièvre (Val-de-Marne) | 2 |
| Parc urbain des Sarrazins ⚠️ | Créteil › Grand Paris Sud Est Avenir | 2 |
| Parc des Prés de la Bièvre ⚠️ | Fresnes › Grand-Orly Seine Bièvre (Val-de-Marne) | 2 |
| Parc La Fontaine ⚠️ | L'Haÿ-les-Roses › Grand-Orly Seine Bièvre (Val-de-Marne) | 2 |
| Parc André Villette ⚠️ | Fresnes › Grand-Orly Seine Bièvre (Val-de-Marne) | 2 |
| Parc du Vert-de-Maisons ⚠️ | Maisons-Alfort › Paris-Est-Marne et Bois | 2 |
| Écoparc des Carrières ⚠️ | Fontenay-sous-Bois › Paris-Est-Marne et Bois | 2 |
| Colline du Bois l'Abbé ⚠️ | Chennevières-sur-Marne › Grand Paris Sud Est Avenir | 2 |
| Parc Léon Bernard ⚠️ | Limeil-Brévannes › Grand Paris Sud Est Avenir | 2 |
| Forêt de Champigny-sur-Marne (4) ⚠️ | Champigny-sur-Marne › Paris-Est-Marne et Bois | 2 |
| Parc des Sœurs ⚠️ | Ablon-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 2 |
| Ferme du Parc des Meuniers ⚠️ | Villeneuve-le-Roi › Grand-Orly Seine Bièvre (Val-de-Marne) | 2 |
| Parc de Fresnes ⚠️ | Fresnes › Grand-Orly Seine Bièvre (Val-de-Marne) | 2 |
| Bois de Chennevières-sur-Marne ⚠️ | Chennevières-sur-Marne › Grand Paris Sud Est Avenir | 2 |
| Parc du domaine de Château Gaillard ⚠️ | Maisons-Alfort › Paris-Est-Marne et Bois | 2 |
| Forêt de Bonneuil-sur-Marne (2) ⚠️ | Bonneuil-sur-Marne › Grand Paris Sud Est Avenir | 2 |
| Forêt de Thiais ⚠️ | Thiais › Grand-Orly Seine Bièvre (Val-de-Marne) | 2 |
| Forêt de Santeny (15) ⚠️ | Santeny › Grand Paris Sud Est Avenir | 2 |
| Forêt de Mandres-les-Roses (5) ⚠️ | Mandres-les-Roses › Grand Paris Sud Est Avenir | 2 |
| Bois de Limeil-Brévannes ⚠️ | Limeil-Brévannes › Grand Paris Sud Est Avenir | 2 |
| Forêt de Villecresnes (4) ⚠️ | Mandres-les-Roses › Grand Paris Sud Est Avenir | 2 |
| Forêt de Villecresnes (9) ⚠️ | Villecresnes › Grand Paris Sud Est Avenir | 2 |
| Parc des Bordières ⚠️ | Créteil › Grand Paris Sud Est Avenir | 2 |
| Forêt de Boissy-Saint-Léger (9) ⚠️ | Boissy-Saint-Léger › Grand Paris Sud Est Avenir | 2 |
| Bois de Créteil (24) ⚠️ | Créteil › Grand Paris Sud Est Avenir | 2 |
| Bois de Choisy-le-Roi ⚠️ | Choisy-le-Roi › Grand-Orly Seine Bièvre (Val-de-Marne) | 2 |
| Bois de Joinville-le-Pont ⚠️ | Joinville-le-Pont › Paris-Est-Marne et Bois | 2 |
| Bois de Saint-Maurice (7) ⚠️ | Saint-Maurice › Paris-Est-Marne et Bois | 2 |
| Bois de Choisy-le-Roi (7) ⚠️ | Choisy-le-Roi › Grand-Orly Seine Bièvre (Val-de-Marne) | 2 |
| Bois de Thiais (34) ⚠️ | Thiais › Grand-Orly Seine Bièvre (Val-de-Marne) | 2 |
| Bois de Ablon-sur-Seine (3) ⚠️ | Ablon-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 2 |
| Bois de Boissy-Saint-Léger (11) ⚠️ | Boissy-Saint-Léger › Grand Paris Sud Est Avenir | 2 |
| Bois de Champigny-sur-Marne (79) ⚠️ | Champigny-sur-Marne › Paris-Est-Marne et Bois | 2 |
| Parc de Villecresnes ⚠️ | Villecresnes › Grand Paris Sud Est Avenir | 2 |
| Bosquet de Saint-Leu ⚠️ | Mandres-les-Roses › Grand Paris Sud Est Avenir | 2 |
| Forêt de Mandres-les-Roses (28) ⚠️ | Mandres-les-Roses › Grand Paris Sud Est Avenir | 2 |
| Bois de Vitry-sur-Seine (46) ⚠️ | Vitry-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 2 |
| Colline Cacao ⚠️ | Rungis › Grand-Orly Seine Bièvre (Val-de-Marne) | 2 |
| Parc de la Chênaie ⚠️ | Sucy-en-Brie › Grand Paris Sud Est Avenir | 2 |
| Esplanade Alexandre Bazin ⚠️ | Champigny-sur-Marne › Paris-Est-Marne et Bois | 2 |
| Forêt de Champigny-sur-Marne ⚠️ | Champigny-sur-Marne › Paris-Est-Marne et Bois | 1 |
| Forêt du Plessis-Trévise ⚠️ | Le Plessis-Trévise › Grand Paris Sud Est Avenir | 1 |
| île des Gords ⚠️ | Champigny-sur-Marne › Paris-Est-Marne et Bois | 1 |
| Forêt de Ormesson-sur-Marne ⚠️ | Ormesson-sur-Marne › Grand Paris Sud Est Avenir | 1 |
| Square Pierre Brossolette ⚠️ | Choisy-le-Roi › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc de l'Europe ⚠️ | Thiais › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc de Ormesson-sur-Marne ⚠️ | Ormesson-sur-Marne › Grand Paris Sud Est Avenir | 1 |
| Forêt de Sucy-en-Brie ⚠️ | Sucy-en-Brie › Grand Paris Sud Est Avenir | 1 |
| Parc Pablo Neruda ⚠️ | Villejuif › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Forêt de Marolles-en-Brie ⚠️ | Marolles-en-Brie › Grand Paris Sud Est Avenir | 1 |
| Forêt de La Queue-en-Brie ⚠️ | La Queue-en-Brie › Grand Paris Sud Est Avenir | 1 |
| Forêt de La Queue-en-Brie (5) ⚠️ | La Queue-en-Brie › Grand Paris Sud Est Avenir | 1 |
| Parc Dupeyroux ⚠️ | Créteil › Grand Paris Sud Est Avenir | 1 |
| Parc de la Brèche ⚠️ | Créteil › Grand Paris Sud Est Avenir | 1 |
| Parc des Lilas ⚠️ | Villejuif › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc du 8 mai 1945 ⚠️ | Villejuif › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc de la Mairie ⚠️ | Choisy-le-Roi › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Square Saint-Hilaire ⚠️ | Saint-Maur-des-Fossés › Paris-Est-Marne et Bois | 1 |
| Parc des Olympiades ⚠️ | Fontenay-sous-Bois › Paris-Est-Marne et Bois | 1 |
| Parc de l'Hôtel de Ville ⚠️ | Fontenay-sous-Bois › Paris-Est-Marne et Bois | 1 |
| Parc des Épivans ⚠️ | Fontenay-sous-Bois › Paris-Est-Marne et Bois | 1 |
| Square Jean Esquirol ⚠️ | Créteil › Grand Paris Sud Est Avenir | 1 |
| Square de l'Abbaye ⚠️ | Saint-Maur-des-Fossés › Paris-Est-Marne et Bois | 1 |
| Parc Paul Vaillant-Couturier ⚠️ | Arcueil › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Jardin Pablo Picasso ⚠️ | Gentilly › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Forêt de Villecresnes ⚠️ | Villecresnes › Grand Paris Sud Est Avenir | 1 |
| Parc de la Libération ⚠️ | Valenton › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Forêt de Orly ⚠️ | Orly › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc du Saut du Loup ⚠️ | Le Perreux-sur-Marne › Paris-Est-Marne et Bois | 1 |
| Square De Lattre de Tassigny ⚠️ | Bry-sur-Marne › Paris-Est-Marne et Bois | 1 |
| Forêt de La Queue-en-Brie (10) ⚠️ | La Queue-en-Brie › Grand Paris Sud Est Avenir | 1 |
| Parc Philippe Pinel ⚠️ | Le Kremlin-Bicêtre › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Montjean ⚠️ | Rungis › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc départemental Maurice Thorez ⚠️ | Ivry-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Promenade des petits bois ⚠️ | Ivry-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Forêt de La Queue-en-Brie (11) ⚠️ | La Queue-en-Brie › Grand Paris Sud Est Avenir | 1 |
| Forêt de La Queue-en-Brie (12) ⚠️ | La Queue-en-Brie › Grand Paris Sud Est Avenir | 1 |
| Square du Regard ⚠️ | Rungis › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc Eliane et Jean-Pierre Gervaise ⚠️ | Villiers-sur-Marne › Paris-Est-Marne et Bois | 1 |
| Forêt de Champigny-sur-Marne (3) ⚠️ | Champigny-sur-Marne › Paris-Est-Marne et Bois | 1 |
| Parc de Fontenay-sous-Bois (3) ⚠️ | Fontenay-sous-Bois › Paris-Est-Marne et Bois | 1 |
| Forêt de La Queue-en-Brie (19) ⚠️ | La Queue-en-Brie › Grand Paris Sud Est Avenir | 1 |
| Parc Chaumoncel ⚠️ | Sucy-en-Brie › Grand Paris Sud Est Avenir | 1 |
| Parc de la Bièvre ⚠️ | L'Haÿ-les-Roses › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc Corot ⚠️ | Chennevières-sur-Marne › Grand Paris Sud Est Avenir | 1 |
| Parc de Cachan ⚠️ | Cachan › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc de Cachan (2) ⚠️ | Cachan › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc de Vincennes ⚠️ | Vincennes › Paris-Est-Marne et Bois | 1 |
| Bois de Sucy-en-Brie ⚠️ | Sucy-en-Brie › Grand Paris Sud Est Avenir | 1 |
| Forêt de Saint-Maurice (2) ⚠️ | Saint-Maurice › Paris-Est-Marne et Bois | 1 |
| Forêt de Saint-Maurice (4) ⚠️ | Saint-Maurice › Paris-Est-Marne et Bois | 1 |
| Parc de Conflans ⚠️ | Charenton-le-Pont › Paris-Est-Marne et Bois | 1 |
| Forêt de Santeny (4) ⚠️ | Santeny › Grand Paris Sud Est Avenir | 1 |
| Forêt de Santeny (8) ⚠️ | Santeny › Grand Paris Sud Est Avenir | 1 |
| La Grande Mademoiselle ⚠️ | Choisy-le-Roi › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Forêt de La Queue-en-Brie (22) ⚠️ | La Queue-en-Brie › Grand Paris Sud Est Avenir | 1 |
| Forêt de La Queue-en-Brie (23) ⚠️ | La Queue-en-Brie › Grand Paris Sud Est Avenir | 1 |
| Forêt de La Queue-en-Brie (24) ⚠️ | La Queue-en-Brie › Grand Paris Sud Est Avenir | 1 |
| Forêt de La Queue-en-Brie (25) ⚠️ | La Queue-en-Brie › Grand Paris Sud Est Avenir | 1 |
| Square de l'Insurrection ⚠️ | Ivry-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc du Parangon ⚠️ | Joinville-le-Pont › Paris-Est-Marne et Bois | 1 |
| Parc des Hannetons ⚠️ | Maisons-Alfort › Paris-Est-Marne et Bois | 1 |
| Parc du Château ⚠️ | Rungis › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc de Cluny ⚠️ | Thiais › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc de Saint-Maurice (2) ⚠️ | Saint-Maurice › Paris-Est-Marne et Bois | 1 |
| Forêt de Saint-Maurice (9) ⚠️ | Saint-Maurice › Paris-Est-Marne et Bois | 1 |
| Forêt de Champigny-sur-Marne (5) ⚠️ | Champigny-sur-Marne › Paris-Est-Marne et Bois | 1 |
| Parc de Saint-Maur-des-Fossés (2) ⚠️ | Saint-Maur-des-Fossés › Paris-Est-Marne et Bois | 1 |
| Bois de Chevilly-Larue ⚠️ | Chevilly-Larue › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Ablon-sur-Seine ⚠️ | Ablon-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc du Coteau - Marcel Rosette ⚠️ | Vitry-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Jardin Michel Germa ⚠️ | Vitry-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc de Villeneuve-le-Roi ⚠️ | Villeneuve-le-Roi › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc de Gentilly ⚠️ | Gentilly › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc Dagobert ⚠️ | Nogent-sur-Marne › Paris-Est-Marne et Bois | 1 |
| Parc des Vinots ⚠️ | Mandres-les-Roses › Grand Paris Sud Est Avenir | 1 |
| Parc de Villeneuve-Saint-Georges ⚠️ | Villeneuve-Saint-Georges › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc Beauregard ⚠️ | Villeneuve-Saint-Georges › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Promenade du Fort ⚠️ | Ivry-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Square Maréchal Berthier ⚠️ | Boissy-Saint-Léger › Grand Paris Sud Est Avenir | 1 |
| Parc Monmousseau ⚠️ | Ivry-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Espace extérieurs cité Louis Bertrand ⚠️ | Ivry-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Forêt de Fresnes (2) ⚠️ | Fresnes › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Forêt de Santeny (11) ⚠️ | Santeny › Grand Paris Sud Est Avenir | 1 |
| Parc de Ivry-sur-Seine (4) ⚠️ | Ivry-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc de Ivry-sur-Seine (9) ⚠️ | Ivry-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc Watteau ⚠️ | Nogent-sur-Marne › Paris-Est-Marne et Bois | 1 |
| Parc de Santeny ⚠️ | Santeny › Grand Paris Sud Est Avenir | 1 |
| Jardin Elsa Triolet ⚠️ | Alfortville › Grand Paris Sud Est Avenir | 1 |
| Parc des Aulnes ⚠️ | Fresnes › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc du château de Réghat ⚠️ | Maisons-Alfort › Paris-Est-Marne et Bois | 1 |
| Parc du Moulin de Berny ⚠️ | Fresnes › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Esplanade de la Fraternité ⚠️ | Cachan › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Forêt de Chennevières-sur-Marne (5) ⚠️ | Chennevières-sur-Marne › Grand Paris Sud Est Avenir | 1 |
| Forêt de Sucy-en-Brie (3) ⚠️ | Sucy-en-Brie › Grand Paris Sud Est Avenir | 1 |
| Bois de Mandres-les-Roses ⚠️ | Mandres-les-Roses › Grand Paris Sud Est Avenir | 1 |
| Parc de Valenton ⚠️ | Valenton › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc de l'Alsacienne ⚠️ | Maisons-Alfort › Paris-Est-Marne et Bois | 1 |
| Parc Montaleau ⚠️ | Sucy-en-Brie › Grand Paris Sud Est Avenir | 1 |
| Square Anne Frank ⚠️ | Fontenay-sous-Bois › Paris-Est-Marne et Bois | 1 |
| Square Sœur Emmanuelle ⚠️ | Champigny-sur-Marne › Paris-Est-Marne et Bois | 1 |
| Parc du Perreux-sur-Marne (2) ⚠️ | Le Perreux-sur-Marne › Paris-Est-Marne et Bois | 1 |
| Parc de l'Haÿ-les-Roses (5) ⚠️ | L'Haÿ-les-Roses › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc de la mairie (2) ⚠️ | Maisons-Alfort › Paris-Est-Marne et Bois | 1 |
| Parc de l'Haÿ-les-Roses (7) ⚠️ | L'Haÿ-les-Roses › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois du Plessis-Trévise ⚠️ | Le Plessis-Trévise › Grand Paris Sud Est Avenir | 1 |
| Bords de Marne (3) ⚠️ | Maisons-Alfort › Paris-Est-Marne et Bois | 1 |
| Le verger de Brévannes ⚠️ | Limeil-Brévannes › Grand Paris Sud Est Avenir | 1 |
| Parc Municipal de la Bibliothèque ⚠️ | Villecresnes › Grand Paris Sud Est Avenir | 1 |
| Parc de Gentilly (6) ⚠️ | Gentilly › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Jardin sur le toit ⚠️ | Arcueil › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc de Thiais ⚠️ | Thiais › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Forêt de Thiais (3) ⚠️ | Thiais › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Saint-Maur-des-Fossés (2) ⚠️ | Saint-Maur-des-Fossés › Paris-Est-Marne et Bois | 1 |
| Forêt de Thiais (6) ⚠️ | Thiais › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc de l'Oiseau ⚠️ | Orly › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Hautes Bornes ⚠️ | Choisy-le-Roi › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc Émile Zola ⚠️ | Vitry-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Forêt de Boissy-Saint-Léger (3) ⚠️ | Boissy-Saint-Léger › Grand Paris Sud Est Avenir | 1 |
| Parc Saint-Pierre (2) ⚠️ | Alfortville › Grand Paris Sud Est Avenir | 1 |
| Forêt de Vitry-sur-Seine (2) ⚠️ | Vitry-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Forêt de Vitry-sur-Seine (7) ⚠️ | Vitry-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Talus des Grands Chemins ⚠️ | Fontenay-sous-Bois › Paris-Est-Marne et Bois | 1 |
| Square Jean Zay ⚠️ | Fontenay-sous-Bois › Paris-Est-Marne et Bois | 1 |
| Square extension de l'Hôtel de Ville ⚠️ | Fontenay-sous-Bois › Paris-Est-Marne et Bois | 1 |
| Parc de Chevilly-Larue ⚠️ | Chevilly-Larue › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Forêt de Mandres-les-Roses (3) ⚠️ | Mandres-les-Roses › Grand Paris Sud Est Avenir | 1 |
| Bois de Limeil-Brévannes (2) ⚠️ | Limeil-Brévannes › Grand Paris Sud Est Avenir | 1 |
| Forêt de La Queue-en-Brie (31) ⚠️ | La Queue-en-Brie › Grand Paris Sud Est Avenir | 1 |
| Forêt de Boissy-Saint-Léger (4) ⚠️ | Boissy-Saint-Léger › Grand Paris Sud Est Avenir | 1 |
| Forêt de Villecresnes (6) ⚠️ | Villecresnes › Grand Paris Sud Est Avenir | 1 |
| Forêt de Villecresnes (8) ⚠️ | Villecresnes › Grand Paris Sud Est Avenir | 1 |
| Forêt de Sucy-en-Brie (8) ⚠️ | Sucy-en-Brie › Grand Paris Sud Est Avenir | 1 |
| Parc de Sucy-en-Brie (3) ⚠️ | Sucy-en-Brie › Grand Paris Sud Est Avenir | 1 |
| Forêt de Sucy-en-Brie (9) ⚠️ | Sucy-en-Brie › Grand Paris Sud Est Avenir | 1 |
| Parc Saint-Martin ⚠️ | Limeil-Brévannes › Grand Paris Sud Est Avenir | 1 |
| Parc des Tourelles ⚠️ | Le Plessis-Trévise › Grand Paris Sud Est Avenir | 1 |
| Forêt de Thiais (10) ⚠️ | Thiais › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc de Ormesson-sur-Marne (2) ⚠️ | Ormesson-sur-Marne › Grand Paris Sud Est Avenir | 1 |
| Parc de Saint-Maur-des-Fossés (5) ⚠️ | Saint-Maur-des-Fossés › Paris-Est-Marne et Bois | 1 |
| Parc de Vitry-sur-Seine (8) ⚠️ | Vitry-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Forêt de Boissy-Saint-Léger (7) ⚠️ | Boissy-Saint-Léger › Grand Paris Sud Est Avenir | 1 |
| Forêt de Boissy-Saint-Léger (8) ⚠️ | Boissy-Saint-Léger › Grand Paris Sud Est Avenir | 1 |
| Bois de l'Haÿ-les-Roses (5) ⚠️ | L'Haÿ-les-Roses › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Créteil (22) ⚠️ | Créteil › Grand Paris Sud Est Avenir | 1 |
| Bois de Créteil (23) ⚠️ | Créteil › Grand Paris Sud Est Avenir | 1 |
| Parc de Valenton (3) ⚠️ | Valenton › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Square de la Mare ⚠️ | Villeneuve-Saint-Georges › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Boissy-Saint-Léger (2) ⚠️ | Boissy-Saint-Léger › Grand Paris Sud Est Avenir | 1 |
| Bois de Bry-sur-Marne (15) ⚠️ | Bry-sur-Marne › Paris-Est-Marne et Bois | 1 |
| Bois de Maisons-Alfort (11) ⚠️ | Maisons-Alfort › Paris-Est-Marne et Bois | 1 |
| Bois de Maisons-Alfort (20) ⚠️ | Maisons-Alfort › Paris-Est-Marne et Bois | 1 |
| Bois de Maisons-Alfort (26) ⚠️ | Maisons-Alfort › Paris-Est-Marne et Bois | 1 |
| Parc de Maisons-Alfort (3) ⚠️ | Maisons-Alfort › Paris-Est-Marne et Bois | 1 |
| Parc de Maisons-Alfort (5) ⚠️ | Maisons-Alfort › Paris-Est-Marne et Bois | 1 |
| Bois de Maisons-Alfort (34) ⚠️ | Maisons-Alfort › Paris-Est-Marne et Bois | 1 |
| Parc de Maisons-Alfort (6) ⚠️ | Maisons-Alfort › Paris-Est-Marne et Bois | 1 |
| Bois de Maisons-Alfort (44) ⚠️ | Maisons-Alfort › Paris-Est-Marne et Bois | 1 |
| Bois de l'Haÿ-les-Roses (6) ⚠️ | L'Haÿ-les-Roses › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Forêt de Villejuif (7) ⚠️ | Villejuif › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de l'Haÿ-les-Roses (7) ⚠️ | L'Haÿ-les-Roses › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Square des Justes Parmi les Nations ⚠️ | Ivry-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Créteil (38) ⚠️ | Créteil › Grand Paris Sud Est Avenir | 1 |
| Bois de Créteil (40) ⚠️ | Créteil › Grand Paris Sud Est Avenir | 1 |
| Bois de Créteil (42) ⚠️ | Créteil › Grand Paris Sud Est Avenir | 1 |
| Bois de Maisons-Alfort (56) ⚠️ | Maisons-Alfort › Paris-Est-Marne et Bois | 1 |
| Bois de Arcueil ⚠️ | Arcueil › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc de Arcueil (6) ⚠️ | Arcueil › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Fontenay-sous-Bois (2) ⚠️ | Fontenay-sous-Bois › Paris-Est-Marne et Bois | 1 |
| Forêt de Orly (4) ⚠️ | Orly › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc de Maisons-Alfort (9) ⚠️ | Maisons-Alfort › Paris-Est-Marne et Bois | 1 |
| Parc de Maisons-Alfort (11) ⚠️ | Maisons-Alfort › Paris-Est-Marne et Bois | 1 |
| Parc de Villejuif (2) ⚠️ | Villejuif › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Forêt de Ivry-sur-Seine ⚠️ | Ivry-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Vitry-sur-Seine (17) ⚠️ | Vitry-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Valenton (4) ⚠️ | Valenton › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Valenton (6) ⚠️ | Valenton › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Valenton (10) ⚠️ | Valenton › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Limeil-Brévannes (5) ⚠️ | Limeil-Brévannes › Grand Paris Sud Est Avenir | 1 |
| Bois de Limeil-Brévannes (7) ⚠️ | Limeil-Brévannes › Grand Paris Sud Est Avenir | 1 |
| Bois de Vitry-sur-Seine (30) ⚠️ | Vitry-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Vitry-sur-Seine (32) ⚠️ | Vitry-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Bonneuil-sur-Marne (2) ⚠️ | Bonneuil-sur-Marne › Grand Paris Sud Est Avenir | 1 |
| Bois de Bonneuil-sur-Marne (13) ⚠️ | Bonneuil-sur-Marne › Grand Paris Sud Est Avenir | 1 |
| Bois de Valenton (16) ⚠️ | Villeneuve-Saint-Georges › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Saint-Maurice (2) ⚠️ | Saint-Maurice › Paris-Est-Marne et Bois | 1 |
| Bois de Saint-Maurice (9) ⚠️ | Saint-Maurice › Paris-Est-Marne et Bois | 1 |
| Bois de Champigny-sur-Marne (7) ⚠️ | Champigny-sur-Marne › Paris-Est-Marne et Bois | 1 |
| Bois de Bry-sur-Marne (30) ⚠️ | Bry-sur-Marne › Paris-Est-Marne et Bois | 1 |
| Bois de Bry-sur-Marne (34) ⚠️ | Bry-sur-Marne › Paris-Est-Marne et Bois | 1 |
| Bois de Champigny-sur-Marne (23) ⚠️ | Champigny-sur-Marne › Paris-Est-Marne et Bois | 1 |
| Bois de Champigny-sur-Marne (27) ⚠️ | Champigny-sur-Marne › Paris-Est-Marne et Bois | 1 |
| Bois de Champigny-sur-Marne (30) ⚠️ | Champigny-sur-Marne › Paris-Est-Marne et Bois | 1 |
| Bois de Champigny-sur-Marne (35) ⚠️ | Champigny-sur-Marne › Paris-Est-Marne et Bois | 1 |
| Bois de Thiais (25) ⚠️ | Thiais › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Créteil (64) ⚠️ | Créteil › Grand Paris Sud Est Avenir | 1 |
| Bois de Créteil (66) ⚠️ | Créteil › Grand Paris Sud Est Avenir | 1 |
| Bois de Créteil (71) ⚠️ | Créteil › Grand Paris Sud Est Avenir | 1 |
| Bois de Saint-Maurice (12) ⚠️ | Saint-Maurice › Paris-Est-Marne et Bois | 1 |
| Bois de Champigny-sur-Marne (41) ⚠️ | Champigny-sur-Marne › Paris-Est-Marne et Bois | 1 |
| Bois de Champigny-sur-Marne (42) ⚠️ | Champigny-sur-Marne › Paris-Est-Marne et Bois | 1 |
| Bois de Chennevières-sur-Marne (4) ⚠️ | Chennevières-sur-Marne › Grand Paris Sud Est Avenir | 1 |
| Bois de Sucy-en-Brie (2) ⚠️ | Sucy-en-Brie › Grand Paris Sud Est Avenir | 1 |
| Bois de Boissy-Saint-Léger (4) ⚠️ | Boissy-Saint-Léger › Grand Paris Sud Est Avenir | 1 |
| Bois de Boissy-Saint-Léger (6) ⚠️ | Boissy-Saint-Léger › Grand Paris Sud Est Avenir | 1 |
| Bois de Ormesson-sur-Marne (2) ⚠️ | Ormesson-sur-Marne › Grand Paris Sud Est Avenir | 1 |
| Bois de Ormesson-sur-Marne (4) ⚠️ | Ormesson-sur-Marne › Grand Paris Sud Est Avenir | 1 |
| Bois de Chennevières-sur-Marne (15) ⚠️ | Chennevières-sur-Marne › Grand Paris Sud Est Avenir | 1 |
| Bois de Rungis (8) ⚠️ | Rungis › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Rungis (10) ⚠️ | Rungis › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Fresnes (8) ⚠️ | Fresnes › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Fresnes (17) ⚠️ | Fresnes › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Fresnes (21) ⚠️ | Fresnes › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Chevilly-Larue (11) ⚠️ | Chevilly-Larue › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Chevilly-Larue (21) ⚠️ | Chevilly-Larue › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Chevilly-Larue (26) ⚠️ | Chevilly-Larue › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc de Villeneuve-Saint-Georges (3) ⚠️ | Villeneuve-Saint-Georges › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Villeneuve-Saint-Georges (5) ⚠️ | Villeneuve-Saint-Georges › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Villeneuve-Saint-Georges (9) ⚠️ | Villeneuve-Saint-Georges › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Villeneuve-Saint-Georges (13) ⚠️ | Villeneuve-Saint-Georges › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Choisy-le-Roi (8) ⚠️ | Choisy-le-Roi › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Choisy-le-Roi (10) ⚠️ | Choisy-le-Roi › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Orly (2) ⚠️ | Orly › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Villeneuve-le-Roi (2) ⚠️ | Villeneuve-le-Roi › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Thiais (33) ⚠️ | Thiais › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Thiais (39) ⚠️ | Thiais › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Orly (17) ⚠️ | Orly › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Thiais (41) ⚠️ | Thiais › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de l'Haÿ-les-Roses (13) ⚠️ | L'Haÿ-les-Roses › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Villejuif (20) ⚠️ | Villejuif › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de l'Haÿ-les-Roses (19) ⚠️ | L'Haÿ-les-Roses › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Villejuif (22) ⚠️ | Villejuif › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Cachan (2) ⚠️ | Cachan › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Arcueil (15) ⚠️ | Gentilly › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Fontenay-sous-Bois (9) ⚠️ | Fontenay-sous-Bois › Paris-Est-Marne et Bois | 1 |
| Bois de Fontenay-sous-Bois (11) ⚠️ | Fontenay-sous-Bois › Paris-Est-Marne et Bois | 1 |
| Bois de Fontenay-sous-Bois (12) ⚠️ | Fontenay-sous-Bois › Paris-Est-Marne et Bois | 1 |
| Bois de Nogent-sur-Marne (7) ⚠️ | Nogent-sur-Marne › Paris-Est-Marne et Bois | 1 |
| Parc Jean Mermoz (3) ⚠️ | Orly › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Champigny-sur-Marne (60) ⚠️ | Champigny-sur-Marne › Paris-Est-Marne et Bois | 1 |
| Bois de Champigny-sur-Marne (68) ⚠️ | Champigny-sur-Marne › Paris-Est-Marne et Bois | 1 |
| Bois de Créteil (75) ⚠️ | Créteil › Grand Paris Sud Est Avenir | 1 |
| Parc de Créteil (6) ⚠️ | Créteil › Grand Paris Sud Est Avenir | 1 |
| Bois de Villeneuve-le-Roi (22) ⚠️ | Villeneuve-le-Roi › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Orly (20) ⚠️ | Orly › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Thiais (50) ⚠️ | Thiais › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Nogent-sur-Marne (9) ⚠️ | Nogent-sur-Marne › Paris-Est-Marne et Bois | 1 |
| Bois de Thiais (54) ⚠️ | Thiais › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Saint-Maur-des-Fossés (7) ⚠️ | Saint-Maur-des-Fossés › Paris-Est-Marne et Bois | 1 |
| Forêt de Périgny (2) ⚠️ | Périgny › Grand Paris Sud Est Avenir | 1 |
| Parc Beauséjour ⚠️ | Mandres-les-Roses › Grand Paris Sud Est Avenir | 1 |
| Forêt de Mandres-les-Roses (12) ⚠️ | Mandres-les-Roses › Grand Paris Sud Est Avenir | 1 |
| Bois de Limeil-Brévannes (9) ⚠️ | Limeil-Brévannes › Grand Paris Sud Est Avenir | 1 |
| Parc de Limeil-Brévannes (3) ⚠️ | Limeil-Brévannes › Grand Paris Sud Est Avenir | 1 |
| Forêt de Villeneuve-Saint-Georges (7) ⚠️ | Villeneuve-Saint-Georges › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Forêt de Villeneuve-Saint-Georges (8) ⚠️ | Villeneuve-Saint-Georges › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Forêt de Villeneuve-Saint-Georges (10) ⚠️ | Villeneuve-Saint-Georges › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Valenton (20) ⚠️ | Valenton › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Valenton (24) ⚠️ | Valenton › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Chevilly-Larue (31) ⚠️ | Chevilly-Larue › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc de Gentilly (10) ⚠️ | Gentilly › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Forêt de Vincennes ⚠️ | Vincennes › Paris-Est-Marne et Bois | 1 |
| Parc de Chevilly-Larue (5) ⚠️ | Chevilly-Larue › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Boissy-Saint-Léger (18) ⚠️ | Boissy-Saint-Léger › Grand Paris Sud Est Avenir | 1 |
| Bois de Limeil-Brévannes (13) ⚠️ | Limeil-Brévannes › Grand Paris Sud Est Avenir | 1 |
| Parc de Limeil-Brévannes (4) ⚠️ | Limeil-Brévannes › Grand Paris Sud Est Avenir | 1 |
| Bois de Orly (34) ⚠️ | Orly › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Bonneuil-sur-Marne (19) ⚠️ | Bonneuil-sur-Marne › Grand Paris Sud Est Avenir | 1 |
| Bois de Saint-Maur-des-Fossés (10) ⚠️ | Saint-Maur-des-Fossés › Paris-Est-Marne et Bois | 1 |
| Parc de Villecresnes (3) ⚠️ | Villecresnes › Grand Paris Sud Est Avenir | 1 |
| Parc de la mairie (3) ⚠️ | La Queue-en-Brie › Grand Paris Sud Est Avenir | 1 |
| Bois de Maisons-Alfort (60) ⚠️ | Maisons-Alfort › Paris-Est-Marne et Bois | 1 |
| Bois de Limeil-Brévannes (20) ⚠️ | Limeil-Brévannes › Grand Paris Sud Est Avenir | 1 |
| Bois de Choisy-le-Roi (22) ⚠️ | Choisy-le-Roi › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Créteil (84) ⚠️ | Créteil › Grand Paris Sud Est Avenir | 1 |
| Forêt de Mandres-les-Roses (16) ⚠️ | Mandres-les-Roses › Grand Paris Sud Est Avenir | 1 |
| Forêt de Périgny (8) ⚠️ | Mandres-les-Roses › Grand Paris Sud Est Avenir | 1 |
| Forêt de Périgny (14) ⚠️ | Périgny › Grand Paris Sud Est Avenir | 1 |
| Forêt de Périgny (21) ⚠️ | Périgny › Grand Paris Sud Est Avenir | 1 |
| Forêt de Villecresnes (22) ⚠️ | Villecresnes › Grand Paris Sud Est Avenir | 1 |
| Forêt de Périgny (25) ⚠️ | Périgny › Grand Paris Sud Est Avenir | 1 |
| Forêt de Périgny (26) ⚠️ | Périgny › Grand Paris Sud Est Avenir | 1 |
| Forêt de Mandres-les-Roses (29) ⚠️ | Mandres-les-Roses › Grand Paris Sud Est Avenir | 1 |
| Forêt de Santeny (23) ⚠️ | Santeny › Grand Paris Sud Est Avenir | 1 |
| Forêt de Santeny (28) ⚠️ | Santeny › Grand Paris Sud Est Avenir | 1 |
| Parc des Prairies du Fort ⚠️ | Vitry-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Forêt de Thiais (11) ⚠️ | Thiais › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Forêt de Thiais (13) ⚠️ | Thiais › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Forêt de Ablon-sur-Seine (4) ⚠️ | Ablon-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Thiais (69) ⚠️ | Thiais › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Santeny (3) ⚠️ | Santeny › Grand Paris Sud Est Avenir | 1 |
| Bois de Villeneuve-le-Roi (28) ⚠️ | Villeneuve-le-Roi › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Forêt de Ivry-sur-Seine (4) ⚠️ | Ivry-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Villecresnes (5) ⚠️ | Villecresnes › Grand Paris Sud Est Avenir | 1 |
| Bois de Choisy-le-Roi (31) ⚠️ | Villeneuve-Saint-Georges › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Choisy-le-Roi (32) ⚠️ | Choisy-le-Roi › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Bois de Créteil (105) ⚠️ | Créteil › Grand Paris Sud Est Avenir | 1 |
| Le Spot ⚠️ | Joinville-le-Pont › Paris-Est-Marne et Bois | 1 |
| Clos de Plaisance ⚠️ | Nogent-sur-Marne › Paris-Est-Marne et Bois | 1 |
| Square des Alliés ⚠️ | Ivry-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc de Ivry-sur-Seine (20) ⚠️ | Ivry-sur-Seine › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc de Villejuif (6) ⚠️ | Villejuif › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Parc Raspail ⚠️ | Cachan › Grand-Orly Seine Bièvre (Val-de-Marne) | 1 |
| Jardin Alexandra David-Néel ⚠️ | Saint-Mandé › Paris-Est-Marne et Bois | 1 |
| Parc des impressionnistes ⚠️ | La Queue-en-Brie › Grand Paris Sud Est Avenir | 1 |
| Forêt de Bry-sur-Marne (7) ⚠️ | Bry-sur-Marne › Paris-Est-Marne et Bois | 1 |
| Forêt de Santeny (35) ⚠️ | Santeny › Grand Paris Sud Est Avenir | 1 |
| Forêt de Santeny (36) ⚠️ | Santeny › Grand Paris Sud Est Avenir | 1 |
| Parc de Villiers-sur-Marne (2) ⚠️ | Villiers-sur-Marne › Paris-Est-Marne et Bois | 1 |

1 579 parc(s) plus petits qu'une cellule ne sont pas listés : la carte les dessine, mais ils n'offrent aucune cellule.

⚠️ 1983 parc(s) hors de la fenêtre 10–125 cellules (1982 trop petit(s), 1 trop grand(s)) : affichés sur la carte, mais ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| airport | 296 |
| military | 62 |
| prison | 7 |
| **Total déclaré** | **365** |
| dont dans une zone de ce territoire | 364 |

Le jeu de données couvre plus large que le territoire — il est produit à une échelle supérieure. Seules les cellules tombant dans une zone d'ici pèsent sur un pourcentage.

### Zones concernées

| Zone | Cellules exclues |
|---|---:|
| Villeneuve-le-Roi | 154 |
| Orly | 141 |
| Maisons-Alfort | 15 |
| Arcueil | 11 |
| Fontenay-sous-Bois | 8 |
| Fresnes | 7 |
| Le Kremlin-Bicêtre | 7 |
| Villeneuve-Saint-Georges | 6 |
| Ivry-sur-Seine | 6 |
| Limeil-Brévannes | 4 |
| Saint-Mandé | 3 |
| Valenton | 2 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
