# Couronne Sud (Montérégie)

Pack `qc-couronne-sud` · version 1.0.1 · grille 200 m · Canada › Québec › Grand Montréal

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
| Parcs | 25 |

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
| Varennes | 4 852 | 53 | 4 799 | 0 | **4 799** | 3 |
| Verchères | 3 725 | 0 | 3 725 | 0 | **3 725** |  |
| Saint-Jean-Baptiste | 3 702 | 17 | 3 685 | 0 | **3 685** |  |
| Beauharnois | 3 422 | 5 | 3 417 | 0 | **3 417** | 2 |
| Contrecœur | 3 345 | 2 | 3 343 | 0 | **3 343** | 3 |
| Carignan | 3 168 | 0 | 3 168 | 0 | **3 168** | 1 |
| Saint-Philippe | 3 127 | 0 | 3 127 | 0 | **3 127** |  |
| Saint-Constant | 2 881 | 2 | 2 879 | 0 | **2 879** | 1 |
| Saint-Isidore | 2 631 | 0 | 2 631 | 0 | **2 631** |  |
| Kahnawake | 3 136 | 611 | 2 525 | 0 | **2 525** |  |
| Sainte-Julie | 2 446 | 0 | 2 446 | 126 | **2 320** | 2 |
| Saint-Mathias-sur-Richelieu | 2 409 | 0 | 2 409 | 5 | **2 404** |  |
| Mercier | 2 323 | 5 | 2 318 | 0 | **2 318** |  |
| La Prairie | 2 225 | 1 | 2 224 | 0 | **2 224** | 3 |
| Mont-Saint-Hilaire | 2 243 | 19 | 2 224 | 0 | **2 224** | 1 |
| Saint-Mathieu-de-Beloeil | 2 011 | 0 | 2 011 | 15 | **1 996** |  |
| Saint-Amable | 1 884 | 0 | 1 884 | 0 | **1 884** | 1 |
| Saint-Basile-le-Grand | 1 834 | 0 | 1 834 | 14 | **1 820** | 1 |
| Châteauguay | 2 848 | 1 033 | 1 815 | 0 | **1 815** | 2 |
| Calixa-Lavallée | 1 683 | 0 | 1 683 | 0 | **1 683** |  |
| Saint-Mathieu | 1 590 | 0 | 1 590 | 0 | **1 590** |  |
| Richelieu | 1 572 | 0 | 1 572 | 0 | **1 572** |  |
| Chambly | 1 261 | 0 | 1 261 | 0 | **1 261** | 2 |
| Beloeil | 1 237 | 0 | 1 237 | 0 | **1 237** |  |
| Candiac | 977 | 100 | 877 | 0 | **877** | 1 |
| Léry | 518 | 0 | 518 | 0 | **518** |  |
| Sainte-Catherine | 693 | 216 | 477 | 0 | **477** | 2 |
| Delson | 389 | 0 | 389 | 0 | **389** |  |
| Otterburn Park | 269 | 0 | 269 | 0 | **269** |  |
| McMasterville | 156 | 0 | 156 | 0 | **156** |  |

## Parcs (25)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Les défis « parc » demandent au moins 10 cellules.

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
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
| Parc Saint-Charles | Varennes | 22 |
| Parc de conservation Barbe-Denys-De La Trinité | Contrecœur | 22 |
| Parc multifonctionnel | Saint-Constant | 22 |
| Réserve naturelle du Ruisseau-Robert | Carignan | 20 |
| Parc Saint-Charles (2) | Varennes | 12 |
| Parc des Écluses | Beauharnois | 10 |
| Parc Champlain ⚠️ | Candiac | 8 |
| Parc Lucie-F.-Roussel ⚠️ | La Prairie | 7 |
| Parc Robert-Lebel ⚠️ | Chambly | 7 |
| Parc de la Commune ⚠️ | Varennes | 6 |
| Parc Émilie-Gamelin ⚠️ | La Prairie | 5 |
| Parc du Ruisseau ⚠️ | Saint-Basile-le-Grand | 5 |
| Parc de la Coulée ⚠️ | Sainte-Julie | 4 |

⚠️ 7 parc(s) sous le seuil de 10 cellules : ils ne peuvent pas servir de cible à un défi.

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
