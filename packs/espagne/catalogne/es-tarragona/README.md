# Province de Tarragone

Pack `es-tarragona` · version 1.0.1 · grille 200 m · Espagne › Catalogne

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 275 873 |
| dont restreintes (aéroport, militaire, prison) | 113 |
| dont sans chemin (aucune voie à moins de 60 m) | 29 277 |
| dont en forêt, sans chemin non plus | 15 992 |
| dont traversées par un cours d'eau, sans chemin non plus | 8 733 |
| Cellules retirées par le masque d'eau | 2 008 |
| Villes | 184 |
| Arrondissements et quartiers | 0 |
| Îles | 10 |
| Parcs | 5 000 |

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
| Alt Camp | 23 867 | somme de 23 villes |
| Baix Camp | 30 733 | somme de 28 villes |
| Baix Ebre | 43 186 | somme de 14 villes |
| Baix Penedès | 13 120 | somme de 14 villes |
| Conca de Barberà | 28 962 | somme de 22 villes |
| Montsià | 31 339 | somme de 12 villes |
| Priorat | 21 981 | somme de 23 villes |
| Ribera d'Ebre | 35 946 | somme de 14 villes |
| Tarragonès | 14 116 | somme de 22 villes |
| Terra Alta | 32 629 | somme de 12 villes |

Une île *composite* n'a pas de cellules à elle : sa progression est la somme de ses villes, et ses cellules ne lui sont jamais rattachées directement — elles compteraient deux fois.

## Villes (184)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Sans chemin | Parcs |
|---|---:|---:|---:|---:|---:|---:|---:|
| Tortosa | 9 582 | 134 | 9 448 | 0 | **9 448** | 1 834 (19 %) | 101 |
| Tivissa | 9 176 | 11 | 9 165 | 0 | **9 165** | 2 042 (22 %) | 32 |
| Roquetes | 5 990 | 1 | 5 989 | 0 | **5 989** | 1 516 (25 %) | 30 |
| Amposta | 6 037 | 383 | 5 654 | 0 | **5 654** | 831 (15 %) | 34 |
| Batea | 5 654 | 0 | 5 654 | 0 | **5 654** | 47 (1 %) | 49 |
| Ulldecona | 5 506 | 0 | 5 506 | 0 | **5 506** | 898 (16 %) | 16 |
| Horta de Sant Joan | 5 212 | 1 | 5 211 | 0 | **5 211** | 194 (4 %) | 53 |
| Flix | 5 138 | 74 | 5 064 | 0 | **5 064** | 807 (16 %) | 42 |
| la Sénia | 4 707 | 1 | 4 706 | 0 | **4 706** | 482 (10 %) | 56 |
| Vandellòs i l'Hospitalet de l'Infant | 4 511 | 1 | 4 510 | 0 | **4 510** | 542 (12 %) | 73 |
| el Perelló | 4 407 | 0 | 4 407 | 0 | **4 407** | 765 (17 %) | 35 |
| Deltebre | 4 550 | 239 | 4 311 | 0 | **4 311** | 800 (19 %) | 13 |
| Riba-roja d'Ebre | 4 407 | 189 | 4 218 | 0 | **4 218** | 689 (16 %) | 27 |
| Montblanc | 4 060 | 1 | 4 059 | 0 | **4 059** | 136 (3 %) | 46 |
| Mas de Barberans | 3 461 | 1 | 3 460 | 0 | **3 460** | 913 (26 %) | 3 |
| Aiguamúrcia | 3 255 | 1 | 3 254 | 0 | **3 254** | 201 (6 %) | 39 |
| Ascó | 3 283 | 58 | 3 225 | 0 | **3 225** | 308 (10 %) | 13 |
| el Montmell | 3 215 | 0 | 3 215 | 0 | **3 215** | 155 (5 %) | 24 |
| Querol | 3 204 | 3 | 3 201 | 0 | **3 201** | 134 (4 %) | 56 |
| Gandesa | 3 124 | 0 | 3 124 | 0 | **3 124** | 200 (6 %) | 6 |
| Pontils | 3 011 | 0 | 3 011 | 0 | **3 011** | 300 (10 %) | 22 |
| Vilalba dels Arcs | 2 967 | 0 | 2 967 | 0 | **2 967** | 428 (14 %) | 12 |
| l'Ametlla de Mar | 2 941 | 0 | 2 941 | 0 | **2 941** | 83 (3 %) | 239 |
| Vimbodí i Poblet | 2 923 | 2 | 2 921 | 0 | **2 921** | 81 (3 %) | 23 |
| Alfara de Carles | 2 804 | 0 | 2 804 | 0 | **2 804** | 244 (9 %) | 20 |
| Mont-roig del Camp | 2 793 | 0 | 2 793 | 0 | **2 793** | 104 (4 %) | 180 |
| Cornudella de Montsant | 2 784 | 37 | 2 747 | 0 | **2 747** | 190 (7 %) | 157 |
| Benifallet | 2 734 | 93 | 2 641 | 0 | **2 641** | 319 (12 %) | 16 |
| Tarragona | 2 594 | 3 | 2 591 | 0 | **2 591** | 14 (1 %) | 191 |
| l'Espluga de Francolí | 2 540 | 0 | 2 540 | 0 | **2 540** | 83 (3 %) | 16 |
| el Pinell de Brai | 2 525 | 0 | 2 525 | 0 | **2 525** | 420 (17 %) | 13 |
| la Fatarella | 2 498 | 0 | 2 498 | 0 | **2 498** | 236 (9 %) | 9 |
| Valls | 2 458 | 2 | 2 456 | 0 | **2 456** | 220 (9 %) | 181 |
| la Morera de Montsant | 2 358 | 0 | 2 358 | 0 | **2 358** | 278 (12 %) | 105 |
| la Ràpita | 2 384 | 30 | 2 354 | 0 | **2 354** | 865 (37 %) | 21 |
| Corbera d'Ebre | 2 351 | 0 | 2 351 | 0 | **2 351** | 162 (7 %) | 21 |
| Sant Jaume d'Enveja | 2 640 | 312 | 2 328 | 0 | **2 328** | 415 (18 %) | 15 |
| Tivenys | 2 345 | 19 | 2 326 | 0 | **2 326** | 511 (22 %) | 6 |
| Sarral | 2 325 | 0 | 2 325 | 0 | **2 325** | 251 (11 %) | 5 |
| Reus | 2 329 | 5 | 2 324 | 78 | **2 246** | 62 (3 %) | 192 |
| Garcia | 2 288 | 37 | 2 251 | 0 | **2 251** | 321 (14 %) | 9 |
| Rasquera | 2 235 | 2 | 2 233 | 0 | **2 233** | 450 (20 %) | 19 |
| Alcover | 2 062 | 0 | 2 062 | 0 | **2 062** | 225 (11 %) | 43 |
| Alcanar | 2 044 | 3 | 2 041 | 0 | **2 041** | 187 (9 %) | 56 |
| Móra d'Ebre | 1 975 | 25 | 1 950 | 0 | **1 950** | 86 (4 %) | 16 |
| Paüls | 1 922 | 0 | 1 922 | 0 | **1 922** | 198 (10 %) | 10 |
| Caseres | 1 886 | 0 | 1 886 | 0 | **1 886** | 73 (4 %) | 17 |
| Arnes | 1 877 | 0 | 1 877 | 0 | **1 877** | 144 (8 %) | 31 |
| la Pobla de Massaluca | 1 905 | 45 | 1 860 | 0 | **1 860** | 305 (16 %) | 8 |
| Ulldemolins | 1 686 | 0 | 1 686 | 0 | **1 686** | 99 (6 %) | 88 |
| la Palma d'Ebre | 1 689 | 7 | 1 682 | 0 | **1 682** | 127 (8 %) | 7 |
| Alforja | 1 680 | 0 | 1 680 | 0 | **1 680** | 57 (3 %) | 9 |
| el Vendrell | 1 623 | 2 | 1 621 | 0 | **1 621** | 21 (1 %) | 135 |
| Pratdip | 1 579 | 0 | 1 579 | 0 | **1 579** | 120 (8 %) | 50 |
| l'Ampolla | 1 563 | 5 | 1 558 | 0 | **1 558** | 421 (27 %) | 12 |
| el Pla de Santa Maria | 1 556 | 0 | 1 556 | 0 | **1 556** | 185 (12 %) | 49 |
| la Selva del Camp | 1 557 | 2 | 1 555 | 0 | **1 555** | 112 (7 %) | 88 |
| Cambrils | 1 548 | 1 | 1 547 | 0 | **1 547** | 89 (6 %) | 76 |
| Margalef | 1 539 | 8 | 1 531 | 0 | **1 531** | 301 (20 %) | 22 |
| Mont-ral | 1 526 | 0 | 1 526 | 0 | **1 526** | 15 (1 %) | 25 |
| Santa Coloma de Queralt | 1 522 | 0 | 1 522 | 0 | **1 522** | 268 (18 %) | 53 |
| Bot | 1 518 | 0 | 1 518 | 0 | **1 518** | 28 (2 %) | 7 |
| Godall | 1 474 | 1 | 1 473 | 0 | **1 473** | 185 (13 %) | 3 |
| Prades | 1 470 | 0 | 1 470 | 0 | **1 470** | 16 (1 %) | 60 |
| Vila-rodona | 1 460 | 0 | 1 460 | 0 | **1 460** | 191 (13 %) | 6 |
| Riudoms | 1 449 | 0 | 1 449 | 0 | **1 449** | 195 (13 %) | 16 |
| la Bisbal del Penedès | 1 447 | 0 | 1 447 | 0 | **1 447** | 86 (6 %) | 43 |
| Falset | 1 415 | 0 | 1 415 | 0 | **1 415** | 80 (6 %) | 23 |
| Cabacés | 1 382 | 0 | 1 382 | 0 | **1 382** | 152 (11 %) | 12 |
| Xerta | 1 414 | 35 | 1 379 | 0 | **1 379** | 189 (14 %) | 8 |
| Miravet | 1 429 | 51 | 1 378 | 0 | **1 378** | 114 (8 %) | 13 |
| Constantí | 1 373 | 5 | 1 368 | 28 | **1 340** | 157 (12 %) | 3 |
| Camarles | 1 297 | 0 | 1 297 | 0 | **1 297** | 280 (22 %) | 4 |
| Conesa | 1 297 | 0 | 1 297 | 0 | **1 297** | 255 (20 %) | 30 |
| l'Aldea | 1 319 | 22 | 1 297 | 0 | **1 297** | 215 (17 %) | 12 |
| Porrera | 1 274 | 1 | 1 273 | 0 | **1 273** | 131 (10 %) | 2 |
| Santa Bàrbara | 1 233 | 0 | 1 233 | 0 | **1 233** | 65 (5 %) |  |
| la Torre de l'Espanyol | 1 233 | 0 | 1 233 | 0 | **1 233** | 56 (5 %) | 3 |
| Passanant i Belltall | 1 227 | 0 | 1 227 | 0 | **1 227** | 157 (13 %) | 66 |
| Cabra del Camp | 1 191 | 0 | 1 191 | 0 | **1 191** | 83 (7 %) | 6 |
| la Galera | 1 191 | 0 | 1 191 | 0 | **1 191** | 36 (3 %) |  |
| Vinebre | 1 176 | 2 | 1 174 | 0 | **1 174** | 88 (7 %) | 5 |
| Barberà de la Conca | 1 170 | 0 | 1 170 | 0 | **1 170** | 65 (6 %) | 2 |
| el Catllar | 1 178 | 8 | 1 170 | 7 | **1 163** | 40 (3 %) | 44 |
| l'Aleixar | 1 163 | 0 | 1 163 | 0 | **1 163** | 32 (3 %) | 25 |
| Prat de Comte | 1 158 | 0 | 1 158 | 0 | **1 158** | 75 (6 %) | 7 |
| Bonastre | 1 102 | 0 | 1 102 | 0 | **1 102** | 34 (3 %) | 21 |
| Sant Jaume dels Domenys | 1 087 | 0 | 1 087 | 0 | **1 087** | 29 (3 %) | 26 |
| Llorac | 1 049 | 0 | 1 049 | 0 | **1 049** | 164 (16 %) | 13 |
| Vilaplana | 1 023 | 2 | 1 021 | 0 | **1 021** | 15 (1 %) | 13 |
| el Molar | 1 017 | 0 | 1 017 | 0 | **1 017** | 122 (12 %) | 1 |
| Benissanet | 1 023 | 11 | 1 012 | 0 | **1 012** | 86 (8 %) | 5 |
| Figuerola del Camp | 1 005 | 0 | 1 005 | 0 | **1 005** | 37 (4 %) | 4 |
| les Piles | 996 | 1 | 995 | 0 | **995** | 183 (18 %) |  |
| Capçanes | 991 | 3 | 988 | 0 | **988** | 35 (4 %) | 14 |
| Pradell de la Teixeta | 975 | 0 | 975 | 0 | **975** | 97 (10 %) | 9 |
| el Pont d'Armentera | 960 | 2 | 958 | 0 | **958** | 147 (15 %) | 7 |
| Vila-seca | 959 | 4 | 955 | 0 | **955** | 45 (5 %) | 50 |
| Solivella | 950 | 0 | 950 | 0 | **950** | 56 (6 %) | 2 |
| Vilanova de Prades | 948 | 2 | 946 | 0 | **946** | 27 (3 %) | 5 |
| Arbolí | 920 | 0 | 920 | 0 | **920** | 8 (1 %) | 6 |
| Calafell | 896 | 0 | 896 | 0 | **896** |  | 250 |
| l'Albiol | 897 | 1 | 896 | 0 | **896** | 40 (4 %) | 11 |
| Albinyana | 867 | 1 | 866 | 0 | **866** | 12 (1 %) | 36 |
| Aldover | 883 | 17 | 866 | 0 | **866** | 131 (15 %) | 4 |
| Montferri | 860 | 0 | 860 | 0 | **860** | 55 (6 %) | 4 |
| Riudecols | 859 | 0 | 859 | 0 | **859** | 18 (2 %) | 5 |
| la Figuera | 820 | 1 | 819 | 0 | **819** | 67 (8 %) | 18 |
| Vilabella | 809 | 3 | 806 | 0 | **806** | 68 (8 %) | 3 |
| Vespella de Gaià | 801 | 8 | 793 | 0 | **793** | 69 (9 %) | 6 |
| la Secuita | 785 | 0 | 785 | 0 | **785** | 55 (7 %) | 34 |
| Vilanova d'Escornalbou | 767 | 0 | 767 | 0 | **767** | 31 (4 %) | 32 |
| Freginals | 757 | 0 | 757 | 0 | **757** | 152 (20 %) |  |
| Forès | 738 | 0 | 738 | 0 | **738** | 137 (19 %) |  |
| Riudecanyes | 752 | 15 | 737 | 0 | **737** | 16 (2 %) | 10 |
| Roda de Berà | 735 | 0 | 735 | 0 | **735** | 2 (0 %) | 63 |
| Vallmoll | 729 | 0 | 729 | 0 | **729** | 92 (13 %) | 3 |
| Marçà | 712 | 0 | 712 | 0 | **712** | 26 (4 %) | 6 |
| la Febró | 704 | 0 | 704 | 0 | **704** | 18 (3 %) | 9 |
| el Masroig | 697 | 0 | 697 | 0 | **697** | 36 (5 %) | 2 |
| Ginestar | 691 | 7 | 684 | 0 | **684** | 59 (9 %) | 2 |
| Móra la Nova | 695 | 18 | 677 | 0 | **677** | 21 (3 %) | 1 |
| Salou | 665 | 3 | 662 | 0 | **662** | 21 (3 %) | 307 |
| Savallà del Comtat | 652 | 0 | 652 | 0 | **652** | 99 (15 %) | 4 |
| Blancafort | 645 | 0 | 645 | 0 | **645** | 5 (1 %) | 5 |
| Masdenverge | 636 | 0 | 636 | 0 | **636** | 91 (14 %) |  |
| Colldejou | 634 | 0 | 634 | 0 | **634** | 18 (3 %) | 34 |
| l'Arboç | 628 | 0 | 628 | 0 | **628** | 20 (3 %) | 33 |
| la Bisbal de Montsant | 620 | 0 | 620 | 0 | **620** | 61 (10 %) | 6 |
| Poboleda | 604 | 1 | 603 | 0 | **603** | 115 (19 %) | 23 |
| Duesaigües | 602 | 0 | 602 | 0 | **602** | 22 (4 %) | 3 |
| Capafonts | 598 | 0 | 598 | 0 | **598** | 17 (3 %) | 55 |
| Vallclara | 597 | 0 | 597 | 0 | **597** | 18 (3 %) | 7 |
| Gratallops | 591 | 0 | 591 | 0 | **591** | 44 (7 %) | 2 |
| Torroja del Priorat | 586 | 0 | 586 | 0 | **586** | 61 (10 %) | 7 |
| Vilaverd | 558 | 0 | 558 | 0 | **558** | 12 (2 %) | 1 |
| la Pobla de Montornès | 545 | 0 | 545 | 0 | **545** | 21 (4 %) | 19 |
| Banyeres del Penedès | 538 | 0 | 538 | 0 | **538** | 9 (2 %) | 42 |
| Salomó | 538 | 0 | 538 | 0 | **538** | 25 (5 %) |  |
| Botarell | 527 | 0 | 527 | 0 | **527** | 65 (12 %) | 1 |
| Senan | 527 | 0 | 527 | 0 | **527** | 18 (3 %) | 6 |
| els Guiamets | 521 | 21 | 500 | 0 | **500** | 19 (4 %) | 2 |
| Vallfogona de Riucorb | 496 | 0 | 496 | 0 | **496** | 68 (14 %) | 9 |
| Vinyols i els Arcs | 477 | 0 | 477 | 0 | **477** | 50 (10 %) | 7 |
| Nulles | 476 | 0 | 476 | 0 | **476** | 71 (15 %) | 4 |
| Montbrió del Camp | 467 | 0 | 467 | 0 | **467** | 28 (6 %) | 12 |
| Creixell | 460 | 0 | 460 | 0 | **460** | 2 (0 %) | 25 |
| l'Argentera | 438 | 0 | 438 | 0 | **438** | 12 (3 %) | 9 |
| Cunit | 432 | 0 | 432 | 0 | **432** | 1 (0 %) | 51 |
| Perafort | 423 | 1 | 422 | 0 | **422** | 22 (5 %) | 2 |
| Puigpelat | 422 | 0 | 422 | 0 | **422** | 30 (7 %) | 6 |
| Santa Oliva | 421 | 1 | 420 | 0 | **420** | 15 (4 %) | 12 |
| Vilallonga del Camp | 401 | 2 | 399 | 0 | **399** | 30 (8 %) | 1 |
| Bellmunt del Priorat | 396 | 0 | 396 | 0 | **396** | 8 (2 %) | 2 |
| Torredembarra | 388 | 1 | 387 | 0 | **387** | 8 (2 %) | 34 |
| la Riera de Gaià | 385 | 0 | 385 | 0 | **385** | 12 (3 %) | 5 |
| Rocafort de Queralt | 378 | 0 | 378 | 0 | **378** | 22 (6 %) | 2 |
| Rodonyà | 369 | 0 | 369 | 0 | **369** | 34 (9 %) | 2 |
| Bellvei | 368 | 0 | 368 | 0 | **368** | 5 (1 %) | 15 |
| les Borges del Camp | 368 | 0 | 368 | 0 | **368** | 4 (1 %) | 1 |
| Pira | 359 | 0 | 359 | 0 | **359** | 3 (1 %) |  |
| la Riba | 354 | 0 | 354 | 0 | **354** | 12 (3 %) | 4 |
| Renau | 370 | 17 | 353 | 0 | **353** | 22 (6 %) | 5 |
| la Canonja | 325 | 0 | 325 | 0 | **325** | 18 (6 %) | 1 |
| Alió | 322 | 0 | 322 | 0 | **322** | 36 (11 %) | 4 |
| la Torre de Fontaubella | 311 | 0 | 311 | 0 | **311** | 23 (7 %) | 5 |
| Altafulla | 307 | 0 | 307 | 0 | **307** | 11 (4 %) | 9 |
| el Lloar | 302 | 0 | 302 | 0 | **302** | 45 (15 %) |  |
| Masllorenç | 289 | 0 | 289 | 0 | **289** | 13 (4 %) | 1 |
| Bràfim | 282 | 0 | 282 | 0 | **282** | 34 (12 %) | 16 |
| la Pobla de Mafumet | 276 | 0 | 276 | 0 | **276** | 10 (4 %) | 3 |
| Almoster | 263 | 0 | 263 | 0 | **263** | 6 (2 %) | 1 |
| el Morell | 258 | 1 | 257 | 0 | **257** | 19 (7 %) | 2 |
| la Vilella Baixa | 243 | 0 | 243 | 0 | **243** | 23 (9 %) | 16 |
| Castellvell del Camp | 229 | 0 | 229 | 0 | **229** |  | 5 |
| la Vilella Alta | 229 | 0 | 229 | 0 | **229** | 43 (19 %) |  |
| els Pallaresos | 220 | 0 | 220 | 0 | **220** | 3 (1 %) | 15 |
| Llorenç del Penedès | 211 | 0 | 211 | 0 | **211** | 6 (3 %) | 22 |
| la Nou de Gaià | 183 | 0 | 183 | 0 | **183** | 3 (2 %) | 1 |
| el Milà | 179 | 0 | 179 | 0 | **179** | 12 (7 %) |  |
| la Masó | 160 | 1 | 159 | 0 | **159** | 11 (7 %) |  |
| Maspujols | 156 | 0 | 156 | 0 | **156** | 2 (1 %) | 1 |
| els Garidells | 136 | 0 | 136 | 0 | **136** | 5 (4 %) |  |
| el Rourell | 104 | 0 | 104 | 0 | **104** | 9 (9 %) |  |

