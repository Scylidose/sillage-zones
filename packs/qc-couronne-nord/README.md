# Couronne Nord (Laurentides–Lanaudière)

Pack `qc-couronne-nord` · version 1.1.0 · grille 200 m · Canada › Québec › Grand Montréal

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
| Parcs | 772 |

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
| Mirabel | 24 772 | 1 | 24 771 | 1 018 | **23 753** | 44 |
| Terrebonne | 8 232 | 254 | 7 978 | 25 | **7 953** | 69 |
| Mascouche | 5 528 | 39 | 5 489 | 0 | **5 489** | 23 |
| L'Assomption | 5 099 | 4 | 5 095 | 0 | **5 095** | 19 |
| Sainte-Anne-des-Plaines | 4 840 | 1 | 4 839 | 91 | **4 748** | 9 |
| Saint-Jérôme | 4 670 | 1 | 4 669 | 0 | **4 669** | 33 |
| Saint-Eustache | 3 710 | 126 | 3 584 | 0 | **3 584** | 15 |
| Repentigny | 3 656 | 552 | 3 104 | 0 | **3 104** | 37 |
| Oka | 4 413 | 1 514 | 2 899 | 0 | **2 899** | 2 |
| Blainville | 2 842 | 35 | 2 807 | 248 | **2 559** | 33 |
| Saint-Joseph-du-Lac | 2 120 | 15 | 2 105 | 0 | **2 105** | 3 |
| Saint-Sulpice | 1 863 | 0 | 1 863 | 0 | **1 863** | 1 |
| Boisbriand | 1 525 | 84 | 1 441 | 0 | **1 441** | 19 |
| Rosemère | 624 | 69 | 555 | 0 | **555** | 11 |
| Sainte-Thérèse | 479 | 0 | 479 | 0 | **479** | 14 |
| Sainte-Marthe-sur-le-Lac | 432 | 1 | 431 | 0 | **431** | 7 |
| Deux-Montagnes | 368 | 53 | 315 | 0 | **315** | 4 |
| Lorraine | 311 | 4 | 307 | 0 | **307** | 7 |
| Pointe-Calumet | 593 | 356 | 237 | 0 | **237** | 2 |
| Bois-des-Filion | 251 | 20 | 231 | 0 | **231** | 4 |
| Charlemagne | 116 | 9 | 107 | 0 | **107** | 5 |

