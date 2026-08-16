# Lévis (Chaudière-Appalaches)

Pack `qc-levis` · version 1.0.1 · grille 200 m · Canada › Québec › Grand Québec

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 23 868 |
| dont restreintes (aéroport, militaire, prison) | 21 |
| Cellules retirées par le masque d'eau | 2 610 |
| Villes | 1 |
| Arrondissements et quartiers | 10 |
| Îles | 0 |
| Parcs | 230 |

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
| Lévis | 26 478 | 2 610 | 23 868 | 21 | **23 847** | 229 |

## Arrondissements et quartiers (10)

| Zone | Ville | Brut | Eau | Sans eau | Restr. | Comptées | Parcs |
|---|---|---:|---:|---:|---:|---:|---:|
| Saint-Étienne-de-Lauzon | levis | 5 117 | 51 | 5 066 | 0 | **5 066** | 26 |
| Saint-Nicolas | levis | 5 005 | 3 | 5 002 | 0 | **5 002** | 38 |
| Saint-Jean-Chrysostome | levis | 4 459 | 43 | 4 416 | 14 | **4 402** | 13 |
| Pintendre | levis | 2 830 | 9 | 2 821 | 7 | **2 814** | 10 |
| Lévis (quartier) | levis | 2 401 | 9 | 2 392 | 0 | **2 392** | 85 |
| Saint-Joseph-de-la-Pointe-De Lévy | levis | 1 949 | 10 | 1 939 | 0 | **1 939** | 2 |
| Saint-Romuald | levis | 949 | 19 | 930 | 0 | **930** | 23 |
| Sainte-Hélène-de-Breakeyville | levis | 604 | 11 | 593 | 0 | **593** | 9 |
| Charny | levis | 505 | 4 | 501 | 0 | **501** | 17 |
| Saint-Rédempteur | levis | 201 | 1 | 200 | 0 | **200** | 6 |

