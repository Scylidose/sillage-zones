# Province de Málaga

Pack `es-malaga` · version 1.0.0 · grille 200 m · Espagne › Andalousie

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 283 667 |
| dont restreintes (aéroport, militaire, prison) | 709 |
| Cellules retirées par le masque d'eau | 1 925 |
| Villes | 103 |
| Arrondissements et quartiers | 0 |
| Îles | 0 |
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

## Villes (103)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Parcs |
|---|---:|---:|---:|---:|---:|---:|
| Antequera | 29 467 | 170 | 29 297 | 4 | **29 293** | 123 |
| Ronda | 15 527 | 1 | 15 526 | 474 | **15 052** | 64 |
| Málaga | 15 439 | 163 | 15 276 | 212 | **15 064** | 1090 |
| Archidona | 7 307 | 3 | 7 304 | 9 | **7 295** | 14 |
| Campillos | 7 377 | 366 | 7 011 | 0 | **7 011** | 4 |
| Cortes de la Frontera | 6 828 | 1 | 6 827 | 0 | **6 827** | 2 |
| Álora | 6 639 | 8 | 6 631 | 0 | **6 631** | 135 |
| Cañete la Real | 6 480 | 0 | 6 480 | 0 | **6 480** |  |
| Almogía | 6 370 | 34 | 6 336 | 0 | **6 336** |  |
| Casares | 6 282 | 18 | 6 264 | 0 | **6 264** | 8 |
| Vélez-Málaga | 6 161 | 32 | 6 129 | 6 | **6 123** | 371 |
| Mijas | 5 766 | 17 | 5 749 | 0 | **5 749** | 650 |
| Benahavís | 5 650 | 9 | 5 641 | 0 | **5 641** | 33 |
| Teba | 5 605 | 50 | 5 555 | 0 | **5 555** | 2 |
| Estepona | 5 318 | 7 | 5 311 | 0 | **5 311** | 62 |
| Coín | 4 956 | 0 | 4 956 | 0 | **4 956** | 32 |
| El Burgo | 4 636 | 0 | 4 636 | 0 | **4 636** | 40 |
| Marbella | 4 537 | 20 | 4 517 | 0 | **4 517** | 288 |
| Casarabonela | 4 443 | 1 | 4 442 | 0 | **4 442** | 1 |
| Cártama | 4 096 | 6 | 4 090 | 0 | **4 090** | 22 |
| Ardales | 4 173 | 210 | 3 963 | 0 | **3 963** | 16 |
| Gaucín | 3 815 | 0 | 3 815 | 0 | **3 815** | 4 |
| Istán | 3 861 | 79 | 3 782 | 0 | **3 782** | 57 |
| Tolox | 3 672 | 0 | 3 672 | 0 | **3 672** | 187 |
| Sierra de Yeguas | 3 378 | 0 | 3 378 | 0 | **3 378** | 1 |
| Ojén | 3 341 | 0 | 3 341 | 0 | **3 341** | 104 |
| Nerja | 3 322 | 0 | 3 322 | 0 | **3 322** | 51 |
| Alhaurín de la Torre | 3 210 | 3 | 3 207 | 4 | **3 203** | 48 |
| Fuente de Piedra | 3 573 | 481 | 3 092 | 0 | **3 092** | 1 |
| Mollina | 2 947 | 0 | 2 947 | 0 | **2 947** | 7 |
| Alhaurín el Grande | 2 851 | 0 | 2 851 | 0 | **2 851** | 61 |
| Villanueva de Algaidas | 2 775 | 2 | 2 773 | 0 | **2 773** | 5 |
| Villanueva de la Concepción | 2 640 | 0 | 2 640 | 0 | **2 640** | 4 |
| Casabermeja | 2 629 | 4 | 2 625 | 0 | **2 625** | 2 |
| Colmenar | 2 581 | 1 | 2 580 | 0 | **2 580** | 23 |
| Alameda | 2 581 | 8 | 2 573 | 0 | **2 573** |  |
| Pizarra | 2 487 | 0 | 2 487 | 0 | **2 487** | 34 |
| Villanueva del Trabuco | 2 319 | 0 | 2 319 | 0 | **2 319** | 68 |
| Periana | 2 282 | 1 | 2 281 | 0 | **2 281** | 33 |
| Monda | 2 238 | 0 | 2 238 | 0 | **2 238** | 97 |
| Yunquera | 2 152 | 0 | 2 152 | 0 | **2 152** | 61 |
| Montecorto | 2 128 | 8 | 2 120 | 0 | **2 120** | 2 |
| Cómpeta | 2 112 | 0 | 2 112 | 0 | **2 112** | 5 |
| Torrox | 1 970 | 2 | 1 968 | 0 | **1 968** | 16 |
| Alcaucín | 1 772 | 1 | 1 771 | 0 | **1 771** | 24 |
| Montejaque | 1 768 | 9 | 1 759 | 0 | **1 759** | 7 |
| Parauta | 1 729 | 0 | 1 729 | 0 | **1 729** | 17 |
| Villanueva del Rosario | 1 727 | 0 | 1 727 | 0 | **1 727** | 17 |
| Igualeja | 1 701 | 0 | 1 701 | 0 | **1 701** | 4 |
| Canillas de Aceituno | 1 642 | 2 | 1 640 | 0 | **1 640** | 10 |
| Frigiliana | 1 584 | 0 | 1 584 | 0 | **1 584** | 25 |
| Riogordo | 1 568 | 1 | 1 567 | 0 | **1 567** | 10 |
| Jubrique | 1 517 | 0 | 1 517 | 0 | **1 517** |  |
| Cuevas de San Marcos | 1 459 | 9 | 1 450 | 0 | **1 450** | 17 |
| Manilva | 1 369 | 3 | 1 366 | 0 | **1 366** | 6 |
| Almargen | 1 349 | 0 | 1 349 | 0 | **1 349** | 8 |
| Humilladero | 1 354 | 5 | 1 349 | 0 | **1 349** | 24 |
| Alfarnate | 1 334 | 1 | 1 333 | 0 | **1 333** | 15 |
| Alozaina | 1 322 | 0 | 1 322 | 0 | **1 322** | 18 |
| Júzcar | 1 313 | 0 | 1 313 | 0 | **1 313** |  |
| Canillas de Albaida | 1 293 | 0 | 1 293 | 0 | **1 293** | 32 |
| Benaoján | 1 250 | 0 | 1 250 | 0 | **1 250** |  |
| Genalguacil | 1 243 | 0 | 1 243 | 0 | **1 243** |  |
| Sedella | 1 238 | 0 | 1 238 | 0 | **1 238** | 17 |
| Alpandeire | 1 213 | 0 | 1 213 | 0 | **1 213** |  |
| Serrato | 1 114 | 0 | 1 114 | 0 | **1 114** | 1 |
| Rincón de la Victoria | 1 099 | 7 | 1 092 | 0 | **1 092** | 81 |
| Jimera de Líbar | 1 064 | 0 | 1 064 | 0 | **1 064** |  |
| Benalmádena | 1 045 | 3 | 1 042 | 0 | **1 042** | 36 |
| Arenas | 1 028 | 0 | 1 028 | 0 | **1 028** | 10 |
| Comares | 993 | 8 | 985 | 0 | **985** | 21 |
| Benarrabá | 972 | 0 | 972 | 0 | **972** |  |
| El Borge | 957 | 0 | 957 | 0 | **957** | 7 |
| Pujerra | 944 | 0 | 944 | 0 | **944** |  |
| Viñuela | 1 092 | 152 | 940 | 0 | **940** | 67 |
| Carratraca | 881 | 0 | 881 | 0 | **881** |  |
| Guaro | 878 | 0 | 878 | 0 | **878** | 10 |
| Villanueva de Tapia | 874 | 0 | 874 | 0 | **874** | 3 |
| Cartajima | 840 | 0 | 840 | 0 | **840** |  |
| Valle de Abdalajís | 833 | 0 | 833 | 0 | **833** | 19 |
| Alfarnatejo | 804 | 0 | 804 | 0 | **804** | 11 |
| Benadalid | 802 | 0 | 802 | 0 | **802** | 2 |
| Faraján | 795 | 0 | 795 | 0 | **795** |  |
| Torremolinos | 782 | 0 | 782 | 0 | **782** | 33 |
| Algatocín | 766 | 0 | 766 | 0 | **766** |  |
| Cútar | 764 | 0 | 764 | 0 | **764** | 7 |
| Benalauría | 764 | 1 | 763 | 0 | **763** |  |
| Sayalonga | 711 | 1 | 710 | 0 | **710** | 2 |
| Cuevas Bajas | 656 | 0 | 656 | 0 | **656** | 2 |
| Cuevas del Becerro | 627 | 0 | 627 | 0 | **627** | 2 |
| Almáchar | 555 | 0 | 555 | 0 | **555** | 5 |
| Moclinejo | 555 | 0 | 555 | 0 | **555** | 2 |
| Benamargosa | 475 | 0 | 475 | 0 | **475** | 13 |
| Atajate | 422 | 0 | 422 | 0 | **422** |  |
| Salares | 405 | 0 | 405 | 0 | **405** | 17 |
| Fuengirola | 395 | 0 | 395 | 0 | **395** | 70 |
| Algarrobo | 383 | 7 | 376 | 0 | **376** | 45 |
| Totalán | 354 | 4 | 350 | 0 | **350** | 4 |
| Arriate | 328 | 0 | 328 | 0 | **328** | 1 |
| Iznate | 294 | 4 | 290 | 0 | **290** | 1 |
| Macharaviaya | 284 | 2 | 282 | 0 | **282** | 6 |
| Benamocarra | 217 | 0 | 217 | 0 | **217** | 9 |
| Árchez | 186 | 0 | 186 | 0 | **186** |  |