## Parcs (772)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Parc national d'Oka ⚠️ | Oka | 796 |
| Parc du Domaine Vert ⚠️ | Mirabel | 138 |
| Parc du Domaine Vert (2) | Mirabel | 99 |
| Parc régional Bois de Belle-Rivière | Mirabel | 88 |
| Parc Faunique Domaine du Parc (Ruisseau de Feu) | Terrebonne | 75 |
| Parc du Grand-Coteau | Mascouche | 64 |
| Parc régional de la Rivière-du-Nord | Saint-Jérôme | 62 |
| Parc nature Saint-Eustache | Saint-Eustache | 61 |
| Parc de Blainville (3) | Blainville | 30 |
| Parc de Terrebonne (26) | Terrebonne | 21 |
| Parc Marais Tylee | Rosemère | 14 |
| Parc de l'Île-Lebel | Repentigny | 12 |
| Parc de la Rivière-des-Mille-Îles (2) | Boisbriand | 12 |
| Parc Équestre | Blainville | 11 |
| Réserve écologique de l'Île-Garth ⚠️ | Bois-des-Filion | 9 |
| Parc écologique de l'Assomption ⚠️ | L'Assomption | 8 |
| Réserve naturelle du Boisé-Roger-Lemoine ⚠️ | Deux-Montagnes | 8 |
| Parc Angora ⚠️ | Terrebonne | 7 |
| Parc des Bolivars ⚠️ | Blainville | 7 |
| Boisé du Parc Équestre ⚠️ | Blainville | 7 |
| Réserve naturelle de l'Île des Juifs ⚠️ | Rosemère | 7 |
| Parc Lorraine ⚠️ | Lorraine | 6 |
| Parc des Méandres (2) ⚠️ | Sainte-Anne-des-Plaines | 6 |
| Parc Jacques-Locas ⚠️ | Saint-Jérôme | 6 |
| Parc Vaillant ⚠️ | Terrebonne | 5 |
| Parc Charbonneau (2) ⚠️ | Rosemère | 5 |
| Parc Régional ⚠️ | Boisbriand | 5 |
| Parc de Boisbriand ⚠️ | Boisbriand | 5 |
| Parc Blainville ⚠️ | Blainville | 5 |
| Parc Des Hirondelles (2) ⚠️ | Blainville | 5 |
| Parc Horizon-Jeunesse ⚠️ | Saint-Jérôme | 5 |
| Parc du lac Claude ⚠️ | Saint-Jérôme | 5 |
| Parc du Sommet ⚠️ | Mirabel | 5 |
| Parc naturel de Rivière-à-Gagnon ⚠️ | Saint-Jérôme | 5 |
| Parc Léo Jacques ⚠️ | L'Assomption | 4 |
| Parc Paul-Gohier ⚠️ | Mascouche | 4 |
| Parc Honorine-Melançon ⚠️ | Saint-Jérôme | 4 |
| Parc de l'école secondaire des Patriotes ⚠️ | Saint-Eustache | 4 |
| Parc de la Source ⚠️ | Saint-Jérôme | 4 |
| Parc Gingras ⚠️ | Mirabel | 4 |
| Parc Jean-Claude-Crevier ⚠️ | Repentigny | 4 |
| Parc Ducharme ⚠️ | Sainte-Thérèse | 4 |
| Le Jardins des Sources ⚠️ | Sainte-Thérèse | 4 |
| Parc Donat-Belisle ⚠️ | Terrebonne | 3 |
| Centre d'Interprétation de la nature ⚠️ | Boisbriand | 3 |
| Parc Champigny ⚠️ | Repentigny | 3 |
| Parc Saint-Laurent (4) ⚠️ | Repentigny | 3 |
| Parc Laverdière ⚠️ | Repentigny | 3 |
| Parc Rivest ⚠️ | Repentigny | 3 |
| Parc Louis-Fréchette  ⚠️ | Repentigny | 3 |
| Parc Des Moissons ⚠️ | L'Assomption | 3 |
| Parc Chénier ⚠️ | Saint-Eustache | 3 |
| Parc des Braves (Île-des-Moulins) ⚠️ | Terrebonne | 3 |
| Parc René-Lévesque (2) ⚠️ | Boisbriand | 3 |
| Parc Cardinal ⚠️ | Mirabel | 3 |
| Parc Philippe-Villeneuve ⚠️ | Terrebonne | 3 |
| Parc Henri-Dunant ⚠️ | Blainville | 3 |
| Parc de Fontainebleau ⚠️ | Blainville | 3 |
| Parc des Méandres ⚠️ | Terrebonne | 3 |
| Parc du Boisé ⚠️ | Terrebonne | 3 |
| Parc Maurice-Richard ⚠️ | Repentigny | 3 |
| Parc du complexe Jean-Laurin ⚠️ | Mirabel | 3 |
| Espace Vert ⚠️ | Mirabel | 3 |
| Parc de la Rivière (4) ⚠️ | Terrebonne | 3 |
| Parc André-Guérard ⚠️ | Terrebonne | 3 |
| Parc Maurice-Tessier (3) ⚠️ | Blainville | 3 |
| Parc Saint-Sacrement ⚠️ | Terrebonne | 2 |
| Parc Corbeil ⚠️ | Terrebonne | 2 |
| Parc André-Clément ⚠️ | Lorraine | 2 |
| Parc des Sorbiers ⚠️ | Lorraine | 2 |
| Marais Le Bouthillier ⚠️ | Rosemère | 2 |
| Parc Bourbonnière (2) ⚠️ | Rosemère | 2 |
| Parc Derek-Aucoin ⚠️ | Boisbriand | 2 |
| Parc Larochelle ⚠️ | Repentigny | 2 |
| Parc du Moulin  ⚠️ | Repentigny | 2 |
| Parc des Moissons  ⚠️ | Repentigny | 2 |
| Parc de la Pointe de l'Ile ⚠️ | Terrebonne | 2 |
| Parc Central ⚠️ | Deux-Montagnes | 2 |
| Parc De Sève ⚠️ | Sainte-Thérèse | 2 |
| Parc Olympia (2) ⚠️ | Deux-Montagnes | 2 |
| Parc Pierre-Laporte (3) ⚠️ | Terrebonne | 2 |
| Parc Gilles Forest ⚠️ | Mascouche | 2 |
| Parc Rivière-Nord ⚠️ | Saint-Eustache | 2 |
| Parc Dumais ⚠️ | Terrebonne | 2 |
| Parc de Boisbriand (2) ⚠️ | Boisbriand | 2 |
| Parc Binette ⚠️ | Mirabel | 2 |
| Parc Marc-Aurèle-Fortin ⚠️ | Blainville | 2 |
| Parc Schulz ⚠️ | Saint-Jérôme | 2 |
| Parc Optimiste-Saint-Antoine ⚠️ | Saint-Jérôme | 2 |
| Parc Félix-Leclerc (2) ⚠️ | Blainville | 2 |
| Parc Frédéric-Coiteux ⚠️ | Repentigny | 2 |
| Parc des Intendants ⚠️ | Mirabel | 2 |
| Parc de la Seigneurie (5) ⚠️ | Mascouche | 2 |
| Parc de Terrebonne (6) ⚠️ | Terrebonne | 2 |
| Parc les Jardins du Manoir ⚠️ | Saint-Eustache | 2 |
| Parc municipal ⚠️ | Sainte-Marthe-sur-le-Lac | 2 |
| Parc Dupuis ⚠️ | Mascouche | 2 |
| Parc des Pins (3) ⚠️ | Mascouche | 2 |
| Parc des Vignobles ⚠️ | Terrebonne | 2 |
| Parc de la Halte-Routière ⚠️ | Terrebonne | 2 |
| Parc des Ruisseaux ⚠️ | Terrebonne | 2 |
| Parc Louis-Laberge ⚠️ | Terrebonne | 2 |
| Parc Arc-en-Ciel ⚠️ | Terrebonne | 2 |
| Parc Rochefort  ⚠️ | Repentigny | 2 |
| Parc de la Montagne ⚠️ | Mirabel | 2 |
| Parc Maurice-Tessier (2) ⚠️ | Blainville | 2 |
| Parc des Semailles ⚠️ | Blainville | 2 |
| Parc du Partage ⚠️ | L'Assomption | 2 |
| Parc Des Christin ⚠️ | L'Assomption | 2 |
| Parc Placide-Cormier ⚠️ | L'Assomption | 2 |
| Parc du Régiment-de-la-Sarre ⚠️ | L'Assomption | 2 |
| Parc Marcel-de la Sablonnière ⚠️ | Terrebonne | 2 |
| Parc Louis-Gilles-Ouimet ⚠️ | Terrebonne | 2 |
| Parc des Saisons ⚠️ | Sainte-Anne-des-Plaines | 2 |
| Parc Jean-Paul Charbonneau ⚠️ | Mirabel | 2 |
| Parc du Centre-Communautaire (2) ⚠️ | Mirabel | 2 |
| Parc Boisé des Moissons ⚠️ | Saint-Eustache | 2 |
| Parc Jean-Maurice-Éthier ⚠️ | Sainte-Thérèse | 2 |
| Parc De La Clairière ⚠️ | Boisbriand | 2 |
| Parc Masson ⚠️ | Terrebonne | 1 |
| Jardin du Souvenir ⚠️ | Rosemère | 1 |
| Parc Hamilton (2) ⚠️ | Rosemère | 1 |
| Parc de Rosemère (2) ⚠️ | Rosemère | 1 |
| Parc Perron ⚠️ | Boisbriand | 1 |
| Parc Chenier ⚠️ | Boisbriand | 1 |
| Parc Gabrielle-Roy (2) ⚠️ | Boisbriand | 1 |
| Parc Blais ⚠️ | Boisbriand | 1 |
| Parc Julien ⚠️ | Boisbriand | 1 |
| Parc Jean-Jacques Rousseau ⚠️ | Boisbriand | 1 |
| Parc Saint-Jacques (2) ⚠️ | Sainte-Thérèse | 1 |
| Parc Damase-Juteau ⚠️ | Sainte-Thérèse | 1 |
| Parc de la Rivière (2) ⚠️ | Sainte-Thérèse | 1 |
| Parc Richelieu ⚠️ | Sainte-Thérèse | 1 |
| Parc Dubreuil ⚠️ | Blainville | 1 |
| Parc des Liserons ⚠️ | Blainville | 1 |
| Parc Des Mélèzes ⚠️ | Blainville | 1 |
| Parc Jacques-Laurin ⚠️ | Charlemagne | 1 |
| Parc de la Coopérative ⚠️ | Repentigny | 1 |
| Parc Laforest ⚠️ | Repentigny | 1 |
| Parc Montcalm ⚠️ | Repentigny | 1 |
| Parc des Érables ⚠️ | Repentigny | 1 |
| Parc Amédée-Meunier ⚠️ | Repentigny | 1 |
| ParcThifault ⚠️ | Repentigny | 1 |
| Parc Optimiste ⚠️ | Oka | 1 |
| Parc Pager ⚠️ | Mirabel | 1 |
| Parc Lacombe ⚠️ | Mirabel | 1 |
| Parc du Gouffre ⚠️ | Terrebonne | 1 |
| Parc Des Artisants ⚠️ | Repentigny | 1 |
| Parc Chamberland  ⚠️ | Repentigny | 1 |
| Parc De La Seigneurie ⚠️ | Repentigny | 1 |
| Parc La Tourterelle  ⚠️ | Repentigny | 1 |
| Parc Sanguinet ⚠️ | Repentigny | 1 |
| Parc Lachapelle ⚠️ | Repentigny | 1 |
| Parc Juneau (2) ⚠️ | L'Assomption | 1 |
| Parc Laurier (2) ⚠️ | L'Assomption | 1 |
| Parc André-Courcelles ⚠️ | L'Assomption | 1 |
| Parc de Saint-Sulpice ⚠️ | Saint-Sulpice | 1 |
| Parc de la Rivière-des-Mille-Îles ⚠️ | Rosemère | 1 |
| Promenade de la Rivière-du-Chêne (2) ⚠️ | Saint-Eustache | 1 |
| Parc de Bois-des-Filion ⚠️ | Bois-des-Filion | 1 |
| Parc Coulombe Saint-Marcoux ⚠️ | Blainville | 1 |
| Parc Marie-Victorin (2) ⚠️ | Blainville | 1 |
| Parc Champagne ⚠️ | Pointe-Calumet | 1 |
| Parc de Saint-Eustache ⚠️ | Saint-Eustache | 1 |
| Parc de Mascouche ⚠️ | Mascouche | 1 |
| Parc de Mascouche (3) ⚠️ | Mascouche | 1 |
| Parc Clair Matin ⚠️ | Saint-Eustache | 1 |
| Parc Sarrazin ⚠️ | Terrebonne | 1 |
| Parc Saint-Malo ⚠️ | Terrebonne | 1 |
| Parc Saint-Louis (2) ⚠️ | Terrebonne | 1 |
| Parc Longchamps ⚠️ | Terrebonne | 1 |
| Parc Armand-Nadeau ⚠️ | Mascouche | 1 |
| Parc Memorial ⚠️ | Mascouche | 1 |
| Parc de Terrebonne (2) ⚠️ | Terrebonne | 1 |
| Parc Jean-Guy-Mathers ⚠️ | Saint-Eustache | 1 |
| Parc Robert ⚠️ | Boisbriand | 1 |
| Parc Claude-Henri-Grignon ⚠️ | Blainville | 1 |
| Parc Chante-Bois ⚠️ | Blainville | 1 |
| Parc Des Chênes ⚠️ | Lorraine | 1 |
| Parc Rochon ⚠️ | Mirabel | 1 |
| Parc de la Loire ⚠️ | Mirabel | 1 |
| Parc de la Rochelle ⚠️ | Mirabel | 1 |
| Parc de Terrebonne (3) ⚠️ | Terrebonne | 1 |
| Parc de Terrebonne (4) ⚠️ | Terrebonne | 1 |
| Parc des Bois-Francs ⚠️ | Mascouche | 1 |
| Parc Laurier (3) ⚠️ | Terrebonne | 1 |
| Parc Trudel ⚠️ | Terrebonne | 1 |
| Parc du Nord ⚠️ | Mascouche | 1 |
| Parc Maurice-Saint-Pierre ⚠️ | Saint-Jérôme | 1 |
| Parc Jean-Baptiste-Rolland ⚠️ | Saint-Jérôme | 1 |
| Parc de la Côte-Parent ⚠️ | Saint-Jérôme | 1 |
| Parc des Soeurs-Notre-Dame-du-Bon-Conseil ⚠️ | Saint-Jérôme | 1 |
| Parc Bouvrette ⚠️ | Saint-Jérôme | 1 |
| Parc du Domaine (2) ⚠️ | Saint-Jérôme | 1 |
| Parc Monseigneur-Émile-Dubois ⚠️ | Saint-Jérôme | 1 |
| Parc des Optimistes ⚠️ | Mascouche | 1 |
| Parc Neuville ⚠️ | Sainte-Anne-des-Plaines | 1 |
| Parc Henri-Daoust ⚠️ | Saint-Jérôme | 1 |
| Parc de Saint-Jérôme (2) ⚠️ | Saint-Jérôme | 1 |
| Parc Pablo-Picasso ⚠️ | Mirabel | 1 |
| Parc Victor-:Lapointe ⚠️ | Mirabel | 1 |
| Parc des Vignes ⚠️ | Terrebonne | 1 |
| Parc des Mesanges ⚠️ | Terrebonne | 1 |
| Parc d'Alençcon ⚠️ | Blainville | 1 |
| Parc Joseph-Masson ⚠️ | Blainville | 1 |
| Parc Notre-Dame-de-l'Assomption ⚠️ | Blainville | 1 |
| Parc Maurice-Tessier ⚠️ | Blainville | 1 |
| Parc de Montauban ⚠️ | Blainville | 1 |
| Parc de Blainville ⚠️ | Blainville | 1 |
| Parc du Plateau St-Louis ⚠️ | Blainville | 1 |
| Parc des Chanterelles ⚠️ | Blainville | 1 |
| Parc du Ruisseau ⚠️ | Blainville | 1 |
| Parc de l'Assomption ⚠️ | L'Assomption | 1 |
| Parc des Roseaux ⚠️ | Blainville | 1 |
| Parc Beauséjour ⚠️ | Sainte-Thérèse | 1 |
| Parc de l'Écluse ⚠️ | Mirabel | 1 |
| Parc du Colombier ⚠️ | Saint-Jérôme | 1 |
| Parc Bigras (2) ⚠️ | Terrebonne | 1 |
| Parc Entramis ⚠️ | Repentigny | 1 |
| Parc de l'Esplanade ⚠️ | Mascouche | 1 |
| Parc des Francs-Bourgeois ⚠️ | Boisbriand | 1 |
| Parc Jacques-Beauchamp ⚠️ | Mirabel | 1 |
| Parc Prud'homme (Parc école au Coeur-du-Boisé) ⚠️ | Saint-Eustache | 1 |
| Parc des Anges ⚠️ | Sainte-Marthe-sur-le-Lac | 1 |
| Parc Félix-Leclerc (3) ⚠️ | Sainte-Marthe-sur-le-Lac | 1 |
| Parc des Pins (2) ⚠️ | Sainte-Marthe-sur-le-Lac | 1 |
| Parc Taschereau ⚠️ | Mirabel | 1 |
| Parc Joseph-Adélard Godbout ⚠️ | Mirabel | 1 |
| Parc Vermette ⚠️ | Mirabel | 1 |
| Parc Félix-Antoine-Savard (2) ⚠️ | Mirabel | 1 |
| Parc Jean-Talon ⚠️ | Mirabel | 1 |
| Parc Hombourg ⚠️ | Lorraine | 1 |
| Parc Havre-Du-Lac ⚠️ | Terrebonne | 1 |
| Parc Des Nations-Unies ⚠️ | Mascouche | 1 |
| Parc Marie des Hauts-Bois ⚠️ | Mascouche | 1 |
| Parc La Source  ⚠️ | Mascouche | 1 |
| Parc De l’Envolée ⚠️ | Mascouche | 1 |
| Parc des Ancêtres (2) ⚠️ | Mascouche | 1 |
| Parc Soleil-Levant  ⚠️ | Mascouche | 1 |
| Parc Bras d'Apic ⚠️ | Terrebonne | 1 |
| Parc Charles-Bruneau ⚠️ | Terrebonne | 1 |
| Parc Patrick ⚠️ | Terrebonne | 1 |
| Parc Île-des-Lys ⚠️ | Terrebonne | 1 |
| Parc St-Denis ⚠️ | Terrebonne | 1 |
| Parc Place Comtois ⚠️ | Terrebonne | 1 |
| Parc Vérone ⚠️ | Terrebonne | 1 |
| Parc Assigny ⚠️ | Terrebonne | 1 |
| Parc Plaisance (2) ⚠️ | Terrebonne | 1 |
| Parc Le Castelet ⚠️ | Terrebonne | 1 |
| Parc Larochelle (2) ⚠️ | Terrebonne | 1 |
| Parc de l'Étincelle ⚠️ | Terrebonne | 1 |
| Parc des Coccinelles ⚠️ | Terrebonne | 1 |
| Parc Guillemette ⚠️ | Terrebonne | 1 |
| Parc de l'Hémérocalle ⚠️ | Terrebonne | 1 |
| Parc Racine (2) ⚠️ | Sainte-Anne-des-Plaines | 1 |
| Parc Fafard ⚠️ | Terrebonne | 1 |
| Parc Médéric-Lebeau ⚠️ | Charlemagne | 1 |
| Parc Des-Rives ⚠️ | Charlemagne | 1 |
| Parc faunique 640 ⚠️ | Charlemagne | 1 |
| Parc de Terrebonne (9) ⚠️ | Terrebonne | 1 |
| Parc Catherine-Bousquet ⚠️ | Repentigny | 1 |
| Parc de Saint-Jérôme (3) ⚠️ | Saint-Jérôme | 1 |
| Parc Jean-Guy Décarie ⚠️ | Saint-Jérôme | 1 |
| Parc de Saint-Jérôme (4) ⚠️ | Saint-Jérôme | 1 |
| Parc De la Durantaye ⚠️ | Saint-Jérôme | 1 |
| Place de la Gare ⚠️ | Saint-Jérôme | 1 |
| Parc Geai-Bleu ⚠️ | Saint-Jérôme | 1 |
| Parc La Salette ⚠️ | Saint-Jérôme | 1 |
| Parc du Marbre ⚠️ | Mirabel | 1 |
| Parc de la Silice ⚠️ | Mirabel | 1 |
| Parc du Granite ⚠️ | Mirabel | 1 |
| Parc Lucien-Meilleur ⚠️ | Mirabel | 1 |
| Parc du Bosquet ⚠️ | Mirabel | 1 |
| Parc Raymond-Fortier ⚠️ | Mirabel | 1 |
| Parc Émile-Berthelot ⚠️ | Mirabel | 1 |
| Parc Jacques Paquin ⚠️ | Saint-Joseph-du-Lac | 1 |
| Parc Filiatrault ⚠️ | Boisbriand | 1 |
| Parc des Jardins (2) ⚠️ | Saint-Jérôme | 1 |
| Parc Charles-Édouard-Renaud ⚠️ | Terrebonne | 1 |
| Parc Bédo-Laurin ⚠️ | Mirabel | 1 |
| Parc de la Rive ⚠️ | Mirabel | 1 |
| Parc Ludger-Duvernay ⚠️ | Saint-Jérôme | 1 |
| Parc du Mont Saint-Eustache ⚠️ | Saint-Eustache | 1 |
| Parc Moir ⚠️ | Deux-Montagnes | 1 |
| Parc des Saules (4) ⚠️ | Lorraine | 1 |
| Parc de Lorraine (9) ⚠️ | Lorraine | 1 |
| Parc de l'Étang des Sources ⚠️ | L'Assomption | 1 |
| Parc linéaire de la Gare-de-Vaucluse ⚠️ | L'Assomption | 1 |
| Parc des Premières-Nations ⚠️ | Repentigny | 1 |
| Parc Robert-Duguay ⚠️ | L'Assomption | 1 |
| Parc Antonio Saint-Roch ⚠️ | L'Assomption | 1 |
| Parc Saint-Louis (3) ⚠️ | L'Assomption | 1 |
| Parc François-Varin ⚠️ | L'Assomption | 1 |
| Carré de la Paruline Jaune ⚠️ | Terrebonne | 1 |
| Parc de l'Engoulevent ⚠️ | Terrebonne | 1 |
| Parc de la Pommeraie ⚠️ | Terrebonne | 1 |
| Parc de Bois-des-Filion (2) ⚠️ | Bois-des-Filion | 1 |
| Espace Vert Chemin du Côteau ⚠️ | Terrebonne | 1 |
| Parc Vallée-des-Rois ⚠️ | Terrebonne | 1 |
| Parc de Sainte-Anne-des-Plaines (2) ⚠️ | Sainte-Anne-des-Plaines | 1 |
| Parc Boisvert (2) ⚠️ | Terrebonne | 1 |
| Parc Pedro-Da Silva ⚠️ | Blainville | 1 |
| Parc de Mirabel (3) ⚠️ | Mirabel | 1 |
| Parc Charlebel ⚠️ | Mirabel | 1 |
| Parc de l'Assomption (3) ⚠️ | L'Assomption | 1 |
| Parc du Ruisseau (5) ⚠️ | Blainville | 1 |
| Parc Désormeaux ⚠️ | Saint-Eustache | 1 |
| Parc de Terrebonne (12) ⚠️ | Terrebonne | 1 |
| Parc de Repentigny ⚠️ | Repentigny | 1 |
| Parc de Repentigny (2) ⚠️ | Repentigny | 1 |
| Place Fernand-Lyndsay ⚠️ | Repentigny | 1 |
| Parc de Repentigny (5) ⚠️ | Repentigny | 1 |
| Parc de Repentigny (6) ⚠️ | Repentigny | 1 |
| Parc de Repentigny (7) ⚠️ | Repentigny | 1 |
| Parc de Mirabel (4) ⚠️ | Mirabel | 1 |
| Parc Canin Le Gardeur/Bassin Lefebvre ⚠️ | Repentigny | 1 |
| Parc de Sainte-Anne-des-Plaines (3) ⚠️ | Sainte-Anne-des-Plaines | 1 |
| Parc de la Fabrique (2) ⚠️ | Terrebonne | 1 |
| Fun Show Amusement ⚠️ | Mirabel | 1 |
| Parc de Sainte-Anne-des-Plaines (4) ⚠️ | Sainte-Anne-des-Plaines | 1 |
| Parc de Sainte-Marthe-sur-le-Lac ⚠️ | Sainte-Marthe-sur-le-Lac | 1 |
| Parc Chambéry ⚠️ | Mascouche | 1 |
| Parc des Hauteurs ⚠️ | Saint-Jérôme | 1 |
| Parc de Terrebonne (18) ⚠️ | Terrebonne | 1 |
| Parc Desrosiers ⚠️ | Repentigny | 1 |
| Parc de Saint-Jérôme (18) ⚠️ | Saint-Jérôme | 1 |
| Parc du Bourg-Fleuri ⚠️ | L'Assomption | 1 |
| Parc de Saint-Jérôme (19) ⚠️ | Saint-Jérôme | 1 |
| Parc Gabriel-Labelle ⚠️ | Sainte-Thérèse | 1 |
| Parc de la Pinière ⚠️ | Terrebonne | 1 |
| Parc Daunais ⚠️ | Terrebonne | 1 |
| Parc Alphonse-Gravel ⚠️ | Pointe-Calumet | 1 |
| Parc de Saint-Joseph-du-Lac (5) ⚠️ | Saint-Joseph-du-Lac | 1 |
| Parc de la Presqu'île ⚠️ | Charlemagne | 1 |
| Parc de Mirabel (8) ⚠️ | Mirabel | 1 |
| Parc Rollans LaLiberté ⚠️ | Sainte-Marthe-sur-le-Lac | 1 |
| Parc de Mirabel (9) ⚠️ | Mirabel | 1 |
| Parc Le Belvédère ⚠️ | Sainte-Thérèse | 1 |
| Parc Émile-Maillé ⚠️ | Sainte-Thérèse | 1 |
| Parc de Saint-Eustache (5) ⚠️ | Saint-Eustache | 1 |
| Parc Desjardins (2) ⚠️ | Boisbriand | 1 |
| Parc Pellerin ⚠️ | Boisbriand | 1 |
| Parc Westgate ⚠️ | Rosemère | 1 |
| Parc Saint-Pierre (4) ⚠️ | Sainte-Thérèse | 1 |
| Parc naturel des Coudriers ⚠️ | Saint-Jérôme | 1 |
| Parc Paul-Yvon-Lauzon ⚠️ | Saint-Joseph-du-Lac | 1 |
| Parc Jean-Guy Cardinal ⚠️ | Sainte-Anne-des-Plaines | 1 |
| Parc des Familles ⚠️ | Sainte-Anne-des-Plaines | 1 |
| Parc de Terrebonne (22) ⚠️ | Terrebonne | 1 |
| Parc de Sainte-Marthe-sur-le-Lac (6) ⚠️ | Sainte-Marthe-sur-le-Lac | 1 |
| Parc de Saint-Jérôme (22) ⚠️ | Saint-Jérôme | 1 |
| Parc de Chambéry ⚠️ | Blainville | 1 |
| Parc de Rosemère (6) ⚠️ | Rosemère | 1 |
| Parc du Ruisseau (9) ⚠️ | Mascouche | 1 |
| Parc Lacroix (3) ⚠️ | Mirabel | 1 |
| Parc Espace-Vert ⚠️ | Mirabel | 1 |
| Parc Verdon ⚠️ | Sainte-Thérèse | 1 |
| Parc de Saint-Eustache (7) ⚠️ | Saint-Eustache | 1 |
| Parc Riverain (3) ⚠️ | Bois-des-Filion | 1 |
| Parc Le Rucher ⚠️ | Mascouche | 1 |
| Parc Jean-Baptiste-Meilleur ⚠️ | Repentigny | 1 |

411 parc(s) plus petits qu'une cellule ne sont pas listés : la carte les dessine, mais ils n'offrent aucune cellule.

⚠️ 760 parc(s) hors de la fenêtre 10–125 cellules (758 trop petit(s), 2 trop grand(s)) : affichés sur la carte, mais ils ne peuvent pas servir de cible à un défi.

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
