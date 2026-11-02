# Communauté de Madrid

Pack `es-madrid` · version 1.0.0 · grille 200 m · Espagne › Communauté de Madrid

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 344 180 |
| dont restreintes (aéroport, militaire, prison) | 4 691 |
| dont sans chemin (aucune voie à moins de 60 m) | 62 254 |
| dont en forêt, sans chemin non plus | 18 895 |
| dont traversées par un cours d'eau, sans chemin non plus | 7 031 |
| Cellules retirées par le masque d'eau | 3 223 |
| Villes | 181 |
| Arrondissements et quartiers | 21 |
| Îles | 0 |
| Parcs | 9 118 |

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

## Villes (181)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Sans chemin | Parcs |
|---|---:|---:|---:|---:|---:|---:|---:|
| Madrid | 26 131 | 252 | 25 879 | 1 310 | **24 569** | 559 (2 %) | 2502 |
| Colmenar Viejo | 7 952 | 6 | 7 946 | 71 | **7 875** | 1 862 (24 %) | 89 |
| Aranjuez | 8 031 | 127 | 7 904 | 8 | **7 896** | 2 628 (33 %) | 293 |
| Rascafría | 6 536 | 5 | 6 531 | 0 | **6 531** | 1 014 (16 %) | 24 |
| Colmenar de Oreja | 5 411 | 4 | 5 407 | 0 | **5 407** | 1 171 (22 %) | 20 |
| Manzanares el Real | 5 574 | 405 | 5 169 | 41 | **5 128** | 934 (18 %) | 41 |
| Villarejo de Salvanés | 5 080 | 0 | 5 080 | 0 | **5 080** | 1 535 (30 %) | 9 |
| Chinchón | 4 990 | 7 | 4 983 | 0 | **4 983** | 853 (17 %) | 17 |
| San Martín de Valdeiglesias | 4 970 | 242 | 4 728 | 0 | **4 728** | 326 (7 %) | 48 |
| San Martín de la Vega | 4 517 | 50 | 4 467 | 311 | **4 156** | 1 024 (25 %) | 52 |
| Navalcarnero | 4 318 | 0 | 4 318 | 10 | **4 308** | 875 (20 %) | 37 |
| Robledo de Chavela | 4 020 | 0 | 4 020 | 0 | **4 020** | 623 (15 %) | 81 |
| Valdemorillo | 4 058 | 207 | 3 851 | 4 | **3 847** | 181 (5 %) | 115 |
| Alcalá de Henares | 3 783 | 17 | 3 766 | 149 | **3 617** | 429 (12 %) | 188 |
| Arganda del Rey | 3 445 | 16 | 3 429 | 0 | **3 429** | 595 (17 %) | 69 |
| Estremera | 3 392 | 0 | 3 392 | 7 | **3 385** | 1 353 (40 %) | 7 |
| Getafe | 3 378 | 20 | 3 358 | 185 | **3 173** | 439 (14 %) | 272 |
| Villa del Prado | 3 374 | 20 | 3 354 | 0 | **3 354** | 325 (10 %) | 44 |
| Santa María de la Alameda | 3 279 | 3 | 3 276 | 0 | **3 276** | 697 (21 %) | 68 |
| Navalagamella | 3 283 | 8 | 3 275 | 7 | **3 268** | 581 (18 %) | 26 |
| El Escorial | 2 990 | 48 | 2 942 | 0 | **2 942** | 288 (10 %) | 93 |
| Villaviciosa de Odón | 2 929 | 5 | 2 924 | 0 | **2 924** | 245 (8 %) | 66 |
| Cenicientos | 2 905 | 0 | 2 905 | 0 | **2 905** | 712 (25 %) | 16 |
| Galapagar | 2 823 | 8 | 2 815 | 0 | **2 815** | 326 (12 %) | 109 |
| Rivas-Vaciamadrid | 2 932 | 168 | 2 764 | 0 | **2 764** | 309 (11 %) | 231 |
| Valdemoro | 2 747 | 1 | 2 746 | 7 | **2 739** | 512 (19 %) | 85 |
| Valdaracete | 2 741 | 0 | 2 741 | 0 | **2 741** | 1 023 (37 %) | 8 |
| Villamanta | 2 721 | 1 | 2 720 | 0 | **2 720** | 504 (19 %) | 10 |
| Campo Real | 2 662 | 0 | 2 662 | 0 | **2 662** | 911 (34 %) | 5 |
| Pinto | 2 664 | 3 | 2 661 | 0 | **2 661** | 716 (27 %) | 88 |
| Fuentidueña de Tajo | 2 597 | 0 | 2 597 | 0 | **2 597** | 967 (37 %) |  |
| San Sebastián de los Reyes | 2 557 | 8 | 2 549 | 85 | **2 464** | 302 (12 %) | 156 |
| Puebla de la Sierra | 2 536 | 0 | 2 536 | 0 | **2 536** | 512 (20 %) | 12 |
| Las Rozas de Madrid | 2 535 | 4 | 2 531 | 0 | **2 531** | 36 (1 %) | 143 |
| Guadalix de la Sierra | 2 664 | 139 | 2 525 | 0 | **2 525** | 819 (32 %) | 15 |
| Bustarviejo | 2 514 | 0 | 2 514 | 0 | **2 514** | 517 (21 %) | 11 |
| Miraflores de la Sierra | 2 475 | 3 | 2 472 | 0 | **2 472** | 408 (17 %) | 26 |
| Puentes Viejas | 2 574 | 109 | 2 465 | 0 | **2 465** | 510 (21 %) | 4 |
| San Lorenzo de El Escorial | 2 452 | 4 | 2 448 | 0 | **2 448** | 168 (7 %) | 60 |
| Guadarrama | 2 470 | 27 | 2 443 | 0 | **2 443** | 147 (6 %) | 76 |
| Lozoya | 2 552 | 158 | 2 394 | 0 | **2 394** | 427 (18 %) | 9 |
| Canencia | 2 303 | 0 | 2 303 | 0 | **2 303** | 617 (27 %) | 6 |
| Lozoyuela-Navas-Sieteiglesias | 2 258 | 0 | 2 258 | 0 | **2 258** | 457 (20 %) | 3 |
| Valdemaqueda | 2 255 | 0 | 2 255 | 0 | **2 255** | 207 (9 %) | 32 |
| Torrejón de Velasco | 2 240 | 0 | 2 240 | 0 | **2 240** | 556 (25 %) | 11 |
| Aldea del Fresno | 2 223 | 25 | 2 198 | 0 | **2 198** | 196 (9 %) | 16 |
| El Molar | 2 188 | 0 | 2 188 | 0 | **2 188** | 500 (23 %) | 11 |
| Colmenar del Arroyo | 2 176 | 2 | 2 174 | 0 | **2 174** | 359 (17 %) | 40 |
| Navas del Rey | 2 188 | 18 | 2 170 | 0 | **2 170** | 174 (8 %) | 14 |
| Brunete | 2 107 | 0 | 2 107 | 0 | **2 107** | 426 (20 %) | 18 |
| Perales de Tajuña | 2 101 | 0 | 2 101 | 0 | **2 101** | 481 (23 %) | 2 |
| Ciempozuelos | 2 113 | 23 | 2 090 | 0 | **2 090** | 404 (19 %) | 30 |
| Cadalso de los Vidrios | 2 050 | 3 | 2 047 | 0 | **2 047** | 346 (17 %) | 6 |
| Carabaña | 2 045 | 0 | 2 045 | 1 | **2 044** | 773 (38 %) |  |
| Boadilla del Monte | 2 040 | 5 | 2 035 | 0 | **2 035** | 12 (1 %) | 156 |
| Alcobendas | 1 973 | 2 | 1 971 | 470 | **1 501** | 81 (5 %) | 135 |
| Hoyo de Manzanares | 1 970 | 2 | 1 968 | 260 | **1 708** | 17 (1 %) | 45 |
| Morata de Tajuña | 1 944 | 0 | 1 944 | 0 | **1 944** | 415 (21 %) | 12 |
| Móstoles | 1 944 | 6 | 1 938 | 0 | **1 938** | 244 (13 %) | 181 |
| Loeches | 1 908 | 0 | 1 908 | 0 | **1 908** | 495 (26 %) | 28 |
| Brea de Tajo | 1 902 | 0 | 1 902 | 0 | **1 902** | 597 (31 %) | 12 |
| Paracuellos de Jarama | 1 911 | 9 | 1 902 | 48 | **1 854** | 211 (11 %) | 92 |
| Moralzarzal | 1 897 | 0 | 1 897 | 484 | **1 413** | 155 (11 %) | 34 |
| Daganzo de Arriba | 1 896 | 0 | 1 896 | 0 | **1 896** | 882 (47 %) | 22 |
| Torrelaguna | 1 886 | 2 | 1 884 | 0 | **1 884** | 424 (23 %) | 28 |
| Torres de la Alameda | 1 872 | 1 | 1 871 | 5 | **1 866** | 567 (30 %) | 20 |
| Pozuelo de Alarcón | 1 864 | 2 | 1 862 | 95 | **1 767** |  | 217 |
| Leganés | 1 852 | 7 | 1 845 | 0 | **1 845** | 48 (3 %) | 139 |
| Soto del Real | 1 880 | 56 | 1 824 | 10 | **1 814** | 451 (25 %) | 15 |
| Valdilecha | 1 814 | 0 | 1 814 | 12 | **1 802** | 485 (27 %) | 3 |
| Valdelaguna | 1 810 | 0 | 1 810 | 0 | **1 810** | 427 (24 %) | 2 |
| Pezuela de las Torres | 1 786 | 0 | 1 786 | 0 | **1 786** | 552 (31 %) | 10 |
| Garganta de los Montes | 1 774 | 39 | 1 735 | 0 | **1 735** | 471 (27 %) | 7 |
| Talamanca de Jarama | 1 714 | 0 | 1 714 | 0 | **1 714** | 713 (42 %) | 13 |
| El Boalo-Cerceda-Mataelpino | 1 710 | 0 | 1 710 | 134 | **1 576** | 210 (13 %) | 12 |
| Fuenlabrada | 1 685 | 0 | 1 685 | 0 | **1 685** | 114 (7 %) | 170 |
| San Fernando de Henares | 1 698 | 17 | 1 681 | 0 | **1 681** | 175 (10 %) | 118 |
| San Agustín del Guadalix | 1 662 | 1 | 1 661 | 0 | **1 661** | 143 (9 %) | 13 |
| Majadahonda | 1 658 | 0 | 1 658 | 0 | **1 658** | 64 (4 %) | 67 |
| Tres Cantos | 1 643 | 2 | 1 641 | 0 | **1 641** | 260 (16 %) | 65 |
| Algete | 1 643 | 12 | 1 631 | 0 | **1 631** | 422 (26 %) | 55 |
| Cercedilla | 1 558 | 3 | 1 555 | 0 | **1 555** | 58 (4 %) | 5 |
| Camarma de Esteruelas | 1 532 | 0 | 1 532 | 0 | **1 532** | 684 (45 %) | 9 |
| Meco | 1 527 | 0 | 1 527 | 1 | **1 526** | 400 (26 %) | 56 |
| Villanueva de la Cañada | 1 515 | 1 | 1 514 | 6 | **1 508** | 69 (5 %) | 51 |
| Villalbilla | 1 504 | 0 | 1 504 | 29 | **1 475** | 285 (19 %) | 21 |
| Los Santos de la Humosa | 1 498 | 0 | 1 498 | 0 | **1 498** | 495 (33 %) | 11 |
| El Vellón | 1 485 | 0 | 1 485 | 0 | **1 485** | 493 (33 %) | 3 |
| Patones | 1 512 | 51 | 1 461 | 0 | **1 461** | 165 (11 %) | 7 |
| Valdetorres de Jarama | 1 458 | 0 | 1 458 | 0 | **1 458** | 532 (36 %) | 22 |
| Alcorcón | 1 451 | 2 | 1 449 | 7 | **1 442** | 128 (9 %) | 144 |
| Fuente el Saz de Jarama | 1 445 | 2 | 1 443 | 0 | **1 443** | 411 (28 %) | 15 |
| Villaconejos | 1 423 | 0 | 1 423 | 6 | **1 417** | 204 (14 %) | 19 |
| Montejo de la Sierra | 1 416 | 0 | 1 416 | 0 | **1 416** | 188 (13 %) | 8 |
| Torrejón de Ardoz | 1 413 | 4 | 1 409 | 555 | **854** | 28 (3 %) | 113 |
| Ribatejada | 1 387 | 1 | 1 386 | 0 | **1 386** | 574 (41 %) | 3 |
| Fresno de Torote | 1 374 | 0 | 1 374 | 0 | **1 374** | 409 (30 %) | 5 |
| Villanueva de Perales | 1 370 | 0 | 1 370 | 0 | **1 370** | 200 (15 %) | 30 |
| Moraleja de Enmedio | 1 340 | 0 | 1 340 | 0 | **1 340** | 294 (22 %) | 11 |
| Pozuelo del Rey | 1 335 | 0 | 1 335 | 0 | **1 335** | 425 (32 %) | 6 |
| Becerril de la Sierra | 1 297 | 1 | 1 296 | 3 | **1 293** | 191 (15 %) | 13 |
| Colmenarejo | 1 368 | 76 | 1 292 | 0 | **1 292** | 78 (6 %) | 21 |
| Rozas de Puerto Real | 1 303 | 12 | 1 291 | 0 | **1 291** | 50 (4 %) | 9 |
| Villamanrique de Tajo | 1 248 | 0 | 1 248 | 0 | **1 248** | 401 (32 %) | 1 |
| Navarredonda y San Mamés | 1 239 | 0 | 1 239 | 0 | **1 239** | 186 (15 %) | 3 |
| Fresnedillas de la Oliva | 1 223 | 2 | 1 221 | 0 | **1 221** | 218 (18 %) | 12 |
| Santorcaz | 1 213 | 0 | 1 213 | 90 | **1 123** | 496 (44 %) | 25 |
| El Atazar | 1 297 | 98 | 1 199 | 0 | **1 199** | 231 (19 %) | 11 |
| Villar del Olmo | 1 196 | 0 | 1 196 | 137 | **1 059** | 379 (36 %) | 10 |
| Pedrezuela | 1 239 | 52 | 1 187 | 0 | **1 187** | 189 (16 %) | 10 |
| El Berrueco | 1 246 | 83 | 1 163 | 0 | **1 163** | 149 (13 %) | 5 |
| Navacerrada | 1 195 | 33 | 1 162 | 0 | **1 162** | 84 (7 %) | 18 |
| Valdeolmos-Alalpardo | 1 162 | 3 | 1 159 | 0 | **1 159** | 387 (33 %) | 8 |
| Tielmes | 1 158 | 0 | 1 158 | 0 | **1 158** | 414 (36 %) | 10 |
| Corpa | 1 123 | 0 | 1 123 | 0 | **1 123** | 456 (41 %) | 11 |
| Ambite | 1 117 | 0 | 1 117 | 0 | **1 117** | 284 (25 %) | 6 |
| Alameda del Valle | 1 111 | 0 | 1 111 | 0 | **1 111** | 249 (22 %) | 4 |
| Quijorna | 1 107 | 0 | 1 107 | 0 | **1 107** | 183 (17 %) | 17 |
| Chapinería | 1 097 | 2 | 1 095 | 0 | **1 095** | 59 (5 %) | 11 |
| Collado Villalba | 1 094 | 0 | 1 094 | 7 | **1 087** | 92 (8 %) | 80 |
| Villanueva del Pardillo | 1 091 | 1 | 1 090 | 5 | **1 085** | 148 (14 %) | 30 |
| Braojos | 1 088 | 0 | 1 088 | 0 | **1 088** | 148 (14 %) | 12 |
| Pinilla del Valle | 1 112 | 28 | 1 084 | 0 | **1 084** | 294 (27 %) | 2 |
| Parla | 1 077 | 1 | 1 076 | 0 | **1 076** | 58 (5 %) | 57 |
| Horcajuelo de la Sierra | 1 075 | 0 | 1 075 | 0 | **1 075** | 198 (18 %) | 4 |
| Sevilla la Nueva | 1 070 | 0 | 1 070 | 0 | **1 070** | 176 (16 %) | 27 |
| Buitrago del Lozoya | 1 118 | 74 | 1 044 | 0 | **1 044** | 238 (23 %) | 18 |
| Villamantilla | 1 034 | 0 | 1 034 | 0 | **1 034** | 80 (8 %) | 31 |
| Villavieja del Lozoya | 1 032 | 1 | 1 031 | 0 | **1 031** | 122 (12 %) | 4 |
| Belmonte de Tajo | 1 023 | 0 | 1 023 | 0 | **1 023** | 153 (15 %) | 4 |
| Prádena del Rincón | 990 | 0 | 990 | 0 | **990** | 140 (14 %) | 1 |
| La Acebeda | 977 | 0 | 977 | 0 | **977** | 101 (10 %) | 8 |
| Gargantilla del Lozoya y Pinilla de Buitrago | 1 044 | 68 | 976 | 0 | **976** | 297 (30 %) |  |
| Collado Mediano | 973 | 1 | 972 | 0 | **972** | 99 (10 %) | 5 |
| La Cabrera | 971 | 0 | 971 | 0 | **971** | 126 (13 %) | 16 |
| El Álamo | 959 | 0 | 959 | 0 | **959** | 222 (23 %) | 10 |
| Torrelodones | 946 | 3 | 943 | 0 | **943** |  | 32 |
| Anchuelo | 936 | 0 | 936 | 0 | **936** | 363 (39 %) | 6 |
| Orusco de Tajuña | 927 | 0 | 927 | 45 | **882** | 399 (45 %) |  |
| Batres | 916 | 0 | 916 | 0 | **916** | 136 (15 %) | 6 |
| Horcajo de la Sierra-Aoslos | 908 | 0 | 908 | 0 | **908** | 297 (33 %) | 6 |
| Cobeña | 907 | 1 | 906 | 0 | **906** | 239 (26 %) | 24 |
| Somosierra | 899 | 0 | 899 | 0 | **899** | 157 (17 %) | 36 |
| Arroyomolinos | 893 | 1 | 892 | 0 | **892** | 99 (11 %) | 39 |
| Zarzalejo | 888 | 0 | 888 | 0 | **888** | 130 (15 %) | 188 |
| Gascones | 872 | 1 | 871 | 0 | **871** | 160 (18 %) | 1 |
| Nuevo Baztán | 866 | 0 | 866 | 0 | **866** | 220 (25 %) | 60 |
| Robledillo de la Jara | 896 | 33 | 863 | 0 | **863** | 201 (23 %) | 5 |
| Los Molinos | 850 | 0 | 850 | 0 | **850** | 116 (14 %) | 10 |
| Ajalvir | 845 | 0 | 845 | 83 | **762** | 177 (23 %) | 9 |
| Humanes de Madrid | 841 | 0 | 841 | 0 | **841** | 108 (13 %) | 15 |
| Valdeavero | 822 | 0 | 822 | 0 | **822** | 348 (42 %) | 4 |
| Torremocha de Jarama | 814 | 0 | 814 | 0 | **814** | 217 (27 %) | 2 |
| Robregordo | 799 | 0 | 799 | 0 | **799** | 170 (21 %) | 5 |
| Mejorada del Campo | 774 | 6 | 768 | 0 | **768** | 52 (7 %) | 64 |
| Piñuécar-Gandullas | 803 | 36 | 767 | 0 | **767** | 197 (26 %) | 16 |
| Valdepiélagos | 766 | 0 | 766 | 0 | **766** | 379 (49 %) | 4 |
| Valdemanco | 762 | 1 | 761 | 0 | **761** | 131 (17 %) |  |
| Griñón | 743 | 0 | 743 | 3 | **740** | 113 (15 %) | 19 |
| La Hiruela | 742 | 0 | 742 | 0 | **742** | 105 (14 %) | 2 |
| Olmeda de las Fuentes | 712 | 0 | 712 | 0 | **712** | 318 (45 %) |  |
| Cabanillas de la Sierra | 614 | 0 | 614 | 0 | **614** | 149 (24 %) | 1 |
| Berzosa del Lozoya | 627 | 18 | 609 | 0 | **609** | 76 (12 %) | 7 |
| Valverde de Alcalá | 592 | 0 | 592 | 0 | **592** | 119 (20 %) | 22 |
| Velilla de San Antonio | 616 | 37 | 579 | 0 | **579** | 125 (22 %) | 35 |
| Redueña | 573 | 0 | 573 | 0 | **573** | 51 (9 %) | 38 |
| Serranillos del Valle | 573 | 0 | 573 | 0 | **573** | 113 (20 %) | 8 |
| Alpedrete | 572 | 0 | 572 | 0 | **572** | 43 (8 %) | 68 |
| Cubas de la Sagra | 552 | 0 | 552 | 0 | **552** | 108 (20 %) | 13 |
| Coslada | 520 | 1 | 519 | 0 | **519** | 2 (0 %) | 87 |
| Navalafuente | 513 | 0 | 513 | 0 | **513** | 145 (28 %) | 3 |
| Venturada | 424 | 0 | 424 | 0 | **424** | 82 (19 %) | 2 |
| Titulcia | 432 | 14 | 418 | 0 | **418** | 90 (22 %) | 12 |
| Torrejón de la Calzada | 379 | 0 | 379 | 0 | **379** | 31 (8 %) | 60 |
| Madarcos | 372 | 1 | 371 | 0 | **371** | 112 (30 %) |  |
| Cervera de Buitrago | 526 | 161 | 365 | 0 | **365** | 153 (42 %) |  |
| Pelayos de la Presa | 320 | 0 | 320 | 0 | **320** | 8 (2 %) | 4 |
| La Serna del Monte | 242 | 0 | 242 | 0 | **242** | 59 (24 %) | 2 |
| Casarrubuelos | 226 | 0 | 226 | 0 | **226** | 41 (18 %) | 19 |
| Los Baldíos | 226 | 0 | 226 | 0 | **226** | 3 (1 %) | 2 |
| El Redegüelo | 27 | 0 | 27 | 0 | **27** |  |  |

## Arrondissements et quartiers (21)

| Zone | Ville | Brut | Eau | Sans eau | Restr. | Comptées | Sans chemin | Parcs |
|---|---|---:|---:|---:|---:|---:|---:|---:|
| Fuencarral-El Pardo | madrid | 10 310 | 192 | 10 118 | 81 | **10 037** | 78 (1 %) | 319 |
| Villa de Vallecas | madrid | 2 221 | 5 | 2 216 | 0 | **2 216** | 245 (11 %) | 111 |
| Moncloa-Aravaca | madrid | 2 019 | 13 | 2 006 | 8 | **1 998** |  | 262 |
| Barajas | madrid | 1 796 | 14 | 1 782 | 946 | **836** | 12 (1 %) | 97 |
| Vicálvaro | madrid | 1 506 | 1 | 1 505 | 0 | **1 505** | 175 (12 %) | 79 |
| Hortaleza | madrid | 1 193 | 3 | 1 190 | 0 | **1 190** | 19 (2 %) | 212 |
| Latina | madrid | 1 103 | 2 | 1 101 | 243 | **858** | 4 (0 %) | 151 |
| San Blas - Canillejas | madrid | 969 | 6 | 963 | 5 | **958** | 8 (1 %) | 95 |
| Villaverde | madrid | 865 | 3 | 862 | 15 | **847** | 18 (2 %) | 124 |
| Puente de Vallecas | madrid | 642 | 4 | 638 | 0 | **638** |  | 136 |
| Carabanchel | madrid | 602 | 1 | 601 | 8 | **593** |  | 219 |
| Ciudad Lineal | madrid | 496 | 1 | 495 | 4 | **491** |  | 105 |
| Chamartín | madrid | 397 | 0 | 397 | 0 | **397** |  | 54 |
| Usera | madrid | 336 | 2 | 334 | 0 | **334** |  | 103 |
| Arganzuela | madrid | 283 | 3 | 280 | 0 | **280** |  | 130 |
| Moratalaz | madrid | 262 | 0 | 262 | 0 | **262** |  | 102 |
| Retiro | madrid | 237 | 2 | 235 | 0 | **235** |  | 78 |
| Salamanca | madrid | 233 | 0 | 233 | 0 | **233** |  | 33 |
| Tetuán | madrid | 232 | 0 | 232 | 0 | **232** |  | 37 |
| Centro | madrid | 228 | 0 | 228 | 0 | **228** |  | 41 |
| Chamberí | madrid | 201 | 0 | 201 | 0 | **201** |  | 21 |

