# Deux-Sèvres

Pack `fr-deux-sevres` · version 1.0.0 · grille 200 m · France › Nouvelle-Aquitaine

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 316 708 |
| dont restreintes (aéroport, militaire, prison) | 568 |
| dont sans chemin (aucune voie à moins de 60 m) | 65 415 |
| dont en forêt, sans chemin non plus | 8 982 |
| dont traversées par un cours d'eau, sans chemin non plus | 5 027 |
| Cellules retirées par le masque d'eau | 2 540 |
| Villes | 252 |
| Arrondissements et quartiers | 0 |
| Îles | 8 |
| Parcs | 7 319 |

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
| Bocage Bressuirais | 70 040 | somme de 33 villes |
| Niortais | 42 641 | somme de 40 villes |
| Airvaudais-Val du Thouet | 12 066 | somme de 9 villes |
| Haut Val de Sèvre | 18 172 | somme de 19 villes |
| Mellois en Poitou | 67 297 | somme de 58 villes |
| Val de Gâtine | 29 205 | somme de 31 villes |
| Parthenay-Gâtine | 44 073 | somme de 38 villes |
| Thouarsais | 33 231 | somme de 24 villes |

Une île *composite* n'a pas de cellules à elle : sa progression est la somme de ses villes, et ses cellules ne lui sont jamais rattachées directement — elles compteraient deux fois.

## Villes (252)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Sans chemin | Parcs |
|---|---:|---:|---:|---:|---:|---:|---:|
| Bressuire | 9 748 | 162 | 9 586 | 0 | **9 586** | 2 198 (23 %) | 240 |
| Mauléon | 6 590 | 37 | 6 553 | 14 | **6 539** | 1 877 (29 %) | 194 |
| Argentonnay | 6 320 | 74 | 6 246 | 0 | **6 246** | 1 635 (26 %) | 129 |
| Nueil-les-Aubiers | 5 403 | 46 | 5 357 | 0 | **5 357** | 1 566 (29 %) | 145 |
| Plaine-et-Vallées | 4 995 | 21 | 4 974 | 0 | **4 974** | 696 (14 %) | 136 |
| Moncoutant-sur-Sèvre | 4 959 | 70 | 4 889 | 0 | **4 889** | 1 146 (23 %) | 29 |
| Vasles | 4 751 | 27 | 4 724 | 0 | **4 724** | 1 395 (30 %) | 41 |
| Thouars | 4 389 | 59 | 4 330 | 7 | **4 323** | 583 (13 %) | 126 |
| Val en Vignes | 4 258 | 38 | 4 220 | 0 | **4 220** | 902 (21 %) | 142 |
| Aigondigné | 3 686 | 4 | 3 682 | 0 | **3 682** | 606 (16 %) | 136 |
| Niort | 3 584 | 54 | 3 530 | 59 | **3 471** | 257 (7 %) | 253 |
| Melle | 3 427 | 8 | 3 419 | 0 | **3 419** | 446 (13 %) | 106 |
| Sauzé-entre-Bois | 3 422 | 9 | 3 413 | 0 | **3 413** | 559 (16 %) | 95 |
| Airvault | 3 416 | 15 | 3 401 | 0 | **3 401** | 471 (14 %) | 112 |
| Saint Maurice Étusson | 3 081 | 53 | 3 028 | 0 | **3 028** | 849 (28 %) | 32 |
| La Forêt-sur-Sèvre | 2 988 | 54 | 2 934 | 0 | **2 934** | 955 (33 %) | 7 |
| Assais-les-Jumeaux | 2 829 | 1 | 2 828 | 0 | **2 828** | 576 (20 %) | 52 |
| Loretz-d'Argenton | 2 840 | 28 | 2 812 | 0 | **2 812** | 474 (17 %) | 109 |
| Rom | 2 751 | 0 | 2 751 | 0 | **2 751** | 589 (21 %) | 103 |
| Valdelaume | 2 659 | 0 | 2 659 | 0 | **2 659** | 491 (18 %) | 64 |
| Gourgé | 2 687 | 66 | 2 621 | 0 | **2 621** | 696 (27 %) | 30 |
| Thénezay | 2 580 | 4 | 2 576 | 0 | **2 576** | 378 (15 %) | 60 |
| Chiché | 2 530 | 37 | 2 493 | 0 | **2 493** | 551 (22 %) | 13 |
| La Peyratte | 2 535 | 69 | 2 466 | 0 | **2 466** | 699 (28 %) | 34 |
| Plaine-d'Argenson | 2 387 | 0 | 2 387 | 0 | **2 387** | 453 (19 %) | 36 |
| Lezay | 2 386 | 13 | 2 373 | 0 | **2 373** | 371 (16 %) | 25 |
| Saint-Aubin-le-Cloud | 2 233 | 38 | 2 195 | 0 | **2 195** | 694 (32 %) | 13 |
| Celles-sur-Belle | 2 184 | 1 | 2 183 | 0 | **2 183** | 335 (15 %) | 103 |
| Chef-Boutonne | 2 127 | 3 | 2 124 | 0 | **2 124** | 464 (22 %) | 13 |
| Saint-Pardoux-Soutiers | 2 123 | 12 | 2 111 | 0 | **2 111** | 565 (27 %) | 14 |
| Secondigny | 2 004 | 25 | 1 979 | 0 | **1 979** | 534 (27 %) | 11 |
| Amailloux | 1 975 | 36 | 1 939 | 0 | **1 939** | 675 (35 %) | 4 |
| Pamproux | 1 911 | 3 | 1 908 | 13 | **1 895** | 553 (29 %) | 23 |
| Boismé | 1 898 | 13 | 1 885 | 0 | **1 885** | 603 (32 %) | 2 |
| Prailles-la-Couarde | 1 860 | 7 | 1 853 | 0 | **1 853** | 216 (12 %) | 43 |
| Saint-Varent | 1 850 | 5 | 1 845 | 0 | **1 845** | 398 (22 %) | 21 |
| La Crèche | 1 810 | 12 | 1 798 | 0 | **1 798** | 189 (11 %) | 45 |
| Fenioux | 1 804 | 7 | 1 797 | 0 | **1 797** | 467 (26 %) | 42 |
| Beugnon-Thireuil | 1 792 | 19 | 1 773 | 0 | **1 773** | 480 (27 %) | 16 |
| Frontenay-Rohan-Rohan | 1 770 | 5 | 1 765 | 0 | **1 765** | 317 (18 %) | 13 |
| Saint-Hilaire-la-Palud | 1 779 | 29 | 1 750 | 0 | **1 750** | 281 (16 %) | 56 |
| Alloinay | 1 718 | 0 | 1 718 | 0 | **1 718** | 296 (17 %) | 39 |
| Saint-Amand-sur-Sèvre | 1 740 | 22 | 1 718 | 0 | **1 718** | 542 (32 %) | 39 |
| Voulmentin | 1 703 | 11 | 1 692 | 0 | **1 692** | 479 (28 %) | 37 |
| Marigny | 1 669 | 0 | 1 669 | 0 | **1 669** | 260 (16 %) | 143 |
| Saint-Léger-de-Montbrun | 1 645 | 1 | 1 644 | 3 | **1 641** | 118 (7 %) | 47 |
| Vernoux-en-Gâtine | 1 675 | 34 | 1 641 | 0 | **1 641** | 455 (28 %) | 23 |
| Clussais-la-Pommeraie | 1 637 | 15 | 1 622 | 0 | **1 622** | 392 (24 %) | 19 |
| Échiré | 1 643 | 22 | 1 621 | 0 | **1 621** | 295 (18 %) | 17 |
| Largeasse | 1 612 | 22 | 1 590 | 0 | **1 590** | 541 (34 %) | 7 |
| Ardin | 1 583 | 3 | 1 580 | 0 | **1 580** | 211 (13 %) | 20 |
| Coulon | 1 572 | 6 | 1 566 | 0 | **1 566** | 322 (21 %) | 44 |
| Courlay | 1 576 | 13 | 1 563 | 0 | **1 563** | 365 (23 %) | 4 |
| La Ferrière-en-Parthenay | 1 555 | 3 | 1 552 | 0 | **1 552** | 358 (23 %) | 20 |
| Saint-Pierre-des-Échaubrognes | 1 568 | 26 | 1 542 | 0 | **1 542** | 602 (39 %) | 35 |
| Aubigné | 1 537 | 0 | 1 537 | 0 | **1 537** | 153 (10 %) | 12 |
| Clessé | 1 563 | 29 | 1 534 | 0 | **1 534** | 455 (30 %) | 3 |
| Val-du-Mignon | 1 502 | 2 | 1 500 | 0 | **1 500** | 255 (17 %) | 14 |
| La Chapelle-Saint-Laurent | 1 530 | 41 | 1 489 | 0 | **1 489** | 314 (21 %) | 5 |
| Villiers-en-Plaine | 1 475 | 2 | 1 473 | 0 | **1 473** | 383 (26 %) | 9 |
| Genneton | 1 487 | 19 | 1 468 | 0 | **1 468** | 412 (28 %) | 18 |
| Le Busseau | 1 480 | 13 | 1 467 | 0 | **1 467** | 393 (27 %) | 12 |
| Beaulieu-sous-Parthenay | 1 424 | 18 | 1 406 | 0 | **1 406** | 388 (28 %) | 4 |
| Verruyes | 1 405 | 11 | 1 394 | 0 | **1 394** | 295 (21 %) | 3 |
| Souvigné | 1 394 | 1 | 1 393 | 0 | **1 393** | 144 (10 %) | 55 |
| Exoudun | 1 392 | 3 | 1 389 | 8 | **1 381** | 320 (23 %) | 23 |
| Les Châteliers | 1 401 | 15 | 1 386 | 0 | **1 386** | 376 (27 %) | 7 |
| Aiffres | 1 359 | 6 | 1 353 | 0 | **1 353** | 193 (14 %) | 152 |
| Beaussais-Vitré | 1 351 | 11 | 1 340 | 0 | **1 340** | 269 (20 %) | 37 |
| Sainte-Soline | 1 347 | 9 | 1 338 | 0 | **1 338** | 335 (25 %) | 30 |
| Neuvy-Bouin | 1 352 | 15 | 1 337 | 0 | **1 337** | 463 (35 %) | 10 |
| Prahecq | 1 310 | 3 | 1 307 | 0 | **1 307** | 202 (15 %) | 121 |
| Brûlain | 1 299 | 1 | 1 298 | 0 | **1 298** | 172 (13 %) | 74 |
| Saint-Martin-de-Sanzay | 1 316 | 22 | 1 294 | 0 | **1 294** | 177 (14 %) | 83 |
| Combrand | 1 309 | 16 | 1 293 | 0 | **1 293** | 441 (34 %) | 60 |
| Fontivillié | 1 286 | 0 | 1 286 | 0 | **1 286** | 233 (18 %) | 25 |
| Secondigné-sur-Belle | 1 279 | 1 | 1 278 | 0 | **1 278** | 176 (14 %) | 33 |
| Limalonges | 1 277 | 0 | 1 277 | 0 | **1 277** | 197 (15 %) | 85 |
| Saint-Pompain | 1 281 | 5 | 1 276 | 0 | **1 276** | 335 (26 %) | 5 |
| Saint-Georges-de-Noisné | 1 312 | 38 | 1 274 | 0 | **1 274** | 183 (14 %) | 5 |
| Couture-d'Argenson | 1 259 | 1 | 1 258 | 0 | **1 258** | 232 (18 %) | 25 |
| Saint-Martin-du-Fouilloux | 1 270 | 13 | 1 257 | 0 | **1 257** | 314 (25 %) | 18 |
| Mauzé-sur-le-Mignon | 1 260 | 7 | 1 253 | 0 | **1 253** | 129 (10 %) | 19 |
| Beauvoir-sur-Niort | 1 237 | 1 | 1 236 | 0 | **1 236** | 151 (12 %) | 38 |
| Faye-l'Abbesse | 1 242 | 6 | 1 236 | 0 | **1 236** | 325 (26 %) | 13 |
| Soudan | 1 235 | 0 | 1 235 | 0 | **1 235** | 215 (17 %) | 7 |
| Allonne | 1 233 | 6 | 1 227 | 0 | **1 227** | 284 (23 %) | 5 |
| Augé | 1 230 | 8 | 1 222 | 0 | **1 222** | 203 (17 %) | 113 |
| Chizé | 1 202 | 4 | 1 198 | 0 | **1 198** | 154 (13 %) | 24 |
| Vouillé | 1 178 | 4 | 1 174 | 0 | **1 174** | 169 (14 %) | 97 |
| Azay-le-Brûlé | 1 169 | 5 | 1 164 | 0 | **1 164** | 109 (9 %) | 27 |
| Cherveux | 1 169 | 5 | 1 164 | 0 | **1 164** | 178 (15 %) | 6 |
| Saint-Loup-Lamairé | 1 194 | 32 | 1 162 | 0 | **1 162** | 70 (6 %) | 62 |
| Chenay | 1 144 | 0 | 1 144 | 0 | **1 144** | 280 (24 %) | 6 |
| Champdeniers | 1 150 | 11 | 1 139 | 0 | **1 139** | 166 (15 %) | 7 |
| Glénay | 1 145 | 6 | 1 139 | 0 | **1 139** | 210 (18 %) | 16 |
| Chey | 1 130 | 1 | 1 129 | 0 | **1 129** | 254 (22 %) | 11 |
| Granzay-Gript | 1 133 | 4 | 1 129 | 0 | **1 129** | 192 (17 %) | 111 |
| Luzay | 1 126 | 1 | 1 125 | 0 | **1 125** | 193 (17 %) | 39 |
| Loubillé | 1 123 | 0 | 1 123 | 0 | **1 123** | 211 (19 %) | 4 |
| Saint-Vincent-la-Châtre | 1 114 | 0 | 1 114 | 0 | **1 114** | 289 (26 %) | 31 |
| Saivres | 1 120 | 9 | 1 111 | 0 | **1 111** | 126 (11 %) | 28 |
| Périgné | 1 112 | 2 | 1 110 | 0 | **1 110** | 194 (17 %) | 46 |
| Saint-Généroux | 1 094 | 0 | 1 094 | 0 | **1 094** | 286 (26 %) | 21 |
| Exireuil | 1 112 | 21 | 1 091 | 0 | **1 091** | 162 (15 %) | 8 |
| Nanteuil | 1 077 | 2 | 1 075 | 0 | **1 075** | 158 (15 %) | 24 |
| Chanteloup | 1 103 | 34 | 1 069 | 0 | **1 069** | 236 (22 %) | 2 |
| Louin | 1 093 | 24 | 1 069 | 0 | **1 069** | 209 (20 %) | 15 |
| Paizay-le-Chapt | 1 069 | 2 | 1 067 | 0 | **1 067** | 127 (12 %) | 8 |
| Azay-sur-Thouet | 1 080 | 16 | 1 064 | 0 | **1 064** | 293 (28 %) | 12 |
| Ensigné | 1 050 | 0 | 1 050 | 0 | **1 050** | 132 (13 %) | 10 |
| Boussais | 1 071 | 22 | 1 049 | 0 | **1 049** | 267 (25 %) | 2 |
| Melleran | 1 045 | 0 | 1 045 | 0 | **1 045** | 202 (19 %) | 32 |
| Saint-André-sur-Sèvre | 1 056 | 11 | 1 045 | 0 | **1 045** | 335 (32 %) | 2 |
| La Chapelle-Bertrand | 1 044 | 12 | 1 032 | 0 | **1 032** | 316 (31 %) | 19 |
| Geay | 1 037 | 13 | 1 024 | 0 | **1 024** | 326 (32 %) | 2 |
| Mazières-en-Gâtine | 1 022 | 4 | 1 018 | 0 | **1 018** | 245 (24 %) | 18 |
| Clavé | 1 046 | 36 | 1 010 | 0 | **1 010** | 172 (17 %) | 3 |
| La Foye-Monjault | 1 010 | 0 | 1 010 | 0 | **1 010** | 104 (10 %) | 6 |
| Louzy | 1 009 | 2 | 1 007 | 0 | **1 007** | 103 (10 %) | 36 |
| Vausseroux | 1 018 | 12 | 1 006 | 0 | **1 006** | 306 (30 %) | 4 |
| Béceleuf | 1 009 | 4 | 1 005 | 0 | **1 005** | 167 (17 %) | 8 |
| Le Pin | 1 018 | 15 | 1 003 | 0 | **1 003** | 238 (24 %) | 41 |
| Le Tallud | 1 021 | 18 | 1 003 | 0 | **1 003** | 246 (25 %) | 5 |
| Ménigoute | 1 015 | 13 | 1 002 | 0 | **1 002** | 197 (20 %) | 8 |
| Saint-Symphorien | 1 007 | 6 | 1 001 | 0 | **1 001** | 193 (19 %) | 61 |
| Cerizay | 1 015 | 18 | 997 | 0 | **997** | 161 (16 %) | 37 |
| Asnières-en-Poitou | 994 | 0 | 994 | 0 | **994** | 151 (15 %) | 15 |
| Coulonges-sur-l'Autize | 994 | 3 | 991 | 0 | **991** | 97 (10 %) | 17 |
| Maisontiers | 992 | 8 | 984 | 0 | **984** | 277 (28 %) | 9 |
| Fors | 982 | 0 | 982 | 0 | **982** | 177 (18 %) | 92 |
| Villiers-en-Bois | 980 | 0 | 980 | 0 | **980** | 38 (4 %) | 3 |
| Marcillé | 963 | 4 | 959 | 0 | **959** | 134 (14 %) | 20 |
| Saint-Martin-de-Bernegoue | 932 | 0 | 932 | 0 | **932** | 161 (17 %) | 90 |
| Germond-Rouvre | 940 | 11 | 929 | 0 | **929** | 136 (15 %) | 13 |
| Saint-Georges-de-Rex | 931 | 4 | 927 | 0 | **927** | 166 (18 %) | 8 |
| Fomperron | 924 | 0 | 924 | 0 | **924** | 169 (18 %) | 8 |
| Coulonges-Thouarsais | 929 | 9 | 920 | 0 | **920** | 243 (26 %) | 20 |
| Mairé-Levescault | 918 | 0 | 918 | 0 | **918** | 152 (17 %) | 24 |
| Marnes | 924 | 6 | 918 | 0 | **918** | 125 (14 %) | 31 |
| Cirières | 916 | 13 | 903 | 0 | **903** | 267 (30 %) | 38 |
| Sepvret | 898 | 1 | 897 | 0 | **897** | 158 (18 %) | 33 |
| Vançais | 891 | 0 | 891 | 0 | **891** | 205 (23 %) | 10 |
| La Chapelle-Bâton | 893 | 4 | 889 | 0 | **889** | 164 (18 %) | 2 |
| Villemain | 870 | 0 | 870 | 0 | **870** | 211 (24 %) | 22 |
| Saint-Gelais | 873 | 8 | 865 | 0 | **865** | 145 (17 %) | 17 |
| Châtillon-sur-Thouet | 877 | 15 | 862 | 0 | **862** | 180 (21 %) | 11 |
| Pierrefitte | 856 | 1 | 855 | 0 | **855** | 259 (30 %) | 3 |
| Prin-Deyrançon | 837 | 5 | 832 | 0 | **832** | 87 (10 %) | 5 |
| Brioux-sur-Boutonne | 815 | 0 | 815 | 0 | **815** | 115 (14 %) | 33 |
| Saint-Paul-en-Gâtine | 813 | 6 | 807 | 0 | **807** | 153 (19 %) | 14 |
| Viennay | 831 | 25 | 806 | 0 | **806** | 225 (28 %) | 7 |
| Faye-sur-Ardin | 793 | 0 | 793 | 0 | **793** | 189 (24 %) | 10 |
| La Mothe-Saint-Héray | 794 | 2 | 792 | 0 | **792** | 90 (11 %) | 32 |
| Fontenille-Saint-Martin-d'Entraigues | 793 | 3 | 790 | 0 | **790** | 141 (18 %) | 2 |
| Cours | 781 | 8 | 773 | 0 | **773** | 204 (26 %) | 2 |
| Arçais | 792 | 21 | 771 | 0 | **771** | 110 (14 %) | 29 |
| Sansais | 792 | 22 | 770 | 0 | **770** | 123 (16 %) | 32 |
| Saint-Germain-de-Longue-Chaume | 779 | 11 | 768 | 0 | **768** | 273 (36 %) | 2 |
| Amuré | 771 | 6 | 765 | 0 | **765** | 142 (19 %) |  |
| Chauray | 763 | 9 | 754 | 0 | **754** | 65 (9 %) | 41 |
| Magné | 773 | 19 | 754 | 0 | **754** | 93 (12 %) | 52 |
| Le Retail | 754 | 6 | 748 | 0 | **748** | 209 (28 %) | 3 |
| Saint-Aubin-du-Plain | 754 | 7 | 747 | 0 | **747** | 223 (30 %) | 17 |
| Vouhé | 752 | 6 | 746 | 0 | **746** | 253 (34 %) | 7 |
| Lageon | 744 | 5 | 739 | 0 | **739** | 246 (33 %) | 4 |
| Saint-Maxire | 754 | 18 | 736 | 0 | **736** | 156 (21 %) | 4 |
| Le Vanneau-Irleau | 746 | 15 | 731 | 0 | **731** | 55 (8 %) | 30 |
| Irais | 727 | 0 | 727 | 0 | **727** | 156 (21 %) | 12 |
| Sainte-Eanne | 732 | 10 | 722 | 0 | **722** | 81 (11 %) | 42 |
| La Petite-Boissière | 719 | 2 | 717 | 0 | **717** | 228 (32 %) | 34 |
| Luché-Thouarsais | 724 | 8 | 716 | 0 | **716** | 204 (28 %) | 14 |
| Saint-Rémy | 717 | 1 | 716 | 0 | **716** | 141 (20 %) | 12 |
| Surin | 718 | 2 | 716 | 0 | **716** | 116 (16 %) | 12 |
| Bretignolles | 702 | 8 | 694 | 0 | **694** | 213 (31 %) | 29 |
| L'Absie | 698 | 10 | 688 | 0 | **688** | 131 (19 %) | 2 |
| Sainte-Verge | 689 | 8 | 681 | 0 | **681** | 46 (7 %) | 20 |
| Adilly | 688 | 10 | 678 | 0 | **678** | 234 (35 %) | 1 |
| Pompaire | 682 | 6 | 676 | 0 | **676** | 216 (32 %) | 2 |
| Saint-Martin-de-Saint-Maixent | 677 | 4 | 673 | 0 | **673** | 40 (6 %) | 45 |
| Saint-Martin-de-Mâcon | 670 | 0 | 670 | 0 | **670** | 81 (12 %) | 26 |
| Fénery | 678 | 9 | 669 | 0 | **669** | 216 (32 %) | 7 |
| Villefollet | 668 | 0 | 668 | 0 | **668** | 97 (15 %) | 22 |
| Avon | 667 | 0 | 667 | 381 | **286** | 114 (40 %) |  |
| Pressigny | 648 | 0 | 648 | 0 | **648** | 55 (8 %) | 7 |
| Messé | 647 | 1 | 646 | 0 | **646** | 170 (26 %) | 4 |
| Pamplie | 648 | 4 | 644 | 0 | **644** | 172 (27 %) | 9 |
| Les Fosses | 639 | 0 | 639 | 0 | **639** | 66 (10 %) | 12 |
| Pougne-Hérisson | 643 | 4 | 639 | 0 | **639** | 126 (20 %) | 23 |
| Aubigny | 636 | 2 | 634 | 0 | **634** | 89 (14 %) | 10 |
| Saint-Coutant | 626 | 1 | 625 | 0 | **625** | 117 (19 %) | 21 |
| Saint-Germier | 630 | 5 | 625 | 0 | **625** | 172 (28 %) | 1 |
| Bougon | 623 | 4 | 619 | 42 | **577** | 105 (18 %) | 5 |
| Scillé | 620 | 5 | 615 | 0 | **615** | 180 (29 %) | 11 |
| Le Vert | 612 | 0 | 612 | 0 | **612** | 50 (8 %) | 11 |
| Romans | 604 | 0 | 604 | 0 | **604** | 64 (11 %) | 11 |
| Saurais | 608 | 4 | 604 | 0 | **604** | 177 (29 %) | 24 |
| Sainte-Ouenne | 602 | 4 | 598 | 0 | **598** | 91 (15 %) | 25 |
| Pas-de-Jeu | 598 | 2 | 596 | 0 | **596** | 74 (12 %) | 30 |
| Vanzay | 596 | 0 | 596 | 0 | **596** | 181 (30 %) | 2 |
| Parthenay | 604 | 9 | 595 | 0 | **595** | 39 (7 %) | 23 |
| Bessines | 594 | 1 | 593 | 0 | **593** | 99 (17 %) | 26 |
| Villiers-sur-Chizé | 593 | 0 | 593 | 0 | **593** | 120 (20 %) | 11 |
| Saint-Lin | 594 | 7 | 587 | 0 | **587** | 108 (18 %) |  |
| Xaintray | 587 | 1 | 586 | 0 | **586** | 89 (15 %) | 3 |
| Saint-Maixent-de-Beugné | 588 | 4 | 584 | 0 | **584** | 116 (20 %) | 5 |
| La Boissière-en-Gâtine | 583 | 2 | 581 | 0 | **581** | 177 (30 %) |  |
| Loubigné | 580 | 2 | 578 | 0 | **578** | 142 (25 %) | 1 |
| Availles-Thouarsais | 583 | 6 | 577 | 0 | **577** | 66 (11 %) | 21 |
| Lorigné | 575 | 0 | 575 | 0 | **575** | 63 (11 %) | 9 |
| Saint-Christophe-sur-Roc | 576 | 4 | 572 | 0 | **572** | 129 (23 %) | 6 |
| Sainte-Néomaye | 562 | 0 | 562 | 0 | **562** | 82 (15 %) | 27 |
| Les Forges | 556 | 3 | 553 | 0 | **553** | 184 (33 %) | 13 |
| Saint-Marc-la-Lande | 547 | 4 | 543 | 0 | **543** | 158 (29 %) | 11 |
| Montravers | 541 | 10 | 531 | 0 | **531** | 116 (22 %) | 19 |
| Doux | 529 | 0 | 529 | 0 | **529** | 56 (11 %) | 19 |
| Lhoumois | 526 | 2 | 524 | 0 | **524** | 76 (15 %) | 12 |
| Séligné | 517 | 0 | 517 | 0 | **517** | 141 (27 %) | 18 |
| Fressines | 502 | 0 | 502 | 0 | **502** | 64 (13 %) | 22 |
| Saint-Cyr-la-Lande | 494 | 1 | 493 | 0 | **493** | 48 (10 %) | 44 |
| François | 496 | 8 | 488 | 0 | **488** | 67 (14 %) | 7 |
| Sainte-Gemme | 472 | 0 | 472 | 0 | **472** | 68 (14 %) | 2 |
| Vallans | 472 | 0 | 472 | 0 | **472** | 53 (11 %) | 3 |
| Saint-Romans-lès-Melle | 467 | 1 | 466 | 0 | **466** | 76 (16 %) | 11 |
| Reffannes | 455 | 0 | 455 | 0 | **455** | 37 (8 %) | 2 |
| Brion-près-Thouet | 450 | 0 | 450 | 0 | **450** | 75 (17 %) | 17 |
| La Rochénard | 449 | 0 | 449 | 0 | **449** | 61 (14 %) | 2 |
| Le Bourdet | 437 | 4 | 433 | 0 | **433** | 64 (15 %) | 3 |
| Saint-Laurs | 436 | 3 | 433 | 0 | **433** | 67 (15 %) | 2 |
| Brieuil-sur-Chizé | 427 | 0 | 427 | 0 | **427** | 89 (21 %) | 6 |
| Vernoux-sur-Boutonne | 427 | 0 | 427 | 0 | **427** | 82 (19 %) | 19 |
| Épannes | 426 | 2 | 424 | 0 | **424** | 45 (11 %) | 3 |
| Lusseray | 423 | 2 | 421 | 0 | **421** | 70 (17 %) | 16 |
| Tourtenay | 418 | 1 | 417 | 0 | **417** | 126 (30 %) | 12 |
| La Chapelle-Pouilloux | 411 | 0 | 411 | 0 | **411** | 67 (16 %) | 8 |
| Chérigné | 408 | 0 | 408 | 0 | **408** | 67 (16 %) | 12 |
| Salles | 414 | 8 | 406 | 0 | **406** | 91 (22 %) | 2 |
| Trayes | 385 | 3 | 382 | 0 | **382** | 125 (33 %) | 3 |
| Vautebis | 380 | 1 | 379 | 0 | **379** | 94 (25 %) | 2 |
| Oroux | 350 | 2 | 348 | 0 | **348** | 65 (19 %) | 3 |
| Juscorps | 339 | 0 | 339 | 0 | **339** | 45 (13 %) | 36 |
| Saint-Jacques-de-Thouars | 300 | 3 | 297 | 0 | **297** | 9 (3 %) | 14 |
| Maisonnay | 274 | 0 | 274 | 0 | **274** | 43 (16 %) | 10 |
| Luché-sur-Brioux | 273 | 3 | 270 | 0 | **270** | 55 (20 %) | 1 |
| Saint-Maixent-l'École | 271 | 1 | 270 | 41 | **229** | 3 (1 %) | 6 |
| Le Chillou | 269 | 0 | 269 | 0 | **269** | 11 (4 %) | 14 |
| Saint-Jean-de-Thouars | 266 | 4 | 262 | 0 | **262** | 13 (5 %) | 7 |
| Juillé | 256 | 0 | 256 | 0 | **256** | 49 (19 %) | 12 |
| Les Groseillers | 242 | 0 | 242 | 0 | **242** | 82 (34 %) |  |
| Sciecq | 236 | 8 | 228 | 0 | **228** | 17 (7 %) | 3 |
| Saint-Romans-des-Champs | 217 | 0 | 217 | 0 | **217** | 26 (12 %) | 13 |
| Puihardy | 63 | 1 | 62 | 0 | **62** | 12 (19 %) |  |

## Parcs (7319)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Forêt domaniale de Chizé ⚠️ | Villiers-en-Bois › Mellois en Poitou | 1 824 |
| Forêt domaniale d'Aulnay ⚠️ | Aubigné › Mellois en Poitou | 978 |
| Forêt de Reffannes ⚠️ | Reffannes › Val de Gâtine | 484 |
| Forêt de Pressigny (6) ⚠️ | Pressigny › Parthenay-Gâtine | 458 |
| Forêt de Saint-Léger-de-Montbrun (42) ⚠️ | Saint-Léger-de-Montbrun › Thouarsais | 362 |
| Forêt de Beauvoir-sur-Niort (16) ⚠️ | Beauvoir-sur-Niort › Niortais | 344 |
| Forêt de Prailles-la-Couarde ⚠️ | Prailles-la-Couarde › Mellois en Poitou | 339 |
| Forêt de Plaine-et-Vallées (78) ⚠️ | Plaine-et-Vallées › Thouarsais | 305 |
| Le Bois Vernoux ⚠️ | L'Absie › Bocage Bressuirais | 272 |
| Forêt de Soudan (2) ⚠️ | Soudan › Haut Val de Sèvre | 265 |
| Forêt domaniale de Secondigny ⚠️ | Le Retail › Parthenay-Gâtine | 252 |
| Forêt de Thouars (64) ⚠️ | Thouars › Thouarsais | 245 |
| Forêt de Moncoutant-sur-Sèvre ⚠️ | Moncoutant-sur-Sèvre › Bocage Bressuirais | 237 |
| Forêt de Saint Maurice Étusson (14) ⚠️ | Saint Maurice Étusson › Bocage Bressuirais | 219 |
| Forêt de Sauzé-entre-Bois (88) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 212 |
| Bois d'Arpentérault ⚠️ | La Chapelle-Bâton › Val de Gâtine | 207 |
| Forêt de Thénezay (2) ⚠️ | Thénezay › Parthenay-Gâtine | 201 |
| Forêt de Couture-d'Argenson (20) ⚠️ | Couture-d'Argenson › Mellois en Poitou | 197 |
| Forêt de Beaulieu-sous-Parthenay ⚠️ | Beaulieu-sous-Parthenay › Val de Gâtine | 195 |
| Forêt de Sauzé-entre-Bois (90) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 184 |
| Forêt de Lezay (3) ⚠️ | Lezay › Mellois en Poitou | 174 |
| Forêt de Xaintray ⚠️ | Xaintray › Val de Gâtine | 165 |
| Bois de Saint-Loup ⚠️ | Assais-les-Jumeaux › Airvaudais-Val du Thouet | 159 |
| Forêt de Saint-Généroux (16) ⚠️ | Saint-Généroux › Thouarsais | 158 |
| Forêt de Aubigné ⚠️ | Aubigné › Mellois en Poitou | 157 |
| Forêt de Chizé ⚠️ | Chizé › Mellois en Poitou | 156 |
| Forêt de Saint-Varent (14) ⚠️ | Saint-Varent › Thouarsais | 155 |
| Forêt de Celles-sur-Belle (30) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 145 |
| Forêt de Boussais (2) ⚠️ | Boussais › Airvaudais-Val du Thouet | 141 |
| Forêt d'Autun ⚠️ | Thénezay › Parthenay-Gâtine | 139 |
| Forêt de Saint-Martin-du-Fouilloux (11) ⚠️ | Saint-Martin-du-Fouilloux › Parthenay-Gâtine | 136 |
| Forêt de Mauléon (25) ⚠️ | Mauléon › Bocage Bressuirais | 126 |
| Forêt de Amailloux (2) | Amailloux › Parthenay-Gâtine | 123 |
| Forêt de Fontivillié | Fontivillié › Mellois en Poitou | 121 |
| Forêt de Vasles (4) | Vasles › Parthenay-Gâtine | 120 |
| Bois de la Coudre | Les Châteliers › Parthenay-Gâtine | 114 |
| Forêt de Fenioux (15) | Fenioux › Val de Gâtine | 114 |
| Forêt de La Ferrière-en-Parthenay (19) | La Ferrière-en-Parthenay › Parthenay-Gâtine | 113 |
| Forêt de Rom (62) | Rom › Mellois en Poitou | 112 |
| Bois d'Ensigné | Ensigné › Mellois en Poitou | 110 |
| Forêt de Plaine-et-Vallées (3) | Plaine-et-Vallées › Thouarsais | 108 |
| Forêt des Fosses (7) | Les Fosses › Mellois en Poitou | 108 |
| Forêt de Fomperron (3) | Fomperron › Parthenay-Gâtine | 107 |
| Forêt de Plaine-et-Vallées (73) | Plaine-et-Vallées › Thouarsais | 107 |
| Forêt de Marigny (57) | Marigny › Niortais | 103 |
| Forêt de Saint Maurice Étusson | Saint Maurice Étusson › Bocage Bressuirais | 95 |
| Bois de Alloinay (2) | Alloinay › Mellois en Poitou | 95 |
| Forêt de Couture-d'Argenson (21) | Couture-d'Argenson › Mellois en Poitou | 92 |
| Forêt de Lezay (22) | Lezay › Mellois en Poitou | 91 |
| Forêt de Villiers-en-Bois | Villiers-en-Bois › Mellois en Poitou | 88 |
| Forêt de Sainte-Néomaye (26) | Sainte-Néomaye › Haut Val de Sèvre | 88 |
| Forêt de Chiché (4) | Chiché › Bocage Bressuirais | 85 |
| Bois d'Allone | Allonne › Parthenay-Gâtine | 83 |
| Forêt de Sauzé-entre-Bois (89) | Sauzé-entre-Bois › Mellois en Poitou | 82 |
| Forêt de Plaine-et-Vallées (72) | Plaine-et-Vallées › Thouarsais | 80 |
| Forêt de Loretz-d'Argenton (39) | Loretz-d'Argenton › Thouarsais | 80 |
| Forêt de Irais (11) | Irais › Airvaudais-Val du Thouet | 75 |
| Forêt de Saurais | Saurais › Parthenay-Gâtine | 74 |
| Forêt de Airvault (2) | Airvault › Airvaudais-Val du Thouet | 73 |
| Forêt de Sauzé-entre-Bois (4) | Sauzé-entre-Bois › Mellois en Poitou | 73 |
| Forêt de Sainte-Verge (4) | Sainte-Verge › Thouarsais | 73 |
| Forêt de La Foye-Monjault | La Foye-Monjault › Niortais | 71 |
| Forêt de Aubigné (2) | Aubigné › Mellois en Poitou | 71 |
| Forêt de Niort | Niort › Niortais | 68 |
| Forêt de Aubigny | Aubigny › Parthenay-Gâtine | 68 |
| Forêt de Vasles (10) | Vasles › Parthenay-Gâtine | 68 |
| Forêt de Paizay-le-Chapt (2) | Paizay-le-Chapt › Mellois en Poitou | 67 |
| Forêt de Loubillé | Loubillé › Mellois en Poitou | 65 |
| Forêt de Marnes | Marnes › Thouarsais | 64 |
| Forêt de Couture-d'Argenson (24) | Couture-d'Argenson › Mellois en Poitou | 64 |
| Forêt de La Chapelle-Saint-Laurent | La Chapelle-Saint-Laurent › Bocage Bressuirais | 63 |
| Forêt de Villemain (3) | Villemain › Mellois en Poitou | 62 |
| Forêt de Chiché (3) | Chiché › Bocage Bressuirais | 62 |
| Forêt de Marigny | Marigny › Niortais | 61 |
| Le Bois de Chasserat | Thouars › Thouarsais | 60 |
| Forêt de Fomperron (5) | Fomperron › Parthenay-Gâtine | 58 |
| Bois de Nery | Vausseroux › Parthenay-Gâtine | 57 |
| Forêt de Saint Maurice Étusson (3) | Saint Maurice Étusson › Bocage Bressuirais | 57 |
| Forêt de Rom (3) | Rom › Mellois en Poitou | 56 |
| Forêt de La Mothe-Saint-Héray (2) | La Mothe-Saint-Héray › Mellois en Poitou | 55 |
| Forêt de Maisontiers (3) | Maisontiers › Airvaudais-Val du Thouet | 55 |
| Forêt de Airvault (105) | Airvault › Airvaudais-Val du Thouet | 55 |
| Forêt de Saint-Pardoux-Soutiers (2) | Saint-Pardoux-Soutiers › Val de Gâtine | 54 |
| Le Bois du Theil | Saint-Aubin-le-Cloud › Parthenay-Gâtine | 54 |
| Les Bois Rocard | Boismé › Bocage Bressuirais | 54 |
| Forêt de Mauzé-sur-le-Mignon (2) | Mauzé-sur-le-Mignon › Niortais | 53 |
| Forêt de Exireuil (3) | Exireuil › Haut Val de Sèvre | 52 |
| Forêt de Moncoutant-sur-Sèvre (2) | Moncoutant-sur-Sèvre › Bocage Bressuirais | 52 |
| Forêt de La Chapelle-Pouilloux | La Chapelle-Pouilloux › Mellois en Poitou | 51 |
| Forêt de La Foye-Monjault (2) | La Foye-Monjault › Niortais | 50 |
| Forêt de Nanteuil (13) | Nanteuil › Haut Val de Sèvre | 50 |
| Forêt de Beaussais-Vitré (35) | Beaussais-Vitré › Mellois en Poitou | 50 |
| Forêt de Airvault (6) | Airvault › Airvaudais-Val du Thouet | 49 |
| Forêt de Melle (23) | Melle › Mellois en Poitou | 49 |
| Forêt de Marigny (51) | Marigny › Niortais | 49 |
| Forêt de Xaintray (2) | Xaintray › Val de Gâtine | 48 |
| Forêt de Val en Vignes (53) | Val en Vignes › Thouarsais | 48 |
| Forêt de Maisontiers (2) | Maisontiers › Airvaudais-Val du Thouet | 46 |
| Forêt de Assais-les-Jumeaux (31) | Assais-les-Jumeaux › Airvaudais-Val du Thouet | 46 |
| Forêt de Vasles (2) | Vasles › Parthenay-Gâtine | 45 |
| Forêt de Mairé-Levescault | Mairé-Levescault › Mellois en Poitou | 45 |
| Forêt de Melle | Melle › Mellois en Poitou | 44 |
| Forêt des Forges (2) | Les Forges › Parthenay-Gâtine | 44 |
| Forêt de Availles-Thouarsais (14) | Availles-Thouarsais › Airvaudais-Val du Thouet | 44 |
| Forêt de Chiché | Chiché › Bocage Bressuirais | 42 |
| Forêt de Augé | Augé › Haut Val de Sèvre | 42 |
| Forêt de Gourgé (3) | Gourgé › Parthenay-Gâtine | 42 |
| Forêt de Genneton (6) | Genneton › Bocage Bressuirais | 42 |
| Forêt de Alloinay | Alloinay › Mellois en Poitou | 41 |
| Forêt de Genneton | Genneton › Bocage Bressuirais | 41 |
| Forêt de Voulmentin | Voulmentin › Bocage Bressuirais | 41 |
| Forêt de Glénay (2) | Glénay › Thouarsais | 41 |
| Forêt de Airvault (4) | Airvault › Airvaudais-Val du Thouet | 41 |
| Forêt de Val-du-Mignon (2) | Val-du-Mignon › Niortais | 41 |
| Forêt de Beauvoir-sur-Niort (3) | Beauvoir-sur-Niort › Niortais | 41 |
| Forêt de Sciecq | Sciecq › Niortais | 40 |
| Bois de la Blandinière | Mauléon › Bocage Bressuirais | 40 |
| Forêt de Ensigné | Ensigné › Mellois en Poitou | 40 |
| Forêt de Germond-Rouvre | Germond-Rouvre › Niortais | 39 |
| Forêt de Neuvy-Bouin (2) | Neuvy-Bouin › Bocage Bressuirais | 39 |
| Forêt de Mauzé-sur-le-Mignon (3) | Mauzé-sur-le-Mignon › Niortais | 39 |
| Forêt de Lezay (21) | Lezay › Mellois en Poitou | 38 |
| Forêt de Availles-Thouarsais | Availles-Thouarsais › Airvaudais-Val du Thouet | 37 |
| Forêt de Loubillé (4) | Loubillé › Mellois en Poitou | 37 |
| Forêt de Saint-Généroux (15) | Saint-Généroux › Thouarsais | 37 |
| Forêt de Gourgé (2) | Gourgé › Parthenay-Gâtine | 36 |
| Forêt de Soudan | Soudan › Haut Val de Sèvre | 36 |
| Bois domanial de la Boucherie | Beugnon-Thireuil › Val de Gâtine | 36 |
| Bois des Mothes | La Chapelle-Saint-Laurent › Bocage Bressuirais | 35 |
| Forêt de Lhoumois (2) | Lhoumois › Parthenay-Gâtine | 35 |
| Forêt des Châteliers | Les Châteliers › Parthenay-Gâtine | 34 |
| Forêt de Lorigné (2) | Lorigné › Mellois en Poitou | 34 |
| Forêt de Boussais | Boussais › Airvaudais-Val du Thouet | 34 |
| Forêt de Arçais (29) | Arçais › Niortais | 34 |
| Forêt de Fomperron (4) | Fomperron › Parthenay-Gâtine | 33 |
| Forêt de Exireuil (2) | Exireuil › Haut Val de Sèvre | 32 |
| Forêt de Neuvy-Bouin | Neuvy-Bouin › Bocage Bressuirais | 32 |
| Forêt de Saint-Vincent-la-Châtre | Saint-Vincent-la-Châtre › Mellois en Poitou | 32 |
| Forêt de Villemain | Villemain › Mellois en Poitou | 32 |
| Forêt de Glénay | Glénay › Thouarsais | 32 |
| Bois de Puyrajoux | Chiché › Bocage Bressuirais | 32 |
| Forêt de Mauléon (5) | Mauléon › Bocage Bressuirais | 32 |
| Bois de Saint-Génard | Marcillé › Mellois en Poitou | 32 |
| Forêt de Airvault (102) | Assais-les-Jumeaux › Airvaudais-Val du Thouet | 32 |
| Forêt de La Mothe-Saint-Héray | La Mothe-Saint-Héray › Mellois en Poitou | 31 |
| Forêt de Thouars (4) | Thouars › Thouarsais | 31 |
| Forêt de Saint Maurice Étusson (4) | Saint Maurice Étusson › Bocage Bressuirais | 31 |
| Bois aux Chèvres | Nueil-les-Aubiers › Bocage Bressuirais | 31 |
| Bois de Bretignolles (31) | Bretignolles › Bocage Bressuirais | 31 |
| Forêt de Surin | Surin › Val de Gâtine | 30 |
| Forêt de Saivres | Saivres › Haut Val de Sèvre | 30 |
| Forêt de Germond-Rouvre (2) | Germond-Rouvre › Niortais | 30 |
| Forêt de Moncoutant-sur-Sèvre (3) | Moncoutant-sur-Sèvre › Bocage Bressuirais | 30 |
| Forêt de Thouars (6) | Thouars › Thouarsais | 30 |
| Forêt de Saint-Loup-Lamairé (61) | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 30 |
| Forêt de Sauzé-entre-Bois (2) | Sauzé-entre-Bois › Mellois en Poitou | 29 |
| Forêt de Vanzay | Vanzay › Mellois en Poitou | 29 |
| Forêt de Melleran | Melleran › Mellois en Poitou | 29 |
| Forêt de Lorigné | Lorigné › Mellois en Poitou | 29 |
| Forêt de Airvault (3) | Airvault › Airvaudais-Val du Thouet | 29 |
| Forêt du Busseau (2) | Le Busseau › Val de Gâtine | 29 |
| Forêt de Chey (2) | Chey › Mellois en Poitou | 29 |
| Forêt de Aubigné (6) | Aubigné › Mellois en Poitou | 29 |
| Forêt de Thouars | Thouars › Thouarsais | 28 |
| Forêt de Nueil-les-Aubiers | Nueil-les-Aubiers › Bocage Bressuirais | 28 |
| Forêt de Louin (2) | Louin › Airvaudais-Val du Thouet | 28 |
| Forêt de Saint-Martin-de-Saint-Maixent (2) | Saint-Martin-de-Saint-Maixent › Haut Val de Sèvre | 28 |
| Forêt de Frontenay-Rohan-Rohan (10) | Frontenay-Rohan-Rohan › Niortais | 28 |
| Forêt de Beugnon-Thireuil | Beugnon-Thireuil › Val de Gâtine | 27 |
| Forêt de Gourgé (4) | La Peyratte › Parthenay-Gâtine | 27 |
| Le Bruyereau | La Peyratte › Parthenay-Gâtine | 27 |
| Forêt de Beugnon-Thireuil (2) | Beugnon-Thireuil › Val de Gâtine | 27 |
| Forêt de Plaine-et-Vallées (6) | Plaine-et-Vallées › Thouarsais | 27 |
| Forêt de Loubillé (2) | Loubillé › Mellois en Poitou | 27 |
| Forêt de Sauzé-entre-Bois (7) | Sauzé-entre-Bois › Mellois en Poitou | 27 |
| Forêt de Rom (63) | Rom › Mellois en Poitou | 27 |
| Forêt de Vasles (9) | Vasles › Parthenay-Gâtine | 26 |
| Forêt de Champdeniers | Champdeniers › Val de Gâtine | 26 |
| Forêt de Val en Vignes (4) | Val en Vignes › Thouarsais | 26 |
| Forêt de Aubigny (2) | Aubigny › Parthenay-Gâtine | 26 |
| Forêt de Val-du-Mignon (4) | Val-du-Mignon › Niortais | 26 |
| Forêt de Soudan (5) | Soudan › Haut Val de Sèvre | 26 |
| Forêt de Arçais (26) | Arçais › Niortais | 26 |
| Bois de la Cassotte | Geay › Bocage Bressuirais | 26 |
| Forêt de Saint-Maixent-de-Beugné (5) | Saint-Maixent-de-Beugné › Val de Gâtine | 26 |
| Forêt de Beauvoir-sur-Niort (2) | Beauvoir-sur-Niort › Niortais | 25 |
| Forêt de Argentonnay | Argentonnay › Bocage Bressuirais | 25 |
| Forêt de Champdeniers (2) | Champdeniers › Val de Gâtine | 25 |
| Forêt de Exoudun (2) | Exoudun › Mellois en Poitou | 25 |
| Forêt de Chiché (2) | Chiché › Bocage Bressuirais | 25 |
| Forêt de La Forêt-sur-Sèvre | La Forêt-sur-Sèvre › Bocage Bressuirais | 25 |
| Forêt de Beugnon-Thireuil (5) | Beugnon-Thireuil › Val de Gâtine | 25 |
| Forêt de Saint-Martin-de-Mâcon (10) | Saint-Martin-de-Mâcon › Thouarsais | 25 |
| La Futaie de Saint-Jean | Saurais › Parthenay-Gâtine | 24 |
| Bois Beauchamp | Aubigny › Parthenay-Gâtine | 24 |
| Forêt de Val en Vignes (5) | Val en Vignes › Thouarsais | 24 |
| Forêt de Plaine-et-Vallées (5) | Plaine-et-Vallées › Thouarsais | 24 |
| Bois de Nueil-les-Aubiers (61) | Nueil-les-Aubiers › Bocage Bressuirais | 24 |
| Forêt de Assais-les-Jumeaux (44) | Assais-les-Jumeaux › Airvaudais-Val du Thouet | 24 |
| Forêt de Marnes (30) | Marnes › Thouarsais | 24 |
| Forêt de Plaine-et-Vallées | Plaine-et-Vallées › Thouarsais | 23 |
| Forêt de Fomperron | Fomperron › Parthenay-Gâtine | 23 |
| Forêt de Asnières-en-Poitou | Asnières-en-Poitou › Mellois en Poitou | 23 |
| Forêt de Airvault | Airvault › Airvaudais-Val du Thouet | 23 |
| Bois de Beauflux | Gourgé › Parthenay-Gâtine | 23 |
| Forêt de La Ferrière-en-Parthenay (3) | La Ferrière-en-Parthenay › Parthenay-Gâtine | 23 |
| Forêt de Pamplie (3) | Pamplie › Val de Gâtine | 23 |
| Forêt de Lezay (2) | Lezay › Mellois en Poitou | 23 |
| Forêt de Sauzé-entre-Bois (6) | Sauzé-entre-Bois › Mellois en Poitou | 23 |
| Forêt de Faye-l'Abbesse (2) | Faye-l'Abbesse › Bocage Bressuirais | 23 |
| Forêt de Cirières | Cirières › Bocage Bressuirais | 23 |
| Forêt de Valdelaume (63) | Valdelaume › Mellois en Poitou | 23 |
| Forêt de Sauzé-entre-Bois (93) | Sauzé-entre-Bois › Mellois en Poitou | 23 |
| Forêt de Maisontiers | Maisontiers › Airvaudais-Val du Thouet | 22 |
| Forêt de Mauzé-sur-le-Mignon | Mauzé-sur-le-Mignon › Niortais | 22 |
| Forêt de Paizay-le-Chapt | Paizay-le-Chapt › Mellois en Poitou | 22 |
| Forêt de Thouars (2) | Thouars › Thouarsais | 22 |
| Forêt de Clessé | Clessé › Bocage Bressuirais | 22 |
| Forêt de Thénezay | Thénezay › Parthenay-Gâtine | 22 |
| Forêt de Pamproux | Pamproux › Haut Val de Sèvre | 22 |
| Forêt de Aubigné (3) | Aubigné › Mellois en Poitou | 22 |
| Forêt de Saint-Martin-de-Mâcon | Saint-Martin-de-Mâcon › Thouarsais | 22 |
| Forêt de Saint-Loup-Lamairé (2) | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 22 |
| Forêt de Saint-Georges-de-Noisné (2) | Saint-Georges-de-Noisné › Val de Gâtine | 22 |
| Forêt de Augé (93) | Augé › Haut Val de Sèvre | 22 |
| Forêt de Saint-Hilaire-la-Palud (28) | Saint-Hilaire-la-Palud › Niortais | 22 |
| Forêt de Arçais | Arçais › Niortais | 22 |
| Forêt de Plaine-et-Vallées (68) | Plaine-et-Vallées › Thouarsais | 22 |
| Forêt de Germond-Rouvre (8) | Germond-Rouvre › Niortais | 22 |
| Forêt de Louzy (15) | Brion-près-Thouet › Thouarsais | 22 |
| Forêt de Pas-de-Jeu (16) | Pas-de-Jeu › Thouarsais | 22 |
| Forêt de Thouars (66) | Thouars › Thouarsais | 22 |
| Forêt de Clussais-la-Pommeraie | Clussais-la-Pommeraie › Mellois en Poitou | 21 |
| Forêt de Fomperron (2) | Fomperron › Parthenay-Gâtine | 21 |
| Forêt de Vernoux-en-Gâtine (3) | Vernoux-en-Gâtine › Parthenay-Gâtine | 21 |
| Forêt de Vasles (12) | Vasles › Parthenay-Gâtine | 21 |
| Forêt de Cherveux (3) | Cherveux › Haut Val de Sèvre | 21 |
| Forêt de Brion-près-Thouet (6) | Brion-près-Thouet › Thouarsais | 21 |
| Forêt de Saint Maurice Étusson (15) | Saint Maurice Étusson › Bocage Bressuirais | 21 |
| Forêt de Mauléon (26) | Mauléon › Bocage Bressuirais | 21 |
| Forêt de Sauzé-entre-Bois (94) | Sauzé-entre-Bois › Mellois en Poitou | 21 |
| Forêt de Pamplie | Pamplie › Val de Gâtine | 20 |
| Forêt de Saint-Maixent-de-Beugné (2) | Saint-Maixent-de-Beugné › Val de Gâtine | 20 |
| Forêt de Glénay (3) | Glénay › Thouarsais | 20 |
| Forêt de Pamproux (2) | Pamproux › Haut Val de Sèvre | 20 |
| Forêt de Mairé-Levescault (4) | Mairé-Levescault › Mellois en Poitou | 20 |
| Forêt de Alloinay (12) | Alloinay › Mellois en Poitou | 20 |
| Forêt de Lusseray | Lusseray › Mellois en Poitou | 20 |
| Forêt de Thénezay (59) | Thénezay › Parthenay-Gâtine | 20 |
| Forêt de Arçais (30) | Arçais › Niortais | 20 |
| Forêt de Saurais (10) | Saurais › Parthenay-Gâtine | 20 |
| Forêt de Exireuil | Exireuil › Haut Val de Sèvre | 19 |
| Forêt de Brioux-sur-Boutonne | Brioux-sur-Boutonne › Mellois en Poitou | 19 |
| Forêt de Thouars (3) | Thouars › Thouarsais | 19 |
| Forêt de Pamplie (4) | Pamplie › Val de Gâtine | 19 |
| Forêt de Saint-Georges-de-Rex | Saint-Georges-de-Rex › Niortais | 19 |
| Forêt de Limalonges (4) | Limalonges › Mellois en Poitou | 19 |
| Forêt de Thénezay (15) | Thénezay › Parthenay-Gâtine | 19 |
| Forêt de La Ferrière-en-Parthenay (11) | La Ferrière-en-Parthenay › Parthenay-Gâtine | 19 |
| Forêt de Vasles (23) | Vasles › Parthenay-Gâtine | 19 |
| Forêt de Saint-Maixent-de-Beugné (4) | Saint-Maixent-de-Beugné › Val de Gâtine | 19 |
| Forêt de Saint-Pompain (5) | Saint-Pompain › Val de Gâtine | 19 |
| Forêt de Vausseroux | Vausseroux › Parthenay-Gâtine | 18 |
| Forêt de Ménigoute | Ménigoute › Parthenay-Gâtine | 18 |
| Forêt de Loretz-d'Argenton (2) | Loretz-d'Argenton › Thouarsais | 18 |
| Bois à Joseph | Le Pin › Bocage Bressuirais | 18 |
| Forêt de Vallans | Vallans › Niortais | 18 |
| Forêt de Val-du-Mignon | Val-du-Mignon › Niortais | 18 |
| Forêt de Tourtenay (2) | Tourtenay › Thouarsais | 18 |
| Forêt de Boismé | Boismé › Bocage Bressuirais | 18 |
| Bois de Niort (47) | Niort › Niortais | 18 |
| Forêt de Saint-Maixent-de-Beugné | Saint-Maixent-de-Beugné › Val de Gâtine | 17 |
| Forêt de Saint-Maixent-de-Beugné (3) | Saint-Maixent-de-Beugné › Val de Gâtine | 17 |
| Forêt de Montravers | Montravers › Bocage Bressuirais | 17 |
| Forêt de Parthenay | Parthenay › Parthenay-Gâtine | 17 |
| Forêt de Lorigné (3) | Lorigné › Mellois en Poitou | 17 |
| Forêt de Saint-Martin-de-Sanzay | Saint-Martin-de-Sanzay › Thouarsais | 17 |
| Forêt de Sansais (21) | Sansais › Niortais | 17 |
| Forêt de Marcillé (18) | Marcillé › Mellois en Poitou | 17 |
| Forêt de Niort (122) | Niort › Niortais | 17 |
| Forêt de Saint-Martin-du-Fouilloux (12) | Saint-Martin-du-Fouilloux › Parthenay-Gâtine | 17 |
| Forêt de La Peyratte | La Peyratte › Parthenay-Gâtine | 16 |
| Forêt de La Ferrière-en-Parthenay (2) | La Ferrière-en-Parthenay › Parthenay-Gâtine | 16 |
| Forêt de Vasles | Vasles › Parthenay-Gâtine | 16 |
| Forêt de Sainte-Soline | Sainte-Soline › Mellois en Poitou | 16 |
| Forêt de Mairé-Levescault (2) | Mairé-Levescault › Mellois en Poitou | 16 |
| Forêt de Limalonges | Limalonges › Mellois en Poitou | 16 |
| Forêt de Loretz-d'Argenton (4) | Loretz-d'Argenton › Thouarsais | 16 |
| Forêt de Saint-Léger-de-Montbrun | Saint-Léger-de-Montbrun › Thouarsais | 16 |
| Forêt de Amailloux | Amailloux › Parthenay-Gâtine | 16 |
| Forêt de Argentonnay (3) | Argentonnay › Bocage Bressuirais | 16 |
| Forêt de Viennay | Viennay › Parthenay-Gâtine | 16 |
| Forêt de Vernoux-en-Gâtine (4) | Vernoux-en-Gâtine › Parthenay-Gâtine | 16 |
| Bois de Saint-Martin-du-Fouilloux | Saint-Martin-du-Fouilloux › Parthenay-Gâtine | 16 |
| Forêt de Argentonnay (5) | Argentonnay › Bocage Bressuirais | 16 |
| Forêt de Thouars (7) | Thouars › Thouarsais | 16 |
| Forêt des Fosses (2) | Les Fosses › Mellois en Poitou | 16 |
| Forêt de Villiers-en-Bois (2) | Villiers-en-Bois › Mellois en Poitou | 16 |
| Forêt de Niort (121) | Niort › Niortais | 16 |
| Forêt de Saurais (8) | Saurais › Parthenay-Gâtine | 16 |
| Forêt de Combrand | Combrand › Bocage Bressuirais | 15 |
| Forêt de Vasles (11) | Vasles › Parthenay-Gâtine | 15 |
| Forêt de Cherveux (2) | Cherveux › Haut Val de Sèvre | 15 |
| Forêt de Prin-Deyrançon | Prin-Deyrançon › Niortais | 15 |
| Forêt de Saint-Coutant | Saint-Coutant › Mellois en Poitou | 15 |
| Forêt de Clussais-la-Pommeraie (3) | Clussais-la-Pommeraie › Mellois en Poitou | 15 |
| Forêt de Asnières-en-Poitou (3) | Asnières-en-Poitou › Mellois en Poitou | 15 |
| Forêt de Argentonnay (4) | Argentonnay › Bocage Bressuirais | 15 |
| Forêt de Argentonnay (6) | Argentonnay › Bocage Bressuirais | 15 |
| Forêt de La Petite-Boissière | La Petite-Boissière › Bocage Bressuirais | 15 |
| Forêt de Airvault (5) | Airvault › Airvaudais-Val du Thouet | 15 |
| Forêt de Louin | Louin › Airvaudais-Val du Thouet | 15 |
| Forêt de Bressuire (7) | Bressuire › Bocage Bressuirais | 15 |
| Forêt de Pierrefitte (3) | Pierrefitte › Thouarsais | 15 |
| Forêt de Magné (14) | Frontenay-Rohan-Rohan › Niortais | 15 |
| Forêt de Coulonges-sur-l'Autize | Coulonges-sur-l'Autize › Val de Gâtine | 15 |
| Forêt de Lezay (17) | Lezay › Mellois en Poitou | 15 |
| Forêt de Thouars (26) | Thouars › Thouarsais | 15 |
| Forêt de Couture-d'Argenson (23) | Couture-d'Argenson › Mellois en Poitou | 15 |
| Forêt de Saint-Cyr-la-Lande (7) | Saint-Cyr-la-Lande › Thouarsais | 15 |
| Forêt du Busseau (13) | Le Busseau › Val de Gâtine | 15 |
| Forêt de Beaulieu-sous-Parthenay (2) | Beaulieu-sous-Parthenay › Val de Gâtine | 14 |
| Forêt de Exoudun | Exoudun › Mellois en Poitou | 14 |
| Forêt de Mauléon (2) | Mauléon › Bocage Bressuirais | 14 |
| Forêt de Vasles (5) | Vasles › Parthenay-Gâtine | 14 |
| Forêt de Bessines | Bessines › Niortais | 14 |
| Forêt de Azay-le-Brûlé | Azay-le-Brûlé › Haut Val de Sèvre | 14 |
| Forêt de Azay-le-Brûlé (2) | Azay-le-Brûlé › Haut Val de Sèvre | 14 |
| Forêt de Mauléon (4) | Mauléon › Bocage Bressuirais | 14 |
| Forêt de Faye-l'Abbesse | Faye-l'Abbesse › Bocage Bressuirais | 14 |
| Forêt de Maisontiers (4) | Maisontiers › Airvaudais-Val du Thouet | 14 |
| Forêt de La Forêt-sur-Sèvre (2) | La Forêt-sur-Sèvre › Bocage Bressuirais | 14 |
| Forêt de Niort (9) | Niort › Niortais | 14 |
| Forêt de Niort (11) | Niort › Niortais | 14 |
| Forêt de Sansais (2) | Sansais › Niortais | 14 |
| Forêt de Prailles-la-Couarde (2) | Prailles-la-Couarde › Mellois en Poitou | 14 |
| Forêt de Sepvret (10) | Sepvret › Mellois en Poitou | 14 |
| Forêt de Couture-d'Argenson (5) | Couture-d'Argenson › Mellois en Poitou | 14 |
| Forêt de Pamplie (9) | Pamplie › Val de Gâtine | 14 |
| Forêt de Argentonnay (33) | Argentonnay › Bocage Bressuirais | 14 |
| Bois de Val en Vignes (90) | Val en Vignes › Thouarsais | 14 |
| Forêt de Plaine-d'Argenson (35) | Plaine-d'Argenson › Niortais | 14 |
| Forêt de La Ferrière-en-Parthenay | La Ferrière-en-Parthenay › Parthenay-Gâtine | 13 |
| Forêt de Pamplie (2) | Pamplie › Val de Gâtine | 13 |
| Forêt de Verruyes | Verruyes › Val de Gâtine | 13 |
| Forêt de Cherveux | Cherveux › Haut Val de Sèvre | 13 |
| Forêt de Melle (2) | Melle › Mellois en Poitou | 13 |
| Forêt de Beauvoir-sur-Niort | Beauvoir-sur-Niort › Niortais | 13 |
| Forêt de Mairé-Levescault (3) | Mairé-Levescault › Mellois en Poitou | 13 |
| Forêt de Luzay | Luzay › Thouarsais | 13 |
| Forêt de Loretz-d'Argenton (3) | Loretz-d'Argenton › Thouarsais | 13 |
| Forêt de Vasles (6) | Vasles › Parthenay-Gâtine | 13 |
| Forêt de Neuvy-Bouin (3) | Neuvy-Bouin › Bocage Bressuirais | 13 |
| Forêt de La Crèche (2) | La Crèche › Haut Val de Sèvre | 13 |
| Forêt de François | François › Haut Val de Sèvre | 13 |
| Forêt de Rom (4) | Rom › Mellois en Poitou | 13 |
| Forêt de La Rochénard | La Rochénard › Niortais | 13 |
| Forêt de Saint-Vincent-la-Châtre (2) | Saint-Vincent-la-Châtre › Mellois en Poitou | 13 |
| Forêt de Saint Maurice Étusson (2) | Saint Maurice Étusson › Bocage Bressuirais | 13 |
| Forêt du Pin | Le Pin › Bocage Bressuirais | 13 |
| Forêt de Val-du-Mignon (5) | Val-du-Mignon › Niortais | 13 |
| Forêt de Vernoux-en-Gâtine (5) | Vernoux-en-Gâtine › Parthenay-Gâtine | 13 |
| Forêt de Airvault (48) | Airvault › Airvaudais-Val du Thouet | 13 |
| Forêt de Vouhé | Vouhé › Val de Gâtine | 13 |
| Forêt de Saint-Hilaire-la-Palud (36) | Saint-Hilaire-la-Palud › Niortais | 13 |
| Forêt de Aigondigné (10) | Aigondigné › Mellois en Poitou | 13 |
| Forêt de Brion-près-Thouet (2) | Saint-Martin-de-Sanzay › Thouarsais | 13 |
| Forêt de Thouars (50) | Thouars › Thouarsais | 13 |
| Forêt de Thouars (65) | Thouars › Thouarsais | 13 |
| Forêt de Gourgé | Gourgé › Parthenay-Gâtine | 12 |
| Forêt de Vernoux-en-Gâtine (2) | Vernoux-en-Gâtine › Parthenay-Gâtine | 12 |
| Forêt de Scillé | Scillé › Val de Gâtine | 12 |
| Forêt de Azay-sur-Thouet | Azay-sur-Thouet › Parthenay-Gâtine | 12 |
| Forêt de Lezay | Lezay › Mellois en Poitou | 12 |
| Forêt de Clussais-la-Pommeraie (2) | Clussais-la-Pommeraie › Mellois en Poitou | 12 |
| Forêt de Chizé (2) | Chizé › Mellois en Poitou | 12 |
| Forêt de Val en Vignes (2) | Val en Vignes › Thouarsais | 12 |
| Forêt de Val en Vignes (3) | Val en Vignes › Thouarsais | 12 |
| Forêt du Chillou | Le Chillou › Airvaudais-Val du Thouet | 12 |
| Forêt de Saint-Loup-Lamairé | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 12 |
| Forêt des Fosses | Les Fosses › Mellois en Poitou | 12 |
| Bois des Éssupes | Vasles › Parthenay-Gâtine | 12 |
| Forêt de Fénery | Fénery › Parthenay-Gâtine | 12 |
| Forêt de Thénezay (3) | Thénezay › Parthenay-Gâtine | 12 |
| Forêt de La Ferrière-en-Parthenay (4) | La Ferrière-en-Parthenay › Parthenay-Gâtine | 12 |
| Forêt de Bressuire (2) | Bressuire › Bocage Bressuirais | 12 |
| Forêt de La Peyratte (5) | La Peyratte › Parthenay-Gâtine | 12 |
| Forêt de Magné (13) | Magné › Niortais | 12 |
| Forêt de Magné (29) | Magné › Niortais | 12 |
| Forêt de Aigondigné (5) | Aigondigné › Mellois en Poitou | 12 |
| Forêt de Saint-Jacques-de-Thouars | Saint-Jacques-de-Thouars › Thouarsais | 12 |
| Forêt de Sainte-Eanne (40) | Sainte-Eanne › Haut Val de Sèvre | 12 |
| Forêt de Nanteuil (11) | Nanteuil › Haut Val de Sèvre | 12 |
| Bois de Plaine-et-Vallées (11) | Plaine-et-Vallées › Thouarsais | 12 |
| Bois de Montravers | Saint-Amand-sur-Sèvre › Bocage Bressuirais | 12 |
| Bois de Bressuire (125) | Bressuire › Bocage Bressuirais | 12 |
| Bois Bréchoux | Villiers-sur-Chizé › Mellois en Poitou | 12 |
| Forêt du Vanneau-Irleau (22) | Le Vanneau-Irleau › Niortais | 12 |
| Forêt de Saint-Hilaire-la-Palud (44) | Saint-Hilaire-la-Palud › Niortais | 12 |
| Forêt de Sainte-Ouenne (13) | Sainte-Ouenne › Val de Gâtine | 12 |
| Forêt de Messé (5) | Sainte-Soline › Mellois en Poitou | 12 |
| Forêt de Argentonnay (35) | Argentonnay › Bocage Bressuirais | 12 |
| Forêt de Marigny (58) | Marigny › Niortais | 12 |
| Forêt de Beauvoir-sur-Niort (27) | Beauvoir-sur-Niort › Niortais | 12 |
| yyyy | Saint-Martin-du-Fouilloux › Parthenay-Gâtine | 12 |
| Forêt de Saint-Pardoux-Soutiers | Saint-Pardoux-Soutiers › Val de Gâtine | 11 |
| Forêt de Vasles (3) | Vasles › Parthenay-Gâtine | 11 |
| Forêt de Échiré | Échiré › Niortais | 11 |
| Forêt de Souvigné | Souvigné › Haut Val de Sèvre | 11 |
| Forêt de Melle (3) | Melle › Mellois en Poitou | 11 |
| Forêt de Marcillé | Marcillé › Mellois en Poitou | 11 |
| Forêt de Lhoumois | Lhoumois › Parthenay-Gâtine | 11 |
| Forêt de Châtillon-sur-Thouet | Châtillon-sur-Thouet › Parthenay-Gâtine | 11 |
| Forêt de Vasles (8) | Vasles › Parthenay-Gâtine | 11 |
| Forêt de Saint-Marc-la-Lande | Saint-Marc-la-Lande › Val de Gâtine | 11 |
| Forêt de Argentonnay (7) | Argentonnay › Bocage Bressuirais | 11 |
| Forêt de Asnières-en-Poitou (5) | Asnières-en-Poitou › Mellois en Poitou | 11 |
| Forêt de Verruyes (2) | Verruyes › Val de Gâtine | 11 |
| Forêt des Forges (5) | Les Forges › Parthenay-Gâtine | 11 |
| Forêt de Souvigné (4) | Souvigné › Haut Val de Sèvre | 11 |
| Forêt de Fenioux (6) | Fenioux › Val de Gâtine | 11 |
| Forêt de Sansais (23) | Sansais › Niortais | 11 |
| Forêt de Prailles-la-Couarde (33) | Prailles-la-Couarde › Mellois en Poitou | 11 |
| Forêt de Beugnon-Thireuil (8) | Fenioux › Val de Gâtine | 11 |
| Forêt de Ménigoute (4) | Ménigoute › Parthenay-Gâtine | 11 |
| Forêt de Pamproux (15) | Pamproux › Haut Val de Sèvre | 11 |
| Forêt de Saint-Généroux (6) | Saint-Généroux › Thouarsais | 11 |
| Forêt de Plaine-et-Vallées (48) | Plaine-et-Vallées › Thouarsais | 11 |
| Forêt de Saint-Martin-du-Fouilloux (3) | Saint-Martin-du-Fouilloux › Parthenay-Gâtine | 11 |
| Forêt de Vouhé (2) | Vouhé › Val de Gâtine | 11 |
| Bois de Saint-Martin-de-Sanzay | Saint-Martin-de-Sanzay › Thouarsais | 11 |
| Forêt de Germond-Rouvre (5) | Germond-Rouvre › Niortais | 11 |
| Bois de Saint-Jacques-de-Thouars (3) | Saint-Jacques-de-Thouars › Thouarsais | 11 |
| Forêt de Saint-Généroux (13) | Saint-Généroux › Thouarsais | 11 |
| Forêt de Loretz-d'Argenton (27) | Loretz-d'Argenton › Thouarsais | 11 |
| Forêt de Nueil-les-Aubiers (7) | Nueil-les-Aubiers › Bocage Bressuirais | 11 |
| Forêt de Argentonnay (36) | Argentonnay › Bocage Bressuirais | 11 |
| Forêt de Sepvret | Sepvret › Mellois en Poitou | 10 |
| Forêt de Plaine-d'Argenson | Plaine-d'Argenson › Niortais | 10 |
| Forêt de Mauléon (3) | Mauléon › Bocage Bressuirais | 10 |
| Forêt du Chillou (2) | Le Chillou › Airvaudais-Val du Thouet | 10 |
| Forêt de Vasles (7) | Vasles › Parthenay-Gâtine | 10 |
| Forêt de Vasles (13) | Vasles › Parthenay-Gâtine | 10 |
| Forêt de La Crèche | La Crèche › Haut Val de Sèvre | 10 |
| Forêt de Valdelaume | Valdelaume › Mellois en Poitou | 10 |
| Forêt de Asnières-en-Poitou (2) | Asnières-en-Poitou › Mellois en Poitou | 10 |
| Forêt de Faye-sur-Ardin | Faye-sur-Ardin › Val de Gâtine | 10 |
| Forêt de Thénezay (14) | Thénezay › Parthenay-Gâtine | 10 |
| Forêt de Secondigny (3) | Secondigny › Parthenay-Gâtine | 10 |
| Forêt de Argentonnay (19) | Argentonnay › Bocage Bressuirais | 10 |
| Forêt de Magné (12) | Magné › Niortais | 10 |
| Forêt de Saint-Martin-de-Saint-Maixent (18) | Saint-Martin-de-Saint-Maixent › Haut Val de Sèvre | 10 |
| Forêt de Romans (11) | Romans › Haut Val de Sèvre | 10 |
| Forêt de Clussais-la-Pommeraie (10) | Clussais-la-Pommeraie › Mellois en Poitou | 10 |
| Forêt de Couture-d'Argenson (10) | Couture-d'Argenson › Mellois en Poitou | 10 |
| Forêt de Valdelaume (33) | Valdelaume › Mellois en Poitou | 10 |
| Forêt de Thénezay (46) | Thénezay › Parthenay-Gâtine | 10 |
| Forêt de Brion-près-Thouet | Brion-près-Thouet › Thouarsais | 10 |
| Forêt de Val en Vignes (34) | Val en Vignes › Thouarsais | 10 |
| Forêt de Saint Maurice Étusson (10) | Saint Maurice Étusson › Bocage Bressuirais | 10 |
| Forêt de Mauléon (22) | Mauléon › Bocage Bressuirais | 10 |
| Forêt de Secondigné-sur-Belle (32) | Secondigné-sur-Belle › Mellois en Poitou | 10 |
| Bois de Beau Lieu | Aiffres › Niortais | 10 |
| Forêt de Saint-Martin-de-Saint-Maixent ⚠️ | Saint-Martin-de-Saint-Maixent › Haut Val de Sèvre | 9 |
| Bois de l'Epinay ⚠️ | Vasles › Parthenay-Gâtine | 9 |
| Forêt de Plaine-et-Vallées (2) ⚠️ | Plaine-et-Vallées › Thouarsais | 9 |
| Forêt de Bressuire ⚠️ | Bressuire › Bocage Bressuirais | 9 |
| Forêt de Chey ⚠️ | Chey › Mellois en Poitou | 9 |
| Bois de la Fortune ⚠️ | Juillé › Mellois en Poitou | 9 |
| Forêt de Luzay (15) ⚠️ | Luzay › Thouarsais | 9 |
| Forêt de Fontivillié (5) ⚠️ | Fontivillié › Mellois en Poitou | 9 |
| Forêt de Airvault (27) ⚠️ | Airvault › Airvaudais-Val du Thouet | 9 |
| Forêt de Fressines ⚠️ | Fressines › Mellois en Poitou | 9 |
| Forêt de Limalonges (14) ⚠️ | Limalonges › Mellois en Poitou | 9 |
| Forêt de Val en Vignes (14) ⚠️ | Val en Vignes › Thouarsais | 9 |
| Bois de Bressuire (127) ⚠️ | Bressuire › Bocage Bressuirais | 9 |
| Bois de Chey ⚠️ | Chey › Mellois en Poitou | 9 |
| Forêt de Arçais (11) ⚠️ | Arçais › Niortais | 9 |
| Forêt de Gourgé (19) ⚠️ | Gourgé › Parthenay-Gâtine | 9 |
| Forêt du Chillou (9) ⚠️ | Le Chillou › Airvaudais-Val du Thouet | 9 |
| Forêt de Coulonges-sur-l'Autize (4) ⚠️ | Coulonges-sur-l'Autize › Val de Gâtine | 9 |
| Forêt de Germond-Rouvre (3) ⚠️ | Germond-Rouvre › Niortais | 9 |
| Bois de Montravers (2) ⚠️ | Montravers › Bocage Bressuirais | 9 |
| Bois de Availles-Thouarsais (4) ⚠️ | Availles-Thouarsais › Airvaudais-Val du Thouet | 9 |
| Bois de Nueil-les-Aubiers (46) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 9 |
| Forêt de Airvault (106) ⚠️ | Airvault › Airvaudais-Val du Thouet | 9 |
| Forêt du Vert (8) ⚠️ | Le Vert › Mellois en Poitou | 9 |
| Forêt de Airvault (107) ⚠️ | Airvault › Airvaudais-Val du Thouet | 9 |
| Forêt de Plaine-et-Vallées (74) ⚠️ | Plaine-et-Vallées › Thouarsais | 9 |
| Forêt de Loretz-d'Argenton (37) ⚠️ | Loretz-d'Argenton › Thouarsais | 9 |
| Bois de Saint-Pierre-des-Échaubrognes (40) ⚠️ | Saint-Pierre-des-Échaubrognes › Bocage Bressuirais | 9 |
| Forêt de Saint-Hilaire-la-Palud ⚠️ | Saint-Hilaire-la-Palud › Niortais | 8 |
| Forêt de Souvigné (2) ⚠️ | Souvigné › Haut Val de Sèvre | 8 |
| Forêt de Plaine-d'Argenson (2) ⚠️ | Plaine-d'Argenson › Niortais | 8 |
| Forêt de Thouars (5) ⚠️ | Thouars › Thouarsais | 8 |
| Forêt de Sainte-Gemme ⚠️ | Sainte-Gemme › Thouarsais | 8 |
| Forêt de Exoudun (3) ⚠️ | Exoudun › Mellois en Poitou | 8 |
| Forêt de Plaine-d'Argenson (3) ⚠️ | Plaine-d'Argenson › Niortais | 8 |
| Forêt de Villemain (4) ⚠️ | Villemain › Mellois en Poitou | 8 |
| Forêt de Augé (2) ⚠️ | Augé › Haut Val de Sèvre | 8 |
| Forêt de Mairé-Levescault (7) ⚠️ | Mairé-Levescault › Mellois en Poitou | 8 |
| Bois de Mauléon (2) ⚠️ | Mauléon › Bocage Bressuirais | 8 |
| Forêt de Viennay (2) ⚠️ | Viennay › Parthenay-Gâtine | 8 |
| Forêt de Pougne-Hérisson (2) ⚠️ | Pougne-Hérisson › Parthenay-Gâtine | 8 |
| Forêt de Neuvy-Bouin (4) ⚠️ | Neuvy-Bouin › Bocage Bressuirais | 8 |
| Forêt de Saint-Martin-du-Fouilloux ⚠️ | Saint-Martin-du-Fouilloux › Parthenay-Gâtine | 8 |
| Forêt de Amailloux (3) ⚠️ | Amailloux › Parthenay-Gâtine | 8 |
| Bois de Bressuire (13) ⚠️ | Bressuire › Bocage Bressuirais | 8 |
| Bois de Argentonnay (24) ⚠️ | Argentonnay › Bocage Bressuirais | 8 |
| Forêt de Saint Maurice Étusson (5) ⚠️ | Saint Maurice Étusson › Bocage Bressuirais | 8 |
| Forêt de Saint-Léger-de-Montbrun (15) ⚠️ | Saint-Léger-de-Montbrun › Thouarsais | 8 |
| Bois de Bressuire (45) ⚠️ | Bressuire › Bocage Bressuirais | 8 |
| Bois de Saint-Romans ⚠️ | Saint-Romans-lès-Melle › Mellois en Poitou | 8 |
| Bois de Bressuire (91) ⚠️ | Bressuire › Bocage Bressuirais | 8 |
| Forêt de Saint-Amand-sur-Sèvre (3) ⚠️ | Saint-Amand-sur-Sèvre › Bocage Bressuirais | 8 |
| Forêt de Prailles-la-Couarde (37) ⚠️ | Prailles-la-Couarde › Mellois en Poitou | 8 |
| Forêt de Exoudun (9) ⚠️ | Exoudun › Mellois en Poitou | 8 |
| Forêt de Augé (114) ⚠️ | Augé › Haut Val de Sèvre | 8 |
| Forêt de Lezay (11) ⚠️ | Lezay › Mellois en Poitou | 8 |
| Forêt de Pamproux (16) ⚠️ | Pamproux › Haut Val de Sèvre | 8 |
| Forêt de Airvault (53) ⚠️ | Airvault › Airvaudais-Val du Thouet | 8 |
| Bois de Cirières (7) ⚠️ | Cirières › Bocage Bressuirais | 8 |
| Bois de Faye-l'Abbesse (2) ⚠️ | Faye-l'Abbesse › Bocage Bressuirais | 8 |
| Forêt de Limalonges (37) ⚠️ | Limalonges › Mellois en Poitou | 8 |
| Forêt de Limalonges (49) ⚠️ | Limalonges › Mellois en Poitou | 8 |
| Forêt de Azay-le-Brûlé (13) ⚠️ | Azay-le-Brûlé › Haut Val de Sèvre | 8 |
| Forêt de Saivres (20) ⚠️ | Saivres › Haut Val de Sèvre | 8 |
| Forêt de Saint-Loup-Lamairé (43) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 8 |
| Forêt de Plaine-d'Argenson (27) ⚠️ | Plaine-d'Argenson › Niortais | 8 |
| Forêt de Saint-Martin-de-Sanzay (33) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 8 |
| Forêt de Loretz-d'Argenton (10) ⚠️ | Loretz-d'Argenton › Thouarsais | 8 |
| Forêt de Loretz-d'Argenton (15) ⚠️ | Loretz-d'Argenton › Thouarsais | 8 |
| Bois de Argentonnay (60) ⚠️ | Argentonnay › Bocage Bressuirais | 8 |
| Bois de Combrand (2) ⚠️ | Combrand › Bocage Bressuirais | 8 |
| Forêt de Nueil-les-Aubiers (11) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 8 |
| Forêt de Cerizay (22) ⚠️ | Cerizay › Bocage Bressuirais | 8 |
| Forêt de Clavé (2) ⚠️ | Clavé › Val de Gâtine | 8 |
| Bois de La Foye-Monjault ⚠️ | La Foye-Monjault › Niortais | 8 |
| Bois de Amailloux ⚠️ | Amailloux › Parthenay-Gâtine | 8 |
| Bois de Argentonnay (90) ⚠️ | Argentonnay › Bocage Bressuirais | 8 |
| Forêt de Fontivillié (21) ⚠️ | Fontivillié › Mellois en Poitou | 8 |
| Forêt de Aigondigné (24) ⚠️ | Aigondigné › Mellois en Poitou | 8 |
| Forêt de Saurais (7) ⚠️ | Saurais › Parthenay-Gâtine | 8 |
| Forêt de Nueil-les-Aubiers (12) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 8 |
| Bois de Bressuire (171) ⚠️ | Bressuire › Bocage Bressuirais | 8 |
| Bois de Mauléon (158) ⚠️ | Mauléon › Bocage Bressuirais | 8 |
| Forêt de Cours ⚠️ | Cours › Val de Gâtine | 7 |
| Forêt de Rom (2) ⚠️ | Rom › Mellois en Poitou | 7 |
| Forêt de Val-du-Mignon (3) ⚠️ | Val-du-Mignon › Niortais | 7 |
| Forêt de Asnières-en-Poitou (6) ⚠️ | Asnières-en-Poitou › Mellois en Poitou | 7 |
| Forêt de Valdelaume (4) ⚠️ | Valdelaume › Mellois en Poitou | 7 |
| Bois de Saint-Pardoux-Soutiers (3) ⚠️ | Saint-Pardoux-Soutiers › Val de Gâtine | 7 |
| Forêt de La Ferrière-en-Parthenay (6) ⚠️ | La Ferrière-en-Parthenay › Parthenay-Gâtine | 7 |
| Forêt de Airvault (17) ⚠️ | Airvault › Airvaudais-Val du Thouet | 7 |
| Forêt de La Peyratte (9) ⚠️ | La Peyratte › Parthenay-Gâtine | 7 |
| Bois de Argentonnay (6) ⚠️ | Argentonnay › Bocage Bressuirais | 7 |
| Forêt de Chizé (5) ⚠️ | Chizé › Mellois en Poitou | 7 |
| Forêt de Brieuil-sur-Chizé ⚠️ | Brieuil-sur-Chizé › Mellois en Poitou | 7 |
| Bois de l'Aiguillon ⚠️ | Saint-Gelais › Niortais | 7 |
| Forêt de Neuvy-Bouin (9) ⚠️ | Neuvy-Bouin › Bocage Bressuirais | 7 |
| Forêt de Marcillé (8) ⚠️ | Marcillé › Mellois en Poitou | 7 |
| Forêt de Marcillé (11) ⚠️ | Marcillé › Mellois en Poitou | 7 |
| Bois de Voulmentin (16) ⚠️ | Voulmentin › Bocage Bressuirais | 7 |
| Forêt de Boismé (2) ⚠️ | Chanteloup › Bocage Bressuirais | 7 |
| Forêt de Assais-les-Jumeaux ⚠️ | Assais-les-Jumeaux › Airvaudais-Val du Thouet | 7 |
| Forêt de Sepvret (18) ⚠️ | Sepvret › Mellois en Poitou | 7 |
| Forêt de La Mothe-Saint-Héray (3) ⚠️ | La Mothe-Saint-Héray › Mellois en Poitou | 7 |
| Forêt de Limalonges (7) ⚠️ | Limalonges › Mellois en Poitou | 7 |
| Forêt de Villefollet (5) ⚠️ | Villefollet › Mellois en Poitou | 7 |
| Forêt de Villemain (14) ⚠️ | Villemain › Mellois en Poitou | 7 |
| Forêt de Pamplie (8) ⚠️ | Pamplie › Val de Gâtine | 7 |
| Forêt de Beugnon-Thireuil (9) ⚠️ | Beugnon-Thireuil › Val de Gâtine | 7 |
| Forêt de Argentonnay (22) ⚠️ | Argentonnay › Bocage Bressuirais | 7 |
| Forêt de Saint-Loup-Lamairé (13) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 7 |
| Forêt de La Peyratte (19) ⚠️ | La Peyratte › Parthenay-Gâtine | 7 |
| Domaine de la Roche ⚠️ | Cerizay › Bocage Bressuirais | 7 |
| Forêt de Vausseroux (3) ⚠️ | Vausseroux › Parthenay-Gâtine | 7 |
| Forêt de Moncoutant-sur-Sèvre (10) ⚠️ | Moncoutant-sur-Sèvre › Bocage Bressuirais | 7 |
| Forêt du Vanneau-Irleau (26) ⚠️ | Le Vanneau-Irleau › Niortais | 7 |
| Forêt de Surin (5) ⚠️ | Surin › Val de Gâtine | 7 |
| Forêt de Surin (6) ⚠️ | Surin › Val de Gâtine | 7 |
| Forêt de Thouars (24) ⚠️ | Thouars › Thouarsais | 7 |
| Bois de Plaine-et-Vallées (17) ⚠️ | Plaine-et-Vallées › Thouarsais | 7 |
| Forêt de Luzay (23) ⚠️ | Luzay › Thouarsais | 7 |
| Forêt de Thouars (55) ⚠️ | Thouars › Thouarsais | 7 |
| Bois de Val en Vignes (30) ⚠️ | Val en Vignes › Thouarsais | 7 |
| Bois de Genneton (10) ⚠️ | Genneton › Bocage Bressuirais | 7 |
| Forêt de Argentonnay (32) ⚠️ | Argentonnay › Bocage Bressuirais | 7 |
| Bois de Trayes ⚠️ | Trayes › Bocage Bressuirais | 7 |
| Forêt de Niort (128) ⚠️ | Niort › Niortais | 7 |
| Forêt de Plaine-et-Vallées (77) ⚠️ | Plaine-et-Vallées › Thouarsais | 7 |
| Forêt de Marigny (75) ⚠️ | Marigny › Niortais | 7 |
| Forêt de Brûlain (9) ⚠️ | Brûlain › Niortais | 7 |
| Bois de Voulmentin (34) ⚠️ | Voulmentin › Bocage Bressuirais | 7 |
| Bois du Pin (34) ⚠️ | Le Pin › Bocage Bressuirais | 7 |
| Bois de Saint-Cyr-la-Lande ⚠️ | Saint-Cyr-la-Lande › Thouarsais | 6 |
| Forêt de Sauzé-entre-Bois ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 6 |
| Forêt de Chizé (3) ⚠️ | Chizé › Mellois en Poitou | 6 |
| Base de Loisirs ⚠️ | Parthenay › Parthenay-Gâtine | 6 |
| Forêt de Valdelaume (3) ⚠️ | Valdelaume › Mellois en Poitou | 6 |
| Forêt de Rom (5) ⚠️ | Rom › Mellois en Poitou | 6 |
| Bois du Tallud (2) ⚠️ | Le Tallud › Parthenay-Gâtine | 6 |
| Bois de Allonne (2) ⚠️ | Allonne › Parthenay-Gâtine | 6 |
| Forêt de Saint-Georges-de-Noisné ⚠️ | Saint-Georges-de-Noisné › Val de Gâtine | 6 |
| Forêt de Mazières-en-Gâtine ⚠️ | Mazières-en-Gâtine › Val de Gâtine | 6 |
| Bois de l'Aumônerie ⚠️ | Secondigny › Parthenay-Gâtine | 6 |
| Bois de Mauléon ⚠️ | Mauléon › Bocage Bressuirais | 6 |
| Bois de Nueil-les-Aubiers (23) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 6 |
| Bois de Saint-Aubin-le-Cloud ⚠️ | Saint-Aubin-le-Cloud › Parthenay-Gâtine | 6 |
| Forêt de Thouars (8) ⚠️ | Thouars › Thouarsais | 6 |
| Forêt de La Peyratte (11) ⚠️ | La Peyratte › Parthenay-Gâtine | 6 |
| Le Bois Bergeronneau ⚠️ | Fontivillié › Mellois en Poitou | 6 |
| Forêt de Gourgé (5) ⚠️ | Gourgé › Parthenay-Gâtine | 6 |
| Le Bois Moreau ⚠️ | Moncoutant-sur-Sèvre › Bocage Bressuirais | 6 |
| Bois de Argentonnay (22) ⚠️ | Argentonnay › Bocage Bressuirais | 6 |
| Forêt de Luché-Thouarsais ⚠️ | Luché-Thouarsais › Thouarsais | 6 |
| Forêt de Marnes (8) ⚠️ | Marnes › Thouarsais | 6 |
| Forêt de Trayes ⚠️ | Trayes › Bocage Bressuirais | 6 |
| Forêt de Melle (65) ⚠️ | Melle › Mellois en Poitou | 6 |
| Forêt de Melle (67) ⚠️ | Melle › Mellois en Poitou | 6 |
| Forêt de Souvigné (18) ⚠️ | Souvigné › Haut Val de Sèvre | 6 |
| Bois de Oroux ⚠️ | Oroux › Parthenay-Gâtine | 6 |
| Base de loisirs Les Adillons ⚠️ | Luché-Thouarsais › Thouarsais | 6 |
| Forêt de Melleran (21) ⚠️ | Melleran › Mellois en Poitou | 6 |
| Forêt de Villemain (8) ⚠️ | Villemain › Mellois en Poitou | 6 |
| Forêt de Saint-Coutant (19) ⚠️ | Saint-Coutant › Mellois en Poitou | 6 |
| Forêt de Saint-Martin-de-Sanzay (4) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 6 |
| Forêt de Saint-Loup-Lamairé (5) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 6 |
| Forêt de Pressigny (5) ⚠️ | Pressigny › Parthenay-Gâtine | 6 |
| Forêt de Saint-Généroux (8) ⚠️ | Saint-Généroux › Thouarsais | 6 |
| Forêt de Limalonges (58) ⚠️ | Limalonges › Mellois en Poitou | 6 |
| Forêt de Mauléon (17) ⚠️ | Mauléon › Bocage Bressuirais | 6 |
| Forêt de Saint-Léger-de-Montbrun (30) ⚠️ | Saint-Léger-de-Montbrun › Thouarsais | 6 |
| Bois de Nueil-les-Aubiers (37) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 6 |
| Forêt de Saint-Hilaire-la-Palud (46) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 6 |
| Bois des Loges ⚠️ | Val-du-Mignon › Niortais | 6 |
| Forêt du Vert (7) ⚠️ | Le Vert › Mellois en Poitou | 6 |
| Forêt de Sainte-Ouenne (3) ⚠️ | Germond-Rouvre › Niortais | 6 |
| Forêt de Ardin (7) ⚠️ | Ardin › Val de Gâtine | 6 |
| Forêt de Saint-Maxire ⚠️ | Saint-Maxire › Niortais | 6 |
| Bois de Galardon ⚠️ | Vernoux-sur-Boutonne › Mellois en Poitou | 6 |
| Forêt de Saint-Généroux (12) ⚠️ | Saint-Généroux › Thouarsais | 6 |
| Forêt de Plaine-et-Vallées (69) ⚠️ | Plaine-et-Vallées › Thouarsais | 6 |
| Forêt de Argentonnay (28) ⚠️ | Argentonnay › Bocage Bressuirais | 6 |
| Bois de Val en Vignes (58) ⚠️ | Val en Vignes › Thouarsais | 6 |
| Forêt de Val en Vignes (50) ⚠️ | Val en Vignes › Thouarsais | 6 |
| Bois de Saint Maurice Étusson (8) ⚠️ | Saint Maurice Étusson › Bocage Bressuirais | 6 |
| Forêt de Argentonnay (31) ⚠️ | Argentonnay › Bocage Bressuirais | 6 |
| Forêt de Voulmentin (3) ⚠️ | Voulmentin › Bocage Bressuirais | 6 |
| Domaine de Soulièvres ⚠️ | Airvault › Airvaudais-Val du Thouet | 6 |
| Forêt de Mauléon (19) ⚠️ | Mauléon › Bocage Bressuirais | 6 |
| Forêt du Retail (2) ⚠️ | Le Retail › Parthenay-Gâtine | 6 |
| Forêt de Azay-sur-Thouet (10) ⚠️ | Azay-sur-Thouet › Parthenay-Gâtine | 6 |
| Bois de Mauléon (110) ⚠️ | Mauléon › Bocage Bressuirais | 6 |
| Bois de Mauzé-sur-le-Mignon (3) ⚠️ | Mauzé-sur-le-Mignon › Niortais | 6 |
| Forêt de Valdelaume (62) ⚠️ | Valdelaume › Mellois en Poitou | 6 |
| Forêt de Plaine-et-Vallées (75) ⚠️ | Plaine-et-Vallées › Thouarsais | 6 |
| Forêt de Celles-sur-Belle (40) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 6 |
| Bois de Argentonnay (95) ⚠️ | Argentonnay › Bocage Bressuirais | 6 |
| Forêt de Beauvoir-sur-Niort (25) ⚠️ | Beauvoir-sur-Niort › Niortais | 6 |
| Forêt de Marigny (72) ⚠️ | Marigny › Niortais | 6 |
| Bois de Mauléon (156) ⚠️ | Mauléon › Bocage Bressuirais | 6 |
| Bois de Combrand (56) ⚠️ | Combrand › Bocage Bressuirais | 6 |
| Forêt de Limalonges (81) ⚠️ | Limalonges › Mellois en Poitou | 6 |
| Forêt de Saint-Pierre-des-Échaubrognes ⚠️ | Saint-Pierre-des-Échaubrognes › Bocage Bressuirais | 5 |
| Forêt de Luzay (2) ⚠️ | Luzay › Thouarsais | 5 |
| Bois de Niort (2) ⚠️ | Niort › Niortais | 5 |
| La Rapière ⚠️ | Moncoutant-sur-Sèvre › Bocage Bressuirais | 5 |
| Bois de Saint-Pardoux-Soutiers ⚠️ | Saint-Pardoux-Soutiers › Val de Gâtine | 5 |
| Bois du Tallud (4) ⚠️ | Le Tallud › Parthenay-Gâtine | 5 |
| Forêt de Échiré (4) ⚠️ | Échiré › Niortais | 5 |
| Bois de Mauléon (6) ⚠️ | Mauléon › Bocage Bressuirais | 5 |
| Forêt de Argentonnay (9) ⚠️ | Argentonnay › Bocage Bressuirais | 5 |
| Forêt de Saint-Loup-Lamairé (3) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 5 |
| Forêt de Luzay (10) ⚠️ | Luzay › Thouarsais | 5 |
| Forêt de Plaine-et-Vallées (13) ⚠️ | Plaine-et-Vallées › Thouarsais | 5 |
| Forêt de Saint-Varent (4) ⚠️ | Saint-Varent › Thouarsais | 5 |
| Forêt de Melle (5) ⚠️ | Melle › Mellois en Poitou | 5 |
| Forêt de Melle (11) ⚠️ | Melle › Mellois en Poitou | 5 |
| Forêt de Irais (6) ⚠️ | Irais › Airvaudais-Val du Thouet | 5 |
| Forêt de Magné (35) ⚠️ | Magné › Niortais | 5 |
| Forêt de Melle (21) ⚠️ | Melle › Mellois en Poitou | 5 |
| Forêt de Souvigné (5) ⚠️ | Souvigné › Haut Val de Sèvre | 5 |
| Forêt de Marcillé (7) ⚠️ | Marcillé › Mellois en Poitou | 5 |
| Forêt de Melle (22) ⚠️ | Melle › Mellois en Poitou | 5 |
| Forêt de Melle (61) ⚠️ | Melle › Mellois en Poitou | 5 |
| Forêt de Melle (71) ⚠️ | Melle › Mellois en Poitou | 5 |
| Forêt de Louzy (6) ⚠️ | Louzy › Thouarsais | 5 |
| Bois de Louzy (5) ⚠️ | Louzy › Thouarsais | 5 |
| Forêt de Secondigné-sur-Belle (5) ⚠️ | Secondigné-sur-Belle › Mellois en Poitou | 5 |
| Forêt de Vernoux-sur-Boutonne (4) ⚠️ | Vernoux-sur-Boutonne › Mellois en Poitou | 5 |
| Forêt de Souvigné (21) ⚠️ | Souvigné › Haut Val de Sèvre | 5 |
| Forêt de Souvigné (27) ⚠️ | Souvigné › Haut Val de Sèvre | 5 |
| Forêt de Exoudun (14) ⚠️ | Exoudun › Mellois en Poitou | 5 |
| Forêt de La Mothe-Saint-Héray (27) ⚠️ | La Mothe-Saint-Héray › Mellois en Poitou | 5 |
| Forêt de La Mothe-Saint-Héray (28) ⚠️ | La Mothe-Saint-Héray › Mellois en Poitou | 5 |
| Forêt de Sainte-Eanne (34) ⚠️ | Sainte-Eanne › Haut Val de Sèvre | 5 |
| Forêt des Forges (11) ⚠️ | Les Forges › Parthenay-Gâtine | 5 |
| Forêt de Maisontiers (5) ⚠️ | Maisontiers › Airvaudais-Val du Thouet | 5 |
| Forêt de Plaine-d'Argenson (16) ⚠️ | Plaine-d'Argenson › Niortais | 5 |
| Le Bois du Chatelier ⚠️ | Fenioux › Val de Gâtine | 5 |
| Forêt de Valdelaume (32) ⚠️ | Valdelaume › Mellois en Poitou | 5 |
| Forêt de Saint-Martin-de-Sanzay (3) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 5 |
| Forêt de Lusseray (6) ⚠️ | Lusseray › Mellois en Poitou | 5 |
| Bois des Chagnasses ⚠️ | Asnières-en-Poitou › Mellois en Poitou | 5 |
| Forêt de Fenioux (33) ⚠️ | Fenioux › Val de Gâtine | 5 |
| Forêt de Villemain (13) ⚠️ | Villemain › Mellois en Poitou | 5 |
| Bois de Alloinay ⚠️ | Alloinay › Mellois en Poitou | 5 |
| Forêt de Sainte-Soline (12) ⚠️ | Sainte-Soline › Mellois en Poitou | 5 |
| Forêt de Arçais (7) ⚠️ | Arçais › Niortais | 5 |
| Forêt de Chef-Boutonne (3) ⚠️ | Chef-Boutonne › Mellois en Poitou | 5 |
| Forêt de Pamproux (17) ⚠️ | Pamproux › Haut Val de Sèvre | 5 |
| Bois de Lavault ⚠️ | Vançais › Mellois en Poitou | 5 |
| Forêt de Saint-Loup-Lamairé (16) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 5 |
| Bois de Combrand ⚠️ | Combrand › Bocage Bressuirais | 5 |
| Forêt de Availles-Thouarsais (6) ⚠️ | Availles-Thouarsais › Airvaudais-Val du Thouet | 5 |
| Forêt de Aubigny (7) ⚠️ | Aubigny › Parthenay-Gâtine | 5 |
| Bois de Cloutiron ⚠️ | Rom › Mellois en Poitou | 5 |
| Bois de la Caillette ⚠️ | Rom › Mellois en Poitou | 5 |
| Forêt de Limalonges (46) ⚠️ | Limalonges › Mellois en Poitou | 5 |
| Forêt de Lhoumois (6) ⚠️ | La Peyratte › Parthenay-Gâtine | 5 |
| Forêt de Saint-Martin-du-Fouilloux (4) ⚠️ | Saint-Martin-du-Fouilloux › Parthenay-Gâtine | 5 |
| Forêt de La Chapelle-Bertrand (10) ⚠️ | La Chapelle-Bertrand › Parthenay-Gâtine | 5 |
| Forêt du Vanneau-Irleau (6) ⚠️ | Le Vanneau-Irleau › Niortais | 5 |
| Forêt de Val en Vignes (15) ⚠️ | Val en Vignes › Thouarsais | 5 |
| Forêt de Lhoumois (10) ⚠️ | Lhoumois › Parthenay-Gâtine | 5 |
| Domaine du Puy Genest ⚠️ | Cerizay › Bocage Bressuirais | 5 |
| Forêt de Saint-Loup-Lamairé (42) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 5 |
| Forêt du Chillou (10) ⚠️ | Le Chillou › Airvaudais-Val du Thouet | 5 |
| Forêt de Saint-Loup-Lamairé (48) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 5 |
| Forêt de Vasles (27) ⚠️ | Vasles › Parthenay-Gâtine | 5 |
| Forêt de Vasles (30) ⚠️ | Vasles › Parthenay-Gâtine | 5 |
| Forêt de Airvault (89) ⚠️ | Airvault › Airvaudais-Val du Thouet | 5 |
| Forêt de Glénay (10) ⚠️ | Glénay › Thouarsais | 5 |
| Forêt de Maisontiers (8) ⚠️ | Maisontiers › Airvaudais-Val du Thouet | 5 |
| Bois de la Touche ⚠️ | Saint-Martin-de-Mâcon › Thouarsais | 5 |
| Forêt de Saint-Hilaire-la-Palud (55) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 5 |
| La Cognasse ⚠️ | Mauzé-sur-le-Mignon › Niortais | 5 |
| Forêt de Mairé-Levescault (16) ⚠️ | Mairé-Levescault › Mellois en Poitou | 5 |
| Forêt de Saint-Léger-de-Montbrun (39) ⚠️ | Saint-Léger-de-Montbrun › Thouarsais | 5 |
| Forêt de Thouars (25) ⚠️ | Thouars › Thouarsais | 5 |
| Forêt de Thouars (36) ⚠️ | Thouars › Thouarsais | 5 |
| Forêt de Thouars (39) ⚠️ | Thouars › Thouarsais | 5 |
| Forêt de Luché-Thouarsais (7) ⚠️ | Luché-Thouarsais › Thouarsais | 5 |
| Forêt de Thouars (48) ⚠️ | Thouars › Thouarsais | 5 |
| Forêt de Availles-Thouarsais (11) ⚠️ | Availles-Thouarsais › Airvaudais-Val du Thouet | 5 |
| Forêt de Airvault (104) ⚠️ | Airvault › Airvaudais-Val du Thouet | 5 |
| Forêt de Availles-Thouarsais (13) ⚠️ | Availles-Thouarsais › Airvaudais-Val du Thouet | 5 |
| Forêt de Plaine-et-Vallées (70) ⚠️ | Plaine-et-Vallées › Thouarsais | 5 |
| Forêt de Sainte-Verge ⚠️ | Sainte-Verge › Thouarsais | 5 |
| Forêt de Val en Vignes (21) ⚠️ | Val en Vignes › Thouarsais | 5 |
| Forêt de Val en Vignes (23) ⚠️ | Val en Vignes › Thouarsais | 5 |
| Forêt de Val en Vignes (51) ⚠️ | Val en Vignes › Thouarsais | 5 |
| Forêt de Loretz-d'Argenton (33) ⚠️ | Loretz-d'Argenton › Thouarsais | 5 |
| Bois de Loretz-d'Argenton (49) ⚠️ | Loretz-d'Argenton › Thouarsais | 5 |
| Forêt de Saint Maurice Étusson (8) ⚠️ | Saint Maurice Étusson › Bocage Bressuirais | 5 |
| Bois de Cerizay (2) ⚠️ | Cerizay › Bocage Bressuirais | 5 |
| Bois du Pin (4) ⚠️ | Le Pin › Bocage Bressuirais | 5 |
| Bois de Mauléon (22) ⚠️ | Mauléon › Bocage Bressuirais | 5 |
| Bois de Mauléon (32) ⚠️ | Mauléon › Bocage Bressuirais | 5 |
| Forêt de Valdelaume (59) ⚠️ | Valdelaume › Mellois en Poitou | 5 |
| Bois de Ardin (8) ⚠️ | Ardin › Val de Gâtine | 5 |
| Forêt de Bressuire (29) ⚠️ | Bressuire › Bocage Bressuirais | 5 |
| Forêt de Saint-Symphorien (37) ⚠️ | Saint-Symphorien › Niortais | 5 |
| Bois de Niort (49) ⚠️ | Niort › Niortais | 5 |
| Forêt de Tourtenay (9) ⚠️ | Tourtenay › Thouarsais | 5 |
| Forêt de Luzay (25) ⚠️ | Luzay › Thouarsais | 5 |
| Forêt de Saint-Gelais (6) ⚠️ | Saint-Gelais › Niortais | 5 |
| Forêt de Saint Maurice Étusson (13) ⚠️ | Saint Maurice Étusson › Bocage Bressuirais | 5 |
| Forêt de Argentonnay (34) ⚠️ | Argentonnay › Bocage Bressuirais | 5 |
| Bois de Mauléon (152) ⚠️ | Mauléon › Bocage Bressuirais | 5 |
| Bois du Pin (38) ⚠️ | Le Pin › Bocage Bressuirais | 5 |
| Bois de Maisonnay ⚠️ | Maisonnay › Mellois en Poitou | 4 |
| Forêt des Forges (3) ⚠️ | Les Forges › Parthenay-Gâtine | 4 |
| Forêt de Limalonges (2) ⚠️ | Limalonges › Mellois en Poitou | 4 |
| Forêt de Limalonges (3) ⚠️ | Limalonges › Mellois en Poitou | 4 |
| Forêt de Niort (2) ⚠️ | Niort › Niortais | 4 |
| Bois de Niort (12) ⚠️ | Niort › Niortais | 4 |
| Le Bois Marot ⚠️ | Beugnon-Thireuil › Val de Gâtine | 4 |
| Bois de Voulmentin ⚠️ | Voulmentin › Bocage Bressuirais | 4 |
| Forêt de Coulon ⚠️ | Coulon › Niortais | 4 |
| Bois de Secondigny (3) ⚠️ | Secondigny › Parthenay-Gâtine | 4 |
| Forêt de Augé (22) ⚠️ | Augé › Haut Val de Sèvre | 4 |
| Forêt de Augé (35) ⚠️ | Augé › Haut Val de Sèvre | 4 |
| Forêt de Fontivillié (2) ⚠️ | Fontivillié › Mellois en Poitou | 4 |
| Forêt de Mazières-en-Gâtine (2) ⚠️ | Mazières-en-Gâtine › Val de Gâtine | 4 |
| Bois de Mauléon (3) ⚠️ | Mauléon › Bocage Bressuirais | 4 |
| Forêt de Saint-Aubin-le-Cloud (3) ⚠️ | Saint-Aubin-le-Cloud › Parthenay-Gâtine | 4 |
| Forêt de Limalonges (5) ⚠️ | Limalonges › Mellois en Poitou | 4 |
| Forêt de Thénezay (13) ⚠️ | Thénezay › Parthenay-Gâtine | 4 |
| Forêt de Argentonnay (8) ⚠️ | Argentonnay › Bocage Bressuirais | 4 |
| Bois de Bressuire (3) ⚠️ | Bressuire › Bocage Bressuirais | 4 |
| Forêt de Saint-Martin-du-Fouilloux (2) ⚠️ | Saint-Martin-du-Fouilloux › Parthenay-Gâtine | 4 |
| Forêt de Airvault (15) ⚠️ | Airvault › Airvaudais-Val du Thouet | 4 |
| Forêt de Luzay (5) ⚠️ | Luzay › Thouarsais | 4 |
| Forêt de Marcillé (2) ⚠️ | Marcillé › Mellois en Poitou | 4 |
| Forêt de Fenioux (4) ⚠️ | Fenioux › Val de Gâtine | 4 |
| Forêt de Louin (5) ⚠️ | Louin › Airvaudais-Val du Thouet | 4 |
| Forêt de Melle (14) ⚠️ | Melle › Mellois en Poitou | 4 |
| Bois de Argentonnay (26) ⚠️ | Argentonnay › Bocage Bressuirais | 4 |
| Forêt de Airvault (21) ⚠️ | Airvault › Airvaudais-Val du Thouet | 4 |
| Forêt du Vert (2) ⚠️ | Le Vert › Mellois en Poitou | 4 |
| Bois de Bressuire (33) ⚠️ | Bressuire › Bocage Bressuirais | 4 |
| Forêt de Marnes (16) ⚠️ | Marnes › Thouarsais | 4 |
| Forêt de Argentonnay (18) ⚠️ | Argentonnay › Bocage Bressuirais | 4 |
| Forêt de Saint-Cyr-la-Lande (2) ⚠️ | Saint-Cyr-la-Lande › Thouarsais | 4 |
| Forêt de Saint-Germier ⚠️ | Saint-Germier › Parthenay-Gâtine | 4 |
| Forêt de Magné (7) ⚠️ | Magné › Niortais | 4 |
| Forêt de Magné (11) ⚠️ | Magné › Niortais | 4 |
| Forêt de Magné (24) ⚠️ | Magné › Niortais | 4 |
| Forêt de Sansais (5) ⚠️ | Sansais › Niortais | 4 |
| Bois de Fontivillié ⚠️ | Fontivillié › Mellois en Poitou | 4 |
| Forêt de Brioux-sur-Boutonne (2) ⚠️ | Brioux-sur-Boutonne › Mellois en Poitou | 4 |
| Forêt de Brûlain ⚠️ | Brûlain › Niortais | 4 |
| Forêt de Secondigné-sur-Belle ⚠️ | Secondigné-sur-Belle › Mellois en Poitou | 4 |
| Bois de Verrines ⚠️ | Celles-sur-Belle › Mellois en Poitou | 4 |
| Forêt de La Crèche (16) ⚠️ | La Crèche › Haut Val de Sèvre | 4 |
| Forêt de Fressines (2) ⚠️ | Fressines › Mellois en Poitou | 4 |
| Forêt de Largeasse ⚠️ | Largeasse › Bocage Bressuirais | 4 |
| Bois de Bressuire (92) ⚠️ | Bressuire › Bocage Bressuirais | 4 |
| Forêt de Valdelaume (8) ⚠️ | Valdelaume › Mellois en Poitou | 4 |
| Forêt de Marcillé (13) ⚠️ | Marcillé › Mellois en Poitou | 4 |
| Forêt de Melle (41) ⚠️ | Saint-Vincent-la-Châtre › Mellois en Poitou | 4 |
| Forêt de Melle (64) ⚠️ | Melle › Mellois en Poitou | 4 |
| Forêt de Melle (69) ⚠️ | Melle › Mellois en Poitou | 4 |
| Forêt de Beaussais-Vitré (4) ⚠️ | Beaussais-Vitré › Mellois en Poitou | 4 |
| Forêt de Périgné (22) ⚠️ | Périgné › Mellois en Poitou | 4 |
| Forêt de Beaussais-Vitré (28) ⚠️ | Beaussais-Vitré › Mellois en Poitou | 4 |
| Forêt de Secondigné-sur-Belle (9) ⚠️ | Secondigné-sur-Belle › Mellois en Poitou | 4 |
| Mouton Village ⚠️ | Vasles › Parthenay-Gâtine | 4 |
| Forêt de Exoudun (6) ⚠️ | Sepvret › Mellois en Poitou | 4 |
| Forêt de Sepvret (19) ⚠️ | Sepvret › Mellois en Poitou | 4 |
| Forêt de Chey (3) ⚠️ | Chey › Mellois en Poitou | 4 |
| Forêt de Sepvret (21) ⚠️ | Chey › Mellois en Poitou | 4 |
| Forêt de Sainte-Eanne (23) ⚠️ | Sainte-Eanne › Haut Val de Sèvre | 4 |
| Forêt de Saint-Martin-de-Saint-Maixent (21) ⚠️ | Saint-Martin-de-Saint-Maixent › Haut Val de Sèvre | 4 |
| Forêt de Clussais-la-Pommeraie (11) ⚠️ | Clussais-la-Pommeraie › Mellois en Poitou | 4 |
| Bois de Échiré ⚠️ | Échiré › Niortais | 4 |
| Forêt de Limalonges (18) ⚠️ | Limalonges › Mellois en Poitou | 4 |
| Forêt de Sciecq (3) ⚠️ | Sciecq › Niortais | 4 |
| Forêt de Melleran (12) ⚠️ | Melleran › Mellois en Poitou | 4 |
| Forêt de Melleran (18) ⚠️ | Melleran › Mellois en Poitou | 4 |
| Forêt de Rom (6) ⚠️ | Rom › Mellois en Poitou | 4 |
| Forêt de Villemain (11) ⚠️ | Villemain › Mellois en Poitou | 4 |
| Bois de Maisonnay (6) ⚠️ | Maisonnay › Mellois en Poitou | 4 |
| Forêt de Saint-Vincent-la-Châtre (11) ⚠️ | Saint-Vincent-la-Châtre › Mellois en Poitou | 4 |
| Forêt de Saint-Coutant (5) ⚠️ | Saint-Coutant › Mellois en Poitou | 4 |
| Forêt de Saint-Coutant (20) ⚠️ | Saint-Coutant › Mellois en Poitou | 4 |
| Forêt de Saint-Hilaire-la-Palud (10) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 4 |
| Forêt de Saint-Hilaire-la-Palud (16) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 4 |
| Forêt de Secondigné-sur-Belle (25) ⚠️ | Secondigné-sur-Belle › Mellois en Poitou | 4 |
| Forêt de Brieuil-sur-Chizé (4) ⚠️ | Brieuil-sur-Chizé › Mellois en Poitou | 4 |
| Forêt de Rom (8) ⚠️ | Rom › Mellois en Poitou | 4 |
| Forêt de Saint-Romans-lès-Melle (8) ⚠️ | Melle › Mellois en Poitou | 4 |
| Forêt de Saint-Paul-en-Gâtine (12) ⚠️ | Saint-Paul-en-Gâtine › Bocage Bressuirais | 4 |
| Forêt de Assais-les-Jumeaux (9) ⚠️ | Assais-les-Jumeaux › Airvaudais-Val du Thouet | 4 |
| Forêt de Assais-les-Jumeaux (18) ⚠️ | Assais-les-Jumeaux › Airvaudais-Val du Thouet | 4 |
| Forêt de Airvault (57) ⚠️ | Airvault › Airvaudais-Val du Thouet | 4 |
| Bois de Cirières (12) ⚠️ | Cirières › Bocage Bressuirais | 4 |
| Bois de Chiché (7) ⚠️ | Chiché › Bocage Bressuirais | 4 |
| Bois de Faye-l'Abbesse (3) ⚠️ | Faye-l'Abbesse › Bocage Bressuirais | 4 |
| Forêt de Airvault (60) ⚠️ | Airvault › Airvaudais-Val du Thouet | 4 |
| Bois de Grelet ⚠️ | Rom › Mellois en Poitou | 4 |
| Bois de Rom (17) ⚠️ | Rom › Mellois en Poitou | 4 |
| Forêt de Arçais (9) ⚠️ | Arçais › Niortais | 4 |
| Forêt de Assais-les-Jumeaux (37) ⚠️ | Assais-les-Jumeaux › Airvaudais-Val du Thouet | 4 |
| Forêt de La Ferrière-en-Parthenay (9) ⚠️ | La Ferrière-en-Parthenay › Parthenay-Gâtine | 4 |
| Forêt de La Ferrière-en-Parthenay (10) ⚠️ | La Ferrière-en-Parthenay › Parthenay-Gâtine | 4 |
| Forêt de Vasles (24) ⚠️ | Vasles › Parthenay-Gâtine | 4 |
| Forêt de Limalonges (25) ⚠️ | Limalonges › Mellois en Poitou | 4 |
| Forêt de Limalonges (59) ⚠️ | Limalonges › Mellois en Poitou | 4 |
| Forêt de La Ferrière-en-Parthenay (12) ⚠️ | La Ferrière-en-Parthenay › Parthenay-Gâtine | 4 |
| Forêt de Ardin (3) ⚠️ | Ardin › Val de Gâtine | 4 |
| Forêt de La Peyratte (16) ⚠️ | La Peyratte › Parthenay-Gâtine | 4 |
| Forêt de Vernoux-en-Gâtine (8) ⚠️ | Vernoux-en-Gâtine › Parthenay-Gâtine | 4 |
| Forêt de Cerizay (2) ⚠️ | Cerizay › Bocage Bressuirais | 4 |
| Forêt de Beaulieu-sous-Parthenay (3) ⚠️ | Beaulieu-sous-Parthenay › Val de Gâtine | 4 |
| Forêt de Beaulieu-sous-Parthenay (4) ⚠️ | Beaulieu-sous-Parthenay › Val de Gâtine | 4 |
| Bois de Saint-Martin-de-Sanzay (5) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 4 |
| Forêt de Saint-Léger-de-Montbrun (38) ⚠️ | Saint-Léger-de-Montbrun › Thouarsais | 4 |
| Forêt de Arçais (12) ⚠️ | Le Vanneau-Irleau › Niortais | 4 |
| Bois de Nueil-les-Aubiers (38) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 4 |
| Bois de La Chapelle-Bertrand ⚠️ | La Chapelle-Bertrand › Parthenay-Gâtine | 4 |
| Forêt de Niort (85) ⚠️ | Niort › Niortais | 4 |
| Forêt de Niort (91) ⚠️ | Niort › Niortais | 4 |
| Forêt de Sauzé-entre-Bois (45) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 4 |
| Forêt de Saint-Rémy (8) ⚠️ | Saint-Rémy › Niortais | 4 |
| Forêt de Saint-Hilaire-la-Palud (37) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 4 |
| Forêt de Saint-Hilaire-la-Palud (41) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 4 |
| Forêt du Busseau (11) ⚠️ | Le Busseau › Val de Gâtine | 4 |
| Forêt de Mairé-Levescault (10) ⚠️ | Mairé-Levescault › Mellois en Poitou | 4 |
| Forêt de Mairé-Levescault (13) ⚠️ | Mairé-Levescault › Mellois en Poitou | 4 |
| Forêt de Saint-Martin-de-Sanzay (23) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 4 |
| Forêt de Rom (19) ⚠️ | Rom › Mellois en Poitou | 4 |
| Forêt de Faye-sur-Ardin (3) ⚠️ | Faye-sur-Ardin › Val de Gâtine | 4 |
| Forêt de Glénay (14) ⚠️ | Glénay › Thouarsais | 4 |
| Forêt de Limalonges (62) ⚠️ | Limalonges › Mellois en Poitou | 4 |
| Bois de Montravers (4) ⚠️ | Montravers › Bocage Bressuirais | 4 |
| Bois de Saint-Martin-de-Sanzay (25) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 4 |
| Bois de Saint-Cyr-la-Lande (30) ⚠️ | Saint-Cyr-la-Lande › Thouarsais | 4 |
| Forêt de Coulonges-Thouarsais (7) ⚠️ | Coulonges-Thouarsais › Thouarsais | 4 |
| Forêt de Thouars (51) ⚠️ | Thouars › Thouarsais | 4 |
| Bois de Assais-les-Jumeaux (3) ⚠️ | Assais-les-Jumeaux › Airvaudais-Val du Thouet | 4 |
| Bois de Sainte-Verge (11) ⚠️ | Sainte-Verge › Thouarsais | 4 |
| Forêt de Val en Vignes (24) ⚠️ | Val en Vignes › Thouarsais | 4 |
| Forêt de Saint Maurice Étusson (9) ⚠️ | Saint Maurice Étusson › Bocage Bressuirais | 4 |
| Bois de Argentonnay (56) ⚠️ | Argentonnay › Bocage Bressuirais | 4 |
| Bois de Argentonnay (61) ⚠️ | Argentonnay › Bocage Bressuirais | 4 |
| Bois de Argentonnay (72) ⚠️ | Argentonnay › Bocage Bressuirais | 4 |
| Bois de Argentonnay (74) ⚠️ | Argentonnay › Bocage Bressuirais | 4 |
| Bois de Argentonnay (84) ⚠️ | Argentonnay › Bocage Bressuirais | 4 |
| Bois de Largeasse ⚠️ | Largeasse › Bocage Bressuirais | 4 |
| Forêt de Vançais (3) ⚠️ | Vançais › Mellois en Poitou | 4 |
| Bois de Nueil-les-Aubiers (55) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 4 |
| Bois de Mauléon (26) ⚠️ | Mauléon › Bocage Bressuirais | 4 |
| Bois de Combrand (33) ⚠️ | Combrand › Bocage Bressuirais | 4 |
| Bois du Pin (22) ⚠️ | Le Pin › Bocage Bressuirais | 4 |
| Bois de Mauléon (93) ⚠️ | Mauléon › Bocage Bressuirais | 4 |
| Forêt de Rom (49) ⚠️ | Rom › Mellois en Poitou | 4 |
| Forêt de La Foye-Monjault (5) ⚠️ | La Foye-Monjault › Niortais | 4 |
| Forêt de Pamproux (18) ⚠️ | Pamproux › Haut Val de Sèvre | 4 |
| Bois de Ardin (7) ⚠️ | Ardin › Val de Gâtine | 4 |
| Bois de Ardin (10) ⚠️ | Ardin › Val de Gâtine | 4 |
| Forêt de Saint-Martin-de-Saint-Maixent (42) ⚠️ | Saint-Martin-de-Saint-Maixent › Haut Val de Sèvre | 4 |
| Forêt de Couture-d'Argenson (22) ⚠️ | Couture-d'Argenson › Mellois en Poitou | 4 |
| Forêt de Saint-Symphorien (31) ⚠️ | Saint-Symphorien › Niortais | 4 |
| Forêt de Sauzé-entre-Bois (92) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 4 |
| Forêt du Vert (9) ⚠️ | Le Vert › Mellois en Poitou | 4 |
| Forêt de Aiffres (42) ⚠️ | Aiffres › Niortais | 4 |
| Bois du Grand May ⚠️ | Aiffres › Niortais | 4 |
| Forêt de Niort (146) ⚠️ | Niort › Niortais | 4 |
| Forêt de Vouillé (32) ⚠️ | Vouillé › Niortais | 4 |
| Bois de Vouillé (43) ⚠️ | Vouillé › Niortais | 4 |
| Forêt de Vouillé (43) ⚠️ | Vouillé › Niortais | 4 |
| Forêt de Plaine-et-Vallées (76) ⚠️ | Plaine-et-Vallées › Thouarsais | 4 |
| Forêt de Marigny (40) ⚠️ | Marigny › Niortais | 4 |
| Forêt de Val en Vignes (54) ⚠️ | Val en Vignes › Thouarsais | 4 |
| Forêt de Celles-sur-Belle (48) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 4 |
| Forêt de Beauvoir-sur-Niort (19) ⚠️ | Beauvoir-sur-Niort › Niortais | 4 |
| Forêt de Beauvoir-sur-Niort (23) ⚠️ | Beauvoir-sur-Niort › Niortais | 4 |
| Bois de Bressuire (169) ⚠️ | Bressuire › Bocage Bressuirais | 4 |
| Bois de Nueil-les-Aubiers (129) ⚠️ | Le Pin › Bocage Bressuirais | 4 |
| Bois du Pin (36) ⚠️ | Le Pin › Bocage Bressuirais | 4 |
| Forêt de Louzy ⚠️ | Louzy › Thouarsais | 3 |
| Forêt de Pamplie (5) ⚠️ | Pamplie › Val de Gâtine | 3 |
| Bois de Bressuire ⚠️ | Bressuire › Bocage Bressuirais | 3 |
| Forêt des Forges (4) ⚠️ | Les Forges › Parthenay-Gâtine | 3 |
| Forêt de Sainte-Néomaye (8) ⚠️ | Sainte-Néomaye › Haut Val de Sèvre | 3 |
| Forêt de Sainte-Néomaye (19) ⚠️ | Sainte-Néomaye › Haut Val de Sèvre | 3 |
| Forêt de Romans (7) ⚠️ | Romans › Haut Val de Sèvre | 3 |
| Forêt de Saint-Martin-de-Saint-Maixent (4) ⚠️ | Saint-Martin-de-Saint-Maixent › Haut Val de Sèvre | 3 |
| Bois de Voulmentin (4) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 3 |
| Forêt de Nueil-les-Aubiers (2) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 3 |
| Forêt de Nueil-les-Aubiers (3) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 3 |
| Forêt de Augé (4) ⚠️ | Augé › Haut Val de Sèvre | 3 |
| Forêt de Augé (8) ⚠️ | Augé › Haut Val de Sèvre | 3 |
| Forêt de Azay-le-Brûlé (3) ⚠️ | Azay-le-Brûlé › Haut Val de Sèvre | 3 |
| Forêt de Azay-le-Brûlé (9) ⚠️ | Azay-le-Brûlé › Haut Val de Sèvre | 3 |
| Forêt de Azay-le-Brûlé (10) ⚠️ | Azay-le-Brûlé › Haut Val de Sèvre | 3 |
| Forêt de Thénezay (7) ⚠️ | Thénezay › Parthenay-Gâtine | 3 |
| Forêt de Augé (62) ⚠️ | Augé › Haut Val de Sèvre | 3 |
| Forêt de Mairé-Levescault (6) ⚠️ | Mairé-Levescault › Mellois en Poitou | 3 |
| Forêt de Melleran (5) ⚠️ | Melleran › Mellois en Poitou | 3 |
| Bois de Bramefont ⚠️ | Melle › Mellois en Poitou | 3 |
| Bois de Saint-Pierre-des-Échaubrognes ⚠️ | Saint-Pierre-des-Échaubrognes › Bocage Bressuirais | 3 |
| Bois du Château de Chaillé ⚠️ | Melle › Mellois en Poitou | 3 |
| Forêt de La Peyratte (3) ⚠️ | La Peyratte › Parthenay-Gâtine | 3 |
| Forêt de Neuvy-Bouin (5) ⚠️ | Neuvy-Bouin › Bocage Bressuirais | 3 |
| Forêt de Fénery (2) ⚠️ | Fénery › Parthenay-Gâtine | 3 |
| Forêt de Saint-Aubin-le-Cloud (2) ⚠️ | Saint-Aubin-le-Cloud › Parthenay-Gâtine | 3 |
| Forêt de Neuvy-Bouin (8) ⚠️ | Neuvy-Bouin › Bocage Bressuirais | 3 |
| Bois de Nueil-les-Aubiers (24) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 3 |
| Bois de Châtillon-sur-Thouet (5) ⚠️ | Châtillon-sur-Thouet › Parthenay-Gâtine | 3 |
| Forêt de La Peyratte (6) ⚠️ | La Peyratte › Parthenay-Gâtine | 3 |
| Forêt de Bressuire (9) ⚠️ | Bressuire › Bocage Bressuirais | 3 |
| Forêt de Airvault (14) ⚠️ | Airvault › Airvaudais-Val du Thouet | 3 |
| Forêt de La Peyratte (10) ⚠️ | La Peyratte › Parthenay-Gâtine | 3 |
| Forêt de Fontivillié (3) ⚠️ | Fontivillié › Mellois en Poitou | 3 |
| Forêt de Glénay (6) ⚠️ | Glénay › Thouarsais | 3 |
| Forêt de Geay ⚠️ | Geay › Bocage Bressuirais | 3 |
| Forêt de Louin (6) ⚠️ | Louin › Airvaudais-Val du Thouet | 3 |
| Forêt de Louin (7) ⚠️ | Louin › Airvaudais-Val du Thouet | 3 |
| Bois de Argentonnay (4) ⚠️ | Argentonnay › Bocage Bressuirais | 3 |
| Forêt de Saint Maurice Étusson (6) ⚠️ | Saint Maurice Étusson › Bocage Bressuirais | 3 |
| Forêt de Saint-Léger-de-Montbrun (13) ⚠️ | Saint-Léger-de-Montbrun › Thouarsais | 3 |
| Forêt de Saint-Léger-de-Montbrun (16) ⚠️ | Saint-Léger-de-Montbrun › Thouarsais | 3 |
| Forêt de Coulon (11) ⚠️ | Coulon › Niortais | 3 |
| Forêt de Niort (15) ⚠️ | Niort › Niortais | 3 |
| Forêt de Plaine-et-Vallées (18) ⚠️ | Plaine-et-Vallées › Thouarsais | 3 |
| Forêt de Airvault (28) ⚠️ | Airvault › Airvaudais-Val du Thouet | 3 |
| Forêt de Airvault (38) ⚠️ | Airvault › Airvaudais-Val du Thouet | 3 |
| Forêt de Bessines (2) ⚠️ | Bessines › Niortais | 3 |
| Forêt de Magné (10) ⚠️ | Magné › Niortais | 3 |
| Forêt de Sansais ⚠️ | Sansais › Niortais | 3 |
| Forêt de Magné (19) ⚠️ | Magné › Niortais | 3 |
| Forêt de Magné (20) ⚠️ | Magné › Niortais | 3 |
| Bois de Bressuire (89) ⚠️ | Bressuire › Bocage Bressuirais | 3 |
| Forêt de Lezay (8) ⚠️ | Lezay › Mellois en Poitou | 3 |
| Forêt de Alloinay (9) ⚠️ | Alloinay › Mellois en Poitou | 3 |
| Forêt de Melleran (7) ⚠️ | Melleran › Mellois en Poitou | 3 |
| Forêt de Celles-sur-Belle (4) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 3 |
| Forêt de Sansais (25) ⚠️ | Sansais › Niortais | 3 |
| Forêt de Airvault (40) ⚠️ | Airvault › Airvaudais-Val du Thouet | 3 |
| Forêt de Melle (25) ⚠️ | Melle › Mellois en Poitou | 3 |
| Forêt de Melle (57) ⚠️ | Melle › Mellois en Poitou | 3 |
| Forêt de Melle (60) ⚠️ | Melle › Mellois en Poitou | 3 |
| Forêt de Melle (66) ⚠️ | Melle › Mellois en Poitou | 3 |
| Forêt de Celles-sur-Belle (17) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 3 |
| Forêt de Beaussais-Vitré (31) ⚠️ | Beaussais-Vitré › Mellois en Poitou | 3 |
| Forêt de Souvigné (6) ⚠️ | Souvigné › Haut Val de Sèvre | 3 |
| Forêt de Prailles-la-Couarde (34) ⚠️ | Prailles-la-Couarde › Mellois en Poitou | 3 |
| Forêt de Prailles-la-Couarde (35) ⚠️ | Prailles-la-Couarde › Mellois en Poitou | 3 |
| Forêt de Prailles-la-Couarde (38) ⚠️ | Prailles-la-Couarde › Mellois en Poitou | 3 |
| Forêt de Prailles-la-Couarde (40) ⚠️ | Prailles-la-Couarde › Mellois en Poitou | 3 |
| Forêt de Souvigné (11) ⚠️ | Souvigné › Haut Val de Sèvre | 3 |
| Forêt de Séligné (6) ⚠️ | Séligné › Mellois en Poitou | 3 |
| Forêt de Souvigné (38) ⚠️ | Souvigné › Haut Val de Sèvre | 3 |
| Forêt de Saint-Léger-de-Montbrun (20) ⚠️ | Saint-Léger-de-Montbrun › Thouarsais | 3 |
| Forêt de Secondigné-sur-Belle (16) ⚠️ | Secondigné-sur-Belle › Mellois en Poitou | 3 |
| Forêt de Exoudun (12) ⚠️ | Exoudun › Mellois en Poitou | 3 |
| Forêt de La Mothe-Saint-Héray (9) ⚠️ | La Mothe-Saint-Héray › Mellois en Poitou | 3 |
| Forêt de Sainte-Eanne (20) ⚠️ | Sainte-Eanne › Haut Val de Sèvre | 3 |
| Forêt de Saint-Martin-de-Saint-Maixent (31) ⚠️ | Saint-Martin-de-Saint-Maixent › Haut Val de Sèvre | 3 |
| Forêt des Forges (12) ⚠️ | Les Forges › Parthenay-Gâtine | 3 |
| Aire de loisirs du Vallon ⚠️ | Saint-Martin-de-Saint-Maixent › Haut Val de Sèvre | 3 |
| Forêt de Plaine-d'Argenson (12) ⚠️ | Plaine-d'Argenson › Niortais | 3 |
| Forêt de Saint-Léger-de-Montbrun (26) ⚠️ | Saint-Léger-de-Montbrun › Thouarsais | 3 |
| Forêt de Couture-d'Argenson (6) ⚠️ | Couture-d'Argenson › Mellois en Poitou | 3 |
| Forêt de Villemain (7) ⚠️ | Villemain › Mellois en Poitou | 3 |
| Forêt de Couture-d'Argenson (11) ⚠️ | Couture-d'Argenson › Mellois en Poitou | 3 |
| Forêt de Exireuil (5) ⚠️ | Nanteuil › Haut Val de Sèvre | 3 |
| Forêt de Limalonges (11) ⚠️ | Limalonges › Mellois en Poitou | 3 |
| Forêt de Limalonges (19) ⚠️ | Limalonges › Mellois en Poitou | 3 |
| Forêt de Valdelaume (19) ⚠️ | Valdelaume › Mellois en Poitou | 3 |
| Forêt de Valdelaume (37) ⚠️ | Valdelaume › Mellois en Poitou | 3 |
| Forêt de Valdelaume (38) ⚠️ | Valdelaume › Mellois en Poitou | 3 |
| Forêt de Valdelaume (51) ⚠️ | Valdelaume › Mellois en Poitou | 3 |
| Forêt de Melleran (22) ⚠️ | Melleran › Mellois en Poitou | 3 |
| Forêt de Villefollet (7) ⚠️ | Villefollet › Mellois en Poitou | 3 |
| Forêt de Beugnon-Thireuil (7) ⚠️ | Beugnon-Thireuil › Val de Gâtine | 3 |
| Forêt de Saint-Gelais (2) ⚠️ | Saint-Gelais › Niortais | 3 |
| Forêt de Saint-Hilaire-la-Palud (23) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 3 |
| Forêt de Adilly ⚠️ | Adilly › Parthenay-Gâtine | 3 |
| Forêt de Sauzé-entre-Bois (20) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 3 |
| Forêt de Chérigné (7) ⚠️ | Chérigné › Mellois en Poitou | 3 |
| Parc de La Crèche (5) ⚠️ | La Crèche › Haut Val de Sèvre | 3 |
| Forêt de Loretz-d'Argenton (7) ⚠️ | Loretz-d'Argenton › Thouarsais | 3 |
| Forêt de Frontenay-Rohan-Rohan (6) ⚠️ | Granzay-Gript › Niortais | 3 |
| Forêt de Loubillé (3) ⚠️ | Loubillé › Mellois en Poitou | 3 |
| Bois de Val-du-Mignon ⚠️ | Val-du-Mignon › Niortais | 3 |
| Bois de Mauléon (13) ⚠️ | Mauléon › Bocage Bressuirais | 3 |
| Forêt de Assais-les-Jumeaux (28) ⚠️ | Assais-les-Jumeaux › Airvaudais-Val du Thouet | 3 |
| Forêt de Saint-Loup-Lamairé (9) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 3 |
| Forêt de Airvault (49) ⚠️ | Airvault › Airvaudais-Val du Thouet | 3 |
| Forêt de Availles-Thouarsais (4) ⚠️ | Availles-Thouarsais › Airvaudais-Val du Thouet | 3 |
| Forêt de Irais (8) ⚠️ | Irais › Airvaudais-Val du Thouet | 3 |
| Bois de Bressuire (146) ⚠️ | Bressuire › Bocage Bressuirais | 3 |
| Bois de Chiché (3) ⚠️ | Chiché › Bocage Bressuirais | 3 |
| Forêt de Thénezay (42) ⚠️ | Thénezay › Parthenay-Gâtine | 3 |
| Forêt de Thénezay (43) ⚠️ | Thénezay › Parthenay-Gâtine | 3 |
| Forêt de Lhoumois (5) ⚠️ | Lhoumois › Parthenay-Gâtine | 3 |
| Forêt de Gourgé (8) ⚠️ | Gourgé › Parthenay-Gâtine | 3 |
| Forêt de Échiré (8) ⚠️ | Échiré › Niortais | 3 |
| Le Patureau ⚠️ | Rom › Mellois en Poitou | 3 |
| Bois de Rom (12) ⚠️ | Rom › Mellois en Poitou | 3 |
| Forêt de La Chapelle-Bertrand ⚠️ | La Chapelle-Bertrand › Parthenay-Gâtine | 3 |
| Forêt de Limalonges (51) ⚠️ | Limalonges › Mellois en Poitou | 3 |
| Forêt de La Ferrière-en-Parthenay (15) ⚠️ | La Ferrière-en-Parthenay › Parthenay-Gâtine | 3 |
| Forêt de Ardin (4) ⚠️ | Ardin › Val de Gâtine | 3 |
| Forêt de La Chapelle-Bertrand (7) ⚠️ | La Chapelle-Bertrand › Parthenay-Gâtine | 3 |
| Forêt de La Chapelle-Bertrand (8) ⚠️ | La Chapelle-Bertrand › Parthenay-Gâtine | 3 |
| Forêt de Gourgé (12) ⚠️ | Gourgé › Parthenay-Gâtine | 3 |
| Forêt de Exireuil (7) ⚠️ | Exireuil › Haut Val de Sèvre | 3 |
| Bois de Rocan ⚠️ | Saivres › Haut Val de Sèvre | 3 |
| Forêt de Saivres (21) ⚠️ | Saivres › Haut Val de Sèvre | 3 |
| Forêt de Saurais (4) ⚠️ | Saurais › Parthenay-Gâtine | 3 |
| Forêt de Saint-Loup-Lamairé (39) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 3 |
| Forêt de Mazières-en-Gâtine (19) ⚠️ | Mazières-en-Gâtine › Val de Gâtine | 3 |
| Forêt de Cerizay (10) ⚠️ | Cerizay › Bocage Bressuirais | 3 |
| Bois de Faye-l'Abbesse (5) ⚠️ | Faye-l'Abbesse › Bocage Bressuirais | 3 |
| Forêt du Chillou (7) ⚠️ | Le Chillou › Airvaudais-Val du Thouet | 3 |
| Forêt de Marnes (29) ⚠️ | Marnes › Thouarsais | 3 |
| Forêt de Saint-Loup-Lamairé (40) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 3 |
| Forêt de Saint-Loup-Lamairé (41) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 3 |
| Forêt de Mauzé-sur-le-Mignon (5) ⚠️ | Mauzé-sur-le-Mignon › Niortais | 3 |
| Bois de Val-du-Mignon (2) ⚠️ | Val-du-Mignon › Niortais | 3 |
| Forêt de Lageon ⚠️ | Lageon › Parthenay-Gâtine | 3 |
| Forêt de Ensigné (8) ⚠️ | Ensigné › Mellois en Poitou | 3 |
| Forêt du Vanneau-Irleau (8) ⚠️ | Le Vanneau-Irleau › Niortais | 3 |
| Forêt de Niort (90) ⚠️ | Niort › Niortais | 3 |
| Forêt de Arçais (22) ⚠️ | Arçais › Niortais | 3 |
| Forêt de Saint-Hilaire-la-Palud (42) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 3 |
| Forêt de Saint-Hilaire-la-Palud (48) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 3 |
| Forêt de Saint-Hilaire-la-Palud (51) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 3 |
| Forêt de Saint-Hilaire-la-Palud (52) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 3 |
| Forêt de Saint-Hilaire-la-Palud (53) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 3 |
| Forêt de Alloinay (24) ⚠️ | Alloinay › Mellois en Poitou | 3 |
| Parc de Bressuire (23) ⚠️ | Bressuire › Bocage Bressuirais | 3 |
| Forêt de Mairé-Levescault (14) ⚠️ | Mairé-Levescault › Mellois en Poitou | 3 |
| Bois de Saint-Gilles ⚠️ | Beauvoir-sur-Niort › Niortais | 3 |
| Forêt de Ensigné (9) ⚠️ | Ensigné › Mellois en Poitou | 3 |
| Forêt du Vert (6) ⚠️ | Le Vert › Mellois en Poitou | 3 |
| Forêt de Chizé (20) ⚠️ | Chizé › Mellois en Poitou | 3 |
| Forêt de Sainte-Ouenne (6) ⚠️ | Sainte-Ouenne › Val de Gâtine | 3 |
| Forêt de Sainte-Ouenne (9) ⚠️ | Sainte-Ouenne › Val de Gâtine | 3 |
| Forêt de Saint-Martin-de-Sanzay (22) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 3 |
| Forêt de Sainte-Ouenne (15) ⚠️ | Sainte-Ouenne › Val de Gâtine | 3 |
| Forêt de Louzy (8) ⚠️ | Louzy › Thouarsais | 3 |
| Forêt de Sauzé-entre-Bois (52) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 3 |
| Forêt de Saint-Martin-de-Sanzay (38) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 3 |
| Forêt de Brion-près-Thouet (3) ⚠️ | Brion-près-Thouet › Thouarsais | 3 |
| Forêt de Saint-Martin-de-Mâcon (8) ⚠️ | Saint-Martin-de-Mâcon › Thouarsais | 3 |
| Forêt de Saint-Martin-de-Mâcon (9) ⚠️ | Saint-Martin-de-Mâcon › Thouarsais | 3 |
| Forêt de Coulonges-Thouarsais (9) ⚠️ | Coulonges-Thouarsais › Thouarsais | 3 |
| Forêt de Thouars (29) ⚠️ | Thouars › Thouarsais | 3 |
| Bois de Thouars (26) ⚠️ | Thouars › Thouarsais | 3 |
| Forêt de Saint-Généroux (10) ⚠️ | Saint-Généroux › Thouarsais | 3 |
| Forêt de Saint-Généroux (11) ⚠️ | Saint-Généroux › Thouarsais | 3 |
| Forêt de Saint-Martin-de-Mâcon (12) ⚠️ | Saint-Martin-de-Mâcon › Thouarsais | 3 |
| Forêt de Thouars (53) ⚠️ | Thouars › Thouarsais | 3 |
| Bois de Argentonnay (53) ⚠️ | Saint Maurice Étusson › Bocage Bressuirais | 3 |
| Forêt de Loretz-d'Argenton (14) ⚠️ | Loretz-d'Argenton › Thouarsais | 3 |
| Forêt de Loretz-d'Argenton (17) ⚠️ | Loretz-d'Argenton › Thouarsais | 3 |
| Forêt de Loretz-d'Argenton (18) ⚠️ | Loretz-d'Argenton › Thouarsais | 3 |
| Forêt de Val en Vignes (45) ⚠️ | Val en Vignes › Thouarsais | 3 |
| Forêt de Fressines (4) ⚠️ | Fressines › Mellois en Poitou | 3 |
| Bois de Loretz-d'Argenton (57) ⚠️ | Loretz-d'Argenton › Thouarsais | 3 |
| Forêt de Loretz-d'Argenton (34) ⚠️ | Loretz-d'Argenton › Thouarsais | 3 |
| Bois de Val en Vignes (80) ⚠️ | Val en Vignes › Thouarsais | 3 |
| Bois de Argentonnay (62) ⚠️ | Argentonnay › Bocage Bressuirais | 3 |
| Bois de Argentonnay (79) ⚠️ | Argentonnay › Bocage Bressuirais | 3 |
| Forêt de Nueil-les-Aubiers (9) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 3 |
| Bois de Largeasse (3) ⚠️ | Largeasse › Bocage Bressuirais | 3 |
| Bois de Largeasse (4) ⚠️ | Largeasse › Bocage Bressuirais | 3 |
| Forêt de Saint-Aubin-du-Plain ⚠️ | Saint-Aubin-du-Plain › Bocage Bressuirais | 3 |
| Bois de Saint Maurice Étusson (15) ⚠️ | Saint Maurice Étusson › Bocage Bressuirais | 3 |
| Bois de Nueil-les-Aubiers (52) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 3 |
| Bois de Nueil-les-Aubiers (100) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 3 |
| Bois de Mauléon (35) ⚠️ | Mauléon › Bocage Bressuirais | 3 |
| Bois de Chanteloup ⚠️ | Chanteloup › Bocage Bressuirais | 3 |
| Bois de La Petite-Boissière (13) ⚠️ | La Petite-Boissière › Bocage Bressuirais | 3 |
| Bois du Pin (21) ⚠️ | Le Pin › Bocage Bressuirais | 3 |
| Bois du Pin (29) ⚠️ | Le Pin › Bocage Bressuirais | 3 |
| Forêt de Saint-Laurs ⚠️ | Saint-Laurs › Val de Gâtine | 3 |
| Bois de Cerizay (6) ⚠️ | Cerizay › Bocage Bressuirais | 3 |
| Forêt de Neuvy-Bouin (10) ⚠️ | Neuvy-Bouin › Bocage Bressuirais | 3 |
| Bois de Saint-Pierre-des-Échaubrognes (14) ⚠️ | Saint-Pierre-des-Échaubrognes › Bocage Bressuirais | 3 |
| Bois de Mauléon (90) ⚠️ | Mauléon › Bocage Bressuirais | 3 |
| Bois de Mauléon (113) ⚠️ | Mauléon › Bocage Bressuirais | 3 |
| Bois de Mauléon (133) ⚠️ | Mauléon › Bocage Bressuirais | 3 |
| Bois de Mauléon (137) ⚠️ | Mauléon › Bocage Bressuirais | 3 |
| Forêt de La Chapelle-Bertrand (13) ⚠️ | La Chapelle-Bertrand › Parthenay-Gâtine | 3 |
| Le Rocher Branlant ⚠️ | Largeasse › Bocage Bressuirais | 3 |
| Bois de Val-du-Mignon (5) ⚠️ | Val-du-Mignon › Niortais | 3 |
| Bois de Faye-sur-Ardin (6) ⚠️ | Faye-sur-Ardin › Val de Gâtine | 3 |
| Forêt de Exoudun (23) ⚠️ | Exoudun › Mellois en Poitou | 3 |
| Bois de Lens ⚠️ | Saint-Symphorien › Niortais | 3 |
| Forêt de Vouillé (27) ⚠️ | Vouillé › Niortais | 3 |
| Forêt de Vouillé (28) ⚠️ | Vouillé › Niortais | 3 |
| Forêt de Niort (139) ⚠️ | Niort › Niortais | 3 |
| Bois de Vouillé (32) ⚠️ | Vouillé › Niortais | 3 |
| Bois de Vouillé (37) ⚠️ | Vouillé › Niortais | 3 |
| Bois de Saint-Martin-de-Sanzay (40) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 3 |
| Bois de Aigondigné (26) ⚠️ | Aigondigné › Mellois en Poitou | 3 |
| Forêt de Chauray (8) ⚠️ | Chauray › Niortais | 3 |
| Bois de Chauray (24) ⚠️ | Chauray › Niortais | 3 |
| Bois de François (2) ⚠️ | François › Haut Val de Sèvre | 3 |
| Bois de Aigondigné (66) ⚠️ | Aigondigné › Mellois en Poitou | 3 |
| Forêt de Celles-sur-Belle (35) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 3 |
| Forêt de Celles-sur-Belle (36) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 3 |
| Forêt de Celles-sur-Belle (38) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 3 |
| Forêt de Celles-sur-Belle (42) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 3 |
| Forêt de Saint Maurice Étusson (12) ⚠️ | Saint Maurice Étusson › Bocage Bressuirais | 3 |
| Forêt de Celles-sur-Belle (44) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 3 |
| Forêt de Celles-sur-Belle (49) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 3 |
| Forêt de Saurais (9) ⚠️ | Saurais › Parthenay-Gâtine | 3 |
| Forêt de La Chapelle-Bertrand (14) ⚠️ | La Chapelle-Bertrand › Parthenay-Gâtine | 3 |
| Bois Rault ⚠️ | Périgné › Mellois en Poitou | 3 |
| Bois de Voulmentin (32) ⚠️ | Voulmentin › Bocage Bressuirais | 3 |
| Bois de Nueil-les-Aubiers (120) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 3 |
| Bois de Combrand (53) ⚠️ | Combrand › Bocage Bressuirais | 3 |
| Bois de Cerizay (11) ⚠️ | Cerizay › Bocage Bressuirais | 3 |
| Forêt de Rom (64) ⚠️ | Rom › Mellois en Poitou | 3 |
| Forêt de Saint-Léger-de-Montbrun (44) ⚠️ | Saint-Léger-de-Montbrun › Thouarsais | 3 |
| Forêt de Vernoux-en-Gâtine ⚠️ | Vernoux-en-Gâtine › Parthenay-Gâtine | 2 |
| Forêt de Villemain (2) ⚠️ | Villemain › Mellois en Poitou | 2 |
| Forêt de Argentonnay (2) ⚠️ | Argentonnay › Bocage Bressuirais | 2 |
| Forêt du Vert ⚠️ | Le Vert › Mellois en Poitou | 2 |
| Forêt de Sauzé-entre-Bois (5) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 2 |
| Château de Bressuire ⚠️ | Bressuire › Bocage Bressuirais | 2 |
| Bois de Niort (3) ⚠️ | Niort › Niortais | 2 |
| Forêt de Villemain (6) ⚠️ | Villemain › Mellois en Poitou | 2 |
| Forêt de La Crèche (5) ⚠️ | La Crèche › Haut Val de Sèvre | 2 |
| Forêt de Sainte-Néomaye (3) ⚠️ | Sainte-Néomaye › Haut Val de Sèvre | 2 |
| Forêt de Sainte-Néomaye (4) ⚠️ | Sainte-Néomaye › Haut Val de Sèvre | 2 |
| Bois de la Fosse ⚠️ | Sainte-Néomaye › Haut Val de Sèvre | 2 |
| Forêt de La Crèche (10) ⚠️ | La Crèche › Haut Val de Sèvre | 2 |
| Forêt de La Crèche (11) ⚠️ | La Crèche › Haut Val de Sèvre | 2 |
| Forêt de Saint-Martin-de-Saint-Maixent (7) ⚠️ | Saint-Martin-de-Saint-Maixent › Haut Val de Sèvre | 2 |
| Forêt de Secondigny ⚠️ | Secondigny › Parthenay-Gâtine | 2 |
| Forêt de Bressuire (5) ⚠️ | Bressuire › Bocage Bressuirais | 2 |
| Bois de Nueil-les-Aubiers (2) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 2 |
| Forêt de Saint-Pardoux-Soutiers (3) ⚠️ | Saint-Pardoux-Soutiers › Val de Gâtine | 2 |
| Forêt de Saint-Pardoux-Soutiers (4) ⚠️ | Saint-Pardoux-Soutiers › Val de Gâtine | 2 |
| Bois de Pompaire (2) ⚠️ | Pompaire › Parthenay-Gâtine | 2 |
| Bois de Vernoux-en-Gâtine (2) ⚠️ | Vernoux-en-Gâtine › Parthenay-Gâtine | 2 |
| Bois de Voulmentin (7) ⚠️ | Voulmentin › Bocage Bressuirais | 2 |
| Bois de Secondigny ⚠️ | Secondigny › Parthenay-Gâtine | 2 |
| Forêt de Augé (5) ⚠️ | Augé › Haut Val de Sèvre | 2 |
| Forêt de Augé (6) ⚠️ | Augé › Haut Val de Sèvre | 2 |
| Forêt de Augé (10) ⚠️ | Augé › Haut Val de Sèvre | 2 |
| Forêt de Azay-le-Brûlé (5) ⚠️ | Azay-le-Brûlé › Haut Val de Sèvre | 2 |
| Forêt de Augé (25) ⚠️ | Azay-le-Brûlé › Haut Val de Sèvre | 2 |
| Forêt de Saint-Léger-de-Montbrun (2) ⚠️ | Saint-Léger-de-Montbrun › Thouarsais | 2 |
| Forêt de Saint-Léger-de-Montbrun (4) ⚠️ | Thouars › Thouarsais | 2 |
| Forêt de Augé (72) ⚠️ | Augé › Haut Val de Sèvre | 2 |
| Forêt de Melleran (2) ⚠️ | Melleran › Mellois en Poitou | 2 |
| Forêt de Clussais-la-Pommeraie (4) ⚠️ | Clussais-la-Pommeraie › Mellois en Poitou | 2 |
| Forêt de Clussais-la-Pommeraie (5) ⚠️ | Clussais-la-Pommeraie › Mellois en Poitou | 2 |
| Forêt de Augé (92) ⚠️ | Augé › Haut Val de Sèvre | 2 |
| Forêt de Melleran (4) ⚠️ | Melleran › Mellois en Poitou | 2 |
| Forêt de Coulon (4) ⚠️ | Coulon › Niortais | 2 |
| Bois Haut ⚠️ | Melle › Mellois en Poitou | 2 |
| Bois de Mauléon (4) ⚠️ | Mauléon › Bocage Bressuirais | 2 |
| Bois de Nueil-les-Aubiers (7) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 2 |
| Bois de Nueil-les-Aubiers (9) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 2 |
| Forêt de Airvault (7) ⚠️ | Airvault › Airvaudais-Val du Thouet | 2 |
| Forêt de Viennay (3) ⚠️ | Viennay › Parthenay-Gâtine | 2 |
| Forêt de Viennay (4) ⚠️ | Viennay › Parthenay-Gâtine | 2 |
| Forêt de Saint-Aubin-le-Cloud ⚠️ | Saint-Aubin-le-Cloud › Parthenay-Gâtine | 2 |
| Forêt de Pougne-Hérisson (8) ⚠️ | Pougne-Hérisson › Parthenay-Gâtine | 2 |
| Forêt de Pougne-Hérisson (14) ⚠️ | Pougne-Hérisson › Parthenay-Gâtine | 2 |
| Forêt de Ménigoute (2) ⚠️ | Ménigoute › Parthenay-Gâtine | 2 |
| Bois de Nueil-les-Aubiers (20) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 2 |
| Bois de La Chapelle-Saint-Laurent ⚠️ | La Chapelle-Saint-Laurent › Bocage Bressuirais | 2 |
| Forêt de La Ferrière-en-Parthenay (5) ⚠️ | La Ferrière-en-Parthenay › Parthenay-Gâtine | 2 |
| Bois de Nueil-les-Aubiers (27) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 2 |
| Bois de Saint-Martin-du-Fouilloux (2) ⚠️ | Saint-Martin-du-Fouilloux › Parthenay-Gâtine | 2 |
| Forêt de Saint-Léger-de-Montbrun (9) ⚠️ | Saint-Léger-de-Montbrun › Thouarsais | 2 |
| Forêt de Vasles (14) ⚠️ | Vasles › Parthenay-Gâtine | 2 |
| Forêt de Saint-Généroux (2) ⚠️ | Saint-Généroux › Thouarsais | 2 |
| Forêt de Parthenay (2) ⚠️ | Parthenay › Parthenay-Gâtine | 2 |
| Le Bois des Touches ⚠️ | Fontivillié › Mellois en Poitou | 2 |
| Forêt de Glénay (8) ⚠️ | Glénay › Thouarsais | 2 |
| Forêt de Moncoutant-sur-Sèvre (7) ⚠️ | Moncoutant-sur-Sèvre › Bocage Bressuirais | 2 |
| Forêt de Beauvoir-sur-Niort (4) ⚠️ | Beauvoir-sur-Niort › Niortais | 2 |
| Bois de Fénery (3) ⚠️ | Fénery › Parthenay-Gâtine | 2 |
| Forêt de Louin (4) ⚠️ | Louin › Airvaudais-Val du Thouet | 2 |
| Forêt de Melle (9) ⚠️ | Melle › Mellois en Poitou | 2 |
| Forêt de Melle (13) ⚠️ | Melle › Mellois en Poitou | 2 |
| Bois de Saint-Aubin-du-Plain ⚠️ | Saint-Aubin-du-Plain › Bocage Bressuirais | 2 |
| Forêt de Melle (18) ⚠️ | Melle › Mellois en Poitou | 2 |
| Forêt de Coulonges-Thouarsais (2) ⚠️ | Coulonges-Thouarsais › Thouarsais | 2 |
| Forêt de Coulonges-Thouarsais (3) ⚠️ | Coulonges-Thouarsais › Thouarsais | 2 |
| Forêt de Saint-Germain-de-Longue-Chaume ⚠️ | Saint-Germain-de-Longue-Chaume › Parthenay-Gâtine | 2 |
| Forêt de Saint-Germain-de-Longue-Chaume (2) ⚠️ | Saint-Germain-de-Longue-Chaume › Parthenay-Gâtine | 2 |
| Forêt de La Ferrière-en-Parthenay (8) ⚠️ | La Ferrière-en-Parthenay › Parthenay-Gâtine | 2 |
| Bois de Argentonnay (5) ⚠️ | Argentonnay › Bocage Bressuirais | 2 |
| Bois de Coulonges-Thouarsais (3) ⚠️ | Coulonges-Thouarsais › Thouarsais | 2 |
| Bois de Argentonnay (18) ⚠️ | Argentonnay › Bocage Bressuirais | 2 |
| Bois de Argentonnay (19) ⚠️ | Argentonnay › Bocage Bressuirais | 2 |
| Forêt de Coulonges-Thouarsais (4) ⚠️ | Coulonges-Thouarsais › Thouarsais | 2 |
| Forêt de Irais (4) ⚠️ | Irais › Airvaudais-Val du Thouet | 2 |
| Forêt de Argentonnay (16) ⚠️ | Argentonnay › Bocage Bressuirais | 2 |
| Forêt de Secondigny (2) ⚠️ | Secondigny › Parthenay-Gâtine | 2 |
| Forêt de Thénezay (17) ⚠️ | Thénezay › Parthenay-Gâtine | 2 |
| Forêt de Thouars (15) ⚠️ | Thouars › Thouarsais | 2 |
| Forêt de Saint Maurice Étusson (7) ⚠️ | Saint Maurice Étusson › Bocage Bressuirais | 2 |
| Forêt de Niort (10) ⚠️ | Niort › Niortais | 2 |
| Forêt de Niort (16) ⚠️ | Niort › Niortais | 2 |
| Bois de Bressuire (21) ⚠️ | Bressuire › Bocage Bressuirais | 2 |
| Bois de Bressuire (23) ⚠️ | Bressuire › Bocage Bressuirais | 2 |
| Forêt de Plaine-d'Argenson (4) ⚠️ | Plaine-d'Argenson › Niortais | 2 |
| Forêt de Plaine-d'Argenson (7) ⚠️ | Plaine-d'Argenson › Niortais | 2 |
| Forêt de Airvault (31) ⚠️ | Airvault › Airvaudais-Val du Thouet | 2 |
| Bois de Bressuire (43) ⚠️ | Bressuire › Bocage Bressuirais | 2 |
| Forêt de Coulon (17) ⚠️ | Coulon › Niortais | 2 |
| Forêt de Coulon (19) ⚠️ | Coulon › Niortais | 2 |
| Forêt de Coulon (20) ⚠️ | Coulon › Niortais | 2 |
| Forêt de Coulon (22) ⚠️ | Coulon › Niortais | 2 |
| Bois de Cirières ⚠️ | Cirières › Bocage Bressuirais | 2 |
| Forêt de Magné (4) ⚠️ | Magné › Niortais | 2 |
| Bois de Bressuire (70) ⚠️ | Bressuire › Bocage Bressuirais | 2 |
| Forêt de Valdelaume (5) ⚠️ | Valdelaume › Mellois en Poitou | 2 |
| Forêt de Frontenay-Rohan-Rohan ⚠️ | Frontenay-Rohan-Rohan › Niortais | 2 |
| Forêt de Magné (27) ⚠️ | Magné › Niortais | 2 |
| Forêt de Magné (30) ⚠️ | Magné › Niortais | 2 |
| Forêt de Frontenay-Rohan-Rohan (2) ⚠️ | Magné › Niortais | 2 |
| Forêt de Lezay (5) ⚠️ | Lezay › Mellois en Poitou | 2 |
| Forêt de Sansais (10) ⚠️ | Sansais › Niortais | 2 |
| Forêt de Alloinay (10) ⚠️ | Alloinay › Mellois en Poitou | 2 |
| Forêt de Sansais (14) ⚠️ | Sansais › Niortais | 2 |
| Forêt de Celles-sur-Belle ⚠️ | Celles-sur-Belle › Mellois en Poitou | 2 |
| Forêt de Marcillé (4) ⚠️ | Marcillé › Mellois en Poitou | 2 |
| Forêt de Melle (19) ⚠️ | Melle › Mellois en Poitou | 2 |
| Forêt de Saint-Romans-lès-Melle (5) ⚠️ | Saint-Romans-lès-Melle › Mellois en Poitou | 2 |
| Forêt de Lezay (10) ⚠️ | Lezay › Mellois en Poitou | 2 |
| Forêt de Reffannes (2) ⚠️ | Reffannes › Parthenay-Gâtine | 2 |
| Forêt de Vouillé (2) ⚠️ | Vouillé › Niortais | 2 |
| Forêt du Vanneau-Irleau ⚠️ | Le Vanneau-Irleau › Niortais | 2 |
| Forêt de Sansais (26) ⚠️ | Sansais › Niortais | 2 |
| Forêt de Sansais (27) ⚠️ | Sansais › Niortais | 2 |
| Forêt de Brioux-sur-Boutonne (3) ⚠️ | Brioux-sur-Boutonne › Mellois en Poitou | 2 |
| Forêt de Celles-sur-Belle (11) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 2 |
| Bois de Scillé (4) ⚠️ | Scillé › Val de Gâtine | 2 |
| Forêt de Bressuire (10) ⚠️ | Bressuire › Bocage Bressuirais | 2 |
| Forêt de Bressuire (12) ⚠️ | Bressuire › Bocage Bressuirais | 2 |
| Bois de Bressuire (93) ⚠️ | Bressuire › Bocage Bressuirais | 2 |
| Forêt de Valdelaume (7) ⚠️ | Valdelaume › Mellois en Poitou | 2 |
| Forêt de Valdelaume (9) ⚠️ | Valdelaume › Mellois en Poitou | 2 |
| Forêt de Marcillé (15) ⚠️ | Marcillé › Mellois en Poitou | 2 |
| Forêt de Saint-Amand-sur-Sèvre ⚠️ | Saint-Amand-sur-Sèvre › Bocage Bressuirais | 2 |
| Forêt de Melle (33) ⚠️ | Melle › Mellois en Poitou | 2 |
| Forêt de Melle (38) ⚠️ | Melle › Mellois en Poitou | 2 |
| Forêt de Melle (46) ⚠️ | Melle › Mellois en Poitou | 2 |
| Forêt de Melle (53) ⚠️ | Melle › Mellois en Poitou | 2 |
| Forêt de Saint-Romans-lès-Melle (7) ⚠️ | Saint-Romans-lès-Melle › Mellois en Poitou | 2 |
| Forêt de Périgné (12) ⚠️ | Périgné › Mellois en Poitou | 2 |
| Forêt de Périgné (17) ⚠️ | Périgné › Mellois en Poitou | 2 |
| Forêt de Bressuire (16) ⚠️ | Bressuire › Bocage Bressuirais | 2 |
| Forêt de Celles-sur-Belle (23) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 2 |
| Forêt de Brûlain (2) ⚠️ | Brûlain › Niortais | 2 |
| Forêt de Périgné (23) ⚠️ | Périgné › Mellois en Poitou | 2 |
| Bois de Coulonges-Thouarsais (5) ⚠️ | Coulonges-Thouarsais › Thouarsais | 2 |
| Forêt de Beaussais-Vitré (9) ⚠️ | Beaussais-Vitré › Mellois en Poitou | 2 |
| Forêt de Beaussais-Vitré (15) ⚠️ | Beaussais-Vitré › Mellois en Poitou | 2 |
| Forêt de Prailles-la-Couarde (3) ⚠️ | Prailles-la-Couarde › Mellois en Poitou | 2 |
| Forêt de Prailles-la-Couarde (4) ⚠️ | Prailles-la-Couarde › Mellois en Poitou | 2 |
| Forêt de Beaussais-Vitré (25) ⚠️ | Beaussais-Vitré › Mellois en Poitou | 2 |
| Forêt de Beaussais-Vitré (26) ⚠️ | Beaussais-Vitré › Mellois en Poitou | 2 |
| Forêt de Beaussais-Vitré (29) ⚠️ | Beaussais-Vitré › Mellois en Poitou | 2 |
| Forêt de Beaussais-Vitré (32) ⚠️ | Beaussais-Vitré › Mellois en Poitou | 2 |
| Forêt de Prailles-la-Couarde (9) ⚠️ | Prailles-la-Couarde › Mellois en Poitou | 2 |
| Forêt de Louzy (5) ⚠️ | Louzy › Thouarsais | 2 |
| Parc de la Salle des Fêtes ⚠️ | Sainte-Ouenne › Val de Gâtine | 2 |
| Forêt de Saint-Pompain (2) ⚠️ | Saint-Pompain › Val de Gâtine | 2 |
| alluviale ⚠️ | Cirières › Bocage Bressuirais | 2 |
| Forêt de Secondigné-sur-Belle (4) ⚠️ | Secondigné-sur-Belle › Mellois en Poitou | 2 |
| Forêt de Prailles-la-Couarde (36) ⚠️ | Prailles-la-Couarde › Mellois en Poitou | 2 |
| Forêt de Vernoux-sur-Boutonne (3) ⚠️ | Vernoux-sur-Boutonne › Mellois en Poitou | 2 |
| Forêt de Vernoux-sur-Boutonne (5) ⚠️ | Vernoux-sur-Boutonne › Mellois en Poitou | 2 |
| Forêt de Vernoux-sur-Boutonne (8) ⚠️ | Vernoux-sur-Boutonne › Mellois en Poitou | 2 |
| Forêt de Vernoux-sur-Boutonne (14) ⚠️ | Vernoux-sur-Boutonne › Mellois en Poitou | 2 |
| Forêt de Augé (111) ⚠️ | Augé › Haut Val de Sèvre | 2 |
| Forêt de Souvigné (17) ⚠️ | Souvigné › Haut Val de Sèvre | 2 |
| Forêt de Sainte-Eanne ⚠️ | Sainte-Eanne › Haut Val de Sèvre | 2 |
| Forêt de Sainte-Eanne (2) ⚠️ | Sainte-Eanne › Haut Val de Sèvre | 2 |
| Forêt de Saint-Léger-de-Montbrun (19) ⚠️ | Saint-Léger-de-Montbrun › Thouarsais | 2 |
| Forêt de Sepvret (11) ⚠️ | Sepvret › Mellois en Poitou | 2 |
| Forêt de Exoudun (7) ⚠️ | Exoudun › Mellois en Poitou | 2 |
| Forêt de Sepvret (22) ⚠️ | Sepvret › Mellois en Poitou | 2 |
| Forêt de Saint-Paul-en-Gâtine (7) ⚠️ | Saint-Paul-en-Gâtine › Bocage Bressuirais | 2 |
| Forêt de La Mothe-Saint-Héray (6) ⚠️ | La Mothe-Saint-Héray › Mellois en Poitou | 2 |
| Forêt de La Mothe-Saint-Héray (11) ⚠️ | La Mothe-Saint-Héray › Mellois en Poitou | 2 |
| Forêt de La Mothe-Saint-Héray (19) ⚠️ | La Mothe-Saint-Héray › Mellois en Poitou | 2 |
| Forêt de La Mothe-Saint-Héray (22) ⚠️ | La Mothe-Saint-Héray › Mellois en Poitou | 2 |
| Forêt de La Mothe-Saint-Héray (24) ⚠️ | La Mothe-Saint-Héray › Mellois en Poitou | 2 |
| Forêt de Salles ⚠️ | Salles › Haut Val de Sèvre | 2 |
| Forêt de Sainte-Eanne (4) ⚠️ | Sainte-Eanne › Haut Val de Sèvre | 2 |
| Forêt de La Mothe-Saint-Héray (29) ⚠️ | La Mothe-Saint-Héray › Mellois en Poitou | 2 |
| Forêt de Sainte-Eanne (6) ⚠️ | Sainte-Eanne › Haut Val de Sèvre | 2 |
| Forêt de Sainte-Eanne (13) ⚠️ | Sainte-Eanne › Haut Val de Sèvre | 2 |
| Forêt de La Mothe-Saint-Héray (30) ⚠️ | Sainte-Eanne › Haut Val de Sèvre | 2 |
| Forêt de Sainte-Eanne (31) ⚠️ | Sainte-Eanne › Haut Val de Sèvre | 2 |
| Forêt de Nanteuil (3) ⚠️ | Nanteuil › Haut Val de Sèvre | 2 |
| Forêt de Nanteuil (5) ⚠️ | Nanteuil › Haut Val de Sèvre | 2 |
| Forêt de Saint-Martin-de-Saint-Maixent (27) ⚠️ | Saint-Martin-de-Saint-Maixent › Haut Val de Sèvre | 2 |
| Forêt de Nanteuil (17) ⚠️ | Nanteuil › Haut Val de Sèvre | 2 |
| Forêt de Marnes (22) ⚠️ | Marnes › Thouarsais | 2 |
| Forêt de Granzay-Gript (2) ⚠️ | Granzay-Gript › Niortais | 2 |
| Forêt de Cerizay ⚠️ | Cerizay › Bocage Bressuirais | 2 |
| Forêt du Busseau (9) ⚠️ | Le Busseau › Val de Gâtine | 2 |
| Forêt de Argentonnay (21) ⚠️ | Argentonnay › Bocage Bressuirais | 2 |
| Forêt de Pamproux (8) ⚠️ | Pamproux › Haut Val de Sèvre | 2 |
| Forêt de Clussais-la-Pommeraie (9) ⚠️ | Clussais-la-Pommeraie › Mellois en Poitou | 2 |
| Forêt de Plaine-d'Argenson (11) ⚠️ | Plaine-d'Argenson › Niortais | 2 |
| Forêt de Saint-Léger-de-Montbrun (24) ⚠️ | Saint-Léger-de-Montbrun › Thouarsais | 2 |
| Forêt de Couture-d'Argenson (3) ⚠️ | Couture-d'Argenson › Mellois en Poitou | 2 |
| Forêt de Couture-d'Argenson (4) ⚠️ | Couture-d'Argenson › Mellois en Poitou | 2 |
| Forêt de Nanteuil (18) ⚠️ | Nanteuil › Haut Val de Sèvre | 2 |
| Forêt de Limalonges (10) ⚠️ | Limalonges › Mellois en Poitou | 2 |
| Forêt de Limalonges (13) ⚠️ | Limalonges › Mellois en Poitou | 2 |
| Forêt de Sauzé-entre-Bois (15) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 2 |
| Le Bois des Taillées ⚠️ | Fenioux › Val de Gâtine | 2 |
| Forêt de Fenioux (14) ⚠️ | Fenioux › Val de Gâtine | 2 |
| Bois de Prin-Deyrançon ⚠️ | Prin-Deyrançon › Niortais | 2 |
| Forêt de Secondigny (4) ⚠️ | Secondigny › Parthenay-Gâtine | 2 |
| Forêt de Valdelaume (28) ⚠️ | Valdelaume › Mellois en Poitou | 2 |
| Forêt de Valdelaume (42) ⚠️ | Valdelaume › Mellois en Poitou | 2 |
| Forêt de Valdelaume (52) ⚠️ | Valdelaume › Mellois en Poitou | 2 |
| Forêt de Pamplie (6) ⚠️ | Pamplie › Val de Gâtine | 2 |
| Forêt de Lusseray (5) ⚠️ | Lusseray › Mellois en Poitou | 2 |
| Forêt de Fenioux (20) ⚠️ | Fenioux › Val de Gâtine | 2 |
| Forêt de Fenioux (21) ⚠️ | Fenioux › Val de Gâtine | 2 |
| Forêt de Asnières-en-Poitou (9) ⚠️ | Asnières-en-Poitou › Mellois en Poitou | 2 |
| Forêt de Fenioux (28) ⚠️ | Fenioux › Val de Gâtine | 2 |
| Forêt de Fenioux (29) ⚠️ | Fenioux › Val de Gâtine | 2 |
| Forêt de Fenioux (35) ⚠️ | Fenioux › Val de Gâtine | 2 |
| Forêt de Villemain (12) ⚠️ | Villemain › Mellois en Poitou | 2 |
| Forêt de Villemain (16) ⚠️ | Villemain › Mellois en Poitou | 2 |
| Forêt de Saint-Vincent-la-Châtre (4) ⚠️ | Saint-Vincent-la-Châtre › Mellois en Poitou | 2 |
| Forêt de Chef-Boutonne ⚠️ | Chef-Boutonne › Mellois en Poitou | 2 |
| Bois de Maisonnay (4) ⚠️ | Maisonnay › Mellois en Poitou | 2 |
| Bois de Maisonnay (5) ⚠️ | Maisonnay › Mellois en Poitou | 2 |
| Forêt des Châteliers (2) ⚠️ | Les Châteliers › Parthenay-Gâtine | 2 |
| Forêt de Ménigoute (6) ⚠️ | Ménigoute › Parthenay-Gâtine | 2 |
| Forêt de Saint-Vincent-la-Châtre (10) ⚠️ | Saint-Vincent-la-Châtre › Mellois en Poitou | 2 |
| Forêt de Saint-Vincent-la-Châtre (12) ⚠️ | Saint-Vincent-la-Châtre › Mellois en Poitou | 2 |
| Forêt de Saint-Vincent-la-Châtre (15) ⚠️ | Saint-Vincent-la-Châtre › Mellois en Poitou | 2 |
| Forêt de Saint-Coutant (7) ⚠️ | Saint-Coutant › Mellois en Poitou | 2 |
| Forêt de Saint-Coutant (14) ⚠️ | Saint-Coutant › Mellois en Poitou | 2 |
| Forêt de Sainte-Soline (5) ⚠️ | Sainte-Soline › Mellois en Poitou | 2 |
| Forêt de Sainte-Soline (15) ⚠️ | Sainte-Soline › Mellois en Poitou | 2 |
| Forêt de Saint-Hilaire-la-Palud (9) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 2 |
| Forêt de Saint-Hilaire-la-Palud (13) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 2 |
| Forêt de Saint-Hilaire-la-Palud (15) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 2 |
| Forêt de Arçais (2) ⚠️ | Arçais › Niortais | 2 |
| Forêt de Arçais (4) ⚠️ | Arçais › Niortais | 2 |
| Forêt de Luché-sur-Brioux ⚠️ | Luché-sur-Brioux › Mellois en Poitou | 2 |
| Forêt de Échiré (5) ⚠️ | Échiré › Niortais | 2 |
| Parc de Thouars ⚠️ | Thouars › Thouarsais | 2 |
| Forêt de Fontivillié (12) ⚠️ | Fontivillié › Mellois en Poitou | 2 |
| Forêt de Fontivillié (13) ⚠️ | Fontivillié › Mellois en Poitou | 2 |
| Forêt de Villefollet (17) ⚠️ | Villefollet › Mellois en Poitou | 2 |
| Forêt de Périgné (31) ⚠️ | Périgné › Mellois en Poitou | 2 |
| Bois de Plaine-et-Vallées (12) ⚠️ | Plaine-et-Vallées › Thouarsais | 2 |
| Forêt de Argentonnay (25) ⚠️ | Argentonnay › Bocage Bressuirais | 2 |
| Bois de Lavault (2) ⚠️ | Vançais › Mellois en Poitou | 2 |
| Bois de Champdeniers ⚠️ | Champdeniers › Val de Gâtine | 2 |
| Forêt de Saint-Paul-en-Gâtine (11) ⚠️ | Saint-Paul-en-Gâtine › Bocage Bressuirais | 2 |
| Forêt de Mauléon (8) ⚠️ | Mauléon › Bocage Bressuirais | 2 |
| La Gaillarderie ⚠️ | Courlay › Bocage Bressuirais | 2 |
| Forêt de Fomperron (7) ⚠️ | Fomperron › Parthenay-Gâtine | 2 |
| Forêt de Mauléon (12) ⚠️ | Mauléon › Bocage Bressuirais | 2 |
| Bois de Rom (3) ⚠️ | Rom › Mellois en Poitou | 2 |
| Forêt de Assais-les-Jumeaux (13) ⚠️ | Assais-les-Jumeaux › Airvaudais-Val du Thouet | 2 |
| Forêt de Assais-les-Jumeaux (19) ⚠️ | Assais-les-Jumeaux › Airvaudais-Val du Thouet | 2 |
| Forêt de Saint-Loup-Lamairé (22) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 2 |
| Bois de Nueil-les-Aubiers (31) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 2 |
| Bois de Nueil-les-Aubiers (32) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 2 |
| Bois de Nueil-les-Aubiers (33) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 2 |
| Bois de Bretignolles (5) ⚠️ | Bretignolles › Bocage Bressuirais | 2 |
| Forêt de Availles-Thouarsais (5) ⚠️ | Availles-Thouarsais › Airvaudais-Val du Thouet | 2 |
| Forêt de Airvault (55) ⚠️ | Airvault › Airvaudais-Val du Thouet | 2 |
| Bois de Bressuire (136) ⚠️ | Bressuire › Bocage Bressuirais | 2 |
| Bois de Chiché (2) ⚠️ | Chiché › Bocage Bressuirais | 2 |
| Bois de Faye-l'Abbesse ⚠️ | Faye-l'Abbesse › Bocage Bressuirais | 2 |
| Bois de Chiché (5) ⚠️ | Chiché › Bocage Bressuirais | 2 |
| Forêt de Pressigny (3) ⚠️ | Pressigny › Parthenay-Gâtine | 2 |
| Forêt de Thénezay (40) ⚠️ | Thénezay › Parthenay-Gâtine | 2 |
| Forêt de Thénezay (44) ⚠️ | Thénezay › Parthenay-Gâtine | 2 |
| Forêt de Louin (8) ⚠️ | Louin › Airvaudais-Val du Thouet | 2 |
| Forêt de Saint-Loup-Lamairé (33) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 2 |
| Forêt de Lhoumois (4) ⚠️ | Lhoumois › Parthenay-Gâtine | 2 |
| Forêt de Airvault (58) ⚠️ | Airvault › Airvaudais-Val du Thouet | 2 |
| Forêt de Airvault (72) ⚠️ | Airvault › Airvaudais-Val du Thouet | 2 |
| Forêt de Faye-sur-Ardin (2) ⚠️ | Faye-sur-Ardin › Val de Gâtine | 2 |
| Bois de Rom (5) ⚠️ | Rom › Mellois en Poitou | 2 |
| bois de Chebriton ⚠️ | Rom › Mellois en Poitou | 2 |
| Bois de Rom (8) ⚠️ | Rom › Mellois en Poitou | 2 |
| Bois de Rom (15) ⚠️ | Rom › Mellois en Poitou | 2 |
| Forêt de Sauzé-entre-Bois (35) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 2 |
| Forêt de Limalonges (54) ⚠️ | Limalonges › Mellois en Poitou | 2 |
| Forêt de La Ferrière-en-Parthenay (16) ⚠️ | La Ferrière-en-Parthenay › Parthenay-Gâtine | 2 |
| Forêt de Ardin (2) ⚠️ | Ardin › Val de Gâtine | 2 |
| Forêt de Saint-Loup-Lamairé (36) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 2 |
| Forêt de Mauléon (16) ⚠️ | Mauléon › Bocage Bressuirais | 2 |
| Forêt de La Chapelle-Bertrand (2) ⚠️ | La Chapelle-Bertrand › Parthenay-Gâtine | 2 |
| Forêt de La Chapelle-Bertrand (6) ⚠️ | La Chapelle-Bertrand › Parthenay-Gâtine | 2 |
| Forêt de Parthenay (3) ⚠️ | Parthenay › Parthenay-Gâtine | 2 |
| Forêt de Gourgé (10) ⚠️ | Gourgé › Parthenay-Gâtine | 2 |
| Forêt de Saivres (10) ⚠️ | Saivres › Haut Val de Sèvre | 2 |
| Forêt de Saivres (17) ⚠️ | Saivres › Haut Val de Sèvre | 2 |
| Forêt de Azay-le-Brûlé (11) ⚠️ | Azay-le-Brûlé › Haut Val de Sèvre | 2 |
| Forêt de Azay-le-Brûlé (20) ⚠️ | Azay-le-Brûlé › Haut Val de Sèvre | 2 |
| Forêt de Saivres (23) ⚠️ | Saivres › Haut Val de Sèvre | 2 |
| Forêt de Saivres (25) ⚠️ | Saivres › Haut Val de Sèvre | 2 |
| Forêt de Saurais (2) ⚠️ | Saurais › Parthenay-Gâtine | 2 |
| Forêt de La Ferrière-en-Parthenay (18) ⚠️ | La Ferrière-en-Parthenay › Parthenay-Gâtine | 2 |
| Forêt du Vanneau-Irleau (4) ⚠️ | Le Vanneau-Irleau › Niortais | 2 |
| Forêt de Gourgé (18) ⚠️ | Gourgé › Parthenay-Gâtine | 2 |
| Forêt de Lhoumois (9) ⚠️ | Lhoumois › Parthenay-Gâtine | 2 |
| Forêt de Gourgé (20) ⚠️ | Gourgé › Parthenay-Gâtine | 2 |
| Forêt de Gourgé (24) ⚠️ | Gourgé › Parthenay-Gâtine | 2 |
| Forêt de Gourgé (27) ⚠️ | Gourgé › Parthenay-Gâtine | 2 |
| Forêt de Gourgé (29) ⚠️ | Gourgé › Parthenay-Gâtine | 2 |
| Jardin des Abiès ⚠️ | L'Absie › Bocage Bressuirais | 2 |
| Forêt de Vernoux-en-Gâtine (9) ⚠️ | Vernoux-en-Gâtine › Parthenay-Gâtine | 2 |
| Forêt de Vernoux-en-Gâtine (15) ⚠️ | Vernoux-en-Gâtine › Parthenay-Gâtine | 2 |
| Forêt de Moncoutant-sur-Sèvre (9) ⚠️ | Moncoutant-sur-Sèvre › Bocage Bressuirais | 2 |
| Forêt de Cerizay (5) ⚠️ | Cerizay › Bocage Bressuirais | 2 |
| Forêt de Marnes (25) ⚠️ | Marnes › Thouarsais | 2 |
| Bois de Val-du-Mignon (4) ⚠️ | Val-du-Mignon › Niortais | 2 |
| Forêt de Saint-Loup-Lamairé (45) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 2 |
| Forêt de Gourgé (30) ⚠️ | Gourgé › Parthenay-Gâtine | 2 |
| Forêt de Saint-Martin-du-Fouilloux (7) ⚠️ | Saint-Martin-du-Fouilloux › Parthenay-Gâtine | 2 |
| Forêt de Vasles (31) ⚠️ | Vasles › Parthenay-Gâtine | 2 |
| Forêt de Glénay (11) ⚠️ | Glénay › Thouarsais | 2 |
| Forêt de Lageon (2) ⚠️ | Lageon › Parthenay-Gâtine | 2 |
| Forêt de Maisontiers (6) ⚠️ | Maisontiers › Airvaudais-Val du Thouet | 2 |
| Forêt de Louin (10) ⚠️ | Louin › Airvaudais-Val du Thouet | 2 |
| Forêt de Bessines (5) ⚠️ | Bessines › Niortais | 2 |
| Forêt de Saint-Martin-de-Mâcon (7) ⚠️ | Saint-Martin-de-Mâcon › Thouarsais | 2 |
| Forêt de Arçais (13) ⚠️ | Arçais › Niortais | 2 |
| Forêt du Vanneau-Irleau (20) ⚠️ | Le Vanneau-Irleau › Niortais | 2 |
| Forêt de Coulon (33) ⚠️ | Coulon › Niortais | 2 |
| Forêt de Coulon (34) ⚠️ | Coulon › Niortais | 2 |
| Forêt de Arçais (16) ⚠️ | Arçais › Niortais | 2 |
| Forêt de Airvault (97) ⚠️ | Airvault › Airvaudais-Val du Thouet | 2 |
| Bois de Nueil-les-Aubiers (35) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 2 |
| Forêt de Rom (11) ⚠️ | Rom › Mellois en Poitou | 2 |
| Forêt de Niort (109) ⚠️ | Niort › Niortais | 2 |
| Forêt de Coulonges-Thouarsais (5) ⚠️ | Coulonges-Thouarsais › Thouarsais | 2 |
| Forêt de Beauvoir-sur-Niort (7) ⚠️ | Beauvoir-sur-Niort › Niortais | 2 |
| Forêt de Arçais (17) ⚠️ | Arçais › Niortais | 2 |
| Forêt de Arçais (24) ⚠️ | Arçais › Niortais | 2 |
| Forêt de Saint-Hilaire-la-Palud (54) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 2 |
| Forêt de Alloinay (21) ⚠️ | Alloinay › Mellois en Poitou | 2 |
| Forêt de Alloinay (25) ⚠️ | Alloinay › Mellois en Poitou | 2 |
| Forêt de Alloinay (26) ⚠️ | Alloinay › Mellois en Poitou | 2 |
| Parc de Bressuire (24) ⚠️ | Bressuire › Bocage Bressuirais | 2 |
| Forêt de Saint-Pompain (4) ⚠️ | Saint-Pompain › Val de Gâtine | 2 |
| Forêt du Busseau (10) ⚠️ | Le Busseau › Val de Gâtine | 2 |
| Forêt de Mairé-Levescault (15) ⚠️ | Mairé-Levescault › Mellois en Poitou | 2 |
| Bois de Mairé-Levescault (2) ⚠️ | Mairé-Levescault › Mellois en Poitou | 2 |
| Forêt de Chizé (8) ⚠️ | Chizé › Mellois en Poitou | 2 |
| Forêt de Sainte-Ouenne (2) ⚠️ | Sainte-Ouenne › Val de Gâtine | 2 |
| Forêt de Saint-Martin-de-Sanzay (28) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 2 |
| Forêt de Saint-Martin-de-Sanzay (29) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 2 |
| Forêt de Sainte-Ouenne (10) ⚠️ | Sainte-Ouenne › Val de Gâtine | 2 |
| Forêt de Sainte-Ouenne (12) ⚠️ | Sainte-Ouenne › Val de Gâtine | 2 |
| Forêt de Béceleuf (3) ⚠️ | Béceleuf › Val de Gâtine | 2 |
| Forêt de Échiré (13) ⚠️ | Échiré › Niortais | 2 |
| Forêt du Bourdet (2) ⚠️ | Le Bourdet › Niortais | 2 |
| Forêt de Prailles-la-Couarde (43) ⚠️ | Prailles-la-Couarde › Mellois en Poitou | 2 |
| Forêt de Melle (90) ⚠️ | Melle › Mellois en Poitou | 2 |
| Forêt de Saint-Symphorien (29) ⚠️ | Saint-Symphorien › Niortais | 2 |
| Forêt de Glénay (15) ⚠️ | Glénay › Thouarsais | 2 |
| Bois de Louzy (11) ⚠️ | Louzy › Thouarsais | 2 |
| Forêt de Louzy (10) ⚠️ | Louzy › Thouarsais | 2 |
| Forêt de Sauzé-entre-Bois (50) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 2 |
| Bois de Louzy (18) ⚠️ | Louzy › Thouarsais | 2 |
| Forêt de Vançais (2) ⚠️ | Vançais › Mellois en Poitou | 2 |
| Forêt de Louzy (14) ⚠️ | Louzy › Thouarsais | 2 |
| Forêt de Sainte-Ouenne (23) ⚠️ | Sainte-Ouenne › Val de Gâtine | 2 |
| Forêt de Surin (7) ⚠️ | Surin › Val de Gâtine | 2 |
| Forêt de Saint-Martin-de-Sanzay (34) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 2 |
| Bois de Loretz-d'Argenton (11) ⚠️ | Loretz-d'Argenton › Thouarsais | 2 |
| Forêt de Saint-Martin-de-Sanzay (36) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 2 |
| Forêt de Saint-Martin-de-Sanzay (39) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 2 |
| Bois de Saint-Martin-de-Sanzay (29) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 2 |
| Bois de Tourtenay ⚠️ | Tourtenay › Thouarsais | 2 |
| Bois de Saint-Cyr-la-Lande (38) ⚠️ | Saint-Cyr-la-Lande › Thouarsais | 2 |
| Forêt de Thouars (23) ⚠️ | Thouars › Thouarsais | 2 |
| Forêt de Coulonges-Thouarsais (11) ⚠️ | Coulonges-Thouarsais › Thouarsais | 2 |
| Forêt de Thouars (27) ⚠️ | Thouars › Thouarsais | 2 |
| Bois de Thouars (10) ⚠️ | Thouars › Thouarsais | 2 |
| Forêt de Luché-Thouarsais (6) ⚠️ | Luché-Thouarsais › Thouarsais | 2 |
| Bois de Thouars (16) ⚠️ | Thouars › Thouarsais | 2 |
| Bois de Saint-Jean-de-Thouars (4) ⚠️ | Saint-Jean-de-Thouars › Thouarsais | 2 |
| Forêt de Thouars (37) ⚠️ | Thouars › Thouarsais | 2 |
| Forêt de Saint-Jacques-de-Thouars (4) ⚠️ | Saint-Jacques-de-Thouars › Thouarsais | 2 |
| Forêt de Luché-Thouarsais (8) ⚠️ | Luché-Thouarsais › Thouarsais | 2 |
| Forêt de Luzay (22) ⚠️ | Luzay › Thouarsais | 2 |
| Bois de Luzay (13) ⚠️ | Luzay › Thouarsais | 2 |
| Forêt de Plaine-et-Vallées (49) ⚠️ | Plaine-et-Vallées › Thouarsais | 2 |
| Bois de Thouars (31) ⚠️ | Thouars › Thouarsais | 2 |
| Bois de Saint-Jean-de-Thouars (5) ⚠️ | Saint-Jean-de-Thouars › Thouarsais | 2 |
| Bois de Plaine-et-Vallées (22) ⚠️ | Plaine-et-Vallées › Thouarsais | 2 |
| Forêt de Saint-Généroux (9) ⚠️ | Saint-Généroux › Thouarsais | 2 |
| Forêt de Pas-de-Jeu (8) ⚠️ | Pas-de-Jeu › Thouarsais | 2 |
| Forêt de Irais (9) ⚠️ | Irais › Airvaudais-Val du Thouet | 2 |
| Forêt de Plaine-et-Vallées (64) ⚠️ | Plaine-et-Vallées › Thouarsais | 2 |
| Bois de Plaine-et-Vallées (47) ⚠️ | Plaine-et-Vallées › Thouarsais | 2 |
| Forêt de Saint-Martin-de-Mâcon (14) ⚠️ | Saint-Martin-de-Mâcon › Thouarsais | 2 |
| Forêt de Thouars (57) ⚠️ | Thouars › Thouarsais | 2 |
| Bois de Val en Vignes (7) ⚠️ | Val en Vignes › Thouarsais | 2 |
| Bois de Thouars (48) ⚠️ | Thouars › Thouarsais | 2 |
| Bois de Val en Vignes (32) ⚠️ | Val en Vignes › Thouarsais | 2 |
| Bois de Argentonnay (52) ⚠️ | Argentonnay › Bocage Bressuirais | 2 |
| Bois de Val en Vignes (38) ⚠️ | Val en Vignes › Thouarsais | 2 |
| Forêt de Val en Vignes (27) ⚠️ | Val en Vignes › Thouarsais | 2 |
| Forêt de Val en Vignes (30) ⚠️ | Val en Vignes › Thouarsais | 2 |
| Forêt de Val en Vignes (31) ⚠️ | Val en Vignes › Thouarsais | 2 |
| Forêt de Argentonnay (29) ⚠️ | Argentonnay › Bocage Bressuirais | 2 |
| Bois de Thouars (49) ⚠️ | Thouars › Thouarsais | 2 |
| Bois de Loretz-d'Argenton (18) ⚠️ | Loretz-d'Argenton › Thouarsais | 2 |
| Forêt de Val en Vignes (43) ⚠️ | Val en Vignes › Thouarsais | 2 |
| Bois de Val en Vignes (52) ⚠️ | Val en Vignes › Thouarsais | 2 |
| Forêt de Val en Vignes (44) ⚠️ | Val en Vignes › Thouarsais | 2 |
| Forêt de Val en Vignes (46) ⚠️ | Val en Vignes › Thouarsais | 2 |
| Forêt de Loretz-d'Argenton (29) ⚠️ | Loretz-d'Argenton › Thouarsais | 2 |
| Forêt de Genneton (4) ⚠️ | Genneton › Bocage Bressuirais | 2 |
| Bois de Saint Maurice Étusson (3) ⚠️ | Saint Maurice Étusson › Bocage Bressuirais | 2 |
| Bois de Saint Maurice Étusson (7) ⚠️ | Saint Maurice Étusson › Bocage Bressuirais | 2 |
| Forêt de Loretz-d'Argenton (35) ⚠️ | Loretz-d'Argenton › Thouarsais | 2 |
| Bois de Argentonnay (57) ⚠️ | Argentonnay › Bocage Bressuirais | 2 |
| Forêt de Argentonnay (30) ⚠️ | Argentonnay › Bocage Bressuirais | 2 |
| Bois de Argentonnay (58) ⚠️ | Argentonnay › Bocage Bressuirais | 2 |
| Bois de Argentonnay (65) ⚠️ | Argentonnay › Bocage Bressuirais | 2 |
| Bois de Saint-Aubin-du-Plain (6) ⚠️ | Saint-Aubin-du-Plain › Bocage Bressuirais | 2 |
| Bois de Nueil-les-Aubiers (39) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 2 |
| Bois de Nueil-les-Aubiers (41) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 2 |
| Bois de Voulmentin (25) ⚠️ | Voulmentin › Bocage Bressuirais | 2 |
| Bois de Voulmentin (26) ⚠️ | Voulmentin › Bocage Bressuirais | 2 |
| Bois de Argentonnay (85) ⚠️ | Argentonnay › Bocage Bressuirais | 2 |
| Bois de Saint-Aubin-du-Plain (12) ⚠️ | Saint-Aubin-du-Plain › Bocage Bressuirais | 2 |
| Bois de Bressuire (160) ⚠️ | Bressuire › Bocage Bressuirais | 2 |
| Bois de Nueil-les-Aubiers (45) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 2 |
| Bois de Nueil-les-Aubiers (54) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 2 |
| Bois de Vernoux-en-Gâtine (6) ⚠️ | Scillé › Val de Gâtine | 2 |
| Bois de Bressuire (165) ⚠️ | Bressuire › Bocage Bressuirais | 2 |
| Bois du Pin (8) ⚠️ | Le Pin › Bocage Bressuirais | 2 |
| Bois de Saint-Pierre-des-Échaubrognes (6) ⚠️ | Mauléon › Bocage Bressuirais | 2 |
| Bois de Mauléon (36) ⚠️ | Mauléon › Bocage Bressuirais | 2 |
| Bois de Argentonnay (87) ⚠️ | Argentonnay › Bocage Bressuirais | 2 |
| Bois de Argentonnay (88) ⚠️ | Argentonnay › Bocage Bressuirais | 2 |
| Bois de Moncoutant-sur-Sèvre (11) ⚠️ | Moncoutant-sur-Sèvre › Bocage Bressuirais | 2 |
| Bois de Moncoutant-sur-Sèvre (13) ⚠️ | Moncoutant-sur-Sèvre › Bocage Bressuirais | 2 |
| Bois de La Petite-Boissière ⚠️ | La Petite-Boissière › Bocage Bressuirais | 2 |
| Bois de La Petite-Boissière (5) ⚠️ | La Petite-Boissière › Bocage Bressuirais | 2 |
| Bois de La Petite-Boissière (6) ⚠️ | La Petite-Boissière › Bocage Bressuirais | 2 |
| Bois de Montravers (13) ⚠️ | Montravers › Bocage Bressuirais | 2 |
| Bois de Montravers (17) ⚠️ | Montravers › Bocage Bressuirais | 2 |
| Bois du Pin (19) ⚠️ | Le Pin › Bocage Bressuirais | 2 |
| Bois de Combrand (42) ⚠️ | Combrand › Bocage Bressuirais | 2 |
| Bois du Pin (25) ⚠️ | Le Pin › Bocage Bressuirais | 2 |
| Forêt de Saint-Maxire (2) ⚠️ | Saint-Maxire › Niortais | 2 |
| Forêt de Germond-Rouvre (9) ⚠️ | Germond-Rouvre › Niortais | 2 |
| Forêt de Champdeniers (4) ⚠️ | Champdeniers › Val de Gâtine | 2 |
| Forêt de Xaintray (3) ⚠️ | Xaintray › Val de Gâtine | 2 |
| Bois de Cerizay (5) ⚠️ | Cerizay › Bocage Bressuirais | 2 |
| Forêt de Plaine-d'Argenson (28) ⚠️ | Plaine-d'Argenson › Niortais | 2 |
| Forêt de Aubigné (7) ⚠️ | Aubigné › Mellois en Poitou | 2 |
| Forêt de Aubigné (10) ⚠️ | Aubigné › Mellois en Poitou | 2 |
| Bois de La Petite-Boissière (23) ⚠️ | La Petite-Boissière › Bocage Bressuirais | 2 |
| Forêt de Azay-sur-Thouet (9) ⚠️ | Azay-sur-Thouet › Parthenay-Gâtine | 2 |
| Bois de Mauléon (54) ⚠️ | Mauléon › Bocage Bressuirais | 2 |
| Bois de Saint-Pierre-des-Échaubrognes (7) ⚠️ | Saint-Pierre-des-Échaubrognes › Bocage Bressuirais | 2 |
| Forêt de Mauléon (21) ⚠️ | Mauléon › Bocage Bressuirais | 2 |
| Bois de Saint-Pierre-des-Échaubrognes (23) ⚠️ | Saint-Pierre-des-Échaubrognes › Bocage Bressuirais | 2 |
| Bois de Saint-Pierre-des-Échaubrognes (24) ⚠️ | Saint-Pierre-des-Échaubrognes › Bocage Bressuirais | 2 |
| Bois de Saint-Pierre-des-Échaubrognes (25) ⚠️ | Saint-Pierre-des-Échaubrognes › Bocage Bressuirais | 2 |
| Bois de Mauléon (88) ⚠️ | Mauléon › Bocage Bressuirais | 2 |
| Bois de Mauléon (105) ⚠️ | Mauléon › Bocage Bressuirais | 2 |
| Bois de Mauléon (114) ⚠️ | Mauléon › Bocage Bressuirais | 2 |
| Bois de Mauléon (117) ⚠️ | Mauléon › Bocage Bressuirais | 2 |
| Bois de Mauléon (119) ⚠️ | Mauléon › Bocage Bressuirais | 2 |
| Bois de Mauléon (124) ⚠️ | Mauléon › Bocage Bressuirais | 2 |
| Forêt de Sauzé-entre-Bois (68) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 2 |
| Forêt de Sauzé-entre-Bois (74) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 2 |
| Forêt de Limalonges (71) ⚠️ | Limalonges › Mellois en Poitou | 2 |
| Forêt de Lorigné (5) ⚠️ | Lorigné › Mellois en Poitou | 2 |
| Forêt de Lorigné (6) ⚠️ | Lorigné › Mellois en Poitou | 2 |
| Forêt de Clavé (3) ⚠️ | Clavé › Val de Gâtine | 2 |
| Forêt de Rom (50) ⚠️ | Rom › Mellois en Poitou | 2 |
| Forêt de Rom (56) ⚠️ | Rom › Mellois en Poitou | 2 |
| Forêt de Rom (58) ⚠️ | Rom › Mellois en Poitou | 2 |
| Forêt de Saivres (26) ⚠️ | Saivres › Haut Val de Sèvre | 2 |
| Bois de Saint-Martin-de-Saint-Maixent (2) ⚠️ | Saint-Martin-de-Saint-Maixent › Haut Val de Sèvre | 2 |
| Forêt de Lageon (3) ⚠️ | Lageon › Parthenay-Gâtine | 2 |
| Parc de La Chapelle-Saint-Laurent ⚠️ | La Chapelle-Saint-Laurent › Bocage Bressuirais | 2 |
| Forêt de Pamproux (19) ⚠️ | Pamproux › Haut Val de Sèvre | 2 |
| Bois de Scillé (7) ⚠️ | Scillé › Val de Gâtine | 2 |
| Bois de Vernoux-en-Gâtine (8) ⚠️ | Vernoux-en-Gâtine › Parthenay-Gâtine | 2 |
| Bois de Ardin (9) ⚠️ | Ardin › Val de Gâtine | 2 |
| Bois de Beugnon-Thireuil (4) ⚠️ | Beugnon-Thireuil › Val de Gâtine | 2 |
| Bois de Faye-sur-Ardin (5) ⚠️ | Faye-sur-Ardin › Val de Gâtine | 2 |
| Forêt de Celles-sur-Belle (31) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 2 |
| Bois de Maisonnay (7) ⚠️ | Maisonnay › Mellois en Poitou | 2 |
| Forêt de Sainte-Soline (22) ⚠️ | Sainte-Soline › Mellois en Poitou | 2 |
| Forêt de Brieuil-sur-Chizé (6) ⚠️ | Brieuil-sur-Chizé › Mellois en Poitou | 2 |
| Forêt de Aiffres (45) ⚠️ | Fors › Niortais | 2 |
| Forêt de Aiffres (46) ⚠️ | Aiffres › Niortais | 2 |
| Forêt de Aiffres (53) ⚠️ | Aiffres › Niortais | 2 |
| Forêt de Aiffres (59) ⚠️ | Aiffres › Niortais | 2 |
| Bois de la Cure ⚠️ | Aiffres › Niortais | 2 |
| Forêt de Saint-Symphorien (38) ⚠️ | Saint-Symphorien › Niortais | 2 |
| Bois de Secondigny (4) ⚠️ | Secondigny › Parthenay-Gâtine | 2 |
| Forêt de Villefollet (22) ⚠️ | Villefollet › Mellois en Poitou | 2 |
| Forêt de Saint-Symphorien (45) ⚠️ | Saint-Symphorien › Niortais | 2 |
| Bois de Niort (48) ⚠️ | Niort › Niortais | 2 |
| Forêt de Saint-Martin-de-Bernegoue (6) ⚠️ | Saint-Martin-de-Bernegoue › Niortais | 2 |
| Forêt de Saint-Martin-de-Bernegoue (7) ⚠️ | Saint-Martin-de-Bernegoue › Niortais | 2 |
| Forêt de Saint-Martin-de-Bernegoue (12) ⚠️ | Saint-Martin-de-Bernegoue › Niortais | 2 |
| Forêt de Prahecq (44) ⚠️ | Prahecq › Niortais | 2 |
| Forêt de Prahecq (51) ⚠️ | Prahecq › Niortais | 2 |
| Forêt de Marigny (14) ⚠️ | Fors › Niortais | 2 |
| Forêt de Granzay-Gript (11) ⚠️ | Granzay-Gript › Niortais | 2 |
| Bois de Prahecq (19) ⚠️ | Prahecq › Niortais | 2 |
| Forêt de Granzay-Gript (30) ⚠️ | Granzay-Gript › Niortais | 2 |
| Forêt de Mauléon (24) ⚠️ | Mauléon › Bocage Bressuirais | 2 |
| Bois de La Crèche (16) ⚠️ | La Crèche › Haut Val de Sèvre | 2 |
| Bois de Saint-Symphorien (5) ⚠️ | Saint-Symphorien › Niortais | 2 |
| Forêt de Aiffres (101) ⚠️ | Fors › Niortais | 2 |
| Forêt de Chauray (4) ⚠️ | Chauray › Niortais | 2 |
| Forêt de Chauray (7) ⚠️ | Chauray › Niortais | 2 |
| Bois de François (4) ⚠️ | François › Haut Val de Sèvre | 2 |
| Bois de François (5) ⚠️ | François › Haut Val de Sèvre | 2 |
| Bois de Aigondigné (53) ⚠️ | Aigondigné › Mellois en Poitou | 2 |
| Bois de Aigondigné (88) ⚠️ | Aigondigné › Mellois en Poitou | 2 |
| Forêt de Celles-sur-Belle (32) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 2 |
| Forêt de Celles-sur-Belle (34) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 2 |
| Bois de Celles-sur-Belle (37) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 2 |
| Forêt de Argentonnay (37) ⚠️ | Argentonnay › Bocage Bressuirais | 2 |
| Bois de Nueil-les-Aubiers (116) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 2 |
| Forêt des Fosses (9) ⚠️ | Les Fosses › Mellois en Poitou | 2 |
| Forêt de Brûlain (21) ⚠️ | Brûlain › Niortais | 2 |
| Bois de Bressuire (170) ⚠️ | Bressuire › Bocage Bressuirais | 2 |
| Bois de Nueil-les-Aubiers (119) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 2 |
| Bois de Voulmentin (33) ⚠️ | Voulmentin › Bocage Bressuirais | 2 |
| Bois de Mauléon (151) ⚠️ | Mauléon › Bocage Bressuirais | 2 |
| Bois de Villiers-en-Plaine (10) ⚠️ | Villiers-en-Plaine › Niortais | 2 |
| Bois de Cirières (33) ⚠️ | Cirières › Bocage Bressuirais | 2 |
| Bois de Saint-Amand-sur-Sèvre (29) ⚠️ | Saint-Amand-sur-Sèvre › Bocage Bressuirais | 2 |
| Bois de Saint-Amand-sur-Sèvre (30) ⚠️ | Saint-Amand-sur-Sèvre › Bocage Bressuirais | 2 |
| Bois de Mauléon (159) ⚠️ | Mauléon › Bocage Bressuirais | 2 |
| Bois de Mauléon (163) ⚠️ | Mauléon › Bocage Bressuirais | 2 |
| Bois de Mauléon (166) ⚠️ | Mauléon › Bocage Bressuirais | 2 |
| Forêt de Granzay-Gript (82) ⚠️ | Granzay-Gript › Niortais | 2 |
| Forêt de Loretz-d'Argenton ⚠️ | Loretz-d'Argenton › Thouarsais | 1 |
| Bois de Loretz-d'Argenton ⚠️ | Loretz-d'Argenton › Thouarsais | 1 |
| Forêt de Rom ⚠️ | Rom › Mellois en Poitou | 1 |
| Forêt de Alloinay (2) ⚠️ | Alloinay › Mellois en Poitou | 1 |
| Forêt de Valdelaume (2) ⚠️ | Valdelaume › Mellois en Poitou | 1 |
| Forêt de Couture-d'Argenson ⚠️ | Couture-d'Argenson › Mellois en Poitou | 1 |
| Parc de Parthenay ⚠️ | Parthenay › Parthenay-Gâtine | 1 |
| Parc des Loges ⚠️ | Parthenay › Parthenay-Gâtine | 1 |
| Parc de Parthenay (2) ⚠️ | Parthenay › Parthenay-Gâtine | 1 |
| Parc de Niort (2) ⚠️ | Niort › Niortais | 1 |
| Bois de Niort ⚠️ | Niort › Niortais | 1 |
| Bois de Niort (4) ⚠️ | Niort › Niortais | 1 |
| Forêt de Couture-d'Argenson (2) ⚠️ | Couture-d'Argenson › Mellois en Poitou | 1 |
| Forêt de Asnières-en-Poitou (4) ⚠️ | Asnières-en-Poitou › Mellois en Poitou | 1 |
| Forêt de Villemain (5) ⚠️ | Villemain › Mellois en Poitou | 1 |
| Bois de Niort (5) ⚠️ | Niort › Niortais | 1 |
| Bois de Doux ⚠️ | Doux › Parthenay-Gâtine | 1 |
| Forêt de La Crèche (3) ⚠️ | La Crèche › Haut Val de Sèvre | 1 |
| Forêt de La Crèche (4) ⚠️ | La Crèche › Haut Val de Sèvre | 1 |
| Forêt de La Crèche (7) ⚠️ | La Crèche › Haut Val de Sèvre | 1 |
| Forêt de Sainte-Néomaye ⚠️ | Sainte-Néomaye › Haut Val de Sèvre | 1 |
| Forêt de Sainte-Néomaye (2) ⚠️ | Sainte-Néomaye › Haut Val de Sèvre | 1 |
| Forêt de Sainte-Néomaye (5) ⚠️ | Sainte-Néomaye › Haut Val de Sèvre | 1 |
| Forêt de Sainte-Néomaye (7) ⚠️ | Sainte-Néomaye › Haut Val de Sèvre | 1 |
| Forêt de Sainte-Néomaye (10) ⚠️ | Sainte-Néomaye › Haut Val de Sèvre | 1 |
| Forêt de Sainte-Néomaye (13) ⚠️ | Sainte-Néomaye › Haut Val de Sèvre | 1 |
| Forêt de Sainte-Néomaye (14) ⚠️ | Sainte-Néomaye › Haut Val de Sèvre | 1 |
| Forêt de Sainte-Néomaye (17) ⚠️ | Sainte-Néomaye › Haut Val de Sèvre | 1 |
| Forêt de La Crèche (12) ⚠️ | La Crèche › Haut Val de Sèvre | 1 |
| Forêt de Romans (2) ⚠️ | Romans › Haut Val de Sèvre | 1 |
| Forêt de Romans (5) ⚠️ | Romans › Haut Val de Sèvre | 1 |
| Forêt de Sainte-Néomaye (20) ⚠️ | Sainte-Néomaye › Haut Val de Sèvre | 1 |
| Forêt de Romans (8) ⚠️ | Romans › Haut Val de Sèvre | 1 |
| Forêt de Saint-Martin-de-Saint-Maixent (3) ⚠️ | Saint-Martin-de-Saint-Maixent › Haut Val de Sèvre | 1 |
| Forêt de Saint-Martin-de-Saint-Maixent (5) ⚠️ | Saint-Martin-de-Saint-Maixent › Haut Val de Sèvre | 1 |
| Forêt de Saint-Martin-de-Saint-Maixent (8) ⚠️ | Saint-Martin-de-Saint-Maixent › Haut Val de Sèvre | 1 |
| Forêt de Saint-Martin-de-Saint-Maixent (13) ⚠️ | Saint-Martin-de-Saint-Maixent › Haut Val de Sèvre | 1 |
| Forêt de La Peyratte (2) ⚠️ | La Peyratte › Parthenay-Gâtine | 1 |
| Bois du Tallud ⚠️ | Le Tallud › Parthenay-Gâtine | 1 |
| Bois du Tallud (3) ⚠️ | Le Tallud › Parthenay-Gâtine | 1 |
| Bois de Saint-Pardoux-Soutiers (2) ⚠️ | Saint-Pardoux-Soutiers › Val de Gâtine | 1 |
| Forêt de Bressuire (4) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Doux (3) ⚠️ | Doux › Parthenay-Gâtine | 1 |
| Bois de Saint-Pardoux-Soutiers (4) ⚠️ | Saint-Pardoux-Soutiers › Val de Gâtine | 1 |
| Bois de Pompaire ⚠️ | Pompaire › Parthenay-Gâtine | 1 |
| Forêt de Scillé (2) ⚠️ | Scillé › Val de Gâtine | 1 |
| Bois de Vernoux-en-Gâtine ⚠️ | Vernoux-en-Gâtine › Parthenay-Gâtine | 1 |
| Bois de Beugnon-Thireuil ⚠️ | Beugnon-Thireuil › Val de Gâtine | 1 |
| Bois de Vernoux-en-Gâtine (3) ⚠️ | Vernoux-en-Gâtine › Parthenay-Gâtine | 1 |
| Bois de Voulmentin (2) ⚠️ | Voulmentin › Bocage Bressuirais | 1 |
| Bois de Voulmentin (3) ⚠️ | Voulmentin › Bocage Bressuirais | 1 |
| Bois de Voulmentin (6) ⚠️ | Voulmentin › Bocage Bressuirais | 1 |
| Bois de Voulmentin (9) ⚠️ | Voulmentin › Bocage Bressuirais | 1 |
| Bois de Voulmentin (10) ⚠️ | Voulmentin › Bocage Bressuirais | 1 |
| Bois de Voulmentin (11) ⚠️ | Voulmentin › Bocage Bressuirais | 1 |
| Bois de Voulmentin (13) ⚠️ | Voulmentin › Bocage Bressuirais | 1 |
| Bois du Tallud (5) ⚠️ | Le Tallud › Parthenay-Gâtine | 1 |
| Bois de Azay-sur-Thouet (2) ⚠️ | Azay-sur-Thouet › Parthenay-Gâtine | 1 |
| Forêt de Augé (3) ⚠️ | Augé › Haut Val de Sèvre | 1 |
| Forêt de Augé (9) ⚠️ | Augé › Haut Val de Sèvre | 1 |
| Forêt de Augé (12) ⚠️ | Augé › Haut Val de Sèvre | 1 |
| Forêt de Augé (14) ⚠️ | Augé › Haut Val de Sèvre | 1 |
| Forêt de Augé (16) ⚠️ | Augé › Haut Val de Sèvre | 1 |
| Forêt de Augé (24) ⚠️ | Augé › Haut Val de Sèvre | 1 |
| Forêt de Augé (27) ⚠️ | Augé › Haut Val de Sèvre | 1 |
| Forêt de Augé (29) ⚠️ | Augé › Haut Val de Sèvre | 1 |
| Forêt de Augé (30) ⚠️ | Augé › Haut Val de Sèvre | 1 |
| Forêt de Augé (33) ⚠️ | Augé › Haut Val de Sèvre | 1 |
| Forêt de Cherveux (5) ⚠️ | Cherveux › Haut Val de Sèvre | 1 |
| Forêt de Augé (36) ⚠️ | Augé › Haut Val de Sèvre | 1 |
| Forêt de Saivres (2) ⚠️ | Saivres › Haut Val de Sèvre | 1 |
| Forêt de Augé (55) ⚠️ | Augé › Haut Val de Sèvre | 1 |
| Forêt de Augé (57) ⚠️ | Augé › Haut Val de Sèvre | 1 |
| Forêt de Augé (58) ⚠️ | Augé › Haut Val de Sèvre | 1 |
| Forêt de Saint-Léger-de-Montbrun (3) ⚠️ | Saint-Léger-de-Montbrun › Thouarsais | 1 |
| Forêt de Pas-de-Jeu ⚠️ | Pas-de-Jeu › Thouarsais | 1 |
| Forêt de Pas-de-Jeu (2) ⚠️ | Pas-de-Jeu › Thouarsais | 1 |
| Forêt de Thénezay (6) ⚠️ | Thénezay › Parthenay-Gâtine | 1 |
| Forêt de Thénezay (8) ⚠️ | Thénezay › Parthenay-Gâtine | 1 |
| Forêt de Saivres (6) ⚠️ | Saivres › Haut Val de Sèvre | 1 |
| Forêt de Saint-Georges-de-Noisné (3) ⚠️ | Saint-Georges-de-Noisné › Val de Gâtine | 1 |
| Forêt de Augé (61) ⚠️ | Augé › Haut Val de Sèvre | 1 |
| Forêt de Augé (70) ⚠️ | Augé › Haut Val de Sèvre | 1 |
| Forêt de Augé (74) ⚠️ | Augé › Haut Val de Sèvre | 1 |
| Forêt de Augé (78) ⚠️ | Augé › Haut Val de Sèvre | 1 |
| Forêt de La Chapelle-Pouilloux (2) ⚠️ | La Chapelle-Pouilloux › Mellois en Poitou | 1 |
| Forêt de Mairé-Levescault (5) ⚠️ | Mairé-Levescault › Mellois en Poitou | 1 |
| Forêt de Augé (82) ⚠️ | Augé › Haut Val de Sèvre | 1 |
| Forêt de Augé (83) ⚠️ | Augé › Haut Val de Sèvre | 1 |
| Forêt de Alloinay (3) ⚠️ | Alloinay › Mellois en Poitou | 1 |
| Forêt de Alloinay (4) ⚠️ | Alloinay › Mellois en Poitou | 1 |
| Bois de Châtillon-sur-Thouet (4) ⚠️ | Châtillon-sur-Thouet › Parthenay-Gâtine | 1 |
| Forêt de Coulon (3) ⚠️ | Coulon › Niortais | 1 |
| Forêt de Niort (4) ⚠️ | Niort › Niortais | 1 |
| Forêt de Augé (95) ⚠️ | Augé › Haut Val de Sèvre | 1 |
| Forêt de Melle (4) ⚠️ | Melle › Mellois en Poitou | 1 |
| La Maladrie ⚠️ | Melle › Mellois en Poitou | 1 |
| Bois de Mauléon (5) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois de Nueil-les-Aubiers (4) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Bois de Nueil-les-Aubiers (5) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Bois de Nueil-les-Aubiers (10) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Bois de Nueil-les-Aubiers (12) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Bois de Nueil-les-Aubiers (13) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Bois de Nueil-les-Aubiers (14) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Forêt de La Peyratte (4) ⚠️ | La Peyratte › Parthenay-Gâtine | 1 |
| Forêt de Pougne-Hérisson ⚠️ | Pougne-Hérisson › Parthenay-Gâtine | 1 |
| Forêt de Pougne-Hérisson (3) ⚠️ | Pougne-Hérisson › Parthenay-Gâtine | 1 |
| Forêt de Neuvy-Bouin (6) ⚠️ | Neuvy-Bouin › Bocage Bressuirais | 1 |
| Forêt de Saint-Aubin-le-Cloud (4) ⚠️ | Saint-Aubin-le-Cloud › Parthenay-Gâtine | 1 |
| Forêt de Pougne-Hérisson (6) ⚠️ | Pougne-Hérisson › Parthenay-Gâtine | 1 |
| Forêt de Saint-Aubin-le-Cloud (5) ⚠️ | Saint-Aubin-le-Cloud › Parthenay-Gâtine | 1 |
| Forêt de Pougne-Hérisson (9) ⚠️ | Pougne-Hérisson › Parthenay-Gâtine | 1 |
| Forêt de Pougne-Hérisson (10) ⚠️ | Pougne-Hérisson › Parthenay-Gâtine | 1 |
| Forêt de Pougne-Hérisson (16) ⚠️ | Pougne-Hérisson › Parthenay-Gâtine | 1 |
| Forêt de Ménigoute (3) ⚠️ | Ménigoute › Parthenay-Gâtine | 1 |
| Bois de Nueil-les-Aubiers (18) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Bois de Nueil-les-Aubiers (19) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Bois de Nueil-les-Aubiers (21) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Bois de Nueil-les-Aubiers (22) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Bois de Fénery (2) ⚠️ | Saint-Aubin-le-Cloud › Parthenay-Gâtine | 1 |
| Forêt de La Ferrière-en-Parthenay (7) ⚠️ | La Ferrière-en-Parthenay › Parthenay-Gâtine | 1 |
| Forêt de Thénezay (10) ⚠️ | Thénezay › Parthenay-Gâtine | 1 |
| Forêt de Thénezay (12) ⚠️ | Thénezay › Parthenay-Gâtine | 1 |
| Parc de Bressuire ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Forêt de Bressuire (8) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Argentonnay ⚠️ | Argentonnay › Bocage Bressuirais | 1 |
| Forêt de Moncoutant-sur-Sèvre (5) ⚠️ | Moncoutant-sur-Sèvre › Bocage Bressuirais | 1 |
| Bois de Saint-Marc-la-Lande ⚠️ | Saint-Marc-la-Lande › Val de Gâtine | 1 |
| Forêt de Saint-Varent ⚠️ | Saint-Varent › Thouarsais | 1 |
| Forêt de Louin (3) ⚠️ | Louin › Airvaudais-Val du Thouet | 1 |
| Forêt de Airvault (8) ⚠️ | Airvault › Airvaudais-Val du Thouet | 1 |
| Forêt de Airvault (10) ⚠️ | Airvault › Airvaudais-Val du Thouet | 1 |
| Forêt de Airvault (13) ⚠️ | Airvault › Airvaudais-Val du Thouet | 1 |
| Forêt de Luzay (4) ⚠️ | Luzay › Thouarsais | 1 |
| Forêt de Saint-Généroux ⚠️ | Saint-Généroux › Thouarsais | 1 |
| Forêt de Luzay (9) ⚠️ | Luzay › Thouarsais | 1 |
| Forêt de Luzay (12) ⚠️ | Luzay › Thouarsais | 1 |
| Forêt de Luzay (13) ⚠️ | Luzay › Thouarsais | 1 |
| Forêt de Saint-Léger-de-Montbrun (10) ⚠️ | Saint-Léger-de-Montbrun › Thouarsais | 1 |
| Forêt de Vasles (15) ⚠️ | Vasles › Parthenay-Gâtine | 1 |
| Forêt de Vasles (16) ⚠️ | Vasles › Parthenay-Gâtine | 1 |
| Forêt de Mazières-en-Gâtine (5) ⚠️ | Mazières-en-Gâtine › Val de Gâtine | 1 |
| Forêt de Mazières-en-Gâtine (10) ⚠️ | Mazières-en-Gâtine › Val de Gâtine | 1 |
| Forêt de Mazières-en-Gâtine (12) ⚠️ | Mazières-en-Gâtine › Val de Gâtine | 1 |
| Forêt de Plaine-et-Vallées (11) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Forêt de Plaine-et-Vallées (12) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Forêt de Marnes (3) ⚠️ | Marnes › Thouarsais | 1 |
| Forêt de Fontivillié (4) ⚠️ | Fontivillié › Mellois en Poitou | 1 |
| Bois de Coulon (3) ⚠️ | Coulon › Niortais | 1 |
| Forêt de Glénay (5) ⚠️ | Glénay › Thouarsais | 1 |
| Forêt de Glénay (7) ⚠️ | Glénay › Thouarsais | 1 |
| Forêt de Glénay (9) ⚠️ | Glénay › Thouarsais | 1 |
| Forêt de Sainte-Gemme (2) ⚠️ | Sainte-Gemme › Thouarsais | 1 |
| Forêt de Pierrefitte (2) ⚠️ | Pierrefitte › Thouarsais | 1 |
| Bois de Bressuire (4) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Forêt de Argentonnay (10) ⚠️ | Argentonnay › Bocage Bressuirais | 1 |
| Forêt de Beauvoir-sur-Niort (5) ⚠️ | Beauvoir-sur-Niort › Niortais | 1 |
| Forêt de Fenioux (5) ⚠️ | Fenioux › Val de Gâtine | 1 |
| Forêt de Melle (8) ⚠️ | Melle › Mellois en Poitou | 1 |
| Forêt de Saint-Gelais ⚠️ | Saint-Gelais › Niortais | 1 |
| Bois de Bressuire (6) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Bressuire (8) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Bressuire (9) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Forêt de Thénezay (16) ⚠️ | Thénezay › Parthenay-Gâtine | 1 |
| Bois de Bressuire (11) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Argentonnay (7) ⚠️ | Argentonnay › Bocage Bressuirais | 1 |
| Forêt de Argentonnay (13) ⚠️ | Argentonnay › Bocage Bressuirais | 1 |
| Bois de Bressuire (12) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Bressuire (14) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Bressuire (15) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Bressuire (16) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Bressuire (17) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Forêt de Argentonnay (15) ⚠️ | Argentonnay › Bocage Bressuirais | 1 |
| Forêt de Thouars (10) ⚠️ | Thouars › Thouarsais | 1 |
| Forêt de Augé (108) ⚠️ | Augé › Haut Val de Sèvre | 1 |
| Forêt de Irais ⚠️ | Irais › Airvaudais-Val du Thouet | 1 |
| Forêt de Irais (2) ⚠️ | Irais › Airvaudais-Val du Thouet | 1 |
| Forêt de Irais (3) ⚠️ | Irais › Airvaudais-Val du Thouet | 1 |
| Forêt de Availles-Thouarsais (3) ⚠️ | Availles-Thouarsais › Airvaudais-Val du Thouet | 1 |
| Forêt de Airvault (24) ⚠️ | Airvault › Airvaudais-Val du Thouet | 1 |
| Bois de Airvault ⚠️ | Airvault › Airvaudais-Val du Thouet | 1 |
| Forêt de Chizé (6) ⚠️ | Chizé › Mellois en Poitou | 1 |
| Forêt de Périgné ⚠️ | Périgné › Mellois en Poitou | 1 |
| Parc de Coulonges-sur-l'Autize ⚠️ | Coulonges-sur-l'Autize › Val de Gâtine | 1 |
| Forêt de Saint-Varent (6) ⚠️ | Saint-Varent › Thouarsais | 1 |
| Forêt de Périgné (7) ⚠️ | Périgné › Mellois en Poitou | 1 |
| Forêt de Thénezay (18) ⚠️ | Thénezay › Parthenay-Gâtine | 1 |
| Forêt de Louzy (3) ⚠️ | Louzy › Thouarsais | 1 |
| Forêt de Thouars (12) ⚠️ | Thouars › Thouarsais | 1 |
| Forêt de Thouars (14) ⚠️ | Thouars › Thouarsais | 1 |
| Forêt de Thouars (16) ⚠️ | Thouars › Thouarsais | 1 |
| Forêt de Marnes (5) ⚠️ | Marnes › Thouarsais | 1 |
| Forêt de Val en Vignes (6) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Forêt de Val en Vignes (7) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Forêt de Val en Vignes (8) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Forêt de Val en Vignes (9) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Forêt de Saint-Léger-de-Montbrun (12) ⚠️ | Saint-Léger-de-Montbrun › Thouarsais | 1 |
| Forêt de Niort (6) ⚠️ | Niort › Niortais | 1 |
| Forêt de Niort (7) ⚠️ | Niort › Niortais | 1 |
| Bois de Argentonnay (30) ⚠️ | Argentonnay › Bocage Bressuirais | 1 |
| Forêt de Doux (7) ⚠️ | Doux › Parthenay-Gâtine | 1 |
| Forêt de Coulon (8) ⚠️ | Coulon › Niortais | 1 |
| Forêt de Coulon (13) ⚠️ | Coulon › Niortais | 1 |
| Forêt de Magné (2) ⚠️ | Magné › Niortais | 1 |
| Forêt de Magné (3) ⚠️ | Magné › Niortais | 1 |
| Forêt de Chizé (7) ⚠️ | Chizé › Mellois en Poitou | 1 |
| Forêt de Villiers-sur-Chizé (6) ⚠️ | Villiers-sur-Chizé › Mellois en Poitou | 1 |
| Forêt de Villiers-sur-Chizé (7) ⚠️ | Villiers-sur-Chizé › Mellois en Poitou | 1 |
| Forêt de Villiers-sur-Chizé (8) ⚠️ | Villiers-sur-Chizé › Mellois en Poitou | 1 |
| Forêt de Villiers-sur-Chizé (9) ⚠️ | Villiers-sur-Chizé › Mellois en Poitou | 1 |
| Forêt de Villiers-sur-Chizé (10) ⚠️ | Villiers-sur-Chizé › Mellois en Poitou | 1 |
| Bois de Bressuire (22) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Bressuire (24) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Bressuire (25) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Bressuire (26) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Bressuire (27) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Bressuire (31) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Bressuire (34) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Forêt de Plaine-d'Argenson (5) ⚠️ | Plaine-d'Argenson › Niortais | 1 |
| Forêt de Plaine-d'Argenson (9) ⚠️ | Plaine-d'Argenson › Niortais | 1 |
| Forêt de Airvault (25) ⚠️ | Airvault › Airvaudais-Val du Thouet | 1 |
| Forêt de Marnes (9) ⚠️ | Marnes › Thouarsais | 1 |
| Forêt de Plaine-et-Vallées (23) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Forêt de Marnes (10) ⚠️ | Marnes › Thouarsais | 1 |
| Forêt de Airvault (29) ⚠️ | Airvault › Airvaudais-Val du Thouet | 1 |
| Forêt de Airvault (30) ⚠️ | Airvault › Airvaudais-Val du Thouet | 1 |
| Forêt de Plaine-et-Vallées (25) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Forêt de Airvault (32) ⚠️ | Airvault › Airvaudais-Val du Thouet | 1 |
| Forêt de Marnes (12) ⚠️ | Marnes › Thouarsais | 1 |
| Forêt de Airvault (35) ⚠️ | Airvault › Airvaudais-Val du Thouet | 1 |
| Forêt de Marnes (21) ⚠️ | Marnes › Thouarsais | 1 |
| Bois de Bressuire (37) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Bressuire (38) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Bressuire (39) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Bressuire (40) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Bressuire (42) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Bressuire (46) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Bressuire (48) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Bressuire (49) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Forêt de Coulon (18) ⚠️ | Coulon › Niortais | 1 |
| Forêt de Coulon (26) ⚠️ | Coulon › Niortais | 1 |
| Forêt de Coulon (28) ⚠️ | Coulon › Niortais | 1 |
| Forêt de Coulon (29) ⚠️ | Coulon › Niortais | 1 |
| Forêt de Coulon (30) ⚠️ | Coulon › Niortais | 1 |
| Bois de Bressuire (53) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Bressuire (60) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Bressuire (67) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Forêt du Busseau (4) ⚠️ | Le Busseau › Val de Gâtine | 1 |
| Forêt du Busseau (5) ⚠️ | Le Busseau › Val de Gâtine | 1 |
| Forêt de Magné (6) ⚠️ | Magné › Niortais | 1 |
| Forêt de Fomperron (6) ⚠️ | Fomperron › Parthenay-Gâtine | 1 |
| Forêt de Soudan (3) ⚠️ | Soudan › Haut Val de Sèvre | 1 |
| Forêt de Aigondigné ⚠️ | Aigondigné › Mellois en Poitou | 1 |
| Forêt de Bessines (3) ⚠️ | Bessines › Niortais | 1 |
| Forêt de Magné (9) ⚠️ | Magné › Niortais | 1 |
| Forêt de Soudan (4) ⚠️ | Soudan › Haut Val de Sèvre | 1 |
| Bois de Cirières (3) ⚠️ | Cirières › Bocage Bressuirais | 1 |
| Bois de Bressuire (71) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Forêt de Melleran (6) ⚠️ | Melleran › Mellois en Poitou | 1 |
| Forêt de Magné (17) ⚠️ | Magné › Niortais | 1 |
| Forêt de Sansais (3) ⚠️ | Sansais › Niortais | 1 |
| Forêt de Magné (22) ⚠️ | Magné › Niortais | 1 |
| Forêt de Magné (26) ⚠️ | Magné › Niortais | 1 |
| Forêt de Magné (31) ⚠️ | Magné › Niortais | 1 |
| Forêt de Magné (32) ⚠️ | Magné › Niortais | 1 |
| Bois de Bressuire (81) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Bressuire (82) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Bressuire (83) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Forêt de Lezay (6) ⚠️ | Lezay › Mellois en Poitou | 1 |
| Forêt de Lezay (7) ⚠️ | Lezay › Mellois en Poitou | 1 |
| Forêt de Saint-Cyr-la-Lande (4) ⚠️ | Saint-Cyr-la-Lande › Thouarsais | 1 |
| Bois de Argentonnay (42) ⚠️ | Argentonnay › Bocage Bressuirais | 1 |
| Bois de Argentonnay (43) ⚠️ | Argentonnay › Bocage Bressuirais | 1 |
| Forêt de Sansais (6) ⚠️ | Sansais › Niortais | 1 |
| Forêt de Magné (39) ⚠️ | Magné › Niortais | 1 |
| Forêt de Magné (42) ⚠️ | Magné › Niortais | 1 |
| Forêt de Sansais (8) ⚠️ | Sansais › Niortais | 1 |
| Forêt de Alloinay (6) ⚠️ | Alloinay › Mellois en Poitou | 1 |
| Forêt de Alloinay (8) ⚠️ | Alloinay › Mellois en Poitou | 1 |
| Forêt de Saint-Cyr-la-Lande (6) ⚠️ | Saint-Cyr-la-Lande › Thouarsais | 1 |
| Forêt de Chenay ⚠️ | Chenay › Mellois en Poitou | 1 |
| Parc de la Mairie ⚠️ | Vouillé › Niortais | 1 |
| Forêt de Sansais (12) ⚠️ | Sansais › Niortais | 1 |
| Forêt de Sansais (13) ⚠️ | Sansais › Niortais | 1 |
| Forêt de Doux (11) ⚠️ | Doux › Parthenay-Gâtine | 1 |
| Forêt de Doux (12) ⚠️ | Doux › Parthenay-Gâtine | 1 |
| Forêt de Doux (13) ⚠️ | Doux › Parthenay-Gâtine | 1 |
| Le Bois de la Grange ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Bressuire (90) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Forêt de Celles-sur-Belle (3) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 1 |
| Forêt de Villefollet (2) ⚠️ | Villefollet › Mellois en Poitou | 1 |
| Forêt de Villefollet (3) ⚠️ | Villefollet › Mellois en Poitou | 1 |
| Forêt de Villefollet (4) ⚠️ | Villefollet › Mellois en Poitou | 1 |
| Forêt de Celles-sur-Belle (5) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 1 |
| Forêt de Saint-Romans-lès-Melle (2) ⚠️ | Saint-Romans-lès-Melle › Mellois en Poitou | 1 |
| Forêt de Saint-Romans-lès-Melle (3) ⚠️ | Saint-Romans-lès-Melle › Mellois en Poitou | 1 |
| Forêt de Saint-Romans-lès-Melle (4) ⚠️ | Saint-Romans-lès-Melle › Mellois en Poitou | 1 |
| Forêt de Marcillé (6) ⚠️ | Marcillé › Mellois en Poitou | 1 |
| Arboretum forestier Les Deux-Sèvres à travers bois ⚠️ | Melle › Mellois en Poitou | 1 |
| Forêt de Celles-sur-Belle (9) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 1 |
| Forêt de Brieuil-sur-Chizé (2) ⚠️ | Brieuil-sur-Chizé › Mellois en Poitou | 1 |
| Forêt de La Crèche (15) ⚠️ | La Crèche › Haut Val de Sèvre | 1 |
| Forêt de Sansais (24) ⚠️ | Sansais › Niortais | 1 |
| Forêt du Vanneau-Irleau (2) ⚠️ | Le Vanneau-Irleau › Niortais | 1 |
| Forêt du Vanneau-Irleau (3) ⚠️ | Le Vanneau-Irleau › Niortais | 1 |
| Forêt de Celles-sur-Belle (12) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 1 |
| Forêt de Vernoux-en-Gâtine (6) ⚠️ | Vernoux-en-Gâtine › Parthenay-Gâtine | 1 |
| Forêt de Sepvret (2) ⚠️ | Sepvret › Mellois en Poitou | 1 |
| Bois de Scillé ⚠️ | Scillé › Val de Gâtine | 1 |
| Bois de Scillé (2) ⚠️ | Scillé › Val de Gâtine | 1 |
| Bois de Scillé (3) ⚠️ | Scillé › Val de Gâtine | 1 |
| Forêt du Busseau (7) ⚠️ | Le Busseau › Val de Gâtine | 1 |
| Forêt de Bressuire (11) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Forêt de Alloinay (11) ⚠️ | Alloinay › Mellois en Poitou | 1 |
| Forêt de Airvault (39) ⚠️ | Airvault › Airvaudais-Val du Thouet | 1 |
| Forêt de Melle (24) ⚠️ | Melle › Mellois en Poitou | 1 |
| Forêt de Valdelaume (6) ⚠️ | Valdelaume › Mellois en Poitou | 1 |
| Forêt de Melle (28) ⚠️ | Melle › Mellois en Poitou | 1 |
| Forêt de Melle (30) ⚠️ | Melle › Mellois en Poitou | 1 |
| Forêt de Marcillé (10) ⚠️ | Marcillé › Mellois en Poitou | 1 |
| Forêt de Marcillé (12) ⚠️ | Marcillé › Mellois en Poitou | 1 |
| Parc de Melle (2) ⚠️ | Melle › Mellois en Poitou | 1 |
| Forêt de Marcillé (16) ⚠️ | Marcillé › Mellois en Poitou | 1 |
| Forêt de Marcillé (17) ⚠️ | Marcillé › Mellois en Poitou | 1 |
| Forêt de Saint-Amand-sur-Sèvre (4) ⚠️ | Saint-Amand-sur-Sèvre › Bocage Bressuirais | 1 |
| Forêt de Saint-Romans-lès-Melle (6) ⚠️ | Saint-Romans-lès-Melle › Mellois en Poitou | 1 |
| Parc de Bressuire (8) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Forêt de Melle (34) ⚠️ | Melle › Mellois en Poitou | 1 |
| Forêt de Melle (35) ⚠️ | Melle › Mellois en Poitou | 1 |
| Forêt de Melle (40) ⚠️ | Melle › Mellois en Poitou | 1 |
| Forêt de Saint-Vincent-la-Châtre (3) ⚠️ | Saint-Vincent-la-Châtre › Mellois en Poitou | 1 |
| Forêt de Melle (42) ⚠️ | Melle › Mellois en Poitou | 1 |
| Bois de Voulmentin (15) ⚠️ | Voulmentin › Bocage Bressuirais | 1 |
| Forêt de Melle (48) ⚠️ | Melle › Mellois en Poitou | 1 |
| Forêt de Melle (50) ⚠️ | Melle › Mellois en Poitou | 1 |
| Forêt de Melle (54) ⚠️ | Melle › Mellois en Poitou | 1 |
| Forêt de Béceleuf ⚠️ | Béceleuf › Val de Gâtine | 1 |
| Forêt de Sepvret (4) ⚠️ | Sepvret › Mellois en Poitou | 1 |
| Forêt de Melle (59) ⚠️ | Melle › Mellois en Poitou | 1 |
| Forêt de Beaussais-Vitré (2) ⚠️ | Beaussais-Vitré › Mellois en Poitou | 1 |
| Forêt de Melle (63) ⚠️ | Melle › Mellois en Poitou | 1 |
| Forêt de Melle (68) ⚠️ | Melle › Mellois en Poitou | 1 |
| Forêt de Melle (70) ⚠️ | Melle › Mellois en Poitou | 1 |
| Forêt de Périgné (13) ⚠️ | Périgné › Mellois en Poitou | 1 |
| Forêt de Périgné (15) ⚠️ | Périgné › Mellois en Poitou | 1 |
| Parc de Celles-sur-Belle (2) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 1 |
| Forêt de Celles-sur-Belle (15) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 1 |
| Forêt de Celles-sur-Belle (16) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 1 |
| Forêt de Celles-sur-Belle (18) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 1 |
| Forêt de Celles-sur-Belle (21) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 1 |
| Forêt de Bressuire (17) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Forêt de Bressuire (18) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Forêt de Périgné (20) ⚠️ | Périgné › Mellois en Poitou | 1 |
| Forêt de Périgné (21) ⚠️ | Périgné › Mellois en Poitou | 1 |
| Bois de Bressuire (96) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Coulonges-Thouarsais (7) ⚠️ | Coulonges-Thouarsais › Thouarsais | 1 |
| Forêt de Bressuire (19) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Forêt de Bressuire (20) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Forêt de Melle (72) ⚠️ | Melle › Mellois en Poitou | 1 |
| Forêt de Beaussais-Vitré (5) ⚠️ | Beaussais-Vitré › Mellois en Poitou | 1 |
| Forêt de Melle (76) ⚠️ | Melle › Mellois en Poitou | 1 |
| Forêt de Beaussais-Vitré (12) ⚠️ | Beaussais-Vitré › Mellois en Poitou | 1 |
| Forêt de Beaussais-Vitré (14) ⚠️ | Beaussais-Vitré › Mellois en Poitou | 1 |
| Forêt de Beaussais-Vitré (16) ⚠️ | Beaussais-Vitré › Mellois en Poitou | 1 |
| Forêt de Beaussais-Vitré (17) ⚠️ | Beaussais-Vitré › Mellois en Poitou | 1 |
| Forêt de Beaussais-Vitré (24) ⚠️ | Beaussais-Vitré › Mellois en Poitou | 1 |
| Forêt de Beaussais-Vitré (27) ⚠️ | Beaussais-Vitré › Mellois en Poitou | 1 |
| Forêt de Airvault (43) ⚠️ | Airvault › Airvaudais-Val du Thouet | 1 |
| Forêt de Airvault (44) ⚠️ | Airvault › Airvaudais-Val du Thouet | 1 |
| Forêt de Beaussais-Vitré (30) ⚠️ | Beaussais-Vitré › Mellois en Poitou | 1 |
| Forêt de Prailles-la-Couarde (6) ⚠️ | Prailles-la-Couarde › Mellois en Poitou | 1 |
| Forêt de Prailles-la-Couarde (7) ⚠️ | Prailles-la-Couarde › Mellois en Poitou | 1 |
| Forêt de Prailles-la-Couarde (8) ⚠️ | Prailles-la-Couarde › Mellois en Poitou | 1 |
| Forêt de Prailles-la-Couarde (10) ⚠️ | Beaussais-Vitré › Mellois en Poitou | 1 |
| Forêt de Thénezay (19) ⚠️ | Thénezay › Parthenay-Gâtine | 1 |
| Forêt de Louzy (7) ⚠️ | Louzy › Thouarsais | 1 |
| Bois de Louzy ⚠️ | Louzy › Thouarsais | 1 |
| Bois de Louzy (4) ⚠️ | Louzy › Thouarsais | 1 |
| Bois de Louzy (9) ⚠️ | Louzy › Thouarsais | 1 |
| Forêt de Saint-Hilaire-la-Palud (3) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 1 |
| Forêt de Saint-Hilaire-la-Palud (5) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 1 |
| Forêt de Saint-Hilaire-la-Palud (6) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 1 |
| Forêt de Saint-Hilaire-la-Palud (7) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 1 |
| Forêt de Saint-Hilaire-la-Palud (8) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 1 |
| Forêt de Prailles-la-Couarde (12) ⚠️ | Prailles-la-Couarde › Mellois en Poitou | 1 |
| Forêt de Prailles-la-Couarde (18) ⚠️ | Prailles-la-Couarde › Mellois en Poitou | 1 |
| Forêt de Prailles-la-Couarde (22) ⚠️ | Prailles-la-Couarde › Mellois en Poitou | 1 |
| Forêt de Prailles-la-Couarde (23) ⚠️ | Prailles-la-Couarde › Mellois en Poitou | 1 |
| Forêt de Aigondigné (7) ⚠️ | Aigondigné › Mellois en Poitou | 1 |
| Parc de Bressuire (13) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Bressuire (105) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Bressuire (107) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Forêt de Brioux-sur-Boutonne (4) ⚠️ | Brioux-sur-Boutonne › Mellois en Poitou | 1 |
| Forêt de Périgné (25) ⚠️ | Périgné › Mellois en Poitou | 1 |
| Forêt de Secondigné-sur-Belle (3) ⚠️ | Secondigné-sur-Belle › Mellois en Poitou | 1 |
| Forêt de Secondigné-sur-Belle (8) ⚠️ | Secondigné-sur-Belle › Mellois en Poitou | 1 |
| Parc de la Mignauderie ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Forêt de Prailles-la-Couarde (25) ⚠️ | Prailles-la-Couarde › Mellois en Poitou | 1 |
| Forêt de Prailles-la-Couarde (26) ⚠️ | Prailles-la-Couarde › Mellois en Poitou | 1 |
| Forêt de Prailles-la-Couarde (27) ⚠️ | Prailles-la-Couarde › Mellois en Poitou | 1 |
| Forêt de Aigondigné (8) ⚠️ | Aigondigné › Mellois en Poitou | 1 |
| Bois de Bressuire (108) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Place de la Brèche ⚠️ | Niort › Niortais | 1 |
| Forêt de Prailles-la-Couarde (39) ⚠️ | Prailles-la-Couarde › Mellois en Poitou | 1 |
| Forêt de Prailles-la-Couarde (41) ⚠️ | Prailles-la-Couarde › Mellois en Poitou | 1 |
| Forêt de Prailles-la-Couarde (42) ⚠️ | Prailles-la-Couarde › Mellois en Poitou | 1 |
| Forêt de Souvigné (8) ⚠️ | Souvigné › Haut Val de Sèvre | 1 |
| Forêt de Vernoux-sur-Boutonne (7) ⚠️ | Vernoux-sur-Boutonne › Mellois en Poitou | 1 |
| Forêt de Vernoux-sur-Boutonne (9) ⚠️ | Vernoux-sur-Boutonne › Mellois en Poitou | 1 |
| Forêt de Vernoux-sur-Boutonne (13) ⚠️ | Vernoux-sur-Boutonne › Mellois en Poitou | 1 |
| Forêt de Vernoux-sur-Boutonne (16) ⚠️ | Vernoux-sur-Boutonne › Mellois en Poitou | 1 |
| Forêt de Vernoux-sur-Boutonne (17) ⚠️ | Vernoux-sur-Boutonne › Mellois en Poitou | 1 |
| Forêt de Augé (113) ⚠️ | Augé › Haut Val de Sèvre | 1 |
| Forêt de Souvigné (10) ⚠️ | Souvigné › Haut Val de Sèvre | 1 |
| Forêt de Séligné ⚠️ | Séligné › Mellois en Poitou | 1 |
| Forêt de Séligné (4) ⚠️ | Séligné › Mellois en Poitou | 1 |
| Forêt de Séligné (5) ⚠️ | Séligné › Mellois en Poitou | 1 |
| Forêt de Séligné (7) ⚠️ | Séligné › Mellois en Poitou | 1 |
| Forêt de Souvigné (19) ⚠️ | Souvigné › Haut Val de Sèvre | 1 |
| Forêt de Souvigné (23) ⚠️ | Souvigné › Haut Val de Sèvre | 1 |
| Forêt de Souvigné (25) ⚠️ | Souvigné › Haut Val de Sèvre | 1 |
| Forêt de Souvigné (26) ⚠️ | Souvigné › Haut Val de Sèvre | 1 |
| Forêt de Souvigné (28) ⚠️ | Souvigné › Haut Val de Sèvre | 1 |
| Forêt de Saint-Martin-de-Saint-Maixent (16) ⚠️ | Saint-Martin-de-Saint-Maixent › Haut Val de Sèvre | 1 |
| Forêt de Saint-Martin-de-Saint-Maixent (17) ⚠️ | Saint-Martin-de-Saint-Maixent › Haut Val de Sèvre | 1 |
| Forêt de Souvigné (35) ⚠️ | Souvigné › Haut Val de Sèvre | 1 |
| Forêt de Souvigné (36) ⚠️ | Souvigné › Haut Val de Sèvre | 1 |
| Forêt de Saint-Jacques-de-Thouars (2) ⚠️ | Saint-Jacques-de-Thouars › Thouarsais | 1 |
| Forêt de Souvigné (40) ⚠️ | Souvigné › Haut Val de Sèvre | 1 |
| Forêt de Souvigné (42) ⚠️ | Souvigné › Haut Val de Sèvre | 1 |
| Forêt de Pas-de-Jeu (3) ⚠️ | Pas-de-Jeu › Thouarsais | 1 |
| Forêt de Pas-de-Jeu (4) ⚠️ | Pas-de-Jeu › Thouarsais | 1 |
| Forêt de Pas-de-Jeu (5) ⚠️ | Pas-de-Jeu › Thouarsais | 1 |
| Forêt de Saint-Léger-de-Montbrun (22) ⚠️ | Saint-Léger-de-Montbrun › Thouarsais | 1 |
| Forêt de Secondigné-sur-Belle (13) ⚠️ | Secondigné-sur-Belle › Mellois en Poitou | 1 |
| Forêt de Secondigné-sur-Belle (18) ⚠️ | Secondigné-sur-Belle › Mellois en Poitou | 1 |
| Forêt de Sepvret (13) ⚠️ | Sepvret › Mellois en Poitou | 1 |
| Forêt de Sepvret (14) ⚠️ | Sepvret › Mellois en Poitou | 1 |
| Forêt de Exoudun (4) ⚠️ | Exoudun › Mellois en Poitou | 1 |
| Forêt de Sepvret (16) ⚠️ | Sepvret › Mellois en Poitou | 1 |
| Forêt de Exoudun (5) ⚠️ | Exoudun › Mellois en Poitou | 1 |
| Forêt de Sepvret (20) ⚠️ | Sepvret › Mellois en Poitou | 1 |
| Forêt de Chey (4) ⚠️ | Chey › Mellois en Poitou | 1 |
| Forêt de Chey (6) ⚠️ | Chey › Mellois en Poitou | 1 |
| Forêt de Sepvret (24) ⚠️ | Sepvret › Mellois en Poitou | 1 |
| Forêt de Saint-Varent (9) ⚠️ | Saint-Varent › Thouarsais | 1 |
| Forêt de Souvigné (46) ⚠️ | Souvigné › Haut Val de Sèvre | 1 |
| Forêt de Séligné (9) ⚠️ | Séligné › Mellois en Poitou | 1 |
| Forêt de Saint-Paul-en-Gâtine (3) ⚠️ | Saint-Paul-en-Gâtine › Bocage Bressuirais | 1 |
| Forêt de Saint-Martin-de-Saint-Maixent (19) ⚠️ | Saint-Martin-de-Saint-Maixent › Haut Val de Sèvre | 1 |
| Forêt de Souvigné (50) ⚠️ | Souvigné › Haut Val de Sèvre | 1 |
| Forêt de Souvigné (52) ⚠️ | Souvigné › Haut Val de Sèvre | 1 |
| Forêt de Saint-Paul-en-Gâtine (8) ⚠️ | Saint-Paul-en-Gâtine › Bocage Bressuirais | 1 |
| Forêt de Saint-Paul-en-Gâtine (9) ⚠️ | Saint-Paul-en-Gâtine › Bocage Bressuirais | 1 |
| Forêt du Busseau (8) ⚠️ | Le Busseau › Val de Gâtine | 1 |
| Forêt de Valdelaume (11) ⚠️ | Valdelaume › Mellois en Poitou | 1 |
| Forêt de La Mothe-Saint-Héray (4) ⚠️ | La Mothe-Saint-Héray › Mellois en Poitou | 1 |
| Forêt de La Mothe-Saint-Héray (16) ⚠️ | La Mothe-Saint-Héray › Mellois en Poitou | 1 |
| Forêt de La Mothe-Saint-Héray (17) ⚠️ | La Mothe-Saint-Héray › Mellois en Poitou | 1 |
| Forêt de La Mothe-Saint-Héray (18) ⚠️ | La Mothe-Saint-Héray › Mellois en Poitou | 1 |
| Forêt de La Mothe-Saint-Héray (21) ⚠️ | La Mothe-Saint-Héray › Mellois en Poitou | 1 |
| Forêt de Exoudun (16) ⚠️ | Exoudun › Mellois en Poitou | 1 |
| Forêt de Exoudun (18) ⚠️ | Exoudun › Mellois en Poitou | 1 |
| Forêt de Exoudun (20) ⚠️ | Exoudun › Mellois en Poitou | 1 |
| Forêt de Exoudun (21) ⚠️ | Exoudun › Mellois en Poitou | 1 |
| Forêt de Sainte-Eanne (11) ⚠️ | Sainte-Eanne › Haut Val de Sèvre | 1 |
| Forêt de Sainte-Eanne (17) ⚠️ | Sainte-Eanne › Haut Val de Sèvre | 1 |
| Forêt de Sainte-Eanne (18) ⚠️ | Sainte-Eanne › Haut Val de Sèvre | 1 |
| Forêt de Sainte-Eanne (22) ⚠️ | Sainte-Eanne › Haut Val de Sèvre | 1 |
| Forêt de Sainte-Eanne (26) ⚠️ | Sainte-Eanne › Haut Val de Sèvre | 1 |
| Forêt de Sainte-Eanne (27) ⚠️ | Sainte-Eanne › Haut Val de Sèvre | 1 |
| Forêt de Sainte-Eanne (29) ⚠️ | Sainte-Eanne › Haut Val de Sèvre | 1 |
| Forêt de Sainte-Eanne (35) ⚠️ | Sainte-Eanne › Haut Val de Sèvre | 1 |
| Forêt de Sainte-Eanne (41) ⚠️ | Sainte-Eanne › Haut Val de Sèvre | 1 |
| Forêt de Nanteuil (2) ⚠️ | Nanteuil › Haut Val de Sèvre | 1 |
| Forêt de Sainte-Eanne (42) ⚠️ | Sainte-Eanne › Haut Val de Sèvre | 1 |
| Forêt de Celles-sur-Belle (25) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 1 |
| Forêt de Saint-Martin-de-Saint-Maixent (23) ⚠️ | Saint-Martin-de-Saint-Maixent › Haut Val de Sèvre | 1 |
| Forêt de Saint-Martin-de-Saint-Maixent (24) ⚠️ | Saint-Martin-de-Saint-Maixent › Haut Val de Sèvre | 1 |
| Forêt de Saint-Martin-de-Saint-Maixent (26) ⚠️ | Saint-Martin-de-Saint-Maixent › Haut Val de Sèvre | 1 |
| Forêt de Nanteuil (7) ⚠️ | Nanteuil › Haut Val de Sèvre | 1 |
| Forêt de Nanteuil (10) ⚠️ | Nanteuil › Haut Val de Sèvre | 1 |
| Forêt de Saint-Martin-de-Saint-Maixent (28) ⚠️ | Saint-Martin-de-Saint-Maixent › Haut Val de Sèvre | 1 |
| Forêt de Nanteuil (12) ⚠️ | Nanteuil › Haut Val de Sèvre | 1 |
| Forêt de Saint-Martin-de-Saint-Maixent (32) ⚠️ | Saint-Martin-de-Saint-Maixent › Haut Val de Sèvre | 1 |
| Forêt de Nanteuil (16) ⚠️ | Nanteuil › Haut Val de Sèvre | 1 |
| Forêt de Loretz-d'Argenton (5) ⚠️ | Loretz-d'Argenton › Thouarsais | 1 |
| Forêt de Bressuire (21) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Cours d'honneur ⚠️ | Niort › Niortais | 1 |
| Forêt de Tourtenay (3) ⚠️ | Tourtenay › Thouarsais | 1 |
| Forêt de Tourtenay (4) ⚠️ | Tourtenay › Thouarsais | 1 |
| Forêt de Paizay-le-Chapt (3) ⚠️ | Paizay-le-Chapt › Mellois en Poitou | 1 |
| Forêt de Sauzé-entre-Bois (8) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Forêt de Mairé-Levescault (9) ⚠️ | Mairé-Levescault › Mellois en Poitou | 1 |
| Forêt de Sauzé-entre-Bois (10) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Forêt de Sauzé-entre-Bois (11) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Forêt de Argentonnay (20) ⚠️ | Argentonnay › Bocage Bressuirais | 1 |
| Forêt de Aigondigné (9) ⚠️ | Aigondigné › Mellois en Poitou | 1 |
| Forêt de Pamproux (4) ⚠️ | Pamproux › Haut Val de Sèvre | 1 |
| Forêt de Pamproux (5) ⚠️ | Pamproux › Haut Val de Sèvre | 1 |
| Forêt de Plaine-d'Argenson (14) ⚠️ | Plaine-d'Argenson › Niortais | 1 |
| Forêt de Plaine-d'Argenson (15) ⚠️ | Plaine-d'Argenson › Niortais | 1 |
| Forêt de Plaine-d'Argenson (19) ⚠️ | Plaine-d'Argenson › Niortais | 1 |
| Forêt de Plaine-d'Argenson (23) ⚠️ | Plaine-d'Argenson › Niortais | 1 |
| Forêt de Plaine-d'Argenson (24) ⚠️ | Plaine-d'Argenson › Niortais | 1 |
| Forêt de Saint-Léger-de-Montbrun (23) ⚠️ | Saint-Léger-de-Montbrun › Thouarsais | 1 |
| Forêt de Plaine-et-Vallées (31) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Forêt de Marigny (4) ⚠️ | Marigny › Niortais | 1 |
| Forêt de Couture-d'Argenson (7) ⚠️ | Couture-d'Argenson › Mellois en Poitou | 1 |
| Forêt de Couture-d'Argenson (8) ⚠️ | Couture-d'Argenson › Mellois en Poitou | 1 |
| Forêt de Couture-d'Argenson (9) ⚠️ | Couture-d'Argenson › Mellois en Poitou | 1 |
| Forêt de Couture-d'Argenson (13) ⚠️ | Couture-d'Argenson › Mellois en Poitou | 1 |
| Forêt de Couture-d'Argenson (14) ⚠️ | Couture-d'Argenson › Mellois en Poitou | 1 |
| Forêt de Couture-d'Argenson (16) ⚠️ | Couture-d'Argenson › Mellois en Poitou | 1 |
| Forêt de Exireuil (4) ⚠️ | Exireuil › Haut Val de Sèvre | 1 |
| Forêt de Limalonges (9) ⚠️ | Limalonges › Mellois en Poitou | 1 |
| Forêt de Sauzé-entre-Bois (12) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Forêt de Sauzé-entre-Bois (13) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Forêt de Limalonges (16) ⚠️ | Limalonges › Mellois en Poitou | 1 |
| Forêt de Limalonges (17) ⚠️ | Limalonges › Mellois en Poitou | 1 |
| Forêt de Sauzé-entre-Bois (17) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Forêt de Limalonges (20) ⚠️ | Limalonges › Mellois en Poitou | 1 |
| Forêt de Sauzé-entre-Bois (18) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Forêt de Sauzé-entre-Bois (19) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Forêt de Limalonges (21) ⚠️ | Limalonges › Mellois en Poitou | 1 |
| Forêt de Val en Vignes (10) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Forêt de Fenioux (7) ⚠️ | Fenioux › Val de Gâtine | 1 |
| Forêt de Fenioux (12) ⚠️ | Fenioux › Val de Gâtine | 1 |
| Forêt de Fenioux (13) ⚠️ | Fenioux › Val de Gâtine | 1 |
| Parc de Mauzé-sur-le-Mignon ⚠️ | Mauzé-sur-le-Mignon › Niortais | 1 |
| Place de la Mairie ⚠️ | Mauzé-sur-le-Mignon › Niortais | 1 |
| Forêt de Fenioux (16) ⚠️ | Fenioux › Val de Gâtine | 1 |
| Forêt de Valdelaume (14) ⚠️ | Valdelaume › Mellois en Poitou | 1 |
| Forêt de Valdelaume (16) ⚠️ | Valdelaume › Mellois en Poitou | 1 |
| Forêt de Valdelaume (17) ⚠️ | Valdelaume › Mellois en Poitou | 1 |
| Forêt de Valdelaume (22) ⚠️ | Valdelaume › Mellois en Poitou | 1 |
| Forêt de Valdelaume (23) ⚠️ | Valdelaume › Mellois en Poitou | 1 |
| Forêt de Valdelaume (27) ⚠️ | Valdelaume › Mellois en Poitou | 1 |
| Forêt de Valdelaume (29) ⚠️ | Valdelaume › Mellois en Poitou | 1 |
| Forêt de Valdelaume (34) ⚠️ | Valdelaume › Mellois en Poitou | 1 |
| Forêt de Valdelaume (41) ⚠️ | Valdelaume › Mellois en Poitou | 1 |
| Forêt de Valdelaume (45) ⚠️ | Valdelaume › Mellois en Poitou | 1 |
| Forêt de Valdelaume (46) ⚠️ | Valdelaume › Mellois en Poitou | 1 |
| Forêt de Valdelaume (48) ⚠️ | Valdelaume › Mellois en Poitou | 1 |
| Forêt de Valdelaume (49) ⚠️ | Valdelaume › Mellois en Poitou | 1 |
| Forêt de Valdelaume (54) ⚠️ | Valdelaume › Mellois en Poitou | 1 |
| Forêt de Valdelaume (55) ⚠️ | Valdelaume › Mellois en Poitou | 1 |
| Forêt de Melleran (8) ⚠️ | Melleran › Mellois en Poitou | 1 |
| Forêt de Melleran (10) ⚠️ | Melleran › Mellois en Poitou | 1 |
| Forêt de Melleran (13) ⚠️ | Melleran › Mellois en Poitou | 1 |
| Forêt de Melleran (16) ⚠️ | Melleran › Mellois en Poitou | 1 |
| Forêt de Fenioux (18) ⚠️ | Fenioux › Val de Gâtine | 1 |
| Forêt de Brioux-sur-Boutonne (6) ⚠️ | Brioux-sur-Boutonne › Mellois en Poitou | 1 |
| Forêt de Brioux-sur-Boutonne (7) ⚠️ | Brioux-sur-Boutonne › Mellois en Poitou | 1 |
| Forêt de Lusseray (3) ⚠️ | Lusseray › Mellois en Poitou | 1 |
| Forêt de Lusseray (4) ⚠️ | Lusseray › Mellois en Poitou | 1 |
| Forêt de Lusseray (8) ⚠️ | Lusseray › Mellois en Poitou | 1 |
| Forêt de Chérigné ⚠️ | Chérigné › Mellois en Poitou | 1 |
| Forêt de Brioux-sur-Boutonne (9) ⚠️ | Brioux-sur-Boutonne › Mellois en Poitou | 1 |
| Forêt de Brioux-sur-Boutonne (25) ⚠️ | Brioux-sur-Boutonne › Mellois en Poitou | 1 |
| Bois de Sainte-Soline ⚠️ | Sainte-Soline › Mellois en Poitou | 1 |
| Forêt de Secondigné-sur-Belle (21) ⚠️ | Secondigné-sur-Belle › Mellois en Poitou | 1 |
| Forêt de Fenioux (23) ⚠️ | Fenioux › Val de Gâtine | 1 |
| Forêt de Beugnon-Thireuil (6) ⚠️ | Beugnon-Thireuil › Val de Gâtine | 1 |
| Parc de Mauléon (3) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Forêt de Fenioux (24) ⚠️ | Fenioux › Val de Gâtine | 1 |
| Forêt de Fenioux (25) ⚠️ | Fenioux › Val de Gâtine | 1 |
| Forêt de Asnières-en-Poitou (7) ⚠️ | Asnières-en-Poitou › Mellois en Poitou | 1 |
| Forêt de Asnières-en-Poitou (8) ⚠️ | Asnières-en-Poitou › Mellois en Poitou | 1 |
| Forêt de Fenioux (26) ⚠️ | Fenioux › Val de Gâtine | 1 |
| Forêt de Fenioux (27) ⚠️ | Fenioux › Val de Gâtine | 1 |
| Forêt de Fenioux (31) ⚠️ | Fenioux › Val de Gâtine | 1 |
| La Chesnaie ⚠️ | Brion-près-Thouet › Thouarsais | 1 |
| Forêt de Fenioux (36) ⚠️ | Fenioux › Val de Gâtine | 1 |
| Forêt de Villemain (9) ⚠️ | Villemain › Mellois en Poitou | 1 |
| Forêt de Villemain (10) ⚠️ | Villemain › Mellois en Poitou | 1 |
| Forêt de Villemain (17) ⚠️ | Villemain › Mellois en Poitou | 1 |
| Forêt de Villemain (18) ⚠️ | Villemain › Mellois en Poitou | 1 |
| Forêt de Villemain (20) ⚠️ | Villemain › Mellois en Poitou | 1 |
| Forêt de Villemain (22) ⚠️ | Villemain › Mellois en Poitou | 1 |
| Forêt de Saint-Vincent-la-Châtre (5) ⚠️ | Saint-Vincent-la-Châtre › Mellois en Poitou | 1 |
| Parc de Niort (3) ⚠️ | Niort › Niortais | 1 |
| Forêt de Saint-Vincent-la-Châtre (6) ⚠️ | Saint-Vincent-la-Châtre › Mellois en Poitou | 1 |
| Bois de Melle ⚠️ | Melle › Mellois en Poitou | 1 |
| Forêt de Loubigné ⚠️ | Loubigné › Mellois en Poitou | 1 |
| Forêt des Châteliers (3) ⚠️ | Les Châteliers › Parthenay-Gâtine | 1 |
| Forêt des Châteliers (4) ⚠️ | Les Châteliers › Parthenay-Gâtine | 1 |
| Forêt de Celles-sur-Belle (26) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 1 |
| Le Bois Michault ⚠️ | Les Fosses › Mellois en Poitou | 1 |
| Forêt de Fontivillié (8) ⚠️ | Fontivillié › Mellois en Poitou | 1 |
| Forêt de Fontivillié (10) ⚠️ | Fontivillié › Mellois en Poitou | 1 |
| Forêt de Fontivillié (11) ⚠️ | Fontivillié › Mellois en Poitou | 1 |
| Forêt de Melle (79) ⚠️ | Melle › Mellois en Poitou | 1 |
| Forêt de Clussais-la-Pommeraie (13) ⚠️ | Clussais-la-Pommeraie › Mellois en Poitou | 1 |
| Forêt de Melle (80) ⚠️ | Melle › Mellois en Poitou | 1 |
| Forêt de Melle (81) ⚠️ | Melle › Mellois en Poitou | 1 |
| Forêt de Melle (83) ⚠️ | Melle › Mellois en Poitou | 1 |
| Forêt de Melle (85) ⚠️ | Melle › Mellois en Poitou | 1 |
| Forêt de Saint-Vincent-la-Châtre (13) ⚠️ | Saint-Vincent-la-Châtre › Mellois en Poitou | 1 |
| Forêt de Saint-Coutant (3) ⚠️ | Saint-Coutant › Mellois en Poitou | 1 |
| Forêt de Saint-Coutant (4) ⚠️ | Saint-Coutant › Mellois en Poitou | 1 |
| Forêt de Saint-Vincent-la-Châtre (21) ⚠️ | Saint-Vincent-la-Châtre › Mellois en Poitou | 1 |
| Forêt de Saint-Vincent-la-Châtre (22) ⚠️ | Saint-Vincent-la-Châtre › Mellois en Poitou | 1 |
| Forêt de Saint-Vincent-la-Châtre (30) ⚠️ | Saint-Vincent-la-Châtre › Mellois en Poitou | 1 |
| Forêt de Melle (86) ⚠️ | Melle › Mellois en Poitou | 1 |
| Forêt de Melle (87) ⚠️ | Melle › Mellois en Poitou | 1 |
| Forêt de Clussais-la-Pommeraie (16) ⚠️ | Clussais-la-Pommeraie › Mellois en Poitou | 1 |
| Forêt de Juillé ⚠️ | Juillé › Mellois en Poitou | 1 |
| Forêt de Juillé (3) ⚠️ | Juillé › Mellois en Poitou | 1 |
| Forêt de Juillé (4) ⚠️ | Juillé › Mellois en Poitou | 1 |
| Forêt de Juillé (5) ⚠️ | Juillé › Mellois en Poitou | 1 |
| Forêt de Juillé (8) ⚠️ | Juillé › Mellois en Poitou | 1 |
| Forêt de Juillé (10) ⚠️ | Juillé › Mellois en Poitou | 1 |
| Forêt de Juillé (11) ⚠️ | Juillé › Mellois en Poitou | 1 |
| Forêt de Saint-Coutant (13) ⚠️ | Saint-Coutant › Mellois en Poitou | 1 |
| Forêt de Saint-Coutant (16) ⚠️ | Saint-Coutant › Mellois en Poitou | 1 |
| Forêt de Saint-Coutant (17) ⚠️ | Saint-Coutant › Mellois en Poitou | 1 |
| Forêt de Clussais-la-Pommeraie (18) ⚠️ | Clussais-la-Pommeraie › Mellois en Poitou | 1 |
| Parc de La Crèche (2) ⚠️ | La Crèche › Haut Val de Sèvre | 1 |
| Forêt de Sainte-Soline (2) ⚠️ | Sainte-Soline › Mellois en Poitou | 1 |
| Forêt de Sainte-Soline (3) ⚠️ | Sainte-Soline › Mellois en Poitou | 1 |
| Forêt de Sainte-Soline (4) ⚠️ | Sainte-Soline › Mellois en Poitou | 1 |
| Forêt de Sainte-Soline (8) ⚠️ | Sainte-Soline › Mellois en Poitou | 1 |
| Parc de La Crèche (3) ⚠️ | La Crèche › Haut Val de Sèvre | 1 |
| Forêt de Clussais-la-Pommeraie (19) ⚠️ | Clussais-la-Pommeraie › Mellois en Poitou | 1 |
| Forêt de Sainte-Soline (13) ⚠️ | Sainte-Soline › Mellois en Poitou | 1 |
| Forêt de Sainte-Soline (14) ⚠️ | Sainte-Soline › Mellois en Poitou | 1 |
| Forêt de Saint-Hilaire-la-Palud (12) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 1 |
| Forêt de Saint-Hilaire-la-Palud (14) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 1 |
| Forêt de Saint-Hilaire-la-Palud (18) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 1 |
| Forêt de Saint-Hilaire-la-Palud (19) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 1 |
| Forêt de Saint-Hilaire-la-Palud (21) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 1 |
| Forêt de Saint-Hilaire-la-Palud (24) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 1 |
| Forêt de Saint-Hilaire-la-Palud (29) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 1 |
| Forêt de Arçais (6) ⚠️ | Arçais › Niortais | 1 |
| Forêt de Secondigné-sur-Belle (26) ⚠️ | Secondigné-sur-Belle › Mellois en Poitou | 1 |
| Forêt de Chérigné (2) ⚠️ | Chérigné › Mellois en Poitou | 1 |
| Forêt de Fontenille-Saint-Martin-d'Entraigues ⚠️ | Fontenille-Saint-Martin-d'Entraigues › Mellois en Poitou | 1 |
| Forêt de Saint-Hilaire-la-Palud (31) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 1 |
| Forêt de Saint-Gelais (3) ⚠️ | Saint-Gelais › Niortais | 1 |
| Forêt de Valdelaume (57) ⚠️ | Valdelaume › Mellois en Poitou | 1 |
| Forêt de Melleran (25) ⚠️ | Melleran › Mellois en Poitou | 1 |
| Forêt de Aubigné (5) ⚠️ | Aubigné › Mellois en Poitou | 1 |
| Forêt de Chérigné (5) ⚠️ | Chérigné › Mellois en Poitou | 1 |
| Forêt de Chérigné (11) ⚠️ | Chérigné › Mellois en Poitou | 1 |
| Forêt de Fontivillié (14) ⚠️ | Fontivillié › Mellois en Poitou | 1 |
| Forêt de Fontivillié (17) ⚠️ | Fontivillié › Mellois en Poitou | 1 |
| Forêt de Chef-Boutonne (5) ⚠️ | Chef-Boutonne › Mellois en Poitou | 1 |
| Forêt de Villefollet (11) ⚠️ | Villefollet › Mellois en Poitou | 1 |
| Forêt de Villefollet (14) ⚠️ | Villefollet › Mellois en Poitou | 1 |
| Forêt de Séligné (17) ⚠️ | Secondigné-sur-Belle › Mellois en Poitou | 1 |
| Forêt de Brieuil-sur-Chizé (5) ⚠️ | Brieuil-sur-Chizé › Mellois en Poitou | 1 |
| Forêt de Asnières-en-Poitou (11) ⚠️ | Asnières-en-Poitou › Mellois en Poitou | 1 |
| Forêt de Séligné (19) ⚠️ | Séligné › Mellois en Poitou | 1 |
| Forêt de Villefollet (19) ⚠️ | Villefollet › Mellois en Poitou | 1 |
| Place du Temple ⚠️ | Saint-Romans-lès-Melle › Mellois en Poitou | 1 |
| Forêt de Plaine-et-Vallées (32) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Bois de Nanteuil ⚠️ | Nanteuil › Haut Val de Sèvre | 1 |
| Bois de Nanteuil (2) ⚠️ | Nanteuil › Haut Val de Sèvre | 1 |
| Bois de Luzay ⚠️ | Luzay › Thouarsais | 1 |
| Bois Morat ⚠️ | Melle › Mellois en Poitou | 1 |
| La Prée ⚠️ | Parthenay › Parthenay-Gâtine | 1 |
| Forêt de Aiffres ⚠️ | Aiffres › Niortais | 1 |
| Forêt de Mazières-en-Gâtine (13) ⚠️ | Mazières-en-Gâtine › Val de Gâtine | 1 |
| Forêt de Mazières-en-Gâtine (14) ⚠️ | Mazières-en-Gâtine › Val de Gâtine | 1 |
| Forêt de Saint-Christophe-sur-Roc (3) ⚠️ | Saint-Christophe-sur-Roc › Val de Gâtine | 1 |
| Forêt de Saint-Christophe-sur-Roc (6) ⚠️ | Saint-Christophe-sur-Roc › Val de Gâtine | 1 |
| Bois de La Crèche ⚠️ | La Crèche › Haut Val de Sèvre | 1 |
| Bois de La Crèche (5) ⚠️ | La Crèche › Haut Val de Sèvre | 1 |
| Bois de Bressuire (117) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Bressuire (118) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Bressuire (119) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Forêt de Coulonges-sur-l'Autize (2) ⚠️ | Coulonges-sur-l'Autize › Val de Gâtine | 1 |
| Forêt de Aiffres (8) ⚠️ | Aiffres › Niortais | 1 |
| Forêt du Retail ⚠️ | Le Retail › Parthenay-Gâtine | 1 |
| Bois de Courlay (3) ⚠️ | Courlay › Bocage Bressuirais | 1 |
| Forêt de Saint-Symphorien (3) ⚠️ | Saint-Symphorien › Niortais | 1 |
| Forêt de Niort (24) ⚠️ | Niort › Niortais | 1 |
| Bois de Saint-Marc-la-Lande (2) ⚠️ | Saint-Marc-la-Lande › Val de Gâtine | 1 |
| Bois de Mauléon (9) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Forêt de Fomperron (8) ⚠️ | Fomperron › Parthenay-Gâtine | 1 |
| Bois de Rom ⚠️ | Rom › Mellois en Poitou | 1 |
| Bois de Rom (2) ⚠️ | Rom › Mellois en Poitou | 1 |
| Bois de La Forêt-sur-Sèvre (2) ⚠️ | La Forêt-sur-Sèvre › Bocage Bressuirais | 1 |
| Forêt de Assais-les-Jumeaux (3) ⚠️ | Assais-les-Jumeaux › Airvaudais-Val du Thouet | 1 |
| Forêt de Assais-les-Jumeaux (4) ⚠️ | Assais-les-Jumeaux › Airvaudais-Val du Thouet | 1 |
| Forêt de Assais-les-Jumeaux (6) ⚠️ | Assais-les-Jumeaux › Airvaudais-Val du Thouet | 1 |
| Forêt de Assais-les-Jumeaux (14) ⚠️ | Assais-les-Jumeaux › Airvaudais-Val du Thouet | 1 |
| Forêt de Assais-les-Jumeaux (15) ⚠️ | Assais-les-Jumeaux › Airvaudais-Val du Thouet | 1 |
| Forêt de Assais-les-Jumeaux (16) ⚠️ | Assais-les-Jumeaux › Airvaudais-Val du Thouet | 1 |
| Forêt de Assais-les-Jumeaux (20) ⚠️ | Assais-les-Jumeaux › Airvaudais-Val du Thouet | 1 |
| Forêt de Assais-les-Jumeaux (23) ⚠️ | Assais-les-Jumeaux › Airvaudais-Val du Thouet | 1 |
| Forêt de Assais-les-Jumeaux (24) ⚠️ | Assais-les-Jumeaux › Airvaudais-Val du Thouet | 1 |
| Forêt de Assais-les-Jumeaux (25) ⚠️ | Assais-les-Jumeaux › Airvaudais-Val du Thouet | 1 |
| Forêt de Assais-les-Jumeaux (26) ⚠️ | Assais-les-Jumeaux › Airvaudais-Val du Thouet | 1 |
| Forêt de Assais-les-Jumeaux (27) ⚠️ | Assais-les-Jumeaux › Airvaudais-Val du Thouet | 1 |
| Forêt de Assais-les-Jumeaux (30) ⚠️ | Assais-les-Jumeaux › Airvaudais-Val du Thouet | 1 |
| Forêt de Assais-les-Jumeaux (34) ⚠️ | Assais-les-Jumeaux › Airvaudais-Val du Thouet | 1 |
| Forêt de Saint-Loup-Lamairé (10) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 1 |
| Forêt de Saint-Loup-Lamairé (15) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 1 |
| Forêt de Saint-Loup-Lamairé (18) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 1 |
| Forêt de Saint-Loup-Lamairé (23) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 1 |
| Forêt de Saint-Loup-Lamairé (24) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 1 |
| Bois de Mauléon (16) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois de Cirières (4) ⚠️ | Cirières › Bocage Bressuirais | 1 |
| Bois de Cirières (5) ⚠️ | Cirières › Bocage Bressuirais | 1 |
| Bois de Cirières (6) ⚠️ | Cirières › Bocage Bressuirais | 1 |
| Forêt de Availles-Thouarsais (8) ⚠️ | Availles-Thouarsais › Airvaudais-Val du Thouet | 1 |
| Forêt de Availles-Thouarsais (10) ⚠️ | Availles-Thouarsais › Airvaudais-Val du Thouet | 1 |
| Bois de Bressuire (126) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Bressuire (134) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Bressuire (135) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Forêt de Plaine-et-Vallées (33) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Forêt de Plaine-et-Vallées (39) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Forêt de Assais-les-Jumeaux (35) ⚠️ | Assais-les-Jumeaux › Airvaudais-Val du Thouet | 1 |
| Forêt de Doux (15) ⚠️ | Doux › Parthenay-Gâtine | 1 |
| Forêt de Saint-Loup-Lamairé (28) ⚠️ | Le Chillou › Airvaudais-Val du Thouet | 1 |
| Forêt de Pressigny ⚠️ | Pressigny › Parthenay-Gâtine | 1 |
| Forêt de Pressigny (4) ⚠️ | Pressigny › Parthenay-Gâtine | 1 |
| Forêt de Saint-Loup-Lamairé (31) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 1 |
| Forêt de Aubigny (3) ⚠️ | Aubigny › Parthenay-Gâtine | 1 |
| Forêt de Aubigny (4) ⚠️ | Aubigny › Parthenay-Gâtine | 1 |
| Forêt de Aubigny (6) ⚠️ | Aubigny › Parthenay-Gâtine | 1 |
| Forêt de Thénezay (28) ⚠️ | Thénezay › Parthenay-Gâtine | 1 |
| Forêt de Thénezay (29) ⚠️ | Thénezay › Parthenay-Gâtine | 1 |
| Forêt de Thénezay (30) ⚠️ | Thénezay › Parthenay-Gâtine | 1 |
| Forêt de Thénezay (31) ⚠️ | Thénezay › Parthenay-Gâtine | 1 |
| Forêt de Aubigny (8) ⚠️ | Aubigny › Parthenay-Gâtine | 1 |
| Forêt de Thénezay (34) ⚠️ | Thénezay › Parthenay-Gâtine | 1 |
| Forêt de Thénezay (35) ⚠️ | Thénezay › Parthenay-Gâtine | 1 |
| Forêt de Thénezay (39) ⚠️ | Thénezay › Parthenay-Gâtine | 1 |
| Forêt de Thénezay (47) ⚠️ | Thénezay › Parthenay-Gâtine | 1 |
| Forêt de Thénezay (50) ⚠️ | Thénezay › Parthenay-Gâtine | 1 |
| Forêt de Thénezay (53) ⚠️ | Thénezay › Parthenay-Gâtine | 1 |
| Forêt de Gourgé (6) ⚠️ | Gourgé › Parthenay-Gâtine | 1 |
| Forêt de Oroux (2) ⚠️ | Oroux › Parthenay-Gâtine | 1 |
| Forêt de Airvault (68) ⚠️ | Airvault › Airvaudais-Val du Thouet | 1 |
| Forêt de Airvault (70) ⚠️ | Airvault › Airvaudais-Val du Thouet | 1 |
| Forêt de Airvault (71) ⚠️ | Airvault › Airvaudais-Val du Thouet | 1 |
| Forêt de Plaine-et-Vallées (45) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Forêt de Plaine-et-Vallées (46) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Bois de Ardin ⚠️ | Ardin › Val de Gâtine | 1 |
| Forêt de Saint-Varent (11) ⚠️ | Saint-Varent › Thouarsais | 1 |
| Bois de Ardin (4) ⚠️ | Ardin › Val de Gâtine | 1 |
| Forêt de Airvault (74) ⚠️ | Airvault › Airvaudais-Val du Thouet | 1 |
| Forêt de Airvault (76) ⚠️ | Airvault › Airvaudais-Val du Thouet | 1 |
| Forêt de Airvault (77) ⚠️ | Airvault › Airvaudais-Val du Thouet | 1 |
| Forêt de La Chapelle-Pouilloux (3) ⚠️ | La Chapelle-Pouilloux › Mellois en Poitou | 1 |
| Forêt de Sauzé-entre-Bois (23) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Forêt de Vanzay (2) ⚠️ | Vanzay › Mellois en Poitou | 1 |
| Forêt de Sauzé-entre-Bois (24) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Forêt de Sauzé-entre-Bois (26) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Bois de Rom (6) ⚠️ | Rom › Mellois en Poitou | 1 |
| Bois de Rom (9) ⚠️ | Rom › Mellois en Poitou | 1 |
| Bois de Rom (11) ⚠️ | Rom › Mellois en Poitou | 1 |
| Bois de Rom (13) ⚠️ | Rom › Mellois en Poitou | 1 |
| Bois de Rom (14) ⚠️ | Rom › Mellois en Poitou | 1 |
| Bois de Rom (16) ⚠️ | Rom › Mellois en Poitou | 1 |
| Petit Bois ⚠️ | Rom › Mellois en Poitou | 1 |
| Bois de Rom (20) ⚠️ | Rom › Mellois en Poitou | 1 |
| Bois de Melle (2) ⚠️ | Melle › Mellois en Poitou | 1 |
| Forêt de Limalonges (22) ⚠️ | Limalonges › Mellois en Poitou | 1 |
| Forêt de Limalonges (23) ⚠️ | Limalonges › Mellois en Poitou | 1 |
| Forêt de Sauzé-entre-Bois (34) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Forêt de Limalonges (30) ⚠️ | Limalonges › Mellois en Poitou | 1 |
| Forêt de Limalonges (33) ⚠️ | Limalonges › Mellois en Poitou | 1 |
| Forêt de Limalonges (34) ⚠️ | Limalonges › Mellois en Poitou | 1 |
| Forêt de Limalonges (35) ⚠️ | Limalonges › Mellois en Poitou | 1 |
| Forêt de Limalonges (38) ⚠️ | Limalonges › Mellois en Poitou | 1 |
| Forêt de Limalonges (41) ⚠️ | Limalonges › Mellois en Poitou | 1 |
| Forêt de Limalonges (42) ⚠️ | Limalonges › Mellois en Poitou | 1 |
| Forêt de Limalonges (47) ⚠️ | Limalonges › Mellois en Poitou | 1 |
| Forêt de Limalonges (50) ⚠️ | Limalonges › Mellois en Poitou | 1 |
| Forêt de Limalonges (52) ⚠️ | Limalonges › Mellois en Poitou | 1 |
| Forêt de Limalonges (56) ⚠️ | Limalonges › Mellois en Poitou | 1 |
| Forêt de Thénezay (57) ⚠️ | Thénezay › Parthenay-Gâtine | 1 |
| Forêt de Thénezay (58) ⚠️ | Thénezay › Parthenay-Gâtine | 1 |
| Forêt de Ardin ⚠️ | Ardin › Val de Gâtine | 1 |
| Port Boinot ⚠️ | Niort › Niortais | 1 |
| Forêt de Chenay (5) ⚠️ | Chenay › Mellois en Poitou | 1 |
| Forêt de Saint-Loup-Lamairé (37) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 1 |
| Forêt de La Peyratte (13) ⚠️ | La Peyratte › Parthenay-Gâtine | 1 |
| Forêt de La Peyratte (15) ⚠️ | La Peyratte › Parthenay-Gâtine | 1 |
| Forêt de La Peyratte (18) ⚠️ | La Peyratte › Parthenay-Gâtine | 1 |
| Forêt de Mauléon (14) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Forêt de La Chapelle-Bertrand (3) ⚠️ | La Chapelle-Bertrand › Parthenay-Gâtine | 1 |
| Forêt de La Chapelle-Bertrand (5) ⚠️ | La Chapelle-Bertrand › Parthenay-Gâtine | 1 |
| Forêt de La Chapelle-Bertrand (9) ⚠️ | La Chapelle-Bertrand › Parthenay-Gâtine | 1 |
| Forêt de La Peyratte (21) ⚠️ | La Peyratte › Parthenay-Gâtine | 1 |
| Parc Camille RICHARD ⚠️ | Niort › Niortais | 1 |
| Forêt de Viennay (5) ⚠️ | Viennay › Parthenay-Gâtine | 1 |
| Forêt de Gourgé (9) ⚠️ | Gourgé › Parthenay-Gâtine | 1 |
| Forêt de Viennay (6) ⚠️ | Viennay › Parthenay-Gâtine | 1 |
| Forêt de Gourgé (11) ⚠️ | Gourgé › Parthenay-Gâtine | 1 |
| Forêt de La Peyratte (23) ⚠️ | La Peyratte › Parthenay-Gâtine | 1 |
| Forêt de Azay-sur-Thouet (5) ⚠️ | Azay-sur-Thouet › Parthenay-Gâtine | 1 |
| Forêt de Gourgé (13) ⚠️ | Gourgé › Parthenay-Gâtine | 1 |
| Forêt de Azay-sur-Thouet (7) ⚠️ | Azay-sur-Thouet › Parthenay-Gâtine | 1 |
| Forêt de Saint-Maixent-l'École (2) ⚠️ | Saint-Maixent-l'École › Haut Val de Sèvre | 1 |
| Bois de Exireuil ⚠️ | Exireuil › Haut Val de Sèvre | 1 |
| Forêt de Saivres (8) ⚠️ | Saivres › Haut Val de Sèvre | 1 |
| Forêt de Saivres (9) ⚠️ | Saivres › Haut Val de Sèvre | 1 |
| Forêt de Saivres (13) ⚠️ | Saivres › Haut Val de Sèvre | 1 |
| Forêt de Azay-le-Brûlé (12) ⚠️ | Azay-le-Brûlé › Haut Val de Sèvre | 1 |
| Forêt de Saivres (19) ⚠️ | Saivres › Haut Val de Sèvre | 1 |
| Forêt de Azay-le-Brûlé (17) ⚠️ | Azay-le-Brûlé › Haut Val de Sèvre | 1 |
| Forêt de Azay-le-Brûlé (18) ⚠️ | Azay-le-Brûlé › Haut Val de Sèvre | 1 |
| Forêt de Azay-le-Brûlé (19) ⚠️ | Azay-le-Brûlé › Haut Val de Sèvre | 1 |
| Forêt de Azay-le-Brûlé (23) ⚠️ | Azay-le-Brûlé › Haut Val de Sèvre | 1 |
| Parc de Niort (9) ⚠️ | Niort › Niortais | 1 |
| Forêt de Airvault (79) ⚠️ | Airvault › Airvaudais-Val du Thouet | 1 |
| Forêt de Airvault (80) ⚠️ | Airvault › Airvaudais-Val du Thouet | 1 |
| Forêt de Airvault (82) ⚠️ | Airvault › Airvaudais-Val du Thouet | 1 |
| Place du Champ de Foire ⚠️ | Saint-Georges-de-Rex › Niortais | 1 |
| Forêt de La Peyratte (24) ⚠️ | La Peyratte › Parthenay-Gâtine | 1 |
| Forêt de Saint-Martin-du-Fouilloux (5) ⚠️ | Saint-Martin-du-Fouilloux › Parthenay-Gâtine | 1 |
| Forêt de Saurais (3) ⚠️ | Saurais › Parthenay-Gâtine | 1 |
| Forêt de La Chapelle-Bertrand (11) ⚠️ | La Chapelle-Bertrand › Parthenay-Gâtine | 1 |
| Bois de Coulonges-sur-l'Autize (3) ⚠️ | Coulonges-sur-l'Autize › Val de Gâtine | 1 |
| Bois de Coulonges-sur-l'Autize (6) ⚠️ | Coulonges-sur-l'Autize › Val de Gâtine | 1 |
| Forêt de Viennay (7) ⚠️ | Viennay › Parthenay-Gâtine | 1 |
| Forêt de Gourgé (15) ⚠️ | Gourgé › Parthenay-Gâtine | 1 |
| Forêt de Gourgé (16) ⚠️ | Gourgé › Parthenay-Gâtine | 1 |
| Forêt de Gourgé (22) ⚠️ | Gourgé › Parthenay-Gâtine | 1 |
| Forêt de Gourgé (23) ⚠️ | Gourgé › Parthenay-Gâtine | 1 |
| Forêt de Gourgé (26) ⚠️ | Gourgé › Parthenay-Gâtine | 1 |
| Forêt de Vernoux-en-Gâtine (7) ⚠️ | Vernoux-en-Gâtine › Parthenay-Gâtine | 1 |
| Forêt de Vernoux-en-Gâtine (11) ⚠️ | Vernoux-en-Gâtine › Parthenay-Gâtine | 1 |
| Forêt de Lhoumois (13) ⚠️ | Lhoumois › Parthenay-Gâtine | 1 |
| Forêt de Cerizay (6) ⚠️ | Cerizay › Bocage Bressuirais | 1 |
| Forêt de Cerizay (7) ⚠️ | Cerizay › Bocage Bressuirais | 1 |
| Forêt de Cerizay (8) ⚠️ | Cerizay › Bocage Bressuirais | 1 |
| Forêt de Cerizay (15) ⚠️ | Cerizay › Bocage Bressuirais | 1 |
| Forêt de Cerizay (16) ⚠️ | Cerizay › Bocage Bressuirais | 1 |
| Forêt du Chillou (6) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 1 |
| Forêt de Marnes (24) ⚠️ | Marnes › Thouarsais | 1 |
| Forêt de Marnes (27) ⚠️ | Marnes › Thouarsais | 1 |
| Forêt de Marnes (28) ⚠️ | Marnes › Thouarsais | 1 |
| Forêt de Mauzé-sur-le-Mignon (6) ⚠️ | Mauzé-sur-le-Mignon › Niortais | 1 |
| Forêt du Chillou (8) ⚠️ | Le Chillou › Airvaudais-Val du Thouet | 1 |
| Forêt de Thouars (21) ⚠️ | Thouars › Thouarsais | 1 |
| Bois de Aiffres (3) ⚠️ | Aiffres › Niortais | 1 |
| Bois de Val-du-Mignon (3) ⚠️ | Val-du-Mignon › Niortais | 1 |
| Forêt de Niort (26) ⚠️ | Niort › Niortais | 1 |
| Forêt de Saint-Loup-Lamairé (44) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 1 |
| Forêt de Saint-Loup-Lamairé (46) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 1 |
| Forêt de Saint-Loup-Lamairé (47) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 1 |
| Forêt de Saint-Loup-Lamairé (50) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 1 |
| Forêt de Saint-Loup-Lamairé (51) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 1 |
| Forêt de Saint-Loup-Lamairé (53) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 1 |
| Forêt de Airvault (88) ⚠️ | Airvault › Airvaudais-Val du Thouet | 1 |
| Forêt de Beugnon-Thireuil (10) ⚠️ | Beugnon-Thireuil › Val de Gâtine | 1 |
| Forêt de Saint-Martin-du-Fouilloux (6) ⚠️ | Saint-Martin-du-Fouilloux › Parthenay-Gâtine | 1 |
| Forêt de Saint-Martin-du-Fouilloux (9) ⚠️ | Saint-Martin-du-Fouilloux › Parthenay-Gâtine | 1 |
| Forêt de La Chapelle-Bertrand (12) ⚠️ | La Chapelle-Bertrand › Parthenay-Gâtine | 1 |
| Forêt de Vasles (32) ⚠️ | Vasles › Parthenay-Gâtine | 1 |
| Forêt de Vasles (34) ⚠️ | Vasles › Parthenay-Gâtine | 1 |
| Forêt de Vasles (35) ⚠️ | Vasles › Parthenay-Gâtine | 1 |
| Forêt de Vasles (38) ⚠️ | Vasles › Parthenay-Gâtine | 1 |
| Forêt de Parthenay (4) ⚠️ | Parthenay › Parthenay-Gâtine | 1 |
| Forêt de Rom (9) ⚠️ | Rom › Mellois en Poitou | 1 |
| Forêt de Vouhé (3) ⚠️ | Vouhé › Val de Gâtine | 1 |
| Bois de Saint-Martin-de-Sanzay (2) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 1 |
| Parc de la mairie ⚠️ | Saint-Symphorien › Niortais | 1 |
| Forêt de Maisontiers (7) ⚠️ | Maisontiers › Airvaudais-Val du Thouet | 1 |
| Forêt de Maisontiers (9) ⚠️ | Maisontiers › Airvaudais-Val du Thouet | 1 |
| Forêt de Saint-André-sur-Sèvre ⚠️ | Saint-André-sur-Sèvre › Bocage Bressuirais | 1 |
| Forêt de Saint-André-sur-Sèvre (2) ⚠️ | Saint-André-sur-Sèvre › Bocage Bressuirais | 1 |
| Bois de Loretz-d'Argenton (3) ⚠️ | Loretz-d'Argenton › Thouarsais | 1 |
| Bois de Loretz-d'Argenton (5) ⚠️ | Loretz-d'Argenton › Thouarsais | 1 |
| Bois de Saint-Martin-de-Sanzay (4) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 1 |
| Forêt de Niort (35) ⚠️ | Niort › Niortais | 1 |
| Forêt de Chef-Boutonne (7) ⚠️ | Chef-Boutonne › Mellois en Poitou | 1 |
| Forêt de Niort (54) ⚠️ | Niort › Niortais | 1 |
| Parc de Niort (13) ⚠️ | Niort › Niortais | 1 |
| Forêt de Niort (63) ⚠️ | Niort › Niortais | 1 |
| Forêt de Niort (68) ⚠️ | Niort › Niortais | 1 |
| Forêt de Limalonges (60) ⚠️ | Limalonges › Mellois en Poitou | 1 |
| Forêt de Niort (71) ⚠️ | Niort › Niortais | 1 |
| Forêt de Chef-Boutonne (8) ⚠️ | Chef-Boutonne › Mellois en Poitou | 1 |
| Forêt de Chef-Boutonne (9) ⚠️ | Chef-Boutonne › Mellois en Poitou | 1 |
| Forêt de Chef-Boutonne (10) ⚠️ | Chef-Boutonne › Mellois en Poitou | 1 |
| Forêt de Niort (75) ⚠️ | Niort › Niortais | 1 |
| Forêt de Saint-Léger-de-Montbrun (27) ⚠️ | Saint-Léger-de-Montbrun › Thouarsais | 1 |
| Forêt de Ensigné (2) ⚠️ | Ensigné › Mellois en Poitou | 1 |
| Forêt de Asnières-en-Poitou (13) ⚠️ | Asnières-en-Poitou › Mellois en Poitou | 1 |
| Forêt de Saint-Léger-de-Montbrun (34) ⚠️ | Saint-Léger-de-Montbrun › Thouarsais | 1 |
| Forêt de Saint-Léger-de-Montbrun (37) ⚠️ | Saint-Léger-de-Montbrun › Thouarsais | 1 |
| Bois de Bressuire (149) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Forêt de Bressuire (25) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Forêt du Vanneau-Irleau (9) ⚠️ | Le Vanneau-Irleau › Niortais | 1 |
| Forêt du Vanneau-Irleau (10) ⚠️ | Le Vanneau-Irleau › Niortais | 1 |
| Forêt du Vanneau-Irleau (16) ⚠️ | Le Vanneau-Irleau › Niortais | 1 |
| Forêt du Vanneau-Irleau (17) ⚠️ | Le Vanneau-Irleau › Niortais | 1 |
| Forêt du Vanneau-Irleau (21) ⚠️ | Le Vanneau-Irleau › Niortais | 1 |
| Forêt de Coulon (31) ⚠️ | Coulon › Niortais | 1 |
| Forêt de Coulon (35) ⚠️ | Coulon › Niortais | 1 |
| Forêt de Arçais (15) ⚠️ | Arçais › Niortais | 1 |
| Forêt de Airvault (94) ⚠️ | Airvault › Airvaudais-Val du Thouet | 1 |
| Forêt de Niort (78) ⚠️ | Niort › Niortais | 1 |
| Forêt de Niort (79) ⚠️ | Niort › Niortais | 1 |
| Forêt de Aiffres (18) ⚠️ | Saint-Symphorien › Niortais | 1 |
| Forêt de Niort (82) ⚠️ | Niort › Niortais | 1 |
| Forêt de Aiffres (23) ⚠️ | Aiffres › Niortais | 1 |
| Forêt de Aiffres (24) ⚠️ | Aiffres › Niortais | 1 |
| Forêt de Rom (10) ⚠️ | Rom › Mellois en Poitou | 1 |
| Forêt de Coulonges-sur-l'Autize (3) ⚠️ | Coulonges-sur-l'Autize › Val de Gâtine | 1 |
| Forêt de Niort (86) ⚠️ | Niort › Niortais | 1 |
| Forêt de Niort (89) ⚠️ | Niort › Niortais | 1 |
| Forêt de Frontenay-Rohan-Rohan (8) ⚠️ | Frontenay-Rohan-Rohan › Niortais | 1 |
| Forêt de Saint-Rémy ⚠️ | Saint-Rémy › Niortais | 1 |
| Forêt de Niort (92) ⚠️ | Niort › Niortais | 1 |
| Forêt de Saint-Rémy (4) ⚠️ | Niort › Niortais | 1 |
| Forêt de Aiffres (30) ⚠️ | Aiffres › Niortais | 1 |
| Forêt de Vouillé (11) ⚠️ | Vouillé › Niortais | 1 |
| Forêt de Vouillé (16) ⚠️ | Vouillé › Niortais | 1 |
| Forêt de Aiffres (33) ⚠️ | Aiffres › Niortais | 1 |
| Forêt de Sauzé-entre-Bois (37) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Forêt de Sauzé-entre-Bois (39) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Forêt de Sauzé-entre-Bois (40) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Forêt de Sauzé-entre-Bois (41) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Forêt de Sauzé-entre-Bois (46) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Forêt de Fors (5) ⚠️ | Fors › Niortais | 1 |
| Forêt de Fors (6) ⚠️ | Fors › Niortais | 1 |
| Forêt de Niort (94) ⚠️ | Niort › Niortais | 1 |
| Forêt de Saint-Symphorien (17) ⚠️ | Saint-Symphorien › Niortais | 1 |
| Forêt de Niort (104) ⚠️ | Niort › Niortais | 1 |
| Forêt de Bessines (10) ⚠️ | Bessines › Niortais | 1 |
| Bois de Granzay-Gript (4) ⚠️ | Granzay-Gript › Niortais | 1 |
| Bois de Granzay-Gript (9) ⚠️ | Granzay-Gript › Niortais | 1 |
| Forêt de Soudan (6) ⚠️ | Soudan › Haut Val de Sèvre | 1 |
| Forêt de Prahecq (2) ⚠️ | Prahecq › Niortais | 1 |
| Forêt de Niort (112) ⚠️ | Niort › Niortais | 1 |
| Forêt de Airvault (101) ⚠️ | Airvault › Airvaudais-Val du Thouet | 1 |
| Forêt de Arçais (19) ⚠️ | Arçais › Niortais | 1 |
| Forêt de Saint-Hilaire-la-Palud (34) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 1 |
| Forêt de Saint-Hilaire-la-Palud (35) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 1 |
| Forêt de Saint-Hilaire-la-Palud (38) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 1 |
| Forêt de Saint-Hilaire-la-Palud (39) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 1 |
| Forêt de Saint-Hilaire-la-Palud (40) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 1 |
| Forêt de Saint-Hilaire-la-Palud (43) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 1 |
| Forêt de Saint-Hilaire-la-Palud (45) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 1 |
| Forêt de Arçais (23) ⚠️ | Arçais › Niortais | 1 |
| Forêt de Saint-Hilaire-la-Palud (47) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 1 |
| Forêt de Saint-Hilaire-la-Palud (49) ⚠️ | Saint-Hilaire-la-Palud › Niortais | 1 |
| Forêt de Arçais (25) ⚠️ | Arçais › Niortais | 1 |
| Forêt de Alloinay (17) ⚠️ | Alloinay › Mellois en Poitou | 1 |
| Forêt de Alloinay (18) ⚠️ | Alloinay › Mellois en Poitou | 1 |
| Bois de Plaine-et-Vallées (13) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Forêt de Alloinay (28) ⚠️ | Alloinay › Mellois en Poitou | 1 |
| Forêt de Alloinay (30) ⚠️ | Alloinay › Mellois en Poitou | 1 |
| Forêt de Alloinay (31) ⚠️ | Alloinay › Mellois en Poitou | 1 |
| Forêt de Alloinay (32) ⚠️ | Alloinay › Mellois en Poitou | 1 |
| Forêt de Alloinay (35) ⚠️ | Alloinay › Mellois en Poitou | 1 |
| Forêt de Alloinay (36) ⚠️ | Alloinay › Mellois en Poitou | 1 |
| Bois de Mauzé-sur-le-Mignon ⚠️ | Mauzé-sur-le-Mignon › Niortais | 1 |
| Forêt de Saint-Pompain (3) ⚠️ | Saint-Pompain › Val de Gâtine | 1 |
| Forêt de Scillé (3) ⚠️ | Scillé › Val de Gâtine | 1 |
| Forêt du Busseau (12) ⚠️ | Le Busseau › Val de Gâtine | 1 |
| Station de la Jeannerie ⚠️ | Le Bourdet › Niortais | 1 |
| Bois de Pamproux ⚠️ | Pamproux › Haut Val de Sèvre | 1 |
| Bois de La Chapelle-Pouilloux ⚠️ | La Chapelle-Pouilloux › Mellois en Poitou | 1 |
| Bois de Mairé-Levescault (3) ⚠️ | Mairé-Levescault › Mellois en Poitou | 1 |
| Forêt de Chizé (12) ⚠️ | Chizé › Mellois en Poitou | 1 |
| Forêt de Chizé (14) ⚠️ | Chizé › Mellois en Poitou | 1 |
| Forêt de Chizé (15) ⚠️ | Chizé › Mellois en Poitou | 1 |
| Forêt de Chizé (21) ⚠️ | Chizé › Mellois en Poitou | 1 |
| Forêt de Chizé (22) ⚠️ | Chizé › Mellois en Poitou | 1 |
| Forêt de Chizé (23) ⚠️ | Chizé › Mellois en Poitou | 1 |
| Forêt de Chizé (24) ⚠️ | Chizé › Mellois en Poitou | 1 |
| Forêt de Sainte-Ouenne ⚠️ | Sainte-Ouenne › Val de Gâtine | 1 |
| Forêt de Surin (2) ⚠️ | Surin › Val de Gâtine | 1 |
| Forêt de Surin (3) ⚠️ | Surin › Val de Gâtine | 1 |
| Bois de Saint-Amand-sur-Sèvre (3) ⚠️ | Saint-Amand-sur-Sèvre › Bocage Bressuirais | 1 |
| Forêt de Germond-Rouvre (4) ⚠️ | Germond-Rouvre › Niortais | 1 |
| Forêt de Saint-Martin-de-Sanzay (7) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 1 |
| Forêt de Saint-Martin-de-Sanzay (10) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 1 |
| Forêt de Saint-Martin-de-Sanzay (12) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 1 |
| Forêt de Saint-Martin-de-Sanzay (13) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 1 |
| Forêt de Saint-Martin-de-Sanzay (16) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 1 |
| Forêt de Saint-Martin-de-Sanzay (17) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 1 |
| Forêt de Saint-Martin-de-Sanzay (24) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 1 |
| Forêt de Saint-Martin-de-Sanzay (25) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 1 |
| Forêt de Saint-Martin-de-Sanzay (31) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 1 |
| Parc de Thouars (2) ⚠️ | Thouars › Thouarsais | 1 |
| Forêt de Luché-Thouarsais (2) ⚠️ | Luché-Thouarsais › Thouarsais | 1 |
| Forêt de Luché-Thouarsais (3) ⚠️ | Luché-Thouarsais › Thouarsais | 1 |
| Forêt de Luché-Thouarsais (4) ⚠️ | Luché-Thouarsais › Thouarsais | 1 |
| Forêt de Saint-Loup-Lamairé (58) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 1 |
| Forêt de Saint-Loup-Lamairé (60) ⚠️ | Saint-Loup-Lamairé › Airvaudais-Val du Thouet | 1 |
| Forêt de Aiffres (38) ⚠️ | Aiffres › Niortais | 1 |
| Forêt de Germond-Rouvre (6) ⚠️ | Germond-Rouvre › Niortais | 1 |
| Forêt du Vanneau-Irleau (24) ⚠️ | Le Vanneau-Irleau › Niortais | 1 |
| Forêt du Vanneau-Irleau (25) ⚠️ | Le Vanneau-Irleau › Niortais | 1 |
| Forêt de Sansais (31) ⚠️ | Sansais › Niortais | 1 |
| Forêt de Rom (15) ⚠️ | Rom › Mellois en Poitou | 1 |
| Forêt de Béceleuf (2) ⚠️ | Béceleuf › Val de Gâtine | 1 |
| Forêt de Faye-sur-Ardin (4) ⚠️ | Faye-sur-Ardin › Val de Gâtine | 1 |
| Bois de Moncoutant-sur-Sèvre (6) ⚠️ | Moncoutant-sur-Sèvre › Bocage Bressuirais | 1 |
| Forêt de Lezay (18) ⚠️ | Lezay › Mellois en Poitou | 1 |
| Forêt de Sepvret (30) ⚠️ | Sepvret › Mellois en Poitou | 1 |
| Forêt de Bressuire (26) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Forêt de Celles-sur-Belle (27) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 1 |
| Forêt de Sansais (33) ⚠️ | Sansais › Niortais | 1 |
| Forêt de Bessines (13) ⚠️ | Bessines › Niortais | 1 |
| Parc de Bessines ⚠️ | Bessines › Niortais | 1 |
| Forêt de Magné (44) ⚠️ | Magné › Niortais | 1 |
| Bois de Champdeniers (2) ⚠️ | Champdeniers › Val de Gâtine | 1 |
| Bois de Glénay ⚠️ | Glénay › Thouarsais | 1 |
| Forêt de Glénay (13) ⚠️ | Glénay › Thouarsais | 1 |
| Forêt de Sauzé-entre-Bois (47) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Forêt de Louzy (9) ⚠️ | Louzy › Thouarsais | 1 |
| Forêt de Mairé-Levescault (17) ⚠️ | Mairé-Levescault › Mellois en Poitou | 1 |
| Bois de Brion-près-Thouet ⚠️ | Brion-près-Thouet › Thouarsais | 1 |
| Forêt de Châtillon-sur-Thouet (2) ⚠️ | Châtillon-sur-Thouet › Parthenay-Gâtine | 1 |
| Forêt de Parthenay (8) ⚠️ | Parthenay › Parthenay-Gâtine | 1 |
| Forêt de Parthenay (9) ⚠️ | Parthenay › Parthenay-Gâtine | 1 |
| Forêt de Parthenay (10) ⚠️ | Parthenay › Parthenay-Gâtine | 1 |
| Forêt de Parthenay (11) ⚠️ | Parthenay › Parthenay-Gâtine | 1 |
| Forêt de Parthenay (12) ⚠️ | Parthenay › Parthenay-Gâtine | 1 |
| Forêt de Parthenay (13) ⚠️ | Parthenay › Parthenay-Gâtine | 1 |
| Forêt de Parthenay (14) ⚠️ | Parthenay › Parthenay-Gâtine | 1 |
| Forêt de La Peyratte (28) ⚠️ | La Peyratte › Parthenay-Gâtine | 1 |
| Forêt de Sauzé-entre-Bois (51) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Bois de Vançais (3) ⚠️ | Vançais › Mellois en Poitou | 1 |
| Bois de Mauléon (17) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois de Plaine-et-Vallées (15) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Parc de Bressuire (29) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Sainte-Soline (3) ⚠️ | Sainte-Soline › Mellois en Poitou | 1 |
| Forêt de Coulon (37) ⚠️ | Coulon › Niortais | 1 |
| Forêt de Coulon (38) ⚠️ | Coulon › Niortais | 1 |
| Bois de Niort (38) ⚠️ | Niort › Niortais | 1 |
| Bois de Montravers (3) ⚠️ | Montravers › Bocage Bressuirais | 1 |
| Forêt de Chauray (3) ⚠️ | Chauray › Niortais | 1 |
| Forêt de Rom (20) ⚠️ | Rom › Mellois en Poitou | 1 |
| Bois de La Crèche (8) ⚠️ | La Crèche › Haut Val de Sèvre | 1 |
| Bois de La Crèche (9) ⚠️ | La Crèche › Haut Val de Sèvre | 1 |
| Bois de La Crèche (13) ⚠️ | La Crèche › Haut Val de Sèvre | 1 |
| Bois de Prahecq (4) ⚠️ | Prahecq › Niortais | 1 |
| Forêt de Sainte-Soline (20) ⚠️ | Sainte-Soline › Mellois en Poitou | 1 |
| Forêt de Messé (3) ⚠️ | Messé › Mellois en Poitou | 1 |
| Bois de Saint-Martin-de-Sanzay (8) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 1 |
| Bois de Loretz-d'Argenton (9) ⚠️ | Loretz-d'Argenton › Thouarsais | 1 |
| Bois de Saint-Martin-de-Sanzay (14) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 1 |
| Bois de Brion-près-Thouet (2) ⚠️ | Brion-près-Thouet › Thouarsais | 1 |
| Bois de Saint-Martin-de-Sanzay (15) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 1 |
| Bois de Saint-Martin-de-Sanzay (17) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 1 |
| Bois de Saint-Martin-de-Sanzay (19) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 1 |
| Forêt de Saint-Martin-de-Sanzay (35) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 1 |
| Bois de Saint-Martin-de-Sanzay (23) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 1 |
| Bois de Saint-Martin-de-Sanzay (24) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 1 |
| Bois de Saint-Cyr-la-Lande (4) ⚠️ | Saint-Cyr-la-Lande › Thouarsais | 1 |
| Bois de Brion-près-Thouet (4) ⚠️ | Brion-près-Thouet › Thouarsais | 1 |
| Bois de Brion-près-Thouet (5) ⚠️ | Brion-près-Thouet › Thouarsais | 1 |
| Bois de Saint-Martin-de-Sanzay (31) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 1 |
| Bois de Saint-Martin-de-Sanzay (32) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 1 |
| Bois de Saint-Martin-de-Sanzay (33) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 1 |
| Bois de Saint-Martin-de-Sanzay (34) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 1 |
| Forêt de Saint-Martin-de-Sanzay (42) ⚠️ | Saint-Martin-de-Sanzay › Thouarsais | 1 |
| Forêt de Tourtenay (8) ⚠️ | Tourtenay › Thouarsais | 1 |
| Bois de Saint-Cyr-la-Lande (12) ⚠️ | Saint-Cyr-la-Lande › Thouarsais | 1 |
| Bois de Saint-Cyr-la-Lande (17) ⚠️ | Saint-Cyr-la-Lande › Thouarsais | 1 |
| Bois de Saint-Cyr-la-Lande (29) ⚠️ | Saint-Cyr-la-Lande › Thouarsais | 1 |
| Bois de Saint-Cyr-la-Lande (32) ⚠️ | Saint-Cyr-la-Lande › Thouarsais | 1 |
| Bois de Saint-Cyr-la-Lande (37) ⚠️ | Saint-Cyr-la-Lande › Thouarsais | 1 |
| Bois de Thouars (3) ⚠️ | Thouars › Thouarsais | 1 |
| Forêt de Saint-Léger-de-Montbrun (40) ⚠️ | Saint-Léger-de-Montbrun › Thouarsais | 1 |
| Bois de Saint-Martin-de-Mâcon (7) ⚠️ | Saint-Martin-de-Mâcon › Thouarsais | 1 |
| Bois de Saint-Martin-de-Mâcon (8) ⚠️ | Saint-Martin-de-Mâcon › Thouarsais | 1 |
| Forêt de Saint-Martin-de-Mâcon (11) ⚠️ | Saint-Martin-de-Mâcon › Thouarsais | 1 |
| Bois de Plaine-et-Vallées (16) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Forêt de Thouars (22) ⚠️ | Thouars › Thouarsais | 1 |
| Bois de Thouars (7) ⚠️ | Thouars › Thouarsais | 1 |
| Forêt de Coulonges-Thouarsais (8) ⚠️ | Coulonges-Thouarsais › Thouarsais | 1 |
| Forêt de Coulonges-Thouarsais (10) ⚠️ | Coulonges-Thouarsais › Thouarsais | 1 |
| Forêt de Coulonges-Thouarsais (12) ⚠️ | Coulonges-Thouarsais › Thouarsais | 1 |
| Forêt de Thouars (28) ⚠️ | Thouars › Thouarsais | 1 |
| Forêt de Thouars (30) ⚠️ | Thouars › Thouarsais | 1 |
| Bois de Thouars (9) ⚠️ | Thouars › Thouarsais | 1 |
| Forêt de Thouars (31) ⚠️ | Thouars › Thouarsais | 1 |
| Bois de Thouars (13) ⚠️ | Thouars › Thouarsais | 1 |
| Forêt de Thouars (34) ⚠️ | Thouars › Thouarsais | 1 |
| Bois de Luzay (4) ⚠️ | Luzay › Thouarsais | 1 |
| Forêt de Thouars (35) ⚠️ | Thouars › Thouarsais | 1 |
| Bois de Thouars (19) ⚠️ | Thouars › Thouarsais | 1 |
| Bois de Saint-Jacques-de-Thouars ⚠️ | Saint-Jacques-de-Thouars › Thouarsais | 1 |
| Bois de Saint-Jacques-de-Thouars (2) ⚠️ | Saint-Jacques-de-Thouars › Thouarsais | 1 |
| Forêt de Saint-Jacques-de-Thouars (6) ⚠️ | Saint-Jacques-de-Thouars › Thouarsais | 1 |
| Forêt de Luzay (21) ⚠️ | Luzay › Thouarsais | 1 |
| Bois de Luzay (8) ⚠️ | Luzay › Thouarsais | 1 |
| Bois de Saint-Varent (5) ⚠️ | Saint-Varent › Thouarsais | 1 |
| Forêt de Saint-Varent (12) ⚠️ | Saint-Varent › Thouarsais | 1 |
| Forêt de Saint-Varent (13) ⚠️ | Saint-Varent › Thouarsais | 1 |
| Bois de Luzay (11) ⚠️ | Luzay › Thouarsais | 1 |
| Bois de Thouars (22) ⚠️ | Thouars › Thouarsais | 1 |
| Forêt de Thouars (40) ⚠️ | Thouars › Thouarsais | 1 |
| Forêt de Thouars (41) ⚠️ | Thouars › Thouarsais | 1 |
| Forêt de Thouars (42) ⚠️ | Thouars › Thouarsais | 1 |
| Forêt de Thouars (43) ⚠️ | Thouars › Thouarsais | 1 |
| Bois de Aigondigné (3) ⚠️ | Aigondigné › Mellois en Poitou | 1 |
| Bois de Luzay (12) ⚠️ | Luzay › Thouarsais | 1 |
| Forêt de Plaine-et-Vallées (50) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Forêt de Thouars (44) ⚠️ | Thouars › Thouarsais | 1 |
| Forêt de Thouars (46) ⚠️ | Thouars › Thouarsais | 1 |
| Forêt de Thouars (47) ⚠️ | Thouars › Thouarsais | 1 |
| Bois de Aigondigné (5) ⚠️ | Aigondigné › Mellois en Poitou | 1 |
| Bois de Availles-Thouarsais (3) ⚠️ | Availles-Thouarsais › Airvaudais-Val du Thouet | 1 |
| Forêt de Plaine-et-Vallées (51) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Bois de Plaine-et-Vallées (21) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Bois de Plaine-et-Vallées (24) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Forêt de Plaine-et-Vallées (54) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Bois de Saint-Varent (6) ⚠️ | Saint-Varent › Thouarsais | 1 |
| Bois de Plaine-et-Vallées (26) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Bois de Plaine-et-Vallées (27) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Bois de Saint-Généroux (5) ⚠️ | Saint-Généroux › Thouarsais | 1 |
| Forêt de Plaine-et-Vallées (60) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Bois de Plaine-et-Vallées (31) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Bois de Plaine-et-Vallées (34) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Forêt de Pas-de-Jeu (6) ⚠️ | Pas-de-Jeu › Thouarsais | 1 |
| Forêt de Pas-de-Jeu (7) ⚠️ | Pas-de-Jeu › Thouarsais | 1 |
| Bois de Pas-de-Jeu (3) ⚠️ | Pas-de-Jeu › Thouarsais | 1 |
| Bois de Pas-de-Jeu (4) ⚠️ | Pas-de-Jeu › Thouarsais | 1 |
| Bois de Assais-les-Jumeaux (4) ⚠️ | Assais-les-Jumeaux › Airvaudais-Val du Thouet | 1 |
| Forêt de Plaine-et-Vallées (62) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Forêt de Plaine-et-Vallées (63) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Bois de Plaine-et-Vallées (44) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Forêt de Plaine-et-Vallées (66) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Bois de Plaine-et-Vallées (46) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Bois de Pas-de-Jeu (9) ⚠️ | Pas-de-Jeu › Thouarsais | 1 |
| Bois de Pas-de-Jeu (10) ⚠️ | Pas-de-Jeu › Thouarsais | 1 |
| Forêt de Pas-de-Jeu (11) ⚠️ | Pas-de-Jeu › Thouarsais | 1 |
| Bois de Plaine-et-Vallées (52) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Bois de Plaine-et-Vallées (53) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Bois de Plaine-et-Vallées (56) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Bois de Plaine-et-Vallées (57) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Forêt de Pas-de-Jeu (14) ⚠️ | Pas-de-Jeu › Thouarsais | 1 |
| Forêt de Pas-de-Jeu (15) ⚠️ | Pas-de-Jeu › Thouarsais | 1 |
| Bois de Val en Vignes ⚠️ | Val en Vignes › Thouarsais | 1 |
| Forêt de Val en Vignes (16) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Bois de Val en Vignes (3) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Bois de Val en Vignes (5) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Bois de Val en Vignes (6) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Forêt de Thouars (54) ⚠️ | Thouars › Thouarsais | 1 |
| Bois de Thouars (42) ⚠️ | Thouars › Thouarsais | 1 |
| Bois de Loretz-d'Argenton (13) ⚠️ | Loretz-d'Argenton › Thouarsais | 1 |
| Bois de Thouars (45) ⚠️ | Thouars › Thouarsais | 1 |
| Forêt de Loretz-d'Argenton (8) ⚠️ | Loretz-d'Argenton › Thouarsais | 1 |
| Forêt de Loretz-d'Argenton (9) ⚠️ | Loretz-d'Argenton › Thouarsais | 1 |
| Forêt de Thouars (58) ⚠️ | Thouars › Thouarsais | 1 |
| Forêt de Thouars (60) ⚠️ | Thouars › Thouarsais | 1 |
| Bois de Sainte-Verge (8) ⚠️ | Sainte-Verge › Thouarsais | 1 |
| Bois de Sainte-Verge (12) ⚠️ | Sainte-Verge › Thouarsais | 1 |
| Bois de Sainte-Verge (13) ⚠️ | Sainte-Verge › Thouarsais | 1 |
| Bois de Sainte-Verge (14) ⚠️ | Sainte-Verge › Thouarsais | 1 |
| Forêt de Sainte-Verge (3) ⚠️ | Sainte-Verge › Thouarsais | 1 |
| Bois de Loretz-d'Argenton (15) ⚠️ | Loretz-d'Argenton › Thouarsais | 1 |
| Bois de Val en Vignes (8) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Bois de Val en Vignes (13) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Forêt de Val en Vignes (19) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Bois de Val en Vignes (24) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Forêt de Val en Vignes (22) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Bois de Val en Vignes (37) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Forêt de Val en Vignes (33) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Forêt de Val en Vignes (35) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Bois de Genneton ⚠️ | Genneton › Bocage Bressuirais | 1 |
| Bois de Val en Vignes (43) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Forêt de Val en Vignes (38) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Forêt de Val en Vignes (40) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Forêt de Thouars (62) ⚠️ | Thouars › Thouarsais | 1 |
| Bois de Thouars (51) ⚠️ | Thouars › Thouarsais | 1 |
| Forêt de Thouars (63) ⚠️ | Thouars › Thouarsais | 1 |
| Forêt de Val en Vignes (41) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Forêt de Val en Vignes (42) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Bois de Loretz-d'Argenton (20) ⚠️ | Loretz-d'Argenton › Thouarsais | 1 |
| Forêt de Loretz-d'Argenton (16) ⚠️ | Loretz-d'Argenton › Thouarsais | 1 |
| Bois de Loretz-d'Argenton (25) ⚠️ | Loretz-d'Argenton › Thouarsais | 1 |
| Bois de Loretz-d'Argenton (31) ⚠️ | Loretz-d'Argenton › Thouarsais | 1 |
| Forêt de Val en Vignes (47) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Bois de Val en Vignes (53) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Forêt de Loretz-d'Argenton (20) ⚠️ | Loretz-d'Argenton › Thouarsais | 1 |
| Forêt de Loretz-d'Argenton (21) ⚠️ | Loretz-d'Argenton › Thouarsais | 1 |
| Bois de Loretz-d'Argenton (38) ⚠️ | Loretz-d'Argenton › Thouarsais | 1 |
| Forêt de Loretz-d'Argenton (24) ⚠️ | Loretz-d'Argenton › Thouarsais | 1 |
| Bois de Loretz-d'Argenton (42) ⚠️ | Loretz-d'Argenton › Thouarsais | 1 |
| Forêt de Loretz-d'Argenton (26) ⚠️ | Loretz-d'Argenton › Thouarsais | 1 |
| Bois de Loretz-d'Argenton (43) ⚠️ | Loretz-d'Argenton › Thouarsais | 1 |
| Forêt de Fressines (5) ⚠️ | Fressines › Mellois en Poitou | 1 |
| Forêt de Fressines (9) ⚠️ | Fressines › Mellois en Poitou | 1 |
| Bois de Aigondigné (18) ⚠️ | Aigondigné › Mellois en Poitou | 1 |
| Bois de Val en Vignes (54) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Bois de Val en Vignes (57) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Forêt de Val en Vignes (48) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Forêt de Val en Vignes (49) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Bois de Val en Vignes (59) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Bois de Val en Vignes (63) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Bois de Val en Vignes (65) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Bois de Val en Vignes (67) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Forêt de Loretz-d'Argenton (32) ⚠️ | Loretz-d'Argenton › Thouarsais | 1 |
| Bois de Val en Vignes (75) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Bois de Val en Vignes (76) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Bois de Loretz-d'Argenton (61) ⚠️ | Loretz-d'Argenton › Thouarsais | 1 |
| Bois de Loretz-d'Argenton (63) ⚠️ | Loretz-d'Argenton › Thouarsais | 1 |
| Forêt de Genneton (3) ⚠️ | Genneton › Bocage Bressuirais | 1 |
| Bois de Genneton (7) ⚠️ | Genneton › Bocage Bressuirais | 1 |
| Bois de Genneton (11) ⚠️ | Genneton › Bocage Bressuirais | 1 |
| Bois de Saint Maurice Étusson ⚠️ | Saint Maurice Étusson › Bocage Bressuirais | 1 |
| Bois de Saint Maurice Étusson (2) ⚠️ | Saint Maurice Étusson › Bocage Bressuirais | 1 |
| Forêt de Saint Maurice Étusson (11) ⚠️ | Saint Maurice Étusson › Bocage Bressuirais | 1 |
| Bois de Saint Maurice Étusson (9) ⚠️ | Saint Maurice Étusson › Bocage Bressuirais | 1 |
| Bois de Loretz-d'Argenton (65) ⚠️ | Loretz-d'Argenton › Thouarsais | 1 |
| Bois de Loretz-d'Argenton (69) ⚠️ | Loretz-d'Argenton › Thouarsais | 1 |
| Bois de Loretz-d'Argenton (70) ⚠️ | Loretz-d'Argenton › Thouarsais | 1 |
| Bois de Val en Vignes (81) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Bois de Val en Vignes (82) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Bois de Argentonnay (63) ⚠️ | Argentonnay › Bocage Bressuirais | 1 |
| Bois de Argentonnay (64) ⚠️ | Argentonnay › Bocage Bressuirais | 1 |
| Bois de Argentonnay (67) ⚠️ | Argentonnay › Bocage Bressuirais | 1 |
| Bois de Voulmentin (17) ⚠️ | Voulmentin › Bocage Bressuirais | 1 |
| Bois de Argentonnay (70) ⚠️ | Argentonnay › Bocage Bressuirais | 1 |
| Bois de Argentonnay (71) ⚠️ | Argentonnay › Bocage Bressuirais | 1 |
| Bois de Argentonnay (82) ⚠️ | Argentonnay › Bocage Bressuirais | 1 |
| Bois de Argentonnay (83) ⚠️ | Argentonnay › Bocage Bressuirais | 1 |
| Forêt de Voulmentin (2) ⚠️ | Voulmentin › Bocage Bressuirais | 1 |
| Bois de Voulmentin (21) ⚠️ | Voulmentin › Bocage Bressuirais | 1 |
| Bois de Nueil-les-Aubiers (40) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Bois de Voulmentin (22) ⚠️ | Voulmentin › Bocage Bressuirais | 1 |
| Bois de Voulmentin (23) ⚠️ | Voulmentin › Bocage Bressuirais | 1 |
| Bois de Aiffres (4) ⚠️ | Aiffres › Niortais | 1 |
| Bois de Marigny (8) ⚠️ | Marigny › Niortais | 1 |
| Bois de Cerizay (3) ⚠️ | Cerizay › Bocage Bressuirais | 1 |
| Bois de Combrand (3) ⚠️ | Combrand › Bocage Bressuirais | 1 |
| Bois de Trayes (2) ⚠️ | Trayes › Bocage Bressuirais | 1 |
| Bois de Melle (3) ⚠️ | Melle › Mellois en Poitou | 1 |
| Forêt de Rom (21) ⚠️ | Rom › Mellois en Poitou | 1 |
| Bois de Louin (5) ⚠️ | Louin › Airvaudais-Val du Thouet | 1 |
| L'Îlot Vert ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Mauléon (19) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Forêt de Fenioux (37) ⚠️ | Fenioux › Val de Gâtine | 1 |
| Bois de Montravers (5) ⚠️ | Montravers › Bocage Bressuirais | 1 |
| Bois de Bressuire (154) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Saint-Aubin-du-Plain (10) ⚠️ | Saint-Aubin-du-Plain › Bocage Bressuirais | 1 |
| Bois de Bressuire (155) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Saint-Aubin-du-Plain (13) ⚠️ | Saint-Aubin-du-Plain › Bocage Bressuirais | 1 |
| Bois de Bressuire (159) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Parc du Logis ⚠️ | Frontenay-Rohan-Rohan › Niortais | 1 |
| Bois de Voulmentin (27) ⚠️ | Voulmentin › Bocage Bressuirais | 1 |
| Bois de Nueil-les-Aubiers (43) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Bois de Saint Maurice Étusson (13) ⚠️ | Saint Maurice Étusson › Bocage Bressuirais | 1 |
| Bois de Saint Maurice Étusson (14) ⚠️ | Saint Maurice Étusson › Bocage Bressuirais | 1 |
| Bois de Nueil-les-Aubiers (53) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Bois de Nueil-les-Aubiers (56) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Bois de Nueil-les-Aubiers (62) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Forêt de Nueil-les-Aubiers (10) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Bois de Nueil-les-Aubiers (68) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Forêt de Mauléon (18) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Parc à Teurtous ⚠️ | Vallans › Niortais | 1 |
| Bois de Bretignolles (18) ⚠️ | Bretignolles › Bocage Bressuirais | 1 |
| Bois de Bressuire (163) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois du Pin (2) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Bois de Nueil-les-Aubiers (89) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Bois de Nueil-les-Aubiers (91) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Bois de Nueil-les-Aubiers (92) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Bois de Nueil-les-Aubiers (98) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Bois de Nueil-les-Aubiers (108) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Bois de Nueil-les-Aubiers (109) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Bois de Nueil-les-Aubiers (113) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Bois de Nueil-les-Aubiers (114) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Bois de Argentonnay (86) ⚠️ | Argentonnay › Bocage Bressuirais | 1 |
| Bois de Val en Vignes (83) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Bois de Mauléon (30) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois de Mauléon (34) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois de Moncoutant-sur-Sèvre (14) ⚠️ | Moncoutant-sur-Sèvre › Bocage Bressuirais | 1 |
| Bois de Montravers (6) ⚠️ | Montravers › Bocage Bressuirais | 1 |
| Bois de Montravers (7) ⚠️ | Montravers › Bocage Bressuirais | 1 |
| Bois de Combrand (5) ⚠️ | Combrand › Bocage Bressuirais | 1 |
| Bois de Combrand (7) ⚠️ | Combrand › Bocage Bressuirais | 1 |
| Bois de Montravers (9) ⚠️ | Montravers › Bocage Bressuirais | 1 |
| Bois de Combrand (12) ⚠️ | Combrand › Bocage Bressuirais | 1 |
| Bois de Combrand (14) ⚠️ | Combrand › Bocage Bressuirais | 1 |
| Bois de Saint-Amand-sur-Sèvre (5) ⚠️ | Saint-Amand-sur-Sèvre › Bocage Bressuirais | 1 |
| Bois de Combrand (17) ⚠️ | Combrand › Bocage Bressuirais | 1 |
| Bois de Combrand (20) ⚠️ | Combrand › Bocage Bressuirais | 1 |
| Bois de La Petite-Boissière (9) ⚠️ | La Petite-Boissière › Bocage Bressuirais | 1 |
| Bois de Combrand (23) ⚠️ | Combrand › Bocage Bressuirais | 1 |
| Bois de Montravers (16) ⚠️ | Montravers › Bocage Bressuirais | 1 |
| Bois du Pin (15) ⚠️ | Le Pin › Bocage Bressuirais | 1 |
| Bois de Montravers (18) ⚠️ | Montravers › Bocage Bressuirais | 1 |
| Bois de Combrand (26) ⚠️ | Combrand › Bocage Bressuirais | 1 |
| Bois de Combrand (29) ⚠️ | Combrand › Bocage Bressuirais | 1 |
| Bois de Combrand (30) ⚠️ | Combrand › Bocage Bressuirais | 1 |
| Bois du Pin (18) ⚠️ | Le Pin › Bocage Bressuirais | 1 |
| Bois de Combrand (40) ⚠️ | Combrand › Bocage Bressuirais | 1 |
| Bois de Combrand (41) ⚠️ | Combrand › Bocage Bressuirais | 1 |
| Bois du Pin (24) ⚠️ | Le Pin › Bocage Bressuirais | 1 |
| Bois de Combrand (49) ⚠️ | Combrand › Bocage Bressuirais | 1 |
| Bois de Saint-Marc-la-Lande (3) ⚠️ | Saint-Marc-la-Lande › Val de Gâtine | 1 |
| Forêt de Échiré (14) ⚠️ | Échiré › Niortais | 1 |
| Forêt de Saint-Maxire (3) ⚠️ | Saint-Maxire › Niortais | 1 |
| Forêt de Germond-Rouvre (7) ⚠️ | Germond-Rouvre › Niortais | 1 |
| Forêt de Cerizay (20) ⚠️ | Cerizay › Bocage Bressuirais | 1 |
| Bois du Pin (27) ⚠️ | Le Pin › Bocage Bressuirais | 1 |
| Forêt de Saint-Laurs (2) ⚠️ | Saint-Laurs › Val de Gâtine | 1 |
| Forêt de Béceleuf (7) ⚠️ | Béceleuf › Val de Gâtine | 1 |
| Forêt de Béceleuf (8) ⚠️ | Béceleuf › Val de Gâtine | 1 |
| Forêt de Surin (12) ⚠️ | Surin › Val de Gâtine | 1 |
| Forêt de Aubigné (8) ⚠️ | Aubigné › Mellois en Poitou | 1 |
| Forêt de Aubigné (11) ⚠️ | Aubigné › Mellois en Poitou | 1 |
| Forêt de Arçais (28) ⚠️ | Arçais › Niortais | 1 |
| Bois du Vanneau-Irleau ⚠️ | Le Vanneau-Irleau › Niortais | 1 |
| Bois de Saint-Georges-de-Rex ⚠️ | Saint-Georges-de-Rex › Niortais | 1 |
| Bois du Vanneau-Irleau (3) ⚠️ | Le Vanneau-Irleau › Niortais | 1 |
| Bois de Saint-Georges-de-Rex (4) ⚠️ | Saint-Georges-de-Rex › Niortais | 1 |
| Bois de Saint-Georges-de-Rex (5) ⚠️ | Saint-Georges-de-Rex › Niortais | 1 |
| Bois de Limalonges (2) ⚠️ | Limalonges › Mellois en Poitou | 1 |
| Bois de Cirières (18) ⚠️ | Cirières › Bocage Bressuirais | 1 |
| Bois de Cirières (19) ⚠️ | Cirières › Bocage Bressuirais | 1 |
| Bois de Cirières (22) ⚠️ | Cirières › Bocage Bressuirais | 1 |
| Bois de Cirières (24) ⚠️ | Cirières › Bocage Bressuirais | 1 |
| Bois de Cirières (25) ⚠️ | Cirières › Bocage Bressuirais | 1 |
| Bois de Cirières (30) ⚠️ | Cirières › Bocage Bressuirais | 1 |
| Bois de Bretignolles (27) ⚠️ | Bretignolles › Bocage Bressuirais | 1 |
| Bois de Mauléon (43) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois de La Petite-Boissière (15) ⚠️ | La Petite-Boissière › Bocage Bressuirais | 1 |
| Forêt de La Petite-Boissière (2) ⚠️ | La Petite-Boissière › Bocage Bressuirais | 1 |
| Bois de La Petite-Boissière (16) ⚠️ | La Petite-Boissière › Bocage Bressuirais | 1 |
| Bois de La Petite-Boissière (20) ⚠️ | La Petite-Boissière › Bocage Bressuirais | 1 |
| Bois de La Petite-Boissière (21) ⚠️ | La Petite-Boissière › Bocage Bressuirais | 1 |
| Bois de Mauléon (50) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Forêt de Allonne ⚠️ | Allonne › Parthenay-Gâtine | 1 |
| Parc de Bressuire (33) ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Mauléon (51) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois de Saint-Amand-sur-Sèvre (27) ⚠️ | Saint-Amand-sur-Sèvre › Bocage Bressuirais | 1 |
| Bois de Saint-Pierre-des-Échaubrognes (8) ⚠️ | Saint-Pierre-des-Échaubrognes › Bocage Bressuirais | 1 |
| Bois de Saint-Pierre-des-Échaubrognes (9) ⚠️ | Saint-Pierre-des-Échaubrognes › Bocage Bressuirais | 1 |
| Bois de Saint-Pierre-des-Échaubrognes (11) ⚠️ | Saint-Pierre-des-Échaubrognes › Bocage Bressuirais | 1 |
| Bois de Saint-Pierre-des-Échaubrognes (12) ⚠️ | Saint-Pierre-des-Échaubrognes › Bocage Bressuirais | 1 |
| Bois de Saint-Pierre-des-Échaubrognes (13) ⚠️ | Saint-Pierre-des-Échaubrognes › Bocage Bressuirais | 1 |
| Bois de Saint-Pierre-des-Échaubrognes (19) ⚠️ | Saint-Pierre-des-Échaubrognes › Bocage Bressuirais | 1 |
| Bois de Saint-Pierre-des-Échaubrognes (20) ⚠️ | Saint-Pierre-des-Échaubrognes › Bocage Bressuirais | 1 |
| Bois de Mauléon (59) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois de Mauléon (60) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois de Mauléon (61) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois de Mauléon (62) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois de Mauléon (64) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois de Mauléon (69) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois de Mauléon (75) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois de Mauléon (79) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois de Mauléon (86) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois de Mauléon (87) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois de Saint-Pierre-des-Échaubrognes (27) ⚠️ | Saint-Pierre-des-Échaubrognes › Bocage Bressuirais | 1 |
| Bois de Saint-Pierre-des-Échaubrognes (29) ⚠️ | Saint-Pierre-des-Échaubrognes › Bocage Bressuirais | 1 |
| Bois de Mauléon (94) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois de Mauléon (96) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois de Mauléon (97) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois de Mauléon (99) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois de Mauléon (103) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois de Mauléon (104) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Forêt de Chef-Boutonne (13) ⚠️ | Chef-Boutonne › Mellois en Poitou | 1 |
| Bois de Mauléon (116) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois de Mauléon (120) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Forêt de Niort (117) ⚠️ | Niort › Niortais | 1 |
| Bois de Mauléon (122) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois de Mauléon (125) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois de Mauléon (130) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois de Mauléon (132) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois de Saint-Pierre-des-Échaubrognes (33) ⚠️ | Saint-Pierre-des-Échaubrognes › Bocage Bressuirais | 1 |
| Bois de Mauléon (142) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois de Niort (43) ⚠️ | Niort › Niortais | 1 |
| Forêt de Rom (22) ⚠️ | Rom › Mellois en Poitou | 1 |
| Forêt de Rom (27) ⚠️ | Rom › Mellois en Poitou | 1 |
| Forêt de Sauzé-entre-Bois (55) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Forêt de Sauzé-entre-Bois (57) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Forêt de Sauzé-entre-Bois (58) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Forêt de Sauzé-entre-Bois (59) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Forêt de Sauzé-entre-Bois (60) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Forêt de Sauzé-entre-Bois (67) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Forêt de Sauzé-entre-Bois (75) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Forêt de Limalonges (73) ⚠️ | Limalonges › Mellois en Poitou | 1 |
| Forêt de Mairé-Levescault (21) ⚠️ | Mairé-Levescault › Mellois en Poitou | 1 |
| Forêt de Lorigné (9) ⚠️ | Lorigné › Mellois en Poitou | 1 |
| Forêt de Aiffres (39) ⚠️ | Aiffres › Niortais | 1 |
| Forêt de Sauzé-entre-Bois (79) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Forêt de Sauzé-entre-Bois (80) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Forêt de Sauzé-entre-Bois (81) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Forêt de Sauzé-entre-Bois (82) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Forêt de Rom (30) ⚠️ | Rom › Mellois en Poitou | 1 |
| Forêt de Rom (31) ⚠️ | Rom › Mellois en Poitou | 1 |
| Forêt de Rom (32) ⚠️ | Rom › Mellois en Poitou | 1 |
| Forêt de Rom (34) ⚠️ | Rom › Mellois en Poitou | 1 |
| Forêt de Rom (38) ⚠️ | Rom › Mellois en Poitou | 1 |
| Forêt de Rom (40) ⚠️ | Rom › Mellois en Poitou | 1 |
| Forêt de Rom (41) ⚠️ | Rom › Mellois en Poitou | 1 |
| Forêt de Rom (42) ⚠️ | Rom › Mellois en Poitou | 1 |
| Forêt de Rom (43) ⚠️ | Rom › Mellois en Poitou | 1 |
| Forêt de Rom (44) ⚠️ | Rom › Mellois en Poitou | 1 |
| Forêt de Rom (47) ⚠️ | Rom › Mellois en Poitou | 1 |
| Forêt de Rom (51) ⚠️ | Rom › Mellois en Poitou | 1 |
| Bois de Chauray (20) ⚠️ | Chauray › Niortais | 1 |
| Forêt de Rom (59) ⚠️ | Rom › Mellois en Poitou | 1 |
| Bois de Ménigoute ⚠️ | Ménigoute › Parthenay-Gâtine | 1 |
| Bois de Ménigoute (2) ⚠️ | Ménigoute › Parthenay-Gâtine | 1 |
| Forêt de François (2) ⚠️ | François › Haut Val de Sèvre | 1 |
| Le Bois des Elfes ⚠️ | Aigondigné › Mellois en Poitou | 1 |
| Parc intergénérationnel ⚠️ | Magné › Niortais | 1 |
| Parc de Cerizay ⚠️ | Cerizay › Bocage Bressuirais | 1 |
| Parc de Cerizay (2) ⚠️ | Cerizay › Bocage Bressuirais | 1 |
| Bois de Mazières-en-Gâtine ⚠️ | Mazières-en-Gâtine › Val de Gâtine | 1 |
| Bois de Saint-Pardoux-Soutiers (9) ⚠️ | Saint-Pardoux-Soutiers › Val de Gâtine | 1 |
| Parc de Beugnon-Thireuil ⚠️ | Beugnon-Thireuil › Val de Gâtine | 1 |
| Bois de Vernoux-en-Gâtine (7) ⚠️ | Vernoux-en-Gâtine › Parthenay-Gâtine | 1 |
| Bois de Scillé (6) ⚠️ | Scillé › Val de Gâtine | 1 |
| Parc du Lavoir ⚠️ | Vernoux-en-Gâtine › Parthenay-Gâtine | 1 |
| Terrain des sapins ⚠️ | Nanteuil › Haut Val de Sèvre | 1 |
| Bois de Mauzé-sur-le-Mignon (4) ⚠️ | Mauzé-sur-le-Mignon › Niortais | 1 |
| Bois de Val-du-Mignon (6) ⚠️ | Val-du-Mignon › Niortais | 1 |
| Bois de Saint-Rémy (2) ⚠️ | Saint-Rémy › Niortais | 1 |
| Bois de Saint-Rémy (3) ⚠️ | Saint-Rémy › Niortais | 1 |
| Bois de Villiers-en-Plaine (4) ⚠️ | Villiers-en-Plaine › Niortais | 1 |
| Bois de Villiers-en-Plaine (9) ⚠️ | Villiers-en-Plaine › Niortais | 1 |
| Place Saint-Jacques ⚠️ | Bressuire › Bocage Bressuirais | 1 |
| Bois de Argentonnay (89) ⚠️ | Argentonnay › Bocage Bressuirais | 1 |
| Forêt de Melle (91) ⚠️ | Melle › Mellois en Poitou | 1 |
| Forêt de Pamproux (22) ⚠️ | Pamproux › Haut Val de Sèvre | 1 |
| Forêt de Sainte-Soline (23) ⚠️ | Sainte-Soline › Mellois en Poitou | 1 |
| Forêt de Brioux-sur-Boutonne (28) ⚠️ | Brioux-sur-Boutonne › Mellois en Poitou | 1 |
| Forêt de Saint-Symphorien (30) ⚠️ | Saint-Symphorien › Niortais | 1 |
| Forêt de Sauzé-entre-Bois (91) ⚠️ | Sauzé-entre-Bois › Mellois en Poitou | 1 |
| Forêt de Bessines (14) ⚠️ | Bessines › Niortais | 1 |
| Forêt de Saint-Symphorien (33) ⚠️ | Saint-Symphorien › Niortais | 1 |
| Forêt de Fors (30) ⚠️ | Fors › Niortais | 1 |
| Forêt de Prahecq (11) ⚠️ | Prahecq › Niortais | 1 |
| Forêt de Aiffres (51) ⚠️ | Aiffres › Niortais | 1 |
| Forêt de Aiffres (55) ⚠️ | Aiffres › Niortais | 1 |
| Forêt de Aiffres (65) ⚠️ | Aiffres › Niortais | 1 |
| Forêt de Aiffres (66) ⚠️ | Aiffres › Niortais | 1 |
| Forêt de Aiffres (68) ⚠️ | Aiffres › Niortais | 1 |
| Forêt de Aiffres (81) ⚠️ | Aiffres › Niortais | 1 |
| Forêt de Aiffres (84) ⚠️ | Aiffres › Niortais | 1 |
| Forêt de Aiffres (85) ⚠️ | Aiffres › Niortais | 1 |
| Forêt de Aiffres (91) ⚠️ | Aiffres › Niortais | 1 |
| Forêt de Aiffres (94) ⚠️ | Aiffres › Niortais | 1 |
| Forêt de Aiffres (98) ⚠️ | Aiffres › Niortais | 1 |
| Forêt de Aiffres (99) ⚠️ | Aiffres › Niortais | 1 |
| Forêt de Saint-Symphorien (34) ⚠️ | Saint-Symphorien › Niortais | 1 |
| Forêt de Niort (126) ⚠️ | Saint-Symphorien › Niortais | 1 |
| Forêt de Niort (127) ⚠️ | Niort › Niortais | 1 |
| Forêt de Saint-Symphorien (36) ⚠️ | Saint-Symphorien › Niortais | 1 |
| Forêt de Prahecq (15) ⚠️ | Prahecq › Niortais | 1 |
| Forêt de Saint-Symphorien (39) ⚠️ | Saint-Symphorien › Niortais | 1 |
| Forêt de Niort (129) ⚠️ | Niort › Niortais | 1 |
| Forêt de Niort (135) ⚠️ | Niort › Niortais | 1 |
| Forêt de Bessines (16) ⚠️ | Niort › Niortais | 1 |
| Forêt de Bessines (17) ⚠️ | Bessines › Niortais | 1 |
| Forêt de Niort (137) ⚠️ | Niort › Niortais | 1 |
| Forêt de Niort (145) ⚠️ | Niort › Niortais | 1 |
| Bois de Bessines (2) ⚠️ | Bessines › Niortais | 1 |
| Forêt de Saint-Symphorien (41) ⚠️ | Saint-Symphorien › Niortais | 1 |
| Forêt de Bessines (21) ⚠️ | Bessines › Niortais | 1 |
| Forêt de Saint-Symphorien (44) ⚠️ | Saint-Symphorien › Niortais | 1 |
| Forêt de Fors (34) ⚠️ | Fors › Niortais | 1 |
| Forêt de Saint-Martin-de-Bernegoue (10) ⚠️ | Saint-Martin-de-Bernegoue › Niortais | 1 |
| Forêt de Prahecq (17) ⚠️ | Prahecq › Niortais | 1 |
| Forêt de Prahecq (19) ⚠️ | Prahecq › Niortais | 1 |
| Forêt de Aigondigné (11) ⚠️ | Aigondigné › Mellois en Poitou | 1 |
| Forêt de Fors (37) ⚠️ | Fors › Niortais | 1 |
| Forêt de Prahecq (26) ⚠️ | Prahecq › Niortais | 1 |
| Forêt de Fors (42) ⚠️ | Fors › Niortais | 1 |
| Forêt de Fors (44) ⚠️ | Fors › Niortais | 1 |
| Forêt de Fors (49) ⚠️ | Fors › Niortais | 1 |
| Forêt de Vouillé (35) ⚠️ | Vouillé › Niortais | 1 |
| Forêt de Vouillé (37) ⚠️ | Vouillé › Niortais | 1 |
| Forêt de Saint-Martin-de-Bernegoue (16) ⚠️ | Saint-Martin-de-Bernegoue › Niortais | 1 |
| Forêt de Saint-Martin-de-Bernegoue (17) ⚠️ | Saint-Martin-de-Bernegoue › Niortais | 1 |
| Forêt de Prahecq (28) ⚠️ | Prahecq › Niortais | 1 |
| Parc du château de la Voute ⚠️ | Prahecq › Niortais | 1 |
| Forêt de Prahecq (41) ⚠️ | Prahecq › Niortais | 1 |
| Forêt de Prahecq (53) ⚠️ | Prahecq › Niortais | 1 |
| Forêt de Prahecq (58) ⚠️ | Prahecq › Niortais | 1 |
| Forêt de Marigny (15) ⚠️ | Marigny › Niortais | 1 |
| Forêt de Fors (58) ⚠️ | Fors › Niortais | 1 |
| Forêt de Fors (62) ⚠️ | Fors › Niortais | 1 |
| Forêt de Granzay-Gript (17) ⚠️ | Granzay-Gript › Niortais | 1 |
| Forêt de Niort (154) ⚠️ | Niort › Niortais | 1 |
| Forêt de Marigny (22) ⚠️ | Marigny › Niortais | 1 |
| Forêt de Marigny (24) ⚠️ | Marigny › Niortais | 1 |
| Forêt de Marigny (34) ⚠️ | Marigny › Niortais | 1 |
| Forêt de Beauvoir-sur-Niort (15) ⚠️ | Granzay-Gript › Niortais | 1 |
| Forêt de Juscorps (7) ⚠️ | Juscorps › Niortais | 1 |
| Forêt de Juscorps (10) ⚠️ | Juscorps › Niortais | 1 |
| Forêt de Saint-Martin-de-Bernegoue (31) ⚠️ | Saint-Martin-de-Bernegoue › Niortais | 1 |
| Forêt de Fressines (11) ⚠️ | Fressines › Mellois en Poitou | 1 |
| Forêt de Marigny (36) ⚠️ | Marigny › Niortais | 1 |
| Forêt de Granzay-Gript (28) ⚠️ | Granzay-Gript › Niortais | 1 |
| Forêt de Saint-Martin-de-Bernegoue (35) ⚠️ | Saint-Martin-de-Bernegoue › Niortais | 1 |
| Forêt de Saint-Martin-de-Bernegoue (46) ⚠️ | Saint-Martin-de-Bernegoue › Niortais | 1 |
| Forêt de Prahecq (62) ⚠️ | Prahecq › Niortais | 1 |
| Bois de Prahecq (20) ⚠️ | Prahecq › Niortais | 1 |
| Forêt de Prahecq (68) ⚠️ | Prahecq › Niortais | 1 |
| Forêt de Granzay-Gript (32) ⚠️ | Granzay-Gript › Niortais | 1 |
| Bois du Griffier ⚠️ | Granzay-Gript › Niortais | 1 |
| Forêt de Granzay-Gript (35) ⚠️ | Granzay-Gript › Niortais | 1 |
| Forêt de Granzay-Gript (37) ⚠️ | Granzay-Gript › Niortais | 1 |
| Forêt de Fors (68) ⚠️ | Fors › Niortais | 1 |
| Forêt de Granzay-Gript (55) ⚠️ | Granzay-Gript › Niortais | 1 |
| Forêt de Granzay-Gript (59) ⚠️ | Granzay-Gript › Niortais | 1 |
| Forêt de Granzay-Gript (66) ⚠️ | Granzay-Gript › Niortais | 1 |
| Forêt de Granzay-Gript (67) ⚠️ | Granzay-Gript › Niortais | 1 |
| Forêt de Granzay-Gript (68) ⚠️ | Granzay-Gript › Niortais | 1 |
| Forêt de Fors (72) ⚠️ | Fors › Niortais | 1 |
| Forêt de Granzay-Gript (74) ⚠️ | Granzay-Gript › Niortais | 1 |
| Forêt de Granzay-Gript (77) ⚠️ | Granzay-Gript › Niortais | 1 |
| Forêt de Granzay-Gript (80) ⚠️ | Granzay-Gript › Niortais | 1 |
| Bois de Prahecq (24) ⚠️ | Prahecq › Niortais | 1 |
| Bois de Prahecq (25) ⚠️ | Prahecq › Niortais | 1 |
| Bois de Vouillé (18) ⚠️ | Vouillé › Niortais | 1 |
| Bois de Vouillé (21) ⚠️ | Vouillé › Niortais | 1 |
| Bois de Vouillé (29) ⚠️ | Vouillé › Niortais | 1 |
| Bois de Vouillé (33) ⚠️ | Vouillé › Niortais | 1 |
| Forêt de Vouillé (40) ⚠️ | Vouillé › Niortais | 1 |
| Bois de Vouillé (34) ⚠️ | Vouillé › Niortais | 1 |
| Forêt de Vouillé (41) ⚠️ | Vouillé › Niortais | 1 |
| Forêt de La Crèche (19) ⚠️ | La Crèche › Haut Val de Sèvre | 1 |
| Forêt de Vouillé (42) ⚠️ | Vouillé › Niortais | 1 |
| Forêt de La Crèche (20) ⚠️ | La Crèche › Haut Val de Sèvre | 1 |
| Forêt de La Crèche (21) ⚠️ | La Crèche › Haut Val de Sèvre | 1 |
| Bois de Vouillé (46) ⚠️ | Vouillé › Niortais | 1 |
| Bois de La Crèche (14) ⚠️ | La Crèche › Haut Val de Sèvre | 1 |
| Bois de Vouillé (47) ⚠️ | Vouillé › Niortais | 1 |
| Bois de La Crèche (15) ⚠️ | La Crèche › Haut Val de Sèvre | 1 |
| Bois de Prahecq (27) ⚠️ | Prahecq › Niortais | 1 |
| Bois de Prahecq (30) ⚠️ | Prahecq › Niortais | 1 |
| Forêt de Brion-près-Thouet (5) ⚠️ | Brion-près-Thouet › Thouarsais | 1 |
| Bois de Prahecq (33) ⚠️ | Prahecq › Niortais | 1 |
| Forêt de Prahecq (70) ⚠️ | Prahecq › Niortais | 1 |
| Bois de Prahecq (41) ⚠️ | Prahecq › Niortais | 1 |
| Bois de Prahecq (42) ⚠️ | Prahecq › Niortais | 1 |
| Bois de Prahecq (47) ⚠️ | Prahecq › Niortais | 1 |
| Forêt de Chauray (6) ⚠️ | Chauray › Niortais | 1 |
| Bois de Plaine-et-Vallées (58) ⚠️ | Plaine-et-Vallées › Thouarsais | 1 |
| Bois de Saint-Martin-de-Bernegoue (14) ⚠️ | Saint-Martin-de-Bernegoue › Niortais | 1 |
| Bois de Vouillé (52) ⚠️ | Vouillé › Niortais | 1 |
| Bois de Saint-Martin-de-Bernegoue (17) ⚠️ | Saint-Martin-de-Bernegoue › Niortais | 1 |
| Forêt de Val en Vignes (55) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Bois de Aigondigné (32) ⚠️ | Aigondigné › Mellois en Poitou | 1 |
| Bois de Aigondigné (36) ⚠️ | Aigondigné › Mellois en Poitou | 1 |
| Bois de Aigondigné (37) ⚠️ | Aigondigné › Mellois en Poitou | 1 |
| Bois de Saint-Martin-de-Bernegoue (29) ⚠️ | Saint-Martin-de-Bernegoue › Niortais | 1 |
| Bois de Brûlain (7) ⚠️ | Brûlain › Niortais | 1 |
| Bois de Chauray (26) ⚠️ | Chauray › Niortais | 1 |
| Bois de Chauray (28) ⚠️ | Chauray › Niortais | 1 |
| Bois de Thouars (55) ⚠️ | Thouars › Thouarsais | 1 |
| Bois de Loretz-d'Argenton (71) ⚠️ | Loretz-d'Argenton › Thouarsais | 1 |
| Bois de Chauray (29) ⚠️ | Chauray › Niortais | 1 |
| Bois de Saint-Gelais (3) ⚠️ | Saint-Gelais › Niortais | 1 |
| Bois de Saint-Gelais (4) ⚠️ | Saint-Gelais › Niortais | 1 |
| Bois de Chauray (31) ⚠️ | Chauray › Niortais | 1 |
| Bois de Saint-Gelais (6) ⚠️ | Saint-Gelais › Niortais | 1 |
| Bois de Saint-Gelais (7) ⚠️ | Saint-Gelais › Niortais | 1 |
| Bois de Saint-Gelais (9) ⚠️ | Saint-Gelais › Niortais | 1 |
| Bois de Saint-Gelais (10) ⚠️ | Saint-Gelais › Niortais | 1 |
| Forêt de Niort (156) ⚠️ | Niort › Niortais | 1 |
| Bois de Val en Vignes (87) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Bois de Aigondigné (50) ⚠️ | Aigondigné › Mellois en Poitou | 1 |
| Forêt de Aigondigné (20) ⚠️ | Aigondigné › Mellois en Poitou | 1 |
| Forêt de Loretz-d'Argenton (38) ⚠️ | Loretz-d'Argenton › Thouarsais | 1 |
| Bois de Aigondigné (57) ⚠️ | Aigondigné › Mellois en Poitou | 1 |
| Bois de Fressines (3) ⚠️ | Fressines › Mellois en Poitou | 1 |
| Bois de Aigondigné (58) ⚠️ | Aigondigné › Mellois en Poitou | 1 |
| Bois de Niort (52) ⚠️ | Niort › Niortais | 1 |
| Bois de Niort (57) ⚠️ | Niort › Niortais | 1 |
| Bois de Niort (58) ⚠️ | Niort › Niortais | 1 |
| Bois de Niort (62) ⚠️ | Niort › Niortais | 1 |
| Bois de Niort (63) ⚠️ | Niort › Niortais | 1 |
| Bois de Aigondigné (61) ⚠️ | Aigondigné › Mellois en Poitou | 1 |
| Bois de Aigondigné (69) ⚠️ | Aigondigné › Mellois en Poitou | 1 |
| Bois de Aigondigné (70) ⚠️ | Aigondigné › Mellois en Poitou | 1 |
| Bois de Brûlain (23) ⚠️ | Brûlain › Niortais | 1 |
| Bois de Brûlain (24) ⚠️ | Brûlain › Niortais | 1 |
| Bois de Aigondigné (84) ⚠️ | Aigondigné › Mellois en Poitou | 1 |
| Forêt de Celles-sur-Belle (33) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 1 |
| Forêt de Celles-sur-Belle (37) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 1 |
| Bois de Aigondigné (101) ⚠️ | Aigondigné › Mellois en Poitou | 1 |
| Bois de Celles-sur-Belle (14) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 1 |
| Bois de Celles-sur-Belle (15) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 1 |
| Forêt de Celles-sur-Belle (39) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 1 |
| Bois de Val en Vignes (89) ⚠️ | Val en Vignes › Thouarsais | 1 |
| Bois de Aigondigné (109) ⚠️ | Aigondigné › Mellois en Poitou | 1 |
| Bois de Celles-sur-Belle (35) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 1 |
| Bois de Genneton (13) ⚠️ | Genneton › Bocage Bressuirais | 1 |
| Bois de Saint Maurice Étusson (16) ⚠️ | Saint Maurice Étusson › Bocage Bressuirais | 1 |
| Bois de Celles-sur-Belle (39) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 1 |
| Forêt de Celles-sur-Belle (47) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 1 |
| Bois de Celles-sur-Belle (46) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 1 |
| Forêt de Celles-sur-Belle (50) ⚠️ | Celles-sur-Belle › Mellois en Poitou | 1 |
| Bois de Négressauve ⚠️ | Celles-sur-Belle › Mellois en Poitou | 1 |
| Bois de Brûlain (29) ⚠️ | Brûlain › Niortais | 1 |
| Forêt de Aiffres (102) ⚠️ | Aiffres › Niortais | 1 |
| Bois de Brûlain (31) ⚠️ | Brûlain › Niortais | 1 |
| Bois de Saint-Aubin-du-Plain (14) ⚠️ | Saint-Aubin-du-Plain › Bocage Bressuirais | 1 |
| Bois de Marigny (20) ⚠️ | Marigny › Niortais | 1 |
| Bois de Marigny (23) ⚠️ | Marigny › Niortais | 1 |
| Forêt de Marigny (54) ⚠️ | Marigny › Niortais | 1 |
| Bois de Marigny (36) ⚠️ | Marigny › Niortais | 1 |
| Bois de Beauvoir-sur-Niort ⚠️ | Beauvoir-sur-Niort › Niortais | 1 |
| Forêt de Beauvoir-sur-Niort (17) ⚠️ | Beauvoir-sur-Niort › Niortais | 1 |
| Bois de Beauvoir-sur-Niort (4) ⚠️ | Beauvoir-sur-Niort › Niortais | 1 |
| Forêt de Marigny (55) ⚠️ | Marigny › Niortais | 1 |
| Forêt de Marigny (56) ⚠️ | Marigny › Niortais | 1 |
| Forêt de Beauvoir-sur-Niort (24) ⚠️ | Beauvoir-sur-Niort › Niortais | 1 |
| Forêt de Aiffres (104) ⚠️ | Aiffres › Niortais | 1 |
| Forêt de Marigny (61) ⚠️ | Marigny › Niortais | 1 |
| Bois de Marigny (63) ⚠️ | Marigny › Niortais | 1 |
| Forêt de Marigny (70) ⚠️ | Marigny › Niortais | 1 |
| Forêt de Marigny (73) ⚠️ | Marigny › Niortais | 1 |
| Forêt de Marigny (74) ⚠️ | Marigny › Niortais | 1 |
| Bois de Juscorps (15) ⚠️ | Juscorps › Niortais | 1 |
| Bois de Marigny (68) ⚠️ | Marigny › Niortais | 1 |
| Bois de Saint-Romans-des-Champs (3) ⚠️ | Saint-Romans-des-Champs › Niortais | 1 |
| Bois de Saurais (4) ⚠️ | Saurais › Parthenay-Gâtine | 1 |
| Forêt de Saurais (5) ⚠️ | Saurais › Parthenay-Gâtine | 1 |
| Forêt de Saint-Martin-du-Fouilloux (13) ⚠️ | Saint-Martin-du-Fouilloux › Parthenay-Gâtine | 1 |
| Forêt de Saint-Martin-du-Fouilloux (14) ⚠️ | Saint-Martin-du-Fouilloux › Parthenay-Gâtine | 1 |
| Forêt de La Chapelle-Bertrand (16) ⚠️ | La Chapelle-Bertrand › Parthenay-Gâtine | 1 |
| Forêt de Saint-Romans-des-Champs ⚠️ | Saint-Romans-des-Champs › Niortais | 1 |
| Forêt de Brûlain (8) ⚠️ | Brûlain › Niortais | 1 |
| Forêt de Saint-Romans-des-Champs (2) ⚠️ | Saint-Romans-des-Champs › Niortais | 1 |
| Bois de Brûlain (38) ⚠️ | Brûlain › Niortais | 1 |
| Forêt de Brûlain (13) ⚠️ | Brûlain › Niortais | 1 |
| Forêt de Brûlain (14) ⚠️ | Brûlain › Niortais | 1 |
| Forêt de Brûlain (19) ⚠️ | Brûlain › Niortais | 1 |
| Forêt des Fosses (8) ⚠️ | Les Fosses › Mellois en Poitou | 1 |
| Bois de Nueil-les-Aubiers (118) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Bois de Saint Maurice Étusson (18) ⚠️ | Saint Maurice Étusson › Bocage Bressuirais | 1 |
| Bois de Nueil-les-Aubiers (121) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Bois de Nueil-les-Aubiers (122) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Bois de Nueil-les-Aubiers (123) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Bois de Bretignolles (28) ⚠️ | Bretignolles › Bocage Bressuirais | 1 |
| Bois de Bretignolles (30) ⚠️ | Bretignolles › Bocage Bressuirais | 1 |
| Bois de Nueil-les-Aubiers (124) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Bois du Pin (32) ⚠️ | Le Pin › Bocage Bressuirais | 1 |
| Bois de Nueil-les-Aubiers (126) ⚠️ | Le Pin › Bocage Bressuirais | 1 |
| Bois de Mauléon (153) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois de Mauléon (155) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois de Combrand (52) ⚠️ | Combrand › Bocage Bressuirais | 1 |
| Bois de Montravers (19) ⚠️ | Montravers › Bocage Bressuirais | 1 |
| Bois de La Petite-Boissière (28) ⚠️ | La Petite-Boissière › Bocage Bressuirais | 1 |
| Bois de Mauléon (157) ⚠️ | Mauléon › Bocage Bressuirais | 1 |
| Bois du Pin (35) ⚠️ | Le Pin › Bocage Bressuirais | 1 |
| Bois de Combrand (54) ⚠️ | Combrand › Bocage Bressuirais | 1 |
| Bois du Pin (37) ⚠️ | Combrand › Bocage Bressuirais | 1 |
| Bois de Cerizay (9) ⚠️ | Cerizay › Bocage Bressuirais | 1 |
| Bois de Combrand (57) ⚠️ | Combrand › Bocage Bressuirais | 1 |
| Bois de Combrand (58) ⚠️ | Combrand › Bocage Bressuirais | 1 |
| Bois de Combrand (59) ⚠️ | Combrand › Bocage Bressuirais | 1 |
| Bois de Cerizay (12) ⚠️ | Cerizay › Bocage Bressuirais | 1 |
| Bois de Cirières (34) ⚠️ | Cirières › Bocage Bressuirais | 1 |
| Bois de Cirières (35) ⚠️ | Cirières › Bocage Bressuirais | 1 |
| Bois de Nueil-les-Aubiers (130) ⚠️ | Nueil-les-Aubiers › Bocage Bressuirais | 1 |
| Forêt de Saint-Amand-sur-Sèvre (6) ⚠️ | Saint-Amand-sur-Sèvre › Bocage Bressuirais | 1 |
| Bois de Saint-Amand-sur-Sèvre (31) ⚠️ | Saint-Amand-sur-Sèvre › Bocage Bressuirais | 1 |
| Bois de Saint-Pierre-des-Échaubrognes (35) ⚠️ | Saint-Pierre-des-Échaubrognes › Bocage Bressuirais | 1 |
| Bois de Saint-Pierre-des-Échaubrognes (39) ⚠️ | Saint-Pierre-des-Échaubrognes › Bocage Bressuirais | 1 |
| Forêt de Niort (161) ⚠️ | Niort › Niortais | 1 |
| Forêt de Niort (162) ⚠️ | Niort › Niortais | 1 |
| Forêt de Aiffres (108) ⚠️ | Aiffres › Niortais | 1 |
| Bois de Aiffres (15) ⚠️ | Aiffres › Niortais | 1 |
| Bois de Aiffres (19) ⚠️ | Aiffres › Niortais | 1 |
| Forêt de Aiffres (110) ⚠️ | Aiffres › Niortais | 1 |
| Forêt de Niort (164) ⚠️ | Niort › Niortais | 1 |
| Forêt de Aiffres (118) ⚠️ | Aiffres › Niortais | 1 |

3 929 parc(s) plus petits qu'une cellule ne sont pas listés : la carte les dessine, mais ils n'offrent aucune cellule.

⚠️ 6888 parc(s) hors de la fenêtre 10–125 cellules (6856 trop petit(s), 32 trop grand(s)) : affichés sur la carte, mais ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| military | 486 |
| airport | 83 |
| prison | 0 |
| **Total déclaré** | **569** |
| dont dans une zone de ce territoire | 568 |

Le jeu de données couvre plus large que le territoire — il est produit à une échelle supérieure. Seules les cellules tombant dans une zone d'ici pèsent sur un pourcentage.

### Zones concernées

| Zone | Cellules exclues |
|---|---:|
| Avon | 381 |
| Niort | 59 |
| Bougon | 42 |
| Saint-Maixent-l'École | 41 |
| Mauléon | 14 |
| Pamproux | 13 |
| Exoudun | 8 |
| Thouars | 7 |
| Saint-Léger-de-Montbrun | 3 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
