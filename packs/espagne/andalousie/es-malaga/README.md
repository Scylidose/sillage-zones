# Province de Málaga

Pack `es-malaga` · version 1.1.1 · grille 200 m · Espagne › Andalousie

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 283 667 |
| dont restreintes (aéroport, militaire, prison) | 709 |
| dont sans chemin (aucune voie à moins de 60 m) | 95 224 |
| Cellules retirées par le masque d'eau | 1 925 |
| Villes | 103 |
| Arrondissements et quartiers | 0 |
| Îles | 9 |
| Parcs | 4 589 |

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

## Îles

| Île | Cellules | Composition |
|---|---:|---|
| Antequera | 44 523 | somme de 7 villes |
| Costa del Sol Occidental | 31 067 | somme de 9 villes |
| Guadalteba | 30 358 | somme de 9 villes |
| La Axarquía | 39 789 | somme de 31 villes |
| Málaga-Costa del Sol | 15 276 | somme de 1 villes |
| Nororma | 17 103 | somme de 7 villes |
| Serranía de Ronda | 47 709 | somme de 22 villes |
| Sierra de las Nieves | 26 463 | somme de 9 villes |
| Valle del Guadalhorce | 31 391 | somme de 8 villes |

Une île *composite* n'a pas de cellules à elle : sa progression est la somme de ses villes, et ses cellules ne lui sont jamais rattachées directement — elles compteraient deux fois.

## Villes (103)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Sans chemin | Parcs |
|---|---:|---:|---:|---:|---:|---:|---:|
| Antequera | 29 467 | 170 | 29 297 | 4 | **29 293** | 14 795 (51 %) | 123 |
| Ronda | 15 527 | 1 | 15 526 | 474 | **15 052** | 4 804 (32 %) | 64 |
| Málaga | 15 439 | 163 | 15 276 | 212 | **15 064** | 1 194 (8 %) | 1090 |
| Archidona | 7 307 | 3 | 7 304 | 9 | **7 295** | 3 537 (48 %) | 14 |
| Campillos | 7 377 | 366 | 7 011 | 0 | **7 011** | 3 334 (48 %) | 4 |
| Cortes de la Frontera | 6 828 | 1 | 6 827 | 0 | **6 827** | 2 767 (41 %) | 2 |
| Álora | 6 639 | 8 | 6 631 | 0 | **6 631** | 2 716 (41 %) | 135 |
| Cañete la Real | 6 480 | 0 | 6 480 | 0 | **6 480** | 4 232 (65 %) |  |
| Almogía | 6 370 | 34 | 6 336 | 0 | **6 336** | 2 367 (37 %) |  |
| Casares | 6 282 | 18 | 6 264 | 0 | **6 264** | 2 957 (47 %) | 8 |
| Vélez-Málaga | 6 161 | 32 | 6 129 | 6 | **6 123** | 408 (7 %) | 371 |
| Mijas | 5 766 | 17 | 5 749 | 0 | **5 749** | 759 (13 %) | 650 |
| Benahavís | 5 650 | 9 | 5 641 | 0 | **5 641** | 1 721 (31 %) | 33 |
| Teba | 5 605 | 50 | 5 555 | 0 | **5 555** | 2 637 (47 %) | 2 |
| Estepona | 5 318 | 7 | 5 311 | 0 | **5 311** | 1 158 (22 %) | 62 |
| Coín | 4 956 | 0 | 4 956 | 0 | **4 956** | 1 476 (30 %) | 32 |
| El Burgo | 4 636 | 0 | 4 636 | 0 | **4 636** | 2 206 (48 %) | 40 |
| Marbella | 4 537 | 20 | 4 517 | 0 | **4 517** | 374 (8 %) | 288 |
| Casarabonela | 4 443 | 1 | 4 442 | 0 | **4 442** | 2 425 (55 %) | 1 |
| Cártama | 4 096 | 6 | 4 090 | 0 | **4 090** | 1 617 (40 %) | 22 |
| Ardales | 4 173 | 210 | 3 963 | 0 | **3 963** | 1 958 (49 %) | 16 |
| Gaucín | 3 815 | 0 | 3 815 | 0 | **3 815** | 1 940 (51 %) | 4 |
| Istán | 3 861 | 79 | 3 782 | 0 | **3 782** | 1 368 (36 %) | 57 |
| Tolox | 3 672 | 0 | 3 672 | 0 | **3 672** | 685 (19 %) | 187 |
| Sierra de Yeguas | 3 378 | 0 | 3 378 | 0 | **3 378** | 1 678 (50 %) | 1 |
| Ojén | 3 341 | 0 | 3 341 | 0 | **3 341** | 1 284 (38 %) | 104 |
| Nerja | 3 322 | 0 | 3 322 | 0 | **3 322** | 1 043 (31 %) | 51 |
| Alhaurín de la Torre | 3 210 | 3 | 3 207 | 4 | **3 203** | 788 (25 %) | 48 |
| Fuente de Piedra | 3 573 | 481 | 3 092 | 0 | **3 092** | 1 514 (49 %) | 1 |
| Mollina | 2 947 | 0 | 2 947 | 0 | **2 947** | 1 143 (39 %) | 7 |
| Alhaurín el Grande | 2 851 | 0 | 2 851 | 0 | **2 851** | 297 (10 %) | 61 |
| Villanueva de Algaidas | 2 775 | 2 | 2 773 | 0 | **2 773** | 1 504 (54 %) | 5 |
| Villanueva de la Concepción | 2 640 | 0 | 2 640 | 0 | **2 640** | 1 234 (47 %) | 4 |
| Casabermeja | 2 629 | 4 | 2 625 | 0 | **2 625** | 507 (19 %) | 2 |
| Colmenar | 2 581 | 1 | 2 580 | 0 | **2 580** | 324 (13 %) | 23 |
| Alameda | 2 581 | 8 | 2 573 | 0 | **2 573** | 1 696 (66 %) |  |
| Pizarra | 2 487 | 0 | 2 487 | 0 | **2 487** | 788 (32 %) | 34 |
| Villanueva del Trabuco | 2 319 | 0 | 2 319 | 0 | **2 319** | 913 (39 %) | 68 |
| Periana | 2 282 | 1 | 2 281 | 0 | **2 281** | 403 (18 %) | 33 |
| Monda | 2 238 | 0 | 2 238 | 0 | **2 238** | 285 (13 %) | 97 |
| Yunquera | 2 152 | 0 | 2 152 | 0 | **2 152** | 412 (19 %) | 61 |
| Montecorto | 2 128 | 8 | 2 120 | 0 | **2 120** | 557 (26 %) | 2 |
| Cómpeta | 2 112 | 0 | 2 112 | 0 | **2 112** | 705 (33 %) | 5 |
| Torrox | 1 970 | 2 | 1 968 | 0 | **1 968** | 82 (4 %) | 16 |
| Alcaucín | 1 772 | 1 | 1 771 | 0 | **1 771** | 384 (22 %) | 24 |
| Montejaque | 1 768 | 9 | 1 759 | 0 | **1 759** | 677 (38 %) | 7 |
| Parauta | 1 729 | 0 | 1 729 | 0 | **1 729** | 688 (40 %) | 17 |
| Villanueva del Rosario | 1 727 | 0 | 1 727 | 0 | **1 727** | 531 (31 %) | 17 |
| Igualeja | 1 701 | 0 | 1 701 | 0 | **1 701** | 558 (33 %) | 4 |
| Canillas de Aceituno | 1 642 | 2 | 1 640 | 0 | **1 640** | 281 (17 %) | 10 |
| Frigiliana | 1 584 | 0 | 1 584 | 0 | **1 584** | 459 (29 %) | 25 |
| Riogordo | 1 568 | 1 | 1 567 | 0 | **1 567** | 247 (16 %) | 10 |
| Jubrique | 1 517 | 0 | 1 517 | 0 | **1 517** | 238 (16 %) |  |
| Cuevas de San Marcos | 1 459 | 9 | 1 450 | 0 | **1 450** | 697 (48 %) | 17 |
| Manilva | 1 369 | 3 | 1 366 | 0 | **1 366** | 134 (10 %) | 6 |
| Almargen | 1 349 | 0 | 1 349 | 0 | **1 349** | 540 (40 %) | 8 |
| Humilladero | 1 354 | 5 | 1 349 | 0 | **1 349** | 587 (44 %) | 24 |
| Alfarnate | 1 334 | 1 | 1 333 | 0 | **1 333** | 270 (20 %) | 15 |
| Alozaina | 1 322 | 0 | 1 322 | 0 | **1 322** | 322 (24 %) | 18 |
| Júzcar | 1 313 | 0 | 1 313 | 0 | **1 313** | 330 (25 %) |  |
| Canillas de Albaida | 1 293 | 0 | 1 293 | 0 | **1 293** | 157 (12 %) | 32 |
| Benaoján | 1 250 | 0 | 1 250 | 0 | **1 250** | 678 (54 %) |  |
| Genalguacil | 1 243 | 0 | 1 243 | 0 | **1 243** | 351 (28 %) |  |
| Sedella | 1 238 | 0 | 1 238 | 0 | **1 238** | 185 (15 %) | 17 |
| Alpandeire | 1 213 | 0 | 1 213 | 0 | **1 213** | 447 (37 %) |  |
| Serrato | 1 114 | 0 | 1 114 | 0 | **1 114** | 609 (55 %) | 1 |
| Rincón de la Victoria | 1 099 | 7 | 1 092 | 0 | **1 092** | 7 (1 %) | 81 |
| Jimera de Líbar | 1 064 | 0 | 1 064 | 0 | **1 064** | 515 (48 %) |  |
| Benalmádena | 1 045 | 3 | 1 042 | 0 | **1 042** | 75 (7 %) | 36 |
| Arenas | 1 028 | 0 | 1 028 | 0 | **1 028** | 133 (13 %) | 10 |
| Comares | 993 | 8 | 985 | 0 | **985** | 17 (2 %) | 21 |
| Benarrabá | 972 | 0 | 972 | 0 | **972** | 139 (14 %) |  |
| El Borge | 957 | 0 | 957 | 0 | **957** | 130 (14 %) | 7 |
| Pujerra | 944 | 0 | 944 | 0 | **944** | 512 (54 %) |  |
| Viñuela | 1 092 | 152 | 940 | 0 | **940** | 33 (4 %) | 67 |
| Carratraca | 881 | 0 | 881 | 0 | **881** | 331 (38 %) |  |
| Guaro | 878 | 0 | 878 | 0 | **878** | 198 (23 %) | 10 |
| Villanueva de Tapia | 874 | 0 | 874 | 0 | **874** | 455 (52 %) | 3 |
| Cartajima | 840 | 0 | 840 | 0 | **840** | 389 (46 %) |  |
| Valle de Abdalajís | 833 | 0 | 833 | 0 | **833** | 385 (46 %) | 19 |
| Alfarnatejo | 804 | 0 | 804 | 0 | **804** | 77 (10 %) | 11 |
| Benadalid | 802 | 0 | 802 | 0 | **802** | 297 (37 %) | 2 |
| Faraján | 795 | 0 | 795 | 0 | **795** | 116 (15 %) |  |
| Torremolinos | 782 | 0 | 782 | 0 | **782** | 78 (10 %) | 33 |
| Algatocín | 766 | 0 | 766 | 0 | **766** | 178 (23 %) |  |
| Cútar | 764 | 0 | 764 | 0 | **764** | 60 (8 %) | 7 |
| Benalauría | 764 | 1 | 763 | 0 | **763** | 229 (30 %) |  |
| Sayalonga | 711 | 1 | 710 | 0 | **710** | 58 (8 %) | 2 |
| Cuevas Bajas | 656 | 0 | 656 | 0 | **656** | 363 (55 %) | 2 |
| Cuevas del Becerro | 627 | 0 | 627 | 0 | **627** | 175 (28 %) | 2 |
| Almáchar | 555 | 0 | 555 | 0 | **555** | 70 (13 %) | 5 |
| Moclinejo | 555 | 0 | 555 | 0 | **555** | 31 (6 %) | 2 |
| Benamargosa | 475 | 0 | 475 | 0 | **475** | 33 (7 %) | 13 |
| Atajate | 422 | 0 | 422 | 0 | **422** | 69 (16 %) |  |
| Salares | 405 | 0 | 405 | 0 | **405** | 19 (5 %) | 17 |
| Fuengirola | 395 | 0 | 395 | 0 | **395** | 2 (1 %) | 70 |
| Algarrobo | 383 | 7 | 376 | 0 | **376** | 9 (2 %) | 45 |
| Totalán | 354 | 4 | 350 | 0 | **350** | 11 (3 %) | 4 |
| Arriate | 328 | 0 | 328 | 0 | **328** | 11 (3 %) | 1 |
| Iznate | 294 | 4 | 290 | 0 | **290** | 22 (8 %) | 1 |
| Macharaviaya | 284 | 2 | 282 | 0 | **282** | 8 (3 %) | 6 |
| Benamocarra | 217 | 0 | 217 | 0 | **217** | 26 (12 %) | 9 |
| Árchez | 186 | 0 | 186 | 0 | **186** | 4 (2 %) |  |

