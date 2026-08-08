# Laval

Pack `qc-laval` · version 1.2.0 · grille 200 m · Canada › Québec › Grand Montréal

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 12 495 |
| dont restreintes (aéroport, militaire, prison) | 24 |
| Cellules retirées par le masque d'eau | 1 000 |
| Villes | 1 |
| Arrondissements et quartiers | 14 |
| Îles | 0 |
| Parcs | 354 |

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

## Villes (1)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Parcs |
|---|---:|---:|---:|---:|---:|---:|
| Laval | 13 495 | 1 000 | 12 495 | 24 | **12 471** | 351 |

## Arrondissements et quartiers (14)

| Zone | Ville | Brut | Eau | Sans eau | Restr. | Comptées | Parcs |
|---|---|---:|---:|---:|---:|---:|---:|
| Duvernay | laval | 2 464 | 155 | 2 309 | 0 | **2 309** | 39 |
| Chomedey | laval | 2 096 | 56 | 2 040 | 0 | **2 040** | 70 |
| Saint-François | laval | 2 072 | 249 | 1 823 | 12 | **1 811** | 13 |
| Auteuil | laval | 1 328 | 77 | 1 251 | 0 | **1 251** | 21 |
| Sainte-Dorothée | laval | 1 184 | 74 | 1 110 | 0 | **1 110** | 41 |
| Fabreville | laval | 1 182 | 122 | 1 060 | 0 | **1 060** | 38 |
| Sainte-Rose | laval | 890 | 48 | 842 | 0 | **842** | 37 |
| Vimont | laval | 711 | 2 | 709 | 0 | **709** | 19 |
| Laval-des-Rapides | laval | 492 | 38 | 454 | 0 | **454** | 29 |
| Saint-Vincent-de-Paul | laval | 402 | 0 | 402 | 12 | **390** | 18 |
| Laval-Ouest | laval | 259 | 54 | 205 | 0 | **205** | 10 |
| Pont-Viau | laval | 181 | 16 | 165 | 0 | **165** | 12 |
| Laval-sur-le-Lac | laval | 129 | 31 | 98 | 0 | **98** | 2 |
| Îles-Laval | laval | 56 | 28 | 28 | 0 | **28** | 2 |