## Parcs (230)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Parc régional de la Pointe-de-la-Martinière | Lévis › Lévis (quartier) | 59 |
| Parc de la Rivière-Etchemin | Lévis › Saint-Romuald | 58 |
| Parc Valéro-Les Écarts | Lévis › Lévis (quartier) | 34 |
| Parc Des Chutes de la Chaudière | Lévis › Saint-Nicolas | 33 |
| Parc Georges-Maranda ⚠️ | Lévis › Lévis (quartier) | 7 |
| Parc Renaud-Maillette ⚠️ | Lévis › Saint-Rédempteur | 7 |
| Parc du Fort-numéro-un-de-la-Pointe-Lévy ⚠️ | Lévis › Lévis (quartier) | 6 |
| Parc des Grandes Pointes ⚠️ | Lévis › Saint-Étienne-de-Lauzon | 5 |
| Parc Quatre-Saisons ⚠️ | Lévis › Saint-Jean-Chrysostome | 4 |
| Parc Champigny ⚠️ | Lévis › Saint-Jean-Chrysostome | 4 |
| Parc de l'Anse-Tibbits ⚠️ | Lévis › Lévis (quartier) | 4 |
| Parc du Domaine-Etchemin ⚠️ | Lévis › Lévis (quartier) | 4 |
| Parc du Rigolet ⚠️ | Lévis › Saint-Romuald | 4 |
| Parc Benoît-Letarte ⚠️ | Lévis › Saint-Nicolas | 2 |
| Parc Maréchal-Joffre ⚠️ | Lévis › Charny | 2 |
| Parc de l'OTJ ⚠️ | Lévis › Charny | 2 |
| Parc Ian-Breakey ⚠️ | Lévis › Sainte-Hélène-de-Breakeyville | 2 |
| Parc Ludger-Bastien ⚠️ | Lévis › Saint-Étienne-de-Lauzon | 2 |
| Parc de la Paix ⚠️ | Lévis › Lévis (quartier) | 2 |
| Parc Turcotte ⚠️ | Lévis › Saint-Rédempteur | 2 |
| Parc-école Taniata ⚠️ | Lévis › Saint-Jean-Chrysostome | 2 |
| Parc Guy-Dionne ⚠️ | Lévis › Lévis (quartier) | 2 |
| Parc Bruno-Verret ⚠️ | Lévis › Saint-Étienne-de-Lauzon | 2 |
| Parc de l'Envol ⚠️ | Lévis › Saint-Nicolas | 2 |
| Quai Paquet ⚠️ | Lévis › Lévis (quartier) | 2 |
| Parc Elizabeth-Johnson-Davie ⚠️ | Lévis › Lévis (quartier) | 2 |
| Parc Lavoisier ⚠️ | Lévis › Saint-Romuald | 2 |
| Parc du Domaine-de-L'Auberivière ⚠️ | Lévis › Lévis (quartier) | 2 |
| Parc de Lévis (16) ⚠️ | Lévis › Pintendre | 2 |
| Parc du Belvédère ⚠️ | Lévis › Lévis (quartier) | 2 |
| Parc du Grand-Quevilly ⚠️ | Lévis › Lévis (quartier) | 2 |
| Parc du Faubourg-des-Arbrisseaux ⚠️ | Lévis › Sainte-Hélène-de-Breakeyville | 1 |
| Parc de Lévis ⚠️ | Lévis › Saint-Nicolas | 1 |
| Parc de l'Érablière ⚠️ | Lévis › Saint-Nicolas | 1 |
| Parc Jean-Dumets ⚠️ | Lévis › Saint-Nicolas | 1 |
| Parc de Lévis (2) ⚠️ | Lévis › Saint-Nicolas | 1 |
| Parc Aline-Welsh-Murphy ⚠️ | Lévis › Saint-Romuald | 1 |
| Parc Olympique ⚠️ | Lévis › Pintendre | 1 |
| Parc Beaumont ⚠️ | Lévis › Saint-Romuald | 1 |
| Parc Claudel ⚠️ | Lévis › Lévis (quartier) | 1 |
| Parc d'Aubigny ⚠️ | Lévis › Lévis (quartier) | 1 |
| Parc Lamartine ⚠️ | Lévis › Lévis (quartier) | 1 |
| Parc des Oiseaux ⚠️ | Lévis › Lévis (quartier) | 1 |
| Parc du Domaine-des-Bois ⚠️ | Lévis › Lévis (quartier) | 1 |
| Parc-école des Mousserons ⚠️ | Lévis › Saint-Jean-Chrysostome | 1 |
| Parc de Verdun ⚠️ | Lévis › Lévis (quartier) | 1 |
| Parc Villemay ⚠️ | Lévis › Lévis (quartier) | 1 |
| Parc Georges-Berberi ⚠️ | Lévis › Lévis (quartier) | 1 |
| Parc des Opales ⚠️ | Lévis › Lévis (quartier) | 1 |
| Parc O'Bernois ⚠️ | Lévis › Saint-Nicolas | 1 |
| Parc du Coteau-Chevreuil ⚠️ | Lévis › Saint-Nicolas | 1 |
| Parc des Châtelets ⚠️ | Lévis › Saint-Étienne-de-Lauzon | 1 |
| Parc-école La Clé-du-Boisé ⚠️ | Lévis › Saint-Étienne-de-Lauzon | 1 |
| Parc des Chênes ⚠️ | Lévis › Sainte-Hélène-de-Breakeyville | 1 |
| Parc des Trois-Manoirs ⚠️ | Lévis › Sainte-Hélène-de-Breakeyville | 1 |
| Parc de la Viorne ⚠️ | Lévis › Sainte-Hélène-de-Breakeyville | 1 |
| Parc de la Pruchière ⚠️ | Lévis › Saint-Nicolas | 1 |
| Parc du Replat ⚠️ | Lévis › Saint-Nicolas | 1 |
| Carré Huot ⚠️ | Lévis › Saint-Nicolas | 1 |
| Terrain de Baseball ⚠️ | Lévis › Saint-Étienne-de-Lauzon | 1 |
| Terrains de soccer ⚠️ | Lévis › Saint-Étienne-de-Lauzon | 1 |
| Parc Plein-Soleil ⚠️ | Lévis › Saint-Étienne-de-Lauzon | 1 |
| Parc-école Sainte-Marie ⚠️ | Lévis › Lévis (quartier) | 1 |
| Parc des Aînées ⚠️ | Lévis › Saint-Étienne-de-Lauzon | 1 |
| Parc de Lévis (9) ⚠️ | Lévis › Saint-Romuald | 1 |
| Place de l'Hôtel-de-Ville ⚠️ | Lévis › Saint-Romuald | 1 |
| Parc de Lévis (10) ⚠️ | Lévis › Lévis (quartier) | 1 |
| Parc des Compositeurs ⚠️ | Lévis › Lévis (quartier) | 1 |
| Parc du Moulin ⚠️ | Lévis › Saint-Jean-Chrysostome | 1 |
| Parc de la Pointe-Benson ⚠️ | Lévis › Saint-Romuald | 1 |
| Parc du Manoir-Wade ⚠️ | Lévis › Saint-Romuald | 1 |
| Parc de la Halte ⚠️ | Lévis › Charny | 1 |
| Parc de Lévis (12) ⚠️ | Lévis › Saint-Rédempteur | 1 |
| Parc Thomas-Chapais ⚠️ | Lévis › Lévis (quartier) | 1 |
| Parc Hector-Fabre ⚠️ | Lévis › Lévis (quartier) | 1 |
| Parc du Lac-Bargoné ⚠️ | Lévis › Saint-Joseph-de-la-Pointe-De Lévy | 1 |
| Parc André-Guay ⚠️ | Lévis › Lévis (quartier) | 1 |
| Parc de l'Aréna André-Lacroix ⚠️ | Lévis › Lévis (quartier) | 1 |
| Parc de l'Armurier ⚠️ | Lévis › Lévis (quartier) | 1 |
| Parc du Batelier ⚠️ | Lévis › Lévis (quartier) | 1 |
| Parc Saindon ⚠️ | Lévis › Saint-Étienne-de-Lauzon | 1 |
| Parc du Fort-de-la-Martinière ⚠️ | Lévis › Lévis (quartier) | 1 |
| Parc du Moulin-Ruel ⚠️ | Lévis › Lévis (quartier) | 1 |
| Parc Langelier ⚠️ | Lévis › Lévis (quartier) | 1 |
| Parc de Coutances ⚠️ | Lévis › Pintendre | 1 |
| Parc de Lévis (15) ⚠️ | Lévis › Pintendre | 1 |
| Parc des Petits Jardins ⚠️ | Lévis › Pintendre | 1 |
| Parc Plante ⚠️ | Lévis › Pintendre | 1 |
| Parc de Lévis (20) ⚠️ | Lévis › Lévis (quartier) | 1 |
| Parc de Lévis (21) ⚠️ | Lévis › Sainte-Hélène-de-Breakeyville | 1 |
| Parc de la Marina-de-la-Chaudière ⚠️ | Lévis › Saint-Romuald | 1 |
| Parc de Bernières-sur-Mer ⚠️ | Lévis › Saint-Nicolas | 1 |
| Parc Élisabeth-Bélanger-Rousseau ⚠️ | Lévis › Saint-Étienne-de-Lauzon | 1 |
| Parc de Lévis (22) ⚠️ | Lévis › Lévis (quartier) | 1 |
| Parc de Lévis (23) ⚠️ | Lévis › Pintendre | 1 |
| Parc Lucie-Dugas ⚠️ | Lévis › Saint-Jean-Chrysostome | 1 |
| Parc du Christ-Roi ⚠️ | Lévis › Lévis (quartier) | 1 |

133 parc(s) plus petits qu'une cellule ne sont pas listés : la carte les dessine, mais ils n'offrent aucune cellule.

⚠️ 226 parc(s) hors de la fenêtre 10–125 cellules (226 trop petit(s), 0 trop grand(s)) : affichés sur la carte, mais ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| airport | 21 |
| military | 0 |
| prison | 0 |
| **Total déclaré** | **21** |
| dont dans une zone de ce territoire | 21 |


### Zones concernées

| Zone | Cellules exclues |
|---|---:|
| Lévis | 21 |
| Saint-Jean-Chrysostome | 14 |
| Pintendre | 7 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