## Parcs (4589)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Bois de Málaga (715) ⚠️ | Málaga | 911 |
| Bois de Málaga (727) ⚠️ | Málaga | 788 |
| Bois de Serrato ⚠️ | Serrato | 311 |
| Bois de Mollina ⚠️ | Mollina | 297 |
| Forêt de Coín (23) ⚠️ | Coín | 210 |
| Forêt de Antequera (3) ⚠️ | Antequera | 209 |
| Forêt de Nerja (2) ⚠️ | Nerja | 191 |
| Forêt de Tolox ⚠️ | Tolox | 179 |
| Forêt de Periana ⚠️ | Periana | 154 |
| Forêt de Tolox (86) ⚠️ | Tolox | 153 |
| Parque Forestal Ciudad de Málaga ⚠️ | Málaga | 137 |
| Forêt de Alfarnatejo | Alfarnatejo | 121 |
| Forêt de Antequera (5) | Antequera | 118 |
| Forêt de Alfarnate (2) | Alfarnate | 116 |
| Forêt de Antequera (14) | Antequera | 115 |
| Forêt de El Burgo | El Burgo | 112 |
| Bois de Benahavís | Benahavís | 110 |
| Bois de Ardales (14) | Ardales | 108 |
| Forêt de Ronda (10) | Ronda | 104 |
| Forêt de Ronda (6) | Ronda | 98 |
| Forêt de Humilladero (5) | Humilladero | 97 |
| Forêt de Nerja | Nerja | 92 |
| Forêt de Yunquera | Yunquera | 90 |
| Forêt de Tolox (2) | Tolox | 88 |
| Bois de Istán (9) | Istán | 88 |
| Forêt de Alhaurín el Grande (40) | Alhaurín el Grande | 82 |
| Forêt de Antequera (2) | Antequera | 78 |
| Forêt de Marbella (13) | Marbella | 78 |
| Bois de Istán (30) | Istán | 76 |
| Forêt de Benalmádena (3) | Benalmádena | 76 |
| Forêt de Antequera (24) | Antequera | 74 |
| Pinar de los Almendrales | Málaga | 73 |
| Forêt de Alfarnate (3) | Alfarnate | 71 |
| Forêt de Monda (23) | Monda | 68 |
| Forêt de Nerja (13) | Nerja | 66 |
| Forêt de Villanueva del Trabuco (5) | Villanueva del Trabuco | 65 |
| Bois de Alfarnate (2) | Alfarnate | 65 |
| Forêt de Coín (24) | Coín | 65 |
| Forêt de Alhaurín el Grande | Alhaurín el Grande | 63 |
| Bois de Colmenar (3) | Colmenar | 63 |
| Forêt de Ojén (50) | Ojén | 61 |
| Forêt de Salares (14) | Salares | 60 |
| Bois de Istán (29) | Istán | 60 |
| Forêt de Alhaurín el Grande (3) | Alhaurín el Grande | 57 |
| Forêt de Tolox (10) | Tolox | 57 |
| Forêt de Coín (4) | Coín | 56 |
| Bois de Istán (13) | Istán | 56 |
| Forêt de Sedella (17) | Sedella | 55 |
| Forêt de Tolox (6) | Tolox | 53 |
| Forêt de Villanueva del Trabuco (4) | Villanueva del Trabuco | 52 |
| Forêt de Arenas (10) | Arenas | 52 |
| Bois de Montejaque (5) | Montejaque | 51 |
| Bois de El Burgo (6) | El Burgo | 49 |
| Bois de Ardales (8) | Ardales | 48 |
| Forêt de Alhaurín el Grande (10) | Alhaurín el Grande | 46 |
| Forêt de Canillas de Albaida (24) | Canillas de Albaida | 45 |
| Forêt de Yunquera (13) | Yunquera | 44 |
| Forêt de Tolox (5) | Tolox | 43 |
| Bois de Nerja (16) | Nerja | 41 |
| Forêt de Alcaucín (9) | Alcaucín | 39 |
| Forêt de Coín (7) | Coín | 39 |
| Forêt de Monda (10) | Monda | 38 |
| Forêt de Álora (3) | Álora | 38 |
| Forêt de Marbella (12) | Marbella | 37 |
| Forêt de Tolox (8) | Tolox | 37 |
| Bois de Alfarnatejo (2) | Alfarnatejo | 37 |
| Bois de Frigiliana (11) | Frigiliana | 37 |
| Forêt de Alfarnate | Alfarnate | 36 |
| Forêt de Alcaucín (16) | Alcaucín | 36 |
| Parque Periurbano Pinar del Hacho | Antequera | 35 |
| Forêt de Yunquera (4) | Yunquera | 35 |
| Forêt de Montecorto (2) | Montecorto | 35 |
| Bois de Frigiliana (8) | Frigiliana | 35 |
| Forêt de Mollina | Mollina | 34 |
| Forêt de Tolox (7) | Tolox | 34 |
| Forêt de Alozaina (3) | Alozaina | 34 |
| Forêt de Tolox (56) | Tolox | 34 |
| Forêt de Ojén (77) | Ojén | 34 |
| Bois de Antequera (25) | Antequera | 34 |
| Forêt de Ojén | Ojén | 33 |
| Forêt de Yunquera (5) | Yunquera | 33 |
| Forêt de Ojén (73) | Ojén | 32 |
| Forêt de Ojén (81) | Ojén | 32 |
| Bois de Málaga (3) | Málaga | 31 |
| Forêt de El Burgo (2) | Yunquera | 31 |
| Forêt de Canillas de Albaida (20) | Canillas de Albaida | 31 |
| Bois de Frigiliana (14) | Frigiliana | 31 |
| Pinar de Nagüeles | Marbella | 30 |
| Forêt de Canillas de Albaida (4) | Canillas de Albaida | 30 |
| Forêt de Marbella | Marbella | 29 |
| Forêt de Tolox (16) | Tolox | 29 |
| Forêt de Antequera (4) | Antequera | 28 |
| Bois de Alfarnate (3) | Alfarnate | 28 |
| Forêt de Alfarnatejo (2) | Alfarnatejo | 28 |
| Bois de Riogordo | Riogordo | 28 |
| Forêt de Antequera (20) | Antequera | 27 |
| Bois de Villanueva de la Concepción | Villanueva de la Concepción | 27 |
| Bois de Istán (3) | Istán | 26 |
| Bois de Antequera (11) | Antequera | 26 |
| Bois de Málaga (659) | Málaga | 26 |
| Forêt de Alhaurín el Grande (48) | Alhaurín el Grande | 26 |
| Bois de Istán (21) | Istán | 25 |
| Bois de Ardales (9) | Ardales | 25 |
| Forêt de Salares (5) | Salares | 24 |
| Forêt de Salares (7) | Salares | 24 |
| Bois de Istán (18) | Istán | 24 |
| Bois de Benahavís (2) | Benahavís | 23 |
| Forêt de Villanueva del Rosario | Villanueva del Rosario | 22 |
| Bois de Monda (23) | Monda | 22 |
| Bois de Istán (17) | Istán | 22 |
| Bois de Istán (33) | Istán | 22 |
| Bois de Ronda (27) | Ronda | 22 |
| Bois de Igualeja | Igualeja | 21 |
| Bois de Antequera (35) | Antequera | 21 |
| Bois de Frigiliana (6) | Frigiliana | 21 |
| Forêt de Antequera | Antequera | 20 |
| Forêt de Cuevas de San Marcos | Cuevas de San Marcos | 20 |
| Bois de Málaga (2) | Málaga | 20 |
| Bois de Marbella (17) | Marbella | 20 |
| Bois de El Burgo (16) | El Burgo | 20 |
| Forêt de Monda (14) | Monda | 20 |
| Bois de Antequera (29) | Antequera | 20 |
| Forêt de Benalmádena (2) | Benalmádena | 20 |
| Forêt de Coín | Coín | 19 |
| Forêt de Canillas de Albaida | Canillas de Albaida | 19 |
| Forêt de Canillas de Albaida (2) | Canillas de Albaida | 19 |
| Forêt de Montecorto | Montecorto | 19 |
| Bois de Villanueva del Trabuco | Villanueva del Trabuco | 19 |
| Forêt de Yunquera (2) | Yunquera | 19 |
| Forêt de Tolox (4) | Tolox | 19 |
| Forêt de Canillas de Albaida (6) | Canillas de Albaida | 19 |
| Bois de Guaro (7) | Guaro | 19 |
| Bois de Alfarnatejo (3) | Alfarnatejo | 19 |
| Forêt de Ardales | Ardales | 18 |
| Forêt de Canillas de Aceituno | Canillas de Aceituno | 18 |
| Bois de Málaga | Málaga | 18 |
| Forêt de Yunquera (3) | Yunquera | 18 |
| Bois de Monda (6) | Monda | 18 |
| Bois de El Burgo (9) | El Burgo | 18 |
| Bois de El Burgo (21) | El Burgo | 18 |
| Forêt de Salares (15) | Salares | 18 |
| Parque Forestal La Virreina | Málaga | 18 |
| Forêt de Monda (15) | Monda | 18 |
| Bois de Antequera (24) | Antequera | 18 |
| Forêt de Arenas (11) | Arenas | 18 |
| Forêt de Canillas de Albaida (13) | Canillas de Albaida | 17 |
| Bois de Istán (28) | Istán | 17 |
| Forêt de Villanueva de la Concepción | Villanueva de la Concepción | 17 |
| Forêt de Marbella (23) | Marbella | 17 |
| Forêt de Monda (12) | Monda | 17 |
| Forêt de Villanueva del Trabuco (26) | Villanueva del Trabuco | 17 |
| Bois de Colmenar (5) | Colmenar | 17 |
| Bois de Ardales (12) | Ardales | 17 |
| Parque Forestal Monte Victoria | Málaga | 16 |
| Forêt de Coín (3) | Coín | 16 |
| Forêt de Monda (4) | Monda | 16 |
| Bois de El Burgo (7) | El Burgo | 16 |
| Bois de Yunquera (43) | Yunquera | 16 |
| Bois de Alcaucín | Alcaucín | 16 |
| Forêt de Canillas de Albaida (19) | Canillas de Albaida | 16 |
| Forêt de Antequera (34) | Antequera | 16 |
| Bois de Riogordo (3) | Riogordo | 16 |
| Bois de Ardales (13) | Ardales | 16 |
| Forêt de Periana (16) | Periana | 15 |
| Forêt de Istán | Istán | 15 |
| Forêt de Alozaina (6) | Alozaina | 15 |
| Bois de Istán (25) | Istán | 15 |
| Bois de Periana | Periana | 15 |
| Forêt de Sedella (16) | Sedella | 15 |
| Forêt de Coín (12) | Coín | 15 |
| Bois de Antequera (30) | Antequera | 15 |
| Forêt de Colmenar | Colmenar | 14 |
| Forêt de Alhaurín el Grande (9) | Alhaurín el Grande | 14 |
| Forêt de Alhaurín el Grande (18) | Alhaurín el Grande | 14 |
| Bois de Istán (42) | Istán | 14 |
| Forêt de Villanueva del Rosario (2) | Villanueva del Rosario | 14 |
| Forêt de Monda (13) | Monda | 14 |
| Forêt de Coín (14) | Coín | 14 |
| Forêt de Villanueva del Rosario (8) | Villanueva del Rosario | 14 |
| Bois de Cuevas de San Marcos (4) | Cuevas de San Marcos | 14 |
| Forêt de Alhaurín el Grande (37) | Alhaurín el Grande | 13 |
| Bois de Villanueva del Trabuco (4) | Villanueva del Trabuco | 13 |
| Forêt de Canillas de Albaida (8) | Canillas de Albaida | 13 |
| Bois de Monda (24) | Monda | 13 |
| Bois de Parauta (2) | Parauta | 13 |
| Bois de Istán (47) | Istán | 13 |
| Forêt de Coín (10) | Coín | 13 |
| Parque Forestal de Gibralfaro | Málaga | 13 |
| Forêt de Alhaurín el Grande (31) | Alhaurín el Grande | 12 |
| Forêt de Parauta | Parauta | 12 |
| Forêt de Monda (2) | Monda | 12 |
| Bois de Parauta | Parauta | 12 |
| Bois de Parauta (10) | Parauta | 12 |
| Bois de Alfarnate (4) | Alfarnate | 12 |
| Parque Forestal Monte San Antón | Málaga | 12 |
| Forêt de Antequera (21) | Antequera | 12 |
| Forêt de Antequera (22) | Antequera | 12 |
| Forêt de Villanueva de la Concepción (3) | Villanueva de la Concepción | 12 |
| Bois de Colmenar (2) | Colmenar | 12 |
| Bois de Antequera (33) | Antequera | 12 |
| Bois de Antequera (34) | Antequera | 12 |
| Forêt de Alhaurín el Grande (14) | Alhaurín el Grande | 11 |
| Forêt de Ronda (8) | Ronda | 11 |
| Forêt de Salares (4) | Salares | 11 |
| Bois de Yunquera (28) | Yunquera | 11 |
| Bois de Casarabonela | Casarabonela | 11 |
| Forêt de Málaga (2) | Málaga | 11 |
| Forêt de Benamargosa (12) | Benamargosa | 11 |
| Bois de Málaga (664) | Málaga | 11 |
| Forêt de Sedella (18) | Sedella | 11 |
| Forêt de Alhaurín el Grande (49) | Alhaurín el Grande | 11 |
| Forêt de Antequera (12) | Antequera | 10 |
| Forêt de Periana (4) | Periana | 10 |
| Forêt de Viñuela (15) | Viñuela | 10 |
| Forêt de Tolox (28) | Tolox | 10 |
| Forêt de Canillas de Albaida (11) | Canillas de Albaida | 10 |
| Forêt de Canillas de Albaida (14) | Canillas de Albaida | 10 |
| Forêt de Canillas de Aceituno (2) | Canillas de Aceituno | 10 |
| Parque Forestal Comandante Benítez | Málaga | 10 |
| Bois de Yunquera (4) | Yunquera | 10 |
| Bois de El Burgo (5) | El Burgo | 10 |
| Parque Forestal La Concepción | Málaga | 10 |
| Forêt de Humilladero | Humilladero | 10 |
| Forêt de Fuente de Piedra | Fuente de Piedra | 10 |
| Forêt de Antequera (19) | Antequera | 10 |
| Bois de Ojén (8) | Ojén | 10 |
| Forêt de Monda (11) | Monda | 10 |
| Forêt de Málaga | Málaga | 10 |
| Bois de Antequera (15) | Antequera | 10 |
| Bois de Antequera (19) | Antequera | 10 |
| Forêt de Istán (7) | Istán | 10 |
| Parque Ibn Al-Baytar | Benalmádena | 10 |
| Bois de Málaga (667) | Málaga | 10 |
| Bois de Benahavís (4) | Benahavís | 10 |
| Forêt de Canillas de Albaida (26) | Canillas de Albaida | 10 |
| Forêt de Marbella (55) | Marbella | 10 |
| Forêt de Coín (2) ⚠️ | Coín | 9 |
| Forêt de Alhaurín el Grande (29) ⚠️ | Alhaurín el Grande | 9 |
| Forêt de Alhaurín el Grande (38) ⚠️ | Alhaurín el Grande | 9 |
| Forêt de Vélez-Málaga (28) ⚠️ | Vélez-Málaga | 9 |
| Forêt de Antequera (15) ⚠️ | Antequera | 9 |
| Forêt de Tolox (17) ⚠️ | Tolox | 9 |
| Bois de Tolox (26) ⚠️ | Tolox | 9 |
| Bois de Yunquera (11) ⚠️ | Yunquera | 9 |
| Bois de Monda (41) ⚠️ | Monda | 9 |
| Forêt de Canillas de Albaida (16) ⚠️ | Canillas de Albaida | 9 |
| Forêt de Coín (8) ⚠️ | Coín | 9 |
| Forêt de Villanueva del Rosario (5) ⚠️ | Villanueva del Rosario | 9 |
| Forêt de Villanueva del Rosario (7) ⚠️ | Villanueva del Rosario | 9 |
| Bois de Antequera (7) ⚠️ | Antequera | 9 |
| Forêt de Cútar (7) ⚠️ | Cútar | 9 |
| Bois de Nerja (12) ⚠️ | Nerja | 9 |
| Bois de Benahavís (15) ⚠️ | Benahavís | 9 |
| Parque Forestal de El Morlaco ⚠️ | Málaga | 8 |
| Forêt de Ojén (46) ⚠️ | Ojén | 8 |
| Forêt de Mijas (352) ⚠️ | Mijas | 8 |
| Forêt de Alhaurín el Grande (41) ⚠️ | Alhaurín el Grande | 8 |
| Forêt de Antequera (11) ⚠️ | Antequera | 8 |
| Forêt de Yunquera (9) ⚠️ | Yunquera | 8 |
| Forêt de Tolox (18) ⚠️ | Tolox | 8 |
| Forêt de Yunquera (12) ⚠️ | Yunquera | 8 |
| Forêt de Salares ⚠️ | Salares | 8 |
| Bois de El Burgo ⚠️ | El Burgo | 8 |
| Bois de El Burgo (4) ⚠️ | El Burgo | 8 |
| Bois de Istán (12) ⚠️ | Istán | 8 |
| Bois de Ronda (16) ⚠️ | Ronda | 8 |
| Parque Forestal El Lagarillo Blanco ⚠️ | Málaga | 8 |
| Forêt de Canillas de Albaida (21) ⚠️ | Canillas de Albaida | 8 |
| Forêt de Coín (20) ⚠️ | Coín | 8 |
| Forêt de Villanueva del Trabuco (27) ⚠️ | Villanueva del Trabuco | 8 |
| Forêt de Arenas (7) ⚠️ | Arenas | 8 |
| Forêt de Mijas (139) ⚠️ | Mijas | 7 |
| Forêt de Alhaurín el Grande (7) ⚠️ | Alhaurín el Grande | 7 |
| Forêt de Torremolinos ⚠️ | Torremolinos | 7 |
| Forêt de Viñuela (3) ⚠️ | Viñuela | 7 |
| Forêt de Comares (4) ⚠️ | Comares | 7 |
| Forêt de Yunquera (6) ⚠️ | Yunquera | 7 |
| Forêt de Alozaina (4) ⚠️ | Alozaina | 7 |
| Bois de Villanueva del Trabuco (9) ⚠️ | Villanueva del Trabuco | 7 |
| Forêt de Salares (13) ⚠️ | Salares | 7 |
| Forêt de Tolox (82) ⚠️ | Tolox | 7 |
| Bois de Yunquera (5) ⚠️ | Yunquera | 7 |
| Bois de Tolox (84) ⚠️ | Tolox | 7 |
| Bois de Yunquera (27) ⚠️ | Yunquera | 7 |
| Bois de El Burgo (10) ⚠️ | El Burgo | 7 |
| Bois de Istán (48) ⚠️ | Istán | 7 |
| Forêt de Canillas de Albaida (18) ⚠️ | Canillas de Albaida | 7 |
| Forêt de Marbella (25) ⚠️ | Marbella | 7 |
| Forêt de Ojén (79) ⚠️ | Ojén | 7 |
| Forêt de Coín (15) ⚠️ | Coín | 7 |
| Bois de Antequera (23) ⚠️ | Antequera | 7 |
| Bois de Antequera (27) ⚠️ | Antequera | 7 |
| Bois de Alfarnatejo (4) ⚠️ | Alfarnatejo | 7 |
| Bois de Álora (2) ⚠️ | Álora | 7 |
| Bois de Frigiliana (5) ⚠️ | Frigiliana | 7 |
| Bois de Mijas (101) ⚠️ | Mijas | 7 |
| Bois de Ojén (10) ⚠️ | Marbella | 7 |
| Bois de Álora (108) ⚠️ | Álora | 7 |
| Forêt de Marbella (6) ⚠️ | Marbella | 6 |
| Forêt de Alhaurín el Grande (13) ⚠️ | Alhaurín el Grande | 6 |
| Forêt de Alhaurín el Grande (24) ⚠️ | Alhaurín el Grande | 6 |
| Forêt de Mijas (366) ⚠️ | Mijas | 6 |
| Forêt de Vélez-Málaga (108) ⚠️ | Vélez-Málaga | 6 |
| Forêt de Vélez-Málaga (155) ⚠️ | Vélez-Málaga | 6 |
| Bois de Málaga (58) ⚠️ | Málaga | 6 |
| Forêt de Canillas de Aceituno (4) ⚠️ | Canillas de Aceituno | 6 |
| Bois de Ronda (2) ⚠️ | Ronda | 6 |
| Forêt de Tolox (44) ⚠️ | Tolox | 6 |
| Forêt de Tolox (58) ⚠️ | Tolox | 6 |
| Forêt de Tolox (76) ⚠️ | Tolox | 6 |
| Forêt de Tolox (81) ⚠️ | Tolox | 6 |
| Bois de Istán (8) ⚠️ | Istán | 6 |
| Bois de Tolox (35) ⚠️ | Tolox | 6 |
| Bois de Tolox (55) ⚠️ | Tolox | 6 |
| Bois de Istán (16) ⚠️ | Istán | 6 |
| Bois de Tolox (81) ⚠️ | Tolox | 6 |
| Bois de Istán (31) ⚠️ | Istán | 6 |
| Bois de Yunquera (39) ⚠️ | Yunquera | 6 |
| Bois de El Burgo (19) ⚠️ | El Burgo | 6 |
| Bois de Monda (38) ⚠️ | Monda | 6 |
| Bois de Igualeja (2) ⚠️ | Igualeja | 6 |
| Bois de Ronda (21) ⚠️ | Ronda | 6 |
| Bois de Ronda (22) ⚠️ | Ronda | 6 |
| Bois de Alfarnate ⚠️ | Alfarnate | 6 |
| Forêt de Canillas de Albaida (17) ⚠️ | Canillas de Albaida | 6 |
| Bois de Málaga (193) ⚠️ | Málaga | 6 |
| Forêt de Humilladero (3) ⚠️ | Humilladero | 6 |
| Forêt de Humilladero (6) ⚠️ | Humilladero | 6 |
| Forêt de Marbella (24) ⚠️ | Marbella | 6 |
| Forêt de Ojén (80) ⚠️ | Ojén | 6 |
| Forêt de Marbella (30) ⚠️ | Marbella | 6 |
| Bois de Colmenar ⚠️ | Colmenar | 6 |
| Bois de Antequera (20) ⚠️ | Antequera | 6 |
| Forêt de Mijas (424) ⚠️ | Mijas | 6 |
| Bois de Frigiliana (3) ⚠️ | Frigiliana | 6 |
| Bois de Frigiliana (9) ⚠️ | Frigiliana | 6 |
| Bois de Frigiliana (13) ⚠️ | Frigiliana | 6 |
| Forêt de Álora (4) ⚠️ | Álora | 6 |
| Forêt de Alhaurín el Grande (20) ⚠️ | Alhaurín el Grande | 5 |
| Forêt de Alhaurín el Grande (34) ⚠️ | Alhaurín el Grande | 5 |
| Forêt de Alhaurín el Grande (35) ⚠️ | Alhaurín el Grande | 5 |
| Bois de Málaga (16) ⚠️ | Málaga | 5 |
| Forêt de Viñuela (19) ⚠️ | Viñuela | 5 |
| Forêt de Viñuela (20) ⚠️ | Viñuela | 5 |
| Forêt de Tolox (3) ⚠️ | Tolox | 5 |
| Forêt de Tolox (9) ⚠️ | Tolox | 5 |
| Forêt de Yunquera (7) ⚠️ | Yunquera | 5 |
| Forêt de Tolox (22) ⚠️ | Tolox | 5 |
| Forêt de Monda (3) ⚠️ | Monda | 5 |
| Nagüeles ⚠️ | Marbella | 5 |
| Forêt de Salares (3) ⚠️ | Salares | 5 |
| Forêt de Sedella ⚠️ | Sedella | 5 |
| Forêt de Ojén (55) ⚠️ | Ojén | 5 |
| Forêt de Tolox (55) ⚠️ | Tolox | 5 |
| Bois de Tolox (5) ⚠️ | Tolox | 5 |
| Bois de Yunquera (13) ⚠️ | Yunquera | 5 |
| Bois de Yunquera (26) ⚠️ | Yunquera | 5 |
| Bois de Ronda (18) ⚠️ | Ronda | 5 |
| Bois de Istán (43) ⚠️ | Istán | 5 |
| Bois de Istán (44) ⚠️ | Istán | 5 |
| Bois de Yunquera (46) ⚠️ | Yunquera | 5 |
| Forêt de Alfarnatejo (3) ⚠️ | Alfarnatejo | 5 |
| Bois de Málaga (191) ⚠️ | Málaga | 5 |
| Forêt de Ojén (61) ⚠️ | Ojén | 5 |
| Forêt de Monda (16) ⚠️ | Monda | 5 |
| Forêt de Ojén (87) ⚠️ | Ojén | 5 |
| Forêt de Villanueva del Rosario (4) ⚠️ | Villanueva del Rosario | 5 |
| Forêt de Villanueva del Rosario (6) ⚠️ | Villanueva del Rosario | 5 |
| Parque Forestal Hacienda Clavero ⚠️ | Málaga | 5 |
| Bois de Antequera (8) ⚠️ | Antequera | 5 |
| Bois de Colmenar (6) ⚠️ | Colmenar | 5 |
| Bois de Riogordo (5) ⚠️ | Riogordo | 5 |
| Forêt de Nerja (12) ⚠️ | Nerja | 5 |
| Bois de Málaga (575) ⚠️ | Málaga | 5 |
| Bois de Frigiliana ⚠️ | Frigiliana | 5 |
| Bois de Frigiliana (10) ⚠️ | Frigiliana | 5 |
| Bois de Riogordo (6) ⚠️ | Riogordo | 5 |
| Bois de Málaga (717) ⚠️ | Málaga | 5 |
| Parque Arquitecta María Eugenia Candau ⚠️ | Málaga | 4 |
| Forêt de Marbella (3) ⚠️ | Marbella | 4 |
| Parque del Norte ⚠️ | Málaga | 4 |
| Forêt de Alhaurín el Grande (23) ⚠️ | Alhaurín el Grande | 4 |
| Forêt de Alhaurín el Grande (28) ⚠️ | Alhaurín el Grande | 4 |
| Forêt de Alhaurín el Grande (32) ⚠️ | Alhaurín el Grande | 4 |
| Forêt de Alhaurín el Grande (36) ⚠️ | Alhaurín el Grande | 4 |
| Parque Forestal Los Tres Jardines ⚠️ | Marbella | 4 |
| Forêt de Antequera (13) ⚠️ | Antequera | 4 |
| Forêt de Alhaurín el Grande (47) ⚠️ | Alhaurín el Grande | 4 |
| Forêt de Viñuela (7) ⚠️ | Viñuela | 4 |
| Forêt de Viñuela (18) ⚠️ | Viñuela | 4 |
| Forêt de Tolox (12) ⚠️ | Tolox | 4 |
| Forêt de Tolox (13) ⚠️ | Tolox | 4 |
| Forêt de Tolox (23) ⚠️ | Tolox | 4 |
| Forêt de Tolox (24) ⚠️ | Tolox | 4 |
| Forêt de Tolox (26) ⚠️ | Tolox | 4 |
| Forêt de Monda ⚠️ | Monda | 4 |
| Forêt de Marbella (19) ⚠️ | Marbella | 4 |
| Bois de Málaga (56) ⚠️ | Málaga | 4 |
| Forêt de Canillas de Albaida (7) ⚠️ | Canillas de Albaida | 4 |
| Forêt de Ojén (51) ⚠️ | Ojén | 4 |
| Forêt de Ojén (54) ⚠️ | Ojén | 4 |
| Bois de Tolox (2) ⚠️ | Tolox | 4 |
| Forêt de Tolox (46) ⚠️ | Tolox | 4 |
| Forêt de Tolox (77) ⚠️ | Tolox | 4 |
| Forêt de Tolox (80) ⚠️ | Tolox | 4 |
| Bois de Tolox (28) ⚠️ | Tolox | 4 |
| Bois de Ojén (2) ⚠️ | Ojén | 4 |
| Bois de Ojén (3) ⚠️ | Ojén | 4 |
| Bois de Ronda (8) ⚠️ | Ronda | 4 |
| Bois de El Burgo (2) ⚠️ | El Burgo | 4 |
| Bois de Málaga (120) ⚠️ | Málaga | 4 |
| Bois de Málaga (121) ⚠️ | Málaga | 4 |
| Bois de Tolox (47) ⚠️ | Tolox | 4 |
| Bois de Alozaina ⚠️ | Tolox | 4 |
| Bois de Yunquera (15) ⚠️ | Yunquera | 4 |
| Bois de Monda (17) ⚠️ | Monda | 4 |
| Bois de Yunquera (18) ⚠️ | Yunquera | 4 |
| Bois de El Burgo (18) ⚠️ | El Burgo | 4 |
| Bois de Ojén (4) ⚠️ | Ojén | 4 |
| Bois de El Burgo (20) ⚠️ | El Burgo | 4 |
| Forêt de Alfarnate (4) ⚠️ | Alfarnate | 4 |
| Bois de Alfarnate (5) ⚠️ | Alfarnate | 4 |
| Bois de Periana (2) ⚠️ | Periana | 4 |
| Forêt de Viñuela (64) ⚠️ | Viñuela | 4 |
| Bois de Málaga (239) ⚠️ | Málaga | 4 |
| Forêt de Humilladero (4) ⚠️ | Humilladero | 4 |
| Forêt de Antequera (31) ⚠️ | Antequera | 4 |
| Forêt de Antequera (41) ⚠️ | Antequera | 4 |
| Forêt de Ojén (63) ⚠️ | Ojén | 4 |
| Forêt de Coín (5) ⚠️ | Coín | 4 |
| Forêt de Istán (6) ⚠️ | Istán | 4 |
| Forêt de Monda (24) ⚠️ | Monda | 4 |
| Forêt de Ojén (82) ⚠️ | Ojén | 4 |
| Forêt de Ojén (83) ⚠️ | Ojén | 4 |
| Bois de Málaga (387) ⚠️ | Málaga | 4 |
| Forêt de Villanueva del Rosario (9) ⚠️ | Villanueva del Rosario | 4 |
| Bois de Villanueva del Rosario ⚠️ | Villanueva del Rosario | 4 |
| Bois de Antequera (10) ⚠️ | Antequera | 4 |
| Bois de Antequera (22) ⚠️ | Antequera | 4 |
| Bois de Villanueva del Rosario (6) ⚠️ | Villanueva del Rosario | 4 |
| Bois de Riogordo (4) ⚠️ | Riogordo | 4 |
| Bois de Álora ⚠️ | Álora | 4 |
| Bois de Comares (3) ⚠️ | Comares | 4 |
| Bois de Teba ⚠️ | Teba | 4 |
| Forêt de Marbella (53) ⚠️ | Marbella | 4 |
| Bois de Málaga (631) ⚠️ | Málaga | 4 |
| Bois de Frigiliana (4) ⚠️ | Frigiliana | 4 |
| Bois de Antequera (39) ⚠️ | Antequera | 4 |
| Bois de Málaga (701) ⚠️ | Málaga | 4 |
| Bois de Ardales (2) ⚠️ | Ardales | 4 |
| Bois de Benahavís (21) ⚠️ | Benahavís | 4 |
| Forêt de Marbella (54) ⚠️ | Marbella | 4 |
| Parc de Málaga (249) ⚠️ | Málaga | 4 |
| Forêt de Tolox (87) ⚠️ | Tolox | 4 |
| Parque de la Paloma ⚠️ | Benalmádena | 3 |
| Parque Botanico El Cerezal ⚠️ | Ojén | 3 |
| Forêt de Marbella (10) ⚠️ | Marbella | 3 |
| Forêt de Mijas (149) ⚠️ | Mijas | 3 |
| Forêt de Mijas (187) ⚠️ | Mijas | 3 |
| Forêt de Alhaurín el Grande (39) ⚠️ | Alhaurín el Grande | 3 |
| Forêt de Mijas (353) ⚠️ | Mijas | 3 |
| Forêt de Ronda ⚠️ | Ronda | 3 |
| Forêt de Ronda (3) ⚠️ | Ronda | 3 |
| Forêt de Ronda (4) ⚠️ | Ronda | 3 |
| Forêt de Antequera (10) ⚠️ | Antequera | 3 |
| Parque Forestal Andrés Jiménez Díaz ⚠️ | Málaga | 3 |
| Forêt de Villanueva del Trabuco ⚠️ | Villanueva del Trabuco | 3 |
| Forêt de Vélez-Málaga (46) ⚠️ | Vélez-Málaga | 3 |
| Forêt de Mijas (364) ⚠️ | Mijas | 3 |
| Forêt de Mijas (368) ⚠️ | Mijas | 3 |
| Forêt de Villanueva del Trabuco (10) ⚠️ | Villanueva del Trabuco | 3 |
| Forêt de Periana (13) ⚠️ | Periana | 3 |
| Forêt de Periana (15) ⚠️ | Periana | 3 |
| Forêt de Viñuela (27) ⚠️ | Viñuela | 3 |
| Forêt de Comares (6) ⚠️ | Comares | 3 |
| Forêt de El Borge (3) ⚠️ | El Borge | 3 |
| Forêt de Vélez-Málaga (223) ⚠️ | Vélez-Málaga | 3 |
| Bois de Marbella (25) ⚠️ | Marbella | 3 |
| Bois de Marbella (51) ⚠️ | Marbella | 3 |
| Bois de Marbella (73) ⚠️ | Marbella | 3 |
| Bois de Mijas (34) ⚠️ | Mijas | 3 |
| Bois de Mijas (35) ⚠️ | Mijas | 3 |
| Forêt de Tolox (19) ⚠️ | Tolox | 3 |
| Forêt de Tolox (27) ⚠️ | Tolox | 3 |
| Forêt de Tolox (29) ⚠️ | Tolox | 3 |
| Forêt de Yunquera (11) ⚠️ | Yunquera | 3 |
| Forêt de Igualeja ⚠️ | Igualeja | 3 |
| Forêt de Canillas de Albaida (5) ⚠️ | Canillas de Albaida | 3 |
| Forêt de Sedella (3) ⚠️ | Sedella | 3 |
| Forêt de Salares (10) ⚠️ | Salares | 3 |
| Forêt de Sedella (10) ⚠️ | Sedella | 3 |
| Forêt de Ojén (53) ⚠️ | Ojén | 3 |
| Forêt de Tolox (61) ⚠️ | Tolox | 3 |
| Bois de Tolox (10) ⚠️ | Tolox | 3 |
| Bois de Istán (4) ⚠️ | Istán | 3 |
| Bois de El Burgo (3) ⚠️ | El Burgo | 3 |
| Bois de Tolox (36) ⚠️ | Tolox | 3 |
| Bois de Yunquera ⚠️ | Yunquera | 3 |
| Bois de Ronda (12) ⚠️ | Ronda | 3 |
| Bois de Tolox (69) ⚠️ | Tolox | 3 |
| Bois de Yunquera (9) ⚠️ | Yunquera | 3 |
| Bois de Istán (14) ⚠️ | Istán | 3 |
| Bois de Monda (9) ⚠️ | Monda | 3 |
| Bois de Monda (20) ⚠️ | Monda | 3 |
| Bois de Monda (26) ⚠️ | Monda | 3 |
| Bois de Tolox (83) ⚠️ | Tolox | 3 |
| Bois de Tolox (88) ⚠️ | Tolox | 3 |
| Bois de Guaro (2) ⚠️ | Guaro | 3 |
| Bois de Istán (24) ⚠️ | Istán | 3 |
| Bois de Yunquera (29) ⚠️ | Yunquera | 3 |
| Bois de El Burgo (11) ⚠️ | El Burgo | 3 |
| Bois de El Burgo (14) ⚠️ | El Burgo | 3 |
| Bois de El Burgo (15) ⚠️ | El Burgo | 3 |
| Bois de El Burgo (17) ⚠️ | El Burgo | 3 |
| Bois de Istán (39) ⚠️ | Istán | 3 |
| Bois de Istán (49) ⚠️ | Istán | 3 |
| Bois de Ojén (6) ⚠️ | Ojén | 3 |
| Bois de Parauta (14) ⚠️ | Parauta | 3 |
| Bois de Parauta (16) ⚠️ | Parauta | 3 |
| Forêt de Viñuela (67) ⚠️ | Viñuela | 3 |
| Forêt de Canillas de Albaida (15) ⚠️ | Canillas de Albaida | 3 |
| Forêt de Periana (27) ⚠️ | Periana | 3 |
| Bois de Málaga (186) ⚠️ | Málaga | 3 |
| Bois de Málaga (199) ⚠️ | Málaga | 3 |
| Bois de Málaga (240) ⚠️ | Málaga | 3 |
| Forêt de Antequera (17) ⚠️ | Antequera | 3 |
| Forêt de Antequera (23) ⚠️ | Antequera | 3 |
| Forêt de Ojén (69) ⚠️ | Ojén | 3 |
| Forêt de Ojén (75) ⚠️ | Ojén | 3 |
| Ribera río Genil La Aceña ⚠️ | Cuevas de San Marcos | 3 |
| Forêt de Ojén (78) ⚠️ | Ojén | 3 |
| Forêt de Monda (22) ⚠️ | Monda | 3 |
| Forêt de Coín (16) ⚠️ | Coín | 3 |
| Forêt de Coín (19) ⚠️ | Coín | 3 |
| Forêt de Marbella (29) ⚠️ | Marbella | 3 |
| Forêt de Monda (28) ⚠️ | Monda | 3 |
| Forêt de Coín (22) ⚠️ | Coín | 3 |
| Bois de Antequera (26) ⚠️ | Antequera | 3 |
| Bois de Alcaucín (4) ⚠️ | Alcaucín | 3 |
| Forêt de Marbella (49) ⚠️ | Marbella | 3 |
| Forêt de Mijas (372) ⚠️ | Mijas | 3 |
| Bois de Málaga (560) ⚠️ | Málaga | 3 |
| Bois de Málaga (564) ⚠️ | Málaga | 3 |
| Forêt de Arenas (8) ⚠️ | Arenas | 3 |
| Forêt de Arenas (9) ⚠️ | Arenas | 3 |
| Bois de Málaga (653) ⚠️ | Málaga | 3 |
| Bois de Frigiliana (2) ⚠️ | Frigiliana | 3 |
| Bois de Nerja (11) ⚠️ | Nerja | 3 |
| Forêt de Ronda (13) ⚠️ | Ronda | 3 |
| Bois de Benahavís (5) ⚠️ | Benahavís | 3 |
| Bois de Benahavís (6) ⚠️ | Benahavís | 3 |
| Bois de Benahavís (25) ⚠️ | Benahavís | 3 |
| Bois de Montejaque (4) ⚠️ | Montejaque | 3 |
| Bois de Ojén (9) ⚠️ | Ojén | 3 |
| Parc de Málaga (255) ⚠️ | Málaga | 3 |
| Parque de Huelin ⚠️ | Málaga | 2 |
| Parc de Vélez-Málaga ⚠️ | Vélez-Málaga | 2 |
| Pinar Molino del Moro ⚠️ | Torremolinos | 2 |
| Parque del Oeste ⚠️ | Málaga | 2 |
| Parque La Batería ⚠️ | Torremolinos | 2 |
| Forêt de Marbella (2) ⚠️ | Marbella | 2 |
| Parque Litoral ⚠️ | Málaga | 2 |
| Forêt de Ojén (41) ⚠️ | Ojén | 2 |
| Forêt de Mijas (44) ⚠️ | Mijas | 2 |
| Forêt de Mijas (76) ⚠️ | Mijas | 2 |
| Forêt de Alhaurín el Grande (5) ⚠️ | Alhaurín el Grande | 2 |
| Forêt de Alhaurín el Grande (11) ⚠️ | Alhaurín el Grande | 2 |
| Forêt de Alhaurín el Grande (22) ⚠️ | Alhaurín el Grande | 2 |
| Forêt de Alhaurín el Grande (43) ⚠️ | Alhaurín el Grande | 2 |
| Palmeral de las Sorpresas ⚠️ | Málaga | 2 |
| Parque San Miguel ⚠️ | Málaga | 2 |
| Parque de Santa Ana ⚠️ | Málaga | 2 |
| Forêt de Marbella (11) ⚠️ | Marbella | 2 |
| Forêt de Ronda (2) ⚠️ | Ronda | 2 |
| Tholos de El Romeral ⚠️ | Antequera | 2 |
| Parque de la Memoria ⚠️ | Málaga | 2 |
| Forêt de Villanueva del Trabuco (2) ⚠️ | Villanueva del Trabuco | 2 |
| Forêt de Villanueva del Trabuco (7) ⚠️ | Villanueva del Trabuco | 2 |
| Forêt de Villanueva del Trabuco (8) ⚠️ | Villanueva del Trabuco | 2 |
| Forêt de Vélez-Málaga (4) ⚠️ | Vélez-Málaga | 2 |
| Forêt de Mijas (360) ⚠️ | Mijas | 2 |
| La Meca ⚠️ | Mijas | 2 |
| Forêt de Vélez-Málaga (12) ⚠️ | Vélez-Málaga | 2 |
| Forêt de Vélez-Málaga (33) ⚠️ | Vélez-Málaga | 2 |
| Forêt de Vélez-Málaga (36) ⚠️ | Vélez-Málaga | 2 |
| Vigil de Quiñones ⚠️ | Marbella | 2 |
| Forêt de Mijas (365) ⚠️ | Mijas | 2 |
| Forêt de Viñuela (2) ⚠️ | Viñuela | 2 |
| Forêt de Viñuela (5) ⚠️ | Viñuela | 2 |
| Forêt de Viñuela (6) ⚠️ | Viñuela | 2 |
| Forêt de Viñuela (8) ⚠️ | Viñuela | 2 |
| Forêt de Periana (17) ⚠️ | Periana | 2 |
| Forêt de Viñuela (25) ⚠️ | Viñuela | 2 |
| Forêt de Viñuela (31) ⚠️ | Viñuela | 2 |
| Forêt de Viñuela (33) ⚠️ | Alcaucín | 2 |
| Forêt de Viñuela (44) ⚠️ | Viñuela | 2 |
| Forêt de Vélez-Málaga (89) ⚠️ | Vélez-Málaga | 2 |
| Forêt de Vélez-Málaga (112) ⚠️ | Vélez-Málaga | 2 |
| Forêt de Rincón de la Victoria (2) ⚠️ | Rincón de la Victoria | 2 |
| Forêt de Vélez-Málaga (150) ⚠️ | Vélez-Málaga | 2 |
| Forêt de Almáchar (3) ⚠️ | Almáchar | 2 |
| Hoya de Las Cabras ⚠️ | Rincón de la Victoria | 2 |
| Forêt de Rincón de la Victoria (12) ⚠️ | Rincón de la Victoria | 2 |
| Bois de Marbella (3) ⚠️ | Marbella | 2 |
| Forêt de Vélez-Málaga (248) ⚠️ | Vélez-Málaga | 2 |
| Forêt de Vélez-Málaga (252) ⚠️ | Vélez-Málaga | 2 |
| Parque natural ⚠️ | Fuengirola | 2 |
| Forêt de Rincón de la Victoria (38) ⚠️ | Rincón de la Victoria | 2 |
| Bois de Marbella (18) ⚠️ | Marbella | 2 |
| Bois de Marbella (30) ⚠️ | Marbella | 2 |
| Bois de Ojén ⚠️ | Ojén | 2 |
| Parc de Marbella (57) ⚠️ | Marbella | 2 |
| Bois de Marbella (48) ⚠️ | Marbella | 2 |
| Forêt de Marbella (18) ⚠️ | Marbella | 2 |
| Parque de los Niños ⚠️ | Estepona | 2 |
| Bois de Cártama (3) ⚠️ | Cártama | 2 |
| Bois de Málaga (32) ⚠️ | Málaga | 2 |
| Parc de Alhaurín de la Torre (21) ⚠️ | Alhaurín de la Torre | 2 |
| Bois de Mijas (33) ⚠️ | Mijas | 2 |
| Parque Atalaya ⚠️ | Antequera | 2 |
| Bois de Málaga (41) ⚠️ | Málaga | 2 |
| Pinar Baños ⚠️ | Estepona | 2 |
| Bois de Mijas (39) ⚠️ | Mijas | 2 |
| Forêt de Tolox (11) ⚠️ | Tolox | 2 |
| Forêt de Yunquera (8) ⚠️ | Yunquera | 2 |
| Forêt de Tolox (15) ⚠️ | Tolox | 2 |
| Forêt de Alozaina (2) ⚠️ | Alozaina | 2 |
| Bois de Mijas (54) ⚠️ | Mijas | 2 |
| Forêt de Guaro ⚠️ | Guaro | 2 |
| Bois de Mijas (57) ⚠️ | Mijas | 2 |
| Parque Fluvial Rio Fuengirola (3) ⚠️ | Fuengirola | 2 |
| Bois de Málaga (51) ⚠️ | Málaga | 2 |
| Forêt de Benahavís (3) ⚠️ | Benahavís | 2 |
| Bois de Málaga (59) ⚠️ | Málaga | 2 |
| Forêt de Villanueva del Trabuco (18) ⚠️ | Villanueva del Trabuco | 2 |
| Bois de Villanueva del Trabuco (3) ⚠️ | Villanueva del Trabuco | 2 |
| Bois de Málaga (74) ⚠️ | Málaga | 2 |
| Forêt de Salares (2) ⚠️ | Salares | 2 |
| Forêt de Sedella (2) ⚠️ | Sedella | 2 |
| Forêt de Canillas de Albaida (10) ⚠️ | Canillas de Albaida | 2 |
| Forêt de Salares (9) ⚠️ | Salares | 2 |
| Forêt de Sedella (4) ⚠️ | Sedella | 2 |
| Forêt de Salares (12) ⚠️ | Salares | 2 |
| Forêt de Sedella (7) ⚠️ | Sedella | 2 |
| Forêt de Sedella (8) ⚠️ | Sedella | 2 |
| Forêt de Ojén (52) ⚠️ | Ojén | 2 |
| Bois de Málaga (97) ⚠️ | Málaga | 2 |
| Bois de Ronda (3) ⚠️ | Ronda | 2 |
| Bois de Tolox (3) ⚠️ | Tolox | 2 |
| Bois de Tolox (4) ⚠️ | Tolox | 2 |
| Forêt de Tolox (41) ⚠️ | Tolox | 2 |
| Forêt de Tolox (42) ⚠️ | Tolox | 2 |
| Forêt de Tolox (51) ⚠️ | Tolox | 2 |
| Forêt de Tolox (59) ⚠️ | Tolox | 2 |
| Forêt de Tolox (63) ⚠️ | Tolox | 2 |
| Forêt de Tolox (65) ⚠️ | Tolox | 2 |
| Forêt de Monda (7) ⚠️ | Monda | 2 |
| Forêt de Monda (9) ⚠️ | Monda | 2 |
| Bois de Tolox (21) ⚠️ | Tolox | 2 |
| Bois de Istán (5) ⚠️ | Istán | 2 |
| Bois de Ronda (6) ⚠️ | Ronda | 2 |
| Bois de Ronda (7) ⚠️ | Ronda | 2 |
| Bois de Ronda (9) ⚠️ | Ronda | 2 |
| Bois de Málaga (115) ⚠️ | Málaga | 2 |
| Bois de Tolox (42) ⚠️ | Tolox | 2 |
| Bois de Ronda (13) ⚠️ | Ronda | 2 |
| Bois de Tolox (59) ⚠️ | Tolox | 2 |
| Bois de Tolox (61) ⚠️ | Tolox | 2 |
| Bois de Tolox (72) ⚠️ | Tolox | 2 |
| Bois de Monda (16) ⚠️ | Monda | 2 |
| Bois de Istán (20) ⚠️ | Istán | 2 |
| Bois de Istán (23) ⚠️ | Istán | 2 |
| Bois de Parauta (3) ⚠️ | Istán | 2 |
| Bois de Istán (32) ⚠️ | Istán | 2 |
| Bois de Parauta (11) ⚠️ | Parauta | 2 |
| Bois de Parauta (12) ⚠️ | Parauta | 2 |
| Bois de Parauta (13) ⚠️ | Parauta | 2 |
| Bois de Yunquera (40) ⚠️ | Yunquera | 2 |
| Bois de Ronda (19) ⚠️ | Ronda | 2 |
| Bois de Istán (41) ⚠️ | Istán | 2 |
| Bois de Benahavís (3) ⚠️ | Benahavís | 2 |
| Bois de Monda (37) ⚠️ | Monda | 2 |
| Bois de Monda (44) ⚠️ | Monda | 2 |
| Bois de Monda (54) ⚠️ | Monda | 2 |
| Bois de Monda (59) ⚠️ | Monda | 2 |
| Bois de Monda (61) ⚠️ | Monda | 2 |
| Bois de Alozaina (6) ⚠️ | Alozaina | 2 |
| Bois de Ronda (23) ⚠️ | Ronda | 2 |
| Bois de Yunquera (44) ⚠️ | Yunquera | 2 |
| Forêt de Alfarnate (6) ⚠️ | Alfarnate | 2 |
| Forêt de Periana (22) ⚠️ | Periana | 2 |
| Forêt de Periana (23) ⚠️ | Periana | 2 |
| Forêt de Alcaucín (14) ⚠️ | Alcaucín | 2 |
| Bois de Alcaucín (3) ⚠️ | Alcaucín | 2 |
| Forêt de Viñuela (63) ⚠️ | Viñuela | 2 |
| Forêt de Vélez-Málaga (255) ⚠️ | Vélez-Málaga | 2 |
| Bois de Málaga (167) ⚠️ | Málaga | 2 |
| Bois de Málaga (176) ⚠️ | Málaga | 2 |
| Bois de Tolox (97) ⚠️ | Tolox | 2 |
| Forêt de Cómpeta ⚠️ | Cómpeta | 2 |
| Bois de Canillas de Albaida (3) ⚠️ | Canillas de Albaida | 2 |
| Parc de Málaga (157) ⚠️ | Málaga | 2 |
| Parque 54 ⚠️ | Rincón de la Victoria | 2 |
| Bois de Málaga (247) ⚠️ | Málaga | 2 |
| Bois de Málaga (254) ⚠️ | Málaga | 2 |
| Parque Marítimo Terrestre Peñón del Cuervo ⚠️ | Málaga | 2 |
| Forêt de Humilladero (2) ⚠️ | Humilladero | 2 |
| Forêt de Antequera (30) ⚠️ | Antequera | 2 |
| Forêt de Villanueva de la Concepción (2) ⚠️ | Villanueva de la Concepción | 2 |
| Parque Torneros ⚠️ | Fuengirola | 2 |
| Bois de Málaga (297) ⚠️ | Málaga | 2 |
| Forêt de Istán (2) ⚠️ | Istán | 2 |
| Forêt de Ojén (65) ⚠️ | Ojén | 2 |
| Forêt de Ojén (67) ⚠️ | Ojén | 2 |
| Forêt de Istán (3) ⚠️ | Istán | 2 |
| Forêt de Ojén (70) ⚠️ | Ojén | 2 |
| Forêt de Ojén (74) ⚠️ | Ojén | 2 |
| Parque Atalaya (2) ⚠️ | Antequera | 2 |
| Forêt de Ojén (76) ⚠️ | Ojén | 2 |
| Forêt de Coín (6) ⚠️ | Coín | 2 |
| Forêt de Monda (17) ⚠️ | Monda | 2 |
| Forêt de Coín (9) ⚠️ | Coín | 2 |
| Forêt de Monda (27) ⚠️ | Monda | 2 |
| Bois de Málaga (360) ⚠️ | Málaga | 2 |
| Bois de Málaga (386) ⚠️ | Málaga | 2 |
| Forêt de Ojén (88) ⚠️ | Ojén | 2 |
| Forêt de Ojén (90) ⚠️ | Ojén | 2 |
| Forêt de Colmenar (11) ⚠️ | Colmenar | 2 |
| Bois de Antequera (4) ⚠️ | Antequera | 2 |
| Bois de Antequera (6) ⚠️ | Antequera | 2 |
| Bois de Antequera (21) ⚠️ | Antequera | 2 |
| Bois de Colmenar (4) ⚠️ | Colmenar | 2 |
| Forêt de Colmenar (12) ⚠️ | Colmenar | 2 |
| Forêt de Marbella (40) ⚠️ | Marbella | 2 |
| Forêt de Marbella (45) ⚠️ | Marbella | 2 |
| Forêt de Marbella (50) ⚠️ | Marbella | 2 |
| Bois de Málaga (434) ⚠️ | Málaga | 2 |
| Bois de Málaga (504) ⚠️ | Málaga | 2 |
| Bois de Málaga (515) ⚠️ | Málaga | 2 |
| Bois de Málaga (521) ⚠️ | Málaga | 2 |
| Parc de Benalmádena (17) ⚠️ | Benalmádena | 2 |
| Bois de Málaga (573) ⚠️ | Málaga | 2 |
| Parc de Benalmádena (20) ⚠️ | Benalmádena | 2 |
| Forêt de Mijas (419) ⚠️ | Mijas | 2 |
| Bois de Mijas (97) ⚠️ | Mijas | 2 |
| Forêt de Mijas (423) ⚠️ | Mijas | 2 |
| Bois de Nerja ⚠️ | Nerja | 2 |
| Bois de Nerja (8) ⚠️ | Nerja | 2 |
| Bois de Nerja (9) ⚠️ | Nerja | 2 |
| Bois de Málaga (670) ⚠️ | Málaga | 2 |
| Bois de Málaga (676) ⚠️ | Málaga | 2 |
| Bois de Málaga (690) ⚠️ | Málaga | 2 |
| Bois de Málaga (697) ⚠️ | Málaga | 2 |
| Bois de Benahavís (22) ⚠️ | Benahavís | 2 |
| Bois de Benahavís (23) ⚠️ | Benahavís | 2 |
| Bois de Benahavís (24) ⚠️ | Benahavís | 2 |
| Bois de Benahavís (26) ⚠️ | Benahavís | 2 |
| Bois de Mijas (102) ⚠️ | Mijas | 2 |
| Bois de Frigiliana (19) ⚠️ | Frigiliana | 2 |
| Parc de Estepona (30) ⚠️ | Estepona | 2 |
| Parque Virgen de Araceli ⚠️ | Málaga | 2 |
| Parque de Málaga ⚠️ | Málaga | 2 |
| Jardines Calle Pirandello ⚠️ | Málaga | 2 |
| Parc de Málaga (261) ⚠️ | Málaga | 2 |
| Bois de Málaga (722) ⚠️ | Málaga | 2 |
| Bois de Málaga (726) ⚠️ | Málaga | 2 |
| Jardines de la Muralla ⚠️ | Mijas | 1 |
| Parque Verano Azul ⚠️ | Nerja | 1 |
| Parque del Calvario ⚠️ | Estepona | 1 |
| Zona verde ⚠️ | Vélez-Málaga | 1 |
| Parc de Marbella ⚠️ | Marbella | 1 |
| Parc de Alhaurín de la Torre ⚠️ | Alhaurín de la Torre | 1 |
| Parc de Vélez-Málaga (6) ⚠️ | Vélez-Málaga | 1 |
| Parc de Vélez-Málaga (8) ⚠️ | Vélez-Málaga | 1 |
| Parc de Algarrobo (2) ⚠️ | Algarrobo | 1 |
| Parc de Nerja (6) ⚠️ | Nerja | 1 |
| Parc de Vélez-Málaga (13) ⚠️ | Vélez-Málaga | 1 |
| Parque María Zambrano ⚠️ | Vélez-Málaga | 1 |
| Parque Juan Jurado Lorca ⚠️ | Vélez-Málaga | 1 |
| Parc de Vélez-Málaga (25) ⚠️ | Vélez-Málaga | 1 |
| Park Rosalia de Castro ⚠️ | Nerja | 1 |
| Parque del Sol ⚠️ | Fuengirola | 1 |
| Parc de Málaga (10) ⚠️ | Málaga | 1 |
| Parc de Málaga (11) ⚠️ | Málaga | 1 |
| Jardines Carmen Fernanda ⚠️ | Málaga | 1 |
| Parc de Málaga (12) ⚠️ | Málaga | 1 |
| Forêt de Marbella (4) ⚠️ | Marbella | 1 |
| Forêt de Marbella (5) ⚠️ | Marbella | 1 |
| Parque Marqués del Duero ⚠️ | Marbella | 1 |
| Bois de Málaga (4) ⚠️ | Málaga | 1 |
| Jardín botánico Santa Fiora ⚠️ | Frigiliana | 1 |
| Plaza Marqués del Turia ⚠️ | Marbella | 1 |
| Plaza de Antonio Banderas ⚠️ | Marbella | 1 |
| Parque de la Escalerilla ⚠️ | Algarrobo | 1 |
| Forêt de Algarrobo ⚠️ | Algarrobo | 1 |
| Bois de Málaga (5) ⚠️ | Málaga | 1 |
| Bois de Málaga (6) ⚠️ | Málaga | 1 |
| Parque del Carmen ⚠️ | Estepona | 1 |
| Forêt de Mijas (13) ⚠️ | Mijas | 1 |
| Forêt de Mijas (79) ⚠️ | Mijas | 1 |
| Forêt de Mijas (81) ⚠️ | Mijas | 1 |
| Forêt de Mijas (93) ⚠️ | Mijas | 1 |
| Forêt de Mijas (120) ⚠️ | Mijas | 1 |
| Forêt de Mijas (125) ⚠️ | Mijas | 1 |
| Forêt de Mijas (147) ⚠️ | Mijas | 1 |
| Forêt de Mijas (189) ⚠️ | Mijas | 1 |
| Forêt de Mijas (209) ⚠️ | Mijas | 1 |
| Forêt de Mijas (224) ⚠️ | Mijas | 1 |
| Forêt de Mijas (235) ⚠️ | Mijas | 1 |
| Forêt de Mijas (258) ⚠️ | Mijas | 1 |
| Forêt de Mijas (308) ⚠️ | Mijas | 1 |
| Forêt de Mijas (316) ⚠️ | Mijas | 1 |
| Forêt de Mijas (318) ⚠️ | Mijas | 1 |
| Forêt de Mijas (326) ⚠️ | Mijas | 1 |
| Parc de Alhaurín de la Torre (2) ⚠️ | Alhaurín de la Torre | 1 |
| Parc de Alhaurín de la Torre (5) ⚠️ | Alhaurín de la Torre | 1 |
| Forêt de Alhaurín el Grande (2) ⚠️ | Alhaurín el Grande | 1 |
| Forêt de Alhaurín el Grande (4) ⚠️ | Alhaurín el Grande | 1 |
| Forêt de Alhaurín el Grande (6) ⚠️ | Alhaurín el Grande | 1 |
| Forêt de Alhaurín el Grande (15) ⚠️ | Alhaurín el Grande | 1 |
| Forêt de Alhaurín el Grande (17) ⚠️ | Alhaurín el Grande | 1 |
| Forêt de Alhaurín el Grande (19) ⚠️ | Alhaurín el Grande | 1 |
| Forêt de Alhaurín el Grande (21) ⚠️ | Alhaurín el Grande | 1 |
| Forêt de Alhaurín el Grande (26) ⚠️ | Alhaurín el Grande | 1 |
| Forêt de Mijas (355) ⚠️ | Mijas | 1 |
| Parque P. Antonio Godino ⚠️ | Gaucín | 1 |
| Jardín Músico Manuel del Campo ⚠️ | Málaga | 1 |
| Parque de Manuel Navarrete ⚠️ | Málaga | 1 |
| Parc de Málaga (23) ⚠️ | Málaga | 1 |
| Forêt de Ojén (49) ⚠️ | Ojén | 1 |
| Forêt de Marbella (16) ⚠️ | Marbella | 1 |
| Bois de Málaga (9) ⚠️ | Málaga | 1 |
| Parque Lineal José Carlos Fajardo ⚠️ | Málaga | 1 |
| Parque Princesa Diana ⚠️ | Mijas | 1 |
| Parque Municipal de la Concordia ⚠️ | Alhaurín de la Torre | 1 |
| Forêt de Ronda (7) ⚠️ | Ronda | 1 |
| Forêt de Ronda (9) ⚠️ | Ronda | 1 |
| Parque Periurbano "Río de La Villa" ⚠️ | Coín | 1 |
| Bois de Fuengirola ⚠️ | Fuengirola | 1 |
| Parc de Málaga (38) ⚠️ | Málaga | 1 |
| Parque El Esparragal ⚠️ | Mijas | 1 |
| Forêt de Marbella (17) ⚠️ | Marbella | 1 |
| Parque "María Cristina" ⚠️ | Antequera | 1 |
| Finca El Portón ⚠️ | Alhaurín de la Torre | 1 |
| Parc de Alhaurín de la Torre (12) ⚠️ | Alhaurín de la Torre | 1 |
| Parc de Alhaurín de la Torre (15) ⚠️ | Alhaurín de la Torre | 1 |
| Parque del Paseo ⚠️ | Antequera | 1 |
| Plaza Era Alta ⚠️ | Mollina | 1 |
| Parc de Málaga (39) ⚠️ | Málaga | 1 |
| Forêt de Antequera (7) ⚠️ | Antequera | 1 |
| Forêt de Antequera (8) ⚠️ | Antequera | 1 |
| Parque San Agustín ⚠️ | Coín | 1 |
| Parque de la Libertad ⚠️ | Alhaurín el Grande | 1 |
| Parc de Torremolinos (2) ⚠️ | Torremolinos | 1 |
| Parc de Málaga (46) ⚠️ | Málaga | 1 |
| Forêt de Villanueva del Trabuco (6) ⚠️ | Villanueva del Trabuco | 1 |
| Bois de Ronda ⚠️ | Ronda | 1 |
| Parque de Santa Paula ⚠️ | Málaga | 1 |
| Parc de Rincón de la Victoria (4) ⚠️ | Rincón de la Victoria | 1 |
| Parc de Mijas (19) ⚠️ | Mijas | 1 |
| Jardín de los Remedios ⚠️ | Vélez-Málaga | 1 |
| Alcazaba-Fortaleza ⚠️ | Vélez-Málaga | 1 |
| Parque Los Olivos ⚠️ | Mijas | 1 |
| Parc de Torremolinos (4) ⚠️ | Torremolinos | 1 |
| Parc de Marbella (19) ⚠️ | Marbella | 1 |
| Parc de Marbella (20) ⚠️ | Marbella | 1 |
| Parc de Marbella (21) ⚠️ | Marbella | 1 |
| Parc de Marbella (33) ⚠️ | Marbella | 1 |
| Parc de Marbella (39) ⚠️ | Marbella | 1 |
| Parc de Marbella (40) ⚠️ | Marbella | 1 |
| Bois de Vélez-Málaga ⚠️ | Vélez-Málaga | 1 |
| Bois de Vélez-Málaga (2) ⚠️ | Vélez-Málaga | 1 |
| Forêt de Vélez-Málaga (27) ⚠️ | Vélez-Málaga | 1 |
| Forêt de Vélez-Málaga (31) ⚠️ | Vélez-Málaga | 1 |
| Forêt de Vélez-Málaga (32) ⚠️ | Vélez-Málaga | 1 |
| Forêt de Vélez-Málaga (35) ⚠️ | Vélez-Málaga | 1 |
| Forêt de Vélez-Málaga (41) ⚠️ | Vélez-Málaga | 1 |
| Forêt de Vélez-Málaga (42) ⚠️ | Vélez-Málaga | 1 |
| Forêt de Vélez-Málaga (51) ⚠️ | Vélez-Málaga | 1 |
| Forêt de Vélez-Málaga (57) ⚠️ | Vélez-Málaga | 1 |
| Forêt de Vélez-Málaga (58) ⚠️ | Vélez-Málaga | 1 |
| Forêt de Arenas ⚠️ | Arenas | 1 |
| Forêt de Viñuela ⚠️ | Viñuela | 1 |
| Forêt de Vélez-Málaga (65) ⚠️ | Vélez-Málaga | 1 |
| Parc de Vélez-Málaga (44) ⚠️ | Vélez-Málaga | 1 |
| Parc de Vélez-Málaga (45) ⚠️ | Vélez-Málaga | 1 |
| Parc de Mijas (33) ⚠️ | Mijas | 1 |
| Parque Homenaje a la Mujer Antequerana ⚠️ | Antequera | 1 |
| Forêt de Alhaurín el Grande (46) ⚠️ | Alhaurín el Grande | 1 |
| Forêt de Mijas (367) ⚠️ | Mijas | 1 |
| Forêt de Mijas (369) ⚠️ | Mijas | 1 |
| Parc de Vélez-Málaga (62) ⚠️ | Vélez-Málaga | 1 |
| Parc de Vélez-Málaga (63) ⚠️ | Vélez-Málaga | 1 |
| Forêt de Benamocarra ⚠️ | Benamocarra | 1 |
| Parque Robert Baden Powell ⚠️ | Málaga | 1 |
| Bois de Málaga (20) ⚠️ | Málaga | 1 |
| Forêt de Periana (3) ⚠️ | Periana | 1 |
| Forêt de Periana (10) ⚠️ | Periana | 1 |
| Forêt de Periana (11) ⚠️ | Periana | 1 |
| Forêt de Periana (12) ⚠️ | Periana | 1 |
| Forêt de Periana (14) ⚠️ | Periana | 1 |
| Forêt de Viñuela (9) ⚠️ | Viñuela | 1 |
| Forêt de Viñuela (12) ⚠️ | Viñuela | 1 |
| Forêt de Periana (18) ⚠️ | Periana | 1 |
| Forêt de Viñuela (23) ⚠️ | Viñuela | 1 |
| Forêt de Viñuela (24) ⚠️ | Viñuela | 1 |
| Forêt de Colmenar (2) ⚠️ | Colmenar | 1 |
| Forêt de Alcaucín (4) ⚠️ | Alcaucín | 1 |
| Parc de Málaga (58) ⚠️ | Málaga | 1 |
| Forêt de Alcaucín (6) ⚠️ | Alcaucín | 1 |
| Forêt de Alcaucín (7) ⚠️ | Alcaucín | 1 |
| Forêt de Alcaucín (8) ⚠️ | Alcaucín | 1 |
| Forêt de Viñuela (34) ⚠️ | Viñuela | 1 |
| Forêt de Viñuela (38) ⚠️ | Viñuela | 1 |
| Forêt de Viñuela (39) ⚠️ | Viñuela | 1 |
| Forêt de Viñuela (50) ⚠️ | Viñuela | 1 |
| Forêt de Viñuela (51) ⚠️ | Viñuela | 1 |
| Forêt de Viñuela (53) ⚠️ | Viñuela | 1 |
| Forêt de Vélez-Málaga (74) ⚠️ | Vélez-Málaga | 1 |
| Forêt de Vélez-Málaga (80) ⚠️ | Vélez-Málaga | 1 |
| Forêt de Vélez-Málaga (91) ⚠️ | Vélez-Málaga | 1 |
| Forêt de Vélez-Málaga (104) ⚠️ | Vélez-Málaga | 1 |
| Forêt de Riogordo ⚠️ | Riogordo | 1 |
| Forêt de Riogordo (2) ⚠️ | Riogordo | 1 |
| Forêt de Vélez-Málaga (133) ⚠️ | Vélez-Málaga | 1 |
| Forêt de Vélez-Málaga (135) ⚠️ | Vélez-Málaga | 1 |
| Bois de Málaga (22) ⚠️ | Málaga | 1 |
| Forêt de Vélez-Málaga (138) ⚠️ | Vélez-Málaga | 1 |
| Forêt de Vélez-Málaga (142) ⚠️ | Vélez-Málaga | 1 |
| Forêt de Vélez-Málaga (146) ⚠️ | Vélez-Málaga | 1 |
| Forêt de Rincón de la Victoria (8) ⚠️ | Rincón de la Victoria | 1 |
| Forêt de Rincón de la Victoria (11) ⚠️ | Rincón de la Victoria | 1 |
| Forêt de Vélez-Málaga (151) ⚠️ | Vélez-Málaga | 1 |
| Forêt de Vélez-Málaga (152) ⚠️ | Vélez-Málaga | 1 |
| Parque Xarblanca ⚠️ | Marbella | 1 |
| Jardines de Carmen Thyssen ⚠️ | Estepona | 1 |
| Parc de Estepona (5) ⚠️ | Estepona | 1 |
| Parque de los Derechos Humanos ⚠️ | Estepona | 1 |
| Forêt de Vélez-Málaga (167) ⚠️ | Vélez-Málaga | 1 |
| Forêt de Vélez-Málaga (168) ⚠️ | Vélez-Málaga | 1 |
| Forêt de Algarrobo (12) ⚠️ | Algarrobo | 1 |
| Forêt de Vélez-Málaga (188) ⚠️ | Vélez-Málaga | 1 |
| Forêt de Vélez-Málaga (191) ⚠️ | Vélez-Málaga | 1 |
| Forêt de Vélez-Málaga (204) ⚠️ | Vélez-Málaga | 1 |
| Forêt de Vélez-Málaga (219) ⚠️ | Vélez-Málaga | 1 |
| Forêt de Vélez-Málaga (222) ⚠️ | Vélez-Málaga | 1 |
| Parc de Algarrobo (9) ⚠️ | Algarrobo | 1 |
| Forêt de Periana (21) ⚠️ | Periana | 1 |
| Bois de Antequera ⚠️ | Antequera | 1 |
| Parc de Villanueva del Trabuco (24) ⚠️ | Villanueva del Trabuco | 1 |
| Parque Martiricos ⚠️ | Málaga | 1 |
| Forêt de Algarrobo (15) ⚠️ | Algarrobo | 1 |
| Forêt de Algarrobo (24) ⚠️ | Algarrobo | 1 |
| Forêt de Algarrobo (25) ⚠️ | Algarrobo | 1 |
| Forêt de Sayalonga (2) ⚠️ | Sayalonga | 1 |
| Parc de Málaga (63) ⚠️ | Málaga | 1 |
| Parc de Marbella (44) ⚠️ | Marbella | 1 |
| Forêt de Vélez-Málaga (231) ⚠️ | Vélez-Málaga | 1 |
| Forêt de Vélez-Málaga (234) ⚠️ | Vélez-Málaga | 1 |
| Parc de Torremolinos (7) ⚠️ | Torremolinos | 1 |
| Parc de Alozaina ⚠️ | Alozaina | 1 |
| Parc de Humilladero (9) ⚠️ | Humilladero | 1 |
| Parc de Humilladero (15) ⚠️ | Humilladero | 1 |
| Parc de Torremolinos (8) ⚠️ | Torremolinos | 1 |
| Forêt de Vélez-Málaga (236) ⚠️ | Vélez-Málaga | 1 |
| Forêt de Vélez-Málaga (253) ⚠️ | Vélez-Málaga | 1 |
| Forêt de Rincón de la Victoria (25) ⚠️ | Rincón de la Victoria | 1 |
| Forêt de Rincón de la Victoria (26) ⚠️ | Rincón de la Victoria | 1 |
| Forêt de Rincón de la Victoria (28) ⚠️ | Rincón de la Victoria | 1 |
| Forêt de Rincón de la Victoria (34) ⚠️ | Rincón de la Victoria | 1 |
| Forêt de Rincón de la Victoria (36) ⚠️ | Rincón de la Victoria | 1 |
| Bois de Málaga (31) ⚠️ | Málaga | 1 |
| Bois de Marbella (15) ⚠️ | Marbella | 1 |
| Bois de Mijas (10) ⚠️ | Mijas | 1 |
| Bois de Marbella (22) ⚠️ | Marbella | 1 |
| Bois de Marbella (23) ⚠️ | Marbella | 1 |
| Bois de Marbella (29) ⚠️ | Marbella | 1 |
| Bois de Marbella (31) ⚠️ | Marbella | 1 |
| Bois de Marbella (38) ⚠️ | Marbella | 1 |
| Bois de Marbella (88) ⚠️ | Marbella | 1 |
| Parc de Manilva (2) ⚠️ | Manilva | 1 |
| Bois de Mijas (23) ⚠️ | Mijas | 1 |
| Bois de Mijas (25) ⚠️ | Mijas | 1 |
| Bois de Cártama ⚠️ | Cártama | 1 |
| Forêt de Nerja (5) ⚠️ | Nerja | 1 |
| Jardín Veintiocho de Junio ⚠️ | Málaga | 1 |
| Parc de Málaga (77) ⚠️ | Málaga | 1 |
| Parc de Alhaurín de la Torre (22) ⚠️ | Alhaurín de la Torre | 1 |
| Parc de Málaga (82) ⚠️ | Málaga | 1 |
| Parque Gym Spinner ⚠️ | Benalmádena | 1 |
| Parque de Torre ⚠️ | Rincón de la Victoria | 1 |
| Bois de Mijas (30) ⚠️ | Mijas | 1 |
| Parc de Málaga (84) ⚠️ | Málaga | 1 |
| Parc de Benalmádena (11) ⚠️ | Benalmádena | 1 |
| Parc de Benalmádena (13) ⚠️ | Benalmádena | 1 |
| Parque Castillo Sohail ⚠️ | Fuengirola | 1 |
| Parc de Fuengirola (6) ⚠️ | Fuengirola | 1 |
| Parc de Benalmádena (14) ⚠️ | Benalmádena | 1 |
| Parc de Marbella (73) ⚠️ | Marbella | 1 |
| Parc de Marbella (74) ⚠️ | Marbella | 1 |
| Plaza de la Concordia ⚠️ | Marbella | 1 |
| Parc de Pizarra ⚠️ | Pizarra | 1 |
| Forêt de Comares (15) ⚠️ | Comares | 1 |
| Forêt de Comares (17) ⚠️ | Comares | 1 |
| Parc de Málaga (94) ⚠️ | Málaga | 1 |
| Parc de Málaga (95) ⚠️ | Málaga | 1 |
| Parc de Benamargosa ⚠️ | Benamargosa | 1 |
| Forêt de Cútar (5) ⚠️ | Cútar | 1 |
| Forêt de Estepona ⚠️ | Estepona | 1 |
| Forêt de El Borge (6) ⚠️ | El Borge | 1 |
| Forêt de Estepona (2) ⚠️ | Estepona | 1 |
| Bois de Mijas (42) ⚠️ | Mijas | 1 |
| Bois de Málaga (43) ⚠️ | Málaga | 1 |
| Bois de Málaga (45) ⚠️ | Málaga | 1 |
| Parc de Málaga (106) ⚠️ | Málaga | 1 |
| Parque Fluvial Rio Fuengirola ⚠️ | Fuengirola | 1 |
| Forêt de Yunquera (10) ⚠️ | Yunquera | 1 |
| Forêt de Tolox (30) ⚠️ | Tolox | 1 |
| Forêt de Alozaina (5) ⚠️ | Alozaina | 1 |
| Bois de Mijas (46) ⚠️ | Mijas | 1 |
| Bois de Mijas (52) ⚠️ | Mijas | 1 |
| Bois de Mijas (53) ⚠️ | Mijas | 1 |
| Parque Forestal Cerro Vallejo ⚠️ | Málaga | 1 |
| Bois de Mijas (55) ⚠️ | Mijas | 1 |
| Bois de Mijas (56) ⚠️ | Mijas | 1 |
| Bosque El Chaparral ⚠️ | Mijas | 1 |
| Forêt de Tolox (32) ⚠️ | Tolox | 1 |
| Forêt de Tolox (34) ⚠️ | Tolox | 1 |
| Parc de Fuengirola (12) ⚠️ | Fuengirola | 1 |
| Parc de Fuengirola (14) ⚠️ | Fuengirola | 1 |
| Forêt de Tolox (35) ⚠️ | Tolox | 1 |
| Forêt de Benahavís ⚠️ | Benahavís | 1 |
| Bois de Málaga (52) ⚠️ | Málaga | 1 |
| Parque Nuevo de Morana ⚠️ | Cuevas de San Marcos | 1 |
| Bois de Málaga (57) ⚠️ | Málaga | 1 |
| Parc de Málaga (121) ⚠️ | Málaga | 1 |
| Bois de Málaga (61) ⚠️ | Málaga | 1 |
| Parc de Cártama (7) ⚠️ | Cártama | 1 |
| Parque Ocio Water wheel ⚠️ | Torremolinos | 1 |
| Parc de Málaga (125) ⚠️ | Málaga | 1 |
| Bois de Málaga (63) ⚠️ | Málaga | 1 |
| Forêt de Villanueva del Trabuco (15) ⚠️ | Villanueva del Trabuco | 1 |
| Bois de Villanueva del Trabuco (7) ⚠️ | Villanueva del Trabuco | 1 |
| Bois de Villanueva del Trabuco (11) ⚠️ | Villanueva del Trabuco | 1 |
| Bois de Málaga (65) ⚠️ | Málaga | 1 |
| Bois de Málaga (67) ⚠️ | Málaga | 1 |
| Bois de Málaga (71) ⚠️ | Málaga | 1 |
| Parque Forestal Cerrado de Calderón ⚠️ | Málaga | 1 |
| Bois de Málaga (75) ⚠️ | Málaga | 1 |
| Bois de Málaga (81) ⚠️ | Málaga | 1 |
| Forêt de Canillas de Albaida (12) ⚠️ | Canillas de Albaida | 1 |
| Forêt de Sedella (6) ⚠️ | Sedella | 1 |
| Forêt de Sedella (11) ⚠️ | Canillas de Aceituno | 1 |
| Forêt de Canillas de Aceituno (5) ⚠️ | Canillas de Aceituno | 1 |
| Forêt de Canillas de Aceituno (6) ⚠️ | Canillas de Aceituno | 1 |
| Forêt de Sedella (13) ⚠️ | Sedella | 1 |
| Forêt de Sedella (14) ⚠️ | Sedella | 1 |
| Parc de Málaga (132) ⚠️ | Málaga | 1 |
| Bois de Málaga (88) ⚠️ | Málaga | 1 |
| Bois de Málaga (95) ⚠️ | Málaga | 1 |
| Bois de Málaga (105) ⚠️ | Málaga | 1 |
| Bois de Tolox ⚠️ | Tolox | 1 |
| Forêt de Tolox (39) ⚠️ | Tolox | 1 |
| Forêt de Tolox (45) ⚠️ | Tolox | 1 |
| Forêt de Monda (5) ⚠️ | Monda | 1 |
| Forêt de Monda (6) ⚠️ | Monda | 1 |
| Forêt de Tolox (57) ⚠️ | Tolox | 1 |
| Forêt de Tolox (60) ⚠️ | Tolox | 1 |
| Forêt de Tolox (66) ⚠️ | Tolox | 1 |
| Forêt de Tolox (73) ⚠️ | Tolox | 1 |
| Forêt de Tolox (75) ⚠️ | Tolox | 1 |
| Forêt de Tolox (78) ⚠️ | Tolox | 1 |
| Forêt de Tolox (79) ⚠️ | Tolox | 1 |
| Forêt de Monda (8) ⚠️ | Monda | 1 |
| Bois de Monda ⚠️ | Monda | 1 |
| Forêt de Tolox (85) ⚠️ | Tolox | 1 |
| Bois de Tolox (11) ⚠️ | Tolox | 1 |
| Bois de Tolox (14) ⚠️ | Tolox | 1 |
| Bois de Tolox (20) ⚠️ | Tolox | 1 |
| Bois de Ronda (4) ⚠️ | Ronda | 1 |
| Bois de Istán ⚠️ | Istán | 1 |
| Bois de Tolox (31) ⚠️ | Tolox | 1 |
| Bois de Istán (6) ⚠️ | Istán | 1 |
| Bois de Istán (7) ⚠️ | Istán | 1 |
| Bois de Tolox (34) ⚠️ | Tolox | 1 |
| Parc de Torremolinos (13) ⚠️ | Torremolinos | 1 |
| Parc de Torremolinos (14) ⚠️ | Torremolinos | 1 |
| Parque Mar de Alborán ⚠️ | Málaga | 1 |
| Bois de Málaga (119) ⚠️ | Málaga | 1 |
| Bois de Málaga (122) ⚠️ | Málaga | 1 |
| Bois de Málaga (123) ⚠️ | Málaga | 1 |
| Bois de Málaga (125) ⚠️ | Málaga | 1 |
| Bois de Tolox (39) ⚠️ | Tolox | 1 |
| Bois de Istán (10) ⚠️ | Tolox | 1 |
| Bois de Tolox (45) ⚠️ | Tolox | 1 |
| Bois de Tolox (48) ⚠️ | Alozaina | 1 |
| Bois de Tolox (50) ⚠️ | Tolox | 1 |
| Bois de Tolox (54) ⚠️ | Tolox | 1 |
| Bois de Ronda (11) ⚠️ | Ronda | 1 |
| Bois de Tolox (56) ⚠️ | Tolox | 1 |
| Bois de Tolox (58) ⚠️ | Tolox | 1 |
| Bois de Yunquera (2) ⚠️ | Yunquera | 1 |
| Bois de Yunquera (6) ⚠️ | Yunquera | 1 |
| Bois de Yunquera (7) ⚠️ | Yunquera | 1 |
| Bois de Tolox (65) ⚠️ | Tolox | 1 |
| Bois de Tolox (67) ⚠️ | Tolox | 1 |
| Bois de Tolox (71) ⚠️ | Tolox | 1 |
| Bois de Yunquera (8) ⚠️ | Tolox | 1 |
| Bois de Yunquera (14) ⚠️ | Yunquera | 1 |
| Bois de Istán (11) ⚠️ | Istán | 1 |
| Bois de Monda (3) ⚠️ | Monda | 1 |
| Bois de Monda (10) ⚠️ | Monda | 1 |
| Bois de Monda (11) ⚠️ | Monda | 1 |
| Bois de Monda (13) ⚠️ | Monda | 1 |
| Bois de Monda (18) ⚠️ | Monda | 1 |
| Bois de Monda (19) ⚠️ | Monda | 1 |
| Bois de Monda (22) ⚠️ | Monda | 1 |
| Bois de Alozaina (3) ⚠️ | Alozaina | 1 |
| Bois de Tolox (77) ⚠️ | Tolox | 1 |
| Bois de Tolox (78) ⚠️ | Tolox | 1 |
| Bois de Monda (25) ⚠️ | Monda | 1 |
| Bois de Istán (22) ⚠️ | Istán | 1 |
| Bois de Parauta (4) ⚠️ | Parauta | 1 |
| Bois de Parauta (6) ⚠️ | Parauta | 1 |
| Bois de Yunquera (20) ⚠️ | Yunquera | 1 |
| Bois de Málaga (132) ⚠️ | Málaga | 1 |
| Bois de Guaro ⚠️ | Guaro | 1 |
| Bois de Istán (26) ⚠️ | Istán | 1 |
| Bois de Monda (28) ⚠️ | Monda | 1 |
| Bois de Monda (30) ⚠️ | Monda | 1 |
| Bois de Monda (33) ⚠️ | Monda | 1 |
| Bois de Monda (34) ⚠️ | Monda | 1 |
| Bois de Yunquera (30) ⚠️ | Yunquera | 1 |
| Bois de Rincón de la Victoria (2) ⚠️ | Rincón de la Victoria | 1 |
| Bois de Yunquera (31) ⚠️ | Yunquera | 1 |
| Bois de Tolox (94) ⚠️ | Tolox | 1 |
| Bois de Yunquera (37) ⚠️ | Yunquera | 1 |
| Bois de El Burgo (8) ⚠️ | El Burgo | 1 |
| Bois de El Burgo (13) ⚠️ | El Burgo | 1 |
| Bois de Istán (27) ⚠️ | Istán | 1 |
| Bois de Istán (35) ⚠️ | Istán | 1 |
| Bois de Istán (37) ⚠️ | Istán | 1 |
| Bois de Istán (38) ⚠️ | Istán | 1 |
| Bois de Istán (40) ⚠️ | Istán | 1 |
| Bois de Málaga (137) ⚠️ | Málaga | 1 |
| Bois de Istán (45) ⚠️ | Istán | 1 |
| Bois de Istán (46) ⚠️ | Istán | 1 |
| Bois de Guaro (3) ⚠️ | Guaro | 1 |
| Bois de Monda (39) ⚠️ | Monda | 1 |
| Bois de Ronda (20) ⚠️ | Ronda | 1 |
| Bois de Guaro (5) ⚠️ | Guaro | 1 |
| Bois de Monda (55) ⚠️ | Monda | 1 |
| Bois de Monda (57) ⚠️ | Monda | 1 |
| Bois de Monda (58) ⚠️ | Monda | 1 |
| Bois de Ojén (5) ⚠️ | Ojén | 1 |
| Bois de Ojén (7) ⚠️ | Ojén | 1 |
| Bois de Monda (60) ⚠️ | Monda | 1 |
| Parque Olisol ⚠️ | Mijas | 1 |
| Bois de Málaga (141) ⚠️ | Málaga | 1 |
| Bois de Parauta (15) ⚠️ | Parauta | 1 |
| Bois de Ronda (24) ⚠️ | Ronda | 1 |
| Bois de El Burgo (22) ⚠️ | El Burgo | 1 |
| Bois de El Burgo (23) ⚠️ | El Burgo | 1 |
| Bois de Málaga (147) ⚠️ | Málaga | 1 |
| Bois de Yunquera (45) ⚠️ | Yunquera | 1 |
| Bois de Yunquera (47) ⚠️ | Yunquera | 1 |
| Bois de Málaga (157) ⚠️ | Málaga | 1 |
| Bois de Alfarnatejo ⚠️ | Alfarnatejo | 1 |
| Bois de Mijas (59) ⚠️ | Mijas | 1 |
| Forêt de Villanueva del Trabuco (24) ⚠️ | Villanueva del Trabuco | 1 |
| Forêt de Alfarnate (8) ⚠️ | Alfarnate | 1 |
| Forêt de Alcaucín (12) ⚠️ | Alcaucín | 1 |
| Parque Monsálvez ⚠️ | Málaga | 1 |
| Plaza Eduardo Flores Carrasco ⚠️ | Estepona | 1 |
| Forêt de Viñuela (62) ⚠️ | Viñuela | 1 |
| Bois de Málaga (166) ⚠️ | Málaga | 1 |
| Bois de Málaga (170) ⚠️ | Málaga | 1 |
| Bois de Málaga (172) ⚠️ | Málaga | 1 |
| Bois de Málaga (177) ⚠️ | Málaga | 1 |
| Bois de Tolox (98) ⚠️ | Tolox | 1 |
| Bois de Tolox (99) ⚠️ | Tolox | 1 |
| Parque Pintor Antonio Segovia ⚠️ | Mollina | 1 |
| Parc de Málaga (151) ⚠️ | Málaga | 1 |
| Forêt de Cómpeta (2) ⚠️ | Cómpeta | 1 |
| Bois de Canillas de Albaida (2) ⚠️ | Canillas de Albaida | 1 |
| Bois de Canillas de Albaida (4) ⚠️ | Canillas de Albaida | 1 |
| Bois de Málaga (179) ⚠️ | Málaga | 1 |
| Forêt de Periana (25) ⚠️ | Periana | 1 |
| Forêt de Periana (26) ⚠️ | Periana | 1 |
| Bois de Canillas de Aceituno ⚠️ | Canillas de Aceituno | 1 |
| Parc de Alhaurín el Grande (3) ⚠️ | Alhaurín el Grande | 1 |
| Forêt de Cútar (6) ⚠️ | Cútar | 1 |
| Parc de Málaga (159) ⚠️ | Málaga | 1 |
| Parc de Málaga (175) ⚠️ | Málaga | 1 |
| Bois de Málaga (197) ⚠️ | Málaga | 1 |
| Bois de Málaga (203) ⚠️ | Málaga | 1 |
| Bois de Málaga (209) ⚠️ | Málaga | 1 |
| Bois de Málaga (210) ⚠️ | Málaga | 1 |
| Arenal Park ⚠️ | Villanueva de Algaidas | 1 |
| Bois de Málaga (212) ⚠️ | Málaga | 1 |
| Bois de Málaga (215) ⚠️ | Málaga | 1 |
| Casa de Convivencias Los Jarales ⚠️ | Antequera | 1 |
| Bois de Málaga (218) ⚠️ | Málaga | 1 |
| Bois de Málaga (220) ⚠️ | Málaga | 1 |
| Bois de Málaga (221) ⚠️ | Málaga | 1 |
| Bois de Málaga (222) ⚠️ | Málaga | 1 |
| Forêt de Colmenar (3) ⚠️ | Colmenar | 1 |
| Forêt de Colmenar (4) ⚠️ | Colmenar | 1 |
| Parc de Málaga (198) ⚠️ | Málaga | 1 |
| Bois de Málaga (228) ⚠️ | Málaga | 1 |
| Bois de Málaga (231) ⚠️ | Málaga | 1 |
| Bois de Málaga (234) ⚠️ | Málaga | 1 |
| Bois de Málaga (236) ⚠️ | Málaga | 1 |
| Bois de Torremolinos (2) ⚠️ | Torremolinos | 1 |
| Bois de Málaga (245) ⚠️ | Málaga | 1 |
| Bois de Málaga (248) ⚠️ | Málaga | 1 |
| Bois de Málaga (249) ⚠️ | Málaga | 1 |
| Forêt de Vélez-Málaga (260) ⚠️ | Vélez-Málaga | 1 |
| Bois de Málaga (257) ⚠️ | Málaga | 1 |
| Bois de Málaga (259) ⚠️ | Málaga | 1 |
| Forêt de Antequera (18) ⚠️ | Antequera | 1 |
| Bois de Málaga (260) ⚠️ | Málaga | 1 |
| Forêt de Antequera (28) ⚠️ | Antequera | 1 |
| Forêt de Antequera (29) ⚠️ | Antequera | 1 |
| Forêt de Antequera (33) ⚠️ | Antequera | 1 |
| Forêt de Antequera (38) ⚠️ | Antequera | 1 |
| Forêt de Antequera (40) ⚠️ | Antequera | 1 |
| Parque de la urbanización Renfe ⚠️ | Antequera | 1 |
| Parque del recinto ferial ⚠️ | Antequera | 1 |
| Parc de Málaga (208) ⚠️ | Málaga | 1 |
| Parc de Málaga (209) ⚠️ | Málaga | 1 |
| Bois de Málaga (265) ⚠️ | Málaga | 1 |
| Bois de Málaga (285) ⚠️ | Málaga | 1 |
| Bois de Málaga (286) ⚠️ | Málaga | 1 |
| Bois de Málaga (288) ⚠️ | Málaga | 1 |
| Bois de Málaga (290) ⚠️ | Málaga | 1 |
| Parc de Málaga (210) ⚠️ | Málaga | 1 |
| Bois de Málaga (296) ⚠️ | Málaga | 1 |
| Bois de Málaga (304) ⚠️ | Málaga | 1 |
| Bois de Málaga (305) ⚠️ | Málaga | 1 |
| Forêt de Ojén (56) ⚠️ | Ojén | 1 |
| Forêt de Ojén (58) ⚠️ | Ojén | 1 |
| Forêt de Ojén (59) ⚠️ | Ojén | 1 |
| Forêt de Ojén (60) ⚠️ | Ojén | 1 |
| Forêt de Ojén (66) ⚠️ | Ojén | 1 |
| Forêt de Ojén (68) ⚠️ | Ojén | 1 |
| Forêt de Ojén (71) ⚠️ | Ojén | 1 |
| Forêt de Ojén (72) ⚠️ | Ojén | 1 |
| Forêt de Marbella (27) ⚠️ | Marbella | 1 |
| Parc de Cuevas de San Marcos (4) ⚠️ | Cuevas de San Marcos | 1 |
| Plaza Antoñita ⚠️ | Vélez-Málaga | 1 |
| Forêt de Marbella (28) ⚠️ | Marbella | 1 |
| Forêt de Coín (13) ⚠️ | Coín | 1 |
| Bois de Málaga (328) ⚠️ | Málaga | 1 |
| Bois de Málaga (331) ⚠️ | Málaga | 1 |
| Bois de Málaga (334) ⚠️ | Málaga | 1 |
| Bois de Málaga (336) ⚠️ | Málaga | 1 |
| Forêt de Coín (17) ⚠️ | Coín | 1 |
| Forêt de Monda (25) ⚠️ | Monda | 1 |
| Bois de Málaga (345) ⚠️ | Málaga | 1 |
| Bois de Málaga (349) ⚠️ | Málaga | 1 |
| Forêt de Coín (21) ⚠️ | Coín | 1 |
| Forêt de Ojén (84) ⚠️ | Ojén | 1 |
| Bois de Málaga (352) ⚠️ | Málaga | 1 |
| Bois de Málaga (366) ⚠️ | Málaga | 1 |
| Bois de Málaga (369) ⚠️ | Málaga | 1 |
| Bois de Málaga (372) ⚠️ | Málaga | 1 |
| Bois de Málaga (374) ⚠️ | Málaga | 1 |
| Bois de Málaga (375) ⚠️ | Málaga | 1 |
| Bois de Mijas (63) ⚠️ | Mijas | 1 |
| Forêt de Colmenar (7) ⚠️ | Colmenar | 1 |
| Bois de Málaga (388) ⚠️ | Málaga | 1 |
| Bois de Málaga (390) ⚠️ | Málaga | 1 |
| Forêt de Ojén (85) ⚠️ | Ojén | 1 |
| Parc de Cuevas del Becerro (2) ⚠️ | Cuevas del Becerro | 1 |
| Forêt de Ojén (91) ⚠️ | Ojén | 1 |
| Forêt de Ojén (93) ⚠️ | Ojén | 1 |
| Forêt de Marbella (31) ⚠️ | Marbella | 1 |
| Forêt de Marbella (34) ⚠️ | Marbella | 1 |
| Bois de Antequera (3) ⚠️ | Antequera | 1 |
| Bois de Antequera (5) ⚠️ | Antequera | 1 |
| Bois de Antequera (9) ⚠️ | Antequera | 1 |
| Bois de Antequera (14) ⚠️ | Antequera | 1 |
| Bois de Antequera (16) ⚠️ | Antequera | 1 |
| Bois de Antequera (18) ⚠️ | Antequera | 1 |
| Bois de Antequera (28) ⚠️ | Antequera | 1 |
| Bois de Antequera (32) ⚠️ | Antequera | 1 |
| Forêt de Alfarnatejo (4) ⚠️ | Alfarnatejo | 1 |
| Bois de Villanueva del Rosario (2) ⚠️ | Villanueva del Rosario | 1 |
| Bois de Villanueva del Rosario (3) ⚠️ | Villanueva del Rosario | 1 |
| Forêt de Alfarnatejo (5) ⚠️ | Alfarnatejo | 1 |
| Forêt de Marbella (35) ⚠️ | Marbella | 1 |
| Forêt de Marbella (36) ⚠️ | Marbella | 1 |
| Parque El Capricho ⚠️ | Marbella | 1 |
| Forêt de Marbella (39) ⚠️ | Marbella | 1 |
| Forêt de Marbella (42) ⚠️ | Marbella | 1 |
| Bois de Málaga (397) ⚠️ | Málaga | 1 |
| Forêt de Marbella (51) ⚠️ | Marbella | 1 |
| Bois de Málaga (407) ⚠️ | Málaga | 1 |
| Parc de Mijas (76) ⚠️ | Mijas | 1 |
| Forêt de Mijas (370) ⚠️ | Mijas | 1 |
| Forêt de Mijas (371) ⚠️ | Mijas | 1 |
| Parc de Mijas (80) ⚠️ | Mijas | 1 |
| Bois de Málaga (418) ⚠️ | Málaga | 1 |
| Parc de Málaga (222) ⚠️ | Málaga | 1 |
| Bois de Málaga (429) ⚠️ | Málaga | 1 |
| Bois de Málaga (430) ⚠️ | Málaga | 1 |
| Bois de Málaga (431) ⚠️ | Málaga | 1 |
| Bois de Málaga (432) ⚠️ | Málaga | 1 |
| Bois de Málaga (435) ⚠️ | Málaga | 1 |
| Bois de Málaga (443) ⚠️ | Málaga | 1 |
| Bois de Málaga (450) ⚠️ | Málaga | 1 |
| Bois de Ronda (26) ⚠️ | Ronda | 1 |
| Bois de Málaga (483) ⚠️ | Málaga | 1 |
| Bois de Málaga (500) ⚠️ | Málaga | 1 |
| Forêt de Mijas (375) ⚠️ | Mijas | 1 |
| Bois de Marbella (90) ⚠️ | Marbella | 1 |
| Bois de Málaga (514) ⚠️ | Málaga | 1 |
| Bois de Málaga (516) ⚠️ | Málaga | 1 |
| Bois de Málaga (517) ⚠️ | Málaga | 1 |
| Bois de Málaga (519) ⚠️ | Málaga | 1 |
| Bois de Málaga (523) ⚠️ | Málaga | 1 |
| Bois de Málaga (525) ⚠️ | Málaga | 1 |
| Bois de Málaga (527) ⚠️ | Málaga | 1 |
| Bois de Málaga (530) ⚠️ | Málaga | 1 |
| Bois de Málaga (533) ⚠️ | Málaga | 1 |
| Bois de Málaga (540) ⚠️ | Málaga | 1 |
| Bois de Málaga (543) ⚠️ | Málaga | 1 |
| Bois de Málaga (547) ⚠️ | Málaga | 1 |
| Parque de Pacolito ⚠️ | Fuengirola | 1 |
| Bois de Málaga (561) ⚠️ | Málaga | 1 |
| Forêt de Benamargosa (10) ⚠️ | Benamargosa | 1 |
| Plaza Sierra de Almijara ⚠️ | Estepona | 1 |
| Forêt de Mijas (377) ⚠️ | Mijas | 1 |
| Bois de Málaga (578) ⚠️ | Málaga | 1 |
| Bois de Málaga (580) ⚠️ | Málaga | 1 |
| Forêt de Marbella (52) ⚠️ | Marbella | 1 |
| Parque Cruz de San Jorge ⚠️ | Ronda | 1 |
| Bois de Mijas (64) ⚠️ | Mijas | 1 |
| Forêt de Mijas (392) ⚠️ | Mijas | 1 |
| Forêt de Mijas (418) ⚠️ | Mijas | 1 |
| Bois de Mijas (98) ⚠️ | Mijas | 1 |
| Bois de Mijas (99) ⚠️ | Mijas | 1 |
| Bois de Mijas (100) ⚠️ | Mijas | 1 |
| Bois de Málaga (628) ⚠️ | Málaga | 1 |
| Bois de Málaga (639) ⚠️ | Málaga | 1 |
| Bois de Málaga (641) ⚠️ | Málaga | 1 |
| Forêt de Canillas de Aceituno (7) ⚠️ | Canillas de Aceituno | 1 |
| Bois de Málaga (656) ⚠️ | Málaga | 1 |
| Bois de Málaga (660) ⚠️ | Málaga | 1 |
| Parque de Santillán ⚠️ | Mollina | 1 |
| Forêt de Mijas (422) ⚠️ | Mijas | 1 |
| Bois de Nerja (5) ⚠️ | Nerja | 1 |
| Forêt de Benalmádena ⚠️ | Benalmádena | 1 |
| Bois de Casares ⚠️ | Casares | 1 |
| Bois de Nerja (6) ⚠️ | Nerja | 1 |
| Bois de Frigiliana (7) ⚠️ | Frigiliana | 1 |
| Parc de Marbella (100) ⚠️ | Marbella | 1 |
| Bois de Málaga (668) ⚠️ | Málaga | 1 |
| Bois de Málaga (673) ⚠️ | Málaga | 1 |
| Bois de Málaga (674) ⚠️ | Málaga | 1 |
| Bois de Málaga (682) ⚠️ | Málaga | 1 |
| Bois de Málaga (685) ⚠️ | Málaga | 1 |
| Bois de Málaga (694) ⚠️ | Málaga | 1 |
| Bois de Valle de Abdalajís (6) ⚠️ | Valle de Abdalajís | 1 |
| Bois de Málaga (695) ⚠️ | Málaga | 1 |
| Bois de Málaga (704) ⚠️ | Málaga | 1 |
| Bois de Totalán (3) ⚠️ | Totalán | 1 |
| Bois de Ardales (5) ⚠️ | Ardales | 1 |
| Forêt de Álora (2) ⚠️ | Álora | 1 |
| Bois de Álora (35) ⚠️ | Álora | 1 |
| Bois de Álora (55) ⚠️ | Álora | 1 |
| Parc de Marbella (102) ⚠️ | Marbella | 1 |
| Parc de Estepona (25) ⚠️ | Estepona | 1 |
| Bois de Benahavís (7) ⚠️ | Benahavís | 1 |
| Bois de Benahavís (10) ⚠️ | Benahavís | 1 |
| Bois de Benahavís (16) ⚠️ | Benahavís | 1 |
| Bois de Benahavís (19) ⚠️ | Benahavís | 1 |
| Bois de Benahavís (20) ⚠️ | Benahavís | 1 |
| Bois de Málaga (712) ⚠️ | Málaga | 1 |
| Parc de Casabermeja (2) ⚠️ | Casabermeja | 1 |
| Forêt de Canillas de Albaida (23) ⚠️ | Canillas de Albaida | 1 |
| Bois de Frigiliana (12) ⚠️ | Frigiliana | 1 |
| Bois de Frigiliana (15) ⚠️ | Frigiliana | 1 |
| Bois de Frigiliana (16) ⚠️ | Frigiliana | 1 |
| Bois de Frigiliana (18) ⚠️ | Frigiliana | 1 |
| Parque Encinas ⚠️ | Fuengirola | 1 |
| Bois de Montejaque (3) ⚠️ | Montejaque | 1 |
| Bois de Montejaque (7) ⚠️ | Montejaque | 1 |
| Golden Beach ⚠️ | Marbella | 1 |
| Parc de Estepona (29) ⚠️ | Estepona | 1 |
| Parque de los Naranjos (2) ⚠️ | Cártama | 1 |
| Parc de Cártama (10) ⚠️ | Cártama | 1 |
| Bois de Estepona (15) ⚠️ | Estepona | 1 |
| Bois de Marbella (94) ⚠️ | Marbella | 1 |
| Bois de Marbella (95) ⚠️ | Marbella | 1 |
| Bois de Marbella (96) ⚠️ | Marbella | 1 |
| Bois de Ojén (11) ⚠️ | Ojén | 1 |
| Bois de Málaga (716) ⚠️ | Málaga | 1 |
| Jardines de Picasso ⚠️ | Málaga | 1 |
| Parque de la Constitución (2) ⚠️ | Marbella | 1 |
| Parque Santo Cristo ⚠️ | Cártama | 1 |
| Parc de Málaga (259) ⚠️ | Málaga | 1 |
| Parc de Málaga (260) ⚠️ | Málaga | 1 |
| Bois de Málaga (723) ⚠️ | Málaga | 1 |
| Bois de Málaga (724) ⚠️ | Málaga | 1 |
| Parc de Málaga (266) ⚠️ | Málaga | 1 |
| Parque del Castillo de Papabellotas ⚠️ | Antequera | 1 |
| Bois de Álora (109) ⚠️ | Álora | 1 |

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