## Parcs (9118)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Forêt de Madrid (242) ⚠️ | Madrid › Fuencarral-El Pardo | 5 389 |
| Forêt de Lozoya (6) ⚠️ | Lozoya | 2 616 |
| Forêt de Rascafría (14) ⚠️ | Rascafría | 1 938 |
| Forêt de Madrid (52) ⚠️ | Madrid › Fuencarral-El Pardo | 1 726 |
| Bois de Cercedilla ⚠️ | Cercedilla | 1 558 |
| Soto de Viñuelas ⚠️ | Madrid › Fuencarral-El Pardo | 1 465 |
| Forêt de Villa del Prado (7) ⚠️ | Villa del Prado | 1 332 |
| Pinares ⚠️ | Puebla de la Sierra | 1 117 |
| Forêt de Navalagamella (9) ⚠️ | Navalagamella | 1 046 |
| Forêt de Navalagamella (21) ⚠️ | Navalagamella | 1 044 |
| Forêt de Guadarrama (18) ⚠️ | Guadarrama | 956 |
| Bois de Villanueva de la Cañada ⚠️ | Villanueva de la Cañada | 940 |
| Forêt de San Martín de Valdeiglesias (21) ⚠️ | San Martín de Valdeiglesias | 937 |
| Forêt de Manzanares el Real (2) ⚠️ | Manzanares el Real | 920 |
| Forêt de San Agustín del Guadalix ⚠️ | San Agustín del Guadalix | 867 |
| Forêt de San Martín de Valdeiglesias (22) ⚠️ | San Martín de Valdeiglesias | 848 |
| Forêt de Colmenar Viejo (2) ⚠️ | Colmenar Viejo | 793 |
| Forêt de Navas del Rey (5) ⚠️ | Navas del Rey | 727 |
| Bois de Villaviciosa de Odón (5) ⚠️ | Villaviciosa de Odón | 712 |
| Forêt de Madrid (9) ⚠️ | Madrid › Fuencarral-El Pardo | 661 |
| Forêt de Canencia ⚠️ | Canencia | 650 |
| Forêt de Canencia (6) ⚠️ | Canencia | 650 |
| Forêt de Rascafría (15) ⚠️ | Rascafría | 647 |
| Forêt de Galapagar (5) ⚠️ | Galapagar | 634 |
| Forêt de El Escorial (44) ⚠️ | El Escorial | 630 |
| Forêt de El Escorial (42) ⚠️ | El Escorial | 624 |
| Bois de Montejo de la Sierra ⚠️ | Horcajuelo de la Sierra | 617 |
| Forêt de Rascafría (6) ⚠️ | Rascafría | 599 |
| Casa de Campo ⚠️ | Madrid › Moncloa-Aravaca | 596 |
| Forêt de Hoyo de Manzanares ⚠️ | Hoyo de Manzanares | 538 |
| Forêt de Lozoya (2) ⚠️ | Lozoya | 513 |
| Forêt de Alameda del Valle (2) ⚠️ | Alameda del Valle | 501 |
| Forêt de Miraflores de la Sierra (2) ⚠️ | Miraflores de la Sierra | 448 |
| Forêt de Ambite (3) ⚠️ | Ambite | 410 |
| Forêt de San Martín de Valdeiglesias ⚠️ | San Martín de Valdeiglesias | 398 |
| Forêt de Valdemorillo ⚠️ | Valdemorillo | 394 |
| Forêt de Rozas de Puerto Real (7) ⚠️ | Rozas de Puerto Real | 393 |
| Forêt de Rascafría (18) ⚠️ | Rascafría | 380 |
| El Monte del Pilar ⚠️ | Pozuelo de Alarcón › Moncloa-Aravaca | 362 |
| Forêt de Buitrago del Lozoya ⚠️ | Buitrago del Lozoya | 360 |
| Forêt de Guadalix de la Sierra (5) ⚠️ | Guadalix de la Sierra | 358 |
| Bois de Chapinería (7) ⚠️ | Chapinería | 356 |
| Forêt de La Acebeda (2) ⚠️ | La Acebeda | 355 |
| Bois de Cenicientos ⚠️ | Cenicientos | 316 |
| Bois de Colmenarejo (3) ⚠️ | Colmenarejo | 316 |
| Forêt de Lozoya (3) ⚠️ | Lozoya | 305 |
| Forêt de Becerril de la Sierra (2) ⚠️ | Becerril de la Sierra | 304 |
| Forêt de Collado Villalba ⚠️ | Collado Villalba | 296 |
| Bois de Aldea del Fresno (4) ⚠️ | Aldea del Fresno | 292 |
| Dehesa Boyal ⚠️ | Manzanares el Real | 290 |
| Bois de Navas del Rey ⚠️ | Navas del Rey | 288 |
| Forêt de Colmenar del Arroyo (5) ⚠️ | Colmenar del Arroyo | 278 |
| Forêt de San Martín de Valdeiglesias (20) ⚠️ | San Martín de Valdeiglesias | 270 |
| Forêt de Moralzarzal ⚠️ | Moralzarzal | 262 |
| Bois de Manzanares el Real (22) ⚠️ | Manzanares el Real | 259 |
| Forêt de Manzanares el Real (13) ⚠️ | Manzanares el Real | 258 |
| Forêt de Piñuécar-Gandullas ⚠️ | Piñuécar-Gandullas | 254 |
| Bois de Batres ⚠️ | Batres | 250 |
| Bois de La Hiruela ⚠️ | La Hiruela | 240 |
| Encinar de Boadilla ⚠️ | Boadilla del Monte | 235 |
| Bois de Pezuela de las Torres ⚠️ | Pezuela de las Torres | 223 |
| Forêt de Manzanares el Real (12) ⚠️ | Manzanares el Real | 214 |
| Forêt de Navas del Rey (3) ⚠️ | Navas del Rey | 213 |
| Forêt de Navarredonda y San Mamés ⚠️ | Navarredonda y San Mamés | 211 |
| Forêt de Puentes Viejas (2) ⚠️ | Puentes Viejas | 211 |
| Forêt de Robledo de Chavela (57) ⚠️ | Robledo de Chavela | 205 |
| Bois de Villamanta (9) ⚠️ | Villamanta | 204 |
| Forêt de Valdemaqueda (20) ⚠️ | Valdemaqueda | 202 |
| Forêt de San Lorenzo de El Escorial (11) ⚠️ | San Lorenzo de El Escorial | 199 |
| Forêt de El Boalo-Cerceda-Mataelpino ⚠️ | El Boalo-Cerceda-Mataelpino | 197 |
| Bois de Chapinería (6) ⚠️ | Chapinería | 195 |
| Forêt de Berzosa del Lozoya ⚠️ | Berzosa del Lozoya | 193 |
| Bois de Villanueva de Perales ⚠️ | Villanueva de Perales | 174 |
| Bois de Horcajuelo de la Sierra ⚠️ | Horcajuelo de la Sierra | 171 |
| Forêt de San Lorenzo de El Escorial (4) ⚠️ | San Lorenzo de El Escorial | 166 |
| Forêt de Valdemaqueda (2) ⚠️ | Valdemaqueda | 163 |
| Monte de Valdelatas ⚠️ | Madrid › Fuencarral-El Pardo | 161 |
| Bois de Rozas de Puerto Real (2) ⚠️ | Rozas de Puerto Real | 161 |
| Forêt de Guadarrama (17) ⚠️ | Guadarrama | 161 |
| Forêt de Alcalá de Henares ⚠️ | Alcalá de Henares | 160 |
| Forêt de Montejo de la Sierra (5) ⚠️ | Montejo de la Sierra | 159 |
| Forêt de Manzanares el Real (11) ⚠️ | Manzanares el Real | 158 |
| Forêt de Garganta de los Montes ⚠️ | Garganta de los Montes | 157 |
| Forêt de Bustarviejo (4) ⚠️ | Bustarviejo | 154 |
| Dehesa de Arriba de Navalquejigo ⚠️ | Fresnedillas de la Oliva | 154 |
| Forêt de Alpedrete ⚠️ | Alpedrete | 153 |
| Forêt de Galapagar (4) ⚠️ | Galapagar | 150 |
| Bois de Villaviciosa de Odón ⚠️ | Villaviciosa de Odón | 146 |
| Forêt de San Martín de la Vega ⚠️ | San Martín de la Vega | 144 |
| Forêt de Navacerrada (2) ⚠️ | Navacerrada | 144 |
| Forêt de San Sebastián de los Reyes (4) ⚠️ | San Sebastián de los Reyes › Fuencarral-El Pardo | 144 |
| Forêt de Miraflores de la Sierra (5) ⚠️ | Miraflores de la Sierra | 141 |
| Forêt de Miraflores de la Sierra ⚠️ | Miraflores de la Sierra | 140 |
| Forêt de Valdemaqueda (19) ⚠️ | Valdemaqueda | 140 |
| Bois de Rozas de Puerto Real ⚠️ | Rozas de Puerto Real | 139 |
| Monte de Boadilla ⚠️ | Boadilla del Monte | 135 |
| Forêt de Valdemorillo (13) ⚠️ | Valdemorillo | 135 |
| Monte de Boadilla (2) ⚠️ | Boadilla del Monte | 135 |
| Forêt de Robledillo de la Jara ⚠️ | Robledillo de la Jara | 133 |
| Forêt de San Lorenzo de El Escorial (5) ⚠️ | San Lorenzo de El Escorial | 129 |
| Forêt de San Lorenzo de El Escorial (13) | San Lorenzo de El Escorial | 125 |
| Bois de Colmenar Viejo (3) | Colmenar Viejo | 122 |
| Forêt de Montejo de la Sierra (3) | Montejo de la Sierra | 119 |
| Forêt de San Lorenzo de El Escorial (9) | San Lorenzo de El Escorial | 119 |
| Forêt de Robledo de Chavela (56) | Robledo de Chavela | 119 |
| Bois de San Lorenzo de El Escorial (6) | San Lorenzo de El Escorial | 119 |
| Forêt de Manzanares el Real (14) | Manzanares el Real | 118 |
| Forêt de Bustarviejo | Bustarviejo | 117 |
| Forêt de Navalcarnero (2) | Navalcarnero | 114 |
| Forêt de Villavieja del Lozoya | Villavieja del Lozoya | 114 |
| Forêt de Colmenar Viejo | Colmenar Viejo | 111 |
| Forêt de Villa del Prado (4) | Villa del Prado | 111 |
| Forêt de Cenicientos (8) | Cenicientos | 111 |
| Forêt de El Escorial (2) | El Escorial | 110 |
| Bois de San Lorenzo de El Escorial | San Lorenzo de El Escorial | 109 |
| Forêt de Prádena del Rincón | Prádena del Rincón | 109 |
| Forêt de Garganta de los Montes (4) | Garganta de los Montes | 109 |
| Bois de Villaviciosa de Odón (2) | Villaviciosa de Odón | 108 |
| Bois de Valdemorillo (2) | Valdemorillo | 107 |
| Forêt de Navalagamella (6) | Navalagamella | 104 |
| Forêt de Villa del Prado (5) | Villa del Prado | 104 |
| Bois de Villamanta (2) | Villamanta | 104 |
| Forêt de Guadarrama (2) | Guadarrama | 103 |
| Bosque Sur (2) | Leganés | 100 |
| Forêt de Pelayos de la Presa | Pelayos de la Presa | 97 |
| Dehesa Boyal (2) | San Sebastián de los Reyes | 96 |
| Forêt de San Lorenzo de El Escorial | San Lorenzo de El Escorial | 95 |
| Forêt de Rascafría (7) | Rascafría | 94 |
| Forêt de San Lorenzo de El Escorial (10) | San Lorenzo de El Escorial | 94 |
| Forêt de San Lorenzo de El Escorial (12) | San Lorenzo de El Escorial | 94 |
| Forêt de Miraflores de la Sierra (6) | Miraflores de la Sierra | 92 |
| Bois de Guadarrama (7) | Guadarrama | 89 |
| Bois de Villamantilla (4) | Villamantilla | 88 |
| Forêt de Robledo de Chavela (22) | Robledo de Chavela | 88 |
| Bois de Redueña (34) | Redueña | 87 |
| Dehesa de Braojos | Braojos | 86 |
| La Dehesa del Carrascal | Arganda del Rey | 85 |
| Forêt de Patones (5) | Patones | 85 |
| Forêt de Valdemaqueda (29) | Valdemaqueda | 84 |
| Bois de Torrelaguna (15) | Torrelaguna | 84 |
| Forêt de Lozoya | Lozoya | 83 |
| Forêt de Bustarviejo (3) | Bustarviejo | 83 |
| Dehesa Boyal de Montejo de la Sierra | Montejo de la Sierra | 81 |
| Forêt de Navalagamella (20) | Navalagamella | 81 |
| Forêt de Sevilla la Nueva (9) | Sevilla la Nueva | 80 |
| Forêt de Valdemorillo (57) | Valdemorillo | 80 |
| Parque Forestal de Valdebebas-Felipe VI | Madrid › Hortaleza | 79 |
| Forêt de Puentes Viejas | Puentes Viejas | 78 |
| Forêt de Somosierra (23) | Somosierra | 78 |
| Forêt de Tres Cantos (5) | Tres Cantos | 78 |
| Forêt de Valdeolmos-Alalpardo | Valdeolmos-Alalpardo | 77 |
| Forêt de Tres Cantos (2) | Tres Cantos | 77 |
| Forêt de Santa María de la Alameda (38) | Santa María de la Alameda | 77 |
| Forêt de Patones (6) | Patones | 76 |
| Forêt de Villamantilla | Villamantilla | 75 |
| Forêt de Collado Mediano | Collado Mediano | 74 |
| Forêt de Robledo de Chavela (16) | Robledo de Chavela | 74 |
| Forêt de Valdemorillo (69) | Valdemorillo | 74 |
| Forêt de Alcalá de Henares (51) | Alcalá de Henares | 74 |
| Forêt de Torres de la Alameda | Torres de la Alameda | 73 |
| Forêt de Rascafría (5) | Rascafría | 72 |
| Forêt de Rascafría | Rascafría | 71 |
| Forêt de Navas del Rey (2) | Navas del Rey | 71 |
| Parque Lineal del Manzanares | Madrid › Villa de Vallecas | 71 |
| Forêt de Guadalix de la Sierra (4) | Guadalix de la Sierra | 70 |
| Forêt de Villanueva de Perales (2) | Villanueva de Perales | 70 |
| Forêt de Arganda del Rey (6) | Arganda del Rey | 70 |
| Forêt de Brea de Tajo (7) | Brea de Tajo | 69 |
| Forêt de Zarzalejo (171) | Zarzalejo | 69 |
| Forêt de Valdemaqueda (21) | Valdemaqueda | 67 |
| Bois de Guadarrama (6) | Guadarrama | 67 |
| Forêt de Villa del Prado (3) | Villa del Prado | 66 |
| Forêt de San Lorenzo de El Escorial (3) | San Lorenzo de El Escorial | 65 |
| Parque de Polvoranca | Leganés | 64 |
| Finca Las Ras | Valdemorillo | 64 |
| Forêt de Majadahonda | Majadahonda | 63 |
| Bois de Colmenarejo (2) | Colmenarejo | 63 |
| Bois de Chapinería (10) | Chapinería | 63 |
| Forêt de San Martín de la Vega (3) | Getafe | 62 |
| Forêt de Villa del Prado (2) | Villa del Prado | 60 |
| Forêt de Madrid (15) | Madrid › Fuencarral-El Pardo | 59 |
| Bois de Los Molinos (2) | Los Molinos | 59 |
| El Monreal | Villaviciosa de Odón | 58 |
| Forêt de Villanueva de Perales (8) | Villanueva de Perales | 57 |
| Parque Forestal Adolfo Suárez | Pozuelo de Alarcón | 57 |
| Bois de San Lorenzo de El Escorial (4) | San Lorenzo de El Escorial | 56 |
| La Fuente del Valle | Arganda del Rey | 55 |
| Forêt de El Atazar (9) | El Atazar | 55 |
| Forêt de Valdemaqueda (14) | Valdemaqueda | 54 |
| Dehesa Boyal del Berrueco | El Berrueco | 54 |
| Forêt de Santa María de la Alameda (37) | Santa María de la Alameda | 54 |
| Parque Juan Carlos I | Madrid › Barajas | 53 |
| Forêt de San Lorenzo de El Escorial (7) | San Lorenzo de El Escorial | 53 |
| Forêt de Arganda del Rey (5) | Arganda del Rey | 53 |
| Forêt de San Lorenzo de El Escorial (14) | San Lorenzo de El Escorial | 53 |
| Forêt de San Lorenzo de El Escorial (2) | San Lorenzo de El Escorial | 52 |
| Bois de Villamanta (4) | Villamanta | 52 |
| Parque Forestal de Los Pinos | Valdilecha | 50 |
| Forêt de Pezuela de las Torres (5) | Pezuela de las Torres | 50 |
| Forêt de El Berrueco | El Berrueco | 50 |
| Forêt de Canencia (4) | Canencia | 49 |
| Parque del Retiro | Madrid › Retiro | 49 |
| Forêt de El Escorial (4) | El Escorial | 48 |
| Bois de Villaviciosa de Odón (3) | Villaviciosa de Odón | 48 |
| Bosque de La Herrería | San Lorenzo de El Escorial | 47 |
| Forêt de Lozoyuela-Navas-Sieteiglesias (2) | Lozoyuela-Navas-Sieteiglesias | 47 |
| Dehesa de Somosierra | Somosierra | 46 |
| Forêt de Guadarrama (3) | Guadarrama | 46 |
| Dehesa de Navalcarbón | Las Rozas de Madrid | 45 |
| Forêt de San Martín de la Vega (6) | San Martín de la Vega | 45 |
| Forêt de Quijorna (4) | Quijorna | 45 |
| Forêt de Robledo de Chavela (26) | Robledo de Chavela | 45 |
| Forêt de Paracuellos de Jarama (6) | Paracuellos de Jarama › Barajas | 45 |
| Forêt de Rascafría (8) | Rascafría | 45 |
| Cerro de los Ángeles | Getafe | 45 |
| Bois de Colmenar del Arroyo (2) | Colmenar del Arroyo | 45 |
| Forêt de Valdemorillo (52) | Valdemorillo | 44 |
| Forêt de Navalagamella (15) | Navalagamella | 44 |
| Dehesa de Abajo de Navalquejigo | Fresnedillas de la Oliva | 43 |
| Forêt de Brea de Tajo (3) | Brea de Tajo | 42 |
| Bois de Redueña (33) | Redueña | 42 |
| Bois de Getafe | Getafe | 41 |
| Bois de Collado Mediano (2) | Collado Mediano | 41 |
| Forêt de Cenicientos (7) | Cenicientos | 41 |
| Forêt de Villanueva de Perales (6) | Villanueva de Perales | 40 |
| Forêt de Manzanares el Real (4) | Manzanares el Real | 40 |
| Forêt de Miraflores de la Sierra (7) | Miraflores de la Sierra | 39 |
| Parque Forestal de Valdemingómez (antiguo vertedero) | Madrid › Villa de Vallecas | 39 |
| Forêt de Villanueva de Perales (10) | Villanueva de Perales | 39 |
| Bois de Redueña (2) | Redueña | 39 |
| Bois de Bustarviejo | Bustarviejo | 39 |
| Bois de Villamanta (3) | Villamanta | 39 |
| Forêt de Valdemorillo (74) | Valdemorillo | 39 |
| Forêt de San Martín de Valdeiglesias (16) | San Martín de Valdeiglesias | 38 |
| Forêt de Valdemaqueda (22) | Valdemaqueda | 38 |
| Parc de Madrid (819) | Madrid › Hortaleza | 38 |
| Bois de Manzanares el Real (5) | Manzanares el Real | 38 |
| Bois de Torrejón de Velasco (2) | Torrejón de Velasco | 38 |
| Forêt de Alcalá de Henares (49) | Alcalá de Henares | 38 |
| Forêt de Robledo de Chavela (11) | Robledo de Chavela | 37 |
| Dehesa de Cobeña | Cobeña | 37 |
| Bois de Villamanta (7) | Villamanta | 37 |
| Parque Alhóndiga | Getafe | 36 |
| Terrenos del antiguo vertedero | Madrid › Villa de Vallecas | 36 |
| Forêt de Robledo de Chavela (38) | Robledo de Chavela | 36 |
| Forêt de Navas del Rey | Navas del Rey | 36 |
| Bois de Belmonte de Tajo | Belmonte de Tajo | 35 |
| Bois de Belmonte de Tajo (2) | Belmonte de Tajo | 35 |
| Forêt de El Boalo-Cerceda-Mataelpino (2) | El Boalo-Cerceda-Mataelpino | 35 |
| Forêt de Lozoyuela-Navas-Sieteiglesias | Lozoyuela-Navas-Sieteiglesias | 35 |
| Forêt de Boadilla del Monte | Boadilla del Monte | 34 |
| Forêt de Villanueva del Pardillo | Villanueva del Pardillo | 34 |
| Bois de Brunete | Brunete | 34 |
| Bois de Miraflores de la Sierra (3) | Miraflores de la Sierra | 34 |
| Parque del Oeste | Madrid › Moncloa-Aravaca | 34 |
| Forêt de Belmonte de Tajo | Belmonte de Tajo | 34 |
| Forêt de El Escorial (43) | El Escorial | 33 |
| Forêt de Rascafría (17) | Rascafría | 33 |
| Parc de Madrid (1538) | Madrid › Villa de Vallecas | 33 |
| Forêt de San Lorenzo de El Escorial (6) | San Lorenzo de El Escorial | 32 |
| Forêt de Madrid (6) | Madrid › Fuencarral-El Pardo | 32 |
| Forêt de Rascafría (2) | Rascafría | 32 |
| Bois de Valdemoro (2) | Valdemoro | 32 |
| Parque Princesa Leonor | Madrid › Hortaleza | 32 |
| Monte Cerro Robledillo | Robledo de Chavela | 31 |
| Bosque Sur | Pinto | 31 |
| Forêt de Robledo de Chavela (48) | Robledo de Chavela | 31 |
| Forêt de Pezuela de las Torres (4) | Pezuela de las Torres | 31 |
| Forêt de Robledo de Chavela (32) | Robledo de Chavela | 30 |
| Forêt de Valverde de Alcalá | Valverde de Alcalá | 30 |
| Bois de Villaviciosa de Odón (6) | Villaviciosa de Odón | 30 |
| Forêt de Torrelaguna (2) | Torrelaguna | 30 |
| Forêt de Valdemorillo (26) | Valdemorillo | 30 |
| Bois de Galapagar (62) | Galapagar | 30 |
| Parque de los Arroyos | San Sebastián de los Reyes | 29 |
| El Bosque del Santander | Boadilla del Monte | 29 |
| Parque de La Cantueña | Fuenlabrada | 29 |
| Bois de Villamantilla | Villamantilla | 29 |
| Forêt de Navalagamella (7) | Navalagamella | 29 |
| Forêt de Robledo de Chavela (15) | Robledo de Chavela | 29 |
| Bois de Madrid (22) | Madrid › Fuencarral-El Pardo | 29 |
| Forêt de Valdelaguna | Valdelaguna | 29 |
| Forêt de Villalbilla (3) | Villalbilla | 29 |
| Forêt de Cenicientos (5) | Cenicientos | 29 |
| Bosque Urbano de Barajas (3) | Madrid › Barajas | 28 |
| Parque Cuña Verde de O'Donnell | Madrid › Moratalaz | 28 |
| Parque de Las Presillas | Alcorcón | 28 |
| Forêt de Paracuellos de Jarama | Paracuellos de Jarama | 28 |
| El Hornillo | Santa María de la Alameda | 28 |
| Dehesa de Abajo | Robledillo de la Jara | 28 |
| Forêt de Los Molinos | Los Molinos | 28 |
| Bois de Galapagar | Galapagar | 27 |
| Bois de Arroyomolinos | Arroyomolinos | 27 |
| Forêt de Fuente el Saz de Jarama | Fuente el Saz de Jarama | 27 |
| Forêt de Navalagamella (3) | Navalagamella | 27 |
| Dehesa de Berzosa del Lozoya | Berzosa del Lozoya | 27 |
| Forêt de Puebla de la Sierra (4) | Puebla de la Sierra | 27 |
| Parque Emperatriz María de Austria | Madrid › Carabanchel | 27 |
| Forêt de El Escorial | El Escorial | 26 |
| Parque de Pradolongo | Madrid › Usera | 26 |
| Bois de Arganda del Rey | Arganda del Rey | 26 |
| Forêt de Villaviciosa de Odón | Villaviciosa de Odón | 26 |
| Forêt de Guadalix de la Sierra (3) | Guadalix de la Sierra | 26 |
| Bois de Villamantilla (6) | Villamantilla | 26 |
| Forêt de Rivas-Vaciamadrid (31) | Rivas-Vaciamadrid | 26 |
| Forêt de Aldea del Fresno (2) | Aldea del Fresno | 26 |
| Forêt de Alcalá de Henares (50) | Alcalá de Henares | 26 |
| Bois de Manzanares el Real (23) | Manzanares el Real | 26 |
| Parque Forestal de Montegandedo | Pozuelo de Alarcón | 25 |
| Forêt de Valdetorres de Jarama (2) | Valdetorres de Jarama | 25 |
| Bois de Villamantilla (7) | Villamantilla | 25 |
| Forêt de Robledo de Chavela (20) | Robledo de Chavela | 25 |
| Forêt de Robledo de Chavela (42) | Robledo de Chavela | 25 |
| Dehesa de la Villa | Madrid › Moncloa-Aravaca | 25 |
| Forêt de Valdemorillo (30) | Valdemorillo | 25 |
| Forêt de Galapagar (8) | Galapagar | 25 |
| Forêt de Puebla de la Sierra (6) | Puebla de la Sierra | 25 |
| Forêt de Puebla de la Sierra (11) | Puebla de la Sierra | 25 |
| Bois de Collado Villalba | Collado Villalba | 24 |
| Forêt de Soto del Real (2) | Soto del Real | 24 |
| Madrid Río | Madrid › Arganzuela | 24 |
| Forêt de Brunete (3) | Brunete | 24 |
| Forêt de Robledo de Chavela (9) | Robledo de Chavela | 24 |
| Forêt de Valdemaqueda (23) | Valdemaqueda | 24 |
| Forêt de Rivas-Vaciamadrid (52) | Rivas-Vaciamadrid | 24 |
| Forêt de Madrid (7) | Madrid › Fuencarral-El Pardo | 23 |
| Forêt de Rivas-Vaciamadrid (5) | Rivas-Vaciamadrid | 23 |
| Forêt de Valdetorres de Jarama (3) | Valdetorres de Jarama | 23 |
| Forêt de El Molar (2) | El Molar | 23 |
| Parque del Humedal | Coslada › Vicálvaro | 23 |
| Forêt de Valdemaqueda | Valdemaqueda | 23 |
| Forêt de Ambite | Ambite | 23 |
| Forêt de Quijorna | Quijorna | 23 |
| Forêt de Soto del Real (4) | Soto del Real | 23 |
| Bois de Boadilla del Monte (3) | Boadilla del Monte | 23 |
| Forêt de Valdemorillo (59) | Valdemorillo | 23 |
| Bois de Aranjuez (20) | Aranjuez | 23 |
| Forêt de Rivas-Vaciamadrid (54) | Rivas-Vaciamadrid | 23 |
| Forêt de San Sebastián de los Reyes | San Sebastián de los Reyes | 22 |
| Parque Forestal de Entrevías | Madrid › Puente de Vallecas | 22 |
| Bois de Alcalá de Henares (6) | Alcalá de Henares | 22 |
| Parque de Las Cruces | Madrid › Latina | 22 |
| Forêt de Cenicientos (4) | Cenicientos | 22 |
| Forêt de Navalagamella (2) | Navalagamella | 22 |
| Forêt de Colmenar del Arroyo (2) | Colmenar del Arroyo | 22 |
| Forêt de El Escorial (6) | El Escorial | 22 |
| Forêt de El Escorial (8) | El Escorial | 22 |
| Forêt de Fresnedillas de la Oliva (2) | Fresnedillas de la Oliva | 22 |
| Forêt de Valdemorillo (15) | Valdemorillo | 22 |
| Forêt de Bustarviejo (6) | Bustarviejo | 22 |
| Parque de la Casita del Príncipe | El Escorial | 21 |
| Bois de Miraflores de la Sierra | Miraflores de la Sierra | 21 |
| Bois de Villanueva del Pardillo | Villanueva del Pardillo | 21 |
| Bois de Villanueva del Pardillo (2) | Villanueva del Pardillo | 21 |
| Forêt de Brea de Tajo (2) | Brea de Tajo | 21 |
| Parque de La Gavia - La Atalayuela | Madrid › Villa de Vallecas | 21 |
| Dehesa Boyal de Serrada de la Fuente | Puentes Viejas | 21 |
| Forêt de Torrelodones (2) | Torrelodones | 21 |
| Forêt de Valdemorillo (41) | Valdemorillo | 21 |
| Forêt de Canencia (5) | Canencia | 21 |
| Bois de Villamanta (5) | Villamanta | 21 |
| Bois de Aldea del Fresno (3) | Aldea del Fresno | 21 |
| Forêt de Cenicientos (6) | Cenicientos | 21 |
| Forêt de San Lorenzo de El Escorial (15) | San Lorenzo de El Escorial | 21 |
| Finca Vista Alegre | Madrid › Carabanchel | 20 |
| Forêt de Pezuela de las Torres (2) | Pezuela de las Torres | 20 |
| Forêt de Rascafría (4) | Rascafría | 20 |
| Bois de San Fernando de Henares (5) | San Fernando de Henares | 20 |
| Forêt de Robledo de Chavela (3) | Robledo de Chavela | 20 |
| Forêt de Robledo de Chavela (14) | Robledo de Chavela | 20 |
| Forêt de Robledo de Chavela (43) | Robledo de Chavela | 20 |
| Forêt de El Atazar (4) | El Atazar | 20 |
| Forêt de Puebla de la Sierra | Puebla de la Sierra | 20 |
| Forêt de Valdemorillo (18) | Valdemorillo | 20 |
| Forêt de Robledo de Chavela (36) | Robledo de Chavela | 19 |
| Forêt de Zarzalejo (158) | Zarzalejo | 19 |
| Forêt de Valdemoro | Valdemoro | 19 |
| Bois de Moralzarzal (6) | Moralzarzal | 19 |
| Parque de Enrique Tierno Galván | Madrid › Arganzuela | 18 |
| Forêt de Bustarviejo (2) | Bustarviejo | 18 |
| Forêt de Robledo de Chavela (35) | Robledo de Chavela | 18 |
| Forêt de El Boalo-Cerceda-Mataelpino (3) | El Boalo-Cerceda-Mataelpino | 18 |
| Forêt de Valdemorillo (66) | Valdemorillo | 18 |
| Forêt de Valdemorillo (68) | Valdemorillo | 18 |
| Forêt de Boadilla del Monte (19) | Boadilla del Monte | 18 |
| Forêt de Buitrago del Lozoya (8) | Buitrago del Lozoya | 18 |
| Forêt de Valdemaqueda (30) | Valdemaqueda | 18 |
| Forêt de El Boalo-Cerceda-Mataelpino (5) | El Boalo-Cerceda-Mataelpino | 18 |
| Bois de El Escorial | El Escorial | 17 |
| Forêt de Guadalix de la Sierra (2) | Guadalix de la Sierra | 17 |
| Bois de Arganda del Rey (4) | Arganda del Rey | 17 |
| Forêt de Santa María de la Alameda (3) | Santa María de la Alameda | 17 |
| Parque Forestal de Valdebernardo | Madrid › Vicálvaro | 17 |
| Forêt de Villanueva de Perales (9) | Villanueva de Perales | 17 |
| Parque Este | Tres Cantos | 17 |
| Bois de Navalcarnero | Navalcarnero | 17 |
| Forêt de Valdemaqueda (24) | Valdemaqueda | 17 |
| Parque Forestal Julio Alguacil Gómez | Madrid › Villaverde | 17 |
| Bois de Alpedrete (4) | Alpedrete | 17 |
| Forêt de Aranjuez (155) | Aranjuez | 17 |
| Parque Cuña Verde de Vicálvaro | Madrid › Vicálvaro | 17 |
| Gran Parque de los Espartales | Alcalá de Henares | 16 |
| Forêt de Guadarrama | Guadarrama | 16 |
| Forêt de San Martín de Valdeiglesias (4) | San Martín de Valdeiglesias | 16 |
| Bois de Villanueva de Perales (2) | Villanueva de Perales | 16 |
| Forêt de Robledo de Chavela (23) | Robledo de Chavela | 16 |
| Forêt de Robledo de Chavela (37) | Robledo de Chavela | 16 |
| Forêt de San Martín de Valdeiglesias (12) | San Martín de Valdeiglesias | 16 |
| Forêt de Robledo de Chavela (44) | Robledo de Chavela | 16 |
| Forêt de Robledo de Chavela (49) | Robledo de Chavela | 16 |
| Forêt de Villa del Prado (6) | Villa del Prado | 16 |
| Forêt de Valdemorillo (3) | Valdemorillo | 16 |
| Bois de San Fernando de Henares (7) | San Fernando de Henares › Barajas | 16 |
| Parc de Madrid (820) | Madrid › Hortaleza | 16 |
| Forêt de Valdemorillo (45) | Valdemorillo | 16 |
| Forêt de Puebla de la Sierra (10) | Puebla de la Sierra | 16 |
| Bois de Chinchón (5) | Chinchón | 16 |
| Bois de Chapinería (8) | Aldea del Fresno | 16 |
| Parque Lineal de Palomeras | Madrid › Puente de Vallecas | 16 |
| Bois de Torrelaguna (17) | Torrelaguna | 16 |
| Parque Central Norte | Tres Cantos | 15 |
| Parque lineal del Arroyo Butarque (2) | Leganés | 15 |
| Bois de Soto del Real (2) | Soto del Real | 15 |
| Forêt de La Acebeda | La Acebeda | 15 |
| Forêt de Pinilla del Valle | Pinilla del Valle | 15 |
| Forêt de Sevilla la Nueva (2) | Sevilla la Nueva | 15 |
| Forêt de Patones (7) | Patones | 15 |
| Forêt de Puebla de la Sierra (7) | Puebla de la Sierra | 15 |
| Forêt de Rascafría (9) | Rascafría | 15 |
| Bois de Colmenar del Arroyo | Colmenar del Arroyo | 15 |
| Parque Forestal de Valdebernardo Sur | Madrid › Vicálvaro | 15 |
| Parque Forestal de Valdebernardo Oeste | Madrid › Vicálvaro | 15 |
| Bois de San Lorenzo de El Escorial (5) | San Lorenzo de El Escorial | 15 |
| Parc de Madrid (144) | Madrid › Vicálvaro | 14 |
| Parque Natural El Soto | Móstoles | 14 |
| Parque de Montecarmelo | Madrid › Fuencarral-El Pardo | 14 |
| Bois de Talamanca de Jarama | Talamanca de Jarama | 14 |
| Forêt de Los Santos de la Humosa (2) | Los Santos de la Humosa | 14 |
| Forêt de Robledo de Chavela (25) | Robledo de Chavela | 14 |
| Forêt de Madrid (50) | Madrid › Moncloa-Aravaca | 14 |
| Dehesa de Arriba | Robledillo de la Jara | 14 |
| Bois de Majadahonda | Majadahonda | 14 |
| Forêt de Manzanares el Real (3) | Manzanares el Real | 14 |
| Forêt de Garganta de los Montes (3) | Garganta de los Montes | 14 |
| Forêt de Valdemorillo (42) | Valdemorillo | 14 |
| Forêt de Valdemorillo (53) | Valdemorillo | 14 |
| Forêt de Pinto (3) | Getafe | 14 |
| Coto de las Suertes | Collado Villalba | 14 |
| Parque de los Alcornoques | Tres Cantos | 13 |
| Espacio natural Bolitas del Airón | Valdemoro | 13 |
| Forêt de San Martín de la Vega (2) | San Martín de la Vega | 13 |
| Forêt de Rascafría (3) | Rascafría | 13 |
| Forêt de Talamanca de Jarama | Talamanca de Jarama | 13 |
| Forêt de Quijorna (2) | Quijorna | 13 |
| Parque Forestal El Gurugú | Villa del Prado | 13 |
| Bois de Villaviciosa de Odón (4) | Villaviciosa de Odón | 13 |
| Forêt de Valdemorillo (55) | Valdemorillo | 13 |
| Forêt de Valdemorillo (62) | Valdemorillo | 13 |
| Forêt de Bustarviejo (7) | Bustarviejo | 13 |
| Bois de El Escorial (9) | El Escorial | 13 |
| Forêt de Valdemaqueda (27) | Valdemaqueda | 13 |
| Bois de Chapinería (9) | Chapinería | 13 |
| Forêt de Rivas-Vaciamadrid (51) | Rivas-Vaciamadrid | 13 |
| Forêt de Cercedilla | Cercedilla | 13 |
| Parque de las Comunidades de España | Parla | 12 |
| Bois de Talamanca de Jarama (2) | Talamanca de Jarama | 12 |
| Parque Fluvial de los Arroyos | Arroyomolinos | 12 |
| Bois de Madrid (20) | Madrid › Fuencarral-El Pardo | 12 |
| Forêt de Collado Villalba (2) | Collado Villalba | 12 |
| Bois de Navacerrada (8) | Navacerrada | 12 |
| Bois de Fresnedillas de la Oliva (2) | Fresnedillas de la Oliva | 12 |
| Bois de El Escorial (3) | El Escorial | 12 |
| Forêt de Rivas-Vaciamadrid (14) | Rivas-Vaciamadrid | 12 |
| Forêt de Patones (4) | Patones | 12 |
| Forêt de Boadilla del Monte (5) | Boadilla del Monte | 12 |
| Bois de Los Santos de la Humosa (3) | Los Santos de la Humosa | 12 |
| Forêt de Valdemorillo (35) | Valdemorillo | 12 |
| Forêt de Valdemorillo (65) | Valdemorillo | 12 |
| Bois de El Boalo-Cerceda-Mataelpino | El Boalo-Cerceda-Mataelpino | 12 |
| Forêt de Moralzarzal (2) | Moralzarzal | 12 |
| Forêt de Somosierra (26) | Somosierra | 12 |
| Parque Forestal Princesa Leonor | Alcobendas | 12 |
| Parque Forestal Princesa Leonor (2) | Alcobendas | 12 |
| Forêt de Villaviciosa de Odón (6) | Villaviciosa de Odón | 12 |
| Parque de las Autonomías | Madrid › Puente de Vallecas | 12 |
| Forêt de Guadarrama (19) | Guadarrama | 12 |
| Parque Quinta de los Molinos | Madrid › San Blas - Canillejas | 11 |
| Forêt de Alcorcón | Alcorcón | 11 |
| Forêt de Soto del Real | Soto del Real | 11 |
| Bois de San Agustín del Guadalix | San Agustín del Guadalix | 11 |
| Forêt de Villaviciosa de Odón (2) | Villaviciosa de Odón | 11 |
| Bosque del Arroyo de la Puerta Verde | Madrid › Moncloa-Aravaca | 11 |
| Bois de Mejorada del Campo (2) | Mejorada del Campo | 11 |
| Forêt de Villanueva de Perales (5) | Villanueva de Perales | 11 |
| Forêt de Robledo de Chavela (8) | Robledo de Chavela | 11 |
| Forêt de Robledo de Chavela (10) | Robledo de Chavela | 11 |
| Bois de Robledo de Chavela (2) | Robledo de Chavela | 11 |
| Forêt de Robledo de Chavela (47) | Robledo de Chavela | 11 |
| El Pinar (3) | Aranjuez | 11 |
| La Dehesilla (2) | Miraflores de la Sierra | 11 |
| Bois de Rivas-Vaciamadrid (13) | Rivas-Vaciamadrid | 11 |
| Bois de Moralzarzal (2) | Moralzarzal | 11 |
| Forêt de Velilla de San Antonio | Velilla de San Antonio | 11 |
| Bois de Las Rozas de Madrid (3) | Las Rozas de Madrid | 11 |
| Forêt de Valdemorillo (39) | Valdemorillo | 11 |
| Forêt de Valdemorillo (56) | Valdemorillo | 11 |
| Parc de Leganés (76) | Leganés | 11 |
| Forêt de San Martín de la Vega (29) | San Martín de la Vega | 11 |
| Cerro del Telégrafo | Rivas-Vaciamadrid | 11 |
| Forêt de Rivas-Vaciamadrid (53) | Rivas-Vaciamadrid | 11 |
| Parque de San Isidro | Madrid › Carabanchel | 10 |
| Parque Juan Carlos I (2) | Pinto | 10 |
| Forêt de Miraflores de la Sierra (3) | Miraflores de la Sierra | 10 |
| Parque Lineal Arroyo Culebro | Leganés | 10 |
| Parque forestal Fuente Carrantona | Madrid › Moratalaz | 10 |
| Forêt de Alcorcón (2) | Alcorcón | 10 |
| Parque de Los Miradores | Torrejón de Ardoz | 10 |
| Forêt de San Martín de la Vega (5) | Getafe | 10 |
| Bois de Valdemorillo | Valdemorillo | 10 |
| Bois de Villamanta | Villamanta | 10 |
| Forêt de Robledo de Chavela (5) | Robledo de Chavela | 10 |
| Parque Arroyo de los Combos | Arroyomolinos | 10 |
| Bois de Becerril de la Sierra (3) | Becerril de la Sierra | 10 |
| Forêt de Somosierra (16) | Somosierra | 10 |
| Forêt de El Escorial (7) | El Escorial | 10 |
| Bois de Batres (2) | Batres | 10 |
| Bois de Villanueva del Pardillo (4) | Villanueva del Pardillo | 10 |
| Forêt de Madrid (54) | Madrid › Barajas | 10 |
| Forêt de El Atazar (7) | El Atazar | 10 |
| Bois de Navalagamella | Navalagamella | 10 |
| Forêt de Garganta de los Montes (5) | Garganta de los Montes | 10 |
| Bois de Torrelaguna (7) | Torrelaguna | 10 |
| Bois de Manzanares el Real (3) | Manzanares el Real | 10 |
| Forêt de Meco | Meco | 10 |
| Forêt de Manzanares el Real (8) | Manzanares el Real | 10 |
| Forêt de Valdemorillo (37) | Valdemorillo | 10 |
| Forêt de Navalagamella (14) | Navalagamella | 10 |
| Parc de Getafe (140) | Getafe › Villaverde | 10 |
| Forêt de Aranjuez (149) | Aranjuez | 10 |
| Forêt de Aranjuez (154) | Aranjuez | 10 |
| Forêt de Aranjuez (159) | Aranjuez | 10 |
| Parc de Aranjuez (37) | Aranjuez | 10 |
| Forêt de Rivas-Vaciamadrid (50) | Rivas-Vaciamadrid | 10 |
| Forêt de Brea de Tajo (9) | Brea de Tajo | 10 |
| Forêt de Guadarrama (22) | Guadarrama | 10 |
| Parque Cuña Verde de Laguna ⚠️ | Madrid › Latina | 9 |
| Cuña Verde de la Latina ⚠️ | Madrid › Latina | 9 |
| Parque del Alcalde de Madrid Don José Luis Álvarez y Álvarez ⚠️ | Madrid › Hortaleza | 9 |
| Pinar Cerro del Águila ⚠️ | Madrid › Moncloa-Aravaca | 9 |
| Parque del Cerro Almodóvar ⚠️ | Madrid › Latina | 9 |
| Parque Europa ⚠️ | Torrejón de Ardoz | 9 |
| Bois de Mejorada del Campo ⚠️ | Mejorada del Campo | 9 |
| Parque de Santa Ana ⚠️ | Madrid › Fuencarral-El Pardo | 9 |
| Bois de Colmenar Viejo ⚠️ | Colmenar Viejo | 9 |
| Huerta del Monasterio ⚠️ | San Lorenzo de El Escorial | 9 |
| Forêt de Sevilla la Nueva (7) ⚠️ | Sevilla la Nueva | 9 |
| Forêt de Sevilla la Nueva (8) ⚠️ | Sevilla la Nueva | 9 |
| Bois de Robledo de Chavela (5) ⚠️ | Robledo de Chavela | 9 |
| Forêt de Becerril de la Sierra ⚠️ | Becerril de la Sierra | 9 |
| Forêt de Zarzalejo (12) ⚠️ | Zarzalejo | 9 |
| Parque Norte - Carmen Tagle ⚠️ | Madrid › Fuencarral-El Pardo | 9 |
| Forêt de El Escorial (22) ⚠️ | El Escorial | 9 |
| Bois de Manzanares el Real (2) ⚠️ | Manzanares el Real | 9 |
| Parque Forestal Cruz de la Atalaya ⚠️ | Pozuelo de Alarcón | 9 |
| Forêt de Aranjuez (157) ⚠️ | Aranjuez | 9 |
| Bois de Aranjuez (15) ⚠️ | Aranjuez | 9 |
| Forêt de Madrid (228) ⚠️ | Madrid › Moncloa-Aravaca | 9 |
| Bois de Aldea del Fresno ⚠️ | Aldea del Fresno | 9 |
| Jardines del Campo del Moro ⚠️ | Madrid › Centro | 9 |
| Parque de El Cerro ⚠️ | Coslada | 9 |
| Parque del Pinar de Barajas ⚠️ | Madrid › Hortaleza | 8 |
| Parque de la Poveda ⚠️ | Collado Villalba | 8 |
| Parque de Plata y Castañar ⚠️ | Madrid › Villaverde | 8 |
| Recinto Ferial ⚠️ | Coslada | 8 |
| Colada del Arroyo Viñuelas ⚠️ | San Sebastián de los Reyes | 8 |
| Parque lineal del Arroyo Butarque ⚠️ | Leganés | 8 |
| Parque de la Volatería ⚠️ | Madrid › Carabanchel | 8 |
| Parque de La Elipa ⚠️ | Madrid › Ciudad Lineal | 8 |
| Bois de Fresno de Torote ⚠️ | Fresno de Torote | 8 |
| Forêt de Arganda del Rey (2) ⚠️ | Arganda del Rey | 8 |
| Forêt de Chinchón ⚠️ | Chinchón | 8 |
| Parque Forestal El Bosque ⚠️ | Morata de Tajuña | 8 |
| Parque Arroyo Pozuelo - Fase 3 ⚠️ | Madrid › Moncloa-Aravaca | 8 |
| Forêt de Rozas de Puerto Real (3) ⚠️ | Rozas de Puerto Real | 8 |
| Forêt de La Cabrera (3) ⚠️ | La Cabrera | 8 |
| Forêt de Santa María de la Alameda (4) ⚠️ | Santa María de la Alameda | 8 |
| Forêt de Sevilla la Nueva (6) ⚠️ | Sevilla la Nueva | 8 |
| Bois de Villamantilla (10) ⚠️ | Villamantilla | 8 |
| Bois de Valdemaqueda (2) ⚠️ | Valdemaqueda | 8 |
| Bois de Robledo de Chavela (6) ⚠️ | Robledo de Chavela | 8 |
| Forêt de Robledo de Chavela (41) ⚠️ | Robledo de Chavela | 8 |
| Forêt de San Martín de Valdeiglesias (14) ⚠️ | San Martín de Valdeiglesias | 8 |
| La Pinarilla ⚠️ | Navas del Rey | 8 |
| Forêt de Somosierra (24) ⚠️ | Somosierra | 8 |
| Forêt de El Escorial (9) ⚠️ | El Escorial | 8 |
| Forêt de San Lorenzo de El Escorial (8) ⚠️ | San Lorenzo de El Escorial | 8 |
| Forêt de Madrid (53) ⚠️ | Madrid › Latina | 8 |
| Bois de Móstoles (5) ⚠️ | Móstoles | 8 |
| Forêt de Valdemaqueda (25) ⚠️ | Valdemaqueda | 8 |
| Forêt de Coslada (2) ⚠️ | Coslada | 8 |
| Parque del Pinar de Barajas (2) ⚠️ | Madrid › Hortaleza | 8 |
| Parc de Coslada (9) ⚠️ | Coslada › Vicálvaro | 8 |
| Parque de la Cabilda ⚠️ | Hoyo de Manzanares | 8 |
| Parque Forestal Cerro Almodóvar ⚠️ | Madrid › Vicálvaro | 8 |
| Forêt de Valdemorillo (16) ⚠️ | Valdemorillo | 8 |
| Forêt de Valdemorillo (40) ⚠️ | Valdemorillo | 8 |
| Forêt de Valdemorillo (50) ⚠️ | Valdemorillo | 8 |
| Parc de Valdemoro (32) ⚠️ | Valdemoro | 8 |
| Forêt de Alcalá de Henares (36) ⚠️ | Alcalá de Henares | 8 |
| Forêt de Madrid (189) ⚠️ | Madrid › Moncloa-Aravaca | 8 |
| Forêt de La Acebeda (7) ⚠️ | La Acebeda | 8 |
| Forêt de Aranjuez (161) ⚠️ | Aranjuez | 8 |
| Forêt de Aranjuez (164) ⚠️ | Aranjuez | 8 |
| Parque Forestal "Mirador del Jarama" ⚠️ | Rivas-Vaciamadrid | 8 |
| Bois de Aldea del Fresno (2) ⚠️ | Aldea del Fresno | 8 |
| Bois de Guadarrama (3) ⚠️ | Guadarrama | 8 |
| Parc de Torrelodones (21) ⚠️ | Torrelodones | 8 |
| Pinar San José ⚠️ | Madrid › Latina | 8 |
| Forêt de Guadarrama (24) ⚠️ | Guadarrama | 8 |
| Parque del Paraíso ⚠️ | Madrid › San Blas - Canillejas | 7 |
| Parque de la Huerta del Obispo ⚠️ | Madrid › Tetuán | 7 |
| Jardín histórico El Capricho de la Alameda Osuna ⚠️ | Madrid › Barajas | 7 |
| Cerro del Tío Pío ⚠️ | Madrid › Puente de Vallecas | 7 |
| Forêt de Madrid (4) ⚠️ | Madrid › Fuencarral-El Pardo | 7 |
| Bois de Madrid ⚠️ | Madrid › Fuencarral-El Pardo | 7 |
| Parc de Leganés (12) ⚠️ | Leganés | 7 |
| Forêt de El Vellón ⚠️ | El Vellón | 7 |
| Forêt de El Molar ⚠️ | El Molar | 7 |
| Bois de Daganzo de Arriba (2) ⚠️ | Daganzo de Arriba | 7 |
| Forêt de Villaviciosa de Odón (3) ⚠️ | Villaviciosa de Odón | 7 |
| Forêt de Arganda del Rey (3) ⚠️ | Arganda del Rey | 7 |
| Pinar de Las Lomas ⚠️ | Majadahonda | 7 |
| Parque del Universo ⚠️ | Parla | 7 |
| Forêt de Montejo de la Sierra (4) ⚠️ | Montejo de la Sierra | 7 |
| Forêt de Canencia (2) ⚠️ | Canencia | 7 |
| Forêt de Brunete (4) ⚠️ | Brunete | 7 |
| Forêt de Navalagamella (5) ⚠️ | Navalagamella | 7 |
| Forêt de Colmenar del Arroyo (3) ⚠️ | Colmenar del Arroyo | 7 |
| Forêt de Robledo de Chavela (39) ⚠️ | Robledo de Chavela | 7 |
| Forêt de Valdemaqueda (7) ⚠️ | Valdemaqueda | 7 |
| Forêt de Madrid (36) ⚠️ | Madrid › Moncloa-Aravaca | 7 |
| Forêt de Robledo de Chavela (45) ⚠️ | Robledo de Chavela | 7 |
| Forêt de Valdemaqueda (16) ⚠️ | Valdemaqueda | 7 |
| Forêt de Manzanares el Real ⚠️ | Manzanares el Real | 7 |
| Bois de San Martín de Valdeiglesias (2) ⚠️ | San Martín de Valdeiglesias | 7 |
| La Dehesilla ⚠️ | Miraflores de la Sierra | 7 |
| Forêt de Somosierra (9) ⚠️ | Somosierra | 7 |
| Forêt de El Escorial (14) ⚠️ | El Escorial | 7 |
| Forêt de Zarzalejo (126) ⚠️ | Zarzalejo | 7 |
| Parque Forestal M-40 ⚠️ | Madrid › Villa de Vallecas | 7 |
| Bois de Batres (3) ⚠️ | Navalcarnero | 7 |
| Forêt de El Atazar (2) ⚠️ | El Atazar | 7 |
| Forêt de Manzanares el Real (5) ⚠️ | Manzanares el Real | 7 |
| Forêt de Robledillo de la Jara (3) ⚠️ | Robledillo de la Jara | 7 |
| Bois de Collado Mediano ⚠️ | Collado Mediano | 7 |
| Parc de Madrid (809) ⚠️ | Madrid › Fuencarral-El Pardo | 7 |
| Campo de radiación gamma de El Encín ⚠️ | Alcalá de Henares | 7 |
| Bois de Manzanares el Real (4) ⚠️ | Manzanares el Real | 7 |
| Forêt de Boadilla del Monte (7) ⚠️ | Boadilla del Monte | 7 |
| Parc de Meco (7) ⚠️ | Meco | 7 |
| Parc de Paracuellos de Jarama (41) ⚠️ | Paracuellos de Jarama | 7 |
| Bois de Los Santos de la Humosa (8) ⚠️ | Los Santos de la Humosa | 7 |
| Parque Agustín Rodríguez Sahagún ⚠️ | Madrid › Tetuán | 7 |
| Forêt de Valdemorillo (70) ⚠️ | Valdemorillo | 7 |
| Parque de Valmores ⚠️ | Nuevo Baztán | 7 |
| Parque Urbano de Entrevías ⚠️ | Madrid › Puente de Vallecas | 7 |
| Parc de Getafe (138) ⚠️ | Getafe | 7 |
| Bois de Ciempozuelos (2) ⚠️ | Ciempozuelos | 7 |
| Bois de Villamantilla (14) ⚠️ | Villamantilla | 7 |
| Forêt de Rascafría (12) ⚠️ | Rascafría | 7 |
| Forêt de Lozoya (5) ⚠️ | Lozoya | 7 |
| Forêt de Torrelodones (3) ⚠️ | Torrelodones | 7 |
| Encinar ⚠️ | Aranjuez | 7 |
| Parc de Pozuelo de Alarcón (148) ⚠️ | Pozuelo de Alarcón | 7 |
| Parque de La Ventilla ⚠️ | Madrid › Tetuán | 6 |
| Parc de Boadilla del Monte ⚠️ | Boadilla del Monte | 6 |
| Forêt de Villanueva de la Cañada ⚠️ | Villanueva de la Cañada | 6 |
| Forêt de Galapagar (3) ⚠️ | Galapagar | 6 |
| Parque Valdegrullas ⚠️ | Leganés | 6 |
| Parque de la Hispanidad ⚠️ | Leganés | 6 |
| Bois de Chinchón ⚠️ | Chinchón | 6 |
| Parque Finca Liana ⚠️ | Móstoles | 6 |
| Parque Nelson Mandela ⚠️ | Móstoles | 6 |
| Parque Ciudad de Mayarí ⚠️ | Alcorcón | 6 |
| Forêt de Valdetorres de Jarama ⚠️ | Valdetorres de Jarama | 6 |
| Zona Verde El Capricho ⚠️ | Madrid › Barajas | 6 |
| Bois de Algete ⚠️ | Algete | 6 |
| Parc de Villanueva de la Cañada (16) ⚠️ | Villanueva de la Cañada | 6 |
| Sabinar de Lozoya ⚠️ | Lozoya | 6 |
| Pinar de Polvoranca ⚠️ | Leganés | 6 |
| Forêt de Sevilla la Nueva (4) ⚠️ | Sevilla la Nueva | 6 |
| Forêt de Robledo de Chavela (2) ⚠️ | Robledo de Chavela | 6 |
| Forêt de Valdemaqueda (8) ⚠️ | Valdemaqueda | 6 |
| Forêt de Robledo de Chavela (40) ⚠️ | Robledo de Chavela | 6 |
| Forêt de Santa María de la Alameda (9) ⚠️ | Santa María de la Alameda | 6 |
| Forêt de Brea de Tajo (5) ⚠️ | Brea de Tajo | 6 |
| Forêt de Madrid (49) ⚠️ | Madrid › Moncloa-Aravaca | 6 |
| Forêt de El Escorial (5) ⚠️ | El Escorial | 6 |
| Forêt de Valdemorillo (7) ⚠️ | Valdemorillo | 6 |
| Bois de Rivas-Vaciamadrid (5) ⚠️ | Rivas-Vaciamadrid | 6 |
| Forêt de Tres Cantos (3) ⚠️ | Tres Cantos | 6 |
| Forêt de Alameda del Valle ⚠️ | Alameda del Valle | 6 |
| Parc de Alcobendas (53) ⚠️ | Alcobendas | 6 |
| Forêt de Rivas-Vaciamadrid (12) ⚠️ | Rivas-Vaciamadrid | 6 |
| Forêt de Rivas-Vaciamadrid (13) ⚠️ | Rivas-Vaciamadrid | 6 |
| Forêt de El Atazar (3) ⚠️ | El Atazar | 6 |
| Forêt de Puebla de la Sierra (2) ⚠️ | Puebla de la Sierra | 6 |
| Parque de la Virgen Blanca ⚠️ | Madrid › Moncloa-Aravaca | 6 |
| Forêt de Nuevo Baztán (3) ⚠️ | Nuevo Baztán | 6 |
| Forêt de Madrid (71) ⚠️ | Madrid › Moncloa-Aravaca | 6 |
| Forêt de Valdemorillo (44) ⚠️ | Valdemorillo | 6 |
| Forêt de Valdemorillo (64) ⚠️ | Valdemorillo | 6 |
| Forêt de Bustarviejo (5) ⚠️ | Bustarviejo | 6 |
| Bois de Moralzarzal (4) ⚠️ | Moralzarzal | 6 |
| Forêt de Puebla de la Sierra (5) ⚠️ | Puebla de la Sierra | 6 |
| Parque Lineal Manolito Gafotas ⚠️ | Madrid › Carabanchel | 6 |
| Pinar de Doña Consuelo ⚠️ | Majadahonda | 6 |
| Forêt de Valdemorillo (73) ⚠️ | Valdemorillo | 6 |
| Bois de Pinto (2) ⚠️ | Pinto | 6 |
| Forêt de Aranjuez (148) ⚠️ | Aranjuez | 6 |
| Forêt de Rivas-Vaciamadrid (43) ⚠️ | Rivas-Vaciamadrid | 6 |
| Forêt de Aldea del Fresno (4) ⚠️ | Aldea del Fresno | 6 |
| Parque de la Bombilla ⚠️ | Madrid › Moncloa-Aravaca | 5 |
| Parque de Andalucía ⚠️ | Alcobendas | 5 |
| Parque Cuña Verde Oeste ⚠️ | Madrid › Latina | 5 |
| Parque del Arroyo Pozuelo ⚠️ | Madrid › Moncloa-Aravaca | 5 |
| La Herrería ⚠️ | San Lorenzo de El Escorial | 5 |
| Parque Payaso Fofó ⚠️ | Madrid › Puente de Vallecas | 5 |
| Parc de Boadilla del Monte (18) ⚠️ | Boadilla del Monte | 5 |
| Forêt de Galapagar ⚠️ | Galapagar | 5 |
| Parque del Arroyo Fontarrón ⚠️ | Madrid › Moratalaz | 5 |
| Bois de San Fernando de Henares (3) ⚠️ | San Fernando de Henares | 5 |
| Bois de Pelayos de la Presa ⚠️ | Pelayos de la Presa | 5 |
| Parque de los Frailes ⚠️ | Leganés | 5 |
| Forêt de Madrid (10) ⚠️ | Madrid › Latina | 5 |
| Bois de Miraflores de la Sierra (2) ⚠️ | Miraflores de la Sierra | 5 |
| Bois de Alcalá de Henares (4) ⚠️ | Alcalá de Henares | 5 |
| Forêt de Algete ⚠️ | Algete | 5 |
| Bois de Las Rozas de Madrid ⚠️ | Las Rozas de Madrid | 5 |
| Bois de Rivas-Vaciamadrid (3) ⚠️ | Rivas-Vaciamadrid | 5 |
| Valdezarza ⚠️ | Chinchón | 5 |
| Forêt de Valdemorillo (2) ⚠️ | Valdemorillo | 5 |
| Parque de La Manguilla ⚠️ | El Escorial | 5 |
| Bois de Tres Cantos ⚠️ | Tres Cantos | 5 |
| Forêt de Montejo de la Sierra (2) ⚠️ | Montejo de la Sierra | 5 |
| Forêt de La Cabrera (7) ⚠️ | La Cabrera | 5 |
| Parc de Madrid (405) ⚠️ | Madrid › Villa de Vallecas | 5 |
| Bois de Torrelodones (2) ⚠️ | Torrelodones | 5 |
| Forêt de Navalagamella ⚠️ | Navalagamella | 5 |
| Forêt de Villanueva de Perales ⚠️ | Villanueva de Perales | 5 |
| Forêt de Villanueva de Perales (3) ⚠️ | Villanueva de Perales | 5 |
| Forêt de Villanueva de Perales (7) ⚠️ | Villanueva de Perales | 5 |
| Forêt de Quijorna (3) ⚠️ | Quijorna | 5 |
| Forêt de Robledo de Chavela (6) ⚠️ | Robledo de Chavela | 5 |
| Forêt de Robledo de Chavela (18) ⚠️ | Robledo de Chavela | 5 |
| Forêt de Robledo de Chavela (19) ⚠️ | Robledo de Chavela | 5 |
| Bois de Robledo de Chavela (4) ⚠️ | Robledo de Chavela | 5 |
| Forêt de Robledo de Chavela (34) ⚠️ | Robledo de Chavela | 5 |
| Forêt de Zarzalejo (2) ⚠️ | Zarzalejo | 5 |
| Forêt de El Escorial (3) ⚠️ | El Escorial | 5 |
| Arboreto Mediterráneo Dehesa del Batán ⚠️ | Alcalá de Henares | 5 |
| Bois de El Escorial (5) ⚠️ | El Escorial | 5 |
| Forêt de El Escorial (12) ⚠️ | El Escorial | 5 |
| Forêt de El Escorial (13) ⚠️ | El Escorial | 5 |
| Forêt de San Martín de la Vega (9) ⚠️ | San Martín de la Vega | 5 |
| Forêt de El Escorial (20) ⚠️ | El Escorial | 5 |
| Forêt de Valdemorillo (4) ⚠️ | Valdemorillo | 5 |
| Bois de Redueña (5) ⚠️ | Redueña | 5 |
| Bois de Cabanillas de la Sierra ⚠️ | Cabanillas de la Sierra | 5 |
| Forêt de Moraleja de Enmedio (2) ⚠️ | Moraleja de Enmedio | 5 |
| Forêt de Rivas-Vaciamadrid (27) ⚠️ | Rivas-Vaciamadrid | 5 |
| Forêt de El Atazar ⚠️ | El Atazar | 5 |
| Forêt de Soto del Real (3) ⚠️ | Soto del Real | 5 |
| Bois de Batres (5) ⚠️ | Batres | 5 |
| Parc de Pinto (15) ⚠️ | Pinto | 5 |
| Parque Ana de Austria ⚠️ | Madrid › Hortaleza | 5 |
| Forêt de Nuevo Baztán (6) ⚠️ | Nuevo Baztán | 5 |
| Parque de la Azuda ⚠️ | Aranjuez | 5 |
| Parc de Parla (25) ⚠️ | Parla | 5 |
| Bois de Arroyomolinos (3) ⚠️ | Arroyomolinos | 5 |
| Forêt de Manzanares el Real (9) ⚠️ | Manzanares el Real | 5 |
| Bois de Manzanares el Real (16) ⚠️ | Manzanares el Real | 5 |
| Parque Sierra Miramadrid ⚠️ | Paracuellos de Jarama | 5 |
| Forêt de Valdemorillo (22) ⚠️ | Valdemorillo | 5 |
| Forêt de Valdemorillo (31) ⚠️ | Valdemorillo | 5 |
| Forêt de Navalagamella (18) ⚠️ | Navalagamella | 5 |
| Parc de Torrelodones (20) ⚠️ | Torrelodones | 5 |
| Forêt de Pozuelo de Alarcón (15) ⚠️ | Pozuelo de Alarcón | 5 |
| Forêt de Bustarviejo (8) ⚠️ | Bustarviejo | 5 |
| Parc de Leganés (77) ⚠️ | Leganés | 5 |
| Ampliación Norte del Parque forestal Julio Alguacil Gómez ⚠️ | Madrid › Villaverde | 5 |
| Forêt de Getafe (7) ⚠️ | Getafe | 5 |
| Bois de Colmenar de Oreja (11) ⚠️ | Colmenar de Oreja | 5 |
| Bois de Alcalá de Henares (7) ⚠️ | Alcalá de Henares | 5 |
| Bois de Las Rozas de Madrid (7) ⚠️ | Las Rozas de Madrid | 5 |
| Forêt de San Sebastián de los Reyes (5) ⚠️ | San Sebastián de los Reyes | 5 |
| Bois de Las Rozas de Madrid (14) ⚠️ | Las Rozas de Madrid | 5 |
| Forêt de Aranjuez (175) ⚠️ | Aranjuez | 5 |
| Bois de San Fernando de Henares (30) ⚠️ | San Fernando de Henares | 5 |
| Forêt de Madrid (241) ⚠️ | Madrid › Moncloa-Aravaca | 5 |
| Forêt de Corpa (8) ⚠️ | Corpa | 5 |
| Parque Central Sur ⚠️ | Tres Cantos | 5 |
| Bois de Majadahonda (4) ⚠️ | Majadahonda | 5 |
| Bois de Torrelaguna (16) ⚠️ | Torrelaguna | 5 |
| Bois de Torrelaguna (18) ⚠️ | Torrelaguna | 5 |
| Bois de Torrelaguna (20) ⚠️ | Torrelaguna | 5 |
| Gran Parque Felipe VI ⚠️ | Majadahonda | 5 |
| Forêt de Somosierra (32) ⚠️ | Somosierra | 5 |
| Parc de Boadilla del Monte (91) ⚠️ | Boadilla del Monte | 5 |
| Forêt de Guadarrama (20) ⚠️ | Guadarrama | 5 |
| Bosque Metropolitano - Barrio Butarque ⚠️ | Madrid › Villaverde | 5 |
| Parque de la Ermita del Santo ⚠️ | Madrid › Latina | 5 |
| Parc de Madrid (17) ⚠️ | Madrid › Latina | 4 |
| Parque de Berlín ⚠️ | Madrid › Chamartín | 4 |
| Parque de Arroyo del Fresno Tomás y Valiente ⚠️ | Madrid › Fuencarral-El Pardo | 4 |
| Parc de Torrejón de Ardoz (2) ⚠️ | Torrejón de Ardoz | 4 |
| Parc de Madrid (119) ⚠️ | Madrid › Ciudad Lineal | 4 |
| Forêt de Navalcarnero ⚠️ | Navalcarnero | 4 |
| Parc de Madrid (149) ⚠️ | Madrid › Puente de Vallecas | 4 |
| Prado Ovejero ⚠️ | Móstoles | 4 |
| Forêt de Guadalix de la Sierra ⚠️ | Guadalix de la Sierra | 4 |
| Dimonio ⚠️ | San Sebastián de los Reyes | 4 |
| Bois de Valdemoro ⚠️ | Valdemoro | 4 |
| Forêt de Coslada ⚠️ | Coslada | 4 |
| Parque de los Cipreses ⚠️ | Leganés | 4 |
| Parque Dehesa Boyal ⚠️ | Madrid › Villaverde | 4 |
| Parc de Madrid (171) ⚠️ | Madrid › Puente de Vallecas | 4 |
| Parc de Madrid (172) ⚠️ | Madrid › Puente de Vallecas | 4 |
| Parque del Espinillo ⚠️ | Madrid › Villaverde | 4 |
| Bois de Chinchón (2) ⚠️ | Chinchón | 4 |
| Parque Cuesta del Reventón ⚠️ | Majadahonda | 4 |
| Parque Buenavista ⚠️ | Getafe | 4 |
| Parque Colonia Zofío ⚠️ | Madrid › Usera | 4 |
| Parque de las Cárcavas ⚠️ | Pozuelo de Alarcón | 4 |
| Forêt de Madrid (8) ⚠️ | Madrid › Moncloa-Aravaca | 4 |
| Parque Peyas ⚠️ | Coslada | 4 |
| Forêt de Alcobendas ⚠️ | Alcobendas | 4 |
| Parque del Cerro del Aire ⚠️ | Majadahonda | 4 |
| Parque del Río ⚠️ | Soto del Real | 4 |
| Parque de Bellavista ⚠️ | Rivas-Vaciamadrid | 4 |
| Forêt de Anchuelo ⚠️ | Anchuelo | 4 |
| Forêt de San Martín de la Vega (7) ⚠️ | San Martín de la Vega | 4 |
| Forêt de Arganda del Rey ⚠️ | Arganda del Rey | 4 |
| Bois de Algete (2) ⚠️ | San Sebastián de los Reyes | 4 |
| Forêt de Paracuellos de Jarama (2) ⚠️ | Paracuellos de Jarama | 4 |
| Bois de San Sebastián de los Reyes (2) ⚠️ | San Sebastián de los Reyes | 4 |
| Forêt de Las Rozas de Madrid (5) ⚠️ | Las Rozas de Madrid | 4 |
| Forêt de Madrid (20) ⚠️ | Madrid › Fuencarral-El Pardo | 4 |
| Forêt de Cenicientos (2) ⚠️ | Cenicientos | 4 |
| Forêt de Canencia (3) ⚠️ | Canencia | 4 |
| Forêt de Madrid (24) ⚠️ | Madrid › Moncloa-Aravaca | 4 |
| Forêt de Brunete (2) ⚠️ | Brunete | 4 |
| Forêt de Sevilla la Nueva (10) ⚠️ | Sevilla la Nueva | 4 |
| Forêt de Navalagamella (4) ⚠️ | Navalagamella | 4 |
| Parque de la Olla ⚠️ | Fuenlabrada | 4 |
| Bois de Zarzalejo (2) ⚠️ | Zarzalejo | 4 |
| Parque Fuente Cisneros ⚠️ | Alcorcón | 4 |
| Forêt de Valdemaqueda (13) ⚠️ | Valdemaqueda | 4 |
| Forêt de Alcorcón (3) ⚠️ | Alcorcón | 4 |
| Parque del Norte ⚠️ | Fuenlabrada | 4 |
| Forêt de Paracuellos de Jarama (4) ⚠️ | Paracuellos de Jarama | 4 |
| Forêt de Somosierra (6) ⚠️ | Somosierra | 4 |
| Forêt de Somosierra (7) ⚠️ | Somosierra | 4 |
| Bois de Fresnedillas de la Oliva (3) ⚠️ | Fresnedillas de la Oliva | 4 |
| Bois de Fresnedillas de la Oliva (5) ⚠️ | Fresnedillas de la Oliva | 4 |
| Bois de Robledo de Chavela (19) ⚠️ | Robledo de Chavela | 4 |
| Parc de Alcobendas (17) ⚠️ | Alcobendas | 4 |
| Bois de El Escorial (6) ⚠️ | El Escorial | 4 |
| Forêt de Zarzalejo (72) ⚠️ | Zarzalejo | 4 |
| Forêt de El Escorial (18) ⚠️ | El Escorial | 4 |
| Forêt de El Escorial (19) ⚠️ | El Escorial | 4 |
| Forêt de Valdemorillo (6) ⚠️ | Valdemorillo | 4 |
| Bois de Aranjuez (2) ⚠️ | Aranjuez | 4 |
| Bois de El Escorial (7) ⚠️ | El Escorial | 4 |
| Bois de El Escorial (8) ⚠️ | El Escorial | 4 |
| Parque Norte (3) ⚠️ | Villalbilla | 4 |
| Forêt de Villanueva de la Cañada (2) ⚠️ | Villanueva de la Cañada | 4 |
| Forêt de Arroyomolinos ⚠️ | Arroyomolinos | 4 |
| Bois de Pozuelo de Alarcón (6) ⚠️ | Madrid › Latina | 4 |
| Forêt de Rivas-Vaciamadrid (15) ⚠️ | Rivas-Vaciamadrid | 4 |
| Futura ampliación del parque de La Marina ⚠️ | San Sebastián de los Reyes | 4 |
| El pinar ⚠️ | El Álamo | 4 |
| Forêt de Robledillo de la Jara (2) ⚠️ | Robledillo de la Jara | 4 |
| Forêt de El Atazar (8) ⚠️ | El Atazar | 4 |
| Bois de Boadilla del Monte ⚠️ | Boadilla del Monte | 4 |
| Parc de Pinto (14) ⚠️ | Pinto | 4 |
| Parc de Alpedrete (4) ⚠️ | Alpedrete | 4 |
| Bois de Nuevo Baztán ⚠️ | Nuevo Baztán | 4 |
| Bois de Valverde de Alcalá (4) ⚠️ | Valverde de Alcalá | 4 |
| Forêt de Rivas-Vaciamadrid (38) ⚠️ | Rivas-Vaciamadrid | 4 |
| Parc de Getafe (51) ⚠️ | Getafe | 4 |
| Área Natural Barranco de Majalacabra ⚠️ | Las Rozas de Madrid | 4 |
| Parque de Alamedillas ⚠️ | Madrid › Fuencarral-El Pardo | 4 |
| Forêt de San Martín de la Vega (15) ⚠️ | San Martín de la Vega | 4 |
| Parc de San Sebastián de los Reyes (34) ⚠️ | San Sebastián de los Reyes | 4 |
| Parc de San Sebastián de los Reyes (70) ⚠️ | San Sebastián de los Reyes | 4 |
| Parc de San Sebastián de los Reyes (84) ⚠️ | San Sebastián de los Reyes | 4 |
| Forêt de Ambite (4) ⚠️ | Ambite | 4 |
| Forêt de Manzanares el Real (7) ⚠️ | Manzanares el Real | 4 |
| Forêt de Manzanares el Real (10) ⚠️ | Manzanares el Real | 4 |
| Parque Semifosteral Metropolitano ⚠️ | Madrid › San Blas - Canillejas | 4 |
| Bois de Boadilla del Monte (4) ⚠️ | Boadilla del Monte | 4 |
| Forêt de Valdemorillo (10) ⚠️ | Valdemorillo | 4 |
| Parc de Madrid (1054) ⚠️ | Madrid › Latina | 4 |
| Forêt de Valdemorillo (27) ⚠️ | Valdemorillo | 4 |
| Forêt de Valdemorillo (28) ⚠️ | Valdemorillo | 4 |
| Bois de Belmonte de Tajo (3) ⚠️ | Belmonte de Tajo | 4 |
| Forêt de Valdemorillo (60) ⚠️ | Valdemorillo | 4 |
| Parque de la Berzosa ⚠️ | Hoyo de Manzanares | 4 |
| Antiguo hipódromo ⚠️ | Nuevo Baztán | 4 |
| Parc de Villar del Olmo (2) ⚠️ | Villar del Olmo | 4 |
| Forêt de Bustarviejo (9) ⚠️ | Bustarviejo | 4 |
| Bosque Metropolitano - Avenida Talgo ⚠️ | Madrid › Moncloa-Aravaca | 4 |
| Forêt de Alcalá de Henares (37) ⚠️ | Alcalá de Henares | 4 |
| Quinta de Vista Alegre ⚠️ | Madrid › Carabanchel | 4 |
| Bosque Metropolitano Campo de las Naciones-Ribera del Sena ⚠️ | Madrid › Hortaleza | 4 |
| Forêt de Puebla de la Sierra (8) ⚠️ | Puebla de la Sierra | 4 |
| Parque Cerro Cascabel ⚠️ | Las Rozas de Madrid | 4 |
| Parc de Las Rozas de Madrid (61) ⚠️ | Las Rozas de Madrid | 4 |
| Parque Lineal de la Ronda de las Naciones Unidas (10) ⚠️ | Alcorcón | 4 |
| Parque Lineal de la Ronda de las Naciones Unidas (11) ⚠️ | Alcorcón | 4 |
| Parc de Las Rozas de Madrid (62) ⚠️ | Las Rozas de Madrid | 4 |
| Parc de Rivas-Vaciamadrid (89) ⚠️ | Rivas-Vaciamadrid | 4 |
| Parc de Valdemorillo (29) ⚠️ | Valdemorillo | 4 |
| Forêt de El Escorial (35) ⚠️ | El Escorial | 4 |
| Bois de San Fernando de Henares (16) ⚠️ | San Fernando de Henares | 4 |
| Forêt de Somosierra (30) ⚠️ | Somosierra | 4 |
| Forêt de Navarredonda y San Mamés (2) ⚠️ | Navarredonda y San Mamés | 4 |
| Forêt de Aranjuez (166) ⚠️ | Aranjuez | 4 |
| Forêt de Rivas-Vaciamadrid (46) ⚠️ | Rivas-Vaciamadrid | 4 |
| Parc de Madrid (1414) ⚠️ | Madrid › Carabanchel | 4 |
| Bois de Villamantilla (15) ⚠️ | Villamantilla | 4 |
| Bois de Rivas-Vaciamadrid (22) ⚠️ | Rivas-Vaciamadrid | 4 |
| Forêt de Guadarrama (14) ⚠️ | Guadarrama | 4 |
| Parque de la Quinta de la Fuente del Berro ⚠️ | Madrid › Salamanca | 4 |
| Parque de Pan Bendito ⚠️ | Madrid › Carabanchel | 4 |
| Bois de Getafe (3) ⚠️ | Getafe | 4 |
| Explanada de Puente del Rey ⚠️ | Madrid › Moncloa-Aravaca | 4 |
| Forêt de Guadarrama (21) ⚠️ | Guadarrama | 4 |
| Parque de Aluche ⚠️ | Madrid › Latina | 3 |
| Parc de Madrid (9) ⚠️ | Madrid › San Blas - Canillejas | 3 |
| Parque del Cuarto Depósito ⚠️ | Madrid › Chamartín | 3 |
| Real Jardín Botánico Alfonso XIII ⚠️ | Madrid › Moncloa-Aravaca | 3 |
| Parc de Madrid (44) ⚠️ | Madrid › Arganzuela | 3 |
| Parque Euskadi ⚠️ | San Sebastián de los Reyes | 3 |
| Parc de Boadilla del Monte (2) ⚠️ | Boadilla del Monte | 3 |
| Parque de Eugenia de Montijo ⚠️ | Madrid › Carabanchel | 3 |
| Parque de las Veredillas ⚠️ | Torrejón de Ardoz | 3 |
| Parque de La Marina ⚠️ | San Sebastián de los Reyes | 3 |
| Parque Laguna del Carrizal ⚠️ | Collado Villalba | 3 |
| Parc de Madrid (138) ⚠️ | Madrid › Fuencarral-El Pardo | 3 |
| Parque Enrique Tierno Galván ⚠️ | Valdemoro | 3 |
| Parque del Olivar ⚠️ | Fuenlabrada | 3 |
| Parque Cerro de los Perdigones ⚠️ | Pozuelo de Alarcón | 3 |
| Parque de La Paz ⚠️ | Alcorcón | 3 |
| Parque de Asturias ⚠️ | Rivas-Vaciamadrid | 3 |
| Parque de las Avenidas ⚠️ | Madrid › Salamanca | 3 |
| Parque de Andalucía (2) ⚠️ | Getafe | 3 |
| Forêt de Madrid (5) ⚠️ | Madrid › Villaverde | 3 |
| Parque de Buenavista ⚠️ | Madrid › Carabanchel | 3 |
| Parque la República ⚠️ | Alcorcón | 3 |
| Parque París ⚠️ | Las Rozas de Madrid | 3 |
| Parc de Madrid (189) ⚠️ | Madrid › Usera | 3 |
| Forêt de San Fernando de Henares ⚠️ | San Fernando de Henares | 3 |
| Parque de Caramuel ⚠️ | Madrid › Latina | 3 |
| Parc de Leganés (3) ⚠️ | Leganés | 3 |
| Forêt de Villa del Prado ⚠️ | Villa del Prado | 3 |
| Bois de Madrid (3) ⚠️ | Madrid › Latina | 3 |
| Parc de Leganés (8) ⚠️ | Leganés | 3 |
| Parque de la Virgen del Puerto ⚠️ | Madrid › Centro | 3 |
| Parc de Coslada ⚠️ | Coslada | 3 |
| Parc de Alcobendas (6) ⚠️ | Alcobendas | 3 |
| Parque de Fuencarral ⚠️ | Madrid › Fuencarral-El Pardo | 3 |
| Parque Occidente-Las Mercedes ⚠️ | Madrid › San Blas - Canillejas | 3 |
| Parque del Encuentro ⚠️ | Rivas-Vaciamadrid | 3 |
| Parc de Madrid (264) ⚠️ | Madrid › Villaverde | 3 |
| Forêt de Rivas-Vaciamadrid (3) ⚠️ | Rivas-Vaciamadrid | 3 |
| Bois de Rivas-Vaciamadrid (2) ⚠️ | Rivas-Vaciamadrid | 3 |
| Parc de Madrid (283) ⚠️ | Madrid › San Blas - Canillejas | 3 |
| Bois de Valdepiélagos ⚠️ | Valdepiélagos | 3 |
| Bois de San Fernando de Henares (4) ⚠️ | San Fernando de Henares | 3 |
| Forêt de Paracuellos de Jarama (3) ⚠️ | Paracuellos de Jarama | 3 |
| Bois de San Sebastián de los Reyes ⚠️ | Algete | 3 |
| Bois de Pozuelo de Alarcón (5) ⚠️ | Pozuelo de Alarcón | 3 |
| Bois de Rivas-Vaciamadrid (4) ⚠️ | Rivas-Vaciamadrid | 3 |
| Bois de Alcalá de Henares (5) ⚠️ | Alcalá de Henares | 3 |
| Forêt de Las Rozas de Madrid (2) ⚠️ | Las Rozas de Madrid | 3 |
| Parque de Santa Teresa ⚠️ | Colmenar Viejo | 3 |
| Bois de Campo Real ⚠️ | Campo Real | 3 |
| Parc de San Agustín del Guadalix ⚠️ | San Agustín del Guadalix | 3 |
| Parque Grande ⚠️ | Torrejón de Ardoz | 3 |
| Forêt de Navacerrada ⚠️ | Navacerrada | 3 |
| Forêt de San Martín de Valdeiglesias (2) ⚠️ | San Martín de Valdeiglesias | 3 |
| Forêt de Santa María de la Alameda (2) ⚠️ | Santa María de la Alameda | 3 |
| Forêt de Rozas de Puerto Real (6) ⚠️ | Rozas de Puerto Real | 3 |
| Forêt de La Cabrera ⚠️ | La Cabrera | 3 |
| Forêt de Madrid (21) ⚠️ | Madrid › Moncloa-Aravaca | 3 |
| Forêt de Madrid (22) ⚠️ | Madrid › Moncloa-Aravaca | 3 |
| Forêt de Madrid (32) ⚠️ | Madrid › Moncloa-Aravaca | 3 |
| Parque de Goya ⚠️ | Majadahonda | 3 |
| Parc de Madrid (413) ⚠️ | Madrid › Villa de Vallecas | 3 |
| Parque La Carpetania ⚠️ | Getafe | 3 |
| Parque Alfredo Nobel ⚠️ | Alcorcón | 3 |
| Parque del Paseo de los Chopos ⚠️ | San Fernando de Henares | 3 |
| Forêt de Rivas-Vaciamadrid (10) ⚠️ | Rivas-Vaciamadrid | 3 |
| El Prado de la Casa ⚠️ | Humanes de Madrid | 3 |
| Forêt de Sevilla la Nueva (11) ⚠️ | Sevilla la Nueva | 3 |
| Bois de Villamantilla (8) ⚠️ | Villamantilla | 3 |
| Bois de Villamantilla (9) ⚠️ | Villamantilla | 3 |
| Forêt de Colmenar del Arroyo (4) ⚠️ | Colmenar del Arroyo | 3 |
| Forêt de Robledo de Chavela (7) ⚠️ | Robledo de Chavela | 3 |
| Bois de Robledo de Chavela (3) ⚠️ | Robledo de Chavela | 3 |
| Forêt de Robledo de Chavela (24) ⚠️ | Robledo de Chavela | 3 |
| Forêt de Valdemaqueda (4) ⚠️ | Valdemaqueda | 3 |
| Forêt de Valdemaqueda (9) ⚠️ | Valdemaqueda | 3 |
| Parque del Barranco del Médico ⚠️ | Arroyomolinos | 3 |
| Forêt de Santa María de la Alameda (18) ⚠️ | Santa María de la Alameda | 3 |
| Forêt de Santa María de la Alameda (24) ⚠️ | Santa María de la Alameda | 3 |
| Forêt de Santa María de la Alameda (33) ⚠️ | Santa María de la Alameda | 3 |
| Forêt de Valdemaqueda (17) ⚠️ | Valdemaqueda | 3 |
| Bois de Navacerrada ⚠️ | Navacerrada | 3 |
| Bois de Manzanares el Real ⚠️ | Manzanares el Real | 3 |
| Bois de Navacerrada (4) ⚠️ | Navacerrada | 3 |
| Bois de Navacerrada (7) ⚠️ | Navacerrada | 3 |
| Forêt de Somosierra (8) ⚠️ | Somosierra | 3 |
| Bois de Quijorna (4) ⚠️ | Quijorna | 3 |
| Forêt de El Escorial (10) ⚠️ | El Escorial | 3 |
| Forêt de Zarzalejo (17) ⚠️ | Zarzalejo | 3 |
| Forêt de Zarzalejo (95) ⚠️ | Zarzalejo | 3 |
| Forêt de Zarzalejo (132) ⚠️ | Zarzalejo | 3 |
| Parque de Tierno Galván ⚠️ | San Martín de la Vega | 3 |
| Forêt de Valdemorillo (5) ⚠️ | Valdemorillo | 3 |
| Forêt de Villanueva del Pardillo (3) ⚠️ | Villanueva del Pardillo | 3 |
| Bois de Galapagar (3) ⚠️ | Galapagar | 3 |
| Bois de Fuenlabrada (2) ⚠️ | Fuenlabrada | 3 |
| Forêt de Tres Cantos ⚠️ | Tres Cantos | 3 |
| Forêt de Valdemorillo (8) ⚠️ | Valdemorillo | 3 |
| Parc de Getafe (30) ⚠️ | Getafe | 3 |
| Forêt de Rivas-Vaciamadrid (20) ⚠️ | Rivas-Vaciamadrid | 3 |
| Forêt de Rivas-Vaciamadrid (28) ⚠️ | Rivas-Vaciamadrid | 3 |
| Bois de Rivas-Vaciamadrid (10) ⚠️ | Rivas-Vaciamadrid | 3 |
| Forêt de El Atazar (6) ⚠️ | El Atazar | 3 |
| Parque Adolfo Suárez (3) ⚠️ | Valdemoro | 3 |
| Parc de Madrid (624) ⚠️ | Madrid › Fuencarral-El Pardo | 3 |
| Parc de Pinto (11) ⚠️ | Pinto | 3 |
| Parc de Pinto (12) ⚠️ | Pinto | 3 |
| Forêt de Garganta de los Montes (2) ⚠️ | Garganta de los Montes | 3 |
| Forêt de Corpa (6) ⚠️ | Corpa | 3 |
| Parque de Roma ⚠️ | Madrid › Retiro | 3 |
| Arboreto INIA-CSIC ⚠️ | Madrid › Moncloa-Aravaca | 3 |
| Forêt de Rivas-Vaciamadrid (35) ⚠️ | Rivas-Vaciamadrid | 3 |
| Forêt de Rivas-Vaciamadrid (37) ⚠️ | Rivas-Vaciamadrid | 3 |
| Parc de Getafe (53) ⚠️ | Getafe | 3 |
| Parc de Las Rozas de Madrid (25) ⚠️ | Las Rozas de Madrid | 3 |
| Bois de Redueña (19) ⚠️ | Redueña | 3 |
| Parque Internacional de Esculturas ⚠️ | San Sebastián de los Reyes | 3 |
| Bois de Valdemoro (3) ⚠️ | Valdemoro | 3 |
| Bois de Torrejón de Velasco ⚠️ | Torrejón de Velasco | 3 |
| Parc de Parla (24) ⚠️ | Parla | 3 |
| Parc de San Sebastián de los Reyes (78) ⚠️ | San Sebastián de los Reyes | 3 |
| Bois de San Fernando de Henares (14) ⚠️ | San Fernando de Henares | 3 |
| Parc de Alcobendas (80) ⚠️ | Alcobendas | 3 |
| Parque Jarama ⚠️ | Coslada | 3 |
| Melojar ⚠️ | Miraflores de la Sierra | 3 |
| Bois de Torrelodones (4) ⚠️ | Las Rozas de Madrid | 3 |
| Parque de Nuevos Ministerios ⚠️ | Madrid › Chamberí | 3 |
| Parque El Toril ⚠️ | Galapagar | 3 |
| Bois de Meco (3) ⚠️ | Meco | 3 |
| Parc de Torrejón de la Calzada (7) ⚠️ | Torrejón de la Calzada | 3 |
| Parc de Guadarrama (25) ⚠️ | Guadarrama | 3 |
| Parque Juan de Ávalos ⚠️ | Morata de Tajuña | 3 |
| Forêt de Alpedrete (2) ⚠️ | Alpedrete | 3 |
| Bois de Valdeavero ⚠️ | Valdeavero | 3 |
| Parc de Paracuellos de Jarama (45) ⚠️ | Paracuellos de Jarama | 3 |
| Parc de Colmenar Viejo (45) ⚠️ | Colmenar Viejo | 3 |
| Bois de Los Santos de la Humosa (5) ⚠️ | Los Santos de la Humosa | 3 |
| Forêt de Horcajuelo de la Sierra ⚠️ | Horcajuelo de la Sierra | 3 |
| La Tejera ⚠️ | Hoyo de Manzanares | 3 |
| Forêt de Valdemorillo (14) ⚠️ | Valdemorillo | 3 |
| Forêt de Valdemorillo (20) ⚠️ | Valdemorillo | 3 |
| Forêt de Valdemorillo (32) ⚠️ | Valdemorillo | 3 |
| Forêt de Valdemorillo (46) ⚠️ | Valdemorillo | 3 |
| Forêt de Navalagamella (10) ⚠️ | Navalagamella | 3 |
| Forêt de Robledo de Chavela (55) ⚠️ | Robledo de Chavela | 3 |
| Forêt de Valdemorillo (51) ⚠️ | Valdemorillo | 3 |
| Forêt de Valdemorillo (58) ⚠️ | Valdemorillo | 3 |
| Parc de Pedrezuela (9) ⚠️ | Pedrezuela | 3 |
| Parque El Grillero ⚠️ | Arganda del Rey | 3 |
| Parque Chopera ⚠️ | San Martín de Valdeiglesias | 3 |
| Parc de Madrid (1069) ⚠️ | Madrid › San Blas - Canillejas | 3 |
| Parc de Pozuelo de Alarcón (103) ⚠️ | Pozuelo de Alarcón | 3 |
| Parc de Pozuelo de Alarcón (104) ⚠️ | Pozuelo de Alarcón | 3 |
| Parc de Pozuelo de Alarcón (109) ⚠️ | Pozuelo de Alarcón | 3 |
| Parc de Madrid (1080) ⚠️ | Madrid › Vicálvaro | 3 |
| Parc de Boadilla del Monte (66) ⚠️ | Boadilla del Monte | 3 |
| Parc de Madrid (1122) ⚠️ | Madrid › Moncloa-Aravaca | 3 |
| Forêt de Valdemoro (2) ⚠️ | Valdemoro | 3 |
| Bois de Las Rozas de Madrid (4) ⚠️ | Las Rozas de Madrid | 3 |
| Forêt de Torrejón de Velasco ⚠️ | Torrejón de Velasco | 3 |
| Forêt de Alcalá de Henares (38) ⚠️ | Alcalá de Henares | 3 |
| Forêt de Puebla de la Sierra (9) ⚠️ | Puebla de la Sierra | 3 |
| Parc de Madrid (1222) ⚠️ | Madrid › Villaverde | 3 |
| Forêt de Getafe (5) ⚠️ | Getafe | 3 |
| Borde Forestal de Orcasitas ⚠️ | Madrid › Usera | 3 |
| Parc de Nuevo Baztán (49) ⚠️ | Nuevo Baztán | 3 |
| Forêt de El Escorial (34) ⚠️ | El Escorial | 3 |
| Forêt de Madrid (188) ⚠️ | Madrid › Moncloa-Aravaca | 3 |
| Parc de Madrid (1267) ⚠️ | Madrid › Moratalaz | 3 |
| Forêt de Torrejón de Velasco (3) ⚠️ | Torrejón de Velasco | 3 |
| Bois de Titulcia ⚠️ | Titulcia | 3 |
| Bois de Titulcia (2) ⚠️ | Titulcia | 3 |
| Forêt de Guadarrama (11) ⚠️ | Guadarrama | 3 |
| Cerrp San Galindo ⚠️ | Chinchón | 3 |
| Forêt de Somosierra (25) ⚠️ | Somosierra | 3 |
| Bois de Valdemoro (6) ⚠️ | Valdemoro | 3 |
| Bois de Valdemoro (8) ⚠️ | Valdemoro | 3 |
| Forêt de Aranjuez (140) ⚠️ | Aranjuez | 3 |
| Forêt de Aranjuez (146) ⚠️ | Aranjuez | 3 |
| Forêt de Aranjuez (156) ⚠️ | Aranjuez | 3 |
| Forêt de Aranjuez (158) ⚠️ | Aranjuez | 3 |
| Forêt de Aranjuez (168) ⚠️ | Aranjuez | 3 |
| Recinto Ferial (7) ⚠️ | Alcalá de Henares | 3 |
| Parc de Madrid (1281) ⚠️ | Madrid › Hortaleza | 3 |
| Bois de San Sebastián de los Reyes (13) ⚠️ | San Sebastián de los Reyes | 3 |
| Parc de Madrid (1286) ⚠️ | Madrid › Moratalaz | 3 |
| Bois de San Fernando de Henares (17) ⚠️ | Torrejón de Ardoz | 3 |
| Bois de San Fernando de Henares (18) ⚠️ | San Fernando de Henares | 3 |
| Bois de San Fernando de Henares (19) ⚠️ | San Fernando de Henares | 3 |
| Bois de San Fernando de Henares (21) ⚠️ | San Fernando de Henares | 3 |
| Bois de Galapagar (4) ⚠️ | Las Rozas de Madrid | 3 |
| Forêt de San Sebastián de los Reyes (6) ⚠️ | San Sebastián de los Reyes | 3 |
| Parque Ribera del Manzanares ⚠️ | Madrid › Moncloa-Aravaca | 3 |
| Parc de Las Rozas de Madrid (70) ⚠️ | Las Rozas de Madrid | 3 |
| Parque Benedicto XVI ⚠️ | Madrid › San Blas - Canillejas | 3 |
| Parque/zona verde Valle del Sol ⚠️ | Colmenar del Arroyo | 3 |
| Bois de Madrid (108) ⚠️ | Madrid › Barajas | 3 |
| Parc de Madrid (1392) ⚠️ | Madrid › San Blas - Canillejas | 3 |
| Parque de Miraflores ⚠️ | Aranjuez | 3 |
| Forêt de Madrid (223) ⚠️ | Madrid › Fuencarral-El Pardo | 3 |
| Bois de Guadarrama (4) ⚠️ | Guadarrama | 3 |
| Parc de Algete (29) ⚠️ | Algete | 3 |
| Parque de Don David Pérez y Don Miguel Ángel Hernández ⚠️ | Madrid › Hortaleza | 3 |
| Parque de Atenas ⚠️ | Madrid › Centro | 3 |
| Hospital Universitario José Germain - Complejo de Santa Teresa ⚠️ | Leganés | 3 |
| Parque Garrigues Walker ⚠️ | Madrid › Puente de Vallecas | 3 |
| Parque de la Alcazaba ⚠️ | Madrid › Fuencarral-El Pardo | 2 |
| Canal Bajo de Madrid ⚠️ | Madrid › Fuencarral-El Pardo | 2 |
| Jardín de la Vega (sector oeste) ⚠️ | Alcobendas | 2 |
| Jardín de la Vega (sector centro) ⚠️ | Alcobendas | 2 |
| Jardines de John Lennon ⚠️ | Madrid › Retiro | 2 |
| Forêt de Las Rozas de Madrid ⚠️ | Las Rozas de Madrid | 2 |
| Parque Los Fresnos ⚠️ | Torrejón de Ardoz | 2 |
| Parc de Torrejón de Ardoz ⚠️ | Torrejón de Ardoz | 2 |
| Parque de Peñuelas ⚠️ | Madrid › Arganzuela | 2 |
| Parque del Castillo ⚠️ | Madrid › Barajas | 2 |
| Parque de Villa Rosa Paco Caño ⚠️ | Madrid › Hortaleza | 2 |
| Parque Alfredo Kraus ⚠️ | Madrid › Hortaleza | 2 |
| Parque de Pinar del Rey ⚠️ | Madrid › Hortaleza | 2 |
| Parc de Madrid (64) ⚠️ | Madrid › Barajas | 2 |
| Parque de Pinar del Rey (2) ⚠️ | Madrid › Hortaleza | 2 |
| Parque de Las Tablas ⚠️ | Madrid › Fuencarral-El Pardo | 2 |
| Parc de San Sebastián de los Reyes (3) ⚠️ | San Sebastián de los Reyes | 2 |
| Parc de Madrid (80) ⚠️ | Madrid › Fuencarral-El Pardo | 2 |
| Parque de Ana Tutor ⚠️ | Madrid › Fuencarral-El Pardo | 2 |
| Parque de Fuentelarreina ⚠️ | Madrid › Fuencarral-El Pardo | 2 |
| Parc de Madrid (91) ⚠️ | Madrid › Fuencarral-El Pardo | 2 |
| Parque de la Almudena ⚠️ | Madrid › Ciudad Lineal | 2 |
| Parc de Boadilla del Monte (6) ⚠️ | Boadilla del Monte | 2 |
| Parc de Boadilla del Monte (8) ⚠️ | Boadilla del Monte | 2 |
| Parc de Boadilla del Monte (12) ⚠️ | Boadilla del Monte | 2 |
| Parc de Madrid (115) ⚠️ | Madrid › Fuencarral-El Pardo | 2 |
| Parque La Rinconada ⚠️ | Madrid › Moncloa-Aravaca | 2 |
| Parc de San Sebastián de los Reyes (7) ⚠️ | San Sebastián de los Reyes | 2 |
| Parque de Alcalá Zamora ⚠️ | Madrid › Hortaleza | 2 |
| Parque María Tudor ⚠️ | Madrid › Hortaleza | 2 |
| Parque Azorín (2) ⚠️ | Madrid › Puente de Vallecas | 2 |
| Parque La viña de Entrevías ⚠️ | Madrid › Puente de Vallecas | 2 |
| Parque del Alcalde José Martín-Crespo Díaz (antiguo parque de las Minas) ⚠️ | Pozuelo de Alarcón | 2 |
| Parque Las Comunidades ⚠️ | Alcorcón | 2 |
| Parc de Pozuelo de Alarcón (16) ⚠️ | Pozuelo de Alarcón | 2 |
| Parque de Montarco ⚠️ | Rivas-Vaciamadrid | 2 |
| Parc de Arganda del Rey (5) ⚠️ | Arganda del Rey | 2 |
| Parc de Colmenar Viejo (2) ⚠️ | Colmenar Viejo | 2 |
| Parque El Restón 2 ⚠️ | Valdemoro | 2 |
| Parque de la Paz ⚠️ | Fuenlabrada | 2 |
| El Carraperal ⚠️ | Griñón | 2 |
| Parque De Los Olivos ⚠️ | Valdemoro | 2 |
| Parque de Breogán ⚠️ | Madrid › Salamanca | 2 |
| Parque de Las Moreras ⚠️ | Leganés | 2 |
| Parque de la Solidaridad ⚠️ | Fuenlabrada | 2 |
| Parque de la Solidaridad (2) ⚠️ | Fuenlabrada | 2 |
| Parc de Getafe (4) ⚠️ | Getafe | 2 |
| Parque Av. de los Poblados ⚠️ | Madrid › Carabanchel | 2 |
| Parque del Anillo Verde ⚠️ | Madrid › Carabanchel | 2 |
| Parc de Leganés ⚠️ | Leganés | 2 |
| Parque de Urtinsa ⚠️ | Alcorcón | 2 |
| Parque de las Vistillas ⚠️ | Madrid › Centro | 2 |
| Parc de Madrid (186) ⚠️ | Madrid › Centro | 2 |
| Parc de Manzanares el Real ⚠️ | Manzanares el Real | 2 |
| Bois de Madrid (2) ⚠️ | Madrid › Arganzuela | 2 |
| Forêt de San Fernando de Henares (2) ⚠️ | Mejorada del Campo | 2 |
| Parque Santa Rita ⚠️ | Madrid › Carabanchel | 2 |
| Parque de Comillas ⚠️ | Madrid › Carabanchel | 2 |
| Parque del Sacramental de San Lorenzo y San José ⚠️ | Madrid › Carabanchel | 2 |
| Parc de Getafe (7) ⚠️ | Getafe | 2 |
| Parc de Getafe (8) ⚠️ | Getafe | 2 |
| Parque Martin Luther King (2) ⚠️ | Madrid › Retiro | 2 |
| Parc de Leganés (4) ⚠️ | Leganés | 2 |
| Parque de Palestina ⚠️ | Leganés | 2 |
| Parque Leganés Norte ⚠️ | Leganés | 2 |
| Parc de Madrid (232) ⚠️ | Madrid › Ciudad Lineal | 2 |
| Paque Alcalde Jesús Pérez Quijano ⚠️ | Madrid › Vicálvaro | 2 |
| El Jardín del Sol y del Agua ⚠️ | Madrid › Hortaleza | 2 |
| Parque de Extremadura (2) ⚠️ | Alcobendas | 2 |
| Parque Mirasierra ⚠️ | Madrid › Fuencarral-El Pardo | 2 |
| Parque las Cambrijas ⚠️ | Madrid › Latina | 2 |
| Forêt de Getafe ⚠️ | Getafe | 2 |
| Parc de Getafe (12) ⚠️ | Getafe | 2 |
| Parque del Lago de Loranca ⚠️ | Fuenlabrada | 2 |
| Parc de Fuenlabrada ⚠️ | Fuenlabrada | 2 |
| Forêt de Moraleja de Enmedio ⚠️ | Moraleja de Enmedio | 2 |
| Parc de Móstoles (3) ⚠️ | Móstoles | 2 |
| Parc de Alcorcón (6) ⚠️ | Alcorcón | 2 |
| Parc de Alcorcón (11) ⚠️ | Alcorcón | 2 |
| Parc de Leganés (13) ⚠️ | Leganés | 2 |
| Parque Arroyo del Caño ⚠️ | Moraleja de Enmedio | 2 |
| Parc de Colmenar Viejo (3) ⚠️ | Colmenar Viejo | 2 |
| Forêt de Rivas-Vaciamadrid (2) ⚠️ | Rivas-Vaciamadrid | 2 |
| Bois de Arganda del Rey (2) ⚠️ | Arganda del Rey | 2 |
| Parque Lineal ⚠️ | Rivas-Vaciamadrid | 2 |
| Bois de Alcalá de Henares (2) ⚠️ | Alcalá de Henares | 2 |
| Parque del Camarmilla ⚠️ | Alcalá de Henares | 2 |
| Parque Camarmilla ⚠️ | Alcalá de Henares | 2 |
| Bois de Daganzo de Arriba ⚠️ | Daganzo de Arriba | 2 |
| Bois de Alcalá de Henares (3) ⚠️ | Alcalá de Henares | 2 |
| Bois de San Martín de la Vega ⚠️ | San Martín de la Vega | 2 |
| Bois de Rivas-Vaciamadrid ⚠️ | Rivas-Vaciamadrid | 2 |
| Parc de Madrid (271) ⚠️ | Madrid › Moncloa-Aravaca | 2 |
| Parc de Madrid (284) ⚠️ | Madrid › San Blas - Canillejas | 2 |
| Parc de Madrid (285) ⚠️ | Madrid › Villaverde | 2 |
| Bois de Cobeña ⚠️ | Cobeña | 2 |
| Parque Arroyo de la Veguilla ⚠️ | Madrid › Fuencarral-El Pardo | 2 |
| Parque Gabriela Mistral. (4) ⚠️ | Madrid › Fuencarral-El Pardo | 2 |
| Parque Segura ⚠️ | Madrid › Usera | 2 |
| Bois de Valdeolmos-Alalpardo (5) ⚠️ | Valdeolmos-Alalpardo | 2 |
| Parc de Daganzo de Arriba ⚠️ | Daganzo de Arriba | 2 |
| Bois de San Sebastián de los Reyes (3) ⚠️ | San Sebastián de los Reyes | 2 |
| Pinar de San Isidro ⚠️ | Alcobendas | 2 |
| Parque de La Torre ⚠️ | Madrid › Hortaleza | 2 |
| Forêt de Pozuelo de Alarcón (7) ⚠️ | Pozuelo de Alarcón | 2 |
| El Pinar (2) ⚠️ | Cubas de la Sagra | 2 |
| Bois de Villanueva del Pardillo (3) ⚠️ | Villanueva del Pardillo | 2 |
| Forêt de Getafe (2) ⚠️ | Getafe | 2 |
| Forêt de Rivas-Vaciamadrid (6) ⚠️ | Rivas-Vaciamadrid | 2 |
| Forêt de Las Rozas de Madrid (3) ⚠️ | Las Rozas de Madrid | 2 |
| Bois de Chinchón (4) ⚠️ | Chinchón | 2 |
| Bois de Hoyo de Manzanares (2) ⚠️ | Hoyo de Manzanares | 2 |
| Calvero de la Higuera ⚠️ | Pinilla del Valle | 2 |
| Parc de Parla (3) ⚠️ | Parla | 2 |
| Bois de Madrid (13) ⚠️ | Madrid › Fuencarral-El Pardo | 2 |
| Bois de Madrid (17) ⚠️ | Madrid › Fuencarral-El Pardo | 2 |
| Parque del Agua ⚠️ | Torrejón de Ardoz | 2 |
| Forêt de Pozuelo de Alarcón (8) ⚠️ | Pozuelo de Alarcón | 2 |
| Forêt de Pozuelo de Alarcón (9) ⚠️ | Pozuelo de Alarcón | 2 |
| Forêt de San Martín de Valdeiglesias (3) ⚠️ | San Martín de Valdeiglesias | 2 |
| Forêt de Rozas de Puerto Real (2) ⚠️ | Rozas de Puerto Real | 2 |
| Forêt de Montejo de la Sierra ⚠️ | Montejo de la Sierra | 2 |
| Forêt de Patones ⚠️ | Patones | 2 |
| Parque Patos ⚠️ | Tres Cantos | 2 |
| Forêt de La Cabrera (2) ⚠️ | La Cabrera | 2 |
| Forêt de La Cabrera (4) ⚠️ | La Cabrera | 2 |
| Forêt de La Cabrera (8) ⚠️ | La Cabrera | 2 |
| Forêt de La Cabrera (9) ⚠️ | La Cabrera | 2 |
| Parque Darwin (2) ⚠️ | Alcorcón | 2 |
| Parc de Madrid (371) ⚠️ | Madrid › Moratalaz | 2 |
| Parc de Madrid (379) ⚠️ | Madrid › Villa de Vallecas | 2 |
| Parque Infantil Las Suertes ⚠️ | Madrid › Villa de Vallecas | 2 |
| Parc de Madrid (387) ⚠️ | Madrid › Villa de Vallecas | 2 |
| Parc de Madrid (388) ⚠️ | Madrid › Villa de Vallecas | 2 |
| Parc de Madrid (399) ⚠️ | Madrid › Villa de Vallecas | 2 |
| Parque Prado Grande ⚠️ | Torrelodones | 2 |
| Parc de Madrid (412) ⚠️ | Madrid › Villa de Vallecas | 2 |
| Forêt de Brunete ⚠️ | Brunete | 2 |
| Jardín de Dionisio Ridruejo ⚠️ | Madrid › Moratalaz | 2 |
| Parc de Madrid (444) ⚠️ | Madrid › San Blas - Canillejas | 2 |
| Bois de Torrelodones ⚠️ | Torrelodones | 2 |
| Parc de Alcalá de Henares (14) ⚠️ | Alcalá de Henares | 2 |
| Parc de Las Rozas de Madrid ⚠️ | Las Rozas de Madrid | 2 |
| Parc de Madrid (497) ⚠️ | Madrid › Moncloa-Aravaca | 2 |
| Parque Manzana XIX ⚠️ | Alcobendas | 2 |
| Paseo del Oceano Pacífico ⚠️ | Coslada | 2 |
| Forêt de Villanueva de Perales (4) ⚠️ | Villanueva de Perales | 2 |
| Forêt de Colmenar del Arroyo ⚠️ | Colmenar del Arroyo | 2 |
| Bois de Villamantilla (3) ⚠️ | Villamantilla | 2 |
| Bois de Villamantilla (5) ⚠️ | Villamantilla | 2 |
| Forêt de Robledo de Chavela ⚠️ | Robledo de Chavela | 2 |
| Forêt de Robledo de Chavela (4) ⚠️ | Robledo de Chavela | 2 |
| Forêt de Robledo de Chavela (12) ⚠️ | Robledo de Chavela | 2 |
| Forêt de Robledo de Chavela (13) ⚠️ | Robledo de Chavela | 2 |
| Forêt de Robledo de Chavela (21) ⚠️ | Robledo de Chavela | 2 |
| Forêt de Robledo de Chavela (30) ⚠️ | Robledo de Chavela | 2 |
| Forêt de Robledo de Chavela (33) ⚠️ | Robledo de Chavela | 2 |
| Bois de Zarzalejo ⚠️ | Zarzalejo | 2 |
| Forêt de Valdemaqueda (6) ⚠️ | Valdemaqueda | 2 |
| Parque de la calle Marbella ⚠️ | Arroyomolinos | 2 |
| Parque de Moratalaz ⚠️ | Madrid › Moratalaz | 2 |
| Forêt de Santa María de la Alameda (8) ⚠️ | Santa María de la Alameda | 2 |
| Bois de Santa María de la Alameda (4) ⚠️ | Santa María de la Alameda | 2 |
| Bois de Santa María de la Alameda (7) ⚠️ | Santa María de la Alameda | 2 |
| Bois de Santa María de la Alameda (11) ⚠️ | Santa María de la Alameda | 2 |
| Parque del Lago H2Ocio ⚠️ | Rivas-Vaciamadrid | 2 |
| Forêt de Santa María de la Alameda (12) ⚠️ | Santa María de la Alameda | 2 |
| Forêt de Santa María de la Alameda (17) ⚠️ | Santa María de la Alameda | 2 |
| Forêt de Santa María de la Alameda (22) ⚠️ | Santa María de la Alameda | 2 |
| Forêt de Santa María de la Alameda (25) ⚠️ | Santa María de la Alameda | 2 |
| Forêt de Santa María de la Alameda (29) ⚠️ | Santa María de la Alameda | 2 |
| Forêt de Santa María de la Alameda (30) ⚠️ | Santa María de la Alameda | 2 |
| Forêt de San Martín de Valdeiglesias (15) ⚠️ | San Martín de Valdeiglesias | 2 |
| Forêt de Robledo de Chavela (46) ⚠️ | Robledo de Chavela | 2 |
| Forêt de Valdemaqueda (15) ⚠️ | Valdemaqueda | 2 |
| Parque de Los Vallejos ⚠️ | Torres de la Alameda | 2 |
| Prado Puente ⚠️ | Manzanares el Real | 2 |
| Bois de Navacerrada (2) ⚠️ | Navacerrada | 2 |
| Bois de Navacerrada (5) ⚠️ | Navacerrada | 2 |
| Bois de Cobeña (2) ⚠️ | Cobeña | 2 |
| Parc de Cadalso de los Vidrios (4) ⚠️ | Cadalso de los Vidrios | 2 |
| Parque de los Derechos Humanos (3) ⚠️ | Fuenlabrada | 2 |
| Parc de Torrejón de Ardoz (7) ⚠️ | Torrejón de Ardoz | 2 |
| Forêt de Brea de Tajo ⚠️ | Brea de Tajo | 2 |
| Forêt de Brea de Tajo (4) ⚠️ | Brea de Tajo | 2 |
| Jardines de Eva Duarte de Perón ⚠️ | Madrid › Salamanca | 2 |
| Jardines de Sancho Dávila ⚠️ | Madrid › Salamanca | 2 |
| Forêt de Madrid (51) ⚠️ | Madrid › Moncloa-Aravaca | 2 |
| Parc de Alcalá de Henares (17) ⚠️ | Alcalá de Henares | 2 |
| La Chopera ⚠️ | Alcalá de Henares | 2 |
| Forêt de Corpa ⚠️ | Corpa | 2 |
| Forêt de Robregordo ⚠️ | Robregordo | 2 |
| Parc de Móstoles (31) ⚠️ | Móstoles | 2 |
| Forêt de Somosierra (12) ⚠️ | Somosierra | 2 |
| Bois de Colmenarejo ⚠️ | Colmenarejo | 2 |
| Bois de Robledo de Chavela (15) ⚠️ | Robledo de Chavela | 2 |
| Bois de Quijorna ⚠️ | Quijorna | 2 |
| Forêt de Zarzalejo (5) ⚠️ | Zarzalejo | 2 |
| Bois de El Escorial (2) ⚠️ | El Escorial | 2 |
| Parc de San Sebastián de los Reyes (10) ⚠️ | San Sebastián de los Reyes | 2 |
| Forêt de El Escorial (11) ⚠️ | El Escorial | 2 |
| Forêt de Zarzalejo (13) ⚠️ | Zarzalejo | 2 |
| Parc de Alcobendas (19) ⚠️ | Alcobendas | 2 |
| Forêt de Zarzalejo (116) ⚠️ | Zarzalejo | 2 |
| Forêt de Zarzalejo (131) ⚠️ | Zarzalejo | 2 |
| Forêt de Robledo de Chavela (52) ⚠️ | Robledo de Chavela | 2 |
| Forêt de Zarzalejo (155) ⚠️ | Zarzalejo | 2 |
| Forêt de El Escorial (16) ⚠️ | El Escorial | 2 |
| Forêt de El Escorial (17) ⚠️ | El Escorial | 2 |
| Forêt de El Escorial (23) ⚠️ | El Escorial | 2 |
| Forêt de Villanueva del Pardillo (2) ⚠️ | Villanueva del Pardillo | 2 |
| Bois de Mejorada del Campo (5) ⚠️ | Mejorada del Campo | 2 |
| Parc de Fuenlabrada (77) ⚠️ | Fuenlabrada | 2 |
| Bois de Redueña ⚠️ | Redueña | 2 |
| Bois de Redueña (8) ⚠️ | Redueña | 2 |
| Bois de Redueña (9) ⚠️ | Redueña | 2 |
| Bois de Madrid (24) ⚠️ | Madrid › Latina | 2 |
| Bois de Redueña (13) ⚠️ | Redueña | 2 |
| Bois de Villaconejos (3) ⚠️ | Villaconejos | 2 |
| Parc de Madrid (568) ⚠️ | Madrid › Carabanchel | 2 |
| Parque Manolito Gafotas ⚠️ | Madrid › Carabanchel | 2 |
| Forêt de Galapagar (6) ⚠️ | Galapagar | 2 |
| Parque de Gregorio Peces-Barba ⚠️ | Madrid › Hortaleza | 2 |
| Parc de Móstoles (44) ⚠️ | Móstoles | 2 |
| Parc de Móstoles (45) ⚠️ | Móstoles | 2 |
| Bois de Pozuelo de Alarcón (7) ⚠️ | Pozuelo de Alarcón | 2 |
| Zona Verde Pública ⚠️ | Pozuelo de Alarcón | 2 |
| Parc de Móstoles (71) ⚠️ | Móstoles | 2 |
| Forêt de Rivas-Vaciamadrid (24) ⚠️ | Rivas-Vaciamadrid | 2 |
| Forêt de Rivas-Vaciamadrid (25) ⚠️ | Rivas-Vaciamadrid | 2 |
| Forêt de Rivas-Vaciamadrid (26) ⚠️ | Rivas-Vaciamadrid | 2 |
| Bois de Rivas-Vaciamadrid (11) ⚠️ | Rivas-Vaciamadrid | 2 |
| Parc de Móstoles (98) ⚠️ | Móstoles | 2 |
| Parque de Valdeserrano ⚠️ | Fuenlabrada | 2 |
| Forêt de Santa María de la Alameda (36) ⚠️ | Santa María de la Alameda | 2 |
| Bois de Casarrubuelos (2) ⚠️ | Casarrubuelos | 2 |
| Bois de Batres (4) ⚠️ | Batres | 2 |
| Parc de Madrid (614) ⚠️ | Madrid › Fuencarral-El Pardo | 2 |
| Los Árboles ⚠️ | Galapagar | 2 |
| Forêt de Montejo de la Sierra (6) ⚠️ | Montejo de la Sierra | 2 |
| Parc de Boadilla del Monte (25) ⚠️ | Boadilla del Monte | 2 |
| Forêt de Boadilla del Monte (3) ⚠️ | Boadilla del Monte | 2 |
| Parc de Madrid (666) ⚠️ | Madrid › Villaverde | 2 |
| Parc de Madrid (691) ⚠️ | Madrid › Villaverde | 2 |
| Santuario de Schoenstatt ⚠️ | Pozuelo de Alarcón | 2 |
| Forêt de Nuevo Baztán (5) ⚠️ | Nuevo Baztán | 2 |
| Parc de Madrid (722) ⚠️ | Madrid › Hortaleza | 2 |
| Forêt de Corpa (4) ⚠️ | Corpa | 2 |
| Parc de Pozuelo de Alarcón (34) ⚠️ | Pozuelo de Alarcón | 2 |
| Bois de Rivas-Vaciamadrid (14) ⚠️ | Rivas-Vaciamadrid | 2 |
| Forêt de Pozuelo del Rey (5) ⚠️ | Pozuelo del Rey | 2 |
| Parc de Madrid (740) ⚠️ | Madrid › Vicálvaro | 2 |
| Parque Forestal Cerro del Castillo ⚠️ | Valdemoro | 2 |
| Parc de Leganés (23) ⚠️ | Leganés | 2 |
| Parc de Leganés (50) ⚠️ | Leganés | 2 |
| Forêt de Rivas-Vaciamadrid (39) ⚠️ | Rivas-Vaciamadrid | 2 |
| Forêt de San Martín de la Vega (17) ⚠️ | San Martín de la Vega | 2 |
| Forêt de Valdaracete ⚠️ | Valdaracete | 2 |
| Forêt de Daganzo de Arriba ⚠️ | Daganzo de Arriba | 2 |
| Forêt de Sevilla la Nueva (12) ⚠️ | Sevilla la Nueva | 2 |
| Forêt de Getafe (3) ⚠️ | Getafe | 2 |
| Parc de Alcobendas (81) ⚠️ | Alcobendas | 2 |
| Bois de San Fernando de Henares (15) ⚠️ | San Fernando de Henares | 2 |
| Bois de Torrelaguna (4) ⚠️ | Torrelaguna | 2 |
| Bois de Torrelaguna (6) ⚠️ | Torrelaguna | 2 |
| Bois de Torrelaguna (12) ⚠️ | Torrelaguna | 2 |
| Forêt de Alcalá de Henares (14) ⚠️ | Alcalá de Henares | 2 |
| Parque Municipal La Dehesa ⚠️ | Meco | 2 |
| Parque del Pinar (2) ⚠️ | Meco | 2 |
| Parque lineal Claudio Coello ⚠️ | Colmenar Viejo | 2 |
| Forêt de Hoyo de Manzanares (2) ⚠️ | Hoyo de Manzanares | 2 |
| Parc de Torrejón de la Calzada (6) ⚠️ | Torrejón de la Calzada | 2 |
| Bois de Manzanares el Real (7) ⚠️ | Manzanares el Real | 2 |
| Bois de Manzanares el Real (13) ⚠️ | Manzanares el Real | 2 |
| Bois de Manzanares el Real (14) ⚠️ | Manzanares el Real | 2 |
| Parc de Coslada (13) ⚠️ | Coslada | 2 |
| Parc de Madrid (927) ⚠️ | Madrid › Hortaleza | 2 |
| Parque de la Vaguada ⚠️ | Madrid › Fuencarral-El Pardo | 2 |
| Parc de Villaviciosa de Odón (6) ⚠️ | Villaviciosa de Odón | 2 |
| Recinto Ferial (6) ⚠️ | Paracuellos de Jarama | 2 |
| Parque Esgaravita ⚠️ | Alcalá de Henares | 2 |
| Parc de Paracuellos de Jarama (35) ⚠️ | Paracuellos de Jarama | 2 |
| Parque del Ancla ⚠️ | Colmenar Viejo | 2 |
| Bois de Torrelodones (5) ⚠️ | Torrelodones | 2 |
| Bois de Los Santos de la Humosa (2) ⚠️ | Los Santos de la Humosa | 2 |
| Bois de Los Santos de la Humosa (9) ⚠️ | Los Santos de la Humosa | 2 |
| Parc de Majadahonda (10) ⚠️ | Majadahonda | 2 |
| Parc de Leganés (64) ⚠️ | Leganés | 2 |
| Bois de Pozuelo de Alarcón (12) ⚠️ | Pozuelo de Alarcón | 2 |
| Parque de La Ribota (2) ⚠️ | Alcorcón | 2 |
| Parc de Madrid (1051) ⚠️ | Madrid › Usera | 2 |
| Forêt de Pozuelo de Alarcón (11) ⚠️ | Pozuelo de Alarcón | 2 |
| Parque Forestal Maria Marzol ⚠️ | Daganzo de Arriba | 2 |
| Parque Soto de Entrevías ⚠️ | Madrid › Puente de Vallecas | 2 |
| Forêt de Valdemorillo (11) ⚠️ | Valdemorillo | 2 |
| Forêt de Valdemorillo (19) ⚠️ | Valdemorillo | 2 |
| Forêt de Valdemorillo (29) ⚠️ | Valdemorillo | 2 |
| Forêt de Valdemorillo (34) ⚠️ | Valdemorillo | 2 |
| Forêt de Valdemorillo (38) ⚠️ | Valdemorillo | 2 |
| Forêt de Navalagamella (11) ⚠️ | Valdemorillo | 2 |
| Forêt de Valdemorillo (54) ⚠️ | Valdemorillo | 2 |
| Parc de El Molar (8) ⚠️ | El Molar | 2 |
| Forêt de Valdemorillo (63) ⚠️ | Valdemorillo | 2 |
| Parque Camarmilla (2) ⚠️ | Alcalá de Henares | 2 |
| Forêt de Valdemorillo (67) ⚠️ | Valdemorillo | 2 |
| Parc de Pozuelo de Alarcón (101) ⚠️ | Pozuelo de Alarcón | 2 |
| Parc de Getafe (94) ⚠️ | Getafe | 2 |
| Forêt de Navalagamella (19) ⚠️ | Navalagamella | 2 |
| Zona Verde Pública (3) ⚠️ | Pozuelo de Alarcón | 2 |
| Paseo av de los encuartes ⚠️ | Tres Cantos | 2 |
| Bois de Manzanares el Real (17) ⚠️ | Manzanares el Real | 2 |
| El pinar de Hoyo ⚠️ | Hoyo de Manzanares | 2 |
| Bois de Buitrago del Lozoya ⚠️ | Buitrago del Lozoya | 2 |
| Parque Sur (2) ⚠️ | Villalbilla | 2 |
| Parque de La Cristina ⚠️ | Pinto | 2 |
| Parc de Madrid (1119) ⚠️ | Madrid › San Blas - Canillejas | 2 |
| Parque Magallanes ⚠️ | Alcalá de Henares | 2 |
| Parc de Villar del Olmo ⚠️ | Villar del Olmo | 2 |
| Parc de Las Rozas de Madrid (43) ⚠️ | Las Rozas de Madrid | 2 |
| Bois de Collado Villalba (2) ⚠️ | Galapagar | 2 |
| Forêt de Pozuelo de Alarcón (16) ⚠️ | Pozuelo de Alarcón | 2 |
| Parque Arroyo de los Pinos ⚠️ | Madrid › Fuencarral-El Pardo | 2 |
| Parc de Madrid (1174) ⚠️ | Madrid › San Blas - Canillejas | 2 |
| Forêt de Villalbilla (9) ⚠️ | Villalbilla | 2 |
| Forêt de Ambite (6) ⚠️ | Ambite | 2 |
| Forêt de Madrid (118) ⚠️ | Madrid › Moncloa-Aravaca | 2 |
| Forêt de Madrid (119) ⚠️ | Madrid › Moncloa-Aravaca | 2 |
| Forêt de Madrid (120) ⚠️ | Madrid › Moncloa-Aravaca | 2 |
| Forêt de Talamanca de Jarama (3) ⚠️ | Talamanca de Jarama | 2 |
| Parc de Valdemoro (36) ⚠️ | Valdemoro | 2 |
| Parc de Valdemoro (37) ⚠️ | Valdemoro | 2 |
| Parc de Madrid (1196) ⚠️ | Madrid › Vicálvaro | 2 |
| Bois de Madrid (73) ⚠️ | Madrid › Hortaleza | 2 |
| Parc de Nuevo Baztán (46) ⚠️ | Nuevo Baztán | 2 |
| Forêt de Guadarrama (8) ⚠️ | Guadarrama | 2 |
| Forêt de Guadarrama (10) ⚠️ | Guadarrama | 2 |
| Parc de Getafe (119) ⚠️ | Getafe | 2 |
| Bois de Moralzarzal (5) ⚠️ | Moralzarzal | 2 |
| Forêt de Getafe (8) ⚠️ | Getafe | 2 |
| Parc de Getafe (139) ⚠️ | Getafe | 2 |
| Forêt de Fuenlabrada (2) ⚠️ | Fuenlabrada | 2 |
| Parc de San Lorenzo de El Escorial (15) ⚠️ | San Lorenzo de El Escorial | 2 |
| Parque de Antonio Herrero ⚠️ | Boadilla del Monte | 2 |
| Parc de Villar del Olmo (4) ⚠️ | Villar del Olmo | 2 |
| Bois de Alpedrete (3) ⚠️ | Alpedrete | 2 |
| Parc de Alpedrete (12) ⚠️ | Alpedrete | 2 |
| Jardines del Guardia Civil Miguel Miranda Puertas ⚠️ | Madrid › Moratalaz | 2 |
| Forêt de El Escorial (32) ⚠️ | El Escorial | 2 |
| Forêt de El Escorial (33) ⚠️ | El Escorial | 2 |
| Parc de Madrid (1259) ⚠️ | Madrid › Villaverde | 2 |
| Forêt de Madrid (173) ⚠️ | Madrid › Moncloa-Aravaca | 2 |
| Forêt de Madrid (175) ⚠️ | Madrid › Moncloa-Aravaca | 2 |
| Bois de Villaconejos (12) ⚠️ | Villaconejos | 2 |
| Bois de Villaconejos (13) ⚠️ | Villaconejos | 2 |
| Forêt de Somosierra (27) ⚠️ | Somosierra | 2 |
| Bois de Villaconejos (15) ⚠️ | Villaconejos | 2 |
| Bois de Villaconejos (16) ⚠️ | Villaconejos | 2 |
| Forêt de Aranjuez (150) ⚠️ | Aranjuez | 2 |
| Forêt de Aranjuez (152) ⚠️ | Aranjuez | 2 |
| Forêt de Aranjuez (162) ⚠️ | Aranjuez | 2 |
| Forêt de Aranjuez (165) ⚠️ | Aranjuez | 2 |
| Forêt de Aranjuez (167) ⚠️ | Aranjuez | 2 |
| Forêt de Aranjuez (169) ⚠️ | Aranjuez | 2 |
| Forêt de Madrid (196) ⚠️ | Alcorcón | 2 |
| Forêt de Alcalá de Henares (46) ⚠️ | Alcalá de Henares | 2 |
| Forêt de Alcalá de Henares (48) ⚠️ | Alcalá de Henares | 2 |
| Bois de Las Rozas de Madrid (6) ⚠️ | Las Rozas de Madrid | 2 |
| Bois de San Sebastián de los Reyes (10) ⚠️ | Alcobendas | 2 |
| Bois de Alcobendas (3) ⚠️ | Alcobendas | 2 |
| Bois de San Sebastián de los Reyes (11) ⚠️ | Alcobendas | 2 |
| Bois de San Sebastián de los Reyes (14) ⚠️ | San Sebastián de los Reyes | 2 |
| Forêt de Guadarrama (13) ⚠️ | Guadarrama | 2 |
| Parc de Madrid (1290) ⚠️ | Madrid › Moratalaz | 2 |
| Parque Alto Lazarejo ⚠️ | Las Rozas de Madrid | 2 |
| Parc de Boadilla del Monte (84) ⚠️ | Boadilla del Monte | 2 |
| Forêt de San Sebastián de los Reyes (7) ⚠️ | San Sebastián de los Reyes | 2 |
| Bois de Las Rozas de Madrid (10) ⚠️ | Las Rozas de Madrid | 2 |
| Bois de Moralzarzal (7) ⚠️ | Moralzarzal | 2 |
| Zona reservada Monte de El Pardo ⚠️ | Madrid › Moncloa-Aravaca | 2 |
| Parque natural de Las Viñuelas ⚠️ | Colmenar del Arroyo | 2 |
| Parc de Madrid (1368) ⚠️ | Madrid › Carabanchel | 2 |
| Forêt de Buitrago del Lozoya (3) ⚠️ | Buitrago del Lozoya | 2 |
| La Dehesa ⚠️ | Madrid › Vicálvaro | 2 |
| Forêt de Becerril de la Sierra (3) ⚠️ | Becerril de la Sierra | 2 |
| Forêt de Becerril de la Sierra (4) ⚠️ | Moralzarzal | 2 |
| Bois de Aranjuez (30) ⚠️ | Aranjuez | 2 |
| Bois de San Sebastián de los Reyes (16) ⚠️ | San Sebastián de los Reyes | 2 |
| Forêt de Daganzo de Arriba (2) ⚠️ | Daganzo de Arriba | 2 |
| Forêt de Madrid (216) ⚠️ | Madrid › Fuencarral-El Pardo | 2 |
| Forêt de Lozoya (4) ⚠️ | Lozoya | 2 |
| Bois de Villamantilla (13) ⚠️ | Villamantilla | 2 |
| Bois de Villamantilla (18) ⚠️ | Villamantilla | 2 |
| Bois de Chapinería (3) ⚠️ | Chapinería | 2 |
| Bois de Villanueva de Perales (6) ⚠️ | Villanueva de Perales | 2 |
| Bois de Colmenar del Arroyo (3) ⚠️ | Colmenar del Arroyo | 2 |
| Bois de Navas del Rey (3) ⚠️ | Navas del Rey | 2 |
| Forêt de Aldea del Fresno (3) ⚠️ | Aldea del Fresno | 2 |
| Forêt de Aldea del Fresno (5) ⚠️ | Aldea del Fresno | 2 |
| Forêt de Buitrago del Lozoya (6) ⚠️ | Buitrago del Lozoya | 2 |
| Forêt de Buitrago del Lozoya (7) ⚠️ | Buitrago del Lozoya | 2 |
| Forêt de Las Rozas de Madrid (12) ⚠️ | Las Rozas de Madrid | 2 |
| Bois de Rivas-Vaciamadrid (21) ⚠️ | Rivas-Vaciamadrid | 2 |
| Parc de Villanueva de la Cañada (36) ⚠️ | Villanueva de la Cañada | 2 |
| Parc de Madrid (1523) ⚠️ | Madrid › Vicálvaro | 2 |
| Forêt de Santorcaz (22) ⚠️ | Santorcaz | 2 |
| Forêt de Valdemaqueda (28) ⚠️ | Valdemaqueda | 2 |
| Parc de Fuenlabrada (114) ⚠️ | Fuenlabrada | 2 |
| Parc de Móstoles (139) ⚠️ | Móstoles | 2 |
| Parque Andalucía (3) ⚠️ | Móstoles | 2 |
| Parque de Castilla-La Mancha ⚠️ | Getafe | 2 |
| Parque Andres Garcia Madrid ⚠️ | Getafe | 2 |
| Recinto ferial ⚠️ | San Fernando de Henares | 2 |
| Bois de Valverde de Alcalá (21) ⚠️ | Valverde de Alcalá | 2 |
| Forêt de Villalbilla (10) ⚠️ | Villalbilla | 2 |
| El Quijote ⚠️ | Alcalá de Henares | 2 |
| Paseo de La Rambla ⚠️ | Coslada | 2 |
| Parque de la Vicalvarada ⚠️ | Madrid › Vicálvaro | 2 |
| Parque Alcalde Agustín San José ⚠️ | Madrid › Vicálvaro | 2 |
| Parque Juan Pablo II (3) ⚠️ | Madrid › Hortaleza | 2 |
| Bois de Torrelaguna (21) ⚠️ | Torrelaguna | 2 |
| Bois de Collado Villalba (3) ⚠️ | Collado Villalba | 2 |
| Forêt de Paracuellos de Jarama (8) ⚠️ | Paracuellos de Jarama | 2 |
| Forêt de Guadarrama (23) ⚠️ | Guadarrama | 2 |
| Parque de los Pinos (3) ⚠️ | Madrid › Tetuán | 2 |
| Parc de Madrid (2) ⚠️ | Madrid › San Blas - Canillejas | 1 |
| Parc de Madrid (4) ⚠️ | Madrid › San Blas - Canillejas | 1 |
| Parc de Madrid (6) ⚠️ | Madrid › San Blas - Canillejas | 1 |
| Jardines del Descubrimiento ⚠️ | Madrid › Salamanca | 1 |
| Plaza de España ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parc de Madrid (10) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parque de la Alcazaba (2) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Jardín del Rastro ⚠️ | Madrid › Arganzuela | 1 |
| Parque Oligisto ⚠️ | Madrid › Usera | 1 |
| Canal Bajo de Madrid (2) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parc de Madrid (20) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parc de Madrid (25) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Jardín de la Vega (sector este) ⚠️ | Alcobendas | 1 |
| Parc de Alcobendas ⚠️ | Alcobendas | 1 |
| Parque de San Fernando ⚠️ | Madrid › Chamartín | 1 |
| Plaza de Pablo Ruiz Picasso ⚠️ | Madrid › Tetuán | 1 |
| Parc de Madrid (32) ⚠️ | Madrid › Ciudad Lineal | 1 |
| Parque Arriaga ⚠️ | Madrid › Ciudad Lineal | 1 |
| Olivar de Castillejo ⚠️ | Madrid › Chamartín | 1 |
| Parque Calero ⚠️ | Madrid › Ciudad Lineal | 1 |
| Parc de Madrid (38) ⚠️ | Madrid › Chamartín | 1 |
| Parque Almansa ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Jardines Doce de Octubre ⚠️ | Madrid › Retiro | 1 |
| Parque de las Ciencias ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parc de Madrid (40) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Jardín Pinar del Arroyo de Cantarranas ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Plaza de Menéndez Pelayo ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parc de Madrid (41) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parque de la Ciudad de los Ángeles ⚠️ | Madrid › Villaverde | 1 |
| Parc de Madrid (49) ⚠️ | Madrid › Arganzuela | 1 |
| Parc de Madrid (56) ⚠️ | Madrid › Barajas | 1 |
| Parc de Madrid (59) ⚠️ | Madrid › Barajas | 1 |
| Parc de Madrid (60) ⚠️ | Madrid › Barajas | 1 |
| Parque Hortaleza ⚠️ | Madrid › Hortaleza | 1 |
| Parque de la Huerta de la Salud ⚠️ | Madrid › Hortaleza | 1 |
| Parc de Madrid (62) ⚠️ | Madrid › Hortaleza | 1 |
| Parque Isabel Clara Eugenia ⚠️ | Madrid › Hortaleza | 1 |
| Parc de Madrid (66) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parc de Madrid (69) ⚠️ | Madrid › Hortaleza | 1 |
| Parque de Doña Guiomar ⚠️ | Madrid › Hortaleza | 1 |
| Parc de Madrid (76) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parque de Galicia (sector norte) ⚠️ | Alcobendas | 1 |
| Parque de Galicia (sector centro) ⚠️ | Alcobendas | 1 |
| Parque Cataluña ⚠️ | Alcobendas | 1 |
| Parque de Castilla La Mancha ⚠️ | Alcobendas | 1 |
| Parque de Valencia ⚠️ | Alcobendas | 1 |
| Parc de Madrid (81) ⚠️ | Madrid › Hortaleza | 1 |
| Parc de Madrid (82) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parc de Madrid (84) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parque de Peñagrande ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parque del Arte ⚠️ | Torrejón de Ardoz | 1 |
| Parque Príncipe Felipe ⚠️ | San Agustín del Guadalix | 1 |
| Parc de Madrid (93) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parc de Madrid (95) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parc de Madrid (97) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parc de Madrid (98) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Forêt de Madrid ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parc de Boadilla del Monte (5) ⚠️ | Boadilla del Monte | 1 |
| Parc de Madrid (101) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parc de Madrid (102) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parc de Madrid (104) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parc de Madrid (106) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parc de Boadilla del Monte (9) ⚠️ | Boadilla del Monte | 1 |
| Parc de Boadilla del Monte (13) ⚠️ | Boadilla del Monte | 1 |
| Parc de Madrid (113) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parque de Valdemarín ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parque Severo Ochoa ⚠️ | Boadilla del Monte | 1 |
| Parque Azorín ⚠️ | Boadilla del Monte | 1 |
| Parque Condado de Treviño ⚠️ | Madrid › Ciudad Lineal | 1 |
| Parc de Madrid (120) ⚠️ | Madrid › Hortaleza | 1 |
| Parc de Alcobendas (5) ⚠️ | Alcobendas | 1 |
| Parc de Madrid (126) ⚠️ | Madrid › Hortaleza | 1 |
| Parc de Madrid (129) ⚠️ | Madrid › Ciudad Lineal | 1 |
| Parque de Manoteras ⚠️ | Madrid › Hortaleza | 1 |
| Parque Doctor Fernández Catalina ⚠️ | Madrid › Ciudad Lineal | 1 |
| Recinto de la Malvaloca ⚠️ | Collado Villalba | 1 |
| Parque Nuestra Señora de Montserrat ⚠️ | Pozuelo de Alarcón | 1 |
| Parque de Félix Rodríguez de la Fuente ⚠️ | Madrid › Chamartín | 1 |
| Parque San Xinaro ⚠️ | Madrid › Hortaleza | 1 |
| Parc de Madrid (135) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parc de Pozuelo de Alarcón (7) ⚠️ | Pozuelo de Alarcón | 1 |
| Parque del Campo de Chito ⚠️ | Collado Villalba | 1 |
| Parque de Peñalba ⚠️ | Collado Villalba | 1 |
| Parque Mirador de Miguel Sarabia ⚠️ | Madrid › Usera | 1 |
| Parque de Pavones Norte ⚠️ | Madrid › Moratalaz | 1 |
| Parque Vandel (2) ⚠️ | Madrid › Moratalaz | 1 |
| Parc de Madrid (145) ⚠️ | Madrid › Usera | 1 |
| Parc de Madrid (146) ⚠️ | Madrid › Latina | 1 |
| Parc de Madrid (147) ⚠️ | Madrid › Latina | 1 |
| Parc de Madrid (148) ⚠️ | Madrid › Villaverde | 1 |
| Parque Brigadas Internacionales ⚠️ | Móstoles | 1 |
| Parque Prados de Torrejón ⚠️ | Pozuelo de Alarcón | 1 |
| Parc de Pozuelo de Alarcón (11) ⚠️ | Pozuelo de Alarcón | 1 |
| Parque Dolores Ibárruri ⚠️ | San Fernando de Henares | 1 |
| Parque Duque de Ahumada ⚠️ | Valdemoro | 1 |
| Parque de las Eras ⚠️ | Valdemoro | 1 |
| Parque España ⚠️ | Valdemoro | 1 |
| Parque de Leganés ⚠️ | Fuenlabrada | 1 |
| Parque de La Ribota ⚠️ | Alcorcón | 1 |
| Parque "Las Piedras" ⚠️ | Paracuellos de Jarama | 1 |
| Parque Egido de la Fuente ⚠️ | Pinto | 1 |
| Parque Norte ⚠️ | Pinto | 1 |
| Parque Saturnino Fernández Vallejo ⚠️ | Galapagar | 1 |
| Parque Gabriela Mistral. ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parque Gabriela Mistral. (2) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Forêt de Pozuelo de Alarcón ⚠️ | Pozuelo de Alarcón | 1 |
| Forêt de Miraflores de la Sierra (4) ⚠️ | Miraflores de la Sierra | 1 |
| Parque Catalina Muñoz ⚠️ | Velilla de San Antonio | 1 |
| Parc de Arganda del Rey ⚠️ | Arganda del Rey | 1 |
| Parc de Arganda del Rey (2) ⚠️ | Arganda del Rey | 1 |
| Parc de Villalbilla ⚠️ | Villalbilla | 1 |
| Parque del Mirador ⚠️ | Colmenar Viejo | 1 |
| Plaza de Nueva Orleans ⚠️ | Madrid › Ciudad Lineal | 1 |
| Parque del Pozo de San Pedro ⚠️ | Valdemoro | 1 |
| Plaza de Jose Crespo ⚠️ | Pinto | 1 |
| 8 de marzo ⚠️ | Pinto | 1 |
| Bois de Ciempozuelos ⚠️ | Ciempozuelos | 1 |
| Parque de Salvador Allende (2) ⚠️ | Coslada | 1 |
| Parque del Olivo ⚠️ | Coslada | 1 |
| Parque de Canillejas ⚠️ | Madrid › San Blas - Canillejas | 1 |
| Parque del Arquitecto Antonio Palacios ⚠️ | Madrid › San Blas - Canillejas | 1 |
| Parque de la Tejera ⚠️ | Moralzarzal | 1 |
| Parc de Valdemoro (2) ⚠️ | Valdemoro | 1 |
| Parque Ana Tutor ⚠️ | Valdemoro | 1 |
| Parque Río Manzanares ⚠️ | Valdemoro | 1 |
| Bois de Pinto ⚠️ | Pinto | 1 |
| Parc de Getafe ⚠️ | Getafe | 1 |
| Parque de la Chopera ⚠️ | Leganés | 1 |
| Plaza del Laberinto ⚠️ | Leganés | 1 |
| Parc de Madrid (156) ⚠️ | Madrid › Villaverde | 1 |
| Parc de Madrid (157) ⚠️ | Madrid › Hortaleza | 1 |
| Parque América ⚠️ | Humanes de Madrid | 1 |
| Parc de Móstoles ⚠️ | Móstoles | 1 |
| Parque Prado de Santo Domingo ⚠️ | Alcorcón | 1 |
| Parque de la Amistad ⚠️ | Madrid › Villaverde | 1 |
| Parque de la Maceta ⚠️ | Madrid › Vicálvaro | 1 |
| Parque Huerta del Obispo ⚠️ | Madrid › Villaverde | 1 |
| Parque del Peralejo ⚠️ | Alpedrete | 1 |
| Parc de Madrid (161) ⚠️ | Madrid › Carabanchel | 1 |
| Parc de Madrid (164) ⚠️ | Madrid › Villaverde | 1 |
| Parque de Serafín Díaz Antón ⚠️ | Leganés | 1 |
| Parc de Madrid (165) ⚠️ | Madrid › Puente de Vallecas | 1 |
| Jardín Campo de la Paloma ⚠️ | Madrid › Puente de Vallecas | 1 |
| Parque de Santa Eugenia ⚠️ | Madrid › Villa de Vallecas | 1 |
| Parque del Camino de Vasares ⚠️ | Madrid › Villa de Vallecas | 1 |
| Parque Saconia ⚠️ | Madrid › Villa de Vallecas | 1 |
| Parque de las cataratas ⚠️ | Madrid › Villa de Vallecas | 1 |
| Parc de Madrid (169) ⚠️ | Madrid › Villa de Vallecas | 1 |
| Parc de Madrid (170) ⚠️ | Madrid › Villa de Vallecas | 1 |
| Parc de Madrid (173) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parc de Madrid (177) ⚠️ | Madrid › Puente de Vallecas | 1 |
| Plaza de la Hispanidad ⚠️ | Alcorcón | 1 |
| Parc de Alcorcón (2) ⚠️ | Alcorcón | 1 |
| Parque de la Fuente Carrantona ⚠️ | Madrid › Moratalaz | 1 |
| Parc de Madrid (180) ⚠️ | Madrid › Moratalaz | 1 |
| Parc de Pinto ⚠️ | Pinto | 1 |
| Parc de Madrid (182) ⚠️ | Madrid › Arganzuela | 1 |
| Parque Plaza de Chozas de Canales ⚠️ | Madrid › Villaverde | 1 |
| Parc de Madrid (188) ⚠️ | Madrid › Usera | 1 |
| Parque Norte San Luciano ⚠️ | Madrid › Villaverde | 1 |
| Parque Bellas Artes ⚠️ | Pozuelo de Alarcón | 1 |
| Jardines de José Luis Jiménez Manso ⚠️ | Madrid › Moratalaz | 1 |
| Parque de La Bolera ⚠️ | San Lorenzo de El Escorial | 1 |
| Cañada Real Coruñesa ⚠️ | Alpedrete | 1 |
| Parque Cuartel Huerta ⚠️ | Móstoles | 1 |
| Real Observatorio de Madrid ⚠️ | Madrid › Retiro | 1 |
| Parc de Madrid (197) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parque de la Ladera ⚠️ | San Lorenzo de El Escorial | 1 |
| Jardín Campo del Toro ⚠️ | Madrid › Puente de Vallecas | 1 |
| Parc de Madrid (200) ⚠️ | Madrid › Usera | 1 |
| Parque de San Isidro (2) ⚠️ | Madrid › Carabanchel | 1 |
| Parc de Madrid (203) ⚠️ | Madrid › Latina | 1 |
| Parque de los Pinos ⚠️ | Madrid › Carabanchel | 1 |
| Parque de Navacerrada ⚠️ | Pozuelo de Alarcón | 1 |
| Parc de Pozuelo de Alarcón (22) ⚠️ | Pozuelo de Alarcón | 1 |
| Bois de San Fernando de Henares (2) ⚠️ | San Fernando de Henares | 1 |
| Parc de Pozuelo de Alarcón (24) ⚠️ | Pozuelo de Alarcón | 1 |
| Plaza de la Inmaculada ⚠️ | Leganés | 1 |
| Parque del DCC Aniversario ⚠️ | Leganés | 1 |
| Parque de la II República ⚠️ | Leganés | 1 |
| Forêt de Leganés ⚠️ | Leganés | 1 |
| Forêt de Leganés (2) ⚠️ | Leganés | 1 |
| Parc de Getafe (10) ⚠️ | Getafe | 1 |
| Parc de Madrid (206) ⚠️ | Madrid › Villaverde | 1 |
| Parc de Madrid (210) ⚠️ | Madrid › Arganzuela | 1 |
| Parque Martin Luther King ⚠️ | Madrid › Retiro | 1 |
| Parc de Madrid (215) ⚠️ | Madrid › Puente de Vallecas | 1 |
| Parc de Madrid (217) ⚠️ | Madrid › Puente de Vallecas | 1 |
| Jardines Casa del Reloj ⚠️ | Leganés | 1 |
| Parque Príncipes de Asturias ⚠️ | Leganés | 1 |
| Parque de Los Olivos ⚠️ | Leganés | 1 |
| Parque Miguel de Cervantes ⚠️ | Leganés | 1 |
| Parc de Madrid (221) ⚠️ | Madrid › Villaverde | 1 |
| Parc de Madrid (222) ⚠️ | Madrid › Villaverde | 1 |
| Parque del Olivar (2) ⚠️ | Madrid › Latina | 1 |
| Parc de Madrid (229) ⚠️ | Madrid › San Blas - Canillejas | 1 |
| Parque del Butrón ⚠️ | Madrid › San Blas - Canillejas | 1 |
| Parque Arriaga (2) ⚠️ | Madrid › Ciudad Lineal | 1 |
| Parque de Ajofrín ⚠️ | Madrid › San Blas - Canillejas | 1 |
| Parc de Madrid (237) ⚠️ | Madrid › Vicálvaro | 1 |
| Parc de Madrid (239) ⚠️ | Madrid › Vicálvaro | 1 |
| Parc de Madrid (240) ⚠️ | Madrid › Moratalaz | 1 |
| Plaza de Juan Benet ⚠️ | Madrid › Vicálvaro | 1 |
| Plaza de Juan Carlos Onetti ⚠️ | Madrid › Vicálvaro | 1 |
| Paseo sobre M-40 ⚠️ | Madrid › Hortaleza | 1 |
| Forêt de Alcobendas (2) ⚠️ | Alcobendas | 1 |
| Parque de Navarra II ⚠️ | Alcobendas | 1 |
| Parque de Galicia (sector sur) ⚠️ | Alcobendas | 1 |
| Parc de Alcobendas (7) ⚠️ | Alcobendas | 1 |
| Parc de Madrid (245) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parc de Madrid (247) ⚠️ | Madrid › Puente de Vallecas | 1 |
| Parc de Madrid (248) ⚠️ | Madrid › Moratalaz | 1 |
| Parc de Madrid (251) ⚠️ | Madrid › San Blas - Canillejas | 1 |
| Jardín de los Parrales ⚠️ | Madrid › Latina | 1 |
| Parque de la Chopera (2) ⚠️ | Getafe | 1 |
| Parque Laderas CB ⚠️ | Getafe | 1 |
| Bois de Parla ⚠️ | Parla | 1 |
| Parc de Móstoles (2) ⚠️ | Móstoles | 1 |
| Parque de Salvador Allende (3) ⚠️ | Móstoles | 1 |
| Parque Levante ⚠️ | Móstoles | 1 |
| Forêt de Madrid (12) ⚠️ | Madrid › Latina | 1 |
| Forêt de Madrid (13) ⚠️ | Madrid › Latina | 1 |
| Forêt de Madrid (14) ⚠️ | Madrid › Latina | 1 |
| Parc de Móstoles (4) ⚠️ | Móstoles | 1 |
| Parc de Alcorcón (9) ⚠️ | Alcorcón | 1 |
| Pinar de Fuente Marcela ⚠️ | Majadahonda | 1 |
| Parque de los Robles ⚠️ | Majadahonda | 1 |
| Parque Delta ⚠️ | Majadahonda | 1 |
| Parc de Soto del Real ⚠️ | Soto del Real | 1 |
| Bois de Soto del Real ⚠️ | Soto del Real | 1 |
| Bois de Colmenar Viejo (2) ⚠️ | Colmenar Viejo | 1 |
| Parque 11-M ⚠️ | Torrejón de Ardoz | 1 |
| Parque del Pinar ⚠️ | Fuenlabrada | 1 |
| Parque de Europa ⚠️ | Fuenlabrada | 1 |
| Bois de Velilla de San Antonio ⚠️ | Velilla de San Antonio | 1 |
| Parc de Rivas-Vaciamadrid (2) ⚠️ | Rivas-Vaciamadrid | 1 |
| Parc de Rivas-Vaciamadrid (5) ⚠️ | Rivas-Vaciamadrid | 1 |
| Parque Aztecas ⚠️ | Torrejón de Ardoz | 1 |
| Parc de Alcalá de Henares ⚠️ | Alcalá de Henares | 1 |
| Parc de Alcalá de Henares (2) ⚠️ | Alcalá de Henares | 1 |
| Parc de Alcalá de Henares (4) ⚠️ | Alcalá de Henares | 1 |
| Parc de Alcalá de Henares (7) ⚠️ | Alcalá de Henares | 1 |
| Jardines de Juan Pablo II ⚠️ | Alcalá de Henares | 1 |
| Parque del Lavadero ⚠️ | Camarma de Esteruelas | 1 |
| Parc de Alcalá de Henares (9) ⚠️ | Alcalá de Henares | 1 |
| Parc de Madrid (266) ⚠️ | Madrid › Villaverde | 1 |
| Bois de El Vellón ⚠️ | El Vellón | 1 |
| Parque del Arroyo Fontarrón (2) ⚠️ | Madrid › Moratalaz | 1 |
| Parc de Madrid (268) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parc de Madrid (269) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Plaza de la Villa de París ⚠️ | Madrid › Centro | 1 |
| Forêt de Mejorada del Campo ⚠️ | Mejorada del Campo | 1 |
| Parque de Justo Gallego ⚠️ | Mejorada del Campo | 1 |
| Forêt de San Fernando de Henares (3) ⚠️ | San Fernando de Henares | 1 |
| Jardín del Tío Basilio ⚠️ | Madrid › Villaverde | 1 |
| Parc de Madrid (273) ⚠️ | Madrid › Tetuán | 1 |
| Parc de Madrid (275) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parc de Griñón ⚠️ | Griñón | 1 |
| Parque de La Espuela ⚠️ | Madrid › Hortaleza | 1 |
| Parc de Madrid (281) ⚠️ | Madrid › San Blas - Canillejas | 1 |
| Parc de Madrid (282) ⚠️ | Madrid › San Blas - Canillejas | 1 |
| Parc de Getafe (13) ⚠️ | Getafe | 1 |
| Plaza de Europa ⚠️ | Rivas-Vaciamadrid | 1 |
| Parque San Isidro ⚠️ | Rivas-Vaciamadrid | 1 |
| Parc de Coslada (2) ⚠️ | Coslada | 1 |
| Parc de Getafe (25) ⚠️ | Getafe | 1 |
| Parc de Leganés (14) ⚠️ | Leganés | 1 |
| Parc de Madrid (290) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Bois de Madrid (6) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Forêt de Ribatejada ⚠️ | Ribatejada | 1 |
| Bois de Valdeolmos-Alalpardo ⚠️ | Valdeolmos-Alalpardo | 1 |
| Bois de Valdeolmos-Alalpardo (2) ⚠️ | Valdeolmos-Alalpardo | 1 |
| Bois de Valdeolmos-Alalpardo (4) ⚠️ | Ribatejada | 1 |
| Parc de Madrid (298) ⚠️ | Madrid › Villaverde | 1 |
| Parc de Madrid (299) ⚠️ | Madrid › Villaverde | 1 |
| Bois de San Sebastián de los Reyes (4) ⚠️ | San Sebastián de los Reyes | 1 |
| Bois de San Sebastián de los Reyes (5) ⚠️ | San Sebastián de los Reyes | 1 |
| Forêt de San Sebastián de los Reyes (2) ⚠️ | San Sebastián de los Reyes | 1 |
| Bois de San Sebastián de los Reyes (6) ⚠️ | San Sebastián de los Reyes | 1 |
| Bois de San Sebastián de los Reyes (7) ⚠️ | San Sebastián de los Reyes | 1 |
| Parc de Pinto (2) ⚠️ | Pinto | 1 |
| Forêt de Alcalá de Henares (2) ⚠️ | Alcalá de Henares | 1 |
| Forêt de Torrejón de la Calzada ⚠️ | Torrejón de la Calzada | 1 |
| Parque Monte Alto ⚠️ | Las Rozas de Madrid | 1 |
| Bois de Galapagar (2) ⚠️ | Galapagar | 1 |
| Parque Víctimas del Terrorismo ⚠️ | Boadilla del Monte | 1 |
| Forêt de Rivas-Vaciamadrid (7) ⚠️ | Rivas-Vaciamadrid | 1 |
| Forêt de Rivas-Vaciamadrid (8) ⚠️ | Rivas-Vaciamadrid | 1 |
| Parc de Arganda del Rey (9) ⚠️ | Arganda del Rey | 1 |
| Bois de Chinchón (3) ⚠️ | Chinchón | 1 |
| Valquejigoso ⚠️ | Chinchón | 1 |
| Bois de Aranjuez ⚠️ | Titulcia | 1 |
| Forêt de Arganda del Rey (4) ⚠️ | Arganda del Rey | 1 |
| Forêt de Las Rozas de Madrid (4) ⚠️ | Las Rozas de Madrid | 1 |
| Bois de Las Rozas de Madrid (2) ⚠️ | Las Rozas de Madrid | 1 |
| Parc de Madrid (304) ⚠️ | Madrid › Hortaleza | 1 |
| Parque Félix Rodríguez de la Fuente (2) ⚠️ | Colmenar Viejo | 1 |
| Parc de Rivas-Vaciamadrid (12) ⚠️ | Rivas-Vaciamadrid | 1 |
| Parque de San Isidro (4) ⚠️ | Torrejón de Ardoz | 1 |
| Centro Cultural Volturno ⚠️ | Pozuelo de Alarcón | 1 |
| Parque del V Centenario ⚠️ | San Martín de la Vega | 1 |
| Parc de Fuenlabrada (3) ⚠️ | Fuenlabrada | 1 |
| Bois de Moralzarzal ⚠️ | Moralzarzal | 1 |
| Bois de Hoyo de Manzanares ⚠️ | Hoyo de Manzanares | 1 |
| Parque de Extrenadura ⚠️ | Parla | 1 |
| Forêt de Madrid (18) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parc de Madrid (312) ⚠️ | Madrid › Chamberí | 1 |
| Plaza del Conde del Valle de Suchil ⚠️ | Madrid › Chamberí | 1 |
| Parque Duque del Infantado ⚠️ | Manzanares el Real | 1 |
| Parc de Aranjuez ⚠️ | Aranjuez | 1 |
| Parque del Encinar ⚠️ | Arroyomolinos | 1 |
| Parc de Algete ⚠️ | Algete | 1 |
| Parque de la Ballena ⚠️ | Parla | 1 |
| Parque de la Hermandad de Nuestra Señora de la Soledad ⚠️ | Parla | 1 |
| Parc de Parla (2) ⚠️ | Parla | 1 |
| Parc de Parla (4) ⚠️ | Parla | 1 |
| Parque de Nicolás Fuster ⚠️ | Pinto | 1 |
| Parc de Parla (8) ⚠️ | Parla | 1 |
| Parque Castilla y León ⚠️ | Parla | 1 |
| Parque de Feliciano Fernández ⚠️ | Navalcarnero | 1 |
| Parc de Navalcarnero (2) ⚠️ | Navalcarnero | 1 |
| Parc de El Boalo-Cerceda-Mataelpino ⚠️ | El Boalo-Cerceda-Mataelpino | 1 |
| Bois de Madrid (8) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parque Lineal de la Serna (2) ⚠️ | Fuenlabrada | 1 |
| El Huerto del Cura ⚠️ | Fuenlabrada | 1 |
| Parque de las Torres ⚠️ | Torrejón de Ardoz | 1 |
| Parque de la Luna ⚠️ | Torrejón de Ardoz | 1 |
| Zona recreativa El Berzalejo ⚠️ | Hoyo de Manzanares | 1 |
| Parc de El Boalo-Cerceda-Mataelpino (2) ⚠️ | El Boalo-Cerceda-Mataelpino | 1 |
| Forêt de Santa María de la Alameda ⚠️ | Santa María de la Alameda | 1 |
| Parque de las Víctimas del Terrorismo ⚠️ | Alcobendas | 1 |
| Parc de San Sebastián de los Reyes (8) ⚠️ | San Sebastián de los Reyes | 1 |
| Jardines de Pablo Sorozábal ⚠️ | Madrid › Chamartín | 1 |
| Parque del Actor Paco Rabal ⚠️ | Alcorcón | 1 |
| Parque central del Bercial ⚠️ | Getafe | 1 |
| Parc de Colmenar Viejo (4) ⚠️ | Colmenar Viejo | 1 |
| Parc de Colmenar Viejo (5) ⚠️ | Colmenar Viejo | 1 |
| Parc de Colmenar Viejo (6) ⚠️ | Colmenar Viejo | 1 |
| Forêt de Cenicientos ⚠️ | Cenicientos | 1 |
| Forêt de Cadalso de los Vidrios ⚠️ | Cadalso de los Vidrios | 1 |
| Forêt de Serranillos del Valle ⚠️ | Serranillos del Valle | 1 |
| Forêt de San Martín de Valdeiglesias (7) ⚠️ | San Martín de Valdeiglesias | 1 |
| Forêt de San Martín de Valdeiglesias (9) ⚠️ | San Martín de Valdeiglesias | 1 |
| Forêt de Patones (2) ⚠️ | Patones | 1 |
| Forêt de Ambite (2) ⚠️ | Ambite | 1 |
| Forêt de Valdepiélagos ⚠️ | Valdepiélagos | 1 |
| Forêt de Torremocha de Jarama (3) ⚠️ | Torremocha de Jarama | 1 |
| Forêt de Pezuela de las Torres (3) ⚠️ | Pezuela de las Torres | 1 |
| Forêt de La Cabrera (6) ⚠️ | La Cabrera | 1 |
| Parc de San Sebastián de los Reyes (9) ⚠️ | San Sebastián de los Reyes | 1 |
| Parc de Madrid (333) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parque de Gabriel Martín ⚠️ | Pinto | 1 |
| Parc de Pozuelo de Alarcón (26) ⚠️ | Pozuelo de Alarcón | 1 |
| Huerta de la Partida ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parque de Lorenzo Azofra ⚠️ | Getafe | 1 |
| Plaza de Setúbal ⚠️ | Madrid › Carabanchel | 1 |
| Plaza de la Parroquia ⚠️ | Madrid › Carabanchel | 1 |
| Parque de Lucero ⚠️ | Madrid › Latina | 1 |
| Parc de Colmenar Viejo (8) ⚠️ | Colmenar Viejo | 1 |
| Parc de Colmenar Viejo (10) ⚠️ | Colmenar Viejo | 1 |
| Parque de Buero Vallejo ⚠️ | Alcorcón | 1 |
| Parc de Madrid (345) ⚠️ | Madrid › Latina | 1 |
| Parque Darwin (3) ⚠️ | Alcorcón | 1 |
| Parc de Madrid (353) ⚠️ | Madrid › Latina | 1 |
| Plaza del Patriarca Eijo y Garay ⚠️ | Madrid › Latina | 1 |
| Parc de Madrid (359) ⚠️ | Madrid › Latina | 1 |
| Forêt de Madrid (23) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Forêt de Madrid (28) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Forêt de Madrid (30) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Forêt de Madrid (33) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parc de Moralzarzal (2) ⚠️ | Moralzarzal | 1 |
| Parque del Rosario ⚠️ | Torrejón de Ardoz | 1 |
| Parc de Moralzarzal (3) ⚠️ | Moralzarzal | 1 |
| Jardines Aniceto Marinas ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Jardín El Torero ⚠️ | Madrid › Usera | 1 |
| Parque del Real ⚠️ | Madrid › Carabanchel | 1 |
| Parc de Madrid (380) ⚠️ | Madrid › Villa de Vallecas | 1 |
| Parc de Madrid (381) ⚠️ | Madrid › Villa de Vallecas | 1 |
| Jardín de Yolanda González ⚠️ | Madrid › Latina | 1 |
| Parc de Madrid (384) ⚠️ | Madrid › Villa de Vallecas | 1 |
| Parc de Madrid (385) ⚠️ | Madrid › Villa de Vallecas | 1 |
| Parc de Madrid (386) ⚠️ | Madrid › Villa de Vallecas | 1 |
| Parc de Madrid (389) ⚠️ | Madrid › Villa de Vallecas | 1 |
| Parc de Madrid (390) ⚠️ | Madrid › Villa de Vallecas | 1 |
| Parque Daniel Zuazo ⚠️ | Madrid › Latina | 1 |
| Parc de Madrid (395) ⚠️ | Madrid › Villa de Vallecas | 1 |
| Parc de Madrid (396) ⚠️ | Madrid › Villa de Vallecas | 1 |
| Parque Manuel de Falla ⚠️ | Majadahonda | 1 |
| Parc de Madrid (402) ⚠️ | Madrid › Villa de Vallecas | 1 |
| Parque Infantil Santa Eugenia ⚠️ | Madrid › Villa de Vallecas | 1 |
| Parque del metro de La Gavia ⚠️ | Madrid › Villa de Vallecas | 1 |
| Parc de Madrid (408) ⚠️ | Madrid › Villa de Vallecas | 1 |
| Parc de Madrid (416) ⚠️ | Madrid › Villa de Vallecas | 1 |
| Parque de Valdeperdices ⚠️ | Madrid › Villa de Vallecas | 1 |
| Parc de Madrid (424) ⚠️ | Madrid › Latina | 1 |
| Parc de Madrid (425) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Paseo Federico García Lorca ⚠️ | Madrid › Villa de Vallecas | 1 |
| Parc de Madrid (430) ⚠️ | Madrid › Villa de Vallecas | 1 |
| Parc de Madrid (431) ⚠️ | Madrid › Villa de Vallecas | 1 |
| Jardín de Francisco Javier Sáenz de Oiza ⚠️ | Madrid › Chamartín | 1 |
| Parc de Pozuelo de Alarcón (29) ⚠️ | Pozuelo de Alarcón | 1 |
| Parc de Madrid (436) ⚠️ | Madrid › Moratalaz | 1 |
| Parc de Fuenlabrada (12) ⚠️ | Fuenlabrada | 1 |
| Parc de Madrid (438) ⚠️ | Madrid › Moratalaz | 1 |
| Forêt de Pozuelo de Alarcón (10) ⚠️ | Pozuelo de Alarcón | 1 |
| Parque Cerro de las Norias ⚠️ | Majadahonda | 1 |
| Parque de la Compresa ⚠️ | Valdemoro | 1 |
| Parc de Alcorcón (17) ⚠️ | Alcorcón | 1 |
| Parc de Alcorcón (19) ⚠️ | Alcorcón | 1 |
| Parc de Alcorcón (20) ⚠️ | Alcorcón | 1 |
| Parc de Rivas-Vaciamadrid (14) ⚠️ | Rivas-Vaciamadrid | 1 |
| Parc de Móstoles (8) ⚠️ | Móstoles | 1 |
| Parc de Móstoles (21) ⚠️ | Móstoles | 1 |
| Parc de Velilla de San Antonio (5) ⚠️ | Velilla de San Antonio | 1 |
| Parc de Velilla de San Antonio (6) ⚠️ | Velilla de San Antonio | 1 |
| Parc de Madrid (470) ⚠️ | Madrid › Hortaleza | 1 |
| Parc de Madrid (472) ⚠️ | Madrid › Hortaleza | 1 |
| Parc de Madrid (481) ⚠️ | Madrid › Hortaleza | 1 |
| Parc de Móstoles (24) ⚠️ | Móstoles | 1 |
| Forêt de San Fernando de Henares (4) ⚠️ | San Fernando de Henares | 1 |
| Forêt de San Fernando de Henares (6) ⚠️ | San Fernando de Henares | 1 |
| Recinto Ferial (3) ⚠️ | Fuenlabrada | 1 |
| Parc de Fuenlabrada (17) ⚠️ | Fuenlabrada | 1 |
| Parque de la Fuente ⚠️ | Fuenlabrada | 1 |
| Parque de La Paz (2) ⚠️ | San Fernando de Henares | 1 |
| Parque Lineal de Las Eras ⚠️ | Fuenlabrada | 1 |
| Vegetación Madrileña ⚠️ | Leganés | 1 |
| Forêt de Leganés (4) ⚠️ | Leganés | 1 |
| Forêt de Leganés (5) ⚠️ | Leganés | 1 |
| Parc de Madrid (496) ⚠️ | Madrid › Retiro | 1 |
| Parque de Francos Rodríguez ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parc de Alcobendas (9) ⚠️ | Alcobendas | 1 |
| Parc de Móstoles (27) ⚠️ | Móstoles | 1 |
| Parc de Quijorna ⚠️ | Quijorna | 1 |
| Parc de Quijorna (2) ⚠️ | Quijorna | 1 |
| Plaza de Los Llanos ⚠️ | Fuenlabrada | 1 |
| Parque Tomillar ⚠️ | Villamantilla | 1 |
| Parque Kiosco ⚠️ | Villamantilla | 1 |
| Parc de Villanueva de Perales (4) ⚠️ | Villanueva de Perales | 1 |
| Parque Arroyo del Soto (2) ⚠️ | Móstoles | 1 |
| Forêt de Sevilla la Nueva ⚠️ | Sevilla la Nueva | 1 |
| Forêt de Navalagamella (8) ⚠️ | Navalagamella | 1 |
| Bois de Robledo de Chavela ⚠️ | Robledo de Chavela | 1 |
| Forêt de Robledo de Chavela (17) ⚠️ | Robledo de Chavela | 1 |
| Forêt de Madrid (35) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Bois de Valdemaqueda ⚠️ | Valdemaqueda | 1 |
| Parque de Tebas ⚠️ | Fuenlabrada | 1 |
| Forêt de Zarzalejo ⚠️ | Zarzalejo | 1 |
| Forêt de Robledo de Chavela (29) ⚠️ | Robledo de Chavela | 1 |
| Forêt de Valdemaqueda (12) ⚠️ | Valdemaqueda | 1 |
| Forêt de Madrid (37) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parque de la Catarata Cortada ⚠️ | Arroyomolinos | 1 |
| Parque Calle de Comillas ⚠️ | Arroyomolinos | 1 |
| Parc de Torrelodones ⚠️ | Torrelodones | 1 |
| Bois de Santa María de la Alameda (3) ⚠️ | Santa María de la Alameda | 1 |
| Bois de Santa María de la Alameda (5) ⚠️ | Santa María de la Alameda | 1 |
| Bois de Santa María de la Alameda (6) ⚠️ | Santa María de la Alameda | 1 |
| Bois de Santa María de la Alameda (9) ⚠️ | Santa María de la Alameda | 1 |
| Forêt de Madrid (39) ⚠️ | Madrid › Vicálvaro | 1 |
| Forêt de Santa María de la Alameda (15) ⚠️ | Santa María de la Alameda | 1 |
| Bois de Santa María de la Alameda (17) ⚠️ | Santa María de la Alameda | 1 |
| Forêt de Santa María de la Alameda (23) ⚠️ | Santa María de la Alameda | 1 |
| Bois de Santa María de la Alameda (21) ⚠️ | Santa María de la Alameda | 1 |
| Forêt de Santa María de la Alameda (27) ⚠️ | Santa María de la Alameda | 1 |
| Forêt de Santa María de la Alameda (31) ⚠️ | Santa María de la Alameda | 1 |
| Forêt de Santa María de la Alameda (32) ⚠️ | Santa María de la Alameda | 1 |
| Parque Lineal Juan Carlos I ⚠️ | Boadilla del Monte | 1 |
| Parque Lineal Juan Carlos I (5) ⚠️ | Boadilla del Monte | 1 |
| Jardines del Museo del Traje ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parque Boadilla Centro ⚠️ | Boadilla del Monte | 1 |
| Parc de Arroyomolinos (3) ⚠️ | Arroyomolinos | 1 |
| Parque de los Galayos ⚠️ | Arroyomolinos | 1 |
| Forêt de San Martín de Valdeiglesias (13) ⚠️ | San Martín de Valdeiglesias | 1 |
| Forêt de Madrid (42) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parque Pozo de las Nieves ⚠️ | Aranjuez | 1 |
| Parc de Alcorcón (23) ⚠️ | Alcorcón | 1 |
| Parc de Villalbilla (2) ⚠️ | Villalbilla | 1 |
| Parque de El Calvario ⚠️ | Torres de la Alameda | 1 |
| Parque de Olof Palme ⚠️ | Torres de la Alameda | 1 |
| Parc de Móstoles (28) ⚠️ | Móstoles | 1 |
| Parc de Rivas-Vaciamadrid (15) ⚠️ | Rivas-Vaciamadrid | 1 |
| Parc de Rivas-Vaciamadrid (16) ⚠️ | Rivas-Vaciamadrid | 1 |
| Parc de Madrid (504) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parque del Trigal ⚠️ | Navacerrada | 1 |
| Parque Antonio López ⚠️ | Tres Cantos | 1 |
| Bois de Navacerrada (6) ⚠️ | Navacerrada | 1 |
| Parc de Navacerrada (3) ⚠️ | Navacerrada | 1 |
| Parque Fuente del Espino ⚠️ | Alcorcón | 1 |
| Bois de Becerril de la Sierra (2) ⚠️ | Becerril de la Sierra | 1 |
| Plaza de las Eras ⚠️ | Getafe | 1 |
| Jardín Narváez ⚠️ | Aranjuez | 1 |
| Parc de Torrejón de Ardoz (8) ⚠️ | Torrejón de Ardoz | 1 |
| Parc de Madrid (507) ⚠️ | Madrid › Centro | 1 |
| Parc de Madrid (508) ⚠️ | Madrid › Hortaleza | 1 |
| Recinto ferial municipal ⚠️ | Collado Villalba | 1 |
| Parque El Mirador ⚠️ | Cobeña | 1 |
| Forêt de Brea de Tajo (6) ⚠️ | Brea de Tajo | 1 |
| Parc de Serranillos del Valle ⚠️ | Serranillos del Valle | 1 |
| Parque Catalina de Aragón ⚠️ | Alcalá de Henares | 1 |
| Parc de Cobeña (6) ⚠️ | Cobeña | 1 |
| Parque del Cerro Peñabel ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Bois de San Martín de Valdeiglesias ⚠️ | San Martín de Valdeiglesias | 1 |
| Parc de Fuenlabrada (40) ⚠️ | Fuenlabrada | 1 |
| Parc de Cobeña (9) ⚠️ | Cobeña | 1 |
| Plaza de Esquivias ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Jardín del Profesor Joaquín Garrigues ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Forêt de San Martín de Valdeiglesias (17) ⚠️ | San Martín de Valdeiglesias | 1 |
| Parque de la Cija ⚠️ | Navas del Rey | 1 |
| Forêt de Paracuellos de Jarama (5) ⚠️ | Paracuellos de Jarama | 1 |
| Parque Rosales ⚠️ | Móstoles | 1 |
| Parque del Machucho Bajo ⚠️ | San Lorenzo de El Escorial | 1 |
| Mirador de Humanes ⚠️ | Moraleja de Enmedio | 1 |
| Forêt de Corpa (2) ⚠️ | Corpa | 1 |
| Forêt de Corpa (3) ⚠️ | Corpa | 1 |
| Parc de Boadilla del Monte (23) ⚠️ | Boadilla del Monte | 1 |
| Parque Salvador de Madariaga (2) ⚠️ | Alcalá de Henares | 1 |
| Parc de Móstoles (29) ⚠️ | Móstoles | 1 |
| Forêt de Braojos ⚠️ | Braojos | 1 |
| Forêt de Braojos (3) ⚠️ | Braojos | 1 |
| Forêt de Horcajo de la Sierra-Aoslos ⚠️ | Horcajo de la Sierra-Aoslos | 1 |
| Parc de Móstoles (32) ⚠️ | Móstoles | 1 |
| Parc de Móstoles (34) ⚠️ | Móstoles | 1 |
| Recinto Ferial (4) ⚠️ | Alcalá de Henares | 1 |
| Forêt de Gascones ⚠️ | Gascones | 1 |
| Forêt de Somosierra (4) ⚠️ | Somosierra | 1 |
| Forêt de Villavieja del Lozoya (2) ⚠️ | Villavieja del Lozoya | 1 |
| Forêt de Braojos (9) ⚠️ | Braojos | 1 |
| Forêt de Somosierra (10) ⚠️ | Somosierra | 1 |
| Forêt de Somosierra (17) ⚠️ | Somosierra | 1 |
| Forêt de Somosierra (22) ⚠️ | Somosierra | 1 |
| Bois de Fresnedillas de la Oliva ⚠️ | Robledo de Chavela | 1 |
| Bois de Robledo de Chavela (12) ⚠️ | Robledo de Chavela | 1 |
| Bois de Robledo de Chavela (13) ⚠️ | Robledo de Chavela | 1 |
| Bois de Robledo de Chavela (18) ⚠️ | Robledo de Chavela | 1 |
| Bois de Quijorna (2) ⚠️ | Quijorna | 1 |
| Bois de Quijorna (7) ⚠️ | Quijorna | 1 |
| Bois de Zarzalejo (3) ⚠️ | Zarzalejo | 1 |
| Parque Darwin (4) ⚠️ | Madrid › Moratalaz | 1 |
| Forêt de Zarzalejo (11) ⚠️ | Zarzalejo | 1 |
| Forêt de Zarzalejo (23) ⚠️ | Zarzalejo | 1 |
| Parc de Alcobendas (40) ⚠️ | Alcobendas | 1 |
| Parc de Alcobendas (46) ⚠️ | Alcobendas | 1 |
| Parc de Alcobendas (47) ⚠️ | Alcobendas | 1 |
| Parque del Cantero ⚠️ | Alpedrete | 1 |
| Forêt de Zarzalejo (52) ⚠️ | Zarzalejo | 1 |
| Forêt de Zarzalejo (59) ⚠️ | Zarzalejo | 1 |
| Forêt de Zarzalejo (97) ⚠️ | Zarzalejo | 1 |
| Forêt de Zarzalejo (99) ⚠️ | Zarzalejo | 1 |
| Forêt de San Martín de la Vega (8) ⚠️ | San Martín de la Vega | 1 |
| Forêt de Zarzalejo (133) ⚠️ | Zarzalejo | 1 |
| Forêt de Zarzalejo (145) ⚠️ | Zarzalejo | 1 |
| Parc de Madrid (531) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Forêt de Zarzalejo (156) ⚠️ | Zarzalejo | 1 |
| Forêt de Robledo de Chavela (53) ⚠️ | Robledo de Chavela | 1 |
| Forêt de Zarzalejo (161) ⚠️ | Zarzalejo | 1 |
| Parque Municipal (2) ⚠️ | Campo Real | 1 |
| Forêt de Zarzalejo (162) ⚠️ | Zarzalejo | 1 |
| Forêt de Zarzalejo (168) ⚠️ | Zarzalejo | 1 |
| Parc de Móstoles (39) ⚠️ | Móstoles | 1 |
| Parc de Madrid (534) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Forêt de El Escorial (21) ⚠️ | El Escorial | 1 |
| Parc de Madrid (535) ⚠️ | Madrid › Ciudad Lineal | 1 |
| Parc de Brunete (2) ⚠️ | Brunete | 1 |
| Parque Juan Pablo II ⚠️ | Brunete | 1 |
| Parc de Madrid (538) ⚠️ | Madrid › Ciudad Lineal | 1 |
| Parque Cerro del Tambor ⚠️ | San Sebastián de los Reyes | 1 |
| Parc de Alcobendas (52) ⚠️ | Alcobendas | 1 |
| Parc de Las Rozas de Madrid (10) ⚠️ | Las Rozas de Madrid | 1 |
| Parc de Villanueva del Pardillo (3) ⚠️ | Villanueva del Pardillo | 1 |
| Paseo del Océano Atlántico ⚠️ | Coslada | 1 |
| Parc de Leganés (17) ⚠️ | Leganés | 1 |
| Parc de Madrid (549) ⚠️ | Madrid › Villa de Vallecas | 1 |
| Jardín de Embajadores M-30 ⚠️ | Madrid › Arganzuela | 1 |
| Parc de Guadarrama (2) ⚠️ | Guadarrama | 1 |
| Parc de Paracuellos de Jarama (3) ⚠️ | Paracuellos de Jarama | 1 |
| Parc de Fuenlabrada (54) ⚠️ | Fuenlabrada | 1 |
| Parc de Fuenlabrada (56) ⚠️ | Fuenlabrada | 1 |
| Parc de Fuenlabrada (58) ⚠️ | Fuenlabrada | 1 |
| Parc de Fuenlabrada (62) ⚠️ | Fuenlabrada | 1 |
| Parque de Olof Palme (2) ⚠️ | Madrid › Usera | 1 |
| Bois de Madrid (23) ⚠️ | Madrid › San Blas - Canillejas | 1 |
| Plaza Elíptica ⚠️ | Aranjuez | 1 |
| Parc de Collado Villalba (3) ⚠️ | Collado Villalba | 1 |
| Parque de Gloria Fuertes ⚠️ | Collado Villalba | 1 |
| Parque de las Provincias ⚠️ | Torrejón de Velasco | 1 |
| Parc de Madrid (556) ⚠️ | Madrid › Hortaleza | 1 |
| Bois de Fuenlabrada ⚠️ | Fuenlabrada | 1 |
| Forêt de Villar del Olmo (2) ⚠️ | Villar del Olmo | 1 |
| Forêt de Villar del Olmo (3) ⚠️ | Villar del Olmo | 1 |
| Parc de Fuenlabrada (70) ⚠️ | Fuenlabrada | 1 |
| Parque de Las Quirogas ⚠️ | Colmenarejo | 1 |
| Parque del Punto Limpio ⚠️ | Colmenarejo | 1 |
| Parque de la Trashumancia ⚠️ | Colmenarejo | 1 |
| Parque de las Islas Filipinas ⚠️ | Alcalá de Henares | 1 |
| Forêt de Redueña ⚠️ | Redueña | 1 |
| Bois de Redueña (10) ⚠️ | Redueña | 1 |
| Forêt de Redueña (2) ⚠️ | Redueña | 1 |
| Parc de San Sebastián de los Reyes (13) ⚠️ | San Sebastián de los Reyes | 1 |
| Parque Fuente de la Salud ⚠️ | Pozuelo de Alarcón | 1 |
| Parque Aluche ⚠️ | Madrid › Latina | 1 |
| Parc de Villanueva de la Cañada (18) ⚠️ | Villanueva de la Cañada | 1 |
| Plaza de la Concordia Adolfo Suárez ⚠️ | Villaviciosa de Odón | 1 |
| Parc de Madrid (565) ⚠️ | Madrid › Puente de Vallecas | 1 |
| Parque fluvial de Villamanrique de Tajo ⚠️ | Villamanrique de Tajo | 1 |
| Parque Carlos Marx ⚠️ | Coslada | 1 |
| Parc de Cubas de la Sagra (3) ⚠️ | Cubas de la Sagra | 1 |
| Parc de Cubas de la Sagra (4) ⚠️ | Cubas de la Sagra | 1 |
| Parc de Cubas de la Sagra (5) ⚠️ | Cubas de la Sagra | 1 |
| Parque de El País de Nunca Jamas ⚠️ | Getafe | 1 |
| Moscatelares park ⚠️ | San Sebastián de los Reyes | 1 |
| Parque Daniel Caballero ⚠️ | Villaconejos | 1 |
| Parque de la Ermita de San Isidro ⚠️ | Villaconejos | 1 |
| Bois de Villaconejos ⚠️ | Villaconejos | 1 |
| Bois de Villaconejos (2) ⚠️ | Villaconejos | 1 |
| Bois de Villaconejos (4) ⚠️ | Villaconejos | 1 |
| Bois de Villaconejos (6) ⚠️ | Villaconejos | 1 |
| Jardines de los Huertos ⚠️ | Colmenar de Oreja | 1 |
| Parque de las Comunidades ⚠️ | Torrejón de la Calzada | 1 |
| Parc de Pinto (9) ⚠️ | Pinto | 1 |
| Parc de Parla (20) ⚠️ | Parla | 1 |
| Plaza de la Rábida ⚠️ | Pinto | 1 |
| Parc de Móstoles (48) ⚠️ | Móstoles | 1 |
| Parc de Móstoles (49) ⚠️ | Móstoles | 1 |
| Parc de Móstoles (50) ⚠️ | Móstoles | 1 |
| Parc de Móstoles (53) ⚠️ | Móstoles | 1 |
| Parc de Móstoles (57) ⚠️ | Móstoles | 1 |
| Parc de Móstoles (59) ⚠️ | Móstoles | 1 |
| Plaza del Viento ⚠️ | Alcalá de Henares | 1 |
| Parc de Móstoles (62) ⚠️ | Móstoles | 1 |
| Parque Calero (2) ⚠️ | Madrid › Ciudad Lineal | 1 |
| Parc de Madrid (576) ⚠️ | Madrid › Vicálvaro | 1 |
| Isla de Chamartín ⚠️ | Madrid › Hortaleza | 1 |
| Bois de Móstoles (4) ⚠️ | Móstoles | 1 |
| Parc de Las Rozas de Madrid (11) ⚠️ | Las Rozas de Madrid | 1 |
| Parc de Las Rozas de Madrid (13) ⚠️ | Las Rozas de Madrid | 1 |
| Bois de Madrid (25) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parc de Pozuelo de Alarcón (33) ⚠️ | Pozuelo de Alarcón | 1 |
| Bois de Arroyomolinos (2) ⚠️ | Arroyomolinos | 1 |
| Parc de Móstoles (68) ⚠️ | Móstoles | 1 |
| Parc de Móstoles (74) ⚠️ | Móstoles | 1 |
| Parc de Móstoles (75) ⚠️ | Móstoles | 1 |
| Parc de Móstoles (76) ⚠️ | Móstoles | 1 |
| Parc de Móstoles (77) ⚠️ | Móstoles | 1 |
| Parc de Móstoles (79) ⚠️ | Móstoles | 1 |
| Parque de Salvador Allende (4) ⚠️ | Móstoles | 1 |
| Parc de Móstoles (89) ⚠️ | Móstoles | 1 |
| Parc de Móstoles (96) ⚠️ | Móstoles | 1 |
| Parc de Madrid (585) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parc de Madrid (587) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parc de Madrid (589) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parc de Getafe (32) ⚠️ | Getafe | 1 |
| Parc de Getafe (33) ⚠️ | Getafe | 1 |
| Forêt de Rivas-Vaciamadrid (17) ⚠️ | Rivas-Vaciamadrid | 1 |
| Forêt de Rivas-Vaciamadrid (19) ⚠️ | Rivas-Vaciamadrid | 1 |
| Forêt de Rivas-Vaciamadrid (22) ⚠️ | Rivas-Vaciamadrid | 1 |
| Bois de Rivas-Vaciamadrid (7) ⚠️ | Rivas-Vaciamadrid | 1 |
| Bois de Rivas-Vaciamadrid (9) ⚠️ | Rivas-Vaciamadrid | 1 |
| Parc de Móstoles (103) ⚠️ | Móstoles | 1 |
| Plaza de Saconia ⚠️ | Fuenlabrada | 1 |
| Parc de Madrid (599) ⚠️ | Madrid › Moratalaz | 1 |
| Jardín del Duque ⚠️ | Valdemoro | 1 |
| Parc de Valdemoro (6) ⚠️ | Valdemoro | 1 |
| Parc de Madrid (608) ⚠️ | Madrid › Moratalaz | 1 |
| Parque Andalucía (2) ⚠️ | Torrejón de Ardoz | 1 |
| Parc de Aranjuez (5) ⚠️ | Aranjuez | 1 |
| Parque Circular ⚠️ | Valdemoro | 1 |
| Parc de Brunete (3) ⚠️ | Brunete | 1 |
| Parc de Valdemoro (12) ⚠️ | Valdemoro | 1 |
| Parc de Coslada (5) ⚠️ | Coslada | 1 |
| Parc de Colmenar Viejo (12) ⚠️ | Colmenar Viejo | 1 |
| Parc de Alcobendas (59) ⚠️ | Alcobendas | 1 |
| Parc de Madrid (625) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parc de Madrid (626) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parque Tamames ⚠️ | Coslada | 1 |
| Paseo av. colmenar ⚠️ | Tres Cantos | 1 |
| Parc de Tres Cantos (2) ⚠️ | Tres Cantos | 1 |
| Paseo av del parque (2) ⚠️ | Tres Cantos | 1 |
| Parc de Humanes de Madrid (9) ⚠️ | Humanes de Madrid | 1 |
| Glorieta de Antoñete ⚠️ | Madrid › Barajas | 1 |
| Parc de Las Rozas de Madrid (16) ⚠️ | Las Rozas de Madrid | 1 |
| Forêt de Madrid (58) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parc de Madrid (631) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Forêt de Alcobendas (3) ⚠️ | Alcobendas | 1 |
| Jardines del Arquitecto Ribera ⚠️ | Madrid › Centro | 1 |
| Parque de Santa Tecla ⚠️ | Collado Villalba | 1 |
| Parc de Madrid (641) ⚠️ | Madrid › Ciudad Lineal | 1 |
| Bois de Madrid (29) ⚠️ | Madrid › Ciudad Lineal | 1 |
| Bois de Madrid (31) ⚠️ | Madrid › Ciudad Lineal | 1 |
| Bois de Madrid (39) ⚠️ | Madrid › Ciudad Lineal | 1 |
| Bois de Madrid (49) ⚠️ | Madrid › Ciudad Lineal | 1 |
| Bois de Madrid (53) ⚠️ | Madrid › Ciudad Lineal | 1 |
| Bois de Madrid (54) ⚠️ | Madrid › Ciudad Lineal | 1 |
| Bois de Madrid (60) ⚠️ | Madrid › Ciudad Lineal | 1 |
| Parc de Madrid (642) ⚠️ | Madrid › Ciudad Lineal | 1 |
| Parc de Guadarrama (12) ⚠️ | Guadarrama | 1 |
| Parque de la Botellera ⚠️ | Fuenlabrada | 1 |
| Parc de Serranillos del Valle (2) ⚠️ | Serranillos del Valle | 1 |
| Parc de Serranillos del Valle (3) ⚠️ | Serranillos del Valle | 1 |
| Bois de Batres (6) ⚠️ | Batres | 1 |
| Parc de Madrid (647) ⚠️ | Madrid › Ciudad Lineal | 1 |
| Parc de Rivas-Vaciamadrid (18) ⚠️ | Rivas-Vaciamadrid | 1 |
| Parc de Getafe (37) ⚠️ | Getafe | 1 |
| Plaza de Las Meninas ⚠️ | Madrid › Carabanchel | 1 |
| Plaza de Hacienda ⚠️ | Madrid › Villa de Vallecas | 1 |
| Parc de Boadilla del Monte (28) ⚠️ | Boadilla del Monte | 1 |
| Parc de Boadilla del Monte (34) ⚠️ | Boadilla del Monte | 1 |
| Forêt de Alcalá de Henares (3) ⚠️ | Alcalá de Henares | 1 |
| Parc de Madrid (668) ⚠️ | Madrid › Usera | 1 |
| Parc de Alcalá de Henares (21) ⚠️ | Alcalá de Henares | 1 |
| Parc de Madrid (684) ⚠️ | Madrid › Villaverde | 1 |
| Parc de Getafe (38) ⚠️ | Getafe | 1 |
| Parc de Madrid (687) ⚠️ | Madrid › Latina | 1 |
| Plaza de la Constitución (3) ⚠️ | Madrid › Puente de Vallecas | 1 |
| Parc de Colmenarejo (6) ⚠️ | Colmenarejo | 1 |
| Forêt de Madrid (64) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Forêt de Piñuécar-Gandullas (2) ⚠️ | Piñuécar-Gandullas | 1 |
| Forêt de Piñuécar-Gandullas (7) ⚠️ | Piñuécar-Gandullas | 1 |
| Parc de Madrid (717) ⚠️ | Madrid › Villaverde | 1 |
| Parque Lavadero ⚠️ | El Berrueco | 1 |
| Forêt de Galapagar (7) ⚠️ | Galapagar | 1 |
| Forêt de Alcobendas (4) ⚠️ | Alcobendas | 1 |
| Bois de Madrid (64) ⚠️ | Madrid › Retiro | 1 |
| Forêt de Madrid (66) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Forêt de Madrid (68) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Forêt de Buitrago del Lozoya (2) ⚠️ | Buitrago del Lozoya | 1 |
| Parc de Madrid (726) ⚠️ | Madrid › Villaverde | 1 |
| Piscina Urbanización Montesoro ⚠️ | Algete | 1 |
| Parque Urbanización Montesoro ⚠️ | Algete | 1 |
| Parc de Coslada (10) ⚠️ | Coslada | 1 |
| Parc de Collado Villalba (6) ⚠️ | Collado Villalba | 1 |
| Forêt de Rivas-Vaciamadrid (34) ⚠️ | Rivas-Vaciamadrid | 1 |
| Forêt de Pozuelo del Rey (3) ⚠️ | Pozuelo del Rey | 1 |
| Parc de Pozuelo de Alarcón (35) ⚠️ | Pozuelo de Alarcón | 1 |
| Parc de Alcalá de Henares (24) ⚠️ | Alcalá de Henares | 1 |
| Forêt de Corpa (7) ⚠️ | Corpa | 1 |
| Bois de Moralzarzal (3) ⚠️ | Moralzarzal | 1 |
| Parc de Alcalá de Henares (28) ⚠️ | Alcalá de Henares | 1 |
| Bois de Valverde de Alcalá (3) ⚠️ | Valverde de Alcalá | 1 |
| Bois de Valverde de Alcalá (8) ⚠️ | Valverde de Alcalá | 1 |
| Bois de Valverde de Alcalá (9) ⚠️ | Valverde de Alcalá | 1 |
| Bois de Valverde de Alcalá (10) ⚠️ | Valverde de Alcalá | 1 |
| Bois de Valverde de Alcalá (15) ⚠️ | Valverde de Alcalá | 1 |
| Bois de Valverde de Alcalá (18) ⚠️ | Valverde de Alcalá | 1 |
| Forêt de Piñuécar-Gandullas (8) ⚠️ | Piñuécar-Gandullas | 1 |
| Forêt de La Serna del Monte ⚠️ | La Serna del Monte | 1 |
| Parc de Villanueva de la Cañada (24) ⚠️ | Villanueva de la Cañada | 1 |
| Forêt de Rivas-Vaciamadrid (36) ⚠️ | Rivas-Vaciamadrid | 1 |
| Parc de Leganés (20) ⚠️ | Leganés | 1 |
| Parc de Leganés (21) ⚠️ | Leganés | 1 |
| Parc de Leganés (22) ⚠️ | Leganés | 1 |
| Parc de Leganés (31) ⚠️ | Leganés | 1 |
| Parc de Leganés (41) ⚠️ | Leganés | 1 |
| Forêt de Las Rozas de Madrid (6) ⚠️ | Las Rozas de Madrid | 1 |
| Dalieda de San Francisco ⚠️ | Madrid › Centro | 1 |
| Forêt de San Fernando de Henares (17) ⚠️ | San Fernando de Henares | 1 |
| Bois de San Fernando de Henares (9) ⚠️ | San Fernando de Henares | 1 |
| Parque del Depósito ⚠️ | Getafe | 1 |
| Parc de Aranjuez (9) ⚠️ | Aranjuez | 1 |
| Parc de Madrid (744) ⚠️ | Madrid › Tetuán | 1 |
| Parc de Aranjuez (15) ⚠️ | Aranjuez | 1 |
| Parque Gabriela Mistral ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parque Pedro Ruiz de León Gómez-Zurdo ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parque Pedro Ruiz de León Gómez-Zurdo (2) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parque Gabriela Mistral (2) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parque Pedro Ruiz de León Gómez-Zurdo (3) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parc de Madrid (750) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parc de Madrid (751) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parc de Madrid (752) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parc de Madrid (763) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parque Río Guadalix ⚠️ | San Agustín del Guadalix | 1 |
| Parque Asturias ⚠️ | Collado Villalba | 1 |
| Bois de Redueña (16) ⚠️ | Redueña | 1 |
| Bois de Redueña (17) ⚠️ | Redueña | 1 |
| Plaza de la Unión Cárcavas-San Antonio ⚠️ | Madrid › Hortaleza | 1 |
| Parc de Aranjuez (24) ⚠️ | Aranjuez | 1 |
| Parc de Madrid (780) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| 2 de Mayo ⚠️ | Loeches | 1 |
| Parc de Loeches (3) ⚠️ | Loeches | 1 |
| Parc de Madrid (782) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parque de las Siete Leguas. ⚠️ | Tres Cantos | 1 |
| Plaza del Cine París ⚠️ | Madrid › Puente de Vallecas | 1 |
| Forêt de San Martín de la Vega (14) ⚠️ | San Martín de la Vega | 1 |
| Forêt de San Martín de la Vega (18) ⚠️ | San Martín de la Vega | 1 |
| Forêt de San Martín de la Vega (19) ⚠️ | San Martín de la Vega | 1 |
| Forêt de San Martín de la Vega (20) ⚠️ | San Martín de la Vega | 1 |
| Forêt de San Martín de la Vega (21) ⚠️ | San Martín de la Vega | 1 |
| Parc de Madrid (794) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parc de Madrid (798) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parque Santiago Apóstol ⚠️ | Torrejón de Ardoz | 1 |
| Parque Santa Barbara ⚠️ | Sevilla la Nueva | 1 |
| Parc de Casarrubuelos (8) ⚠️ | Casarrubuelos | 1 |
| Parque Miralrío ⚠️ | Rivas-Vaciamadrid | 1 |
| Forêt de San Fernando de Henares (20) ⚠️ | San Fernando de Henares | 1 |
| Parc de Colmenar Viejo (22) ⚠️ | Colmenar Viejo | 1 |
| Parque Federico García Lorca ⚠️ | Algete | 1 |
| Parque Las Fuentes ⚠️ | Algete | 1 |
| Parc de San Sebastián de los Reyes (17) ⚠️ | San Sebastián de los Reyes | 1 |
| Parque Calle Poeta Rafael Morales ⚠️ | San Sebastián de los Reyes | 1 |
| Parc de San Sebastián de los Reyes (20) ⚠️ | San Sebastián de los Reyes | 1 |
| Parc de San Sebastián de los Reyes (25) ⚠️ | San Sebastián de los Reyes | 1 |
| Parc de Madrid (805) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parque de las Laderas de Santa Elena ⚠️ | San Martín de la Vega | 1 |
| Parc de Boadilla del Monte (40) ⚠️ | Boadilla del Monte | 1 |
| leocerio ⚠️ | San Martín de la Vega | 1 |
| Bois de Valdemoro (4) ⚠️ | Valdemoro | 1 |
| Parc de Torrejón de Ardoz (26) ⚠️ | Torrejón de Ardoz | 1 |
| Parc de Villanueva de la Cañada (30) ⚠️ | Villanueva de la Cañada | 1 |
| Parc de Torrejón de Ardoz (29) ⚠️ | Torrejón de Ardoz | 1 |
| Jardines del Instituto Santamarca ⚠️ | Madrid › Chamartín | 1 |
| Parc de Navalcarnero (12) ⚠️ | Navalcarnero | 1 |
| Parc de Sevilla la Nueva (2) ⚠️ | Sevilla la Nueva | 1 |
| Parque El Encinar ⚠️ | Sevilla la Nueva | 1 |
| Parque Carlos Sainz ⚠️ | Pozuelo de Alarcón | 1 |
| Parc de Madrid (814) ⚠️ | Madrid › Arganzuela | 1 |
| Bois de San Fernando de Henares (13) ⚠️ | San Fernando de Henares | 1 |
| Parc de San Sebastián de los Reyes (60) ⚠️ | San Sebastián de los Reyes | 1 |
| Pradera ⚠️ | Villanueva de la Cañada | 1 |
| Forêt de Boadilla del Monte (6) ⚠️ | Boadilla del Monte | 1 |
| Parc de San Sebastián de los Reyes (68) ⚠️ | San Sebastián de los Reyes | 1 |
| Parc de San Sebastián de los Reyes (69) ⚠️ | San Sebastián de los Reyes | 1 |
| Plaza de Argüelles ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parc de San Sebastián de los Reyes (79) ⚠️ | San Sebastián de los Reyes | 1 |
| Parque Av Comunidad de Madrid ⚠️ | San Martín de la Vega | 1 |
| Parc de San Sebastián de los Reyes (90) ⚠️ | San Sebastián de los Reyes | 1 |
| Parc de Pozuelo de Alarcón (47) ⚠️ | Pozuelo de Alarcón | 1 |
| Forêt de Getafe (4) ⚠️ | Getafe | 1 |
| Parc de Pozuelo de Alarcón (51) ⚠️ | Pozuelo de Alarcón | 1 |
| Parc de Alcobendas (82) ⚠️ | Alcobendas | 1 |
| Parc de Alcobendas (85) ⚠️ | Alcobendas | 1 |
| Parc de San Sebastián de los Reyes (95) ⚠️ | San Sebastián de los Reyes | 1 |
| Parc de San Sebastián de los Reyes (103) ⚠️ | San Sebastián de los Reyes | 1 |
| Parc de Pozuelo de Alarcón (60) ⚠️ | Pozuelo de Alarcón | 1 |
| Parc de Pinto (26) ⚠️ | Pinto | 1 |
| Parc de Pinto (27) ⚠️ | Pinto | 1 |
| Parc de Madrid (846) ⚠️ | Madrid › Villaverde | 1 |
| Parque Darwin (5) ⚠️ | Alcorcón | 1 |
| Parc de Madrid (851) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Forêt de Colmenar Viejo (3) ⚠️ | Colmenar Viejo | 1 |
| Parc de Madrid (857) ⚠️ | Madrid › Usera | 1 |
| Parc de Alcorcón (37) ⚠️ | Alcorcón | 1 |
| Parc de Madrid (858) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parc de Alcalá de Henares (38) ⚠️ | Alcalá de Henares | 1 |
| Parc de Alcorcón (42) ⚠️ | Alcorcón | 1 |
| Bois de Redueña (32) ⚠️ | Redueña | 1 |
| Bois de Torrelaguna (8) ⚠️ | Torrelaguna | 1 |
| Bois de Torrelaguna (10) ⚠️ | Torrelaguna | 1 |
| Forêt de Alcalá de Henares (10) ⚠️ | Alcalá de Henares | 1 |
| Forêt de Alcalá de Henares (12) ⚠️ | Alcalá de Henares | 1 |
| Parc de Algete (23) ⚠️ | Algete | 1 |
| Parc de Tielmes ⚠️ | Tielmes | 1 |
| Parc de Algete (26) ⚠️ | Algete | 1 |
| Forêt de Algete (2) ⚠️ | Algete | 1 |
| Parc de Algete (27) ⚠️ | Algete | 1 |
| Forêt de Alcalá de Henares (17) ⚠️ | Alcalá de Henares | 1 |
| Parc de Madrid (863) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Paseo Mar del Norte ⚠️ | Coslada | 1 |
| Bois de Pozuelo de Alarcón (10) ⚠️ | Pozuelo de Alarcón | 1 |
| Bois de Pozuelo de Alarcón (11) ⚠️ | Pozuelo de Alarcón | 1 |
| Parque de la Llave de Coslada (2) ⚠️ | Coslada | 1 |
| El Pinar de Colmenar ⚠️ | Colmenar del Arroyo | 1 |
| Forêt de El Boalo-Cerceda-Mataelpino (4) ⚠️ | El Boalo-Cerceda-Mataelpino | 1 |
| Parc de Madrid (875) ⚠️ | Madrid › Centro | 1 |
| Forêt de Manzanares el Real (6) ⚠️ | Manzanares el Real | 1 |
| Jardín de la Luz ⚠️ | Madrid › Villaverde | 1 |
| Parque El Cano ⚠️ | Boadilla del Monte | 1 |
| Parque de la avenida de europa II ⚠️ | Arroyomolinos | 1 |
| Parque del Rio Tajo I ⚠️ | Arroyomolinos | 1 |
| Parque Vista Real ⚠️ | Móstoles | 1 |
| Parque Virgen de Pilar ⚠️ | Boadilla del Monte | 1 |
| Parc de Madrid (879) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parc de Boadilla del Monte (47) ⚠️ | Boadilla del Monte | 1 |
| Parc de Boadilla del Monte (49) ⚠️ | Boadilla del Monte | 1 |
| Parc de Alpedrete (5) ⚠️ | Alpedrete | 1 |
| Parc de Meco (4) ⚠️ | Meco | 1 |
| Parque Senda de la Plata ⚠️ | Meco | 1 |
| Parc de Madrid (883) ⚠️ | Madrid › San Blas - Canillejas | 1 |
| Forêt de Meco (2) ⚠️ | Meco | 1 |
| Bois de Meco ⚠️ | Meco | 1 |
| Bois de Meco (2) ⚠️ | Meco | 1 |
| Parque Calle de Alicante ⚠️ | Arroyomolinos | 1 |
| Parc de Los Molinos (2) ⚠️ | Los Molinos | 1 |
| Parc de Meco (8) ⚠️ | Meco | 1 |
| Parc de Alcalá de Henares (41) ⚠️ | Alcalá de Henares | 1 |
| Parc de Torrejón de la Calzada (4) ⚠️ | Torrejón de la Calzada | 1 |
| Parc de Torrejón de la Calzada (10) ⚠️ | Torrejón de la Calzada | 1 |
| Parc de Velilla de San Antonio (15) ⚠️ | Velilla de San Antonio | 1 |
| Bois de Manzanares el Real (6) ⚠️ | Manzanares el Real | 1 |
| Bois de Manzanares el Real (9) ⚠️ | Manzanares el Real | 1 |
| Bois de Manzanares el Real (10) ⚠️ | Manzanares el Real | 1 |
| Bois de Manzanares el Real (12) ⚠️ | Manzanares el Real | 1 |
| Bois de Navacerrada (9) ⚠️ | Navacerrada | 1 |
| Parc de Getafe (68) ⚠️ | Getafe | 1 |
| Parc de Getafe (70) ⚠️ | Getafe | 1 |
| Parc de Móstoles (110) ⚠️ | Móstoles | 1 |
| Plaza de la Paloma ⚠️ | Aranjuez | 1 |
| Pinar de Cables ⚠️ | Aranjuez | 1 |
| Plaza del Gorrion ⚠️ | Aranjuez | 1 |
| Recinto Ferial El Vaillo ⚠️ | Villaviciosa de Odón | 1 |
| Bulevar Sur ⚠️ | Parla | 1 |
| Parc de Ciempozuelos (9) ⚠️ | Ciempozuelos | 1 |
| Parte de atras del campo de futbol ⚠️ | San Martín de la Vega | 1 |
| Parque 1º de Mayo ⚠️ | Guadalix de la Sierra | 1 |
| Parc de Madrid (899) ⚠️ | Madrid › Puente de Vallecas | 1 |
| Parc de Alcalá de Henares (43) ⚠️ | Alcalá de Henares | 1 |
| Parc de Madrid (907) ⚠️ | Madrid › Puente de Vallecas | 1 |
| Jardín de Carlos Matallanas ⚠️ | Madrid › Latina | 1 |
| Parque Gloria Fuertes ⚠️ | Torrejón de Ardoz | 1 |
| Parc de Madrid (917) ⚠️ | Madrid › Latina | 1 |
| Parc de Madrid (920) ⚠️ | Madrid › Latina | 1 |
| Parque Caleruega ⚠️ | Madrid › Ciudad Lineal | 1 |
| Parque Santa María del Pinar ⚠️ | Madrid › Ciudad Lineal | 1 |
| Parc de Madrid (930) ⚠️ | Madrid › Hortaleza | 1 |
| Parque público Los Jarales ⚠️ | Las Rozas de Madrid | 1 |
| Parque de la Supermanzana ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parque Vista Alegre ⚠️ | Pozuelo de Alarcón | 1 |
| Plaza Valencia ⚠️ | Móstoles | 1 |
| Parc de Serranillos del Valle (4) ⚠️ | Serranillos del Valle | 1 |
| Parc de Madrid (944) ⚠️ | Madrid › Carabanchel | 1 |
| Parc de Leganés (63) ⚠️ | Leganés | 1 |
| Parc de Madrid (955) ⚠️ | Madrid › Latina | 1 |
| Bois de Boadilla del Monte (2) ⚠️ | Boadilla del Monte | 1 |
| Parque Doctor Fleming ⚠️ | Coslada | 1 |
| Parc de Alcalá de Henares (45) ⚠️ | Alcalá de Henares | 1 |
| Parque Viñuelas ⚠️ | Tres Cantos | 1 |
| Parque de juegos Rayo Vallecano ⚠️ | Madrid › Villa de Vallecas | 1 |
| Parc de Madrid (958) ⚠️ | Madrid › Villa de Vallecas | 1 |
| Parc de Madrid (959) ⚠️ | Madrid › Chamartín | 1 |
| Parc de Coslada (14) ⚠️ | Coslada | 1 |
| Parque Reap ⚠️ | Collado Villalba | 1 |
| Parc de Colmenar Viejo (26) ⚠️ | Colmenar Viejo | 1 |
| Parc de Colmenar Viejo (28) ⚠️ | Colmenar Viejo | 1 |
| Parc de Madrid (962) ⚠️ | Madrid › Carabanchel | 1 |
| Parc de Torrejón de Ardoz (32) ⚠️ | Torrejón de Ardoz | 1 |
| Parc de Madrid (965) ⚠️ | Madrid › Carabanchel | 1 |
| Parc de Madrid (977) ⚠️ | Madrid › Usera | 1 |
| Parc de Majadahonda (9) ⚠️ | Majadahonda | 1 |
| Parque del Solitario ⚠️ | Paracuellos de Jarama | 1 |
| Parc de Paracuellos de Jarama (11) ⚠️ | Paracuellos de Jarama | 1 |
| Parc de Paracuellos de Jarama (12) ⚠️ | Paracuellos de Jarama | 1 |
| Parc de Paracuellos de Jarama (15) ⚠️ | Paracuellos de Jarama | 1 |
| Parc de Paracuellos de Jarama (21) ⚠️ | Paracuellos de Jarama | 1 |
| Parc de Paracuellos de Jarama (23) ⚠️ | Paracuellos de Jarama | 1 |
| Parc de Paracuellos de Jarama (33) ⚠️ | Paracuellos de Jarama | 1 |
| Parc de Paracuellos de Jarama (40) ⚠️ | Paracuellos de Jarama | 1 |
| Parc de Paracuellos de Jarama (42) ⚠️ | Paracuellos de Jarama | 1 |
| Parc de Paracuellos de Jarama (54) ⚠️ | Paracuellos de Jarama | 1 |
| Parc de Paracuellos de Jarama (55) ⚠️ | Paracuellos de Jarama | 1 |
| Camino entre Torreon y el Instituto ⚠️ | Arroyomolinos | 1 |
| Parque del Ancla (2) ⚠️ | Colmenar Viejo | 1 |
| Parque de La Coruña (2) ⚠️ | Collado Villalba | 1 |
| Parc de Madrid (994) ⚠️ | Madrid › Latina | 1 |
| Parc de Rivas-Vaciamadrid (36) ⚠️ | Rivas-Vaciamadrid | 1 |
| Parc de Rivas-Vaciamadrid (37) ⚠️ | Rivas-Vaciamadrid | 1 |
| Parc de Rivas-Vaciamadrid (41) ⚠️ | Rivas-Vaciamadrid | 1 |
| Forêt de Rivas-Vaciamadrid (40) ⚠️ | Rivas-Vaciamadrid | 1 |
| Forêt de Rivas-Vaciamadrid (41) ⚠️ | Rivas-Vaciamadrid | 1 |
| Parc de Alpedrete (7) ⚠️ | Alpedrete | 1 |
| Parc de Boadilla del Monte (55) ⚠️ | Boadilla del Monte | 1 |
| Arqueopinto. Parque de la Prehistoria en Madrid ⚠️ | Pinto | 1 |
| Parc de El Álamo (3) ⚠️ | El Álamo | 1 |
| Parc de Getafe (77) ⚠️ | Getafe | 1 |
| Parc de Getafe (80) ⚠️ | Getafe | 1 |
| Parc de Getafe (81) ⚠️ | Getafe | 1 |
| Parc de Getafe (82) ⚠️ | Getafe | 1 |
| Parc de Getafe (83) ⚠️ | Getafe | 1 |
| Parc de Colmenar Viejo (41) ⚠️ | Colmenar Viejo | 1 |
| Parque Adolfo Bollaín ⚠️ | Colmenar Viejo | 1 |
| Parc de Colmenar Viejo (46) ⚠️ | Colmenar Viejo | 1 |
| Parc de Las Rozas de Madrid (39) ⚠️ | Las Rozas de Madrid | 1 |
| Parc de Alcorcón (50) ⚠️ | Alcorcón | 1 |
| Bois de Los Santos de la Humosa ⚠️ | Los Santos de la Humosa | 1 |
| Bois de Los Santos de la Humosa (6) ⚠️ | Los Santos de la Humosa | 1 |
| Parque Chirivita ⚠️ | Madrid › Carabanchel | 1 |
| Parc de Majadahonda (11) ⚠️ | Majadahonda | 1 |
| Parque Dr. Alejandro Vallejo Hierro ⚠️ | Pinto | 1 |
| parque velilla arena ⚠️ | Velilla de San Antonio | 1 |
| Parque ferial La poveda ⚠️ | Arganda del Rey | 1 |
| Parc de Madrid (1029) ⚠️ | Madrid › Usera | 1 |
| Parque Calle de Alicante II ⚠️ | Arroyomolinos | 1 |
| Parc de Arroyomolinos (6) ⚠️ | Arroyomolinos | 1 |
| Parc de Madrid (1035) ⚠️ | Madrid › Hortaleza | 1 |
| Parque Fernando Mugica ⚠️ | Getafe | 1 |
| Parc de Madrid (1036) ⚠️ | Madrid › Hortaleza | 1 |
| Parc de Pozuelo de Alarcón (93) ⚠️ | Pozuelo de Alarcón | 1 |
| Parc de San Lorenzo de El Escorial (12) ⚠️ | San Lorenzo de El Escorial | 1 |
| Bois de Coslada (4) ⚠️ | Coslada | 1 |
| Parc de Madrid (1038) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parc de El Berrueco ⚠️ | El Berrueco | 1 |
| Parc de Alcorcón (52) ⚠️ | Alcorcón | 1 |
| Parc de Madrid (1045) ⚠️ | Madrid › Barajas | 1 |
| Parc de Coslada (19) ⚠️ | Coslada | 1 |
| Jardín Los Arcos ⚠️ | Colmenar Viejo | 1 |
| Parc de Madrid (1049) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parque de los Girasoles (3) ⚠️ | Torrejón de Ardoz | 1 |
| Parque Foresta ⚠️ | Tres Cantos | 1 |
| Parc de Mejorada del Campo (17) ⚠️ | Mejorada del Campo | 1 |
| Parc de Mejorada del Campo (20) ⚠️ | Mejorada del Campo | 1 |
| Parc de Mejorada del Campo (25) ⚠️ | Mejorada del Campo | 1 |
| Parque JH ⚠️ | Torrelodones | 1 |
| Parc de Valdemorillo (8) ⚠️ | Valdemorillo | 1 |
| Parc de Valdemorillo (14) ⚠️ | Valdemorillo | 1 |
| Parc de Valdemorillo (15) ⚠️ | Valdemorillo | 1 |
| Forêt de Valdemorillo (17) ⚠️ | Valdemorillo | 1 |
| Forêt de Valdemorillo (24) ⚠️ | Valdemorillo | 1 |
| Forêt de Valdemorillo (25) ⚠️ | Valdemorillo | 1 |
| Forêt de Valdemorillo (33) ⚠️ | Valdemorillo | 1 |
| Forêt de Valdemorillo (36) ⚠️ | Valdemorillo | 1 |
| Parque Abraham Quintanilla ⚠️ | Morata de Tajuña | 1 |
| Forêt de Valdemorillo (43) ⚠️ | Valdemorillo | 1 |
| Forêt de Alpedrete (3) ⚠️ | Alpedrete | 1 |
| Parque Forestal Mirador Del Nacedero ⚠️ | Boadilla del Monte | 1 |
| Parc de Pedrezuela ⚠️ | Pedrezuela | 1 |
| Parc de El Molar ⚠️ | El Molar | 1 |
| Forêt de Valdemorillo (48) ⚠️ | Navalagamella | 1 |
| Forêt de Navalagamella (12) ⚠️ | Navalagamella | 1 |
| Forêt de Navalagamella (13) ⚠️ | Navalagamella | 1 |
| Parc de Madrid (1057) ⚠️ | Madrid › Chamartín | 1 |
| Parque Félix Cimas ⚠️ | San Agustín del Guadalix | 1 |
| Parc de Pedrezuela (6) ⚠️ | Pedrezuela | 1 |
| Parc de Pedrezuela (7) ⚠️ | Pedrezuela | 1 |
| Parc de Pedrezuela (8) ⚠️ | Pedrezuela | 1 |
| Parc de Meco (21) ⚠️ | Meco | 1 |
| Parc de Meco (28) ⚠️ | Meco | 1 |
| Forêt de Rivas-Vaciamadrid (42) ⚠️ | Rivas-Vaciamadrid | 1 |
| Parc de Getafe (91) ⚠️ | Getafe | 1 |
| Forêt de Valdemorillo (61) ⚠️ | Valdemorillo | 1 |
| Parc de Rivas-Vaciamadrid (48) ⚠️ | Rivas-Vaciamadrid | 1 |
| Parque de Manoteras (3) ⚠️ | Madrid › Hortaleza | 1 |
| Forêt de Boadilla del Monte (12) ⚠️ | Boadilla del Monte | 1 |
| Parc de Arganda del Rey (23) ⚠️ | Arganda del Rey | 1 |
| Parc de Arganda del Rey (24) ⚠️ | Arganda del Rey | 1 |
| Parc de Arganda del Rey (26) ⚠️ | Arganda del Rey | 1 |
| Parc de Móstoles (117) ⚠️ | Móstoles | 1 |
| Parc de San Fernando de Henares (14) ⚠️ | San Fernando de Henares | 1 |
| Parc de San Martín de Valdeiglesias (7) ⚠️ | San Martín de Valdeiglesias | 1 |
| Parque de Pino Alto ⚠️ | Valdemorillo | 1 |
| Parc de San Martín de Valdeiglesias (15) ⚠️ | San Martín de Valdeiglesias | 1 |
| Parc de Berzosa del Lozoya ⚠️ | Berzosa del Lozoya | 1 |
| Parc de Rivas-Vaciamadrid (58) ⚠️ | Rivas-Vaciamadrid | 1 |
| Parc de Las Rozas de Madrid (42) ⚠️ | Las Rozas de Madrid | 1 |
| Rancho Chico ⚠️ | Loeches | 1 |
| Parc de Loeches (19) ⚠️ | Loeches | 1 |
| Parc de Madrid (1063) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Bois de Rivas-Vaciamadrid (19) ⚠️ | Rivas-Vaciamadrid | 1 |
| Parc de Alcorcón (64) ⚠️ | Alcorcón | 1 |
| Parc de Loeches (20) ⚠️ | Loeches | 1 |
| Parc de Torrejón de la Calzada (31) ⚠️ | Cubas de la Sagra | 1 |
| Parc de Madrid (1068) ⚠️ | Madrid › San Blas - Canillejas | 1 |
| Parc de Alpedrete (9) ⚠️ | Alpedrete | 1 |
| Parc de Getafe (92) ⚠️ | Getafe | 1 |
| Parc de Sevilla la Nueva (7) ⚠️ | Sevilla la Nueva | 1 |
| Parc de Pozuelo de Alarcón (100) ⚠️ | Pozuelo de Alarcón | 1 |
| Parc de Villanueva del Pardillo (15) ⚠️ | Villanueva del Pardillo | 1 |
| Parc de Alcorcón (66) ⚠️ | Alcorcón | 1 |
| Parc de Pozuelo de Alarcón (105) ⚠️ | Pozuelo de Alarcón | 1 |
| Zona Verde Pública (2) ⚠️ | Pozuelo de Alarcón | 1 |
| Zona Verde Pública (4) ⚠️ | Pozuelo de Alarcón | 1 |
| Parc de Rivas-Vaciamadrid (73) ⚠️ | Rivas-Vaciamadrid | 1 |
| Parque Peñalara ⚠️ | Tres Cantos | 1 |
| Parque Zafiro Azul ⚠️ | Tres Cantos | 1 |
| Parque de los antiguos patos ⚠️ | Tres Cantos | 1 |
| Paseo Sector Descubridores ⚠️ | Tres Cantos | 1 |
| Plaza Constitución ⚠️ | Tres Cantos | 1 |
| Parc de Pozuelo de Alarcón (113) ⚠️ | Pozuelo de Alarcón | 1 |
| Parc de Madrid (1077) ⚠️ | Madrid › Latina | 1 |
| Parc de Madrid (1081) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parc de Madrid (1085) ⚠️ | Madrid › Usera | 1 |
| Bois de Manzanares el Real (19) ⚠️ | Manzanares el Real | 1 |
| Bois de Manzanares el Real (20) ⚠️ | Manzanares el Real | 1 |
| Parque de Los Morrones ⚠️ | Majadahonda | 1 |
| Parque Adolfo Suárez (5) ⚠️ | Majadahonda | 1 |
| Bois de Manzanares el Real (21) ⚠️ | Manzanares el Real | 1 |
| Paseo av del parque (4) ⚠️ | Tres Cantos | 1 |
| Paseo de la Avenida de Viñuelas (2) ⚠️ | Tres Cantos | 1 |
| Parque Peña del Rayo ⚠️ | Hoyo de Manzanares | 1 |
| Parque Gurugú ⚠️ | Guadarrama | 1 |
| Parque de Santa Ana (2) ⚠️ | Alcalá de Henares | 1 |
| Parc de Madrid (1096) ⚠️ | Madrid › Puente de Vallecas | 1 |
| Forêt de Colmenar Viejo (4) ⚠️ | Colmenar Viejo | 1 |
| Parc de Boadilla del Monte (60) ⚠️ | Boadilla del Monte | 1 |
| Parc de Boadilla del Monte (73) ⚠️ | Boadilla del Monte | 1 |
| Parc de Rivas-Vaciamadrid (74) ⚠️ | Rivas-Vaciamadrid | 1 |
| Parc de Madrid (1105) ⚠️ | Madrid › Arganzuela | 1 |
| Jardines de arriba ⚠️ | Villa del Prado | 1 |
| Parque de la Retorna ⚠️ | Las Rozas de Madrid | 1 |
| Parc de Madrid (1117) ⚠️ | Madrid › Villaverde | 1 |
| Parc de Pozuelo de Alarcón (115) ⚠️ | Pozuelo de Alarcón | 1 |
| Parc de Galapagar (16) ⚠️ | Galapagar | 1 |
| Forêt de Alcalá de Henares (31) ⚠️ | Alcalá de Henares | 1 |
| Pinar de la Sacedilla ⚠️ | Majadahonda | 1 |
| Forêt de Madrid (87) ⚠️ | Madrid › Barajas | 1 |
| Forêt de Madrid (88) ⚠️ | Madrid › Barajas | 1 |
| Forêt de Madrid (95) ⚠️ | Madrid › Barajas | 1 |
| Parc de Madrid (1120) ⚠️ | Madrid › Arganzuela | 1 |
| Bois de Getafe (2) ⚠️ | Getafe | 1 |
| Parc de Boadilla del Monte (77) ⚠️ | Boadilla del Monte | 1 |
| Parc de Nuevo Baztán (2) ⚠️ | Nuevo Baztán | 1 |
| Parc de El Boalo-Cerceda-Mataelpino (5) ⚠️ | El Boalo-Cerceda-Mataelpino | 1 |
| Parc de Nuevo Baztán (29) ⚠️ | Nuevo Baztán | 1 |
| Parc de Getafe (101) ⚠️ | Getafe | 1 |
| Parc de Madrid (1128) ⚠️ | Madrid › Villaverde | 1 |
| Parc de Madrid (1129) ⚠️ | Madrid › Villaverde | 1 |
| Parc de Nuevo Baztán (32) ⚠️ | Nuevo Baztán | 1 |
| Bois de Villar del Olmo ⚠️ | Villar del Olmo | 1 |
| Parc de Nuevo Baztán (33) ⚠️ | Nuevo Baztán | 1 |
| Parc de Las Rozas de Madrid (46) ⚠️ | Las Rozas de Madrid | 1 |
| Parc de Las Rozas de Madrid (50) ⚠️ | Las Rozas de Madrid | 1 |
| Parc de Móstoles (122) ⚠️ | Móstoles | 1 |
| Forêt de Aranjuez (36) ⚠️ | Aranjuez | 1 |
| Forêt de Aranjuez (39) ⚠️ | Aranjuez | 1 |
| Forêt de Aranjuez (45) ⚠️ | Aranjuez | 1 |
| Forêt de Aranjuez (52) ⚠️ | Aranjuez | 1 |
| Forêt de Aranjuez (78) ⚠️ | Aranjuez | 1 |
| Plaza de Casto Fernández-Shaw ⚠️ | Madrid › Hortaleza | 1 |
| Parc de Madrid (1140) ⚠️ | Madrid › Villa de Vallecas | 1 |
| Parc de Madrid (1141) ⚠️ | Madrid › Villaverde | 1 |
| Parc de Madrid (1142) ⚠️ | Madrid › Villaverde | 1 |
| Parc de Madrid (1144) ⚠️ | Madrid › Villaverde | 1 |
| Parc de Madrid (1158) ⚠️ | Madrid › Moratalaz | 1 |
| Parc de Pozuelo de Alarcón (117) ⚠️ | Pozuelo de Alarcón | 1 |
| Parc de Madrid (1162) ⚠️ | Madrid › Vicálvaro | 1 |
| Parc de Madrid (1163) ⚠️ | Madrid › Vicálvaro | 1 |
| Parc de Moralzarzal (6) ⚠️ | Moralzarzal | 1 |
| Parc de Majadahonda (14) ⚠️ | Majadahonda | 1 |
| Forêt de Madrid (102) ⚠️ | Madrid › Moratalaz | 1 |
| Parque Europa (2) ⚠️ | Estremera | 1 |
| Canal Bajo de Madrid (4) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parc de Villar del Olmo (3) ⚠️ | Villar del Olmo | 1 |
| Parc de Nuevo Baztán (41) ⚠️ | Nuevo Baztán | 1 |
| Parc de Torrejón de la Calzada (36) ⚠️ | Torrejón de la Calzada | 1 |
| Parc de Madrid (1178) ⚠️ | Madrid › Puente de Vallecas | 1 |
| Parc de Torrejón de Ardoz (34) ⚠️ | Torrejón de Ardoz | 1 |
| Parc de Madrid (1190) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Bois de Villar del Olmo (2) ⚠️ | Villar del Olmo | 1 |
| Parque Vosa ⚠️ | Móstoles | 1 |
| Urbanización Los Monteros ⚠️ | El Escorial | 1 |
| Forêt de Madrid (115) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Forêt de Madrid (116) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Forêt de Madrid (117) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parc de Collado Villalba (13) ⚠️ | Collado Villalba | 1 |
| Forêt de Madrid (122) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Forêt de Madrid (123) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parque de las Eras (2) ⚠️ | Guadalix de la Sierra | 1 |
| Plaza de La Paloma ⚠️ | Parla | 1 |
| Forêt de Talamanca de Jarama (2) ⚠️ | Talamanca de Jarama | 1 |
| Forêt de Madrid (136) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Forêt de Madrid (148) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Forêt de Valdemoro (3) ⚠️ | Valdemoro | 1 |
| Bois de Rascafría ⚠️ | Rascafría | 1 |
| Parc de Collado Villalba (25) ⚠️ | Collado Villalba | 1 |
| Parc de Madrid (1198) ⚠️ | Madrid › Ciudad Lineal | 1 |
| Bois de Madrid (78) ⚠️ | Madrid › Hortaleza | 1 |
| Bois de Madrid (79) ⚠️ | Madrid › Hortaleza | 1 |
| Forêt de Alcalá de Henares (35) ⚠️ | Alcalá de Henares | 1 |
| Parc de Rivas-Vaciamadrid (79) ⚠️ | Rivas-Vaciamadrid | 1 |
| Parque de la Reguerilla ⚠️ | Fresno de Torote | 1 |
| Forêt de Madrid (159) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Forêt de Guadarrama (4) ⚠️ | Guadarrama | 1 |
| Forêt de Guadarrama (9) ⚠️ | Guadarrama | 1 |
| Bois de San Lorenzo de El Escorial (2) ⚠️ | San Lorenzo de El Escorial | 1 |
| Parc de Alcalá de Henares (52) ⚠️ | Alcalá de Henares | 1 |
| Parc de Rivas-Vaciamadrid (84) ⚠️ | Rivas-Vaciamadrid | 1 |
| Parc de Madrid (1209) ⚠️ | Madrid › Carabanchel | 1 |
| Parc de Madrid (1219) ⚠️ | Madrid › Puente de Vallecas | 1 |
| Parc de Leganés (72) ⚠️ | Leganés | 1 |
| Parc de Madrid (1220) ⚠️ | Madrid › Villaverde | 1 |
| Parc de Madrid (1221) ⚠️ | Madrid › Villaverde | 1 |
| Parc de Leganés (78) ⚠️ | Leganés | 1 |
| Forêt de Getafe (6) ⚠️ | Getafe | 1 |
| Forêt de Fuenlabrada ⚠️ | Fuenlabrada | 1 |
| Parc de Getafe (141) ⚠️ | Getafe | 1 |
| Parc de Getafe (144) ⚠️ | Getafe | 1 |
| Forêt de Madrid (166) ⚠️ | Madrid › Tetuán | 1 |
| Parque Camino del Olivo ⚠️ | Meco | 1 |
| Parc de Meco (31) ⚠️ | Meco | 1 |
| Forêt de Las Rozas de Madrid (8) ⚠️ | Las Rozas de Madrid | 1 |
| Parc de Majadahonda (15) ⚠️ | Majadahonda | 1 |
| Parque Municipal Calle Siroco ⚠️ | Pozuelo de Alarcón | 1 |
| Zona Verde Pública (7) ⚠️ | Pozuelo de Alarcón | 1 |
| Parque Valle de la Oliva ⚠️ | Majadahonda | 1 |
| Parc de Pozuelo de Alarcón (125) ⚠️ | Pozuelo de Alarcón | 1 |
| Forêt de San Fernando de Henares (24) ⚠️ | San Fernando de Henares | 1 |
| La Pastrana ⚠️ | Miraflores de la Sierra | 1 |
| Forêt de Madrid (168) ⚠️ | Madrid › Latina | 1 |
| Forêt de Madrid (170) ⚠️ | Madrid › Latina | 1 |
| Parc de Getafe (145) ⚠️ | Getafe | 1 |
| Parc de Getafe (154) ⚠️ | Getafe | 1 |
| Parc de Getafe (155) ⚠️ | Getafe | 1 |
| Parc de Rivas-Vaciamadrid (85) ⚠️ | Rivas-Vaciamadrid | 1 |
| Bois de Alpedrete (2) ⚠️ | Alpedrete | 1 |
| Parc de Colmenar Viejo (53) ⚠️ | Colmenar Viejo | 1 |
| Forêt de Pezuela de las Torres (7) ⚠️ | Pezuela de las Torres | 1 |
| Forêt de Pezuela de las Torres (8) ⚠️ | Pezuela de las Torres | 1 |
| Parc de Madrid (1241) ⚠️ | Madrid › Arganzuela | 1 |
| Forêt de Alpedrete (4) ⚠️ | Alpedrete | 1 |
| Parc de San Lorenzo de El Escorial (16) ⚠️ | San Lorenzo de El Escorial | 1 |
| Parque Jesús María Rabanal "Chusmari" ⚠️ | Pinto | 1 |
| Parc de Collado Villalba (27) ⚠️ | Collado Villalba | 1 |
| Parc de Madrid (1252) ⚠️ | Madrid › Moratalaz | 1 |
| Bois de Las Rozas de Madrid (5) ⚠️ | Las Rozas de Madrid | 1 |
| Parc de Rivas-Vaciamadrid (92) ⚠️ | Rivas-Vaciamadrid | 1 |
| Parc de Rivas-Vaciamadrid (94) ⚠️ | Rivas-Vaciamadrid | 1 |
| Parc de Leganés (84) ⚠️ | Leganés | 1 |
| Forêt de El Escorial (30) ⚠️ | El Escorial | 1 |
| Parc de El Escorial (22) ⚠️ | El Escorial | 1 |
| Parc de El Escorial (25) ⚠️ | El Escorial | 1 |
| Forêt de Coslada (6) ⚠️ | Coslada | 1 |
| Parc de Madrid (1256) ⚠️ | Madrid › Chamartín | 1 |
| Bois de Madrid (89) ⚠️ | Madrid › Ciudad Lineal | 1 |
| Bois de Madrid (90) ⚠️ | Madrid › Ciudad Lineal | 1 |
| Parc de Pozuelo de Alarcón (132) ⚠️ | Pozuelo de Alarcón | 1 |
| Parc de Tres Cantos (11) ⚠️ | Tres Cantos | 1 |
| Forêt de Madrid (180) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Forêt de Madrid (181) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Forêt de Madrid (182) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Forêt de Madrid (184) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Forêt de Madrid (186) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Forêt de Madrid (187) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parc de Pozuelo de Alarcón (133) ⚠️ | Pozuelo de Alarcón | 1 |
| Parc de Rivas-Vaciamadrid (100) ⚠️ | Rivas-Vaciamadrid | 1 |
| Parc de Getafe (165) ⚠️ | Getafe | 1 |
| Parc de Rivas-Vaciamadrid (108) ⚠️ | Rivas-Vaciamadrid | 1 |
| Parc de Rivas-Vaciamadrid (110) ⚠️ | Rivas-Vaciamadrid | 1 |
| Parc de Rivas-Vaciamadrid (113) ⚠️ | Rivas-Vaciamadrid | 1 |
| Parc de Madrid (1265) ⚠️ | Madrid › Villaverde | 1 |
| Parc de Las Rozas de Madrid (63) ⚠️ | Las Rozas de Madrid | 1 |
| Parc de Somosierra (3) ⚠️ | Somosierra | 1 |
| Parc de Torrejón de Ardoz (36) ⚠️ | Torrejón de Ardoz | 1 |
| Parque El Coto ⚠️ | Aranjuez | 1 |
| Bois de Colmenar de Oreja (8) ⚠️ | Colmenar de Oreja | 1 |
| Bois de Aranjuez (6) ⚠️ | Aranjuez | 1 |
| Parc de Griñón (13) ⚠️ | Griñón | 1 |
| Bois de Titulcia (3) ⚠️ | Titulcia | 1 |
| Bois de Titulcia (4) ⚠️ | Titulcia | 1 |
| Bois de Colmenar de Oreja (9) ⚠️ | Colmenar de Oreja | 1 |
| Bois de Villaconejos (10) ⚠️ | Villaconejos | 1 |
| Bois de Villaconejos (11) ⚠️ | Villaconejos | 1 |
| Parc de Boadilla del Monte (82) ⚠️ | Boadilla del Monte | 1 |
| Parque Mary Paz Pondal ⚠️ | Boadilla del Monte | 1 |
| Forêt de Ciempozuelos ⚠️ | Ciempozuelos | 1 |
| Forêt de Somosierra (28) ⚠️ | Somosierra | 1 |
| Bois de Valdemoro (7) ⚠️ | Valdemoro | 1 |
| Parc de Pozuelo de Alarcón (139) ⚠️ | Pozuelo de Alarcón | 1 |
| Forêt de Aranjuez (143) ⚠️ | Aranjuez | 1 |
| Parc de Robledo de Chavela (3) ⚠️ | Robledo de Chavela | 1 |
| Bois de Chinchón (8) ⚠️ | Chinchón | 1 |
| Forêt de Aranjuez (153) ⚠️ | Aranjuez | 1 |
| Forêt de Aranjuez (160) ⚠️ | Aranjuez | 1 |
| Parc de Madrid (1274) ⚠️ | Madrid › Carabanchel | 1 |
| Parc de Torrejón de Ardoz (44) ⚠️ | Torrejón de Ardoz | 1 |
| Parc de El Escorial (27) ⚠️ | El Escorial | 1 |
| Forêt de Aranjuez (163) ⚠️ | Aranjuez | 1 |
| Forêt de Aranjuez (170) ⚠️ | Aranjuez | 1 |
| Parc de Torrejón de la Calzada (49) ⚠️ | Torrejón de la Calzada | 1 |
| Parc de Alcorcón (74) ⚠️ | Alcorcón | 1 |
| Parc de Madrid (1277) ⚠️ | Madrid › Moratalaz | 1 |
| Forêt de Boadilla del Monte (16) ⚠️ | Boadilla del Monte | 1 |
| Parc de Madrid (1278) ⚠️ | Madrid › Arganzuela | 1 |
| Parque Campo del Ángel ⚠️ | Alcalá de Henares | 1 |
| Bois de Navalcarnero (2) ⚠️ | Navalcarnero | 1 |
| Forêt de Alcalá de Henares (47) ⚠️ | Alcalá de Henares | 1 |
| Parc de Madrid (1280) ⚠️ | Madrid › Hortaleza | 1 |
| Parque Garena Sur ⚠️ | Alcalá de Henares | 1 |
| Parque Villalón ⚠️ | Fuenlabrada | 1 |
| Bois de San Sebastián de los Reyes (12) ⚠️ | San Sebastián de los Reyes | 1 |
| Parc de Getafe (176) ⚠️ | Getafe | 1 |
| Paseo del Stmo. Cristo de los Ultrajes ⚠️ | Valdetorres de Jarama | 1 |
| Bois de Aranjuez (11) ⚠️ | Aranjuez | 1 |
| Plaza del Barro ⚠️ | Alcalá de Henares | 1 |
| Parc de Valdetorres de Jarama (7) ⚠️ | Valdetorres de Jarama | 1 |
| Forêt de Valdetorres de Jarama (6) ⚠️ | Valdetorres de Jarama | 1 |
| Parque del Foro ⚠️ | Talamanca de Jarama | 1 |
| Parc de Alpedrete (15) ⚠️ | Alpedrete | 1 |
| Parc de Torrejón de Ardoz (48) ⚠️ | Torrejón de Ardoz | 1 |
| Bois de Alcalá de Henares (9) ⚠️ | San Fernando de Henares | 1 |
| Parc de Alpedrete (27) ⚠️ | Alpedrete | 1 |
| Parc de Torrejón de la Calzada (50) ⚠️ | Torrejón de la Calzada | 1 |
| Parc de Madrid (1292) ⚠️ | Madrid › Carabanchel | 1 |
| Forêt de Boadilla del Monte (18) ⚠️ | Boadilla del Monte | 1 |
| Parc de Boadilla del Monte (85) ⚠️ | Boadilla del Monte | 1 |
| Parc de Alpedrete (32) ⚠️ | Alpedrete | 1 |
| Bois de San Fernando de Henares (22) ⚠️ | San Fernando de Henares | 1 |
| Bois de Aranjuez (16) ⚠️ | Aranjuez | 1 |
| Bois de Aranjuez (19) ⚠️ | Aranjuez | 1 |
| Parc de Madrid (1296) ⚠️ | Madrid › Carabanchel | 1 |
| Parc de Madrid (1297) ⚠️ | Madrid › Usera | 1 |
| Parc de Madrid (1299) ⚠️ | Madrid › Usera | 1 |
| Parc de Las Rozas de Madrid (67) ⚠️ | Las Rozas de Madrid | 1 |
| Bois de Rascafría (2) ⚠️ | Rascafría | 1 |
| Bois de Las Rozas de Madrid (8) ⚠️ | Las Rozas de Madrid | 1 |
| Forêt de Madrid (200) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Bois de Buitrago del Lozoya (3) ⚠️ | Buitrago del Lozoya | 1 |
| Bois de Buitrago del Lozoya (4) ⚠️ | Buitrago del Lozoya | 1 |
| Bois de Buitrago del Lozoya (5) ⚠️ | Buitrago del Lozoya | 1 |
| Parc de Madrid (1304) ⚠️ | Madrid › Puente de Vallecas | 1 |
| Bois de Navarredonda y San Mamés ⚠️ | Navarredonda y San Mamés | 1 |
| Forêt de Rascafría (10) ⚠️ | Rascafría | 1 |
| Parc de Madrid (1308) ⚠️ | Madrid › Arganzuela | 1 |
| Bois de Madrid (97) ⚠️ | Madrid › Arganzuela | 1 |
| Parc de Madrid (1310) ⚠️ | Madrid › Arganzuela | 1 |
| Parc de Getafe (186) ⚠️ | Getafe | 1 |
| Parque de la Cartuja ⚠️ | Talamanca de Jarama | 1 |
| Parque Lisboa ⚠️ | Getafe | 1 |
| Parc de Villaviciosa de Odón (15) ⚠️ | Villaviciosa de Odón | 1 |
| Parc de Villaviciosa de Odón (16) ⚠️ | Villaviciosa de Odón | 1 |
| Parque Huerta de Talabares ⚠️ | San Lorenzo de El Escorial | 1 |
| Parc de Madrid (1312) ⚠️ | Madrid › Puente de Vallecas | 1 |
| Parc de Getafe (192) ⚠️ | Getafe | 1 |
| Parc de Madrid (1329) ⚠️ | Madrid › Barajas | 1 |
| Triángulo de la Parra ⚠️ | Alpedrete | 1 |
| Parc de Velilla de San Antonio (21) ⚠️ | Velilla de San Antonio | 1 |
| Bois de Las Rozas de Madrid (11) ⚠️ | Las Rozas de Madrid | 1 |
| Bois de Las Rozas de Madrid (13) ⚠️ | Las Rozas de Madrid | 1 |
| Bois de Las Rozas de Madrid (17) ⚠️ | Las Rozas de Madrid | 1 |
| Bois de Las Rozas de Madrid (32) ⚠️ | Las Rozas de Madrid | 1 |
| Bois de Las Rozas de Madrid (33) ⚠️ | Las Rozas de Madrid | 1 |
| Parc de Moralzarzal (9) ⚠️ | Moralzarzal | 1 |
| Parc de Moralzarzal (10) ⚠️ | Moralzarzal | 1 |
| Bois de Coslada (23) ⚠️ | Coslada | 1 |
| Parc de Fuenlabrada (108) ⚠️ | Fuenlabrada | 1 |
| Parc de Madrid (1351) ⚠️ | Madrid › Arganzuela | 1 |
| Parc de Madrid (1353) ⚠️ | Madrid › Carabanchel | 1 |
| Parc de Colmenar del Arroyo (3) ⚠️ | Colmenar del Arroyo | 1 |
| Parc de Colmenar del Arroyo (9) ⚠️ | Colmenar del Arroyo | 1 |
| Parc de Madrid (1356) ⚠️ | Madrid › Moratalaz | 1 |
| Parc de Madrid (1357) ⚠️ | Madrid › Moratalaz | 1 |
| Parc de Colmenar del Arroyo (13) ⚠️ | Colmenar del Arroyo | 1 |
| Zona verde miradores de C. Arroyo ⚠️ | Colmenar del Arroyo | 1 |
| Parque Albert Einstein ⚠️ | San Fernando de Henares | 1 |
| Parc de Colmenar Viejo (55) ⚠️ | Colmenar Viejo | 1 |
| Parc de Villaviciosa de Odón (20) ⚠️ | Villaviciosa de Odón | 1 |
| Forêt de Titulcia ⚠️ | Titulcia | 1 |
| Forêt de Titulcia (3) ⚠️ | Titulcia | 1 |
| Parque Isla de Tarifa ⚠️ | Boadilla del Monte | 1 |
| Forêt de Madrid (208) ⚠️ | Madrid › Moncloa-Aravaca | 1 |
| Parc de Madrid (1393) ⚠️ | Madrid › San Blas - Canillejas | 1 |
| Bois de Aranjuez (22) ⚠️ | Aranjuez | 1 |
| La Boticaria (2) ⚠️ | Aranjuez | 1 |
| El Soto ⚠️ | Aranjuez | 1 |
| Bois de Aranjuez (32) ⚠️ | Aranjuez | 1 |
| Parc de Madrid (1405) ⚠️ | Madrid › Usera | 1 |
| Bois de Madrid (113) ⚠️ | Madrid › Hortaleza | 1 |
| Parque Municipal "El Plantio" ⚠️ | Daganzo de Arriba | 1 |
| Parc de Las Rozas de Madrid (76) ⚠️ | Las Rozas de Madrid | 1 |
| Parc de Alcorcón (87) ⚠️ | Alcorcón | 1 |
| Parque Craqdi (2) ⚠️ | San Sebastián de los Reyes | 1 |
| Parc de Colmenar Viejo (58) ⚠️ | Colmenar Viejo | 1 |
| Parque de Fuente Santa ⚠️ | Colmenar Viejo | 1 |
| Parc de Madrid (1413) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Forêt de Madrid (212) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Forêt de Madrid (214) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Forêt de Madrid (218) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Forêt de Madrid (227) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parc de Rivas-Vaciamadrid (125) ⚠️ | Rivas-Vaciamadrid | 1 |
| Parc de Alcalá de Henares (58) ⚠️ | Alcalá de Henares | 1 |
| Forêt de Paracuellos de Jarama (7) ⚠️ | Paracuellos de Jarama | 1 |
| Parc de Villavieja del Lozoya ⚠️ | Villavieja del Lozoya | 1 |
| Bois de Paracuellos de Jarama (8) ⚠️ | Paracuellos de Jarama | 1 |
| Bois de Leganés ⚠️ | Leganés | 1 |
| Forêt de Madrid (229) ⚠️ | Madrid › Hortaleza | 1 |
| Forêt de Madrid (230) ⚠️ | Madrid › Hortaleza | 1 |
| Parc de Villamantilla (3) ⚠️ | Villamantilla | 1 |
| Parque Arroyo ⚠️ | Villamantilla | 1 |
| Parc de San Sebastián de los Reyes (116) ⚠️ | San Sebastián de los Reyes | 1 |
| Bois de Villamantilla (11) ⚠️ | Villamantilla | 1 |
| Bois de Villamantilla (12) ⚠️ | Villamantilla | 1 |
| Bois de Villamantilla (16) ⚠️ | Villamantilla | 1 |
| Bois de Villamantilla (17) ⚠️ | Villamantilla | 1 |
| Parc de Rascafría ⚠️ | Rascafría | 1 |
| Bois de Villamanta (6) ⚠️ | Villamanta | 1 |
| Bois de Villamantilla (20) ⚠️ | Villanueva de Perales | 1 |
| Parc de Villanueva de Perales (5) ⚠️ | Villanueva de Perales | 1 |
| Bois de Chapinería ⚠️ | Chapinería | 1 |
| Bois de Chapinería (2) ⚠️ | Chapinería | 1 |
| Bois de Chapinería (4) ⚠️ | Chapinería | 1 |
| Bois de Chapinería (5) ⚠️ | Chapinería | 1 |
| Forêt de Pozuelo de Alarcón (21) ⚠️ | Pozuelo de Alarcón | 1 |
| Bois de Villamanta (8) ⚠️ | Villamanta | 1 |
| Bois de Villanueva de Perales (4) ⚠️ | Villanueva de Perales | 1 |
| Bois de Villanueva de Perales (7) ⚠️ | Villanueva de Perales | 1 |
| Bois de Villanueva de Perales (10) ⚠️ | Villanueva de Perales | 1 |
| Bois de Navas del Rey (2) ⚠️ | Navas del Rey | 1 |
| Parc de Meco (33) ⚠️ | Meco | 1 |
| Forêt de Navas del Rey (4) ⚠️ | Navas del Rey | 1 |
| Forêt de Buitrago del Lozoya (9) ⚠️ | Buitrago del Lozoya | 1 |
| Parc de Rivas-Vaciamadrid (128) ⚠️ | Rivas-Vaciamadrid | 1 |
| Parque forestal ⚠️ | Villamantilla | 1 |
| Parc de Madrid (1431) ⚠️ | Madrid › Vicálvaro | 1 |
| Parc de Madrid (1432) ⚠️ | Madrid › Vicálvaro | 1 |
| Parc de Madrid (1433) ⚠️ | Madrid › Vicálvaro | 1 |
| Parc de Madrid (1434) ⚠️ | Madrid › Vicálvaro | 1 |
| Forêt de Pinto (6) ⚠️ | Pinto | 1 |
| Forêt de Madrid (233) ⚠️ | Madrid › Villa de Vallecas | 1 |
| Parc de Madrid (1452) ⚠️ | Madrid › Vicálvaro | 1 |
| Bois de Santa María de la Alameda (30) ⚠️ | Santa María de la Alameda | 1 |
| Bois de Aranjuez (36) ⚠️ | Aranjuez | 1 |
| Bois de Aranjuez (37) ⚠️ | Aranjuez | 1 |
| Parc de Villanueva de la Cañada (34) ⚠️ | Villanueva de la Cañada | 1 |
| Parc de Villanueva de la Cañada (35) ⚠️ | Villanueva de la Cañada | 1 |
| Parc de Madrid (1467) ⚠️ | Madrid › Puente de Vallecas | 1 |
| Parc de Moralzarzal (14) ⚠️ | Moralzarzal | 1 |
| Forêt de Guadarrama (16) ⚠️ | Guadarrama | 1 |
| Bois de Galapagar (7) ⚠️ | Galapagar | 1 |
| Parc de Valdemorillo (30) ⚠️ | Valdemorillo | 1 |
| Parc de Madrid (1474) ⚠️ | Madrid › Vicálvaro | 1 |
| Parc de Madrid (1479) ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Parc de Las Rozas de Madrid (82) ⚠️ | Las Rozas de Madrid | 1 |
| Parc de Navalcarnero (21) ⚠️ | Navalcarnero | 1 |
| Forêt de Villaviciosa de Odón (4) ⚠️ | Villaviciosa de Odón | 1 |
| Parc de Boadilla del Monte (89) ⚠️ | Boadilla del Monte | 1 |
| Forêt de Pinto (9) ⚠️ | Pinto | 1 |
| Parc de Madrid (1503) ⚠️ | Madrid › Barajas | 1 |
| Parc de Madrid (1506) ⚠️ | Madrid › Arganzuela | 1 |
| Parc de Madrid (1507) ⚠️ | Madrid › Arganzuela | 1 |
| Parc de Parla (32) ⚠️ | Parla | 1 |
| Parc de Madrid (1510) ⚠️ | Madrid › Tetuán | 1 |
| Parc de Villanueva de la Cañada (40) ⚠️ | Villanueva de la Cañada | 1 |
| Forêt de Villamantilla (2) ⚠️ | Villamantilla | 1 |
| Parc de Madrid (1512) ⚠️ | Madrid › Villa de Vallecas | 1 |
| Parc de Madrid (1518) ⚠️ | Madrid › Vicálvaro | 1 |
| Parc de Algete (28) ⚠️ | Algete | 1 |
| Parc de Algete (30) ⚠️ | Algete | 1 |
| Parc de Algete (31) ⚠️ | Algete | 1 |
| Parc de Algete (33) ⚠️ | Algete | 1 |
| Parc de Collado Villalba (43) ⚠️ | Collado Villalba | 1 |
| Parc de Madrid (1524) ⚠️ | Madrid › Villa de Vallecas | 1 |
| Parc de Valdemoro (42) ⚠️ | Valdemoro | 1 |
| Forêt de Meco (7) ⚠️ | Meco | 1 |
| Bois de Tielmes (2) ⚠️ | Tielmes | 1 |
| Bois de Guadarrama (5) ⚠️ | Guadarrama | 1 |
| Parc de Madrid (1525) ⚠️ | Madrid › Puente de Vallecas | 1 |
| Prado de Juan Llanos ⚠️ | Guadarrama | 1 |
| Parc de Fuenlabrada (115) ⚠️ | Fuenlabrada | 1 |
| Parc de Leganés (87) ⚠️ | Leganés | 1 |
| Parc de Torrejón de Velasco (5) ⚠️ | Torrejón de Velasco | 1 |
| Parque Meseta de Orcasitas ⚠️ | Madrid › Usera | 1 |
| Parque Municipal O'Donnell ⚠️ | Alcalá de Henares | 1 |
| Parque de Sementales ⚠️ | Alcalá de Henares | 1 |
| Parque Tierno Galván ⚠️ | Alcalá de Henares | 1 |
| Parc de Madrid (1530) ⚠️ | Madrid › Vicálvaro | 1 |
| Parc de Guadarrama (33) ⚠️ | Guadarrama | 1 |
| Parque del Mareo ⚠️ | Guadarrama | 1 |
| Alto de la Torre ⚠️ | Guadarrama | 1 |
| Casino de la Reina ⚠️ | Madrid › Centro | 1 |
| Parc de Coslada (29) ⚠️ | Coslada | 1 |
| Plaza de Maruja ⚠️ | Madrid › Fuencarral-El Pardo | 1 |
| Bois de San Fernando de Henares (31) ⚠️ | San Fernando de Henares | 1 |
| Parc de Alcalá de Henares (74) ⚠️ | Alcalá de Henares | 1 |
| Forêt de Somosierra (31) ⚠️ | Somosierra | 1 |
| Parque Colón ⚠️ | Majadahonda | 1 |
| Parque de la Granja del Conde ⚠️ | Majadahonda | 1 |
| Bois de Villaconejos (17) ⚠️ | Villaconejos | 1 |
| Brujas ⚠️ | Madrid › Moratalaz | 1 |
| Parque Lineal Lonja de la Seda ⚠️ | Madrid › Carabanchel | 1 |
| Parque Abogados de Atocha (2) ⚠️ | San Fernando de Henares | 1 |
| Parque de Rafael Sánchez Ferlosio ⚠️ | San Fernando de Henares | 1 |
| Parque Lola Camarena ⚠️ | Madrid › Villa de Vallecas | 1 |
| Parc de Villanueva de la Cañada (41) ⚠️ | Villanueva de la Cañada | 1 |
| Plaza de Oriente ⚠️ | Madrid › Centro | 1 |
| Parc de Pozuelo de Alarcón (149) ⚠️ | Pozuelo de Alarcón | 1 |
| Parque La Perla ⚠️ | Madrid › Usera | 1 |
| Parc de Madrid (1543) ⚠️ | Madrid › Latina | 1 |

