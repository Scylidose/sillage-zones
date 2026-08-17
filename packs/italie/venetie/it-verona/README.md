# Province de Vérone

Pack `it-verona` · version 1.0.1 · grille 200 m · Italie › Vénétie

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 147 601 |
| dont restreintes (aéroport, militaire, prison) | 398 |
| dont sans chemin (aucune voie à moins de 60 m) | 31 399 |
| Cellules retirées par le masque d'eau | 9 555 |
| Villes | 98 |
| Arrondissements et quartiers | 0 |
| Îles | 0 |
| Parcs | 6 866 |

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
| **Sans chemin** | parmi les comptées, celles qu'aucune voie n'approche à moins de 60 m — l'utilisateur peut les marquer inaccessibles zone par zone, elles restent comptées tant qu'il ne le fait pas |

## Villes (98)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Sans chemin | Parcs |
|---|---:|---:|---:|---:|---:|---:|---:|
| Verona | 10 098 | 171 | 9 927 | 77 | **9 850** | 857 (9 %) | 757 |
| Legnago | 3 984 | 62 | 3 922 | 7 | **3 915** | 1 171 (30 %) | 44 |
| Cerea | 3 547 | 15 | 3 532 | 21 | **3 511** | 1 363 (39 %) | 34 |
| Isola della Scala | 3 538 | 10 | 3 528 | 0 | **3 528** | 1 629 (46 %) | 28 |
| Bosco Chiesanuova | 3 301 | 1 | 3 300 | 0 | **3 300** | 483 (15 %) | 386 |
| Valeggio sul Mincio | 3 237 | 13 | 3 224 | 54 | **3 170** | 462 (15 %) | 82 |
| Villafranca di Verona | 2 897 | 4 | 2 893 | 62 | **2 831** | 283 (10 %) | 64 |
| Gazzo Veronese | 2 843 | 1 | 2 842 | 0 | **2 842** | 1 127 (40 %) | 10 |
| Zevio | 2 789 | 59 | 2 730 | 0 | **2 730** | 789 (29 %) | 21 |
| Villa Bartolomea | 2 696 | 51 | 2 645 | 0 | **2 645** | 906 (34 %) | 25 |
| Grezzana | 2 529 | 1 | 2 528 | 0 | **2 528** | 113 (4 %) | 185 |
| Malcesine | 3 593 | 1 071 | 2 522 | 0 | **2 522** | 368 (15 %) | 178 |
| Caprino Veronese | 2 419 | 0 | 2 419 | 0 | **2 419** | 120 (5 %) | 373 |
| Oppeano | 2 360 | 10 | 2 350 | 0 | **2 350** | 817 (35 %) | 10 |
| Sant'Anna d'Alfaedo | 2 237 | 0 | 2 237 | 0 | **2 237** | 165 (7 %) | 280 |
| Cologna Veneta | 2 187 | 1 | 2 186 | 0 | **2 186** | 834 (38 %) | 9 |
| Selva di Progno | 2 109 | 3 | 2 106 | 0 | **2 106** | 58 (3 %) | 228 |
| Sona | 2 106 | 0 | 2 106 | 0 | **2 106** | 343 (16 %) | 30 |
| Bovolone | 2 087 | 4 | 2 083 | 12 | **2 071** | 721 (35 %) | 27 |
| Negrar di Valpolicella | 2 062 | 0 | 2 062 | 0 | **2 062** | 92 (4 %) | 122 |
| Sommacampagna | 2 060 | 3 | 2 057 | 145 | **1 912** | 319 (17 %) | 44 |
| Ronco all'Adige | 2 160 | 161 | 1 999 | 0 | **1 999** | 798 (40 %) | 28 |
| Nogara | 1 958 | 0 | 1 958 | 0 | **1 958** | 826 (42 %) | 13 |
| Casaleone | 1 917 | 0 | 1 917 | 0 | **1 917** | 870 (45 %) | 22 |
| Tregnago | 1 907 | 20 | 1 887 | 0 | **1 887** | 95 (5 %) | 208 |
| Roverè Veronese | 1 869 | 2 | 1 867 | 0 | **1 867** | 130 (7 %) | 198 |
| Fumane | 1 750 | 0 | 1 750 | 0 | **1 750** | 44 (3 %) | 220 |
| Castagnaro | 1 743 | 4 | 1 739 | 0 | **1 739** | 644 (37 %) | 3 |
| San Martino Buon Albergo | 1 752 | 16 | 1 736 | 0 | **1 736** | 297 (17 %) | 65 |
| San Bonifacio | 1 715 | 10 | 1 705 | 0 | **1 705** | 407 (24 %) | 13 |
| Erbezzo | 1 633 | 1 | 1 632 | 0 | **1 632** | 154 (9 %) | 210 |
| Sorgà | 1 594 | 0 | 1 594 | 0 | **1 594** | 799 (50 %) | 13 |
| Vigasio | 1 572 | 1 | 1 571 | 0 | **1 571** | 572 (36 %) | 14 |
| Brenzone sul Garda | 2 672 | 1 104 | 1 568 | 0 | **1 568** | 141 (9 %) | 86 |
| Salizzole | 1 541 | 1 | 1 540 | 0 | **1 540** | 710 (46 %) | 1 |
| Dolcè | 1 580 | 46 | 1 534 | 0 | **1 534** | 44 (3 %) | 82 |
| Minerbe | 1 500 | 1 | 1 499 | 0 | **1 499** | 661 (44 %) | 6 |
| Castelnuovo del Garda | 1 759 | 263 | 1 496 | 0 | **1 496** | 161 (11 %) | 38 |
| Nogarole Rocca | 1 471 | 16 | 1 455 | 0 | **1 455** | 611 (42 %) | 6 |
| San Zeno di Montagna | 1 444 | 0 | 1 444 | 0 | **1 444** | 90 (6 %) | 231 |
| Lazise | 3 211 | 1 818 | 1 393 | 0 | **1 393** | 73 (5 %) | 163 |
| Albaredo d'Adige | 1 417 | 31 | 1 386 | 0 | **1 386** | 447 (32 %) | 51 |
| Ferrara di Monte Baldo | 1 378 | 0 | 1 378 | 0 | **1 378** | 259 (19 %) | 159 |
| Badia Calavena | 1 373 | 7 | 1 366 | 0 | **1 366** | 36 (3 %) | 236 |
| Trevenzuolo | 1 364 | 0 | 1 364 | 0 | **1 364** | 744 (55 %) | 4 |
| Belfiore | 1 338 | 26 | 1 312 | 0 | **1 312** | 404 (31 %) | 15 |
| San Giovanni Ilarione | 1 301 | 0 | 1 301 | 0 | **1 301** | 88 (7 %) | 187 |
| Brentino Belluno | 1 329 | 31 | 1 298 | 0 | **1 298** | 19 (1 %) | 90 |
| Illasi | 1 262 | 0 | 1 262 | 0 | **1 262** | 215 (17 %) | 31 |
| Mozzecane | 1 243 | 2 | 1 241 | 0 | **1 241** | 370 (30 %) | 26 |
| Vestenanova | 1 223 | 0 | 1 223 | 0 | **1 223** | 70 (6 %) | 225 |
| Bussolengo | 1 235 | 22 | 1 213 | 0 | **1 213** | 70 (6 %) | 49 |
| Sant'Ambrogio di Valpolicella | 1 196 | 3 | 1 193 | 0 | **1 193** | 57 (5 %) | 47 |
| Soave | 1 159 | 0 | 1 159 | 0 | **1 159** | 133 (11 %) | 37 |
| Montecchia di Crosara | 1 073 | 6 | 1 067 | 0 | **1 067** | 168 (16 %) | 99 |
| Colognola ai Colli | 1 063 | 0 | 1 063 | 0 | **1 063** | 151 (14 %) | 5 |
| Veronella | 1 051 | 0 | 1 051 | 0 | **1 051** | 426 (41 %) | 1 |
| Monteforte d'Alpone | 1 038 | 0 | 1 038 | 0 | **1 038** | 76 (7 %) | 22 |
| San Pietro in Cariano | 1 030 | 1 | 1 029 | 0 | **1 029** | 114 (11 %) | 15 |
| Zimella | 1 023 | 0 | 1 023 | 0 | **1 023** | 441 (43 %) | 1 |
| Terrazzo | 1 029 | 26 | 1 003 | 0 | **1 003** | 360 (36 %) | 4 |
| Mezzane di Sotto | 999 | 0 | 999 | 0 | **999** | 62 (6 %) | 85 |
| Pescantina | 1 000 | 18 | 982 | 0 | **982** | 83 (8 %) | 12 |
| Roverchiara | 993 | 19 | 974 | 0 | **974** | 362 (37 %) | 8 |
| Velo Veronese | 972 | 0 | 972 | 0 | **972** | 101 (10 %) | 93 |
| Arcole | 959 | 0 | 959 | 0 | **959** | 323 (34 %) | 1 |
| Marano di Valpolicella | 949 | 0 | 949 | 0 | **949** | 21 (2 %) | 40 |
| Povegliano Veronese | 946 | 0 | 946 | 6 | **940** | 302 (32 %) | 19 |
| San Giovanni Lupatoto | 962 | 18 | 944 | 0 | **944** | 212 (22 %) | 31 |
| Roncà | 924 | 0 | 924 | 0 | **924** | 67 (7 %) | 139 |
| Rivoli Veronese | 944 | 28 | 916 | 0 | **916** | 54 (6 %) | 39 |
| Pressana | 891 | 0 | 891 | 0 | **891** | 355 (40 %) | 5 |
| Bonavigo | 900 | 24 | 876 | 0 | **876** | 353 (40 %) | 6 |
| Costermano sul Garda | 865 | 0 | 865 | 0 | **865** | 15 (2 %) | 64 |
| Isola Rizza | 861 | 1 | 860 | 0 | **860** | 302 (35 %) | 8 |
| Buttapietra | 871 | 24 | 847 | 0 | **847** | 291 (34 %) | 11 |
| Bardolino | 2 919 | 2 080 | 839 | 0 | **839** | 23 (3 %) | 33 |
| San Pietro di Morubio | 806 | 0 | 806 | 0 | **806** | 312 (39 %) | 9 |
| Erbè | 793 | 9 | 784 | 0 | **784** | 378 (48 %) | 5 |
| Peschiera del Garda | 921 | 170 | 751 | 7 | **744** | 49 (7 %) | 48 |
| Lavagno | 748 | 2 | 746 | 0 | **746** | 108 (14 %) | 15 |
| Sanguinetto | 691 | 0 | 691 | 0 | **691** | 317 (46 %) | 3 |
| Palù | 682 | 0 | 682 | 0 | **682** | 211 (31 %) | 1 |
| Torri del Benaco | 2 312 | 1 635 | 677 | 0 | **677** | 1 (0 %) | 37 |
| Angiari | 681 | 19 | 662 | 0 | **662** | 137 (21 %) | 5 |
| Cavaion Veronese | 653 | 6 | 647 | 0 | **647** | 54 (8 %) | 16 |
| Cazzano di Tramigna | 627 | 0 | 627 | 0 | **627** | 79 (13 %) | 27 |
| Bevilacqua | 613 | 0 | 613 | 0 | **613** | 277 (45 %) |  |
| San Mauro di Saline | 567 | 1 | 566 | 0 | **566** | 44 (8 %) | 50 |
| Caldiero | 524 | 0 | 524 | 0 | **524** | 105 (20 %) | 13 |
| Cerro Veronese | 515 | 0 | 515 | 0 | **515** | 23 (4 %) | 58 |
| Roveredo di Guà | 515 | 0 | 515 | 0 | **515** | 106 (21 %) | 1 |
| Affi | 500 | 0 | 500 | 0 | **500** | 18 (4 %) | 21 |
| Castel d'Azzano | 485 | 0 | 485 | 0 | **485** | 86 (18 %) | 12 |
| Pastrengo | 461 | 10 | 451 | 0 | **451** | 20 (4 %) | 19 |
| Boschi Sant'Anna | 446 | 0 | 446 | 0 | **446** | 213 (48 %) | 2 |
| Concamarise | 391 | 0 | 391 | 7 | **384** | 142 (37 %) | 2 |
| Garda | 729 | 392 | 337 | 0 | **337** | 2 (1 %) | 28 |