## Parcs (4589)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Bois de Málaga (715) ⚠️ | Málaga › Málaga-Costa del Sol | 911 |
| Bois de Málaga (727) ⚠️ | Málaga › Málaga-Costa del Sol | 788 |
| Bois de Serrato ⚠️ | Serrato › Guadalteba | 311 |
| Bois de Mollina ⚠️ | Mollina › Antequera | 297 |
| Forêt de Coín (23) ⚠️ | Coín › Valle del Guadalhorce | 210 |
| Forêt de Antequera (3) ⚠️ | Antequera › Antequera | 209 |
| Forêt de Nerja (2) ⚠️ | Nerja › La Axarquía | 191 |
| Forêt de Tolox ⚠️ | Tolox › Sierra de las Nieves | 179 |
| Forêt de Periana ⚠️ | Periana › La Axarquía | 154 |
| Forêt de Tolox (86) ⚠️ | Tolox › Sierra de las Nieves | 153 |
| Parque Forestal Ciudad de Málaga ⚠️ | Málaga › Málaga-Costa del Sol | 137 |
| Forêt de Alfarnatejo | Alfarnatejo › La Axarquía | 121 |
| Forêt de Antequera (5) | Antequera › Antequera | 118 |
| Forêt de Alfarnate (2) | Alfarnate › La Axarquía | 116 |
| Forêt de Antequera (14) | Antequera › Antequera | 115 |
| Forêt de El Burgo | El Burgo › Sierra de las Nieves | 112 |
| Bois de Benahavís | Benahavís › Costa del Sol Occidental | 110 |
| Bois de Ardales (14) | Ardales › Guadalteba | 108 |
| Forêt de Ronda (10) | Ronda › Serranía de Ronda | 104 |
| Forêt de Ronda (6) | Ronda › Serranía de Ronda | 98 |
| Forêt de Humilladero (5) | Humilladero › Antequera | 97 |
| Forêt de Nerja | Nerja › La Axarquía | 92 |
| Forêt de Yunquera | Yunquera › Sierra de las Nieves | 90 |
| Forêt de Tolox (2) | Tolox › Sierra de las Nieves | 88 |
| Bois de Istán (9) | Istán › Sierra de las Nieves | 88 |
| Forêt de Alhaurín el Grande (40) | Alhaurín el Grande › Valle del Guadalhorce | 82 |
| Forêt de Antequera (2) | Antequera › Antequera | 78 |
| Forêt de Marbella (13) | Marbella › Costa del Sol Occidental | 78 |
| Bois de Istán (30) | Istán › Sierra de las Nieves | 76 |
| Forêt de Benalmádena (3) | Benalmádena › Costa del Sol Occidental | 76 |
| Forêt de Antequera (24) | Antequera › Antequera | 74 |
| Pinar de los Almendrales | Málaga › Málaga-Costa del Sol | 73 |
| Forêt de Alfarnate (3) | Alfarnate › La Axarquía | 71 |
| Forêt de Monda (23) | Monda › Sierra de las Nieves | 68 |
| Forêt de Nerja (13) | Nerja › La Axarquía | 66 |
| Forêt de Villanueva del Trabuco (5) | Villanueva del Trabuco › Nororma | 65 |
| Bois de Alfarnate (2) | Alfarnate › La Axarquía | 65 |
| Forêt de Coín (24) | Coín › Valle del Guadalhorce | 65 |
| Forêt de Alhaurín el Grande | Alhaurín el Grande › Valle del Guadalhorce | 63 |
| Bois de Colmenar (3) | Colmenar › La Axarquía | 63 |
| Forêt de Ojén (50) | Ojén › Sierra de las Nieves | 61 |
| Forêt de Salares (14) | Salares › La Axarquía | 60 |
| Bois de Istán (29) | Istán › Sierra de las Nieves | 60 |
| Forêt de Alhaurín el Grande (3) | Alhaurín el Grande › Valle del Guadalhorce | 57 |
| Forêt de Tolox (10) | Tolox › Sierra de las Nieves | 57 |
| Forêt de Coín (4) | Coín › Valle del Guadalhorce | 56 |
| Bois de Istán (13) | Istán › Sierra de las Nieves | 56 |
| Forêt de Sedella (17) | Sedella › La Axarquía | 55 |
| Forêt de Tolox (6) | Tolox › Sierra de las Nieves | 53 |
| Forêt de Villanueva del Trabuco (4) | Villanueva del Trabuco › Nororma | 52 |
| Forêt de Arenas (10) | Arenas › La Axarquía | 52 |
| Bois de Montejaque (5) | Montejaque › Serranía de Ronda | 51 |
| Bois de El Burgo (6) | El Burgo › Sierra de las Nieves | 49 |
| Bois de Ardales (8) | Ardales › Guadalteba | 48 |
| Forêt de Alhaurín el Grande (10) | Alhaurín el Grande › Valle del Guadalhorce | 46 |
| Forêt de Canillas de Albaida (24) | Canillas de Albaida › La Axarquía | 45 |
| Forêt de Yunquera (13) | Yunquera › Sierra de las Nieves | 44 |
| Forêt de Tolox (5) | Tolox › Sierra de las Nieves | 43 |
| Bois de Nerja (16) | Nerja › La Axarquía | 41 |
| Forêt de Alcaucín (9) | Alcaucín › La Axarquía | 39 |
| Forêt de Coín (7) | Coín › Valle del Guadalhorce | 39 |
| Forêt de Monda (10) | Monda › Sierra de las Nieves | 38 |
| Forêt de Álora (3) | Álora › Valle del Guadalhorce | 38 |
| Forêt de Marbella (12) | Marbella › Costa del Sol Occidental | 37 |
| Forêt de Tolox (8) | Tolox › Sierra de las Nieves | 37 |
| Bois de Alfarnatejo (2) | Alfarnatejo › La Axarquía | 37 |
| Bois de Frigiliana (11) | Frigiliana › La Axarquía | 37 |
| Forêt de Alfarnate | Alfarnate › La Axarquía | 36 |
| Forêt de Alcaucín (16) | Alcaucín › La Axarquía | 36 |
| Parque Periurbano Pinar del Hacho | Antequera › Antequera | 35 |
| Forêt de Yunquera (4) | Yunquera › Sierra de las Nieves | 35 |
| Forêt de Montecorto (2) | Montecorto › Serranía de Ronda | 35 |
| Bois de Frigiliana (8) | Frigiliana › La Axarquía | 35 |
| Forêt de Mollina | Mollina › Antequera | 34 |
| Forêt de Tolox (7) | Tolox › Sierra de las Nieves | 34 |
| Forêt de Alozaina (3) | Alozaina › Sierra de las Nieves | 34 |
| Forêt de Tolox (56) | Tolox › Sierra de las Nieves | 34 |
| Forêt de Ojén (77) | Ojén › Sierra de las Nieves | 34 |
| Bois de Antequera (25) | Antequera › Antequera | 34 |
| Forêt de Ojén | Ojén › Sierra de las Nieves | 33 |
| Forêt de Yunquera (5) | Yunquera › Sierra de las Nieves | 33 |
| Forêt de Ojén (73) | Ojén › Sierra de las Nieves | 32 |
| Forêt de Ojén (81) | Ojén › Sierra de las Nieves | 32 |
| Bois de Málaga (3) | Málaga › Málaga-Costa del Sol | 31 |
| Forêt de El Burgo (2) | Yunquera › Sierra de las Nieves | 31 |
| Forêt de Canillas de Albaida (20) | Canillas de Albaida › La Axarquía | 31 |
| Bois de Frigiliana (14) | Frigiliana › La Axarquía | 31 |
| Pinar de Nagüeles | Marbella › Costa del Sol Occidental | 30 |
| Forêt de Canillas de Albaida (4) | Canillas de Albaida › La Axarquía | 30 |
| Forêt de Marbella | Marbella › Costa del Sol Occidental | 29 |
| Forêt de Tolox (16) | Tolox › Sierra de las Nieves | 29 |
| Forêt de Antequera (4) | Antequera › Antequera | 28 |
| Bois de Alfarnate (3) | Alfarnate › La Axarquía | 28 |
| Forêt de Alfarnatejo (2) | Alfarnatejo › La Axarquía | 28 |
| Bois de Riogordo | Riogordo › La Axarquía | 28 |
| Forêt de Antequera (20) | Antequera › Antequera | 27 |
| Bois de Villanueva de la Concepción | Villanueva de la Concepción › Antequera | 27 |
| Bois de Istán (3) | Istán › Sierra de las Nieves | 26 |
| Bois de Antequera (11) | Antequera › Antequera | 26 |
| Bois de Málaga (659) | Málaga › Málaga-Costa del Sol | 26 |
| Forêt de Alhaurín el Grande (48) | Alhaurín el Grande › Valle del Guadalhorce | 26 |
| Bois de Istán (21) | Istán › Sierra de las Nieves | 25 |
| Bois de Ardales (9) | Ardales › Guadalteba | 25 |
| Forêt de Salares (5) | Salares › La Axarquía | 24 |
| Forêt de Salares (7) | Salares › La Axarquía | 24 |
| Bois de Istán (18) | Istán › Sierra de las Nieves | 24 |
| Bois de Benahavís (2) | Benahavís › Costa del Sol Occidental | 23 |
| Forêt de Villanueva del Rosario | Villanueva del Rosario › Nororma | 22 |
| Bois de Monda (23) | Monda › Sierra de las Nieves | 22 |
| Bois de Istán (17) | Istán › Sierra de las Nieves | 22 |
| Bois de Istán (33) | Istán › Sierra de las Nieves | 22 |
| Bois de Ronda (27) | Ronda › Serranía de Ronda | 22 |
| Bois de Igualeja | Igualeja › Serranía de Ronda | 21 |
| Bois de Antequera (35) | Antequera › Antequera | 21 |
| Bois de Frigiliana (6) | Frigiliana › La Axarquía | 21 |
| Forêt de Antequera | Antequera › Antequera | 20 |
| Forêt de Cuevas de San Marcos | Cuevas de San Marcos › Nororma | 20 |
| Bois de Málaga (2) | Málaga › Málaga-Costa del Sol | 20 |
| Bois de Marbella (17) | Marbella › Costa del Sol Occidental | 20 |
| Bois de El Burgo (16) | El Burgo › Sierra de las Nieves | 20 |
| Forêt de Monda (14) | Monda › Sierra de las Nieves | 20 |
| Bois de Antequera (29) | Antequera › Antequera | 20 |
| Forêt de Benalmádena (2) | Benalmádena › Costa del Sol Occidental | 20 |
| Forêt de Coín | Coín › Valle del Guadalhorce | 19 |
| Forêt de Canillas de Albaida | Canillas de Albaida › La Axarquía | 19 |
| Forêt de Canillas de Albaida (2) | Canillas de Albaida › La Axarquía | 19 |
| Forêt de Montecorto | Montecorto › Serranía de Ronda | 19 |
| Bois de Villanueva del Trabuco | Villanueva del Trabuco › Nororma | 19 |
| Forêt de Yunquera (2) | Yunquera › Sierra de las Nieves | 19 |
| Forêt de Tolox (4) | Tolox › Sierra de las Nieves | 19 |
| Forêt de Canillas de Albaida (6) | Canillas de Albaida › La Axarquía | 19 |
| Bois de Guaro (7) | Guaro › Sierra de las Nieves | 19 |
| Bois de Alfarnatejo (3) | Alfarnatejo › La Axarquía | 19 |
| Forêt de Ardales | Ardales › Guadalteba | 18 |
| Forêt de Canillas de Aceituno | Canillas de Aceituno › La Axarquía | 18 |
| Bois de Málaga | Málaga › Málaga-Costa del Sol | 18 |
| Forêt de Yunquera (3) | Yunquera › Sierra de las Nieves | 18 |
| Bois de Monda (6) | Monda › Sierra de las Nieves | 18 |
| Bois de El Burgo (9) | El Burgo › Sierra de las Nieves | 18 |
| Bois de El Burgo (21) | El Burgo › Sierra de las Nieves | 18 |
| Forêt de Salares (15) | Salares › La Axarquía | 18 |
| Parque Forestal La Virreina | Málaga › Málaga-Costa del Sol | 18 |
| Forêt de Monda (15) | Monda › Sierra de las Nieves | 18 |
| Bois de Antequera (24) | Antequera › Antequera | 18 |
| Forêt de Arenas (11) | Arenas › La Axarquía | 18 |
| Forêt de Canillas de Albaida (13) | Canillas de Albaida › La Axarquía | 17 |
| Bois de Istán (28) | Istán › Sierra de las Nieves | 17 |
| Forêt de Villanueva de la Concepción | Villanueva de la Concepción › Antequera | 17 |
| Forêt de Marbella (23) | Marbella › Costa del Sol Occidental | 17 |
| Forêt de Monda (12) | Monda › Sierra de las Nieves | 17 |
| Forêt de Villanueva del Trabuco (26) | Villanueva del Trabuco › Nororma | 17 |
| Bois de Colmenar (5) | Colmenar › La Axarquía | 17 |
| Bois de Ardales (12) | Ardales › Guadalteba | 17 |
| Parque Forestal Monte Victoria | Málaga › Málaga-Costa del Sol | 16 |
| Forêt de Coín (3) | Coín › Valle del Guadalhorce | 16 |
| Forêt de Monda (4) | Monda › Sierra de las Nieves | 16 |
| Bois de El Burgo (7) | El Burgo › Sierra de las Nieves | 16 |
| Bois de Yunquera (43) | Yunquera › Sierra de las Nieves | 16 |
| Bois de Alcaucín | Alcaucín › La Axarquía | 16 |
| Forêt de Canillas de Albaida (19) | Canillas de Albaida › La Axarquía | 16 |
| Forêt de Antequera (34) | Antequera › Antequera | 16 |
| Bois de Riogordo (3) | Riogordo › La Axarquía | 16 |
| Bois de Ardales (13) | Ardales › Guadalteba | 16 |
| Forêt de Periana (16) | Periana › La Axarquía | 15 |
| Forêt de Istán | Istán › Sierra de las Nieves | 15 |
| Forêt de Alozaina (6) | Alozaina › Sierra de las Nieves | 15 |
| Bois de Istán (25) | Istán › Sierra de las Nieves | 15 |
| Bois de Periana | Periana › La Axarquía | 15 |
| Forêt de Sedella (16) | Sedella › La Axarquía | 15 |
| Forêt de Coín (12) | Coín › Valle del Guadalhorce | 15 |
| Bois de Antequera (30) | Antequera › Antequera | 15 |
| Forêt de Colmenar | Colmenar › La Axarquía | 14 |
| Forêt de Alhaurín el Grande (9) | Alhaurín el Grande › Valle del Guadalhorce | 14 |
| Forêt de Alhaurín el Grande (18) | Alhaurín el Grande › Valle del Guadalhorce | 14 |
| Bois de Istán (42) | Istán › Sierra de las Nieves | 14 |
| Forêt de Villanueva del Rosario (2) | Villanueva del Rosario › Nororma | 14 |
| Forêt de Monda (13) | Monda › Sierra de las Nieves | 14 |
| Forêt de Coín (14) | Coín › Valle del Guadalhorce | 14 |
| Forêt de Villanueva del Rosario (8) | Villanueva del Rosario › Nororma | 14 |
| Bois de Cuevas de San Marcos (4) | Cuevas de San Marcos › Nororma | 14 |
| Forêt de Alhaurín el Grande (37) | Alhaurín el Grande › Valle del Guadalhorce | 13 |
| Bois de Villanueva del Trabuco (4) | Villanueva del Trabuco › Nororma | 13 |
| Forêt de Canillas de Albaida (8) | Canillas de Albaida › La Axarquía | 13 |
| Bois de Monda (24) | Monda › Sierra de las Nieves | 13 |
| Bois de Parauta (2) | Parauta › Serranía de Ronda | 13 |
| Bois de Istán (47) | Istán › Sierra de las Nieves | 13 |
| Forêt de Coín (10) | Coín › Valle del Guadalhorce | 13 |
| Parque Forestal de Gibralfaro | Málaga › Málaga-Costa del Sol | 13 |
| Forêt de Alhaurín el Grande (31) | Alhaurín el Grande › Valle del Guadalhorce | 12 |
| Forêt de Parauta | Parauta › Serranía de Ronda | 12 |
| Forêt de Monda (2) | Monda › Sierra de las Nieves | 12 |
| Bois de Parauta | Parauta › Serranía de Ronda | 12 |
| Bois de Parauta (10) | Parauta › Serranía de Ronda | 12 |
| Bois de Alfarnate (4) | Alfarnate › La Axarquía | 12 |
| Parque Forestal Monte San Antón | Málaga › Málaga-Costa del Sol | 12 |
| Forêt de Antequera (21) | Antequera › Antequera | 12 |
| Forêt de Antequera (22) | Antequera › Antequera | 12 |
| Forêt de Villanueva de la Concepción (3) | Villanueva de la Concepción › Antequera | 12 |
| Bois de Colmenar (2) | Colmenar › La Axarquía | 12 |
| Bois de Antequera (33) | Antequera › Antequera | 12 |
| Bois de Antequera (34) | Antequera › Antequera | 12 |
| Forêt de Alhaurín el Grande (14) | Alhaurín el Grande › Valle del Guadalhorce | 11 |
| Forêt de Ronda (8) | Ronda › Serranía de Ronda | 11 |
| Forêt de Salares (4) | Salares › La Axarquía | 11 |
| Bois de Yunquera (28) | Yunquera › Sierra de las Nieves | 11 |
| Bois de Casarabonela | Casarabonela › Sierra de las Nieves | 11 |
| Forêt de Málaga (2) | Málaga › Málaga-Costa del Sol | 11 |
| Forêt de Benamargosa (12) | Benamargosa › La Axarquía | 11 |
| Bois de Málaga (664) | Málaga › Málaga-Costa del Sol | 11 |
| Forêt de Sedella (18) | Sedella › La Axarquía | 11 |
| Forêt de Alhaurín el Grande (49) | Alhaurín el Grande › Valle del Guadalhorce | 11 |
| Forêt de Antequera (12) | Antequera › Antequera | 10 |
| Forêt de Periana (4) | Periana › La Axarquía | 10 |
| Forêt de Viñuela (15) | Viñuela › La Axarquía | 10 |
| Forêt de Tolox (28) | Tolox › Sierra de las Nieves | 10 |
| Forêt de Canillas de Albaida (11) | Canillas de Albaida › La Axarquía | 10 |
| Forêt de Canillas de Albaida (14) | Canillas de Albaida › La Axarquía | 10 |
| Forêt de Canillas de Aceituno (2) | Canillas de Aceituno › La Axarquía | 10 |
| Parque Forestal Comandante Benítez | Málaga › Málaga-Costa del Sol | 10 |
| Bois de Yunquera (4) | Yunquera › Sierra de las Nieves | 10 |
| Bois de El Burgo (5) | El Burgo › Sierra de las Nieves | 10 |
| Parque Forestal La Concepción | Málaga › Málaga-Costa del Sol | 10 |
| Forêt de Humilladero | Humilladero › Antequera | 10 |
| Forêt de Fuente de Piedra | Fuente de Piedra › Antequera | 10 |
| Forêt de Antequera (19) | Antequera › Antequera | 10 |
| Bois de Ojén (8) | Ojén › Sierra de las Nieves | 10 |
| Forêt de Monda (11) | Monda › Sierra de las Nieves | 10 |
| Forêt de Málaga | Málaga › Málaga-Costa del Sol | 10 |
| Bois de Antequera (15) | Antequera › Antequera | 10 |
| Bois de Antequera (19) | Antequera › Antequera | 10 |
| Forêt de Istán (7) | Istán › Sierra de las Nieves | 10 |
| Parque Ibn Al-Baytar | Benalmádena › Costa del Sol Occidental | 10 |
| Bois de Málaga (667) | Málaga › Málaga-Costa del Sol | 10 |
| Bois de Benahavís (4) | Benahavís › Costa del Sol Occidental | 10 |
| Forêt de Canillas de Albaida (26) | Canillas de Albaida › La Axarquía | 10 |
| Forêt de Marbella (55) | Marbella › Costa del Sol Occidental | 10 |
| Forêt de Coín (2) ⚠️ | Coín › Valle del Guadalhorce | 9 |
| Forêt de Alhaurín el Grande (29) ⚠️ | Alhaurín el Grande › Valle del Guadalhorce | 9 |
| Forêt de Alhaurín el Grande (38) ⚠️ | Alhaurín el Grande › Valle del Guadalhorce | 9 |
| Forêt de Vélez-Málaga (28) ⚠️ | Vélez-Málaga › La Axarquía | 9 |
| Forêt de Antequera (15) ⚠️ | Antequera › Antequera | 9 |
| Forêt de Tolox (17) ⚠️ | Tolox › Sierra de las Nieves | 9 |
| Bois de Tolox (26) ⚠️ | Tolox › Sierra de las Nieves | 9 |
| Bois de Yunquera (11) ⚠️ | Yunquera › Sierra de las Nieves | 9 |
| Bois de Monda (41) ⚠️ | Monda › Sierra de las Nieves | 9 |
| Forêt de Canillas de Albaida (16) ⚠️ | Canillas de Albaida › La Axarquía | 9 |
| Forêt de Coín (8) ⚠️ | Coín › Valle del Guadalhorce | 9 |
| Forêt de Villanueva del Rosario (5) ⚠️ | Villanueva del Rosario › Nororma | 9 |
| Forêt de Villanueva del Rosario (7) ⚠️ | Villanueva del Rosario › Nororma | 9 |
| Bois de Antequera (7) ⚠️ | Antequera › Antequera | 9 |
| Forêt de Cútar (7) ⚠️ | Cútar › La Axarquía | 9 |
| Bois de Nerja (12) ⚠️ | Nerja › La Axarquía | 9 |
| Bois de Benahavís (15) ⚠️ | Benahavís › Costa del Sol Occidental | 9 |
| Parque Forestal de El Morlaco ⚠️ | Málaga › Málaga-Costa del Sol | 8 |
| Forêt de Ojén (46) ⚠️ | Ojén › Sierra de las Nieves | 8 |
| Forêt de Mijas (352) ⚠️ | Mijas › Costa del Sol Occidental | 8 |
| Forêt de Alhaurín el Grande (41) ⚠️ | Alhaurín el Grande › Valle del Guadalhorce | 8 |
| Forêt de Antequera (11) ⚠️ | Antequera › Antequera | 8 |
| Forêt de Yunquera (9) ⚠️ | Yunquera › Sierra de las Nieves | 8 |
| Forêt de Tolox (18) ⚠️ | Tolox › Sierra de las Nieves | 8 |
| Forêt de Yunquera (12) ⚠️ | Yunquera › Sierra de las Nieves | 8 |
| Forêt de Salares ⚠️ | Salares › La Axarquía | 8 |
| Bois de El Burgo ⚠️ | El Burgo › Sierra de las Nieves | 8 |
| Bois de El Burgo (4) ⚠️ | El Burgo › Sierra de las Nieves | 8 |
| Bois de Istán (12) ⚠️ | Istán › Sierra de las Nieves | 8 |
| Bois de Ronda (16) ⚠️ | Ronda › Serranía de Ronda | 8 |
| Parque Forestal El Lagarillo Blanco ⚠️ | Málaga › Málaga-Costa del Sol | 8 |
| Forêt de Canillas de Albaida (21) ⚠️ | Canillas de Albaida › La Axarquía | 8 |
| Forêt de Coín (20) ⚠️ | Coín › Valle del Guadalhorce | 8 |
| Forêt de Villanueva del Trabuco (27) ⚠️ | Villanueva del Trabuco › Nororma | 8 |
| Forêt de Arenas (7) ⚠️ | Arenas › La Axarquía | 8 |
| Forêt de Mijas (139) ⚠️ | Mijas › Costa del Sol Occidental | 7 |
| Forêt de Alhaurín el Grande (7) ⚠️ | Alhaurín el Grande › Valle del Guadalhorce | 7 |
| Forêt de Torremolinos ⚠️ | Torremolinos › Costa del Sol Occidental | 7 |
| Forêt de Viñuela (3) ⚠️ | Viñuela › La Axarquía | 7 |
| Forêt de Comares (4) ⚠️ | Comares › La Axarquía | 7 |
| Forêt de Yunquera (6) ⚠️ | Yunquera › Sierra de las Nieves | 7 |
| Forêt de Alozaina (4) ⚠️ | Alozaina › Sierra de las Nieves | 7 |
| Bois de Villanueva del Trabuco (9) ⚠️ | Villanueva del Trabuco › Nororma | 7 |
| Forêt de Salares (13) ⚠️ | Salares › La Axarquía | 7 |
| Forêt de Tolox (82) ⚠️ | Tolox › Sierra de las Nieves | 7 |
| Bois de Yunquera (5) ⚠️ | Yunquera › Sierra de las Nieves | 7 |
| Bois de Tolox (84) ⚠️ | Tolox › Sierra de las Nieves | 7 |
| Bois de Yunquera (27) ⚠️ | Yunquera › Sierra de las Nieves | 7 |
| Bois de El Burgo (10) ⚠️ | El Burgo › Sierra de las Nieves | 7 |
| Bois de Istán (48) ⚠️ | Istán › Sierra de las Nieves | 7 |
| Forêt de Canillas de Albaida (18) ⚠️ | Canillas de Albaida › La Axarquía | 7 |
| Forêt de Marbella (25) ⚠️ | Marbella › Costa del Sol Occidental | 7 |
| Forêt de Ojén (79) ⚠️ | Ojén › Sierra de las Nieves | 7 |
| Forêt de Coín (15) ⚠️ | Coín › Valle del Guadalhorce | 7 |
| Bois de Antequera (23) ⚠️ | Antequera › Antequera | 7 |
| Bois de Antequera (27) ⚠️ | Antequera › Antequera | 7 |
| Bois de Alfarnatejo (4) ⚠️ | Alfarnatejo › La Axarquía | 7 |
| Bois de Álora (2) ⚠️ | Álora › Valle del Guadalhorce | 7 |
| Bois de Frigiliana (5) ⚠️ | Frigiliana › La Axarquía | 7 |
| Bois de Mijas (101) ⚠️ | Mijas › Costa del Sol Occidental | 7 |
| Bois de Ojén (10) ⚠️ | Marbella › Costa del Sol Occidental | 7 |
| Bois de Álora (108) ⚠️ | Álora › Valle del Guadalhorce | 7 |
| Forêt de Marbella (6) ⚠️ | Marbella › Costa del Sol Occidental | 6 |
| Forêt de Alhaurín el Grande (13) ⚠️ | Alhaurín el Grande › Valle del Guadalhorce | 6 |
| Forêt de Alhaurín el Grande (24) ⚠️ | Alhaurín el Grande › Valle del Guadalhorce | 6 |
| Forêt de Mijas (366) ⚠️ | Mijas › Costa del Sol Occidental | 6 |
| Forêt de Vélez-Málaga (108) ⚠️ | Vélez-Málaga › La Axarquía | 6 |
| Forêt de Vélez-Málaga (155) ⚠️ | Vélez-Málaga › La Axarquía | 6 |
| Bois de Málaga (58) ⚠️ | Málaga › Málaga-Costa del Sol | 6 |
| Forêt de Canillas de Aceituno (4) ⚠️ | Canillas de Aceituno › La Axarquía | 6 |
| Bois de Ronda (2) ⚠️ | Ronda › Serranía de Ronda | 6 |
| Forêt de Tolox (44) ⚠️ | Tolox › Sierra de las Nieves | 6 |
| Forêt de Tolox (58) ⚠️ | Tolox › Sierra de las Nieves | 6 |
| Forêt de Tolox (76) ⚠️ | Tolox › Sierra de las Nieves | 6 |
| Forêt de Tolox (81) ⚠️ | Tolox › Sierra de las Nieves | 6 |
| Bois de Istán (8) ⚠️ | Istán › Sierra de las Nieves | 6 |
| Bois de Tolox (35) ⚠️ | Tolox › Sierra de las Nieves | 6 |
| Bois de Tolox (55) ⚠️ | Tolox › Sierra de las Nieves | 6 |
| Bois de Istán (16) ⚠️ | Istán › Sierra de las Nieves | 6 |
| Bois de Tolox (81) ⚠️ | Tolox › Sierra de las Nieves | 6 |
| Bois de Istán (31) ⚠️ | Istán › Sierra de las Nieves | 6 |
| Bois de Yunquera (39) ⚠️ | Yunquera › Sierra de las Nieves | 6 |
| Bois de El Burgo (19) ⚠️ | El Burgo › Sierra de las Nieves | 6 |
| Bois de Monda (38) ⚠️ | Monda › Sierra de las Nieves | 6 |
| Bois de Igualeja (2) ⚠️ | Igualeja › Serranía de Ronda | 6 |
| Bois de Ronda (21) ⚠️ | Ronda › Serranía de Ronda | 6 |
| Bois de Ronda (22) ⚠️ | Ronda › Serranía de Ronda | 6 |
| Bois de Alfarnate ⚠️ | Alfarnate › La Axarquía | 6 |
| Forêt de Canillas de Albaida (17) ⚠️ | Canillas de Albaida › La Axarquía | 6 |
| Bois de Málaga (193) ⚠️ | Málaga › Málaga-Costa del Sol | 6 |
| Forêt de Humilladero (3) ⚠️ | Humilladero › Antequera | 6 |
| Forêt de Humilladero (6) ⚠️ | Humilladero › Antequera | 6 |
| Forêt de Marbella (24) ⚠️ | Marbella › Costa del Sol Occidental | 6 |
| Forêt de Ojén (80) ⚠️ | Ojén › Sierra de las Nieves | 6 |
| Forêt de Marbella (30) ⚠️ | Marbella › Costa del Sol Occidental | 6 |
| Bois de Colmenar ⚠️ | Colmenar › La Axarquía | 6 |
| Bois de Antequera (20) ⚠️ | Antequera › Antequera | 6 |
| Forêt de Mijas (424) ⚠️ | Mijas › Costa del Sol Occidental | 6 |
| Bois de Frigiliana (3) ⚠️ | Frigiliana › La Axarquía | 6 |
| Bois de Frigiliana (9) ⚠️ | Frigiliana › La Axarquía | 6 |
| Bois de Frigiliana (13) ⚠️ | Frigiliana › La Axarquía | 6 |
| Forêt de Álora (4) ⚠️ | Álora › Valle del Guadalhorce | 6 |
| Forêt de Alhaurín el Grande (20) ⚠️ | Alhaurín el Grande › Valle del Guadalhorce | 5 |
| Forêt de Alhaurín el Grande (34) ⚠️ | Alhaurín el Grande › Valle del Guadalhorce | 5 |
| Forêt de Alhaurín el Grande (35) ⚠️ | Alhaurín el Grande › Valle del Guadalhorce | 5 |
| Bois de Málaga (16) ⚠️ | Málaga › Málaga-Costa del Sol | 5 |
| Forêt de Viñuela (19) ⚠️ | Viñuela › La Axarquía | 5 |
| Forêt de Viñuela (20) ⚠️ | Viñuela › La Axarquía | 5 |
| Forêt de Tolox (3) ⚠️ | Tolox › Sierra de las Nieves | 5 |
| Forêt de Tolox (9) ⚠️ | Tolox › Sierra de las Nieves | 5 |
| Forêt de Yunquera (7) ⚠️ | Yunquera › Sierra de las Nieves | 5 |
| Forêt de Tolox (22) ⚠️ | Tolox › Sierra de las Nieves | 5 |
| Forêt de Monda (3) ⚠️ | Monda › Sierra de las Nieves | 5 |
| Nagüeles ⚠️ | Marbella › Costa del Sol Occidental | 5 |
| Forêt de Salares (3) ⚠️ | Salares › La Axarquía | 5 |
| Forêt de Sedella ⚠️ | Sedella › La Axarquía | 5 |
| Forêt de Ojén (55) ⚠️ | Ojén › Sierra de las Nieves | 5 |
| Forêt de Tolox (55) ⚠️ | Tolox › Sierra de las Nieves | 5 |
| Bois de Tolox (5) ⚠️ | Tolox › Sierra de las Nieves | 5 |
| Bois de Yunquera (13) ⚠️ | Yunquera › Sierra de las Nieves | 5 |
| Bois de Yunquera (26) ⚠️ | Yunquera › Sierra de las Nieves | 5 |
| Bois de Ronda (18) ⚠️ | Ronda › Serranía de Ronda | 5 |
| Bois de Istán (43) ⚠️ | Istán › Sierra de las Nieves | 5 |
| Bois de Istán (44) ⚠️ | Istán › Sierra de las Nieves | 5 |
| Bois de Yunquera (46) ⚠️ | Yunquera › Sierra de las Nieves | 5 |
| Forêt de Alfarnatejo (3) ⚠️ | Alfarnatejo › La Axarquía | 5 |
| Bois de Málaga (191) ⚠️ | Málaga › Málaga-Costa del Sol | 5 |
| Forêt de Ojén (61) ⚠️ | Ojén › Sierra de las Nieves | 5 |
| Forêt de Monda (16) ⚠️ | Monda › Sierra de las Nieves | 5 |
| Forêt de Ojén (87) ⚠️ | Ojén › Sierra de las Nieves | 5 |
| Forêt de Villanueva del Rosario (4) ⚠️ | Villanueva del Rosario › Nororma | 5 |
| Forêt de Villanueva del Rosario (6) ⚠️ | Villanueva del Rosario › Nororma | 5 |
| Parque Forestal Hacienda Clavero ⚠️ | Málaga › Málaga-Costa del Sol | 5 |
| Bois de Antequera (8) ⚠️ | Antequera › Antequera | 5 |
| Bois de Colmenar (6) ⚠️ | Colmenar › La Axarquía | 5 |
| Bois de Riogordo (5) ⚠️ | Riogordo › La Axarquía | 5 |
| Forêt de Nerja (12) ⚠️ | Nerja › La Axarquía | 5 |
| Bois de Málaga (575) ⚠️ | Málaga › Málaga-Costa del Sol | 5 |
| Bois de Frigiliana ⚠️ | Frigiliana › La Axarquía | 5 |
| Bois de Frigiliana (10) ⚠️ | Frigiliana › La Axarquía | 5 |
| Bois de Riogordo (6) ⚠️ | Riogordo › La Axarquía | 5 |
| Bois de Málaga (717) ⚠️ | Málaga › Málaga-Costa del Sol | 5 |
| Parque Arquitecta María Eugenia Candau ⚠️ | Málaga › Málaga-Costa del Sol | 4 |
| Forêt de Marbella (3) ⚠️ | Marbella › Costa del Sol Occidental | 4 |
| Parque del Norte ⚠️ | Málaga › Málaga-Costa del Sol | 4 |
| Forêt de Alhaurín el Grande (23) ⚠️ | Alhaurín el Grande › Valle del Guadalhorce | 4 |
| Forêt de Alhaurín el Grande (28) ⚠️ | Alhaurín el Grande › Valle del Guadalhorce | 4 |
| Forêt de Alhaurín el Grande (32) ⚠️ | Alhaurín el Grande › Valle del Guadalhorce | 4 |
| Forêt de Alhaurín el Grande (36) ⚠️ | Alhaurín el Grande › Valle del Guadalhorce | 4 |
| Parque Forestal Los Tres Jardines ⚠️ | Marbella › Costa del Sol Occidental | 4 |
| Forêt de Antequera (13) ⚠️ | Antequera › Antequera | 4 |
| Forêt de Alhaurín el Grande (47) ⚠️ | Alhaurín el Grande › Valle del Guadalhorce | 4 |
| Forêt de Viñuela (7) ⚠️ | Viñuela › La Axarquía | 4 |
| Forêt de Viñuela (18) ⚠️ | Viñuela › La Axarquía | 4 |
| Forêt de Tolox (12) ⚠️ | Tolox › Sierra de las Nieves | 4 |
| Forêt de Tolox (13) ⚠️ | Tolox › Sierra de las Nieves | 4 |
| Forêt de Tolox (23) ⚠️ | Tolox › Sierra de las Nieves | 4 |
| Forêt de Tolox (24) ⚠️ | Tolox › Sierra de las Nieves | 4 |
| Forêt de Tolox (26) ⚠️ | Tolox › Sierra de las Nieves | 4 |
| Forêt de Monda ⚠️ | Monda › Sierra de las Nieves | 4 |
| Forêt de Marbella (19) ⚠️ | Marbella › Costa del Sol Occidental | 4 |
| Bois de Málaga (56) ⚠️ | Málaga › Málaga-Costa del Sol | 4 |
| Forêt de Canillas de Albaida (7) ⚠️ | Canillas de Albaida › La Axarquía | 4 |
| Forêt de Ojén (51) ⚠️ | Ojén › Sierra de las Nieves | 4 |
| Forêt de Ojén (54) ⚠️ | Ojén › Sierra de las Nieves | 4 |
| Bois de Tolox (2) ⚠️ | Tolox › Sierra de las Nieves | 4 |
| Forêt de Tolox (46) ⚠️ | Tolox › Sierra de las Nieves | 4 |
| Forêt de Tolox (77) ⚠️ | Tolox › Sierra de las Nieves | 4 |
| Forêt de Tolox (80) ⚠️ | Tolox › Sierra de las Nieves | 4 |
| Bois de Tolox (28) ⚠️ | Tolox › Sierra de las Nieves | 4 |
| Bois de Ojén (2) ⚠️ | Ojén › Sierra de las Nieves | 4 |
| Bois de Ojén (3) ⚠️ | Ojén › Sierra de las Nieves | 4 |
| Bois de Ronda (8) ⚠️ | Ronda › Serranía de Ronda | 4 |
| Bois de El Burgo (2) ⚠️ | El Burgo › Sierra de las Nieves | 4 |
| Bois de Málaga (120) ⚠️ | Málaga › Málaga-Costa del Sol | 4 |
| Bois de Málaga (121) ⚠️ | Málaga › Málaga-Costa del Sol | 4 |
| Bois de Tolox (47) ⚠️ | Tolox › Sierra de las Nieves | 4 |
| Bois de Alozaina ⚠️ | Tolox › Sierra de las Nieves | 4 |
| Bois de Yunquera (15) ⚠️ | Yunquera › Sierra de las Nieves | 4 |
| Bois de Monda (17) ⚠️ | Monda › Sierra de las Nieves | 4 |
| Bois de Yunquera (18) ⚠️ | Yunquera › Sierra de las Nieves | 4 |
| Bois de El Burgo (18) ⚠️ | El Burgo › Sierra de las Nieves | 4 |
| Bois de Ojén (4) ⚠️ | Ojén › Sierra de las Nieves | 4 |
| Bois de El Burgo (20) ⚠️ | El Burgo › Sierra de las Nieves | 4 |
| Forêt de Alfarnate (4) ⚠️ | Alfarnate › La Axarquía | 4 |
| Bois de Alfarnate (5) ⚠️ | Alfarnate › La Axarquía | 4 |
| Bois de Periana (2) ⚠️ | Periana › La Axarquía | 4 |
| Forêt de Viñuela (64) ⚠️ | Viñuela › La Axarquía | 4 |
| Bois de Málaga (239) ⚠️ | Málaga › Málaga-Costa del Sol | 4 |
| Forêt de Humilladero (4) ⚠️ | Humilladero › Antequera | 4 |
| Forêt de Antequera (31) ⚠️ | Antequera › Antequera | 4 |
| Forêt de Antequera (41) ⚠️ | Antequera › Antequera | 4 |
| Forêt de Ojén (63) ⚠️ | Ojén › Sierra de las Nieves | 4 |
| Forêt de Coín (5) ⚠️ | Coín › Valle del Guadalhorce | 4 |
| Forêt de Istán (6) ⚠️ | Istán › Sierra de las Nieves | 4 |
| Forêt de Monda (24) ⚠️ | Monda › Sierra de las Nieves | 4 |
| Forêt de Ojén (82) ⚠️ | Ojén › Sierra de las Nieves | 4 |
| Forêt de Ojén (83) ⚠️ | Ojén › Sierra de las Nieves | 4 |
| Bois de Málaga (387) ⚠️ | Málaga › Málaga-Costa del Sol | 4 |
| Forêt de Villanueva del Rosario (9) ⚠️ | Villanueva del Rosario › Nororma | 4 |
| Bois de Villanueva del Rosario ⚠️ | Villanueva del Rosario › Nororma | 4 |
| Bois de Antequera (10) ⚠️ | Antequera › Antequera | 4 |
| Bois de Antequera (22) ⚠️ | Antequera › Antequera | 4 |
| Bois de Villanueva del Rosario (6) ⚠️ | Villanueva del Rosario › Nororma | 4 |
| Bois de Riogordo (4) ⚠️ | Riogordo › La Axarquía | 4 |
| Bois de Álora ⚠️ | Álora › Valle del Guadalhorce | 4 |
| Bois de Comares (3) ⚠️ | Comares › La Axarquía | 4 |
| Bois de Teba ⚠️ | Teba › Guadalteba | 4 |
| Forêt de Marbella (53) ⚠️ | Marbella › Costa del Sol Occidental | 4 |
| Bois de Málaga (631) ⚠️ | Málaga › Málaga-Costa del Sol | 4 |
| Bois de Frigiliana (4) ⚠️ | Frigiliana › La Axarquía | 4 |
| Bois de Antequera (39) ⚠️ | Antequera › Antequera | 4 |
| Bois de Málaga (701) ⚠️ | Málaga › Málaga-Costa del Sol | 4 |
| Bois de Ardales (2) ⚠️ | Ardales › Guadalteba | 4 |
| Bois de Benahavís (21) ⚠️ | Benahavís › Costa del Sol Occidental | 4 |
| Forêt de Marbella (54) ⚠️ | Marbella › Costa del Sol Occidental | 4 |
| Parc de Málaga (249) ⚠️ | Málaga › Málaga-Costa del Sol | 4 |
| Forêt de Tolox (87) ⚠️ | Tolox › Sierra de las Nieves | 4 |
| Parque de la Paloma ⚠️ | Benalmádena › Costa del Sol Occidental | 3 |
| Parque Botanico El Cerezal ⚠️ | Ojén › Sierra de las Nieves | 3 |
| Forêt de Marbella (10) ⚠️ | Marbella › Costa del Sol Occidental | 3 |
| Forêt de Mijas (149) ⚠️ | Mijas › Costa del Sol Occidental | 3 |
| Forêt de Mijas (187) ⚠️ | Mijas › Costa del Sol Occidental | 3 |
| Forêt de Alhaurín el Grande (39) ⚠️ | Alhaurín el Grande › Valle del Guadalhorce | 3 |
| Forêt de Mijas (353) ⚠️ | Mijas › Costa del Sol Occidental | 3 |
| Forêt de Ronda ⚠️ | Ronda › Serranía de Ronda | 3 |
| Forêt de Ronda (3) ⚠️ | Ronda › Serranía de Ronda | 3 |
| Forêt de Ronda (4) ⚠️ | Ronda › Serranía de Ronda | 3 |
| Forêt de Antequera (10) ⚠️ | Antequera › Antequera | 3 |
| Parque Forestal Andrés Jiménez Díaz ⚠️ | Málaga › Málaga-Costa del Sol | 3 |
| Forêt de Villanueva del Trabuco ⚠️ | Villanueva del Trabuco › Nororma | 3 |
| Forêt de Vélez-Málaga (46) ⚠️ | Vélez-Málaga › La Axarquía | 3 |
| Forêt de Mijas (364) ⚠️ | Mijas › Costa del Sol Occidental | 3 |
| Forêt de Mijas (368) ⚠️ | Mijas › Costa del Sol Occidental | 3 |
| Forêt de Villanueva del Trabuco (10) ⚠️ | Villanueva del Trabuco › Nororma | 3 |
| Forêt de Periana (13) ⚠️ | Periana › La Axarquía | 3 |
| Forêt de Periana (15) ⚠️ | Periana › La Axarquía | 3 |
| Forêt de Viñuela (27) ⚠️ | Viñuela › La Axarquía | 3 |
| Forêt de Comares (6) ⚠️ | Comares › La Axarquía | 3 |
| Forêt de El Borge (3) ⚠️ | El Borge › La Axarquía | 3 |
| Forêt de Vélez-Málaga (223) ⚠️ | Vélez-Málaga › La Axarquía | 3 |
| Bois de Marbella (25) ⚠️ | Marbella › Costa del Sol Occidental | 3 |
| Bois de Marbella (51) ⚠️ | Marbella › Costa del Sol Occidental | 3 |
| Bois de Marbella (73) ⚠️ | Marbella › Costa del Sol Occidental | 3 |
| Bois de Mijas (34) ⚠️ | Mijas › Costa del Sol Occidental | 3 |
| Bois de Mijas (35) ⚠️ | Mijas › Costa del Sol Occidental | 3 |
| Forêt de Tolox (19) ⚠️ | Tolox › Sierra de las Nieves | 3 |
| Forêt de Tolox (27) ⚠️ | Tolox › Sierra de las Nieves | 3 |
| Forêt de Tolox (29) ⚠️ | Tolox › Sierra de las Nieves | 3 |
| Forêt de Yunquera (11) ⚠️ | Yunquera › Sierra de las Nieves | 3 |
| Forêt de Igualeja ⚠️ | Igualeja › Serranía de Ronda | 3 |
| Forêt de Canillas de Albaida (5) ⚠️ | Canillas de Albaida › La Axarquía | 3 |
| Forêt de Sedella (3) ⚠️ | Sedella › La Axarquía | 3 |
| Forêt de Salares (10) ⚠️ | Salares › La Axarquía | 3 |
| Forêt de Sedella (10) ⚠️ | Sedella › La Axarquía | 3 |
| Forêt de Ojén (53) ⚠️ | Ojén › Sierra de las Nieves | 3 |
| Forêt de Tolox (61) ⚠️ | Tolox › Sierra de las Nieves | 3 |
| Bois de Tolox (10) ⚠️ | Tolox › Sierra de las Nieves | 3 |
| Bois de Istán (4) ⚠️ | Istán › Sierra de las Nieves | 3 |
| Bois de El Burgo (3) ⚠️ | El Burgo › Sierra de las Nieves | 3 |
| Bois de Tolox (36) ⚠️ | Tolox › Sierra de las Nieves | 3 |
| Bois de Yunquera ⚠️ | Yunquera › Sierra de las Nieves | 3 |
| Bois de Ronda (12) ⚠️ | Ronda › Serranía de Ronda | 3 |
| Bois de Tolox (69) ⚠️ | Tolox › Sierra de las Nieves | 3 |
| Bois de Yunquera (9) ⚠️ | Yunquera › Sierra de las Nieves | 3 |
| Bois de Istán (14) ⚠️ | Istán › Sierra de las Nieves | 3 |
| Bois de Monda (9) ⚠️ | Monda › Sierra de las Nieves | 3 |
| Bois de Monda (20) ⚠️ | Monda › Sierra de las Nieves | 3 |
| Bois de Monda (26) ⚠️ | Monda › Sierra de las Nieves | 3 |
| Bois de Tolox (83) ⚠️ | Tolox › Sierra de las Nieves | 3 |
| Bois de Tolox (88) ⚠️ | Tolox › Sierra de las Nieves | 3 |
| Bois de Guaro (2) ⚠️ | Guaro › Sierra de las Nieves | 3 |
| Bois de Istán (24) ⚠️ | Istán › Sierra de las Nieves | 3 |
| Bois de Yunquera (29) ⚠️ | Yunquera › Sierra de las Nieves | 3 |
| Bois de El Burgo (11) ⚠️ | El Burgo › Sierra de las Nieves | 3 |
| Bois de El Burgo (14) ⚠️ | El Burgo › Sierra de las Nieves | 3 |
| Bois de El Burgo (15) ⚠️ | El Burgo › Sierra de las Nieves | 3 |
| Bois de El Burgo (17) ⚠️ | El Burgo › Sierra de las Nieves | 3 |
| Bois de Istán (39) ⚠️ | Istán › Sierra de las Nieves | 3 |
| Bois de Istán (49) ⚠️ | Istán › Sierra de las Nieves | 3 |
| Bois de Ojén (6) ⚠️ | Ojén › Sierra de las Nieves | 3 |
| Bois de Parauta (14) ⚠️ | Parauta › Serranía de Ronda | 3 |
| Bois de Parauta (16) ⚠️ | Parauta › Serranía de Ronda | 3 |
| Forêt de Viñuela (67) ⚠️ | Viñuela › La Axarquía | 3 |
| Forêt de Canillas de Albaida (15) ⚠️ | Canillas de Albaida › La Axarquía | 3 |
| Forêt de Periana (27) ⚠️ | Periana › La Axarquía | 3 |
| Bois de Málaga (186) ⚠️ | Málaga › Málaga-Costa del Sol | 3 |
| Bois de Málaga (199) ⚠️ | Málaga › Málaga-Costa del Sol | 3 |
| Bois de Málaga (240) ⚠️ | Málaga › Málaga-Costa del Sol | 3 |
| Forêt de Antequera (17) ⚠️ | Antequera › Antequera | 3 |
| Forêt de Antequera (23) ⚠️ | Antequera › Antequera | 3 |
| Forêt de Ojén (69) ⚠️ | Ojén › Sierra de las Nieves | 3 |
| Forêt de Ojén (75) ⚠️ | Ojén › Sierra de las Nieves | 3 |
| Ribera río Genil La Aceña ⚠️ | Cuevas de San Marcos › Nororma | 3 |
| Forêt de Ojén (78) ⚠️ | Ojén › Sierra de las Nieves | 3 |
| Forêt de Monda (22) ⚠️ | Monda › Sierra de las Nieves | 3 |
| Forêt de Coín (16) ⚠️ | Coín › Valle del Guadalhorce | 3 |
| Forêt de Coín (19) ⚠️ | Coín › Valle del Guadalhorce | 3 |
| Forêt de Marbella (29) ⚠️ | Marbella › Costa del Sol Occidental | 3 |
| Forêt de Monda (28) ⚠️ | Monda › Sierra de las Nieves | 3 |
| Forêt de Coín (22) ⚠️ | Coín › Valle del Guadalhorce | 3 |
| Bois de Antequera (26) ⚠️ | Antequera › Antequera | 3 |
| Bois de Alcaucín (4) ⚠️ | Alcaucín › La Axarquía | 3 |
| Forêt de Marbella (49) ⚠️ | Marbella › Costa del Sol Occidental | 3 |
| Forêt de Mijas (372) ⚠️ | Mijas › Costa del Sol Occidental | 3 |
| Bois de Málaga (560) ⚠️ | Málaga › Málaga-Costa del Sol | 3 |
| Bois de Málaga (564) ⚠️ | Málaga › Málaga-Costa del Sol | 3 |
| Forêt de Arenas (8) ⚠️ | Arenas › La Axarquía | 3 |
| Forêt de Arenas (9) ⚠️ | Arenas › La Axarquía | 3 |
| Bois de Málaga (653) ⚠️ | Málaga › Málaga-Costa del Sol | 3 |
| Bois de Frigiliana (2) ⚠️ | Frigiliana › La Axarquía | 3 |
| Bois de Nerja (11) ⚠️ | Nerja › La Axarquía | 3 |
| Forêt de Ronda (13) ⚠️ | Ronda › Serranía de Ronda | 3 |
| Bois de Benahavís (5) ⚠️ | Benahavís › Costa del Sol Occidental | 3 |
| Bois de Benahavís (6) ⚠️ | Benahavís › Costa del Sol Occidental | 3 |
| Bois de Benahavís (25) ⚠️ | Benahavís › Costa del Sol Occidental | 3 |
| Bois de Montejaque (4) ⚠️ | Montejaque › Serranía de Ronda | 3 |
| Bois de Ojén (9) ⚠️ | Ojén › Sierra de las Nieves | 3 |
| Parc de Málaga (255) ⚠️ | Málaga › Málaga-Costa del Sol | 3 |
| Parque de Huelin ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Parc de Vélez-Málaga ⚠️ | Vélez-Málaga › La Axarquía | 2 |
| Pinar Molino del Moro ⚠️ | Torremolinos › Costa del Sol Occidental | 2 |
| Parque del Oeste ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Parque La Batería ⚠️ | Torremolinos › Costa del Sol Occidental | 2 |
| Forêt de Marbella (2) ⚠️ | Marbella › Costa del Sol Occidental | 2 |
| Parque Litoral ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Forêt de Ojén (41) ⚠️ | Ojén › Sierra de las Nieves | 2 |
| Forêt de Mijas (44) ⚠️ | Mijas › Costa del Sol Occidental | 2 |
| Forêt de Mijas (76) ⚠️ | Mijas › Costa del Sol Occidental | 2 |
| Forêt de Alhaurín el Grande (5) ⚠️ | Alhaurín el Grande › Valle del Guadalhorce | 2 |
| Forêt de Alhaurín el Grande (11) ⚠️ | Alhaurín el Grande › Valle del Guadalhorce | 2 |
| Forêt de Alhaurín el Grande (22) ⚠️ | Alhaurín el Grande › Valle del Guadalhorce | 2 |
| Forêt de Alhaurín el Grande (43) ⚠️ | Alhaurín el Grande › Valle del Guadalhorce | 2 |
| Palmeral de las Sorpresas ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Parque San Miguel ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Parque de Santa Ana ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Forêt de Marbella (11) ⚠️ | Marbella › Costa del Sol Occidental | 2 |
| Forêt de Ronda (2) ⚠️ | Ronda › Serranía de Ronda | 2 |
| Tholos de El Romeral ⚠️ | Antequera › Antequera | 2 |
| Parque de la Memoria ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Forêt de Villanueva del Trabuco (2) ⚠️ | Villanueva del Trabuco › Nororma | 2 |
| Forêt de Villanueva del Trabuco (7) ⚠️ | Villanueva del Trabuco › Nororma | 2 |
| Forêt de Villanueva del Trabuco (8) ⚠️ | Villanueva del Trabuco › Nororma | 2 |
| Forêt de Vélez-Málaga (4) ⚠️ | Vélez-Málaga › La Axarquía | 2 |
| Forêt de Mijas (360) ⚠️ | Mijas › Costa del Sol Occidental | 2 |
| La Meca ⚠️ | Mijas › Costa del Sol Occidental | 2 |
| Forêt de Vélez-Málaga (12) ⚠️ | Vélez-Málaga › La Axarquía | 2 |
| Forêt de Vélez-Málaga (33) ⚠️ | Vélez-Málaga › La Axarquía | 2 |
| Forêt de Vélez-Málaga (36) ⚠️ | Vélez-Málaga › La Axarquía | 2 |
| Vigil de Quiñones ⚠️ | Marbella › Costa del Sol Occidental | 2 |
| Forêt de Mijas (365) ⚠️ | Mijas › Costa del Sol Occidental | 2 |
| Forêt de Viñuela (2) ⚠️ | Viñuela › La Axarquía | 2 |
| Forêt de Viñuela (5) ⚠️ | Viñuela › La Axarquía | 2 |
| Forêt de Viñuela (6) ⚠️ | Viñuela › La Axarquía | 2 |
| Forêt de Viñuela (8) ⚠️ | Viñuela › La Axarquía | 2 |
| Forêt de Periana (17) ⚠️ | Periana › La Axarquía | 2 |
| Forêt de Viñuela (25) ⚠️ | Viñuela › La Axarquía | 2 |
| Forêt de Viñuela (31) ⚠️ | Viñuela › La Axarquía | 2 |
| Forêt de Viñuela (33) ⚠️ | Alcaucín › La Axarquía | 2 |
| Forêt de Viñuela (44) ⚠️ | Viñuela › La Axarquía | 2 |
| Forêt de Vélez-Málaga (89) ⚠️ | Vélez-Málaga › La Axarquía | 2 |
| Forêt de Vélez-Málaga (112) ⚠️ | Vélez-Málaga › La Axarquía | 2 |
| Forêt de Rincón de la Victoria (2) ⚠️ | Rincón de la Victoria › La Axarquía | 2 |
| Forêt de Vélez-Málaga (150) ⚠️ | Vélez-Málaga › La Axarquía | 2 |
| Forêt de Almáchar (3) ⚠️ | Almáchar › La Axarquía | 2 |
| Hoya de Las Cabras ⚠️ | Rincón de la Victoria › La Axarquía | 2 |
| Forêt de Rincón de la Victoria (12) ⚠️ | Rincón de la Victoria › La Axarquía | 2 |
| Bois de Marbella (3) ⚠️ | Marbella › Costa del Sol Occidental | 2 |
| Forêt de Vélez-Málaga (248) ⚠️ | Vélez-Málaga › La Axarquía | 2 |
| Forêt de Vélez-Málaga (252) ⚠️ | Vélez-Málaga › La Axarquía | 2 |
| Parque natural ⚠️ | Fuengirola › Costa del Sol Occidental | 2 |
| Forêt de Rincón de la Victoria (38) ⚠️ | Rincón de la Victoria › La Axarquía | 2 |
| Bois de Marbella (18) ⚠️ | Marbella › Costa del Sol Occidental | 2 |
| Bois de Marbella (30) ⚠️ | Marbella › Costa del Sol Occidental | 2 |
| Bois de Ojén ⚠️ | Ojén › Sierra de las Nieves | 2 |
| Parc de Marbella (57) ⚠️ | Marbella › Costa del Sol Occidental | 2 |
| Bois de Marbella (48) ⚠️ | Marbella › Costa del Sol Occidental | 2 |
| Forêt de Marbella (18) ⚠️ | Marbella › Costa del Sol Occidental | 2 |
| Parque de los Niños ⚠️ | Estepona › Costa del Sol Occidental | 2 |
| Bois de Cártama (3) ⚠️ | Cártama › Valle del Guadalhorce | 2 |
| Bois de Málaga (32) ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Parc de Alhaurín de la Torre (21) ⚠️ | Alhaurín de la Torre › Valle del Guadalhorce | 2 |
| Bois de Mijas (33) ⚠️ | Mijas › Costa del Sol Occidental | 2 |
| Parque Atalaya ⚠️ | Antequera › Antequera | 2 |
| Bois de Málaga (41) ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Pinar Baños ⚠️ | Estepona › Costa del Sol Occidental | 2 |
| Bois de Mijas (39) ⚠️ | Mijas › Costa del Sol Occidental | 2 |
| Forêt de Tolox (11) ⚠️ | Tolox › Sierra de las Nieves | 2 |
| Forêt de Yunquera (8) ⚠️ | Yunquera › Sierra de las Nieves | 2 |
| Forêt de Tolox (15) ⚠️ | Tolox › Sierra de las Nieves | 2 |
| Forêt de Alozaina (2) ⚠️ | Alozaina › Sierra de las Nieves | 2 |
| Bois de Mijas (54) ⚠️ | Mijas › Costa del Sol Occidental | 2 |
| Forêt de Guaro ⚠️ | Guaro › Sierra de las Nieves | 2 |
| Bois de Mijas (57) ⚠️ | Mijas › Costa del Sol Occidental | 2 |
| Parque Fluvial Rio Fuengirola (3) ⚠️ | Fuengirola › Costa del Sol Occidental | 2 |
| Bois de Málaga (51) ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Forêt de Benahavís (3) ⚠️ | Benahavís › Costa del Sol Occidental | 2 |
| Bois de Málaga (59) ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Forêt de Villanueva del Trabuco (18) ⚠️ | Villanueva del Trabuco › Nororma | 2 |
| Bois de Villanueva del Trabuco (3) ⚠️ | Villanueva del Trabuco › Nororma | 2 |
| Bois de Málaga (74) ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Forêt de Salares (2) ⚠️ | Salares › La Axarquía | 2 |
| Forêt de Sedella (2) ⚠️ | Sedella › La Axarquía | 2 |
| Forêt de Canillas de Albaida (10) ⚠️ | Canillas de Albaida › La Axarquía | 2 |
| Forêt de Salares (9) ⚠️ | Salares › La Axarquía | 2 |
| Forêt de Sedella (4) ⚠️ | Sedella › La Axarquía | 2 |
| Forêt de Salares (12) ⚠️ | Salares › La Axarquía | 2 |
| Forêt de Sedella (7) ⚠️ | Sedella › La Axarquía | 2 |
| Forêt de Sedella (8) ⚠️ | Sedella › La Axarquía | 2 |
| Forêt de Ojén (52) ⚠️ | Ojén › Sierra de las Nieves | 2 |
| Bois de Málaga (97) ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Bois de Ronda (3) ⚠️ | Ronda › Serranía de Ronda | 2 |
| Bois de Tolox (3) ⚠️ | Tolox › Sierra de las Nieves | 2 |
| Bois de Tolox (4) ⚠️ | Tolox › Sierra de las Nieves | 2 |
| Forêt de Tolox (41) ⚠️ | Tolox › Sierra de las Nieves | 2 |
| Forêt de Tolox (42) ⚠️ | Tolox › Sierra de las Nieves | 2 |
| Forêt de Tolox (51) ⚠️ | Tolox › Sierra de las Nieves | 2 |
| Forêt de Tolox (59) ⚠️ | Tolox › Sierra de las Nieves | 2 |
| Forêt de Tolox (63) ⚠️ | Tolox › Sierra de las Nieves | 2 |
| Forêt de Tolox (65) ⚠️ | Tolox › Sierra de las Nieves | 2 |
| Forêt de Monda (7) ⚠️ | Monda › Sierra de las Nieves | 2 |
| Forêt de Monda (9) ⚠️ | Monda › Sierra de las Nieves | 2 |
| Bois de Tolox (21) ⚠️ | Tolox › Sierra de las Nieves | 2 |
| Bois de Istán (5) ⚠️ | Istán › Sierra de las Nieves | 2 |
| Bois de Ronda (6) ⚠️ | Ronda › Serranía de Ronda | 2 |
| Bois de Ronda (7) ⚠️ | Ronda › Serranía de Ronda | 2 |
| Bois de Ronda (9) ⚠️ | Ronda › Serranía de Ronda | 2 |
| Bois de Málaga (115) ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Bois de Tolox (42) ⚠️ | Tolox › Sierra de las Nieves | 2 |
| Bois de Ronda (13) ⚠️ | Ronda › Serranía de Ronda | 2 |
| Bois de Tolox (59) ⚠️ | Tolox › Sierra de las Nieves | 2 |
| Bois de Tolox (61) ⚠️ | Tolox › Sierra de las Nieves | 2 |
| Bois de Tolox (72) ⚠️ | Tolox › Sierra de las Nieves | 2 |
| Bois de Monda (16) ⚠️ | Monda › Sierra de las Nieves | 2 |
| Bois de Istán (20) ⚠️ | Istán › Sierra de las Nieves | 2 |
| Bois de Istán (23) ⚠️ | Istán › Sierra de las Nieves | 2 |
| Bois de Parauta (3) ⚠️ | Istán › Sierra de las Nieves | 2 |
| Bois de Istán (32) ⚠️ | Istán › Sierra de las Nieves | 2 |
| Bois de Parauta (11) ⚠️ | Parauta › Serranía de Ronda | 2 |
| Bois de Parauta (12) ⚠️ | Parauta › Serranía de Ronda | 2 |
| Bois de Parauta (13) ⚠️ | Parauta › Serranía de Ronda | 2 |
| Bois de Yunquera (40) ⚠️ | Yunquera › Sierra de las Nieves | 2 |
| Bois de Ronda (19) ⚠️ | Ronda › Serranía de Ronda | 2 |
| Bois de Istán (41) ⚠️ | Istán › Sierra de las Nieves | 2 |
| Bois de Benahavís (3) ⚠️ | Benahavís › Costa del Sol Occidental | 2 |
| Bois de Monda (37) ⚠️ | Monda › Sierra de las Nieves | 2 |
| Bois de Monda (44) ⚠️ | Monda › Sierra de las Nieves | 2 |
| Bois de Monda (54) ⚠️ | Monda › Sierra de las Nieves | 2 |
| Bois de Monda (59) ⚠️ | Monda › Sierra de las Nieves | 2 |
| Bois de Monda (61) ⚠️ | Monda › Sierra de las Nieves | 2 |
| Bois de Alozaina (6) ⚠️ | Alozaina › Sierra de las Nieves | 2 |
| Bois de Ronda (23) ⚠️ | Ronda › Serranía de Ronda | 2 |
| Bois de Yunquera (44) ⚠️ | Yunquera › Sierra de las Nieves | 2 |
| Forêt de Alfarnate (6) ⚠️ | Alfarnate › La Axarquía | 2 |
| Forêt de Periana (22) ⚠️ | Periana › La Axarquía | 2 |
| Forêt de Periana (23) ⚠️ | Periana › La Axarquía | 2 |
| Forêt de Alcaucín (14) ⚠️ | Alcaucín › La Axarquía | 2 |
| Bois de Alcaucín (3) ⚠️ | Alcaucín › La Axarquía | 2 |
| Forêt de Viñuela (63) ⚠️ | Viñuela › La Axarquía | 2 |
| Forêt de Vélez-Málaga (255) ⚠️ | Vélez-Málaga › La Axarquía | 2 |
| Bois de Málaga (167) ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Bois de Málaga (176) ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Bois de Tolox (97) ⚠️ | Tolox › Sierra de las Nieves | 2 |
| Forêt de Cómpeta ⚠️ | Cómpeta › La Axarquía | 2 |
| Bois de Canillas de Albaida (3) ⚠️ | Canillas de Albaida › La Axarquía | 2 |
| Parc de Málaga (157) ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Parque 54 ⚠️ | Rincón de la Victoria › La Axarquía | 2 |
| Bois de Málaga (247) ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Bois de Málaga (254) ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Parque Marítimo Terrestre Peñón del Cuervo ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Forêt de Humilladero (2) ⚠️ | Humilladero › Antequera | 2 |
| Forêt de Antequera (30) ⚠️ | Antequera › Antequera | 2 |
| Forêt de Villanueva de la Concepción (2) ⚠️ | Villanueva de la Concepción › Antequera | 2 |
| Parque Torneros ⚠️ | Fuengirola › Costa del Sol Occidental | 2 |
| Bois de Málaga (297) ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Forêt de Istán (2) ⚠️ | Istán › Sierra de las Nieves | 2 |
| Forêt de Ojén (65) ⚠️ | Ojén › Sierra de las Nieves | 2 |
| Forêt de Ojén (67) ⚠️ | Ojén › Sierra de las Nieves | 2 |
| Forêt de Istán (3) ⚠️ | Istán › Sierra de las Nieves | 2 |
| Forêt de Ojén (70) ⚠️ | Ojén › Sierra de las Nieves | 2 |
| Forêt de Ojén (74) ⚠️ | Ojén › Sierra de las Nieves | 2 |
| Parque Atalaya (2) ⚠️ | Antequera › Antequera | 2 |
| Forêt de Ojén (76) ⚠️ | Ojén › Sierra de las Nieves | 2 |
| Forêt de Coín (6) ⚠️ | Coín › Valle del Guadalhorce | 2 |
| Forêt de Monda (17) ⚠️ | Monda › Sierra de las Nieves | 2 |
| Forêt de Coín (9) ⚠️ | Coín › Valle del Guadalhorce | 2 |
| Forêt de Monda (27) ⚠️ | Monda › Sierra de las Nieves | 2 |
| Bois de Málaga (360) ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Bois de Málaga (386) ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Forêt de Ojén (88) ⚠️ | Ojén › Sierra de las Nieves | 2 |
| Forêt de Ojén (90) ⚠️ | Ojén › Sierra de las Nieves | 2 |
| Forêt de Colmenar (11) ⚠️ | Colmenar › La Axarquía | 2 |
| Bois de Antequera (4) ⚠️ | Antequera › Antequera | 2 |
| Bois de Antequera (6) ⚠️ | Antequera › Antequera | 2 |
| Bois de Antequera (21) ⚠️ | Antequera › Antequera | 2 |
| Bois de Colmenar (4) ⚠️ | Colmenar › La Axarquía | 2 |
| Forêt de Colmenar (12) ⚠️ | Colmenar › La Axarquía | 2 |
| Forêt de Marbella (40) ⚠️ | Marbella › Costa del Sol Occidental | 2 |
| Forêt de Marbella (45) ⚠️ | Marbella › Costa del Sol Occidental | 2 |
| Forêt de Marbella (50) ⚠️ | Marbella › Costa del Sol Occidental | 2 |
| Bois de Málaga (434) ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Bois de Málaga (504) ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Bois de Málaga (515) ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Bois de Málaga (521) ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Parc de Benalmádena (17) ⚠️ | Benalmádena › Costa del Sol Occidental | 2 |
| Bois de Málaga (573) ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Parc de Benalmádena (20) ⚠️ | Benalmádena › Costa del Sol Occidental | 2 |
| Forêt de Mijas (419) ⚠️ | Mijas › Costa del Sol Occidental | 2 |
| Bois de Mijas (97) ⚠️ | Mijas › Costa del Sol Occidental | 2 |
| Forêt de Mijas (423) ⚠️ | Mijas › Costa del Sol Occidental | 2 |
| Bois de Nerja ⚠️ | Nerja › La Axarquía | 2 |
| Bois de Nerja (8) ⚠️ | Nerja › La Axarquía | 2 |
| Bois de Nerja (9) ⚠️ | Nerja › La Axarquía | 2 |
| Bois de Málaga (670) ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Bois de Málaga (676) ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Bois de Málaga (690) ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Bois de Málaga (697) ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Bois de Benahavís (22) ⚠️ | Benahavís › Costa del Sol Occidental | 2 |
| Bois de Benahavís (23) ⚠️ | Benahavís › Costa del Sol Occidental | 2 |
| Bois de Benahavís (24) ⚠️ | Benahavís › Costa del Sol Occidental | 2 |
| Bois de Benahavís (26) ⚠️ | Benahavís › Costa del Sol Occidental | 2 |
| Bois de Mijas (102) ⚠️ | Mijas › Costa del Sol Occidental | 2 |
| Bois de Frigiliana (19) ⚠️ | Frigiliana › La Axarquía | 2 |
| Parc de Estepona (30) ⚠️ | Estepona › Costa del Sol Occidental | 2 |
| Parque Virgen de Araceli ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Parque de Málaga ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Jardines Calle Pirandello ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Parc de Málaga (261) ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Bois de Málaga (722) ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Bois de Málaga (726) ⚠️ | Málaga › Málaga-Costa del Sol | 2 |
| Jardines de la Muralla ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Parque Verano Azul ⚠️ | Nerja › La Axarquía | 1 |
| Parque del Calvario ⚠️ | Estepona › Costa del Sol Occidental | 1 |
| Zona verde ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Parc de Marbella ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Parc de Alhaurín de la Torre ⚠️ | Alhaurín de la Torre › Valle del Guadalhorce | 1 |
| Parc de Vélez-Málaga (6) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Parc de Vélez-Málaga (8) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Parc de Algarrobo (2) ⚠️ | Algarrobo › La Axarquía | 1 |
| Parc de Nerja (6) ⚠️ | Nerja › La Axarquía | 1 |
| Parc de Vélez-Málaga (13) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Parque María Zambrano ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Parque Juan Jurado Lorca ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Parc de Vélez-Málaga (25) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Park Rosalia de Castro ⚠️ | Nerja › La Axarquía | 1 |
| Parque del Sol ⚠️ | Fuengirola › Costa del Sol Occidental | 1 |
| Parc de Málaga (10) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parc de Málaga (11) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Jardines Carmen Fernanda ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parc de Málaga (12) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Forêt de Marbella (4) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Forêt de Marbella (5) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Parque Marqués del Duero ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Bois de Málaga (4) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Jardín botánico Santa Fiora ⚠️ | Frigiliana › La Axarquía | 1 |
| Plaza Marqués del Turia ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Plaza de Antonio Banderas ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Parque de la Escalerilla ⚠️ | Algarrobo › La Axarquía | 1 |
| Forêt de Algarrobo ⚠️ | Algarrobo › La Axarquía | 1 |
| Bois de Málaga (5) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (6) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parque del Carmen ⚠️ | Estepona › Costa del Sol Occidental | 1 |
| Forêt de Mijas (13) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Forêt de Mijas (79) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Forêt de Mijas (81) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Forêt de Mijas (93) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Forêt de Mijas (120) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Forêt de Mijas (125) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Forêt de Mijas (147) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Forêt de Mijas (189) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Forêt de Mijas (209) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Forêt de Mijas (224) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Forêt de Mijas (235) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Forêt de Mijas (258) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Forêt de Mijas (308) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Forêt de Mijas (316) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Forêt de Mijas (318) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Forêt de Mijas (326) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Parc de Alhaurín de la Torre (2) ⚠️ | Alhaurín de la Torre › Valle del Guadalhorce | 1 |
| Parc de Alhaurín de la Torre (5) ⚠️ | Alhaurín de la Torre › Valle del Guadalhorce | 1 |
| Forêt de Alhaurín el Grande (2) ⚠️ | Alhaurín el Grande › Valle del Guadalhorce | 1 |
| Forêt de Alhaurín el Grande (4) ⚠️ | Alhaurín el Grande › Valle del Guadalhorce | 1 |
| Forêt de Alhaurín el Grande (6) ⚠️ | Alhaurín el Grande › Valle del Guadalhorce | 1 |
| Forêt de Alhaurín el Grande (15) ⚠️ | Alhaurín el Grande › Valle del Guadalhorce | 1 |
| Forêt de Alhaurín el Grande (17) ⚠️ | Alhaurín el Grande › Valle del Guadalhorce | 1 |
| Forêt de Alhaurín el Grande (19) ⚠️ | Alhaurín el Grande › Valle del Guadalhorce | 1 |
| Forêt de Alhaurín el Grande (21) ⚠️ | Alhaurín el Grande › Valle del Guadalhorce | 1 |
| Forêt de Alhaurín el Grande (26) ⚠️ | Alhaurín el Grande › Valle del Guadalhorce | 1 |
| Forêt de Mijas (355) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Parque P. Antonio Godino ⚠️ | Gaucín › Serranía de Ronda | 1 |
| Jardín Músico Manuel del Campo ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parque de Manuel Navarrete ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parc de Málaga (23) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Forêt de Ojén (49) ⚠️ | Ojén › Sierra de las Nieves | 1 |
| Forêt de Marbella (16) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Bois de Málaga (9) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parque Lineal José Carlos Fajardo ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parque Princesa Diana ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Parque Municipal de la Concordia ⚠️ | Alhaurín de la Torre › Valle del Guadalhorce | 1 |
| Forêt de Ronda (7) ⚠️ | Ronda › Serranía de Ronda | 1 |
| Forêt de Ronda (9) ⚠️ | Ronda › Serranía de Ronda | 1 |
| Parque Periurbano "Río de La Villa" ⚠️ | Coín › Valle del Guadalhorce | 1 |
| Bois de Fuengirola ⚠️ | Fuengirola › Costa del Sol Occidental | 1 |
| Parc de Málaga (38) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parque El Esparragal ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Forêt de Marbella (17) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Parque "María Cristina" ⚠️ | Antequera › Antequera | 1 |
| Finca El Portón ⚠️ | Alhaurín de la Torre › Valle del Guadalhorce | 1 |
| Parc de Alhaurín de la Torre (12) ⚠️ | Alhaurín de la Torre › Valle del Guadalhorce | 1 |
| Parc de Alhaurín de la Torre (15) ⚠️ | Alhaurín de la Torre › Valle del Guadalhorce | 1 |
| Parque del Paseo ⚠️ | Antequera › Antequera | 1 |
| Plaza Era Alta ⚠️ | Mollina › Antequera | 1 |
| Parc de Málaga (39) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Forêt de Antequera (7) ⚠️ | Antequera › Antequera | 1 |
| Forêt de Antequera (8) ⚠️ | Antequera › Antequera | 1 |
| Parque San Agustín ⚠️ | Coín › Valle del Guadalhorce | 1 |
| Parque de la Libertad ⚠️ | Alhaurín el Grande › Valle del Guadalhorce | 1 |
| Parc de Torremolinos (2) ⚠️ | Torremolinos › Costa del Sol Occidental | 1 |
| Parc de Málaga (46) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Forêt de Villanueva del Trabuco (6) ⚠️ | Villanueva del Trabuco › Nororma | 1 |
| Bois de Ronda ⚠️ | Ronda › Serranía de Ronda | 1 |
| Parque de Santa Paula ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parc de Rincón de la Victoria (4) ⚠️ | Rincón de la Victoria › La Axarquía | 1 |
| Parc de Mijas (19) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Jardín de los Remedios ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Alcazaba-Fortaleza ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Parque Los Olivos ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Parc de Torremolinos (4) ⚠️ | Torremolinos › Costa del Sol Occidental | 1 |
| Parc de Marbella (19) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Parc de Marbella (20) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Parc de Marbella (21) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Parc de Marbella (33) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Parc de Marbella (39) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Parc de Marbella (40) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Bois de Vélez-Málaga ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Bois de Vélez-Málaga (2) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Forêt de Vélez-Málaga (27) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Forêt de Vélez-Málaga (31) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Forêt de Vélez-Málaga (32) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Forêt de Vélez-Málaga (35) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Forêt de Vélez-Málaga (41) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Forêt de Vélez-Málaga (42) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Forêt de Vélez-Málaga (51) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Forêt de Vélez-Málaga (57) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Forêt de Vélez-Málaga (58) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Forêt de Arenas ⚠️ | Arenas › La Axarquía | 1 |
| Forêt de Viñuela ⚠️ | Viñuela › La Axarquía | 1 |
| Forêt de Vélez-Málaga (65) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Parc de Vélez-Málaga (44) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Parc de Vélez-Málaga (45) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Parc de Mijas (33) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Parque Homenaje a la Mujer Antequerana ⚠️ | Antequera › Antequera | 1 |
| Forêt de Alhaurín el Grande (46) ⚠️ | Alhaurín el Grande › Valle del Guadalhorce | 1 |
| Forêt de Mijas (367) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Forêt de Mijas (369) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Parc de Vélez-Málaga (62) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Parc de Vélez-Málaga (63) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Forêt de Benamocarra ⚠️ | Benamocarra › La Axarquía | 1 |
| Parque Robert Baden Powell ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (20) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Forêt de Periana (3) ⚠️ | Periana › La Axarquía | 1 |
| Forêt de Periana (10) ⚠️ | Periana › La Axarquía | 1 |
| Forêt de Periana (11) ⚠️ | Periana › La Axarquía | 1 |
| Forêt de Periana (12) ⚠️ | Periana › La Axarquía | 1 |
| Forêt de Periana (14) ⚠️ | Periana › La Axarquía | 1 |
| Forêt de Viñuela (9) ⚠️ | Viñuela › La Axarquía | 1 |
| Forêt de Viñuela (12) ⚠️ | Viñuela › La Axarquía | 1 |
| Forêt de Periana (18) ⚠️ | Periana › La Axarquía | 1 |
| Forêt de Viñuela (23) ⚠️ | Viñuela › La Axarquía | 1 |
| Forêt de Viñuela (24) ⚠️ | Viñuela › La Axarquía | 1 |
| Forêt de Colmenar (2) ⚠️ | Colmenar › La Axarquía | 1 |
| Forêt de Alcaucín (4) ⚠️ | Alcaucín › La Axarquía | 1 |
| Parc de Málaga (58) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Forêt de Alcaucín (6) ⚠️ | Alcaucín › La Axarquía | 1 |
| Forêt de Alcaucín (7) ⚠️ | Alcaucín › La Axarquía | 1 |
| Forêt de Alcaucín (8) ⚠️ | Alcaucín › La Axarquía | 1 |
| Forêt de Viñuela (34) ⚠️ | Viñuela › La Axarquía | 1 |
| Forêt de Viñuela (38) ⚠️ | Viñuela › La Axarquía | 1 |
| Forêt de Viñuela (39) ⚠️ | Viñuela › La Axarquía | 1 |
| Forêt de Viñuela (50) ⚠️ | Viñuela › La Axarquía | 1 |
| Forêt de Viñuela (51) ⚠️ | Viñuela › La Axarquía | 1 |
| Forêt de Viñuela (53) ⚠️ | Viñuela › La Axarquía | 1 |
| Forêt de Vélez-Málaga (74) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Forêt de Vélez-Málaga (80) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Forêt de Vélez-Málaga (91) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Forêt de Vélez-Málaga (104) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Forêt de Riogordo ⚠️ | Riogordo › La Axarquía | 1 |
| Forêt de Riogordo (2) ⚠️ | Riogordo › La Axarquía | 1 |
| Forêt de Vélez-Málaga (133) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Forêt de Vélez-Málaga (135) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Bois de Málaga (22) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Forêt de Vélez-Málaga (138) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Forêt de Vélez-Málaga (142) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Forêt de Vélez-Málaga (146) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Forêt de Rincón de la Victoria (8) ⚠️ | Rincón de la Victoria › La Axarquía | 1 |
| Forêt de Rincón de la Victoria (11) ⚠️ | Rincón de la Victoria › La Axarquía | 1 |
| Forêt de Vélez-Málaga (151) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Forêt de Vélez-Málaga (152) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Parque Xarblanca ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Jardines de Carmen Thyssen ⚠️ | Estepona › Costa del Sol Occidental | 1 |
| Parc de Estepona (5) ⚠️ | Estepona › Costa del Sol Occidental | 1 |
| Parque de los Derechos Humanos ⚠️ | Estepona › Costa del Sol Occidental | 1 |
| Forêt de Vélez-Málaga (167) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Forêt de Vélez-Málaga (168) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Forêt de Algarrobo (12) ⚠️ | Algarrobo › La Axarquía | 1 |
| Forêt de Vélez-Málaga (188) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Forêt de Vélez-Málaga (191) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Forêt de Vélez-Málaga (204) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Forêt de Vélez-Málaga (219) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Forêt de Vélez-Málaga (222) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Parc de Algarrobo (9) ⚠️ | Algarrobo › La Axarquía | 1 |
| Forêt de Periana (21) ⚠️ | Periana › La Axarquía | 1 |
| Bois de Antequera ⚠️ | Antequera › Antequera | 1 |
| Parc de Villanueva del Trabuco (24) ⚠️ | Villanueva del Trabuco › Nororma | 1 |
| Parque Martiricos ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Forêt de Algarrobo (15) ⚠️ | Algarrobo › La Axarquía | 1 |
| Forêt de Algarrobo (24) ⚠️ | Algarrobo › La Axarquía | 1 |
| Forêt de Algarrobo (25) ⚠️ | Algarrobo › La Axarquía | 1 |
| Forêt de Sayalonga (2) ⚠️ | Sayalonga › La Axarquía | 1 |
| Parc de Málaga (63) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parc de Marbella (44) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Forêt de Vélez-Málaga (231) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Forêt de Vélez-Málaga (234) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Parc de Torremolinos (7) ⚠️ | Torremolinos › Costa del Sol Occidental | 1 |
| Parc de Alozaina ⚠️ | Alozaina › Sierra de las Nieves | 1 |
| Parc de Humilladero (9) ⚠️ | Humilladero › Antequera | 1 |
| Parc de Humilladero (15) ⚠️ | Humilladero › Antequera | 1 |
| Parc de Torremolinos (8) ⚠️ | Torremolinos › Costa del Sol Occidental | 1 |
| Forêt de Vélez-Málaga (236) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Forêt de Vélez-Málaga (253) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Forêt de Rincón de la Victoria (25) ⚠️ | Rincón de la Victoria › La Axarquía | 1 |
| Forêt de Rincón de la Victoria (26) ⚠️ | Rincón de la Victoria › La Axarquía | 1 |
| Forêt de Rincón de la Victoria (28) ⚠️ | Rincón de la Victoria › La Axarquía | 1 |
| Forêt de Rincón de la Victoria (34) ⚠️ | Rincón de la Victoria › La Axarquía | 1 |
| Forêt de Rincón de la Victoria (36) ⚠️ | Rincón de la Victoria › La Axarquía | 1 |
| Bois de Málaga (31) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Marbella (15) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Bois de Mijas (10) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Bois de Marbella (22) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Bois de Marbella (23) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Bois de Marbella (29) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Bois de Marbella (31) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Bois de Marbella (38) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Bois de Marbella (88) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Parc de Manilva (2) ⚠️ | Manilva › Costa del Sol Occidental | 1 |
| Bois de Mijas (23) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Bois de Mijas (25) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Bois de Cártama ⚠️ | Cártama › Valle del Guadalhorce | 1 |
| Forêt de Nerja (5) ⚠️ | Nerja › La Axarquía | 1 |
| Jardín Veintiocho de Junio ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parc de Málaga (77) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parc de Alhaurín de la Torre (22) ⚠️ | Alhaurín de la Torre › Valle del Guadalhorce | 1 |
| Parc de Málaga (82) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parque Gym Spinner ⚠️ | Benalmádena › Costa del Sol Occidental | 1 |
| Parque de Torre ⚠️ | Rincón de la Victoria › La Axarquía | 1 |
| Bois de Mijas (30) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Parc de Málaga (84) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parc de Benalmádena (11) ⚠️ | Benalmádena › Costa del Sol Occidental | 1 |
| Parc de Benalmádena (13) ⚠️ | Benalmádena › Costa del Sol Occidental | 1 |
| Parque Castillo Sohail ⚠️ | Fuengirola › Costa del Sol Occidental | 1 |
| Parc de Fuengirola (6) ⚠️ | Fuengirola › Costa del Sol Occidental | 1 |
| Parc de Benalmádena (14) ⚠️ | Benalmádena › Costa del Sol Occidental | 1 |
| Parc de Marbella (73) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Parc de Marbella (74) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Plaza de la Concordia ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Parc de Pizarra ⚠️ | Pizarra › Valle del Guadalhorce | 1 |
| Forêt de Comares (15) ⚠️ | Comares › La Axarquía | 1 |
| Forêt de Comares (17) ⚠️ | Comares › La Axarquía | 1 |
| Parc de Málaga (94) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parc de Málaga (95) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parc de Benamargosa ⚠️ | Benamargosa › La Axarquía | 1 |
| Forêt de Cútar (5) ⚠️ | Cútar › La Axarquía | 1 |
| Forêt de Estepona ⚠️ | Estepona › Costa del Sol Occidental | 1 |
| Forêt de El Borge (6) ⚠️ | El Borge › La Axarquía | 1 |
| Forêt de Estepona (2) ⚠️ | Estepona › Costa del Sol Occidental | 1 |
| Bois de Mijas (42) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Bois de Málaga (43) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (45) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parc de Málaga (106) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parque Fluvial Rio Fuengirola ⚠️ | Fuengirola › Costa del Sol Occidental | 1 |
| Forêt de Yunquera (10) ⚠️ | Yunquera › Sierra de las Nieves | 1 |
| Forêt de Tolox (30) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Forêt de Alozaina (5) ⚠️ | Alozaina › Sierra de las Nieves | 1 |
| Bois de Mijas (46) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Bois de Mijas (52) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Bois de Mijas (53) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Parque Forestal Cerro Vallejo ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Mijas (55) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Bois de Mijas (56) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Bosque El Chaparral ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Forêt de Tolox (32) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Forêt de Tolox (34) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Parc de Fuengirola (12) ⚠️ | Fuengirola › Costa del Sol Occidental | 1 |
| Parc de Fuengirola (14) ⚠️ | Fuengirola › Costa del Sol Occidental | 1 |
| Forêt de Tolox (35) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Forêt de Benahavís ⚠️ | Benahavís › Costa del Sol Occidental | 1 |
| Bois de Málaga (52) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parque Nuevo de Morana ⚠️ | Cuevas de San Marcos › Nororma | 1 |
| Bois de Málaga (57) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parc de Málaga (121) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (61) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parc de Cártama (7) ⚠️ | Cártama › Valle del Guadalhorce | 1 |
| Parque Ocio Water wheel ⚠️ | Torremolinos › Costa del Sol Occidental | 1 |
| Parc de Málaga (125) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (63) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Forêt de Villanueva del Trabuco (15) ⚠️ | Villanueva del Trabuco › Nororma | 1 |
| Bois de Villanueva del Trabuco (7) ⚠️ | Villanueva del Trabuco › Nororma | 1 |
| Bois de Villanueva del Trabuco (11) ⚠️ | Villanueva del Trabuco › Nororma | 1 |
| Bois de Málaga (65) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (67) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (71) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parque Forestal Cerrado de Calderón ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (75) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (81) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Forêt de Canillas de Albaida (12) ⚠️ | Canillas de Albaida › La Axarquía | 1 |
| Forêt de Sedella (6) ⚠️ | Sedella › La Axarquía | 1 |
| Forêt de Sedella (11) ⚠️ | Canillas de Aceituno › La Axarquía | 1 |
| Forêt de Canillas de Aceituno (5) ⚠️ | Canillas de Aceituno › La Axarquía | 1 |
| Forêt de Canillas de Aceituno (6) ⚠️ | Canillas de Aceituno › La Axarquía | 1 |
| Forêt de Sedella (13) ⚠️ | Sedella › La Axarquía | 1 |
| Forêt de Sedella (14) ⚠️ | Sedella › La Axarquía | 1 |
| Parc de Málaga (132) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (88) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (95) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (105) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Tolox ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Forêt de Tolox (39) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Forêt de Tolox (45) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Forêt de Monda (5) ⚠️ | Monda › Sierra de las Nieves | 1 |
| Forêt de Monda (6) ⚠️ | Monda › Sierra de las Nieves | 1 |
| Forêt de Tolox (57) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Forêt de Tolox (60) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Forêt de Tolox (66) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Forêt de Tolox (73) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Forêt de Tolox (75) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Forêt de Tolox (78) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Forêt de Tolox (79) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Forêt de Monda (8) ⚠️ | Monda › Sierra de las Nieves | 1 |
| Bois de Monda ⚠️ | Monda › Sierra de las Nieves | 1 |
| Forêt de Tolox (85) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Bois de Tolox (11) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Bois de Tolox (14) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Bois de Tolox (20) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Bois de Ronda (4) ⚠️ | Ronda › Serranía de Ronda | 1 |
| Bois de Istán ⚠️ | Istán › Sierra de las Nieves | 1 |
| Bois de Tolox (31) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Bois de Istán (6) ⚠️ | Istán › Sierra de las Nieves | 1 |
| Bois de Istán (7) ⚠️ | Istán › Sierra de las Nieves | 1 |
| Bois de Tolox (34) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Parc de Torremolinos (13) ⚠️ | Torremolinos › Costa del Sol Occidental | 1 |
| Parc de Torremolinos (14) ⚠️ | Torremolinos › Costa del Sol Occidental | 1 |
| Parque Mar de Alborán ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (119) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (122) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (123) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (125) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Tolox (39) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Bois de Istán (10) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Bois de Tolox (45) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Bois de Tolox (48) ⚠️ | Alozaina › Sierra de las Nieves | 1 |
| Bois de Tolox (50) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Bois de Tolox (54) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Bois de Ronda (11) ⚠️ | Ronda › Serranía de Ronda | 1 |
| Bois de Tolox (56) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Bois de Tolox (58) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Bois de Yunquera (2) ⚠️ | Yunquera › Sierra de las Nieves | 1 |
| Bois de Yunquera (6) ⚠️ | Yunquera › Sierra de las Nieves | 1 |
| Bois de Yunquera (7) ⚠️ | Yunquera › Sierra de las Nieves | 1 |
| Bois de Tolox (65) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Bois de Tolox (67) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Bois de Tolox (71) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Bois de Yunquera (8) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Bois de Yunquera (14) ⚠️ | Yunquera › Sierra de las Nieves | 1 |
| Bois de Istán (11) ⚠️ | Istán › Sierra de las Nieves | 1 |
| Bois de Monda (3) ⚠️ | Monda › Sierra de las Nieves | 1 |
| Bois de Monda (10) ⚠️ | Monda › Sierra de las Nieves | 1 |
| Bois de Monda (11) ⚠️ | Monda › Sierra de las Nieves | 1 |
| Bois de Monda (13) ⚠️ | Monda › Sierra de las Nieves | 1 |
| Bois de Monda (18) ⚠️ | Monda › Sierra de las Nieves | 1 |
| Bois de Monda (19) ⚠️ | Monda › Sierra de las Nieves | 1 |
| Bois de Monda (22) ⚠️ | Monda › Sierra de las Nieves | 1 |
| Bois de Alozaina (3) ⚠️ | Alozaina › Sierra de las Nieves | 1 |
| Bois de Tolox (77) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Bois de Tolox (78) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Bois de Monda (25) ⚠️ | Monda › Sierra de las Nieves | 1 |
| Bois de Istán (22) ⚠️ | Istán › Sierra de las Nieves | 1 |
| Bois de Parauta (4) ⚠️ | Parauta › Serranía de Ronda | 1 |
| Bois de Parauta (6) ⚠️ | Parauta › Serranía de Ronda | 1 |
| Bois de Yunquera (20) ⚠️ | Yunquera › Sierra de las Nieves | 1 |
| Bois de Málaga (132) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Guaro ⚠️ | Guaro › Sierra de las Nieves | 1 |
| Bois de Istán (26) ⚠️ | Istán › Sierra de las Nieves | 1 |
| Bois de Monda (28) ⚠️ | Monda › Sierra de las Nieves | 1 |
| Bois de Monda (30) ⚠️ | Monda › Sierra de las Nieves | 1 |
| Bois de Monda (33) ⚠️ | Monda › Sierra de las Nieves | 1 |
| Bois de Monda (34) ⚠️ | Monda › Sierra de las Nieves | 1 |
| Bois de Yunquera (30) ⚠️ | Yunquera › Sierra de las Nieves | 1 |
| Bois de Rincón de la Victoria (2) ⚠️ | Rincón de la Victoria › La Axarquía | 1 |
| Bois de Yunquera (31) ⚠️ | Yunquera › Sierra de las Nieves | 1 |
| Bois de Tolox (94) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Bois de Yunquera (37) ⚠️ | Yunquera › Sierra de las Nieves | 1 |
| Bois de El Burgo (8) ⚠️ | El Burgo › Sierra de las Nieves | 1 |
| Bois de El Burgo (13) ⚠️ | El Burgo › Sierra de las Nieves | 1 |
| Bois de Istán (27) ⚠️ | Istán › Sierra de las Nieves | 1 |
| Bois de Istán (35) ⚠️ | Istán › Sierra de las Nieves | 1 |
| Bois de Istán (37) ⚠️ | Istán › Sierra de las Nieves | 1 |
| Bois de Istán (38) ⚠️ | Istán › Sierra de las Nieves | 1 |
| Bois de Istán (40) ⚠️ | Istán › Sierra de las Nieves | 1 |
| Bois de Málaga (137) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Istán (45) ⚠️ | Istán › Sierra de las Nieves | 1 |
| Bois de Istán (46) ⚠️ | Istán › Sierra de las Nieves | 1 |
| Bois de Guaro (3) ⚠️ | Guaro › Sierra de las Nieves | 1 |
| Bois de Monda (39) ⚠️ | Monda › Sierra de las Nieves | 1 |
| Bois de Ronda (20) ⚠️ | Ronda › Serranía de Ronda | 1 |
| Bois de Guaro (5) ⚠️ | Guaro › Sierra de las Nieves | 1 |
| Bois de Monda (55) ⚠️ | Monda › Sierra de las Nieves | 1 |
| Bois de Monda (57) ⚠️ | Monda › Sierra de las Nieves | 1 |
| Bois de Monda (58) ⚠️ | Monda › Sierra de las Nieves | 1 |
| Bois de Ojén (5) ⚠️ | Ojén › Sierra de las Nieves | 1 |
| Bois de Ojén (7) ⚠️ | Ojén › Sierra de las Nieves | 1 |
| Bois de Monda (60) ⚠️ | Monda › Sierra de las Nieves | 1 |
| Parque Olisol ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Bois de Málaga (141) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Parauta (15) ⚠️ | Parauta › Serranía de Ronda | 1 |
| Bois de Ronda (24) ⚠️ | Ronda › Serranía de Ronda | 1 |
| Bois de El Burgo (22) ⚠️ | El Burgo › Sierra de las Nieves | 1 |
| Bois de El Burgo (23) ⚠️ | El Burgo › Sierra de las Nieves | 1 |
| Bois de Málaga (147) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Yunquera (45) ⚠️ | Yunquera › Sierra de las Nieves | 1 |
| Bois de Yunquera (47) ⚠️ | Yunquera › Sierra de las Nieves | 1 |
| Bois de Málaga (157) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Alfarnatejo ⚠️ | Alfarnatejo › La Axarquía | 1 |
| Bois de Mijas (59) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Forêt de Villanueva del Trabuco (24) ⚠️ | Villanueva del Trabuco › Nororma | 1 |
| Forêt de Alfarnate (8) ⚠️ | Alfarnate › La Axarquía | 1 |
| Forêt de Alcaucín (12) ⚠️ | Alcaucín › La Axarquía | 1 |
| Parque Monsálvez ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Plaza Eduardo Flores Carrasco ⚠️ | Estepona › Costa del Sol Occidental | 1 |
| Forêt de Viñuela (62) ⚠️ | Viñuela › La Axarquía | 1 |
| Bois de Málaga (166) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (170) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (172) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (177) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Tolox (98) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Bois de Tolox (99) ⚠️ | Tolox › Sierra de las Nieves | 1 |
| Parque Pintor Antonio Segovia ⚠️ | Mollina › Antequera | 1 |
| Parc de Málaga (151) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Forêt de Cómpeta (2) ⚠️ | Cómpeta › La Axarquía | 1 |
| Bois de Canillas de Albaida (2) ⚠️ | Canillas de Albaida › La Axarquía | 1 |
| Bois de Canillas de Albaida (4) ⚠️ | Canillas de Albaida › La Axarquía | 1 |
| Bois de Málaga (179) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Forêt de Periana (25) ⚠️ | Periana › La Axarquía | 1 |
| Forêt de Periana (26) ⚠️ | Periana › La Axarquía | 1 |
| Bois de Canillas de Aceituno ⚠️ | Canillas de Aceituno › La Axarquía | 1 |
| Parc de Alhaurín el Grande (3) ⚠️ | Alhaurín el Grande › Valle del Guadalhorce | 1 |
| Forêt de Cútar (6) ⚠️ | Cútar › La Axarquía | 1 |
| Parc de Málaga (159) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parc de Málaga (175) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (197) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (203) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (209) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (210) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Arenal Park ⚠️ | Villanueva de Algaidas › Nororma | 1 |
| Bois de Málaga (212) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (215) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Casa de Convivencias Los Jarales ⚠️ | Antequera › Antequera | 1 |
| Bois de Málaga (218) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (220) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (221) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (222) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Forêt de Colmenar (3) ⚠️ | Colmenar › La Axarquía | 1 |
| Forêt de Colmenar (4) ⚠️ | Colmenar › La Axarquía | 1 |
| Parc de Málaga (198) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (228) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (231) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (234) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (236) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Torremolinos (2) ⚠️ | Torremolinos › Costa del Sol Occidental | 1 |
| Bois de Málaga (245) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (248) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (249) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Forêt de Vélez-Málaga (260) ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Bois de Málaga (257) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (259) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Forêt de Antequera (18) ⚠️ | Antequera › Antequera | 1 |
| Bois de Málaga (260) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Forêt de Antequera (28) ⚠️ | Antequera › Antequera | 1 |
| Forêt de Antequera (29) ⚠️ | Antequera › Antequera | 1 |
| Forêt de Antequera (33) ⚠️ | Antequera › Antequera | 1 |
| Forêt de Antequera (38) ⚠️ | Antequera › Antequera | 1 |
| Forêt de Antequera (40) ⚠️ | Antequera › Antequera | 1 |
| Parque de la urbanización Renfe ⚠️ | Antequera › Antequera | 1 |
| Parque del recinto ferial ⚠️ | Antequera › Antequera | 1 |
| Parc de Málaga (208) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parc de Málaga (209) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (265) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (285) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (286) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (288) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (290) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parc de Málaga (210) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (296) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (304) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (305) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Forêt de Ojén (56) ⚠️ | Ojén › Sierra de las Nieves | 1 |
| Forêt de Ojén (58) ⚠️ | Ojén › Sierra de las Nieves | 1 |
| Forêt de Ojén (59) ⚠️ | Ojén › Sierra de las Nieves | 1 |
| Forêt de Ojén (60) ⚠️ | Ojén › Sierra de las Nieves | 1 |
| Forêt de Ojén (66) ⚠️ | Ojén › Sierra de las Nieves | 1 |
| Forêt de Ojén (68) ⚠️ | Ojén › Sierra de las Nieves | 1 |
| Forêt de Ojén (71) ⚠️ | Ojén › Sierra de las Nieves | 1 |
| Forêt de Ojén (72) ⚠️ | Ojén › Sierra de las Nieves | 1 |
| Forêt de Marbella (27) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Parc de Cuevas de San Marcos (4) ⚠️ | Cuevas de San Marcos › Nororma | 1 |
| Plaza Antoñita ⚠️ | Vélez-Málaga › La Axarquía | 1 |
| Forêt de Marbella (28) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Forêt de Coín (13) ⚠️ | Coín › Valle del Guadalhorce | 1 |
| Bois de Málaga (328) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (331) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (334) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (336) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Forêt de Coín (17) ⚠️ | Coín › Valle del Guadalhorce | 1 |
| Forêt de Monda (25) ⚠️ | Monda › Sierra de las Nieves | 1 |
| Bois de Málaga (345) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (349) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Forêt de Coín (21) ⚠️ | Coín › Valle del Guadalhorce | 1 |
| Forêt de Ojén (84) ⚠️ | Ojén › Sierra de las Nieves | 1 |
| Bois de Málaga (352) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (366) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (369) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (372) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (374) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (375) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Mijas (63) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Forêt de Colmenar (7) ⚠️ | Colmenar › La Axarquía | 1 |
| Bois de Málaga (388) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (390) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Forêt de Ojén (85) ⚠️ | Ojén › Sierra de las Nieves | 1 |
| Parc de Cuevas del Becerro (2) ⚠️ | Cuevas del Becerro › Guadalteba | 1 |
| Forêt de Ojén (91) ⚠️ | Ojén › Sierra de las Nieves | 1 |
| Forêt de Ojén (93) ⚠️ | Ojén › Sierra de las Nieves | 1 |
| Forêt de Marbella (31) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Forêt de Marbella (34) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Bois de Antequera (3) ⚠️ | Antequera › Antequera | 1 |
| Bois de Antequera (5) ⚠️ | Antequera › Antequera | 1 |
| Bois de Antequera (9) ⚠️ | Antequera › Antequera | 1 |
| Bois de Antequera (14) ⚠️ | Antequera › Antequera | 1 |
| Bois de Antequera (16) ⚠️ | Antequera › Antequera | 1 |
| Bois de Antequera (18) ⚠️ | Antequera › Antequera | 1 |
| Bois de Antequera (28) ⚠️ | Antequera › Antequera | 1 |
| Bois de Antequera (32) ⚠️ | Antequera › Antequera | 1 |
| Forêt de Alfarnatejo (4) ⚠️ | Alfarnatejo › La Axarquía | 1 |
| Bois de Villanueva del Rosario (2) ⚠️ | Villanueva del Rosario › Nororma | 1 |
| Bois de Villanueva del Rosario (3) ⚠️ | Villanueva del Rosario › Nororma | 1 |
| Forêt de Alfarnatejo (5) ⚠️ | Alfarnatejo › La Axarquía | 1 |
| Forêt de Marbella (35) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Forêt de Marbella (36) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Parque El Capricho ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Forêt de Marbella (39) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Forêt de Marbella (42) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Bois de Málaga (397) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Forêt de Marbella (51) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Bois de Málaga (407) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parc de Mijas (76) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Forêt de Mijas (370) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Forêt de Mijas (371) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Parc de Mijas (80) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Bois de Málaga (418) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parc de Málaga (222) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (429) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (430) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (431) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (432) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (435) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (443) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (450) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Ronda (26) ⚠️ | Ronda › Serranía de Ronda | 1 |
| Bois de Málaga (483) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (500) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Forêt de Mijas (375) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Bois de Marbella (90) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Bois de Málaga (514) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (516) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (517) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (519) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (523) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (525) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (527) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (530) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (533) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (540) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (543) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (547) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parque de Pacolito ⚠️ | Fuengirola › Costa del Sol Occidental | 1 |
| Bois de Málaga (561) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Forêt de Benamargosa (10) ⚠️ | Benamargosa › La Axarquía | 1 |
| Plaza Sierra de Almijara ⚠️ | Estepona › Costa del Sol Occidental | 1 |
| Forêt de Mijas (377) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Bois de Málaga (578) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (580) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Forêt de Marbella (52) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Parque Cruz de San Jorge ⚠️ | Ronda › Serranía de Ronda | 1 |
| Bois de Mijas (64) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Forêt de Mijas (392) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Forêt de Mijas (418) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Bois de Mijas (98) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Bois de Mijas (99) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Bois de Mijas (100) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Bois de Málaga (628) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (639) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (641) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Forêt de Canillas de Aceituno (7) ⚠️ | Canillas de Aceituno › La Axarquía | 1 |
| Bois de Málaga (656) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (660) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parque de Santillán ⚠️ | Mollina › Antequera | 1 |
| Forêt de Mijas (422) ⚠️ | Mijas › Costa del Sol Occidental | 1 |
| Bois de Nerja (5) ⚠️ | Nerja › La Axarquía | 1 |
| Forêt de Benalmádena ⚠️ | Benalmádena › Costa del Sol Occidental | 1 |
| Bois de Casares ⚠️ | Casares › Costa del Sol Occidental | 1 |
| Bois de Nerja (6) ⚠️ | Nerja › La Axarquía | 1 |
| Bois de Frigiliana (7) ⚠️ | Frigiliana › La Axarquía | 1 |
| Parc de Marbella (100) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Bois de Málaga (668) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (673) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (674) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (682) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (685) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (694) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Valle de Abdalajís (6) ⚠️ | Valle de Abdalajís › Valle del Guadalhorce | 1 |
| Bois de Málaga (695) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (704) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Totalán (3) ⚠️ | Totalán › La Axarquía | 1 |
| Bois de Ardales (5) ⚠️ | Ardales › Guadalteba | 1 |
| Forêt de Álora (2) ⚠️ | Álora › Valle del Guadalhorce | 1 |
| Bois de Álora (35) ⚠️ | Álora › Valle del Guadalhorce | 1 |
| Bois de Álora (55) ⚠️ | Álora › Valle del Guadalhorce | 1 |
| Parc de Marbella (102) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Parc de Estepona (25) ⚠️ | Estepona › Costa del Sol Occidental | 1 |
| Bois de Benahavís (7) ⚠️ | Benahavís › Costa del Sol Occidental | 1 |
| Bois de Benahavís (10) ⚠️ | Benahavís › Costa del Sol Occidental | 1 |
| Bois de Benahavís (16) ⚠️ | Benahavís › Costa del Sol Occidental | 1 |
| Bois de Benahavís (19) ⚠️ | Benahavís › Costa del Sol Occidental | 1 |
| Bois de Benahavís (20) ⚠️ | Benahavís › Costa del Sol Occidental | 1 |
| Bois de Málaga (712) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parc de Casabermeja (2) ⚠️ | Casabermeja › Antequera | 1 |
| Forêt de Canillas de Albaida (23) ⚠️ | Canillas de Albaida › La Axarquía | 1 |
| Bois de Frigiliana (12) ⚠️ | Frigiliana › La Axarquía | 1 |
| Bois de Frigiliana (15) ⚠️ | Frigiliana › La Axarquía | 1 |
| Bois de Frigiliana (16) ⚠️ | Frigiliana › La Axarquía | 1 |
| Bois de Frigiliana (18) ⚠️ | Frigiliana › La Axarquía | 1 |
| Parque Encinas ⚠️ | Fuengirola › Costa del Sol Occidental | 1 |
| Bois de Montejaque (3) ⚠️ | Montejaque › Serranía de Ronda | 1 |
| Bois de Montejaque (7) ⚠️ | Montejaque › Serranía de Ronda | 1 |
| Golden Beach ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Parc de Estepona (29) ⚠️ | Estepona › Costa del Sol Occidental | 1 |
| Parque de los Naranjos (2) ⚠️ | Cártama › Valle del Guadalhorce | 1 |
| Parc de Cártama (10) ⚠️ | Cártama › Valle del Guadalhorce | 1 |
| Bois de Estepona (15) ⚠️ | Estepona › Costa del Sol Occidental | 1 |
| Bois de Marbella (94) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Bois de Marbella (95) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Bois de Marbella (96) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Bois de Ojén (11) ⚠️ | Ojén › Sierra de las Nieves | 1 |
| Bois de Málaga (716) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Jardines de Picasso ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parque de la Constitución (2) ⚠️ | Marbella › Costa del Sol Occidental | 1 |
| Parque Santo Cristo ⚠️ | Cártama › Valle del Guadalhorce | 1 |
| Parc de Málaga (259) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parc de Málaga (260) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (723) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Bois de Málaga (724) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parc de Málaga (266) ⚠️ | Málaga › Málaga-Costa del Sol | 1 |
| Parque del Castillo de Papabellotas ⚠️ | Antequera › Antequera | 1 |
| Bois de Álora (109) ⚠️ | Álora › Valle del Guadalhorce | 1 |

3 180 parc(s) plus petits qu'une cellule ne sont pas listés : la carte les dessine, mais ils n'offrent aucune cellule.

⚠️ 4364 parc(s) hors de la fenêtre 10–125 cellules (4353 trop petit(s), 11 trop grand(s)) : affichés sur la carte, mais ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| military | 487 |
| airport | 209 |
| prison | 13 |
| **Total déclaré** | **709** |
| dont dans une zone de ce territoire | 709 |


### Zones concernées

| Zone | Cellules exclues |
|---|---:|
| Ronda | 474 |
| Málaga | 212 |
| Archidona | 9 |
| Vélez-Málaga | 6 |
| Alhaurín de la Torre | 4 |
| Antequera | 4 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
