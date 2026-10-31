# Seine-Saint-Denis

Pack `fr-seine-saint-denis` · version 1.0.0 · grille 200 m · France › Île-de-France

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 13 523 |
| dont restreintes (aéroport, militaire, prison) | 615 |
| dont sans chemin (aucune voie à moins de 60 m) | 89 |
| dont en forêt, sans chemin non plus | 26 |
| dont traversées par un cours d'eau, sans chemin non plus | 1 |
| Cellules retirées par le masque d'eau | 168 |
| Villes | 39 |
| Arrondissements et quartiers | 0 |
| Îles | 4 |
| Parcs | 1 589 |

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
| Est Ensemble | 2 257 | somme de 9 villes |
| Grand Paris - Grand Est | 4 118 | somme de 14 villes |
| Paris Terres d'Envol | 4 495 | somme de 8 villes |
| Plaine Commune | 2 655 | somme de 8 villes |

Une île *composite* n'a pas de cellules à elle : sa progression est la somme de ses villes, et ses cellules ne lui sont jamais rattachées directement — elles compteraient deux fois.

## Villes (39)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Sans chemin | Parcs |
|---|---:|---:|---:|---:|---:|---:|---:|
| Tremblay-en-France | 1 313 | 16 | 1 297 | 460 | **837** | 75 (9 %) | 57 |
| Aulnay-sous-Bois | 940 | 6 | 934 | 0 | **934** |  | 102 |
| Saint-Denis | 914 | 14 | 900 | 7 | **893** | 1 (0 %) | 157 |
| Noisy-le-Grand | 758 | 9 | 749 | 0 | **749** |  | 214 |
| Villepinte | 596 | 4 | 592 | 3 | **589** |  | 54 |
| Montreuil | 510 | 0 | 510 | 0 | **510** |  | 49 |
| Le Blanc-Mesnil | 467 | 2 | 465 | 0 | **465** |  | 33 |
| Drancy | 444 | 0 | 444 | 0 | **444** | 2 (0 %) | 19 |
| Livry-Gargan | 432 | 1 | 431 | 0 | **431** | 3 (1 %) | 29 |
| La Courneuve | 434 | 11 | 423 | 0 | **423** |  | 66 |
| Sevran | 419 | 4 | 415 | 0 | **415** | 5 (1 %) | 29 |
| Gagny | 405 | 2 | 403 | 0 | **403** |  | 44 |
| Bobigny | 395 | 2 | 393 | 0 | **393** |  | 22 |
| Neuilly-sur-Marne | 399 | 13 | 386 | 0 | **386** | 1 (0 %) | 53 |
| Rosny-sous-Bois | 343 | 0 | 343 | 14 | **329** |  | 38 |
| Aubervilliers | 334 | 4 | 330 | 0 | **330** |  | 41 |
| Montfermeil | 312 | 0 | 312 | 0 | **312** |  | 13 |
| Bondy | 312 | 1 | 311 | 0 | **311** |  | 40 |
| Stains | 311 | 1 | 310 | 0 | **310** |  | 46 |
| Noisy-le-Sec | 293 | 1 | 292 | 0 | **292** |  | 69 |
| Pantin | 291 | 2 | 289 | 0 | **289** |  | 43 |
| Épinay-sur-Seine | 265 | 11 | 254 | 0 | **254** |  | 33 |
| Saint-Ouen-sur-Seine | 252 | 11 | 241 | 0 | **241** |  | 31 |
| Coubron | 240 | 5 | 235 | 0 | **235** |  | 16 |
| Villemomble | 235 | 0 | 235 | 0 | **235** |  | 36 |
| Clichy-sous-Bois | 227 | 0 | 227 | 0 | **227** |  | 11 |
| Dugny | 226 | 3 | 223 | 113 | **110** |  | 20 |
| Vaujours | 218 | 0 | 218 | 0 | **218** | 2 (1 %) | 9 |
| Neuilly-Plaisance | 200 | 1 | 199 | 0 | **199** |  | 13 |
| Romainville | 199 | 0 | 199 | 11 | **188** |  | 19 |
| Les Pavillons-sous-Bois | 168 | 4 | 164 | 0 | **164** |  | 5 |
| Bagnolet | 146 | 0 | 146 | 0 | **146** |  | 40 |
| Villetaneuse | 133 | 0 | 133 | 0 | **133** |  | 29 |
| Le Raincy | 128 | 1 | 127 | 0 | **127** |  | 5 |
| Le Bourget | 125 | 0 | 125 | 7 | **118** |  | 16 |
| Gournay-sur-Marne | 93 | 4 | 89 | 0 | **89** |  | 37 |
| Les Lilas | 75 | 0 | 75 | 0 | **75** |  | 11 |
| L'Île-Saint-Denis | 99 | 35 | 64 | 0 | **64** |  | 13 |
| Le Pré-Saint-Gervais | 42 | 0 | 42 | 0 | **42** |  | 8 |