6 087 parc(s) plus petits qu'une cellule ne sont pas listés : la carte les dessine, mais ils n'offrent aucune cellule.

⚠️ 8673 parc(s) hors de la fenêtre 10–125 cellules (8573 trop petit(s), 100 trop grand(s)) : affichés sur la carte, mais ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| military | 2 465 |
| airport | 2 183 |
| prison | 48 |
| **Total déclaré** | **4 696** |
| dont dans une zone de ce territoire | 4 691 |

Le jeu de données couvre plus large que le territoire — il est produit à une échelle supérieure. Seules les cellules tombant dans une zone d'ici pèsent sur un pourcentage.

### Zones concernées

| Zone | Cellules exclues |
|---|---:|
| Madrid | 1 310 |
| Barajas | 946 |
| Torrejón de Ardoz | 555 |
| Moralzarzal | 484 |
| Alcobendas | 470 |
| San Martín de la Vega | 311 |
| Hoyo de Manzanares | 260 |
| Latina | 243 |
| Getafe | 185 |
| Alcalá de Henares | 149 |
| Villar del Olmo | 137 |
| El Boalo-Cerceda-Mataelpino | 134 |
| Pozuelo de Alarcón | 95 |
| Santorcaz | 90 |
| San Sebastián de los Reyes | 85 |
| Ajalvir | 83 |
| Fuencarral-El Pardo | 81 |
| Colmenar Viejo | 71 |
| Paracuellos de Jarama | 48 |
| Orusco de Tajuña | 45 |
| Manzanares el Real | 41 |
| Villalbilla | 29 |
| Villaverde | 15 |
| Valdilecha | 12 |
| Navalcarnero | 10 |
| Soto del Real | 10 |
| Aranjuez | 8 |
| Carabanchel | 8 |
| Moncloa-Aravaca | 8 |
| Estremera | 7 |
| Valdemoro | 7 |
| Alcorcón | 7 |
| Navalagamella | 7 |
| Collado Villalba | 7 |
| Villaconejos | 6 |
| Villanueva de la Cañada | 6 |
| San Blas - Canillejas | 5 |
| Torres de la Alameda | 5 |
| Villanueva del Pardillo | 5 |
| Ciudad Lineal | 4 |
| Valdemorillo | 4 |
| Griñón | 3 |
| Becerril de la Sierra | 3 |
| Carabaña | 1 |
| Meco | 1 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
