# Cantabrie

Pack `es-cantabria` · version 1.0.1 · grille 200 m · Espagne › Cantabrie

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 247 551 |
| dont restreintes (aéroport, militaire, prison) | 96 |
| dont sans chemin (aucune voie à moins de 60 m) | 52 586 |
| dont en forêt, sans chemin non plus | 41 873 |
| dont traversées par un cours d'eau, sans chemin non plus | 7 157 |
| Cellules retirées par le masque d'eau | 3 221 |
| Villes | 103 |
| Arrondissements et quartiers | 0 |
| Îles | 0 |
| Parcs | 4 384 |

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

## Villes (103)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Sans chemin | Parcs |
|---|---:|---:|---:|---:|---:|---:|---:|
| Valderredible | 13 857 | 48 | 13 809 | 4 | **13 805** | 2 618 (19 %) | 112 |
| Hermandad de Campoo de Suso | 10 419 | 18 | 10 401 | 0 | **10 401** | 3 124 (30 %) | 34 |
| Soba | 10 056 | 6 | 10 050 | 0 | **10 050** | 3 101 (31 %) | 103 |
| Camaleño | 7 587 | 1 | 7 586 | 0 | **7 586** | 1 561 (21 %) | 41 |
| Vega de Liébana | 6 228 | 1 | 6 227 | 0 | **6 227** | 1 191 (19 %) | 30 |
| Rionansa | 5 562 | 24 | 5 538 | 0 | **5 538** | 2 097 (38 %) | 60 |
| Cillorigo de Liébana | 4 932 | 7 | 4 925 | 0 | **4 925** | 1 418 (29 %) | 26 |
| Valdáliga | 4 613 | 17 | 4 596 | 0 | **4 596** | 884 (19 %) | 76 |
| Castro-Urdiales | 4 524 | 14 | 4 510 | 0 | **4 510** | 458 (10 %) | 240 |
| Luena | 4 247 | 13 | 4 234 | 0 | **4 234** | 1 312 (31 %) | 40 |
| Los Tojos | 4 210 | 5 | 4 205 | 0 | **4 205** | 1 410 (34 %) | 22 |
| Polaciones | 4 223 | 21 | 4 202 | 0 | **4 202** | 1 030 (25 %) | 56 |
| Campoo de Enmedio | 4 260 | 101 | 4 159 | 0 | **4 159** | 1 034 (25 %) | 16 |
| Valdeprado del Río | 4 170 | 13 | 4 157 | 0 | **4 157** | 984 (24 %) | 31 |
| Ruesga | 4 153 | 14 | 4 139 | 0 | **4 139** | 1 470 (36 %) | 33 |
| Vega de Pas | 4 111 | 13 | 4 098 | 0 | **4 098** | 1 217 (30 %) | 48 |
| Arenas de Iguña | 4 081 | 10 | 4 071 | 0 | **4 071** | 1 113 (27 %) | 24 |
| Cabuérniga | 4 058 | 9 | 4 049 | 0 | **4 049** | 1 370 (34 %) | 23 |
| Piélagos | 3 955 | 52 | 3 903 | 0 | **3 903** | 152 (4 %) | 68 |
| Valdeolea | 3 902 | 0 | 3 902 | 0 | **3 902** | 915 (23 %) | 19 |
| Cabezón de Liébana | 3 820 | 0 | 3 820 | 0 | **3 820** | 365 (10 %) | 5 |
| Guriezo | 3 763 | 18 | 3 745 | 0 | **3 745** | 478 (13 %) | 44 |
| Voto | 3 677 | 49 | 3 628 | 0 | **3 628** | 603 (17 %) | 34 |
| Lamasón | 3 351 | 6 | 3 345 | 0 | **3 345** | 1 430 (43 %) | 41 |
| Molledo | 3 338 | 4 | 3 334 | 0 | **3 334** | 734 (22 %) | 25 |
| Pesaguero | 3 279 | 0 | 3 279 | 0 | **3 279** | 470 (14 %) | 8 |
| Mancomunidad de Campoo-Cabuérniga | 3 224 | 0 | 3 224 | 0 | **3 224** | 1 247 (39 %) | 1 |
| Campoo de Yuso | 4 199 | 1 024 | 3 175 | 0 | **3 175** | 672 (21 %) | 24 |
| Ruente | 3 110 | 15 | 3 095 | 0 | **3 095** | 593 (19 %) | 26 |
| San Pedro del Romeral | 2 696 | 1 | 2 695 | 0 | **2 695** | 727 (27 %) | 12 |
| Mazcuerras | 2 633 | 10 | 2 623 | 0 | **2 623** | 512 (20 %) | 26 |
| Peñarrubia | 2 551 | 7 | 2 544 | 0 | **2 544** | 1 004 (39 %) | 9 |
| Tudanca | 2 464 | 7 | 2 457 | 0 | **2 457** | 937 (38 %) | 28 |
| Villacarriedo | 2 400 | 5 | 2 395 | 0 | **2 395** | 529 (22 %) | 17 |
| Val de San Vicente | 2 400 | 57 | 2 343 | 0 | **2 343** | 344 (15 %) | 48 |
| Corvera de Toranzo | 2 327 | 12 | 2 315 | 0 | **2 315** | 628 (27 %) | 18 |
| Santa María de Cayón | 2 263 | 9 | 2 254 | 0 | **2 254** | 149 (7 %) | 757 |
| Arredondo | 2 220 | 6 | 2 214 | 0 | **2 214** | 759 (34 %) | 22 |
| Alfoz de Lloredo | 2 190 | 1 | 2 189 | 0 | **2 189** | 204 (9 %) | 33 |
| Los Corrales de Buelna | 2 142 | 8 | 2 134 | 0 | **2 134** | 291 (14 %) | 47 |
| Cieza | 2 075 | 5 | 2 070 | 0 | **2 070** | 660 (32 %) | 12 |
| Entrambasaguas | 2 034 | 2 | 2 032 | 0 | **2 032** | 268 (13 %) | 76 |
| Las Rozas de Valdearroyo | 2 677 | 657 | 2 020 | 0 | **2 020** | 612 (30 %) | 25 |
| Rasines | 2 024 | 5 | 2 019 | 0 | **2 019** | 255 (13 %) | 12 |
| Ribamontán al Monte | 1 995 | 2 | 1 993 | 0 | **1 993** | 109 (5 %) | 10 |
| San Vicente de la Barquera | 1 969 | 53 | 1 916 | 0 | **1 916** | 310 (16 %) | 44 |
| Herrerías | 1 911 | 17 | 1 894 | 0 | **1 894** | 317 (17 %) | 47 |
| Selaya | 1 846 | 0 | 1 846 | 0 | **1 846** | 539 (29 %) | 20 |
| Ribamontán al Mar | 1 789 | 40 | 1 749 | 0 | **1 749** | 108 (6 %) | 17 |
| Liérganes | 1 745 | 8 | 1 737 | 0 | **1 737** | 275 (16 %) | 98 |
| Camargo | 1 761 | 25 | 1 736 | 76 | **1 660** | 90 (5 %) | 69 |
| Santiurde de Toranzo | 1 738 | 22 | 1 716 | 0 | **1 716** | 390 (23 %) | 27 |
| San Felices de Buelna | 1 710 | 9 | 1 701 | 0 | **1 701** | 435 (26 %) | 27 |
| San Roque de Riomiera | 1 696 | 0 | 1 696 | 0 | **1 696** | 519 (31 %) | 26 |
| Puente Viesgo | 1 703 | 8 | 1 695 | 0 | **1 695** | 375 (22 %) | 51 |
| Santander | 1 682 | 4 | 1 678 | 0 | **1 678** | 3 (0 %) | 124 |
| Bárcena de Cicero | 1 780 | 105 | 1 675 | 0 | **1 675** | 197 (12 %) | 28 |
| Torrelavega | 1 679 | 16 | 1 663 | 0 | **1 663** | 68 (4 %) | 93 |
| San Miguel de Aguayo | 1 684 | 92 | 1 592 | 0 | **1 592** | 345 (22 %) | 24 |
| Miera | 1 590 | 0 | 1 590 | 0 | **1 590** | 698 (44 %) | 21 |
| Cabezón de la Sal | 1 572 | 8 | 1 564 | 0 | **1 564** | 195 (12 %) | 33 |
| Ramales de la Victoria | 1 547 | 13 | 1 534 | 0 | **1 534** | 233 (15 %) | 40 |
| Bareyo | 1 527 | 10 | 1 517 | 0 | **1 517** | 86 (6 %) | 7 |
| Ampuero | 1 530 | 23 | 1 507 | 0 | **1 507** | 118 (8 %) | 18 |
| Penagos | 1 500 | 4 | 1 496 | 0 | **1 496** | 260 (17 %) | 113 |
| Reocín | 1 516 | 21 | 1 495 | 0 | **1 495** | 136 (9 %) | 51 |
| Santiurde de Reinosa | 1 445 | 3 | 1 442 | 0 | **1 442** | 240 (17 %) | 11 |
| Riotuerto | 1 440 | 1 | 1 439 | 0 | **1 439** | 206 (14 %) | 180 |
| Bárcena de Pie de Concha | 1 439 | 4 | 1 435 | 0 | **1 435** | 341 (24 %) | 7 |
| Villafufre | 1 407 | 1 | 1 406 | 0 | **1 406** | 286 (20 %) | 7 |
| Marina de Cudeyo | 1 376 | 26 | 1 350 | 0 | **1 350** | 147 (11 %) | 22 |
| Santillana del Mar | 1 349 | 3 | 1 346 | 0 | **1 346** | 205 (15 %) | 26 |
| Villaescusa | 1 344 | 9 | 1 335 | 0 | **1 335** | 82 (6 %) | 36 |
| Liendo | 1 254 | 0 | 1 254 | 0 | **1 254** | 136 (11 %) | 8 |
| Medio Cudeyo | 1 257 | 16 | 1 241 | 0 | **1 241** | 69 (6 %) | 79 |
| Solórzano | 1 204 | 0 | 1 204 | 0 | **1 204** | 164 (14 %) | 13 |
| Arnuero | 1 169 | 24 | 1 145 | 0 | **1 145** | 54 (5 %) | 13 |
| Suances | 1 169 | 38 | 1 131 | 0 | **1 131** | 100 (9 %) | 14 |
| Miengo | 1 160 | 53 | 1 107 | 0 | **1 107** | 127 (11 %) | 11 |
| Hazas de Cesto | 1 040 | 2 | 1 038 | 0 | **1 038** | 142 (14 %) | 20 |
| Anievas | 984 | 0 | 984 | 0 | **984** | 270 (27 %) | 13 |
| Udías | 929 | 0 | 929 | 0 | **929** | 100 (11 %) | 5 |
| Valle de Villaverde | 923 | 0 | 923 | 0 | **923** | 96 (10 %) | 49 |
| Castañeda | 906 | 12 | 894 | 0 | **894** | 15 (2 %) | 127 |
| Cartes | 898 | 6 | 892 | 0 | **892** | 64 (7 %) | 36 |
| Comillas | 880 | 1 | 879 | 0 | **879** | 46 (5 %) | 14 |
| Escalante | 938 | 76 | 862 | 0 | **862** | 101 (12 %) | 7 |
| Polanco | 847 | 2 | 845 | 0 | **845** | 25 (3 %) | 18 |
| Saro | 846 | 1 | 845 | 0 | **845** | 172 (20 %) | 27 |
| Santa Cruz de Bezana | 814 | 0 | 814 | 0 | **814** | 37 (5 %) | 12 |
| Meruelo | 777 | 2 | 775 | 0 | **775** | 63 (8 %) | 9 |
| Tresviso | 764 | 0 | 764 | 0 | **764** | 226 (30 %) | 5 |
| Ruiloba | 714 | 0 | 714 | 0 | **714** | 60 (8 %) | 4 |
| Laredo | 750 | 44 | 706 | 0 | **706** | 59 (8 %) | 30 |
| Santoña | 552 | 39 | 513 | 16 | **497** | 30 (6 %) | 10 |
| Limpias | 477 | 16 | 461 | 0 | **461** | 32 (7 %) | 9 |
| Pesquera | 421 | 3 | 418 | 0 | **418** | 102 (24 %) | 2 |
| Noja | 419 | 16 | 403 | 0 | **403** | 15 (4 %) | 15 |
| Potes | 356 | 0 | 356 | 0 | **356** | 8 (2 %) | 4 |
| El Astillero | 313 | 13 | 300 | 0 | **300** | 4 (1 %) | 24 |
| Argoños | 264 | 4 | 260 | 0 | **260** | 14 (5 %) | 14 |
| Colindres | 282 | 26 | 256 | 0 | **256** | 7 (3 %) | 14 |
| Reinosa | 191 | 5 | 186 | 0 | **186** | 5 (3 %) | 11 |