## Parcs (1589)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Parc départemental Georges-Valbon ⚠️ | La Courneuve › Plaine Commune | 171 |
| bois du Luzard ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 155 |
| Parc départemental du Sausset | Aulnay-sous-Bois › Paris Terres d'Envol | 112 |
| Forêt Régionale de Bondy | Coubron › Grand Paris - Grand Est | 91 |
| Parc forestier de la Poudrerie | Sevran › Paris Terres d'Envol | 65 |
| Bois de Bernouille | Coubron › Grand Paris - Grand Est | 63 |
| Forêt de Villepinte (17) | Villepinte › Paris Terres d'Envol | 52 |
| Bois du Renard | Livry-Gargan › Grand Paris - Grand Est | 51 |
| Parc départemental de la Haute-Île | Neuilly-sur-Marne › Grand Paris - Grand Est | 38 |
| Parc des Coteaux d'Avron | Neuilly-Plaisance › Grand Paris - Grand Est | 29 |
| Base de loisirs de la Corniche des Forts | Romainville › Est Ensemble | 28 |
| Bois de la Couronne | Clichy-sous-Bois › Grand Paris - Grand Est | 20 |
| Parc des 33 Hectares | Neuilly-sur-Marne › Grand Paris - Grand Est | 19 |
| Parc Robert Ballanger | Aulnay-sous-Bois › Paris Terres d'Envol | 19 |
| Forêt de Gagny (27) | Gagny › Grand Paris - Grand Est | 19 |
| Bois Saint-Denis | Tremblay-en-France › Paris Terres d'Envol | 16 |
| Bois départemental des Sablons | Sevran › Paris Terres d'Envol | 16 |
| Parc de l'Île Saint-Denis | L'Île-Saint-Denis › Plaine Commune | 14 |
| Parc départemental Jean-Moulin - Les Guilands | Montreuil › Est Ensemble | 14 |
| Parc Anne de Kiev | Le Blanc-Mesnil › Paris Terres d'Envol | 13 |
| Espace naturel régional de la Butte Pinson | Villetaneuse › Plaine Commune | 13 |
| Parc départemental de la Fosse Maussoin | Clichy-sous-Bois › Grand Paris - Grand Est | 12 |
| Parc des Beaumonts | Montreuil › Est Ensemble | 12 |
| La Morichonne | Vaujours › Grand Paris - Grand Est | 11 |
| Parc de la Légion d'Honneur | Saint-Denis › Plaine Commune | 11 |
| Aire des Vents | Dugny › Paris Terres d'Envol | 11 |
| Parc départemental de la Bergère | Bobigny › Est Ensemble | 11 |
| Bois départemental de la Tussion | Villepinte › Paris Terres d'Envol | 11 |
| Bois de La Courneuve (12) | La Courneuve › Plaine Commune | 10 |
| Bois de Dugny (2) | Dugny › Paris Terres d'Envol | 10 |
| Parc Montreau ⚠️ | Montreuil › Est Ensemble | 9 |
| Forêt de Vaujours (4) ⚠️ | Vaujours › Grand Paris - Grand Est | 9 |
| Parc du Château Bleu ⚠️ | Tremblay-en-France › Paris Terres d'Envol | 9 |
| Forêt de Villepinte (21) ⚠️ | Villepinte › Paris Terres d'Envol | 9 |
| Forêt de La Courneuve (4) ⚠️ | La Courneuve › Plaine Commune | 8 |
| Forêt de La Courneuve (9) ⚠️ | La Courneuve › Plaine Commune | 8 |
| Parc Forestier du Bois de l’Étoile ⚠️ | Gagny › Grand Paris - Grand Est | 8 |
| Forêt de Romainville ⚠️ | Romainville › Est Ensemble | 8 |
| Bois de La Courneuve (3) ⚠️ | La Courneuve › Plaine Commune | 8 |
| Bois de Stains ⚠️ | Dugny › Paris Terres d'Envol | 8 |
| Bois de l'Étoile ⚠️ | Gagny › Grand Paris - Grand Est | 8 |
| Forêt de Sevran (12) ⚠️ | Sevran › Paris Terres d'Envol | 8 |
| Forêt de Aulnay-sous-Bois (60) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 8 |
| Forêt de Vaujours ⚠️ | Vaujours › Grand Paris - Grand Est | 7 |
| Parc Georges-Pompidou ⚠️ | Livry-Gargan › Grand Paris - Grand Est | 7 |
| Forêt de Neuilly-sur-Marne (18) ⚠️ | Neuilly-sur-Marne › Grand Paris - Grand Est | 7 |
| Terrain des Essences ⚠️ | La Courneuve › Plaine Commune | 7 |
| Parc Nature du Plateau d'Avron ⚠️ | Rosny-sous-Bois › Grand Paris - Grand Est | 7 |
| Forêt de Tremblay-en-France (14) ⚠️ | Tremblay-en-France › Paris Terres d'Envol | 7 |
| Parc de la République (2) ⚠️ | Les Lilas › Est Ensemble | 7 |
| Forêt de Romainville (9) ⚠️ | Les Lilas › Est Ensemble | 7 |
| Parc Lefèvre ⚠️ | Livry-Gargan › Grand Paris - Grand Est | 6 |
| Bois de Bondy ⚠️ | Bondy › Est Ensemble | 6 |
| Parc de Neuilly-sur-Marne ⚠️ | Neuilly-sur-Marne › Grand Paris - Grand Est | 6 |
| Forêt de La Courneuve ⚠️ | La Courneuve › Plaine Commune | 6 |
| Parc de la Ferme de Montceleux ⚠️ | Sevran › Paris Terres d'Envol | 6 |
| Forêt de Vaujours (2) ⚠️ | Vaujours › Grand Paris - Grand Est | 6 |
| Grand Parc des Docks de Saint-Ouen ⚠️ | Saint-Ouen-sur-Seine › Plaine Commune | 6 |
| Parc des Friches ⚠️ | Livry-Gargan › Grand Paris - Grand Est | 6 |
| Forêt de Clichy-sous-Bois (3) ⚠️ | Clichy-sous-Bois › Grand Paris - Grand Est | 6 |
| Bois de Stains (22) ⚠️ | Stains › Plaine Commune | 6 |
| Forêt de Tremblay-en-France (15) ⚠️ | Tremblay-en-France › Paris Terres d'Envol | 6 |
| Parc paysager de la friche Kodak ⚠️ | Sevran › Paris Terres d'Envol | 6 |
| Bois de Aubervilliers ⚠️ | Aubervilliers › Plaine Commune | 5 |
| Forêt de Gagny (2) ⚠️ | Gagny › Grand Paris - Grand Est | 5 |
| Forêt de Tremblay-en-France ⚠️ | Tremblay-en-France › Paris Terres d'Envol | 5 |
| Parc Arboretum ⚠️ | Montfermeil › Grand Paris - Grand Est | 5 |
| Parc de Villepinte ⚠️ | Villepinte › Paris Terres d'Envol | 5 |
| Bois de Livry-Gargan ⚠️ | Livry-Gargan › Grand Paris - Grand Est | 5 |
| Forêt de Villepinte (8) ⚠️ | Villepinte › Paris Terres d'Envol | 5 |
| Forêt de Saint-Denis (15) ⚠️ | Saint-Denis › Plaine Commune | 5 |
| Parc de Romainville (3) ⚠️ | Romainville › Est Ensemble | 5 |
| Forêt de Villetaneuse (25) ⚠️ | Villetaneuse › Plaine Commune | 5 |
| Forêt de Saint-Denis (20) ⚠️ | Saint-Denis › Plaine Commune | 5 |
| Forêt de Villepinte (18) ⚠️ | Villepinte › Paris Terres d'Envol | 5 |
| Forêt de Villepinte (24) ⚠️ | Villepinte › Paris Terres d'Envol | 5 |
| Forêt de Neuilly-sur-Marne (9) ⚠️ | Neuilly-sur-Marne › Grand Paris - Grand Est | 4 |
| Parc de la Mairie (2) ⚠️ | Clichy-sous-Bois › Grand Paris - Grand Est | 4 |
| Bois d'Eguisy ⚠️ | Vaujours › Grand Paris - Grand Est | 4 |
| Parc de Stains ⚠️ | Stains › Plaine Commune | 4 |
| Forêt de La Courneuve (3) ⚠️ | La Courneuve › Plaine Commune | 4 |
| Parc des Saules ⚠️ | Épinay-sur-Seine › Plaine Commune | 4 |
| Forêt de Aulnay-sous-Bois (29) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 4 |
| Parc de Ladoucette ⚠️ | Drancy › Paris Terres d'Envol | 4 |
| Forêt de Montreuil ⚠️ | Montreuil › Est Ensemble | 4 |
| Parc de Noisy-le-Sec ⚠️ | Noisy-le-Sec › Est Ensemble | 4 |
| Bois du Blanc-Mesnil (6) ⚠️ | Le Blanc-Mesnil › Paris Terres d'Envol | 4 |
| Forêt de Rosny-sous-Bois (12) ⚠️ | Rosny-sous-Bois › Grand Paris - Grand Est | 4 |
| Parc Madeleine Riffaud ⚠️ | Saint-Denis › Plaine Commune | 4 |
| Forêt de La Courneuve (10) ⚠️ | La Courneuve › Plaine Commune | 4 |
| Forêt de Villepinte (26) ⚠️ | Villepinte › Paris Terres d'Envol | 4 |
| Parc Jean Decesari ⚠️ | Rosny-sous-Bois › Grand Paris - Grand Est | 3 |
| Bois des 33 Hectares ⚠️ | Neuilly-sur-Marne › Grand Paris - Grand Est | 3 |
| Forêt de Noisy-le-Grand ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 3 |
| Bois des Charcalets ⚠️ | Rosny-sous-Bois › Grand Paris - Grand Est | 3 |
| Bois des Yvris ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 3 |
| Forêt de Neuilly-sur-Marne (7) ⚠️ | Neuilly-sur-Marne › Grand Paris - Grand Est | 3 |
| Forêt de Gagny (3) ⚠️ | Gagny › Grand Paris - Grand Est | 3 |
| Forêt de Neuilly-sur-Marne (11) ⚠️ | Neuilly-sur-Marne › Grand Paris - Grand Est | 3 |
| Square Lucien Brun ⚠️ | Aubervilliers › Plaine Commune | 3 |
| Forêt de Tremblay-en-France (3) ⚠️ | Tremblay-en-France › Paris Terres d'Envol | 3 |
| Forêt de Neuilly-sur-Marne (19) ⚠️ | Neuilly-sur-Marne › Grand Paris - Grand Est | 3 |
| Parc Jean-Pierre Jousseaume ⚠️ | Montfermeil › Grand Paris - Grand Est | 3 |
| Forêt de Gagny (5) ⚠️ | Gagny › Grand Paris - Grand Est | 3 |
| Forêt de Clichy-sous-Bois (2) ⚠️ | Clichy-sous-Bois › Grand Paris - Grand Est | 3 |
| Parc Pierre Bérégovoy ⚠️ | Livry-Gargan › Grand Paris - Grand Est | 3 |
| Forêt de l'Île-Saint-Denis ⚠️ | L'Île-Saint-Denis › Plaine Commune | 3 |
| Bois de l'Île-Saint-Denis (3) ⚠️ | L'Île-Saint-Denis › Plaine Commune | 3 |
| Bois de Noisy-le-Grand (67) ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 3 |
| Parc de la Pointe Sud ⚠️ | Tremblay-en-France › Paris Terres d'Envol | 3 |
| Parc de Gournay-sur-Marne (6) ⚠️ | Gournay-sur-Marne › Grand Paris - Grand Est | 3 |
| Bois de Saint-Denis (11) ⚠️ | Saint-Denis › Plaine Commune | 3 |
| Bois de Stains (5) ⚠️ | Stains › Plaine Commune | 3 |
| Plaine des Cerisiers ⚠️ | Neuilly-sur-Marne › Grand Paris - Grand Est | 3 |
| Bois de Neuilly-sur-Marne (5) ⚠️ | Neuilly-sur-Marne › Grand Paris - Grand Est | 3 |
| Parc de la Pépinière ⚠️ | Villepinte › Paris Terres d'Envol | 3 |
| Parc de la Butte Verte ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 3 |
| Parc Pierre Bérégovoy (2) ⚠️ | Livry-Gargan › Grand Paris - Grand Est | 3 |
| Forêt de Tremblay-en-France (16) ⚠️ | Tremblay-en-France › Paris Terres d'Envol | 3 |
| Parc de la Garenne ⚠️ | Villemomble › Grand Paris - Grand Est | 2 |
| Forêt de Neuilly-Plaisance ⚠️ | Neuilly-Plaisance › Grand Paris - Grand Est | 2 |
| Parc Gustave Courbet ⚠️ | Gagny › Grand Paris - Grand Est | 2 |
| Parc de la Mairie ⚠️ | Livry-Gargan › Grand Paris - Grand Est | 2 |
| Forêt de Livry-Gargan ⚠️ | Livry-Gargan › Grand Paris - Grand Est | 2 |
| Parc de Gournay-sur-Marne ⚠️ | Gournay-sur-Marne › Grand Paris - Grand Est | 2 |
| Forêt de Sevran ⚠️ | Sevran › Paris Terres d'Envol | 2 |
| Forêt de Aulnay-sous-Bois (4) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 2 |
| Forêt de Aulnay-sous-Bois (6) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 2 |
| Forêt de Aulnay-sous-Bois (11) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 2 |
| Bois Médéric ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 2 |
| Parc Louis Armand ⚠️ | Sevran › Paris Terres d'Envol | 2 |
| Forêt de Saint-Denis ⚠️ | Saint-Denis › Plaine Commune | 2 |
| Forêt de Aulnay-sous-Bois (20) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 2 |
| Forêt de Tremblay-en-France (2) ⚠️ | Tremblay-en-France › Paris Terres d'Envol | 2 |
| Mail Maurice de Fontenay ⚠️ | La Courneuve › Plaine Commune | 2 |
| Parc des Sœurs ⚠️ | Sevran › Paris Terres d'Envol | 2 |
| Parc du Bassin de la Maltournée ⚠️ | Saint-Denis › Plaine Commune | 2 |
| Arboretum du Bois de l'Étoile ⚠️ | Gagny › Grand Paris - Grand Est | 2 |
| Forêt de Gagny (4) ⚠️ | Gagny › Grand Paris - Grand Est | 2 |
| Parc d'orgemont ⚠️ | Épinay-sur-Seine › Plaine Commune | 2 |
| Forêt de Clichy-sous-Bois ⚠️ | Clichy-sous-Bois › Grand Paris - Grand Est | 2 |
| Forêt de Villetaneuse ⚠️ | Villetaneuse › Plaine Commune | 2 |
| Bois de l'Île-Saint-Denis (2) ⚠️ | L'Île-Saint-Denis › Plaine Commune | 2 |
| Parc de Romainville ⚠️ | Romainville › Est Ensemble | 2 |
| Parc de Gournay-sur-Marne (3) ⚠️ | Gournay-sur-Marne › Grand Paris - Grand Est | 2 |
| Bois du Blanc-Mesnil (7) ⚠️ | Le Blanc-Mesnil › Paris Terres d'Envol | 2 |
| Bois de La Courneuve (16) ⚠️ | La Courneuve › Plaine Commune | 2 |
| Bois de Dugny ⚠️ | Dugny › Paris Terres d'Envol | 2 |
| Bois de Saint-Denis (12) ⚠️ | Saint-Denis › Plaine Commune | 2 |
| Bois de Stains (16) ⚠️ | Stains › Plaine Commune | 2 |
| Forêt de Noisy-le-Sec (2) ⚠️ | Romainville › Est Ensemble | 2 |
| Bois de Aulnay-sous-Bois (3) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 2 |
| Bois de Villepinte (6) ⚠️ | Villepinte › Paris Terres d'Envol | 2 |
| Bois de Villepinte (7) ⚠️ | Villepinte › Paris Terres d'Envol | 2 |
| Bois de Villepinte (10) ⚠️ | Villepinte › Paris Terres d'Envol | 2 |
| Parc de Tremblay-en-France ⚠️ | Tremblay-en-France › Paris Terres d'Envol | 2 |
| Parc de Saint-Denis (40) ⚠️ | Saint-Denis › Plaine Commune | 2 |
| Bois de Noisy-le-Sec (8) ⚠️ | Romainville › Est Ensemble | 2 |
| Bois de Romainville ⚠️ | Romainville › Est Ensemble | 2 |
| Bois de Aulnay-sous-Bois (8) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 2 |
| Forêt de Noisy-le-Grand (47) ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 2 |
| Bois de Bobigny (5) ⚠️ | Bobigny › Est Ensemble | 2 |
| Parc des Guillaumes (2) ⚠️ | Noisy-le-Sec › Est Ensemble | 2 |
| Forêt de Tremblay-en-France (19) ⚠️ | Tremblay-en-France › Paris Terres d'Envol | 2 |
| Forêt de Tremblay-en-France (20) ⚠️ | Tremblay-en-France › Paris Terres d'Envol | 2 |
| Forêt de Tremblay-en-France (24) ⚠️ | Tremblay-en-France › Paris Terres d'Envol | 2 |
| Forêt de Sevran (15) ⚠️ | Sevran › Paris Terres d'Envol | 2 |
| Forêt de Aulnay-sous-Bois (59) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 2 |
| Forêt de Villepinte (25) ⚠️ | Villepinte › Paris Terres d'Envol | 2 |
| Forêt de Aulnay-sous-Bois (63) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 2 |
| Square Constantin Balmont ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 1 |
| Square Richard Gardebled ⚠️ | Rosny-sous-Bois › Grand Paris - Grand Est | 1 |
| Forêt de Noisy-le-Grand (2) ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 1 |
| Forêt de Villemomble ⚠️ | Neuilly-Plaisance › Grand Paris - Grand Est | 1 |
| Forêt de Neuilly-sur-Marne (5) ⚠️ | Neuilly-sur-Marne › Grand Paris - Grand Est | 1 |
| Forêt de Neuilly-sur-Marne (6) ⚠️ | Neuilly-sur-Marne › Grand Paris - Grand Est | 1 |
| Le Bois Lumière ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 1 |
| Forêt de Noisy-le-Grand (4) ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 1 |
| Parc de Bobigny ⚠️ | Bobigny › Est Ensemble | 1 |
| Parc de Noisy-le-Grand ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 1 |
| Parc Abel-Mézières ⚠️ | Saint-Ouen-sur-Seine › Plaine Commune | 1 |
| Bois de Noisy-le-Grand ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 1 |
| Parc municipal Lucie-Aubrac ⚠️ | Les Lilas › Est Ensemble | 1 |
| Forêt de Gagny ⚠️ | Gagny › Grand Paris - Grand Est | 1 |
| Forêt de Neuilly-sur-Marne (12) ⚠️ | Neuilly-sur-Marne › Grand Paris - Grand Est | 1 |
| Forêt de Neuilly-sur-Marne (13) ⚠️ | Neuilly-sur-Marne › Grand Paris - Grand Est | 1 |
| Forêt de Neuilly-sur-Marne (14) ⚠️ | Neuilly-sur-Marne › Grand Paris - Grand Est | 1 |
| Forêt de Noisy-le-Grand (16) ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 1 |
| Forêt de Noisy-le-Grand (21) ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 1 |
| Forêt de Noisy-le-Grand (22) ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 1 |
| Square Stalingrad ⚠️ | Aubervilliers › Plaine Commune | 1 |
| Forêt de Pantin ⚠️ | Pantin › Est Ensemble | 1 |
| Parc de la République ⚠️ | Saint-Denis › Plaine Commune | 1 |
| Parc Josette et Maurice Audin ⚠️ | Bagnolet › Est Ensemble | 1 |
| Parc Diderot ⚠️ | Pantin › Est Ensemble | 1 |
| Espaces Verts des Courtillères ⚠️ | Pantin › Est Ensemble | 1 |
| Parc de la Bergère ⚠️ | Bobigny › Est Ensemble | 1 |
| Forêt de Neuilly-sur-Marne (16) ⚠️ | Neuilly-sur-Marne › Grand Paris - Grand Est | 1 |
| Forêt de Aulnay-sous-Bois (2) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 1 |
| Forêt de Aulnay-sous-Bois (5) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 1 |
| Forêt de La Courneuve (6) ⚠️ | La Courneuve › Plaine Commune | 1 |
| Parc des Béatus ⚠️ | Épinay-sur-Seine › Plaine Commune | 1 |
| Parc de Bagnolet ⚠️ | Bagnolet › Est Ensemble | 1 |
| Parc du Blanc-Mesnil ⚠️ | Le Blanc-Mesnil › Paris Terres d'Envol | 1 |
| Parc Gainville ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 1 |
| Parc Roger Badier ⚠️ | Sevran › Paris Terres d'Envol | 1 |
| Square Féry ⚠️ | Saint-Denis › Plaine Commune | 1 |
| Jardin Communal Danielle Casanova ⚠️ | Stains › Plaine Commune | 1 |
| Forêt de Montfermeil ⚠️ | Montfermeil › Grand Paris - Grand Est | 1 |
| Forêt de Montfermeil (2) ⚠️ | Montfermeil › Grand Paris - Grand Est | 1 |
| Forêt de Coubron (3) ⚠️ | Coubron › Grand Paris - Grand Est | 1 |
| Forêt de Aulnay-sous-Bois (15) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 1 |
| Forêt de Aulnay-sous-Bois (25) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 1 |
| Forêt de Aulnay-sous-Bois (27) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 1 |
| Forêt de Aulnay-sous-Bois (34) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 1 |
| Forêt de Aulnay-sous-Bois (36) ⚠️ | Villepinte › Paris Terres d'Envol | 1 |
| Forêt de Aulnay-sous-Bois (37) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 1 |
| Forêt de Villepinte (3) ⚠️ | Villepinte › Paris Terres d'Envol | 1 |
| Forêt de Aulnay-sous-Bois (38) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 1 |
| Forêt de Villepinte (4) ⚠️ | Villepinte › Paris Terres d'Envol | 1 |
| Forêt de Aulnay-sous-Bois (41) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 1 |
| Forêt de Aulnay-sous-Bois (42) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 1 |
| Parc de Saint-Denis (2) ⚠️ | Saint-Denis › Plaine Commune | 1 |
| Parc de Saint-Denis (3) ⚠️ | Saint-Denis › Plaine Commune | 1 |
| Parc de Saint-Denis (4) ⚠️ | Saint-Denis › Plaine Commune | 1 |
| Parc Pescarolo ⚠️ | Montfermeil › Grand Paris - Grand Est | 1 |
| Forêt de Montfermeil (3) ⚠️ | Montfermeil › Grand Paris - Grand Est | 1 |
| Butte Verte ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 1 |
| Square Pierrette Duffourt ⚠️ | Gournay-sur-Marne › Grand Paris - Grand Est | 1 |
| Parc de Aulnay-sous-Bois (2) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 1 |
| Parc de Aulnay-sous-Bois (4) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 1 |
| Parc de Sevran (2) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 1 |
| Parc de Sevran (3) ⚠️ | Sevran › Paris Terres d'Envol | 1 |
| Parc Bigottini ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 1 |
| Parc Jean Mermoz ⚠️ | Villemomble › Grand Paris - Grand Est | 1 |
| Parc Joseph Bologne ⚠️ | Le Blanc-Mesnil › Paris Terres d'Envol | 1 |
| Parc Vincent-Auriol ⚠️ | Livry-Gargan › Grand Paris - Grand Est | 1 |
| Jardin des Sources ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 1 |
| Parc du Blanc-Mesnil (2) ⚠️ | Le Blanc-Mesnil › Paris Terres d'Envol | 1 |
| Bois de Aulnay-sous-Bois (2) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 1 |
| Bois de Neuilly-sur-Marne (2) ⚠️ | Neuilly-sur-Marne › Grand Paris - Grand Est | 1 |
| Bois de Neuilly-sur-Marne (3) ⚠️ | Neuilly-sur-Marne › Grand Paris - Grand Est | 1 |
| Parc Guérin ⚠️ | Neuilly-sur-Marne › Grand Paris - Grand Est | 1 |
| Parc Pierre Lihou ⚠️ | Épinay-sur-Seine › Plaine Commune | 1 |
| Forêt de Coubron (6) ⚠️ | Coubron › Grand Paris - Grand Est | 1 |
| Forêt de Coubron (8) ⚠️ | Coubron › Grand Paris - Grand Est | 1 |
| Forêt de Coubron (9) ⚠️ | Coubron › Grand Paris - Grand Est | 1 |
| Parc de la Mare à la Veuve Honorine de Beauvais ⚠️ | Bondy › Est Ensemble | 1 |
| Parc de la Manufacture des tabacs ⚠️ | Pantin › Est Ensemble | 1 |
| Square Frantz Fanon ⚠️ | Saint-Denis › Plaine Commune | 1 |
| Square Alcacer do Sal ⚠️ | Bondy › Est Ensemble | 1 |
| Square de la Libération ⚠️ | Drancy › Paris Terres d'Envol | 1 |
| Forêt de Aulnay-sous-Bois (47) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 1 |
| Forêt de Aulnay-sous-Bois (50) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 1 |
| Forêt du Bourget (3) ⚠️ | Le Bourget › Paris Terres d'Envol | 1 |
| Square Jean Jaurès ⚠️ | Noisy-le-Sec › Est Ensemble | 1 |
| Mail Jean Rostand ⚠️ | Bobigny › Est Ensemble | 1 |
| Square du Pré Gobelin ⚠️ | Tremblay-en-France › Paris Terres d'Envol | 1 |
| Parc de Épinay-sur-Seine ⚠️ | Épinay-sur-Seine › Plaine Commune | 1 |
| Forêt de Saint-Denis (2) ⚠️ | Saint-Denis › Plaine Commune | 1 |
| Square Blumenthal ⚠️ | Épinay-sur-Seine › Plaine Commune | 1 |
| Square Cézanne ⚠️ | Saint-Denis › Plaine Commune | 1 |
| La prairie ⚠️ | Saint-Denis › Plaine Commune | 1 |
| Forêt de Saint-Denis (3) ⚠️ | Saint-Denis › Plaine Commune | 1 |
| Forêt de Saint-Denis (6) ⚠️ | Saint-Denis › Plaine Commune | 1 |
| Forêt de Montreuil (3) ⚠️ | Montreuil › Est Ensemble | 1 |
| Parc Georges Clémenceau ⚠️ | Livry-Gargan › Grand Paris - Grand Est | 1 |
| Parc Joanny Berlioz ⚠️ | Épinay-sur-Seine › Plaine Commune | 1 |
| Jardin Ecole ⚠️ | Montreuil › Est Ensemble | 1 |
| Parc Stalingrad ⚠️ | Pantin › Est Ensemble | 1 |
| Parc de Pantin (11) ⚠️ | Pantin › Est Ensemble | 1 |
| Square des Francs-Moisins ⚠️ | Saint-Denis › Plaine Commune | 1 |
| Bois de Saint-Denis (5) ⚠️ | Saint-Denis › Plaine Commune | 1 |
| Parc de Saint-Denis (12) ⚠️ | Saint-Denis › Plaine Commune | 1 |
| Square des Clos ⚠️ | La Courneuve › Plaine Commune | 1 |
| Square Gabriel Péri ⚠️ | Saint-Denis › Plaine Commune | 1 |
| Square Charles de Gaulle ⚠️ | Le Bourget › Paris Terres d'Envol | 1 |
| Parc de Montreuil (3) ⚠️ | Montreuil › Est Ensemble | 1 |
| Mare Bris ⚠️ | Montreuil › Est Ensemble | 1 |
| Forêt de Dugny (5) ⚠️ | Dugny › Paris Terres d'Envol | 1 |
| Forêt de Dugny (6) ⚠️ | Dugny › Paris Terres d'Envol | 1 |
| Parc Simone Veil (2) ⚠️ | Romainville › Est Ensemble | 1 |
| Parc de Aubervilliers (8) ⚠️ | Aubervilliers › Plaine Commune | 1 |
| Parc de Villemomble (10) ⚠️ | Villemomble › Grand Paris - Grand Est | 1 |
| Parc de Villemomble (17) ⚠️ | Villemomble › Grand Paris - Grand Est | 1 |
| Parc Louis Antoine de Bougainville ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 1 |
| Promenade François-Mitterrand ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 1 |
| Square des Amis ⚠️ | Neuilly-sur-Marne › Grand Paris - Grand Est | 1 |
| Parc de la Mairie (3) ⚠️ | Coubron › Grand Paris - Grand Est | 1 |
| Square du 19 mars 1962 ⚠️ | Pantin › Est Ensemble | 1 |
| Parc Henri Barbusse ⚠️ | Pantin › Est Ensemble | 1 |
| Forêt urbaine ⚠️ | Aubervilliers › Plaine Commune | 1 |
| Square Barbara ⚠️ | Montreuil › Est Ensemble | 1 |
| Parc de Bobigny (4) ⚠️ | Bobigny › Est Ensemble | 1 |
| Square Honoré d'Estienne d'Orves ⚠️ | Les Pavillons-sous-Bois › Grand Paris - Grand Est | 1 |
| Parc de la Liberté ⚠️ | La Courneuve › Plaine Commune | 1 |
| Plaine de jeux ⚠️ | Noisy-le-Sec › Est Ensemble | 1 |
| Bois de Noisy-le-Grand (6) ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 1 |
| Parc de Neuilly-Plaisance (2) ⚠️ | Neuilly-Plaisance › Grand Paris - Grand Est | 1 |
| Parc de Neuilly-Plaisance (3) ⚠️ | Neuilly-Plaisance › Grand Paris - Grand Est | 1 |
| Parc de Neuilly-Plaisance (4) ⚠️ | Neuilly-Plaisance › Grand Paris - Grand Est | 1 |
| Parc des Fauvettes ⚠️ | Neuilly-sur-Marne › Grand Paris - Grand Est | 1 |
| Square de Thann ⚠️ | Rosny-sous-Bois › Grand Paris - Grand Est | 1 |
| Forêt de Sevran (5) ⚠️ | Sevran › Paris Terres d'Envol | 1 |
| Forêt de Sevran (6) ⚠️ | Sevran › Paris Terres d'Envol | 1 |
| Bois de l'Île-Saint-Denis ⚠️ | L'Île-Saint-Denis › Plaine Commune | 1 |
| Forêt de l'Île-Saint-Denis (2) ⚠️ | L'Île-Saint-Denis › Plaine Commune | 1 |
| Parc de Sevran (6) ⚠️ | Sevran › Paris Terres d'Envol | 1 |
| Parc des Oiseaux ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 1 |
| Bois de Noisy-le-Grand (61) ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 1 |
| Bois de Noisy-le-Grand (69) ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 1 |
| Bois de Noisy-le-Grand (71) ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 1 |
| Bois de Noisy-le-Grand (75) ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 1 |
| Parc de Noisy-le-Grand (7) ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 1 |
| Bois de Noisy-le-Grand (108) ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 1 |
| Square Boughera El Ouafi ⚠️ | Bobigny › Est Ensemble | 1 |
| Parc de Gournay-sur-Marne (5) ⚠️ | Gournay-sur-Marne › Grand Paris - Grand Est | 1 |
| Bois du Blanc-Mesnil (8) ⚠️ | Le Blanc-Mesnil › Paris Terres d'Envol | 1 |
| Bois du Blanc-Mesnil (9) ⚠️ | Le Blanc-Mesnil › Paris Terres d'Envol | 1 |
| Bois du Blanc-Mesnil (11) ⚠️ | Le Blanc-Mesnil › Paris Terres d'Envol | 1 |
| Bois de La Courneuve (6) ⚠️ | La Courneuve › Plaine Commune | 1 |
| Bois de La Courneuve (8) ⚠️ | La Courneuve › Plaine Commune | 1 |
| Bois de La Courneuve (11) ⚠️ | La Courneuve › Plaine Commune | 1 |
| Bois de Saint-Denis (9) ⚠️ | Saint-Denis › Plaine Commune | 1 |
| Bois de Stains (4) ⚠️ | Stains › Plaine Commune | 1 |
| Bois de Stains (11) ⚠️ | Stains › Plaine Commune | 1 |
| Forêt de Gournay-sur-Marne (18) ⚠️ | Gournay-sur-Marne › Grand Paris - Grand Est | 1 |
| Forêt de Noisy-le-Sec ⚠️ | Noisy-le-Sec › Est Ensemble | 1 |
| Forêt de Noisy-le-Sec (12) ⚠️ | Noisy-le-Sec › Est Ensemble | 1 |
| Forêt de Noisy-le-Sec (17) ⚠️ | Noisy-le-Sec › Est Ensemble | 1 |
| Forêt de Noisy-le-Sec (19) ⚠️ | Noisy-le-Sec › Est Ensemble | 1 |
| Forêt de Noisy-le-Sec (21) ⚠️ | Noisy-le-Sec › Est Ensemble | 1 |
| Forêt de Bondy (3) ⚠️ | Bondy › Est Ensemble | 1 |
| Forêt de Bondy (4) ⚠️ | Noisy-le-Sec › Est Ensemble | 1 |
| Forêt de Bondy (5) ⚠️ | Bondy › Est Ensemble | 1 |
| Forêt de Bondy (8) ⚠️ | Bondy › Est Ensemble | 1 |
| Forêt de Bondy (9) ⚠️ | Bondy › Est Ensemble | 1 |
| Forêt du Blanc-Mesnil (3) ⚠️ | Bondy › Est Ensemble | 1 |
| Forêt de Saint-Denis (14) ⚠️ | Saint-Denis › Plaine Commune | 1 |
| Bois de Saint-Denis (19) ⚠️ | Saint-Denis › Plaine Commune | 1 |
| Forêt de Saint-Ouen-sur-Seine ⚠️ | Saint-Ouen-sur-Seine › Plaine Commune | 1 |
| Jardin d'Alcobendas ⚠️ | Épinay-sur-Seine › Plaine Commune | 1 |
| Parc des Trois Rivières ⚠️ | Stains › Plaine Commune | 1 |
| Forêt de Gagny (11) ⚠️ | Gagny › Grand Paris - Grand Est | 1 |
| Bois de Noisy-le-Grand (113) ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 1 |
| Forêt de Gagny (12) ⚠️ | Gagny › Grand Paris - Grand Est | 1 |
| Forêt de Gagny (13) ⚠️ | Gagny › Grand Paris - Grand Est | 1 |
| Square Nelson Mandela ⚠️ | Drancy › Paris Terres d'Envol | 1 |
| Forêt de Dugny (8) ⚠️ | Dugny › Paris Terres d'Envol | 1 |
| Bois de Villepinte (2) ⚠️ | Villepinte › Paris Terres d'Envol | 1 |
| Bois de Aulnay-sous-Bois (4) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 1 |
| Bois de Villepinte (14) ⚠️ | Villepinte › Paris Terres d'Envol | 1 |
| Forêt de Neuilly-sur-Marne (27) ⚠️ | Neuilly-sur-Marne › Grand Paris - Grand Est | 1 |
| Château de la Queue ⚠️ | Tremblay-en-France › Paris Terres d'Envol | 1 |
| Forêt urbaine Général Morand ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 1 |
| Fort de Villiers ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 1 |
| Forêt de Villepinte (15) ⚠️ | Villepinte › Paris Terres d'Envol | 1 |
| Parc de Saint-Denis (37) ⚠️ | Saint-Denis › Plaine Commune | 1 |
| Parc de La Courneuve (2) ⚠️ | La Courneuve › Plaine Commune | 1 |
| Promenade Cesária Évora ⚠️ | Saint-Ouen-sur-Seine › Plaine Commune | 1 |
| Square Émile Bellepêche ⚠️ | Rosny-sous-Bois › Grand Paris - Grand Est | 1 |
| Forêt de Romainville (6) ⚠️ | Romainville › Est Ensemble | 1 |
| Forêt de Romainville (8) ⚠️ | Romainville › Est Ensemble | 1 |
| Jardin de l'Orme Seul ⚠️ | La Courneuve › Plaine Commune | 1 |
| La réserve écologique ⚠️ | Épinay-sur-Seine › Plaine Commune | 1 |
| Parc des Guillaumes ⚠️ | Noisy-le-Sec › Est Ensemble | 1 |
| Parc de Noisy-le-Grand (20) ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 1 |
| Forêt de Villetaneuse (17) ⚠️ | Villetaneuse › Plaine Commune | 1 |
| Parc de La Courneuve (3) ⚠️ | La Courneuve › Plaine Commune | 1 |
| Bois de Saint-Denis (37) ⚠️ | Saint-Denis › Plaine Commune | 1 |
| Bois de Villepinte (18) ⚠️ | Villepinte › Paris Terres d'Envol | 1 |
| Bois de Rosny-sous-Bois (11) ⚠️ | Rosny-sous-Bois › Grand Paris - Grand Est | 1 |
| Bois de Aulnay-sous-Bois (12) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 1 |
| Bois de Aulnay-sous-Bois (16) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 1 |
| Bois de Aulnay-sous-Bois (17) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 1 |
| Bois de Villepinte (19) ⚠️ | Villepinte › Paris Terres d'Envol | 1 |
| Square Jean Lebas ⚠️ | Bondy › Est Ensemble | 1 |
| Square du 11 Novembre ⚠️ | Épinay-sur-Seine › Plaine Commune | 1 |
| Square Toussaint Louverture ⚠️ | Stains › Plaine Commune | 1 |
| Bois de Neuilly-Plaisance (3) ⚠️ | Neuilly-sur-Marne › Grand Paris - Grand Est | 1 |
| Parc de la villa Cathala et son arboretum ⚠️ | Noisy-le-Grand › Grand Paris - Grand Est | 1 |
| Forêt de Noisy-le-Sec (26) ⚠️ | Noisy-le-Sec › Est Ensemble | 1 |
| Parc du Docteur Herpin ⚠️ | Livry-Gargan › Grand Paris - Grand Est | 1 |
| Parc Bellevue ⚠️ | Livry-Gargan › Grand Paris - Grand Est | 1 |
| Parc de Saint-Denis (42) ⚠️ | Saint-Denis › Plaine Commune | 1 |
| Forêt de Gagny (28) ⚠️ | Gagny › Grand Paris - Grand Est | 1 |
| Parc de Tremblay ⚠️ | Tremblay-en-France › Paris Terres d'Envol | 1 |
| Forêt de Tremblay-en-France (18) ⚠️ | Tremblay-en-France › Paris Terres d'Envol | 1 |
| Parc de Sevran (8) ⚠️ | Sevran › Paris Terres d'Envol | 1 |
| Forêt de Villepinte (19) ⚠️ | Villepinte › Paris Terres d'Envol | 1 |
| Forêt de Villepinte (20) ⚠️ | Villepinte › Paris Terres d'Envol | 1 |
| Forêt de Aulnay-sous-Bois (61) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 1 |
| Forêt de Aulnay-sous-Bois (62) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 1 |
| Forêt de Aulnay-sous-Bois (64) ⚠️ | Aulnay-sous-Bois › Paris Terres d'Envol | 1 |

1 195 parc(s) plus petits qu'une cellule ne sont pas listés : la carte les dessine, mais ils n'offrent aucune cellule.

⚠️ 1561 parc(s) hors de la fenêtre 10–125 cellules (1559 trop petit(s), 2 trop grand(s)) : affichés sur la carte, mais ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| airport | 585 |
| military | 37 |
| prison | 3 |
| **Total déclaré** | **625** |
| dont dans une zone de ce territoire | 615 |

Le jeu de données couvre plus large que le territoire — il est produit à une échelle supérieure. Seules les cellules tombant dans une zone d'ici pèsent sur un pourcentage.

### Zones concernées

| Zone | Cellules exclues |
|---|---:|
| Tremblay-en-France | 460 |
| Dugny | 113 |
| Rosny-sous-Bois | 14 |
| Romainville | 11 |
| Saint-Denis | 7 |
| Le Bourget | 7 |
| Villepinte | 3 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
