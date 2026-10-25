# Province de Lérida

Pack `es-lleida` · version 1.0.0 · grille 200 m · Espagne › Catalogne

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 547 209 |
| dont restreintes (aéroport, militaire, prison) | 134 |
| dont sans chemin (aucune voie à moins de 60 m) | 78 892 |
| dont en forêt, sans chemin non plus | 71 029 |
| dont traversées par un cours d'eau, sans chemin non plus | 20 247 |
| Cellules retirées par le masque d'eau | 4 701 |
| Villes | 231 |
| Arrondissements et quartiers | 0 |
| Îles | 14 |
| Parcs | 8 301 |

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
| Alt Urgell | 65 489 | somme de 19 villes |
| Alta Ribagorça | 19 450 | somme de 3 villes |
| Berguedà (Lérida) | 2 542 | somme de 1 villes |
| Cerdanya (Lérida) | 13 481 | somme de 6 villes |
| Garrigues | 35 293 | somme de 24 villes |
| Noguera | 79 206 | somme de 30 villes |
| Pallars Jussà | 60 534 | somme de 14 villes |
| Pallars Sobirà | 63 186 | somme de 15 villes |
| Pla d'Urgell | 13 628 | somme de 16 villes |
| Segarra | 25 263 | somme de 19 villes |
| Segrià | 61 766 | somme de 38 villes |
| Solsonès | 52 374 | somme de 17 villes |
| Urgell | 25 890 | somme de 20 villes |
| Val d'Aran | 29 113 | somme de 9 villes |

Une île *composite* n'a pas de cellules à elle : sa progression est la somme de ses villes, et ses cellules ne lui sont jamais rattachées directement — elles compteraient deux fois.

## Villes (231)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Sans chemin | Parcs |
|---|---:|---:|---:|---:|---:|---:|---:|
| Tremp | 13 794 | 40 | 13 754 | 13 | **13 741** | 3 222 (23 %) | 144 |
| Naut Aran | 11 835 | 151 | 11 684 | 0 | **11 684** | 4 061 (35 %) | 152 |
| la Vall de Boí | 10 124 | 111 | 10 013 | 0 | **10 013** | 3 891 (39 %) | 296 |
| Alt Àneu | 10 070 | 91 | 9 979 | 0 | **9 979** | 3 395 (34 %) | 153 |
| Vielha e Mijaran | 9 797 | 40 | 9 757 | 0 | **9 757** | 2 507 (26 %) | 93 |
| Lleida | 9 492 | 103 | 9 389 | 0 | **9 389** | 915 (10 %) | 126 |
| Alins | 8 502 | 41 | 8 461 | 0 | **8 461** | 2 203 (26 %) | 117 |
| Montferrer i Castellbò | 8 101 | 4 | 8 097 | 0 | **8 097** | 758 (9 %) | 121 |
| Artesa de Segre | 7 994 | 18 | 7 976 | 0 | **7 976** | 683 (9 %) | 26 |
| les Valls de Valira | 7 733 | 4 | 7 729 | 0 | **7 729** | 948 (12 %) | 158 |
| Conca de Dalt | 7 573 | 110 | 7 463 | 0 | **7 463** | 1 231 (16 %) | 56 |
| la Torre de Cabdella | 7 587 | 145 | 7 442 | 0 | **7 442** | 2 221 (30 %) | 74 |
| Àger | 7 276 | 168 | 7 108 | 0 | **7 108** | 946 (13 %) | 190 |
| Coll de Nargó | 6 999 | 97 | 6 902 | 0 | **6 902** | 860 (12 %) | 132 |
| Camarasa | 7 096 | 209 | 6 887 | 0 | **6 887** | 627 (9 %) | 49 |
| el Pont de Suert | 6 800 | 76 | 6 724 | 0 | **6 724** | 1 453 (22 %) | 108 |
| Lladorre | 6 800 | 93 | 6 707 | 0 | **6 707** | 2 224 (33 %) | 55 |
| Navès | 6 604 | 64 | 6 540 | 0 | **6 540** | 201 (3 %) | 222 |
| la Baronia de Rialb | 6 539 | 209 | 6 330 | 0 | **6 330** | 366 (6 %) | 55 |
| Isona i Conca Dellà | 6 382 | 72 | 6 310 | 0 | **6 310** | 680 (11 %) | 34 |
| Lladurs | 5 871 | 4 | 5 867 | 0 | **5 867** | 308 (5 %) | 281 |
| Baix Pallars | 5 880 | 18 | 5 862 | 0 | **5 862** | 923 (16 %) | 83 |
| Os de Balaguer | 6 127 | 289 | 5 838 | 0 | **5 838** | 692 (12 %) | 87 |
| les Valls d'Aguilar | 5 650 | 3 | 5 647 | 0 | **5 647** | 831 (15 %) | 40 |
| Odèn | 5 179 | 0 | 5 179 | 0 | **5 179** | 497 (10 %) | 139 |
| Alcarràs | 5 129 | 51 | 5 078 | 0 | **5 078** | 722 (14 %) | 18 |
| la Guingueta d'Àneu | 5 027 | 37 | 4 990 | 0 | **4 990** | 1 196 (24 %) | 89 |
| Ribera d'Urgellet | 4 896 | 13 | 4 883 | 8 | **4 875** | 371 (8 %) | 57 |
| Soriguera | 4 872 | 9 | 4 863 | 0 | **4 863** | 595 (12 %) | 59 |
| la Vansa i Fórnols | 4 854 | 0 | 4 854 | 0 | **4 854** | 754 (16 %) | 39 |
| Sort | 4 797 | 13 | 4 784 | 0 | **4 784** | 1 425 (30 %) | 41 |
| Vilanova de Meià | 4 751 | 3 | 4 748 | 0 | **4 748** | 592 (12 %) | 18 |
| Pinós | 4 712 | 1 | 4 711 | 0 | **4 711** | 429 (9 %) | 163 |
| Lles de Cerdanya | 4 675 | 5 | 4 670 | 0 | **4 670** | 858 (18 %) | 36 |
| Fígols i Alinyà | 4 655 | 7 | 4 648 | 0 | **4 648** | 678 (15 %) | 32 |
| les Avellanes i Santa Linya | 4 666 | 100 | 4 566 | 0 | **4 566** | 455 (10 %) | 21 |
| Bellver de Cerdanya | 4 470 | 4 | 4 466 | 0 | **4 466** | 571 (13 %) | 108 |
| Espot | 4 471 | 74 | 4 397 | 0 | **4 397** | 1 372 (31 %) | 61 |
| Sant Esteve de la Sarga | 4 244 | 15 | 4 229 | 0 | **4 229** | 970 (23 %) | 80 |
| Torà | 4 199 | 0 | 4 199 | 0 | **4 199** | 442 (11 %) | 39 |
| Gavet de la Conca | 4 131 | 4 | 4 127 | 0 | **4 127** | 426 (10 %) | 13 |
| Pinell de Solsonès | 4 118 | 0 | 4 118 | 0 | **4 118** | 588 (14 %) | 39 |
| Torrefeta i Florejacs | 4 013 | 7 | 4 006 | 0 | **4 006** | 698 (17 %) | 16 |
| Sarroca de Bellera | 3 983 | 1 | 3 982 | 0 | **3 982** | 1 300 (33 %) | 25 |
| la Granadella | 3 957 | 0 | 3 957 | 0 | **3 957** | 478 (12 %) | 17 |
| Tàrrega | 3 929 | 5 | 3 924 | 0 | **3 924** | 361 (9 %) | 10 |
| Oliola | 3 893 | 0 | 3 893 | 0 | **3 893** | 794 (20 %) | 11 |
| Seròs | 3 816 | 27 | 3 789 | 0 | **3 789** | 226 (6 %) | 11 |
| Cabó | 3 621 | 0 | 3 621 | 0 | **3 621** | 568 (16 %) | 49 |
| Agramunt | 3 568 | 3 | 3 565 | 0 | **3 565** | 439 (12 %) | 20 |
| Abella de la Conca | 3 560 | 0 | 3 560 | 0 | **3 560** | 638 (18 %) | 84 |
| Juncosa | 3 415 | 3 | 3 412 | 0 | **3 412** | 691 (20 %) | 23 |
| Llavorsí | 3 147 | 14 | 3 133 | 0 | **3 133** | 377 (12 %) | 72 |
| Josa i Tuixén | 3 122 | 0 | 3 122 | 0 | **3 122** | 605 (19 %) | 61 |
| Alòs de Balaguer | 3 106 | 17 | 3 089 | 0 | **3 089** | 434 (14 %) | 9 |
| Biosca | 2 992 | 0 | 2 992 | 0 | **2 992** | 337 (11 %) | 18 |
| Almenar | 3 000 | 10 | 2 990 | 0 | **2 990** | 294 (10 %) | 6 |
| Aitona | 2 989 | 40 | 2 949 | 0 | **2 949** | 126 (4 %) | 12 |
| Bassella | 3 225 | 280 | 2 945 | 0 | **2 945** | 179 (6 %) | 33 |
| Rialp | 2 953 | 9 | 2 944 | 0 | **2 944** | 305 (10 %) | 32 |
| Guixers | 2 994 | 57 | 2 937 | 0 | **2 937** | 123 (4 %) | 151 |
| Llardecans | 2 937 | 4 | 2 933 | 0 | **2 933** | 301 (10 %) | 7 |
| Farrera | 2 917 | 1 | 2 916 | 0 | **2 916** | 406 (14 %) | 33 |
| Castelldans | 2 889 | 2 | 2 887 | 0 | **2 887** | 489 (17 %) | 3 |
| Castell de Mur | 2 860 | 88 | 2 772 | 0 | **2 772** | 659 (24 %) | 33 |
| la Pobla de Cérvoles | 2 770 | 4 | 2 766 | 0 | **2 766** | 72 (3 %) | 18 |
| la Coma i la Pedra | 2 755 | 0 | 2 755 | 0 | **2 755** | 153 (6 %) | 184 |
| les Borges Blanques | 2 747 | 10 | 2 737 | 0 | **2 737** | 104 (4 %) | 5 |
| Vilaller | 2 737 | 24 | 2 713 | 0 | **2 713** | 628 (23 %) | 71 |
| Castellar de la Ribera | 2 707 | 0 | 2 707 | 0 | **2 707** | 169 (6 %) | 29 |
| Alàs i Cerc | 2 643 | 3 | 2 640 | 0 | **2 640** | 149 (6 %) | 49 |
| Arbeca | 2 603 | 7 | 2 596 | 0 | **2 596** | 197 (8 %) | 7 |
| Vall de Cardós | 2 598 | 3 | 2 595 | 0 | **2 595** | 554 (21 %) | 64 |
| Maials | 2 555 | 0 | 2 555 | 0 | **2 555** | 321 (13 %) | 24 |
| Balaguer | 2 572 | 19 | 2 553 | 0 | **2 553** | 395 (15 %) | 25 |
| Gósol | 2 542 | 0 | 2 542 | 0 | **2 542** | 137 (5 %) | 114 |
| els Plans de Sió | 2 531 | 3 | 2 528 | 0 | **2 528** | 350 (14 %) | 21 |
| Montellà i Martinet | 2 526 | 3 | 2 523 | 0 | **2 523** | 245 (10 %) | 56 |
| Gimenells i el Pla de la Font | 2 507 | 25 | 2 482 | 0 | **2 482** | 468 (19 %) | 69 |
| Olius | 2 496 | 14 | 2 482 | 0 | **2 482** | 123 (5 %) | 368 |
| Cervera | 2 480 | 1 | 2 479 | 3 | **2 476** | 250 (10 %) | 33 |
| Almatret | 2 503 | 39 | 2 464 | 0 | **2 464** | 173 (7 %) | 17 |
| Peramola | 2 531 | 71 | 2 460 | 0 | **2 460** | 249 (10 %) | 45 |
| Algerri | 2 445 | 6 | 2 439 | 0 | **2 439** | 450 (18 %) | 7 |
| Vilanova de l'Aguda | 2 427 | 0 | 2 427 | 0 | **2 427** | 290 (12 %) | 6 |
| Ribera d'Ondara | 2 426 | 0 | 2 426 | 0 | **2 426** | 429 (18 %) | 35 |
| Castelló de Farfanya | 2 365 | 6 | 2 359 | 0 | **2 359** | 505 (21 %) | 1 |
| Canejan | 2 270 | 17 | 2 253 | 0 | **2 253** | 415 (18 %) | 31 |
| Alguaire | 2 258 | 11 | 2 247 | 83 | **2 164** | 415 (19 %) | 1 |
| Almacelles | 2 203 | 5 | 2 198 | 0 | **2 198** | 274 (12 %) | 12 |
| Riner | 2 139 | 1 | 2 138 | 0 | **2 138** | 190 (9 %) | 171 |
| Torres de Segre | 2 258 | 139 | 2 119 | 0 | **2 119** | 75 (4 %) | 29 |
| Bellvís | 2 101 | 3 | 2 098 | 0 | **2 098** | 146 (7 %) | 9 |
| Juneda | 2 108 | 17 | 2 091 | 0 | **2 091** | 139 (7 %) | 17 |
| el Pont de Bar | 1 992 | 7 | 1 985 | 0 | **1 985** | 136 (7 %) | 55 |
| Cava | 1 904 | 0 | 1 904 | 0 | **1 904** | 237 (12 %) | 29 |
| Sarroca de Lleida | 1 847 | 8 | 1 839 | 0 | **1 839** | 95 (5 %) | 2 |
| Torregrossa | 1 823 | 7 | 1 816 | 0 | **1 816** | 104 (6 %) | 1 |
| Llimiana | 1 851 | 40 | 1 811 | 0 | **1 811** | 128 (7 %) | 19 |
| Clariana de Cardener | 1 848 | 62 | 1 786 | 0 | **1 786** | 58 (3 %) | 241 |
| Cubells | 1 777 | 3 | 1 774 | 0 | **1 774** | 209 (12 %) | 1 |
| Llobera | 1 768 | 0 | 1 768 | 0 | **1 768** | 103 (6 %) | 537 |
| Albesa | 1 676 | 0 | 1 676 | 0 | **1 676** | 184 (11 %) | 1 |
| la Granja d'Escarp | 1 698 | 24 | 1 674 | 0 | **1 674** | 178 (11 %) | 15 |
| Vinaixa | 1 664 | 0 | 1 664 | 0 | **1 664** | 40 (2 %) | 9 |
| Verdú | 1 597 | 7 | 1 590 | 0 | **1 590** | 137 (9 %) | 1 |
| Senterada | 1 587 | 3 | 1 584 | 0 | **1 584** | 159 (10 %) | 21 |
| Bell-lloc d'Urgell | 1 579 | 4 | 1 575 | 0 | **1 575** | 149 (9 %) | 2 |
| Bellpuig | 1 570 | 1 | 1 569 | 0 | **1 569** | 123 (8 %) | 3 |
| Sant Martí de Riucorb | 1 554 | 0 | 1 554 | 0 | **1 554** | 184 (12 %) | 17 |
| Vallbona de les Monges | 1 547 | 0 | 1 547 | 0 | **1 547** | 167 (11 %) | 13 |
| la Pobla de Segur | 1 523 | 44 | 1 479 | 0 | **1 479** | 144 (10 %) | 42 |
| Cervià de les Garrigues | 1 511 | 34 | 1 477 | 0 | **1 477** | 167 (11 %) | 4 |
| Sanaüja | 1 459 | 0 | 1 459 | 0 | **1 459** | 187 (13 %) | 2 |
| l'Albi | 1 455 | 2 | 1 453 | 0 | **1 453** | 47 (3 %) | 2 |
| Alfés | 1 427 | 3 | 1 424 | 0 | **1 424** | 126 (9 %) | 1 |
| Maldà | 1 413 | 4 | 1 409 | 0 | **1 409** | 122 (9 %) | 5 |
| Bellcaire d'Urgell | 1 397 | 2 | 1 395 | 0 | **1 395** | 105 (8 %) | 5 |
| Ponts | 1 396 | 12 | 1 384 | 0 | **1 384** | 96 (7 %) | 22 |
| Bovera | 1 367 | 0 | 1 367 | 0 | **1 367** | 182 (13 %) | 7 |
| Oliana | 1 437 | 73 | 1 364 | 0 | **1 364** | 83 (6 %) | 29 |
| Talavera | 1 341 | 0 | 1 341 | 0 | **1 341** | 271 (20 %) | 78 |
| Soses | 1 347 | 10 | 1 337 | 0 | **1 337** | 15 (1 %) | 3 |
| la Sentiu de Sió | 1 336 | 6 | 1 330 | 0 | **1 330** | 72 (5 %) |  |
| Montoliu de Segarra | 1 323 | 0 | 1 323 | 0 | **1 323** | 175 (13 %) | 8 |
| Montgai | 1 312 | 1 | 1 311 | 0 | **1 311** | 63 (5 %) | 2 |
| Preixens | 1 294 | 0 | 1 294 | 0 | **1 294** | 157 (12 %) | 1 |
| Bossòst | 1 297 | 5 | 1 292 | 0 | **1 292** | 74 (6 %) | 12 |
| Foradada | 1 293 | 7 | 1 286 | 0 | **1 286** | 123 (10 %) | 5 |
| Linyola | 1 285 | 0 | 1 285 | 0 | **1 285** | 148 (12 %) | 1 |
| Torrebesses | 1 234 | 2 | 1 232 | 0 | **1 232** | 18 (1 %) | 1 |
| Térmens | 1 236 | 15 | 1 221 | 0 | **1 221** | 91 (7 %) | 9 |
| Vallfogona de Balaguer | 1 223 | 2 | 1 221 | 0 | **1 221** | 96 (8 %) | 7 |
| la Molsosa | 1 203 | 1 | 1 202 | 0 | **1 202** | 78 (6 %) | 79 |
| Talarn | 1 270 | 76 | 1 194 | 27 | **1 167** | 80 (7 %) | 12 |
| Massoteres | 1 181 | 0 | 1 181 | 0 | **1 181** | 203 (17 %) | 1 |
| Ossó de Sió | 1 173 | 0 | 1 173 | 0 | **1 173** | 229 (20 %) | 4 |
| Ivars de Noguera | 1 224 | 67 | 1 157 | 0 | **1 157** | 115 (10 %) | 20 |
| Penelles | 1 149 | 1 | 1 148 | 0 | **1 148** | 159 (14 %) | 5 |
| Guimerà | 1 147 | 0 | 1 147 | 0 | **1 147** | 163 (14 %) | 10 |
| Sant Guim de Freixenet | 1 117 | 0 | 1 117 | 0 | **1 117** | 152 (14 %) | 15 |
| Granyanella | 1 079 | 3 | 1 076 | 0 | **1 076** | 104 (10 %) | 4 |
| Artesa de Lleida | 1 072 | 5 | 1 067 | 0 | **1 067** | 51 (5 %) | 3 |
| Anglesola | 1 063 | 4 | 1 059 | 0 | **1 059** | 92 (9 %) | 3 |
| Les | 1 062 | 4 | 1 058 | 0 | **1 058** | 55 (5 %) | 5 |
| Ivars d'Urgell | 1 088 | 35 | 1 053 | 0 | **1 053** | 93 (9 %) |  |
| Torrefarrera | 1 058 | 7 | 1 051 | 0 | **1 051** | 171 (16 %) | 1 |
| l'Albagés | 1 156 | 129 | 1 027 | 0 | **1 027** | 113 (11 %) | 3 |
| Es Bòrdes | 1 000 | 2 | 998 | 0 | **998** | 133 (13 %) | 17 |
| Estamariu | 978 | 0 | 978 | 0 | **978** | 38 (4 %) | 22 |
| Prullans | 971 | 2 | 969 | 0 | **969** | 168 (17 %) | 10 |
| l'Espluga Calba | 963 | 0 | 963 | 0 | **963** | 36 (4 %) | 3 |
| Preixana | 962 | 0 | 962 | 0 | **962** | 142 (15 %) | 2 |
| Puigverd d'Agramunt | 956 | 0 | 956 | 0 | **956** | 115 (12 %) |  |
| Estaràs | 953 | 0 | 953 | 0 | **953** | 109 (11 %) | 4 |
| Alcanó | 945 | 2 | 943 | 0 | **943** | 37 (4 %) |  |
| Vilanova de la Barca | 957 | 16 | 941 | 0 | **941** | 35 (4 %) | 12 |
| Corbins | 952 | 14 | 938 | 0 | **938** | 18 (2 %) | 4 |
| Menàrguens | 915 | 5 | 910 | 0 | **910** | 128 (14 %) |  |
| Granyena de les Garrigues | 903 | 4 | 899 | 0 | **899** | 28 (3 %) |  |
| Tornabous | 901 | 2 | 899 | 0 | **899** | 96 (11 %) | 3 |
| els Alamús | 898 | 2 | 896 | 0 | **896** | 129 (14 %) | 1 |
| Vilagrassa | 875 | 0 | 875 | 0 | **875** | 83 (9 %) | 2 |
| les Oluges | 862 | 0 | 862 | 0 | **862** | 116 (13 %) | 7 |
| Vila-sana | 863 | 16 | 847 | 0 | **847** | 56 (7 %) | 6 |
| Sant Ramon | 836 | 0 | 836 | 0 | **836** | 42 (5 %) | 1 |
| el Vilosell | 834 | 1 | 833 | 0 | **833** | 50 (6 %) | 3 |
| Salàs de Pallars | 942 | 115 | 827 | 0 | **827** | 76 (9 %) | 7 |
| Bausen | 825 | 0 | 825 | 0 | **825** | 151 (18 %) | 10 |
| Guissona | 815 | 0 | 815 | 0 | **815** | 68 (8 %) | 14 |
| Solsona | 804 | 2 | 802 | 0 | **802** | 8 (1 %) | 170 |
| Bellaguarda | 774 | 2 | 772 | 0 | **772** | 74 (10 %) | 6 |
| el Cogul | 772 | 1 | 771 | 0 | **771** | 4 (1 %) |  |
| Esterri de Cardós | 761 | 0 | 761 | 0 | **761** | 114 (15 %) | 11 |
| Golmés | 750 | 2 | 748 | 0 | **748** | 83 (11 %) | 3 |
| Ciutadilla | 745 | 0 | 745 | 0 | **745** | 42 (6 %) | 3 |
| Granyena de Segarra | 738 | 0 | 738 | 0 | **738** | 44 (6 %) |  |
| Alcoletge | 739 | 6 | 733 | 0 | **733** | 29 (4 %) | 4 |
| Castellnou de Seana | 734 | 2 | 732 | 0 | **732** | 49 (7 %) | 1 |
| Fulleda | 720 | 0 | 720 | 0 | **720** | 7 (1 %) | 6 |
| Vilamòs | 715 | 2 | 713 | 0 | **713** | 38 (5 %) | 13 |
| Belianes | 705 | 0 | 705 | 0 | **705** | 96 (14 %) |  |
| Castellserà | 709 | 6 | 703 | 0 | **703** | 46 (7 %) | 4 |
| Ivorra | 693 | 0 | 693 | 0 | **693** | 81 (12 %) | 1 |
| la Seu d'Urgell | 694 | 8 | 686 | 0 | **686** | 17 (2 %) | 43 |
| Alpicat | 684 | 6 | 678 | 0 | **678** | 107 (16 %) | 7 |
| Miralcamp | 663 | 6 | 657 | 0 | **657** | 26 (4 %) | 3 |
| Cabanabona | 648 | 0 | 648 | 0 | **648** | 142 (22 %) | 1 |
| Vilanova de Bellpuig | 614 | 0 | 614 | 0 | **614** | 93 (15 %) | 1 |
| Massalcoreig | 633 | 24 | 609 | 0 | **609** | 2 (0 %) | 13 |
| els Torms | 594 | 1 | 593 | 0 | **593** | 151 (25 %) | 2 |
| els Omells de na Gaia | 591 | 0 | 591 | 0 | **591** | 13 (2 %) | 6 |
| Riu de Cerdanya | 572 | 0 | 572 | 0 | **572** | 11 (2 %) | 27 |
| Sunyer | 571 | 0 | 571 | 0 | **571** | 8 (1 %) |  |
| Tarrés | 569 | 0 | 569 | 0 | **569** | 3 (1 %) | 12 |
| la Portella | 565 | 3 | 562 | 0 | **562** | 15 (3 %) | 1 |
| el Palau d'Anglesola | 552 | 0 | 552 | 0 | **552** | 42 (8 %) | 5 |
| el Soleràs | 555 | 3 | 552 | 0 | **552** | 20 (4 %) | 1 |
| Organyà | 557 | 7 | 550 | 0 | **550** | 32 (6 %) | 27 |
| Sant Guim de la Plana | 548 | 0 | 548 | 0 | **548** | 51 (9 %) | 5 |
| Puigverd de Lleida | 547 | 3 | 544 | 0 | **544** | 2 (0 %) |  |
| Arres | 534 | 1 | 533 | 0 | **533** | 24 (5 %) | 5 |
| Montornès de Segarra | 532 | 0 | 532 | 0 | **532** | 26 (5 %) | 2 |
| Tiurana | 698 | 167 | 531 | 0 | **531** | 21 (4 %) | 3 |
| Alfarràs | 515 | 2 | 513 | 0 | **513** | 29 (6 %) | 7 |
| la Fuliola | 501 | 1 | 500 | 0 | **500** | 53 (11 %) | 1 |
| els Omellons | 497 | 0 | 497 | 0 | **497** | 13 (3 %) | 1 |
| Torrelameu | 485 | 1 | 484 | 0 | **484** | 4 (1 %) |  |
| Arsèguel | 480 | 6 | 474 | 0 | **474** |  | 18 |
| Albatàrrec | 474 | 7 | 467 | 0 | **467** | 29 (6 %) |  |
| Aspa | 452 | 0 | 452 | 0 | **452** | 6 (1 %) | 3 |
| Puiggròs | 447 | 3 | 444 | 0 | **444** | 20 (5 %) |  |
| Rosselló | 445 | 1 | 444 | 0 | **444** | 46 (10 %) | 8 |
| Nalec | 417 | 0 | 417 | 0 | **417** | 34 (8 %) | 2 |
| Tírvia | 403 | 4 | 399 | 0 | **399** | 20 (5 %) | 11 |
| Esterri d'Àneu | 396 | 1 | 395 | 0 | **395** | 58 (15 %) | 21 |
| el Poal | 397 | 2 | 395 | 0 | **395** | 68 (17 %) | 2 |
| Vilanova de Segrià | 374 | 0 | 374 | 0 | **374** | 21 (6 %) | 1 |
| Sudanell | 368 | 6 | 362 | 0 | **362** | 30 (8 %) | 11 |
| Sidamon | 361 | 2 | 359 | 0 | **359** | 52 (14 %) | 4 |
| Tarroja de Segarra | 350 | 0 | 350 | 0 | **350** | 20 (6 %) | 3 |
| Barbens | 347 | 1 | 346 | 0 | **346** | 35 (10 %) |  |
| Benavent de Segrià | 337 | 1 | 336 | 0 | **336** | 23 (7 %) | 1 |
| Montoliu de Lleida | 333 | 10 | 323 | 0 | **323** | 53 (16 %) | 5 |
| Mollerussa | 309 | 0 | 309 | 0 | **309** | 11 (4 %) | 8 |
| Prats i Sansor | 283 | 2 | 281 | 0 | **281** | 13 (5 %) | 6 |
| Torre-serona | 263 | 0 | 263 | 0 | **263** | 55 (21 %) | 3 |
| la Floresta | 247 | 1 | 246 | 0 | **246** | 6 (2 %) | 2 |
| Fondarella | 243 | 1 | 242 | 0 | **242** | 16 (7 %) | 1 |
| Bellmunt d'Urgell | 224 | 1 | 223 | 0 | **223** | 11 (5 %) |  |
| Sant Llorenç de Morunys | 191 | 0 | 191 | 0 | **191** |  | 49 |

## Parcs (8301)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Forêt de Rialp (7) ⚠️ | Rialp › Pallars Sobirà | 1 483 |
| Forêt de les Valls d'Aguilar (27) ⚠️ | les Valls d'Aguilar › Alt Urgell | 1 253 |
| Forêt de Fígols i Alinyà (8) ⚠️ | Fígols i Alinyà › Alt Urgell | 1 203 |
| Forêt de Navès (30) ⚠️ | Navès › Solsonès | 1 173 |
| Forêt de Lles de Cerdanya (19) ⚠️ | Lles de Cerdanya › Cerdanya (Lérida) | 1 147 |
| Forêt de Peramola (8) ⚠️ | Peramola › Alt Urgell | 1 122 |
| Forêt de Fígols i Alinyà (26) ⚠️ | Fígols i Alinyà › Alt Urgell | 1 061 |
| Forêt de la Vall de Boí (246) ⚠️ | la Vall de Boí › Alta Ribagorça | 1 047 |
| Forêt de Llimiana (4) ⚠️ | Llimiana › Pallars Jussà | 1 042 |
| Forêt de Les (3) ⚠️ | Les › Val d'Aran | 909 |
| Forêt de Espot (29) ⚠️ | Espot › Pallars Sobirà | 878 |
| Forêt de Lladurs (172) ⚠️ | Lladurs › Solsonès | 790 |
| Forêt de Alins (23) ⚠️ | Alins › Pallars Sobirà | 782 |
| Forêt de les Valls de Valira (17) ⚠️ | les Valls de Valira › Alt Urgell | 773 |
| Forêt de Bassella (7) ⚠️ | Bassella › Alt Urgell | 742 |
| Forêt de Navès (39) ⚠️ | Navès › Solsonès | 740 |
| Forêt de Es Bòrdes (2) ⚠️ | Es Bòrdes › Val d'Aran | 739 |
| Forêt de Ribera d'Urgellet (29) ⚠️ | Ribera d'Urgellet › Alt Urgell | 675 |
| Forêt de la Baronia de Rialb (39) ⚠️ | la Baronia de Rialb › Noguera | 668 |
| Forêt de Ribera d'Urgellet (26) ⚠️ | Ribera d'Urgellet › Alt Urgell | 667 |
| Forêt de Àger ⚠️ | Àger › Noguera | 645 |
| Forêt de Llobera (522) ⚠️ | Llobera › Solsonès | 633 |
| Forêt de Bassella (6) ⚠️ | Bassella › Alt Urgell | 623 |
| Forêt de Pinell de Solsonès (33) ⚠️ | Pinell de Solsonès › Solsonès | 607 |
| Forêt de Josa i Tuixén (9) ⚠️ | Josa i Tuixén › Alt Urgell | 585 |
| Forêt de Almatret (12) ⚠️ | Almatret › Segrià | 561 |
| Forêt de Les (2) ⚠️ | Les › Val d'Aran | 558 |
| Forêt de Os de Balaguer (26) ⚠️ | Os de Balaguer › Noguera | 556 |
| Forêt de Odèn (31) ⚠️ | Odèn › Solsonès | 555 |
| Forêt de Navès (38) ⚠️ | Navès › Solsonès | 506 |
| Forêt de el Pont de Suert (6) ⚠️ | el Pont de Suert › Pallars Jussà | 504 |
| Forêt de Riner (133) ⚠️ | Riner › Solsonès | 493 |
| Forêt de Pinell de Solsonès (32) ⚠️ | Pinell de Solsonès › Solsonès | 484 |
| Forêt de Montferrer i Castellbò (29) ⚠️ | Montferrer i Castellbò › Alt Urgell | 468 |
| Forêt de Naut Aran (55) ⚠️ | Naut Aran › Val d'Aran | 463 |
| Forêt de Naut Aran (56) ⚠️ | Naut Aran › Val d'Aran | 459 |
| Forêt de Montellà i Martinet (4) ⚠️ | Montellà i Martinet › Cerdanya (Lérida) | 448 |
| Forêt de la Baronia de Rialb (33) ⚠️ | la Baronia de Rialb › Noguera | 438 |
| Forêt de Bellver de Cerdanya (17) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 437 |
| Forêt de Pinós (80) ⚠️ | Pinós › Solsonès | 436 |
| Forêt de la Vansa i Fórnols (23) ⚠️ | la Vansa i Fórnols › Alt Urgell | 435 |
| Forêt de la Pobla de Cérvoles (8) ⚠️ | la Pobla de Cérvoles › Garrigues | 431 |
| Forêt de Bassella (4) ⚠️ | Bassella › Alt Urgell | 425 |
| Forêt de Soriguera (7) ⚠️ | Soriguera › Pallars Sobirà | 421 |
| Forêt de Rialp (9) ⚠️ | Rialp › Pallars Sobirà | 419 |
| Forêt de Montferrer i Castellbò (17) ⚠️ | Montferrer i Castellbò › Alt Urgell | 411 |
| Forêt de les Valls d'Aguilar (11) ⚠️ | les Valls d'Aguilar › Alt Urgell | 409 |
| Forêt de Artesa de Segre (25) ⚠️ | Artesa de Segre › Noguera | 409 |
| Forêt de Vielha e Mijaran (8) ⚠️ | Vielha e Mijaran › Val d'Aran | 406 |
| Forêt de Lles de Cerdanya (24) ⚠️ | Lles de Cerdanya › Cerdanya (Lérida) | 403 |
| Forêt de la Torre de Cabdella (21) ⚠️ | la Torre de Cabdella › Pallars Jussà | 402 |
| Forêt de Sarroca de Bellera (21) ⚠️ | Sarroca de Bellera › Pallars Jussà | 399 |
| Forêt de Alt Àneu (36) ⚠️ | Alt Àneu › Pallars Sobirà | 399 |
| Forêt de Castellar de la Ribera (16) ⚠️ | Castellar de la Ribera › Solsonès | 399 |
| Forêt de les Valls de Valira (64) ⚠️ | les Valls de Valira › Alt Urgell | 391 |
| Forêt de Bossòst (6) ⚠️ | Bossòst › Val d'Aran | 390 |
| Forêt de Josa i Tuixén (12) ⚠️ | Josa i Tuixén › Alt Urgell | 389 |
| Forêt de Isona i Conca Dellà (7) ⚠️ | Isona i Conca Dellà › Pallars Jussà | 387 |
| Forêt de Cabó (9) ⚠️ | Cabó › Alt Urgell | 381 |
| Forêt de Castellar de la Ribera (21) ⚠️ | Castellar de la Ribera › Solsonès | 380 |
| Forêt de Josa i Tuixén (10) ⚠️ | Josa i Tuixén › Alt Urgell | 379 |
| Forêt de Farrera (6) ⚠️ | Farrera › Pallars Sobirà | 377 |
| Forêt de Vielha e Mijaran (15) ⚠️ | Vielha e Mijaran › Val d'Aran | 358 |
| Forêt de Montferrer i Castellbò (8) ⚠️ | Montferrer i Castellbò › Alt Urgell | 357 |
| Forêt de la Coma i la Pedra (93) ⚠️ | la Coma i la Pedra › Solsonès | 357 |
| Forêt de Baix Pallars (13) ⚠️ | Baix Pallars › Pallars Sobirà | 352 |
| Forêt de la Guingueta d'Àneu (19) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 349 |
| Forêt de Alòs de Balaguer (4) ⚠️ | Alòs de Balaguer › Noguera | 348 |
| Forêt de Lladorre (22) ⚠️ | Lladorre › Pallars Sobirà | 345 |
| Forêt de Lladorre (16) ⚠️ | Lladorre › Pallars Sobirà | 344 |
| Forêt de Camarasa (30) ⚠️ | Àger › Noguera | 343 |
| Forêt de Artesa de Segre (10) ⚠️ | Artesa de Segre › Noguera | 341 |
| Forêt de Vielha e Mijaran (33) ⚠️ | Vielha e Mijaran › Val d'Aran | 339 |
| Forêt de la Guingueta d'Àneu (17) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 338 |
| Forêt de la Baronia de Rialb (40) ⚠️ | la Baronia de Rialb › Noguera | 337 |
| Forêt de Oliana (3) ⚠️ | Oliana › Alt Urgell | 337 |
| Forêt de Vilaller (34) ⚠️ | Vilaller › Alta Ribagorça | 337 |
| Forêt de Sant Esteve de la Sarga (7) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 336 |
| Forêt de Fígols i Alinyà (32) ⚠️ | Fígols i Alinyà › Alt Urgell | 334 |
| Forêt de Camarasa (4) ⚠️ | Camarasa › Noguera | 332 |
| Forêt de Salàs de Pallars (2) ⚠️ | Salàs de Pallars › Pallars Jussà | 329 |
| Forêt de Artesa de Segre (15) ⚠️ | Artesa de Segre › Noguera | 329 |
| Forêt de Vall de Cardós ⚠️ | Vall de Cardós › Pallars Sobirà | 326 |
| Forêt de Soriguera (25) ⚠️ | Soriguera › Pallars Sobirà | 321 |
| Forêt de Espot (30) ⚠️ | Espot › Pallars Sobirà | 316 |
| Forêt de Rialp (30) ⚠️ | Rialp › Pallars Sobirà | 301 |
| Forêt de Isona i Conca Dellà (32) ⚠️ | Isona i Conca Dellà › Pallars Jussà | 300 |
| Forêt de Pinós (87) ⚠️ | Pinós › Solsonès | 300 |
| Forêt de Soriguera (23) ⚠️ | Soriguera › Pallars Sobirà | 299 |
| Forêt de Alàs i Cerc (32) ⚠️ | Alàs i Cerc › Alt Urgell | 297 |
| Forêt de les Valls de Valira (24) ⚠️ | les Valls de Valira › Alt Urgell | 295 |
| Forêt de Odèn (39) ⚠️ | Odèn › Solsonès | 292 |
| Forêt de Castellar de la Ribera (17) ⚠️ | Castellar de la Ribera › Solsonès | 291 |
| Forêt de Lladurs (171) ⚠️ | Lladurs › Solsonès | 289 |
| Forêt de Josa i Tuixén (11) ⚠️ | Josa i Tuixén › Alt Urgell | 283 |
| Forêt de Conca de Dalt ⚠️ | Conca de Dalt › Pallars Jussà | 279 |
| Forêt de Tiurana ⚠️ | Tiurana › Noguera | 276 |
| Forêt de Cava (13) ⚠️ | Cava › Alt Urgell | 274 |
| Forêt de Canejan (9) ⚠️ | Canejan › Val d'Aran | 272 |
| Forêt de Coll de Nargó (2) ⚠️ | Coll de Nargó › Alt Urgell | 271 |
| Forêt de Olius (311) ⚠️ | Olius › Solsonès | 271 |
| Forêt de Canejan (10) ⚠️ | Canejan › Val d'Aran | 271 |
| Forêt de la Torre de Cabdella (17) ⚠️ | la Torre de Cabdella › Pallars Jussà | 265 |
| Forêt de Vilaller (23) ⚠️ | Vilaller › Alta Ribagorça | 264 |
| Forêt de Rialp (11) ⚠️ | Rialp › Pallars Sobirà | 263 |
| Forêt de Alins (20) ⚠️ | Alins › Pallars Sobirà | 259 |
| Forêt de Lladorre (32) ⚠️ | Lladorre › Pallars Sobirà | 257 |
| Forêt de Camarasa (31) ⚠️ | Camarasa › Noguera | 255 |
| Forêt de Cabó (48) ⚠️ | Cabó › Alt Urgell | 255 |
| Forêt de la Vansa i Fórnols (33) ⚠️ | la Vansa i Fórnols › Alt Urgell | 252 |
| Forêt de Montferrer i Castellbò (6) ⚠️ | Montferrer i Castellbò › Alt Urgell | 251 |
| Forêt de Àger (31) ⚠️ | Àger › Noguera | 250 |
| Forêt de Biosca (10) ⚠️ | Biosca › Solsonès | 243 |
| Forêt de Conca de Dalt (44) ⚠️ | Conca de Dalt › Pallars Jussà | 238 |
| Forêt de Esterri de Cardós ⚠️ | Esterri de Cardós › Pallars Sobirà | 235 |
| Forêt de la Coma i la Pedra (98) ⚠️ | la Coma i la Pedra › Solsonès | 235 |
| Forêt de Clariana de Cardener (157) ⚠️ | Clariana de Cardener › Solsonès | 232 |
| Forêt de Soriguera (26) ⚠️ | Soriguera › Pallars Sobirà | 232 |
| Forêt de Artesa de Segre (24) ⚠️ | Artesa de Segre › Noguera | 232 |
| Forêt de Vielha e Mijaran (63) ⚠️ | Vielha e Mijaran › Val d'Aran | 231 |
| Forêt de la Molsosa (21) ⚠️ | la Molsosa › Solsonès | 230 |
| Forêt de Bellver de Cerdanya (39) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 230 |
| Forêt de Artesa de Segre (11) ⚠️ | Artesa de Segre › Noguera | 229 |
| Forêt de Vilanova de l'Aguda (5) ⚠️ | Vilanova de l'Aguda › Noguera | 228 |
| Forêt de les Avellanes i Santa Linya (9) ⚠️ | les Avellanes i Santa Linya › Noguera | 226 |
| Forêt de Vielha e Mijaran (21) ⚠️ | Vielha e Mijaran › Val d'Aran | 226 |
| Forêt de Alòs de Balaguer (8) ⚠️ | Alòs de Balaguer › Noguera | 226 |
| Forêt de les Valls de Valira (54) ⚠️ | les Valls de Valira › Alt Urgell | 226 |
| Forêt de Llavorsí (47) ⚠️ | Llavorsí › Pallars Sobirà | 224 |
| Forêt de Canejan (8) ⚠️ | Canejan › Val d'Aran | 222 |
| Forêt de Cava (23) ⚠️ | Cava › Alt Urgell | 222 |
| Forêt de Ribera d'Urgellet (4) ⚠️ | Ribera d'Urgellet › Alt Urgell | 221 |
| Forêt de Sarroca de Bellera (23) ⚠️ | Sarroca de Bellera › Pallars Jussà | 219 |
| Forêt de Alt Àneu (109) ⚠️ | Alt Àneu › Pallars Sobirà | 219 |
| Forêt de Navès (33) ⚠️ | Navès › Solsonès | 218 |
| Forêt de Conca de Dalt (23) ⚠️ | Conca de Dalt › Pallars Jussà | 218 |
| Forêt de Alòs de Balaguer (7) ⚠️ | Alòs de Balaguer › Noguera | 218 |
| Forêt de Castellar de la Ribera (28) ⚠️ | Castellar de la Ribera › Solsonès | 218 |
| Forêt de Isona i Conca Dellà (30) ⚠️ | Gavet de la Conca › Pallars Jussà | 217 |
| Forêt de Alins (27) ⚠️ | Alins › Pallars Sobirà | 217 |
| Forêt de Llavorsí (35) ⚠️ | Llavorsí › Pallars Sobirà | 217 |
| Forêt de Vilaller (8) ⚠️ | Vilaller › Alta Ribagorça | 214 |
| Forêt de Lles de Cerdanya (20) ⚠️ | Lles de Cerdanya › Cerdanya (Lérida) | 213 |
| Forêt de Montferrer i Castellbò (34) ⚠️ | Montferrer i Castellbò › Alt Urgell | 213 |
| Forêt de Riu de Cerdanya (2) ⚠️ | Riu de Cerdanya › Cerdanya (Lérida) | 211 |
| Forêt de Os de Balaguer (51) ⚠️ | Os de Balaguer › Noguera | 211 |
| Forêt de la Vansa i Fórnols (36) ⚠️ | la Vansa i Fórnols › Alt Urgell | 210 |
| Forêt de Guixers (28) ⚠️ | Guixers › Solsonès | 209 |
| Forêt de Camarasa (5) ⚠️ | Camarasa › Noguera | 205 |
| Forêt de la Vall de Boí (245) ⚠️ | la Vall de Boí › Alta Ribagorça | 203 |
| Forêt de Foradada (4) ⚠️ | Foradada › Noguera | 203 |
| Forêt de Abella de la Conca (22) ⚠️ | Abella de la Conca › Pallars Jussà | 203 |
| Forêt de Peramola (7) ⚠️ | Peramola › Alt Urgell | 202 |
| Forêt de Sort (12) ⚠️ | Sort › Pallars Sobirà | 201 |
| Forêt de Soriguera (30) ⚠️ | Soriguera › Pallars Sobirà | 201 |
| Forêt de Camarasa (20) ⚠️ | Camarasa › Noguera | 200 |
| Forêt de Biosca (7) ⚠️ | Biosca › Solsonès | 199 |
| Forêt de la Baronia de Rialb (26) ⚠️ | la Baronia de Rialb › Noguera | 199 |
| Forêt de Os de Balaguer (23) ⚠️ | Os de Balaguer › Noguera | 196 |
| Forêt de Fígols i Alinyà (16) ⚠️ | Fígols i Alinyà › Alt Urgell | 195 |
| Forêt de Vilanova de Meià (13) ⚠️ | Vilanova de Meià › Noguera | 193 |
| Forêt de Fígols i Alinyà (14) ⚠️ | Fígols i Alinyà › Alt Urgell | 193 |
| Forêt de Oliola (3) ⚠️ | Oliola › Noguera | 192 |
| Forêt de Bausen (10) ⚠️ | Bausen › Val d'Aran | 190 |
| Forêt de Alins (51) ⚠️ | Alins › Pallars Sobirà | 190 |
| Forêt de Naut Aran (60) ⚠️ | Naut Aran › Val d'Aran | 189 |
| Forêt de Conca de Dalt (28) ⚠️ | Conca de Dalt › Pallars Jussà | 189 |
| Forêt de Vilaller (9) ⚠️ | Vilaller › Alta Ribagorça | 188 |
| Forêt de Castellar de la Ribera (24) ⚠️ | Castellar de la Ribera › Solsonès | 186 |
| Forêt de el Pont de Suert (3) ⚠️ | el Pont de Suert › Alta Ribagorça | 185 |
| Forêt de la Torre de Cabdella (15) ⚠️ | la Torre de Cabdella › Pallars Jussà | 184 |
| Forêt de Vilanova de Meià (9) ⚠️ | Vilanova de Meià › Noguera | 181 |
| Forêt de les Avellanes i Santa Linya (15) ⚠️ | les Avellanes i Santa Linya › Noguera | 180 |
| Forêt de Conca de Dalt (6) ⚠️ | Conca de Dalt › Pallars Jussà | 179 |
| Forêt de Vinaixa (9) ⚠️ | Vinaixa › Garrigues | 179 |
| Forêt de Tremp (43) ⚠️ | Tremp › Pallars Jussà | 179 |
| Forêt de Cabó (33) ⚠️ | Cabó › Alt Urgell | 179 |
| Forêt de Pinell de Solsonès (5) ⚠️ | Pinell de Solsonès › Solsonès | 178 |
| Forêt de Almatret (5) ⚠️ | Almatret › Segrià | 178 |
| Forêt de la Guingueta d'Àneu (44) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 178 |
| Forêt de Bellver de Cerdanya (35) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 178 |
| Forêt de Riu de Cerdanya ⚠️ | Riu de Cerdanya › Cerdanya (Lérida) | 177 |
| Forêt de les Valls de Valira (63) ⚠️ | les Valls de Valira › Alt Urgell | 177 |
| Forêt de les Avellanes i Santa Linya (16) ⚠️ | les Avellanes i Santa Linya › Noguera | 176 |
| Forêt de Alins (3) ⚠️ | Alins › Pallars Sobirà | 175 |
| Bois de Fulleda (3) ⚠️ | Fulleda › Garrigues | 175 |
| Forêt de Alins (19) ⚠️ | Alins › Pallars Sobirà | 175 |
| Forêt de les Valls d'Aguilar (36) ⚠️ | les Valls d'Aguilar › Alt Urgell | 175 |
| Forêt de Gavet de la Conca (11) ⚠️ | Gavet de la Conca › Pallars Jussà | 174 |
| Forêt de Senterada (12) ⚠️ | Senterada › Pallars Jussà | 174 |
| Forêt de Lladorre (23) ⚠️ | Lladorre › Pallars Sobirà | 174 |
| Forêt de les Valls d'Aguilar (32) ⚠️ | les Valls d'Aguilar › Alt Urgell | 174 |
| Forêt de Cabó (24) ⚠️ | Cabó › Alt Urgell | 174 |
| Forêt de la Torre de Cabdella (11) ⚠️ | la Torre de Cabdella › Pallars Jussà | 173 |
| Forêt de Ribera d'Urgellet (50) ⚠️ | Ribera d'Urgellet › Alt Urgell | 173 |
| Forêt de Odèn (30) ⚠️ | Odèn › Solsonès | 172 |
| Forêt de el Pont de Suert (35) ⚠️ | el Pont de Suert › Alta Ribagorça | 172 |
| Forêt de Alins (30) ⚠️ | Alins › Pallars Sobirà | 172 |
| Forêt de Llavorsí (20) ⚠️ | Llavorsí › Pallars Sobirà | 172 |
| Forêt de Montferrer i Castellbò (43) ⚠️ | Montferrer i Castellbò › Alt Urgell | 172 |
| Forêt de Ponts ⚠️ | Ponts › Noguera | 171 |
| Forêt de la Vansa i Fórnols (6) ⚠️ | la Vansa i Fórnols › Alt Urgell | 171 |
| Forêt de Espot (51) ⚠️ | Espot › Pallars Sobirà | 171 |
| Forêt de la Coma i la Pedra (110) ⚠️ | la Coma i la Pedra › Solsonès | 170 |
| Forêt de la Vansa i Fórnols (35) ⚠️ | la Vansa i Fórnols › Alt Urgell | 170 |
| Forêt de Vielha e Mijaran (29) ⚠️ | Vielha e Mijaran › Val d'Aran | 169 |
| Forêt de la Torre de Cabdella (24) ⚠️ | la Torre de Cabdella › Pallars Jussà | 169 |
| Forêt de Estamariu (12) ⚠️ | Estamariu › Alt Urgell | 169 |
| Forêt de Navès (37) ⚠️ | Navès › Solsonès | 168 |
| Forêt de Guixers (99) ⚠️ | Guixers › Solsonès | 168 |
| Forêt de la Baronia de Rialb (41) ⚠️ | la Baronia de Rialb › Noguera | 167 |
| Forêt de Isona i Conca Dellà (10) ⚠️ | Isona i Conca Dellà › Pallars Jussà | 166 |
| Forêt de les Valls de Valira (19) ⚠️ | les Valls de Valira › Alt Urgell | 165 |
| Forêt de Senterada (9) ⚠️ | Senterada › Pallars Jussà | 165 |
| Forêt de Ribera d'Urgellet (25) ⚠️ | Ribera d'Urgellet › Alt Urgell | 165 |
| Forêt de Coll de Nargó (32) ⚠️ | Coll de Nargó › Alt Urgell | 164 |
| Forêt de Montferrer i Castellbò (61) ⚠️ | Montferrer i Castellbò › Alt Urgell | 163 |
| Forêt de la Baronia de Rialb (18) ⚠️ | la Baronia de Rialb › Noguera | 162 |
| Forêt de Montferrer i Castellbò (82) ⚠️ | Montferrer i Castellbò › Alt Urgell | 162 |
| Forêt de les Valls d'Aguilar (17) ⚠️ | les Valls d'Aguilar › Alt Urgell | 161 |
| Forêt de Camarasa (27) ⚠️ | Camarasa › Noguera | 161 |
| Forêt de Estamariu (15) ⚠️ | Estamariu › Alt Urgell | 161 |
| Forêt de les Valls de Valira (5) ⚠️ | les Valls de Valira › Alt Urgell | 160 |
| Forêt de Vall de Cardós (18) ⚠️ | Vall de Cardós › Pallars Sobirà | 160 |
| Forêt de Sarroca de Bellera (22) ⚠️ | Sarroca de Bellera › Pallars Jussà | 160 |
| Forêt de Alins (32) ⚠️ | Alins › Pallars Sobirà | 160 |
| Forêt de Vilanova de Meià (4) ⚠️ | Vilanova de Meià › Noguera | 159 |
| Forêt de Lladurs (9) ⚠️ | Lladurs › Solsonès | 159 |
| Forêt de Riner (132) ⚠️ | Riner › Solsonès | 159 |
| Forêt de Farrera (19) ⚠️ | Farrera › Pallars Sobirà | 158 |
| Forêt de Lladurs (202) ⚠️ | Lladurs › Solsonès | 157 |
| Forêt de Soriguera (17) ⚠️ | Soriguera › Pallars Sobirà | 156 |
| Forêt de Montferrer i Castellbò (5) ⚠️ | Montferrer i Castellbò › Alt Urgell | 154 |
| Forêt de Gavet de la Conca (6) ⚠️ | Gavet de la Conca › Pallars Jussà | 154 |
| Forêt de Alins (22) ⚠️ | Alins › Pallars Sobirà | 154 |
| Forêt de Vielha e Mijaran (9) ⚠️ | Vielha e Mijaran › Val d'Aran | 153 |
| Forêt de el Pont de Suert (40) ⚠️ | el Pont de Suert › Alta Ribagorça | 153 |
| Forêt de Soriguera (28) ⚠️ | Soriguera › Pallars Sobirà | 153 |
| Forêt de Lladorre ⚠️ | Lladorre › Pallars Sobirà | 152 |
| Forêt de Llimiana (7) ⚠️ | Llimiana › Pallars Jussà | 152 |
| Forêt de Naut Aran (147) ⚠️ | Naut Aran › Val d'Aran | 152 |
| Forêt de Conca de Dalt (35) ⚠️ | Conca de Dalt › Pallars Jussà | 151 |
| Forêt de Farrera (10) ⚠️ | Farrera › Pallars Sobirà | 150 |
| Forêt de Naut Aran (105) ⚠️ | Naut Aran › Val d'Aran | 149 |
| Forêt de Espot (50) ⚠️ | Espot › Pallars Sobirà | 149 |
| Forêt de Tarrés (8) ⚠️ | Tarrés › Garrigues | 148 |
| Forêt de Ribera d'Urgellet ⚠️ | Ribera d'Urgellet › Alt Urgell | 147 |
| Forêt de Soriguera (6) ⚠️ | Soriguera › Pallars Sobirà | 147 |
| Forêt de Baix Pallars (18) ⚠️ | Baix Pallars › Pallars Sobirà | 147 |
| Forêt de Pinós (16) ⚠️ | Pinós › Solsonès | 147 |
| Forêt de Àger (30) ⚠️ | Àger › Noguera | 147 |
| Forêt de Coll de Nargó (84) ⚠️ | Coll de Nargó › Alt Urgell | 147 |
| Forêt de les Valls de Valira (84) ⚠️ | les Valls de Valira › Alt Urgell | 147 |
| Forêt de Conca de Dalt (20) ⚠️ | Conca de Dalt › Pallars Jussà | 146 |
| Forêt de Navès (34) ⚠️ | Navès › Solsonès | 146 |
| Forêt de Alàs i Cerc (11) ⚠️ | Alàs i Cerc › Alt Urgell | 146 |
| Forêt de Pinós (10) ⚠️ | Pinós › Solsonès | 145 |
| Forêt de Alòs de Balaguer (5) ⚠️ | Alòs de Balaguer › Noguera | 144 |
| Forêt de la Molsosa (20) ⚠️ | la Molsosa › Solsonès | 142 |
| Forêt de Montferrer i Castellbò ⚠️ | Montferrer i Castellbò › Alt Urgell | 141 |
| Forêt de Cava (14) ⚠️ | Cava › Alt Urgell | 141 |
| Forêt de Montferrer i Castellbò (98) ⚠️ | Montferrer i Castellbò › Alt Urgell | 141 |
| Forêt de Baix Pallars (5) ⚠️ | Baix Pallars › Pallars Sobirà | 140 |
| Forêt de Isona i Conca Dellà (31) ⚠️ | Isona i Conca Dellà › Pallars Jussà | 140 |
| Forêt de Salàs de Pallars ⚠️ | Salàs de Pallars › Pallars Jussà | 139 |
| Forêt de Àger (18) ⚠️ | Àger › Noguera | 139 |
| Forêt de Riner (134) ⚠️ | Riner › Solsonès | 139 |
| Forêt de Alàs i Cerc (31) ⚠️ | Alàs i Cerc › Alt Urgell | 139 |
| Forêt de Arres (6) ⚠️ | Arres › Val d'Aran | 138 |
| Forêt de les Valls d'Aguilar (7) ⚠️ | les Valls d'Aguilar › Alt Urgell | 137 |
| Forêt de Senterada (5) ⚠️ | Senterada › Pallars Jussà | 137 |
| Forêt de Os de Balaguer (69) ⚠️ | Os de Balaguer › Noguera | 137 |
| Forêt de Foradada (2) ⚠️ | Foradada › Noguera | 136 |
| Forêt de Alt Àneu (149) ⚠️ | Alt Àneu › Pallars Sobirà | 136 |
| Forêt de Alins (63) ⚠️ | Alins › Pallars Sobirà | 136 |
| Forêt de Abella de la Conca (37) ⚠️ | Abella de la Conca › Pallars Jussà | 136 |
| Forêt de les Valls de Valira (3) ⚠️ | les Valls de Valira › Alt Urgell | 135 |
| Forêt de Coll de Nargó (30) ⚠️ | Coll de Nargó › Alt Urgell | 135 |
| Forêt de Biosca ⚠️ | Biosca › Solsonès | 133 |
| Forêt de les Valls d'Aguilar (5) ⚠️ | les Valls d'Aguilar › Alt Urgell | 133 |
| Forêt de Cabó (6) ⚠️ | Cabó › Alt Urgell | 133 |
| Forêt de Canejan (4) ⚠️ | Canejan › Val d'Aran | 133 |
| Forêt de Torà (21) ⚠️ | Torà › Solsonès | 133 |
| Forêt de Canejan (11) ⚠️ | Canejan › Val d'Aran | 133 |
| Forêt de Lladurs (260) ⚠️ | Lladurs › Solsonès | 133 |
| Forêt de Lladurs (36) ⚠️ | Lladurs › Solsonès | 132 |
| Forêt de Sarroca de Bellera (24) ⚠️ | Sarroca de Bellera › Pallars Jussà | 132 |
| Forêt de Pinós (51) ⚠️ | Pinós › Solsonès | 132 |
| Forêt de el Pont de Suert (13) ⚠️ | el Pont de Suert › Alta Ribagorça | 131 |
| Forêt de Abella de la Conca ⚠️ | Abella de la Conca › Pallars Jussà | 129 |
| Forêt de les Valls de Valira (62) ⚠️ | les Valls de Valira › Alt Urgell | 129 |
| Forêt de Torà (34) ⚠️ | Torà › Solsonès | 129 |
| Forêt de les Valls de Valira (27) ⚠️ | les Valls de Valira › Alt Urgell | 128 |
| Forêt de la Guingueta d'Àneu (29) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 128 |
| Forêt de Montferrer i Castellbò (3) ⚠️ | Montferrer i Castellbò › Alt Urgell | 127 |
| Forêt de Juncosa (8) ⚠️ | Juncosa › Garrigues | 127 |
| Forêt de Ribera d'Urgellet (3) ⚠️ | Ribera d'Urgellet › Alt Urgell | 127 |
| Forêt de el Pont de Suert (9) ⚠️ | el Pont de Suert › Alta Ribagorça | 127 |
| Forêt de la Vall de Boí (252) ⚠️ | la Vall de Boí › Alta Ribagorça | 127 |
| Forêt de Abella de la Conca (17) ⚠️ | Abella de la Conca › Pallars Jussà | 127 |
| Forêt de Sarroca de Bellera ⚠️ | Sarroca de Bellera › Pallars Jussà | 126 |
| Forêt de la Granadella (14) ⚠️ | la Granadella › Garrigues | 126 |
| Forêt de Olius (310) ⚠️ | Olius › Solsonès | 126 |
| Forêt de Peramola (17) ⚠️ | Peramola › Alt Urgell | 126 |
| Forêt de Soriguera (13) | Soriguera › Pallars Sobirà | 125 |
| Forêt de Tiurana (2) | Tiurana › Noguera | 125 |
| Forêt de la Vall de Boí (251) | la Vall de Boí › Alta Ribagorça | 125 |
| Forêt de Llimiana (6) | Llimiana › Pallars Jussà | 124 |
| Forêt de Bassella (9) | Bassella › Alt Urgell | 124 |
| Forêt de Vilamòs (5) | Vilamòs › Val d'Aran | 124 |
| Forêt de la Pobla de Segur (33) | la Pobla de Segur › Pallars Jussà | 124 |
| Forêt de Cabó (38) | Cabó › Alt Urgell | 123 |
| Forêt de Soriguera (8) | Soriguera › Pallars Sobirà | 122 |
| Forêt de les Valls d'Aguilar (8) | les Valls d'Aguilar › Alt Urgell | 122 |
| Forêt de Gósol (8) | Gósol › Berguedà (Lérida) | 122 |
| Forêt de Gósol (53) | Gósol › Berguedà (Lérida) | 122 |
| Forêt de Cabó (27) | Cabó › Alt Urgell | 122 |
| Forêt de Odèn (41) | Odèn › Solsonès | 121 |
| Forêt de Artesa de Segre (16) | Artesa de Segre › Noguera | 120 |
| Forêt de Navès (44) | Navès › Solsonès | 120 |
| Forêt de Alàs i Cerc (38) | Alàs i Cerc › Alt Urgell | 120 |
| Forêt de Vilanova de Meià (2) | Vilanova de Meià › Noguera | 119 |
| Forêt de la Baronia de Rialb (28) | la Baronia de Rialb › Noguera | 119 |
| Forêt de Vilaller (35) | Vilaller › Alta Ribagorça | 119 |
| Forêt de la Guingueta d'Àneu (53) | la Guingueta d'Àneu › Pallars Sobirà | 119 |
| Forêt de Montferrer i Castellbò (42) | Montferrer i Castellbò › Alt Urgell | 119 |
| Forêt de la Guingueta d'Àneu (3) | la Guingueta d'Àneu › Pallars Sobirà | 118 |
| Forêt de la Baronia de Rialb (34) | la Baronia de Rialb › Noguera | 118 |
| Forêt de Ribera d'Urgellet (19) | Ribera d'Urgellet › Alt Urgell | 118 |
| Forêt de el Pont de Bar (42) | el Pont de Bar › Alt Urgell | 118 |
| Forêt de Tremp (32) | Tremp › Pallars Jussà | 117 |
| Forêt de la Baronia de Rialb (42) | la Baronia de Rialb › Noguera | 116 |
| Forêt de Montellà i Martinet (20) | Montellà i Martinet › Cerdanya (Lérida) | 116 |
| Forêt de la Vall de Boí (110) | la Vall de Boí › Alta Ribagorça | 115 |
| Forêt de Llavorsí (13) | Llavorsí › Pallars Sobirà | 115 |
| Forêt de Conca de Dalt (31) | Conca de Dalt › Pallars Jussà | 115 |
| Forêt de Os de Balaguer (61) | Os de Balaguer › Noguera | 115 |
| Forêt de les Avellanes i Santa Linya (6) | les Avellanes i Santa Linya › Noguera | 114 |
| Forêt de Àger (3) | Àger › Noguera | 114 |
| Forêt de Cubells | Cubells › Noguera | 114 |
| Forêt de Coll de Nargó (122) | Coll de Nargó › Alt Urgell | 114 |
| Forêt de el Pont de Suert (92) | el Pont de Suert › Alta Ribagorça | 114 |
| Forêt de les Valls d'Aguilar (19) | les Valls d'Aguilar › Alt Urgell | 113 |
| Forêt de Naut Aran (64) | Naut Aran › Val d'Aran | 113 |
| Forêt de Navès (126) | Navès › Solsonès | 113 |
| Forêt de el Pont de Suert (76) | el Pont de Suert › Alta Ribagorça | 113 |
| Forêt de Alins (79) | Alins › Pallars Sobirà | 113 |
| Forêt de Baix Pallars (83) | Baix Pallars › Pallars Sobirà | 113 |
| Forêt de Isona i Conca Dellà (3) | Isona i Conca Dellà › Pallars Jussà | 112 |
| Forêt de Àger (7) | Àger › Noguera | 112 |
| Forêt de Guixers (30) | Guixers › Solsonès | 112 |
| Forêt de la Torre de Cabdella (20) | la Torre de Cabdella › Pallars Jussà | 112 |
| Forêt de Pinós (81) | Pinós › Solsonès | 112 |
| Forêt de Estamariu (6) | Estamariu › Alt Urgell | 112 |
| Forêt de Torà (31) | Torà › Solsonès | 112 |
| Forêt de Conca de Dalt (3) | Conca de Dalt › Pallars Jussà | 111 |
| Forêt de Farrera (12) | Farrera › Pallars Sobirà | 111 |
| Forêt de Montellà i Martinet (50) | Montellà i Martinet › Cerdanya (Lérida) | 111 |
| Forêt de Gavet de la Conca (4) | Gavet de la Conca › Pallars Jussà | 110 |
| Forêt de Organyà (20) | Organyà › Alt Urgell | 110 |
| Forêt de Peramola (25) | Peramola › Alt Urgell | 110 |
| Forêt de Sant Esteve de la Sarga (34) | Sant Esteve de la Sarga › Pallars Jussà | 110 |
| Forêt de Os de Balaguer (35) | Os de Balaguer › Noguera | 110 |
| Forêt de Coll de Nargó (5) | Coll de Nargó › Alt Urgell | 109 |
| Forêt de Conca de Dalt (4) | Conca de Dalt › Pallars Jussà | 109 |
| Forêt de Alins (18) | Alins › Pallars Sobirà | 109 |
| Forêt de Guixers (37) | Guixers › Solsonès | 109 |
| Forêt de Montellà i Martinet (34) | Montellà i Martinet › Cerdanya (Lérida) | 109 |
| Forêt de Josa i Tuixén (22) | Josa i Tuixén › Alt Urgell | 109 |
| Forêt de el Pont de Suert (91) | el Pont de Suert › Alta Ribagorça | 108 |
| Forêt de Tremp (75) | Tremp › Pallars Jussà | 107 |
| Forêt de Montferrer i Castellbò (83) | Montferrer i Castellbò › Alt Urgell | 107 |
| Forêt de Llavorsí (2) | Llavorsí › Pallars Sobirà | 106 |
| Forêt de la Guingueta d'Àneu (14) | la Guingueta d'Àneu › Pallars Sobirà | 106 |
| Forêt de Cava (12) | Cava › Alt Urgell | 106 |
| Forêt de Guixers (107) | Guixers › Solsonès | 106 |
| Forêt de Lladurs (272) | Lladurs › Solsonès | 106 |
| Forêt de el Pont de Suert (45) | el Pont de Suert › Alta Ribagorça | 106 |
| Forêt de Alins (74) | Alins › Pallars Sobirà | 106 |
| Forêt de Pinell de Solsonès (35) | Pinell de Solsonès › Solsonès | 105 |
| Forêt de la Vansa i Fórnols (21) | la Vansa i Fórnols › Alt Urgell | 105 |
| Forêt de les Avellanes i Santa Linya (21) | les Avellanes i Santa Linya › Noguera | 105 |
| Forêt de Gósol (82) | Gósol › Berguedà (Lérida) | 105 |
| Forêt de les Valls d'Aguilar (31) | les Valls d'Aguilar › Alt Urgell | 105 |
| Forêt de les Valls d'Aguilar (21) | les Valls d'Aguilar › Alt Urgell | 104 |
| Forêt de Soriguera (19) | Soriguera › Pallars Sobirà | 104 |
| Forêt de Navès (49) | Navès › Solsonès | 104 |
| Forêt de Vielha e Mijaran (66) | Vielha e Mijaran › Val d'Aran | 104 |
| Forêt de la Baronia de Rialb (52) | la Baronia de Rialb › Noguera | 104 |
| Forêt de Biosca (9) | Biosca › Solsonès | 103 |
| Forêt de Pinell de Solsonès (25) | Pinell de Solsonès › Solsonès | 103 |
| Forêt de Almenar (3) | Almenar › Segrià | 103 |
| Forêt de Oliana (8) | Oliana › Alt Urgell | 103 |
| Forêt de Soriguera (46) | Soriguera › Pallars Sobirà | 103 |
| Forêt de Vall de Cardós (14) | Vall de Cardós › Pallars Sobirà | 102 |
| Forêt de Alt Àneu (30) | Alt Àneu › Pallars Sobirà | 102 |
| Forêt de Naut Aran (47) | Naut Aran › Val d'Aran | 102 |
| Forêt de la Guingueta d'Àneu (24) | la Guingueta d'Àneu › Pallars Sobirà | 102 |
| Forêt de Lles de Cerdanya (22) | Lles de Cerdanya › Cerdanya (Lérida) | 102 |
| Forêt de Lladorre (19) | Lladorre › Pallars Sobirà | 101 |
| Forêt de Alt Àneu (69) | Alt Àneu › Pallars Sobirà | 101 |
| Forêt de les Valls de Valira (89) | les Valls de Valira › Alt Urgell | 101 |
| Forêt de Isona i Conca Dellà (8) | Isona i Conca Dellà › Pallars Jussà | 100 |
| Forêt de Àger (19) | Àger › Noguera | 100 |
| Forêt de Josa i Tuixén (23) | Josa i Tuixén › Alt Urgell | 100 |
| Forêt de Lladorre (26) | Lladorre › Pallars Sobirà | 100 |
| Forêt de la Baronia de Rialb (8) | la Baronia de Rialb › Noguera | 99 |
| Forêt de el Pont de Suert (5) | el Pont de Suert › Alta Ribagorça | 99 |
| Forêt de Bassella (5) | Bassella › Alt Urgell | 99 |
| Forêt de les Avellanes i Santa Linya (5) | les Avellanes i Santa Linya › Noguera | 98 |
| Forêt de Vielha e Mijaran (41) | Vielha e Mijaran › Val d'Aran | 98 |
| Forêt de la Guingueta d'Àneu (57) | la Guingueta d'Àneu › Pallars Sobirà | 98 |
| Forêt de la Vall de Boí (267) | la Vall de Boí › Alta Ribagorça | 98 |
| Forêt de la Baronia de Rialb (5) | la Baronia de Rialb › Noguera | 97 |
| Forêt de Coll de Nargó (15) | Coll de Nargó › Alt Urgell | 97 |
| Forêt de Llavorsí (5) | Llavorsí › Pallars Sobirà | 97 |
| Forêt de Montellà i Martinet (15) | Montellà i Martinet › Cerdanya (Lérida) | 97 |
| Forêt de Sant Esteve de la Sarga (57) | Sant Esteve de la Sarga › Pallars Jussà | 97 |
| Forêt de Alt Àneu | Alt Àneu › Pallars Sobirà | 96 |
| Forêt de la Baronia de Rialb (38) | la Baronia de Rialb › Noguera | 96 |
| Forêt de Farrera (7) | Farrera › Pallars Sobirà | 96 |
| Forêt de Alins (93) | Alins › Pallars Sobirà | 96 |
| Forêt de Torà (37) | Torà › Solsonès | 96 |
| Forêt de Vinaixa (2) | Vinaixa › Garrigues | 95 |
| Forêt de Torà (12) | Torà › Solsonès | 95 |
| Forêt de Alt Àneu (37) | Alt Àneu › Pallars Sobirà | 95 |
| Forêt de Torà (23) | Torà › Solsonès | 95 |
| Forêt de Ribera d'Urgellet (48) | Ribera d'Urgellet › Alt Urgell | 95 |
| Forêt de Àger (45) | Àger › Noguera | 95 |
| Forêt de Tírvia (6) | Tírvia › Pallars Sobirà | 95 |
| Forêt de la Vall de Boí (2) | la Vall de Boí › Alta Ribagorça | 94 |
| Forêt de Ribera d'Urgellet (20) | Ribera d'Urgellet › Alt Urgell | 94 |
| Forêt de Guixers (31) | Guixers › Solsonès | 94 |
| Forêt de Llavorsí (4) | Llavorsí › Pallars Sobirà | 94 |
| Forêt de Cava (11) | Cava › Alt Urgell | 94 |
| Forêt de les Valls de Valira (49) | les Valls de Valira › Alt Urgell | 94 |
| Forêt de Bellver de Cerdanya (69) | Bellver de Cerdanya › Cerdanya (Lérida) | 94 |
| Forêt de el Pont de Bar (35) | el Pont de Bar › Alt Urgell | 94 |
| Forêt de Fígols i Alinyà | Fígols i Alinyà › Alt Urgell | 93 |
| Forêt de Lladurs (25) | Lladurs › Solsonès | 93 |
| Forêt de Senterada (6) | Senterada › Pallars Jussà | 93 |
| Forêt de la Guingueta d'Àneu (48) | la Guingueta d'Àneu › Pallars Sobirà | 93 |
| Forêt de la Pobla de Cérvoles (12) | la Pobla de Cérvoles › Garrigues | 92 |
| Forêt de el Pont de Suert (11) | el Pont de Suert › Alta Ribagorça | 92 |
| Forêt de Os de Balaguer (5) | Os de Balaguer › Noguera | 92 |
| Forêt de Vielha e Mijaran (12) | Vielha e Mijaran › Val d'Aran | 92 |
| Forêt de la Guingueta d'Àneu (51) | la Guingueta d'Àneu › Pallars Sobirà | 92 |
| Forêt de Conca de Dalt (29) | Conca de Dalt › Pallars Jussà | 92 |
| Forêt de el Pont de Bar (28) | el Pont de Bar › Alt Urgell | 92 |
| Forêt de el Pont de Bar (38) | el Pont de Bar › Alt Urgell | 92 |
| Forêt de Lladurs (278) | Lladurs › Solsonès | 92 |
| Forêt de la Torre de Cabdella (3) | la Torre de Cabdella › Pallars Jussà | 91 |
| Forêt de la Coma i la Pedra (94) | la Coma i la Pedra › Solsonès | 91 |
| Forêt de Naut Aran (102) | Naut Aran › Val d'Aran | 91 |
| Forêt de Llavorsí (39) | Llavorsí › Pallars Sobirà | 91 |
| Forêt de el Pont de Bar (10) | el Pont de Bar › Alt Urgell | 91 |
| Forêt de la Vansa i Fórnols (29) | la Vansa i Fórnols › Alt Urgell | 91 |
| Forêt de Baix Pallars (4) | Baix Pallars › Pallars Sobirà | 90 |
| Forêt de el Pont de Bar | el Pont de Bar › Alt Urgell | 90 |
| Forêt de la Vansa i Fórnols (19) | la Vansa i Fórnols › Alt Urgell | 90 |
| Forêt de Alàs i Cerc (10) | Alàs i Cerc › Alt Urgell | 90 |
| Forêt de Castellar de la Ribera (20) | Castellar de la Ribera › Solsonès | 90 |
| Forêt de Pinós (57) | Pinós › Solsonès | 90 |
| Forêt de Conca de Dalt (43) | Conca de Dalt › Pallars Jussà | 90 |
| Forêt de Senterada (15) | Senterada › Pallars Jussà | 90 |
| Forêt de el Pont de Bar (51) | el Pont de Bar › Alt Urgell | 90 |
| Forêt de Soriguera (3) | Soriguera › Pallars Sobirà | 89 |
| Forêt de Castell de Mur | Castell de Mur › Pallars Jussà | 89 |
| Forêt de Gósol (46) | Gósol › Berguedà (Lérida) | 89 |
| Forêt de Alins (54) | Alins › Pallars Sobirà | 89 |
| Forêt de Ribera d'Urgellet (49) | Ribera d'Urgellet › Alt Urgell | 89 |
| Forêt de Baix Pallars (78) | Baix Pallars › Pallars Sobirà | 89 |
| Forêt de Lladurs (274) | Lladurs › Solsonès | 89 |
| Forêt de la Pobla de Cérvoles (4) | la Pobla de Cérvoles › Garrigues | 88 |
| Bois de els Omells de na Gaia | els Omells de na Gaia › Urgell | 88 |
| Forêt de Lladurs (22) | Lladurs › Solsonès | 88 |
| Forêt de el Pont de Suert (17) | el Pont de Suert › Alta Ribagorça | 88 |
| Forêt de Lles de Cerdanya (10) | Lles de Cerdanya › Cerdanya (Lérida) | 88 |
| Forêt de Sant Esteve de la Sarga (8) | Sant Esteve de la Sarga › Pallars Jussà | 88 |
| Forêt de Lladurs (190) | Lladurs › Solsonès | 88 |
| Forêt de Conca de Dalt (39) | Conca de Dalt › Pallars Jussà | 88 |
| Forêt de Farrera (20) | Farrera › Pallars Sobirà | 88 |
| Forêt de Montferrer i Castellbò (99) | Montferrer i Castellbò › Alt Urgell | 88 |
| Forêt de Ribera d'Ondara | Ribera d'Ondara › Segarra | 87 |
| Forêt de Castell de Mur (4) | Castell de Mur › Pallars Jussà | 87 |
| Forêt de la Vall de Boí (247) | la Vall de Boí › Alta Ribagorça | 87 |
| Forêt de Castellar de la Ribera (26) | Castellar de la Ribera › Solsonès | 87 |
| Forêt de Cabó (37) | Cabó › Alt Urgell | 87 |
| Forêt de Clariana de Cardener (165) | Clariana de Cardener › Solsonès | 87 |
| Forêt de Montferrer i Castellbò (79) | Montferrer i Castellbò › Alt Urgell | 87 |
| Forêt de Llobera (484) | Llobera › Solsonès | 87 |
| Bois de Vallbona de les Monges (8) | Vallbona de les Monges › Urgell | 86 |
| Forêt de Alins (24) | Alins › Pallars Sobirà | 86 |
| Forêt de Cabó (44) | Cabó › Alt Urgell | 86 |
| Forêt de Coll de Nargó (101) | Coll de Nargó › Alt Urgell | 86 |
| Forêt de Arsèguel (8) | Arsèguel › Alt Urgell | 86 |
| Forêt de la Guingueta d'Àneu (52) | la Guingueta d'Àneu › Pallars Sobirà | 85 |
| Forêt de Montellà i Martinet (28) | Montellà i Martinet › Cerdanya (Lérida) | 85 |
| Forêt de Llavorsí (61) | Llavorsí › Pallars Sobirà | 85 |
| Forêt de Alàs i Cerc (20) | Alàs i Cerc › Alt Urgell | 85 |
| Forêt de Montferrer i Castellbò (94) | Montferrer i Castellbò › Alt Urgell | 85 |
| Forêt de Cervià de les Garrigues (3) | Cervià de les Garrigues › Garrigues | 84 |
| Forêt de Pinell de Solsonès (13) | Biosca › Solsonès | 84 |
| Forêt de Vall de Cardós (11) | Vall de Cardós › Pallars Sobirà | 84 |
| Forêt de Artesa de Segre (23) | Artesa de Segre › Noguera | 84 |
| Forêt de la Coma i la Pedra (123) | la Coma i la Pedra › Solsonès | 84 |
| Forêt de Llavorsí (41) | Llavorsí › Pallars Sobirà | 84 |
| Forêt de Baix Pallars (80) | Baix Pallars › Pallars Sobirà | 84 |
| Forêt de Cava (27) | Cava › Alt Urgell | 84 |
| Forêt de Montferrer i Castellbò (96) | Montferrer i Castellbò › Alt Urgell | 84 |
| Forêt de les Avellanes i Santa Linya (8) | les Avellanes i Santa Linya › Noguera | 83 |
| Forêt de Camarasa (18) | Camarasa › Noguera | 83 |
| Forêt de Alins (73) | Alins › Pallars Sobirà | 83 |
| Forêt de la Baronia de Rialb (30) | la Baronia de Rialb › Noguera | 82 |
| Forêt de Lladurs (170) | Lladurs › Solsonès | 82 |
| Forêt de Odèn (28) | Odèn › Solsonès | 82 |
| Forêt de Vielha e Mijaran (67) | Vielha e Mijaran › Val d'Aran | 82 |
| Forêt de Lladurs (266) | Lladurs › Solsonès | 82 |
| Forêt de les Valls de Valira (129) | les Valls de Valira › Alt Urgell | 82 |
| Forêt de la Vall de Boí (278) | la Vall de Boí › Alta Ribagorça | 82 |
| Forêt de la Vall de Boí (3) | la Vall de Boí › Alta Ribagorça | 81 |
| Forêt de Maials (13) | Maials › Segrià | 81 |
| Forêt de Maials (18) | Maials › Segrià | 81 |
| Forêt de Coll de Nargó (41) | Coll de Nargó › Alt Urgell | 81 |
| Forêt de Os de Balaguer (25) | Os de Balaguer › Noguera | 81 |
| Forêt de la Torre de Cabdella (23) | la Torre de Cabdella › Pallars Jussà | 81 |
| Forêt de Vilanova de l'Aguda (6) | Vilanova de l'Aguda › Noguera | 81 |
| Forêt de Ponts (10) | Ponts › Noguera | 81 |
| Forêt de Sant Esteve de la Sarga (54) | Sant Esteve de la Sarga › Pallars Jussà | 81 |
| Forêt de Àger (104) | Àger › Noguera | 81 |
| Forêt de Coll de Nargó (111) | Coll de Nargó › Alt Urgell | 81 |
| Bois de Fulleda (2) | Fulleda › Garrigues | 80 |
| Forêt de Navès (36) | Navès › Solsonès | 80 |
| Forêt de Vielha e Mijaran (49) | Vielha e Mijaran › Val d'Aran | 80 |
| Forêt de Navès (108) | Navès › Solsonès | 80 |
| Forêt de Gósol (60) | Gósol › Berguedà (Lérida) | 80 |
| Forêt de Rialp (19) | Rialp › Pallars Sobirà | 80 |
| Forêt de les Valls de Valira (47) | les Valls de Valira › Alt Urgell | 80 |
| Forêt de Sant Esteve de la Sarga (48) | Sant Esteve de la Sarga › Pallars Jussà | 80 |
| Forêt de Farrera (13) | Farrera › Pallars Sobirà | 80 |
| Forêt de Tremp (19) | Tremp › Pallars Jussà | 79 |
| Forêt de Baix Pallars (21) | Baix Pallars › Pallars Sobirà | 79 |
| Forêt de Lles de Cerdanya (17) | Lles de Cerdanya › Cerdanya (Lérida) | 79 |
| Forêt de Fígols i Alinyà (13) | Fígols i Alinyà › Alt Urgell | 79 |
| Forêt de Naut Aran (114) | Naut Aran › Val d'Aran | 79 |
| Forêt de Tremp (3) | Tremp › Pallars Jussà | 78 |
| Forêt de Artesa de Segre (4) | Artesa de Segre › Noguera | 78 |
| Forêt de la Vansa i Fórnols (4) | la Vansa i Fórnols › Alt Urgell | 78 |
| Forêt de les Valls d'Aguilar (16) | les Valls d'Aguilar › Alt Urgell | 78 |
| Forêt de Lladurs (32) | Lladurs › Solsonès | 78 |
| Forêt de Os de Balaguer (7) | Os de Balaguer › Noguera | 78 |
| Forêt de Josa i Tuixén (43) | Josa i Tuixén › Alt Urgell | 78 |
| Forêt de Castellar de la Ribera | Castellar de la Ribera › Solsonès | 77 |
| Forêt de Baix Pallars (7) | Baix Pallars › Pallars Sobirà | 77 |
| Forêt de Odèn (8) | Odèn › Solsonès | 77 |
| Forêt de les Valls de Valira (36) | les Valls de Valira › Alt Urgell | 77 |
| Forêt de Alins (52) | Alins › Pallars Sobirà | 77 |
| Forêt de Ribera d'Urgellet (33) | Ribera d'Urgellet › Alt Urgell | 76 |
| Forêt de Ribera d'Urgellet (53) | Ribera d'Urgellet › Alt Urgell | 76 |
| Forêt de les Avellanes i Santa Linya (17) | les Avellanes i Santa Linya › Noguera | 75 |
| Forêt de Torà (24) | Torà › Solsonès | 75 |
| Forêt de Alins (101) | Alins › Pallars Sobirà | 75 |
| Forêt de Fígols i Alinyà (2) | Fígols i Alinyà › Alt Urgell | 74 |
| Forêt de Os de Balaguer (22) | Os de Balaguer › Noguera | 74 |
| Forêt de les Valls de Valira (26) | les Valls de Valira › Alt Urgell | 74 |
| Forêt de Farrera (26) | Farrera › Pallars Sobirà | 74 |
| Forêt de Vall de Cardós (4) | Vall de Cardós › Pallars Sobirà | 73 |
| Forêt de Tremp (15) | Tremp › Pallars Jussà | 73 |
| Forêt de Coll de Nargó (14) | Coll de Nargó › Alt Urgell | 73 |
| Forêt de Alàs i Cerc (3) | Alàs i Cerc › Alt Urgell | 73 |
| Forêt de Alt Àneu (152) | Alt Àneu › Pallars Sobirà | 73 |
| Forêt de Àger (105) | Àger › Noguera | 73 |
| Forêt de Farrera (25) | Farrera › Pallars Sobirà | 73 |
| Forêt de Artesa de Segre (18) | Artesa de Segre › Noguera | 72 |
| Forêt de les Avellanes i Santa Linya (14) | les Avellanes i Santa Linya › Noguera | 72 |
| Forêt de Alins (29) | Alins › Pallars Sobirà | 72 |
| Forêt de la Baronia de Rialb (23) | la Baronia de Rialb › Noguera | 71 |
| Forêt de la Torre de Cabdella (10) | la Torre de Cabdella › Pallars Jussà | 71 |
| Forêt de Montellà i Martinet (25) | Montellà i Martinet › Cerdanya (Lérida) | 71 |
| Forêt de Sort (20) | Sort › Pallars Sobirà | 71 |
| Forêt de Os de Balaguer (56) | Os de Balaguer › Noguera | 71 |
| Forêt de Ivars de Noguera (18) | Ivars de Noguera › Noguera | 71 |
| Forêt de Conca de Dalt (40) | Conca de Dalt › Pallars Jussà | 71 |
| Forêt de Tremp (5) | Tremp › Pallars Jussà | 70 |
| Forêt de Alt Àneu (5) | Alt Àneu › Pallars Sobirà | 70 |
| Forêt de Alt Àneu (151) | Alt Àneu › Pallars Sobirà | 70 |
| Forêt de Alins (66) | Alins › Pallars Sobirà | 70 |
| Forêt de Abella de la Conca (78) | Abella de la Conca › Pallars Jussà | 70 |
| Forêt de Tremp (117) | Tremp › Pallars Jussà | 70 |
| Forêt de Torà (35) | Torà › Solsonès | 70 |
| Forêt de Os de Balaguer (3) | Os de Balaguer › Noguera | 69 |
| Forêt de el Pont de Suert (31) | el Pont de Suert › Alta Ribagorça | 69 |
| Forêt de les Valls de Valira (15) | les Valls de Valira › Alt Urgell | 69 |
| Forêt de Àger (17) | Àger › Noguera | 69 |
| Forêt de Naut Aran (51) | Naut Aran › Val d'Aran | 69 |
| Forêt de Vilamòs (2) | Vilamòs › Val d'Aran | 69 |
| Forêt de Navès (138) | Navès › Solsonès | 69 |
| Forêt de Vielha e Mijaran (54) | Vielha e Mijaran › Val d'Aran | 69 |
| Forêt de Alt Àneu (51) | Alt Àneu › Pallars Sobirà | 69 |
| Forêt de Montellà i Martinet (22) | Montellà i Martinet › Cerdanya (Lérida) | 69 |
| Forêt de Vinaixa (3) | Vinaixa › Garrigues | 68 |
| Forêt de Lladurs (180) | Lladurs › Solsonès | 68 |
| Forêt de Montferrer i Castellbò (32) | Montferrer i Castellbò › Alt Urgell | 68 |
| Forêt de Alins (46) | Alins › Pallars Sobirà | 68 |
| Forêt de Ribera d'Urgellet (54) | Ribera d'Urgellet › Alt Urgell | 68 |
| Forêt de Sant Esteve de la Sarga (59) | Sant Esteve de la Sarga › Pallars Jussà | 68 |
| Forêt de Montferrer i Castellbò (90) | Montferrer i Castellbò › Alt Urgell | 68 |
| Forêt de Alins (72) | Alins › Pallars Sobirà | 68 |
| Forêt de les Valls de Valira (150) | les Valls de Valira › Alt Urgell | 68 |
| Forêt de Isona i Conca Dellà (2) | Isona i Conca Dellà › Pallars Jussà | 67 |
| Forêt de la Torre de Cabdella (4) | la Torre de Cabdella › Pallars Jussà | 67 |
| Forêt de Pinell de Solsonès (14) | Pinell de Solsonès › Solsonès | 67 |
| Forêt de les Valls d'Aguilar (12) | les Valls d'Aguilar › Alt Urgell | 67 |
| Forêt de la Torre de Cabdella (8) | la Torre de Cabdella › Pallars Jussà | 67 |
| Forêt de Pinell de Solsonès (21) | Pinell de Solsonès › Solsonès | 67 |
| Forêt de Navès (45) | Navès › Solsonès | 67 |
| Forêt de Odèn (58) | Odèn › Solsonès | 67 |
| Forêt de Vielha e Mijaran (62) | Vielha e Mijaran › Val d'Aran | 67 |
| Forêt de Montferrer i Castellbò (56) | Montferrer i Castellbò › Alt Urgell | 67 |
| Forêt de Lladurs (271) | Lladurs › Solsonès | 67 |
| Forêt de Coll de Nargó (114) | Coll de Nargó › Alt Urgell | 67 |
| Forêt de Maials (5) | Maials › Segrià | 66 |
| Forêt de Pinós (3) | Pinós › Solsonès | 66 |
| Forêt de Cava (2) | Cava › Alt Urgell | 66 |
| Forêt de Alòs de Balaguer (2) | Alòs de Balaguer › Noguera | 66 |
| Forêt de Camarasa (12) | Camarasa › Noguera | 66 |
| Forêt de les Valls de Valira (33) | les Valls de Valira › Alt Urgell | 66 |
| Forêt de la Guingueta d'Àneu (54) | la Guingueta d'Àneu › Pallars Sobirà | 66 |
| Forêt de Bellver de Cerdanya (34) | Bellver de Cerdanya › Cerdanya (Lérida) | 66 |
| Forêt de Bellver de Cerdanya (51) | Bellver de Cerdanya › Cerdanya (Lérida) | 66 |
| Forêt de Vielha e Mijaran (65) | Vielha e Mijaran › Val d'Aran | 66 |
| Forêt de Montferrer i Castellbò (85) | Montferrer i Castellbò › Alt Urgell | 66 |
| Forêt de Montferrer i Castellbò (86) | Montferrer i Castellbò › Alt Urgell | 66 |
| Forêt de Sanaüja | Sanaüja › Segarra | 65 |
| Forêt de Vilaller (6) | Vilaller › Alta Ribagorça | 65 |
| Forêt de Coll de Nargó (21) | Coll de Nargó › Alt Urgell | 65 |
| Forêt de Lles de Cerdanya (16) | Lles de Cerdanya › Cerdanya (Lérida) | 65 |
| Forêt de Naut Aran (107) | Naut Aran › Val d'Aran | 65 |
| Forêt de Lladurs (257) | Lladurs › Solsonès | 65 |
| Forêt de Espot (58) | Espot › Pallars Sobirà | 65 |
| Forêt de Ribera d'Urgellet (5) | Ribera d'Urgellet › Alt Urgell | 64 |
| Forêt de Vilanova de Meià (12) | Vilanova de Meià › Noguera | 64 |
| Forêt de Conca de Dalt (13) | Conca de Dalt › Pallars Jussà | 64 |
| Forêt de Odèn (7) | Odèn › Solsonès | 64 |
| Forêt de la Baronia de Rialb (35) | la Baronia de Rialb › Noguera | 64 |
| Forêt de Baix Pallars (31) | Baix Pallars › Pallars Sobirà | 64 |
| Forêt de Rialp (8) | Rialp › Pallars Sobirà | 64 |
| Forêt de Gósol (54) | Gósol › Berguedà (Lérida) | 64 |
| Forêt de Tremp (115) | Tremp › Pallars Jussà | 64 |
| Forêt de Lles de Cerdanya (27) | Lles de Cerdanya › Cerdanya (Lérida) | 64 |
| Forêt de Soriguera (18) | Soriguera › Pallars Sobirà | 63 |
| Forêt de Gósol (7) | Gósol › Berguedà (Lérida) | 63 |
| Forêt de Talarn (2) | Talarn › Pallars Jussà | 63 |
| Forêt de Bellver de Cerdanya (14) | Bellver de Cerdanya › Cerdanya (Lérida) | 63 |
| Forêt de Gósol (19) | Gósol › Berguedà (Lérida) | 63 |
| Forêt de Guixers (61) | Guixers › Solsonès | 63 |
| Forêt de la Vall de Boí (264) | la Vall de Boí › Alta Ribagorça | 63 |
| Forêt de Pinós | Pinós › Solsonès | 62 |
| Bois de Vallbona de les Monges (7) | Vallbona de les Monges › Urgell | 62 |
| Forêt de Vilanova de Meià (10) | Vilanova de Meià › Noguera | 62 |
| Forêt de Tremp (46) | Tremp › Pallars Jussà | 62 |
| Forêt de Navès (32) | Navès › Solsonès | 62 |
| Forêt de Navès (54) | Navès › Solsonès | 62 |
| Forêt de Odèn (59) | Odèn › Solsonès | 62 |
| Forêt de les Valls de Valira (25) | les Valls de Valira › Alt Urgell | 62 |
| Forêt de Alt Àneu (74) | Alt Àneu › Pallars Sobirà | 62 |
| Forêt de Llimiana (14) | Llimiana › Pallars Jussà | 62 |
| Forêt de Pinós (44) | Pinós › Solsonès | 61 |
| Forêt de Fígols i Alinyà (30) | Fígols i Alinyà › Alt Urgell | 61 |
| Forêt de Rialp (26) | Rialp › Pallars Sobirà | 61 |
| Forêt de Àger (91) | Àger › Noguera | 61 |
| Forêt de el Pont de Bar (34) | el Pont de Bar › Alt Urgell | 61 |
| Forêt de Torà | Torà › Solsonès | 60 |
| Forêt de Odèn (4) | Odèn › Solsonès | 60 |
| Forêt de Baix Pallars (16) | Baix Pallars › Pallars Sobirà | 60 |
| Forêt de Coll de Nargó (13) | Coll de Nargó › Alt Urgell | 60 |
| Forêt de la Baronia de Rialb (37) | la Baronia de Rialb › Noguera | 60 |
| Forêt de Alàs i Cerc (9) | Alàs i Cerc › Alt Urgell | 60 |
| Forêt de la Torre de Cabdella (19) | la Torre de Cabdella › Pallars Jussà | 60 |
| Forêt de Es Bòrdes (3) | Es Bòrdes › Val d'Aran | 60 |
| Forêt de Coll de Nargó (69) | Coll de Nargó › Alt Urgell | 60 |
| Forêt de Lladurs (178) | Lladurs › Solsonès | 60 |
| Forêt de Olius (326) | Olius › Solsonès | 60 |
| Forêt de Alt Àneu (57) | Alt Àneu › Pallars Sobirà | 60 |
| Forêt de Gósol (47) | Gósol › Berguedà (Lérida) | 60 |
| Forêt de la Coma i la Pedra (161) | la Coma i la Pedra › Solsonès | 60 |
| Forêt de l'Albi | l'Albi › Garrigues | 59 |
| Forêt de les Avellanes i Santa Linya (3) | les Avellanes i Santa Linya › Noguera | 59 |
| Forêt de Camarasa (11) | Camarasa › Noguera | 59 |
| Forêt de Isona i Conca Dellà (27) | Isona i Conca Dellà › Pallars Jussà | 59 |
| Forêt de Odèn (50) | Odèn › Solsonès | 59 |
| Forêt de Montellà i Martinet (14) | Montellà i Martinet › Cerdanya (Lérida) | 59 |
| Forêt de Montellà i Martinet (19) | Montellà i Martinet › Cerdanya (Lérida) | 59 |
| Forêt de Naut Aran (141) | Naut Aran › Val d'Aran | 59 |
| Forêt de Montferrer i Castellbò (64) | Montferrer i Castellbò › Alt Urgell | 59 |
| Forêt de el Pont de Suert (81) | el Pont de Suert › Alta Ribagorça | 59 |
| Forêt de Arsèguel (11) | Arsèguel › Alt Urgell | 59 |
| Forêt de el Pont de Bar (41) | el Pont de Bar › Alt Urgell | 59 |
| Forêt de el Pont de Suert | el Pont de Suert › Alta Ribagorça | 58 |
| Forêt de Juncosa (3) | Juncosa › Garrigues | 58 |
| Forêt de Oliola (4) | Oliola › Noguera | 58 |
| Forêt de Lles de Cerdanya (3) | Lles de Cerdanya › Cerdanya (Lérida) | 58 |
| Forêt de Almatret (2) | Almatret › Segrià | 58 |
| Forêt de Sarroca de Bellera (4) | Sarroca de Bellera › Pallars Jussà | 58 |
| Forêt de el Pont de Bar (3) | el Pont de Bar › Alt Urgell | 58 |
| Forêt de Navès (139) | Navès › Solsonès | 58 |
| Forêt de Montferrer i Castellbò (31) | Montferrer i Castellbò › Alt Urgell | 58 |
| Forêt de Montellà i Martinet (30) | Montellà i Martinet › Cerdanya (Lérida) | 58 |
| Forêt de Lladurs (203) | Lladurs › Solsonès | 58 |
| Forêt de Naut Aran (97) | Naut Aran › Val d'Aran | 58 |
| Forêt de Fígols i Alinyà (33) | Fígols i Alinyà › Alt Urgell | 58 |
| Forêt de el Pont de Bar (13) | el Pont de Bar › Alt Urgell | 58 |
| Forêt de Lladurs (19) | Lladurs › Solsonès | 57 |
| Forêt de Conca de Dalt (11) | Conca de Dalt › Pallars Jussà | 57 |
| Forêt de la Pobla de Segur (6) | la Pobla de Segur › Pallars Jussà | 57 |
| Forêt de Ivars de Noguera (7) | Ivars de Noguera › Noguera | 57 |
| Forêt de Olius (318) | Olius › Solsonès | 57 |
| Forêt de Ribera d'Urgellet (37) | Ribera d'Urgellet › Alt Urgell | 57 |
| Forêt de Lles de Cerdanya (25) | Lles de Cerdanya › Cerdanya (Lérida) | 57 |
| Forêt de Conca de Dalt (30) | Conca de Dalt › Pallars Jussà | 57 |
| Forêt de Baix Pallars (79) | Baix Pallars › Pallars Sobirà | 57 |
| Forêt de Alins (78) | Alins › Pallars Sobirà | 57 |
| Forêt de les Valls de Valira (145) | les Valls de Valira › Alt Urgell | 57 |
| Forêt de Alins | Alins › Pallars Sobirà | 56 |
| Forêt de la Baronia de Rialb (7) | la Baronia de Rialb › Noguera | 56 |
| Forêt de Peramola | Peramola › Alt Urgell | 56 |
| Forêt de la Baronia de Rialb (27) | la Baronia de Rialb › Noguera | 56 |
| Forêt de Corbins (3) | Corbins › Segrià | 56 |
| Forêt de Navès (135) | Navès › Solsonès | 56 |
| Forêt de Llavorsí (12) | Llavorsí › Pallars Sobirà | 56 |
| Forêt de Montferrer i Castellbò (33) | Montferrer i Castellbò › Alt Urgell | 56 |
| Forêt de Prats i Sansor (6) | Prats i Sansor › Cerdanya (Lérida) | 56 |
| Forêt de el Pont de Bar (39) | el Pont de Bar › Alt Urgell | 56 |
| Forêt de Montellà i Martinet | Montellà i Martinet › Cerdanya (Lérida) | 55 |
| Forêt de Vall de Cardós (13) | Vall de Cardós › Pallars Sobirà | 55 |
| Forêt de Peramola (6) | Peramola › Alt Urgell | 55 |
| Forêt de Gósol (6) | Gósol › Berguedà (Lérida) | 55 |
| Forêt de Tremp (74) | Tremp › Pallars Jussà | 55 |
| Forêt de Coll de Nargó (33) | Coll de Nargó › Alt Urgell | 55 |
| Forêt de Navès (41) | Navès › Solsonès | 55 |
| Forêt de Ivars de Noguera (8) | Ivars de Noguera › Noguera | 55 |
| Forêt de la Coma i la Pedra (108) | la Coma i la Pedra › Solsonès | 55 |
| Forêt de Navès (76) | Navès › Solsonès | 55 |
| Forêt de Navès (133) | Navès › Solsonès | 55 |
| Forêt de Navès (136) | Navès › Solsonès | 55 |
| Forêt de Llavorsí (8) | Llavorsí › Pallars Sobirà | 55 |
| Forêt de Llavorsí (14) | Llavorsí › Pallars Sobirà | 55 |
| Forêt de Lladorre (31) | Lladorre › Pallars Sobirà | 55 |
| Forêt de les Valls de Valira (128) | les Valls de Valira › Alt Urgell | 55 |
| Forêt de Lladorre (55) | Lladorre › Pallars Sobirà | 55 |
| Forêt de Tremp (24) | Tremp › Pallars Jussà | 54 |
| Forêt de Artesa de Segre (14) | Artesa de Segre › Noguera | 54 |
| Forêt de Navès (47) | Navès › Solsonès | 54 |
| Forêt de la Coma i la Pedra (152) | la Coma i la Pedra › Solsonès | 54 |
| Forêt de Llavorsí (51) | Llavorsí › Pallars Sobirà | 54 |
| Forêt de la Seu d'Urgell (17) | la Seu d'Urgell › Alt Urgell | 54 |
| Forêt de Montferrer i Castellbò (78) | Montferrer i Castellbò › Alt Urgell | 54 |
| Forêt de Tremp (107) | Tremp › Pallars Jussà | 54 |
| Forêt de Montferrer i Castellbò (16) | Montferrer i Castellbò › Alt Urgell | 53 |
| Forêt de Guixers (21) | Guixers › Solsonès | 53 |
| Forêt de Odèn (32) | Odèn › Solsonès | 53 |
| Forêt de Vilaller (24) | Vilaller › Alta Ribagorça | 53 |
| Forêt de Farrera (9) | Farrera › Pallars Sobirà | 53 |
| Forêt de Bellver de Cerdanya (29) | Bellver de Cerdanya › Cerdanya (Lérida) | 53 |
| Forêt de Montellà i Martinet (26) | Montellà i Martinet › Cerdanya (Lérida) | 53 |
| Forêt de la Coma i la Pedra (159) | la Coma i la Pedra › Solsonès | 53 |
| Forêt de les Valls de Valira (133) | les Valls de Valira › Alt Urgell | 53 |
| Forêt de Montferrer i Castellbò (122) | Montferrer i Castellbò › Alt Urgell | 53 |
| Forêt de la Torre de Cabdella (6) | la Torre de Cabdella › Pallars Jussà | 52 |
| Forêt de les Valls de Valira (6) | les Valls de Valira › Alt Urgell | 52 |
| Forêt de Alins (8) | Alins › Pallars Sobirà | 52 |
| Forêt de Senterada (4) | Senterada › Pallars Jussà | 52 |
| Forêt de Isona i Conca Dellà (11) | Isona i Conca Dellà › Pallars Jussà | 52 |
| Forêt de Os de Balaguer (15) | Os de Balaguer › Noguera | 52 |
| Forêt de Peramola (11) | Peramola › Alt Urgell | 52 |
| Forêt de Alt Àneu (31) | Alt Àneu › Pallars Sobirà | 52 |
| Forêt de Vielha e Mijaran (40) | Vielha e Mijaran › Val d'Aran | 52 |
| Forêt de la Guingueta d'Àneu (68) | la Guingueta d'Àneu › Pallars Sobirà | 52 |
| Forêt de Montferrer i Castellbò (36) | Montferrer i Castellbò › Alt Urgell | 52 |
| Forêt de Riu de Cerdanya (19) | Riu de Cerdanya › Cerdanya (Lérida) | 52 |
| Forêt de Montellà i Martinet (21) | Montellà i Martinet › Cerdanya (Lérida) | 52 |
| Forêt de Gósol (55) | Gósol › Berguedà (Lérida) | 52 |
| Forêt de Gósol (63) | Gósol › Berguedà (Lérida) | 52 |
| Forêt de Alt Àneu (70) | Alt Àneu › Pallars Sobirà | 52 |
| Forêt de Montellà i Martinet (47) | Montellà i Martinet › Cerdanya (Lérida) | 52 |
| Forêt de Baix Pallars (51) | Baix Pallars › Pallars Sobirà | 52 |
| Forêt de Montferrer i Castellbò (108) | Montferrer i Castellbò › Alt Urgell | 52 |
| Forêt de Montferrer i Castellbò (121) | Montferrer i Castellbò › Alt Urgell | 52 |
| Forêt de Artesa de Segre (3) | Artesa de Segre › Noguera | 51 |
| Forêt de Alòs de Balaguer | Alòs de Balaguer › Noguera | 51 |
| Forêt de la Torre de Cabdella (7) | la Torre de Cabdella › Pallars Jussà | 51 |
| Forêt de la Baronia de Rialb (25) | la Baronia de Rialb › Noguera | 51 |
| Forêt de Lladurs (28) | Lladurs › Solsonès | 51 |
| Forêt de la Vansa i Fórnols (12) | la Vansa i Fórnols › Alt Urgell | 51 |
| Forêt de Os de Balaguer (6) | Os de Balaguer › Noguera | 51 |
| Forêt de Gósol (9) | Gósol › Berguedà (Lérida) | 51 |
| Forêt de Llimiana (5) | Llimiana › Pallars Jussà | 51 |
| Forêt de Fígols i Alinyà (22) | Fígols i Alinyà › Alt Urgell | 51 |
| Forêt de Farrera (8) | Farrera › Pallars Sobirà | 51 |
| Forêt de Josa i Tuixén (17) | Josa i Tuixén › Alt Urgell | 51 |
| Forêt de les Valls de Valira (101) | les Valls de Valira › Alt Urgell | 51 |
| Forêt de Lladurs (258) | Lladurs › Solsonès | 51 |
| Forêt de Lladurs (268) | Lladurs › Solsonès | 51 |
| Forêt de Àger (92) | Àger › Noguera | 51 |
| Forêt de Àger (185) | Àger › Noguera | 51 |
| Forêt de Alàs i Cerc (21) | Alàs i Cerc › Alt Urgell | 51 |
| Forêt de Odèn | Odèn › Solsonès | 50 |
| Forêt de Isona i Conca Dellà (5) | Isona i Conca Dellà › Pallars Jussà | 50 |
| Forêt de Oliola (7) | Oliola › Noguera | 50 |
| Forêt de Castellar de la Ribera (9) | Castellar de la Ribera › Solsonès | 50 |
| Forêt de Sort (3) | Sort › Pallars Sobirà | 50 |
| Forêt de el Pont de Suert (12) | el Pont de Suert › Alta Ribagorça | 50 |
| Forêt de les Valls de Valira (32) | les Valls de Valira › Alt Urgell | 50 |
| Forêt de Gósol (48) | Gósol › Berguedà (Lérida) | 50 |
| Forêt de Naut Aran (116) | Naut Aran › Val d'Aran | 50 |
| Forêt de Naut Aran (129) | Naut Aran › Val d'Aran | 50 |
| Forêt de les Valls de Valira (46) | les Valls de Valira › Alt Urgell | 50 |
| Forêt de les Valls de Valira (93) | les Valls de Valira › Alt Urgell | 50 |
| Forêt de Oliola (10) | Ponts › Noguera | 50 |
| Forêt de Coll de Nargó (106) | Coll de Nargó › Alt Urgell | 50 |
| Forêt de la Guingueta d'Àneu (89) | la Guingueta d'Àneu › Pallars Sobirà | 50 |
| Forêt de Montferrer i Castellbò (103) | Montferrer i Castellbò › Alt Urgell | 50 |
| Forêt de Lladorre (47) | Lladorre › Pallars Sobirà | 50 |
| Forêt de les Valls d'Aguilar (14) | les Valls d'Aguilar › Alt Urgell | 49 |
| Forêt de Isona i Conca Dellà (15) | Isona i Conca Dellà › Pallars Jussà | 49 |
| Forêt de Torà (10) | Torà › Solsonès | 49 |
| Forêt de Oliana (4) | Oliana › Alt Urgell | 49 |
| Forêt de Bellver de Cerdanya (46) | Bellver de Cerdanya › Cerdanya (Lérida) | 49 |
| Forêt de Odèn (87) | Odèn › Solsonès | 49 |
| Forêt de Canejan (23) | Canejan › Val d'Aran | 49 |
| Forêt de Baix Pallars (48) | Baix Pallars › Pallars Sobirà | 49 |
| Forêt de Coll de Nargó (123) | Coll de Nargó › Alt Urgell | 49 |
| Forêt de Tremp (108) | Tremp › Pallars Jussà | 49 |
| Forêt de el Pont de Bar (37) | el Pont de Bar › Alt Urgell | 49 |
| Forêt de Baix Pallars (6) | Baix Pallars › Pallars Sobirà | 48 |
| Forêt de Vilanova de Meià (6) | Vilanova de Meià › Noguera | 48 |
| Forêt de Castellar de la Ribera (10) | Castellar de la Ribera › Solsonès | 48 |
| Forêt de la Pobla de Cérvoles (13) | la Pobla de Cérvoles › Garrigues | 48 |
| Forêt de Montferrer i Castellbò (21) | Montferrer i Castellbò › Alt Urgell | 48 |
| Forêt de Sort (7) | Sort › Pallars Sobirà | 48 |
| Forêt de Baix Pallars (29) | Baix Pallars › Pallars Sobirà | 48 |
| Forêt de Alins (21) | Alins › Pallars Sobirà | 48 |
| Forêt de la Vall de Boí (249) | la Vall de Boí › Alta Ribagorça | 48 |
| Forêt de Naut Aran (66) | Naut Aran › Val d'Aran | 48 |
| Forêt de les Valls d'Aguilar (30) | les Valls d'Aguilar › Alt Urgell | 48 |
| Forêt de Lladurs (235) | Lladurs › Solsonès | 48 |
| Forêt de Alt Àneu (121) | Alt Àneu › Pallars Sobirà | 48 |
| Forêt de Canejan (12) | Canejan › Val d'Aran | 48 |
| Forêt de les Valls de Valira (61) | les Valls de Valira › Alt Urgell | 48 |
| Forêt de Vilanova de Meià (18) | Vilanova de Meià › Noguera | 48 |
| Forêt de Os de Balaguer (46) | Os de Balaguer › Noguera | 48 |
| Forêt de les Valls d'Aguilar (35) | les Valls d'Aguilar › Alt Urgell | 48 |
| Forêt de Llavorsí (59) | Llavorsí › Pallars Sobirà | 48 |
| Forêt de Llavorsí (60) | Llavorsí › Pallars Sobirà | 48 |
| Forêt de Arsèguel (17) | Arsèguel › Alt Urgell | 48 |
| Forêt de Lles de Cerdanya (32) | Lles de Cerdanya › Cerdanya (Lérida) | 48 |
| Forêt de Montferrer i Castellbò (97) | Montferrer i Castellbò › Alt Urgell | 48 |
| Forêt de Alàs i Cerc (41) | Alàs i Cerc › Alt Urgell | 48 |
| Forêt de Vall de Cardós (2) | Vall de Cardós › Pallars Sobirà | 47 |
| Forêt de Tremp (6) | Tremp › Pallars Jussà | 47 |
| Forêt de la Granadella (2) | la Granadella › Garrigues | 47 |
| Forêt de Juncosa (9) | Juncosa › Garrigues | 47 |
| Forêt de la Pobla de Cérvoles (10) | la Pobla de Cérvoles › Garrigues | 47 |
| Forêt de Llavorsí | Llavorsí › Pallars Sobirà | 47 |
| Forêt de les Valls d'Aguilar (20) | les Valls d'Aguilar › Alt Urgell | 47 |
| Forêt de Baix Pallars (28) | Baix Pallars › Pallars Sobirà | 47 |
| Forêt de el Pont de Bar (2) | el Pont de Bar › Alt Urgell | 47 |
| Forêt de Guixers (19) | Guixers › Solsonès | 47 |
| Forêt de Vielha e Mijaran (36) | Vielha e Mijaran › Val d'Aran | 47 |
| Forêt de el Pont de Suert (39) | el Pont de Suert › Alta Ribagorça | 47 |
| Forêt de Sant Esteve de la Sarga (9) | Sant Esteve de la Sarga › Pallars Jussà | 47 |
| Forêt de Torà (22) | Torà › Solsonès | 47 |
| Forêt de Rialp (16) | Rialp › Pallars Sobirà | 47 |
| Forêt de Odèn (123) | Odèn › Solsonès | 47 |
| Forêt de Vielha e Mijaran (64) | Vielha e Mijaran › Val d'Aran | 47 |
| Forêt de les Valls de Valira (80) | les Valls de Valira › Alt Urgell | 47 |
| Forêt de Josa i Tuixén (32) | Josa i Tuixén › Alt Urgell | 47 |
| Forêt de Abella de la Conca (66) | Abella de la Conca › Pallars Jussà | 47 |
| Forêt de la Vall de Boí (268) | la Vall de Boí › Alta Ribagorça | 47 |
| Forêt de les Valls de Valira (132) | les Valls de Valira › Alt Urgell | 47 |
| Forêt de Vall de Cardós (5) | Vall de Cardós › Pallars Sobirà | 46 |
| Forêt de Baix Pallars (9) | Baix Pallars › Pallars Sobirà | 46 |
| Forêt de Baix Pallars (14) | Baix Pallars › Pallars Sobirà | 46 |
| Forêt de Vielha e Mijaran (46) | Vielha e Mijaran › Val d'Aran | 46 |
| Forêt de Conca de Dalt (24) | Conca de Dalt › Pallars Jussà | 46 |
| Forêt de Sant Guim de Freixenet (9) | Sant Guim de Freixenet › Segarra | 46 |
| Forêt de Soriguera (29) | Soriguera › Pallars Sobirà | 46 |
| Forêt de les Valls de Valira (68) | les Valls de Valira › Alt Urgell | 46 |
| Forêt de Baix Pallars (44) | Baix Pallars › Pallars Sobirà | 46 |
| Forêt de Sant Esteve de la Sarga (69) | Sant Esteve de la Sarga › Pallars Jussà | 46 |
| Forêt de Ivars de Noguera (9) | Ivars de Noguera › Noguera | 46 |
| Forêt de Coll de Nargó (126) | Coll de Nargó › Alt Urgell | 46 |
| Forêt de la Vall de Boí (266) | la Vall de Boí › Alta Ribagorça | 46 |
| Forêt de Alàs i Cerc (14) | Alàs i Cerc › Alt Urgell | 46 |
| Forêt de les Valls d'Aguilar | les Valls d'Aguilar › Alt Urgell | 45 |
| Forêt de Alt Àneu (2) | Alt Àneu › Pallars Sobirà | 45 |
| Forêt de el Pont de Suert (10) | el Pont de Suert › Alta Ribagorça | 45 |
| Forêt de la Granadella (13) | la Granadella › Garrigues | 45 |
| Forêt de Odèn (6) | Odèn › Solsonès | 45 |
| Forêt de Lladurs (52) | Lladurs › Solsonès | 45 |
| Forêt de Montferrer i Castellbò (27) | Montferrer i Castellbò › Alt Urgell | 45 |
| Forêt de les Avellanes i Santa Linya (12) | les Avellanes i Santa Linya › Noguera | 45 |
| Forêt de Alt Àneu (49) | Alt Àneu › Pallars Sobirà | 45 |
| Forêt de Coll de Nargó (78) | Coll de Nargó › Alt Urgell | 45 |
| Forêt de Cava (10) | Cava › Alt Urgell | 45 |
| Forêt de Guixers (100) | Guixers › Solsonès | 45 |
| Forêt de Naut Aran (88) | Naut Aran › Val d'Aran | 45 |
| Forêt de Alt Àneu (148) | Alt Àneu › Pallars Sobirà | 45 |
| Forêt de Coll de Nargó (91) | Coll de Nargó › Alt Urgell | 45 |
| Forêt de Lladurs (254) | Lladurs › Solsonès | 45 |
| Forêt de la Pobla de Segur (16) | la Pobla de Segur › Pallars Jussà | 45 |
| Forêt de el Pont de Suert (55) | el Pont de Suert › Alta Ribagorça | 45 |
| Forêt de Soriguera (48) | Soriguera › Pallars Sobirà | 45 |
| Forêt de Soriguera (10) | Soriguera › Pallars Sobirà | 44 |
| Forêt de Coll de Nargó (9) | Coll de Nargó › Alt Urgell | 44 |
| Forêt de les Avellanes i Santa Linya (10) | les Avellanes i Santa Linya › Noguera | 44 |
| Forêt de Canejan (3) | Canejan › Val d'Aran | 44 |
| Forêt de Vilaller (25) | Vilaller › Alta Ribagorça | 44 |
| Forêt de Es Bòrdes (6) | Es Bòrdes › Val d'Aran | 44 |
| Forêt de Fígols i Alinyà (19) | Fígols i Alinyà › Alt Urgell | 44 |
| Forêt de Guixers (50) | Guixers › Solsonès | 44 |
| Forêt de Gósol (17) | Gósol › Berguedà (Lérida) | 44 |
| Forêt de Navès (134) | Navès › Solsonès | 44 |
| Forêt de Montferrer i Castellbò (37) | Montferrer i Castellbò › Alt Urgell | 44 |
| Forêt de Torà (25) | Torà › Solsonès | 44 |
| Forêt de Gósol (93) | Gósol › Berguedà (Lérida) | 44 |
| Forêt de Coll de Nargó (92) | Coll de Nargó › Alt Urgell | 44 |
| Forêt de el Pont de Suert (66) | el Pont de Suert › Alta Ribagorça | 44 |
| Forêt de Alins (71) | Alins › Pallars Sobirà | 44 |
| Forêt de Alàs i Cerc (28) | Alàs i Cerc › Alt Urgell | 44 |
| Forêt de la Vansa i Fórnols (2) | la Vansa i Fórnols › Alt Urgell | 43 |
| Forêt de Oliola | Oliola › Noguera | 43 |
| Forêt de la Torre de Cabdella (2) | la Torre de Cabdella › Pallars Jussà | 43 |
| Forêt de Baix Pallars (10) | Baix Pallars › Pallars Sobirà | 43 |
| Forêt de Baix Pallars (12) | Baix Pallars › Pallars Sobirà | 43 |
| Forêt de la Baronia de Rialb (21) | la Baronia de Rialb › Noguera | 43 |
| Forêt de Vinaixa (8) | Vinaixa › Garrigues | 43 |
| Forêt de Bellaguarda (4) | Bellaguarda › Garrigues | 43 |
| Forêt de Conca de Dalt (16) | Conca de Dalt › Pallars Jussà | 43 |
| Forêt de Pinós (15) | Pinós › Solsonès | 43 |
| Forêt de Clariana de Cardener (156) | Clariana de Cardener › Solsonès | 43 |
| Forêt de Isona i Conca Dellà (26) | Isona i Conca Dellà › Pallars Jussà | 43 |
| Forêt de Alt Àneu (39) | Alt Àneu › Pallars Sobirà | 43 |
| Forêt de la Guingueta d'Àneu (22) | la Guingueta d'Àneu › Pallars Sobirà | 43 |
| Forêt de Navès (92) | Navès › Solsonès | 43 |
| Forêt de Coll de Nargó (67) | Coll de Nargó › Alt Urgell | 43 |
| Forêt de Coll de Nargó (76) | Coll de Nargó › Alt Urgell | 43 |
| Forêt de Odèn (43) | Odèn › Solsonès | 43 |
| Forêt de Abella de la Conca (15) | Abella de la Conca › Pallars Jussà | 43 |
| Forêt de Torà (26) | Torà › Solsonès | 43 |
| Forêt de Bellver de Cerdanya (28) | Bellver de Cerdanya › Cerdanya (Lérida) | 43 |
| Forêt de Gósol (56) | Gósol › Berguedà (Lérida) | 43 |
| Forêt de Naut Aran (75) | Naut Aran › Val d'Aran | 43 |
| Forêt de Clariana de Cardener (167) | Clariana de Cardener › Solsonès | 43 |
| Forêt de Sant Esteve de la Sarga (58) | Sant Esteve de la Sarga › Pallars Jussà | 43 |
| Forêt de Àger (103) | Àger › Noguera | 43 |
| Forêt de les Valls d'Aguilar (38) | les Valls d'Aguilar › Alt Urgell | 43 |
| Forêt de el Pont de Bar (53) | el Pont de Bar › Alt Urgell | 43 |
| Forêt de la Pobla de Cérvoles (7) | la Pobla de Cérvoles › Garrigues | 42 |
| Forêt de Vall de Cardós (8) | Vall de Cardós › Pallars Sobirà | 42 |
| Forêt de Pinell de Solsonès (16) | Pinell de Solsonès › Solsonès | 42 |
| Forêt de Almatret (4) | Almatret › Segrià | 42 |
| Forêt de Castell de Mur (2) | Castell de Mur › Pallars Jussà | 42 |
| Forêt de Vielha e Mijaran (47) | Vielha e Mijaran › Val d'Aran | 42 |
| Forêt de Baix Pallars (38) | Baix Pallars › Pallars Sobirà | 42 |
| Forêt de Castellar de la Ribera (25) | Castellar de la Ribera › Solsonès | 42 |
| Forêt de Pinell de Solsonès (34) | Pinell de Solsonès › Solsonès | 42 |
| Forêt de les Valls de Valira (60) | les Valls de Valira › Alt Urgell | 42 |
| Forêt de el Pont de Bar (6) | el Pont de Bar › Alt Urgell | 42 |
| Forêt de Cava (18) | Cava › Alt Urgell | 42 |
| Forêt de Abella de la Conca (76) | Abella de la Conca › Pallars Jussà | 42 |
| Forêt de Estamariu (20) | Estamariu › Alt Urgell | 42 |
| Bois de Vallbona de les Monges (5) | Vallbona de les Monges › Urgell | 41 |
| Forêt de Vinaixa (7) | Vinaixa › Garrigues | 41 |
| Forêt de Baix Pallars (15) | Baix Pallars › Pallars Sobirà | 41 |
| Forêt de Àger (20) | Àger › Noguera | 41 |
| Forêt de la Guingueta d'Àneu (21) | la Guingueta d'Àneu › Pallars Sobirà | 41 |
| Forêt de Guixers (42) | Guixers › Solsonès | 41 |
| Forêt de Navès (121) | Navès › Solsonès | 41 |
| Forêt de Vilaller (62) | Vilaller › Alta Ribagorça | 41 |
| Forêt de Olius (351) | Olius › Solsonès | 41 |
| Forêt de Baix Pallars (54) | Baix Pallars › Pallars Sobirà | 41 |
| Forêt de Àger (74) | Àger › Noguera | 41 |
| Forêt de Soriguera (45) | Soriguera › Pallars Sobirà | 41 |
| Forêt de Seròs | Seròs › Segrià | 40 |
| Forêt de Conca de Dalt (9) | Conca de Dalt › Pallars Jussà | 40 |
| Forêt de Bellver de Cerdanya | Bellver de Cerdanya › Cerdanya (Lérida) | 40 |
| Forêt de Tremp (33) | Tremp › Pallars Jussà | 40 |
| Forêt de Soriguera (15) | Soriguera › Pallars Sobirà | 40 |
| Forêt de Conca de Dalt (17) | Conca de Dalt › Pallars Jussà | 40 |
| Forêt de Alt Àneu (33) | Alt Àneu › Pallars Sobirà | 40 |
| Forêt de Rialp (18) | Rialp › Pallars Sobirà | 40 |
| Forêt de la Baronia de Rialb (48) | la Baronia de Rialb › Noguera | 40 |
| Forêt de Abella de la Conca (52) | Abella de la Conca › Pallars Jussà | 40 |
| Forêt de Odèn (136) | Odèn › Solsonès | 40 |
| Forêt de Ribera d'Urgellet (59) | Ribera d'Urgellet › Alt Urgell | 40 |
| Forêt de el Pont de Bar (32) | el Pont de Bar › Alt Urgell | 40 |
| Forêt de Almatret (15) | Almatret › Segrià | 40 |
| Forêt de Soriguera (2) | Soriguera › Pallars Sobirà | 39 |
| Forêt de Odèn (3) | Odèn › Solsonès | 39 |
| Forêt de Alins (5) | Alins › Pallars Sobirà | 39 |
| Forêt de Isona i Conca Dellà (13) | Isona i Conca Dellà › Pallars Jussà | 39 |
| Forêt de Isona i Conca Dellà (14) | Isona i Conca Dellà › Pallars Jussà | 39 |
| Forêt de Lladurs (43) | Lladurs › Solsonès | 39 |
| Forêt de Sarroca de Bellera (11) | Sarroca de Bellera › Pallars Jussà | 39 |
| Forêt de Torà (4) | Torà › Solsonès | 39 |
| Forêt de el Pont de Suert (30) | el Pont de Suert › Alta Ribagorça | 39 |
| Forêt de la Coma i la Pedra (96) | la Coma i la Pedra › Solsonès | 39 |
| Forêt de Alt Àneu (41) | Alt Àneu › Pallars Sobirà | 39 |
| Forêt de Navès (129) | Navès › Solsonès | 39 |
| Forêt de Alins (31) | Alins › Pallars Sobirà | 39 |
| Forêt de Guixers (78) | Guixers › Solsonès | 39 |
| Forêt de les Valls de Valira (94) | les Valls de Valira › Alt Urgell | 39 |
| Forêt de Torà (32) | Torà › Solsonès | 39 |
| Bois de Olius | Olius › Solsonès | 39 |
| Forêt de Sant Esteve de la Sarga (67) | Sant Esteve de la Sarga › Pallars Jussà | 39 |
| Forêt de Abella de la Conca (73) | Abella de la Conca › Pallars Jussà | 39 |
| Forêt de Odèn (138) | Odèn › Solsonès | 39 |
| Forêt de Conca de Dalt (51) | Conca de Dalt › Pallars Jussà | 39 |
| Bois de Vallbona de les Monges (2) | Vallbona de les Monges › Urgell | 38 |
| Forêt de Tremp (16) | Tremp › Pallars Jussà | 38 |
| Forêt de Maials (7) | Maials › Segrià | 38 |
| Forêt de Montferrer i Castellbò (15) | Montferrer i Castellbò › Alt Urgell | 38 |
| Forêt de Sort (4) | Sort › Pallars Sobirà | 38 |
| Forêt de el Pont de Suert (14) | el Pont de Suert › Alta Ribagorça | 38 |
| Forêt de Lles de Cerdanya (13) | Lles de Cerdanya › Cerdanya (Lérida) | 38 |
| Forêt de Castell de Mur (9) | Castell de Mur › Pallars Jussà | 38 |
| Forêt de Pinell de Solsonès (36) | Pinell de Solsonès › Solsonès | 38 |
| Forêt de Navès (77) | Navès › Solsonès | 38 |
| Forêt de Bellver de Cerdanya (32) | Bellver de Cerdanya › Cerdanya (Lérida) | 38 |
| Forêt de Lladurs (262) | Lladurs › Solsonès | 38 |
| Forêt de Baix Pallars (47) | Baix Pallars › Pallars Sobirà | 38 |
| Forêt de Montferrer i Castellbò (91) | Montferrer i Castellbò › Alt Urgell | 38 |
| Forêt de Llavorsí (55) | Llavorsí › Pallars Sobirà | 38 |
| Forêt de el Pont de Bar (50) | el Pont de Bar › Alt Urgell | 38 |
| Forêt de Tremp (7) | Tremp › Pallars Jussà | 37 |
| Forêt de Pinell de Solsonès (6) | Pinell de Solsonès › Solsonès | 37 |
| Forêt de les Valls d'Aguilar (3) | les Valls d'Aguilar › Alt Urgell | 37 |
| Forêt de Tremp (25) | Tremp › Pallars Jussà | 37 |
| Forêt de la Vansa i Fórnols (10) | Ribera d'Urgellet › Alt Urgell | 37 |
| Forêt de Artesa de Segre (20) | Artesa de Segre › Noguera | 37 |
| Forêt de Alàs i Cerc (6) | Alàs i Cerc › Alt Urgell | 37 |
| Forêt de Navès (123) | Navès › Solsonès | 37 |
| Forêt de Alins (40) | Alins › Pallars Sobirà | 37 |
| Forêt de Alàs i Cerc (12) | Alàs i Cerc › Alt Urgell | 37 |
| Forêt de les Valls de Valira (86) | les Valls de Valira › Alt Urgell | 37 |
| Forêt de Peramola (19) | Peramola › Alt Urgell | 37 |
| Forêt de la Baronia de Rialb (45) | la Baronia de Rialb › Noguera | 37 |
| Forêt de Coll de Nargó (95) | Coll de Nargó › Alt Urgell | 37 |
| Forêt de Os de Balaguer (67) | Os de Balaguer › Noguera | 37 |
| Forêt de Àger (184) | Àger › Noguera | 37 |
| Forêt de Farrera (32) | Farrera › Pallars Sobirà | 37 |
| Forêt de Alàs i Cerc | Alàs i Cerc › Alt Urgell | 36 |
| Forêt de Baix Pallars (3) | Baix Pallars › Pallars Sobirà | 36 |
| Forêt de Tremp (34) | Tremp › Pallars Jussà | 36 |
| Forêt de Pinell de Solsonès (26) | Pinell de Solsonès › Solsonès | 36 |
| Forêt de Baix Pallars (23) | Baix Pallars › Pallars Sobirà | 36 |
| Forêt de la Torre de Cabdella (12) | la Torre de Cabdella › Pallars Jussà | 36 |
| Forêt de la Torre de Cabdella (16) | la Torre de Cabdella › Pallars Jussà | 36 |
| Forêt de Torà (6) | Torà › Solsonès | 36 |
| Forêt de Cabó (5) | Cabó › Alt Urgell | 36 |
| Forêt de Odèn (33) | Odèn › Solsonès | 36 |
| Forêt de Lladorre (20) | Lladorre › Pallars Sobirà | 36 |
| Forêt de Castell de Mur (10) | Castell de Mur › Pallars Jussà | 36 |
| Forêt de Vilamòs | Vilamòs › Val d'Aran | 36 |
| Forêt de Montferrer i Castellbò (35) | Montferrer i Castellbò › Alt Urgell | 36 |
| Forêt de Montferrer i Castellbò (38) | Montferrer i Castellbò › Alt Urgell | 36 |
| Forêt de Montferrer i Castellbò (40) | Montferrer i Castellbò › Alt Urgell | 36 |
| Forêt de Pinós (100) | Pinós › Solsonès | 36 |
| Forêt de Navès (173) | Navès › Solsonès | 36 |
| Forêt de les Valls de Valira (44) | les Valls de Valira › Alt Urgell | 36 |
| Forêt de les Valls de Valira (82) | les Valls de Valira › Alt Urgell | 36 |
| Forêt de Odèn (135) | Odèn › Solsonès | 36 |
| Forêt de Cabó (14) | Cabó › Alt Urgell | 36 |
| Forêt de Navès (186) | Navès › Solsonès | 36 |
| Forêt de Sant Esteve de la Sarga (53) | Sant Esteve de la Sarga › Pallars Jussà | 36 |
| Forêt de Àger (111) | Àger › Noguera | 36 |
| Forêt de la Pobla de Segur (26) | la Pobla de Segur › Pallars Jussà | 36 |
| Forêt de Àger (180) | Àger › Noguera | 36 |
| Forêt de Oliola (11) | Oliola › Noguera | 36 |
| Forêt de Estamariu (19) | Estamariu › Alt Urgell | 36 |
| Forêt de Montferrer i Castellbò (104) | Montferrer i Castellbò › Alt Urgell | 36 |
| Forêt de Juncosa (6) | Juncosa › Garrigues | 35 |
| Forêt de la Baronia de Rialb (14) | la Baronia de Rialb › Noguera | 35 |
| Forêt de Lladurs (14) | Lladurs › Solsonès | 35 |
| Forêt de Biosca (5) | Biosca › Solsonès | 35 |
| Forêt de Oliola (6) | Oliola › Noguera | 35 |
| Forêt de la Pobla de Cérvoles (11) | la Pobla de Cérvoles › Garrigues | 35 |
| Forêt de Conca de Dalt (12) | Conca de Dalt › Pallars Jussà | 35 |
| Forêt de Lladorre (5) | Lladorre › Pallars Sobirà | 35 |
| Forêt de Navès (131) | Navès › Solsonès | 35 |
| Forêt de Esterri de Cardós (11) | Esterri de Cardós › Pallars Sobirà | 35 |
| Forêt de Gósol (42) | Gósol › Berguedà (Lérida) | 35 |
| Forêt de la Coma i la Pedra (148) | la Coma i la Pedra › Solsonès | 35 |
| Forêt de Alt Àneu (79) | Alt Àneu › Pallars Sobirà | 35 |
| Forêt de Alt Àneu (94) | Alt Àneu › Pallars Sobirà | 35 |
| Forêt de Alins (61) | Alins › Pallars Sobirà | 35 |
| Forêt de les Valls de Valira (95) | les Valls de Valira › Alt Urgell | 35 |
| Forêt de Llimiana (11) | Llimiana › Pallars Jussà | 35 |
| Forêt de Clariana de Cardener (214) | Clariana de Cardener › Solsonès | 35 |
| Forêt de Llobera (491) | Llobera › Solsonès | 35 |
| Forêt de Sant Esteve de la Sarga (60) | Sant Esteve de la Sarga › Pallars Jussà | 35 |
| Forêt de Àger (154) | Àger › Noguera | 35 |
| Forêt de Llavorsí (62) | Llavorsí › Pallars Sobirà | 35 |
| Forêt de Espot (57) | Espot › Pallars Sobirà | 35 |
| Forêt de Montferrer i Castellbò (116) | Montferrer i Castellbò › Alt Urgell | 35 |
| Forêt de Juncosa (5) | Juncosa › Garrigues | 34 |
| Forêt de Senterada (2) | Senterada › Pallars Jussà | 34 |
| Forêt de l'Albi (2) | l'Albi › Garrigues | 34 |
| Forêt de Sarroca de Bellera (2) | Sarroca de Bellera › Pallars Jussà | 34 |
| Forêt de el Pont de Suert (8) | el Pont de Suert › Alta Ribagorça | 34 |
| Forêt de Os de Balaguer (4) | Os de Balaguer › Noguera | 34 |
| Forêt de la Granadella (12) | la Granadella › Garrigues | 34 |
| Forêt de Maials (16) | Maials › Segrià | 34 |
| Forêt de Tarrés (9) | Tarrés › Garrigues | 34 |
| Forêt de Vall de Cardós (17) | Vall de Cardós › Pallars Sobirà | 34 |
| Forêt de Artesa de Segre (17) | Artesa de Segre › Noguera | 34 |
| Forêt de Soriguera (16) | Soriguera › Pallars Sobirà | 34 |
| Forêt de la Baronia de Rialb (36) | la Baronia de Rialb › Noguera | 34 |
| Forêt de Sort (5) | Sort › Pallars Sobirà | 34 |
| Forêt de Alàs i Cerc (8) | Alàs i Cerc › Alt Urgell | 34 |
| Bois de l'Espluga Calba (2) | l'Espluga Calba › Garrigues | 34 |
| Forêt de Rialp (10) | Rialp › Pallars Sobirà | 34 |
| Forêt de Ribera d'Urgellet (28) | Ribera d'Urgellet › Alt Urgell | 34 |
| Forêt de Navès (75) | Navès › Solsonès | 34 |
| Forêt de Esterri de Cardós (3) | Esterri de Cardós › Pallars Sobirà | 34 |
| Forêt de Alt Àneu (81) | Alt Àneu › Pallars Sobirà | 34 |
| Forêt de Alt Àneu (90) | Alt Àneu › Pallars Sobirà | 34 |
| Forêt de Alt Àneu (96) | Alt Àneu › Pallars Sobirà | 34 |
| Forêt de Alt Àneu (117) | Alt Àneu › Pallars Sobirà | 34 |
| Forêt de Rialp (17) | Rialp › Pallars Sobirà | 34 |
| Forêt de Alins (48) | Alins › Pallars Sobirà | 34 |
| Forêt de Montferrer i Castellbò (46) | Montferrer i Castellbò › Alt Urgell | 34 |
| Forêt de Cabó (36) | Cabó › Alt Urgell | 34 |
| Forêt de Coll de Nargó (94) | Coll de Nargó › Alt Urgell | 34 |
| Forêt de la Vansa i Fórnols (27) | la Vansa i Fórnols › Alt Urgell | 34 |
| Forêt de Abella de la Conca (62) | Abella de la Conca › Pallars Jussà | 34 |
| Forêt de el Pont de Bar (47) | el Pont de Bar › Alt Urgell | 34 |
| Forêt de la Torre de Cabdella (27) | la Torre de Cabdella › Pallars Jussà | 34 |
| Forêt de Vall de Cardós (63) | Vall de Cardós › Pallars Sobirà | 34 |
| Forêt de Bausen (2) | Bausen › Val d'Aran | 33 |
| Forêt de Cervià de les Garrigues | Cervià de les Garrigues › Garrigues | 33 |
| Forêt de Vilanova de Meià (5) | Vilanova de Meià › Noguera | 33 |
| Forêt de Tremp (22) | Tremp › Pallars Jussà | 33 |
| Forêt de Juncosa (10) | Juncosa › Garrigues | 33 |
| Forêt de Pinós (5) | Pinós › Solsonès | 33 |
| Forêt de Isona i Conca Dellà (12) | Isona i Conca Dellà › Pallars Jussà | 33 |
| Forêt de Fulleda (3) | Fulleda › Garrigues | 33 |
| Forêt de Coll de Nargó (18) | Coll de Nargó › Alt Urgell | 33 |
| Forêt de la Granadella (17) | la Granadella › Garrigues | 33 |
| Forêt de Sarroca de Bellera (7) | Sarroca de Bellera › Pallars Jussà | 33 |
| Forêt de Lladurs (55) | Lladurs › Solsonès | 33 |
| Parc municipal de la Mitjana | Lleida › Segrià | 33 |
| Forêt de la Coma i la Pedra (97) | la Coma i la Pedra › Solsonès | 33 |
| Forêt de Alins (28) | Alins › Pallars Sobirà | 33 |
| Forêt de Odèn (114) | Odèn › Solsonès | 33 |
| Forêt de Baix Pallars (45) | Baix Pallars › Pallars Sobirà | 33 |
| Forêt de Clariana de Cardener (192) | Clariana de Cardener › Solsonès | 33 |
| Forêt de Sant Esteve de la Sarga (70) | Sant Esteve de la Sarga › Pallars Jussà | 33 |
| Forêt de Àger (123) | Àger › Noguera | 33 |
| Forêt de Camarasa (52) | Camarasa › Noguera | 33 |
| Forêt de Ivars de Noguera (15) | Ivars de Noguera › Noguera | 33 |
| Forêt de Àger (183) | Àger › Noguera | 33 |
| Forêt de Tremp (106) | Tremp › Pallars Jussà | 33 |
| Forêt de el Pont de Suert (49) | el Pont de Suert › Alta Ribagorça | 33 |
| Forêt de Tremp (132) | Tremp › Pallars Jussà | 33 |
| Forêt de Farrera (24) | Farrera › Pallars Sobirà | 33 |
| Forêt de la Vansa i Fórnols (37) | la Vansa i Fórnols › Alt Urgell | 33 |
| Forêt de Rialp | Rialp › Pallars Sobirà | 32 |
| Forêt de Baix Pallars (2) | Baix Pallars › Pallars Sobirà | 32 |
| Forêt de la Pobla de Segur (3) | la Pobla de Segur › Pallars Jussà | 32 |
| Forêt de Oliola (5) | Oliola › Noguera | 32 |
| Forêt de Alt Àneu (3) | Alt Àneu › Pallars Sobirà | 32 |
| Forêt de les Valls d'Aguilar (13) | les Valls d'Aguilar › Alt Urgell | 32 |
| Forêt de Sort (2) | Sort › Pallars Sobirà | 32 |
| Forêt de Sant Esteve de la Sarga | Sant Esteve de la Sarga › Pallars Jussà | 32 |
| Forêt de Lladorre (3) | Lladorre › Pallars Sobirà | 32 |
| Bois de els Omells de na Gaia (3) | els Omells de na Gaia › Urgell | 32 |
| Forêt de Olius (27) | Olius › Solsonès | 32 |
| Forêt de Alins (13) | Alins › Pallars Sobirà | 32 |
| Forêt de Lladurs (56) | Lladurs › Solsonès | 32 |
| Forêt de la Vall de Boí (248) | la Vall de Boí › Alta Ribagorça | 32 |
| Forêt de el Pont de Suert (37) | el Pont de Suert › Alta Ribagorça | 32 |
| Forêt de Naut Aran (63) | Naut Aran › Val d'Aran | 32 |
| Forêt de Tírvia (3) | Tírvia › Pallars Sobirà | 32 |
| Forêt de Riu de Cerdanya (11) | Riu de Cerdanya › Cerdanya (Lérida) | 32 |
| Forêt de Gósol (71) | Gósol › Berguedà (Lérida) | 32 |
| Forêt de Alt Àneu (137) | Alt Àneu › Pallars Sobirà | 32 |
| Forêt de Rialp (24) | Rialp › Pallars Sobirà | 32 |
| Forêt de la Baronia de Rialb (44) | la Baronia de Rialb › Noguera | 32 |
| Forêt de Coll de Nargó (93) | Coll de Nargó › Alt Urgell | 32 |
| Forêt de Montellà i Martinet (45) | Montellà i Martinet › Cerdanya (Lérida) | 32 |
| Forêt de Àger (76) | Àger › Noguera | 32 |
| Forêt de Coll de Nargó (110) | Coll de Nargó › Alt Urgell | 32 |
| Forêt de Coll de Nargó (118) | Coll de Nargó › Alt Urgell | 32 |
| Forêt de el Pont de Suert (97) | el Pont de Suert › Alta Ribagorça | 32 |
| Forêt de Montferrer i Castellbò (92) | Montferrer i Castellbò › Alt Urgell | 32 |
| Forêt de Rialp (27) | Rialp › Pallars Sobirà | 32 |
| Forêt de el Pont de Bar (14) | el Pont de Bar › Alt Urgell | 32 |
| Forêt de Alàs i Cerc (33) | Alàs i Cerc › Alt Urgell | 32 |
| Forêt de la Baronia de Rialb (3) | la Baronia de Rialb › Noguera | 31 |
| Forêt de Artesa de Segre (2) | Artesa de Segre › Noguera | 31 |
| Forêt de Cava | Cava › Alt Urgell | 31 |
| Forêt de Artesa de Segre (6) | Artesa de Segre › Noguera | 31 |
| Forêt de Vilanova de l'Aguda (3) | Vilanova de l'Aguda › Noguera | 31 |
| Forêt de Conca de Dalt (10) | Conca de Dalt › Pallars Jussà | 31 |
| Forêt de Pinell de Solsonès (24) | Pinell de Solsonès › Solsonès | 31 |
| Forêt de Naut Aran (6) | Naut Aran › Val d'Aran | 31 |
| Forêt de Cava (5) | Cava › Alt Urgell | 31 |
| Forêt de Vielha e Mijaran (38) | Vielha e Mijaran › Val d'Aran | 31 |
| Forêt de Vilanova de Meià (17) | Vilanova de Meià › Noguera | 31 |
| Forêt de Fígols i Alinyà (24) | Fígols i Alinyà › Alt Urgell | 31 |
| Forêt de la Vall de Boí (258) | la Vall de Boí › Alta Ribagorça | 31 |
| Forêt de Naut Aran (73) | Naut Aran › Val d'Aran | 31 |
| Forêt de Alt Àneu (107) | Alt Àneu › Pallars Sobirà | 31 |
| Forêt de Naut Aran (117) | Naut Aran › Val d'Aran | 31 |
| Forêt de Vilaller (61) | Vilaller › Alta Ribagorça | 31 |
| Forêt de Baix Pallars (49) | Baix Pallars › Pallars Sobirà | 31 |
| Forêt de Camarasa (41) | Camarasa › Noguera | 31 |
| Forêt de Àger (93) | Àger › Noguera | 31 |
| Forêt de el Pont de Suert (73) | el Pont de Suert › Alta Ribagorça | 31 |
| Forêt de Farrera (11) | Farrera › Pallars Sobirà | 31 |
| Bois de Sort (3) | Sort › Pallars Sobirà | 31 |
| Forêt de la Granadella (5) | la Granadella › Garrigues | 30 |
| Forêt de Coll de Nargó (7) | Coll de Nargó › Alt Urgell | 30 |
| Bois de Ciutadilla (2) | Ciutadilla › Urgell | 30 |
| Forêt de Pinell de Solsonès (15) | Pinell de Solsonès › Solsonès | 30 |
| Forêt de Castellar de la Ribera (7) | Castellar de la Ribera › Solsonès | 30 |
| Bois de Montoliu de Segarra | Montoliu de Segarra › Segarra | 30 |
| Forêt de el Pont de Suert (15) | el Pont de Suert › Alta Ribagorça | 30 |
| Forêt de la Guingueta d'Àneu (8) | la Guingueta d'Àneu › Pallars Sobirà | 30 |
| Forêt de Lles de Cerdanya (12) | Lles de Cerdanya › Cerdanya (Lérida) | 30 |
| Forêt de Montoliu de Segarra (7) | Montoliu de Segarra › Segarra | 30 |
| Forêt de Corbins (2) | Corbins › Segrià | 30 |
| Forêt de Guixers (33) | Guixers › Solsonès | 30 |
| Forêt de Guixers (36) | Guixers › Solsonès | 30 |
| Forêt de Bassella (15) | Bassella › Alt Urgell | 30 |
| Forêt de Bassella (22) | Bassella › Alt Urgell | 30 |
| Forêt de Guixers (49) | Guixers › Solsonès | 30 |
| Forêt de la Guingueta d'Àneu (42) | la Guingueta d'Àneu › Pallars Sobirà | 30 |
| Forêt de Pinós (128) | Pinós › Solsonès | 30 |
| Forêt de Guixers (91) | Guixers › Solsonès | 30 |
| Forêt de Alt Àneu (71) | Alt Àneu › Pallars Sobirà | 30 |
| Forêt de Es Bòrdes (17) | Es Bòrdes › Val d'Aran | 30 |
| Forêt de Alins (62) | Alins › Pallars Sobirà | 30 |
| Forêt de Peramola (18) | Peramola › Alt Urgell | 30 |
| Forêt de la Baronia de Rialb (46) | la Baronia de Rialb › Noguera | 30 |
| Forêt de Baix Pallars (43) | Baix Pallars › Pallars Sobirà | 30 |
| Forêt de Navès (217) | Navès › Solsonès | 30 |
| Forêt de Castell de Mur (30) | Castell de Mur › Pallars Jussà | 30 |
| Forêt de Abella de la Conca (46) | Abella de la Conca › Pallars Jussà | 30 |
| Forêt de Àger (182) | Àger › Noguera | 30 |
| Forêt de Estamariu (14) | Estamariu › Alt Urgell | 30 |
| Forêt de Arsèguel (13) | Arsèguel › Alt Urgell | 30 |
| Forêt de el Pont de Bar (44) | el Pont de Bar › Alt Urgell | 30 |
| Forêt de el Pont de Suert (2) | el Pont de Suert › Alta Ribagorça | 29 |
| Forêt de el Pont de Suert (4) | el Pont de Suert › Alta Ribagorça | 29 |
| Forêt de Sant Guim de la Plana | Sant Guim de la Plana › Segarra | 29 |
| Forêt de la Granadella (10) | la Granadella › Garrigues | 29 |
| Forêt de les Avellanes i Santa Linya (7) | les Avellanes i Santa Linya › Noguera | 29 |
| Forêt de Juncosa (14) | Juncosa › Garrigues | 29 |
| Forêt de Baix Pallars (19) | Baix Pallars › Pallars Sobirà | 29 |
| Forêt de Oliola (8) | Oliola › Noguera | 29 |
| Forêt de Pinell de Solsonès (27) | Pinell de Solsonès › Solsonès | 29 |
| Forêt de Soriguera (14) | Soriguera › Pallars Sobirà | 29 |
| Forêt de Lles de Cerdanya (9) | Lles de Cerdanya › Cerdanya (Lérida) | 29 |
| Forêt de Baix Pallars (30) | Baix Pallars › Pallars Sobirà | 29 |
| Forêt de Conca de Dalt (21) | Conca de Dalt › Pallars Jussà | 29 |
| Forêt de Navès (29) | Navès › Solsonès | 29 |
| Forêt de Guixers (22) | Guixers › Solsonès | 29 |
| Forêt de el Pont de Suert (36) | el Pont de Suert › Alta Ribagorça | 29 |
| Forêt de Vielha e Mijaran (22) | Vielha e Mijaran › Val d'Aran | 29 |
| Forêt de Navès (122) | Navès › Solsonès | 29 |
| Forêt de Odèn (122) | Odèn › Solsonès | 29 |
| Forêt de Vilamòs (9) | Vilamòs › Val d'Aran | 29 |
| Forêt de Montferrer i Castellbò (47) | Montferrer i Castellbò › Alt Urgell | 29 |
| Forêt de Josa i Tuixén (34) | Josa i Tuixén › Alt Urgell | 29 |
| Forêt de Navès (179) | Navès › Solsonès | 29 |
| Forêt de Àger (52) | Àger › Noguera | 29 |
| Forêt de Baix Pallars (58) | Baix Pallars › Pallars Sobirà | 29 |
| Forêt de Àger (80) | Àger › Noguera | 29 |
| Forêt de Àger (90) | Àger › Noguera | 29 |
| Forêt de Os de Balaguer (50) | Os de Balaguer › Noguera | 29 |
| Forêt de Abella de la Conca (83) | Abella de la Conca › Alt Urgell | 29 |
| Forêt de Tírvia (8) | Tírvia › Pallars Sobirà | 29 |
| Forêt de Farrera (29) | Farrera › Pallars Sobirà | 29 |
| Forêt de Tremp (2) | Tremp › Pallars Jussà | 28 |
| Forêt de la Vansa i Fórnols (3) | la Vansa i Fórnols › Alt Urgell | 28 |
| Forêt de Tremp (12) | Tremp › Pallars Jussà | 28 |
| Forêt de Baix Pallars (8) | Baix Pallars › Pallars Sobirà | 28 |
| Forêt de Montferrer i Castellbò (7) | Montferrer i Castellbò › Alt Urgell | 28 |
| Forêt de la Baronia de Rialb (17) | la Baronia de Rialb › Noguera | 28 |
| Forêt de Farrera (2) | Farrera › Pallars Sobirà | 28 |
| Forêt de Almatret (3) | Almatret › Segrià | 28 |
| Forêt de Biosca (8) | Biosca › Solsonès | 28 |
| Forêt de Lles de Cerdanya (6) | Lles de Cerdanya › Cerdanya (Lérida) | 28 |
| Forêt de Sarroca de Bellera (6) | Sarroca de Bellera › Pallars Jussà | 28 |
| Forêt de Cava (6) | Cava › Alt Urgell | 28 |
| Forêt de Lladurs (54) | Lladurs › Solsonès | 28 |
| Bois de Alàs i Cerc | Alàs i Cerc › Alt Urgell | 28 |
| Forêt de Vielha e Mijaran (16) | Vielha e Mijaran › Val d'Aran | 28 |
| Forêt de les Valls de Valira (20) | les Valls de Valira › Alt Urgell | 28 |
| Forêt de Navès (71) | Navès › Solsonès | 28 |
| Forêt de Gósol (13) | Gósol › Berguedà (Lérida) | 28 |
| Forêt de Odèn (44) | Odèn › Solsonès | 28 |
| Forêt de Montferrer i Castellbò (41) | Montferrer i Castellbò › Alt Urgell | 28 |
| Forêt de Coll de Nargó (85) | Coll de Nargó › Alt Urgell | 28 |
| Forêt de les Valls de Valira (34) | les Valls de Valira › Alt Urgell | 28 |
| Forêt de Riner (155) | Riner › Solsonès | 28 |
| Forêt de Gósol (98) | Gósol › Berguedà (Lérida) | 28 |
| Forêt de les Valls de Valira (56) | les Valls de Valira › Alt Urgell | 28 |
| Forêt de Montferrer i Castellbò (77) | Montferrer i Castellbò › Alt Urgell | 28 |
| Forêt de Àger (165) | Àger › Noguera | 28 |
| Forêt de Os de Balaguer (48) | Os de Balaguer › Noguera | 28 |
| Forêt de Abella de la Conca (34) | Abella de la Conca › Pallars Jussà | 28 |
| Forêt de Abella de la Conca (77) | Abella de la Conca › Pallars Jussà | 28 |
| Forêt de Àger (181) | Àger › Noguera | 28 |
| Forêt de Gavet de la Conca (12) | Gavet de la Conca › Pallars Jussà | 28 |
| Forêt de Alàs i Cerc (34) | Alàs i Cerc › Alt Urgell | 28 |
| Forêt de Tremp (17) | Tremp › Pallars Jussà | 27 |
| Forêt de Vall de Cardós (7) | Vall de Cardós › Pallars Sobirà | 27 |
| Forêt de la Granadella (6) | la Granadella › Garrigues | 27 |
| Forêt de Gavet de la Conca (2) | Gavet de la Conca › Pallars Jussà | 27 |
| Forêt de Isona i Conca Dellà (6) | Isona i Conca Dellà › Pallars Jussà | 27 |
| Forêt de el Pont de Suert (7) | el Pont de Suert › Alta Ribagorça | 27 |
| Forêt de Tremp (31) | Tremp › Pallars Jussà | 27 |
| Forêt de Cervià de les Garrigues (4) | Cervià de les Garrigues › Garrigues | 27 |
| Forêt de Estaràs (6) | Estaràs › Segarra | 27 |
| Forêt de Pinós (34) | Pinós › Solsonès | 27 |
| Forêt de el Pont de Suert (29) | el Pont de Suert › Alta Ribagorça | 27 |
| Bois de Vallbona de les Monges (11) | Vallbona de les Monges › Urgell | 27 |
| Forêt de Vielha e Mijaran (48) | Vielha e Mijaran › Val d'Aran | 27 |
| Forêt de Riner (131) | Riner › Solsonès | 27 |
| Forêt de la Molsosa (27) | la Molsosa › Solsonès | 27 |
| Forêt de Coll de Nargó (48) | Coll de Nargó › Alt Urgell | 27 |
| Forêt de la Coma i la Pedra (109) | la Coma i la Pedra › Solsonès | 27 |
| Forêt de la Coma i la Pedra (135) | la Coma i la Pedra › Solsonès | 27 |
| Forêt de Lladurs (218) | Lladurs › Solsonès | 27 |
| Forêt de Naut Aran (72) | Naut Aran › Val d'Aran | 27 |
| Forêt de Vielha e Mijaran (71) | Vielha e Mijaran › Val d'Aran | 27 |
| Forêt de Vilaller (71) | Vilaller › Alta Ribagorça | 27 |
| Forêt de Clariana de Cardener (172) | Clariana de Cardener › Solsonès | 27 |
| Forêt de Clariana de Cardener (176) | Clariana de Cardener › Solsonès | 27 |
| Forêt de el Pont de Suert (47) | el Pont de Suert › Alta Ribagorça | 27 |
| Forêt de les Valls d'Aguilar (34) | les Valls d'Aguilar › Alt Urgell | 27 |
| Forêt de Montferrer i Castellbò (113) | Montferrer i Castellbò › Alt Urgell | 27 |
| Forêt de les Valls de Valira (151) | les Valls de Valira › Alt Urgell | 27 |
| Forêt de la Vansa i Fórnols (38) | la Vansa i Fórnols › Alt Urgell | 27 |
| Bois de Ciutadilla | Ciutadilla › Urgell | 26 |
| Forêt de la Granadella (3) | la Granadella › Garrigues | 26 |
| Forêt de Biosca (2) | Biosca › Solsonès | 26 |
| Forêt de la Granadella (4) | la Granadella › Garrigues | 26 |
| Forêt de Os de Balaguer | Os de Balaguer › Noguera | 26 |
| Forêt de Os de Balaguer (2) | Os de Balaguer › Noguera | 26 |
| Forêt de Tremp (29) | Tremp › Pallars Jussà | 26 |
| Forêt de Torrebesses | Torrebesses › Segrià | 26 |
| Forêt de Maials (17) | Maials › Segrià | 26 |
| Forêt de Navès (42) | Navès › Solsonès | 26 |
| Forêt de Balaguer (3) | Balaguer › Noguera | 26 |
| Forêt de Alt Àneu (53) | Alt Àneu › Pallars Sobirà | 26 |
| Forêt de Gósol (21) | Gósol › Berguedà (Lérida) | 26 |
| Forêt de Cava (9) | Cava › Alt Urgell | 26 |
| Forêt de Guixers (94) | Guixers › Solsonès | 26 |
| Forêt de Josa i Tuixén (21) | Josa i Tuixén › Alt Urgell | 26 |
| Forêt de Guixers (101) | Gósol › Berguedà (Lérida) | 26 |
| Forêt de Sant Llorenç de Morunys (33) | Sant Llorenç de Morunys › Solsonès | 26 |
| Forêt de Sant Esteve de la Sarga (30) | Sant Esteve de la Sarga › Pallars Jussà | 26 |
| Forêt de Àger (55) | Àger › Noguera | 26 |
| Forêt de les Valls de Valira (140) | les Valls de Valira › Alt Urgell | 26 |
| Forêt de les Valls de Valira (141) | les Valls de Valira › Alt Urgell | 26 |
| Forêt de la Seu d'Urgell (20) | la Seu d'Urgell › Alt Urgell | 26 |
| Forêt de Baix Pallars (82) | Baix Pallars › Pallars Sobirà | 26 |
| Forêt de Riner (167) | Riner › Solsonès | 26 |
| Forêt de Juncosa (4) | Juncosa › Garrigues | 25 |
| Forêt de Espot | Espot › Pallars Sobirà | 25 |
| Forêt de Senterada | Senterada › Pallars Jussà | 25 |
| Forêt de Conca de Dalt (8) | Conca de Dalt › Pallars Jussà | 25 |
| Forêt de Tremp (30) | Tremp › Pallars Jussà | 25 |
| Forêt de la Granadella (11) | la Granadella › Garrigues | 25 |
| Forêt de Artesa de Segre (13) | Artesa de Segre › Noguera | 25 |
| Forêt de Lladurs (35) | Lladurs › Solsonès | 25 |
| Forêt de la Pobla de Cérvoles (14) | la Pobla de Cérvoles › Garrigues | 25 |
| Forêt de Gavet de la Conca (8) | Gavet de la Conca › Pallars Jussà | 25 |
| Bois de Oliola | Oliola › Noguera | 25 |
| Forêt de Gimenells i el Pla de la Font (11) | Gimenells i el Pla de la Font › Segrià | 25 |
| Forêt de Gimenells i el Pla de la Font (13) | Gimenells i el Pla de la Font › Segrià | 25 |
| Forêt de Alt Àneu (42) | Alt Àneu › Pallars Sobirà | 25 |
| Forêt de les Valls de Valira (23) | les Valls de Valira › Alt Urgell | 25 |
| Forêt de la Molsosa (78) | la Molsosa › Solsonès | 25 |
| Forêt de les Valls de Valira (30) | les Valls de Valira › Alt Urgell | 25 |
| Forêt de Vielha e Mijaran (52) | Vielha e Mijaran › Val d'Aran | 25 |
| Forêt de Esterri de Cardós (8) | Esterri de Cardós › Pallars Sobirà | 25 |
| Forêt de Montellà i Martinet (33) | Montellà i Martinet › Cerdanya (Lérida) | 25 |
| Forêt de Guixers (112) | Guixers › Solsonès | 25 |
| Forêt de Lladurs (216) | Lladurs › Solsonès | 25 |
| Forêt de Lladurs (219) | Lladurs › Solsonès | 25 |
| Bois de Vallbona de les Monges (12) | Vallbona de les Monges › Urgell | 25 |
| Forêt de Alt Àneu (108) | Alt Àneu › Pallars Sobirà | 25 |
| Forêt de Alt Àneu (131) | Alt Àneu › Pallars Sobirà | 25 |
| Forêt de Naut Aran (115) | Naut Aran › Val d'Aran | 25 |
| Forêt de Arsèguel (3) | Arsèguel › Alt Urgell | 25 |
| Forêt de Bellver de Cerdanya (70) | Bellver de Cerdanya › Cerdanya (Lérida) | 25 |
| Forêt de Montferrer i Castellbò (65) | Montferrer i Castellbò › Alt Urgell | 25 |
| Forêt de Coll de Nargó (90) | Coll de Nargó › Alt Urgell | 25 |
| Forêt de Cava (19) | Cava › Alt Urgell | 25 |
| Forêt de Sant Esteve de la Sarga (33) | Sant Esteve de la Sarga › Pallars Jussà | 25 |
| Forêt de Os de Balaguer (63) | Os de Balaguer › Noguera | 25 |
| Forêt de Algerri (3) | Algerri › Noguera | 25 |
| Forêt de el Pont de Suert (77) | el Pont de Suert › Alta Ribagorça | 25 |
| Forêt de Ivars de Noguera (21) | Ivars de Noguera › Noguera | 25 |
| Forêt de Farrera (31) | Farrera › Pallars Sobirà | 25 |
| Forêt de Alàs i Cerc (18) | Alàs i Cerc › Alt Urgell | 25 |
| Forêt de Riner (162) | Riner › Solsonès | 25 |
| Forêt de la Baronia de Rialb | la Baronia de Rialb › Noguera | 24 |
| Forêt de Artesa de Segre | Artesa de Segre › Noguera | 24 |
| Forêt de la Granadella | la Granadella › Garrigues | 24 |
| Forêt de Pinell de Solsonès (4) | Pinell de Solsonès › Solsonès | 24 |
| Forêt de Tremp (11) | Tremp › Pallars Jussà | 24 |
| Forêt de Vilanova de l'Aguda | Vilanova de l'Aguda › Noguera | 24 |
| Bois de Vallbona de les Monges (4) | Vallbona de les Monges › Urgell | 24 |
| Forêt de la Baronia de Rialb (12) | la Baronia de Rialb › Noguera | 24 |
| Forêt de Coll de Nargó (8) | Coll de Nargó › Alt Urgell | 24 |
| Forêt de Senterada (3) | Senterada › Pallars Jussà | 24 |
| Forêt de Vall de Cardós (9) | Vall de Cardós › Pallars Sobirà | 24 |
| Forêt de Tremp (35) | Tremp › Pallars Jussà | 24 |
| Forêt de Juncosa (16) | Juncosa › Garrigues | 24 |
| Forêt de Vall de Cardós (15) | Vall de Cardós › Pallars Sobirà | 24 |
| Forêt de Vinaixa (10) | Vinaixa › Garrigues | 24 |
| Forêt de Bellver de Cerdanya (10) | Bellver de Cerdanya › Cerdanya (Lérida) | 24 |
| Forêt de el Pont de Suert (32) | el Pont de Suert › Alta Ribagorça | 24 |
| Forêt de Navès (35) | Navès › Solsonès | 24 |
| Forêt de Coll de Nargó (68) | Coll de Nargó › Alt Urgell | 24 |
| Forêt de Odèn (47) | Odèn › Solsonès | 24 |
| Forêt de Navès (127) | Navès › Solsonès | 24 |
| Forêt de Navès (132) | Navès › Solsonès | 24 |
| Forêt de la Coma i la Pedra (114) | la Coma i la Pedra › Solsonès | 24 |
| Forêt de Alins (39) | Alins › Pallars Sobirà | 24 |
| Forêt de la Coma i la Pedra (125) | la Coma i la Pedra › Solsonès | 24 |
| Forêt de Torà (27) | Torà › Solsonès | 24 |
| Forêt de la Coma i la Pedra (156) | la Coma i la Pedra › Solsonès | 24 |
| Forêt de Odèn (76) | Odèn › Solsonès | 24 |
| Forêt de Odèn (103) | Odèn › Solsonès | 24 |
| Forêt de Lladurs (209) | Lladurs › Solsonès | 24 |
| Forêt de Lladurs (223) | Lladurs › Solsonès | 24 |
| Forêt de Alt Àneu (115) | Alt Àneu › Pallars Sobirà | 24 |
| Forêt de Vilamòs (8) | Vilamòs › Val d'Aran | 24 |
| Forêt de Estamariu (9) | Estamariu › Alt Urgell | 24 |
| Forêt de Cava (20) | Cava › Alt Urgell | 24 |
| Forêt de Montferrer i Castellbò (81) | Montferrer i Castellbò › Alt Urgell | 24 |
| Forêt de Tremp (85) | Tremp › Pallars Jussà | 24 |
| Forêt de Lladorre (46) | Lladorre › Pallars Sobirà | 24 |
| Forêt de Castell de Mur (31) | Castell de Mur › Pallars Jussà | 24 |
| Forêt de Sant Esteve de la Sarga (61) | Sant Esteve de la Sarga › Pallars Jussà | 24 |
| Forêt de Àger (77) | Àger › Noguera | 24 |
| Forêt de Ivars de Noguera (12) | Ivars de Noguera › Noguera | 24 |
| Forêt de Coll de Nargó (109) | Coll de Nargó › Alt Urgell | 24 |
| Forêt de Coll de Nargó (116) | Coll de Nargó › Alt Urgell | 24 |
| Forêt de Baix Pallars (69) | Baix Pallars › Pallars Sobirà | 24 |
| Forêt de Llavorsí (63) | Llavorsí › Pallars Sobirà | 24 |
| Forêt de Estamariu (17) | Estamariu › Alt Urgell | 24 |
| Forêt de Montferrer i Castellbò (95) | Montferrer i Castellbò › Alt Urgell | 24 |
| Forêt de les Valls de Valira (148) | les Valls de Valira › Alt Urgell | 24 |
| Forêt de Riner (164) | Riner › Solsonès | 24 |
| Forêt de Soriguera (58) | Soriguera › Pallars Sobirà | 24 |
| Forêt de Tremp (10) | Tremp › Pallars Jussà | 23 |
| Forêt de Alàs i Cerc (2) | Alàs i Cerc › Alt Urgell | 23 |
| Forêt de la Granadella (7) | la Granadella › Garrigues | 23 |
| Forêt de la Granadella (8) | la Granadella › Garrigues | 23 |
| Forêt de Solsona | Solsona › Solsonès | 23 |
| Forêt de Vilanova de l'Aguda (4) | Vilanova de l'Aguda › Noguera | 23 |
| Forêt de les Valls d'Aguilar (15) | les Valls d'Aguilar › Alt Urgell | 23 |
| Forêt de la Pobla de Segur (5) | la Pobla de Segur › Pallars Jussà | 23 |
| Forêt de Sant Esteve de la Sarga (3) | Sant Esteve de la Sarga › Pallars Jussà | 23 |
| Forêt de Vall de Cardós (16) | Vall de Cardós › Pallars Sobirà | 23 |
| Forêt de Lladurs (37) | Lladurs › Solsonès | 23 |
| Forêt de Tremp (44) | Tremp › Pallars Jussà | 23 |
| Forêt de Torà (5) | Torà › Solsonès | 23 |
| Forêt de la Coma i la Pedra (91) | la Coma i la Pedra › Solsonès | 23 |
| Bois de Peramola | Peramola › Alt Urgell | 23 |
| Forêt de Lladurs (51) | Lladurs › Solsonès | 23 |
| Forêt de Espot (28) | Espot › Pallars Sobirà | 23 |
| Forêt de la Vall de Boí (250) | la Vall de Boí › Alta Ribagorça | 23 |
| Forêt de Vielha e Mijaran (10) | Vielha e Mijaran › Val d'Aran | 23 |
| Forêt de Vilaller (27) | Vilaller › Alta Ribagorça | 23 |
| Forêt de Torà (19) | Torà › Solsonès | 23 |
| Bois de Bellver de Cerdanya (4) | Bellver de Cerdanya › Cerdanya (Lérida) | 23 |
| Forêt de Llavorsí (19) | Llavorsí › Pallars Sobirà | 23 |
| Forêt de Gósol (20) | Gósol › Berguedà (Lérida) | 23 |
| Forêt de Pinós (103) | Pinós › Solsonès | 23 |
| Forêt de Bellver de Cerdanya (45) | Bellver de Cerdanya › Cerdanya (Lérida) | 23 |
| Forêt de Guixers (72) | Guixers › Solsonès | 23 |
| Forêt de la Coma i la Pedra (168) | la Coma i la Pedra › Solsonès | 23 |
| Forêt de Gósol (100) | Gósol › Berguedà (Lérida) | 23 |
| Forêt de Lladorre (25) | Lladorre › Pallars Sobirà | 23 |
| Forêt de les Valls de Valira (67) | les Valls de Valira › Alt Urgell | 23 |
| Forêt de Tremp (84) | Tremp › Pallars Jussà | 23 |
| Forêt de Olius (333) | Olius › Solsonès | 23 |
| Forêt de Lladurs (267) | Lladurs › Solsonès | 23 |
| Forêt de Olius (354) | Olius › Solsonès | 23 |
| Forêt de Lladorre (40) | Lladorre › Pallars Sobirà | 23 |
| Forêt de Clariana de Cardener (188) | Clariana de Cardener › Solsonès | 23 |
| Forêt de Os de Balaguer (59) | Os de Balaguer › Noguera | 23 |
| Forêt de Coll de Nargó (124) | Coll de Nargó › Alt Urgell | 23 |
| Forêt de Tremp (128) | Tremp › Pallars Jussà | 23 |
| Forêt de Alins (113) | Alins › Pallars Sobirà | 23 |
| Forêt de el Pont de Bar (36) | el Pont de Bar › Alt Urgell | 23 |
| Forêt de Almatret (11) | Almatret › Segrià | 23 |
| Forêt de Montferrer i Castellbò (106) | Montferrer i Castellbò › Alt Urgell | 23 |
| Forêt de Lladurs (273) | Lladurs › Solsonès | 23 |
| Forêt de Sort (35) | Sort › Pallars Sobirà | 23 |
| Forêt de Soriguera (53) | Soriguera › Pallars Sobirà | 23 |
| Forêt de Vall de Cardós (3) | Vall de Cardós › Pallars Sobirà | 22 |
| Forêt de Cabó | Cabó › Alt Urgell | 22 |
| Forêt de Tarrés (6) | Tarrés › Garrigues | 22 |
| Forêt de Lladurs (20) | Lladurs › Solsonès | 22 |
| Forêt de Maials (10) | Maials › Segrià | 22 |
| Forêt de Bovera (6) | Bovera › Garrigues | 22 |
| Forêt de Torrefeta i Florejacs | Torrefeta i Florejacs › Segarra | 22 |
| Forêt de Talavera (7) | Talavera › Segarra | 22 |
| Forêt de Navès | Navès › Solsonès | 22 |
| Forêt de la Vall de Boí (5) | la Vall de Boí › Alta Ribagorça | 22 |
| Forêt de les Valls de Valira (8) | les Valls de Valira › Alt Urgell | 22 |
| Forêt de Conca de Dalt (19) | Conca de Dalt › Pallars Jussà | 22 |
| Forêt de Clariana de Cardener (158) | Clariana de Cardener › Solsonès | 22 |
| Forêt de Algerri (2) | Algerri › Noguera | 22 |
| Forêt de Bellver de Cerdanya (13) | Bellver de Cerdanya › Cerdanya (Lérida) | 22 |
| Forêt de Pinell de Solsonès (37) | Pinell de Solsonès › Solsonès | 22 |
| Forêt de Ribera d'Urgellet (36) | Ribera d'Urgellet › Alt Urgell | 22 |
| Forêt de Fígols i Alinyà (27) | Fígols i Alinyà › Alt Urgell | 22 |
| Forêt de Pinós (50) | Pinós › Solsonès | 22 |
| Forêt de Pinós (82) | Pinós › Solsonès | 22 |
| Forêt de la Guingueta d'Àneu (43) | la Guingueta d'Àneu › Pallars Sobirà | 22 |
| Forêt de les Valls de Valira (35) | les Valls de Valira › Alt Urgell | 22 |
| Forêt de la Coma i la Pedra (139) | la Coma i la Pedra › Solsonès | 22 |
| Forêt de la Coma i la Pedra (150) | la Coma i la Pedra › Solsonès | 22 |
| Forêt de Naut Aran (87) | Naut Aran › Val d'Aran | 22 |
| Forêt de Canejan (31) | Canejan › Val d'Aran | 22 |
| Forêt de Vielha e Mijaran (81) | Vielha e Mijaran › Val d'Aran | 22 |
| Forêt de Peramola (22) | Peramola › Alt Urgell | 22 |
| Forêt de Montferrer i Castellbò (80) | Montferrer i Castellbò › Alt Urgell | 22 |
| Forêt de Coll de Nargó (100) | Coll de Nargó › Alt Urgell | 22 |
| Forêt de Coll de Nargó (113) | Coll de Nargó › Alt Urgell | 22 |
| Forêt de la Pobla de Segur (13) | la Pobla de Segur › Pallars Jussà | 22 |
| Forêt de Castell de Mur (33) | Castell de Mur › Pallars Jussà | 22 |
| Forêt de Alins (84) | Alins › Pallars Sobirà | 22 |
| Bois de Vallbona de les Monges | Vallbona de les Monges › Urgell | 21 |
| Forêt de Tremp (13) | Tremp › Pallars Jussà | 21 |
| Forêt de Vilanova de Meià (3) | Vilanova de Meià › Noguera | 21 |
| Forêt de la Pobla de Segur (2) | la Pobla de Segur › Pallars Jussà | 21 |
| Bois de Maldà | Maldà › Urgell | 21 |
| Forêt de la Vansa i Fórnols (7) | la Vansa i Fórnols › Alt Urgell | 21 |
| Forêt de Lladurs (11) | Lladurs › Solsonès | 21 |
| Forêt de Juncosa (7) | Juncosa › Garrigues | 21 |
| Forêt de Fígols i Alinyà (3) | Fígols i Alinyà › Alt Urgell | 21 |
| Forêt de Canejan (2) | Canejan › Val d'Aran | 21 |
| Forêt de la Baronia de Rialb (20) | la Baronia de Rialb › Noguera | 21 |
| Forêt de Conca de Dalt (7) | Conca de Dalt › Pallars Jussà | 21 |
| Forêt de Tremp (27) | Tremp › Pallars Jussà | 21 |
| Bosc dels Masets | Guimerà › Urgell | 21 |
| Forêt de Tremp (28) | Tremp › Pallars Jussà | 21 |
| Forêt de Vinaixa (6) | Vinaixa › Garrigues | 21 |
| Forêt de els Torms (2) | els Torms › Garrigues | 21 |
| Forêt de Tremp (36) | Tremp › Pallars Jussà | 21 |
| Forêt de Tremp (38) | Tremp › Pallars Jussà | 21 |
| Forêt de Sarroca de Bellera (5) | Sarroca de Bellera › Pallars Jussà | 21 |
| Forêt de Ribera d'Ondara (5) | Ribera d'Ondara › Segarra | 21 |
| Forêt de Lladurs (42) | Lladurs › Solsonès | 21 |
| Forêt de l'Albagés (2) | l'Albagés › Garrigues | 21 |
| Forêt de Tremp (45) | Tremp › Pallars Jussà | 21 |
| Forêt de el Pont de Suert (16) | el Pont de Suert › Alta Ribagorça | 21 |
| Forêt de la Coma i la Pedra (60) | la Coma i la Pedra › Solsonès | 21 |
| Forêt de Pinós (14) | Pinós › Solsonès | 21 |
| Forêt de Odèn (29) | Odèn › Solsonès | 21 |
| Forêt de Lles de Cerdanya (21) | Lles de Cerdanya › Cerdanya (Lérida) | 21 |
| Forêt de Alt Àneu (40) | Alt Àneu › Pallars Sobirà | 21 |
| Forêt de Vielha e Mijaran (13) | Vielha e Mijaran › Val d'Aran | 21 |
| Forêt de Naut Aran (49) | Naut Aran › Val d'Aran | 21 |
| Forêt de Vielha e Mijaran (50) | Vielha e Mijaran › Val d'Aran | 21 |
| Forêt de Navès (113) | Navès › Solsonès | 21 |
| Forêt de Alcoletge (3) | Alcoletge › Segrià | 21 |
| Forêt de Guixers (54) | Guixers › Solsonès | 21 |
| Bois de Llobera | Llobera › Solsonès | 21 |
| Forêt de Navès (137) | Navès › Solsonès | 21 |
| Forêt de la Coma i la Pedra (117) | la Coma i la Pedra › Solsonès | 21 |
| Forêt de la Molsosa (64) | la Molsosa › Solsonès | 21 |
| Forêt de la Molsosa (81) | la Molsosa › Solsonès | 21 |
| Forêt de Bellver de Cerdanya (36) | Bellver de Cerdanya › Cerdanya (Lérida) | 21 |
| Forêt de Alt Àneu (78) | Alt Àneu › Pallars Sobirà | 21 |
| Forêt de Llavorsí (46) | Llavorsí › Pallars Sobirà | 21 |
| Forêt de Estamariu (5) | Estamariu › Alt Urgell | 21 |
| Forêt de les Valls de Valira (81) | les Valls de Valira › Alt Urgell | 21 |
| Forêt de Cava (17) | Cava › Alt Urgell | 21 |
| Forêt de Olius (347) | Olius › Solsonès | 21 |
| Forêt de Farrera (18) | Farrera › Pallars Sobirà | 21 |
| Forêt de Espot (56) | Espot › Pallars Sobirà | 21 |
| Forêt de la Guingueta d'Àneu (88) | Espot › Pallars Sobirà | 21 |
| Forêt de el Pont de Bar (22) | el Pont de Bar › Alt Urgell | 21 |
| Forêt de la Vall de Boí (274) | la Vall de Boí › Alta Ribagorça | 21 |
| Forêt de el Pont de Bar (54) | el Pont de Bar › Alt Urgell | 21 |
| Forêt de Montferrer i Castellbò (115) | Montferrer i Castellbò › Alt Urgell | 21 |
| Forêt de Coll de Nargó | Coll de Nargó › Alt Urgell | 20 |
| Forêt de Lladurs (8) | Lladurs › Solsonès | 20 |
| Forêt de les Avellanes i Santa Linya (2) | les Avellanes i Santa Linya › Noguera | 20 |
| Forêt de Coll de Nargó (6) | Coll de Nargó › Alt Urgell | 20 |
| Forêt de Pinell de Solsonès (11) | Pinell de Solsonès › Solsonès | 20 |
| Forêt de la Baronia de Rialb (16) | la Baronia de Rialb › Noguera | 20 |
| Forêt de la Vall de Boí | la Vall de Boí › Alta Ribagorça | 20 |
| Forêt de Fígols i Alinyà (4) | Fígols i Alinyà › Alt Urgell | 20 |
| Forêt de Pinós (4) | Pinós › Solsonès | 20 |
| Forêt de la Granja d'Escarp (2) | la Granja d'Escarp › Segrià | 20 |
| Forêt de Cava (3) | Cava › Alt Urgell | 20 |
| Forêt de la Guingueta d'Àneu (2) | la Guingueta d'Àneu › Pallars Sobirà | 20 |
| Forêt de Ribera d'Ondara (4) | Ribera d'Ondara › Segarra | 20 |
| Forêt de Vilanova de Meià (11) | Vilanova de Meià › Noguera | 20 |
| Forêt de Lladurs (34) | Lladurs › Solsonès | 20 |
| Forêt de Conca de Dalt (15) | Conca de Dalt › Pallars Jussà | 20 |
| Forêt de la Pobla de Segur (7) | la Pobla de Segur › Pallars Jussà | 20 |
| Forêt de Os de Balaguer (8) | Os de Balaguer › Noguera | 20 |
| Forêt de la Vall de Boí (6) | la Vall de Boí › Alta Ribagorça | 20 |
| Forêt de les Avellanes i Santa Linya (11) | les Avellanes i Santa Linya › Noguera | 20 |
| Forêt de Coll de Nargó (22) | Coll de Nargó › Alt Urgell | 20 |
| Forêt de Tremp (60) | Tremp › Pallars Jussà | 20 |
| Forêt de Pinós (39) | Pinós › Solsonès | 20 |
| Forêt de Tremp (73) | Tremp › Pallars Jussà | 20 |
| Forêt de Espot (34) | Espot › Pallars Sobirà | 20 |
| Forêt de Esterri d'Àneu (3) | Esterri d'Àneu › Pallars Sobirà | 20 |
| Forêt de Coll de Nargó (34) | Coll de Nargó › Alt Urgell | 20 |
| Forêt de Térmens (10) | Térmens › Noguera | 20 |
| Forêt de Navès (61) | Navès › Solsonès | 20 |
| Forêt de Àger (26) | Àger › Noguera | 20 |
| Forêt de Prullans (6) | Prullans › Cerdanya (Lérida) | 20 |
| Bois de Talavera (55) | Talavera › Segarra | 20 |
| Forêt de Torres de Segre (10) | Torres de Segre › Segrià | 20 |
| Forêt de Talavera (26) | Talavera › Segarra | 20 |
| Forêt de Odèn (51) | Odèn › Solsonès | 20 |
| Forêt de Odèn (52) | Odèn › Solsonès | 20 |
| Forêt de Cabó (11) | Cabó › Alt Urgell | 20 |
| Forêt de Pinós (135) | Pinós › Solsonès | 20 |
| Forêt de Montellà i Martinet (27) | Montellà i Martinet › Cerdanya (Lérida) | 20 |
| Forêt de Montellà i Martinet (29) | Montellà i Martinet › Cerdanya (Lérida) | 20 |
| Forêt de la Coma i la Pedra (153) | la Coma i la Pedra › Solsonès | 20 |
| Forêt de Alins (49) | Alins › Pallars Sobirà | 20 |
| Forêt de la Baronia de Rialb (47) | la Baronia de Rialb › Noguera | 20 |
| Forêt de Montferrer i Castellbò (84) | Montferrer i Castellbò › Alt Urgell | 20 |
| Forêt de Olius (345) | Olius › Solsonès | 20 |
| Forêt de Lladurs (259) | Lladurs › Solsonès | 20 |
| Forêt de Baix Pallars (46) | Baix Pallars › Pallars Sobirà | 20 |
| Forêt de Baix Pallars (53) | Baix Pallars › Pallars Sobirà | 20 |
| Forêt de Camarasa (44) | Camarasa › Noguera | 20 |
| Forêt de Àger (86) | Àger › Noguera | 20 |
| Forêt de Àger (110) | Àger › Noguera | 20 |
| Forêt de Coll de Nargó (107) | Coll de Nargó › Alt Urgell | 20 |
| Forêt de Abella de la Conca (35) | Abella de la Conca › Pallars Jussà | 20 |
| Forêt de Abella de la Conca (51) | Abella de la Conca › Pallars Jussà | 20 |
| Forêt de Llobera (511) | Llobera › Solsonès | 20 |
| Forêt de Torà (36) | Torà › Solsonès | 20 |
| Forêt de Llavorsí (64) | Llavorsí › Pallars Sobirà | 20 |
| Forêt de Espot (53) | Espot › Pallars Sobirà | 20 |
| Forêt de Estamariu (13) | Estamariu › Alt Urgell | 20 |
| Forêt de el Pont de Bar (46) | el Pont de Bar › Alt Urgell | 20 |
| Forêt de les Valls de Valira (147) | les Valls de Valira › Alt Urgell | 20 |
| Forêt de Soriguera (49) | Soriguera › Pallars Sobirà | 20 |
| Forêt de la Vansa i Fórnols | la Vansa i Fórnols › Alt Urgell | 19 |
| Forêt de Isona i Conca Dellà | Isona i Conca Dellà › Pallars Jussà | 19 |
| Forêt de Vilaller (2) | Vilaller › Alta Ribagorça | 19 |
| Forêt de Conca de Dalt (2) | Conca de Dalt › Pallars Jussà | 19 |
| Forêt de Pinell de Solsonès (2) | Pinell de Solsonès › Solsonès | 19 |
| Forêt de la Baronia de Rialb (4) | la Baronia de Rialb › Noguera | 19 |
| Forêt de les Valls d'Aguilar (4) | les Valls d'Aguilar › Alt Urgell | 19 |
| Forêt de Lladurs (3) | Lladurs › Solsonès | 19 |
| Forêt de Lladurs (5) | Lladurs › Solsonès | 19 |
| Forêt de Gavet de la Conca | Gavet de la Conca › Pallars Jussà | 19 |
| Forêt de l'Albagés | l'Albagés › Garrigues | 19 |
| Forêt de la Torre de Cabdella (5) | la Torre de Cabdella › Pallars Jussà | 19 |
| Forêt de Alins (7) | Alins › Pallars Sobirà | 19 |
| Forêt de Lladorre (2) | Lladorre › Pallars Sobirà | 19 |
| Forêt de Clariana de Cardener (3) | Clariana de Cardener › Solsonès | 19 |
| Forêt de Pinós (6) | Pinós › Solsonès | 19 |
| Forêt de Àger (6) | Àger › Noguera | 19 |
| Forêt de Juncosa (21) | Juncosa › Garrigues | 19 |
| Forêt de Seròs (2) | Seròs › Segrià | 19 |
| Forêt de Abella de la Conca (2) | Abella de la Conca › Pallars Jussà | 19 |
| Forêt de la Torre de Cabdella (14) | la Torre de Cabdella › Pallars Jussà | 19 |
| Forêt de Tremp (68) | Tremp › Pallars Jussà | 19 |
| Forêt de la Guingueta d'Àneu (15) | la Guingueta d'Àneu › Pallars Sobirà | 19 |
| Forêt de les Avellanes i Santa Linya (13) | les Avellanes i Santa Linya › Noguera | 19 |
| Forêt de Lladorre (18) | Lladorre › Pallars Sobirà | 19 |
| Forêt de Castell de Mur (7) | Castell de Mur › Pallars Jussà | 19 |
| Forêt de Vielha e Mijaran (11) | Vielha e Mijaran › Val d'Aran | 19 |
| Forêt de Guixers (29) | Guixers › Solsonès | 19 |
| Forêt de Camarasa (25) | Camarasa › Noguera | 19 |
| Forêt de Odèn (38) | Odèn › Solsonès | 19 |
| Forêt de Pinós (59) | Pinós › Solsonès | 19 |
| Forêt de Esterri de Cardós (9) | Esterri de Cardós › Pallars Sobirà | 19 |
| Forêt de Pinós (134) | Pinós › Solsonès | 19 |
| Forêt de Torà (28) | Torà › Solsonès | 19 |
| Forêt de Montellà i Martinet (23) | Montellà i Martinet › Cerdanya (Lérida) | 19 |
| Forêt de Navès (149) | Navès › Solsonès | 19 |
| Forêt de Guixers (92) | Guixers › Solsonès | 19 |
| Forêt de la Coma i la Pedra (140) | la Coma i la Pedra › Solsonès | 19 |
| Forêt de la Coma i la Pedra (163) | la Coma i la Pedra › Solsonès | 19 |
| Forêt de Guixers (113) | Guixers › Solsonès | 19 |
| Forêt de Gósol (64) | Gósol › Berguedà (Lérida) | 19 |
| Forêt de Naut Aran (79) | Naut Aran › Val d'Aran | 19 |
| Forêt de Llavorsí (38) | Llavorsí › Pallars Sobirà | 19 |
| Forêt de les Valls de Valira (88) | les Valls de Valira › Alt Urgell | 19 |
| Forêt de Cabó (34) | Cabó › Alt Urgell | 19 |
| Forêt de Prats i Sansor (5) | Prats i Sansor › Cerdanya (Lérida) | 19 |
| Forêt de Lladurs (270) | Lladurs › Solsonès | 19 |
| Forêt de Sant Esteve de la Sarga (32) | Sant Esteve de la Sarga › Pallars Jussà | 19 |
| Forêt de Àger (129) | Àger › Noguera | 19 |
| Forêt de Àger (166) | Àger › Noguera | 19 |
| Forêt de Coll de Nargó (103) | Coll de Nargó › Alt Urgell | 19 |
| Forêt de Abella de la Conca (57) | Abella de la Conca › Pallars Jussà | 19 |
| Forêt de Baix Pallars (77) | Baix Pallars › Pallars Sobirà | 19 |
| Forêt de Tremp (104) | Tremp › Pallars Jussà | 19 |
| Forêt de Tremp (120) | Tremp › Pallars Jussà | 19 |
| Forêt de les Valls de Valira (130) | les Valls de Valira › Alt Urgell | 19 |
| Forêt de el Pont de Bar (45) | el Pont de Bar › Alt Urgell | 19 |
| Forêt de Montferrer i Castellbò (93) | Montferrer i Castellbò › Alt Urgell | 19 |
| Forêt de les Valls de Valira (146) | les Valls de Valira › Alt Urgell | 19 |
| Forêt de Odèn (137) | Odèn › Solsonès | 19 |
| Forêt de Sort (27) | Sort › Pallars Sobirà | 19 |
| Forêt de Lladorre (48) | Lladorre › Pallars Sobirà | 19 |
| Forêt de Tremp (4) | Tremp › Pallars Jussà | 18 |
| Forêt de les Avellanes i Santa Linya | les Avellanes i Santa Linya › Noguera | 18 |
| Forêt de Bellaguarda (3) | Bellaguarda › Garrigues | 18 |
| Forêt de la Baronia de Rialb (15) | la Baronia de Rialb › Noguera | 18 |
| Pineda del Molí | Sant Martí de Riucorb › Urgell | 18 |
| Forêt de Coll de Nargó (10) | Coll de Nargó › Alt Urgell | 18 |
| Forêt de Lladurs (23) | Lladurs › Solsonès | 18 |
| Forêt de Àger (4) | Àger › Noguera | 18 |
| Forêt de la Vansa i Fórnols (11) | la Vansa i Fórnols › Alt Urgell | 18 |
| Forêt de Vall de Cardós (10) | Esterri de Cardós › Pallars Sobirà | 18 |
| Forêt de Tremp (37) | Tremp › Pallars Jussà | 18 |
| Forêt de Prullans (2) | Prullans › Cerdanya (Lérida) | 18 |
| Bois de Torrefeta i Florejacs (2) | Torrefeta i Florejacs › Segarra | 18 |
| Forêt de la Torre de Cabdella (13) | la Torre de Cabdella › Pallars Jussà | 18 |
| Forêt de la Guingueta d'Àneu (7) | la Guingueta d'Àneu › Pallars Sobirà | 18 |
| Forêt de Vilanova de Meià (15) | Vilanova de Meià › Noguera | 18 |
| Forêt de Aitona (6) | Aitona › Segrià | 18 |
| Forêt de Pinós (38) | Pinós › Solsonès | 18 |
| Forêt de la Seu d'Urgell (3) | la Seu d'Urgell › Alt Urgell | 18 |
| Bois de Sant Esteve de la Sarga | Sant Esteve de la Sarga › Pallars Jussà | 18 |
| Forêt de Lles de Cerdanya (18) | Lles de Cerdanya › Cerdanya (Lérida) | 18 |
| Forêt de Navès (28) | Navès › Solsonès | 18 |
| Forêt de Coll de Nargó (31) | Coll de Nargó › Alt Urgell | 18 |
| Forêt de Isona i Conca Dellà (29) | Isona i Conca Dellà › Pallars Jussà | 18 |
| Forêt de Vielha e Mijaran (37) | Vielha e Mijaran › Val d'Aran | 18 |
| Forêt de Camarasa (21) | Camarasa › Noguera | 18 |
| Forêt de Corbins | Lleida › Segrià | 18 |
| Forêt de Bassella (21) | Bassella › Alt Urgell | 18 |
| Forêt de Olius (317) | Olius › Solsonès | 18 |
| Forêt de Prullans (9) | Prullans › Cerdanya (Lérida) | 18 |
| Forêt de Odèn (45) | Odèn › Solsonès | 18 |
| Forêt de Lladurs (177) | Lladurs › Solsonès | 18 |
| Forêt de Olius (325) | Olius › Solsonès | 18 |
| Forêt de la Coma i la Pedra (112) | la Coma i la Pedra › Solsonès | 18 |
| Forêt de la Molsosa (50) | la Molsosa › Solsonès | 18 |
| Forêt de Pinós (58) | Pinós › Solsonès | 18 |
| Forêt de Pinós (88) | Pinós › Solsonès | 18 |
| Forêt de Llavorsí (18) | Llavorsí › Pallars Sobirà | 18 |
| Forêt de la Guingueta d'Àneu (45) | la Guingueta d'Àneu › Pallars Sobirà | 18 |
| Forêt de Gósol (24) | Gósol › Berguedà (Lérida) | 18 |
| Forêt de Alins (45) | Alins › Pallars Sobirà | 18 |
| Forêt de Riner (156) | Riner › Solsonès | 18 |
| Forêt de Montellà i Martinet (18) | Montellà i Martinet › Cerdanya (Lérida) | 18 |
| Forêt de Montellà i Martinet (24) | Montellà i Martinet › Cerdanya (Lérida) | 18 |
| Forêt de Guixers (121) | Guixers › Solsonès | 18 |
| Forêt de Gósol (99) | Gósol › Berguedà (Lérida) | 18 |
| Forêt de Naut Aran (70) | Naut Aran › Val d'Aran | 18 |
| Forêt de Alt Àneu (144) | Alt Àneu › Pallars Sobirà | 18 |
| Forêt de Rialp (25) | Rialp › Pallars Sobirà | 18 |
| Forêt de les Valls de Valira (115) | les Valls de Valira › Alt Urgell | 18 |
| Forêt de Peramola (23) | Peramola › Alt Urgell | 18 |
| Forêt de Ponts (13) | Ponts › Noguera | 18 |
| Forêt de Olius (342) | Olius › Solsonès | 18 |
| Forêt de Torà (33) | Torà › Solsonès | 18 |
| Forêt de Sant Esteve de la Sarga (16) | Sant Esteve de la Sarga › Pallars Jussà | 18 |
| Forêt de Sant Esteve de la Sarga (62) | Sant Esteve de la Sarga › Pallars Jussà | 18 |
| Forêt de Sant Esteve de la Sarga (64) | Sant Esteve de la Sarga › Pallars Jussà | 18 |
| Forêt de Os de Balaguer (84) | Os de Balaguer › Noguera | 18 |
| Forêt de Coll de Nargó (115) | Coll de Nargó › Alt Urgell | 18 |
| Forêt de la Pobla de Segur (28) | la Pobla de Segur › Pallars Jussà | 18 |
| Forêt de Montferrer i Castellbò (87) | Montferrer i Castellbò › Alt Urgell | 18 |
| Forêt de Alins (75) | Alins › Pallars Sobirà | 18 |
| Forêt de Naut Aran (148) | Naut Aran › Val d'Aran | 18 |
| Forêt de Rialp (28) | Rialp › Pallars Sobirà | 18 |
| Forêt de Lles de Cerdanya (31) | Lles de Cerdanya › Cerdanya (Lérida) | 18 |
| Forêt de Alàs i Cerc (15) | Alàs i Cerc › Alt Urgell | 18 |
| Forêt de la Vall de Boí (276) | la Vall de Boí › Alta Ribagorça | 18 |
| Forêt de Farrera (23) | Farrera › Pallars Sobirà | 18 |
| Forêt de Farrera (27) | Farrera › Pallars Sobirà | 18 |
| Forêt de Alàs i Cerc (23) | Alàs i Cerc › Alt Urgell | 18 |
| Forêt de Montferrer i Castellbò (105) | Montferrer i Castellbò › Alt Urgell | 18 |
| Forêt de Montferrer i Castellbò (107) | Montferrer i Castellbò › Alt Urgell | 18 |
| Forêt de Fulleda (2) | Fulleda › Garrigues | 17 |
| Forêt de Ribera d'Urgellet (2) | Ribera d'Urgellet › Alt Urgell | 17 |
| Forêt de Montoliu de Segarra | Montoliu de Segarra › Segarra | 17 |
| Forêt de Lles de Cerdanya | Lles de Cerdanya › Cerdanya (Lérida) | 17 |
| Forêt de Guixers | Guixers › Solsonès | 17 |
| Forêt de Tremp (14) | Tremp › Pallars Jussà | 17 |
| Forêt de les Valls de Valira (2) | les Valls de Valira › Alt Urgell | 17 |
| Forêt de Tremp (21) | Tremp › Pallars Jussà | 17 |
| Forêt de Isona i Conca Dellà (4) | Isona i Conca Dellà › Pallars Jussà | 17 |
| Forêt de Pinell de Solsonès (18) | Pinell de Solsonès › Solsonès | 17 |
| Forêt de Pinell de Solsonès (19) | Pinell de Solsonès › Solsonès | 17 |
| Forêt de Àger (5) | Àger › Noguera | 17 |
| Forêt de Odèn (5) | Odèn › Solsonès | 17 |
| Forêt de Sant Esteve de la Sarga (2) | Sant Esteve de la Sarga › Pallars Jussà | 17 |
| Forêt de Tremp (40) | Tremp › Pallars Jussà | 17 |
| Bois de els Omells de na Gaia (4) | els Omells de na Gaia › Urgell | 17 |
| Forêt de Pinós (7) | Pinós › Solsonès | 17 |
| Forêt de la Granadella (16) | la Granadella › Garrigues | 17 |
| Forêt de Castell de Mur (3) | Castell de Mur › Pallars Jussà | 17 |
| Forêt de Peramola (3) | Peramola › Alt Urgell | 17 |
| Bois de Agramunt | Agramunt › Urgell | 17 |
| Forêt de la Coma i la Pedra (95) | la Coma i la Pedra › Solsonès | 17 |
| Forêt de Espot (31) | Espot › Pallars Sobirà | 17 |
| Forêt de Bellver de Cerdanya (21) | Bellver de Cerdanya › Cerdanya (Lérida) | 17 |
| Forêt de Odèn (49) | Odèn › Solsonès | 17 |
| Forêt de la Molsosa (72) | la Molsosa › Solsonès | 17 |
| Forêt de Pinós (71) | Pinós › Solsonès | 17 |
| Forêt de Llavorsí (16) | Llavorsí › Pallars Sobirà | 17 |
| Forêt de Lladorre (21) | Lladorre › Pallars Sobirà | 17 |
| Forêt de Guixers (71) | Guixers › Solsonès | 17 |
| Forêt de Gósol (43) | Gósol › Berguedà (Lérida) | 17 |
| Forêt de la Coma i la Pedra (134) | la Coma i la Pedra › Solsonès | 17 |
| Forêt de Gósol (61) | Gósol › Berguedà (Lérida) | 17 |
| Forêt de Odèn (86) | Odèn › Solsonès | 17 |
| Forêt de Josa i Tuixén (28) | Josa i Tuixén › Alt Urgell | 17 |
| Forêt de Alt Àneu (112) | Alt Àneu › Pallars Sobirà | 17 |
| Forêt de Alt Àneu (118) | Alt Àneu › Pallars Sobirà | 17 |
| Forêt de les Valls de Valira (55) | les Valls de Valira › Alt Urgell | 17 |
| Forêt de Cabó (23) | Cabó › Alt Urgell | 17 |
| Forêt de la Baronia de Rialb (49) | la Baronia de Rialb › Noguera | 17 |
| Forêt de Olius (327) | Olius › Solsonès | 17 |
| Forêt de Navès (178) | Navès › Solsonès | 17 |
| Forêt de Lladurs (261) | Lladurs › Solsonès | 17 |
| Forêt de Peramola (32) | Peramola › Alt Urgell | 17 |
| Forêt de Llobera (489) | Llobera › Solsonès | 17 |
| Forêt de Camarasa (45) | Camarasa › Noguera | 17 |
| Forêt de Sant Esteve de la Sarga (47) | Sant Esteve de la Sarga › Pallars Jussà | 17 |
| Forêt de Àger (122) | Àger › Noguera | 17 |
| Forêt de Ivars de Noguera (13) | Ivars de Noguera › Noguera | 17 |
| Forêt de Coll de Nargó (134) | Coll de Nargó › Alt Urgell | 17 |
| Forêt de Tremp (116) | Tremp › Pallars Jussà | 17 |
| Forêt de el Pont de Suert (75) | el Pont de Suert › Alta Ribagorça | 17 |
| Forêt de el Pont de Suert (102) | el Pont de Suert › Alta Ribagorça | 17 |
| Forêt de Tremp (126) | Tremp › Pallars Jussà | 17 |
| Forêt de Llavorsí (57) | Llavorsí › Pallars Sobirà | 17 |
| Forêt de Arsèguel (6) | Arsèguel › Alt Urgell | 17 |
| Forêt de la Vall de Boí (275) | la Vall de Boí › Alta Ribagorça | 17 |
| Forêt de Lladorre (52) | Lladorre › Pallars Sobirà | 17 |
| Forêt de Soriguera (56) | Soriguera › Pallars Sobirà | 17 |
| Forêt de Soriguera (59) | Soriguera › Pallars Sobirà | 17 |
| Forêt de Pinell de Solsonès (8) | Pinell de Solsonès › Solsonès | 16 |
| Forêt de la Vansa i Fórnols (5) | la Vansa i Fórnols › Alt Urgell | 16 |
| Forêt de les Valls d'Aguilar (10) | les Valls d'Aguilar › Alt Urgell | 16 |
| Forêt de Tremp (20) | Tremp › Pallars Jussà | 16 |
| Forêt de Gimenells i el Pla de la Font (4) | Gimenells i el Pla de la Font › Segrià | 16 |
| Forêt de Tremp (23) | Tremp › Pallars Jussà | 16 |
| Forêt de les Avellanes i Santa Linya (4) | les Avellanes i Santa Linya › Noguera | 16 |
| Forêt de la Torre de Cabdella (9) | la Torre de Cabdella › Pallars Jussà | 16 |
| Forêt de Juncosa (13) | Juncosa › Garrigues | 16 |
| Forêt de la Pobla de Segur (4) | la Pobla de Segur › Pallars Jussà | 16 |
| Forêt de Maials (14) | Maials › Segrià | 16 |
| Forêt de Vilaller (11) | Vilaller › Alta Ribagorça | 16 |
| Forêt de Gavet de la Conca (7) | Gavet de la Conca › Pallars Jussà | 16 |
| Forêt de Talavera (8) | Talavera › Segarra | 16 |
| Forêt de Baix Pallars (26) | Baix Pallars › Pallars Sobirà | 16 |
| Forêt de les Valls de Valira (12) | les Valls de Valira › Alt Urgell | 16 |
| Forêt de Sarroca de Bellera (17) | Sarroca de Bellera › Pallars Jussà | 16 |
| Forêt de Torà (11) | Torà › Solsonès | 16 |
| Forêt de Alàs i Cerc (7) | Alàs i Cerc › Alt Urgell | 16 |
| Forêt de Farrera (5) | Farrera › Pallars Sobirà | 16 |
| Forêt de Lladorre (17) | Lladorre › Pallars Sobirà | 16 |
| Forêt de Vielha e Mijaran (23) | Vielha e Mijaran › Val d'Aran | 16 |
| Forêt de Vielha e Mijaran (30) | Vielha e Mijaran › Val d'Aran | 16 |
| Forêt de Naut Aran (54) | Naut Aran › Val d'Aran | 16 |
| Forêt de Talarn (3) | Talarn › Pallars Jussà | 16 |
| Forêt de Navès (59) | Navès › Solsonès | 16 |
| Parc Fluvial del Segre | Lleida › Segrià | 16 |
| Forêt de Coll de Nargó (55) | Coll de Nargó › Alt Urgell | 16 |
| Forêt de Guixers (51) | Guixers › Solsonès | 16 |
| Forêt de la Coma i la Pedra (115) | la Coma i la Pedra › Solsonès | 16 |
| Forêt de la Molsosa (46) | la Molsosa › Solsonès | 16 |
| Forêt de Pinós (67) | Pinós › Solsonès | 16 |
| Forêt de la Molsosa (79) | la Molsosa › Solsonès | 16 |
| Forêt de Pinós (86) | Pinós › Solsonès | 16 |
| Forêt de Conca de Dalt (27) | Conca de Dalt › Pallars Jussà | 16 |
| Forêt de Alt Àneu (52) | Alt Àneu › Pallars Sobirà | 16 |
| Forêt de Torà (29) | Torà › Solsonès | 16 |
| Forêt de la Coma i la Pedra (133) | la Coma i la Pedra › Solsonès | 16 |
| Forêt de Gósol (50) | Gósol › Berguedà (Lérida) | 16 |
| Forêt de Gósol (83) | Gósol › Berguedà (Lérida) | 16 |
| Forêt de Lles de Cerdanya (26) | Lles de Cerdanya › Cerdanya (Lérida) | 16 |
| Forêt de Naut Aran (89) | Naut Aran › Val d'Aran | 16 |
| Forêt de Alt Àneu (116) | Alt Àneu › Pallars Sobirà | 16 |
| Forêt de Peramola (24) | Peramola › Alt Urgell | 16 |
| Forêt de Cabó (28) | Cabó › Alt Urgell | 16 |
| Forêt de Cabó (30) | Cabó › Alt Urgell | 16 |
| Forêt de la Vansa i Fórnols (25) | la Vansa i Fórnols › Alt Urgell | 16 |
| Forêt de la Vansa i Fórnols (28) | la Vansa i Fórnols › Alt Urgell | 16 |
| Forêt de les Valls de Valira (127) | les Valls de Valira › Alt Urgell | 16 |
| Forêt de Tremp (83) | Tremp › Pallars Jussà | 16 |
| Forêt de Àger (96) | Àger › Noguera | 16 |
| Forêt de Àger (107) | Àger › Noguera | 16 |
| Forêt de Àger (112) | Àger › Noguera | 16 |
| Forêt de Àger (168) | Àger › Noguera | 16 |
| Forêt de Os de Balaguer (47) | Os de Balaguer › Noguera | 16 |
| Forêt de Os de Balaguer (70) | Os de Balaguer › Noguera | 16 |
| Forêt de Ivars de Noguera (16) | Ivars de Noguera › Noguera | 16 |
| Forêt de Os de Balaguer (75) | Os de Balaguer › Noguera | 16 |
| Forêt de Os de Balaguer (89) | Os de Balaguer › Noguera | 16 |
| Forêt de Abella de la Conca (39) | Abella de la Conca › Pallars Jussà | 16 |
| Forêt de la Pobla de Segur (22) | la Pobla de Segur › Pallars Jussà | 16 |
| Forêt de Tremp (103) | Tremp › Pallars Jussà | 16 |
| Forêt de les Valls de Valira (131) | les Valls de Valira › Alt Urgell | 16 |
| Forêt de Talarn (5) | Talarn › Pallars Jussà | 16 |
| Forêt de Alins (76) | Alins › Pallars Sobirà | 16 |
| Forêt de Llobera (525) | Llobera › Solsonès | 16 |
| Forêt de Esterri d'Àneu (10) | Esterri d'Àneu › Pallars Sobirà | 16 |
| Forêt de Llavorsí (58) | Llavorsí › Pallars Sobirà | 16 |
| Forêt de Espot (52) | Espot › Pallars Sobirà | 16 |
| Forêt de la Guingueta d'Àneu (86) | la Guingueta d'Àneu › Pallars Sobirà | 16 |
| Forêt de el Pont de Bar (24) | el Pont de Bar › Alt Urgell | 16 |
| Forêt de la Vall de Boí (277) | la Vall de Boí › Alta Ribagorça | 16 |
| Forêt de Alàs i Cerc (19) | Alàs i Cerc › Alt Urgell | 16 |
| Forêt de Montferrer i Castellbò (114) | Montferrer i Castellbò › Alt Urgell | 16 |
| Forêt de Baix Pallars | Baix Pallars › Pallars Sobirà | 15 |
| Forêt de la Baronia de Rialb (6) | la Baronia de Rialb › Noguera | 15 |
| Forêt de Cervià de les Garrigues (2) | Cervià de les Garrigues › Garrigues | 15 |
| Forêt de Josa i Tuixén | Josa i Tuixén › Alt Urgell | 15 |
| Forêt de la Vansa i Fórnols (8) | la Vansa i Fórnols › Alt Urgell | 15 |
| Forêt de Cabó (3) | Cabó › Alt Urgell | 15 |
| Bois de Vallbona de les Monges (6) | Vallbona de les Monges › Urgell | 15 |
| Forêt de Gavet de la Conca (3) | Gavet de la Conca › Pallars Jussà | 15 |
| Forêt de Lles de Cerdanya (5) | Lles de Cerdanya › Cerdanya (Lérida) | 15 |
| Forêt de Coll de Nargó (12) | Coll de Nargó › Alt Urgell | 15 |
| Bois de Guimerà (2) | Guimerà › Urgell | 15 |
| Forêt de Cava (4) | Cava › Alt Urgell | 15 |
| Forêt de Vall de Cardós (12) | Vall de Cardós › Pallars Sobirà | 15 |
| Forêt de Espot (3) | Espot › Pallars Sobirà | 15 |
| Forêt de la Granadella (15) | la Granadella › Garrigues | 15 |
| Forêt de Juncosa (20) | Juncosa › Garrigues | 15 |
| Forêt de Pinós (8) | Pinós › Solsonès | 15 |
| Forêt de la Vall de Boí (14) | la Vall de Boí › Alta Ribagorça | 15 |
| Forêt de el Pont de Suert (28) | el Pont de Suert › Alta Ribagorça | 15 |
| Forêt de Vall de Cardós (19) | Vall de Cardós › Pallars Sobirà | 15 |
| Forêt de Coll de Nargó (23) | Coll de Nargó › Alt Urgell | 15 |
| Forêt de Vielha e Mijaran (18) | Vielha e Mijaran › Val d'Aran | 15 |
| Forêt de Vielha e Mijaran (45) | Vielha e Mijaran › Val d'Aran | 15 |
| Forêt de Guixers (32) | Guixers › Solsonès | 15 |
| Forêt de Soriguera (24) | Soriguera › Pallars Sobirà | 15 |
| Forêt de Bossòst (9) | Bossòst › Val d'Aran | 15 |
| Forêt de la Coma i la Pedra (100) | la Coma i la Pedra › Solsonès | 15 |
| Forêt de Navès (73) | Navès › Solsonès | 15 |
| Forêt de Navès (90) | Navès › Solsonès | 15 |
| Bois de Bellver de Cerdanya (6) | Bellver de Cerdanya › Cerdanya (Lérida) | 15 |
| Forêt de Lladurs (184) | Lladurs › Solsonès | 15 |
| Forêt de Pinós (46) | Pinós › Solsonès | 15 |
| Forêt de Odèn (55) | Odèn › Solsonès | 15 |
| Forêt de la Guingueta d'Àneu (47) | la Guingueta d'Àneu › Pallars Sobirà | 15 |
| Forêt de Montferrer i Castellbò (30) | Montferrer i Castellbò › Alt Urgell | 15 |
| Forêt de Conca de Dalt (25) | Conca de Dalt › Pallars Jussà | 15 |
| Forêt de Bellver de Cerdanya (30) | Bellver de Cerdanya › Cerdanya (Lérida) | 15 |
| Forêt de Bellver de Cerdanya (33) | Bellver de Cerdanya › Cerdanya (Lérida) | 15 |
| Forêt de Lladurs (193) | Lladurs › Solsonès | 15 |
| Forêt de Vall de Cardós (57) | Vall de Cardós › Pallars Sobirà | 15 |
| Forêt de Gósol (73) | Gósol › Berguedà (Lérida) | 15 |
| Forêt de Gósol (84) | Gósol › Berguedà (Lérida) | 15 |
| Forêt de Naut Aran (81) | Naut Aran › Val d'Aran | 15 |
| Forêt de Naut Aran (82) | Naut Aran › Val d'Aran | 15 |
| Forêt de Naut Aran (86) | Naut Aran › Val d'Aran | 15 |
| Forêt de Naut Aran (118) | Naut Aran › Val d'Aran | 15 |
| Forêt de Naut Aran (128) | Naut Aran › Val d'Aran | 15 |
| Forêt de Alins (65) | Alins › Pallars Sobirà | 15 |
| Forêt de Vilaller (48) | Vilaller › Alta Ribagorça | 15 |
| Forêt de Cabó (19) | Cabó › Alt Urgell | 15 |
| Forêt de Josa i Tuixén (33) | Josa i Tuixén › Alt Urgell | 15 |
| Forêt de Josa i Tuixén (46) | Josa i Tuixén › Alt Urgell | 15 |
| Forêt de Montellà i Martinet (41) | Montellà i Martinet › Cerdanya (Lérida) | 15 |
| Forêt de Navès (210) | Navès › Solsonès | 15 |
| Forêt de Ribera d'Urgellet (57) | Ribera d'Urgellet › Alt Urgell | 15 |
| Forêt de Olius (361) | Olius › Solsonès | 15 |
| Forêt de Clariana de Cardener (175) | Clariana de Cardener › Solsonès | 15 |
| Forêt de Llobera (487) | Llobera › Solsonès | 15 |
| Forêt de Àger (73) | Àger › Noguera | 15 |
| Forêt de Àger (88) | Àger › Noguera | 15 |
| Forêt de Ivars de Noguera (17) | Ivars de Noguera › Noguera | 15 |
| Forêt de Coll de Nargó (131) | Coll de Nargó › Alt Urgell | 15 |
| Forêt de Farrera (15) | Farrera › Pallars Sobirà | 15 |
| Forêt de Rialp (29) | Rialp › Pallars Sobirà | 15 |
| Forêt de Espot (48) | Espot › Pallars Sobirà | 15 |
| Forêt de la Guingueta d'Àneu (87) | la Guingueta d'Àneu › Pallars Sobirà | 15 |
| Forêt de Lles de Cerdanya (28) | Lles de Cerdanya › Cerdanya (Lérida) | 15 |
| Forêt de el Pont de Bar (29) | el Pont de Bar › Alt Urgell | 15 |
| Forêt de el Pont de Bar (40) | el Pont de Bar › Alt Urgell | 15 |
| Forêt de Farrera (22) | Farrera › Pallars Sobirà | 15 |
| Forêt de Alàs i Cerc (17) | Alàs i Cerc › Alt Urgell | 15 |
| Forêt de Alàs i Cerc (35) | Alàs i Cerc › Alt Urgell | 15 |
| Forêt de Lladurs (277) | Lladurs › Solsonès | 15 |
| Forêt de Conca de Dalt (52) | Conca de Dalt › Pallars Jussà | 15 |
| Forêt de Tremp | Tremp › Pallars Jussà | 14 |
| Forêt de les Valls d'Aguilar (2) | les Valls d'Aguilar › Alt Urgell | 14 |
| Forêt de Soriguera (4) | Soriguera › Pallars Sobirà | 14 |
| Forêt de la Pobla de Cérvoles (5) | la Pobla de Cérvoles › Garrigues | 14 |
| Forêt de Odèn (2) | Odèn › Solsonès | 14 |
| Forêt de Sant Guim de Freixenet | Sant Guim de Freixenet › Segarra | 14 |
| Bois de Vallbona de les Monges (3) | Vallbona de les Monges › Urgell | 14 |
| Forêt de Biosca (4) | Biosca › Solsonès | 14 |
| Forêt de Alt Àneu (4) | Alt Àneu › Pallars Sobirà | 14 |
| Forêt de Biosca (6) | Biosca › Solsonès | 14 |
| Forêt de Juncosa (11) | Juncosa › Garrigues | 14 |
| Forêt de la Pobla de Cérvoles (9) | la Pobla de Cérvoles › Garrigues | 14 |
| Forêt de Pinell de Solsonès (20) | Pinell de Solsonès › Solsonès | 14 |
| Bois de Sant Martí de Riucorb | Sant Martí de Riucorb › Urgell | 14 |
| Bois de els Omells de na Gaia (2) | els Omells de na Gaia › Urgell | 14 |
| Forêt de Clariana de Cardener (2) | Clariana de Cardener › Solsonès | 14 |
| Forêt de Juncosa (17) | Juncosa › Garrigues | 14 |
| Forêt de Baix Pallars (24) | Baix Pallars › Pallars Sobirà | 14 |
| Forêt de Oliola (9) | Oliola › Noguera | 14 |
| Forêt de Juncosa (19) | Juncosa › Garrigues | 14 |
| Forêt de Maials (19) | Maials › Segrià | 14 |
| Forêt de la Coma i la Pedra (81) | la Coma i la Pedra › Solsonès | 14 |
| Forêt de Solsona (88) | Solsona › Solsonès | 14 |
| Forêt de Isona i Conca Dellà (18) | Isona i Conca Dellà › Pallars Jussà | 14 |
| Forêt de Tremp (71) | Tremp › Pallars Jussà | 14 |
| Bois de Sant Esteve de la Sarga (2) | Sant Esteve de la Sarga › Pallars Jussà | 14 |
| Bois de Sant Esteve de la Sarga (3) | Sant Esteve de la Sarga › Pallars Jussà | 14 |
| Forêt de el Pont de Suert (38) | el Pont de Suert › Alta Ribagorça | 14 |
| Forêt de Sort (13) | Sort › Pallars Sobirà | 14 |
| Forêt de Naut Aran (61) | Naut Aran › Val d'Aran | 14 |
| Forêt de Castellar de la Ribera (19) | Castellar de la Ribera › Solsonès | 14 |
| Forêt de el Pont de Suert (42) | el Pont de Suert › Alta Ribagorça | 14 |
| Forêt de Vilanova de la Barca (11) | Vilanova de la Barca › Segrià | 14 |
| Forêt de Balaguer (6) | Balaguer › Noguera | 14 |
| Forêt de Montellà i Martinet (5) | Montellà i Martinet › Cerdanya (Lérida) | 14 |
| Forêt de Olius (321) | Olius › Solsonès | 14 |
| Forêt de Navès (69) | Navès › Solsonès | 14 |
| Forêt de Fígols i Alinyà (31) | Fígols i Alinyà › Alt Urgell | 14 |
| Forêt de la Molsosa (62) | la Molsosa › Solsonès | 14 |
| Forêt de la Molsosa (71) | la Molsosa › Solsonès | 14 |
| Forêt de Conca de Dalt (26) | Conca de Dalt › Pallars Jussà | 14 |
| Forêt de Espot (37) | Espot › Pallars Sobirà | 14 |
| Forêt de Gósol (32) | Gósol › Berguedà (Lérida) | 14 |
| Forêt de Pinós (120) | Pinós › Solsonès | 14 |
| Forêt de Bellver de Cerdanya (38) | Bellver de Cerdanya › Cerdanya (Lérida) | 14 |
| Forêt de Montellà i Martinet (32) | Montellà i Martinet › Cerdanya (Lérida) | 14 |
| Forêt de Cava (7) | Cava › Alt Urgell | 14 |
| Forêt de Navès (150) | Navès › Solsonès | 14 |
| Forêt de Josa i Tuixén (18) | Josa i Tuixén › Alt Urgell | 14 |
| Forêt de Guixers (111) | Guixers › Solsonès | 14 |
| Forêt de Odèn (126) | Odèn › Solsonès | 14 |
| Forêt de Naut Aran (95) | Naut Aran › Val d'Aran | 14 |
| Forêt de Naut Aran (111) | Naut Aran › Val d'Aran | 14 |
| Forêt de les Valls de Valira (45) | les Valls de Valira › Alt Urgell | 14 |
| Forêt de les Valls d'Aguilar (33) | les Valls d'Aguilar › Alt Urgell | 14 |
| Forêt de Cava (15) | Cava › Alt Urgell | 14 |
| Forêt de Olius (344) | Olius › Solsonès | 14 |
| Forêt de Lladorre (41) | Lladorre › Pallars Sobirà | 14 |
| Forêt de Sant Esteve de la Sarga (26) | Sant Esteve de la Sarga › Pallars Jussà | 14 |
| Forêt de Clariana de Cardener (224) | Clariana de Cardener › Solsonès | 14 |
| Forêt de Àger (68) | Àger › Noguera | 14 |
| Forêt de Camarasa (46) | Camarasa › Noguera | 14 |
| Forêt de Castell de Mur (29) | Castell de Mur › Pallars Jussà | 14 |
| Forêt de Sant Esteve de la Sarga (36) | Sant Esteve de la Sarga › Pallars Jussà | 14 |
| Forêt de Sant Esteve de la Sarga (43) | Sant Esteve de la Sarga › Pallars Jussà | 14 |
| Forêt de Sant Esteve de la Sarga (49) | Sant Esteve de la Sarga › Pallars Jussà | 14 |
| Forêt de Os de Balaguer (40) | Os de Balaguer › Noguera | 14 |
| Forêt de Os de Balaguer (44) | Os de Balaguer › Noguera | 14 |
| Forêt de Os de Balaguer (58) | Os de Balaguer › Noguera | 14 |
| Forêt de Coll de Nargó (121) | Coll de Nargó › Alt Urgell | 14 |
| Forêt de Conca de Dalt (34) | Abella de la Conca › Pallars Jussà | 14 |
| Forêt de la Pobla de Segur (30) | la Pobla de Segur › Pallars Jussà | 14 |
| Forêt de Llobera (503) | Llobera › Solsonès | 14 |
| Forêt de Talarn (9) | Talarn › Pallars Jussà | 14 |
| Forêt de Tremp (131) | Tremp › Pallars Jussà | 14 |
| Forêt de Llobera (534) | Llobera › Solsonès | 14 |
| Forêt de Alins (100) | Alins › Pallars Sobirà | 14 |
| Forêt de el Pont de Bar (23) | el Pont de Bar › Alt Urgell | 14 |
| Forêt de Arsèguel (12) | Arsèguel › Alt Urgell | 14 |
| Forêt de Riner (163) | Riner › Solsonès | 14 |
| Forêt de les Valls de Valira (152) | les Valls de Valira › Alt Urgell | 14 |
| Forêt de Soriguera (54) | Soriguera › Pallars Sobirà | 14 |
| Forêt de la Baronia de Rialb (2) | la Baronia de Rialb › Noguera | 13 |
| Forêt de la Pobla de Cérvoles (3) | la Pobla de Cérvoles › Garrigues | 13 |
| Forêt de Juncosa (2) | Juncosa › Garrigues | 13 |
| Forêt de Balaguer | Balaguer › Noguera | 13 |
| Forêt de la Torre de Cabdella | la Torre de Cabdella › Pallars Jussà | 13 |
| Forêt de Tremp (8) | Tremp › Pallars Jussà | 13 |
| Forêt de Estaràs | Estaràs › Segarra | 13 |
| Forêt de la Pobla de Segur | la Pobla de Segur › Pallars Jussà | 13 |
| Forêt de la Guingueta d'Àneu | la Guingueta d'Àneu › Pallars Sobirà | 13 |
| Forêt de Vinaixa (4) | Vinaixa › Garrigues | 13 |
| Forêt de la Baronia de Rialb (11) | la Baronia de Rialb › Noguera | 13 |
| Forêt de Talarn | Talarn › Pallars Jussà | 13 |
| Forêt de Vall de Cardós (6) | Vall de Cardós › Pallars Sobirà | 13 |
| Forêt de Montoliu de Segarra (2) | Montoliu de Segarra › Segarra | 13 |
| Forêt de la Baronia de Rialb (13) | la Baronia de Rialb › Noguera | 13 |
| Forêt de Camarasa (2) | Camarasa › Noguera | 13 |
| Forêt de Lladurs (17) | Lladurs › Solsonès | 13 |
| Forêt de Alins (6) | Alins › Pallars Sobirà | 13 |
| Forêt de l'Espluga Calba | l'Espluga Calba › Garrigues | 13 |
| Forêt de Estamariu | Estamariu › Alt Urgell | 13 |
| Forêt de Soriguera (12) | Soriguera › Pallars Sobirà | 13 |
| Forêt de Vilanova de Meià (8) | Vilanova de Meià › Noguera | 13 |
| Forêt de Lladurs (27) | Lladurs › Solsonès | 13 |
| Forêt de Juncosa (15) | Juncosa › Garrigues | 13 |
| Forêt de Camarasa (3) | Camarasa › Noguera | 13 |
| Forêt de Naut Aran (2) | Naut Aran › Val d'Aran | 13 |
| Forêt de Ribera d'Ondara (3) | Ribera d'Ondara › Segarra | 13 |
| Forêt de Estaràs (2) | Estaràs › Segarra | 13 |
| Forêt de la Vall de Boí (4) | la Vall de Boí › Alta Ribagorça | 13 |
| Forêt de Juncosa (18) | Juncosa › Garrigues | 13 |
| Forêt de Tremp (39) | Tremp › Pallars Jussà | 13 |
| Forêt de Tremp (42) | Tremp › Pallars Jussà | 13 |
| Forêt de Conca de Dalt (14) | Conca de Dalt › Pallars Jussà | 13 |
| Forêt de Torrefeta i Florejacs (2) | Torrefeta i Florejacs › Segarra | 13 |
| Forêt de Torà (3) | Torà › Solsonès | 13 |
| Bois de Ciutadilla (3) | Ciutadilla › Urgell | 13 |
| Forêt de Bellver de Cerdanya (5) | Bellver de Cerdanya › Cerdanya (Lérida) | 13 |
| Forêt de Isona i Conca Dellà (22) | Isona i Conca Dellà › Pallars Jussà | 13 |
| Forêt de Aitona (8) | Aitona › Segrià | 13 |
| Forêt de Tremp (70) | Tremp › Pallars Jussà | 13 |
| Forêt de Vall de Cardós (21) | Vall de Cardós › Pallars Sobirà | 13 |
| Forêt de Navès (27) | Navès › Solsonès | 13 |
| Forêt de Peramola (9) | Peramola › Alt Urgell | 13 |
| Forêt de Alt Àneu (34) | Alt Àneu › Pallars Sobirà | 13 |
| Forêt de Vielha e Mijaran (39) | Vielha e Mijaran › Val d'Aran | 13 |
| Forêt de Os de Balaguer (27) | Os de Balaguer › Noguera | 13 |
| Forêt de Àger (24) | Àger › Noguera | 13 |
| Forêt de Pinell de Solsonès (38) | Pinell de Solsonès › Solsonès | 13 |
| Forêt de la Vansa i Fórnols (22) | la Vansa i Fórnols › Alt Urgell | 13 |
| Forêt de Navès (109) | Navès › Solsonès | 13 |
| Forêt de Alins (26) | Alins › Pallars Sobirà | 13 |
| Forêt de Navès (124) | Navès › Solsonès | 13 |
| Forêt de les Valls de Valira (29) | les Valls de Valira › Alt Urgell | 13 |
| Forêt de Alt Àneu (56) | Alt Àneu › Pallars Sobirà | 13 |
| Forêt de Gósol (25) | Gósol › Berguedà (Lérida) | 13 |
| Forêt de Pinós (109) | Pinós › Solsonès | 13 |
| Forêt de Bellver de Cerdanya (44) | Bellver de Cerdanya › Cerdanya (Lérida) | 13 |
| Forêt de Guixers (75) | Guixers › Solsonès | 13 |
| Forêt de Guixers (98) | Guixers › Solsonès | 13 |
| Forêt de la Coma i la Pedra (157) | la Coma i la Pedra › Solsonès | 13 |
| Forêt de Guixers (130) | Guixers › Solsonès | 13 |
| Forêt de Odèn (82) | Odèn › Solsonès | 13 |
| Forêt de Odèn (106) | Odèn › Solsonès | 13 |
| Forêt de Alt Àneu (86) | Alt Àneu › Pallars Sobirà | 13 |
| Forêt de Alt Àneu (95) | Alt Àneu › Pallars Sobirà | 13 |
| Forêt de Alt Àneu (114) | Alt Àneu › Pallars Sobirà | 13 |
| Forêt de Alt Àneu (122) | Alt Àneu › Pallars Sobirà | 13 |
| Forêt de la Guingueta d'Àneu (81) | la Guingueta d'Àneu › Pallars Sobirà | 13 |
| Forêt de Vilaller (54) | Vilaller › Alta Ribagorça | 13 |
| Forêt de el Pont de Bar (4) | el Pont de Bar › Alt Urgell | 13 |
| Forêt de Navès (175) | Navès › Solsonès | 13 |
| Forêt de Sant Esteve de la Sarga (20) | Sant Esteve de la Sarga › Pallars Jussà | 13 |
| Forêt de Baix Pallars (50) | Baix Pallars › Pallars Sobirà | 13 |
| Forêt de Castell de Mur (22) | Castell de Mur › Pallars Jussà | 13 |
| Forêt de Sant Esteve de la Sarga (68) | Sant Esteve de la Sarga › Pallars Jussà | 13 |
| Forêt de Sant Esteve de la Sarga (72) | Sant Esteve de la Sarga › Pallars Jussà | 13 |
| Forêt de Àger (137) | Àger › Noguera | 13 |
| Forêt de la Pobla de Segur (15) | la Pobla de Segur › Pallars Jussà | 13 |
| Forêt de el Pont de Suert (70) | el Pont de Suert › Alta Ribagorça | 13 |
| Forêt de Llobera (504) | Llobera › Solsonès | 13 |
| Forêt de Arsèguel (7) | Arsèguel › Alt Urgell | 13 |
| Forêt de Arsèguel (10) | Arsèguel › Alt Urgell | 13 |
| Forêt de Cava (26) | Cava › Alt Urgell | 13 |
| Forêt de Cava (29) | Cava › Alt Urgell | 13 |
| Forêt de Lles de Cerdanya (33) | Lles de Cerdanya › Cerdanya (Lérida) | 13 |
| Forêt de Conca de Dalt (46) | Conca de Dalt › Pallars Jussà | 13 |
| Forêt de Alàs i Cerc (39) | Alàs i Cerc › Alt Urgell | 13 |
| Forêt de Soriguera (55) | Soriguera › Pallars Sobirà | 13 |
| Forêt de Tarrés (4) | Tarrés › Garrigues | 12 |
| Forêt de Torà (2) | Torà › Solsonès | 12 |
| Forêt de Àger (2) | Àger › Noguera | 12 |
| Forêt de la Baronia de Rialb (10) | la Baronia de Rialb › Noguera | 12 |
| Forêt de Conca de Dalt (5) | Conca de Dalt › Pallars Jussà | 12 |
| Forêt de Vilanova de l'Aguda (2) | Vilanova de l'Aguda › Noguera | 12 |
| Forêt de Llardecans (2) | Llardecans › Segrià | 12 |
| Forêt de els Torms | els Torms › Garrigues | 12 |
| Forêt de Vilaller (5) | Vilaller › Alta Ribagorça | 12 |
| Forêt de Ribera d'Ondara (2) | Ribera d'Ondara › Segarra | 12 |
| Forêt de Sarroca de Bellera (3) | Sarroca de Bellera › Pallars Jussà | 12 |
| Forêt de Llardecans (3) | Llardecans › Segrià | 12 |
| Forêt de Castelló de Farfanya | Castelló de Farfanya › Noguera | 12 |
| Forêt de l'Albagés (3) | l'Albagés › Garrigues | 12 |
| Bois de Maldà (3) | Maldà › Urgell | 12 |
| Forêt de la Vall de Boí (9) | la Vall de Boí › Alta Ribagorça | 12 |
| Forêt de Sarroca de Bellera (19) | Sarroca de Bellera › Pallars Jussà | 12 |
| Forêt de Alins (14) | Alins › Pallars Sobirà | 12 |
| Bois de Llimiana | Llimiana › Pallars Jussà | 12 |
| Bois de Prullans (2) | Prullans › Cerdanya (Lérida) | 12 |
| Bois de Conca de Dalt | Conca de Dalt › Pallars Jussà | 12 |
| Forêt de Odèn (26) | Odèn › Solsonès | 12 |
| Forêt de Sarroca de Bellera (20) | Sarroca de Bellera › Pallars Jussà | 12 |
| Forêt de Bellver de Cerdanya (16) | Bellver de Cerdanya › Cerdanya (Lérida) | 12 |
| Forêt de Navès (43) | Navès › Solsonès | 12 |
| Forêt de Àger (27) | Àger › Noguera | 12 |
| Forêt de Lles de Cerdanya (23) | Lles de Cerdanya › Cerdanya (Lérida) | 12 |
| Forêt de Riner (141) | Riner › Solsonès | 12 |
| Forêt de la Coma i la Pedra (104) | la Coma i la Pedra › Solsonès | 12 |
| Forêt de Camarasa (32) | Camarasa › Noguera | 12 |
| Forêt de Navès (119) | Navès › Solsonès | 12 |
| Forêt de Odèn (54) | Odèn › Solsonès | 12 |
| Forêt de Pinós (113) | Pinós › Solsonès | 12 |
| Forêt de Pinós (124) | Pinós › Solsonès | 12 |
| Forêt de Bellver de Cerdanya (40) | Bellver de Cerdanya › Cerdanya (Lérida) | 12 |
| Forêt de Gósol (41) | Gósol › Berguedà (Lérida) | 12 |
| Forêt de Gósol (44) | Gósol › Berguedà (Lérida) | 12 |
| Forêt de Guixers (114) | la Coma i la Pedra › Solsonès | 12 |
| Forêt de Gósol (86) | Gósol › Berguedà (Lérida) | 12 |
| Forêt de Odèn (69) | Odèn › Solsonès | 12 |
| Forêt de Odèn (70) | Odèn › Solsonès | 12 |
| Forêt de Lladurs (197) | Lladurs › Solsonès | 12 |
| Forêt de Alt Àneu (98) | Alt Àneu › Pallars Sobirà | 12 |
| Forêt de Alt Àneu (119) | Alt Àneu › Pallars Sobirà | 12 |
| Forêt de Canejan (14) | Canejan › Val d'Aran | 12 |
| Forêt de Alins (53) | Alins › Pallars Sobirà | 12 |
| Forêt de Ribera d'Urgellet (51) | Ribera d'Urgellet › Alt Urgell | 12 |
| Forêt de Navès (218) | Navès › Solsonès | 12 |
| Forêt de Clariana de Cardener (186) | Clariana de Cardener › Solsonès | 12 |
| Forêt de Sant Esteve de la Sarga (52) | Sant Esteve de la Sarga › Pallars Jussà | 12 |
| Forêt de Àger (127) | Àger › Noguera | 12 |
| Forêt de Àger (162) | Àger › Noguera | 12 |
| Forêt de Os de Balaguer (49) | Os de Balaguer › Noguera | 12 |
| Forêt de Baix Pallars (73) | Baix Pallars › Pallars Sobirà | 12 |
| Forêt de Baix Pallars (76) | Baix Pallars › Pallars Sobirà | 12 |
| Forêt de Àger (176) | Àger › Noguera | 12 |
| Forêt de Tírvia (7) | Tírvia › Pallars Sobirà | 12 |
| Forêt de Alins (92) | Alins › Pallars Sobirà | 12 |
| Forêt de Llobera (507) | Llobera › Solsonès | 12 |
| Forêt de Clariana de Cardener (233) | Clariana de Cardener › Solsonès | 12 |
| Forêt de Arsèguel (9) | Arsèguel › Alt Urgell | 12 |
| Forêt de la Vansa i Fórnols (34) | la Vansa i Fórnols › Alt Urgell | 12 |
| Forêt de Lladurs (279) | Lladurs › Solsonès | 12 |
| Forêt de Riner (161) | Riner › Solsonès | 12 |
| Forêt de Maials (4) | Maials › Segrià | 11 |
| Forêt de Prullans | Prullans › Cerdanya (Lérida) | 11 |
| Forêt de Farrera | Farrera › Pallars Sobirà | 11 |
| Forêt de Lladurs (10) | Lladurs › Solsonès | 11 |
| Forêt de les Valls d'Aguilar (9) | les Valls d'Aguilar › Alt Urgell | 11 |
| Forêt de Sort | Sort › Pallars Sobirà | 11 |
| Forêt de Tremp (26) | Tremp › Pallars Jussà | 11 |
| Forêt de la Vansa i Fórnols (9) | la Vansa i Fórnols › Alt Urgell | 11 |
| Forêt de la Molsosa (4) | la Molsosa › Solsonès | 11 |
| Forêt de Ponts (2) | Ponts › Noguera | 11 |
| Forêt de Baix Pallars (22) | Baix Pallars › Pallars Sobirà | 11 |
| Forêt de Pinós (13) | Pinós › Solsonès | 11 |
| Forêt de Sarroca de Bellera (8) | Sarroca de Bellera › Pallars Jussà | 11 |
| Forêt de Bellver de Cerdanya (7) | Bellver de Cerdanya › Cerdanya (Lérida) | 11 |
| Forêt de Tremp (52) | Tremp › Pallars Jussà | 11 |
| Forêt de Olius (242) | Olius › Solsonès | 11 |
| Forêt de Guixers (25) | Guixers › Solsonès | 11 |
| Forêt de la Vall de Boí (254) | la Vall de Boí › Alta Ribagorça | 11 |
| Forêt de Vielha e Mijaran (34) | Vielha e Mijaran › Val d'Aran | 11 |
| Forêt de Vilaller (33) | Vilaller › Alta Ribagorça | 11 |
| Forêt de Alt Àneu (48) | Alt Àneu › Pallars Sobirà | 11 |
| Forêt de Vilanova de la Barca (12) | Vilanova de la Barca › Segrià | 11 |
| Forêt de Vallfogona de Balaguer (3) | Vallfogona de Balaguer › Noguera | 11 |
| Forêt de Montellà i Martinet (8) | Montellà i Martinet › Cerdanya (Lérida) | 11 |
| Forêt de Naut Aran (67) | Naut Aran › Val d'Aran | 11 |
| Forêt de Vilamòs (4) | Vilamòs › Val d'Aran | 11 |
| Forêt de la Coma i la Pedra (103) | la Coma i la Pedra › Solsonès | 11 |
| Forêt de la Coma i la Pedra (105) | la Coma i la Pedra › Solsonès | 11 |
| Forêt de les Avellanes i Santa Linya (20) | les Avellanes i Santa Linya › Noguera | 11 |
| Forêt de Navès (68) | Navès › Solsonès | 11 |
| Forêt de Coll de Nargó (46) | Coll de Nargó › Alt Urgell | 11 |
| Bois de Bellver de Cerdanya (5) | Bellver de Cerdanya › Cerdanya (Lérida) | 11 |
| Bois de Vilaller | Vilaller › Alta Ribagorça | 11 |
| Forêt de Lladurs (183) | Lladurs › Solsonès | 11 |
| Forêt de Navès (130) | Navès › Solsonès | 11 |
| Forêt de Pinós (61) | Pinós › Solsonès | 11 |
| Forêt de Pinós (90) | Pinós › Solsonès | 11 |
| Forêt de la Guingueta d'Àneu (77) | la Guingueta d'Àneu › Pallars Sobirà | 11 |
| Forêt de Esterri de Cardós (10) | Esterri de Cardós › Pallars Sobirà | 11 |
| Forêt de Pinós (138) | Pinós › Solsonès | 11 |
| Forêt de Riu de Cerdanya (12) | Riu de Cerdanya › Cerdanya (Lérida) | 11 |
| Forêt de Bellver de Cerdanya (37) | Bellver de Cerdanya › Cerdanya (Lérida) | 11 |
| Forêt de Cava (8) | Cava › Alt Urgell | 11 |
| Forêt de Guixers (87) | Guixers › Solsonès | 11 |
| Forêt de Gósol (38) | Gósol › Berguedà (Lérida) | 11 |
| Forêt de la Coma i la Pedra (164) | la Coma i la Pedra › Solsonès | 11 |
| Forêt de Gósol (94) | Gósol › Berguedà (Lérida) | 11 |
| Forêt de Naut Aran (103) | Naut Aran › Val d'Aran | 11 |
| Forêt de Naut Aran (104) | Naut Aran › Val d'Aran | 11 |
| Forêt de Vielha e Mijaran (72) | Vielha e Mijaran › Val d'Aran | 11 |
| Forêt de Alins (50) | Alins › Pallars Sobirà | 11 |
| Forêt de Vilaller (52) | Vilaller › Alta Ribagorça | 11 |
| Forêt de les Valls de Valira (74) | les Valls de Valira › Alt Urgell | 11 |
| Forêt de Ribera d'Urgellet (52) | Ribera d'Urgellet › Alt Urgell | 11 |
| Forêt de Montferrer i Castellbò (62) | Montferrer i Castellbò › Alt Urgell | 11 |
| Forêt de Peramola (21) | Peramola › Alt Urgell | 11 |
| Forêt de Cabó (39) | Cabó › Alt Urgell | 11 |
| Forêt de Navès (204) | Navès › Solsonès | 11 |
| Forêt de Lladurs (265) | Lladurs › Solsonès | 11 |
| Forêt de Clariana de Cardener (174) | Clariana de Cardener › Solsonès | 11 |
| Forêt de Àger (125) | Àger › Noguera | 11 |
| Forêt de Àger (170) | Àger › Noguera | 11 |
| Forêt de Os de Balaguer (60) | Os de Balaguer › Noguera | 11 |
| Forêt de Os de Balaguer (74) | Os de Balaguer › Noguera | 11 |
| Forêt de Os de Balaguer (86) | Os de Balaguer › Noguera | 11 |
| Forêt de Abella de la Conca (33) | Abella de la Conca › Pallars Jussà | 11 |
| Forêt de Coll de Nargó (117) | Coll de Nargó › Alt Urgell | 11 |
| Forêt de Coll de Nargó (119) | Coll de Nargó › Alt Urgell | 11 |
| Forêt de Coll de Nargó (127) | Coll de Nargó › Alt Urgell | 11 |
| Forêt de Conca de Dalt (36) | Conca de Dalt › Pallars Jussà | 11 |
| Forêt de Conca de Dalt (38) | Conca de Dalt › Pallars Jussà | 11 |
| Forêt de Tremp (99) | Tremp › Pallars Jussà | 11 |
| Forêt de Alins (77) | Alins › Pallars Sobirà | 11 |
| Forêt de Alins (80) | Alins › Pallars Sobirà | 11 |
| Forêt de Alins (94) | Alins › Pallars Sobirà | 11 |
| Forêt de Bellver de Cerdanya (86) | Bellver de Cerdanya › Cerdanya (Lérida) | 11 |
| Forêt de Clariana de Cardener (232) | Clariana de Cardener › Solsonès | 11 |
| Forêt de Espot (46) | Espot › Pallars Sobirà | 11 |
| Forêt de el Pont de Bar (52) | el Pont de Bar › Alt Urgell | 11 |
| Forêt de Farrera (28) | Farrera › Pallars Sobirà | 11 |
| Forêt de Sarroca de Bellera (25) | Sarroca de Bellera › Pallars Jussà | 11 |
| Forêt de Estamariu (22) | Estamariu › Alt Urgell | 11 |
| Forêt de la Seu d'Urgell (21) | la Seu d'Urgell › Alt Urgell | 11 |
| Forêt de Gimenells i el Pla de la Font | Gimenells i el Pla de la Font › Segrià | 10 |
| Forêt de Bassella (2) | Pinell de Solsonès › Solsonès | 10 |
| Forêt de Lles de Cerdanya (4) | Lles de Cerdanya › Cerdanya (Lérida) | 10 |
| Forêt de la Coma i la Pedra (56) | la Coma i la Pedra › Solsonès | 10 |
| Forêt de Pinós (11) | Pinós › Solsonès | 10 |
| Forêt de Pinós (12) | Pinós › Solsonès | 10 |
| Parc de les Basses d'Alpicat | Lleida › Segrià | 10 |
| Forêt de Gósol (2) | Gósol › Berguedà (Lérida) | 10 |
| Forêt de Sarroca de Bellera (9) | Sarroca de Bellera › Pallars Jussà | 10 |
| Bois de les Oluges (2) | les Oluges › Segarra | 10 |
| Forêt de Isona i Conca Dellà (19) | Isona i Conca Dellà › Pallars Jussà | 10 |
| Forêt de Prats i Sansor | Prats i Sansor › Cerdanya (Lérida) | 10 |
| Forêt de el Pont de Suert (24) | el Pont de Suert › Alta Ribagorça | 10 |
| Forêt de el Pont de Suert (25) | el Pont de Suert › Alta Ribagorça | 10 |
| Forêt de Lles de Cerdanya (11) | Lles de Cerdanya › Cerdanya (Lérida) | 10 |
| Forêt de Alins (10) | Alins › Pallars Sobirà | 10 |
| Bois de Bellver de Cerdanya (2) | Bellver de Cerdanya › Cerdanya (Lérida) | 10 |
| Forêt de Lladurs (50) | Lladurs › Solsonès | 10 |
| Forêt de Lladurs (53) | Lladurs › Solsonès | 10 |
| Forêt de Olius (170) | Olius › Solsonès | 10 |
| Forêt de Vilaller (28) | Vilaller › Alta Ribagorça | 10 |
| Forêt de la Guingueta d'Àneu (18) | la Guingueta d'Àneu › Pallars Sobirà | 10 |
| Forêt de Alt Àneu (50) | Alt Àneu › Pallars Sobirà | 10 |
| Forêt de Alòs de Balaguer (6) | Alòs de Balaguer › Noguera | 10 |
| Forêt de Alfarràs (5) | Alfarràs › Segrià | 10 |
| Forêt de Os de Balaguer (24) | Os de Balaguer › Noguera | 10 |
| Forêt de Tremp (80) | Tremp › Pallars Jussà | 10 |
| Forêt de Torà (17) | Torà › Solsonès | 10 |
| Forêt de Montellà i Martinet (6) | Montellà i Martinet › Cerdanya (Lérida) | 10 |
| Forêt de Olius (314) | Olius › Solsonès | 10 |
| Forêt de Bassella (10) | Bassella › Alt Urgell | 10 |
| Forêt de Vilamòs (7) | Vilamòs › Val d'Aran | 10 |
| Forêt de Fígols i Alinyà (10) | Fígols i Alinyà › Alt Urgell | 10 |
| Forêt de les Avellanes i Santa Linya (19) | les Avellanes i Santa Linya › Noguera | 10 |
| Forêt de Navès (72) | Navès › Solsonès | 10 |
| Forêt de Coll de Nargó (83) | Coll de Nargó › Alt Urgell | 10 |
| Forêt de Odèn (40) | Odèn › Solsonès | 10 |
| Forêt de Lladurs (174) | Lladurs › Solsonès | 10 |
| Forêt de Odèn (46) | Odèn › Solsonès | 10 |
| Forêt de Odèn (48) | Odèn › Solsonès | 10 |
| Forêt de la Guingueta d'Àneu (76) | la Guingueta d'Àneu › Pallars Sobirà | 10 |
| Forêt de la Vall de Boí (261) | la Vall de Boí › Alta Ribagorça | 10 |
| Forêt de Pinós (101) | Pinós › Solsonès | 10 |
| Forêt de Pinós (104) | Pinós › Solsonès | 10 |
| Forêt de Pinós (125) | Pinós › Solsonès | 10 |
| Forêt de Riner (149) | Riner › Solsonès | 10 |
| Forêt de Montellà i Martinet (16) | Montellà i Martinet › Cerdanya (Lérida) | 10 |
| Forêt de Guixers (79) | Guixers › Solsonès | 10 |
| Forêt de Gósol (72) | Gósol › Berguedà (Lérida) | 10 |
| Forêt de Odèn (132) | Odèn › Solsonès | 10 |
| Forêt de Naut Aran (93) | Naut Aran › Val d'Aran | 10 |
| Forêt de Naut Aran (108) | Naut Aran › Val d'Aran | 10 |
| Forêt de Naut Aran (122) | Naut Aran › Val d'Aran | 10 |
| Forêt de Naut Aran (134) | Naut Aran › Val d'Aran | 10 |
| Forêt de Vielha e Mijaran (68) | Vielha e Mijaran › Val d'Aran | 10 |
| Forêt de les Valls de Valira (58) | les Valls de Valira › Alt Urgell | 10 |
| Forêt de Alins (57) | Alins › Pallars Sobirà | 10 |
| Forêt de Alins (64) | Alins › Pallars Sobirà | 10 |
| Forêt de les Valls de Valira (122) | les Valls de Valira › Alt Urgell | 10 |
| Forêt de Cabó (32) | Cabó › Alt Urgell | 10 |
| Forêt de Montellà i Martinet (46) | Montellà i Martinet › Cerdanya (Lérida) | 10 |
| Forêt de Cava (16) | Cava › Alt Urgell | 10 |
| Forêt de Olius (340) | Olius › Solsonès | 10 |
| Forêt de Lladurs (269) | Lladurs › Solsonès | 10 |
| Forêt de Llimiana (10) | Llimiana › Pallars Jussà | 10 |
| Forêt de Àger (51) | Àger › Noguera | 10 |
| Forêt de Sant Esteve de la Sarga (25) | Sant Esteve de la Sarga › Pallars Jussà | 10 |
| Forêt de Clariana de Cardener (195) | Clariana de Cardener › Solsonès | 10 |
| Forêt de Àger (72) | Àger › Noguera | 10 |
| Forêt de Camarasa (51) | Camarasa › Noguera | 10 |
| Forêt de Àger (135) | Àger › Noguera | 10 |
| Forêt de Os de Balaguer (64) | Os de Balaguer › Noguera | 10 |
| Forêt de Abella de la Conca (69) | Abella de la Conca › Pallars Jussà | 10 |
| Forêt de Abella de la Conca (75) | Abella de la Conca › Pallars Jussà | 10 |
| Forêt de la Pobla de Segur (23) | la Pobla de Segur › Pallars Jussà | 10 |
| Forêt de la Pobla de Segur (25) | la Pobla de Segur › Pallars Jussà | 10 |
| Forêt de Baix Pallars (81) | Baix Pallars › Pallars Sobirà | 10 |
| Forêt de Tremp (111) | Tremp › Pallars Jussà | 10 |
| Forêt de Tremp (119) | Tremp › Pallars Jussà | 10 |
| Forêt de Llobera (524) | Llobera › Solsonès | 10 |
| Forêt de Bellver de Cerdanya (88) | Bellver de Cerdanya › Cerdanya (Lérida) | 10 |
| Forêt de Alins (102) | Alins › Pallars Sobirà | 10 |
| Forêt de Alins (114) | Alins › Pallars Sobirà | 10 |
| Forêt de les Valls de Valira (137) | les Valls de Valira › Alt Urgell | 10 |
| Forêt de Arsèguel (18) | Arsèguel › Alt Urgell | 10 |
| Forêt de la Seu d'Urgell (22) | la Seu d'Urgell › Alt Urgell | 10 |
| Forêt de Lladurs (280) | Lladurs › Solsonès | 10 |
| Forêt de Lladorre (49) | Lladorre › Pallars Sobirà | 10 |
| Forêt de Lladorre (50) | Lladorre › Pallars Sobirà | 10 |
| Forêt de Lladorre (53) | Lladorre › Pallars Sobirà | 10 |
| Forêt de Soriguera (52) | Soriguera › Pallars Sobirà | 10 |
| Forêt de Tarrés (5) ⚠️ | Tarrés › Garrigues | 9 |
| Bois de Talavera ⚠️ | Talavera › Segarra | 9 |
| Forêt de Talavera (3) ⚠️ | Talavera › Segarra | 9 |
| Forêt de Montferrer i Castellbò (19) ⚠️ | Montferrer i Castellbò › Alt Urgell | 9 |
| Forêt de Montferrer i Castellbò (20) ⚠️ | Montferrer i Castellbò › Alt Urgell | 9 |
| Forêt de la Coma i la Pedra (53) ⚠️ | la Coma i la Pedra › Solsonès | 9 |
| Forêt de Espot (23) ⚠️ | Espot › Pallars Sobirà | 9 |
| Forêt de Isona i Conca Dellà (17) ⚠️ | Isona i Conca Dellà › Pallars Jussà | 9 |
| Forêt de Isona i Conca Dellà (21) ⚠️ | Isona i Conca Dellà › Pallars Jussà | 9 |
| Forêt de Coll de Nargó (24) ⚠️ | Coll de Nargó › Alt Urgell | 9 |
| Forêt de Olius (40) ⚠️ | Olius › Solsonès | 9 |
| Forêt de Tremp (63) ⚠️ | Tremp › Pallars Jussà | 9 |
| Forêt de Clariana de Cardener (93) ⚠️ | Clariana de Cardener › Solsonès | 9 |
| Forêt de Clariana de Cardener (147) ⚠️ | Clariana de Cardener › Solsonès | 9 |
| Forêt de Riner (129) ⚠️ | Riner › Solsonès | 9 |
| Bois de Vallbona de les Monges (10) ⚠️ | Vallbona de les Monges › Urgell | 9 |
| Forêt de Solsona (132) ⚠️ | Solsona › Solsonès | 9 |
| Forêt de la Vall de Boí (253) ⚠️ | la Vall de Boí › Alta Ribagorça | 9 |
| Forêt de Vielha e Mijaran (27) ⚠️ | Vielha e Mijaran › Val d'Aran | 9 |
| Forêt de Esterri d'Àneu (4) ⚠️ | Esterri d'Àneu › Pallars Sobirà | 9 |
| Forêt de Riner (130) ⚠️ | Riner › Solsonès | 9 |
| Forêt de Navès (51) ⚠️ | Navès › Solsonès | 9 |
| Forêt de Àger (25) ⚠️ | Àger › Noguera | 9 |
| Forêt de Bassella (17) ⚠️ | Bassella › Alt Urgell | 9 |
| Forêt de Riner (142) ⚠️ | Riner › Solsonès | 9 |
| Forêt de Montellà i Martinet (13) ⚠️ | Montellà i Martinet › Cerdanya (Lérida) | 9 |
| Forêt de Navès (70) ⚠️ | Navès › Solsonès | 9 |
| Forêt de Navès (97) ⚠️ | Navès › Solsonès | 9 |
| Forêt de Navès (112) ⚠️ | Navès › Solsonès | 9 |
| Forêt de Navès (114) ⚠️ | Navès › Solsonès | 9 |
| Forêt de Coll de Nargó (47) ⚠️ | Coll de Nargó › Alt Urgell | 9 |
| Forêt de Navès (143) ⚠️ | Navès › Solsonès | 9 |
| Forêt de la Molsosa (58) ⚠️ | la Molsosa › Solsonès | 9 |
| Forêt de Pinós (70) ⚠️ | Pinós › Solsonès | 9 |
| Forêt de la Guingueta d'Àneu (56) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 9 |
| Forêt de la Guingueta d'Àneu (59) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 9 |
| Forêt de Soriguera (38) ⚠️ | Soriguera › Pallars Sobirà | 9 |
| Forêt de Pinós (110) ⚠️ | Pinós › Solsonès | 9 |
| Forêt de Pinós (129) ⚠️ | Pinós › Solsonès | 9 |
| Forêt de Torà (30) ⚠️ | Torà › Solsonès | 9 |
| Forêt de Pinós (153) ⚠️ | Pinós › Solsonès | 9 |
| Forêt de Guixers (63) ⚠️ | Guixers › Solsonès | 9 |
| Forêt de Guixers (64) ⚠️ | Guixers › Solsonès | 9 |
| Forêt de Josa i Tuixén (19) ⚠️ | Josa i Tuixén › Alt Urgell | 9 |
| Forêt de la Coma i la Pedra (162) ⚠️ | la Coma i la Pedra › Solsonès | 9 |
| Forêt de Guixers (115) ⚠️ | Guixers › Solsonès | 9 |
| Forêt de la Coma i la Pedra (167) ⚠️ | la Coma i la Pedra › Solsonès | 9 |
| Forêt de Gósol (69) ⚠️ | Gósol › Berguedà (Lérida) | 9 |
| Forêt de Guixers (119) ⚠️ | Guixers › Solsonès | 9 |
| Forêt de Gósol (95) ⚠️ | Gósol › Berguedà (Lérida) | 9 |
| Forêt de Gósol (101) ⚠️ | Gósol › Berguedà (Lérida) | 9 |
| Forêt de Navès (156) ⚠️ | Navès › Solsonès | 9 |
| Forêt de Odèn (100) ⚠️ | Odèn › Solsonès | 9 |
| Forêt de Odèn (115) ⚠️ | Odèn › Solsonès | 9 |
| Forêt de Lladurs (210) ⚠️ | Lladurs › Solsonès | 9 |
| Forêt de Lladurs (215) ⚠️ | Lladurs › Solsonès | 9 |
| Forêt de Naut Aran (68) ⚠️ | Naut Aran › Val d'Aran | 9 |
| Forêt de Naut Aran (110) ⚠️ | Naut Aran › Val d'Aran | 9 |
| Forêt de Canejan (22) ⚠️ | Canejan › Val d'Aran | 9 |
| Forêt de Llavorsí (45) ⚠️ | Llavorsí › Pallars Sobirà | 9 |
| Forêt de Rialp (22) ⚠️ | Rialp › Pallars Sobirà | 9 |
| Forêt de Es Bòrdes (10) ⚠️ | Es Bòrdes › Val d'Aran | 9 |
| Forêt de Vielha e Mijaran (75) ⚠️ | Vielha e Mijaran › Val d'Aran | 9 |
| Forêt de Vilamòs (11) ⚠️ | Vilamòs › Val d'Aran | 9 |
| Forêt de les Valls de Valira (52) ⚠️ | les Valls de Valira › Alt Urgell | 9 |
| Forêt de Alins (67) ⚠️ | Alins › Pallars Sobirà | 9 |
| Forêt de Vilaller (69) ⚠️ | Vilaller › Alta Ribagorça | 9 |
| Forêt de Estamariu (10) ⚠️ | Estamariu › Alt Urgell | 9 |
| Forêt de Ribera d'Urgellet (39) ⚠️ | Ribera d'Urgellet › Alt Urgell | 9 |
| Forêt de les Valls de Valira (121) ⚠️ | les Valls de Valira › Alt Urgell | 9 |
| Forêt de Oliana (12) ⚠️ | Oliana › Alt Urgell | 9 |
| Forêt de Josa i Tuixén (38) ⚠️ | Josa i Tuixén › Alt Urgell | 9 |
| Forêt de Josa i Tuixén (44) ⚠️ | Josa i Tuixén › Alt Urgell | 9 |
| Forêt de Camarasa (39) ⚠️ | Camarasa › Noguera | 9 |
| Forêt de Olius (334) ⚠️ | Olius › Solsonès | 9 |
| Forêt de Navès (196) ⚠️ | Navès › Solsonès | 9 |
| Forêt de Clariana de Cardener (170) ⚠️ | Clariana de Cardener › Solsonès | 9 |
| Forêt de Lladurs (256) ⚠️ | Lladurs › Solsonès | 9 |
| Forêt de Bellver de Cerdanya (75) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 9 |
| Forêt de Àger (47) ⚠️ | Àger › Noguera | 9 |
| Forêt de Sant Esteve de la Sarga (22) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 9 |
| Forêt de Castell de Mur (19) ⚠️ | Castell de Mur › Pallars Jussà | 9 |
| Forêt de Àger (118) ⚠️ | Àger › Noguera | 9 |
| Forêt de Os de Balaguer (68) ⚠️ | Os de Balaguer › Noguera | 9 |
| Forêt de Abella de la Conca (61) ⚠️ | Abella de la Conca › Pallars Jussà | 9 |
| Forêt de Coll de Nargó (132) ⚠️ | Coll de Nargó › Alt Urgell | 9 |
| Forêt de Àger (186) ⚠️ | Àger › Noguera | 9 |
| Forêt de Navès (226) ⚠️ | Navès › Solsonès | 9 |
| Forêt de Alins (96) ⚠️ | Alins › Pallars Sobirà | 9 |
| Forêt de Farrera (16) ⚠️ | Farrera › Pallars Sobirà | 9 |
| Forêt de Montoliu de Segarra (8) ⚠️ | Montoliu de Segarra › Segarra | 9 |
| Forêt de Naut Aran (150) ⚠️ | Naut Aran › Val d'Aran | 9 |
| Forêt de Clariana de Cardener (235) ⚠️ | Clariana de Cardener › Solsonès | 9 |
| Forêt de Cava (25) ⚠️ | Cava › Alt Urgell | 9 |
| Forêt de Cava (28) ⚠️ | Cava › Alt Urgell | 9 |
| Forêt de Alàs i Cerc (16) ⚠️ | Alàs i Cerc › Alt Urgell | 9 |
| Forêt de el Pont de Bar (49) ⚠️ | el Pont de Bar › Alt Urgell | 9 |
| Forêt de la Granja d'Escarp (14) ⚠️ | la Granja d'Escarp › Segrià | 9 |
| Forêt de Seròs (10) ⚠️ | Seròs › Segrià | 9 |
| Forêt de Alàs i Cerc (36) ⚠️ | Alàs i Cerc › Alt Urgell | 9 |
| Forêt de les Valls de Valira (149) ⚠️ | les Valls de Valira › Alt Urgell | 9 |
| Forêt de Montferrer i Castellbò (120) ⚠️ | Montferrer i Castellbò › Alt Urgell | 9 |
| Forêt de la Pobla de Segur (35) ⚠️ | la Pobla de Segur › Pallars Jussà | 9 |
| Forêt de Lladorre (54) ⚠️ | Lladorre › Pallars Sobirà | 9 |
| Forêt de Montferrer i Castellbò (2) ⚠️ | Montferrer i Castellbò › Alt Urgell | 8 |
| Forêt de Artesa de Segre (5) ⚠️ | Artesa de Segre › Noguera | 8 |
| Forêt de Gimenells i el Pla de la Font (3) ⚠️ | Gimenells i el Pla de la Font › Segrià | 8 |
| Forêt de Bovera (5) ⚠️ | Bovera › Garrigues | 8 |
| Forêt de Montoliu de Segarra (3) ⚠️ | Montoliu de Segarra › Segarra | 8 |
| Forêt de Almenar ⚠️ | Almenar › Segrià | 8 |
| Forêt de Olius (4) ⚠️ | Olius › Solsonès | 8 |
| Forêt de la Coma i la Pedra (52) ⚠️ | la Coma i la Pedra › Solsonès | 8 |
| Forêt de Agramunt ⚠️ | Agramunt › Urgell | 8 |
| Bois de Agramunt (2) ⚠️ | Agramunt › Urgell | 8 |
| Forêt de Gimenells i el Pla de la Font (8) ⚠️ | Gimenells i el Pla de la Font › Segrià | 8 |
| la Seu Vella ⚠️ | Lleida › Segrià | 8 |
| Forêt de Sarroca de Bellera (10) ⚠️ | Sarroca de Bellera › Pallars Jussà | 8 |
| Forêt de el Pont de Suert (26) ⚠️ | el Pont de Suert › Alta Ribagorça | 8 |
| Forêt de Olius (26) ⚠️ | Olius › Solsonès | 8 |
| Forêt de Olius (29) ⚠️ | Olius › Solsonès | 8 |
| Forêt de Alins (15) ⚠️ | Alins › Pallars Sobirà | 8 |
| Bois de Bellver de Cerdanya ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 8 |
| Bois de Alcarràs (9) ⚠️ | Alcarràs › Segrià | 8 |
| Forêt de Olius (213) ⚠️ | Olius › Solsonès | 8 |
| Forêt de Odèn (36) ⚠️ | Odèn › Solsonès | 8 |
| Forêt de Vielha e Mijaran (28) ⚠️ | Vielha e Mijaran › Val d'Aran | 8 |
| Forêt de les Valls de Valira (18) ⚠️ | les Valls de Valira › Alt Urgell | 8 |
| Forêt de la Seu d'Urgell (6) ⚠️ | la Seu d'Urgell › Alt Urgell | 8 |
| Forêt de la Molsosa (22) ⚠️ | la Molsosa › Solsonès | 8 |
| Forêt de Ivars de Noguera (5) ⚠️ | Ivars de Noguera › Noguera | 8 |
| Forêt de Baix Pallars (37) ⚠️ | Baix Pallars › Pallars Sobirà | 8 |
| Forêt de Prullans (4) ⚠️ | Prullans › Cerdanya (Lérida) | 8 |
| Forêt de Olius (315) ⚠️ | Olius › Solsonès | 8 |
| Forêt de Arres (4) ⚠️ | Vilamòs › Val d'Aran | 8 |
| Forêt de la Coma i la Pedra (106) ⚠️ | la Coma i la Pedra › Solsonès | 8 |
| Forêt de la Molsosa (23) ⚠️ | la Molsosa › Solsonès | 8 |
| Forêt de Navès (67) ⚠️ | Navès › Solsonès | 8 |
| Forêt de Navès (99) ⚠️ | Navès › Solsonès | 8 |
| Forêt de Coll de Nargó (42) ⚠️ | Coll de Nargó › Alt Urgell | 8 |
| Forêt de Coll de Nargó (45) ⚠️ | Coll de Nargó › Alt Urgell | 8 |
| Bois de Lladurs ⚠️ | Lladurs › Solsonès | 8 |
| Forêt de Lladurs (173) ⚠️ | Lladurs › Solsonès | 8 |
| Forêt de Lladurs (185) ⚠️ | Lladurs › Solsonès | 8 |
| Forêt de Navès (146) ⚠️ | Navès › Solsonès | 8 |
| Forêt de Pinós (74) ⚠️ | Pinós › Solsonès | 8 |
| Forêt de les Valls de Valira (31) ⚠️ | les Valls de Valira › Alt Urgell | 8 |
| Forêt de Llavorsí (26) ⚠️ | Llavorsí › Pallars Sobirà | 8 |
| Forêt de la Guingueta d'Àneu (36) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 8 |
| Forêt de la Guingueta d'Àneu (73) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 8 |
| Forêt de la Guingueta d'Àneu (75) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 8 |
| Forêt de Montgai ⚠️ | Montgai › Noguera | 8 |
| Forêt de la Coma i la Pedra (124) ⚠️ | la Coma i la Pedra › Solsonès | 8 |
| Forêt de Pinós (127) ⚠️ | Pinós › Solsonès | 8 |
| Forêt de Pinós (145) ⚠️ | Pinós › Solsonès | 8 |
| Forêt de Josa i Tuixén (16) ⚠️ | Josa i Tuixén › Alt Urgell | 8 |
| Forêt de Guixers (80) ⚠️ | Guixers › Solsonès | 8 |
| Forêt de la Coma i la Pedra (136) ⚠️ | la Coma i la Pedra › Solsonès | 8 |
| Forêt de Gósol (68) ⚠️ | Gósol › Berguedà (Lérida) | 8 |
| Forêt de Gósol (103) ⚠️ | Gósol › Berguedà (Lérida) | 8 |
| Forêt de Odèn (102) ⚠️ | Odèn › Solsonès | 8 |
| Forêt de Odèn (107) ⚠️ | Odèn › Solsonès | 8 |
| Forêt de Lladurs (221) ⚠️ | Lladurs › Solsonès | 8 |
| Forêt de Navès (174) ⚠️ | Navès › Solsonès | 8 |
| Forêt de Odèn (134) ⚠️ | Odèn › Solsonès | 8 |
| Forêt de Josa i Tuixén (24) ⚠️ | Josa i Tuixén › Alt Urgell | 8 |
| Forêt de Naut Aran (71) ⚠️ | Naut Aran › Val d'Aran | 8 |
| Forêt de Alt Àneu (68) ⚠️ | Alt Àneu › Pallars Sobirà | 8 |
| Forêt de Alt Àneu (76) ⚠️ | Alt Àneu › Pallars Sobirà | 8 |
| Forêt de Naut Aran (98) ⚠️ | Naut Aran › Val d'Aran | 8 |
| Forêt de Canejan (24) ⚠️ | Canejan › Val d'Aran | 8 |
| Forêt de Canejan (29) ⚠️ | Canejan › Val d'Aran | 8 |
| Forêt de la Guingueta d'Àneu (80) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 8 |
| Forêt de Es Bòrdes (13) ⚠️ | Es Bòrdes › Val d'Aran | 8 |
| Forêt de les Valls de Valira (48) ⚠️ | les Valls de Valira › Alt Urgell | 8 |
| Forêt de Alins (47) ⚠️ | Alins › Pallars Sobirà | 8 |
| Forêt de Ribera d'Urgellet (47) ⚠️ | Ribera d'Urgellet › Alt Urgell | 8 |
| Forêt de Oliana (14) ⚠️ | Oliana › Alt Urgell | 8 |
| Forêt de la Baronia de Rialb (43) ⚠️ | la Baronia de Rialb › Noguera | 8 |
| Forêt de Montellà i Martinet (39) ⚠️ | Montellà i Martinet › Cerdanya (Lérida) | 8 |
| Forêt de Cava (24) ⚠️ | Cava › Alt Urgell | 8 |
| Forêt de Navès (188) ⚠️ | Navès › Solsonès | 8 |
| Forêt de Navès (192) ⚠️ | Navès › Solsonès | 8 |
| Forêt de Olius (346) ⚠️ | Olius › Solsonès | 8 |
| Forêt de Lladurs (264) ⚠️ | Lladurs › Solsonès | 8 |
| Forêt de Navès (215) ⚠️ | Navès › Solsonès | 8 |
| Forêt de Clariana de Cardener (180) ⚠️ | Clariana de Cardener › Solsonès | 8 |
| Forêt de Clariana de Cardener (223) ⚠️ | Clariana de Cardener › Solsonès | 8 |
| Forêt de Àger (138) ⚠️ | Àger › Noguera | 8 |
| Forêt de Os de Balaguer (45) ⚠️ | Os de Balaguer › Noguera | 8 |
| Forêt de Abella de la Conca (70) ⚠️ | Abella de la Conca › Pallars Jussà | 8 |
| Forêt de Àger (177) ⚠️ | Àger › Noguera | 8 |
| Forêt de Talarn (4) ⚠️ | Talarn › Pallars Jussà | 8 |
| Forêt de Alins (91) ⚠️ | Alins › Pallars Sobirà | 8 |
| Forêt de Llobera (514) ⚠️ | Llobera › Solsonès | 8 |
| Forêt de Llobera (521) ⚠️ | Llobera › Solsonès | 8 |
| Forêt de Llobera (523) ⚠️ | Llobera › Solsonès | 8 |
| Forêt de Pinell de Solsonès (39) ⚠️ | Pinell de Solsonès › Solsonès | 8 |
| Forêt de Alins (108) ⚠️ | Alins › Pallars Sobirà | 8 |
| Forêt de Clariana de Cardener (230) ⚠️ | Clariana de Cardener › Solsonès | 8 |
| Forêt de Llavorsí (56) ⚠️ | Llavorsí › Pallars Sobirà | 8 |
| Forêt de el Pont de Bar (16) ⚠️ | el Pont de Bar › Alt Urgell | 8 |
| Forêt de el Pont de Bar (26) ⚠️ | el Pont de Bar › Alt Urgell | 8 |
| Forêt de Llavorsí (65) ⚠️ | Llavorsí › Pallars Sobirà | 8 |
| Forêt de Almatret (17) ⚠️ | Almatret › Segrià | 8 |
| Forêt de les Valls de Valira (136) ⚠️ | les Valls de Valira › Alt Urgell | 8 |
| Forêt de les Valls de Valira (138) ⚠️ | les Valls de Valira › Alt Urgell | 8 |
| Forêt de Estamariu (18) ⚠️ | Estamariu › Alt Urgell | 8 |
| Forêt de Montferrer i Castellbò (110) ⚠️ | Montferrer i Castellbò › Alt Urgell | 8 |
| Forêt de Lladurs ⚠️ | Lladurs › Solsonès | 7 |
| Forêt de Lladurs (13) ⚠️ | Lladurs › Solsonès | 7 |
| Forêt de Sant Guim de Freixenet (2) ⚠️ | Sant Guim de Freixenet › Segarra | 7 |
| Forêt de Lleida ⚠️ | Lleida › Segrià | 7 |
| Forêt de la Baronia de Rialb (24) ⚠️ | la Baronia de Rialb › Noguera | 7 |
| Bois de Maldà (4) ⚠️ | Maldà › Urgell | 7 |
| Bois de Lleida (10) ⚠️ | Lleida › Segrià | 7 |
| Forêt de Ribera d'Ondara (7) ⚠️ | Ribera d'Ondara › Segarra | 7 |
| Forêt de Guixers (2) ⚠️ | Guixers › Solsonès | 7 |
| Forêt de Guixers (3) ⚠️ | Guixers › Solsonès | 7 |
| Forêt de Guixers (4) ⚠️ | Guixers › Solsonès | 7 |
| Bois de Torrefeta i Florejacs (9) ⚠️ | Torrefeta i Florejacs › Segarra | 7 |
| Forêt de Espot (24) ⚠️ | Espot › Pallars Sobirà | 7 |
| Forêt de Fígols i Alinyà (7) ⚠️ | Fígols i Alinyà › Alt Urgell | 7 |
| Forêt de Llimiana (3) ⚠️ | Llimiana › Pallars Jussà | 7 |
| Bois de Talavera (4) ⚠️ | Talavera › Segarra | 7 |
| Forêt de Tremp (58) ⚠️ | Tremp › Pallars Jussà | 7 |
| Forêt de Tremp (67) ⚠️ | Tremp › Pallars Jussà | 7 |
| Forêt de la Vansa i Fórnols (20) ⚠️ | la Vansa i Fórnols › Alt Urgell | 7 |
| Forêt de Vall de Cardós (23) ⚠️ | Vall de Cardós › Pallars Sobirà | 7 |
| Forêt de Navès (31) ⚠️ | Navès › Solsonès | 7 |
| Forêt de Esterri d'Àneu (2) ⚠️ | Esterri d'Àneu › Pallars Sobirà | 7 |
| Forêt de la Guingueta d'Àneu (16) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 7 |
| Forêt de Alt Àneu (35) ⚠️ | Alt Àneu › Pallars Sobirà | 7 |
| Forêt de la Vall de Boí (255) ⚠️ | la Vall de Boí › Alta Ribagorça | 7 |
| Forêt de Vielha e Mijaran (14) ⚠️ | Vielha e Mijaran › Val d'Aran | 7 |
| Forêt de Tremp (79) ⚠️ | Tremp › Pallars Jussà | 7 |
| Forêt de el Pont de Suert (44) ⚠️ | el Pont de Suert › Alta Ribagorça | 7 |
| Forêt de Balaguer (4) ⚠️ | Balaguer › Noguera | 7 |
| Forêt de Guixers (35) ⚠️ | Guixers › Solsonès | 7 |
| Forêt de Bellver de Cerdanya (24) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 7 |
| Forêt de Navès (56) ⚠️ | Navès › Solsonès | 7 |
| Forêt de Prullans (7) ⚠️ | Prullans › Cerdanya (Lérida) | 7 |
| Forêt de les Valls d'Aguilar (28) ⚠️ | les Valls d'Aguilar › Alt Urgell | 7 |
| Forêt de Navès (78) ⚠️ | Navès › Solsonès | 7 |
| Forêt de Navès (85) ⚠️ | Navès › Solsonès | 7 |
| Forêt de Navès (116) ⚠️ | Navès › Solsonès | 7 |
| Forêt de Guixers (48) ⚠️ | Guixers › Solsonès | 7 |
| Forêt de Lladurs (188) ⚠️ | Lladurs › Solsonès | 7 |
| Forêt de la Coma i la Pedra (113) ⚠️ | la Coma i la Pedra › Solsonès | 7 |
| Forêt de Peramola (15) ⚠️ | Peramola › Alt Urgell | 7 |
| Forêt de Llavorsí (27) ⚠️ | Llavorsí › Pallars Sobirà | 7 |
| Forêt de Llavorsí (29) ⚠️ | Llavorsí › Pallars Sobirà | 7 |
| Forêt de la Vall de Boí (263) ⚠️ | la Vall de Boí › Alta Ribagorça | 7 |
| Forêt de Gósol (22) ⚠️ | Gósol › Berguedà (Lérida) | 7 |
| Forêt de la Coma i la Pedra (119) ⚠️ | la Coma i la Pedra › Solsonès | 7 |
| Forêt de la Coma i la Pedra (122) ⚠️ | la Coma i la Pedra › Solsonès | 7 |
| Forêt de Pinós (102) ⚠️ | Pinós › Solsonès | 7 |
| Forêt de Pinós (105) ⚠️ | Pinós › Solsonès | 7 |
| Forêt de Pinós (131) ⚠️ | Pinós › Solsonès | 7 |
| Forêt de Riu de Cerdanya (18) ⚠️ | Riu de Cerdanya › Cerdanya (Lérida) | 7 |
| Forêt de Bellver de Cerdanya (47) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 7 |
| Forêt de Guixers (62) ⚠️ | Guixers › Solsonès | 7 |
| Forêt de Guixers (76) ⚠️ | Guixers › Solsonès | 7 |
| Forêt de la Coma i la Pedra (130) ⚠️ | la Coma i la Pedra › Solsonès | 7 |
| Forêt de la Coma i la Pedra (154) ⚠️ | la Coma i la Pedra › Solsonès | 7 |
| Forêt de la Coma i la Pedra (160) ⚠️ | la Coma i la Pedra › Solsonès | 7 |
| Forêt de Guixers (109) ⚠️ | Guixers › Solsonès | 7 |
| Forêt de Guixers (110) ⚠️ | Guixers › Solsonès | 7 |
| Forêt de Gósol (65) ⚠️ | Gósol › Berguedà (Lérida) | 7 |
| Forêt de Gósol (89) ⚠️ | Gósol › Berguedà (Lérida) | 7 |
| Forêt de la Coma i la Pedra (176) ⚠️ | la Coma i la Pedra › Solsonès | 7 |
| Forêt de Gósol (105) ⚠️ | Gósol › Berguedà (Lérida) | 7 |
| Forêt de Odèn (75) ⚠️ | Odèn › Solsonès | 7 |
| Forêt de Odèn (83) ⚠️ | Odèn › Solsonès | 7 |
| Forêt de Odèn (101) ⚠️ | Odèn › Solsonès | 7 |
| Forêt de Odèn (125) ⚠️ | Odèn › Solsonès | 7 |
| Forêt de Odèn (129) ⚠️ | Odèn › Solsonès | 7 |
| Forêt de Alt Àneu (83) ⚠️ | Alt Àneu › Pallars Sobirà | 7 |
| Forêt de Alt Àneu (106) ⚠️ | Alt Àneu › Pallars Sobirà | 7 |
| Forêt de Alt Àneu (125) ⚠️ | Alt Àneu › Pallars Sobirà | 7 |
| Forêt de Canejan (28) ⚠️ | Canejan › Val d'Aran | 7 |
| Forêt de Naut Aran (146) ⚠️ | Naut Aran › Val d'Aran | 7 |
| Forêt de Vielha e Mijaran (73) ⚠️ | Vielha e Mijaran › Val d'Aran | 7 |
| Forêt de Vielha e Mijaran (74) ⚠️ | Vielha e Mijaran › Val d'Aran | 7 |
| Forêt de Vilamòs (10) ⚠️ | Vilamòs › Val d'Aran | 7 |
| Forêt de les Valls de Valira (43) ⚠️ | les Valls de Valira › Alt Urgell | 7 |
| Forêt de Estamariu (11) ⚠️ | Estamariu › Alt Urgell | 7 |
| Forêt de les Valls de Valira (97) ⚠️ | les Valls de Valira › Alt Urgell | 7 |
| Forêt de la Seu d'Urgell (12) ⚠️ | la Seu d'Urgell › Alt Urgell | 7 |
| Forêt de les Valls de Valira (111) ⚠️ | les Valls de Valira › Alt Urgell | 7 |
| Forêt de les Valls de Valira (117) ⚠️ | les Valls de Valira › Alt Urgell | 7 |
| Forêt de Ribera d'Urgellet (45) ⚠️ | Ribera d'Urgellet › Alt Urgell | 7 |
| Forêt de Peramola (20) ⚠️ | Peramola › Alt Urgell | 7 |
| Forêt de Oliana (9) ⚠️ | Oliana › Alt Urgell | 7 |
| Forêt de Bassella (33) ⚠️ | Bassella › Alt Urgell | 7 |
| Forêt de Montellà i Martinet (44) ⚠️ | Montellà i Martinet › Cerdanya (Lérida) | 7 |
| Forêt de Bellver de Cerdanya (72) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 7 |
| Forêt de Olius (335) ⚠️ | Olius › Solsonès | 7 |
| Forêt de Olius (338) ⚠️ | Olius › Solsonès | 7 |
| Forêt de Peramola (34) ⚠️ | Peramola › Alt Urgell | 7 |
| Forêt de Tremp (96) ⚠️ | Tremp › Pallars Jussà | 7 |
| Forêt de Riner (157) ⚠️ | Riner › Solsonès | 7 |
| Forêt de Àger (44) ⚠️ | Àger › Noguera | 7 |
| Forêt de Baix Pallars (59) ⚠️ | Baix Pallars › Pallars Sobirà | 7 |
| Forêt de Clariana de Cardener (215) ⚠️ | Clariana de Cardener › Solsonès | 7 |
| Forêt de Lleida (23) ⚠️ | Lleida › Segrià | 7 |
| Forêt de Llimiana (13) ⚠️ | Llimiana › Pallars Jussà | 7 |
| Forêt de Sant Esteve de la Sarga (37) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 7 |
| Forêt de Sant Esteve de la Sarga (63) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 7 |
| Forêt de Camarasa (49) ⚠️ | Àger › Noguera | 7 |
| Forêt de Àger (124) ⚠️ | Àger › Noguera | 7 |
| Forêt de Os de Balaguer (39) ⚠️ | Os de Balaguer › Noguera | 7 |
| Forêt de Os de Balaguer (41) ⚠️ | Os de Balaguer › Noguera | 7 |
| Forêt de Os de Balaguer (81) ⚠️ | Os de Balaguer › Noguera | 7 |
| Forêt de Coll de Nargó (125) ⚠️ | Coll de Nargó › Alt Urgell | 7 |
| Forêt de Abella de la Conca (67) ⚠️ | Abella de la Conca › Pallars Jussà | 7 |
| Forêt de Abella de la Conca (80) ⚠️ | Abella de la Conca › Pallars Jussà | 7 |
| Forêt de la Pobla de Segur (19) ⚠️ | la Pobla de Segur › Pallars Jussà | 7 |
| Forêt de la Pobla de Segur (24) ⚠️ | la Pobla de Segur › Pallars Jussà | 7 |
| Forêt de el Pont de Suert (62) ⚠️ | el Pont de Suert › Alta Ribagorça | 7 |
| Forêt de el Pont de Suert (68) ⚠️ | el Pont de Suert › Alta Ribagorça | 7 |
| Forêt de el Pont de Suert (100) ⚠️ | el Pont de Suert › Alta Ribagorça | 7 |
| Forêt de les Valls d'Aguilar (37) ⚠️ | les Valls d'Aguilar › Alt Urgell | 7 |
| Forêt de Bellver de Cerdanya (89) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 7 |
| Forêt de el Pont de Bar (17) ⚠️ | el Pont de Bar › Alt Urgell | 7 |
| Forêt de Lles de Cerdanya (29) ⚠️ | Lles de Cerdanya › Cerdanya (Lérida) | 7 |
| Forêt de el Pont de Bar (43) ⚠️ | el Pont de Bar › Alt Urgell | 7 |
| Forêt de Massalcoreig (10) ⚠️ | Massalcoreig › Segrià | 7 |
| Forêt de Massalcoreig (12) ⚠️ | Massalcoreig › Segrià | 7 |
| Forêt de Almatret (14) ⚠️ | Almatret › Segrià | 7 |
| Forêt de Almatret (16) ⚠️ | Almatret › Segrià | 7 |
| Forêt de la Vall de Boí (281) ⚠️ | la Vall de Boí › Alta Ribagorça | 7 |
| Bois de Alàs i Cerc (5) ⚠️ | Alàs i Cerc › Alt Urgell | 7 |
| Forêt de Alàs i Cerc (40) ⚠️ | Alàs i Cerc › Alt Urgell | 7 |
| Forêt de Montferrer i Castellbò (119) ⚠️ | Montferrer i Castellbò › Alt Urgell | 7 |
| Forêt de Soriguera (44) ⚠️ | Soriguera › Pallars Sobirà | 7 |
| Parc de Sant Eloi ⚠️ | Tàrrega › Urgell | 6 |
| Forêt de Alins (2) ⚠️ | Alins › Pallars Sobirà | 6 |
| Forêt de Coll de Nargó (4) ⚠️ | Coll de Nargó › Alt Urgell | 6 |
| Forêt de Pinell de Solsonès (10) ⚠️ | Pinell de Solsonès › Solsonès | 6 |
| Forêt de Lladurs (26) ⚠️ | Lladurs › Solsonès | 6 |
| Forêt de Gimenells i el Pla de la Font (9) ⚠️ | Gimenells i el Pla de la Font › Segrià | 6 |
| Bois de Gimenells i el Pla de la Font (25) ⚠️ | Gimenells i el Pla de la Font › Segrià | 6 |
| Forêt de Lleida (9) ⚠️ | Lleida › Segrià | 6 |
| Forêt de la Molsosa (9) ⚠️ | la Molsosa › Solsonès | 6 |
| Forêt de Bellver de Cerdanya (4) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 6 |
| Forêt de Gósol (3) ⚠️ | Gósol › Berguedà (Lérida) | 6 |
| Forêt de Montferrer i Castellbò (23) ⚠️ | Montferrer i Castellbò › Alt Urgell | 6 |
| Bois de Cervera (4) ⚠️ | Cervera › Segarra | 6 |
| Forêt de Isona i Conca Dellà (16) ⚠️ | Isona i Conca Dellà › Pallars Jussà | 6 |
| Forêt de Isona i Conca Dellà (20) ⚠️ | Isona i Conca Dellà › Pallars Jussà | 6 |
| Forêt de Vielha e Mijaran (6) ⚠️ | Vielha e Mijaran › Val d'Aran | 6 |
| Forêt de Organyà (3) ⚠️ | Organyà › Alt Urgell | 6 |
| Forêt de Coll de Nargó (20) ⚠️ | Coll de Nargó › Alt Urgell | 6 |
| Bois de Sant Martí de Riucorb (13) ⚠️ | Sant Martí de Riucorb › Urgell | 6 |
| Forêt de la Vansa i Fórnols (17) ⚠️ | la Vansa i Fórnols › Alt Urgell | 6 |
| Parc Ambiental de Serra Llarga ⚠️ | Lleida › Segrià | 6 |
| Forêt de Olius (110) ⚠️ | Olius › Solsonès | 6 |
| Forêt de la Pobla de Cérvoles (17) ⚠️ | la Pobla de Cérvoles › Garrigues | 6 |
| Forêt de Olius (240) ⚠️ | Olius › Solsonès | 6 |
| Forêt de Llobera (22) ⚠️ | Llobera › Solsonès | 6 |
| Forêt de Tremp (62) ⚠️ | Tremp › Pallars Jussà | 6 |
| Forêt de Tremp (65) ⚠️ | Tremp › Pallars Jussà | 6 |
| Forêt de Guixers (27) ⚠️ | Guixers › Solsonès | 6 |
| Forêt de la Vall de Boí (257) ⚠️ | la Vall de Boí › Alta Ribagorça | 6 |
| Forêt de Castellar de la Ribera (18) ⚠️ | Castellar de la Ribera › Solsonès | 6 |
| Forêt de Àger (23) ⚠️ | Àger › Noguera | 6 |
| Forêt de Ponts (4) ⚠️ | Ponts › Noguera | 6 |
| Forêt de Torà (14) ⚠️ | Torà › Solsonès | 6 |
| Forêt de Camarasa (29) ⚠️ | Camarasa › Noguera | 6 |
| Forêt de Bassella (19) ⚠️ | Bassella › Alt Urgell | 6 |
| Forêt de Fígols i Alinyà (9) ⚠️ | Fígols i Alinyà › Alt Urgell | 6 |
| Forêt de Fígols i Alinyà (11) ⚠️ | Fígols i Alinyà › Alt Urgell | 6 |
| Forêt de Navès (74) ⚠️ | Navès › Solsonès | 6 |
| Forêt de Navès (104) ⚠️ | Navès › Solsonès | 6 |
| Forêt de Navès (120) ⚠️ | Navès › Solsonès | 6 |
| Forêt de Coll de Nargó (77) ⚠️ | Coll de Nargó › Alt Urgell | 6 |
| Bois de Sant Guim de Freixenet (5) ⚠️ | Sant Guim de Freixenet › Segarra | 6 |
| Bois de Bellver de Cerdanya (7) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 6 |
| Forêt de Navès (128) ⚠️ | Navès › Solsonès | 6 |
| Forêt de Guixers (57) ⚠️ | Guixers › Solsonès | 6 |
| Forêt de Sant Llorenç de Morunys (23) ⚠️ | Sant Llorenç de Morunys › Solsonès | 6 |
| Forêt de Peramola (13) ⚠️ | Peramola › Alt Urgell | 6 |
| Forêt de la Molsosa (53) ⚠️ | la Molsosa › Solsonès | 6 |
| Forêt de la Molsosa (70) ⚠️ | la Molsosa › Solsonès | 6 |
| Forêt de la Molsosa (82) ⚠️ | Pinós › Solsonès | 6 |
| Forêt de Pinós (72) ⚠️ | Pinós › Solsonès | 6 |
| Forêt de Llavorsí (30) ⚠️ | Llavorsí › Pallars Sobirà | 6 |
| Forêt de la Guingueta d'Àneu (71) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 6 |
| Forêt de Gósol (29) ⚠️ | Gósol › Berguedà (Lérida) | 6 |
| Forêt de Esterri de Cardós (6) ⚠️ | Esterri de Cardós › Pallars Sobirà | 6 |
| Forêt de Pinós (106) ⚠️ | Pinós › Solsonès | 6 |
| Forêt de Pinós (115) ⚠️ | Pinós › Solsonès | 6 |
| Forêt de Pinós (119) ⚠️ | Pinós › Solsonès | 6 |
| Forêt de Pinós (121) ⚠️ | Pinós › Solsonès | 6 |
| Forêt de Montellà i Martinet (17) ⚠️ | Montellà i Martinet › Cerdanya (Lérida) | 6 |
| Forêt de Guixers (70) ⚠️ | Guixers › Solsonès | 6 |
| Forêt de Guixers (95) ⚠️ | Guixers › Solsonès | 6 |
| Forêt de la Coma i la Pedra (141) ⚠️ | la Coma i la Pedra › Solsonès | 6 |
| Forêt de Gósol (51) ⚠️ | Gósol › Berguedà (Lérida) | 6 |
| Forêt de Gósol (52) ⚠️ | Gósol › Berguedà (Lérida) | 6 |
| Forêt de Gósol (59) ⚠️ | Gósol › Berguedà (Lérida) | 6 |
| Forêt de Gósol (91) ⚠️ | Gósol › Berguedà (Lérida) | 6 |
| Forêt de Odèn (64) ⚠️ | Odèn › Solsonès | 6 |
| Forêt de Odèn (65) ⚠️ | Odèn › Solsonès | 6 |
| Forêt de Odèn (81) ⚠️ | Odèn › Solsonès | 6 |
| Forêt de Odèn (96) ⚠️ | Odèn › Solsonès | 6 |
| Forêt de Guixers (140) ⚠️ | Guixers › Solsonès | 6 |
| Forêt de Guixers (152) ⚠️ | Guixers › Solsonès | 6 |
| Forêt de Lladurs (204) ⚠️ | Lladurs › Solsonès | 6 |
| Forêt de Lladurs (211) ⚠️ | Lladurs › Solsonès | 6 |
| Forêt de Lladurs (213) ⚠️ | Lladurs › Solsonès | 6 |
| Forêt de Odèn (127) ⚠️ | Odèn › Solsonès | 6 |
| Forêt de Naut Aran (96) ⚠️ | Naut Aran › Val d'Aran | 6 |
| Forêt de Rialp (21) ⚠️ | Rialp › Pallars Sobirà | 6 |
| Forêt de Rialp (23) ⚠️ | Rialp › Pallars Sobirà | 6 |
| Forêt de Vilamòs (12) ⚠️ | Vilamòs › Val d'Aran | 6 |
| Forêt de les Valls de Valira (37) ⚠️ | les Valls de Valira › Alt Urgell | 6 |
| Forêt de les Valls de Valira (41) ⚠️ | les Valls de Valira › Alt Urgell | 6 |
| Forêt de les Valls de Valira (42) ⚠️ | les Valls de Valira › Alt Urgell | 6 |
| Forêt de Vilaller (60) ⚠️ | Vilaller › Alta Ribagorça | 6 |
| Forêt de Vilaller (68) ⚠️ | Vilaller › Alta Ribagorça | 6 |
| Forêt de Llardecans (5) ⚠️ | Llardecans › Segrià | 6 |
| Forêt de el Pont de Bar (8) ⚠️ | el Pont de Bar › Alt Urgell | 6 |
| Forêt de Oliana (15) ⚠️ | Oliana › Alt Urgell | 6 |
| Forêt de Oliana (20) ⚠️ | Oliana › Alt Urgell | 6 |
| Forêt de Cabó (13) ⚠️ | Cabó › Alt Urgell | 6 |
| Forêt de Cabó (18) ⚠️ | Cabó › Alt Urgell | 6 |
| Forêt de Coll de Nargó (88) ⚠️ | Coll de Nargó › Alt Urgell | 6 |
| Forêt de Olius (341) ⚠️ | Olius › Solsonès | 6 |
| Forêt de Bellver de Cerdanya (82) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 6 |
| Forêt de Olius (360) ⚠️ | Olius › Solsonès | 6 |
| Forêt de Lladorre (39) ⚠️ | Lladorre › Pallars Sobirà | 6 |
| Forêt de Lladorre (43) ⚠️ | Lladorre › Pallars Sobirà | 6 |
| Forêt de Àger (54) ⚠️ | Àger › Noguera | 6 |
| Forêt de Navès (220) ⚠️ | Navès › Solsonès | 6 |
| Forêt de Clariana de Cardener (181) ⚠️ | Clariana de Cardener › Solsonès | 6 |
| Forêt de Camarasa (47) ⚠️ | Camarasa › Noguera | 6 |
| Forêt de Sant Esteve de la Sarga (35) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 6 |
| Forêt de Sant Esteve de la Sarga (45) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 6 |
| Forêt de Àger (95) ⚠️ | Àger › Noguera | 6 |
| Forêt de Àger (128) ⚠️ | Àger › Noguera | 6 |
| Forêt de Àger (131) ⚠️ | Àger › Noguera | 6 |
| Forêt de Àger (153) ⚠️ | Àger › Noguera | 6 |
| Forêt de Àger (171) ⚠️ | Àger › Noguera | 6 |
| Forêt de Os de Balaguer (88) ⚠️ | Os de Balaguer › Noguera | 6 |
| Forêt de Coll de Nargó (102) ⚠️ | Coll de Nargó › Alt Urgell | 6 |
| Forêt de Coll de Nargó (104) ⚠️ | Coll de Nargó › Alt Urgell | 6 |
| Forêt de Abella de la Conca (79) ⚠️ | Abella de la Conca › Pallars Jussà | 6 |
| Forêt de Llobera (498) ⚠️ | Llobera › Solsonès | 6 |
| Forêt de el Pont de Suert (46) ⚠️ | el Pont de Suert › Alta Ribagorça | 6 |
| Forêt de la Vall de Boí (265) ⚠️ | la Vall de Boí › Alta Ribagorça | 6 |
| Forêt de el Pont de Suert (99) ⚠️ | el Pont de Suert › Alta Ribagorça | 6 |
| Forêt de Llobera (501) ⚠️ | Llobera › Solsonès | 6 |
| Forêt de Montferrer i Castellbò (88) ⚠️ | Montferrer i Castellbò › Alt Urgell | 6 |
| Forêt de Alins (70) ⚠️ | Alins › Pallars Sobirà | 6 |
| Forêt de Talarn (6) ⚠️ | Talarn › Pallars Jussà | 6 |
| Forêt de Tremp (129) ⚠️ | Tremp › Pallars Jussà | 6 |
| Forêt de Tírvia (5) ⚠️ | Tírvia › Pallars Sobirà | 6 |
| Forêt de Alins (98) ⚠️ | Alins › Pallars Sobirà | 6 |
| Forêt de Llobera (518) ⚠️ | Llobera › Solsonès | 6 |
| Forêt de Gósol (112) ⚠️ | Gósol › Berguedà (Lérida) | 6 |
| Forêt de Gósol (113) ⚠️ | Gósol › Berguedà (Lérida) | 6 |
| Forêt de Alins (103) ⚠️ | Alins › Pallars Sobirà | 6 |
| Forêt de Llavorsí (54) ⚠️ | Llavorsí › Pallars Sobirà | 6 |
| Forêt de Lles de Cerdanya (34) ⚠️ | Lles de Cerdanya › Cerdanya (Lérida) | 6 |
| Forêt de la Vall de Boí (270) ⚠️ | la Vall de Boí › Alta Ribagorça | 6 |
| Forêt de Massalcoreig (11) ⚠️ | Massalcoreig › Segrià | 6 |
| Forêt de Montferrer i Castellbò (109) ⚠️ | Montferrer i Castellbò › Alt Urgell | 6 |
| Forêt de Sort (36) ⚠️ | Sort › Pallars Sobirà | 6 |
| Forêt de Riner (171) ⚠️ | Riner › Solsonès | 6 |
| Forêt de Oliola (2) ⚠️ | Oliola › Noguera | 5 |
| Forêt de Pinell de Solsonès (7) ⚠️ | Pinell de Solsonès › Solsonès | 5 |
| Forêt de Talavera (2) ⚠️ | Talavera › Segarra | 5 |
| Forêt de Maials (6) ⚠️ | Maials › Segrià | 5 |
| Forêt de Artesa de Segre (8) ⚠️ | Artesa de Segre › Noguera | 5 |
| Forêt de Maials (8) ⚠️ | Maials › Segrià | 5 |
| Forêt de Montferrer i Castellbò (11) ⚠️ | Montferrer i Castellbò › Alt Urgell | 5 |
| Forêt de Sant Guim de Freixenet (4) ⚠️ | Sant Guim de Freixenet › Segarra | 5 |
| Forêt de Maials (12) ⚠️ | Maials › Segrià | 5 |
| Forêt de Tarrés (7) ⚠️ | Tarrés › Garrigues | 5 |
| Forêt de Isona i Conca Dellà (9) ⚠️ | Isona i Conca Dellà › Pallars Jussà | 5 |
| Forêt de la Baronia de Rialb (31) ⚠️ | la Baronia de Rialb › Noguera | 5 |
| Forêt de Bovera (7) ⚠️ | Bovera › Garrigues | 5 |
| Bosc del Miró ⚠️ | Cervera › Segarra | 5 |
| Forêt de la Coma i la Pedra (39) ⚠️ | la Coma i la Pedra › Solsonès | 5 |
| Forêt de la Coma i la Pedra (48) ⚠️ | la Coma i la Pedra › Solsonès | 5 |
| Forêt de la Coma i la Pedra (67) ⚠️ | la Coma i la Pedra › Solsonès | 5 |
| Forêt de Lleida (7) ⚠️ | Lleida › Segrià | 5 |
| Forêt de Espot (20) ⚠️ | Espot › Pallars Sobirà | 5 |
| Forêt de la Vall de Boí (12) ⚠️ | la Vall de Boí › Alta Ribagorça | 5 |
| Forêt de Montoliu de Segarra (4) ⚠️ | Montoliu de Segarra › Segarra | 5 |
| Forêt de Alins (9) ⚠️ | Alins › Pallars Sobirà | 5 |
| Forêt de Naut Aran (15) ⚠️ | Naut Aran › Val d'Aran | 5 |
| Forêt de Alt Àneu (16) ⚠️ | Alt Àneu › Pallars Sobirà | 5 |
| Forêt de Almenar (2) ⚠️ | Almenar › Segrià | 5 |
| Forêt de Sort (6) ⚠️ | Sort › Pallars Sobirà | 5 |
| Forêt de Gavet de la Conca (9) ⚠️ | Gavet de la Conca › Pallars Jussà | 5 |
| Forêt de Bellver de Cerdanya (9) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 5 |
| Bois de Sant Guim de Freixenet (2) ⚠️ | Sant Guim de Freixenet › Segarra | 5 |
| Forêt de les Valls de Valira (14) ⚠️ | les Valls de Valira › Alt Urgell | 5 |
| Forêt de la Vall de Boí (19) ⚠️ | la Vall de Boí › Alta Ribagorça | 5 |
| Forêt de Gósol (5) ⚠️ | Gósol › Berguedà (Lérida) | 5 |
| Forêt de Tremp (72) ⚠️ | Tremp › Pallars Jussà | 5 |
| Forêt de Llobera (321) ⚠️ | Llobera › Solsonès | 5 |
| Forêt de Clariana de Cardener (109) ⚠️ | Clariana de Cardener › Solsonès | 5 |
| Forêt de Clariana de Cardener (116) ⚠️ | Clariana de Cardener › Solsonès | 5 |
| Forêt de Clariana de Cardener (119) ⚠️ | Clariana de Cardener › Solsonès | 5 |
| Forêt de Clariana de Cardener (144) ⚠️ | Clariana de Cardener › Solsonès | 5 |
| Forêt de Odèn (27) ⚠️ | Odèn › Solsonès | 5 |
| Forêt de la Vall de Boí (26) ⚠️ | la Vall de Boí › Alta Ribagorça | 5 |
| Bois de Sant Esteve de la Sarga (4) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 5 |
| Forêt de Vall de Cardós (32) ⚠️ | Vall de Cardós › Pallars Sobirà | 5 |
| Forêt de Guixers (26) ⚠️ | Guixers › Solsonès | 5 |
| Forêt de Naut Aran (48) ⚠️ | Naut Aran › Val d'Aran | 5 |
| Forêt de Vielha e Mijaran (43) ⚠️ | Vielha e Mijaran › Val d'Aran | 5 |
| Forêt de Vilaller (29) ⚠️ | Vilaller › Alta Ribagorça | 5 |
| Forêt de la Seu d'Urgell (4) ⚠️ | la Seu d'Urgell › Alt Urgell | 5 |
| Forêt de Naut Aran (62) ⚠️ | Naut Aran › Val d'Aran | 5 |
| Forêt de Os de Balaguer (28) ⚠️ | Os de Balaguer › Noguera | 5 |
| Forêt de Guixers (34) ⚠️ | Guixers › Solsonès | 5 |
| Forêt de Navès (46) ⚠️ | Navès › Solsonès | 5 |
| Forêt de Olius (312) ⚠️ | Olius › Solsonès | 5 |
| Forêt de Olius (313) ⚠️ | Olius › Solsonès | 5 |
| Forêt de Castellar de la Ribera (23) ⚠️ | Castellar de la Ribera › Solsonès | 5 |
| Forêt de Navès (66) ⚠️ | Navès › Solsonès | 5 |
| Forêt de Es Bòrdes (5) ⚠️ | Es Bòrdes › Val d'Aran | 5 |
| Forêt de la Coma i la Pedra (101) ⚠️ | la Coma i la Pedra › Solsonès | 5 |
| Forêt de la Molsosa (38) ⚠️ | la Molsosa › Solsonès | 5 |
| Forêt de Navès (84) ⚠️ | Navès › Solsonès | 5 |
| Forêt de Navès (107) ⚠️ | Navès › Solsonès | 5 |
| Forêt de Navès (111) ⚠️ | Navès › Solsonès | 5 |
| Bois de Llardecans ⚠️ | Llardecans › Segrià | 5 |
| Forêt de Coll de Nargó (43) ⚠️ | Coll de Nargó › Alt Urgell | 5 |
| Forêt de Fígols i Alinyà (29) ⚠️ | Fígols i Alinyà › Alt Urgell | 5 |
| Forêt de Alins (25) ⚠️ | Alins › Pallars Sobirà | 5 |
| Bois de Sant Guim de Freixenet (6) ⚠️ | Sant Guim de Freixenet › Segarra | 5 |
| Forêt de Lladurs (181) ⚠️ | Lladurs › Solsonès | 5 |
| Forêt de Lladurs (189) ⚠️ | Lladurs › Solsonès | 5 |
| Forêt de Odèn (57) ⚠️ | Odèn › Solsonès | 5 |
| Forêt de la Molsosa (39) ⚠️ | la Molsosa › Solsonès | 5 |
| Forêt de la Molsosa (40) ⚠️ | la Molsosa › Solsonès | 5 |
| Forêt de la Molsosa (42) ⚠️ | la Molsosa › Solsonès | 5 |
| Forêt de Pinós (60) ⚠️ | Pinós › Solsonès | 5 |
| Forêt de Pinós (96) ⚠️ | Pinós › Solsonès | 5 |
| Forêt de les Valls de Valira (28) ⚠️ | les Valls de Valira › Alt Urgell | 5 |
| Forêt de Llavorsí (24) ⚠️ | Llavorsí › Pallars Sobirà | 5 |
| Forêt de la Guingueta d'Àneu (38) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 5 |
| Forêt de la Guingueta d'Àneu (41) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 5 |
| Forêt de la Guingueta d'Àneu (60) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 5 |
| Forêt de Soriguera (34) ⚠️ | Soriguera › Pallars Sobirà | 5 |
| Forêt de la Vall de Boí (260) ⚠️ | la Vall de Boí › Alta Ribagorça | 5 |
| Forêt de Alt Àneu (60) ⚠️ | Alt Àneu › Pallars Sobirà | 5 |
| Forêt de Alt Àneu (61) ⚠️ | Alt Àneu › Pallars Sobirà | 5 |
| Forêt de Alt Àneu (66) ⚠️ | Alt Àneu › Pallars Sobirà | 5 |
| Forêt de Gósol (18) ⚠️ | Gósol › Berguedà (Lérida) | 5 |
| Forêt de Esterri de Cardós (7) ⚠️ | Esterri de Cardós › Pallars Sobirà | 5 |
| Forêt de Riner (144) ⚠️ | Riner › Solsonès | 5 |
| Forêt de Pinós (111) ⚠️ | Pinós › Solsonès | 5 |
| Forêt de Pinós (116) ⚠️ | Pinós › Solsonès | 5 |
| Forêt de Riner (151) ⚠️ | Riner › Solsonès | 5 |
| Forêt de Pinós (130) ⚠️ | Pinós › Solsonès | 5 |
| Forêt de Riu de Cerdanya (6) ⚠️ | Riu de Cerdanya › Cerdanya (Lérida) | 5 |
| Forêt de Guixers (81) ⚠️ | Guixers › Solsonès | 5 |
| Forêt de Gósol (39) ⚠️ | Gósol › Berguedà (Lérida) | 5 |
| Forêt de Navès (152) ⚠️ | Navès › Solsonès | 5 |
| Forêt de la Coma i la Pedra (137) ⚠️ | la Coma i la Pedra › Solsonès | 5 |
| Forêt de la Coma i la Pedra (151) ⚠️ | la Coma i la Pedra › Solsonès | 5 |
| Forêt de la Coma i la Pedra (169) ⚠️ | la Coma i la Pedra › Solsonès | 5 |
| Forêt de Gósol (70) ⚠️ | Gósol › Berguedà (Lérida) | 5 |
| Forêt de Gósol (75) ⚠️ | Gósol › Berguedà (Lérida) | 5 |
| Forêt de Gósol (85) ⚠️ | Gósol › Berguedà (Lérida) | 5 |
| Forêt de la Coma i la Pedra (175) ⚠️ | la Coma i la Pedra › Solsonès | 5 |
| Forêt de Gósol (107) ⚠️ | Gósol › Berguedà (Lérida) | 5 |
| Forêt de Navès (158) ⚠️ | Navès › Solsonès | 5 |
| Forêt de Guixers (139) ⚠️ | Guixers › Solsonès | 5 |
| Forêt de Guixers (151) ⚠️ | Guixers › Solsonès | 5 |
| Forêt de Odèn (128) ⚠️ | Odèn › Solsonès | 5 |
| Forêt de Odèn (131) ⚠️ | Odèn › Solsonès | 5 |
| Forêt de Bellver de Cerdanya (55) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 5 |
| Forêt de Josa i Tuixén (26) ⚠️ | Josa i Tuixén › Alt Urgell | 5 |
| Forêt de Naut Aran (74) ⚠️ | Naut Aran › Val d'Aran | 5 |
| Forêt de Alt Àneu (72) ⚠️ | Alt Àneu › Pallars Sobirà | 5 |
| Forêt de Alt Àneu (75) ⚠️ | Alt Àneu › Pallars Sobirà | 5 |
| Forêt de Alt Àneu (136) ⚠️ | Alt Àneu › Pallars Sobirà | 5 |
| Forêt de Naut Aran (106) ⚠️ | Naut Aran › Val d'Aran | 5 |
| Forêt de Canejan (27) ⚠️ | Canejan › Val d'Aran | 5 |
| Forêt de Llavorsí (49) ⚠️ | Llavorsí › Pallars Sobirà | 5 |
| Forêt de Vielha e Mijaran (60) ⚠️ | Vielha e Mijaran › Val d'Aran | 5 |
| Forêt de les Valls de Valira (40) ⚠️ | les Valls de Valira › Alt Urgell | 5 |
| Forêt de Vilaller (37) ⚠️ | Vilaller › Alta Ribagorça | 5 |
| Forêt de el Pont de Bar (5) ⚠️ | el Pont de Bar › Alt Urgell | 5 |
| Forêt de Bellver de Cerdanya (66) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 5 |
| Forêt de les Valls de Valira (66) ⚠️ | les Valls de Valira › Alt Urgell | 5 |
| Forêt de les Valls de Valira (69) ⚠️ | les Valls de Valira › Alt Urgell | 5 |
| Forêt de les Valls de Valira (78) ⚠️ | les Valls de Valira › Alt Urgell | 5 |
| Forêt de les Valls de Valira (79) ⚠️ | les Valls de Valira › Alt Urgell | 5 |
| Forêt de les Valls de Valira (83) ⚠️ | les Valls de Valira › Alt Urgell | 5 |
| Forêt de les Valls de Valira (98) ⚠️ | les Valls de Valira › Alt Urgell | 5 |
| Forêt de Ribera d'Urgellet (38) ⚠️ | Ribera d'Urgellet › Alt Urgell | 5 |
| Forêt de Ribera d'Urgellet (41) ⚠️ | Ribera d'Urgellet › Alt Urgell | 5 |
| Forêt de Ribera d'Urgellet (56) ⚠️ | Ribera d'Urgellet › Alt Urgell | 5 |
| Forêt de Cabó (26) ⚠️ | Cabó › Alt Urgell | 5 |
| Forêt de Coll de Nargó (87) ⚠️ | Coll de Nargó › Alt Urgell | 5 |
| Forêt de la Baronia de Rialb (51) ⚠️ | la Baronia de Rialb › Noguera | 5 |
| Forêt de Ponts (8) ⚠️ | Ponts › Noguera | 5 |
| Forêt de Bassella (26) ⚠️ | Bassella › Alt Urgell | 5 |
| Forêt de Josa i Tuixén (31) ⚠️ | Josa i Tuixén › Alt Urgell | 5 |
| Forêt de Josa i Tuixén (45) ⚠️ | Josa i Tuixén › Alt Urgell | 5 |
| Forêt de Josa i Tuixén (47) ⚠️ | Josa i Tuixén › Alt Urgell | 5 |
| Forêt de Tremp (88) ⚠️ | Tremp › Pallars Jussà | 5 |
| Forêt de Olius (328) ⚠️ | Olius › Solsonès | 5 |
| Forêt de Navès (180) ⚠️ | Navès › Solsonès | 5 |
| Forêt de Navès (198) ⚠️ | Navès › Solsonès | 5 |
| Forêt de Navès (208) ⚠️ | Navès › Solsonès | 5 |
| Forêt de Llimiana (8) ⚠️ | Llimiana › Pallars Jussà | 5 |
| Forêt de Àger (46) ⚠️ | Àger › Noguera | 5 |
| Forêt de Sant Esteve de la Sarga (11) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 5 |
| Forêt de Sant Esteve de la Sarga (19) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 5 |
| Forêt de Àger (56) ⚠️ | Àger › Noguera | 5 |
| Forêt de Baix Pallars (56) ⚠️ | Baix Pallars › Pallars Sobirà | 5 |
| Forêt de Clariana de Cardener (185) ⚠️ | Clariana de Cardener › Solsonès | 5 |
| Forêt de Clariana de Cardener (187) ⚠️ | Clariana de Cardener › Solsonès | 5 |
| Forêt de Llimiana (12) ⚠️ | Llimiana › Pallars Jussà | 5 |
| Forêt de Camarasa (40) ⚠️ | Camarasa › Noguera | 5 |
| Forêt de Sant Esteve de la Sarga (56) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 5 |
| Forêt de Sant Esteve de la Sarga (71) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 5 |
| Forêt de Camarasa (50) ⚠️ | Camarasa › Noguera | 5 |
| Forêt de Àger (130) ⚠️ | Àger › Noguera | 5 |
| Forêt de Àger (161) ⚠️ | Àger › Noguera | 5 |
| Forêt de Os de Balaguer (30) ⚠️ | Os de Balaguer › Noguera | 5 |
| Forêt de Os de Balaguer (54) ⚠️ | Os de Balaguer › Noguera | 5 |
| Forêt de Os de Balaguer (78) ⚠️ | Os de Balaguer › Noguera | 5 |
| Forêt de Os de Balaguer (85) ⚠️ | Os de Balaguer › Noguera | 5 |
| Forêt de Coll de Nargó (105) ⚠️ | Coll de Nargó › Alt Urgell | 5 |
| Forêt de Abella de la Conca (38) ⚠️ | Abella de la Conca › Pallars Jussà | 5 |
| Forêt de Abella de la Conca (74) ⚠️ | Abella de la Conca › Pallars Jussà | 5 |
| Forêt de Coll de Nargó (133) ⚠️ | Coll de Nargó › Alt Urgell | 5 |
| Forêt de la Pobla de Segur (14) ⚠️ | la Pobla de Segur › Pallars Jussà | 5 |
| Forêt de la Pobla de Segur (18) ⚠️ | la Pobla de Segur › Pallars Jussà | 5 |
| Forêt de el Pont de Suert (61) ⚠️ | el Pont de Suert › Alta Ribagorça | 5 |
| Forêt de el Pont de Suert (84) ⚠️ | el Pont de Suert › Alta Ribagorça | 5 |
| Forêt de Llobera (502) ⚠️ | Llobera › Solsonès | 5 |
| Forêt de la Vansa i Fórnols (31) ⚠️ | la Vansa i Fórnols › Alt Urgell | 5 |
| Forêt de la Vansa i Fórnols (32) ⚠️ | la Vansa i Fórnols › Alt Urgell | 5 |
| Forêt de Tremp (124) ⚠️ | Tremp › Pallars Jussà | 5 |
| Forêt de Llimiana (17) ⚠️ | Llimiana › Pallars Jussà | 5 |
| Forêt de Alins (86) ⚠️ | Alins › Pallars Sobirà | 5 |
| Forêt de Alins (90) ⚠️ | Alins › Pallars Sobirà | 5 |
| Forêt de Farrera (17) ⚠️ | Farrera › Pallars Sobirà | 5 |
| Bois de la Vall de Boí (3) ⚠️ | la Vall de Boí › Alta Ribagorça | 5 |
| Forêt de Clariana de Cardener (237) ⚠️ | Clariana de Cardener › Solsonès | 5 |
| Forêt de Lles de Cerdanya (30) ⚠️ | Lles de Cerdanya › Cerdanya (Lérida) | 5 |
| Forêt de Arsèguel (14) ⚠️ | Arsèguel › Alt Urgell | 5 |
| Forêt de Conca de Dalt (45) ⚠️ | Conca de Dalt › Pallars Jussà | 5 |
| Forêt de Massalcoreig (9) ⚠️ | Massalcoreig › Segrià | 5 |
| Forêt de Alàs i Cerc (37) ⚠️ | Alàs i Cerc › Alt Urgell | 5 |
| Forêt de Conca de Dalt (47) ⚠️ | Conca de Dalt › Pallars Jussà | 5 |
| Forêt de la Pobla de Segur (32) ⚠️ | la Pobla de Segur › Pallars Jussà | 5 |
| Forêt de Senterada (18) ⚠️ | Senterada › Pallars Jussà | 5 |
| Forêt de Senterada (19) ⚠️ | Senterada › Pallars Jussà | 5 |
| Forêt de Salàs de Pallars (3) ⚠️ | Salàs de Pallars › Pallars Jussà | 5 |
| Forêt de Riner (168) ⚠️ | Riner › Solsonès | 5 |
| Forêt de Sort (21) ⚠️ | Sort › Pallars Sobirà | 5 |
| Forêt de Soriguera (47) ⚠️ | Soriguera › Pallars Sobirà | 5 |
| Forêt de Torres de Segre (14) ⚠️ | Torres de Segre › Segrià | 5 |
| Forêt de Vall de Cardós (61) ⚠️ | Vall de Cardós › Pallars Sobirà | 5 |
| Forêt de Bossòst ⚠️ | Bossòst › Val d'Aran | 4 |
| Parc Municipal dels Camps Elisis ⚠️ | Lleida › Segrià | 4 |
| Forêt de Gósol ⚠️ | Gósol › Berguedà (Lérida) | 4 |
| Forêt de Alins (4) ⚠️ | Alins › Pallars Sobirà | 4 |
| Forêt de Castellar de la Ribera (5) ⚠️ | Castellar de la Ribera › Solsonès | 4 |
| Forêt de Les ⚠️ | Les › Val d'Aran | 4 |
| Forêt de Castellar de la Ribera (8) ⚠️ | Castellar de la Ribera › Solsonès | 4 |
| Forêt de la Molsosa (3) ⚠️ | la Molsosa › Solsonès | 4 |
| Forêt de Bellver de Cerdanya (2) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 4 |
| Forêt de Vilaller (22) ⚠️ | Vilaller › Alta Ribagorça | 4 |
| Forêt de Ribera d'Ondara (6) ⚠️ | Ribera d'Ondara › Segarra | 4 |
| Bois de Maldà (2) ⚠️ | Maldà › Urgell | 4 |
| Bois de els Plans de Sió (7) ⚠️ | els Plans de Sió › Segarra | 4 |
| Bois de Gimenells i el Pla de la Font (10) ⚠️ | Gimenells i el Pla de la Font › Segrià | 4 |
| Forêt de Lleida (8) ⚠️ | Lleida › Segrià | 4 |
| Forêt de Espot (5) ⚠️ | Espot › Pallars Sobirà | 4 |
| Forêt de Prullans (3) ⚠️ | Prullans › Cerdanya (Lérida) | 4 |
| Forêt de Sarroca de Bellera (15) ⚠️ | Sarroca de Bellera › Pallars Jussà | 4 |
| Forêt de Solsona (12) ⚠️ | Solsona › Solsonès | 4 |
| Forêt de Cervera (4) ⚠️ | Cervera › Segarra | 4 |
| Bois de Ribera d'Ondara (2) ⚠️ | Ribera d'Ondara › Segarra | 4 |
| Bois de Alcarràs (6) ⚠️ | Alcarràs › Segrià | 4 |
| Forêt de Alt Àneu (15) ⚠️ | Alt Àneu › Pallars Sobirà | 4 |
| Forêt de Navès (9) ⚠️ | Navès › Solsonès | 4 |
| Forêt de el Pont de Suert (27) ⚠️ | el Pont de Suert › Alta Ribagorça | 4 |
| Forêt de Olius (25) ⚠️ | Olius › Solsonès | 4 |
| Forêt de Olius (28) ⚠️ | Olius › Solsonès | 4 |
| Forêt de Naut Aran (29) ⚠️ | Naut Aran › Val d'Aran | 4 |
| Bois de Farrera ⚠️ | Farrera › Pallars Sobirà | 4 |
| Bois de Talarn ⚠️ | Talarn › Pallars Jussà | 4 |
| Bois de Llimiana (2) ⚠️ | Llimiana › Pallars Jussà | 4 |
| Bois de la Torre de Cabdella ⚠️ | la Torre de Cabdella › Pallars Jussà | 4 |
| Bois de Lleida (11) ⚠️ | Lleida › Segrià | 4 |
| Forêt de Algerri ⚠️ | Algerri › Noguera | 4 |
| Forêt de Lleida (15) ⚠️ | Lleida › Segrià | 4 |
| Forêt de Lladurs (77) ⚠️ | Lladurs › Solsonès | 4 |
| Forêt de Olius (85) ⚠️ | Olius › Solsonès | 4 |
| Forêt de Olius (271) ⚠️ | Olius › Solsonès | 4 |
| Forêt de Olius (302) ⚠️ | Olius › Solsonès | 4 |
| Bois de Sant Guim de Freixenet (3) ⚠️ | Sant Guim de Freixenet › Segarra | 4 |
| Forêt de Llobera (55) ⚠️ | Llobera › Solsonès | 4 |
| Forêt de Àger (11) ⚠️ | Àger › Noguera | 4 |
| Forêt de Abella de la Conca (13) ⚠️ | Abella de la Conca › Pallars Jussà | 4 |
| Bois de la Torre de Cabdella (4) ⚠️ | la Torre de Cabdella › Pallars Jussà | 4 |
| Bois de la Torre de Cabdella (31) ⚠️ | la Torre de Cabdella › Pallars Jussà | 4 |
| Bois de la Torre de Cabdella (36) ⚠️ | la Torre de Cabdella › Pallars Jussà | 4 |
| Bois de Alàs i Cerc (4) ⚠️ | Alàs i Cerc › Alt Urgell | 4 |
| Forêt de Llobera (308) ⚠️ | Llobera › Solsonès | 4 |
| Bois de les Valls de Valira (8) ⚠️ | les Valls de Valira › Alt Urgell | 4 |
| Forêt de Naut Aran (32) ⚠️ | Naut Aran › Val d'Aran | 4 |
| Forêt de Naut Aran (36) ⚠️ | Naut Aran › Val d'Aran | 4 |
| Forêt de Naut Aran (41) ⚠️ | Naut Aran › Val d'Aran | 4 |
| Forêt de Clariana de Cardener (121) ⚠️ | Clariana de Cardener › Solsonès | 4 |
| Forêt de la Vall de Boí (28) ⚠️ | la Vall de Boí › Alta Ribagorça | 4 |
| Forêt de la Vall de Boí (41) ⚠️ | la Vall de Boí › Alta Ribagorça | 4 |
| Forêt de la Vall de Boí (71) ⚠️ | la Vall de Boí › Alta Ribagorça | 4 |
| Forêt de Navès (26) ⚠️ | Navès › Solsonès | 4 |
| Forêt de Alt Àneu (32) ⚠️ | Alt Àneu › Pallars Sobirà | 4 |
| Forêt de Espot (27) ⚠️ | Espot › Pallars Sobirà | 4 |
| Forêt de Castell de Mur (11) ⚠️ | Castell de Mur › Pallars Jussà | 4 |
| Forêt de Vilaller (30) ⚠️ | Vilaller › Alta Ribagorça | 4 |
| Forêt de la Seu d'Urgell (5) ⚠️ | la Seu d'Urgell › Alt Urgell | 4 |
| Forêt de Naut Aran (50) ⚠️ | Naut Aran › Val d'Aran | 4 |
| Forêt de Esterri d'Àneu (5) ⚠️ | Esterri d'Àneu › Pallars Sobirà | 4 |
| Forêt de Baix Pallars (33) ⚠️ | Baix Pallars › Pallars Sobirà | 4 |
| Forêt de Camarasa (19) ⚠️ | Camarasa › Noguera | 4 |
| Forêt de Tremp (78) ⚠️ | Tremp › Pallars Jussà | 4 |
| Forêt de Torà (16) ⚠️ | Torà › Solsonès | 4 |
| Forêt de Torà (18) ⚠️ | Torà › Solsonès | 4 |
| Forêt de Torà (20) ⚠️ | Torà › Solsonès | 4 |
| Forêt de Balaguer (7) ⚠️ | Balaguer › Noguera | 4 |
| Forêt de Camarasa (24) ⚠️ | Camarasa › Noguera | 4 |
| Forêt de Guixers (41) ⚠️ | Guixers › Solsonès | 4 |
| Forêt de Guixers (45) ⚠️ | Guixers › Solsonès | 4 |
| Forêt de Baix Pallars (39) ⚠️ | Baix Pallars › Pallars Sobirà | 4 |
| Forêt de Senterada (8) ⚠️ | Senterada › Pallars Jussà | 4 |
| Forêt de Bellver de Cerdanya (22) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 4 |
| Forêt de Navès (55) ⚠️ | Navès › Solsonès | 4 |
| Forêt de Àger (28) ⚠️ | Àger › Noguera | 4 |
| Forêt de Navès (63) ⚠️ | Navès › Solsonès | 4 |
| Forêt de Bassella (13) ⚠️ | Bassella › Alt Urgell | 4 |
| Forêt de Bassella (16) ⚠️ | Bassella › Alt Urgell | 4 |
| Forêt de Olius (319) ⚠️ | Olius › Solsonès | 4 |
| Forêt de Vilamòs (3) ⚠️ | Vilamòs › Val d'Aran | 4 |
| Forêt de les Avellanes i Santa Linya (18) ⚠️ | les Avellanes i Santa Linya › Noguera | 4 |
| Forêt de la Molsosa (35) ⚠️ | la Molsosa › Solsonès | 4 |
| Forêt de Navès (89) ⚠️ | Navès › Solsonès | 4 |
| Forêt de Navès (91) ⚠️ | Navès › Solsonès | 4 |
| Forêt de Navès (110) ⚠️ | Navès › Solsonès | 4 |
| Forêt de Gósol (14) ⚠️ | Gósol › Berguedà (Lérida) | 4 |
| Forêt de Coll de Nargó (82) ⚠️ | Coll de Nargó › Alt Urgell | 4 |
| Forêt de Juncosa (23) ⚠️ | Juncosa › Garrigues | 4 |
| Forêt de Isona i Conca Dellà (33) ⚠️ | Isona i Conca Dellà › Pallars Jussà | 4 |
| Forêt de Guixers (56) ⚠️ | Guixers › Solsonès | 4 |
| Forêt de Lladurs (191) ⚠️ | Lladurs › Solsonès | 4 |
| Forêt de Lladurs (192) ⚠️ | Lladurs › Solsonès | 4 |
| Forêt de les Oluges (2) ⚠️ | les Oluges › Segarra | 4 |
| Forêt de les Oluges (3) ⚠️ | les Oluges › Segarra | 4 |
| Forêt de Navès (142) ⚠️ | Navès › Solsonès | 4 |
| Forêt de Oliana (7) ⚠️ | Oliana › Alt Urgell | 4 |
| Forêt de la Coma i la Pedra (111) ⚠️ | la Coma i la Pedra › Solsonès | 4 |
| Forêt de Guixers (60) ⚠️ | Guixers › Solsonès | 4 |
| Forêt de la Coma i la Pedra (116) ⚠️ | la Coma i la Pedra › Solsonès | 4 |
| Forêt de Peramola (12) ⚠️ | Peramola › Alt Urgell | 4 |
| Forêt de Peramola (16) ⚠️ | Peramola › Alt Urgell | 4 |
| Forêt de Sort (16) ⚠️ | Sort › Pallars Sobirà | 4 |
| Forêt de Pinós (56) ⚠️ | Pinós › Solsonès | 4 |
| Forêt de Pinós (94) ⚠️ | Pinós › Solsonès | 4 |
| Forêt de Pinós (97) ⚠️ | Pinós › Solsonès | 4 |
| Forêt de Llavorsí (17) ⚠️ | Llavorsí › Pallars Sobirà | 4 |
| Forêt de la Guingueta d'Àneu (39) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 4 |
| Forêt de la Guingueta d'Àneu (49) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 4 |
| Forêt de la Guingueta d'Àneu (58) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 4 |
| Forêt de la Guingueta d'Àneu (69) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 4 |
| Forêt de Soriguera (37) ⚠️ | Soriguera › Pallars Sobirà | 4 |
| Forêt de Soriguera (39) ⚠️ | Soriguera › Pallars Sobirà | 4 |
| Forêt de Montgai (2) ⚠️ | Montgai › Noguera | 4 |
| Forêt de Vielha e Mijaran (55) ⚠️ | Vielha e Mijaran › Val d'Aran | 4 |
| Forêt de Vielha e Mijaran (59) ⚠️ | Vielha e Mijaran › Val d'Aran | 4 |
| Forêt de la Vall de Boí (259) ⚠️ | la Vall de Boí › Alta Ribagorça | 4 |
| Forêt de Gósol (26) ⚠️ | Gósol › Berguedà (Lérida) | 4 |
| Forêt de Gósol (30) ⚠️ | Gósol › Berguedà (Lérida) | 4 |
| Forêt de la Coma i la Pedra (127) ⚠️ | la Coma i la Pedra › Solsonès | 4 |
| Forêt de la Coma i la Pedra (128) ⚠️ | la Coma i la Pedra › Solsonès | 4 |
| Forêt de Pinós (133) ⚠️ | Pinós › Solsonès | 4 |
| Forêt de Pinós (151) ⚠️ | Pinós › Solsonès | 4 |
| Forêt de Riu de Cerdanya (15) ⚠️ | Riu de Cerdanya › Cerdanya (Lérida) | 4 |
| Forêt de Montellà i Martinet (35) ⚠️ | Montellà i Martinet › Cerdanya (Lérida) | 4 |
| Forêt de Montellà i Martinet (36) ⚠️ | Montellà i Martinet › Cerdanya (Lérida) | 4 |
| Forêt de Guixers (77) ⚠️ | Guixers › Solsonès | 4 |
| Forêt de Guixers (89) ⚠️ | Guixers › Solsonès | 4 |
| Forêt de Guixers (93) ⚠️ | Guixers › Solsonès | 4 |
| Forêt de la Coma i la Pedra (138) ⚠️ | la Coma i la Pedra › Solsonès | 4 |
| Forêt de la Coma i la Pedra (144) ⚠️ | la Coma i la Pedra › Solsonès | 4 |
| Forêt de Guixers (102) ⚠️ | Guixers › Solsonès | 4 |
| Forêt de Guixers (106) ⚠️ | Guixers › Solsonès | 4 |
| Forêt de la Coma i la Pedra (166) ⚠️ | la Coma i la Pedra › Solsonès | 4 |
| Forêt de Gósol (81) ⚠️ | Gósol › Berguedà (Lérida) | 4 |
| Forêt de Gósol (87) ⚠️ | Gósol › Berguedà (Lérida) | 4 |
| Forêt de Gósol (88) ⚠️ | Gósol › Berguedà (Lérida) | 4 |
| Forêt de la Coma i la Pedra (177) ⚠️ | la Coma i la Pedra › Solsonès | 4 |
| Forêt de Gósol (106) ⚠️ | Gósol › Berguedà (Lérida) | 4 |
| Forêt de Navès (161) ⚠️ | Navès › Solsonès | 4 |
| Forêt de Guixers (129) ⚠️ | Guixers › Solsonès | 4 |
| Forêt de Odèn (68) ⚠️ | Odèn › Solsonès | 4 |
| Forêt de Odèn (91) ⚠️ | Odèn › Solsonès | 4 |
| Forêt de Odèn (93) ⚠️ | Odèn › Solsonès | 4 |
| Forêt de Guixers (138) ⚠️ | Guixers › Solsonès | 4 |
| Forêt de Sant Llorenç de Morunys (31) ⚠️ | Sant Llorenç de Morunys › Solsonès | 4 |
| Forêt de Guixers (143) ⚠️ | Guixers › Solsonès | 4 |
| Forêt de Guixers (144) ⚠️ | Guixers › Solsonès | 4 |
| Forêt de Lladurs (196) ⚠️ | Lladurs › Solsonès | 4 |
| Forêt de Lladurs (201) ⚠️ | Lladurs › Solsonès | 4 |
| Forêt de Odèn (105) ⚠️ | Odèn › Solsonès | 4 |
| Forêt de Odèn (112) ⚠️ | Odèn › Solsonès | 4 |
| Forêt de Lladurs (217) ⚠️ | Lladurs › Solsonès | 4 |
| Forêt de Lladurs (233) ⚠️ | Lladurs › Solsonès | 4 |
| Forêt de Lladurs (251) ⚠️ | Lladurs › Solsonès | 4 |
| Forêt de Lladurs (253) ⚠️ | Lladurs › Solsonès | 4 |
| Forêt de Josa i Tuixén (25) ⚠️ | Josa i Tuixén › Alt Urgell | 4 |
| Forêt de Josa i Tuixén (27) ⚠️ | Josa i Tuixén › Alt Urgell | 4 |
| Forêt de Bellver de Cerdanya (58) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 4 |
| Forêt de Alt Àneu (92) ⚠️ | Alt Àneu › Pallars Sobirà | 4 |
| Forêt de Alt Àneu (101) ⚠️ | Alt Àneu › Pallars Sobirà | 4 |
| Forêt de Alt Àneu (102) ⚠️ | Alt Àneu › Pallars Sobirà | 4 |
| Forêt de Alt Àneu (105) ⚠️ | Alt Àneu › Pallars Sobirà | 4 |
| Forêt de Alt Àneu (139) ⚠️ | Alt Àneu › Pallars Sobirà | 4 |
| Forêt de Alt Àneu (142) ⚠️ | Alt Àneu › Pallars Sobirà | 4 |
| Forêt de Alt Àneu (150) ⚠️ | Alt Àneu › Pallars Sobirà | 4 |
| Forêt de Naut Aran (101) ⚠️ | Naut Aran › Val d'Aran | 4 |
| Forêt de Canejan (16) ⚠️ | Canejan › Val d'Aran | 4 |
| Forêt de Lladorre (24) ⚠️ | Lladorre › Pallars Sobirà | 4 |
| Forêt de Lladorre (30) ⚠️ | Lladorre › Pallars Sobirà | 4 |
| Forêt de les Valls de Valira (59) ⚠️ | les Valls de Valira › Alt Urgell | 4 |
| Forêt de Alins (68) ⚠️ | Alins › Pallars Sobirà | 4 |
| Forêt de Vilaller (47) ⚠️ | Vilaller › Alta Ribagorça | 4 |
| Forêt de Vilaller (59) ⚠️ | Vilaller › Alta Ribagorça | 4 |
| Forêt de Vilaller (67) ⚠️ | Vilaller › Alta Ribagorça | 4 |
| Forêt de Arsèguel (4) ⚠️ | Arsèguel › Alt Urgell | 4 |
| Forêt de les Valls de Valira (71) ⚠️ | les Valls de Valira › Alt Urgell | 4 |
| Forêt de les Valls de Valira (73) ⚠️ | les Valls de Valira › Alt Urgell | 4 |
| Forêt de la Seu d'Urgell (11) ⚠️ | la Seu d'Urgell › Alt Urgell | 4 |
| Forêt de les Valls de Valira (100) ⚠️ | la Seu d'Urgell › Alt Urgell | 4 |
| Forêt de Ribera d'Urgellet (40) ⚠️ | Ribera d'Urgellet › Alt Urgell | 4 |
| Forêt de Montferrer i Castellbò (50) ⚠️ | Montferrer i Castellbò › Alt Urgell | 4 |
| Forêt de Montferrer i Castellbò (63) ⚠️ | Montferrer i Castellbò › Alt Urgell | 4 |
| Forêt de Cabó (21) ⚠️ | Cabó › Alt Urgell | 4 |
| Forêt de Cabó (22) ⚠️ | Cabó › Alt Urgell | 4 |
| Forêt de Cabó (29) ⚠️ | Cabó › Alt Urgell | 4 |
| Forêt de Ponts (9) ⚠️ | Ponts › Noguera | 4 |
| Forêt de Ponts (14) ⚠️ | Ponts › Noguera | 4 |
| Forêt de Josa i Tuixén (29) ⚠️ | Josa i Tuixén › Alt Urgell | 4 |
| Forêt de Josa i Tuixén (37) ⚠️ | Josa i Tuixén › Alt Urgell | 4 |
| Forêt de Camarasa (33) ⚠️ | Camarasa › Noguera | 4 |
| Forêt de Camarasa (38) ⚠️ | Camarasa › Noguera | 4 |
| Forêt de Tremp (82) ⚠️ | Tremp › Pallars Jussà | 4 |
| Forêt de Navès (191) ⚠️ | Navès › Solsonès | 4 |
| Forêt de Navès (194) ⚠️ | Navès › Solsonès | 4 |
| Forêt de Castell de Mur (12) ⚠️ | Castell de Mur › Pallars Jussà | 4 |
| Forêt de Sant Esteve de la Sarga (18) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 4 |
| Forêt de Clariana de Cardener (193) ⚠️ | Clariana de Cardener › Solsonès | 4 |
| Forêt de Clariana de Cardener (227) ⚠️ | Clariana de Cardener › Solsonès | 4 |
| Forêt de Llobera (492) ⚠️ | Llobera › Solsonès | 4 |
| Forêt de Camarasa (42) ⚠️ | Camarasa › Noguera | 4 |
| Forêt de Àger (75) ⚠️ | Àger › Noguera | 4 |
| Forêt de Àger (87) ⚠️ | Àger › Noguera | 4 |
| Forêt de Àger (89) ⚠️ | Àger › Noguera | 4 |
| Forêt de Àger (94) ⚠️ | Àger › Noguera | 4 |
| Forêt de Àger (113) ⚠️ | Àger › Noguera | 4 |
| Forêt de Àger (126) ⚠️ | Àger › Noguera | 4 |
| Forêt de Àger (157) ⚠️ | Àger › Noguera | 4 |
| Forêt de Os de Balaguer (31) ⚠️ | Os de Balaguer › Noguera | 4 |
| Forêt de Os de Balaguer (87) ⚠️ | Os de Balaguer › Noguera | 4 |
| Forêt de Abella de la Conca (41) ⚠️ | Abella de la Conca › Pallars Jussà | 4 |
| Forêt de Abella de la Conca (45) ⚠️ | Abella de la Conca › Pallars Jussà | 4 |
| Forêt de Abella de la Conca (55) ⚠️ | Abella de la Conca › Pallars Jussà | 4 |
| Forêt de Baix Pallars (68) ⚠️ | Baix Pallars › Pallars Sobirà | 4 |
| Forêt de Conca de Dalt (42) ⚠️ | Conca de Dalt › Pallars Jussà | 4 |
| Forêt de Àger (187) ⚠️ | Àger › Noguera | 4 |
| Forêt de Tremp (122) ⚠️ | Tremp › Pallars Jussà | 4 |
| Forêt de la Vall de Boí (269) ⚠️ | la Vall de Boí › Alta Ribagorça | 4 |
| Forêt de Llobera (499) ⚠️ | Llobera › Solsonès | 4 |
| Forêt de Castellar de la Ribera (29) ⚠️ | Castellar de la Ribera › Solsonès | 4 |
| Forêt de Talarn (8) ⚠️ | Talarn › Pallars Jussà | 4 |
| Forêt de Tírvia (4) ⚠️ | Tírvia › Pallars Sobirà | 4 |
| Forêt de Alins (81) ⚠️ | Alins › Pallars Sobirà | 4 |
| Forêt de Alins (82) ⚠️ | Alins › Pallars Sobirà | 4 |
| Forêt de Alins (95) ⚠️ | Alins › Pallars Sobirà | 4 |
| Forêt de Llobera (512) ⚠️ | Llobera › Solsonès | 4 |
| Forêt de Alins (112) ⚠️ | Alins › Pallars Sobirà | 4 |
| Forêt de Naut Aran (149) ⚠️ | Naut Aran › Val d'Aran | 4 |
| Forêt de Naut Aran (151) ⚠️ | Naut Aran › Val d'Aran | 4 |
| Forêt de Vielha e Mijaran (84) ⚠️ | Vielha e Mijaran › Val d'Aran | 4 |
| Forêt de Vielha e Mijaran (85) ⚠️ | Vielha e Mijaran › Val d'Aran | 4 |
| Forêt de Espot (54) ⚠️ | Espot › Pallars Sobirà | 4 |
| Forêt de les Valls de Valira (135) ⚠️ | les Valls de Valira › Alt Urgell | 4 |
| Forêt de Farrera (30) ⚠️ | Farrera › Pallars Sobirà | 4 |
| Forêt de la Granja d'Escarp (13) ⚠️ | la Granja d'Escarp › Segrià | 4 |
| Forêt de les Valls de Valira (139) ⚠️ | les Valls de Valira › Alt Urgell | 4 |
| Forêt de les Valls de Valira (142) ⚠️ | les Valls de Valira › Alt Urgell | 4 |
| Forêt de Arsèguel (19) ⚠️ | el Pont de Bar › Alt Urgell | 4 |
| Forêt de el Pont de Bar (56) ⚠️ | el Pont de Bar › Alt Urgell | 4 |
| Forêt de Alàs i Cerc (25) ⚠️ | Alàs i Cerc › Alt Urgell | 4 |
| Forêt de Riner (166) ⚠️ | Riner › Solsonès | 4 |
| Forêt de Conca de Dalt (53) ⚠️ | Conca de Dalt › Pallars Jussà | 4 |
| Forêt de Sort (28) ⚠️ | Sort › Pallars Sobirà | 4 |
| Plaça de Joan Oro ⚠️ | Lleida › Segrià | 3 |
| Forêt de Vilaller (3) ⚠️ | Vilaller › Alta Ribagorça | 3 |
| Forêt de la Granja d'Escarp ⚠️ | la Granja d'Escarp › Segrià | 3 |
| Forêt de Lladurs (2) ⚠️ | Lladurs › Solsonès | 3 |
| Forêt de Lladurs (7) ⚠️ | Lladurs › Solsonès | 3 |
| Forêt de Gimenells i el Pla de la Font (2) ⚠️ | Gimenells i el Pla de la Font › Segrià | 3 |
| Forêt de Montferrer i Castellbò (4) ⚠️ | Montferrer i Castellbò › Alt Urgell | 3 |
| Forêt de Espot (2) ⚠️ | Espot › Pallars Sobirà | 3 |
| Forêt de Almatret ⚠️ | Almatret › Segrià | 3 |
| Forêt de Artesa de Segre (12) ⚠️ | Artesa de Segre › Noguera | 3 |
| Bois de els Omells de na Gaia (5) ⚠️ | els Omells de na Gaia › Urgell | 3 |
| Forêt de Lleida (6) ⚠️ | Lleida › Segrià | 3 |
| Bois de els Plans de Sió (14) ⚠️ | els Plans de Sió › Segarra | 3 |
| Forêt de la Coma i la Pedra (38) ⚠️ | la Coma i la Pedra › Solsonès | 3 |
| Forêt de la Coma i la Pedra (43) ⚠️ | la Coma i la Pedra › Solsonès | 3 |
| Forêt de la Coma i la Pedra (51) ⚠️ | la Coma i la Pedra › Solsonès | 3 |
| Forêt de la Coma i la Pedra (68) ⚠️ | la Coma i la Pedra › Solsonès | 3 |
| Forêt de la Coma i la Pedra (75) ⚠️ | la Coma i la Pedra › Solsonès | 3 |
| Bois de Gimenells i el Pla de la Font (26) ⚠️ | Gimenells i el Pla de la Font › Segrià | 3 |
| Bois de Gimenells i el Pla de la Font (27) ⚠️ | Gimenells i el Pla de la Font › Segrià | 3 |
| Bois de Gimenells i el Pla de la Font (52) ⚠️ | Gimenells i el Pla de la Font › Segrià | 3 |
| Forêt de la Vall de Boí (11) ⚠️ | la Vall de Boí › Alta Ribagorça | 3 |
| Forêt de Naut Aran (5) ⚠️ | Naut Aran › Val d'Aran | 3 |
| Forêt de Espot (21) ⚠️ | Espot › Pallars Sobirà | 3 |
| Bois de Torrefeta i Florejacs (10) ⚠️ | Torrefeta i Florejacs › Segarra | 3 |
| Arborètum ⚠️ | Lleida › Segrià | 3 |
| Forêt de el Pont de Suert (23) ⚠️ | el Pont de Suert › Alta Ribagorça | 3 |
| Forêt de Artesa de Segre (19) ⚠️ | Artesa de Segre › Noguera | 3 |
| Forêt de Olius (19) ⚠️ | Olius › Solsonès | 3 |
| Bois de Cervera (6) ⚠️ | Cervera › Segarra | 3 |
| Forêt de Naut Aran (14) ⚠️ | Naut Aran › Val d'Aran | 3 |
| Forêt de Alt Àneu (11) ⚠️ | Alt Àneu › Pallars Sobirà | 3 |
| Forêt de Alt Àneu (17) ⚠️ | Alt Àneu › Pallars Sobirà | 3 |
| Forêt de Alt Àneu (21) ⚠️ | Alt Àneu › Pallars Sobirà | 3 |
| Forêt de Vielha e Mijaran (4) ⚠️ | Vielha e Mijaran › Val d'Aran | 3 |
| Forêt de Tremp (51) ⚠️ | Tremp › Pallars Jussà | 3 |
| Forêt de Olius (24) ⚠️ | Olius › Solsonès | 3 |
| Forêt de Bellver de Cerdanya (8) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 3 |
| Forêt de Mollerussa (2) ⚠️ | Mollerussa › Pla d'Urgell | 3 |
| Bois de Rialp ⚠️ | Rialp › Pallars Sobirà | 3 |
| Forêt de Aitona (9) ⚠️ | Aitona › Segrià | 3 |
| Parc de l'Ermita de Montalbà ⚠️ | Preixana › Urgell | 3 |
| Forêt de Isona i Conca Dellà (24) ⚠️ | Isona i Conca Dellà › Pallars Jussà | 3 |
| Bois de Sant Martí de Riucorb (2) ⚠️ | Sant Martí de Riucorb › Urgell | 3 |
| Bois de Sant Martí de Riucorb (8) ⚠️ | Sant Martí de Riucorb › Urgell | 3 |
| Forêt de Montferrer i Castellbò (24) ⚠️ | Montferrer i Castellbò › Alt Urgell | 3 |
| Forêt de Montferrer i Castellbò (25) ⚠️ | Montferrer i Castellbò › Alt Urgell | 3 |
| Forêt de Golmés ⚠️ | Golmés › Pla d'Urgell | 3 |
| Forêt de Guixers (13) ⚠️ | Guixers › Solsonès | 3 |
| Forêt de Guixers (14) ⚠️ | Guixers › Solsonès | 3 |
| Bois de Vallbona de les Monges (9) ⚠️ | Vallbona de les Monges › Urgell | 3 |
| Forêt de la Vansa i Fórnols (18) ⚠️ | la Vansa i Fórnols › Alt Urgell | 3 |
| Forêt de Lladurs (93) ⚠️ | Lladurs › Solsonès | 3 |
| Forêt de Olius (58) ⚠️ | Olius › Solsonès | 3 |
| Forêt de Lladurs (118) ⚠️ | Lladurs › Solsonès | 3 |
| Forêt de Lladurs (164) ⚠️ | Lladurs › Solsonès | 3 |
| Forêt de Olius (84) ⚠️ | Olius › Solsonès | 3 |
| Forêt de Olius (89) ⚠️ | Olius › Solsonès | 3 |
| Forêt de Olius (118) ⚠️ | Olius › Solsonès | 3 |
| Forêt de Olius (165) ⚠️ | Olius › Solsonès | 3 |
| Forêt de la Pobla de Cérvoles (19) ⚠️ | la Pobla de Cérvoles › Garrigues | 3 |
| Forêt de Olius (238) ⚠️ | Olius › Solsonès | 3 |
| Forêt de Olius (244) ⚠️ | Olius › Solsonès | 3 |
| Forêt de Navès (21) ⚠️ | Navès › Solsonès | 3 |
| Forêt de Àger (9) ⚠️ | Àger › Noguera | 3 |
| Forêt de Àger (10) ⚠️ | Àger › Noguera | 3 |
| Forêt de Camarasa (10) ⚠️ | Camarasa › Noguera | 3 |
| Forêt de Llobera (83) ⚠️ | Llobera › Solsonès | 3 |
| Forêt de Abella de la Conca (7) ⚠️ | Abella de la Conca › Pallars Jussà | 3 |
| Forêt de Coll de Nargó (28) ⚠️ | Coll de Nargó › Alt Urgell | 3 |
| Forêt de Coll de Nargó (29) ⚠️ | Coll de Nargó › Alt Urgell | 3 |
| Forêt de Llobera (114) ⚠️ | Llobera › Solsonès | 3 |
| Forêt de Tremp (61) ⚠️ | Tremp › Pallars Jussà | 3 |
| Forêt de Tremp (66) ⚠️ | Tremp › Pallars Jussà | 3 |
| Forêt de Tremp (69) ⚠️ | Tremp › Pallars Jussà | 3 |
| Bois de la Torre de Cabdella (14) ⚠️ | la Torre de Cabdella › Pallars Jussà | 3 |
| Bois de la Torre de Cabdella (15) ⚠️ | la Torre de Cabdella › Pallars Jussà | 3 |
| Bois de la Torre de Cabdella (18) ⚠️ | la Torre de Cabdella › Pallars Jussà | 3 |
| Bois de la Torre de Cabdella (41) ⚠️ | la Torre de Cabdella › Pallars Jussà | 3 |
| Bois de la Seu d'Urgell ⚠️ | la Seu d'Urgell › Alt Urgell | 3 |
| Bois de les Valls de Valira (6) ⚠️ | les Valls de Valira › Alt Urgell | 3 |
| Forêt de Llobera (301) ⚠️ | Llobera › Solsonès | 3 |
| Forêt de Clariana de Cardener (97) ⚠️ | Clariana de Cardener › Solsonès | 3 |
| Forêt de Riner (4) ⚠️ | Riner › Solsonès | 3 |
| Forêt de Clariana de Cardener (120) ⚠️ | Clariana de Cardener › Solsonès | 3 |
| Forêt de Clariana de Cardener (123) ⚠️ | Clariana de Cardener › Solsonès | 3 |
| Forêt de Clariana de Cardener (130) ⚠️ | Clariana de Cardener › Solsonès | 3 |
| Forêt de Farrera (4) ⚠️ | Farrera › Pallars Sobirà | 3 |
| Forêt de Vall de Cardós (24) ⚠️ | Vall de Cardós › Pallars Sobirà | 3 |
| Forêt de Vall de Cardós (37) ⚠️ | Vall de Cardós › Pallars Sobirà | 3 |
| Forêt de Vall de Cardós (40) ⚠️ | Vall de Cardós › Pallars Sobirà | 3 |
| Forêt de Vall de Cardós (45) ⚠️ | Vall de Cardós › Pallars Sobirà | 3 |
| Forêt de Vall de Cardós (46) ⚠️ | Vall de Cardós › Pallars Sobirà | 3 |
| Forêt de Riner (120) ⚠️ | Riner › Solsonès | 3 |
| Forêt de Odèn (34) ⚠️ | Odèn › Solsonès | 3 |
| Forêt de Odèn (35) ⚠️ | Odèn › Solsonès | 3 |
| Forêt de Foradada (5) ⚠️ | Foradada › Noguera | 3 |
| Forêt de Castell de Mur (6) ⚠️ | Castell de Mur › Pallars Jussà | 3 |
| Forêt de Isona i Conca Dellà (28) ⚠️ | Isona i Conca Dellà › Pallars Jussà | 3 |
| Forêt de Tremp (76) ⚠️ | Tremp › Pallars Jussà | 3 |
| Forêt de Vielha e Mijaran (17) ⚠️ | Vielha e Mijaran › Val d'Aran | 3 |
| Forêt de Vielha e Mijaran (25) ⚠️ | Vielha e Mijaran › Val d'Aran | 3 |
| Forêt de Vielha e Mijaran (42) ⚠️ | Vielha e Mijaran › Val d'Aran | 3 |
| Forêt de Naut Aran (53) ⚠️ | Naut Aran › Val d'Aran | 3 |
| Forêt de la Guingueta d'Àneu (26) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 3 |
| Forêt de Alt Àneu (43) ⚠️ | Alt Àneu › Pallars Sobirà | 3 |
| Forêt de Cabó (10) ⚠️ | Cabó › Alt Urgell | 3 |
| Forêt de Coll de Nargó (35) ⚠️ | Coll de Nargó › Alt Urgell | 3 |
| Forêt de les Valls de Valira (21) ⚠️ | les Valls de Valira › Alt Urgell | 3 |
| Forêt de Àger (21) ⚠️ | Àger › Noguera | 3 |
| Forêt de Camarasa (14) ⚠️ | Camarasa › Noguera | 3 |
| Forêt de Camarasa (17) ⚠️ | Camarasa › Noguera | 3 |
| Forêt de Clariana de Cardener (159) ⚠️ | Clariana de Cardener › Solsonès | 3 |
| Forêt de Clariana de Cardener (160) ⚠️ | Clariana de Cardener › Solsonès | 3 |
| Forêt de Torà (13) ⚠️ | Torà › Solsonès | 3 |
| Forêt de Riu de Cerdanya (3) ⚠️ | Riu de Cerdanya › Cerdanya (Lérida) | 3 |
| Forêt de Balaguer (5) ⚠️ | Balaguer › Noguera | 3 |
| Forêt de Camarasa (23) ⚠️ | Camarasa › Noguera | 3 |
| Forêt de les Valls de Valira (22) ⚠️ | les Valls de Valira › Alt Urgell | 3 |
| Forêt de Guixers (40) ⚠️ | Guixers › Solsonès | 3 |
| Forêt de la Pobla de Segur (11) ⚠️ | la Pobla de Segur › Pallars Jussà | 3 |
| Forêt de Navès (48) ⚠️ | Navès › Solsonès | 3 |
| Forêt de Navès (50) ⚠️ | Navès › Solsonès | 3 |
| Forêt de Navès (52) ⚠️ | Navès › Solsonès | 3 |
| Forêt de Montellà i Martinet (7) ⚠️ | Montellà i Martinet › Cerdanya (Lérida) | 3 |
| Forêt de Navès (64) ⚠️ | Navès › Solsonès | 3 |
| Forêt de Olius (316) ⚠️ | Olius › Solsonès | 3 |
| Forêt de Naut Aran (65) ⚠️ | Naut Aran › Val d'Aran | 3 |
| Forêt de Bassella (11) ⚠️ | Bassella › Alt Urgell | 3 |
| Forêt de Castellar de la Ribera (22) ⚠️ | Castellar de la Ribera › Solsonès | 3 |
| Forêt de Solsona (134) ⚠️ | Solsona › Solsonès | 3 |
| Forêt de Riner (136) ⚠️ | Riner › Solsonès | 3 |
| Forêt de Es Bòrdes (8) ⚠️ | Es Bòrdes › Val d'Aran | 3 |
| Forêt de Ribera d'Urgellet (34) ⚠️ | Ribera d'Urgellet › Alt Urgell | 3 |
| Forêt de la Molsosa (26) ⚠️ | la Molsosa › Solsonès | 3 |
| Forêt de la Molsosa (31) ⚠️ | la Molsosa › Solsonès | 3 |
| Forêt de la Molsosa (34) ⚠️ | la Molsosa › Solsonès | 3 |
| Forêt de Navès (87) ⚠️ | Navès › Solsonès | 3 |
| Forêt de Navès (95) ⚠️ | Navès › Solsonès | 3 |
| Forêt de Navès (105) ⚠️ | Navès › Solsonès | 3 |
| Forêt de Navès (106) ⚠️ | Navès › Solsonès | 3 |
| Forêt de Coll de Nargó (74) ⚠️ | Coll de Nargó › Alt Urgell | 3 |
| Forêt de Coll de Nargó (75) ⚠️ | Coll de Nargó › Alt Urgell | 3 |
| Forêt de Coll de Nargó (79) ⚠️ | Coll de Nargó › Alt Urgell | 3 |
| Forêt de Odèn (37) ⚠️ | Odèn › Solsonès | 3 |
| Forêt de Guixers (52) ⚠️ | Guixers › Solsonès | 3 |
| Forêt de Sant Llorenç de Morunys (21) ⚠️ | Sant Llorenç de Morunys › Solsonès | 3 |
| Bois de la Torre de Cabdella (43) ⚠️ | la Torre de Cabdella › Pallars Jussà | 3 |
| Forêt de Soses (2) ⚠️ | Soses › Segrià | 3 |
| Forêt de Lladurs (175) ⚠️ | Lladurs › Solsonès | 3 |
| Forêt de Navès (125) ⚠️ | Navès › Solsonès | 3 |
| Forêt de Sort (17) ⚠️ | Sort › Pallars Sobirà | 3 |
| Forêt de Pinós (48) ⚠️ | Pinós › Solsonès | 3 |
| Forêt de la Molsosa (44) ⚠️ | la Molsosa › Solsonès | 3 |
| Forêt de la Molsosa (47) ⚠️ | la Molsosa › Solsonès | 3 |
| Forêt de la Molsosa (52) ⚠️ | la Molsosa › Solsonès | 3 |
| Forêt de la Molsosa (65) ⚠️ | la Molsosa › Solsonès | 3 |
| Forêt de la Molsosa (76) ⚠️ | la Molsosa › Solsonès | 3 |
| Forêt de la Molsosa (77) ⚠️ | la Molsosa › Solsonès | 3 |
| Forêt de Llavorsí (21) ⚠️ | Llavorsí › Pallars Sobirà | 3 |
| Forêt de la Guingueta d'Àneu (46) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 3 |
| Forêt de la Guingueta d'Àneu (64) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 3 |
| Forêt de la Guingueta d'Àneu (65) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 3 |
| Forêt de la Guingueta d'Àneu (74) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 3 |
| Forêt de Soriguera (31) ⚠️ | Soriguera › Pallars Sobirà | 3 |
| Forêt de Riu de Cerdanya (5) ⚠️ | Riu de Cerdanya › Cerdanya (Lérida) | 3 |
| Forêt de Vielha e Mijaran (56) ⚠️ | Vielha e Mijaran › Val d'Aran | 3 |
| Forêt de Alt Àneu (64) ⚠️ | Alt Àneu › Pallars Sobirà | 3 |
| Forêt de Gósol (23) ⚠️ | Gósol › Berguedà (Lérida) | 3 |
| Forêt de Alins (44) ⚠️ | Alins › Pallars Sobirà | 3 |
| Forêt de Esterri de Cardós (4) ⚠️ | Esterri de Cardós › Pallars Sobirà | 3 |
| Forêt de la Coma i la Pedra (121) ⚠️ | la Coma i la Pedra › Solsonès | 3 |
| Forêt de Pinós (112) ⚠️ | Pinós › Solsonès | 3 |
| Forêt de Pinós (117) ⚠️ | Pinós › Solsonès | 3 |
| Forêt de Pinós (123) ⚠️ | Pinós › Solsonès | 3 |
| Forêt de Riner (145) ⚠️ | Riner › Solsonès | 3 |
| Forêt de Riner (153) ⚠️ | Riner › Solsonès | 3 |
| Forêt de Riner (154) ⚠️ | Pinós › Solsonès | 3 |
| Forêt de Pinós (157) ⚠️ | Pinós › Solsonès | 3 |
| Forêt de Riu de Cerdanya (7) ⚠️ | Riu de Cerdanya › Cerdanya (Lérida) | 3 |
| Forêt de Montellà i Martinet (31) ⚠️ | Montellà i Martinet › Cerdanya (Lérida) | 3 |
| Forêt de Navès (147) ⚠️ | Navès › Solsonès | 3 |
| Forêt de Guixers (68) ⚠️ | Guixers › Solsonès | 3 |
| Forêt de Guixers (73) ⚠️ | Guixers › Solsonès | 3 |
| Forêt de Guixers (74) ⚠️ | Guixers › Solsonès | 3 |
| Forêt de Guixers (85) ⚠️ | Guixers › Solsonès | 3 |
| Forêt de Guixers (90) ⚠️ | Guixers › Solsonès | 3 |
| Forêt de Gósol (37) ⚠️ | Gósol › Berguedà (Lérida) | 3 |
| Forêt de Gósol (57) ⚠️ | Gósol › Berguedà (Lérida) | 3 |
| Forêt de la Coma i la Pedra (170) ⚠️ | la Coma i la Pedra › Solsonès | 3 |
| Forêt de Gósol (92) ⚠️ | Gósol › Berguedà (Lérida) | 3 |
| Forêt de la Coma i la Pedra (172) ⚠️ | la Coma i la Pedra › Solsonès | 3 |
| Forêt de Gósol (102) ⚠️ | Gósol › Berguedà (Lérida) | 3 |
| Forêt de Guixers (124) ⚠️ | Guixers › Solsonès | 3 |
| Forêt de Odèn (60) ⚠️ | Odèn › Solsonès | 3 |
| Forêt de Guixers (136) ⚠️ | Guixers › Solsonès | 3 |
| Forêt de Odèn (71) ⚠️ | Odèn › Solsonès | 3 |
| Forêt de Odèn (72) ⚠️ | Odèn › Solsonès | 3 |
| Forêt de Odèn (73) ⚠️ | Odèn › Solsonès | 3 |
| Forêt de Odèn (80) ⚠️ | Odèn › Solsonès | 3 |
| Forêt de Odèn (92) ⚠️ | Odèn › Solsonès | 3 |
| Forêt de Guixers (150) ⚠️ | Guixers › Solsonès | 3 |
| Forêt de Lladurs (194) ⚠️ | Lladurs › Solsonès | 3 |
| Forêt de Odèn (104) ⚠️ | Odèn › Solsonès | 3 |
| Forêt de Odèn (117) ⚠️ | Odèn › Solsonès | 3 |
| Forêt de Lladurs (220) ⚠️ | Lladurs › Solsonès | 3 |
| Forêt de Odèn (130) ⚠️ | Odèn › Solsonès | 3 |
| Forêt de Bellver de Cerdanya (48) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 3 |
| Forêt de Montellà i Martinet (38) ⚠️ | Montellà i Martinet › Cerdanya (Lérida) | 3 |
| Forêt de Naut Aran (69) ⚠️ | Naut Aran › Val d'Aran | 3 |
| Forêt de Naut Aran (85) ⚠️ | Naut Aran › Val d'Aran | 3 |
| Forêt de Alt Àneu (67) ⚠️ | Alt Àneu › Pallars Sobirà | 3 |
| Forêt de Alt Àneu (73) ⚠️ | Alt Àneu › Pallars Sobirà | 3 |
| Forêt de Alt Àneu (111) ⚠️ | Alt Àneu › Pallars Sobirà | 3 |
| Forêt de Alt Àneu (128) ⚠️ | Alt Àneu › Pallars Sobirà | 3 |
| Forêt de Alt Àneu (135) ⚠️ | Alt Àneu › Pallars Sobirà | 3 |
| Forêt de Alt Àneu (146) ⚠️ | Alt Àneu › Pallars Sobirà | 3 |
| Forêt de Alt Àneu (147) ⚠️ | Alt Àneu › Pallars Sobirà | 3 |
| Forêt de Naut Aran (112) ⚠️ | Naut Aran › Val d'Aran | 3 |
| Forêt de Canejan (13) ⚠️ | Canejan › Val d'Aran | 3 |
| Forêt de Canejan (21) ⚠️ | Canejan › Val d'Aran | 3 |
| Forêt de Naut Aran (132) ⚠️ | Naut Aran › Val d'Aran | 3 |
| Forêt de Naut Aran (133) ⚠️ | Naut Aran › Val d'Aran | 3 |
| Forêt de Naut Aran (139) ⚠️ | Naut Aran › Val d'Aran | 3 |
| Forêt de Alt Àneu (153) ⚠️ | Alt Àneu › Pallars Sobirà | 3 |
| Forêt de Lladorre (28) ⚠️ | Lladorre › Pallars Sobirà | 3 |
| Forêt de Lladorre (29) ⚠️ | Lladorre › Pallars Sobirà | 3 |
| Forêt de Lladorre (38) ⚠️ | Lladorre › Pallars Sobirà | 3 |
| Forêt de Llavorsí (37) ⚠️ | Llavorsí › Pallars Sobirà | 3 |
| Forêt de Llavorsí (40) ⚠️ | Llavorsí › Pallars Sobirà | 3 |
| Forêt de Llavorsí (50) ⚠️ | Llavorsí › Pallars Sobirà | 3 |
| Forêt de Rialp (20) ⚠️ | Rialp › Pallars Sobirà | 3 |
| Forêt de Vielha e Mijaran (78) ⚠️ | Vielha e Mijaran › Val d'Aran | 3 |
| Forêt de Vielha e Mijaran (80) ⚠️ | Vielha e Mijaran › Val d'Aran | 3 |
| Forêt de les Valls de Valira (39) ⚠️ | les Valls de Valira › Alt Urgell | 3 |
| Forêt de Alins (59) ⚠️ | Alins › Pallars Sobirà | 3 |
| Forêt de Vilaller (38) ⚠️ | Vilaller › Alta Ribagorça | 3 |
| Forêt de Vilaller (57) ⚠️ | Vilaller › Alta Ribagorça | 3 |
| Forêt de Vilaller (63) ⚠️ | Vilaller › Alta Ribagorça | 3 |
| Forêt de Vilaller (70) ⚠️ | Vilaller › Alta Ribagorça | 3 |
| Forêt de Coll de Nargó (86) ⚠️ | Coll de Nargó › Alt Urgell | 3 |
| Forêt de Bellver de Cerdanya (61) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 3 |
| Forêt de Estamariu (4) ⚠️ | Estamariu › Alt Urgell | 3 |
| Forêt de Arsèguel (5) ⚠️ | Arsèguel › Alt Urgell | 3 |
| Forêt de Estamariu (7) ⚠️ | Estamariu › Alt Urgell | 3 |
| Forêt de la Seu d'Urgell (8) ⚠️ | la Seu d'Urgell › Alt Urgell | 3 |
| Forêt de la Seu d'Urgell (10) ⚠️ | Alàs i Cerc › Alt Urgell | 3 |
| Forêt de les Valls de Valira (72) ⚠️ | les Valls de Valira › Alt Urgell | 3 |
| Forêt de les Valls de Valira (87) ⚠️ | les Valls de Valira › Alt Urgell | 3 |
| Forêt de les Valls de Valira (92) ⚠️ | les Valls de Valira › Alt Urgell | 3 |
| Forêt de les Valls de Valira (96) ⚠️ | les Valls de Valira › Alt Urgell | 3 |
| Forêt de les Valls de Valira (108) ⚠️ | les Valls de Valira › Alt Urgell | 3 |
| Forêt de les Valls de Valira (119) ⚠️ | les Valls de Valira › Alt Urgell | 3 |
| Forêt de Oliana (11) ⚠️ | Oliana › Alt Urgell | 3 |
| Forêt de Oliana (25) ⚠️ | Oliana › Alt Urgell | 3 |
| Forêt de Cabó (20) ⚠️ | Cabó › Alt Urgell | 3 |
| Forêt de Cabó (45) ⚠️ | Cabó › Alt Urgell | 3 |
| Forêt de la Baronia de Rialb (53) ⚠️ | la Baronia de Rialb › Noguera | 3 |
| Forêt de Ponts (6) ⚠️ | Ponts › Noguera | 3 |
| Forêt de la Baronia de Rialb (54) ⚠️ | la Baronia de Rialb › Noguera | 3 |
| Forêt de Ponts (7) ⚠️ | Ponts › Noguera | 3 |
| Forêt de Ponts (12) ⚠️ | Ponts › Noguera | 3 |
| Forêt de Bassella (25) ⚠️ | Peramola › Alt Urgell | 3 |
| Forêt de Bassella (31) ⚠️ | Bassella › Alt Urgell | 3 |
| Forêt de Bassella (32) ⚠️ | Bassella › Alt Urgell | 3 |
| Forêt de la Vansa i Fórnols (24) ⚠️ | la Vansa i Fórnols › Alt Urgell | 3 |
| Forêt de la Vansa i Fórnols (26) ⚠️ | la Vansa i Fórnols › Alt Urgell | 3 |
| Forêt de Montellà i Martinet (43) ⚠️ | Montellà i Martinet › Cerdanya (Lérida) | 3 |
| Forêt de Riu de Cerdanya (22) ⚠️ | Riu de Cerdanya › Cerdanya (Lérida) | 3 |
| Forêt de Josa i Tuixén (58) ⚠️ | Josa i Tuixén › Alt Urgell | 3 |
| Forêt de Josa i Tuixén (60) ⚠️ | Josa i Tuixén › Alt Urgell | 3 |
| Forêt de Camarasa (36) ⚠️ | Camarasa › Noguera | 3 |
| Forêt de Tremp (91) ⚠️ | Tremp › Pallars Jussà | 3 |
| Forêt de Olius (330) ⚠️ | Olius › Solsonès | 3 |
| Forêt de Navès (195) ⚠️ | Navès › Solsonès | 3 |
| Forêt de Bellver de Cerdanya (76) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 3 |
| Forêt de Bellver de Cerdanya (78) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 3 |
| Forêt de Peramola (30) ⚠️ | Peramola › Alt Urgell | 3 |
| Forêt de Tremp (93) ⚠️ | Tremp › Pallars Jussà | 3 |
| Forêt de Lladorre (45) ⚠️ | Lladorre › Pallars Sobirà | 3 |
| Forêt de Castell de Mur (14) ⚠️ | Castell de Mur › Pallars Jussà | 3 |
| Forêt de Àger (43) ⚠️ | Àger › Noguera | 3 |
| Forêt de Àger (49) ⚠️ | Àger › Noguera | 3 |
| Forêt de Sant Esteve de la Sarga (21) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 3 |
| Forêt de Sant Esteve de la Sarga (24) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 3 |
| Forêt de Sant Esteve de la Sarga (27) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 3 |
| Forêt de Àger (57) ⚠️ | Àger › Noguera | 3 |
| Forêt de Àger (59) ⚠️ | Àger › Noguera | 3 |
| Forêt de Soriguera (42) ⚠️ | Soriguera › Pallars Sobirà | 3 |
| Forêt de Soriguera (43) ⚠️ | Soriguera › Pallars Sobirà | 3 |
| Forêt de Baix Pallars (65) ⚠️ | Baix Pallars › Pallars Sobirà | 3 |
| Forêt de Clariana de Cardener (177) ⚠️ | Clariana de Cardener › Solsonès | 3 |
| Forêt de Clariana de Cardener (182) ⚠️ | Clariana de Cardener › Solsonès | 3 |
| Forêt de Clariana de Cardener (225) ⚠️ | Clariana de Cardener › Solsonès | 3 |
| Forêt de Pinós (164) ⚠️ | Pinós › Solsonès | 3 |
| Forêt de Castell de Mur (21) ⚠️ | Castell de Mur › Pallars Jussà | 3 |
| Forêt de Àger (60) ⚠️ | Àger › Noguera | 3 |
| Forêt de Castell de Mur (27) ⚠️ | Castell de Mur › Pallars Jussà | 3 |
| Forêt de Àger (64) ⚠️ | Àger › Noguera | 3 |
| Forêt de Camarasa (43) ⚠️ | Camarasa › Noguera | 3 |
| Forêt de Sant Esteve de la Sarga (39) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 3 |
| Forêt de Sant Esteve de la Sarga (42) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 3 |
| Forêt de Sant Esteve de la Sarga (55) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 3 |
| Forêt de Àger (81) ⚠️ | Àger › Noguera | 3 |
| Forêt de Àger (97) ⚠️ | Àger › Noguera | 3 |
| Forêt de Àger (117) ⚠️ | Àger › Noguera | 3 |
| Forêt de Àger (152) ⚠️ | Àger › Noguera | 3 |
| Forêt de Àger (155) ⚠️ | Àger › Noguera | 3 |
| Forêt de Àger (159) ⚠️ | Àger › Noguera | 3 |
| Forêt de Os de Balaguer (29) ⚠️ | Os de Balaguer › Noguera | 3 |
| Forêt de Os de Balaguer (52) ⚠️ | Os de Balaguer › Noguera | 3 |
| Forêt de Os de Balaguer (62) ⚠️ | Os de Balaguer › Noguera | 3 |
| Forêt de Os de Balaguer (66) ⚠️ | Os de Balaguer › Noguera | 3 |
| Forêt de Os de Balaguer (73) ⚠️ | Os de Balaguer › Noguera | 3 |
| Forêt de Os de Balaguer (77) ⚠️ | Os de Balaguer › Noguera | 3 |
| Forêt de Os de Balaguer (79) ⚠️ | Os de Balaguer › Noguera | 3 |
| Forêt de Os de Balaguer (82) ⚠️ | Os de Balaguer › Noguera | 3 |
| Forêt de Os de Balaguer (83) ⚠️ | Os de Balaguer › Noguera | 3 |
| Forêt de Coll de Nargó (108) ⚠️ | Coll de Nargó › Alt Urgell | 3 |
| Forêt de Abella de la Conca (40) ⚠️ | Abella de la Conca › Pallars Jussà | 3 |
| Forêt de Abella de la Conca (42) ⚠️ | Abella de la Conca › Pallars Jussà | 3 |
| Forêt de Abella de la Conca (43) ⚠️ | Abella de la Conca › Pallars Jussà | 3 |
| Forêt de Abella de la Conca (44) ⚠️ | Abella de la Conca › Pallars Jussà | 3 |
| Forêt de Abella de la Conca (47) ⚠️ | Abella de la Conca › Pallars Jussà | 3 |
| Forêt de Abella de la Conca (48) ⚠️ | Abella de la Conca › Pallars Jussà | 3 |
| Forêt de Abella de la Conca (60) ⚠️ | Abella de la Conca › Pallars Jussà | 3 |
| Forêt de Abella de la Conca (64) ⚠️ | Abella de la Conca › Pallars Jussà | 3 |
| Forêt de Abella de la Conca (68) ⚠️ | Abella de la Conca › Pallars Jussà | 3 |
| Forêt de Conca de Dalt (41) ⚠️ | Conca de Dalt › Pallars Jussà | 3 |
| Forêt de Tremp (109) ⚠️ | Tremp › Pallars Jussà | 3 |
| Forêt de Tremp (113) ⚠️ | Tremp › Pallars Jussà | 3 |
| Forêt de Tremp (123) ⚠️ | Tremp › Pallars Jussà | 3 |
| Forêt de el Pont de Suert (56) ⚠️ | el Pont de Suert › Alta Ribagorça | 3 |
| Forêt de el Pont de Suert (93) ⚠️ | el Pont de Suert › Alta Ribagorça | 3 |
| Forêt de el Pont de Suert (96) ⚠️ | el Pont de Suert › Alta Ribagorça | 3 |
| Forêt de el Pont de Suert (98) ⚠️ | el Pont de Suert › Alta Ribagorça | 3 |
| Bois de la Torre de Cabdella (47) ⚠️ | la Torre de Cabdella › Pallars Jussà | 3 |
| Forêt de la Vansa i Fórnols (30) ⚠️ | la Vansa i Fórnols › Alt Urgell | 3 |
| Forêt de Alins (88) ⚠️ | Alins › Pallars Sobirà | 3 |
| Forêt de Alins (97) ⚠️ | Alins › Pallars Sobirà | 3 |
| Forêt de Bellver de Cerdanya (84) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 3 |
| Forêt de Bellver de Cerdanya (85) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 3 |
| Forêt de la Guingueta d'Àneu (84) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 3 |
| Forêt de Clariana de Cardener (231) ⚠️ | Clariana de Cardener › Solsonès | 3 |
| Forêt de Vielha e Mijaran (87) ⚠️ | Vielha e Mijaran › Val d'Aran | 3 |
| Forêt de Clariana de Cardener (236) ⚠️ | Clariana de Cardener › Solsonès | 3 |
| Forêt de Espot (47) ⚠️ | Espot › Pallars Sobirà | 3 |
| Forêt de Montellà i Martinet (52) ⚠️ | Montellà i Martinet › Cerdanya (Lérida) | 3 |
| Forêt de Montellà i Martinet (54) ⚠️ | Montellà i Martinet › Cerdanya (Lérida) | 3 |
| Forêt de el Pont de Bar (27) ⚠️ | Lles de Cerdanya › Cerdanya (Lérida) | 3 |
| Forêt de la Vall de Boí (273) ⚠️ | la Vall de Boí › Alta Ribagorça | 3 |
| Forêt de Farrera (21) ⚠️ | Farrera › Pallars Sobirà | 3 |
| Forêt de la Granja d'Escarp (11) ⚠️ | la Granja d'Escarp › Segrià | 3 |
| Forêt de Almatret (20) ⚠️ | Almatret › Segrià | 3 |
| Forêt de la Granja d'Escarp (16) ⚠️ | la Granja d'Escarp › Segrià | 3 |
| Forêt de les Valls de Valira (143) ⚠️ | les Valls de Valira › Alt Urgell | 3 |
| Forêt de Montferrer i Castellbò (118) ⚠️ | Montferrer i Castellbò › Alt Urgell | 3 |
| Forêt de Salàs de Pallars (5) ⚠️ | Salàs de Pallars › Pallars Jussà | 3 |
| Forêt de Salàs de Pallars (6) ⚠️ | Salàs de Pallars › Pallars Jussà | 3 |
| Forêt de Salàs de Pallars (7) ⚠️ | Salàs de Pallars › Pallars Jussà | 3 |
| Forêt de Sort (23) ⚠️ | Sort › Pallars Sobirà | 3 |
| Forêt de Sort (24) ⚠️ | Sort › Pallars Sobirà | 3 |
| Forêt de Camarasa ⚠️ | Camarasa › Noguera | 2 |
| Forêt de Alcarràs ⚠️ | Alcarràs › Segrià | 2 |
| Parc sobre les Vies ⚠️ | Lleida › Segrià | 2 |
| Forêt de la Pobla de Cérvoles (2) ⚠️ | la Pobla de Cérvoles › Garrigues | 2 |
| Forêt de Soriguera ⚠️ | Soriguera › Pallars Sobirà | 2 |
| Bois de Guimerà ⚠️ | Guimerà › Urgell | 2 |
| Forêt de Clariana de Cardener ⚠️ | Clariana de Cardener › Solsonès | 2 |
| Forêt de Lladurs (6) ⚠️ | Lladurs › Solsonès | 2 |
| Forêt de Tremp (18) ⚠️ | Tremp › Pallars Jussà | 2 |
| Forêt de Cabó (2) ⚠️ | Cabó › Alt Urgell | 2 |
| Forêt de Gimenells i el Pla de la Font (5) ⚠️ | Gimenells i el Pla de la Font › Segrià | 2 |
| Forêt de Talavera (5) ⚠️ | Talavera › Segarra | 2 |
| Forêt de Maials (9) ⚠️ | Maials › Segrià | 2 |
| Forêt de Sanaüja (2) ⚠️ | Sanaüja › Segarra | 2 |
| Forêt de Juncosa (12) ⚠️ | Juncosa › Garrigues | 2 |
| Forêt de el Vilosell (2) ⚠️ | el Vilosell › Garrigues | 2 |
| Forêt de Olius (2) ⚠️ | Olius › Solsonès | 2 |
| Forêt de Vilaller (10) ⚠️ | Vilaller › Alta Ribagorça | 2 |
| Forêt de Peramola (2) ⚠️ | Peramola › Alt Urgell | 2 |
| Forêt de Pinell de Solsonès (28) ⚠️ | Pinell de Solsonès › Solsonès | 2 |
| Forêt de Alfarràs (3) ⚠️ | Alfarràs › Segrià | 2 |
| Forêt de la Baronia de Rialb (32) ⚠️ | la Baronia de Rialb › Noguera | 2 |
| Forêt de Fígols i Alinyà (6) ⚠️ | Fígols i Alinyà › Alt Urgell | 2 |
| Forêt de Baix Pallars (25) ⚠️ | Baix Pallars › Pallars Sobirà | 2 |
| Forêt de Maials (20) ⚠️ | Maials › Segrià | 2 |
| Forêt de Ivars de Noguera (2) ⚠️ | Alfarràs › Segrià | 2 |
| Forêt de Maials (21) ⚠️ | Maials › Segrià | 2 |
| Forêt de Sant Guim de Freixenet (8) ⚠️ | Sant Guim de Freixenet › Segarra | 2 |
| Forêt de Lleida (2) ⚠️ | Lleida › Segrià | 2 |
| Forêt de Lleida (4) ⚠️ | Lleida › Segrià | 2 |
| Forêt de Lleida (5) ⚠️ | Lleida › Segrià | 2 |
| Muntanya de Monterrós ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 2 |
| Forêt de Seròs (6) ⚠️ | Seròs › Segrià | 2 |
| Parc de la Valira ⚠️ | la Seu d'Urgell › Alt Urgell | 2 |
| Parc del Toll del Bressol ⚠️ | la Seu d'Urgell › Alt Urgell | 2 |
| Bois de Sant Guim de la Plana (2) ⚠️ | Sant Guim de la Plana › Segarra | 2 |
| Forêt de la Coma i la Pedra (21) ⚠️ | la Coma i la Pedra › Solsonès | 2 |
| Forêt de la Coma i la Pedra (50) ⚠️ | la Coma i la Pedra › Solsonès | 2 |
| Forêt de la Coma i la Pedra (59) ⚠️ | la Coma i la Pedra › Solsonès | 2 |
| Forêt de la Coma i la Pedra (66) ⚠️ | la Coma i la Pedra › Solsonès | 2 |
| Bois de Agramunt (3) ⚠️ | Agramunt › Urgell | 2 |
| Bois de Gimenells i el Pla de la Font (12) ⚠️ | Gimenells i el Pla de la Font › Segrià | 2 |
| Forêt de Gimenells i el Pla de la Font (10) ⚠️ | Gimenells i el Pla de la Font › Segrià | 2 |
| Bois de Alcarràs ⚠️ | Alcarràs › Segrià | 2 |
| Bois de Gimenells i el Pla de la Font (22) ⚠️ | Gimenells i el Pla de la Font › Segrià | 2 |
| Bois de Gimenells i el Pla de la Font (23) ⚠️ | Gimenells i el Pla de la Font › Segrià | 2 |
| Bois de Gimenells i el Pla de la Font (28) ⚠️ | Gimenells i el Pla de la Font › Segrià | 2 |
| Forêt de Gimenells i el Pla de la Font (12) ⚠️ | Gimenells i el Pla de la Font › Segrià | 2 |
| Forêt de Cervera ⚠️ | Cervera › Segarra | 2 |
| Forêt de la Coma i la Pedra (82) ⚠️ | la Coma i la Pedra › Solsonès | 2 |
| Forêt de la Vall de Boí (8) ⚠️ | la Vall de Boí › Alta Ribagorça | 2 |
| Forêt de la Vall de Boí (10) ⚠️ | la Vall de Boí › Alta Ribagorça | 2 |
| Bois de Montoliu de Segarra (2) ⚠️ | Guimerà › Urgell | 2 |
| Forêt de Naut Aran (4) ⚠️ | Naut Aran › Val d'Aran | 2 |
| Jardins de l'Alcalde Estadella ⚠️ | Lleida › Segrià | 2 |
| Forêt de Espot (10) ⚠️ | Espot › Pallars Sobirà | 2 |
| Forêt de Espot (11) ⚠️ | Espot › Pallars Sobirà | 2 |
| Forêt de Espot (12) ⚠️ | Espot › Pallars Sobirà | 2 |
| Forêt de Espot (22) ⚠️ | Espot › Pallars Sobirà | 2 |
| Forêt de les Valls de Valira (10) ⚠️ | les Valls de Valira › Alt Urgell | 2 |
| Bois de Torrefeta i Florejacs (11) ⚠️ | Torrefeta i Florejacs › Segarra | 2 |
| Forêt de Ribera d'Ondara (8) ⚠️ | Ribera d'Ondara › Segarra | 2 |
| Forêt de la Vall de Boí (13) ⚠️ | la Vall de Boí › Alta Ribagorça | 2 |
| Forêt de la Vall de Boí (15) ⚠️ | la Vall de Boí › Alta Ribagorça | 2 |
| Forêt de Tírvia ⚠️ | Tírvia › Pallars Sobirà | 2 |
| Forêt de Torres de Segre (9) ⚠️ | Torres de Segre › Segrià | 2 |
| Forêt de Sarroca de Bellera (13) ⚠️ | Sarroca de Bellera › Pallars Jussà | 2 |
| Forêt de Olius (7) ⚠️ | Solsona › Solsonès | 2 |
| Forêt de Solsona (11) ⚠️ | Solsona › Solsonès | 2 |
| Forêt de Solsona (17) ⚠️ | Solsona › Solsonès | 2 |
| Forêt de Solsona (24) ⚠️ | Solsona › Solsonès | 2 |
| Forêt de Solsona (33) ⚠️ | Solsona › Solsonès | 2 |
| Forêt de Olius (12) ⚠️ | Olius › Solsonès | 2 |
| Forêt de Olius (18) ⚠️ | Olius › Solsonès | 2 |
| Forêt de Cervera (2) ⚠️ | Cervera › Segarra | 2 |
| Forêt de Cervera (6) ⚠️ | Cervera › Segarra | 2 |
| Bois de Ribera d'Ondara (3) ⚠️ | Ribera d'Ondara › Segarra | 2 |
| Forêt de Naut Aran (7) ⚠️ | Naut Aran › Val d'Aran | 2 |
| Forêt de la Guingueta d'Àneu (11) ⚠️ | Esterri d'Àneu › Pallars Sobirà | 2 |
| Forêt de Alt Àneu (12) ⚠️ | Alt Àneu › Pallars Sobirà | 2 |
| Forêt de Alt Àneu (13) ⚠️ | Alt Àneu › Pallars Sobirà | 2 |
| Forêt de Alt Àneu (19) ⚠️ | Alt Àneu › Pallars Sobirà | 2 |
| Bois de Alcarràs (8) ⚠️ | Alcarràs › Segrià | 2 |
| Forêt de Solsona (90) ⚠️ | Solsona › Solsonès | 2 |
| Forêt de Vielha e Mijaran (3) ⚠️ | Vielha e Mijaran › Val d'Aran | 2 |
| Forêt de la Guingueta d'Àneu (13) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 2 |
| Forêt de Tremp (48) ⚠️ | Tremp › Pallars Jussà | 2 |
| Forêt de Tremp (53) ⚠️ | Tremp › Pallars Jussà | 2 |
| Forêt de Navès (6) ⚠️ | Navès › Solsonès | 2 |
| Forêt de Navès (11) ⚠️ | Navès › Solsonès | 2 |
| Forêt de Olius (23) ⚠️ | Olius › Solsonès | 2 |
| Forêt de Montoliu de Lleida ⚠️ | Montoliu de Lleida › Segrià | 2 |
| Bois de Balaguer ⚠️ | Balaguer › Noguera | 2 |
| Forêt de la Coma i la Pedra (86) ⚠️ | la Coma i la Pedra › Solsonès | 2 |
| Forêt de la Coma i la Pedra (87) ⚠️ | la Coma i la Pedra › Solsonès | 2 |
| Bois de Maials ⚠️ | Maials › Segrià | 2 |
| Forêt de Lleida (14) ⚠️ | Lleida › Segrià | 2 |
| Forêt de Guixers (11) ⚠️ | Guixers › Solsonès | 2 |
| Parc del Riu ⚠️ | Corbins › Segrià | 2 |
| Bois de Prullans ⚠️ | Prullans › Cerdanya (Lérida) | 2 |
| Bois de Tremp ⚠️ | Tremp › Pallars Jussà | 2 |
| Bois de Talavera (9) ⚠️ | Talavera › Segarra | 2 |
| Forêt de Artesa de Segre (21) ⚠️ | Artesa de Segre › Noguera | 2 |
| Bois de Ribera d'Ondara (12) ⚠️ | Ribera d'Ondara › Segarra | 2 |
| Bois de Talavera (20) ⚠️ | Talavera › Segarra | 2 |
| Forêt de la Vall de Boí (17) ⚠️ | la Vall de Boí › Alta Ribagorça | 2 |
| Bois de Talavera (22) ⚠️ | Talavera › Segarra | 2 |
| Bois de Ribera d'Ondara (25) ⚠️ | Ribera d'Ondara › Segarra | 2 |
| Bois de Talavera (39) ⚠️ | Talavera › Segarra | 2 |
| Forêt de Alt Àneu (28) ⚠️ | Alt Àneu › Pallars Sobirà | 2 |
| Forêt de Alt Àneu (29) ⚠️ | Alt Àneu › Pallars Sobirà | 2 |
| Forêt de Lladorre (6) ⚠️ | Lladorre › Pallars Sobirà | 2 |
| Forêt de Llavorsí (3) ⚠️ | Llavorsí › Pallars Sobirà | 2 |
| Forêt de Arres ⚠️ | Arres › Val d'Aran | 2 |
| Forêt de Llardecans (4) ⚠️ | Llardecans › Segrià | 2 |
| Forêt de Cabó (8) ⚠️ | Cabó › Alt Urgell | 2 |
| Forêt de Josa i Tuixén (3) ⚠️ | Josa i Tuixén › Alt Urgell | 2 |
| Forêt de Olius (41) ⚠️ | Olius › Solsonès | 2 |
| Forêt de Olius (42) ⚠️ | Olius › Solsonès | 2 |
| Forêt de Lladurs (95) ⚠️ | Lladurs › Solsonès | 2 |
| Forêt de Lladurs (99) ⚠️ | Lladurs › Solsonès | 2 |
| Forêt de Olius (43) ⚠️ | Olius › Solsonès | 2 |
| Forêt de Olius (72) ⚠️ | Olius › Solsonès | 2 |
| Forêt de Lladurs (112) ⚠️ | Lladurs › Solsonès | 2 |
| Forêt de Lladurs (133) ⚠️ | Lladurs › Solsonès | 2 |
| Forêt de Lladurs (136) ⚠️ | Lladurs › Solsonès | 2 |
| Forêt de Lladurs (147) ⚠️ | Lladurs › Solsonès | 2 |
| Forêt de Lladurs (161) ⚠️ | Lladurs › Solsonès | 2 |
| Forêt de Olius (80) ⚠️ | Olius › Solsonès | 2 |
| Forêt de Lladurs (165) ⚠️ | Lladurs › Solsonès | 2 |
| Forêt de Olius (95) ⚠️ | Olius › Solsonès | 2 |
| Forêt de Olius (96) ⚠️ | Olius › Solsonès | 2 |
| Forêt de Olius (114) ⚠️ | Olius › Solsonès | 2 |
| Forêt de Olius (135) ⚠️ | Olius › Solsonès | 2 |
| Parc Aventura, ESPORTEC ⚠️ | la Coma i la Pedra › Solsonès | 2 |
| Forêt de Olius (181) ⚠️ | Olius › Solsonès | 2 |
| Forêt de Olius (210) ⚠️ | Olius › Solsonès | 2 |
| Forêt de Riner (3) ⚠️ | Riner › Solsonès | 2 |
| Forêt de Olius (224) ⚠️ | Olius › Solsonès | 2 |
| Forêt de Olius (234) ⚠️ | Olius › Solsonès | 2 |
| Forêt de Olius (235) ⚠️ | Olius › Solsonès | 2 |
| Forêt de Olius (248) ⚠️ | Olius › Solsonès | 2 |
| Forêt de Olius (280) ⚠️ | Olius › Solsonès | 2 |
| Forêt de Olius (306) ⚠️ | Olius › Solsonès | 2 |
| Forêt de Llobera (6) ⚠️ | Llobera › Solsonès | 2 |
| Forêt de Llobera (84) ⚠️ | Llobera › Solsonès | 2 |
| Forêt de Llobera (98) ⚠️ | Llobera › Solsonès | 2 |
| Forêt de Abella de la Conca (9) ⚠️ | Abella de la Conca › Pallars Jussà | 2 |
| Forêt de Bellaguarda (5) ⚠️ | Bellaguarda › Garrigues | 2 |
| Forêt de Llobera (128) ⚠️ | Llobera › Solsonès | 2 |
| Forêt de Llobera (161) ⚠️ | Llobera › Solsonès | 2 |
| Bois de la Torre de Cabdella (9) ⚠️ | la Torre de Cabdella › Pallars Jussà | 2 |
| Bois de la Torre de Cabdella (19) ⚠️ | la Torre de Cabdella › Pallars Jussà | 2 |
| Bois de la Torre de Cabdella (23) ⚠️ | la Torre de Cabdella › Pallars Jussà | 2 |
| Bois de la Torre de Cabdella (39) ⚠️ | la Torre de Cabdella › Pallars Jussà | 2 |
| Forêt de Llobera (190) ⚠️ | Llobera › Solsonès | 2 |
| Bois de Alàs i Cerc (2) ⚠️ | Alàs i Cerc › Alt Urgell | 2 |
| Bois de la Seu d'Urgell (3) ⚠️ | la Seu d'Urgell › Alt Urgell | 2 |
| Bois de Alàs i Cerc (3) ⚠️ | Alàs i Cerc › Alt Urgell | 2 |
| Bois de Lles de Cerdanya ⚠️ | Lles de Cerdanya › Cerdanya (Lérida) | 2 |
| Forêt de Talavera (21) ⚠️ | Talavera › Segarra | 2 |
| Forêt de Llobera (300) ⚠️ | Llobera › Solsonès | 2 |
| Forêt de Llobera (333) ⚠️ | Llobera › Solsonès | 2 |
| Forêt de Llobera (378) ⚠️ | Llobera › Solsonès | 2 |
| Bois de les Valls de Valira (7) ⚠️ | les Valls de Valira › Alt Urgell | 2 |
| Forêt de Llobera (396) ⚠️ | Llobera › Solsonès | 2 |
| Forêt de Llobera (397) ⚠️ | Llobera › Solsonès | 2 |
| Forêt de Llobera (403) ⚠️ | Llobera › Solsonès | 2 |
| Forêt de Llobera (442) ⚠️ | Llobera › Solsonès | 2 |
| Forêt de Llobera (445) ⚠️ | Llobera › Solsonès | 2 |
| Forêt de Llobera (476) ⚠️ | Llobera › Solsonès | 2 |
| Forêt de Clariana de Cardener (14) ⚠️ | Clariana de Cardener › Solsonès | 2 |
| Forêt de Clariana de Cardener (112) ⚠️ | Clariana de Cardener › Solsonès | 2 |
| Forêt de Naut Aran (34) ⚠️ | Naut Aran › Val d'Aran | 2 |
| Forêt de Naut Aran (39) ⚠️ | Naut Aran › Val d'Aran | 2 |
| Forêt de Naut Aran (46) ⚠️ | Naut Aran › Val d'Aran | 2 |
| Forêt de Clariana de Cardener (126) ⚠️ | Clariana de Cardener › Solsonès | 2 |
| Forêt de Clariana de Cardener (146) ⚠️ | Clariana de Cardener › Solsonès | 2 |
| Forêt de la Vall de Boí (74) ⚠️ | la Vall de Boí › Alta Ribagorça | 2 |
| Forêt de la Vall de Boí (101) ⚠️ | la Vall de Boí › Alta Ribagorça | 2 |
| Forêt de la Vall de Boí (103) ⚠️ | la Vall de Boí › Alta Ribagorça | 2 |
| Forêt de Riner (63) ⚠️ | Riner › Solsonès | 2 |
| Forêt de la Vall de Boí (112) ⚠️ | la Vall de Boí › Alta Ribagorça | 2 |
| Forêt de Riner (71) ⚠️ | Riner › Solsonès | 2 |
| Forêt de Riner (73) ⚠️ | Riner › Solsonès | 2 |
| Forêt de Vall de Cardós (22) ⚠️ | Vall de Cardós › Pallars Sobirà | 2 |
| Forêt de Vall de Cardós (27) ⚠️ | Vall de Cardós › Pallars Sobirà | 2 |
| Forêt de Vall de Cardós (28) ⚠️ | Vall de Cardós › Pallars Sobirà | 2 |
| Forêt de Vall de Cardós (53) ⚠️ | Vall de Cardós › Pallars Sobirà | 2 |
| Jardins de Jaume Magre ⚠️ | Lleida › Segrià | 2 |
| Forêt de Vallfogona de Balaguer (2) ⚠️ | Vallfogona de Balaguer › Noguera | 2 |
| Forêt de Guixers (23) ⚠️ | Guixers › Solsonès | 2 |
| Forêt de Guixers (24) ⚠️ | Guixers › Solsonès | 2 |
| Forêt de Peramola (10) ⚠️ | Peramola › Alt Urgell | 2 |
| Forêt de Alt Àneu (38) ⚠️ | Alt Àneu › Pallars Sobirà | 2 |
| Forêt de Tremp (77) ⚠️ | Tremp › Pallars Jussà | 2 |
| Forêt de Bossòst (8) ⚠️ | Bossòst › Val d'Aran | 2 |
| Forêt de Vielha e Mijaran (20) ⚠️ | Vielha e Mijaran › Val d'Aran | 2 |
| Forêt de Vielha e Mijaran (24) ⚠️ | Vielha e Mijaran › Val d'Aran | 2 |
| Forêt de Vielha e Mijaran (32) ⚠️ | Vielha e Mijaran › Val d'Aran | 2 |
| Forêt de Vielha e Mijaran (44) ⚠️ | Vielha e Mijaran › Val d'Aran | 2 |
| Forêt de Vilaller (32) ⚠️ | Vilaller › Alta Ribagorça | 2 |
| Forêt de Montferrer i Castellbò (28) ⚠️ | Montferrer i Castellbò › Alt Urgell | 2 |
| Forêt de la Guingueta d'Àneu (20) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 2 |
| Forêt de la Guingueta d'Àneu (23) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 2 |
| Forêt de Esterri d'Àneu (7) ⚠️ | Esterri d'Àneu › Pallars Sobirà | 2 |
| Forêt de Organyà (6) ⚠️ | Organyà › Alt Urgell | 2 |
| Forêt de Organyà (11) ⚠️ | Organyà › Alt Urgell | 2 |
| Forêt de Organyà (12) ⚠️ | Organyà › Alt Urgell | 2 |
| Forêt de Organyà (15) ⚠️ | Organyà › Alt Urgell | 2 |
| Forêt de Organyà (19) ⚠️ | Organyà › Alt Urgell | 2 |
| Forêt de Coll de Nargó (37) ⚠️ | Coll de Nargó › Alt Urgell | 2 |
| Forêt de Camarasa (16) ⚠️ | Camarasa › Noguera | 2 |
| Forêt de Oliana (5) ⚠️ | Oliana › Alt Urgell | 2 |
| Forêt de Prats i Sansor (2) ⚠️ | Prats i Sansor › Cerdanya (Lérida) | 2 |
| Forêt de el Pont de Suert (41) ⚠️ | el Pont de Suert › Alta Ribagorça | 2 |
| Forêt de Àger (22) ⚠️ | Àger › Noguera | 2 |
| Forêt de Torà (15) ⚠️ | Torà › Solsonès | 2 |
| Forêt de Guixers (39) ⚠️ | Guixers › Solsonès | 2 |
| Forêt de Guixers (44) ⚠️ | Guixers › Solsonès | 2 |
| Forêt de Sant Llorenç de Morunys (18) ⚠️ | Sant Llorenç de Morunys › Solsonès | 2 |
| Forêt de Lleida (20) ⚠️ | Lleida › Segrià | 2 |
| Forêt de Baix Pallars (36) ⚠️ | Baix Pallars › Pallars Sobirà | 2 |
| Forêt de Baix Pallars (40) ⚠️ | Baix Pallars › Pallars Sobirà | 2 |
| Forêt de la Seu d'Urgell (7) ⚠️ | la Seu d'Urgell › Alt Urgell | 2 |
| Forêt de Ribera d'Urgellet (23) ⚠️ | Ribera d'Urgellet › Alt Urgell | 2 |
| Forêt de la Torre de Cabdella (22) ⚠️ | la Torre de Cabdella › Pallars Jussà | 2 |
| Forêt de Bellver de Cerdanya (19) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 2 |
| Forêt de Navès (60) ⚠️ | Navès › Solsonès | 2 |
| Forêt de Àger (29) ⚠️ | Àger › Noguera | 2 |
| Forêt de Bassella (14) ⚠️ | Bassella › Alt Urgell | 2 |
| Forêt de Bassella (18) ⚠️ | Bassella › Alt Urgell | 2 |
| Forêt de Bassella (23) ⚠️ | Bassella › Alt Urgell | 2 |
| Forêt de Bassella (24) ⚠️ | Bassella › Alt Urgell | 2 |
| Forêt de Olius (324) ⚠️ | Olius › Solsonès | 2 |
| Forêt de Riner (135) ⚠️ | Riner › Solsonès | 2 |
| Forêt de Riner (138) ⚠️ | Riner › Solsonès | 2 |
| Forêt de Riner (139) ⚠️ | Riner › Solsonès | 2 |
| Forêt de Es Bòrdes (4) ⚠️ | Es Bòrdes › Val d'Aran | 2 |
| Forêt de Es Bòrdes (7) ⚠️ | Es Bòrdes › Val d'Aran | 2 |
| Forêt de Prullans (5) ⚠️ | Montellà i Martinet › Cerdanya (Lérida) | 2 |
| Forêt de Bellver de Cerdanya (27) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 2 |
| Forêt de Fígols i Alinyà (12) ⚠️ | Fígols i Alinyà › Alt Urgell | 2 |
| Forêt de les Valls d'Aguilar (25) ⚠️ | les Valls d'Aguilar › Alt Urgell | 2 |
| Forêt de Ribera d'Urgellet (31) ⚠️ | Ribera d'Urgellet › Alt Urgell | 2 |
| Forêt de Ribera d'Urgellet (32) ⚠️ | Ribera d'Urgellet › Alt Urgell | 2 |
| Forêt de Fígols i Alinyà (21) ⚠️ | Organyà › Alt Urgell | 2 |
| Forêt de la Coma i la Pedra (102) ⚠️ | la Coma i la Pedra › Solsonès | 2 |
| Forêt de la Molsosa (28) ⚠️ | la Molsosa › Solsonès | 2 |
| Forêt de la Molsosa (36) ⚠️ | la Molsosa › Solsonès | 2 |
| Forêt de Navès (81) ⚠️ | Navès › Solsonès | 2 |
| Forêt de Navès (83) ⚠️ | Navès › Solsonès | 2 |
| Forêt de Navès (93) ⚠️ | Navès › Solsonès | 2 |
| Forêt de Navès (117) ⚠️ | Navès › Solsonès | 2 |
| Forêt de Navès (118) ⚠️ | Navès › Solsonès | 2 |
| Bois de Tremp (2) ⚠️ | Tremp › Pallars Jussà | 2 |
| Forêt de Organyà (23) ⚠️ | Organyà › Alt Urgell | 2 |
| Forêt de Organyà (24) ⚠️ | Organyà › Alt Urgell | 2 |
| Forêt de Fígols i Alinyà (25) ⚠️ | Fígols i Alinyà › Alt Urgell | 2 |
| Forêt de Coll de Nargó (62) ⚠️ | Coll de Nargó › Alt Urgell | 2 |
| Forêt de Coll de Nargó (71) ⚠️ | Coll de Nargó › Alt Urgell | 2 |
| Forêt de Sant Llorenç de Morunys (19) ⚠️ | Sant Llorenç de Morunys › Solsonès | 2 |
| Forêt de Guixers (53) ⚠️ | Guixers › Solsonès | 2 |
| Forêt de Guixers (55) ⚠️ | Guixers › Solsonès | 2 |
| Forêt de Soses ⚠️ | Soses › Segrià | 2 |
| Forêt de Lladurs (176) ⚠️ | Lladurs › Solsonès | 2 |
| Forêt de Navès (141) ⚠️ | Navès › Solsonès | 2 |
| Forêt de Guixers (59) ⚠️ | Guixers › Solsonès | 2 |
| Forêt de Sant Llorenç de Morunys (26) ⚠️ | Sant Llorenç de Morunys › Solsonès | 2 |
| Forêt de Peramola (14) ⚠️ | Peramola › Alt Urgell | 2 |
| Forêt de Navès (144) ⚠️ | Navès › Solsonès | 2 |
| Forêt de Pinós (55) ⚠️ | Pinós › Solsonès | 2 |
| Forêt de la Molsosa (45) ⚠️ | la Molsosa › Solsonès | 2 |
| Forêt de la Molsosa (55) ⚠️ | la Molsosa › Solsonès | 2 |
| Forêt de la Molsosa (61) ⚠️ | la Molsosa › Solsonès | 2 |
| Forêt de Pinós (62) ⚠️ | Pinós › Solsonès | 2 |
| Forêt de la Molsosa (73) ⚠️ | la Molsosa › Solsonès | 2 |
| Forêt de la Molsosa (75) ⚠️ | la Molsosa › Solsonès | 2 |
| Forêt de Pinós (68) ⚠️ | Pinós › Solsonès | 2 |
| Forêt de Pinós (69) ⚠️ | Pinós › Solsonès | 2 |
| Forêt de Pinós (91) ⚠️ | Pinós › Solsonès | 2 |
| Forêt de Pinós (95) ⚠️ | Pinós › Solsonès | 2 |
| Forêt de Llavorsí (10) ⚠️ | Llavorsí › Pallars Sobirà | 2 |
| Forêt de Llavorsí (23) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 2 |
| Forêt de la Guingueta d'Àneu (28) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 2 |
| Forêt de la Guingueta d'Àneu (30) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 2 |
| Forêt de la Guingueta d'Àneu (31) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 2 |
| Forêt de la Guingueta d'Àneu (37) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 2 |
| Forêt de la Guingueta d'Àneu (40) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 2 |
| Forêt de la Guingueta d'Àneu (50) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 2 |
| Forêt de la Guingueta d'Àneu (72) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 2 |
| Forêt de Montferrer i Castellbò (39) ⚠️ | Montferrer i Castellbò › Alt Urgell | 2 |
| Forêt de Soriguera (32) ⚠️ | Soriguera › Pallars Sobirà | 2 |
| Forêt de Soriguera (33) ⚠️ | Soriguera › Pallars Sobirà | 2 |
| Forêt de Sort (18) ⚠️ | Sort › Pallars Sobirà | 2 |
| Forêt de Sort (19) ⚠️ | Sort › Pallars Sobirà | 2 |
| Forêt de Soriguera (40) ⚠️ | Soriguera › Pallars Sobirà | 2 |
| Forêt de Conca de Dalt (32) ⚠️ | Conca de Dalt › Pallars Jussà | 2 |
| Forêt de Vielha e Mijaran (53) ⚠️ | Vielha e Mijaran › Val d'Aran | 2 |
| Forêt de Espot (36) ⚠️ | Espot › Pallars Sobirà | 2 |
| Forêt de Espot (41) ⚠️ | Espot › Pallars Sobirà | 2 |
| Forêt de Alt Àneu (58) ⚠️ | Alt Àneu › Pallars Sobirà | 2 |
| Forêt de Gósol (27) ⚠️ | Gósol › Berguedà (Lérida) | 2 |
| Forêt de Gósol (28) ⚠️ | Gósol › Berguedà (Lérida) | 2 |
| Forêt de Alins (37) ⚠️ | Alins › Pallars Sobirà | 2 |
| Forêt de Alins (38) ⚠️ | Alins › Pallars Sobirà | 2 |
| Forêt de Alins (41) ⚠️ | Alins › Pallars Sobirà | 2 |
| Forêt de Pinós (114) ⚠️ | Pinós › Solsonès | 2 |
| Forêt de Pinós (118) ⚠️ | Pinós › Solsonès | 2 |
| Forêt de Riner (146) ⚠️ | Riner › Solsonès | 2 |
| Forêt de Riner (147) ⚠️ | Riner › Solsonès | 2 |
| Forêt de Riner (150) ⚠️ | Riner › Solsonès | 2 |
| Forêt de Pinós (132) ⚠️ | Pinós › Solsonès | 2 |
| Forêt de Pinós (139) ⚠️ | Pinós › Solsonès | 2 |
| Forêt de Pinós (147) ⚠️ | Pinós › Solsonès | 2 |
| Forêt de Pinós (152) ⚠️ | Pinós › Solsonès | 2 |
| Forêt de Pinós (159) ⚠️ | Pinós › Solsonès | 2 |
| Forêt de Pinós (163) ⚠️ | Pinós › Solsonès | 2 |
| Forêt de Riu de Cerdanya (9) ⚠️ | Riu de Cerdanya › Cerdanya (Lérida) | 2 |
| Forêt de Riu de Cerdanya (13) ⚠️ | Riu de Cerdanya › Cerdanya (Lérida) | 2 |
| Forêt de Riu de Cerdanya (14) ⚠️ | Riu de Cerdanya › Cerdanya (Lérida) | 2 |
| Forêt de Bellver de Cerdanya (41) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 2 |
| Forêt de Bellver de Cerdanya (43) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 2 |
| Forêt de Guixers (69) ⚠️ | Guixers › Solsonès | 2 |
| Forêt de la Coma i la Pedra (131) ⚠️ | la Coma i la Pedra › Solsonès | 2 |
| Forêt de la Coma i la Pedra (147) ⚠️ | la Coma i la Pedra › Solsonès | 2 |
| Forêt de la Coma i la Pedra (155) ⚠️ | la Coma i la Pedra › Solsonès | 2 |
| Forêt de la Coma i la Pedra (158) ⚠️ | la Coma i la Pedra › Solsonès | 2 |
| Forêt de Guixers (103) ⚠️ | Guixers › Solsonès | 2 |
| Forêt de Guixers (104) ⚠️ | Guixers › Solsonès | 2 |
| Forêt de Gósol (58) ⚠️ | Gósol › Berguedà (Lérida) | 2 |
| Forêt de Guixers (108) ⚠️ | Guixers › Solsonès | 2 |
| Forêt de Gósol (62) ⚠️ | Gósol › Berguedà (Lérida) | 2 |
| Forêt de Guixers (117) ⚠️ | Guixers › Solsonès | 2 |
| Forêt de la Coma i la Pedra (165) ⚠️ | la Coma i la Pedra › Solsonès | 2 |
| Forêt de Gósol (66) ⚠️ | Gósol › Berguedà (Lérida) | 2 |
| Forêt de Gósol (77) ⚠️ | Gósol › Berguedà (Lérida) | 2 |
| Forêt de Gósol (78) ⚠️ | Gósol › Berguedà (Lérida) | 2 |
| Forêt de Guixers (122) ⚠️ | Guixers › Solsonès | 2 |
| Forêt de Gósol (90) ⚠️ | Gósol › Berguedà (Lérida) | 2 |
| Forêt de Gósol (97) ⚠️ | Gósol › Berguedà (Lérida) | 2 |
| Forêt de la Coma i la Pedra (174) ⚠️ | la Coma i la Pedra › Solsonès | 2 |
| Forêt de Gósol (104) ⚠️ | Gósol › Berguedà (Lérida) | 2 |
| Forêt de Guixers (125) ⚠️ | Guixers › Solsonès | 2 |
| Forêt de Navès (154) ⚠️ | Navès › Solsonès | 2 |
| Forêt de Navès (159) ⚠️ | Navès › Solsonès | 2 |
| Forêt de Navès (160) ⚠️ | Navès › Solsonès | 2 |
| Forêt de Navès (162) ⚠️ | Navès › Solsonès | 2 |
| Forêt de Guixers (127) ⚠️ | Guixers › Solsonès | 2 |
| Forêt de Navès (167) ⚠️ | Navès › Solsonès | 2 |
| Forêt de Odèn (74) ⚠️ | Odèn › Solsonès | 2 |
| Forêt de Odèn (78) ⚠️ | Odèn › Solsonès | 2 |
| Forêt de Odèn (85) ⚠️ | Odèn › Solsonès | 2 |
| Forêt de Sant Llorenç de Morunys (32) ⚠️ | Sant Llorenç de Morunys › Solsonès | 2 |
| Forêt de Guixers (141) ⚠️ | Sant Llorenç de Morunys › Solsonès | 2 |
| Forêt de Guixers (145) ⚠️ | Guixers › Solsonès | 2 |
| Forêt de Lladurs (199) ⚠️ | Lladurs › Solsonès | 2 |
| Forêt de Odèn (109) ⚠️ | Odèn › Solsonès | 2 |
| Forêt de Lladurs (208) ⚠️ | Lladurs › Solsonès | 2 |
| Forêt de Odèn (113) ⚠️ | Odèn › Solsonès | 2 |
| Forêt de Odèn (116) ⚠️ | Odèn › Solsonès | 2 |
| Forêt de Lladurs (214) ⚠️ | Lladurs › Solsonès | 2 |
| Forêt de Lladurs (226) ⚠️ | Lladurs › Solsonès | 2 |
| Forêt de Lladurs (231) ⚠️ | Lladurs › Solsonès | 2 |
| Forêt de Lladurs (242) ⚠️ | Lladurs › Solsonès | 2 |
| Forêt de Lladurs (247) ⚠️ | Lladurs › Solsonès | 2 |
| Forêt de Lladurs (249) ⚠️ | Lladurs › Solsonès | 2 |
| Forêt de Odèn (121) ⚠️ | Odèn › Solsonès | 2 |
| Forêt de Bellver de Cerdanya (52) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 2 |
| Forêt de Bellver de Cerdanya (56) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 2 |
| Forêt de Naut Aran (78) ⚠️ | Naut Aran › Val d'Aran | 2 |
| Forêt de Alt Àneu (77) ⚠️ | Alt Àneu › Pallars Sobirà | 2 |
| Forêt de Alt Àneu (93) ⚠️ | Alt Àneu › Pallars Sobirà | 2 |
| Forêt de Alt Àneu (124) ⚠️ | Alt Àneu › Pallars Sobirà | 2 |
| Forêt de Alt Àneu (133) ⚠️ | Alt Àneu › Pallars Sobirà | 2 |
| Forêt de Alt Àneu (141) ⚠️ | Alt Àneu › Pallars Sobirà | 2 |
| Forêt de Alt Àneu (143) ⚠️ | Alt Àneu › Pallars Sobirà | 2 |
| Forêt de Alt Àneu (145) ⚠️ | Alt Àneu › Pallars Sobirà | 2 |
| Forêt de Naut Aran (99) ⚠️ | Naut Aran › Val d'Aran | 2 |
| Forêt de Naut Aran (123) ⚠️ | Naut Aran › Val d'Aran | 2 |
| Forêt de Naut Aran (124) ⚠️ | Naut Aran › Val d'Aran | 2 |
| Forêt de Canejan (17) ⚠️ | Canejan › Val d'Aran | 2 |
| Forêt de Canejan (25) ⚠️ | Canejan › Val d'Aran | 2 |
| Forêt de Canejan (26) ⚠️ | Canejan › Val d'Aran | 2 |
| Forêt de Llavorsí (36) ⚠️ | Llavorsí › Pallars Sobirà | 2 |
| Forêt de Llavorsí (42) ⚠️ | Llavorsí › Pallars Sobirà | 2 |
| Forêt de Llavorsí (44) ⚠️ | Llavorsí › Pallars Sobirà | 2 |
| Forêt de Vielha e Mijaran (61) ⚠️ | Vielha e Mijaran › Val d'Aran | 2 |
| Forêt de Vielha e Mijaran (69) ⚠️ | Vielha e Mijaran › Val d'Aran | 2 |
| Forêt de Vielha e Mijaran (70) ⚠️ | Vielha e Mijaran › Val d'Aran | 2 |
| Forêt de Es Bòrdes (15) ⚠️ | Es Bòrdes › Val d'Aran | 2 |
| Forêt de Es Bòrdes (16) ⚠️ | Es Bòrdes › Val d'Aran | 2 |
| Forêt de Alins (55) ⚠️ | Alins › Pallars Sobirà | 2 |
| Forêt de Alins (56) ⚠️ | Alins › Pallars Sobirà | 2 |
| Forêt de Vilaller (45) ⚠️ | Vilaller › Alta Ribagorça | 2 |
| Forêt de Vilaller (46) ⚠️ | Vilaller › Alta Ribagorça | 2 |
| Forêt de Vilaller (53) ⚠️ | Vilaller › Alta Ribagorça | 2 |
| Forêt de Vilaller (56) ⚠️ | Vilaller › Alta Ribagorça | 2 |
| Forêt de el Pont de Bar (9) ⚠️ | el Pont de Bar › Alt Urgell | 2 |
| Forêt de Bellver de Cerdanya (62) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 2 |
| Forêt de Bellver de Cerdanya (63) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 2 |
| Forêt de Bellver de Cerdanya (65) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 2 |
| Forêt de la Seu d'Urgell (9) ⚠️ | la Seu d'Urgell › Alt Urgell | 2 |
| Forêt de Alàs i Cerc (13) ⚠️ | Alàs i Cerc › Alt Urgell | 2 |
| Forêt de les Valls de Valira (85) ⚠️ | les Valls de Valira › Alt Urgell | 2 |
| Forêt de les Valls de Valira (99) ⚠️ | les Valls de Valira › Alt Urgell | 2 |
| Forêt de les Valls de Valira (120) ⚠️ | les Valls de Valira › Alt Urgell | 2 |
| Forêt de la Seu d'Urgell (15) ⚠️ | la Seu d'Urgell › Alt Urgell | 2 |
| Forêt de Ribera d'Urgellet (43) ⚠️ | Ribera d'Urgellet › Alt Urgell | 2 |
| Forêt de Montferrer i Castellbò (48) ⚠️ | Ribera d'Urgellet › Alt Urgell | 2 |
| Forêt de Montferrer i Castellbò (54) ⚠️ | Montferrer i Castellbò › Alt Urgell | 2 |
| Forêt de Montferrer i Castellbò (66) ⚠️ | Montferrer i Castellbò › Alt Urgell | 2 |
| Forêt de Montferrer i Castellbò (70) ⚠️ | Montferrer i Castellbò › Alt Urgell | 2 |
| Forêt de Oliana (13) ⚠️ | Oliana › Alt Urgell | 2 |
| Forêt de Oliana (16) ⚠️ | Oliana › Alt Urgell | 2 |
| Forêt de Cabó (25) ⚠️ | Cabó › Alt Urgell | 2 |
| Forêt de Cabó (31) ⚠️ | Cabó › Alt Urgell | 2 |
| Forêt de Cabó (42) ⚠️ | Cabó › Alt Urgell | 2 |
| Forêt de Cabó (47) ⚠️ | Cabó › Alt Urgell | 2 |
| Forêt de la Baronia de Rialb (50) ⚠️ | la Baronia de Rialb › Noguera | 2 |
| Forêt de Ponts (5) ⚠️ | Ponts › Noguera | 2 |
| Forêt de Bassella (27) ⚠️ | Bassella › Alt Urgell | 2 |
| Forêt de Bassella (29) ⚠️ | Bassella › Alt Urgell | 2 |
| Forêt de Josa i Tuixén (30) ⚠️ | Josa i Tuixén › Alt Urgell | 2 |
| Forêt de Josa i Tuixén (48) ⚠️ | Josa i Tuixén › Alt Urgell | 2 |
| Forêt de Josa i Tuixén (49) ⚠️ | Josa i Tuixén › Alt Urgell | 2 |
| Forêt de Josa i Tuixén (55) ⚠️ | Josa i Tuixén › Alt Urgell | 2 |
| Forêt de Montellà i Martinet (40) ⚠️ | Montellà i Martinet › Cerdanya (Lérida) | 2 |
| Forêt de Montellà i Martinet (48) ⚠️ | Montellà i Martinet › Cerdanya (Lérida) | 2 |
| Forêt de Bellver de Cerdanya (74) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 2 |
| Forêt de Gósol (108) ⚠️ | Gósol › Berguedà (Lérida) | 2 |
| Forêt de les Valls de Valira (125) ⚠️ | les Valls de Valira › Alt Urgell | 2 |
| Forêt de Camarasa (35) ⚠️ | Camarasa › Noguera | 2 |
| Forêt de Tremp (89) ⚠️ | Tremp › Pallars Jussà | 2 |
| Forêt de Tremp (90) ⚠️ | Tremp › Pallars Jussà | 2 |
| Forêt de Navès (177) ⚠️ | Navès › Solsonès | 2 |
| Forêt de Olius (332) ⚠️ | Olius › Solsonès | 2 |
| Forêt de Olius (336) ⚠️ | Olius › Solsonès | 2 |
| Forêt de Olius (339) ⚠️ | Olius › Solsonès | 2 |
| Forêt de Olius (343) ⚠️ | Olius › Solsonès | 2 |
| Forêt de Navès (197) ⚠️ | Navès › Solsonès | 2 |
| Forêt de Navès (203) ⚠️ | Navès › Solsonès | 2 |
| Forêt de Navès (211) ⚠️ | Navès › Solsonès | 2 |
| Forêt de Navès (214) ⚠️ | Navès › Solsonès | 2 |
| Forêt de Clariana de Cardener (168) ⚠️ | Clariana de Cardener › Solsonès | 2 |
| Forêt de Clariana de Cardener (173) ⚠️ | Clariana de Cardener › Solsonès | 2 |
| Forêt de Bellver de Cerdanya (79) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 2 |
| Forêt de Peramola (28) ⚠️ | Peramola › Alt Urgell | 2 |
| Forêt de Tremp (92) ⚠️ | Tremp › Pallars Jussà | 2 |
| Forêt de Tremp (95) ⚠️ | Tremp › Pallars Jussà | 2 |
| Forêt de Conca de Dalt (33) ⚠️ | Conca de Dalt › Pallars Jussà | 2 |
| Forêt de Olius (356) ⚠️ | Olius › Solsonès | 2 |
| Forêt de Àger (42) ⚠️ | Àger › Noguera | 2 |
| Forêt de Àger (48) ⚠️ | Àger › Noguera | 2 |
| Forêt de Sant Esteve de la Sarga (10) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 2 |
| Forêt de Àger (53) ⚠️ | Àger › Noguera | 2 |
| Forêt de Sant Esteve de la Sarga (29) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 2 |
| Forêt de Sant Esteve de la Sarga (31) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 2 |
| Forêt de Baix Pallars (42) ⚠️ | Baix Pallars › Pallars Sobirà | 2 |
| Forêt de Baix Pallars (60) ⚠️ | Baix Pallars › Pallars Sobirà | 2 |
| Forêt de Navès (219) ⚠️ | Clariana de Cardener › Solsonès | 2 |
| Forêt de Riner (158) ⚠️ | Riner › Solsonès | 2 |
| Forêt de Clariana de Cardener (190) ⚠️ | Clariana de Cardener › Solsonès | 2 |
| Forêt de Clariana de Cardener (191) ⚠️ | Clariana de Cardener › Solsonès | 2 |
| Forêt de Clariana de Cardener (196) ⚠️ | Clariana de Cardener › Solsonès | 2 |
| Forêt de Clariana de Cardener (198) ⚠️ | Clariana de Cardener › Solsonès | 2 |
| Forêt de Clariana de Cardener (200) ⚠️ | Clariana de Cardener › Solsonès | 2 |
| Forêt de Clariana de Cardener (204) ⚠️ | Clariana de Cardener › Solsonès | 2 |
| Forêt de Clariana de Cardener (206) ⚠️ | Clariana de Cardener › Solsonès | 2 |
| Forêt de Clariana de Cardener (210) ⚠️ | Clariana de Cardener › Solsonès | 2 |
| Forêt de Llobera (488) ⚠️ | Llobera › Solsonès | 2 |
| Forêt de Llobera (490) ⚠️ | Llobera › Solsonès | 2 |
| Forêt de Castell de Mur (28) ⚠️ | Castell de Mur › Pallars Jussà | 2 |
| Forêt de Àger (61) ⚠️ | Àger › Noguera | 2 |
| Forêt de Àger (67) ⚠️ | Àger › Noguera | 2 |
| Forêt de Àger (71) ⚠️ | Àger › Noguera | 2 |
| Forêt de Camarasa (48) ⚠️ | Camarasa › Noguera | 2 |
| Forêt de Llimiana (15) ⚠️ | Llimiana › Pallars Jussà | 2 |
| Forêt de Llimiana (16) ⚠️ | Llimiana › Pallars Jussà | 2 |
| Forêt de Sant Esteve de la Sarga (40) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 2 |
| Forêt de Sant Esteve de la Sarga (65) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 2 |
| Forêt de Sant Esteve de la Sarga (66) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 2 |
| Forêt de Àger (79) ⚠️ | Àger › Noguera | 2 |
| Forêt de Àger (82) ⚠️ | Àger › Noguera | 2 |
| Forêt de Àger (85) ⚠️ | Àger › Noguera | 2 |
| Forêt de Àger (100) ⚠️ | Àger › Noguera | 2 |
| Forêt de Àger (106) ⚠️ | Àger › Noguera | 2 |
| Forêt de Àger (108) ⚠️ | Àger › Noguera | 2 |
| Forêt de Àger (109) ⚠️ | Àger › Noguera | 2 |
| Forêt de Àger (147) ⚠️ | Àger › Noguera | 2 |
| Forêt de Àger (151) ⚠️ | Àger › Noguera | 2 |
| Forêt de Àger (163) ⚠️ | Àger › Noguera | 2 |
| Forêt de Àger (167) ⚠️ | Àger › Noguera | 2 |
| Forêt de Àger (169) ⚠️ | Àger › Noguera | 2 |
| Forêt de Os de Balaguer (42) ⚠️ | Os de Balaguer › Noguera | 2 |
| Forêt de Llobera (495) ⚠️ | Llobera › Solsonès | 2 |
| Forêt de Os de Balaguer (55) ⚠️ | Os de Balaguer › Noguera | 2 |
| Forêt de Ivars de Noguera (11) ⚠️ | Ivars de Noguera › Noguera | 2 |
| Forêt de Ivars de Noguera (14) ⚠️ | Ivars de Noguera › Noguera | 2 |
| Forêt de Os de Balaguer (76) ⚠️ | Os de Balaguer › Noguera | 2 |
| Forêt de Algerri (6) ⚠️ | Algerri › Noguera | 2 |
| Forêt de Coll de Nargó (99) ⚠️ | Coll de Nargó › Alt Urgell | 2 |
| Forêt de Coll de Nargó (128) ⚠️ | Coll de Nargó › Alt Urgell | 2 |
| Forêt de Abella de la Conca (72) ⚠️ | Abella de la Conca › Pallars Jussà | 2 |
| Forêt de Tremp (97) ⚠️ | Tremp › Pallars Jussà | 2 |
| Forêt de Tremp (121) ⚠️ | Tremp › Pallars Jussà | 2 |
| Forêt de el Pont de Suert (57) ⚠️ | el Pont de Suert › Alta Ribagorça | 2 |
| Forêt de el Pont de Suert (65) ⚠️ | el Pont de Suert › Alta Ribagorça | 2 |
| Forêt de el Pont de Suert (72) ⚠️ | el Pont de Suert › Alta Ribagorça | 2 |
| Forêt de el Pont de Suert (86) ⚠️ | el Pont de Suert › Alta Ribagorça | 2 |
| Forêt de el Pont de Suert (89) ⚠️ | el Pont de Suert › Alta Ribagorça | 2 |
| Forêt de el Pont de Suert (90) ⚠️ | el Pont de Suert › Alta Ribagorça | 2 |
| Forêt de Vilaller (72) ⚠️ | Vilaller › Alta Ribagorça | 2 |
| Forêt de Navès (223) ⚠️ | Navès › Solsonès | 2 |
| Forêt de Navès (225) ⚠️ | Navès › Solsonès | 2 |
| Bois de la Torre de Cabdella (44) ⚠️ | la Torre de Cabdella › Pallars Jussà | 2 |
| Forêt de Montferrer i Castellbò (89) ⚠️ | Montferrer i Castellbò › Alt Urgell | 2 |
| Forêt de Tremp (127) ⚠️ | Tremp › Pallars Jussà | 2 |
| Forêt de Alins (83) ⚠️ | Alins › Pallars Sobirà | 2 |
| Forêt de Alins (85) ⚠️ | Alins › Pallars Sobirà | 2 |
| Forêt de Alins (87) ⚠️ | Alins › Pallars Sobirà | 2 |
| Forêt de Alins (89) ⚠️ | Alins › Pallars Sobirà | 2 |
| Forêt de Llobera (517) ⚠️ | Llobera › Solsonès | 2 |
| Parc de Barruera ⚠️ | la Vall de Boí › Alta Ribagorça | 2 |
| Forêt de Llobera (529) ⚠️ | Llobera › Solsonès | 2 |
| Forêt de Alins (105) ⚠️ | Alins › Pallars Sobirà | 2 |
| Forêt de Alins (116) ⚠️ | Alins › Pallars Sobirà | 2 |
| Forêt de la Guingueta d'Àneu (83) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 2 |
| Forêt de Lleida (27) ⚠️ | Lleida › Segrià | 2 |
| Forêt de Vielha e Mijaran (82) ⚠️ | Vielha e Mijaran › Val d'Aran | 2 |
| Forêt de Vielha e Mijaran (83) ⚠️ | Vielha e Mijaran › Val d'Aran | 2 |
| Forêt de Clariana de Cardener (238) ⚠️ | Clariana de Cardener › Solsonès | 2 |
| Forêt de el Pont de Bar (12) ⚠️ | el Pont de Bar › Alt Urgell | 2 |
| Forêt de el Pont de Bar (18) ⚠️ | el Pont de Bar › Alt Urgell | 2 |
| Forêt de Montellà i Martinet (49) ⚠️ | Montellà i Martinet › Cerdanya (Lérida) | 2 |
| Forêt de Montellà i Martinet (51) ⚠️ | Montellà i Martinet › Cerdanya (Lérida) | 2 |
| Forêt de el Pont de Bar (30) ⚠️ | el Pont de Bar › Alt Urgell | 2 |
| Forêt de el Pont de Bar (31) ⚠️ | el Pont de Bar › Alt Urgell | 2 |
| Forêt de Arsèguel (15) ⚠️ | Arsèguel › Alt Urgell | 2 |
| Forêt de Arsèguel (16) ⚠️ | Arsèguel › Alt Urgell | 2 |
| Forêt de la Vall de Boí (271) ⚠️ | la Vall de Boí › Alta Ribagorça | 2 |
| Forêt de Seròs (9) ⚠️ | Seròs › Segrià | 2 |
| Forêt de la Granja d'Escarp (12) ⚠️ | la Granja d'Escarp › Segrià | 2 |
| Forêt de Massalcoreig (7) ⚠️ | Massalcoreig › Segrià | 2 |
| Forêt de Massalcoreig (8) ⚠️ | Massalcoreig › Segrià | 2 |
| Forêt de Estamariu (16) ⚠️ | Estamariu › Alt Urgell | 2 |
| Forêt de Estamariu (21) ⚠️ | Estamariu › Alt Urgell | 2 |
| Forêt de Montferrer i Castellbò (102) ⚠️ | Montferrer i Castellbò › Alt Urgell | 2 |
| Forêt de la Seu d'Urgell (23) ⚠️ | la Seu d'Urgell › Alt Urgell | 2 |
| Forêt de Lladurs (275) ⚠️ | Lladurs › Solsonès | 2 |
| Forêt de Conca de Dalt (48) ⚠️ | Conca de Dalt › Pallars Jussà | 2 |
| Forêt de la Pobla de Segur (34) ⚠️ | la Pobla de Segur › Pallars Jussà | 2 |
| Forêt de Conca de Dalt (54) ⚠️ | Conca de Dalt › Pallars Jussà | 2 |
| Forêt de Senterada (17) ⚠️ | Senterada › Pallars Jussà | 2 |
| Forêt de la Pobla de Segur (36) ⚠️ | la Pobla de Segur › Pallars Jussà | 2 |
| Forêt de Vall de Cardós (59) ⚠️ | Vall de Cardós › Pallars Sobirà | 2 |
| Forêt de Vall de Cardós (64) ⚠️ | Vall de Cardós › Pallars Sobirà | 2 |
| Forêt de Lladorre (51) ⚠️ | Lladorre › Pallars Sobirà | 2 |
| Forêt de la Vall de Boí (283) ⚠️ | la Vall de Boí › Alta Ribagorça | 2 |
| Forêt de Riner (170) ⚠️ | Riner › Solsonès | 2 |
| Parc del Joc de la Bola ⚠️ | Lleida › Segrià | 1 |
| Forêt de Tarrés ⚠️ | Tarrés › Garrigues | 1 |
| Forêt de Maials ⚠️ | Maials › Segrià | 1 |
| Forêt de Vilaller ⚠️ | Vilaller › Alta Ribagorça | 1 |
| Forêt de Castellar de la Ribera (2) ⚠️ | Castellar de la Ribera › Solsonès | 1 |
| Forêt de Tremp (9) ⚠️ | Tremp › Pallars Jussà | 1 |
| Forêt de Lladurs (4) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Talavera ⚠️ | Talavera › Segarra | 1 |
| Forêt de les Valls d'Aguilar (6) ⚠️ | les Valls d'Aguilar › Alt Urgell | 1 |
| Forêt de Pinell de Solsonès (12) ⚠️ | Pinell de Solsonès › Solsonès | 1 |
| Forêt de Vinaixa (5) ⚠️ | Vinaixa › Garrigues | 1 |
| Forêt de Talavera (4) ⚠️ | Talavera › Segarra | 1 |
| Forêt de Montferrer i Castellbò (9) ⚠️ | Montferrer i Castellbò › Alt Urgell | 1 |
| Forêt de les Valls de Valira (4) ⚠️ | les Valls de Valira › Alt Urgell | 1 |
| Forêt de Montferrer i Castellbò (12) ⚠️ | Montferrer i Castellbò › Alt Urgell | 1 |
| Forêt de les Valls d'Aguilar (18) ⚠️ | les Valls d'Aguilar › Alt Urgell | 1 |
| Forêt de Fígols i Alinyà (5) ⚠️ | Fígols i Alinyà › Alt Urgell | 1 |
| Forêt de Coll de Nargó (11) ⚠️ | Coll de Nargó › Alt Urgell | 1 |
| Forêt de Olius (3) ⚠️ | Olius › Solsonès | 1 |
| Forêt de la Baronia de Rialb (29) ⚠️ | la Baronia de Rialb › Noguera | 1 |
| Forêt de Baix Pallars (20) ⚠️ | Baix Pallars › Pallars Sobirà | 1 |
| Forêt de Coll de Nargó (16) ⚠️ | Coll de Nargó › Alt Urgell | 1 |
| Forêt de el Vilosell (3) ⚠️ | el Vilosell › Garrigues | 1 |
| Forêt de Montferrer i Castellbò (18) ⚠️ | Montferrer i Castellbò › Alt Urgell | 1 |
| Forêt de Coll de Nargó (17) ⚠️ | Coll de Nargó › Alt Urgell | 1 |
| Forêt de Lladurs (41) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de la Granja d'Escarp (5) ⚠️ | la Granja d'Escarp › Segrià | 1 |
| Forêt de Seròs (3) ⚠️ | Seròs › Segrià | 1 |
| Forêt de Tarrés (11) ⚠️ | Tarrés › Garrigues | 1 |
| Forêt de Talavera (12) ⚠️ | Talavera › Segarra | 1 |
| Forêt de Tremp (47) ⚠️ | Tremp › Pallars Jussà | 1 |
| Forêt de el Pont de Suert (19) ⚠️ | el Pont de Suert › Alta Ribagorça | 1 |
| Forêt de Ivars de Noguera ⚠️ | Ivars de Noguera › Noguera | 1 |
| Forêt de el Pont de Suert (21) ⚠️ | el Pont de Suert › Alta Ribagorça | 1 |
| Forêt de Vilaller (19) ⚠️ | Vilaller › Alta Ribagorça | 1 |
| Forêt de Vilaller (21) ⚠️ | Vilaller › Alta Ribagorça | 1 |
| Forêt de Os de Balaguer (14) ⚠️ | Os de Balaguer › Noguera | 1 |
| Forêt de la Molsosa (6) ⚠️ | la Molsosa › Solsonès | 1 |
| Forêt de Riner ⚠️ | Riner › Solsonès | 1 |
| Forêt de Navès (2) ⚠️ | Navès › Solsonès | 1 |
| Forêt de la Molsosa (8) ⚠️ | la Molsosa › Solsonès | 1 |
| Parc de la Boixadera ⚠️ | la Seu d'Urgell › Alt Urgell | 1 |
| Forêt de Lleida (3) ⚠️ | Lleida › Segrià | 1 |
| Parc Mare de la Font ⚠️ | Solsona › Solsonès | 1 |
| Parc de Sant Llorenç de Morunys (2) ⚠️ | Sant Llorenç de Morunys › Solsonès | 1 |
| Parc de la Roca del Call ⚠️ | Ponts › Noguera | 1 |
| Forêt de Penelles ⚠️ | Penelles › Noguera | 1 |
| Parc de l'Aigua ⚠️ | Almacelles › Segrià | 1 |
| Parc de Olius ⚠️ | Olius › Solsonès | 1 |
| Bosc de Montcortès ⚠️ | els Plans de Sió › Segarra | 1 |
| Bosc del Pi ⚠️ | els Plans de Sió › Segarra | 1 |
| Parc de la Transsegre ⚠️ | Balaguer › Noguera | 1 |
| Parc de Tremp ⚠️ | Tremp › Pallars Jussà | 1 |
| Bosc del Tresó ⚠️ | els Plans de Sió › Segarra | 1 |
| Forêt de Rialp (4) ⚠️ | Rialp › Pallars Sobirà | 1 |
| Forêt de Seròs (4) ⚠️ | Seròs › Segrià | 1 |
| Parc de Bellver de Cerdanya (3) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 1 |
| Bosc de l'Hort Tancat ⚠️ | Tàrrega › Urgell | 1 |
| Bois de els Plans de Sió ⚠️ | els Plans de Sió › Segarra | 1 |
| Bois de els Plans de Sió (4) ⚠️ | els Plans de Sió › Segarra | 1 |
| Bosquet del Ventura ⚠️ | Torrefeta i Florejacs › Segarra | 1 |
| Bosc de la Quadra del Gomar ⚠️ | Granyanella › Segarra | 1 |
| Bois de Torrefeta i Florejacs (4) ⚠️ | Torrefeta i Florejacs › Segarra | 1 |
| Bosquet del Gomar ⚠️ | Sant Guim de la Plana › Segarra | 1 |
| Bois de Torrefeta i Florejacs (6) ⚠️ | Torrefeta i Florejacs › Segarra | 1 |
| Forêt de la Coma i la Pedra (5) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de la Coma i la Pedra (6) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de la Coma i la Pedra (8) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de la Coma i la Pedra (10) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de la Coma i la Pedra (14) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de la Coma i la Pedra (27) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de la Coma i la Pedra (28) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de la Coma i la Pedra (31) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de la Coma i la Pedra (33) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de la Coma i la Pedra (35) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de la Coma i la Pedra (36) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de la Coma i la Pedra (40) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de la Coma i la Pedra (41) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de la Coma i la Pedra (42) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de la Coma i la Pedra (44) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de la Coma i la Pedra (45) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de la Coma i la Pedra (46) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de la Coma i la Pedra (47) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de la Coma i la Pedra (57) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de la Coma i la Pedra (62) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de la Coma i la Pedra (63) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de la Coma i la Pedra (64) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de la Coma i la Pedra (65) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Bois de Agramunt (4) ⚠️ | Agramunt › Urgell | 1 |
| Forêt de les Valls de Valira (9) ⚠️ | les Valls de Valira › Alt Urgell | 1 |
| Forêt de Bellver de Cerdanya (3) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 1 |
| Plaça de l'Amistat ⚠️ | Lleida › Segrià | 1 |
| Plaça d'Elisenda de Montcada ⚠️ | Lleida › Segrià | 1 |
| Bois de Gimenells i el Pla de la Font ⚠️ | Gimenells i el Pla de la Font › Segrià | 1 |
| Forêt de Gimenells i el Pla de la Font (7) ⚠️ | Gimenells i el Pla de la Font › Segrià | 1 |
| Bois de Gimenells i el Pla de la Font (8) ⚠️ | Gimenells i el Pla de la Font › Segrià | 1 |
| Bois de Gimenells i el Pla de la Font (9) ⚠️ | Gimenells i el Pla de la Font › Segrià | 1 |
| Bois de Gimenells i el Pla de la Font (13) ⚠️ | Gimenells i el Pla de la Font › Segrià | 1 |
| Bois de Gimenells i el Pla de la Font (16) ⚠️ | Gimenells i el Pla de la Font › Segrià | 1 |
| Bois de Gimenells i el Pla de la Font (17) ⚠️ | Gimenells i el Pla de la Font › Segrià | 1 |
| Bois de Gimenells i el Pla de la Font (21) ⚠️ | Gimenells i el Pla de la Font › Segrià | 1 |
| Bois de Gimenells i el Pla de la Font (24) ⚠️ | Gimenells i el Pla de la Font › Segrià | 1 |
| Bois de Gimenells i el Pla de la Font (32) ⚠️ | Gimenells i el Pla de la Font › Segrià | 1 |
| Bois de Gimenells i el Pla de la Font (36) ⚠️ | Gimenells i el Pla de la Font › Segrià | 1 |
| Bois de Gimenells i el Pla de la Font (38) ⚠️ | Gimenells i el Pla de la Font › Segrià | 1 |
| Bois de Gimenells i el Pla de la Font (39) ⚠️ | Gimenells i el Pla de la Font › Segrià | 1 |
| Bois de Gimenells i el Pla de la Font (41) ⚠️ | Gimenells i el Pla de la Font › Segrià | 1 |
| Bois de Gimenells i el Pla de la Font (42) ⚠️ | Gimenells i el Pla de la Font › Segrià | 1 |
| Bois de Gimenells i el Pla de la Font (44) ⚠️ | Gimenells i el Pla de la Font › Segrià | 1 |
| Bois de Gimenells i el Pla de la Font (45) ⚠️ | Gimenells i el Pla de la Font › Segrià | 1 |
| Bois de Gimenells i el Pla de la Font (46) ⚠️ | Gimenells i el Pla de la Font › Segrià | 1 |
| Bois de Gimenells i el Pla de la Font (51) ⚠️ | Gimenells i el Pla de la Font › Segrià | 1 |
| Bois de Gimenells i el Pla de la Font (53) ⚠️ | Gimenells i el Pla de la Font › Segrià | 1 |
| Bois de Lleida (9) ⚠️ | Lleida › Segrià | 1 |
| Parc del Graó ⚠️ | Alpicat › Segrià | 1 |
| Parc municipal ⚠️ | Mollerussa › Pla d'Urgell | 1 |
| Plaça del Vell Pla ⚠️ | Guissona › Segarra | 1 |
| Parc del Graó (2) ⚠️ | Alpicat › Segrià | 1 |
| Forêt de Biosca (12) ⚠️ | Biosca › Solsonès | 1 |
| Bois de Guimerà (6) ⚠️ | Guimerà › Urgell | 1 |
| Plaça de Clara Campoamor ⚠️ | Lleida › Segrià | 1 |
| Plaça del Clot de les Granotes ⚠️ | Lleida › Segrià | 1 |
| Forêt de Espot (8) ⚠️ | Espot › Pallars Sobirà | 1 |
| Forêt de Espot (15) ⚠️ | Espot › Pallars Sobirà | 1 |
| Forêt de Espot (16) ⚠️ | Espot › Pallars Sobirà | 1 |
| Forêt de Espot (17) ⚠️ | Espot › Pallars Sobirà | 1 |
| Forêt de Espot (18) ⚠️ | Espot › Pallars Sobirà | 1 |
| Forêt de Espot (19) ⚠️ | Espot › Pallars Sobirà | 1 |
| Plaça de l'Escorxador ⚠️ | Lleida › Segrià | 1 |
| Parc de La Serra ⚠️ | Mollerussa › Pla d'Urgell | 1 |
| Bois de els Plans de Sió (15) ⚠️ | els Plans de Sió › Segarra | 1 |
| Forêt de Ivars de Noguera (3) ⚠️ | Ivars de Noguera › Noguera | 1 |
| Forêt de Llimiana ⚠️ | Llimiana › Pallars Jussà | 1 |
| Forêt de Peramola (4) ⚠️ | Peramola › Alt Urgell | 1 |
| Passeig de Joan Brudieu ⚠️ | la Seu d'Urgell › Alt Urgell | 1 |
| Parc de el Pont de Suert ⚠️ | el Pont de Suert › Alta Ribagorça | 1 |
| Forêt de Vilanova de la Barca (3) ⚠️ | Vilanova de la Barca › Segrià | 1 |
| Forêt de Os de Balaguer (18) ⚠️ | Os de Balaguer › Noguera | 1 |
| Parc de el Palau d'Anglesola ⚠️ | el Palau d'Anglesola › Pla d'Urgell | 1 |
| Forêt de Solsona (3) ⚠️ | Solsona › Solsonès | 1 |
| Bois de Solsona (2) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Solsona (4) ⚠️ | Solsona › Solsonès | 1 |
| Parc de Solsona (5) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Solsona (5) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Solsona (6) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Solsona (7) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Solsona (8) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Sarroca de Bellera (16) ⚠️ | Sarroca de Bellera › Pallars Jussà | 1 |
| Forêt de Sarroca de Bellera (18) ⚠️ | Sarroca de Bellera › Pallars Jussà | 1 |
| Forêt de Solsona (16) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Solsona (18) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Solsona (20) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Solsona (22) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Solsona (23) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Solsona (25) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (9) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Solsona (47) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Solsona (49) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Olius (11) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Solsona (51) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Solsona (59) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Solsona (60) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Solsona (61) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Solsona (62) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Solsona (64) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Solsona (66) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Solsona (68) ⚠️ | Solsona › Solsonès | 1 |
| Plaça de les Pobles ⚠️ | la Pobla de Segur › Pallars Jussà | 1 |
| Forêt de la Granja d'Escarp (9) ⚠️ | la Granja d'Escarp › Segrià | 1 |
| Forêt de Olius (13) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (15) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (20) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Solsona (70) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Olius (21) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Massalcoreig ⚠️ | Massalcoreig › Segrià | 1 |
| Forêt de Cervera (5) ⚠️ | Cervera › Segarra | 1 |
| Bois de Cervera (2) ⚠️ | Cervera › Segarra | 1 |
| Bois de Ribera d'Ondara ⚠️ | Ribera d'Ondara › Segarra | 1 |
| Bois de les Oluges ⚠️ | les Oluges › Segarra | 1 |
| Forêt de Naut Aran (13) ⚠️ | Naut Aran › Val d'Aran | 1 |
| Forêt de la Guingueta d'Àneu (9) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 1 |
| Forêt de Alt Àneu (6) ⚠️ | Alt Àneu › Pallars Sobirà | 1 |
| Forêt de Alt Àneu (7) ⚠️ | Alt Àneu › Pallars Sobirà | 1 |
| Forêt de Alt Àneu (8) ⚠️ | Alt Àneu › Pallars Sobirà | 1 |
| Forêt de Solsona (73) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Olius (22) ⚠️ | Olius › Solsonès | 1 |
| Bois de Alcarràs (4) ⚠️ | Alcarràs › Segrià | 1 |
| Bois de Alcarràs (7) ⚠️ | Alcarràs › Segrià | 1 |
| Forêt de Alt Àneu (14) ⚠️ | Alt Àneu › Pallars Sobirà | 1 |
| Forêt de la Guingueta d'Àneu (12) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 1 |
| Forêt de Solsona (81) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Solsona (86) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Solsona (87) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Solsona (89) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Solsona (92) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Solsona (97) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Solsona (98) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Solsona (101) ⚠️ | Solsona › Solsonès | 1 |
| Parc de Les ⚠️ | Les › Val d'Aran | 1 |
| Forêt de Bossòst (4) ⚠️ | Bossòst › Val d'Aran | 1 |
| Forêt de Cabó (4) ⚠️ | Cabó › Alt Urgell | 1 |
| Forêt de Coll de Nargó (19) ⚠️ | Coll de Nargó › Alt Urgell | 1 |
| Jardins de George Orwell ⚠️ | Lleida › Segrià | 1 |
| Forêt de Tremp (49) ⚠️ | Tremp › Pallars Jussà | 1 |
| Forêt de Tremp (50) ⚠️ | Tremp › Pallars Jussà | 1 |
| Forêt de Navès (5) ⚠️ | Navès › Solsonès | 1 |
| Parc d'Europa ⚠️ | Almacelles › Segrià | 1 |
| Forêt de Pinós (17) ⚠️ | Pinós › Solsonès | 1 |
| Parc de Mollerussa (2) ⚠️ | Mollerussa › Pla d'Urgell | 1 |
| Forêt de Castellar de la Ribera (12) ⚠️ | Castellar de la Ribera › Solsonès | 1 |
| Forêt de Conca de Dalt (18) ⚠️ | Conca de Dalt › Pallars Jussà | 1 |
| Parc municipal Alcalde Boixareu ⚠️ | la Pobla de Segur › Pallars Jussà | 1 |
| Parc de Miralcamp ⚠️ | Miralcamp › Pla d'Urgell | 1 |
| Tossal dels Morts ⚠️ | Alcoletge › Segrià | 1 |
| Forêt de Sidamon (2) ⚠️ | Sidamon › Pla d'Urgell | 1 |
| Forêt de Naut Aran (19) ⚠️ | Naut Aran › Val d'Aran | 1 |
| Forêt de Naut Aran (20) ⚠️ | Naut Aran › Val d'Aran | 1 |
| Forêt de Naut Aran (26) ⚠️ | Naut Aran › Val d'Aran | 1 |
| Forêt de Naut Aran (28) ⚠️ | Naut Aran › Val d'Aran | 1 |
| Forêt de Bellvís ⚠️ | Bellvís › Pla d'Urgell | 1 |
| Parc de Balaguer (3) ⚠️ | Balaguer › Noguera | 1 |
| Parc del Sindicat ⚠️ | Cervera › Segarra | 1 |
| Parc de Balaguer (9) ⚠️ | Balaguer › Noguera | 1 |
| Parc de Lleida (16) ⚠️ | Lleida › Segrià | 1 |
| Forêt de la Vansa i Fórnols (13) ⚠️ | la Vansa i Fórnols › Alt Urgell | 1 |
| Forêt de la Vansa i Fórnols (15) ⚠️ | la Vansa i Fórnols › Alt Urgell | 1 |
| Forêt de la Coma i la Pedra (84) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de la Coma i la Pedra (85) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de Vilanova de Meià (16) ⚠️ | Vilanova de Meià › Noguera | 1 |
| Forêt de Navès (12) ⚠️ | Navès › Solsonès | 1 |
| Pins del Pallera ⚠️ | Alguaire › Segrià | 1 |
| Bois de Sant Guim de Freixenet ⚠️ | Sant Guim de Freixenet › Segarra | 1 |
| Bois de la Torre de Cabdella (3) ⚠️ | la Torre de Cabdella › Pallars Jussà | 1 |
| Bois de Talavera (5) ⚠️ | Talavera › Segarra | 1 |
| Bois de Talavera (6) ⚠️ | Talavera › Segarra | 1 |
| Bois de Talavera (7) ⚠️ | Talavera › Segarra | 1 |
| Bois de Talavera (10) ⚠️ | Talavera › Segarra | 1 |
| Bois de Nalec ⚠️ | Nalec › Urgell | 1 |
| Bois de Sant Martí de Riucorb (3) ⚠️ | Sant Martí de Riucorb › Urgell | 1 |
| Bois de Sant Martí de Riucorb (4) ⚠️ | Sant Martí de Riucorb › Urgell | 1 |
| Bois de Sant Martí de Riucorb (6) ⚠️ | Sant Martí de Riucorb › Urgell | 1 |
| Bois de Sant Martí de Riucorb (7) ⚠️ | Sant Martí de Riucorb › Urgell | 1 |
| Bois de Sant Martí de Riucorb (10) ⚠️ | Sant Martí de Riucorb › Urgell | 1 |
| Bois de Sant Martí de Riucorb (11) ⚠️ | Sant Martí de Riucorb › Urgell | 1 |
| Pla de Rovellons ⚠️ | Sant Martí de Riucorb › Urgell | 1 |
| Forêt de Talavera (16) ⚠️ | Talavera › Segarra | 1 |
| Forêt de Talavera (18) ⚠️ | Talavera › Segarra | 1 |
| Bois de les Valls de Valira ⚠️ | les Valls de Valira › Alt Urgell | 1 |
| Bois de les Valls de Valira (2) ⚠️ | les Valls de Valira › Alt Urgell | 1 |
| Bois de Ribera d'Ondara (4) ⚠️ | Ribera d'Ondara › Segarra | 1 |
| Bois de Ribera d'Ondara (8) ⚠️ | Ribera d'Ondara › Segarra | 1 |
| Bois de Ribera d'Ondara (11) ⚠️ | Ribera d'Ondara › Segarra | 1 |
| Bois de Talavera (17) ⚠️ | Talavera › Segarra | 1 |
| Bois de Talavera (19) ⚠️ | Talavera › Segarra | 1 |
| Forêt de la Molsosa (14) ⚠️ | la Molsosa › Solsonès | 1 |
| Forêt de la Molsosa (15) ⚠️ | la Molsosa › Solsonès | 1 |
| Forêt de Pinós (24) ⚠️ | Pinós › Solsonès | 1 |
| Forêt de Pinós (30) ⚠️ | Pinós › Solsonès | 1 |
| Forêt de Pinós (32) ⚠️ | Pinós › Solsonès | 1 |
| Forêt de Montferrer i Castellbò (26) ⚠️ | Montferrer i Castellbò › Alt Urgell | 1 |
| Parc de Lleida (23) ⚠️ | Lleida › Segrià | 1 |
| Forêt de Lleida (16) ⚠️ | Lleida › Segrià | 1 |
| Forêt de Alt Àneu (23) ⚠️ | Alt Àneu › Pallars Sobirà | 1 |
| Bois de Ribera d'Ondara (18) ⚠️ | Ribera d'Ondara › Segarra | 1 |
| Bois de Ribera d'Ondara (20) ⚠️ | Ribera d'Ondara › Segarra | 1 |
| Bois de Talavera (23) ⚠️ | Talavera › Segarra | 1 |
| Bois de Ribera d'Ondara (24) ⚠️ | Ribera d'Ondara › Segarra | 1 |
| Bois de Talavera (29) ⚠️ | Talavera › Segarra | 1 |
| Bois de Talavera (30) ⚠️ | Talavera › Segarra | 1 |
| Bois de Talavera (34) ⚠️ | Talavera › Segarra | 1 |
| Bois de Talavera (48) ⚠️ | Talavera › Segarra | 1 |
| Bois de Talavera (49) ⚠️ | Talavera › Segarra | 1 |
| Bois de Talavera (50) ⚠️ | Talavera › Segarra | 1 |
| Bois de Talavera (52) ⚠️ | Talavera › Segarra | 1 |
| Bois de Talavera (53) ⚠️ | Talavera › Segarra | 1 |
| Forêt de Pinós (35) ⚠️ | Pinós › Solsonès | 1 |
| Bois de Talavera (54) ⚠️ | Talavera › Segarra | 1 |
| Forêt de Guixers (12) ⚠️ | Guixers › Solsonès | 1 |
| Forêt de Gósol (4) ⚠️ | Gósol › Berguedà (Lérida) | 1 |
| Forêt de Navès (13) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Navès (15) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Navès (16) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Navès (17) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Guixers (18) ⚠️ | Guixers › Solsonès | 1 |
| Forêt de Odèn (20) ⚠️ | Odèn › Solsonès | 1 |
| Forêt de Navès (18) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Navès (20) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Naut Aran (30) ⚠️ | Naut Aran › Val d'Aran | 1 |
| Forêt de Naut Aran (31) ⚠️ | Naut Aran › Val d'Aran | 1 |
| Forêt de Sant Esteve de la Sarga (4) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 1 |
| Forêt de Alàs i Cerc (5) ⚠️ | Alàs i Cerc › Alt Urgell | 1 |
| Forêt de Oliana (2) ⚠️ | Oliana › Alt Urgell | 1 |
| Forêt de Josa i Tuixén (4) ⚠️ | Josa i Tuixén › Alt Urgell | 1 |
| Forêt de Josa i Tuixén (8) ⚠️ | Josa i Tuixén › Alt Urgell | 1 |
| Jardins de Francesc Solana ⚠️ | Lleida › Segrià | 1 |
| Forêt de Tremp (56) ⚠️ | Tremp › Pallars Jussà | 1 |
| Forêt de Coll de Nargó (25) ⚠️ | Coll de Nargó › Alt Urgell | 1 |
| Forêt de Coll de Nargó (26) ⚠️ | Coll de Nargó › Alt Urgell | 1 |
| Forêt de Tremp (59) ⚠️ | Tremp › Pallars Jussà | 1 |
| Forêt de Lladurs (59) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (60) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (66) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Solsona (110) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Olius (38) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Solsona (115) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Solsona (118) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Solsona (121) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Solsona (125) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Solsona (127) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Lladurs (74) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (81) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (83) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (85) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (86) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (92) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (96) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Olius (44) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (47) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (49) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (59) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (69) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Solsona (130) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Lladurs (102) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (105) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (106) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (114) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (115) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (116) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (119) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (121) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (122) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (130) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (132) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (134) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (135) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (137) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (149) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (151) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (163) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Olius (81) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (88) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (90) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (91) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (113) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (116) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (117) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (121) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (127) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (132) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (133) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (143) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (158) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (159) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (169) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (174) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (192) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (195) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (197) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (199) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (206) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (212) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (215) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (220) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (229) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (231) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (239) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (241) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (249) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (253) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (255) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (256) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (260) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (264) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (270) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (289) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (291) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (296) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (298) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (308) ⚠️ | Olius › Solsonès | 1 |
| Les Costes ⚠️ | Arbeca › Garrigues | 1 |
| Forêt de Sant Esteve de la Sarga (5) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 1 |
| Forêt de Clariana de Cardener (13) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Forêt de Llobera (8) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (9) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (10) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (11) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (23) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (26) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (28) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (30) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (35) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (49) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (52) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (54) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (57) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (61) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (64) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (66) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (67) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (72) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (77) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (79) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (80) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (89) ⚠️ | Llobera › Solsonès | 1 |
| Parc Fluvial del Pont de Claverol ⚠️ | Conca de Dalt › Pallars Jussà | 1 |
| Forêt de Àger (16) ⚠️ | Àger › Noguera | 1 |
| Forêt de Llobera (95) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Os de Balaguer (21) ⚠️ | Os de Balaguer › Noguera | 1 |
| Forêt de Ivars de Noguera (4) ⚠️ | Ivars de Noguera › Noguera | 1 |
| Forêt de Abella de la Conca (6) ⚠️ | Abella de la Conca › Pallars Jussà | 1 |
| Forêt de Coll de Nargó (27) ⚠️ | Coll de Nargó › Alt Urgell | 1 |
| Forêt de Abella de la Conca (10) ⚠️ | Abella de la Conca › Pallars Jussà | 1 |
| Forêt de Baix Pallars (32) ⚠️ | Baix Pallars › Pallars Sobirà | 1 |
| Forêt de Llobera (103) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (104) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (105) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (106) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (107) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Bellaguarda (6) ⚠️ | Bellaguarda › Garrigues | 1 |
| Forêt de Llobera (117) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (119) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (120) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (121) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Tremp (64) ⚠️ | Tremp › Pallars Jussà | 1 |
| Forêt de el Pont de Suert (33) ⚠️ | el Pont de Suert › Alta Ribagorça | 1 |
| Forêt de Llobera (123) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (124) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (135) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (137) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (146) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (147) ⚠️ | Llobera › Solsonès | 1 |
| Bois de la Torre de Cabdella (7) ⚠️ | la Torre de Cabdella › Pallars Jussà | 1 |
| Forêt de Llobera (160) ⚠️ | Llobera › Solsonès | 1 |
| Bois de la Torre de Cabdella (8) ⚠️ | la Torre de Cabdella › Pallars Jussà | 1 |
| Bois de la Torre de Cabdella (16) ⚠️ | la Torre de Cabdella › Pallars Jussà | 1 |
| Bois de la Torre de Cabdella (21) ⚠️ | la Torre de Cabdella › Pallars Jussà | 1 |
| Bois de la Torre de Cabdella (22) ⚠️ | la Torre de Cabdella › Pallars Jussà | 1 |
| Bois de la Torre de Cabdella (25) ⚠️ | la Torre de Cabdella › Pallars Jussà | 1 |
| Bois de la Torre de Cabdella (34) ⚠️ | la Torre de Cabdella › Pallars Jussà | 1 |
| Bois de la Torre de Cabdella (35) ⚠️ | la Torre de Cabdella › Pallars Jussà | 1 |
| Bois de la Torre de Cabdella (38) ⚠️ | la Torre de Cabdella › Pallars Jussà | 1 |
| Forêt de Llobera (173) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (182) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (191) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (199) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (202) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (203) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (204) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (224) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (229) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (230) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (232) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (241) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (244) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (247) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (259) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (261) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (262) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (266) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (272) ⚠️ | Torà › Solsonès | 1 |
| Forêt de Llobera (276) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (280) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (282) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Talavera (25) ⚠️ | Talavera › Segarra | 1 |
| Forêt de Llobera (299) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (310) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (312) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (324) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (327) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (342) ⚠️ | Llobera › Solsonès | 1 |
| Bois de la Vall de Boí (2) ⚠️ | la Vall de Boí › Alta Ribagorça | 1 |
| Forêt de Llobera (345) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (357) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (364) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (371) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (376) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (388) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (399) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (404) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (409) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (412) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (435) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (453) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (459) ⚠️ | Llobera › Solsonès | 1 |
| Parc del Convent ⚠️ | Bellpuig › Urgell | 1 |
| Forêt de Llobera (463) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Conca de Dalt (22) ⚠️ | Conca de Dalt › Pallars Jussà | 1 |
| Forêt de Llobera (474) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (480) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (483) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Clariana de Cardener (15) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Forêt de Clariana de Cardener (18) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Clariana de Cardener (21) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Forêt de Clariana de Cardener (24) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Forêt de Clariana de Cardener (37) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Forêt de Clariana de Cardener (38) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Forêt de Isona i Conca Dellà (25) ⚠️ | Isona i Conca Dellà › Pallars Jussà | 1 |
| Forêt de Clariana de Cardener (46) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Parc de Rosselló (2) ⚠️ | Rosselló › Segrià | 1 |
| Parc de Rosselló (6) ⚠️ | Rosselló › Segrià | 1 |
| Forêt de Clariana de Cardener (54) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Forêt de Clariana de Cardener (57) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Parc de la Via ⚠️ | Alcarràs › Segrià | 1 |
| Bois de Cervera (12) ⚠️ | Cervera › Segarra | 1 |
| Forêt de Clariana de Cardener (62) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Forêt de Clariana de Cardener (72) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Forêt de Clariana de Cardener (74) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Forêt de Clariana de Cardener (80) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Forêt de Clariana de Cardener (88) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Forêt de Clariana de Cardener (91) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Forêt de Clariana de Cardener (94) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Forêt de Clariana de Cardener (104) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Forêt de Clariana de Cardener (106) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Bosc del Ferran ⚠️ | Sant Guim de Freixenet › Segarra | 1 |
| Forêt de Clariana de Cardener (110) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Forêt de Naut Aran (33) ⚠️ | Naut Aran › Val d'Aran | 1 |
| Forêt de Naut Aran (42) ⚠️ | Naut Aran › Val d'Aran | 1 |
| Forêt de Naut Aran (45) ⚠️ | Naut Aran › Val d'Aran | 1 |
| Forêt de Clariana de Cardener (127) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Forêt de Clariana de Cardener (131) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Forêt de Clariana de Cardener (142) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Forêt de Clariana de Cardener (148) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Forêt de la Coma i la Pedra (92) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de Lles de Cerdanya (15) ⚠️ | Lles de Cerdanya › Cerdanya (Lérida) | 1 |
| Forêt de la Vall de Boí (24) ⚠️ | la Vall de Boí › Alta Ribagorça | 1 |
| Forêt de la Vall de Boí (32) ⚠️ | la Vall de Boí › Alta Ribagorça | 1 |
| Forêt de la Vall de Boí (39) ⚠️ | la Vall de Boí › Alta Ribagorça | 1 |
| Forêt de la Vall de Boí (43) ⚠️ | la Vall de Boí › Alta Ribagorça | 1 |
| Forêt de la Vall de Boí (45) ⚠️ | la Vall de Boí › Alta Ribagorça | 1 |
| Forêt de la Vall de Boí (48) ⚠️ | la Vall de Boí › Alta Ribagorça | 1 |
| Forêt de la Vall de Boí (52) ⚠️ | la Vall de Boí › Alta Ribagorça | 1 |
| Forêt de la Vall de Boí (53) ⚠️ | la Vall de Boí › Alta Ribagorça | 1 |
| Forêt de la Vall de Boí (67) ⚠️ | la Vall de Boí › Alta Ribagorça | 1 |
| Forêt de la Vall de Boí (68) ⚠️ | la Vall de Boí › Alta Ribagorça | 1 |
| Forêt de la Vall de Boí (85) ⚠️ | la Vall de Boí › Alta Ribagorça | 1 |
| Forêt de la Vall de Boí (86) ⚠️ | la Vall de Boí › Alta Ribagorça | 1 |
| Forêt de Massalcoreig (4) ⚠️ | Massalcoreig › Segrià | 1 |
| Forêt de Alins (16) ⚠️ | Alins › Pallars Sobirà | 1 |
| Forêt de les Valls de Valira (16) ⚠️ | les Valls de Valira › Alt Urgell | 1 |
| Forêt de la Vall de Boí (104) ⚠️ | la Vall de Boí › Alta Ribagorça | 1 |
| Forêt de la Vall de Boí (105) ⚠️ | la Vall de Boí › Alta Ribagorça | 1 |
| Forêt de Riner (8) ⚠️ | Riner › Solsonès | 1 |
| Forêt de Riner (9) ⚠️ | Riner › Solsonès | 1 |
| Forêt de Riner (16) ⚠️ | Riner › Solsonès | 1 |
| Forêt de la Vall de Boí (108) ⚠️ | la Vall de Boí › Alta Ribagorça | 1 |
| Forêt de Riner (36) ⚠️ | Riner › Solsonès | 1 |
| Forêt de la Vall de Boí (109) ⚠️ | la Vall de Boí › Alta Ribagorça | 1 |
| Forêt de Riner (47) ⚠️ | Riner › Solsonès | 1 |
| Forêt de Riner (48) ⚠️ | Riner › Solsonès | 1 |
| Parc de la Vansa i Fórnols (2) ⚠️ | la Vansa i Fórnols › Alt Urgell | 1 |
| Forêt de Riner (68) ⚠️ | Riner › Solsonès | 1 |
| Bois de Sant Esteve de la Sarga (5) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 1 |
| Forêt de Vall de Cardós (25) ⚠️ | Vall de Cardós › Pallars Sobirà | 1 |
| Forêt de Vall de Cardós (31) ⚠️ | Vall de Cardós › Pallars Sobirà | 1 |
| Forêt de Vall de Cardós (39) ⚠️ | Vall de Cardós › Pallars Sobirà | 1 |
| Forêt de Vall de Cardós (41) ⚠️ | Vall de Cardós › Pallars Sobirà | 1 |
| Forêt de Vall de Cardós (43) ⚠️ | Vall de Cardós › Pallars Sobirà | 1 |
| Forêt de Vall de Cardós (56) ⚠️ | Vall de Cardós › Pallars Sobirà | 1 |
| Forêt de Riner (102) ⚠️ | Riner › Solsonès | 1 |
| Forêt de Riner (105) ⚠️ | Riner › Solsonès | 1 |
| Forêt de Riner (106) ⚠️ | Riner › Solsonès | 1 |
| Forêt de Lladorre (10) ⚠️ | Lladorre › Pallars Sobirà | 1 |
| Forêt de Lladorre (12) ⚠️ | Lladorre › Pallars Sobirà | 1 |
| Forêt de Lladorre (14) ⚠️ | Lladorre › Pallars Sobirà | 1 |
| Forêt de la Vall de Boí (162) ⚠️ | la Vall de Boí › Alta Ribagorça | 1 |
| Forêt de la Vall de Boí (187) ⚠️ | la Vall de Boí › Alta Ribagorça | 1 |
| Forêt de la Vall de Boí (191) ⚠️ | la Vall de Boí › Alta Ribagorça | 1 |
| Forêt de la Vall de Boí (194) ⚠️ | la Vall de Boí › Alta Ribagorça | 1 |
| Forêt de la Vall de Boí (218) ⚠️ | la Vall de Boí › Alta Ribagorça | 1 |
| Forêt de Riner (128) ⚠️ | Riner › Solsonès | 1 |
| Forêt de Pinós (42) ⚠️ | Pinós › Solsonès | 1 |
| Jardins de Maria Mercè Marçal ⚠️ | Lleida › Segrià | 1 |
| Forêt de el Pont de Suert (34) ⚠️ | el Pont de Suert › Alta Ribagorça | 1 |
| Forêt de Espot (32) ⚠️ | Espot › Pallars Sobirà | 1 |
| Forêt de Espot (33) ⚠️ | Espot › Pallars Sobirà | 1 |
| Forêt de Bausen (8) ⚠️ | Bausen › Val d'Aran | 1 |
| Forêt de Bausen (9) ⚠️ | Bausen › Val d'Aran | 1 |
| Forêt de Bossòst (7) ⚠️ | Bossòst › Val d'Aran | 1 |
| Forêt de Vielha e Mijaran (19) ⚠️ | Vielha e Mijaran › Val d'Aran | 1 |
| Forêt de Vielha e Mijaran (35) ⚠️ | Vielha e Mijaran › Val d'Aran | 1 |
| Forêt de Vilaller (31) ⚠️ | Vilaller › Alta Ribagorça | 1 |
| Parc del Segre ⚠️ | la Seu d'Urgell › Alt Urgell | 1 |
| Forêt de Naut Aran (57) ⚠️ | Naut Aran › Val d'Aran | 1 |
| Forêt de Naut Aran (58) ⚠️ | Naut Aran › Val d'Aran | 1 |
| Forêt de Esterri d'Àneu (6) ⚠️ | Esterri d'Àneu › Pallars Sobirà | 1 |
| Forêt de Alt Àneu (46) ⚠️ | Esterri d'Àneu › Pallars Sobirà | 1 |
| Forêt de Esterri d'Àneu (9) ⚠️ | Esterri d'Àneu › Pallars Sobirà | 1 |
| Forêt de Alt Àneu (47) ⚠️ | Alt Àneu › Pallars Sobirà | 1 |
| Forêt de Organyà (5) ⚠️ | Organyà › Alt Urgell | 1 |
| Forêt de Organyà (9) ⚠️ | Organyà › Alt Urgell | 1 |
| Forêt de Organyà (16) ⚠️ | Organyà › Alt Urgell | 1 |
| Forêt de Organyà (18) ⚠️ | Organyà › Alt Urgell | 1 |
| Forêt de la Pobla de Segur (9) ⚠️ | la Pobla de Segur › Pallars Jussà | 1 |
| Forêt de la Pobla de Segur (10) ⚠️ | la Pobla de Segur › Pallars Jussà | 1 |
| Forêt de Camarasa (13) ⚠️ | Camarasa › Noguera | 1 |
| Forêt de Camarasa (15) ⚠️ | Camarasa › Noguera | 1 |
| Forêt de Navès (40) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Gavet de la Conca (10) ⚠️ | Gavet de la Conca › Pallars Jussà | 1 |
| Forêt de Ivars de Noguera (6) ⚠️ | Ivars de Noguera › Noguera | 1 |
| Forêt de Prats i Sansor (3) ⚠️ | Prats i Sansor › Cerdanya (Lérida) | 1 |
| Forêt de Prats i Sansor (4) ⚠️ | Prats i Sansor › Cerdanya (Lérida) | 1 |
| Forêt de el Pont de Suert (43) ⚠️ | el Pont de Suert › Alta Ribagorça | 1 |
| Forêt de Gósol (10) ⚠️ | Gósol › Berguedà (Lérida) | 1 |
| Forêt de Lleida (19) ⚠️ | Lleida › Segrià | 1 |
| Forêt de Guixers (43) ⚠️ | Guixers › Solsonès | 1 |
| Forêt de Lleida (21) ⚠️ | Lleida › Segrià | 1 |
| Forêt de Baix Pallars (35) ⚠️ | Baix Pallars › Pallars Sobirà | 1 |
| Forêt de Ribera d'Urgellet (24) ⚠️ | Ribera d'Urgellet › Alt Urgell | 1 |
| Forêt de Senterada (10) ⚠️ | Senterada › Pallars Jussà | 1 |
| Forêt de Senterada (11) ⚠️ | Senterada › Pallars Jussà | 1 |
| Forêt de Senterada (13) ⚠️ | Senterada › Pallars Jussà | 1 |
| Forêt de la Torre de Cabdella (18) ⚠️ | la Torre de Cabdella › Pallars Jussà | 1 |
| Forêt de Navès (53) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Bellver de Cerdanya (20) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 1 |
| Forêt de Bellver de Cerdanya (23) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 1 |
| Forêt de Bellver de Cerdanya (25) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 1 |
| Forêt de Bellver de Cerdanya (26) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 1 |
| Forêt de Navès (62) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Cervera (8) ⚠️ | Cervera › Segarra | 1 |
| Forêt de Clariana de Cardener (162) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Platja-jardí d'Ogern ⚠️ | Bassella › Alt Urgell | 1 |
| Forêt de Castellar de la Ribera (27) ⚠️ | Castellar de la Ribera › Solsonès | 1 |
| Forêt de Bassella (20) ⚠️ | Bassella › Alt Urgell | 1 |
| Forêt de Olius (320) ⚠️ | Olius › Solsonès | 1 |
| Parc de la Mina ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Olius (323) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Arres (2) ⚠️ | Arres › Val d'Aran | 1 |
| Forêt de Arres (5) ⚠️ | Arres › Val d'Aran | 1 |
| Forêt de Vilamòs (6) ⚠️ | Vilamòs › Val d'Aran | 1 |
| Forêt de Prullans (8) ⚠️ | Prullans › Cerdanya (Lérida) | 1 |
| Bois de el Pont de Suert (4) ⚠️ | el Pont de Suert › Alta Ribagorça | 1 |
| Forêt de Ribera d'Urgellet (27) ⚠️ | Ribera d'Urgellet › Alt Urgell | 1 |
| Forêt de les Valls d'Aguilar (26) ⚠️ | les Valls d'Aguilar › Alt Urgell | 1 |
| Forêt de Ribera d'Urgellet (35) ⚠️ | Ribera d'Urgellet › Alt Urgell | 1 |
| Forêt de Fígols i Alinyà (20) ⚠️ | Fígols i Alinyà › Alt Urgell | 1 |
| Forêt de la Molsosa (29) ⚠️ | la Molsosa › Solsonès | 1 |
| Forêt de la Molsosa (30) ⚠️ | la Molsosa › Solsonès | 1 |
| Forêt de la Molsosa (32) ⚠️ | la Molsosa › Solsonès | 1 |
| Forêt de la Molsosa (33) ⚠️ | la Molsosa › Solsonès | 1 |
| Forêt de la Molsosa (37) ⚠️ | la Molsosa › Solsonès | 1 |
| Forêt de Navès (88) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Navès (94) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Navès (102) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Navès (115) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Pinós (45) ⚠️ | — | 1 |
| Forêt de Gósol (11) ⚠️ | Gósol › Berguedà (Lérida) | 1 |
| Forêt de Gósol (12) ⚠️ | Gósol › Berguedà (Lérida) | 1 |
| Forêt de Gósol (15) ⚠️ | Gósol › Berguedà (Lérida) | 1 |
| Forêt de Coll de Nargó (44) ⚠️ | Coll de Nargó › Alt Urgell | 1 |
| Forêt de Coll de Nargó (50) ⚠️ | Coll de Nargó › Alt Urgell | 1 |
| Forêt de Coll de Nargó (53) ⚠️ | Coll de Nargó › Alt Urgell | 1 |
| Forêt de Coll de Nargó (54) ⚠️ | Coll de Nargó › Alt Urgell | 1 |
| Forêt de Coll de Nargó (57) ⚠️ | Coll de Nargó › Alt Urgell | 1 |
| Forêt de Coll de Nargó (58) ⚠️ | Coll de Nargó › Alt Urgell | 1 |
| Forêt de Coll de Nargó (59) ⚠️ | Coll de Nargó › Alt Urgell | 1 |
| Forêt de Fígols i Alinyà (23) ⚠️ | Fígols i Alinyà › Alt Urgell | 1 |
| Forêt de Coll de Nargó (65) ⚠️ | Coll de Nargó › Alt Urgell | 1 |
| Forêt de Coll de Nargó (72) ⚠️ | Coll de Nargó › Alt Urgell | 1 |
| Forêt de Coll de Nargó (73) ⚠️ | Coll de Nargó › Alt Urgell | 1 |
| Forêt de Coll de Nargó (80) ⚠️ | Coll de Nargó › Alt Urgell | 1 |
| Forêt de Guixers (47) ⚠️ | Guixers › Solsonès | 1 |
| Forêt de Sant Llorenç de Morunys (20) ⚠️ | Sant Llorenç de Morunys › Solsonès | 1 |
| Forêt de Aitona (10) ⚠️ | Aitona › Segrià | 1 |
| Bois de Bellver de Cerdanya (8) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 1 |
| Forêt de Lladurs (179) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Odèn (53) ⚠️ | Odèn › Solsonès | 1 |
| Forêt de les Oluges (4) ⚠️ | les Oluges › Segarra | 1 |
| Forêt de Sant Llorenç de Morunys (22) ⚠️ | Sant Llorenç de Morunys › Solsonès | 1 |
| Forêt de Guixers (58) ⚠️ | Guixers › Solsonès | 1 |
| Forêt de Sant Llorenç de Morunys (24) ⚠️ | Sant Llorenç de Morunys › Solsonès | 1 |
| Forêt de Sort (14) ⚠️ | Sort › Pallars Sobirà | 1 |
| Forêt de Sort (15) ⚠️ | Sort › Pallars Sobirà | 1 |
| Forêt de Sudanell (3) ⚠️ | Sudanell › Segrià | 1 |
| Forêt de Pinós (49) ⚠️ | Pinós › Solsonès | 1 |
| Forêt de Pinós (52) ⚠️ | Pinós › Solsonès | 1 |
| Forêt de la Molsosa (51) ⚠️ | la Molsosa › Solsonès | 1 |
| Forêt de la Molsosa (56) ⚠️ | la Molsosa › Solsonès | 1 |
| Forêt de la Molsosa (63) ⚠️ | la Molsosa › Solsonès | 1 |
| Forêt de la Molsosa (67) ⚠️ | la Molsosa › Solsonès | 1 |
| Forêt de la Molsosa (68) ⚠️ | la Molsosa › Solsonès | 1 |
| Forêt de la Molsosa (69) ⚠️ | la Molsosa › Solsonès | 1 |
| Forêt de Pinós (63) ⚠️ | Pinós › Solsonès | 1 |
| Forêt de Pinós (64) ⚠️ | Pinós › Solsonès | 1 |
| Forêt de la Molsosa (74) ⚠️ | la Molsosa › Solsonès | 1 |
| Forêt de Pinós (66) ⚠️ | Pinós › Solsonès | 1 |
| Forêt de Pinós (75) ⚠️ | Pinós › Solsonès | 1 |
| Forêt de Pinós (76) ⚠️ | Pinós › Solsonès | 1 |
| Forêt de Pinós (79) ⚠️ | Pinós › Solsonès | 1 |
| Forêt de Pinós (85) ⚠️ | Pinós › Solsonès | 1 |
| Forêt de Pinós (92) ⚠️ | Pinós › Solsonès | 1 |
| Forêt de Pinós (93) ⚠️ | Pinós › Solsonès | 1 |
| Forêt de Pinós (99) ⚠️ | Pinós › Solsonès | 1 |
| Forêt de Rialp (13) ⚠️ | Rialp › Pallars Sobirà | 1 |
| Forêt de Rialp (15) ⚠️ | Rialp › Pallars Sobirà | 1 |
| Forêt de Llavorsí (6) ⚠️ | Llavorsí › Pallars Sobirà | 1 |
| Forêt de Llavorsí (7) ⚠️ | Llavorsí › Pallars Sobirà | 1 |
| Forêt de Llavorsí (11) ⚠️ | Llavorsí › Pallars Sobirà | 1 |
| Forêt de Llavorsí (22) ⚠️ | Llavorsí › Pallars Sobirà | 1 |
| Forêt de la Guingueta d'Àneu (33) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 1 |
| Forêt de la Guingueta d'Àneu (34) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 1 |
| Forêt de la Guingueta d'Àneu (35) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 1 |
| Forêt de la Guingueta d'Àneu (61) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 1 |
| Forêt de la Guingueta d'Àneu (62) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 1 |
| Forêt de les Valls d'Aguilar (29) ⚠️ | les Valls d'Aguilar › Alt Urgell | 1 |
| Forêt de Soriguera (27) ⚠️ | Soriguera › Pallars Sobirà | 1 |
| Forêt de Soriguera (35) ⚠️ | Sort › Pallars Sobirà | 1 |
| Forêt de Soriguera (36) ⚠️ | Soriguera › Pallars Sobirà | 1 |
| Forêt de Vielha e Mijaran (57) ⚠️ | Vielha e Mijaran › Val d'Aran | 1 |
| Forêt de la Vall de Boí (262) ⚠️ | la Vall de Boí › Alta Ribagorça | 1 |
| Forêt de Espot (38) ⚠️ | Espot › Pallars Sobirà | 1 |
| Forêt de Espot (39) ⚠️ | Espot › Pallars Sobirà | 1 |
| Forêt de Espot (43) ⚠️ | Espot › Pallars Sobirà | 1 |
| Forêt de Alt Àneu (54) ⚠️ | Alt Àneu › Pallars Sobirà | 1 |
| Forêt de Alt Àneu (63) ⚠️ | Alt Àneu › Pallars Sobirà | 1 |
| Forêt de Josa i Tuixén (15) ⚠️ | Josa i Tuixén › Alt Urgell | 1 |
| Forêt de Gósol (34) ⚠️ | Gósol › Berguedà (Lérida) | 1 |
| Forêt de Gósol (36) ⚠️ | Gósol › Berguedà (Lérida) | 1 |
| Forêt de Alins (34) ⚠️ | Alins › Pallars Sobirà | 1 |
| Forêt de Alins (35) ⚠️ | Alins › Pallars Sobirà | 1 |
| Forêt de Esterri de Cardós (2) ⚠️ | Esterri de Cardós › Pallars Sobirà | 1 |
| Forêt de Esterri de Cardós (5) ⚠️ | Alins › Pallars Sobirà | 1 |
| Forêt de la Coma i la Pedra (118) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de la Coma i la Pedra (120) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de la Coma i la Pedra (129) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de Pinós (108) ⚠️ | Pinós › Solsonès | 1 |
| Forêt de Pinós (122) ⚠️ | Pinós › Solsonès | 1 |
| Forêt de Riner (148) ⚠️ | Pinós › Solsonès | 1 |
| Forêt de Pinós (141) ⚠️ | Pinós › Solsonès | 1 |
| Forêt de Pinós (143) ⚠️ | Pinós › Solsonès | 1 |
| Forêt de Pinós (144) ⚠️ | Pinós › Solsonès | 1 |
| Forêt de Pinós (146) ⚠️ | Pinós › Solsonès | 1 |
| Forêt de Pinós (148) ⚠️ | Pinós › Solsonès | 1 |
| Forêt de Pinós (154) ⚠️ | Pinós › Solsonès | 1 |
| Forêt de Pinós (155) ⚠️ | Pinós › Solsonès | 1 |
| Forêt de Pinós (161) ⚠️ | Pinós › Solsonès | 1 |
| Forêt de Bellver de Cerdanya (31) ⚠️ | — | 1 |
| Forêt de Riu de Cerdanya (10) ⚠️ | Riu de Cerdanya › Cerdanya (Lérida) | 1 |
| Forêt de Bellver de Cerdanya (42) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 1 |
| Forêt de Navès (148) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Guixers (66) ⚠️ | Guixers › Solsonès | 1 |
| Forêt de Guixers (67) ⚠️ | Guixers › Solsonès | 1 |
| Forêt de Guixers (82) ⚠️ | Guixers › Solsonès | 1 |
| Forêt de Guixers (88) ⚠️ | Guixers › Solsonès | 1 |
| Forêt de Guixers (96) ⚠️ | Guixers › Solsonès | 1 |
| Forêt de Guixers (97) ⚠️ | Guixers › Solsonès | 1 |
| Forêt de Gósol (40) ⚠️ | Gósol › Berguedà (Lérida) | 1 |
| Forêt de la Coma i la Pedra (132) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de la Coma i la Pedra (142) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de la Coma i la Pedra (143) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de la Coma i la Pedra (145) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de Guixers (116) ⚠️ | Guixers › Solsonès | 1 |
| Forêt de la Coma i la Pedra (171) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de Gósol (67) ⚠️ | Gósol › Berguedà (Lérida) | 1 |
| Forêt de Gósol (74) ⚠️ | Gósol › Berguedà (Lérida) | 1 |
| Forêt de Gósol (76) ⚠️ | Gósol › Berguedà (Lérida) | 1 |
| Forêt de Gósol (79) ⚠️ | Gósol › Berguedà (Lérida) | 1 |
| Forêt de Gósol (80) ⚠️ | Gósol › Berguedà (Lérida) | 1 |
| Forêt de Guixers (118) ⚠️ | Guixers › Solsonès | 1 |
| Forêt de Guixers (120) ⚠️ | Guixers › Solsonès | 1 |
| Forêt de Gósol (96) ⚠️ | Gósol › Berguedà (Lérida) | 1 |
| Forêt de la Coma i la Pedra (173) ⚠️ | la Coma i la Pedra › Solsonès | 1 |
| Forêt de Sant Llorenç de Morunys (30) ⚠️ | Sant Llorenç de Morunys › Solsonès | 1 |
| Forêt de Guixers (123) ⚠️ | Guixers › Solsonès | 1 |
| Forêt de Navès (155) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Navès (157) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Guixers (126) ⚠️ | Guixers › Solsonès | 1 |
| Forêt de Navès (166) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Guixers (132) ⚠️ | Guixers › Solsonès | 1 |
| Forêt de Guixers (133) ⚠️ | Guixers › Solsonès | 1 |
| Forêt de Guixers (135) ⚠️ | Guixers › Solsonès | 1 |
| Forêt de Odèn (62) ⚠️ | Odèn › Solsonès | 1 |
| Forêt de Odèn (63) ⚠️ | Odèn › Solsonès | 1 |
| Forêt de Guixers (137) ⚠️ | Guixers › Solsonès | 1 |
| Forêt de Odèn (66) ⚠️ | Odèn › Solsonès | 1 |
| Forêt de Odèn (67) ⚠️ | Odèn › Solsonès | 1 |
| Forêt de Odèn (77) ⚠️ | Odèn › Solsonès | 1 |
| Forêt de Odèn (84) ⚠️ | Odèn › Solsonès | 1 |
| Forêt de Odèn (88) ⚠️ | Odèn › Solsonès | 1 |
| Forêt de Odèn (89) ⚠️ | Odèn › Solsonès | 1 |
| Forêt de Odèn (97) ⚠️ | Odèn › Solsonès | 1 |
| Forêt de Guixers (146) ⚠️ | Guixers › Solsonès | 1 |
| Forêt de Guixers (148) ⚠️ | Guixers › Solsonès | 1 |
| Forêt de Guixers (149) ⚠️ | Guixers › Solsonès | 1 |
| Forêt de Navès (169) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Lladurs (195) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Navès (171) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Lladurs (198) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Guixers (153) ⚠️ | Guixers › Solsonès | 1 |
| Forêt de Guixers (155) ⚠️ | Guixers › Solsonès | 1 |
| Forêt de Lladurs (205) ⚠️ | Odèn › Solsonès | 1 |
| Forêt de Navès (172) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Lladurs (206) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Odèn (111) ⚠️ | Odèn › Solsonès | 1 |
| Forêt de Odèn (119) ⚠️ | Odèn › Solsonès | 1 |
| Forêt de Lladurs (212) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Odèn (120) ⚠️ | Odèn › Solsonès | 1 |
| Forêt de Lladurs (227) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (232) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (234) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (237) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (238) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (241) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (245) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (248) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (250) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Lladurs (252) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Odèn (124) ⚠️ | Odèn › Solsonès | 1 |
| Forêt de Bellver de Cerdanya (49) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 1 |
| Forêt de Bellver de Cerdanya (50) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 1 |
| Forêt de Bellver de Cerdanya (53) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 1 |
| Forêt de Montellà i Martinet (37) ⚠️ | Montellà i Martinet › Cerdanya (Lérida) | 1 |
| Forêt de Bellver de Cerdanya (57) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 1 |
| Forêt de Naut Aran (90) ⚠️ | Naut Aran › Val d'Aran | 1 |
| Forêt de Alt Àneu (87) ⚠️ | Alt Àneu › Pallars Sobirà | 1 |
| Forêt de Alt Àneu (91) ⚠️ | Alt Àneu › Pallars Sobirà | 1 |
| Forêt de Alt Àneu (97) ⚠️ | Alt Àneu › Pallars Sobirà | 1 |
| Forêt de Alt Àneu (99) ⚠️ | Alt Àneu › Pallars Sobirà | 1 |
| Forêt de Alt Àneu (103) ⚠️ | Alt Àneu › Pallars Sobirà | 1 |
| Forêt de Alt Àneu (110) ⚠️ | Alt Àneu › Pallars Sobirà | 1 |
| Forêt de Alt Àneu (113) ⚠️ | Alt Àneu › Pallars Sobirà | 1 |
| Forêt de Alt Àneu (138) ⚠️ | Alt Àneu › Pallars Sobirà | 1 |
| Forêt de Naut Aran (113) ⚠️ | Naut Aran › Val d'Aran | 1 |
| Forêt de Naut Aran (119) ⚠️ | Naut Aran › Val d'Aran | 1 |
| Forêt de Naut Aran (120) ⚠️ | Naut Aran › Val d'Aran | 1 |
| Forêt de Naut Aran (121) ⚠️ | Naut Aran › Val d'Aran | 1 |
| Forêt de Canejan (18) ⚠️ | Canejan › Val d'Aran | 1 |
| Forêt de Canejan (19) ⚠️ | Canejan › Val d'Aran | 1 |
| Forêt de Canejan (20) ⚠️ | Canejan › Val d'Aran | 1 |
| Forêt de Naut Aran (125) ⚠️ | Naut Aran › Val d'Aran | 1 |
| Forêt de Naut Aran (126) ⚠️ | Naut Aran › Val d'Aran | 1 |
| Forêt de Naut Aran (135) ⚠️ | Naut Aran › Val d'Aran | 1 |
| Forêt de Naut Aran (142) ⚠️ | Naut Aran › Val d'Aran | 1 |
| Forêt de Naut Aran (144) ⚠️ | Naut Aran › Val d'Aran | 1 |
| Forêt de Naut Aran (145) ⚠️ | Naut Aran › Val d'Aran | 1 |
| Forêt de Alt Àneu (154) ⚠️ | Alt Àneu › Pallars Sobirà | 1 |
| Forêt de Canejan (30) ⚠️ | Canejan › Val d'Aran | 1 |
| Forêt de Lladorre (36) ⚠️ | Lladorre › Pallars Sobirà | 1 |
| Forêt de Llavorsí (34) ⚠️ | Llavorsí › Pallars Sobirà | 1 |
| Forêt de Llavorsí (48) ⚠️ | Llavorsí › Pallars Sobirà | 1 |
| Forêt de Es Bòrdes (11) ⚠️ | Es Bòrdes › Val d'Aran | 1 |
| Forêt de Es Bòrdes (12) ⚠️ | Es Bòrdes › Val d'Aran | 1 |
| Forêt de Vielha e Mijaran (76) ⚠️ | Vielha e Mijaran › Val d'Aran | 1 |
| Forêt de Vielha e Mijaran (79) ⚠️ | Vielha e Mijaran › Val d'Aran | 1 |
| Forêt de les Valls de Valira (38) ⚠️ | les Valls de Valira › Alt Urgell | 1 |
| Forêt de les Valls de Valira (50) ⚠️ | les Valls de Valira › Alt Urgell | 1 |
| Forêt de les Valls de Valira (53) ⚠️ | les Valls de Valira › Alt Urgell | 1 |
| Forêt de les Valls de Valira (57) ⚠️ | les Valls de Valira › Alt Urgell | 1 |
| Forêt de Vilaller (39) ⚠️ | Vilaller › Alta Ribagorça | 1 |
| Forêt de Vilaller (40) ⚠️ | Vilaller › Alta Ribagorça | 1 |
| Forêt de Vilaller (42) ⚠️ | Vilaller › Alta Ribagorça | 1 |
| Forêt de Vilaller (51) ⚠️ | Vilaller › Alta Ribagorça | 1 |
| Forêt de Vilaller (58) ⚠️ | Vilaller › Alta Ribagorça | 1 |
| Forêt de el Pont de Bar (7) ⚠️ | el Pont de Bar › Alt Urgell | 1 |
| Forêt de Bellver de Cerdanya (60) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 1 |
| Forêt de Bellver de Cerdanya (64) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 1 |
| Forêt de les Valls de Valira (65) ⚠️ | les Valls de Valira › Alt Urgell | 1 |
| Forêt de les Valls de Valira (70) ⚠️ | les Valls de Valira › Alt Urgell | 1 |
| Forêt de les Valls de Valira (76) ⚠️ | les Valls de Valira › Alt Urgell | 1 |
| Forêt de les Valls de Valira (91) ⚠️ | les Valls de Valira › Alt Urgell | 1 |
| Forêt de les Valls de Valira (104) ⚠️ | les Valls de Valira › Alt Urgell | 1 |
| Forêt de les Valls de Valira (106) ⚠️ | les Valls de Valira › Alt Urgell | 1 |
| Forêt de les Valls de Valira (109) ⚠️ | les Valls de Valira › Alt Urgell | 1 |
| Forêt de la Seu d'Urgell (14) ⚠️ | la Seu d'Urgell › Alt Urgell | 1 |
| Forêt de Ribera d'Urgellet (42) ⚠️ | Ribera d'Urgellet › Alt Urgell | 1 |
| Forêt de Ribera d'Urgellet (46) ⚠️ | Ribera d'Urgellet › Alt Urgell | 1 |
| Forêt de Montferrer i Castellbò (58) ⚠️ | Montferrer i Castellbò › Alt Urgell | 1 |
| Forêt de Montferrer i Castellbò (59) ⚠️ | Montferrer i Castellbò › Alt Urgell | 1 |
| Forêt de Montferrer i Castellbò (60) ⚠️ | Montferrer i Castellbò › Alt Urgell | 1 |
| Forêt de Montferrer i Castellbò (69) ⚠️ | Montferrer i Castellbò › Alt Urgell | 1 |
| Forêt de Montferrer i Castellbò (71) ⚠️ | Montferrer i Castellbò › Alt Urgell | 1 |
| Forêt de Montferrer i Castellbò (73) ⚠️ | Montferrer i Castellbò › Alt Urgell | 1 |
| Forêt de la Seu d'Urgell (18) ⚠️ | la Seu d'Urgell › Alt Urgell | 1 |
| Forêt de Oliana (10) ⚠️ | Oliana › Alt Urgell | 1 |
| Forêt de Oliana (18) ⚠️ | Oliana › Alt Urgell | 1 |
| Forêt de Oliana (19) ⚠️ | Oliana › Alt Urgell | 1 |
| Forêt de Oliana (21) ⚠️ | Oliana › Alt Urgell | 1 |
| Forêt de Oliana (22) ⚠️ | Oliana › Alt Urgell | 1 |
| Forêt de Oliana (23) ⚠️ | Oliana › Alt Urgell | 1 |
| Forêt de Oliana (24) ⚠️ | Oliana › Alt Urgell | 1 |
| Forêt de Oliana (26) ⚠️ | Oliana › Alt Urgell | 1 |
| Forêt de Cabó (16) ⚠️ | Cabó › Alt Urgell | 1 |
| Forêt de Cabó (40) ⚠️ | Cabó › Alt Urgell | 1 |
| Forêt de Cabó (43) ⚠️ | Cabó › Alt Urgell | 1 |
| Forêt de Coll de Nargó (89) ⚠️ | Coll de Nargó › Alt Urgell | 1 |
| Forêt de Bassella (28) ⚠️ | Bassella › Alt Urgell | 1 |
| Forêt de Bassella (30) ⚠️ | Bassella › Alt Urgell | 1 |
| Forêt de Bassella (34) ⚠️ | Bassella › Alt Urgell | 1 |
| Forêt de Josa i Tuixén (36) ⚠️ | Josa i Tuixén › Alt Urgell | 1 |
| Forêt de Josa i Tuixén (39) ⚠️ | Josa i Tuixén › Alt Urgell | 1 |
| Forêt de Josa i Tuixén (40) ⚠️ | Josa i Tuixén › Alt Urgell | 1 |
| Forêt de Josa i Tuixén (41) ⚠️ | Josa i Tuixén › Alt Urgell | 1 |
| Forêt de Josa i Tuixén (51) ⚠️ | Josa i Tuixén › Alt Urgell | 1 |
| Forêt de Josa i Tuixén (52) ⚠️ | Josa i Tuixén › Alt Urgell | 1 |
| Forêt de Josa i Tuixén (53) ⚠️ | Josa i Tuixén › Alt Urgell | 1 |
| Forêt de Montellà i Martinet (42) ⚠️ | Montellà i Martinet › Cerdanya (Lérida) | 1 |
| Forêt de Bellver de Cerdanya (71) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 1 |
| Forêt de Riu de Cerdanya (20) ⚠️ | Riu de Cerdanya › Cerdanya (Lérida) | 1 |
| Forêt de Bellver de Cerdanya (73) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 1 |
| Forêt de Riu de Cerdanya (23) ⚠️ | Riu de Cerdanya › Cerdanya (Lérida) | 1 |
| Forêt de Riu de Cerdanya (26) ⚠️ | Riu de Cerdanya › Cerdanya (Lérida) | 1 |
| Forêt de Josa i Tuixén (62) ⚠️ | Josa i Tuixén › Alt Urgell | 1 |
| Forêt de Gósol (111) ⚠️ | Gósol › Berguedà (Lérida) | 1 |
| Forêt de Tremp (81) ⚠️ | Tremp › Pallars Jussà | 1 |
| Forêt de Tremp (86) ⚠️ | Tremp › Pallars Jussà | 1 |
| Forêt de Navès (176) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Olius (331) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Navès (181) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Navès (182) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Navès (187) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Navès (190) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Navès (193) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Olius (337) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Navès (200) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Navès (206) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Navès (209) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Navès (212) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Navès (213) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Clariana de Cardener (169) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Forêt de Lladurs (263) ⚠️ | Lladurs › Solsonès | 1 |
| Forêt de Bellver de Cerdanya (77) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 1 |
| Forêt de Bellver de Cerdanya (80) ⚠️ | Bellver de Cerdanya › Cerdanya (Lérida) | 1 |
| Forêt de Peramola (29) ⚠️ | Peramola › Alt Urgell | 1 |
| Forêt de Peramola (35) ⚠️ | Peramola › Alt Urgell | 1 |
| Forêt de Peramola (36) ⚠️ | Peramola › Alt Urgell | 1 |
| Forêt de Peramola (41) ⚠️ | Peramola › Alt Urgell | 1 |
| Forêt de Coll de Nargó (98) ⚠️ | Coll de Nargó › Alt Urgell | 1 |
| Forêt de Solsona (135) ⚠️ | Solsona › Solsonès | 1 |
| Forêt de Olius (353) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (357) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Olius (358) ⚠️ | Olius › Solsonès | 1 |
| Forêt de Soriguera (41) ⚠️ | Soriguera › Pallars Sobirà | 1 |
| Forêt de Llimiana (9) ⚠️ | Llimiana › Pallars Jussà | 1 |
| Forêt de Castell de Mur (13) ⚠️ | Castell de Mur › Pallars Jussà | 1 |
| Forêt de Àger (38) ⚠️ | Àger › Noguera | 1 |
| Forêt de Àger (50) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 1 |
| Forêt de Sant Esteve de la Sarga (12) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 1 |
| Forêt de Sant Esteve de la Sarga (17) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 1 |
| Forêt de Sant Esteve de la Sarga (28) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 1 |
| Forêt de Àger (58) ⚠️ | Àger › Noguera | 1 |
| Forêt de Baix Pallars (41) ⚠️ | Baix Pallars › Pallars Sobirà | 1 |
| Forêt de Baix Pallars (52) ⚠️ | Baix Pallars › Pallars Sobirà | 1 |
| Forêt de Baix Pallars (57) ⚠️ | Baix Pallars › Pallars Sobirà | 1 |
| Forêt de Baix Pallars (62) ⚠️ | Baix Pallars › Pallars Sobirà | 1 |
| Forêt de Baix Pallars (63) ⚠️ | Baix Pallars › Pallars Sobirà | 1 |
| Forêt de Baix Pallars (64) ⚠️ | Baix Pallars › Pallars Sobirà | 1 |
| Forêt de Navès (221) ⚠️ | Navès › Solsonès | 1 |
| Forêt de Clariana de Cardener (189) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Forêt de Clariana de Cardener (197) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Forêt de Clariana de Cardener (201) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Forêt de Clariana de Cardener (203) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Forêt de Clariana de Cardener (212) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Forêt de Clariana de Cardener (213) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Forêt de Clariana de Cardener (216) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Forêt de Clariana de Cardener (221) ⚠️ | Clariana de Cardener › Solsonès | 1 |
| Forêt de Llobera (485) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Castell de Mur (18) ⚠️ | Castell de Mur › Pallars Jussà | 1 |
| Forêt de Castell de Mur (20) ⚠️ | Castell de Mur › Pallars Jussà | 1 |
| Forêt de Castell de Mur (24) ⚠️ | Castell de Mur › Pallars Jussà | 1 |
| Forêt de Castell de Mur (25) ⚠️ | Castell de Mur › Pallars Jussà | 1 |
| Forêt de Àger (62) ⚠️ | Àger › Noguera | 1 |
| Forêt de Àger (63) ⚠️ | Camarasa › Noguera | 1 |
| Forêt de Àger (66) ⚠️ | Àger › Noguera | 1 |
| Forêt de Àger (70) ⚠️ | Àger › Noguera | 1 |
| Forêt de Sant Esteve de la Sarga (38) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 1 |
| Forêt de Sant Esteve de la Sarga (41) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 1 |
| Forêt de Sant Esteve de la Sarga (46) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 1 |
| Forêt de Sant Esteve de la Sarga (50) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 1 |
| Forêt de Sant Esteve de la Sarga (51) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 1 |
| Forêt de Àger (78) ⚠️ | Àger › Noguera | 1 |
| Forêt de Sant Esteve de la Sarga (73) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 1 |
| Forêt de Sant Esteve de la Sarga (74) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 1 |
| Forêt de Sant Esteve de la Sarga (75) ⚠️ | Sant Esteve de la Sarga › Pallars Jussà | 1 |
| Forêt de Castell de Mur (32) ⚠️ | Castell de Mur › Pallars Jussà | 1 |
| Forêt de Àger (98) ⚠️ | Àger › Noguera | 1 |
| Forêt de Llobera (493) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Àger (99) ⚠️ | Àger › Noguera | 1 |
| Forêt de Àger (102) ⚠️ | Àger › Noguera | 1 |
| Forêt de Àger (114) ⚠️ | Àger › Noguera | 1 |
| Forêt de Àger (115) ⚠️ | Àger › Noguera | 1 |
| Forêt de Àger (116) ⚠️ | Àger › Noguera | 1 |
| Forêt de Àger (119) ⚠️ | Àger › Noguera | 1 |
| Forêt de Àger (121) ⚠️ | Àger › Noguera | 1 |
| Forêt de Àger (132) ⚠️ | Àger › Noguera | 1 |
| Forêt de Àger (134) ⚠️ | Àger › Noguera | 1 |
| Forêt de Àger (140) ⚠️ | Àger › Noguera | 1 |
| Forêt de Àger (141) ⚠️ | Àger › Noguera | 1 |
| Forêt de Àger (143) ⚠️ | Àger › Noguera | 1 |
| Forêt de Àger (144) ⚠️ | Àger › Noguera | 1 |
| Forêt de Àger (146) ⚠️ | Àger › Noguera | 1 |
| Forêt de Àger (150) ⚠️ | Àger › Noguera | 1 |
| Forêt de Àger (156) ⚠️ | Àger › Noguera | 1 |
| Forêt de Àger (172) ⚠️ | Àger › Noguera | 1 |
| Forêt de Àger (173) ⚠️ | Àger › Noguera | 1 |
| Forêt de Os de Balaguer (33) ⚠️ | Os de Balaguer › Noguera | 1 |
| Forêt de Os de Balaguer (43) ⚠️ | Os de Balaguer › Noguera | 1 |
| Forêt de Llobera (494) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Ivars de Noguera (10) ⚠️ | Ivars de Noguera › Noguera | 1 |
| Forêt de Algerri (5) ⚠️ | Algerri › Noguera | 1 |
| Forêt de Algerri (7) ⚠️ | Algerri › Noguera | 1 |
| Forêt de Os de Balaguer (80) ⚠️ | Os de Balaguer › Noguera | 1 |
| Forêt de Abella de la Conca (16) ⚠️ | Abella de la Conca › Pallars Jussà | 1 |
| Forêt de Abella de la Conca (21) ⚠️ | Abella de la Conca › Pallars Jussà | 1 |
| Forêt de Abella de la Conca (25) ⚠️ | Abella de la Conca › Pallars Jussà | 1 |
| Forêt de Coll de Nargó (112) ⚠️ | Coll de Nargó › Alt Urgell | 1 |
| Forêt de Coll de Nargó (120) ⚠️ | Coll de Nargó › Alt Urgell | 1 |
| Forêt de Abella de la Conca (36) ⚠️ | Abella de la Conca › Pallars Jussà | 1 |
| Forêt de Abella de la Conca (50) ⚠️ | Abella de la Conca › Pallars Jussà | 1 |
| Forêt de Abella de la Conca (59) ⚠️ | Abella de la Conca › Pallars Jussà | 1 |
| Forêt de Abella de la Conca (71) ⚠️ | Abella de la Conca › Pallars Jussà | 1 |
| Forêt de Conca de Dalt (37) ⚠️ | Conca de Dalt › Pallars Jussà | 1 |
| Forêt de Abella de la Conca (82) ⚠️ | Abella de la Conca › Pallars Jussà | 1 |
| Forêt de Cabó (49) ⚠️ | Cabó › Alt Urgell | 1 |
| Forêt de la Pobla de Segur (17) ⚠️ | la Pobla de Segur › Pallars Jussà | 1 |
| Forêt de la Pobla de Segur (20) ⚠️ | la Pobla de Segur › Pallars Jussà | 1 |
| Forêt de Baix Pallars (67) ⚠️ | Baix Pallars › Pallars Sobirà | 1 |
| Forêt de Baix Pallars (74) ⚠️ | Baix Pallars › Pallars Sobirà | 1 |
| Forêt de Àger (174) ⚠️ | Àger › Noguera | 1 |
| Forêt de Àger (175) ⚠️ | Àger › Noguera | 1 |
| Forêt de Àger (179) ⚠️ | Àger › Noguera | 1 |
| Forêt de Tremp (98) ⚠️ | Tremp › Pallars Jussà | 1 |
| Forêt de Tremp (105) ⚠️ | Tremp › Pallars Jussà | 1 |
| Forêt de Llobera (497) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Tremp (114) ⚠️ | Tremp › Pallars Jussà | 1 |
| Forêt de el Pont de Suert (50) ⚠️ | el Pont de Suert › Alta Ribagorça | 1 |
| Forêt de el Pont de Suert (53) ⚠️ | el Pont de Suert › Alta Ribagorça | 1 |
| Forêt de el Pont de Suert (59) ⚠️ | el Pont de Suert › Alta Ribagorça | 1 |
| Forêt de el Pont de Suert (64) ⚠️ | el Pont de Suert › Alta Ribagorça | 1 |
| Forêt de el Pont de Suert (67) ⚠️ | el Pont de Suert › Alta Ribagorça | 1 |
| Forêt de el Pont de Suert (74) ⚠️ | el Pont de Suert › Alta Ribagorça | 1 |
| Forêt de el Pont de Suert (79) ⚠️ | el Pont de Suert › Alta Ribagorça | 1 |
| Forêt de el Pont de Suert (82) ⚠️ | el Pont de Suert › Alta Ribagorça | 1 |
| Forêt de el Pont de Suert (94) ⚠️ | el Pont de Suert › Alta Ribagorça | 1 |
| Forêt de el Pont de Suert (95) ⚠️ | el Pont de Suert › Alta Ribagorça | 1 |
| Forêt de el Pont de Suert (101) ⚠️ | el Pont de Suert › Alta Ribagorça | 1 |
| Forêt de Llobera (500) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Navès (222) ⚠️ | Navès › Solsonès | 1 |
| Bois de la Torre de Cabdella (45) ⚠️ | la Torre de Cabdella › Pallars Jussà | 1 |
| Bois de la Torre de Cabdella (46) ⚠️ | la Torre de Cabdella › Pallars Jussà | 1 |
| Forêt de Farrera (14) ⚠️ | Farrera › Pallars Sobirà | 1 |
| Forêt de Ribera d'Urgellet (58) ⚠️ | Ribera d'Urgellet › Alt Urgell | 1 |
| Forêt de Talarn (7) ⚠️ | Talarn › Pallars Jussà | 1 |
| Forêt de Tremp (125) ⚠️ | Tremp › Pallars Jussà | 1 |
| Forêt de Tremp (130) ⚠️ | Tremp › Pallars Jussà | 1 |
| Forêt de Tírvia (9) ⚠️ | Tírvia › Pallars Sobirà | 1 |
| Forêt de Llobera (505) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (506) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (509) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (510) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (515) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Lleida (24) ⚠️ | Lleida › Segrià | 1 |
| Forêt de Llobera (531) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (532) ⚠️ | Llobera › Solsonès | 1 |
| Forêt de Llobera (533) ⚠️ | Llobera › Solsonès | 1 |
| Parc del Pinell ⚠️ | Tremp › Pallars Jussà | 1 |
| Parc de Tremp (2) ⚠️ | Tremp › Pallars Jussà | 1 |
| Passeig Mercè Ros ⚠️ | Agramunt › Urgell | 1 |
| Parc de Josep Brufau ⚠️ | Agramunt › Urgell | 1 |
| Forêt de Alins (110) ⚠️ | Alins › Pallars Sobirà | 1 |
| Forêt de Alins (111) ⚠️ | Alins › Pallars Sobirà | 1 |
| Forêt de Alins (115) ⚠️ | Alins › Pallars Sobirà | 1 |
| Forêt de la Guingueta d'Àneu (82) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 1 |
| Forêt de la Guingueta d'Àneu (85) ⚠️ | la Guingueta d'Àneu › Pallars Sobirà | 1 |
| Forêt de Lleida (26) ⚠️ | Lleida › Segrià | 1 |
| Forêt de Lleida (28) ⚠️ | Lleida › Segrià | 1 |
| Forêt de Lleida (30) ⚠️ | Lleida › Segrià | 1 |
| Forêt de Vila-sana (4) ⚠️ | Vila-sana › Pla d'Urgell | 1 |
| Forêt de Vielha e Mijaran (89) ⚠️ | Vielha e Mijaran › Val d'Aran | 1 |
| Forêt de Espot (49) ⚠️ | Espot › Pallars Sobirà | 1 |
| Forêt de Espot (55) ⚠️ | Espot › Pallars Sobirà | 1 |
| Forêt de el Pont de Bar (20) ⚠️ | el Pont de Bar › Alt Urgell | 1 |
| Forêt de Montellà i Martinet (53) ⚠️ | Montellà i Martinet › Cerdanya (Lérida) | 1 |
| Forêt de el Pont de Bar (48) ⚠️ | el Pont de Bar › Alt Urgell | 1 |
| Forêt de la Granja d'Escarp (10) ⚠️ | la Granja d'Escarp › Segrià | 1 |
| Forêt de Almatret (13) ⚠️ | Almatret › Segrià | 1 |
| Forêt de Almatret (19) ⚠️ | Almatret › Segrià | 1 |
| Forêt de el Pont de Bar (55) ⚠️ | el Pont de Bar › Alt Urgell | 1 |
| Forêt de Alàs i Cerc (29) ⚠️ | Alàs i Cerc › Alt Urgell | 1 |
| Forêt de Alàs i Cerc (30) ⚠️ | Alàs i Cerc › Alt Urgell | 1 |
| Bois de Alàs i Cerc (6) ⚠️ | Alàs i Cerc › Alt Urgell | 1 |
| Forêt de Montferrer i Castellbò (101) ⚠️ | Montferrer i Castellbò › Alt Urgell | 1 |
| Forêt de Montferrer i Castellbò (111) ⚠️ | Montferrer i Castellbò › Alt Urgell | 1 |
| Forêt de Montferrer i Castellbò (117) ⚠️ | Montferrer i Castellbò › Alt Urgell | 1 |
| Forêt de la Seu d'Urgell (24) ⚠️ | la Seu d'Urgell › Alt Urgell | 1 |
| Forêt de la Pobla de Segur (31) ⚠️ | la Pobla de Segur › Pallars Jussà | 1 |
| Forêt de Conca de Dalt (55) ⚠️ | Conca de Dalt › Pallars Jussà | 1 |
| Forêt de Senterada (16) ⚠️ | Senterada › Pallars Jussà | 1 |
| Forêt de Sort (29) ⚠️ | Sort › Pallars Sobirà | 1 |
| Forêt de Sort (30) ⚠️ | Sort › Pallars Sobirà | 1 |
| Forêt de Sort (31) ⚠️ | Sort › Pallars Sobirà | 1 |
| Forêt de Torres de Segre (11) ⚠️ | Torres de Segre › Segrià | 1 |
| Forêt de Torres de Segre (13) ⚠️ | Torres de Segre › Segrià | 1 |
| Forêt de Torres de Segre (16) ⚠️ | Aitona › Segrià | 1 |
| Forêt de Torres de Segre (18) ⚠️ | Aitona › Segrià | 1 |
| Forêt de Torres de Segre (25) ⚠️ | Torres de Segre › Segrià | 1 |
| Forêt de Torres de Segre (30) ⚠️ | Torres de Segre › Segrià | 1 |
| Forêt de Vall de Cardós (60) ⚠️ | Vall de Cardós › Pallars Sobirà | 1 |
| Forêt de Vall de Cardós (62) ⚠️ | Vall de Cardós › Pallars Sobirà | 1 |
| Forêt de Sort (34) ⚠️ | Sort › Pallars Sobirà | 1 |
| Forêt de Rialp (31) ⚠️ | Rialp › Pallars Sobirà | 1 |
| Forêt de la Vall de Boí (288) ⚠️ | la Vall de Boí › Alta Ribagorça | 1 |
| Forêt de la Vall de Boí (289) ⚠️ | la Vall de Boí › Alta Ribagorça | 1 |
| Forêt de les Valls de Valira (153) ⚠️ | les Valls de Valira › Alt Urgell | 1 |
| Forêt de Soriguera (51) ⚠️ | Soriguera › Pallars Sobirà | 1 |

2 952 parc(s) plus petits qu'une cellule ne sont pas listés : la carte les dessine, mais ils n'offrent aucune cellule.

⚠️ 6193 parc(s) hors de la fenêtre 10–125 cellules (5889 trop petit(s), 304 trop grand(s)) : affichés sur la carte, mais ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| airport | 94 |
| military | 40 |
| prison | 0 |
| **Total déclaré** | **134** |
| dont dans une zone de ce territoire | 134 |


### Zones concernées

| Zone | Cellules exclues |
|---|---:|
| Alguaire | 83 |
| Talarn | 27 |
| Tremp | 13 |
| Ribera d'Urgellet | 8 |
| Cervera | 3 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
