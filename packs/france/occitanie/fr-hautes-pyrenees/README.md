# Hautes-Pyrénées

Pack `fr-hautes-pyrenees` · version 1.0.1 · grille 200 m · France › Occitanie

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 210 254 |
| dont restreintes (aéroport, militaire, prison) | 518 |
| dont sans chemin (aucune voie à moins de 60 m) | 41 125 |
| dont en forêt, sans chemin non plus | 23 890 |
| dont traversées par un cours d'eau, sans chemin non plus | 7 723 |
| Cellules retirées par le masque d'eau | 1 409 |
| Villes | 469 |
| Arrondissements et quartiers | 0 |
| Îles | 10 |
| Parcs | 23 771 |

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
| Tarbes-Lourdes-Pyrénées | 28 984 | somme de 87 villes |
| Adour-Madiran (Hautes-Pyrénées) | 21 077 | somme de 61 villes |
| Aure Louron | 32 146 | somme de 46 villes |
| Neste Barousse | 14 224 | somme de 43 villes |
| Pyrénées Vallées des Gaves | 46 338 | somme de 46 villes |
| Haute-Bigorre | 18 248 | somme de 25 villes |
| Coteaux du Val-d'Arros | 12 054 | somme de 52 villes |
| Pays de Nay (Hautes-Pyrénées) | 1 513 | somme de 2 villes |
| Pays de Trie et du Magnoac | 15 508 | somme de 50 villes |
| Plateau de Lannemezan | 20 176 | somme de 57 villes |

Une île *composite* n'a pas de cellules à elle : sa progression est la somme de ses villes, et ses cellules ne lui sont jamais rattachées directement — elles compteraient deux fois.

## Villes (469)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Sans chemin | Parcs |
|---|---:|---:|---:|---:|---:|---:|---:|
| Gavarnie-Gèdre | 10 497 | 18 | 10 479 | 0 | **10 479** | 5 072 (48 %) | 413 |
| Cauterets | 7 348 | 51 | 7 297 | 0 | **7 297** | 3 413 (47 %) | 729 |
| Bagnères-de-Bigorre | 5 886 | 26 | 5 860 | 0 | **5 860** | 1 720 (29 %) | 345 |
| Aragnouet | 5 023 | 83 | 4 940 | 0 | **4 940** | 2 170 (44 %) | 290 |
| Arrens-Marsous | 4 635 | 45 | 4 590 | 0 | **4 590** | 1 961 (43 %) | 434 |
| Campan | 4 525 | 2 | 4 523 | 0 | **4 523** | 1 088 (24 %) | 341 |
| Saint-Lary-Soulan | 4 230 | 36 | 4 194 | 0 | **4 194** | 1 502 (36 %) | 267 |
| Estaing | 3 466 | 33 | 3 433 | 0 | **3 433** | 1 910 (56 %) | 210 |
| Ferrère | 2 690 | 2 | 2 688 | 0 | **2 688** | 409 (15 %) | 95 |
| Luz-Saint-Sauveur | 2 356 | 24 | 2 332 | 0 | **2 332** | 1 039 (45 %) | 101 |
| Barèges | 2 074 | 27 | 2 047 | 0 | **2 047** | 999 (49 %) | 320 |
| Loudenvielle | 2 020 | 43 | 1 977 | 0 | **1 977** | 978 (49 %) | 193 |
| Saint-Pé-de-Bigorre | 1 995 | 19 | 1 976 | 0 | **1 976** | 78 (4 %) | 130 |
| Ancizan | 1 940 | 0 | 1 940 | 0 | **1 940** | 616 (32 %) | 65 |
| Gazost | 1 913 | 1 | 1 912 | 0 | **1 912** | 541 (28 %) | 111 |
| Beaucens | 1 731 | 41 | 1 690 | 0 | **1 690** | 627 (37 %) | 155 |
| Hèches | 1 692 | 3 | 1 689 | 0 | **1 689** | 71 (4 %) | 121 |
| Lourdes | 1 735 | 49 | 1 686 | 0 | **1 686** | 47 (3 %) | 297 |
| Tramezaïgues | 1 626 | 4 | 1 622 | 0 | **1 622** | 732 (45 %) | 113 |
| Vielle-Aure | 1 638 | 64 | 1 574 | 0 | **1 574** | 554 (35 %) | 223 |
| Ibos | 1 559 | 2 | 1 557 | 0 | **1 557** | 91 (6 %) | 132 |
| Nistos | 1 540 | 0 | 1 540 | 0 | **1 540** | 105 (7 %) | 82 |
| Esparros | 1 508 | 0 | 1 508 | 0 | **1 508** | 83 (6 %) | 85 |
| Sarrancolin | 1 502 | 8 | 1 494 | 0 | **1 494** | 111 (7 %) | 57 |
| Vic-en-Bigorre | 1 516 | 26 | 1 490 | 0 | **1 490** | 211 (14 %) | 143 |
| Sost | 1 471 | 0 | 1 471 | 0 | **1 471** | 185 (13 %) | 67 |
| Sers | 1 427 | 6 | 1 421 | 0 | **1 421** | 561 (39 %) | 126 |
| Sazos | 1 419 | 7 | 1 412 | 0 | **1 412** | 738 (52 %) | 81 |
| Ossun | 1 319 | 0 | 1 319 | 227 | **1 092** | 102 (9 %) | 93 |
| Aulon | 1 317 | 0 | 1 317 | 0 | **1 317** | 613 (47 %) | 31 |
| Salles | 1 284 | 0 | 1 284 | 0 | **1 284** | 331 (26 %) | 84 |
| Azet | 1 249 | 3 | 1 246 | 0 | **1 246** | 533 (43 %) | 112 |
| Asté | 1 239 | 2 | 1 237 | 0 | **1 237** | 70 (6 %) | 58 |
| Arras-en-Lavedan | 1 157 | 4 | 1 153 | 0 | **1 153** | 149 (13 %) | 132 |
| Génos | 1 099 | 14 | 1 085 | 0 | **1 085** | 491 (45 %) | 114 |
| Capvern | 1 042 | 3 | 1 039 | 0 | **1 039** | 81 (8 %) | 229 |
| Maubourguet | 1 055 | 23 | 1 032 | 0 | **1 032** | 180 (17 %) | 135 |
| Bareilles | 984 | 0 | 984 | 0 | **984** | 107 (11 %) | 50 |
| Villelongue | 951 | 3 | 948 | 0 | **948** | 404 (43 %) | 67 |
| Monléon-Magnoac | 929 | 2 | 927 | 0 | **927** | 72 (8 %) | 134 |
| Beyrède-Jumet-Camous | 899 | 2 | 897 | 0 | **897** | 53 (6 %) | 37 |
| Lannemezan | 906 | 11 | 895 | 3 | **892** | 41 (5 %) | 284 |
| Cieutat | 884 | 0 | 884 | 0 | **884** | 95 (11 %) | 64 |
| Castelnau-Rivière-Basse | 877 | 10 | 867 | 0 | **867** | 58 (7 %) | 81 |
| Avezac-Prat-Lahitte | 826 | 0 | 826 | 0 | **826** | 30 (4 %) | 117 |
| Bordères-Louron | 828 | 4 | 824 | 0 | **824** | 96 (12 %) | 58 |
| Ferrières | 808 | 0 | 808 | 0 | **808** | 146 (18 %) | 52 |
| Betpouey | 803 | 4 | 799 | 0 | **799** | 441 (55 %) | 49 |
| Beaudéan | 774 | 1 | 773 | 0 | **773** | 112 (14 %) | 61 |
| Auriébat | 772 | 1 | 771 | 0 | **771** | 80 (10 %) | 128 |
| Vidouze | 773 | 5 | 768 | 0 | **768** | 103 (13 %) | 107 |
| Bordères-sur-l'Échez | 769 | 5 | 764 | 0 | **764** | 30 (4 %) | 82 |
| Asque | 737 | 0 | 737 | 0 | **737** | 47 (6 %) | 52 |
| Bonnefont | 735 | 9 | 726 | 0 | **726** | 66 (9 %) | 138 |
| Madiran | 719 | 3 | 716 | 0 | **716** | 32 (4 %) | 81 |
| Tarbes | 717 | 3 | 714 | 24 | **690** | 4 (1 %) | 87 |
| Azereix | 712 | 0 | 712 | 137 | **575** | 45 (8 %) | 37 |
| Arcizans-Avant | 715 | 5 | 710 | 0 | **710** | 139 (20 %) | 61 |
| Arbéost | 705 | 0 | 705 | 0 | **705** | 123 (17 %) | 69 |
| Gardères | 734 | 42 | 692 | 0 | **692** | 113 (16 %) | 96 |
| Tournay | 680 | 4 | 676 | 0 | **676** | 18 (3 %) | 93 |
| Recurt | 649 | 0 | 649 | 0 | **649** | 45 (7 %) | 58 |
| Galan | 644 | 4 | 640 | 0 | **640** | 53 (8 %) | 126 |
| Sacoué | 627 | 0 | 627 | 0 | **627** | 11 (2 %) | 26 |
| Saint-Lanne | 630 | 4 | 626 | 0 | **626** | 35 (6 %) | 52 |
| Bize | 614 | 0 | 614 | 0 | **614** | 37 (6 %) | 84 |
| Aucun | 613 | 0 | 613 | 0 | **613** | 9 (1 %) | 90 |
| Germs-sur-l'Oussouet | 610 | 0 | 610 | 0 | **610** | 66 (11 %) | 75 |
| Puydarrieux | 690 | 80 | 610 | 0 | **610** | 50 (8 %) | 97 |
| Labatut-Rivière | 613 | 7 | 606 | 0 | **606** | 98 (16 %) | 64 |
| Burg | 603 | 0 | 603 | 0 | **603** | 31 (5 %) | 127 |
| Sadournin | 589 | 0 | 589 | 4 | **585** | 79 (14 %) | 93 |
| Castelnau-Magnoac | 604 | 17 | 587 | 9 | **578** | 81 (14 %) | 137 |
| Montastruc | 586 | 0 | 586 | 0 | **586** | 31 (5 %) | 100 |
| Cazaux-Fréchet-Anéran-Camors | 579 | 0 | 579 | 0 | **579** | 129 (22 %) | 50 |
| Germ | 580 | 1 | 579 | 0 | **579** | 103 (18 %) | 47 |
| Aspin-Aure | 570 | 0 | 570 | 0 | **570** | 10 (2 %) | 38 |
| Jézeau | 570 | 0 | 570 | 0 | **570** | 59 (10 %) | 34 |
| Générest | 556 | 0 | 556 | 0 | **556** | 47 (8 %) | 30 |
| Pouyastruc | 556 | 0 | 556 | 0 | **556** | 47 (8 %) | 73 |
| Oursbelille | 541 | 1 | 540 | 0 | **540** | 27 (5 %) | 44 |
| Trie-sur-Baïse | 538 | 1 | 537 | 0 | **537** | 48 (9 %) | 73 |
| Saint-Lézer | 536 | 1 | 535 | 0 | **535** | 16 (3 %) | 37 |
| Clarens | 529 | 0 | 529 | 0 | **529** | 42 (8 %) | 98 |
| Bordes | 529 | 3 | 526 | 0 | **526** | 38 (7 %) | 114 |
| Arreau | 526 | 7 | 519 | 0 | **519** | 18 (3 %) | 59 |
| Sarriac-Bigorre | 515 | 0 | 515 | 0 | **515** | 134 (26 %) | 34 |
| Thermes-Magnoac | 516 | 1 | 515 | 0 | **515** | 55 (11 %) | 109 |
| Sariac-Magnoac | 516 | 4 | 512 | 0 | **512** | 80 (16 %) | 81 |
| Lamarque-Pontacq | 511 | 0 | 511 | 0 | **511** | 80 (16 %) | 55 |
| Ségus | 501 | 0 | 501 | 0 | **501** | 83 (17 %) | 63 |
| Monfaucon | 500 | 1 | 499 | 0 | **499** | 82 (16 %) | 95 |
| Sauveterre | 497 | 1 | 496 | 0 | **496** | 68 (14 %) | 58 |
| Larreule | 488 | 2 | 486 | 0 | **486** | 67 (14 %) | 51 |
| Saint-Laurent-de-Neste | 493 | 7 | 486 | 0 | **486** | 23 (5 %) | 121 |
| Trébons | 487 | 1 | 486 | 0 | **486** | 18 (4 %) | 59 |
| Campistrous | 479 | 0 | 479 | 0 | **479** | 42 (9 %) | 91 |
| Bazillac | 485 | 7 | 478 | 0 | **478** | 69 (14 %) | 70 |
| Bégole | 476 | 0 | 476 | 0 | **476** | 20 (4 %) | 87 |
| Orignac | 474 | 0 | 474 | 0 | **474** | 38 (8 %) | 49 |
| Labassère | 473 | 0 | 473 | 0 | **473** | 36 (8 %) | 111 |
| Chèze | 473 | 3 | 470 | 0 | **470** | 140 (30 %) | 31 |
| Mauvezin | 468 | 0 | 468 | 0 | **468** | 25 (5 %) | 73 |
| Barbazan-Debat | 465 | 0 | 465 | 0 | **465** | 12 (3 %) | 28 |
| Tarasteix | 464 | 0 | 464 | 0 | **464** | 44 (9 %) | 48 |
| Saint-Sever-de-Rustan | 465 | 3 | 462 | 0 | **462** | 46 (10 %) | 35 |
| Sombrun | 462 | 0 | 462 | 0 | **462** | 32 (7 %) | 43 |
| Aureilhan | 455 | 4 | 451 | 1 | **450** | 17 (4 %) | 41 |
| Grust | 451 | 0 | 451 | 0 | **451** | 70 (16 %) | 38 |
| Montgaillard | 449 | 3 | 446 | 0 | **446** | 6 (1 %) | 79 |
| Vier-Bordes | 442 | 0 | 442 | 0 | **442** | 110 (25 %) | 51 |
| Lascazères | 442 | 1 | 441 | 0 | **441** | 69 (16 %) | 40 |
| Séron | 442 | 2 | 440 | 0 | **440** | 47 (11 %) | 54 |
| Bazordan | 436 | 0 | 436 | 0 | **436** | 20 (5 %) | 92 |
| Rabastens-de-Bigorre | 438 | 3 | 435 | 0 | **435** | 36 (8 %) | 50 |
| Libaros | 429 | 0 | 429 | 0 | **429** | 52 (12 %) | 56 |
| Adervielle-Pouchergues | 426 | 0 | 426 | 0 | **426** | 67 (16 %) | 49 |
| Ozon | 429 | 4 | 425 | 0 | **425** | 21 (5 %) | 59 |
| Bernadets-Debat | 421 | 1 | 420 | 0 | **420** | 21 (5 %) | 68 |
| Sénac | 424 | 4 | 420 | 0 | **420** | 46 (11 %) | 58 |
| Oroix | 421 | 2 | 419 | 0 | **419** | 58 (14 %) | 33 |
| Fontrailles | 420 | 2 | 418 | 0 | **418** | 74 (18 %) | 62 |
| Lafitole | 418 | 1 | 417 | 0 | **417** | 61 (15 %) | 68 |
| Odos | 417 | 0 | 417 | 0 | **417** | 18 (4 %) | 71 |
| Bonrepos | 415 | 0 | 415 | 0 | **415** | 22 (5 %) | 72 |
| Chelle-Debat | 418 | 8 | 410 | 0 | **410** | 39 (10 %) | 41 |
| Esbareich | 409 | 0 | 409 | 0 | **409** | 20 (5 %) | 42 |
| Uglas | 405 | 1 | 404 | 0 | **404** | 28 (7 %) | 67 |
| Caixon | 403 | 0 | 403 | 0 | **403** | 40 (10 %) | 34 |
| Puntous | 403 | 1 | 402 | 0 | **402** | 36 (9 %) | 43 |
| Gaillagos | 399 | 0 | 399 | 0 | **399** | 41 (10 %) | 106 |
| Orleix | 396 | 0 | 396 | 0 | **396** | 31 (8 %) | 38 |
| Saint-Martin | 396 | 1 | 395 | 0 | **395** | 33 (8 %) | 67 |
| Castelbajac | 390 | 0 | 390 | 0 | **390** | 15 (4 %) | 70 |
| Arné | 389 | 0 | 389 | 0 | **389** | 29 (7 %) | 85 |
| Mont | 384 | 0 | 384 | 0 | **384** | 149 (39 %) | 42 |
| Ilhet | 386 | 3 | 383 | 0 | **383** | 5 (1 %) | 63 |
| Bernadets-Dessus | 382 | 0 | 382 | 0 | **382** | 9 (2 %) | 32 |
| Juillan | 383 | 3 | 380 | 13 | **367** | 6 (2 %) | 93 |
| Astugue | 375 | 0 | 375 | 0 | **375** | 16 (4 %) | 95 |
| Bourg-de-Bigorre | 374 | 0 | 374 | 0 | **374** | 18 (5 %) | 60 |
| Orieux | 380 | 6 | 374 | 0 | **374** | 33 (9 %) | 34 |
| Bénac | 373 | 0 | 373 | 0 | **373** | 15 (4 %) | 45 |
| Bouilh-Péreuilh | 373 | 1 | 372 | 0 | **372** | 18 (5 %) | 37 |
| Saint-Pastous | 369 | 0 | 369 | 0 | **369** | 50 (14 %) | 65 |
| Cizos | 368 | 0 | 368 | 0 | **368** | 49 (13 %) | 48 |
| Montoussé | 371 | 3 | 368 | 0 | **368** | 65 (18 %) | 77 |
| Luquet | 384 | 18 | 366 | 0 | **366** | 26 (7 %) | 53 |
| Gaussan | 363 | 0 | 363 | 0 | **363** | 28 (8 %) | 37 |
| Tuzaguet | 361 | 3 | 358 | 0 | **358** | 23 (6 %) | 60 |
| Antin | 359 | 5 | 354 | 0 | **354** | 34 (10 %) | 39 |
| La Barthe-de-Neste | 360 | 6 | 354 | 0 | **354** | 12 (3 %) | 81 |
| Thèbe | 354 | 0 | 354 | 0 | **354** | 18 (5 %) | 31 |
| Goudon | 356 | 3 | 353 | 0 | **353** | 36 (10 %) | 30 |
| Adé | 352 | 0 | 352 | 0 | **352** | 2 (1 %) | 40 |
| Pouzac | 354 | 2 | 352 | 0 | **352** | 16 (5 %) | 84 |
| Houeydets | 352 | 1 | 351 | 0 | **351** | 23 (7 %) | 45 |
| Galez | 349 | 1 | 348 | 0 | **348** | 29 (8 %) | 50 |
| Monlong | 344 | 0 | 344 | 0 | **344** | 26 (8 %) | 48 |
| Bartrès | 342 | 0 | 342 | 0 | **342** | 29 (8 %) | 77 |
| Sentous | 342 | 0 | 342 | 0 | **342** | 33 (10 %) | 32 |
| Guizerix | 340 | 0 | 340 | 0 | **340** | 45 (13 %) | 47 |
| Luby-Betmont | 339 | 1 | 338 | 0 | **338** | 47 (14 %) | 33 |
| Seich | 336 | 0 | 336 | 0 | **336** | 18 (5 %) | 55 |
| Aurensan | 337 | 3 | 334 | 0 | **334** | 40 (12 %) | 35 |
| Gazave | 331 | 0 | 331 | 0 | **331** | 3 (1 %) | 14 |
| Gerde | 329 | 0 | 329 | 0 | **329** | 7 (2 %) | 60 |
| Moulédous | 331 | 2 | 329 | 0 | **329** | 14 (4 %) | 15 |
| Saligos | 334 | 6 | 328 | 0 | **328** | 65 (20 %) | 55 |
| Larroque | 341 | 16 | 325 | 0 | **325** | 31 (10 %) | 72 |
| Montégut | 328 | 5 | 323 | 0 | **323** | 11 (3 %) | 31 |
| Ossen | 323 | 0 | 323 | 0 | **323** | 21 (7 %) | 40 |
| Saint-Paul | 323 | 0 | 323 | 0 | **323** | 26 (8 %) | 89 |
| Réjaumont | 322 | 0 | 322 | 0 | **322** | 15 (5 %) | 59 |
| Lacassagne | 318 | 0 | 318 | 0 | **318** | 52 (16 %) | 27 |
| Vignec | 317 | 0 | 317 | 0 | **317** | 65 (21 %) | 50 |
| Viscos | 317 | 3 | 314 | 0 | **314** | 31 (10 %) | 13 |
| Loubajac | 310 | 0 | 310 | 0 | **310** | 24 (8 %) | 58 |
| Tilhouse | 310 | 1 | 309 | 0 | **309** | 11 (4 %) | 37 |
| Lalanne | 307 | 0 | 307 | 0 | **307** | 48 (16 %) | 56 |
| Mazerolles | 303 | 1 | 302 | 0 | **302** | 25 (8 %) | 40 |
| Campuzan | 307 | 7 | 300 | 0 | **300** | 20 (7 %) | 22 |
| Tibiran-Jaunac | 302 | 2 | 300 | 0 | **300** | 11 (4 %) | 83 |
| Tostat | 299 | 0 | 299 | 0 | **299** | 44 (15 %) | 21 |
| Poueyferré | 298 | 0 | 298 | 0 | **298** | 10 (3 %) | 90 |
| Cadéac | 297 | 1 | 296 | 0 | **296** |  | 25 |
| Caussade-Rivière | 295 | 0 | 295 | 0 | **295** | 41 (14 %) | 31 |
| Clarac | 297 | 2 | 295 | 0 | **295** | 18 (6 %) | 43 |
| Peyret-Saint-André | 295 | 0 | 295 | 0 | **295** | 63 (21 %) | 60 |
| Soublecause | 295 | 1 | 294 | 0 | **294** | 27 (9 %) | 43 |
| Andrest | 292 | 0 | 292 | 0 | **292** | 25 (9 %) | 40 |
| Siarrouy | 295 | 3 | 292 | 0 | **292** | 21 (7 %) | 36 |
| Souyeaux | 292 | 0 | 292 | 0 | **292** | 19 (7 %) | 32 |
| Louey | 291 | 0 | 291 | 58 | **233** | 5 (2 %) | 50 |
| Séméac | 294 | 3 | 291 | 0 | **291** | 4 (1 %) | 41 |
| Escaunets | 302 | 13 | 289 | 0 | **289** | 41 (14 %) | 39 |
| Grailhen | 288 | 0 | 288 | 0 | **288** | 7 (2 %) | 6 |
| Ségalas | 286 | 0 | 286 | 0 | **286** | 46 (16 %) | 36 |
| Viey | 286 | 0 | 286 | 0 | **286** | 129 (45 %) | 39 |
| Agos-Vidalos | 291 | 7 | 284 | 0 | **284** | 23 (8 %) | 65 |
| Pinas | 281 | 0 | 281 | 0 | **281** | 20 (7 %) | 56 |
| Hères | 287 | 8 | 279 | 0 | **279** | 29 (10 %) | 41 |
| Julos | 279 | 0 | 279 | 0 | **279** | 22 (8 %) | 70 |
| Ardengost | 274 | 0 | 274 | 0 | **274** | 65 (24 %) | 15 |
| Cantaous | 274 | 0 | 274 | 0 | **274** | 15 (5 %) | 100 |
| Orincles | 273 | 0 | 273 | 0 | **273** | 6 (2 %) | 39 |
| Ordizan | 274 | 2 | 272 | 0 | **272** | 7 (3 %) | 67 |
| Berbérust-Lias | 271 | 0 | 271 | 0 | **271** | 37 (14 %) | 37 |
| Gouaux | 271 | 0 | 271 | 0 | **271** |  | 9 |
| Lahitte-Toupière | 271 | 0 | 271 | 0 | **271** | 18 (7 %) | 33 |
| Vielle-Adour | 271 | 0 | 271 | 0 | **271** | 14 (5 %) | 35 |
| Lanne | 270 | 0 | 270 | 16 | **254** | 5 (2 %) | 34 |
| Omex | 269 | 0 | 269 | 0 | **269** | 72 (27 %) | 48 |
| Labastide | 267 | 0 | 267 | 0 | **267** | 17 (6 %) | 49 |
| Estampures | 265 | 0 | 265 | 0 | **265** | 30 (11 %) | 26 |
| Lubret-Saint-Luc | 264 | 0 | 264 | 0 | **264** | 16 (6 %) | 12 |
| Tournous-Darré | 262 | 0 | 262 | 0 | **262** | 24 (9 %) | 27 |
| Cabanac | 266 | 5 | 261 | 0 | **261** | 19 (7 %) | 38 |
| Aries-Espénan | 261 | 1 | 260 | 0 | **260** | 14 (5 %) | 32 |
| Ourde | 260 | 0 | 260 | 0 | **260** | 21 (8 %) | 40 |
| Guchen | 260 | 1 | 259 | 0 | **259** | 7 (3 %) | 18 |
| Poumarous | 259 | 0 | 259 | 0 | **259** | 9 (3 %) | 24 |
| Villembits | 259 | 0 | 259 | 0 | **259** | 35 (14 %) | 48 |
| Fréchède | 257 | 3 | 254 | 0 | **254** | 13 (5 %) | 31 |
| Pujo | 252 | 0 | 252 | 0 | **252** | 42 (17 %) | 26 |
| Laméac | 252 | 1 | 251 | 0 | **251** | 15 (6 %) | 13 |
| Loudervielle | 251 | 0 | 251 | 4 | **247** | 49 (20 %) | 50 |
| Castelvieilh | 248 | 0 | 248 | 0 | **248** | 14 (6 %) | 39 |
| Mauléon-Barousse | 250 | 2 | 248 | 0 | **248** | 19 (8 %) | 26 |
| Bugard | 250 | 5 | 245 | 0 | **245** | 16 (7 %) | 29 |
| Izaux | 247 | 2 | 245 | 0 | **245** | 23 (9 %) | 47 |
| Lescurry | 244 | 0 | 244 | 0 | **244** | 17 (7 %) | 44 |
| Aventignan | 250 | 7 | 243 | 0 | **243** | 12 (5 %) | 40 |
| Arcizans-Dessus | 243 | 1 | 242 | 0 | **242** | 10 (4 %) | 58 |
| Lalanne-Trie | 242 | 0 | 242 | 0 | **242** | 15 (6 %) | 37 |
| Sère-Rustaing | 254 | 13 | 241 | 0 | **241** | 19 (8 %) | 27 |
| Banios | 240 | 0 | 240 | 0 | **240** | 5 (2 %) | 15 |
| Bonnemazon | 239 | 0 | 239 | 0 | **239** | 7 (3 %) | 33 |
| Arcizac-Adour | 241 | 3 | 238 | 0 | **238** | 3 (1 %) | 67 |
| Devèze | 239 | 1 | 238 | 0 | **238** | 29 (12 %) | 29 |
| Estirac | 246 | 9 | 237 | 0 | **237** | 49 (21 %) | 31 |
| Dours | 236 | 0 | 236 | 0 | **236** | 16 (7 %) | 22 |
| Louit | 234 | 0 | 234 | 0 | **234** | 25 (11 %) | 29 |
| Osmets | 234 | 0 | 234 | 0 | **234** | 2 (1 %) | 8 |
| Vieuzos | 234 | 1 | 233 | 0 | **233** | 26 (11 %) | 28 |
| Castéra-Lou | 232 | 1 | 231 | 0 | **231** | 23 (10 %) | 37 |
| Laslades | 245 | 14 | 231 | 0 | **231** | 11 (5 %) | 34 |
| Lustar | 231 | 0 | 231 | 0 | **231** | 24 (10 %) | 54 |
| Tajan | 231 | 0 | 231 | 0 | **231** | 29 (13 %) | 52 |
| Lagarde | 230 | 0 | 230 | 0 | **230** | 3 (1 %) | 13 |
| Ourdis-Cotdoussan | 230 | 0 | 230 | 0 | **230** | 30 (13 %) | 25 |
| Mun | 229 | 0 | 229 | 0 | **229** | 10 (4 %) | 48 |
| Nestier | 230 | 1 | 229 | 0 | **229** | 23 (10 %) | 55 |
| Artagnan | 233 | 5 | 228 | 0 | **228** | 36 (16 %) | 39 |
| Aubarède | 231 | 3 | 228 | 0 | **228** | 4 (2 %) | 41 |
| Luc | 228 | 0 | 228 | 0 | **228** | 18 (8 %) | 14 |
| Mascaras | 228 | 0 | 228 | 0 | **228** | 12 (5 %) | 30 |
| Vidou | 228 | 1 | 227 | 0 | **227** | 16 (7 %) | 32 |
| Arrayou-Lahitte | 226 | 0 | 226 | 0 | **226** | 12 (5 %) | 47 |
| Camalès | 226 | 1 | 225 | 0 | **225** | 31 (14 %) | 24 |
| Péré | 224 | 0 | 224 | 0 | **224** | 6 (3 %) | 29 |
| Ouzous | 222 | 0 | 222 | 0 | **222** | 71 (32 %) | 21 |
| Tournous-Devant | 222 | 0 | 222 | 0 | **222** | 23 (10 %) | 17 |
| Arrodets-ez-Angles | 219 | 0 | 219 | 0 | **219** | 20 (9 %) | 30 |
| Bernac-Dessus | 218 | 0 | 218 | 0 | **218** | 16 (7 %) | 38 |
| Peyrouse | 220 | 2 | 218 | 0 | **218** | 17 (8 %) | 58 |
| Cadeilhan-Trachère | 217 | 0 | 217 | 0 | **217** | 78 (36 %) | 37 |
| Horgues | 216 | 1 | 215 | 0 | **215** | 10 (5 %) | 31 |
| Chelle-Spou | 216 | 2 | 214 | 0 | **214** | 5 (2 %) | 37 |
| Lanespède | 214 | 0 | 214 | 0 | **214** |  | 22 |
| Nouilhan | 216 | 2 | 214 | 0 | **214** | 21 (10 %) | 22 |
| Trouley-Labarthe | 212 | 0 | 212 | 0 | **212** | 26 (12 %) | 24 |
| Marseillan | 210 | 1 | 209 | 0 | **209** | 14 (7 %) | 22 |
| Buzon | 208 | 0 | 208 | 0 | **208** | 40 (19 %) | 27 |
| Jarret | 208 | 0 | 208 | 0 | **208** | 6 (3 %) | 50 |
| Oueilloux | 208 | 0 | 208 | 0 | **208** | 10 (5 %) | 12 |
| Sarrouilles | 208 | 0 | 208 | 0 | **208** | 17 (8 %) | 36 |
| Saint-Arroman | 203 | 0 | 203 | 0 | **203** | 42 (21 %) | 39 |
| Averan | 201 | 0 | 201 | 0 | **201** | 6 (3 %) | 12 |
| Liac | 201 | 0 | 201 | 0 | **201** | 30 (15 %) | 36 |
| Bours | 219 | 19 | 200 | 0 | **200** | 11 (6 %) | 39 |
| Peyriguère | 198 | 0 | 198 | 0 | **198** | 3 (2 %) | 18 |
| Barbazan-Dessus | 197 | 0 | 197 | 0 | **197** | 13 (7 %) | 23 |
| Sère-Lanso | 195 | 0 | 195 | 0 | **195** | 13 (7 %) | 32 |
| Laloubère | 194 | 0 | 194 | 22 | **172** | 14 (8 %) | 44 |
| Betpouy | 193 | 0 | 193 | 0 | **193** | 10 (5 %) | 31 |
| Escots | 192 | 0 | 192 | 0 | **192** | 10 (5 %) | 30 |
| Saléchan | 194 | 3 | 191 | 0 | **191** | 15 (8 %) | 37 |
| Visker | 191 | 0 | 191 | 0 | **191** | 6 (3 %) | 24 |
| Peyrun | 192 | 2 | 190 | 0 | **190** | 20 (11 %) | 25 |
| Barlest | 187 | 0 | 187 | 0 | **187** | 12 (6 %) | 29 |
| Gez | 187 | 0 | 187 | 0 | **187** | 3 (2 %) | 31 |
| Bernac-Debat | 186 | 0 | 186 | 0 | **186** | 22 (12 %) | 19 |
| Artalens-Souin | 185 | 0 | 185 | 0 | **185** | 2 (1 %) | 78 |
| Sinzos | 199 | 15 | 184 | 0 | **184** | 15 (8 %) | 8 |
| Barrancoueu | 182 | 0 | 182 | 0 | **182** | 5 (3 %) | 12 |
| Saint-Savin | 181 | 0 | 181 | 0 | **181** | 25 (14 %) | 54 |
| Escala | 182 | 2 | 180 | 0 | **180** | 10 (6 %) | 47 |
| Bramevaque | 177 | 0 | 177 | 0 | **177** | 9 (5 %) | 12 |
| Oléac-Dessus | 177 | 0 | 177 | 0 | **177** | 6 (3 %) | 9 |
| Soues | 183 | 6 | 177 | 0 | **177** | 10 (6 %) | 35 |
| Caubous | 176 | 0 | 176 | 0 | **176** | 24 (14 %) | 27 |
| Escondeaux | 176 | 0 | 176 | 0 | **176** | 25 (14 %) | 22 |
| Loucrup | 175 | 0 | 175 | 0 | **175** | 13 (7 %) | 42 |
| Sabarros | 176 | 1 | 175 | 0 | **175** | 7 (4 %) | 23 |
| Villemur | 175 | 0 | 175 | 0 | **175** | 19 (11 %) | 38 |
| Allier | 174 | 0 | 174 | 0 | **174** | 13 (7 %) | 23 |
| Lansac | 188 | 15 | 173 | 0 | **173** | 9 (5 %) | 27 |
| Lapeyre | 173 | 1 | 172 | 0 | **172** | 9 (5 %) | 20 |
| Uzer | 172 | 0 | 172 | 0 | **172** | 4 (2 %) | 22 |
| Lagrange | 171 | 0 | 171 | 0 | **171** | 6 (4 %) | 36 |
| Benqué-Molère | 170 | 0 | 170 | 0 | **170** | 2 (1 %) | 24 |
| Lies | 170 | 0 | 170 | 0 | **170** | 6 (4 %) | 22 |
| Chis | 181 | 13 | 168 | 0 | **168** | 21 (12 %) | 9 |
| Marquerie | 166 | 0 | 166 | 0 | **166** | 8 (5 %) | 16 |
| Gensac | 166 | 1 | 165 | 0 | **165** | 31 (19 %) | 18 |
| Lutilhous | 164 | 0 | 164 | 0 | **164** | 4 (2 %) | 38 |
| Lortet | 169 | 6 | 163 | 0 | **163** | 18 (11 %) | 49 |
| Peyraube | 164 | 1 | 163 | 0 | **163** | 5 (3 %) | 28 |
| Sarlabous | 163 | 0 | 163 | 0 | **163** |  | 18 |
| Bulan | 162 | 0 | 162 | 0 | **162** | 17 (10 %) | 35 |
| Fréchet-Aure | 161 | 0 | 161 | 0 | **161** |  | 5 |
| Laran | 162 | 1 | 161 | 0 | **161** | 19 (12 %) | 12 |
| Layrisse | 161 | 0 | 161 | 0 | **161** | 14 (9 %) | 28 |
| Betbèze | 160 | 0 | 160 | 0 | **160** | 10 (6 %) | 23 |
| Bettes | 158 | 0 | 158 | 0 | **158** | 1 (1 %) | 30 |
| Moumoulous | 158 | 0 | 158 | 0 | **158** | 9 (6 %) | 17 |
| Castillon | 157 | 0 | 157 | 0 | **157** | 6 (4 %) | 20 |
| Ens | 157 | 0 | 157 | 0 | **157** | 20 (13 %) | 14 |
| Juncalas | 158 | 1 | 157 | 0 | **157** | 9 (6 %) | 51 |
| Mérilheu | 157 | 0 | 157 | 0 | **157** | 2 (1 %) | 20 |
| Ricaud | 155 | 3 | 152 | 0 | **152** | 2 (1 %) | 16 |
| Mazères-de-Neste | 156 | 5 | 151 | 0 | **151** | 9 (6 %) | 43 |
| Coussan | 150 | 0 | 150 | 0 | **150** | 10 (7 %) | 15 |
| Viger | 150 | 0 | 150 | 0 | **150** | 19 (13 %) | 39 |
| Villefranque | 150 | 0 | 150 | 0 | **150** | 12 (8 %) | 15 |
| Cazarilh | 149 | 0 | 149 | 0 | **149** | 10 (7 %) | 22 |
| Bizous | 150 | 2 | 148 | 0 | **148** | 8 (5 %) | 37 |
| Viella | 150 | 2 | 148 | 0 | **148** | 26 (18 %) | 26 |
| Avajan | 150 | 3 | 147 | 0 | **147** |  | 22 |
| Boô-Silhen | 150 | 3 | 147 | 0 | **147** | 2 (1 %) | 54 |
| Hiis | 147 | 0 | 147 | 0 | **147** | 9 (6 %) | 38 |
| Aveux | 146 | 0 | 146 | 0 | **146** | 5 (3 %) | 18 |
| Villenave-près-Béarn | 146 | 0 | 146 | 0 | **146** | 23 (16 %) | 21 |
| Cheust | 144 | 0 | 144 | 0 | **144** | 13 (9 %) | 28 |
| Argelès-Gazost | 144 | 1 | 143 | 0 | **143** | 1 (1 %) | 42 |
| Barbachen | 145 | 2 | 143 | 0 | **143** | 15 (10 %) | 17 |
| Ayzac-Ost | 143 | 2 | 141 | 0 | **141** | 7 (5 %) | 27 |
| Fréchou-Fréchet | 141 | 0 | 141 | 0 | **141** | 6 (4 %) | 21 |
| Hitte | 140 | 0 | 140 | 0 | **140** | 10 (7 %) | 16 |
| Artiguemy | 141 | 3 | 138 | 0 | **138** | 15 (11 %) | 24 |
| Bouilh-Devant | 141 | 3 | 138 | 0 | **138** | 9 (7 %) | 32 |
| Les Angles | 138 | 0 | 138 | 0 | **138** | 6 (4 %) | 36 |
| Soulom | 141 | 3 | 138 | 0 | **138** |  | 21 |
| Angos | 137 | 0 | 137 | 0 | **137** | 11 (8 %) | 23 |
| Lau-Balagnas | 138 | 1 | 137 | 0 | **137** | 3 (2 %) | 52 |
| Vielle-Louron | 136 | 0 | 136 | 0 | **136** | 11 (8 %) | 28 |
| Lançon | 133 | 0 | 133 | 0 | **133** | 1 (1 %) | 5 |
| Anla | 133 | 1 | 132 | 0 | **132** | 4 (3 %) | 31 |
| Bun | 132 | 0 | 132 | 0 | **132** | 11 (8 %) | 51 |
| Escoubès-Pouts | 132 | 0 | 132 | 0 | **132** | 4 (3 %) | 23 |
| Lomné | 132 | 0 | 132 | 0 | **132** | 9 (7 %) | 27 |
| Ourdon | 132 | 0 | 132 | 0 | **132** | 10 (8 %) | 8 |
| Gayan | 131 | 0 | 131 | 0 | **131** | 17 (13 %) | 19 |
| Troubat | 131 | 0 | 131 | 0 | **131** | 8 (6 %) | 16 |
| Lamarque-Rustaing | 135 | 5 | 130 | 0 | **130** | 11 (8 %) | 8 |
| Lespouey | 136 | 6 | 130 | 0 | **130** | 8 (6 %) | 17 |
| Bazet | 138 | 9 | 129 | 0 | **129** | 5 (4 %) | 19 |
| Sailhan | 129 | 0 | 129 | 0 | **129** | 12 (9 %) | 23 |
| Anères | 129 | 2 | 127 | 0 | **127** | 16 (13 %) | 31 |
| Marsas | 127 | 0 | 127 | 0 | **127** | 12 (9 %) | 19 |
| Ayros-Arbouix | 127 | 1 | 126 | 0 | **126** | 2 (2 %) | 63 |
| Espèche | 126 | 0 | 126 | 0 | **126** | 7 (6 %) | 26 |
| Guchan | 127 | 1 | 126 | 0 | **126** | 2 (2 %) | 21 |
| Siradan | 126 | 0 | 126 | 0 | **126** | 2 (2 %) | 20 |
| Argelès-Bagnères | 125 | 0 | 125 | 0 | **125** | 3 (2 %) | 28 |
| Lézignan | 125 | 0 | 125 | 0 | **125** | 1 (1 %) | 10 |
| Organ | 125 | 0 | 125 | 0 | **125** | 5 (4 %) | 12 |
| Barry | 122 | 0 | 122 | 0 | **122** |  | 24 |
| Bertren | 122 | 1 | 121 | 0 | **121** | 5 (4 %) | 26 |
| Samuran | 120 | 0 | 120 | 0 | **120** | 2 (2 %) | 10 |
| Boulin | 118 | 0 | 118 | 0 | **118** | 13 (11 %) | 11 |
| Lassales | 118 | 0 | 118 | 0 | **118** | 17 (14 %) | 17 |
| Geu | 124 | 7 | 117 | 0 | **117** | 1 (1 %) | 18 |
| Salles-Adour | 117 | 1 | 116 | 0 | **116** | 11 (9 %) | 22 |
| Antist | 114 | 0 | 114 | 0 | **114** | 1 (1 %) | 14 |
| Bazus-Neste | 116 | 2 | 114 | 0 | **114** | 10 (9 %) | 20 |
| Gez-ez-Angles | 114 | 0 | 114 | 0 | **114** | 1 (1 %) | 29 |
| Uz | 113 | 0 | 113 | 0 | **113** | 10 (9 %) | 10 |
| Izaourt | 113 | 1 | 112 | 0 | **112** | 2 (2 %) | 26 |
| Paréac | 112 | 0 | 112 | 0 | **112** | 3 (3 %) | 19 |
| Ousté | 111 | 0 | 111 | 0 | **111** | 9 (8 %) | 25 |
| Soréac | 111 | 0 | 111 | 0 | **111** | 13 (12 %) | 11 |
| Momères | 111 | 1 | 110 | 0 | **110** | 7 (6 %) | 19 |
| Neuilh | 110 | 0 | 110 | 0 | **110** | 2 (2 %) | 37 |
| Camparan | 109 | 0 | 109 | 0 | **109** | 1 (1 %) | 8 |
| Batsère | 108 | 0 | 108 | 0 | **108** | 7 (6 %) | 20 |
| Montsérié | 107 | 0 | 107 | 0 | **107** | 1 (1 %) | 23 |
| Ansost | 106 | 1 | 105 | 0 | **105** | 17 (16 %) | 5 |
| Esconnets | 105 | 0 | 105 | 0 | **105** |  | 13 |
| Collongues | 104 | 0 | 104 | 0 | **104** | 4 (4 %) | 17 |
| Hagedet | 104 | 0 | 104 | 0 | **104** | 7 (7 %) | 21 |
| Hauban | 104 | 0 | 104 | 0 | **104** | 8 (8 %) | 17 |
| Sabalos | 104 | 0 | 104 | 0 | **104** | 13 (12 %) | 18 |
| Calavanté | 101 | 0 | 101 | 0 | **101** | 8 (8 %) | 27 |
| Loures-Barousse | 106 | 5 | 101 | 0 | **101** | 8 (8 %) | 29 |
| Mansan | 101 | 0 | 101 | 0 | **101** | 1 (1 %) | 16 |
| Ossun-ez-Angles | 100 | 0 | 100 | 0 | **100** | 1 (1 %) | 17 |
| Sarniguet | 102 | 2 | 100 | 0 | **100** | 12 (12 %) | 9 |
| Espieilh | 98 | 0 | 98 | 0 | **98** | 3 (3 %) | 17 |
| Saint-Créac | 100 | 2 | 98 | 0 | **98** | 4 (4 %) | 50 |
| Fréchendets | 97 | 0 | 97 | 0 | **97** | 8 (8 %) | 7 |
| Hourc | 95 | 0 | 95 | 0 | **95** | 8 (8 %) | 12 |
| Grézian | 94 | 0 | 94 | 0 | **94** | 1 (1 %) | 14 |
| Ilheu | 94 | 0 | 94 | 0 | **94** | 9 (10 %) | 16 |
| Oléac-Debat | 92 | 0 | 92 | 0 | **92** | 11 (12 %) | 8 |
| Pouy | 91 | 0 | 91 | 0 | **91** | 14 (15 %) | 20 |
| Ris | 91 | 0 | 91 | 0 | **91** | 11 (12 %) | 2 |
| Arcizac-ez-Angles | 90 | 0 | 90 | 0 | **90** | 1 (1 %) | 22 |
| Bazus-Aure | 91 | 2 | 89 | 0 | **89** | 2 (2 %) | 22 |
| Jacque | 89 | 0 | 89 | 0 | **89** | 4 (4 %) | 15 |
| Bourisp | 88 | 0 | 88 | 0 | **88** |  | 18 |
| Casterets | 86 | 0 | 86 | 0 | **86** | 20 (23 %) | 18 |
| Esterre | 86 | 0 | 86 | 0 | **86** | 23 (27 %) | 11 |
| Sère-en-Lavedan | 86 | 0 | 86 | 0 | **86** | 3 (3 %) | 14 |
| Hachan | 86 | 1 | 85 | 0 | **85** | 3 (4 %) | 14 |
| Laborde | 85 | 0 | 85 | 0 | **85** | 3 (4 %) | 24 |
| Sarp | 86 | 2 | 84 | 0 | **84** | 1 (1 %) | 7 |
| Lizos | 83 | 0 | 83 | 0 | **83** | 4 (5 %) | 19 |
| Ger | 88 | 6 | 82 | 0 | **82** |  | 21 |
| Mingot | 82 | 0 | 82 | 0 | **82** | 5 (6 %) | 17 |
| Pierrefitte-Nestalas | 81 | 1 | 80 | 0 | **80** |  | 21 |
| Aspin-en-Lavedan | 82 | 3 | 79 | 0 | **79** |  | 36 |
| Sanous | 78 | 0 | 78 | 0 | **78** | 5 (6 %) | 6 |
| Sireix | 78 | 0 | 78 | 0 | **78** |  | 19 |
| Talazac | 75 | 0 | 75 | 0 | **75** | 4 (5 %) | 6 |
| Ugnouas | 75 | 0 | 75 | 0 | **75** | 10 (13 %) | 6 |
| Gaudent | 74 | 0 | 74 | 0 | **74** | 8 (11 %) | 23 |
| Hibarette | 74 | 0 | 74 | 0 | **74** |  | 13 |
| Marsac | 74 | 0 | 74 | 0 | **74** | 7 (9 %) | 6 |
| Estensan | 72 | 0 | 72 | 0 | **72** | 5 (7 %) | 10 |
| Pintac | 72 | 0 | 72 | 0 | **72** | 6 (8 %) | 5 |
| Cazaux-Debat | 72 | 1 | 71 | 0 | **71** |  | 16 |
| Préchac | 75 | 4 | 71 | 0 | **71** |  | 62 |
| Gourgue | 71 | 1 | 70 | 0 | **70** |  | 5 |
| Artigues | 69 | 0 | 69 | 0 | **69** | 1 (1 %) | 16 |
| Esquièze-Sère | 72 | 3 | 69 | 0 | **69** |  | 37 |
| Lombrès | 69 | 0 | 69 | 0 | **69** | 2 (3 %) | 13 |
| Barthe | 66 | 0 | 66 | 0 | **66** | 6 (9 %) | 4 |
| Hautaget | 66 | 0 | 66 | 0 | **66** | 6 (9 %) | 18 |
| Mazouau | 65 | 0 | 65 | 0 | **65** | 3 (5 %) | 8 |
| Bourréac | 62 | 0 | 62 | 0 | **62** | 2 (3 %) | 15 |
| Antichan | 55 | 0 | 55 | 0 | **55** | 3 (5 %) | 28 |
| Caharet | 55 | 0 | 55 | 0 | **55** | 2 (4 %) | 6 |
| Montignac | 52 | 0 | 52 | 0 | **52** | 2 (4 %) | 9 |
| Villenave-près-Marsac | 50 | 0 | 50 | 0 | **50** | 9 (18 %) | 2 |
| Adast | 49 | 0 | 49 | 0 | **49** | 1 (2 %) | 7 |
| Gembrie | 46 | 0 | 46 | 0 | **46** |  | 16 |
| Gonez | 48 | 2 | 46 | 0 | **46** | 1 (2 %) | 3 |
| Pailhac | 46 | 0 | 46 | 0 | **46** |  | 13 |
| Créchets | 45 | 0 | 45 | 0 | **45** | 6 (13 %) | 11 |
| Arrodets | 44 | 0 | 44 | 0 | **44** |  | 8 |
| Castéra-Lanusse | 43 | 0 | 43 | 0 | **43** | 4 (9 %) | 4 |
| Lhez | 41 | 0 | 41 | 0 | **41** |  | 6 |
| Estarvielle | 39 | 1 | 38 | 0 | **38** |  | 23 |
| Lugagnan | 37 | 3 | 34 | 0 | **34** | 1 (3 %) | 24 |
| Sassis | 29 | 3 | 26 | 0 | **26** |  | 11 |
| Thuy | 25 | 0 | 25 | 0 | **25** | 2 (8 %) |  |
| Sainte-Marie | 13 | 0 | 13 | 0 | **13** |  | 4 |

## Parcs (23771)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Forêt de Esparros (77) ⚠️ | Esparros › Plateau de Lannemezan | 1 591 |
| Forêt de Sost (34) ⚠️ | Sost › Neste Barousse | 1 543 |
| Forêt de Hèches (21) ⚠️ | Hèches › Plateau de Lannemezan | 1 386 |
| Forêt de Très Crouts ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 1 319 |
| Forêt de Générest (3) ⚠️ | Générest › Neste Barousse | 1 073 |
| Forêt de Ferrère (82) ⚠️ | Ferrère › Neste Barousse | 859 |
| Forêt de Ferrère (87) ⚠️ | Ferrère › Neste Barousse | 799 |
| Forêt de Sarrancolin (19) ⚠️ | Sarrancolin › Aure Louron | 791 |
| Forêt de Beyrède-Jumet-Camous (15) ⚠️ | Beyrède-Jumet-Camous › Aure Louron | 640 |
| Forêt de Grailhen (2) ⚠️ | Grailhen › Aure Louron | 639 |
| Forêt de Bagnères-de-Bigorre (225) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 574 |
| Forêt de Nistos (22) ⚠️ | Nistos › Neste Barousse | 561 |
| Forêt de Moulédous (13) ⚠️ | Moulédous › Coteaux du Val-d'Arros | 500 |
| Forêt de Asque (47) ⚠️ | Asque › Plateau de Lannemezan | 470 |
| Forêt de Ancizan (36) ⚠️ | Ancizan › Aure Louron | 469 |
| Forêt de Ferrère (83) ⚠️ | Ferrère › Neste Barousse | 432 |
| Forêt de Campan (314) ⚠️ | Campan › Haute-Bigorre | 414 |
| Forêt de Bordères-Louron (26) ⚠️ | Bordères-Louron › Aure Louron | 401 |
| Forêt de Lourdes (153) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 374 |
| Forêt de Samuran ⚠️ | Samuran › Neste Barousse | 367 |
| Forêt de Jézeau (10) ⚠️ | Jézeau › Aure Louron | 361 |
| Forêt de Bagnères-de-Bigorre (224) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 347 |
| Forêt de Ossen (3) ⚠️ | Ségus › Tarbes-Lourdes-Pyrénées | 331 |
| Forêt de Ibos (105) ⚠️ | Ibos › Tarbes-Lourdes-Pyrénées | 300 |
| Forêt de Saint-Lary-Soulan (205) ⚠️ | Saint-Lary-Soulan › Aure Louron | 299 |
| Forêt de Osmets (3) ⚠️ | Osmets › Pays de Trie et du Magnoac | 281 |
| Forêt de Saint-Lary-Soulan (206) ⚠️ | Saint-Lary-Soulan › Aure Louron | 280 |
| Forêt de Cauterets (672) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 274 |
| Forêt de Sarrancolin (20) ⚠️ | Sarrancolin › Aure Louron | 253 |
| Forêt de Guchen (3) ⚠️ | Guchen › Aure Louron | 253 |
| Forêt de Asté (50) ⚠️ | Asté › Haute-Bigorre | 249 |
| Forêt de Bagnères-de-Bigorre (238) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 241 |
| Forêt de Hèches (22) ⚠️ | Sarrancolin › Aure Louron | 236 |
| Forêt de Bagnères-de-Bigorre (233) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 227 |
| Forêt de Ferrières (41) ⚠️ | Ferrières › Pays de Nay (Hautes-Pyrénées) | 223 |
| Forêt de Cauterets (668) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 219 |
| Forêt de Souyeaux (15) ⚠️ | Souyeaux › Coteaux du Val-d'Arros | 218 |
| Forêt de Lourdes (152) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 217 |
| Forêt de Banios (15) ⚠️ | Banios › Haute-Bigorre | 212 |
| Forêt de Tournay (88) ⚠️ | Tournay › Coteaux du Val-d'Arros | 210 |
| Forêt de Bouilh-Péreuilh (18) ⚠️ | Bouilh-Péreuilh › Coteaux du Val-d'Arros | 209 |
| Forêt de Cieutat (63) ⚠️ | Cieutat › Haute-Bigorre | 208 |
| Forêt de Grust (27) ⚠️ | Grust › Pyrénées Vallées des Gaves | 203 |
| Forêt de Ricaud (16) ⚠️ | Ricaud › Coteaux du Val-d'Arros | 203 |
| Forêt de Campan (299) ⚠️ | Campan › Haute-Bigorre | 198 |
| Forêt de Saint-Lary-Soulan (207) ⚠️ | Saint-Lary-Soulan › Aure Louron | 198 |
| Forêt de Bareilles (27) ⚠️ | Bareilles › Aure Louron | 197 |
| Bois de Cauterets (41) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 196 |
| Forêt de Aragnouet (205) ⚠️ | Aragnouet › Aure Louron | 189 |
| Forêt de Ferrières (37) ⚠️ | Ferrières › Pays de Nay (Hautes-Pyrénées) | 185 |
| Forêt de Peyriguère (7) ⚠️ | Peyriguère › Coteaux du Val-d'Arros | 182 |
| Bois du Commandeur ⚠️ | Bordères-sur-l'Échez › Tarbes-Lourdes-Pyrénées | 180 |
| Forêt de Campan (305) ⚠️ | Campan › Haute-Bigorre | 178 |
| Forêt de Campan (315) ⚠️ | Campan › Haute-Bigorre | 173 |
| Forêt de Gavarnie-Gèdre (323) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 172 |
| Forêt de Aveux (2) ⚠️ | Aveux › Neste Barousse | 172 |
| Forêt de Gouaux ⚠️ | Gouaux › Aure Louron | 172 |
| Forêt de Ossun (65) ⚠️ | Ossun › Tarbes-Lourdes-Pyrénées | 170 |
| Forêt de Génos (52) ⚠️ | Génos › Aure Louron | 169 |
| Forêt de Bégole (15) ⚠️ | Bégole › Coteaux du Val-d'Arros | 168 |
| Forêt de Galan (13) ⚠️ | Recurt › Plateau de Lannemezan | 168 |
| Forêt de Sazos (50) ⚠️ | Sazos › Pyrénées Vallées des Gaves | 167 |
| Forêt de Vielle-Aure (197) ⚠️ | Vielle-Aure › Aure Louron | 166 |
| Forêt de Arras-en-Lavedan (78) ⚠️ | Arras-en-Lavedan › Pyrénées Vallées des Gaves | 164 |
| Forêt de Chèze (15) ⚠️ | Chèze › Pyrénées Vallées des Gaves | 162 |
| Foret de Campuzan ⚠️ | Campuzan › Pays de Trie et du Magnoac | 162 |
| Forêt de Cauterets (674) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 158 |
| Forêt de Cauterets (679) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 158 |
| Forêt de Cadéac (4) ⚠️ | Cadéac › Aure Louron | 158 |
| Forêt de Tibiran-Jaunac (20) ⚠️ | Tibiran-Jaunac › Neste Barousse | 158 |
| Bois de Marmajou ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 158 |
| Forêt de Bordères-Louron (25) ⚠️ | Bordères-Louron › Aure Louron | 157 |
| Forêt de Barbazan-Debat (18) ⚠️ | Barbazan-Debat › Tarbes-Lourdes-Pyrénées | 156 |
| Forêt d'Arragnat ⚠️ | Arcizans-Dessus › Pyrénées Vallées des Gaves | 155 |
| Forêt de Ibos (110) ⚠️ | Ibos › Tarbes-Lourdes-Pyrénées | 155 |
| Forêt de Aucun (73) ⚠️ | Aucun › Pyrénées Vallées des Gaves | 152 |
| Forêt de Aragnouet (201) ⚠️ | Aragnouet › Aure Louron | 150 |
| Forêt de Averan (7) ⚠️ | Averan › Tarbes-Lourdes-Pyrénées | 150 |
| Forêt de Ozon (55) ⚠️ | Ozon › Coteaux du Val-d'Arros | 150 |
| Forêt de Aubarède (6) ⚠️ | Aubarède › Coteaux du Val-d'Arros | 150 |
| Forêt de Aragnouet (212) ⚠️ | Aragnouet › Aure Louron | 148 |
| Forêt de Cieutat (64) ⚠️ | Cieutat › Haute-Bigorre | 144 |
| Forêt de Clarens (17) ⚠️ | Clarens › Plateau de Lannemezan | 144 |
| Forêt de Gazost (38) ⚠️ | Gazost › Tarbes-Lourdes-Pyrénées | 141 |
| Forêt de Fréchède (10) ⚠️ | Fréchède › Pays de Trie et du Magnoac | 141 |
| Forêt de Villefranque (2) ⚠️ | Sombrun › Adour-Madiran (Hautes-Pyrénées) | 140 |
| Forêt de Aspin-Aure (10) ⚠️ | Aspin-Aure › Aure Louron | 139 |
| Forêt de Salles (27) ⚠️ | Salles › Pyrénées Vallées des Gaves | 137 |
| Forêt de Lourdes (144) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 135 |
| Forêt de Chelle-Debat (4) ⚠️ | Chelle-Debat › Coteaux du Val-d'Arros | 135 |
| Forêt de Saint-Lary-Soulan (204) ⚠️ | Saint-Lary-Soulan › Aure Louron | 134 |
| Forêt de Luz-Saint-Sauveur (39) ⚠️ | Luz-Saint-Sauveur › Pyrénées Vallées des Gaves | 132 |
| Forêt de Sazos (51) ⚠️ | Sazos › Pyrénées Vallées des Gaves | 131 |
| Forêt de Luz-Saint-Sauveur (41) ⚠️ | Luz-Saint-Sauveur › Pyrénées Vallées des Gaves | 131 |
| Forêt de Uzer (17) ⚠️ | Uzer › Haute-Bigorre | 131 |
| Forêt de Tournay (89) ⚠️ | Tournay › Coteaux du Val-d'Arros | 131 |
| Forêt de Nistos (19) ⚠️ | Nistos › Neste Barousse | 130 |
| Forêt de Bernadets-Debat (8) ⚠️ | Bernadets-Debat › Pays de Trie et du Magnoac | 129 |
| Forêt de Villelongue (43) ⚠️ | Villelongue › Pyrénées Vallées des Gaves | 128 |
| Forêt de Guizerix (3) ⚠️ | Guizerix › Pays de Trie et du Magnoac | 128 |
| Forêt de Lalanne (5) ⚠️ | Lalanne › Pays de Trie et du Magnoac | 128 |
| Forêt de Aragnouet (202) ⚠️ | Aragnouet › Aure Louron | 128 |
| Forêt de Viscos (10) ⚠️ | Viscos › Pyrénées Vallées des Gaves | 128 |
| Forêt de Mauvezin (73) ⚠️ | Mauvezin › Plateau de Lannemezan | 127 |
| Forêt de Avezac-Prat-Lahitte (109) | Avezac-Prat-Lahitte › Plateau de Lannemezan | 124 |
| Forêt de Cadéac (5) | Cadéac › Aure Louron | 124 |
| Forêt de Recurt (26) | Recurt › Plateau de Lannemezan | 124 |
| Forêt de Aragnouet (210) | Aragnouet › Aure Louron | 124 |
| Forêt de Sombrun (3) | Sombrun › Adour-Madiran (Hautes-Pyrénées) | 124 |
| Forêt de Gazost (40) | Gazost › Tarbes-Lourdes-Pyrénées | 123 |
| Forêt de Sarrancolin (21) | Sarrancolin › Aure Louron | 123 |
| Forêt de Soublecause (10) | Soublecause › Adour-Madiran (Hautes-Pyrénées) | 122 |
| Forêt de Oursbelille (22) | Oursbelille › Tarbes-Lourdes-Pyrénées | 121 |
| Forêt de Asté (51) | Asté › Haute-Bigorre | 119 |
| Forêt de Lies (22) | Lies › Haute-Bigorre | 119 |
| Forêt de Adervielle-Pouchergues (22) | Adervielle-Pouchergues › Aure Louron | 119 |
| Forêt de Tramezaïgues (107) | Tramezaïgues › Aure Louron | 119 |
| Forêt de Tarasteix (14) | Tarasteix › Adour-Madiran (Hautes-Pyrénées) | 118 |
| Forêt de Salles (29) | Salles › Pyrénées Vallées des Gaves | 118 |
| Forêt de Bareilles (28) | Bareilles › Aure Louron | 118 |
| Forêt de Ourdon | Ourdon › Tarbes-Lourdes-Pyrénées | 117 |
| Forêt de Sinzos (7) | Sinzos › Coteaux du Val-d'Arros | 117 |
| Forêt de Gavarnie-Gèdre (328) | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 116 |
| Forêt de Monléon-Magnoac (16) | Monléon-Magnoac › Pays de Trie et du Magnoac | 113 |
| Forêt de Sarrancolin (22) | Sarrancolin › Aure Louron | 113 |
| Forêt de Gazost (44) | Gazost › Tarbes-Lourdes-Pyrénées | 112 |
| Forêt de Berbérust-Lias (21) | Berbérust-Lias › Tarbes-Lourdes-Pyrénées | 111 |
| Forêt de Trébons (43) | Trébons › Haute-Bigorre | 111 |
| Forêt de Germs-sur-l'Oussouet (13) | Germs-sur-l'Oussouet › Tarbes-Lourdes-Pyrénées | 111 |
| Forêt de Arrens-Marsous (261) | Arrens-Marsous › Pyrénées Vallées des Gaves | 111 |
| Forêt de Sentous (3) | Tournous-Darré › Pays de Trie et du Magnoac | 110 |
| Forêt de Gez (11) | Gez › Pyrénées Vallées des Gaves | 110 |
| Forêt de Cauterets (670) | Cauterets › Pyrénées Vallées des Gaves | 109 |
| Forêt de Campan (307) | Campan › Haute-Bigorre | 109 |
| Forêt de Bartrès (45) | Bartrès › Tarbes-Lourdes-Pyrénées | 108 |
| Forêt de Tilhouse (33) | Tilhouse › Plateau de Lannemezan | 108 |
| Forêt de Cauterets (3) | Cauterets › Pyrénées Vallées des Gaves | 107 |
| Forêt de Cauterets (669) | Cauterets › Pyrénées Vallées des Gaves | 107 |
| Forêt de Laran (4) | Laran › Pays de Trie et du Magnoac | 107 |
| Forêt de Mun (16) | Mun › Pays de Trie et du Magnoac | 106 |
| Forêt de Gavarnie-Gèdre (327) | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 105 |
| Forêt de Ferrières (39) | Ferrières › Pays de Nay (Hautes-Pyrénées) | 105 |
| Forêt de Orleix (31) | Orleix › Tarbes-Lourdes-Pyrénées | 105 |
| Forêt de Escots (29) | Escots › Plateau de Lannemezan | 104 |
| Forêt de Sentous (4) | Bonnefont › Pays de Trie et du Magnoac | 102 |
| Forêt de Lançon (5) | Lançon › Aure Louron | 102 |
| Forêt de Asté (3) | Asté › Haute-Bigorre | 101 |
| Forêt de Gerde (56) | Gerde › Haute-Bigorre | 101 |
| Forêt de Monlong (6) | Monlong › Pays de Trie et du Magnoac | 100 |
| Forêt de Luz-Saint-Sauveur (42) | Luz-Saint-Sauveur › Pyrénées Vallées des Gaves | 100 |
| Forêt de Saint-Lézer (26) | Saint-Lézer › Adour-Madiran (Hautes-Pyrénées) | 99 |
| Forêt de Ourdis-Cotdoussan (3) | Ourdis-Cotdoussan › Tarbes-Lourdes-Pyrénées | 99 |
| Forêt de Montégut (8) | Montégut › Neste Barousse | 99 |
| Forêt de Labatut-Rivière (15) | Labatut-Rivière › Adour-Madiran (Hautes-Pyrénées) | 97 |
| Bois de Bégole (69) | Bégole › Plateau de Lannemezan | 97 |
| Forêt de Uglas (14) | Uglas › Plateau de Lannemezan | 97 |
| Forêt de Auriébat (17) | Auriébat › Adour-Madiran (Hautes-Pyrénées) | 96 |
| Bois de Arrens-Marsous (167) | Arrens-Marsous › Pyrénées Vallées des Gaves | 95 |
| Forêt de Saligos (27) | Saligos › Pyrénées Vallées des Gaves | 95 |
| Forêt de Barèges (215) | Barèges › Pyrénées Vallées des Gaves | 95 |
| Forêt de Arras-en-Lavedan (75) | Arras-en-Lavedan › Pyrénées Vallées des Gaves | 94 |
| Forêt de Labassère (64) | Labassère › Haute-Bigorre | 94 |
| Forêt de Ossun (61) | Ossun › Tarbes-Lourdes-Pyrénées | 94 |
| Forêt de Ossun (64) | Ossun › Tarbes-Lourdes-Pyrénées | 94 |
| Forêt de Ferrère (86) | Ferrère › Neste Barousse | 94 |
| Forêt de Salles (33) | Salles › Pyrénées Vallées des Gaves | 93 |
| Forêt de Sère-Lanso (25) | Sère-Lanso › Tarbes-Lourdes-Pyrénées | 92 |
| Forêt de Orignac (48) | Orignac › Haute-Bigorre | 91 |
| Forêt de Salles (26) | Salles › Pyrénées Vallées des Gaves | 90 |
| Forêt de Saint-Savin (22) | Saint-Savin › Pyrénées Vallées des Gaves | 90 |
| Forêt de Barbazan-Debat (20) | Barbazan-Debat › Tarbes-Lourdes-Pyrénées | 90 |
| Forêt de Gazost | Gazost › Tarbes-Lourdes-Pyrénées | 89 |
| Forêt de Arrens-Marsous (236) | Arrens-Marsous › Pyrénées Vallées des Gaves | 89 |
| Forêt de Lansac (11) | Lansac › Coteaux du Val-d'Arros | 89 |
| Forêt de Azet (57) | Azet › Aure Louron | 89 |
| Forêt de Louey (45) | Louey › Tarbes-Lourdes-Pyrénées | 88 |
| Forêt de Campistrous (29) | Campistrous › Plateau de Lannemezan | 88 |
| Forêt de Barbazan-Dessus (27) | Hitte › Coteaux du Val-d'Arros | 87 |
| Forêt de Cazaux-Fréchet-Anéran-Camors (8) | Cazaux-Fréchet-Anéran-Camors › Aure Louron | 86 |
| Forêt de Arras-en-Lavedan (83) | Arras-en-Lavedan › Pyrénées Vallées des Gaves | 86 |
| Forêt de Ordizan (60) | Ordizan › Haute-Bigorre | 86 |
| Forêt de Bazus-Aure (4) | Bazus-Aure › Aure Louron | 86 |
| Forêt de Saint-Pastous (13) | Saint-Pastous › Pyrénées Vallées des Gaves | 85 |
| Forêt de Lanne (32) | Lanne › Tarbes-Lourdes-Pyrénées | 85 |
| Forêt de Benqué-Molère (16) | Benqué-Molère › Plateau de Lannemezan | 85 |
| Forêt de Oueilloux (12) | Oueilloux › Coteaux du Val-d'Arros | 82 |
| Forêt de Gavarnie-Gèdre (324) | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 81 |
| Forêt de Arbéost (60) | Arbéost › Pays de Nay (Hautes-Pyrénées) | 81 |
| Forêt de Campan (300) | Campan › Haute-Bigorre | 81 |
| Forêt de Campan (313) | Campan › Haute-Bigorre | 81 |
| Forêt de Maubourguet (18) | Lahitte-Toupière › Adour-Madiran (Hautes-Pyrénées) | 81 |
| Forêt de Escots (30) | Escots › Plateau de Lannemezan | 80 |
| Forêt de Laméac (4) | Laméac › Adour-Madiran (Hautes-Pyrénées) | 80 |
| Forêt de Cadeilhan-Trachère (33) | Cadeilhan-Trachère › Aure Louron | 80 |
| Forêt de Lourdes (154) | Lourdes › Tarbes-Lourdes-Pyrénées | 80 |
| Forêt de Germs-sur-l'Oussouet (10) | Germs-sur-l'Oussouet › Tarbes-Lourdes-Pyrénées | 79 |
| Forêt de Arrayou-Lahitte (39) | Arrayou-Lahitte › Tarbes-Lourdes-Pyrénées | 79 |
| Forêt de Saligos (28) | Saligos › Pyrénées Vallées des Gaves | 78 |
| Forêt de Larroque (12) | Larroque › Pays de Trie et du Magnoac | 78 |
| Forêt de Bagnères-de-Bigorre (2) | Bagnères-de-Bigorre › Haute-Bigorre | 77 |
| Forêt de Lascazères (2) | Lascazères › Adour-Madiran (Hautes-Pyrénées) | 77 |
| Forêt de Gazost (45) | Gazost › Tarbes-Lourdes-Pyrénées | 77 |
| Forêt de Bourg-de-Bigorre (62) | Bourg-de-Bigorre › Plateau de Lannemezan | 76 |
| Forêt de Hèches (23) | Hèches › Plateau de Lannemezan | 76 |
| Forêt de Fréchet-Aure (2) | Fréchet-Aure › Aure Louron | 75 |
| Forêt de Gavarnie-Gèdre (330) | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 75 |
| Forêt de Ozon (54) | Ozon › Coteaux du Val-d'Arros | 75 |
| Forêt de Capvern (203) | Capvern › Plateau de Lannemezan | 75 |
| Forêt de Sadournin (7) | Sadournin › Pays de Trie et du Magnoac | 75 |
| Forêt de Arras-en-Lavedan (84) | Arras-en-Lavedan › Pyrénées Vallées des Gaves | 73 |
| Forêt de Campan (308) | Campan › Haute-Bigorre | 73 |
| Forêt de Orignac (47) | Orignac › Haute-Bigorre | 73 |
| Forêt de Salles | Salles › Pyrénées Vallées des Gaves | 72 |
| Forêt de Dours (4) | Dours › Coteaux du Val-d'Arros | 72 |
| Forêt de Saint-Lézer (29) | Saint-Lézer › Adour-Madiran (Hautes-Pyrénées) | 72 |
| Forêt de Montastruc (18) | Montastruc › Plateau de Lannemezan | 72 |
| Forêt de Houeydets (9) | Houeydets › Plateau de Lannemezan | 72 |
| Forêt de Oroix (6) | Oroix › Adour-Madiran (Hautes-Pyrénées) | 71 |
| Forêt de Germs-sur-l'Oussouet (11) | Germs-sur-l'Oussouet › Tarbes-Lourdes-Pyrénées | 71 |
| Forêt de Avezac-Prat-Lahitte (108) | Avezac-Prat-Lahitte › Plateau de Lannemezan | 71 |
| Forêt de Louit (7) | Louit › Coteaux du Val-d'Arros | 71 |
| Forêt de Bernadets-Debat (7) | Bernadets-Debat › Pays de Trie et du Magnoac | 71 |
| Forêt de Loudenvielle (81) | Loudenvielle › Aure Louron | 71 |
| Forêt de Ayzac-Ost (2) | Ayzac-Ost › Pyrénées Vallées des Gaves | 71 |
| Forêt de Bénac (30) | Bénac › Tarbes-Lourdes-Pyrénées | 71 |
| Forêt de Estaing (133) | Estaing › Pyrénées Vallées des Gaves | 70 |
| Forêt de Vidouze (12) | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 69 |
| Forêt de Gavarnie-Gèdre (329) | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 69 |
| Forêt de Ozon (53) | Ozon › Coteaux du Val-d'Arros | 69 |
| Forêt de Ferrières (38) | Ferrières › Pays de Nay (Hautes-Pyrénées) | 68 |
| Forêt de Bagnères-de-Bigorre (232) | Bagnères-de-Bigorre › Haute-Bigorre | 68 |
| Forêt de Tostat (15) | Tostat › Adour-Madiran (Hautes-Pyrénées) | 68 |
| Forêt de Puydarrieux (13) | Puydarrieux › Pays de Trie et du Magnoac | 68 |
| Forêt de Bonrepos (24) | Bonrepos › Plateau de Lannemezan | 68 |
| Forêt de Bareilles (32) | Bareilles › Aure Louron | 68 |
| Forêt de Ossun | Ossun › Tarbes-Lourdes-Pyrénées | 67 |
| Forêt de Gavarnie-Gèdre (325) | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 67 |
| Forêt de Bagnères-de-Bigorre (240) | Bagnères-de-Bigorre › Haute-Bigorre | 67 |
| Bois de Agos-Vidalos (62) | Agos-Vidalos › Pyrénées Vallées des Gaves | 66 |
| Forêt de Arrayou-Lahitte (40) | Arrayou-Lahitte › Tarbes-Lourdes-Pyrénées | 66 |
| Forêt de Fréchet-Aure | Fréchet-Aure › Aure Louron | 65 |
| Forêt de Trébons (46) | Trébons › Haute-Bigorre | 65 |
| Forêt de Recurt (21) | Recurt › Plateau de Lannemezan | 65 |
| Forêt de Arrodets-ez-Angles (18) | Arrodets-ez-Angles › Tarbes-Lourdes-Pyrénées | 64 |
| Forêt de Asque (43) | Asque › Plateau de Lannemezan | 64 |
| Forêt de Organ (3) | Organ › Pays de Trie et du Magnoac | 64 |
| Forêt de Cizos (12) | Cizos › Pays de Trie et du Magnoac | 64 |
| Forêt de Beaucens (57) | Beaucens › Pyrénées Vallées des Gaves | 63 |
| Forêt de Castelbajac (11) | Castelbajac › Plateau de Lannemezan | 63 |
| Forêt de Capvern (216) | Capvern › Plateau de Lannemezan | 63 |
| Forêt de Ancizan (39) | Ancizan › Aure Louron | 63 |
| Forêt de Monléon-Magnoac (18) | Monléon-Magnoac › Pays de Trie et du Magnoac | 62 |
| Forêt de Estaing (131) | Estaing › Pyrénées Vallées des Gaves | 62 |
| Forêt de Ossun (24) | Ossun › Tarbes-Lourdes-Pyrénées | 60 |
| Forêt de Arrens-Marsous (252) | Arrens-Marsous › Pyrénées Vallées des Gaves | 60 |
| Forêt de Barry (11) | Barry › Tarbes-Lourdes-Pyrénées | 60 |
| Forêt de Vielle-Adour (30) | Vielle-Adour › Tarbes-Lourdes-Pyrénées | 60 |
| Forêt de Sarlabous (16) | Sarlabous › Plateau de Lannemezan | 60 |
| Forêt de Azet (46) | Azet › Aure Louron | 59 |
| Bois de Bordes (47) | Vier-Bordes › Pyrénées Vallées des Gaves | 59 |
| Forêt de Visker (22) | Visker › Tarbes-Lourdes-Pyrénées | 59 |
| Forêt de Bouilh-Péreuilh (14) | Bouilh-Péreuilh › Coteaux du Val-d'Arros | 58 |
| Forêt de Sariac-Magnoac (6) | Sariac-Magnoac › Pays de Trie et du Magnoac | 58 |
| Forêt de Thèbe | Thèbe › Neste Barousse | 58 |
| Forêt de Saint-Lary-Soulan (210) | Saint-Lary-Soulan › Aure Louron | 58 |
| Forêt de Campan (298) | Campan › Haute-Bigorre | 57 |
| Forêt de Bénac (27) | Bénac › Tarbes-Lourdes-Pyrénées | 57 |
| Forêt de Asque (44) | Asque › Plateau de Lannemezan | 57 |
| Forêt de Tilhouse (34) | Tilhouse › Plateau de Lannemezan | 57 |
| Forêt de Sariac-Magnoac (4) | Sariac-Magnoac › Pays de Trie et du Magnoac | 57 |
| Forêt de Gazost (50) | Gazost › Tarbes-Lourdes-Pyrénées | 57 |
| Forêt de Asté (2) | Asté › Haute-Bigorre | 56 |
| Forêt de Caixon (3) | Caixon › Adour-Madiran (Hautes-Pyrénées) | 56 |
| Forêt de Gez-ez-Angles (26) | Gez-ez-Angles › Tarbes-Lourdes-Pyrénées | 56 |
| Forêt de Saint-Sever-de-Rustan (9) | Saint-Sever-de-Rustan › Adour-Madiran (Hautes-Pyrénées) | 56 |
| Forêt de Vieuzos (2) | Vieuzos › Pays de Trie et du Magnoac | 56 |
| Forêt de Izaux (12) | Izaux › Plateau de Lannemezan | 56 |
| Forêt de Castelnau-Rivière-Basse (26) | Castelnau-Rivière-Basse › Adour-Madiran (Hautes-Pyrénées) | 56 |
| Forêt de Bonnefont (16) | Bonnefont › Pays de Trie et du Magnoac | 56 |
| Forêt de Cauterets (658) | Cauterets › Pyrénées Vallées des Gaves | 55 |
| Forêt de Salles (25) | Salles › Pyrénées Vallées des Gaves | 55 |
| Forêt de Vic-en-Bigorre (66) | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 54 |
| Forêt de Benqué-Molère (15) | Benqué-Molère › Plateau de Lannemezan | 54 |
| Forêt de Nistos | Nistos › Neste Barousse | 53 |
| Forêt de Burg (26) | Burg › Coteaux du Val-d'Arros | 53 |
| Forêt de Monléon-Magnoac (15) | Monléon-Magnoac › Pays de Trie et du Magnoac | 53 |
| Forêt de Sailhan (4) | Sailhan › Aure Louron | 53 |
| Forêt de Vic-en-Bigorre (67) | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 53 |
| Forêt de Ferrère (2) | Ferrère › Neste Barousse | 52 |
| Forêt de Campan (301) | Campan › Haute-Bigorre | 52 |
| Forêt de Bénac (26) | Bénac › Tarbes-Lourdes-Pyrénées | 52 |
| Forêt de Fréchendets (7) | Fréchendets › Plateau de Lannemezan | 52 |
| Forêt de Bugard (10) | Bugard › Pays de Trie et du Magnoac | 52 |
| Forêt de Bazordan (18) | Bazordan › Pays de Trie et du Magnoac | 52 |
| Forêt de Nistos (20) | Nistos › Neste Barousse | 52 |
| Forêt de Ens (6) | Ens › Aure Louron | 52 |
| Forêt de Lançon (3) | Lançon › Aure Louron | 51 |
| Forêt de Barbazan-Debat (19) | Barbazan-Debat › Tarbes-Lourdes-Pyrénées | 51 |
| Forêt de Barrancoueu (7) | Barrancoueu › Aure Louron | 51 |
| Bois de Beaucens (99) | Beaucens › Pyrénées Vallées des Gaves | 51 |
| Forêt de Bernadets-Dessus | Bernadets-Dessus › Coteaux du Val-d'Arros | 50 |
| Forêt de Montastruc (21) | Montastruc › Plateau de Lannemezan | 50 |
| Forêt de Sabarros (8) | Sabarros › Plateau de Lannemezan | 50 |
| Forêt de Juncalas (9) | Juncalas › Tarbes-Lourdes-Pyrénées | 49 |
| Forêt de Capvern (214) | Capvern › Plateau de Lannemezan | 49 |
| Forêt de Aubarède (7) | Aubarède › Coteaux du Val-d'Arros | 49 |
| Forêt de Ancizan (40) | Ancizan › Aure Louron | 49 |
| Forêt de Vic-en-Bigorre (68) | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 49 |
| Forêt de Cauterets (4) | Cauterets › Pyrénées Vallées des Gaves | 48 |
| Forêt de Estaing (127) | Estaing › Pyrénées Vallées des Gaves | 48 |
| Forêt de Gavarnie-Gèdre (326) | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 48 |
| Forêt de Nistos (18) | Nistos › Neste Barousse | 48 |
| Forêt de Bouilh-Péreuilh (17) | Bouilh-Péreuilh › Coteaux du Val-d'Arros | 48 |
| Forêt de Lassales (3) | Lassales › Pays de Trie et du Magnoac | 48 |
| Forêt de Castelnau-Rivière-Basse (23) | Castelnau-Rivière-Basse › Adour-Madiran (Hautes-Pyrénées) | 48 |
| Forêt de Bagnères-de-Bigorre (239) | Bagnères-de-Bigorre › Haute-Bigorre | 48 |
| Sapinière de Thou | Saint-Lary-Soulan › Aure Louron | 48 |
| Forêt de Azereix | Azereix › Tarbes-Lourdes-Pyrénées | 47 |
| Forêt de Chèze | Chèze › Pyrénées Vallées des Gaves | 47 |
| Forêt de Trouley-Labarthe | Trouley-Labarthe › Adour-Madiran (Hautes-Pyrénées) | 47 |
| Forêt de Ibos (104) | Ibos › Tarbes-Lourdes-Pyrénées | 47 |
| Forêt de Berbérust-Lias (23) | Berbérust-Lias › Tarbes-Lourdes-Pyrénées | 47 |
| Forêt de Bagnères-de-Bigorre (235) | Bagnères-de-Bigorre › Haute-Bigorre | 47 |
| Forêt de Aries-Espénan (2) | Aries-Espénan › Pays de Trie et du Magnoac | 47 |
| Bois de Ancizan (18) | Ancizan › Aure Louron | 47 |
| Forêt de Barèges (217) | Barèges › Pyrénées Vallées des Gaves | 47 |
| Forêt de Asque (48) | Asque › Plateau de Lannemezan | 47 |
| Forêt de Gavarnie-Gèdre (338) | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 47 |
| Forêt de Campan (221) | Campan › Haute-Bigorre | 46 |
| Forêt de Beaudéan (36) | Beaudéan › Haute-Bigorre | 46 |
| Forêt de Campan (304) | Campan › Haute-Bigorre | 46 |
| Forêt de Chelle-Spou (36) | Chelle-Spou › Plateau de Lannemezan | 46 |
| Forêt de Réjaumont (23) | Réjaumont › Plateau de Lannemezan | 46 |
| Forêt de Libaros | Libaros › Plateau de Lannemezan | 45 |
| Forêt de Vidouze (13) | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 45 |
| Forêt de Cauterets (673) | Cauterets › Pyrénées Vallées des Gaves | 45 |
| Forêt de Bulan (34) | Bulan › Plateau de Lannemezan | 45 |
| Forêt de Betpouy (3) | Betpouy › Pays de Trie et du Magnoac | 45 |
| Forêt de Arreau (6) | Arreau › Aure Louron | 45 |
| Forêt de Ancizan (41) | Ancizan › Aure Louron | 45 |
| Bois de Aulon (25) | Aulon › Aure Louron | 45 |
| Forêt de Azet (59) | Azet › Aure Louron | 45 |
| Forêt de Ger (2) | Saint-Créac › Tarbes-Lourdes-Pyrénées | 44 |
| Forêt de Beyrède-Jumet-Camous (17) | Beyrède-Jumet-Camous › Aure Louron | 44 |
| Forêt de Bonnefont (13) | Bonnefont › Pays de Trie et du Magnoac | 44 |
| Forêt de Castelbajac (10) | Castelbajac › Plateau de Lannemezan | 44 |
| Forêt de Vignec (46) | Vignec › Aure Louron | 44 |
| Forêt de Buzon (5) | Monfaucon › Adour-Madiran (Hautes-Pyrénées) | 44 |
| Forêt de Ossun-ez-Angles (14) | Ossun-ez-Angles › Tarbes-Lourdes-Pyrénées | 44 |
| Forêt de Gaillagos | Gaillagos › Pyrénées Vallées des Gaves | 43 |
| Forêt de Aurensan (30) | Aurensan › Tarbes-Lourdes-Pyrénées | 43 |
| Forêt de Estaing (126) | Estaing › Pyrénées Vallées des Gaves | 43 |
| Forêt de Lannemezan (67) | Lannemezan › Plateau de Lannemezan | 43 |
| Forêt de Bourg-de-Bigorre | Bourg-de-Bigorre › Plateau de Lannemezan | 42 |
| Forêt de Estaing (2) | Estaing › Pyrénées Vallées des Gaves | 42 |
| Forêt de Bagnères-de-Bigorre (149) | Bagnères-de-Bigorre › Haute-Bigorre | 42 |
| Forêt de Bonnemazon (2) | Bonnemazon › Plateau de Lannemezan | 42 |
| Forêt de Arrens-Marsous (238) | Arrens-Marsous › Pyrénées Vallées des Gaves | 42 |
| Forêt de Lézignan (5) | Lézignan › Tarbes-Lourdes-Pyrénées | 42 |
| Forêt de Lagrange (4) | Lagrange › Plateau de Lannemezan | 42 |
| Forêt de Luby-Betmont (12) | Luby-Betmont › Pays de Trie et du Magnoac | 42 |
| Forêt de Pouyastruc (27) | Pouyastruc › Coteaux du Val-d'Arros | 42 |
| Forêt de Boô-Silhen | Boô-Silhen › Pyrénées Vallées des Gaves | 41 |
| Forêt de Cauterets (684) | Cauterets › Pyrénées Vallées des Gaves | 41 |
| Forêt de Barbazan-Dessus (26) | Barbazan-Dessus › Tarbes-Lourdes-Pyrénées | 41 |
| Forêt de Lomné (25) | Lomné › Plateau de Lannemezan | 41 |
| Forêt de Rabastens-de-Bigorre (13) | Rabastens-de-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 41 |
| Forêt de Bonnefont (12) | Bonnefont › Pays de Trie et du Magnoac | 41 |
| Forêt de Anères (2) | Anères › Neste Barousse | 41 |
| Forêt de Lombrès (3) | Lombrès › Neste Barousse | 41 |
| Forêt de Sost (35) | Sost › Neste Barousse | 41 |
| Forêt de Cazaux-Fréchet-Anéran-Camors (24) | Cazaux-Fréchet-Anéran-Camors › Aure Louron | 41 |
| Forêt de Castelnau-Rivière-Basse (27) | Castelnau-Rivière-Basse › Adour-Madiran (Hautes-Pyrénées) | 41 |
| Forêt de Pouyastruc (11) | Pouyastruc › Coteaux du Val-d'Arros | 40 |
| Forêt de Arrens-Marsous (235) | Estaing › Pyrénées Vallées des Gaves | 40 |
| Forêt de Adé (34) | Adé › Tarbes-Lourdes-Pyrénées | 40 |
| Forêt de Grézian (2) | Grézian › Aure Louron | 40 |
| Forêt de Vielle-Aure (193) | Vielle-Aure › Aure Louron | 40 |
| Forêt de Arrens-Marsous (243) | Arrens-Marsous › Pyrénées Vallées des Gaves | 39 |
| Forêt de Orincles (22) | Orincles › Tarbes-Lourdes-Pyrénées | 39 |
| Forêt de Labastide (46) | Labastide › Plateau de Lannemezan | 39 |
| Forêt de Arreau (5) | Arreau › Aure Louron | 39 |
| Forêt de Gazost (48) | Gazost › Tarbes-Lourdes-Pyrénées | 39 |
| Forêt de Saint-Pé-de-Bigorre (27) | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 38 |
| Forêt de Arné (10) | Arné › Plateau de Lannemezan | 38 |
| Forêt de Sost (7) | Sost › Neste Barousse | 38 |
| Forêt de Génos (27) | Génos › Aure Louron | 38 |
| Forêt de Trébons (48) | Trébons › Haute-Bigorre | 38 |
| Forêt de Avajan (3) | Cazaux-Fréchet-Anéran-Camors › Aure Louron | 38 |
| Forêt de Arcizans-Avant (36) | Arcizans-Avant › Pyrénées Vallées des Gaves | 37 |
| Forêt de Sers (85) | Sers › Pyrénées Vallées des Gaves | 37 |
| Forêt de Uz (9) | Uz › Pyrénées Vallées des Gaves | 37 |
| Forêt de Trébons (45) | Trébons › Haute-Bigorre | 37 |
| Forêt de Montgaillard (60) | Montgaillard › Haute-Bigorre | 37 |
| Forêt de Moumoulous (3) | Moumoulous › Adour-Madiran (Hautes-Pyrénées) | 37 |
| Forêt de Arné (17) | Arné › Plateau de Lannemezan | 37 |
| Forêt de Loudenvielle (77) | Loudenvielle › Aure Louron | 37 |
| Forêt de Esparros (2) | Esparros › Plateau de Lannemezan | 36 |
| Forêt de Asté (6) | Asté › Haute-Bigorre | 36 |
| Forêt de Lamarque-Pontacq (51) | Lamarque-Pontacq › Tarbes-Lourdes-Pyrénées | 36 |
| Forêt de Betbèze (4) | Thermes-Magnoac › Pays de Trie et du Magnoac | 36 |
| Forêt de Génos (53) | Génos › Aure Louron | 36 |
| Forêt de Bonnemazon (3) | Bonnemazon › Plateau de Lannemezan | 35 |
| Forêt de Arcizans-Avant (35) | Arcizans-Avant › Pyrénées Vallées des Gaves | 35 |
| Forêt de Jarret (10) | Jarret › Tarbes-Lourdes-Pyrénées | 35 |
| Forêt de Bagnères-de-Bigorre (230) | Bagnères-de-Bigorre › Haute-Bigorre | 35 |
| Forêt de Campan (311) | Campan › Haute-Bigorre | 35 |
| Forêt de Astugue (69) | Astugue › Haute-Bigorre | 35 |
| Forêt de Mauvezin (71) | Mauvezin › Plateau de Lannemezan | 35 |
| Forêt de Castillon (20) | Castillon › Plateau de Lannemezan | 35 |
| Forêt de Monléon-Magnoac (17) | Monléon-Magnoac › Pays de Trie et du Magnoac | 35 |
| Forêt de Pinas (9) | Pinas › Plateau de Lannemezan | 35 |
| Forêt de Azet (56) | Azet › Aure Louron | 35 |
| Forêt de Larreule (4) | Larreule › Adour-Madiran (Hautes-Pyrénées) | 35 |
| Forêt de Castelnau-Rivière-Basse (28) | Castelnau-Rivière-Basse › Adour-Madiran (Hautes-Pyrénées) | 35 |
| Forêt de Oroix (2) | Oroix › Adour-Madiran (Hautes-Pyrénées) | 34 |
| Forêt de Bareilles | Bareilles › Aure Louron | 34 |
| Forêt de Estaing (130) | Estaing › Pyrénées Vallées des Gaves | 34 |
| Forêt de Aucun (75) | Aucun › Pyrénées Vallées des Gaves | 34 |
| Forêt de Cauterets (677) | Cauterets › Pyrénées Vallées des Gaves | 34 |
| Forêt de Cauterets (678) | Cauterets › Pyrénées Vallées des Gaves | 34 |
| Forêt de Galan (12) | Galan › Plateau de Lannemezan | 34 |
| Forêt de Thermes-Magnoac (15) | Thermes-Magnoac › Pays de Trie et du Magnoac | 34 |
| Forêt de Sariac-Magnoac (7) | Sariac-Magnoac › Pays de Trie et du Magnoac | 34 |
| Forêt de Bizous (12) | Bizous › Neste Barousse | 34 |
| Forêt de Monléon-Magnoac (2) | Monléon-Magnoac › Pays de Trie et du Magnoac | 33 |
| Forêt de Gavarnie-Gèdre (320) | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 33 |
| Forêt de Vier-Bordes (32) | Vier-Bordes › Pyrénées Vallées des Gaves | 33 |
| Forêt de Caixon (4) | Caixon › Adour-Madiran (Hautes-Pyrénées) | 33 |
| Forêt de Monléon-Magnoac | Monléon-Magnoac › Pays de Trie et du Magnoac | 32 |
| Forêt de Germ | Germ › Aure Louron | 32 |
| Forêt de Gavarnie-Gèdre (272) | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 32 |
| Forêt de Avezac-Prat-Lahitte (8) | Avezac-Prat-Lahitte › Plateau de Lannemezan | 32 |
| Forêt de Marseillan (4) | Castelvieilh › Coteaux du Val-d'Arros | 32 |
| Forêt de Cheust (9) | Cheust › Tarbes-Lourdes-Pyrénées | 32 |
| Forêt de Germs-sur-l'Oussouet (12) | Germs-sur-l'Oussouet › Tarbes-Lourdes-Pyrénées | 32 |
| Forêt de Cauterets (676) | Cauterets › Pyrénées Vallées des Gaves | 32 |
| Forêt de Séméac (34) | Séméac › Tarbes-Lourdes-Pyrénées | 32 |
| Forêt de Bouilh-Devant (15) | Bouilh-Devant › Adour-Madiran (Hautes-Pyrénées) | 32 |
| Forêt de Salles (28) | Salles › Pyrénées Vallées des Gaves | 32 |
| Forêt de Chelle-Debat (3) | Chelle-Debat › Coteaux du Val-d'Arros | 32 |
| Forêt de Galez (9) | Galez › Plateau de Lannemezan | 32 |
| Forêt de Nestier (8) | Nestier › Neste Barousse | 32 |
| Forêt de Tuzaguet (11) | Tuzaguet › Neste Barousse | 32 |
| Forêt de Gazost (49) | Gazost › Tarbes-Lourdes-Pyrénées | 32 |
| Forêt de Asté | Asté › Haute-Bigorre | 31 |
| Forêt de Esparros (56) | Esparros › Plateau de Lannemezan | 31 |
| Forêt de Viscos (9) | Viscos › Pyrénées Vallées des Gaves | 31 |
| Forêt de Gavarnie-Gèdre (334) | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 31 |
| Forêt de Cauterets (681) | Cauterets › Pyrénées Vallées des Gaves | 31 |
| Forêt de Sazos (52) | Sazos › Pyrénées Vallées des Gaves | 31 |
| Forêt de Bagnères-de-Bigorre (231) | Bagnères-de-Bigorre › Haute-Bigorre | 31 |
| Forêt de Astugue (64) | Astugue › Haute-Bigorre | 31 |
| Forêt de Lamarque-Pontacq (50) | Lamarque-Pontacq › Tarbes-Lourdes-Pyrénées | 31 |
| Forêt de Montignac (7) | Montignac › Tarbes-Lourdes-Pyrénées | 31 |
| Forêt de Castillon (19) | Castillon › Plateau de Lannemezan | 31 |
| Forêt de Avezac-Prat-Lahitte (110) | Avezac-Prat-Lahitte › Plateau de Lannemezan | 31 |
| Forêt de Capvern (202) | Capvern › Plateau de Lannemezan | 31 |
| Forêt de Bordes (70) | Bordes › Coteaux du Val-d'Arros | 31 |
| Forêt de Bagnères-de-Bigorre (241) | Bagnères-de-Bigorre › Haute-Bigorre | 31 |
| Forêt de Villelongue (12) | Villelongue › Pyrénées Vallées des Gaves | 30 |
| Forêt de Barèges (33) | Barèges › Pyrénées Vallées des Gaves | 30 |
| Forêt de Aragnouet (66) | Aragnouet › Aure Louron | 30 |
| Forêt de Caixon (2) | Caixon › Adour-Madiran (Hautes-Pyrénées) | 30 |
| Forêt de Séron (8) | Séron › Tarbes-Lourdes-Pyrénées | 30 |
| Forêt de Aucun (72) | Aucun › Pyrénées Vallées des Gaves | 30 |
| Forêt de Beaucens (55) | Beaucens › Pyrénées Vallées des Gaves | 30 |
| Forêt de Villelongue (44) | Villelongue › Pyrénées Vallées des Gaves | 30 |
| Forêt de Arcizans-Avant (39) | Arcizans-Avant › Pyrénées Vallées des Gaves | 30 |
| Forêt de Aucun (74) | Aucun › Pyrénées Vallées des Gaves | 30 |
| Forêt de Gavarnie-Gèdre (336) | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 30 |
| Forêt de Orincles (21) | Orincles › Tarbes-Lourdes-Pyrénées | 30 |
| Forêt de Bordes (69) | Bordes › Coteaux du Val-d'Arros | 30 |
| Forêt de Angos (12) | Angos › Coteaux du Val-d'Arros | 30 |
| Bois de Saint-Pastous (50) | Saint-Pastous › Pyrénées Vallées des Gaves | 30 |
| Forêt de Ferrère | Ferrère › Neste Barousse | 29 |
| Forêt de Tarasteix (2) | Tarasteix › Adour-Madiran (Hautes-Pyrénées) | 29 |
| Forêt de Ibos (106) | Ibos › Tarbes-Lourdes-Pyrénées | 29 |
| Forêt de Sénac (29) | Sénac › Adour-Madiran (Hautes-Pyrénées) | 29 |
| Forêt de Saint-Paul (26) | Saint-Paul › Neste Barousse | 29 |
| Forêt de Bareilles (30) | Bareilles › Aure Louron | 29 |
| Forêt de Sauveterre | Sauveterre › Adour-Madiran (Hautes-Pyrénées) | 28 |
| Forêt de Estaing | Estaing › Pyrénées Vallées des Gaves | 28 |
| Forêt de Ancizan (3) | Ancizan › Aure Louron | 28 |
| Forêt de Saint-Lézer (27) | Saint-Lézer › Adour-Madiran (Hautes-Pyrénées) | 28 |
| Forêt de Bagnères-de-Bigorre (226) | Bagnères-de-Bigorre › Haute-Bigorre | 28 |
| Forêt de Viella (20) | Viella › Pyrénées Vallées des Gaves | 28 |
| Forêt de Labassère (62) | Labassère › Haute-Bigorre | 28 |
| Forêt de Poumarous (21) | Poumarous › Coteaux du Val-d'Arros | 28 |
| Forêt de Bettes (28) | Bettes › Haute-Bigorre | 28 |
| Forêt de Cabanac (9) | Cabanac › Coteaux du Val-d'Arros | 28 |
| Forêt de Saint-Sever-de-Rustan (11) | Saint-Sever-de-Rustan › Adour-Madiran (Hautes-Pyrénées) | 28 |
| Forêt de Recurt (25) | Recurt › Plateau de Lannemezan | 28 |
| Forêt de Cantaous (16) | Cantaous › Neste Barousse | 28 |
| Forêt de Loudenvielle (75) | Loudenvielle › Aure Louron | 28 |
| Forêt de Saint-Lary-Soulan (215) | Saint-Lary-Soulan › Aure Louron | 28 |
| Forêt de Cauterets (688) | Cauterets › Pyrénées Vallées des Gaves | 28 |
| Forêt de Aragnouet (214) | Aragnouet › Aure Louron | 28 |
| Forêt de Cauterets (263) | Cauterets › Pyrénées Vallées des Gaves | 27 |
| Forêt de Astugue (67) | Astugue › Haute-Bigorre | 27 |
| Forêt de Saint-Pé-de-Bigorre (72) | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 27 |
| Forêt de Sazos (53) | Sazos › Pyrénées Vallées des Gaves | 27 |
| Forêt de Asque (45) | Asque › Plateau de Lannemezan | 27 |
| Forêt de Montastruc (20) | Montastruc › Plateau de Lannemezan | 27 |
| Forêt de Vieuzos | Vieuzos › Pays de Trie et du Magnoac | 27 |
| Forêt de Uglas (15) | Uglas › Plateau de Lannemezan | 27 |
| Forêt de Vignec (45) | Vignec › Aure Louron | 27 |
| Forêt de Vidouze (16) | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 27 |
| Forêt de Saint-Lanne (14) | Saint-Lanne › Adour-Madiran (Hautes-Pyrénées) | 27 |
| Forêt de Barry | Orincles › Tarbes-Lourdes-Pyrénées | 26 |
| Forêt de Villelongue | Villelongue › Pyrénées Vallées des Gaves | 26 |
| Forêt de Tuzaguet | Tuzaguet › Neste Barousse | 26 |
| Forêt de Arras-en-Lavedan (76) | Arras-en-Lavedan › Pyrénées Vallées des Gaves | 26 |
| Forêt de Artalens-Souin (44) | Artalens-Souin › Pyrénées Vallées des Gaves | 26 |
| Bois de Gavarnie-Gèdre (73) | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 26 |
| Forêt de Gavarnie-Gèdre (331) | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 26 |
| Forêt de Cauterets (671) | Cauterets › Pyrénées Vallées des Gaves | 26 |
| Forêt de Beyrède-Jumet-Camous (16) | Beyrède-Jumet-Camous › Aure Louron | 26 |
| Forêt de Astugue (65) | Astugue › Haute-Bigorre | 26 |
| Forêt de Villemur (5) | Villemur › Pays de Trie et du Magnoac | 26 |
| Forêt de Aragnouet (213) | Aragnouet › Aure Louron | 26 |
| Bois de Cauterets (43) | Cauterets › Pyrénées Vallées des Gaves | 26 |
| Forêt de Saint-Lézer | Saint-Lézer › Adour-Madiran (Hautes-Pyrénées) | 25 |
| Forêt de Aspin-Aure | Aspin-Aure › Aure Louron | 25 |
| Forêt de Houeydets | Houeydets › Plateau de Lannemezan | 25 |
| Bois de Guchen (13) | Guchen › Aure Louron | 25 |
| Forêt de Ferrère (81) | Ferrère › Neste Barousse | 25 |
| Forêt de Poueyferré (68) | Poueyferré › Tarbes-Lourdes-Pyrénées | 25 |
| Forêt de Hibarette (10) | Hibarette › Tarbes-Lourdes-Pyrénées | 25 |
| Forêt de Marquerie (3) | Marquerie › Coteaux du Val-d'Arros | 25 |
| Forêt de Saint-Laurent-de-Neste (21) | Saint-Laurent-de-Neste › Neste Barousse | 25 |
| Forêt de Adervielle-Pouchergues (23) | Adervielle-Pouchergues › Aure Louron | 25 |
| Forêt de Vielle-Aure (195) | Vielle-Aure › Aure Louron | 25 |
| Forêt de Saint-Lary-Soulan (208) | Saint-Lary-Soulan › Aure Louron | 25 |
| Forêt de Hagedet (3) | Hagedet › Adour-Madiran (Hautes-Pyrénées) | 25 |
| Forêt de Bagnères-de-Bigorre (242) | Bagnères-de-Bigorre › Haute-Bigorre | 25 |
| Forêt de Salles (30) | Salles › Pyrénées Vallées des Gaves | 25 |
| Forêt de Ordizan (61) | Ordizan › Haute-Bigorre | 25 |
| Bois de Cauterets | Cauterets › Pyrénées Vallées des Gaves | 24 |
| Forêt de Uzer (12) | Uzer › Haute-Bigorre | 24 |
| Forêt de Clarens (12) | Clarens › Plateau de Lannemezan | 24 |
| Forêt de Escaunets (10) | Escaunets › Adour-Madiran (Hautes-Pyrénées) | 24 |
| Forêt de Siarrouy (24) | Siarrouy › Adour-Madiran (Hautes-Pyrénées) | 24 |
| Forêt de Arras-en-Lavedan (81) | Arras-en-Lavedan › Pyrénées Vallées des Gaves | 24 |
| Forêt de Labassère (60) | Labassère › Haute-Bigorre | 24 |
| Forêt de Viey (25) | Viey › Pyrénées Vallées des Gaves | 24 |
| Forêt de Campan (303) | Campan › Haute-Bigorre | 24 |
| Forêt de Ferrières (40) | Ferrières › Pays de Nay (Hautes-Pyrénées) | 24 |
| Forêt de Bazillac (57) | Bazillac › Adour-Madiran (Hautes-Pyrénées) | 24 |
| Forêt de Péré (27) | Péré › Plateau de Lannemezan | 24 |
| Forêt de Bégole (16) | Bégole › Coteaux du Val-d'Arros | 24 |
| Forêt de Campan (317) | Campan › Haute-Bigorre | 24 |
| Forêt de Marquerie (4) | Marquerie › Coteaux du Val-d'Arros | 24 |
| Forêt de Vidou (6) | Vidou › Pays de Trie et du Magnoac | 24 |
| Forêt de Peyret-Saint-André (6) | Peyret-Saint-André › Pays de Trie et du Magnoac | 24 |
| Forêt de Saint-Laurent-de-Neste (19) | Saint-Laurent-de-Neste › Neste Barousse | 24 |
| Forêt de Esbareich | Esbareich › Neste Barousse | 24 |
| Forêt de Oroix (8) | Oroix › Adour-Madiran (Hautes-Pyrénées) | 24 |
| Forêt de Castelvieilh | Cabanac › Coteaux du Val-d'Arros | 23 |
| Forêt de Viella (11) | Viella › Pyrénées Vallées des Gaves | 23 |
| Forêt de Gavarnie-Gèdre (222) | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 23 |
| Forêt de Thermes-Magnoac (7) | Thermes-Magnoac › Pays de Trie et du Magnoac | 23 |
| Forêt de Luquet (19) | Luquet › Tarbes-Lourdes-Pyrénées | 23 |
| Forêt de Arrens-Marsous (242) | Arrens-Marsous › Pyrénées Vallées des Gaves | 23 |
| Forêt de Arbéost (61) | Arbéost › Pays de Nay (Hautes-Pyrénées) | 23 |
| Forêt Communale d'Aureilhan | Aureilhan › Tarbes-Lourdes-Pyrénées | 23 |
| Forêt de Lomné (26) | Lomné › Plateau de Lannemezan | 23 |
| Forêt de Lanespède (22) | Lanespède › Coteaux du Val-d'Arros | 23 |
| Forêt de Anla (5) | Anla › Neste Barousse | 23 |
| Forêt de Bareilles (31) | Bareilles › Aure Louron | 23 |
| Forêt de Vic-en-Bigorre (69) | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 23 |
| Forêt de Gazost (46) | Gazost › Tarbes-Lourdes-Pyrénées | 23 |
| Forêt de Arrens-Marsous (266) | Arrens-Marsous › Pyrénées Vallées des Gaves | 23 |
| Forêt de Grust (28) | Grust › Pyrénées Vallées des Gaves | 23 |
| Forêt de Lourdes (155) | Lourdes › Tarbes-Lourdes-Pyrénées | 23 |
| Forêt de Beaucens | Beaucens › Pyrénées Vallées des Gaves | 22 |
| Forêt de Bagnères-de-Bigorre | Bagnères-de-Bigorre › Haute-Bigorre | 22 |
| Forêt de Montgaillard (8) | Montgaillard › Haute-Bigorre | 22 |
| Forêt de Artiguemy (13) | Artiguemy › Plateau de Lannemezan | 22 |
| Forêt de Capvern (132) | Capvern › Plateau de Lannemezan | 22 |
| Forêt de Castelvieilh (8) | Castelvieilh › Coteaux du Val-d'Arros | 22 |
| Forêt de Lutilhous (2) | Lutilhous › Plateau de Lannemezan | 22 |
| Forêt de Bagnères-de-Bigorre (227) | Bagnères-de-Bigorre › Haute-Bigorre | 22 |
| Forêt de Trébons (44) | Trébons › Haute-Bigorre | 22 |
| Forêt de Mingot (3) | Mingot › Adour-Madiran (Hautes-Pyrénées) | 22 |
| Forêt de Bonnefont (15) | Bonnefont › Pays de Trie et du Magnoac | 22 |
| Forêt de Sabarros (9) | Sabarros › Plateau de Lannemezan | 22 |
| Sapinière de Balestas | Loudervielle › Aure Louron | 22 |
| Forêt de Aulon (5) | Aulon › Aure Louron | 22 |
| Forêt de Lafitole (11) | Lafitole › Adour-Madiran (Hautes-Pyrénées) | 22 |
| Forêt de Chèze (17) | Chèze › Pyrénées Vallées des Gaves | 22 |
| Forêt de Barèges (218) | Barèges › Pyrénées Vallées des Gaves | 22 |
| Forêt de Cabanac | Cabanac › Coteaux du Val-d'Arros | 21 |
| Forêt de Lamarque-Pontacq (14) | Lamarque-Pontacq › Tarbes-Lourdes-Pyrénées | 21 |
| Forêt de Ferrère (29) | Ferrère › Neste Barousse | 21 |
| Forêt de Omex (5) | Omex › Tarbes-Lourdes-Pyrénées | 21 |
| Forêt de Cauterets (682) | Cauterets › Pyrénées Vallées des Gaves | 21 |
| Forêt de Arrens-Marsous (257) | Arrens-Marsous › Pyrénées Vallées des Gaves | 21 |
| Forêt de Ancizan (37) | Ancizan › Aure Louron | 21 |
| Forêt de Tournay (90) | Tournay › Coteaux du Val-d'Arros | 21 |
| Forêt de Castéra-Lou (6) | Castéra-Lou › Coteaux du Val-d'Arros | 21 |
| Forêt de Castéra-Lou (7) | Castéra-Lou › Coteaux du Val-d'Arros | 21 |
| Forêt de Lalanne-Trie (6) | Lalanne-Trie › Pays de Trie et du Magnoac | 21 |
| Forêt de Tournous-Devant (4) | Tournous-Devant › Plateau de Lannemezan | 21 |
| Forêt de Bazordan (19) | Bazordan › Pays de Trie et du Magnoac | 21 |
| Forêt de Tramezaïgues (105) | Tramezaïgues › Aure Louron | 21 |
| Forêt de Gavarnie-Gèdre | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 20 |
| Forêt de Saint-Lézer (2) | Saint-Lézer › Adour-Madiran (Hautes-Pyrénées) | 20 |
| Forêt de Cauterets | Cauterets › Pyrénées Vallées des Gaves | 20 |
| Forêt de Gavarnie-Gèdre (3) | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 20 |
| Forêt de Sost (2) | Sost › Neste Barousse | 20 |
| Forêt de Antin | Antin › Pays de Trie et du Magnoac | 20 |
| Forêt de Mun | Mun › Coteaux du Val-d'Arros | 20 |
| Forêt de Pouyastruc (5) | Pouyastruc › Coteaux du Val-d'Arros | 20 |
| Forêt de Lannemezan (33) | Lannemezan › Plateau de Lannemezan | 20 |
| Forêt de Lortet (3) | Lortet › Plateau de Lannemezan | 20 |
| Forêt de Burg (23) | Burg › Coteaux du Val-d'Arros | 20 |
| Forêt de Vier-Bordes (31) | Artalens-Souin › Pyrénées Vallées des Gaves | 20 |
| Forêt de Cauterets (683) | Cauterets › Pyrénées Vallées des Gaves | 20 |
| Bois de Monesté | Estaing › Pyrénées Vallées des Gaves | 20 |
| Forêt de Bagnères-de-Bigorre (236) | Bagnères-de-Bigorre › Haute-Bigorre | 20 |
| Forêt de Vielle-Adour (28) | Vielle-Adour › Tarbes-Lourdes-Pyrénées | 20 |
| Forêt de Esparros (81) | Esparros › Plateau de Lannemezan | 20 |
| Forêt de Avezac-Prat-Lahitte (111) | Avezac-Prat-Lahitte › Plateau de Lannemezan | 20 |
| Forêt de Capvern (213) | Capvern › Plateau de Lannemezan | 20 |
| Forêt de Caubous (13) | Caubous › Pays de Trie et du Magnoac | 20 |
| Forêt de Seich (5) | Seich › Neste Barousse | 20 |
| Forêt de Bourisp | Bourisp › Aure Louron | 20 |
| Forêt de Sanous | Sanous › Adour-Madiran (Hautes-Pyrénées) | 20 |
| Forêt de Salles (31) | Salles › Pyrénées Vallées des Gaves | 20 |
| Forêt de Sost | Sost › Neste Barousse | 19 |
| Forêt de Laméac | Laméac › Adour-Madiran (Hautes-Pyrénées) | 19 |
| Forêt de Cauterets (2) | Cauterets › Pyrénées Vallées des Gaves | 19 |
| Forêt de Labassère (33) | Labassère › Haute-Bigorre | 19 |
| Forêt de Boô-Silhen (2) | Boô-Silhen › Pyrénées Vallées des Gaves | 19 |
| Forêt de Arrens-Marsous (250) | Arrens-Marsous › Pyrénées Vallées des Gaves | 19 |
| Forêt de Loubajac (37) | Loubajac › Tarbes-Lourdes-Pyrénées | 19 |
| Forêt de Sazos (54) | Sazos › Pyrénées Vallées des Gaves | 19 |
| Forêt de Ibos (112) | Ibos › Tarbes-Lourdes-Pyrénées | 19 |
| Forêt de Orleix (32) | Orleix › Tarbes-Lourdes-Pyrénées | 19 |
| Forêt de Bernac-Debat (8) | Bernac-Debat › Tarbes-Lourdes-Pyrénées | 19 |
| Forêt de Arcizac-Adour (29) | Arcizac-Adour › Tarbes-Lourdes-Pyrénées | 19 |
| Forêt de Gavarnie-Gèdre (337) | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 19 |
| Forêt de Rabastens-de-Bigorre (14) | Rabastens-de-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 19 |
| Forêt de Galan (14) | Galan › Plateau de Lannemezan | 19 |
| Forêt de Betpouy (4) | Betpouy › Pays de Trie et du Magnoac | 19 |
| Forêt de Camparan | Camparan › Aure Louron | 19 |
| Forêt de Cadeilhan-Trachère (34) | Cadeilhan-Trachère › Aure Louron | 19 |
| Forêt de Sombrun (4) | Sombrun › Adour-Madiran (Hautes-Pyrénées) | 19 |
| Forêt de Madiran (29) | Madiran › Adour-Madiran (Hautes-Pyrénées) | 19 |
| Forêt de Esparros | Esparros › Plateau de Lannemezan | 18 |
| Forêt de Oroix | Oroix › Adour-Madiran (Hautes-Pyrénées) | 18 |
| Forêt de Bagnères-de-Bigorre (3) | Bagnères-de-Bigorre › Haute-Bigorre | 18 |
| Forêt de Gavarnie-Gèdre (216) | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 18 |
| Forêt de Adé (10) | Adé › Tarbes-Lourdes-Pyrénées | 18 |
| Forêt de Bonnemazon (4) | Bonnemazon › Plateau de Lannemezan | 18 |
| Forêt de Chelle-Spou (10) | Chelle-Spou › Plateau de Lannemezan | 18 |
| Forêt de Coussan (2) | Coussan › Coteaux du Val-d'Arros | 18 |
| Forêt de La Barthe-de-Neste (7) | La Barthe-de-Neste › Plateau de Lannemezan | 18 |
| Forêt de Bareilles (10) | Bareilles › Aure Louron | 18 |
| Bois de Saint-Lary-Soulan (26) | Saint-Lary-Soulan › Aure Louron | 18 |
| Forêt de Beaudéan (35) | Beaudéan › Haute-Bigorre | 18 |
| Forêt de Saint-Pastous (12) | Saint-Pastous › Pyrénées Vallées des Gaves | 18 |
| Forêt de Aspin-en-Lavedan (10) | Aspin-en-Lavedan › Tarbes-Lourdes-Pyrénées | 18 |
| Forêt de Estaing (129) | Estaing › Pyrénées Vallées des Gaves | 18 |
| Forêt de Saint-Pé-de-Bigorre (69) | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 18 |
| Forêt de Castelbajac (9) | Castelbajac › Plateau de Lannemezan | 18 |
| Forêt de Antichan | Antichan › Neste Barousse | 18 |
| Forêt de Ferrère (84) | Ferrère › Neste Barousse | 18 |
| Forêt de Bizous (13) | Bizous › Neste Barousse | 18 |
| Forêt de Guchen (4) | Guchen › Aure Louron | 18 |
| Forêt de Saint-Lary-Soulan (209) | Saint-Lary-Soulan › Aure Louron | 18 |
| Forêt de Tramezaïgues (108) | Tramezaïgues › Aure Louron | 18 |
| Forêt de Luz-Saint-Sauveur (43) | Luz-Saint-Sauveur › Pyrénées Vallées des Gaves | 18 |
| Forêt de Viger (5) | Viger › Tarbes-Lourdes-Pyrénées | 18 |
| Forêt de Poueyferré (69) | Poueyferré › Tarbes-Lourdes-Pyrénées | 18 |
| Forêt de Lanespède | Lanespède › Coteaux du Val-d'Arros | 17 |
| Forêt de Bégole | Bégole › Coteaux du Val-d'Arros | 17 |
| Forêt de Escoubès-Pouts (6) | Escoubès-Pouts › Tarbes-Lourdes-Pyrénées | 17 |
| Forêt de Marseillan (5) | Marseillan › Coteaux du Val-d'Arros | 17 |
| Forêt de Lustar (15) | Lustar › Pays de Trie et du Magnoac | 17 |
| Forêt de Lannemezan (55) | Lannemezan › Plateau de Lannemezan | 17 |
| Forêt de Betpouy (2) | Betpouy › Pays de Trie et du Magnoac | 17 |
| Sapinière de Perche | Saint-Lary-Soulan › Aure Louron | 17 |
| Forêt de Aragnouet (65) | Aragnouet › Aure Louron | 17 |
| Forêt de Aragnouet (177) | Aragnouet › Aure Louron | 17 |
| Forêt de Saint-Lanne (3) | Saint-Lanne › Adour-Madiran (Hautes-Pyrénées) | 17 |
| Forêt de Aucun (70) | Aucun › Pyrénées Vallées des Gaves | 17 |
| Forêt de Peyrouse (41) | Peyrouse › Tarbes-Lourdes-Pyrénées | 17 |
| Forêt de Arrens-Marsous (254) | Arrens-Marsous › Pyrénées Vallées des Gaves | 17 |
| Forêt de Viscos (8) | Viscos › Pyrénées Vallées des Gaves | 17 |
| Forêt de Saint-Martin (45) | Saint-Martin › Tarbes-Lourdes-Pyrénées | 17 |
| Forêt de Bernac-Dessus (26) | Vielle-Adour › Tarbes-Lourdes-Pyrénées | 17 |
| Forêt de Montgaillard (62) | Montgaillard › Haute-Bigorre | 17 |
| Forêt de Tibiran-Jaunac (21) | Tibiran-Jaunac › Neste Barousse | 17 |
| Forêt de Sacoué (7) | Sacoué › Neste Barousse | 17 |
| Forêt de Loudenvielle (82) | Loudenvielle › Aure Louron | 17 |
| Forêt de Ancizan (38) | Ancizan › Aure Louron | 17 |
| Forêt de Cauterets (687) | Cauterets › Pyrénées Vallées des Gaves | 17 |
| Forêt de Auriébat (16) | Auriébat › Adour-Madiran (Hautes-Pyrénées) | 17 |
| Forêt de Vielle-Aure | Vielle-Aure › Aure Louron | 16 |
| Forêt de Ibos | Ibos › Tarbes-Lourdes-Pyrénées | 16 |
| Forêt de Trébons (2) | Trébons › Haute-Bigorre | 16 |
| Forêt de Camalès (7) | Camalès › Adour-Madiran (Hautes-Pyrénées) | 16 |
| Forêt de Bourg-de-Bigorre (7) | Bourg-de-Bigorre › Plateau de Lannemezan | 16 |
| Forêt de Chelle-Spou (13) | Chelle-Spou › Plateau de Lannemezan | 16 |
| Forêt de Gaussan | Gaussan › Pays de Trie et du Magnoac | 16 |
| Forêt de Cadéac | Cadéac › Aure Louron | 16 |
| Forêt de Monfaucon (7) | Monfaucon › Adour-Madiran (Hautes-Pyrénées) | 16 |
| Forêt de Saint-Lanne (8) | Saint-Lanne › Adour-Madiran (Hautes-Pyrénées) | 16 |
| Forêt de Gaillagos (86) | Gaillagos › Pyrénées Vallées des Gaves | 16 |
| Forêt de Arcizans-Dessus (40) | Arcizans-Dessus › Pyrénées Vallées des Gaves | 16 |
| Forêt des Angles (15) | Arcizac-ez-Angles › Tarbes-Lourdes-Pyrénées | 16 |
| Forêt de Gerde (55) | Gerde › Haute-Bigorre | 16 |
| Forêt de Orincles (23) | Orincles › Tarbes-Lourdes-Pyrénées | 16 |
| Forêt de Ordizan (59) | Ordizan › Haute-Bigorre | 16 |
| Forêt de Esparros (80) | Esparros › Plateau de Lannemezan | 16 |
| Forêt de Mauvezin (72) | Mauvezin › Plateau de Lannemezan | 16 |
| Forêt de Sadournin (8) | Sadournin › Pays de Trie et du Magnoac | 16 |
| Forêt de Génos (51) | Génos › Aure Louron | 16 |
| Forêt de Saint-Lary-Soulan (212) | Saint-Lary-Soulan › Aure Louron | 16 |
| Forêt de Vidouze (17) | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 16 |
| Forêt de Adast | Adast › Pyrénées Vallées des Gaves | 16 |
| Forêt de Campan | Campan › Haute-Bigorre | 15 |
| Forêt de Neuilh | Neuilh › Haute-Bigorre | 15 |
| Forêt de Arrens-Marsous | Arrens-Marsous › Pyrénées Vallées des Gaves | 15 |
| Forêt de Ancizan (2) | Ancizan › Aure Louron | 15 |
| Forêt de Viella | Viella › Pyrénées Vallées des Gaves | 15 |
| Forêt de Sazos (2) | Sazos › Pyrénées Vallées des Gaves | 15 |
| Forêt de Gavarnie-Gèdre (16) | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 15 |
| Forêt de Gavarnie-Gèdre (20) | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 15 |
| Forêt de Cauterets (233) | Cauterets › Pyrénées Vallées des Gaves | 15 |
| Forêt de Avezac-Prat-Lahitte (2) | Avezac-Prat-Lahitte › Plateau de Lannemezan | 15 |
| Forêt de Saint-Lary-Soulan (94) | Saint-Lary-Soulan › Aure Louron | 15 |
| Forêt de Castelnau-Rivière-Basse (2) | Castelnau-Rivière-Basse › Adour-Madiran (Hautes-Pyrénées) | 15 |
| Forêt de Gez (10) | Gez › Pyrénées Vallées des Gaves | 15 |
| Forêt de Ayros-Arbouix (31) | Préchac › Pyrénées Vallées des Gaves | 15 |
| Forêt de Arrens-Marsous (251) | Arrens-Marsous › Pyrénées Vallées des Gaves | 15 |
| Forêt de Campan (312) | Campan › Haute-Bigorre | 15 |
| Forêt de Saint-Pé-de-Bigorre (70) | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 15 |
| Forêt de Peyrouse (45) | Peyrouse › Tarbes-Lourdes-Pyrénées | 15 |
| Forêt de Lourdes (147) | Lourdes › Tarbes-Lourdes-Pyrénées | 15 |
| Forêt de Bettes (29) | Bettes › Haute-Bigorre | 15 |
| Forêt de Mauvezin (70) | Mauvezin › Plateau de Lannemezan | 15 |
| Forêt de Castelvieilh (19) | Castelvieilh › Coteaux du Val-d'Arros | 15 |
| Forêt de Bouilh-Péreuilh (16) | Bouilh-Péreuilh › Coteaux du Val-d'Arros | 15 |
| Forêt de Sénac (28) | Mansan › Adour-Madiran (Hautes-Pyrénées) | 15 |
| Forêt de Bégole (17) | Bégole › Coteaux du Val-d'Arros | 15 |
| Forêt de Villemur (4) | Pouy › Pays de Trie et du Magnoac | 15 |
| Forêt de Pinas (8) | Pinas › Plateau de Lannemezan | 15 |
| Forêt de Cantaous (14) | Cantaous › Neste Barousse | 15 |
| Forêt de Bramevaque (2) | Bramevaque › Neste Barousse | 15 |
| Forêt de Montoussé (9) | Montoussé › Plateau de Lannemezan | 15 |
| Forêt de La Barthe-de-Neste (16) | La Barthe-de-Neste › Plateau de Lannemezan | 15 |
| Forêt de Madiran (26) | Madiran › Adour-Madiran (Hautes-Pyrénées) | 15 |
| Forêt de Saint-Lézer (3) | Saint-Lézer › Adour-Madiran (Hautes-Pyrénées) | 14 |
| Forêt de Lourdes (2) | Lourdes › Tarbes-Lourdes-Pyrénées | 14 |
| Forêt de Ourdis-Cotdoussan | Ourdis-Cotdoussan › Tarbes-Lourdes-Pyrénées | 14 |
| Forêt de Arrens-Marsous (2) | Arrens-Marsous › Pyrénées Vallées des Gaves | 14 |
| Bois de Campan (3) | Campan › Haute-Bigorre | 14 |
| Forêt de Laslades | Laslades › Coteaux du Val-d'Arros | 14 |
| Forêt de Caubous | Caubous › Pays de Trie et du Magnoac | 14 |
| Forêt de Uglas (6) | Uglas › Plateau de Lannemezan | 14 |
| Bois de Labatut-Rivière (28) | Labatut-Rivière › Adour-Madiran (Hautes-Pyrénées) | 14 |
| Forêt de Ibos (107) | Ibos › Tarbes-Lourdes-Pyrénées | 14 |
| Forêt de Arras-en-Lavedan (77) | Arras-en-Lavedan › Pyrénées Vallées des Gaves | 14 |
| Forêt de Bun (35) | Bun › Pyrénées Vallées des Gaves | 14 |
| Forêt de Beaucens (54) | Beaucens › Pyrénées Vallées des Gaves | 14 |
| Forêt de Viey (24) | Viey › Pyrénées Vallées des Gaves | 14 |
| Forêt de Pouzac (75) | Pouzac › Haute-Bigorre | 14 |
| Forêt de Pouzac (76) | Pouzac › Haute-Bigorre | 14 |
| Forêt de Bazillac (59) | Bazillac › Adour-Madiran (Hautes-Pyrénées) | 14 |
| Forêt de Visker (23) | Arcizac-Adour › Tarbes-Lourdes-Pyrénées | 14 |
| Forêt de Mauvezin (69) | Mauvezin › Plateau de Lannemezan | 14 |
| Forêt de Mingot (2) | Mingot › Adour-Madiran (Hautes-Pyrénées) | 14 |
| Forêt de Louit (8) | Louit › Coteaux du Val-d'Arros | 14 |
| Forêt de Arné (16) | Arné › Plateau de Lannemezan | 14 |
| Forêt de Mazères-de-Neste (10) | Mazères-de-Neste › Neste Barousse | 14 |
| Forêt de Mont (40) | Mont › Aure Louron | 14 |
| Forêt de Lahitte-Toupière (3) | Lahitte-Toupière › Adour-Madiran (Hautes-Pyrénées) | 14 |
| Forêt de Arcizans-Dessus (42) | Arcizans-Dessus › Pyrénées Vallées des Gaves | 14 |
| Forêt de Lourdes (3) | Lourdes › Tarbes-Lourdes-Pyrénées | 13 |
| Forêt de Cieutat | Cieutat › Haute-Bigorre | 13 |
| Forêt de Aventignan | Aventignan › Neste Barousse | 13 |
| Forêt de Gazost (2) | Gazost › Tarbes-Lourdes-Pyrénées | 13 |
| Forêt de Espieilh (6) | Espieilh › Plateau de Lannemezan | 13 |
| Forêt de Lannemezan (44) | Lannemezan › Plateau de Lannemezan | 13 |
| Forêt de La Barthe-de-Neste (10) | La Barthe-de-Neste › Plateau de Lannemezan | 13 |
| Forêt de Saint-Lary-Soulan (46) | Saint-Lary-Soulan › Aure Louron | 13 |
| Forêt de Sazos (46) | Sazos › Pyrénées Vallées des Gaves | 13 |
| Forêt de Betpouey (21) | Betpouey › Pyrénées Vallées des Gaves | 13 |
| Forêt de Aucun (69) | Aucun › Pyrénées Vallées des Gaves | 13 |
| Forêt de Gavarnie-Gèdre (322) | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 13 |
| Forêt de Ossen (4) | Ossen › Tarbes-Lourdes-Pyrénées | 13 |
| Forêt de Omex (6) | Omex › Tarbes-Lourdes-Pyrénées | 13 |
| Forêt de Gazost (39) | Gazost › Tarbes-Lourdes-Pyrénées | 13 |
| Forêt de Peyrouse (42) | Peyrouse › Tarbes-Lourdes-Pyrénées | 13 |
| Forêt de Arras-en-Lavedan (86) | Arras-en-Lavedan › Pyrénées Vallées des Gaves | 13 |
| Forêt de Bours (36) | Bours › Tarbes-Lourdes-Pyrénées | 13 |
| Forêt de Esconnets (14) | Bettes › Haute-Bigorre | 13 |
| Forêt de Espieilh (15) | Espieilh › Plateau de Lannemezan | 13 |
| Forêt de Villembits (13) | Villembits › Pays de Trie et du Magnoac | 13 |
| Forêt de Campuzan (2) | Campuzan › Pays de Trie et du Magnoac | 13 |
| Forêt de Saint-Paul (29) | Saint-Paul › Neste Barousse | 13 |
| Forêt de Estarvielle (12) | Mont › Aure Louron | 13 |
| Forêt de Saint-Lary-Soulan (211) | Saint-Lary-Soulan › Aure Louron | 13 |
| Forêt de Saint-Lary-Soulan (214) | Saint-Lary-Soulan › Aure Louron | 13 |
| Forêt de Tramezaïgues (106) | Tramezaïgues › Aure Louron | 13 |
| Forêt de Aragnouet (206) | Aragnouet › Aure Louron | 13 |
| Forêt de Villenave-près-Béarn (4) | Villenave-près-Béarn › Adour-Madiran (Hautes-Pyrénées) | 13 |
| Forêt de Larreule (3) | Larreule › Adour-Madiran (Hautes-Pyrénées) | 13 |
| Forêt de Adé (35) | Adé › Tarbes-Lourdes-Pyrénées | 13 |
| Forêt de Arrens-Marsous (260) | Arrens-Marsous › Pyrénées Vallées des Gaves | 13 |
| Forêt de Gazost (47) | Gazost › Tarbes-Lourdes-Pyrénées | 13 |
| Forêt de Pouzac (78) | Labassère › Haute-Bigorre | 13 |
| Forêt de Réjaumont | Réjaumont › Plateau de Lannemezan | 12 |
| Forêt de Bonnemazon | Bonnemazon › Plateau de Lannemezan | 12 |
| Forêt de Barèges | Barèges › Pyrénées Vallées des Gaves | 12 |
| Forêt de Gavarnie-Gèdre (2) | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 12 |
| Forêt de Burg | Burg › Coteaux du Val-d'Arros | 12 |
| Forêt de Adervielle-Pouchergues | Adervielle-Pouchergues › Aure Louron | 12 |
| Forêt de Cauterets (232) | Cauterets › Pyrénées Vallées des Gaves | 12 |
| Forêt de Aurensan (2) | Aurensan › Tarbes-Lourdes-Pyrénées | 12 |
| Forêt de Julos (17) | Julos › Tarbes-Lourdes-Pyrénées | 12 |
| Forêt de Espèche (7) | Espèche › Plateau de Lannemezan | 12 |
| Forêt de Espèche (8) | Espèche › Plateau de Lannemezan | 12 |
| Forêt de Montastruc (17) | Montastruc › Plateau de Lannemezan | 12 |
| Forêt de Castelnau-Magnoac (7) | Castelnau-Magnoac › Pays de Trie et du Magnoac | 12 |
| Forêt de Aries-Espénan | Aries-Espénan › Pays de Trie et du Magnoac | 12 |
| Forêt de Nestier (6) | Nestier › Neste Barousse | 12 |
| Forêt de Aragnouet (48) | Aragnouet › Aure Louron | 12 |
| Forêt de Beaudéan (37) | Beaudéan › Haute-Bigorre | 12 |
| Forêt de Agos-Vidalos (2) | Agos-Vidalos › Pyrénées Vallées des Gaves | 12 |
| Bois de Cauterets (42) | Cauterets › Pyrénées Vallées des Gaves | 12 |
| Forêt de Labassère (61) | Labassère › Haute-Bigorre | 12 |
| Forêt de Labassère (63) | Labassère › Haute-Bigorre | 12 |
| Forêt de Madiran (20) | Madiran › Adour-Madiran (Hautes-Pyrénées) | 12 |
| Forêt de Loucrup (36) | Hiis › Tarbes-Lourdes-Pyrénées | 12 |
| Forêt de Burg (24) | Bernadets-Dessus › Coteaux du Val-d'Arros | 12 |
| Forêt de Castelbajac (13) | Castelbajac › Plateau de Lannemezan | 12 |
| Forêt de Aragnouet (208) | Aragnouet › Aure Louron | 12 |
| Forêt de Barèges (216) | Barèges › Pyrénées Vallées des Gaves | 12 |
| Forêt de Séron (12) | Séron › Tarbes-Lourdes-Pyrénées | 12 |
| Forêt de Saint-Lézer (30) | Saint-Lézer › Adour-Madiran (Hautes-Pyrénées) | 12 |
| Forêt de Auriébat (15) | Auriébat › Adour-Madiran (Hautes-Pyrénées) | 12 |
| Forêt de Saint-Lanne (15) | Saint-Lanne › Adour-Madiran (Hautes-Pyrénées) | 12 |
| Forêt de Tilhouse | Tilhouse › Plateau de Lannemezan | 11 |
| Forêt de Ancizan | Ancizan › Aure Louron | 11 |
| Forêt de Loudenvielle | Loudenvielle › Aure Louron | 11 |
| Forêt de Arrens-Marsous (17) | Arrens-Marsous › Pyrénées Vallées des Gaves | 11 |
| Forêt de Sers (41) | Sers › Pyrénées Vallées des Gaves | 11 |
| Forêt de Cauterets (343) | Cauterets › Pyrénées Vallées des Gaves | 11 |
| Forêt de Saint-Pé-de-Bigorre (37) | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 11 |
| Forêt de Bazillac | Bazillac › Adour-Madiran (Hautes-Pyrénées) | 11 |
| Forêt de Orleix (28) | Orleix › Tarbes-Lourdes-Pyrénées | 11 |
| Forêt de Bordes (8) | Bordes › Coteaux du Val-d'Arros | 11 |
| Forêt de Sénac (12) | Sénac › Adour-Madiran (Hautes-Pyrénées) | 11 |
| Forêt de Galan (7) | Galan › Plateau de Lannemezan | 11 |
| Forêt de Bazordan (5) | Bazordan › Pays de Trie et du Magnoac | 11 |
| Forêt de Izaux | Izaux › Plateau de Lannemezan | 11 |
| Forêt de La Barthe-de-Neste (9) | La Barthe-de-Neste › Plateau de Lannemezan | 11 |
| Forêt de Saint-Lary-Soulan (149) | Saint-Lary-Soulan › Aure Louron | 11 |
| Forêt de Salles (23) | Salles › Pyrénées Vallées des Gaves | 11 |
| Forêt de Arrens-Marsous (239) | Arrens-Marsous › Pyrénées Vallées des Gaves | 11 |
| Forêt de Omex (4) | Omex › Tarbes-Lourdes-Pyrénées | 11 |
| Forêt de Paréac (9) | Paréac › Tarbes-Lourdes-Pyrénées | 11 |
| Forêt de Montgaillard (61) | Montgaillard › Haute-Bigorre | 11 |
| Forêt de Labastide (49) | Labastide › Plateau de Lannemezan | 11 |
| Forêt de Mauvezin (74) | Mauvezin › Plateau de Lannemezan | 11 |
| Forêt de Capvern (215) | Capvern › Plateau de Lannemezan | 11 |
| Forêt de Burg (25) | Burg › Coteaux du Val-d'Arros | 11 |
| Forêt de Galan (15) | Galan › Plateau de Lannemezan | 11 |
| Forêt de Bazordan (17) | Bazordan › Pays de Trie et du Magnoac | 11 |
| Forêt de La Barthe-de-Neste (17) | La Barthe-de-Neste › Plateau de Lannemezan | 11 |
| Forêt de Mont (41) | Mont › Aure Louron | 11 |
| Forêt de Aragnouet (209) | Aragnouet › Aure Louron | 11 |
| Forêt de Saint-Lary-Soulan (216) | Saint-Lary-Soulan › Aure Louron | 11 |
| Forêt des Angles (16) | Les Angles › Tarbes-Lourdes-Pyrénées | 11 |
| Forêt de Arras-en-Lavedan (90) | Arras-en-Lavedan › Pyrénées Vallées des Gaves | 11 |
| Forêt de Bazillac (17) | Bazillac › Adour-Madiran (Hautes-Pyrénées) | 10 |
| Forêt de Barbazan-Dessus (2) | Bernac-Dessus › Tarbes-Lourdes-Pyrénées | 10 |
| Forêt de Tournay | Tournay › Coteaux du Val-d'Arros | 10 |
| Forêt de Bourg-de-Bigorre (8) | Bourg-de-Bigorre › Plateau de Lannemezan | 10 |
| Forêt de Avezac-Prat-Lahitte (11) | Avezac-Prat-Lahitte › Plateau de Lannemezan | 10 |
| Forêt de Artiguemy (14) | Artiguemy › Plateau de Lannemezan | 10 |
| Forêt de Moumoulous (2) | Moumoulous › Adour-Madiran (Hautes-Pyrénées) | 10 |
| Forêt de Sadournin (4) | Sadournin › Pays de Trie et du Magnoac | 10 |
| Forêt de Bize (2) | Bize › Neste Barousse | 10 |
| Forêt de Aragnouet (186) | Aragnouet › Aure Louron | 10 |
| Forêt de Escaunets (9) | Escaunets › Adour-Madiran (Hautes-Pyrénées) | 10 |
| Forêt de Nouilhan (2) | Nouilhan › Adour-Madiran (Hautes-Pyrénées) | 10 |
| Forêt de Lourdes (140) | Lourdes › Tarbes-Lourdes-Pyrénées | 10 |
| Forêt de Saint-Pé-de-Bigorre (67) | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 10 |
| Forêt de Arrens-Marsous (237) | Arrens-Marsous › Pyrénées Vallées des Gaves | 10 |
| Forêt de Gavarnie-Gèdre (321) | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 10 |
| Forêt de Arras-en-Lavedan (80) | Arras-en-Lavedan › Pyrénées Vallées des Gaves | 10 |
| Forêt de Berbérust-Lias (24) | Berbérust-Lias › Tarbes-Lourdes-Pyrénées | 10 |
| Forêt de Sers (84) | Sers › Pyrénées Vallées des Gaves | 10 |
| Forêt de Astugue (66) | Astugue › Haute-Bigorre | 10 |
| Forêt de Arrodets-ez-Angles (19) | Arrodets-ez-Angles › Tarbes-Lourdes-Pyrénées | 10 |
| Forêt de Beaudéan (38) | Beaudéan › Haute-Bigorre | 10 |
| Forêt de Tostat (14) | Tostat › Adour-Madiran (Hautes-Pyrénées) | 10 |
| Forêt de Bazillac (58) | Bazillac › Adour-Madiran (Hautes-Pyrénées) | 10 |
| Forêt de Espieilh (16) | Espieilh › Plateau de Lannemezan | 10 |
| Forêt de Lacassagne (14) | Lacassagne › Adour-Madiran (Hautes-Pyrénées) | 10 |
| Forêt de Villembits (12) | Villembits › Pays de Trie et du Magnoac | 10 |
| Forêt de Sère-Rustaing (9) | Bugard › Pays de Trie et du Magnoac | 10 |
| Forêt de Recurt (22) | Recurt › Plateau de Lannemezan | 10 |
| Forêt de Tournous-Devant (3) | Tournous-Devant › Plateau de Lannemezan | 10 |
| Forêt de Puntous (5) | Puntous › Pays de Trie et du Magnoac | 10 |
| Forêt de Tuzaguet (10) | Tuzaguet › Neste Barousse | 10 |
| Forêt de Aventignan (8) | Aventignan › Neste Barousse | 10 |
| Forêt de Thèbe (2) | Thèbe › Neste Barousse | 10 |
| Forêt de Aragnouet (211) | Aragnouet › Aure Louron | 10 |
| Forêt de Gardères (18) | Gardères › Tarbes-Lourdes-Pyrénées | 10 |
| Forêt de Escaunets (11) | Escaunets › Adour-Madiran (Hautes-Pyrénées) | 10 |
| Forêt de Sauveterre (6) | Sauveterre › Adour-Madiran (Hautes-Pyrénées) | 10 |
| Forêt de Madiran (23) | Madiran › Adour-Madiran (Hautes-Pyrénées) | 10 |
| Forêt de Madiran (27) | Madiran › Adour-Madiran (Hautes-Pyrénées) | 10 |
| Forêt de Arrens-Marsous (263) | Arrens-Marsous › Pyrénées Vallées des Gaves | 10 |
| Forêt de Arrens-Marsous (265) | Arrens-Marsous › Pyrénées Vallées des Gaves | 10 |
| Forêt de Vidouze ⚠️ | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 9 |
| Forêt de Coussan ⚠️ | Coussan › Coteaux du Val-d'Arros | 9 |
| Forêt de Cheust (2) ⚠️ | Cheust › Tarbes-Lourdes-Pyrénées | 9 |
| Forêt de Cauterets (481) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 9 |
| Bois de Labarthe ⚠️ | Séméac › Tarbes-Lourdes-Pyrénées | 9 |
| Forêt de Neuilh (7) ⚠️ | Neuilh › Haute-Bigorre | 9 |
| Forêt de Bourréac (6) ⚠️ | Bourréac › Tarbes-Lourdes-Pyrénées | 9 |
| Forêt de Camalès (3) ⚠️ | Camalès › Adour-Madiran (Hautes-Pyrénées) | 9 |
| Forêt de Bonnemazon (13) ⚠️ | Bonnemazon › Plateau de Lannemezan | 9 |
| Forêt de Marquerie (2) ⚠️ | Marquerie › Coteaux du Val-d'Arros | 9 |
| Forêt de Fontrailles (4) ⚠️ | Fontrailles › Pays de Trie et du Magnoac | 9 |
| Forêt de Bonrepos (4) ⚠️ | Bonrepos › Plateau de Lannemezan | 9 |
| Forêt de Lannemezan (26) ⚠️ | Lannemezan › Plateau de Lannemezan | 9 |
| Forêt de Betbèze ⚠️ | Betbèze › Pays de Trie et du Magnoac | 9 |
| Forêt de Saint-Paul (14) ⚠️ | Saint-Paul › Neste Barousse | 9 |
| Forêt de Bazus-Neste (3) ⚠️ | Saint-Arroman › Plateau de Lannemezan | 9 |
| Forêt de Azet (48) ⚠️ | Azet › Aure Louron | 9 |
| Forêt de Saint-Lary-Soulan (69) ⚠️ | Saint-Lary-Soulan › Aure Louron | 9 |
| Forêt de Tramezaïgues (40) ⚠️ | Tramezaïgues › Aure Louron | 9 |
| Forêt de Saint-Lary-Soulan (127) ⚠️ | Saint-Lary-Soulan › Aure Louron | 9 |
| Forêt de Sarriac-Bigorre (14) ⚠️ | Sarriac-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 9 |
| Forêt de Monfaucon (4) ⚠️ | Monfaucon › Adour-Madiran (Hautes-Pyrénées) | 9 |
| Forêt de Soublecause (5) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 9 |
| Forêt de Sassis (3) ⚠️ | Sassis › Pyrénées Vallées des Gaves | 9 |
| Forêt de Estaing (125) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 9 |
| Forêt de Arras-en-Lavedan (73) ⚠️ | Arras-en-Lavedan › Pyrénées Vallées des Gaves | 9 |
| Forêt de Aurensan (29) ⚠️ | Aurensan › Tarbes-Lourdes-Pyrénées | 9 |
| Forêt de Gez (9) ⚠️ | Gez › Pyrénées Vallées des Gaves | 9 |
| Forêt de Arras-en-Lavedan (82) ⚠️ | Arras-en-Lavedan › Pyrénées Vallées des Gaves | 9 |
| Bois de Geu (18) ⚠️ | Geu › Tarbes-Lourdes-Pyrénées | 9 |
| Forêt de Saint-Pastous (10) ⚠️ | Saint-Pastous › Pyrénées Vallées des Gaves | 9 |
| Forêt de Saint-Créac (5) ⚠️ | Saint-Créac › Tarbes-Lourdes-Pyrénées | 9 |
| Forêt de Bagnères-de-Bigorre (234) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 9 |
| Forêt de Gez-ez-Angles (27) ⚠️ | Gez-ez-Angles › Tarbes-Lourdes-Pyrénées | 9 |
| Forêt de Julos (54) ⚠️ | Julos › Tarbes-Lourdes-Pyrénées | 9 |
| Forêt de Ossun (62) ⚠️ | Ossun › Tarbes-Lourdes-Pyrénées | 9 |
| Forêt de Villenave-près-Marsac (2) ⚠️ | Villenave-près-Marsac › Adour-Madiran (Hautes-Pyrénées) | 9 |
| Forêt de Arcizac-Adour (30) ⚠️ | Arcizac-Adour › Tarbes-Lourdes-Pyrénées | 9 |
| Forêt de Hauban (16) ⚠️ | Hauban › Haute-Bigorre | 9 |
| Forêt de Bordes (67) ⚠️ | Bordes › Coteaux du Val-d'Arros | 9 |
| Forêt de Bouilh-Péreuilh (15) ⚠️ | Bouilh-Péreuilh › Coteaux du Val-d'Arros | 9 |
| Forêt de Saint-Paul (28) ⚠️ | Saint-Paul › Neste Barousse | 9 |
| Forêt de Montoussé (7) ⚠️ | Montoussé › Plateau de Lannemezan | 9 |
| Forêt de Escala (7) ⚠️ | Escala › Plateau de Lannemezan | 9 |
| Forêt de La Barthe-de-Neste (19) ⚠️ | La Barthe-de-Neste › Plateau de Lannemezan | 9 |
| Forêt de Arreau (4) ⚠️ | Aspin-Aure › Aure Louron | 9 |
| Forêt de Aulon (6) ⚠️ | Aulon › Aure Louron | 9 |
| Forêt de Larreule (2) ⚠️ | Larreule › Adour-Madiran (Hautes-Pyrénées) | 9 |
| Forêt de Estirac (2) ⚠️ | Estirac › Adour-Madiran (Hautes-Pyrénées) | 9 |
| Forêt de Maubourguet (19) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 9 |
| Bois de Castelnau-Rivière-Basse (50) ⚠️ | Castelnau-Rivière-Basse › Adour-Madiran (Hautes-Pyrénées) | 9 |
| Forêt de Saligos (29) ⚠️ | Saligos › Pyrénées Vallées des Gaves | 9 |
| Forêt de Viscos (11) ⚠️ | Viscos › Pyrénées Vallées des Gaves | 9 |
| Forêt de Viger (4) ⚠️ | Viger › Tarbes-Lourdes-Pyrénées | 9 |
| Forêt de Ségus (4) ⚠️ | Ségus › Tarbes-Lourdes-Pyrénées | 9 |
| Forêt de Omex (7) ⚠️ | Omex › Tarbes-Lourdes-Pyrénées | 9 |
| Forêt de Germs-sur-l'Oussouet (15) ⚠️ | Germs-sur-l'Oussouet › Tarbes-Lourdes-Pyrénées | 9 |
| Forêt de Pouyastruc (26) ⚠️ | Pouyastruc › Coteaux du Val-d'Arros | 9 |
| Forêt de Fontrailles ⚠️ | Fontrailles › Pays de Trie et du Magnoac | 8 |
| Artigamia ⚠️ | Estaing › Pyrénées Vallées des Gaves | 8 |
| Forêt de Estaing (46) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 8 |
| Forêt de Vielle-Aure (86) ⚠️ | Vielle-Aure › Aure Louron | 8 |
| Forêt de Gavarnie-Gèdre (140) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 8 |
| Forêt de Cauterets (334) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 8 |
| Forêt de Ancizan (4) ⚠️ | Ancizan › Aure Louron | 8 |
| Forêt de Saint-Lézer (9) ⚠️ | Pujo › Adour-Madiran (Hautes-Pyrénées) | 8 |
| Forêt de Pouyastruc (25) ⚠️ | Pouyastruc › Coteaux du Val-d'Arros | 8 |
| Forêt de Fréchède (3) ⚠️ | Fréchède › Pays de Trie et du Magnoac | 8 |
| Bois de Bernadets-Debat ⚠️ | Bernadets-Debat › Pays de Trie et du Magnoac | 8 |
| Forêt de Campistrous (13) ⚠️ | Campistrous › Plateau de Lannemezan | 8 |
| Forêt de Capvern (198) ⚠️ | Capvern › Plateau de Lannemezan | 8 |
| Forêt de Tajan (3) ⚠️ | Recurt › Plateau de Lannemezan | 8 |
| Forêt de Lalanne (4) ⚠️ | Lalanne › Pays de Trie et du Magnoac | 8 |
| Forêt de Bazus-Neste (5) ⚠️ | Bazus-Neste › Plateau de Lannemezan | 8 |
| Forêt de Izaux (4) ⚠️ | Izaux › Plateau de Lannemezan | 8 |
| Forêt de Cazaux-Fréchet-Anéran-Camors (10) ⚠️ | Cazaux-Fréchet-Anéran-Camors › Aure Louron | 8 |
| Forêt de Aulon ⚠️ | Aulon › Aure Louron | 8 |
| Forêt de Azet (45) ⚠️ | Azet › Aure Louron | 8 |
| Bois de Saint-Lary-Soulan ⚠️ | Saint-Lary-Soulan › Aure Louron | 8 |
| Forêt de Aragnouet (45) ⚠️ | Aragnouet › Aure Louron | 8 |
| Forêt de Aragnouet (84) ⚠️ | Aragnouet › Aure Louron | 8 |
| Forêt de Saint-Lary-Soulan (158) ⚠️ | Saint-Lary-Soulan › Aure Louron | 8 |
| Forêt de Sombrun (2) ⚠️ | Sombrun › Adour-Madiran (Hautes-Pyrénées) | 8 |
| Forêt de Vidouze (10) ⚠️ | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 8 |
| Forêt de Saint-Lanne (9) ⚠️ | Saint-Lanne › Adour-Madiran (Hautes-Pyrénées) | 8 |
| Forêt de Sers (80) ⚠️ | Sers › Pyrénées Vallées des Gaves | 8 |
| Forêt de Gaillagos (88) ⚠️ | Gaillagos › Pyrénées Vallées des Gaves | 8 |
| Forêt de Ayzac-Ost ⚠️ | Ayzac-Ost › Pyrénées Vallées des Gaves | 8 |
| Forêt de Arrens-Marsous (246) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 8 |
| Forêt de Esterre (4) ⚠️ | Esterre › Pyrénées Vallées des Gaves | 8 |
| Forêt de Sers (86) ⚠️ | Sers › Pyrénées Vallées des Gaves | 8 |
| Forêt de Cauterets (685) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 8 |
| Forêt de Montgaillard (59) ⚠️ | Montgaillard › Haute-Bigorre | 8 |
| Forêt de Poueyferré (66) ⚠️ | Poueyferré › Tarbes-Lourdes-Pyrénées | 8 |
| Forêt de Juillan (92) ⚠️ | Juillan › Tarbes-Lourdes-Pyrénées | 8 |
| Forêt de Mascaras (28) ⚠️ | Mascaras › Coteaux du Val-d'Arros | 8 |
| Forêt de Hitte (15) ⚠️ | Hitte › Haute-Bigorre | 8 |
| Forêt de Esparros (78) ⚠️ | Esparros › Plateau de Lannemezan | 8 |
| Forêt de Avezac-Prat-Lahitte (114) ⚠️ | Avezac-Prat-Lahitte › Plateau de Lannemezan | 8 |
| Forêt de Capvern (201) ⚠️ | Capvern › Plateau de Lannemezan | 8 |
| Forêt de Péré (28) ⚠️ | Péré › Plateau de Lannemezan | 8 |
| Forêt de Moulédous (14) ⚠️ | Moulédous › Coteaux du Val-d'Arros | 8 |
| Forêt de Fréchède (11) ⚠️ | Fréchède › Pays de Trie et du Magnoac | 8 |
| Forêt de Lutilhous (3) ⚠️ | Lutilhous › Plateau de Lannemezan | 8 |
| Forêt de Lannemezan (70) ⚠️ | Lannemezan › Plateau de Lannemezan | 8 |
| Forêt de Sabarros (6) ⚠️ | Sabarros › Plateau de Lannemezan | 8 |
| Forêt de Castelnau-Magnoac (12) ⚠️ | Castelnau-Magnoac › Pays de Trie et du Magnoac | 8 |
| Forêt de Saint-Laurent-de-Neste (20) ⚠️ | Saint-Laurent-de-Neste › Neste Barousse | 8 |
| Forêt de Aventignan (7) ⚠️ | Aventignan › Neste Barousse | 8 |
| Forêt de Gembrie ⚠️ | Gembrie › Neste Barousse | 8 |
| Forêt de Montégut (7) ⚠️ | Montégut › Neste Barousse | 8 |
| Forêt de Génos (54) ⚠️ | Génos › Aure Louron | 8 |
| Forêt de Monfaucon (10) ⚠️ | Monfaucon › Adour-Madiran (Hautes-Pyrénées) | 8 |
| Forêt de Auriébat (14) ⚠️ | Auriébat › Adour-Madiran (Hautes-Pyrénées) | 8 |
| Forêt de Vidouze (18) ⚠️ | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 8 |
| Forêt de Madiran (24) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 8 |
| Forêt de Sers (88) ⚠️ | Sers › Pyrénées Vallées des Gaves | 8 |
| Forêt de Madiran (28) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 8 |
| Forêt de Marseillan ⚠️ | Marseillan › Coteaux du Val-d'Arros | 7 |
| Forêt de Arrens-Marsous (16) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 7 |
| Forêt de Germs-sur-l'Oussouet ⚠️ | Germs-sur-l'Oussouet › Tarbes-Lourdes-Pyrénées | 7 |
| Forêt de Estaing (70) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 7 |
| Forêt de Gavarnie-Gèdre (229) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 7 |
| Forêt de Arbéost (4) ⚠️ | Arbéost › Pays de Nay (Hautes-Pyrénées) | 7 |
| Bois de Bordères-sur-l'Échez (2) ⚠️ | Oursbelille › Tarbes-Lourdes-Pyrénées | 7 |
| Forêt de Campan (195) ⚠️ | Campan › Haute-Bigorre | 7 |
| Forêt de Beyrède-Jumet-Camous (4) ⚠️ | Beyrède-Jumet-Camous › Aure Louron | 7 |
| Forêt de Loucrup (2) ⚠️ | Loucrup › Tarbes-Lourdes-Pyrénées | 7 |
| Forêt de Bartrès (39) ⚠️ | Bartrès › Tarbes-Lourdes-Pyrénées | 7 |
| Forêt de Ossun (5) ⚠️ | Ossun › Tarbes-Lourdes-Pyrénées | 7 |
| Forêt de Julos (18) ⚠️ | Julos › Tarbes-Lourdes-Pyrénées | 7 |
| Forêt de Sarniguet (6) ⚠️ | Sarniguet › Tarbes-Lourdes-Pyrénées | 7 |
| Forêt de Ordizan (39) ⚠️ | Ordizan › Haute-Bigorre | 7 |
| Forêt de Espèche (13) ⚠️ | Espèche › Plateau de Lannemezan | 7 |
| Forêt de Lannemezan (7) ⚠️ | Lannemezan › Plateau de Lannemezan | 7 |
| Forêt de Péré (15) ⚠️ | Péré › Plateau de Lannemezan | 7 |
| Forêt de Pouyastruc (4) ⚠️ | Pouyastruc › Coteaux du Val-d'Arros | 7 |
| Forêt de Collongues ⚠️ | Collongues › Coteaux du Val-d'Arros | 7 |
| Forêt de Lizos (6) ⚠️ | Lizos › Coteaux du Val-d'Arros | 7 |
| Forêt de Osmets (2) ⚠️ | Osmets › Pays de Trie et du Magnoac | 7 |
| Forêt de Bouilh-Devant (10) ⚠️ | Bouilh-Devant › Adour-Madiran (Hautes-Pyrénées) | 7 |
| Forêt de Sère-Rustaing (3) ⚠️ | Sère-Rustaing › Pays de Trie et du Magnoac | 7 |
| Forêt de Montastruc (15) ⚠️ | Montastruc › Plateau de Lannemezan | 7 |
| Forêt de Bonrepos ⚠️ | Bonrepos › Plateau de Lannemezan | 7 |
| Forêt de Clarens (11) ⚠️ | Clarens › Plateau de Lannemezan | 7 |
| Forêt de Larroque (5) ⚠️ | Larroque › Pays de Trie et du Magnoac | 7 |
| Forêt de Peyret-Saint-André (4) ⚠️ | Peyret-Saint-André › Pays de Trie et du Magnoac | 7 |
| Bois de Gaussan (27) ⚠️ | Gaussan › Pays de Trie et du Magnoac | 7 |
| Forêt de Tuzaguet (3) ⚠️ | Cantaous › Neste Barousse | 7 |
| Bois de Nestier ⚠️ | Nestier › Neste Barousse | 7 |
| Forêt de Aveux ⚠️ | Aveux › Neste Barousse | 7 |
| Forêt de Hautaget ⚠️ | Hautaget › Neste Barousse | 7 |
| Forêt de Mont ⚠️ | Mont › Aure Louron | 7 |
| Bois de Aulon (8) ⚠️ | Aulon › Aure Louron | 7 |
| Forêt de Aulon (2) ⚠️ | Aulon › Aure Louron | 7 |
| Forêt de Tramezaïgues (25) ⚠️ | Tramezaïgues › Aure Louron | 7 |
| Forêt de Aragnouet (87) ⚠️ | Aragnouet › Aure Louron | 7 |
| Forêt de Saint-Lary-Soulan (144) ⚠️ | Saint-Lary-Soulan › Aure Louron | 7 |
| Forêt de Artagnan (8) ⚠️ | Artagnan › Adour-Madiran (Hautes-Pyrénées) | 7 |
| Forêt de Lafitole (8) ⚠️ | Lafitole › Adour-Madiran (Hautes-Pyrénées) | 7 |
| Bois de Maubourguet (59) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 7 |
| Bois de Labatut-Rivière (26) ⚠️ | Labatut-Rivière › Adour-Madiran (Hautes-Pyrénées) | 7 |
| Forêt de Madiran (7) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 7 |
| Forêt de Madiran (19) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 7 |
| Forêt de Villenave-près-Béarn (2) ⚠️ | Villenave-près-Béarn › Adour-Madiran (Hautes-Pyrénées) | 7 |
| Forêt de Arrens-Marsous (240) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 7 |
| Forêt de Aucun (71) ⚠️ | Aucun › Pyrénées Vallées des Gaves | 7 |
| Forêt de Ségus (3) ⚠️ | Ségus › Tarbes-Lourdes-Pyrénées | 7 |
| Forêt de Arrens-Marsous (247) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 7 |
| Forêt de Artalens-Souin (45) ⚠️ | Artalens-Souin › Pyrénées Vallées des Gaves | 7 |
| Forêt de Loubajac (39) ⚠️ | Loubajac › Tarbes-Lourdes-Pyrénées | 7 |
| Forêt de Antist (10) ⚠️ | Antist › Haute-Bigorre | 7 |
| Forêt de Avezac-Prat-Lahitte (107) ⚠️ | Avezac-Prat-Lahitte › Plateau de Lannemezan | 7 |
| Forêt de Trouley-Labarthe (6) ⚠️ | Trouley-Labarthe › Adour-Madiran (Hautes-Pyrénées) | 7 |
| Forêt de Orieux (11) ⚠️ | Orieux › Coteaux du Val-d'Arros | 7 |
| Forêt de Libaros (9) ⚠️ | Libaros › Plateau de Lannemezan | 7 |
| Forêt de Cizos (14) ⚠️ | Cizos › Pays de Trie et du Magnoac | 7 |
| Forêt de Lalanne (8) ⚠️ | Lalanne › Pays de Trie et du Magnoac | 7 |
| Forêt de Thermes-Magnoac (14) ⚠️ | Thermes-Magnoac › Pays de Trie et du Magnoac | 7 |
| Forêt de Cantaous (15) ⚠️ | Cantaous › Neste Barousse | 7 |
| Forêt de Tibiran-Jaunac (17) ⚠️ | Tibiran-Jaunac › Neste Barousse | 7 |
| Forêt de Troubat (2) ⚠️ | Troubat › Neste Barousse | 7 |
| Forêt de Mauléon-Barousse ⚠️ | Cazarilh › Neste Barousse | 7 |
| Forêt de Siradan ⚠️ | Siradan › Neste Barousse | 7 |
| Forêt de Bareilles (29) ⚠️ | Bareilles › Aure Louron | 7 |
| Forêt de Germ (23) ⚠️ | Germ › Aure Louron | 7 |
| Forêt de Aragnouet (207) ⚠️ | Aragnouet › Aure Louron | 7 |
| Forêt de Séron (10) ⚠️ | Séron › Tarbes-Lourdes-Pyrénées | 7 |
| Forêt de Monfaucon (12) ⚠️ | Monfaucon › Adour-Madiran (Hautes-Pyrénées) | 7 |
| Bois de Boô-Silhen (51) ⚠️ | Boô-Silhen › Pyrénées Vallées des Gaves | 7 |
| Forêt de Lourdes (151) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 7 |
| Bois de Lourdes (128) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 7 |
| Forêt de Labassère (65) ⚠️ | Labassère › Haute-Bigorre | 7 |
| Forêt de Viella (21) ⚠️ | Betpouey › Pyrénées Vallées des Gaves | 7 |
| Forêt de Barèges (2) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 6 |
| Forêt de Lourdes ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 6 |
| Forêt de Marsac ⚠️ | Marsac › Adour-Madiran (Hautes-Pyrénées) | 6 |
| Forêt de Arrens-Marsous (3) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 6 |
| Forêt de Madiran (2) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 6 |
| Forêt de Bagnères-de-Bigorre (28) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 6 |
| Forêt de Arrens-Marsous (85) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 6 |
| Forêt de Gavarnie-Gèdre (71) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 6 |
| Forêt de Gavarnie-Gèdre (141) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 6 |
| Bois de Cauterets (13) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 6 |
| Forêt de Cauterets (462) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 6 |
| Forêt de Loucrup (8) ⚠️ | Loucrup › Tarbes-Lourdes-Pyrénées | 6 |
| Forêt de Tostat ⚠️ | Tostat › Adour-Madiran (Hautes-Pyrénées) | 6 |
| Forêt de Odos (13) ⚠️ | Odos › Tarbes-Lourdes-Pyrénées | 6 |
| Forêt de Capvern (19) ⚠️ | Capvern › Plateau de Lannemezan | 6 |
| Forêt de Capvern (23) ⚠️ | Capvern › Plateau de Lannemezan | 6 |
| Forêt de Capvern (26) ⚠️ | Capvern › Plateau de Lannemezan | 6 |
| Forêt de Capvern (105) ⚠️ | Capvern › Plateau de Lannemezan | 6 |
| Forêt de Capvern (111) ⚠️ | Capvern › Plateau de Lannemezan | 6 |
| Forêt de Peyraube (9) ⚠️ | Peyraube › Coteaux du Val-d'Arros | 6 |
| Forêt de Peyraube (13) ⚠️ | Peyraube › Coteaux du Val-d'Arros | 6 |
| Forêt de Tournous-Darré (3) ⚠️ | Tournous-Darré › Pays de Trie et du Magnoac | 6 |
| Forêt de Bugard (9) ⚠️ | Bugard › Pays de Trie et du Magnoac | 6 |
| Forêt de Burg (15) ⚠️ | Burg › Coteaux du Val-d'Arros | 6 |
| Forêt de Bégole (9) ⚠️ | Bégole › Coteaux du Val-d'Arros | 6 |
| Bois de Bégole (25) ⚠️ | Houeydets › Plateau de Lannemezan | 6 |
| Forêt de Libaros (2) ⚠️ | Libaros › Plateau de Lannemezan | 6 |
| Forêt de Bonrepos (21) ⚠️ | Bonrepos › Plateau de Lannemezan | 6 |
| Forêt de Galez (6) ⚠️ | Galez › Plateau de Lannemezan | 6 |
| Forêt de Saint-Laurent-de-Neste (8) ⚠️ | Saint-Laurent-de-Neste › Neste Barousse | 6 |
| Forêt de Saint-Laurent-de-Neste (12) ⚠️ | Saint-Laurent-de-Neste › Neste Barousse | 6 |
| Bois de Aventignan (5) ⚠️ | Aventignan › Neste Barousse | 6 |
| Forêt de Tibiran-Jaunac (3) ⚠️ | Tibiran-Jaunac › Neste Barousse | 6 |
| Forêt de Bizous (9) ⚠️ | Bizous › Neste Barousse | 6 |
| Forêt de Escala (3) ⚠️ | Escala › Plateau de Lannemezan | 6 |
| Forêt de La Barthe-de-Neste (5) ⚠️ | Izaux › Plateau de Lannemezan | 6 |
| Forêt de Izaux (3) ⚠️ | La Barthe-de-Neste › Plateau de Lannemezan | 6 |
| Forêt de Izaux (5) ⚠️ | Izaux › Plateau de Lannemezan | 6 |
| Forêt de Izaux (9) ⚠️ | Izaux › Plateau de Lannemezan | 6 |
| Forêt de Lortet (4) ⚠️ | Lortet › Plateau de Lannemezan | 6 |
| Forêt de Ilhet (3) ⚠️ | Ilhet › Aure Louron | 6 |
| Forêt de Bareilles (15) ⚠️ | Bareilles › Aure Louron | 6 |
| Forêt de Loudenvielle (52) ⚠️ | Loudenvielle › Aure Louron | 6 |
| Forêt de Aragnouet (169) ⚠️ | Aragnouet › Aure Louron | 6 |
| Forêt de Vignec (35) ⚠️ | Vignec › Aure Louron | 6 |
| Forêt de Cadeilhan-Trachère (27) ⚠️ | Cadeilhan-Trachère › Aure Louron | 6 |
| Forêt de Gez (7) ⚠️ | Gez › Pyrénées Vallées des Gaves | 6 |
| Forêt de Lourdes (138) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 6 |
| Forêt de Peyrouse (36) ⚠️ | Peyrouse › Tarbes-Lourdes-Pyrénées | 6 |
| Forêt de Oroix (7) ⚠️ | Oroix › Adour-Madiran (Hautes-Pyrénées) | 6 |
| Forêt de Arrens-Marsous (241) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 6 |
| Forêt de Ossen (5) ⚠️ | Ossen › Tarbes-Lourdes-Pyrénées | 6 |
| Forêt de Arrens-Marsous (248) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 6 |
| Forêt de Beaucens (53) ⚠️ | Beaucens › Pyrénées Vallées des Gaves | 6 |
| Forêt de Luquet (21) ⚠️ | Luquet › Tarbes-Lourdes-Pyrénées | 6 |
| Forêt de Trébons (47) ⚠️ | Trébons › Haute-Bigorre | 6 |
| Forêt de Saint-Pé-de-Bigorre (71) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 6 |
| Forêt de Louey (47) ⚠️ | Louey › Tarbes-Lourdes-Pyrénées | 6 |
| Forêt de Mascaras (26) ⚠️ | Mascaras › Coteaux du Val-d'Arros | 6 |
| Forêt de Bordes (68) ⚠️ | Bordes › Coteaux du Val-d'Arros | 6 |
| Forêt de Avezac-Prat-Lahitte (106) ⚠️ | Avezac-Prat-Lahitte › Plateau de Lannemezan | 6 |
| Forêt de Pouzac (77) ⚠️ | Pouzac › Haute-Bigorre | 6 |
| Forêt de Capvern (204) ⚠️ | Capvern › Plateau de Lannemezan | 6 |
| Forêt de Capvern (206) ⚠️ | Capvern › Plateau de Lannemezan | 6 |
| Forêt de Capvern (211) ⚠️ | Capvern › Plateau de Lannemezan | 6 |
| Forêt de Campan (316) ⚠️ | Campan › Haute-Bigorre | 6 |
| Forêt de Lustar (17) ⚠️ | Lustar › Pays de Trie et du Magnoac | 6 |
| Forêt de Bernadets-Dessus (10) ⚠️ | Bernadets-Dessus › Coteaux du Val-d'Arros | 6 |
| Forêt de Campistrous (26) ⚠️ | Campistrous › Plateau de Lannemezan | 6 |
| Forêt de Bonnefont (14) ⚠️ | Bonnefont › Pays de Trie et du Magnoac | 6 |
| Forêt de Montastruc (22) ⚠️ | Montastruc › Plateau de Lannemezan | 6 |
| Forêt de Sadournin (11) ⚠️ | Sadournin › Pays de Trie et du Magnoac | 6 |
| Forêt de Recurt (24) ⚠️ | Recurt › Plateau de Lannemezan | 6 |
| Forêt de Peyret-Saint-André (5) ⚠️ | Peyret-Saint-André › Pays de Trie et du Magnoac | 6 |
| Forêt de Mazères-de-Neste (11) ⚠️ | Mazères-de-Neste › Neste Barousse | 6 |
| Forêt de Nistos (21) ⚠️ | Nistos › Neste Barousse | 6 |
| Bois de Montsérié (23) ⚠️ | Montsérié › Plateau de Lannemezan | 6 |
| Forêt de Montoussé (8) ⚠️ | Montoussé › Plateau de Lannemezan | 6 |
| Forêt de Tarasteix (15) ⚠️ | Tarasteix › Adour-Madiran (Hautes-Pyrénées) | 6 |
| Forêt de Escaunets (12) ⚠️ | Escaunets › Adour-Madiran (Hautes-Pyrénées) | 6 |
| Forêt de Castelnau-Rivière-Basse (24) ⚠️ | Castelnau-Rivière-Basse › Adour-Madiran (Hautes-Pyrénées) | 6 |
| Forêt de Saint-Lanne (13) ⚠️ | Saint-Lanne › Adour-Madiran (Hautes-Pyrénées) | 6 |
| Forêt de Arrens-Marsous (262) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 6 |
| Bois de Montastruc (80) ⚠️ | Montastruc › Plateau de Lannemezan | 6 |
| Jardin Massey ⚠️ | Tarbes › Tarbes-Lourdes-Pyrénées | 5 |
| Forêt de Bartrès ⚠️ | Adé › Tarbes-Lourdes-Pyrénées | 5 |
| Forêt de Montégut ⚠️ | Montégut › Neste Barousse | 5 |
| Forêt de Madiran (4) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 5 |
| Forêt de Chis ⚠️ | Chis › Tarbes-Lourdes-Pyrénées | 5 |
| Bois de Ger ⚠️ | Geu › Tarbes-Lourdes-Pyrénées | 5 |
| Forêt de Beaucens (3) ⚠️ | Beaucens › Pyrénées Vallées des Gaves | 5 |
| Forêt de Lourdes (16) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 5 |
| Forêt de Arrens-Marsous (119) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 5 |
| Forêt de Estaing (75) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 5 |
| Forêt de Sers (2) ⚠️ | Sers › Pyrénées Vallées des Gaves | 5 |
| Forêt de Betpouey (5) ⚠️ | Betpouey › Pyrénées Vallées des Gaves | 5 |
| Forêt de Gardères (5) ⚠️ | Gardères › Tarbes-Lourdes-Pyrénées | 5 |
| Forêt de Cauterets (289) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 5 |
| Forêt de Cauterets (507) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 5 |
| Forêt de Campan (68) ⚠️ | Campan › Haute-Bigorre | 5 |
| Forêt de Campan (127) ⚠️ | Campan › Haute-Bigorre | 5 |
| Forêt de Campan (203) ⚠️ | Campan › Haute-Bigorre | 5 |
| Forêt de Bartrès (32) ⚠️ | Bartrès › Tarbes-Lourdes-Pyrénées | 5 |
| Forêt de Julos (2) ⚠️ | Julos › Tarbes-Lourdes-Pyrénées | 5 |
| Forêt de Escoubès-Pouts (4) ⚠️ | Escoubès-Pouts › Tarbes-Lourdes-Pyrénées | 5 |
| Forêt de Ossun (7) ⚠️ | Ossun › Tarbes-Lourdes-Pyrénées | 5 |
| Forêt de Louey (10) ⚠️ | Louey › Tarbes-Lourdes-Pyrénées | 5 |
| Forêt de Saint-Martin (17) ⚠️ | Saint-Martin › Tarbes-Lourdes-Pyrénées | 5 |
| Forêt de Marsac (4) ⚠️ | Marsac › Adour-Madiran (Hautes-Pyrénées) | 5 |
| Forêt de Aurensan (7) ⚠️ | Aurensan › Tarbes-Lourdes-Pyrénées | 5 |
| Forêt de Aurensan (17) ⚠️ | Aurensan › Tarbes-Lourdes-Pyrénées | 5 |
| Forêt de Sarniguet (5) ⚠️ | Sarniguet › Tarbes-Lourdes-Pyrénées | 5 |
| Forêt de Tostat (2) ⚠️ | Ugnouas › Adour-Madiran (Hautes-Pyrénées) | 5 |
| Forêt de Bernac-Debat (2) ⚠️ | Bernac-Debat › Tarbes-Lourdes-Pyrénées | 5 |
| Forêt de Bernac-Dessus (5) ⚠️ | Bernac-Dessus › Tarbes-Lourdes-Pyrénées | 5 |
| Forêt de Ordizan (36) ⚠️ | Ordizan › Haute-Bigorre | 5 |
| Forêt de Cieutat (45) ⚠️ | Cieutat › Haute-Bigorre | 5 |
| Forêt de Marsas (13) ⚠️ | Marsas › Haute-Bigorre | 5 |
| Forêt de Capvern (96) ⚠️ | Capvern › Plateau de Lannemezan | 5 |
| Forêt de Capvern (121) ⚠️ | Capvern › Plateau de Lannemezan | 5 |
| Forêt de Burg (4) ⚠️ | Burg › Coteaux du Val-d'Arros | 5 |
| Forêt de Bordes (56) ⚠️ | Bordes › Coteaux du Val-d'Arros | 5 |
| Forêt de Lacassagne (4) ⚠️ | Lacassagne › Adour-Madiran (Hautes-Pyrénées) | 5 |
| Forêt de Dours (3) ⚠️ | Dours › Coteaux du Val-d'Arros | 5 |
| Forêt de Sabalos (3) ⚠️ | Oléac-Debat › Coteaux du Val-d'Arros | 5 |
| Forêt de Souyeaux (13) ⚠️ | Souyeaux › Coteaux du Val-d'Arros | 5 |
| Forêt de Fontrailles (2) ⚠️ | Fontrailles › Pays de Trie et du Magnoac | 5 |
| Forêt de Bonrepos (12) ⚠️ | Bonrepos › Plateau de Lannemezan | 5 |
| Forêt de Galan (9) ⚠️ | Galan › Plateau de Lannemezan | 5 |
| Bois de Lassales (3) ⚠️ | Lassales › Pays de Trie et du Magnoac | 5 |
| Forêt de Réjaumont (8) ⚠️ | Réjaumont › Plateau de Lannemezan | 5 |
| Bois de Thermes-Magnoac (28) ⚠️ | Thermes-Magnoac › Pays de Trie et du Magnoac | 5 |
| Bois de Aventignan (4) ⚠️ | Aventignan › Neste Barousse | 5 |
| Forêt de Mazères-de-Neste (8) ⚠️ | Mazères-de-Neste › Neste Barousse | 5 |
| Forêt de Lombrès ⚠️ | Montégut › Neste Barousse | 5 |
| Forêt de Bize (8) ⚠️ | Bize › Neste Barousse | 5 |
| Forêt de Escala (5) ⚠️ | Escala › Plateau de Lannemezan | 5 |
| Forêt de Izaux (6) ⚠️ | Izaux › Plateau de Lannemezan | 5 |
| Bois de Sarrancolin (15) ⚠️ | Sarrancolin › Aure Louron | 5 |
| Forêt de Vielle-Louron (10) ⚠️ | Vielle-Louron › Aure Louron | 5 |
| Forêt de Azet (3) ⚠️ | Azet › Aure Louron | 5 |
| Forêt de Saint-Lary-Soulan (21) ⚠️ | Saint-Lary-Soulan › Aure Louron | 5 |
| Forêt de Saint-Lary-Soulan (62) ⚠️ | Saint-Lary-Soulan › Aure Louron | 5 |
| Forêt de Tramezaïgues (3) ⚠️ | Tramezaïgues › Aure Louron | 5 |
| Forêt de Saint-Lary-Soulan (95) ⚠️ | Saint-Lary-Soulan › Aure Louron | 5 |
| Forêt de Tramezaïgues (60) ⚠️ | Tramezaïgues › Aure Louron | 5 |
| Forêt de Tramezaïgues (65) ⚠️ | Tramezaïgues › Aure Louron | 5 |
| Forêt de Aragnouet (24) ⚠️ | Aragnouet › Aure Louron | 5 |
| Forêt de Vignec (4) ⚠️ | Vignec › Aure Louron | 5 |
| Forêt de Barèges (167) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 5 |
| Forêt de Gardères (17) ⚠️ | Gardères › Tarbes-Lourdes-Pyrénées | 5 |
| Bois de Nouilhan (9) ⚠️ | Nouilhan › Adour-Madiran (Hautes-Pyrénées) | 5 |
| Forêt de Lafitole (4) ⚠️ | Lafitole › Adour-Madiran (Hautes-Pyrénées) | 5 |
| Forêt de Sarriac-Bigorre (10) ⚠️ | Sarriac-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 5 |
| Forêt de Labatut-Rivière (2) ⚠️ | Labatut-Rivière › Adour-Madiran (Hautes-Pyrénées) | 5 |
| Forêt de Soublecause (4) ⚠️ | Hagedet › Adour-Madiran (Hautes-Pyrénées) | 5 |
| Bois de Estirac (15) ⚠️ | Estirac › Adour-Madiran (Hautes-Pyrénées) | 5 |
| Bois de Hères (8) ⚠️ | Hères › Adour-Madiran (Hautes-Pyrénées) | 5 |
| Forêt de Estaing (123) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 5 |
| Bois de Arcizans-Avant (19) ⚠️ | Arcizans-Avant › Pyrénées Vallées des Gaves | 5 |
| Forêt de Aucun (68) ⚠️ | Aucun › Pyrénées Vallées des Gaves | 5 |
| Forêt de Salles (22) ⚠️ | Salles › Pyrénées Vallées des Gaves | 5 |
| Forêt de Luquet (18) ⚠️ | Luquet › Tarbes-Lourdes-Pyrénées | 5 |
| Forêt de Gaillagos (87) ⚠️ | Gaillagos › Pyrénées Vallées des Gaves | 5 |
| Forêt de Lau-Balagnas (6) ⚠️ | Lau-Balagnas › Pyrénées Vallées des Gaves | 5 |
| Forêt de Agos-Vidalos ⚠️ | Agos-Vidalos › Pyrénées Vallées des Gaves | 5 |
| Bois de Geu (17) ⚠️ | Geu › Tarbes-Lourdes-Pyrénées | 5 |
| Forêt de Lau-Balagnas (7) ⚠️ | Lau-Balagnas › Pyrénées Vallées des Gaves | 5 |
| Forêt de Jarret (11) ⚠️ | Jarret › Tarbes-Lourdes-Pyrénées | 5 |
| Forêt de Estaing (128) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 5 |
| Forêt de Saint-Savin (23) ⚠️ | Saint-Savin › Pyrénées Vallées des Gaves | 5 |
| Forêt de Gavarnie-Gèdre (335) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 5 |
| Forêt de Cauterets (675) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 5 |
| Forêt de Bours (37) ⚠️ | Bours › Tarbes-Lourdes-Pyrénées | 5 |
| Forêt de Mérilheu (20) ⚠️ | Mérilheu › Haute-Bigorre | 5 |
| Forêt de Peyrouse (46) ⚠️ | Peyrouse › Tarbes-Lourdes-Pyrénées | 5 |
| Forêt de Poueyferré (67) ⚠️ | Poueyferré › Tarbes-Lourdes-Pyrénées | 5 |
| Forêt de Lamarque-Pontacq (48) ⚠️ | Lamarque-Pontacq › Tarbes-Lourdes-Pyrénées | 5 |
| Bois de Lamarque-Pontacq (2) ⚠️ | Lamarque-Pontacq › Tarbes-Lourdes-Pyrénées | 5 |
| Bois de Horgues (13) ⚠️ | Odos › Tarbes-Lourdes-Pyrénées | 5 |
| Forêt de Arcizac-Adour (31) ⚠️ | Arcizac-Adour › Tarbes-Lourdes-Pyrénées | 5 |
| Forêt de Avezac-Prat-Lahitte (112) ⚠️ | Avezac-Prat-Lahitte › Plateau de Lannemezan | 5 |
| Forêt de Bours (38) ⚠️ | Bours › Tarbes-Lourdes-Pyrénées | 5 |
| Forêt de Dours (5) ⚠️ | Dours › Coteaux du Val-d'Arros | 5 |
| Forêt de Burg (27) ⚠️ | Burg › Coteaux du Val-d'Arros | 5 |
| Bois de Montastruc (79) ⚠️ | Montastruc › Plateau de Lannemezan | 5 |
| Forêt de Castelbajac (12) ⚠️ | Castelbajac › Plateau de Lannemezan | 5 |
| Forêt de Bonrepos (23) ⚠️ | Bonrepos › Plateau de Lannemezan | 5 |
| Forêt de Clarens (20) ⚠️ | Clarens › Plateau de Lannemezan | 5 |
| Bois de Libaros (42) ⚠️ | Libaros › Plateau de Lannemezan | 5 |
| Forêt de Sabarros (7) ⚠️ | Sabarros › Plateau de Lannemezan | 5 |
| Bois de Saint-Laurent-de-Neste (103) ⚠️ | Saint-Laurent-de-Neste › Neste Barousse | 5 |
| Forêt de Tibiran-Jaunac (19) ⚠️ | Tibiran-Jaunac › Neste Barousse | 5 |
| Forêt de Tuzaguet (13) ⚠️ | Tuzaguet › Neste Barousse | 5 |
| Bois de Azet (52) ⚠️ | Azet › Aure Louron | 5 |
| Bois de Nouilhan (19) ⚠️ | Nouilhan › Adour-Madiran (Hautes-Pyrénées) | 5 |
| Forêt de Madiran (22) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 5 |
| Bois de Castelnau-Rivière-Basse (48) ⚠️ | Castelnau-Rivière-Basse › Adour-Madiran (Hautes-Pyrénées) | 5 |
| Forêt de Aspin-en-Lavedan (11) ⚠️ | Aspin-en-Lavedan › Tarbes-Lourdes-Pyrénées | 5 |
| Forêt de Saint-Pastous (14) ⚠️ | Saint-Pastous › Pyrénées Vallées des Gaves | 5 |
| Forêt de Ségus (5) ⚠️ | Ségus › Tarbes-Lourdes-Pyrénées | 5 |
| Bois de Poueyferré (21) ⚠️ | Poueyferré › Tarbes-Lourdes-Pyrénées | 5 |
| Bois de Astugue (25) ⚠️ | Astugue › Haute-Bigorre | 5 |
| Forêt de Salles (32) ⚠️ | Salles › Pyrénées Vallées des Gaves | 5 |
| Forêt de Gavarnie-Gèdre (339) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 5 |
| Forêt de Arrens-Marsous (4) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 4 |
| Forêt de Artagnan ⚠️ | Artagnan › Adour-Madiran (Hautes-Pyrénées) | 4 |
| Forêt de Juillan (3) ⚠️ | Juillan › Tarbes-Lourdes-Pyrénées | 4 |
| Forêt de Salles (8) ⚠️ | Salles › Pyrénées Vallées des Gaves | 4 |
| Forêt de Estaing (62) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 4 |
| Forêt de Estaing (79) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 4 |
| Bois de Lau-Balagnas (22) ⚠️ | Lau-Balagnas › Pyrénées Vallées des Gaves | 4 |
| Forêt de Artalens-Souin (11) ⚠️ | Artalens-Souin › Pyrénées Vallées des Gaves | 4 |
| Forêt de Villelongue (18) ⚠️ | Villelongue › Pyrénées Vallées des Gaves | 4 |
| Forêt de Pierrefitte-Nestalas (2) ⚠️ | Pierrefitte-Nestalas › Pyrénées Vallées des Gaves | 4 |
| Forêt de Sazos (35) ⚠️ | Sazos › Pyrénées Vallées des Gaves | 4 |
| Forêt de Viey (3) ⚠️ | Viey › Pyrénées Vallées des Gaves | 4 |
| Forêt de Vielle-Aure (23) ⚠️ | Vielle-Aure › Aure Louron | 4 |
| Bois de Barèges (7) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 4 |
| Forêt de Gavarnie-Gèdre (173) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 4 |
| Forêt de Cauterets (275) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 4 |
| Forêt de Cauterets (285) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 4 |
| Forêt de Cauterets (312) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 4 |
| Forêt de Cauterets (328) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 4 |
| Forêt de Cauterets (443) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 4 |
| Forêt de Cauterets (456) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 4 |
| Forêt de Cauterets (463) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 4 |
| Forêt de Arreau ⚠️ | Arreau › Aure Louron | 4 |
| Forêt de Labassère (2) ⚠️ | Labassère › Haute-Bigorre | 4 |
| Forêt de Labassère (23) ⚠️ | Labassère › Haute-Bigorre | 4 |
| Forêt de Asté (8) ⚠️ | Asté › Haute-Bigorre | 4 |
| Forêt de Campan (222) ⚠️ | Campan › Haute-Bigorre | 4 |
| Forêt de Montgaillard (20) ⚠️ | Montgaillard › Haute-Bigorre | 4 |
| Forêt de Montgaillard (23) ⚠️ | Ordizan › Haute-Bigorre | 4 |
| Forêt de Saint-Pé-de-Bigorre (28) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 4 |
| Forêt de Saint-Pé-de-Bigorre (47) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 4 |
| Forêt de Bartrès (16) ⚠️ | Bartrès › Tarbes-Lourdes-Pyrénées | 4 |
| Forêt de Lourdes (86) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 4 |
| Forêt de Orincles (3) ⚠️ | Orincles › Tarbes-Lourdes-Pyrénées | 4 |
| Forêt de Aurensan (6) ⚠️ | Aurensan › Tarbes-Lourdes-Pyrénées | 4 |
| Forêt de Bazillac (2) ⚠️ | Bazillac › Adour-Madiran (Hautes-Pyrénées) | 4 |
| Forêt de Pujo (9) ⚠️ | Pujo › Adour-Madiran (Hautes-Pyrénées) | 4 |
| Forêt de Aureilhan (4) ⚠️ | Aureilhan › Tarbes-Lourdes-Pyrénées | 4 |
| Forêt de Odos (6) ⚠️ | Odos › Tarbes-Lourdes-Pyrénées | 4 |
| Forêt de Salles-Adour ⚠️ | Salles-Adour › Tarbes-Lourdes-Pyrénées | 4 |
| Forêt de Odos (16) ⚠️ | Odos › Tarbes-Lourdes-Pyrénées | 4 |
| Forêt de Montgaillard (39) ⚠️ | Montgaillard › Haute-Bigorre | 4 |
| Forêt de Mascaras (17) ⚠️ | Mascaras › Coteaux du Val-d'Arros | 4 |
| Forêt de Uzer (15) ⚠️ | Uzer › Haute-Bigorre | 4 |
| Forêt de Marsas (16) ⚠️ | Marsas › Haute-Bigorre | 4 |
| Forêt de Bourg-de-Bigorre (17) ⚠️ | Bourg-de-Bigorre › Plateau de Lannemezan | 4 |
| Forêt de Benqué-Molère ⚠️ | Benqué-Molère › Plateau de Lannemezan | 4 |
| Forêt de Tilhouse (2) ⚠️ | Avezac-Prat-Lahitte › Plateau de Lannemezan | 4 |
| Forêt de Mauvezin (10) ⚠️ | Mauvezin › Plateau de Lannemezan | 4 |
| Forêt de Capvern (43) ⚠️ | Capvern › Plateau de Lannemezan | 4 |
| Forêt de Mauvezin (50) ⚠️ | Mauvezin › Plateau de Lannemezan | 4 |
| Forêt de Capvern (115) ⚠️ | Capvern › Plateau de Lannemezan | 4 |
| Forêt de Clarac (5) ⚠️ | Clarac › Coteaux du Val-d'Arros | 4 |
| Forêt de Moulédous (7) ⚠️ | Goudon › Coteaux du Val-d'Arros | 4 |
| Forêt de Bouilh-Péreuilh (11) ⚠️ | Bouilh-Péreuilh › Coteaux du Val-d'Arros | 4 |
| Forêt de Sénac (23) ⚠️ | Sénac › Adour-Madiran (Hautes-Pyrénées) | 4 |
| Forêt de Bouilh-Devant (2) ⚠️ | Bouilh-Devant › Adour-Madiran (Hautes-Pyrénées) | 4 |
| Forêt de Lacassagne (11) ⚠️ | Lacassagne › Adour-Madiran (Hautes-Pyrénées) | 4 |
| Forêt de Lescurry (8) ⚠️ | Lescurry › Adour-Madiran (Hautes-Pyrénées) | 4 |
| Bois de Escondeaux (6) ⚠️ | Lescurry › Adour-Madiran (Hautes-Pyrénées) | 4 |
| Forêt de Oléac-Debat (2) ⚠️ | Oléac-Debat › Coteaux du Val-d'Arros | 4 |
| Forêt de Aubarède (4) ⚠️ | Aubarède › Coteaux du Val-d'Arros | 4 |
| Forêt de Mun (6) ⚠️ | Mun › Coteaux du Val-d'Arros | 4 |
| Forêt de Estampures (6) ⚠️ | Estampures › Pays de Trie et du Magnoac | 4 |
| Forêt de Mazerolles (3) ⚠️ | Mazerolles › Pays de Trie et du Magnoac | 4 |
| Bois de Tournous-Darré (2) ⚠️ | Tournous-Darré › Pays de Trie et du Magnoac | 4 |
| Bois de Castelbajac ⚠️ | Castelbajac › Plateau de Lannemezan | 4 |
| Forêt de Houeydets (7) ⚠️ | Houeydets › Plateau de Lannemezan | 4 |
| Forêt de Houeydets (8) ⚠️ | Houeydets › Plateau de Lannemezan | 4 |
| Bois de Lagrange (9) ⚠️ | Lagrange › Plateau de Lannemezan | 4 |
| Forêt de Montastruc (13) ⚠️ | Montastruc › Plateau de Lannemezan | 4 |
| Forêt de Castelbajac (4) ⚠️ | Castelbajac › Plateau de Lannemezan | 4 |
| Forêt de Campistrous (18) ⚠️ | Campistrous › Plateau de Lannemezan | 4 |
| Parc du Guérissa ⚠️ | Lannemezan › Plateau de Lannemezan | 4 |
| Forêt de Pinas (3) ⚠️ | Pinas › Plateau de Lannemezan | 4 |
| Forêt de Lannemezan (59) ⚠️ | Lannemezan › Plateau de Lannemezan | 4 |
| Forêt de Clarens (13) ⚠️ | Clarens › Plateau de Lannemezan | 4 |
| Forêt de Puydarrieux (8) ⚠️ | Puydarrieux › Pays de Trie et du Magnoac | 4 |
| Forêt de Peyret-Saint-André ⚠️ | Peyret-Saint-André › Pays de Trie et du Magnoac | 4 |
| Forêt de Cizos (3) ⚠️ | Cizos › Pays de Trie et du Magnoac | 4 |
| Forêt de Uglas ⚠️ | Uglas › Plateau de Lannemezan | 4 |
| Bois de Gaussan (26) ⚠️ | Gaussan › Pays de Trie et du Magnoac | 4 |
| Forêt de Villemur ⚠️ | Villemur › Pays de Trie et du Magnoac | 4 |
| Forêt de Lalanne (2) ⚠️ | Lalanne › Pays de Trie et du Magnoac | 4 |
| Forêt de Pinas (6) ⚠️ | Pinas › Plateau de Lannemezan | 4 |
| Forêt de Cantaous (6) ⚠️ | Cantaous › Neste Barousse | 4 |
| Bois de Saint-Paul (27) ⚠️ | Saint-Paul › Neste Barousse | 4 |
| Bois de Saint-Arroman (3) ⚠️ | Saint-Arroman › Plateau de Lannemezan | 4 |
| Bois de Bazus-Neste (6) ⚠️ | Bazus-Neste › Plateau de Lannemezan | 4 |
| Forêt de Izaux (11) ⚠️ | Izaux › Plateau de Lannemezan | 4 |
| Forêt de Cazaux-Fréchet-Anéran-Camors (3) ⚠️ | Cazaux-Fréchet-Anéran-Camors › Aure Louron | 4 |
| Forêt de Cazaux-Fréchet-Anéran-Camors (14) ⚠️ | Cazaux-Fréchet-Anéran-Camors › Aure Louron | 4 |
| Forêt de Mont (24) ⚠️ | Mont › Aure Louron | 4 |
| Forêt de Loudenvielle (21) ⚠️ | Loudenvielle › Aure Louron | 4 |
| Forêt de Génos (30) ⚠️ | Génos › Aure Louron | 4 |
| Forêt de Loudenvielle (57) ⚠️ | Loudenvielle › Aure Louron | 4 |
| Forêt de Azet (49) ⚠️ | Azet › Aure Louron | 4 |
| Forêt de Saint-Lary-Soulan (102) ⚠️ | Saint-Lary-Soulan › Aure Louron | 4 |
| Forêt de Tramezaïgues (59) ⚠️ | Tramezaïgues › Aure Louron | 4 |
| Forêt de Tramezaïgues (61) ⚠️ | Tramezaïgues › Aure Louron | 4 |
| Forêt de Aragnouet (29) ⚠️ | Aragnouet › Aure Louron | 4 |
| Forêt de Aragnouet (35) ⚠️ | Aragnouet › Aure Louron | 4 |
| Forêt de Aragnouet (37) ⚠️ | Aragnouet › Aure Louron | 4 |
| Forêt de Aragnouet (133) ⚠️ | Aragnouet › Aure Louron | 4 |
| Forêt de Aragnouet (179) ⚠️ | Aragnouet › Aure Louron | 4 |
| Forêt de Vignec (32) ⚠️ | Vignec › Aure Louron | 4 |
| Forêt de Cadeilhan-Trachère (13) ⚠️ | Cadeilhan-Trachère › Aure Louron | 4 |
| Forêt de Sarriac-Bigorre (9) ⚠️ | Sarriac-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 4 |
| Forêt de Tarasteix (10) ⚠️ | Tarasteix › Adour-Madiran (Hautes-Pyrénées) | 4 |
| Forêt de Gardères (14) ⚠️ | Gardères › Tarbes-Lourdes-Pyrénées | 4 |
| Forêt de Vic-en-Bigorre (58) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 4 |
| Forêt de Lafitole ⚠️ | Lafitole › Adour-Madiran (Hautes-Pyrénées) | 4 |
| Bois de Sarriac-Bigorre (5) ⚠️ | Sarriac-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 4 |
| Forêt de Auriébat (3) ⚠️ | Auriébat › Adour-Madiran (Hautes-Pyrénées) | 4 |
| Forêt de Auriébat (12) ⚠️ | Auriébat › Adour-Madiran (Hautes-Pyrénées) | 4 |
| Bois de Estirac (13) ⚠️ | Estirac › Adour-Madiran (Hautes-Pyrénées) | 4 |
| Forêt de Castelnau-Rivière-Basse (3) ⚠️ | Castelnau-Rivière-Basse › Adour-Madiran (Hautes-Pyrénées) | 4 |
| Forêt de Castelnau-Rivière-Basse (7) ⚠️ | Castelnau-Rivière-Basse › Adour-Madiran (Hautes-Pyrénées) | 4 |
| Forêt de Saint-Pastous (9) ⚠️ | Saint-Pastous › Pyrénées Vallées des Gaves | 4 |
| Forêt de Cauterets (663) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 4 |
| Forêt de Cauterets (664) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 4 |
| Forêt de Ibos (100) ⚠️ | Ibos › Tarbes-Lourdes-Pyrénées | 4 |
| Forêt de Aspin-en-Lavedan (9) ⚠️ | Aspin-en-Lavedan › Tarbes-Lourdes-Pyrénées | 4 |
| Forêt de Siarrouy (25) ⚠️ | Siarrouy › Adour-Madiran (Hautes-Pyrénées) | 4 |
| Forêt de Vidouze (14) ⚠️ | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 4 |
| Forêt de Vidouze (15) ⚠️ | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 4 |
| Forêt de Préchac (9) ⚠️ | Préchac › Pyrénées Vallées des Gaves | 4 |
| Bois de Boô-Silhen (50) ⚠️ | Boô-Silhen › Pyrénées Vallées des Gaves | 4 |
| Forêt de Bagnères-de-Bigorre (229) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 4 |
| Forêt de Lourdes (145) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 4 |
| Forêt de Arrens-Marsous (249) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 4 |
| Forêt de Sers (83) ⚠️ | Sers › Pyrénées Vallées des Gaves | 4 |
| Forêt de Hauban (15) ⚠️ | Hauban › Haute-Bigorre | 4 |
| Forêt de Mérilheu (19) ⚠️ | Mérilheu › Haute-Bigorre | 4 |
| Forêt de Campan (306) ⚠️ | Campan › Haute-Bigorre | 4 |
| Forêt de Astugue (68) ⚠️ | Astugue › Haute-Bigorre | 4 |
| Forêt de Bartrès (56) ⚠️ | Bartrès › Tarbes-Lourdes-Pyrénées | 4 |
| Forêt de Loubajac (38) ⚠️ | Loubajac › Tarbes-Lourdes-Pyrénées | 4 |
| Forêt de Louey (46) ⚠️ | Louey › Tarbes-Lourdes-Pyrénées | 4 |
| Forêt de Andrest (37) ⚠️ | Andrest › Adour-Madiran (Hautes-Pyrénées) | 4 |
| Forêt de Allier (10) ⚠️ | Allier › Tarbes-Lourdes-Pyrénées | 4 |
| Bois de Momères (9) ⚠️ | Momères › Tarbes-Lourdes-Pyrénées | 4 |
| Bois de Horgues (14) ⚠️ | Odos › Tarbes-Lourdes-Pyrénées | 4 |
| Forêt de Mascaras (25) ⚠️ | Mascaras › Coteaux du Val-d'Arros | 4 |
| Forêt de Bordes (66) ⚠️ | Bordes › Coteaux du Val-d'Arros | 4 |
| Forêt de Bourg-de-Bigorre (61) ⚠️ | Bourg-de-Bigorre › Plateau de Lannemezan | 4 |
| Forêt de Capvern (208) ⚠️ | Capvern › Plateau de Lannemezan | 4 |
| Forêt de Capvern (212) ⚠️ | Capvern › Plateau de Lannemezan | 4 |
| Bois de Tournay (3) ⚠️ | Tournay › Coteaux du Val-d'Arros | 4 |
| Forêt de Marquerie (5) ⚠️ | Marquerie › Coteaux du Val-d'Arros | 4 |
| Forêt de Lacassagne (13) ⚠️ | Lacassagne › Adour-Madiran (Hautes-Pyrénées) | 4 |
| Forêt de Estampures (13) ⚠️ | Estampures › Pays de Trie et du Magnoac | 4 |
| Forêt de Bernadets-Dessus (11) ⚠️ | Bernadets-Dessus › Coteaux du Val-d'Arros | 4 |
| Forêt de Campistrous (27) ⚠️ | Campistrous › Plateau de Lannemezan | 4 |
| Forêt de Montastruc (23) ⚠️ | Montastruc › Plateau de Lannemezan | 4 |
| Forêt de Lannemezan (68) ⚠️ | Lannemezan › Plateau de Lannemezan | 4 |
| Forêt de Lannemezan (69) ⚠️ | Lannemezan › Plateau de Lannemezan | 4 |
| Forêt de Sadournin (9) ⚠️ | Sadournin › Pays de Trie et du Magnoac | 4 |
| Forêt de Castelnau-Magnoac (11) ⚠️ | Castelnau-Magnoac › Pays de Trie et du Magnoac | 4 |
| Forêt de Uglas (13) ⚠️ | Uglas › Plateau de Lannemezan | 4 |
| Bois de Saléchan (34) ⚠️ | Saléchan › Neste Barousse | 4 |
| Bois de Escala (39) ⚠️ | Escala › Plateau de Lannemezan | 4 |
| Forêt de La Barthe-de-Neste (18) ⚠️ | La Barthe-de-Neste › Plateau de Lannemezan | 4 |
| Bois de Ilhet (59) ⚠️ | Ilhet › Aure Louron | 4 |
| Forêt de Loudenvielle (76) ⚠️ | Loudenvielle › Aure Louron | 4 |
| Forêt de Séron (11) ⚠️ | Séron › Tarbes-Lourdes-Pyrénées | 4 |
| Bois de Caixon (27) ⚠️ | Caixon › Adour-Madiran (Hautes-Pyrénées) | 4 |
| Forêt de Artagnan (21) ⚠️ | Artagnan › Adour-Madiran (Hautes-Pyrénées) | 4 |
| Forêt de Soublecause (9) ⚠️ | Soublecause › Adour-Madiran (Hautes-Pyrénées) | 4 |
| Forêt de Madiran (25) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 4 |
| Bois de Hères (30) ⚠️ | Hères › Adour-Madiran (Hautes-Pyrénées) | 4 |
| Bois de Hères (31) ⚠️ | Hères › Adour-Madiran (Hautes-Pyrénées) | 4 |
| Bois de Horgues (15) ⚠️ | Salles-Adour › Tarbes-Lourdes-Pyrénées | 4 |
| Forêt de Chèze (16) ⚠️ | Chèze › Pyrénées Vallées des Gaves | 4 |
| Forêt de Arras-en-Lavedan (89) ⚠️ | Arras-en-Lavedan › Pyrénées Vallées des Gaves | 4 |
| Forêt de Aucun (76) ⚠️ | Aucun › Pyrénées Vallées des Gaves | 4 |
| Bois de Agos-Vidalos (64) ⚠️ | Boô-Silhen › Pyrénées Vallées des Gaves | 4 |
| Bois de Ger (19) ⚠️ | Ger › Tarbes-Lourdes-Pyrénées | 4 |
| Bois de Saint-Pé-de-Bigorre (53) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 4 |
| Bois de Juncalas (44) ⚠️ | Juncalas › Tarbes-Lourdes-Pyrénées | 4 |
| Forêt de Sers (89) ⚠️ | Sers › Pyrénées Vallées des Gaves | 4 |
| Bois de Arcizac-Adour (36) ⚠️ | Arcizac-Adour › Tarbes-Lourdes-Pyrénées | 4 |
| Forêt de Cheust ⚠️ | Cheust › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Sazos ⚠️ | Sazos › Pyrénées Vallées des Gaves | 3 |
| Forêt de Gardères ⚠️ | Gardères › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Lourdes (4) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Vic-en-Bigorre (3) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Oursbelille (3) ⚠️ | Oursbelille › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Ouzous ⚠️ | Ouzous › Pyrénées Vallées des Gaves | 3 |
| Forêt de Barèges (6) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 3 |
| Bois de Lau-Balagnas (9) ⚠️ | Préchac › Pyrénées Vallées des Gaves | 3 |
| Bois de Ségus (5) ⚠️ | Ségus › Tarbes-Lourdes-Pyrénées | 3 |
| Bois de Ségus (19) ⚠️ | Ségus › Tarbes-Lourdes-Pyrénées | 3 |
| Bois de Ossen (20) ⚠️ | Ossen › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Bagnères-de-Bigorre (25) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 3 |
| Forêt des Angles ⚠️ | Les Angles › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Artalens-Souin (9) ⚠️ | Artalens-Souin › Pyrénées Vallées des Gaves | 3 |
| Forêt de Betpouey (9) ⚠️ | Betpouey › Pyrénées Vallées des Gaves | 3 |
| Forêt de Sers (14) ⚠️ | Sers › Pyrénées Vallées des Gaves | 3 |
| Forêt de Sers (51) ⚠️ | Sers › Pyrénées Vallées des Gaves | 3 |
| Forêt de Barèges (29) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 3 |
| Forêt de Aragnouet ⚠️ | Aragnouet › Aure Louron | 3 |
| Forêt de Gavarnie-Gèdre (19) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 3 |
| Forêt de Gavarnie-Gèdre (91) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 3 |
| Forêt de Cauterets (36) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 3 |
| Forêt de Cauterets (124) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 3 |
| Forêt de Cauterets (144) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 3 |
| Forêt de Cauterets (276) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 3 |
| Forêt de Cauterets (300) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 3 |
| Forêt de Cauterets (323) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 3 |
| Forêt de Cauterets (371) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 3 |
| Forêt de Cauterets (372) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 3 |
| Forêt de Cauterets (373) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 3 |
| Forêt de Cauterets (403) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 3 |
| Forêt de Cauterets (464) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 3 |
| Forêt de Cauterets (500) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 3 |
| Forêt de Sazos (36) ⚠️ | Sazos › Pyrénées Vallées des Gaves | 3 |
| Forêt de Ferrières (17) ⚠️ | Ferrières › Pays de Nay (Hautes-Pyrénées) | 3 |
| Bois de Oursbelille (4) ⚠️ | Oursbelille › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Bazet (7) ⚠️ | Bazet › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Labassère (6) ⚠️ | Labassère › Haute-Bigorre | 3 |
| Forêt de Labassère (18) ⚠️ | Labassère › Haute-Bigorre | 3 |
| Forêt de Labassère (40) ⚠️ | Labassère › Haute-Bigorre | 3 |
| Forêt de Bagnères-de-Bigorre (40) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 3 |
| Forêt de Pouzac (53) ⚠️ | Pouzac › Haute-Bigorre | 3 |
| Forêt de Argelès-Bagnères ⚠️ | Argelès-Bagnères › Haute-Bigorre | 3 |
| Forêt de Campan (228) ⚠️ | Campan › Haute-Bigorre | 3 |
| Forêt de Ancizan (15) ⚠️ | Ancizan › Aure Louron | 3 |
| Forêt de Aspin-Aure (4) ⚠️ | Aspin-Aure › Aure Louron | 3 |
| Forêt de Montgaillard (7) ⚠️ | Montgaillard › Haute-Bigorre | 3 |
| Forêt de Montgaillard (9) ⚠️ | Montgaillard › Haute-Bigorre | 3 |
| Forêt de Gez-ez-Angles (5) ⚠️ | Gez-ez-Angles › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Arcizac-ez-Angles (5) ⚠️ | Arcizac-ez-Angles › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Saint-Pé-de-Bigorre (41) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Saint-Pé-de-Bigorre (49) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Peyrouse (25) ⚠️ | Peyrouse › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Paréac (4) ⚠️ | Paréac › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Julos (34) ⚠️ | Julos › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Adé (13) ⚠️ | Adé › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Bénac ⚠️ | Bénac › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Ossun (32) ⚠️ | Ossun › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Ossun (33) ⚠️ | Ossun › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Lanne (12) ⚠️ | Lanne › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Ibos (47) ⚠️ | Ibos › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Andrest (20) ⚠️ | Andrest › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Bours (23) ⚠️ | Bours › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Camalès (5) ⚠️ | Bazillac › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Camalès (10) ⚠️ | Camalès › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Vic-en-Bigorre (16) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Odos (5) ⚠️ | Odos › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Salles-Adour (2) ⚠️ | Salles-Adour › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Salles-Adour (4) ⚠️ | Salles-Adour › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Montgaillard (29) ⚠️ | Montgaillard › Haute-Bigorre | 3 |
| Forêt de Bernac-Dessus (8) ⚠️ | Bernac-Dessus › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Antist (5) ⚠️ | Antist › Haute-Bigorre | 3 |
| Forêt de Hauban (2) ⚠️ | Hauban › Haute-Bigorre | 3 |
| Forêt de Mascaras (14) ⚠️ | Mascaras › Coteaux du Val-d'Arros | 3 |
| Forêt de Bordes (6) ⚠️ | Bordes › Coteaux du Val-d'Arros | 3 |
| Forêt de Tournay (3) ⚠️ | Tournay › Coteaux du Val-d'Arros | 3 |
| Forêt de Uzer (5) ⚠️ | Uzer › Haute-Bigorre | 3 |
| Forêt de Bourg-de-Bigorre (4) ⚠️ | Bourg-de-Bigorre › Plateau de Lannemezan | 3 |
| Forêt de Laborde (3) ⚠️ | Laborde › Plateau de Lannemezan | 3 |
| Forêt de Lomné (9) ⚠️ | Lomné › Plateau de Lannemezan | 3 |
| Forêt de Esparros (23) ⚠️ | Esparros › Plateau de Lannemezan | 3 |
| Forêt de Labastide (8) ⚠️ | Labastide › Plateau de Lannemezan | 3 |
| Forêt de Capvern ⚠️ | Capvern › Plateau de Lannemezan | 3 |
| Forêt de Avezac-Prat-Lahitte (33) ⚠️ | Avezac-Prat-Lahitte › Plateau de Lannemezan | 3 |
| Forêt de Avezac-Prat-Lahitte (53) ⚠️ | Avezac-Prat-Lahitte › Plateau de Lannemezan | 3 |
| Forêt de Péré (3) ⚠️ | Péré › Plateau de Lannemezan | 3 |
| Forêt de Monfaucon ⚠️ | Monfaucon › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Capvern (129) ⚠️ | Capvern › Plateau de Lannemezan | 3 |
| Forêt de Péré (20) ⚠️ | Péré › Plateau de Lannemezan | 3 |
| Forêt de Bégole (2) ⚠️ | Péré › Plateau de Lannemezan | 3 |
| Forêt de Tournay (43) ⚠️ | Tournay › Coteaux du Val-d'Arros | 3 |
| Forêt de Bordes (65) ⚠️ | Lhez › Coteaux du Val-d'Arros | 3 |
| Forêt de Clarac (32) ⚠️ | Clarac › Coteaux du Val-d'Arros | 3 |
| Forêt de Coussan (4) ⚠️ | Coussan › Coteaux du Val-d'Arros | 3 |
| Forêt de Castelvieilh (2) ⚠️ | Castelvieilh › Coteaux du Val-d'Arros | 3 |
| Forêt de Castelvieilh (11) ⚠️ | Castelvieilh › Coteaux du Val-d'Arros | 3 |
| Forêt de Bouilh-Péreuilh (2) ⚠️ | Bouilh-Péreuilh › Coteaux du Val-d'Arros | 3 |
| Bois de Jacque (6) ⚠️ | Jacque › Coteaux du Val-d'Arros | 3 |
| Bois de Peyrun ⚠️ | Peyrun › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Sénac (20) ⚠️ | Sénac › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Sénac (25) ⚠️ | Sénac › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Bois de Lescurry (9) ⚠️ | Lescurry › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Dours (2) ⚠️ | Dours › Coteaux du Val-d'Arros | 3 |
| Forêt de Pouyastruc (10) ⚠️ | Pouyastruc › Coteaux du Val-d'Arros | 3 |
| Forêt de Lizos ⚠️ | Lizos › Coteaux du Val-d'Arros | 3 |
| Bois de Pouyastruc (27) ⚠️ | Pouyastruc › Coteaux du Val-d'Arros | 3 |
| Forêt de Lansac (4) ⚠️ | Lansac › Coteaux du Val-d'Arros | 3 |
| Forêt de Osmets ⚠️ | Osmets › Pays de Trie et du Magnoac | 3 |
| Forêt de Trouley-Labarthe (5) ⚠️ | Trouley-Labarthe › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Bouilh-Devant (12) ⚠️ | Bouilh-Devant › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Estampures (4) ⚠️ | Estampures › Pays de Trie et du Magnoac | 3 |
| Forêt de Bernadets-Debat ⚠️ | Bernadets-Debat › Pays de Trie et du Magnoac | 3 |
| Forêt de Trie-sur-Baïse (2) ⚠️ | Trie-sur-Baïse › Pays de Trie et du Magnoac | 3 |
| Bois de Trie-sur-Baïse (16) ⚠️ | Trie-sur-Baïse › Pays de Trie et du Magnoac | 3 |
| Forêt de Bazus-Aure ⚠️ | Bazus-Aure › Aure Louron | 3 |
| Bois de Tournous-Darré ⚠️ | Tournous-Darré › Pays de Trie et du Magnoac | 3 |
| Bois de Bernadets-Dessus (2) ⚠️ | Bernadets-Dessus › Coteaux du Val-d'Arros | 3 |
| Forêt de Burg (12) ⚠️ | Burg › Coteaux du Val-d'Arros | 3 |
| Forêt de Castelbajac ⚠️ | Castelbajac › Plateau de Lannemezan | 3 |
| Forêt de Bégole (12) ⚠️ | Bégole › Coteaux du Val-d'Arros | 3 |
| Forêt de Lannemezan (9) ⚠️ | Lannemezan › Plateau de Lannemezan | 3 |
| Forêt de Campistrous (8) ⚠️ | Campistrous › Plateau de Lannemezan | 3 |
| Forêt de Galan ⚠️ | Galan › Plateau de Lannemezan | 3 |
| Forêt de Castelbajac (6) ⚠️ | Castelbajac › Plateau de Lannemezan | 3 |
| Forêt de Capvern (199) ⚠️ | Capvern › Plateau de Lannemezan | 3 |
| Forêt de Lannemezan (41) ⚠️ | Lannemezan › Plateau de Lannemezan | 3 |
| Forêt de Lannemezan (57) ⚠️ | Lannemezan › Plateau de Lannemezan | 3 |
| Forêt de Clarens (10) ⚠️ | Clarens › Plateau de Lannemezan | 3 |
| Forêt de Galan (10) ⚠️ | Galan › Plateau de Lannemezan | 3 |
| Forêt de Libaros (7) ⚠️ | Libaros › Plateau de Lannemezan | 3 |
| Bois de Puntous (7) ⚠️ | Larroque › Pays de Trie et du Magnoac | 3 |
| Forêt de Recurt (15) ⚠️ | Recurt › Plateau de Lannemezan | 3 |
| Bois de Castelnau-Magnoac (60) ⚠️ | Castelnau-Magnoac › Pays de Trie et du Magnoac | 3 |
| Forêt de Cizos (4) ⚠️ | Cizos › Pays de Trie et du Magnoac | 3 |
| Bois de Tajan (8) ⚠️ | Tajan › Plateau de Lannemezan | 3 |
| Bois de Arné (2) ⚠️ | Arné › Plateau de Lannemezan | 3 |
| Forêt de Monléon-Magnoac (6) ⚠️ | Monléon-Magnoac › Pays de Trie et du Magnoac | 3 |
| Forêt de Monléon-Magnoac (7) ⚠️ | Monléon-Magnoac › Pays de Trie et du Magnoac | 3 |
| Forêt de Monléon-Magnoac (11) ⚠️ | Monléon-Magnoac › Pays de Trie et du Magnoac | 3 |
| Bois de Aries-Espénan (15) ⚠️ | Aries-Espénan › Pays de Trie et du Magnoac | 3 |
| Bois de Aries-Espénan (22) ⚠️ | Aries-Espénan › Pays de Trie et du Magnoac | 3 |
| Bois de Sariac-Magnoac (6) ⚠️ | Sariac-Magnoac › Pays de Trie et du Magnoac | 3 |
| Forêt de Arné (6) ⚠️ | Arné › Plateau de Lannemezan | 3 |
| Forêt de Thermes-Magnoac (8) ⚠️ | Thermes-Magnoac › Pays de Trie et du Magnoac | 3 |
| Forêt de Bazordan (3) ⚠️ | Bazordan › Pays de Trie et du Magnoac | 3 |
| Forêt de Bazordan (10) ⚠️ | Bazordan › Pays de Trie et du Magnoac | 3 |
| Forêt de Pinas (7) ⚠️ | Pinas › Plateau de Lannemezan | 3 |
| Bois de Cantaous (25) ⚠️ | Cantaous › Neste Barousse | 3 |
| Forêt de Saint-Laurent-de-Neste (7) ⚠️ | Saint-Laurent-de-Neste › Neste Barousse | 3 |
| Forêt de Cantaous (12) ⚠️ | Cantaous › Neste Barousse | 3 |
| Forêt de Saint-Laurent-de-Neste (15) ⚠️ | Saint-Laurent-de-Neste › Neste Barousse | 3 |
| Bois de Saint-Paul (43) ⚠️ | Aventignan › Neste Barousse | 3 |
| Forêt de Saint-Paul (19) ⚠️ | Mazères-de-Neste › Neste Barousse | 3 |
| Forêt de Tibiran-Jaunac (16) ⚠️ | Tibiran-Jaunac › Neste Barousse | 3 |
| Bois de Saléchan (6) ⚠️ | Saléchan › Neste Barousse | 3 |
| Bois de Nestier (7) ⚠️ | Nestier › Neste Barousse | 3 |
| Forêt de Nistos (14) ⚠️ | Nistos › Neste Barousse | 3 |
| Bois de Anères (11) ⚠️ | Anères › Neste Barousse | 3 |
| Forêt de Bizous (4) ⚠️ | Bizous › Neste Barousse | 3 |
| Forêt de Escala (4) ⚠️ | Escala › Plateau de Lannemezan | 3 |
| Bois de Aspin-Aure (3) ⚠️ | Aspin-Aure › Aure Louron | 3 |
| Bois de Jézeau (7) ⚠️ | Jézeau › Aure Louron | 3 |
| Forêt de Cazaux-Debat (2) ⚠️ | Cazaux-Debat › Aure Louron | 3 |
| Forêt de Azet (5) ⚠️ | Azet › Aure Louron | 3 |
| Forêt de Loudenvielle (30) ⚠️ | Loudenvielle › Aure Louron | 3 |
| Forêt de Loudenvielle (37) ⚠️ | Loudenvielle › Aure Louron | 3 |
| Forêt de Lançon (2) ⚠️ | Lançon › Aure Louron | 3 |
| Bois de Aulon (9) ⚠️ | Aulon › Aure Louron | 3 |
| Forêt de Guchan ⚠️ | Guchan › Aure Louron | 3 |
| Forêt de Azet (42) ⚠️ | Azet › Aure Louron | 3 |
| Forêt de Saint-Lary-Soulan (70) ⚠️ | Saint-Lary-Soulan › Aure Louron | 3 |
| Forêt de Saint-Lary-Soulan (96) ⚠️ | Saint-Lary-Soulan › Aure Louron | 3 |
| Forêt de Saint-Lary-Soulan (100) ⚠️ | Saint-Lary-Soulan › Aure Louron | 3 |
| Forêt de Tramezaïgues (66) ⚠️ | Tramezaïgues › Aure Louron | 3 |
| Forêt de Tramezaïgues (67) ⚠️ | Tramezaïgues › Aure Louron | 3 |
| Forêt de Aragnouet (26) ⚠️ | Aragnouet › Aure Louron | 3 |
| Forêt de Aragnouet (70) ⚠️ | Aragnouet › Aure Louron | 3 |
| Forêt de Aragnouet (75) ⚠️ | Aragnouet › Aure Louron | 3 |
| Forêt de Aragnouet (85) ⚠️ | Aragnouet › Aure Louron | 3 |
| Forêt de Aragnouet (86) ⚠️ | Aragnouet › Aure Louron | 3 |
| Forêt de Aragnouet (93) ⚠️ | Aragnouet › Aure Louron | 3 |
| Forêt de Aragnouet (95) ⚠️ | Aragnouet › Aure Louron | 3 |
| Forêt de Aragnouet (152) ⚠️ | Aragnouet › Aure Louron | 3 |
| Forêt de Saint-Lary-Soulan (145) ⚠️ | Saint-Lary-Soulan › Aure Louron | 3 |
| Forêt de Saint-Pé-de-Bigorre (63) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Barèges (182) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 3 |
| Forêt de Liac (3) ⚠️ | Liac › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Bois de Sauveterre ⚠️ | Sauveterre › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Bois de Gardères (6) ⚠️ | Gardères › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Séron ⚠️ | Séron › Tarbes-Lourdes-Pyrénées | 3 |
| Bois de Escaunets (13) ⚠️ | Escaunets › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Bois de Vic-en-Bigorre (55) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Bois de Larreule (6) ⚠️ | Larreule › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Artagnan (6) ⚠️ | Artagnan › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Artagnan (15) ⚠️ | Artagnan › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Lafitole (3) ⚠️ | Lafitole › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Maubourguet (4) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Monfaucon (8) ⚠️ | Monfaucon › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Monfaucon (9) ⚠️ | Monfaucon › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Auriébat (2) ⚠️ | Auriébat › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Lafitole (7) ⚠️ | Lafitole › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Lafitole (10) ⚠️ | Lafitole › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Bois de Maubourguet (67) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Maubourguet (9) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Bois de Maubourguet (98) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Bois de Vidouze (8) ⚠️ | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Bois de Vidouze (14) ⚠️ | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Vidouze (5) ⚠️ | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Vidouze (8) ⚠️ | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Labatut-Rivière (7) ⚠️ | Labatut-Rivière › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Madiran (9) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Madiran (12) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Bois de Saint-Lanne (10) ⚠️ | Saint-Lanne › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Gaillagos (84) ⚠️ | Gaillagos › Pyrénées Vallées des Gaves | 3 |
| Forêt de Arrens-Marsous (232) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 3 |
| Bois de Lourdes (56) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Bartrès (48) ⚠️ | Bartrès › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Lourdes (141) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Cauterets (667) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 3 |
| Parc de Cauterets ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 3 |
| Bois de Sers (27) ⚠️ | Sers › Pyrénées Vallées des Gaves | 3 |
| Forêt de Saint-Lary-Soulan (198) ⚠️ | Saint-Lary-Soulan › Aure Louron | 3 |
| Forêt de Vielle-Adour (26) ⚠️ | Vielle-Adour › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Aulon (4) ⚠️ | Aulon › Aure Louron | 3 |
| Forêt de Ossun-ez-Angles (12) ⚠️ | Ossun-ez-Angles › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Hiis (20) ⚠️ | Hiis › Haute-Bigorre | 3 |
| Bois de Vieuzos (23) ⚠️ | Vieuzos › Pays de Trie et du Magnoac | 3 |
| Forêt de Bizous (10) ⚠️ | Bizous › Neste Barousse | 3 |
| Forêt de Tarasteix (12) ⚠️ | Tarasteix › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Villenave-près-Béarn ⚠️ | Villenave-près-Béarn › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Arras-en-Lavedan (79) ⚠️ | Arras-en-Lavedan › Pyrénées Vallées des Gaves | 3 |
| Forêt de Saint-Pastous (11) ⚠️ | Saint-Pastous › Pyrénées Vallées des Gaves | 3 |
| Forêt de Gazost (41) ⚠️ | Gazost › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Gazost (43) ⚠️ | Gazost › Tarbes-Lourdes-Pyrénées | 3 |
| Bois de Gazost (60) ⚠️ | Gazost › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt des Angles (14) ⚠️ | Les Angles › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Gaillagos (89) ⚠️ | Gaillagos › Pyrénées Vallées des Gaves | 3 |
| Forêt de Arras-en-Lavedan (88) ⚠️ | Arras-en-Lavedan › Pyrénées Vallées des Gaves | 3 |
| Forêt de Sers (82) ⚠️ | Sers › Pyrénées Vallées des Gaves | 3 |
| Forêt de Sers (87) ⚠️ | Sers › Pyrénées Vallées des Gaves | 3 |
| Forêt de Luquet (20) ⚠️ | Luquet › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Gavarnie-Gèdre (332) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 3 |
| Forêt de Cauterets (680) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 3 |
| Bois de Oursbelille (17) ⚠️ | Oursbelille › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Bours (35) ⚠️ | Bours › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Campan (310) ⚠️ | Campan › Haute-Bigorre | 3 |
| Forêt de Arrayou-Lahitte (41) ⚠️ | Arrayou-Lahitte › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Peyrouse (43) ⚠️ | Peyrouse › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Peyrouse (47) ⚠️ | Peyrouse › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Poueyferré (63) ⚠️ | Poueyferré › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Lourdes (149) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Gez-ez-Angles (28) ⚠️ | Arcizac-ez-Angles › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Julos (55) ⚠️ | Julos › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Lamarque-Pontacq (49) ⚠️ | Lamarque-Pontacq › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Ossun (63) ⚠️ | Ossun › Tarbes-Lourdes-Pyrénées | 3 |
| Bois de Vic-en-Bigorre (73) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Momères (9) ⚠️ | Momères › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Bernac-Dessus (27) ⚠️ | Bernac-Dessus › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Poumarous (20) ⚠️ | Poumarous › Coteaux du Val-d'Arros | 3 |
| Forêt de Poumarous (22) ⚠️ | Poumarous › Coteaux du Val-d'Arros | 3 |
| Forêt de Labastide (47) ⚠️ | Labastide › Plateau de Lannemezan | 3 |
| Forêt de Avezac-Prat-Lahitte (113) ⚠️ | Avezac-Prat-Lahitte › Plateau de Lannemezan | 3 |
| Forêt de Capvern (207) ⚠️ | Capvern › Plateau de Lannemezan | 3 |
| Forêt de Clarens (18) ⚠️ | Clarens › Plateau de Lannemezan | 3 |
| Forêt de Clarens (19) ⚠️ | Clarens › Plateau de Lannemezan | 3 |
| Bois de Clarens (81) ⚠️ | Clarens › Plateau de Lannemezan | 3 |
| Bois de Bonrepos (48) ⚠️ | Bonrepos › Plateau de Lannemezan | 3 |
| Bois de Galan (112) ⚠️ | Galan › Plateau de Lannemezan | 3 |
| Parc de Castelnau-Magnoac (2) ⚠️ | Castelnau-Magnoac › Pays de Trie et du Magnoac | 3 |
| Forêt de Monléon-Magnoac (19) ⚠️ | Monléon-Magnoac › Pays de Trie et du Magnoac | 3 |
| Bois de Hèches (98) ⚠️ | Hèches › Plateau de Lannemezan | 3 |
| Forêt de Escala (8) ⚠️ | Escala › Plateau de Lannemezan | 3 |
| Forêt de Cazaux-Fréchet-Anéran-Camors (25) ⚠️ | Cazaux-Fréchet-Anéran-Camors › Aure Louron | 3 |
| Forêt de Loudervielle (45) ⚠️ | Loudervielle › Aure Louron | 3 |
| Bois de Génos (60) ⚠️ | Génos › Aure Louron | 3 |
| Forêt de Ancizan (42) ⚠️ | Ancizan › Aure Louron | 3 |
| Forêt de Vielle-Aure (194) ⚠️ | Vielle-Aure › Aure Louron | 3 |
| Forêt de Vielle-Aure (196) ⚠️ | Vielle-Aure › Aure Louron | 3 |
| Bois de Aragnouet (75) ⚠️ | Aragnouet › Aure Louron | 3 |
| Bois de Gardères (76) ⚠️ | Gardères › Tarbes-Lourdes-Pyrénées | 3 |
| Bois de Séron (42) ⚠️ | Séron › Tarbes-Lourdes-Pyrénées | 3 |
| Bois de Larreule (43) ⚠️ | Larreule › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Artagnan (19) ⚠️ | Artagnan › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Artagnan (20) ⚠️ | Artagnan › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Bois de Maubourguet (122) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Madiran (21) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Bois de Castelnau-Rivière-Basse (51) ⚠️ | Castelnau-Rivière-Basse › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Bois de Hères (32) ⚠️ | Hères › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Bois de Labatut-Rivière (52) ⚠️ | Labatut-Rivière › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Bois de Castelnau-Rivière-Basse (54) ⚠️ | Castelnau-Rivière-Basse › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Bordères-sur-l'Échez (53) ⚠️ | Bordères-sur-l'Échez › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Bazillac (60) ⚠️ | Bazillac › Adour-Madiran (Hautes-Pyrénées) | 3 |
| Forêt de Bours (40) ⚠️ | Bours › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Sireix (4) ⚠️ | Sireix › Pyrénées Vallées des Gaves | 3 |
| Bois de Gazost (61) ⚠️ | Gazost › Tarbes-Lourdes-Pyrénées | 3 |
| Forêt de Sazos (55) ⚠️ | Grust › Pyrénées Vallées des Gaves | 3 |
| Forêt de Betpouey (22) ⚠️ | Betpouey › Pyrénées Vallées des Gaves | 3 |
| Bois de Horgues (16) ⚠️ | Horgues › Tarbes-Lourdes-Pyrénées | 3 |
| Bois de Soues (15) ⚠️ | Soues › Tarbes-Lourdes-Pyrénées | 3 |
| Parc de l'Echez ⚠️ | Tarbes › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Tarasteix ⚠️ | Tarasteix › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Vic-en-Bigorre ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Vic-en-Bigorre (2) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Vic-en-Bigorre (5) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Larreule (2) ⚠️ | Larreule › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Caixon ⚠️ | Caixon › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Soublecause ⚠️ | Soublecause › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Madiran (3) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Soublecause (2) ⚠️ | Soublecause › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Soublecause (3) ⚠️ | Soublecause › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Escaunets (3) ⚠️ | Escaunets › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Oroix (3) ⚠️ | Oroix › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Tarasteix (3) ⚠️ | Tarasteix › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Ibos (4) ⚠️ | Ibos › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Ibos (6) ⚠️ | Ibos › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Sère-en-Lavedan (2) ⚠️ | Sère-en-Lavedan › Pyrénées Vallées des Gaves | 2 |
| Bois de Ouzous ⚠️ | Ouzous › Pyrénées Vallées des Gaves | 2 |
| Forêt de Salles (3) ⚠️ | Salles › Pyrénées Vallées des Gaves | 2 |
| Forêt de Gez (3) ⚠️ | Gez › Pyrénées Vallées des Gaves | 2 |
| Forêt de Tarbes ⚠️ | Tarbes › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Saint-Lézer (5) ⚠️ | Saint-Lézer › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Juillan ⚠️ | Juillan › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Gavarnie-Gèdre (8) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 2 |
| Forêt de Arrens-Marsous (15) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 2 |
| Forêt de Luquet ⚠️ | Luquet › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Campan (4) ⚠️ | Campan › Haute-Bigorre | 2 |
| Bois de Beaudéan (4) ⚠️ | Beaudéan › Haute-Bigorre | 2 |
| Forêt de Barèges (8) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 2 |
| Forêt de Barèges (9) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 2 |
| Forêt de Andrest (3) ⚠️ | Andrest › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Siarrouy (12) ⚠️ | Siarrouy › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Vic-en-Bigorre (13) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Bagnères-de-Bigorre (17) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 2 |
| Bois de Ossen (8) ⚠️ | Ossen › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Omex ⚠️ | Omex › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Jarret (5) ⚠️ | Jarret › Tarbes-Lourdes-Pyrénées | 2 |
| Bois de Saint-Créac (17) ⚠️ | Saint-Créac › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Arrodets-ez-Angles ⚠️ | Arrodets-ez-Angles › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt des Angles (2) ⚠️ | Les Angles › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt des Angles (4) ⚠️ | Les Angles › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Lourdes (20) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Lourdes (26) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 2 |
| Bois de Lourdes (15) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Poueyferré (3) ⚠️ | Poueyferré › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Arrens-Marsous (28) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 2 |
| Forêt de Arrens-Marsous (102) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 2 |
| Forêt de Arrens-Marsous (113) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 2 |
| Forêt de Arrens-Marsous (115) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 2 |
| Forêt de Estaing (45) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 2 |
| Forêt de Estaing (48) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 2 |
| Forêt de Gaillagos (55) ⚠️ | Gaillagos › Pyrénées Vallées des Gaves | 2 |
| Forêt de Arcizans-Dessus (32) ⚠️ | Arcizans-Dessus › Pyrénées Vallées des Gaves | 2 |
| Forêt de Arras-en-Lavedan (18) ⚠️ | Arras-en-Lavedan › Pyrénées Vallées des Gaves | 2 |
| Bois de Lau-Balagnas (24) ⚠️ | Lau-Balagnas › Pyrénées Vallées des Gaves | 2 |
| Bois de Lau-Balagnas (29) ⚠️ | Lau-Balagnas › Pyrénées Vallées des Gaves | 2 |
| Forêt de Ayros-Arbouix (26) ⚠️ | Ayros-Arbouix › Pyrénées Vallées des Gaves | 2 |
| Forêt de Saligos (18) ⚠️ | Saligos › Pyrénées Vallées des Gaves | 2 |
| Forêt de Chèze (14) ⚠️ | Chèze › Pyrénées Vallées des Gaves | 2 |
| Forêt de Sazos (16) ⚠️ | Sazos › Pyrénées Vallées des Gaves | 2 |
| Forêt de Grust (18) ⚠️ | Grust › Pyrénées Vallées des Gaves | 2 |
| Forêt de Viey (4) ⚠️ | Viey › Pyrénées Vallées des Gaves | 2 |
| Forêt de Viella (7) ⚠️ | Esterre › Pyrénées Vallées des Gaves | 2 |
| Forêt de Sers (25) ⚠️ | Sers › Pyrénées Vallées des Gaves | 2 |
| Forêt de Sers (56) ⚠️ | Sers › Pyrénées Vallées des Gaves | 2 |
| Bois de Betpouey (8) ⚠️ | Betpouey › Pyrénées Vallées des Gaves | 2 |
| Forêt de Gavarnie-Gèdre (14) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 2 |
| Forêt de Luquet (2) ⚠️ | Luquet › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Luquet (10) ⚠️ | Luquet › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Gardères (9) ⚠️ | Gardères › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Gavarnie-Gèdre (23) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 2 |
| Forêt de Gavarnie-Gèdre (75) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 2 |
| Forêt de Gavarnie-Gèdre (89) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 2 |
| Forêt de Gavarnie-Gèdre (93) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 2 |
| Forêt de Gavarnie-Gèdre (200) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 2 |
| Forêt de Gavarnie-Gèdre (226) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 2 |
| Forêt de Gavarnie-Gèdre (271) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 2 |
| Forêt de Luquet (14) ⚠️ | Luquet › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Gardères (13) ⚠️ | Gardères › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Cauterets (41) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 2 |
| Forêt de Cauterets (65) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 2 |
| Forêt de Cauterets (86) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 2 |
| Forêt de Cauterets (174) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 2 |
| Forêt de Cauterets (177) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 2 |
| Forêt de Cauterets (264) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 2 |
| Forêt de Cauterets (279) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 2 |
| Forêt de Cauterets (306) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 2 |
| Forêt de Cauterets (347) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 2 |
| Forêt de Cauterets (360) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 2 |
| Forêt de Cauterets (366) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 2 |
| Forêt de Cauterets (378) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 2 |
| Forêt de Cauterets (384) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 2 |
| Forêt de Cauterets (394) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 2 |
| Forêt de Cauterets (395) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 2 |
| Forêt de Cauterets (397) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 2 |
| Forêt de Cauterets (400) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 2 |
| Forêt de Cauterets (401) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 2 |
| Bois de Cauterets (12) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 2 |
| Forêt de Cauterets (475) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 2 |
| Forêt de Cauterets (477) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 2 |
| Bois de Cauterets (15) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 2 |
| Forêt de Cauterets (497) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 2 |
| Forêt de Gazost (21) ⚠️ | Gazost › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Germ (3) ⚠️ | Germ › Aure Louron | 2 |
| Forêt de Loudervielle (5) ⚠️ | Loudervielle › Aure Louron | 2 |
| Bois de Bordères-sur-l'Échez (3) ⚠️ | Bordères-sur-l'Échez › Tarbes-Lourdes-Pyrénées | 2 |
| Parc de Ibos ⚠️ | Tarbes › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Bazet (5) ⚠️ | Bazet › Tarbes-Lourdes-Pyrénées | 2 |
| Bois de Bordères-sur-l'Échez (11) ⚠️ | Bordères-sur-l'Échez › Tarbes-Lourdes-Pyrénées | 2 |
| Parc de Bordères-sur-l'Échez (2) ⚠️ | Bordères-sur-l'Échez › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Pouzac (3) ⚠️ | Pouzac › Haute-Bigorre | 2 |
| Forêt de Trébons (4) ⚠️ | Trébons › Haute-Bigorre | 2 |
| Forêt de Pouzac (12) ⚠️ | Pouzac › Haute-Bigorre | 2 |
| Bois de Pouzac ⚠️ | Pouzac › Haute-Bigorre | 2 |
| Forêt de Bagnères-de-Bigorre (83) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 2 |
| Forêt de Pouzac (74) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 2 |
| Forêt de Bagnères-de-Bigorre (99) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 2 |
| Forêt de Bagnères-de-Bigorre (103) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 2 |
| Forêt de Asté (7) ⚠️ | Asté › Haute-Bigorre | 2 |
| Forêt de Campan (72) ⚠️ | Campan › Haute-Bigorre | 2 |
| Forêt de Campan (108) ⚠️ | Campan › Haute-Bigorre | 2 |
| Forêt de Asque ⚠️ | Asque › Plateau de Lannemezan | 2 |
| Forêt de Campan (200) ⚠️ | Campan › Haute-Bigorre | 2 |
| Forêt de Campan (224) ⚠️ | Campan › Haute-Bigorre | 2 |
| Forêt de Astugue (14) ⚠️ | Astugue › Haute-Bigorre | 2 |
| Forêt de Astugue (17) ⚠️ | Astugue › Haute-Bigorre | 2 |
| Forêt de Loucrup (5) ⚠️ | Loucrup › Tarbes-Lourdes-Pyrénées | 2 |
| Bois de Trébons (2) ⚠️ | Trébons › Haute-Bigorre | 2 |
| Forêt de Montgaillard (24) ⚠️ | Montgaillard › Haute-Bigorre | 2 |
| Forêt de Saint-Lary-Soulan (18) ⚠️ | Saint-Lary-Soulan › Aure Louron | 2 |
| Forêt de Saint-Pé-de-Bigorre (21) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Saint-Pé-de-Bigorre (44) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Saint-Pé-de-Bigorre (54) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 2 |
| Bois de Peyrouse (3) ⚠️ | Peyrouse › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Peyrouse (15) ⚠️ | Peyrouse › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Poueyferré (18) ⚠️ | Poueyferré › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Poueyferré (48) ⚠️ | Poueyferré › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Lourdes (52) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Lourdes (84) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Lourdes (89) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Bourréac (2) ⚠️ | Bourréac › Tarbes-Lourdes-Pyrénées | 2 |
| Bois de Julos (5) ⚠️ | Julos › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Bourréac (9) ⚠️ | Bourréac › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Julos (10) ⚠️ | Bourréac › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Julos (16) ⚠️ | Julos › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Barry (3) ⚠️ | Barry › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Barry (5) ⚠️ | Barry › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Lamarque-Pontacq (30) ⚠️ | Lamarque-Pontacq › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Lamarque-Pontacq (33) ⚠️ | Lamarque-Pontacq › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Ossun (50) ⚠️ | Ossun › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Lanne (13) ⚠️ | Lanne › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Loucrup (11) ⚠️ | Loucrup › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Orincles (16) ⚠️ | Orincles › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Bénac (8) ⚠️ | Bénac › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Saint-Martin (14) ⚠️ | Saint-Martin › Tarbes-Lourdes-Pyrénées | 2 |
| Bois de Ibos (2) ⚠️ | Ibos › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Juillan (84) ⚠️ | Juillan › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Juillan (90) ⚠️ | Juillan › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Tostat (3) ⚠️ | Tostat › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Bazillac (18) ⚠️ | Bazillac › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Vic-en-Bigorre (12) ⚠️ | Pujo › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Escondeaux (3) ⚠️ | Escondeaux › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Aureilhan (7) ⚠️ | Aureilhan › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Séméac (4) ⚠️ | Séméac › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Séméac (9) ⚠️ | Séméac › Tarbes-Lourdes-Pyrénées | 2 |
| CRCAM Pyrénées Gascogne ⚠️ | Tarbes › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Soues (10) ⚠️ | Soues › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Laloubère (23) ⚠️ | Laloubère › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Laloubère (28) ⚠️ | Laloubère › Tarbes-Lourdes-Pyrénées | 2 |
| Bois de Horgues ⚠️ | Horgues › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Soues (15) ⚠️ | Soues › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Barbazan-Debat (7) ⚠️ | Calavanté › Coteaux du Val-d'Arros | 2 |
| Forêt de Barbazan-Debat (8) ⚠️ | Barbazan-Debat › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Barbazan-Debat (10) ⚠️ | Barbazan-Debat › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Barbazan-Debat (11) ⚠️ | Barbazan-Debat › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Allier (4) ⚠️ | Allier › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Arcizac-Adour (5) ⚠️ | Arcizac-Adour › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Odos (14) ⚠️ | Odos › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Momères (8) ⚠️ | Momères › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Arcizac-Adour (17) ⚠️ | Arcizac-Adour › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Visker (5) ⚠️ | Saint-Martin › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Saint-Martin (38) ⚠️ | Saint-Martin › Tarbes-Lourdes-Pyrénées | 2 |
| Bois de Saint-Martin (9) ⚠️ | Saint-Martin › Tarbes-Lourdes-Pyrénées | 2 |
| Bois de Arcizac-Adour (13) ⚠️ | Arcizac-Adour › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Hiis (16) ⚠️ | Hiis › Haute-Bigorre | 2 |
| Bois de Arcizac-Adour (19) ⚠️ | Arcizac-Adour › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Vielle-Adour (2) ⚠️ | Vielle-Adour › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Vielle-Adour (6) ⚠️ | Vielle-Adour › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Bernac-Dessus (15) ⚠️ | Bernac-Dessus › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Vielle-Adour (11) ⚠️ | Vielle-Adour › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Orignac (6) ⚠️ | Orignac › Haute-Bigorre | 2 |
| Forêt de Visker (20) ⚠️ | Visker › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Mascaras (4) ⚠️ | Mascaras › Coteaux du Val-d'Arros | 2 |
| Forêt de Fréchou-Fréchet (5) ⚠️ | Montignac › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Bordes (11) ⚠️ | Bordes › Coteaux du Val-d'Arros | 2 |
| Forêt de Luc (6) ⚠️ | Orignac › Haute-Bigorre | 2 |
| Forêt de Chelle-Spou (4) ⚠️ | Chelle-Spou › Plateau de Lannemezan | 2 |
| Forêt de Argelès-Bagnères (23) ⚠️ | Argelès-Bagnères › Haute-Bigorre | 2 |
| Forêt de Bettes (3) ⚠️ | Bettes › Haute-Bigorre | 2 |
| Forêt de Marsas (14) ⚠️ | Marsas › Haute-Bigorre | 2 |
| Forêt de Esconnets (5) ⚠️ | Esconnets › Plateau de Lannemezan | 2 |
| Forêt de Bettes (24) ⚠️ | Bettes › Haute-Bigorre | 2 |
| Forêt de Escots (13) ⚠️ | Escots › Plateau de Lannemezan | 2 |
| Forêt de Espèche (4) ⚠️ | Espèche › Plateau de Lannemezan | 2 |
| Forêt de Esparros (16) ⚠️ | Esparros › Plateau de Lannemezan | 2 |
| Forêt de Labastide (2) ⚠️ | Labastide › Plateau de Lannemezan | 2 |
| Forêt de Labastide (4) ⚠️ | Esparros › Plateau de Lannemezan | 2 |
| Forêt de Hèches (3) ⚠️ | Hèches › Plateau de Lannemezan | 2 |
| Forêt de Labastide (14) ⚠️ | Labastide › Plateau de Lannemezan | 2 |
| Forêt de Avezac-Prat-Lahitte (23) ⚠️ | Avezac-Prat-Lahitte › Plateau de Lannemezan | 2 |
| Forêt de Capvern (10) ⚠️ | Capvern › Plateau de Lannemezan | 2 |
| Forêt de Ozon (15) ⚠️ | Ozon › Coteaux du Val-d'Arros | 2 |
| Forêt de Ricaud (3) ⚠️ | Ricaud › Coteaux du Val-d'Arros | 2 |
| Forêt de Gourgue ⚠️ | Gourgue › Plateau de Lannemezan | 2 |
| Forêt de Ozon (18) ⚠️ | Ozon › Coteaux du Val-d'Arros | 2 |
| Forêt de Ozon (19) ⚠️ | Ozon › Coteaux du Val-d'Arros | 2 |
| Forêt de Capvern (128) ⚠️ | Capvern › Plateau de Lannemezan | 2 |
| Forêt de Lannemezan (5) ⚠️ | Lannemezan › Plateau de Lannemezan | 2 |
| Forêt de Péré (16) ⚠️ | Péré › Plateau de Lannemezan | 2 |
| Forêt de Tournay (11) ⚠️ | Tournay › Coteaux du Val-d'Arros | 2 |
| Forêt de Tournay (28) ⚠️ | Tournay › Coteaux du Val-d'Arros | 2 |
| Forêt de Tournay (58) ⚠️ | Tournay › Coteaux du Val-d'Arros | 2 |
| Forêt de Bordes (33) ⚠️ | Bordes › Coteaux du Val-d'Arros | 2 |
| Forêt de Bordes (45) ⚠️ | Bordes › Coteaux du Val-d'Arros | 2 |
| Forêt de Lhez (2) ⚠️ | Lhez › Coteaux du Val-d'Arros | 2 |
| Forêt de Bordes (57) ⚠️ | Bordes › Coteaux du Val-d'Arros | 2 |
| Forêt de Peyraube (17) ⚠️ | Peyraube › Coteaux du Val-d'Arros | 2 |
| Bois de Goudon ⚠️ | Goudon › Coteaux du Val-d'Arros | 2 |
| Forêt de Goudon (8) ⚠️ | Goudon › Coteaux du Val-d'Arros | 2 |
| Forêt de Goudon (15) ⚠️ | Goudon › Coteaux du Val-d'Arros | 2 |
| Forêt de Pouyastruc ⚠️ | Pouyastruc › Coteaux du Val-d'Arros | 2 |
| Forêt de Souyeaux ⚠️ | Souyeaux › Coteaux du Val-d'Arros | 2 |
| Forêt de Hourc ⚠️ | Hourc › Coteaux du Val-d'Arros | 2 |
| Forêt de Coussan (8) ⚠️ | Coussan › Coteaux du Val-d'Arros | 2 |
| Forêt de Cabanac (7) ⚠️ | Cabanac › Coteaux du Val-d'Arros | 2 |
| Bois de Chelle-Debat (4) ⚠️ | Chelle-Debat › Coteaux du Val-d'Arros | 2 |
| Forêt de Louit ⚠️ | Louit › Coteaux du Val-d'Arros | 2 |
| Forêt de Bouilh-Péreuilh (4) ⚠️ | Bouilh-Péreuilh › Coteaux du Val-d'Arros | 2 |
| Forêt de Bouilh-Péreuilh (6) ⚠️ | Bouilh-Péreuilh › Coteaux du Val-d'Arros | 2 |
| Forêt de Saint-Sever-de-Rustan (2) ⚠️ | Saint-Sever-de-Rustan › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Sénac (4) ⚠️ | Sénac › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Peyrun (8) ⚠️ | Peyrun › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Peyrun (13) ⚠️ | Peyrun › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Lacassagne (5) ⚠️ | Lacassagne › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Saint-Sever-de-Rustan (3) ⚠️ | Saint-Sever-de-Rustan › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Moumoulous ⚠️ | Moumoulous › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Fréchède ⚠️ | Fréchède › Pays de Trie et du Magnoac | 2 |
| Forêt de Lescurry (2) ⚠️ | Lescurry › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Lescurry (5) ⚠️ | Castéra-Lou › Coteaux du Val-d'Arros | 2 |
| Forêt de Lescurry (7) ⚠️ | Lescurry › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Dours ⚠️ | Dours › Coteaux du Val-d'Arros | 2 |
| Forêt de Collongues (3) ⚠️ | Collongues › Coteaux du Val-d'Arros | 2 |
| Forêt de Collongues (4) ⚠️ | Collongues › Coteaux du Val-d'Arros | 2 |
| Bois de Sabalos (8) ⚠️ | Sabalos › Coteaux du Val-d'Arros | 2 |
| Forêt de Pouyastruc (12) ⚠️ | Pouyastruc › Coteaux du Val-d'Arros | 2 |
| Forêt de Hourc (3) ⚠️ | Hourc › Coteaux du Val-d'Arros | 2 |
| Forêt de Pouyastruc (19) ⚠️ | Pouyastruc › Coteaux du Val-d'Arros | 2 |
| Forêt de Pouyastruc (20) ⚠️ | Pouyastruc › Coteaux du Val-d'Arros | 2 |
| Forêt de Pouyastruc (22) ⚠️ | Pouyastruc › Coteaux du Val-d'Arros | 2 |
| Forêt de Laslades (6) ⚠️ | Laslades › Coteaux du Val-d'Arros | 2 |
| Forêt de Souyeaux (14) ⚠️ | Souyeaux › Coteaux du Val-d'Arros | 2 |
| Bois de Lansac (11) ⚠️ | Lansac › Coteaux du Val-d'Arros | 2 |
| Forêt de Sarrouilles (6) ⚠️ | Sarrouilles › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Aubarède (3) ⚠️ | Aubarède › Coteaux du Val-d'Arros | 2 |
| Forêt de Bouilh-Devant (7) ⚠️ | Bouilh-Devant › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Estampures (2) ⚠️ | Estampures › Pays de Trie et du Magnoac | 2 |
| Forêt de Antin (4) ⚠️ | Antin › Pays de Trie et du Magnoac | 2 |
| Forêt de Estampures (11) ⚠️ | Estampures › Pays de Trie et du Magnoac | 2 |
| Forêt de Lapeyre ⚠️ | Lapeyre › Pays de Trie et du Magnoac | 2 |
| Bois de Antin (12) ⚠️ | Antin › Pays de Trie et du Magnoac | 2 |
| Bois de Lapeyre (4) ⚠️ | Lapeyre › Pays de Trie et du Magnoac | 2 |
| Forêt de Antin (7) ⚠️ | Antin › Pays de Trie et du Magnoac | 2 |
| Forêt de Luby-Betmont (2) ⚠️ | Luby-Betmont › Pays de Trie et du Magnoac | 2 |
| Forêt de Bernadets-Debat (2) ⚠️ | Bernadets-Debat › Pays de Trie et du Magnoac | 2 |
| Bois de Trie-sur-Baïse (12) ⚠️ | Trie-sur-Baïse › Pays de Trie et du Magnoac | 2 |
| Bois de Lalanne-Trie (4) ⚠️ | Lalanne-Trie › Pays de Trie et du Magnoac | 2 |
| Bois de Bourisp ⚠️ | Bourisp › Aure Louron | 2 |
| Forêt de Tournous-Darré (6) ⚠️ | Tournous-Darré › Pays de Trie et du Magnoac | 2 |
| Forêt de Lalanne-Trie (4) ⚠️ | Lalanne-Trie › Pays de Trie et du Magnoac | 2 |
| Forêt de Fontrailles (15) ⚠️ | Fontrailles › Pays de Trie et du Magnoac | 2 |
| Bois de Fontrailles (23) ⚠️ | Fontrailles › Pays de Trie et du Magnoac | 2 |
| Bois de Mun ⚠️ | Luby-Betmont › Pays de Trie et du Magnoac | 2 |
| Forêt de Mun (7) ⚠️ | Mun › Coteaux du Val-d'Arros | 2 |
| Forêt de Mun (15) ⚠️ | Mun › Coteaux du Val-d'Arros | 2 |
| Bois de Mun (5) ⚠️ | Mun › Coteaux du Val-d'Arros | 2 |
| Bois de Mun (7) ⚠️ | Mun › Coteaux du Val-d'Arros | 2 |
| Bois de Luby-Betmont (6) ⚠️ | Luby-Betmont › Pays de Trie et du Magnoac | 2 |
| Forêt de Lustar ⚠️ | Lustar › Pays de Trie et du Magnoac | 2 |
| Forêt de Orieux (4) ⚠️ | Orieux › Coteaux du Val-d'Arros | 2 |
| Bois de Lustar (10) ⚠️ | Lustar › Pays de Trie et du Magnoac | 2 |
| Forêt de Montastruc ⚠️ | Montastruc › Plateau de Lannemezan | 2 |
| Forêt de Bégole (6) ⚠️ | Bégole › Coteaux du Val-d'Arros | 2 |
| Forêt de Burg (21) ⚠️ | Burg › Coteaux du Val-d'Arros | 2 |
| Bois de Montastruc (41) ⚠️ | Montastruc › Plateau de Lannemezan | 2 |
| Forêt de Bégole (8) ⚠️ | Bégole › Coteaux du Val-d'Arros | 2 |
| Forêt de Lagrange (3) ⚠️ | Lagrange › Plateau de Lannemezan | 2 |
| Forêt de Campistrous (6) ⚠️ | Campistrous › Plateau de Lannemezan | 2 |
| Bois de Bonnefont (45) ⚠️ | Bonnefont › Pays de Trie et du Magnoac | 2 |
| Forêt de Montastruc (12) ⚠️ | Montastruc › Plateau de Lannemezan | 2 |
| Forêt de Libaros (4) ⚠️ | Libaros › Plateau de Lannemezan | 2 |
| Bois de Libaros ⚠️ | Libaros › Plateau de Lannemezan | 2 |
| Forêt de Castelbajac (5) ⚠️ | Castelbajac › Plateau de Lannemezan | 2 |
| Forêt de Bonrepos (9) ⚠️ | Bonrepos › Plateau de Lannemezan | 2 |
| Forêt de Castelbajac (7) ⚠️ | Castelbajac › Plateau de Lannemezan | 2 |
| Bois de Galan (3) ⚠️ | Galan › Plateau de Lannemezan | 2 |
| Forêt de Campistrous (23) ⚠️ | Campistrous › Plateau de Lannemezan | 2 |
| Bois de Lannemezan (15) ⚠️ | Lannemezan › Plateau de Lannemezan | 2 |
| Forêt de Lannemezan (31) ⚠️ | Lannemezan › Plateau de Lannemezan | 2 |
| Bois de Lannemezan (55) ⚠️ | Lannemezan › Plateau de Lannemezan | 2 |
| Forêt de Lannemezan (37) ⚠️ | Lannemezan › Plateau de Lannemezan | 2 |
| Forêt de Lannemezan (52) ⚠️ | Lannemezan › Plateau de Lannemezan | 2 |
| Bois de Escala (3) ⚠️ | Cantaous › Neste Barousse | 2 |
| Bois de Uglas ⚠️ | Uglas › Plateau de Lannemezan | 2 |
| Forêt de Lannemezan (64) ⚠️ | Lannemezan › Plateau de Lannemezan | 2 |
| Forêt de Clarens (3) ⚠️ | Clarens › Plateau de Lannemezan | 2 |
| Forêt de Clarens (14) ⚠️ | Clarens › Plateau de Lannemezan | 2 |
| Forêt de Recurt (3) ⚠️ | Recurt › Plateau de Lannemezan | 2 |
| Forêt de Recurt (4) ⚠️ | Recurt › Plateau de Lannemezan | 2 |
| Bois de Galan (51) ⚠️ | Galan › Plateau de Lannemezan | 2 |
| Bois de Galan (74) ⚠️ | Galan › Plateau de Lannemezan | 2 |
| Bois de Galan (97) ⚠️ | Galan › Plateau de Lannemezan | 2 |
| Forêt de Libaros (8) ⚠️ | Libaros › Plateau de Lannemezan | 2 |
| Forêt de Sadournin (6) ⚠️ | Sadournin › Pays de Trie et du Magnoac | 2 |
| Bois de Puntous (11) ⚠️ | Puntous › Pays de Trie et du Magnoac | 2 |
| Forêt de Puntous ⚠️ | Guizerix › Pays de Trie et du Magnoac | 2 |
| Bois de Larroque (2) ⚠️ | Larroque › Pays de Trie et du Magnoac | 2 |
| Bois de Larroque (9) ⚠️ | Larroque › Pays de Trie et du Magnoac | 2 |
| Bois de Puntous (25) ⚠️ | Puntous › Pays de Trie et du Magnoac | 2 |
| Bois de Vieuzos (2) ⚠️ | Vieuzos › Pays de Trie et du Magnoac | 2 |
| Forêt de Betpouy ⚠️ | Betpouy › Pays de Trie et du Magnoac | 2 |
| Forêt de Recurt (7) ⚠️ | Recurt › Plateau de Lannemezan | 2 |
| Forêt de Recurt (16) ⚠️ | Recurt › Plateau de Lannemezan | 2 |
| Forêt de Castelnau-Magnoac ⚠️ | Castelnau-Magnoac › Pays de Trie et du Magnoac | 2 |
| Forêt de Castelnau-Magnoac (8) ⚠️ | Castelnau-Magnoac › Pays de Trie et du Magnoac | 2 |
| Forêt de Castelnau-Magnoac (9) ⚠️ | Castelnau-Magnoac › Pays de Trie et du Magnoac | 2 |
| Bois de Cizos (4) ⚠️ | Cizos › Pays de Trie et du Magnoac | 2 |
| Bois de Caubous (10) ⚠️ | Caubous › Pays de Trie et du Magnoac | 2 |
| Bois de Laran (2) ⚠️ | Laran › Pays de Trie et du Magnoac | 2 |
| Bois de Cizos (21) ⚠️ | Cizos › Pays de Trie et du Magnoac | 2 |
| Bois de Tajan (10) ⚠️ | Tajan › Plateau de Lannemezan | 2 |
| Bois de Tajan (14) ⚠️ | Monlong › Pays de Trie et du Magnoac | 2 |
| Bois de Réjaumont (5) ⚠️ | Tajan › Plateau de Lannemezan | 2 |
| Bois de Tajan (21) ⚠️ | Tajan › Plateau de Lannemezan | 2 |
| Forêt de Tajan (5) ⚠️ | Tajan › Plateau de Lannemezan | 2 |
| Forêt de Réjaumont (17) ⚠️ | Réjaumont › Plateau de Lannemezan | 2 |
| Bois de Gaussan (20) ⚠️ | Lassales › Pays de Trie et du Magnoac | 2 |
| Forêt de Lassales (2) ⚠️ | Lassales › Pays de Trie et du Magnoac | 2 |
| Bois de Monléon-Magnoac (46) ⚠️ | Monléon-Magnoac › Pays de Trie et du Magnoac | 2 |
| Forêt de Monléon-Magnoac (4) ⚠️ | Monléon-Magnoac › Pays de Trie et du Magnoac | 2 |
| Forêt de Monléon-Magnoac (13) ⚠️ | Monléon-Magnoac › Pays de Trie et du Magnoac | 2 |
| Bois de Pouy (15) ⚠️ | Pouy › Pays de Trie et du Magnoac | 2 |
| Forêt de Pouy ⚠️ | Pouy › Pays de Trie et du Magnoac | 2 |
| Bois de Arné (24) ⚠️ | Arné › Plateau de Lannemezan | 2 |
| Bois de Arné (62) ⚠️ | Arné › Plateau de Lannemezan | 2 |
| Bois de Lalanne (9) ⚠️ | Lalanne › Pays de Trie et du Magnoac | 2 |
| Bois de Thermes-Magnoac (51) ⚠️ | Thermes-Magnoac › Pays de Trie et du Magnoac | 2 |
| Forêt de Thermes-Magnoac (10) ⚠️ | Thermes-Magnoac › Pays de Trie et du Magnoac | 2 |
| Bois de Thermes-Magnoac (73) ⚠️ | Thermes-Magnoac › Pays de Trie et du Magnoac | 2 |
| Bois de Casterets (9) ⚠️ | Casterets › Pays de Trie et du Magnoac | 2 |
| Forêt de Sariac-Magnoac ⚠️ | Sariac-Magnoac › Pays de Trie et du Magnoac | 2 |
| Bois de Sariac-Magnoac (26) ⚠️ | Sariac-Magnoac › Pays de Trie et du Magnoac | 2 |
| Bois de Sariac-Magnoac (58) ⚠️ | Sariac-Magnoac › Pays de Trie et du Magnoac | 2 |
| Bois de Bazordan (6) ⚠️ | Bazordan › Pays de Trie et du Magnoac | 2 |
| Forêt de Bazordan (6) ⚠️ | Bazordan › Pays de Trie et du Magnoac | 2 |
| Forêt de Cantaous ⚠️ | Cantaous › Neste Barousse | 2 |
| Bois de Saint-Laurent-de-Neste (8) ⚠️ | Saint-Laurent-de-Neste › Neste Barousse | 2 |
| Bois de Saint-Laurent-de-Neste (9) ⚠️ | Saint-Laurent-de-Neste › Neste Barousse | 2 |
| Forêt de Saint-Paul ⚠️ | Saint-Paul › Neste Barousse | 2 |
| Forêt de Saint-Paul (2) ⚠️ | Saint-Paul › Neste Barousse | 2 |
| Forêt de Saint-Paul (8) ⚠️ | Saint-Paul › Neste Barousse | 2 |
| Bois de Cantaous (20) ⚠️ | Cantaous › Neste Barousse | 2 |
| Forêt de Cantaous (2) ⚠️ | Cantaous › Neste Barousse | 2 |
| Forêt de Saint-Paul (10) ⚠️ | Saint-Paul › Neste Barousse | 2 |
| Forêt de Saint-Laurent-de-Neste (10) ⚠️ | Saint-Laurent-de-Neste › Neste Barousse | 2 |
| Bois de Cantaous (69) ⚠️ | Cantaous › Neste Barousse | 2 |
| Forêt de Cantaous (9) ⚠️ | Cantaous › Neste Barousse | 2 |
| Forêt de Cantaous (10) ⚠️ | Cantaous › Neste Barousse | 2 |
| Bois de Saint-Laurent-de-Neste (83) ⚠️ | Saint-Laurent-de-Neste › Neste Barousse | 2 |
| Bois de Saint-Laurent-de-Neste (88) ⚠️ | Saint-Laurent-de-Neste › Neste Barousse | 2 |
| Bois de Nestier (2) ⚠️ | Nestier › Neste Barousse | 2 |
| Bois de Aventignan (6) ⚠️ | Aventignan › Neste Barousse | 2 |
| Bois de Mazères-de-Neste (28) ⚠️ | Mazères-de-Neste › Neste Barousse | 2 |
| Forêt de Tibiran-Jaunac (2) ⚠️ | Tibiran-Jaunac › Neste Barousse | 2 |
| Forêt de Saint-Paul (20) ⚠️ | Saint-Paul › Neste Barousse | 2 |
| Forêt de Mazères-de-Neste (6) ⚠️ | Mazères-de-Neste › Neste Barousse | 2 |
| Forêt de Tibiran-Jaunac (6) ⚠️ | Tibiran-Jaunac › Neste Barousse | 2 |
| Forêt de Tibiran-Jaunac (7) ⚠️ | Tibiran-Jaunac › Neste Barousse | 2 |
| Forêt de Tibiran-Jaunac (15) ⚠️ | Tibiran-Jaunac › Neste Barousse | 2 |
| Forêt de Gaudent ⚠️ | Gaudent › Neste Barousse | 2 |
| Bois de Loures-Barousse (6) ⚠️ | Loures-Barousse › Neste Barousse | 2 |
| Bois de Loures-Barousse (18) ⚠️ | Loures-Barousse › Neste Barousse | 2 |
| Bois de Anla (22) ⚠️ | Anla › Neste Barousse | 2 |
| Bois de Sost (2) ⚠️ | Sost › Neste Barousse | 2 |
| Forêt de Sost (13) ⚠️ | Sost › Neste Barousse | 2 |
| Bois de Ourde (29) ⚠️ | Ourde › Neste Barousse | 2 |
| Bois de Seich (12) ⚠️ | Seich › Neste Barousse | 2 |
| Forêt de Nistos (9) ⚠️ | Nistos › Neste Barousse | 2 |
| Bois de Nestier (19) ⚠️ | Nestier › Neste Barousse | 2 |
| Bois de Nestier (30) ⚠️ | Nestier › Neste Barousse | 2 |
| Forêt de Nestier (5) ⚠️ | Nestier › Neste Barousse | 2 |
| Bois de Anères (10) ⚠️ | Anères › Neste Barousse | 2 |
| Forêt de Tuzaguet (6) ⚠️ | Tuzaguet › Neste Barousse | 2 |
| Bois de Bizous (6) ⚠️ | Bizous › Neste Barousse | 2 |
| Bois de Tuzaguet (37) ⚠️ | Tuzaguet › Neste Barousse | 2 |
| Forêt de Bizous (6) ⚠️ | Bizous › Neste Barousse | 2 |
| Bois de Montoussé (13) ⚠️ | Montoussé › Plateau de Lannemezan | 2 |
| Forêt de Montoussé (4) ⚠️ | Montoussé › Plateau de Lannemezan | 2 |
| Bois de Montoussé (40) ⚠️ | Montoussé › Plateau de Lannemezan | 2 |
| Bois de Montoussé (41) ⚠️ | Montoussé › Plateau de Lannemezan | 2 |
| Bois de Escala (10) ⚠️ | Escala › Plateau de Lannemezan | 2 |
| Bois de Bazus-Neste (10) ⚠️ | Bazus-Neste › Plateau de Lannemezan | 2 |
| Forêt de Bazus-Neste ⚠️ | Bazus-Neste › Plateau de Lannemezan | 2 |
| Bois de Escala (22) ⚠️ | La Barthe-de-Neste › Plateau de Lannemezan | 2 |
| Bois de Escala (31) ⚠️ | Escala › Plateau de Lannemezan | 2 |
| Forêt de Escala (6) ⚠️ | Escala › Plateau de Lannemezan | 2 |
| Bois de La Barthe-de-Neste (46) ⚠️ | La Barthe-de-Neste › Plateau de Lannemezan | 2 |
| Forêt de La Barthe-de-Neste (12) ⚠️ | La Barthe-de-Neste › Plateau de Lannemezan | 2 |
| Forêt de La Barthe-de-Neste (13) ⚠️ | La Barthe-de-Neste › Plateau de Lannemezan | 2 |
| Forêt de Lortet (7) ⚠️ | Lortet › Plateau de Lannemezan | 2 |
| Forêt de Lortet (8) ⚠️ | Lortet › Plateau de Lannemezan | 2 |
| Bois de Hèches (72) ⚠️ | Hèches › Plateau de Lannemezan | 2 |
| Bois de Pailhac (10) ⚠️ | Pailhac › Aure Louron | 2 |
| Forêt de Aspin-Aure (9) ⚠️ | Aspin-Aure › Aure Louron | 2 |
| Forêt de Bareilles (7) ⚠️ | Bareilles › Aure Louron | 2 |
| Bois de Bareilles (8) ⚠️ | Bareilles › Aure Louron | 2 |
| Forêt de Bordères-Louron (18) ⚠️ | Bordères-Louron › Aure Louron | 2 |
| Forêt de Cazaux-Fréchet-Anéran-Camors (11) ⚠️ | Cazaux-Fréchet-Anéran-Camors › Aure Louron | 2 |
| Forêt de Vielle-Louron (7) ⚠️ | Vielle-Louron › Aure Louron | 2 |
| Forêt de Loudervielle (17) ⚠️ | Loudervielle › Aure Louron | 2 |
| Forêt de Germ (11) ⚠️ | Germ › Aure Louron | 2 |
| Forêt de Germ (17) ⚠️ | Germ › Aure Louron | 2 |
| Bois de Ancizan (3) ⚠️ | Ancizan › Aure Louron | 2 |
| Forêt de Ancizan (32) ⚠️ | Ancizan › Aure Louron | 2 |
| Bois de Grézian (11) ⚠️ | Grézian › Aure Louron | 2 |
| Bois de Guchen (10) ⚠️ | Guchen › Aure Louron | 2 |
| Bois de Aulon ⚠️ | Aulon › Aure Louron | 2 |
| Forêt de Bazus-Aure (2) ⚠️ | Bazus-Aure › Aure Louron | 2 |
| Forêt de Estensan ⚠️ | Estensan › Aure Louron | 2 |
| Forêt de Azet (18) ⚠️ | Azet › Aure Louron | 2 |
| Forêt de Azet (43) ⚠️ | Azet › Aure Louron | 2 |
| Forêt de Saint-Lary-Soulan (48) ⚠️ | Saint-Lary-Soulan › Aure Louron | 2 |
| Forêt de Tramezaïgues (2) ⚠️ | Tramezaïgues › Aure Louron | 2 |
| Forêt de Saint-Lary-Soulan (64) ⚠️ | Saint-Lary-Soulan › Aure Louron | 2 |
| Forêt de Saint-Lary-Soulan (89) ⚠️ | Saint-Lary-Soulan › Aure Louron | 2 |
| Forêt de Saint-Lary-Soulan (93) ⚠️ | Saint-Lary-Soulan › Aure Louron | 2 |
| Forêt de Saint-Lary-Soulan (99) ⚠️ | Saint-Lary-Soulan › Aure Louron | 2 |
| Forêt de Saint-Lary-Soulan (101) ⚠️ | Saint-Lary-Soulan › Aure Louron | 2 |
| Forêt de Saint-Lary-Soulan (107) ⚠️ | Saint-Lary-Soulan › Aure Louron | 2 |
| Forêt de Aragnouet (4) ⚠️ | Aragnouet › Aure Louron | 2 |
| Forêt de Aragnouet (5) ⚠️ | Aragnouet › Aure Louron | 2 |
| Forêt de Tramezaïgues (64) ⚠️ | Tramezaïgues › Aure Louron | 2 |
| Forêt de Tramezaïgues (70) ⚠️ | Tramezaïgues › Aure Louron | 2 |
| Forêt de Tramezaïgues (85) ⚠️ | Tramezaïgues › Aure Louron | 2 |
| Forêt de Aragnouet (12) ⚠️ | Aragnouet › Aure Louron | 2 |
| Forêt de Aragnouet (25) ⚠️ | Aragnouet › Aure Louron | 2 |
| Forêt de Aragnouet (67) ⚠️ | Aragnouet › Aure Louron | 2 |
| Forêt de Aragnouet (79) ⚠️ | Aragnouet › Aure Louron | 2 |
| Forêt de Aragnouet (80) ⚠️ | Aragnouet › Aure Louron | 2 |
| Forêt de Aragnouet (83) ⚠️ | Aragnouet › Aure Louron | 2 |
| Forêt de Aragnouet (153) ⚠️ | Aragnouet › Aure Louron | 2 |
| Forêt de Aragnouet (176) ⚠️ | Aragnouet › Aure Louron | 2 |
| Forêt de Aragnouet (182) ⚠️ | Aragnouet › Aure Louron | 2 |
| Forêt de Vielle-Aure (168) ⚠️ | Vielle-Aure › Aure Louron | 2 |
| Forêt de Vignec (11) ⚠️ | Vignec › Aure Louron | 2 |
| Forêt de Saint-Lary-Soulan (171) ⚠️ | Saint-Lary-Soulan › Aure Louron | 2 |
| Forêt de Saint-Lary-Soulan (172) ⚠️ | Saint-Lary-Soulan › Aure Louron | 2 |
| Forêt de Saint-Lary-Soulan (176) ⚠️ | Saint-Lary-Soulan › Aure Louron | 2 |
| Forêt de Barèges (179) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 2 |
| Forêt de Artagnan (3) ⚠️ | Artagnan › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Artagnan (5) ⚠️ | Artagnan › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Tarasteix (11) ⚠️ | Tarasteix › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Luquet (15) ⚠️ | Luquet › Tarbes-Lourdes-Pyrénées | 2 |
| Bois de Gardères (25) ⚠️ | Gardères › Tarbes-Lourdes-Pyrénées | 2 |
| Bois de Séron (19) ⚠️ | Séron › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Vic-en-Bigorre (54) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Vic-en-Bigorre (56) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Larreule (10) ⚠️ | Larreule › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Larreule (39) ⚠️ | Larreule › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Larreule (40) ⚠️ | Larreule › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Nouilhan ⚠️ | Nouilhan › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Vic-en-Bigorre (61) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Liac (5) ⚠️ | Artagnan › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Maubourguet (11) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Maubourguet (5) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Maubourguet (6) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Sarriac-Bigorre (12) ⚠️ | Sarriac-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Sarriac-Bigorre (15) ⚠️ | Sarriac-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Gensac (5) ⚠️ | Gensac › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Monfaucon (20) ⚠️ | Monfaucon › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Auriébat (5) ⚠️ | Auriébat › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Maubourguet (23) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Maubourguet (36) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Maubourguet (8) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Maubourguet (68) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Maubourguet (83) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Maubourguet (11) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Labatut-Rivière (4) ⚠️ | Labatut-Rivière › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Sombrun (7) ⚠️ | Sombrun › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Sombrun (8) ⚠️ | Sombrun › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Maubourguet (13) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Hagedet (2) ⚠️ | Hagedet › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Parc de Lascazères ⚠️ | Lascazères › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Caussade-Rivière (6) ⚠️ | Caussade-Rivière › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Caussade-Rivière (12) ⚠️ | Caussade-Rivière › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Caussade-Rivière (13) ⚠️ | Caussade-Rivière › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Labatut-Rivière (8) ⚠️ | Hères › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Madiran (7) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Madiran (9) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Saint-Lanne (11) ⚠️ | Saint-Lanne › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Madiran (30) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Saint-Lanne (24) ⚠️ | Saint-Lanne › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Saint-Lanne (6) ⚠️ | Saint-Lanne › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Saint-Lanne (7) ⚠️ | Saint-Lanne › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Castelnau-Rivière-Basse (12) ⚠️ | Castelnau-Rivière-Basse › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Hères (13) ⚠️ | Hères › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Hères (7) ⚠️ | Hères › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Lourdes (132) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 2 |
| Bois de Viey (13) ⚠️ | Viey › Pyrénées Vallées des Gaves | 2 |
| Forêt de Cauterets (659) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 2 |
| Forêt de Arrens-Marsous (224) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 2 |
| Forêt de Estaing (121) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 2 |
| Bois de Pierrefitte-Nestalas (17) ⚠️ | Pierrefitte-Nestalas › Pyrénées Vallées des Gaves | 2 |
| Bois de Agos-Vidalos (46) ⚠️ | Agos-Vidalos › Pyrénées Vallées des Gaves | 2 |
| Forêt de Luz-Saint-Sauveur (33) ⚠️ | Luz-Saint-Sauveur › Pyrénées Vallées des Gaves | 2 |
| Bois de Lourdes (62) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Peyrouse (40) ⚠️ | Peyrouse › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Gazost (30) ⚠️ | Gazost › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Gazost (36) ⚠️ | Gazost › Tarbes-Lourdes-Pyrénées | 2 |
| Bois de Ayros-Arbouix (33) ⚠️ | Ayros-Arbouix › Pyrénées Vallées des Gaves | 2 |
| Forêt de Barèges (203) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 2 |
| Bois de Saint-Lary-Soulan (30) ⚠️ | Saint-Lary-Soulan › Aure Louron | 2 |
| Forêt de Capvern (200) ⚠️ | Capvern › Plateau de Lannemezan | 2 |
| Bois de Barèges (56) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 2 |
| Bois de Barèges (64) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 2 |
| Bois de Betpouey (18) ⚠️ | Betpouey › Pyrénées Vallées des Gaves | 2 |
| Bois de Orincles (5) ⚠️ | Orincles › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Loucrup (35) ⚠️ | Loucrup › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Saint-Pé-de-Bigorre (68) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Ossun-ez-Angles (13) ⚠️ | Ossun-ez-Angles › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Labassère (59) ⚠️ | Labassère › Haute-Bigorre | 2 |
| Bois de Vieuzos (25) ⚠️ | Vieuzos › Pays de Trie et du Magnoac | 2 |
| Bois de Puntous (37) ⚠️ | Puntous › Pays de Trie et du Magnoac | 2 |
| Bois de Guizerix (43) ⚠️ | Guizerix › Pays de Trie et du Magnoac | 2 |
| Bois de Labatut-Rivière (48) ⚠️ | Labatut-Rivière › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Ancizan (35) ⚠️ | Ancizan › Aure Louron | 2 |
| Bois de Hères (28) ⚠️ | Hères › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Madiran (17) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Séron (7) ⚠️ | Séron › Tarbes-Lourdes-Pyrénées | 2 |
| Bois de Oursbelille (15) ⚠️ | Oursbelille › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Ibos (108) ⚠️ | Ibos › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Arras-en-Lavedan (74) ⚠️ | Arras-en-Lavedan › Pyrénées Vallées des Gaves | 2 |
| Bois de Oursbelille (16) ⚠️ | Oursbelille › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Beaudéan (34) ⚠️ | Beaudéan › Haute-Bigorre | 2 |
| Forêt de Arcizans-Avant (37) ⚠️ | Arcizans-Avant › Pyrénées Vallées des Gaves | 2 |
| Bois de Viger (32) ⚠️ | Viger › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Arrens-Marsous (253) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 2 |
| Forêt de Arrens-Marsous (256) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 2 |
| Forêt de Cauterets (686) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 2 |
| Forêt de Oursbelille (23) ⚠️ | Oursbelille › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Campan (309) ⚠️ | Campan › Haute-Bigorre | 2 |
| Forêt de Poueyferré (64) ⚠️ | Poueyferré › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Ossun (67) ⚠️ | Ossun › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Bénac (29) ⚠️ | Bénac › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Ibos (111) ⚠️ | Ibos › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Ibos (114) ⚠️ | Ibos › Tarbes-Lourdes-Pyrénées | 2 |
| Bois de Barbazan-Debat (8) ⚠️ | Barbazan-Debat › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Vielle-Adour (29) ⚠️ | Vielle-Adour › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Mascaras (27) ⚠️ | Mascaras › Coteaux du Val-d'Arros | 2 |
| Forêt de Esparros (79) ⚠️ | Esparros › Plateau de Lannemezan | 2 |
| Forêt de Labastide (50) ⚠️ | Labastide › Plateau de Lannemezan | 2 |
| Forêt de Capvern (205) ⚠️ | Capvern › Plateau de Lannemezan | 2 |
| Forêt de Ozon (56) ⚠️ | Ozon › Coteaux du Val-d'Arros | 2 |
| Bois de Laméac (11) ⚠️ | Laméac › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Saint-Sever-de-Rustan (10) ⚠️ | Saint-Sever-de-Rustan › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Dours (14) ⚠️ | Dours › Coteaux du Val-d'Arros | 2 |
| Forêt de Campistrous (28) ⚠️ | Campistrous › Plateau de Lannemezan | 2 |
| Bois de Lannemezan (212) ⚠️ | Lannemezan › Plateau de Lannemezan | 2 |
| Bois de Lannemezan (213) ⚠️ | Lannemezan › Plateau de Lannemezan | 2 |
| Forêt de Libaros (10) ⚠️ | Libaros › Plateau de Lannemezan | 2 |
| Forêt de Puydarrieux (14) ⚠️ | Puydarrieux › Pays de Trie et du Magnoac | 2 |
| Forêt de Cizos (13) ⚠️ | Cizos › Pays de Trie et du Magnoac | 2 |
| Bois de Monléon-Magnoac (114) ⚠️ | Monléon-Magnoac › Pays de Trie et du Magnoac | 2 |
| Bois de Aries-Espénan (30) ⚠️ | Aries-Espénan › Pays de Trie et du Magnoac | 2 |
| Bois de Aries-Espénan (31) ⚠️ | Aries-Espénan › Pays de Trie et du Magnoac | 2 |
| Forêt de Sariac-Magnoac (5) ⚠️ | Sariac-Magnoac › Pays de Trie et du Magnoac | 2 |
| Bois de Cantaous (82) ⚠️ | Escala › Plateau de Lannemezan | 2 |
| Forêt de Tuzaguet (9) ⚠️ | Tuzaguet › Neste Barousse | 2 |
| Bois de Anla (24) ⚠️ | Anla › Neste Barousse | 2 |
| Bois de Troubat (14) ⚠️ | Troubat › Neste Barousse | 2 |
| Forêt de Saléchan (2) ⚠️ | Saléchan › Neste Barousse | 2 |
| Bois de Esbareich (41) ⚠️ | Esbareich › Neste Barousse | 2 |
| Forêt de Ferrère (85) ⚠️ | Ferrère › Neste Barousse | 2 |
| Forêt de Tuzaguet (12) ⚠️ | Tuzaguet › Neste Barousse | 2 |
| Bois de Hèches (100) ⚠️ | Hèches › Plateau de Lannemezan | 2 |
| Forêt de Vielle-Louron (11) ⚠️ | Vielle-Louron › Aure Louron | 2 |
| Forêt de Loudervielle (44) ⚠️ | Loudervielle › Aure Louron | 2 |
| Forêt de Loudenvielle (78) ⚠️ | Loudenvielle › Aure Louron | 2 |
| Forêt de Loudenvielle (80) ⚠️ | Loudenvielle › Aure Louron | 2 |
| Bois de Ancizan (20) ⚠️ | Ancizan › Aure Louron | 2 |
| Forêt de Tramezaïgues (104) ⚠️ | Saint-Lary-Soulan › Aure Louron | 2 |
| Forêt de Cadeilhan-Trachère (35) ⚠️ | Cadeilhan-Trachère › Aure Louron | 2 |
| Forêt de Tarasteix (16) ⚠️ | Tarasteix › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Caixon (28) ⚠️ | Caixon › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Monfaucon (11) ⚠️ | Monfaucon › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Monfaucon (87) ⚠️ | Monfaucon › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Lascazères (37) ⚠️ | Lascazères › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Madiran (51) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Madiran (52) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Castelnau-Rivière-Basse (49) ⚠️ | Castelnau-Rivière-Basse › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Bois de Castelnau-Rivière-Basse (53) ⚠️ | Castelnau-Rivière-Basse › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Ferrières (42) ⚠️ | Ferrières › Pays de Nay (Hautes-Pyrénées) | 2 |
| Forêt de Oursbelille (24) ⚠️ | Oursbelille › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Bours (39) ⚠️ | Bours › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Sarriac-Bigorre (15) ⚠️ | Sarriac-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 2 |
| Forêt de Arrens-Marsous (259) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 2 |
| Forêt de Arrens-Marsous (264) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 2 |
| Forêt de Préchac (11) ⚠️ | Préchac › Pyrénées Vallées des Gaves | 2 |
| Bois de Agos-Vidalos (65) ⚠️ | Agos-Vidalos › Pyrénées Vallées des Gaves | 2 |
| Bois de Aspin-en-Lavedan (26) ⚠️ | Aspin-en-Lavedan › Tarbes-Lourdes-Pyrénées | 2 |
| Bois de Lourdes (126) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Saint-Pé-de-Bigorre (73) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Artalens-Souin (49) ⚠️ | Artalens-Souin › Pyrénées Vallées des Gaves | 2 |
| Forêt des Angles (17) ⚠️ | Les Angles › Tarbes-Lourdes-Pyrénées | 2 |
| Bois de Bourréac (6) ⚠️ | Arcizac-ez-Angles › Tarbes-Lourdes-Pyrénées | 2 |
| Forêt de Montgaillard (63) ⚠️ | Montgaillard › Haute-Bigorre | 2 |
| Bois de Lourdes (129) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 2 |
| Parc du Casino ⚠️ | Argelès-Gazost › Pyrénées Vallées des Gaves | 2 |
| Bois de Larreule ⚠️ | Larreule › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Bazordan ⚠️ | Bazordan › Pays de Trie et du Magnoac | 1 |
| Forêt de Ossun (2) ⚠️ | Ossun › Tarbes-Lourdes-Pyrénées | 1 |
| Place des Tilleuls ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bordères-sur-l'Échez ⚠️ | Bordères-sur-l'Échez › Tarbes-Lourdes-Pyrénées | 1 |
| Parc de Tarasteix ⚠️ | Tarasteix › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Parc Chastellain ⚠️ | Tarbes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Camalès ⚠️ | Camalès › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vic-en-Bigorre (7) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vic-en-Bigorre (8) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Place Comte Henri Russel ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Gardères (2) ⚠️ | Gardères › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Nouilhan ⚠️ | Nouilhan › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Maubourguet ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Maubourguet (2) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Larreule (3) ⚠️ | Larreule › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Larreule (4) ⚠️ | Larreule › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vidouze ⚠️ | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Caixon (2) ⚠️ | Caixon › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Andrest ⚠️ | Andrest › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Gayan ⚠️ | Gayan › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Oursbelille ⚠️ | Oursbelille › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Oursbelille (4) ⚠️ | Oursbelille › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Saint-Lanne ⚠️ | Saint-Lanne › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Madiran (5) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Saint-Lanne (2) ⚠️ | Saint-Lanne › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Vidouze (2) ⚠️ | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Escaunets ⚠️ | Escaunets › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Escaunets (4) ⚠️ | Escaunets › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Ibos (3) ⚠️ | Ibos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Ibos (5) ⚠️ | Ibos › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Vic-en-Bigorre (9) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Argelès-Gazost (2) ⚠️ | Argelès-Gazost › Pyrénées Vallées des Gaves | 1 |
| Forêt de Sère-en-Lavedan ⚠️ | Sère-en-Lavedan › Pyrénées Vallées des Gaves | 1 |
| Forêt de Salles (4) ⚠️ | Salles › Pyrénées Vallées des Gaves | 1 |
| Bois de Salles ⚠️ | Salles › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arrens-Marsous (8) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arrens-Marsous (9) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arrens-Marsous (11) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Aucun (2) ⚠️ | Aucun › Pyrénées Vallées des Gaves | 1 |
| Forêt de Tarasteix (5) ⚠️ | Tarasteix › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Parc de Vielle-Aure ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Forêt de Laloubère ⚠️ | Soues › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Vic-en-Bigorre (12) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Sarriac-Bigorre ⚠️ | Sarriac-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Gavarnie-Gèdre (6) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (7) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (9) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Hagedet ⚠️ | Hagedet › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Saint-Lanne (4) ⚠️ | Saint-Lanne › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Arrens-Marsous (14) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gazost (5) ⚠️ | Gazost › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Gazost (12) ⚠️ | Gazost › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Gazost (14) ⚠️ | Gazost › Tarbes-Lourdes-Pyrénées | 1 |
| Parc de Campan ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Beaudéan ⚠️ | Beaudéan › Haute-Bigorre | 1 |
| Forêt de Beaudéan (3) ⚠️ | Beaudéan › Haute-Bigorre | 1 |
| Forêt de Beaudéan (4) ⚠️ | Beaudéan › Haute-Bigorre | 1 |
| Bois de Beaudéan ⚠️ | Beaudéan › Haute-Bigorre | 1 |
| Forêt de Bagnères-de-Bigorre (5) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Beaudéan (7) ⚠️ | Beaudéan › Haute-Bigorre | 1 |
| Forêt de Beaudéan (8) ⚠️ | Beaudéan › Haute-Bigorre | 1 |
| Forêt de Campan (7) ⚠️ | Campan › Haute-Bigorre | 1 |
| Bois de Beaudéan (3) ⚠️ | Beaudéan › Haute-Bigorre | 1 |
| Forêt de Barèges (7) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Forêt de Barèges (13) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Forêt de Bun (3) ⚠️ | Bun › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arcizans-Dessus (2) ⚠️ | Arras-en-Lavedan › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arras-en-Lavedan (3) ⚠️ | Arras-en-Lavedan › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arras-en-Lavedan (4) ⚠️ | Arras-en-Lavedan › Pyrénées Vallées des Gaves | 1 |
| Forêt de Lau-Balagnas (2) ⚠️ | Lau-Balagnas › Pyrénées Vallées des Gaves | 1 |
| Forêt de Saint-Savin ⚠️ | Saint-Savin › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arras-en-Lavedan (9) ⚠️ | Arras-en-Lavedan › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arras-en-Lavedan (10) ⚠️ | Arras-en-Lavedan › Pyrénées Vallées des Gaves | 1 |
| Forêt de Siarrouy (5) ⚠️ | Siarrouy › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Siarrouy (8) ⚠️ | Siarrouy › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Talazac (2) ⚠️ | Talazac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Saint-Lézer (7) ⚠️ | Saint-Lézer › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Oursbelille (6) ⚠️ | Oursbelille › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Agos-Vidalos (3) ⚠️ | Agos-Vidalos › Pyrénées Vallées des Gaves | 1 |
| Forêt de Salles (6) ⚠️ | Salles › Pyrénées Vallées des Gaves | 1 |
| Bois de Salles (2) ⚠️ | Salles › Pyrénées Vallées des Gaves | 1 |
| Bois de Salles (4) ⚠️ | Salles › Pyrénées Vallées des Gaves | 1 |
| Bois de Salles (6) ⚠️ | Salles › Pyrénées Vallées des Gaves | 1 |
| Bois de Ouzous (11) ⚠️ | Ouzous › Pyrénées Vallées des Gaves | 1 |
| Bois de Ayzac-Ost (3) ⚠️ | Ayzac-Ost › Pyrénées Vallées des Gaves | 1 |
| Bois de Ouzous (12) ⚠️ | Ouzous › Pyrénées Vallées des Gaves | 1 |
| Bois de Ayzac-Ost (5) ⚠️ | Ayzac-Ost › Pyrénées Vallées des Gaves | 1 |
| Forêt de Lugagnan ⚠️ | Lugagnan › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Geu (4) ⚠️ | Geu › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Berbérust-Lias (2) ⚠️ | Berbérust-Lias › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Berbérust-Lias (10) ⚠️ | Berbérust-Lias › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Berbérust-Lias (11) ⚠️ | Berbérust-Lias › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Berbérust-Lias (13) ⚠️ | Berbérust-Lias › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Ayzac-Ost (6) ⚠️ | Ayzac-Ost › Pyrénées Vallées des Gaves | 1 |
| Bois de Ayzac-Ost (11) ⚠️ | Ayzac-Ost › Pyrénées Vallées des Gaves | 1 |
| Bois de Ayzac-Ost (12) ⚠️ | Ayzac-Ost › Pyrénées Vallées des Gaves | 1 |
| Forêt de Ayros-Arbouix (4) ⚠️ | Ayros-Arbouix › Pyrénées Vallées des Gaves | 1 |
| Bois de Boô-Silhen (15) ⚠️ | Boô-Silhen › Pyrénées Vallées des Gaves | 1 |
| Forêt de Ayros-Arbouix (6) ⚠️ | Ayros-Arbouix › Pyrénées Vallées des Gaves | 1 |
| Bois de Saint-Pastous (11) ⚠️ | Saint-Pastous › Pyrénées Vallées des Gaves | 1 |
| Bois de Boô-Silhen (19) ⚠️ | Boô-Silhen › Pyrénées Vallées des Gaves | 1 |
| Bois de Boô-Silhen (26) ⚠️ | Boô-Silhen › Pyrénées Vallées des Gaves | 1 |
| Bois de Ayros-Arbouix (3) ⚠️ | Ayros-Arbouix › Pyrénées Vallées des Gaves | 1 |
| Forêt de Ayros-Arbouix (12) ⚠️ | Ayros-Arbouix › Pyrénées Vallées des Gaves | 1 |
| Bois de Boô-Silhen (28) ⚠️ | Boô-Silhen › Pyrénées Vallées des Gaves | 1 |
| Forêt de Ayros-Arbouix (14) ⚠️ | Ayros-Arbouix › Pyrénées Vallées des Gaves | 1 |
| Forêt de Vier-Bordes (2) ⚠️ | Vier-Bordes › Pyrénées Vallées des Gaves | 1 |
| Forêt de Artalens-Souin ⚠️ | Artalens-Souin › Pyrénées Vallées des Gaves | 1 |
| Forêt de Berbérust-Lias (20) ⚠️ | Berbérust-Lias › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Lau-Balagnas (3) ⚠️ | Lau-Balagnas › Pyrénées Vallées des Gaves | 1 |
| Bois de Lau-Balagnas (5) ⚠️ | Lau-Balagnas › Pyrénées Vallées des Gaves | 1 |
| Bois de Vic-en-Bigorre (11) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Bagnères-de-Bigorre (11) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Bagnères-de-Bigorre (12) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Bagnères-de-Bigorre (13) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Bagnères-de-Bigorre (15) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Bois de Campan (2) ⚠️ | Campan › Haute-Bigorre | 1 |
| Bois de Vier-Bordes (2) ⚠️ | Vier-Bordes › Pyrénées Vallées des Gaves | 1 |
| Bois de Vier-Bordes (3) ⚠️ | Vier-Bordes › Pyrénées Vallées des Gaves | 1 |
| Bois de Lugagnan (5) ⚠️ | Lugagnan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Aspin-en-Lavedan ⚠️ | Aspin-en-Lavedan › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Aspin-en-Lavedan ⚠️ | Aspin-en-Lavedan › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Aspin-en-Lavedan (11) ⚠️ | Aspin-en-Lavedan › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Ossen (6) ⚠️ | Ossen › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Ossen (9) ⚠️ | Ossen › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Ossen (10) ⚠️ | Ossen › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Ossen (11) ⚠️ | Ossen › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Ségus (3) ⚠️ | Ségus › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Omex (3) ⚠️ | Omex › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Ségus (6) ⚠️ | Ségus › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Ségus (12) ⚠️ | Ségus › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Omex (10) ⚠️ | Omex › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Ségus (28) ⚠️ | Ségus › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Omex (20) ⚠️ | Omex › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Ségus (29) ⚠️ | Omex › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Omex (21) ⚠️ | Omex › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Omex (29) ⚠️ | Omex › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lourdes (7) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Saint-Créac (2) ⚠️ | Saint-Créac › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Saint-Créac (15) ⚠️ | Saint-Créac › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Saint-Créac (16) ⚠️ | Saint-Créac › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Jarret (19) ⚠️ | Jarret › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Jarret (20) ⚠️ | Jarret › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Juncalas (2) ⚠️ | Juncalas › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Ousté (3) ⚠️ | Ousté › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Juncalas (4) ⚠️ | Juncalas › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Juncalas (4) ⚠️ | Cheust › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Cheust (3) ⚠️ | Cheust › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Cheust (4) ⚠️ | Cheust › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Cheust (9) ⚠️ | Cheust › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Gazost (5) ⚠️ | Gazost › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Gazost (19) ⚠️ | Gazost › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Arrodets-ez-Angles ⚠️ | Arrodets-ez-Angles › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Cheust (6) ⚠️ | Cheust › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Ourdis-Cotdoussan (2) ⚠️ | Ourdis-Cotdoussan › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Germs-sur-l'Oussouet (7) ⚠️ | Germs-sur-l'Oussouet › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Germs-sur-l'Oussouet (12) ⚠️ | Germs-sur-l'Oussouet › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Germs-sur-l'Oussouet (15) ⚠️ | Germs-sur-l'Oussouet › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Ourdis-Cotdoussan (12) ⚠️ | Germs-sur-l'Oussouet › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Germs-sur-l'Oussouet (18) ⚠️ | Germs-sur-l'Oussouet › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Germs-sur-l'Oussouet (19) ⚠️ | Germs-sur-l'Oussouet › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Juncalas (23) ⚠️ | Juncalas › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Germs-sur-l'Oussouet (7) ⚠️ | Germs-sur-l'Oussouet › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Labassère (3) ⚠️ | Labassère › Haute-Bigorre | 1 |
| Forêt de Bagnères-de-Bigorre (21) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Bagnères-de-Bigorre (24) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Bois de Germs-sur-l'Oussouet (41) ⚠️ | Germs-sur-l'Oussouet › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Bagnères-de-Bigorre (5) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Bois de Bagnères-de-Bigorre (24) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Sère-Lanso (13) ⚠️ | Sère-Lanso › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Sère-Lanso (16) ⚠️ | Sère-Lanso › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Arrodets-ez-Angles (2) ⚠️ | Arrodets-ez-Angles › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Arcizac-ez-Angles ⚠️ | Les Angles › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Arcizac-ez-Angles (2) ⚠️ | Les Angles › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lourdes (15) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Poueyferré ⚠️ | Poueyferré › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Saint-Pé-de-Bigorre (9) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lourdes (27) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lourdes (33) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lourdes (40) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Aucun (6) ⚠️ | Aucun › Pyrénées Vallées des Gaves | 1 |
| Forêt de Aucun (9) ⚠️ | Aucun › Pyrénées Vallées des Gaves | 1 |
| Bois de Arrens-Marsous (2) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arrens-Marsous (26) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arrens-Marsous (31) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arrens-Marsous (53) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arrens-Marsous (57) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arrens-Marsous (59) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arrens-Marsous (60) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arrens-Marsous (87) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arrens-Marsous (92) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arrens-Marsous (98) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arrens-Marsous (101) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arrens-Marsous (105) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arrens-Marsous (107) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arrens-Marsous (110) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arrens-Marsous (114) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Bois de Arrens-Marsous (14) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Estaing (16) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 1 |
| Forêt de Estaing (27) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 1 |
| Forêt de Estaing (29) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 1 |
| Forêt de Estaing (42) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 1 |
| Forêt de Estaing (43) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 1 |
| Forêt de Estaing (44) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 1 |
| Forêt de Estaing (53) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 1 |
| Forêt de Estaing (67) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 1 |
| Forêt de Estaing (74) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 1 |
| Forêt de Estaing (76) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 1 |
| Forêt de Estaing (85) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 1 |
| Forêt de Estaing (87) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 1 |
| Forêt de Estaing (90) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 1 |
| Forêt de Estaing (91) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 1 |
| Forêt de Estaing (92) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arrens-Marsous (129) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arrens-Marsous (133) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gaillagos (11) ⚠️ | Gaillagos › Pyrénées Vallées des Gaves | 1 |
| Forêt de Aucun (32) ⚠️ | Aucun › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arrens-Marsous (142) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arcizans-Dessus (14) ⚠️ | Arcizans-Dessus › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arcizans-Dessus (18) ⚠️ | Arcizans-Dessus › Pyrénées Vallées des Gaves | 1 |
| Forêt de Aucun (59) ⚠️ | Aucun › Pyrénées Vallées des Gaves | 1 |
| Forêt de Bun (24) ⚠️ | Bun › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arras-en-Lavedan (13) ⚠️ | Arras-en-Lavedan › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arras-en-Lavedan (29) ⚠️ | Arras-en-Lavedan › Pyrénées Vallées des Gaves | 1 |
| Forêt de Saint-Savin (13) ⚠️ | Saint-Savin › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arras-en-Lavedan (59) ⚠️ | Arras-en-Lavedan › Pyrénées Vallées des Gaves | 1 |
| Forêt de Préchac (5) ⚠️ | Préchac › Pyrénées Vallées des Gaves | 1 |
| Bois de Préchac (14) ⚠️ | Préchac › Pyrénées Vallées des Gaves | 1 |
| Bois de Préchac (21) ⚠️ | Préchac › Pyrénées Vallées des Gaves | 1 |
| Forêt de Vier-Bordes (5) ⚠️ | Vier-Bordes › Pyrénées Vallées des Gaves | 1 |
| Bois de Beaucens (23) ⚠️ | Beaucens › Pyrénées Vallées des Gaves | 1 |
| Forêt de Vier-Bordes (15) ⚠️ | Vier-Bordes › Pyrénées Vallées des Gaves | 1 |
| Forêt de Artalens-Souin (20) ⚠️ | Artalens-Souin › Pyrénées Vallées des Gaves | 1 |
| Forêt de Artalens-Souin (23) ⚠️ | Artalens-Souin › Pyrénées Vallées des Gaves | 1 |
| Forêt de Vier-Bordes (25) ⚠️ | Vier-Bordes › Pyrénées Vallées des Gaves | 1 |
| Bois de Beaucens (39) ⚠️ | Beaucens › Pyrénées Vallées des Gaves | 1 |
| Bois de Beaucens (43) ⚠️ | Beaucens › Pyrénées Vallées des Gaves | 1 |
| Bois de Beaucens (51) ⚠️ | Beaucens › Pyrénées Vallées des Gaves | 1 |
| Bois de Beaucens (56) ⚠️ | Beaucens › Pyrénées Vallées des Gaves | 1 |
| Bois de Beaucens (62) ⚠️ | Préchac › Pyrénées Vallées des Gaves | 1 |
| Forêt de Beaucens (23) ⚠️ | Beaucens › Pyrénées Vallées des Gaves | 1 |
| Forêt de Beaucens (29) ⚠️ | Beaucens › Pyrénées Vallées des Gaves | 1 |
| Forêt de Beaucens (34) ⚠️ | Beaucens › Pyrénées Vallées des Gaves | 1 |
| Forêt de Beaucens (35) ⚠️ | Beaucens › Pyrénées Vallées des Gaves | 1 |
| Bois de Beaucens (67) ⚠️ | Beaucens › Pyrénées Vallées des Gaves | 1 |
| Forêt de Villelongue (17) ⚠️ | Villelongue › Pyrénées Vallées des Gaves | 1 |
| Forêt de Villelongue (19) ⚠️ | Villelongue › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (7) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (14) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (19) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Bois de Arras-en-Lavedan (9) ⚠️ | Arras-en-Lavedan › Pyrénées Vallées des Gaves | 1 |
| Forêt de Viscos ⚠️ | Viscos › Pyrénées Vallées des Gaves | 1 |
| Forêt de Saligos (9) ⚠️ | Saligos › Pyrénées Vallées des Gaves | 1 |
| Forêt de Chèze (8) ⚠️ | Chèze › Pyrénées Vallées des Gaves | 1 |
| Forêt de Chèze (10) ⚠️ | Chèze › Pyrénées Vallées des Gaves | 1 |
| Forêt de Saligos (17) ⚠️ | Saligos › Pyrénées Vallées des Gaves | 1 |
| Forêt de Esquièze-Sère (5) ⚠️ | Esquièze-Sère › Pyrénées Vallées des Gaves | 1 |
| Forêt de Sazos (10) ⚠️ | Sazos › Pyrénées Vallées des Gaves | 1 |
| Forêt de Grust (11) ⚠️ | Grust › Pyrénées Vallées des Gaves | 1 |
| Forêt de Grust (12) ⚠️ | Grust › Pyrénées Vallées des Gaves | 1 |
| Forêt de Sazos (18) ⚠️ | Sazos › Pyrénées Vallées des Gaves | 1 |
| Forêt de Grust (19) ⚠️ | Grust › Pyrénées Vallées des Gaves | 1 |
| Forêt de Sazos (25) ⚠️ | Sazos › Pyrénées Vallées des Gaves | 1 |
| Forêt de Sazos (31) ⚠️ | Sazos › Pyrénées Vallées des Gaves | 1 |
| Forêt de Luz-Saint-Sauveur (4) ⚠️ | Luz-Saint-Sauveur › Pyrénées Vallées des Gaves | 1 |
| Parc de Luz-Saint-Sauveur (2) ⚠️ | Luz-Saint-Sauveur › Pyrénées Vallées des Gaves | 1 |
| Forêt de Luz-Saint-Sauveur (21) ⚠️ | Luz-Saint-Sauveur › Pyrénées Vallées des Gaves | 1 |
| Forêt de Saligos (24) ⚠️ | Saligos › Pyrénées Vallées des Gaves | 1 |
| Forêt de Viey ⚠️ | Viey › Pyrénées Vallées des Gaves | 1 |
| Forêt de Esterre (2) ⚠️ | Esterre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Viey (2) ⚠️ | Viey › Pyrénées Vallées des Gaves | 1 |
| Forêt de Viey (10) ⚠️ | Viey › Pyrénées Vallées des Gaves | 1 |
| Forêt de Viey (12) ⚠️ | Viey › Pyrénées Vallées des Gaves | 1 |
| Forêt de Viey (13) ⚠️ | Viey › Pyrénées Vallées des Gaves | 1 |
| Forêt de Viella (8) ⚠️ | Viella › Pyrénées Vallées des Gaves | 1 |
| Forêt de Viella (10) ⚠️ | Viella › Pyrénées Vallées des Gaves | 1 |
| Forêt de Betpouey (11) ⚠️ | Betpouey › Pyrénées Vallées des Gaves | 1 |
| Bois de Viella (3) ⚠️ | Viella › Pyrénées Vallées des Gaves | 1 |
| Forêt de Sers (26) ⚠️ | Sers › Pyrénées Vallées des Gaves | 1 |
| Forêt de Sers (35) ⚠️ | Sers › Pyrénées Vallées des Gaves | 1 |
| Forêt de Sers (40) ⚠️ | Sers › Pyrénées Vallées des Gaves | 1 |
| Forêt de Sers (44) ⚠️ | Sers › Pyrénées Vallées des Gaves | 1 |
| Forêt de Sers (49) ⚠️ | Sers › Pyrénées Vallées des Gaves | 1 |
| Forêt de Sers (50) ⚠️ | Sers › Pyrénées Vallées des Gaves | 1 |
| Forêt de Sers (53) ⚠️ | Sers › Pyrénées Vallées des Gaves | 1 |
| Forêt de Sers (54) ⚠️ | Sers › Pyrénées Vallées des Gaves | 1 |
| Forêt de Sers (57) ⚠️ | Sers › Pyrénées Vallées des Gaves | 1 |
| Forêt de Sers (71) ⚠️ | Sers › Pyrénées Vallées des Gaves | 1 |
| Forêt de Barèges (21) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Forêt de Barèges (26) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Forêt de Barèges (28) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Forêt de Barèges (30) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Forêt de Barèges (34) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Forêt de Saint-Lary-Soulan (2) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Vielle-Aure (22) ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Forêt de Vielle-Aure (25) ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (5) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Vielle-Aure (44) ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Forêt de Vielle-Aure (45) ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Forêt de Vielle-Aure (51) ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Forêt de Vielle-Aure (52) ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Forêt de Vielle-Aure (58) ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Forêt de Vielle-Aure (61) ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (11) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Vielle-Aure (71) ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Forêt de Vielle-Aure (72) ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Forêt de Vielle-Aure (88) ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Forêt de Barèges (41) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Forêt de Barèges (76) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Forêt de Barèges (87) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Forêt de Barèges (92) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Forêt de Barèges (94) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Forêt de Barèges (97) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Forêt de Barèges (99) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Forêt de Barèges (101) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Forêt de Barèges (103) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Forêt de Barèges (107) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Forêt de Barèges (111) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Bois de Barèges (8) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Forêt de Barèges (112) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Forêt de Barèges (114) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Forêt de Barèges (149) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (15) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Bois de Luquet (4) ⚠️ | Luquet › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Gardères (7) ⚠️ | Gardères › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Luquet (11) ⚠️ | Luquet › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Luquet (13) ⚠️ | Luquet › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Arrens-Marsous (155) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Luz-Saint-Sauveur (25) ⚠️ | Luz-Saint-Sauveur › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (26) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (42) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (62) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (66) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Bois de Gavarnie-Gèdre (2) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (69) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Bois de Gavarnie-Gèdre (7) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (74) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Bois de Gavarnie-Gèdre (11) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (85) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (87) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (90) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (107) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (112) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (114) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (116) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (121) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (123) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (125) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (162) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (172) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (189) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (193) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (204) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (208) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (211) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (215) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (218) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (219) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (220) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (269) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (270) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (293) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (296) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gardères (11) ⚠️ | Gardères › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Gardères (12) ⚠️ | Gardères › Tarbes-Lourdes-Pyrénées | 1 |
| Parc des Bois Blancs ⚠️ | Tarbes › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Cauterets (3) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (39) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (67) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (68) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Bois de Cauterets (9) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (80) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (97) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (115) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (136) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (137) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (142) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (150) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (151) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (153) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (159) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (163) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (164) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (165) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (171) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (172) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (173) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (175) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (176) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (178) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (220) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (225) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (226) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (229) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (265) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (278) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (294) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (297) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (299) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (304) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (332) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (335) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (337) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (342) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (344) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (348) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (349) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (350) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (351) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (353) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (354) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (355) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (367) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (369) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (374) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (382) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (388) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (392) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (409) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (417) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (423) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (424) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (425) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (430) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (434) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (446) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (453) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (454) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (457) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (460) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (473) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (483) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (488) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (495) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (496) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (499) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (505) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (510) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (511) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (520) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (522) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (540) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arrens-Marsous (173) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arrens-Marsous (174) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arrens-Marsous (185) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arrens-Marsous (188) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Germ (6) ⚠️ | Germ › Aure Louron | 1 |
| Forêt de Estaing (114) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (548) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (549) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (551) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (552) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (568) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (569) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (582) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (587) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (591) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (592) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (608) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (609) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (613) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (617) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Luz-Saint-Sauveur (28) ⚠️ | Luz-Saint-Sauveur › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (619) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (630) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (637) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arbéost (3) ⚠️ | Arbéost › Pays de Nay (Hautes-Pyrénées) | 1 |
| Forêt de Arbéost (5) ⚠️ | Arbéost › Pays de Nay (Hautes-Pyrénées) | 1 |
| Forêt de Arbéost (8) ⚠️ | Arbéost › Pays de Nay (Hautes-Pyrénées) | 1 |
| Forêt de Arbéost (33) ⚠️ | Arbéost › Pays de Nay (Hautes-Pyrénées) | 1 |
| Forêt de Arbéost (36) ⚠️ | Arbéost › Pays de Nay (Hautes-Pyrénées) | 1 |
| Forêt de Arbéost (39) ⚠️ | Arbéost › Pays de Nay (Hautes-Pyrénées) | 1 |
| Forêt de Arbéost (40) ⚠️ | Arbéost › Pays de Nay (Hautes-Pyrénées) | 1 |
| Forêt de Arbéost (44) ⚠️ | Arbéost › Pays de Nay (Hautes-Pyrénées) | 1 |
| Bois de Beyrède-Jumet-Camous (3) ⚠️ | Beyrède-Jumet-Camous › Aure Louron | 1 |
| Forêt de Beyrède-Jumet-Camous ⚠️ | Beyrède-Jumet-Camous › Aure Louron | 1 |
| Bois de Cadéac (3) ⚠️ | Cadéac › Aure Louron | 1 |
| Forêt de Bordères-sur-l'Échez (3) ⚠️ | Bordères-sur-l'Échez › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bordères-sur-l'Échez (5) ⚠️ | Bordères-sur-l'Échez › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Bordères-sur-l'Échez (4) ⚠️ | Bordères-sur-l'Échez › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bordères-sur-l'Échez (10) ⚠️ | Bordères-sur-l'Échez › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Oursbelille (11) ⚠️ | Oursbelille › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bordères-sur-l'Échez (16) ⚠️ | Bordères-sur-l'Échez › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Oursbelille (16) ⚠️ | Oursbelille › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bordères-sur-l'Échez (26) ⚠️ | Bordères-sur-l'Échez › Tarbes-Lourdes-Pyrénées | 1 |
| Park de l'Échez ⚠️ | Tarbes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Tarbes (7) ⚠️ | Tarbes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Beaucens (41) ⚠️ | Beaucens › Pyrénées Vallées des Gaves | 1 |
| Forêt de Bours (2) ⚠️ | Bours › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bordères-sur-l'Échez (33) ⚠️ | Bordères-sur-l'Échez › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bordères-sur-l'Échez (38) ⚠️ | Bordères-sur-l'Échez › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bordères-sur-l'Échez (43) ⚠️ | Bordères-sur-l'Échez › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bours (21) ⚠️ | Bours › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Labassère (13) ⚠️ | Labassère › Haute-Bigorre | 1 |
| Forêt de Labassère (25) ⚠️ | Labassère › Haute-Bigorre | 1 |
| Bois de Labassère (15) ⚠️ | Labassère › Haute-Bigorre | 1 |
| Forêt de Pouzac (2) ⚠️ | Pouzac › Haute-Bigorre | 1 |
| Forêt de Labassère (31) ⚠️ | Labassère › Haute-Bigorre | 1 |
| Forêt de Labassère (36) ⚠️ | Labassère › Haute-Bigorre | 1 |
| Bois de Bagnères-de-Bigorre (25) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Pouzac (8) ⚠️ | Pouzac › Haute-Bigorre | 1 |
| Forêt de Labassère (58) ⚠️ | Labassère › Haute-Bigorre | 1 |
| Bois de Bagnères-de-Bigorre (26) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Trébons (3) ⚠️ | Trébons › Haute-Bigorre | 1 |
| Forêt de Bagnères-de-Bigorre (37) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Bagnères-de-Bigorre (42) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Bagnères-de-Bigorre (44) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Bagnères-de-Bigorre (47) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Pouzac (18) ⚠️ | Pouzac › Haute-Bigorre | 1 |
| Forêt de Bagnères-de-Bigorre (55) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Pouzac (27) ⚠️ | Pouzac › Haute-Bigorre | 1 |
| Forêt de Ordizan ⚠️ | Ordizan › Haute-Bigorre | 1 |
| Forêt de Pouzac (37) ⚠️ | Pouzac › Haute-Bigorre | 1 |
| Forêt de Pouzac (39) ⚠️ | Pouzac › Haute-Bigorre | 1 |
| Forêt de Pouzac (44) ⚠️ | Pouzac › Haute-Bigorre | 1 |
| Forêt de Pouzac (45) ⚠️ | Pouzac › Haute-Bigorre | 1 |
| Forêt de Pouzac (46) ⚠️ | Pouzac › Haute-Bigorre | 1 |
| Forêt de Pouzac (50) ⚠️ | Pouzac › Haute-Bigorre | 1 |
| Bois de Bagnères-de-Bigorre (30) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Bagnères-de-Bigorre (68) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Bagnères-de-Bigorre (78) ⚠️ | Gerde › Haute-Bigorre | 1 |
| Forêt de Gerde (7) ⚠️ | Gerde › Haute-Bigorre | 1 |
| Forêt de Bagnères-de-Bigorre (100) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Bagnères-de-Bigorre (102) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Bagnères-de-Bigorre (106) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Gerde (9) ⚠️ | Gerde › Haute-Bigorre | 1 |
| Forêt de Gerde (14) ⚠️ | Gerde › Haute-Bigorre | 1 |
| Forêt de Mérilheu ⚠️ | Mérilheu › Haute-Bigorre | 1 |
| Forêt de Mérilheu (5) ⚠️ | Mérilheu › Haute-Bigorre | 1 |
| Forêt de Bagnères-de-Bigorre (140) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Asté (5) ⚠️ | Asté › Haute-Bigorre | 1 |
| Forêt de Gerde (19) ⚠️ | Gerde › Haute-Bigorre | 1 |
| Forêt de Gerde (21) ⚠️ | Gerde › Haute-Bigorre | 1 |
| Forêt de Gerde (26) ⚠️ | Gerde › Haute-Bigorre | 1 |
| Forêt de Gerde (27) ⚠️ | Gerde › Haute-Bigorre | 1 |
| Forêt de Gerde (34) ⚠️ | Gerde › Haute-Bigorre | 1 |
| Forêt de Uzer ⚠️ | Uzer › Haute-Bigorre | 1 |
| Forêt de Lies (2) ⚠️ | Lies › Haute-Bigorre | 1 |
| Forêt de Campan (17) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Asté (17) ⚠️ | Asté › Haute-Bigorre | 1 |
| Forêt de Campan (20) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Asté (23) ⚠️ | Asté › Haute-Bigorre | 1 |
| Forêt de Asté (24) ⚠️ | Asté › Haute-Bigorre | 1 |
| Forêt de Asté (25) ⚠️ | Asté › Haute-Bigorre | 1 |
| Parc Bel-Air ⚠️ | Tarbes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Asté (37) ⚠️ | Asté › Haute-Bigorre | 1 |
| Forêt de Campan (31) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (39) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (47) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (50) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (53) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (56) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (58) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (59) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (61) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (63) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (64) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (65) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (67) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (99) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (104) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (105) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (106) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Asté (40) ⚠️ | Asté › Haute-Bigorre | 1 |
| Forêt de Campan (107) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (112) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (119) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (125) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (132) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (146) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (147) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (148) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (155) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (161) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (170) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (177) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Bagnères-de-Bigorre (152) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Bois de Campan (5) ⚠️ | Campan › Haute-Bigorre | 1 |
| Bois de Campan (6) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (204) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (206) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (220) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Asté (44) ⚠️ | Asté › Haute-Bigorre | 1 |
| Forêt de Ancizan (13) ⚠️ | Ancizan › Aure Louron | 1 |
| Forêt de Aspin-Aure (3) ⚠️ | Aspin-Aure › Aure Louron | 1 |
| Forêt de Campan (260) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (263) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Beyrède-Jumet-Camous (3) ⚠️ | Beyrède-Jumet-Camous › Aure Louron | 1 |
| Bois de Beyrède-Jumet-Camous (5) ⚠️ | Beyrède-Jumet-Camous › Aure Louron | 1 |
| Forêt de Sarrancolin (3) ⚠️ | Sarrancolin › Aure Louron | 1 |
| Forêt de Ossun-ez-Angles ⚠️ | Ossun-ez-Angles › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Astugue (9) ⚠️ | Astugue › Haute-Bigorre | 1 |
| Forêt de Astugue (10) ⚠️ | Astugue › Haute-Bigorre | 1 |
| Forêt de Astugue (12) ⚠️ | Astugue › Haute-Bigorre | 1 |
| Forêt de Astugue (13) ⚠️ | Astugue › Haute-Bigorre | 1 |
| Forêt de Astugue (24) ⚠️ | Astugue › Haute-Bigorre | 1 |
| Forêt de Astugue (27) ⚠️ | Astugue › Haute-Bigorre | 1 |
| Forêt de Astugue (30) ⚠️ | Astugue › Haute-Bigorre | 1 |
| Forêt de Astugue (31) ⚠️ | Astugue › Haute-Bigorre | 1 |
| Forêt de Montgaillard (4) ⚠️ | Montgaillard › Haute-Bigorre | 1 |
| Forêt de Loucrup (4) ⚠️ | Loucrup › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Astugue (36) ⚠️ | Astugue › Haute-Bigorre | 1 |
| Forêt de Astugue (37) ⚠️ | Astugue › Haute-Bigorre | 1 |
| Forêt de Montgaillard (10) ⚠️ | Montgaillard › Haute-Bigorre | 1 |
| Forêt de Astugue (39) ⚠️ | Astugue › Haute-Bigorre | 1 |
| Forêt de Astugue (40) ⚠️ | Astugue › Haute-Bigorre | 1 |
| Forêt de Loucrup (7) ⚠️ | Loucrup › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Arrayou-Lahitte (2) ⚠️ | Arrayou-Lahitte › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Astugue (47) ⚠️ | Astugue › Haute-Bigorre | 1 |
| Forêt de Cheust (7) ⚠️ | Cheust › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Arrayou-Lahitte (10) ⚠️ | Arrayou-Lahitte › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Arrayou-Lahitte (17) ⚠️ | Arrayou-Lahitte › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Arrayou-Lahitte (29) ⚠️ | Arrayou-Lahitte › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Arcizac-ez-Angles (3) ⚠️ | Arcizac-ez-Angles › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Gez-ez-Angles (23) ⚠️ | Gez-ez-Angles › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Gez-ez-Angles (24) ⚠️ | Gez-ez-Angles › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Montgaillard (16) ⚠️ | Montgaillard › Haute-Bigorre | 1 |
| Forêt de Trébons (16) ⚠️ | Trébons › Haute-Bigorre | 1 |
| Forêt de Trébons (26) ⚠️ | Trébons › Haute-Bigorre | 1 |
| Forêt de Trébons (29) ⚠️ | Trébons › Haute-Bigorre | 1 |
| Forêt de Ordizan (18) ⚠️ | Ordizan › Haute-Bigorre | 1 |
| Forêt de Ordizan (19) ⚠️ | Ordizan › Haute-Bigorre | 1 |
| Forêt de Trébons (41) ⚠️ | Trébons › Haute-Bigorre | 1 |
| Bois de Bagnères-de-Bigorre (34) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Saint-Pé-de-Bigorre (13) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Saint-Pé-de-Bigorre (16) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Saint-Pé-de-Bigorre (14) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Saint-Pé-de-Bigorre (15) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Saint-Pé-de-Bigorre (31) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Saint-Pé-de-Bigorre (34) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Saint-Pé-de-Bigorre (42) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Saint-Pé-de-Bigorre (43) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Saint-Pé-de-Bigorre (45) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Saint-Pé-de-Bigorre (24) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Saint-Pé-de-Bigorre (62) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Peyrouse (13) ⚠️ | Peyrouse › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Peyrouse (26) ⚠️ | Peyrouse › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Poueyferré (5) ⚠️ | Poueyferré › Tarbes-Lourdes-Pyrénées | 1 |
| Parc de Poueyferré ⚠️ | Poueyferré › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Poueyferré (16) ⚠️ | Poueyferré › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Poueyferré (27) ⚠️ | Poueyferré › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Poueyferré (36) ⚠️ | Poueyferré › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lourdes (49) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Poueyferré (42) ⚠️ | Poueyferré › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Poueyferré (49) ⚠️ | Poueyferré › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Poueyferré (50) ⚠️ | Poueyferré › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bartrès (3) ⚠️ | Bartrès › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lourdes (53) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bartrès (9) ⚠️ | Bartrès › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bartrès (14) ⚠️ | Bartrès › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bartrès (18) ⚠️ | Bartrès › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bartrès (29) ⚠️ | Bartrès › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lourdes (71) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lourdes (76) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lourdes (77) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lourdes (78) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lourdes (79) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lourdes (81) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lourdes (82) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lourdes (83) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lourdes (87) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Parc de Lourdes (2) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bartrès (43) ⚠️ | Bartrès › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lourdes (95) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Lourdes (32) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Lourdes (44) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Adé (4) ⚠️ | Adé › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lourdes (120) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lézignan (3) ⚠️ | Lézignan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lourdes (122) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Julos (2) ⚠️ | Paréac › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Paréac ⚠️ | Paréac › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Paréac (2) ⚠️ | Paréac › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Paréac ⚠️ | Paréac › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Paréac (3) ⚠️ | Paréac › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bourréac (7) ⚠️ | Bourréac › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bourréac (8) ⚠️ | Bourréac › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Paréac (5) ⚠️ | Paréac › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Julos (20) ⚠️ | Julos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Julos (22) ⚠️ | Julos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Julos (23) ⚠️ | Julos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Julos (32) ⚠️ | Julos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Julos (42) ⚠️ | Julos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Julos (43) ⚠️ | Julos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Julos (44) ⚠️ | Julos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Julos (45) ⚠️ | Julos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Julos (49) ⚠️ | Julos › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Orincles ⚠️ | Orincles › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Paréac (4) ⚠️ | Paréac › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Paréac (7) ⚠️ | Paréac › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Adé (9) ⚠️ | Adé › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Adé (11) ⚠️ | Adé › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Averan ⚠️ | Averan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Adé (26) ⚠️ | Adé › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lanne ⚠️ | Lanne › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Averan (3) ⚠️ | Averan › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Averan ⚠️ | Averan › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Averan (3) ⚠️ | Barry › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Barlest ⚠️ | Loubajac › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Loubajac (12) ⚠️ | Loubajac › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Barlest ⚠️ | Barlest › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Loubajac (27) ⚠️ | Loubajac › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lamarque-Pontacq (9) ⚠️ | Lamarque-Pontacq › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Barlest (7) ⚠️ | Barlest › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Ossun (9) ⚠️ | Ossun › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lamarque-Pontacq (17) ⚠️ | Lamarque-Pontacq › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Barlest (11) ⚠️ | Barlest › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lamarque-Pontacq (20) ⚠️ | Lamarque-Pontacq › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lamarque-Pontacq (23) ⚠️ | Lamarque-Pontacq › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lamarque-Pontacq (25) ⚠️ | Lamarque-Pontacq › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lamarque-Pontacq (31) ⚠️ | Lamarque-Pontacq › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lamarque-Pontacq (32) ⚠️ | Lamarque-Pontacq › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lamarque-Pontacq (42) ⚠️ | Lamarque-Pontacq › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Ossun (12) ⚠️ | Ossun › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Azereix (3) ⚠️ | Azereix › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Ossun (26) ⚠️ | Ossun › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Ossun (28) ⚠️ | Ossun › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Ossun (29) ⚠️ | Ossun › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Ossun (30) ⚠️ | Ossun › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Ossun (17) ⚠️ | Ossun › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Azereix (2) ⚠️ | Azereix › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Ossun (52) ⚠️ | Ossun › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Ibos (7) ⚠️ | Ibos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Ossun (58) ⚠️ | Ossun › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Ens ⚠️ | Ens › Aure Louron | 1 |
| Forêt de Lanne (8) ⚠️ | Lanne › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lanne (11) ⚠️ | Lanne › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lanne (14) ⚠️ | Lanne › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lanne (16) ⚠️ | Lanne › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lanne (17) ⚠️ | Lanne › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Ibos (12) ⚠️ | Ibos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Azereix (13) ⚠️ | Azereix › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Azereix (17) ⚠️ | Azereix › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Azereix (6) ⚠️ | Azereix › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Ibos (16) ⚠️ | Ibos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Juillan (7) ⚠️ | Ibos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Salles (11) ⚠️ | Salles › Pyrénées Vallées des Gaves | 1 |
| Forêt de Orincles (7) ⚠️ | Orincles › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Orincles (9) ⚠️ | Orincles › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Barry ⚠️ | Barry › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Layrisse ⚠️ | Layrisse › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bénac (6) ⚠️ | Bénac › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Loucrup (14) ⚠️ | Loucrup › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Visker (3) ⚠️ | Visker › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bénac (11) ⚠️ | Bénac › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Layrisse (5) ⚠️ | Layrisse › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bénac (13) ⚠️ | Bénac › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Layrisse (8) ⚠️ | Layrisse › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bénac (17) ⚠️ | Bénac › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bénac (18) ⚠️ | Bénac › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Saint-Martin ⚠️ | Saint-Martin › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Saint-Martin (3) ⚠️ | Saint-Martin › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Saint-Martin (4) ⚠️ | Saint-Martin › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Saint-Martin (5) ⚠️ | Saint-Martin › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Juillan (13) ⚠️ | Juillan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Juillan (14) ⚠️ | Juillan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Saint-Martin (8) ⚠️ | Saint-Martin › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Juillan (15) ⚠️ | Juillan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Saint-Martin (9) ⚠️ | Saint-Martin › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Saint-Martin (11) ⚠️ | Saint-Martin › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Saint-Martin (12) ⚠️ | Saint-Martin › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Juillan (17) ⚠️ | Juillan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Saint-Martin (13) ⚠️ | Saint-Martin › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Saint-Martin (15) ⚠️ | Saint-Martin › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Louey (11) ⚠️ | Louey › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Odos (2) ⚠️ | Odos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Louey (21) ⚠️ | Louey › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Juillan (24) ⚠️ | Juillan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Juillan (25) ⚠️ | Juillan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Juillan (26) ⚠️ | Louey › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Juillan (30) ⚠️ | Juillan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Juillan (31) ⚠️ | Juillan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Juillan (32) ⚠️ | Juillan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Juillan (33) ⚠️ | Juillan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Juillan (48) ⚠️ | Juillan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Juillan (52) ⚠️ | Juillan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Juillan (55) ⚠️ | Juillan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Juillan (61) ⚠️ | Odos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Ibos (21) ⚠️ | Ibos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Juillan (76) ⚠️ | Juillan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Ibos (26) ⚠️ | Ibos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Ibos (27) ⚠️ | Ibos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Ibos (28) ⚠️ | Ibos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Juillan (79) ⚠️ | Juillan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Tarbes (18) ⚠️ | Tarbes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Tarbes (21) ⚠️ | Tarbes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Juillan (85) ⚠️ | Juillan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Juillan (86) ⚠️ | Juillan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Tarbes (24) ⚠️ | Tarbes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Ibos (61) ⚠️ | Ibos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Ibos (66) ⚠️ | Ibos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Ibos (69) ⚠️ | Ibos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Ibos (94) ⚠️ | Ibos › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Loucrup (4) ⚠️ | Loucrup › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Loucrup (26) ⚠️ | Loucrup › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Loucrup (28) ⚠️ | Loucrup › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Loucrup (29) ⚠️ | Loucrup › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lagarde (4) ⚠️ | Lagarde › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Andrest (10) ⚠️ | Andrest › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Pujo (3) ⚠️ | Saint-Lézer › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Andrest (30) ⚠️ | Andrest › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Pujo (5) ⚠️ | Pujo › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Aurensan (9) ⚠️ | Aurensan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Aurensan (10) ⚠️ | Aurensan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Aurensan (12) ⚠️ | Aurensan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Aurensan (16) ⚠️ | Aurensan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Aurensan (18) ⚠️ | Aurensan › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Sarniguet (2) ⚠️ | Sarniguet › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Ugnouas ⚠️ | Ugnouas › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Pujo (8) ⚠️ | Pujo › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Tostat (4) ⚠️ | Tostat › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Pujo (10) ⚠️ | Pujo › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Ugnouas (2) ⚠️ | Ugnouas › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Ugnouas (3) ⚠️ | Ugnouas › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Escondeaux ⚠️ | Tostat › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Bazillac (6) ⚠️ | Bazillac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Escondeaux (2) ⚠️ | Escondeaux › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Bazillac (23) ⚠️ | Bazillac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Bazillac (28) ⚠️ | Bazillac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Bazillac (30) ⚠️ | Bazillac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Bazillac (31) ⚠️ | Bazillac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Bazillac (33) ⚠️ | Bazillac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Camalès (8) ⚠️ | Camalès › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Bazillac (38) ⚠️ | Bazillac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Bazillac (43) ⚠️ | Bazillac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Rabastens-de-Bigorre ⚠️ | Bazillac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Bazillac (47) ⚠️ | Bazillac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Bazillac (53) ⚠️ | Bazillac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Camalès (16) ⚠️ | Camalès › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Camalès (17) ⚠️ | Camalès › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Place de la Biole ⚠️ | Camalès › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Vic-en-Bigorre (19) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Saint-Lézer (14) ⚠️ | Saint-Lézer › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Saint-Lézer (18) ⚠️ | Saint-Lézer › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vic-en-Bigorre (15) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Saint-Lézer (25) ⚠️ | Saint-Lézer › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Vic-en-Bigorre (30) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Vic-en-Bigorre (35) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Vic-en-Bigorre (37) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vic-en-Bigorre (17) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Auriébat ⚠️ | Auriébat › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Escondeaux (10) ⚠️ | Escondeaux › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Escondeaux (11) ⚠️ | Escondeaux › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Escondeaux (12) ⚠️ | Escondeaux › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Chis (5) ⚠️ | Chis › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bours (24) ⚠️ | Bours › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Orleix (6) ⚠️ | Chis › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bours (27) ⚠️ | Bours › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Orleix (7) ⚠️ | Orleix › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Orleix (17) ⚠️ | Orleix › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Orleix (24) ⚠️ | Orleix › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Aureilhan (12) ⚠️ | Aureilhan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Aureilhan (21) ⚠️ | Aureilhan › Tarbes-Lourdes-Pyrénées | 1 |
| Villa Ousteau ⚠️ | Aureilhan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Aragnouet (2) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Tarbes (29) ⚠️ | Tarbes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Séméac (13) ⚠️ | Séméac › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Séméac (14) ⚠️ | Séméac › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Séméac (16) ⚠️ | Séméac › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Séméac (24) ⚠️ | Séméac › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Soues (2) ⚠️ | Soues › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Laloubère (6) ⚠️ | Laloubère › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Laloubère (18) ⚠️ | Laloubère › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Laloubère (19) ⚠️ | Laloubère › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Laloubère (20) ⚠️ | Laloubère › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Laloubère (21) ⚠️ | Laloubère › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Laloubère (26) ⚠️ | Laloubère › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Tarbes (32) ⚠️ | Tarbes › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Salles-Adour ⚠️ | Salles-Adour › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Horgues ⚠️ | Horgues › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Salles-Adour (2) ⚠️ | Salles-Adour › Tarbes-Lourdes-Pyrénées | 1 |
| Parc de Laloubère ⚠️ | Laloubère › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Allier ⚠️ | Allier › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Angos (2) ⚠️ | Angos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Allier (8) ⚠️ | Allier › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Allier ⚠️ | Allier › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Bernac-Debat (2) ⚠️ | Bernac-Debat › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Momères (4) ⚠️ | Momères › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Arcizac-Adour (6) ⚠️ | Arcizac-Adour › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Momères ⚠️ | Momères › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Horgues (7) ⚠️ | Horgues › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Saint-Martin (25) ⚠️ | Saint-Martin › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Odos (15) ⚠️ | Odos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Odos (17) ⚠️ | Odos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Odos (20) ⚠️ | Odos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Horgues (11) ⚠️ | Horgues › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Horgues (12) ⚠️ | Horgues › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Horgues (4) ⚠️ | Horgues › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Saint-Martin (32) ⚠️ | Saint-Martin › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Saint-Martin (33) ⚠️ | Saint-Martin › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Odos (27) ⚠️ | Odos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Odos (29) ⚠️ | Odos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Odos (31) ⚠️ | Odos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Odos (36) ⚠️ | Odos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Odos (39) ⚠️ | Odos › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Odos (5) ⚠️ | Odos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Arcizac-Adour (9) ⚠️ | Arcizac-Adour › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Montgaillard (26) ⚠️ | Montgaillard › Haute-Bigorre | 1 |
| Forêt de Hiis (2) ⚠️ | Hiis › Haute-Bigorre | 1 |
| Forêt de Hiis (4) ⚠️ | Hiis › Haute-Bigorre | 1 |
| Forêt de Saint-Martin (37) ⚠️ | Saint-Martin › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Visker (4) ⚠️ | Visker › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Hiis (5) ⚠️ | Hiis › Haute-Bigorre | 1 |
| Bois de Arcizac-Adour (9) ⚠️ | Arcizac-Adour › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Saint-Martin (10) ⚠️ | Saint-Martin › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Saint-Martin (11) ⚠️ | Saint-Martin › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Saint-Martin (12) ⚠️ | Saint-Martin › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Arcizac-Adour (22) ⚠️ | Hiis › Haute-Bigorre | 1 |
| Forêt de Hiis (9) ⚠️ | Hiis › Haute-Bigorre | 1 |
| Forêt de Hiis (13) ⚠️ | Hiis › Haute-Bigorre | 1 |
| Bois de Montgaillard (2) ⚠️ | Hiis › Haute-Bigorre | 1 |
| Bois de Saint-Martin (14) ⚠️ | Saint-Martin › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bernac-Debat (3) ⚠️ | Bernac-Debat › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Montgaillard (36) ⚠️ | Montgaillard › Haute-Bigorre | 1 |
| Forêt de Bernac-Debat (5) ⚠️ | Bernac-Debat › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Vielle-Adour (5) ⚠️ | Vielle-Adour › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Bernac-Debat (3) ⚠️ | Bernac-Debat › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bernac-Dessus (14) ⚠️ | Bernac-Dessus › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Orignac ⚠️ | Vielle-Adour › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Antist (3) ⚠️ | Antist › Haute-Bigorre | 1 |
| Forêt de Antist (4) ⚠️ | Antist › Haute-Bigorre | 1 |
| Forêt de Montgaillard (45) ⚠️ | Montgaillard › Haute-Bigorre | 1 |
| Forêt de Orignac (2) ⚠️ | Orignac › Haute-Bigorre | 1 |
| Bois de Montgaillard (9) ⚠️ | Montgaillard › Haute-Bigorre | 1 |
| Forêt de Orignac (8) ⚠️ | Orignac › Haute-Bigorre | 1 |
| Forêt de Ordizan (28) ⚠️ | Ordizan › Haute-Bigorre | 1 |
| Forêt de Ordizan (32) ⚠️ | Ordizan › Haute-Bigorre | 1 |
| Forêt de Ordizan (40) ⚠️ | Ordizan › Haute-Bigorre | 1 |
| Forêt de Ordizan (53) ⚠️ | Ordizan › Haute-Bigorre | 1 |
| Forêt de Fréchou-Fréchet ⚠️ | Fréchou-Fréchet › Coteaux du Val-d'Arros | 1 |
| Forêt de Oueilloux (2) ⚠️ | Oueilloux › Coteaux du Val-d'Arros | 1 |
| Forêt de Hitte (2) ⚠️ | Hitte › Haute-Bigorre | 1 |
| Forêt de Mascaras (6) ⚠️ | Mascaras › Coteaux du Val-d'Arros | 1 |
| Forêt de Mascaras (8) ⚠️ | Mascaras › Coteaux du Val-d'Arros | 1 |
| Forêt de Mascaras (10) ⚠️ | Mascaras › Coteaux du Val-d'Arros | 1 |
| Forêt de Fréchou-Fréchet (7) ⚠️ | Fréchou-Fréchet › Coteaux du Val-d'Arros | 1 |
| Forêt de Angos (6) ⚠️ | Angos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Fréchou-Fréchet (8) ⚠️ | Fréchou-Fréchet › Coteaux du Val-d'Arros | 1 |
| Forêt de Mascaras (13) ⚠️ | Mascaras › Coteaux du Val-d'Arros | 1 |
| Forêt de Fréchou-Fréchet (10) ⚠️ | Fréchou-Fréchet › Coteaux du Val-d'Arros | 1 |
| Forêt de Bordes (10) ⚠️ | Bordes › Coteaux du Val-d'Arros | 1 |
| Forêt de Ozon ⚠️ | Ozon › Coteaux du Val-d'Arros | 1 |
| Forêt de Poumarous (2) ⚠️ | Poumarous › Coteaux du Val-d'Arros | 1 |
| Forêt de Orignac (26) ⚠️ | Orignac › Haute-Bigorre | 1 |
| Forêt de Tournay (2) ⚠️ | Tournay › Coteaux du Val-d'Arros | 1 |
| Forêt de Bordes (13) ⚠️ | Bordes › Coteaux du Val-d'Arros | 1 |
| Forêt de Ozon (2) ⚠️ | Poumarous › Coteaux du Val-d'Arros | 1 |
| Forêt de Orignac (29) ⚠️ | Orignac › Haute-Bigorre | 1 |
| Forêt de Hitte (8) ⚠️ | Hitte › Haute-Bigorre | 1 |
| Forêt de Mérilheu (9) ⚠️ | Mérilheu › Haute-Bigorre | 1 |
| Forêt de Hauban (11) ⚠️ | Hauban › Haute-Bigorre | 1 |
| Forêt de Orignac (44) ⚠️ | Orignac › Haute-Bigorre | 1 |
| Forêt de Tournay (4) ⚠️ | Tournay › Coteaux du Val-d'Arros | 1 |
| Forêt de Fréchou-Fréchet (17) ⚠️ | Fréchou-Fréchet › Coteaux du Val-d'Arros | 1 |
| Bois de Angos (7) ⚠️ | Angos › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Cieutat (16) ⚠️ | Cieutat › Haute-Bigorre | 1 |
| Forêt de Cieutat (23) ⚠️ | Cieutat › Haute-Bigorre | 1 |
| Forêt de Cieutat (30) ⚠️ | Cieutat › Haute-Bigorre | 1 |
| Forêt de Cieutat (37) ⚠️ | Cieutat › Haute-Bigorre | 1 |
| Forêt de Cieutat (38) ⚠️ | Cieutat › Haute-Bigorre | 1 |
| Forêt de Cieutat (43) ⚠️ | Cieutat › Haute-Bigorre | 1 |
| Forêt de Cieutat (44) ⚠️ | Cieutat › Haute-Bigorre | 1 |
| Forêt de Cieutat (46) ⚠️ | Cieutat › Haute-Bigorre | 1 |
| Forêt de Cieutat (55) ⚠️ | Cieutat › Haute-Bigorre | 1 |
| Forêt de Chelle-Spou (6) ⚠️ | Chelle-Spou › Plateau de Lannemezan | 1 |
| Forêt de Cieutat (57) ⚠️ | Cieutat › Haute-Bigorre | 1 |
| Forêt de Argelès-Bagnères (4) ⚠️ | Argelès-Bagnères › Haute-Bigorre | 1 |
| Forêt de Argelès-Bagnères (6) ⚠️ | Argelès-Bagnères › Haute-Bigorre | 1 |
| Bois de Uzer ⚠️ | Uzer › Haute-Bigorre | 1 |
| Forêt de Argelès-Bagnères (18) ⚠️ | Argelès-Bagnères › Haute-Bigorre | 1 |
| Forêt de Argelès-Bagnères (19) ⚠️ | Argelès-Bagnères › Haute-Bigorre | 1 |
| Forêt de Argelès-Bagnères (20) ⚠️ | Argelès-Bagnères › Haute-Bigorre | 1 |
| Forêt de Argelès-Bagnères (25) ⚠️ | Argelès-Bagnères › Haute-Bigorre | 1 |
| Forêt de Uzer (14) ⚠️ | Uzer › Haute-Bigorre | 1 |
| Forêt de Banios (3) ⚠️ | Banios › Haute-Bigorre | 1 |
| Forêt de Banios (4) ⚠️ | Banios › Haute-Bigorre | 1 |
| Forêt de Lies (3) ⚠️ | Lies › Haute-Bigorre | 1 |
| Forêt de Marsas (7) ⚠️ | Marsas › Haute-Bigorre | 1 |
| Forêt de Marsas (9) ⚠️ | Marsas › Haute-Bigorre | 1 |
| Forêt de Lies (12) ⚠️ | Lies › Haute-Bigorre | 1 |
| Forêt de Lies (14) ⚠️ | Lies › Haute-Bigorre | 1 |
| Forêt de Lies (15) ⚠️ | Lies › Haute-Bigorre | 1 |
| Forêt de Marsas (18) ⚠️ | Marsas › Haute-Bigorre | 1 |
| Forêt de Lies (20) ⚠️ | Lies › Haute-Bigorre | 1 |
| Forêt de Banios (12) ⚠️ | Banios › Haute-Bigorre | 1 |
| Forêt de Bettes (14) ⚠️ | Bettes › Haute-Bigorre | 1 |
| Forêt de Espieilh (7) ⚠️ | Espieilh › Plateau de Lannemezan | 1 |
| Forêt de Espieilh (8) ⚠️ | Espieilh › Plateau de Lannemezan | 1 |
| Forêt de Bourg-de-Bigorre (10) ⚠️ | Bourg-de-Bigorre › Plateau de Lannemezan | 1 |
| Forêt de Bourg-de-Bigorre (11) ⚠️ | Bourg-de-Bigorre › Plateau de Lannemezan | 1 |
| Forêt de Bourg-de-Bigorre (12) ⚠️ | Bourg-de-Bigorre › Plateau de Lannemezan | 1 |
| Forêt de Bourg-de-Bigorre (14) ⚠️ | Bourg-de-Bigorre › Plateau de Lannemezan | 1 |
| Forêt de Bourg-de-Bigorre (22) ⚠️ | Bourg-de-Bigorre › Plateau de Lannemezan | 1 |
| Forêt de Escots (7) ⚠️ | Escots › Plateau de Lannemezan | 1 |
| Forêt de Escots (8) ⚠️ | Escots › Plateau de Lannemezan | 1 |
| Forêt de Batsère (2) ⚠️ | Batsère › Plateau de Lannemezan | 1 |
| Forêt de Bulan (2) ⚠️ | Bulan › Plateau de Lannemezan | 1 |
| Forêt de Banios (14) ⚠️ | Banios › Haute-Bigorre | 1 |
| Forêt de Bourg-de-Bigorre (27) ⚠️ | Bourg-de-Bigorre › Plateau de Lannemezan | 1 |
| Forêt de Escots (11) ⚠️ | Escots › Plateau de Lannemezan | 1 |
| Forêt de Asque (9) ⚠️ | Asque › Plateau de Lannemezan | 1 |
| Forêt de Escots (15) ⚠️ | Escots › Plateau de Lannemezan | 1 |
| Forêt de Asque (10) ⚠️ | Asque › Plateau de Lannemezan | 1 |
| Forêt de Escots (18) ⚠️ | Escots › Plateau de Lannemezan | 1 |
| Forêt de Laborde ⚠️ | Laborde › Plateau de Lannemezan | 1 |
| Forêt de Esparros (4) ⚠️ | Laborde › Plateau de Lannemezan | 1 |
| Forêt de Bulan (11) ⚠️ | Bulan › Plateau de Lannemezan | 1 |
| Forêt de Batsère (11) ⚠️ | Batsère › Plateau de Lannemezan | 1 |
| Forêt de Bulan (17) ⚠️ | Bulan › Plateau de Lannemezan | 1 |
| Forêt de Lomné (6) ⚠️ | Lomné › Plateau de Lannemezan | 1 |
| Forêt de Asque (20) ⚠️ | Asque › Plateau de Lannemezan | 1 |
| Forêt de Lomné (7) ⚠️ | Lomné › Plateau de Lannemezan | 1 |
| Forêt de Bulan (20) ⚠️ | Bulan › Plateau de Lannemezan | 1 |
| Forêt de Esparros (7) ⚠️ | Esparros › Plateau de Lannemezan | 1 |
| Forêt de Laborde (13) ⚠️ | Laborde › Plateau de Lannemezan | 1 |
| Forêt de Bulan (21) ⚠️ | Bulan › Plateau de Lannemezan | 1 |
| Forêt de Asque (28) ⚠️ | Asque › Plateau de Lannemezan | 1 |
| Forêt de Bulan (22) ⚠️ | Bulan › Plateau de Lannemezan | 1 |
| Forêt de Esparros (8) ⚠️ | Esparros › Plateau de Lannemezan | 1 |
| Forêt de Arrodets (7) ⚠️ | Arrodets › Plateau de Lannemezan | 1 |
| Forêt de Espèche (5) ⚠️ | Espèche › Plateau de Lannemezan | 1 |
| Forêt de Asque (30) ⚠️ | Asque › Plateau de Lannemezan | 1 |
| Forêt de Laborde (16) ⚠️ | Laborde › Plateau de Lannemezan | 1 |
| Forêt de Bourg-de-Bigorre (47) ⚠️ | Bourg-de-Bigorre › Plateau de Lannemezan | 1 |
| Forêt de Asque (41) ⚠️ | Asque › Plateau de Lannemezan | 1 |
| Forêt de Benqué-Molère (2) ⚠️ | Benqué-Molère › Plateau de Lannemezan | 1 |
| Forêt de Avezac-Prat-Lahitte (3) ⚠️ | Avezac-Prat-Lahitte › Plateau de Lannemezan | 1 |
| Forêt de Esparros (14) ⚠️ | Esparros › Plateau de Lannemezan | 1 |
| Forêt de Esparros (15) ⚠️ | Esparros › Plateau de Lannemezan | 1 |
| Forêt de Avezac-Prat-Lahitte (6) ⚠️ | Avezac-Prat-Lahitte › Plateau de Lannemezan | 1 |
| Forêt de Avezac-Prat-Lahitte (7) ⚠️ | Avezac-Prat-Lahitte › Plateau de Lannemezan | 1 |
| Forêt de Lomné (18) ⚠️ | Lomné › Plateau de Lannemezan | 1 |
| Forêt de Lomné (19) ⚠️ | Lomné › Plateau de Lannemezan | 1 |
| Forêt de Avezac-Prat-Lahitte (12) ⚠️ | Avezac-Prat-Lahitte › Plateau de Lannemezan | 1 |
| Forêt de Esparros (20) ⚠️ | Esparros › Plateau de Lannemezan | 1 |
| Forêt de Avezac-Prat-Lahitte (14) ⚠️ | Avezac-Prat-Lahitte › Plateau de Lannemezan | 1 |
| Forêt de Esparros (42) ⚠️ | Esparros › Plateau de Lannemezan | 1 |
| Forêt de Esparros (43) ⚠️ | Esparros › Plateau de Lannemezan | 1 |
| Forêt de Esparros (45) ⚠️ | Esparros › Plateau de Lannemezan | 1 |
| Forêt de Esparros (46) ⚠️ | Esparros › Plateau de Lannemezan | 1 |
| Forêt de Esparros (47) ⚠️ | Esparros › Plateau de Lannemezan | 1 |
| Forêt de Hèches (2) ⚠️ | Hèches › Plateau de Lannemezan | 1 |
| Forêt de Esparros (60) ⚠️ | Esparros › Plateau de Lannemezan | 1 |
| Forêt de Esparros (63) ⚠️ | Esparros › Plateau de Lannemezan | 1 |
| Forêt de Esparros (67) ⚠️ | Esparros › Plateau de Lannemezan | 1 |
| Forêt de Laborde (22) ⚠️ | Laborde › Plateau de Lannemezan | 1 |
| Forêt de Lortet ⚠️ | Lortet › Plateau de Lannemezan | 1 |
| Forêt de Labastide (17) ⚠️ | Labastide › Plateau de Lannemezan | 1 |
| Forêt de Labastide (30) ⚠️ | Labastide › Plateau de Lannemezan | 1 |
| Forêt de Avezac-Prat-Lahitte (37) ⚠️ | Avezac-Prat-Lahitte › Plateau de Lannemezan | 1 |
| Forêt de Avezac-Prat-Lahitte (38) ⚠️ | Avezac-Prat-Lahitte › Plateau de Lannemezan | 1 |
| Forêt de Avezac-Prat-Lahitte (40) ⚠️ | Avezac-Prat-Lahitte › Plateau de Lannemezan | 1 |
| Forêt de Avezac-Prat-Lahitte (43) ⚠️ | Avezac-Prat-Lahitte › Plateau de Lannemezan | 1 |
| Forêt de Avezac-Prat-Lahitte (46) ⚠️ | Avezac-Prat-Lahitte › Plateau de Lannemezan | 1 |
| Forêt de Avezac-Prat-Lahitte (47) ⚠️ | Avezac-Prat-Lahitte › Plateau de Lannemezan | 1 |
| Forêt de Labastide (33) ⚠️ | Labastide › Plateau de Lannemezan | 1 |
| Forêt de Avezac-Prat-Lahitte (58) ⚠️ | Avezac-Prat-Lahitte › Plateau de Lannemezan | 1 |
| Forêt de Avezac-Prat-Lahitte (80) ⚠️ | Avezac-Prat-Lahitte › Plateau de Lannemezan | 1 |
| Forêt de Hèches (7) ⚠️ | Hèches › Plateau de Lannemezan | 1 |
| Forêt de Tilhouse (16) ⚠️ | Tilhouse › Plateau de Lannemezan | 1 |
| Forêt de Bonnemazon (14) ⚠️ | Bonnemazon › Plateau de Lannemezan | 1 |
| Forêt de Bonnemazon (22) ⚠️ | Bonnemazon › Plateau de Lannemezan | 1 |
| Forêt de Mauvezin (15) ⚠️ | Mauvezin › Plateau de Lannemezan | 1 |
| Forêt de Mauvezin (16) ⚠️ | Mauvezin › Plateau de Lannemezan | 1 |
| Forêt de Bonnemazon (25) ⚠️ | Bonnemazon › Plateau de Lannemezan | 1 |
| Forêt de Capvern (18) ⚠️ | Capvern › Plateau de Lannemezan | 1 |
| Forêt de Artiguemy (7) ⚠️ | Artiguemy › Plateau de Lannemezan | 1 |
| Forêt de Artiguemy (8) ⚠️ | Artiguemy › Plateau de Lannemezan | 1 |
| Forêt de Mauvezin (33) ⚠️ | Mauvezin › Plateau de Lannemezan | 1 |
| Forêt de Capvern (30) ⚠️ | Capvern › Plateau de Lannemezan | 1 |
| Forêt de Chelle-Spou (11) ⚠️ | Chelle-Spou › Plateau de Lannemezan | 1 |
| Forêt de Capvern (38) ⚠️ | Capvern › Plateau de Lannemezan | 1 |
| Forêt de Mauvezin (42) ⚠️ | Mauvezin › Plateau de Lannemezan | 1 |
| Forêt de Mauvezin (43) ⚠️ | Mauvezin › Plateau de Lannemezan | 1 |
| Forêt de Chelle-Spou (12) ⚠️ | Chelle-Spou › Plateau de Lannemezan | 1 |
| Forêt de Capvern (44) ⚠️ | Capvern › Plateau de Lannemezan | 1 |
| Forêt de Capvern (45) ⚠️ | Capvern › Plateau de Lannemezan | 1 |
| Forêt de Capvern (76) ⚠️ | Capvern › Plateau de Lannemezan | 1 |
| Forêt de Capvern (82) ⚠️ | Capvern › Plateau de Lannemezan | 1 |
| Forêt de Capvern (101) ⚠️ | Capvern › Plateau de Lannemezan | 1 |
| Forêt de Capvern (107) ⚠️ | Capvern › Plateau de Lannemezan | 1 |
| Forêt de Capvern (113) ⚠️ | Capvern › Plateau de Lannemezan | 1 |
| Forêt de Capvern (114) ⚠️ | Capvern › Plateau de Lannemezan | 1 |
| Forêt de Capvern (116) ⚠️ | Capvern › Plateau de Lannemezan | 1 |
| Forêt de Avezac-Prat-Lahitte (92) ⚠️ | Avezac-Prat-Lahitte › Plateau de Lannemezan | 1 |
| Forêt de La Barthe-de-Neste ⚠️ | La Barthe-de-Neste › Plateau de Lannemezan | 1 |
| Forêt de La Barthe-de-Neste (2) ⚠️ | La Barthe-de-Neste › Plateau de Lannemezan | 1 |
| Forêt de Lannemezan ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Forêt de Lannemezan (2) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Forêt de Avezac-Prat-Lahitte (99) ⚠️ | Avezac-Prat-Lahitte › Plateau de Lannemezan | 1 |
| Forêt de Avezac-Prat-Lahitte (100) ⚠️ | Avezac-Prat-Lahitte › Plateau de Lannemezan | 1 |
| Forêt de La Barthe-de-Neste (3) ⚠️ | La Barthe-de-Neste › Plateau de Lannemezan | 1 |
| Forêt de Capvern (131) ⚠️ | Avezac-Prat-Lahitte › Plateau de Lannemezan | 1 |
| Forêt de Capvern (146) ⚠️ | Capvern › Plateau de Lannemezan | 1 |
| Forêt de Capvern (147) ⚠️ | Capvern › Plateau de Lannemezan | 1 |
| Forêt de Capvern (173) ⚠️ | Capvern › Plateau de Lannemezan | 1 |
| Forêt de Capvern (174) ⚠️ | Capvern › Plateau de Lannemezan | 1 |
| Forêt de Capvern (178) ⚠️ | Capvern › Plateau de Lannemezan | 1 |
| Forêt de Capvern (184) ⚠️ | Capvern › Plateau de Lannemezan | 1 |
| Forêt de Capvern (190) ⚠️ | Capvern › Plateau de Lannemezan | 1 |
| Forêt de Capvern (193) ⚠️ | Capvern › Plateau de Lannemezan | 1 |
| Forêt de Chelle-Spou (18) ⚠️ | Chelle-Spou › Plateau de Lannemezan | 1 |
| Forêt de Chelle-Spou (28) ⚠️ | Chelle-Spou › Plateau de Lannemezan | 1 |
| Forêt de Ricaud (7) ⚠️ | Ricaud › Coteaux du Val-d'Arros | 1 |
| Forêt de Péré (10) ⚠️ | Péré › Plateau de Lannemezan | 1 |
| Forêt de Ozon (21) ⚠️ | Ozon › Coteaux du Val-d'Arros | 1 |
| Forêt de Péré (19) ⚠️ | Péré › Plateau de Lannemezan | 1 |
| Bois de Vielle-Aure (2) ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Bois de Vielle-Aure (3) ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Forêt de Bagnères-de-Bigorre (164) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Bagnères-de-Bigorre (165) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Bagnères-de-Bigorre (167) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Ozon (37) ⚠️ | Ozon › Coteaux du Val-d'Arros | 1 |
| Forêt de Tournay (18) ⚠️ | Tournay › Coteaux du Val-d'Arros | 1 |
| Forêt de Ozon (45) ⚠️ | Ozon › Coteaux du Val-d'Arros | 1 |
| Forêt de Tournay (25) ⚠️ | Tournay › Coteaux du Val-d'Arros | 1 |
| Forêt de Lanespède (17) ⚠️ | Lanespède › Coteaux du Val-d'Arros | 1 |
| Forêt de Lanespède (19) ⚠️ | Lanespède › Coteaux du Val-d'Arros | 1 |
| Forêt de Tournay (36) ⚠️ | Tournay › Coteaux du Val-d'Arros | 1 |
| Forêt de Tournay (39) ⚠️ | Tournay › Coteaux du Val-d'Arros | 1 |
| Forêt de Tournay (42) ⚠️ | Tournay › Coteaux du Val-d'Arros | 1 |
| Forêt de Tournay (53) ⚠️ | Tournay › Coteaux du Val-d'Arros | 1 |
| Forêt de Tournay (57) ⚠️ | Tournay › Coteaux du Val-d'Arros | 1 |
| Forêt de Tournay (59) ⚠️ | Tournay › Coteaux du Val-d'Arros | 1 |
| Forêt de Tournay (67) ⚠️ | Tournay › Coteaux du Val-d'Arros | 1 |
| Forêt de Tournay (68) ⚠️ | Tournay › Coteaux du Val-d'Arros | 1 |
| Parc de Tournay ⚠️ | Tournay › Coteaux du Val-d'Arros | 1 |
| Forêt de Peyraube (3) ⚠️ | Tournay › Coteaux du Val-d'Arros | 1 |
| Bois de Bordes (14) ⚠️ | Bordes › Coteaux du Val-d'Arros | 1 |
| Forêt de Tournay (79) ⚠️ | Tournay › Coteaux du Val-d'Arros | 1 |
| Forêt de Bordes (35) ⚠️ | Bordes › Coteaux du Val-d'Arros | 1 |
| Bois de Bordes (22) ⚠️ | Bordes › Coteaux du Val-d'Arros | 1 |
| Forêt de Clarac ⚠️ | Clarac › Coteaux du Val-d'Arros | 1 |
| Forêt de Peyraube (6) ⚠️ | Peyraube › Coteaux du Val-d'Arros | 1 |
| Forêt de Bordes (58) ⚠️ | Bordes › Coteaux du Val-d'Arros | 1 |
| Forêt de Bordes (59) ⚠️ | Bordes › Coteaux du Val-d'Arros | 1 |
| Forêt de Clarac (3) ⚠️ | Clarac › Coteaux du Val-d'Arros | 1 |
| Forêt de Peyraube (12) ⚠️ | Peyraube › Coteaux du Val-d'Arros | 1 |
| Forêt de Clarac (15) ⚠️ | Clarac › Coteaux du Val-d'Arros | 1 |
| Forêt de Moulédous (3) ⚠️ | Moulédous › Coteaux du Val-d'Arros | 1 |
| Forêt de Clarac (25) ⚠️ | Clarac › Coteaux du Val-d'Arros | 1 |
| Forêt de Moulédous (11) ⚠️ | Moulédous › Coteaux du Val-d'Arros | 1 |
| Bois de Goudon (2) ⚠️ | Goudon › Coteaux du Val-d'Arros | 1 |
| Forêt de Goudon (9) ⚠️ | Goudon › Coteaux du Val-d'Arros | 1 |
| Forêt de Peyriguère (2) ⚠️ | Peyriguère › Coteaux du Val-d'Arros | 1 |
| Forêt de Peyriguère (3) ⚠️ | Peyriguère › Coteaux du Val-d'Arros | 1 |
| Forêt de Goudon (12) ⚠️ | Goudon › Coteaux du Val-d'Arros | 1 |
| Forêt de Marquerie ⚠️ | Marquerie › Coteaux du Val-d'Arros | 1 |
| Forêt de Coussan (3) ⚠️ | Coussan › Coteaux du Val-d'Arros | 1 |
| Forêt de Coussan (5) ⚠️ | Coussan › Coteaux du Val-d'Arros | 1 |
| Bois de Cabanac (2) ⚠️ | Cabanac › Coteaux du Val-d'Arros | 1 |
| Forêt de Coussan (7) ⚠️ | Coussan › Coteaux du Val-d'Arros | 1 |
| Forêt de Laslades (2) ⚠️ | Laslades › Coteaux du Val-d'Arros | 1 |
| Forêt de Castelvieilh (3) ⚠️ | Castelvieilh › Coteaux du Val-d'Arros | 1 |
| Bois de Marquerie (3) ⚠️ | Marquerie › Coteaux du Val-d'Arros | 1 |
| Bois de Coussan (3) ⚠️ | Coussan › Coteaux du Val-d'Arros | 1 |
| Forêt de Castelvieilh (5) ⚠️ | Castelvieilh › Coteaux du Val-d'Arros | 1 |
| Forêt de Castelvieilh (7) ⚠️ | Castelvieilh › Coteaux du Val-d'Arros | 1 |
| Forêt de Castelvieilh (9) ⚠️ | Castelvieilh › Coteaux du Val-d'Arros | 1 |
| Forêt de Castelvieilh (10) ⚠️ | Castelvieilh › Coteaux du Val-d'Arros | 1 |
| Forêt de Cabanac (6) ⚠️ | Cabanac › Coteaux du Val-d'Arros | 1 |
| Forêt de Castelvieilh (13) ⚠️ | Castelvieilh › Coteaux du Val-d'Arros | 1 |
| Forêt de Chelle-Debat ⚠️ | Chelle-Debat › Coteaux du Val-d'Arros | 1 |
| Forêt de Marseillan (6) ⚠️ | Marseillan › Coteaux du Val-d'Arros | 1 |
| Bois de Chelle-Debat (2) ⚠️ | Chelle-Debat › Coteaux du Val-d'Arros | 1 |
| Bois de Castelvieilh (8) ⚠️ | Castelvieilh › Coteaux du Val-d'Arros | 1 |
| Bois de Castelvieilh (10) ⚠️ | Castelvieilh › Coteaux du Val-d'Arros | 1 |
| Bois de Marseillan ⚠️ | Marseillan › Coteaux du Val-d'Arros | 1 |
| Bois de Cabanac (16) ⚠️ | Cabanac › Coteaux du Val-d'Arros | 1 |
| Bois de Chelle-Debat (8) ⚠️ | Chelle-Debat › Coteaux du Val-d'Arros | 1 |
| Bois de Cabanac (18) ⚠️ | Cabanac › Coteaux du Val-d'Arros | 1 |
| Bois de Chelle-Debat (12) ⚠️ | Chelle-Debat › Coteaux du Val-d'Arros | 1 |
| Forêt de Louit (2) ⚠️ | Louit › Coteaux du Val-d'Arros | 1 |
| Forêt de Jacque (2) ⚠️ | Jacque › Coteaux du Val-d'Arros | 1 |
| Forêt de Bouilh-Péreuilh (9) ⚠️ | Bouilh-Péreuilh › Coteaux du Val-d'Arros | 1 |
| Forêt de Bouilh-Péreuilh (10) ⚠️ | Bouilh-Péreuilh › Coteaux du Val-d'Arros | 1 |
| Forêt de Peyrun (3) ⚠️ | Peyrun › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Bouilh-Péreuilh (12) ⚠️ | Bouilh-Péreuilh › Coteaux du Val-d'Arros | 1 |
| Forêt de Laméac (3) ⚠️ | Laméac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Saint-Sever-de-Rustan (3) ⚠️ | Bouilh-Devant › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Sénac (2) ⚠️ | Sénac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Sénac (3) ⚠️ | Sénac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Mansan (2) ⚠️ | Mansan › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Mansan (2) ⚠️ | Mansan › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Sénac (6) ⚠️ | Sénac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Sénac (8) ⚠️ | Sénac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Sénac (13) ⚠️ | Sénac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Sénac (21) ⚠️ | Sénac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Sénac (24) ⚠️ | Sénac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Lacassagne ⚠️ | Lacassagne › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Saint-Sever-de-Rustan (6) ⚠️ | Saint-Sever-de-Rustan › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Sénac (20) ⚠️ | Sénac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Sénac (22) ⚠️ | Sénac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Rabastens-de-Bigorre (3) ⚠️ | Rabastens-de-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Lacassagne (2) ⚠️ | Lacassagne › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Saint-Sever-de-Rustan (5) ⚠️ | Saint-Sever-de-Rustan › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Saint-Sever-de-Rustan (7) ⚠️ | Saint-Sever-de-Rustan › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Saint-Sever-de-Rustan (15) ⚠️ | Saint-Sever-de-Rustan › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Moumoulous (2) ⚠️ | Moumoulous › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Bouilh-Devant ⚠️ | Bouilh-Devant › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Castéra-Lou ⚠️ | Castéra-Lou › Coteaux du Val-d'Arros | 1 |
| Forêt de Mingot ⚠️ | Mingot › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Rabastens-de-Bigorre (6) ⚠️ | Rabastens-de-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Lacassagne (6) ⚠️ | Lacassagne › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Rabastens-de-Bigorre (10) ⚠️ | Rabastens-de-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Rabastens-de-Bigorre (29) ⚠️ | Rabastens-de-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Lescurry ⚠️ | Lescurry › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Lescurry (12) ⚠️ | Lescurry › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Lescurry (18) ⚠️ | Lescurry › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Castéra-Lou ⚠️ | Castéra-Lou › Coteaux du Val-d'Arros | 1 |
| Bois de Lescurry (28) ⚠️ | Lescurry › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Castéra-Lou (3) ⚠️ | Castéra-Lou › Coteaux du Val-d'Arros | 1 |
| Forêt de Louit (4) ⚠️ | Louit › Coteaux du Val-d'Arros | 1 |
| Bois de Castéra-Lou (5) ⚠️ | Castéra-Lou › Coteaux du Val-d'Arros | 1 |
| Bois de Castéra-Lou (9) ⚠️ | Castéra-Lou › Coteaux du Val-d'Arros | 1 |
| Bois de Castéra-Lou (18) ⚠️ | Castéra-Lou › Coteaux du Val-d'Arros | 1 |
| Forêt de Pouyastruc (7) ⚠️ | Pouyastruc › Coteaux du Val-d'Arros | 1 |
| Forêt de Pouyastruc (9) ⚠️ | Pouyastruc › Coteaux du Val-d'Arros | 1 |
| Forêt de Collongues (2) ⚠️ | Collongues › Coteaux du Val-d'Arros | 1 |
| Bois de Dours (11) ⚠️ | Dours › Coteaux du Val-d'Arros | 1 |
| Bois de Collongues (6) ⚠️ | Collongues › Coteaux du Val-d'Arros | 1 |
| Bois de Pouyastruc (6) ⚠️ | Pouyastruc › Coteaux du Val-d'Arros | 1 |
| Bois de Oléac-Debat ⚠️ | Pouyastruc › Coteaux du Val-d'Arros | 1 |
| Forêt de Lizos (2) ⚠️ | Lizos › Coteaux du Val-d'Arros | 1 |
| Forêt de Lizos (3) ⚠️ | Lizos › Coteaux du Val-d'Arros | 1 |
| Forêt de Lizos (5) ⚠️ | Lizos › Coteaux du Val-d'Arros | 1 |
| Forêt de Oléac-Debat (3) ⚠️ | Oléac-Debat › Coteaux du Val-d'Arros | 1 |
| Bois de Oléac-Debat (4) ⚠️ | Oléac-Debat › Coteaux du Val-d'Arros | 1 |
| Bois de Lizos (7) ⚠️ | Lizos › Coteaux du Val-d'Arros | 1 |
| Bois de Pouyastruc (16) ⚠️ | Pouyastruc › Coteaux du Val-d'Arros | 1 |
| Bois de Lizos (11) ⚠️ | Lizos › Coteaux du Val-d'Arros | 1 |
| Forêt de Boulin (2) ⚠️ | Boulin › Coteaux du Val-d'Arros | 1 |
| Forêt de Pouyastruc (16) ⚠️ | Pouyastruc › Coteaux du Val-d'Arros | 1 |
| Forêt de Hourc (2) ⚠️ | Hourc › Coteaux du Val-d'Arros | 1 |
| Forêt de Pouyastruc (21) ⚠️ | Pouyastruc › Coteaux du Val-d'Arros | 1 |
| Bois de Pouyastruc (24) ⚠️ | Pouyastruc › Coteaux du Val-d'Arros | 1 |
| Forêt de Souyeaux (2) ⚠️ | Souyeaux › Coteaux du Val-d'Arros | 1 |
| Forêt de Souyeaux (4) ⚠️ | Souyeaux › Coteaux du Val-d'Arros | 1 |
| Forêt de Laslades (4) ⚠️ | Laslades › Coteaux du Val-d'Arros | 1 |
| Forêt de Souyeaux (10) ⚠️ | Souyeaux › Coteaux du Val-d'Arros | 1 |
| Bois de Lansac (5) ⚠️ | Lansac › Coteaux du Val-d'Arros | 1 |
| Forêt de Lespouey (3) ⚠️ | Lespouey › Coteaux du Val-d'Arros | 1 |
| Forêt de Lespouey (4) ⚠️ | Lespouey › Coteaux du Val-d'Arros | 1 |
| Forêt de Calavanté (4) ⚠️ | Calavanté › Coteaux du Val-d'Arros | 1 |
| Forêt de Lansac (7) ⚠️ | Lansac › Coteaux du Val-d'Arros | 1 |
| Forêt de Lansac (9) ⚠️ | Lansac › Coteaux du Val-d'Arros | 1 |
| Forêt de Calavanté (9) ⚠️ | Calavanté › Coteaux du Val-d'Arros | 1 |
| Forêt de Lespouey (8) ⚠️ | Lespouey › Coteaux du Val-d'Arros | 1 |
| Bois de Calavanté (2) ⚠️ | Calavanté › Coteaux du Val-d'Arros | 1 |
| Bois de Calavanté (4) ⚠️ | Calavanté › Coteaux du Val-d'Arros | 1 |
| Bois de Calavanté (8) ⚠️ | Calavanté › Coteaux du Val-d'Arros | 1 |
| Forêt de Sarrouilles (2) ⚠️ | Sarrouilles › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Sarrouilles (4) ⚠️ | Sarrouilles › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Sarrouilles (5) ⚠️ | Sarrouilles › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Sarrouilles (7) ⚠️ | Sarrouilles › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Sarrouilles (20) ⚠️ | Sarrouilles › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Sarrouilles (31) ⚠️ | Sarrouilles › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Oursbelille (7) ⚠️ | Oursbelille › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Peyriguère (6) ⚠️ | Peyriguère › Coteaux du Val-d'Arros | 1 |
| Forêt de Aubarède (2) ⚠️ | Aubarède › Coteaux du Val-d'Arros | 1 |
| Bois de Aubarède (11) ⚠️ | Aubarède › Coteaux du Val-d'Arros | 1 |
| Forêt de Chelle-Debat (2) ⚠️ | Chelle-Debat › Coteaux du Val-d'Arros | 1 |
| Bois de Chelle-Debat (26) ⚠️ | Chelle-Debat › Coteaux du Val-d'Arros | 1 |
| Bois de Chelle-Debat (29) ⚠️ | Chelle-Debat › Coteaux du Val-d'Arros | 1 |
| Bois de Aubarède (31) ⚠️ | Aubarède › Coteaux du Val-d'Arros | 1 |
| Forêt de Mun (4) ⚠️ | Mun › Coteaux du Val-d'Arros | 1 |
| Bois de Chelle-Debat (31) ⚠️ | Chelle-Debat › Coteaux du Val-d'Arros | 1 |
| Bois de Chelle-Debat (35) ⚠️ | Chelle-Debat › Coteaux du Val-d'Arros | 1 |
| Bois de Osmets (2) ⚠️ | Chelle-Debat › Coteaux du Val-d'Arros | 1 |
| Forêt de Lubret-Saint-Luc ⚠️ | Lubret-Saint-Luc › Pays de Trie et du Magnoac | 1 |
| Forêt de Bouilh-Devant (11) ⚠️ | Bouilh-Devant › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Bouilh-Devant (13) ⚠️ | Bouilh-Devant › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Antin (3) ⚠️ | Antin › Pays de Trie et du Magnoac | 1 |
| Bois de Bouilh-Devant (2) ⚠️ | Bouilh-Devant › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Antin (6) ⚠️ | Antin › Pays de Trie et du Magnoac | 1 |
| Bois de Bouilh-Devant (13) ⚠️ | Bouilh-Devant › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Estampures ⚠️ | Estampures › Pays de Trie et du Magnoac | 1 |
| Forêt de Fréchède (7) ⚠️ | Fréchède › Pays de Trie et du Magnoac | 1 |
| Forêt de Fréchède (8) ⚠️ | Fréchède › Pays de Trie et du Magnoac | 1 |
| Forêt de Fréchède (9) ⚠️ | Fréchède › Pays de Trie et du Magnoac | 1 |
| Bois de Fréchède (6) ⚠️ | Fréchède › Pays de Trie et du Magnoac | 1 |
| Bois de Fréchède (9) ⚠️ | Fréchède › Pays de Trie et du Magnoac | 1 |
| Forêt de Estampures (9) ⚠️ | Estampures › Pays de Trie et du Magnoac | 1 |
| Forêt de Estampures (10) ⚠️ | Estampures › Pays de Trie et du Magnoac | 1 |
| Bois de Estampures (4) ⚠️ | Estampures › Pays de Trie et du Magnoac | 1 |
| Bois de Estampures (6) ⚠️ | Estampures › Pays de Trie et du Magnoac | 1 |
| Forêt de Mazerolles (2) ⚠️ | Mazerolles › Pays de Trie et du Magnoac | 1 |
| Bois de Mazerolles (25) ⚠️ | Mazerolles › Pays de Trie et du Magnoac | 1 |
| Bois de Antin (9) ⚠️ | Antin › Pays de Trie et du Magnoac | 1 |
| Bois de Antin (13) ⚠️ | Bernadets-Debat › Pays de Trie et du Magnoac | 1 |
| Bois de Lapeyre ⚠️ | Antin › Pays de Trie et du Magnoac | 1 |
| Bois de Antin (14) ⚠️ | Antin › Pays de Trie et du Magnoac | 1 |
| Bois de Antin (16) ⚠️ | Antin › Pays de Trie et du Magnoac | 1 |
| Bois de Antin (18) ⚠️ | Antin › Pays de Trie et du Magnoac | 1 |
| Forêt de Antin (5) ⚠️ | Antin › Pays de Trie et du Magnoac | 1 |
| Forêt de Antin (6) ⚠️ | Antin › Pays de Trie et du Magnoac | 1 |
| Bois de Antin (27) ⚠️ | Antin › Pays de Trie et du Magnoac | 1 |
| Bois de Antin (32) ⚠️ | Antin › Pays de Trie et du Magnoac | 1 |
| Forêt de Luby-Betmont ⚠️ | Luby-Betmont › Pays de Trie et du Magnoac | 1 |
| Forêt de Bernadets-Debat (4) ⚠️ | Bernadets-Debat › Pays de Trie et du Magnoac | 1 |
| Forêt de Bernadets-Debat (6) ⚠️ | Bernadets-Debat › Pays de Trie et du Magnoac | 1 |
| Bois de Bernadets-Debat (14) ⚠️ | Bernadets-Debat › Pays de Trie et du Magnoac | 1 |
| Bois de Bernadets-Debat (15) ⚠️ | Bernadets-Debat › Pays de Trie et du Magnoac | 1 |
| Bois de Bernadets-Debat (29) ⚠️ | Bernadets-Debat › Pays de Trie et du Magnoac | 1 |
| Bois de Bernadets-Debat (31) ⚠️ | Bernadets-Debat › Pays de Trie et du Magnoac | 1 |
| Bois de Bernadets-Debat (33) ⚠️ | Bernadets-Debat › Pays de Trie et du Magnoac | 1 |
| Bois de Bernadets-Debat (35) ⚠️ | Bernadets-Debat › Pays de Trie et du Magnoac | 1 |
| Bois de Bernadets-Debat (39) ⚠️ | Bernadets-Debat › Pays de Trie et du Magnoac | 1 |
| Bois de Bernadets-Debat (40) ⚠️ | Bernadets-Debat › Pays de Trie et du Magnoac | 1 |
| Bois de Bernadets-Debat (48) ⚠️ | Bernadets-Debat › Pays de Trie et du Magnoac | 1 |
| Forêt de Trie-sur-Baïse ⚠️ | Trie-sur-Baïse › Pays de Trie et du Magnoac | 1 |
| Forêt de Trie-sur-Baïse (4) ⚠️ | Trie-sur-Baïse › Pays de Trie et du Magnoac | 1 |
| Bois de Trie-sur-Baïse (3) ⚠️ | Trie-sur-Baïse › Pays de Trie et du Magnoac | 1 |
| Bois de Lapeyre (12) ⚠️ | Lapeyre › Pays de Trie et du Magnoac | 1 |
| Forêt de Trie-sur-Baïse (5) ⚠️ | Trie-sur-Baïse › Pays de Trie et du Magnoac | 1 |
| Bois de Fontrailles (12) ⚠️ | Fontrailles › Pays de Trie et du Magnoac | 1 |
| Forêt de Lalanne-Trie (2) ⚠️ | Lalanne-Trie › Pays de Trie et du Magnoac | 1 |
| Bois de Guchan ⚠️ | Guchan › Aure Louron | 1 |
| Forêt de Vielle-Aure (98) ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Bois de Sentous ⚠️ | Sentous › Plateau de Lannemezan | 1 |
| Forêt de Lalanne-Trie (5) ⚠️ | Lalanne-Trie › Pays de Trie et du Magnoac | 1 |
| Forêt de Fontrailles (5) ⚠️ | Fontrailles › Pays de Trie et du Magnoac | 1 |
| Forêt de Fontrailles (6) ⚠️ | Fontrailles › Pays de Trie et du Magnoac | 1 |
| Forêt de Fontrailles (14) ⚠️ | Fontrailles › Pays de Trie et du Magnoac | 1 |
| Bois de Fontrailles (17) ⚠️ | Fontrailles › Pays de Trie et du Magnoac | 1 |
| Bois de Fontrailles (20) ⚠️ | Fontrailles › Pays de Trie et du Magnoac | 1 |
| Bois de Fontrailles (32) ⚠️ | Fontrailles › Pays de Trie et du Magnoac | 1 |
| Forêt de Luby-Betmont (3) ⚠️ | Osmets › Pays de Trie et du Magnoac | 1 |
| Forêt de Sère-Rustaing (2) ⚠️ | Sère-Rustaing › Pays de Trie et du Magnoac | 1 |
| Forêt de Sère-Rustaing (4) ⚠️ | Sère-Rustaing › Pays de Trie et du Magnoac | 1 |
| Forêt de Mun (13) ⚠️ | Mun › Coteaux du Val-d'Arros | 1 |
| Forêt de Mun (14) ⚠️ | Mun › Coteaux du Val-d'Arros | 1 |
| Bois de Mun (2) ⚠️ | Mun › Coteaux du Val-d'Arros | 1 |
| Bois de Mun (29) ⚠️ | Mun › Coteaux du Val-d'Arros | 1 |
| Forêt de Bugard ⚠️ | Bugard › Pays de Trie et du Magnoac | 1 |
| Forêt de Vidou (3) ⚠️ | Vidou › Pays de Trie et du Magnoac | 1 |
| Forêt de Bugard (3) ⚠️ | Bugard › Pays de Trie et du Magnoac | 1 |
| Forêt de Villembits (2) ⚠️ | Villembits › Pays de Trie et du Magnoac | 1 |
| Forêt de Bugard (6) ⚠️ | Bugard › Pays de Trie et du Magnoac | 1 |
| Forêt de Villembits (8) ⚠️ | Villembits › Pays de Trie et du Magnoac | 1 |
| Forêt de Vidou (4) ⚠️ | Vidou › Pays de Trie et du Magnoac | 1 |
| Bois de Bugard ⚠️ | Sère-Rustaing › Pays de Trie et du Magnoac | 1 |
| Bois de Villembits (9) ⚠️ | Villembits › Pays de Trie et du Magnoac | 1 |
| Bois de Sère-Rustaing (2) ⚠️ | Sère-Rustaing › Pays de Trie et du Magnoac | 1 |
| Bois de Villembits (11) ⚠️ | Villembits › Pays de Trie et du Magnoac | 1 |
| Bois de Villembits (12) ⚠️ | Lamarque-Rustaing › Pays de Trie et du Magnoac | 1 |
| Forêt de Lustar (2) ⚠️ | Lustar › Pays de Trie et du Magnoac | 1 |
| Forêt de Lustar (5) ⚠️ | Lustar › Pays de Trie et du Magnoac | 1 |
| Forêt de Tournous-Darré (8) ⚠️ | Tournous-Darré › Pays de Trie et du Magnoac | 1 |
| Forêt de Lustar (6) ⚠️ | Lustar › Pays de Trie et du Magnoac | 1 |
| Forêt de Lustar (8) ⚠️ | Lustar › Pays de Trie et du Magnoac | 1 |
| Forêt de Lustar (9) ⚠️ | Lustar › Pays de Trie et du Magnoac | 1 |
| Forêt de Lustar (10) ⚠️ | Lustar › Pays de Trie et du Magnoac | 1 |
| Bois de Villembits (28) ⚠️ | Lustar › Pays de Trie et du Magnoac | 1 |
| Forêt de Orieux (3) ⚠️ | Orieux › Coteaux du Val-d'Arros | 1 |
| Forêt de Lustar (13) ⚠️ | Lustar › Pays de Trie et du Magnoac | 1 |
| Forêt de Bonnefont (3) ⚠️ | Bonnefont › Pays de Trie et du Magnoac | 1 |
| Forêt de Orieux (6) ⚠️ | Sère-Rustaing › Pays de Trie et du Magnoac | 1 |
| Forêt de Orieux (7) ⚠️ | Orieux › Coteaux du Val-d'Arros | 1 |
| Bois de Bugard (12) ⚠️ | Orieux › Coteaux du Val-d'Arros | 1 |
| Bois de Orieux (3) ⚠️ | Orieux › Coteaux du Val-d'Arros | 1 |
| Forêt de Burg (10) ⚠️ | Burg › Coteaux du Val-d'Arros | 1 |
| Bois de Montastruc (4) ⚠️ | Montastruc › Plateau de Lannemezan | 1 |
| Bois de Orieux (15) ⚠️ | Orieux › Coteaux du Val-d'Arros | 1 |
| Forêt de Montastruc (7) ⚠️ | Montastruc › Plateau de Lannemezan | 1 |
| Bois de Burg (8) ⚠️ | Burg › Coteaux du Val-d'Arros | 1 |
| Bois de Bernadets-Dessus (12) ⚠️ | Bernadets-Dessus › Coteaux du Val-d'Arros | 1 |
| Bois de Bonnefont (13) ⚠️ | Bonnefont › Pays de Trie et du Magnoac | 1 |
| Bois de Bonnefont (21) ⚠️ | Bonnefont › Pays de Trie et du Magnoac | 1 |
| Bois de Bonnefont (22) ⚠️ | Bonnefont › Pays de Trie et du Magnoac | 1 |
| Forêt de Bégole (5) ⚠️ | Bégole › Coteaux du Val-d'Arros | 1 |
| Forêt de Burg (20) ⚠️ | Burg › Coteaux du Val-d'Arros | 1 |
| Bois de Burg (14) ⚠️ | Burg › Coteaux du Val-d'Arros | 1 |
| Bois de Burg (27) ⚠️ | Burg › Coteaux du Val-d'Arros | 1 |
| Bois de Montastruc (27) ⚠️ | Montastruc › Plateau de Lannemezan | 1 |
| Bois de Montastruc (30) ⚠️ | Montastruc › Plateau de Lannemezan | 1 |
| Bois de Montastruc (36) ⚠️ | Montastruc › Plateau de Lannemezan | 1 |
| Bois de Montastruc (44) ⚠️ | Montastruc › Plateau de Lannemezan | 1 |
| Bois de Burg (48) ⚠️ | Burg › Coteaux du Val-d'Arros | 1 |
| Bois de Montastruc (48) ⚠️ | Montastruc › Plateau de Lannemezan | 1 |
| Bois de Burg (83) ⚠️ | Burg › Coteaux du Val-d'Arros | 1 |
| Bois de Castelbajac (16) ⚠️ | Castelbajac › Plateau de Lannemezan | 1 |
| Bois de Castelbajac (24) ⚠️ | Castelbajac › Plateau de Lannemezan | 1 |
| Forêt de Lagrange (2) ⚠️ | Lagrange › Plateau de Lannemezan | 1 |
| Forêt de Houeydets (4) ⚠️ | Houeydets › Plateau de Lannemezan | 1 |
| Bois de Castelbajac (25) ⚠️ | Castelbajac › Plateau de Lannemezan | 1 |
| Bois de Lutilhous (9) ⚠️ | Lutilhous › Plateau de Lannemezan | 1 |
| Bois de Lutilhous (10) ⚠️ | Lutilhous › Plateau de Lannemezan | 1 |
| Bois de Bégole (18) ⚠️ | Bégole › Coteaux du Val-d'Arros | 1 |
| Bois de Lutilhous (11) ⚠️ | Lutilhous › Plateau de Lannemezan | 1 |
| Bois de Houeydets (6) ⚠️ | Houeydets › Plateau de Lannemezan | 1 |
| Bois de Bégole (23) ⚠️ | Bégole › Coteaux du Val-d'Arros | 1 |
| Bois de Burg (98) ⚠️ | Burg › Coteaux du Val-d'Arros | 1 |
| Bois de Houeydets (11) ⚠️ | Houeydets › Plateau de Lannemezan | 1 |
| Bois de Houeydets (12) ⚠️ | Houeydets › Plateau de Lannemezan | 1 |
| Bois de Houeydets (16) ⚠️ | Houeydets › Plateau de Lannemezan | 1 |
| Bois de Lagrange (19) ⚠️ | Lagrange › Plateau de Lannemezan | 1 |
| Bois de Campistrous (3) ⚠️ | Campistrous › Plateau de Lannemezan | 1 |
| Bois de Lagrange (24) ⚠️ | Lagrange › Plateau de Lannemezan | 1 |
| Forêt de Capvern (195) ⚠️ | Capvern › Plateau de Lannemezan | 1 |
| Forêt de Campistrous (3) ⚠️ | Campistrous › Plateau de Lannemezan | 1 |
| Forêt de Campistrous (5) ⚠️ | Campistrous › Plateau de Lannemezan | 1 |
| Forêt de Capvern (197) ⚠️ | Capvern › Plateau de Lannemezan | 1 |
| Forêt de Campistrous (10) ⚠️ | Campistrous › Plateau de Lannemezan | 1 |
| Bois de Campistrous (16) ⚠️ | Campistrous › Plateau de Lannemezan | 1 |
| Forêt de Campistrous (12) ⚠️ | Campistrous › Plateau de Lannemezan | 1 |
| Forêt de Puydarrieux ⚠️ | Puydarrieux › Pays de Trie et du Magnoac | 1 |
| Forêt de Sentous ⚠️ | Sentous › Plateau de Lannemezan | 1 |
| Forêt de Sentous (2) ⚠️ | Sentous › Plateau de Lannemezan | 1 |
| Forêt de Bonnefont (6) ⚠️ | Bonnefont › Pays de Trie et du Magnoac | 1 |
| Forêt de Puydarrieux (2) ⚠️ | Puydarrieux › Pays de Trie et du Magnoac | 1 |
| Bois de Bonnefont (47) ⚠️ | Bonnefont › Pays de Trie et du Magnoac | 1 |
| Bois de Lustar (26) ⚠️ | Lustar › Pays de Trie et du Magnoac | 1 |
| Bois de Bonnefont (59) ⚠️ | Bonnefont › Pays de Trie et du Magnoac | 1 |
| Bois de Bonnefont (67) ⚠️ | Bonnefont › Pays de Trie et du Magnoac | 1 |
| Forêt de Montastruc (11) ⚠️ | Montastruc › Plateau de Lannemezan | 1 |
| Bois de Bonnefont (90) ⚠️ | Bonnefont › Pays de Trie et du Magnoac | 1 |
| Bois de Bonnefont (103) ⚠️ | Bonnefont › Pays de Trie et du Magnoac | 1 |
| Forêt de Montastruc (14) ⚠️ | Libaros › Plateau de Lannemezan | 1 |
| Forêt de Bonrepos (3) ⚠️ | Bonrepos › Plateau de Lannemezan | 1 |
| Forêt de Libaros (6) ⚠️ | Libaros › Plateau de Lannemezan | 1 |
| Forêt de Bonrepos (10) ⚠️ | Bonrepos › Plateau de Lannemezan | 1 |
| Bois de Castelbajac (36) ⚠️ | Castelbajac › Plateau de Lannemezan | 1 |
| Bois de Castelbajac (38) ⚠️ | Castelbajac › Plateau de Lannemezan | 1 |
| Bois de Castelbajac (39) ⚠️ | Castelbajac › Plateau de Lannemezan | 1 |
| Bois de Libaros (2) ⚠️ | Libaros › Plateau de Lannemezan | 1 |
| Bois de Libaros (3) ⚠️ | Libaros › Plateau de Lannemezan | 1 |
| Forêt de Bonrepos (13) ⚠️ | Bonrepos › Plateau de Lannemezan | 1 |
| Forêt de Castelbajac (8) ⚠️ | Castelbajac › Plateau de Lannemezan | 1 |
| Bois de Bonrepos (13) ⚠️ | Bonrepos › Plateau de Lannemezan | 1 |
| Bois de Bonrepos (15) ⚠️ | Bonrepos › Plateau de Lannemezan | 1 |
| Bois de Bonrepos (25) ⚠️ | Bonrepos › Plateau de Lannemezan | 1 |
| Bois de Castelbajac (49) ⚠️ | Castelbajac › Plateau de Lannemezan | 1 |
| Bois de Houeydets (32) ⚠️ | Houeydets › Plateau de Lannemezan | 1 |
| Bois de Bonrepos (31) ⚠️ | Bonrepos › Plateau de Lannemezan | 1 |
| Bois de Castelbajac (55) ⚠️ | Castelbajac › Plateau de Lannemezan | 1 |
| Bois de Campistrous (25) ⚠️ | Campistrous › Plateau de Lannemezan | 1 |
| Forêt de Galez (2) ⚠️ | Galez › Plateau de Lannemezan | 1 |
| Forêt de Galan (3) ⚠️ | Galan › Plateau de Lannemezan | 1 |
| Bois de Galan (2) ⚠️ | Galan › Plateau de Lannemezan | 1 |
| Forêt de Campistrous (20) ⚠️ | Campistrous › Plateau de Lannemezan | 1 |
| Forêt de Lannemezan (11) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Forêt de Campistrous (22) ⚠️ | Campistrous › Plateau de Lannemezan | 1 |
| Forêt de Lannemezan (14) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Bois de Campistrous (36) ⚠️ | Campistrous › Plateau de Lannemezan | 1 |
| Forêt de Lannemezan (16) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Piscine Municipale ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Bois de Lannemezan (25) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Bois de Lannemezan (36) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Bois de Lannemezan (37) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Forêt de Clarens ⚠️ | Clarens › Plateau de Lannemezan | 1 |
| Forêt de Lannemezan (17) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Forêt de Lannemezan (21) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Forêt de Lannemezan (27) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Bois de Lannemezan (58) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Bois de Lannemezan (61) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Bois de Lannemezan (90) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Forêt de Lannemezan (38) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Bois de Lannemezan (97) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Bois de Lannemezan (101) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Bois de Lannemezan (104) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Bois de Lannemezan (114) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Forêt de Lannemezan (42) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Forêt de Lannemezan (43) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Forêt de Pinas (2) ⚠️ | Pinas › Plateau de Lannemezan | 1 |
| Forêt de Lannemezan (49) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Forêt de Lannemezan (51) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Bois de Pinas ⚠️ | Pinas › Plateau de Lannemezan | 1 |
| Bois de Lannemezan (129) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Bois de Lannemezan (134) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Bois de Lannemezan (139) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Bois de Lannemezan (146) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Bois de Lannemezan (150) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Bois de Lannemezan (171) ⚠️ | Escala › Plateau de Lannemezan | 1 |
| Bois de Lannemezan (175) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Bois de Lannemezan (181) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Bois de Lannemezan (186) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Forêt de Lannemezan (62) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Forêt de Lannemezan (63) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Bois de Lannemezan (193) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Bois de Lannemezan (197) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Bois de Lannemezan (204) ⚠️ | Lannemezan › Plateau de Lannemezan | 1 |
| Bois de Clarens (3) ⚠️ | Clarens › Plateau de Lannemezan | 1 |
| Forêt de Clarens (4) ⚠️ | Clarens › Plateau de Lannemezan | 1 |
| Forêt de Clarens (6) ⚠️ | Clarens › Plateau de Lannemezan | 1 |
| Forêt de Clarens (7) ⚠️ | Clarens › Plateau de Lannemezan | 1 |
| Bois de Clarens (11) ⚠️ | Clarens › Plateau de Lannemezan | 1 |
| Bois de Clarens (14) ⚠️ | Clarens › Plateau de Lannemezan | 1 |
| Bois de Clarens (19) ⚠️ | Clarens › Plateau de Lannemezan | 1 |
| Bois de Uglas (3) ⚠️ | Uglas › Plateau de Lannemezan | 1 |
| Bois de Clarens (24) ⚠️ | Clarens › Plateau de Lannemezan | 1 |
| Bois de Clarens (25) ⚠️ | Clarens › Plateau de Lannemezan | 1 |
| Forêt de Clarens (8) ⚠️ | Clarens › Plateau de Lannemezan | 1 |
| Forêt de Clarens (9) ⚠️ | Clarens › Plateau de Lannemezan | 1 |
| Bois de Galez (7) ⚠️ | Galez › Plateau de Lannemezan | 1 |
| Bois de Galez (10) ⚠️ | Galez › Plateau de Lannemezan | 1 |
| Bois de Campistrous (58) ⚠️ | Campistrous › Plateau de Lannemezan | 1 |
| Bois de Clarens (56) ⚠️ | Clarens › Plateau de Lannemezan | 1 |
| Bois de Clarens (69) ⚠️ | Réjaumont › Plateau de Lannemezan | 1 |
| Bois de Galan (13) ⚠️ | Galan › Plateau de Lannemezan | 1 |
| Bois de Galan (31) ⚠️ | Galan › Plateau de Lannemezan | 1 |
| Bois de Galan (34) ⚠️ | Galan › Plateau de Lannemezan | 1 |
| Parc de Galan ⚠️ | Galan › Plateau de Lannemezan | 1 |
| Bois de Galan (47) ⚠️ | Galan › Plateau de Lannemezan | 1 |
| Bois de Galan (54) ⚠️ | Galan › Plateau de Lannemezan | 1 |
| Bois de Galan (55) ⚠️ | Galan › Plateau de Lannemezan | 1 |
| Bois de Galan (58) ⚠️ | Galan › Plateau de Lannemezan | 1 |
| Bois de Galan (60) ⚠️ | Galan › Plateau de Lannemezan | 1 |
| Forêt de Galan (4) ⚠️ | Galan › Plateau de Lannemezan | 1 |
| Bois de Galan (75) ⚠️ | Galan › Plateau de Lannemezan | 1 |
| Bois de Galan (77) ⚠️ | Galan › Plateau de Lannemezan | 1 |
| Bois de Galan (81) ⚠️ | Galan › Plateau de Lannemezan | 1 |
| Bois de Galan (96) ⚠️ | Galan › Plateau de Lannemezan | 1 |
| Forêt de Galan (6) ⚠️ | Galan › Plateau de Lannemezan | 1 |
| Bois de Sentous (7) ⚠️ | Libaros › Plateau de Lannemezan | 1 |
| Bois de Tournous-Devant (3) ⚠️ | Libaros › Plateau de Lannemezan | 1 |
| Bois de Sentous (8) ⚠️ | Sentous › Plateau de Lannemezan | 1 |
| Bois de Puydarrieux (7) ⚠️ | Puydarrieux › Pays de Trie et du Magnoac | 1 |
| Bois de Sentous (11) ⚠️ | Sentous › Plateau de Lannemezan | 1 |
| Bois de Libaros (24) ⚠️ | Libaros › Plateau de Lannemezan | 1 |
| Bois de Sentous (13) ⚠️ | Sentous › Plateau de Lannemezan | 1 |
| Bois de Libaros (25) ⚠️ | Libaros › Plateau de Lannemezan | 1 |
| Bois de Puydarrieux (8) ⚠️ | Puydarrieux › Pays de Trie et du Magnoac | 1 |
| Forêt de Puydarrieux (3) ⚠️ | Puydarrieux › Pays de Trie et du Magnoac | 1 |
| Forêt de Campuzan ⚠️ | Campuzan › Pays de Trie et du Magnoac | 1 |
| Forêt de Devèze ⚠️ | Devèze › Pays de Trie et du Magnoac | 1 |
| Bois de Juillan (2) ⚠️ | Juillan › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Sentous (24) ⚠️ | Sentous › Plateau de Lannemezan | 1 |
| Bois de Sentous (27) ⚠️ | Sentous › Plateau de Lannemezan | 1 |
| Forêt de Puydarrieux (4) ⚠️ | Puydarrieux › Pays de Trie et du Magnoac | 1 |
| Forêt de Puydarrieux (6) ⚠️ | Puydarrieux › Pays de Trie et du Magnoac | 1 |
| Bois de Puydarrieux (40) ⚠️ | Puydarrieux › Pays de Trie et du Magnoac | 1 |
| Bois de Puydarrieux (41) ⚠️ | Puydarrieux › Pays de Trie et du Magnoac | 1 |
| Bois de Puydarrieux (44) ⚠️ | Puydarrieux › Pays de Trie et du Magnoac | 1 |
| Forêt de Puydarrieux (9) ⚠️ | Puydarrieux › Pays de Trie et du Magnoac | 1 |
| Bois de Puydarrieux (65) ⚠️ | Puydarrieux › Pays de Trie et du Magnoac | 1 |
| Bois de Puydarrieux (68) ⚠️ | Puydarrieux › Pays de Trie et du Magnoac | 1 |
| Forêt de Puydarrieux (12) ⚠️ | Puydarrieux › Pays de Trie et du Magnoac | 1 |
| Bois de Campuzan (8) ⚠️ | Campuzan › Pays de Trie et du Magnoac | 1 |
| Bois de Sadournin (23) ⚠️ | Sadournin › Pays de Trie et du Magnoac | 1 |
| Bois de Sadournin (47) ⚠️ | Sadournin › Pays de Trie et du Magnoac | 1 |
| Forêt de Sadournin (2) ⚠️ | Sadournin › Pays de Trie et du Magnoac | 1 |
| Forêt de Sadournin (3) ⚠️ | Sadournin › Pays de Trie et du Magnoac | 1 |
| Bois de Guizerix (9) ⚠️ | Guizerix › Pays de Trie et du Magnoac | 1 |
| Bois de Guizerix (13) ⚠️ | Guizerix › Pays de Trie et du Magnoac | 1 |
| Bois de Guizerix (22) ⚠️ | Guizerix › Pays de Trie et du Magnoac | 1 |
| Bois de Guizerix (24) ⚠️ | Guizerix › Pays de Trie et du Magnoac | 1 |
| Bois de Guizerix (31) ⚠️ | Guizerix › Pays de Trie et du Magnoac | 1 |
| Forêt de Puntous (2) ⚠️ | Puntous › Pays de Trie et du Magnoac | 1 |
| Bois de Puntous (13) ⚠️ | Puntous › Pays de Trie et du Magnoac | 1 |
| Bois de Larroque (13) ⚠️ | Larroque › Pays de Trie et du Magnoac | 1 |
| Bois de Puntous (21) ⚠️ | Puntous › Pays de Trie et du Magnoac | 1 |
| Bois de Larroque (15) ⚠️ | Puntous › Pays de Trie et du Magnoac | 1 |
| Bois de Larroque (17) ⚠️ | Larroque › Pays de Trie et du Magnoac | 1 |
| Bois de Larroque (18) ⚠️ | Larroque › Pays de Trie et du Magnoac | 1 |
| Forêt de Puntous (3) ⚠️ | Puntous › Pays de Trie et du Magnoac | 1 |
| Bois de Larroque (21) ⚠️ | Larroque › Pays de Trie et du Magnoac | 1 |
| Bois de Vieuzos ⚠️ | Vieuzos › Pays de Trie et du Magnoac | 1 |
| Bois de Betpouy (4) ⚠️ | Vieuzos › Pays de Trie et du Magnoac | 1 |
| Bois de Barthe (3) ⚠️ | Barthe › Pays de Trie et du Magnoac | 1 |
| Bois de Betpouy (12) ⚠️ | Betpouy › Pays de Trie et du Magnoac | 1 |
| Forêt de Sabarros ⚠️ | Sabarros › Plateau de Lannemezan | 1 |
| Bois de Hachan (8) ⚠️ | Hachan › Pays de Trie et du Magnoac | 1 |
| Bois de Vieuzos (8) ⚠️ | Vieuzos › Pays de Trie et du Magnoac | 1 |
| Bois de Vieuzos (11) ⚠️ | Vieuzos › Pays de Trie et du Magnoac | 1 |
| Bois de Vieuzos (13) ⚠️ | Vieuzos › Pays de Trie et du Magnoac | 1 |
| Bois de Vieuzos (16) ⚠️ | Vieuzos › Pays de Trie et du Magnoac | 1 |
| Forêt de Sabarros (4) ⚠️ | Sabarros › Plateau de Lannemezan | 1 |
| Forêt de Recurt (9) ⚠️ | Recurt › Plateau de Lannemezan | 1 |
| Forêt de Recurt (10) ⚠️ | Recurt › Plateau de Lannemezan | 1 |
| Bois de Tajan ⚠️ | Tajan › Plateau de Lannemezan | 1 |
| Forêt de Recurt (12) ⚠️ | Recurt › Plateau de Lannemezan | 1 |
| Forêt de Tajan (4) ⚠️ | Tajan › Plateau de Lannemezan | 1 |
| Forêt de Recurt (19) ⚠️ | Recurt › Plateau de Lannemezan | 1 |
| Forêt de Monlong (2) ⚠️ | Monlong › Pays de Trie et du Magnoac | 1 |
| Bois de Peyret-Saint-André (13) ⚠️ | Peyret-Saint-André › Pays de Trie et du Magnoac | 1 |
| Bois de Peyret-Saint-André (14) ⚠️ | Peyret-Saint-André › Pays de Trie et du Magnoac | 1 |
| Bois de Castelnau-Magnoac ⚠️ | Castelnau-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Peyret-Saint-André (27) ⚠️ | Peyret-Saint-André › Pays de Trie et du Magnoac | 1 |
| Bois de Castelnau-Magnoac (2) ⚠️ | Larroque › Pays de Trie et du Magnoac | 1 |
| Bois de Peyret-Saint-André (36) ⚠️ | Peyret-Saint-André › Pays de Trie et du Magnoac | 1 |
| Bois de Peyret-Saint-André (44) ⚠️ | Peyret-Saint-André › Pays de Trie et du Magnoac | 1 |
| Bois de Castelnau-Magnoac (5) ⚠️ | Peyret-Saint-André › Pays de Trie et du Magnoac | 1 |
| Forêt de Larroque (11) ⚠️ | Larroque › Pays de Trie et du Magnoac | 1 |
| Bois de Castelnau-Magnoac (40) ⚠️ | Castelnau-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Castelnau-Magnoac (52) ⚠️ | Castelnau-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Castelnau-Magnoac (55) ⚠️ | Castelnau-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Castelnau-Magnoac (61) ⚠️ | Castelnau-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Castelnau-Magnoac (62) ⚠️ | Castelnau-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Castelnau-Magnoac (72) ⚠️ | Castelnau-Magnoac › Pays de Trie et du Magnoac | 1 |
| Forêt de Castelnau-Magnoac (3) ⚠️ | Castelnau-Magnoac › Pays de Trie et du Magnoac | 1 |
| Forêt de Castelnau-Magnoac (4) ⚠️ | Castelnau-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Castelnau-Magnoac (75) ⚠️ | Castelnau-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Sariac-Magnoac ⚠️ | Sariac-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Castelnau-Magnoac (78) ⚠️ | Castelnau-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Castelnau-Magnoac (82) ⚠️ | Castelnau-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Organ (3) ⚠️ | Organ › Pays de Trie et du Magnoac | 1 |
| Bois de Sariac-Magnoac (3) ⚠️ | Sariac-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Castelnau-Magnoac (94) ⚠️ | Castelnau-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Castelnau-Magnoac (98) ⚠️ | Castelnau-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Castelnau-Magnoac (105) ⚠️ | Castelnau-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Castelnau-Magnoac (111) ⚠️ | Castelnau-Magnoac › Pays de Trie et du Magnoac | 1 |
| Forêt de Organ ⚠️ | Organ › Pays de Trie et du Magnoac | 1 |
| Bois de Cizos (9) ⚠️ | Cizos › Pays de Trie et du Magnoac | 1 |
| Bois de Organ (4) ⚠️ | Organ › Pays de Trie et du Magnoac | 1 |
| Bois de Organ (6) ⚠️ | Organ › Pays de Trie et du Magnoac | 1 |
| Bois de Cizos (17) ⚠️ | Cizos › Pays de Trie et du Magnoac | 1 |
| Bois de Cizos (19) ⚠️ | Cizos › Pays de Trie et du Magnoac | 1 |
| Forêt de Cizos (2) ⚠️ | Cizos › Pays de Trie et du Magnoac | 1 |
| Forêt de Caubous (2) ⚠️ | Caubous › Pays de Trie et du Magnoac | 1 |
| Forêt de Caubous (3) ⚠️ | Caubous › Pays de Trie et du Magnoac | 1 |
| Forêt de Laran (3) ⚠️ | Laran › Pays de Trie et du Magnoac | 1 |
| Forêt de Caubous (6) ⚠️ | Caubous › Pays de Trie et du Magnoac | 1 |
| Forêt de Caubous (7) ⚠️ | Caubous › Pays de Trie et du Magnoac | 1 |
| Forêt de Cizos (6) ⚠️ | Cizos › Pays de Trie et du Magnoac | 1 |
| Forêt de Cizos (9) ⚠️ | Cizos › Pays de Trie et du Magnoac | 1 |
| Forêt de Cizos (10) ⚠️ | Cizos › Pays de Trie et du Magnoac | 1 |
| Bois de Monléon-Magnoac (4) ⚠️ | Monléon-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Gaussan (10) ⚠️ | Gaussan › Pays de Trie et du Magnoac | 1 |
| Forêt de Caubous (11) ⚠️ | Caubous › Pays de Trie et du Magnoac | 1 |
| Bois de Monlong (5) ⚠️ | Monlong › Pays de Trie et du Magnoac | 1 |
| Forêt de Monlong (3) ⚠️ | Monlong › Pays de Trie et du Magnoac | 1 |
| Bois de Tajan (6) ⚠️ | Tajan › Plateau de Lannemezan | 1 |
| Bois de Monlong (26) ⚠️ | Monlong › Pays de Trie et du Magnoac | 1 |
| Bois de Tajan (15) ⚠️ | Tajan › Plateau de Lannemezan | 1 |
| Bois de Monlong (35) ⚠️ | Monlong › Pays de Trie et du Magnoac | 1 |
| Bois de Monlong (36) ⚠️ | Monlong › Pays de Trie et du Magnoac | 1 |
| Forêt de Monlong (4) ⚠️ | Monlong › Pays de Trie et du Magnoac | 1 |
| Bois de Tajan (26) ⚠️ | Tajan › Plateau de Lannemezan | 1 |
| Bois de Réjaumont (17) ⚠️ | Réjaumont › Plateau de Lannemezan | 1 |
| Forêt de Réjaumont (7) ⚠️ | Réjaumont › Plateau de Lannemezan | 1 |
| Forêt de Tajan (6) ⚠️ | Tajan › Plateau de Lannemezan | 1 |
| Forêt de Réjaumont (14) ⚠️ | Réjaumont › Plateau de Lannemezan | 1 |
| Forêt de Réjaumont (20) ⚠️ | Réjaumont › Plateau de Lannemezan | 1 |
| Forêt de Réjaumont (21) ⚠️ | Réjaumont › Plateau de Lannemezan | 1 |
| Forêt de Tajan (8) ⚠️ | Tajan › Plateau de Lannemezan | 1 |
| Bois de Uglas (21) ⚠️ | Uglas › Plateau de Lannemezan | 1 |
| Bois de Uglas (27) ⚠️ | Uglas › Plateau de Lannemezan | 1 |
| Bois de Uglas (28) ⚠️ | Uglas › Plateau de Lannemezan | 1 |
| Forêt de Uglas (7) ⚠️ | Uglas › Plateau de Lannemezan | 1 |
| Bois de Monléon-Magnoac (8) ⚠️ | Monléon-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Monléon-Magnoac (10) ⚠️ | Monléon-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Gaussan (24) ⚠️ | Gaussan › Pays de Trie et du Magnoac | 1 |
| Bois de Monléon-Magnoac (13) ⚠️ | Monléon-Magnoac › Pays de Trie et du Magnoac | 1 |
| Forêt de Gaussan (4) ⚠️ | Gaussan › Pays de Trie et du Magnoac | 1 |
| Bois de Monléon-Magnoac (39) ⚠️ | Monléon-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Monléon-Magnoac (43) ⚠️ | Monléon-Magnoac › Pays de Trie et du Magnoac | 1 |
| Parc de Monléon-Magnoac (3) ⚠️ | Monléon-Magnoac › Pays de Trie et du Magnoac | 1 |
| Forêt de Monléon-Magnoac (12) ⚠️ | Monléon-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Monléon-Magnoac (93) ⚠️ | Monléon-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Monléon-Magnoac (101) ⚠️ | Monléon-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Pouy (2) ⚠️ | Pouy › Pays de Trie et du Magnoac | 1 |
| Bois de Aries-Espénan (7) ⚠️ | Aries-Espénan › Pays de Trie et du Magnoac | 1 |
| Bois de Aries-Espénan (12) ⚠️ | Aries-Espénan › Pays de Trie et du Magnoac | 1 |
| Bois de Pouy (8) ⚠️ | Pouy › Pays de Trie et du Magnoac | 1 |
| Bois de Villemur (15) ⚠️ | Villemur › Pays de Trie et du Magnoac | 1 |
| Bois de Pouy (14) ⚠️ | Pouy › Pays de Trie et du Magnoac | 1 |
| Bois de Arné (12) ⚠️ | Arné › Plateau de Lannemezan | 1 |
| Bois de Arné (20) ⚠️ | Arné › Plateau de Lannemezan | 1 |
| Bois de Arné (22) ⚠️ | Arné › Plateau de Lannemezan | 1 |
| Bois de Arné (33) ⚠️ | Arné › Plateau de Lannemezan | 1 |
| Forêt de Arné (5) ⚠️ | Arné › Plateau de Lannemezan | 1 |
| Forêt de Arné (7) ⚠️ | Arné › Plateau de Lannemezan | 1 |
| Forêt de Arné (12) ⚠️ | Arné › Plateau de Lannemezan | 1 |
| Forêt de Arné (14) ⚠️ | Arné › Plateau de Lannemezan | 1 |
| Forêt de Arné (15) ⚠️ | Arné › Plateau de Lannemezan | 1 |
| Bois de Sariac-Magnoac (11) ⚠️ | Sariac-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Villemur (20) ⚠️ | Lalanne › Pays de Trie et du Magnoac | 1 |
| Bois de Lalanne ⚠️ | Lalanne › Pays de Trie et du Magnoac | 1 |
| Bois de Devèze (24) ⚠️ | Devèze › Pays de Trie et du Magnoac | 1 |
| Bois de Devèze (26) ⚠️ | Devèze › Pays de Trie et du Magnoac | 1 |
| Bois de Lalanne (3) ⚠️ | Lalanne › Pays de Trie et du Magnoac | 1 |
| Bois de Lalanne (18) ⚠️ | Lalanne › Pays de Trie et du Magnoac | 1 |
| Bois de Lalanne (19) ⚠️ | Lalanne › Pays de Trie et du Magnoac | 1 |
| Bois de Lalanne (22) ⚠️ | Lalanne › Pays de Trie et du Magnoac | 1 |
| Forêt de Thermes-Magnoac (2) ⚠️ | Thermes-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Lalanne (24) ⚠️ | Lalanne › Pays de Trie et du Magnoac | 1 |
| Bois de Betbèze (3) ⚠️ | Betbèze › Pays de Trie et du Magnoac | 1 |
| Bois de Thermes-Magnoac (17) ⚠️ | Thermes-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Thermes-Magnoac (33) ⚠️ | Thermes-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Lalanne (31) ⚠️ | Lalanne › Pays de Trie et du Magnoac | 1 |
| Bois de Thermes-Magnoac (37) ⚠️ | Thermes-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Thermes-Magnoac (38) ⚠️ | Thermes-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Thermes-Magnoac (42) ⚠️ | Thermes-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Thermes-Magnoac (43) ⚠️ | Thermes-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Thermes-Magnoac (44) ⚠️ | Thermes-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Thermes-Magnoac (45) ⚠️ | Thermes-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Lalanne (35) ⚠️ | Lalanne › Pays de Trie et du Magnoac | 1 |
| Bois de Thermes-Magnoac (46) ⚠️ | Thermes-Magnoac › Pays de Trie et du Magnoac | 1 |
| Forêt de Thermes-Magnoac (3) ⚠️ | Thermes-Magnoac › Pays de Trie et du Magnoac | 1 |
| Forêt de Thermes-Magnoac (6) ⚠️ | Thermes-Magnoac › Pays de Trie et du Magnoac | 1 |
| Forêt de Betbèze (2) ⚠️ | Betbèze › Pays de Trie et du Magnoac | 1 |
| Forêt de Lalanne (3) ⚠️ | Lalanne › Pays de Trie et du Magnoac | 1 |
| Bois de Thermes-Magnoac (53) ⚠️ | Thermes-Magnoac › Pays de Trie et du Magnoac | 1 |
| Forêt de Thermes-Magnoac (12) ⚠️ | Thermes-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Lalanne (42) ⚠️ | Lalanne › Pays de Trie et du Magnoac | 1 |
| Bois de Thermes-Magnoac (59) ⚠️ | Thermes-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Thermes-Magnoac (60) ⚠️ | Thermes-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Thermes-Magnoac (81) ⚠️ | Thermes-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Sariac-Magnoac (61) ⚠️ | Sariac-Magnoac › Pays de Trie et du Magnoac | 1 |
| Forêt de Sariac-Magnoac (2) ⚠️ | Sariac-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Sariac-Magnoac (70) ⚠️ | Sariac-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Sariac-Magnoac (75) ⚠️ | Sariac-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Sariac-Magnoac (76) ⚠️ | Sariac-Magnoac › Pays de Trie et du Magnoac | 1 |
| Forêt de Sariac-Magnoac (3) ⚠️ | Sariac-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Bazordan (2) ⚠️ | Bazordan › Pays de Trie et du Magnoac | 1 |
| Bois de Bazordan (8) ⚠️ | Bazordan › Pays de Trie et du Magnoac | 1 |
| Bois de Bazordan (11) ⚠️ | Bazordan › Pays de Trie et du Magnoac | 1 |
| Forêt de Bazordan (2) ⚠️ | Bazordan › Pays de Trie et du Magnoac | 1 |
| Bois de Bazordan (44) ⚠️ | Bazordan › Pays de Trie et du Magnoac | 1 |
| Bois de Bazordan (47) ⚠️ | Bazordan › Pays de Trie et du Magnoac | 1 |
| Bois de Bazordan (49) ⚠️ | Bazordan › Pays de Trie et du Magnoac | 1 |
| Bois de Bazordan (51) ⚠️ | Bazordan › Pays de Trie et du Magnoac | 1 |
| Bois de Bazordan (56) ⚠️ | Bazordan › Pays de Trie et du Magnoac | 1 |
| Forêt de Bazordan (8) ⚠️ | Bazordan › Pays de Trie et du Magnoac | 1 |
| Forêt de Bazordan (9) ⚠️ | Bazordan › Pays de Trie et du Magnoac | 1 |
| Forêt de Bazordan (11) ⚠️ | Bazordan › Pays de Trie et du Magnoac | 1 |
| Forêt de Bazordan (12) ⚠️ | Bazordan › Pays de Trie et du Magnoac | 1 |
| Bois de Bazordan (59) ⚠️ | Bazordan › Pays de Trie et du Magnoac | 1 |
| Forêt de Bazordan (16) ⚠️ | Bazordan › Pays de Trie et du Magnoac | 1 |
| Bois de Pinas (5) ⚠️ | Pinas › Plateau de Lannemezan | 1 |
| Bois de Pinas (11) ⚠️ | Pinas › Plateau de Lannemezan | 1 |
| Bois de Pinas (14) ⚠️ | Pinas › Plateau de Lannemezan | 1 |
| Bois de Pinas (15) ⚠️ | Pinas › Plateau de Lannemezan | 1 |
| Bois de Pinas (18) ⚠️ | Pinas › Plateau de Lannemezan | 1 |
| Bois de Pinas (23) ⚠️ | Pinas › Plateau de Lannemezan | 1 |
| Bois de Pinas (26) ⚠️ | Pinas › Plateau de Lannemezan | 1 |
| Bois de Pinas (27) ⚠️ | Pinas › Plateau de Lannemezan | 1 |
| Bois de Pinas (28) ⚠️ | Pinas › Plateau de Lannemezan | 1 |
| Bois de Pinas (31) ⚠️ | Pinas › Plateau de Lannemezan | 1 |
| Bois de Pinas (44) ⚠️ | Pinas › Plateau de Lannemezan | 1 |
| Bois de Saint-Laurent-de-Neste (10) ⚠️ | Saint-Laurent-de-Neste › Neste Barousse | 1 |
| Bois de Cantaous (14) ⚠️ | Cantaous › Neste Barousse | 1 |
| Forêt de Saint-Laurent-de-Neste ⚠️ | Saint-Laurent-de-Neste › Neste Barousse | 1 |
| Forêt de Saint-Laurent-de-Neste (2) ⚠️ | Saint-Laurent-de-Neste › Neste Barousse | 1 |
| Bois de Saint-Laurent-de-Neste (17) ⚠️ | Saint-Laurent-de-Neste › Neste Barousse | 1 |
| Bois de Saint-Paul (7) ⚠️ | Saint-Paul › Neste Barousse | 1 |
| Bois de Saint-Laurent-de-Neste (20) ⚠️ | Saint-Paul › Neste Barousse | 1 |
| Bois de Saint-Paul (10) ⚠️ | Saint-Paul › Neste Barousse | 1 |
| Bois de Saint-Paul (11) ⚠️ | Saint-Paul › Neste Barousse | 1 |
| Bois de Saint-Laurent-de-Neste (26) ⚠️ | Saint-Laurent-de-Neste › Neste Barousse | 1 |
| Forêt de Saint-Paul (6) ⚠️ | Saint-Paul › Neste Barousse | 1 |
| Bois de Saint-Laurent-de-Neste (29) ⚠️ | Saint-Laurent-de-Neste › Neste Barousse | 1 |
| Bois de Saint-Laurent-de-Neste (30) ⚠️ | Saint-Laurent-de-Neste › Neste Barousse | 1 |
| Bois de Cantaous (23) ⚠️ | Cantaous › Neste Barousse | 1 |
| Bois de Saint-Laurent-de-Neste (38) ⚠️ | Saint-Laurent-de-Neste › Neste Barousse | 1 |
| Bois de Saint-Laurent-de-Neste (40) ⚠️ | Saint-Laurent-de-Neste › Neste Barousse | 1 |
| Forêt de Cantaous (4) ⚠️ | Cantaous › Neste Barousse | 1 |
| Forêt de Saint-Paul (11) ⚠️ | Saint-Paul › Neste Barousse | 1 |
| Bois de Cantaous (36) ⚠️ | Cantaous › Neste Barousse | 1 |
| Bois de Cantaous (43) ⚠️ | Cantaous › Neste Barousse | 1 |
| Bois de Cantaous (58) ⚠️ | Cantaous › Neste Barousse | 1 |
| Bois de Cantaous (59) ⚠️ | Cantaous › Neste Barousse | 1 |
| Bois de Cantaous (61) ⚠️ | Cantaous › Neste Barousse | 1 |
| Forêt de Cantaous (8) ⚠️ | Cantaous › Neste Barousse | 1 |
| Forêt de Saint-Laurent-de-Neste (14) ⚠️ | Saint-Laurent-de-Neste › Neste Barousse | 1 |
| Bois de Saint-Laurent-de-Neste (53) ⚠️ | Saint-Laurent-de-Neste › Neste Barousse | 1 |
| Bois de Saint-Laurent-de-Neste (62) ⚠️ | Saint-Laurent-de-Neste › Neste Barousse | 1 |
| Bois de Saint-Paul (17) ⚠️ | Saint-Paul › Neste Barousse | 1 |
| Bois de Saint-Laurent-de-Neste (72) ⚠️ | Saint-Laurent-de-Neste › Neste Barousse | 1 |
| Bois de Saint-Laurent-de-Neste (78) ⚠️ | Saint-Laurent-de-Neste › Neste Barousse | 1 |
| Forêt de Saint-Laurent-de-Neste (17) ⚠️ | Saint-Laurent-de-Neste › Neste Barousse | 1 |
| Forêt de Saint-Laurent-de-Neste (18) ⚠️ | Saint-Laurent-de-Neste › Neste Barousse | 1 |
| Bois de Saint-Laurent-de-Neste (96) ⚠️ | Saint-Laurent-de-Neste › Neste Barousse | 1 |
| Forêt de Saint-Paul (15) ⚠️ | Saint-Paul › Neste Barousse | 1 |
| Forêt de Saint-Paul (16) ⚠️ | Saint-Paul › Neste Barousse | 1 |
| Bois de Anères (4) ⚠️ | Anères › Neste Barousse | 1 |
| Bois de Saint-Paul (29) ⚠️ | Saint-Paul › Neste Barousse | 1 |
| Bois de Saint-Paul (33) ⚠️ | Saint-Paul › Neste Barousse | 1 |
| Bois de Mazères-de-Neste (6) ⚠️ | Mazères-de-Neste › Neste Barousse | 1 |
| Bois de Tibiran-Jaunac (3) ⚠️ | Tibiran-Jaunac › Neste Barousse | 1 |
| Bois de Mazères-de-Neste (18) ⚠️ | Mazères-de-Neste › Neste Barousse | 1 |
| Bois de Mazères-de-Neste (19) ⚠️ | Mazères-de-Neste › Neste Barousse | 1 |
| Bois de Mazères-de-Neste (21) ⚠️ | Mazères-de-Neste › Neste Barousse | 1 |
| Bois de Aventignan (10) ⚠️ | Aventignan › Neste Barousse | 1 |
| Bois de Saint-Paul (50) ⚠️ | Saint-Paul › Neste Barousse | 1 |
| Bois de Saint-Paul (53) ⚠️ | Saint-Paul › Neste Barousse | 1 |
| Forêt de Saint-Paul (17) ⚠️ | Saint-Paul › Neste Barousse | 1 |
| Forêt de Mazères-de-Neste (2) ⚠️ | Mazères-de-Neste › Neste Barousse | 1 |
| Forêt de Tibiran-Jaunac (4) ⚠️ | Tibiran-Jaunac › Neste Barousse | 1 |
| Forêt de Mazères-de-Neste (4) ⚠️ | Mazères-de-Neste › Neste Barousse | 1 |
| Forêt de Saint-Paul (22) ⚠️ | Saint-Paul › Neste Barousse | 1 |
| Forêt de Mazères-de-Neste (5) ⚠️ | Mazères-de-Neste › Neste Barousse | 1 |
| Forêt de Saint-Paul (24) ⚠️ | Saint-Paul › Neste Barousse | 1 |
| Forêt de Saint-Paul (25) ⚠️ | Saint-Paul › Neste Barousse | 1 |
| Forêt de Mazères-de-Neste (7) ⚠️ | Mazères-de-Neste › Neste Barousse | 1 |
| Bois de Mazères-de-Neste (32) ⚠️ | Mazères-de-Neste › Neste Barousse | 1 |
| Bois de Mazères-de-Neste (33) ⚠️ | Mazères-de-Neste › Neste Barousse | 1 |
| Bois de Tibiran-Jaunac (13) ⚠️ | Tibiran-Jaunac › Neste Barousse | 1 |
| Bois de Tibiran-Jaunac (25) ⚠️ | Tibiran-Jaunac › Neste Barousse | 1 |
| Bois de Tibiran-Jaunac (31) ⚠️ | Tibiran-Jaunac › Neste Barousse | 1 |
| Bois de Tibiran-Jaunac (36) ⚠️ | Tibiran-Jaunac › Neste Barousse | 1 |
| Bois de Tibiran-Jaunac (41) ⚠️ | Tibiran-Jaunac › Neste Barousse | 1 |
| Forêt de Tibiran-Jaunac (9) ⚠️ | Tibiran-Jaunac › Neste Barousse | 1 |
| Forêt de Tibiran-Jaunac (11) ⚠️ | Tibiran-Jaunac › Neste Barousse | 1 |
| Forêt de Tibiran-Jaunac (12) ⚠️ | Tibiran-Jaunac › Neste Barousse | 1 |
| Forêt de Tibiran-Jaunac (13) ⚠️ | Tibiran-Jaunac › Neste Barousse | 1 |
| Forêt de Tibiran-Jaunac (14) ⚠️ | Tibiran-Jaunac › Neste Barousse | 1 |
| Bois de Aventignan (12) ⚠️ | Aventignan › Neste Barousse | 1 |
| Bois de Aventignan (14) ⚠️ | Aventignan › Neste Barousse | 1 |
| Bois de Générest (3) ⚠️ | Générest › Neste Barousse | 1 |
| Bois de Lombrès ⚠️ | Lombrès › Neste Barousse | 1 |
| Bois de Aventignan (32) ⚠️ | Aventignan › Neste Barousse | 1 |
| Bois de Ourde ⚠️ | Ourde › Neste Barousse | 1 |
| Bois de Gaudent (13) ⚠️ | Gaudent › Neste Barousse | 1 |
| Forêt de Lombrès (2) ⚠️ | Lombrès › Neste Barousse | 1 |
| Bois de Générest (14) ⚠️ | Générest › Neste Barousse | 1 |
| Bois de Générest (17) ⚠️ | Générest › Neste Barousse | 1 |
| Bois de Générest (23) ⚠️ | Générest › Neste Barousse | 1 |
| Bois de Générest (26) ⚠️ | Générest › Neste Barousse | 1 |
| Bois de Izaourt ⚠️ | Izaourt › Neste Barousse | 1 |
| Bois de Loures-Barousse (12) ⚠️ | Loures-Barousse › Neste Barousse | 1 |
| Bois de Loures-Barousse (16) ⚠️ | Loures-Barousse › Neste Barousse | 1 |
| Bois de Izaourt (3) ⚠️ | Izaourt › Neste Barousse | 1 |
| Forêt de Loures-Barousse ⚠️ | Loures-Barousse › Neste Barousse | 1 |
| Forêt de Loures-Barousse (2) ⚠️ | Loures-Barousse › Neste Barousse | 1 |
| Bois de Izaourt (9) ⚠️ | Izaourt › Neste Barousse | 1 |
| Bois de Izaourt (13) ⚠️ | Izaourt › Neste Barousse | 1 |
| Bois de Izaourt (14) ⚠️ | Izaourt › Neste Barousse | 1 |
| Bois de Izaourt (20) ⚠️ | Izaourt › Neste Barousse | 1 |
| Bois de Anla (8) ⚠️ | Anla › Neste Barousse | 1 |
| Bois de Anla (9) ⚠️ | Anla › Neste Barousse | 1 |
| Forêt de Anla (3) ⚠️ | Anla › Neste Barousse | 1 |
| Forêt de Anla (4) ⚠️ | Anla › Neste Barousse | 1 |
| Bois de Samuran (7) ⚠️ | Samuran › Neste Barousse | 1 |
| Bois de Créchets (7) ⚠️ | Créchets › Neste Barousse | 1 |
| Bois de Ilheu (10) ⚠️ | Ilheu › Neste Barousse | 1 |
| Bois de Gembrie (6) ⚠️ | Gembrie › Neste Barousse | 1 |
| Bois de Antichan (17) ⚠️ | Anla › Neste Barousse | 1 |
| Bois de Gembrie (9) ⚠️ | Gembrie › Neste Barousse | 1 |
| Bois de Troubat (8) ⚠️ | Troubat › Neste Barousse | 1 |
| Bois de Antichan (21) ⚠️ | Antichan › Neste Barousse | 1 |
| Forêt de Bramevaque ⚠️ | Bramevaque › Neste Barousse | 1 |
| Bois de Mauléon-Barousse ⚠️ | Mauléon-Barousse › Neste Barousse | 1 |
| Bois de Mauléon-Barousse (7) ⚠️ | Mauléon-Barousse › Neste Barousse | 1 |
| Bois de Mauléon-Barousse (10) ⚠️ | Mauléon-Barousse › Neste Barousse | 1 |
| Bois de Mauléon-Barousse (11) ⚠️ | Mauléon-Barousse › Neste Barousse | 1 |
| Bois de Thèbe (12) ⚠️ | Thèbe › Neste Barousse | 1 |
| Forêt de Cazarilh ⚠️ | Cazarilh › Neste Barousse | 1 |
| Bois de Saléchan (4) ⚠️ | Saléchan › Neste Barousse | 1 |
| Bois de Saléchan (9) ⚠️ | Saléchan › Neste Barousse | 1 |
| Bois de Sainte-Marie (4) ⚠️ | Saléchan › Neste Barousse | 1 |
| Bois de Bertren (23) ⚠️ | Bertren › Neste Barousse | 1 |
| Bois de Siradan ⚠️ | Siradan › Neste Barousse | 1 |
| Bois de Siradan (11) ⚠️ | Siradan › Neste Barousse | 1 |
| Bois de Siradan (13) ⚠️ | Siradan › Neste Barousse | 1 |
| Bois de Sost ⚠️ | Sost › Neste Barousse | 1 |
| Bois de Esbareich (5) ⚠️ | Esbareich › Neste Barousse | 1 |
| Bois de Esbareich (6) ⚠️ | Esbareich › Neste Barousse | 1 |
| Bois de Cazarilh (12) ⚠️ | Cazarilh › Neste Barousse | 1 |
| Forêt de Saléchan ⚠️ | Saléchan › Neste Barousse | 1 |
| Bois de Saléchan (31) ⚠️ | Saléchan › Neste Barousse | 1 |
| Bois de Thèbe (28) ⚠️ | Thèbe › Neste Barousse | 1 |
| Bois de Esbareich (11) ⚠️ | Esbareich › Neste Barousse | 1 |
| Bois de Esbareich (14) ⚠️ | Esbareich › Neste Barousse | 1 |
| Bois de Ferrère (3) ⚠️ | Ferrère › Neste Barousse | 1 |
| Bois de Sost (12) ⚠️ | Sost › Neste Barousse | 1 |
| Bois de Esbareich (39) ⚠️ | Esbareich › Neste Barousse | 1 |
| Bois de Ourde (14) ⚠️ | Ourde › Neste Barousse | 1 |
| Bois de Ourde (21) ⚠️ | Ourde › Neste Barousse | 1 |
| Forêt de Sost (8) ⚠️ | Sost › Neste Barousse | 1 |
| Bois de Sost (24) ⚠️ | Sost › Neste Barousse | 1 |
| Bois de Sost (28) ⚠️ | Sost › Neste Barousse | 1 |
| Bois de Sost (29) ⚠️ | Sost › Neste Barousse | 1 |
| Forêt de Sost (31) ⚠️ | Sost › Neste Barousse | 1 |
| Bois de Ourde (32) ⚠️ | Ourde › Neste Barousse | 1 |
| Forêt de Ferrère (12) ⚠️ | Ferrère › Neste Barousse | 1 |
| Forêt de Ferrère (17) ⚠️ | Ferrère › Neste Barousse | 1 |
| Forêt de Ferrère (33) ⚠️ | Ferrère › Neste Barousse | 1 |
| Forêt de Ferrère (35) ⚠️ | Ferrère › Neste Barousse | 1 |
| Forêt de Ferrère (47) ⚠️ | Ferrère › Neste Barousse | 1 |
| Forêt de Ferrère (51) ⚠️ | Ferrère › Neste Barousse | 1 |
| Forêt de Ferrère (57) ⚠️ | Ferrère › Neste Barousse | 1 |
| Forêt de Ferrère (71) ⚠️ | Ferrère › Neste Barousse | 1 |
| Forêt de Sarrancolin (11) ⚠️ | Sarrancolin › Aure Louron | 1 |
| Bois de Seich (2) ⚠️ | Seich › Neste Barousse | 1 |
| Bois de Nistos ⚠️ | Nistos › Neste Barousse | 1 |
| Bois de Seich (8) ⚠️ | Seich › Neste Barousse | 1 |
| Bois de Seich (9) ⚠️ | Seich › Neste Barousse | 1 |
| Bois de Nistos (3) ⚠️ | Nistos › Neste Barousse | 1 |
| Bois de Nistos (6) ⚠️ | Nistos › Neste Barousse | 1 |
| Bois de Seich (23) ⚠️ | Seich › Neste Barousse | 1 |
| Bois de Seich (26) ⚠️ | Seich › Neste Barousse | 1 |
| Bois de Seich (28) ⚠️ | Seich › Neste Barousse | 1 |
| Forêt de Seich (3) ⚠️ | Seich › Neste Barousse | 1 |
| Bois de Nestier (6) ⚠️ | Nestier › Neste Barousse | 1 |
| Bois de Nistos (13) ⚠️ | Nistos › Neste Barousse | 1 |
| Bois de Montégut (11) ⚠️ | Montégut › Neste Barousse | 1 |
| Bois de Seich (34) ⚠️ | Seich › Neste Barousse | 1 |
| Bois de Nestier (11) ⚠️ | Nestier › Neste Barousse | 1 |
| Bois de Seich (38) ⚠️ | Nistos › Neste Barousse | 1 |
| Bois de Montégut (19) ⚠️ | Montégut › Neste Barousse | 1 |
| Forêt de Montégut (3) ⚠️ | Montégut › Neste Barousse | 1 |
| Forêt de Montégut (5) ⚠️ | Montégut › Neste Barousse | 1 |
| Bois de Bize (23) ⚠️ | Bize › Neste Barousse | 1 |
| Bois de Nistos (40) ⚠️ | Nistos › Neste Barousse | 1 |
| Bois de Nistos (42) ⚠️ | Nistos › Neste Barousse | 1 |
| Bois de Nistos (49) ⚠️ | Nistos › Neste Barousse | 1 |
| Bois de Nistos (58) ⚠️ | Nistos › Neste Barousse | 1 |
| Bois de Bize (29) ⚠️ | Bize › Neste Barousse | 1 |
| Bois de Bize (43) ⚠️ | Bize › Neste Barousse | 1 |
| Bois de Bize (44) ⚠️ | Bize › Neste Barousse | 1 |
| Bois de Bize (47) ⚠️ | Bize › Neste Barousse | 1 |
| Bois de Nestier (16) ⚠️ | Nestier › Neste Barousse | 1 |
| Bois de Bize (65) ⚠️ | Bize › Neste Barousse | 1 |
| Bois de Hautaget (4) ⚠️ | Hautaget › Neste Barousse | 1 |
| Bois de Nestier (40) ⚠️ | Nestier › Neste Barousse | 1 |
| Bois de Hautaget (11) ⚠️ | Hautaget › Neste Barousse | 1 |
| Forêt de Bizous ⚠️ | Bizous › Neste Barousse | 1 |
| Forêt de Tuzaguet (5) ⚠️ | Tuzaguet › Neste Barousse | 1 |
| Bois de Tuzaguet (6) ⚠️ | Tuzaguet › Neste Barousse | 1 |
| Bois de Tuzaguet (11) ⚠️ | Tuzaguet › Neste Barousse | 1 |
| Bois de Tuzaguet (14) ⚠️ | Tuzaguet › Neste Barousse | 1 |
| Bois de Tuzaguet (24) ⚠️ | Tuzaguet › Neste Barousse | 1 |
| Bois de Tuzaguet (36) ⚠️ | Tuzaguet › Neste Barousse | 1 |
| Forêt de Tuzaguet (8) ⚠️ | Tuzaguet › Neste Barousse | 1 |
| Forêt de Bizous (5) ⚠️ | Bizous › Neste Barousse | 1 |
| Bois de Bizous (15) ⚠️ | Bizous › Neste Barousse | 1 |
| Forêt de Bizous (7) ⚠️ | Bizous › Neste Barousse | 1 |
| Bois de Montsérié (9) ⚠️ | Montsérié › Neste Barousse | 1 |
| Bois de Montoussé (8) ⚠️ | Montoussé › Plateau de Lannemezan | 1 |
| Bois de Montoussé (12) ⚠️ | Montoussé › Plateau de Lannemezan | 1 |
| Bois de Montoussé (18) ⚠️ | Montoussé › Plateau de Lannemezan | 1 |
| Forêt de Ferrère (79) ⚠️ | Ferrère › Neste Barousse | 1 |
| Forêt de Montoussé (3) ⚠️ | Montoussé › Plateau de Lannemezan | 1 |
| Bois de Izaux (3) ⚠️ | Izaux › Plateau de Lannemezan | 1 |
| Bois de Bazus-Neste (3) ⚠️ | Bazus-Neste › Plateau de Lannemezan | 1 |
| Bois de La Barthe-de-Neste (3) ⚠️ | La Barthe-de-Neste › Plateau de Lannemezan | 1 |
| Bois de Montoussé (57) ⚠️ | Montoussé › Plateau de Lannemezan | 1 |
| Bois de Mazouau (5) ⚠️ | Mazouau › Plateau de Lannemezan | 1 |
| Bois de Izaux (13) ⚠️ | Izaux › Plateau de Lannemezan | 1 |
| Bois de Izaux (15) ⚠️ | Izaux › Plateau de Lannemezan | 1 |
| Bois de Montoussé (65) ⚠️ | Montoussé › Plateau de Lannemezan | 1 |
| Bois de Izaux (17) ⚠️ | Izaux › Plateau de Lannemezan | 1 |
| Forêt de Hèches (8) ⚠️ | Hèches › Plateau de Lannemezan | 1 |
| Forêt de Saint-Arroman (4) ⚠️ | Saint-Arroman › Plateau de Lannemezan | 1 |
| Forêt de Bazus-Neste (6) ⚠️ | Bazus-Neste › Plateau de Lannemezan | 1 |
| Bois de Montoussé (69) ⚠️ | Montoussé › Plateau de Lannemezan | 1 |
| Bois de Escala (23) ⚠️ | Escala › Plateau de Lannemezan | 1 |
| Bois de Escala (25) ⚠️ | Escala › Plateau de Lannemezan | 1 |
| Bois de La Barthe-de-Neste (19) ⚠️ | La Barthe-de-Neste › Plateau de Lannemezan | 1 |
| Bois de La Barthe-de-Neste (36) ⚠️ | La Barthe-de-Neste › Plateau de Lannemezan | 1 |
| Forêt de La Barthe-de-Neste (8) ⚠️ | La Barthe-de-Neste › Plateau de Lannemezan | 1 |
| Bois de La Barthe-de-Neste (45) ⚠️ | La Barthe-de-Neste › Plateau de Lannemezan | 1 |
| Forêt de La Barthe-de-Neste (14) ⚠️ | La Barthe-de-Neste › Plateau de Lannemezan | 1 |
| Forêt de Izaux (2) ⚠️ | Izaux › Plateau de Lannemezan | 1 |
| Forêt de Jarret (7) ⚠️ | Jarret › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Izaux (21) ⚠️ | Izaux › Plateau de Lannemezan | 1 |
| Forêt de Izaux (7) ⚠️ | Izaux › Plateau de Lannemezan | 1 |
| Bois de Lortet (25) ⚠️ | Lortet › Plateau de Lannemezan | 1 |
| Bois de Izaux (27) ⚠️ | Izaux › Plateau de Lannemezan | 1 |
| Bois de Lortet (28) ⚠️ | Lortet › Plateau de Lannemezan | 1 |
| Forêt de Lortet (9) ⚠️ | Lortet › Plateau de Lannemezan | 1 |
| Bois de Hèches (22) ⚠️ | Hèches › Plateau de Lannemezan | 1 |
| Bois de Hèches (26) ⚠️ | Hèches › Plateau de Lannemezan | 1 |
| Bois de Hèches (30) ⚠️ | Hèches › Plateau de Lannemezan | 1 |
| Bois de Hèches (35) ⚠️ | Hèches › Plateau de Lannemezan | 1 |
| Bois de Hèches (67) ⚠️ | Hèches › Plateau de Lannemezan | 1 |
| Bois de Hèches (71) ⚠️ | Hèches › Plateau de Lannemezan | 1 |
| Forêt de Hèches (9) ⚠️ | Hèches › Plateau de Lannemezan | 1 |
| Forêt de Hèches (12) ⚠️ | Hèches › Plateau de Lannemezan | 1 |
| Forêt de Hèches (13) ⚠️ | Hèches › Plateau de Lannemezan | 1 |
| Bois de Hèches (88) ⚠️ | Hèches › Plateau de Lannemezan | 1 |
| Bois de Sarrancolin (11) ⚠️ | Sarrancolin › Aure Louron | 1 |
| Bois de Sarrancolin (14) ⚠️ | Sarrancolin › Aure Louron | 1 |
| Bois de Ilhet (23) ⚠️ | Ilhet › Aure Louron | 1 |
| Bois de Sarrancolin (16) ⚠️ | Sarrancolin › Aure Louron | 1 |
| Bois de Ilhet (30) ⚠️ | Sarrancolin › Aure Louron | 1 |
| Bois de Ilhet (32) ⚠️ | Ilhet › Aure Louron | 1 |
| Bois de Fréchet-Aure ⚠️ | Fréchet-Aure › Aure Louron | 1 |
| Bois de Ilhet (38) ⚠️ | Ilhet › Aure Louron | 1 |
| Forêt de Ardengost (6) ⚠️ | Ardengost › Aure Louron | 1 |
| Forêt de Ardengost (9) ⚠️ | Ardengost › Aure Louron | 1 |
| Forêt de Ardengost (10) ⚠️ | Ardengost › Aure Louron | 1 |
| Bois de Beyrède-Jumet-Camous (16) ⚠️ | Beyrède-Jumet-Camous › Aure Louron | 1 |
| Bois de Beyrède-Jumet-Camous (18) ⚠️ | Beyrède-Jumet-Camous › Aure Louron | 1 |
| Bois de Arreau (4) ⚠️ | Arreau › Aure Louron | 1 |
| Bois de Arreau (8) ⚠️ | Arreau › Aure Louron | 1 |
| Bois de Aspin-Aure (2) ⚠️ | Aspin-Aure › Aure Louron | 1 |
| Bois de Arreau (9) ⚠️ | Arreau › Aure Louron | 1 |
| Bois de Aspin-Aure (12) ⚠️ | Aspin-Aure › Aure Louron | 1 |
| Bois de Pailhac (6) ⚠️ | Pailhac › Aure Louron | 1 |
| Bois de Pailhac (7) ⚠️ | Pailhac › Aure Louron | 1 |
| Bois de Pailhac (8) ⚠️ | Pailhac › Aure Louron | 1 |
| Bois de Aspin-Aure (14) ⚠️ | Aspin-Aure › Aure Louron | 1 |
| Bois de Aspin-Aure (16) ⚠️ | Aspin-Aure › Aure Louron | 1 |
| Forêt de Aspin-Aure (8) ⚠️ | Aspin-Aure › Aure Louron | 1 |
| Bois de Aspin-Aure (18) ⚠️ | Aspin-Aure › Aure Louron | 1 |
| Bois de Arreau (12) ⚠️ | Arreau › Aure Louron | 1 |
| Bois de Arreau (27) ⚠️ | Arreau › Aure Louron | 1 |
| Bois de Arreau (32) ⚠️ | Arreau › Aure Louron | 1 |
| Bois de Arreau (41) ⚠️ | Arreau › Aure Louron | 1 |
| Bois de Jézeau (8) ⚠️ | Jézeau › Aure Louron | 1 |
| Bois de Jézeau (9) ⚠️ | Jézeau › Aure Louron | 1 |
| Bois de Jézeau (13) ⚠️ | Jézeau › Aure Louron | 1 |
| Bois de Jézeau (14) ⚠️ | Jézeau › Aure Louron | 1 |
| Bois de Jézeau (16) ⚠️ | Jézeau › Aure Louron | 1 |
| Forêt de Bareilles (4) ⚠️ | Bareilles › Aure Louron | 1 |
| Bois de Arreau (51) ⚠️ | Arreau › Aure Louron | 1 |
| Bois de Arreau (53) ⚠️ | Arreau › Aure Louron | 1 |
| Forêt de Barrancoueu (5) ⚠️ | Barrancoueu › Aure Louron | 1 |
| Forêt de Bordères-Louron (5) ⚠️ | Bordères-Louron › Aure Louron | 1 |
| Forêt de Bordères-Louron (6) ⚠️ | Bordères-Louron › Aure Louron | 1 |
| Forêt de Cazaux-Debat (3) ⚠️ | Cazaux-Debat › Aure Louron | 1 |
| Forêt de Bareilles (12) ⚠️ | Bareilles › Aure Louron | 1 |
| Forêt de Bareilles (14) ⚠️ | Bareilles › Aure Louron | 1 |
| Forêt de Bordères-Louron (17) ⚠️ | Bordères-Louron › Aure Louron | 1 |
| Forêt de Bareilles (18) ⚠️ | Bareilles › Aure Louron | 1 |
| Forêt de Bordères-Louron (20) ⚠️ | Bordères-Louron › Aure Louron | 1 |
| Forêt de Bordères-Louron (21) ⚠️ | Bordères-Louron › Aure Louron | 1 |
| Forêt de Bordères-Louron (22) ⚠️ | Bordères-Louron › Aure Louron | 1 |
| Forêt de Bareilles (20) ⚠️ | Bareilles › Aure Louron | 1 |
| Forêt de Bareilles (21) ⚠️ | Bareilles › Aure Louron | 1 |
| Bois de Bordères-Louron (4) ⚠️ | Bordères-Louron › Aure Louron | 1 |
| Bois de Bordères-Louron (13) ⚠️ | Bordères-Louron › Aure Louron | 1 |
| Bois de Bordères-Louron (21) ⚠️ | Bordères-Louron › Aure Louron | 1 |
| Bois de Avajan (8) ⚠️ | Avajan › Aure Louron | 1 |
| Bois de Avajan (13) ⚠️ | Avajan › Aure Louron | 1 |
| Bois de Bordères-Louron (27) ⚠️ | Bordères-Louron › Aure Louron | 1 |
| Bois de Avajan (16) ⚠️ | Avajan › Aure Louron | 1 |
| Forêt de Vielle-Louron (3) ⚠️ | Vielle-Louron › Aure Louron | 1 |
| Bois de Vielle-Louron (4) ⚠️ | Vielle-Louron › Aure Louron | 1 |
| Bois de Vielle-Louron (12) ⚠️ | Vielle-Louron › Aure Louron | 1 |
| Forêt de Vielle-Louron (9) ⚠️ | Vielle-Louron › Aure Louron | 1 |
| Bois de Adervielle-Pouchergues (5) ⚠️ | Adervielle-Pouchergues › Aure Louron | 1 |
| Bois de Estarvielle (5) ⚠️ | Estarvielle › Aure Louron | 1 |
| Forêt de Estarvielle ⚠️ | Estarvielle › Aure Louron | 1 |
| Forêt de Cazaux-Fréchet-Anéran-Camors (20) ⚠️ | Cazaux-Fréchet-Anéran-Camors › Aure Louron | 1 |
| Forêt de Estarvielle (2) ⚠️ | Estarvielle › Aure Louron | 1 |
| Bois de Loudenvielle (6) ⚠️ | Loudenvielle › Aure Louron | 1 |
| Forêt de Mont (14) ⚠️ | Mont › Aure Louron | 1 |
| Forêt de Mont (20) ⚠️ | Mont › Aure Louron | 1 |
| Forêt de Loudervielle (28) ⚠️ | Loudervielle › Aure Louron | 1 |
| Forêt de Estarvielle (10) ⚠️ | Estarvielle › Aure Louron | 1 |
| Forêt de Loudenvielle (7) ⚠️ | Loudenvielle › Aure Louron | 1 |
| Forêt de Mont (32) ⚠️ | Mont › Aure Louron | 1 |
| Bois de Estarvielle (11) ⚠️ | Estarvielle › Aure Louron | 1 |
| Bois de Génos (11) ⚠️ | Génos › Aure Louron | 1 |
| Bois de Génos (14) ⚠️ | Génos › Aure Louron | 1 |
| Bois de Génos (15) ⚠️ | Génos › Aure Louron | 1 |
| Bois de Loudenvielle (33) ⚠️ | Loudenvielle › Aure Louron | 1 |
| Bois de Loudenvielle (34) ⚠️ | Loudenvielle › Aure Louron | 1 |
| Bois de Loudenvielle (35) ⚠️ | Loudenvielle › Aure Louron | 1 |
| Forêt de Loudenvielle (15) ⚠️ | Loudenvielle › Aure Louron | 1 |
| Bois de Génos (24) ⚠️ | Génos › Aure Louron | 1 |
| Bois de Loudenvielle (77) ⚠️ | Loudenvielle › Aure Louron | 1 |
| Bois de Loudenvielle (78) ⚠️ | Loudenvielle › Aure Louron | 1 |
| Bois de Génos (42) ⚠️ | Génos › Aure Louron | 1 |
| Bois de Génos (44) ⚠️ | Génos › Aure Louron | 1 |
| Forêt de Grailhen ⚠️ | Grailhen › Aure Louron | 1 |
| Forêt de Adervielle-Pouchergues (10) ⚠️ | Adervielle-Pouchergues › Aure Louron | 1 |
| Bois de Génos (47) ⚠️ | Génos › Aure Louron | 1 |
| Forêt de Adervielle-Pouchergues (16) ⚠️ | Adervielle-Pouchergues › Aure Louron | 1 |
| Forêt de Loudenvielle (22) ⚠️ | Loudenvielle › Aure Louron | 1 |
| Forêt de Loudenvielle (26) ⚠️ | Loudenvielle › Aure Louron | 1 |
| Forêt de Loudenvielle (27) ⚠️ | Loudenvielle › Aure Louron | 1 |
| Forêt de Loudenvielle (28) ⚠️ | Loudenvielle › Aure Louron | 1 |
| Forêt de Loudenvielle (34) ⚠️ | Loudenvielle › Aure Louron | 1 |
| Forêt de Loudenvielle (44) ⚠️ | Loudenvielle › Aure Louron | 1 |
| Forêt de Loudenvielle (47) ⚠️ | Loudenvielle › Aure Louron | 1 |
| Forêt de Génos (28) ⚠️ | Génos › Aure Louron | 1 |
| Forêt de Génos (29) ⚠️ | Génos › Aure Louron | 1 |
| Forêt de Loudenvielle (50) ⚠️ | Loudenvielle › Aure Louron | 1 |
| Forêt de Loudenvielle (51) ⚠️ | Loudenvielle › Aure Louron | 1 |
| Forêt de Loudenvielle (53) ⚠️ | Loudenvielle › Aure Louron | 1 |
| Forêt de Loudenvielle (54) ⚠️ | Loudenvielle › Aure Louron | 1 |
| Bois de Loudenvielle (99) ⚠️ | Loudenvielle › Aure Louron | 1 |
| Forêt de Loudenvielle (70) ⚠️ | Loudenvielle › Aure Louron | 1 |
| Bois de Jézeau (22) ⚠️ | Jézeau › Aure Louron | 1 |
| Bois de Cazaux-Debat (11) ⚠️ | Cazaux-Debat › Aure Louron | 1 |
| Bois de Cazaux-Debat (12) ⚠️ | Cazaux-Debat › Aure Louron | 1 |
| Bois de Cadéac (8) ⚠️ | Cadéac › Aure Louron | 1 |
| Bois de Cadéac (14) ⚠️ | Cadéac › Aure Louron | 1 |
| Forêt de Ancizan (25) ⚠️ | Ancizan › Aure Louron | 1 |
| Forêt de Ancizan (28) ⚠️ | Ancizan › Aure Louron | 1 |
| Bois de Grézian (3) ⚠️ | Grézian › Aure Louron | 1 |
| Forêt de Guchen ⚠️ | Guchen › Aure Louron | 1 |
| Forêt de Guchen (2) ⚠️ | Guchen › Aure Louron | 1 |
| Forêt de Aulon (3) ⚠️ | Aulon › Aure Louron | 1 |
| Bois de Guchen (15) ⚠️ | Bazus-Aure › Aure Louron | 1 |
| Bois de Camparan (3) ⚠️ | Camparan › Aure Louron | 1 |
| Bois de Guchan (11) ⚠️ | Guchan › Aure Louron | 1 |
| Bois de Guchan (12) ⚠️ | Guchan › Aure Louron | 1 |
| Forêt de Guchan (3) ⚠️ | Guchan › Aure Louron | 1 |
| Bois de Bourisp (4) ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Bois de Vielle-Aure (4) ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Bois de Vielle-Aure (7) ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Base de Loisir d'Agos ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Forêt de Vielle-Aure (102) ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Bois de Sailhan (8) ⚠️ | Sailhan › Aure Louron | 1 |
| Bois de Vielle-Aure (12) ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Bois de Sailhan (13) ⚠️ | Sailhan › Aure Louron | 1 |
| Bois de Azet (32) ⚠️ | Azet › Aure Louron | 1 |
| Bois de Azet (34) ⚠️ | Azet › Aure Louron | 1 |
| Forêt de Estensan (2) ⚠️ | Estensan › Aure Louron | 1 |
| Forêt de Estensan (3) ⚠️ | Azet › Aure Louron | 1 |
| Bois de Azet (43) ⚠️ | Azet › Aure Louron | 1 |
| Bois de Estensan (6) ⚠️ | Ens › Aure Louron | 1 |
| Bois de Azet (48) ⚠️ | Azet › Aure Louron | 1 |
| Bois de Estensan (7) ⚠️ | Estensan › Aure Louron | 1 |
| Bois de Ens (6) ⚠️ | Ens › Aure Louron | 1 |
| Forêt de Azet (26) ⚠️ | Azet › Aure Louron | 1 |
| Forêt de Azet (33) ⚠️ | Azet › Aure Louron | 1 |
| Forêt de Azet (34) ⚠️ | Azet › Aure Louron | 1 |
| Forêt de Ens (4) ⚠️ | Ens › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (27) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (40) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (44) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (47) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (49) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (53) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (55) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (56) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (57) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (61) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (67) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (68) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (71) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (86) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (88) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (90) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (91) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (92) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Bois de Saint-Lary-Soulan (6) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (106) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Tramezaïgues (19) ⚠️ | Tramezaïgues › Aure Louron | 1 |
| Forêt de Tramezaïgues (32) ⚠️ | Tramezaïgues › Aure Louron | 1 |
| Forêt de Tramezaïgues (35) ⚠️ | Tramezaïgues › Aure Louron | 1 |
| Forêt de Tramezaïgues (36) ⚠️ | Tramezaïgues › Aure Louron | 1 |
| Forêt de Tramezaïgues (43) ⚠️ | Tramezaïgues › Aure Louron | 1 |
| Forêt de Tramezaïgues (44) ⚠️ | Tramezaïgues › Aure Louron | 1 |
| Forêt de Tramezaïgues (45) ⚠️ | Tramezaïgues › Aure Louron | 1 |
| Forêt de Tramezaïgues (47) ⚠️ | Tramezaïgues › Aure Louron | 1 |
| Forêt de Tramezaïgues (51) ⚠️ | Tramezaïgues › Aure Louron | 1 |
| Forêt de Tramezaïgues (52) ⚠️ | Tramezaïgues › Aure Louron | 1 |
| Forêt de Tramezaïgues (53) ⚠️ | Tramezaïgues › Aure Louron | 1 |
| Forêt de Tramezaïgues (54) ⚠️ | Tramezaïgues › Aure Louron | 1 |
| Forêt de Tramezaïgues (55) ⚠️ | Tramezaïgues › Aure Louron | 1 |
| Forêt de Tramezaïgues (56) ⚠️ | Tramezaïgues › Aure Louron | 1 |
| Forêt de Tramezaïgues (58) ⚠️ | Tramezaïgues › Aure Louron | 1 |
| Forêt de Tramezaïgues (63) ⚠️ | Tramezaïgues › Aure Louron | 1 |
| Forêt de Tramezaïgues (68) ⚠️ | Tramezaïgues › Aure Louron | 1 |
| Forêt de Tramezaïgues (84) ⚠️ | Tramezaïgues › Aure Louron | 1 |
| Forêt de Tramezaïgues (91) ⚠️ | Tramezaïgues › Aure Louron | 1 |
| Forêt de Aragnouet (7) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (8) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (13) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (22) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (23) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (27) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (49) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (54) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (55) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (63) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (68) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (69) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (71) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (72) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (73) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (76) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (77) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (81) ⚠️ | Aragnouet › Aure Louron | 1 |
| Bois de Aragnouet (29) ⚠️ | Aragnouet › Aure Louron | 1 |
| Bois de Aragnouet (32) ⚠️ | Aragnouet › Aure Louron | 1 |
| Bois de Aragnouet (45) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (98) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (100) ⚠️ | Aragnouet › Aure Louron | 1 |
| Bois de Aragnouet (50) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (105) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (111) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (113) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (118) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (124) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (134) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (128) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Aragnouet (139) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (144) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (131) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (132) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Aragnouet (150) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (151) ⚠️ | Aragnouet › Aure Louron | 1 |
| Bois de Aragnouet (55) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (163) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (172) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (174) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (178) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (180) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Vielle-Aure (110) ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Forêt de Vielle-Aure (111) ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Forêt de Vielle-Aure (126) ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Forêt de Vielle-Aure (147) ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Forêt de Vielle-Aure (154) ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Forêt de Vielle-Aure (158) ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Forêt de Vielle-Aure (161) ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Forêt de Vielle-Aure (165) ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Forêt de Vielle-Aure (169) ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Forêt de Vielle-Aure (175) ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Bois de Aragnouet (61) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Aragnouet (196) ⚠️ | Aragnouet › Aure Louron | 1 |
| Forêt de Cadeilhan-Trachère (5) ⚠️ | Cadeilhan-Trachère › Aure Louron | 1 |
| Forêt de Tramezaïgues (99) ⚠️ | Tramezaïgues › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (143) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Bois de Saint-Lary-Soulan (9) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Vignec (3) ⚠️ | Vignec › Aure Louron | 1 |
| Forêt de Vignec (10) ⚠️ | Vignec › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (153) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Vignec (24) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (168) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Vignec (25) ⚠️ | Vignec › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (170) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (183) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (186) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Vignec (38) ⚠️ | Vignec › Aure Louron | 1 |
| Forêt de Vignec (39) ⚠️ | Vignec › Aure Louron | 1 |
| Forêt de Cadeilhan-Trachère (17) ⚠️ | Cadeilhan-Trachère › Aure Louron | 1 |
| Forêt de Cadeilhan-Trachère (32) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Bois de Vielle-Aure (14) ⚠️ | Bourisp › Aure Louron | 1 |
| Forêt de Bagnères-de-Bigorre (172) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Bagnères-de-Bigorre (181) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Bagnères-de-Bigorre (188) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Campan (291) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Campan (292) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Bagnères-de-Bigorre (190) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Bagnères-de-Bigorre (191) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Bagnères-de-Bigorre (192) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Bagnères-de-Bigorre (193) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Bagnères-de-Bigorre (194) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Bagnères-de-Bigorre (195) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Sers (76) ⚠️ | Sers › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arrens-Marsous (206) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (306) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Barèges (173) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Forêt de Barèges (180) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Forêt de Barèges (183) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Forêt de Barèges (192) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Forêt de Barèges (197) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Forêt de Villelongue (39) ⚠️ | Villelongue › Pyrénées Vallées des Gaves | 1 |
| Forêt de Villelongue (40) ⚠️ | Villelongue › Pyrénées Vallées des Gaves | 1 |
| Forêt de Sazos (42) ⚠️ | Sazos › Pyrénées Vallées des Gaves | 1 |
| Forêt de Vic-en-Bigorre (53) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Liac (2) ⚠️ | Liac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Artagnan (2) ⚠️ | Artagnan › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Liac (4) ⚠️ | Liac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Maubourguet ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Hères (2) ⚠️ | Hères › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Lourdes (47) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lourdes (131) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Pintac (3) ⚠️ | Pintac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Oroix (14) ⚠️ | Oroix › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Oroix (16) ⚠️ | Oroix › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Pintac (4) ⚠️ | Pintac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Tarasteix ⚠️ | Tarasteix › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Tarasteix (13) ⚠️ | Tarasteix › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Tarasteix (16) ⚠️ | Tarasteix › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Luquet (10) ⚠️ | Luquet › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Gardères (2) ⚠️ | Gardères › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Luquet (11) ⚠️ | Luquet › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Luquet (13) ⚠️ | Luquet › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Luquet (16) ⚠️ | Luquet › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Luquet (17) ⚠️ | Gardères › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Luquet (16) ⚠️ | Luquet › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Luquet (17) ⚠️ | Luquet › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Gardères (9) ⚠️ | Gardères › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Luquet (33) ⚠️ | Luquet › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Gardères (35) ⚠️ | Gardères › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Gardères (45) ⚠️ | Gardères › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Gardères (50) ⚠️ | Gardères › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Gardères (53) ⚠️ | Gardères › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Gardères (57) ⚠️ | Gardères › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Gardères (15) ⚠️ | Gardères › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Gardères (72) ⚠️ | Gardères › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Séron (6) ⚠️ | Séron › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Séron (10) ⚠️ | Séron › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Séron (13) ⚠️ | Séron › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Séron (16) ⚠️ | Séron › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Séron (2) ⚠️ | Séron › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Escaunets (5) ⚠️ | Escaunets › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Séron (6) ⚠️ | Séron › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Escaunets (17) ⚠️ | Escaunets › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Villenave-près-Béarn (16) ⚠️ | Villenave-près-Béarn › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vic-en-Bigorre (25) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vic-en-Bigorre (26) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vic-en-Bigorre (33) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vic-en-Bigorre (38) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Nouilhan (5) ⚠️ | Nouilhan › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vic-en-Bigorre (44) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vic-en-Bigorre (47) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vic-en-Bigorre (48) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vic-en-Bigorre (52) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vic-en-Bigorre (53) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vic-en-Bigorre (54) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Caixon ⚠️ | Caixon › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Vic-en-Bigorre (55) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Caixon (6) ⚠️ | Caixon › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Caixon (8) ⚠️ | Caixon › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Sanous (5) ⚠️ | Sanous › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Sanous (6) ⚠️ | Saint-Lézer › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Sanous (7) ⚠️ | Sanous › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Nouilhan (8) ⚠️ | Nouilhan › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Larreule (7) ⚠️ | Larreule › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Caixon (20) ⚠️ | Caixon › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Larreule (8) ⚠️ | Larreule › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Nouilhan (10) ⚠️ | Nouilhan › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Larreule (11) ⚠️ | Larreule › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Larreule (12) ⚠️ | Larreule › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Larreule (24) ⚠️ | Larreule › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Larreule (25) ⚠️ | Larreule › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Larreule (26) ⚠️ | Larreule › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Larreule (28) ⚠️ | Larreule › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Maubourguet (5) ⚠️ | Larreule › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Larreule (37) ⚠️ | Larreule › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Larreule (38) ⚠️ | Larreule › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Artagnan (7) ⚠️ | Artagnan › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Artagnan (8) ⚠️ | Artagnan › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vic-en-Bigorre (62) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Artagnan (11) ⚠️ | Artagnan › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Artagnan (14) ⚠️ | Artagnan › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Vic-en-Bigorre (60) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Artagnan (17) ⚠️ | Artagnan › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Vic-en-Bigorre (62) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vic-en-Bigorre (64) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Artagnan (18) ⚠️ | Artagnan › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Gensac ⚠️ | Gensac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Lafitole (2) ⚠️ | Lafitole › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vic-en-Bigorre (68) ⚠️ | Vic-en-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Maubourguet (12) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Lafitole (5) ⚠️ | Lafitole › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Liac (4) ⚠️ | Liac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Ségalas ⚠️ | Ségalas › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Ségalas (11) ⚠️ | Ségalas › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Ségalas (13) ⚠️ | Ségalas › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Ségalas (15) ⚠️ | Ségalas › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Barbachen ⚠️ | Barbachen › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Barbachen (6) ⚠️ | Barbachen › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Barbachen (7) ⚠️ | Barbachen › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Ségalas (36) ⚠️ | Liac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Monfaucon ⚠️ | Monfaucon › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Monfaucon (23) ⚠️ | Monfaucon › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Monfaucon (34) ⚠️ | Monfaucon › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Monfaucon (35) ⚠️ | Monfaucon › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Monfaucon (43) ⚠️ | Monfaucon › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Monfaucon (53) ⚠️ | Monfaucon › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Buzon (3) ⚠️ | Buzon › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Monfaucon (5) ⚠️ | Monfaucon › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Sauveterre (3) ⚠️ | Sauveterre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Sauveterre (2) ⚠️ | Sauveterre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Auriébat (2) ⚠️ | Auriébat › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Auriébat (8) ⚠️ | Auriébat › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Sauveterre (11) ⚠️ | Sauveterre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Auriébat (18) ⚠️ | Auriébat › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Sauveterre (22) ⚠️ | Sauveterre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Sauveterre (23) ⚠️ | Sauveterre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Auriébat (25) ⚠️ | Auriébat › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Sauveterre (35) ⚠️ | Sauveterre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Sauveterre (38) ⚠️ | Sauveterre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Auriébat (4) ⚠️ | Auriébat › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Auriébat (7) ⚠️ | Auriébat › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Sauveterre (5) ⚠️ | Sauveterre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Auriébat (39) ⚠️ | Auriébat › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Auriébat (43) ⚠️ | Auriébat › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Auriébat (51) ⚠️ | Auriébat › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Auriébat (54) ⚠️ | Auriébat › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Auriébat (59) ⚠️ | Auriébat › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Sauveterre (49) ⚠️ | Sauveterre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Auriébat (74) ⚠️ | Auriébat › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Auriébat (75) ⚠️ | Auriébat › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Maubourguet (26) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Auriébat (77) ⚠️ | Auriébat › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Maubourguet (28) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Lafitole (26) ⚠️ | Lafitole › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Maubourguet (29) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Lafitole (9) ⚠️ | Lafitole › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Lafitole (46) ⚠️ | Lafitole › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Lafitole (48) ⚠️ | Lafitole › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Maubourguet (39) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Maubourguet (51) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Maubourguet (64) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Maubourguet (66) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Maubourguet (78) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Maubourguet (10) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Auriébat (81) ⚠️ | Auriébat › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Auriébat (82) ⚠️ | Estirac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Auriébat (86) ⚠️ | Auriébat › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Maubourguet (90) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Maubourguet (91) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Labatut-Rivière (7) ⚠️ | Labatut-Rivière › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Labatut-Rivière (8) ⚠️ | Labatut-Rivière › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Auriébat (90) ⚠️ | Auriébat › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Maubourguet (92) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Estirac (2) ⚠️ | Estirac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Maubourguet (94) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Maubourguet (95) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Maubourguet (96) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Maubourguet (97) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Maubourguet (100) ⚠️ | Auriébat › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Auriébat (13) ⚠️ | Auriébat › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Labatut-Rivière (3) ⚠️ | Labatut-Rivière › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Estirac ⚠️ | Estirac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vidouze (2) ⚠️ | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vidouze (3) ⚠️ | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Lahitte-Toupière (8) ⚠️ | Lahitte-Toupière › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vidouze (10) ⚠️ | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Lahitte-Toupière (13) ⚠️ | Lahitte-Toupière › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vidouze (11) ⚠️ | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vidouze (13) ⚠️ | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Sombrun (17) ⚠️ | Sombrun › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Sombrun (23) ⚠️ | Sombrun › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Sombrun (28) ⚠️ | Sombrun › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vidouze (24) ⚠️ | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Vidouze (4) ⚠️ | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vidouze (37) ⚠️ | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vidouze (45) ⚠️ | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vidouze (49) ⚠️ | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vidouze (58) ⚠️ | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vidouze (61) ⚠️ | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Vidouze (6) ⚠️ | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Vidouze (9) ⚠️ | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vidouze (74) ⚠️ | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vidouze (83) ⚠️ | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Sombrun (31) ⚠️ | Sombrun › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Villefranque (7) ⚠️ | Villefranque › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Caussade-Rivière (2) ⚠️ | Caussade-Rivière › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Lascazères (4) ⚠️ | Lascazères › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Hagedet (3) ⚠️ | Hagedet › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Hagedet (4) ⚠️ | Hagedet › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Lascazères (16) ⚠️ | Lascazères › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Lascazères (19) ⚠️ | Lascazères › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Hagedet (5) ⚠️ | Hagedet › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Lascazères (23) ⚠️ | Lascazères › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Lascazères (30) ⚠️ | Lascazères › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Lascazères (34) ⚠️ | Lascazères › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Caussade-Rivière (4) ⚠️ | Caussade-Rivière › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Labatut-Rivière (17) ⚠️ | Labatut-Rivière › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Caussade-Rivière (9) ⚠️ | Caussade-Rivière › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Estirac (19) ⚠️ | Estirac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Estirac (20) ⚠️ | Estirac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Caussade-Rivière (10) ⚠️ | Estirac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Caussade-Rivière (14) ⚠️ | Caussade-Rivière › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Caussade-Rivière (20) ⚠️ | Hagedet › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Labatut-Rivière (33) ⚠️ | Labatut-Rivière › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Caussade-Rivière (29) ⚠️ | Caussade-Rivière › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Soublecause (5) ⚠️ | Soublecause › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Soublecause (6) ⚠️ | Soublecause › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Hères ⚠️ | Hères › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Hères (2) ⚠️ | Hères › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Madiran (3) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Madiran (8) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Madiran (10) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Madiran (15) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Soublecause (18) ⚠️ | Soublecause › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Madiran (18) ⚠️ | Soublecause › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Madiran (11) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Larreule ⚠️ | Larreule › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Hères (7) ⚠️ | Hères › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Saint-Lanne (9) ⚠️ | Saint-Lanne › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Madiran (24) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Saint-Lanne (16) ⚠️ | Saint-Lanne › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Saint-Lanne (17) ⚠️ | Saint-Lanne › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Madiran (27) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Saint-Lanne (21) ⚠️ | Saint-Lanne › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Madiran (29) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Saint-Lanne (4) ⚠️ | Saint-Lanne › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Castelnau-Rivière-Basse (4) ⚠️ | Castelnau-Rivière-Basse › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Saint-Lanne (5) ⚠️ | Saint-Lanne › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Madiran (14) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Madiran (33) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Castelnau-Rivière-Basse (6) ⚠️ | Castelnau-Rivière-Basse › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Madiran (49) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Castelnau-Rivière-Basse (11) ⚠️ | Castelnau-Rivière-Basse › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Castelnau-Rivière-Basse (5) ⚠️ | Castelnau-Rivière-Basse › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Castelnau-Rivière-Basse (17) ⚠️ | Castelnau-Rivière-Basse › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Castelnau-Rivière-Basse (10) ⚠️ | Castelnau-Rivière-Basse › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Castelnau-Rivière-Basse (12) ⚠️ | Castelnau-Rivière-Basse › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Castelnau-Rivière-Basse (22) ⚠️ | Castelnau-Rivière-Basse › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Castelnau-Rivière-Basse (33) ⚠️ | Castelnau-Rivière-Basse › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Castelnau-Rivière-Basse (34) ⚠️ | Castelnau-Rivière-Basse › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Hères (4) ⚠️ | Hères › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Hères (6) ⚠️ | Hères › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Saint-Lary-Soulan (193) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (194) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Bagnères-de-Bigorre (204) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Ancizan (33) ⚠️ | Ancizan › Aure Louron | 1 |
| Forêt de Ancizan (34) ⚠️ | Ancizan › Aure Louron | 1 |
| Bois de Ancizan (15) ⚠️ | Ancizan › Aure Louron | 1 |
| Bois de Castelnau-Rivière-Basse (37) ⚠️ | Castelnau-Rivière-Basse › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Arrens-Marsous (219) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Bois de Ourdis-Cotdoussan (19) ⚠️ | Ourdis-Cotdoussan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Germs-sur-l'Oussouet (9) ⚠️ | Germs-sur-l'Oussouet › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Gavarnie-Gèdre (16) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Bois de Bagnères-de-Bigorre (37) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Bois de Beaudéan (15) ⚠️ | Beaudéan › Haute-Bigorre | 1 |
| Bois de Beaudéan (17) ⚠️ | Campan › Haute-Bigorre | 1 |
| Bois de Campan (14) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Beaudéan (32) ⚠️ | Beaudéan › Haute-Bigorre | 1 |
| Forêt de Campan (295) ⚠️ | Campan › Haute-Bigorre | 1 |
| Forêt de Beaudéan (33) ⚠️ | Beaudéan › Haute-Bigorre | 1 |
| Forêt de Bagnères-de-Bigorre (215) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Bois de Beaudéan (21) ⚠️ | Beaudéan › Haute-Bigorre | 1 |
| Forêt de Ferrières (35) ⚠️ | Ferrières › Pays de Nay (Hautes-Pyrénées) | 1 |
| Forêt de Bagnères-de-Bigorre (219) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Bois de Tarbes (9) ⚠️ | Tarbes › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Tarbes (12) ⚠️ | Tarbes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lagarde (8) ⚠️ | Lagarde › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Gayan (9) ⚠️ | Gayan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Viger ⚠️ | Viger › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Bagnères-de-Bigorre (49) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Bois de Bagnères-de-Bigorre (59) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Bois de Azereix (9) ⚠️ | Azereix › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Orleix (30) ⚠️ | Orleix › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Siarrouy (7) ⚠️ | Siarrouy › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Soulom (16) ⚠️ | Villelongue › Pyrénées Vallées des Gaves | 1 |
| Bois de Lau-Balagnas (31) ⚠️ | Lau-Balagnas › Pyrénées Vallées des Gaves | 1 |
| Bois de Geu (9) ⚠️ | Agos-Vidalos › Pyrénées Vallées des Gaves | 1 |
| Bois de Saint-Pé-de-Bigorre (27) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lourdes (133) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Sers (78) ⚠️ | Sers › Pyrénées Vallées des Gaves | 1 |
| Forêt de Sers (79) ⚠️ | Sers › Pyrénées Vallées des Gaves | 1 |
| Forêt de Barèges (202) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Bois de Villelongue (13) ⚠️ | Villelongue › Pyrénées Vallées des Gaves | 1 |
| Parc de Rabastens-de-Bigorre ⚠️ | Rabastens-de-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Cauterets (19) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Forêt de Cauterets (660) ⚠️ | Cauterets › Pyrénées Vallées des Gaves | 1 |
| Bois de Ossen (27) ⚠️ | Ossen › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Argelès-Gazost (23) ⚠️ | Argelès-Gazost › Pyrénées Vallées des Gaves | 1 |
| Bois de Lau-Balagnas (36) ⚠️ | Lau-Balagnas › Pyrénées Vallées des Gaves | 1 |
| Forêt de Argelès-Gazost (3) ⚠️ | Argelès-Gazost › Pyrénées Vallées des Gaves | 1 |
| Forêt de Aucun (64) ⚠️ | Aucun › Pyrénées Vallées des Gaves | 1 |
| Bois de Aucun (7) ⚠️ | Aucun › Pyrénées Vallées des Gaves | 1 |
| Bois de Arrens-Marsous (50) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arrens-Marsous (226) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Bois de Arrens-Marsous (74) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Bois de Arrens-Marsous (77) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Bois de Estaing (30) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 1 |
| Bois de Estaing (48) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 1 |
| Bois de Estaing (56) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 1 |
| Bois de Arras-en-Lavedan (24) ⚠️ | Arras-en-Lavedan › Pyrénées Vallées des Gaves | 1 |
| Bois de Arcizans-Avant (12) ⚠️ | Arcizans-Avant › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gez (4) ⚠️ | Gez › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arrens-Marsous (231) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Bois de Arrens-Marsous (108) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Bois de Arrens-Marsous (116) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Bois de Arrens-Marsous (121) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Bois de Arrens-Marsous (122) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Bois de Soulom (20) ⚠️ | Soulom › Pyrénées Vallées des Gaves | 1 |
| Bois de Salles (13) ⚠️ | Salles › Pyrénées Vallées des Gaves | 1 |
| Forêt de Salles (21) ⚠️ | Salles › Pyrénées Vallées des Gaves | 1 |
| Bois de Bagnères-de-Bigorre (76) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Bois de Artalens-Souin (17) ⚠️ | Artalens-Souin › Pyrénées Vallées des Gaves | 1 |
| Forêt de Ayros-Arbouix (30) ⚠️ | Ayros-Arbouix › Pyrénées Vallées des Gaves | 1 |
| Bois de Lugagnan (9) ⚠️ | Lugagnan › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Lugagnan (18) ⚠️ | Lugagnan › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Lugagnan (19) ⚠️ | Lugagnan › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Jarret (25) ⚠️ | Jarret › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Agos-Vidalos (57) ⚠️ | Viger › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Agos-Vidalos (58) ⚠️ | Agos-Vidalos › Pyrénées Vallées des Gaves | 1 |
| Bois de Viger (19) ⚠️ | Viger › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Luz-Saint-Sauveur (38) ⚠️ | Luz-Saint-Sauveur › Pyrénées Vallées des Gaves | 1 |
| Forêt de Luz-Saint-Sauveur (35) ⚠️ | Luz-Saint-Sauveur › Pyrénées Vallées des Gaves | 1 |
| Bois de Lau-Balagnas (44) ⚠️ | Lau-Balagnas › Pyrénées Vallées des Gaves | 1 |
| Bois de Luz-Saint-Sauveur (46) ⚠️ | Luz-Saint-Sauveur › Pyrénées Vallées des Gaves | 1 |
| Forêt de Aspin-en-Lavedan (6) ⚠️ | Aspin-en-Lavedan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Ossen ⚠️ | Ossen › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Lourdes (71) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lourdes (135) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Viger (27) ⚠️ | Viger › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Viger (29) ⚠️ | Viger › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Viger (30) ⚠️ | Viger › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Lourdes (85) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bartrès (47) ⚠️ | Bartrès › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lourdes (137) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Saint-Pé-de-Bigorre (33) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Saint-Pé-de-Bigorre (35) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Ibos (13) ⚠️ | Ibos › Tarbes-Lourdes-Pyrénées | 1 |
| Parc de Lourdes (7) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Bazet (3) ⚠️ | Bazet › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Lourdes (109) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Peyrouse (37) ⚠️ | Peyrouse › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Saint-Pé-de-Bigorre (36) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Loubajac (5) ⚠️ | Loubajac › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Poueyferré (20) ⚠️ | Poueyferré › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Bartrès (11) ⚠️ | Bartrès › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Loubajac (14) ⚠️ | Loubajac › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Barlest (9) ⚠️ | Barlest › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bartrès (54) ⚠️ | Bartrès › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Juncalas (28) ⚠️ | Juncalas › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Saint-Créac (37) ⚠️ | Saint-Créac › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Saint-Créac (39) ⚠️ | Saint-Créac › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Juncalas (8) ⚠️ | Ousté › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Germs-sur-l'Oussouet (47) ⚠️ | Germs-sur-l'Oussouet › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Arrodets-ez-Angles (10) ⚠️ | Arrodets-ez-Angles › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bagnères-de-Bigorre (222) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Bois de Bagnères-de-Bigorre (85) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Bois de Juncalas (35) ⚠️ | Juncalas › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Juncalas (36) ⚠️ | Juncalas › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Gazost (45) ⚠️ | Gazost › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Gazost (37) ⚠️ | Gazost › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Ourdis-Cotdoussan (21) ⚠️ | Ourdis-Cotdoussan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Tostat (13) ⚠️ | Tostat › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Saint-Pé-de-Bigorre (45) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 1 |
| Parc de Caixon (2) ⚠️ | Caixon › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Aucun (67) ⚠️ | Aucun › Pyrénées Vallées des Gaves | 1 |
| Bois de Beaucens (96) ⚠️ | Beaucens › Pyrénées Vallées des Gaves | 1 |
| Bois de Sers (15) ⚠️ | Sers › Pyrénées Vallées des Gaves | 1 |
| Bois de Sers (30) ⚠️ | Sers › Pyrénées Vallées des Gaves | 1 |
| Bois de Chèze (14) ⚠️ | Chèze › Pyrénées Vallées des Gaves | 1 |
| Bois de Saint-Lary-Soulan (27) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Bois de Saint-Lary-Soulan (31) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Bois de Saint-Lary-Soulan (36) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (196) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (199) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (201) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Bois de Saint-Lary-Soulan (42) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Bois de Tramezaïgues (5) ⚠️ | Tramezaïgues › Aure Louron | 1 |
| Bois de Aucun (14) ⚠️ | Salles › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gez (8) ⚠️ | Gez › Pyrénées Vallées des Gaves | 1 |
| Bois de Barèges (14) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Bois de Asque (4) ⚠️ | Asque › Plateau de Lannemezan | 1 |
| Forêt de Barèges (204) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Bois de Barèges (17) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Bois de Barèges (19) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Bois de Bun (15) ⚠️ | Bun › Pyrénées Vallées des Gaves | 1 |
| Forêt de Estaing (124) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 1 |
| Bois de Barèges (23) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Bois de Barèges (36) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Bois de Barèges (45) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Bois de Barèges (55) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Bois de Barèges (76) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Forêt de Villelongue (42) ⚠️ | Villelongue › Pyrénées Vallées des Gaves | 1 |
| Bois de Villelongue (19) ⚠️ | Villelongue › Pyrénées Vallées des Gaves | 1 |
| Bois de Betpouey (20) ⚠️ | Betpouey › Pyrénées Vallées des Gaves | 1 |
| Bois de Betpouey (21) ⚠️ | Betpouey › Pyrénées Vallées des Gaves | 1 |
| Bois de Betpouey (25) ⚠️ | Betpouey › Pyrénées Vallées des Gaves | 1 |
| Bois de Barèges (92) ⚠️ | Barèges › Pyrénées Vallées des Gaves | 1 |
| Bois de Sazos (17) ⚠️ | Sazos › Pyrénées Vallées des Gaves | 1 |
| Bois de Sazos (27) ⚠️ | Sazos › Pyrénées Vallées des Gaves | 1 |
| Bois de Aulon (23) ⚠️ | Aulon › Aure Louron | 1 |
| Bois de Bagnères-de-Bigorre (90) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Bois de Estaing (74) ⚠️ | Estaing › Pyrénées Vallées des Gaves | 1 |
| Forêt de Bénac (25) ⚠️ | Bénac › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Layrisse (3) ⚠️ | Layrisse › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Escoubès-Pouts (12) ⚠️ | Escoubès-Pouts › Tarbes-Lourdes-Pyrénées | 1 |
| Parc de Astugue ⚠️ | Astugue › Haute-Bigorre | 1 |
| Forêt de Astugue (61) ⚠️ | Astugue › Haute-Bigorre | 1 |
| Forêt de Astugue (62) ⚠️ | Astugue › Haute-Bigorre | 1 |
| Bois de Sère-Lanso (4) ⚠️ | Sère-Lanso › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Arcizac-ez-Angles (8) ⚠️ | Arcizac-ez-Angles › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Bourréac (2) ⚠️ | Bourréac › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Escoubès-Pouts (16) ⚠️ | Escoubès-Pouts › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Paréac (8) ⚠️ | Paréac › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Paréac (7) ⚠️ | Paréac › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Ossun-ez-Angles (2) ⚠️ | Ossun-ez-Angles › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Neuilh (17) ⚠️ | Neuilh › Haute-Bigorre | 1 |
| Forêt de Ossun-ez-Angles (11) ⚠️ | Ossun-ez-Angles › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Astugue (63) ⚠️ | Neuilh › Haute-Bigorre | 1 |
| Forêt de Lourdes (142) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Arcizac-Adour (27) ⚠️ | Arcizac-Adour › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Salles-Adour (10) ⚠️ | Horgues › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Horgues (9) ⚠️ | Horgues › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Horgues (12) ⚠️ | Horgues › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Barbazan-Debat (4) ⚠️ | Barbazan-Debat › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Barbazan-Debat (5) ⚠️ | Barbazan-Debat › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Arcizac-Adour (28) ⚠️ | Arcizac-Adour › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Hiis (21) ⚠️ | Hiis › Haute-Bigorre | 1 |
| Forêt de Vielle-Adour (27) ⚠️ | Vielle-Adour › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Gavarnie-Gèdre (62) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Gavarnie-Gèdre (313) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Bois de Luz-Saint-Sauveur (51) ⚠️ | Luz-Saint-Sauveur › Pyrénées Vallées des Gaves | 1 |
| Bois de Luz-Saint-Sauveur (53) ⚠️ | Luz-Saint-Sauveur › Pyrénées Vallées des Gaves | 1 |
| Bois de Fontrailles (50) ⚠️ | Fontrailles › Pays de Trie et du Magnoac | 1 |
| Bois de Galan (111) ⚠️ | Galan › Plateau de Lannemezan | 1 |
| Bois de Vieuzos (24) ⚠️ | Vieuzos › Pays de Trie et du Magnoac | 1 |
| Bois de Betpouy (22) ⚠️ | Betpouy › Pays de Trie et du Magnoac | 1 |
| Bois de Betpouy (25) ⚠️ | Betpouy › Pays de Trie et du Magnoac | 1 |
| Bois de Puntous (35) ⚠️ | Hachan › Pays de Trie et du Magnoac | 1 |
| Bois de Puntous (40) ⚠️ | Puntous › Pays de Trie et du Magnoac | 1 |
| Bois de Caussade-Rivière (31) ⚠️ | Caussade-Rivière › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Labatut-Rivière (49) ⚠️ | Labatut-Rivière › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Maubourguet (16) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Salles (24) ⚠️ | Salles › Pyrénées Vallées des Gaves | 1 |
| Forêt de Aspin-en-Lavedan (8) ⚠️ | Aspin-en-Lavedan › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Gardères (75) ⚠️ | Gardères › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Campan (297) ⚠️ | Campan › Haute-Bigorre | 1 |
| Bois de Bonnefont (119) ⚠️ | Bonnefont › Pays de Trie et du Magnoac | 1 |
| Parc de Laloubère (2) ⚠️ | Laloubère › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Gavarnie-Gèdre (315) ⚠️ | Gavarnie-Gèdre › Pyrénées Vallées des Gaves | 1 |
| Forêt de Lanespède (21) ⚠️ | Lanespède › Coteaux du Val-d'Arros | 1 |
| Forêt de Saint-Lanne (11) ⚠️ | Saint-Lanne › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Saint-Lanne (12) ⚠️ | Saint-Lanne › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Castelnau-Rivière-Basse (42) ⚠️ | Castelnau-Rivière-Basse › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Castelnau-Rivière-Basse (44) ⚠️ | Castelnau-Rivière-Basse › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Castelnau-Rivière-Basse (46) ⚠️ | Castelnau-Rivière-Basse › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Madiran (18) ⚠️ | Madiran › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Parc de Lourdes (14) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Villenave-près-Béarn (3) ⚠️ | Villenave-près-Béarn › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Bun (36) ⚠️ | Bun › Pyrénées Vallées des Gaves | 1 |
| Forêt de Saint-Savin (21) ⚠️ | Saint-Savin › Pyrénées Vallées des Gaves | 1 |
| Forêt de Viger (3) ⚠️ | Viger › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Berbérust-Lias (22) ⚠️ | Berbérust-Lias › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Agos-Vidalos (63) ⚠️ | Agos-Vidalos › Pyrénées Vallées des Gaves | 1 |
| Bois de Ségus (57) ⚠️ | Ségus › Tarbes-Lourdes-Pyrénées | 1 |
| Bois des Angles (19) ⚠️ | Les Angles › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Gazost (42) ⚠️ | Gazost › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bagnères-de-Bigorre (228) ⚠️ | Bagnères-de-Bigorre › Haute-Bigorre | 1 |
| Forêt de Arrens-Marsous (244) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arrens-Marsous (245) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arras-en-Lavedan (85) ⚠️ | Arcizans-Dessus › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arcizans-Avant (38) ⚠️ | Arcizans-Avant › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arras-en-Lavedan (87) ⚠️ | Arras-en-Lavedan › Pyrénées Vallées des Gaves | 1 |
| Bois de Lau-Balagnas (49) ⚠️ | Lau-Balagnas › Pyrénées Vallées des Gaves | 1 |
| Forêt de Artalens-Souin (46) ⚠️ | Artalens-Souin › Pyrénées Vallées des Gaves | 1 |
| Forêt de Lourdes (146) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Aurensan (5) ⚠️ | Aurensan › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Bordères-sur-l'Échez (25) ⚠️ | Bordères-sur-l'Échez › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Montgaillard (58) ⚠️ | Montgaillard › Haute-Bigorre | 1 |
| Forêt de Peyrouse (44) ⚠️ | Peyrouse › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Poueyferré (62) ⚠️ | Poueyferré › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Bartrès (57) ⚠️ | Bartrès › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lourdes (148) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Lézignan (4) ⚠️ | Lézignan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Barlest (20) ⚠️ | Barlest › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Azereix (26) ⚠️ | Azereix › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Louey ⚠️ | Louey › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Aurensan (6) ⚠️ | Aurensan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Saint-Lézer (28) ⚠️ | Saint-Lézer › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Barbazan-Debat (6) ⚠️ | Soues › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Barbazan-Debat (7) ⚠️ | Salles-Adour › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Saint-Martin (25) ⚠️ | Saint-Martin › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Hitte (13) ⚠️ | Hitte › Haute-Bigorre | 1 |
| Forêt de Hitte (14) ⚠️ | Hitte › Haute-Bigorre | 1 |
| Forêt de Asque (46) ⚠️ | Asque › Plateau de Lannemezan | 1 |
| Forêt de Bulan (35) ⚠️ | Bulan › Plateau de Lannemezan | 1 |
| Forêt de Labastide (48) ⚠️ | Labastide › Plateau de Lannemezan | 1 |
| Forêt de Tournay (91) ⚠️ | Tournay › Coteaux du Val-d'Arros | 1 |
| Bois de Marseillan (16) ⚠️ | Marseillan › Coteaux du Val-d'Arros | 1 |
| Forêt de Sénac (27) ⚠️ | Sénac › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Lacassagne (12) ⚠️ | Lacassagne › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Rabastens-de-Bigorre (36) ⚠️ | Rabastens-de-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Sarriac-Bigorre (21) ⚠️ | Rabastens-de-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Lansac (10) ⚠️ | Lansac › Coteaux du Val-d'Arros | 1 |
| Bois de Mazerolles (38) ⚠️ | Mazerolles › Pays de Trie et du Magnoac | 1 |
| Forêt de Fontrailles (17) ⚠️ | Fontrailles › Pays de Trie et du Magnoac | 1 |
| Forêt de Orieux (10) ⚠️ | Orieux › Coteaux du Val-d'Arros | 1 |
| Forêt de Montastruc (19) ⚠️ | Montastruc › Plateau de Lannemezan | 1 |
| Bois de Burg (102) ⚠️ | Burg › Coteaux du Val-d'Arros | 1 |
| Bois de Bégole (70) ⚠️ | Bégole › Coteaux du Val-d'Arros | 1 |
| Bois de Bégole (71) ⚠️ | Bégole › Coteaux du Val-d'Arros | 1 |
| Bois de Bégole (72) ⚠️ | Bégole › Coteaux du Val-d'Arros | 1 |
| Bois de Cantaous (81) ⚠️ | Cantaous › Neste Barousse | 1 |
| Forêt de Sadournin (10) ⚠️ | Sadournin › Pays de Trie et du Magnoac | 1 |
| Bois de Recurt (30) ⚠️ | Recurt › Plateau de Lannemezan | 1 |
| Bois de Castelnau-Magnoac (122) ⚠️ | Castelnau-Magnoac › Pays de Trie et du Magnoac | 1 |
| Forêt de Monlong (5) ⚠️ | Monlong › Pays de Trie et du Magnoac | 1 |
| Bois de Monléon-Magnoac (113) ⚠️ | Monléon-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Arné (71) ⚠️ | Arné › Plateau de Lannemezan | 1 |
| Forêt de Lalanne (6) ⚠️ | Lalanne › Pays de Trie et du Magnoac | 1 |
| Bois de Thermes-Magnoac (94) ⚠️ | Thermes-Magnoac › Pays de Trie et du Magnoac | 1 |
| Bois de Saint-Paul (60) ⚠️ | Saint-Paul › Neste Barousse | 1 |
| Forêt de Tibiran-Jaunac (18) ⚠️ | Tibiran-Jaunac › Neste Barousse | 1 |
| Bois de Anla (25) ⚠️ | Ilheu › Neste Barousse | 1 |
| Bois de Antichan (28) ⚠️ | Antichan › Neste Barousse | 1 |
| Bois de Antichan (29) ⚠️ | Antichan › Neste Barousse | 1 |
| Bois de Gembrie (14) ⚠️ | Gembrie › Neste Barousse | 1 |
| Bois de Saléchan (33) ⚠️ | Saléchan › Neste Barousse | 1 |
| Bois de Bertren (26) ⚠️ | Bertren › Neste Barousse | 1 |
| Bois de Esbareich (40) ⚠️ | Esbareich › Neste Barousse | 1 |
| Bois de Seich (51) ⚠️ | Seich › Neste Barousse | 1 |
| Forêt de Cazaux-Fréchet-Anéran-Camors (23) ⚠️ | Cazaux-Fréchet-Anéran-Camors › Aure Louron | 1 |
| Bois de Cazaux-Fréchet-Anéran-Camors (24) ⚠️ | Cazaux-Fréchet-Anéran-Camors › Aure Louron | 1 |
| Forêt de Loudervielle (43) ⚠️ | Loudervielle › Aure Louron | 1 |
| Forêt de Loudervielle (46) ⚠️ | Loudervielle › Aure Louron | 1 |
| Bois de Adervielle-Pouchergues (27) ⚠️ | Adervielle-Pouchergues › Aure Louron | 1 |
| Bois de Génos (59) ⚠️ | Génos › Aure Louron | 1 |
| Forêt de Loudenvielle (79) ⚠️ | Loudenvielle › Aure Louron | 1 |
| Bois de Cadéac (22) ⚠️ | Cadéac › Aure Louron | 1 |
| Bois de Ancizan (19) ⚠️ | Ancizan › Aure Louron | 1 |
| Forêt de Guchan (4) ⚠️ | Guchan › Aure Louron | 1 |
| Bois de Vielle-Aure (24) ⚠️ | Vielle-Aure › Aure Louron | 1 |
| Forêt de Azet (58) ⚠️ | Azet › Aure Louron | 1 |
| Forêt de Saint-Lary-Soulan (213) ⚠️ | Saint-Lary-Soulan › Aure Louron | 1 |
| Forêt de Aragnouet (203) ⚠️ | Aragnouet › Aure Louron | 1 |
| Bois de Séron (41) ⚠️ | Séron › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Maubourguet (119) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Ségalas (2) ⚠️ | Ségalas › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Auriébat (111) ⚠️ | Auriébat › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Lafitole (57) ⚠️ | Lafitole › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Maubourguet (120) ⚠️ | Maubourguet › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Lafitole (12) ⚠️ | Lafitole › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vidouze (91) ⚠️ | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Vidouze (92) ⚠️ | Vidouze › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Hères (29) ⚠️ | Hères › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Larreule (5) ⚠️ | Larreule › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Bois de Soublecause (35) ⚠️ | Soublecause › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Aureilhan (32) ⚠️ | Aureilhan › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Soues (17) ⚠️ | Soues › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Artalens-Souin (47) ⚠️ | Artalens-Souin › Pyrénées Vallées des Gaves | 1 |
| Bois de Sarriac-Bigorre (22) ⚠️ | Sarriac-Bigorre › Adour-Madiran (Hautes-Pyrénées) | 1 |
| Forêt de Arrens-Marsous (258) ⚠️ | Arrens-Marsous › Pyrénées Vallées des Gaves | 1 |
| Forêt de Arras-en-Lavedan (91) ⚠️ | Arras-en-Lavedan › Pyrénées Vallées des Gaves | 1 |
| Bois de Arras-en-Lavedan (42) ⚠️ | Arras-en-Lavedan › Pyrénées Vallées des Gaves | 1 |
| Forêt de Ayros-Arbouix (32) ⚠️ | Ayros-Arbouix › Pyrénées Vallées des Gaves | 1 |
| Bois de Ayros-Arbouix (34) ⚠️ | Ayros-Arbouix › Pyrénées Vallées des Gaves | 1 |
| Bois de Viger (33) ⚠️ | Viger › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Ségus (58) ⚠️ | Ségus › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Lourdes (125) ⚠️ | Lourdes › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Peyrouse (48) ⚠️ | Peyrouse › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Saint-Pé-de-Bigorre (54) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Germs-sur-l'Oussouet (14) ⚠️ | Germs-sur-l'Oussouet › Tarbes-Lourdes-Pyrénées | 1 |
| Forêt de Artalens-Souin (48) ⚠️ | Artalens-Souin › Pyrénées Vallées des Gaves | 1 |
| Bois de Arbéost (9) ⚠️ | Arbéost › Pays de Nay (Hautes-Pyrénées) | 1 |
| Bois de Clarens (82) ⚠️ | Recurt › Plateau de Lannemezan | 1 |
| Bois de Beyrède-Jumet-Camous (20) ⚠️ | Beyrède-Jumet-Camous › Aure Louron | 1 |
| Forêt de Lansac (13) ⚠️ | Lansac › Coteaux du Val-d'Arros | 1 |
| Forêt de Arrayou-Lahitte (42) ⚠️ | Arrayou-Lahitte › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Saint-Pé-de-Bigorre (55) ⚠️ | Saint-Pé-de-Bigorre › Tarbes-Lourdes-Pyrénées | 1 |
| Bois de Salles-Adour (17) ⚠️ | Salles-Adour › Tarbes-Lourdes-Pyrénées | 1 |
| Parc de Tarbes (12) ⚠️ | Tarbes › Tarbes-Lourdes-Pyrénées | 1 |

18 525 parc(s) plus petits qu'une cellule ne sont pas listés : la carte les dessine, mais ils n'offrent aucune cellule.

⚠️ 22954 parc(s) hors de la fenêtre 10–125 cellules (22850 trop petit(s), 104 trop grand(s)) : affichés sur la carte, mais ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| military | 318 |
| airport | 197 |
| prison | 3 |
| **Total déclaré** | **518** |
| dont dans une zone de ce territoire | 518 |


### Zones concernées

| Zone | Cellules exclues |
|---|---:|
| Ossun | 227 |
| Azereix | 137 |
| Louey | 58 |
| Tarbes | 24 |
| Laloubère | 22 |
| Lanne | 16 |
| Juillan | 13 |
| Castelnau-Magnoac | 9 |
| Loudervielle | 4 |
| Sadournin | 4 |
| Lannemezan | 3 |
| Aureilhan | 1 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
