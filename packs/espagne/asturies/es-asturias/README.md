# Principauté des Asturies

Pack `es-asturias` · version 1.0.0 · grille 200 m · Espagne › Asturies

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 498 715 |
| dont restreintes (aéroport, militaire, prison) | 561 |
| dont sans chemin (aucune voie à moins de 60 m) | 128 222 |
| dont en forêt, sans chemin non plus | 85 627 |
| dont traversées par un cours d'eau, sans chemin non plus | 4 437 |
| Cellules retirées par le masque d'eau | 1 636 |
| Villes | 78 |
| Arrondissements et quartiers | 0 |
| Îles | 0 |
| Parcs | 6 396 |

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

## Villes (78)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Sans chemin | Parcs |
|---|---:|---:|---:|---:|---:|---:|---:|
| Cangas del Narcea | 38 618 | 3 | 38 615 | 0 | **38 615** | 13 784 (36 %) | 129 |
| Tineo | 25 570 | 73 | 25 497 | 0 | **25 497** | 7 311 (29 %) | 1081 |
| Aller | 17 659 | 1 | 17 658 | 0 | **17 658** | 6 027 (34 %) | 74 |
| Valdés | 16 744 | 5 | 16 739 | 0 | **16 739** | 2 725 (16 %) | 472 |
| Allande | 16 003 | 1 | 16 002 | 0 | **16 002** | 6 092 (38 %) | 68 |
| Ibias | 15 582 | 15 | 15 567 | 0 | **15 567** | 6 723 (43 %) | 32 |
| Lena | 14 913 | 4 | 14 909 | 0 | **14 909** | 3 230 (22 %) | 50 |
| Caso | 14 409 | 62 | 14 347 | 0 | **14 347** | 4 400 (31 %) | 71 |
| Somiedo | 13 611 | 27 | 13 584 | 0 | **13 584** | 5 874 (43 %) | 179 |
| Piloña | 13 458 | 5 | 13 453 | 0 | **13 453** | 3 725 (28 %) | 91 |
| Villaviciosa | 12 998 | 172 | 12 826 | 0 | **12 826** | 1 639 (13 %) | 137 |
| Llanes | 12 472 | 2 | 12 470 | 0 | **12 470** | 4 140 (33 %) | 145 |
| Cabrales | 11 267 | 1 | 11 266 | 0 | **11 266** | 4 802 (43 %) | 268 |
| Salas | 10 768 | 35 | 10 733 | 0 | **10 733** | 2 599 (24 %) | 109 |
| Grado | 10 241 | 12 | 10 229 | 0 | **10 229** | 3 993 (39 %) | 48 |
| Cangas de Onís | 10 096 | 44 | 10 052 | 0 | **10 052** | 2 554 (25 %) | 142 |
| Siero | 9 998 | 2 | 9 996 | 469 | **9 527** | 516 (5 %) | 121 |
| Belmonte de Miranda | 9 815 | 30 | 9 785 | 0 | **9 785** | 4 318 (44 %) | 33 |
| Ponga | 9 708 | 0 | 9 708 | 0 | **9 708** | 3 009 (31 %) | 60 |
| Quirós | 9 555 | 8 | 9 547 | 0 | **9 547** | 2 877 (30 %) | 56 |
| Oviedo | 8 840 | 61 | 8 779 | 0 | **8 779** | 995 (11 %) | 469 |
| Gijón | 8 761 | 30 | 8 731 | 0 | **8 731** | 297 (3 %) | 639 |
| Teverga | 8 270 | 1 | 8 269 | 0 | **8 269** | 3 379 (41 %) | 22 |
| Mieres | 6 884 | 35 | 6 849 | 0 | **6 849** | 1 086 (16 %) | 77 |
| Villayón | 6 278 | 44 | 6 234 | 0 | **6 234** | 1 905 (31 %) | 27 |
| Laviana | 6 174 | 7 | 6 167 | 0 | **6 167** | 809 (13 %) | 58 |
| Castropol | 5 965 | 2 | 5 963 | 0 | **5 963** | 576 (10 %) | 42 |
| Parres | 5 965 | 37 | 5 928 | 0 | **5 928** | 1 239 (21 %) | 61 |
| Boal | 5 709 | 79 | 5 630 | 0 | **5 630** | 869 (15 %) | 36 |
| Amieva | 5 414 | 3 | 5 411 | 0 | **5 411** | 2 397 (44 %) | 15 |
| Grandas de Salime | 5 387 | 110 | 5 277 | 0 | **5 277** | 1 453 (28 %) | 48 |
| Llanera | 4 974 | 2 | 4 972 | 8 | **4 964** | 622 (13 %) | 52 |
| Pravia | 4 886 | 45 | 4 841 | 0 | **4 841** | 268 (6 %) | 64 |
| Cudillero | 4 784 | 0 | 4 784 | 0 | **4 784** | 522 (11 %) | 63 |
| Illano | 4 856 | 110 | 4 746 | 0 | **4 746** | 1 465 (31 %) | 24 |
| Colunga | 4 573 | 0 | 4 573 | 0 | **4 573** | 540 (12 %) | 45 |
| Nava | 4 533 | 0 | 4 533 | 0 | **4 533** | 669 (15 %) | 27 |
| Peñamellera Alta | 4 357 | 6 | 4 351 | 0 | **4 351** | 1 917 (44 %) | 20 |
| Degaña | 4 067 | 2 | 4 065 | 0 | **4 065** | 1 314 (32 %) | 19 |
| Ribadesella | 4 007 | 38 | 3 969 | 0 | **3 969** | 745 (19 %) | 95 |
| Peñamellera Baja | 3 965 | 21 | 3 944 | 0 | **3 944** | 1 389 (35 %) | 39 |
| Vegadeo | 3 948 | 5 | 3 943 | 0 | **3 943** | 235 (6 %) | 24 |
| Langreo | 3 948 | 11 | 3 937 | 0 | **3 937** | 207 (5 %) | 120 |
| Taramundi | 3 885 | 0 | 3 885 | 0 | **3 885** | 107 (3 %) | 78 |
| Gozón | 3 870 | 22 | 3 848 | 0 | **3 848** | 472 (12 %) | 35 |
| El Franco | 3 699 | 0 | 3 699 | 0 | **3 699** | 161 (4 %) | 56 |
| Proaza | 3 626 | 0 | 3 626 | 0 | **3 626** | 1 344 (37 %) | 15 |
| Onís | 3 544 | 0 | 3 544 | 0 | **3 544** | 1 203 (34 %) | 69 |
| Villanueva de Oscos | 3 446 | 0 | 3 446 | 0 | **3 446** | 717 (21 %) | 13 |
| Candamo | 3 419 | 35 | 3 384 | 0 | **3 384** | 607 (18 %) | 10 |
| Sobrescobio | 3 283 | 24 | 3 259 | 0 | **3 259** | 951 (29 %) | 16 |
| San Martín de Oscos | 3 193 | 0 | 3 193 | 0 | **3 193** | 1 078 (34 %) | 12 |
| Las Regueras | 3 201 | 17 | 3 184 | 0 | **3 184** | 579 (18 %) | 31 |
| Carreño | 3 162 | 7 | 3 155 | 0 | **3 155** | 239 (8 %) | 33 |
| Tapia de Casariego | 3 110 | 0 | 3 110 | 0 | **3 110** | 83 (3 %) | 21 |
| Coaña | 3 117 | 54 | 3 063 | 0 | **3 063** | 155 (5 %) | 64 |
| Navia | 2 996 | 28 | 2 968 | 0 | **2 968** | 329 (11 %) | 157 |
| Castrillón | 2 620 | 4 | 2 616 | 84 | **2 532** | 76 (3 %) | 40 |
| Samartín del Rei Aurelio | 2 592 | 13 | 2 579 | 0 | **2 579** | 188 (7 %) | 25 |
| Morcín | 2 369 | 26 | 2 343 | 0 | **2 343** | 555 (24 %) | 13 |
| Santa Eulalia de Oscos | 2 233 | 0 | 2 233 | 0 | **2 233** | 393 (18 %) | 18 |
| Riosa | 2 185 | 0 | 2 185 | 0 | **2 185** | 456 (21 %) | 19 |
| Corvera de Asturias | 2 190 | 30 | 2 160 | 0 | **2 160** | 131 (6 %) | 18 |
| Pesoz | 1 829 | 5 | 1 824 | 0 | **1 824** | 448 (25 %) | 5 |
| Cabranes | 1 815 | 0 | 1 815 | 0 | **1 815** | 213 (12 %) | 12 |
| Ribadedeva | 1 673 | 16 | 1 657 | 0 | **1 657** | 359 (22 %) | 16 |
| Soto del Barco | 1 669 | 53 | 1 616 | 0 | **1 616** | 105 (6 %) | 13 |
| Bimenes | 1 543 | 0 | 1 543 | 0 | **1 543** | 148 (10 %) | 10 |
| Yernes y Tameza | 1 493 | 0 | 1 493 | 0 | **1 493** | 833 (56 %) | 8 |
| San Tirso de Abres | 1 476 | 0 | 1 476 | 0 | **1 476** | 20 (1 %) | 23 |
| Sariego | 1 220 | 0 | 1 220 | 0 | **1 220** | 213 (17 %) | 9 |
| Illas | 1 208 | 0 | 1 208 | 0 | **1 208** | 139 (12 %) | 4 |
| Avilés | 1 274 | 81 | 1 193 | 0 | **1 193** | 62 (5 %) | 48 |
| Santo Adriano | 1 069 | 2 | 1 067 | 0 | **1 067** | 309 (29 %) | 7 |
| Ribera de Arriba | 1 034 | 26 | 1 008 | 0 | **1 008** | 215 (21 %) | 13 |
| Caravia | 635 | 1 | 634 | 0 | **634** | 66 (10 %) | 8 |
| Muros de Nalón | 384 | 41 | 343 | 0 | **343** | 21 (6 %) | 4 |
| Noreña | 263 | 0 | 263 | 0 | **263** | 12 (5 %) | 13 |