## Parcs (354)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Bois Duvernay ⚠️ | Laval › Duvernay | 152 |
| Le Boisé Sainte-Dorothée ⚠️ | Laval › Sainte-Dorothée | 143 |
| Bois de l'Équerre | Laval › Sainte-Rose | 111 |
| Bois Papineau | Laval › Duvernay | 53 |
| Bois de la Source | Laval › Fabreville | 22 |
| Centre de la nature | Laval › Saint-Vincent-de-Paul | 20 |
| Parc Bernard-Landry | Laval › Laval-des-Rapides | 15 |
| Parc de Lausanne | Laval › Vimont | 10 |
| Réserve naturelle de l'Île Locas ⚠️ | Laval › Fabreville | 6 |
| Berge des Baigneurs ⚠️ | Laval › Sainte-Rose | 5 |
| Le Boutillier Park ⚠️ | Laval › Chomedey | 5 |
| Parc Marc-Aurèle-Fortin (2) ⚠️ | Laval › Fabreville | 5 |
| Parc Olier-Payette ⚠️ | Laval › Sainte-Rose | 5 |
| Berge de la Plage-Idéale ⚠️ | Laval › Auteuil | 5 |
| Parc Couvrette ⚠️ | Laval › Sainte-Dorothée | 4 |
| Parc École Odyssée des Jeunes ⚠️ | Laval › Auteuil | 4 |
| Parc Rosaire-Gauthier ⚠️ | Laval › Pont-Viau | 4 |
| Parc Saint-Martin ⚠️ | Laval › Chomedey | 4 |
| Parc Isabelle ⚠️ | Laval › Fabreville | 4 |
| Parc Sylvie ⚠️ | Laval › Sainte-Dorothée | 4 |
| Parc Champfleury ⚠️ | Laval › Sainte-Rose | 4 |
| Berge de l'Orée-des-Bois ⚠️ | Laval › Fabreville | 4 |
| Parc de Laval (11) ⚠️ | Laval › Fabreville | 4 |
| Berge de la Plage-des-Îles ⚠️ | Laval › Fabreville | 4 |
| Parc Giovanni-Caboto ⚠️ | Laval › Duvernay | 4 |
| Parc Émile ⚠️ | Laval › Laval-des-Rapides | 4 |
| Parc-école Horizon-Jeunesse ⚠️ | Laval › Auteuil | 4 |
| Parc-École Poly-Jeunesse ⚠️ | Laval › Fabreville | 4 |
| Parc Laval-Ouest ⚠️ | Laval › Laval-Ouest | 3 |
| Parc du Moulin ⚠️ | Laval › Saint-François | 3 |
| Parc Jolibourg ⚠️ | Laval › Sainte-Dorothée | 3 |
| Parc Masson (3) ⚠️ | Laval › Saint-François | 3 |
| Parc Curé-Coursol ⚠️ | Laval › Chomedey | 3 |
| Parc du Sablon ⚠️ | Laval › Chomedey | 3 |
| Parc Berthiaume-Du Tremblay ⚠️ | Laval › Chomedey | 3 |
| Berge Berthiaume-Du Tremblay ⚠️ | Laval › Chomedey | 3 |
| Berge des Baigneurs (2) ⚠️ | Laval › Sainte-Rose | 3 |
| Parc des Ambassadeurs ⚠️ | Laval › Duvernay | 3 |
| Parc Bois-de-Boulogne ⚠️ | Laval › Chomedey | 3 |
| Parc Bois-de-Boulogne (2) ⚠️ | Laval › Chomedey | 3 |
| Parc Lévis-Paquette ⚠️ | Laval › Chomedey | 2 |
| Parc des Chênes ⚠️ | Laval › Laval-sur-le-Lac | 2 |
| Parc Saint-Édouard ⚠️ | Laval › Fabreville | 2 |
| Parc Prince-Rupert ⚠️ | Laval › Auteuil | 2 |
| Parc Paul-Marcel-Maheu ⚠️ | Laval › Laval-des-Rapides | 2 |
| Parc Madeleine ⚠️ | Laval › Fabreville | 2 |
| Parc Chénier (2) ⚠️ | Laval › Pont-Viau | 2 |
| Parc Val Des Arbres ⚠️ | Laval › Duvernay | 2 |
| Parc Raymond-Millar ⚠️ | Laval › Sainte-Rose | 2 |
| Parc de la Renaissance ⚠️ | Laval › Sainte-Rose | 2 |
| Parc Légaré ⚠️ | Laval › Chomedey | 2 |
| Berge des Cageux ⚠️ | Laval › Chomedey | 2 |
| Parc des Terrasses ⚠️ | Laval › Sainte-Rose | 2 |
| Parc Prévost ⚠️ | Laval › Vimont | 2 |
| Berge Délia-Tétreault ⚠️ | Laval › Pont-Viau | 2 |
| Parc de Laval (25) ⚠️ | Laval › Chomedey | 2 |
| Berge Aux-Quatre-Vents ⚠️ | Laval › Laval-Ouest | 2 |
| Berge du Grand-Brochet ⚠️ | Laval › Laval-Ouest | 2 |
| Réserve naturelle de l'Île Darling ⚠️ | Laval › Sainte-Rose | 2 |
| Parc-école Gerry-Dattilio ⚠️ | Laval › Chomedey | 2 |
| Parc Chopin ⚠️ | Laval › Chomedey | 2 |
| Berge de la Plage-Jacques-Cartier ⚠️ | Laval › Auteuil | 2 |
| Parc Notre-Dame ⚠️ | Laval › Sainte-Rose | 2 |
| Parc des Cardinaux ⚠️ | Laval › Sainte-Rose | 2 |
| Parc Saint-Claude ⚠️ | Laval › Laval-des-Rapides | 1 |
| Parc Louis-Durocher ⚠️ | Laval › Vimont | 1 |
| Parc de la Rivière-des-Mille-Iles ⚠️ | Laval › Sainte-Rose | 1 |
| Parc Père-Vimont ⚠️ | Laval › Vimont | 1 |
| Parc Paradis ⚠️ | Laval › Vimont | 1 |
| Parc Nicole ⚠️ | Laval › Fabreville | 1 |
| Parc Saint-Mathieu ⚠️ | Laval › Saint-François | 1 |
| Parc l'Escale ⚠️ | Laval › Saint-François | 1 |
| Berge du Vieux-Moulin ⚠️ | Laval › Saint-François | 1 |
| Parc des Tilleuls ⚠️ | Laval › Duvernay | 1 |
| Parc Jean-XXIII ⚠️ | Laval › Saint-Vincent-de-Paul | 1 |
| Parc René-Patenaude ⚠️ | Laval › Pont-Viau | 1 |
| Parc des Saules ⚠️ | Laval › Auteuil | 1 |
| Parc Robitaille ⚠️ | Laval › Sainte-Dorothée | 1 |
| Parc de Laval (2) ⚠️ | Laval › Duvernay | 1 |
| Parc de Laval (3) ⚠️ | Laval › Laval-Ouest | 1 |
| Parc Ivan-Pavlov ⚠️ | Laval › Vimont | 1 |
| Parc-école Notre-Dame du Sourire ⚠️ | Laval › Duvernay | 1 |
| Parc Montcalm (2) ⚠️ | Laval › Chomedey | 1 |
| Parc Bigras ⚠️ | Laval › Îles-Laval | 1 |
| Île Ronde ⚠️ | Laval › Îles-Laval | 1 |
| Halte de la Promenade-Paton ⚠️ | Laval › Chomedey | 1 |
| Berge Olivier-Charbonneau ⚠️ | Laval › Saint-François | 1 |
| Parc Ulric Desbiens ⚠️ | Laval › Auteuil | 1 |
| Parc de la Mauricie ⚠️ | Laval › Duvernay | 1 |
| Parc d'Argenson ⚠️ | Laval › Duvernay | 1 |
| Parc Robert-L'Herbier ⚠️ | Laval › Duvernay | 1 |
| Parc St-Maurice ⚠️ | Laval › Duvernay | 1 |
| Parc du Bon-Pasteur ⚠️ | Laval › Laval-des-Rapides | 1 |
| Parc Raymond-Millar (2) ⚠️ | Laval › Sainte-Rose | 1 |
| Parc de la Terrasse-Germaine ⚠️ | Laval › Sainte-Dorothée | 1 |
| Berge de la Halte-à-la-Rivière ⚠️ | Laval › Sainte-Dorothée | 1 |
| Parc de Laval (6) ⚠️ | Laval › Chomedey | 1 |
| Parc de Laval (7) ⚠️ | Laval › Sainte-Dorothée | 1 |
| Parc de la Volière ⚠️ | Laval › Sainte-Rose | 1 |
| Parc des Anémones ⚠️ | Laval › Sainte-Dorothée | 1 |
| Parc des Roseaux (2) ⚠️ | Laval › Sainte-Dorothée | 1 |
| Parc des Néuphars ⚠️ | Laval › Sainte-Dorothée | 1 |
| Parc de Laval (9) ⚠️ | Laval › Sainte-Dorothée | 1 |
| Parc Benjamin-Dion ⚠️ | Laval › Sainte-Dorothée | 1 |
| Parc du Faubourg ⚠️ | Laval › Fabreville | 1 |
| Berge des Goélands ⚠️ | Laval › Laval-Ouest | 1 |
| Parc Montglfier ⚠️ | Laval › Chomedey | 1 |
| Parc de Laval (12) ⚠️ | Laval › Chomedey | 1 |
| Parc de Laval (13) ⚠️ | Laval › Chomedey | 1 |
| Parc École-Hillcrest ⚠️ | Laval › Chomedey | 1 |
| Berge de la Promenade ⚠️ | Laval › Chomedey | 1 |
| Berge du Havre ⚠️ | Laval › Chomedey | 1 |
| Parc John F. Kennedy ⚠️ | Laval › Chomedey | 1 |
| Parc Éliot ⚠️ | Laval › Chomedey | 1 |
| Parc de la Fabrique Saint-Martin ⚠️ | Laval › Chomedey | 1 |
| Parc Pie-X ⚠️ | Laval › Chomedey | 1 |
| Parc Saint-Norbert ⚠️ | Laval › Chomedey | 1 |
| Parc Marcel-Proust ⚠️ | Laval › Chomedey | 1 |
| Parc Joachim-du Bellay ⚠️ | Laval › Chomedey | 1 |
| Parc École des Cèdres ⚠️ | Laval › Fabreville | 1 |
| Parc Ferme Sainte-Thérèse ⚠️ | Laval › Fabreville | 1 |
| Parc Pépin ⚠️ | Laval › Fabreville | 1 |
| Parc Sacré-Coeur (2) ⚠️ | Laval › Fabreville | 1 |
| Parc Roch-Hébert ⚠️ | Laval › Sainte-Rose | 1 |
| Parc de la Fabrique-Sainte-Rose ⚠️ | Laval › Sainte-Rose | 1 |
| Parc de Ségovie ⚠️ | Laval › Vimont | 1 |
| Parc Dumas ⚠️ | Laval › Vimont | 1 |
| Parc de Laval (20) ⚠️ | Laval › Vimont | 1 |
| Halte de Livourne ⚠️ | Laval › Vimont | 1 |
| Parc Henri-Dunant (2) ⚠️ | Laval › Pont-Viau | 1 |
| Parc Bousquet ⚠️ | Laval › Chomedey | 1 |
| Parc de Laval (21) ⚠️ | Laval › Duvernay | 1 |
| Parc de Laval (22) ⚠️ | Laval › Duvernay | 1 |
| Parc Sun Valley ⚠️ | Laval › Chomedey | 1 |
| Parc des Mésanges ⚠️ | Laval › Laval-des-Rapides | 1 |
| Parc de Montceau ⚠️ | Laval › Laval-des-Rapides | 1 |
| Parc Pontmain ⚠️ | Laval › Laval-des-Rapides | 1 |
| Parc Lucien-Cartier ⚠️ | Laval › Saint-François | 1 |
| Berge de l'Anse ⚠️ | Laval › Laval-Ouest | 1 |
| Parc de Calvi ⚠️ | Laval › Fabreville | 1 |
| Parc Sainte-Marie (4) ⚠️ | Laval › Saint-François | 1 |
| Parc Des Trembles ⚠️ | Laval › Duvernay | 1 |
| Parc des Tisserands ⚠️ | Laval › Duvernay | 1 |
| Berge des Pinsons ⚠️ | Laval › Duvernay | 1 |
| Parc St-Maxime ⚠️ | Laval › Chomedey | 1 |
| Parc Islemère ⚠️ | Laval › Sainte-Dorothée | 1 |
| Parc-École du Bois-Joli ⚠️ | Laval › Saint-Vincent-de-Paul | 1 |
| Parc Fabre-Joie ⚠️ | Laval › Fabreville | 1 |
| Parc de Laval (30) ⚠️ | Laval › Sainte-Rose | 1 |
| Parc des Sommelières ⚠️ | Laval › Duvernay | 1 |
| Parc Du Moulin-Desbiens ⚠️ | Laval › Auteuil | 1 |
| Parc municipal (2) ⚠️ | Laval › Auteuil | 1 |
| Parc de Laval (34) ⚠️ | Laval › Laval-des-Rapides | 1 |
| Parc-école Laval-Catholic ⚠️ | Laval › Chomedey | 1 |
| Parc des Crécerelles ⚠️ | Laval › Sainte-Rose | 1 |
| Parc des Coccinelles (2) ⚠️ | Laval › Chomedey | 1 |
| Parc Frégault ⚠️ | Laval › Chomedey | 1 |
| Parc Eva-Circé-Côté ⚠️ | Laval › Auteuil | 1 |
| Parc Champenois ⚠️ | Laval › Sainte-Rose | 1 |
| Parc des Choucas ⚠️ | Laval › Sainte-Rose | 1 |
| Parc Bizet ⚠️ | Laval › Chomedey | 1 |
| Parc Francine ⚠️ | Laval › Chomedey | 1 |
| Parc de Cluny ⚠️ | Laval › Laval-des-Rapides | 1 |
| Parc Sainte-Béatrice ⚠️ | Laval › Auteuil | 1 |
| Parc-école Jacques-Bourdon ⚠️ | Laval › Duvernay | 1 |
| Parc de Laval (49) ⚠️ | Laval › Sainte-Dorothée | 1 |

188 parc(s) plus petits qu'une cellule ne sont pas listés : la carte les dessine, mais ils n'offrent aucune cellule.

⚠️ 348 parc(s) hors de la fenêtre 10–125 cellules (346 trop petit(s), 2 trop grand(s)) : affichés sur la carte, mais ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| airport | 12 |
| prison | 12 |
| military | 0 |
| **Total déclaré** | **24** |
| dont dans une zone de ce territoire | 24 |


### Zones concernées

| Zone | Cellules exclues |
|---|---:|
| Laval | 24 |
| Saint-Vincent-de-Paul | 12 |
| Saint-François | 12 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