## Parcs (5000)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Forêt de Querol (34) ⚠️ | Querol › Alt Camp | 972 |
| Forêt de Horta de Sant Joan (37) ⚠️ | Horta de Sant Joan › Terra Alta | 818 |
| Forêt de la Febró (8) ⚠️ | la Febró › Baix Camp | 573 |
| Forêt de el Montmell (7) ⚠️ | el Montmell › Baix Penedès | 541 |
| Forêt de Tivissa (9) ⚠️ | Tivissa › Ribera d'Ebre | 533 |
| Forêt de Montblanc (16) ⚠️ | Montblanc › Conca de Barberà | 521 |
| Forêt de Montblanc ⚠️ | Montblanc › Conca de Barberà | 497 |
| Forêt de Móra d'Ebre (11) ⚠️ | Móra d'Ebre › Ribera d'Ebre | 495 |
| Forêt de Vimbodí i Poblet (9) ⚠️ | Vimbodí i Poblet › Conca de Barberà | 477 |
| Forêt de Rasquera (7) ⚠️ | Rasquera › Ribera d'Ebre | 471 |
| Barranc del Restós ⚠️ | Cornudella de Montsant › Priorat | 449 |
| Forêt de Tivissa (6) ⚠️ | Tivissa › Priorat | 444 |
| Forêt de Prades (55) ⚠️ | Prades › Baix Camp | 441 |
| Forêt de Ulldemolins (84) ⚠️ | Ulldemolins › Priorat | 419 |
| Forêt de la Sénia (31) ⚠️ | la Sénia › Montsià | 385 |
| Forêt de la Torre de l'Espanyol (2) ⚠️ | la Torre de l'Espanyol › Ribera d'Ebre | 376 |
| Forêt de Batea (7) ⚠️ | Batea › Terra Alta | 370 |
| Forêt de Cabacés (6) ⚠️ | Cabacés › Priorat | 368 |
| Forêt de Montblanc (14) ⚠️ | Montblanc › Conca de Barberà | 367 |
| Forêt de Tivissa (12) ⚠️ | Tivissa › Ribera d'Ebre | 355 |
| Forêt de Corbera d'Ebre (5) ⚠️ | Corbera d'Ebre › Terra Alta | 355 |
| Forêt de el Masroig (2) ⚠️ | el Masroig › Priorat | 352 |
| Forêt de Arbolí (6) ⚠️ | Arbolí › Baix Camp | 341 |
| Forêt de Falset (6) ⚠️ | Falset › Priorat | 330 |
| Forêt de Paüls ⚠️ | Paüls › Baix Ebre | 325 |
| Forêt de Montferri (3) ⚠️ | Montferri › Alt Camp | 321 |
| Forêt de la Sénia (32) ⚠️ | la Sénia › Montsià | 321 |
| Forêt de el Vendrell (35) ⚠️ | el Vendrell › Baix Penedès | 320 |
| Forêt de el Montmell (5) ⚠️ | el Montmell › Baix Penedès | 311 |
| Forêt de Tivissa (22) ⚠️ | Tivissa › Ribera d'Ebre | 311 |
| Forêt de Vilanova de Prades (6) ⚠️ | Vilanova de Prades › Conca de Barberà | 303 |
| Forêt de Batea (10) ⚠️ | Batea › Terra Alta | 299 |
| Forêt de Bot (2) ⚠️ | Bot › Terra Alta | 299 |
| Forêt de Vimbodí i Poblet (24) ⚠️ | Vimbodí i Poblet › Conca de Barberà | 299 |
| Forêt de Ascó (6) ⚠️ | Ascó › Ribera d'Ebre | 297 |
| Forêt de l'Aleixar (21) ⚠️ | l'Aleixar › Baix Camp | 297 |
| Forêt de Cabacés (2) ⚠️ | Cabacés › Priorat | 291 |
| Forêt de Vilalba dels Arcs (9) ⚠️ | Vilalba dels Arcs › Terra Alta | 287 |
| Forêt de Prat de Comte ⚠️ | Prat de Comte › Terra Alta | 286 |
| Forêt de el Pinell de Brai (7) ⚠️ | el Pinell de Brai › Terra Alta | 280 |
| Bois de Pontils (2) ⚠️ | Pontils › Conca de Barberà | 266 |
| Forêt de Garcia (5) ⚠️ | Garcia › Ribera d'Ebre | 265 |
| Forêt de la Bisbal de Montsant (3) ⚠️ | la Bisbal de Montsant › Ribera d'Ebre | 264 |
| Forêt de la Fatarella (6) ⚠️ | la Fatarella › Terra Alta | 261 |
| Forêt de Sant Jaume dels Domenys ⚠️ | Sant Jaume dels Domenys › Baix Penedès | 261 |
| Forêt de Vimbodí i Poblet (8) ⚠️ | Vimbodí i Poblet › Conca de Barberà | 260 |
| Forêt de Ulldemolins (85) ⚠️ | Ulldemolins › Priorat | 260 |
| Forêt de Montblanc (15) ⚠️ | Montblanc › Conca de Barberà | 259 |
| Forêt de Arnes (3) ⚠️ | Arnes › Terra Alta | 257 |
| Forêt de Gandesa (3) ⚠️ | Gandesa › Terra Alta | 255 |
| Forêt de Vilaverd ⚠️ | Vilaverd › Conca de Barberà | 255 |
| Forêt de Flix (30) ⚠️ | Flix › Ribera d'Ebre | 254 |
| Forêt de Capçanes (3) ⚠️ | Capçanes › Priorat | 252 |
| Forêt de Vallclara (5) ⚠️ | Vallclara › Conca de Barberà | 250 |
| Forêt de Alforja (3) ⚠️ | Alforja › Baix Camp | 249 |
| Forêt de Tivissa (23) ⚠️ | Tivissa › Ribera d'Ebre | 248 |
| Forêt de Mont-ral (18) ⚠️ | Mont-ral › Alt Camp | 248 |
| Forêt de Arbolí (5) ⚠️ | Arbolí › Baix Camp | 245 |
| Forêt de Horta de Sant Joan (17) ⚠️ | Horta de Sant Joan › Terra Alta | 244 |
| Forêt de Riba-roja d'Ebre (15) ⚠️ | Riba-roja d'Ebre › Ribera d'Ebre | 242 |
| Forêt de Cornudella de Montsant (154) ⚠️ | Cornudella de Montsant › Priorat | 235 |
| Forêt de la Pobla de Massaluca (6) ⚠️ | la Pobla de Massaluca › Terra Alta | 227 |
| Forêt de Prat de Comte (2) ⚠️ | Prat de Comte › Terra Alta | 223 |
| Forêt de Prades (56) ⚠️ | Prades › Baix Camp | 220 |
| Forêt de la Pobla de Massaluca (3) ⚠️ | la Pobla de Massaluca › Terra Alta | 214 |
| Forêt de la Fatarella (2) ⚠️ | la Fatarella › Terra Alta | 212 |
| Forêt de Aiguamúrcia ⚠️ | Aiguamúrcia › Alt Camp | 211 |
| Forêt de Riba-roja d'Ebre (16) ⚠️ | Riba-roja d'Ebre › Ribera d'Ebre | 211 |
| Forêt de Cabra del Camp (4) ⚠️ | Cabra del Camp › Alt Camp | 210 |
| Forêt de Alfara de Carles (2) ⚠️ | Alfara de Carles › Baix Ebre | 205 |
| Forêt de Flix (26) ⚠️ | Flix › Ribera d'Ebre | 204 |
| Forêt de Bonastre (10) ⚠️ | Bonastre › Baix Penedès | 203 |
| Forêt de Benifallet (8) ⚠️ | Benifallet › Baix Ebre | 201 |
| Forêt de Arnes (2) ⚠️ | Arnes › Baix Ebre | 199 |
| Forêt de Sarral (4) ⚠️ | Sarral › Conca de Barberà | 196 |
| Forêt de Duesaigües ⚠️ | Duesaigües › Baix Camp | 191 |
| Forêt de la Fatarella ⚠️ | la Fatarella › Terra Alta | 190 |
| Bois de Pontils ⚠️ | Pontils › Conca de Barberà | 190 |
| Forêt de Tortosa (6) ⚠️ | Tortosa › Baix Ebre | 186 |
| Forêt de Horta de Sant Joan (22) ⚠️ | Horta de Sant Joan › Terra Alta | 185 |
| Forêt de Bonastre (6) ⚠️ | Bonastre › Baix Penedès | 185 |
| Forêt de Vilaplana (2) ⚠️ | Vilaplana › Baix Camp | 183 |
| Bois de Senan (7) ⚠️ | Senan › Conca de Barberà | 181 |
| Forêt de Vilalba dels Arcs (10) ⚠️ | Vilalba dels Arcs › Terra Alta | 180 |
| Forêt de Horta de Sant Joan (38) ⚠️ | Horta de Sant Joan › Terra Alta | 180 |
| Bois de Tarragona ⚠️ | Tarragona › Tarragonès | 178 |
| Forêt de la Sénia (41) ⚠️ | la Sénia › Montsià | 174 |
| Forêt de Roquetes (5) ⚠️ | Roquetes › Baix Ebre | 173 |
| Forêt de Cornudella de Montsant (4) ⚠️ | Cornudella de Montsant › Priorat | 172 |
| Forêt de Vilaplana (11) ⚠️ | Vilaplana › Baix Camp | 172 |
| Forêt de Alcover ⚠️ | Alcover › Alt Camp | 168 |
| Forêt de Gratallops ⚠️ | Gratallops › Priorat | 168 |
| Forêt de Ascó (4) ⚠️ | Ascó › Ribera d'Ebre | 168 |
| Forêt de Tortosa (45) ⚠️ | Tortosa › Baix Ebre | 167 |
| Forêt de la Fatarella (5) ⚠️ | la Fatarella › Terra Alta | 162 |
| Forêt de Alfara de Carles (5) ⚠️ | Alfara de Carles › Baix Ebre | 160 |
| Forêt de Prat de Comte (4) ⚠️ | Prat de Comte › Terra Alta | 160 |
| Forêt de Caseres (6) ⚠️ | Caseres › Terra Alta | 159 |
| Forêt de Gandesa ⚠️ | Gandesa › Terra Alta | 158 |
| Forêt de Vinebre (3) ⚠️ | Vinebre › Ribera d'Ebre | 158 |
| Forêt de la Palma d'Ebre (7) ⚠️ | la Palma d'Ebre › Ribera d'Ebre | 158 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (14) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 158 |
| Forêt de la Torre de l'Espanyol (3) ⚠️ | la Torre de l'Espanyol › Ribera d'Ebre | 157 |
| Forêt de Mont-ral (21) ⚠️ | Mont-ral › Alt Camp | 157 |
| Forêt de Arnes (13) ⚠️ | Arnes › Terra Alta | 154 |
| Forêt de Capafonts (49) ⚠️ | Capafonts › Baix Camp | 154 |
| Forêt de Benifallet (2) ⚠️ | Benifallet › Baix Ebre | 152 |
| Bois de Masllorenç ⚠️ | Masllorenç › Baix Penedès | 151 |
| Forêt de Corbera d'Ebre (7) ⚠️ | Corbera d'Ebre › Terra Alta | 149 |
| Forêt de Tarragona (18) ⚠️ | Tarragona › Tarragonès | 149 |
| Forêt de Riba-roja d'Ebre (2) ⚠️ | Riba-roja d'Ebre › Ribera d'Ebre | 148 |
| Forêt de Bot ⚠️ | Bot › Terra Alta | 147 |
| Forêt de la Sénia (54) ⚠️ | la Sénia › Montsià | 147 |
| Forêt de Paüls (6) ⚠️ | Paüls › Baix Ebre | 146 |
| Forêt de Roquetes (4) ⚠️ | Alfara de Carles › Baix Ebre | 146 |
| Forêt de Vilalba dels Arcs (8) ⚠️ | Vilalba dels Arcs › Terra Alta | 146 |
| Forêt de Aiguamúrcia (27) ⚠️ | Aiguamúrcia › Alt Camp | 145 |
| Forêt de Capçanes (2) ⚠️ | Capçanes › Priorat | 144 |
| Forêt de la Sénia (52) ⚠️ | la Sénia › Montsià | 144 |
| Forêt de Vila-rodona (4) ⚠️ | Vila-rodona › Alt Camp | 143 |
| Forêt de Roquetes (13) ⚠️ | Roquetes › Baix Ebre | 141 |
| Forêt de Mont-ral (20) ⚠️ | Mont-ral › Alt Camp | 139 |
| Forêt de Alfara de Carles (18) ⚠️ | Alfara de Carles › Baix Ebre | 139 |
| Forêt de la Morera de Montsant (4) ⚠️ | la Morera de Montsant › Priorat | 138 |
| Forêt de el Perelló ⚠️ | el Perelló › Baix Ebre | 136 |
| Forêt de Vimbodí i Poblet (22) ⚠️ | Vimbodí i Poblet › Conca de Barberà | 135 |
| Forêt de Prades ⚠️ | Prades › Baix Camp | 134 |
| Forêt de Alcover (2) ⚠️ | Alcover › Alt Camp | 132 |
| Forêt de Horta de Sant Joan (11) ⚠️ | Horta de Sant Joan › Terra Alta | 131 |
| Forêt de Roda de Berà (7) ⚠️ | Roda de Berà › Tarragonès | 131 |
| Forêt de Tivissa (14) ⚠️ | Tivissa › Ribera d'Ebre | 130 |
| Forêt de Bonastre (13) ⚠️ | Creixell › Tarragonès | 129 |
| Forêt de Horta de Sant Joan (14) ⚠️ | Horta de Sant Joan › Terra Alta | 127 |
| Forêt de Riudecols ⚠️ | Riudecols › Baix Camp | 126 |
| Forêt de Bonastre (12) | Albinyana › Baix Penedès | 125 |
| Forêt de Querol (52) | Querol › Alt Camp | 124 |
| Bois de Senan (5) | Senan › Conca de Barberà | 123 |
| Forêt de Pratdip (3) | Pratdip › Baix Camp | 121 |
| Forêt de Arnes (4) | Arnes › Terra Alta | 120 |
| Forêt de Roquetes (3) | Roquetes › Baix Ebre | 120 |
| Forêt de Prades (8) | Prades › Baix Camp | 120 |
| Forêt de la Sénia (40) | la Sénia › Montsià | 120 |
| Forêt de Benifallet | Benifallet › Baix Ebre | 119 |
| Forêt de l'Ametlla de Mar (187) | l'Ametlla de Mar › Baix Ebre | 119 |
| Forêt de Creixell (5) | Creixell › Tarragonès | 119 |
| Forêt de Pontils (3) | Pontils › Conca de Barberà | 117 |
| Forêt de Flix (7) | Flix › Ribera d'Ebre | 117 |
| Forêt de Benifallet (6) | Benifallet › Baix Ebre | 115 |
| Forêt de Caseres (9) | Caseres › Terra Alta | 115 |
| Forêt de Roquetes (12) | Roquetes › Baix Ebre | 115 |
| Forêt de Alforja | Alforja › Baix Camp | 114 |
| Forêt de Riba-roja d'Ebre (13) | Riba-roja d'Ebre › Ribera d'Ebre | 114 |
| Forêt de Ginestar | Ginestar › Ribera d'Ebre | 113 |
| Forêt de Margalef (10) | Margalef › Priorat | 113 |
| Forêt de Horta de Sant Joan (15) | Horta de Sant Joan › Terra Alta | 112 |
| Forêt de Pontils (10) | Pontils › Conca de Barberà | 112 |
| Forêt de Mont-ral | Mont-ral › Alt Camp | 110 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (7) | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 107 |
| Forêt de Benifallet (13) | Benifallet › Baix Ebre | 107 |
| Bois de Tivenys (2) | Tivenys › Baix Ebre | 106 |
| Forêt de la Nou de Gaià | la Nou de Gaià › Tarragonès | 106 |
| Forêt de Cunit (10) | Cunit › Baix Penedès | 105 |
| Forêt de Flix (8) | Flix › Ribera d'Ebre | 104 |
| Bois de Alcover (16) | Alcover › Alt Camp | 104 |
| Forêt de la Sénia (51) | la Sénia › Montsià | 104 |
| Forêt de el Montmell (12) | el Montmell › Baix Penedès | 102 |
| Forêt de Tivissa (7) | Tivissa › Ribera d'Ebre | 100 |
| Forêt de la Fatarella (8) | la Fatarella › Terra Alta | 100 |
| Forêt de Arbolí (2) | Arbolí › Baix Camp | 98 |
| Bois de Blancafort (2) | Blancafort › Conca de Barberà | 98 |
| Forêt de Vilaplana (12) | Vilaplana › Baix Camp | 98 |
| Forêt de Savallà del Comtat (2) | Savallà del Comtat › Conca de Barberà | 97 |
| Forêt de Ascó (2) | Ascó › Ribera d'Ebre | 96 |
| Forêt de Figuerola del Camp (3) | Figuerola del Camp › Alt Camp | 95 |
| Forêt de Cornudella de Montsant (148) | Cornudella de Montsant › Priorat | 94 |
| Forêt de Mont-ral (16) | Mont-ral › Alt Camp | 93 |
| Forêt de el Pinell de Brai | el Pinell de Brai › Terra Alta | 92 |
| Forêt de Vilaplana (4) | Vilaplana › Baix Camp | 92 |
| Forêt de Prades (58) | Prades › Baix Camp | 91 |
| Forêt de Aiguamúrcia (2) | Aiguamúrcia › Alt Camp | 90 |
| Forêt de la Febró (2) | la Febró › Baix Camp | 90 |
| Forêt de Margalef (2) | Margalef › Priorat | 90 |
| Forêt de Figuerola del Camp | Figuerola del Camp › Alt Camp | 90 |
| Forêt de Renau | Renau › Tarragonès | 89 |
| Forêt de Margalef (6) | Margalef › Priorat | 87 |
| Forêt de Vimbodí i Poblet (21) | Vimbodí i Poblet › Conca de Barberà | 87 |
| Forêt de Horta de Sant Joan (27) | Horta de Sant Joan › Terra Alta | 87 |
| Forêt de l'Espluga de Francolí (11) | l'Espluga de Francolí › Conca de Barberà | 87 |
| Forêt de el Perelló (3) | el Perelló › Baix Ebre | 86 |
| Forêt de Móra d'Ebre (4) | Móra d'Ebre › Ribera d'Ebre | 84 |
| Bois de Montblanc (17) | Montblanc › Conca de Barberà | 84 |
| Forêt de Flix (3) | Flix › Ribera d'Ebre | 83 |
| Forêt de el Montmell (3) | el Montmell › Baix Penedès | 83 |
| Forêt de la Ràpita | la Ràpita › Montsià | 83 |
| Forêt de Flix (4) | Flix › Ribera d'Ebre | 81 |
| Forêt de Querol (23) | Querol › Alt Camp | 81 |
| Forêt de Tivissa (17) | Tivissa › Ribera d'Ebre | 80 |
| Forêt de Montblanc (17) | Montblanc › Conca de Barberà | 80 |
| Forêt de Margalef (18) | Margalef › Priorat | 80 |
| Forêt de Pontils (14) | Pontils › Conca de Barberà | 80 |
| Forêt de Riudecanyes (9) | Riudecanyes › Baix Camp | 79 |
| Forêt de Garcia (6) | Garcia › Ribera d'Ebre | 78 |
| Forêt de Montferri (2) | Montferri › Alt Camp | 78 |
| Forêt de Tarragona (54) | Tarragona › Tarragonès | 78 |
| Bois de Alcover (17) | Alcover › Alt Camp | 78 |
| Forêt de el Montmell (6) | el Montmell › Baix Penedès | 77 |
| Forêt de Aiguamúrcia (11) | Aiguamúrcia › Alt Camp | 77 |
| la Rojala | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 77 |
| Forêt de Albinyana (18) | Albinyana › Baix Penedès | 76 |
| Forêt de Bonastre (11) | Bonastre › Baix Penedès | 76 |
| Forêt de Tortosa (38) | Tortosa › Baix Ebre | 76 |
| Forêt de Batea (21) | Batea › Terra Alta | 75 |
| Forêt de Caseres (4) | Caseres › Terra Alta | 74 |
| Forêt de Móra d'Ebre (5) | Móra d'Ebre › Ribera d'Ebre | 74 |
| Forêt de la Palma d'Ebre (5) | la Palma d'Ebre › Ribera d'Ebre | 73 |
| Forêt de Querol (9) | Querol › Alt Camp | 73 |
| Forêt de Mas de Barberans | Mas de Barberans › Montsià | 72 |
| Forêt de Flix (28) | Flix › Ribera d'Ebre | 72 |
| Forêt de Horta de Sant Joan (32) | Horta de Sant Joan › Terra Alta | 72 |
| Forêt de Cabacés (3) | Cabacés › Priorat | 71 |
| Forêt de Garcia (4) | Garcia › Ribera d'Ebre | 71 |
| Forêt de Paüls (8) | Paüls › Baix Ebre | 71 |
| Forêt de Querol (30) | Querol › Alt Camp | 71 |
| Forêt de Prades (2) | Prades › Baix Camp | 70 |
| Forêt de Pontils (8) | Pontils › Conca de Barberà | 70 |
| Bois de la Bisbal del Penedès (7) | la Bisbal del Penedès › Baix Penedès | 70 |
| Forêt de Calafell (49) | Calafell › Baix Penedès | 70 |
| Forêt de Tortosa (5) | Tortosa › Baix Ebre | 69 |
| Forêt de la Sénia (45) | la Sénia › Montsià | 69 |
| Forêt de la Sénia (50) | la Sénia › Montsià | 69 |
| Forêt de Colldejou (30) | Colldejou › Baix Camp | 69 |
| Forêt de Vimbodí i Poblet (3) | Vimbodí i Poblet › Conca de Barberà | 68 |
| Forêt de Riba-roja d'Ebre | Riba-roja d'Ebre › Ribera d'Ebre | 68 |
| Forêt de Tivenys (3) | Tivenys › Baix Ebre | 68 |
| Forêt de Porrera | Porrera › Priorat | 67 |
| Forêt de l'Albiol (2) | l'Albiol › Baix Camp | 67 |
| Forêt de Bonastre (15) | Bonastre › Baix Penedès | 67 |
| Forêt de Montblanc (19) | Montblanc › Conca de Barberà | 67 |
| Forêt de la Pobla de Massaluca (2) | la Pobla de Massaluca › Terra Alta | 66 |
| Forêt de Batea (4) | Batea › Terra Alta | 66 |
| Forêt de Alfara de Carles (9) | Alfara de Carles › Baix Ebre | 66 |
| Forêt de Tivissa (11) | Tivissa › Ribera d'Ebre | 65 |
| Forêt de Alforja (2) | Alforja › Baix Camp | 65 |
| Forêt de Pontils (9) | Pontils › Conca de Barberà | 64 |
| Forêt de Vilaplana (5) | Vilaplana › Baix Camp | 64 |
| Bois de Conesa (2) | Conesa › Conca de Barberà | 64 |
| Forêt de la Morera de Montsant (22) | la Morera de Montsant › Priorat | 64 |
| Forêt de Bonastre (14) | Bonastre › Baix Penedès | 64 |
| Forêt de Alfara de Carles | Alfara de Carles › Baix Ebre | 63 |
| Forêt de Arbolí | Arbolí › Baix Camp | 63 |
| Forêt de Horta de Sant Joan (21) | Horta de Sant Joan › Terra Alta | 63 |
| Forêt de Corbera d'Ebre (6) | Corbera d'Ebre › Terra Alta | 63 |
| Forêt de l'Espluga de Francolí (8) | l'Espluga de Francolí › Conca de Barberà | 62 |
| Forêt de Mont-ral (13) | Mont-ral › Alt Camp | 62 |
| Forêt de Mont-ral (25) | Mont-ral › Alt Camp | 62 |
| Forêt de Torroja del Priorat | Torroja del Priorat › Priorat | 61 |
| Forêt de Conesa (3) | Conesa › Conca de Barberà | 61 |
| Forêt de Pontils (6) | Pontils › Conca de Barberà | 61 |
| Forêt de Batea (24) | Batea › Terra Alta | 61 |
| Forêt de l'Ametlla de Mar (115) | l'Ametlla de Mar › Baix Ebre | 61 |
| Forêt de Querol (32) | Querol › Alt Camp | 61 |
| Forêt de Perafort | Perafort › Tarragonès | 60 |
| Forêt de la Febró | la Febró › Baix Camp | 60 |
| Forêt de la Figuera (4) | la Figuera › Priorat | 60 |
| Forêt de l'Argentera (8) | l'Argentera › Baix Camp | 60 |
| Forêt de Pontils (15) | Pontils › Conca de Barberà | 60 |
| Forêt de Conesa | Conesa › Conca de Barberà | 59 |
| Forêt de Conesa (2) | Conesa › Conca de Barberà | 59 |
| Forêt de Gandesa (2) | Gandesa › Terra Alta | 59 |
| Forêt de Flix (25) | Flix › Ribera d'Ebre | 59 |
| Forêt de Flix | Flix › Ribera d'Ebre | 58 |
| Forêt de la Palma d'Ebre (4) | la Palma d'Ebre › Ribera d'Ebre | 58 |
| Bois de Alcover | Alcover › Alt Camp | 58 |
| Forêt de Roda de Berà (9) | Roda de Berà › Tarragonès | 58 |
| Forêt de Paüls (2) | Paüls › Baix Ebre | 57 |
| Forêt de Mas de Barberans (2) | Mas de Barberans › Montsià | 57 |
| Forêt de la Bisbal del Penedès (25) | la Bisbal del Penedès › Baix Penedès | 57 |
| Forêt de Prades (59) | Prades › Baix Camp | 57 |
| Forêt de Vilabella | Vilabella › Alt Camp | 57 |
| Forêt de el Molar | el Molar › Priorat | 56 |
| Forêt de Arbolí (3) | Arbolí › Baix Camp | 56 |
| Forêt de la Figuera (5) | la Figuera › Priorat | 56 |
| Forêt de el Vendrell (41) | el Vendrell › Baix Penedès | 56 |
| Forêt de Horta de Sant Joan | Horta de Sant Joan › Terra Alta | 55 |
| Forêt de Vilalba dels Arcs (3) | Vilalba dels Arcs › Terra Alta | 55 |
| Bois de Passanant i Belltall (5) | Passanant i Belltall › Conca de Barberà | 55 |
| Forêt de Tivissa (15) | Tivissa › Ribera d'Ebre | 55 |
| Forêt de Horta de Sant Joan (24) | Horta de Sant Joan › Terra Alta | 55 |
| Forêt de Albinyana (17) | Albinyana › Baix Penedès | 55 |
| Forêt de Pontils (16) | Pontils › Conca de Barberà | 55 |
| Forêt de el Pont d'Armentera (2) | el Pont d'Armentera › Alt Camp | 55 |
| Forêt de Tivissa (24) | Tivissa › Ribera d'Ebre | 54 |
| Forêt de el Vendrell (34) | el Vendrell › Baix Penedès | 54 |
| Forêt de Bellvei | Bellvei › Baix Penedès | 53 |
| Forêt de Aiguamúrcia (12) | Aiguamúrcia › Alt Camp | 53 |
| Forêt de Vimbodí i Poblet (20) | Vallclara › Conca de Barberà | 53 |
| Forêt de Aiguamúrcia (25) | Aiguamúrcia › Alt Camp | 53 |
| Forêt de Flix (27) | Flix › Ribera d'Ebre | 52 |
| Forêt de Pratdip (4) | Pratdip › Baix Camp | 52 |
| Forêt de Margalef (19) | Margalef › Priorat | 52 |
| Forêt de Paüls (7) | Paüls › Baix Ebre | 51 |
| Forêt de Horta de Sant Joan (28) | Horta de Sant Joan › Terra Alta | 51 |
| Forêt de Arnes (8) | Arnes › Terra Alta | 50 |
| Forêt de Montblanc (4) | Montblanc › Conca de Barberà | 50 |
| Forêt de Duesaigües (2) | Duesaigües › Baix Camp | 50 |
| Forêt de Vimbodí i Poblet (23) | Vimbodí i Poblet › Conca de Barberà | 50 |
| Forêt de Riudecanyes (3) | Riudecanyes › Baix Camp | 50 |
| Forêt de Roda de Berà (8) | Roda de Berà › Tarragonès | 50 |
| Forêt de Vilalba dels Arcs | Vilalba dels Arcs › Terra Alta | 49 |
| Forêt de Tivissa (20) | Tivissa › Ribera d'Ebre | 49 |
| Forêt de la Morera de Montsant (5) | la Morera de Montsant › Priorat | 49 |
| Forêt de Horta de Sant Joan (33) | Horta de Sant Joan › Terra Alta | 49 |
| Forêt de Alcover (22) | Alcover › Alt Camp | 49 |
| Forêt de Calafell (53) | Calafell › Baix Penedès | 49 |
| Forêt de Miravet | Miravet › Ribera d'Ebre | 48 |
| Forêt de la Riera de Gaià | la Riera de Gaià › Tarragonès | 48 |
| Forêt de els Pallaresos | els Pallaresos › Tarragonès | 48 |
| Forêt de l'Albiol (7) | l'Albiol › Baix Camp | 48 |
| Forêt de el Vendrell (33) | el Vendrell › Baix Penedès | 48 |
| Forêt de Tortosa | Tortosa › Baix Ebre | 47 |
| Forêt de Sarral (3) | Sarral › Conca de Barberà | 47 |
| Forêt de la Morera de Montsant (2) | la Morera de Montsant › Priorat | 47 |
| Forêt de Ascó (5) | Ascó › Ribera d'Ebre | 47 |
| Forêt de Benifallet (9) | Benifallet › Baix Ebre | 47 |
| Forêt de Vila-rodona (3) | Vila-rodona › Alt Camp | 47 |
| Forêt de Tivissa (21) | Tivissa › Ribera d'Ebre | 47 |
| Bois de Conesa | Conesa › Conca de Barberà | 47 |
| Forêt de Albinyana (21) | Albinyana › Baix Penedès | 47 |
| Forêt de Pratdip (44) | Pratdip › Baix Camp | 47 |
| Forêt de la Sénia (49) | la Sénia › Montsià | 47 |
| Forêt de la Torre de Fontaubella (6) | la Torre de Fontaubella › Priorat | 47 |
| Forêt de Vimbodí i Poblet (5) | Vimbodí i Poblet › Conca de Barberà | 46 |
| Forêt de Montblanc (3) | Montblanc › Conca de Barberà | 46 |
| Forêt de la Bisbal de Montsant (5) | la Bisbal de Montsant › Priorat | 46 |
| Forêt de Montblanc (6) | Montblanc › Conca de Barberà | 46 |
| Forêt de Rasquera (6) | Rasquera › Ribera d'Ebre | 46 |
| Forêt de Tarragona (45) | Tarragona › Tarragonès | 46 |
| Forêt de Flix (2) | Flix › Ribera d'Ebre | 45 |
| Forêt de Cabacés | Cabacés › Priorat | 45 |
| Forêt de Riudecols (3) | Riudecols › Baix Camp | 45 |
| Forêt de Rocafort de Queralt | Rocafort de Queralt › Conca de Barberà | 45 |
| Forêt de Cornudella de Montsant (153) | Cornudella de Montsant › Priorat | 45 |
| Forêt de Cabra del Camp | Cabra del Camp › Alt Camp | 44 |
| Forêt de Prades (5) | Prades › Baix Camp | 44 |
| Forêt de la Fatarella (10) | la Fatarella › Terra Alta | 44 |
| Forêt de Capçanes (5) | Capçanes › Priorat | 44 |
| Forêt de Querol (55) | Querol › Alt Camp | 44 |
| Forêt de Vimbodí i Poblet | Vimbodí i Poblet › Conca de Barberà | 43 |
| Forêt de Falset (3) | Falset › Priorat | 43 |
| Forêt de Pontils (5) | Pontils › Conca de Barberà | 43 |
| Forêt de Margalef (14) | Margalef › Priorat | 43 |
| Forêt de Colldejou (5) | Colldejou › Baix Camp | 43 |
| Forêt de Horta de Sant Joan (39) | Horta de Sant Joan › Terra Alta | 43 |
| Forêt de Xerta | Xerta › Baix Ebre | 42 |
| Forêt de l'Albiol (3) | l'Albiol › Baix Camp | 42 |
| Forêt de Capçanes | Capçanes › Priorat | 42 |
| Forêt de Aiguamúrcia (5) | Aiguamúrcia › Alt Camp | 42 |
| Forêt de Horta de Sant Joan (19) | Horta de Sant Joan › Terra Alta | 42 |
| Forêt de el Perelló (13) | el Perelló › Baix Ebre | 42 |
| Forêt de la Sénia (55) | la Sénia › Montsià | 42 |
| Forêt de Bellvei (12) | Bellvei › Baix Penedès | 42 |
| Forêt de Batea (19) | Batea › Terra Alta | 41 |
| Forêt de Aiguamúrcia (9) | Aiguamúrcia › Alt Camp | 41 |
| Forêt de Bot (3) | Bot › Terra Alta | 41 |
| Forêt de Aiguamúrcia (14) | Aiguamúrcia › Alt Camp | 41 |
| Forêt de Querol (53) | Querol › Alt Camp | 41 |
| Forêt de Horta de Sant Joan (3) | Horta de Sant Joan › Terra Alta | 40 |
| Forêt de Vilaplana (3) | Vilaplana › Baix Camp | 40 |
| Forêt de Miravet (2) | Miravet › Ribera d'Ebre | 40 |
| Bois de Passanant i Belltall (17) | Passanant i Belltall › Conca de Barberà | 40 |
| Bois de Tarragona (2) | Tarragona › Tarragonès | 40 |
| Forêt de Capçanes (7) | Capçanes › Priorat | 40 |
| Forêt de Alcanar (2) | Alcanar › Montsià | 40 |
| Forêt de Roquetes (18) | Roquetes › Baix Ebre | 40 |
| Forêt de Altafulla (6) | Altafulla › Tarragonès | 40 |
| Forêt de Alcover (21) | Alcover › Alt Camp | 40 |
| Forêt de Vinebre (2) | Vinebre › Ribera d'Ebre | 39 |
| Forêt de Falset (5) | Falset › Priorat | 39 |
| Forêt de la Bisbal del Penedès | la Bisbal del Penedès › Baix Penedès | 39 |
| Forêt de Vallfogona de Riucorb | Vallfogona de Riucorb › Conca de Barberà | 39 |
| Forêt de Vespella de Gaià (4) | Vespella de Gaià › Tarragonès | 39 |
| Forêt de Caseres (8) | Caseres › Terra Alta | 38 |
| Forêt de el Perelló (5) | el Perelló › Baix Ebre | 38 |
| Bois de Blancafort | Blancafort › Conca de Barberà | 38 |
| Forêt de Horta de Sant Joan (29) | Horta de Sant Joan › Terra Alta | 38 |
| Forêt de Tivissa (25) | Tivissa › Ribera d'Ebre | 38 |
| Forêt de la Sénia (19) | la Sénia › Montsià | 38 |
| Forêt de Alcover (20) | Alcover › Alt Camp | 38 |
| Forêt de Renau (2) | Renau › Tarragonès | 38 |
| Forêt de Vespella de Gaià (2) | Vespella de Gaià › Tarragonès | 38 |
| Forêt de Aiguamúrcia (3) | Aiguamúrcia › Alt Camp | 37 |
| Forêt de Garcia (3) | Garcia › Ribera d'Ebre | 37 |
| Forêt de Colldejou (2) | Colldejou › Baix Camp | 37 |
| Forêt de Tivissa (18) | Tivissa › Ribera d'Ebre | 37 |
| Forêt de l'Espluga de Francolí (7) | l'Espluga de Francolí › Conca de Barberà | 37 |
| Forêt de Cabra del Camp (5) | Cabra del Camp › Alt Camp | 37 |
| Forêt de Batea (28) | Batea › Terra Alta | 37 |
| Forêt de el Vendrell (43) | el Vendrell › Baix Penedès | 37 |
| Bois de Alcover (18) | Alcover › Alt Camp | 37 |
| Forêt de Capafonts (54) | Capafonts › Baix Camp | 37 |
| Forêt de Santa Coloma de Queralt (3) | Santa Coloma de Queralt › Conca de Barberà | 36 |
| Forêt de Roquetes | Roquetes › Baix Ebre | 36 |
| Forêt de Llorac (5) | Llorac › Conca de Barberà | 36 |
| Forêt de Aiguamúrcia (10) | Aiguamúrcia › Alt Camp | 36 |
| Forêt de Colldejou (4) | Colldejou › Baix Camp | 36 |
| Forêt de Benifallet (11) | Benifallet › Baix Ebre | 36 |
| Forêt de els Guiamets (2) | els Guiamets › Priorat | 36 |
| Bois de Tarragona (7) | Tarragona › Tarragonès | 36 |
| Forêt de Tortosa (41) | Tortosa › Baix Ebre | 36 |
| Forêt de Alcover (18) | Alcover › Alt Camp | 36 |
| Forêt de el Catllar (5) | el Catllar › Tarragonès | 36 |
| Forêt de Tivissa (4) | Tivissa › Ribera d'Ebre | 35 |
| Forêt de Margalef (4) | Margalef › Priorat | 35 |
| Forêt de Horta de Sant Joan (12) | Horta de Sant Joan › Terra Alta | 35 |
| Forêt de Pradell de la Teixeta | Pradell de la Teixeta › Priorat | 35 |
| Forêt de Tivissa (19) | Tivissa › Ribera d'Ebre | 35 |
| Forêt de la Figuera (6) | la Figuera › Priorat | 35 |
| Forêt de Mont-ral (3) | Mont-ral › Alt Camp | 35 |
| Forêt de la Sénia (20) | la Sénia › Montsià | 35 |
| Forêt de Figuerola del Camp (4) | Figuerola del Camp › Alt Camp | 35 |
| Forêt de Querol (25) | Querol › Alt Camp | 35 |
| Forêt de Tortosa (39) | Tortosa › Baix Ebre | 35 |
| Forêt de la Palma d'Ebre (3) | la Palma d'Ebre › Ribera d'Ebre | 34 |
| Forêt de Savallà del Comtat | Savallà del Comtat › Conca de Barberà | 33 |
| Forêt de Pontils (4) | Pontils › Conca de Barberà | 33 |
| Forêt de Móra d'Ebre (3) | Móra d'Ebre › Ribera d'Ebre | 33 |
| Forêt de Prades (6) | Prades › Baix Camp | 33 |
| Forêt de Vespella de Gaià | Vespella de Gaià › Tarragonès | 33 |
| Forêt de Capafonts | Capafonts › Baix Camp | 33 |
| Forêt de Riudecols (5) | Riudecols › Baix Camp | 33 |
| Forêt de Llorac (14) | Llorac › Conca de Barberà | 33 |
| Forêt de l'Arboç (23) | l'Arboç › Baix Penedès | 33 |
| Forêt de Querol (35) | Querol › Alt Camp | 33 |
| Forêt de la Riba (2) | la Riba › Alt Camp | 33 |
| Forêt de el Catllar (6) | el Catllar › Tarragonès | 33 |
| Forêt de Falset | Falset › Priorat | 32 |
| Forêt de el Perelló (2) | el Perelló › Baix Ebre | 32 |
| Forêt de Margalef | Margalef › Priorat | 32 |
| Forêt de Cornudella de Montsant | Cornudella de Montsant › Priorat | 32 |
| Forêt de Vilanova de Prades (3) | Vilanova de Prades › Conca de Barberà | 32 |
| Forêt de Tivenys | Tivenys › Baix Ebre | 32 |
| Forêt de la Sénia (12) | la Sénia › Montsià | 32 |
| Forêt de Savallà del Comtat (4) | Savallà del Comtat › Conca de Barberà | 32 |
| Forêt de Arnes (10) | Arnes › Terra Alta | 32 |
| Forêt de Montblanc (5) | Montblanc › Conca de Barberà | 32 |
| Forêt de Miravet (3) | Miravet › Ribera d'Ebre | 32 |
| Forêt de Alforja (5) | Alforja › Baix Camp | 32 |
| Forêt de Tarragona (4) | Tarragona › Tarragonès | 32 |
| Forêt de Alcover (16) | Alcover › Alt Camp | 32 |
| Forêt de Vallclara | Vallclara › Conca de Barberà | 31 |
| Forêt de Barberà de la Conca | Barberà de la Conca › Conca de Barberà | 31 |
| Forêt de Conesa (4) | Conesa › Conca de Barberà | 31 |
| Forêt de Alfara de Carles (11) | Alfara de Carles › Baix Ebre | 31 |
| Forêt de Llorac (8) | Llorac › Conca de Barberà | 31 |
| Forêt de Tarragona (3) | Tarragona › Tarragonès | 31 |
| Forêt de Mont-roig del Camp (8) | Mont-roig del Camp › Baix Camp | 31 |
| Forêt de la Secuita (2) | la Secuita › Tarragonès | 31 |
| Forêt de Querol (27) | Querol › Alt Camp | 31 |
| Forêt de la Morera de Montsant (93) | la Morera de Montsant › Priorat | 31 |
| Forêt de la Sénia (48) | la Sénia › Montsià | 31 |
| Forêt de Vimbodí i Poblet (2) | Vimbodí i Poblet › Conca de Barberà | 30 |
| Forêt de Benifallet (7) | Benifallet › Baix Ebre | 30 |
| Forêt de Cabacés (5) | Cabacés › Priorat | 30 |
| Forêt de Flix (23) | Flix › Ribera d'Ebre | 30 |
| Forêt de Santa Coloma de Queralt (7) | Santa Coloma de Queralt › Conca de Barberà | 30 |
| Forêt de Pradell de la Teixeta (4) | Pradell de la Teixeta › Priorat | 30 |
| Forêt de el Perelló (6) | el Perelló › Baix Ebre | 30 |
| Forêt de Ascó (7) | Ascó › Ribera d'Ebre | 30 |
| Forêt de Conesa (6) | Conesa › Conca de Barberà | 30 |
| Forêt de Alforja (6) | Alforja › Baix Camp | 30 |
| Forêt de Roquetes (10) | Roquetes › Baix Ebre | 30 |
| Forêt de Móra d'Ebre | Móra d'Ebre › Ribera d'Ebre | 29 |
| Forêt de el Pont d'Armentera | el Pont d'Armentera › Alt Camp | 29 |
| Forêt de Blancafort (3) | Blancafort › Conca de Barberà | 29 |
| Forêt de Alfara de Carles (16) | Alfara de Carles › Baix Ebre | 29 |
| Forêt de l'Ametlla de Mar (90) | l'Ametlla de Mar › Baix Ebre | 29 |
| Forêt de Pratdip (10) | Pratdip › Baix Camp | 29 |
| Forêt de Rodonyà (2) | Rodonyà › Alt Camp | 29 |
| Forêt de la Sénia (18) | la Sénia › Montsià | 29 |
| Forêt de Albinyana (19) | Albinyana › Baix Penedès | 29 |
| Forêt de Calafell (41) | Calafell › Baix Penedès | 29 |
| Forêt de la Morera de Montsant (88) | la Morera de Montsant › Priorat | 29 |
| Forêt de Vila-rodona (2) | Vila-rodona › Alt Camp | 28 |
| Forêt de Querol | Querol › Alt Camp | 28 |
| Forêt de Caseres (5) | Caseres › Terra Alta | 28 |
| Forêt de Horta de Sant Joan (9) | Horta de Sant Joan › Terra Alta | 28 |
| Forêt de Benifallet (5) | Benifallet › Baix Ebre | 28 |
| Forêt de l'Ametlla de Mar (190) | l'Ametlla de Mar › Baix Ebre | 28 |
| Forêt de la Sénia (36) | la Sénia › Montsià | 28 |
| Forêt de Mont-roig del Camp (113) | Mont-roig del Camp › Baix Camp | 28 |
| Forêt de Alcanar (16) | Alcanar › Montsià | 28 |
| Forêt de Riba-roja d'Ebre (18) | Riba-roja d'Ebre › Ribera d'Ebre | 28 |
| Forêt de la Palma d'Ebre | la Palma d'Ebre › Ribera d'Ebre | 27 |
| Forêt de Caseres (7) | Caseres › Terra Alta | 27 |
| Forêt de la Figuera (3) | la Figuera › Priorat | 27 |
| Forêt de Cornudella de Montsant (2) | Cornudella de Montsant › Priorat | 27 |
| Forêt de Horta de Sant Joan (20) | Horta de Sant Joan › Terra Alta | 27 |
| Forêt de Caseres (13) | Caseres › Terra Alta | 27 |
| Forêt de Riudecols (4) | Riudecols › Baix Camp | 27 |
| Bois de Horta de Sant Joan (11) | Horta de Sant Joan › Terra Alta | 27 |
| Forêt de Bonastre (16) | Bonastre › Baix Penedès | 27 |
| Forêt de la Riba (3) | la Riba › Alt Camp | 27 |
| Forêt de Mont-ral (24) | Mont-ral › Alt Camp | 27 |
| Forêt de Tortosa (2) | Tortosa › Baix Ebre | 26 |
| Forêt de Vinebre | Vinebre › Ribera d'Ebre | 26 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (2) | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 26 |
| Forêt de Caseres (10) | Caseres › Terra Alta | 26 |
| Forêt de Horta de Sant Joan (18) | Horta de Sant Joan › Terra Alta | 26 |
| Forêt de Rasquera (3) | Rasquera › Ribera d'Ebre | 26 |
| Forêt de Alfara de Carles (10) | Alfara de Carles › Baix Ebre | 26 |
| Forêt de la Fatarella (9) | la Fatarella › Terra Alta | 26 |
| Forêt de Horta de Sant Joan (34) | Horta de Sant Joan › Terra Alta | 26 |
| Forêt de Querol (51) | Querol › Alt Camp | 26 |
| Forêt de l'Aleixar | l'Aleixar › Baix Camp | 25 |
| Forêt de la Fatarella (4) | la Fatarella › Terra Alta | 25 |
| Forêt de Batea (12) | Batea › Terra Alta | 25 |
| Forêt de Tivissa (13) | Tivissa › Ribera d'Ebre | 25 |
| Forêt de Riba-roja d'Ebre (12) | Riba-roja d'Ebre › Ribera d'Ebre | 25 |
| Forêt de Arnes (9) | Arnes › Terra Alta | 25 |
| Forêt de la Bisbal de Montsant (4) | la Bisbal de Montsant › Priorat | 25 |
| Forêt de Margalef (11) | Margalef › Priorat | 25 |
| Bois de Passanant i Belltall (54) | Passanant i Belltall › Conca de Barberà | 25 |
| Forêt de Calafell (39) | Calafell › Baix Penedès | 25 |
| Forêt de Móra la Nova | Móra la Nova › Ribera d'Ebre | 25 |
| Forêt de la Sénia (44) | la Sénia › Montsià | 25 |
| Forêt de Arnes (22) | Arnes › Terra Alta | 25 |
| Forêt de la Sénia (47) | la Sénia › Montsià | 25 |
| Forêt de Pontils | Pontils › Conca de Barberà | 24 |
| Forêt de la Figuera (2) | la Figuera › Priorat | 24 |
| Forêt de el Pinell de Brai (3) | el Pinell de Brai › Terra Alta | 24 |
| Forêt de els Guiamets | els Guiamets › Priorat | 24 |
| Forêt de l'Espluga de Francolí (6) | l'Espluga de Francolí › Conca de Barberà | 24 |
| Forêt de Caseres (11) | Caseres › Terra Alta | 24 |
| Forêt de Batea (26) | Batea › Terra Alta | 24 |
| Forêt de Conesa (5) | Conesa › Conca de Barberà | 24 |
| Forêt de Bot (4) | Bot › Terra Alta | 24 |
| Bois de el Catllar (20) | el Catllar › Tarragonès | 24 |
| Forêt de Vila-rodona (5) | Vila-rodona › Alt Camp | 24 |
| Forêt de Querol (24) | Querol › Alt Camp | 24 |
| Forêt de Querol (48) | Querol › Alt Camp | 24 |
| Forêt de Blancafort | Blancafort › Conca de Barberà | 23 |
| Forêt de l'Albiol | l'Albiol › Baix Camp | 23 |
| Forêt de Vilaplana | Vilaplana › Baix Camp | 23 |
| Forêt de Amposta | Amposta › Montsià | 23 |
| Forêt de Tivissa (8) | Tivissa › Ribera d'Ebre | 23 |
| Forêt de Cabra del Camp (3) | Cabra del Camp › Alt Camp | 23 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (6) | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 23 |
| Forêt de Aldover (2) | Aldover › Baix Ebre | 23 |
| Forêt de el Pinell de Brai (5) | el Pinell de Brai › Terra Alta | 23 |
| Forêt de Bot (5) | Bot › Terra Alta | 23 |
| Forêt de Montferri | Montferri › Alt Camp | 23 |
| Forêt de Capçanes (12) | Capçanes › Priorat | 23 |
| Bois de Pontils (3) | Pontils › Conca de Barberà | 23 |
| Forêt de el Catllar (3) | el Catllar › Tarragonès | 23 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (42) | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 23 |
| Bosc de la Marquesa | Tarragona › Tarragonès | 23 |
| Forêt de Vimbodí i Poblet (4) | Vimbodí i Poblet › Conca de Barberà | 22 |
| Forêt de Blancafort (2) | Blancafort › Conca de Barberà | 22 |
| Forêt de Flix (5) | Flix › Ribera d'Ebre | 22 |
| Forêt de Sarral (2) | Sarral › Conca de Barberà | 22 |
| Forêt de Alfara de Carles (6) | Alfara de Carles › Baix Ebre | 22 |
| Forêt de Margalef (3) | Margalef › Priorat | 22 |
| Forêt de l'Espluga de Francolí (4) | l'Espluga de Francolí › Conca de Barberà | 22 |
| Forêt de Paüls (4) | Paüls › Baix Ebre | 22 |
| Forêt de Bot (6) | Bot › Terra Alta | 22 |
| Forêt de l'Ametlla de Mar (137) | l'Ametlla de Mar › Baix Ebre | 22 |
| Forêt de Cornudella de Montsant (147) | Cornudella de Montsant › Priorat | 22 |
| Forêt de Riudecanyes (8) | Riudecanyes › Baix Camp | 22 |
| Forêt de la Bisbal del Penedès (23) | la Bisbal del Penedès › Baix Penedès | 22 |
| Forêt de Albinyana (20) | Albinyana › Baix Penedès | 22 |
| Forêt de la Sénia (53) | la Sénia › Montsià | 22 |
| Forêt de Calafell (55) | Calafell › Baix Penedès | 22 |
| Forêt de Tivissa | Tivissa › Ribera d'Ebre | 21 |
| Forêt de Tortosa (3) | Tortosa › Baix Ebre | 21 |
| Forêt de Pontils (2) | Pontils › Conca de Barberà | 21 |
| Forêt de l'Espluga de Francolí | l'Espluga de Francolí › Conca de Barberà | 21 |
| Forêt de Santa Coloma de Queralt (2) | Santa Coloma de Queralt › Conca de Barberà | 21 |
| Forêt de Savallà del Comtat (3) | Savallà del Comtat › Conca de Barberà | 21 |
| Forêt de Pratdip (2) | Pratdip › Baix Camp | 21 |
| Forêt de Vilalba dels Arcs (6) | Vilalba dels Arcs › Terra Alta | 21 |
| Forêt de Mont-ral (2) | Mont-ral › Alt Camp | 21 |
| Forêt de Batea (25) | Batea › Terra Alta | 21 |
| Bois de Tarragona (4) | Tarragona › Tarragonès | 21 |
| Forêt de Mont-ral (22) | Mont-ral › Alt Camp | 21 |
| Forêt de Bonastre (18) | Bonastre › Baix Penedès | 21 |
| Forêt de Colldejou (29) | Colldejou › Baix Camp | 21 |
| Forêt de Arnes | Arnes › Terra Alta | 20 |
| Forêt de Garcia | Garcia › Ribera d'Ebre | 20 |
| Forêt de Corbera d'Ebre (3) | Corbera d'Ebre › Terra Alta | 20 |
| Forêt de Vilanova de Prades (2) | Vilanova de Prades › Conca de Barberà | 20 |
| Forêt de Tivissa (10) | Tivissa › Ribera d'Ebre | 20 |
| Forêt de Horta de Sant Joan (10) | Horta de Sant Joan › Terra Alta | 20 |
| Forêt de Vimbodí i Poblet (10) | Vimbodí i Poblet › Conca de Barberà | 20 |
| Forêt de la Morera de Montsant (3) | la Morera de Montsant › Priorat | 20 |
| Forêt de Corbera d'Ebre (4) | Corbera d'Ebre › Terra Alta | 20 |
| Forêt de Colldejou (3) | Colldejou › Baix Camp | 20 |
| Forêt de Vinebre (4) | Vinebre › Ribera d'Ebre | 20 |
| Forêt de Flix (29) | Flix › Ribera d'Ebre | 20 |
| Forêt de l'Espluga de Francolí (9) | l'Espluga de Francolí › Conca de Barberà | 20 |
| Forêt de l'Ametlla de Mar (135) | l'Ametlla de Mar › Baix Ebre | 20 |
| Bois de l'Aleixar | l'Aleixar › Baix Camp | 20 |
| Forêt de Mont-roig del Camp (72) | Mont-roig del Camp › Baix Camp | 20 |
| Bois de l'Espluga de Francolí (2) | l'Espluga de Francolí › Conca de Barberà | 20 |
| Forêt de Montblanc (18) | Montblanc › Conca de Barberà | 20 |
| Forêt de Querol (36) | Pontils › Conca de Barberà | 20 |
| Forêt de Alcover (19) | Alcover › Alt Camp | 20 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 19 |
| Bosc del Ferrer Ric | la Secuita › Tarragonès | 19 |
| Forêt de Falset (2) | Falset › Priorat | 19 |
| Forêt de el Pinell de Brai (4) | el Pinell de Brai › Terra Alta | 19 |
| Forêt de la Sénia (10) | la Sénia › Montsià | 19 |
| Forêt de Batea (20) | Batea › Terra Alta | 19 |
| Forêt de Aiguamúrcia (8) | Aiguamúrcia › Alt Camp | 19 |
| Forêt de Rasquera (4) | Rasquera › Ribera d'Ebre | 19 |
| Forêt de la Fatarella (7) | Ascó › Ribera d'Ebre | 19 |
| Forêt de Cornudella de Montsant (3) | Cornudella de Montsant › Priorat | 19 |
| Forêt de Caseres (12) | Caseres › Terra Alta | 19 |
| Forêt de Arbolí (4) | Arbolí › Baix Camp | 19 |
| Forêt de Tortosa (10) | Tortosa › Baix Ebre | 19 |
| Forêt de Pratdip (16) | Pratdip › Baix Camp | 19 |
| Forêt de Bonastre (17) | Bonastre › Baix Penedès | 19 |
| Forêt de Querol (26) | Querol › Alt Camp | 19 |
| Forêt de Batea | Batea › Terra Alta | 18 |
| Forêt de la Pobla de Massaluca | la Pobla de Massaluca › Terra Alta | 18 |
| Forêt de Rasquera (2) | Rasquera › Ribera d'Ebre | 18 |
| Forêt de Móra d'Ebre (2) | Móra d'Ebre › Ribera d'Ebre | 18 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (4) | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 18 |
| Forêt de Barberà de la Conca (2) | Barberà de la Conca › Conca de Barberà | 18 |
| Forêt de Pradell de la Teixeta (3) | Pradell de la Teixeta › Priorat | 18 |
| Forêt de Riudecanyes (2) | Riudecanyes › Baix Camp | 18 |
| Forêt de Sarral (5) | Sarral › Conca de Barberà | 18 |
| Forêt de Tarragona (12) | Tarragona › Tarragonès | 18 |
| Forêt de la Morera de Montsant (24) | la Morera de Montsant › Priorat | 18 |
| Forêt de Cabacés (8) | Cabacés › Priorat | 18 |
| Forêt de Roda de Berà (6) | Roda de Berà › Tarragonès | 18 |
| Forêt de Calafell (38) | Calafell › Baix Penedès | 18 |
| Forêt de el Pla de Santa Maria (34) | el Pla de Santa Maria › Alt Camp | 18 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (49) | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 18 |
| Forêt de Colldejou (28) | Colldejou › Baix Camp | 18 |
| Forêt de Vila-rodona | Vila-rodona › Alt Camp | 17 |
| Forêt de Ascó | Ascó › Ribera d'Ebre | 17 |
| Forêt de Tivissa (2) | Tivissa › Ribera d'Ebre | 17 |
| Forêt de Corbera d'Ebre | Corbera d'Ebre › Terra Alta | 17 |
| Forêt de Batea (5) | Batea › Terra Alta | 17 |
| Forêt de el Masroig | el Masroig › Priorat | 17 |
| Forêt de la Sénia (8) | la Sénia › Montsià | 17 |
| Forêt de Prades (4) | Prades › Baix Camp | 17 |
| Forêt de Tivissa (16) | Tivissa › Ribera d'Ebre | 17 |
| Forêt de Vimbodí i Poblet (16) | Vimbodí i Poblet › Conca de Barberà | 17 |
| Forêt de Tortosa (7) | Tortosa › Baix Ebre | 17 |
| Forêt de Vilalba dels Arcs (11) | Vilalba dels Arcs › Terra Alta | 17 |
| Forêt de Montblanc (7) | Montblanc › Conca de Barberà | 17 |
| Forêt de la Morera de Montsant (18) | la Morera de Montsant › Priorat | 17 |
| Forêt de Pratdip (5) | Pratdip › Baix Camp | 17 |
| Bois de Torroja del Priorat (4) | Torroja del Priorat › Priorat | 17 |
| Forêt de Cornudella de Montsant (55) | Cornudella de Montsant › Priorat | 17 |
| Forêt de Ulldecona (8) | Ulldecona › Montsià | 17 |
| Forêt de Alcover (13) | Alcover › Alt Camp | 17 |
| Forêt de Prades (57) | Prades › Baix Camp | 17 |
| Forêt de el Pont d'Armentera (3) | el Pont d'Armentera › Alt Camp | 17 |
| Forêt de Riudecols (2) | Riudecols › Baix Camp | 16 |
| Forêt de Querol (2) | Querol › Alt Camp | 16 |
| Forêt de la Bisbal de Montsant | la Bisbal de Montsant › Priorat | 16 |
| Forêt de Ascó (3) | Ascó › Ribera d'Ebre | 16 |
| Forêt de Paüls (3) | Paüls › Baix Ebre | 16 |
| Forêt de Benissanet | Benissanet › Ribera d'Ebre | 16 |
| Forêt de Aiguamúrcia (7) | Aiguamúrcia › Alt Camp | 16 |
| Forêt de Benissanet (2) | Miravet › Ribera d'Ebre | 16 |
| Forêt de Horta de Sant Joan (26) | Horta de Sant Joan › Terra Alta | 16 |
| Forêt de Pontils (11) | Pontils › Conca de Barberà | 16 |
| la Miloquera | Marçà › Priorat | 16 |
| Parc Torre d'en Dolça | Vila-seca › Tarragonès | 16 |
| Forêt de Cornudella de Montsant (9) | Cornudella de Montsant › Priorat | 16 |
| Forêt de l'Ametlla de Mar (128) | l'Ametlla de Mar › Baix Ebre | 16 |
| Forêt de Mont-roig del Camp (55) | Mont-roig del Camp › Baix Camp | 16 |
| Forêt de Ulldemolins (81) | Ulldemolins › Priorat | 16 |
| Bois de el Pla de Santa Maria (10) | el Pla de Santa Maria › Alt Camp | 16 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (34) | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 16 |
| Forêt de la Morera de Montsant (103) | la Morera de Montsant › Priorat | 16 |
| Forêt de Colldejou (31) | Colldejou › Baix Camp | 16 |
| Forêt de l'Aldea | l'Aldea › Baix Ebre | 15 |
| Forêt de Alfara de Carles (3) | Alfara de Carles › Baix Ebre | 15 |
| Forêt de Prades (3) | Prades › Baix Camp | 15 |
| Forêt de l'Albiol (4) | l'Albiol › Baix Camp | 15 |
| Forêt de Batea (6) | Batea › Terra Alta | 15 |
| Forêt de la Bisbal de Montsant (2) | la Bisbal de Montsant › Priorat | 15 |
| Forêt de Margalef (5) | Margalef › Priorat | 15 |
| Forêt de Margalef (12) | Margalef › Priorat | 15 |
| Forêt de la Sénia (14) | la Sénia › Montsià | 15 |
| Forêt de Alforja (4) | Alforja › Baix Camp | 15 |
| Forêt de Alfara de Carles (15) | Alfara de Carles › Baix Ebre | 15 |
| Forêt de Calafell (2) | Calafell › Baix Penedès | 15 |
| Forêt de Vilanova d'Escornalbou (11) | Vilanova d'Escornalbou › Baix Camp | 15 |
| Forêt de Mont-roig del Camp (73) | Mont-roig del Camp › Baix Camp | 15 |
| Bois de Horta de Sant Joan (14) | Horta de Sant Joan › Terra Alta | 15 |
| Forêt de Torredembarra (7) | Torredembarra › Tarragonès | 15 |
| Forêt de Querol (33) | Querol › Alt Camp | 15 |
| Forêt de Alcover (15) | Alcover › Alt Camp | 15 |
| Forêt de Vilabella (2) | Vilabella › Alt Camp | 15 |
| Bois de Alcover (19) | Alcover › Alt Camp | 15 |
| Forêt de Aiguamúrcia (30) | Aiguamúrcia › Alt Camp | 15 |
| Forêt de Cornudella de Montsant (155) | Cornudella de Montsant › Priorat | 15 |
| Bois de Senan | Senan › Conca de Barberà | 14 |
| Forêt de l'Argentera | l'Argentera › Baix Camp | 14 |
| Forêt de Caseres (3) | Caseres › Terra Alta | 14 |
| Forêt de Tortosa (4) | Tortosa › Baix Ebre | 14 |
| Forêt de Montblanc (2) | Montblanc › Conca de Barberà | 14 |
| Forêt de Riba-roja d'Ebre (3) | Riba-roja d'Ebre › Ribera d'Ebre | 14 |
| Forêt de l'Espluga de Francolí (3) | l'Espluga de Francolí › Conca de Barberà | 14 |
| Forêt de l'Espluga de Francolí (5) | l'Espluga de Francolí › Conca de Barberà | 14 |
| Forêt de Colldejou | Colldejou › Baix Camp | 14 |
| Forêt de Pontils (7) | Pontils › Conca de Barberà | 14 |
| Bosc de Salt de Roca | Renau › Tarragonès | 14 |
| Forêt de el Pinell de Brai (6) | el Pinell de Brai › Terra Alta | 14 |
| Forêt de Mont-ral (4) | Mont-ral › Alt Camp | 14 |
| Forêt de Cunit (2) | Cunit › Baix Penedès | 14 |
| Forêt de Ulldecona (5) | Ulldecona › Montsià | 14 |
| Forêt de l'Ametlla de Mar (46) | l'Ametlla de Mar › Baix Ebre | 14 |
| Forêt de Mont-roig del Camp (70) | Mont-roig del Camp › Baix Camp | 14 |
| Forêt de Mont-roig del Camp (87) | Mont-roig del Camp › Baix Camp | 14 |
| Forêt de Pratdip (11) | Pratdip › Baix Camp | 14 |
| Forêt de Mont-ral (11) | Mont-ral › Alt Camp | 14 |
| Forêt de Roda de Berà (21) | Roda de Berà › Tarragonès | 14 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (30) | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 14 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (37) | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 14 |
| Forêt de Mont-roig del Camp (106) | Mont-roig del Camp › Baix Camp | 14 |
| Forêt de el Catllar (4) | el Catllar › Tarragonès | 14 |
| Forêt de Aiguamúrcia (32) | Aiguamúrcia › Alt Camp | 14 |
| Forêt de Caseres | Caseres › Terra Alta | 13 |
| Forêt de Horta de Sant Joan (5) | Horta de Sant Joan › Terra Alta | 13 |
| Forêt de Batea (3) | Batea › Terra Alta | 13 |
| Forêt de Aldover | Aldover › Baix Ebre | 13 |
| Forêt de Flix (9) | Flix › Ribera d'Ebre | 13 |
| Forêt de el Perelló (4) | el Perelló › Baix Ebre | 13 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (5) | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 13 |
| Forêt de Flix (11) | Flix › Ribera d'Ebre | 13 |
| Forêt de Vimbodí i Poblet (18) | Vimbodí i Poblet › Conca de Barberà | 13 |
| Forêt de Prades (7) | Prades › Baix Camp | 13 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (10) | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 13 |
| Forêt de Aiguamúrcia (13) | Aiguamúrcia › Alt Camp | 13 |
| Forêt de el Perelló (11) | el Perelló › Baix Ebre | 13 |
| Forêt de Tarragona | Tarragona › Tarragonès | 13 |
| Forêt de la Morera de Montsant (21) | la Morera de Montsant › Priorat | 13 |
| Forêt de l'Ametlla de Mar (127) | l'Ametlla de Mar › Baix Ebre | 13 |
| Bois de el Catllar (9) | el Catllar › Tarragonès | 13 |
| Bois de Valls (5) | Valls › Alt Camp | 13 |
| Bois de la Bisbal del Penedès (3) | la Bisbal del Penedès › Baix Penedès | 13 |
| Forêt de l'Ametlla de Mar (189) | l'Ametlla de Mar › Baix Ebre | 13 |
| Forêt de el Vendrell (49) | el Vendrell › Baix Penedès | 13 |
| Forêt de la Sénia (27) | la Sénia › Montsià | 13 |
| Forêt de Roquetes (14) | Roquetes › Baix Ebre | 13 |
| Forêt de el Perelló (29) | el Perelló › Baix Ebre | 13 |
| Forêt de Riba-roja d'Ebre (19) | Riba-roja d'Ebre › Ribera d'Ebre | 13 |
| Forêt de Flix (6) | Flix › Ribera d'Ebre | 12 |
| Forêt de Batea (9) | Batea › Terra Alta | 12 |
| Forêt de Cabra del Camp (2) | Cabra del Camp › Alt Camp | 12 |
| Bois de Passanant i Belltall | Passanant i Belltall › Conca de Barberà | 12 |
| Forêt de el Montmell (4) | el Montmell › Baix Penedès | 12 |
| Forêt de Pradell de la Teixeta (2) | Pradell de la Teixeta › Priorat | 12 |
| Forêt de Tortosa (8) | Tortosa › Baix Ebre | 12 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (8) | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 12 |
| Forêt de Riba-roja d'Ebre (14) | Riba-roja d'Ebre › Ribera d'Ebre | 12 |
| Forêt de Tortosa (9) | Tortosa › Baix Ebre | 12 |
| Forêt de Alfara de Carles (12) | Alfara de Carles › Baix Ebre | 12 |
| Forêt de Rasquera (5) | Rasquera › Ribera d'Ebre | 12 |
| Forêt de Gandesa (4) | Gandesa › Terra Alta | 12 |
| Forêt de Caseres (14) | Caseres › Terra Alta | 12 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (11) | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 12 |
| Forêt de Batea (29) | Batea › Terra Alta | 12 |
| Forêt de Mas de Barberans (3) | Mas de Barberans › Montsià | 12 |
| Bois de Flix (8) | Flix › Ribera d'Ebre | 12 |
| Forêt de Tarragona (11) | Tarragona › Tarragonès | 12 |
| El Pont de Ferro, Riera de Marmellar | l'Arboç › Baix Penedès | 12 |
| Forêt de el Vendrell (11) | el Vendrell › Baix Penedès | 12 |
| Forêt de l'Ametlla de Mar (150) | l'Ametlla de Mar › Baix Ebre | 12 |
| Forêt de Tivissa (27) | Tivissa › Ribera d'Ebre | 12 |
| Forêt de Vilanova d'Escornalbou (12) | Vilanova d'Escornalbou › Baix Camp | 12 |
| Forêt de Mont-roig del Camp (66) | Mont-roig del Camp › Baix Camp | 12 |
| Forêt de Cornudella de Montsant (75) | Cornudella de Montsant › Priorat | 12 |
| Forêt de la Bisbal del Penedès (22) | la Bisbal del Penedès › Baix Penedès | 12 |
| Forêt de Santa Coloma de Queralt (40) | Santa Coloma de Queralt › Conca de Barberà | 12 |
| Forêt de Prat de Comte (6) | Prat de Comte › Terra Alta | 12 |
| Forêt de Arnes (20) | Arnes › Terra Alta | 12 |
| Forêt de Querol (29) | Querol › Alt Camp | 12 |
| Forêt de la Sénia (29) | la Sénia › Montsià | 12 |
| Forêt de la Morera de Montsant (94) | la Morera de Montsant › Priorat | 12 |
| Forêt de la Sénia (46) | la Sénia › Montsià | 12 |
| Forêt de Querol (50) | Querol › Alt Camp | 12 |
| Forêt de la Figuera | la Figuera › Priorat | 11 |
| Forêt de Sarral | Sarral › Conca de Barberà | 11 |
| Forêt de el Pinell de Brai (2) | el Pinell de Brai › Terra Alta | 11 |
| Forêt de Garcia (2) | Garcia › Ribera d'Ebre | 11 |
| Forêt de la Morera de Montsant | Margalef › Priorat | 11 |
| Forêt de Cabacés (4) | Cabacés › Priorat | 11 |
| Forêt de Vilalba dels Arcs (5) | Vilalba dels Arcs › Terra Alta | 11 |
| Bois de Passanant i Belltall (4) | Passanant i Belltall › Conca de Barberà | 11 |
| Forêt de Flix (24) | Flix › Ribera d'Ebre | 11 |
| Forêt de Batea (22) | Batea › Terra Alta | 11 |
| Forêt de Margalef (13) | Margalef › Priorat | 11 |
| Forêt de Batea (30) | Batea › Terra Alta | 11 |
| Bois de els Pallaresos (6) | els Pallaresos › Tarragonès | 11 |
| Forêt de Móra d'Ebre (9) | Móra d'Ebre › Ribera d'Ebre | 11 |
| Forêt de Vilanova d'Escornalbou (22) | Mont-roig del Camp › Baix Camp | 11 |
| Forêt de Pratdip (37) | Pratdip › Baix Camp | 11 |
| Forêt de Colldejou (16) | Colldejou › Baix Camp | 11 |
| Forêt de la Selva del Camp (58) | la Selva del Camp › Baix Camp | 11 |
| Forêt de Querol (31) | Querol › Alt Camp | 11 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (38) | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 11 |
| Forêt de Mont-roig del Camp (112) | Mont-roig del Camp › Baix Camp | 11 |
| Forêt de Mont-roig del Camp (146) | Mont-roig del Camp › Baix Camp | 11 |
| Forêt de Pratdip | Pratdip › Baix Camp | 10 |
| Forêt de Corbera d'Ebre (2) | Corbera d'Ebre › Terra Alta | 10 |
| Forêt de Santa Coloma de Queralt (4) | Santa Coloma de Queralt › Conca de Barberà | 10 |
| Bois de Vallfogona de Riucorb (2) | Vallfogona de Riucorb › Conca de Barberà | 10 |
| Forêt de Montblanc (12) | Montblanc › Conca de Barberà | 10 |
| Forêt de la Bisbal del Penedès (8) | la Bisbal del Penedès › Baix Penedès | 10 |
| Bosc de la Futa | el Pla de Santa Maria › Alt Camp | 10 |
| Bois de el Catllar (5) | el Catllar › Tarragonès | 10 |
| Bois de el Catllar (17) | el Catllar › Tarragonès | 10 |
| Forêt de Falset (10) | Falset › Priorat | 10 |
| Forêt de Vilanova d'Escornalbou (10) | Vilanova d'Escornalbou › Baix Camp | 10 |
| Forêt de Vilanova d'Escornalbou (13) | Vilanova d'Escornalbou › Baix Camp | 10 |
| Forêt de Mont-roig del Camp (62) | Mont-roig del Camp › Baix Camp | 10 |
| Forêt de Pratdip (15) | Pratdip › Baix Camp | 10 |
| Forêt de Cornudella de Montsant (149) | Cornudella de Montsant › Priorat | 10 |
| Forêt de Cornudella de Montsant (150) | Cornudella de Montsant › Priorat | 10 |
| Forêt de Ulldecona (9) | Ulldecona › Montsià | 10 |
| Forêt de Roda de Berà (19) | Roda de Berà › Tarragonès | 10 |
| Forêt de Valls (13) | Valls › Alt Camp | 10 |
| Forêt de la Sénia (37) | la Sénia › Montsià | 10 |
| Forêt de la Morera de Montsant (89) | la Morera de Montsant › Priorat | 10 |
| Forêt de Roquetes (21) | Roquetes › Baix Ebre | 10 |
| Forêt de Paüls (9) | Paüls › Baix Ebre | 10 |
| Forêt de Ulldemolins ⚠️ | Ulldemolins › Priorat | 9 |
| Forêt de Horta de Sant Joan (7) ⚠️ | Horta de Sant Joan › Terra Alta | 9 |
| Forêt de Falset (4) ⚠️ | Falset › Priorat | 9 |
| Forêt de Santa Coloma de Queralt (9) ⚠️ | Santa Coloma de Queralt › Conca de Barberà | 9 |
| Forêt de el Perelló (7) ⚠️ | el Perelló › Baix Ebre | 9 |
| Bois de Horta de Sant Joan (8) ⚠️ | Horta de Sant Joan › Terra Alta | 9 |
| Forêt de Móra d'Ebre (10) ⚠️ | Móra d'Ebre › Ribera d'Ebre | 9 |
| Forêt de Pratdip (12) ⚠️ | Pratdip › Baix Camp | 9 |
| Forêt de Pratdip (42) ⚠️ | Pratdip › Baix Camp | 9 |
| Forêt de Banyeres del Penedès (25) ⚠️ | Banyeres del Penedès › Baix Penedès | 9 |
| Forêt de la Selva del Camp (29) ⚠️ | la Selva del Camp › Baix Camp | 9 |
| Bois de Horta de Sant Joan (12) ⚠️ | Horta de Sant Joan › Terra Alta | 9 |
| Forêt de la Bisbal del Penedès (24) ⚠️ | la Bisbal del Penedès › Baix Penedès | 9 |
| Forêt de Roda de Berà (15) ⚠️ | Roda de Berà › Tarragonès | 9 |
| Forêt de Calafell (43) ⚠️ | Calafell › Baix Penedès | 9 |
| Bois de l'Espluga de Francolí (4) ⚠️ | l'Espluga de Francolí › Conca de Barberà | 9 |
| Forêt de Mont-roig del Camp (116) ⚠️ | Mont-roig del Camp › Baix Camp | 9 |
| Forêt de Salou (34) ⚠️ | Salou › Tarragonès | 9 |
| Forêt de Alcanar (13) ⚠️ | Alcanar › Montsià | 9 |
| Forêt de la Riba (4) ⚠️ | la Riba › Alt Camp | 9 |
| Forêt de la Morera de Montsant (92) ⚠️ | la Morera de Montsant › Priorat | 9 |
| Forêt de Querol (43) ⚠️ | Querol › Alt Camp | 9 |
| Forêt de Querol (47) ⚠️ | Querol › Alt Camp | 9 |
| Forêt de Querol (49) ⚠️ | Querol › Alt Camp | 9 |
| Forêt de Pratdip (48) ⚠️ | Pratdip › Baix Camp | 9 |
| Forêt de Riba-roja d'Ebre (21) ⚠️ | Riba-roja d'Ebre › Ribera d'Ebre | 9 |
| Forêt de Prat de Comte (5) ⚠️ | Prat de Comte › Terra Alta | 8 |
| Forêt de Albinyana (5) ⚠️ | Albinyana › Baix Penedès | 8 |
| Forêt de el Vendrell (24) ⚠️ | el Vendrell › Baix Penedès | 8 |
| Forêt de Ulldecona (6) ⚠️ | Ulldecona › Montsià | 8 |
| Forêt de l'Ametlla de Mar (140) ⚠️ | l'Ametlla de Mar › Baix Ebre | 8 |
| Forêt de l'Ametlla de Mar (156) ⚠️ | l'Ametlla de Mar › Baix Ebre | 8 |
| Bois de Aiguamúrcia (2) ⚠️ | Aiguamúrcia › Alt Camp | 8 |
| Forêt de Mont-roig del Camp (43) ⚠️ | Mont-roig del Camp › Baix Camp | 8 |
| Forêt de Mont-roig del Camp (63) ⚠️ | Mont-roig del Camp › Baix Camp | 8 |
| Forêt de Mont-roig del Camp (71) ⚠️ | Mont-roig del Camp › Baix Camp | 8 |
| Forêt de Mont-roig del Camp (86) ⚠️ | Mont-roig del Camp › Baix Camp | 8 |
| Forêt de Prades (31) ⚠️ | Prades › Baix Camp | 8 |
| Forêt de Tarragona (48) ⚠️ | Tarragona › Tarragonès | 8 |
| Forêt de Aldover (4) ⚠️ | Aldover › Baix Ebre | 8 |
| Forêt de el Vendrell (36) ⚠️ | el Vendrell › Baix Penedès | 8 |
| Forêt de la Sénia (30) ⚠️ | la Sénia › Montsià | 8 |
| Forêt de Salou (26) ⚠️ | Salou › Tarragonès | 8 |
| Forêt de la Morera de Montsant (97) ⚠️ | la Morera de Montsant › Priorat | 8 |
| Forêt de Pratdip (45) ⚠️ | Pratdip › Baix Camp | 8 |
| Forêt de Vilabella (3) ⚠️ | Vilabella › Alt Camp | 8 |
| Forêt de Horta de Sant Joan (23) ⚠️ | Horta de Sant Joan › Terra Alta | 7 |
| Forêt de Batea (27) ⚠️ | Batea › Terra Alta | 7 |
| Forêt de Calafell ⚠️ | Calafell › Baix Penedès | 7 |
| Forêt de el Vendrell (20) ⚠️ | el Vendrell › Baix Penedès | 7 |
| Forêt de el Vendrell (21) ⚠️ | el Vendrell › Baix Penedès | 7 |
| Forêt de Poboleda (22) ⚠️ | Poboleda › Priorat | 7 |
| Forêt de Albinyana (9) ⚠️ | Albinyana › Baix Penedès | 7 |
| Forêt de Montblanc (9) ⚠️ | Montblanc › Conca de Barberà | 7 |
| Forêt de el Catllar (2) ⚠️ | el Catllar › Tarragonès | 7 |
| Illa del Galatxo ⚠️ | Móra d'Ebre › Ribera d'Ebre | 7 |
| Bosc del Frai ⚠️ | el Pla de Santa Maria › Alt Camp | 7 |
| Forêt de l'Ametlla de Mar (13) ⚠️ | l'Ametlla de Mar › Baix Ebre | 7 |
| Bois de el Catllar (21) ⚠️ | el Catllar › Tarragonès | 7 |
| Forêt de Mont-roig del Camp (19) ⚠️ | Mont-roig del Camp › Baix Camp | 7 |
| Bois de el Pla de Santa Maria ⚠️ | el Pla de Santa Maria › Alt Camp | 7 |
| Forêt de Benissanet (3) ⚠️ | Benissanet › Ribera d'Ebre | 7 |
| Fageda del Retaule ⚠️ | la Sénia › Montsià | 7 |
| Forêt de Santa Coloma de Queralt (28) ⚠️ | Santa Coloma de Queralt › Conca de Barberà | 7 |
| Forêt de l'Albiol (8) ⚠️ | l'Albiol › Baix Camp | 7 |
| Bois de Batea (10) ⚠️ | Batea › Terra Alta | 7 |
| Forêt de Salou (21) ⚠️ | Salou › Tarragonès | 7 |
| Forêt de Margalef (15) ⚠️ | Margalef › Priorat | 7 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (19) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 7 |
| Forêt de Creixell (7) ⚠️ | Creixell › Tarragonès | 7 |
| Forêt de la Sénia (26) ⚠️ | la Sénia › Montsià | 7 |
| Forêt de la Sénia (39) ⚠️ | la Sénia › Montsià | 7 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (33) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 7 |
| Forêt de Mont-roig del Camp (90) ⚠️ | Mont-roig del Camp › Baix Camp | 7 |
| Forêt de Salou (29) ⚠️ | Salou › Tarragonès | 7 |
| Forêt de Salou (33) ⚠️ | Salou › Tarragonès | 7 |
| Forêt de Tarragona (58) ⚠️ | Tarragona › Tarragonès | 7 |
| Forêt de l'Ametlla de Mar (208) ⚠️ | l'Ametlla de Mar › Baix Ebre | 7 |
| Forêt de l'Ametlla de Mar (229) ⚠️ | l'Ametlla de Mar › Baix Ebre | 7 |
| Forêt de Mont-roig del Camp (137) ⚠️ | Mont-roig del Camp › Baix Camp | 7 |
| Forêt de Vespella de Gaià (3) ⚠️ | Vespella de Gaià › Tarragonès | 7 |
| Parc Samà ⚠️ | Cambrils › Baix Camp | 6 |
| Forêt de la Bisbal de Montsant (6) ⚠️ | la Bisbal de Montsant › Priorat | 6 |
| Forêt de el Perelló (8) ⚠️ | el Perelló › Baix Ebre | 6 |
| Parc de la Muntanyeta ⚠️ | Tarragona › Tarragonès | 6 |
| Forêt de Albinyana ⚠️ | Albinyana › Baix Penedès | 6 |
| Forêt de l'Arboç (18) ⚠️ | l'Arboç › Baix Penedès | 6 |
| Forêt de Rodonyà ⚠️ | Rodonyà › Alt Camp | 6 |
| Bosc del Borràs ⚠️ | el Pla de Santa Maria › Alt Camp | 6 |
| Forêt de el Pla de Santa Maria (28) ⚠️ | el Pla de Santa Maria › Alt Camp | 6 |
| Forêt de l'Ametlla de Mar (186) ⚠️ | l'Ametlla de Mar › Baix Ebre | 6 |
| Bois de la Secuita ⚠️ | la Secuita › Tarragonès | 6 |
| Bois de el Catllar (10) ⚠️ | el Catllar › Tarragonès | 6 |
| Bois de el Catllar (14) ⚠️ | el Catllar › Tarragonès | 6 |
| Forêt de Horta de Sant Joan (31) ⚠️ | Horta de Sant Joan › Terra Alta | 6 |
| Forêt de Rasquera (12) ⚠️ | Rasquera › Ribera d'Ebre | 6 |
| Forêt de Bellmunt del Priorat (2) ⚠️ | Bellmunt del Priorat › Priorat | 6 |
| Forêt de Falset (9) ⚠️ | Falset › Priorat | 6 |
| Forêt de Vilanova d'Escornalbou (27) ⚠️ | Vilanova d'Escornalbou › Baix Camp | 6 |
| Forêt de la Bisbal del Penedès (21) ⚠️ | la Bisbal del Penedès › Baix Penedès | 6 |
| Forêt de Cornudella de Montsant (77) ⚠️ | Cornudella de Montsant › Priorat | 6 |
| Bois de el Montmell (5) ⚠️ | el Montmell › Baix Penedès | 6 |
| Bois de la Bisbal del Penedès (8) ⚠️ | la Bisbal del Penedès › Baix Penedès | 6 |
| Forêt de Santa Coloma de Queralt (18) ⚠️ | Santa Coloma de Queralt › Conca de Barberà | 6 |
| Forêt de Santa Coloma de Queralt (22) ⚠️ | Santa Coloma de Queralt › Conca de Barberà | 6 |
| Forêt de l'Aleixar (16) ⚠️ | l'Aleixar › Baix Camp | 6 |
| Forêt de Alcover (10) ⚠️ | Alcover › Alt Camp | 6 |
| Bois de Alcover (8) ⚠️ | Alcover › Alt Camp | 6 |
| Bois de Tivenys ⚠️ | Tivenys › Baix Ebre | 6 |
| Forêt de Tortosa (15) ⚠️ | Tortosa › Baix Ebre | 6 |
| Forêt de Mont-ral (19) ⚠️ | Mont-ral › Alt Camp | 6 |
| Forêt de l'Espluga de Francolí (12) ⚠️ | l'Espluga de Francolí › Conca de Barberà | 6 |
| Forêt de Tortosa (33) ⚠️ | Tortosa › Baix Ebre | 6 |
| Forêt de Calafell (36) ⚠️ | Calafell › Baix Penedès | 6 |
| Forêt de Arnes (21) ⚠️ | Arnes › Terra Alta | 6 |
| Bois de Aiguamúrcia (4) ⚠️ | Aiguamúrcia › Alt Camp | 6 |
| Forêt de la Sénia (22) ⚠️ | la Sénia › Montsià | 6 |
| Forêt de la Sénia (28) ⚠️ | la Sénia › Montsià | 6 |
| Forêt de Roquetes (11) ⚠️ | Roquetes › Baix Ebre | 6 |
| Forêt de Roquetes (17) ⚠️ | Roquetes › Baix Ebre | 6 |
| Forêt de la Riera de Gaià (3) ⚠️ | la Riera de Gaià › Tarragonès | 6 |
| Forêt de Tortosa (42) ⚠️ | Tortosa › Baix Ebre | 6 |
| Forêt de Alcanar (5) ⚠️ | Alcanar › Montsià | 6 |
| Forêt de Cunit (19) ⚠️ | Cunit › Baix Penedès | 6 |
| Forêt de la Vilella Baixa (12) ⚠️ | la Vilella Baixa › Priorat | 6 |
| Forêt de Riba-roja d'Ebre (17) ⚠️ | Riba-roja d'Ebre › Ribera d'Ebre | 6 |
| Forêt de Renau (3) ⚠️ | Renau › Tarragonès | 6 |
| Forêt de Mont-roig del Camp (141) ⚠️ | Mont-roig del Camp › Baix Camp | 6 |
| Forêt de Mont-roig del Camp (143) ⚠️ | Mont-roig del Camp › Baix Camp | 6 |
| Forêt de Pratdip (49) ⚠️ | Pratdip › Baix Camp | 6 |
| Forêt de la Pobla de Montornès (5) ⚠️ | la Pobla de Montornès › Tarragonès | 6 |
| Forêt de l'Aldea (5) ⚠️ | l'Aldea › Baix Ebre | 6 |
| Illa de Jesús ⚠️ | Tortosa › Baix Ebre | 5 |
| Forêt de el Montmell ⚠️ | el Montmell › Baix Penedès | 5 |
| Forêt de Batea (17) ⚠️ | Batea › Terra Alta | 5 |
| Forêt de Llorac (6) ⚠️ | Llorac › Conca de Barberà | 5 |
| Forêt de Llorac (7) ⚠️ | Llorac › Conca de Barberà | 5 |
| Forêt de Alfara de Carles (13) ⚠️ | Alfara de Carles › Baix Ebre | 5 |
| Forêt de Santa Coloma de Queralt (8) ⚠️ | Santa Coloma de Queralt › Conca de Barberà | 5 |
| Forêt de Capçanes (4) ⚠️ | Capçanes › Priorat | 5 |
| Bois de Passanant i Belltall (23) ⚠️ | Passanant i Belltall › Conca de Barberà | 5 |
| Bois de Passanant i Belltall (30) ⚠️ | Passanant i Belltall › Conca de Barberà | 5 |
| Bois de Passanant i Belltall (46) ⚠️ | Passanant i Belltall › Conca de Barberà | 5 |
| Forêt de el Pla de Santa Maria (11) ⚠️ | Cabra del Camp › Alt Camp | 5 |
| Forêt de l'Ametlla de Mar (18) ⚠️ | l'Ametlla de Mar › Baix Ebre | 5 |
| Forêt de l'Ametlla de Mar (142) ⚠️ | l'Ametlla de Mar › Baix Ebre | 5 |
| Bois de el Vendrell ⚠️ | el Vendrell › Baix Penedès | 5 |
| Bosc de Mercader ⚠️ | la Secuita › Tarragonès | 5 |
| Bosc de Cal Porta ⚠️ | la Secuita › Tarragonès | 5 |
| Bois de la Secuita (5) ⚠️ | la Secuita › Tarragonès | 5 |
| Bois de el Catllar (11) ⚠️ | el Catllar › Tarragonès | 5 |
| Bois de la Secuita (12) ⚠️ | la Secuita › Tarragonès | 5 |
| Forêt de Mont-roig del Camp (18) ⚠️ | Mont-roig del Camp › Baix Camp | 5 |
| Bois de Horta de Sant Joan (2) ⚠️ | Horta de Sant Joan › Terra Alta | 5 |
| Forêt de Ulldemolins (14) ⚠️ | Ulldemolins › Priorat | 5 |
| Forêt de l'Aleixar (2) ⚠️ | l'Aleixar › Baix Camp | 5 |
| Bois de el Pla de Santa Maria (3) ⚠️ | el Pla de Santa Maria › Alt Camp | 5 |
| Bois de Vila-rodona ⚠️ | Vila-rodona › Alt Camp | 5 |
| Bois de Torroja del Priorat (3) ⚠️ | Torroja del Priorat › Priorat | 5 |
| Forêt de Querol (14) ⚠️ | Querol › Alt Camp | 5 |
| Forêt de l'Albiol (5) ⚠️ | l'Albiol › Baix Camp | 5 |
| Forêt de Mont-roig del Camp (34) ⚠️ | Mont-roig del Camp › Baix Camp | 5 |
| Forêt de Banyeres del Penedès (29) ⚠️ | Banyeres del Penedès › Baix Penedès | 5 |
| Forêt de Cornudella de Montsant (86) ⚠️ | Cornudella de Montsant › Priorat | 5 |
| Forêt de Querol (21) ⚠️ | Querol › Alt Camp | 5 |
| Forêt de Prades (20) ⚠️ | Prades › Baix Camp | 5 |
| Forêt de Llorac (11) ⚠️ | Llorac › Conca de Barberà | 5 |
| Forêt de Mont-ral (12) ⚠️ | Mont-ral › Alt Camp | 5 |
| Forêt de Colldejou (6) ⚠️ | Colldejou › Baix Camp | 5 |
| Forêt de Colldejou (12) ⚠️ | Colldejou › Baix Camp | 5 |
| Forêt de la Riba ⚠️ | la Riba › Alt Camp | 5 |
| Forêt de Cornudella de Montsant (146) ⚠️ | Cornudella de Montsant › Priorat | 5 |
| Parc del Francolí (2) ⚠️ | Tarragona › Tarragonès | 5 |
| Forêt de Tarragona (49) ⚠️ | Tarragona › Tarragonès | 5 |
| Forêt de Mont-roig del Camp (88) ⚠️ | Mont-roig del Camp › Baix Camp | 5 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (23) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 5 |
| Forêt de Creixell (9) ⚠️ | Creixell › Tarragonès | 5 |
| Forêt de Querol (22) ⚠️ | Querol › Alt Camp | 5 |
| Forêt de la Sénia (24) ⚠️ | la Sénia › Montsià | 5 |
| Forêt de Tarragona (56) ⚠️ | Tarragona › Tarragonès | 5 |
| Forêt de Amposta (5) ⚠️ | Amposta › Montsià | 5 |
| Forêt de Deltebre (7) ⚠️ | Deltebre › Baix Ebre | 5 |
| Forêt de Cunit (25) ⚠️ | Cunit › Baix Penedès | 5 |
| Forêt de Alcover (14) ⚠️ | Alcover › Alt Camp | 5 |
| Forêt de la Morera de Montsant (95) ⚠️ | la Morera de Montsant › Priorat | 5 |
| Forêt de Capafonts (50) ⚠️ | Capafonts › Baix Camp | 5 |
| Forêt de Capafonts (52) ⚠️ | Capafonts › Baix Camp | 5 |
| Forêt de Querol (54) ⚠️ | Querol › Alt Camp | 5 |
| Forêt de Mont-roig del Camp (140) ⚠️ | Mont-roig del Camp › Baix Camp | 5 |
| Forêt de Riba-roja d'Ebre (20) ⚠️ | Riba-roja d'Ebre › Ribera d'Ebre | 5 |
| Forêt de Colldejou (25) ⚠️ | Colldejou › Baix Camp | 5 |
| Forêt de Colldejou (32) ⚠️ | Colldejou › Baix Camp | 5 |
| Parc de la Ciutat ⚠️ | Tarragona › Tarragonès | 4 |
| Forêt de Santa Coloma de Queralt ⚠️ | Santa Coloma de Queralt › Conca de Barberà | 4 |
| Forêt de Vimbodí i Poblet (7) ⚠️ | Vimbodí i Poblet › Conca de Barberà | 4 |
| Forêt de Batea (14) ⚠️ | Batea › Terra Alta | 4 |
| Forêt de Paüls (5) ⚠️ | Paüls › Baix Ebre | 4 |
| Forêt de Santa Coloma de Queralt (6) ⚠️ | Santa Coloma de Queralt › Conca de Barberà | 4 |
| Forêt de Vimbodí i Poblet (19) ⚠️ | Vimbodí i Poblet › Conca de Barberà | 4 |
| Forêt de Benifallet (12) ⚠️ | Benifallet › Baix Ebre | 4 |
| Forêt de Santa Coloma de Queralt (10) ⚠️ | Santa Coloma de Queralt › Conca de Barberà | 4 |
| Forêt de el Perelló (9) ⚠️ | el Perelló › Baix Ebre | 4 |
| les Socarrades ⚠️ | Cornudella de Montsant › Priorat | 4 |
| Forêt de Albinyana (2) ⚠️ | Albinyana › Baix Penedès | 4 |
| Forêt de el Vendrell ⚠️ | el Vendrell › Baix Penedès | 4 |
| Forêt de el Vendrell (3) ⚠️ | el Vendrell › Baix Penedès | 4 |
| Forêt de la Morera de Montsant (14) ⚠️ | la Morera de Montsant › Priorat | 4 |
| Forêt de Cornudella de Montsant (12) ⚠️ | Cornudella de Montsant › Priorat | 4 |
| Forêt de Santa Oliva (7) ⚠️ | Santa Oliva › Baix Penedès | 4 |
| Forêt de Bonastre ⚠️ | Bonastre › Baix Penedès | 4 |
| Forêt de Mont-roig del Camp (7) ⚠️ | Mont-roig del Camp › Baix Camp | 4 |
| Forêt de Mont-roig del Camp (10) ⚠️ | Mont-roig del Camp › Baix Camp | 4 |
| Forêt de Capafonts (3) ⚠️ | Capafonts › Baix Camp | 4 |
| Parc de Bonavista ⚠️ | Tarragona › Tarragonès | 4 |
| Forêt de l'Ametlla de Mar (5) ⚠️ | l'Ametlla de Mar › Baix Ebre | 4 |
| Forêt de l'Ametlla de Mar (83) ⚠️ | l'Ametlla de Mar › Baix Ebre | 4 |
| Forêt de l'Ametlla de Mar (144) ⚠️ | l'Ametlla de Mar › Baix Ebre | 4 |
| Forêt de l'Ametlla de Mar (162) ⚠️ | l'Ametlla de Mar › Baix Ebre | 4 |
| Forêt de l'Ametlla de Mar (164) ⚠️ | l'Ametlla de Mar › Baix Ebre | 4 |
| Forêt de Valls (5) ⚠️ | Valls › Alt Camp | 4 |
| Forêt de Valls (6) ⚠️ | Valls › Alt Camp | 4 |
| Forêt de Figuerola del Camp (2) ⚠️ | Figuerola del Camp › Alt Camp | 4 |
| Bois de Horta de Sant Joan (3) ⚠️ | Horta de Sant Joan › Terra Alta | 4 |
| Forêt de Rasquera (11) ⚠️ | Rasquera › Ribera d'Ebre | 4 |
| Bois de el Pla de Santa Maria (5) ⚠️ | el Pla de Santa Maria › Alt Camp | 4 |
| Bois de Aiguamúrcia ⚠️ | Aiguamúrcia › Alt Camp | 4 |
| Forêt de Mont-roig del Camp (74) ⚠️ | Mont-roig del Camp › Baix Camp | 4 |
| Forêt de Mont-roig del Camp (77) ⚠️ | Mont-roig del Camp › Baix Camp | 4 |
| Forêt de Mont-roig del Camp (81) ⚠️ | Mont-roig del Camp › Baix Camp | 4 |
| Forêt de Pratdip (39) ⚠️ | Pratdip › Baix Camp | 4 |
| Forêt de Cornudella de Montsant (65) ⚠️ | Cornudella de Montsant › Priorat | 4 |
| Forêt de Cornudella de Montsant (70) ⚠️ | Cornudella de Montsant › Priorat | 4 |
| Forêt de Cornudella de Montsant (71) ⚠️ | Cornudella de Montsant › Priorat | 4 |
| Forêt de Reus (14) ⚠️ | Reus › Baix Camp | 4 |
| Forêt de Capafonts (36) ⚠️ | Capafonts › Baix Camp | 4 |
| Forêt de Santa Coloma de Queralt (29) ⚠️ | Santa Coloma de Queralt › Conca de Barberà | 4 |
| Forêt de Santa Coloma de Queralt (32) ⚠️ | Santa Coloma de Queralt › Conca de Barberà | 4 |
| Forêt de Santa Coloma de Queralt (38) ⚠️ | Santa Coloma de Queralt › Conca de Barberà | 4 |
| Forêt de Vilaplana (10) ⚠️ | Vilaplana › Baix Camp | 4 |
| Bois de Alcover (13) ⚠️ | Alcover › Alt Camp | 4 |
| Forêt de la Febró (5) ⚠️ | la Febró › Baix Camp | 4 |
| Bois de el Montmell (9) ⚠️ | el Montmell › Baix Penedès | 4 |
| Forêt de la Selva del Camp (61) ⚠️ | la Selva del Camp › Baix Camp | 4 |
| Bosc Gran ⚠️ | Salou › Tarragonès | 4 |
| Forêt de Tarragona (53) ⚠️ | Tarragona › Tarragonès | 4 |
| Forêt de Tortosa (27) ⚠️ | Tortosa › Baix Ebre | 4 |
| Bois de Horta de Sant Joan (13) ⚠️ | Horta de Sant Joan › Terra Alta | 4 |
| Forêt de Ulldemolins (83) ⚠️ | Ulldemolins › Priorat | 4 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (26) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 4 |
| Forêt de Altafulla (4) ⚠️ | Altafulla › Tarragonès | 4 |
| Forêt de Creixell (8) ⚠️ | Creixell › Tarragonès | 4 |
| Forêt de el Vendrell (44) ⚠️ | el Vendrell › Baix Penedès | 4 |
| Forêt de Roquetes (9) ⚠️ | Roquetes › Baix Ebre | 4 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (36) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 4 |
| Forêt de Mont-roig del Camp (110) ⚠️ | Mont-roig del Camp › Baix Camp | 4 |
| Forêt de Mont-roig del Camp (120) ⚠️ | Mont-roig del Camp › Baix Camp | 4 |
| Forêt de Salou (28) ⚠️ | Salou › Tarragonès | 4 |
| Forêt de Tarragona (61) ⚠️ | Tarragona › Tarragonès | 4 |
| Forêt de Tarragona (62) ⚠️ | Tarragona › Tarragonès | 4 |
| Forêt de Sant Jaume d'Enveja (2) ⚠️ | Sant Jaume d'Enveja › Montsià | 4 |
| Forêt de Sant Jaume d'Enveja (9) ⚠️ | Sant Jaume d'Enveja › Montsià | 4 |
| Forêt de Sant Jaume d'Enveja (12) ⚠️ | Sant Jaume d'Enveja › Montsià | 4 |
| Forêt de l'Ametlla de Mar (209) ⚠️ | l'Ametlla de Mar › Baix Ebre | 4 |
| Forêt de Mont-roig del Camp (130) ⚠️ | Mont-roig del Camp › Baix Camp | 4 |
| Forêt de Cunit (18) ⚠️ | Cunit › Baix Penedès | 4 |
| Forêt de Calafell (47) ⚠️ | Calafell › Baix Penedès | 4 |
| Forêt de Calafell (48) ⚠️ | Calafell › Baix Penedès | 4 |
| Forêt de Alcover (17) ⚠️ | Alcover › Alt Camp | 4 |
| Forêt de Prades (60) ⚠️ | Prades › Baix Camp | 4 |
| Forêt de la Selva del Camp (64) ⚠️ | la Selva del Camp › Baix Camp | 4 |
| Forêt de Mont-roig del Camp (145) ⚠️ | Mont-roig del Camp › Baix Camp | 4 |
| Forêt de Tivissa (3) ⚠️ | Tivissa › Ribera d'Ebre | 3 |
| Forêt de la Palma d'Ebre (2) ⚠️ | la Palma d'Ebre › Ribera d'Ebre | 3 |
| Forêt de Horta de Sant Joan (4) ⚠️ | Horta de Sant Joan › Terra Alta | 3 |
| Bois de Senan (2) ⚠️ | Senan › Conca de Barberà | 3 |
| Forêt de Ulldemolins (4) ⚠️ | Ulldemolins › Priorat | 3 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (9) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 3 |
| Forêt de Querol (5) ⚠️ | Querol › Alt Camp | 3 |
| Forêt de el Perelló (10) ⚠️ | el Perelló › Baix Ebre | 3 |
| Parc de Cambrils ⚠️ | Cambrils › Baix Camp | 3 |
| Forêt de Tarragona (6) ⚠️ | Tarragona › Tarragonès | 3 |
| Parc de Mas Iglesias ⚠️ | Reus › Baix Camp | 3 |
| Parc de Salou (94) ⚠️ | Salou › Tarragonès | 3 |
| Forêt de el Vendrell (2) ⚠️ | el Vendrell › Baix Penedès | 3 |
| Bois de Camarles (2) ⚠️ | Camarles › Baix Ebre | 3 |
| Forêt de el Vendrell (6) ⚠️ | el Vendrell › Baix Penedès | 3 |
| Forêt de Sant Jaume dels Domenys (2) ⚠️ | Sant Jaume dels Domenys › Baix Penedès | 3 |
| Forêt de l'Arboç (19) ⚠️ | l'Arboç › Baix Penedès | 3 |
| Forêt de Ulldecona ⚠️ | Ulldecona › Montsià | 3 |
| les Províncies ⚠️ | Cambrils › Baix Camp | 3 |
| Forêt de la Morera de Montsant (13) ⚠️ | la Morera de Montsant › Priorat | 3 |
| Forêt de la Morera de Montsant (20) ⚠️ | la Morera de Montsant › Priorat | 3 |
| Forêt de Banyeres del Penedès (19) ⚠️ | Banyeres del Penedès › Baix Penedès | 3 |
| Forêt de Bonastre (5) ⚠️ | Bonastre › Baix Penedès | 3 |
| Forêt de Horta de Sant Joan (30) ⚠️ | Horta de Sant Joan › Terra Alta | 3 |
| Forêt de la Bisbal del Penedès (4) ⚠️ | la Bisbal del Penedès › Baix Penedès | 3 |
| Bois de Passanant i Belltall (60) ⚠️ | Passanant i Belltall › Conca de Barberà | 3 |
| Forêt de el Pla de Santa Maria (4) ⚠️ | el Pla de Santa Maria › Alt Camp | 3 |
| Forêt de Sant Jaume dels Domenys (17) ⚠️ | Sant Jaume dels Domenys › Baix Penedès | 3 |
| Bosc de Sant Joan ⚠️ | el Pla de Santa Maria › Alt Camp | 3 |
| Forêt de Capafonts (2) ⚠️ | Capafonts › Baix Camp | 3 |
| Forêt de Mont-ral (5) ⚠️ | Mont-ral › Alt Camp | 3 |
| Bosc del Cendrós ⚠️ | Alió › Alt Camp | 3 |
| Parc del Francolí ⚠️ | Tarragona › Tarragonès | 3 |
| Forêt de l'Ametlla de Mar (19) ⚠️ | l'Ametlla de Mar › Baix Ebre | 3 |
| Forêt de l'Ametlla de Mar (21) ⚠️ | l'Ametlla de Mar › Baix Ebre | 3 |
| Forêt de l'Ametlla de Mar (62) ⚠️ | l'Ametlla de Mar › Baix Ebre | 3 |
| Forêt de l'Ametlla de Mar (138) ⚠️ | l'Ametlla de Mar › Baix Ebre | 3 |
| Forêt de l'Ametlla de Mar (170) ⚠️ | l'Ametlla de Mar › Baix Ebre | 3 |
| Forêt de l'Ametlla de Mar (172) ⚠️ | l'Ametlla de Mar › Baix Ebre | 3 |
| Forêt de l'Ametlla de Mar (173) ⚠️ | l'Ametlla de Mar › Baix Ebre | 3 |
| Forêt de Banyeres del Penedès (21) ⚠️ | Banyeres del Penedès › Baix Penedès | 3 |
| Bosc de Ralet ⚠️ | la Secuita › Tarragonès | 3 |
| Bois de el Catllar (7) ⚠️ | el Catllar › Tarragonès | 3 |
| Bois de el Catllar (13) ⚠️ | el Catllar › Tarragonès | 3 |
| Bois de el Catllar (15) ⚠️ | el Catllar › Tarragonès | 3 |
| Bois de els Pallaresos (3) ⚠️ | els Pallaresos › Tarragonès | 3 |
| Bois de Tarragona (5) ⚠️ | Tarragona › Tarragonès | 3 |
| Bois de Horta de Sant Joan (4) ⚠️ | Horta de Sant Joan › Terra Alta | 3 |
| Bois de Godall ⚠️ | Godall › Montsià | 3 |
| Bois de Santa Coloma de Queralt ⚠️ | Santa Coloma de Queralt › Conca de Barberà | 3 |
| Forêt de Montbrió del Camp (2) ⚠️ | Montbrió del Camp › Baix Camp | 3 |
| Forêt de Vilanova d'Escornalbou (5) ⚠️ | Vilanova d'Escornalbou › Baix Camp | 3 |
| Forêt de Mont-roig del Camp (24) ⚠️ | Mont-roig del Camp › Baix Camp | 3 |
| Forêt de l'Argentera (3) ⚠️ | l'Argentera › Baix Camp | 3 |
| Forêt de Marçà (3) ⚠️ | Marçà › Priorat | 3 |
| Forêt de Falset (12) ⚠️ | Falset › Priorat | 3 |
| Forêt de Capafonts (11) ⚠️ | Capafonts › Baix Camp | 3 |
| Forêt de Capafonts (12) ⚠️ | Capafonts › Baix Camp | 3 |
| Forêt de Mont-roig del Camp (48) ⚠️ | Mont-roig del Camp › Baix Camp | 3 |
| Forêt de Mont-roig del Camp (59) ⚠️ | Mont-roig del Camp › Baix Camp | 3 |
| Forêt de Mont-roig del Camp (75) ⚠️ | Mont-roig del Camp › Baix Camp | 3 |
| Forêt de Mont-roig del Camp (78) ⚠️ | Mont-roig del Camp › Baix Camp | 3 |
| Forêt de Mont-roig del Camp (79) ⚠️ | Mont-roig del Camp › Baix Camp | 3 |
| Bois de Margalef ⚠️ | Margalef › Priorat | 3 |
| Forêt de la Bisbal del Penedès (16) ⚠️ | la Bisbal del Penedès › Baix Penedès | 3 |
| Bois de la Bisbal del Penedès (6) ⚠️ | la Bisbal del Penedès › Baix Penedès | 3 |
| Forêt de Cornudella de Montsant (80) ⚠️ | Cornudella de Montsant › Priorat | 3 |
| Parc de Reus (54) ⚠️ | Reus › Baix Camp | 3 |
| Bois de el Pinell de Brai (2) ⚠️ | el Pinell de Brai › Terra Alta | 3 |
| Forêt de la Vilella Baixa (4) ⚠️ | la Vilella Baixa › Priorat | 3 |
| Forêt de l'Aleixar (9) ⚠️ | l'Aleixar › Baix Camp | 3 |
| Forêt de la Selva del Camp (4) ⚠️ | la Selva del Camp › Baix Camp | 3 |
| Forêt de la Selva del Camp (6) ⚠️ | la Selva del Camp › Baix Camp | 3 |
| Forêt de la Selva del Camp (11) ⚠️ | la Selva del Camp › Baix Camp | 3 |
| Forêt de la Selva del Camp (34) ⚠️ | la Selva del Camp › Baix Camp | 3 |
| Forêt de Tivenys (4) ⚠️ | Tivenys › Baix Ebre | 3 |
| Forêt de la Torre de Fontaubella ⚠️ | la Torre de Fontaubella › Priorat | 3 |
| Forêt de l'Albiol (10) ⚠️ | l'Albiol › Baix Camp | 3 |
| Forêt de Mont-ral (17) ⚠️ | Mont-ral › Alt Camp | 3 |
| Forêt de Cornudella de Montsant (152) ⚠️ | Cornudella de Montsant › Priorat | 3 |
| Forêt de Tortosa (28) ⚠️ | Tortosa › Baix Ebre | 3 |
| Forêt de Tortosa (32) ⚠️ | Tortosa › Baix Ebre | 3 |
| Forêt de Ulldemolins (82) ⚠️ | Ulldemolins › Priorat | 3 |
| Forêt de Margalef (20) ⚠️ | Margalef › Priorat | 3 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (27) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 3 |
| Forêt de Creixell (6) ⚠️ | Creixell › Tarragonès | 3 |
| Bosc de la Bassota ⚠️ | Bràfim › Alt Camp | 3 |
| Forêt de l'Argentera (9) ⚠️ | l'Argentera › Baix Camp | 3 |
| Bois de Aiguamúrcia (3) ⚠️ | Aiguamúrcia › Alt Camp | 3 |
| Forêt de Tortosa (40) ⚠️ | Tortosa › Baix Ebre | 3 |
| Forêt de la Sénia (42) ⚠️ | la Sénia › Montsià | 3 |
| Forêt de l'Ametlla de Mar (197) ⚠️ | l'Ametlla de Mar › Baix Ebre | 3 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (31) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 3 |
| Forêt de Mont-roig del Camp (91) ⚠️ | Mont-roig del Camp › Baix Camp | 3 |
| Forêt de Mont-roig del Camp (123) ⚠️ | Mont-roig del Camp › Baix Camp | 3 |
| Forêt de Salou (25) ⚠️ | Salou › Tarragonès | 3 |
| Forêt de Salou (30) ⚠️ | Salou › Tarragonès | 3 |
| Forêt de Salou (32) ⚠️ | Salou › Tarragonès | 3 |
| Forêt de Salou (36) ⚠️ | Salou › Tarragonès | 3 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (55) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 3 |
| Forêt de Tarragona (55) ⚠️ | Tarragona › Tarragonès | 3 |
| Forêt de l'Ametlla de Mar (213) ⚠️ | l'Ametlla de Mar › Baix Ebre | 3 |
| Forêt de Alcanar (11) ⚠️ | Alcanar › Montsià | 3 |
| Forêt de Alcanar (19) ⚠️ | Alcanar › Montsià | 3 |
| Forêt de Calafell (50) ⚠️ | Calafell › Baix Penedès | 3 |
| Parc de Cambrils (52) ⚠️ | Cambrils › Baix Camp | 3 |
| Forêt de Ulldemolins (89) ⚠️ | Ulldemolins › Priorat | 3 |
| Forêt de Querol (42) ⚠️ | Querol › Alt Camp | 3 |
| Forêt de la Vilella Baixa (14) ⚠️ | la Vilella Baixa › Priorat | 3 |
| Forêt de Renau (4) ⚠️ | Renau › Tarragonès | 3 |
| Forêt de Mont-roig del Camp (142) ⚠️ | Mont-roig del Camp › Baix Camp | 3 |
| Forêt de Roda de Berà (22) ⚠️ | Roda de Berà › Tarragonès | 3 |
| Parc de l'Ampolla (2) ⚠️ | l'Ampolla › Baix Ebre | 3 |
| Forêt de Cornudella de Montsant (156) ⚠️ | Cornudella de Montsant › Priorat | 3 |
| Forêt de Colldejou (26) ⚠️ | Colldejou › Baix Camp | 3 |
| Forêt de Vilalba dels Arcs (2) ⚠️ | Vilalba dels Arcs › Terra Alta | 2 |
| Forêt de Vimbodí i Poblet (6) ⚠️ | Vimbodí i Poblet › Conca de Barberà | 2 |
| Forêt de la Fatarella (3) ⚠️ | la Fatarella › Terra Alta | 2 |
| Forêt de Flix (10) ⚠️ | Flix › Ribera d'Ebre | 2 |
| Forêt de Flix (16) ⚠️ | Flix › Ribera d'Ebre | 2 |
| Forêt de Ulldemolins (3) ⚠️ | Ulldemolins › Priorat | 2 |
| Forêt de Llorac (4) ⚠️ | Llorac › Conca de Barberà | 2 |
| Forêt de Riba-roja d'Ebre (11) ⚠️ | Riba-roja d'Ebre › Ribera d'Ebre | 2 |
| Forêt de Alfara de Carles (8) ⚠️ | Alfara de Carles › Baix Ebre | 2 |
| Forêt de Querol (3) ⚠️ | Querol › Alt Camp | 2 |
| Forêt de Querol (4) ⚠️ | Querol › Alt Camp | 2 |
| Forêt de Alfara de Carles (14) ⚠️ | Alfara de Carles › Baix Ebre | 2 |
| Forêt de Horta de Sant Joan (25) ⚠️ | Horta de Sant Joan › Terra Alta | 2 |
| Forêt de Aiguamúrcia (15) ⚠️ | Aiguamúrcia › Alt Camp | 2 |
| Bois de Flix (2) ⚠️ | Flix › Ribera d'Ebre | 2 |
| Bois de Passanant i Belltall (34) ⚠️ | Passanant i Belltall › Conca de Barberà | 2 |
| Bois de Passanant i Belltall (37) ⚠️ | Passanant i Belltall › Conca de Barberà | 2 |
| Parc municipal Teodor González ⚠️ | Tortosa › Baix Ebre | 2 |
| Bois de Conesa (3) ⚠️ | Conesa › Conca de Barberà | 2 |
| Parc del Pinaret ⚠️ | Cambrils › Baix Camp | 2 |
| Bois de Salou ⚠️ | Salou › Tarragonès | 2 |
| Bois de Salou (3) ⚠️ | Salou › Tarragonès | 2 |
| Forêt de Santa Oliva (4) ⚠️ | Santa Oliva › Baix Penedès | 2 |
| Forêt de Bellvei (8) ⚠️ | Bellvei › Baix Penedès | 2 |
| Forêt de el Vendrell (8) ⚠️ | el Vendrell › Baix Penedès | 2 |
| Forêt de Calafell (5) ⚠️ | Calafell › Baix Penedès | 2 |
| Forêt de Salou (2) ⚠️ | Salou › Tarragonès | 2 |
| Forêt de Ulldecona (2) ⚠️ | Ulldecona › Montsià | 2 |
| Bois de Conesa (9) ⚠️ | Conesa › Conca de Barberà | 2 |
| Forêt de la Morera de Montsant (6) ⚠️ | la Morera de Montsant › Priorat | 2 |
| Forêt de Cornudella de Montsant (5) ⚠️ | Cornudella de Montsant › Priorat | 2 |
| Forêt de Cornudella de Montsant (8) ⚠️ | Cornudella de Montsant › Priorat | 2 |
| Forêt de Poboleda (16) ⚠️ | Poboleda › Priorat | 2 |
| Forêt de la Morera de Montsant (17) ⚠️ | la Morera de Montsant › Priorat | 2 |
| Forêt de el Catllar ⚠️ | el Catllar › Tarragonès | 2 |
| Forêt de Ascó (9) ⚠️ | Ascó › Ribera d'Ebre | 2 |
| Forêt de Ascó (10) ⚠️ | Ascó › Ribera d'Ebre | 2 |
| Bois de Montblanc ⚠️ | Montblanc › Conca de Barberà | 2 |
| Forêt de Montblanc (13) ⚠️ | Montblanc › Conca de Barberà | 2 |
| Forêt de la Bisbal del Penedès (6) ⚠️ | la Bisbal del Penedès › Baix Penedès | 2 |
| Forêt de Aiguamúrcia (18) ⚠️ | Aiguamúrcia › Alt Camp | 2 |
| Forêt de el Pla de Santa Maria ⚠️ | el Pla de Santa Maria › Alt Camp | 2 |
| Forêt de la Bisbal del Penedès (10) ⚠️ | la Bisbal del Penedès › Baix Penedès | 2 |
| Parc de Salou (221) ⚠️ | Salou › Tarragonès | 2 |
| Bosc de la Capona ⚠️ | el Pla de Santa Maria › Alt Camp | 2 |
| Bois de Passanant i Belltall (64) ⚠️ | Passanant i Belltall › Conca de Barberà | 2 |
| Forêt de el Pla de Santa Maria (19) ⚠️ | el Pla de Santa Maria › Alt Camp | 2 |
| Forêt de el Pla de Santa Maria (31) ⚠️ | el Pla de Santa Maria › Alt Camp | 2 |
| Parc de Vandellòs i l'Hospitalet de l'Infant (2) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 2 |
| Forêt de Corbera d'Ebre (13) ⚠️ | Corbera d'Ebre › Terra Alta | 2 |
| Bois de Vandellòs i l'Hospitalet de l'Infant (3) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 2 |
| Forêt de l'Ametlla de Mar ⚠️ | l'Ametlla de Mar › Baix Ebre | 2 |
| Forêt de l'Ametlla de Mar (16) ⚠️ | l'Ametlla de Mar › Baix Ebre | 2 |
| Forêt de l'Ametlla de Mar (23) ⚠️ | l'Ametlla de Mar › Baix Ebre | 2 |
| Forêt de l'Ametlla de Mar (43) ⚠️ | l'Ametlla de Mar › Baix Ebre | 2 |
| Forêt de l'Ametlla de Mar (60) ⚠️ | l'Ametlla de Mar › Baix Ebre | 2 |
| Forêt de l'Ametlla de Mar (63) ⚠️ | l'Ametlla de Mar › Baix Ebre | 2 |
| Forêt de l'Ametlla de Mar (80) ⚠️ | l'Ametlla de Mar › Baix Ebre | 2 |
| Forêt de l'Ametlla de Mar (89) ⚠️ | l'Ametlla de Mar › Baix Ebre | 2 |
| Forêt de l'Ametlla de Mar (129) ⚠️ | l'Ametlla de Mar › Baix Ebre | 2 |
| Forêt de l'Ametlla de Mar (132) ⚠️ | l'Ametlla de Mar › Baix Ebre | 2 |
| Forêt de l'Ametlla de Mar (152) ⚠️ | l'Ametlla de Mar › Baix Ebre | 2 |
| Forêt de l'Ametlla de Mar (154) ⚠️ | l'Ametlla de Mar › Baix Ebre | 2 |
| Forêt de l'Ametlla de Mar (179) ⚠️ | l'Ametlla de Mar › Baix Ebre | 2 |
| Bosc Mediterrani ⚠️ | Tarragona › Tarragonès | 2 |
| Bois de Mont-roig del Camp (11) ⚠️ | Mont-roig del Camp › Baix Camp | 2 |
| Bosc de la Rajola ⚠️ | la Secuita › Tarragonès | 2 |
| Bosc de Capestany ⚠️ | Nulles › Alt Camp | 2 |
| Bois de la Secuita (9) ⚠️ | la Secuita › Tarragonès | 2 |
| Bois de els Pallaresos ⚠️ | els Pallaresos › Tarragonès | 2 |
| Bois de els Pallaresos (2) ⚠️ | els Pallaresos › Tarragonès | 2 |
| Bois de la Secuita (15) ⚠️ | la Secuita › Tarragonès | 2 |
| Bois de el Catllar (19) ⚠️ | el Catllar › Tarragonès | 2 |
| Bois de la Secuita (19) ⚠️ | la Secuita › Tarragonès | 2 |
| Forêt de Mont-roig del Camp (13) ⚠️ | Mont-roig del Camp › Baix Camp | 2 |
| Forêt de Mont-roig del Camp (17) ⚠️ | Mont-roig del Camp › Baix Camp | 2 |
| Forêt de Mont-roig del Camp (21) ⚠️ | Mont-roig del Camp › Baix Camp | 2 |
| Bois de Horta de Sant Joan (5) ⚠️ | Horta de Sant Joan › Terra Alta | 2 |
| Bois de Horta de Sant Joan (7) ⚠️ | Horta de Sant Joan › Terra Alta | 2 |
| Bois de Horta de Sant Joan (9) ⚠️ | Horta de Sant Joan › Terra Alta | 2 |
| Bois de Capçanes ⚠️ | Capçanes › Priorat | 2 |
| Bois de Valls (2) ⚠️ | Valls › Alt Camp | 2 |
| Forêt de Ulldecona (7) ⚠️ | Ulldecona › Montsià | 2 |
| Zona picnic ⚠️ | Tarragona › Tarragonès | 2 |
| Forêt de Conesa (7) ⚠️ | Conesa › Conca de Barberà | 2 |
| Bois de Santa Coloma de Queralt (8) ⚠️ | Santa Coloma de Queralt › Conca de Barberà | 2 |
| Forêt de Mont-ral (6) ⚠️ | Mont-ral › Alt Camp | 2 |
| Forêt de Riudecanyes (4) ⚠️ | Riudecanyes › Baix Camp | 2 |
| Forêt de Godall ⚠️ | Godall › Montsià | 2 |
| Forêt de Valls (9) ⚠️ | Valls › Alt Camp | 2 |
| Bosc del Plana ⚠️ | Valls › Alt Camp | 2 |
| Forêt de Valls (12) ⚠️ | Valls › Alt Camp | 2 |
| Bois de el Pla de Santa Maria (2) ⚠️ | el Pla de Santa Maria › Alt Camp | 2 |
| Bois de el Pla de Santa Maria (7) ⚠️ | el Pla de Santa Maria › Alt Camp | 2 |
| Forêt de Tarragona (44) ⚠️ | Tarragona › Tarragonès | 2 |
| Forêt de la Selva del Camp ⚠️ | l'Aleixar › Baix Camp | 2 |
| Forêt de l'Aleixar (4) ⚠️ | l'Aleixar › Baix Camp | 2 |
| Forêt de Tivissa (28) ⚠️ | Tivissa › Ribera d'Ebre | 2 |
| Forêt de Falset (7) ⚠️ | Falset › Priorat | 2 |
| Forêt de Falset (13) ⚠️ | Falset › Priorat | 2 |
| Forêt de el Vendrell (32) ⚠️ | el Vendrell › Baix Penedès | 2 |
| Forêt de Capafonts (6) ⚠️ | Capafonts › Baix Camp | 2 |
| Bois de la Secuita (21) ⚠️ | la Secuita › Tarragonès | 2 |
| Forêt de Bonastre (9) ⚠️ | Bonastre › Baix Penedès | 2 |
| Forêt de la Pobla de Montornès (2) ⚠️ | la Pobla de Montornès › Tarragonès | 2 |
| Bois de la Pobla de Montornès ⚠️ | la Pobla de Montornès › Tarragonès | 2 |
| Forêt de Vilanova d'Escornalbou (8) ⚠️ | Vilanova d'Escornalbou › Baix Camp | 2 |
| Forêt de Vilanova d'Escornalbou (21) ⚠️ | Vilanova d'Escornalbou › Baix Camp | 2 |
| Forêt de Vilanova d'Escornalbou (30) ⚠️ | Vilanova d'Escornalbou › Baix Camp | 2 |
| Forêt de Mont-roig del Camp (35) ⚠️ | Mont-roig del Camp › Baix Camp | 2 |
| Forêt de Mont-roig del Camp (40) ⚠️ | Mont-roig del Camp › Baix Camp | 2 |
| Forêt de Mont-roig del Camp (41) ⚠️ | Mont-roig del Camp › Baix Camp | 2 |
| Forêt de Mont-roig del Camp (44) ⚠️ | Mont-roig del Camp › Baix Camp | 2 |
| Forêt de Mont-roig del Camp (45) ⚠️ | Mont-roig del Camp › Baix Camp | 2 |
| Forêt de Mont-roig del Camp (52) ⚠️ | Mont-roig del Camp › Baix Camp | 2 |
| Forêt de Mont-roig del Camp (60) ⚠️ | Mont-roig del Camp › Baix Camp | 2 |
| Forêt de Mont-roig del Camp (61) ⚠️ | Mont-roig del Camp › Baix Camp | 2 |
| Forêt de Mont-roig del Camp (64) ⚠️ | Mont-roig del Camp › Baix Camp | 2 |
| Forêt de Mont-roig del Camp (65) ⚠️ | Mont-roig del Camp › Baix Camp | 2 |
| Forêt de Mont-roig del Camp (67) ⚠️ | Mont-roig del Camp › Baix Camp | 2 |
| Forêt de Mont-roig del Camp (69) ⚠️ | Mont-roig del Camp › Baix Camp | 2 |
| Forêt de Mont-roig del Camp (83) ⚠️ | Mont-roig del Camp › Baix Camp | 2 |
| Forêt de Pratdip (17) ⚠️ | Pratdip › Baix Camp | 2 |
| Forêt de Pratdip (24) ⚠️ | Pratdip › Baix Camp | 2 |
| Forêt de Pratdip (25) ⚠️ | Pratdip › Baix Camp | 2 |
| Forêt de Pratdip (31) ⚠️ | Pratdip › Baix Camp | 2 |
| Forêt de Pratdip (33) ⚠️ | Pratdip › Baix Camp | 2 |
| Forêt de Cornudella de Montsant (60) ⚠️ | Cornudella de Montsant › Priorat | 2 |
| Forêt de Cornudella de Montsant (63) ⚠️ | Cornudella de Montsant › Priorat | 2 |
| Forêt de Ulldemolins (16) ⚠️ | Ulldemolins › Priorat | 2 |
| Forêt de la Morera de Montsant (23) ⚠️ | la Morera de Montsant › Priorat | 2 |
| Forêt de Ulldemolins (22) ⚠️ | Ulldemolins › Priorat | 2 |
| Forêt de Ulldemolins (31) ⚠️ | Ulldemolins › Priorat | 2 |
| Forêt de Albinyana (15) ⚠️ | Albinyana › Baix Penedès | 2 |
| Forêt de l'Arboç (22) ⚠️ | l'Arboç › Baix Penedès | 2 |
| Forêt de Banyeres del Penedès (28) ⚠️ | Banyeres del Penedès › Baix Penedès | 2 |
| Forêt de la Bisbal del Penedès (20) ⚠️ | la Bisbal del Penedès › Baix Penedès | 2 |
| Forêt de la Morera de Montsant (47) ⚠️ | la Morera de Montsant › Priorat | 2 |
| Parc del Mas de la Mel ⚠️ | Calafell › Baix Penedès | 2 |
| Forêt de el Pinell de Brai (8) ⚠️ | el Pinell de Brai › Terra Alta | 2 |
| Forêt de Querol (18) ⚠️ | Querol › Alt Camp | 2 |
| Forêt de Querol (20) ⚠️ | Querol › Alt Camp | 2 |
| Bois de el Pinell de Brai (3) ⚠️ | el Pinell de Brai › Terra Alta | 2 |
| Bois de el Pinell de Brai (4) ⚠️ | el Pinell de Brai › Terra Alta | 2 |
| Forêt de la Vilella Baixa (6) ⚠️ | la Vilella Baixa › Priorat | 2 |
| Forêt de la Vilella Baixa (9) ⚠️ | la Vilella Baixa › Priorat | 2 |
| Plaça de Dalmau de Cunit ⚠️ | Cunit › Baix Penedès | 2 |
| Bois de la Figuera (2) ⚠️ | la Figuera › Priorat | 2 |
| Forêt de Prades (17) ⚠️ | Prades › Baix Camp | 2 |
| Forêt de Prades (24) ⚠️ | Prades › Baix Camp | 2 |
| Forêt de Prades (25) ⚠️ | Prades › Baix Camp | 2 |
| Forêt de Prades (32) ⚠️ | Prades › Baix Camp | 2 |
| Forêt de Prades (36) ⚠️ | Prades › Baix Camp | 2 |
| Forêt de Prades (39) ⚠️ | Prades › Baix Camp | 2 |
| Forêt de Prades (54) ⚠️ | Prades › Baix Camp | 2 |
| Forêt de Santa Coloma de Queralt (17) ⚠️ | Santa Coloma de Queralt › Conca de Barberà | 2 |
| Forêt de Santa Coloma de Queralt (34) ⚠️ | Santa Coloma de Queralt › Conca de Barberà | 2 |
| Forêt de Vilaplana (7) ⚠️ | Vilaplana › Baix Camp | 2 |
| Forêt de Vilaplana (8) ⚠️ | Vilaplana › Baix Camp | 2 |
| Forêt de l'Aleixar (20) ⚠️ | l'Aleixar › Baix Camp | 2 |
| Forêt de la Selva del Camp (5) ⚠️ | la Selva del Camp › Baix Camp | 2 |
| Forêt de la Selva del Camp (9) ⚠️ | la Selva del Camp › Baix Camp | 2 |
| Forêt de la Selva del Camp (26) ⚠️ | la Selva del Camp › Baix Camp | 2 |
| Forêt de la Selva del Camp (43) ⚠️ | la Selva del Camp › Baix Camp | 2 |
| Forêt de Alcover (8) ⚠️ | Alcover › Alt Camp | 2 |
| Bois de Alcover (9) ⚠️ | Alcover › Alt Camp | 2 |
| Bois de Alcover (14) ⚠️ | Alcover › Alt Camp | 2 |
| Bois de Alcover (15) ⚠️ | Alcover › Alt Camp | 2 |
| Bois de el Vendrell (11) ⚠️ | el Vendrell › Baix Penedès | 2 |
| Bois de Vimbodí i Poblet (2) ⚠️ | Vimbodí i Poblet › Conca de Barberà | 2 |
| Forêt de Reus (31) ⚠️ | Riudoms › Baix Camp | 2 |
| Forêt de Cornudella de Montsant (94) ⚠️ | Cornudella de Montsant › Priorat | 2 |
| Forêt de Cornudella de Montsant (104) ⚠️ | Cornudella de Montsant › Priorat | 2 |
| Forêt de Cornudella de Montsant (105) ⚠️ | Cornudella de Montsant › Priorat | 2 |
| Forêt de Cornudella de Montsant (111) ⚠️ | Cornudella de Montsant › Priorat | 2 |
| Forêt de Cornudella de Montsant (114) ⚠️ | Cornudella de Montsant › Priorat | 2 |
| Forêt de Cornudella de Montsant (117) ⚠️ | Cornudella de Montsant › Priorat | 2 |
| Forêt de Cornudella de Montsant (121) ⚠️ | Cornudella de Montsant › Priorat | 2 |
| Forêt de la Torre de Fontaubella (3) ⚠️ | Colldejou › Baix Camp | 2 |
| Forêt de Colldejou (8) ⚠️ | Colldejou › Baix Camp | 2 |
| Forêt de Colldejou (17) ⚠️ | Colldejou › Baix Camp | 2 |
| Bois de Batea ⚠️ | Batea › Terra Alta | 2 |
| Bois de Batea (2) ⚠️ | Batea › Terra Alta | 2 |
| Bois de Batea (7) ⚠️ | Batea › Terra Alta | 2 |
| Bois de Batea (8) ⚠️ | Batea › Terra Alta | 2 |
| Forêt de la Selva del Camp (56) ⚠️ | la Selva del Camp › Baix Camp | 2 |
| Forêt de Arnes (18) ⚠️ | Arnes › Terra Alta | 2 |
| Forêt de Cornudella de Montsant (151) ⚠️ | Cornudella de Montsant › Priorat | 2 |
| Parc de la Fira ⚠️ | Tortosa › Baix Ebre | 2 |
| Platja de la Xiquina ⚠️ | Tortosa › Baix Ebre | 2 |
| Forêt de Tortosa (16) ⚠️ | Tortosa › Baix Ebre | 2 |
| Forêt de Tortosa (26) ⚠️ | Tortosa › Baix Ebre | 2 |
| Forêt de Tortosa (29) ⚠️ | Tortosa › Baix Ebre | 2 |
| Forêt de Tortosa (31) ⚠️ | Tortosa › Baix Ebre | 2 |
| Forêt de l'Aldea (2) ⚠️ | l'Aldea › Baix Ebre | 2 |
| Forêt de Margalef (17) ⚠️ | Margalef › Priorat | 2 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (16) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 2 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (22) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 2 |
| Forêt de Reus (34) ⚠️ | Reus › Baix Camp | 2 |
| Forêt de Roda de Berà (16) ⚠️ | Roda de Berà › Tarragonès | 2 |
| Forêt de el Vendrell (40) ⚠️ | el Vendrell › Baix Penedès | 2 |
| Parc de Creixell (12) ⚠️ | Creixell › Tarragonès | 2 |
| Forêt de Creixell (10) ⚠️ | Creixell › Tarragonès | 2 |
| Forêt de Roda de Berà (20) ⚠️ | Roda de Berà › Tarragonès | 2 |
| Bois de Calafell (170) ⚠️ | Calafell › Baix Penedès | 2 |
| Forêt de el Vendrell (47) ⚠️ | el Vendrell › Baix Penedès | 2 |
| Forêt de Calafell (37) ⚠️ | Calafell › Baix Penedès | 2 |
| Forêt de Cunit (13) ⚠️ | Cunit › Baix Penedès | 2 |
| Forêt de Cunit (15) ⚠️ | Cunit › Baix Penedès | 2 |
| Forêt de la Sénia (21) ⚠️ | la Sénia › Montsià | 2 |
| Forêt de la Sénia (34) ⚠️ | la Sénia › Montsià | 2 |
| Forêt de Roquetes (19) ⚠️ | Roquetes › Baix Ebre | 2 |
| Forêt de l'Ametlla de Mar (194) ⚠️ | l'Ametlla de Mar › Baix Ebre | 2 |
| Forêt de l'Ametlla de Mar (199) ⚠️ | l'Ametlla de Mar › Baix Ebre | 2 |
| Forêt de Mont-roig del Camp (103) ⚠️ | Mont-roig del Camp › Baix Camp | 2 |
| Forêt de Mont-roig del Camp (107) ⚠️ | Mont-roig del Camp › Baix Camp | 2 |
| Forêt de Mont-roig del Camp (109) ⚠️ | Mont-roig del Camp › Baix Camp | 2 |
| Forêt de Mont-roig del Camp (111) ⚠️ | Mont-roig del Camp › Baix Camp | 2 |
| Forêt de Mont-roig del Camp (118) ⚠️ | Mont-roig del Camp › Baix Camp | 2 |
| Forêt de Mont-roig del Camp (119) ⚠️ | Mont-roig del Camp › Baix Camp | 2 |
| Forêt de Salou (31) ⚠️ | Salou › Tarragonès | 2 |
| Forêt de Salou (35) ⚠️ | Salou › Tarragonès | 2 |
| Forêt de Salou (39) ⚠️ | Salou › Tarragonès | 2 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (44) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 2 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (48) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 2 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (53) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 2 |
| Forêt de l'Ametlla de Mar (201) ⚠️ | l'Ametlla de Mar › Baix Ebre | 2 |
| Forêt de l'Ametlla de Mar (203) ⚠️ | l'Ametlla de Mar › Baix Ebre | 2 |
| Forêt de la Riera de Gaià (4) ⚠️ | la Riera de Gaià › Tarragonès | 2 |
| Forêt de Vila-seca (3) ⚠️ | Vila-seca › Tarragonès | 2 |
| Forêt de Sant Jaume d'Enveja ⚠️ | Sant Jaume d'Enveja › Montsià | 2 |
| Forêt de Amposta (4) ⚠️ | Amposta › Montsià | 2 |
| Forêt de Sant Jaume d'Enveja (10) ⚠️ | Sant Jaume d'Enveja › Montsià | 2 |
| Forêt de Amposta (6) ⚠️ | Amposta › Montsià | 2 |
| Forêt de l'Ampolla (2) ⚠️ | l'Ampolla › Baix Ebre | 2 |
| Forêt de el Perelló (16) ⚠️ | el Perelló › Baix Ebre | 2 |
| Forêt de el Perelló (17) ⚠️ | el Perelló › Baix Ebre | 2 |
| Forêt de l'Ametlla de Mar (219) ⚠️ | l'Ametlla de Mar › Baix Ebre | 2 |
| Forêt de Alcanar (8) ⚠️ | Alcanar › Montsià | 2 |
| Forêt de Alcanar (21) ⚠️ | Alcanar › Montsià | 2 |
| Forêt de Alcanar (25) ⚠️ | Alcanar › Montsià | 2 |
| Forêt de Mont-roig del Camp (131) ⚠️ | Mont-roig del Camp › Baix Camp | 2 |
| Forêt de Mont-roig del Camp (132) ⚠️ | Mont-roig del Camp › Baix Camp | 2 |
| Forêt de Calafell (51) ⚠️ | Calafell › Baix Penedès | 2 |
| Forêt de Cunit (20) ⚠️ | Cunit › Baix Penedès | 2 |
| Forêt de Cunit (21) ⚠️ | Cunit › Baix Penedès | 2 |
| Forêt de Cunit (23) ⚠️ | Cunit › Baix Penedès | 2 |
| Forêt de Alcover (23) ⚠️ | Alcover › Alt Camp | 2 |
| Forêt de Ulldemolins (87) ⚠️ | Ulldemolins › Priorat | 2 |
| Forêt de la Morera de Montsant (99) ⚠️ | la Morera de Montsant › Priorat | 2 |
| Forêt de la Morera de Montsant (100) ⚠️ | la Morera de Montsant › Priorat | 2 |
| Forêt de la Morera de Montsant (102) ⚠️ | la Morera de Montsant › Priorat | 2 |
| Forêt de Querol (39) ⚠️ | Querol › Alt Camp | 2 |
| Forêt de Pontils (18) ⚠️ | Pontils › Conca de Barberà | 2 |
| Forêt de la Selva del Camp (65) ⚠️ | la Selva del Camp › Baix Camp | 2 |
| Forêt de el Pont d'Armentera (6) ⚠️ | el Pont d'Armentera › Alt Camp | 2 |
| Forêt de la Pobla de Montornès (4) ⚠️ | la Pobla de Montornès › Tarragonès | 2 |
| Forêt de l'Aldea (6) ⚠️ | l'Aldea › Baix Ebre | 2 |
| Forêt de el Perelló (28) ⚠️ | el Perelló › Baix Ebre | 2 |
| Forêt de el Perelló (30) ⚠️ | el Perelló › Baix Ebre | 2 |
| Illa del Barranc dels Estrets ⚠️ | Tortosa › Baix Ebre | 1 |
| Illa de Riu Gran ⚠️ | Miravet › Ribera d'Ebre | 1 |
| Illa de Sapinya ⚠️ | Amposta › Montsià | 1 |
| Parc dels Aragalls ⚠️ | Vila-seca › Tarragonès | 1 |
| Parc de la Bassa ⚠️ | Alcanar › Montsià | 1 |
| Camp de Mart ⚠️ | Tarragona › Tarragonès | 1 |
| Forêt de la Sénia (3) ⚠️ | la Sénia › Montsià | 1 |
| Forêt de Vilanova de Prades ⚠️ | Vilanova de Prades › Conca de Barberà | 1 |
| Forêt de la Torre de l'Espanyol ⚠️ | la Torre de l'Espanyol › Ribera d'Ebre | 1 |
| Forêt de Batea (2) ⚠️ | Batea › Terra Alta | 1 |
| Forêt de Aiguamúrcia (4) ⚠️ | Aiguamúrcia › Alt Camp | 1 |
| Forêt de Benifallet (3) ⚠️ | Benifallet › Baix Ebre | 1 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (3) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 1 |
| Forêt de la Sénia (9) ⚠️ | la Sénia › Montsià | 1 |
| Forêt de Alfara de Carles (7) ⚠️ | Alfara de Carles › Baix Ebre | 1 |
| Forêt de Vimbodí i Poblet (12) ⚠️ | Vallclara › Conca de Barberà | 1 |
| Forêt de Riba-roja d'Ebre (8) ⚠️ | Riba-roja d'Ebre › Ribera d'Ebre | 1 |
| Bois de l'Espluga de Francolí ⚠️ | l'Espluga de Francolí › Conca de Barberà | 1 |
| Forêt de Margalef (9) ⚠️ | Margalef › Priorat | 1 |
| Forêt de Batea (13) ⚠️ | Batea › Terra Alta | 1 |
| Forêt de Batea (16) ⚠️ | Batea › Terra Alta | 1 |
| Forêt de la Pobla de Massaluca (5) ⚠️ | la Pobla de Massaluca › Terra Alta | 1 |
| Forêt de Vilanova de Prades (5) ⚠️ | Vilanova de Prades › Conca de Barberà | 1 |
| Forêt de la Palma d'Ebre (6) ⚠️ | la Palma d'Ebre › Ribera d'Ebre | 1 |
| Forêt de Ulldemolins (5) ⚠️ | Ulldemolins › Priorat | 1 |
| Bois de Senan (4) ⚠️ | Senan › Conca de Barberà | 1 |
| Forêt de la Pobla de Massaluca (8) ⚠️ | la Pobla de Massaluca › Terra Alta | 1 |
| Forêt de el Perelló (12) ⚠️ | el Perelló › Baix Ebre | 1 |
| Forêt de Pontils (12) ⚠️ | Pontils › Conca de Barberà | 1 |
| Forêt de Santa Coloma de Queralt (13) ⚠️ | Santa Coloma de Queralt › Conca de Barberà | 1 |
| Forêt de Arnes (14) ⚠️ | Arnes › Terra Alta | 1 |
| Forêt de la Sénia (17) ⚠️ | la Sénia › Montsià | 1 |
| Bois de Passanant i Belltall (8) ⚠️ | Passanant i Belltall › Conca de Barberà | 1 |
| Forêt de Flix (32) ⚠️ | Flix › Ribera d'Ebre | 1 |
| Forêt de Flix (34) ⚠️ | Flix › Ribera d'Ebre | 1 |
| Bois de Flix ⚠️ | Flix › Ribera d'Ebre | 1 |
| Parc de Salou (2) ⚠️ | Salou › Tarragonès | 1 |
| Bois de Passanant i Belltall (18) ⚠️ | Passanant i Belltall › Conca de Barberà | 1 |
| Bois de Passanant i Belltall (25) ⚠️ | Passanant i Belltall › Conca de Barberà | 1 |
| Parc Municipal de Salou ⚠️ | Salou › Tarragonès | 1 |
| Parc de Salou (33) ⚠️ | Salou › Tarragonès | 1 |
| Parc de Salou (74) ⚠️ | Salou › Tarragonès | 1 |
| Parc de Salou (88) ⚠️ | Salou › Tarragonès | 1 |
| Parc de Tarragona (5) ⚠️ | Tarragona › Tarragonès | 1 |
| Parc de el Vendrell ⚠️ | el Vendrell › Baix Penedès | 1 |
| Parc del Mil·lenari ⚠️ | Tortosa › Baix Ebre | 1 |
| Bois de Mont-roig del Camp ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Parc del Bon Repòs ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Parc de Cambrils (2) ⚠️ | Cambrils › Baix Camp | 1 |
| Parc de Cambrils (9) ⚠️ | Cambrils › Baix Camp | 1 |
| Parc de Cambrils (14) ⚠️ | Cambrils › Baix Camp | 1 |
| Parc de Cambrils (16) ⚠️ | Cambrils › Baix Camp | 1 |
| Parc de Cambrils (17) ⚠️ | Cambrils › Baix Camp | 1 |
| Parc de Cambrils (18) ⚠️ | Cambrils › Baix Camp | 1 |
| Parc del Pescador ⚠️ | Cambrils › Baix Camp | 1 |
| Forêt de Tarragona (2) ⚠️ | Tarragona › Tarragonès | 1 |
| Forêt de Tarragona (7) ⚠️ | Tarragona › Tarragonès | 1 |
| Forêt de Tarragona (8) ⚠️ | Tarragona › Tarragonès | 1 |
| Parc Municipal ⚠️ | Amposta › Montsià | 1 |
| Parc dels Capellans ⚠️ | Reus › Baix Camp | 1 |
| Parc del Trenet (2) ⚠️ | Reus › Baix Camp | 1 |
| Plaça dels Ganxets ⚠️ | Reus › Baix Camp | 1 |
| Parc de Salou (93) ⚠️ | Salou › Tarragonès | 1 |
| Parc dels Prats ⚠️ | Vila-seca › Tarragonès | 1 |
| Bois de Salou (2) ⚠️ | Salou › Tarragonès | 1 |
| Parc de Vila-seca (3) ⚠️ | Vila-seca › Tarragonès | 1 |
| Parc de Mont-roig del Camp ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Parc d'Amics d'Alforja ⚠️ | Alforja › Baix Camp | 1 |
| Bois de Conesa (4) ⚠️ | Conesa › Conca de Barberà | 1 |
| Forêt de Santa Oliva ⚠️ | Santa Oliva › Baix Penedès | 1 |
| Plaça de Clara Campoamor ⚠️ | Cunit › Baix Penedès | 1 |
| Bois de Camarles ⚠️ | Camarles › Baix Ebre | 1 |
| Forêt de Banyeres del Penedès ⚠️ | Banyeres del Penedès › Baix Penedès | 1 |
| Parc de el Vendrell (7) ⚠️ | el Vendrell › Baix Penedès | 1 |
| Forêt de el Vendrell (4) ⚠️ | el Vendrell › Baix Penedès | 1 |
| Forêt de l'Arboç (3) ⚠️ | l'Arboç › Baix Penedès | 1 |
| Forêt de l'Arboç (5) ⚠️ | l'Arboç › Baix Penedès | 1 |
| Forêt de Banyeres del Penedès (2) ⚠️ | Banyeres del Penedès › Baix Penedès | 1 |
| Parc del Pujolet ⚠️ | Banyeres del Penedès › Baix Penedès | 1 |
| Forêt de Banyeres del Penedès (4) ⚠️ | Banyeres del Penedès › Baix Penedès | 1 |
| Bosc del Castell ⚠️ | Llorenç del Penedès › Baix Penedès | 1 |
| Forêt de l'Arboç (8) ⚠️ | l'Arboç › Baix Penedès | 1 |
| Forêt de l'Arboç (9) ⚠️ | l'Arboç › Baix Penedès | 1 |
| Forêt de Banyeres del Penedès (9) ⚠️ | Banyeres del Penedès › Baix Penedès | 1 |
| Forêt de Bellvei (2) ⚠️ | Bellvei › Baix Penedès | 1 |
| Forêt de Banyeres del Penedès (14) ⚠️ | Banyeres del Penedès › Baix Penedès | 1 |
| Forêt de Banyeres del Penedès (15) ⚠️ | Banyeres del Penedès › Baix Penedès | 1 |
| Forêt de Bellvei (4) ⚠️ | Bellvei › Baix Penedès | 1 |
| Forêt de Banyeres del Penedès (16) ⚠️ | Banyeres del Penedès › Baix Penedès | 1 |
| Forêt de l'Arboç (16) ⚠️ | l'Arboç › Baix Penedès | 1 |
| Forêt de el Vendrell (9) ⚠️ | el Vendrell › Baix Penedès | 1 |
| Forêt de Banyeres del Penedès (18) ⚠️ | Banyeres del Penedès › Baix Penedès | 1 |
| Forêt de el Vendrell (14) ⚠️ | el Vendrell › Baix Penedès | 1 |
| Forêt de el Vendrell (16) ⚠️ | el Vendrell › Baix Penedès | 1 |
| Forêt de el Vendrell (19) ⚠️ | el Vendrell › Baix Penedès | 1 |
| Forêt de Albinyana (4) ⚠️ | Albinyana › Baix Penedès | 1 |
| Forêt de Albinyana (8) ⚠️ | Albinyana › Baix Penedès | 1 |
| Bosc del Mas ⚠️ | Llorenç del Penedès › Baix Penedès | 1 |
| Bosc de Ca l'Oller ⚠️ | Sant Jaume dels Domenys › Baix Penedès | 1 |
| Forêt de la Bisbal del Penedès (2) ⚠️ | la Bisbal del Penedès › Baix Penedès | 1 |
| Forêt de el Vendrell (22) ⚠️ | el Vendrell › Baix Penedès | 1 |
| Forêt de Sant Jaume dels Domenys (6) ⚠️ | Sant Jaume dels Domenys › Baix Penedès | 1 |
| Bosc del Mas del Sol ⚠️ | la Bisbal del Penedès › Baix Penedès | 1 |
| Forêt de Sant Jaume dels Domenys (13) ⚠️ | Sant Jaume dels Domenys › Baix Penedès | 1 |
| Bosc de Cal Figueres ⚠️ | Llorenç del Penedès › Baix Penedès | 1 |
| Bosc d'en Romeu ⚠️ | Llorenç del Penedès › Baix Penedès | 1 |
| Parc del Rectoret - Rocaplana ⚠️ | Cunit › Baix Penedès | 1 |
| Forêt de Roda de Berà ⚠️ | Roda de Berà › Tarragonès | 1 |
| Forêt de Sant Jaume dels Domenys (15) ⚠️ | Sant Jaume dels Domenys › Baix Penedès | 1 |
| Parc de la Sínia ⚠️ | Calafell › Baix Penedès | 1 |
| Bois de Conesa (17) ⚠️ | Conesa › Conca de Barberà | 1 |
| Bois de Conesa (20) ⚠️ | Conesa › Conca de Barberà | 1 |
| La Foia ⚠️ | Cabacés › Priorat | 1 |
| Parc de Sant Antoni ⚠️ | Riudoms › Baix Camp | 1 |
| Forêt de la Secuita ⚠️ | la Secuita › Tarragonès | 1 |
| Forêt de Mont-roig del Camp ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Parc Arcadia ⚠️ | Cambrils › Baix Camp | 1 |
| Bois de Passanant i Belltall (51) ⚠️ | Passanant i Belltall › Conca de Barberà | 1 |
| Forêt de Cornudella de Montsant (6) ⚠️ | la Morera de Montsant › Priorat | 1 |
| Forêt de Ulldemolins (12) ⚠️ | Ulldemolins › Priorat | 1 |
| Forêt de Ulldemolins (13) ⚠️ | Ulldemolins › Priorat | 1 |
| Forêt de la Morera de Montsant (11) ⚠️ | la Morera de Montsant › Priorat | 1 |
| Forêt de la Morera de Montsant (12) ⚠️ | la Morera de Montsant › Priorat | 1 |
| Bois de Passanant i Belltall (57) ⚠️ | Passanant i Belltall › Conca de Barberà | 1 |
| Forêt de la Morera de Montsant (15) ⚠️ | la Morera de Montsant › Priorat | 1 |
| Forêt de la Morera de Montsant (19) ⚠️ | la Morera de Montsant › Priorat | 1 |
| Forêt de Montblanc (8) ⚠️ | Montblanc › Conca de Barberà | 1 |
| Parc de Cambrils (26) ⚠️ | Cambrils › Baix Camp | 1 |
| Àrea recreativa de la bassa de l'ermita ⚠️ | Ulldecona › Montsià | 1 |
| Plaça d'Antoni Correig i Massó ⚠️ | Reus › Baix Camp | 1 |
| Forêt de Santa Oliva (6) ⚠️ | Santa Oliva › Baix Penedès | 1 |
| Forêt de Albinyana (10) ⚠️ | Albinyana › Baix Penedès | 1 |
| Forêt de Albinyana (11) ⚠️ | Albinyana › Baix Penedès | 1 |
| el Calvari ⚠️ | Batea › Terra Alta | 1 |
| Bois de Passanant i Belltall (58) ⚠️ | Passanant i Belltall › Conca de Barberà | 1 |
| Forêt de Bonastre (2) ⚠️ | Bonastre › Baix Penedès | 1 |
| Forêt de Bonastre (4) ⚠️ | Bonastre › Baix Penedès | 1 |
| Bois de Montblanc (6) ⚠️ | Montblanc › Conca de Barberà | 1 |
| Bois de Montblanc (7) ⚠️ | Montblanc › Conca de Barberà | 1 |
| Bois de Montblanc (8) ⚠️ | Montblanc › Conca de Barberà | 1 |
| Bois de Montblanc (9) ⚠️ | Montblanc › Conca de Barberà | 1 |
| Bois de Montblanc (15) ⚠️ | Montblanc › Conca de Barberà | 1 |
| Jardins del Príncep ⚠️ | Tortosa › Baix Ebre | 1 |
| Forêt de el Montmell (9) ⚠️ | el Montmell › Baix Penedès | 1 |
| Forêt de Tarragona (17) ⚠️ | Tarragona › Tarragonès | 1 |
| Bois de Calafell ⚠️ | Calafell › Baix Penedès | 1 |
| Forêt de Calafell (9) ⚠️ | Calafell › Baix Penedès | 1 |
| Forêt de Montblanc (10) ⚠️ | Montblanc › Conca de Barberà | 1 |
| Forêt de el Vendrell (27) ⚠️ | el Vendrell › Baix Penedès | 1 |
| Bois de Passanant i Belltall (59) ⚠️ | Passanant i Belltall › Conca de Barberà | 1 |
| Plaça de Tirant lo Blanc ⚠️ | Reus › Baix Camp | 1 |
| Forêt de la Bisbal del Penedès (7) ⚠️ | la Bisbal del Penedès › Baix Penedès | 1 |
| Bois de Passanant i Belltall (63) ⚠️ | Conesa › Conca de Barberà | 1 |
| Forêt de Querol (12) ⚠️ | Querol › Alt Camp | 1 |
| Forêt de el Pla de Santa Maria (2) ⚠️ | el Pla de Santa Maria › Alt Camp | 1 |
| Forêt de el Pla de Santa Maria (5) ⚠️ | el Pla de Santa Maria › Alt Camp | 1 |
| Forêt de el Pla de Santa Maria (6) ⚠️ | el Pla de Santa Maria › Alt Camp | 1 |
| Forêt de el Pla de Santa Maria (7) ⚠️ | el Pla de Santa Maria › Alt Camp | 1 |
| Forêt de Aiguamúrcia (22) ⚠️ | Aiguamúrcia › Alt Camp | 1 |
| Forêt de Querol (13) ⚠️ | Querol › Alt Camp | 1 |
| Parc de Salou (186) ⚠️ | Salou › Tarragonès | 1 |
| Forêt de Salou (8) ⚠️ | Salou › Tarragonès | 1 |
| Parc de la Febró ⚠️ | la Febró › Baix Camp | 1 |
| Forêt de Aiguamúrcia (23) ⚠️ | Aiguamúrcia › Alt Camp | 1 |
| Forêt de Valls ⚠️ | Valls › Alt Camp | 1 |
| Forêt de Valls (2) ⚠️ | Valls › Alt Camp | 1 |
| Forêt de Valls (3) ⚠️ | Valls › Alt Camp | 1 |
| Forêt de Mont-roig del Camp (5) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (11) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Parc de Salou (204) ⚠️ | Salou › Tarragonès | 1 |
| Forêt de Vilanova d'Escornalbou ⚠️ | Vilanova d'Escornalbou › Baix Camp | 1 |
| Forêt de Cambrils (4) ⚠️ | Cambrils › Baix Camp | 1 |
| Parc de Reus (26) ⚠️ | Reus › Baix Camp | 1 |
| Forêt de Tivenys (2) ⚠️ | Xerta › Baix Ebre | 1 |
| Illa de Benifallet ⚠️ | Benifallet › Baix Ebre | 1 |
| Forêt de Garcia (7) ⚠️ | Garcia › Ribera d'Ebre | 1 |
| Forêt de Garcia (8) ⚠️ | Garcia › Ribera d'Ebre | 1 |
| Illa de Caloi ⚠️ | Riba-roja d'Ebre › Ribera d'Ebre | 1 |
| Illa de Maurício ⚠️ | Flix › Ribera d'Ebre | 1 |
| Parc de Salou (212) ⚠️ | Salou › Tarragonès | 1 |
| Parc de Salou (219) ⚠️ | Salou › Tarragonès | 1 |
| Parc de Tarragona (23) ⚠️ | Tarragona › Tarragonès | 1 |
| Forêt de el Pla de Santa Maria (10) ⚠️ | el Pla de Santa Maria › Alt Camp | 1 |
| Forêt de el Pla de Santa Maria (14) ⚠️ | el Pla de Santa Maria › Alt Camp | 1 |
| Forêt de el Pla de Santa Maria (29) ⚠️ | el Pla de Santa Maria › Alt Camp | 1 |
| Parc de el Vendrell (23) ⚠️ | el Vendrell › Baix Penedès | 1 |
| Forêt de Cambrils (6) ⚠️ | Cambrils › Baix Camp | 1 |
| Forêt de Cambrils (7) ⚠️ | Cambrils › Baix Camp | 1 |
| Bois de Passanant i Belltall (65) ⚠️ | Passanant i Belltall › Conca de Barberà | 1 |
| Parc de Reus (29) ⚠️ | Reus › Baix Camp | 1 |
| Parc de el Perelló (3) ⚠️ | el Perelló › Baix Ebre | 1 |
| Parc de Vinyols i els Arcs (5) ⚠️ | Vinyols i els Arcs › Baix Camp | 1 |
| Parc Albert Via ⚠️ | Reus › Baix Camp | 1 |
| Parc de Creixell (4) ⚠️ | Creixell › Tarragonès | 1 |
| Parc de Vila-seca (7) ⚠️ | Vila-seca › Tarragonès | 1 |
| Parc Barrau ⚠️ | Valls › Alt Camp | 1 |
| Bois de Alió ⚠️ | Alió › Alt Camp | 1 |
| Bois de Vandellòs i l'Hospitalet de l'Infant ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 1 |
| Parc de Vila-seca (15) ⚠️ | Vila-seca › Tarragonès | 1 |
| Parc de Vila-seca (17) ⚠️ | Vila-seca › Tarragonès | 1 |
| Parc de L'Aubareda ⚠️ | Almoster › Baix Camp | 1 |
| Bois de Mont-roig del Camp (3) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Parc de Calafell (2) ⚠️ | Calafell › Baix Penedès | 1 |
| Parc de Amposta (2) ⚠️ | Amposta › Montsià | 1 |
| Parc del Fortí ⚠️ | Tarragona › Tarragonès | 1 |
| Parc de Tortosa (13) ⚠️ | Tortosa › Baix Ebre | 1 |
| Parc Països Catalans ⚠️ | Tortosa › Baix Ebre | 1 |
| Hort de Cruells ⚠️ | Roquetes › Baix Ebre | 1 |
| Parc de Tarragona (27) ⚠️ | Tarragona › Tarragonès | 1 |
| Parc de les Quintanes ⚠️ | Amposta › Montsià | 1 |
| Parc de la Pobla de Montornès (2) ⚠️ | la Pobla de Montornès › Tarragonès | 1 |
| Parc de la Pobla de Montornès (3) ⚠️ | la Pobla de Montornès › Tarragonès | 1 |
| Parc de la Pobla de Montornès (4) ⚠️ | la Pobla de Montornès › Tarragonès | 1 |
| Parc de la Pobla de Montornès (5) ⚠️ | la Pobla de Montornès › Tarragonès | 1 |
| Parc de la Pobla de Montornès (6) ⚠️ | la Pobla de Montornès › Tarragonès | 1 |
| Parc Infantil Els Masos ⚠️ | el Vendrell › Baix Penedès | 1 |
| Parc de Tarragona (28) ⚠️ | Tarragona › Tarragonès | 1 |
| Forêt de l'Ametlla de Mar (4) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (6) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (7) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (11) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (12) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (14) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (15) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (24) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (28) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (31) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (36) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (51) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (56) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (61) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (64) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (75) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (77) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (81) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (84) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (85) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (87) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (95) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (96) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (106) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (109) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (117) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (118) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (124) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (125) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (126) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (141) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (143) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (145) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (146) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (147) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (157) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (158) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (163) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (168) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (169) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (171) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (175) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (177) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (180) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (181) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (184) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (185) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Bois de la Bisbal del Penedès ⚠️ | la Bisbal del Penedès › Baix Penedès | 1 |
| Parc de la Pobla de Montornès (11) ⚠️ | la Pobla de Montornès › Tarragonès | 1 |
| Bois de Torroja del Priorat (2) ⚠️ | Torroja del Priorat › Priorat | 1 |
| Bois de Tarragona (3) ⚠️ | Tarragona › Tarragonès | 1 |
| Jardins Antoni Gaudí ⚠️ | Albinyana › Baix Penedès | 1 |
| Jardins de la vinya ⚠️ | Albinyana › Baix Penedès | 1 |
| Parc de Mont-roig del Camp (5) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Parc de Salou (241) ⚠️ | Salou › Tarragonès | 1 |
| Bois de el Catllar ⚠️ | el Catllar › Tarragonès | 1 |
| Bois de el Catllar (2) ⚠️ | el Catllar › Tarragonès | 1 |
| Bois de el Catllar (3) ⚠️ | el Catllar › Tarragonès | 1 |
| Parc Mercé Rodoreda ⚠️ | Roda de Berà › Tarragonès | 1 |
| Parc urbà (2) ⚠️ | Roda de Berà › Tarragonès | 1 |
| Plaça Major de Campclar ⚠️ | Tarragona › Tarragonès | 1 |
| Plaça de la Salut ⚠️ | Tarragona › Tarragonès | 1 |
| Rambla del Ball de Bastons ⚠️ | l'Arboç › Baix Penedès | 1 |
| Bois de Banyeres del Penedès (2) ⚠️ | Banyeres del Penedès › Baix Penedès | 1 |
| Bois de Banyeres del Penedès (5) ⚠️ | Banyeres del Penedès › Baix Penedès | 1 |
| Forêt de Banyeres del Penedès (23) ⚠️ | Banyeres del Penedès › Baix Penedès | 1 |
| Parc de Tarragona (37) ⚠️ | Tarragona › Tarragonès | 1 |
| Parc de Llorenç del Penedès (4) ⚠️ | Llorenç del Penedès › Baix Penedès | 1 |
| Parc de la Passarela ⚠️ | Llorenç del Penedès › Baix Penedès | 1 |
| Forêt de Valls (8) ⚠️ | Valls › Alt Camp | 1 |
| Parc Infantil (2) ⚠️ | Perafort › Tarragonès | 1 |
| Parc de el Vendrell (38) ⚠️ | el Vendrell › Baix Penedès | 1 |
| Bosc de Brunet ⚠️ | la Secuita › Tarragonès | 1 |
| Bosc del Ferrer ⚠️ | la Secuita › Tarragonès | 1 |
| Bosc del Sastre ⚠️ | la Secuita › Tarragonès | 1 |
| Bosc de Requesents ⚠️ | Nulles › Alt Camp | 1 |
| Bois de la Secuita (2) ⚠️ | la Secuita › Tarragonès | 1 |
| Bois de la Secuita (4) ⚠️ | la Secuita › Tarragonès | 1 |
| Bois de la Secuita (6) ⚠️ | la Secuita › Tarragonès | 1 |
| Bois de la Secuita (7) ⚠️ | la Secuita › Tarragonès | 1 |
| Bois de la Secuita (8) ⚠️ | la Secuita › Tarragonès | 1 |
| Bois de la Secuita (10) ⚠️ | la Secuita › Tarragonès | 1 |
| Bois de el Catllar (4) ⚠️ | el Catllar › Tarragonès | 1 |
| Bois de el Catllar (6) ⚠️ | el Catllar › Tarragonès | 1 |
| Bois de el Catllar (8) ⚠️ | el Catllar › Tarragonès | 1 |
| Bois de el Catllar (12) ⚠️ | el Catllar › Tarragonès | 1 |
| Bois de la Secuita (11) ⚠️ | la Secuita › Tarragonès | 1 |
| Bois de el Catllar (16) ⚠️ | el Catllar › Tarragonès | 1 |
| Bois de els Pallaresos (4) ⚠️ | els Pallaresos › Tarragonès | 1 |
| Bois de els Pallaresos (5) ⚠️ | els Pallaresos › Tarragonès | 1 |
| Bois de el Catllar (18) ⚠️ | el Catllar › Tarragonès | 1 |
| Bois de el Catllar (22) ⚠️ | el Catllar › Tarragonès | 1 |
| Bois de la Secuita (16) ⚠️ | la Secuita › Tarragonès | 1 |
| Bois de la Secuita (17) ⚠️ | la Secuita › Tarragonès | 1 |
| Bois de la Secuita (18) ⚠️ | la Secuita › Tarragonès | 1 |
| Bois de la Secuita (20) ⚠️ | la Secuita › Tarragonès | 1 |
| Parc de Cambrils (43) ⚠️ | Cambrils › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (15) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (16) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (20) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Bois de Horta de Sant Joan ⚠️ | Horta de Sant Joan › Terra Alta | 1 |
| Bois de Horta de Sant Joan (6) ⚠️ | Horta de Sant Joan › Terra Alta | 1 |
| Parc de Altafulla (2) ⚠️ | Altafulla › Tarragonès | 1 |
| Forêt de Roda de Berà (2) ⚠️ | Roda de Berà › Tarragonès | 1 |
| Forêt de el Vendrell (31) ⚠️ | el Vendrell › Baix Penedès | 1 |
| Forêt de Alió ⚠️ | Alió › Alt Camp | 1 |
| Forêt de Puigpelat (2) ⚠️ | Puigpelat › Alt Camp | 1 |
| Bois de el Catllar (28) ⚠️ | el Catllar › Tarragonès | 1 |
| Bois de el Catllar (30) ⚠️ | el Catllar › Tarragonès | 1 |
| Bois de Valls (3) ⚠️ | Valls › Alt Camp | 1 |
| Bois de Bràfim ⚠️ | Bràfim › Alt Camp | 1 |
| Bois de Bràfim (2) ⚠️ | Bràfim › Alt Camp | 1 |
| Bois de Bràfim (3) ⚠️ | Bràfim › Alt Camp | 1 |
| Forêt de la Ràpita (2) ⚠️ | la Ràpita › Montsià | 1 |
| Parc de Tarragona (41) ⚠️ | Tarragona › Tarragonès | 1 |
| Forêt de Tarragona (19) ⚠️ | Tarragona › Tarragonès | 1 |
| Forêt de Tarragona (31) ⚠️ | Tarragona › Tarragonès | 1 |
| Forêt de Tarragona (32) ⚠️ | Tarragona › Tarragonès | 1 |
| Parc de Roda de Berà (17) ⚠️ | Roda de Berà › Tarragonès | 1 |
| Forêt de Reus (6) ⚠️ | Reus › Baix Camp | 1 |
| Bois de Santa Coloma de Queralt (6) ⚠️ | Santa Coloma de Queralt › Conca de Barberà | 1 |
| Bois de Santa Coloma de Queralt (7) ⚠️ | Santa Coloma de Queralt › Conca de Barberà | 1 |
| Bois de Santa Coloma de Queralt (9) ⚠️ | Santa Coloma de Queralt › Conca de Barberà | 1 |
| Bois de Reus (5) ⚠️ | Reus › Baix Camp | 1 |
| Forêt de Cornudella de Montsant (19) ⚠️ | Cornudella de Montsant › Priorat | 1 |
| Forêt de Montbrió del Camp (3) ⚠️ | Montbrió del Camp › Baix Camp | 1 |
| Forêt de Montbrió del Camp (5) ⚠️ | Montbrió del Camp › Baix Camp | 1 |
| Forêt de Montbrió del Camp (9) ⚠️ | Montbrió del Camp › Baix Camp | 1 |
| Forêt de Mont-ral (7) ⚠️ | Mont-ral › Alt Camp | 1 |
| Forêt de Mont-ral (8) ⚠️ | Mont-ral › Alt Camp | 1 |
| Forêt de Cornudella de Montsant (21) ⚠️ | Cornudella de Montsant › Priorat | 1 |
| Forêt de Cornudella de Montsant (22) ⚠️ | Cornudella de Montsant › Priorat | 1 |
| Forêt de l'Argentera (2) ⚠️ | l'Argentera › Baix Camp | 1 |
| Forêt de Riudecanyes (5) ⚠️ | Riudecanyes › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (23) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de l'Argentera (4) ⚠️ | l'Argentera › Baix Camp | 1 |
| Forêt de l'Argentera (5) ⚠️ | l'Argentera › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (30) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Parc de Torredembarra (7) ⚠️ | Torredembarra › Tarragonès | 1 |
| Parc Mas Miquel ⚠️ | Valls › Alt Camp | 1 |
| Bois de Miravet (2) ⚠️ | Miravet › Ribera d'Ebre | 1 |
| Bois de Arnes (3) ⚠️ | Arnes › Terra Alta | 1 |
| Bois de Santa Coloma de Queralt (12) ⚠️ | Santa Coloma de Queralt › Conca de Barberà | 1 |
| Parc Educació Vial ⚠️ | Roda de Berà › Tarragonès | 1 |
| Forêt de Rasquera (8) ⚠️ | Rasquera › Ribera d'Ebre | 1 |
| Forêt de Rasquera (9) ⚠️ | Rasquera › Ribera d'Ebre | 1 |
| Forêt de Rasquera (10) ⚠️ | Rasquera › Ribera d'Ebre | 1 |
| Parc la Fàbrica ⚠️ | el Pla de Santa Maria › Alt Camp | 1 |
| Bosc de l'Avi ⚠️ | Valls › Alt Camp | 1 |
| Bois de el Pla de Santa Maria (4) ⚠️ | el Pla de Santa Maria › Alt Camp | 1 |
| Bois de el Pla de Santa Maria (8) ⚠️ | el Pla de Santa Maria › Alt Camp | 1 |
| Bois de el Pla de Santa Maria (9) ⚠️ | el Pla de Santa Maria › Alt Camp | 1 |
| Forêt de Querol (15) ⚠️ | Querol › Alt Camp | 1 |
| Parc de Reus (48) ⚠️ | Reus › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (32) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Tarragona (47) ⚠️ | Tarragona › Tarragonès | 1 |
| Parc de la Ràpita (10) ⚠️ | la Ràpita › Montsià | 1 |
| Forêt de l'Aleixar (3) ⚠️ | l'Aleixar › Baix Camp | 1 |
| Forêt de l'Albiol (6) ⚠️ | l'Albiol › Baix Camp | 1 |
| Parc de Cunit (9) ⚠️ | Cunit › Baix Penedès | 1 |
| Forêt de Calafell (15) ⚠️ | Calafell › Baix Penedès | 1 |
| Forêt de Calafell (18) ⚠️ | Calafell › Baix Penedès | 1 |
| Forêt de Bràfim ⚠️ | Bràfim › Alt Camp | 1 |
| Forêt de Bràfim (3) ⚠️ | Bràfim › Alt Camp | 1 |
| Forêt de Puigpelat (4) ⚠️ | Puigpelat › Alt Camp | 1 |
| Parc de Salou (246) ⚠️ | Salou › Tarragonès | 1 |
| Forêt de Albinyana (12) ⚠️ | Albinyana › Baix Penedès | 1 |
| Parc de les Parades ⚠️ | Vilallonga del Camp › Tarragonès | 1 |
| Bois de el Vendrell (3) ⚠️ | el Vendrell › Baix Penedès | 1 |
| Jardí del Castell ⚠️ | Vila-seca › Tarragonès | 1 |
| Forêt de Amposta (2) ⚠️ | Amposta › Montsià | 1 |
| Forêt de Falset (15) ⚠️ | Falset › Priorat | 1 |
| Forêt de Falset (16) ⚠️ | Falset › Priorat | 1 |
| Forêt de Capafonts (9) ⚠️ | Capafonts › Baix Camp | 1 |
| Forêt de Capafonts (10) ⚠️ | Capafonts › Baix Camp | 1 |
| Forêt de Bonastre (7) ⚠️ | Bonastre › Baix Penedès | 1 |
| Forêt de Bonastre (8) ⚠️ | Bonastre › Baix Penedès | 1 |
| Forêt de Altafulla ⚠️ | Altafulla › Tarragonès | 1 |
| Forêt de Vilanova d'Escornalbou (9) ⚠️ | Vilanova d'Escornalbou › Baix Camp | 1 |
| Forêt de Vilanova d'Escornalbou (15) ⚠️ | Vilanova d'Escornalbou › Baix Camp | 1 |
| Forêt de Riudecanyes (7) ⚠️ | Riudecanyes › Baix Camp | 1 |
| Forêt de Vilanova d'Escornalbou (23) ⚠️ | Vilanova d'Escornalbou › Baix Camp | 1 |
| Forêt de Vilanova d'Escornalbou (24) ⚠️ | Vilanova d'Escornalbou › Baix Camp | 1 |
| Forêt de Vilanova d'Escornalbou (26) ⚠️ | Vilanova d'Escornalbou › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (38) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (42) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (46) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (49) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (51) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (54) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (56) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (68) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Pratdip (8) ⚠️ | Pratdip › Baix Camp | 1 |
| Forêt de Pratdip (9) ⚠️ | Pratdip › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (76) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (80) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (82) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Pratdip (14) ⚠️ | Pratdip › Baix Camp | 1 |
| Forêt de Pratdip (19) ⚠️ | Pratdip › Baix Camp | 1 |
| Forêt de Pratdip (23) ⚠️ | Pratdip › Baix Camp | 1 |
| Forêt de Pratdip (26) ⚠️ | Pratdip › Baix Camp | 1 |
| Forêt de Pratdip (27) ⚠️ | Pratdip › Baix Camp | 1 |
| Forêt de Pratdip (34) ⚠️ | Pratdip › Baix Camp | 1 |
| Forêt de Pratdip (35) ⚠️ | Pratdip › Baix Camp | 1 |
| Forêt de Pratdip (36) ⚠️ | Pratdip › Baix Camp | 1 |
| Forêt de Pratdip (40) ⚠️ | Pratdip › Baix Camp | 1 |
| Forêt de Pratdip (41) ⚠️ | Pratdip › Baix Camp | 1 |
| Forêt de Cornudella de Montsant (30) ⚠️ | Cornudella de Montsant › Priorat | 1 |
| Forêt de Cornudella de Montsant (50) ⚠️ | Cornudella de Montsant › Priorat | 1 |
| Forêt de Cornudella de Montsant (56) ⚠️ | Cornudella de Montsant › Priorat | 1 |
| Forêt de Cornudella de Montsant (61) ⚠️ | Cornudella de Montsant › Priorat | 1 |
| Forêt de Cornudella de Montsant (62) ⚠️ | Cornudella de Montsant › Priorat | 1 |
| Forêt de Cornudella de Montsant (64) ⚠️ | Cornudella de Montsant › Priorat | 1 |
| Forêt de Roda de Berà (3) ⚠️ | Roda de Berà › Tarragonès | 1 |
| Forêt de Ulldemolins (24) ⚠️ | Ulldemolins › Priorat | 1 |
| Forêt de Ulldemolins (29) ⚠️ | Ulldemolins › Priorat | 1 |
| Forêt de Ulldemolins (32) ⚠️ | Ulldemolins › Priorat | 1 |
| Forêt de Ulldemolins (43) ⚠️ | Ulldemolins › Priorat | 1 |
| Forêt de Ulldemolins (47) ⚠️ | Ulldemolins › Priorat | 1 |
| Forêt de Ulldemolins (57) ⚠️ | Ulldemolins › Priorat | 1 |
| Forêt de Ulldemolins (59) ⚠️ | Ulldemolins › Priorat | 1 |
| Forêt de Ulldemolins (74) ⚠️ | Ulldemolins › Priorat | 1 |
| Forêt de Ulldemolins (77) ⚠️ | Ulldemolins › Priorat | 1 |
| Forêt de la Bisbal del Penedès (17) ⚠️ | la Bisbal del Penedès › Baix Penedès | 1 |
| Bois de Bonastre (3) ⚠️ | Bonastre › Baix Penedès | 1 |
| Parc de Cambrils (46) ⚠️ | Cambrils › Baix Camp | 1 |
| Forêt de Cornudella de Montsant (67) ⚠️ | Cornudella de Montsant › Priorat | 1 |
| Forêt de Cornudella de Montsant (69) ⚠️ | Cornudella de Montsant › Priorat | 1 |
| Forêt de Cornudella de Montsant (76) ⚠️ | Cornudella de Montsant › Priorat | 1 |
| Bois de Bonastre (5) ⚠️ | Bonastre › Baix Penedès | 1 |
| Forêt de Cornudella de Montsant (78) ⚠️ | Cornudella de Montsant › Priorat | 1 |
| Forêt de la Morera de Montsant (28) ⚠️ | la Morera de Montsant › Priorat | 1 |
| Forêt de la Morera de Montsant (39) ⚠️ | la Morera de Montsant › Priorat | 1 |
| Forêt de la Morera de Montsant (45) ⚠️ | la Morera de Montsant › Priorat | 1 |
| Forêt de la Morera de Montsant (57) ⚠️ | la Morera de Montsant › Priorat | 1 |
| Bois de el Vendrell (7) ⚠️ | el Vendrell › Baix Penedès | 1 |
| Forêt de la Morera de Montsant (83) ⚠️ | la Morera de Montsant › Priorat | 1 |
| Bois de Calafell (3) ⚠️ | Calafell › Baix Penedès | 1 |
| Parc de Reus (51) ⚠️ | Reus › Baix Camp | 1 |
| Parc de Reus (55) ⚠️ | Reus › Baix Camp | 1 |
| Bois de Calafell (32) ⚠️ | Calafell › Baix Penedès | 1 |
| Parc de Reus (61) ⚠️ | Reus › Baix Camp | 1 |
| Forêt de Calafell (20) ⚠️ | Calafell › Baix Penedès | 1 |
| Bois de la Figuera ⚠️ | la Figuera › Priorat | 1 |
| Forêt de Querol (19) ⚠️ | Querol › Alt Camp | 1 |
| Parc de Reus (68) ⚠️ | Reus › Baix Camp | 1 |
| Forêt de la Vilella Baixa (2) ⚠️ | la Vilella Baixa › Priorat | 1 |
| Forêt de Reus (11) ⚠️ | Reus › Baix Camp | 1 |
| Parc de Albinyana (4) ⚠️ | Albinyana › Baix Penedès | 1 |
| Plaça del President Companys ⚠️ | Valls › Alt Camp | 1 |
| Bois de la Figuera (3) ⚠️ | la Figuera › Priorat | 1 |
| Forêt de Prades (18) ⚠️ | Prades › Baix Camp | 1 |
| Forêt de Prades (19) ⚠️ | Prades › Baix Camp | 1 |
| Forêt de Prades (21) ⚠️ | Prades › Baix Camp | 1 |
| Forêt de Prades (26) ⚠️ | Prades › Baix Camp | 1 |
| Forêt de Capafonts (21) ⚠️ | Capafonts › Baix Camp | 1 |
| Forêt de Prades (33) ⚠️ | Prades › Baix Camp | 1 |
| Forêt de Prades (34) ⚠️ | Prades › Baix Camp | 1 |
| Forêt de Prades (38) ⚠️ | Prades › Baix Camp | 1 |
| Forêt de Prades (42) ⚠️ | Prades › Baix Camp | 1 |
| Forêt de Prades (43) ⚠️ | Prades › Baix Camp | 1 |
| Forêt de Prades (47) ⚠️ | Prades › Baix Camp | 1 |
| Forêt de Prades (48) ⚠️ | Prades › Baix Camp | 1 |
| Forêt de Capafonts (29) ⚠️ | Capafonts › Baix Camp | 1 |
| Forêt de Capafonts (33) ⚠️ | Capafonts › Baix Camp | 1 |
| Forêt de Capafonts (34) ⚠️ | Capafonts › Baix Camp | 1 |
| Forêt de Capafonts (38) ⚠️ | Capafonts › Baix Camp | 1 |
| Forêt de Santa Coloma de Queralt (20) ⚠️ | Santa Coloma de Queralt › Conca de Barberà | 1 |
| Forêt de Santa Coloma de Queralt (21) ⚠️ | Santa Coloma de Queralt › Conca de Barberà | 1 |
| Forêt de Santa Coloma de Queralt (23) ⚠️ | Santa Coloma de Queralt › Conca de Barberà | 1 |
| Forêt de Santa Coloma de Queralt (24) ⚠️ | Santa Coloma de Queralt › Conca de Barberà | 1 |
| Forêt de Santa Coloma de Queralt (25) ⚠️ | Santa Coloma de Queralt › Conca de Barberà | 1 |
| Forêt de Santa Coloma de Queralt (26) ⚠️ | Santa Coloma de Queralt › Conca de Barberà | 1 |
| Forêt de Santa Coloma de Queralt (27) ⚠️ | Santa Coloma de Queralt › Conca de Barberà | 1 |
| Forêt de Santa Coloma de Queralt (33) ⚠️ | Santa Coloma de Queralt › Conca de Barberà | 1 |
| Forêt de Llorac (12) ⚠️ | Llorac › Conca de Barberà | 1 |
| Forêt de Llorac (13) ⚠️ | Llorac › Conca de Barberà | 1 |
| Parc de la Família ⚠️ | Reus › Baix Camp | 1 |
| Forêt de Reus (17) ⚠️ | Reus › Baix Camp | 1 |
| Forêt de Reus (18) ⚠️ | Reus › Baix Camp | 1 |
| Forêt de Reus (20) ⚠️ | Reus › Baix Camp | 1 |
| Bois de Valls (8) ⚠️ | Valls › Alt Camp | 1 |
| Bois de Valls (19) ⚠️ | Valls › Alt Camp | 1 |
| Bois de Valls (24) ⚠️ | Valls › Alt Camp | 1 |
| Bois de Valls (64) ⚠️ | Valls › Alt Camp | 1 |
| Forêt de Santa Coloma de Queralt (43) ⚠️ | Santa Coloma de Queralt › Conca de Barberà | 1 |
| Forêt de Reus (21) ⚠️ | Reus › Baix Camp | 1 |
| Forêt de Roquetes (7) ⚠️ | Roquetes › Baix Ebre | 1 |
| Bois de Valls (81) ⚠️ | Valls › Alt Camp | 1 |
| Parc de Reus (90) ⚠️ | Reus › Baix Camp | 1 |
| Forêt de l'Aleixar (8) ⚠️ | l'Aleixar › Baix Camp | 1 |
| Forêt de l'Aleixar (10) ⚠️ | l'Aleixar › Baix Camp | 1 |
| Forêt de l'Aleixar (11) ⚠️ | l'Aleixar › Baix Camp | 1 |
| Forêt de l'Aleixar (13) ⚠️ | l'Aleixar › Baix Camp | 1 |
| Forêt de l'Aleixar (15) ⚠️ | l'Aleixar › Baix Camp | 1 |
| Forêt de l'Aleixar (17) ⚠️ | l'Aleixar › Baix Camp | 1 |
| Forêt de l'Aleixar (18) ⚠️ | l'Aleixar › Baix Camp | 1 |
| Forêt de l'Aleixar (19) ⚠️ | l'Aleixar › Baix Camp | 1 |
| Forêt de Reus (29) ⚠️ | Castellvell del Camp › Baix Camp | 1 |
| Forêt de Reus (30) ⚠️ | Reus › Baix Camp | 1 |
| Forêt de la Selva del Camp (3) ⚠️ | la Selva del Camp › Baix Camp | 1 |
| Forêt de la Selva del Camp (18) ⚠️ | la Selva del Camp › Baix Camp | 1 |
| Forêt de la Selva del Camp (19) ⚠️ | la Selva del Camp › Baix Camp | 1 |
| Forêt de la Selva del Camp (20) ⚠️ | la Selva del Camp › Baix Camp | 1 |
| Forêt de la Selva del Camp (23) ⚠️ | la Selva del Camp › Baix Camp | 1 |
| Forêt de la Selva del Camp (25) ⚠️ | la Selva del Camp › Baix Camp | 1 |
| Forêt de la Selva del Camp (30) ⚠️ | la Selva del Camp › Baix Camp | 1 |
| Forêt de la Selva del Camp (32) ⚠️ | la Selva del Camp › Baix Camp | 1 |
| Forêt de la Selva del Camp (33) ⚠️ | la Selva del Camp › Baix Camp | 1 |
| Forêt de la Selva del Camp (36) ⚠️ | la Selva del Camp › Baix Camp | 1 |
| Forêt de la Selva del Camp (47) ⚠️ | la Selva del Camp › Baix Camp | 1 |
| Forêt de la Selva del Camp (48) ⚠️ | la Selva del Camp › Baix Camp | 1 |
| Bois de Alcover (6) ⚠️ | Alcover › Alt Camp | 1 |
| Forêt de Mont-ral (9) ⚠️ | Mont-ral › Alt Camp | 1 |
| Forêt de Alcover (9) ⚠️ | Alcover › Alt Camp | 1 |
| Bois de Alcover (12) ⚠️ | Alcover › Alt Camp | 1 |
| Forêt de Capafonts (46) ⚠️ | Capafonts › Baix Camp | 1 |
| Forêt de la Febró (4) ⚠️ | la Febró › Baix Camp | 1 |
| Bois de Calafell (54) ⚠️ | Calafell › Baix Penedès | 1 |
| Bois de Calafell (61) ⚠️ | Calafell › Baix Penedès | 1 |
| Forêt de la Febró (6) ⚠️ | la Febró › Baix Camp | 1 |
| Bois de Calafell (70) ⚠️ | Calafell › Baix Penedès | 1 |
| Bois de Calafell (117) ⚠️ | Calafell › Baix Penedès | 1 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (13) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 1 |
| Forêt de Calafell (25) ⚠️ | Calafell › Baix Penedès | 1 |
| Forêt de Calafell (27) ⚠️ | Calafell › Baix Penedès | 1 |
| Forêt de Gratallops (2) ⚠️ | Gratallops › Priorat | 1 |
| Forêt de la Morera de Montsant (87) ⚠️ | la Morera de Montsant › Priorat | 1 |
| Parc de l'Aldea (3) ⚠️ | l'Aldea › Baix Ebre | 1 |
| Bois de Calafell (150) ⚠️ | Calafell › Baix Penedès | 1 |
| Bois de la Figuera (4) ⚠️ | la Figuera › Priorat | 1 |
| Forêt de Horta de Sant Joan (35) ⚠️ | Horta de Sant Joan › Terra Alta | 1 |
| Parc de Prat de Comte ⚠️ | Prat de Comte › Terra Alta | 1 |
| Forêt de Mont-ral (14) ⚠️ | Mont-ral › Alt Camp | 1 |
| Forêt de Mont-ral (15) ⚠️ | Mont-ral › Alt Camp | 1 |
| Forêt de Porrera (2) ⚠️ | Porrera › Priorat | 1 |
| Parc de Tarragona (64) ⚠️ | Tarragona › Tarragonès | 1 |
| Forêt de Xerta (3) ⚠️ | Xerta › Baix Ebre | 1 |
| Forêt de Cornudella de Montsant (99) ⚠️ | Cornudella de Montsant › Priorat | 1 |
| Forêt de Cornudella de Montsant (103) ⚠️ | Cornudella de Montsant › Priorat | 1 |
| Forêt de Cornudella de Montsant (106) ⚠️ | Cornudella de Montsant › Priorat | 1 |
| Forêt de Cornudella de Montsant (107) ⚠️ | Cornudella de Montsant › Priorat | 1 |
| Forêt de Cornudella de Montsant (127) ⚠️ | Cornudella de Montsant › Priorat | 1 |
| Forêt de Cornudella de Montsant (131) ⚠️ | Cornudella de Montsant › Priorat | 1 |
| Forêt de Cornudella de Montsant (133) ⚠️ | Cornudella de Montsant › Priorat | 1 |
| Forêt de Cornudella de Montsant (137) ⚠️ | Cornudella de Montsant › Priorat | 1 |
| Forêt de Cornudella de Montsant (142) ⚠️ | Cornudella de Montsant › Priorat | 1 |
| Forêt de Cornudella de Montsant (143) ⚠️ | Cornudella de Montsant › Priorat | 1 |
| Forêt de Cornudella de Montsant (144) ⚠️ | Cornudella de Montsant › Priorat | 1 |
| Forêt de Creixell (4) ⚠️ | Creixell › Tarragonès | 1 |
| Parc de Torredembarra (17) ⚠️ | Torredembarra › Tarragonès | 1 |
| Forêt de la Torre de Fontaubella (2) ⚠️ | la Torre de Fontaubella › Priorat | 1 |
| Forêt de Colldejou (13) ⚠️ | Colldejou › Baix Camp | 1 |
| Forêt de Colldejou (15) ⚠️ | Colldejou › Baix Camp | 1 |
| Forêt de Colldejou (19) ⚠️ | Colldejou › Baix Camp | 1 |
| Forêt de Colldejou (24) ⚠️ | Colldejou › Baix Camp | 1 |
| Bois de Batea (9) ⚠️ | Batea › Terra Alta | 1 |
| Bois de Batea (12) ⚠️ | Batea › Terra Alta | 1 |
| Bois de Batea (14) ⚠️ | Batea › Terra Alta | 1 |
| Forêt de la Selva del Camp (53) ⚠️ | la Selva del Camp › Baix Camp | 1 |
| Bois de Reus (7) ⚠️ | Reus › Baix Camp | 1 |
| Forêt de la Selva del Camp (57) ⚠️ | la Selva del Camp › Baix Camp | 1 |
| Forêt de la Selva del Camp (59) ⚠️ | la Selva del Camp › Baix Camp | 1 |
| Forêt de la Selva del Camp (62) ⚠️ | la Selva del Camp › Baix Camp | 1 |
| Parc de Salou (249) ⚠️ | Salou › Tarragonès | 1 |
| Forêt de Tarragona (50) ⚠️ | Tarragona › Tarragonès | 1 |
| Forêt de Tortosa (17) ⚠️ | Tortosa › Baix Ebre | 1 |
| Forêt de Tortosa (18) ⚠️ | Tortosa › Baix Ebre | 1 |
| Forêt de Tortosa (20) ⚠️ | Tortosa › Baix Ebre | 1 |
| Forêt de Tortosa (23) ⚠️ | Tortosa › Baix Ebre | 1 |
| Forêt de Tortosa (24) ⚠️ | Tortosa › Baix Ebre | 1 |
| Forêt de Tortosa (25) ⚠️ | Tortosa › Baix Ebre | 1 |
| Forêt de Tortosa (30) ⚠️ | Tortosa › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (191) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de Margalef (16) ⚠️ | Margalef › Priorat | 1 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (15) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 1 |
| Forêt de l'Ametlla de Mar (192) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 1 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (18) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 1 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (20) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 1 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (28) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 1 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (29) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 1 |
| Forêt de Reus (33) ⚠️ | Reus › Baix Camp | 1 |
| Forêt de Torredembarra (2) ⚠️ | Torredembarra › Tarragonès | 1 |
| Forêt de Torredembarra (3) ⚠️ | Torredembarra › Tarragonès | 1 |
| Forêt de Torredembarra (5) ⚠️ | Torredembarra › Tarragonès | 1 |
| Forêt de Altafulla (3) ⚠️ | Altafulla › Tarragonès | 1 |
| Forêt de Altafulla (5) ⚠️ | Altafulla › Tarragonès | 1 |
| Parc de Torredembarra (18) ⚠️ | Torredembarra › Tarragonès | 1 |
| Forêt de Torredembarra (9) ⚠️ | Torredembarra › Tarragonès | 1 |
| Forêt de el Vendrell (39) ⚠️ | el Vendrell › Baix Penedès | 1 |
| Forêt de Roda de Berà (12) ⚠️ | Roda de Berà › Tarragonès | 1 |
| Forêt de Roda de Berà (13) ⚠️ | Roda de Berà › Tarragonès | 1 |
| Forêt de Roda de Berà (14) ⚠️ | Roda de Berà › Tarragonès | 1 |
| Forêt de el Vendrell (42) ⚠️ | el Vendrell › Baix Penedès | 1 |
| Forêt de el Vendrell (45) ⚠️ | el Vendrell › Baix Penedès | 1 |
| Bois de Calafell (171) ⚠️ | Calafell › Baix Penedès | 1 |
| Forêt de Cunit (14) ⚠️ | Cunit › Baix Penedès | 1 |
| Forêt de Cunit (16) ⚠️ | Cunit › Baix Penedès | 1 |
| Forêt de Bràfim (7) ⚠️ | Bràfim › Alt Camp | 1 |
| Plaça de les Xiquetes i els Xiquets ⚠️ | Reus › Baix Camp | 1 |
| Forêt de l'Ametlla de Mar (193) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de Querol (28) ⚠️ | Querol › Alt Camp | 1 |
| Forêt de la Sénia (23) ⚠️ | la Sénia › Montsià | 1 |
| Forêt de la Sénia (33) ⚠️ | la Sénia › Montsià | 1 |
| Forêt de la Sénia (38) ⚠️ | la Sénia › Montsià | 1 |
| Forêt de Roquetes (15) ⚠️ | Roquetes › Baix Ebre | 1 |
| Forêt de Roquetes (16) ⚠️ | Roquetes › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (195) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (198) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (32) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 1 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (35) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 1 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (39) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 1 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (40) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (89) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (41) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 1 |
| Bois de Mont-roig del Camp (12) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (92) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (94) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (95) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (96) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (99) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Bois de Mont-roig del Camp (17) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (105) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (108) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (117) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (124) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Cambrils (16) ⚠️ | Cambrils › Baix Camp | 1 |
| Parc ⚠️ | Salou › Tarragonès | 1 |
| Forêt de Salou (37) ⚠️ | Salou › Tarragonès | 1 |
| Forêt de Salou (38) ⚠️ | Salou › Tarragonès | 1 |
| Forêt de Salou (40) ⚠️ | Salou › Tarragonès | 1 |
| Bosquet de Llastres ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (43) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 1 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (46) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 1 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (47) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 1 |
| Forêt de Vandellòs i l'Hospitalet de l'Infant (50) ⚠️ | Vandellòs i l'Hospitalet de l'Infant › Baix Camp | 1 |
| Forêt de l'Ametlla de Mar (204) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de la Riera de Gaià (2) ⚠️ | la Riera de Gaià › Tarragonès | 1 |
| Forêt de Tarragona (57) ⚠️ | Tarragona › Tarragonès | 1 |
| Forêt de Tarragona (59) ⚠️ | Tarragona › Tarragonès | 1 |
| Forêt de la Riera de Gaià (5) ⚠️ | la Riera de Gaià › Tarragonès | 1 |
| Forêt de Sant Jaume d'Enveja (3) ⚠️ | Sant Jaume d'Enveja › Montsià | 1 |
| Forêt de Sant Jaume d'Enveja (5) ⚠️ | Sant Jaume d'Enveja › Montsià | 1 |
| Forêt de Sant Jaume d'Enveja (7) ⚠️ | Sant Jaume d'Enveja › Montsià | 1 |
| Forêt de Deltebre (2) ⚠️ | Deltebre › Baix Ebre | 1 |
| Forêt de Deltebre (3) ⚠️ | Deltebre › Baix Ebre | 1 |
| Forêt de Deltebre (4) ⚠️ | Deltebre › Baix Ebre | 1 |
| Forêt de Tortosa (43) ⚠️ | Tortosa › Baix Ebre | 1 |
| Forêt de Tortosa (44) ⚠️ | Tortosa › Baix Ebre | 1 |
| Forêt de l'Ampolla (7) ⚠️ | l'Ampolla › Baix Ebre | 1 |
| Forêt de el Perelló (18) ⚠️ | el Perelló › Baix Ebre | 1 |
| Forêt de el Perelló (21) ⚠️ | el Perelló › Baix Ebre | 1 |
| Forêt de el Perelló (22) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (207) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (210) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (211) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (212) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de el Perelló (26) ⚠️ | el Perelló › Baix Ebre | 1 |
| Forêt de el Perelló (27) ⚠️ | el Perelló › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (214) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (218) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (221) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (223) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Pinar de Paletes ⚠️ | Alcanar › Montsià | 1 |
| Forêt de Alcanar (12) ⚠️ | Alcanar › Montsià | 1 |
| Forêt de Alcanar (18) ⚠️ | Alcanar › Montsià | 1 |
| Forêt de Alcanar (23) ⚠️ | Alcanar › Montsià | 1 |
| Forêt de Alcanar (24) ⚠️ | Alcanar › Montsià | 1 |
| Forêt de Mont-roig del Camp (127) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (128) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de l'Ametlla de Mar (228) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (230) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de l'Ametlla de Mar (232) ⚠️ | l'Ametlla de Mar › Baix Ebre | 1 |
| Forêt de Calafell (45) ⚠️ | Calafell › Baix Penedès | 1 |
| Forêt de Cunit (26) ⚠️ | Cunit › Baix Penedès | 1 |
| Parc de Mas Abelló ⚠️ | Reus › Baix Camp | 1 |
| Parc Claudi Tricaz ⚠️ | Reus › Baix Camp | 1 |
| Forêt de l'Aldea (3) ⚠️ | l'Aldea › Baix Ebre | 1 |
| Parc de Reus (102) ⚠️ | Reus › Baix Camp | 1 |
| Forêt de Vallfogona de Riucorb (2) ⚠️ | Vallfogona de Riucorb › Conca de Barberà | 1 |
| Parc del Riu (2) ⚠️ | Deltebre › Baix Ebre | 1 |
| Forêt de Ulldemolins (88) ⚠️ | Ulldemolins › Priorat | 1 |
| Parc de Reus (103) ⚠️ | Reus › Baix Camp | 1 |
| Forêt de la Morera de Montsant (96) ⚠️ | la Morera de Montsant › Priorat | 1 |
| Pinar de Perrruquet ⚠️ | Vila-seca › Tarragonès | 1 |
| Forêt de Querol (40) ⚠️ | Querol › Alt Camp | 1 |
| Forêt de Querol (44) ⚠️ | Querol › Alt Camp | 1 |
| Forêt de Querol (45) ⚠️ | Querol › Alt Camp | 1 |
| Forêt de la Morera de Montsant (104) ⚠️ | la Morera de Montsant › Priorat | 1 |
| Forêt de la Vilella Baixa (13) ⚠️ | la Vilella Baixa › Priorat | 1 |
| Forêt de la Vilella Baixa (16) ⚠️ | la Vilella Baixa › Priorat | 1 |
| Plaça de l'Arbre ⚠️ | Riudoms › Baix Camp | 1 |
| Parc de la Sort ⚠️ | Riudoms › Baix Camp | 1 |
| Forêt de Capafonts (53) ⚠️ | Capafonts › Baix Camp | 1 |
| Forêt de el Pont d'Armentera (4) ⚠️ | Aiguamúrcia › Alt Camp | 1 |
| Forêt de Aiguamúrcia (29) ⚠️ | Aiguamúrcia › Alt Camp | 1 |
| Forêt de Aiguamúrcia (31) ⚠️ | Aiguamúrcia › Alt Camp | 1 |
| Forêt de el Pont d'Armentera (7) ⚠️ | el Pont d'Armentera › Alt Camp | 1 |
| Forêt de Mont-roig del Camp (133) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (134) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (135) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (139) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Forêt de Mont-roig del Camp (147) ⚠️ | Mont-roig del Camp › Baix Camp | 1 |
| Parc de Reus (104) ⚠️ | Reus › Baix Camp | 1 |
| Forêt de Calafell (54) ⚠️ | Calafell › Baix Penedès | 1 |
| Plaça Passeig Clariana ⚠️ | Valls › Alt Camp | 1 |
| Plaça Centre Cultural ⚠️ | Valls › Alt Camp | 1 |
| Plaça Cinc de Nou ⚠️ | Valls › Alt Camp | 1 |
| Parc de Cambrils (53) ⚠️ | Cambrils › Baix Camp | 1 |
| Parc de Salou (251) ⚠️ | Salou › Tarragonès | 1 |
| Parc de Salou (252) ⚠️ | Salou › Tarragonès | 1 |
| Forêt de Roda de Berà (23) ⚠️ | Roda de Berà › Tarragonès | 1 |
| Forêt de el Vendrell (50) ⚠️ | el Vendrell › Baix Penedès | 1 |
| Forêt de Tortosa (46) ⚠️ | Tortosa › Baix Ebre | 1 |
| Forêt de Creixell (11) ⚠️ | Creixell › Tarragonès | 1 |
| Forêt de Roda de Berà (24) ⚠️ | Roda de Berà › Tarragonès | 1 |
| Forêt de Roda de Berà (25) ⚠️ | Roda de Berà › Tarragonès | 1 |
| Forêt de el Vendrell (51) ⚠️ | el Vendrell › Baix Penedès | 1 |
| Forêt de Riba-roja d'Ebre (24) ⚠️ | Riba-roja d'Ebre › Ribera d'Ebre | 1 |
| Forêt de Riba-roja d'Ebre (25) ⚠️ | Riba-roja d'Ebre › Ribera d'Ebre | 1 |
| Forêt de Riba-roja d'Ebre (26) ⚠️ | Riba-roja d'Ebre › Ribera d'Ebre | 1 |
| Forêt de Colldejou (27) ⚠️ | Colldejou › Baix Camp | 1 |
| Forêt de Calafell (56) ⚠️ | Calafell › Baix Penedès | 1 |

2 781 parc(s) plus petits qu'une cellule ne sont pas listés : la carte les dessine, mais ils n'offrent aucune cellule.

⚠️ 4301 parc(s) hors de la fenêtre 10–125 cellules (4167 trop petit(s), 134 trop grand(s)) : affichés sur la carte, mais ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| airport | 106 |
| prison | 7 |
| military | 0 |
| **Total déclaré** | **113** |
| dont dans une zone de ce territoire | 113 |


### Zones concernées

| Zone | Cellules exclues |
|---|---:|
| Reus | 78 |
| Constantí | 28 |
| el Catllar | 7 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