## Parcs (6396)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Forêt de Cangas del Narcea (123) ⚠️ | Cangas del Narcea | 3 253 |
| Forêt de San Tirso de Abres (15) ⚠️ | San Tirso de Abres | 2 092 |
| Forêt de Valdés (401) ⚠️ | Valdés | 1 769 |
| Forêt de Teverga (15) ⚠️ | Teverga | 1 580 |
| Forêt de Caso (6) ⚠️ | Caso | 1 274 |
| Forêt de Somiedo (19) ⚠️ | Somiedo | 1 215 |
| Forêt de Castrillón (18) ⚠️ | Castrillón | 1 087 |
| Forêt de Lena (17) ⚠️ | Lena | 1 075 |
| Forêt de Cangas del Narcea (116) ⚠️ | Cangas del Narcea | 1 065 |
| Forêt de Proaza ⚠️ | Proaza | 1 039 |
| Forêt de Salas (5) ⚠️ | Salas | 1 009 |
| Forêt de Belmonte de Miranda (2) ⚠️ | Belmonte de Miranda | 1 004 |
| Forêt de Caso (59) ⚠️ | Caso | 973 |
| Forêt de Pravia (7) ⚠️ | Pravia | 834 |
| Bois de Colunga (4) ⚠️ | Colunga | 831 |
| Forêt de Castropol (37) ⚠️ | Castropol | 827 |
| Forêt de Amieva (12) ⚠️ | Amieva | 811 |
| Forêt de Valdés (85) ⚠️ | Valdés | 774 |
| Forêt de Teverga (8) ⚠️ | Teverga | 753 |
| Forêt de Santa Eulalia de Oscos (17) ⚠️ | Santa Eulalia de Oscos | 740 |
| Forêt de Navia (135) ⚠️ | Navia | 717 |
| Forêt de Lena (39) ⚠️ | Lena | 712 |
| Forêt de Degaña (8) ⚠️ | Degaña | 685 |
| Forêt de Parres (13) ⚠️ | Parres | 677 |
| Forêt de Tineo (951) ⚠️ | Tineo | 673 |
| Forêt de Villaviciosa (12) ⚠️ | Villaviciosa | 664 |
| Forêt de Aller (20) ⚠️ | Aller | 664 |
| Forêt de Aller (12) ⚠️ | Aller | 663 |
| Forêt de Lena (10) ⚠️ | Lena | 638 |
| Forêt de Lena (37) ⚠️ | Lena | 615 |
| Forêt de Candamo (8) ⚠️ | Candamo | 607 |
| Forêt de Boal (18) ⚠️ | Boal | 593 |
| Forêt de Villaviciosa (46) ⚠️ | Villaviciosa | 582 |
| Forêt de Ibias (15) ⚠️ | Ibias | 579 |
| Forêt de Pesoz (2) ⚠️ | Pesoz | 576 |
| Forêt de Taramundi (62) ⚠️ | Taramundi | 574 |
| Forêt de Cangas del Narcea (122) ⚠️ | Cangas del Narcea | 564 |
| Forêt de Cangas del Narcea (76) ⚠️ | Cangas del Narcea | 547 |
| Forêt de Lena (8) ⚠️ | Lena | 544 |
| Forêt de Langreo (24) ⚠️ | Langreo | 537 |
| Forêt de Taramundi (15) ⚠️ | Taramundi | 504 |
| Forêt de Sobrescobio (6) ⚠️ | Sobrescobio | 494 |
| Forêt de Riosa (3) ⚠️ | Riosa | 491 |
| Forêt de Grado (34) ⚠️ | Grado | 491 |
| Forêt de Colunga (13) ⚠️ | Colunga | 490 |
| Forêt de Aller (34) ⚠️ | Aller | 486 |
| Forêt de Pravia (24) ⚠️ | Pravia | 470 |
| Forêt de Aller (56) ⚠️ | Aller | 443 |
| Forêt de Boal (24) ⚠️ | Boal | 434 |
| Forêt de Tapia de Casariego (12) ⚠️ | Tapia de Casariego | 422 |
| Forêt de Tapia de Casariego (3) ⚠️ | Tapia de Casariego | 421 |
| Forêt de Lena (25) ⚠️ | Lena | 413 |
| Forêt de Allande (29) ⚠️ | Allande | 411 |
| Forêt de Cabrales (215) ⚠️ | Cabrales | 408 |
| Forêt de Grado (7) ⚠️ | Grado | 406 |
| Forêt de Quirós (40) ⚠️ | Quirós | 385 |
| Forêt de Salas (16) ⚠️ | Salas | 383 |
| Forêt de Ponga (28) ⚠️ | Ponga | 383 |
| Bois de Cangas de Onís ⚠️ | Cangas de Onís | 381 |
| Forêt de Corvera de Asturias (3) ⚠️ | Corvera de Asturias | 372 |
| Forêt de Caso (52) ⚠️ | Caso | 369 |
| Forêt de Salas (12) ⚠️ | Salas | 368 |
| Forêt de Allande (3) ⚠️ | Allande | 363 |
| Forêt de Aller (44) ⚠️ | Aller | 356 |
| Bois de Oviedo (3) ⚠️ | Oviedo | 354 |
| Forêt de Tineo (952) ⚠️ | Tineo | 354 |
| Forêt de Villaviciosa (35) ⚠️ | Villaviciosa | 351 |
| Forêt de Tineo (77) ⚠️ | Tineo | 343 |
| Forêt de Mieres (9) ⚠️ | Mieres | 340 |
| Forêt de El Franco (11) ⚠️ | El Franco | 335 |
| Forêt de Siero (55) ⚠️ | Siero | 335 |
| Forêt de Degaña (17) ⚠️ | Degaña | 331 |
| Forêt de Valdés (400) ⚠️ | Navia | 331 |
| Forêt de Llanes (38) ⚠️ | Llanes | 331 |
| Forêt de Mieres ⚠️ | Mieres | 330 |
| Forêt de Valdés (50) ⚠️ | Valdés | 330 |
| Forêt de Aller (25) ⚠️ | Aller | 328 |
| Forêt de Candamo (2) ⚠️ | Candamo | 326 |
| Forêt de Ponga (45) ⚠️ | Ponga | 322 |
| Forêt de Cangas del Narcea (97) ⚠️ | Cangas del Narcea | 318 |
| Forêt de Piloña (33) ⚠️ | Piloña | 315 |
| Forêt de Quirós (28) ⚠️ | Quirós | 315 |
| Forêt de Aller (14) ⚠️ | Aller | 311 |
| Forêt de Cangas del Narcea (111) ⚠️ | Cangas del Narcea | 308 |
| Forêt de Cangas del Narcea (53) ⚠️ | Cangas del Narcea | 306 |
| Forêt de Colunga ⚠️ | Colunga | 303 |
| Bois de Tineo ⚠️ | Tineo | 303 |
| Forêt de Caso (58) ⚠️ | Caso | 303 |
| Forêt de Castropol (36) ⚠️ | Castropol | 301 |
| Bois de Caso (6) ⚠️ | Caso | 301 |
| Forêt de Cudillero (3) ⚠️ | Cudillero | 299 |
| Forêt de Ponga (51) ⚠️ | Ponga | 299 |
| Forêt de Cangas del Narcea (84) ⚠️ | Cangas del Narcea | 298 |
| Forêt de Laviana (36) ⚠️ | Laviana | 296 |
| Forêt de Allande (41) ⚠️ | Allande | 290 |
| Forêt de Parres (6) ⚠️ | Parres | 288 |
| Forêt de El Franco (17) ⚠️ | El Franco | 286 |
| Forêt de Ponga (49) ⚠️ | Ponga | 286 |
| Forêt de Carreño (21) ⚠️ | Gijón | 286 |
| Forêt de Peñamellera Alta (5) ⚠️ | Peñamellera Alta | 285 |
| Forêt de Tineo (29) ⚠️ | Tineo | 284 |
| Forêt de Caso (53) ⚠️ | Caso | 284 |
| Forêt de Caso (8) ⚠️ | Caso | 280 |
| Forêt de Somiedo (15) ⚠️ | Somiedo | 280 |
| Forêt de Valdés (402) ⚠️ | Valdés | 280 |
| Forêt de Vegadeo (11) ⚠️ | Vegadeo | 279 |
| Forêt de Llanes (21) ⚠️ | Llanes | 279 |
| Forêt de Taramundi (59) ⚠️ | Taramundi | 279 |
| Forêt de Grandas de Salime (2) ⚠️ | Grandas de Salime | 278 |
| Forêt de Illas ⚠️ | Illas | 277 |
| Forêt de Colunga (31) ⚠️ | Colunga | 277 |
| Forêt de Ponga (50) ⚠️ | Ponga | 276 |
| Forêt de Llanes (40) ⚠️ | Llanes | 276 |
| Forêt de Somiedo (21) ⚠️ | Somiedo | 275 |
| Forêt de Ibias (31) ⚠️ | Ibias | 275 |
| Bois de Llanes (39) ⚠️ | Llanes | 274 |
| Forêt de Tineo (95) ⚠️ | Tineo | 271 |
| Forêt de Salas (38) ⚠️ | Salas | 270 |
| Forêt de Cangas de Onís (21) ⚠️ | Cangas de Onís | 265 |
| Forêt de Laviana (20) ⚠️ | Laviana | 265 |
| Forêt de Samartín del Rei Aurelio (4) ⚠️ | Samartín del Rei Aurelio | 263 |
| Forêt de Caso (39) ⚠️ | Caso | 260 |
| Forêt de Gozón (16) ⚠️ | Gozón | 260 |
| Forêt de Castropol (38) ⚠️ | Castropol | 260 |
| Forêt de Laviana (38) ⚠️ | Laviana | 258 |
| Forêt de Somiedo (27) ⚠️ | Somiedo | 257 |
| Forêt de Llanera (14) ⚠️ | Llanera | 251 |
| Forêt de Amieva (9) ⚠️ | Amieva | 251 |
| Forêt de Villaviciosa (16) ⚠️ | Villaviciosa | 249 |
| Forêt de Castropol (6) ⚠️ | Castropol | 248 |
| El Monte Llaímu ⚠️ | Sobrescobio | 246 |
| Forêt de Coaña (41) ⚠️ | Coaña | 246 |
| Forêt de Aller (2) ⚠️ | Aller | 245 |
| Forêt de Allande (26) ⚠️ | Allande | 245 |
| Forêt de Cangas del Narcea (20) ⚠️ | Cangas del Narcea | 243 |
| Forêt de Cangas del Narcea (95) ⚠️ | Cangas del Narcea | 242 |
| Forêt de Valdés (66) ⚠️ | Valdés | 242 |
| Forêt de Quirós (18) ⚠️ | Quirós | 241 |
| Forêt de Aller (49) ⚠️ | Aller | 241 |
| Forêt de Belmonte de Miranda (3) ⚠️ | Belmonte de Miranda | 240 |
| Forêt de Valdés (53) ⚠️ | Valdés | 240 |
| Forêt de Gijón (45) ⚠️ | Gijón | 239 |
| Forêt de Villanueva de Oscos (7) ⚠️ | Villanueva de Oscos | 237 |
| Forêt de Cangas del Narcea (32) ⚠️ | Cangas del Narcea | 234 |
| Forêt de Tineo (34) ⚠️ | Tineo | 234 |
| Forêt de Cangas del Narcea (41) ⚠️ | Cangas del Narcea | 234 |
| Forêt de Ribadesella (17) ⚠️ | Ribadesella | 234 |
| Bois de Allande (24) ⚠️ | Allande | 233 |
| Forêt de Aller (15) ⚠️ | Aller | 230 |
| Forêt de Grandas de Salime (29) ⚠️ | Grandas de Salime | 230 |
| Forêt de Villaviciosa (22) ⚠️ | Villaviciosa | 229 |
| Forêt de Vegadeo (18) ⚠️ | Vegadeo | 227 |
| Forêt de Piloña (28) ⚠️ | Piloña | 226 |
| Forêt de Carreño (12) ⚠️ | Carreño | 224 |
| Forêt de Castrillón (15) ⚠️ | Castrillón | 224 |
| Forêt de Piloña (58) ⚠️ | Piloña | 222 |
| Bois de Santo Adriano (2) ⚠️ | Santo Adriano | 222 |
| Forêt de Corvera de Asturias (5) ⚠️ | Corvera de Asturias | 220 |
| Forêt de Cangas del Narcea (28) ⚠️ | Cangas del Narcea | 219 |
| Forêt de Pravia (29) ⚠️ | Pravia | 219 |
| Forêt de Cangas de Onís (29) ⚠️ | Cangas de Onís | 218 |
| Forêt de Ponga (10) ⚠️ | Ponga | 217 |
| Forêt de Peñamellera Alta (7) ⚠️ | Peñamellera Alta | 217 |
| Forêt de Caso (33) ⚠️ | Caso | 216 |
| Forêt de Quirós (34) ⚠️ | Quirós | 216 |
| Forêt de Cudillero (18) ⚠️ | Cudillero | 215 |
| Forêt de Ponga (13) ⚠️ | Ponga | 214 |
| Forêt de Caso (64) ⚠️ | Caso | 214 |
| Forêt de Quirós (41) ⚠️ | Quirós | 212 |
| Forêt de Castrillón (5) ⚠️ | Castrillón | 211 |
| Forêt de Cabranes (8) ⚠️ | Cabranes | 211 |
| Forêt de Quirós (7) ⚠️ | Quirós | 208 |
| Forêt de Llanera (10) ⚠️ | Llanera | 208 |
| Forêt de Taramundi (21) ⚠️ | Taramundi | 208 |
| Forêt de Pravia (55) ⚠️ | Pravia | 208 |
| Forêt de Laviana (15) ⚠️ | Laviana | 207 |
| Forêt de Langreo (23) ⚠️ | Langreo | 207 |
| Forêt de Tineo (110) ⚠️ | Tineo | 207 |
| Forêt de Piloña (77) ⚠️ | Piloña | 207 |
| Forêt de Cangas del Narcea (46) ⚠️ | Cangas del Narcea | 206 |
| Forêt de Aller (42) ⚠️ | Aller | 205 |
| Forêt de Ponga (52) ⚠️ | Ponga | 205 |
| Forêt de Lena (7) ⚠️ | Lena | 204 |
| Forêt de Caso (57) ⚠️ | Caso | 203 |
| Forêt de Gijón (49) ⚠️ | Gijón | 202 |
| Forêt de Lena (30) ⚠️ | Lena | 202 |
| Forêt de Piloña (27) ⚠️ | Piloña | 201 |
| Forêt de Onís (69) ⚠️ | Onís | 201 |
| Forêt de Tapia de Casariego (11) ⚠️ | Tapia de Casariego | 199 |
| Forêt de Valdés (64) ⚠️ | Valdés | 199 |
| Forêt de Cangas del Narcea (50) ⚠️ | Cangas del Narcea | 198 |
| Forêt de Peñamellera Baja (17) ⚠️ | Peñamellera Baja | 196 |
| Forêt de Villaviciosa (18) ⚠️ | Villaviciosa | 195 |
| Forêt de Aller (47) ⚠️ | Aller | 194 |
| Forêt de Villaviciosa (65) ⚠️ | Villaviciosa | 194 |
| Forêt de Muros de Nalón (2) ⚠️ | Muros de Nalón | 194 |
| Forêt de Vegadeo (9) ⚠️ | Vegadeo | 193 |
| Forêt de Gijón (46) ⚠️ | Gijón | 193 |
| Forêt de Cudillero (46) ⚠️ | Cudillero | 191 |
| Forêt de Caso (62) ⚠️ | Caso | 190 |
| Forêt de Quirós (26) ⚠️ | Quirós | 189 |
| Forêt de Cangas de Onís (35) ⚠️ | Cangas de Onís | 189 |
| Forêt de Villaviciosa (117) ⚠️ | Villaviciosa | 189 |
| Forêt de Tapia de Casariego (5) ⚠️ | Tapia de Casariego | 188 |
| Forêt de Cangas del Narcea (7) ⚠️ | Cangas del Narcea | 187 |
| Forêt de Pravia (23) ⚠️ | Pravia | 186 |
| Forêt de Taramundi (18) ⚠️ | Taramundi | 186 |
| Forêt de Caravia ⚠️ | Caravia | 186 |
| Forêt de Villaviciosa (58) ⚠️ | Villaviciosa | 186 |
| Forêt de Somiedo (10) ⚠️ | Somiedo | 184 |
| Forêt de Grado (22) ⚠️ | Grado | 183 |
| Forêt de Somiedo (33) ⚠️ | Somiedo | 183 |
| Forêt de Caso (26) ⚠️ | Caso | 181 |
| Forêt de Caso (61) ⚠️ | Caso | 180 |
| Forêt de Cangas de Onís (130) ⚠️ | Cangas de Onís | 179 |
| Forêt de Aller (46) ⚠️ | Aller | 178 |
| Forêt de Boal (6) ⚠️ | Boal | 175 |
| Forêt de Allande (14) ⚠️ | Allande | 174 |
| Forêt de Cabrales (221) ⚠️ | Cabrales | 174 |
| Forêt de Grandas de Salime (12) ⚠️ | Grandas de Salime | 172 |
| Forêt de Morcín ⚠️ | Morcín | 172 |
| Forêt de Piloña (69) ⚠️ | Piloña | 172 |
| Forêt de Langreo (28) ⚠️ | Langreo | 171 |
| Forêt de Pravia (2) ⚠️ | Pravia | 170 |
| Forêt de Corvera de Asturias ⚠️ | Corvera de Asturias | 170 |
| Forêt de Sobrescobio (4) ⚠️ | Sobrescobio | 170 |
| Forêt de Carreño (3) ⚠️ | Carreño | 170 |
| Forêt de Colunga (6) ⚠️ | Colunga | 170 |
| Forêt de Soto del Barco (4) ⚠️ | Soto del Barco | 170 |
| Forêt de Cangas del Narcea (99) ⚠️ | Cangas del Narcea | 170 |
| Forêt de Illano ⚠️ | Illano | 169 |
| Forêt de Oviedo (74) ⚠️ | Oviedo | 168 |
| Forêt de Villaviciosa (36) ⚠️ | Villaviciosa | 166 |
| Forêt de Ribadedeva (15) ⚠️ | Ribadedeva | 166 |
| Forêt de Siero (29) ⚠️ | Siero | 164 |
| Forêt de Cangas del Narcea (115) ⚠️ | Cangas del Narcea | 163 |
| Forêt de Cudillero (8) ⚠️ | Cudillero | 162 |
| Forêt de Las Regueras (7) ⚠️ | Las Regueras | 162 |
| Forêt de Parres (7) ⚠️ | Parres | 162 |
| Forêt de Valdés (29) ⚠️ | Valdés | 162 |
| Forêt de Illano (18) ⚠️ | Illano | 162 |
| Forêt de Piloña (61) ⚠️ | Piloña | 161 |
| Forêt de Ibias (26) ⚠️ | Ibias | 161 |
| Forêt de Aller (60) ⚠️ | Aller | 161 |
| Forêt de Degaña (10) ⚠️ | Degaña | 160 |
| Forêt de Coaña (6) ⚠️ | Coaña | 160 |
| Forêt de Langreo (20) ⚠️ | Langreo | 160 |
| Serruca ⚠️ | Las Regueras | 160 |
| Forêt de Gozón (13) ⚠️ | Gozón | 160 |
| Forêt de Castropol (35) ⚠️ | Castropol | 160 |
| Forêt de Coaña (9) ⚠️ | Coaña | 159 |
| Forêt de Villaviciosa (7) ⚠️ | Villaviciosa | 158 |
| Forêt de Laviana (23) ⚠️ | Laviana | 158 |
| Forêt de Piloña (55) ⚠️ | Piloña | 158 |
| Forêt de Mieres (6) ⚠️ | Mieres | 157 |
| Forêt de Candamo (5) ⚠️ | Candamo | 157 |
| Forêt de Aller (3) ⚠️ | Aller | 156 |
| Forêt de San Martín de Oscos (7) ⚠️ | San Martín de Oscos | 156 |
| Forêt de Valdés (65) ⚠️ | Valdés | 156 |
| Forêt de Ponga (20) ⚠️ | Ponga | 155 |
| Forêt de Tineo (68) ⚠️ | Tineo | 155 |
| Forêt de Aller (51) ⚠️ | Aller | 155 |
| Forêt de Piloña (17) ⚠️ | Piloña | 154 |
| Forêt de Villaviciosa (48) ⚠️ | Villaviciosa | 154 |
| Forêt de Piloña (80) ⚠️ | Piloña | 154 |
| Forêt de Villaviciosa (19) ⚠️ | Villaviciosa | 153 |
| Forêt de Mieres (19) ⚠️ | Mieres | 153 |
| Forêt de Villaviciosa (118) ⚠️ | Villaviciosa | 153 |
| Forêt de Degaña (15) ⚠️ | Degaña | 152 |
| Forêt de Cangas del Narcea (93) ⚠️ | Cangas del Narcea | 151 |
| Forêt de Somiedo (37) ⚠️ | Somiedo | 151 |
| Forêt de Cangas del Narcea (61) ⚠️ | Cangas del Narcea | 150 |
| Forêt de Aller (55) ⚠️ | Aller | 150 |
| Forêt de Ibias (32) ⚠️ | Ibias | 150 |
| Forêt de Coaña (2) ⚠️ | Coaña | 149 |
| Forêt de Valdés (31) ⚠️ | Valdés | 149 |
| Forêt de Quirós (21) ⚠️ | Quirós | 148 |
| Forêt de Candamo (4) ⚠️ | Candamo | 147 |
| Forêt de Cangas del Narcea (40) ⚠️ | Cangas del Narcea | 146 |
| Forêt de Allande (20) ⚠️ | Allande | 146 |
| Forêt de Ponga (48) ⚠️ | Ponga | 145 |
| Forêt de Nava (6) ⚠️ | Nava | 144 |
| Forêt de Tineo (36) ⚠️ | Tineo | 144 |
| Forêt de Aller (27) ⚠️ | Aller | 144 |
| Forêt de Illano (2) ⚠️ | Illano | 143 |
| Forêt de Pravia (8) ⚠️ | Pravia | 143 |
| Forêt de Gozón (7) ⚠️ | Gozón | 143 |
| Forêt de Cangas del Narcea (12) ⚠️ | Cangas del Narcea | 142 |
| Forêt de Vegadeo (8) ⚠️ | Vegadeo | 142 |
| Forêt de Ibias (19) ⚠️ | Ibias | 142 |
| Forêt de Tineo (30) ⚠️ | Tineo | 140 |
| Forêt de Lena (9) ⚠️ | Lena | 139 |
| Forêt de Aller (13) ⚠️ | Aller | 139 |
| Forêt de Boal (15) ⚠️ | Boal | 139 |
| Forêt de Boal ⚠️ | Boal | 138 |
| Forêt de El Franco (4) ⚠️ | El Franco | 138 |
| Forêt de Samartín del Rei Aurelio (3) ⚠️ | Samartín del Rei Aurelio | 138 |
| Forêt de Quirós (14) ⚠️ | Quirós | 138 |
| Forêt de Proaza (2) ⚠️ | Proaza | 138 |
| Forêt de Caso (50) ⚠️ | Caso | 138 |
| Forêt de Colunga (32) ⚠️ | Colunga | 138 |
| Forêt de Ponga (54) ⚠️ | Ponga | 138 |
| Forêt de Degaña (21) ⚠️ | Degaña | 138 |
| Forêt de Coaña ⚠️ | Coaña | 137 |
| Forêt de Tineo (44) ⚠️ | Tineo | 137 |
| Forêt de Villaviciosa (28) ⚠️ | Villaviciosa | 137 |
| Forêt de Boal (23) ⚠️ | Boal | 137 |
| Forêt de Allande (39) ⚠️ | Allande | 137 |
| Forêt de Pravia (35) ⚠️ | Pravia | 136 |
| Forêt de Quirós (3) ⚠️ | Quirós | 135 |
| Forêt de Illano (4) ⚠️ | Illano | 135 |
| Forêt de Quirós (30) ⚠️ | Quirós | 135 |
| Forêt de Cangas del Narcea (91) ⚠️ | Cangas del Narcea | 135 |
| Forêt de Langreo (11) ⚠️ | Langreo | 134 |
| Forêt de Mieres (21) ⚠️ | Mieres | 134 |
| Forêt de Siero (17) ⚠️ | Siero | 133 |
| Forêt de Laviana (19) ⚠️ | Laviana | 133 |
| Forêt de Villaviciosa (61) ⚠️ | Villaviciosa | 133 |
| Forêt de Grandas de Salime (34) ⚠️ | Grandas de Salime | 133 |
| Bois de Tineo (121) ⚠️ | Tineo | 133 |
| Forêt de Siero (11) ⚠️ | Siero | 132 |
| Forêt de Cangas del Narcea (43) ⚠️ | Cangas del Narcea | 132 |
| Forêt de Somiedo (28) ⚠️ | Somiedo | 132 |
| Forêt de Oviedo (44) ⚠️ | Oviedo | 132 |
| Forêt de Cangas de Onís (126) ⚠️ | Cangas de Onís | 132 |
| Forêt de Siero (4) ⚠️ | Siero | 131 |
| Forêt de Quirós (8) ⚠️ | Quirós | 131 |
| Forêt de Lena (16) ⚠️ | Lena | 131 |
| Forêt de Ponga (32) ⚠️ | Ponga | 131 |
| Forêt de Llanes (28) ⚠️ | Llanes | 131 |
| Forêt de Gijón (53) ⚠️ | Gijón | 131 |
| Bois de Oviedo (2) ⚠️ | Oviedo | 130 |
| Forêt de Cudillero (31) ⚠️ | Cudillero | 130 |
| Forêt de Cangas del Narcea (112) ⚠️ | Cangas del Narcea | 130 |
| Forêt de Ponga (53) ⚠️ | Ponga | 130 |
| Forêt de Ponga (56) ⚠️ | Ponga | 130 |
| Forêt de Onís ⚠️ | Onís | 129 |
| Forêt de Salas (17) ⚠️ | Salas | 128 |
| Forêt de Peñamellera Baja (12) ⚠️ | Peñamellera Baja | 128 |
| Forêt de Ibias (18) ⚠️ | Ibias | 128 |
| Forêt de Belmonte de Miranda (15) ⚠️ | Belmonte de Miranda | 128 |
| Forêt de Nava (16) ⚠️ | Nava | 128 |
| Forêt de Lena (29) ⚠️ | Lena | 128 |
| Forêt de Mieres (25) ⚠️ | Mieres | 127 |
| Forêt de Tineo (48) ⚠️ | Tineo | 126 |
| Forêt de Allande (19) ⚠️ | Allande | 126 |
| Forêt de Nava (18) ⚠️ | Nava | 126 |
| Forêt de Gijón (20) | Gijón | 125 |
| Forêt de Cangas del Narcea (10) | Cangas del Narcea | 125 |
| Forêt de Valdés (404) | Valdés | 125 |
| Forêt de Valdés (17) | Valdés | 124 |
| Forêt de Mieres (13) | Mieres | 124 |
| Forêt de Villayón (9) | Villayón | 124 |
| Forêt de Langreo (16) | Langreo | 123 |
| Forêt de Illano (13) | Illano | 123 |
| Forêt de Lena (26) | Lena | 123 |
| Forêt de Langreo | Langreo | 122 |
| Forêt de Santo Adriano (2) | Santo Adriano | 122 |
| Forêt de Villayón (18) | Villayón | 121 |
| Forêt de Sobrescobio | Sobrescobio | 120 |
| Forêt de Pravia (3) | Pravia | 120 |
| Forêt de Ponga (38) | Ponga | 120 |
| Forêt de Salas | Salas | 119 |
| Forêt de Valdés (26) | Valdés | 119 |
| Forêt de Ribadesella (7) | Ribadesella | 119 |
| Forêt de Pravia (4) | Pravia | 117 |
| Forêt de Allande (9) | Allande | 117 |
| Forêt de Somiedo (22) | Somiedo | 116 |
| Forêt de Tineo (21) | Tineo | 115 |
| Forêt de El Franco (16) | El Franco | 115 |
| Forêt de Pravia (27) | Pravia | 114 |
| Forêt de Villaviciosa (20) | Villaviciosa | 113 |
| Forêt de Salas (23) | Salas | 112 |
| Forêt de Valdés (45) | Valdés | 112 |
| Forêt de Cangas del Narcea (22) | Cangas del Narcea | 111 |
| Forêt de Allande (42) | Allande | 111 |
| Forêt de Aller (31) | Aller | 110 |
| Forêt de Boal (20) | Boal | 110 |
| Forêt de Proaza (4) | Proaza | 110 |
| Forêt de El Franco (19) | El Franco | 110 |
| Forêt de Tineo (51) | Tineo | 109 |
| Forêt de Ibias (20) | Ibias | 109 |
| Forêt de Sobrescobio (10) | Sobrescobio | 109 |
| Forêt de Villaviciosa (119) | Villaviciosa | 109 |
| Forêt de Tineo (957) | Tineo | 109 |
| Forêt de Oviedo (20) | Oviedo | 108 |
| Forêt de Villaviciosa (60) | Villaviciosa | 108 |
| Forêt de Oviedo (50) | Oviedo | 108 |
| Forêt de Amieva (2) | Amieva | 107 |
| Forêt de El Franco (6) | El Franco | 107 |
| Forêt de Morcín (7) | Morcín | 107 |
| Forêt de Belmonte de Miranda (26) | Belmonte de Miranda | 107 |
| Forêt de Castrillón (14) | Castrillón | 107 |
| Forêt de Llanes | Llanes | 106 |
| Forêt de Coaña (7) | Coaña | 106 |
| Sorribios | Cabrales | 106 |
| Forêt de Quirós (5) | Quirós | 105 |
| Forêt de Tineo (99) | Tineo | 105 |
| Forêt de Peñamellera Baja (6) | Peñamellera Baja | 104 |
| Forêt de Nava (9) | Nava | 104 |
| Forêt de Quirós (25) | Quirós | 104 |
| Forêt de Llanes (22) | Llanes | 104 |
| Forêt de Oviedo (10) | Oviedo | 103 |
| Forêt de Laviana (26) | Laviana | 103 |
| Forêt de Tineo (87) | Tineo | 103 |
| Forêt de Salas (11) | Salas | 102 |
| Forêt de Ponga (25) | Ponga | 102 |
| Forêt de Villaviciosa (59) | Villaviciosa | 102 |
| Forêt de Pesoz (5) | Pesoz | 102 |
| Forêt de Amieva (11) | Amieva | 102 |
| Forêt de Mieres (8) | Mieres | 101 |
| Forêt de Cangas de Onís (11) | Cangas de Onís | 101 |
| Forêt de Villayón (16) | Villayón | 101 |
| Forêt de Villaviciosa (45) | Villaviciosa | 101 |
| Forêt de Cangas de Onís (39) | Cangas de Onís | 101 |
| Forêt de El Franco (41) | El Franco | 101 |
| Forêt de Cangas de Onís (17) | Cangas de Onís | 100 |
| Forêt de Taramundi (17) | Taramundi | 100 |
| Forêt de Navia (136) | Navia | 100 |
| Forêt de Caso (35) | Caso | 99 |
| Forêt de Illano (14) | Illano | 99 |
| Forêt de Samartín del Rei Aurelio (8) | Samartín del Rei Aurelio | 99 |
| Monte de UP Barandon | Villayón | 98 |
| Forêt de Tineo (109) | Tineo | 98 |
| Forêt de Cangas del Narcea (11) | Cangas del Narcea | 97 |
| Forêt de Grado (19) | Grado | 97 |
| Forêt de Illano (12) | Illano | 97 |
| Forêt de Quirós (9) | Quirós | 96 |
| Forêt de Lena (6) | Lena | 96 |
| Forêt de San Martín de Oscos (2) | San Martín de Oscos | 96 |
| Forêt de Degaña (19) | Degaña | 96 |
| Forêt de Vegadeo (21) | Vegadeo | 96 |
| Forêt de Ponga (12) | Ponga | 95 |
| Forêt de Valdés (23) | Valdés | 95 |
| Forêt de Aller (18) | Aller | 95 |
| Forêt de Teverga (9) | Teverga | 95 |
| Forêt de Grado (31) | Grado | 95 |
| Forêt de Tineo (97) | Tineo | 94 |
| Forêt de Siero (35) | Siero | 94 |
| Bois de Llanes (32) | Llanes | 94 |
| Forêt de Grado (2) | Grado | 93 |
| Forêt de Mieres (20) | Mieres | 93 |
| Forêt de Tineo (89) | Tineo | 93 |
| Forêt de Cangas del Narcea (98) | Cangas del Narcea | 93 |
| Forêt de Llanes (25) | Llanes | 93 |
| Forêt de Villayón | Villayón | 92 |
| Forêt de Nava (8) | Nava | 92 |
| Forêt de Aller (22) | Aller | 92 |
| Forêt de Illano (22) | Illano | 92 |
| Forêt de Taramundi (14) | Taramundi | 91 |
| Forêt de Tineo (58) | Tineo | 91 |
| Carretera de San Martín de Luiña a Brieves | Cudillero | 91 |
| Forêt de Pravia | Pravia | 90 |
| Forêt de Illano (3) | Illano | 90 |
| Forêt de Pravia (13) | Pravia | 90 |
| Forêt de Cangas del Narcea (85) | Cangas del Narcea | 90 |
| Forêt de Villayón (4) | Villayón | 89 |
| Forêt de Somiedo (14) | Somiedo | 89 |
| Forêt de Quirós (16) | Quirós | 89 |
| Forêt de Cangas del Narcea (71) | Cangas del Narcea | 89 |
| Forêt de Belmonte de Miranda (18) | Belmonte de Miranda | 89 |
| Forêt de Piloña (62) | Piloña | 89 |
| Forêt de Lena (23) | Lena | 89 |
| Forêt de Belmonte de Miranda (27) | Belmonte de Miranda | 89 |
| Forêt de Proaza (12) | Proaza | 89 |
| Forêt de Caso (22) | Caso | 88 |
| Forêt de El Franco (13) | El Franco | 88 |
| Forêt de Peñamellera Baja (18) | Peñamellera Baja | 88 |
| Forêt de San Tirso de Abres (6) | San Tirso de Abres | 88 |
| Forêt de Cabrales (8) | Cabrales | 88 |
| Forêt de Caso (54) | Caso | 88 |
| Forêt de Bimenes | Bimenes | 87 |
| Forêt de Siero (28) | Siero | 87 |
| Forêt de Samartín del Rei Aurelio | Samartín del Rei Aurelio | 86 |
| Forêt de Teverga (2) | Teverga | 86 |
| Forêt de Nava (5) | Nava | 86 |
| Forêt de Allande (15) | Allande | 85 |
| Forêt de Boal (19) | Boal | 85 |
| Forêt de Piloña (40) | Piloña | 85 |
| Forêt de Piloña (41) | Piloña | 85 |
| Forêt de Belmonte de Miranda (29) | Belmonte de Miranda | 85 |
| Forêt de Valdés (403) | Valdés | 85 |
| Forêt de Llanes (41) | Llanes | 85 |
| Forêt de Belmonte de Miranda (13) | Belmonte de Miranda | 84 |
| Forêt de Gozón (9) | Gozón | 84 |
| Forêt de Valdés (9) | Valdés | 83 |
| Forêt de Mieres (5) | Mieres | 83 |
| Forêt de Parres (12) | Parres | 83 |
| Forêt de Piloña (63) | Piloña | 83 |
| Forêt de Parres (24) | Parres | 83 |
| Forêt de Cabrales (226) | Cabrales | 83 |
| Forêt de Llanes (6) | Llanes | 82 |
| Forêt de Cangas del Narcea (25) | Cangas del Narcea | 82 |
| Forêt de Boal (5) | Boal | 82 |
| Forêt de Cangas del Narcea (38) | Cangas del Narcea | 82 |
| Forêt de Peñamellera Alta (8) | Peñamellera Alta | 82 |
| Forêt de Valdés (11) | Valdés | 81 |
| Forêt de Llanera (11) | Llanera | 81 |
| Bois de Allande | Allande | 81 |
| Forêt de Valdés (47) | Valdés | 81 |
| Forêt de Llanera (19) | Llanera | 81 |
| Forêt de Peñamellera Alta (19) | Peñamellera Alta | 81 |
| Forêt de Ponga (7) | Ponga | 80 |
| Forêt de Piloña (15) | Piloña | 80 |
| Forêt de Morcín (2) | Morcín | 80 |
| Forêt de Caso (11) | Caso | 80 |
| Forêt de Laviana (7) | Laviana | 80 |
| Forêt de Oviedo (28) | Oviedo | 80 |
| Forêt de Cangas del Narcea (70) | Cangas del Narcea | 80 |
| Forêt de Villaviciosa (56) | Villaviciosa | 80 |
| Forêt de Tapia de Casariego (8) | Tapia de Casariego | 79 |
| Forêt de Gijón (39) | Gijón | 79 |
| Forêt de Cangas del Narcea (78) | Cangas del Narcea | 79 |
| Forêt de Mieres (22) | Mieres | 79 |
| Forêt de Nava (17) | Nava | 79 |
| Forêt de Samartín del Rei Aurelio (9) | Samartín del Rei Aurelio | 79 |
| Forêt de Bimenes (6) | Bimenes | 78 |
| Forêt de Illano (21) | Illano | 78 |
| Forêt de Cangas del Narcea (15) | Cangas del Narcea | 77 |
| Forêt de Salas (6) | Salas | 77 |
| Forêt de Cangas del Narcea (27) | Cangas del Narcea | 77 |
| Forêt de Cangas del Narcea (33) | Cangas del Narcea | 77 |
| Forêt de Mieres (14) | Mieres | 77 |
| Forêt de Piloña (57) | Piloña | 77 |
| Forêt de Oviedo (12) | Oviedo | 76 |
| Forêt de San Martín de Oscos (3) | San Martín de Oscos | 76 |
| Forêt de Caso (21) | Caso | 76 |
| Forêt de Allande (7) | Allande | 75 |
| Forêt de Villanueva de Oscos (9) | Villanueva de Oscos | 75 |
| Forêt de Ribadesella (72) | Ribadesella | 75 |
| Forêt de Cangas del Narcea (6) | Cangas del Narcea | 74 |
| Forêt de Taramundi (7) | Taramundi | 74 |
| Forêt de El Franco (8) | El Franco | 74 |
| Forêt de Tineo (61) | Tineo | 74 |
| Forêt de Valdés (70) | Valdés | 74 |
| Forêt de Villaviciosa (72) | Villaviciosa | 74 |
| Forêt de Ibias (5) | Ibias | 73 |
| Forêt de Valdés (16) | Valdés | 73 |
| Forêt de Nava (10) | Nava | 73 |
| Forêt de Cudillero (14) | Cudillero | 73 |
| Forêt de Cudillero (17) | Cudillero | 73 |
| Forêt de El Franco (12) | El Franco | 73 |
| Forêt de Laviana (18) | Laviana | 73 |
| Forêt de Valdés (38) | Valdés | 73 |
| Forêt de Riosa (4) | Riosa | 73 |
| Forêt de Valdés (10) | Valdés | 72 |
| Forêt de Mieres (7) | Mieres | 72 |
| Forêt de Allande (11) | Allande | 72 |
| Forêt de Allande (18) | Allande | 72 |
| Forêt de Ponga (36) | Ponga | 72 |
| Forêt de Villaviciosa (55) | Villaviciosa | 72 |
| Forêt de Langreo (4) | Langreo | 71 |
| Forêt de Pravia (12) | Pravia | 71 |
| Forêt de Illano (5) | Illano | 71 |
| Forêt de Piloña (21) | Piloña | 71 |
| Forêt de Valdés (40) | Valdés | 71 |
| Forêt de Grandas de Salime (27) | Grandas de Salime | 71 |
| Forêt de Llanes (23) | Llanes | 71 |
| Forêt de Cabrales (214) | Cabrales | 71 |
| Forêt de Salas (2) | Salas | 70 |
| Forêt de Siero (3) | Siero | 70 |
| Forêt de Cudillero (7) | Cudillero | 70 |
| Forêt de Corvera de Asturias (2) | Corvera de Asturias | 70 |
| Forêt de Grado (16) | Grado | 70 |
| Forêt de Valdés (28) | Valdés | 70 |
| Forêt de Allande (22) | Allande | 70 |
| Forêt de Grandas de Salime (25) | Grandas de Salime | 70 |
| Forêt de Cudillero (25) | Cudillero | 70 |
| Forêt de Valdés (63) | Valdés | 70 |
| Forêt de Boal (12) | Boal | 69 |
| Forêt de Oviedo (29) | Oviedo | 69 |
| Forêt de Tineo (55) | Tineo | 69 |
| Forêt de Villaviciosa (32) | Villaviciosa | 69 |
| Forêt de Siero (24) | Siero | 69 |
| Forêt de Cangas del Narcea (82) | Cangas del Narcea | 69 |
| Forêt de Cangas del Narcea (110) | Cangas del Narcea | 69 |
| Forêt de Parres (53) | Parres | 69 |
| Forêt de Onís (67) | Onís | 69 |
| Forêt de Degaña (7) | Degaña | 68 |
| Forêt de Teverga (4) | Teverga | 68 |
| Forêt de Candamo (3) | Candamo | 68 |
| Forêt de Mieres (15) | Mieres | 68 |
| Forêt de Illano (11) | Illano | 68 |
| Forêt de Yernes y Tameza (3) | Yernes y Tameza | 68 |
| Forêt de Grado (36) | Grado | 68 |
| Forêt de Tineo (33) | Tineo | 67 |
| Forêt de El Franco (9) | El Franco | 67 |
| Forêt de Cangas del Narcea (72) | Cangas del Narcea | 67 |
| Forêt de Grado (27) | Grado | 67 |
| Forêt de Parres (52) | Parres | 67 |
| Forêt de Allande | Allande | 66 |
| Forêt de Tineo (2) | Tineo | 66 |
| Forêt de Piloña (13) | Piloña | 66 |
| Forêt de Candamo | Candamo | 66 |
| Forêt de Valdés (54) | Valdés | 66 |
| Forêt de Valdés (68) | Valdés | 66 |
| Forêt de Somiedo (42) | Somiedo | 66 |
| Forêt de Mieres (28) | Mieres | 66 |
| Bois de Llanes (81) | Llanes | 66 |
| Forêt de Cangas de Onís (12) | Cangas de Onís | 65 |
| Forêt de Tineo (37) | Tineo | 65 |
| Forêt de Caso (15) | Caso | 65 |
| Forêt de Villaviciosa (29) | Villaviciosa | 65 |
| Forêt de Piloña (66) | Piloña | 65 |
| Forêt de Grado (33) | Grado | 65 |
| Forêt de Peñamellera Baja (24) | Peñamellera Baja | 65 |
| Forêt de Ribadesella (73) | Ribadesella | 65 |
| Forêt de Teverga (5) | Teverga | 64 |
| Forêt de Piloña (22) | Piloña | 64 |
| Forêt de Piloña (23) | Piloña | 64 |
| Forêt de Caso (20) | Caso | 64 |
| Forêt de Somiedo (24) | Somiedo | 64 |
| Forêt de Villayón (13) | Villayón | 64 |
| Forêt de Valdés (60) | Valdés | 64 |
| Forêt de San Tirso de Abres (3) | San Tirso de Abres | 63 |
| Forêt de Valdés (18) | Valdés | 63 |
| Forêt de Villaviciosa (21) | Villaviciosa | 63 |
| Forêt de Aller (21) | Aller | 63 |
| Forêt de Langreo (14) | Langreo | 63 |
| Forêt de Valdés (30) | Valdés | 63 |
| Forêt de Salas (34) | Salas | 63 |
| Forêt de San Martín de Oscos (8) | San Martín de Oscos | 63 |
| Forêt de Allande (32) | Allande | 63 |
| Forêt de Llanera (18) | Llanera | 63 |
| Forêt de Cangas del Narcea (102) | Cangas del Narcea | 63 |
| Forêt de Cangas de Onís (128) | Cangas de Onís | 63 |
| Forêt de Cangas de Onís (4) | Cangas de Onís | 62 |
| Forêt de Llanes (13) | Llanes | 62 |
| Forêt de Ribadesella (9) | Ribadesella | 62 |
| Forêt de Castropol (10) | Castropol | 62 |
| Forêt de Valdés (49) | Valdés | 62 |
| Forêt de Bimenes (9) | Bimenes | 62 |
| Forêt de Cangas de Onís (5) | Cangas de Onís | 61 |
| Forêt de Villaviciosa (4) | Villaviciosa | 61 |
| Forêt de Tineo (12) | Tineo | 61 |
| Forêt de Cangas del Narcea (34) | Cangas del Narcea | 61 |
| Forêt de Grado (14) | Grado | 61 |
| Forêt de Salas (33) | Salas | 61 |
| Forêt de Tineo (88) | Tineo | 61 |
| Forêt de Belmonte de Miranda (22) | Belmonte de Miranda | 61 |
| Forêt de Llanes (26) | Llanes | 61 |
| Forêt de Valdés (71) | Valdés | 61 |
| Forêt de Tineo (9) | Tineo | 60 |
| Forêt de Allande (6) | Allande | 60 |
| Forêt de Laviana (9) | Laviana | 60 |
| Forêt de Caso (42) | Caso | 60 |
| Forêt de Riosa (5) | Riosa | 60 |
| Forêt de Oviedo (49) | Oviedo | 60 |
| Forêt de Cabrales (210) | Cabrales | 60 |
| Forêt de Tineo (26) | Tineo | 59 |
| Forêt de Coaña (5) | Coaña | 59 |
| Forêt de Las Regueras (8) | Las Regueras | 59 |
| Forêt de Valdés (35) | Valdés | 59 |
| Forêt de Piloña (43) | Piloña | 59 |
| Forêt de Piloña (59) | Piloña | 59 |
| Forêt de Cangas del Narcea (88) | Cangas del Narcea | 59 |
| Forêt de Villaviciosa (54) | Villaviciosa | 59 |
| Forêt de Lena (24) | Lena | 59 |
| Forêt de Castropol (17) | Castropol | 59 |
| Bois de Taramundi | Taramundi | 59 |
| Forêt de Caso (63) | Caso | 59 |
| Forêt de Cangas del Narcea (19) | Cangas del Narcea | 58 |
| Monte de la Varera | Cabrales | 58 |
| Forêt de Valdés (19) | Valdés | 58 |
| Forêt de Morcín (3) | Morcín | 58 |
| Forêt de Cangas del Narcea (55) | Cangas del Narcea | 58 |
| Forêt de Cangas de Onís (25) | Cangas de Onís | 58 |
| Forêt de El Franco (18) | El Franco | 58 |
| Forêt de Illano (20) | Illano | 58 |
| Forêt de Cabrales (227) | Cabrales | 58 |
| Bois de Ribadesella (5) | Ribadesella | 58 |
| Forêt de Valdés (8) | Valdés | 57 |
| Forêt de Tineo (19) | Tineo | 57 |
| Forêt de Allande (8) | Allande | 57 |
| Forêt de Piloña (16) | Piloña | 57 |
| Forêt de Cabrales (4) | Cabrales | 57 |
| Forêt de Tineo (27) | Tineo | 57 |
| Forêt de Lena (12) | Lena | 57 |
| Forêt de Gijón (30) | Gijón | 57 |
| Forêt de Mieres (16) | Mieres | 57 |
| Forêt de Nava (13) | Nava | 57 |
| Forêt de Degaña (16) | Degaña | 57 |
| Forêt de Navia (4) | Navia | 57 |
| Forêt de Siero (30) | Siero | 57 |
| Forêt de Valdés (57) | Valdés | 57 |
| Forêt de Tineo (13) | Tineo | 56 |
| Forêt de Valdés (33) | Valdés | 56 |
| Forêt de Villanueva de Oscos (6) | Villanueva de Oscos | 56 |
| Forêt de Tineo (83) | Tineo | 56 |
| Forêt de Morcín (6) | Morcín | 56 |
| Forêt de Ponga (55) | Ponga | 56 |
| Forêt de Somiedo (3) | Somiedo | 55 |
| Forêt de Peñamellera Baja (9) | Peñamellera Baja | 55 |
| Forêt de Gozón (4) | Gozón | 55 |
| Bois de Siero | Siero | 55 |
| Forêt de Taramundi (19) | Taramundi | 55 |
| Forêt de Somiedo (34) | Somiedo | 55 |
| Forêt de Tineo (107) | Tineo | 55 |
| Forêt de Allande (36) | Allande | 55 |
| Forêt de Tineo (7) | Tineo | 54 |
| Forêt de Caso (16) | Caso | 54 |
| Forêt de Caso (24) | Caso | 54 |
| Forêt de Piloña (36) | Piloña | 54 |
| Forêt de Salas (32) | Salas | 54 |
| Forêt de Ribadesella (10) | Ribadesella | 54 |
| Forêt de Aller (40) | Aller | 54 |
| Forêt de Allande (38) | Allande | 54 |
| Forêt de Ribadesella (20) | Ribadesella | 54 |
| Forêt de Gijón (29) | Gijón | 53 |
| Forêt de Somiedo (12) | Somiedo | 53 |
| Forêt de Tineo (45) | Tineo | 53 |
| Forêt de Pravia (21) | Pravia | 53 |
| Forêt de Tineo (62) | Tineo | 53 |
| Forêt de Piloña (42) | Piloña | 53 |
| Forêt de Caso (37) | Caso | 53 |
| Forêt de Tineo (82) | Tineo | 53 |
| Forêt de Siero (31) | Siero | 53 |
| Forêt de Piloña (64) | Piloña | 53 |
| Forêt de Degaña (9) | Degaña | 52 |
| Forêt de Piloña (24) | Piloña | 52 |
| Forêt de Pravia (20) | Pravia | 52 |
| Forêt de Grandas de Salime (22) | Grandas de Salime | 52 |
| Forêt de Castropol (13) | Castropol | 52 |
| Forêt de Colunga (11) | Colunga | 52 |
| Forêt de Tineo (98) | Tineo | 52 |
| Forêt de Aller (58) | Aller | 52 |
| Forêt de Llanes (29) | Llanes | 52 |
| Forêt de Cangas de Onís (127) | Cangas de Onís | 52 |
| Forêt de Cabrales (220) | Cabrales | 52 |
| Forêt de Langreo (2) | Langreo | 51 |
| Forêt de Cangas del Narcea (23) | Cangas del Narcea | 51 |
| Forêt de San Martín de Oscos | San Martín de Oscos | 51 |
| Forêt de Allande (12) | Allande | 51 |
| Forêt de Villayón (7) | Villayón | 51 |
| Forêt de Ibias (16) | Ibias | 51 |
| Forêt de Quirós (24) | Quirós | 51 |
| Forêt de Tineo (78) | Tineo | 51 |
| Forêt de Proaza (3) | Proaza | 51 |
| Forêt de Gozón (10) | Gozón | 51 |
| Forêt de Villayón (21) | Villayón | 51 |
| Forêt de Salas (40) | Salas | 51 |
| Forêt de Colunga (33) | Colunga | 51 |
| Forêt de Gijón (19) | Gijón | 50 |
| Forêt de Nava | Nava | 50 |
| Forêt de Vegadeo (2) | Vegadeo | 50 |
| Forêt de Lena | Lena | 50 |
| Forêt de Laviana (4) | Laviana | 50 |
| Forêt de Teverga (3) | Teverga | 50 |
| Forêt de Sariego | Sariego | 50 |
| Forêt de Allande (16) | Allande | 50 |
| Forêt de Gijón (44) | Gijón | 50 |
| Forêt de Cabrales (223) | Cabrales | 50 |
| Bois de Las Regueras | Las Regueras | 49 |
| Forêt de Villanueva de Oscos (2) | Villanueva de Oscos | 49 |
| Forêt de Illano (8) | Illano | 49 |
| Forêt de Parres (9) | Parres | 49 |
| Forêt de Salas (35) | Salas | 49 |
| Forêt de Allande (30) | Allande | 49 |
| Forêt de Valdés (56) | Valdés | 49 |
| Forêt de Tineo (96) | Tineo | 49 |
| Forêt de Cudillero (30) | Cudillero | 49 |
| Forêt de Piloña (68) | Piloña | 49 |
| Forêt de Pravia (49) | Pravia | 49 |
| Forêt de Castropol (4) | Castropol | 48 |
| Forêt de Piloña (18) | Piloña | 48 |
| Forêt de Ibias (10) | Ibias | 48 |
| Forêt de Ribadesella (4) | Ribadesella | 48 |
| Forêt de Lena (14) | Lena | 48 |
| Forêt de Carreño (4) | Carreño | 48 |
| Forêt de Illano (9) | Illano | 48 |
| Forêt de Piloña (46) | Piloña | 48 |
| Forêt de Aller (41) | Aller | 48 |
| Forêt de Castropol (14) | Castropol | 48 |
| Forêt de Bimenes (10) | Bimenes | 48 |
| Monte la Viular | Lena | 48 |
| Forêt de Tineo (6) | Tineo | 47 |
| Forêt de Llanes (5) | Llanes | 47 |
| Forêt de Gijón (26) | Gijón | 47 |
| Forêt de Sobrescobio (5) | Sobrescobio | 47 |
| Forêt de Cudillero (16) | Cudillero | 47 |
| Forêt de Pravia (22) | Pravia | 47 |
| Forêt de Mieres (18) | Mieres | 47 |
| Forêt de Cangas de Onís (30) | Cangas de Onís | 47 |
| Forêt de Piloña (72) | Piloña | 47 |
| Forêt de Taramundi (5) | Taramundi | 46 |
| Forêt de Tineo (14) | Tineo | 46 |
| Forêt de Castropol (2) | Castropol | 46 |
| Forêt de Llanes (7) | Llanes | 46 |
| Forêt de Piloña (19) | Piloña | 46 |
| Forêt de Avilés (3) | Avilés | 46 |
| Forêt de Cangas del Narcea (66) | Cangas del Narcea | 46 |
| Forêt de Amieva (5) | Amieva | 46 |
| Forêt de Siero (22) | Siero | 46 |
| Forêt de Grandas de Salime (24) | Grandas de Salime | 46 |
| Forêt de Siero (26) | Siero | 46 |
| Forêt de Carreño (9) | Carreño | 46 |
| Forêt de Villaviciosa (47) | Villaviciosa | 46 |
| Forêt de Pesoz (3) | Pesoz | 46 |
| Forêt de Villaviciosa (57) | Villaviciosa | 46 |
| Forêt de Allande (34) | Allande | 46 |
| Forêt de Ponga (47) | Ponga | 46 |
| Forêt de Peñamellera Alta (20) | Peñamellera Alta | 46 |
| Forêt de Ponga (2) | Ponga | 45 |
| Forêt de Belmonte de Miranda | Belmonte de Miranda | 45 |
| Forêt de Vegadeo (3) | Vegadeo | 45 |
| Forêt de Gijón (23) | Gijón | 45 |
| Forêt de Mieres (3) | Mieres | 45 |
| Forêt de Valdés (24) | Valdés | 45 |
| Forêt de Piloña (35) | Piloña | 45 |
| Forêt de Castropol (8) | Castropol | 45 |
| Forêt de Valdés (44) | Valdés | 45 |
| Forêt de Pravia (39) | Pravia | 45 |
| Forêt de Grado (29) | Grado | 45 |
| Forêt de Siero (33) | Siero | 45 |
| Forêt de Quirós (36) | Quirós | 45 |
| Forêt de Cudillero (33) | Cudillero | 45 |
| Forêt de Piloña | Piloña | 44 |
| Forêt de Ibias (7) | Ibias | 44 |
| Forêt de Coaña (4) | Coaña | 44 |
| Forêt de Cabrales (5) | Cabrales | 44 |
| Forêt de Salas (19) | Salas | 44 |
| Forêt de Grado (17) | Grado | 44 |
| Forêt de Parres (8) | Parres | 44 |
| Forêt de Cangas del Narcea (63) | Cangas del Narcea | 44 |
| Forêt de Somiedo (25) | Somiedo | 44 |
| Forêt de Cudillero (22) | Cudillero | 44 |
| Forêt de Nava (15) | Nava | 44 |
| Forêt de Carreño (8) | Carreño | 44 |
| Forêt de Siero (37) | Siero | 44 |
| Forêt de Llanera (26) | Llanera | 44 |
| Forêt de Pravia (54) | Pravia | 44 |
| Forêt de Ponga (46) | Ponga | 44 |
| Forêt de Coaña (3) | Coaña | 43 |
| Forêt de Piloña (11) | Piloña | 43 |
| Forêt de Nava (7) | Nava | 43 |
| Forêt de Gozón (6) | Gozón | 43 |
| Forêt de Piloña (38) | Piloña | 43 |
| Forêt de Cangas del Narcea (100) | Cangas del Narcea | 43 |
| Forêt de Salas (42) | Salas | 43 |
| Forêt de Siero (38) | Siero | 43 |
| Forêt de Piloña (78) | Piloña | 43 |
| Bois de Laviana | Laviana | 42 |
| Forêt de Villanueva de Oscos (3) | Villanueva de Oscos | 42 |
| Forêt de Parres (2) | Parres | 42 |
| Forêt de Mieres (10) | Mieres | 42 |
| Forêt de Ibias (12) | Ibias | 42 |
| Forêt de Tineo (42) | Tineo | 42 |
| Forêt de Valdés (25) | Valdés | 42 |
| Forêt de Villanueva de Oscos (5) | Villanueva de Oscos | 42 |
| Forêt de Laviana (22) | Laviana | 42 |
| Forêt de Las Regueras (14) | Las Regueras | 42 |
| Forêt de Carreño (7) | Carreño | 42 |
| Forêt de Allande (33) | Allande | 42 |
| Forêt de Castropol (16) | Castropol | 42 |
| Forêt de Gijón (50) | Gijón | 42 |
| Forêt de Salas (44) | Salas | 42 |
| Forêt de Parres (30) | Parres | 42 |
| Forêt de Cangas del Narcea (3) | Cangas del Narcea | 41 |
| Forêt de Cangas del Narcea (5) | Cangas del Narcea | 41 |
| Forêt de Ibias (8) | Ibias | 41 |
| Forêt de Boal (4) | Boal | 41 |
| Forêt de Villaviciosa (27) | Villaviciosa | 41 |
| Forêt de Bimenes (5) | Bimenes | 41 |
| Forêt de Santo Adriano (4) | Santo Adriano | 41 |
| Forêt de Grado (28) | Grado | 41 |
| Forêt de Las Regueras (19) | Las Regueras | 41 |
| Forêt de Aller (48) | Aller | 41 |
| Forêt de Pesoz (4) | Pesoz | 41 |
| Forêt de Coaña (11) | Coaña | 41 |
| Forêt de Las Regueras (22) | Las Regueras | 41 |
| Forêt de Laviana (33) | Laviana | 41 |
| Forêt de Villaviciosa (63) | Villaviciosa | 41 |
| Forêt de Grandas de Salime (35) | Grandas de Salime | 41 |
| Forêt de Cangas de Onís (43) | Cangas de Onís | 41 |
| Forêt de Valdés (6) | Valdés | 40 |
| Forêt de Carreño (2) | Carreño | 40 |
| Forêt de Aller (8) | Aller | 40 |
| Forêt de Ponga (17) | Ponga | 40 |
| Forêt de Aller (16) | Aller | 40 |
| Forêt de Valdés (32) | Valdés | 40 |
| Forêt de Colunga (8) | Colunga | 40 |
| Forêt de Parres (14) | Parres | 40 |
| Forêt de Laviana (24) | Laviana | 40 |
| Forêt de Siero (25) | Siero | 40 |
| Forêt de Cangas de Onís (28) | Cangas de Onís | 40 |
| Forêt de Aller (43) | Aller | 40 |
| Forêt de Allande (28) | Allande | 40 |
| Forêt de Peñamellera Alta (11) | Peñamellera Alta | 40 |
| Forêt de Corvera de Asturias (7) | Corvera de Asturias | 40 |
| Forêt de Caso (46) | Caso | 40 |
| Forêt de Valdés (61) | Valdés | 40 |
| Forêt de Illano (17) | Illano | 40 |
| Forêt de Salas (41) | Salas | 40 |
| Forêt de Somiedo (40) | Somiedo | 40 |
| Forêt de Belmonte de Miranda (30) | Belmonte de Miranda | 40 |
| Bois de Taramundi (3) | Taramundi | 40 |
| Forêt de Valdés | Valdés | 39 |
| Forêt de El Franco (2) | El Franco | 39 |
| Forêt de Lena (5) | Lena | 39 |
| Forêt de Boal (7) | Boal | 39 |
| Forêt de Salas (15) | Salas | 39 |
| Forêt de Ponga (15) | Ponga | 39 |
| Forêt de Castrillón (3) | Castrillón | 39 |
| Forêt de Ibias (13) | Ibias | 39 |
| Forêt de Tineo (47) | Tineo | 39 |
| Forêt de Laviana (12) | Laviana | 39 |
| Forêt de Siero (21) | Siero | 39 |
| Forêt de Allande (24) | Allande | 39 |
| Forêt de Grado (23) | Grado | 39 |
| Forêt de Laviana (21) | Laviana | 39 |
| Monte Les Lláscares | Laviana | 39 |
| Forêt de Grandas de Salime (30) | Grandas de Salime | 39 |
| Forêt de Mieres (26) | Mieres | 39 |
| Forêt de Ribadesella (19) | Ribadesella | 39 |
| Forêt de Aller (54) | Aller | 39 |
| Forêt de Cudillero (35) | Cudillero | 39 |
| Forêt de Sobrescobio (11) | Sobrescobio | 39 |
| Forêt de Samartín del Rei Aurelio (10) | Samartín del Rei Aurelio | 39 |
| Forêt de Boal (30) | Boal | 39 |
| Forêt de Salas (4) | Salas | 38 |
| Forêt de Cangas del Narcea (17) | Cangas del Narcea | 38 |
| Forêt de Illano (7) | Illano | 38 |
| Forêt de Tineo (40) | Tineo | 38 |
| Monte La Secuesta | Sobrescobio | 38 |
| Forêt de Cangas del Narcea (59) | Cangas del Narcea | 38 |
| Forêt de Cangas del Narcea (64) | Cangas del Narcea | 38 |
| Forêt de Tapia de Casariego (9) | Tapia de Casariego | 38 |
| Forêt de Cangas del Narcea (81) | Cangas del Narcea | 38 |
| Forêt de Lena (21) | Lena | 38 |
| Forêt de Quirós (32) | Quirós | 38 |
| Forêt de Valdés (69) | Valdés | 38 |
| Monte la Vaḷḷina Negra | Lena | 38 |
| Forêt de Cangas de Onís (117) | Cangas de Onís | 38 |
| Forêt de Amieva (3) | Amieva | 37 |
| Forêt de Laviana (5) | Laviana | 37 |
| Forêt de Ponga (14) | Ponga | 37 |
| Forêt de Ibias (11) | Ibias | 37 |
| Forêt de Llanes (14) | Llanes | 37 |
| Forêt de Cangas del Narcea (45) | Cangas del Narcea | 37 |
| Forêt de Cangas de Onís (18) | Cangas de Onís | 37 |
| Forêt de Colunga (3) | Colunga | 37 |
| Forêt de Cangas del Narcea (52) | Cangas del Narcea | 37 |
| Forêt de Salas (24) | Salas | 37 |
| Forêt de Taramundi (16) | Taramundi | 37 |
| Forêt de Sobrescobio (8) | Sobrescobio | 37 |
| Forêt de Cangas del Narcea (69) | Cangas del Narcea | 37 |
| Forêt de Illas (2) | Illas | 37 |
| Forêt de Ribadesella (14) | Ribadesella | 37 |
| Forêt de Santa Eulalia de Oscos (15) | Santa Eulalia de Oscos | 37 |
| Bois de Villaviciosa (2) | Villaviciosa | 37 |
| Forêt de Parres (22) | Parres | 37 |
| Forêt de Cangas del Narcea (101) | Cangas del Narcea | 37 |
| Bois de Taramundi (7) | Taramundi | 37 |
| Forêt de Siero | Siero | 36 |
| Forêt de Valdés (4) | Valdés | 36 |
| Forêt de Lena (4) | Lena | 36 |
| Forêt de El Franco (3) | El Franco | 36 |
| Forêt de Peñamellera Baja (8) | Peñamellera Baja | 36 |
| Monte Acebucu | Cabrales | 36 |
| Forêt de Valdés (20) | Valdés | 36 |
| Forêt de Cangas del Narcea (49) | Cangas del Narcea | 36 |
| Forêt de Belmonte de Miranda (11) | Belmonte de Miranda | 36 |
| Forêt de Tineo (67) | Tineo | 36 |
| Forêt de Soto del Barco (6) | Soto del Barco | 36 |
| Forêt de Cabranes (9) | Cabranes | 36 |
| Forêt de Ribadedeva (7) | Ribadedeva | 36 |
| Forêt de Yernes y Tameza (5) | Yernes y Tameza | 36 |
| Forêt de Pravia (46) | Pravia | 36 |
| Forêt de Navia (6) | Navia | 36 |
| Monte Camba | Cabrales | 36 |
| Forêt de Grado (38) | Grado | 36 |
| Forêt de Cangas de Onís (7) | Cangas de Onís | 35 |
| Forêt de Vegadeo (4) | Vegadeo | 35 |
| Forêt de Llanes (4) | Llanes | 35 |
| Forêt de Ponga (9) | Ponga | 35 |
| Forêt de Gozón | Gozón | 35 |
| Forêt de Tineo (31) | Tineo | 35 |
| Forêt de Valdés (21) | Valdés | 35 |
| Forêt de Nava (11) | Nava | 35 |
| Forêt de El Franco (10) | El Franco | 35 |
| Forêt de Salas (27) | Salas | 35 |
| Forêt de Aller (35) | Aller | 35 |
| Forêt de Samartín del Rei Aurelio (6) | Samartín del Rei Aurelio | 35 |
| Forêt de Cangas del Narcea (80) | Cangas del Narcea | 35 |
| Forêt de Ibias (23) | Ibias | 35 |
| Forêt de Cangas del Narcea (90) | Cangas del Narcea | 35 |
| Forêt de Vegadeo (15) | Vegadeo | 35 |
| Forêt de Cangas del Narcea (107) | Cangas del Narcea | 35 |
| Forêt de Castropol (3) | Castropol | 34 |
| Forêt de Ponga (16) | Ponga | 34 |
| Forêt de Ribadesella (5) | Ribadesella | 34 |
| Forêt de Bimenes (4) | Bimenes | 34 |
| Forêt de Teverga (7) | Teverga | 34 |
| Forêt de Cangas del Narcea (48) | Cangas del Narcea | 34 |
| Forêt de Somiedo (17) | Somiedo | 34 |
| Forêt de Gijón (35) | Gijón | 34 |
| Forêt de Tineo (57) | Tineo | 34 |
| Forêt de El Franco (14) | El Franco | 34 |
| Forêt de Amieva (7) | Amieva | 34 |
| Forêt de Vegadeo (12) | Vegadeo | 34 |
| Forêt de Caso (43) | Caso | 34 |
| Forêt de Amieva (8) | Amieva | 34 |
| Forêt de Las Regueras (20) | Las Regueras | 34 |
| Forêt de El Franco (21) | El Franco | 34 |
| Forêt de Cangas del Narcea (105) | Cangas del Narcea | 34 |
| Forêt de Castropol (18) | Castropol | 34 |
| Forêt de Salas (3) | Salas | 33 |
| Forêt de Cangas del Narcea (8) | Cangas del Narcea | 33 |
| Forêt de Teverga | Teverga | 33 |
| Forêt de Piloña (8) | Piloña | 33 |
| Forêt de Tineo (25) | Tineo | 33 |
| Forêt de Aller (9) | Aller | 33 |
| Forêt de Cangas del Narcea (42) | Cangas del Narcea | 33 |
| Forêt de Vegadeo (10) | Vegadeo | 33 |
| Forêt de Degaña (13) | Degaña | 33 |
| Forêt de Candamo (6) | Candamo | 33 |
| Forêt de Allande (27) | Allande | 33 |
| Forêt de Cangas del Narcea (86) | Cangas del Narcea | 33 |
| Forêt de Ibias (27) | Ibias | 33 |
| Forêt de Laviana (30) | Laviana | 33 |
| Forêt de Lena (28) | Lena | 33 |
| Forêt de Boal (28) | Boal | 33 |
| Forêt de Nava (19) | Nava | 33 |
| Forêt de Navia (11) | Navia | 33 |
| Forêt de Cangas de Onís (129) | Cangas de Onís | 33 |
| Forêt de Villaviciosa (8) | Villaviciosa | 32 |
| Forêt de Nava (4) | Nava | 32 |
| Forêt de Cangas del Narcea (31) | Cangas del Narcea | 32 |
| Forêt de Siero (14) | Siero | 32 |
| Forêt de Ribera de Arriba (3) | Ribera de Arriba | 32 |
| Forêt de Taramundi (9) | Taramundi | 32 |
| Forêt de Boal (10) | Boal | 32 |
| Forêt de Llanera (15) | Llanera | 32 |
| Forêt de Villayón (12) | Villayón | 32 |
| Forêt de Valdés (39) | Valdés | 32 |
| Forêt de Carreño (5) | Carreño | 32 |
| Forêt de Tineo (66) | Tineo | 32 |
| Forêt de Grado (25) | Grado | 32 |
| Forêt de Cabranes (6) | Cabranes | 32 |
| Forêt de Boal (21) | Boal | 32 |
| Forêt de Oviedo (38) | Oviedo | 32 |
| Forêt de Las Regueras (23) | Las Regueras | 32 |
| Forêt de Cangas del Narcea (103) | Cangas del Narcea | 32 |
| Forêt de Villaviciosa (67) | Villaviciosa | 32 |
| Bois de Llanes (55) | Llanes | 32 |
| Forêt de Cangas de Onís (14) | Cangas de Onís | 31 |
| Forêt de Villayón (8) | Villayón | 31 |
| Forêt de Ibias (14) | Ibias | 31 |
| Forêt de Piloña (31) | Piloña | 31 |
| Forêt de Somiedo (18) | Somiedo | 31 |
| El Fayíu | Lena | 31 |
| Forêt de Tineo (70) | Tineo | 31 |
| Forêt de Las Regueras (15) | Las Regueras | 31 |
| Forêt de Caso (34) | Caso | 31 |
| Forêt de Boal (22) | Boal | 31 |
| Forêt de Ribadesella (13) | Ribadesella | 31 |
| Forêt de Siero (32) | Siero | 31 |
| Forêt de Illano (19) | Illano | 31 |
| Forêt de Caso (47) | Caso | 31 |
| Forêt de Allande (35) | Allande | 31 |
| Monte Llué | Cabrales | 31 |
| Forêt de Boal (31) | Boal | 31 |
| Forêt de Cabrales (225) | Cabrales | 31 |
| Forêt de Laviana | Laviana | 30 |
| Forêt de Taramundi (8) | Taramundi | 30 |
| Forêt de Tapia de Casariego (2) | Tapia de Casariego | 30 |
| Forêt de Degaña (11) | Degaña | 30 |
| Forêt de Grado (13) | Grado | 30 |
| Forêt de Salas (22) | Salas | 30 |
| Forêt de Tineo (52) | Tineo | 30 |
| Forêt de Cangas del Narcea (58) | Cangas del Narcea | 30 |
| Forêt de Somiedo (26) | Somiedo | 30 |
| Forêt de Amieva (6) | Amieva | 30 |
| Forêt de Lena (20) | Lena | 30 |
| Forêt de Ribera de Arriba (7) | Ribera de Arriba | 30 |
| Forêt de Salas (37) | Salas | 30 |
| Forêt de Yernes y Tameza (4) | Yernes y Tameza | 30 |
| Forêt de Langreo (26) | Langreo | 30 |
| Forêt de Valdés (58) | Valdés | 30 |
| Forêt de Valdés (59) | Valdés | 30 |
| Forêt de Vegadeo (17) | Vegadeo | 30 |
| Forêt de Pravia (43) | Pravia | 30 |
| Forêt de El Franco (20) | El Franco | 30 |
| Forêt de Piloña (2) | Piloña | 29 |
| Forêt de Peñamellera Alta (4) | Peñamellera Alta | 29 |
| Forêt de Grado (5) | Grado | 29 |
| Forêt de Belmonte de Miranda (4) | Belmonte de Miranda | 29 |
| Forêt de Valdés (14) | Valdés | 29 |
| Forêt de Tineo (18) | Tineo | 29 |
| Forêt de Oviedo (23) | Oviedo | 29 |
| Forêt de Siero (13) | Siero | 29 |
| Forêt de Tineo (35) | Tineo | 29 |
| Forêt de Siero (16) | Siero | 29 |
| Forêt de San Martín de Oscos (4) | San Martín de Oscos | 29 |
| Forêt de Boal (16) | Boal | 29 |
| Forêt de Valdés (46) | Valdés | 29 |
| Forêt de Villaviciosa (40) | Villaviciosa | 29 |
| Forêt de Valdés (52) | Valdés | 29 |
| Forêt de Sobrescobio (9) | Sobrescobio | 29 |
| Forêt de Cangas de Onís (34) | Cangas de Onís | 29 |
| Forêt de Piloña (71) | Piloña | 29 |
| Forêt de Peñamellera Baja (21) | Peñamellera Baja | 29 |
| Forêt de Cudillero (41) | Cudillero | 29 |
| Bois de Ribadesella (6) | Ribadesella | 29 |
| Forêt de Boal (2) | Boal | 28 |
| Forêt de Villaviciosa (6) | Villaviciosa | 28 |
| Forêt de Cangas del Narcea (21) | Cangas del Narcea | 28 |
| Forêt de Grandas de Salime (15) | Grandas de Salime | 28 |
| Forêt de Cangas de Onís (10) | Cangas de Onís | 28 |
| Forêt de Ponga (11) | Ponga | 28 |
| Forêt de Peñamellera Baja (11) | Peñamellera Baja | 28 |
| Forêt de Mieres (11) | Mieres | 28 |
| Forêt de Somiedo (13) | Somiedo | 28 |
| Forêt de Salas (20) | Salas | 28 |
| Forêt de Piloña (26) | Piloña | 28 |
| Forêt de Aller (19) | Aller | 28 |
| Forêt de Cangas del Narcea (57) | Cangas del Narcea | 28 |
| Forêt de Grado (18) | Grado | 28 |
| Forêt de Samartín del Rei Aurelio (5) | Samartín del Rei Aurelio | 28 |
| Forêt de Aller (28) | Aller | 28 |
| Forêt de Piloña (47) | Piloña | 28 |
| Forêt de Santa Eulalia de Oscos (13) | Santa Eulalia de Oscos | 28 |
| Forêt de Cangas del Narcea (74) | Cangas del Narcea | 28 |
| Forêt de Tineo (73) | Tineo | 28 |
| Forêt de Tineo (76) | Tineo | 28 |
| Forêt de Parres (20) | Parres | 28 |
| Forêt de Somiedo (30) | Somiedo | 28 |
| Forêt de Laviana (28) | Laviana | 28 |
| Forêt de Salas (36) | Salas | 28 |
| Forêt de Villaviciosa (50) | Villaviciosa | 28 |
| Forêt de Boal (26) | Boal | 28 |
| Forêt de Villayón (22) | Villayón | 28 |
| Forêt de Belmonte de Miranda (23) | Belmonte de Miranda | 28 |
| Forêt de Allande (37) | Allande | 28 |
| Forêt de Peñamellera Alta (12) | Peñamellera Alta | 28 |
| Forêt de Valdés (75) | Valdés | 28 |
| Forêt de Valdés (88) | Valdés | 28 |
| Forêt de Llanes (34) | Llanes | 28 |
| Forêt de Oviedo (67) | Oviedo | 28 |
| Bois de Mieres (2) | Mieres | 28 |
| Forêt de Onís (68) | Onís | 28 |
| Forêt de Oviedo (17) | Oviedo | 27 |
| Forêt de Cudillero (4) | Cudillero | 27 |
| Forêt de Allande (5) | Allande | 27 |
| Forêt de Tineo (20) | Tineo | 27 |
| Forêt de Cangas del Narcea (29) | Cangas del Narcea | 27 |
| La Fayalunta | Piloña | 27 |
| Forêt de Riosa | Riosa | 27 |
| Forêt de Sariego (2) | Sariego | 27 |
| Forêt de Aller (17) | Aller | 27 |
| Forêt de Cabrales (7) | Cabrales | 27 |
| Forêt de Piloña (45) | Piloña | 27 |
| Forêt de Piloña (49) | Piloña | 27 |
| Forêt de Cudillero (23) | Cudillero | 27 |
| Forêt de Belmonte de Miranda (21) | Belmonte de Miranda | 27 |
| Forêt de Tineo (92) | Tineo | 27 |
| Forêt de Villaviciosa (62) | Villaviciosa | 27 |
| Forêt de Cangas de Onís (116) | Cangas de Onís | 27 |
| Forêt de Taramundi (61) | Taramundi | 27 |
| Forêt de Tineo (955) | Tineo | 27 |
| Forêt de Tineo | Tineo | 26 |
| Forêt de Piloña (4) | Piloña | 26 |
| Forêt de Valdés (2) | Valdés | 26 |
| Forêt de Villaviciosa (5) | Villaviciosa | 26 |
| Forêt de Cangas del Narcea (16) | Cangas del Narcea | 26 |
| Forêt de Cangas del Narcea (35) | Cangas del Narcea | 26 |
| Forêt de Grado (10) | Grado | 26 |
| Forêt de Aller (10) | Aller | 26 |
| Forêt de Grandas de Salime (16) | Grandas de Salime | 26 |
| Forêt de Caso (17) | Caso | 26 |
| Forêt de Tapia de Casariego (6) | Tapia de Casariego | 26 |
| Forêt de Oviedo (27) | Oviedo | 26 |
| Forêt de Taramundi (13) | Taramundi | 26 |
| Forêt de Cangas del Narcea (54) | Cangas del Narcea | 26 |
| Forêt de Ribera de Arriba (4) | Ribera de Arriba | 26 |
| Forêt de Tineo (54) | Tineo | 26 |
| Forêt de Caso (23) | Caso | 26 |
| El Raigosu | Laviana | 26 |
| Forêt de Colunga (9) | Colunga | 26 |
| Forêt de Aller (29) | Aller | 26 |
| Forêt de Ponga (29) | Ponga | 26 |
| Forêt de Cudillero (24) | Cudillero | 26 |
| Forêt de Bimenes (8) | Bimenes | 26 |
| Forêt de Cangas del Narcea (83) | Cangas del Narcea | 26 |
| Forêt de Tineo (91) | Tineo | 26 |
| Forêt de Oviedo (42) | Oviedo | 26 |
| Forêt de Oviedo (43) | Oviedo | 26 |
| Forêt de Ribadesella (16) | Ribadesella | 26 |
| Forêt de Somiedo (41) | Somiedo | 26 |
| Forêt de Valdés (76) | Valdés | 26 |
| Forêt de Somiedo | Somiedo | 25 |
| Forêt de El Franco | El Franco | 25 |
| Forêt de Avilés (2) | Avilés | 25 |
| Forêt de Pravia (6) | Pravia | 25 |
| Forêt de Grado (4) | Grado | 25 |
| Forêt de Siero (7) | Siero | 25 |
| Forêt de Tineo (17) | Tineo | 25 |
| Forêt de Llanes (9) | Llanes | 25 |
| Forêt de Ribadesella (3) | Ribadesella | 25 |
| Forêt de Boal (8) | Boal | 25 |
| Forêt de Tapia de Casariego (4) | Tapia de Casariego | 25 |
| Forêt de Grado (12) | Grado | 25 |
| Forêt de Parres (5) | Parres | 25 |
| Forêt de San Martín de Oscos (5) | San Martín de Oscos | 25 |
| Forêt de Siero (19) | Siero | 25 |
| Forêt de Cabranes (4) | Cabranes | 25 |
| Forêt de Llanes (16) | Llanes | 25 |
| Forêt de Caso (28) | Caso | 25 |
| Forêt de Coaña (8) | Coaña | 25 |
| Forêt de Llanes (19) | Llanes | 25 |
| Forêt de Piloña (48) | Piloña | 25 |
| Forêt de Santo Adriano (5) | Santo Adriano | 25 |
| Forêt de Piloña (50) | Piloña | 25 |
| Forêt de Oviedo (36) | Oviedo | 25 |
| Forêt de Grandas de Salime (28) | Grandas de Salime | 25 |
| Forêt de Tineo (85) | Tineo | 25 |
| Forêt de Cangas del Narcea (79) | Cangas del Narcea | 25 |
| Forêt de Valdés (55) | Valdés | 25 |
| Forêt de Castropol (15) | Castropol | 25 |
| Forêt de Somiedo (32) | Somiedo | 25 |
| Forêt de Coaña (10) | Coaña | 25 |
| Forêt de Proaza (5) | Proaza | 25 |
| Forêt de Caso (48) | Caso | 25 |
| Forêt de Riosa (6) | Riosa | 25 |
| Forêt de Cangas del Narcea (117) | Cangas del Narcea | 25 |
| Forêt de Mieres (27) | Mieres | 25 |
| Forêt de Taramundi (44) | Taramundi | 25 |
| Bois de Proaza (2) | Proaza | 25 |
| Forêt de Valdés (405) | Valdés | 25 |
| Forêt de Cangas de Onís (6) | Cangas de Onís | 24 |
| Forêt de Lena (3) | Lena | 24 |
| Forêt de Tineo (11) | Tineo | 24 |
| Forêt de Ponga (8) | Ponga | 24 |
| Forêt de Villayón (2) | Villayón | 24 |
| Forêt de Las Regueras (4) | Las Regueras | 24 |
| Forêt de Cudillero (12) | Cudillero | 24 |
| Forêt de Tineo (38) | Tineo | 24 |
| Forêt de Boal (13) | Boal | 24 |
| Forêt de Villayón (10) | Villayón | 24 |
| Forêt de Allande (17) | Allande | 24 |
| Forêt de Cudillero (19) | Cudillero | 24 |
| Forêt de Lena (15) | Lena | 24 |
| Forêt de Caso (25) | Caso | 24 |
| Forêt de Villaviciosa (31) | Villaviciosa | 24 |
| Forêt de Aller (24) | Aller | 24 |
| Forêt de Grado (20) | Grado | 24 |
| Forêt de Soto del Barco (5) | Soto del Barco | 24 |
| Forêt de Salas (28) | Salas | 24 |
| Forêt de Valdés (42) | Valdés | 24 |
| Forêt de Lena (19) | Lena | 24 |
| Forêt de Tineo (79) | Tineo | 24 |
| Forêt de Parres (21) | Parres | 24 |
| Forêt de Boal (25) | Boal | 24 |
| Forêt de Tineo (94) | Tineo | 24 |
| Forêt de Villayón (20) | Villayón | 24 |
| Forêt de Ibias (29) | Ibias | 24 |
| Forêt de Morcín (8) | Morcín | 24 |
| Forêt de Somiedo (38) | Somiedo | 24 |
| Forêt de Llanes (27) | Llanes | 24 |
| Forêt de Parres (25) | Parres | 24 |
| Forêt de Illas (3) | Illas | 24 |
| Forêt de Colunga (14) | Colunga | 24 |
| Bois de Taramundi (10) | Taramundi | 24 |
| Forêt de Taramundi (60) | Taramundi | 24 |
| Forêt de Lena (40) | Lena | 24 |
| Forêt de Grado | Grado | 23 |
| Forêt de Laviana (2) | Laviana | 23 |
| Forêt de Caso (7) | Caso | 23 |
| Forêt de Llanes (11) | Llanes | 23 |
| Forêt de Aller (11) | Aller | 23 |
| Forêt de Laviana (11) | Laviana | 23 |
| Forêt de Salas (21) | Salas | 23 |
| Forêt de Laviana (13) | Laviana | 23 |
| Forêt de Sobrescobio (7) | Sobrescobio | 23 |
| Forêt de Peñamellera Alta (9) | Peñamellera Alta | 23 |
| Forêt de Yernes y Tameza | Yernes y Tameza | 23 |
| Forêt de Las Regueras (10) | Las Regueras | 23 |
| Forêt de Langreo (17) | Langreo | 23 |
| Forêt de Siero (23) | Siero | 23 |
| Forêt de Morcín (5) | Morcín | 23 |
| Forêt de Cangas del Narcea (75) | Cangas del Narcea | 23 |
| Forêt de Ibias (22) | Ibias | 23 |
| Forêt de Degaña (18) | Degaña | 23 |
| Forêt de Ribadedeva (6) | Ribadedeva | 23 |
| Forêt de Grado (30) | Grado | 23 |
| Forêt de Tineo (105) | Tineo | 23 |
| Forêt de Quirós (35) | Quirós | 23 |
| Forêt de Tineo (108) | Tineo | 23 |
| Forêt de Villayón (24) | Villayón | 23 |
| Forêt de Villaviciosa (66) | Villaviciosa | 23 |
| Forêt de Llanes (43) | Llanes | 23 |
| Forêt de Tineo (953) | Tineo | 23 |
| Forêt de Allande (2) | Allande | 22 |
| Forêt de Caso (2) | Caso | 22 |
| Forêt de Ponga (4) | Ponga | 22 |
| Forêt de Piloña (6) | Piloña | 22 |
| Forêt de Castropol | Castropol | 22 |
| Forêt de Siero (6) | Siero | 22 |
| Forêt de Ribera de Arriba (2) | Ribera de Arriba | 22 |
| Forêt de Cangas del Narcea (18) | Cangas del Narcea | 22 |
| Forêt de Aller (7) | Aller | 22 |
| Forêt de Salas (13) | Salas | 22 |
| Forêt de Gozón (5) | Gozón | 22 |
| Forêt de Cangas del Narcea (37) | Cangas del Narcea | 22 |
| Forêt de Grandas de Salime (18) | Grandas de Salime | 22 |
| Forêt de Somiedo (16) | Somiedo | 22 |
| Forêt de Cangas de Onís (20) | Cangas de Onís | 22 |
| Forêt de Villayón (11) | Villayón | 22 |
| Forêt de Aller (26) | Aller | 22 |
| Forêt de Ponga (26) | Ponga | 22 |
| Forêt de Sariego (3) | Sariego | 22 |
| Forêt de Ibias (21) | Ibias | 22 |
| Forêt de Caso (44) | Caso | 22 |
| Forêt de Villanueva de Oscos (8) | Villanueva de Oscos | 22 |
| Forêt de Vegadeo (13) | Vegadeo | 22 |
| Forêt de Ribadesella (15) | Ribadesella | 22 |
| Forêt de Cangas del Narcea (92) | Cangas del Narcea | 22 |
| Forêt de Aller (52) | Aller | 22 |
| Forêt de Laviana (34) | Laviana | 22 |
| Forêt de Pravia (48) | Pravia | 22 |
| Forêt de Ribadedeva (9) | Ribadedeva | 22 |
| Bois de Villanueva de Oscos | Villanueva de Oscos | 22 |
| Forêt de Sobrescobio (2) | Sobrescobio | 21 |
| Bosque de la Zoreda | Oviedo | 21 |
| Forêt de Somiedo (6) | Somiedo | 21 |
| Forêt de Somiedo (7) | Somiedo | 21 |
| Forêt de Llanes (8) | Llanes | 21 |
| Forêt de Caso (10) | Caso | 21 |
| Forêt de Pravia (15) | Pravia | 21 |
| Forêt de Ribadesella (6) | Ribadesella | 21 |
| Forêt de Belmonte de Miranda (8) | Belmonte de Miranda | 21 |
| Forêt de Peñamellera Baja (16) | Peñamellera Baja | 21 |
| Forêt de Belmonte de Miranda (9) | Belmonte de Miranda | 21 |
| Forêt de Mieres (17) | Mieres | 21 |
| Forêt de Gijón (37) | Gijón | 21 |
| Forêt de San Martín de Oscos (6) | San Martín de Oscos | 21 |
| Forêt de Allande (25) | Allande | 21 |
| Forêt de Illano (10) | Illano | 21 |
| Forêt de Grandas de Salime (23) | Grandas de Salime | 21 |
| Forêt de Cudillero (21) | Cudillero | 21 |
| Forêt de Cangas del Narcea (73) | Cangas del Narcea | 21 |
| Forêt de Villaviciosa (42) | Villaviciosa | 21 |
| Forêt de Oviedo (35) | Oviedo | 21 |
| Forêt de Santa Eulalia de Oscos (14) | Santa Eulalia de Oscos | 21 |
| Forêt de Grado (26) | Grado | 21 |
| Forêt de Tineo (84) | Tineo | 21 |
| Forêt de Illano (15) | Illano | 21 |
| Forêt de Ibias (24) | Ibias | 21 |
| Forêt de Tineo (90) | Tineo | 21 |
| Forêt de Tineo (102) | Tineo | 21 |
| Forêt de Grandas de Salime (31) | Grandas de Salime | 21 |
| Forêt de Cangas del Narcea (96) | Cangas del Narcea | 21 |
| Forêt de Villayón (23) | Villayón | 21 |
| Forêt de Cangas de Onís (33) | Cangas de Onís | 21 |
| Forêt de Somiedo (39) | Somiedo | 21 |
| Forêt de Valdés (74) | Valdés | 21 |
| Forêt de Valdés (87) | Valdés | 21 |
| Bois de Allande (15) | Allande | 21 |
| Forêt de Ribadedeva (14) | Ribadedeva | 21 |
| Forêt de Cabrales (212) | Cabrales | 21 |
| Forêt de Cudillero | Cudillero | 20 |
| Forêt de Cudillero (2) | Cudillero | 20 |
| Forêt de Cangas del Narcea (4) | Cangas del Narcea | 20 |
| Forêt de Grandas de Salime (11) | Grandas de Salime | 20 |
| Forêt de Villaviciosa (2) | Villaviciosa | 20 |
| Forêt de Llanes (2) | Llanes | 20 |
| Forêt de Piloña (7) | Piloña | 20 |
| Forêt de Ribadesella | Ribadesella | 20 |
| Forêt de Nava (3) | Nava | 20 |
| Forêt de Cabranes (2) | Cabranes | 20 |
| Forêt de Cangas del Narcea (26) | Cangas del Narcea | 20 |
| Forêt de Salas (10) | Salas | 20 |
| Forêt de Cabrales (3) | Cabrales | 20 |
| Forêt de Villanueva de Oscos (4) | Villanueva de Oscos | 20 |
| Forêt de Samartín del Rei Aurelio (2) | Samartín del Rei Aurelio | 20 |
| Forêt de Cangas del Narcea (44) | Cangas del Narcea | 20 |
| Forêt de Riosa (2) | Riosa | 20 |
| Forêt de Piloña (30) | Piloña | 20 |
| Forêt de Belmonte de Miranda (10) | Belmonte de Miranda | 20 |
| Forêt de Ribadesella (8) | Parres | 20 |
| Forêt de Cangas de Onís (22) | Cangas de Onís | 20 |
| Forêt de Grandas de Salime (21) | Grandas de Salime | 20 |
| Forêt de El Franco (15) | El Franco | 20 |
| Forêt de Aller (33) | Aller | 20 |
| Forêt de Parres (15) | Parres | 20 |
| Forêt de Salas (30) | Salas | 20 |
| Bois de Morcín | Morcín | 20 |
| Forêt de Cangas de Onís (27) | Cangas de Onís | 20 |
| Forêt de Aller (36) | Aller | 20 |
| Forêt de Parres (19) | Parres | 20 |
| Forêt de Caso (36) | Caso | 20 |
| Forêt de Ponga (33) | Ponga | 20 |
| Forêt de Tineo (103) | Tineo | 20 |
| Forêt de Laviana (35) | Laviana | 20 |
| Forêt de Coaña (12) | Coaña | 20 |
| Bois de Morcín (2) | Morcín | 20 |
| Bois de Peñamellera Baja (11) | Peñamellera Baja | 20 |
| Forêt de Coaña (45) | Coaña | 20 |
| Bois de Cabrales (28) | Cabrales | 20 |
| Forêt de Siero (2) | Siero | 19 |
| Forêt de Ribadesella (2) | Ribadesella | 19 |
| Forêt de Somiedo (2) | Somiedo | 19 |
| Forêt de Aller (4) | Aller | 19 |
| Forêt de Villaviciosa (10) | Villaviciosa | 19 |
| Forêt de Tineo (15) | Tineo | 19 |
| Forêt de Valdés (13) | Valdés | 19 |
| Forêt de Oviedo (22) | Oviedo | 19 |
| Forêt de Gijón (25) | Gijón | 19 |
| Forêt de Gozón (3) | Gozón | 19 |
| Forêt de Llanes (12) | Llanes | 19 |
| Forêt de Tineo (41) | Tineo | 19 |
| Forêt de Bimenes (3) | Bimenes | 19 |
| Forêt de Taramundi (11) | Taramundi | 19 |
| Forêt de Caso (19) | Caso | 19 |
| Forêt de Cangas del Narcea (51) | Cangas del Narcea | 19 |
| Forêt de Cangas del Narcea (56) | Cangas del Narcea | 19 |
| Forêt de Morcín (4) | Morcín | 19 |
| Forêt de Tineo (53) | Tineo | 19 |
| Forêt de Salas (26) | Salas | 19 |
| Forêt de Grado (21) | Grado | 19 |
| Forêt de Valdés (37) | Valdés | 19 |
| Forêt de Cangas de Onís (24) | Cangas de Onís | 19 |
| Forêt de Valdés (43) | Valdés | 19 |
| Forêt de Villaviciosa (41) | Villaviciosa | 19 |
| Forêt de Lena (18) | Lena | 19 |
| Forêt de Tineo (75) | Tineo | 19 |
| Forêt de Cangas del Narcea (87) | Cangas del Narcea | 19 |
| Forêt de Ibias (25) | Ibias | 19 |
| Forêt de Boal (27) | Boal | 19 |
| Forêt de Mieres (24) | Mieres | 19 |
| Forêt de Sariego (4) | Sariego | 19 |
| Forêt de Cabrales (10) | Cabrales | 19 |
| Forêt de Muros de Nalón | Muros de Nalón | 19 |
| Forêt de Grandas de Salime (33) | Grandas de Salime | 19 |
| Forêt de Belmonte de Miranda (28) | Belmonte de Miranda | 19 |
| Forêt de Samartín del Rei Aurelio (7) | Samartín del Rei Aurelio | 19 |
| Forêt de Cudillero (50) | Cudillero | 19 |
| Forêt de Onís (4) | Onís | 19 |
| Forêt de Onís (21) | Onís | 19 |
| Bois de Quirós (9) | Quirós | 19 |
| Bois de Quirós (11) | Quirós | 19 |
| Forêt de Cangas del Narcea (120) | Cangas del Narcea | 19 |
| Bois de Llanes (72) | Llanes | 19 |
| Forêt de Taramundi (4) | Taramundi | 18 |
| Forêt de Ibias (6) | Ibias | 18 |
| Forêt de Oviedo (18) | Oviedo | 18 |
| Forêt de Llanera (7) | Llanera | 18 |
| Forêt de Las Regueras | Las Regueras | 18 |
| Forêt de Cangas del Narcea (24) | Cangas del Narcea | 18 |
| Forêt de Salas (8) | Salas | 18 |
| Forêt de Vegadeo (5) | Vegadeo | 18 |
| Forêt de Valdés (15) | Valdés | 18 |
| Forêt de Belmonte de Miranda (5) | Belmonte de Miranda | 18 |
| Forêt de Llanes (10) | Llanes | 18 |
| Forêt de Oviedo (24) | Oviedo | 18 |
| Forêt de Gijón (28) | Gijón | 18 |
| Forêt de Villayón (6) | Villayón | 18 |
| Forêt de Peñamellera Baja (14) | Peñamellera Baja | 18 |
| Forêt de Navia (3) | Navia | 18 |
| Forêt de Piloña (29) | Piloña | 18 |
| Forêt de Boal (14) | Boal | 18 |
| Forêt de Langreo (13) | Langreo | 18 |
| Forêt de Piloña (34) | Piloña | 18 |
| Forêt de Castrillón (7) | Castrillón | 18 |
| Forêt de Allande (21) | Allande | 18 |
| Forêt de Llanes (17) | Llanes | 18 |
| Forêt de Allande (23) | Allande | 18 |
| Forêt de Corvera de Asturias (6) | Corvera de Asturias | 18 |
| Forêt de Gozón (8) | Gozón | 18 |
| Forêt de Belmonte de Miranda (16) | Belmonte de Miranda | 18 |
| Forêt de Tineo (80) | Tineo | 18 |
| Forêt de Somiedo (29) | Somiedo | 18 |
| Forêt de Pravia (33) | Pravia | 18 |
| Forêt de Ribadedeva (5) | Ribadedeva | 18 |
| Forêt de Laviana (29) | Laviana | 18 |
| Forêt de Villaviciosa (53) | Villaviciosa | 18 |
| Forêt de Tineo (100) | Tineo | 18 |
| Forêt de Tineo (101) | Tineo | 18 |
| Forêt de Carreño (10) | Carreño | 18 |
| Forêt de Ribadesella (18) | Ribadesella | 18 |
| Forêt de Valdés (67) | Valdés | 18 |
| Forêt de Proaza (6) | Proaza | 18 |
| Forêt de Cangas del Narcea (109) | Cangas del Narcea | 18 |
| Sauceda de Buelles | Peñamellera Baja | 18 |
| Forêt de Colunga (16) | Colunga | 18 |
| Forêt de Tapia de Casariego (16) | Tapia de Casariego | 18 |
| Forêt de Cabrales (37) | Cabrales | 18 |
| Forêt de Cudillero (57) | Cudillero | 18 |
| Forêt de Peñamellera Alta (18) | Peñamellera Alta | 18 |
| Forêt de Llanera | Llanera | 17 |
| Forêt de Santo Adriano | Santo Adriano | 17 |
| Forêt de Cudillero (5) | Cudillero | 17 |
| Forêt de Tineo (10) | Tineo | 17 |
| Forêt de Caso (5) | Caso | 17 |
| Forêt de Grado (6) | Grado | 17 |
| Forêt de Somiedo (5) | Somiedo | 17 |
| Forêt de Bimenes (2) | Bimenes | 17 |
| Forêt de Peñamellera Baja (10) | Peñamellera Baja | 17 |
| Forêt de Grado (9) | Grado | 17 |
| Forêt de Parres (3) | Parres | 17 |
| Forêt de Vegadeo (7) | Vegadeo | 17 |
| Forêt de Teverga (6) | Teverga | 17 |
| Forêt de Oviedo (26) | Oviedo | 17 |
| Forêt de Tineo (39) | Tineo | 17 |
| Forêt de Tineo (43) | Tineo | 17 |
| Forêt de Caso (18) | Caso | 17 |
| Forêt de Villaviciosa (25) | Villaviciosa | 17 |
| Forêt de Castrillón (4) | Castrillón | 17 |
| Forêt de Belmonte de Miranda (7) | Belmonte de Miranda | 17 |
| Forêt de Valdés (27) | Valdés | 17 |
| Forêt de Cangas del Narcea (62) | Cangas del Narcea | 17 |
| Forêt de Salas (25) | Salas | 17 |
| Forêt de Tineo (64) | Tineo | 17 |
| Forêt de Parres (16) | Parres | 17 |
| Forêt de Piloña (52) | Piloña | 17 |
| Forêt de Parres (17) | Parres | 17 |
| Forêt de Valdés (48) | Valdés | 17 |
| Forêt de Belmonte de Miranda (19) | Belmonte de Miranda | 17 |
| Forêt de Tineo (86) | Tineo | 17 |
| Forêt de Teverga (11) | Teverga | 17 |
| Forêt de Mieres (23) | Mieres | 17 |
| Forêt de Degaña (20) | Degaña | 17 |
| Forêt de San Martín de Oscos (9) | San Martín de Oscos | 17 |
| Forêt de Cudillero (51) | Cudillero | 17 |
| Forêt de Gijón (54) | Gijón | 17 |
| Forêt de Langreo (57) | Langreo | 17 |
| Bois de Allande (8) | Allande | 17 |
| Forêt de Cangas de Onís (114) | Cangas de Onís | 17 |
| Forêt de Cabrales (211) | Cabrales | 17 |
| Forêt de Piloña (5) | Piloña | 16 |
| Forêt de Villaviciosa (3) | Villaviciosa | 16 |
| Forêt de Villanueva de Oscos | Villanueva de Oscos | 16 |
| Bois de Villaviciosa | Villaviciosa | 16 |
| Forêt de Piloña (9) | Piloña | 16 |
| Forêt de Lena (2) | Lena | 16 |
| Forêt de Grandas de Salime (13) | Grandas de Salime | 16 |
| Forêt de Boal (3) | Boal | 16 |
| Forêt de Aller (6) | Aller | 16 |
| Forêt de Carreño | Carreño | 16 |
| Forêt de Grado (8) | Grado | 16 |
| Forêt de Siero (9) | Siero | 16 |
| Forêt de Siero (12) | Siero | 16 |
| Forêt de El Franco (5) | El Franco | 16 |
| Forêt de Villayón (5) | Villayón | 16 |
| Forêt de Somiedo (8) | Somiedo | 16 |
| Forêt de Vegadeo (6) | Vegadeo | 16 |
| Forêt de Illano (6) | Illano | 16 |
| Forêt de Cangas de Onís (15) | Cangas de Onís | 16 |
| Forêt de Parres (4) | Parres | 16 |
| Forêt de Amieva (4) | Amieva | 16 |
| Forêt de Laviana (10) | Laviana | 16 |
| Forêt de Cangas de Onís (19) | Cangas de Onís | 16 |
| Forêt de Ibias (17) | Ibias | 16 |
| Forêt de Cangas del Narcea (65) | Cangas del Narcea | 16 |
| Forêt de Parres (11) | Parres | 16 |
| Forêt de Cabranes (5) | Cabranes | 16 |
| Forêt de Ponga (27) | Ponga | 16 |
| Forêt de Cangas de Onís (26) | Cangas de Onís | 16 |
| Forêt de Yernes y Tameza (2) | Yernes y Tameza | 16 |
| Forêt de San Tirso de Abres (7) | San Tirso de Abres | 16 |
| Forêt de Castropol (12) | Castropol | 16 |
| Forêt de Ponga (30) | Ponga | 16 |
| Forêt de Oviedo (39) | Oviedo | 16 |
| Forêt de Cabranes (10) | Cabranes | 16 |
| Forêt de Ibias (28) | Ibias | 16 |
| Forêt de Parres (23) | Parres | 16 |
| Forêt de Grandas de Salime (32) | Grandas de Salime | 16 |
| Forêt de Cangas del Narcea (108) | Cangas del Narcea | 16 |
| Forêt de Siero (36) | Siero | 16 |
| Forêt de Valdés (72) | Valdés | 16 |
| Forêt de Boal (29) | Boal | 16 |
| Forêt de Tineo (111) | Tineo | 16 |
| Forêt de Cudillero (40) | Cudillero | 16 |
| Bois de Taramundi (2) | Taramundi | 16 |
| Parque de Los Pericones | Gijón | 16 |
| Forêt de Parres (51) | Parres | 16 |
| Forêt de Caso (60) | Caso | 16 |
| Forêt de Cangas de Onís (3) | Cangas de Onís | 15 |
| Forêt de Cangas del Narcea (9) | Cangas del Narcea | 15 |
| Forêt de Parres | Parres | 15 |
| Forêt de Peñamellera Baja (7) | Peñamellera Baja | 15 |
| Forêt de Cangas de Onís (13) | Cangas de Onís | 15 |
| Forêt de Boal (9) | Boal | 15 |
| Monte Castiello | Cabrales | 15 |
| Forêt de Grandas de Salime (17) | Grandas de Salime | 15 |
| Forêt de Nava (12) | Nava | 15 |
| Forêt de Somiedo (20) | Somiedo | 15 |
| Forêt de Valdés (34) | Valdés | 15 |
| Forêt de Valdés (36) | Valdés | 15 |
| Forêt de Aller (23) | Aller | 15 |
| Forêt de Cangas del Narcea (68) | Cangas del Narcea | 15 |
| Forêt de Valdés (41) | Valdés | 15 |
| Forêt de Las Regueras (13) | Las Regueras | 15 |
| Forêt de Caso (30) | Caso | 15 |
| Forêt de Belmonte de Miranda (17) | Belmonte de Miranda | 15 |
| Forêt de Pravia (31) | Pravia | 15 |
| Forêt de Tineo (72) | Tineo | 15 |
| Forêt de Castropol (11) | Castropol | 15 |
| Forêt de Villayón (17) | Villayón | 15 |
| Forêt de Ribadesella (12) | Ribadesella | 15 |
| Forêt de Tineo (93) | Tineo | 15 |
| Forêt de Vegadeo (16) | Vegadeo | 15 |
| Forêt de Oviedo (47) | Oviedo | 15 |
| Forêt de Cangas del Narcea (104) | Cangas del Narcea | 15 |
| Forêt de Illano (23) | Illano | 15 |
| Forêt de Valdés (73) | Valdés | 15 |
| Forêt de Pravia (51) | Pravia | 15 |
| Forêt de Langreo (54) | Langreo | 15 |
| Forêt de Oviedo (56) | Oviedo | 15 |
| Forêt de Valdés (131) | Valdés | 15 |
| Forêt de Candamo (10) | Candamo | 15 |
| Forêt de Cabrales (149) | Cabrales | 15 |
| Forêt de Villanueva de Oscos (10) | Villanueva de Oscos | 15 |
| Bois de Pravia (2) | Pravia | 15 |
| Bois de Quirós (15) | Quirós | 15 |
| Forêt de Peñamellera Baja (25) | Peñamellera Baja | 15 |
| Forêt de Tineo (956) | Tineo | 15 |
| Forêt de Villaviciosa | Villaviciosa | 14 |
| Forêt de Tineo (3) | Tineo | 14 |
| Forêt de Tineo (5) | Tineo | 14 |
| Forêt de Mieres (2) | Mieres | 14 |
| Forêt de Cangas del Narcea (13) | Cangas del Narcea | 14 |
| Forêt de Cudillero (6) | Cudillero | 14 |
| Forêt de Tapia de Casariego | Tapia de Casariego | 14 |
| Forêt de Villaviciosa (17) | Gijón | 14 |
| Forêt de Ribadedeva (2) | Ribadedeva | 14 |
| Forêt de Tineo (23) | Tineo | 14 |
| Forêt de Tineo (24) | Tineo | 14 |
| Forêt de Castropol (5) | Castropol | 14 |
| Forêt de Valdés (22) | Valdés | 14 |
| Forêt de Allande (13) | Allande | 14 |
| Forêt de Llanes (15) | Llanes | 14 |
| Forêt de Taramundi (12) | Taramundi | 14 |
| Forêt de Corvera de Asturias (4) | Corvera de Asturias | 14 |
| Forêt de Tineo (46) | Tineo | 14 |
| Forêt de Somiedo (23) | Somiedo | 14 |
| Forêt de Tineo (59) | Tineo | 14 |
| Forêt de Ponga (23) | Ponga | 14 |
| Forêt de Oviedo (32) | Oviedo | 14 |
| Forêt de Piloña (44) | Piloña | 14 |
| Forêt de Tapia de Casariego (10) | Tapia de Casariego | 14 |
| Forêt de Caso (31) | Caso | 14 |
| Forêt de Tineo (71) | Tineo | 14 |
| Forêt de Las Regueras (16) | Las Regueras | 14 |
| Forêt de Caso (38) | Caso | 14 |
| Forêt de Caso (40) | Caso | 14 |
| Forêt de Belmonte de Miranda (20) | Belmonte de Miranda | 14 |
| Forêt de Allande (31) | Allande | 14 |
| Forêt de Somiedo (31) | Somiedo | 14 |
| Forêt de Cangas del Narcea (89) | Cangas del Narcea | 14 |
| Forêt de Llanes (24) | Llanes | 14 |
| Forêt de Somiedo (35) | Somiedo | 14 |
| Forêt de Peñamellera Baja (19) | Peñamellera Baja | 14 |
| Forêt de Llanera (20) | Llanera | 14 |
| Forêt de Navia (5) | Navia | 14 |
| Forêt de Aller (50) | Aller | 14 |
| Forêt de Caso (49) | Caso | 14 |
| Forêt de Cangas del Narcea (106) | Cangas del Narcea | 14 |
| Forêt de Tapia de Casariego (13) | Tapia de Casariego | 14 |
| Bois de Santo Adriano | Santo Adriano | 14 |
| Forêt de Cangas de Onís (46) | Cangas de Onís | 14 |
| Forêt de Onís (7) | Onís | 14 |
| Bois de Tineo (2) | Tineo | 14 |
| Forêt de Noreña | Noreña | 14 |
| Parque fluvial del Rio Piles | Gijón | 14 |
| Forêt de Oviedo (83) | Oviedo | 14 |
| Bois de Llanes (33) | Llanes | 14 |
| Bois de Llanes (65) | Llanes | 14 |
| Parque de Invierno | Oviedo | 13 |
| Forêt de Oviedo (16) | Oviedo | 13 |
| Forêt de Cangas de Onís | Cangas de Onís | 13 |
| Forêt de Cangas de Onís (2) | Cangas de Onís | 13 |
| Forêt de Amieva | Amieva | 13 |
| Forêt de Caso (4) | Caso | 13 |
| Forêt de Oviedo (21) | Oviedo | 13 |
| Forêt de Tineo (16) | Tineo | 13 |
| Forêt de Caso (9) | Caso | 13 |
| Forêt de Gozón (2) | Gozón | 13 |
| Forêt de Allande (10) | Allande | 13 |
| Forêt de Cabrales (6) | Cabrales | 13 |
| Forêt de Siero (15) | Siero | 13 |
| Forêt de Cangas del Narcea (39) | Cangas del Narcea | 13 |
| Forêt de El Franco (7) | El Franco | 13 |
| Forêt de Villaviciosa (24) | Villaviciosa | 13 |
| Forêt de Grado (15) | Grado | 13 |
| Forêt de Castrillón (6) | Castrillón | 13 |
| Forêt de Cangas del Narcea (60) | Cangas del Narcea | 13 |
| Forêt de Santo Adriano (3) | Santo Adriano | 13 |
| Forêt de Boal (17) | Boal | 13 |
| Forêt de Pravia (25) | Pravia | 13 |
| Forêt de Piloña (37) | Piloña | 13 |
| Forêt de Quirós (19) | Quirós | 13 |
| Forêt de Llanes (18) | Llanes | 13 |
| Forêt de Pravia (28) | Pravia | 13 |
| Forêt de Aller (32) | Aller | 13 |
| Forêt de Bimenes (7) | Bimenes | 13 |
| Forêt de Quirós (27) | Quirós | 13 |
| Forêt de Parres (18) | Parres | 13 |
| Forêt de Aller (37) | Aller | 13 |
| Forêt de Valdés (51) | Valdés | 13 |
| Forêt de Villayón (19) | Villayón | 13 |
| Forêt de Cabrales (9) | Cabrales | 13 |
| Forêt de Teverga (10) | Teverga | 13 |
| Forêt de Soto del Barco (7) | Soto del Barco | 13 |
| Forêt de Cangas del Narcea (94) | Cangas del Narcea | 13 |
| Forêt de Illano (16) | Illano | 13 |
| Forêt de Grado (32) | Grado | 13 |
| Forêt de Cangas de Onís (37) | Cangas de Onís | 13 |
| Forêt de Caso (51) | Caso | 13 |
| Forêt de Cabranes (11) | Cabranes | 13 |
| Bois de Langreo (31) | Langreo | 13 |
| Forêt de Valdés (116) | Valdés | 13 |
| Forêt de Cangas de Onís (42) | Cangas de Onís | 13 |
| Forêt de Morcín (9) | Morcín | 13 |
| Forêt de Grandas de Salime (43) | Grandas de Salime | 13 |
| Bois de Caso (2) | Caso | 13 |
| Forêt de Cabrales (89) | Cabrales | 13 |
| Bois de Villanueva de Oscos (3) | Villanueva de Oscos | 13 |
| Forêt de Onís (13) | Onís | 13 |
| Forêt de Onís (20) | Onís | 13 |
| Bois de Teverga (3) | Teverga | 13 |
| Forêt de Tineo (210) | Tineo | 13 |
| Parque de La Cebera | Siero | 13 |
| Forêt de Aller | Aller | 12 |
| Forêt de Piloña (3) | Piloña | 12 |
| Forêt de Allande (4) | Allande | 12 |
| Forêt de Peñamellera Alta (3) | Peñamellera Alta | 12 |
| Forêt de Ribera de Arriba | Ribera de Arriba | 12 |
| Forêt de Mieres (4) | Mieres | 12 |
| Forêt de Santa Eulalia de Oscos (8) | Santa Eulalia de Oscos | 12 |
| Forêt de Villayón (3) | Villayón | 12 |
| Forêt de Cudillero (11) | Cudillero | 12 |
| Forêt de Laviana (8) | Laviana | 12 |
| Forêt de Grandas de Salime (19) | Grandas de Salime | 12 |
| Forêt de Tineo (50) | Tineo | 12 |
| Forêt de Cangas de Onís (23) | Cangas de Onís | 12 |
| Forêt de Villayón (14) | Villayón | 12 |
| Forêt de Tineo (65) | Tineo | 12 |
| Forêt de Ribadedeva (4) | Ribadedeva | 12 |
| Forêt de Llanes (20) | Llanes | 12 |
| Forêt de Piloña (54) | Piloña | 12 |
| Forêt de Aller (38) | Aller | 12 |
| Forêt de Aller (39) | Aller | 12 |
| Forêt de Tineo (81) | Tineo | 12 |
| Forêt de Villaviciosa (49) | Villaviciosa | 12 |
| Forêt de Vegadeo (14) | Vegadeo | 12 |
| Forêt de Tineo (106) | Tineo | 12 |
| Forêt de Valdés (62) | Valdés | 12 |
| Forêt de Cudillero (34) | Cudillero | 12 |
| Forêt de Ibias (30) | Ibias | 12 |
| Forêt de Pravia (47) | Pravia | 12 |
| Forêt de Cangas de Onís (38) | Cangas de Onís | 12 |
| Forêt de Valdés (82) | Valdés | 12 |
| Bois de Langreo (27) | Langreo | 12 |
| Forêt de El Franco (26) | El Franco | 12 |
| Forêt de Coaña (25) | Coaña | 12 |
| Forêt de Villaviciosa (75) | Villaviciosa | 12 |
| Forêt de Peñamellera Alta (16) | Peñamellera Alta | 12 |
| Bois de Oviedo (46) | Oviedo | 12 |
| Bois de Siero (8) | Siero | 12 |
| Forêt de Onís (46) | Onís | 12 |
| Forêt de Valdés (264) | Valdés | 12 |
| Forêt de Ribadesella (74) | Ribadesella | 12 |
| Bois de Llanes (73) | Llanes | 12 |
| Bois de Llanes (94) | Llanes | 12 |
| Forêt de Valdés (3) | Valdés | 11 |
| Forêt de Taramundi (6) | Taramundi | 11 |
| Forêt de Quirós (6) | Quirós | 11 |
| Forêt de Valdés (12) | Valdés | 11 |
| Forêt de Villaviciosa (14) | Villaviciosa | 11 |
| Forêt de Tineo (22) | Tineo | 11 |
| Forêt de Grado (11) | Grado | 11 |
| Forêt de Mieres (12) | Mieres | 11 |
| Forêt de Boal (11) | Boal | 11 |
| Forêt de Tapia de Casariego (7) | Tapia de Casariego | 11 |
| Forêt de Quirós (22) | Quirós | 11 |
| Forêt de Llanera (16) | Llanera | 11 |
| Forêt de Oviedo (33) | Oviedo | 11 |
| Forêt de Piloña (53) | Piloña | 11 |
| Forêt de Gijón (41) | Gijón | 11 |
| Forêt de Colunga (10) | Colunga | 11 |
| Forêt de Taramundi (20) | Taramundi | 11 |
| Forêt de Gozón (12) | Gozón | 11 |
| Forêt de Ponga (41) | Ponga | 11 |
| Forêt de Langreo (29) | Langreo | 11 |
| Forêt de Valdés (104) | Valdés | 11 |
| Forêt de Taramundi (25) | Taramundi | 11 |
| Bois de Oviedo (54) | Oviedo | 11 |
| Forêt de Onís (30) | Onís | 11 |
| Bois de Somiedo | Somiedo | 11 |
| Bois de Oviedo (162) | Oviedo | 11 |
| Forêt de Valdés (187) | Valdés | 11 |
| Forêt de Oviedo (84) | Oviedo | 11 |
| Forêt de Cabrales | Cabrales | 10 |
| Forêt de Santa Eulalia de Oscos (7) | Santa Eulalia de Oscos | 10 |
| Forêt de Nava (2) | Nava | 10 |
| Forêt de Siero (5) | Siero | 10 |
| Forêt de Siero (10) | Siero | 10 |
| Forêt de Pesoz | Pesoz | 10 |
| Forêt de Navia (2) | Navia | 10 |
| Forêt de Ponga (18) | Ponga | 10 |
| Forêt de Cangas del Narcea (47) | Cangas del Narcea | 10 |
| Forêt de Lena (13) | Lena | 10 |
| Forêt de Tineo (60) | Tineo | 10 |
| Forêt de Caso (27) | Caso | 10 |
| Forêt de Villayón (15) | Villayón | 10 |
| Forêt de Caso (32) | Caso | 10 |
| Forêt de Nava (14) | Nava | 10 |
| Forêt de Las Regueras (17) | Las Regueras | 10 |
| Forêt de Oviedo (40) | Oviedo | 10 |
| Forêt de Cangas de Onís (31) | Cangas de Onís | 10 |
| Forêt de Valdés (90) | Valdés | 10 |
| Bosque del Payán (3) | Oviedo | 10 |
| Forêt de Valdés (101) | Valdés | 10 |
| Forêt de Oviedo (54) | Oviedo | 10 |
| Forêt de Gijón (78) | Gijón | 10 |
| Forêt de Gijón (79) | Gijón | 10 |
| Forêt de Villaviciosa (73) | Villaviciosa | 10 |
| Forêt de Onís (12) | Onís | 10 |
| Bois de Salas | Salas | 10 |
| Bois de Salas (3) | Salas | 10 |
| Bois de Allande (22) | Allande | 10 |
| Forêt de Tineo (455) | Tineo | 10 |
| Forêt de Llanera (31) | Llanera | 10 |
| Forêt de Cabrales (217) | Cabrales | 10 |
| Forêt de Navia (137) | Navia | 10 |
| Forêt de Oviedo (6) ⚠️ | Oviedo | 9 |
| Forêt de Salas (18) ⚠️ | Salas | 9 |
| Forêt de Tineo (49) ⚠️ | Tineo | 9 |
| Forêt de Las Regueras (12) ⚠️ | Las Regueras | 9 |
| Forêt de Aller (45) ⚠️ | Aller | 9 |
| Forêt de Caso (45) ⚠️ | Caso | 9 |
| Forêt de Valdés (80) ⚠️ | Valdés | 9 |
| Bois de Allande (4) ⚠️ | Allande | 9 |
| Bois de Langreo (20) ⚠️ | Langreo | 9 |
| Forêt de Ribadedeva (8) ⚠️ | Ribadedeva | 9 |
| Forêt de Amieva (10) ⚠️ | Amieva | 9 |
| Forêt de Valdés (121) ⚠️ | Valdés | 9 |
| Forêt de Caso (55) ⚠️ | Caso | 9 |
| Forêt de Villaviciosa (77) ⚠️ | Villaviciosa | 9 |
| Forêt de Cabrales (161) ⚠️ | Cabrales | 9 |
| Bois de Ponga (2) ⚠️ | Ponga | 9 |
| Bois de Piloña (3) ⚠️ | Piloña | 9 |
| Bois de Oviedo (88) ⚠️ | Oviedo | 9 |
| Forêt de Navia (134) ⚠️ | Navia | 9 |
| Forêt de Cabrales (218) ⚠️ | Cabrales | 9 |
| Bois de Llanes (46) ⚠️ | Llanes | 9 |
| Bois de Llanes (52) ⚠️ | Llanes | 9 |
| Bois de Llanes (64) ⚠️ | Llanes | 9 |
| Parque Purificación Tomás ⚠️ | Oviedo | 8 |
| Forêt de Gijón (18) ⚠️ | Gijón | 8 |
| Forêt de Llanes (3) ⚠️ | Llanes | 8 |
| Forêt de Aller (5) ⚠️ | Aller | 8 |
| Forêt de Gijón (32) ⚠️ | Gijón | 8 |
| Forêt de Pravia (19) ⚠️ | Pravia | 8 |
| Forêt de Ponga (19) ⚠️ | Ponga | 8 |
| Forêt de Valdés (97) ⚠️ | Valdés | 8 |
| Forêt de Navia (12) ⚠️ | Navia | 8 |
| Forêt de Langreo (53) ⚠️ | Langreo | 8 |
| Forêt de Villaviciosa (74) ⚠️ | Villaviciosa | 8 |
| Forêt de Cabrales (24) ⚠️ | Cabrales | 8 |
| Forêt de Lena (34) ⚠️ | Lena | 8 |
| Forêt de Cabrales (157) ⚠️ | Cabrales | 8 |
| Forêt de Cabrales (167) ⚠️ | Cabrales | 8 |
| Forêt de Onís (14) ⚠️ | Onís | 8 |
| Forêt de Onís (26) ⚠️ | Onís | 8 |
| Forêt de Onís (40) ⚠️ | Onís | 8 |
| Forêt de Onís (42) ⚠️ | Onís | 8 |
| Forêt de Onís (47) ⚠️ | Onís | 8 |
| Bois de Quirós (10) ⚠️ | Quirós | 8 |
| Bois de Llanes (30) ⚠️ | Llanes | 8 |
| Forêt de Tineo (449) ⚠️ | Tineo | 8 |
| Forêt de Tineo (491) ⚠️ | Tineo | 8 |
| Forêt de Valdés (188) ⚠️ | Valdés | 8 |
| Forêt de Somiedo (101) ⚠️ | Somiedo | 8 |
| Forêt de Cudillero (55) ⚠️ | Cudillero | 8 |
| Forêt de Coaña (44) ⚠️ | Coaña | 8 |
| Bois de Ribadesella (16) ⚠️ | Ribadesella | 8 |
| Parque del Oeste ⚠️ | Oviedo | 7 |
| Forêt de Oviedo (7) ⚠️ | Oviedo | 7 |
| Forêt de Avilés ⚠️ | Castrillón | 7 |
| Forêt de Cangas de Onís (9) ⚠️ | Cangas de Onís | 7 |
| Forêt de Cabrales (2) ⚠️ | Cabrales | 7 |
| Forêt de Piloña (25) ⚠️ | Piloña | 7 |
| Forêt de Carreño (6) ⚠️ | Carreño | 7 |
| Forêt de Cudillero (26) ⚠️ | Cudillero | 7 |
| Forêt de Oviedo (41) ⚠️ | Oviedo | 7 |
| Forêt de Piloña (60) ⚠️ | Piloña | 7 |
| Forêt de Cudillero (27) ⚠️ | Cudillero | 7 |
| Forêt de Pravia (38) ⚠️ | Pravia | 7 |
| Forêt de Piloña (65) ⚠️ | Piloña | 7 |
| Forêt de Carreño (11) ⚠️ | Carreño | 7 |
| Forêt de Cangas de Onís (36) ⚠️ | Cangas de Onís | 7 |
| Forêt de Siero (34) ⚠️ | Siero | 7 |
| Forêt de Nava (21) ⚠️ | Nava | 7 |
| Forêt de Coaña (38) ⚠️ | Coaña | 7 |
| Forêt de Somiedo (43) ⚠️ | Somiedo | 7 |
| Bois de Valdés (4) ⚠️ | Valdés | 7 |
| Forêt de Valdés (129) ⚠️ | Valdés | 7 |
| Monte Los Pedruizos ⚠️ | Lena | 7 |
| Forêt de Samartín del Rei Aurelio (12) ⚠️ | Samartín del Rei Aurelio | 7 |
| Forêt de Proaza (7) ⚠️ | Proaza | 7 |
| Forêt de Langreo (60) ⚠️ | Langreo | 7 |
| Bois de Aller (2) ⚠️ | Aller | 7 |
| Bois de Allande (12) ⚠️ | Allande | 7 |
| Bois de Laviana (2) ⚠️ | Laviana | 7 |
| Forêt de Cabrales (31) ⚠️ | Cabrales | 7 |
| Forêt de Cabrales (32) ⚠️ | Cabrales | 7 |
| Forêt de Cabrales (34) ⚠️ | Cabrales | 7 |
| Forêt de Taramundi (37) ⚠️ | Taramundi | 7 |
| Forêt de Cabrales (76) ⚠️ | Cabrales | 7 |
| Monte las Ḷḷevias ⚠️ | Lena | 7 |
| Forêt de Cudillero (52) ⚠️ | Cudillero | 7 |
| Forêt de Onís (6) ⚠️ | Onís | 7 |
| Bois de Tineo (3) ⚠️ | Tineo | 7 |
| Forêt de Villaviciosa (80) ⚠️ | Villaviciosa | 7 |
| Forêt de Cangas de Onís (115) ⚠️ | Cangas de Onís | 7 |
| Bois de Gijón (60) ⚠️ | Gijón | 7 |
| Forêt de Tineo (209) ⚠️ | Tineo | 7 |
| Forêt de Tineo (450) ⚠️ | Tineo | 7 |
| Forêt de Somiedo (166) ⚠️ | Somiedo | 7 |
| Forêt de Castropol (29) ⚠️ | Castropol | 7 |
| Forêt de Cangas de Onís (124) ⚠️ | Cangas de Onís | 7 |
| Parque de Isabel la Católica ⚠️ | Gijón | 7 |
| Forêt de Gijón (343) ⚠️ | Gijón | 7 |
| Forêt de Cangas de Onís (125) ⚠️ | Cangas de Onís | 7 |
| Forêt de Llanes (39) ⚠️ | Llanes | 7 |
| Bois de Llanes (31) ⚠️ | Llanes | 7 |
| Parc de Gijón (96) ⚠️ | Gijón | 7 |
| Parque del Cabo San Lorenzo ⚠️ | Gijón | 6 |
| Forêt de Gijón ⚠️ | Gijón | 6 |
| Forêt de Gijón (6) ⚠️ | Gijón | 6 |
| Forêt de Gijón (17) ⚠️ | Gijón | 6 |
| Forêt de Oviedo (2) ⚠️ | Oviedo | 6 |
| Forêt de Vegadeo ⚠️ | Vegadeo | 6 |
| Forêt de Gijón (22) ⚠️ | Gijón | 6 |
| Forêt de Oviedo (25) ⚠️ | Oviedo | 6 |
| Forêt de Caso (14) ⚠️ | Caso | 6 |
| Forêt de Belmonte de Miranda (6) ⚠️ | Belmonte de Miranda | 6 |
| Forêt de Oviedo (31) ⚠️ | Oviedo | 6 |
| Forêt de Taramundi (22) ⚠️ | Taramundi | 6 |
| Bosque del Payán (2) ⚠️ | Oviedo | 6 |
| Forêt de Cudillero (38) ⚠️ | Cudillero | 6 |
| Bois de Langreo (18) ⚠️ | Langreo | 6 |
| Forêt de Ribadedeva (12) ⚠️ | Ribadedeva | 6 |
| Forêt de Cabrales (12) ⚠️ | Cabrales | 6 |
| Forêt de Llanes (36) ⚠️ | Llanes | 6 |
| Forêt de Cangas del Narcea (119) ⚠️ | Cangas del Narcea | 6 |
| Forêt de Oviedo (62) ⚠️ | Oviedo | 6 |
| Bois de Cabrales (11) ⚠️ | Cabrales | 6 |
| Forêt de Villaviciosa (76) ⚠️ | Villaviciosa | 6 |
| Forêt de Villaviciosa (78) ⚠️ | Villaviciosa | 6 |
| Bois de Caso (3) ⚠️ | Caso | 6 |
| Bois de Allande (13) ⚠️ | Allande | 6 |
| Forêt de Gijón (91) ⚠️ | Gijón | 6 |
| Bois de Oviedo (45) ⚠️ | Oviedo | 6 |
| Forêt de Taramundi (27) ⚠️ | Taramundi | 6 |
| Forêt de Taramundi (34) ⚠️ | Taramundi | 6 |
| Forêt de Taramundi (45) ⚠️ | Taramundi | 6 |
| Forêt de Taramundi (49) ⚠️ | Taramundi | 6 |
| Forêt de Taramundi (55) ⚠️ | Taramundi | 6 |
| Forêt de Peñamellera Alta (15) ⚠️ | Peñamellera Alta | 6 |
| Forêt de Cabrales (85) ⚠️ | Cabrales | 6 |
| Forêt de Cabrales (121) ⚠️ | Cabrales | 6 |
| Forêt de Cabrales (146) ⚠️ | Cabrales | 6 |
| Forêt de Cabrales (164) ⚠️ | Cabrales | 6 |
| Forêt de Cabrales (176) ⚠️ | Cabrales | 6 |
| Bois de Ponga ⚠️ | Ponga | 6 |
| Forêt de Oviedo (76) ⚠️ | Oviedo | 6 |
| Forêt de Onís (28) ⚠️ | Onís | 6 |
| Bois de Quirós (3) ⚠️ | Quirós | 6 |
| Forêt de Onís (32) ⚠️ | Onís | 6 |
| Bois de Llanera (5) ⚠️ | Llanera | 6 |
| Bois de Oviedo (153) ⚠️ | Oviedo | 6 |
| Forêt de Proaza (8) ⚠️ | Proaza | 6 |
| Bois de Oviedo (225) ⚠️ | Oviedo | 6 |
| Forêt de Ribadesella (68) ⚠️ | Ribadesella | 6 |
| Forêt de Siero (52) ⚠️ | Siero | 6 |
| Bois de Las Regueras (3) ⚠️ | Las Regueras | 6 |
| Bois de Oviedo (232) ⚠️ | Oviedo | 6 |
| Forêt de Llanera (32) ⚠️ | Llanera | 6 |
| Forêt de Llanera (33) ⚠️ | Llanera | 6 |
| Parque de Moreda ⚠️ | Gijón | 5 |
| Forêt de Gijón (5) ⚠️ | Gijón | 5 |
| Forêt de Gijón (14) ⚠️ | Gijón | 5 |
| Forêt de Oviedo ⚠️ | Oviedo | 5 |
| Forêt de Quirós (4) ⚠️ | Quirós | 5 |
| Forêt de Ponga (5) ⚠️ | Ponga | 5 |
| Forêt de Grandas de Salime (14) ⚠️ | Grandas de Salime | 5 |
| Forêt de Piloña (14) ⚠️ | Piloña | 5 |
| Forêt de Cangas del Narcea (30) ⚠️ | Cangas del Narcea | 5 |
| Forêt de Santa Eulalia de Oscos (9) ⚠️ | Santa Eulalia de Oscos | 5 |
| Forêt de Villaviciosa (23) ⚠️ | Villaviciosa | 5 |
| Forêt de Ponga (22) ⚠️ | Ponga | 5 |
| Forêt de Langreo (21) ⚠️ | Langreo | 5 |
| Forêt de Oviedo (37) ⚠️ | Oviedo | 5 |
| Forêt de Candamo (7) ⚠️ | Candamo | 5 |
| Forêt de Pravia (41) ⚠️ | Pravia | 5 |
| Forêt de Ponga (39) ⚠️ | Ponga | 5 |
| Forêt de Piloña (70) ⚠️ | Piloña | 5 |
| Forêt de Ponga (40) ⚠️ | Ponga | 5 |
| Forêt de Oviedo (48) ⚠️ | Oviedo | 5 |
| Forêt de Valdés (83) ⚠️ | Valdés | 5 |
| Forêt de Oviedo (51) ⚠️ | Oviedo | 5 |
| Forêt de Llanes (30) ⚠️ | Llanes | 5 |
| Forêt de Ribadesella (21) ⚠️ | Ribadesella | 5 |
| Forêt de Llanes (33) ⚠️ | Llanes | 5 |
| Forêt de Ribadedeva (10) ⚠️ | Ribadedeva | 5 |
| Forêt de Ribadedeva (11) ⚠️ | Ribadedeva | 5 |
| Forêt de Cudillero (49) ⚠️ | Cudillero | 5 |
| Forêt de Gozón (18) ⚠️ | Gozón | 5 |
| Forêt de El Franco (48) ⚠️ | El Franco | 5 |
| Forêt de Coaña (35) ⚠️ | Coaña | 5 |
| Forêt de Navia (9) ⚠️ | Navia | 5 |
| Forêt de Cangas de Onís (45) ⚠️ | Cangas de Onís | 5 |
| Forêt de Grandas de Salime (44) ⚠️ | Grandas de Salime | 5 |
| Forêt de El Franco (53) ⚠️ | El Franco | 5 |
| Forêt de Gijón (65) ⚠️ | Gijón | 5 |
| Forêt de Gijón (67) ⚠️ | Gijón | 5 |
| Bois de Gijón (6) ⚠️ | Gijón | 5 |
| Forêt de Gijón (82) ⚠️ | Gijón | 5 |
| Forêt de Cabrales (18) ⚠️ | Cabrales | 5 |
| Forêt de Gijón (93) ⚠️ | Gijón | 5 |
| Forêt de Tineo (120) ⚠️ | Tineo | 5 |
| Forêt de Cabrales (46) ⚠️ | Cabrales | 5 |
| Forêt de Ponga (43) ⚠️ | Ponga | 5 |
| Forêt de Ponga (44) ⚠️ | Ponga | 5 |
| Bois de Taramundi (4) ⚠️ | Taramundi | 5 |
| Bois de Taramundi (9) ⚠️ | Taramundi | 5 |
| Forêt de Taramundi (50) ⚠️ | Taramundi | 5 |
| Forêt de San Tirso de Abres (13) ⚠️ | San Tirso de Abres | 5 |
| Forêt de Peñamellera Alta (14) ⚠️ | Peñamellera Alta | 5 |
| Forêt de Cabrales (123) ⚠️ | Cabrales | 5 |
| Forêt de Cabrales (147) ⚠️ | Cabrales | 5 |
| Forêt de Cabrales (175) ⚠️ | Cabrales | 5 |
| Forêt de Cabrales (177) ⚠️ | Cabrales | 5 |
| Forêt de Cabrales (180) ⚠️ | Cabrales | 5 |
| Bois de Ponga (3) ⚠️ | Ponga | 5 |
| Forêt de Cabrales (181) ⚠️ | Cabrales | 5 |
| Forêt de Cabrales (194) ⚠️ | Cabrales | 5 |
| Bois de Llanes (3) ⚠️ | Llanes | 5 |
| Bois de Las Regueras (2) ⚠️ | Las Regueras | 5 |
| Forêt de Cabrales (208) ⚠️ | Cabrales | 5 |
| Forêt de Onís (22) ⚠️ | Onís | 5 |
| Forêt de Onís (35) ⚠️ | Onís | 5 |
| Forêt de Onís (44) ⚠️ | Onís | 5 |
| Forêt de Cangas de Onís (81) ⚠️ | Cangas de Onís | 5 |
| Forêt de Cangas de Onís (110) ⚠️ | Cangas de Onís | 5 |
| Bois de Oviedo (89) ⚠️ | Oviedo | 5 |
| Forêt de Teverga (13) ⚠️ | Teverga | 5 |
| Forêt de Teverga (14) ⚠️ | Teverga | 5 |
| Forêt de Valdés (240) ⚠️ | Valdés | 5 |
| Forêt de Gijón (208) ⚠️ | Gijón | 5 |
| Forêt de Gijón (209) ⚠️ | Gijón | 5 |
| Forêt de Riosa (8) ⚠️ | Riosa | 5 |
| Forêt de Somiedo (136) ⚠️ | Somiedo | 5 |
| Forêt de Ribadesella (67) ⚠️ | Ribadesella | 5 |
| Forêt de Oviedo (82) ⚠️ | Oviedo | 5 |
| Forêt de Siero (48) ⚠️ | Siero | 5 |
| Forêt de Siero (51) ⚠️ | Siero | 5 |
| Forêt de Siero (53) ⚠️ | Siero | 5 |
| Bois de Las Regueras (4) ⚠️ | Las Regueras | 5 |
| Forêt de Villaviciosa (116) ⚠️ | Villaviciosa | 5 |
| Forêt de Cabrales (213) ⚠️ | Cabrales | 5 |
| Forêt de Cabrales (216) ⚠️ | Cabrales | 5 |
| Bois de Llanes (50) ⚠️ | Llanes | 5 |
| Bois de Llanes (92) ⚠️ | Llanes | 5 |
| Parque de Ferrera ⚠️ | Avilés | 4 |
| Forêt de Gijón (15) ⚠️ | Gijón | 4 |
| Forêt de Oviedo (9) ⚠️ | Oviedo | 4 |
| Eucaliptal de Rodiles ⚠️ | Villaviciosa | 4 |
| Bois de Oviedo ⚠️ | Oviedo | 4 |
| Forêt de Tineo (8) ⚠️ | Tineo | 4 |
| Forêt de Navia ⚠️ | Navia | 4 |
| Forêt de Ibias (9) ⚠️ | Ibias | 4 |
| Forêt de Caso (13) ⚠️ | Caso | 4 |
| Forêt de Gijón (33) ⚠️ | Gijón | 4 |
| Forêt de Quirós (15) ⚠️ | Quirós | 4 |
| Forêt de Siero (20) ⚠️ | Siero | 4 |
| Forêt de Villaviciosa (33) ⚠️ | Villaviciosa | 4 |
| Forêt de Pravia (26) ⚠️ | Pravia | 4 |
| Forêt de Lena (22) ⚠️ | Lena | 4 |
| Forêt de Valdés (91) ⚠️ | Valdés | 4 |
| Forêt de Castrillón (10) ⚠️ | Castrillón | 4 |
| Forêt de Llanera (21) ⚠️ | Llanera | 4 |
| Bois de Oviedo (4) ⚠️ | Oviedo | 4 |
| Bois de Allande (3) ⚠️ | Allande | 4 |
| Forêt de Siero (43) ⚠️ | Siero | 4 |
| Parc de Oviedo (20) ⚠️ | Oviedo | 4 |
| Forêt de Llanes (35) ⚠️ | Llanes | 4 |
| Parc de Oviedo (26) ⚠️ | Oviedo | 4 |
| Forêt de Ribadedeva (13) ⚠️ | Ribadedeva | 4 |
| Forêt de Valdés (113) ⚠️ | Valdés | 4 |
| Forêt de Coaña (37) ⚠️ | Coaña | 4 |
| Forêt de Langreo (52) ⚠️ | Langreo | 4 |
| Forêt de Villaviciosa (68) ⚠️ | Villaviciosa | 4 |
| Bois de Tapia de Casariego ⚠️ | Tapia de Casariego | 4 |
| Forêt de Tapia de Casariego (15) ⚠️ | Tapia de Casariego | 4 |
| Forêt de Oviedo (64) ⚠️ | Oviedo | 4 |
| Forêt de Cabrales (15) ⚠️ | Cabrales | 4 |
| Bois de Cabrales (9) ⚠️ | Cabrales | 4 |
| Forêt de Gijón (66) ⚠️ | Gijón | 4 |
| Forêt de Llanera (22) ⚠️ | Llanera | 4 |
| Bois de Mieres ⚠️ | Mieres | 4 |
| Bois de Noreña ⚠️ | Noreña | 4 |
| Forêt de Carreño (13) ⚠️ | Carreño | 4 |
| Bois de Gijón (16) ⚠️ | Gijón | 4 |
| Forêt de Peñamellera Baja (22) ⚠️ | Peñamellera Baja | 4 |
| Bois de Peñamellera Baja (2) ⚠️ | Peñamellera Baja | 4 |
| Bois de San Martín de Oscos (2) ⚠️ | San Martín de Oscos | 4 |
| Forêt de Gijón (83) ⚠️ | Gijón | 4 |
| Bois de Castrillón ⚠️ | Castrillón | 4 |
| Forêt de Siero (45) ⚠️ | Siero | 4 |
| Bois de Gijón (22) ⚠️ | Gijón | 4 |
| Forêt de Salas (46) ⚠️ | Salas | 4 |
| Monte de Ojos Negros ⚠️ | Cabrales | 4 |
| Forêt de Cabrales (23) ⚠️ | Cabrales | 4 |
| Forêt de Cabrales (26) ⚠️ | Cabrales | 4 |
| Forêt de Cabrales (28) ⚠️ | Cabrales | 4 |
| Forêt de Cabrales (33) ⚠️ | Cabrales | 4 |
| Forêt de Cabrales (47) ⚠️ | Cabrales | 4 |
| Bois de Taramundi (12) ⚠️ | Taramundi | 4 |
| Forêt de Gozón (20) ⚠️ | Gozón | 4 |
| Forêt de Cabrales (51) ⚠️ | Cabrales | 4 |
| Forêt de Cabrales (67) ⚠️ | Cabrales | 4 |
| Coazón ⚠️ | Cabrales | 4 |
| Forêt de Cabrales (72) ⚠️ | Cabrales | 4 |
| Forêt de Cabrales (102) ⚠️ | Cabrales | 4 |
| Forêt de Cabrales (106) ⚠️ | Cabrales | 4 |
| Forêt de Cabrales (117) ⚠️ | Cabrales | 4 |
| Forêt de Cabrales (140) ⚠️ | Cabrales | 4 |
| Forêt de Cabrales (162) ⚠️ | Cabrales | 4 |
| Forêt de Cabrales (165) ⚠️ | Cabrales | 4 |
| Forêt de Cabrales (171) ⚠️ | Cabrales | 4 |
| Forêt de Onís (5) ⚠️ | Onís | 4 |
| Bois de Caso (5) ⚠️ | Caso | 4 |
| Bois de Oviedo (48) ⚠️ | Oviedo | 4 |
| Bois de Oviedo (53) ⚠️ | Oviedo | 4 |
| Bois de Cabrales (26) ⚠️ | Cabrales | 4 |
| Forêt de Onís (23) ⚠️ | Onís | 4 |
| Forêt de Onís (48) ⚠️ | Onís | 4 |
| Bois de Allande (21) ⚠️ | Allande | 4 |
| Forêt de Onís (53) ⚠️ | Onís | 4 |
| Bois de Quirós (4) ⚠️ | Quirós | 4 |
| Forêt de Cangas de Onís (119) ⚠️ | Cangas de Onís | 4 |
| Bois de Cabrales (27) ⚠️ | Cabrales | 4 |
| Bois de Oviedo (112) ⚠️ | Oviedo | 4 |
| Bois de Teverga (4) ⚠️ | Teverga | 4 |
| Bois de Oviedo (158) ⚠️ | Oviedo | 4 |
| Bois de Tineo (57) ⚠️ | Tineo | 4 |
| Bois de Oviedo (163) ⚠️ | Oviedo | 4 |
| Bois de Oviedo (166) ⚠️ | Oviedo | 4 |
| Bois de Oviedo (167) ⚠️ | Oviedo | 4 |
| Bois de Llanera (6) ⚠️ | Llanera | 4 |
| Forêt de Navia (78) ⚠️ | Navia | 4 |
| Bois de Oviedo (202) ⚠️ | Oviedo | 4 |
| Forêt de Tineo (451) ⚠️ | Tineo | 4 |
| Forêt de Valdés (209) ⚠️ | Valdés | 4 |
| Forêt de Valdés (211) ⚠️ | Valdés | 4 |
| Forêt de Proaza (10) ⚠️ | Proaza | 4 |
| Bois de Corvera de Asturias ⚠️ | Corvera de Asturias | 4 |
| La Carbayera ⚠️ | Gijón | 4 |
| Forêt de Cabrales (222) ⚠️ | Cabrales | 4 |
| Forêt de Onís (66) ⚠️ | Onís | 4 |
| Bois de Llanes (37) ⚠️ | Llanes | 4 |
| Bois de Llanes (76) ⚠️ | Llanes | 4 |
| Forêt de Gijón (13) ⚠️ | Gijón | 3 |
| Forêt de Santa Eulalia de Oscos (5) ⚠️ | Santa Eulalia de Oscos | 3 |
| Forêt de Grandas de Salime (7) ⚠️ | Grandas de Salime | 3 |
| Forêt de Tineo (4) ⚠️ | Tineo | 3 |
| Forêt de Somiedo (4) ⚠️ | Somiedo | 3 |
| Forêt de Piloña (12) ⚠️ | Piloña | 3 |
| Forêt de Pravia (9) ⚠️ | Pravia | 3 |
| Forêt de Salas (9) ⚠️ | Salas | 3 |
| Forêt de Castrillón (2) ⚠️ | Castrillón | 3 |
| Forêt de Cudillero (9) ⚠️ | Cudillero | 3 |
| Forêt de Caso (12) ⚠️ | Caso | 3 |
| Forêt de Las Regueras (5) ⚠️ | Las Regueras | 3 |
| Forêt de Las Regueras (6) ⚠️ | Las Regueras | 3 |
| Forêt de Colunga (7) ⚠️ | Colunga | 3 |
| Forêt de Gijón (36) ⚠️ | Gijón | 3 |
| Forêt de Belmonte de Miranda (14) ⚠️ | Belmonte de Miranda | 3 |
| Forêt de Villaviciosa (43) ⚠️ | Villaviciosa | 3 |
| Forêt de Siero (27) ⚠️ | Siero | 3 |
| Forêt de Pravia (34) ⚠️ | Pravia | 3 |
| Forêt de Gozón (11) ⚠️ | Gozón | 3 |
| Forêt de Tineo (104) ⚠️ | Tineo | 3 |
| Forêt de Belmonte de Miranda (25) ⚠️ | Belmonte de Miranda | 3 |
| Forêt de Cabrales (11) ⚠️ | Cabrales | 3 |
| Forêt de Peñamellera Alta (13) ⚠️ | Peñamellera Alta | 3 |
| Forêt de Valdés (84) ⚠️ | Valdés | 3 |
| Forêt de Valdés (86) ⚠️ | Valdés | 3 |
| Forêt de San Tirso de Abres (8) ⚠️ | San Tirso de Abres | 3 |
| Forêt de Onís (2) ⚠️ | Onís | 3 |
| Bois de San Martín de Oscos ⚠️ | San Martín de Oscos | 3 |
| Forêt de Coaña (13) ⚠️ | Coaña | 3 |
| Forêt de Pravia (50) ⚠️ | Pravia | 3 |
| Forêt de San Tirso de Abres (9) ⚠️ | San Tirso de Abres | 3 |
| Forêt de Cudillero (37) ⚠️ | Cudillero | 3 |
| Forêt de Valdés (98) ⚠️ | Valdés | 3 |
| Forêt de Gijón (51) ⚠️ | Gijón | 3 |
| Bois de Langreo (33) ⚠️ | Langreo | 3 |
| Bois de Langreo (36) ⚠️ | Langreo | 3 |
| Forêt de Cudillero (43) ⚠️ | Cudillero | 3 |
| Forêt de Valdés (102) ⚠️ | Valdés | 3 |
| Forêt de Valdés (108) ⚠️ | Valdés | 3 |
| Forêt de Valdés (114) ⚠️ | Valdés | 3 |
| Forêt de Ribadesella (53) ⚠️ | Ribadesella | 3 |
| Forêt de Cangas de Onís (40) ⚠️ | Cangas de Onís | 3 |
| Forêt de Coaña (27) ⚠️ | Coaña | 3 |
| Forêt de Coaña (28) ⚠️ | Coaña | 3 |
| Forêt de El Franco (46) ⚠️ | El Franco | 3 |
| Forêt de El Franco (47) ⚠️ | El Franco | 3 |
| Forêt de Navia (13) ⚠️ | Navia | 3 |
| Forêt de Langreo (51) ⚠️ | Langreo | 3 |
| Forêt de Gijón (58) ⚠️ | Gijón | 3 |
| Forêt de Gijón (61) ⚠️ | Gijón | 3 |
| Forêt de Samartín del Rei Aurelio (11) ⚠️ | Samartín del Rei Aurelio | 3 |
| Bois de Gijón ⚠️ | Gijón | 3 |
| Forêt de Tineo (118) ⚠️ | Tineo | 3 |
| Bois de Oviedo (8) ⚠️ | Oviedo | 3 |
| Bois de Oviedo (14) ⚠️ | Oviedo | 3 |
| Bois de Lena (2) ⚠️ | Lena | 3 |
| Forêt de Llanera (23) ⚠️ | Llanera | 3 |
| Bois de Quirós (2) ⚠️ | Quirós | 3 |
| Bois de Villaviciosa (3) ⚠️ | Villaviciosa | 3 |
| Forêt de Cangas de Onís (47) ⚠️ | Cangas de Onís | 3 |
| Parque del Lauredal ⚠️ | Gijón | 3 |
| Bois de Gijón (12) ⚠️ | Gijón | 3 |
| Forêt de Villayón (25) ⚠️ | Villayón | 3 |
| Forêt de Caravia (5) ⚠️ | Caravia | 3 |
| Bois de Grandas de Salime (3) ⚠️ | Grandas de Salime | 3 |
| Bois de Gijón (23) ⚠️ | Gijón | 3 |
| Forêt de Gijón (90) ⚠️ | Gijón | 3 |
| Bois de Siero (7) ⚠️ | Siero | 3 |
| Forêt de Cabrales (30) ⚠️ | Cabrales | 3 |
| Forêt de Taramundi (33) ⚠️ | Taramundi | 3 |
| Forêt de Taramundi (35) ⚠️ | Taramundi | 3 |
| Bois de Taramundi (8) ⚠️ | Taramundi | 3 |
| Forêt de Cabrales (60) ⚠️ | Cabrales | 3 |
| Forêt de Cabrales (69) ⚠️ | Cabrales | 3 |
| Forêt de Cabrales (71) ⚠️ | Cabrales | 3 |
| Forêt de Cabrales (74) ⚠️ | Cabrales | 3 |
| Forêt de Cabrales (80) ⚠️ | Cabrales | 3 |
| Forêt de Cabrales (92) ⚠️ | Cabrales | 3 |
| Forêt de Cabrales (96) ⚠️ | Cabrales | 3 |
| Forêt de Cabrales (104) ⚠️ | Cabrales | 3 |
| Forêt de Cabrales (107) ⚠️ | Cabrales | 3 |
| Forêt de Cabrales (108) ⚠️ | Cabrales | 3 |
| Forêt de Cabrales (124) ⚠️ | Cabrales | 3 |
| Forêt de Cabrales (127) ⚠️ | Cabrales | 3 |
| Forêt de Cabrales (129) ⚠️ | Cabrales | 3 |
| Forêt de Cabrales (131) ⚠️ | Cabrales | 3 |
| Forêt de Cabrales (136) ⚠️ | Cabrales | 3 |
| Forêt de Cabrales (142) ⚠️ | Cabrales | 3 |
| Forêt de Cabrales (143) ⚠️ | Cabrales | 3 |
| Forêt de Cabrales (160) ⚠️ | Cabrales | 3 |
| Forêt de Cabrales (168) ⚠️ | Cabrales | 3 |
| Forêt de Cabrales (170) ⚠️ | Cabrales | 3 |
| Forêt de Cabrales (172) ⚠️ | Cabrales | 3 |
| Forêt de Siero (46) ⚠️ | Siero | 3 |
| Bois de Villanueva de Oscos (2) ⚠️ | Villanueva de Oscos | 3 |
| Forêt de Onís (11) ⚠️ | Onís | 3 |
| Bois de Caso (4) ⚠️ | Caso | 3 |
| Forêt de Cabrales (182) ⚠️ | Cabrales | 3 |
| Bois de Oviedo (47) ⚠️ | Oviedo | 3 |
| Forêt de Cabrales (191) ⚠️ | Cabrales | 3 |
| Forêt de Cabrales (195) ⚠️ | Cabrales | 3 |
| Forêt de Cabrales (206) ⚠️ | Cabrales | 3 |
| Bois de Aller (3) ⚠️ | Aller | 3 |
| Bois de Oviedo (52) ⚠️ | Oviedo | 3 |
| Bois de Gozón (2) ⚠️ | Gozón | 3 |
| Bois de Proaza ⚠️ | Proaza | 3 |
| Forêt de Oviedo (75) ⚠️ | Oviedo | 3 |
| Bosque de El Fulminato ⚠️ | Oviedo | 3 |
| Bois de Riosa (5) ⚠️ | Riosa | 3 |
| Forêt de Onís (27) ⚠️ | Onís | 3 |
| Forêt de Onís (29) ⚠️ | Onís | 3 |
| Forêt de Cabrales (209) ⚠️ | Cabrales | 3 |
| Forêt de Cangas de Onís (75) ⚠️ | Cangas de Onís | 3 |
| Forêt de Cangas de Onís (79) ⚠️ | Cangas de Onís | 3 |
| Forêt de Cangas de Onís (82) ⚠️ | Cangas de Onís | 3 |
| Bois de Allande (18) ⚠️ | Allande | 3 |
| Bois de Allande (19) ⚠️ | Allande | 3 |
| Forêt de Onís (60) ⚠️ | Onís | 3 |
| Forêt de Siero (47) ⚠️ | Siero | 3 |
| Bois de Proaza (3) ⚠️ | Proaza | 3 |
| Bois de Oviedo (55) ⚠️ | Oviedo | 3 |
| Bois de Llanera (4) ⚠️ | Llanera | 3 |
| Bois de Quirós (7) ⚠️ | Quirós | 3 |
| Bois de Aller (4) ⚠️ | Aller | 3 |
| Parc de Siero (18) ⚠️ | Siero | 3 |
| Bois de Salas (30) ⚠️ | Salas | 3 |
| Monte Les Muyeres ⚠️ | Cabrales | 3 |
| Bois de Siero (12) ⚠️ | Siero | 3 |
| Forêt de Gijón (111) ⚠️ | Gijón | 3 |
| Bois de Oviedo (139) ⚠️ | Oviedo | 3 |
| Bois de Peñamellera Baja (3) ⚠️ | Peñamellera Baja | 3 |
| Bois de Oviedo (168) ⚠️ | Oviedo | 3 |
| Bois de Oviedo (169) ⚠️ | Oviedo | 3 |
| Bois de Oviedo (176) ⚠️ | Oviedo | 3 |
| Bois de Valdés (42) ⚠️ | Valdés | 3 |
| Bois de Oviedo (198) ⚠️ | Oviedo | 3 |
| Bois de Quirós (14) ⚠️ | Quirós | 3 |
| Forêt de Tineo (327) ⚠️ | Tineo | 3 |
| Forêt de Tineo (329) ⚠️ | Tineo | 3 |
| Forêt de Tineo (330) ⚠️ | Tineo | 3 |
| Forêt de Tineo (385) ⚠️ | Tineo | 3 |
| Forêt de Tineo (445) ⚠️ | Tineo | 3 |
| Forêt de Valdés (296) ⚠️ | Valdés | 3 |
| Forêt de Riosa (11) ⚠️ | Riosa | 3 |
| Forêt de Riosa (12) ⚠️ | Riosa | 3 |
| Forêt de Somiedo (174) ⚠️ | Somiedo | 3 |
| Bois de Teverga (6) ⚠️ | Teverga | 3 |
| Forêt de Parres (50) ⚠️ | Parres | 3 |
| Forêt de Gijón (286) ⚠️ | Gijón | 3 |
| Forêt de Gijón (302) ⚠️ | Gijón | 3 |
| Parque de El Rinconín ⚠️ | Gijón | 3 |
| Parque de Julián Ayesta ⚠️ | Gijón | 3 |
| Forêt de San Tirso de Abres (16) ⚠️ | San Tirso de Abres | 3 |
| Forêt de Cabrales (219) ⚠️ | Cabrales | 3 |
| Bois de Llanes (35) ⚠️ | Llanes | 3 |
| Bois de Ribadesella (17) ⚠️ | Ribadesella | 3 |
| Bois de Llanes (49) ⚠️ | Llanes | 3 |
| Bois de Llanes (62) ⚠️ | Llanes | 3 |
| Bois de Llanes (80) ⚠️ | Llanes | 3 |
| Forêt de Navia (138) ⚠️ | Navia | 3 |
| Parc de Oviedo ⚠️ | Oviedo | 2 |
| Parque de La Magdalena ⚠️ | Avilés | 2 |
| Forêt de Oviedo (4) ⚠️ | Oviedo | 2 |
| La Barquerina ⚠️ | Villaviciosa | 2 |
| Parc de Oviedo (11) ⚠️ | Oviedo | 2 |
| Forêt de Llanera (4) ⚠️ | Llanera | 2 |
| Forêt de Llanera (5) ⚠️ | Llanera | 2 |
| Forêt de Grandas de Salime (6) ⚠️ | Grandas de Salime | 2 |
| Forêt de Ibias (4) ⚠️ | Ibias | 2 |
| Forêt de Grandas de Salime (9) ⚠️ | Grandas de Salime | 2 |
| Forêt de Valdés (5) ⚠️ | Valdés | 2 |
| Forêt de Caso (3) ⚠️ | Caso | 2 |
| Forêt de Ponga (6) ⚠️ | Ponga | 2 |
| Forêt de Quirós (13) ⚠️ | Quirós | 2 |
| Forêt de Colunga (2) ⚠️ | Colunga | 2 |
| Forêt de Somiedo (9) ⚠️ | Somiedo | 2 |
| Forêt de Somiedo (11) ⚠️ | Somiedo | 2 |
| Forêt de Cangas de Onís (16) ⚠️ | Cangas de Onís | 2 |
| Forêt de Cudillero (13) ⚠️ | Cudillero | 2 |
| Forêt de Llanera (12) ⚠️ | Llanera | 2 |
| Forêt de Llanera (13) ⚠️ | Llanera | 2 |
| Forêt de Grandas de Salime (20) ⚠️ | Grandas de Salime | 2 |
| Forêt de Ponga (24) ⚠️ | Ponga | 2 |
| Forêt de Villaviciosa (38) ⚠️ | Villaviciosa | 2 |
| Forêt de Grandas de Salime (26) ⚠️ | Grandas de Salime | 2 |
| Forêt de Salas (31) ⚠️ | Salas | 2 |
| Forêt de Ribadesella (11) ⚠️ | Ribadesella | 2 |
| Forêt de Ponga (31) ⚠️ | Ponga | 2 |
| Forêt de Villaviciosa (52) ⚠️ | Villaviciosa | 2 |
| Forêt de Quirós (31) ⚠️ | Quirós | 2 |
| Forêt de Cudillero (28) ⚠️ | Cudillero | 2 |
| Forêt de Cudillero (29) ⚠️ | Cudillero | 2 |
| Forêt de Quirós (33) ⚠️ | Quirós | 2 |
| Forêt de Piloña (67) ⚠️ | Piloña | 2 |
| Forêt de Laviana (32) ⚠️ | Laviana | 2 |
| Forêt de Peñamellera Baja (20) ⚠️ | Peñamellera Baja | 2 |
| Plaza Tuero Bertrand ⚠️ | Oviedo | 2 |
| Parc de Oviedo (14) ⚠️ | Oviedo | 2 |
| Bois de Avilés ⚠️ | Avilés | 2 |
| Bois de Colunga ⚠️ | Colunga | 2 |
| Forêt de Illano (24) ⚠️ | Illano | 2 |
| Parque del Camino de Santiago ⚠️ | Oviedo | 2 |
| Forêt de Allande (40) ⚠️ | Allande | 2 |
| Forêt de Llanes (31) ⚠️ | Llanes | 2 |
| Forêt de Ribadesella (22) ⚠️ | Ribadesella | 2 |
| Forêt de Oviedo (52) ⚠️ | Oviedo | 2 |
| Forêt de Las Regueras (26) ⚠️ | Las Regueras | 2 |
| Parc de Oviedo (25) ⚠️ | Oviedo | 2 |
| Forêt de Salas (45) ⚠️ | Salas | 2 |
| Bois de Valdés ⚠️ | Valdés | 2 |
| Forêt de Valdés (119) ⚠️ | Valdés | 2 |
| Forêt de Ribadesella (31) ⚠️ | Ribadesella | 2 |
| Forêt de Ribadesella (43) ⚠️ | Ribadesella | 2 |
| Forêt de Ribadesella (44) ⚠️ | Ribadesella | 2 |
| Forêt de Ribadesella (45) ⚠️ | Ribadesella | 2 |
| Forêt de Ribadesella (47) ⚠️ | Ribadesella | 2 |
| Forêt de Ribadesella (49) ⚠️ | Ribadesella | 2 |
| Forêt de Ribadesella (50) ⚠️ | Ribadesella | 2 |
| Forêt de El Franco (31) ⚠️ | El Franco | 2 |
| Forêt de El Franco (32) ⚠️ | El Franco | 2 |
| Forêt de El Franco (36) ⚠️ | El Franco | 2 |
| Forêt de Coaña (16) ⚠️ | Coaña | 2 |
| Forêt de El Franco (43) ⚠️ | El Franco | 2 |
| Forêt de Coaña (21) ⚠️ | Coaña | 2 |
| Forêt de Coaña (22) ⚠️ | Coaña | 2 |
| Forêt de Coaña (24) ⚠️ | Coaña | 2 |
| Forêt de Coaña (30) ⚠️ | Coaña | 2 |
| Forêt de Coaña (31) ⚠️ | Coaña | 2 |
| Forêt de Coaña (32) ⚠️ | Coaña | 2 |
| Bois de Valdés (2) ⚠️ | Valdés | 2 |
| Forêt de Navia (7) ⚠️ | Navia | 2 |
| Bois de Valdés (3) ⚠️ | Valdés | 2 |
| Forêt de Valdés (123) ⚠️ | Valdés | 2 |
| Forêt de Valdés (127) ⚠️ | Valdés | 2 |
| Forêt de Langreo (48) ⚠️ | Langreo | 2 |
| Forêt de Langreo (50) ⚠️ | Langreo | 2 |
| Bois de Colunga (2) ⚠️ | Colunga | 2 |
| Forêt de Gijón (57) ⚠️ | Gijón | 2 |
| Forêt de Colunga (25) ⚠️ | Colunga | 2 |
| Parc de Gijón (4) ⚠️ | Gijón | 2 |
| Forêt de Langreo (55) ⚠️ | Langreo | 2 |
| Forêt de Riosa (7) ⚠️ | Riosa | 2 |
| Forêt de Oviedo (53) ⚠️ | Oviedo | 2 |
| Forêt de Piloña (73) ⚠️ | Piloña | 2 |
| Forêt de Oviedo (55) ⚠️ | Oviedo | 2 |
| Bois de Llanera ⚠️ | Llanera | 2 |
| Forêt de Oviedo (57) ⚠️ | Oviedo | 2 |
| Forêt de Oviedo (63) ⚠️ | Oviedo | 2 |
| Forêt de Oviedo (65) ⚠️ | Oviedo | 2 |
| Bois de Cabrales (16) ⚠️ | Cabrales | 2 |
| Bois de Caso ⚠️ | Caso | 2 |
| Forêt de Caso (56) ⚠️ | Caso | 2 |
| Bois de Gijón (7) ⚠️ | Gijón | 2 |
| Parque La Libertad ⚠️ | Castrillón | 2 |
| Parque Dorado ⚠️ | Langreo | 2 |
| Forêt de Gijón (69) ⚠️ | Gijón | 2 |
| Forêt de Gijón (70) ⚠️ | Gijón | 2 |
| Parc de Oviedo (72) ⚠️ | Oviedo | 2 |
| Bois de Aller ⚠️ | Aller | 2 |
| Bois de Siero (6) ⚠️ | Siero | 2 |
| Forêt de Gijón (80) ⚠️ | Gijón | 2 |
| Bois de Ribadesella (3) ⚠️ | Ribadesella | 2 |
| La Collada ⚠️ | Degaña | 2 |
| Forêt de Caravia (3) ⚠️ | Caravia | 2 |
| Bois de Gijón (21) ⚠️ | Gijón | 2 |
| Forêt de Siero (44) ⚠️ | Siero | 2 |
| Forêt de Sariego (5) ⚠️ | Sariego | 2 |
| Bois de Allande (6) ⚠️ | Allande | 2 |
| Bois de Allande (9) ⚠️ | Allande | 2 |
| Bois de Grado ⚠️ | Grado | 2 |
| Forêt de Cabrales (19) ⚠️ | Cabrales | 2 |
| Forêt de Cabrales (20) ⚠️ | Cabrales | 2 |
| Forêt de Salas (47) ⚠️ | Salas | 2 |
| Forêt de Tineo (119) ⚠️ | Tineo | 2 |
| Forêt de Parres (31) ⚠️ | Parres | 2 |
| Forêt de Cabrales (35) ⚠️ | Cabrales | 2 |
| Forêt de Cabrales (36) ⚠️ | Cabrales | 2 |
| Forêt de Cabrales (39) ⚠️ | Cabrales | 2 |
| Forêt de Cabrales (41) ⚠️ | Cabrales | 2 |
| Forêt de Cabrales (42) ⚠️ | Cabrales | 2 |
| Forêt de Cabrales (44) ⚠️ | Cabrales | 2 |
| Forêt de Oviedo (73) ⚠️ | Oviedo | 2 |
| Forêt de Taramundi (28) ⚠️ | Taramundi | 2 |
| Forêt de Taramundi (29) ⚠️ | Taramundi | 2 |
| Forêt de Taramundi (31) ⚠️ | Taramundi | 2 |
| Forêt de Taramundi (32) ⚠️ | Taramundi | 2 |
| Bois de Taramundi (6) ⚠️ | Taramundi | 2 |
| Forêt de Taramundi (47) ⚠️ | Taramundi | 2 |
| Forêt de San Tirso de Abres (12) ⚠️ | San Tirso de Abres | 2 |
| Forêt de Carreño (16) ⚠️ | Carreño | 2 |
| Forêt de Cabrales (49) ⚠️ | Cabrales | 2 |
| Forêt de Gijón (99) ⚠️ | Gijón | 2 |
| Campo de San Francisco ⚠️ | Oviedo | 2 |
| Forêt de Lena (36) ⚠️ | Lena | 2 |
| Forêt de Cabrales (94) ⚠️ | Cabrales | 2 |
| Forêt de Cabrales (95) ⚠️ | Cabrales | 2 |
| Forêt de Cabrales (98) ⚠️ | Cabrales | 2 |
| Forêt de Cabrales (101) ⚠️ | Cabrales | 2 |
| Forêt de Cabrales (114) ⚠️ | Cabrales | 2 |
| Forêt de Cabrales (122) ⚠️ | Cabrales | 2 |
| Forêt de Cabrales (138) ⚠️ | Cabrales | 2 |
| Forêt de Cabrales (139) ⚠️ | Cabrales | 2 |
| Forêt de Cabrales (148) ⚠️ | Cabrales | 2 |
| Forêt de Cabrales (151) ⚠️ | Cabrales | 2 |
| Forêt de Cabrales (169) ⚠️ | Cabrales | 2 |
| Forêt de Onís (9) ⚠️ | Onís | 2 |
| Bois de Piloña (2) ⚠️ | Piloña | 2 |
| Forêt de Cabrales (193) ⚠️ | Cabrales | 2 |
| Forêt de Cabrales (196) ⚠️ | Cabrales | 2 |
| Forêt de Cabrales (201) ⚠️ | Cabrales | 2 |
| Forêt de Cabrales (204) ⚠️ | Cabrales | 2 |
| Forêt de Cabrales (205) ⚠️ | Cabrales | 2 |
| Forêt de Peñamellera Alta (17) ⚠️ | Peñamellera Alta | 2 |
| Forêt de Gijón (101) ⚠️ | Gijón | 2 |
| Bois de Cabrales (25) ⚠️ | Cabrales | 2 |
| Bois de Tineo (4) ⚠️ | Tineo | 2 |
| Bois de Castrillón (2) ⚠️ | Castrillón | 2 |
| Forêt de Onís (19) ⚠️ | Onís | 2 |
| Forêt de Onís (24) ⚠️ | Onís | 2 |
| Forêt de Onís (31) ⚠️ | Onís | 2 |
| Forêt de Onís (33) ⚠️ | Onís | 2 |
| Forêt de Onís (34) ⚠️ | Onís | 2 |
| Forêt de Onís (37) ⚠️ | Onís | 2 |
| Forêt de Onís (41) ⚠️ | Onís | 2 |
| Forêt de Cangas de Onís (49) ⚠️ | Cangas de Onís | 2 |
| Forêt de Cangas de Onís (51) ⚠️ | Cangas de Onís | 2 |
| Forêt de Cangas de Onís (59) ⚠️ | Cangas de Onís | 2 |
| Forêt de Cangas de Onís (85) ⚠️ | Cangas de Onís | 2 |
| Forêt de Onís (52) ⚠️ | Onís | 2 |
| Bois de Tineo (8) ⚠️ | Tineo | 2 |
| Forêt de Cangas de Onís (105) ⚠️ | Cangas de Onís | 2 |
| Bois de Oviedo (56) ⚠️ | Oviedo | 2 |
| Bois de Llanes (6) ⚠️ | Llanes | 2 |
| Bois de Siero (10) ⚠️ | Siero | 2 |
| Bois de Quirós (12) ⚠️ | Quirós | 2 |
| Bois de Gijón (54) ⚠️ | Gijón | 2 |
| Forêt de Cangas de Onís (120) ⚠️ | Cangas de Onís | 2 |
| Forêt de Cangas de Onís (121) ⚠️ | Cangas de Onís | 2 |
| Forêt de Pravia (52) ⚠️ | Pravia | 2 |
| Monte El Ardinal ⚠️ | Cabrales | 2 |
| Parc de Gijón (44) ⚠️ | Gijón | 2 |
| Bois de Oviedo (57) ⚠️ | Oviedo | 2 |
| Bois de Oviedo (67) ⚠️ | Oviedo | 2 |
| Forêt de Gijón (117) ⚠️ | Gijón | 2 |
| Forêt de Gijón (143) ⚠️ | Gijón | 2 |
| Bois de Oviedo (83) ⚠️ | Oviedo | 2 |
| Bois de Oviedo (86) ⚠️ | Siero | 2 |
| Bois de Oviedo (96) ⚠️ | Oviedo | 2 |
| Bois de Oviedo (98) ⚠️ | Oviedo | 2 |
| Bois de Siero (13) ⚠️ | Siero | 2 |
| Bois de Oviedo (110) ⚠️ | Oviedo | 2 |
| Bois de Oviedo (126) ⚠️ | Oviedo | 2 |
| Bois de Llanes (13) ⚠️ | Llanes | 2 |
| Bois de Llanes (23) ⚠️ | Llanes | 2 |
| Bois de Oviedo (147) ⚠️ | Oviedo | 2 |
| Bois de Tineo (80) ⚠️ | Tineo | 2 |
| Bois de Oviedo (164) ⚠️ | Oviedo | 2 |
| Bois de Oviedo (165) ⚠️ | Oviedo | 2 |
| Bois de Tineo (102) ⚠️ | Tineo | 2 |
| Forêt de Villaviciosa (94) ⚠️ | Villaviciosa | 2 |
| Forêt de Valdés (153) ⚠️ | Valdés | 2 |
| Forêt de Navia (118) ⚠️ | Navia | 2 |
| Forêt de Navia (128) ⚠️ | Navia | 2 |
| Forêt de Tineo (231) ⚠️ | Tineo | 2 |
| Forêt de Tineo (237) ⚠️ | Tineo | 2 |
| Forêt de Tineo (261) ⚠️ | Tineo | 2 |
| Forêt de Tineo (302) ⚠️ | Tineo | 2 |
| Bois de Oviedo (196) ⚠️ | Oviedo | 2 |
| Bois de Gijón (62) ⚠️ | Gijón | 2 |
| Forêt de Tineo (642) ⚠️ | Tineo | 2 |
| Forêt de Valdés (212) ⚠️ | Valdés | 2 |
| Forêt de Valdés (252) ⚠️ | Valdés | 2 |
| Forêt de Riosa (13) ⚠️ | Riosa | 2 |
| Bois de Oviedo (210) ⚠️ | Oviedo | 2 |
| Bois de Oviedo (211) ⚠️ | Oviedo | 2 |
| Forêt de Cangas del Narcea (121) ⚠️ | Cangas del Narcea | 2 |
| Forêt de Proaza (9) ⚠️ | Proaza | 2 |
| Forêt de Proaza (11) ⚠️ | Proaza | 2 |
| Forêt de Tineo (930) ⚠️ | Tineo | 2 |
| Forêt de Somiedo (99) ⚠️ | Somiedo | 2 |
| Forêt de Somiedo (118) ⚠️ | Somiedo | 2 |
| Forêt de Gijón (240) ⚠️ | Gijón | 2 |
| Bois de Oviedo (218) ⚠️ | Oviedo | 2 |
| Forêt de Castropol (22) ⚠️ | Castropol | 2 |
| Forêt de Castropol (24) ⚠️ | Castropol | 2 |
| Forêt de Castropol (32) ⚠️ | Tapia de Casariego | 2 |
| Forêt de Ribadesella (65) ⚠️ | Ribadesella | 2 |
| Forêt de Avilés (5) ⚠️ | Avilés | 2 |
| Forêt de Piloña (79) ⚠️ | Piloña | 2 |
| Forêt de Gijón (284) ⚠️ | Gijón | 2 |
| Forêt de Siero (49) ⚠️ | Siero | 2 |
| Forêt de Siero (50) ⚠️ | Siero | 2 |
| Forêt de Noreña (2) ⚠️ | Noreña | 2 |
| Forêt de Gijón (290) ⚠️ | Gijón | 2 |
| Parque de La Llaguna ⚠️ | Samartín del Rei Aurelio | 2 |
| Parque Hermanos Castro ⚠️ | Gijón | 2 |
| Parque Europa ⚠️ | Corvera de Asturias | 2 |
| Parque del Nuevo Roces ⚠️ | Gijón | 2 |
| Forêt de Cabrales (224) ⚠️ | Cabrales | 2 |
| Bois de Valdés (59) ⚠️ | Valdés | 2 |
| Parc de Gijón (95) ⚠️ | Gijón | 2 |
| Bois de Ribadesella (11) ⚠️ | Ribadesella | 2 |
| Bois de Ribadesella (15) ⚠️ | Ribadesella | 2 |
| Bois de Llanes (38) ⚠️ | Llanes | 2 |
| Bois de Llanes (42) ⚠️ | Llanes | 2 |
| Bois de Llanes (45) ⚠️ | Llanes | 2 |
| Bois de Llanes (70) ⚠️ | Llanes | 2 |
| Bois de Llanes (71) ⚠️ | Llanes | 2 |
| Bois de Llanes (86) ⚠️ | Llanes | 2 |
| Bois de Llanes (89) ⚠️ | Llanes | 2 |
| Bois de Amieva ⚠️ | Amieva | 2 |
| Campillín ⚠️ | Oviedo | 1 |
| Parc de Oviedo (3) ⚠️ | Oviedo | 1 |
| Parque de Ismael Fuente ⚠️ | Oviedo | 1 |
| Parque del Doctor Juan Negrín ⚠️ | Gijón | 1 |
| Santuyano ⚠️ | Oviedo | 1 |
| Parque de Fernando VI ⚠️ | Gijón | 1 |
| Parque de Las Meanas ⚠️ | Avilés | 1 |
| Plaza Mirador del Aramo ⚠️ | Oviedo | 1 |
| Plaza Luis Arrones ⚠️ | Oviedo | 1 |
| Plaza de Madrid ⚠️ | Oviedo | 1 |
| Parque de Los Estibadores ⚠️ | Gijón | 1 |
| Forêt de Gijón (2) ⚠️ | Gijón | 1 |
| Forêt de Gijón (9) ⚠️ | Gijón | 1 |
| Forêt de Gijón (10) ⚠️ | Gijón | 1 |
| Parque de El Nodo (Sol Naciente) ⚠️ | Avilés | 1 |
| Plaza Pierre de Coubertin ⚠️ | Oviedo | 1 |
| Parc de Oviedo (6) ⚠️ | Oviedo | 1 |
| Parc de Oviedo (7) ⚠️ | Oviedo | 1 |
| Parc de Oviedo (8) ⚠️ | Oviedo | 1 |
| Parque Ciudad de Tampa ⚠️ | Oviedo | 1 |
| Parc de Oviedo (9) ⚠️ | Oviedo | 1 |
| Parque de La Cabornia ⚠️ | Oviedo | 1 |
| Forêt de Oviedo (5) ⚠️ | Oviedo | 1 |
| Forêt de Oviedo (8) ⚠️ | Oviedo | 1 |
| Monte Picota ⚠️ | Villaviciosa | 1 |
| Parque de la Llera ⚠️ | Parres | 1 |
| Forêt de Llanera (2) ⚠️ | Llanera | 1 |
| Forêt de Llanera (3) ⚠️ | Llanera | 1 |
| "Parque de Arriba" ⚠️ | Grado | 1 |
| Jardines de Lázaro Cárdenas (2) ⚠️ | Gijón | 1 |
| Forêt de Degaña ⚠️ | Degaña | 1 |
| Forêt de Ponga ⚠️ | Ponga | 1 |
| Forêt de Taramundi ⚠️ | Taramundi | 1 |
| Forêt de Santa Eulalia de Oscos ⚠️ | Santa Eulalia de Oscos | 1 |
| Forêt de San Tirso de Abres (2) ⚠️ | San Tirso de Abres | 1 |
| Forêt de Santa Eulalia de Oscos (3) ⚠️ | Santa Eulalia de Oscos | 1 |
| Forêt de Taramundi (2) ⚠️ | Taramundi | 1 |
| Forêt de Grandas de Salime (4) ⚠️ | Grandas de Salime | 1 |
| Forêt de Grandas de Salime (5) ⚠️ | Grandas de Salime | 1 |
| Forêt de Santa Eulalia de Oscos (6) ⚠️ | Santa Eulalia de Oscos | 1 |
| Forêt de Grandas de Salime (8) ⚠️ | Grandas de Salime | 1 |
| Forêt de Peñamellera Baja ⚠️ | Peñamellera Baja | 1 |
| Forêt de Peñamellera Baja (4) ⚠️ | Peñamellera Baja | 1 |
| Forêt de Quirós ⚠️ | Quirós | 1 |
| Forêt de Gijón (21) ⚠️ | Gijón | 1 |
| Forêt de Laviana (3) ⚠️ | Laviana | 1 |
| Forêt de Piloña (10) ⚠️ | Piloña | 1 |
| Forêt de Pravia (5) ⚠️ | Pravia | 1 |
| Forêt de Langreo (6) ⚠️ | Langreo | 1 |
| Forêt de Quirós (11) ⚠️ | Quirós | 1 |
| Forêt de Quirós (12) ⚠️ | Quirós | 1 |
| Forêt de Lena (11) ⚠️ | Lena | 1 |
| Forêt de Ribadedeva (3) ⚠️ | Ribadedeva | 1 |
| Forêt de Langreo (9) ⚠️ | Langreo | 1 |
| Forêt de Cudillero (10) ⚠️ | Cudillero | 1 |
| Forêt de Pravia (18) ⚠️ | Pravia | 1 |
| Forêt de Peñamellera Alta (6) ⚠️ | Peñamellera Alta | 1 |
| Forêt de Piloña (32) ⚠️ | Piloña | 1 |
| Forêt de Santa Eulalia de Oscos (10) ⚠️ | Santa Eulalia de Oscos | 1 |
| Forêt de Soto del Barco (3) ⚠️ | Soto del Barco | 1 |
| Forêt de Ribera de Arriba (5) ⚠️ | Ribera de Arriba | 1 |
| Forêt de Tineo (56) ⚠️ | Tineo | 1 |
| Forêt de Gijón (38) ⚠️ | Gijón | 1 |
| Forêt de Langreo (15) ⚠️ | Langreo | 1 |
| Forêt de Santa Eulalia de Oscos (12) ⚠️ | Santa Eulalia de Oscos | 1 |
| Forêt de Castropol (7) ⚠️ | Castropol | 1 |
| Forêt de Aller (30) ⚠️ | Aller | 1 |
| Forêt de Grado (24) ⚠️ | Grado | 1 |
| Forêt de Caso (29) ⚠️ | Caso | 1 |
| Forêt de Salas (29) ⚠️ | Salas | 1 |
| Forêt de Quirós (23) ⚠️ | Quirós | 1 |
| Forêt de Peñamellera Alta (10) ⚠️ | Peñamellera Alta | 1 |
| Bois de Peñamellera Baja ⚠️ | Peñamellera Baja | 1 |
| Forêt de Oviedo (34) ⚠️ | Oviedo | 1 |
| Forêt de Caso (41) ⚠️ | Caso | 1 |
| Forêt de Las Regueras (18) ⚠️ | Las Regueras | 1 |
| Forêt de Langreo (25) ⚠️ | Langreo | 1 |
| Monte Xarragúa ⚠️ | Sobrescobio | 1 |
| Forêt de Belmonte de Miranda (24) ⚠️ | Belmonte de Miranda | 1 |
| Forêt de Pravia (44) ⚠️ | Pravia | 1 |
| Forêt de Pravia (45) ⚠️ | Pravia | 1 |
| Forêt de Oviedo (46) ⚠️ | Oviedo | 1 |
| Forêt de Villaviciosa (64) ⚠️ | Villaviciosa | 1 |
| Forêt de Quirós (37) ⚠️ | Quirós | 1 |
| Forêt de Langreo (30) ⚠️ | Langreo | 1 |
| Forêt de Grandas de Salime (36) ⚠️ | Grandas de Salime | 1 |
| Forêt de Nava (20) ⚠️ | Nava | 1 |
| Forêt de Valdés (77) ⚠️ | Valdés | 1 |
| Forêt de Valdés (78) ⚠️ | Valdés | 1 |
| Forêt de Valdés (79) ⚠️ | Valdés | 1 |
| Forêt de Valdés (89) ⚠️ | Valdés | 1 |
| Forêt de Soto del Barco (8) ⚠️ | Soto del Barco | 1 |
| Forêt de Castrillón (8) ⚠️ | Castrillón | 1 |
| Forêt de Castrillón (9) ⚠️ | Castrillón | 1 |
| Forêt de Cangas del Narcea (113) ⚠️ | Cangas del Narcea | 1 |
| Parc de Oviedo (15) ⚠️ | Oviedo | 1 |
| Parc de Avilés (2) ⚠️ | Avilés | 1 |
| Parque del Pozón ⚠️ | Avilés | 1 |
| Forêt de Siero (40) ⚠️ | Siero | 1 |
| Forêt de Siero (41) ⚠️ | Siero | 1 |
| Forêt de Siero (42) ⚠️ | Siero | 1 |
| Parque de Redes ⚠️ | Siero | 1 |
| Bois de Avilés (2) ⚠️ | Avilés | 1 |
| Forêt de Tineo (113) ⚠️ | Tineo | 1 |
| Forêt de Tineo (114) ⚠️ | Tineo | 1 |
| Forêt de Tineo (115) ⚠️ | Tineo | 1 |
| Bosque del Payán ⚠️ | Oviedo | 1 |
| Parque de Los Riegos ⚠️ | Noreña | 1 |
| Prao el Molín ⚠️ | Cangas del Narcea | 1 |
| Parque Somorrostro ⚠️ | Avilés | 1 |
| Parc de Oviedo (17) ⚠️ | Oviedo | 1 |
| Parc de Avilés (11) ⚠️ | Avilés | 1 |
| Forêt de Colunga (15) ⚠️ | Colunga | 1 |
| Parque Aníbal Vázquez ⚠️ | Mieres | 1 |
| Parque Enrique Quirós Montes de Oca ⚠️ | Oviedo | 1 |
| Forêt de Lena (32) ⚠️ | Lena | 1 |
| Forêt de Avilés (4) ⚠️ | Avilés | 1 |
| Parc de Mieres ⚠️ | Mieres | 1 |
| Parc de Mieres (5) ⚠️ | Mieres | 1 |
| Forêt de Lena (33) ⚠️ | Lena | 1 |
| Bois de Lena ⚠️ | Lena | 1 |
| Parque Tartiere ⚠️ | Mieres | 1 |
| Bois de Santa Eulalia de Oscos ⚠️ | Santa Eulalia de Oscos | 1 |
| Bois de Grandas de Salime ⚠️ | Grandas de Salime | 1 |
| Forêt de Grandas de Salime (41) ⚠️ | Grandas de Salime | 1 |
| Bois de San Tirso de Abres ⚠️ | San Tirso de Abres | 1 |
| Jardines de Constancia de la Mora y Maura ⚠️ | Gijón | 1 |
| Area Recreativa Parteayer ⚠️ | Morcín | 1 |
| Parc de Mieres (26) ⚠️ | Mieres | 1 |
| Forêt de Grado (35) ⚠️ | Grado | 1 |
| Forêt de Cudillero (39) ⚠️ | Cudillero | 1 |
| Forêt de Valdés (96) ⚠️ | Valdés | 1 |
| Bois de Langreo (2) ⚠️ | Langreo | 1 |
| Bois de Langreo (5) ⚠️ | Langreo | 1 |
| Parc de Oviedo (22) ⚠️ | Oviedo | 1 |
| Bois de Langreo (16) ⚠️ | Langreo | 1 |
| Forêt de Langreo (46) ⚠️ | Langreo | 1 |
| Bois de Langreo (23) ⚠️ | Langreo | 1 |
| Bois de Langreo (24) ⚠️ | Langreo | 1 |
| Bois de Langreo (25) ⚠️ | Langreo | 1 |
| Bois de Langreo (28) ⚠️ | Langreo | 1 |
| Bois de Langreo (30) ⚠️ | Langreo | 1 |
| Bois de Langreo (37) ⚠️ | Langreo | 1 |
| Forêt de Grandas de Salime (42) ⚠️ | Grandas de Salime | 1 |
| Forêt de Candamo (9) ⚠️ | Grado | 1 |
| Parc de Oviedo (27) ⚠️ | Oviedo | 1 |
| Forêt de Langreo (47) ⚠️ | Langreo | 1 |
| Bois de Oviedo (5) ⚠️ | Oviedo | 1 |
| Forêt de Valdés (99) ⚠️ | Valdés | 1 |
| Forêt de Valdés (100) ⚠️ | Valdés | 1 |
| Forêt de Valdés (109) ⚠️ | Valdés | 1 |
| Forêt de Valdés (111) ⚠️ | Valdés | 1 |
| Forêt de Valdés (112) ⚠️ | Valdés | 1 |
| Forêt de Valdés (115) ⚠️ | Valdés | 1 |
| Forêt de Cudillero (48) ⚠️ | Cudillero | 1 |
| Forêt de Valdés (120) ⚠️ | Valdés | 1 |
| Parc de Llanera (3) ⚠️ | Llanera | 1 |
| Forêt de Ribadesella (29) ⚠️ | Ribadesella | 1 |
| Forêt de Ribadesella (30) ⚠️ | Ribadesella | 1 |
| Forêt de Ribadesella (33) ⚠️ | Ribadesella | 1 |
| Forêt de Ribadesella (36) ⚠️ | Ribadesella | 1 |
| Forêt de Ribadesella (39) ⚠️ | Ribadesella | 1 |
| Forêt de Ribadesella (40) ⚠️ | Ribadesella | 1 |
| Forêt de Ribadesella (41) ⚠️ | Ribadesella | 1 |
| Forêt de Ribadesella (46) ⚠️ | Ribadesella | 1 |
| Forêt de Ribadesella (51) ⚠️ | Ribadesella | 1 |
| Forêt de El Franco (22) ⚠️ | El Franco | 1 |
| Forêt de El Franco (23) ⚠️ | El Franco | 1 |
| Forêt de El Franco (25) ⚠️ | El Franco | 1 |
| Forêt de El Franco (28) ⚠️ | El Franco | 1 |
| Forêt de El Franco (33) ⚠️ | El Franco | 1 |
| Forêt de El Franco (35) ⚠️ | El Franco | 1 |
| Forêt de El Franco (37) ⚠️ | El Franco | 1 |
| Forêt de El Franco (38) ⚠️ | El Franco | 1 |
| Forêt de Gozón (17) ⚠️ | Gozón | 1 |
| Forêt de Coaña (15) ⚠️ | Coaña | 1 |
| Forêt de Coaña (17) ⚠️ | Coaña | 1 |
| Forêt de Coaña (19) ⚠️ | Coaña | 1 |
| Forêt de Coaña (20) ⚠️ | Coaña | 1 |
| Forêt de Coaña (23) ⚠️ | Coaña | 1 |
| Forêt de El Franco (44) ⚠️ | El Franco | 1 |
| Forêt de El Franco (45) ⚠️ | El Franco | 1 |
| Forêt de Coaña (29) ⚠️ | Coaña | 1 |
| Forêt de El Franco (49) ⚠️ | El Franco | 1 |
| Forêt de El Franco (50) ⚠️ | El Franco | 1 |
| Forêt de Caravia (2) ⚠️ | Caravia | 1 |
| Forêt de Castrillón (12) ⚠️ | Castrillón | 1 |
| Forêt de Gijón (55) ⚠️ | Gijón | 1 |
| Forêt de Valdés (122) ⚠️ | Valdés | 1 |
| Forêt de Valdés (124) ⚠️ | Valdés | 1 |
| Forêt de Valdés (125) ⚠️ | Valdés | 1 |
| Forêt de Navia (10) ⚠️ | Navia | 1 |
| Forêt de Valdés (130) ⚠️ | Valdés | 1 |
| Parc de Ribadesella ⚠️ | Ribadesella | 1 |
| Forêt de Tapia de Casariego (14) ⚠️ | Tapia de Casariego | 1 |
| Forêt de Coaña (40) ⚠️ | Coaña | 1 |
| Carbayera de Leorio ⚠️ | Gijón | 1 |
| Carbayera de las Monxas ⚠️ | Gijón | 1 |
| Forêt de Gijón (56) ⚠️ | Gijón | 1 |
| Forêt de Colunga (21) ⚠️ | Colunga | 1 |
| Forêt de Colunga (24) ⚠️ | Colunga | 1 |
| Forêt de Colunga (26) ⚠️ | Colunga | 1 |
| Parc de Oviedo (31) ⚠️ | Oviedo | 1 |
| Bois de Cangas de Onís (3) ⚠️ | Cangas de Onís | 1 |
| Forêt de Cangas de Onís (44) ⚠️ | Cangas de Onís | 1 |
| Parc de Lena (2) ⚠️ | Lena | 1 |
| Parc de Oviedo (34) ⚠️ | Oviedo | 1 |
| Parc de Siero (10) ⚠️ | Siero | 1 |
| Forêt de Cangas del Narcea (118) ⚠️ | Cangas del Narcea | 1 |
| Parc de Gijón (12) ⚠️ | Gijón | 1 |
| Parc de Gijón (14) ⚠️ | Gijón | 1 |
| Parc de Oviedo (36) ⚠️ | Oviedo | 1 |
| Parc de Gijón (15) ⚠️ | Gijón | 1 |
| Parc de Oviedo (37) ⚠️ | Oviedo | 1 |
| Parc de Oviedo (41) ⚠️ | Oviedo | 1 |
| Bois de Siero (4) ⚠️ | Siero | 1 |
| Forêt de Grado (37) ⚠️ | Grado | 1 |
| Alfonso X El Sabio ⚠️ | Siero | 1 |
| Parc de Oviedo (47) ⚠️ | Oviedo | 1 |
| Parc de Oviedo (50) ⚠️ | Oviedo | 1 |
| Parc de Oviedo (51) ⚠️ | Oviedo | 1 |
| Forêt de Oviedo (60) ⚠️ | Oviedo | 1 |
| Forêt de Oviedo (61) ⚠️ | Oviedo | 1 |
| Forêt de Oviedo (66) ⚠️ | Oviedo | 1 |
| Bois de Cabrales (10) ⚠️ | Cabrales | 1 |
| Bois de Cabrales (23) ⚠️ | Cabrales | 1 |
| Parque Inglés ⚠️ | Carreño | 1 |
| Prao de San Antonio ⚠️ | Carreño | 1 |
| Parc de Oviedo (57) ⚠️ | Oviedo | 1 |
| Bois de Gijón (3) ⚠️ | Gijón | 1 |
| Forêt de Oviedo (68) ⚠️ | Oviedo | 1 |
| Forêt de Oviedo (71) ⚠️ | Oviedo | 1 |
| Parc de Oviedo (62) ⚠️ | Oviedo | 1 |
| Bois de Oviedo (11) ⚠️ | Oviedo | 1 |
| Bois de Oviedo (12) ⚠️ | Oviedo | 1 |
| Bois de Oviedo (15) ⚠️ | Oviedo | 1 |
| Bois de Oviedo (21) ⚠️ | Oviedo | 1 |
| Bois de Oviedo (25) ⚠️ | Oviedo | 1 |
| Bois de Oviedo (31) ⚠️ | Oviedo | 1 |
| Bois de Oviedo (32) ⚠️ | Oviedo | 1 |
| Bois de Oviedo (35) ⚠️ | Oviedo | 1 |
| Parc de Gijón (22) ⚠️ | Gijón | 1 |
| Bois de Oviedo (36) ⚠️ | Oviedo | 1 |
| Bois de Gijón (4) ⚠️ | Gijón | 1 |
| Forêt de Gijón (64) ⚠️ | Gijón | 1 |
| Forêt de Langreo (56) ⚠️ | Langreo | 1 |
| Forêt de Langreo (58) ⚠️ | Langreo | 1 |
| Forêt de Gijón (68) ⚠️ | Gijón | 1 |
| Bois de Gijón (8) ⚠️ | Gijón | 1 |
| Parc de Oviedo (69) ⚠️ | Oviedo | 1 |
| Parc de Ribera de Arriba ⚠️ | Ribera de Arriba | 1 |
| Bois de Gijón (10) ⚠️ | Gijón | 1 |
| Parc de Castrillón (2) ⚠️ | Castrillón | 1 |
| Bois de Cudillero ⚠️ | Cudillero | 1 |
| Parque Campo Grande ⚠️ | Samartín del Rei Aurelio | 1 |
| Bois de Illas ⚠️ | Illas | 1 |
| Forêt de Gijón (71) ⚠️ | Gijón | 1 |
| Parque Sogepsa ⚠️ | Gijón | 1 |
| Forêt de Gijón (73) ⚠️ | Gijón | 1 |
| Parc de Oviedo (73) ⚠️ | Oviedo | 1 |
| Forêt de Gijón (75) ⚠️ | Gijón | 1 |
| Forêt de Gijón (76) ⚠️ | Gijón | 1 |
| Parc de Oviedo (74) ⚠️ | Oviedo | 1 |
| Bois de Gijón (11) ⚠️ | Gijón | 1 |
| Forêt de Villaviciosa (69) ⚠️ | Villaviciosa | 1 |
| Bois de Gijón (14) ⚠️ | Gijón | 1 |
| Bois de Gijón (17) ⚠️ | Gijón | 1 |
| Forêt de Peñamellera Baja (23) ⚠️ | Peñamellera Baja | 1 |
| Bois de Gijón (19) ⚠️ | Gijón | 1 |
| Forêt de Ribadesella (60) ⚠️ | Ribadesella | 1 |
| Forêt de Gijón (84) ⚠️ | Gijón | 1 |
| Parc de Oviedo (76) ⚠️ | Oviedo | 1 |
| Parc de Oviedo (77) ⚠️ | Oviedo | 1 |
| Bois de Oviedo (44) ⚠️ | Oviedo | 1 |
| Forêt de Villaviciosa (70) ⚠️ | Villaviciosa | 1 |
| Forêt de Sariego (6) ⚠️ | Sariego | 1 |
| Forêt de Villaviciosa (79) ⚠️ | Villaviciosa | 1 |
| Forêt de Gijón (85) ⚠️ | Gijón | 1 |
| Bois de Cudillero (2) ⚠️ | Cudillero | 1 |
| Bois de Gijón (24) ⚠️ | Gijón | 1 |
| Forêt de Gijón (88) ⚠️ | Gijón | 1 |
| Bois de Gijón (25) ⚠️ | Gijón | 1 |
| Bois de Gijón (26) ⚠️ | Gijón | 1 |
| Forêt de Cabrales (16) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (17) ⚠️ | Cabrales | 1 |
| Bois de Riosa (2) ⚠️ | Riosa | 1 |
| Forêt de Gijón (92) ⚠️ | Gijón | 1 |
| Forêt de Cabrales (21) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (22) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (25) ⚠️ | Cabrales | 1 |
| Parque del Truébano ⚠️ | Oviedo | 1 |
| Forêt de Parres (26) ⚠️ | Parres | 1 |
| Forêt de Parres (27) ⚠️ | Parres | 1 |
| Forêt de Parres (28) ⚠️ | Parres | 1 |
| Forêt de Parres (33) ⚠️ | Parres | 1 |
| Forêt de Parres (35) ⚠️ | Parres | 1 |
| Parc de Belmonte de Miranda (2) ⚠️ | Belmonte de Miranda | 1 |
| Forêt de Cabrales (29) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (38) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (40) ⚠️ | Cabrales | 1 |
| Forêt de Gijón (95) ⚠️ | Gijón | 1 |
| Forêt de Cabrales (45) ⚠️ | Cabrales | 1 |
| Forêt de Gijón (97) ⚠️ | Gijón | 1 |
| Forêt de Vegadeo (19) ⚠️ | Vegadeo | 1 |
| Forêt de Taramundi (24) ⚠️ | Taramundi | 1 |
| Bois de Taramundi (5) ⚠️ | Taramundi | 1 |
| Forêt de Taramundi (39) ⚠️ | Taramundi | 1 |
| Forêt de Taramundi (42) ⚠️ | Taramundi | 1 |
| Forêt de Taramundi (43) ⚠️ | Taramundi | 1 |
| Bois de Taramundi (11) ⚠️ | Taramundi | 1 |
| Bois de Taramundi (13) ⚠️ | Taramundi | 1 |
| Forêt de Taramundi (53) ⚠️ | Taramundi | 1 |
| Bois de Taramundi (14) ⚠️ | Taramundi | 1 |
| Forêt de Taramundi (54) ⚠️ | Taramundi | 1 |
| Forêt de Taramundi (57) ⚠️ | Taramundi | 1 |
| Parque del Florán ⚠️ | Samartín del Rei Aurelio | 1 |
| Parque Polígono Montevil Oeste ⚠️ | Gijón | 1 |
| Forêt de Gozón (19) ⚠️ | Gozón | 1 |
| Bois de Gozón ⚠️ | Gozón | 1 |
| Forêt de Carreño (18) ⚠️ | Carreño | 1 |
| Forêt de Gozón (21) ⚠️ | Gozón | 1 |
| Parque del Frontón ⚠️ | Cangas de Onís | 1 |
| Forêt de Cabrales (50) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (54) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (58) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (62) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (63) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (65) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (66) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (73) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (75) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (78) ⚠️ | Cabrales | 1 |
| Parc de Castrillón (10) ⚠️ | Castrillón | 1 |
| Parc de Castrillón (14) ⚠️ | Castrillón | 1 |
| Forêt de Cabrales (87) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (93) ⚠️ | Cabrales | 1 |
| Forêt de Onís (3) ⚠️ | Onís | 1 |
| Forêt de Lena (35) ⚠️ | Lena | 1 |
| Forêt de Cabrales (97) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (100) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (103) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (105) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (112) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (113) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (118) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (120) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (125) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (126) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (128) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (133) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (137) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (145) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (152) ⚠️ | Cabrales | 1 |
| Bois de Carreño ⚠️ | Carreño | 1 |
| Forêt de Cabrales (163) ⚠️ | Cabrales | 1 |
| Parque Santarúa ⚠️ | Carreño | 1 |
| Forêt de Cabrales (179) ⚠️ | Cabrales | 1 |
| Forêt de Onís (8) ⚠️ | Onís | 1 |
| Forêt de Onís (10) ⚠️ | Onís | 1 |
| Forêt de Cabrales (186) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (189) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (197) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (199) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (200) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (202) ⚠️ | Cabrales | 1 |
| Forêt de Cabrales (203) ⚠️ | Cabrales | 1 |
| Forêt de Llanera (24) ⚠️ | Llanera | 1 |
| Forêt de Llanera (25) ⚠️ | Llanera | 1 |
| Bois de Llanes (4) ⚠️ | Llanes | 1 |
| Forêt de Gijón (100) ⚠️ | Gijón | 1 |
| Bois de Gijón (32) ⚠️ | Gijón | 1 |
| Bois de Gijón (34) ⚠️ | Gijón | 1 |
| Bois de Gijón (41) ⚠️ | Gijón | 1 |
| Bois de Gijón (46) ⚠️ | Gijón | 1 |
| Bois de Gijón (47) ⚠️ | Gijón | 1 |
| Parque del Príncipe ⚠️ | Cangas de Onís | 1 |
| Bois de Cangas del Narcea (2) ⚠️ | Cangas del Narcea | 1 |
| Bois de Llanes (5) ⚠️ | Llanes | 1 |
| Bois de Gijón (48) ⚠️ | Gijón | 1 |
| Parc de Villayón ⚠️ | Villayón | 1 |
| Forêt de Laviana (37) ⚠️ | Laviana | 1 |
| Forêt de Onís (15) ⚠️ | Onís | 1 |
| Forêt de Onís (16) ⚠️ | Onís | 1 |
| Forêt de Onís (25) ⚠️ | Onís | 1 |
| Forêt de Onís (36) ⚠️ | Onís | 1 |
| Forêt de Onís (38) ⚠️ | Onís | 1 |
| Forêt de Onís (43) ⚠️ | Onís | 1 |
| Forêt de Villaviciosa (81) ⚠️ | Villaviciosa | 1 |
| Forêt de Onís (45) ⚠️ | Onís | 1 |
| Forêt de Cangas de Onís (52) ⚠️ | Cangas de Onís | 1 |
| Forêt de Cangas de Onís (53) ⚠️ | Cangas de Onís | 1 |
| Forêt de Cangas de Onís (54) ⚠️ | Cangas de Onís | 1 |
| Forêt de Cangas de Onís (55) ⚠️ | Cangas de Onís | 1 |
| Forêt de Cangas de Onís (58) ⚠️ | Cangas de Onís | 1 |
| Forêt de Cangas de Onís (60) ⚠️ | Cangas de Onís | 1 |
| Forêt de Cangas de Onís (62) ⚠️ | Cangas de Onís | 1 |
| Forêt de Cangas de Onís (64) ⚠️ | Cangas de Onís | 1 |
| Forêt de Cangas de Onís (66) ⚠️ | Cangas de Onís | 1 |
| Forêt de Cangas de Onís (68) ⚠️ | Cangas de Onís | 1 |
| Forêt de Onís (49) ⚠️ | Onís | 1 |
| Forêt de Cangas de Onís (77) ⚠️ | Cangas de Onís | 1 |
| Forêt de Cangas de Onís (78) ⚠️ | Cangas de Onís | 1 |
| Bois de Allande (16) ⚠️ | Allande | 1 |
| Bois de Tineo (5) ⚠️ | Tineo | 1 |
| Forêt de Cangas de Onís (83) ⚠️ | Cangas de Onís | 1 |
| Forêt de Cangas de Onís (93) ⚠️ | Cangas de Onís | 1 |
| Forêt de Cangas de Onís (97) ⚠️ | Cangas de Onís | 1 |
| Forêt de Onís (55) ⚠️ | Onís | 1 |
| Forêt de Onís (58) ⚠️ | Onís | 1 |
| Forêt de Onís (59) ⚠️ | Onís | 1 |
| Forêt de Onís (64) ⚠️ | Onís | 1 |
| Forêt de Cangas de Onís (100) ⚠️ | Cangas de Onís | 1 |
| Forêt de Cangas de Onís (103) ⚠️ | Cangas de Onís | 1 |
| Forêt de Ribadesella (61) ⚠️ | Ribadesella | 1 |
| Parque de Cabruñana ⚠️ | Avilés | 1 |
| Bois de Siero (9) ⚠️ | Siero | 1 |
| Bois de Llanera (2) ⚠️ | Llanera | 1 |
| Forêt de Salas (49) ⚠️ | Salas | 1 |
| Forêt de Carreño (20) ⚠️ | Carreño | 1 |
| Bois de Gijón (53) ⚠️ | Carreño | 1 |
| Parque de Mohías ⚠️ | Coaña | 1 |
| Camino de Mataoveya ⚠️ | Gijón | 1 |
| Área Recreativa de Buelles ⚠️ | Peñamellera Baja | 1 |
| Bois de Quirós (6) ⚠️ | Quirós | 1 |
| Bois de Quirós (8) ⚠️ | Quirós | 1 |
| Bois de Quirós (13) ⚠️ | Quirós | 1 |
| Bois de Valdés (6) ⚠️ | Valdés | 1 |
| Parc de Parres (3) ⚠️ | Parres | 1 |
| Parc de Oviedo (87) ⚠️ | Oviedo | 1 |
| Parque Rafael Cuartas ⚠️ | Oviedo | 1 |
| Forêt de Gijón (104) ⚠️ | Gijón | 1 |
| Forêt de Gijón (105) ⚠️ | Gijón | 1 |
| Bois de Coaña (3) ⚠️ | Coaña | 1 |
| Bois de Salas (18) ⚠️ | Salas | 1 |
| Forêt de Salas (58) ⚠️ | Salas | 1 |
| Forêt de Salas (61) ⚠️ | Salas | 1 |
| Parque del Desarme ⚠️ | Oviedo | 1 |
| Bois de Valdés (7) ⚠️ | Valdés | 1 |
| Prau de La Rula ⚠️ | Soto del Barco | 1 |
| Parc de Gijón (42) ⚠️ | Gijón | 1 |
| Parc de Gijón (46) ⚠️ | Gijón | 1 |
| Parc de Gijón (50) ⚠️ | Gijón | 1 |
| Bois de Oviedo (66) ⚠️ | Oviedo | 1 |
| Forêt de Gijón (110) ⚠️ | Gijón | 1 |
| Forêt de Gijón (112) ⚠️ | Gijón | 1 |
| Forêt de Gijón (113) ⚠️ | Gijón | 1 |
| Forêt de Gijón (114) ⚠️ | Gijón | 1 |
| Forêt de Gijón (120) ⚠️ | Gijón | 1 |
| Forêt de Gijón (123) ⚠️ | Gijón | 1 |
| Parc de Gijón (54) ⚠️ | Gijón | 1 |
| Parc de Gijón (55) ⚠️ | Gijón | 1 |
| Forêt de Gijón (134) ⚠️ | Gijón | 1 |
| Forêt de Gijón (144) ⚠️ | Gijón | 1 |
| Bois de Oviedo (72) ⚠️ | Oviedo | 1 |
| Bois de Gijón (59) ⚠️ | Gijón | 1 |
| Bois de Oviedo (90) ⚠️ | Oviedo | 1 |
| Bois de Oviedo (91) ⚠️ | Oviedo | 1 |
| Bois de Oviedo (92) ⚠️ | Oviedo | 1 |
| Bois de Oviedo (95) ⚠️ | Oviedo | 1 |
| Bois de Oviedo (99) ⚠️ | Oviedo | 1 |
| Forêt de Llanera (27) ⚠️ | Llanera | 1 |
| Parque de Santa Bárbara ⚠️ | Avilés | 1 |
| Parc de Mieres (31) ⚠️ | Mieres | 1 |
| Parc de Gijón (57) ⚠️ | Gijón | 1 |
| Bois de Oviedo (101) ⚠️ | Oviedo | 1 |
| Bois de Oviedo (102) ⚠️ | Oviedo | 1 |
| Bois de Oviedo (103) ⚠️ | Oviedo | 1 |
| Bois de Oviedo (109) ⚠️ | Oviedo | 1 |
| Bois de Llanes (7) ⚠️ | Llanes | 1 |
| Bois de Llanes (8) ⚠️ | Llanes | 1 |
| Bois de Llanes (9) ⚠️ | Llanes | 1 |
| Bois de Oviedo (111) ⚠️ | Oviedo | 1 |
| Bois de Oviedo (113) ⚠️ | Oviedo | 1 |
| Bois de Oviedo (117) ⚠️ | Oviedo | 1 |
| Bois de Oviedo (121) ⚠️ | Oviedo | 1 |
| Parc de Gijón (58) ⚠️ | Gijón | 1 |
| Bois de Oviedo (125) ⚠️ | Oviedo | 1 |
| Forêt de Cudillero (53) ⚠️ | Cudillero | 1 |
| Bois de Oviedo (131) ⚠️ | Oviedo | 1 |
| Bois de Llanes (11) ⚠️ | Llanes | 1 |
| Bois de Llanes (12) ⚠️ | Llanes | 1 |
| Bois de Siero (15) ⚠️ | Siero | 1 |
| Bois de Llanes (14) ⚠️ | Llanes | 1 |
| Bois de Llanes (15) ⚠️ | Llanes | 1 |
| Bois de Llanes (16) ⚠️ | Llanes | 1 |
| Bois de Oviedo (134) ⚠️ | Oviedo | 1 |
| Bois de Llanes (18) ⚠️ | Llanes | 1 |
| Bois de Llanes (25) ⚠️ | Llanes | 1 |
| Bois de Llanes (29) ⚠️ | Llanes | 1 |
| Bois de Oviedo (138) ⚠️ | Oviedo | 1 |
| Parc de Gijón (59) ⚠️ | Gijón | 1 |
| Forêt de Llanera (28) ⚠️ | Llanera | 1 |
| Bois de Siero (17) ⚠️ | Siero | 1 |
| Bois de Oviedo (155) ⚠️ | Oviedo | 1 |
| Bois de Oviedo (156) ⚠️ | Oviedo | 1 |
| Bois de Tineo (17) ⚠️ | Tineo | 1 |
| Bois de Tineo (23) ⚠️ | Tineo | 1 |
| Bois de Peñamellera Baja (10) ⚠️ | Peñamellera Baja | 1 |
| Bois de Tineo (41) ⚠️ | Tineo | 1 |
| Bois de Tineo (45) ⚠️ | Tineo | 1 |
| Bois de Tineo (47) ⚠️ | Tineo | 1 |
| Bois de Oviedo (160) ⚠️ | Oviedo | 1 |
| Bois de Tineo (53) ⚠️ | Tineo | 1 |
| Bois de Tineo (60) ⚠️ | Tineo | 1 |
| Bois de Tineo (62) ⚠️ | Tineo | 1 |
| Bois de Tineo (65) ⚠️ | Tineo | 1 |
| Bois de Tineo (79) ⚠️ | Tineo | 1 |
| Parc de Corvera de Asturias (4) ⚠️ | Corvera de Asturias | 1 |
| Bois de Tineo (93) ⚠️ | Tineo | 1 |
| Bois de Tineo (95) ⚠️ | Tineo | 1 |
| Bois de Tineo (108) ⚠️ | Tineo | 1 |
| Forêt de Tineo (146) ⚠️ | Tineo | 1 |
| Forêt de Tineo (153) ⚠️ | Tineo | 1 |
| Bois de Oviedo (177) ⚠️ | Oviedo | 1 |
| Forêt de Villaviciosa (85) ⚠️ | Villaviciosa | 1 |
| Forêt de Villaviciosa (87) ⚠️ | Villaviciosa | 1 |
| Forêt de Villaviciosa (88) ⚠️ | Villaviciosa | 1 |
| Forêt de Villaviciosa (90) ⚠️ | Villaviciosa | 1 |
| Forêt de Villaviciosa (92) ⚠️ | Villaviciosa | 1 |
| Forêt de Villaviciosa (97) ⚠️ | Villaviciosa | 1 |
| Forêt de Villaviciosa (99) ⚠️ | Villaviciosa | 1 |
| Forêt de Villaviciosa (103) ⚠️ | Villaviciosa | 1 |
| Bois de Oviedo (188) ⚠️ | Oviedo | 1 |
| Forêt de Valdés (154) ⚠️ | Valdés | 1 |
| Forêt de Navia (14) ⚠️ | Navia | 1 |
| Forêt de Navia (17) ⚠️ | Navia | 1 |
| Forêt de Navia (105) ⚠️ | Navia | 1 |
| Forêt de Navia (117) ⚠️ | Navia | 1 |
| Forêt de Navia (121) ⚠️ | Navia | 1 |
| Forêt de Navia (130) ⚠️ | Navia | 1 |
| Bois de Oviedo (194) ⚠️ | Oviedo | 1 |
| Forêt de Tineo (211) ⚠️ | Tineo | 1 |
| Forêt de Tineo (216) ⚠️ | Tineo | 1 |
| Forêt de Tineo (260) ⚠️ | Tineo | 1 |
| Forêt de Tineo (268) ⚠️ | Tineo | 1 |
| Forêt de Tineo (288) ⚠️ | Tineo | 1 |
| Forêt de Tineo (291) ⚠️ | Tineo | 1 |
| Forêt de Tineo (306) ⚠️ | Tineo | 1 |
| Forêt de Tineo (307) ⚠️ | Tineo | 1 |
| Forêt de Villaviciosa (110) ⚠️ | Villaviciosa | 1 |
| Bois de Gijón (61) ⚠️ | Gijón | 1 |
| Forêt de Tineo (315) ⚠️ | Tineo | 1 |
| Forêt de Tineo (348) ⚠️ | Tineo | 1 |
| Forêt de Tineo (444) ⚠️ | Tineo | 1 |
| Forêt de Tineo (454) ⚠️ | Tineo | 1 |
| Forêt de Tineo (486) ⚠️ | Tineo | 1 |
| Forêt de Tineo (488) ⚠️ | Tineo | 1 |
| Forêt de Tineo (489) ⚠️ | Tineo | 1 |
| Forêt de Tineo (490) ⚠️ | Tineo | 1 |
| Forêt de Tineo (492) ⚠️ | Tineo | 1 |
| Forêt de Tineo (494) ⚠️ | Tineo | 1 |
| Forêt de Villaviciosa (111) ⚠️ | Villaviciosa | 1 |
| Bois de Tineo (120) ⚠️ | Tineo | 1 |
| Forêt de Villaviciosa (114) ⚠️ | Villaviciosa | 1 |
| Bois de Gijón (78) ⚠️ | Gijón | 1 |
| Forêt de Gijón (154) ⚠️ | Gijón | 1 |
| Forêt de Gijón (175) ⚠️ | Gijón | 1 |
| Forêt de Tineo (549) ⚠️ | Tineo | 1 |
| Forêt de Tineo (553) ⚠️ | Tineo | 1 |
| Forêt de Tineo (583) ⚠️ | Tineo | 1 |
| Forêt de Tineo (584) ⚠️ | Tineo | 1 |
| Forêt de Tineo (626) ⚠️ | Tineo | 1 |
| Forêt de Tineo (659) ⚠️ | Tineo | 1 |
| Forêt de Tineo (686) ⚠️ | Tineo | 1 |
| Forêt de Tineo (730) ⚠️ | Tineo | 1 |
| Forêt de Valdés (189) ⚠️ | Valdés | 1 |
| Forêt de Valdés (191) ⚠️ | Valdés | 1 |
| Forêt de Valdés (208) ⚠️ | Valdés | 1 |
| Forêt de Valdés (217) ⚠️ | Valdés | 1 |
| Forêt de Valdés (218) ⚠️ | Valdés | 1 |
| Forêt de Valdés (255) ⚠️ | Valdés | 1 |
| Forêt de Valdés (256) ⚠️ | Valdés | 1 |
| Forêt de Valdés (265) ⚠️ | Valdés | 1 |
| Forêt de Valdés (266) ⚠️ | Valdés | 1 |
| Forêt de Valdés (293) ⚠️ | Valdés | 1 |
| Forêt de Valdés (332) ⚠️ | Valdés | 1 |
| Forêt de Valdés (349) ⚠️ | Valdés | 1 |
| Forêt de Valdés (351) ⚠️ | Valdés | 1 |
| Forêt de Gijón (201) ⚠️ | Gijón | 1 |
| Forêt de Gijón (205) ⚠️ | Gijón | 1 |
| Forêt de Gijón (210) ⚠️ | Gijón | 1 |
| Forêt de Riosa (9) ⚠️ | Riosa | 1 |
| Forêt de Riosa (10) ⚠️ | Riosa | 1 |
| Parc de Laviana (11) ⚠️ | Laviana | 1 |
| Campu Lleres ⚠️ | Piloña | 1 |
| Forêt de Tineo (815) ⚠️ | Tineo | 1 |
| Forêt de Valdés (386) ⚠️ | Valdés | 1 |
| Forêt de Tineo (831) ⚠️ | Tineo | 1 |
| Forêt de Somiedo (104) ⚠️ | Somiedo | 1 |
| Forêt de Somiedo (138) ⚠️ | Somiedo | 1 |
| Forêt de Somiedo (164) ⚠️ | Somiedo | 1 |
| Forêt de Somiedo (165) ⚠️ | Somiedo | 1 |
| Forêt de Somiedo (173) ⚠️ | Somiedo | 1 |
| Forêt de Somiedo (178) ⚠️ | Somiedo | 1 |
| Forêt de Gijón (227) ⚠️ | Gijón | 1 |
| Forêt de Gijón (234) ⚠️ | Gijón | 1 |
| Forêt de Gijón (241) ⚠️ | Gijón | 1 |
| Forêt de Gijón (245) ⚠️ | Gijón | 1 |
| Forêt de Gijón (246) ⚠️ | Gijón | 1 |
| Forêt de Gijón (248) ⚠️ | Gijón | 1 |
| Forêt de Gijón (249) ⚠️ | Gijón | 1 |
| Forêt de Gijón (257) ⚠️ | Gijón | 1 |
| Forêt de Valdés (398) ⚠️ | Valdés | 1 |
| Forêt de Gijón (264) ⚠️ | Gijón | 1 |
| Forêt de Gijón (276) ⚠️ | Gijón | 1 |
| Forêt de Gijón (277) ⚠️ | Gijón | 1 |
| Playa verde 'Luis Enrique' ⚠️ | Gijón | 1 |
| Forêt de Castropol (21) ⚠️ | Castropol | 1 |
| Forêt de Castropol (26) ⚠️ | Castropol | 1 |
| Forêt de Castropol (28) ⚠️ | Castropol | 1 |
| Forêt de Castropol (34) ⚠️ | Castropol | 1 |
| Bois de Oviedo (221) ⚠️ | Oviedo | 1 |
| Bois de Oviedo (222) ⚠️ | Oviedo | 1 |
| Playa Verde 'Luis Enrique' ⚠️ | Gijón | 1 |
| Forêt de Caravia (6) ⚠️ | Caravia | 1 |
| Forêt de Cangas de Onís (123) ⚠️ | Cangas de Onís | 1 |
| Forêt de Parres (39) ⚠️ | Parres | 1 |
| Bois de Siero (29) ⚠️ | Oviedo | 1 |
| Bois de Oviedo (226) ⚠️ | Oviedo | 1 |
| Parque de Sueros ⚠️ | Mieres | 1 |
| Forêt de Piloña (76) ⚠️ | Piloña | 1 |
| Forêt de Castrillón (16) ⚠️ | Castrillón | 1 |
| Forêt de Ribadesella (66) ⚠️ | Ribadesella | 1 |
| Forêt de Ribadesella (69) ⚠️ | Ribadesella | 1 |
| Forêt de Parres (44) ⚠️ | Parres | 1 |
| Forêt de Parres (46) ⚠️ | Parres | 1 |
| Forêt de Parres (47) ⚠️ | Parres | 1 |
| El Llosu ⚠️ | Cabrales | 1 |
| Forêt de Parres (48) ⚠️ | Parres | 1 |
| Forêt de Parres (49) ⚠️ | Parres | 1 |
| Parc de Vegadeo ⚠️ | Vegadeo | 1 |
| Bois de Gozón (4) ⚠️ | Gozón | 1 |
| Forêt de Cudillero (54) ⚠️ | Cudillero | 1 |
| Forêt de Ribera de Arriba (8) ⚠️ | Ribera de Arriba | 1 |
| Forêt de Ribera de Arriba (9) ⚠️ | Oviedo | 1 |
| Forêt de Cudillero (56) ⚠️ | Cudillero | 1 |
| Forêt de Gijón (282) ⚠️ | Gijón | 1 |
| Forêt de Gijón (287) ⚠️ | Gijón | 1 |
| Forêt de Siero (54) ⚠️ | Siero | 1 |
| Bois de Avilés (3) ⚠️ | Avilés | 1 |
| Forêt de Gijón (291) ⚠️ | Gijón | 1 |
| Forêt de Gijón (294) ⚠️ | Gijón | 1 |
| Forêt de Gijón (295) ⚠️ | Gijón | 1 |
| Forêt de Gijón (298) ⚠️ | Gijón | 1 |
| Forêt de Gijón (301) ⚠️ | Gijón | 1 |
| Forêt de Llanera (36) ⚠️ | Llanera | 1 |
| Forêt de Llanera (37) ⚠️ | Llanera | 1 |
| Forêt de Llanera (38) ⚠️ | Llanera | 1 |
| Forêt de Llanera (40) ⚠️ | Llanera | 1 |
| Forêt de Gijón (303) ⚠️ | Gijón | 1 |
| Forêt de Gijón (311) ⚠️ | Gijón | 1 |
| Forêt de Gijón (312) ⚠️ | Gijón | 1 |
| Forêt de Gijón (313) ⚠️ | Gijón | 1 |
| Forêt de Gijón (316) ⚠️ | Gijón | 1 |
| Forêt de Gijón (318) ⚠️ | Gijón | 1 |
| Forêt de Gijón (322) ⚠️ | Gijón | 1 |
| Forêt de Gijón (326) ⚠️ | Gijón | 1 |
| Forêt de Gijón (328) ⚠️ | Gijón | 1 |
| Forêt de Gijón (332) ⚠️ | Gijón | 1 |
| Parque del Arquero José Fernández ⚠️ | Gijón | 1 |
| Jardines de la Filósofa Amelia Valcárcel ⚠️ | Gijón | 1 |
| Carbayera de Castiello ⚠️ | Gijón | 1 |
| Forêt de Taramundi (58) ⚠️ | Taramundi | 1 |
| Jardines de Samuel Gonzalez Granda ⚠️ | Gijón | 1 |
| Parque de las 13 Rosas ⚠️ | Gijón | 1 |
| Parque de Los Labradores ⚠️ | Pravia | 1 |
| Parque Rafaela Lozana ⚠️ | Gijón | 1 |
| Parque Primero de Mayo ⚠️ | Gijón | 1 |
| Carbayera de Granda ⚠️ | Gijón | 1 |
| Parque de Vicente Ferrer ⚠️ | Gijón | 1 |
| Parque del Cerro ⚠️ | Gijón | 1 |
| Parque de Rafael Marcos Delgado «Falín» ⚠️ | Gijón | 1 |
| Parque Puerto de Vegarada ⚠️ | Gijón | 1 |
| Parc de Samartín del Rei Aurelio (3) ⚠️ | Samartín del Rei Aurelio | 1 |
| Parque de La Memoria Histórica ⚠️ | Grado | 1 |
| Parque de El Floran ⚠️ | Samartín del Rei Aurelio | 1 |
| Parc de Candamo ⚠️ | Candamo | 1 |
| Parque Inglés (2) ⚠️ | Samartín del Rei Aurelio | 1 |
| Parc de Gijón (94) ⚠️ | Gijón | 1 |
| Parque Pinín ⚠️ | Langreo | 1 |
| Parque de la Plaza de Toros ⚠️ | Oviedo | 1 |
| Parque Cristino García Granda ⚠️ | Gijón | 1 |
| Bois de Castropol (3) ⚠️ | Castropol | 1 |
| Bois de Oviedo (234) ⚠️ | Oviedo | 1 |
| Parc de Ribadesella (3) ⚠️ | Ribadesella | 1 |
| Bois de Ribadesella (7) ⚠️ | Ribadesella | 1 |
| Bois de Ribadesella (8) ⚠️ | Ribadesella | 1 |
| Bois de Ribadesella (13) ⚠️ | Ribadesella | 1 |
| Bois de Ribadesella (14) ⚠️ | Ribadesella | 1 |
| Bois de Llanes (36) ⚠️ | Llanes | 1 |
| Bois de Llanes (41) ⚠️ | Llanes | 1 |
| Bois de Llanes (44) ⚠️ | Llanes | 1 |
| Bois de Llanes (48) ⚠️ | Llanes | 1 |
| Bois de Llanes (51) ⚠️ | Llanes | 1 |
| Bois de Llanes (54) ⚠️ | Llanes | 1 |
| Bois de Llanes (58) ⚠️ | Llanes | 1 |
| Bois de Llanes (60) ⚠️ | Llanes | 1 |
| Bois de Llanes (61) ⚠️ | Llanes | 1 |
| Bois de Llanes (63) ⚠️ | Llanes | 1 |
| Bois de Llanes (67) ⚠️ | Llanes | 1 |
| Bois de Llanes (74) ⚠️ | Llanes | 1 |
| Bois de Llanes (78) ⚠️ | Llanes | 1 |
| Bois de Llanes (79) ⚠️ | Llanes | 1 |
| Bois de Llanes (83) ⚠️ | Llanes | 1 |
| Bois de Llanes (84) ⚠️ | Llanes | 1 |
| Forêt de Tineo (954) ⚠️ | Tineo | 1 |
| Parque Antonio Ortega ⚠️ | Gijón | 1 |
| Parc de Gijón (97) ⚠️ | Gijón | 1 |
| Bois de Ponga (4) ⚠️ | Ponga | 1 |

3 109 parc(s) plus petits qu'une cellule ne sont pas listés : la carte les dessine, mais ils n'offrent aucune cellule.

⚠️ 4917 parc(s) hors de la fenêtre 10–125 cellules (4570 trop petit(s), 347 trop grand(s)) : affichés sur la carte, mais ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| military | 469 |
| airport | 85 |
| prison | 8 |
| **Total déclaré** | **562** |
| dont dans une zone de ce territoire | 561 |

Le jeu de données couvre plus large que le territoire — il est produit à une échelle supérieure. Seules les cellules tombant dans une zone d'ici pèsent sur un pourcentage.

### Zones concernées

| Zone | Cellules exclues |
|---|---:|
| Siero | 469 |
| Castrillón | 84 |
| Llanera | 8 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
