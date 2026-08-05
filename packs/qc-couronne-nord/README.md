# Couronne Nord

Pack `qc-couronne-nord` · version 1.0.0 · grille 200 m · Canada › Québec › Grand Montréal

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 73 305 |
| dont restreintes (aéroport, militaire, prison) | 1 382 |
| Cellules retirées par le masque d'eau | 3 138 |
| Villes | 21 |
| Arrondissements et quartiers | 0 |
| Îles | 0 |
| Parcs | 22 |

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

## Villes (21)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Parcs |
|---|---:|---:|---:|---:|---:|---:|
| Mirabel | 24 772 | 1 | 24 771 | 1 018 | **23 753** | 3 |
| Terrebonne | 8 232 | 254 | 7 978 | 25 | **7 953** | 4 |
| Mascouche | 5 528 | 39 | 5 489 | 0 | **5 489** | 1 |
| L'Assomption | 5 099 | 4 | 5 095 | 0 | **5 095** | 1 |
| Sainte-Anne-des-Plaines | 4 840 | 1 | 4 839 | 91 | **4 748** | 1 |
| Saint-Jérôme | 4 670 | 1 | 4 669 | 0 | **4 669** | 3 |
| Saint-Eustache | 3 710 | 126 | 3 584 | 0 | **3 584** | 1 |
| Repentigny | 3 656 | 552 | 3 104 | 0 | **3 104** | 1 |
| Oka | 4 413 | 1 514 | 2 899 | 0 | **2 899** |  |
| Blainville | 2 842 | 35 | 2 807 | 248 | **2 559** | 2 |
| Saint-Joseph-du-Lac | 2 120 | 15 | 2 105 | 0 | **2 105** |  |
| Saint-Sulpice | 1 863 | 0 | 1 863 | 0 | **1 863** |  |
| Boisbriand | 1 525 | 84 | 1 441 | 0 | **1 441** | 1 |
| Rosemère | 624 | 69 | 555 | 0 | **555** | 2 |
| Sainte-Thérèse | 479 | 0 | 479 | 0 | **479** |  |
| Sainte-Marthe-sur-le-Lac | 432 | 1 | 431 | 0 | **431** |  |
| Deux-Montagnes | 368 | 53 | 315 | 0 | **315** | 1 |
| Lorraine | 311 | 4 | 307 | 0 | **307** |  |
| Pointe-Calumet | 593 | 356 | 237 | 0 | **237** |  |
| Bois-des-Filion | 251 | 20 | 231 | 0 | **231** | 1 |
| Charlemagne | 116 | 9 | 107 | 0 | **107** |  |

## Parcs (22)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Les défis « parc » demandent au moins 10 cellules.

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Parc du Domaine Vert | Mirabel | 138 |
| Parc du Domaine Vert (2) | Mirabel | 99 |
| Parc régional Bois de Belle-Rivière | Mirabel | 88 |
| Parc Faunique Domaine du Parc (Ruisseau de Feu) | Terrebonne | 75 |
| Parc du Grand-Coteau | Mascouche | 64 |
| Parc régional de la Rivière-du-Nord | Saint-Jérôme | 62 |
| Parc nature Saint-Eustache | Saint-Eustache | 61 |
| Parc de Blainville | Blainville | 30 |
| Parc de Terrebonne | Terrebonne | 21 |
| Parc Marais Tylee | Rosemère | 14 |
| Parc de l'Île-Lebel | Repentigny | 12 |
| Parc de la Rivière-des-Mille-Îles | Boisbriand | 12 |
| Parc Équestre | Blainville | 11 |
| Réserve écologique de l'Île-Garth ⚠️ | Bois-des-Filion | 9 |
| Parc écologique de l'Assomption ⚠️ | L'Assomption | 8 |
| Réserve naturelle du Boisé-Roger-Lemoine ⚠️ | Deux-Montagnes | 8 |
| Parc Angora ⚠️ | Terrebonne | 7 |
| Réserve naturelle de l'Île des Juifs ⚠️ | Rosemère | 7 |
| Parc des Méandres ⚠️ | Sainte-Anne-des-Plaines | 6 |
| Parc Jacques-Locas ⚠️ | Saint-Jérôme | 6 |
| Parc Vaillant ⚠️ | Terrebonne | 5 |
| Parc naturel de Rivière-à-Gagnon ⚠️ | Saint-Jérôme | 5 |

⚠️ 9 parc(s) sous le seuil de 10 cellules : ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| airport | 1 018 |
| military | 273 |
| prison | 91 |
| **Total déclaré** | **1 382** |
| dont dans une zone de ce territoire | 1 382 |


### Zones concernées

| Zone | Cellules exclues |
|---|---:|
| Mirabel | 1 018 |
| Blainville | 248 |
| Sainte-Anne-des-Plaines | 91 |
| Terrebonne | 25 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