## Parcs (4384)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Bois de Vega de Liébana (18) ⚠️ | Vega de Liébana | 11 335 |
| Forêt de Castro-Urdiales (94) ⚠️ | Castro-Urdiales | 1 409 |
| Bois de Hermandad de Campoo de Suso (5) ⚠️ | Hermandad de Campoo de Suso | 1 399 |
| Forêt de Ruente (13) ⚠️ | Ruente | 1 286 |
| Forêt de Mancomunidad de Campoo-Cabuérniga ⚠️ | Mancomunidad de Campoo-Cabuérniga | 1 255 |
| Forêt de Guriezo (41) ⚠️ | Guriezo | 1 196 |
| Forêt de Alfoz de Lloredo (17) ⚠️ | Alfoz de Lloredo | 1 165 |
| Forêt de Castañeda (20) ⚠️ | Castañeda | 1 105 |
| Forêt de Ribamontán al Monte (7) ⚠️ | Ribamontán al Monte | 1 075 |
| Forêt de Valderredible (65) ⚠️ | Valderredible | 822 |
| Forêt de Valderredible (14) ⚠️ | Valderredible | 685 |
| Forêt de Molledo (16) ⚠️ | Molledo | 629 |
| Bois de Voto (16) ⚠️ | Voto | 616 |
| Bois de Rionansa (4) ⚠️ | Rionansa | 608 |
| Forêt de Hermandad de Campoo de Suso (20) ⚠️ | Hermandad de Campoo de Suso | 607 |
| Bois de Camaleño (24) ⚠️ | Camaleño | 578 |
| Forêt de Lamasón (40) ⚠️ | Lamasón | 566 |
| Forêt de Comillas (3) ⚠️ | Comillas | 540 |
| Bois de Guriezo (2) ⚠️ | Guriezo | 516 |
| Forêt de Piélagos (41) ⚠️ | Piélagos | 511 |
| Forêt de Valderredible (25) ⚠️ | Valderredible | 505 |
| Forêt de Los Tojos (13) ⚠️ | Los Tojos | 491 |
| Bois de Arenas de Iguña (3) ⚠️ | Arenas de Iguña | 486 |
| Bois de Arenas de Iguña (5) ⚠️ | Arenas de Iguña | 453 |
| Forêt de Piélagos (42) ⚠️ | Piélagos | 441 |
| Bois de San Felices de Buelna (5) ⚠️ | San Felices de Buelna | 440 |
| Forêt de Peñarrubia (9) ⚠️ | Peñarrubia | 440 |
| Forêt de Los Tojos (23) ⚠️ | Los Tojos | 435 |
| Monte Hijedo ⚠️ | Valderredible | 421 |
| Forêt de Ruesga (24) ⚠️ | Ruesga | 418 |
| Forêt de Valderredible (57) ⚠️ | Valderredible | 414 |
| Forêt de Valdeprado del Río (4) ⚠️ | Valdeprado del Río | 407 |
| Forêt de Ribamontán al Mar ⚠️ | Ribamontán al Mar | 405 |
| Forêt de Soba (69) ⚠️ | Soba | 372 |
| Forêt de Tresviso (3) ⚠️ | Tresviso | 357 |
| Forêt de Polaciones ⚠️ | Polaciones | 353 |
| Forêt de Soba (13) ⚠️ | Soba | 351 |
| Forêt de Hermandad de Campoo de Suso (12) ⚠️ | Hermandad de Campoo de Suso | 341 |
| Forêt de Valdeolea (3) ⚠️ | Valdeolea | 326 |
| Forêt de Mazcuerras (25) ⚠️ | Mazcuerras | 322 |
| Forêt de Santiurde de Reinosa (2) ⚠️ | Santiurde de Reinosa | 313 |
| Forêt de Valderredible (71) ⚠️ | Valderredible | 313 |
| Forêt de Ampuero (7) ⚠️ | Ampuero | 308 |
| Forêt de Hermandad de Campoo de Suso (9) ⚠️ | Hermandad de Campoo de Suso | 298 |
| Forêt de San Pedro del Romeral (2) ⚠️ | San Pedro del Romeral | 295 |
| Forêt de Bárcena de Cicero (13) ⚠️ | Bárcena de Cicero | 295 |
| Forêt de Valderredible (78) ⚠️ | Valderredible | 295 |
| Forêt de Cabezón de la Sal (3) ⚠️ | Cabezón de la Sal | 285 |
| Bois de Los Corrales de Buelna ⚠️ | Los Corrales de Buelna | 285 |
| Forêt de Escalante ⚠️ | Escalante | 274 |
| Forêt de Valdeprado del Río (15) ⚠️ | Valdeprado del Río | 266 |
| Forêt de Cieza (8) ⚠️ | Cieza | 260 |
| Bois de Cabuérniga ⚠️ | Cabuérniga | 259 |
| Forêt de Cabuérniga (3) ⚠️ | Cabuérniga | 255 |
| Forêt de Cabezón de la Sal (24) ⚠️ | Cabezón de la Sal | 255 |
| Hayedos de Uznayo ⚠️ | Polaciones | 254 |
| Forêt de Valderredible (13) ⚠️ | Valderredible | 249 |
| Forêt de Cillorigo de Liébana ⚠️ | Cillorigo de Liébana | 240 |
| Forêt de Valdeprado del Río ⚠️ | Valdeprado del Río | 237 |
| Forêt de Valderredible (64) ⚠️ | Valderredible | 236 |
| Bois de Camaleño (2) ⚠️ | Camaleño | 234 |
| Forêt de San Miguel de Aguayo (7) ⚠️ | San Miguel de Aguayo | 234 |
| Forêt de Tudanca (20) ⚠️ | Tudanca | 230 |
| Forêt de Hermandad de Campoo de Suso (2) ⚠️ | Hermandad de Campoo de Suso | 227 |
| Forêt de Santoña ⚠️ | Santoña | 220 |
| Forêt de San Miguel de Aguayo (2) ⚠️ | San Miguel de Aguayo | 214 |
| Forêt de Valderredible (69) ⚠️ | Valderredible | 211 |
| Forêt de Udías (5) ⚠️ | Udías | 211 |
| Forêt de Voto (6) ⚠️ | Voto | 206 |
| Forêt de Valderredible (42) ⚠️ | Valderredible | 205 |
| Forêt de Valderredible (12) ⚠️ | Valderredible | 204 |
| Forêt de Guriezo (11) ⚠️ | Guriezo | 202 |
| Forêt de Soba (80) ⚠️ | Soba | 201 |
| Forêt de Limpias (2) ⚠️ | Limpias | 200 |
| Forêt de Cillorigo de Liébana (19) ⚠️ | Cillorigo de Liébana | 200 |
| Forêt de Valderredible (61) ⚠️ | Valderredible | 200 |
| Forêt de San Pedro del Romeral ⚠️ | San Pedro del Romeral | 194 |
| Forêt de San Miguel de Aguayo (4) ⚠️ | San Miguel de Aguayo | 194 |
| Forêt de Valderredible (72) ⚠️ | Valderredible | 186 |
| Forêt de Hermandad de Campoo de Suso (8) ⚠️ | Hermandad de Campoo de Suso | 184 |
| Forêt de Castro-Urdiales (24) ⚠️ | Castro-Urdiales | 182 |
| Forêt de Rasines (7) ⚠️ | Rasines | 181 |
| Forêt de Arredondo (8) ⚠️ | Arredondo | 181 |
| Forêt de Valdeprado del Río (26) ⚠️ | Valdeprado del Río | 181 |
| Bois de Bárcena de Pie de Concha ⚠️ | Bárcena de Pie de Concha | 172 |
| Forêt de Soba (75) ⚠️ | Soba | 170 |
| Forêt de Tudanca ⚠️ | Tudanca | 169 |
| Forêt de Cabuérniga (12) ⚠️ | Cabuérniga | 166 |
| Forêt de Tudanca (21) ⚠️ | Tudanca | 162 |
| Forêt de Voto (8) ⚠️ | Voto | 161 |
| Forêt de Tudanca (29) ⚠️ | Tudanca | 161 |
| Forêt de Ruesga (5) ⚠️ | Ruesga | 158 |
| Forêt de Bárcena de Pie de Concha (2) ⚠️ | Bárcena de Pie de Concha | 157 |
| Forêt de Ruesga (31) ⚠️ | Ruesga | 157 |
| Bois de Luena ⚠️ | Luena | 157 |
| Forêt de Val de San Vicente ⚠️ | Val de San Vicente | 156 |
| Forêt de Cartes (6) ⚠️ | Cartes | 155 |
| Forêt de Guriezo (9) ⚠️ | Guriezo | 150 |
| Bois de Ramales de la Victoria (12) ⚠️ | Ramales de la Victoria | 149 |
| Forêt de Molledo ⚠️ | Molledo | 146 |
| Forêt de Rasines (5) ⚠️ | Rasines | 146 |
| Forêt de Entrambasaguas (7) ⚠️ | Entrambasaguas | 145 |
| El Tamareo ⚠️ | Hermandad de Campoo de Suso | 144 |
| Forêt de Corvera de Toranzo (11) ⚠️ | Corvera de Toranzo | 144 |
| Forêt de Argoños ⚠️ | Argoños | 143 |
| Forêt de Valderredible (63) ⚠️ | Valderredible | 143 |
| Forêt de Miera (9) ⚠️ | Miera | 142 |
| Forêt de Cieza (2) ⚠️ | Cieza | 141 |
| Forêt de Meruelo (6) ⚠️ | Meruelo | 140 |
| Forêt de Solórzano (5) ⚠️ | Solórzano | 139 |
| Forêt de Herrerías (21) ⚠️ | Herrerías | 138 |
| Forêt de Soba (23) ⚠️ | Soba | 138 |
| Forêt de Rasines (6) ⚠️ | Rasines | 136 |
| Forêt de Valderredible (37) ⚠️ | Valderredible | 135 |
| Robledal del Monte Arria ⚠️ | Lamasón | 134 |
| Forêt de Valle de Villaverde (43) ⚠️ | Valle de Villaverde | 133 |
| Forêt de Molledo (2) ⚠️ | Molledo | 132 |
| Bois de Valderredible (26) ⚠️ | Valderredible | 132 |
| Forêt de Valderredible (48) ⚠️ | Valderredible | 131 |
| Forêt de Entrambasaguas (16) ⚠️ | Entrambasaguas | 130 |
| Forêt de Villacarriedo (16) ⚠️ | Villacarriedo | 130 |
| El Monterín ⚠️ | Camargo | 130 |
| Forêt de Peñarrubia (3) ⚠️ | Peñarrubia | 129 |
| Forêt de Val de San Vicente (10) ⚠️ | Val de San Vicente | 128 |
| Forêt de San Pedro del Romeral (10) ⚠️ | San Pedro del Romeral | 128 |
| Forêt de Peñarrubia (2) ⚠️ | Peñarrubia | 127 |
| Forêt de Guriezo (33) ⚠️ | Guriezo | 127 |
| Forêt de Valderredible (23) ⚠️ | Valderredible | 126 |
| Forêt de Liendo (2) ⚠️ | Liendo | 126 |
| Bois de Valderredible (10) ⚠️ | Valderredible | 126 |
| Forêt de Arenas de Iguña (6) | Arenas de Iguña | 125 |
| Forêt de Luena (26) | Luena | 124 |
| Forêt de Voto (5) | Voto | 122 |
| Forêt de Ruesga (21) | Ruesga | 122 |
| Bois de Las Rozas de Valdearroyo | Las Rozas de Valdearroyo | 122 |
| Forêt de Puente Viesgo (24) | Puente Viesgo | 120 |
| Forêt de Polaciones (12) | Polaciones | 119 |
| Forêt de Ruente (3) | Ruente | 119 |
| Forêt de Mazcuerras (17) | Mazcuerras | 117 |
| Forêt de Santiurde de Reinosa (5) | Santiurde de Reinosa | 115 |
| Forêt de Puente Viesgo (22) | Puente Viesgo | 115 |
| Forêt de Guriezo (19) | Guriezo | 113 |
| Forêt de Peñarrubia (7) | Peñarrubia | 113 |
| Forêt de Valdáliga (49) | Valdáliga | 113 |
| Forêt de Campoo de Enmedio (3) | Campoo de Enmedio | 112 |
| Forêt de Soba (77) | Soba | 111 |
| Forêt de Valdáliga (52) | Valdáliga | 110 |
| Forêt de Liendo | Liendo | 109 |
| Forêt de Campoo de Enmedio (6) | Campoo de Enmedio | 109 |
| Forêt de Los Corrales de Buelna (2) | Los Corrales de Buelna | 108 |
| Forêt de Soba (81) | Soba | 107 |
| Forêt de Valderredible (20) | Valderredible | 106 |
| Forêt de Las Rozas de Valdearroyo (3) | Las Rozas de Valdearroyo | 106 |
| Forêt de Rasines (2) | Rasines | 106 |
| Forêt de Valdáliga (9) | Valdáliga | 105 |
| Forêt de Mazcuerras (24) | Mazcuerras | 104 |
| Forêt de Vega de Pas (41) | Vega de Pas | 104 |
| Forêt de San Vicente de la Barquera (6) | San Vicente de la Barquera | 103 |
| Forêt de Lamasón (13) | Lamasón | 101 |
| Forêt de Cabuérniga (8) | Cabuérniga | 100 |
| Forêt de Molledo (6) | Molledo | 99 |
| Forêt de Ruesga (30) | Ruesga | 99 |
| Abeludar de Ajoto | Lamasón | 99 |
| Forêt de Entrambasaguas (8) | Entrambasaguas | 98 |
| Robledal y hayedo de San Sebastián de Garabandal | Rionansa | 96 |
| Forêt de Valdáliga (10) | Valdáliga | 96 |
| Forêt de Valderredible (15) | Valderredible | 96 |
| Forêt de Santiurde de Toranzo (2) | Santiurde de Toranzo | 95 |
| Forêt de Ramales de la Victoria (2) | Ramales de la Victoria | 94 |
| Forêt de Ruesga (22) | Ruesga | 92 |
| Forêt de Cabezón de la Sal (10) | Cabezón de la Sal | 91 |
| Forêt de San Felices de Buelna (6) | San Felices de Buelna | 90 |
| Forêt de Anievas (2) | Anievas | 89 |
| Forêt de Valderredible (62) | Valderredible | 89 |
| Forêt de Soba (7) | Soba | 88 |
| Forêt de Corvera de Toranzo (5) | Corvera de Toranzo | 88 |
| Forêt de Rionansa (29) | Rionansa | 88 |
| Forêt de Medio Cudeyo (4) | Medio Cudeyo | 88 |
| Forêt de Bárcena de Cicero (5) | Bárcena de Cicero | 87 |
| Forêt de Puente Viesgo (21) | Puente Viesgo | 87 |
| Forêt de Ramales de la Victoria (3) | Ramales de la Victoria | 86 |
| Forêt de Castro-Urdiales (52) | Castro-Urdiales | 86 |
| Forêt de Herrerías (26) | Herrerías | 85 |
| Forêt de Valdeprado del Río (17) | Valdeprado del Río | 85 |
| Forêt de Ruesga (19) | Ruesga | 85 |
| Forêt de Hazas de Cesto (5) | Hazas de Cesto | 85 |
| Forêt de Vega de Pas (29) | Vega de Pas | 85 |
| Forêt de Hermandad de Campoo de Suso (3) | Hermandad de Campoo de Suso | 84 |
| Forêt de Reocín (7) | Reocín | 84 |
| Hayedo de Peñagafa | Vega de Pas | 84 |
| Forêt de Valdáliga (59) | Valdáliga | 83 |
| Forêt de Valderredible (70) | Valderredible | 82 |
| Forêt de Mazcuerras (4) | Mazcuerras | 81 |
| Forêt de Corvera de Toranzo (6) | Corvera de Toranzo | 81 |
| Forêt de Valdeprado del Río (25) | Valdeprado del Río | 80 |
| Forêt de Liérganes (31) | Liérganes | 80 |
| Forêt de Herrerías (14) | Herrerías | 79 |
| Forêt de Santiurde de Toranzo (6) | Santiurde de Toranzo | 79 |
| Forêt de Valdeprado del Río (20) | Valdeprado del Río | 79 |
| Forêt de Santa María de Cayón (80) | Santa María de Cayón | 77 |
| Forêt de Soba (8) | Soba | 76 |
| Forêt de Luena (24) | Luena | 76 |
| Forêt de Castro-Urdiales (98) | Castro-Urdiales | 75 |
| Forêt de San Pedro del Romeral (8) | San Pedro del Romeral | 74 |
| Forêt de Anievas (7) | Anievas | 74 |
| Forêt de Camaleño (13) | Camaleño | 74 |
| Forêt de Rionansa (15) | Rionansa | 73 |
| Forêt de Rionansa (22) | Rionansa | 73 |
| Forêt de Santiurde de Toranzo | Santiurde de Toranzo | 72 |
| Forêt de Cabuérniga (7) | Cabuérniga | 72 |
| Forêt de Santa María de Cayón (81) | Saro | 72 |
| Forêt de Herrerías (37) | Val de San Vicente | 71 |
| Forêt de Ampuero (8) | Ampuero | 70 |
| Forêt de Val de San Vicente (44) | Val de San Vicente | 70 |
| Forêt de Torrelavega (36) | Torrelavega | 70 |
| Forêt de Campoo de Yuso (3) | Campoo de Yuso | 69 |
| Forêt de Molledo (4) | Molledo | 68 |
| Forêt de Valderredible (17) | Valderredible | 68 |
| Forêt de Valdáliga (21) | Valdáliga | 68 |
| Forêt de Los Corrales de Buelna (4) | Los Corrales de Buelna | 67 |
| Forêt de Valle de Villaverde (2) | Valle de Villaverde | 67 |
| Forêt de Voto (11) | Voto | 67 |
| Forêt de Hazas de Cesto (2) | Bárcena de Cicero | 66 |
| Forêt de Val de San Vicente (7) | Val de San Vicente | 66 |
| Bois de Arnuero | Arnuero | 66 |
| Forêt de Ramales de la Victoria (11) | Ramales de la Victoria | 66 |
| Forêt de Campoo de Enmedio (2) | Campoo de Enmedio | 65 |
| Forêt de Val de San Vicente (22) | Val de San Vicente | 65 |
| Bois de Vega de Pas | Vega de Pas | 64 |
| Bois de Ramales de la Victoria | Ramales de la Victoria | 64 |
| Forêt de Santiurde de Reinosa (4) | Santiurde de Reinosa | 63 |
| Forêt de Valderredible (29) | Valderredible | 62 |
| Forêt de Luena (20) | Luena | 62 |
| Forêt de Mazcuerras (22) | Mazcuerras | 62 |
| Forêt de Valdáliga (48) | Valdáliga | 62 |
| Forêt de San Miguel de Aguayo (24) | San Miguel de Aguayo | 62 |
| Forêt de Valderredible (77) | Valderredible | 62 |
| Forêt de Ruente | Ruente | 61 |
| Forêt de Rionansa (30) | Rionansa | 61 |
| Forêt de Voto (3) | Voto | 60 |
| Forêt de Soba (24) | Soba | 60 |
| Forêt de Luena (33) | Luena | 60 |
| Forêt de Arnuero | Arnuero | 58 |
| Forêt de Tudanca (2) | Tudanca | 58 |
| Forêt de Mazcuerras (6) | Mazcuerras | 58 |
| Forêt de Villaescusa (2) | Villaescusa | 58 |
| Forêt de Alfoz de Lloredo (4) | Alfoz de Lloredo | 58 |
| Bois de Valderredible (18) | Valderredible | 58 |
| Pinar de Liencres | Piélagos | 57 |
| Forêt de Cartes (2) | Cartes | 57 |
| Forêt de Rionansa (5) | Rionansa | 57 |
| Forêt de Soba (17) | Soba | 57 |
| Forêt de Cabuérniga (22) | Cabuérniga | 57 |
| Forêt de Vega de Pas (35) | Vega de Pas | 57 |
| Forêt de Las Rozas de Valdearroyo (16) | Las Rozas de Valdearroyo | 57 |
| Forêt de Cillorigo de Liébana (6) | Cillorigo de Liébana | 56 |
| Forêt de Hermandad de Campoo de Suso (18) | Hermandad de Campoo de Suso | 56 |
| Forêt de Corvera de Toranzo | Corvera de Toranzo | 55 |
| Forêt de Cartes (26) | Cartes | 55 |
| Forêt de Mazcuerras | Mazcuerras | 54 |
| Forêt de Corvera de Toranzo (7) | Corvera de Toranzo | 54 |
| Forêt de Campoo de Yuso (14) | Campoo de Yuso | 54 |
| Forêt de Molledo (3) | Molledo | 53 |
| Forêt de Arredondo (2) | Arredondo | 53 |
| Forêt de Luena (9) | Luena | 53 |
| Forêt de Reocín (4) | Reocín | 53 |
| Forêt de Villaescusa (3) | Villaescusa | 53 |
| Forêt de Cillorigo de Liébana (21) | Cillorigo de Liébana | 53 |
| Forêt de Hermandad de Campoo de Suso | Hermandad de Campoo de Suso | 52 |
| Forêt de Luena (25) | Luena | 52 |
| Forêt de Soba (53) | Soba | 52 |
| Bois de Arenas de Iguña (2) | Arenas de Iguña | 51 |
| Forêt de Molledo (12) | Molledo | 50 |
| Forêt de Cillorigo de Liébana (14) | Cillorigo de Liébana | 50 |
| Forêt de Santiurde de Reinosa (3) | Santiurde de Reinosa | 50 |
| Forêt de Soba (26) | Soba | 50 |
| Forêt de Lamasón (36) | Lamasón | 50 |
| Forêt de Guriezo (24) | Guriezo | 50 |
| Forêt de Selaya (2) | Selaya | 49 |
| Forêt de Cillorigo de Liébana (3) | Cillorigo de Liébana | 49 |
| Forêt de Cillorigo de Liébana (9) | Cillorigo de Liébana | 49 |
| Forêt de Valdeprado del Río (8) | Valdeprado del Río | 49 |
| Forêt de Tudanca (17) | Tudanca | 49 |
| Forêt de Entrambasaguas (54) | Entrambasaguas | 49 |
| Bois de San Roque de Riomiera (13) | San Roque de Riomiera | 49 |
| Forêt de Rionansa (14) | Rionansa | 48 |
| Forêt de Rasines | Rasines | 48 |
| Forêt de Villafufre | Villafufre | 48 |
| Forêt de Voto (7) | Voto | 48 |
| Forêt de Voto (10) | Voto | 48 |
| Forêt de Valderredible (47) | Valderredible | 48 |
| Forêt de Rionansa (53) | Rionansa | 48 |
| Forêt de Cartes | Cartes | 47 |
| Forêt de Campoo de Yuso (2) | Campoo de Yuso | 47 |
| Forêt de Valdáliga (26) | Valdáliga | 47 |
| Forêt de Mazcuerras (16) | Mazcuerras | 47 |
| Forêt de Soba (27) | Soba | 47 |
| Abedular de Tisuerra | Hermandad de Campoo de Suso | 47 |
| Forêt de Selaya (3) | Selaya | 46 |
| Forêt de Valdáliga (31) | Valdáliga | 46 |
| Forêt de Los Tojos (2) | Los Tojos | 45 |
| Forêt de Valdáliga (24) | Valdáliga | 45 |
| Forêt de Arenas de Iguña (7) | Arenas de Iguña | 45 |
| Forêt de Peñarrubia (6) | Peñarrubia | 45 |
| Bois de San Roque de Riomiera (14) | San Roque de Riomiera | 45 |
| Forêt de Soba (4) | Soba | 44 |
| Forêt de Cillorigo de Liébana (10) | Cillorigo de Liébana | 44 |
| Forêt de Rasines (3) | Rasines | 44 |
| Forêt de Cabuérniga (13) | Cabuérniga | 44 |
| Forêt de Valderredible (40) | Valderredible | 44 |
| Forêt de Vega de Pas (16) | Vega de Pas | 44 |
| Forêt de Hermandad de Campoo de Suso (17) | Hermandad de Campoo de Suso | 44 |
| Forêt de Puente Viesgo (14) | Puente Viesgo | 44 |
| Forêt de Riotuerto (156) | Riotuerto | 44 |
| Forêt de Voto | Voto | 43 |
| Bois de Los Corrales de Buelna (2) | Los Corrales de Buelna | 43 |
| Forêt de San Vicente de la Barquera | San Vicente de la Barquera | 43 |
| Forêt de San Roque de Riomiera (4) | San Roque de Riomiera | 43 |
| Forêt de Val de San Vicente (11) | Val de San Vicente | 43 |
| Forêt de Luena (19) | Luena | 43 |
| Forêt de Arenas de Iguña (15) | Arenas de Iguña | 43 |
| Forêt de Voto (14) | Voto | 43 |
| Forêt de Polaciones (10) | Polaciones | 42 |
| Forêt de Piélagos (5) | Piélagos | 42 |
| Forêt de Vega de Pas (10) | Vega de Pas | 42 |
| Forêt de Valdáliga (36) | Valdáliga | 42 |
| Forêt de Soba (16) | Soba | 42 |
| Forêt de Luena (18) | Luena | 42 |
| Bois de Camaleño | Camaleño | 41 |
| Forêt de Bárcena de Cicero (3) | Bárcena de Cicero | 41 |
| Forêt de Santiurde de Toranzo (5) | Santiurde de Toranzo | 41 |
| Forêt de Campoo de Enmedio (5) | Campoo de Enmedio | 41 |
| Forêt de Bareyo | Bareyo | 40 |
| Forêt de Ampuero (5) | Ampuero | 40 |
| Forêt de Entrambasaguas (10) | Entrambasaguas | 40 |
| Forêt de Luena (10) | Luena | 40 |
| Forêt de Cieza (7) | Cieza | 40 |
| Forêt de Ribamontán al Monte (2) | Ribamontán al Monte | 40 |
| Forêt de Villacarriedo (7) | Villacarriedo | 40 |
| Forêt de Ramales de la Victoria (12) | Ramales de la Victoria | 40 |
| Forêt de Las Rozas de Valdearroyo (2) | Las Rozas de Valdearroyo | 39 |
| Forêt de Arenas de Iguña (2) | Arenas de Iguña | 39 |
| Forêt de Vega de Pas (6) | Vega de Pas | 39 |
| Forêt de Cabuérniga (18) | Cabuérniga | 39 |
| Forêt de Polanco | Polanco | 39 |
| Forêt de Castro-Urdiales (96) | Castro-Urdiales | 39 |
| Bois de Soba (16) | Soba | 39 |
| Forêt de Castro-Urdiales | Castro-Urdiales | 38 |
| Forêt de Lamasón (3) | Lamasón | 38 |
| Forêt de Camargo | Camargo | 38 |
| Forêt de Luena (8) | Luena | 38 |
| Forêt de Las Rozas de Valdearroyo (9) | Las Rozas de Valdearroyo | 38 |
| Forêt de Saro (2) | Saro | 38 |
| Forêt de Rasines (10) | Rasines | 38 |
| Forêt de Soba (40) | Soba | 38 |
| Forêt de San Felices de Buelna (2) | San Felices de Buelna | 37 |
| Forêt de Piélagos (2) | Piélagos | 37 |
| Forêt de San Roque de Riomiera (6) | San Roque de Riomiera | 37 |
| Forêt de Lamasón (33) | Lamasón | 37 |
| Parque de interpretación de la cantera de Cuchía | Miengo | 36 |
| Forêt de Val de San Vicente (4) | Val de San Vicente | 36 |
| Forêt de Vega de Pas (8) | Vega de Pas | 36 |
| Forêt de Cabuérniga (11) | Cabuérniga | 36 |
| Forêt de Soba (20) | Soba | 36 |
| Forêt de Villaescusa (4) | Villaescusa | 36 |
| Bois de Valderredible (24) | Valderredible | 36 |
| Forêt de Herrerías | Herrerías | 35 |
| Forêt de Peñarrubia | Peñarrubia | 35 |
| Forêt de Campoo de Enmedio | Campoo de Enmedio | 35 |
| Forêt de Valderredible (49) | Valderredible | 35 |
| Forêt de Valderredible (50) | Valderredible | 35 |
| Forêt de Val de San Vicente (16) | Val de San Vicente | 35 |
| Forêt de Polaciones (53) | Polaciones | 35 |
| Forêt de Puente Viesgo (13) | Puente Viesgo | 35 |
| Forêt de Cillorigo de Liébana (2) | Cillorigo de Liébana | 34 |
| Forêt de Valderredible (21) | Valderredible | 34 |
| Forêt de Mazcuerras (7) | Mazcuerras | 34 |
| Forêt de Cillorigo de Liébana (8) | Cillorigo de Liébana | 34 |
| Forêt de Villacarriedo (4) | Villacarriedo | 34 |
| Forêt de San Vicente de la Barquera (8) | San Vicente de la Barquera | 34 |
| Forêt de Solórzano (12) | Solórzano | 34 |
| Forêt de Val de San Vicente (43) | Val de San Vicente | 34 |
| Forêt de Comillas | Comillas | 33 |
| Forêt de Cillorigo de Liébana (4) | Cillorigo de Liébana | 33 |
| Forêt de Mazcuerras (8) | Mazcuerras | 33 |
| Forêt de Molledo (7) | Molledo | 33 |
| Forêt de Valderredible (30) | Valderredible | 33 |
| Forêt de Bárcena de Pie de Concha (4) | Bárcena de Pie de Concha | 33 |
| Forêt de Lamasón (26) | Lamasón | 33 |
| Forêt de Vega de Pas (18) | Vega de Pas | 33 |
| Forêt de Alfoz de Lloredo (8) | Alfoz de Lloredo | 33 |
| Forêt de Valderredible (58) | Valderredible | 33 |
| Forêt de Corvera de Toranzo (12) | Corvera de Toranzo | 33 |
| Bois de Valdeolea (7) | Valdeolea | 33 |
| Forêt de Soba (76) | Soba | 33 |
| Forêt de San Pedro del Romeral (3) | San Pedro del Romeral | 32 |
| Forêt de Los Corrales de Buelna (10) | Los Corrales de Buelna | 32 |
| Forêt de Herrerías (32) | Herrerías | 32 |
| Forêt de Valderredible (52) | Valderredible | 32 |
| Forêt de Ruente (9) | Ruente | 32 |
| Forêt de Valdáliga (50) | Valdáliga | 32 |
| Forêt de Soba (61) | Soba | 32 |
| Forêt de Camaleño (14) | Camaleño | 32 |
| Bois de Valderredible (30) | Valderredible | 32 |
| Forêt de Piélagos (7) | Piélagos | 31 |
| Forêt de Cabezón de Liébana (3) | Cabezón de Liébana | 31 |
| Forêt de Ampuero (11) | Ampuero | 31 |
| Forêt de Castro-Urdiales (62) | Castro-Urdiales | 31 |
| Forêt de Luena (31) | Luena | 31 |
| Monte El Henar | Villaescusa | 31 |
| Forêt de Selaya | Selaya | 30 |
| Forêt de Cabuérniga | Cabuérniga | 30 |
| Forêt de Rionansa (11) | Rionansa | 30 |
| Forêt de Hermandad de Campoo de Suso (7) | Hermandad de Campoo de Suso | 30 |
| Forêt de Lamasón (12) | Lamasón | 30 |
| Forêt de Hermandad de Campoo de Suso (11) | Hermandad de Campoo de Suso | 30 |
| Forêt de Hermandad de Campoo de Suso (15) | Hermandad de Campoo de Suso | 30 |
| Forêt de Valdeprado del Río (14) | Valdeprado del Río | 30 |
| Forêt de Valdáliga (44) | Valdáliga | 30 |
| Forêt de Valderredible (56) | Valderredible | 30 |
| Forêt de Camaleño (6) | Camaleño | 30 |
| Forêt de Torrelavega (35) | Torrelavega | 30 |
| Forêt de San Felices de Buelna (17) | San Felices de Buelna | 30 |
| Forêt de Campoo de Yuso (8) | Campoo de Yuso | 29 |
| Forêt de Selaya (5) | Selaya | 29 |
| Forêt de Valle de Villaverde (3) | Valle de Villaverde | 29 |
| Forêt de Valdáliga (42) | Valdáliga | 29 |
| Forêt de Las Rozas de Valdearroyo (12) | Las Rozas de Valdearroyo | 29 |
| Forêt de Piélagos (16) | Piélagos | 29 |
| Forêt de San Miguel de Aguayo (19) | San Miguel de Aguayo | 29 |
| Forêt de Valdáliga (57) | Valdáliga | 29 |
| Forêt de Hermandad de Campoo de Suso (21) | Hermandad de Campoo de Suso | 29 |
| Forêt de Cabuérniga (2) | Cabuérniga | 28 |
| Forêt de San Roque de Riomiera (3) | San Roque de Riomiera | 28 |
| Forêt de Guriezo (5) | Guriezo | 28 |
| Forêt de Cabezón de Liébana (2) | Cabezón de Liébana | 28 |
| Forêt de Anievas (4) | Anievas | 28 |
| Forêt de Selaya (6) | Selaya | 28 |
| Forêt de Ruesga (17) | Ruesga | 28 |
| Forêt de Reocín (6) | Reocín | 28 |
| Forêt de Los Tojos (15) | Los Tojos | 28 |
| Forêt de Luena (23) | Luena | 28 |
| Forêt de Valdeolea (5) | Valdeolea | 28 |
| Forêt de Los Tojos (18) | Los Tojos | 28 |
| Forêt de Castro-Urdiales (53) | Castro-Urdiales | 28 |
| Forêt de Solórzano (2) | Solórzano | 27 |
| Forêt de Valdáliga (15) | Valdáliga | 27 |
| Forêt de Mazcuerras (10) | Mazcuerras | 27 |
| Forêt de Cabuérniga (6) | Cabuérniga | 27 |
| Forêt de Cillorigo de Liébana (7) | Cillorigo de Liébana | 27 |
| Forêt de San Felices de Buelna (5) | Los Corrales de Buelna | 27 |
| Forêt de Val de San Vicente (6) | Val de San Vicente | 27 |
| Forêt de Valle de Villaverde | Valle de Villaverde | 27 |
| Forêt de Selaya (7) | Selaya | 27 |
| Forêt de Cabuérniga (17) | Cabuérniga | 27 |
| Bois de Miera | Miera | 27 |
| Forêt de Torrelavega (7) | Torrelavega | 27 |
| Forêt de Soba (37) | Soba | 27 |
| Forêt de Reocín (28) | Reocín | 27 |
| Forêt de Valderredible (74) | Valderredible | 27 |
| Bois de Entrambasaguas | Entrambasaguas | 26 |
| Forêt de Mazcuerras (2) | Mazcuerras | 26 |
| Forêt de Castro-Urdiales (2) | Castro-Urdiales | 26 |
| Forêt de Comillas (2) | Comillas | 26 |
| Forêt de Solórzano (3) | Solórzano | 26 |
| Forêt de Las Rozas de Valdearroyo (7) | Las Rozas de Valdearroyo | 26 |
| Forêt de San Felices de Buelna (7) | San Felices de Buelna | 26 |
| Forêt de Arenas de Iguña (8) | Arenas de Iguña | 26 |
| Forêt de Vega de Liébana (6) | Vega de Liébana | 26 |
| Forêt de Limpias | Limpias | 26 |
| Forêt de Anievas (6) | Anievas | 26 |
| Forêt de Mazcuerras (20) | Mazcuerras | 26 |
| Forêt de Riotuerto (2) | Riotuerto | 26 |
| Forêt de Rasines (9) | Rasines | 26 |
| Forêt de Voto (12) | Voto | 26 |
| Forêt de Puente Viesgo (9) | Puente Viesgo | 26 |
| Forêt de Herrerías (38) | Herrerías | 26 |
| Hayedo de Guares | Hermandad de Campoo de Suso | 26 |
| Forêt de Arnuero (4) | Arnuero | 26 |
| Forêt de Cieza | Cieza | 25 |
| Forêt de Mazcuerras (3) | Mazcuerras | 25 |
| Forêt de Los Corrales de Buelna | Los Corrales de Buelna | 25 |
| Forêt de Valdáliga (16) | Valdáliga | 25 |
| Forêt de Ampuero (2) | Ampuero | 25 |
| Forêt de Valderredible (18) | Valderredible | 25 |
| Forêt de Campoo de Yuso (5) | Campoo de Yuso | 25 |
| Forêt de Lamasón (9) | Lamasón | 25 |
| Forêt de Mazcuerras (9) | Mazcuerras | 25 |
| Forêt de San Vicente de la Barquera (3) | San Vicente de la Barquera | 25 |
| Forêt de Val de San Vicente (9) | Val de San Vicente | 25 |
| Forêt de Puente Viesgo (5) | Puente Viesgo | 25 |
| Forêt de Lamasón (22) | Lamasón | 25 |
| Forêt de Valdeprado del Río (18) | Valdeprado del Río | 25 |
| Forêt de Miengo | Miengo | 25 |
| Forêt de Meruelo (3) | Meruelo | 25 |
| Forêt de Torrelavega (32) | Torrelavega | 25 |
| Forêt de Vega de Pas (31) | Vega de Pas | 25 |
| Forêt de Arenas de Iguña (3) | Arenas de Iguña | 24 |
| Forêt de Luena (4) | Luena | 24 |
| Forêt de Luena (5) | Luena | 24 |
| Forêt de Santillana del Mar (2) | Santillana del Mar | 24 |
| Forêt de Soba (14) | Soba | 24 |
| Forêt de Valderredible (38) | Valderredible | 24 |
| Forêt de Los Corrales de Buelna (9) | Los Corrales de Buelna | 24 |
| Forêt de Los Tojos (14) | Los Tojos | 24 |
| Forêt de Soba (28) | Soba | 24 |
| Forêt de Piélagos (17) | Piélagos | 24 |
| Forêt de Cabezón de la Sal (23) | Cabezón de la Sal | 24 |
| Forêt de Guriezo (42) | Guriezo | 24 |
| Forêt de Valderredible (8) | Valderredible | 23 |
| Forêt de Ruesga | Ruesga | 23 |
| Forêt de Lamasón (2) | Lamasón | 23 |
| Forêt de Polaciones (17) | Polaciones | 23 |
| Forêt de San Pedro del Romeral (5) | San Pedro del Romeral | 23 |
| Forêt de Valdáliga (28) | Valdáliga | 23 |
| Forêt de Castro-Urdiales (5) | Castro-Urdiales | 23 |
| Forêt de Cillorigo de Liébana (11) | Cillorigo de Liébana | 23 |
| Forêt de Corvera de Toranzo (9) | Corvera de Toranzo | 23 |
| Forêt de Saro (3) | Saro | 23 |
| Forêt de Mazcuerras (21) | Mazcuerras | 23 |
| Forêt de Ribamontán al Mar (3) | Ribamontán al Mar | 23 |
| Forêt de Liérganes (24) | Liérganes | 23 |
| Forêt de Laredo (3) | Laredo | 23 |
| Forêt de Soba (78) | Soba | 23 |
| Bois de Soba (15) | Soba | 23 |
| Bois de Valderredible (16) | Valderredible | 23 |
| Forêt de Castro-Urdiales (3) | Castro-Urdiales | 22 |
| Forêt de Val de San Vicente (5) | Val de San Vicente | 22 |
| Forêt de Piélagos (4) | Piélagos | 22 |
| Forêt de Valdáliga (29) | Valdáliga | 22 |
| Forêt de Valderredible (32) | Valderredible | 22 |
| Forêt de Selaya (4) | Selaya | 22 |
| Forêt de Ampuero (4) | Ampuero | 22 |
| Forêt de Guriezo (14) | Guriezo | 22 |
| Forêt de Soba (15) | Soba | 22 |
| Forêt de Mazcuerras (15) | Mazcuerras | 22 |
| Forêt de Solórzano (4) | Solórzano | 22 |
| Forêt de Penagos | Penagos | 22 |
| Forêt de Udías (2) | Udías | 22 |
| Forêt de San Vicente de la Barquera (7) | San Vicente de la Barquera | 22 |
| Forêt de Camaleño (4) | Camaleño | 22 |
| Forêt de Campoo de Enmedio (7) | Campoo de Enmedio | 22 |
| Forêt de Polanco (3) | Polanco | 22 |
| Bois de Guriezo | Guriezo | 22 |
| Forêt de Val de San Vicente (2) | Val de San Vicente | 21 |
| Forêt de Bárcena de Pie de Concha | Bárcena de Pie de Concha | 21 |
| Peñas Blancas | Camargo | 21 |
| Forêt de Valdáliga (23) | Valdáliga | 21 |
| Forêt de Valderredible (28) | Valderredible | 21 |
| Forêt de Torrelavega (4) | Torrelavega | 21 |
| Forêt de Cabuérniga (9) | Cabuérniga | 21 |
| Forêt de Vega de Liébana (9) | Vega de Liébana | 21 |
| Forêt de Campoo de Yuso (11) | Campoo de Yuso | 21 |
| Forêt de Vega de Pas (15) | Vega de Pas | 21 |
| Hayedo de Valdició | Soba | 21 |
| Forêt de Torrelavega (6) | Torrelavega | 21 |
| Forêt de Piélagos (32) | Piélagos | 21 |
| Acebal de Abiada | Hermandad de Campoo de Suso | 21 |
| Forêt de Soba (33) | Soba | 21 |
| Forêt de Valderredible (9) | Valderredible | 20 |
| Forêt de Soba (3) | Soba | 20 |
| Forêt de Vega de Liébana (2) | Vega de Liébana | 20 |
| Forêt de Cabezón de Liébana | Cabezón de Liébana | 20 |
| Forêt de Saro | Saro | 20 |
| Forêt de Mazcuerras (5) | Mazcuerras | 20 |
| Forêt de Voto (2) | Voto | 20 |
| Forêt de Campoo de Yuso (6) | Campoo de Yuso | 20 |
| Forêt de Luena (6) | Luena | 20 |
| Forêt de Hermandad de Campoo de Suso (10) | Hermandad de Campoo de Suso | 20 |
| Forêt de Vega de Pas (9) | Vega de Pas | 20 |
| Forêt de Los Corrales de Buelna (6) | Los Corrales de Buelna | 20 |
| Forêt de San Pedro del Romeral (7) | San Pedro del Romeral | 20 |
| Forêt de Ruente (4) | Ruente | 20 |
| Forêt de Valdeprado del Río (16) | Valdeprado del Río | 20 |
| Forêt de Alfoz de Lloredo (5) | Alfoz de Lloredo | 20 |
| Forêt de Valderredible (45) | Valderredible | 20 |
| Forêt de Las Rozas de Valdearroyo (11) | Las Rozas de Valdearroyo | 20 |
| Forêt de Polaciones (43) | Polaciones | 20 |
| Forêt de Valdeolea (4) | Valdeolea | 20 |
| Forêt de Luena (22) | Luena | 20 |
| Forêt de Ampuero (12) | Ampuero | 20 |
| Forêt de Lamasón (31) | Lamasón | 20 |
| Forêt de Anievas (9) | Anievas | 20 |
| Forêt de Puente Viesgo (10) | Puente Viesgo | 20 |
| Forêt de Riotuerto (140) | Riotuerto | 20 |
| Forêt de Luena (36) | Luena | 20 |
| Forêt de Anievas | Anievas | 19 |
| Forêt de Bárcena de Cicero | Bárcena de Cicero | 19 |
| Forêt de Herrerías (9) | Herrerías | 19 |
| Forêt de Cartes (4) | Cartes | 19 |
| Forêt de San Felices de Buelna (4) | San Felices de Buelna | 19 |
| Forêt de Val de San Vicente (8) | Val de San Vicente | 19 |
| Forêt de Ruesga (14) | Ruesga | 19 |
| Forêt de Villacarriedo (5) | Villacarriedo | 19 |
| Forêt de Voto (9) | Voto | 19 |
| Forêt de Ruente (6) | Ruente | 19 |
| Bois de Cieza | Cieza | 19 |
| Forêt de Valdáliga (46) | Valdáliga | 19 |
| Forêt de Meruelo (4) | Meruelo | 19 |
| Forêt de Val de San Vicente (23) | Val de San Vicente | 19 |
| Forêt de Riotuerto (70) | Riotuerto | 19 |
| Forêt de Cartes (11) | Cartes | 19 |
| Forêt de Vega de Pas (25) | Vega de Pas | 19 |
| Forêt de Liérganes (13) | Liérganes | 19 |
| Forêt de Arredondo (13) | Arredondo | 19 |
| Forêt de Castro-Urdiales (85) | Castro-Urdiales | 19 |
| Forêt de Campoo de Yuso | Campoo de Yuso | 18 |
| Forêt de Guriezo (4) | Guriezo | 18 |
| Forêt de Torrelavega | Torrelavega | 18 |
| Forêt de Puente Viesgo (4) | Puente Viesgo | 18 |
| Forêt de Lamasón (10) | Lamasón | 18 |
| Forêt de Polaciones (19) | Polaciones | 18 |
| Forêt de Soba (11) | Soba | 18 |
| Forêt de Valdáliga (30) | Valdáliga | 18 |
| Forêt de Valderredible (36) | Valderredible | 18 |
| Forêt de Miera (2) | Miera | 18 |
| Forêt de San Miguel de Aguayo (3) | San Miguel de Aguayo | 18 |
| Forêt de Lamasón (29) | Lamasón | 18 |
| Forêt de Medio Cudeyo (5) | Medio Cudeyo | 18 |
| Forêt de Lamasón (38) | Lamasón | 18 |
| Forêt de Riotuerto (64) | Riotuerto | 18 |
| Forêt de Piélagos (28) | Piélagos | 18 |
| Forêt de El Astillero (2) | El Astillero | 18 |
| Forêt de Campoo de Yuso (4) | Campoo de Yuso | 17 |
| Forêt de Reocín (3) | Reocín | 17 |
| Forêt de Bárcena de Cicero (2) | Bárcena de Cicero | 17 |
| Forêt de Mazcuerras (11) | Mazcuerras | 17 |
| Forêt de Alfoz de Lloredo (2) | Alfoz de Lloredo | 17 |
| Forêt de Valdáliga (32) | Valdáliga | 17 |
| Forêt de Peñarrubia (4) | Peñarrubia | 17 |
| Forêt de Mazcuerras (18) | Mazcuerras | 17 |
| Forêt de Camargo (2) | Camargo | 17 |
| Forêt de Cabezón de Liébana (4) | Cabezón de Liébana | 17 |
| Forêt de Cillorigo de Liébana (15) | Cillorigo de Liébana | 17 |
| Forêt de Campoo de Yuso (13) | Campoo de Yuso | 17 |
| Forêt de Anievas (8) | Anievas | 17 |
| Forêt de Valdáliga (45) | Valdáliga | 17 |
| Forêt de Luena (21) | Luena | 17 |
| Forêt de Santillana del Mar (4) | Santillana del Mar | 17 |
| Forêt de Ruiloba (2) | Ruiloba | 17 |
| Forêt de Reocín (18) | Reocín | 17 |
| Forêt de Castro-Urdiales (48) | Castro-Urdiales | 17 |
| Forêt de San Vicente de la Barquera (10) | San Vicente de la Barquera | 17 |
| Forêt de Miera (8) | Miera | 17 |
| Bois de Castro-Urdiales (103) | Castro-Urdiales | 17 |
| Bois de Valderredible (8) | Valderredible | 17 |
| Forêt de Valderredible (10) | Valderredible | 16 |
| Forêt de San Roque de Riomiera | San Roque de Riomiera | 16 |
| Forêt de Hermandad de Campoo de Suso (5) | Hermandad de Campoo de Suso | 16 |
| Forêt de Valdeolea | Valdeolea | 16 |
| Forêt de Corvera de Toranzo (2) | Corvera de Toranzo | 16 |
| Forêt de Ruesga (6) | Ruesga | 16 |
| Forêt de Villacarriedo | Villacarriedo | 16 |
| Forêt de Campoo de Yuso (7) | Campoo de Yuso | 16 |
| Forêt de Piélagos (3) | Piélagos | 16 |
| Forêt de Villacarriedo (3) | Villacarriedo | 16 |
| Forêt de Escalante (2) | Escalante | 16 |
| Forêt de Ruesga (11) | Ruesga | 16 |
| Forêt de Las Rozas de Valdearroyo (6) | Las Rozas de Valdearroyo | 16 |
| Forêt de Polaciones (27) | Polaciones | 16 |
| Forêt de Guriezo (15) | Guriezo | 16 |
| Forêt de Bárcena de Pie de Concha (3) | Bárcena de Pie de Concha | 16 |
| Forêt de Herrerías (24) | Herrerías | 16 |
| Forêt de San Vicente de la Barquera (5) | San Vicente de la Barquera | 16 |
| Forêt de Castro-Urdiales (6) | Castro-Urdiales | 16 |
| Forêt de Piélagos (8) | Piélagos | 16 |
| Forêt de Arenas de Iguña (11) | Arenas de Iguña | 16 |
| Forêt de Val de San Vicente (17) | Val de San Vicente | 16 |
| Forêt de Medio Cudeyo (21) | Medio Cudeyo | 16 |
| Forêt de Puente Viesgo (16) | Puente Viesgo | 16 |
| Forêt de Solórzano (13) | Solórzano | 16 |
| Forêt de Guriezo (25) | Guriezo | 16 |
| Forêt de Guriezo (29) | Guriezo | 16 |
| Forêt de Castro-Urdiales (97) | Castro-Urdiales | 16 |
| Parque de La Magdalena | Santander | 15 |
| Forêt de Hermandad de Campoo de Suso (4) | Hermandad de Campoo de Suso | 15 |
| Forêt de San Felices de Buelna (3) | San Felices de Buelna | 15 |
| Forêt de Medio Cudeyo (2) | Medio Cudeyo | 15 |
| Forêt de Castro-Urdiales (4) | Castro-Urdiales | 15 |
| Forêt de Santiurde de Reinosa | Santiurde de Reinosa | 15 |
| Forêt de Hermandad de Campoo de Suso (13) | Hermandad de Campoo de Suso | 15 |
| Forêt de Los Corrales de Buelna (5) | Los Corrales de Buelna | 15 |
| Forêt de Molledo (10) | Molledo | 15 |
| Forêt de Polaciones (28) | Polaciones | 15 |
| Forêt de Cieza (5) | Cieza | 15 |
| Forêt de Ribamontán al Mar (2) | Ribamontán al Mar | 15 |
| Forêt de Hazas de Cesto (4) | Hazas de Cesto | 15 |
| Forêt de Lamasón (23) | Lamasón | 15 |
| Forêt de Potes | Potes | 15 |
| Forêt de Riotuerto | Riotuerto | 15 |
| Forêt de Cabuérniga (19) | Cabuérniga | 15 |
| Forêt de Rionansa (42) | Rionansa | 15 |
| Forêt de Ruente (8) | Ruente | 15 |
| Forêt de Villaescusa (6) | Villaescusa | 15 |
| Forêt de Arredondo (9) | Arredondo | 15 |
| Bois de Castro-Urdiales (62) | Castro-Urdiales | 15 |
| Forêt de Reocín (24) | Reocín | 15 |
| Forêt de Ruesga (29) | Ruesga | 15 |
| Forêt de Guriezo (26) | Guriezo | 15 |
| Forêt de Valle de Villaverde (39) | Valle de Villaverde | 15 |
| Bois de Camaleño (19) | Camaleño | 15 |
| Forêt de San Felices de Buelna | San Felices de Buelna | 14 |
| Forêt de Cieza (3) | Cieza | 14 |
| Forêt de Santiurde de Toranzo (3) | Santiurde de Toranzo | 14 |
| Forêt de Udías | Udías | 14 |
| Forêt de Arenas de Iguña (5) | Arenas de Iguña | 14 |
| Forêt de Los Tojos (6) | Los Tojos | 14 |
| Forêt de Miera | Miera | 14 |
| Forêt de Las Rozas de Valdearroyo (10) | Las Rozas de Valdearroyo | 14 |
| Forêt de Santillana del Mar (3) | Santillana del Mar | 14 |
| Forêt de Vega de Liébana (7) | Vega de Liébana | 14 |
| Forêt de Hazas de Cesto (3) | Hazas de Cesto | 14 |
| Forêt de Hermandad de Campoo de Suso (16) | Hermandad de Campoo de Suso | 14 |
| Forêt de Luena (15) | Luena | 14 |
| Forêt de Camaleño (3) | Camaleño | 14 |
| Forêt de Mazcuerras (19) | Mazcuerras | 14 |
| Forêt de Cillorigo de Liébana (18) | Cillorigo de Liébana | 14 |
| Forêt de San Felices de Buelna (10) | San Felices de Buelna | 14 |
| Forêt de Cabuérniga (21) | Cabuérniga | 14 |
| Forêt de Vega de Pas (20) | Vega de Pas | 14 |
| Forêt de Vega de Pas (21) | Vega de Pas | 14 |
| Forêt de Voto (13) | Voto | 14 |
| Forêt de Piélagos (15) | Piélagos | 14 |
| Forêt de Hazas de Cesto (8) | Hazas de Cesto | 14 |
| Forêt de Guriezo (35) | Guriezo | 14 |
| Bois de Cabezón de la Sal | Cabezón de la Sal | 14 |
| Forêt de Reocín (25) | Reocín | 14 |
| Bois de Castañeda (105) | Castañeda | 14 |
| Forêt de Solórzano | Solórzano | 13 |
| Bois de Valdeolea | Valdeolea | 13 |
| Forêt de Cabezón de la Sal (5) | Cabezón de la Sal | 13 |
| Forêt de Santillana del Mar | Santillana del Mar | 13 |
| Forêt de Hermandad de Campoo de Suso (6) | Hermandad de Campoo de Suso | 13 |
| Forêt de Ruesga (4) | Ruesga | 13 |
| Forêt de Valderredible (19) | Valderredible | 13 |
| Forêt de Santiurde de Toranzo (4) | Santiurde de Toranzo | 13 |
| Forêt de San Pedro del Romeral (4) | San Pedro del Romeral | 13 |
| Forêt de Cieza (4) | Cieza | 13 |
| Forêt de San Pedro del Romeral (6) | San Pedro del Romeral | 13 |
| Forêt de Los Tojos (10) | Los Tojos | 13 |
| Forêt de Los Tojos (11) | Los Tojos | 13 |
| Forêt de Entrambasaguas (13) | Entrambasaguas | 13 |
| Forêt de Ruesga (18) | Ruesga | 13 |
| Forêt de Campoo de Enmedio (4) | Campoo de Enmedio | 13 |
| Forêt de Los Tojos (17) | Los Tojos | 13 |
| Forêt de Bárcena de Cicero (4) | Bárcena de Cicero | 13 |
| Forêt de Marina de Cudeyo (2) | Marina de Cudeyo | 13 |
| Forêt de Riotuerto (30) | Riotuerto | 13 |
| Forêt de Torrelavega (13) | Torrelavega | 13 |
| Forêt de Cartes (13) | Cartes | 13 |
| Forêt de Hazas de Cesto (9) | Hazas de Cesto | 13 |
| Forêt de Valdeolea (6) | Valdeolea | 13 |
| Forêt de Guriezo (32) | Guriezo | 13 |
| Forêt de Santiurde de Reinosa (8) | Santiurde de Reinosa | 13 |
| Forêt de Luena (34) | Luena | 13 |
| Forêt de Valdeolea (7) | Valdeolea | 13 |
| Forêt de Cillorigo de Liébana (20) | Cillorigo de Liébana | 13 |
| Forêt de Castro-Urdiales (92) | Castro-Urdiales | 13 |
| Bois de Liérganes (64) | Liérganes | 13 |
| Forêt de Valdeolea (11) | Valdeolea | 13 |
| Forêt de Medio Cudeyo (28) | Medio Cudeyo | 13 |
| Forêt de Val de San Vicente (45) | Val de San Vicente | 13 |
| Bois de Soba (14) | Soba | 13 |
| Bois de Valderredible (11) | Valderredible | 13 |
| Forêt de Valdeprado del Río (2) | Valdeprado del Río | 12 |
| Forêt de Camaleño | Camaleño | 12 |
| Forêt de Puente Viesgo (2) | Puente Viesgo | 12 |
| Forêt de Valdáliga (17) | Valdáliga | 12 |
| Forêt de Valdáliga (18) | Valdáliga | 12 |
| Forêt de Alfoz de Lloredo | Alfoz de Lloredo | 12 |
| Forêt de Anievas (3) | Anievas | 12 |
| Forêt de Torrelavega (3) | Torrelavega | 12 |
| Forêt de Lamasón (18) | Lamasón | 12 |
| Forêt de Arredondo (6) | Arredondo | 12 |
| Forêt de Puente Viesgo (6) | Puente Viesgo | 12 |
| Forêt de Campoo de Yuso (10) | Campoo de Yuso | 12 |
| Forêt de Ruente (5) | Ruente | 12 |
| Forêt de Valderredible (51) | Valderredible | 12 |
| Forêt de Udías (3) | Udías | 12 |
| Forêt de Santiurde de Toranzo (9) | Santiurde de Toranzo | 12 |
| Forêt de Piélagos (10) | Piélagos | 12 |
| Forêt de Riotuerto (7) | Riotuerto | 12 |
| Forêt de Riotuerto (9) | Riotuerto | 12 |
| Forêt de Riotuerto (48) | Riotuerto | 12 |
| Forêt de Camargo (3) | Camargo | 12 |
| Forêt de Polanco (5) | Polanco | 12 |
| Bois de Campoo de Yuso (3) | Campoo de Yuso | 12 |
| Forêt de Laredo (2) | Laredo | 12 |
| Forêt de San Roque de Riomiera (12) | San Roque de Riomiera | 12 |
| Forêt de Riotuerto (157) | Riotuerto | 12 |
| Forêt de Riotuerto (160) | Riotuerto | 12 |
| Bois de Valderredible (29) | Valderredible | 12 |
| Forêt de San Miguel de Aguayo | San Miguel de Aguayo | 11 |
| Forêt de Valdeolea (2) | Valdeolea | 11 |
| Forêt de San Vicente de la Barquera (2) | San Vicente de la Barquera | 11 |
| Forêt de Camaleño (2) | Camaleño | 11 |
| Forêt de Cabezón de la Sal (13) | Cabezón de la Sal | 11 |
| Forêt de Polaciones (31) | Polaciones | 11 |
| Forêt de Campoo de Yuso (9) | Campoo de Yuso | 11 |
| Forêt de Anievas (5) | Anievas | 11 |
| Forêt de Vega de Pas (14) | Vega de Pas | 11 |
| Forêt de Rionansa (39) | Rionansa | 11 |
| Forêt de Rionansa (44) | Rionansa | 11 |
| Bois de Saro | Saro | 11 |
| Bois de Castro-Urdiales (75) | Castro-Urdiales | 11 |
| Forêt de Guriezo (36) | Guriezo | 11 |
| Forêt de Guriezo (38) | Guriezo | 11 |
| Parque de la vaguada de Las Llamas | Santander | 11 |
| Forêt de Valdeolea (8) | Valdeolea | 11 |
| Forêt de Selaya (10) | Selaya | 11 |
| Forêt de Valdeolea (10) | Valdeolea | 11 |
| Forêt de Campoo de Yuso (18) | Campoo de Yuso | 11 |
| Bois de Valderredible (14) | Valderredible | 11 |
| Forêt de Soba (82) | Soba | 11 |
| Forêt de Hazas de Cesto | Hazas de Cesto | 10 |
| Forêt de Puente Viesgo (3) | Puente Viesgo | 10 |
| Forêt de San Felices de Buelna (8) | San Felices de Buelna | 10 |
| Forêt de Ruiloba | Ruiloba | 10 |
| Forêt de Rasines (8) | Rasines | 10 |
| Forêt de Villaescusa (7) | Villaescusa | 10 |
| Bois de Campoo de Yuso (2) | Campoo de Yuso | 10 |
| Forêt de San Miguel de Aguayo (14) | San Miguel de Aguayo | 10 |
| Forêt de Alfoz de Lloredo (12) | Reocín | 10 |
| Forêt de Val de San Vicente (26) | Val de San Vicente | 10 |
| Forêt de Medio Cudeyo (24) | Medio Cudeyo | 10 |
| Forêt de Rionansa (54) | Rionansa | 10 |
| Forêt de Soba (71) | Soba | 10 |
| Forêt de Valderredible (66) | Valderredible | 10 |
| Parque de La Remonta ⚠️ | Santander | 9 |
| Forêt de Vega de Pas ⚠️ | Vega de Pas | 9 |
| Forêt de San Roque de Riomiera (2) ⚠️ | San Roque de Riomiera | 9 |
| Forêt de San Vicente de la Barquera (4) ⚠️ | San Vicente de la Barquera | 9 |
| Pinar de Arna ⚠️ | Ribamontán al Mar | 9 |
| Bois de Herrerías (2) ⚠️ | Herrerías | 9 |
| Forêt de Tudanca (26) ⚠️ | Tudanca | 9 |
| Forêt de Polaciones (49) ⚠️ | Polaciones | 9 |
| Forêt de Polaciones (50) ⚠️ | Polaciones | 9 |
| Bois de Saro (2) ⚠️ | Saro | 9 |
| Bois de Santa María de Cayón (3) ⚠️ | Santa María de Cayón | 9 |
| Forêt de San Roque de Riomiera (8) ⚠️ | San Roque de Riomiera | 9 |
| Forêt de Escalante (4) ⚠️ | Escalante | 9 |
| Forêt de Camargo (6) ⚠️ | Camargo | 9 |
| Forêt de Soba (38) ⚠️ | Soba | 9 |
| Forêt de Soba (47) ⚠️ | Soba | 9 |
| Forêt de Valle de Villaverde (23) ⚠️ | Valle de Villaverde | 9 |
| Forêt de Castro-Urdiales (84) ⚠️ | Castro-Urdiales | 9 |
| Forêt de Valle de Villaverde (36) ⚠️ | Valle de Villaverde | 9 |
| Bois de Valdeolea (3) ⚠️ | Valdeolea | 9 |
| Bois de Camargo (8) ⚠️ | Camargo | 9 |
| Bois de Vega de Pas (4) ⚠️ | Vega de Pas | 9 |
| Bois de Camaleño (25) ⚠️ | Camaleño | 9 |
| Bois de Valderredible (20) ⚠️ | Valderredible | 9 |
| Parque de la Viesca ⚠️ | Torrelavega | 8 |
| Forêt de Rionansa (3) ⚠️ | Rionansa | 8 |
| Bois de Herrerías ⚠️ | Herrerías | 8 |
| Bois de San Roque de Riomiera ⚠️ | San Roque de Riomiera | 8 |
| Forêt de Liérganes ⚠️ | Liérganes | 8 |
| Forêt de Rionansa (31) ⚠️ | Rionansa | 8 |
| Forêt de Herrerías (34) ⚠️ | Herrerías | 8 |
| Forêt de Riotuerto (11) ⚠️ | Riotuerto | 8 |
| Forêt de Riotuerto (41) ⚠️ | Riotuerto | 8 |
| Forêt de Riotuerto (82) ⚠️ | Riotuerto | 8 |
| Forêt de Piélagos (20) ⚠️ | Piélagos | 8 |
| Forêt de Val de San Vicente (27) ⚠️ | Val de San Vicente | 8 |
| Forêt de Arnuero (3) ⚠️ | Arnuero | 8 |
| Forêt de Polanco (13) ⚠️ | Polanco | 8 |
| Forêt de Valdáliga (54) ⚠️ | Valdáliga | 8 |
| Forêt de Corvera de Toranzo (14) ⚠️ | Corvera de Toranzo | 8 |
| Forêt de Soba (35) ⚠️ | Soba | 8 |
| Forêt de Guriezo (27) ⚠️ | Guriezo | 8 |
| Forêt de Santiurde de Reinosa (6) ⚠️ | Santiurde de Reinosa | 8 |
| Forêt de Camaleño (12) ⚠️ | Camaleño | 8 |
| Forêt de Soba (68) ⚠️ | Soba | 8 |
| Forêt de Villaescusa (25) ⚠️ | Villaescusa | 8 |
| Forêt de Valdáliga (58) ⚠️ | Valdáliga | 8 |
| Forêt de Soba (70) ⚠️ | Soba | 8 |
| Finca del Marqués de Valdecilla ⚠️ | Medio Cudeyo | 7 |
| Forêt de Cabezón de la Sal ⚠️ | Cabezón de la Sal | 7 |
| Forêt de Cabezón de la Sal (7) ⚠️ | Cabezón de la Sal | 7 |
| Forêt de Ribamontán al Monte ⚠️ | Ribamontán al Monte | 7 |
| Forêt de Pesaguero (2) ⚠️ | Pesaguero | 7 |
| Forêt de Escalante (3) ⚠️ | Escalante | 7 |
| Forêt de Mazcuerras (13) ⚠️ | Mazcuerras | 7 |
| Forêt de Marina de Cudeyo ⚠️ | Marina de Cudeyo | 7 |
| Forêt de Soba (19) ⚠️ | Soba | 7 |
| Forêt de Villacarriedo (6) ⚠️ | Villacarriedo | 7 |
| Forêt de Luena (13) ⚠️ | Luena | 7 |
| Forêt de Reocín (5) ⚠️ | Reocín | 7 |
| Forêt de Campoo de Yuso (12) ⚠️ | Campoo de Yuso | 7 |
| Forêt de Valderredible (53) ⚠️ | Valderredible | 7 |
| Forêt de Rionansa (50) ⚠️ | Rionansa | 7 |
| Forêt de Torrelavega (16) ⚠️ | Torrelavega | 7 |
| Forêt de Piélagos (26) ⚠️ | Piélagos | 7 |
| Forêt de Piélagos (27) ⚠️ | Piélagos | 7 |
| Bois de Campoo de Yuso ⚠️ | Campoo de Yuso | 7 |
| Bois de Puente Viesgo (2) ⚠️ | Puente Viesgo | 7 |
| Bois de Castro-Urdiales ⚠️ | Castro-Urdiales | 7 |
| Forêt de Val de San Vicente (37) ⚠️ | Val de San Vicente | 7 |
| Forêt de Castro-Urdiales (69) ⚠️ | Castro-Urdiales | 7 |
| Forêt de Valle de Villaverde (24) ⚠️ | Valle de Villaverde | 7 |
| Bois de Saro (17) ⚠️ | Saro | 7 |
| Forêt de San Roque de Riomiera (11) ⚠️ | San Roque de Riomiera | 7 |
| Bois de Vega de Pas (3) ⚠️ | Vega de Pas | 7 |
| Forêt de Riotuerto (161) ⚠️ | Riotuerto | 7 |
| Forêt de Liérganes (33) ⚠️ | Liérganes | 7 |
| Forêt de Puente Viesgo (23) ⚠️ | Puente Viesgo | 7 |
| Bois de Valderredible (7) ⚠️ | Valderredible | 7 |
| Bois de Las Rozas de Valdearroyo (7) ⚠️ | Las Rozas de Valdearroyo | 7 |
| Bois de Soba (18) ⚠️ | Soba | 7 |
| Forêt de Cabezón de la Sal (2) ⚠️ | Cabezón de la Sal | 6 |
| Forêt de Rionansa ⚠️ | Rionansa | 6 |
| Forêt de Villacarriedo (2) ⚠️ | Villacarriedo | 6 |
| Forêt de Rionansa (19) ⚠️ | Rionansa | 6 |
| Forêt de Polaciones (22) ⚠️ | Polaciones | 6 |
| Forêt de Peñarrubia (5) ⚠️ | Peñarrubia | 6 |
| Forêt de Mazcuerras (14) ⚠️ | Mazcuerras | 6 |
| Forêt de Riotuerto (5) ⚠️ | Riotuerto | 6 |
| Forêt de Riotuerto (51) ⚠️ | Riotuerto | 6 |
| Forêt de Riotuerto (68) ⚠️ | Riotuerto | 6 |
| Forêt de Entrambasaguas (43) ⚠️ | Entrambasaguas | 6 |
| Forêt de Torrelavega (21) ⚠️ | Torrelavega | 6 |
| Bois de Santillana del Mar (3) ⚠️ | Santillana del Mar | 6 |
| Forêt de Puente Viesgo (12) ⚠️ | Puente Viesgo | 6 |
| Forêt de Puente Viesgo (15) ⚠️ | Puente Viesgo | 6 |
| Forêt de Solórzano (8) ⚠️ | Solórzano | 6 |
| Forêt de Solórzano (11) ⚠️ | Solórzano | 6 |
| Forêt de Campoo de Enmedio (8) ⚠️ | Campoo de Enmedio | 6 |
| Bosque de Valverde ⚠️ | Castro-Urdiales | 6 |
| El Encinar ⚠️ | Castro-Urdiales | 6 |
| Forêt de Castro-Urdiales (66) ⚠️ | Castro-Urdiales | 6 |
| Forêt de San Felices de Buelna (14) ⚠️ | San Felices de Buelna | 6 |
| Bois de Ramales de la Victoria (10) ⚠️ | Ramales de la Victoria | 6 |
| Forêt de Castro-Urdiales (83) ⚠️ | Castro-Urdiales | 6 |
| Forêt de San Roque de Riomiera (10) ⚠️ | San Roque de Riomiera | 6 |
| Bois de Vega de Pas (2) ⚠️ | Vega de Pas | 6 |
| Forêt de Vega de Pas (37) ⚠️ | Vega de Pas | 6 |
| Forêt de Vega de Pas (39) ⚠️ | Vega de Pas | 6 |
| Forêt de Riotuerto (155) ⚠️ | Riotuerto | 6 |
| Parc de Santillana del Mar (2) ⚠️ | Santillana del Mar | 6 |
| Forêt de Selaya (11) ⚠️ | Selaya | 6 |
| Forêt de Riotuerto (158) ⚠️ | Riotuerto | 6 |
| Forêt de Riotuerto (159) ⚠️ | Riotuerto | 6 |
| Parc de Santoña (6) ⚠️ | Santoña | 6 |
| Forêt de Riotuerto (162) ⚠️ | Riotuerto | 6 |
| Bois de Puente Viesgo (22) ⚠️ | Puente Viesgo | 6 |
| Bois de Valderredible (19) ⚠️ | Valderredible | 6 |
| Bois de Valderredible (27) ⚠️ | Valderredible | 6 |
| Forêt de Herrerías (3) ⚠️ | Herrerías | 5 |
| Forêt de Herrerías (10) ⚠️ | Herrerías | 5 |
| Forêt de Lamasón (21) ⚠️ | Lamasón | 5 |
| Forêt de San Felices de Buelna (9) ⚠️ | San Felices de Buelna | 5 |
| Forêt de Riotuerto (3) ⚠️ | Riotuerto | 5 |
| Forêt de Riotuerto (20) ⚠️ | Riotuerto | 5 |
| Bois de Camargo ⚠️ | Camargo | 5 |
| Forêt de Entrambasaguas (41) ⚠️ | Entrambasaguas | 5 |
| Forêt de Torrelavega (12) ⚠️ | Torrelavega | 5 |
| Forêt de Cartes (12) ⚠️ | Cartes | 5 |
| Forêt de Piélagos (23) ⚠️ | Piélagos | 5 |
| Forêt de Hazas de Cesto (7) ⚠️ | Hazas de Cesto | 5 |
| Forêt de Solórzano (9) ⚠️ | Solórzano | 5 |
| Forêt de Piélagos (29) ⚠️ | Piélagos | 5 |
| Forêt de Ribamontán al Monte (4) ⚠️ | Ribamontán al Monte | 5 |
| Forêt de San Miguel de Aguayo (10) ⚠️ | San Miguel de Aguayo | 5 |
| Forêt de Santiurde de Toranzo (11) ⚠️ | Santiurde de Toranzo | 5 |
| Forêt de Arnuero (2) ⚠️ | Arnuero | 5 |
| Parque del Doctor Morales ⚠️ | Santander | 5 |
| Forêt de Castro-Urdiales (50) ⚠️ | Castro-Urdiales | 5 |
| Forêt de Valdáliga (56) ⚠️ | Valdáliga | 5 |
| Forêt de Torrelavega (34) ⚠️ | Torrelavega | 5 |
| Forêt de Villaescusa (23) ⚠️ | Villaescusa | 5 |
| Forêt de San Vicente de la Barquera (15) ⚠️ | San Vicente de la Barquera | 5 |
| Parque de La Planchada ⚠️ | El Astillero | 5 |
| Bois de Riotuerto (14) ⚠️ | Riotuerto | 5 |
| Forêt de Soba (48) ⚠️ | Soba | 5 |
| Forêt de Guriezo (34) ⚠️ | Guriezo | 5 |
| Forêt de Castro-Urdiales (72) ⚠️ | Castro-Urdiales | 5 |
| Bois de Valle de Villaverde (3) ⚠️ | Valle de Villaverde | 5 |
| Forêt de Castro-Urdiales (79) ⚠️ | Castro-Urdiales | 5 |
| Forêt de Valle de Villaverde (34) ⚠️ | Valle de Villaverde | 5 |
| Forêt de Castro-Urdiales (89) ⚠️ | Castro-Urdiales | 5 |
| Forêt de Villacarriedo (13) ⚠️ | Villacarriedo | 5 |
| Bois de Valdeolea (5) ⚠️ | Valdeolea | 5 |
| Forêt de Los Tojos (22) ⚠️ | Los Tojos | 5 |
| Castañar de El Habario ⚠️ | Cillorigo de Liébana | 5 |
| Bois de Santillana del Mar (4) ⚠️ | Santillana del Mar | 5 |
| Forêt de Molledo (19) ⚠️ | Molledo | 5 |
| Forêt de Ribamontán al Monte (6) ⚠️ | Ribamontán al Monte | 5 |
| Forêt de Molledo (20) ⚠️ | Molledo | 5 |
| Bois de Marina de Cudeyo (11) ⚠️ | Marina de Cudeyo | 5 |
| Bois de Arredondo (3) ⚠️ | Arredondo | 5 |
| Forêt de Miera (7) ⚠️ | Miera | 5 |
| Bois de Liérganes (65) ⚠️ | Liérganes | 5 |
| Forêt de Cartes (27) ⚠️ | Reocín | 5 |
| Forêt de Ramales de la Victoria (10) ⚠️ | Ramales de la Victoria | 5 |
| Forêt de Valderredible (68) ⚠️ | Valderredible | 5 |
| Bois de Las Rozas de Valdearroyo (4) ⚠️ | Las Rozas de Valdearroyo | 5 |
| Bois de Ramales de la Victoria (18) ⚠️ | Ramales de la Victoria | 5 |
| Forêt de Valderredible (3) ⚠️ | Valderredible | 4 |
| Forêt de Polaciones (4) ⚠️ | Polaciones | 4 |
| Forêt de Guriezo (8) ⚠️ | Guriezo | 4 |
| Forêt de Medio Cudeyo (3) ⚠️ | Medio Cudeyo | 4 |
| Forêt de Herrerías (16) ⚠️ | Herrerías | 4 |
| Forêt de Polaciones (24) ⚠️ | Polaciones | 4 |
| Forêt de Valderredible (39) ⚠️ | Valderredible | 4 |
| Forêt de Arredondo (7) ⚠️ | Arredondo | 4 |
| Forêt de Rionansa (49) ⚠️ | Rionansa | 4 |
| Forêt de Tudanca (28) ⚠️ | Tudanca | 4 |
| Forêt de Polaciones (52) ⚠️ | Polaciones | 4 |
| Forêt de Medio Cudeyo (7) ⚠️ | Medio Cudeyo | 4 |
| Parque de Mataleñas ⚠️ | Santander | 4 |
| Forêt de Liérganes (2) ⚠️ | Liérganes | 4 |
| Bois de Liérganes (3) ⚠️ | Liérganes | 4 |
| Forêt de Riotuerto (35) ⚠️ | Riotuerto | 4 |
| Forêt de Riotuerto (42) ⚠️ | Riotuerto | 4 |
| Forêt de Entrambasaguas (45) ⚠️ | Entrambasaguas | 4 |
| Bois de Piélagos ⚠️ | Piélagos | 4 |
| Parque de Las Tablas ⚠️ | Torrelavega | 4 |
| Forêt de Polanco (4) ⚠️ | Polanco | 4 |
| Forêt de Piélagos (14) ⚠️ | Piélagos | 4 |
| Forêt de Suances ⚠️ | Suances | 4 |
| Forêt de Reocín (15) ⚠️ | Reocín | 4 |
| Forêt de Villacarriedo (8) ⚠️ | Villacarriedo | 4 |
| Forêt de Solórzano (7) ⚠️ | Solórzano | 4 |
| Forêt de Polanco (9) ⚠️ | Polanco | 4 |
| Forêt de Cartes (16) ⚠️ | Cartes | 4 |
| Forêt de Piélagos (30) ⚠️ | Piélagos | 4 |
| Bois de Reocín (7) ⚠️ | Reocín | 4 |
| Forêt de Piélagos (37) ⚠️ | Piélagos | 4 |
| Forêt de Cartes (24) ⚠️ | Cartes | 4 |
| Bois de Alfoz de Lloredo (3) ⚠️ | Alfoz de Lloredo | 4 |
| Forêt de Santa María de Cayón (5) ⚠️ | Santa María de Cayón | 4 |
| Bois de Bárcena de Cicero ⚠️ | Bárcena de Cicero | 4 |
| Parque de la Antigua Marisma de Cacho ⚠️ | Camargo | 4 |
| Forêt de Campoo de Yuso (17) ⚠️ | Campoo de Yuso | 4 |
| Forêt de Los Corrales de Buelna (13) ⚠️ | Los Corrales de Buelna | 4 |
| Bois de Medio Cudeyo (14) ⚠️ | Medio Cudeyo | 4 |
| Forêt de Villafufre (3) ⚠️ | Villafufre | 4 |
| Forêt de Santa María de Cayón (34) ⚠️ | Santa María de Cayón | 4 |
| Parque de Rafael de la Sierra ⚠️ | Cartes | 4 |
| Forêt de Santa María de Cayón (56) ⚠️ | Santa María de Cayón | 4 |
| Bois de Ramales de la Victoria (2) ⚠️ | Ramales de la Victoria | 4 |
| Forêt de Soba (39) ⚠️ | Soba | 4 |
| Forêt de Ramales de la Victoria (6) ⚠️ | Ramales de la Victoria | 4 |
| Forêt de Guriezo (28) ⚠️ | Guriezo | 4 |
| Forêt de Guriezo (30) ⚠️ | Guriezo | 4 |
| Forêt de Castro-Urdiales (77) ⚠️ | Castro-Urdiales | 4 |
| Forêt de Castro-Urdiales (81) ⚠️ | Castro-Urdiales | 4 |
| Forêt de Castro-Urdiales (82) ⚠️ | Castro-Urdiales | 4 |
| Forêt de Guriezo (39) ⚠️ | Guriezo | 4 |
| Forêt de Ramales de la Victoria (9) ⚠️ | Ramales de la Victoria | 4 |
| Bois de Pesaguero (2) ⚠️ | Pesaguero | 4 |
| Forêt de Luena (35) ⚠️ | Luena | 4 |
| Forêt de Santiurde de Reinosa (9) ⚠️ | Santiurde de Reinosa | 4 |
| Carandía ⚠️ | San Pedro del Romeral | 4 |
| Forêt de Liendo (3) ⚠️ | Liendo | 4 |
| Bois de Valdeolea (2) ⚠️ | Valdeolea | 4 |
| Forêt de Entrambasaguas (58) ⚠️ | Entrambasaguas | 4 |
| Forêt de Bárcena de Pie de Concha (5) ⚠️ | Bárcena de Pie de Concha | 4 |
| Bois de Alfoz de Lloredo (9) ⚠️ | Alfoz de Lloredo | 4 |
| Bois de San Roque de Riomiera (6) ⚠️ | San Roque de Riomiera | 4 |
| Forêt de Entrambasaguas (59) ⚠️ | Entrambasaguas | 4 |
| Forêt de Riotuerto (152) ⚠️ | Riotuerto | 4 |
| Forêt de Vega de Pas (40) ⚠️ | Vega de Pas | 4 |
| Forêt de Cartes (25) ⚠️ | Cartes | 4 |
| Forêt de Castro-Urdiales (95) ⚠️ | Castro-Urdiales | 4 |
| Bois de Soba (12) ⚠️ | Soba | 4 |
| Forêt de Lamasón (4) ⚠️ | Lamasón | 3 |
| Forêt de Reocín ⚠️ | Reocín | 3 |
| Forêt de Rionansa (9) ⚠️ | Rionansa | 3 |
| Forêt de Rionansa (10) ⚠️ | Rionansa | 3 |
| Forêt de Tudanca (5) ⚠️ | Tudanca | 3 |
| Forêt de Corvera de Toranzo (4) ⚠️ | Corvera de Toranzo | 3 |
| Forêt de Cabuérniga (10) ⚠️ | Cabuérniga | 3 |
| Forêt de Lamasón (19) ⚠️ | Lamasón | 3 |
| Forêt de Tresviso (2) ⚠️ | Tresviso | 3 |
| Forêt de Val de San Vicente (12) ⚠️ | Val de San Vicente | 3 |
| Forêt de Valderredible (44) ⚠️ | Valderredible | 3 |
| Forêt de Alfoz de Lloredo (6) ⚠️ | Alfoz de Lloredo | 3 |
| Forêt de Rionansa (40) ⚠️ | Rionansa | 3 |
| Forêt de Riotuerto (6) ⚠️ | Riotuerto | 3 |
| Forêt de Riotuerto (13) ⚠️ | Riotuerto | 3 |
| Forêt de Riotuerto (18) ⚠️ | Riotuerto | 3 |
| Forêt de Bárcena de Cicero (6) ⚠️ | Bárcena de Cicero | 3 |
| Forêt de Riotuerto (65) ⚠️ | Riotuerto | 3 |
| Forêt de Entrambasaguas (35) ⚠️ | Entrambasaguas | 3 |
| Forêt de Riotuerto (95) ⚠️ | Riotuerto | 3 |
| Forêt de Medio Cudeyo (19) ⚠️ | Medio Cudeyo | 3 |
| Bois de Entrambasaguas (6) ⚠️ | Entrambasaguas | 3 |
| Forêt de Riotuerto (125) ⚠️ | Riotuerto | 3 |
| Parc de Torrelavega ⚠️ | Torrelavega | 3 |
| Parc de Santander (8) ⚠️ | Santander | 3 |
| Forêt de Villaescusa (12) ⚠️ | Villaescusa | 3 |
| Bois de Torrelavega ⚠️ | Torrelavega | 3 |
| Forêt de Torrelavega (14) ⚠️ | Torrelavega | 3 |
| Forêt de Reocín (9) ⚠️ | Reocín | 3 |
| Forêt de Cartes (14) ⚠️ | Cartes | 3 |
| Bois de Reocín (3) ⚠️ | Reocín | 3 |
| Bois de Reocín (4) ⚠️ | Reocín | 3 |
| Forêt de Piélagos (24) ⚠️ | Piélagos | 3 |
| Forêt de Miengo (2) ⚠️ | Miengo | 3 |
| Forêt de Camaleño (5) ⚠️ | Camaleño | 3 |
| Forêt de Alfoz de Lloredo (9) ⚠️ | Alfoz de Lloredo | 3 |
| Bois de Comillas (2) ⚠️ | Comillas | 3 |
| Forêt de Reocín (16) ⚠️ | Reocín | 3 |
| Forêt de Piélagos (33) ⚠️ | Piélagos | 3 |
| Forêt de Vega de Pas (24) ⚠️ | Vega de Pas | 3 |
| Forêt de Hermandad de Campoo de Suso (19) ⚠️ | Hermandad de Campoo de Suso | 3 |
| Bois de Alfoz de Lloredo (2) ⚠️ | Alfoz de Lloredo | 3 |
| Forêt de Udías (4) ⚠️ | Udías | 3 |
| El Pinar ⚠️ | Noja | 3 |
| Forêt de Luena (27) ⚠️ | Luena | 3 |
| Forêt de Castro-Urdiales (60) ⚠️ | Castro-Urdiales | 3 |
| Forêt de Castro-Urdiales (61) ⚠️ | Castro-Urdiales | 3 |
| Bois de Camaleño (7) ⚠️ | Camaleño | 3 |
| Forêt de Corvera de Toranzo (13) ⚠️ | Corvera de Toranzo | 3 |
| Parque de la Barquera ⚠️ | Torrelavega | 3 |
| Forêt de Los Corrales de Buelna (16) ⚠️ | Los Corrales de Buelna | 3 |
| Forêt de Reocín (22) ⚠️ | Reocín | 3 |
| Forêt de Santa María de Cayón (16) ⚠️ | Santa María de Cayón | 3 |
| Forêt de Santa María de Cayón (24) ⚠️ | Santa María de Cayón | 3 |
| Forêt de Villacarriedo (9) ⚠️ | Villacarriedo | 3 |
| Parque de Vegacorredor ⚠️ | Ramales de la Victoria | 3 |
| Parc de Santander (31) ⚠️ | Santander | 3 |
| Bois de Ramales de la Victoria (7) ⚠️ | Ramales de la Victoria | 3 |
| Bois de Ramales de la Victoria (11) ⚠️ | Ramales de la Victoria | 3 |
| Bois de Villafufre ⚠️ | Villafufre | 3 |
| Forêt de Luena (30) ⚠️ | Luena | 3 |
| Forêt de Valderredible (59) ⚠️ | Valderredible | 3 |
| Forêt de Soba (46) ⚠️ | Soba | 3 |
| Bois de Valle de Villaverde ⚠️ | Valle de Villaverde | 3 |
| Forêt de Castro-Urdiales (71) ⚠️ | Castro-Urdiales | 3 |
| Forêt de Valle de Villaverde (18) ⚠️ | Valle de Villaverde | 3 |
| Forêt de Valle de Villaverde (19) ⚠️ | Valle de Villaverde | 3 |
| Forêt de Valle de Villaverde (27) ⚠️ | Valle de Villaverde | 3 |
| Forêt de Soba (60) ⚠️ | Soba | 3 |
| Bois de Santa María de Cayón (602) ⚠️ | Santa María de Cayón | 3 |
| Bois de Valle de Villaverde (5) ⚠️ | Valle de Villaverde | 3 |
| Forêt de Soba (63) ⚠️ | Soba | 3 |
| Forêt de Castro-Urdiales (88) ⚠️ | Castro-Urdiales | 3 |
| Forêt de Arredondo (19) ⚠️ | Arredondo | 3 |
| Forêt de Liérganes (27) ⚠️ | Liérganes | 3 |
| Bois de Pesaguero (4) ⚠️ | Pesaguero | 3 |
| Bois de Liérganes (60) ⚠️ | Liérganes | 3 |
| Bois de Liérganes (62) ⚠️ | Liérganes | 3 |
| Forêt de Valderredible (60) ⚠️ | Valderredible | 3 |
| Terrenos de la antigua fábrica de vídrios La Cantábrica ⚠️ | Las Rozas de Valdearroyo | 3 |
| Forêt de Luena (37) ⚠️ | Luena | 3 |
| Forêt de Molledo (17) ⚠️ | Molledo | 3 |
| Bois de Alfoz de Lloredo (7) ⚠️ | Alfoz de Lloredo | 3 |
| Bois de Comillas (3) ⚠️ | Comillas | 3 |
| Bois de Valderredible (4) ⚠️ | Valderredible | 3 |
| Bois de San Vicente de la Barquera (25) ⚠️ | San Vicente de la Barquera | 3 |
| Forêt de Santiurde de Toranzo (12) ⚠️ | Santiurde de Toranzo | 3 |
| Forêt de Santillana del Mar (9) ⚠️ | Santillana del Mar | 3 |
| Bois de Selaya (3) ⚠️ | Selaya | 3 |
| Bois de Camaleño (10) ⚠️ | Camaleño | 3 |
| Bois de Camaleño (18) ⚠️ | Camaleño | 3 |
| Parque Ría del Carmen ⚠️ | Camargo | 3 |
| Forêt de Ramales de la Victoria (14) ⚠️ | Ramales de la Victoria | 3 |
| Bois de Castañeda (104) ⚠️ | Castañeda | 3 |
| Bois de Las Rozas de Valdearroyo (2) ⚠️ | Las Rozas de Valdearroyo | 3 |
| Parque Sotileza ⚠️ | Santander | 2 |
| Parque del Doctor Fleming ⚠️ | Santander | 2 |
| Bois de Santillana del Mar ⚠️ | Santillana del Mar | 2 |
| Prao las Peñas ⚠️ | Valdáliga | 2 |
| Bois de Valdáliga (11) ⚠️ | Valdáliga | 2 |
| Bois de Suances ⚠️ | Suances | 2 |
| Forêt de Entrambasaguas ⚠️ | Entrambasaguas | 2 |
| Forêt de Valderredible (4) ⚠️ | Valderredible | 2 |
| Bois de Riotuerto (6) ⚠️ | Riotuerto | 2 |
| Forêt de Rionansa (8) ⚠️ | Rionansa | 2 |
| Forêt de Herrerías (8) ⚠️ | Herrerías | 2 |
| Bois de Castañeda (2) ⚠️ | Castañeda | 2 |
| Forêt de Arredondo (3) ⚠️ | Soba | 2 |
| Forêt de Valderredible (31) ⚠️ | Valderredible | 2 |
| Forêt de Rionansa (21) ⚠️ | Rionansa | 2 |
| Forêt de Molledo (9) ⚠️ | Molledo | 2 |
| Forêt de Valderredible (35) ⚠️ | Valderredible | 2 |
| Forêt de Los Tojos (9) ⚠️ | Los Tojos | 2 |
| Forêt de Polaciones (26) ⚠️ | Polaciones | 2 |
| Forêt de Cabuérniga (14) ⚠️ | Cabuérniga | 2 |
| Forêt de Cabuérniga (15) ⚠️ | Cabuérniga | 2 |
| Forêt de Valdáliga (41) ⚠️ | Valdáliga | 2 |
| Forêt de Ruente (7) ⚠️ | Ruente | 2 |
| Forêt de Cieza (9) ⚠️ | Cieza | 2 |
| Forêt de Valderredible (46) ⚠️ | Valdeprado del Río | 2 |
| Forêt de Santiurde de Toranzo (8) ⚠️ | Santiurde de Toranzo | 2 |
| Forêt de Valdeprado del Río (23) ⚠️ | Valdeprado del Río | 2 |
| Forêt de Mazcuerras (23) ⚠️ | Mazcuerras | 2 |
| Forêt de Polaciones (54) ⚠️ | Polaciones | 2 |
| Parque de la Alianza ⚠️ | Santillana del Mar | 2 |
| Forêt de Entrambasaguas (18) ⚠️ | Entrambasaguas | 2 |
| Parque de Alceda ⚠️ | Corvera de Toranzo | 2 |
| Parque de los tres Laredos ⚠️ | Laredo | 2 |
| Bois de Liérganes ⚠️ | Liérganes | 2 |
| Forêt de Riotuerto (4) ⚠️ | Riotuerto | 2 |
| Forêt de Riotuerto (8) ⚠️ | Riotuerto | 2 |
| Forêt de Riotuerto (25) ⚠️ | Riotuerto | 2 |
| Forêt de Bárcena de Cicero (7) ⚠️ | Bárcena de Cicero | 2 |
| Forêt de Bárcena de Cicero (9) ⚠️ | Bárcena de Cicero | 2 |
| Parque Cros ⚠️ | Camargo | 2 |
| Parque Atilano Amigo ⚠️ | Camargo | 2 |
| Jardines de José María Pereda ⚠️ | Santander | 2 |
| Forêt de Entrambasaguas (27) ⚠️ | Entrambasaguas | 2 |
| Forêt de Riotuerto (66) ⚠️ | Riotuerto | 2 |
| Forêt de Medio Cudeyo (10) ⚠️ | Medio Cudeyo | 2 |
| Forêt de Riotuerto (96) ⚠️ | Riotuerto | 2 |
| Forêt de Riotuerto (101) ⚠️ | Riotuerto | 2 |
| Forêt de Medio Cudeyo (20) ⚠️ | Medio Cudeyo | 2 |
| Forêt de Entrambasaguas (46) ⚠️ | Entrambasaguas | 2 |
| Forêt de Riotuerto (130) ⚠️ | Riotuerto | 2 |
| Bois de Riotuerto (8) ⚠️ | Riotuerto | 2 |
| Forêt de Piélagos (11) ⚠️ | Piélagos | 2 |
| Forêt de Cartes (9) ⚠️ | Cartes | 2 |
| Parc de Miengo ⚠️ | Miengo | 2 |
| Forêt de Valdáliga (53) ⚠️ | Valdáliga | 2 |
| Parque de la Pedrosa ⚠️ | Torrelavega | 2 |
| Bois de Torrelavega (2) ⚠️ | Torrelavega | 2 |
| Forêt de Cartes (10) ⚠️ | Cartes | 2 |
| Forêt de Torrelavega (17) ⚠️ | Torrelavega | 2 |
| Forêt de Torrelavega (22) ⚠️ | Torrelavega | 2 |
| Forêt de Polanco (2) ⚠️ | Polanco | 2 |
| Forêt de Polanco (6) ⚠️ | Polanco | 2 |
| Forêt de Cartes (15) ⚠️ | Cartes | 2 |
| Forêt de San Felices de Buelna (11) ⚠️ | San Felices de Buelna | 2 |
| Bois de Puente Viesgo ⚠️ | Puente Viesgo | 2 |
| Forêt de Reocín (14) ⚠️ | Reocín | 2 |
| Forêt de Piélagos (22) ⚠️ | Piélagos | 2 |
| Forêt de Ampuero (13) ⚠️ | Ampuero | 2 |
| Forêt de Hazas de Cesto (6) ⚠️ | Hazas de Cesto | 2 |
| Bois de San Felices de Buelna ⚠️ | San Felices de Buelna | 2 |
| Bois de San Felices de Buelna (3) ⚠️ | San Felices de Buelna | 2 |
| Bois de Los Corrales de Buelna (4) ⚠️ | Los Corrales de Buelna | 2 |
| Parc de Santiurde de Toranzo (2) ⚠️ | Santiurde de Toranzo | 2 |
| Forêt de Puente Viesgo (17) ⚠️ | Puente Viesgo | 2 |
| Parque del Tintero ⚠️ | Colindres | 2 |
| Forêt de San Miguel de Aguayo (8) ⚠️ | San Miguel de Aguayo | 2 |
| Forêt de San Miguel de Aguayo (9) ⚠️ | San Miguel de Aguayo | 2 |
| Forêt de Alfoz de Lloredo (13) ⚠️ | Alfoz de Lloredo | 2 |
| Bois de Alfoz de Lloredo ⚠️ | Alfoz de Lloredo | 2 |
| Forêt de Meruelo (5) ⚠️ | Meruelo | 2 |
| Forêt de Meruelo (7) ⚠️ | Meruelo | 2 |
| Forêt de Liérganes (12) ⚠️ | Liérganes | 2 |
| Bosque del Nacimiento del Río Ebro ⚠️ | Hermandad de Campoo de Suso | 2 |
| Parc de Soba ⚠️ | Soba | 2 |
| Forêt de Villaescusa (18) ⚠️ | Villaescusa | 2 |
| Forêt de Piélagos (38) ⚠️ | Piélagos | 2 |
| Parc de El Astillero ⚠️ | El Astillero | 2 |
| Parque de Riosequillo ⚠️ | Villaescusa | 2 |
| Parque Pocillo de los Frailes ⚠️ | Castro-Urdiales | 2 |
| Bois de Ribamontán al Monte (2) ⚠️ | Ribamontán al Monte | 2 |
| Bois de Suances (4) ⚠️ | Suances | 2 |
| Forêt de Santillana del Mar (6) ⚠️ | Santillana del Mar | 2 |
| Bois de Valderredible (2) ⚠️ | Valderredible | 2 |
| Forêt de Castro-Urdiales (8) ⚠️ | Castro-Urdiales | 2 |
| Forêt de Castro-Urdiales (11) ⚠️ | Castro-Urdiales | 2 |
| Forêt de Castro-Urdiales (16) ⚠️ | Castro-Urdiales | 2 |
| Bois de Castro-Urdiales (10) ⚠️ | Castro-Urdiales | 2 |
| Bois de Castro-Urdiales (13) ⚠️ | Castro-Urdiales | 2 |
| Forêt de Castro-Urdiales (32) ⚠️ | Castro-Urdiales | 2 |
| Bois de Castro-Urdiales (19) ⚠️ | Castro-Urdiales | 2 |
| Bois de Castro-Urdiales (41) ⚠️ | Castro-Urdiales | 2 |
| Encinar de la Cantera de Bilbao ⚠️ | Camargo | 2 |
| Forêt de Peñarrubia (8) ⚠️ | Peñarrubia | 2 |
| Bois de Liérganes (5) ⚠️ | Liérganes | 2 |
| Bois de Liérganes (9) ⚠️ | Liérganes | 2 |
| Bois de Camaleño (4) ⚠️ | Camaleño | 2 |
| Forêt de Polanco (12) ⚠️ | Polanco | 2 |
| Parque de Riego ⚠️ | Colindres | 2 |
| Parque de Tregandín ⚠️ | Noja | 2 |
| Forêt de Vega de Pas (30) ⚠️ | Vega de Pas | 2 |
| Bois de Torrelavega (9) ⚠️ | Torrelavega | 2 |
| Forêt de Santa María de Cayón (6) ⚠️ | Santa María de Cayón | 2 |
| Forêt de San Felices de Buelna (15) ⚠️ | San Felices de Buelna | 2 |
| Forêt de Cabezón de la Sal (20) ⚠️ | Cabezón de la Sal | 2 |
| Forêt de Santa María de Cayón (33) ⚠️ | Santa María de Cayón | 2 |
| Forêt de Liérganes (17) ⚠️ | Liérganes | 2 |
| Forêt de Liérganes (18) ⚠️ | Liérganes | 2 |
| Forêt de Liérganes (22) ⚠️ | Liérganes | 2 |
| Forêt de Villaescusa (19) ⚠️ | Villaescusa | 2 |
| Forêt de Medio Cudeyo (26) ⚠️ | Medio Cudeyo | 2 |
| Bois de Santa María de Cayón (20) ⚠️ | Santa María de Cayón | 2 |
| Bois de Liérganes (11) ⚠️ | Penagos | 2 |
| Forêt de San Vicente de la Barquera (12) ⚠️ | San Vicente de la Barquera | 2 |
| Forêt de San Vicente de la Barquera (13) ⚠️ | San Vicente de la Barquera | 2 |
| Forêt de Val de San Vicente (40) ⚠️ | Val de San Vicente | 2 |
| Forêt de Val de San Vicente (41) ⚠️ | Val de San Vicente | 2 |
| Bois de Soba (3) ⚠️ | Soba | 2 |
| Bois de Voto ⚠️ | Voto | 2 |
| Parque público de Cubillas ⚠️ | Ramales de la Victoria | 2 |
| Bois de Ramales de la Victoria (3) ⚠️ | Ramales de la Victoria | 2 |
| Bois de Santa María de Cayón (220) ⚠️ | Santa María de Cayón | 2 |
| Forêt de Arredondo (10) ⚠️ | Arredondo | 2 |
| Bois de Marina de Cudeyo ⚠️ | Marina de Cudeyo | 2 |
| Forêt de Soba (32) ⚠️ | Soba | 2 |
| Forêt de Arredondo (12) ⚠️ | Arredondo | 2 |
| Bois de Santa María de Cayón (406) ⚠️ | Santa María de Cayón | 2 |
| Bois de Villafufre (2) ⚠️ | Villafufre | 2 |
| Forêt de Luena (32) ⚠️ | Luena | 2 |
| Parque de la Teja (2) ⚠️ | Santander | 2 |
| Forêt de Vega de Pas (33) ⚠️ | Vega de Pas | 2 |
| Forêt de Soba (36) ⚠️ | Soba | 2 |
| Forêt de Soba (50) ⚠️ | Soba | 2 |
| Forêt de Soba (52) ⚠️ | Soba | 2 |
| Forêt de Rasines (12) ⚠️ | Rasines | 2 |
| Forêt de Castro-Urdiales (70) ⚠️ | Castro-Urdiales | 2 |
| Forêt de Castro-Urdiales (75) ⚠️ | Castro-Urdiales | 2 |
| Forêt de Valle de Villaverde (16) ⚠️ | Valle de Villaverde | 2 |
| Forêt de Valle de Villaverde (35) ⚠️ | Valle de Villaverde | 2 |
| Forêt de Ramales de la Victoria (8) ⚠️ | Soba | 2 |
| Forêt de Castro-Urdiales (87) ⚠️ | Castro-Urdiales | 2 |
| Forêt de Soba (64) ⚠️ | Soba | 2 |
| Forêt de Soba (65) ⚠️ | Soba | 2 |
| Forêt de Santiurde de Reinosa (7) ⚠️ | Santiurde de Reinosa | 2 |
| Bois de Pesaguero ⚠️ | Pesaguero | 2 |
| Bois de Liérganes (61) ⚠️ | Liérganes | 2 |
| Bois de Miera (4) ⚠️ | Miera | 2 |
| Forêt de Villacarriedo (11) ⚠️ | Villacarriedo | 2 |
| Bois de Santiurde de Toranzo (10) ⚠️ | Santiurde de Toranzo | 2 |
| Forêt de Anievas (11) ⚠️ | Anievas | 2 |
| Bois de Campoo de Yuso (4) ⚠️ | Campoo de Yuso | 2 |
| Bois de Castañeda (80) ⚠️ | Castañeda | 2 |
| Forêt de Santiurde de Reinosa (11) ⚠️ | Santiurde de Reinosa | 2 |
| Parc de Hazas de Cesto (9) ⚠️ | Hazas de Cesto | 2 |
| Forêt de Los Tojos (20) ⚠️ | Los Tojos | 2 |
| Forêt de Los Tojos (21) ⚠️ | Los Tojos | 2 |
| Bois de Soba (9) ⚠️ | Soba | 2 |
| Bois de Reocín (12) ⚠️ | Reocín | 2 |
| Bois de San Vicente de la Barquera (5) ⚠️ | San Vicente de la Barquera | 2 |
| Bois de Alfoz de Lloredo (8) ⚠️ | Alfoz de Lloredo | 2 |
| Forêt de Alfoz de Lloredo (16) ⚠️ | Alfoz de Lloredo | 2 |
| Bois de Alfoz de Lloredo (10) ⚠️ | Alfoz de Lloredo | 2 |
| Forêt de Molledo (21) ⚠️ | Molledo | 2 |
| Bois de San Vicente de la Barquera (21) ⚠️ | San Vicente de la Barquera | 2 |
| Forêt de San Pedro del Romeral (11) ⚠️ | San Pedro del Romeral | 2 |
| Bois de San Vicente de la Barquera (24) ⚠️ | San Vicente de la Barquera | 2 |
| Bois de Cabezón de la Sal (2) ⚠️ | Cabezón de la Sal | 2 |
| Forêt de Bárcena de Cicero (11) ⚠️ | Bárcena de Cicero | 2 |
| Bois de Escalante ⚠️ | Escalante | 2 |
| Forêt de Miera (6) ⚠️ | Miera | 2 |
| Bois de Camargo (11) ⚠️ | Camargo | 2 |
| Bois de Camargo (14) ⚠️ | Camargo | 2 |
| Bois de El Astillero (3) ⚠️ | Camargo | 2 |
| Bois de Valderredible (6) ⚠️ | Valderredible | 2 |
| Forêt de Selaya (9) ⚠️ | Selaya | 2 |
| Bois de Castro-Urdiales (102) ⚠️ | Castro-Urdiales | 2 |
| Forêt de Selaya (12) ⚠️ | Selaya | 2 |
| Forêt de Valle de Villaverde (40) ⚠️ | Valle de Villaverde | 2 |
| Bois de Camaleño (9) ⚠️ | Camaleño | 2 |
| Bois de Vega de Pas (5) ⚠️ | Vega de Pas | 2 |
| Bois de Cillorigo de Liébana (4) ⚠️ | Cillorigo de Liébana | 2 |
| Bois de Camaleño (23) ⚠️ | Camaleño | 2 |
| Forêt de Marina de Cudeyo (3) ⚠️ | Marina de Cudeyo | 2 |
| Forêt de El Astillero ⚠️ | El Astillero | 2 |
| Bois de Marina de Cudeyo (15) ⚠️ | Marina de Cudeyo | 2 |
| Bois de Santa María de Cayón (664) ⚠️ | Santa María de Cayón | 2 |
| Bois de Santa María de Cayón (665) ⚠️ | Santa María de Cayón | 2 |
| Bois de Puente Viesgo (23) ⚠️ | Puente Viesgo | 2 |
| Forêt de Las Rozas de Valdearroyo (15) ⚠️ | Las Rozas de Valdearroyo | 2 |
| Jardines de Sobrellano ⚠️ | Comillas | 2 |
| Bois de Valderredible (15) ⚠️ | Valderredible | 2 |
| Bois de San Felices de Buelna (6) ⚠️ | San Felices de Buelna | 2 |
| Bois de Valderredible (22) ⚠️ | Valderredible | 2 |
| Forêt de Valderredible (73) ⚠️ | Valderredible | 2 |
| Parque de La Marga ⚠️ | Santander | 1 |
| Parque de González Trevilla ⚠️ | Santander | 1 |
| Parque de El Ferial ⚠️ | Medio Cudeyo | 1 |
| Parque del Doctor González Mesones ⚠️ | Santander | 1 |
| Bois de Valdáliga ⚠️ | Valdáliga | 1 |
| Peña el Ramo ⚠️ | Valdáliga | 1 |
| Forêt de Valdáliga (2) ⚠️ | Valdáliga | 1 |
| Forêt de Valdáliga (3) ⚠️ | Valdáliga | 1 |
| Forêt de Valdáliga (7) ⚠️ | Valdáliga | 1 |
| Bois de Valdáliga (9) ⚠️ | Valdáliga | 1 |
| Bois de Riotuerto ⚠️ | Riotuerto | 1 |
| Parque La Pereda ⚠️ | Santander | 1 |
| Bois de Valdáliga (13) ⚠️ | Valdáliga | 1 |
| Calle del Obispo Puchol Montis ⚠️ | Santander | 1 |
| Parque de las Fuentes ⚠️ | Reinosa | 1 |
| Parque de Amestoy ⚠️ | Castro-Urdiales | 1 |
| Parc de Laredo ⚠️ | Laredo | 1 |
| Bois de Suances (2) ⚠️ | Suances | 1 |
| Forêt de Entrambasaguas (2) ⚠️ | Entrambasaguas | 1 |
| Forêt de Entrambasaguas (3) ⚠️ | Entrambasaguas | 1 |
| Bois de Entrambasaguas (4) ⚠️ | Entrambasaguas | 1 |
| Bois de Entrambasaguas (5) ⚠️ | Entrambasaguas | 1 |
| Forêt de Valderredible (2) ⚠️ | Valderredible | 1 |
| Forêt de Ruesga (2) ⚠️ | Ruesga | 1 |
| Forêt de Polaciones (3) ⚠️ | Polaciones | 1 |
| Forêt de Piélagos ⚠️ | Piélagos | 1 |
| Forêt de Rionansa (2) ⚠️ | Rionansa | 1 |
| Forêt de Herrerías (2) ⚠️ | Herrerías | 1 |
| Forêt de Arenas de Iguña ⚠️ | Arenas de Iguña | 1 |
| Forêt de Polaciones (7) ⚠️ | Polaciones | 1 |
| Forêt de Guriezo (2) ⚠️ | Guriezo | 1 |
| Forêt de Rionansa (4) ⚠️ | Rionansa | 1 |
| Forêt de Ampuero ⚠️ | Ampuero | 1 |
| Forêt de Lamasón (8) ⚠️ | Lamasón | 1 |
| Forêt de Vega de Pas (3) ⚠️ | Vega de Pas | 1 |
| Forêt de Polaciones (11) ⚠️ | Polaciones | 1 |
| Forêt de Rionansa (12) ⚠️ | Rionansa | 1 |
| Forêt de Tresviso ⚠️ | Tresviso | 1 |
| Forêt de Santa María de Cayón ⚠️ | Santa María de Cayón | 1 |
| Forêt de Guriezo (6) ⚠️ | Guriezo | 1 |
| Forêt de Cillorigo de Liébana (5) ⚠️ | Cillorigo de Liébana | 1 |
| Forêt de Polaciones (14) ⚠️ | Polaciones | 1 |
| Forêt de Herrerías (11) ⚠️ | Herrerías | 1 |
| Forêt de Los Tojos (5) ⚠️ | Los Tojos | 1 |
| Forêt de Valderredible (24) ⚠️ | Valderredible | 1 |
| Forêt de Cabezón de la Sal (9) ⚠️ | Cabezón de la Sal | 1 |
| Forêt de Voto (4) ⚠️ | Voto | 1 |
| Forêt de Rionansa (18) ⚠️ | Rionansa | 1 |
| Forêt de Lamasón (15) ⚠️ | Lamasón | 1 |
| Forêt de Molledo (8) ⚠️ | Molledo | 1 |
| Forêt de Villaescusa ⚠️ | Villaescusa | 1 |
| Forêt de Las Rozas de Valdearroyo (5) ⚠️ | Las Rozas de Valdearroyo | 1 |
| Forêt de Los Tojos (7) ⚠️ | Los Tojos | 1 |
| Forêt de Ruente (2) ⚠️ | Ruente | 1 |
| Forêt de Ruesga (10) ⚠️ | Ruesga | 1 |
| Forêt de Castañeda ⚠️ | Castañeda | 1 |
| Forêt de San Roque de Riomiera (5) ⚠️ | San Roque de Riomiera | 1 |
| Forêt de Valderredible (33) ⚠️ | Valderredible | 1 |
| Forêt de Vega de Liébana (5) ⚠️ | Vega de Liébana | 1 |
| Forêt de Los Tojos (8) ⚠️ | Los Tojos | 1 |
| Forêt de Herrerías (19) ⚠️ | Herrerías | 1 |
| Forêt de Valdáliga (35) ⚠️ | Valdáliga | 1 |
| Forêt de Ruesga (12) ⚠️ | Ruesga | 1 |
| Forêt de Luena (11) ⚠️ | Luena | 1 |
| Forêt de Polaciones (30) ⚠️ | Polaciones | 1 |
| Forêt de Entrambasaguas (12) ⚠️ | Entrambasaguas | 1 |
| Forêt de Cillorigo de Liébana (12) ⚠️ | Cillorigo de Liébana | 1 |
| Forêt de Polaciones (32) ⚠️ | Polaciones | 1 |
| Forêt de Cillorigo de Liébana (13) ⚠️ | Cillorigo de Liébana | 1 |
| Forêt de Herrerías (27) ⚠️ | Herrerías | 1 |
| Forêt de Vega de Pas (13) ⚠️ | Vega de Pas | 1 |
| Forêt de Valderredible (43) ⚠️ | Valderredible | 1 |
| Forêt de Cabezón de la Sal (14) ⚠️ | Cabezón de la Sal | 1 |
| Forêt de Polaciones (36) ⚠️ | Polaciones | 1 |
| Forêt de Luena (17) ⚠️ | Luena | 1 |
| Forêt de Rionansa (37) ⚠️ | Rionansa | 1 |
| Forêt de Polaciones (41) ⚠️ | Polaciones | 1 |
| Forêt de Valdeprado del Río (21) ⚠️ | Valdeprado del Río | 1 |
| Forêt de Polaciones (42) ⚠️ | Polaciones | 1 |
| Forêt de Herrerías (31) ⚠️ | Herrerías | 1 |
| Forêt de Rionansa (41) ⚠️ | Rionansa | 1 |
| Forêt de Piélagos (9) ⚠️ | Piélagos | 1 |
| Forêt de Tudanca (25) ⚠️ | Tudanca | 1 |
| Forêt de Herrerías (33) ⚠️ | Herrerías | 1 |
| Forêt de Polaciones (46) ⚠️ | Polaciones | 1 |
| Forêt de Las Rozas de Valdearroyo (13) ⚠️ | Las Rozas de Valdearroyo | 1 |
| Forêt de Cieza (11) ⚠️ | Cieza | 1 |
| Forêt de Polaciones (48) ⚠️ | Polaciones | 1 |
| Forêt de Ramales de la Victoria (4) ⚠️ | Ramales de la Victoria | 1 |
| Forêt de Val de San Vicente (19) ⚠️ | Val de San Vicente | 1 |
| Forêt de Polaciones (51) ⚠️ | Polaciones | 1 |
| Forêt de Medio Cudeyo (6) ⚠️ | Medio Cudeyo | 1 |
| Forêt de Ribamontán al Monte (3) ⚠️ | Ribamontán al Monte | 1 |
| Forêt de Medio Cudeyo (8) ⚠️ | Medio Cudeyo | 1 |
| Bois de Medio Cudeyo (4) ⚠️ | Medio Cudeyo | 1 |
| Parque del Campo Colorado ⚠️ | Reinosa | 1 |
| Forêt de Soba (31) ⚠️ | Soba | 1 |
| Forêt de Santander ⚠️ | Santander | 1 |
| Parque de los Tres Pescadores ⚠️ | Laredo | 1 |
| Alameda El Bosque ⚠️ | Laredo | 1 |
| Bois de Liérganes (2) ⚠️ | Liérganes | 1 |
| Forêt de Riotuerto (10) ⚠️ | Riotuerto | 1 |
| Forêt de Riotuerto (19) ⚠️ | Entrambasaguas | 1 |
| Forêt de Riotuerto (24) ⚠️ | Riotuerto | 1 |
| Bois de Riotuerto (7) ⚠️ | Riotuerto | 1 |
| Forêt de Riotuerto (28) ⚠️ | Riotuerto | 1 |
| Forêt de Bárcena de Cicero (8) ⚠️ | Bárcena de Cicero | 1 |
| Forêt de Riotuerto (37) ⚠️ | Riotuerto | 1 |
| Forêt de Riotuerto (38) ⚠️ | Riotuerto | 1 |
| Forêt de Riotuerto (39) ⚠️ | Riotuerto | 1 |
| Forêt de Bareyo (2) ⚠️ | Bareyo | 1 |
| Forêt de Riotuerto (44) ⚠️ | Riotuerto | 1 |
| Forêt de Liérganes (3) ⚠️ | Liérganes | 1 |
| Forêt de Riotuerto (47) ⚠️ | Riotuerto | 1 |
| Forêt de Riotuerto (50) ⚠️ | Riotuerto | 1 |
| Forêt de Riotuerto (53) ⚠️ | Riotuerto | 1 |
| Forêt de Riotuerto (63) ⚠️ | Riotuerto | 1 |
| Forêt de Entrambasaguas (21) ⚠️ | Entrambasaguas | 1 |
| Forêt de Entrambasaguas (23) ⚠️ | Entrambasaguas | 1 |
| Forêt de Riotuerto (67) ⚠️ | Riotuerto | 1 |
| Forêt de Entrambasaguas (42) ⚠️ | Entrambasaguas | 1 |
| Forêt de Riotuerto (76) ⚠️ | Riotuerto | 1 |
| Forêt de Riotuerto (77) ⚠️ | Riotuerto | 1 |
| Forêt de Riotuerto (79) ⚠️ | Riotuerto | 1 |
| Forêt de Riotuerto (91) ⚠️ | Riotuerto | 1 |
| Forêt de Medio Cudeyo (11) ⚠️ | Medio Cudeyo | 1 |
| Forêt de Medio Cudeyo (12) ⚠️ | Medio Cudeyo | 1 |
| Forêt de Medio Cudeyo (16) ⚠️ | Medio Cudeyo | 1 |
| Forêt de Riotuerto (94) ⚠️ | Liérganes | 1 |
| Forêt de Riotuerto (97) ⚠️ | Riotuerto | 1 |
| Forêt de Riotuerto (98) ⚠️ | Riotuerto | 1 |
| Forêt de Riotuerto (100) ⚠️ | Riotuerto | 1 |
| Forêt de Riotuerto (102) ⚠️ | Riotuerto | 1 |
| Forêt de Riotuerto (104) ⚠️ | Riotuerto | 1 |
| Forêt de Liérganes (8) ⚠️ | Liérganes | 1 |
| Forêt de Liérganes (10) ⚠️ | Liérganes | 1 |
| Forêt de Liérganes (11) ⚠️ | Liérganes | 1 |
| Forêt de Riotuerto (127) ⚠️ | Riotuerto | 1 |
| Forêt de Riotuerto (131) ⚠️ | Riotuerto | 1 |
| Forêt de Riotuerto (132) ⚠️ | Riotuerto | 1 |
| Forêt de Riotuerto (133) ⚠️ | Riotuerto | 1 |
| Forêt de Riotuerto (136) ⚠️ | Riotuerto | 1 |
| Forêt de Riotuerto (137) ⚠️ | Riotuerto | 1 |
| Forêt de Riotuerto (139) ⚠️ | Riotuerto | 1 |
| Forêt de Riotuerto (141) ⚠️ | Riotuerto | 1 |
| Parque El Refugio ⚠️ | Santander | 1 |
| Parc de Castañeda ⚠️ | Castañeda | 1 |
| Forêt de Puente Viesgo (11) ⚠️ | Puente Viesgo | 1 |
| Parque Güell y Martos ⚠️ | Comillas | 1 |
| Parque de El Camarao ⚠️ | Reocín | 1 |
| Bois de Los Corrales de Buelna (3) ⚠️ | Los Corrales de Buelna | 1 |
| Forêt de Villaescusa (9) ⚠️ | Villaescusa | 1 |
| Forêt de Villaescusa (10) ⚠️ | Villaescusa | 1 |
| Parc de Laredo (4) ⚠️ | Laredo | 1 |
| Forêt de Torrelavega (15) ⚠️ | Torrelavega | 1 |
| Bois de Torrelavega (3) ⚠️ | Torrelavega | 1 |
| Forêt de Torrelavega (19) ⚠️ | Torrelavega | 1 |
| Bois de Torrelavega (5) ⚠️ | Torrelavega | 1 |
| Parc de Santander (9) ⚠️ | Santander | 1 |
| Bois de Cartes (2) ⚠️ | Cartes | 1 |
| Forêt de Torrelavega (20) ⚠️ | Torrelavega | 1 |
| Forêt de Torrelavega (23) ⚠️ | Torrelavega | 1 |
| Forêt de Santillana del Mar (5) ⚠️ | Santillana del Mar | 1 |
| Forêt de Torrelavega (25) ⚠️ | Torrelavega | 1 |
| Forêt de Reocín (10) ⚠️ | Reocín | 1 |
| Bois de Reocín (2) ⚠️ | Reocín | 1 |
| Forêt de Reocín (12) ⚠️ | Reocín | 1 |
| Bois de Reocín (5) ⚠️ | Reocín | 1 |
| Forêt de Reocín (13) ⚠️ | Reocín | 1 |
| Área recreativa de Limpias ⚠️ | Limpias | 1 |
| Parc de Piélagos (2) ⚠️ | Piélagos | 1 |
| Parc de Miengo (2) ⚠️ | Miengo | 1 |
| Forêt de Piélagos (25) ⚠️ | Piélagos | 1 |
| Parc de Piélagos (5) ⚠️ | Piélagos | 1 |
| Forêt de Miengo (3) ⚠️ | Miengo | 1 |
| Forêt de Bareyo (3) ⚠️ | Bareyo | 1 |
| Parc de Santander (12) ⚠️ | Santander | 1 |
| Forêt de Solórzano (6) ⚠️ | Solórzano | 1 |
| Forêt de Solórzano (10) ⚠️ | Solórzano | 1 |
| Parc de Piélagos (6) ⚠️ | Piélagos | 1 |
| Parc de Corvera de Toranzo ⚠️ | Corvera de Toranzo | 1 |
| Bois de Suances (3) ⚠️ | Suances | 1 |
| Forêt de Polanco (7) ⚠️ | Polanco | 1 |
| Forêt de Polanco (8) ⚠️ | Polanco | 1 |
| Bois de San Felices de Buelna (2) ⚠️ | San Felices de Buelna | 1 |
| Bois de Los Corrales de Buelna (5) ⚠️ | Los Corrales de Buelna | 1 |
| Forêt de Santiurde de Toranzo (10) ⚠️ | Santiurde de Toranzo | 1 |
| Bois de Santiurde de Toranzo ⚠️ | Santiurde de Toranzo | 1 |
| Parque de El Centenario ⚠️ | Torrelavega | 1 |
| Bois de Cartes (3) ⚠️ | Cartes | 1 |
| Forêt de Castañeda (5) ⚠️ | Castañeda | 1 |
| Bois de Comillas ⚠️ | Comillas | 1 |
| Parc de Ribamontán al Mar ⚠️ | Ribamontán al Mar | 1 |
| Bois de Torrelavega (7) ⚠️ | Torrelavega | 1 |
| Forêt de Alfoz de Lloredo (10) ⚠️ | Alfoz de Lloredo | 1 |
| Forêt de Cartes (19) ⚠️ | Cartes | 1 |
| Forêt de Reocín (17) ⚠️ | Reocín | 1 |
| Bois de Cartes (7) ⚠️ | Cartes | 1 |
| Forêt de Torrelavega (27) ⚠️ | Torrelavega | 1 |
| Forêt de Val de San Vicente (28) ⚠️ | Val de San Vicente | 1 |
| Forêt de Val de San Vicente (30) ⚠️ | Val de San Vicente | 1 |
| Bois de Reocín (8) ⚠️ | Reocín | 1 |
| Forêt de Vega de Pas (26) ⚠️ | Vega de Pas | 1 |
| Forêt de Vega de Pas (27) ⚠️ | Vega de Pas | 1 |
| Forêt de Cabezón de la Sal (16) ⚠️ | Cabezón de la Sal | 1 |
| Forêt de Cabezón de la Sal (17) ⚠️ | Cabezón de la Sal | 1 |
| Forêt de Piélagos (36) ⚠️ | Piélagos | 1 |
| Parque de la Ribera ⚠️ | Suances | 1 |
| Bois de Santander ⚠️ | Santander | 1 |
| Parque de las Canteras de Cueto ⚠️ | Santander | 1 |
| Plaza Roja ⚠️ | Santander | 1 |
| Parque de Gamazo ⚠️ | Santander | 1 |
| Forêt de Castro-Urdiales (7) ⚠️ | Castro-Urdiales | 1 |
| Parc de Santa Cruz de Bezana (4) ⚠️ | Santa Cruz de Bezana | 1 |
| Parque Mitológico de Mina Pepita ⚠️ | Medio Cudeyo | 1 |
| Forêt de Medio Cudeyo (23) ⚠️ | Medio Cudeyo | 1 |
| Parque de Mendicoague ⚠️ | Santander | 1 |
| Forêt de Val de San Vicente (34) ⚠️ | Val de San Vicente | 1 |
| Parque Manuel Barquín Agüero ⚠️ | Torrelavega | 1 |
| Forêt de Castro-Urdiales (9) ⚠️ | Castro-Urdiales | 1 |
| Bois de Castro-Urdiales (4) ⚠️ | Castro-Urdiales | 1 |
| Forêt de Castro-Urdiales (12) ⚠️ | Castro-Urdiales | 1 |
| Forêt de Castro-Urdiales (13) ⚠️ | Castro-Urdiales | 1 |
| Forêt de Castro-Urdiales (15) ⚠️ | Castro-Urdiales | 1 |
| Bois de Castro-Urdiales (5) ⚠️ | Castro-Urdiales | 1 |
| Bois de Castro-Urdiales (7) ⚠️ | Castro-Urdiales | 1 |
| Forêt de Castro-Urdiales (18) ⚠️ | Castro-Urdiales | 1 |
| Bois de Castro-Urdiales (9) ⚠️ | Castro-Urdiales | 1 |
| Forêt de Castro-Urdiales (26) ⚠️ | Castro-Urdiales | 1 |
| Forêt de Castro-Urdiales (29) ⚠️ | Castro-Urdiales | 1 |
| Forêt de Castro-Urdiales (38) ⚠️ | Castro-Urdiales | 1 |
| Bois de Castro-Urdiales (42) ⚠️ | Castro-Urdiales | 1 |
| Bois de Castro-Urdiales (52) ⚠️ | Castro-Urdiales | 1 |
| Forêt de Castro-Urdiales (42) ⚠️ | Castro-Urdiales | 1 |
| Forêt de Castro-Urdiales (44) ⚠️ | Castro-Urdiales | 1 |
| La Pista ⚠️ | Camargo | 1 |
| Forêt de Castro-Urdiales (49) ⚠️ | Castro-Urdiales | 1 |
| Bois de Castro-Urdiales (63) ⚠️ | Castro-Urdiales | 1 |
| Bois de Castro-Urdiales (66) ⚠️ | Castro-Urdiales | 1 |
| Forêt de Castro-Urdiales (55) ⚠️ | Castro-Urdiales | 1 |
| Forêt de Castro-Urdiales (57) ⚠️ | Castro-Urdiales | 1 |
| Forêt de Castro-Urdiales (58) ⚠️ | Castro-Urdiales | 1 |
| Forêt de Castro-Urdiales (59) ⚠️ | Castro-Urdiales | 1 |
| Parc de Castro-Urdiales (4) ⚠️ | Castro-Urdiales | 1 |
| Bois de Castro-Urdiales (69) ⚠️ | Castro-Urdiales | 1 |
| Bois de Castro-Urdiales (70) ⚠️ | Castro-Urdiales | 1 |
| Forêt de Castro-Urdiales (64) ⚠️ | Castro-Urdiales | 1 |
| Bois de Castro-Urdiales (82) ⚠️ | Castro-Urdiales | 1 |
| Forêt de Castro-Urdiales (65) ⚠️ | Castro-Urdiales | 1 |
| Parc de Suances (2) ⚠️ | Suances | 1 |
| Forêt de Castro-Urdiales (68) ⚠️ | Castro-Urdiales | 1 |
| Parque Los Juncos ⚠️ | Noja | 1 |
| Bois de Liérganes (7) ⚠️ | Liérganes | 1 |
| Bois de Liérganes (8) ⚠️ | Liérganes | 1 |
| Forêt de Camaleño (8) ⚠️ | Camaleño | 1 |
| Bois de Camaleño (5) ⚠️ | Camaleño | 1 |
| Bois de Camaleño (6) ⚠️ | Camaleño | 1 |
| Forêt de Camaleño (10) ⚠️ | Camaleño | 1 |
| Bois de Ruente ⚠️ | Ruente | 1 |
| Bois de Bárcena de Cicero (2) ⚠️ | Bárcena de Cicero | 1 |
| Parc de Camargo (4) ⚠️ | Camargo | 1 |
| Parc de Camargo (7) ⚠️ | Camargo | 1 |
| Bois de San Vicente de la Barquera (3) ⚠️ | San Vicente de la Barquera | 1 |
| Bois de Penagos ⚠️ | Penagos | 1 |
| Bois de Penagos (3) ⚠️ | Penagos | 1 |
| Palacio del Marqués de Albaicín ⚠️ | Noja | 1 |
| Bois de Arenas de Iguña (4) ⚠️ | Arenas de Iguña | 1 |
| Forêt de Campoo de Yuso (15) ⚠️ | Campoo de Yuso | 1 |
| Bois de Herrerías (4) ⚠️ | Herrerías | 1 |
| Parc de Santander (24) ⚠️ | Santander | 1 |
| Forêt de Santa María de Cayón (8) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (4) ⚠️ | Santa María de Cayón | 1 |
| Parque de La Lama ⚠️ | San Felices de Buelna | 1 |
| Forêt de Los Corrales de Buelna (14) ⚠️ | Los Corrales de Buelna | 1 |
| Bois de Los Corrales de Buelna (7) ⚠️ | Los Corrales de Buelna | 1 |
| Parque Ría de Solía ⚠️ | El Astillero | 1 |
| Bois de Los Corrales de Buelna (8) ⚠️ | Los Corrales de Buelna | 1 |
| Parc de Torrelavega (24) ⚠️ | Torrelavega | 1 |
| Bois de Rionansa ⚠️ | Rionansa | 1 |
| Parque Los Pinares (2) ⚠️ | Noja | 1 |
| Parc de Santoña (2) ⚠️ | Santoña | 1 |
| Forêt de Cabezón de la Sal (21) ⚠️ | Cabezón de la Sal | 1 |
| Forêt de Cabezón de la Sal (22) ⚠️ | Cabezón de la Sal | 1 |
| Forêt de Valdáliga (55) ⚠️ | Valdáliga | 1 |
| Forêt de San Vicente de la Barquera (9) ⚠️ | San Vicente de la Barquera | 1 |
| Forêt de Val de San Vicente (39) ⚠️ | Val de San Vicente | 1 |
| Forêt de San Vicente de la Barquera (11) ⚠️ | San Vicente de la Barquera | 1 |
| Forêt de Santa María de Cayón (18) ⚠️ | Santa María de Cayón | 1 |
| Forêt de Santa María de Cayón (19) ⚠️ | Santa María de Cayón | 1 |
| Forêt de Medio Cudeyo (25) ⚠️ | Liérganes | 1 |
| Forêt de Santa María de Cayón (22) ⚠️ | Santa María de Cayón | 1 |
| Forêt de Santa María de Cayón (23) ⚠️ | Santa María de Cayón | 1 |
| Forêt de Villafufre (2) ⚠️ | Villafufre | 1 |
| Forêt de Vega de Pas (32) ⚠️ | Vega de Pas | 1 |
| Forêt de Santa María de Cayón (26) ⚠️ | Santa María de Cayón | 1 |
| Forêt de Santa María de Cayón (27) ⚠️ | Santa María de Cayón | 1 |
| Forêt de Santa María de Cayón (28) ⚠️ | Santa María de Cayón | 1 |
| Forêt de Saro (4) ⚠️ | Saro | 1 |
| Forêt de Santa María de Cayón (30) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (8) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (9) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (10) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (11) ⚠️ | Santa María de Cayón | 1 |
| Forêt de Santa María de Cayón (31) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (12) ⚠️ | Santa María de Cayón | 1 |
| Forêt de Santa María de Cayón (38) ⚠️ | Santa María de Cayón | 1 |
| Forêt de Liérganes (15) ⚠️ | Liérganes | 1 |
| Forêt de Liérganes (25) ⚠️ | Liérganes | 1 |
| Forêt de Villaescusa (22) ⚠️ | Villaescusa | 1 |
| Forêt de Santa María de Cayón (44) ⚠️ | Santa María de Cayón | 1 |
| Forêt de Santa María de Cayón (50) ⚠️ | Santa María de Cayón | 1 |
| Forêt de Santa María de Cayón (54) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (30) ⚠️ | Santa María de Cayón | 1 |
| Bois de Penagos (19) ⚠️ | Penagos | 1 |
| Area recreativa de Jesús del Monte ⚠️ | Hazas de Cesto | 1 |
| Forêt de Reocín (23) ⚠️ | Reocín | 1 |
| Bois de Liérganes (10) ⚠️ | Liérganes | 1 |
| Bois de Liérganes (15) ⚠️ | Liérganes | 1 |
| Bois de Liérganes (17) ⚠️ | Liérganes | 1 |
| Bois de Liérganes (22) ⚠️ | Liérganes | 1 |
| Bois de Liérganes (26) ⚠️ | Liérganes | 1 |
| Bois de Liérganes (31) ⚠️ | Liérganes | 1 |
| Forêt de San Vicente de la Barquera (14) ⚠️ | San Vicente de la Barquera | 1 |
| Bois de Liérganes (35) ⚠️ | Liérganes | 1 |
| Bois de Liérganes (42) ⚠️ | Liérganes | 1 |
| Bois de Liérganes (44) ⚠️ | Liérganes | 1 |
| Bois de Liérganes (46) ⚠️ | Liérganes | 1 |
| Bois de Medio Cudeyo (16) ⚠️ | Medio Cudeyo | 1 |
| Bois de Liérganes (47) ⚠️ | Liérganes | 1 |
| Bois de Liérganes (48) ⚠️ | Liérganes | 1 |
| Bois de Liérganes (49) ⚠️ | Liérganes | 1 |
| Bois de Liérganes (56) ⚠️ | Liérganes | 1 |
| Bois de Medio Cudeyo (25) ⚠️ | Medio Cudeyo | 1 |
| Bois de Medio Cudeyo (28) ⚠️ | Medio Cudeyo | 1 |
| Bois de Medio Cudeyo (36) ⚠️ | Medio Cudeyo | 1 |
| Bois de Medio Cudeyo (38) ⚠️ | Medio Cudeyo | 1 |
| Bois de Santa María de Cayón (44) ⚠️ | Santa María de Cayón | 1 |
| Forêt de Bareyo (4) ⚠️ | Bareyo | 1 |
| Bois de Santa María de Cayón (49) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (57) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (64) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (116) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (165) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (167) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (175) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (180) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (223) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (241) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (251) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (265) ⚠️ | Santa María de Cayón | 1 |
| Bois de Castañeda (4) ⚠️ | Castañeda | 1 |
| Bois de Ramales de la Victoria (13) ⚠️ | Ramales de la Victoria | 1 |
| Bois de Castañeda (10) ⚠️ | Castañeda | 1 |
| Bois de Castañeda (13) ⚠️ | Castañeda | 1 |
| Bois de Santa María de Cayón (308) ⚠️ | Santa María de Cayón | 1 |
| Bois de Castañeda (15) ⚠️ | Castañeda | 1 |
| Bois de Santa María de Cayón (316) ⚠️ | Santa María de Cayón | 1 |
| Forêt de Arredondo (16) ⚠️ | Arredondo | 1 |
| Parque de María Cristina ⚠️ | Santander | 1 |
| Bois de Santa María de Cayón (342) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (355) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (378) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (397) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (411) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (437) ⚠️ | Santa María de Cayón | 1 |
| Forêt de Luena (28) ⚠️ | Luena | 1 |
| Forêt de Luena (29) ⚠️ | Luena | 1 |
| Bois de Santa María de Cayón (472) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (476) ⚠️ | Santa María de Cayón | 1 |
| Bois de Riotuerto (10) ⚠️ | Riotuerto | 1 |
| Bois de Riotuerto (11) ⚠️ | Riotuerto | 1 |
| Bois de Riotuerto (12) ⚠️ | Riotuerto | 1 |
| Bois de Riotuerto (13) ⚠️ | Riotuerto | 1 |
| Parque de El Corrobolos ⚠️ | Hermandad de Campoo de Suso | 1 |
| Forêt de Las Rozas de Valdearroyo (14) ⚠️ | Las Rozas de Valdearroyo | 1 |
| Bois de Santa María de Cayón (494) ⚠️ | Santa María de Cayón | 1 |
| Parc de Santander (38) ⚠️ | Santander | 1 |
| Forêt de Soba (34) ⚠️ | Soba | 1 |
| Bois de Santa María de Cayón (500) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (511) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (514) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (519) ⚠️ | Santa María de Cayón | 1 |
| Forêt de Soba (42) ⚠️ | Soba | 1 |
| Forêt de Soba (45) ⚠️ | Soba | 1 |
| Forêt de Soba (49) ⚠️ | Soba | 1 |
| Forêt de Rasines (11) ⚠️ | Rasines | 1 |
| Forêt de Ramales de la Victoria (7) ⚠️ | Ramales de la Victoria | 1 |
| Forêt de Valle de Villaverde (9) ⚠️ | Valle de Villaverde | 1 |
| Forêt de Valle de Villaverde (10) ⚠️ | Valle de Villaverde | 1 |
| Forêt de Valle de Villaverde (11) ⚠️ | Valle de Villaverde | 1 |
| Forêt de Valle de Villaverde (13) ⚠️ | Valle de Villaverde | 1 |
| Forêt de Valle de Villaverde (14) ⚠️ | Valle de Villaverde | 1 |
| Bois de Valle de Villaverde (2) ⚠️ | Valle de Villaverde | 1 |
| Forêt de Valle de Villaverde (15) ⚠️ | Valle de Villaverde | 1 |
| Forêt de Valle de Villaverde (17) ⚠️ | Valle de Villaverde | 1 |
| Forêt de Valle de Villaverde (21) ⚠️ | Valle de Villaverde | 1 |
| Forêt de Soba (54) ⚠️ | Soba | 1 |
| Forêt de Soba (55) ⚠️ | Soba | 1 |
| Forêt de Soba (59) ⚠️ | Soba | 1 |
| Forêt de Riotuerto (143) ⚠️ | Riotuerto | 1 |
| Bois de Santa María de Cayón (548) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (552) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (556) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (570) ⚠️ | Santa María de Cayón | 1 |
| Forêt de Valle de Villaverde (37) ⚠️ | Valle de Villaverde | 1 |
| Forêt de Castro-Urdiales (90) ⚠️ | Castro-Urdiales | 1 |
| Bois de Santa María de Cayón (634) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (642) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (647) ⚠️ | Santa María de Cayón | 1 |
| Forêt de Liérganes (26) ⚠️ | Liérganes | 1 |
| Bois de Liérganes (57) ⚠️ | Liérganes | 1 |
| Bois de Saro (22) ⚠️ | Saro | 1 |
| Forêt de Soba (66) ⚠️ | Soba | 1 |
| Bois de Santander (5) ⚠️ | Santander | 1 |
| Bois de Pesaguero (3) ⚠️ | Pesaguero | 1 |
| Bois de Pesaguero (5) ⚠️ | Pesaguero | 1 |
| Bois de Penagos (74) ⚠️ | Penagos | 1 |
| Bois de Villaescusa (6) ⚠️ | Villaescusa | 1 |
| Parc de Santander (44) ⚠️ | Santander | 1 |
| Bois de Penagos (77) ⚠️ | Penagos | 1 |
| Forêt de Vega de Pas (34) ⚠️ | Vega de Pas | 1 |
| Bois de Penagos (78) ⚠️ | Penagos | 1 |
| Bois de Penagos (85) ⚠️ | Penagos | 1 |
| Bois de Miera (3) ⚠️ | Miera | 1 |
| Forêt de Liérganes (29) ⚠️ | Liérganes | 1 |
| Bois de Penagos (93) ⚠️ | Penagos | 1 |
| Bois de Penagos (96) ⚠️ | Penagos | 1 |
| Bois de Penagos (99) ⚠️ | Penagos | 1 |
| Forêt de Villacarriedo (12) ⚠️ | Villacarriedo | 1 |
| Bois de Riotuerto (15) ⚠️ | Riotuerto | 1 |
| Forêt de Medio Cudeyo (27) ⚠️ | Medio Cudeyo | 1 |
| Bois de Castañeda (34) ⚠️ | Castañeda | 1 |
| Bois de Castañeda (36) ⚠️ | Castañeda | 1 |
| Forêt de Rionansa (55) ⚠️ | Rionansa | 1 |
| Bois de Castañeda (39) ⚠️ | Castañeda | 1 |
| Forêt de Castañeda (9) ⚠️ | Castañeda | 1 |
| Parc de Piélagos (15) ⚠️ | Piélagos | 1 |
| Bois de Castañeda (65) ⚠️ | Castañeda | 1 |
| Parc de Argoños (4) ⚠️ | Argoños | 1 |
| Bois de Castañeda (72) ⚠️ | Castañeda | 1 |
| Parc de Santander (45) ⚠️ | Santander | 1 |
| Bois de Castañeda (89) ⚠️ | Castañeda | 1 |
| Bois de Castañeda (90) ⚠️ | Castañeda | 1 |
| Bois de Castañeda (93) ⚠️ | Castañeda | 1 |
| Bois de Puente Viesgo (4) ⚠️ | Puente Viesgo | 1 |
| Forêt de Santiurde de Reinosa (10) ⚠️ | Santiurde de Reinosa | 1 |
| Bois de Castañeda (102) ⚠️ | Castañeda | 1 |
| Parc de Santoña (5) ⚠️ | Santoña | 1 |
| Forêt de Selaya (8) ⚠️ | Selaya | 1 |
| Forêt de Riotuerto (149) ⚠️ | Riotuerto | 1 |
| Parc de Hazas de Cesto (8) ⚠️ | Hazas de Cesto | 1 |
| Bois de Bárcena de Cicero (4) ⚠️ | Bárcena de Cicero | 1 |
| Forêt de Vega de Pas (36) ⚠️ | Vega de Pas | 1 |
| Parc de Torrelavega (37) ⚠️ | Torrelavega | 1 |
| Bois de Piélagos (2) ⚠️ | Piélagos | 1 |
| Bois de Soba (8) ⚠️ | Soba | 1 |
| Bois de San Roque de Riomiera (3) ⚠️ | San Roque de Riomiera | 1 |
| Bois de Soba (10) ⚠️ | Soba | 1 |
| Monte San Martín ⚠️ | Marina de Cudeyo | 1 |
| Bois de Ruente (3) ⚠️ | Ruente | 1 |
| Bois de Camargo (7) ⚠️ | Camargo | 1 |
| Bois de Piélagos (5) ⚠️ | Piélagos | 1 |
| Bois de Piélagos (6) ⚠️ | Piélagos | 1 |
| Bois de San Vicente de la Barquera (4) ⚠️ | San Vicente de la Barquera | 1 |
| Forêt de Molledo (18) ⚠️ | Molledo | 1 |
| Bois de Alfoz de Lloredo (5) ⚠️ | Alfoz de Lloredo | 1 |
| Forêt de Alfoz de Lloredo (15) ⚠️ | Alfoz de Lloredo | 1 |
| Parc de Liendo ⚠️ | Liendo | 1 |
| Forêt de Soba (67) ⚠️ | Soba | 1 |
| Forêt de Castro-Urdiales (91) ⚠️ | Castro-Urdiales | 1 |
| Bois de Castro-Urdiales (91) ⚠️ | Castro-Urdiales | 1 |
| Bois de Castro-Urdiales (96) ⚠️ | Castro-Urdiales | 1 |
| Forêt de Ribamontán al Monte (5) ⚠️ | Ribamontán al Monte | 1 |
| Bois de Arnuero (3) ⚠️ | Arnuero | 1 |
| Parc de Ribamontán al Monte ⚠️ | Ribamontán al Monte | 1 |
| Bois de Valderredible (5) ⚠️ | Valderredible | 1 |
| Bois de San Roque de Riomiera (5) ⚠️ | San Roque de Riomiera | 1 |
| Bois de San Roque de Riomiera (9) ⚠️ | San Roque de Riomiera | 1 |
| Parc de Colindres (3) ⚠️ | Colindres | 1 |
| Bois de Soba (11) ⚠️ | Soba | 1 |
| Bois de Comillas (6) ⚠️ | Comillas | 1 |
| Bois de San Vicente de la Barquera (10) ⚠️ | San Vicente de la Barquera | 1 |
| Bois de San Vicente de la Barquera (12) ⚠️ | San Vicente de la Barquera | 1 |
| Bois de San Vicente de la Barquera (17) ⚠️ | San Vicente de la Barquera | 1 |
| Bois de San Vicente de la Barquera (19) ⚠️ | San Vicente de la Barquera | 1 |
| Bois de Cabezón de la Sal (4) ⚠️ | Cabezón de la Sal | 1 |
| Forêt de Limpias (3) ⚠️ | Limpias | 1 |
| Parc de Camargo (11) ⚠️ | Camargo | 1 |
| Parc de Santander (55) ⚠️ | Santander | 1 |
| Forêt de Riotuerto (154) ⚠️ | Riotuerto | 1 |
| Forêt de Polanco (14) ⚠️ | Polanco | 1 |
| Bois de Santander (15) ⚠️ | Santander | 1 |
| Parc de Miengo (5) ⚠️ | Miengo | 1 |
| Área Recreativa Playa de Marzán ⚠️ | Miengo | 1 |
| Forêt de Miera (4) ⚠️ | Miera | 1 |
| Bois de Voto (3) ⚠️ | Voto | 1 |
| Bois de Castro-Urdiales (100) ⚠️ | Castro-Urdiales | 1 |
| Bois de Castro-Urdiales (101) ⚠️ | Castro-Urdiales | 1 |
| Bois de Bárcena de Pie de Concha (2) ⚠️ | Bárcena de Pie de Concha | 1 |
| Forêt de Valdeolea (9) ⚠️ | Valdeolea | 1 |
| Bois de Hermandad de Campoo de Suso (4) ⚠️ | Hermandad de Campoo de Suso | 1 |
| Bois de Voto (13) ⚠️ | Voto | 1 |
| Bois de Camargo (10) ⚠️ | Camargo | 1 |
| Bois de Camargo (13) ⚠️ | Camargo | 1 |
| Bois de Camargo (15) ⚠️ | Camargo | 1 |
| Bois de Camargo (18) ⚠️ | Camargo | 1 |
| Bois de Camargo (19) ⚠️ | Camargo | 1 |
| Bois de Camargo (20) ⚠️ | Camargo | 1 |
| Forêt de Reocín (26) ⚠️ | Reocín | 1 |
| Bois de Marina de Cudeyo (2) ⚠️ | Marina de Cudeyo | 1 |
| Bois de Ribamontán al Mar ⚠️ | Ribamontán al Mar | 1 |
| Parc de Laredo (15) ⚠️ | Laredo | 1 |
| Parc de Laredo (18) ⚠️ | Laredo | 1 |
| Forêt de Liendo (4) ⚠️ | Liendo | 1 |
| Bois de Selaya ⚠️ | Selaya | 1 |
| Forêt de Santillana del Mar (8) ⚠️ | Santillana del Mar | 1 |
| Forêt de Santillana del Mar (10) ⚠️ | Santillana del Mar | 1 |
| Bois de Selaya (2) ⚠️ | Selaya | 1 |
| Bois de Selaya (5) ⚠️ | Selaya | 1 |
| Bois de Selaya (7) ⚠️ | Selaya | 1 |
| Bois de San Roque de Riomiera (10) ⚠️ | San Roque de Riomiera | 1 |
| Parque de Cenón ⚠️ | Laredo | 1 |
| Bois de Valle de Villaverde (7) ⚠️ | Valle de Villaverde | 1 |
| Bois de Camaleño (11) ⚠️ | Camaleño | 1 |
| Bois de Camaleño (12) ⚠️ | Camaleño | 1 |
| Bois de Camaleño (14) ⚠️ | Camaleño | 1 |
| Bois de Camaleño (15) ⚠️ | Camaleño | 1 |
| Bois de Camaleño (17) ⚠️ | Camaleño | 1 |
| Parc de Piélagos (19) ⚠️ | Piélagos | 1 |
| Bois de Vega de Liébana (9) ⚠️ | Vega de Liébana | 1 |
| Bois de Potes ⚠️ | Potes | 1 |
| Bois de Camaleño (21) ⚠️ | Camaleño | 1 |
| Forêt de Arredondo (21) ⚠️ | Arredondo | 1 |
| Parc de Ribamontán al Mar (4) ⚠️ | Ribamontán al Mar | 1 |
| Parque El Juego ⚠️ | Ribamontán al Mar | 1 |
| Forêt de Liérganes (32) ⚠️ | Riotuerto | 1 |
| Parque Cotolino ⚠️ | Castro-Urdiales | 1 |
| Forêt de Santa María de Cayón (79) ⚠️ | Santa María de Cayón | 1 |
| Bois de Santa María de Cayón (660) ⚠️ | Santa María de Cayón | 1 |
| Bois de Medio Cudeyo (44) ⚠️ | Medio Cudeyo | 1 |
| Bois de Santa María de Cayón (662) ⚠️ | Santa María de Cayón | 1 |
| Parc de Santander (56) ⚠️ | Santander | 1 |
| Forêt de Valle de Villaverde (42) ⚠️ | Valle de Villaverde | 1 |
| Forêt de Ramales de la Victoria (13) ⚠️ | Ramales de la Victoria | 1 |
| Forêt de Soba (73) ⚠️ | Soba | 1 |
| Forêt de Castañeda (21) ⚠️ | Castañeda | 1 |
| Forêt de Castañeda (22) ⚠️ | Castañeda | 1 |
| Forêt de Soba (79) ⚠️ | Soba | 1 |
| Forêt de Valderredible (67) ⚠️ | Valderredible | 1 |
| Paque Municipal de Sobrellano ⚠️ | Comillas | 1 |
| Bois de Valderredible (13) ⚠️ | Valderredible | 1 |
| Bois de Soba (17) ⚠️ | Soba | 1 |
| Bois de Luena (2) ⚠️ | Luena | 1 |
| Bois de Valderredible (21) ⚠️ | Valderredible | 1 |
| Bois de Valderredible (28) ⚠️ | Valderredible | 1 |
| Bois de Valderredible (31) ⚠️ | Valderredible | 1 |

2 464 parc(s) plus petits qu'une cellule ne sont pas listés : la carte les dessine, mais ils n'offrent aucune cellule.

⚠️ 3686 parc(s) hors de la fenêtre 10–125 cellules (3556 trop petit(s), 130 trop grand(s)) : affichés sur la carte, mais ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| airport | 86 |
| prison | 16 |
| military | 0 |
| **Total déclaré** | **102** |
| dont dans une zone de ce territoire | 96 |

Le jeu de données couvre plus large que le territoire — il est produit à une échelle supérieure. Seules les cellules tombant dans une zone d'ici pèsent sur un pourcentage.

### Zones concernées

| Zone | Cellules exclues |
|---|---:|
| Camargo | 76 |
| Santoña | 16 |
| Valderredible | 4 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