## Parcs (6866)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Forêt de Dolcè (85) ⚠️ | Dolcè | 823 |
| Forêt de Brentino Belluno (94) ⚠️ | Brentino Belluno | 767 |
| Forêt de Costermano sul Garda (50) ⚠️ | Costermano sul Garda | 383 |
| Forêt de Brenzone sul Garda (73) ⚠️ | Brenzone sul Garda | 380 |
| Forêt de Malcesine (145) ⚠️ | Malcesine | 378 |
| Forêt de Malcesine (153) ⚠️ | Malcesine | 333 |
| Forêt de Selva di Progno (224) ⚠️ | Selva di Progno | 319 |
| Forêt de Fumane (210) ⚠️ | Fumane | 302 |
| Forêt de Verona (471) ⚠️ | Verona | 244 |
| Forêt de Dolcè (83) ⚠️ | Dolcè | 234 |
| Oasi Palude del Busatello ⚠️ | Gazzo Veronese | 229 |
| Oasi Palude del Busatello (2) ⚠️ | Gazzo Veronese | 229 |
| Forêt de Sant'Ambrogio di Valpolicella (30) ⚠️ | Sant'Ambrogio di Valpolicella | 204 |
| Forêt de Fumane (208) ⚠️ | Fumane | 189 |
| Forêt de Selva di Progno (229) ⚠️ | Selva di Progno | 182 |
| Forêt de San Zeno di Montagna (230) ⚠️ | San Zeno di Montagna | 181 |
| Forêt de Verona (472) ⚠️ | Verona | 177 |
| Forêt de Sant'Anna d'Alfaedo (271) ⚠️ | Sant'Anna d'Alfaedo | 175 |
| Forêt de Badia Calavena (222) ⚠️ | Badia Calavena | 158 |
| Foresta dei Folignani ⚠️ | Bosco Chiesanuova | 150 |
| Forêt de Brenzone sul Garda (70) ⚠️ | Brenzone sul Garda | 143 |
| Forêt de Erbezzo (209) ⚠️ | Erbezzo | 133 |
| Forêt de Brenzone sul Garda (78) ⚠️ | Brenzone sul Garda | 127 |
| Forêt de Sant'Anna d'Alfaedo (277) | Sant'Anna d'Alfaedo | 119 |
| Forêt de Torri del Benaco (35) | Torri del Benaco | 114 |
| Forêt de Marano di Valpolicella (24) | Marano di Valpolicella | 112 |
| Forêt de Caprino Veronese (352) | Caprino Veronese | 103 |
| Forêt de Fumane (206) | Fumane | 100 |
| Forêt de Bosco Chiesanuova (386) | Bosco Chiesanuova | 95 |
| Forêt de Verona (456) | Verona | 94 |
| Forêt de Ferrara di Monte Baldo (154) | Ferrara di Monte Baldo | 94 |
| Forêt de Torri del Benaco (36) | Torri del Benaco | 93 |
| Forêt de Selva di Progno (228) | Selva di Progno | 92 |
| Forêt de Malcesine (148) | Malcesine | 91 |
| Forêt de Selva di Progno (223) | Selva di Progno | 90 |
| Forêt de Tregnago (190) | Tregnago | 85 |
| Forêt de Affi | Affi | 84 |
| Forêt de Bosco Chiesanuova (372) | Bosco Chiesanuova | 83 |
| Forêt de Badia Calavena (227) | Badia Calavena | 83 |
| Forêt de Erbezzo (210) | Erbezzo | 82 |
| Forêt de Rivoli Veronese (31) | Rivoli Veronese | 81 |
| Forêt de Verona (459) | Verona | 80 |
| Forêt de Caprino Veronese (350) | Caprino Veronese | 76 |
| Forêt de Roverè Veronese (74) | Roverè Veronese | 75 |
| Forêt de Caprino Veronese (354) | Caprino Veronese | 75 |
| Forêt de Vestenanova (227) | Vestenanova | 75 |
| Bois de San Mauro di Saline (23) | San Mauro di Saline | 73 |
| Forêt de Garda (9) | Garda | 73 |
| Forêt de San Zeno di Montagna (62) | San Zeno di Montagna | 69 |
| Forêt de Vestenanova (224) | Vestenanova | 68 |
| Forêt de Tregnago (184) | Tregnago | 68 |
| Forêt de Malcesine (150) | Malcesine | 67 |
| Forêt de Malcesine (149) | Malcesine | 65 |
| Forêt de Erbezzo (204) | Erbezzo | 64 |
| Forêt de Tregnago (189) | Tregnago | 63 |
| Forêt de Grezzana (75) | Grezzana | 62 |
| Forêt de Roverè Veronese (53) | Roverè Veronese | 61 |
| Forêt de Verona (458) | Verona | 59 |
| Forêt de Tregnago (193) | Tregnago | 59 |
| Forêt de San Zeno di Montagna (229) | San Zeno di Montagna | 58 |
| Forêt de Negrar di Valpolicella (13) | Negrar di Valpolicella | 56 |
| Forêt de Sant'Anna d'Alfaedo (226) | Sant'Anna d'Alfaedo | 56 |
| Forêt de Badia Calavena (18) | Badia Calavena | 56 |
| Forêt de Bosco Chiesanuova (385) | Bosco Chiesanuova | 56 |
| Forêt de Selva di Progno (222) | Selva di Progno | 56 |
| Forêt de Grezzana (111) | Grezzana | 56 |
| Forêt de Rivoli Veronese (30) | Rivoli Veronese | 55 |
| Forêt de Sant'Ambrogio di Valpolicella (26) | Sant'Ambrogio di Valpolicella | 54 |
| Forêt de San Giovanni Ilarione (164) | San Giovanni Ilarione | 54 |
| Forêt de Tregnago (182) | Tregnago | 53 |
| Forêt de Roverè Veronese (94) | Roverè Veronese | 52 |
| Forêt de Caprino Veronese (356) | Caprino Veronese | 52 |
| Forêt de Bosco Chiesanuova (384) | Bosco Chiesanuova | 50 |
| Forêt de Vestenanova (220) | Vestenanova | 50 |
| Forêt de San Zeno di Montagna (99) | San Zeno di Montagna | 48 |
| Forêt de Grezzana (37) | Grezzana | 47 |
| Forêt de Caprino Veronese (16) | Caprino Veronese | 47 |
| Forêt de Selva di Progno (226) | Selva di Progno | 47 |
| Forêt de Selva di Progno (231) | Selva di Progno | 47 |
| Forêt de Malcesine (154) | Malcesine | 46 |
| Forêt de Grezzana (45) | Grezzana | 44 |
| Forêt de Negrar di Valpolicella (27) | Negrar di Valpolicella | 44 |
| Forêt de Roverè Veronese (38) | Roverè Veronese | 44 |
| Forêt de Erbezzo (196) | Erbezzo | 44 |
| Forêt de Sant'Anna d'Alfaedo (268) | Sant'Anna d'Alfaedo | 44 |
| Forêt de Ferrara di Monte Baldo (157) | Ferrara di Monte Baldo | 44 |
| Forêt de Vestenanova (218) | Vestenanova | 44 |
| Forêt de Badia Calavena (230) | Badia Calavena | 44 |
| Forêt de Tregnago (192) | Tregnago | 44 |
| Forêt de Garda (8) | Garda | 43 |
| Forêt de Erbezzo (200) | Erbezzo | 43 |
| Forêt de Grezzana (6) | Grezzana | 42 |
| Forêt de Malcesine (117) | Malcesine | 42 |
| Bois de Grezzana (35) | Grezzana | 42 |
| Forêt de Caprino Veronese (351) | Caprino Veronese | 42 |
| Forêt de Roncà (137) | Roncà | 42 |
| Forêt de Tregnago (185) | Tregnago | 41 |
| Forêt de Cerro Veronese (48) | Cerro Veronese | 40 |
| Forêt de Sant'Anna d'Alfaedo (273) | Sant'Anna d'Alfaedo | 40 |
| Forêt de Sant'Anna d'Alfaedo (275) | Sant'Anna d'Alfaedo | 40 |
| Forêt de Verona (467) | Verona | 40 |
| Forêt de Pastrengo (7) | Pastrengo | 40 |
| Forêt de Tregnago (191) | Tregnago | 40 |
| Forêt de Valeggio sul Mincio (36) | Valeggio sul Mincio | 39 |
| Forêt de Selva di Progno (217) | Selva di Progno | 38 |
| Forêt de Negrar di Valpolicella (78) | Negrar di Valpolicella | 38 |
| Forêt de Roverè Veronese (136) | Roverè Veronese | 38 |
| Forêt de Bosco Chiesanuova (359) | Bosco Chiesanuova | 37 |
| Forêt de Grezzana (94) | Grezzana | 37 |
| Forêt de Selva di Progno (130) | Selva di Progno | 37 |
| Forêt de Malcesine (147) | Malcesine | 37 |
| Forêt de Selva di Progno (230) | Selva di Progno | 37 |
| Forêt de Tregnago (183) | Tregnago | 37 |
| Bois de Badia Calavena | Badia Calavena | 36 |
| Forêt de Brenzone sul Garda (50) | Brenzone sul Garda | 36 |
| Bois de Grezzana (32) | Grezzana | 36 |
| Forêt de San Zeno di Montagna (223) | San Zeno di Montagna | 36 |
| Forêt de Ferrara di Monte Baldo (158) | Ferrara di Monte Baldo | 36 |
| Forêt de Erbezzo (205) | Erbezzo | 35 |
| Forêt de Erbezzo (208) | Erbezzo | 35 |
| Forêt de Sant'Anna d'Alfaedo (266) | Sant'Anna d'Alfaedo | 35 |
| Forêt de Bosco Chiesanuova (355) | Bosco Chiesanuova | 34 |
| Forêt de Tregnago (40) | Tregnago | 34 |
| Forêt de Bosco Chiesanuova (379) | Bosco Chiesanuova | 34 |
| Forêt de Verona (475) | Verona | 34 |
| Forêt de Grezzana (12) | Grezzana | 33 |
| Forêt de Cavaion Veronese (8) | Cavaion Veronese | 33 |
| Forêt de Selva di Progno (84) | Selva di Progno | 33 |
| Forêt de Verona (465) | Verona | 33 |
| Forêt de Badia Calavena (233) | Badia Calavena | 33 |
| Forêt de Roverè Veronese (68) | Roverè Veronese | 32 |
| Forêt de Selva di Progno (92) | Selva di Progno | 32 |
| Forêt de Brenzone sul Garda (71) | Brenzone sul Garda | 32 |
| Forêt de Ferrara di Monte Baldo (155) | Ferrara di Monte Baldo | 32 |
| Forêt de Fumane (211) | Fumane | 32 |
| Forêt de Badia Calavena (226) | Badia Calavena | 31 |
| Forêt de Vestenanova (99) | Vestenanova | 30 |
| Bois de San Mauro di Saline (18) | Roverè Veronese | 30 |
| Forêt de Caprino Veronese (353) | Caprino Veronese | 30 |
| Forêt de Erbezzo (168) | Erbezzo | 29 |
| Oasi Palude di Ostiglia | Gazzo Veronese | 29 |
| Forêt de Erbezzo (207) | Erbezzo | 29 |
| Forêt de Cazzano di Tramigna (6) | Cazzano di Tramigna | 28 |
| Forêt de Selva di Progno (15) | Selva di Progno | 28 |
| Palude del Busatello VR | Gazzo Veronese | 28 |
| Forêt de Tregnago (52) | Tregnago | 28 |
| Forêt de San Zeno di Montagna (222) | San Zeno di Montagna | 28 |
| Forêt de Badia Calavena (224) | Badia Calavena | 28 |
| Forêt de Grezzana (66) | Grezzana | 27 |
| Forêt de Bosco Chiesanuova (280) | Bosco Chiesanuova | 27 |
| Forêt de San Zeno di Montagna (55) | San Zeno di Montagna | 27 |
| Forêt de Caprino Veronese (216) | Caprino Veronese | 27 |
| Forêt de Marano di Valpolicella (40) | Marano di Valpolicella | 27 |
| Forêt de Caprino Veronese (360) | Caprino Veronese | 27 |
| Forêt de Cerro Veronese (15) | Cerro Veronese | 26 |
| Forêt de Brenzone sul Garda (75) | Brenzone sul Garda | 26 |
| Forêt de Ferrara di Monte Baldo | Ferrara di Monte Baldo | 25 |
| Forêt de Ferrara di Monte Baldo (6) | Ferrara di Monte Baldo | 25 |
| Forêt de Fumane (125) | Fumane | 25 |
| Forêt de Grezzana (87) | Grezzana | 25 |
| Forêt de Badia Calavena (17) | Badia Calavena | 25 |
| Forêt de Roncà (139) | Roncà | 25 |
| Forêt de Grezzana (110) | Grezzana | 25 |
| Forêt de Grezzana (83) | Grezzana | 24 |
| Forêt de Tregnago (82) | Tregnago | 24 |
| Forêt de Bosco Chiesanuova (382) | Bosco Chiesanuova | 24 |
| Forêt de Caprino Veronese (277) | Caprino Veronese | 23 |
| Forêt de Grezzana (97) | Grezzana | 23 |
| Forêt de Roverè Veronese (107) | Roverè Veronese | 23 |
| Bois de Negrar di Valpolicella (32) | Negrar di Valpolicella | 23 |
| Forêt de Sant'Anna d'Alfaedo (274) | Sant'Anna d'Alfaedo | 23 |
| Forêt de San Zeno di Montagna (227) | San Zeno di Montagna | 23 |
| Forêt de San Zeno di Montagna (231) | San Zeno di Montagna | 23 |
| Forêt de Grezzana (27) | Grezzana | 22 |
| Forêt de Sant'Anna d'Alfaedo (82) | Sant'Anna d'Alfaedo | 22 |
| Forêt de Bosco Chiesanuova (297) | Bosco Chiesanuova | 22 |
| Forêt de Caprino Veronese (159) | Caprino Veronese | 22 |
| Forêt de Malcesine (103) | Malcesine | 22 |
| Forêt de San Zeno di Montagna (134) | San Zeno di Montagna | 22 |
| Forêt de Selva di Progno (98) | Selva di Progno | 22 |
| Forêt de Negrar di Valpolicella (70) | Negrar di Valpolicella | 22 |
| Forêt de Badia Calavena (223) | Badia Calavena | 22 |
| Forêt de Lavagno (2) | San Martino Buon Albergo | 21 |
| Forêt de Velo Veronese (2) | Velo Veronese | 21 |
| Forêt de Roverè Veronese (48) | Roverè Veronese | 21 |
| Forêt de Brentino Belluno (54) | Brentino Belluno | 21 |
| Forêt de Rivoli Veronese (17) | Rivoli Veronese | 21 |
| Forêt de Roverè Veronese (105) | Roverè Veronese | 21 |
| Bois de Mezzane di Sotto (19) | Mezzane di Sotto | 21 |
| Forêt de Ferrara di Monte Baldo (153) | Ferrara di Monte Baldo | 21 |
| Forêt de Fumane (212) | Fumane | 21 |
| Forêt de Grezzana (108) | Grezzana | 21 |
| Forêt de San Giovanni Ilarione (179) | San Giovanni Ilarione | 21 |
| Forêt de Selva di Progno (233) | Selva di Progno | 21 |
| Forêt de San Zeno di Montagna (66) | San Zeno di Montagna | 20 |
| Forêt de Ferrara di Monte Baldo (85) | Ferrara di Monte Baldo | 20 |
| Forêt de Malcesine (55) | Malcesine | 20 |
| Forêt de Grezzana (96) | Grezzana | 20 |
| Bois de Mezzane di Sotto (2) | Mezzane di Sotto | 20 |
| Forêt de Brenzone sul Garda (77) | Brenzone sul Garda | 20 |
| Forêt de San Giovanni Ilarione (170) | San Giovanni Ilarione | 20 |
| Forêt de Velo Veronese | Velo Veronese | 19 |
| Forêt de Malcesine (15) | Malcesine | 19 |
| Forêt de Brenzone sul Garda (30) | Brenzone sul Garda | 19 |
| Forêt de Ferrara di Monte Baldo (52) | Ferrara di Monte Baldo | 19 |
| Forêt de Malcesine (127) | Malcesine | 19 |
| Forêt de Malcesine (129) | Malcesine | 19 |
| Forêt de Costermano sul Garda (3) | Costermano sul Garda | 19 |
| Forêt de San Zeno di Montagna (135) | San Zeno di Montagna | 19 |
| Forêt de Cerro Veronese (54) | Cerro Veronese | 19 |
| Forêt de Grezzana (102) | Grezzana | 19 |
| Forêt de Brentino Belluno (78) | Brentino Belluno | 19 |
| Forêt de Badia Calavena (42) | Badia Calavena | 19 |
| Bois de Mezzane di Sotto (8) | Mezzane di Sotto | 19 |
| Bois de Grezzana (30) | Grezzana | 19 |
| Bois de Roverè Veronese (18) | Roverè Veronese | 19 |
| Forêt de Verona (469) | Verona | 19 |
| Forêt de San Giovanni Ilarione (169) | San Giovanni Ilarione | 19 |
| Forêt de Badia Calavena (221) | Badia Calavena | 19 |
| Forêt de Negrar di Valpolicella (37) | Negrar di Valpolicella | 18 |
| Forêt de San Martino Buon Albergo (30) | San Martino Buon Albergo | 18 |
| Forêt de San Zeno di Montagna (5) | San Zeno di Montagna | 18 |
| Forêt de Brenzone sul Garda (55) | Brenzone sul Garda | 18 |
| Forêt de Ferrara di Monte Baldo (75) | Ferrara di Monte Baldo | 18 |
| Forêt de Ferrara di Monte Baldo (86) | Ferrara di Monte Baldo | 18 |
| Forêt de Fumane (7) | Fumane | 18 |
| Forêt de Malcesine (99) | Malcesine | 18 |
| Forêt de San Zeno di Montagna (169) | San Zeno di Montagna | 18 |
| Forêt de San Giovanni Ilarione (92) | San Giovanni Ilarione | 18 |
| Bois de Mezzane di Sotto (10) | Mezzane di Sotto | 18 |
| Forêt de Dolcè (84) | Dolcè | 18 |
| Forêt de Montecchia di Crosara (90) | Montecchia di Crosara | 18 |
| Forêt de Roncà (140) | Roncà | 18 |
| Forêt de Badia Calavena (219) | Badia Calavena | 18 |
| Bois de Bonavigo (5) | Bonavigo | 18 |
| Forêt de Grezzana (15) | Grezzana | 17 |
| Forêt de Sant'Anna d'Alfaedo (105) | Sant'Anna d'Alfaedo | 17 |
| Forêt de Sant'Anna d'Alfaedo (164) | Sant'Anna d'Alfaedo | 17 |
| Forêt de Bosco Chiesanuova (175) | Bosco Chiesanuova | 17 |
| Forêt de Bosco Chiesanuova (352) | Bosco Chiesanuova | 17 |
| Forêt de Caprino Veronese (6) | Caprino Veronese | 17 |
| Forêt de Malcesine (33) | Malcesine | 17 |
| Forêt de Roverè Veronese (139) | Roverè Veronese | 17 |
| Forêt de Erbezzo (206) | Erbezzo | 17 |
| Forêt de Sant'Anna d'Alfaedo (276) | Sant'Anna d'Alfaedo | 17 |
| Forêt de Velo Veronese (54) | Velo Veronese | 17 |
| Forêt de Malcesine (146) | Malcesine | 17 |
| Forêt de Vestenanova (222) | Vestenanova | 17 |
| Forêt de Badia Calavena (220) | Badia Calavena | 17 |
| Forêt de Tregnago (188) | Tregnago | 17 |
| Forêt de Roverè Veronese (9) | Roverè Veronese | 16 |
| Forêt de Cerro Veronese (7) | Cerro Veronese | 16 |
| Forêt de Roverè Veronese (72) | Roverè Veronese | 16 |
| Forêt de Grezzana (107) | Grezzana | 16 |
| Forêt de Sant'Anna d'Alfaedo (267) | Sant'Anna d'Alfaedo | 16 |
| Forêt de Caprino Veronese (343) | Caprino Veronese | 16 |
| Forêt de Roncà (138) | Roncà | 16 |
| Forêt de Montecchia di Crosara (92) | Montecchia di Crosara | 16 |
| Forêt de Sant'Anna d'Alfaedo (58) | Sant'Anna d'Alfaedo | 15 |
| Forêt de Sant'Anna d'Alfaedo (122) | Sant'Anna d'Alfaedo | 15 |
| Forêt de Bosco Chiesanuova (202) | Bosco Chiesanuova | 15 |
| Forêt de Bosco Chiesanuova (216) | Bosco Chiesanuova | 15 |
| Forêt de Ferrara di Monte Baldo (2) | Ferrara di Monte Baldo | 15 |
| Forêt de Ferrara di Monte Baldo (23) | Ferrara di Monte Baldo | 15 |
| Forêt de Malcesine (66) | Malcesine | 15 |
| Forêt de Selva di Progno (139) | Selva di Progno | 15 |
| Forêt de Roverè Veronese (104) | Roverè Veronese | 15 |
| Forêt de Roverè Veronese (106) | Roverè Veronese | 15 |
| Bois de Velo Veronese (25) | Velo Veronese | 15 |
| Bois de San Mauro di Saline (25) | San Mauro di Saline | 15 |
| Forêt de Roverè Veronese (140) | Roverè Veronese | 15 |
| Forêt de San Zeno di Montagna (228) | San Zeno di Montagna | 15 |
| Forêt de Caprino Veronese (346) | Caprino Veronese | 15 |
| Forêt de Caprino Veronese (348) | Caprino Veronese | 15 |
| Forêt de Ferrara di Monte Baldo (152) | Ferrara di Monte Baldo | 15 |
| Forêt de San Giovanni Ilarione (168) | San Giovanni Ilarione | 15 |
| Forêt de Grezzana (18) | Grezzana | 14 |
| Forêt de Roverè Veronese (14) | Roverè Veronese | 14 |
| Forêt de Negrar di Valpolicella (29) | Negrar di Valpolicella | 14 |
| Forêt de Negrar di Valpolicella (66) | Negrar di Valpolicella | 14 |
| Forêt de San Zeno di Montagna (15) | San Zeno di Montagna | 14 |
| Forêt de Caprino Veronese (275) | Caprino Veronese | 14 |
| Forêt de Fumane (38) | Fumane | 14 |
| Forêt de Malcesine (126) | Malcesine | 14 |
| Forêt de Malcesine (130) | Malcesine | 14 |
| Bois de Grezzana (12) | Grezzana | 14 |
| Forêt de Selva di Progno (56) | Selva di Progno | 14 |
| Forêt de Roverè Veronese (111) | Roverè Veronese | 14 |
| Bois de Affi | Affi | 14 |
| Forêt de Roverè Veronese (138) | Roverè Veronese | 14 |
| Forêt de Vestenanova (229) | Vestenanova | 14 |
| Forêt de San Zeno di Montagna (232) | San Zeno di Montagna | 14 |
| Forêt de Cerro Veronese (14) | Cerro Veronese | 13 |
| Forêt de Sommacampagna (8) | Sommacampagna | 13 |
| Forêt de Roverè Veronese (51) | Roverè Veronese | 13 |
| Forêt de Erbezzo (92) | Erbezzo | 13 |
| Forêt de Erbezzo (104) | Erbezzo | 13 |
| Forêt de Sant'Anna d'Alfaedo (80) | Sant'Anna d'Alfaedo | 13 |
| Forêt de San Zeno di Montagna (46) | San Zeno di Montagna | 13 |
| Forêt de Fumane (145) | Fumane | 13 |
| Forêt de Dolcè (11) | Dolcè | 13 |
| Forêt de Dolcè (16) | Dolcè | 13 |
| Forêt de San Zeno di Montagna (128) | San Zeno di Montagna | 13 |
| Forêt de Marano di Valpolicella (28) | Marano di Valpolicella | 13 |
| Forêt de Roncà (121) | Roncà | 13 |
| Bois de Grezzana (8) | Grezzana | 13 |
| Forêt de Selva di Progno (30) | Selva di Progno | 13 |
| Bois de Grezzana (61) | Grezzana | 13 |
| Bois de Grezzana (68) | Grezzana | 13 |
| Forêt de Verona (474) | Verona | 13 |
| Forêt de San Giovanni Ilarione (167) | San Giovanni Ilarione | 13 |
| Forêt de San Giovanni Ilarione (174) | San Giovanni Ilarione | 13 |
| Forêt de Negrar di Valpolicella (28) | Negrar di Valpolicella | 12 |
| Parco Le Vallette | Cerea | 12 |
| Forêt de Erbezzo (147) | Erbezzo | 12 |
| Forêt de Caprino Veronese (184) | Caprino Veronese | 12 |
| Forêt de Brenzone sul Garda (60) | Brenzone sul Garda | 12 |
| Forêt de Ferrara di Monte Baldo (72) | Ferrara di Monte Baldo | 12 |
| Forêt de Ferrara di Monte Baldo (93) | Ferrara di Monte Baldo | 12 |
| Forêt de Fumane (41) | Fumane | 12 |
| Forêt de Malcesine (42) | Malcesine | 12 |
| Forêt de Malcesine (49) | Malcesine | 12 |
| Forêt de Fumane (118) | Fumane | 12 |
| Forêt de Rivoli Veronese (23) | Rivoli Veronese | 12 |
| Forêt de Roncà (36) | Roncà | 12 |
| Forêt de Selva di Progno (80) | Selva di Progno | 12 |
| Forêt de Montecchia di Crosara (49) | Montecchia di Crosara | 12 |
| Forêt de Roverè Veronese (109) | Roverè Veronese | 12 |
| Bois de Albaredo d'Adige | Albaredo d'Adige | 12 |
| Bois de San Mauro di Saline (34) | San Mauro di Saline | 12 |
| Bois de Roverè Veronese (24) | Roverè Veronese | 12 |
| Forêt de Sant'Anna d'Alfaedo (270) | Sant'Anna d'Alfaedo | 12 |
| Forêt de Bosco Chiesanuova (373) | Bosco Chiesanuova | 12 |
| Forêt de Bosco Chiesanuova (375) | Bosco Chiesanuova | 12 |
| Forêt de Bosco Chiesanuova (383) | Bosco Chiesanuova | 12 |
| Forêt de Malcesine (156) | Malcesine | 12 |
| Forêt de Roncà (136) | Roncà | 12 |
| Forêt de San Giovanni Ilarione (165) | San Giovanni Ilarione | 12 |
| Forêt de Grezzana (109) | Grezzana | 12 |
| Forêt de Brenzone sul Garda (80) | Brenzone sul Garda | 12 |
| Ex Cava Speziala | Verona | 11 |
| Forêt de San Martino Buon Albergo (29) | San Martino Buon Albergo | 11 |
| Forêt de Velo Veronese (16) | Velo Veronese | 11 |
| Forêt de Bosco Chiesanuova (163) | Bosco Chiesanuova | 11 |
| Forêt de Verona (91) | Verona | 11 |
| Forêt de Grezzana (85) | Grezzana | 11 |
| Forêt de Verona (295) | Verona | 11 |
| Forêt de Malcesine (17) | Malcesine | 11 |
| Bois de Valeggio sul Mincio (3) | Valeggio sul Mincio | 11 |
| Forêt de Malcesine (21) | Malcesine | 11 |
| Forêt de Grezzana (92) | Grezzana | 11 |
| Forêt de Vestenanova (186) | Vestenanova | 11 |
| Forêt de Peschiera del Garda (7) | Peschiera del Garda | 11 |
| Forêt de San Giovanni Ilarione (115) | San Giovanni Ilarione | 11 |
| Forêt de Roverè Veronese (103) | Roverè Veronese | 11 |
| Forêt de Tregnago (44) | Tregnago | 11 |
| Bois de San Mauro di Saline (26) | San Mauro di Saline | 11 |
| Bois de Negrar di Valpolicella (28) | Negrar di Valpolicella | 11 |
| Forêt de Roverè Veronese (141) | Roverè Veronese | 11 |
| Forêt de San Zeno di Montagna (221) | San Zeno di Montagna | 11 |
| Forêt de Fumane (205) | Fumane | 11 |
| Forêt de Vestenanova (216) | Vestenanova | 11 |
| Forêt de Vestenanova (223) | Vestenanova | 11 |
| Forêt de San Giovanni Ilarione (177) | San Giovanni Ilarione | 11 |
| Forêt de Badia Calavena (231) | Badia Calavena | 11 |
| Forêt de Tregnago (181) | Tregnago | 11 |
| Forêt de Valeggio sul Mincio | Valeggio sul Mincio | 10 |
| Forêt de Cerro Veronese (21) | Cerro Veronese | 10 |
| Forêt de Negrar di Valpolicella (48) | Negrar di Valpolicella | 10 |
| Forêt de Caprino Veronese (191) | Caprino Veronese | 10 |
| Forêt de Caprino Veronese (214) | Caprino Veronese | 10 |
| Forêt de Caprino Veronese (222) | Caprino Veronese | 10 |
| Forêt de Brenzone sul Garda (61) | Brenzone sul Garda | 10 |
| Forêt de Brentino Belluno (6) | Brentino Belluno | 10 |
| Forêt de Malcesine (84) | Malcesine | 10 |
| Forêt de Malcesine (118) | Malcesine | 10 |
| Forêt de Dolcè (6) | Dolcè | 10 |
| Forêt de Dolcè (24) | Dolcè | 10 |
| Forêt de Dolcè (50) | Dolcè | 10 |
| Forêt de Caprino Veronese (308) | Caprino Veronese | 10 |
| Forêt de Cazzano di Tramigna (18) | Cazzano di Tramigna | 10 |
| Forêt de Vestenanova (52) | Vestenanova | 10 |
| Forêt de Vestenanova (134) | Vestenanova | 10 |
| Forêt de Rivoli Veronese (29) | Rivoli Veronese | 10 |
| Forêt de Grezzana (106) | Grezzana | 10 |
| Bois de San Mauro di Saline (16) | San Mauro di Saline | 10 |
| Bois de Grezzana (45) | Grezzana | 10 |
| Bois de Grezzana (64) | Grezzana | 10 |
| Forêt de Bosco Chiesanuova (377) | Bosco Chiesanuova | 10 |
| Forêt de Verona (453) | Verona | 10 |
| Forêt de Caprino Veronese (345) | Caprino Veronese | 10 |
| Forêt de Ferrara di Monte Baldo (156) | Ferrara di Monte Baldo | 10 |
| Forêt de Soave (29) | Soave | 10 |
| Forêt de Roncà (133) | Roncà | 10 |
| Forêt de Selva di Progno (225) | Selva di Progno | 10 |
| Forêt de Badia Calavena (228) | Badia Calavena | 10 |
| Forêt de Tregnago (186) | Tregnago | 10 |
| Forêt de San Mauro di Saline (5) ⚠️ | San Mauro di Saline | 9 |
| Forêt de Mezzane di Sotto (22) ⚠️ | Mezzane di Sotto | 9 |
| Forêt de Roverè Veronese (5) ⚠️ | Roverè Veronese | 9 |
| Forêt de San Martino Buon Albergo (19) ⚠️ | San Martino Buon Albergo | 9 |
| Forêt de Negrar di Valpolicella (34) ⚠️ | Negrar di Valpolicella | 9 |
| Forêt de Negrar di Valpolicella (42) ⚠️ | Negrar di Valpolicella | 9 |
| Forêt de Verona (65) ⚠️ | Verona | 9 |
| Forêt de Verona (302) ⚠️ | Verona | 9 |
| Forêt de Verona (318) ⚠️ | Verona | 9 |
| Forêt de Verona (329) ⚠️ | Verona | 9 |
| Forêt de San Zeno di Montagna (95) ⚠️ | San Zeno di Montagna | 9 |
| Forêt de San Zeno di Montagna (111) ⚠️ | San Zeno di Montagna | 9 |
| Forêt de Caprino Veronese (163) ⚠️ | Caprino Veronese | 9 |
| Forêt de Caprino Veronese (230) ⚠️ | Caprino Veronese | 9 |
| Forêt de Brenzone sul Garda (8) ⚠️ | Brenzone sul Garda | 9 |
| Forêt de Ferrara di Monte Baldo (18) ⚠️ | Ferrara di Monte Baldo | 9 |
| Forêt de Ferrara di Monte Baldo (37) ⚠️ | Ferrara di Monte Baldo | 9 |
| Forêt de Brentino Belluno (13) ⚠️ | Brentino Belluno | 9 |
| Forêt de Malcesine (31) ⚠️ | Malcesine | 9 |
| Forêt de Malcesine (135) ⚠️ | Malcesine | 9 |
| Forêt de San Zeno di Montagna (205) ⚠️ | San Zeno di Montagna | 9 |
| Parc de Roncà (2) ⚠️ | Roncà | 9 |
| Forêt de Vestenanova (65) ⚠️ | Vestenanova | 9 |
| Bois de Grezzana (27) ⚠️ | Grezzana | 9 |
| Forêt de San Giovanni Ilarione (27) ⚠️ | San Giovanni Ilarione | 9 |
| Forêt de Negrar di Valpolicella (69) ⚠️ | Negrar di Valpolicella | 9 |
| Bois de Rivoli Veronese (5) ⚠️ | Rivoli Veronese | 9 |
| Forêt de Roverè Veronese (132) ⚠️ | Roverè Veronese | 9 |
| Bois de Velo Veronese (24) ⚠️ | Velo Veronese | 9 |
| Bois de San Mauro di Saline (36) ⚠️ | San Mauro di Saline | 9 |
| Bois de Negrar di Valpolicella (24) ⚠️ | Negrar di Valpolicella | 9 |
| Bois de Negrar di Valpolicella (34) ⚠️ | Negrar di Valpolicella | 9 |
| Forêt de Bosco Chiesanuova (376) ⚠️ | Bosco Chiesanuova | 9 |
| Forêt de Verona (450) ⚠️ | Verona | 9 |
| Forêt de Verona (466) ⚠️ | Verona | 9 |
| Forêt de Fumane (204) ⚠️ | Fumane | 9 |
| Forêt de Malcesine (151) ⚠️ | Malcesine | 9 |
| Forêt de Malcesine (155) ⚠️ | Malcesine | 9 |
| Forêt de Vestenanova (215) ⚠️ | Vestenanova | 9 |
| Forêt de San Mauro di Saline (2) ⚠️ | San Mauro di Saline | 8 |
| Forêt de Negrar di Valpolicella (21) ⚠️ | Negrar di Valpolicella | 8 |
| Bois de San Giovanni Lupatoto ⚠️ | San Giovanni Lupatoto | 8 |
| Forêt de San Martino Buon Albergo (14) ⚠️ | San Martino Buon Albergo | 8 |
| Forêt de Negrar di Valpolicella (30) ⚠️ | Negrar di Valpolicella | 8 |
| Forêt de Grezzana (79) ⚠️ | Grezzana | 8 |
| Forêt de Grezzana (82) ⚠️ | Grezzana | 8 |
| Forêt de San Mauro di Saline (11) ⚠️ | San Mauro di Saline | 8 |
| Forêt de San Martino Buon Albergo (39) ⚠️ | San Martino Buon Albergo | 8 |
| Forêt de Erbezzo (6) ⚠️ | Erbezzo | 8 |
| Forêt de Erbezzo (35) ⚠️ | Erbezzo | 8 |
| Forêt de Erbezzo (41) ⚠️ | Erbezzo | 8 |
| Forêt de Erbezzo (62) ⚠️ | Erbezzo | 8 |
| Forêt de Erbezzo (77) ⚠️ | Erbezzo | 8 |
| Forêt de Sant'Anna d'Alfaedo (40) ⚠️ | Sant'Anna d'Alfaedo | 8 |
| Forêt de Sant'Anna d'Alfaedo (84) ⚠️ | Sant'Anna d'Alfaedo | 8 |
| Forêt de Sant'Anna d'Alfaedo (88) ⚠️ | Sant'Anna d'Alfaedo | 8 |
| Forêt de Bosco Chiesanuova (368) ⚠️ | Bosco Chiesanuova | 8 |
| Forêt de Verona (267) ⚠️ | Verona | 8 |
| Forêt de Verona (391) ⚠️ | Verona | 8 |
| Forêt de Caprino Veronese (24) ⚠️ | Caprino Veronese | 8 |
| Forêt de Caprino Veronese (155) ⚠️ | Caprino Veronese | 8 |
| Forêt de Caprino Veronese (239) ⚠️ | Caprino Veronese | 8 |
| Forêt de Caprino Veronese (270) ⚠️ | Caprino Veronese | 8 |
| Forêt de Ferrara di Monte Baldo (99) ⚠️ | Ferrara di Monte Baldo | 8 |
| Forêt de Malcesine (110) ⚠️ | Malcesine | 8 |
| Forêt de Malcesine (123) ⚠️ | Malcesine | 8 |
| Forêt de Garda (2) ⚠️ | Garda | 8 |
| Forêt de Rivoli Veronese (15) ⚠️ | Rivoli Veronese | 8 |
| Forêt de San Giovanni Ilarione ⚠️ | San Giovanni Ilarione | 8 |
| Forêt de Cazzano di Tramigna (23) ⚠️ | Cazzano di Tramigna | 8 |
| Forêt de San Giovanni Ilarione (83) ⚠️ | San Giovanni Ilarione | 8 |
| Forêt de Selva di Progno (39) ⚠️ | Selva di Progno | 8 |
| Forêt de Selva di Progno (133) ⚠️ | Selva di Progno | 8 |
| Forêt de Selva di Progno (135) ⚠️ | Selva di Progno | 8 |
| Forêt de Roverè Veronese (100) ⚠️ | Roverè Veronese | 8 |
| Bois de Rivoli Veronese ⚠️ | Rivoli Veronese | 8 |
| Forêt de Tregnago (61) ⚠️ | Tregnago | 8 |
| Forêt de Tregnago (86) ⚠️ | Tregnago | 8 |
| Bois de Roverè Veronese (8) ⚠️ | Roverè Veronese | 8 |
| Bois de Mezzane di Sotto (12) ⚠️ | Mezzane di Sotto | 8 |
| Bois de Verona (20) ⚠️ | Verona | 8 |
| Bois de Grezzana (56) ⚠️ | Grezzana | 8 |
| Bois de Negrar di Valpolicella (37) ⚠️ | Negrar di Valpolicella | 8 |
| Forêt de Roverè Veronese (137) ⚠️ | Velo Veronese | 8 |
| Forêt de Brenzone sul Garda (72) ⚠️ | Brenzone sul Garda | 8 |
| Forêt de Roncà (134) ⚠️ | Roncà | 8 |
| Forêt de Roncà (135) ⚠️ | Roncà | 8 |
| Forêt de Vestenanova (217) ⚠️ | Vestenanova | 8 |
| Forêt de Vestenanova (221) ⚠️ | Vestenanova | 8 |
| Forêt de Montecchia di Crosara (93) ⚠️ | Montecchia di Crosara | 8 |
| Forêt de Mezzane di Sotto (16) ⚠️ | Mezzane di Sotto | 7 |
| Forêt de Negrar di Valpolicella (6) ⚠️ | Negrar di Valpolicella | 7 |
| Forêt de Sommacampagna (9) ⚠️ | Sommacampagna | 7 |
| Forêt de Cavaion Veronese (2) ⚠️ | Cavaion Veronese | 7 |
| Parc de Belfiore (8) ⚠️ | Belfiore | 7 |
| Forêt de Negrar di Valpolicella (64) ⚠️ | Negrar di Valpolicella | 7 |
| Forêt de Valeggio sul Mincio (27) ⚠️ | Valeggio sul Mincio | 7 |
| Parco urbano del Tione ⚠️ | Villafranca di Verona | 7 |
| Forêt de Erbezzo (31) ⚠️ | Erbezzo | 7 |
| Forêt de Erbezzo (66) ⚠️ | Erbezzo | 7 |
| Forêt de Sant'Anna d'Alfaedo (11) ⚠️ | Sant'Anna d'Alfaedo | 7 |
| Forêt de Sant'Anna d'Alfaedo (78) ⚠️ | Sant'Anna d'Alfaedo | 7 |
| Forêt de Sant'Anna d'Alfaedo (99) ⚠️ | Sant'Anna d'Alfaedo | 7 |
| Forêt de Bosco Chiesanuova (49) ⚠️ | Bosco Chiesanuova | 7 |
| Forêt de Bosco Chiesanuova (51) ⚠️ | Bosco Chiesanuova | 7 |
| Forêt de Bosco Chiesanuova (63) ⚠️ | Bosco Chiesanuova | 7 |
| Forêt de Bosco Chiesanuova (217) ⚠️ | Bosco Chiesanuova | 7 |
| Forêt de Bosco Chiesanuova (222) ⚠️ | Bosco Chiesanuova | 7 |
| Forêt de Verona (383) ⚠️ | Verona | 7 |
| Forêt de San Zeno di Montagna (26) ⚠️ | San Zeno di Montagna | 7 |
| Forêt de San Zeno di Montagna (115) ⚠️ | San Zeno di Montagna | 7 |
| Forêt de Brenzone sul Garda (20) ⚠️ | Brenzone sul Garda | 7 |
| Forêt de Brenzone sul Garda (28) ⚠️ | Brenzone sul Garda | 7 |
| Forêt de Ferrara di Monte Baldo (57) ⚠️ | Ferrara di Monte Baldo | 7 |
| Forêt de Ferrara di Monte Baldo (76) ⚠️ | Ferrara di Monte Baldo | 7 |
| Forêt de Ferrara di Monte Baldo (94) ⚠️ | Ferrara di Monte Baldo | 7 |
| Forêt de Ferrara di Monte Baldo (105) ⚠️ | Ferrara di Monte Baldo | 7 |
| Forêt de Fumane (11) ⚠️ | Fumane | 7 |
| Forêt de Malcesine (44) ⚠️ | Malcesine | 7 |
| Forêt de Malcesine (48) ⚠️ | Malcesine | 7 |
| Forêt de Fumane (136) ⚠️ | Fumane | 7 |
| Forêt de Soave (4) ⚠️ | Soave | 7 |
| Forêt de Vestenanova (28) ⚠️ | Vestenanova | 7 |
| Forêt de Vestenanova (54) ⚠️ | Vestenanova | 7 |
| Forêt de Selva di Progno (74) ⚠️ | Selva di Progno | 7 |
| Forêt de Selva di Progno (88) ⚠️ | Selva di Progno | 7 |
| Forêt de Selva di Progno (124) ⚠️ | Selva di Progno | 7 |
| Forêt de Selva di Progno (138) ⚠️ | Selva di Progno | 7 |
| Forêt de Badia Calavena (70) ⚠️ | Badia Calavena | 7 |
| Forêt de Badia Calavena (78) ⚠️ | Badia Calavena | 7 |
| Forêt de Tregnago (60) ⚠️ | Tregnago | 7 |
| Forêt de Roverè Veronese (129) ⚠️ | Roverè Veronese | 7 |
| Bois de Ronco all'Adige (13) ⚠️ | Ronco all'Adige | 7 |
| Bois de Roverè Veronese (26) ⚠️ | Roverè Veronese | 7 |
| Forêt de Sant'Anna d'Alfaedo (269) ⚠️ | Sant'Anna d'Alfaedo | 7 |
| Forêt de Bosco Chiesanuova (371) ⚠️ | Bosco Chiesanuova | 7 |
| Forêt de Verona (457) ⚠️ | Verona | 7 |
| Forêt de Verona (460) ⚠️ | Verona | 7 |
| Forêt de Verona (461) ⚠️ | Verona | 7 |
| Forêt de Brenzone sul Garda (74) ⚠️ | Brenzone sul Garda | 7 |
| Forêt de San Giovanni Ilarione (166) ⚠️ | San Giovanni Ilarione | 7 |
| Forêt de Selva di Progno (232) ⚠️ | Selva di Progno | 7 |
| Forêt de Tregnago (187) ⚠️ | Tregnago | 7 |
| Forêt de San Martino Buon Albergo ⚠️ | San Martino Buon Albergo | 6 |
| Bois de Legnago ⚠️ | Legnago | 6 |
| Forêt de Grezzana (2) ⚠️ | Grezzana | 6 |
| Forêt de Grezzana (17) ⚠️ | Grezzana | 6 |
| Forêt de Grezzana (23) ⚠️ | Grezzana | 6 |
| Forêt de San Martino Buon Albergo (11) ⚠️ | San Martino Buon Albergo | 6 |
| Forêt de San Martino Buon Albergo (27) ⚠️ | San Martino Buon Albergo | 6 |
| Forêt de Valeggio sul Mincio (5) ⚠️ | Valeggio sul Mincio | 6 |
| Bois de San Martino Buon Albergo (3) ⚠️ | San Martino Buon Albergo | 6 |
| Forêt de Marano di Valpolicella (5) ⚠️ | Marano di Valpolicella | 6 |
| Forêt de Roverè Veronese (24) ⚠️ | Roverè Veronese | 6 |
| Forêt de Negrar di Valpolicella (63) ⚠️ | Negrar di Valpolicella | 6 |
| Forêt de Negrar di Valpolicella (65) ⚠️ | Negrar di Valpolicella | 6 |
| Forêt de Sommacampagna (19) ⚠️ | Sommacampagna | 6 |
| Forêt de Erbezzo (20) ⚠️ | Erbezzo | 6 |
| Forêt de Erbezzo (170) ⚠️ | Erbezzo | 6 |
| Forêt de Sant'Anna d'Alfaedo (81) ⚠️ | Sant'Anna d'Alfaedo | 6 |
| Forêt de Bosco Chiesanuova (31) ⚠️ | Bosco Chiesanuova | 6 |
| Forêt de Bosco Chiesanuova (70) ⚠️ | Bosco Chiesanuova | 6 |
| Forêt de Bosco Chiesanuova (75) ⚠️ | Bosco Chiesanuova | 6 |
| Forêt de Bosco Chiesanuova (84) ⚠️ | Bosco Chiesanuova | 6 |
| Forêt de Bosco Chiesanuova (105) ⚠️ | Bosco Chiesanuova | 6 |
| Forêt de Bosco Chiesanuova (122) ⚠️ | Bosco Chiesanuova | 6 |
| Forêt de Bosco Chiesanuova (208) ⚠️ | Bosco Chiesanuova | 6 |
| Forêt de Verona (16) ⚠️ | Verona | 6 |
| Forêt de Grezzana (84) ⚠️ | Grezzana | 6 |
| Forêt de Verona (158) ⚠️ | Verona | 6 |
| Forêt de Verona (160) ⚠️ | Verona | 6 |
| Forêt de San Zeno di Montagna (19) ⚠️ | San Zeno di Montagna | 6 |
| Forêt de San Zeno di Montagna (93) ⚠️ | San Zeno di Montagna | 6 |
| Forêt de Caprino Veronese (57) ⚠️ | Caprino Veronese | 6 |
| Forêt de Caprino Veronese (80) ⚠️ | Caprino Veronese | 6 |
| Forêt de Caprino Veronese (181) ⚠️ | Caprino Veronese | 6 |
| Forêt de Caprino Veronese (221) ⚠️ | Caprino Veronese | 6 |
| Forêt de Brenzone sul Garda (9) ⚠️ | Brenzone sul Garda | 6 |
| Forêt de Brenzone sul Garda (13) ⚠️ | Brenzone sul Garda | 6 |
| Forêt de Brenzone sul Garda (29) ⚠️ | Brenzone sul Garda | 6 |
| Forêt de Brenzone sul Garda (44) ⚠️ | Brenzone sul Garda | 6 |
| Forêt de Brenzone sul Garda (47) ⚠️ | Brenzone sul Garda | 6 |
| Forêt de Ferrara di Monte Baldo (13) ⚠️ | Ferrara di Monte Baldo | 6 |
| Forêt de Ferrara di Monte Baldo (15) ⚠️ | Ferrara di Monte Baldo | 6 |
| Forêt de Ferrara di Monte Baldo (21) ⚠️ | Ferrara di Monte Baldo | 6 |
| Forêt de Ferrara di Monte Baldo (68) ⚠️ | Ferrara di Monte Baldo | 6 |
| Forêt de Fumane (9) ⚠️ | Fumane | 6 |
| Forêt de Brentino Belluno (9) ⚠️ | Brentino Belluno | 6 |
| Forêt de Ferrara di Monte Baldo (111) ⚠️ | Ferrara di Monte Baldo | 6 |
| Forêt de Malcesine (30) ⚠️ | Malcesine | 6 |
| Forêt de Malcesine (73) ⚠️ | Malcesine | 6 |
| Forêt de Malcesine (76) ⚠️ | Malcesine | 6 |
| Forêt de Malcesine (122) ⚠️ | Malcesine | 6 |
| Forêt de Dolcè (26) ⚠️ | Dolcè | 6 |
| Forêt de Fumane (161) ⚠️ | Fumane | 6 |
| Forêt de Garda ⚠️ | Garda | 6 |
| Forêt de Illasi (14) ⚠️ | Illasi | 6 |
| Forêt de Cazzano di Tramigna (5) ⚠️ | Cazzano di Tramigna | 6 |
| Forêt de Roncà (46) ⚠️ | Roncà | 6 |
| Forêt de Roncà (69) ⚠️ | Roncà | 6 |
| Forêt de Vestenanova (39) ⚠️ | Vestenanova | 6 |
| Forêt de Vestenanova (40) ⚠️ | Vestenanova | 6 |
| Forêt de San Giovanni Ilarione (34) ⚠️ | San Giovanni Ilarione | 6 |
| Forêt de San Giovanni Ilarione (155) ⚠️ | San Giovanni Ilarione | 6 |
| Forêt de Selva di Progno (14) ⚠️ | Selva di Progno | 6 |
| Forêt de Selva di Progno (42) ⚠️ | Selva di Progno | 6 |
| Forêt de Selva di Progno (167) ⚠️ | Selva di Progno | 6 |
| Forêt de Selva di Progno (190) ⚠️ | Selva di Progno | 6 |
| Forêt de Montecchia di Crosara (35) ⚠️ | Montecchia di Crosara | 6 |
| Forêt de Montecchia di Crosara (71) ⚠️ | Montecchia di Crosara | 6 |
| Forêt de Roverè Veronese (101) ⚠️ | Roverè Veronese | 6 |
| Forêt de Lazise (18) ⚠️ | Lazise | 6 |
| Forêt de Montecchia di Crosara (89) ⚠️ | Montecchia di Crosara | 6 |
| Forêt de Badia Calavena (50) ⚠️ | Badia Calavena | 6 |
| Forêt de Tregnago (33) ⚠️ | Tregnago | 6 |
| Bois de Grezzana (49) ⚠️ | Grezzana | 6 |
| Bois de Mezzane di Sotto (41) ⚠️ | Mezzane di Sotto | 6 |
| Forêt de Sant'Anna d'Alfaedo (272) ⚠️ | Sant'Anna d'Alfaedo | 6 |
| Forêt de Bosco Chiesanuova (374) ⚠️ | Bosco Chiesanuova | 6 |
| Forêt de Verona (452) ⚠️ | Verona | 6 |
| Forêt de Verona (470) ⚠️ | Verona | 6 |
| Forêt de San Zeno di Montagna (226) ⚠️ | San Zeno di Montagna | 6 |
| Forêt de Caprino Veronese (355) ⚠️ | Caprino Veronese | 6 |
| Forêt de Fumane (209) ⚠️ | Fumane | 6 |
| Forêt de Vestenanova (219) ⚠️ | Vestenanova | 6 |
| Forêt de Selva di Progno (227) ⚠️ | Selva di Progno | 6 |
| Forêt de Badia Calavena (225) ⚠️ | Badia Calavena | 6 |
| Forêt de Grezzana (39) ⚠️ | Grezzana | 5 |
| Forêt de Negrar di Valpolicella (14) ⚠️ | Negrar di Valpolicella | 5 |
| Forêt de Cerro Veronese (20) ⚠️ | Cerro Veronese | 5 |
| Forêt de Negrar di Valpolicella (24) ⚠️ | Negrar di Valpolicella | 5 |
| Forêt de Negrar di Valpolicella (35) ⚠️ | Negrar di Valpolicella | 5 |
| Bois de Velo Veronese (3) ⚠️ | Velo Veronese | 5 |
| Forêt de Sant'Ambrogio di Valpolicella (9) ⚠️ | Sant'Ambrogio di Valpolicella | 5 |
| Forêt de Marano di Valpolicella (6) ⚠️ | Marano di Valpolicella | 5 |
| Forêt de Negrar di Valpolicella (59) ⚠️ | Negrar di Valpolicella | 5 |
| Forêt de Sona (15) ⚠️ | Sona | 5 |
| Forêt de Nogara (3) ⚠️ | Nogara | 5 |
| Forêt de Roverè Veronese (29) ⚠️ | Roverè Veronese | 5 |
| Forêt de Roverè Veronese (71) ⚠️ | Roverè Veronese | 5 |
| Parc de Verona (49) ⚠️ | Verona | 5 |
| Forêt de Erbezzo (11) ⚠️ | Erbezzo | 5 |
| Forêt de Erbezzo (17) ⚠️ | Erbezzo | 5 |
| Forêt de Erbezzo (54) ⚠️ | Erbezzo | 5 |
| Forêt de Sant'Anna d'Alfaedo (18) ⚠️ | Sant'Anna d'Alfaedo | 5 |
| Forêt de Sant'Anna d'Alfaedo (45) ⚠️ | Sant'Anna d'Alfaedo | 5 |
| Forêt de Sant'Anna d'Alfaedo (47) ⚠️ | Sant'Anna d'Alfaedo | 5 |
| Forêt de Sant'Anna d'Alfaedo (59) ⚠️ | Sant'Anna d'Alfaedo | 5 |
| Forêt de Sant'Anna d'Alfaedo (87) ⚠️ | Sant'Anna d'Alfaedo | 5 |
| Forêt de Sant'Anna d'Alfaedo (123) ⚠️ | Sant'Anna d'Alfaedo | 5 |
| Forêt de Sant'Anna d'Alfaedo (178) ⚠️ | Sant'Anna d'Alfaedo | 5 |
| Forêt de Sant'Anna d'Alfaedo (249) ⚠️ | Sant'Anna d'Alfaedo | 5 |
| Forêt de Sant'Anna d'Alfaedo (255) ⚠️ | Sant'Anna d'Alfaedo | 5 |
| Forêt de Bosco Chiesanuova (61) ⚠️ | Bosco Chiesanuova | 5 |
| Forêt de Bosco Chiesanuova (91) ⚠️ | Bosco Chiesanuova | 5 |
| Forêt de Bosco Chiesanuova (92) ⚠️ | Bosco Chiesanuova | 5 |
| Forêt de Bosco Chiesanuova (99) ⚠️ | Bosco Chiesanuova | 5 |
| Forêt de Bosco Chiesanuova (104) ⚠️ | Bosco Chiesanuova | 5 |
| Forêt de Bosco Chiesanuova (112) ⚠️ | Bosco Chiesanuova | 5 |
| Forêt de Bosco Chiesanuova (121) ⚠️ | Bosco Chiesanuova | 5 |
| Forêt de Bosco Chiesanuova (293) ⚠️ | Bosco Chiesanuova | 5 |
| Forêt de Bosco Chiesanuova (348) ⚠️ | Bosco Chiesanuova | 5 |
| Forêt de Verona (120) ⚠️ | Verona | 5 |
| Forêt de Verona (144) ⚠️ | Verona | 5 |
| Parco Le Sorgenti del Castello ⚠️ | Castel d'Azzano | 5 |
| Forêt de Verona (310) ⚠️ | Verona | 5 |
| Forêt de Verona (388) ⚠️ | Verona | 5 |
| Forêt de Verona (411) ⚠️ | Verona | 5 |
| Forêt de San Zeno di Montagna (16) ⚠️ | San Zeno di Montagna | 5 |
| Forêt de San Zeno di Montagna (56) ⚠️ | San Zeno di Montagna | 5 |
| Forêt de San Zeno di Montagna (74) ⚠️ | San Zeno di Montagna | 5 |
| Forêt de San Zeno di Montagna (107) ⚠️ | Brenzone sul Garda | 5 |
| Forêt de San Zeno di Montagna (114) ⚠️ | San Zeno di Montagna | 5 |
| Forêt de Caprino Veronese (117) ⚠️ | Caprino Veronese | 5 |
| Forêt de Caprino Veronese (169) ⚠️ | Caprino Veronese | 5 |
| Forêt de Caprino Veronese (255) ⚠️ | Caprino Veronese | 5 |
| Forêt de Ferrara di Monte Baldo (24) ⚠️ | Ferrara di Monte Baldo | 5 |
| Forêt de Ferrara di Monte Baldo (31) ⚠️ | Ferrara di Monte Baldo | 5 |
| Forêt de Ferrara di Monte Baldo (95) ⚠️ | Ferrara di Monte Baldo | 5 |
| Forêt de Fumane (79) ⚠️ | Fumane | 5 |
| Forêt de Malcesine (96) ⚠️ | Malcesine | 5 |
| Forêt de Malcesine (113) ⚠️ | Malcesine | 5 |
| Forêt de Malcesine (128) ⚠️ | Malcesine | 5 |
| Forêt de Fumane (128) ⚠️ | Fumane | 5 |
| Forêt de Dolcè (9) ⚠️ | Dolcè | 5 |
| Forêt de Sant'Ambrogio di Valpolicella (15) ⚠️ | Sant'Ambrogio di Valpolicella | 5 |
| Bois de Valeggio sul Mincio (8) ⚠️ | Valeggio sul Mincio | 5 |
| Forêt de Costermano sul Garda (33) ⚠️ | Costermano sul Garda | 5 |
| Forêt de Cazzano di Tramigna (7) ⚠️ | Cazzano di Tramigna | 5 |
| Forêt de Cazzano di Tramigna (9) ⚠️ | Cazzano di Tramigna | 5 |
| Forêt de Illasi (16) ⚠️ | Illasi | 5 |
| Forêt de Roncà (42) ⚠️ | Roncà | 5 |
| Forêt de Vestenanova (56) ⚠️ | Vestenanova | 5 |
| Forêt de San Giovanni Ilarione (9) ⚠️ | San Giovanni Ilarione | 5 |
| Forêt de Vestenanova (128) ⚠️ | Vestenanova | 5 |
| Forêt de Vestenanova (131) ⚠️ | Vestenanova | 5 |
| Forêt de Vestenanova (169) ⚠️ | Vestenanova | 5 |
| Forêt de Vestenanova (177) ⚠️ | Vestenanova | 5 |
| Forêt de San Giovanni Ilarione (17) ⚠️ | San Giovanni Ilarione | 5 |
| Forêt de San Giovanni Ilarione (125) ⚠️ | San Giovanni Ilarione | 5 |
| Forêt de Selva di Progno (99) ⚠️ | Selva di Progno | 5 |
| Forêt de Selva di Progno (186) ⚠️ | Selva di Progno | 5 |
| Forêt de Selva di Progno (195) ⚠️ | Selva di Progno | 5 |
| Forêt de Selva di Progno (205) ⚠️ | Selva di Progno | 5 |
| Forêt de Montecchia di Crosara (48) ⚠️ | Montecchia di Crosara | 5 |
| Forêt de Roverè Veronese (110) ⚠️ | Roverè Veronese | 5 |
| Forêt de Ronco all'Adige ⚠️ | Ronco all'Adige | 5 |
| Forêt de Badia Calavena (13) ⚠️ | Badia Calavena | 5 |
| Forêt de Badia Calavena (49) ⚠️ | Badia Calavena | 5 |
| Forêt de Tregnago (19) ⚠️ | Tregnago | 5 |
| Forêt de Tregnago (24) ⚠️ | Tregnago | 5 |
| Forêt de Tregnago (41) ⚠️ | Tregnago | 5 |
| Forêt de Tregnago (55) ⚠️ | Tregnago | 5 |
| Bois de Albaredo d'Adige (6) ⚠️ | Albaredo d'Adige | 5 |
| Bois de Ronco all'Adige (3) ⚠️ | Ronco all'Adige | 5 |
| Bois de Ronco all'Adige (9) ⚠️ | Ronco all'Adige | 5 |
| Forêt de San Mauro di Saline (12) ⚠️ | San Mauro di Saline | 5 |
| Bois de San Mauro di Saline (22) ⚠️ | San Mauro di Saline | 5 |
| Bois de San Mauro di Saline (28) ⚠️ | San Mauro di Saline | 5 |
| Bois de Roverè Veronese (28) ⚠️ | Roverè Veronese | 5 |
| Bois de Roverè Veronese (31) ⚠️ | Roverè Veronese | 5 |
| Bois de Negrar di Valpolicella (33) ⚠️ | Negrar di Valpolicella | 5 |
| Forêt de Affi (19) ⚠️ | Affi | 5 |
| Forêt de Bosco Chiesanuova (378) ⚠️ | Bosco Chiesanuova | 5 |
| Forêt de Verona (449) ⚠️ | Verona | 5 |
| Forêt de San Zeno di Montagna (224) ⚠️ | San Zeno di Montagna | 5 |
| Forêt de Malcesine (152) ⚠️ | Malcesine | 5 |
| Forêt de San Giovanni Ilarione (175) ⚠️ | San Giovanni Ilarione | 5 |
| Forêt de San Giovanni Ilarione (176) ⚠️ | San Giovanni Ilarione | 5 |
| Forêt de San Giovanni Ilarione (181) ⚠️ | San Giovanni Ilarione | 5 |
| Forêt de Montecchia di Crosara (94) ⚠️ | Montecchia di Crosara | 5 |
| Forêt de Montecchia di Crosara (95) ⚠️ | Montecchia di Crosara | 5 |
| Bois de Rivoli Veronese (6) ⚠️ | Rivoli Veronese | 5 |
| Forêt de Tregnago (194) ⚠️ | Tregnago | 5 |
| Nuovo Parco San Giacomo ⚠️ | Verona | 4 |
| Parco Villa Pullè ⚠️ | Verona | 4 |
| Bois de Monteforte d'Alpone ⚠️ | Monteforte d'Alpone | 4 |
| Bois de Villa Bartolomea (4) ⚠️ | Villa Bartolomea | 4 |
| Forêt de Cerro Veronese ⚠️ | Cerro Veronese | 4 |
| Forêt de Cerro Veronese (5) ⚠️ | Cerro Veronese | 4 |
| Forêt de Grezzana (9) ⚠️ | Grezzana | 4 |
| Forêt de Negrar di Valpolicella (10) ⚠️ | Negrar di Valpolicella | 4 |
| Forêt de Cerro Veronese (13) ⚠️ | Cerro Veronese | 4 |
| Forêt de Grezzana (47) ⚠️ | Grezzana | 4 |
| Forêt de Cerro Veronese (19) ⚠️ | Cerro Veronese | 4 |
| Forêt de Cerro Veronese (22) ⚠️ | Cerro Veronese | 4 |
| Forêt de Negrar di Valpolicella (31) ⚠️ | Negrar di Valpolicella | 4 |
| Forêt de Negrar di Valpolicella (36) ⚠️ | Negrar di Valpolicella | 4 |
| Forêt de Rivoli Veronese ⚠️ | Rivoli Veronese | 4 |
| Forêt de Marano di Valpolicella (2) ⚠️ | Marano di Valpolicella | 4 |
| Forêt de Negrar di Valpolicella (46) ⚠️ | Negrar di Valpolicella | 4 |
| Forêt de Negrar di Valpolicella (58) ⚠️ | Negrar di Valpolicella | 4 |
| Forêt de Rivoli Veronese (3) ⚠️ | Rivoli Veronese | 4 |
| Forêt de Cavaion Veronese (4) ⚠️ | Cavaion Veronese | 4 |
| Forêt de Affi (10) ⚠️ | Affi | 4 |
| Parco dei Tigli ⚠️ | Legnago | 4 |
| Forêt de Roverè Veronese (26) ⚠️ | Roverè Veronese | 4 |
| Forêt de Erbezzo (23) ⚠️ | Erbezzo | 4 |
| Forêt de Erbezzo (29) ⚠️ | Erbezzo | 4 |
| Forêt de Erbezzo (113) ⚠️ | Erbezzo | 4 |
| Forêt de Erbezzo (179) ⚠️ | Erbezzo | 4 |
| Forêt de Erbezzo (184) ⚠️ | Erbezzo | 4 |
| Forêt de Erbezzo (194) ⚠️ | Erbezzo | 4 |
| Forêt de Sant'Anna d'Alfaedo (16) ⚠️ | Sant'Anna d'Alfaedo | 4 |
| Forêt de Sant'Anna d'Alfaedo (19) ⚠️ | Sant'Anna d'Alfaedo | 4 |
| Forêt de Sant'Anna d'Alfaedo (30) ⚠️ | Sant'Anna d'Alfaedo | 4 |
| Forêt de Sant'Anna d'Alfaedo (37) ⚠️ | Sant'Anna d'Alfaedo | 4 |
| Forêt de Sant'Anna d'Alfaedo (43) ⚠️ | Sant'Anna d'Alfaedo | 4 |
| Forêt de Sant'Anna d'Alfaedo (46) ⚠️ | Sant'Anna d'Alfaedo | 4 |
| Forêt de Sant'Anna d'Alfaedo (52) ⚠️ | Sant'Anna d'Alfaedo | 4 |
| Forêt de Sant'Anna d'Alfaedo (185) ⚠️ | Sant'Anna d'Alfaedo | 4 |
| Forêt de Sant'Anna d'Alfaedo (239) ⚠️ | Sant'Anna d'Alfaedo | 4 |
| Forêt de Bosco Chiesanuova (42) ⚠️ | Bosco Chiesanuova | 4 |
| Forêt de Bosco Chiesanuova (68) ⚠️ | Bosco Chiesanuova | 4 |
| Forêt de Bosco Chiesanuova (290) ⚠️ | Bosco Chiesanuova | 4 |
| Forêt de Bosco Chiesanuova (332) ⚠️ | Bosco Chiesanuova | 4 |
| Bois de Verona (2) ⚠️ | Verona | 4 |
| Forêt de Verona (39) ⚠️ | Verona | 4 |
| Forêt de Verona (69) ⚠️ | Verona | 4 |
| Forêt de Verona (83) ⚠️ | Verona | 4 |
| Forêt de Verona (88) ⚠️ | Verona | 4 |
| Parc de Verona (67) ⚠️ | Verona | 4 |
| Forêt de Verona (106) ⚠️ | Verona | 4 |
| Forêt de Verona (107) ⚠️ | Verona | 4 |
| Forêt de Verona (108) ⚠️ | Verona | 4 |
| Forêt de Verona (121) ⚠️ | Verona | 4 |
| Forêt de Verona (221) ⚠️ | Verona | 4 |
| Forêt de Velo Veronese (30) ⚠️ | Velo Veronese | 4 |
| Forêt de Verona (363) ⚠️ | Verona | 4 |
| Forêt de Verona (379) ⚠️ | Verona | 4 |
| Forêt de Malcesine (18) ⚠️ | Malcesine | 4 |
| Forêt de San Zeno di Montagna (9) ⚠️ | San Zeno di Montagna | 4 |
| Forêt de San Zeno di Montagna (40) ⚠️ | San Zeno di Montagna | 4 |
| Forêt de San Zeno di Montagna (80) ⚠️ | San Zeno di Montagna | 4 |
| Forêt de Caprino Veronese (85) ⚠️ | Caprino Veronese | 4 |
| Forêt de Caprino Veronese (140) ⚠️ | Caprino Veronese | 4 |
| Forêt de Caprino Veronese (164) ⚠️ | Caprino Veronese | 4 |
| Forêt de Caprino Veronese (170) ⚠️ | Caprino Veronese | 4 |
| Forêt de Caprino Veronese (235) ⚠️ | Caprino Veronese | 4 |
| Forêt de Caprino Veronese (267) ⚠️ | Caprino Veronese | 4 |
| Forêt de Caprino Veronese (268) ⚠️ | Caprino Veronese | 4 |
| Forêt de Brenzone sul Garda (48) ⚠️ | Brenzone sul Garda | 4 |
| Forêt de Ferrara di Monte Baldo (53) ⚠️ | Ferrara di Monte Baldo | 4 |
| Forêt de Brentino Belluno (31) ⚠️ | Brentino Belluno | 4 |
| Forêt de Brentino Belluno (56) ⚠️ | Brentino Belluno | 4 |
| Forêt de Fumane (60) ⚠️ | Fumane | 4 |
| Forêt de Malcesine (40) ⚠️ | Malcesine | 4 |
| Forêt de Malcesine (43) ⚠️ | Malcesine | 4 |
| Forêt de Malcesine (59) ⚠️ | Malcesine | 4 |
| Forêt de Malcesine (71) ⚠️ | Malcesine | 4 |
| Forêt de Malcesine (74) ⚠️ | Malcesine | 4 |
| Forêt de Malcesine (86) ⚠️ | Malcesine | 4 |
| Forêt de Malcesine (119) ⚠️ | Malcesine | 4 |
| Forêt de Malcesine (141) ⚠️ | Malcesine | 4 |
| Forêt de Fumane (99) ⚠️ | Fumane | 4 |
| Forêt de Fumane (115) ⚠️ | Fumane | 4 |
| Forêt de Fumane (154) ⚠️ | Fumane | 4 |
| Forêt de Dolcè (15) ⚠️ | Dolcè | 4 |
| Forêt de Dolcè (51) ⚠️ | Dolcè | 4 |
| Forêt de Fumane (166) ⚠️ | Fumane | 4 |
| Forêt de Marano di Valpolicella (34) ⚠️ | Marano di Valpolicella | 4 |
| Forêt de Costermano sul Garda (22) ⚠️ | Costermano sul Garda | 4 |
| Forêt de Caprino Veronese (298) ⚠️ | Caprino Veronese | 4 |
| Forêt de Caprino Veronese (334) ⚠️ | Caprino Veronese | 4 |
| Forêt de Costermano sul Garda (43) ⚠️ | Costermano sul Garda | 4 |
| Forêt de Cerea (8) ⚠️ | Cerea | 4 |
| Forêt de Illasi (4) ⚠️ | Illasi | 4 |
| Forêt de Illasi (12) ⚠️ | Illasi | 4 |
| Forêt de Cazzano di Tramigna (2) ⚠️ | Cazzano di Tramigna | 4 |
| Forêt de Cazzano di Tramigna (8) ⚠️ | Cazzano di Tramigna | 4 |
| Forêt de Cazzano di Tramigna (13) ⚠️ | Cazzano di Tramigna | 4 |
| Forêt de Cazzano di Tramigna (19) ⚠️ | Cazzano di Tramigna | 4 |
| Forêt de Illasi (18) ⚠️ | Illasi | 4 |
| Forêt de Villa Bartolomea ⚠️ | Villa Bartolomea | 4 |
| Forêt de Grezzana (95) ⚠️ | Grezzana | 4 |
| Forêt de Velo Veronese (34) ⚠️ | Velo Veronese | 4 |
| Forêt de Velo Veronese (39) ⚠️ | Velo Veronese | 4 |
| Forêt de Roncà (21) ⚠️ | Roncà | 4 |
| Forêt de Roncà (32) ⚠️ | Roncà | 4 |
| Forêt de Roncà (54) ⚠️ | Roncà | 4 |
| Forêt de Roncà (93) ⚠️ | Roncà | 4 |
| Forêt de Roncà (120) ⚠️ | Roncà | 4 |
| Forêt de Vestenanova (151) ⚠️ | Vestenanova | 4 |
| Forêt de Vestenanova (184) ⚠️ | Vestenanova | 4 |
| Forêt de Vestenanova (199) ⚠️ | Vestenanova | 4 |
| Forêt de Vestenanova (208) ⚠️ | Vestenanova | 4 |
| Bois de Negrar di Valpolicella (7) ⚠️ | Negrar di Valpolicella | 4 |
| Forêt de San Giovanni Ilarione (48) ⚠️ | San Giovanni Ilarione | 4 |
| Forêt de San Giovanni Ilarione (51) ⚠️ | San Giovanni Ilarione | 4 |
| Forêt de San Giovanni Ilarione (60) ⚠️ | San Giovanni Ilarione | 4 |
| Forêt de San Giovanni Ilarione (131) ⚠️ | San Giovanni Ilarione | 4 |
| Forêt de San Giovanni Ilarione (144) ⚠️ | San Giovanni Ilarione | 4 |
| Forêt de Selva di Progno (7) ⚠️ | Selva di Progno | 4 |
| Forêt de Selva di Progno (63) ⚠️ | Selva di Progno | 4 |
| Forêt de Selva di Progno (68) ⚠️ | Selva di Progno | 4 |
| Forêt de Selva di Progno (72) ⚠️ | Selva di Progno | 4 |
| Forêt de Velo Veronese (48) ⚠️ | Roverè Veronese | 4 |
| Forêt de Roverè Veronese (97) ⚠️ | Roverè Veronese | 4 |
| Forêt de Montecchia di Crosara (10) ⚠️ | Montecchia di Crosara | 4 |
| Forêt de Montecchia di Crosara (57) ⚠️ | Montecchia di Crosara | 4 |
| Forêt de Montecchia di Crosara (58) ⚠️ | Montecchia di Crosara | 4 |
| Forêt de Montecchia di Crosara (72) ⚠️ | Montecchia di Crosara | 4 |
| Forêt de Montecchia di Crosara (86) ⚠️ | Montecchia di Crosara | 4 |
| Forêt de Roverè Veronese (117) ⚠️ | Roverè Veronese | 4 |
| Bois de Rivoli Veronese (3) ⚠️ | Rivoli Veronese | 4 |
| Bois de Zevio ⚠️ | Zevio | 4 |
| Bois de Albaredo d'Adige (2) ⚠️ | Albaredo d'Adige | 4 |
| Forêt de Grezzana (105) ⚠️ | Grezzana | 4 |
| Forêt de Badia Calavena (23) ⚠️ | Badia Calavena | 4 |
| Forêt de Badia Calavena (65) ⚠️ | Badia Calavena | 4 |
| Forêt de Badia Calavena (79) ⚠️ | Badia Calavena | 4 |
| Forêt de Badia Calavena (80) ⚠️ | Badia Calavena | 4 |
| Forêt de Badia Calavena (87) ⚠️ | Badia Calavena | 4 |
| Forêt de Badia Calavena (89) ⚠️ | Badia Calavena | 4 |
| Forêt de Tregnago (46) ⚠️ | Tregnago | 4 |
| Forêt de Tregnago (92) ⚠️ | Tregnago | 4 |
| Forêt de Tregnago (112) ⚠️ | Tregnago | 4 |
| Bois de Angiari (3) ⚠️ | Angiari | 4 |
| Forêt de Sorgà (9) ⚠️ | Sorgà | 4 |
| Bois de San Mauro di Saline (10) ⚠️ | San Mauro di Saline | 4 |
| Bois de San Mauro di Saline (29) ⚠️ | San Mauro di Saline | 4 |
| Forêt de Negrar di Valpolicella (77) ⚠️ | Negrar di Valpolicella | 4 |
| Bois de Negrar di Valpolicella (23) ⚠️ | Negrar di Valpolicella | 4 |
| Bois de Mezzane di Sotto (25) ⚠️ | Mezzane di Sotto | 4 |
| Bois de Mezzane di Sotto (30) ⚠️ | Mezzane di Sotto | 4 |
| Bois de Roverè Veronese (37) ⚠️ | Roverè Veronese | 4 |
| Bois de Grezzana (60) ⚠️ | Grezzana | 4 |
| Bois de Grezzana (65) ⚠️ | Grezzana | 4 |
| Forêt de Erbezzo (202) ⚠️ | Erbezzo | 4 |
| Forêt de Erbezzo (203) ⚠️ | Erbezzo | 4 |
| Forêt de Sant'Anna d'Alfaedo (265) ⚠️ | Sant'Anna d'Alfaedo | 4 |
| Forêt de Bosco Chiesanuova (380) ⚠️ | Bosco Chiesanuova | 4 |
| Forêt de Verona (454) ⚠️ | Verona | 4 |
| Forêt de Verona (455) ⚠️ | Verona | 4 |
| Forêt de Brenzone sul Garda (76) ⚠️ | Brenzone sul Garda | 4 |
| Forêt de Fumane (207) ⚠️ | Fumane | 4 |
| Forêt de San Giovanni Ilarione (178) ⚠️ | San Giovanni Ilarione | 4 |
| Forêt de Brentino Belluno (95) ⚠️ | Brentino Belluno | 4 |
| Parco delle Mura ⚠️ | Verona | 3 |
| Parco delle Mura (2) ⚠️ | Verona | 3 |
| Parco delle Mura (3) ⚠️ | Verona | 3 |
| Parc de Verona (12) ⚠️ | Verona | 3 |
| Parco Maggiolino ⚠️ | Verona | 3 |
| Lazzaretto ⚠️ | Verona | 3 |
| Forêt de Verona (2) ⚠️ | Verona | 3 |
| Forêt de Mezzane di Sotto (3) ⚠️ | Mezzane di Sotto | 3 |
| Forêt de Mezzane di Sotto (26) ⚠️ | Mezzane di Sotto | 3 |
| Forêt de Cerro Veronese (4) ⚠️ | Cerro Veronese | 3 |
| Forêt de Negrar di Valpolicella (8) ⚠️ | Negrar di Valpolicella | 3 |
| Forêt de Grezzana (20) ⚠️ | Grezzana | 3 |
| Forêt de Grezzana (34) ⚠️ | Grezzana | 3 |
| Forêt de Grezzana (41) ⚠️ | Grezzana | 3 |
| Forêt de Negrar di Valpolicella (16) ⚠️ | Negrar di Valpolicella | 3 |
| Forêt de Grezzana (48) ⚠️ | Grezzana | 3 |
| Forêt de Grezzana (67) ⚠️ | Grezzana | 3 |
| Forêt de Grezzana (71) ⚠️ | Grezzana | 3 |
| Bois de San Giovanni Lupatoto (2) ⚠️ | San Giovanni Lupatoto | 3 |
| Forêt de San Martino Buon Albergo (10) ⚠️ | San Martino Buon Albergo | 3 |
| Forêt de San Martino Buon Albergo (24) ⚠️ | San Martino Buon Albergo | 3 |
| Forêt de San Martino Buon Albergo (28) ⚠️ | San Martino Buon Albergo | 3 |
| Forêt de Negrar di Valpolicella (38) ⚠️ | Negrar di Valpolicella | 3 |
| Forêt de Sommacampagna (2) ⚠️ | Sommacampagna | 3 |
| Forêt de Negrar di Valpolicella (54) ⚠️ | Negrar di Valpolicella | 3 |
| Forêt de Negrar di Valpolicella (56) ⚠️ | Negrar di Valpolicella | 3 |
| Forêt de Negrar di Valpolicella (57) ⚠️ | Negrar di Valpolicella | 3 |
| Forêt de Velo Veronese (4) ⚠️ | Velo Veronese | 3 |
| Forêt de Roverè Veronese (21) ⚠️ | Roverè Veronese | 3 |
| Forêt de Rivoli Veronese (5) ⚠️ | Rivoli Veronese | 3 |
| Forêt de Rivoli Veronese (10) ⚠️ | Rivoli Veronese | 3 |
| Forêt de Lazise ⚠️ | Lazise | 3 |
| Forêt de Valeggio sul Mincio (21) ⚠️ | Valeggio sul Mincio | 3 |
| Forêt de Sona (13) ⚠️ | Sona | 3 |
| Forêt de Isola della Scala (4) ⚠️ | Isola della Scala | 3 |
| Forêt de Isola della Scala (8) ⚠️ | Isola della Scala | 3 |
| Forêt de Isola della Scala (9) ⚠️ | Isola della Scala | 3 |
| Forêt de Isola della Scala (12) ⚠️ | Isola della Scala | 3 |
| Forêt de Nogara (7) ⚠️ | Nogara | 3 |
| Forêt de Roverè Veronese (30) ⚠️ | Roverè Veronese | 3 |
| Forêt de Roverè Veronese (33) ⚠️ | Roverè Veronese | 3 |
| Forêt de Roverè Veronese (41) ⚠️ | Roverè Veronese | 3 |
| Forêt de Velo Veronese (20) ⚠️ | Velo Veronese | 3 |
| Forêt de Erbezzo (5) ⚠️ | Erbezzo | 3 |
| Forêt de Erbezzo (7) ⚠️ | Erbezzo | 3 |
| Forêt de Erbezzo (8) ⚠️ | Erbezzo | 3 |
| Forêt de Erbezzo (16) ⚠️ | Erbezzo | 3 |
| Forêt de Erbezzo (49) ⚠️ | Erbezzo | 3 |
| Forêt de Erbezzo (97) ⚠️ | Erbezzo | 3 |
| Forêt de Erbezzo (103) ⚠️ | Erbezzo | 3 |
| Forêt de Erbezzo (125) ⚠️ | Erbezzo | 3 |
| Forêt de Erbezzo (153) ⚠️ | Erbezzo | 3 |
| Forêt de Erbezzo (181) ⚠️ | Erbezzo | 3 |
| Forêt de Erbezzo (192) ⚠️ | Erbezzo | 3 |
| Forêt de Sant'Anna d'Alfaedo (8) ⚠️ | Sant'Anna d'Alfaedo | 3 |
| Forêt de Sant'Anna d'Alfaedo (9) ⚠️ | Sant'Anna d'Alfaedo | 3 |
| Forêt de Sant'Anna d'Alfaedo (31) ⚠️ | Sant'Anna d'Alfaedo | 3 |
| Forêt de Sant'Anna d'Alfaedo (33) ⚠️ | Sant'Anna d'Alfaedo | 3 |
| Forêt de Sant'Anna d'Alfaedo (38) ⚠️ | Sant'Anna d'Alfaedo | 3 |
| Forêt de Sant'Anna d'Alfaedo (44) ⚠️ | Sant'Anna d'Alfaedo | 3 |
| Forêt de Sant'Anna d'Alfaedo (50) ⚠️ | Sant'Anna d'Alfaedo | 3 |
| Forêt de Sant'Anna d'Alfaedo (53) ⚠️ | Sant'Anna d'Alfaedo | 3 |
| Forêt de Sant'Anna d'Alfaedo (131) ⚠️ | Sant'Anna d'Alfaedo | 3 |
| Forêt de Sant'Anna d'Alfaedo (134) ⚠️ | Sant'Anna d'Alfaedo | 3 |
| Forêt de Marano di Valpolicella (21) ⚠️ | Marano di Valpolicella | 3 |
| Forêt de Sant'Anna d'Alfaedo (194) ⚠️ | Sant'Anna d'Alfaedo | 3 |
| Forêt de Sant'Anna d'Alfaedo (231) ⚠️ | Sant'Anna d'Alfaedo | 3 |
| Forêt de Sant'Anna d'Alfaedo (243) ⚠️ | Sant'Anna d'Alfaedo | 3 |
| Forêt de Sant'Anna d'Alfaedo (244) ⚠️ | Sant'Anna d'Alfaedo | 3 |
| Forêt de Sant'Anna d'Alfaedo (248) ⚠️ | Sant'Anna d'Alfaedo | 3 |
| Forêt de Bosco Chiesanuova (6) ⚠️ | Bosco Chiesanuova | 3 |
| Forêt de Bosco Chiesanuova (11) ⚠️ | Bosco Chiesanuova | 3 |
| Forêt de Bosco Chiesanuova (25) ⚠️ | Bosco Chiesanuova | 3 |
| Forêt de Bosco Chiesanuova (28) ⚠️ | Bosco Chiesanuova | 3 |
| Forêt de Bosco Chiesanuova (34) ⚠️ | Bosco Chiesanuova | 3 |
| Forêt de Bosco Chiesanuova (35) ⚠️ | Bosco Chiesanuova | 3 |
| Forêt de Bosco Chiesanuova (44) ⚠️ | Bosco Chiesanuova | 3 |
| Forêt de Bosco Chiesanuova (46) ⚠️ | Bosco Chiesanuova | 3 |
| Forêt de Bosco Chiesanuova (67) ⚠️ | Bosco Chiesanuova | 3 |
| Forêt de Bosco Chiesanuova (74) ⚠️ | Bosco Chiesanuova | 3 |
| Forêt de Bosco Chiesanuova (77) ⚠️ | Bosco Chiesanuova | 3 |
| Forêt de Bosco Chiesanuova (83) ⚠️ | Bosco Chiesanuova | 3 |
| Forêt de Bosco Chiesanuova (106) ⚠️ | Bosco Chiesanuova | 3 |
| Forêt de Bosco Chiesanuova (276) ⚠️ | Bosco Chiesanuova | 3 |
| Forêt de Bosco Chiesanuova (331) ⚠️ | Bosco Chiesanuova | 3 |
| Forêt de Bosco Chiesanuova (343) ⚠️ | Bosco Chiesanuova | 3 |
| Forêt de Bosco Chiesanuova (349) ⚠️ | Bosco Chiesanuova | 3 |
| Forêt de Bosco Chiesanuova (356) ⚠️ | Bosco Chiesanuova | 3 |
| Bois de Verona (3) ⚠️ | Verona | 3 |
| Forêt de Verona (49) ⚠️ | Verona | 3 |
| Forêt de Verona (155) ⚠️ | Verona | 3 |
| Parco della risorgiva Fossa Bova ⚠️ | Verona | 3 |
| Forêt de Verona (207) ⚠️ | Verona | 3 |
| Forêt de Verona (282) ⚠️ | Verona | 3 |
| Forêt de Verona (344) ⚠️ | Verona | 3 |
| Forêt de Verona (352) ⚠️ | Verona | 3 |
| Forêt de Verona (372) ⚠️ | Verona | 3 |
| Forêt de Verona (393) ⚠️ | Verona | 3 |
| Forêt de Verona (401) ⚠️ | Verona | 3 |
| Forêt de Verona (429) ⚠️ | Verona | 3 |
| Forêt de Cerea (4) ⚠️ | Cerea | 3 |
| Forêt de Malcesine (13) ⚠️ | Malcesine | 3 |
| Forêt de Torri del Benaco (15) ⚠️ | Torri del Benaco | 3 |
| Forêt de Torri del Benaco (26) ⚠️ | Torri del Benaco | 3 |
| Forêt de San Zeno di Montagna (59) ⚠️ | San Zeno di Montagna | 3 |
| Forêt de San Zeno di Montagna (72) ⚠️ | San Zeno di Montagna | 3 |
| Forêt de San Zeno di Montagna (79) ⚠️ | San Zeno di Montagna | 3 |
| Forêt de Caprino Veronese (2) ⚠️ | Caprino Veronese | 3 |
| Forêt de Caprino Veronese (56) ⚠️ | Caprino Veronese | 3 |
| Forêt de Caprino Veronese (61) ⚠️ | Caprino Veronese | 3 |
| Forêt de Caprino Veronese (76) ⚠️ | Caprino Veronese | 3 |
| Forêt de Caprino Veronese (98) ⚠️ | Caprino Veronese | 3 |
| Forêt de Caprino Veronese (105) ⚠️ | Caprino Veronese | 3 |
| Forêt de Caprino Veronese (106) ⚠️ | Caprino Veronese | 3 |
| Forêt de Caprino Veronese (135) ⚠️ | Caprino Veronese | 3 |
| Forêt de Caprino Veronese (162) ⚠️ | Caprino Veronese | 3 |
| Forêt de Ferrara di Monte Baldo (4) ⚠️ | Caprino Veronese | 3 |
| Forêt de Caprino Veronese (172) ⚠️ | Caprino Veronese | 3 |
| Forêt de Caprino Veronese (182) ⚠️ | Caprino Veronese | 3 |
| Forêt de Caprino Veronese (198) ⚠️ | Caprino Veronese | 3 |
| Forêt de Caprino Veronese (205) ⚠️ | Caprino Veronese | 3 |
| Forêt de Brenzone sul Garda (11) ⚠️ | Brenzone sul Garda | 3 |
| Forêt de Brenzone sul Garda (14) ⚠️ | Brenzone sul Garda | 3 |
| Forêt de Brenzone sul Garda (32) ⚠️ | Brenzone sul Garda | 3 |
| Forêt de Brenzone sul Garda (53) ⚠️ | Brenzone sul Garda | 3 |
| Forêt de Ferrara di Monte Baldo (10) ⚠️ | Ferrara di Monte Baldo | 3 |
| Forêt de Ferrara di Monte Baldo (32) ⚠️ | Ferrara di Monte Baldo | 3 |
| Forêt de Ferrara di Monte Baldo (38) ⚠️ | Ferrara di Monte Baldo | 3 |
| Forêt de Ferrara di Monte Baldo (49) ⚠️ | Ferrara di Monte Baldo | 3 |
| Forêt de Ferrara di Monte Baldo (60) ⚠️ | Ferrara di Monte Baldo | 3 |
| Forêt de Ferrara di Monte Baldo (62) ⚠️ | Ferrara di Monte Baldo | 3 |
| Forêt de Ferrara di Monte Baldo (65) ⚠️ | Ferrara di Monte Baldo | 3 |
| Forêt de Ferrara di Monte Baldo (67) ⚠️ | Ferrara di Monte Baldo | 3 |
| Forêt de Ferrara di Monte Baldo (97) ⚠️ | Ferrara di Monte Baldo | 3 |
| Forêt de Fumane (33) ⚠️ | Fumane | 3 |
| Forêt de Fumane (40) ⚠️ | Fumane | 3 |
| Forêt de Brentino Belluno (45) ⚠️ | Brentino Belluno | 3 |
| Forêt de Brentino Belluno (62) ⚠️ | Brentino Belluno | 3 |
| Forêt de Brentino Belluno (63) ⚠️ | Brentino Belluno | 3 |
| Forêt de Brentino Belluno (64) ⚠️ | Brentino Belluno | 3 |
| Forêt de Fumane (59) ⚠️ | Fumane | 3 |
| Forêt de Fumane (74) ⚠️ | Fumane | 3 |
| Forêt de Fumane (82) ⚠️ | Fumane | 3 |
| Forêt de Malcesine (68) ⚠️ | Malcesine | 3 |
| Forêt de Malcesine (69) ⚠️ | Malcesine | 3 |
| Forêt de Malcesine (75) ⚠️ | Malcesine | 3 |
| Forêt de Malcesine (85) ⚠️ | Malcesine | 3 |
| Forêt de Malcesine (87) ⚠️ | Malcesine | 3 |
| Forêt de Malcesine (104) ⚠️ | Malcesine | 3 |
| Forêt de Malcesine (105) ⚠️ | Malcesine | 3 |
| Forêt de Malcesine (112) ⚠️ | Malcesine | 3 |
| Forêt de Malcesine (120) ⚠️ | Malcesine | 3 |
| Forêt de Malcesine (136) ⚠️ | Malcesine | 3 |
| Forêt de Malcesine (138) ⚠️ | Malcesine | 3 |
| Forêt de Malcesine (139) ⚠️ | Malcesine | 3 |
| Forêt de Malcesine (140) ⚠️ | Malcesine | 3 |
| Forêt de Fumane (102) ⚠️ | Fumane | 3 |
| Forêt de Fumane (105) ⚠️ | Fumane | 3 |
| Forêt de Lazise (12) ⚠️ | Lazise | 3 |
| Forêt de Fumane (148) ⚠️ | Fumane | 3 |
| Forêt de Fumane (156) ⚠️ | Fumane | 3 |
| Forêt de San Zeno di Montagna (120) ⚠️ | San Zeno di Montagna | 3 |
| Forêt de Dolcè (36) ⚠️ | Dolcè | 3 |
| Bois de Valeggio sul Mincio (7) ⚠️ | Valeggio sul Mincio | 3 |
| Forêt de Costermano sul Garda (7) ⚠️ | Costermano sul Garda | 3 |
| Forêt de Costermano sul Garda (18) ⚠️ | Costermano sul Garda | 3 |
| Forêt de Caprino Veronese (331) ⚠️ | Caprino Veronese | 3 |
| Forêt de Brenzone sul Garda (62) ⚠️ | Brenzone sul Garda | 3 |
| Forêt de Roverè Veronese (78) ⚠️ | Roverè Veronese | 3 |
| Parc de San Bonifacio (3) ⚠️ | San Bonifacio | 3 |
| Forêt de Rivoli Veronese (24) ⚠️ | Rivoli Veronese | 3 |
| Forêt de Peschiera del Garda ⚠️ | Peschiera del Garda | 3 |
| Forêt de Peschiera del Garda (2) ⚠️ | Peschiera del Garda | 3 |
| Forêt de Cerro Veronese (28) ⚠️ | Cerro Veronese | 3 |
| Forêt de Cazzano di Tramigna ⚠️ | Cazzano di Tramigna | 3 |
| Forêt de Vestenanova (4) ⚠️ | Vestenanova | 3 |
| Forêt de Soave (15) ⚠️ | Soave | 3 |
| Forêt de Villa Bartolomea (2) ⚠️ | Villa Bartolomea | 3 |
| Forêt de Caldiero ⚠️ | Caldiero | 3 |
| Forêt de Velo Veronese (38) ⚠️ | Velo Veronese | 3 |
| Forêt de Soave (23) ⚠️ | Soave | 3 |
| Forêt de Roncà (16) ⚠️ | Roncà | 3 |
| Forêt de Montecchia di Crosara ⚠️ | Montecchia di Crosara | 3 |
| Forêt de Roncà (64) ⚠️ | Roncà | 3 |
| Forêt de Roncà (88) ⚠️ | Roncà | 3 |
| Forêt de Roncà (125) ⚠️ | Roncà | 3 |
| Forêt de Vestenanova (42) ⚠️ | Vestenanova | 3 |
| Forêt de Vestenanova (45) ⚠️ | Vestenanova | 3 |
| Forêt de Vestenanova (49) ⚠️ | Vestenanova | 3 |
| Forêt de Vestenanova (66) ⚠️ | Vestenanova | 3 |
| Forêt de Vestenanova (69) ⚠️ | Vestenanova | 3 |
| Forêt de Vestenanova (82) ⚠️ | Vestenanova | 3 |
| Forêt de Vestenanova (85) ⚠️ | Vestenanova | 3 |
| Forêt de Vestenanova (86) ⚠️ | Vestenanova | 3 |
| Forêt de Vestenanova (104) ⚠️ | Vestenanova | 3 |
| Forêt de Vestenanova (122) ⚠️ | Vestenanova | 3 |
| Forêt de Vestenanova (181) ⚠️ | Vestenanova | 3 |
| Forêt de Vestenanova (203) ⚠️ | Vestenanova | 3 |
| Forêt de Vestenanova (212) ⚠️ | Vestenanova | 3 |
| Bois de Pastrengo (2) ⚠️ | Pastrengo | 3 |
| Bois de Bussolengo ⚠️ | Bussolengo | 3 |
| Forêt de San Giovanni Ilarione (19) ⚠️ | San Giovanni Ilarione | 3 |
| Forêt de San Giovanni Ilarione (26) ⚠️ | San Giovanni Ilarione | 3 |
| Forêt de San Giovanni Ilarione (33) ⚠️ | San Giovanni Ilarione | 3 |
| Forêt de San Giovanni Ilarione (37) ⚠️ | San Giovanni Ilarione | 3 |
| Forêt de San Giovanni Ilarione (53) ⚠️ | San Giovanni Ilarione | 3 |
| Forêt de San Giovanni Ilarione (59) ⚠️ | San Giovanni Ilarione | 3 |
| Forêt de San Giovanni Ilarione (62) ⚠️ | San Giovanni Ilarione | 3 |
| Forêt de San Giovanni Ilarione (64) ⚠️ | San Giovanni Ilarione | 3 |
| Forêt de San Giovanni Ilarione (69) ⚠️ | San Giovanni Ilarione | 3 |
| Forêt de San Giovanni Ilarione (78) ⚠️ | San Giovanni Ilarione | 3 |
| Forêt de Selva di Progno (12) ⚠️ | Selva di Progno | 3 |
| Forêt de Selva di Progno (22) ⚠️ | Selva di Progno | 3 |
| Forêt de Selva di Progno (38) ⚠️ | Selva di Progno | 3 |
| Forêt de Selva di Progno (101) ⚠️ | Selva di Progno | 3 |
| Forêt de Selva di Progno (108) ⚠️ | Selva di Progno | 3 |
| Forêt de Selva di Progno (112) ⚠️ | Selva di Progno | 3 |
| Forêt de Selva di Progno (113) ⚠️ | Selva di Progno | 3 |
| Forêt de Selva di Progno (131) ⚠️ | Selva di Progno | 3 |
| Forêt de Selva di Progno (147) ⚠️ | Selva di Progno | 3 |
| Forêt de Selva di Progno (174) ⚠️ | Selva di Progno | 3 |
| Forêt de Selva di Progno (182) ⚠️ | Selva di Progno | 3 |
| Forêt de Selva di Progno (185) ⚠️ | Selva di Progno | 3 |
| Forêt de Selva di Progno (204) ⚠️ | Selva di Progno | 3 |
| Forêt de Selva di Progno (212) ⚠️ | Selva di Progno | 3 |
| Forêt de Roverè Veronese (95) ⚠️ | Velo Veronese | 3 |
| Forêt de Roverè Veronese (98) ⚠️ | Roverè Veronese | 3 |
| Forêt de Montecchia di Crosara (21) ⚠️ | Montecchia di Crosara | 3 |
| Forêt de Rivoli Veronese (28) ⚠️ | Rivoli Veronese | 3 |
| Forêt de Bussolengo (28) ⚠️ | Bussolengo | 3 |
| Parc de Castelnuovo del Garda (13) ⚠️ | Castelnuovo del Garda | 3 |
| Forêt de Marano di Valpolicella (39) ⚠️ | Marano di Valpolicella | 3 |
| Bois de Roverè Veronese (2) ⚠️ | Roverè Veronese | 3 |
| Forêt de Badia Calavena (43) ⚠️ | Badia Calavena | 3 |
| Forêt de Badia Calavena (44) ⚠️ | Badia Calavena | 3 |
| Forêt de Badia Calavena (46) ⚠️ | Badia Calavena | 3 |
| Forêt de Badia Calavena (102) ⚠️ | Badia Calavena | 3 |
| Forêt de Badia Calavena (136) ⚠️ | Badia Calavena | 3 |
| Forêt de Tregnago (31) ⚠️ | Tregnago | 3 |
| Forêt de Tregnago (50) ⚠️ | Tregnago | 3 |
| Forêt de Tregnago (51) ⚠️ | Tregnago | 3 |
| Forêt de Tregnago (67) ⚠️ | Tregnago | 3 |
| Forêt de Tregnago (72) ⚠️ | Tregnago | 3 |
| Forêt de Tregnago (78) ⚠️ | Tregnago | 3 |
| Forêt de Tregnago (89) ⚠️ | Tregnago | 3 |
| Forêt de Tregnago (105) ⚠️ | Tregnago | 3 |
| Forêt de Tregnago (175) ⚠️ | Tregnago | 3 |
| Bois de Lazise (76) ⚠️ | Lazise | 3 |
| Forêt de Roverè Veronese (130) ⚠️ | Roverè Veronese | 3 |
| Bois de Mezzane di Sotto (7) ⚠️ | Mezzane di Sotto | 3 |
| Bois de Velo Veronese (23) ⚠️ | Velo Veronese | 3 |
| Bois de Grezzana (31) ⚠️ | Grezzana | 3 |
| Bois de San Mauro di Saline (20) ⚠️ | San Mauro di Saline | 3 |
| Bois de San Mauro di Saline (27) ⚠️ | San Mauro di Saline | 3 |
| Bois de San Mauro di Saline (38) ⚠️ | San Mauro di Saline | 3 |
| Bois de Grezzana (42) ⚠️ | Grezzana | 3 |
| Bois de Zevio (4) ⚠️ | Zevio | 3 |
| Bois de Roverè Veronese (29) ⚠️ | Roverè Veronese | 3 |
| Bois de Roverè Veronese (42) ⚠️ | Roverè Veronese | 3 |
| Bois de Roverè Veronese (45) ⚠️ | Roverè Veronese | 3 |
| Bois de Grezzana (62) ⚠️ | Grezzana | 3 |
| Bois de Cerro Veronese ⚠️ | Cerro Veronese | 3 |
| Forêt de Erbezzo (201) ⚠️ | Erbezzo | 3 |
| Forêt de Bosco Chiesanuova (381) ⚠️ | Bosco Chiesanuova | 3 |
| Forêt de Verona (451) ⚠️ | Verona | 3 |
| Forêt de Verona (464) ⚠️ | Verona | 3 |
| Forêt de Verona (468) ⚠️ | Verona | 3 |
| Forêt de Caprino Veronese (357) ⚠️ | Caprino Veronese | 3 |
| Forêt de Fumane (203) ⚠️ | Fumane | 3 |
| Forêt de Dolcè (82) ⚠️ | Dolcè | 3 |
| Bois de Valeggio sul Mincio (25) ⚠️ | Valeggio sul Mincio | 3 |
| Porto di San Giovanni Lupatoto ⚠️ | San Giovanni Lupatoto | 3 |
| Forêt de Vestenanova (228) ⚠️ | Vestenanova | 3 |
| Forêt de San Giovanni Ilarione (163) ⚠️ | San Giovanni Ilarione | 3 |
| Forêt de San Giovanni Ilarione (173) ⚠️ | San Giovanni Ilarione | 3 |
| Forêt de Montecchia di Crosara (91) ⚠️ | Montecchia di Crosara | 3 |
| Bois de Ronco all'Adige (22) ⚠️ | Ronco all'Adige | 3 |
| Parco delle Mura (4) ⚠️ | Verona | 2 |
| Parco delle Mura (5) ⚠️ | Verona | 2 |
| Bois de Verona ⚠️ | Verona | 2 |
| Forêt de Lavagno ⚠️ | Lavagno | 2 |
| Forêt de Lavagno (3) ⚠️ | Lavagno | 2 |
| Forêt de Lavagno (4) ⚠️ | Lavagno | 2 |
| Parco Catullo ⚠️ | Peschiera del Garda | 2 |
| Giardini San Marco ⚠️ | Verona | 2 |
| Bois de Monteforte d'Alpone (2) ⚠️ | Monteforte d'Alpone | 2 |
| Forêt de Lavagno (5) ⚠️ | San Martino Buon Albergo | 2 |
| Forêt de San Mauro di Saline ⚠️ | San Mauro di Saline | 2 |
| Forêt de Mezzane di Sotto (17) ⚠️ | Mezzane di Sotto | 2 |
| Forêt de Mezzane di Sotto (25) ⚠️ | Mezzane di Sotto | 2 |
| Forêt de Grezzana (3) ⚠️ | Grezzana | 2 |
| Forêt de Cerro Veronese (2) ⚠️ | Cerro Veronese | 2 |
| Forêt de Negrar di Valpolicella (5) ⚠️ | Negrar di Valpolicella | 2 |
| Forêt de Grezzana (14) ⚠️ | Grezzana | 2 |
| Forêt de Negrar di Valpolicella (11) ⚠️ | Negrar di Valpolicella | 2 |
| Forêt de Negrar di Valpolicella (12) ⚠️ | Negrar di Valpolicella | 2 |
| Forêt de Grezzana (38) ⚠️ | Grezzana | 2 |
| Forêt de Cerro Veronese (11) ⚠️ | Cerro Veronese | 2 |
| Forêt de Roverè Veronese (16) ⚠️ | Roverè Veronese | 2 |
| Forêt de Cerro Veronese (17) ⚠️ | Cerro Veronese | 2 |
| Forêt de Grezzana (54) ⚠️ | Grezzana | 2 |
| Forêt de Roverè Veronese (19) ⚠️ | Roverè Veronese | 2 |
| Forêt de Grezzana (63) ⚠️ | Grezzana | 2 |
| Forêt de Grezzana (64) ⚠️ | Grezzana | 2 |
| Forêt de Negrar di Valpolicella (22) ⚠️ | Negrar di Valpolicella | 2 |
| Forêt de Grezzana (68) ⚠️ | Grezzana | 2 |
| Forêt de Grezzana (69) ⚠️ | Grezzana | 2 |
| Forêt de Grezzana (70) ⚠️ | Grezzana | 2 |
| Forêt de Negrar di Valpolicella (25) ⚠️ | Negrar di Valpolicella | 2 |
| Forêt de Buttapietra (3) ⚠️ | Buttapietra | 2 |
| Forêt de San Martino Buon Albergo (23) ⚠️ | San Martino Buon Albergo | 2 |
| Forêt de Negrar di Valpolicella (32) ⚠️ | Negrar di Valpolicella | 2 |
| Forêt de Bussolengo ⚠️ | Bussolengo | 2 |
| Forêt de Bussolengo (4) ⚠️ | Bussolengo | 2 |
| Forêt de Bussolengo (10) ⚠️ | Bussolengo | 2 |
| Forêt de Sant'Ambrogio di Valpolicella (3) ⚠️ | Sant'Ambrogio di Valpolicella | 2 |
| Forêt de Valeggio sul Mincio (6) ⚠️ | Valeggio sul Mincio | 2 |
| Forêt de Valeggio sul Mincio (8) ⚠️ | Valeggio sul Mincio | 2 |
| Forêt de Valeggio sul Mincio (9) ⚠️ | Valeggio sul Mincio | 2 |
| Forêt de Valeggio sul Mincio (14) ⚠️ | Valeggio sul Mincio | 2 |
| Forêt de Valeggio sul Mincio (15) ⚠️ | Valeggio sul Mincio | 2 |
| Forêt de Sommacampagna (6) ⚠️ | Sommacampagna | 2 |
| Forêt de Sommacampagna (7) ⚠️ | Sommacampagna | 2 |
| Forêt de Sant'Ambrogio di Valpolicella (10) ⚠️ | Sant'Ambrogio di Valpolicella | 2 |
| Forêt de Negrar di Valpolicella (41) ⚠️ | Negrar di Valpolicella | 2 |
| Forêt de Negrar di Valpolicella (50) ⚠️ | Negrar di Valpolicella | 2 |
| Forêt de Negrar di Valpolicella (51) ⚠️ | Negrar di Valpolicella | 2 |
| Forêt de Marano di Valpolicella (10) ⚠️ | Marano di Valpolicella | 2 |
| Forêt de Marano di Valpolicella (13) ⚠️ | Marano di Valpolicella | 2 |
| Forêt de Grezzana (76) ⚠️ | Grezzana | 2 |
| Forêt de Roverè Veronese (22) ⚠️ | Roverè Veronese | 2 |
| Forêt de Sant'Ambrogio di Valpolicella (13) ⚠️ | Sant'Ambrogio di Valpolicella | 2 |
| Forêt de Marano di Valpolicella (16) ⚠️ | Marano di Valpolicella | 2 |
| Forêt de Cavaion Veronese (6) ⚠️ | Cavaion Veronese | 2 |
| Forêt de Affi (7) ⚠️ | Affi | 2 |
| Forêt de Vigasio (3) ⚠️ | Vigasio | 2 |
| Forêt de Sona (12) ⚠️ | Sona | 2 |
| Forêt de Sona (16) ⚠️ | Sommacampagna | 2 |
| Forêt de Nogara ⚠️ | Nogara | 2 |
| Parc de Legnago (10) ⚠️ | Legnago | 2 |
| Forêt de Velo Veronese (12) ⚠️ | Velo Veronese | 2 |
| Forêt de Velo Veronese (13) ⚠️ | Velo Veronese | 2 |
| Forêt de Roverè Veronese (52) ⚠️ | Roverè Veronese | 2 |
| Forêt de Velo Veronese (21) ⚠️ | Velo Veronese | 2 |
| Forêt de Velo Veronese (24) ⚠️ | Velo Veronese | 2 |
| Forêt de Roverè Veronese (69) ⚠️ | Roverè Veronese | 2 |
| Bois de Lazise ⚠️ | Lazise | 2 |
| Forêt de Sommacampagna (23) ⚠️ | Sommacampagna | 2 |
| Forêt de Bovolone (3) ⚠️ | Bovolone | 2 |
| Forêt de Erbezzo (10) ⚠️ | Erbezzo | 2 |
| Forêt de Erbezzo (13) ⚠️ | Erbezzo | 2 |
| Forêt de Erbezzo (15) ⚠️ | Erbezzo | 2 |
| Forêt de Erbezzo (18) ⚠️ | Erbezzo | 2 |
| Forêt de Erbezzo (21) ⚠️ | Erbezzo | 2 |
| Forêt de Erbezzo (27) ⚠️ | Erbezzo | 2 |
| Forêt de Erbezzo (36) ⚠️ | Erbezzo | 2 |
| Forêt de Erbezzo (37) ⚠️ | Erbezzo | 2 |
| Forêt de Erbezzo (45) ⚠️ | Erbezzo | 2 |
| Forêt de Erbezzo (93) ⚠️ | Erbezzo | 2 |
| Forêt de Erbezzo (108) ⚠️ | Erbezzo | 2 |
| Forêt de Erbezzo (122) ⚠️ | Erbezzo | 2 |
| Forêt de Erbezzo (134) ⚠️ | Erbezzo | 2 |
| Forêt de Erbezzo (135) ⚠️ | Erbezzo | 2 |
| Forêt de Erbezzo (149) ⚠️ | Erbezzo | 2 |
| Forêt de Erbezzo (151) ⚠️ | Erbezzo | 2 |
| Forêt de Erbezzo (155) ⚠️ | Erbezzo | 2 |
| Forêt de Erbezzo (156) ⚠️ | Erbezzo | 2 |
| Forêt de Erbezzo (161) ⚠️ | Erbezzo | 2 |
| Forêt de Erbezzo (167) ⚠️ | Erbezzo | 2 |
| Forêt de Erbezzo (171) ⚠️ | Erbezzo | 2 |
| Forêt de Erbezzo (174) ⚠️ | Erbezzo | 2 |
| Forêt de Erbezzo (182) ⚠️ | Erbezzo | 2 |
| Forêt de Sant'Anna d'Alfaedo (5) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Sant'Anna d'Alfaedo (6) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Sant'Anna d'Alfaedo (22) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Sant'Anna d'Alfaedo (32) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Sant'Anna d'Alfaedo (39) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Sant'Anna d'Alfaedo (51) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Sant'Anna d'Alfaedo (69) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Sant'Anna d'Alfaedo (107) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Sant'Anna d'Alfaedo (111) ⚠️ | Dolcè | 2 |
| Forêt de Sant'Anna d'Alfaedo (126) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Sant'Anna d'Alfaedo (137) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Sant'Anna d'Alfaedo (163) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Sant'Anna d'Alfaedo (168) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Sant'Anna d'Alfaedo (177) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Sant'Anna d'Alfaedo (199) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Sant'Anna d'Alfaedo (200) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Sant'Anna d'Alfaedo (213) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Sant'Anna d'Alfaedo (214) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Sant'Anna d'Alfaedo (215) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Sant'Anna d'Alfaedo (220) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Sant'Anna d'Alfaedo (222) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Sant'Anna d'Alfaedo (228) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Sant'Anna d'Alfaedo (232) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Sant'Anna d'Alfaedo (235) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Sant'Anna d'Alfaedo (238) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Sant'Anna d'Alfaedo (240) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Sant'Anna d'Alfaedo (241) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Sant'Anna d'Alfaedo (246) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Sant'Anna d'Alfaedo (250) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Sant'Anna d'Alfaedo (251) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Sant'Anna d'Alfaedo (259) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Bosco Chiesanuova (4) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (7) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (15) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (16) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (17) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (33) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (38) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (48) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (50) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (52) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (55) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (58) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (87) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (98) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (129) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (133) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (157) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (179) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (201) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (218) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (228) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (229) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (235) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (260) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (261) ⚠️ | Roverè Veronese | 2 |
| Forêt de Bosco Chiesanuova (266) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (267) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (274) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (277) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (278) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (282) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (284) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (294) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (298) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (299) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (304) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (310) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (313) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (317) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (322) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (325) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (333) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (336) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (337) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (338) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (340) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (342) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (350) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (353) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Bosco Chiesanuova (366) ⚠️ | Bosco Chiesanuova | 2 |
| Bosco Buri ⚠️ | Verona | 2 |
| Forêt de Verona (8) ⚠️ | Verona | 2 |
| Forêt de Verona (9) ⚠️ | Verona | 2 |
| Forêt de Verona (11) ⚠️ | Verona | 2 |
| Forêt de Verona (27) ⚠️ | Verona | 2 |
| Forêt de Verona (46) ⚠️ | Verona | 2 |
| Forêt de Verona (50) ⚠️ | Verona | 2 |
| Forêt de Verona (52) ⚠️ | Verona | 2 |
| Forêt de Verona (59) ⚠️ | Verona | 2 |
| Forêt de Verona (72) ⚠️ | Verona | 2 |
| Forêt de Verona (82) ⚠️ | Verona | 2 |
| Forêt de Verona (84) ⚠️ | Verona | 2 |
| Forêt de Verona (97) ⚠️ | Verona | 2 |
| Forêt de Verona (102) ⚠️ | Verona | 2 |
| Forêt de Verona (104) ⚠️ | Verona | 2 |
| Forêt de Verona (118) ⚠️ | Verona | 2 |
| Forêt de Verona (119) ⚠️ | Verona | 2 |
| Forêt de Verona (129) ⚠️ | Verona | 2 |
| Forêt de Verona (137) ⚠️ | Verona | 2 |
| Forêt de Verona (139) ⚠️ | Verona | 2 |
| Forêt de Verona (143) ⚠️ | Verona | 2 |
| Forêt de Verona (147) ⚠️ | Verona | 2 |
| Forêt de Verona (149) ⚠️ | Verona | 2 |
| Forêt de Verona (152) ⚠️ | Verona | 2 |
| Forêt de Verona (154) ⚠️ | Verona | 2 |
| Forêt de Verona (162) ⚠️ | Verona | 2 |
| Forêt de Verona (168) ⚠️ | Verona | 2 |
| Forêt de Verona (169) ⚠️ | Verona | 2 |
| Forêt de Verona (179) ⚠️ | Verona | 2 |
| Forêt de Verona (190) ⚠️ | Verona | 2 |
| Parc de Verona (80) ⚠️ | Verona | 2 |
| Forêt de Verona (223) ⚠️ | Verona | 2 |
| Forêt de Verona (224) ⚠️ | Verona | 2 |
| Forêt de Verona (235) ⚠️ | Verona | 2 |
| Forêt de Verona (244) ⚠️ | Verona | 2 |
| Forêt de Verona (249) ⚠️ | Verona | 2 |
| Forêt de Verona (274) ⚠️ | Verona | 2 |
| Forêt de Verona (275) ⚠️ | Verona | 2 |
| Forêt de Verona (286) ⚠️ | Verona | 2 |
| Forêt de Verona (287) ⚠️ | Verona | 2 |
| Forêt de Verona (288) ⚠️ | Verona | 2 |
| Forêt de Verona (319) ⚠️ | Verona | 2 |
| Forêt de Verona (321) ⚠️ | Verona | 2 |
| Forêt de Verona (330) ⚠️ | Verona | 2 |
| Forêt de Verona (334) ⚠️ | Verona | 2 |
| Forêt de Verona (355) ⚠️ | Verona | 2 |
| Forêt de Verona (359) ⚠️ | Verona | 2 |
| Forêt de Verona (376) ⚠️ | Verona | 2 |
| Forêt de Verona (396) ⚠️ | Verona | 2 |
| Forêt de Verona (400) ⚠️ | Verona | 2 |
| Forêt de Verona (413) ⚠️ | Verona | 2 |
| Forêt de Verona (421) ⚠️ | Verona | 2 |
| Forêt de Verona (424) ⚠️ | Verona | 2 |
| Forêt de Verona (430) ⚠️ | Verona | 2 |
| Bois de Cerea ⚠️ | Cerea | 2 |
| Bois de Legnago (7) ⚠️ | Legnago | 2 |
| Bois de Legnago (8) ⚠️ | Legnago | 2 |
| Forêt de Cerea (2) ⚠️ | Cerea | 2 |
| Parc de Villafranca di Verona (47) ⚠️ | Villafranca di Verona | 2 |
| Forêt de Cerea (5) ⚠️ | Cerea | 2 |
| Forêt de Malcesine (19) ⚠️ | Malcesine | 2 |
| Forêt de Torri del Benaco (10) ⚠️ | Torri del Benaco | 2 |
| Forêt de Torri del Benaco (17) ⚠️ | Torri del Benaco | 2 |
| Forêt de San Zeno di Montagna ⚠️ | San Zeno di Montagna | 2 |
| Forêt de Torri del Benaco (27) ⚠️ | Torri del Benaco | 2 |
| Forêt de San Zeno di Montagna (21) ⚠️ | San Zeno di Montagna | 2 |
| Forêt de San Zeno di Montagna (28) ⚠️ | San Zeno di Montagna | 2 |
| Forêt de San Zeno di Montagna (38) ⚠️ | San Zeno di Montagna | 2 |
| Forêt de San Zeno di Montagna (45) ⚠️ | San Zeno di Montagna | 2 |
| Forêt de San Zeno di Montagna (60) ⚠️ | San Zeno di Montagna | 2 |
| Forêt de Brenzone sul Garda ⚠️ | Brenzone sul Garda | 2 |
| Forêt de San Zeno di Montagna (69) ⚠️ | San Zeno di Montagna | 2 |
| Forêt de San Zeno di Montagna (75) ⚠️ | San Zeno di Montagna | 2 |
| Forêt de San Zeno di Montagna (77) ⚠️ | San Zeno di Montagna | 2 |
| Forêt de San Zeno di Montagna (88) ⚠️ | San Zeno di Montagna | 2 |
| Forêt de San Zeno di Montagna (90) ⚠️ | San Zeno di Montagna | 2 |
| Forêt de Caprino Veronese ⚠️ | Caprino Veronese | 2 |
| Forêt de San Zeno di Montagna (94) ⚠️ | San Zeno di Montagna | 2 |
| Forêt de San Zeno di Montagna (106) ⚠️ | San Zeno di Montagna | 2 |
| Forêt de San Zeno di Montagna (108) ⚠️ | San Zeno di Montagna | 2 |
| Forêt de Brenzone sul Garda (3) ⚠️ | Brenzone sul Garda | 2 |
| Forêt de San Zeno di Montagna (110) ⚠️ | San Zeno di Montagna | 2 |
| Forêt de Caprino Veronese (5) ⚠️ | Caprino Veronese | 2 |
| Forêt de Caprino Veronese (17) ⚠️ | Caprino Veronese | 2 |
| Forêt de Caprino Veronese (18) ⚠️ | Caprino Veronese | 2 |
| Forêt de Caprino Veronese (19) ⚠️ | Caprino Veronese | 2 |
| Forêt de Caprino Veronese (29) ⚠️ | Caprino Veronese | 2 |
| Forêt de Caprino Veronese (32) ⚠️ | Caprino Veronese | 2 |
| Forêt de Caprino Veronese (33) ⚠️ | Caprino Veronese | 2 |
| Forêt de Caprino Veronese (34) ⚠️ | Caprino Veronese | 2 |
| Forêt de Caprino Veronese (55) ⚠️ | Caprino Veronese | 2 |
| Forêt de Brentino Belluno ⚠️ | Caprino Veronese | 2 |
| Forêt de Caprino Veronese (64) ⚠️ | Caprino Veronese | 2 |
| Forêt de Brentino Belluno (2) ⚠️ | Brentino Belluno | 2 |
| Forêt de Caprino Veronese (75) ⚠️ | Caprino Veronese | 2 |
| Forêt de Caprino Veronese (87) ⚠️ | Caprino Veronese | 2 |
| Forêt de Caprino Veronese (118) ⚠️ | Caprino Veronese | 2 |
| Forêt de Caprino Veronese (122) ⚠️ | Caprino Veronese | 2 |
| Forêt de Caprino Veronese (130) ⚠️ | Caprino Veronese | 2 |
| Forêt de Caprino Veronese (137) ⚠️ | Caprino Veronese | 2 |
| Forêt de Caprino Veronese (142) ⚠️ | Caprino Veronese | 2 |
| Forêt de Caprino Veronese (144) ⚠️ | Caprino Veronese | 2 |
| Forêt de Ferrara di Monte Baldo (3) ⚠️ | Caprino Veronese | 2 |
| Forêt de Caprino Veronese (173) ⚠️ | Caprino Veronese | 2 |
| Forêt de Caprino Veronese (176) ⚠️ | Caprino Veronese | 2 |
| Forêt de Caprino Veronese (186) ⚠️ | Caprino Veronese | 2 |
| Forêt de Caprino Veronese (188) ⚠️ | Caprino Veronese | 2 |
| Forêt de Caprino Veronese (196) ⚠️ | Caprino Veronese | 2 |
| Forêt de Caprino Veronese (201) ⚠️ | Caprino Veronese | 2 |
| Forêt de Caprino Veronese (204) ⚠️ | Caprino Veronese | 2 |
| Forêt de Caprino Veronese (213) ⚠️ | Caprino Veronese | 2 |
| Forêt de Caprino Veronese (219) ⚠️ | Caprino Veronese | 2 |
| Forêt de Caprino Veronese (240) ⚠️ | Caprino Veronese | 2 |
| Forêt de Caprino Veronese (241) ⚠️ | Caprino Veronese | 2 |
| Forêt de Caprino Veronese (242) ⚠️ | Caprino Veronese | 2 |
| Forêt de Caprino Veronese (251) ⚠️ | Caprino Veronese | 2 |
| Forêt de Caprino Veronese (258) ⚠️ | Caprino Veronese | 2 |
| Forêt de Brenzone sul Garda (15) ⚠️ | Brenzone sul Garda | 2 |
| Forêt de Brenzone sul Garda (17) ⚠️ | Brenzone sul Garda | 2 |
| Forêt de Brenzone sul Garda (18) ⚠️ | Brenzone sul Garda | 2 |
| Forêt de Brenzone sul Garda (31) ⚠️ | Brenzone sul Garda | 2 |
| Forêt de Brenzone sul Garda (37) ⚠️ | Brenzone sul Garda | 2 |
| Forêt de Brenzone sul Garda (38) ⚠️ | Brenzone sul Garda | 2 |
| Forêt de Brenzone sul Garda (52) ⚠️ | Brenzone sul Garda | 2 |
| Forêt de Ferrara di Monte Baldo (12) ⚠️ | Ferrara di Monte Baldo | 2 |
| Forêt de Ferrara di Monte Baldo (36) ⚠️ | Ferrara di Monte Baldo | 2 |
| Forêt de Ferrara di Monte Baldo (39) ⚠️ | Ferrara di Monte Baldo | 2 |
| Forêt de Ferrara di Monte Baldo (44) ⚠️ | Ferrara di Monte Baldo | 2 |
| Forêt de Ferrara di Monte Baldo (50) ⚠️ | Ferrara di Monte Baldo | 2 |
| Forêt de Ferrara di Monte Baldo (54) ⚠️ | Ferrara di Monte Baldo | 2 |
| Forêt de Ferrara di Monte Baldo (56) ⚠️ | Ferrara di Monte Baldo | 2 |
| Forêt de Ferrara di Monte Baldo (59) ⚠️ | Ferrara di Monte Baldo | 2 |
| Forêt de Ferrara di Monte Baldo (88) ⚠️ | Ferrara di Monte Baldo | 2 |
| Forêt de Ferrara di Monte Baldo (89) ⚠️ | Ferrara di Monte Baldo | 2 |
| Forêt de Ferrara di Monte Baldo (101) ⚠️ | Ferrara di Monte Baldo | 2 |
| Forêt de Ferrara di Monte Baldo (103) ⚠️ | Ferrara di Monte Baldo | 2 |
| Forêt de Ferrara di Monte Baldo (107) ⚠️ | Ferrara di Monte Baldo | 2 |
| Forêt de Fumane (4) ⚠️ | Fumane | 2 |
| Forêt de Fumane (19) ⚠️ | Fumane | 2 |
| Forêt de Fumane (28) ⚠️ | Fumane | 2 |
| Forêt de Fumane (29) ⚠️ | Fumane | 2 |
| Forêt de Fumane (32) ⚠️ | Fumane | 2 |
| Forêt de Fumane (35) ⚠️ | Fumane | 2 |
| Forêt de Fumane (39) ⚠️ | Fumane | 2 |
| Forêt de Fumane (43) ⚠️ | Fumane | 2 |
| Forêt de Fumane (49) ⚠️ | Fumane | 2 |
| Forêt de Fumane (50) ⚠️ | Fumane | 2 |
| Forêt de Fumane (51) ⚠️ | Fumane | 2 |
| Forêt de Fumane (52) ⚠️ | Fumane | 2 |
| Forêt de Fumane (54) ⚠️ | Fumane | 2 |
| Forêt de Caprino Veronese (276) ⚠️ | Caprino Veronese | 2 |
| Forêt de Brentino Belluno (11) ⚠️ | Brentino Belluno | 2 |
| Forêt de Brentino Belluno (12) ⚠️ | Brentino Belluno | 2 |
| Forêt de Brentino Belluno (24) ⚠️ | Brentino Belluno | 2 |
| Forêt de Brentino Belluno (26) ⚠️ | Brentino Belluno | 2 |
| Forêt de Brentino Belluno (30) ⚠️ | Brentino Belluno | 2 |
| Forêt de Brentino Belluno (32) ⚠️ | Brentino Belluno | 2 |
| Forêt de Brentino Belluno (37) ⚠️ | Brentino Belluno | 2 |
| Forêt de Brentino Belluno (41) ⚠️ | Brentino Belluno | 2 |
| Forêt de Brentino Belluno (52) ⚠️ | Brentino Belluno | 2 |
| Forêt de Brentino Belluno (55) ⚠️ | Ferrara di Monte Baldo | 2 |
| Forêt de Brentino Belluno (57) ⚠️ | Brentino Belluno | 2 |
| Forêt de Fumane (58) ⚠️ | Fumane | 2 |
| Forêt de Malcesine (26) ⚠️ | Malcesine | 2 |
| Forêt de Malcesine (28) ⚠️ | Malcesine | 2 |
| Forêt de Malcesine (29) ⚠️ | Malcesine | 2 |
| Forêt de Malcesine (32) ⚠️ | Malcesine | 2 |
| Forêt de Malcesine (35) ⚠️ | Malcesine | 2 |
| Forêt de Malcesine (41) ⚠️ | Malcesine | 2 |
| Forêt de Malcesine (45) ⚠️ | Malcesine | 2 |
| Forêt de Malcesine (51) ⚠️ | Malcesine | 2 |
| Forêt de Malcesine (54) ⚠️ | Malcesine | 2 |
| Forêt de Malcesine (56) ⚠️ | Malcesine | 2 |
| Forêt de Malcesine (61) ⚠️ | Malcesine | 2 |
| Forêt de Malcesine (63) ⚠️ | Malcesine | 2 |
| Forêt de Malcesine (65) ⚠️ | Malcesine | 2 |
| Forêt de Malcesine (81) ⚠️ | Malcesine | 2 |
| Forêt de Malcesine (91) ⚠️ | Malcesine | 2 |
| Forêt de Malcesine (98) ⚠️ | Malcesine | 2 |
| Forêt de Malcesine (108) ⚠️ | Malcesine | 2 |
| Forêt de Malcesine (109) ⚠️ | Malcesine | 2 |
| Forêt de Malcesine (124) ⚠️ | Malcesine | 2 |
| Forêt de Fumane (96) ⚠️ | Fumane | 2 |
| Forêt de Fumane (111) ⚠️ | Fumane | 2 |
| Forêt de Lazise (11) ⚠️ | Lazise | 2 |
| Forêt de Fumane (127) ⚠️ | Fumane | 2 |
| Forêt de Fumane (131) ⚠️ | Fumane | 2 |
| Forêt de Fumane (133) ⚠️ | Fumane | 2 |
| Forêt de Fumane (149) ⚠️ | Fumane | 2 |
| Forêt de Fumane (152) ⚠️ | Fumane | 2 |
| Forêt de San Zeno di Montagna (121) ⚠️ | San Zeno di Montagna | 2 |
| Forêt de Dolcè (7) ⚠️ | Dolcè | 2 |
| Forêt de Dolcè (12) ⚠️ | Dolcè | 2 |
| Forêt de Dolcè (17) ⚠️ | Dolcè | 2 |
| Forêt de Dolcè (19) ⚠️ | Dolcè | 2 |
| Forêt de Sant'Anna d'Alfaedo (262) ⚠️ | Sant'Anna d'Alfaedo | 2 |
| Forêt de Dolcè (21) ⚠️ | Dolcè | 2 |
| Forêt de Dolcè (44) ⚠️ | Dolcè | 2 |
| Forêt de Fumane (158) ⚠️ | Fumane | 2 |
| Forêt de Dolcè (62) ⚠️ | Dolcè | 2 |
| Forêt de Dolcè (69) ⚠️ | Dolcè | 2 |
| Bois de Valeggio sul Mincio (6) ⚠️ | Valeggio sul Mincio | 2 |
| Forêt de Caprino Veronese (328) ⚠️ | Caprino Veronese | 2 |
| Forêt de San Zeno di Montagna (195) ⚠️ | San Zeno di Montagna | 2 |
| Forêt de Dolcè (78) ⚠️ | Dolcè | 2 |
| Forêt de Peschiera del Garda (5) ⚠️ | Peschiera del Garda | 2 |
| Forêt de Cerro Veronese (24) ⚠️ | Cerro Veronese | 2 |
| Forêt de Illasi (3) ⚠️ | Illasi | 2 |
| Forêt de Cerea (7) ⚠️ | Cerea | 2 |
| Forêt de Cerea (9) ⚠️ | Cerea | 2 |
| Forêt de Illasi (9) ⚠️ | Illasi | 2 |
| Forêt de Cazzano di Tramigna (3) ⚠️ | Cazzano di Tramigna | 2 |
| Bois de Costermano sul Garda ⚠️ | Costermano sul Garda | 2 |
| Forêt de Cazzano di Tramigna (4) ⚠️ | Cazzano di Tramigna | 2 |
| Forêt de San Giovanni Ilarione (3) ⚠️ | San Giovanni Ilarione | 2 |
| Forêt de Monteforte d'Alpone (5) ⚠️ | Monteforte d'Alpone | 2 |
| Forêt de Soave (2) ⚠️ | Soave | 2 |
| Forêt de Monteforte d'Alpone (16) ⚠️ | Monteforte d'Alpone | 2 |
| Forêt de Monteforte d'Alpone (17) ⚠️ | Monteforte d'Alpone | 2 |
| Forêt de Monteforte d'Alpone (20) ⚠️ | Soave | 2 |
| Forêt de Povegliano Veronese (2) ⚠️ | Povegliano Veronese | 2 |
| Parco Santa Teresa (2) ⚠️ | Verona | 2 |
| Forêt de Grezzana (91) ⚠️ | Grezzana | 2 |
| Forêt de Grezzana (100) ⚠️ | Grezzana | 2 |
| Parc de Bardolino (5) ⚠️ | Bardolino | 2 |
| Forêt de Marano di Valpolicella (35) ⚠️ | Marano di Valpolicella | 2 |
| Bois de Roverè Veronese ⚠️ | Roverè Veronese | 2 |
| Forêt de Soave (17) ⚠️ | Soave | 2 |
| Forêt de Legnago (4) ⚠️ | Legnago | 2 |
| Forêt de Soave (22) ⚠️ | Soave | 2 |
| Forêt de Soave (24) ⚠️ | Soave | 2 |
| Bois de Caldiero ⚠️ | Caldiero | 2 |
| Forêt de Pastrengo (5) ⚠️ | Pastrengo | 2 |
| Forêt de Roncà (11) ⚠️ | Roncà | 2 |
| Forêt de Roncà (17) ⚠️ | Roncà | 2 |
| Forêt de Roncà (19) ⚠️ | Roncà | 2 |
| Forêt de Roncà (23) ⚠️ | Roncà | 2 |
| Forêt de Roncà (31) ⚠️ | Roncà | 2 |
| Parc de Roncà ⚠️ | Roncà | 2 |
| Forêt de Roncà (67) ⚠️ | Roncà | 2 |
| Forêt de Roncà (74) ⚠️ | Roncà | 2 |
| Forêt de Roncà (83) ⚠️ | Roncà | 2 |
| Forêt de Roncà (97) ⚠️ | Roncà | 2 |
| Forêt de Roncà (99) ⚠️ | Roncà | 2 |
| Forêt de Roncà (101) ⚠️ | Roncà | 2 |
| Forêt de Roncà (109) ⚠️ | Roncà | 2 |
| Forêt de Roncà (110) ⚠️ | Roncà | 2 |
| Forêt de Roncà (114) ⚠️ | Roncà | 2 |
| Forêt de Vestenanova (16) ⚠️ | Vestenanova | 2 |
| Forêt de Vestenanova (20) ⚠️ | Vestenanova | 2 |
| Forêt de Vestenanova (22) ⚠️ | Vestenanova | 2 |
| Forêt de Vestenanova (26) ⚠️ | Vestenanova | 2 |
| Forêt de Vestenanova (35) ⚠️ | Vestenanova | 2 |
| Forêt de Vestenanova (37) ⚠️ | Vestenanova | 2 |
| Forêt de Vestenanova (74) ⚠️ | Vestenanova | 2 |
| Forêt de Vestenanova (76) ⚠️ | Vestenanova | 2 |
| Forêt de Vestenanova (114) ⚠️ | Vestenanova | 2 |
| Forêt de Vestenanova (120) ⚠️ | Vestenanova | 2 |
| Forêt de Vestenanova (125) ⚠️ | Vestenanova | 2 |
| Forêt de Vestenanova (167) ⚠️ | Vestenanova | 2 |
| Forêt de Vestenanova (173) ⚠️ | Vestenanova | 2 |
| Forêt de Vestenanova (178) ⚠️ | Vestenanova | 2 |
| Forêt de Vestenanova (185) ⚠️ | Vestenanova | 2 |
| Forêt de Vestenanova (187) ⚠️ | Vestenanova | 2 |
| Bois de Bardolino ⚠️ | Lazise | 2 |
| Bois de Negrar di Valpolicella (8) ⚠️ | Negrar di Valpolicella | 2 |
| Bois de Negrar di Valpolicella (11) ⚠️ | Verona | 2 |
| Bois de Grezzana (11) ⚠️ | Grezzana | 2 |
| Forêt de San Giovanni Ilarione (29) ⚠️ | San Giovanni Ilarione | 2 |
| Forêt de San Giovanni Ilarione (36) ⚠️ | San Giovanni Ilarione | 2 |
| Forêt de San Giovanni Ilarione (41) ⚠️ | San Giovanni Ilarione | 2 |
| Forêt de San Giovanni Ilarione (43) ⚠️ | San Giovanni Ilarione | 2 |
| Forêt de San Giovanni Ilarione (44) ⚠️ | San Giovanni Ilarione | 2 |
| Forêt de San Giovanni Ilarione (73) ⚠️ | San Giovanni Ilarione | 2 |
| Forêt de San Giovanni Ilarione (77) ⚠️ | San Giovanni Ilarione | 2 |
| Forêt de San Giovanni Ilarione (84) ⚠️ | San Giovanni Ilarione | 2 |
| Forêt de San Giovanni Ilarione (110) ⚠️ | San Giovanni Ilarione | 2 |
| Forêt de San Giovanni Ilarione (117) ⚠️ | San Giovanni Ilarione | 2 |
| Forêt de San Giovanni Ilarione (120) ⚠️ | San Giovanni Ilarione | 2 |
| Forêt de San Giovanni Ilarione (137) ⚠️ | San Giovanni Ilarione | 2 |
| Forêt de San Giovanni Ilarione (140) ⚠️ | San Giovanni Ilarione | 2 |
| Forêt de San Giovanni Ilarione (146) ⚠️ | San Giovanni Ilarione | 2 |
| Forêt de Selva di Progno (9) ⚠️ | Selva di Progno | 2 |
| Forêt de Selva di Progno (23) ⚠️ | Selva di Progno | 2 |
| Forêt de Selva di Progno (66) ⚠️ | Selva di Progno | 2 |
| Forêt de Selva di Progno (67) ⚠️ | Selva di Progno | 2 |
| Forêt de Selva di Progno (69) ⚠️ | Selva di Progno | 2 |
| Forêt de Selva di Progno (70) ⚠️ | Selva di Progno | 2 |
| Forêt de Selva di Progno (73) ⚠️ | Selva di Progno | 2 |
| Forêt de Selva di Progno (75) ⚠️ | Selva di Progno | 2 |
| Forêt de Selva di Progno (79) ⚠️ | Selva di Progno | 2 |
| Forêt de Selva di Progno (93) ⚠️ | Selva di Progno | 2 |
| Forêt de Selva di Progno (107) ⚠️ | Selva di Progno | 2 |
| Forêt de Selva di Progno (115) ⚠️ | Selva di Progno | 2 |
| Forêt de Selva di Progno (123) ⚠️ | Selva di Progno | 2 |
| Forêt de Badia Calavena (3) ⚠️ | Badia Calavena | 2 |
| Forêt de Selva di Progno (142) ⚠️ | Selva di Progno | 2 |
| Forêt de Selva di Progno (145) ⚠️ | Selva di Progno | 2 |
| Forêt de Selva di Progno (153) ⚠️ | Selva di Progno | 2 |
| Forêt de Selva di Progno (164) ⚠️ | Selva di Progno | 2 |
| Forêt de Selva di Progno (170) ⚠️ | Selva di Progno | 2 |
| Forêt de Selva di Progno (177) ⚠️ | Selva di Progno | 2 |
| Forêt de Selva di Progno (180) ⚠️ | Selva di Progno | 2 |
| Forêt de Selva di Progno (193) ⚠️ | Selva di Progno | 2 |
| Forêt de Selva di Progno (194) ⚠️ | Selva di Progno | 2 |
| Forêt de Roverè Veronese (96) ⚠️ | Roverè Veronese | 2 |
| Parc de Verona (145) ⚠️ | Verona | 2 |
| Forêt de Montecchia di Crosara (12) ⚠️ | Montecchia di Crosara | 2 |
| Forêt de Montecchia di Crosara (13) ⚠️ | Montecchia di Crosara | 2 |
| Forêt de Montecchia di Crosara (23) ⚠️ | Montecchia di Crosara | 2 |
| Forêt de Montecchia di Crosara (47) ⚠️ | Montecchia di Crosara | 2 |
| Forêt de Montecchia di Crosara (83) ⚠️ | Montecchia di Crosara | 2 |
| Forêt de Cerro Veronese (56) ⚠️ | Cerro Veronese | 2 |
| Parco dell' amicizia dei popoli ⚠️ | Costermano sul Garda | 2 |
| Bois de Valeggio sul Mincio (21) ⚠️ | Valeggio sul Mincio | 2 |
| Bois de Bovolone (4) ⚠️ | Bovolone | 2 |
| Forêt de Erbezzo (198) ⚠️ | Erbezzo | 2 |
| Bois de Legnago (11) ⚠️ | Legnago | 2 |
| Pioppeto ⚠️ | San Pietro di Morubio | 2 |
| Parc de Bardolino (6) ⚠️ | Bardolino | 2 |
| Bois de Roverchiara ⚠️ | Roverchiara | 2 |
| Bois de Costermano sul Garda (2) ⚠️ | Costermano sul Garda | 2 |
| Forêt de Cerea (10) ⚠️ | Cerea | 2 |
| Parc de Bussolengo (9) ⚠️ | Bussolengo | 2 |
| Bois de Roverè Veronese (3) ⚠️ | Roverè Veronese | 2 |
| Parc de San Pietro di Morubio (6) ⚠️ | San Pietro di Morubio | 2 |
| Forêt de Badia Calavena (30) ⚠️ | Badia Calavena | 2 |
| Forêt de Badia Calavena (32) ⚠️ | Badia Calavena | 2 |
| Forêt de Badia Calavena (36) ⚠️ | Badia Calavena | 2 |
| Forêt de Badia Calavena (39) ⚠️ | Badia Calavena | 2 |
| Forêt de Badia Calavena (56) ⚠️ | Badia Calavena | 2 |
| Forêt de Badia Calavena (64) ⚠️ | Badia Calavena | 2 |
| Forêt de Badia Calavena (66) ⚠️ | Badia Calavena | 2 |
| Forêt de Badia Calavena (71) ⚠️ | Badia Calavena | 2 |
| Forêt de Badia Calavena (81) ⚠️ | Badia Calavena | 2 |
| Forêt de Badia Calavena (86) ⚠️ | Badia Calavena | 2 |
| Forêt de Badia Calavena (95) ⚠️ | Badia Calavena | 2 |
| Forêt de Badia Calavena (99) ⚠️ | Badia Calavena | 2 |
| Forêt de Badia Calavena (105) ⚠️ | Badia Calavena | 2 |
| Forêt de Badia Calavena (109) ⚠️ | Badia Calavena | 2 |
| Forêt de Badia Calavena (112) ⚠️ | Badia Calavena | 2 |
| Forêt de Badia Calavena (114) ⚠️ | Badia Calavena | 2 |
| Forêt de Badia Calavena (125) ⚠️ | Badia Calavena | 2 |
| Forêt de Badia Calavena (127) ⚠️ | Badia Calavena | 2 |
| Forêt de Badia Calavena (130) ⚠️ | Badia Calavena | 2 |
| Forêt de Badia Calavena (131) ⚠️ | Badia Calavena | 2 |
| Forêt de Badia Calavena (137) ⚠️ | Badia Calavena | 2 |
| Forêt de Badia Calavena (142) ⚠️ | Badia Calavena | 2 |
| Forêt de Badia Calavena (146) ⚠️ | Badia Calavena | 2 |
| Forêt de Badia Calavena (173) ⚠️ | Badia Calavena | 2 |
| Forêt de Badia Calavena (178) ⚠️ | Badia Calavena | 2 |
| Forêt de Badia Calavena (218) ⚠️ | Badia Calavena | 2 |
| Forêt de Tregnago (5) ⚠️ | Tregnago | 2 |
| Forêt de Tregnago (12) ⚠️ | Tregnago | 2 |
| Forêt de Tregnago (20) ⚠️ | Tregnago | 2 |
| Forêt de Tregnago (23) ⚠️ | Tregnago | 2 |
| Forêt de Tregnago (28) ⚠️ | Tregnago | 2 |
| Forêt de Tregnago (39) ⚠️ | Tregnago | 2 |
| Forêt de Tregnago (54) ⚠️ | Tregnago | 2 |
| Forêt de Tregnago (71) ⚠️ | Tregnago | 2 |
| Forêt de Tregnago (95) ⚠️ | Tregnago | 2 |
| Forêt de Tregnago (107) ⚠️ | Tregnago | 2 |
| Forêt de Tregnago (111) ⚠️ | Tregnago | 2 |
| Forêt de Tregnago (114) ⚠️ | Tregnago | 2 |
| Forêt de Tregnago (132) ⚠️ | Tregnago | 2 |
| Forêt de Tregnago (138) ⚠️ | Tregnago | 2 |
| Forêt de Tregnago (143) ⚠️ | Tregnago | 2 |
| Forêt de Sant'Ambrogio di Valpolicella (41) ⚠️ | Sant'Ambrogio di Valpolicella | 2 |
| Bois de Oppeano ⚠️ | Oppeano | 2 |
| Bois de Lazise (28) ⚠️ | Lazise | 2 |
| Bois de Lazise (52) ⚠️ | Lazise | 2 |
| Bois de Lazise (60) ⚠️ | Lazise | 2 |
| Bois de Lazise (61) ⚠️ | Lazise | 2 |
| Bois de Castelnuovo del Garda (11) ⚠️ | Castelnuovo del Garda | 2 |
| Forêt de Roverè Veronese (131) ⚠️ | Roverè Veronese | 2 |
| Bois de San Mauro di Saline ⚠️ | San Mauro di Saline | 2 |
| Forêt de Mezzane di Sotto (38) ⚠️ | Mezzane di Sotto | 2 |
| Bois de Velo Veronese (36) ⚠️ | Velo Veronese | 2 |
| Bois de Roverè Veronese (15) ⚠️ | Roverè Veronese | 2 |
| Bois de San Mauro di Saline (21) ⚠️ | San Mauro di Saline | 2 |
| Bois de Roverè Veronese (17) ⚠️ | Roverè Veronese | 2 |
| Bois de Grezzana (34) ⚠️ | Grezzana | 2 |
| Bois de Roverè Veronese (19) ⚠️ | Roverè Veronese | 2 |
| Bois de Roverè Veronese (20) ⚠️ | Roverè Veronese | 2 |
| Bois de San Mauro di Saline (33) ⚠️ | San Mauro di Saline | 2 |
| Bois de Albaredo d'Adige (7) ⚠️ | Albaredo d'Adige | 2 |
| Bois de Albaredo d'Adige (8) ⚠️ | Albaredo d'Adige | 2 |
| Bois de Legnago (16) ⚠️ | Legnago | 2 |
| Bois de Illasi (3) ⚠️ | Illasi | 2 |
| Bois de Negrar di Valpolicella (14) ⚠️ | Negrar di Valpolicella | 2 |
| Bois de Negrar di Valpolicella (21) ⚠️ | Negrar di Valpolicella | 2 |
| Bois de Grezzana (40) ⚠️ | Grezzana | 2 |
| Bois de Grezzana (41) ⚠️ | Grezzana | 2 |
| Bois de Grezzana (43) ⚠️ | Grezzana | 2 |
| Bois de Mezzane di Sotto (28) ⚠️ | Mezzane di Sotto | 2 |
| Bois de Lazise (108) ⚠️ | Lazise | 2 |
| Bois de Mezzane di Sotto (35) ⚠️ | Mezzane di Sotto | 2 |
| Bois de Mezzane di Sotto (37) ⚠️ | Mezzane di Sotto | 2 |
| Oasi di San Giacomo ⚠️ | Lavagno | 2 |
| Forêt de Brenzone sul Garda (68) ⚠️ | Brenzone sul Garda | 2 |
| Parc de Minerbe (5) ⚠️ | Minerbe | 2 |
| Bois de Roverè Veronese (27) ⚠️ | Roverè Veronese | 2 |
| Bois de Grezzana (51) ⚠️ | Grezzana | 2 |
| Bois de Grezzana (54) ⚠️ | Grezzana | 2 |
| Bois de Roverè Veronese (32) ⚠️ | Roverè Veronese | 2 |
| Bois de Roverè Veronese (34) ⚠️ | Roverè Veronese | 2 |
| Bois de Roverè Veronese (35) ⚠️ | Roverè Veronese | 2 |
| Forêt de Valeggio sul Mincio (35) ⚠️ | Valeggio sul Mincio | 2 |
| Bois de Negrar di Valpolicella (36) ⚠️ | Negrar di Valpolicella | 2 |
| Bois de Grezzana (66) ⚠️ | Grezzana | 2 |
| Forêt de Verona (462) ⚠️ | Verona | 2 |
| Forêt de Verona (473) ⚠️ | Verona | 2 |
| Forêt de Bosco Chiesanuova (387) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de San Giovanni Ilarione (171) ⚠️ | San Giovanni Ilarione | 2 |
| Forêt de San Giovanni Ilarione (172) ⚠️ | San Giovanni Ilarione | 2 |
| Forêt de Caprino Veronese (359) ⚠️ | Caprino Veronese | 2 |
| Forêt de Bosco Chiesanuova (388) ⚠️ | Bosco Chiesanuova | 2 |
| Forêt de Brenzone sul Garda (79) ⚠️ | Brenzone sul Garda | 2 |
| Bois de Valeggio sul Mincio (26) ⚠️ | Valeggio sul Mincio | 2 |
| Forêt de Ferrara di Monte Baldo (159) ⚠️ | Ferrara di Monte Baldo | 2 |
| Forêt de Malcesine (158) ⚠️ | Malcesine | 2 |
| Forêt de Badia Calavena (229) ⚠️ | Badia Calavena | 2 |
| Forêt de Badia Calavena (232) ⚠️ | Badia Calavena | 2 |
| Forêt de Tregnago (195) ⚠️ | Tregnago | 2 |
| Forêt de San Giovanni Ilarione (182) ⚠️ | San Giovanni Ilarione | 2 |
| Parco giochi dell'Amicizia ⚠️ | Verona | 1 |
| Giardini Cantori Veronesi ⚠️ | Verona | 1 |
| Piazza Indipendenza ⚠️ | Verona | 1 |
| Parc de Verona (10) ⚠️ | Verona | 1 |
| Parc de San Giovanni Lupatoto ⚠️ | San Giovanni Lupatoto | 1 |
| Parco Gio Battista Marani ⚠️ | Verona | 1 |
| Parc de Bardolino (2) ⚠️ | Bardolino | 1 |
| Giardini Zardini Gaetano ⚠️ | Verona | 1 |
| Parc de Verona (27) ⚠️ | Verona | 1 |
| Giardini Vaclav Pelisek ⚠️ | Verona | 1 |
| Bois de Legnago (2) ⚠️ | Legnago | 1 |
| Bois de Legnago (3) ⚠️ | Legnago | 1 |
| Bois de Terrazzo ⚠️ | Terrazzo | 1 |
| Bois de Villa Bartolomea ⚠️ | Villa Bartolomea | 1 |
| Parc de San Martino Buon Albergo (3) ⚠️ | San Martino Buon Albergo | 1 |
| Parco dei Cotoni ⚠️ | San Giovanni Lupatoto | 1 |
| Parc de Sommacampagna ⚠️ | Sommacampagna | 1 |
| Parc de Verona (35) ⚠️ | Verona | 1 |
| Parco delle Colombare ⚠️ | Verona | 1 |
| Forêt de Monteforte d'Alpone ⚠️ | Monteforte d'Alpone | 1 |
| Parco Achille Forti ⚠️ | Verona | 1 |
| Forêt de Mezzane di Sotto ⚠️ | Mezzane di Sotto | 1 |
| Forêt de Mezzane di Sotto (2) ⚠️ | Mezzane di Sotto | 1 |
| Forêt de Roverè Veronese ⚠️ | Roverè Veronese | 1 |
| Forêt de Roverè Veronese (2) ⚠️ | Roverè Veronese | 1 |
| Forêt de Roverè Veronese (3) ⚠️ | Roverè Veronese | 1 |
| Forêt de Lavagno (6) ⚠️ | Lavagno | 1 |
| Forêt de Mezzane di Sotto (7) ⚠️ | Mezzane di Sotto | 1 |
| Forêt de Mezzane di Sotto (8) ⚠️ | Mezzane di Sotto | 1 |
| Forêt de Mezzane di Sotto (10) ⚠️ | Mezzane di Sotto | 1 |
| Forêt de Mezzane di Sotto (12) ⚠️ | Mezzane di Sotto | 1 |
| Forêt de Mezzane di Sotto (15) ⚠️ | Mezzane di Sotto | 1 |
| Forêt de Mezzane di Sotto (20) ⚠️ | Mezzane di Sotto | 1 |
| Forêt de San Mauro di Saline (7) ⚠️ | San Mauro di Saline | 1 |
| Forêt de Mezzane di Sotto (30) ⚠️ | Mezzane di Sotto | 1 |
| Forêt de San Mauro di Saline (10) ⚠️ | San Mauro di Saline | 1 |
| Forêt de Roverè Veronese (6) ⚠️ | Roverè Veronese | 1 |
| Forêt de San Martino Buon Albergo (9) ⚠️ | San Martino Buon Albergo | 1 |
| Forêt de Negrar di Valpolicella ⚠️ | Negrar di Valpolicella | 1 |
| Forêt de Grezzana ⚠️ | Grezzana | 1 |
| Forêt de Grezzana (4) ⚠️ | Grezzana | 1 |
| Forêt de Roverè Veronese (11) ⚠️ | Roverè Veronese | 1 |
| Forêt de Negrar di Valpolicella (9) ⚠️ | Negrar di Valpolicella | 1 |
| Forêt de Grezzana (19) ⚠️ | Grezzana | 1 |
| Forêt de Grezzana (24) ⚠️ | Grezzana | 1 |
| Forêt de Grezzana (25) ⚠️ | Grezzana | 1 |
| Forêt de Grezzana (33) ⚠️ | Grezzana | 1 |
| Forêt de Roverè Veronese (15) ⚠️ | Roverè Veronese | 1 |
| Forêt de Grezzana (46) ⚠️ | Grezzana | 1 |
| Forêt de Negrar di Valpolicella (17) ⚠️ | Negrar di Valpolicella | 1 |
| Forêt de Grezzana (50) ⚠️ | Grezzana | 1 |
| Forêt de Grezzana (51) ⚠️ | Grezzana | 1 |
| Forêt de Cerro Veronese (16) ⚠️ | Cerro Veronese | 1 |
| Forêt de Grezzana (53) ⚠️ | Grezzana | 1 |
| Forêt de Roverè Veronese (18) ⚠️ | Roverè Veronese | 1 |
| Forêt de Grezzana (59) ⚠️ | Grezzana | 1 |
| Forêt de Grezzana (60) ⚠️ | Grezzana | 1 |
| Forêt de Negrar di Valpolicella (20) ⚠️ | Negrar di Valpolicella | 1 |
| Forêt de Grezzana (61) ⚠️ | Grezzana | 1 |
| Forêt de Grezzana (62) ⚠️ | Grezzana | 1 |
| Forêt de Grezzana (65) ⚠️ | Grezzana | 1 |
| Forêt de Negrar di Valpolicella (26) ⚠️ | Negrar di Valpolicella | 1 |
| Forêt de Grezzana (74) ⚠️ | Grezzana | 1 |
| Parc de Verona (39) ⚠️ | Verona | 1 |
| Forêt de San Giovanni Lupatoto ⚠️ | San Giovanni Lupatoto | 1 |
| Forêt de Buttapietra (5) ⚠️ | San Giovanni Lupatoto | 1 |
| Bois de San Martino Buon Albergo ⚠️ | San Martino Buon Albergo | 1 |
| Bois de San Martino Buon Albergo (2) ⚠️ | San Martino Buon Albergo | 1 |
| Forêt de San Martino Buon Albergo (13) ⚠️ | San Martino Buon Albergo | 1 |
| Forêt de San Martino Buon Albergo (15) ⚠️ | San Martino Buon Albergo | 1 |
| Forêt de San Martino Buon Albergo (22) ⚠️ | San Martino Buon Albergo | 1 |
| Forêt de San Martino Buon Albergo (26) ⚠️ | San Martino Buon Albergo | 1 |
| Forêt de Lavagno (9) ⚠️ | Lavagno | 1 |
| Forêt de Bussolengo (3) ⚠️ | Bussolengo | 1 |
| Forêt de Bussolengo (6) ⚠️ | Bussolengo | 1 |
| Forêt de Negrar di Valpolicella (39) ⚠️ | Negrar di Valpolicella | 1 |
| Bois de Velo Veronese (2) ⚠️ | Velo Veronese | 1 |
| Forêt de Sant'Ambrogio di Valpolicella ⚠️ | Sant'Ambrogio di Valpolicella | 1 |
| Forêt de Valeggio sul Mincio (2) ⚠️ | Valeggio sul Mincio | 1 |
| Forêt de Valeggio sul Mincio (3) ⚠️ | Valeggio sul Mincio | 1 |
| Forêt de Valeggio sul Mincio (7) ⚠️ | Valeggio sul Mincio | 1 |
| Forêt de Valeggio sul Mincio (10) ⚠️ | Valeggio sul Mincio | 1 |
| Forêt de Valeggio sul Mincio (11) ⚠️ | Valeggio sul Mincio | 1 |
| Forêt de Valeggio sul Mincio (12) ⚠️ | Valeggio sul Mincio | 1 |
| Forêt de Valeggio sul Mincio (16) ⚠️ | Valeggio sul Mincio | 1 |
| Forêt de Sommacampagna (3) ⚠️ | Sommacampagna | 1 |
| Forêt de Sommacampagna (4) ⚠️ | Sommacampagna | 1 |
| Forêt de Sommacampagna (5) ⚠️ | Sommacampagna | 1 |
| Forêt de Villafranca di Verona (3) ⚠️ | Villafranca di Verona | 1 |
| Forêt de Sommacampagna (10) ⚠️ | Sommacampagna | 1 |
| Forêt de Sommacampagna (14) ⚠️ | Sommacampagna | 1 |
| Parc de Lavagno ⚠️ | Lavagno | 1 |
| Forêt de Bussolengo (14) ⚠️ | Bussolengo | 1 |
| Forêt de Sona (6) ⚠️ | Sona | 1 |
| Forêt de Sommacampagna (16) ⚠️ | Sommacampagna | 1 |
| Forêt de Sona (7) ⚠️ | Sona | 1 |
| Forêt de Castel d'Azzano (2) ⚠️ | Castel d'Azzano | 1 |
| Parco Ichenhausen ⚠️ | Valeggio sul Mincio | 1 |
| Parc de Bussolengo (5) ⚠️ | Bussolengo | 1 |
| Parc de Bussolengo (6) ⚠️ | Bussolengo | 1 |
| Parc de San Giovanni Lupatoto (7) ⚠️ | San Giovanni Lupatoto | 1 |
| Parc de Lazise (3) ⚠️ | Lazise | 1 |
| Forêt de Sant'Ambrogio di Valpolicella (7) ⚠️ | Sant'Ambrogio di Valpolicella | 1 |
| Parc de Belfiore (7) ⚠️ | Belfiore | 1 |
| Parc de Zevio (2) ⚠️ | Zevio | 1 |
| Forêt de Marano di Valpolicella ⚠️ | Marano di Valpolicella | 1 |
| Forêt de Negrar di Valpolicella (44) ⚠️ | Negrar di Valpolicella | 1 |
| Forêt de Marano di Valpolicella (4) ⚠️ | Marano di Valpolicella | 1 |
| Forêt de Marano di Valpolicella (7) ⚠️ | Marano di Valpolicella | 1 |
| Forêt de Negrar di Valpolicella (49) ⚠️ | Negrar di Valpolicella | 1 |
| Forêt de Marano di Valpolicella (9) ⚠️ | Marano di Valpolicella | 1 |
| Forêt de Negrar di Valpolicella (52) ⚠️ | Negrar di Valpolicella | 1 |
| Forêt de Negrar di Valpolicella (53) ⚠️ | Negrar di Valpolicella | 1 |
| Forêt de Negrar di Valpolicella (55) ⚠️ | Negrar di Valpolicella | 1 |
| Forêt de Valeggio sul Mincio (19) ⚠️ | Valeggio sul Mincio | 1 |
| Forêt de Grezzana (77) ⚠️ | Grezzana | 1 |
| Forêt de Verona (3) ⚠️ | Verona | 1 |
| Forêt de Grezzana (80) ⚠️ | Grezzana | 1 |
| Parc de San Martino Buon Albergo (6) ⚠️ | San Martino Buon Albergo | 1 |
| Parc de Fumane (2) ⚠️ | Fumane | 1 |
| Parc de Villafranca di Verona (4) ⚠️ | Villafranca di Verona | 1 |
| Forêt de Velo Veronese (7) ⚠️ | Velo Veronese | 1 |
| Forêt de Velo Veronese (8) ⚠️ | Velo Veronese | 1 |
| Forêt de Roverè Veronese (20) ⚠️ | Roverè Veronese | 1 |
| Forêt de Roverè Veronese (23) ⚠️ | Roverè Veronese | 1 |
| Parco Mantegna ⚠️ | Lavagno | 1 |
| Parc de San Martino Buon Albergo (10) ⚠️ | San Martino Buon Albergo | 1 |
| Parco di Villa Gazzola ⚠️ | Villafranca di Verona | 1 |
| Parc de Valeggio sul Mincio ⚠️ | Valeggio sul Mincio | 1 |
| Forêt de Sant'Ambrogio di Valpolicella (14) ⚠️ | Sant'Ambrogio di Valpolicella | 1 |
| Forêt de Rivoli Veronese (6) ⚠️ | Rivoli Veronese | 1 |
| Forêt de Sona (8) ⚠️ | Sona | 1 |
| Forêt de Sant'Anna d'Alfaedo ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Marano di Valpolicella (15) ⚠️ | Marano di Valpolicella | 1 |
| Forêt de Marano di Valpolicella (17) ⚠️ | Negrar di Valpolicella | 1 |
| Forêt de Negrar di Valpolicella (60) ⚠️ | Negrar di Valpolicella | 1 |
| Forêt de Negrar di Valpolicella (61) ⚠️ | Negrar di Valpolicella | 1 |
| Forêt de Marano di Valpolicella (20) ⚠️ | Marano di Valpolicella | 1 |
| Forêt de Cavaion Veronese (3) ⚠️ | Cavaion Veronese | 1 |
| Forêt de Bardolino (2) ⚠️ | Bardolino | 1 |
| Forêt de Affi (3) ⚠️ | Affi | 1 |
| Forêt de Affi (5) ⚠️ | Affi | 1 |
| Forêt de Lazise (2) ⚠️ | Lazise | 1 |
| Forêt de Affi (6) ⚠️ | Affi | 1 |
| Forêt de Costermano sul Garda ⚠️ | Costermano sul Garda | 1 |
| Forêt de Affi (8) ⚠️ | Affi | 1 |
| Forêt de Lazise (3) ⚠️ | Lazise | 1 |
| Forêt de Affi (9) ⚠️ | Affi | 1 |
| Forêt de Pastrengo (4) ⚠️ | Pastrengo | 1 |
| Forêt de Vigasio ⚠️ | Vigasio | 1 |
| Forêt de Vigasio (2) ⚠️ | Vigasio | 1 |
| Forêt de Vigasio (5) ⚠️ | Vigasio | 1 |
| Forêt de Trevenzuolo ⚠️ | Trevenzuolo | 1 |
| Forêt de Trevenzuolo (2) ⚠️ | Trevenzuolo | 1 |
| Forêt de Valeggio sul Mincio (22) ⚠️ | Valeggio sul Mincio | 1 |
| Forêt de Sommacampagna (18) ⚠️ | Sommacampagna | 1 |
| Forêt de Sona (14) ⚠️ | Sona | 1 |
| Forêt de Sommacampagna (21) ⚠️ | Sommacampagna | 1 |
| Forêt de Valeggio sul Mincio (30) ⚠️ | Valeggio sul Mincio | 1 |
| Parco della Fratellanza ⚠️ | Verona | 1 |
| Forêt de Oppeano (3) ⚠️ | Oppeano | 1 |
| Forêt de Oppeano (4) ⚠️ | Oppeano | 1 |
| Parc de San Giovanni Lupatoto (9) ⚠️ | San Giovanni Lupatoto | 1 |
| Forêt de Isola della Scala ⚠️ | Isola della Scala | 1 |
| Forêt de Isola della Scala (10) ⚠️ | Isola della Scala | 1 |
| Forêt de Erbè (2) ⚠️ | Erbè | 1 |
| Forêt de Isola della Scala (11) ⚠️ | Isola della Scala | 1 |
| Forêt de Isola della Scala (13) ⚠️ | Isola della Scala | 1 |
| Forêt de Erbè (3) ⚠️ | Sorgà | 1 |
| Forêt de Sorgà (3) ⚠️ | Sorgà | 1 |
| Forêt de Sorgà (7) ⚠️ | Sorgà | 1 |
| Forêt de Sorgà (8) ⚠️ | Sorgà | 1 |
| Forêt de Nogara (5) ⚠️ | Nogara | 1 |
| Forêt de Nogara (6) ⚠️ | Nogara | 1 |
| Forêt de Nogara (10) ⚠️ | Nogara | 1 |
| Parc de Affi ⚠️ | Affi | 1 |
| Giardini Pubblici "Vittorio Bozzi" ⚠️ | Villafranca di Verona | 1 |
| Parco Stadecken-Elsheim ⚠️ | Bovolone | 1 |
| Bois de Mezzane di Sotto ⚠️ | Mezzane di Sotto | 1 |
| Parc de Cerea (2) ⚠️ | Cerea | 1 |
| Parc de Cerea (5) ⚠️ | Cerea | 1 |
| Parc de Legnago (5) ⚠️ | Legnago | 1 |
| Parc de Legnago (6) ⚠️ | Legnago | 1 |
| Parc de Sommacampagna (2) ⚠️ | Sommacampagna | 1 |
| Forêt de Roverè Veronese (27) ⚠️ | Roverè Veronese | 1 |
| Forêt de Roverè Veronese (31) ⚠️ | Roverè Veronese | 1 |
| Forêt de Roverè Veronese (32) ⚠️ | Roverè Veronese | 1 |
| Forêt de Roverè Veronese (35) ⚠️ | Roverè Veronese | 1 |
| Bois de Castelnuovo del Garda (2) ⚠️ | Castelnuovo del Garda | 1 |
| Forêt de Velo Veronese (11) ⚠️ | Velo Veronese | 1 |
| Forêt de Roverè Veronese (37) ⚠️ | Roverè Veronese | 1 |
| Forêt de Roverè Veronese (40) ⚠️ | Roverè Veronese | 1 |
| Bois de Castelnuovo del Garda (5) ⚠️ | Castelnuovo del Garda | 1 |
| Forêt de Roverè Veronese (42) ⚠️ | Roverè Veronese | 1 |
| Forêt de Roverè Veronese (43) ⚠️ | Roverè Veronese | 1 |
| Forêt de Roverè Veronese (44) ⚠️ | Roverè Veronese | 1 |
| Forêt de Velo Veronese (14) ⚠️ | Velo Veronese | 1 |
| Forêt de Velo Veronese (15) ⚠️ | Velo Veronese | 1 |
| Forêt de Roverè Veronese (46) ⚠️ | Roverè Veronese | 1 |
| Forêt de Roverè Veronese (47) ⚠️ | Roverè Veronese | 1 |
| Forêt de Roverè Veronese (50) ⚠️ | Roverè Veronese | 1 |
| Forêt de Velo Veronese (18) ⚠️ | Velo Veronese | 1 |
| Forêt de Velo Veronese (19) ⚠️ | Velo Veronese | 1 |
| Forêt de Roverè Veronese (55) ⚠️ | Roverè Veronese | 1 |
| Forêt de Roverè Veronese (57) ⚠️ | Roverè Veronese | 1 |
| Forêt de Velo Veronese (26) ⚠️ | Velo Veronese | 1 |
| Forêt de Roverè Veronese (65) ⚠️ | Roverè Veronese | 1 |
| Parc de Cologna Veneta (6) ⚠️ | Cologna Veneta | 1 |
| Parc de Valeggio sul Mincio (11) ⚠️ | Valeggio sul Mincio | 1 |
| Parc de Bardolino (3) ⚠️ | Bardolino | 1 |
| Parc de Verona (45) ⚠️ | Verona | 1 |
| Parc de Villafranca di Verona (14) ⚠️ | Villafranca di Verona | 1 |
| Parc de Villafranca di Verona (15) ⚠️ | Villafranca di Verona | 1 |
| Parc de Verona (46) ⚠️ | Verona | 1 |
| Parc de Villafranca di Verona (19) ⚠️ | Villafranca di Verona | 1 |
| Vecchio Parco San Giacomo ⚠️ | Verona | 1 |
| Parc de Sommacampagna (4) ⚠️ | Sommacampagna | 1 |
| Parco Villa Balladoro ⚠️ | Povegliano Veronese | 1 |
| Giardino della Speranza ⚠️ | Povegliano Veronese | 1 |
| Forêt de Bosco Chiesanuova ⚠️ | Bosco Chiesanuova | 1 |
| Parc de Villafranca di Verona (33) ⚠️ | Villafranca di Verona | 1 |
| Parc de Villafranca di Verona (34) ⚠️ | Villafranca di Verona | 1 |
| Parc de Nogarole Rocca ⚠️ | Nogarole Rocca | 1 |
| Forêt de Bovolone ⚠️ | Bovolone | 1 |
| Forêt de Bovolone (6) ⚠️ | Bovolone | 1 |
| Parc de Bovolone (7) ⚠️ | Bovolone | 1 |
| Parc de Bovolone (11) ⚠️ | Bovolone | 1 |
| Forêt de Erbezzo ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (2) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (3) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (4) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (12) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (14) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (22) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (32) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (33) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (40) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (46) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (47) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (48) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (50) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (53) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (56) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (58) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (59) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (60) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (63) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (64) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (68) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (70) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (71) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (74) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (75) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (79) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (81) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (83) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (88) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (90) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (91) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (94) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (95) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (96) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (99) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (100) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (102) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (111) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (114) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (115) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (117) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (118) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (126) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (128) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (129) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (130) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (133) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (136) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (137) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (139) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (141) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (142) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (143) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (144) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (145) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (146) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (148) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (152) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (159) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (160) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (162) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (164) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (165) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (169) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (172) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (176) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (177) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (183) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (186) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (188) ⚠️ | Erbezzo | 1 |
| Forêt de Erbezzo (193) ⚠️ | Erbezzo | 1 |
| Parc de Terrazzo ⚠️ | Terrazzo | 1 |
| Parco Europa ⚠️ | Grezzana | 1 |
| Parc de Verona (50) ⚠️ | Verona | 1 |
| Forêt de Sant'Anna d'Alfaedo (7) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (10) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (15) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (21) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (24) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (25) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (27) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Erbezzo (197) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (55) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (60) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Dolcè ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (63) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (64) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (65) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (66) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (68) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (70) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (72) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (75) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (76) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (79) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (85) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (86) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (89) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (90) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (91) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (93) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (96) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (97) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (101) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (103) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (106) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (113) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (127) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (135) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (136) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (138) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (145) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (146) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (154) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (155) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (156) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (158) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (160) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (162) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (165) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (166) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (167) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (169) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (171) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (172) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (174) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (175) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (180) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (181) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (187) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (190) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (191) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (192) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (197) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (203) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (205) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (206) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (207) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (208) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (209) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (210) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (211) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (212) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (216) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (217) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (218) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (219) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (221) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (223) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (224) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (227) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (229) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (234) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (242) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (254) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (257) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Sant'Anna d'Alfaedo (258) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Bosco Chiesanuova (5) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (8) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (9) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (10) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (20) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (23) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (24) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (26) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (27) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (29) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (30) ⚠️ | Roverè Veronese | 1 |
| Forêt de Bosco Chiesanuova (36) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (37) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (39) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (40) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (41) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (43) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (45) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (53) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (56) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (57) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (60) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (62) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (64) ⚠️ | Roverè Veronese | 1 |
| Forêt de Bosco Chiesanuova (71) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (73) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (76) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (78) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (85) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (86) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (93) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (100) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (101) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (107) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (114) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (115) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (116) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Roverè Veronese (76) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (117) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (118) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (125) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (130) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (134) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (136) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (137) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (138) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (140) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (142) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (143) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (144) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (146) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (148) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (150) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (158) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (164) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (165) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (168) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (169) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (172) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (173) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (177) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (178) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (181) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (182) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (184) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (185) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (186) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (188) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (189) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Roverè Veronese (77) ⚠️ | Roverè Veronese | 1 |
| Forêt de Bosco Chiesanuova (191) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (193) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (196) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (197) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (198) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (200) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (210) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (213) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (215) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (219) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (221) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (227) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (230) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (232) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (236) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (240) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (243) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (244) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (250) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (252) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (255) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (256) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (257) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (258) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (263) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (269) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (270) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (281) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (283) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (285) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (286) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (291) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (292) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (295) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (300) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (301) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (303) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (305) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (306) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (309) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (311) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (314) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (318) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (320) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (321) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (323) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (326) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (335) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (339) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (354) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (360) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (361) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Bosco Chiesanuova (362) ⚠️ | Bosco Chiesanuova | 1 |
| Parco di Villa Rizzardi ⚠️ | Negrar di Valpolicella | 1 |
| Forêt de Negrar di Valpolicella (67) ⚠️ | Negrar di Valpolicella | 1 |
| Parc de Villafranca di Verona (37) ⚠️ | Villafranca di Verona | 1 |
| Forêt de Verona (12) ⚠️ | Verona | 1 |
| Forêt de Verona (13) ⚠️ | Verona | 1 |
| Forêt de Verona (17) ⚠️ | Verona | 1 |
| Forêt de Verona (18) ⚠️ | Verona | 1 |
| Forêt de Verona (20) ⚠️ | Verona | 1 |
| Forêt de Verona (24) ⚠️ | Verona | 1 |
| Forêt de Verona (26) ⚠️ | Verona | 1 |
| Forêt de Verona (30) ⚠️ | Verona | 1 |
| Forêt de Verona (32) ⚠️ | Verona | 1 |
| Parc de Verona (59) ⚠️ | Verona | 1 |
| Parco unità d'Italia ⚠️ | Gazzo Veronese | 1 |
| Parc de Verona (60) ⚠️ | Verona | 1 |
| Forêt de Verona (35) ⚠️ | Verona | 1 |
| Forêt de Verona (37) ⚠️ | Verona | 1 |
| Forêt de Verona (43) ⚠️ | Verona | 1 |
| Parc de Verona (61) ⚠️ | Verona | 1 |
| Forêt de Verona (47) ⚠️ | Verona | 1 |
| Forêt de Verona (51) ⚠️ | Verona | 1 |
| Forêt de Verona (54) ⚠️ | Verona | 1 |
| Forêt de Verona (56) ⚠️ | Verona | 1 |
| Forêt de Verona (57) ⚠️ | Verona | 1 |
| Forêt de Verona (58) ⚠️ | Verona | 1 |
| Forêt de Verona (61) ⚠️ | Verona | 1 |
| Forêt de Verona (62) ⚠️ | Verona | 1 |
| Parc de Verona (62) ⚠️ | Verona | 1 |
| Forêt de Verona (64) ⚠️ | Verona | 1 |
| Forêt de Verona (73) ⚠️ | Verona | 1 |
| Forêt de Verona (75) ⚠️ | Verona | 1 |
| Bois de Valeggio sul Mincio ⚠️ | Valeggio sul Mincio | 1 |
| Forêt de Verona (77) ⚠️ | Verona | 1 |
| Forêt de Verona (85) ⚠️ | Verona | 1 |
| Forêt de Verona (90) ⚠️ | Verona | 1 |
| Forêt de Verona (92) ⚠️ | Verona | 1 |
| Forêt de Verona (94) ⚠️ | Verona | 1 |
| Parc de Verona (68) ⚠️ | Verona | 1 |
| Forêt de Verona (100) ⚠️ | Verona | 1 |
| Forêt de Verona (101) ⚠️ | Verona | 1 |
| Forêt de Verona (103) ⚠️ | Verona | 1 |
| Forêt de Verona (105) ⚠️ | Verona | 1 |
| Forêt de Verona (111) ⚠️ | Verona | 1 |
| Forêt de Verona (113) ⚠️ | Verona | 1 |
| Forêt de Verona (115) ⚠️ | Verona | 1 |
| Parc de Verona (70) ⚠️ | Verona | 1 |
| Forêt de Verona (116) ⚠️ | Verona | 1 |
| Forêt de Verona (117) ⚠️ | Verona | 1 |
| Forêt de Verona (123) ⚠️ | Verona | 1 |
| Forêt de Verona (130) ⚠️ | Verona | 1 |
| Forêt de Verona (133) ⚠️ | Verona | 1 |
| Forêt de Verona (134) ⚠️ | Verona | 1 |
| Forêt de Verona (135) ⚠️ | Verona | 1 |
| Forêt de Verona (136) ⚠️ | Verona | 1 |
| Forêt de Verona (142) ⚠️ | Verona | 1 |
| Forêt de Verona (150) ⚠️ | Verona | 1 |
| Forêt de Verona (151) ⚠️ | Verona | 1 |
| Forêt de Verona (156) ⚠️ | Verona | 1 |
| Forêt de Verona (157) ⚠️ | Verona | 1 |
| Forêt de Verona (161) ⚠️ | Verona | 1 |
| Forêt de Verona (165) ⚠️ | Verona | 1 |
| Forêt de Verona (167) ⚠️ | Verona | 1 |
| Forêt de Verona (170) ⚠️ | Verona | 1 |
| Forêt de Verona (171) ⚠️ | Verona | 1 |
| Forêt de Verona (172) ⚠️ | Verona | 1 |
| Forêt de Verona (173) ⚠️ | Verona | 1 |
| Forêt de Verona (174) ⚠️ | Verona | 1 |
| Forêt de Verona (175) ⚠️ | Verona | 1 |
| Forêt de Verona (177) ⚠️ | Verona | 1 |
| Forêt de Verona (178) ⚠️ | Verona | 1 |
| Parc de Mozzecane (16) ⚠️ | Mozzecane | 1 |
| Forêt de Verona (182) ⚠️ | Verona | 1 |
| Forêt de Verona (183) ⚠️ | Verona | 1 |
| Forêt de Verona (184) ⚠️ | Verona | 1 |
| Forêt de Verona (187) ⚠️ | Verona | 1 |
| Forêt de Verona (191) ⚠️ | Verona | 1 |
| Forêt de Verona (192) ⚠️ | Verona | 1 |
| Forêt de Verona (194) ⚠️ | Verona | 1 |
| Forêt de Verona (200) ⚠️ | Verona | 1 |
| Forêt de Verona (201) ⚠️ | Verona | 1 |
| Forêt de Verona (202) ⚠️ | Verona | 1 |
| Parc de Verona (73) ⚠️ | Verona | 1 |
| Forêt de Verona (205) ⚠️ | Verona | 1 |
| Parc de Verona (74) ⚠️ | Verona | 1 |
| Parc de Verona (76) ⚠️ | Verona | 1 |
| Forêt de Verona (209) ⚠️ | Verona | 1 |
| Parc de Verona (79) ⚠️ | Verona | 1 |
| Forêt de Verona (215) ⚠️ | Verona | 1 |
| Parc de Verona (84) ⚠️ | Verona | 1 |
| Parc de Verona (85) ⚠️ | Verona | 1 |
| Forêt de Verona (222) ⚠️ | Verona | 1 |
| Bois de Verona (4) ⚠️ | Verona | 1 |
| Forêt de Verona (225) ⚠️ | Verona | 1 |
| Parc de Verona (88) ⚠️ | Verona | 1 |
| Forêt de Verona (231) ⚠️ | Verona | 1 |
| Forêt de Verona (233) ⚠️ | Verona | 1 |
| Forêt de Verona (236) ⚠️ | Verona | 1 |
| Forêt de Verona (243) ⚠️ | Verona | 1 |
| Forêt de Verona (247) ⚠️ | Verona | 1 |
| Forêt de Velo Veronese (29) ⚠️ | Velo Veronese | 1 |
| Forêt de Verona (248) ⚠️ | Verona | 1 |
| Forêt de Verona (252) ⚠️ | Verona | 1 |
| Forêt de Verona (254) ⚠️ | Verona | 1 |
| Forêt de Verona (255) ⚠️ | Verona | 1 |
| Forêt de Verona (261) ⚠️ | Verona | 1 |
| Forêt de Verona (264) ⚠️ | Verona | 1 |
| Forêt de Verona (269) ⚠️ | Verona | 1 |
| Parc de Malcesine ⚠️ | Malcesine | 1 |
| Forêt de Verona (277) ⚠️ | Verona | 1 |
| Forêt de Verona (278) ⚠️ | Verona | 1 |
| Forêt de Verona (280) ⚠️ | Verona | 1 |
| Forêt de Valeggio sul Mincio (33) ⚠️ | Valeggio sul Mincio | 1 |
| Forêt de Verona (281) ⚠️ | Verona | 1 |
| Forêt de Verona (292) ⚠️ | Verona | 1 |
| Forêt de Verona (296) ⚠️ | Verona | 1 |
| Forêt de Verona (303) ⚠️ | Verona | 1 |
| Forêt de Verona (305) ⚠️ | Verona | 1 |
| Forêt de Verona (307) ⚠️ | Verona | 1 |
| Forêt de Verona (308) ⚠️ | Verona | 1 |
| Forêt de Verona (309) ⚠️ | Verona | 1 |
| Forêt de Verona (312) ⚠️ | Verona | 1 |
| Forêt de Verona (313) ⚠️ | Verona | 1 |
| Forêt de Verona (320) ⚠️ | Verona | 1 |
| Forêt de Verona (322) ⚠️ | Verona | 1 |
| Forêt de Verona (323) ⚠️ | Verona | 1 |
| Forêt de Verona (324) ⚠️ | Verona | 1 |
| Forêt de Verona (328) ⚠️ | Verona | 1 |
| Forêt de Verona (333) ⚠️ | Verona | 1 |
| Forêt de Verona (341) ⚠️ | Verona | 1 |
| Parc de Verona (98) ⚠️ | Verona | 1 |
| Bois de Verona (6) ⚠️ | Verona | 1 |
| Forêt de Verona (345) ⚠️ | Verona | 1 |
| Forêt de Verona (346) ⚠️ | Verona | 1 |
| Parc de Verona (100) ⚠️ | Verona | 1 |
| Forêt de Verona (350) ⚠️ | Verona | 1 |
| Forêt de Verona (362) ⚠️ | Verona | 1 |
| Forêt de Verona (370) ⚠️ | Grezzana | 1 |
| Forêt de Verona (373) ⚠️ | Verona | 1 |
| Forêt de Verona (374) ⚠️ | Verona | 1 |
| Forêt de Verona (382) ⚠️ | Verona | 1 |
| Forêt de Verona (384) ⚠️ | Verona | 1 |
| Forêt de Verona (389) ⚠️ | Verona | 1 |
| Forêt de Verona (390) ⚠️ | Verona | 1 |
| Forêt de Verona (398) ⚠️ | Verona | 1 |
| Forêt de Verona (399) ⚠️ | Verona | 1 |
| Forêt de Verona (402) ⚠️ | Verona | 1 |
| Forêt de Verona (403) ⚠️ | Verona | 1 |
| Forêt de Verona (405) ⚠️ | Verona | 1 |
| Forêt de Verona (417) ⚠️ | Verona | 1 |
| Forêt de Verona (422) ⚠️ | Verona | 1 |
| Forêt de Verona (423) ⚠️ | Verona | 1 |
| Forêt de Verona (425) ⚠️ | Verona | 1 |
| Forêt de Verona (427) ⚠️ | Verona | 1 |
| Parc de Concamarise ⚠️ | Concamarise | 1 |
| Parco di Via Trieste ⚠️ | Zevio | 1 |
| Parc de Verona (102) ⚠️ | Verona | 1 |
| Bois de Legnago (6) ⚠️ | Legnago | 1 |
| Paludi di Ostiglia ⚠️ | Gazzo Veronese | 1 |
| Parc de Isola della Scala (11) ⚠️ | Isola della Scala | 1 |
| Parc de Pressana (2) ⚠️ | Pressana | 1 |
| Area Verde ⚠️ | San Bonifacio | 1 |
| Parc de San Pietro di Morubio (4) ⚠️ | San Pietro di Morubio | 1 |
| Forêt de Verona (432) ⚠️ | Verona | 1 |
| Parc de Verona (106) ⚠️ | Verona | 1 |
| Forêt de Malcesine (2) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (4) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (6) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (11) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (12) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (16) ⚠️ | Malcesine | 1 |
| Forêt de Torri del Benaco ⚠️ | Torri del Benaco | 1 |
| Forêt de Torri del Benaco (7) ⚠️ | Torri del Benaco | 1 |
| Forêt de Torri del Benaco (13) ⚠️ | Torri del Benaco | 1 |
| Forêt de Torri del Benaco (14) ⚠️ | Torri del Benaco | 1 |
| Forêt de Torri del Benaco (16) ⚠️ | Torri del Benaco | 1 |
| Forêt de Torri del Benaco (18) ⚠️ | Torri del Benaco | 1 |
| Forêt de Torri del Benaco (22) ⚠️ | Torri del Benaco | 1 |
| Forêt de Torri del Benaco (25) ⚠️ | Torri del Benaco | 1 |
| Forêt de Torri del Benaco (28) ⚠️ | Torri del Benaco | 1 |
| Forêt de Torri del Benaco (29) ⚠️ | Torri del Benaco | 1 |
| Forêt de San Zeno di Montagna (2) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (4) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (11) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (12) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (22) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (25) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (27) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (34) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (36) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (41) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (42) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (43) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (44) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (48) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (51) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (52) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (54) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (61) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (64) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (65) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (68) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (70) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (73) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (78) ⚠️ | Brenzone sul Garda | 1 |
| Forêt de San Zeno di Montagna (84) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (85) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (86) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (92) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (96) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (97) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (98) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (100) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (101) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (103) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (104) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (112) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de Caprino Veronese (3) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (4) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (8) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (12) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (15) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (20) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (22) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (23) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (25) ⚠️ | Caprino Veronese | 1 |
| Parc de Caprino Veronese (5) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (26) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (28) ⚠️ | Caprino Veronese | 1 |
| Forêt de San Zeno di Montagna (116) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de Caprino Veronese (36) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (41) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (42) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (45) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (50) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (52) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (54) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (60) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (62) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (70) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (72) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (86) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (89) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (90) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (93) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (94) ⚠️ | Caprino Veronese | 1 |
| Forêt de Rivoli Veronese (13) ⚠️ | Rivoli Veronese | 1 |
| Forêt de Caprino Veronese (99) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (101) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (102) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (104) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (107) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (108) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (109) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (113) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (116) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (121) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (123) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (124) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (125) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (127) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (128) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (133) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (134) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (136) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (139) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (141) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (145) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (147) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (149) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (151) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (153) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (156) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (157) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (165) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (171) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (175) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (177) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (178) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (183) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (185) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (189) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (190) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (195) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (206) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (207) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (210) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (212) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (218) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (225) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (227) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (228) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (231) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (232) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (238) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (244) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (245) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (246) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (247) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (249) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (259) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (260) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (265) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (271) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (272) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (273) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (274) ⚠️ | Caprino Veronese | 1 |
| Forêt de Brenzone sul Garda (6) ⚠️ | Brenzone sul Garda | 1 |
| Forêt de Brenzone sul Garda (10) ⚠️ | Brenzone sul Garda | 1 |
| Forêt de Brenzone sul Garda (12) ⚠️ | Brenzone sul Garda | 1 |
| Forêt de Brenzone sul Garda (16) ⚠️ | Brenzone sul Garda | 1 |
| Forêt de Brenzone sul Garda (21) ⚠️ | Brenzone sul Garda | 1 |
| Forêt de Brenzone sul Garda (23) ⚠️ | Brenzone sul Garda | 1 |
| Forêt de Brenzone sul Garda (33) ⚠️ | Brenzone sul Garda | 1 |
| Forêt de Brenzone sul Garda (34) ⚠️ | Brenzone sul Garda | 1 |
| Forêt de Brenzone sul Garda (36) ⚠️ | Brenzone sul Garda | 1 |
| Forêt de Brenzone sul Garda (39) ⚠️ | Brenzone sul Garda | 1 |
| Forêt de Brenzone sul Garda (41) ⚠️ | Brenzone sul Garda | 1 |
| Forêt de Brenzone sul Garda (46) ⚠️ | Brenzone sul Garda | 1 |
| Forêt de Brenzone sul Garda (54) ⚠️ | Brenzone sul Garda | 1 |
| Forêt de Brenzone sul Garda (56) ⚠️ | Brenzone sul Garda | 1 |
| Forêt de Brenzone sul Garda (57) ⚠️ | Brenzone sul Garda | 1 |
| Forêt de Ferrara di Monte Baldo (16) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Ferrara di Monte Baldo (19) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Ferrara di Monte Baldo (22) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Ferrara di Monte Baldo (26) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Ferrara di Monte Baldo (27) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Ferrara di Monte Baldo (29) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Ferrara di Monte Baldo (30) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Ferrara di Monte Baldo (35) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Ferrara di Monte Baldo (40) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Ferrara di Monte Baldo (41) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Ferrara di Monte Baldo (45) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Ferrara di Monte Baldo (47) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Ferrara di Monte Baldo (48) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Ferrara di Monte Baldo (51) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Ferrara di Monte Baldo (55) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Ferrara di Monte Baldo (58) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Ferrara di Monte Baldo (61) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Ferrara di Monte Baldo (70) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Ferrara di Monte Baldo (73) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Ferrara di Monte Baldo (80) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Ferrara di Monte Baldo (82) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Ferrara di Monte Baldo (84) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Ferrara di Monte Baldo (87) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Ferrara di Monte Baldo (90) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Ferrara di Monte Baldo (96) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Ferrara di Monte Baldo (102) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Ferrara di Monte Baldo (106) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Fumane (5) ⚠️ | Fumane | 1 |
| Forêt de Fumane (14) ⚠️ | Fumane | 1 |
| Forêt de Fumane (17) ⚠️ | Fumane | 1 |
| Forêt de Fumane (20) ⚠️ | Fumane | 1 |
| Forêt de Fumane (21) ⚠️ | Fumane | 1 |
| Forêt de Sant'Anna d'Alfaedo (261) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Forêt de Fumane (24) ⚠️ | Fumane | 1 |
| Forêt de Fumane (26) ⚠️ | Fumane | 1 |
| Forêt de Fumane (30) ⚠️ | Fumane | 1 |
| Forêt de Fumane (34) ⚠️ | Fumane | 1 |
| Forêt de Fumane (36) ⚠️ | Fumane | 1 |
| Forêt de Fumane (37) ⚠️ | Fumane | 1 |
| Forêt de Marano di Valpolicella (23) ⚠️ | Marano di Valpolicella | 1 |
| Forêt de Fumane (45) ⚠️ | Fumane | 1 |
| Forêt de Fumane (46) ⚠️ | Fumane | 1 |
| Forêt de Fumane (53) ⚠️ | Fumane | 1 |
| Forêt de Fumane (55) ⚠️ | Fumane | 1 |
| Forêt de Brentino Belluno (3) ⚠️ | Brentino Belluno | 1 |
| Forêt de Brentino Belluno (4) ⚠️ | Brentino Belluno | 1 |
| Forêt de Brentino Belluno (7) ⚠️ | Brentino Belluno | 1 |
| Forêt de Brentino Belluno (14) ⚠️ | Brentino Belluno | 1 |
| Forêt de Brentino Belluno (15) ⚠️ | Brentino Belluno | 1 |
| Forêt de Brentino Belluno (16) ⚠️ | Brentino Belluno | 1 |
| Forêt de Brentino Belluno (18) ⚠️ | Brentino Belluno | 1 |
| Forêt de Brentino Belluno (20) ⚠️ | Brentino Belluno | 1 |
| Forêt de Brentino Belluno (25) ⚠️ | Brentino Belluno | 1 |
| Forêt de Brentino Belluno (27) ⚠️ | Brentino Belluno | 1 |
| Forêt de Brentino Belluno (29) ⚠️ | Brentino Belluno | 1 |
| Forêt de Brentino Belluno (36) ⚠️ | Brentino Belluno | 1 |
| Forêt de Brentino Belluno (38) ⚠️ | Brentino Belluno | 1 |
| Forêt de Brentino Belluno (40) ⚠️ | Brentino Belluno | 1 |
| Forêt de Brentino Belluno (43) ⚠️ | Brentino Belluno | 1 |
| Forêt de Brentino Belluno (46) ⚠️ | Brentino Belluno | 1 |
| Forêt de Brentino Belluno (47) ⚠️ | Brentino Belluno | 1 |
| Forêt de Brentino Belluno (48) ⚠️ | Brentino Belluno | 1 |
| Forêt de Brentino Belluno (50) ⚠️ | Brentino Belluno | 1 |
| Forêt de Brentino Belluno (51) ⚠️ | Brentino Belluno | 1 |
| Forêt de Brentino Belluno (59) ⚠️ | Brentino Belluno | 1 |
| Forêt de Brentino Belluno (60) ⚠️ | Brentino Belluno | 1 |
| Forêt de Dolcè (4) ⚠️ | Dolcè | 1 |
| Prà della Fiera ⚠️ | Cerea | 1 |
| Forêt de Fumane (57) ⚠️ | Fumane | 1 |
| Forêt de Fumane (61) ⚠️ | Fumane | 1 |
| Forêt de Fumane (67) ⚠️ | Fumane | 1 |
| Forêt de Fumane (69) ⚠️ | Fumane | 1 |
| Forêt de Fumane (72) ⚠️ | Fumane | 1 |
| Forêt de Fumane (78) ⚠️ | Fumane | 1 |
| Forêt de Fumane (80) ⚠️ | Fumane | 1 |
| Forêt de Fumane (84) ⚠️ | Fumane | 1 |
| Forêt de Fumane (87) ⚠️ | Fumane | 1 |
| Forêt de Malcesine (20) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (22) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (23) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (25) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (27) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (36) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (37) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (38) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (39) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (46) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (47) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (62) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (64) ⚠️ | Malcesine | 1 |
| Parc de Malcesine (4) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (78) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (79) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (80) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (82) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (83) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (88) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (90) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (93) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (94) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (95) ⚠️ | Malcesine | 1 |
| Parc de Malcesine (6) ⚠️ | Malcesine | 1 |
| Parc de Malcesine (8) ⚠️ | Malcesine | 1 |
| Parc de Malcesine (9) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (102) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (106) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (107) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (111) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (115) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (116) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (125) ⚠️ | Malcesine | 1 |
| Forêt de Malcesine (132) ⚠️ | Malcesine | 1 |
| Parc de Isola della Scala (12) ⚠️ | Isola della Scala | 1 |
| Forêt de Fumane (90) ⚠️ | Fumane | 1 |
| Forêt de Fumane (91) ⚠️ | Fumane | 1 |
| Forêt de Fumane (94) ⚠️ | Fumane | 1 |
| Forêt de Fumane (95) ⚠️ | Fumane | 1 |
| Forêt de Fumane (97) ⚠️ | Fumane | 1 |
| Forêt de Fumane (98) ⚠️ | Fumane | 1 |
| Forêt de Fumane (104) ⚠️ | Fumane | 1 |
| Forêt de Fumane (108) ⚠️ | Fumane | 1 |
| Forêt de Fumane (120) ⚠️ | Fumane | 1 |
| Forêt de Costermano sul Garda (4) ⚠️ | Costermano sul Garda | 1 |
| Parc de Fumane (7) ⚠️ | Fumane | 1 |
| Forêt de Fumane (124) ⚠️ | Fumane | 1 |
| Forêt de Fumane (126) ⚠️ | Fumane | 1 |
| Forêt de Fumane (130) ⚠️ | Fumane | 1 |
| Forêt de Fumane (141) ⚠️ | Fumane | 1 |
| Forêt de Fumane (147) ⚠️ | Fumane | 1 |
| Forêt de Fumane (150) ⚠️ | Fumane | 1 |
| Forêt de Fumane (155) ⚠️ | Fumane | 1 |
| Forêt de San Zeno di Montagna (122) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de Dolcè (20) ⚠️ | Dolcè | 1 |
| Forêt de San Zeno di Montagna (123) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (125) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de Dolcè (22) ⚠️ | Dolcè | 1 |
| Forêt de Dolcè (23) ⚠️ | Dolcè | 1 |
| Forêt de San Zeno di Montagna (138) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (142) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (148) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (154) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (165) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de Dolcè (27) ⚠️ | Dolcè | 1 |
| Forêt de Dolcè (28) ⚠️ | Dolcè | 1 |
| Forêt de Dolcè (32) ⚠️ | Dolcè | 1 |
| Forêt de Dolcè (34) ⚠️ | Dolcè | 1 |
| Forêt de Dolcè (35) ⚠️ | Dolcè | 1 |
| Forêt de Dolcè (39) ⚠️ | Dolcè | 1 |
| Forêt de Dolcè (41) ⚠️ | Dolcè | 1 |
| Forêt de Dolcè (45) ⚠️ | Dolcè | 1 |
| Forêt de Fumane (157) ⚠️ | Fumane | 1 |
| Forêt de Dolcè (48) ⚠️ | Dolcè | 1 |
| Forêt de Dolcè (52) ⚠️ | Dolcè | 1 |
| Forêt de Caprino Veronese (284) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (285) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (290) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (291) ⚠️ | Caprino Veronese | 1 |
| Forêt de Sant'Ambrogio di Valpolicella (17) ⚠️ | Sant'Ambrogio di Valpolicella | 1 |
| Forêt de Dolcè (54) ⚠️ | Dolcè | 1 |
| Forêt de Dolcè (60) ⚠️ | Dolcè | 1 |
| Forêt de Dolcè (67) ⚠️ | Dolcè | 1 |
| Forêt de Dolcè (71) ⚠️ | Dolcè | 1 |
| Forêt de Fumane (159) ⚠️ | Fumane | 1 |
| Forêt de Fumane (165) ⚠️ | Fumane | 1 |
| Forêt de Fumane (168) ⚠️ | Fumane | 1 |
| Parc de Verona (109) ⚠️ | Verona | 1 |
| Bois de Valeggio sul Mincio (4) ⚠️ | Valeggio sul Mincio | 1 |
| Forêt de Fumane (171) ⚠️ | Fumane | 1 |
| Forêt de Marano di Valpolicella (29) ⚠️ | Marano di Valpolicella | 1 |
| Forêt de Marano di Valpolicella (31) ⚠️ | Marano di Valpolicella | 1 |
| Forêt de Marano di Valpolicella (32) ⚠️ | Marano di Valpolicella | 1 |
| Forêt de Costermano sul Garda (6) ⚠️ | Costermano sul Garda | 1 |
| Forêt de Torri del Benaco (33) ⚠️ | Torri del Benaco | 1 |
| Forêt de Costermano sul Garda (10) ⚠️ | Costermano sul Garda | 1 |
| Forêt de Costermano sul Garda (15) ⚠️ | Costermano sul Garda | 1 |
| Forêt de San Zeno di Montagna (168) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de Costermano sul Garda (26) ⚠️ | Costermano sul Garda | 1 |
| Forêt de Costermano sul Garda (28) ⚠️ | Costermano sul Garda | 1 |
| Forêt de Caprino Veronese (299) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (300) ⚠️ | Caprino Veronese | 1 |
| Forêt de Lazise (13) ⚠️ | Lazise | 1 |
| Forêt de Caprino Veronese (309) ⚠️ | Caprino Veronese | 1 |
| Forêt de San Zeno di Montagna (172) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (186) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (188) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (190) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (191) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (203) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (204) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de San Zeno di Montagna (207) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de Caprino Veronese (330) ⚠️ | Caprino Veronese | 1 |
| Forêt de Costermano sul Garda (36) ⚠️ | Costermano sul Garda | 1 |
| Forêt de Costermano sul Garda (37) ⚠️ | Costermano sul Garda | 1 |
| Forêt de Costermano sul Garda (38) ⚠️ | Costermano sul Garda | 1 |
| Forêt de Costermano sul Garda (39) ⚠️ | Costermano sul Garda | 1 |
| Forêt de Costermano sul Garda (40) ⚠️ | Costermano sul Garda | 1 |
| Forêt de Costermano sul Garda (45) ⚠️ | Costermano sul Garda | 1 |
| Forêt de Cerea (6) ⚠️ | Cerea | 1 |
| Forêt de Fumane (176) ⚠️ | Fumane | 1 |
| Forêt de Fumane (177) ⚠️ | Fumane | 1 |
| Forêt de Fumane (190) ⚠️ | Fumane | 1 |
| Forêt de Fumane (194) ⚠️ | Fumane | 1 |
| Forêt de Sant'Ambrogio di Valpolicella (33) ⚠️ | Sant'Ambrogio di Valpolicella | 1 |
| Forêt de Sant'Ambrogio di Valpolicella (36) ⚠️ | Sant'Ambrogio di Valpolicella | 1 |
| Forêt de Dolcè (72) ⚠️ | Dolcè | 1 |
| Forêt de Rivoli Veronese (14) ⚠️ | Rivoli Veronese | 1 |
| Forêt de Dolcè (75) ⚠️ | Dolcè | 1 |
| Forêt de Rivoli Veronese (16) ⚠️ | Rivoli Veronese | 1 |
| Forêt de Brentino Belluno (67) ⚠️ | Brentino Belluno | 1 |
| Forêt de Rivoli Veronese (18) ⚠️ | Rivoli Veronese | 1 |
| Forêt de Rivoli Veronese (20) ⚠️ | Rivoli Veronese | 1 |
| Forêt de Ferrara di Monte Baldo (112) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Ferrara di Monte Baldo (115) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Ferrara di Monte Baldo (117) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Ferrara di Monte Baldo (131) ⚠️ | Ferrara di Monte Baldo | 1 |
| Forêt de Ferrara di Monte Baldo (136) ⚠️ | Ferrara di Monte Baldo | 1 |
| Parc de San Pietro in Cariano (4) ⚠️ | San Pietro in Cariano | 1 |
| Forêt de Ferrara di Monte Baldo (146) ⚠️ | Ferrara di Monte Baldo | 1 |
| Parco comunale del Raziol ⚠️ | Castel d'Azzano | 1 |
| Parc de Villafranca di Verona (49) ⚠️ | Villafranca di Verona | 1 |
| Orti Comunali di Castel d'Azzano ⚠️ | Castel d'Azzano | 1 |
| Parc de Vigasio (4) ⚠️ | Vigasio | 1 |
| Forêt de Peschiera del Garda (3) ⚠️ | Peschiera del Garda | 1 |
| Forêt de Peschiera del Garda (4) ⚠️ | Peschiera del Garda | 1 |
| Forêt de Cerro Veronese (27) ⚠️ | Cerro Veronese | 1 |
| Forêt de Cerro Veronese (29) ⚠️ | Cerro Veronese | 1 |
| Forêt de Cerro Veronese (32) ⚠️ | Cerro Veronese | 1 |
| Forêt de Cerro Veronese (35) ⚠️ | Cerro Veronese | 1 |
| Forêt de Cerro Veronese (36) ⚠️ | Cerro Veronese | 1 |
| Forêt de Grezzana (86) ⚠️ | Grezzana | 1 |
| Forêt de Cerro Veronese (38) ⚠️ | Cerro Veronese | 1 |
| Forêt de Cerro Veronese (46) ⚠️ | Cerro Veronese | 1 |
| Forêt de Cerro Veronese (49) ⚠️ | Cerro Veronese | 1 |
| Forêt de Cerro Veronese (51) ⚠️ | Bosco Chiesanuova | 1 |
| Parc de Caldiero (4) ⚠️ | Caldiero | 1 |
| Forêt de Mezzane di Sotto (35) ⚠️ | Mezzane di Sotto | 1 |
| Forêt de Illasi (2) ⚠️ | Illasi | 1 |
| Forêt de Soave ⚠️ | Soave | 1 |
| Parc de Verona (116) ⚠️ | Verona | 1 |
| Parc de Minerbe (4) ⚠️ | Minerbe | 1 |
| Bois de Cerea (3) ⚠️ | Cerea | 1 |
| Forêt de Illasi (5) ⚠️ | Illasi | 1 |
| Oasi della Bora (2) ⚠️ | Povegliano Veronese | 1 |
| Parc de Sorgà (3) ⚠️ | Sorgà | 1 |
| Forêt de Garda (4) ⚠️ | Garda | 1 |
| Forêt de Illasi (13) ⚠️ | Illasi | 1 |
| Forêt de Illasi (15) ⚠️ | Illasi | 1 |
| Forêt de Cazzano di Tramigna (12) ⚠️ | Cazzano di Tramigna | 1 |
| Forêt de Cazzano di Tramigna (14) ⚠️ | Cazzano di Tramigna | 1 |
| Forêt de Cazzano di Tramigna (15) ⚠️ | Cazzano di Tramigna | 1 |
| Forêt de Cazzano di Tramigna (17) ⚠️ | Cazzano di Tramigna | 1 |
| Forêt de Illasi (17) ⚠️ | Illasi | 1 |
| Forêt de Vestenanova (5) ⚠️ | Vestenanova | 1 |
| Forêt de Monteforte d'Alpone (7) ⚠️ | Monteforte d'Alpone | 1 |
| Forêt de Soave (3) ⚠️ | Soave | 1 |
| Forêt de Soave (5) ⚠️ | Soave | 1 |
| Forêt de Soave (7) ⚠️ | Soave | 1 |
| Forêt de Monteforte d'Alpone (12) ⚠️ | Monteforte d'Alpone | 1 |
| Forêt de Soave (10) ⚠️ | Soave | 1 |
| Forêt de Soave (11) ⚠️ | Soave | 1 |
| Forêt de Cazzano di Tramigna (21) ⚠️ | Cazzano di Tramigna | 1 |
| Forêt de Illasi (19) ⚠️ | Illasi | 1 |
| Forêt de Monteforte d'Alpone (19) ⚠️ | Monteforte d'Alpone | 1 |
| Forêt de Soave (16) ⚠️ | Soave | 1 |
| Forêt de Cazzano di Tramigna (22) ⚠️ | Cazzano di Tramigna | 1 |
| Parc de Mozzecane (21) ⚠️ | Mozzecane | 1 |
| Parco Pubblico ⚠️ | Vigasio | 1 |
| Parco Santa Teresa ⚠️ | Verona | 1 |
| Parc de Cazzano di Tramigna ⚠️ | Cazzano di Tramigna | 1 |
| Forêt de Villa Bartolomea (3) ⚠️ | Villa Bartolomea | 1 |
| Parc de Villa Bartolomea (3) ⚠️ | Villa Bartolomea | 1 |
| Forêt de Villa Bartolomea (7) ⚠️ | Villa Bartolomea | 1 |
| Forêt de Villa Bartolomea (8) ⚠️ | Villa Bartolomea | 1 |
| Forêt de Villa Bartolomea (9) ⚠️ | Villa Bartolomea | 1 |
| Parc de Villa Bartolomea (4) ⚠️ | Villa Bartolomea | 1 |
| Forêt de Villa Bartolomea (11) ⚠️ | Villa Bartolomea | 1 |
| Parc de Colognola ai Colli (3) ⚠️ | Colognola ai Colli | 1 |
| Forêt de Grezzana (88) ⚠️ | Grezzana | 1 |
| Bois de Verona (7) ⚠️ | Verona | 1 |
| Bois de Valeggio sul Mincio (17) ⚠️ | Valeggio sul Mincio | 1 |
| Parc de San Martino Buon Albergo (13) ⚠️ | San Martino Buon Albergo | 1 |
| Parc de Sona ⚠️ | Sona | 1 |
| Parc de Casaleone (11) ⚠️ | Casaleone | 1 |
| Forêt de Bussolengo (19) ⚠️ | Bussolengo | 1 |
| Forêt de Bussolengo (21) ⚠️ | Bussolengo | 1 |
| Forêt de Lazise (15) ⚠️ | Lazise | 1 |
| Forêt de Marano di Valpolicella (36) ⚠️ | Marano di Valpolicella | 1 |
| Forêt de Roverè Veronese (83) ⚠️ | Roverè Veronese | 1 |
| Forêt de Roverè Veronese (84) ⚠️ | Roverè Veronese | 1 |
| Forêt de Roverè Veronese (87) ⚠️ | Roverè Veronese | 1 |
| Forêt de Roverè Veronese (88) ⚠️ | Roverè Veronese | 1 |
| Forêt de Velo Veronese (35) ⚠️ | Velo Veronese | 1 |
| Forêt de Velo Veronese (42) ⚠️ | Velo Veronese | 1 |
| Forêt de Velo Veronese (43) ⚠️ | Velo Veronese | 1 |
| Forêt de Soave (19) ⚠️ | Soave | 1 |
| Parc de Caldiero (6) ⚠️ | Caldiero | 1 |
| Forêt de Roverè Veronese (91) ⚠️ | Roverè Veronese | 1 |
| Forêt de Roverè Veronese (92) ⚠️ | Roverè Veronese | 1 |
| Forêt de Legnago (2) ⚠️ | Legnago | 1 |
| Forêt de Legnago (3) ⚠️ | Legnago | 1 |
| Forêt de Soave (20) ⚠️ | Soave | 1 |
| Forêt de Soave (21) ⚠️ | Soave | 1 |
| Forêt de Soave (25) ⚠️ | Soave | 1 |
| Bois de Legnago (9) ⚠️ | Legnago | 1 |
| Forêt de Pastrengo (6) ⚠️ | Pastrengo | 1 |
| Forêt de Roncà (14) ⚠️ | Roncà | 1 |
| Forêt de Roncà (24) ⚠️ | Roncà | 1 |
| Forêt de Roncà (29) ⚠️ | Roncà | 1 |
| Forêt de Roncà (30) ⚠️ | Roncà | 1 |
| Forêt de Roncà (33) ⚠️ | Roncà | 1 |
| Forêt de Roncà (35) ⚠️ | Roncà | 1 |
| Forêt de Roncà (39) ⚠️ | Roncà | 1 |
| Forêt de Roncà (40) ⚠️ | Roncà | 1 |
| Forêt de Roncà (41) ⚠️ | Roncà | 1 |
| Forêt de Roncà (43) ⚠️ | Roncà | 1 |
| Forêt de Roncà (44) ⚠️ | Roncà | 1 |
| Forêt de Roncà (50) ⚠️ | Roncà | 1 |
| Forêt de Roncà (52) ⚠️ | Roncà | 1 |
| Forêt de Roncà (53) ⚠️ | Roncà | 1 |
| Forêt de Roncà (58) ⚠️ | Roncà | 1 |
| Forêt de Roncà (59) ⚠️ | Roncà | 1 |
| Forêt de Roncà (61) ⚠️ | Roncà | 1 |
| Forêt de Roncà (63) ⚠️ | Roncà | 1 |
| Forêt de Roncà (68) ⚠️ | Roncà | 1 |
| Forêt de Roncà (70) ⚠️ | Roncà | 1 |
| Forêt de Roncà (72) ⚠️ | Roncà | 1 |
| Forêt de Roncà (81) ⚠️ | Roncà | 1 |
| Forêt de Roncà (89) ⚠️ | Roncà | 1 |
| Forêt de Roncà (92) ⚠️ | Roncà | 1 |
| Forêt de Roncà (94) ⚠️ | Roncà | 1 |
| Forêt de Roncà (95) ⚠️ | Roncà | 1 |
| Forêt de Roncà (96) ⚠️ | Roncà | 1 |
| Forêt de Roncà (102) ⚠️ | Roncà | 1 |
| Forêt de Roncà (103) ⚠️ | Roncà | 1 |
| Forêt de Roncà (105) ⚠️ | Roncà | 1 |
| Forêt de Roncà (112) ⚠️ | Roncà | 1 |
| Forêt de Roncà (117) ⚠️ | Roncà | 1 |
| Forêt de Roncà (122) ⚠️ | Roncà | 1 |
| Forêt de Roncà (126) ⚠️ | Roncà | 1 |
| Forêt de Roncà (127) ⚠️ | Roncà | 1 |
| Forêt de Vestenanova (8) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (9) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (10) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (18) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (21) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (24) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (27) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (29) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (30) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (31) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (47) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (48) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (50) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (51) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (53) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (64) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (70) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (73) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (78) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (88) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (92) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (93) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (94) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (97) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (107) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (109) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (110) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (111) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (115) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (121) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (123) ⚠️ | Vestenanova | 1 |
| Forêt de San Giovanni Ilarione (11) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de Vestenanova (132) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (133) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (135) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (136) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (141) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (142) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (144) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (146) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (147) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (148) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (152) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (155) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (164) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (165) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (171) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (172) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (175) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (176) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (179) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (180) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (183) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (189) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (192) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (198) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (200) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (202) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (209) ⚠️ | Vestenanova | 1 |
| Piazzetta degli artisti ⚠️ | Caldiero | 1 |
| Parc de Castelnuovo del Garda (11) ⚠️ | Castelnuovo del Garda | 1 |
| Parco Ottocento ⚠️ | Verona | 1 |
| Parco dello Zodiaco ⚠️ | Bussolengo | 1 |
| Bois de Peschiera del Garda (3) ⚠️ | Peschiera del Garda | 1 |
| Forêt de Affi (14) ⚠️ | Affi | 1 |
| Forêt de Affi (15) ⚠️ | Affi | 1 |
| Giardini Oriana Fallaci ⚠️ | Verona | 1 |
| Parc de Sommacampagna (12) ⚠️ | Sommacampagna | 1 |
| Parc de Verona (133) ⚠️ | Verona | 1 |
| Parc de Verona (134) ⚠️ | Verona | 1 |
| Parc de Povegliano Veronese (7) ⚠️ | Povegliano Veronese | 1 |
| Bois de Verona (10) ⚠️ | Verona | 1 |
| Bois de Sant'Anna d'Alfaedo (2) ⚠️ | Sant'Anna d'Alfaedo | 1 |
| Bois de Bosco Chiesanuova ⚠️ | Bosco Chiesanuova | 1 |
| Bois de Pastrengo (4) ⚠️ | Pastrengo | 1 |
| Bois de Pastrengo (6) ⚠️ | Pastrengo | 1 |
| Bois de Pastrengo (7) ⚠️ | Pastrengo | 1 |
| Bois de Pastrengo (8) ⚠️ | Pastrengo | 1 |
| Bois de Pastrengo (9) ⚠️ | Pastrengo | 1 |
| Bois de Pastrengo (10) ⚠️ | Pastrengo | 1 |
| Bois de Negrar di Valpolicella ⚠️ | Negrar di Valpolicella | 1 |
| Bois de Negrar di Valpolicella (5) ⚠️ | Negrar di Valpolicella | 1 |
| Bois de Negrar di Valpolicella (6) ⚠️ | Negrar di Valpolicella | 1 |
| Bois de Negrar di Valpolicella (9) ⚠️ | Negrar di Valpolicella | 1 |
| Bois de Negrar di Valpolicella (10) ⚠️ | Negrar di Valpolicella | 1 |
| Bois de Grezzana ⚠️ | Grezzana | 1 |
| Bois de Grezzana (2) ⚠️ | Grezzana | 1 |
| Bois de Grezzana (3) ⚠️ | Grezzana | 1 |
| Bois de Grezzana (4) ⚠️ | Grezzana | 1 |
| Bois de Grezzana (5) ⚠️ | Grezzana | 1 |
| Bois de Grezzana (6) ⚠️ | Grezzana | 1 |
| Bois de Grezzana (9) ⚠️ | Grezzana | 1 |
| Bois de Grezzana (13) ⚠️ | Grezzana | 1 |
| Bois de Grezzana (18) ⚠️ | Grezzana | 1 |
| Bois de Grezzana (19) ⚠️ | Grezzana | 1 |
| Bois de Grezzana (20) ⚠️ | Grezzana | 1 |
| Bois de Grezzana (26) ⚠️ | Grezzana | 1 |
| Bois de Grezzana (28) ⚠️ | Grezzana | 1 |
| Parc de Verona (136) ⚠️ | Verona | 1 |
| Forêt de San Giovanni Ilarione (18) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (21) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (24) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (25) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (31) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (32) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (35) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (39) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (45) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (47) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (50) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (54) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (56) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (57) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (63) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (65) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (67) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (71) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (81) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (82) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (87) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (89) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (96) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (99) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (101) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (103) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (104) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (106) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (114) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (121) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (122) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (124) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (133) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (142) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (149) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de San Giovanni Ilarione (154) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de Selva di Progno (10) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (13) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (16) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (18) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (24) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (28) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (32) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (33) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (35) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (37) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (40) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (41) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (46) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (48) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (50) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (51) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (52) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (53) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (58) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (60) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (62) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (64) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (71) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (78) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (81) ⚠️ | Selva di Progno | 1 |
| Forêt de Bosco Chiesanuova (370) ⚠️ | Bosco Chiesanuova | 1 |
| Forêt de Selva di Progno (89) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (90) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (91) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (94) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (95) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (100) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (103) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (104) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (105) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (109) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (114) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (116) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (121) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (126) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (129) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (134) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (136) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (140) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (146) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (148) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (149) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (150) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (152) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (154) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (156) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (159) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (161) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (162) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (163) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (165) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (166) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (168) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (176) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (178) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (181) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (184) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (188) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (189) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (192) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (196) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (199) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (207) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (208) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (211) ⚠️ | Selva di Progno | 1 |
| Forêt de Selva di Progno (216) ⚠️ | Selva di Progno | 1 |
| Bois de Velo Veronese (6) ⚠️ | Velo Veronese | 1 |
| Bois de Velo Veronese (8) ⚠️ | Velo Veronese | 1 |
| Bois de Velo Veronese (9) ⚠️ | Velo Veronese | 1 |
| Parc de Grezzana (2) ⚠️ | Grezzana | 1 |
| Parc de Verona (137) ⚠️ | Verona | 1 |
| Parc de San Martino Buon Albergo (16) ⚠️ | San Martino Buon Albergo | 1 |
| Forêt de Velo Veronese (47) ⚠️ | Velo Veronese | 1 |
| Bosco di via Pasetto Pasetto ⚠️ | Zevio | 1 |
| Forêt de Verona (433) ⚠️ | Verona | 1 |
| Parc de Buttapietra ⚠️ | Buttapietra | 1 |
| Forêt de Montecchia di Crosara (5) ⚠️ | Montecchia di Crosara | 1 |
| Forêt de Montecchia di Crosara (7) ⚠️ | Montecchia di Crosara | 1 |
| Forêt de Montecchia di Crosara (8) ⚠️ | Montecchia di Crosara | 1 |
| Forêt de Montecchia di Crosara (9) ⚠️ | Montecchia di Crosara | 1 |
| Forêt de Montecchia di Crosara (11) ⚠️ | Montecchia di Crosara | 1 |
| Forêt de Montecchia di Crosara (14) ⚠️ | Montecchia di Crosara | 1 |
| Forêt de Montecchia di Crosara (20) ⚠️ | Montecchia di Crosara | 1 |
| Forêt de Montecchia di Crosara (27) ⚠️ | Montecchia di Crosara | 1 |
| Forêt de Montecchia di Crosara (28) ⚠️ | Montecchia di Crosara | 1 |
| Forêt de Montecchia di Crosara (33) ⚠️ | Montecchia di Crosara | 1 |
| Forêt de Montecchia di Crosara (37) ⚠️ | Montecchia di Crosara | 1 |
| Forêt de Montecchia di Crosara (41) ⚠️ | Montecchia di Crosara | 1 |
| Forêt de Montecchia di Crosara (51) ⚠️ | Montecchia di Crosara | 1 |
| Forêt de Montecchia di Crosara (52) ⚠️ | Montecchia di Crosara | 1 |
| Forêt de Montecchia di Crosara (53) ⚠️ | Montecchia di Crosara | 1 |
| Forêt de Montecchia di Crosara (54) ⚠️ | Montecchia di Crosara | 1 |
| Forêt de Montecchia di Crosara (61) ⚠️ | Montecchia di Crosara | 1 |
| Forêt de Montecchia di Crosara (65) ⚠️ | Montecchia di Crosara | 1 |
| Forêt de Montecchia di Crosara (67) ⚠️ | Montecchia di Crosara | 1 |
| Forêt de Montecchia di Crosara (70) ⚠️ | Montecchia di Crosara | 1 |
| Forêt de Montecchia di Crosara (74) ⚠️ | Montecchia di Crosara | 1 |
| Forêt de Montecchia di Crosara (78) ⚠️ | Montecchia di Crosara | 1 |
| Forêt de Montecchia di Crosara (84) ⚠️ | Montecchia di Crosara | 1 |
| Forêt de Montecchia di Crosara (87) ⚠️ | Montecchia di Crosara | 1 |
| Forêt de Cerro Veronese (55) ⚠️ | Cerro Veronese | 1 |
| Parc de Costermano sul Garda (2) ⚠️ | Costermano sul Garda | 1 |
| Forêt de Roverè Veronese (102) ⚠️ | Roverè Veronese | 1 |
| Bois de Valeggio sul Mincio (19) ⚠️ | Valeggio sul Mincio | 1 |
| Bois de Valeggio sul Mincio (22) ⚠️ | Valeggio sul Mincio | 1 |
| Bois de Valeggio sul Mincio (23) ⚠️ | Valeggio sul Mincio | 1 |
| Bois de Bovolone ⚠️ | Bovolone | 1 |
| Bois de Bovolone (2) ⚠️ | Bovolone | 1 |
| Bois de Bovolone (3) ⚠️ | Bovolone | 1 |
| Forêt de San Zeno di Montagna (216) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de Lazise (16) ⚠️ | Lazise | 1 |
| Forêt de Lazise (17) ⚠️ | Lazise | 1 |
| Parc de Valeggio sul Mincio (16) ⚠️ | Valeggio sul Mincio | 1 |
| Parco Belvedere ⚠️ | Castelnuovo del Garda | 1 |
| Forêt de Grezzana (101) ⚠️ | Grezzana | 1 |
| Forêt de Roverè Veronese (112) ⚠️ | Roverè Veronese | 1 |
| Forêt de Roverè Veronese (119) ⚠️ | Roverè Veronese | 1 |
| Forêt de Roverè Veronese (126) ⚠️ | Roverè Veronese | 1 |
| Forêt de Roverè Veronese (127) ⚠️ | Roverè Veronese | 1 |
| Bois de Legnago (13) ⚠️ | Legnago | 1 |
| Bois de Legnago (14) ⚠️ | Legnago | 1 |
| Parc de Legnago (16) ⚠️ | Legnago | 1 |
| Forêt de Albaredo d'Adige (5) ⚠️ | Albaredo d'Adige | 1 |
| Forêt de Albaredo d'Adige (7) ⚠️ | Albaredo d'Adige | 1 |
| Pioppeto (2) ⚠️ | San Pietro di Morubio | 1 |
| Forêt de Bussolengo (24) ⚠️ | Bussolengo | 1 |
| Parco Conegliano ⚠️ | Verona | 1 |
| Forêt de Albaredo d'Adige (19) ⚠️ | Albaredo d'Adige | 1 |
| Forêt de Albaredo d'Adige (20) ⚠️ | Albaredo d'Adige | 1 |
| Parco della Savia ⚠️ | Tregnago | 1 |
| Parco parrocchiale Santa Maria Assunta ⚠️ | Tregnago | 1 |
| Parco Cavalier Romani ⚠️ | Sona | 1 |
| Parc de Roveredo di Guà ⚠️ | Roveredo di Guà | 1 |
| Forêt de Cavaion Veronese (9) ⚠️ | Cavaion Veronese | 1 |
| Parc de Mozzecane (22) ⚠️ | Mozzecane | 1 |
| Parc de Verona (179) ⚠️ | Verona | 1 |
| Bois de San Giovanni Lupatoto (3) ⚠️ | San Giovanni Lupatoto | 1 |
| Forêt de Garda (7) ⚠️ | Garda | 1 |
| Parco dell'educazione stradale di Lazise ⚠️ | Lazise | 1 |
| Parc de Verona (184) ⚠️ | Verona | 1 |
| Bois de Isola Rizza ⚠️ | Isola Rizza | 1 |
| Forêt de Costermano sul Garda (49) ⚠️ | Costermano sul Garda | 1 |
| Bois de Garda (6) ⚠️ | Garda | 1 |
| Bois de Bardolino (4) ⚠️ | Bardolino | 1 |
| Bois de Bardolino (5) ⚠️ | Bardolino | 1 |
| Bois de Sant'Ambrogio di Valpolicella ⚠️ | Sant'Ambrogio di Valpolicella | 1 |
| Bois de Roverchiara (2) ⚠️ | Roverchiara | 1 |
| Forêt de Dolcè (80) ⚠️ | Dolcè | 1 |
| Forêt de Isola Rizza ⚠️ | Isola Rizza | 1 |
| Forêt de Isola Rizza (3) ⚠️ | Isola Rizza | 1 |
| Forêt de Velo Veronese (49) ⚠️ | Velo Veronese | 1 |
| Forêt de Valeggio sul Mincio (34) ⚠️ | Valeggio sul Mincio | 1 |
| Forêt de Peschiera del Garda (11) ⚠️ | Peschiera del Garda | 1 |
| Bois de Roverchiara (3) ⚠️ | Roverchiara | 1 |
| Forêt de Roverè Veronese (128) ⚠️ | Roverè Veronese | 1 |
| Parc de Castelnuovo del Garda (15) ⚠️ | Castelnuovo del Garda | 1 |
| Parc de San Giovanni Ilarione ⚠️ | San Giovanni Ilarione | 1 |
| Bois de Belfiore ⚠️ | Belfiore | 1 |
| Forêt de Albaredo d'Adige (32) ⚠️ | Albaredo d'Adige | 1 |
| Parco Michelangelo ⚠️ | San Bonifacio | 1 |
| Parc de Verona (189) ⚠️ | Verona | 1 |
| Parc de Verona (192) ⚠️ | Verona | 1 |
| Parco Guidorizzi ⚠️ | Cerea | 1 |
| Parc de Peschiera del Garda (20) ⚠️ | Peschiera del Garda | 1 |
| Forêt de Peschiera del Garda (13) ⚠️ | Peschiera del Garda | 1 |
| Forêt de Albaredo d'Adige (38) ⚠️ | Albaredo d'Adige | 1 |
| Forêt de Nogara (11) ⚠️ | Nogara | 1 |
| Forêt de Grezzana (103) ⚠️ | Grezzana | 1 |
| Forêt de Badia Calavena (8) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (9) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (11) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (12) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (14) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (25) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (26) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (33) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (38) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (40) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (48) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (51) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (55) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (58) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (60) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (61) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (62) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (69) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (72) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (75) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (83) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (84) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (88) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (91) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (92) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (94) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (96) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (98) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (100) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (103) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (104) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (106) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (107) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (108) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (113) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (115) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (116) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (117) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (119) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (122) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (126) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (128) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (129) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (132) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (133) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (135) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (138) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (139) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (143) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (147) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (148) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (155) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (156) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (158) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (159) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (160) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (162) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (164) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (171) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (172) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (177) ⚠️ | Badia Calavena | 1 |
| Forêt de Velo Veronese (50) ⚠️ | Velo Veronese | 1 |
| Forêt de Badia Calavena (181) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (187) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (188) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (192) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (195) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (197) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (198) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (200) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (204) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (205) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (213) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (215) ⚠️ | Badia Calavena | 1 |
| Forêt de Badia Calavena (216) ⚠️ | Badia Calavena | 1 |
| Forêt de Negrar di Valpolicella (74) ⚠️ | Negrar di Valpolicella | 1 |
| Forêt de Verona (444) ⚠️ | Verona | 1 |
| Forêt de Tregnago (2) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (3) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (4) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (6) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (8) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (15) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (16) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (17) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (22) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (26) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (27) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (29) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (34) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (37) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (42) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (43) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (45) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (47) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (56) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (58) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (64) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (81) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de Tregnago (90) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (94) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (96) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (97) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (98) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (100) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (102) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (104) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (106) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (108) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (109) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (113) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (115) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (121) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (123) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (125) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (128) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (129) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (131) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (135) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (136) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (139) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (141) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (142) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (144) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (147) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (150) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (152) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (153) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (155) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (158) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (159) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (160) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (162) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (163) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (165) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (166) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (168) ⚠️ | Tregnago | 1 |
| Forêt de Tregnago (173) ⚠️ | Tregnago | 1 |
| Parc de Tregnago (3) ⚠️ | Tregnago | 1 |
| Parc de Sant'Ambrogio di Valpolicella (5) ⚠️ | Sant'Ambrogio di Valpolicella | 1 |
| Forêt de Sant'Ambrogio di Valpolicella (40) ⚠️ | Sant'Ambrogio di Valpolicella | 1 |
| Bois de Bonavigo (2) ⚠️ | Bonavigo | 1 |
| Bois de Bonavigo (3) ⚠️ | Bonavigo | 1 |
| Bois de Ronco all'Adige (4) ⚠️ | Ronco all'Adige | 1 |
| Bois de Ronco all'Adige (5) ⚠️ | Ronco all'Adige | 1 |
| Bois de Belfiore (2) ⚠️ | Belfiore | 1 |
| Bois de Ronco all'Adige (19) ⚠️ | Ronco all'Adige | 1 |
| Bois de Ronco all'Adige (21) ⚠️ | Ronco all'Adige | 1 |
| Bois de Angiari (2) ⚠️ | Angiari | 1 |
| Forêt de San Bonifacio ⚠️ | San Bonifacio | 1 |
| Bois de Legnago (15) ⚠️ | Legnago | 1 |
| Parc de Lazise (13) ⚠️ | Lazise | 1 |
| Bois de Lazise (16) ⚠️ | Lazise | 1 |
| Bois de Lazise (23) ⚠️ | Lazise | 1 |
| Bois de Lazise (31) ⚠️ | Lazise | 1 |
| Bois de Lazise (39) ⚠️ | Lazise | 1 |
| Bois de Lazise (40) ⚠️ | Lazise | 1 |
| Bois de Lazise (42) ⚠️ | Lazise | 1 |
| Parc de Legnago (18) ⚠️ | Legnago | 1 |
| Bois de Bardolino (12) ⚠️ | Bardolino | 1 |
| Bois de Lazise (47) ⚠️ | Lazise | 1 |
| Bois de Lazise (54) ⚠️ | Lazise | 1 |
| Bois de Lazise (55) ⚠️ | Lazise | 1 |
| Bois de Lazise (62) ⚠️ | Lazise | 1 |
| Bois de Lazise (63) ⚠️ | Lazise | 1 |
| Bois de Lazise (69) ⚠️ | Lazise | 1 |
| Bois de Lazise (78) ⚠️ | Lazise | 1 |
| Bois de Lazise (79) ⚠️ | Lazise | 1 |
| Bois de Lazise (81) ⚠️ | Lazise | 1 |
| Bois de Castelnuovo del Garda (10) ⚠️ | Castelnuovo del Garda | 1 |
| Bois de Lazise (87) ⚠️ | Lazise | 1 |
| Bois de Lazise (92) ⚠️ | Lazise | 1 |
| Bois de Lazise (99) ⚠️ | Lazise | 1 |
| Bois de Lazise (100) ⚠️ | Lazise | 1 |
| Bois de Lazise (101) ⚠️ | Lazise | 1 |
| Bois de Lazise (103) ⚠️ | Lazise | 1 |
| Bois de Lazise (106) ⚠️ | Lazise | 1 |
| Parc de Salizzole ⚠️ | Salizzole | 1 |
| Parc de Palù ⚠️ | Palù | 1 |
| Forêt de Lavagno (10) ⚠️ | Lavagno | 1 |
| Bois de San Mauro di Saline (2) ⚠️ | San Mauro di Saline | 1 |
| Bois de San Mauro di Saline (5) ⚠️ | San Mauro di Saline | 1 |
| Bois de Mezzane di Sotto (4) ⚠️ | Mezzane di Sotto | 1 |
| Bois de Roverè Veronese (5) ⚠️ | Roverè Veronese | 1 |
| Bois de Roverè Veronese (6) ⚠️ | Roverè Veronese | 1 |
| Bois de Roverè Veronese (7) ⚠️ | Roverè Veronese | 1 |
| Bois de Velo Veronese (19) ⚠️ | Velo Veronese | 1 |
| Bois de Velo Veronese (21) ⚠️ | Velo Veronese | 1 |
| Bois de San Mauro di Saline (6) ⚠️ | San Mauro di Saline | 1 |
| Bois de San Mauro di Saline (7) ⚠️ | San Mauro di Saline | 1 |
| Bois de San Mauro di Saline (8) ⚠️ | San Mauro di Saline | 1 |
| Bois de San Mauro di Saline (9) ⚠️ | San Mauro di Saline | 1 |
| Bois de Mezzane di Sotto (11) ⚠️ | Mezzane di Sotto | 1 |
| Bois de Mezzane di Sotto (13) ⚠️ | Mezzane di Sotto | 1 |
| Bois de Mezzane di Sotto (16) ⚠️ | Mezzane di Sotto | 1 |
| Bois de Mezzane di Sotto (18) ⚠️ | Mezzane di Sotto | 1 |
| Bois de Velo Veronese (27) ⚠️ | Velo Veronese | 1 |
| Bois de Velo Veronese (30) ⚠️ | Velo Veronese | 1 |
| Bois de Velo Veronese (34) ⚠️ | Velo Veronese | 1 |
| Bois de Velo Veronese (37) ⚠️ | Velo Veronese | 1 |
| Bois de San Mauro di Saline (11) ⚠️ | San Mauro di Saline | 1 |
| Forêt de Legnago (7) ⚠️ | Legnago | 1 |
| Bois de Grezzana (33) ⚠️ | Grezzana | 1 |
| Bois de San Mauro di Saline (24) ⚠️ | San Mauro di Saline | 1 |
| Bois de San Mauro di Saline (30) ⚠️ | San Mauro di Saline | 1 |
| Bois de Illasi (2) ⚠️ | Illasi | 1 |
| Bois de Negrar di Valpolicella (16) ⚠️ | Negrar di Valpolicella | 1 |
| Bois de Negrar di Valpolicella (19) ⚠️ | Negrar di Valpolicella | 1 |
| Bois de Grezzana (36) ⚠️ | Grezzana | 1 |
| Bois de Grezzana (37) ⚠️ | Grezzana | 1 |
| Bois de Grezzana (39) ⚠️ | Grezzana | 1 |
| Bois de Illasi (4) ⚠️ | Illasi | 1 |
| Bois de Verona (21) ⚠️ | Verona | 1 |
| Bois de Verona (22) ⚠️ | Verona | 1 |
| Bois de Verona (23) ⚠️ | Verona | 1 |
| Bois de Verona (25) ⚠️ | Verona | 1 |
| Bois de Verona (26) ⚠️ | Verona | 1 |
| Bois de Mezzane di Sotto (21) ⚠️ | Mezzane di Sotto | 1 |
| Bois de Verona (27) ⚠️ | Verona | 1 |
| Bois de Grezzana (47) ⚠️ | Grezzana | 1 |
| Bois de Grezzana (48) ⚠️ | Grezzana | 1 |
| Bois de Grezzana (50) ⚠️ | Grezzana | 1 |
| Bois de Mezzane di Sotto (22) ⚠️ | Mezzane di Sotto | 1 |
| Bois de Mezzane di Sotto (23) ⚠️ | Mezzane di Sotto | 1 |
| Bois de Mezzane di Sotto (26) ⚠️ | Mezzane di Sotto | 1 |
| Bois de Mezzane di Sotto (29) ⚠️ | Mezzane di Sotto | 1 |
| Bois de Lazise (111) ⚠️ | Lazise | 1 |
| Bois de Lazise (113) ⚠️ | Lazise | 1 |
| Bois de Lazise (115) ⚠️ | Lazise | 1 |
| Bois de Lazise (116) ⚠️ | Lazise | 1 |
| Bois de Mezzane di Sotto (36) ⚠️ | Mezzane di Sotto | 1 |
| Bois de Zevio (3) ⚠️ | Zevio | 1 |
| Bois de Verona (29) ⚠️ | Verona | 1 |
| Bois de Roverè Veronese (25) ⚠️ | Roverè Veronese | 1 |
| Bois de Mezzane di Sotto (38) ⚠️ | Mezzane di Sotto | 1 |
| Forêt de Brenzone sul Garda (69) ⚠️ | Brenzone sul Garda | 1 |
| Bois de Grezzana (52) ⚠️ | Grezzana | 1 |
| Bois de Grezzana (57) ⚠️ | Grezzana | 1 |
| Bois de Grezzana (59) ⚠️ | Grezzana | 1 |
| Bois de Roverè Veronese (30) ⚠️ | Roverè Veronese | 1 |
| Bois de Roverè Veronese (36) ⚠️ | Roverè Veronese | 1 |
| Bois de Roverè Veronese (38) ⚠️ | Roverè Veronese | 1 |
| Bois de Roverè Veronese (39) ⚠️ | Roverè Veronese | 1 |
| Bois de Roverè Veronese (44) ⚠️ | Roverè Veronese | 1 |
| Bois de Roverè Veronese (46) ⚠️ | Roverè Veronese | 1 |
| Bois de Negrar di Valpolicella (25) ⚠️ | Negrar di Valpolicella | 1 |
| Bois de Negrar di Valpolicella (27) ⚠️ | Negrar di Valpolicella | 1 |
| Bois de Negrar di Valpolicella (35) ⚠️ | Negrar di Valpolicella | 1 |
| Bois de Grezzana (67) ⚠️ | Grezzana | 1 |
| Forêt de Brentino Belluno (86) ⚠️ | Brentino Belluno | 1 |
| Forêt de Bussolengo (30) ⚠️ | Bussolengo | 1 |
| Parco Walner ⚠️ | San Giovanni Lupatoto | 1 |
| Forêt de Verona (463) ⚠️ | Verona | 1 |
| Forêt de San Zeno di Montagna (225) ⚠️ | San Zeno di Montagna | 1 |
| Forêt de Caprino Veronese (344) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (347) ⚠️ | Caprino Veronese | 1 |
| Forêt de Caprino Veronese (349) ⚠️ | Caprino Veronese | 1 |
| Forêt de San Giovanni Ilarione (162) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de Selva di Progno (220) ⚠️ | Selva di Progno | 1 |
| Forêt de Vestenanova (214) ⚠️ | Vestenanova | 1 |
| Forêt de Vestenanova (226) ⚠️ | Vestenanova | 1 |
| Forêt de San Giovanni Ilarione (180) ⚠️ | San Giovanni Ilarione | 1 |
| Forêt de Montecchia di Crosara (96) ⚠️ | Montecchia di Crosara | 1 |
| Forêt de Caprino Veronese (358) ⚠️ | Caprino Veronese | 1 |
| Bois de Mezzane di Sotto (42) ⚠️ | Mezzane di Sotto | 1 |
| Bois de Lazise (128) ⚠️ | Lazise | 1 |

3 350 parc(s) plus petits qu'une cellule ne sont pas listés : la carte les dessine, mais ils n'offrent aucune cellule.

⚠️ 6492 parc(s) hors de la fenêtre 10–125 cellules (6469 trop petit(s), 23 trop grand(s)) : affichés sur la carte, mais ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| airport | 228 |
| military | 165 |
| prison | 5 |
| **Total déclaré** | **398** |
| dont dans une zone de ce territoire | 398 |


### Zones concernées

| Zone | Cellules exclues |
|---|---:|
| Sommacampagna | 145 |
| Verona | 77 |
| Villafranca di Verona | 62 |
| Valeggio sul Mincio | 54 |
| Cerea | 21 |
| Bovolone | 12 |
| Legnago | 7 |
| Concamarise | 7 |
| Peschiera del Garda | 7 |
| Povegliano Veronese | 6 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
