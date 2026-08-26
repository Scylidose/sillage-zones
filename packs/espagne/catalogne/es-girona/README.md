# Province de Gérone

Pack `es-girona` · version 1.0.0 · grille 200 m · Espagne › Catalogne

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 267 619 |
| dont restreintes (aéroport, militaire, prison) | 889 |
| dont sans chemin (aucune voie à moins de 60 m) | 14 833 |
| dont en forêt, sans chemin non plus | 34 460 |
| dont traversées par un cours d'eau, sans chemin non plus | 4 601 |
| Cellules retirées par le masque d'eau | 1 081 |
| Villes | 221 |
| Arrondissements et quartiers | 0 |
| Îles | 9 |
| Parcs | 6 799 |

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
| Alt Empordà | 61 735 | somme de 68 villes |
| Baix Empordà | 31 688 | somme de 36 villes |
| Cerdanya (Gérone) | 11 493 | somme de 11 villes |
| Garrotxa | 33 433 | somme de 21 villes |
| Gironès | 25 936 | somme de 27 villes |
| Osona (Gérone) | 4 639 | somme de 3 villes |
| Pla de l'Estany | 11 895 | somme de 11 villes |
| Ripollès | 43 658 | somme de 19 villes |
| la Selva (Gérone) | 43 146 | somme de 25 villes |

Une île *composite* n'a pas de cellules à elle : sa progression est la somme de ses villes, et ses cellules ne lui sont jamais rattachées directement — elles compteraient deux fois.

## Villes (221)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Sans chemin | Parcs |
|---|---:|---:|---:|---:|---:|---:|---:|
| les Llosses | 5 209 | 8 | 5 201 | 0 | **5 201** | 25 (0 %) | 126 |
| Camprodon | 4 720 | 7 | 4 713 | 0 | **4 713** | 99 (2 %) | 73 |
| Cruïlles, Monells i Sant Sadurní de l'Heura | 4 501 | 0 | 4 501 | 0 | **4 501** | 41 (1 %) | 37 |
| Albanyà | 4 323 | 0 | 4 323 | 0 | **4 323** | 4 (0 %) | 32 |
| la Vall de Bianya | 4 287 | 0 | 4 287 | 0 | **4 287** | 26 (1 %) | 39 |
| Montagut i Oix | 4 284 | 0 | 4 284 | 0 | **4 284** | 24 (1 %) | 87 |
| Queralbs | 4 286 | 5 | 4 281 | 0 | **4 281** | 1 151 (27 %) | 49 |
| la Vall d'en Bas | 4 121 | 4 | 4 117 | 0 | **4 117** | 86 (2 %) | 77 |
| Arbúcies | 3 891 | 0 | 3 891 | 0 | **3 891** | 22 (1 %) | 46 |
| Sant Hilari Sacalm | 3 757 | 70 | 3 687 | 0 | **3 687** | 6 (0 %) | 41 |
| Llagostera | 3 446 | 0 | 3 446 | 0 | **3 446** | 89 (3 %) | 80 |
| Ripoll | 3 342 | 11 | 3 331 | 0 | **3 331** | 23 (1 %) | 123 |
| Santa Coloma de Farners | 3 199 | 6 | 3 193 | 0 | **3 193** | 8 (0 %) | 74 |
| Maçanet de Cabrenys | 3 094 | 0 | 3 094 | 0 | **3 094** | 29 (1 %) | 33 |
| Santa Cristina d'Aro | 3 062 | 0 | 3 062 | 0 | **3 062** | 11 (0 %) | 57 |
| Torroella de Montgrí | 2 997 | 31 | 2 966 | 0 | **2 966** | 200 (7 %) | 120 |
| Vilallonga de Ter | 2 957 | 6 | 2 951 | 0 | **2 951** | 605 (21 %) | 47 |
| Vilademuls | 2 828 | 10 | 2 818 | 0 | **2 818** | 302 (11 %) | 60 |
| Sant Feliu de Buixalleu | 2 798 | 0 | 2 798 | 0 | **2 798** | 25 (1 %) | 40 |
| Toses | 2 641 | 0 | 2 641 | 0 | **2 641** | 391 (15 %) | 61 |
| la Jonquera | 2 632 | 0 | 2 632 | 0 | **2 632** | 18 (1 %) | 30 |
| Caldes de Malavella | 2 577 | 14 | 2 563 | 0 | **2 563** | 180 (7 %) | 40 |
| Cabanelles | 2 554 | 3 | 2 551 | 0 | **2 551** | 98 (4 %) | 16 |
| Sant Joan de les Abadesses | 2 427 | 12 | 2 415 | 0 | **2 415** | 36 (1 %) | 67 |
| Osor | 2 354 | 2 | 2 352 | 0 | **2 352** |  | 34 |
| Viladrau | 2 280 | 1 | 2 279 | 0 | **2 279** | 4 (0 %) | 63 |
| Forallac | 2 275 | 0 | 2 275 | 0 | **2 275** | 62 (3 %) | 52 |
| Setcases | 2 251 | 5 | 2 246 | 0 | **2 246** | 184 (8 %) | 109 |
| Santa Pau | 2 225 | 1 | 2 224 | 0 | **2 224** | 35 (2 %) | 27 |
| Sant Gregori | 2 211 | 5 | 2 206 | 0 | **2 206** | 61 (3 %) | 50 |
| Lloret de Mar | 2 185 | 0 | 2 185 | 0 | **2 185** | 14 (1 %) | 65 |
| Vidreres | 2 172 | 2 | 2 170 | 0 | **2 170** | 56 (3 %) | 48 |
| Sant Aniol de Finestres | 2 163 | 0 | 2 163 | 0 | **2 163** | 20 (1 %) | 5 |
| Susqueda | 2 275 | 148 | 2 127 | 0 | **2 127** | 11 (1 %) | 16 |
| Riudarenes | 2 120 | 0 | 2 120 | 0 | **2 120** | 91 (4 %) | 33 |
| Roses | 2 102 | 16 | 2 086 | 6 | **2 080** | 146 (7 %) | 170 |
| Ogassa | 2 078 | 0 | 2 078 | 0 | **2 078** | 168 (8 %) | 13 |
| Rabós | 2 063 | 0 | 2 063 | 0 | **2 063** | 666 (32 %) | 15 |
| Cassà de la Selva | 2 051 | 0 | 2 051 | 0 | **2 051** | 112 (5 %) | 48 |
| Maçanet de la Selva | 2 050 | 3 | 2 047 | 0 | **2 047** | 105 (5 %) | 33 |
| Canet d'Adri | 2 028 | 0 | 2 028 | 0 | **2 028** | 13 (1 %) | 23 |
| Alp | 2 027 | 4 | 2 023 | 0 | **2 023** | 91 (4 %) | 111 |
| Espolla | 2 009 | 1 | 2 008 | 156 | **1 852** | 320 (17 %) | 21 |
| Peralada | 2 006 | 8 | 1 998 | 0 | **1 998** | 333 (17 %) | 28 |
| Molló | 1 996 | 0 | 1 996 | 0 | **1 996** | 98 (5 %) | 91 |
| Gombrèn | 1 972 | 0 | 1 972 | 0 | **1 972** | 32 (2 %) | 79 |
| Sant Martí de Llémena | 1 945 | 0 | 1 945 | 0 | **1 945** | 5 (0 %) | 4 |
| Ribes de Freser | 1 924 | 5 | 1 919 | 0 | **1 919** | 43 (2 %) | 59 |
| Sant Ferriol | 1 931 | 14 | 1 917 | 0 | **1 917** | 21 (1 %) | 19 |
| el Port de la Selva | 1 903 | 1 | 1 902 | 0 | **1 902** | 310 (16 %) | 42 |
| Castelló d'Empúries | 1 933 | 92 | 1 841 | 8 | **1 833** | 316 (17 %) | 41 |
| Amer | 1 831 | 12 | 1 819 | 0 | **1 819** | 25 (1 %) | 13 |
| Vallfogona de Ripollès | 1 761 | 0 | 1 761 | 0 | **1 761** | 11 (1 %) | 22 |
| Quart | 1 741 | 0 | 1 741 | 0 | **1 741** |  | 22 |
| Girona | 1 751 | 26 | 1 725 | 0 | **1 725** | 9 (1 %) | 220 |
| Meranges | 1 731 | 8 | 1 723 | 0 | **1 723** | 385 (22 %) | 26 |
| Tossa de Mar | 1 710 | 0 | 1 710 | 0 | **1 710** | 3 (0 %) | 47 |
| les Planes d'Hostoles | 1 691 | 0 | 1 691 | 0 | **1 691** | 20 (1 %) | 16 |
| Brunyola i Sant Martí Sapresa | 1 667 | 5 | 1 662 | 0 | **1 662** | 60 (4 %) | 19 |
| Sales de Llierca | 1 656 | 0 | 1 656 | 0 | **1 656** | 15 (1 %) | 16 |
| Beuda | 1 625 | 0 | 1 625 | 0 | **1 625** | 29 (2 %) | 6 |
| Bescanó | 1 641 | 18 | 1 623 | 0 | **1 623** | 24 (1 %) | 46 |
| Sant Feliu de Pallerols | 1 591 | 0 | 1 591 | 0 | **1 591** | 4 (0 %) | 11 |
| Vidrà | 1 580 | 0 | 1 580 | 0 | **1 580** | 21 (1 %) | 9 |
| Porqueres | 1 537 | 1 | 1 536 | 0 | **1 536** | 6 (0 %) | 71 |
| Sant Miquel de Campmajor | 1 534 | 0 | 1 534 | 0 | **1 534** | 8 (1 %) | 8 |
| Calonge i Sant Antoni | 1 526 | 0 | 1 526 | 0 | **1 526** | 3 (0 %) | 72 |
| Darnius | 1 609 | 106 | 1 503 | 0 | **1 503** | 2 (0 %) | 11 |
| Campdevànol | 1 497 | 2 | 1 495 | 0 | **1 495** | 5 (0 %) | 98 |
| Ger | 1 497 | 3 | 1 494 | 0 | **1 494** | 203 (14 %) | 26 |
| Vilobí d'Onyar | 1 469 | 4 | 1 465 | 48 | **1 417** | 71 (5 %) | 59 |
| Sant Joan les Fonts | 1 456 | 5 | 1 451 | 0 | **1 451** | 13 (1 %) | 28 |
| Pardines | 1 425 | 0 | 1 425 | 0 | **1 425** | 195 (14 %) | 17 |
| Sant Llorenç de la Muga | 1 460 | 48 | 1 412 | 0 | **1 412** | 8 (1 %) | 25 |
| Sils | 1 359 | 4 | 1 355 | 0 | **1 355** | 79 (6 %) | 63 |
| Olot | 1 328 | 7 | 1 321 | 0 | **1 321** | 45 (3 %) | 69 |
| Fontanals de Cerdanya | 1 312 | 4 | 1 308 | 5 | **1 303** | 96 (7 %) | 72 |
| Llançà | 1 278 | 0 | 1 278 | 0 | **1 278** | 88 (7 %) | 54 |
| Agullana | 1 266 | 0 | 1 266 | 0 | **1 266** | 24 (2 %) | 5 |
| Cornellà del Terri | 1 262 | 0 | 1 262 | 0 | **1 262** | 57 (5 %) | 48 |
| Capmany | 1 215 | 1 | 1 214 | 0 | **1 214** | 178 (15 %) | 3 |
| Palafrugell | 1 212 | 0 | 1 212 | 0 | **1 212** | 25 (2 %) | 201 |
| Riells i Viabrea | 1 211 | 0 | 1 211 | 0 | **1 211** |  | 45 |
| Cadaqués | 1 201 | 0 | 1 201 | 0 | **1 201** | 155 (13 %) | 23 |
| Mieres | 1 196 | 0 | 1 196 | 0 | **1 196** | 11 (1 %) | 7 |
| Cistella | 1 172 | 0 | 1 172 | 0 | **1 172** | 121 (10 %) | 9 |
| Massanes | 1 170 | 0 | 1 170 | 0 | **1 170** | 17 (1 %) | 26 |
| Pals | 1 160 | 3 | 1 157 | 0 | **1 157** | 66 (6 %) | 91 |
| Ventalló | 1 160 | 12 | 1 148 | 0 | **1 148** | 107 (9 %) | 34 |
| Colera | 1 115 | 0 | 1 115 | 0 | **1 115** | 109 (10 %) | 17 |
| Sant Climent Sescebes | 1 117 | 3 | 1 114 | 624 | **490** | 67 (14 %) | 1 |
| Llanars | 1 113 | 1 | 1 112 | 0 | **1 112** | 53 (5 %) | 30 |
| Riudaura | 1 099 | 0 | 1 099 | 0 | **1 099** | 11 (1 %) | 6 |
| Guils de Cerdanya | 1 033 | 0 | 1 033 | 0 | **1 033** | 108 (10 %) | 47 |
| Castell d'Aro, Platja d'Aro i s'Agaró | 986 | 6 | 980 | 0 | **980** | 2 (0 %) | 102 |
| Llers | 976 | 1 | 975 | 0 | **975** | 83 (9 %) | 16 |
| Garriguella | 965 | 0 | 965 | 0 | **965** | 149 (15 %) | 4 |
| Terrades | 956 | 2 | 954 | 0 | **954** | 184 (19 %) | 4 |
| Begur | 952 | 0 | 952 | 0 | **952** | 8 (1 %) | 52 |
| la Bisbal d'Empordà | 934 | 0 | 934 | 0 | **934** | 19 (2 %) | 36 |
| Celrà | 905 | 8 | 897 | 0 | **897** | 20 (2 %) | 29 |
| Cantallops | 895 | 0 | 895 | 4 | **891** | 127 (14 %) | 9 |
| Garrigàs | 886 | 11 | 875 | 0 | **875** | 128 (15 %) | 22 |
| Figueres | 865 | 3 | 862 | 7 | **855** | 68 (8 %) | 34 |
| Planoles | 860 | 2 | 858 | 0 | **858** | 64 (7 %) | 18 |
| Campelles | 857 | 1 | 856 | 0 | **856** | 12 (1 %) | 14 |
| Puigcerdà | 856 | 7 | 849 | 0 | **849** | 77 (9 %) | 147 |
| Foixà | 856 | 12 | 844 | 0 | **844** | 116 (14 %) | 14 |
| Navata | 836 | 4 | 832 | 0 | **832** | 74 (9 %) | 20 |
| Sant Julià de Ramis | 842 | 10 | 832 | 0 | **832** | 30 (4 %) | 32 |
| Palol de Revardit | 819 | 0 | 819 | 0 | **819** | 4 (0 %) | 16 |
| Urús | 809 | 0 | 809 | 0 | **809** | 61 (8 %) | 16 |
| Blanes | 800 | 1 | 799 | 0 | **799** | 8 (1 %) | 47 |
| Sant Pere Pescador | 821 | 26 | 795 | 0 | **795** | 70 (9 %) | 22 |
| Serinyà | 783 | 2 | 781 | 0 | **781** | 19 (2 %) | 7 |
| Espinelves | 780 | 0 | 780 | 0 | **780** | 1 (0 %) | 11 |
| Fontcoberta | 779 | 1 | 778 | 0 | **778** | 53 (7 %) | 18 |
| Bàscara | 776 | 2 | 774 | 0 | **774** | 50 (6 %) | 19 |
| Vilanant | 772 | 0 | 772 | 0 | **772** | 96 (12 %) | 11 |
| Maià de Montcal | 770 | 3 | 767 | 0 | **767** | 64 (8 %) | 8 |
| Torroella de Fluvià | 766 | 7 | 759 | 0 | **759** | 105 (14 %) | 20 |
| Sant Martí Vell | 758 | 0 | 758 | 0 | **758** | 22 (3 %) | 2 |
| Vilopriu | 755 | 0 | 755 | 0 | **755** | 47 (6 %) | 10 |
| la Tallada d'Empordà | 760 | 5 | 755 | 0 | **755** | 68 (9 %) | 6 |
| Palau-saverdera | 748 | 1 | 747 | 0 | **747** | 63 (8 %) | 116 |
| Anglès | 740 | 1 | 739 | 0 | **739** | 5 (1 %) | 20 |
| l'Escala | 734 | 0 | 734 | 0 | **734** | 79 (11 %) | 51 |
| Corçà | 726 | 0 | 726 | 0 | **726** | 74 (10 %) | 18 |
| Sant Feliu de Guíxols | 718 | 0 | 718 | 0 | **718** | 3 (0 %) | 55 |
| Viladasens | 710 | 0 | 710 | 0 | **710** | 70 (10 %) | 17 |
| Camós | 705 | 1 | 704 | 0 | **704** | 4 (1 %) | 14 |
| Esponellà | 715 | 13 | 702 | 0 | **702** | 39 (6 %) | 9 |
| Cabanes | 686 | 3 | 683 | 0 | **683** | 73 (11 %) | 11 |
| Das | 678 | 1 | 677 | 14 | **663** | 81 (12 %) | 28 |
| Llambilles | 656 | 0 | 656 | 0 | **656** | 10 (2 %) | 10 |
| la Cellera de Ter | 659 | 7 | 652 | 0 | **652** |  | 65 |
| Aiguaviva | 633 | 0 | 633 | 13 | **620** | 41 (7 %) | 44 |
| Madremanya | 631 | 0 | 631 | 0 | **631** | 14 (2 %) | 4 |
| Palamós | 630 | 0 | 630 | 0 | **630** | 3 (0 %) | 57 |
| Pontós | 624 | 3 | 621 | 0 | **621** | 48 (8 %) | 16 |
| Lladó | 620 | 0 | 620 | 0 | **620** | 20 (3 %) | 19 |
| Vilajuïga | 604 | 0 | 604 | 0 | **604** | 58 (10 %) | 6 |
| Riudellots de la Selva | 602 | 0 | 602 | 0 | **602** | 37 (6 %) | 30 |
| Llívia | 599 | 0 | 599 | 0 | **599** | 79 (13 %) | 14 |
| Argelaguer | 581 | 7 | 574 | 0 | **574** | 18 (3 %) | 13 |
| Masarac i Vilarnadal | 572 | 0 | 572 | 0 | **572** | 93 (16 %) |  |
| Avinyonet de Puigventós | 568 | 0 | 568 | 0 | **568** | 77 (14 %) | 7 |
| Bellcaire d'Empordà | 565 | 0 | 565 | 0 | **565** | 140 (25 %) |  |
| Palau-sator | 563 | 0 | 563 | 0 | **563** | 64 (11 %) | 28 |
| Mont-ras | 557 | 1 | 556 | 0 | **556** | 12 (2 %) | 28 |
| la Pera | 540 | 0 | 540 | 0 | **540** | 66 (12 %) | 11 |
| Sant Jordi Desvalls | 537 | 2 | 535 | 0 | **535** | 62 (12 %) | 27 |
| Saus, Camallera i Llampaies | 529 | 0 | 529 | 0 | **529** | 25 (5 %) | 6 |
| Fornells de la Selva | 528 | 0 | 528 | 0 | **528** | 28 (5 %) | 27 |
| Albons | 523 | 0 | 523 | 0 | **523** | 84 (16 %) | 1 |
| Viladamat | 521 | 0 | 521 | 4 | **517** | 66 (13 %) | 7 |
| Crespià | 515 | 4 | 511 | 0 | **511** | 33 (6 %) | 7 |
| Boadella i les Escaules | 501 | 0 | 501 | 0 | **501** | 18 (4 %) | 2 |
| Tortellà | 498 | 0 | 498 | 0 | **498** | 18 (4 %) | 21 |
| Fortià | 496 | 0 | 496 | 0 | **496** | 118 (24 %) |  |
| Isòvol | 499 | 4 | 495 | 0 | **495** | 62 (13 %) | 16 |
| Ullastret | 495 | 0 | 495 | 0 | **495** | 69 (14 %) | 13 |
| Bolvir | 483 | 0 | 483 | 0 | **483** | 52 (11 %) | 23 |
| Siurana | 481 | 2 | 479 | 0 | **479** | 73 (15 %) | 11 |
| Pau | 478 | 4 | 474 | 0 | **474** | 72 (15 %) | 23 |
| Biure | 456 | 0 | 456 | 0 | **456** | 17 (4 %) | 3 |
| Cervià de Ter | 461 | 7 | 454 | 0 | **454** | 25 (6 %) | 53 |
| Banyoles | 503 | 53 | 450 | 0 | **450** | 12 (3 %) | 98 |
| Sant Julià del Llor i Bonmatí | 455 | 6 | 449 | 0 | **449** | 4 (1 %) | 12 |
| Borrassà | 429 | 0 | 429 | 0 | **429** | 15 (3 %) | 7 |
| Verges | 429 | 3 | 426 | 0 | **426** | 52 (12 %) | 1 |
| Portbou | 426 | 1 | 425 | 0 | **425** | 19 (4 %) | 2 |
| Fontanilles | 427 | 3 | 424 | 0 | **424** | 46 (11 %) | 8 |
| el Far d'Empordà | 424 | 2 | 422 | 0 | **422** | 69 (16 %) | 2 |
| les Preses | 421 | 0 | 421 | 0 | **421** |  | 8 |
| Sant Pau de Segúries | 408 | 1 | 407 | 0 | **407** | 9 (2 %) | 7 |
| Gualta | 415 | 10 | 405 | 0 | **405** | 60 (15 %) | 6 |
| Garrigoles | 404 | 0 | 404 | 0 | **404** | 33 (8 %) | 13 |
| Vilamalla | 398 | 0 | 398 | 0 | **398** | 55 (14 %) | 4 |
| Palau de Santa Eulàlia | 397 | 3 | 394 | 0 | **394** | 43 (11 %) | 3 |
| Pedret i Marzà | 396 | 2 | 394 | 0 | **394** | 55 (14 %) |  |
| Ordis | 389 | 0 | 389 | 0 | **389** | 57 (15 %) | 4 |
| Pont de Molins | 391 | 3 | 388 | 0 | **388** | 21 (5 %) | 10 |
| Vilafant | 381 | 0 | 381 | 0 | **381** | 25 (7 %) | 9 |
| Campllong | 380 | 0 | 380 | 0 | **380** | 25 (7 %) | 23 |
| Juià | 374 | 0 | 374 | 0 | **374** | 9 (2 %) | 4 |
| Serra de Daró | 371 | 4 | 367 | 0 | **367** | 71 (19 %) |  |
| Torrent | 355 | 0 | 355 | 0 | **355** | 28 (8 %) | 18 |
| Ullà | 330 | 2 | 328 | 0 | **328** | 61 (19 %) | 3 |
| la Selva de Mar | 328 | 0 | 328 | 0 | **328** | 49 (15 %) | 11 |
| Sant Mori | 332 | 5 | 327 | 0 | **327** | 5 (2 %) | 10 |
| Bordils | 318 | 3 | 315 | 0 | **315** | 47 (15 %) |  |
| Sant Jaume de Llierca | 321 | 9 | 312 | 0 | **312** | 6 (2 %) | 7 |
| Flaçà | 304 | 2 | 302 | 0 | **302** | 11 (4 %) | 7 |
| Jafre | 302 | 2 | 300 | 0 | **300** | 33 (11 %) | 6 |
| Salt | 299 | 6 | 293 | 0 | **293** | 6 (2 %) | 39 |
| Riumors | 291 | 0 | 291 | 0 | **291** | 108 (37 %) | 2 |
| Regencós | 287 | 0 | 287 | 0 | **287** | 31 (11 %) | 3 |
| Mollet de Peralada | 282 | 0 | 282 | 0 | **282** | 52 (18 %) | 3 |
| Parlavà | 278 | 0 | 278 | 0 | **278** | 43 (15 %) |  |
| l'Armentera | 278 | 0 | 278 | 0 | **278** | 36 (13 %) | 6 |
| Vila-sacra | 276 | 1 | 275 | 0 | **275** | 61 (22 %) | 4 |
| Vilablareix | 274 | 0 | 274 | 0 | **274** | 11 (4 %) | 12 |
| Vilamacolum | 266 | 0 | 266 | 0 | **266** | 55 (21 %) | 3 |
| Vilaür | 266 | 0 | 266 | 0 | **266** | 7 (3 %) | 6 |
| Sant Andreu Salou | 260 | 0 | 260 | 0 | **260** | 25 (10 %) | 11 |
| Vall-llobrega | 249 | 0 | 249 | 0 | **249** |  | 5 |
| Rupià | 247 | 1 | 246 | 0 | **246** | 43 (17 %) | 2 |
| Vilamaniscle | 246 | 0 | 246 | 0 | **246** | 33 (13 %) | 4 |
| Breda | 227 | 0 | 227 | 0 | **227** | 8 (4 %) | 11 |
| la Vajol | 215 | 0 | 215 | 0 | **215** | 11 (5 %) | 56 |
| Besalú | 212 | 5 | 207 | 0 | **207** | 2 (1 %) | 19 |
| Sarrià de Ter | 194 | 0 | 194 | 0 | **194** |  | 32 |
| Ultramort | 195 | 1 | 194 | 0 | **194** | 34 (18 %) | 1 |
| Colomers | 195 | 5 | 190 | 0 | **190** | 18 (9 %) | 6 |
| Sant Miquel de Fluvià | 164 | 1 | 163 | 0 | **163** | 24 (15 %) | 8 |
| Hostalric | 153 | 0 | 153 | 0 | **153** |  | 24 |
| Sant Joan de Mollet | 148 | 3 | 145 | 0 | **145** | 24 (17 %) | 3 |
| Vilabertran | 103 | 0 | 103 | 0 | **103** | 1 (1 %) | 6 |
| Santa Llogaia d'Àlguema | 91 | 0 | 91 | 0 | **91** | 3 (3 %) | 2 |
| Castellfollit de la Roca | 33 | 1 | 32 | 0 | **32** | 2 (6 %) | 8 |

## Parcs (6799)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| les Gavarres ⚠️ | Cruïlles, Monells i Sant Sadurní de l'Heura › Baix Empordà | 14 794 |
| Forêt de la Vall d'en Bas (13) ⚠️ | la Vall d'en Bas › Garrotxa | 6 526 |
| Forêt de Sant Gregori (25) ⚠️ | Sant Gregori › Gironès | 4 458 |
| Forêt de Cabanelles (4) ⚠️ | Cabanelles › Alt Empordà | 3 226 |
| Forêt de Sant Aniol de Finestres (5) ⚠️ | Sant Aniol de Finestres › Garrotxa | 2 990 |
| Forêt de Sant Ferriol (5) ⚠️ | Sant Ferriol › Garrotxa | 2 622 |
| Forêt de Susqueda (2) ⚠️ | Susqueda › la Selva (Gérone) | 2 422 |
| Forêt de la Vall de Bianya (6) ⚠️ | la Vall de Bianya › Garrotxa | 2 087 |
| Forêt de Sant Martí de Llémena (4) ⚠️ | Sant Martí de Llémena › Gironès | 1 764 |
| Forêt de Sant Hilari Sacalm (26) ⚠️ | Sant Hilari Sacalm › la Selva (Gérone) | 1 741 |
| Forêt de Ogassa (9) ⚠️ | Ogassa › Ripollès | 1 467 |
| Forêt de Sales de Llierca (15) ⚠️ | Sales de Llierca › Garrotxa | 1 408 |
| Forêt de les Llosses (39) ⚠️ | les Llosses › Ripollès | 1 349 |
| Forêt de Camprodon (5) ⚠️ | Camprodon › Ripollès | 1 329 |
| Forêt de Riudarenes (22) ⚠️ | Riudarenes › la Selva (Gérone) | 1 312 |
| Forêt de Osor (17) ⚠️ | Osor › la Selva (Gérone) | 1 298 |
| Forêt de Arbúcies (8) ⚠️ | Arbúcies › la Selva (Gérone) | 1 298 |
| Forêt de Arbúcies (10) ⚠️ | Arbúcies › la Selva (Gérone) | 1 231 |
| Forêt de Sant Llorenç de la Muga (23) ⚠️ | Sant Llorenç de la Muga › Alt Empordà | 1 229 |
| Forêt de Sant Feliu de Buixalleu (19) ⚠️ | Sant Feliu de Buixalleu › la Selva (Gérone) | 1 118 |
| Forêt de Ripoll (10) ⚠️ | Ripoll › Ripollès | 1 100 |
| Forêt de Urús ⚠️ | Urús › Cerdanya (Gérone) | 1 095 |
| Forêt de les Llosses (41) ⚠️ | les Llosses › Ripollès | 1 056 |
| Forêt de Sant Feliu de Pallerols ⚠️ | Sant Feliu de Pallerols › Garrotxa | 1 028 |
| Forêt de Beuda (2) ⚠️ | Beuda › Garrotxa | 1 016 |
| Forêt de Porqueres ⚠️ | Porqueres › Pla de l'Estany | 993 |
| Forêt de Cabanelles (5) ⚠️ | Cabanelles › Alt Empordà | 975 |
| Forêt de Fontanals de Cerdanya (57) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 973 |
| Forêt de Agullana ⚠️ | Agullana › Alt Empordà | 895 |
| Forêt de Santa Coloma de Farners (29) ⚠️ | Santa Coloma de Farners › la Selva (Gérone) | 894 |
| Forêt de Porqueres (19) ⚠️ | Porqueres › Pla de l'Estany | 881 |
| Forêt de Santa Cristina d'Aro (21) ⚠️ | Santa Cristina d'Aro › Baix Empordà | 877 |
| Forêt de Sant Feliu de Pallerols (2) ⚠️ | Sant Feliu de Pallerols › Garrotxa | 869 |
| Forêt de Ogassa (8) ⚠️ | Ogassa › Ripollès | 861 |
| Forêt de Camprodon (3) ⚠️ | Camprodon › Ripollès | 849 |
| Forêt de Albanyà (18) ⚠️ | Albanyà › Alt Empordà | 845 |
| Forêt de Beuda (3) ⚠️ | Beuda › Alt Empordà | 804 |
| Forêt de Sant Hilari Sacalm (28) ⚠️ | Sant Hilari Sacalm › la Selva (Gérone) | 773 |
| Forêt de Lloret de Mar (19) ⚠️ | Lloret de Mar › la Selva (Gérone) | 768 |
| Forêt de Espinelves (8) ⚠️ | Espinelves › Osona (Gérone) | 752 |
| Forêt de Bescanó (12) ⚠️ | Bescanó › Gironès | 738 |
| Forêt de Albanyà (25) ⚠️ | Albanyà › Alt Empordà | 709 |
| Forêt de Maçanet de Cabrenys (7) ⚠️ | Maçanet de Cabrenys › Alt Empordà | 687 |
| Forêt de Setcases (37) ⚠️ | Setcases › Ripollès | 654 |
| Forêt de Albanyà (19) ⚠️ | Albanyà › Alt Empordà | 651 |
| Forêt de Arbúcies (35) ⚠️ | Arbúcies › la Selva (Gérone) | 646 |
| Forêt de Vilanant (5) ⚠️ | Vilanant › Alt Empordà | 645 |
| Forêt de Queralbs (20) ⚠️ | Queralbs › Ripollès | 623 |
| Forêt de Pals (8) ⚠️ | Pals › Baix Empordà | 617 |
| Forêt de Maçanet de Cabrenys (24) ⚠️ | Maçanet de Cabrenys › Alt Empordà | 617 |
| Forêt de Anglès (5) ⚠️ | Anglès › la Selva (Gérone) | 610 |
| Forêt de Viladrau (24) ⚠️ | Viladrau › Osona (Gérone) | 603 |
| Forêt de Caldes de Malavella (31) ⚠️ | Caldes de Malavella › la Selva (Gérone) | 541 |
| Forêt de Vidreres (19) ⚠️ | Vidreres › la Selva (Gérone) | 541 |
| Forêt de Queralbs (21) ⚠️ | Queralbs › Ripollès | 536 |
| Forêt de Riells i Viabrea (19) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 534 |
| Forêt de Camprodon (38) ⚠️ | Camprodon › Ripollès | 503 |
| Forêt de Ripoll (9) ⚠️ | Ripoll › Ripollès | 498 |
| Forêt de Ribes de Freser (10) ⚠️ | Ribes de Freser › Ripollès | 459 |
| Forêt de Toses (33) ⚠️ | Toses › Ripollès | 448 |
| Forêt de la Jonquera (29) ⚠️ | la Jonquera › Alt Empordà | 444 |
| Forêt de Sant Llorenç de la Muga (2) ⚠️ | Sant Llorenç de la Muga › Alt Empordà | 425 |
| Forêt de Capmany ⚠️ | Capmany › Alt Empordà | 418 |
| Forêt de Massanes (19) ⚠️ | Massanes › la Selva (Gérone) | 413 |
| Forêt de Torroella de Montgrí (96) ⚠️ | Torroella de Montgrí › Baix Empordà | 413 |
| Forêt de Albanyà (10) ⚠️ | Albanyà › Alt Empordà | 405 |
| Forêt de Tossa de Mar (38) ⚠️ | Tossa de Mar › la Selva (Gérone) | 396 |
| Forêt de Susqueda ⚠️ | Susqueda › la Selva (Gérone) | 377 |
| Forêt de Montagut i Oix (16) ⚠️ | Montagut i Oix › Garrotxa | 373 |
| Forêt de la Jonquera (23) ⚠️ | la Jonquera › Alt Empordà | 365 |
| Forêt de Maçanet de Cabrenys (8) ⚠️ | Maçanet de Cabrenys › Alt Empordà | 355 |
| Forêt de Llagostera (42) ⚠️ | Llagostera › Gironès | 350 |
| Forêt de Camprodon (39) ⚠️ | Camprodon › Ripollès | 350 |
| Forêt de Tossa de Mar (9) ⚠️ | Tossa de Mar › la Selva (Gérone) | 349 |
| Forêt de Osor (18) ⚠️ | Osor › la Selva (Gérone) | 347 |
| Forêt de Santa Coloma de Farners (27) ⚠️ | Santa Coloma de Farners › la Selva (Gérone) | 342 |
| Forêt de Sant Hilari Sacalm (27) ⚠️ | Sant Hilari Sacalm › la Selva (Gérone) | 339 |
| Forêt de Montagut i Oix (4) ⚠️ | Montagut i Oix › Garrotxa | 338 |
| Forêt de Montagut i Oix (2) ⚠️ | Montagut i Oix › Garrotxa | 328 |
| Forêt de Brunyola i Sant Martí Sapresa (6) ⚠️ | Brunyola i Sant Martí Sapresa › la Selva (Gérone) | 325 |
| Forêt de Vidreres (18) ⚠️ | Vidreres › la Selva (Gérone) | 323 |
| Forêt de Guils de Cerdanya (45) ⚠️ | Guils de Cerdanya › Cerdanya (Gérone) | 320 |
| Forêt de Sils (31) ⚠️ | Sils › la Selva (Gérone) | 316 |
| Forêt de Palol de Revardit (4) ⚠️ | Palol de Revardit › Pla de l'Estany | 314 |
| Forêt de Vilademuls (14) ⚠️ | Vilademuls › Pla de l'Estany | 313 |
| Forêt de Pardines (11) ⚠️ | Pardines › Ripollès | 311 |
| Forêt de Darnius (8) ⚠️ | Darnius › Alt Empordà | 308 |
| Forêt de Viladamat (5) ⚠️ | Viladamat › Baix Empordà | 307 |
| Forêt de la Vall d'en Bas (72) ⚠️ | la Vall d'en Bas › Garrotxa | 305 |
| Forêt de Caldes de Malavella (30) ⚠️ | Caldes de Malavella › la Selva (Gérone) | 302 |
| Forêt de Santa Pau (14) ⚠️ | Santa Pau › Garrotxa | 301 |
| Forêt de Osor (22) ⚠️ | Osor › la Selva (Gérone) | 292 |
| Forêt de Vilallonga de Ter (7) ⚠️ | Vilallonga de Ter › Ripollès | 288 |
| Forêt de Riudarenes (13) ⚠️ | Riudarenes › la Selva (Gérone) | 287 |
| Forêt de Espolla (2) ⚠️ | Espolla › Alt Empordà | 283 |
| Forêt de Terrades (3) ⚠️ | Terrades › Alt Empordà | 279 |
| Forêt de Biure ⚠️ | Biure › Alt Empordà | 277 |
| Forêt de Viladasens (6) ⚠️ | Viladasens › Gironès | 272 |
| Forêt de Arbúcies (16) ⚠️ | Arbúcies › la Selva (Gérone) | 272 |
| Forêt de Sant Feliu de Pallerols (3) ⚠️ | Sant Feliu de Pallerols › Garrotxa | 271 |
| Forêt de Montagut i Oix (5) ⚠️ | Montagut i Oix › Garrotxa | 270 |
| Forêt de Vidreres (15) ⚠️ | Vidreres › la Selva (Gérone) | 267 |
| Forêt de Massanes (18) ⚠️ | Massanes › la Selva (Gérone) | 266 |
| Forêt de la Jonquera (15) ⚠️ | la Jonquera › Alt Empordà | 265 |
| Forêt de Mieres ⚠️ | Mieres › Garrotxa | 263 |
| Forêt de Camós (3) ⚠️ | Camós › Pla de l'Estany | 262 |
| Forêt de Cantallops (7) ⚠️ | Cantallops › Alt Empordà | 260 |
| Forêt de Sant Hilari Sacalm (33) ⚠️ | Sant Hilari Sacalm › la Selva (Gérone) | 260 |
| Forêt de Santa Cristina d'Aro (27) ⚠️ | Santa Cristina d'Aro › Baix Empordà | 259 |
| Forêt de Arbúcies (17) ⚠️ | Arbúcies › la Selva (Gérone) | 255 |
| Forêt de Biure (2) ⚠️ | Biure › Alt Empordà | 250 |
| Forêt de Bescanó (13) ⚠️ | Bescanó › Gironès | 248 |
| Forêt de Sant Feliu de Guíxols (31) ⚠️ | Sant Feliu de Guíxols › Baix Empordà | 244 |
| Forêt de la Jonquera (25) ⚠️ | la Jonquera › Alt Empordà | 244 |
| Forêt de les Llosses (110) ⚠️ | les Llosses › Ripollès | 243 |
| Forêt de Llagostera (49) ⚠️ | Llagostera › Gironès | 240 |
| Forêt de Lloret de Mar (20) ⚠️ | Lloret de Mar › la Selva (Gérone) | 237 |
| Forêt de Camprodon (4) ⚠️ | Camprodon › Ripollès | 237 |
| Forêt de la Jonquera (30) ⚠️ | la Jonquera › Alt Empordà | 237 |
| Forêt de Lloret de Mar (47) ⚠️ | Lloret de Mar › la Selva (Gérone) | 234 |
| Forêt de les Planes d'Hostoles (3) ⚠️ | les Planes d'Hostoles › Garrotxa | 234 |
| Forêt de Maçanet de la Selva (15) ⚠️ | Maçanet de la Selva › la Selva (Gérone) | 231 |
| Forêt de Montagut i Oix (57) ⚠️ | Montagut i Oix › Garrotxa | 231 |
| Forêt de Santa Coloma de Farners (32) ⚠️ | Santa Coloma de Farners › la Selva (Gérone) | 231 |
| Forêt de Anglès (6) ⚠️ | Anglès › la Selva (Gérone) | 229 |
| Forêt de la Jonquera (22) ⚠️ | la Jonquera › Alt Empordà | 226 |
| Forêt de la Jonquera (18) ⚠️ | la Jonquera › Alt Empordà | 224 |
| Forêt de Montagut i Oix (76) ⚠️ | Montagut i Oix › Garrotxa | 224 |
| Forêt de Meranges (3) ⚠️ | Meranges › Cerdanya (Gérone) | 223 |
| Forêt de Sant Feliu de Buixalleu (3) ⚠️ | Sant Feliu de Buixalleu › la Selva (Gérone) | 214 |
| Forêt de Palafrugell (118) ⚠️ | Palafrugell › Baix Empordà | 213 |
| Forêt de Lloret de Mar (21) ⚠️ | Lloret de Mar › la Selva (Gérone) | 212 |
| Forêt de Cervià de Ter (35) ⚠️ | Cervià de Ter › Gironès | 208 |
| Forêt de Camprodon (25) ⚠️ | Camprodon › Ripollès | 206 |
| Forêt de Toses (32) ⚠️ | Toses › Ripollès | 201 |
| Forêt de Ripoll (26) ⚠️ | Ripoll › Ripollès | 200 |
| Forêt de Llanars (6) ⚠️ | Llanars › Ripollès | 199 |
| Forêt de Albanyà (21) ⚠️ | Albanyà › Alt Empordà | 196 |
| Forêt de Sant Joan les Fonts (13) ⚠️ | Sant Joan les Fonts › Garrotxa | 192 |
| Forêt de Beuda (4) ⚠️ | Beuda › Garrotxa | 190 |
| Forêt de Gombrèn (6) ⚠️ | Gombrèn › Ripollès | 189 |
| Forêt de Sant Ferriol (14) ⚠️ | Sant Ferriol › Garrotxa | 189 |
| Forêt de Campdevànol (40) ⚠️ | Campdevànol › Ripollès | 187 |
| Forêt de Espolla (3) ⚠️ | Espolla › Alt Empordà | 186 |
| Forêt de Ger (20) ⚠️ | Ger › Cerdanya (Gérone) | 182 |
| Forêt de Santa Coloma de Farners (17) ⚠️ | Santa Coloma de Farners › la Selva (Gérone) | 179 |
| Forêt de les Llosses (40) ⚠️ | les Llosses › Ripollès | 178 |
| Forêt de Vilademuls (21) ⚠️ | Vilademuls › Pla de l'Estany | 178 |
| Forêt de Llagostera (6) ⚠️ | Llagostera › Gironès | 175 |
| Forêt de Ripoll (77) ⚠️ | Ripoll › Ripollès | 175 |
| Forêt de Riells i Viabrea (29) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 175 |
| Forêt de Sant Joan les Fonts (3) ⚠️ | Sant Joan les Fonts › Garrotxa | 174 |
| Forêt de Sant Hilari Sacalm (23) ⚠️ | Sant Hilari Sacalm › la Selva (Gérone) | 172 |
| Forêt de Ripoll (90) ⚠️ | Ripoll › Ripollès | 172 |
| Forêt de Darnius (3) ⚠️ | Darnius › Alt Empordà | 170 |
| Forêt de Cistella (8) ⚠️ | Cistella › Alt Empordà | 169 |
| Forêt de Toses (31) ⚠️ | Toses › Ripollès | 167 |
| Forêt de Montagut i Oix ⚠️ | Montagut i Oix › Garrotxa | 166 |
| Forêt de Sant Feliu de Buixalleu (20) ⚠️ | Sant Feliu de Buixalleu › la Selva (Gérone) | 166 |
| Forêt de Foixà (12) ⚠️ | Foixà › Baix Empordà | 164 |
| Forêt de Sant Ferriol (9) ⚠️ | Sant Ferriol › Garrotxa | 163 |
| Forêt de la Jonquera (28) ⚠️ | la Jonquera › Alt Empordà | 162 |
| Forêt de la Vall de Bianya (10) ⚠️ | la Vall de Bianya › Garrotxa | 161 |
| Forêt de la Vall de Bianya (2) ⚠️ | la Vall de Bianya › Garrotxa | 157 |
| Forêt de Sant Martí de Llémena (2) ⚠️ | Sant Martí de Llémena › Gironès | 157 |
| Forêt de Vallfogona de Ripollès (3) ⚠️ | Vallfogona de Ripollès › Ripollès | 156 |
| Forêt de Ripoll (78) ⚠️ | Ripoll › Ripollès | 156 |
| Forêt de Riells i Viabrea (15) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 153 |
| Forêt de Camprodon (35) ⚠️ | Camprodon › Ripollès | 153 |
| Forêt de Canet d'Adri (15) ⚠️ | Canet d'Adri › Gironès | 152 |
| Forêt de Sant Joan de les Abadesses (9) ⚠️ | Sant Joan de les Abadesses › Ripollès | 149 |
| Forêt de Campelles (2) ⚠️ | Campelles › Ripollès | 149 |
| Forêt de Mont-ras (11) ⚠️ | Mont-ras › Baix Empordà | 148 |
| Forêt de Arbúcies (34) ⚠️ | Arbúcies › la Selva (Gérone) | 148 |
| Forêt de Caldes de Malavella (2) ⚠️ | Caldes de Malavella › la Selva (Gérone) | 147 |
| Forêt de Sant Miquel de Campmajor (3) ⚠️ | Sant Miquel de Campmajor › Pla de l'Estany | 147 |
| Forêt de les Llosses (36) ⚠️ | les Llosses › Ripollès | 144 |
| Forêt de Llagostera (47) ⚠️ | Llagostera › Gironès | 144 |
| Forêt de Santa Coloma de Farners (23) ⚠️ | Santa Coloma de Farners › la Selva (Gérone) | 143 |
| Forêt de Sant Ferriol (10) ⚠️ | Sant Ferriol › Garrotxa | 142 |
| Forêt de Camprodon (23) ⚠️ | Camprodon › Ripollès | 137 |
| Forêt de Vilobí d'Onyar (43) ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 135 |
| Forêt de Olot (13) ⚠️ | Olot › Garrotxa | 135 |
| Forêt de Meranges (6) ⚠️ | Meranges › Cerdanya (Gérone) | 135 |
| Forêt de Sant Miquel de Campmajor (2) ⚠️ | Sant Miquel de Campmajor › Pla de l'Estany | 134 |
| Forêt de Queralbs (22) ⚠️ | Queralbs › Ripollès | 134 |
| Forêt de Campelles ⚠️ | Campelles › Ripollès | 133 |
| Forêt de les Llosses (38) ⚠️ | les Llosses › Ripollès | 133 |
| Forêt de Setcases (64) ⚠️ | Setcases › Ripollès | 131 |
| Forêt de Darnius (6) ⚠️ | Darnius › Alt Empordà | 130 |
| Forêt de Tossa de Mar (35) ⚠️ | Tossa de Mar › la Selva (Gérone) | 128 |
| Forêt de Osor (20) ⚠️ | Osor › la Selva (Gérone) | 128 |
| Forêt de Sant Miquel de Campmajor (5) ⚠️ | Sant Miquel de Campmajor › Pla de l'Estany | 128 |
| Forêt de Sant Feliu de Buixalleu (15) ⚠️ | Sant Feliu de Buixalleu › la Selva (Gérone) | 127 |
| Forêt de Darnius (7) ⚠️ | Darnius › Alt Empordà | 127 |
| Forêt de Toses (6) ⚠️ | Toses › Ripollès | 126 |
| Forêt de la Vall de Bianya (34) ⚠️ | la Vall de Bianya › Garrotxa | 126 |
| Forêt de Llagostera (48) | Llagostera › Gironès | 124 |
| Forêt de Llanars (11) | Llanars › Ripollès | 124 |
| Forêt de Cabanelles (2) | Cabanelles › Alt Empordà | 121 |
| Forêt de Tossa de Mar (33) | Tossa de Mar › la Selva (Gérone) | 121 |
| Forêt de Riudarenes (21) | Riudarenes › la Selva (Gérone) | 120 |
| Forêt de Bàscara (2) | Bàscara › Alt Empordà | 118 |
| Forêt de Lladó (14) | Lladó › Alt Empordà | 118 |
| Forêt de Viladrau (33) | Viladrau › Osona (Gérone) | 118 |
| Forêt de Sales de Llierca (9) | Sales de Llierca › Garrotxa | 118 |
| Forêt de Viladrau (52) | Viladrau › Osona (Gérone) | 118 |
| Forêt de Torroella de Montgrí (61) | Torroella de Montgrí › Baix Empordà | 117 |
| Forêt de Darnius (4) | Darnius › Alt Empordà | 117 |
| Forêt de les Llosses (35) | les Llosses › Ripollès | 116 |
| Forêt de les Llosses (58) | les Llosses › Ripollès | 116 |
| Forêt de Sant Feliu de Buixalleu (7) | Sant Feliu de Buixalleu › la Selva (Gérone) | 113 |
| Forêt de Planoles (3) | Planoles › Ripollès | 113 |
| Forêt de Albanyà (24) | Albanyà › Alt Empordà | 113 |
| Forêt de Massanes | Massanes › la Selva (Gérone) | 112 |
| Forêt de Maçanet de Cabrenys (23) | Maçanet de Cabrenys › Alt Empordà | 112 |
| Forêt de Santa Pau (17) | Santa Pau › Garrotxa | 112 |
| Forêt de Santa Coloma de Farners (30) | Santa Coloma de Farners › la Selva (Gérone) | 112 |
| Forêt de Llagostera (7) | Llagostera › Gironès | 111 |
| Forêt de Albanyà | Albanyà › Alt Empordà | 110 |
| Forêt de Camprodon (33) | Camprodon › Ripollès | 110 |
| Forêt de Setcases (100) | Setcases › Ripollès | 110 |
| Forêt de Vilopriu (3) | Vilopriu › Baix Empordà | 109 |
| Forêt de Beuda (5) | Beuda › Garrotxa | 109 |
| Forêt de Espinelves (11) | Espinelves › Osona (Gérone) | 109 |
| Forêt de Torroella de Montgrí (72) | Torroella de Montgrí › Baix Empordà | 108 |
| Forêt de Espolla (7) | Espolla › Alt Empordà | 108 |
| Forêt de Planoles (17) | Planoles › Ripollès | 107 |
| Forêt de Planoles | Planoles › Ripollès | 106 |
| Forêt de Maçanet de la Selva (14) | Maçanet de la Selva › la Selva (Gérone) | 105 |
| Forêt de Setcases (67) | Setcases › Ripollès | 105 |
| Forêt de Setcases (68) | Setcases › Ripollès | 105 |
| Forêt de Maçanet de la Selva (9) | Maçanet de la Selva › la Selva (Gérone) | 104 |
| Forêt de Bescanó (21) | Bescanó › Gironès | 104 |
| Forêt de Molló (65) | Molló › Ripollès | 104 |
| Forêt de Sant Feliu de Buixalleu (10) | Sant Feliu de Buixalleu › la Selva (Gérone) | 103 |
| Forêt de Vilanant (6) | Vilanant › Alt Empordà | 103 |
| Forêt de Vilallonga de Ter (25) | Vilallonga de Ter › Ripollès | 103 |
| Forêt de Vidreres | Vidreres › la Selva (Gérone) | 102 |
| Forêt de Foixà (2) | Foixà › Baix Empordà | 101 |
| Forêt de Sant Feliu de Buixalleu (5) | Sant Feliu de Buixalleu › la Selva (Gérone) | 100 |
| Forêt de Viladrau (51) | Viladrau › Osona (Gérone) | 99 |
| Forêt de Tossa de Mar (25) | Tossa de Mar › la Selva (Gérone) | 98 |
| Forêt de Montagut i Oix (54) | Montagut i Oix › Garrotxa | 97 |
| Forêt de Albanyà (22) | Albanyà › Alt Empordà | 97 |
| Forêt de Santa Cristina d'Aro (22) | Santa Cristina d'Aro › Baix Empordà | 95 |
| Forêt de Vilademuls (17) | Vilademuls › Pla de l'Estany | 95 |
| Forêt de Vilademuls (23) | Vilademuls › Pla de l'Estany | 94 |
| Forêt de Boadella i les Escaules | Boadella i les Escaules › Alt Empordà | 94 |
| Forêt de Osor (23) | Osor › la Selva (Gérone) | 93 |
| Forêt de Sant Ferriol (3) | Sant Ferriol › Garrotxa | 92 |
| Forêt de Canet d'Adri (17) | Canet d'Adri › Gironès | 92 |
| Forêt de les Llosses (12) | les Llosses › Ripollès | 91 |
| Forêt de Lloret de Mar (49) | Lloret de Mar › la Selva (Gérone) | 91 |
| Forêt de Ribes de Freser (38) | Ribes de Freser › Ripollès | 91 |
| Forêt de Espolla (5) | Espolla › Alt Empordà | 89 |
| Forêt de Montagut i Oix (82) | Montagut i Oix › Garrotxa | 89 |
| Forêt de Cabanelles (3) | Cabanelles › Alt Empordà | 88 |
| Forêt de les Llosses (42) | les Llosses › Ripollès | 88 |
| Forêt de Sils (2) | Sils › la Selva (Gérone) | 87 |
| Forêt de Pardines (9) | Pardines › Ripollès | 87 |
| Forêt de Albanyà (8) | Albanyà › Alt Empordà | 87 |
| Forêt de Sant Ferriol (8) | Sant Ferriol › Garrotxa | 87 |
| Forêt de Sant Joan de les Abadesses (16) | Sant Joan de les Abadesses › Ripollès | 86 |
| Forêt de les Llosses (26) | les Llosses › Ripollès | 85 |
| Bois de Vilopriu (2) | Vilopriu › Baix Empordà | 85 |
| Forêt de Ripoll (13) | Ripoll › Ripollès | 85 |
| Forêt de Toses (45) | Toses › Ripollès | 85 |
| Forêt de Meranges (5) | Meranges › Cerdanya (Gérone) | 84 |
| Forêt de les Llosses (75) | les Llosses › Ripollès | 84 |
| Bois de Vilallonga de Ter (3) | Vilallonga de Ter › Ripollès | 83 |
| Forêt de les Llosses (115) | les Llosses › Ripollès | 82 |
| Forêt de Tossa de Mar (22) | Tossa de Mar › la Selva (Gérone) | 81 |
| Forêt de Campdevànol (21) | Campdevànol › Ripollès | 80 |
| Forêt de Palol de Revardit (3) | Palol de Revardit › Pla de l'Estany | 79 |
| Forêt de Montagut i Oix (53) | Montagut i Oix › Garrotxa | 79 |
| Forêt de Montagut i Oix (55) | Montagut i Oix › Garrotxa | 79 |
| Forêt de Camprodon (24) | Camprodon › Ripollès | 79 |
| Forêt de Arbúcies (19) | Arbúcies › la Selva (Gérone) | 79 |
| Forêt de Vilademuls (3) | Vilademuls › Pla de l'Estany | 78 |
| Forêt de Fornells de la Selva (23) | Fornells de la Selva › Gironès | 78 |
| Forêt de Vilallonga de Ter (5) | Vilallonga de Ter › Ripollès | 78 |
| Forêt de les Llosses (111) | les Llosses › Ripollès | 78 |
| Forêt de Sant Feliu de Buixalleu (11) | Sant Feliu de Buixalleu › la Selva (Gérone) | 77 |
| Bois de Garrigoles (2) | Garrigoles › Baix Empordà | 77 |
| Forêt de Gombrèn (4) | Gombrèn › Ripollès | 77 |
| Forêt de Portbou | Portbou › Alt Empordà | 77 |
| Forêt de Vidreres (21) | Vidreres › la Selva (Gérone) | 77 |
| Forêt de la Vall de Bianya | la Vall de Bianya › Garrotxa | 76 |
| Forêt de Llagostera (45) | Llagostera › Gironès | 76 |
| Forêt de Vallfogona de Ripollès (9) | Vallfogona de Ripollès › Ripollès | 76 |
| Forêt de Molló (51) | Molló › Ripollès | 76 |
| Forêt de Campelles (14) | Campelles › Ripollès | 76 |
| Forêt de Vilaür | Vilaür › Alt Empordà | 75 |
| Forêt de Sant Hilari Sacalm (21) | Sant Hilari Sacalm › la Selva (Gérone) | 75 |
| Forêt de Campdevànol (3) | Campdevànol › Ripollès | 75 |
| Forêt de Ventalló | Ventalló › Alt Empordà | 74 |
| Forêt de les Planes d'Hostoles (4) | les Planes d'Hostoles › Garrotxa | 74 |
| Forêt de Espinelves (2) | Espinelves › Osona (Gérone) | 73 |
| Forêt de Brunyola i Sant Martí Sapresa (9) | Brunyola i Sant Martí Sapresa › la Selva (Gérone) | 73 |
| Forêt de Toses (10) | Toses › Ripollès | 73 |
| Forêt de les Llosses (128) | les Llosses › Ripollès | 73 |
| Forêt de Tossa de Mar (14) | Tossa de Mar › la Selva (Gérone) | 72 |
| Forêt de Lloret de Mar (28) | Lloret de Mar › la Selva (Gérone) | 72 |
| Bosc d'en Riera | Brunyola i Sant Martí Sapresa › la Selva (Gérone) | 71 |
| Forêt de Sant Miquel de Campmajor (4) | Sant Miquel de Campmajor › Pla de l'Estany | 71 |
| Forêt de Queralbs (25) | Queralbs › Ripollès | 71 |
| Forêt de Tossa de Mar (17) | Tossa de Mar › la Selva (Gérone) | 71 |
| Forêt de les Llosses (99) | les Llosses › Ripollès | 71 |
| Forêt de Montagut i Oix (27) | Montagut i Oix › Garrotxa | 71 |
| Forêt de Camprodon (37) | Camprodon › Ripollès | 71 |
| Forêt de Vilallonga de Ter (14) | Vilallonga de Ter › Ripollès | 71 |
| Forêt de Riudarenes (23) | Riudarenes › la Selva (Gérone) | 71 |
| Forêt de Vilallonga de Ter (6) | Vilallonga de Ter › Ripollès | 70 |
| Forêt de Sant Joan de les Abadesses (8) | Sant Joan de les Abadesses › Ripollès | 69 |
| Forêt de Cervià de Ter (36) | Cervià de Ter › Gironès | 69 |
| Forêt de Palol de Revardit (8) | Palol de Revardit › Pla de l'Estany | 69 |
| Forêt de Viladrau (49) | Viladrau › Osona (Gérone) | 69 |
| Forêt de Santa Pau (19) | Santa Pau › Garrotxa | 69 |
| Forêt de Ogassa (6) | Ogassa › Ripollès | 68 |
| Forêt de Ripoll (43) | Ripoll › Ripollès | 68 |
| Forêt de Bàscara (14) | Bàscara › Alt Empordà | 68 |
| Forêt de Maçanet de Cabrenys (12) | Maçanet de Cabrenys › Alt Empordà | 68 |
| Forêt de Molló (8) | Molló › Ripollès | 68 |
| Forêt de les Llosses (130) | les Llosses › Ripollès | 68 |
| Forêt de les Llosses (136) | les Llosses › Ripollès | 67 |
| Bosc d'en Nadal | Cruïlles, Monells i Sant Sadurní de l'Heura › Baix Empordà | 66 |
| Forêt de les Llosses (59) | les Llosses › Ripollès | 66 |
| Forêt de Campelles (5) | Campelles › Ripollès | 66 |
| Forêt de les Llosses (129) | les Llosses › Ripollès | 66 |
| Forêt de Vilallonga de Ter (4) | Vilallonga de Ter › Ripollès | 65 |
| Forêt de Palol de Revardit (5) | Palol de Revardit › Pla de l'Estany | 65 |
| Forêt de Agullana (3) | Agullana › Alt Empordà | 65 |
| Forêt de Toses (40) | Toses › Ripollès | 65 |
| Forêt de les Llosses (19) | les Llosses › Ripollès | 64 |
| Forêt de Borrassà (4) | Borrassà › Alt Empordà | 64 |
| Forêt de Sant Joan de les Abadesses (20) | Sant Joan de les Abadesses › Ripollès | 64 |
| Forêt de Sant Jordi Desvalls (4) | Sant Jordi Desvalls › Gironès | 64 |
| Forêt de Santa Cristina d'Aro (23) | Santa Cristina d'Aro › Baix Empordà | 63 |
| Forêt de Montagut i Oix (26) | Montagut i Oix › Garrotxa | 63 |
| Forêt de Meranges (14) | Meranges › Cerdanya (Gérone) | 63 |
| Forêt de Sant Joan de les Abadesses (13) | Sant Joan de les Abadesses › Ripollès | 63 |
| Forêt de Llanars (26) | Llanars › Ripollès | 63 |
| Forêt de Sant Feliu de Buixalleu (9) | Sant Feliu de Buixalleu › la Selva (Gérone) | 62 |
| Forêt de Maçanet de Cabrenys (15) | Maçanet de Cabrenys › Alt Empordà | 62 |
| Forêt de Cornellà del Terri (13) | Cornellà del Terri › Pla de l'Estany | 61 |
| Forêt de Riells i Viabrea (14) | Riells i Viabrea › la Selva (Gérone) | 61 |
| Forêt de Maçanet de Cabrenys (17) | Maçanet de Cabrenys › Alt Empordà | 61 |
| Forêt de Molló (73) | Molló › Ripollès | 61 |
| Forêt de Molló (74) | Molló › Ripollès | 61 |
| Forêt de Sant Feliu de Buixalleu (21) | Sant Feliu de Buixalleu › la Selva (Gérone) | 61 |
| Forêt de Sils (13) | Sils › la Selva (Gérone) | 60 |
| Forêt de Sant Julià de Ramis (9) | Sant Julià de Ramis › Gironès | 60 |
| Forêt de Sils (33) | Sils › la Selva (Gérone) | 60 |
| Forêt de Sales de Llierca (8) | Sales de Llierca › Garrotxa | 60 |
| Forêt de Setcases (81) | Setcases › Ripollès | 60 |
| Forêt de Llanars (13) | Llanars › Ripollès | 60 |
| Forêt de Pardines (2) | Pardines › Ripollès | 59 |
| Forêt de Santa Pau (13) | Santa Pau › Garrotxa | 59 |
| Forêt de Vidreres (13) | Vidreres › la Selva (Gérone) | 59 |
| Forêt de les Llosses (71) | les Llosses › Ripollès | 59 |
| Forêt de Montagut i Oix (83) | Montagut i Oix › Garrotxa | 59 |
| Forêt de Palau de Santa Eulàlia | Palau de Santa Eulàlia › Alt Empordà | 58 |
| Forêt de Tortellà (2) | Tortellà › Garrotxa | 58 |
| Forêt de Camprodon (19) | Camprodon › Ripollès | 58 |
| Forêt de Montagut i Oix (23) | Montagut i Oix › Garrotxa | 58 |
| Forêt de Maçanet de Cabrenys (19) | Maçanet de Cabrenys › Alt Empordà | 58 |
| Forêt de Vilallonga de Ter (18) | Vilallonga de Ter › Ripollès | 58 |
| Forêt de Santa Pau (4) | Santa Pau › Garrotxa | 57 |
| Forêt de Porqueres (5) | Porqueres › Pla de l'Estany | 57 |
| Forêt de la Jonquera (16) | la Jonquera › Alt Empordà | 57 |
| Forêt de Ribes de Freser (8) | Ribes de Freser › Ripollès | 57 |
| Forêt de Camprodon (14) | Camprodon › Ripollès | 57 |
| Forêt de les Llosses (60) | les Llosses › Ripollès | 57 |
| Forêt de les Llosses (117) | les Llosses › Ripollès | 57 |
| Forêt de Massanes (17) | Massanes › la Selva (Gérone) | 57 |
| Forêt de Porqueres (11) | Porqueres › Pla de l'Estany | 56 |
| Forêt de Tossa de Mar (34) | Tossa de Mar › la Selva (Gérone) | 56 |
| Forêt de Massanes (7) | Massanes › la Selva (Gérone) | 55 |
| Forêt de Ribes de Freser (5) | Ribes de Freser › Ripollès | 55 |
| Forêt de Viladrau (36) | Viladrau › Osona (Gérone) | 55 |
| Forêt de Gombrèn (10) | Gombrèn › Ripollès | 55 |
| Forêt de Ribes de Freser (35) | Ribes de Freser › Ripollès | 55 |
| Forêt de Molló (35) | Molló › Ripollès | 55 |
| Forêt de Maçanet de la Selva (13) | Maçanet de la Selva › la Selva (Gérone) | 54 |
| Forêt de Tossa de Mar (16) | Tossa de Mar › la Selva (Gérone) | 54 |
| Forêt de Campdevànol (10) | Campdevànol › Ripollès | 54 |
| Forêt de Maçanet de Cabrenys (18) | Maçanet de Cabrenys › Alt Empordà | 54 |
| Forêt de Camprodon (34) | Camprodon › Ripollès | 54 |
| Forêt de Viladrau (12) | Viladrau › Osona (Gérone) | 53 |
| Forêt de Viladrau (40) | Viladrau › Osona (Gérone) | 53 |
| Bois de Brunyola i Sant Martí Sapresa (2) | Brunyola i Sant Martí Sapresa › la Selva (Gérone) | 53 |
| Forêt de Ribes de Freser (31) | Ribes de Freser › Ripollès | 53 |
| Forêt de Vilallonga de Ter (10) | Vilallonga de Ter › Ripollès | 53 |
| Forêt de Begur (25) | Begur › Baix Empordà | 52 |
| Forêt de Campelles (3) | Campelles › Ripollès | 52 |
| Forêt de Sant Joan de les Abadesses (26) | Sant Joan de les Abadesses › Ripollès | 52 |
| Forêt de Viladrau (13) | Viladrau › Osona (Gérone) | 51 |
| Forêt de Canet d'Adri (4) | Canet d'Adri › Gironès | 51 |
| Forêt de Vilademuls (16) | Vilademuls › Pla de l'Estany | 51 |
| Forêt de Capmany (2) | Capmany › Alt Empordà | 51 |
| Forêt de Begur (19) | Begur › Baix Empordà | 51 |
| Forêt de Gombrèn (9) | Gombrèn › Ripollès | 51 |
| Forêt de Molló (76) | Molló › Ripollès | 51 |
| Forêt de Ribes de Freser (40) | Ribes de Freser › Ripollès | 51 |
| Forêt de Ventalló (26) | Ventalló › Alt Empordà | 51 |
| Forêt de Riudarenes (3) | Riudarenes › la Selva (Gérone) | 50 |
| Bosc d'en Ros (2) | Aiguaviva › Gironès | 50 |
| Forêt de Mieres (3) | Mieres › Garrotxa | 50 |
| Forêt de Forallac (43) | Forallac › Baix Empordà | 50 |
| Forêt de la Vall de Bianya (14) | la Vall de Bianya › Garrotxa | 50 |
| Forêt de la Jonquera | la Jonquera › Alt Empordà | 49 |
| Forêt de Ribes de Freser (2) | Ribes de Freser › Ripollès | 49 |
| Forêt de Ordis (3) | Ordis › Alt Empordà | 49 |
| Forêt de Bolvir (2) | Bolvir › Cerdanya (Gérone) | 49 |
| Forêt de Gombrèn (63) | Gombrèn › Ripollès | 49 |
| Forêt de Montagut i Oix (56) | Montagut i Oix › Garrotxa | 49 |
| Forêt de Vilademuls (2) | Vilademuls › Pla de l'Estany | 48 |
| Bois de Sant Feliu de Buixalleu (4) | Sant Feliu de Buixalleu › la Selva (Gérone) | 48 |
| Forêt de Fontanals de Cerdanya (46) | Fontanals de Cerdanya › Cerdanya (Gérone) | 48 |
| Forêt de Ogassa (5) | Ogassa › Ripollès | 47 |
| Forêt de Vilaür (5) | Vilaür › Alt Empordà | 47 |
| Forêt de Canet d'Adri (16) | Canet d'Adri › Gironès | 47 |
| Forêt de Garrigoles (11) | Garrigoles › Baix Empordà | 47 |
| Forêt de Gombrèn (7) | Gombrèn › Ripollès | 47 |
| Forêt de Planoles (2) | Planoles › Ripollès | 47 |
| Forêt de Montagut i Oix (29) | Montagut i Oix › Garrotxa | 47 |
| Forêt de Ogassa (2) | Ogassa › Ripollès | 46 |
| Forêt de Molló (15) | Molló › Ripollès | 46 |
| Forêt de Sant Mori (7) | Sant Mori › Alt Empordà | 46 |
| Forêt de Darnius (2) | Darnius › Alt Empordà | 45 |
| Forêt de Pontós (4) | Pontós › Alt Empordà | 45 |
| Forêt de les Llosses (62) | les Llosses › Ripollès | 45 |
| Forêt de Montagut i Oix (25) | Montagut i Oix › Garrotxa | 45 |
| Forêt de Camprodon (29) | Camprodon › Ripollès | 45 |
| Forêt de la Vall de Bianya (16) | la Vall de Bianya › Garrotxa | 45 |
| Forêt de Vilademuls (19) | Vilademuls › Pla de l'Estany | 44 |
| Forêt de Queralbs (30) | Queralbs › Ripollès | 44 |
| Forêt de la Jonquera (20) | la Jonquera › Alt Empordà | 44 |
| Forêt de Vilallonga de Ter (29) | Vilallonga de Ter › Ripollès | 44 |
| Forêt de Garrigàs (21) | Garrigàs › Alt Empordà | 44 |
| Forêt de Garrigoles | Garrigoles › Baix Empordà | 43 |
| Forêt de les Llosses (28) | les Llosses › Ripollès | 43 |
| Forêt de Blanes (11) | Blanes › la Selva (Gérone) | 43 |
| Forêt de Viladamat (4) | Viladamat › Alt Empordà | 43 |
| Forêt de Gombrèn (3) | Gombrèn › Ripollès | 43 |
| Forêt de Ribes de Freser (9) | Ribes de Freser › Ripollès | 43 |
| Forêt de Cabanelles (6) | Cabanelles › Alt Empordà | 43 |
| Forêt de Llanars (16) | Llanars › Ripollès | 43 |
| Forêt de Crespià | Crespià › Pla de l'Estany | 42 |
| Forêt de les Planes d'Hostoles | les Planes d'Hostoles › Garrotxa | 42 |
| Forêt de Viladrau (29) | Viladrau › Osona (Gérone) | 42 |
| Forêt de Vilobí d'Onyar (41) | Vilobí d'Onyar › la Selva (Gérone) | 42 |
| Forêt de Torroella de Montgrí (62) | Torroella de Montgrí › Baix Empordà | 42 |
| Forêt de Sant Julià de Ramis (8) | Sant Julià de Ramis › Gironès | 41 |
| Forêt de la Jonquera (17) | la Jonquera › Alt Empordà | 41 |
| Forêt de les Llosses (105) | les Llosses › Ripollès | 41 |
| Forêt de Ogassa (11) | Ribes de Freser › Ripollès | 41 |
| Forêt de Sant Mori (8) | Sant Mori › Alt Empordà | 41 |
| Forêt de Sant Joan de les Abadesses (5) | Sant Joan de les Abadesses › Ripollès | 40 |
| Forêt de Campllong (18) | Campllong › Gironès | 40 |
| Forêt de Sant Ferriol (4) | Sant Ferriol › Garrotxa | 40 |
| Forêt de Ogassa (14) | Ogassa › Ripollès | 40 |
| Forêt de Meranges (10) | Meranges › Cerdanya (Gérone) | 40 |
| Forêt de Sant Joan de les Abadesses (4) | Sant Joan de les Abadesses › Ripollès | 39 |
| Forêt de Saus, Camallera i Llampaies (2) | Saus, Camallera i Llampaies › Alt Empordà | 39 |
| Forêt de Torrent | Torrent › Baix Empordà | 39 |
| Forêt de Sant Feliu de Buixalleu (16) | Sant Feliu de Buixalleu › la Selva (Gérone) | 39 |
| Forêt de Viladrau (30) | Viladrau › Osona (Gérone) | 39 |
| Forêt de Fontanals de Cerdanya (2) | Fontanals de Cerdanya › Cerdanya (Gérone) | 39 |
| Forêt de Castell d'Aro, Platja d'Aro i s'Agaró (32) | Castell d'Aro, Platja d'Aro i s'Agaró › Baix Empordà | 39 |
| Forêt de Viladrau (37) | Viladrau › Osona (Gérone) | 39 |
| Forêt de Gombrèn (5) | Gombrèn › Ripollès | 39 |
| Forêt de Gombrèn (38) | Gombrèn › Ripollès | 39 |
| Forêt de Molló (72) | Molló › Ripollès | 39 |
| Forêt de Campelles (12) | Campelles › Ripollès | 39 |
| Forêt de les Llosses (11) | les Llosses › Ripollès | 38 |
| Forêt de Vilallonga de Ter (2) | Vilallonga de Ter › Ripollès | 38 |
| Forêt de Arbúcies (14) | Arbúcies › la Selva (Gérone) | 38 |
| Forêt de Camós (4) | Camós › Pla de l'Estany | 38 |
| Forêt de Tossa de Mar (31) | Tossa de Mar › la Selva (Gérone) | 38 |
| Forêt de Campdevànol (14) | Campdevànol › Ripollès | 38 |
| Forêt de Sant Llorenç de la Muga (24) | Sant Llorenç de la Muga › Alt Empordà | 38 |
| Forêt de Maçanet de Cabrenys (26) | Maçanet de Cabrenys › Alt Empordà | 38 |
| Forêt de Ripoll (6) | Ripoll › Ripollès | 37 |
| Forêt de Queralbs (23) | Queralbs › Ripollès | 37 |
| Forêt de Camprodon (20) | Camprodon › Ripollès | 37 |
| Forêt de Vilallonga de Ter (15) | Vilallonga de Ter › Ripollès | 37 |
| Forêt de Riudarenes (2) | Riudarenes › la Selva (Gérone) | 36 |
| Forêt de Maçanet de la Selva (7) | Maçanet de la Selva › la Selva (Gérone) | 36 |
| Forêt de Pardines (4) | Pardines › Ripollès | 36 |
| Forêt de Queralbs | Queralbs › Ripollès | 36 |
| Forêt de Sils | Sils › la Selva (Gérone) | 36 |
| Forêt de Vilademuls (5) | Vilademuls › Pla de l'Estany | 36 |
| Forêt de Toses (5) | Toses › Ripollès | 36 |
| Forêt de Mieres (2) | Mieres › Garrotxa | 36 |
| Forêt de Gombrèn (13) | Gombrèn › Ripollès | 36 |
| Forêt de Ventalló (13) | Ventalló › Alt Empordà | 36 |
| Forêt de Saus, Camallera i Llampaies | Saus, Camallera i Llampaies › Alt Empordà | 35 |
| Forêt de les Llosses (24) | les Llosses › Ripollès | 35 |
| Forêt de Arbúcies (13) | Arbúcies › la Selva (Gérone) | 35 |
| Forêt de la Vall de Bianya (11) | la Vall de Bianya › Garrotxa | 35 |
| Forêt de Espinelves (9) | Espinelves › Osona (Gérone) | 35 |
| Forêt de Sant Feliu de Buixalleu (26) | Sant Feliu de Buixalleu › la Selva (Gérone) | 35 |
| Forêt de Sant Mori (9) | Sant Mori › Alt Empordà | 35 |
| Forêt de Sant Ferriol | Sant Ferriol › Garrotxa | 34 |
| Forêt de Llers (2) | Llers › Alt Empordà | 34 |
| Forêt de Santa Pau (3) | Santa Pau › Garrotxa | 34 |
| Forêt de Vallfogona de Ripollès (5) | Vallfogona de Ripollès › Ripollès | 34 |
| Forêt de Sant Aniol de Finestres | Sant Aniol de Finestres › Garrotxa | 34 |
| Forêt de Arbúcies (9) | Arbúcies › la Selva (Gérone) | 34 |
| Forêt de Alp (88) | Alp › Cerdanya (Gérone) | 34 |
| Forêt de Vilademuls (22) | Vilademuls › Pla de l'Estany | 34 |
| Forêt de Begur (16) | Begur › Baix Empordà | 34 |
| Forêt de les Llosses (95) | les Llosses › Ripollès | 34 |
| Forêt de les Llosses (96) | les Llosses › Ripollès | 34 |
| Forêt de Gombrèn (62) | Gombrèn › Ripollès | 34 |
| Forêt de Campdevànol (61) | Campdevànol › Ripollès | 34 |
| Forêt de Sales de Llierca (5) | Sales de Llierca › Garrotxa | 34 |
| Forêt de Camprodon (31) | Camprodon › Ripollès | 34 |
| Forêt de Viladrau (50) | Viladrau › Osona (Gérone) | 34 |
| Forêt de Sant Julià de Ramis (17) | Sant Julià de Ramis › Gironès | 34 |
| Forêt de Pontós (6) | Pontós › Alt Empordà | 34 |
| Forêt de Massanes (14) | Massanes › la Selva (Gérone) | 33 |
| Forêt de Caldes de Malavella (28) | Caldes de Malavella › la Selva (Gérone) | 33 |
| Forêt de Llagostera (43) | Llagostera › Gironès | 33 |
| Forêt de Toses (14) | Toses › Ripollès | 33 |
| Forêt de Tortellà (3) | Tortellà › Garrotxa | 33 |
| Forêt de Sant Mori (10) | Sant Mori › Alt Empordà | 33 |
| Forêt de Llers | Llers › Alt Empordà | 32 |
| Forêt de Palafrugell (116) | Palafrugell › Baix Empordà | 32 |
| Forêt de Sant Hilari Sacalm (24) | Sant Hilari Sacalm › la Selva (Gérone) | 32 |
| Forêt de Vilademuls (20) | Vilademuls › Pla de l'Estany | 32 |
| Forêt de Camprodon (6) | Camprodon › Ripollès | 32 |
| Forêt de Sant Climent Sescebes (2) | Cantallops › Alt Empordà | 32 |
| Forêt de Gombrèn (54) | Gombrèn › Ripollès | 32 |
| Forêt de Ribes de Freser (24) | Ribes de Freser › Ripollès | 32 |
| Forêt de Montagut i Oix (9) | Montagut i Oix › Garrotxa | 32 |
| Forêt de Maçanet de Cabrenys (22) | Maçanet de Cabrenys › Alt Empordà | 32 |
| Forêt de Molló (48) | Molló › Ripollès | 32 |
| Forêt de Llanars (10) | Llanars › Ripollès | 32 |
| Forêt de les Llosses (134) | les Llosses › Ripollès | 32 |
| Forêt de Palau de Santa Eulàlia (2) | Palau de Santa Eulàlia › Alt Empordà | 32 |
| Forêt de Cabanelles | Cabanelles › Alt Empordà | 31 |
| Forêt de Garrigàs | Garrigàs › Alt Empordà | 31 |
| Forêt de Regencós | Regencós › Baix Empordà | 31 |
| Forêt de Viladamat (3) | Viladamat › Alt Empordà | 31 |
| Forêt de Alp (95) | Alp › Cerdanya (Gérone) | 31 |
| Forêt de Ger (13) | Ger › Cerdanya (Gérone) | 31 |
| Forêt de Campdevànol (63) | Campdevànol › Ripollès | 31 |
| Forêt de Vilallonga de Ter (11) | Vilallonga de Ter › Ripollès | 31 |
| Forêt de la Vall de Bianya (13) | la Vall de Bianya › Garrotxa | 31 |
| Forêt de Arbúcies (23) | Arbúcies › la Selva (Gérone) | 31 |
| Forêt de Llanars (24) | Llanars › Ripollès | 31 |
| Forêt de Corçà (2) | Corçà › Baix Empordà | 30 |
| Forêt de Caldes de Malavella (19) | Sils › la Selva (Gérone) | 30 |
| Forêt de Arbúcies (11) | Arbúcies › la Selva (Gérone) | 30 |
| Forêt de Vilobí d'Onyar (42) | Vilobí d'Onyar › la Selva (Gérone) | 30 |
| Forêt de Porqueres (6) | Porqueres › Pla de l'Estany | 30 |
| Forêt de Pardines (10) | Pardines › Ripollès | 30 |
| Forêt de Espolla (8) | Espolla › Alt Empordà | 30 |
| Forêt de Setcases (65) | Setcases › Ripollès | 30 |
| Forêt de Planoles (4) | Planoles › Ripollès | 30 |
| Forêt de Toses (49) | Toses › Ripollès | 30 |
| Forêt de Vilademuls (37) | Vilademuls › Pla de l'Estany | 30 |
| Forêt de Garrigoles (2) | Garrigoles › Baix Empordà | 29 |
| Forêt de Canet d'Adri (14) | Canet d'Adri › Gironès | 29 |
| Forêt de Ribes de Freser (7) | Ribes de Freser › Ripollès | 29 |
| Forêt de Fontanals de Cerdanya (3) | Fontanals de Cerdanya › Cerdanya (Gérone) | 29 |
| Forêt de Campdevànol (8) | Campdevànol › Ripollès | 29 |
| Forêt de Montagut i Oix (24) | Montagut i Oix › Garrotxa | 29 |
| Forêt de Maçanet de Cabrenys (6) | Maçanet de Cabrenys › Alt Empordà | 29 |
| Forêt de Maçanet de Cabrenys (11) | Maçanet de Cabrenys › Alt Empordà | 29 |
| Forêt de Maçanet de Cabrenys (28) | Maçanet de Cabrenys › Alt Empordà | 29 |
| Forêt de Lloret de Mar (50) | Lloret de Mar › la Selva (Gérone) | 29 |
| Forêt de Sant Hilari Sacalm (34) | Sant Hilari Sacalm › la Selva (Gérone) | 29 |
| Forêt de Sant Joan de les Abadesses | Sant Joan de les Abadesses › Ripollès | 28 |
| Forêt de les Llosses (22) | les Llosses › Ripollès | 28 |
| Forêt de Foixà (10) | Foixà › Baix Empordà | 28 |
| Forêt de Ordis (2) | Ordis › Alt Empordà | 28 |
| Forêt de les Llosses (69) | les Llosses › Ripollès | 28 |
| Forêt de Gombrèn (27) | Gombrèn › Ripollès | 28 |
| Forêt de les Llosses (103) | les Llosses › Ripollès | 28 |
| Forêt de Montagut i Oix (28) | Montagut i Oix › Garrotxa | 28 |
| Forêt de Montagut i Oix (31) | Montagut i Oix › Garrotxa | 28 |
| Forêt de Rabós (2) | Rabós › Alt Empordà | 28 |
| Forêt de Rabós (5) | Rabós › Alt Empordà | 28 |
| Forêt de Molló (9) | Molló › Ripollès | 28 |
| Forêt de Molló (27) | Molló › Ripollès | 28 |
| Forêt de Vilallonga de Ter (12) | Vilallonga de Ter › Ripollès | 28 |
| Forêt de Vilademuls (24) | Vilademuls › Pla de l'Estany | 28 |
| Forêt de Sant Ferriol (15) | Sant Ferriol › Garrotxa | 28 |
| Forêt de Vilopriu (5) | Vilopriu › Baix Empordà | 28 |
| Forêt de les Llosses (15) | les Llosses › Ripollès | 27 |
| Forêt de Lladó | Lladó › Alt Empordà | 27 |
| Forêt de Cistella (2) | Cistella › Alt Empordà | 27 |
| Forêt de Cornellà del Terri (22) | Cornellà del Terri › Pla de l'Estany | 27 |
| Forêt de Cornellà del Terri (23) | Cornellà del Terri › Pla de l'Estany | 27 |
| Forêt de Ribes de Freser (13) | Ribes de Freser › Ripollès | 27 |
| Forêt de les Llosses (57) | les Llosses › Ripollès | 27 |
| Forêt de Fontanals de Cerdanya (49) | Fontanals de Cerdanya › Cerdanya (Gérone) | 27 |
| Forêt de la Vajol (54) | la Vajol › Alt Empordà | 27 |
| Forêt de Meranges (8) | Meranges › Cerdanya (Gérone) | 27 |
| Forêt de Vilallonga de Ter | Vilallonga de Ter › Ripollès | 26 |
| Forêt de Espinelves (3) | Espinelves › Osona (Gérone) | 26 |
| Forêt de Sant Hilari Sacalm (13) | Sant Hilari Sacalm › la Selva (Gérone) | 26 |
| Forêt de la Bisbal d'Empordà | la Bisbal d'Empordà › Baix Empordà | 26 |
| Forêt de la Pera (5) | la Pera › Baix Empordà | 26 |
| Forêt de Cornellà del Terri (15) | Cornellà del Terri › Pla de l'Estany | 26 |
| Forêt de la Jonquera (14) | la Jonquera › Alt Empordà | 26 |
| Forêt de Campdevànol (5) | Campdevànol › Ripollès | 26 |
| Bois de Sant Jaume de Llierca | Sant Jaume de Llierca › Garrotxa | 26 |
| Forêt de Ribes de Freser (25) | Ribes de Freser › Ripollès | 26 |
| Forêt de la Vall de Bianya (9) | la Vall de Bianya › Garrotxa | 26 |
| Forêt de la Vajol (55) | la Vajol › Alt Empordà | 26 |
| Forêt de la Jonquera (24) | Espolla › Alt Empordà | 26 |
| Forêt de Ribes de Freser (39) | Ribes de Freser › Ripollès | 26 |
| Forêt de Meranges (15) | Meranges › Cerdanya (Gérone) | 26 |
| Forêt de Camprodon (51) | Camprodon › Ripollès | 26 |
| Forêt de Arbúcies (29) | Arbúcies › la Selva (Gérone) | 26 |
| Forêt de Hostalric (5) | Hostalric › la Selva (Gérone) | 26 |
| Forêt de Sant Julià de Ramis | Sant Julià de Ramis › Gironès | 25 |
| Forêt de Llanars | Llanars › Ripollès | 25 |
| Forêt de Viladrau (19) | Viladrau › Osona (Gérone) | 25 |
| Forêt de Viladrau (28) | Viladrau › Osona (Gérone) | 25 |
| Forêt de Sant Llorenç de la Muga (3) | Sant Llorenç de la Muga › Alt Empordà | 25 |
| Forêt de Cistella (7) | Cistella › Alt Empordà | 25 |
| Forêt de la Jonquera (12) | la Jonquera › Alt Empordà | 25 |
| Forêt de Ger (5) | Ger › Cerdanya (Gérone) | 25 |
| Forêt de Torroella de Montgrí (70) | Torroella de Montgrí › Baix Empordà | 25 |
| Forêt de Ripoll (35) | Ripoll › Ripollès | 25 |
| Forêt de Toses (22) | Toses › Ripollès | 25 |
| Forêt de les Llosses (88) | les Llosses › Ripollès | 25 |
| Forêt de les Llosses (89) | les Llosses › Ripollès | 25 |
| Forêt de Campdevànol (13) | Campdevànol › Ripollès | 25 |
| Forêt de les Llosses (109) | les Llosses › Ripollès | 25 |
| Forêt de Vallfogona de Ripollès (15) | Vallfogona de Ripollès › Ripollès | 25 |
| Forêt de Sales de Llierca (14) | Sales de Llierca › Garrotxa | 25 |
| Forêt de Rabós (14) | Rabós › Alt Empordà | 25 |
| Forêt de Ger (24) | Ger › Cerdanya (Gérone) | 25 |
| Forêt de Ripoll (82) | Ripoll › Ripollès | 25 |
| Forêt de Ripoll (86) | Ripoll › Ripollès | 25 |
| Forêt de Sant Miquel de Fluvià (3) | Sant Miquel de Fluvià › Alt Empordà | 25 |
| Forêt de Santa Pau | Santa Pau › Garrotxa | 24 |
| Forêt de Girona (3) | Girona › Gironès | 24 |
| Forêt de Maçanet de la Selva (6) | Maçanet de la Selva › la Selva (Gérone) | 24 |
| Forêt de Espolla | Espolla › Alt Empordà | 24 |
| Forêt de Vidreres (2) | Vidreres › la Selva (Gérone) | 24 |
| Forêt de Sant Hilari Sacalm (15) | Sant Hilari Sacalm › la Selva (Gérone) | 24 |
| Forêt de Maià de Montcal (2) | Maià de Montcal › Garrotxa | 24 |
| Forêt de Girona (60) | Girona › Gironès | 24 |
| Forêt de Fornells de la Selva (18) | Fornells de la Selva › Gironès | 24 |
| Forêt de Torroella de Fluvià (8) | Torroella de Fluvià › Alt Empordà | 24 |
| Forêt de Viladrau (31) | Viladrau › Osona (Gérone) | 24 |
| Forêt de Palamós (12) | Palamós › Baix Empordà | 24 |
| Forêt de Fontcoberta (9) | Fontcoberta › Pla de l'Estany | 24 |
| Forêt de Cornellà del Terri (19) | Cornellà del Terri › Pla de l'Estany | 24 |
| Forêt de Albanyà (9) | Albanyà › Alt Empordà | 24 |
| Forêt de Camprodon (11) | Camprodon › Ripollès | 24 |
| Forêt de Vallfogona de Ripollès (20) | Vallfogona de Ripollès › Ripollès | 24 |
| Forêt de Albanyà (11) | Albanyà › Alt Empordà | 24 |
| Forêt de Molló (24) | Molló › Ripollès | 24 |
| Forêt de Toses (38) | Toses › Ripollès | 24 |
| Forêt de Sant Joan de les Abadesses (24) | Sant Joan de les Abadesses › Ripollès | 24 |
| Forêt de Sant Pau de Segúries (8) | Sant Pau de Segúries › Ripollès | 24 |
| Forêt de les Llosses (112) | les Llosses › Ripollès | 24 |
| Forêt de Isòvol (11) | Isòvol › Cerdanya (Gérone) | 24 |
| Forêt de Garrigàs (19) | Garrigàs › Alt Empordà | 24 |
| Forêt de Beuda | Beuda › Garrotxa | 23 |
| Forêt de Pardines (3) | Pardines › Ripollès | 23 |
| Forêt de Cistella | Cistella › Alt Empordà | 23 |
| Bois de Flaçà | Flaçà › Gironès | 23 |
| Forêt de Santa Cristina d'Aro (25) | Santa Cristina d'Aro › Baix Empordà | 23 |
| Forêt de Queralbs (31) | Queralbs › Ripollès | 23 |
| Forêt de Gombrèn (18) | Gombrèn › Ripollès | 23 |
| Forêt de Montagut i Oix (17) | Montagut i Oix › Garrotxa | 23 |
| Forêt de Maçanet de Cabrenys (14) | Maçanet de Cabrenys › Alt Empordà | 23 |
| Forêt de Beuda (6) | Beuda › Garrotxa | 23 |
| Forêt de Sant Feliu de Buixalleu (2) | Sant Feliu de Buixalleu › la Selva (Gérone) | 22 |
| Forêt de Ogassa (4) | Ogassa › Ripollès | 22 |
| Forêt de Maçanet de la Selva (8) | Maçanet de la Selva › la Selva (Gérone) | 22 |
| Forêt de Esponellà (2) | Esponellà › Pla de l'Estany | 22 |
| Forêt de Toses (7) | Toses › Ripollès | 22 |
| Forêt de Torroella de Montgrí (71) | Torroella de Montgrí › Baix Empordà | 22 |
| Forêt de Lloret de Mar (40) | Lloret de Mar › la Selva (Gérone) | 22 |
| Forêt de les Llosses (72) | les Llosses › Ripollès | 22 |
| Forêt de Vallfogona de Ripollès (10) | Vallfogona de Ripollès › Ripollès | 22 |
| Forêt de Gombrèn (8) | Gombrèn › Ripollès | 22 |
| Forêt de Toses (23) | Toses › Ripollès | 22 |
| Forêt de Montagut i Oix (71) | Montagut i Oix › Garrotxa | 22 |
| Forêt de Molló (49) | Molló › Ripollès | 22 |
| Forêt de Molló (56) | Molló › Ripollès | 22 |
| Forêt de Llanars (18) | Llanars › Ripollès | 22 |
| Forêt de Llanars (19) | Llanars › Ripollès | 22 |
| Forêt de Sant Ferriol (11) | Sant Ferriol › Garrotxa | 22 |
| Forêt de Borrassà | Borrassà › Alt Empordà | 21 |
| Forêt de Ogassa | Ogassa › Ripollès | 21 |
| Forêt de Caldes de Malavella | Caldes de Malavella › la Selva (Gérone) | 21 |
| Forêt de Caldes de Malavella (3) | Caldes de Malavella › la Selva (Gérone) | 21 |
| Forêt de la Jonquera (4) | la Jonquera › Alt Empordà | 21 |
| Forêt de Riudellots de la Selva | Riudellots de la Selva › la Selva (Gérone) | 21 |
| Forêt de Llanars (4) | Llanars › Ripollès | 21 |
| Forêt de Caldes de Malavella (27) | Caldes de Malavella › la Selva (Gérone) | 21 |
| Forêt de la Vajol (47) | la Vajol › Alt Empordà | 21 |
| Forêt de Fontcoberta (10) | Fontcoberta › Pla de l'Estany | 21 |
| Forêt de Lloret de Mar (34) | Lloret de Mar › la Selva (Gérone) | 21 |
| Forêt de Arbúcies (15) | Arbúcies › la Selva (Gérone) | 21 |
| Forêt de Campelles (4) | Campelles › Ripollès | 21 |
| Forêt de Montagut i Oix (21) | Montagut i Oix › Garrotxa | 21 |
| Forêt de Maçanet de Cabrenys (16) | Maçanet de Cabrenys › Alt Empordà | 21 |
| Forêt de Molló (16) | Molló › Ripollès | 21 |
| Forêt de Molló (52) | Molló › Ripollès | 21 |
| Forêt de Molló (84) | Molló › Ripollès | 21 |
| Forêt de Arbúcies (18) | Arbúcies › la Selva (Gérone) | 21 |
| Bois de Amer (4) | Amer › la Selva (Gérone) | 21 |
| Forêt de Sant Ferriol (17) | Sant Ferriol › Garrotxa | 21 |
| Forêt de Alp (74) | Alp › Cerdanya (Gérone) | 20 |
| Bois de Pardines | Pardines › Ripollès | 20 |
| Forêt de Sant Hilari Sacalm (25) | Sant Hilari Sacalm › la Selva (Gérone) | 20 |
| Forêt de Meranges (4) | Meranges › Cerdanya (Gérone) | 20 |
| Forêt de Sant Feliu de Guíxols (30) | Sant Feliu de Guíxols › Baix Empordà | 20 |
| Forêt de Riudarenes (15) | Riudarenes › la Selva (Gérone) | 20 |
| Forêt de Gombrèn (28) | Gombrèn › Ripollès | 20 |
| Forêt de Gombrèn (39) | Gombrèn › Ripollès | 20 |
| Forêt de Sales de Llierca (2) | Sales de Llierca › Garrotxa | 20 |
| Forêt de Maçanet de Cabrenys (13) | Maçanet de Cabrenys › Alt Empordà | 20 |
| Forêt de Espolla (4) | Espolla › Alt Empordà | 20 |
| Forêt de Molló (57) | Molló › Ripollès | 20 |
| Forêt de Llanars (14) | Llanars › Ripollès | 20 |
| Forêt de Setcases (105) | Setcases › Ripollès | 20 |
| Forêt de Sils (34) | Sils › la Selva (Gérone) | 20 |
| Forêt de Susqueda (10) | Susqueda › la Selva (Gérone) | 20 |
| Forêt de Tossa de Mar (44) | Tossa de Mar › la Selva (Gérone) | 20 |
| Forêt de les Llosses (13) | les Llosses › Ripollès | 19 |
| Forêt de Sant Joan de les Abadesses (6) | Sant Joan de les Abadesses › Ripollès | 19 |
| Forêt de Pardines (6) | Pardines › Ripollès | 19 |
| Forêt de les Llosses (30) | les Llosses › Ripollès | 19 |
| Forêt de Vilobí d'Onyar (24) | Vilobí d'Onyar › la Selva (Gérone) | 19 |
| Forêt de Das (5) | Das › Cerdanya (Gérone) | 19 |
| Bois de Corçà | Corçà › Baix Empordà | 19 |
| Forêt de Viladrau (27) | Viladrau › Osona (Gérone) | 19 |
| Forêt de Cassà de la Selva (32) | Cassà de la Selva › Gironès | 19 |
| Forêt de Garrigàs (15) | Garrigàs › Alt Empordà | 19 |
| Forêt de Cornellà del Terri (25) | Cornellà del Terri › Pla de l'Estany | 19 |
| Forêt de Lladó (15) | Lladó › Alt Empordà | 19 |
| Forêt de Queralbs (29) | Queralbs › Ripollès | 19 |
| Forêt de Torroella de Montgrí (75) | Torroella de Montgrí › Baix Empordà | 19 |
| Forêt de Fontanals de Cerdanya (51) | Fontanals de Cerdanya › Cerdanya (Gérone) | 19 |
| Forêt de Gombrèn (11) | Gombrèn › Ripollès | 19 |
| Forêt de Montagut i Oix (20) | Montagut i Oix › Garrotxa | 19 |
| Forêt de Montagut i Oix (44) | Montagut i Oix › Garrotxa | 19 |
| Forêt de Molló (14) | Molló › Ripollès | 19 |
| Forêt de Molló (25) | Molló › Ripollès | 19 |
| Forêt de Planoles (6) | Planoles › Ripollès | 19 |
| Forêt de Sant Feliu de Guíxols (35) | Sant Feliu de Guíxols › Baix Empordà | 19 |
| Forêt de Viladrau (61) | Viladrau › Osona (Gérone) | 19 |
| Forêt de Queralbs (48) | Queralbs › Ripollès | 19 |
| Forêt de les Llosses (14) | les Llosses › Ripollès | 18 |
| Forêt de Terrades | Terrades › Alt Empordà | 18 |
| Forêt de Pardines | Pardines › Ripollès | 18 |
| Forêt de Viladrau (10) | Viladrau › Osona (Gérone) | 18 |
| Forêt de Pardines (5) | Pardines › Ripollès | 18 |
| Forêt de Borrassà (2) | Borrassà › Alt Empordà | 18 |
| Forêt de Viladrau (15) | Viladrau › Osona (Gérone) | 18 |
| Forêt de Argelaguer | Argelaguer › Garrotxa | 18 |
| Forêt de Massanes (4) | Massanes › la Selva (Gérone) | 18 |
| Forêt de Corçà (11) | Corçà › Baix Empordà | 18 |
| Forêt de Riudarenes (8) | Riudarenes › la Selva (Gérone) | 18 |
| Forêt de Vallfogona de Ripollès (6) | Vallfogona de Ripollès › Ripollès | 18 |
| Forêt de Saus, Camallera i Llampaies (5) | Saus, Camallera i Llampaies › Alt Empordà | 18 |
| Forêt de Llambilles (9) | Llambilles › Gironès | 18 |
| Forêt de Caldes de Malavella (29) | Caldes de Malavella › la Selva (Gérone) | 18 |
| Forêt de Navata (6) | Navata › Alt Empordà | 18 |
| Forêt de Serinyà (4) | Serinyà › Pla de l'Estany | 18 |
| Forêt de Ribes de Freser (6) | Ribes de Freser › Ripollès | 18 |
| Forêt de Toses (15) | Toses › Ripollès | 18 |
| Bois de Vilopriu (3) | Vilopriu › Baix Empordà | 18 |
| Forêt de Mont-ras (14) | Mont-ras › Baix Empordà | 18 |
| Forêt de Fontanals de Cerdanya (25) | Fontanals de Cerdanya › Cerdanya (Gérone) | 18 |
| Forêt de Gombrèn (14) | Gombrèn › Ripollès | 18 |
| Forêt de Maçanet de Cabrenys (25) | Maçanet de Cabrenys › Alt Empordà | 18 |
| Forêt de Viladasens (9) | Viladasens › Gironès | 18 |
| Forêt de Massanes (22) | Massanes › la Selva (Gérone) | 18 |
| Forêt de Sant Ferriol (16) | Maià de Montcal › Garrotxa | 18 |
| Forêt de Santa Pau (2) | Santa Pau › Garrotxa | 17 |
| Forêt de Sant Joan de les Abadesses (2) | Sant Joan de les Abadesses › Ripollès | 17 |
| Forêt de Flaçà | Flaçà › Gironès | 17 |
| Forêt de Vallfogona de Ripollès | Vallfogona de Ripollès › Ripollès | 17 |
| Forêt de Riudarenes | Riudarenes › la Selva (Gérone) | 17 |
| Forêt de les Llosses (25) | les Llosses › Ripollès | 17 |
| Forêt de Ripoll (2) | Ripoll › Ripollès | 17 |
| Forêt de Aiguaviva (13) | Aiguaviva › Gironès | 17 |
| Forêt de Avinyonet de Puigventós (7) | Avinyonet de Puigventós › Alt Empordà | 17 |
| Forêt de Viladrau (25) | Viladrau › Osona (Gérone) | 17 |
| Forêt de Sant Hilari Sacalm (22) | Sant Hilari Sacalm › la Selva (Gérone) | 17 |
| Forêt de Crespià (4) | Crespià › Pla de l'Estany | 17 |
| Forêt de Sant Ferriol (7) | Sant Ferriol › Garrotxa | 17 |
| Forêt de el Port de la Selva (24) | el Port de la Selva › Alt Empordà | 17 |
| Forêt de Ribes de Freser (11) | Ribes de Freser › Ripollès | 17 |
| Forêt de Lloret de Mar (46) | Lloret de Mar › la Selva (Gérone) | 17 |
| Forêt de Toses (11) | Toses › Ripollès | 17 |
| Forêt de Alp (100) | Alp › Cerdanya (Gérone) | 17 |
| Forêt de Gombrèn (31) | Gombrèn › Ripollès | 17 |
| Forêt de Campdevànol (38) | Campdevànol › Ripollès | 17 |
| Forêt de la Vall d'en Bas (21) | la Vall d'en Bas › Garrotxa | 17 |
| Forêt de Albanyà (12) | Albanyà › Alt Empordà | 17 |
| Forêt de Albanyà (20) | Albanyà › Alt Empordà | 17 |
| Forêt de Darnius (9) | Darnius › Alt Empordà | 17 |
| Forêt de Camprodon (36) | Camprodon › Ripollès | 17 |
| Forêt de Setcases (90) | Setcases › Ripollès | 17 |
| Forêt de la Vall d'en Bas (71) | la Vall d'en Bas › Garrotxa | 17 |
| Forêt de Sant Miquel de Campmajor | Sant Miquel de Campmajor › Pla de l'Estany | 16 |
| Forêt de Verges | Verges › Baix Empordà | 16 |
| Forêt de les Llosses (27) | les Llosses › Ripollès | 16 |
| Forêt de Castell d'Aro, Platja d'Aro i s'Agaró (27) | Castell d'Aro, Platja d'Aro i s'Agaró › Baix Empordà | 16 |
| Forêt de Tossa de Mar (24) | Tossa de Mar › la Selva (Gérone) | 16 |
| Forêt de Blanes (15) | Blanes › la Selva (Gérone) | 16 |
| Forêt de Ripoll (34) | Ripoll › Ripollès | 16 |
| Forêt de Lloret de Mar (43) | Lloret de Mar › la Selva (Gérone) | 16 |
| Forêt de Viladrau (35) | Viladrau › Osona (Gérone) | 16 |
| Forêt de Fontanals de Cerdanya (48) | Fontanals de Cerdanya › Cerdanya (Gérone) | 16 |
| Forêt de Campdevànol (15) | Campdevànol › Ripollès | 16 |
| Forêt de Gombrèn (34) | Gombrèn › Ripollès | 16 |
| Forêt de les Llosses (101) | les Llosses › Ripollès | 16 |
| Forêt de Camprodon (21) | Camprodon › Ripollès | 16 |
| Forêt de la Vajol (53) | la Vajol › Alt Empordà | 16 |
| Forêt de la Jonquera (21) | la Jonquera › Alt Empordà | 16 |
| Forêt de Espolla (6) | Espolla › Alt Empordà | 16 |
| Forêt de Rabós (7) | Rabós › Alt Empordà | 16 |
| Forêt de Molló (23) | Molló › Ripollès | 16 |
| Forêt de Molló (40) | Molló › Ripollès | 16 |
| Forêt de Camprodon (40) | Camprodon › Ripollès | 16 |
| Forêt de Ribes de Freser (41) | Ribes de Freser › Ripollès | 16 |
| Forêt de la Vall de Bianya (15) | la Vall de Bianya › Garrotxa | 16 |
| Forêt de Santa Coloma de Farners (31) | Arbúcies › la Selva (Gérone) | 16 |
| Forêt de Espinelves (10) | Espinelves › Osona (Gérone) | 16 |
| Forêt de Osor (25) | Osor › la Selva (Gérone) | 16 |
| Forêt de les Llosses (125) | les Llosses › Ripollès | 16 |
| Forêt de les Llosses (127) | les Llosses › Ripollès | 16 |
| Forêt de Sant Joan de les Abadesses (39) | Sant Joan de les Abadesses › Ripollès | 16 |
| Forêt de Viladrau (54) | Viladrau › Osona (Gérone) | 16 |
| Forêt de Vallfogona de Ripollès (2) | Vallfogona de Ripollès › Ripollès | 15 |
| Forêt de les Llosses (23) | les Llosses › Ripollès | 15 |
| Forêt de Terrades (2) | Terrades › Alt Empordà | 15 |
| Forêt de Llagostera (35) | Llagostera › Gironès | 15 |
| Forêt de Sant Gregori (21) | Sant Gregori › Gironès | 15 |
| Forêt de Llívia (13) | Llívia › Cerdanya (Gérone) | 15 |
| Forêt de Mont-ras (13) | Mont-ras › Baix Empordà | 15 |
| Forêt de Salt (2) | Salt › Gironès | 15 |
| Forêt de Colomers (2) | Colomers › Baix Empordà | 15 |
| Forêt de Begur (28) | Begur › Baix Empordà | 15 |
| Forêt de Torroella de Montgrí (65) | Torroella de Montgrí › Baix Empordà | 15 |
| Forêt de Ribes de Freser (23) | Ribes de Freser › Ripollès | 15 |
| Bois de Isòvol | Isòvol › Cerdanya (Gérone) | 15 |
| Forêt de Riudarenes (14) | Riudarenes › la Selva (Gérone) | 15 |
| Forêt de Maçanet de Cabrenys (4) | Maçanet de Cabrenys › Alt Empordà | 15 |
| Bois de Ger | Ger › Cerdanya (Gérone) | 15 |
| Forêt de Campdevànol (16) | Campdevànol › Ripollès | 15 |
| Forêt de Ripoll (44) | Ripoll › Ripollès | 15 |
| Forêt de Ribes de Freser (30) | Ribes de Freser › Ripollès | 15 |
| Forêt de Ripoll (67) | Ripoll › Ripollès | 15 |
| Forêt de Montagut i Oix (19) | Montagut i Oix › Garrotxa | 15 |
| Forêt de Rabós (10) | Rabós › Alt Empordà | 15 |
| Forêt de Camprodon (27) | Camprodon › Ripollès | 15 |
| Forêt de Setcases (78) | Setcases › Ripollès | 15 |
| Forêt de Molló (71) | Molló › Ripollès | 15 |
| Forêt de Vilallonga de Ter (13) | Vilallonga de Ter › Ripollès | 15 |
| Forêt de Meranges (11) | Meranges › Cerdanya (Gérone) | 15 |
| Forêt de Meranges (23) | Meranges › Cerdanya (Gérone) | 15 |
| Forêt de la Vall de Bianya (12) | la Vall de Bianya › Garrotxa | 15 |
| Forêt de la Vall de Bianya (22) | la Vall de Bianya › Garrotxa | 15 |
| Forêt de Arbúcies (22) | Arbúcies › la Selva (Gérone) | 15 |
| Forêt de Arbúcies (28) | Arbúcies › la Selva (Gérone) | 15 |
| Forêt de Osor (27) | Osor › la Selva (Gérone) | 15 |
| Forêt de Sant Hilari Sacalm (38) | Sant Hilari Sacalm › la Selva (Gérone) | 15 |
| Forêt de Sant Mori | Sant Mori › Alt Empordà | 15 |
| la Devesa | Girona › Gironès | 14 |
| Bois de Maçanet de Cabrenys | Maçanet de Cabrenys › Alt Empordà | 14 |
| Forêt de Maçanet de la Selva (5) | Maçanet de la Selva › la Selva (Gérone) | 14 |
| Forêt de Foixà | Foixà › Baix Empordà | 14 |
| Forêt de Sant Joan de les Abadesses (3) | Sant Joan de les Abadesses › Ripollès | 14 |
| Forêt de Ribes de Freser | Ribes de Freser › Ripollès | 14 |
| Forêt de Maià de Montcal | Maià de Montcal › Garrotxa | 14 |
| Forêt de les Llosses (21) | les Llosses › Ripollès | 14 |
| Forêt de Sant Llorenç de la Muga | Sant Llorenç de la Muga › Alt Empordà | 14 |
| Forêt de Flaçà (2) | Flaçà › Gironès | 14 |
| Forêt de Foixà (3) | Foixà › Baix Empordà | 14 |
| Forêt de les Llosses (29) | les Llosses › Ripollès | 14 |
| Forêt de la Vajol (22) | la Vajol › Alt Empordà | 14 |
| Forêt de Cornellà del Terri (11) | Cornellà del Terri › Pla de l'Estany | 14 |
| Forêt de Olot (5) | Olot › Garrotxa | 14 |
| Forêt de Llívia (10) | Llívia › Cerdanya (Gérone) | 14 |
| Forêt de Brunyola i Sant Martí Sapresa (8) | Brunyola i Sant Martí Sapresa › la Selva (Gérone) | 14 |
| Forêt de Riudellots de la Selva (19) | Riudellots de la Selva › la Selva (Gérone) | 14 |
| Forêt de Aiguaviva (31) | Aiguaviva › Gironès | 14 |
| Forêt de Brunyola i Sant Martí Sapresa (11) | Brunyola i Sant Martí Sapresa › la Selva (Gérone) | 14 |
| Forêt de Serinyà (3) | Serinyà › Pla de l'Estany | 14 |
| Forêt de Vilopriu (4) | Vilopriu › Baix Empordà | 14 |
| Forêt de Pals (9) | Pals › Baix Empordà | 14 |
| Forêt de Ger (9) | Ger › Cerdanya (Gérone) | 14 |
| Forêt de Toses (13) | Toses › Ripollès | 14 |
| Forêt de Pardines (12) | Pardines › Ripollès | 14 |
| Forêt de Ribes de Freser (22) | Ribes de Freser › Ripollès | 14 |
| Forêt de Pals (13) | Pals › Baix Empordà | 14 |
| Forêt de Pals (17) | Pals › Baix Empordà | 14 |
| Bois de Maià de Montcal | Maià de Montcal › Garrotxa | 14 |
| Forêt de Queralbs (35) | Queralbs › Ripollès | 14 |
| Forêt de Das (25) | Das › Cerdanya (Gérone) | 14 |
| Forêt de Gombrèn (37) | Gombrèn › Ripollès | 14 |
| Forêt de Campdevànol (24) | Campdevànol › Ripollès | 14 |
| Forêt de Gombrèn (56) | Gombrèn › Ripollès | 14 |
| Forêt de Campdevànol (41) | Campdevànol › Ripollès | 14 |
| Forêt de Gombrèn (65) | Gombrèn › Ripollès | 14 |
| Forêt de Sales de Llierca | Sales de Llierca › Garrotxa | 14 |
| Forêt de Sales de Llierca (6) | Sales de Llierca › Garrotxa | 14 |
| Forêt de Camprodon (22) | Camprodon › Ripollès | 14 |
| Forêt de Maçanet de Cabrenys (9) | Maçanet de Cabrenys › Alt Empordà | 14 |
| Forêt de Maçanet de Cabrenys (10) | Maçanet de Cabrenys › Alt Empordà | 14 |
| Forêt de Molló (77) | Molló › Ripollès | 14 |
| Forêt de Toses (50) | Toses › Ripollès | 14 |
| Forêt de les Llosses (131) | les Llosses › Ripollès | 14 |
| Forêt de Camprodon (65) | Camprodon › Ripollès | 14 |
| Forêt de Viladrau (62) | Viladrau › Osona (Gérone) | 14 |
| Forêt de Crespià (5) | Cabanelles › Alt Empordà | 14 |
| Forêt de Navata (9) | Navata › Alt Empordà | 14 |
| Forêt de Vilademuls | Vilademuls › Pla de l'Estany | 13 |
| Forêt de Ogassa (3) | Ogassa › Ripollès | 13 |
| Forêt de Vallfogona de Ripollès (4) | Vallfogona de Ripollès › Ripollès | 13 |
| Forêt de Sant Joan de les Abadesses (7) | Sant Joan de les Abadesses › Ripollès | 13 |
| Forêt de Canet d'Adri | Canet d'Adri › Gironès | 13 |
| Forêt de Llers (6) | Llers › Alt Empordà | 13 |
| Forêt de Caldes de Malavella (16) | Caldes de Malavella › la Selva (Gérone) | 13 |
| Bois de Ullastret | Ullastret › Baix Empordà | 13 |
| Forêt de Ullastret (4) | Ullastret › Baix Empordà | 13 |
| Forêt de Viladasens (5) | Viladasens › Gironès | 13 |
| Forêt de Vilamalla (2) | Vilamalla › Alt Empordà | 13 |
| Bois de Cornellà del Terri (8) | Cornellà del Terri › Pla de l'Estany | 13 |
| Forêt de Torroella de Montgrí (63) | Torroella de Montgrí › Baix Empordà | 13 |
| Forêt de la Jonquera (13) | la Jonquera › Alt Empordà | 13 |
| Forêt de Castell d'Aro, Platja d'Aro i s'Agaró (24) | Castell d'Aro, Platja d'Aro i s'Agaró › Baix Empordà | 13 |
| Forêt de Torroella de Montgrí (69) | Torroella de Montgrí › Baix Empordà | 13 |
| Forêt de Ripoll (12) | Ripoll › Ripollès | 13 |
| Bois de Vilallonga de Ter (5) | Vilallonga de Ter › Ripollès | 13 |
| Forêt de Fontanals de Cerdanya (24) | Fontanals de Cerdanya › Cerdanya (Gérone) | 13 |
| Forêt de Urús (9) | Urús › Cerdanya (Gérone) | 13 |
| Forêt de Gombrèn (15) | Gombrèn › Ripollès | 13 |
| Forêt de Gombrèn (21) | Gombrèn › Ripollès | 13 |
| Forêt de Gombrèn (35) | Gombrèn › Ripollès | 13 |
| Forêt de Gombrèn (53) | Gombrèn › Ripollès | 13 |
| Forêt de Campdevànol (48) | Campdevànol › Ripollès | 13 |
| Forêt de Ribes de Freser (32) | Ribes de Freser › Ripollès | 13 |
| Forêt de Albanyà (23) | Albanyà › Alt Empordà | 13 |
| Forêt de Molló (28) | Molló › Ripollès | 13 |
| Forêt de Molló (47) | Molló › Ripollès | 13 |
| Forêt de Molló (58) | Molló › Ripollès | 13 |
| Forêt de Vilallonga de Ter (17) | Vilallonga de Ter › Ripollès | 13 |
| Forêt de Llanars (17) | Llanars › Ripollès | 13 |
| Forêt de les Llosses (123) | les Llosses › Ripollès | 13 |
| Forêt de les Llosses (137) | les Llosses › Ripollès | 13 |
| Forêt de Vilopriu | Vilopriu › Baix Empordà | 12 |
| Forêt de Campllong | Campllong › Gironès | 12 |
| Forêt de Viladasens | Viladasens › Gironès | 12 |
| Bois de Santa Cristina d'Aro | Santa Cristina d'Aro › Baix Empordà | 12 |
| Forêt de Olot (8) | Olot › Garrotxa | 12 |
| Forêt de Sant Feliu de Guíxols (20) | Sant Feliu de Guíxols › Baix Empordà | 12 |
| Forêt de Sils (14) | Sils › la Selva (Gérone) | 12 |
| Forêt de Saus, Camallera i Llampaies (6) | Saus, Camallera i Llampaies › Alt Empordà | 12 |
| Forêt de Viladrau (32) | Viladrau › Osona (Gérone) | 12 |
| Bois de Olot (20) | Olot › Garrotxa | 12 |
| Forêt de Alp (90) | Alp › Cerdanya (Gérone) | 12 |
| Forêt de Vilademuls (18) | Vilademuls › Pla de l'Estany | 12 |
| Forêt de Queralbs (28) | Queralbs › Ripollès | 12 |
| Forêt de Maçanet de la Selva (16) | Maçanet de la Selva › la Selva (Gérone) | 12 |
| Forêt de Palamós (15) | Palamós › Baix Empordà | 12 |
| Forêt de Besalú (9) | Besalú › Garrotxa | 12 |
| Forêt de Ribes de Freser (14) | Ribes de Freser › Ripollès | 12 |
| Forêt de Gualta | Gualta › Baix Empordà | 12 |
| Forêt de Viladrau (42) | Viladrau › Osona (Gérone) | 12 |
| Forêt de Sant Joan de les Abadesses (10) | Sant Joan de les Abadesses › Ripollès | 12 |
| Forêt de Gombrèn (20) | Gombrèn › Ripollès | 12 |
| Forêt de les Llosses (104) | les Llosses › Ripollès | 12 |
| Forêt de Maçanet de Cabrenys (27) | Maçanet de Cabrenys › Alt Empordà | 12 |
| Forêt de Molló (19) | Molló › Ripollès | 12 |
| Forêt de Molló (21) | Molló › Ripollès | 12 |
| Forêt de Molló (59) | Molló › Ripollès | 12 |
| Forêt de Setcases (77) | Setcases › Ripollès | 12 |
| Forêt de Camprodon (44) | Camprodon › Ripollès | 12 |
| Forêt de Vilallonga de Ter (8) | Vilallonga de Ter › Ripollès | 12 |
| Forêt de Santa Pau (18) | Santa Pau › Garrotxa | 12 |
| Forêt de Santa Coloma de Farners (26) | Santa Coloma de Farners › la Selva (Gérone) | 12 |
| Forêt de Begur (44) | Begur › Baix Empordà | 12 |
| Forêt de Sant Joan de les Abadesses (42) | Sant Joan de les Abadesses › Ripollès | 12 |
| Forêt de Riells i Viabrea (34) | Riells i Viabrea › la Selva (Gérone) | 12 |
| Forêt de Camprodon (64) | Camprodon › Ripollès | 12 |
| Forêt de Vidreres (20) | Vidreres › la Selva (Gérone) | 12 |
| Forêt de Navata (8) | Navata › Alt Empordà | 12 |
| Forêt de les Llosses (16) | les Llosses › Ripollès | 11 |
| Forêt de les Llosses (20) | les Llosses › Ripollès | 11 |
| Forêt de Arbúcies (2) | Arbúcies › la Selva (Gérone) | 11 |
| Forêt de Palau-sator (4) | Palau-sator › Baix Empordà | 11 |
| Forêt de Vilademuls (6) | Vilademuls › Pla de l'Estany | 11 |
| Bois de Amer (2) | Amer › la Selva (Gérone) | 11 |
| Forêt de Llagostera (23) | Llagostera › Gironès | 11 |
| Bois de Garrigàs | Garrigàs › Alt Empordà | 11 |
| Forêt de Sils (29) | Sils › la Selva (Gérone) | 11 |
| Forêt de Ripoll (5) | Ripoll › Ripollès | 11 |
| Parc de Pedra Tosca | les Preses › Garrotxa | 11 |
| Forêt de Llívia (5) | Llívia › Cerdanya (Gérone) | 11 |
| Forêt de Llívia (8) | Llívia › Cerdanya (Gérone) | 11 |
| Forêt de la Tallada d'Empordà (6) | Ullà › Baix Empordà | 11 |
| Forêt de Cornellà del Terri (14) | Cornellà del Terri › Pla de l'Estany | 11 |
| Forêt de Cornellà del Terri (17) | Cornellà del Terri › Pla de l'Estany | 11 |
| Forêt de Girona (61) | Girona › Gironès | 11 |
| Forêt de Salt | Salt › Gironès | 11 |
| Forêt de Vilademuls (15) | Vilademuls › Pla de l'Estany | 11 |
| Forêt de Sant Ferriol (6) | Sant Ferriol › Garrotxa | 11 |
| Forêt de Porqueres (16) | Porqueres › Pla de l'Estany | 11 |
| Parc Natural del Montgrí | l'Escala › Alt Empordà | 11 |
| Forêt de Santa Pau (15) | Santa Pau › Garrotxa | 11 |
| Forêt de Lloret de Mar (41) | Lloret de Mar › la Selva (Gérone) | 11 |
| Forêt de les Llosses (47) | les Llosses › Ripollès | 11 |
| Forêt de les Llosses (50) | les Llosses › Ripollès | 11 |
| Forêt de les Llosses (63) | les Llosses › Ripollès | 11 |
| Forêt de Queralbs (32) | Queralbs › Ripollès | 11 |
| Forêt de Queralbs (33) | Queralbs › Ripollès | 11 |
| Forêt de Viladrau (38) | Viladrau › Osona (Gérone) | 11 |
| Forêt de Bolvir (19) | Guils de Cerdanya › Cerdanya (Gérone) | 11 |
| Forêt de les Llosses (92) | les Llosses › Ripollès | 11 |
| Forêt de Gombrèn (22) | Gombrèn › Ripollès | 11 |
| Forêt de Gombrèn (36) | Gombrèn › Ripollès | 11 |
| Forêt de les Llosses (108) | les Llosses › Ripollès | 11 |
| Forêt de Montagut i Oix (18) | Montagut i Oix › Garrotxa | 11 |
| Forêt de Montagut i Oix (45) | Montagut i Oix › Garrotxa | 11 |
| Forêt de Maçanet de Cabrenys (29) | Maçanet de Cabrenys › Alt Empordà | 11 |
| Forêt de Espolla (15) | Espolla › Alt Empordà | 11 |
| Forêt de Molló (53) | Molló › Ripollès | 11 |
| Forêt de Molló (82) | Molló › Ripollès | 11 |
| Forêt de Planoles (5) | Planoles › Ripollès | 11 |
| Forêt de Osor (29) | Osor › la Selva (Gérone) | 11 |
| Forêt de Palafrugell (129) | Palafrugell › Baix Empordà | 11 |
| Forêt de Pont de Molins (2) | Pont de Molins › Alt Empordà | 11 |
| Forêt de Urús (13) | Urús › Cerdanya (Gérone) | 11 |
| Forêt de Gombrèn (76) | Gombrèn › Ripollès | 11 |
| Forêt de Celrà (10) | Celrà › Gironès | 11 |
| Forêt de les Llosses (133) | les Llosses › Ripollès | 11 |
| Forêt de Garrigàs (17) | Garrigàs › Alt Empordà | 11 |
| Forêt de Viladrau (14) | Viladrau › Osona (Gérone) | 10 |
| Forêt de Sant Feliu de Buixalleu (8) | Sant Feliu de Buixalleu › la Selva (Gérone) | 10 |
| Forêt de Cervià de Ter (21) | Cervià de Ter › Gironès | 10 |
| Bois de Sant Jordi Desvalls (8) | Sant Jordi Desvalls › Gironès | 10 |
| Bois de Colomers | Colomers › Baix Empordà | 10 |
| Forêt de Besalú (3) | Besalú › Garrotxa | 10 |
| Forêt de Arbúcies (5) | Arbúcies › la Selva (Gérone) | 10 |
| Forêt de Vilopriu (2) | Vilopriu › Baix Empordà | 10 |
| Forêt de Jafre (6) | Jafre › Baix Empordà | 10 |
| Forêt de Campllong (19) | Campllong › Gironès | 10 |
| Forêt de Begur (24) | Begur › Baix Empordà | 10 |
| Forêt de Lloret de Mar (26) | Lloret de Mar › la Selva (Gérone) | 10 |
| Forêt de Roses (13) | Roses › Alt Empordà | 10 |
| Forêt de Ripoll (29) | Ripoll › Ripollès | 10 |
| Forêt de Lloret de Mar (42) | Lloret de Mar › la Selva (Gérone) | 10 |
| Forêt de Toses (8) | Toses › Ripollès | 10 |
| Forêt de les Llosses (66) | les Llosses › Ripollès | 10 |
| Forêt de Fontanals de Cerdanya (47) | Fontanals de Cerdanya › Cerdanya (Gérone) | 10 |
| Forêt de Gombrèn (32) | Gombrèn › Ripollès | 10 |
| Forêt de Gombrèn (57) | Gombrèn › Ripollès | 10 |
| Forêt de Ribes de Freser (33) | Ribes de Freser › Ripollès | 10 |
| Forêt de Montagut i Oix (8) | Montagut i Oix › Garrotxa | 10 |
| Forêt de Agullana (2) | Agullana › Alt Empordà | 10 |
| Forêt de Camprodon (26) | Camprodon › Ripollès | 10 |
| Forêt de la Vajol (56) | la Vajol › Alt Empordà | 10 |
| Forêt de Maçanet de Cabrenys (31) | Maçanet de Cabrenys › Alt Empordà | 10 |
| Forêt de Rabós (13) | Rabós › Alt Empordà | 10 |
| Forêt de Molló (89) | Molló › Ripollès | 10 |
| Forêt de Toses (30) | Toses › Ripollès | 10 |
| Forêt de Toses (48) | Toses › Ripollès | 10 |
| Forêt de la Vall de Bianya (20) | la Vall de Bianya › Garrotxa | 10 |
| Forêt de Arbúcies (24) | Arbúcies › la Selva (Gérone) | 10 |
| Forêt de Vilamaniscle (2) | Vilamaniscle › Alt Empordà | 10 |
| Forêt de Gombrèn (70) | Gombrèn › Ripollès | 10 |
| Forêt de Susqueda (13) | Susqueda › la Selva (Gérone) | 10 |
| Forêt de les Llosses (135) | les Llosses › Ripollès | 10 |
| Forêt de Hostalric (6) | Hostalric › la Selva (Gérone) | 10 |
| Forêt de Breda (2) | Breda › la Selva (Gérone) | 10 |
| Forêt de Camprodon (62) | Camprodon › Ripollès | 10 |
| Forêt de Arbúcies (39) | Arbúcies › la Selva (Gérone) | 10 |
| Forêt de Pontós (5) | Pontós › Alt Empordà | 10 |
| Forêt de Vilopriu (6) | Vilopriu › Baix Empordà | 10 |
| Forêt de Castell d'Aro, Platja d'Aro i s'Agaró ⚠️ | Castell d'Aro, Platja d'Aro i s'Agaró › Baix Empordà | 9 |
| Forêt de Tossa de Mar ⚠️ | Tossa de Mar › la Selva (Gérone) | 9 |
| Forêt de Arbúcies ⚠️ | Arbúcies › la Selva (Gérone) | 9 |
| Forêt de Bàscara ⚠️ | Bàscara › Alt Empordà | 9 |
| Forêt de Castelló d'Empúries ⚠️ | Castelló d'Empúries › Alt Empordà | 9 |
| Forêt de Cruïlles, Monells i Sant Sadurní de l'Heura (10) ⚠️ | Cruïlles, Monells i Sant Sadurní de l'Heura › Baix Empordà | 9 |
| Forêt de Corçà (5) ⚠️ | Corçà › Baix Empordà | 9 |
| Bosc de Can Terrer ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 9 |
| Forêt de Sant Feliu de Guíxols (11) ⚠️ | Sant Feliu de Guíxols › Baix Empordà | 9 |
| Forêt de Alp (25) ⚠️ | Alp › Cerdanya (Gérone) | 9 |
| Forêt de Sarrià de Ter (4) ⚠️ | Sarrià de Ter › Gironès | 9 |
| Bois de Fontcoberta ⚠️ | Fontcoberta › Pla de l'Estany | 9 |
| Forêt de Vilademuls (10) ⚠️ | Vilademuls › Pla de l'Estany | 9 |
| Forêt de la Vall de Bianya (5) ⚠️ | la Vall de Bianya › Garrotxa | 9 |
| Bois de Vilademuls (18) ⚠️ | Vilademuls › Pla de l'Estany | 9 |
| Forêt de Sils (25) ⚠️ | Sils › la Selva (Gérone) | 9 |
| Forêt de Llívia (12) ⚠️ | Llívia › Cerdanya (Gérone) | 9 |
| Forêt de Forallac (42) ⚠️ | Forallac › Baix Empordà | 9 |
| Forêt de Camós (6) ⚠️ | Camós › Pla de l'Estany | 9 |
| Forêt de Quart (11) ⚠️ | Quart › Gironès | 9 |
| Forêt de Begur (18) ⚠️ | Begur › Baix Empordà | 9 |
| Forêt de Tossa de Mar (27) ⚠️ | Tossa de Mar › la Selva (Gérone) | 9 |
| Forêt de Ger (8) ⚠️ | Ger › Cerdanya (Gérone) | 9 |
| Forêt de Toses (20) ⚠️ | Toses › Ripollès | 9 |
| Forêt de Ribes de Freser (20) ⚠️ | Ribes de Freser › Ripollès | 9 |
| Forêt de la Vall d'en Bas (15) ⚠️ | la Vall d'en Bas › Garrotxa | 9 |
| Bois de Bàscara ⚠️ | Bàscara › Alt Empordà | 9 |
| Forêt de Gombrèn (17) ⚠️ | Gombrèn › Ripollès | 9 |
| Forêt de Campdevànol (12) ⚠️ | Campdevànol › Ripollès | 9 |
| Forêt de Campdevànol (22) ⚠️ | Campdevànol › Ripollès | 9 |
| Forêt de Gombrèn (58) ⚠️ | Gombrèn › Ripollès | 9 |
| Forêt de Campdevànol (46) ⚠️ | Campdevànol › Ripollès | 9 |
| Forêt de Vallfogona de Ripollès (16) ⚠️ | Vallfogona de Ripollès › Ripollès | 9 |
| Forêt de Montagut i Oix (38) ⚠️ | Montagut i Oix › Garrotxa | 9 |
| Forêt de Argelaguer (4) ⚠️ | Argelaguer › Garrotxa | 9 |
| Forêt de Molló (22) ⚠️ | Molló › Ripollès | 9 |
| Forêt de Molló (37) ⚠️ | Molló › Ripollès | 9 |
| Forêt de Setcases (83) ⚠️ | Setcases › Ripollès | 9 |
| Forêt de Setcases (91) ⚠️ | Setcases › Ripollès | 9 |
| Forêt de Molló (83) ⚠️ | Molló › Ripollès | 9 |
| Forêt de Setcases (104) ⚠️ | Setcases › Ripollès | 9 |
| Forêt de Campelles (10) ⚠️ | Campelles › Ripollès | 9 |
| Forêt de Camprodon (52) ⚠️ | Camprodon › Ripollès | 9 |
| Forêt de Peralada (9) ⚠️ | Peralada › Alt Empordà | 9 |
| Forêt de Santa Pau (21) ⚠️ | Santa Pau › Garrotxa | 9 |
| Forêt de Forallac (44) ⚠️ | Forallac › Baix Empordà | 9 |
| Forêt de Sant Feliu de Buixalleu (30) ⚠️ | Sant Feliu de Buixalleu › la Selva (Gérone) | 9 |
| Forêt de Cabanelles (9) ⚠️ | Cabanelles › Alt Empordà | 9 |
| Forêt de Vilademuls (26) ⚠️ | Vilademuls › Pla de l'Estany | 9 |
| Forêt de Navata (7) ⚠️ | Navata › Alt Empordà | 9 |
| Forêt de Vilademuls (27) ⚠️ | Vilademuls › Pla de l'Estany | 9 |
| Forêt de Pontós (7) ⚠️ | Pontós › Alt Empordà | 9 |
| Forêt de Montagut i Oix (84) ⚠️ | Montagut i Oix › Garrotxa | 9 |
| Forêt de Torroella de Fluvià (18) ⚠️ | Torroella de Fluvià › Alt Empordà | 9 |
| Forêt de Begur (45) ⚠️ | Begur › Baix Empordà | 9 |
| Forêt de Avinyonet de Puigventós (3) ⚠️ | Avinyonet de Puigventós › Alt Empordà | 8 |
| Forêt de Aiguaviva (16) ⚠️ | Aiguaviva › Gironès | 8 |
| Forêt de Llagostera (30) ⚠️ | Llagostera › Gironès | 8 |
| Forêt de Palafrugell (18) ⚠️ | Palafrugell › Baix Empordà | 8 |
| Forêt de Riudellots de la Selva (16) ⚠️ | Riudellots de la Selva › la Selva (Gérone) | 8 |
| Forêt de Girona (11) ⚠️ | Girona › Gironès | 8 |
| Forêt de la Vajol (37) ⚠️ | la Vajol › Alt Empordà | 8 |
| Forêt de Sils (6) ⚠️ | Sils › la Selva (Gérone) | 8 |
| Forêt de Vilademuls (9) ⚠️ | Vilademuls › Pla de l'Estany | 8 |
| Bois de Sant Jordi Desvalls (12) ⚠️ | Sant Jordi Desvalls › Gironès | 8 |
| Forêt de Cassà de la Selva (31) ⚠️ | Cassà de la Selva › Gironès | 8 |
| Bois de Sant Gregori (2) ⚠️ | Sant Gregori › Gironès | 8 |
| Forêt de Aiguaviva (24) ⚠️ | Aiguaviva › Gironès | 8 |
| Forêt de Foixà (8) ⚠️ | Foixà › Baix Empordà | 8 |
| Forêt de Sant Feliu de Buixalleu (18) ⚠️ | Sant Feliu de Buixalleu › la Selva (Gérone) | 8 |
| Forêt de Sant Julià de Ramis (10) ⚠️ | Sant Julià de Ramis › Gironès | 8 |
| Bois de Sant Julià del Llor i Bonmatí (4) ⚠️ | Sant Julià del Llor i Bonmatí › la Selva (Gérone) | 8 |
| Forêt de Girona (71) ⚠️ | Girona › Gironès | 8 |
| Forêt de Aiguaviva (32) ⚠️ | Aiguaviva › Gironès | 8 |
| Forêt de Palafrugell (122) ⚠️ | Palafrugell › Baix Empordà | 8 |
| Forêt de Begur (35) ⚠️ | Begur › Baix Empordà | 8 |
| Forêt de Palafrugell (125) ⚠️ | Palafrugell › Baix Empordà | 8 |
| Forêt de Sant Feliu de Guíxols (29) ⚠️ | Sant Feliu de Guíxols › Baix Empordà | 8 |
| Forêt de Lloret de Mar (38) ⚠️ | Lloret de Mar › la Selva (Gérone) | 8 |
| Forêt de el Port de la Selva (25) ⚠️ | el Port de la Selva › Alt Empordà | 8 |
| Forêt de Setcases (49) ⚠️ | Setcases › Ripollès | 8 |
| Forêt de Ripoll (36) ⚠️ | Ripoll › Ripollès | 8 |
| Forêt de Alp (94) ⚠️ | Alp › Cerdanya (Gérone) | 8 |
| Forêt de Bolvir (4) ⚠️ | Bolvir › Cerdanya (Gérone) | 8 |
| Forêt de Fontanilles (4) ⚠️ | Fontanilles › Baix Empordà | 8 |
| Forêt de les Llosses (68) ⚠️ | les Llosses › Ripollès | 8 |
| Bois de la Vall d'en Bas (2) ⚠️ | la Vall d'en Bas › Garrotxa | 8 |
| Forêt de Pals (67) ⚠️ | Pals › Baix Empordà | 8 |
| Forêt de Campdevànol (20) ⚠️ | Campdevànol › Ripollès | 8 |
| Forêt de les Llosses (107) ⚠️ | les Llosses › Ripollès | 8 |
| Forêt de Montagut i Oix (12) ⚠️ | Montagut i Oix › Garrotxa | 8 |
| Forêt de Molló (26) ⚠️ | Molló › Ripollès | 8 |
| Forêt de Molló (64) ⚠️ | Molló › Ripollès | 8 |
| Forêt de Molló (66) ⚠️ | Molló › Ripollès | 8 |
| Forêt de Molló (69) ⚠️ | Molló › Ripollès | 8 |
| Forêt de Llanars (12) ⚠️ | Llanars › Ripollès | 8 |
| Forêt de Toses (44) ⚠️ | Toses › Ripollès | 8 |
| Forêt de Osor (21) ⚠️ | Osor › la Selva (Gérone) | 8 |
| Forêt de la Selva de Mar (2) ⚠️ | la Selva de Mar › Alt Empordà | 8 |
| Forêt de la Selva de Mar (5) ⚠️ | la Selva de Mar › Alt Empordà | 8 |
| Forêt de Brunyola i Sant Martí Sapresa (13) ⚠️ | Brunyola i Sant Martí Sapresa › la Selva (Gérone) | 8 |
| Forêt de Sant Hilari Sacalm (37) ⚠️ | Sant Hilari Sacalm › la Selva (Gérone) | 8 |
| Forêt de Hostalric (8) ⚠️ | Hostalric › la Selva (Gérone) | 8 |
| Forêt de Riells i Viabrea (26) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 8 |
| Forêt de Riudaura (3) ⚠️ | Riudaura › Garrotxa | 8 |
| Forêt de Cabanelles (15) ⚠️ | Cabanelles › Alt Empordà | 8 |
| Forêt de Pontós (8) ⚠️ | Pontós › Alt Empordà | 8 |
| Forêt de Sant Ferriol (18) ⚠️ | Sant Ferriol › Garrotxa | 8 |
| Forêt de Ripoll (94) ⚠️ | Ripoll › Ripollès | 8 |
| Forêt de Sant Hilari Sacalm (8) ⚠️ | Sant Hilari Sacalm › la Selva (Gérone) | 7 |
| Forêt de Sant Feliu de Buixalleu ⚠️ | Sant Feliu de Buixalleu › la Selva (Gérone) | 7 |
| Forêt de Espinelves (4) ⚠️ | Espinelves › Osona (Gérone) | 7 |
| Forêt de Corçà ⚠️ | Corçà › Baix Empordà | 7 |
| Forêt de Fornells de la Selva (4) ⚠️ | Fornells de la Selva › Gironès | 7 |
| Bosc d'en Llach ⚠️ | Garrigàs › Alt Empordà | 7 |
| Forêt de Cassà de la Selva (9) ⚠️ | Cassà de la Selva › Gironès | 7 |
| Forêt de Sant Jordi Desvalls ⚠️ | Sant Jordi Desvalls › Gironès | 7 |
| Forêt de la Vajol (38) ⚠️ | la Vajol › Alt Empordà | 7 |
| Forêt de Girona (16) ⚠️ | Girona › Gironès | 7 |
| Forêt de Maià de Montcal (4) ⚠️ | Maià de Montcal › Garrotxa | 7 |
| Forêt de Alp (23) ⚠️ | Alp › Cerdanya (Gérone) | 7 |
| Forêt de Alp (24) ⚠️ | Alp › Cerdanya (Gérone) | 7 |
| Forêt de Sarrià de Ter (5) ⚠️ | Sarrià de Ter › Gironès | 7 |
| Forêt de Vilobí d'Onyar (36) ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 7 |
| Bois de la Bisbal d'Empordà (2) ⚠️ | la Bisbal d'Empordà › Baix Empordà | 7 |
| Forêt de Olot (6) ⚠️ | Olot › Garrotxa | 7 |
| Forêt de Sant Feliu de Guíxols (21) ⚠️ | Sant Feliu de Guíxols › Baix Empordà | 7 |
| Bois de Girona (12) ⚠️ | Girona › Gironès | 7 |
| Bois de Vilademuls (17) ⚠️ | Vilademuls › Pla de l'Estany | 7 |
| Bois de Ullastret (4) ⚠️ | la Bisbal d'Empordà › Baix Empordà | 7 |
| Forêt de Vilademuls (11) ⚠️ | Vilademuls › Pla de l'Estany | 7 |
| Forêt de la Vall d'en Bas (11) ⚠️ | la Vall d'en Bas › Garrotxa | 7 |
| Forêt de Riudarenes (12) ⚠️ | Riudarenes › la Selva (Gérone) | 7 |
| Forêt de Sant Gregori (24) ⚠️ | Sant Gregori › Gironès | 7 |
| Bois de Banyoles ⚠️ | Banyoles › Pla de l'Estany | 7 |
| Forêt de la Cellera de Ter (31) ⚠️ | la Cellera de Ter › la Selva (Gérone) | 7 |
| Forêt de Blanes (12) ⚠️ | Blanes › la Selva (Gérone) | 7 |
| Forêt de Besalú (6) ⚠️ | Besalú › Garrotxa | 7 |
| Forêt de Camprodon (17) ⚠️ | Camprodon › Ripollès | 7 |
| Forêt de Sant Joan les Fonts (12) ⚠️ | Sant Joan les Fonts › Garrotxa | 7 |
| Forêt de Cornellà del Terri (26) ⚠️ | Cornellà del Terri › Pla de l'Estany | 7 |
| Forêt de Calonge i Sant Antoni (36) ⚠️ | Calonge i Sant Antoni › Baix Empordà | 7 |
| Forêt de les Llosses (49) ⚠️ | les Llosses › Ripollès | 7 |
| Bois de Regencós (2) ⚠️ | Regencós › Baix Empordà | 7 |
| Bois de Ripoll ⚠️ | Ripoll › Ripollès | 7 |
| Forêt de les Llosses (80) ⚠️ | les Llosses › Ripollès | 7 |
| Forêt de Sant Feliu de Pallerols (8) ⚠️ | Sant Feliu de Pallerols › Garrotxa | 7 |
| Forêt de les Planes d'Hostoles (12) ⚠️ | les Planes d'Hostoles › Garrotxa | 7 |
| Forêt de Queralbs (34) ⚠️ | Queralbs › Ripollès | 7 |
| Forêt de Palafrugell (127) ⚠️ | Palafrugell › Baix Empordà | 7 |
| Forêt de Viladrau (46) ⚠️ | Viladrau › Osona (Gérone) | 7 |
| Forêt de Fontanals de Cerdanya (50) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 7 |
| Forêt de Puigcerdà (121) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 7 |
| Forêt de Urús (7) ⚠️ | Urús › Cerdanya (Gérone) | 7 |
| Forêt de Gombrèn (19) ⚠️ | Gombrèn › Ripollès | 7 |
| Forêt de Campdevànol (9) ⚠️ | Campdevànol › Ripollès | 7 |
| Forêt de Gombrèn (41) ⚠️ | Gombrèn › Ripollès | 7 |
| Forêt de Gombrèn (52) ⚠️ | Gombrèn › Ripollès | 7 |
| Forêt de Campdevànol (47) ⚠️ | Campdevànol › Ripollès | 7 |
| Forêt de Campdevànol (60) ⚠️ | Campdevànol › Ripollès | 7 |
| Forêt de Ogassa (12) ⚠️ | Ogassa › Ripollès | 7 |
| Forêt de Montagut i Oix (47) ⚠️ | Montagut i Oix › Garrotxa | 7 |
| Forêt de Montagut i Oix (64) ⚠️ | Montagut i Oix › Garrotxa | 7 |
| Forêt de Montagut i Oix (70) ⚠️ | Montagut i Oix › Garrotxa | 7 |
| Forêt de Montagut i Oix (73) ⚠️ | Montagut i Oix › Garrotxa | 7 |
| Forêt de Argelaguer (5) ⚠️ | Argelaguer › Garrotxa | 7 |
| Forêt de Sant Llorenç de la Muga (22) ⚠️ | Sant Llorenç de la Muga › Alt Empordà | 7 |
| Forêt de Rabós (3) ⚠️ | Rabós › Alt Empordà | 7 |
| Forêt de Molló (54) ⚠️ | Molló › Ripollès | 7 |
| Forêt de Planoles (7) ⚠️ | Planoles › Ripollès | 7 |
| Forêt de Planoles (16) ⚠️ | Planoles › Ripollès | 7 |
| Forêt de Campelles (13) ⚠️ | Campelles › Ripollès | 7 |
| Forêt de Ribes de Freser (42) ⚠️ | Ribes de Freser › Ripollès | 7 |
| Forêt de Meranges (7) ⚠️ | Meranges › Cerdanya (Gérone) | 7 |
| Forêt de Ger (22) ⚠️ | Ger › Cerdanya (Gérone) | 7 |
| Forêt de Meranges (27) ⚠️ | Meranges › Cerdanya (Gérone) | 7 |
| Forêt de Ripoll (79) ⚠️ | Ripoll › Ripollès | 7 |
| Forêt de Santa Coloma de Farners (25) ⚠️ | Santa Coloma de Farners › la Selva (Gérone) | 7 |
| Forêt de la Selva de Mar (8) ⚠️ | la Selva de Mar › Alt Empordà | 7 |
| Forêt de Cabanes (9) ⚠️ | Cabanes › Alt Empordà | 7 |
| Forêt de Peralada (17) ⚠️ | Castelló d'Empúries › Alt Empordà | 7 |
| Forêt de Urús (17) ⚠️ | Urús › Cerdanya (Gérone) | 7 |
| Forêt de Girona (75) ⚠️ | Girona › Gironès | 7 |
| Forêt de Queralbs (40) ⚠️ | Queralbs › Ripollès | 7 |
| Forêt de Susqueda (7) ⚠️ | Susqueda › la Selva (Gérone) | 7 |
| Forêt de Susqueda (11) ⚠️ | Susqueda › la Selva (Gérone) | 7 |
| Bois de Sant Jordi Desvalls (15) ⚠️ | Sant Jordi Desvalls › Gironès | 7 |
| Bois de la Bisbal d'Empordà (4) ⚠️ | la Bisbal d'Empordà › Baix Empordà | 7 |
| Forêt de la Vall de Bianya (36) ⚠️ | la Vall de Bianya › Garrotxa | 7 |
| Forêt de Tossa de Mar (42) ⚠️ | Tossa de Mar › la Selva (Gérone) | 7 |
| Forêt de Viladrau (64) ⚠️ | Viladrau › Osona (Gérone) | 7 |
| Forêt de Ribes de Freser (46) ⚠️ | Ribes de Freser › Ripollès | 7 |
| Forêt de Queralbs (47) ⚠️ | Queralbs › Ripollès | 7 |
| Forêt de Cabanelles (10) ⚠️ | Cabanelles › Alt Empordà | 7 |
| Forêt de la Jonquera (2) ⚠️ | la Jonquera › Alt Empordà | 6 |
| Forêt de Sant Hilari Sacalm (9) ⚠️ | Sant Hilari Sacalm › la Selva (Gérone) | 6 |
| Forêt de Cruïlles, Monells i Sant Sadurní de l'Heura (2) ⚠️ | Cruïlles, Monells i Sant Sadurní de l'Heura › Baix Empordà | 6 |
| Forêt de Palau-sator (3) ⚠️ | Palau-sator › Baix Empordà | 6 |
| Forêt de Lloret de Mar ⚠️ | Lloret de Mar › la Selva (Gérone) | 6 |
| Bois de Llers (7) ⚠️ | Llers › Alt Empordà | 6 |
| Forêt de Setcases (18) ⚠️ | Setcases › Ripollès | 6 |
| Forêt de Molló (5) ⚠️ | Molló › Ripollès | 6 |
| Forêt de Riudarenes (10) ⚠️ | Riudarenes › la Selva (Gérone) | 6 |
| Bois de Pardines (3) ⚠️ | Pardines › Ripollès | 6 |
| Forêt de Santa Cristina d'Aro (19) ⚠️ | Santa Cristina d'Aro › Baix Empordà | 6 |
| Parc de Girona (66) ⚠️ | Girona › Gironès | 6 |
| Forêt de Colomers ⚠️ | Colomers › Baix Empordà | 6 |
| Forêt de Sant Andreu Salou (9) ⚠️ | Sant Andreu Salou › Gironès | 6 |
| Forêt de Banyoles (7) ⚠️ | Banyoles › Pla de l'Estany | 6 |
| Forêt de Brunyola i Sant Martí Sapresa (10) ⚠️ | Brunyola i Sant Martí Sapresa › la Selva (Gérone) | 6 |
| Bois de Pontós (7) ⚠️ | Pontós › Alt Empordà | 6 |
| Forêt de Banyoles (16) ⚠️ | Banyoles › Pla de l'Estany | 6 |
| Forêt de Queralbs (24) ⚠️ | Queralbs › Ripollès | 6 |
| Forêt de Begur (22) ⚠️ | Begur › Baix Empordà | 6 |
| Forêt de Torroella de Montgrí (67) ⚠️ | Torroella de Montgrí › Baix Empordà | 6 |
| Forêt de Llançà (16) ⚠️ | Llançà › Alt Empordà | 6 |
| Forêt de Roses (25) ⚠️ | Roses › Alt Empordà | 6 |
| Forêt de Setcases (39) ⚠️ | Setcases › Ripollès | 6 |
| Forêt de Campdevànol (4) ⚠️ | Campdevànol › Ripollès | 6 |
| Forêt de Serinyà (5) ⚠️ | Serinyà › Pla de l'Estany | 6 |
| Forêt de la Vall d'en Bas (14) ⚠️ | la Vall d'en Bas › Garrotxa | 6 |
| Forêt de Torroella de Montgrí (77) ⚠️ | Torroella de Montgrí › Baix Empordà | 6 |
| Forêt de Toses (18) ⚠️ | Toses › Ripollès | 6 |
| Forêt de Guils de Cerdanya (3) ⚠️ | Guils de Cerdanya › Cerdanya (Gérone) | 6 |
| Forêt de les Llosses (61) ⚠️ | les Llosses › Ripollès | 6 |
| Forêt de Sant Feliu de Pallerols (6) ⚠️ | Sant Feliu de Pallerols › Garrotxa | 6 |
| Forêt de Riells i Viabrea (17) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 6 |
| Forêt de Urús (2) ⚠️ | Urús › Cerdanya (Gérone) | 6 |
| Forêt de Gombrèn (16) ⚠️ | Gombrèn › Ripollès | 6 |
| Forêt de Campdevànol (23) ⚠️ | Campdevànol › Ripollès | 6 |
| Forêt de les Llosses (106) ⚠️ | les Llosses › Ripollès | 6 |
| Forêt de Campdevànol (62) ⚠️ | Campdevànol › Ripollès | 6 |
| Forêt de Ribes de Freser (36) ⚠️ | Ribes de Freser › Ripollès | 6 |
| Forêt de Sales de Llierca (10) ⚠️ | Sales de Llierca › Garrotxa | 6 |
| Forêt de Montagut i Oix (43) ⚠️ | Montagut i Oix › Garrotxa | 6 |
| Forêt de Montagut i Oix (52) ⚠️ | Montagut i Oix › Garrotxa | 6 |
| Forêt de Sant Llorenç de la Muga (8) ⚠️ | Sant Llorenç de la Muga › Alt Empordà | 6 |
| Forêt de Rabós (11) ⚠️ | Rabós › Alt Empordà | 6 |
| Forêt de Espolla (14) ⚠️ | Espolla › Alt Empordà | 6 |
| Forêt de Molló (11) ⚠️ | Molló › Ripollès | 6 |
| Forêt de Setcases (66) ⚠️ | Setcases › Ripollès | 6 |
| Forêt de Setcases (72) ⚠️ | Setcases › Ripollès | 6 |
| Forêt de Setcases (95) ⚠️ | Setcases › Ripollès | 6 |
| Forêt de Molló (80) ⚠️ | Molló › Ripollès | 6 |
| Forêt de Toses (43) ⚠️ | Toses › Ripollès | 6 |
| Forêt de Camprodon (46) ⚠️ | Camprodon › Ripollès | 6 |
| Forêt de Camprodon (47) ⚠️ | Camprodon › Ripollès | 6 |
| Forêt de la Vall de Bianya (17) ⚠️ | la Vall de Bianya › Garrotxa | 6 |
| Forêt de la Vall de Bianya (18) ⚠️ | la Vall de Bianya › Garrotxa | 6 |
| Forêt de la Vall de Bianya (19) ⚠️ | la Vall de Bianya › Garrotxa | 6 |
| Forêt de Sant Joan de les Abadesses (21) ⚠️ | Sant Joan de les Abadesses › Ripollès | 6 |
| Forêt de la Vall de Bianya (25) ⚠️ | la Vall de Bianya › Garrotxa | 6 |
| Forêt de Ripoll (88) ⚠️ | Ripoll › Ripollès | 6 |
| Forêt de Vidrà (7) ⚠️ | Vidrà › Osona (Gérone) | 6 |
| Forêt de Ripoll (92) ⚠️ | Ripoll › Ripollès | 6 |
| Forêt de Montagut i Oix (81) ⚠️ | Montagut i Oix › Garrotxa | 6 |
| Forêt de Arbúcies (36) ⚠️ | Arbúcies › la Selva (Gérone) | 6 |
| Forêt de Osor (26) ⚠️ | Osor › la Selva (Gérone) | 6 |
| El Trabuc ⚠️ | Castelló d'Empúries › Alt Empordà | 6 |
| Bois de Olot (21) ⚠️ | Olot › Garrotxa | 6 |
| Bois de Bescanó (8) ⚠️ | Bescanó › Gironès | 6 |
| Forêt de Amer (4) ⚠️ | Amer › la Selva (Gérone) | 6 |
| Forêt de Gombrèn (68) ⚠️ | Gombrèn › Ripollès | 6 |
| Forêt de Siurana (8) ⚠️ | Siurana › Alt Empordà | 6 |
| Forêt de Cervià de Ter (43) ⚠️ | Cervià de Ter › Gironès | 6 |
| Forêt de Sant Feliu de Buixalleu (23) ⚠️ | Sant Feliu de Buixalleu › la Selva (Gérone) | 6 |
| Forêt de Riells i Viabrea (33) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 6 |
| Forêt de Riudaura (4) ⚠️ | Riudaura › Garrotxa | 6 |
| Forêt de Vilademuls (28) ⚠️ | Vilademuls › Pla de l'Estany | 6 |
| Forêt de Garrigàs (20) ⚠️ | Garrigàs › Alt Empordà | 6 |
| Forêt de Sant Mori (2) ⚠️ | Sant Mori › Alt Empordà | 6 |
| Forêt de Massanes (2) ⚠️ | Massanes › la Selva (Gérone) | 5 |
| Forêt de Avinyonet de Puigventós (4) ⚠️ | Avinyonet de Puigventós › Alt Empordà | 5 |
| Bosc d'en Llobet ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 5 |
| Forêt de Vilobí d'Onyar (23) ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 5 |
| Forêt de Vilafant ⚠️ | Vilafant › Alt Empordà | 5 |
| Forêt de Cassà de la Selva (13) ⚠️ | Cassà de la Selva › Gironès | 5 |
| Forêt de Cassà de la Selva (14) ⚠️ | Cassà de la Selva › Gironès | 5 |
| Forêt de Cassà de la Selva (24) ⚠️ | Cassà de la Selva › Gironès | 5 |
| Forêt de Riudellots de la Selva (12) ⚠️ | Riudellots de la Selva › la Selva (Gérone) | 5 |
| Forêt de Fornells de la Selva (14) ⚠️ | Riudellots de la Selva › la Selva (Gérone) | 5 |
| Forêt de Palamós (3) ⚠️ | Palamós › Baix Empordà | 5 |
| Forêt de Cervià de Ter ⚠️ | Cervià de Ter › Gironès | 5 |
| Forêt de la Vajol (45) ⚠️ | la Vajol › Alt Empordà | 5 |
| Forêt de Fontcoberta (4) ⚠️ | Fontcoberta › Pla de l'Estany | 5 |
| Forêt de Maià de Montcal (3) ⚠️ | Maià de Montcal › Garrotxa | 5 |
| Forêt de Girona (36) ⚠️ | Girona › Gironès | 5 |
| Forêt de la Vall d'en Bas (3) ⚠️ | la Vall d'en Bas › Garrotxa | 5 |
| Forêt de Fontcoberta (8) ⚠️ | Fontcoberta › Pla de l'Estany | 5 |
| Bois de Vilademuls (13) ⚠️ | Vilademuls › Pla de l'Estany | 5 |
| Bois de Sant Julià de Ramis (2) ⚠️ | Sant Julià de Ramis › Gironès | 5 |
| Forêt de Ventalló (6) ⚠️ | Ventalló › Alt Empordà | 5 |
| Bois de Sant Jordi Desvalls (10) ⚠️ | Sant Jordi Desvalls › Gironès | 5 |
| Forêt de Torroella de Montgrí (15) ⚠️ | Torroella de Montgrí › Baix Empordà | 5 |
| Forêt de Garrigàs (11) ⚠️ | Siurana › Alt Empordà | 5 |
| Forêt de Forallac (26) ⚠️ | Forallac › Baix Empordà | 5 |
| Forêt de Llagostera (34) ⚠️ | Llagostera › Gironès | 5 |
| Forêt de Massanes (5) ⚠️ | Massanes › la Selva (Gérone) | 5 |
| Forêt de Olot (10) ⚠️ | Olot › Garrotxa | 5 |
| Forêt de Llagostera (37) ⚠️ | Llagostera › Gironès | 5 |
| Forêt de Sant Feliu de Guíxols (18) ⚠️ | Sant Feliu de Guíxols › Baix Empordà | 5 |
| Forêt de Ullastret (6) ⚠️ | Ullastret › Baix Empordà | 5 |
| Forêt de Crespià (2) ⚠️ | Crespià › Pla de l'Estany | 5 |
| Bois de Navata (3) ⚠️ | Navata › Alt Empordà | 5 |
| Forêt de Ullastret (7) ⚠️ | Ullastret › Baix Empordà | 5 |
| Forêt de Bàscara (8) ⚠️ | Bàscara › Alt Empordà | 5 |
| Bois de Llagostera (19) ⚠️ | Llagostera › Gironès | 5 |
| Forêt de Garrigàs (14) ⚠️ | Garrigàs › Alt Empordà | 5 |
| Forêt de Bescanó (16) ⚠️ | Bescanó › Gironès | 5 |
| Forêt de Jafre (5) ⚠️ | Jafre › Baix Empordà | 5 |
| Forêt de Ventalló (12) ⚠️ | Ventalló › Alt Empordà | 5 |
| Forêt de Llívia (11) ⚠️ | Llívia › Cerdanya (Gérone) | 5 |
| Forêt de Cruïlles, Monells i Sant Sadurní de l'Heura (28) ⚠️ | Cruïlles, Monells i Sant Sadurní de l'Heura › Baix Empordà | 5 |
| Forêt de Brunyola i Sant Martí Sapresa (7) ⚠️ | Brunyola i Sant Martí Sapresa › la Selva (Gérone) | 5 |
| Forêt de Girona (62) ⚠️ | Girona › Gironès | 5 |
| Parc de la Draga ⚠️ | Banyoles › Pla de l'Estany | 5 |
| Forêt de Salt (4) ⚠️ | Salt › Gironès | 5 |
| Forêt de Aiguaviva (29) ⚠️ | Aiguaviva › Gironès | 5 |
| Forêt de Flaçà (6) ⚠️ | Flaçà › Gironès | 5 |
| Forêt de Palamós (14) ⚠️ | Palamós › Baix Empordà | 5 |
| Forêt de Tossa de Mar (20) ⚠️ | Tossa de Mar › la Selva (Gérone) | 5 |
| Forêt de Tossa de Mar (23) ⚠️ | Tossa de Mar › la Selva (Gérone) | 5 |
| Forêt de Lloret de Mar (27) ⚠️ | Lloret de Mar › la Selva (Gérone) | 5 |
| Forêt de Lloret de Mar (32) ⚠️ | Lloret de Mar › la Selva (Gérone) | 5 |
| Forêt de Lloret de Mar (35) ⚠️ | Lloret de Mar › la Selva (Gérone) | 5 |
| Forêt de Torroella de Montgrí (68) ⚠️ | Torroella de Montgrí › Baix Empordà | 5 |
| Forêt de l'Escala (31) ⚠️ | l'Escala › Alt Empordà | 5 |
| Forêt de Roses (20) ⚠️ | Roses › Alt Empordà | 5 |
| Forêt de el Port de la Selva (23) ⚠️ | el Port de la Selva › Alt Empordà | 5 |
| Forêt de Ripoll (11) ⚠️ | Ripoll › Ripollès | 5 |
| Forêt de Sant Joan les Fonts (5) ⚠️ | Sant Joan les Fonts › Garrotxa | 5 |
| Forêt de Sant Joan les Fonts (11) ⚠️ | Sant Joan les Fonts › Garrotxa | 5 |
| Forêt de Ripoll (42) ⚠️ | Ripoll › Ripollès | 5 |
| Forêt de Puigcerdà (6) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 5 |
| Forêt de les Llosses (67) ⚠️ | les Llosses › Ripollès | 5 |
| Forêt de Maçanet de Cabrenys (5) ⚠️ | Maçanet de Cabrenys › Alt Empordà | 5 |
| Forêt de Sant Feliu de Pallerols (4) ⚠️ | Sant Feliu de Pallerols › Garrotxa | 5 |
| Forêt de Sant Feliu de Pallerols (7) ⚠️ | Sant Feliu de Pallerols › Garrotxa | 5 |
| Forêt de Viladrau (34) ⚠️ | Viladrau › Osona (Gérone) | 5 |
| Forêt de Viladrau (43) ⚠️ | Viladrau › Osona (Gérone) | 5 |
| Forêt de Viladrau (47) ⚠️ | Viladrau › Osona (Gérone) | 5 |
| Forêt de Bolvir (6) ⚠️ | Bolvir › Cerdanya (Gérone) | 5 |
| Forêt de Riells i Viabrea (18) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 5 |
| Forêt de Das (26) ⚠️ | Das › Cerdanya (Gérone) | 5 |
| Forêt de Campdevànol (11) ⚠️ | Campdevànol › Ripollès | 5 |
| Forêt de Gombrèn (29) ⚠️ | Gombrèn › Ripollès | 5 |
| Forêt de Campdevànol (27) ⚠️ | Campdevànol › Ripollès | 5 |
| Forêt de Gombrèn (42) ⚠️ | Gombrèn › Ripollès | 5 |
| Forêt de Gombrèn (43) ⚠️ | Gombrèn › Ripollès | 5 |
| Forêt de Gombrèn (55) ⚠️ | Gombrèn › Ripollès | 5 |
| Forêt de Campdevànol (44) ⚠️ | Campdevànol › Ripollès | 5 |
| Forêt de Campdevànol (59) ⚠️ | Campdevànol › Ripollès | 5 |
| Forêt de Campdevànol (64) ⚠️ | Campdevànol › Ripollès | 5 |
| Forêt de Campelles (7) ⚠️ | Campelles › Ripollès | 5 |
| Forêt de Ripoll (58) ⚠️ | Ripoll › Ripollès | 5 |
| Forêt de Ripoll (61) ⚠️ | Ripoll › Ripollès | 5 |
| Forêt de Vallfogona de Ripollès (13) ⚠️ | Vallfogona de Ripollès › Ripollès | 5 |
| Forêt de Montagut i Oix (6) ⚠️ | Montagut i Oix › Garrotxa | 5 |
| Forêt de Montagut i Oix (7) ⚠️ | Montagut i Oix › Garrotxa | 5 |
| Forêt de Montagut i Oix (49) ⚠️ | Montagut i Oix › Garrotxa | 5 |
| Forêt de Tortellà (5) ⚠️ | Tortellà › Garrotxa | 5 |
| Forêt de Albanyà (15) ⚠️ | Albanyà › Alt Empordà | 5 |
| Forêt de Sant Llorenç de la Muga (6) ⚠️ | Sant Llorenç de la Muga › Alt Empordà | 5 |
| Forêt de Sant Llorenç de la Muga (11) ⚠️ | Sant Llorenç de la Muga › Alt Empordà | 5 |
| Forêt de Darnius (5) ⚠️ | Darnius › Alt Empordà | 5 |
| Forêt de la Vajol (50) ⚠️ | la Vajol › Alt Empordà | 5 |
| Forêt de Maçanet de Cabrenys (30) ⚠️ | Maçanet de Cabrenys › Alt Empordà | 5 |
| Forêt de Camprodon (32) ⚠️ | Camprodon › Ripollès | 5 |
| Forêt de Llanars (9) ⚠️ | Llanars › Ripollès | 5 |
| Forêt de Molló (86) ⚠️ | Molló › Ripollès | 5 |
| Forêt de Molló (88) ⚠️ | Molló › Ripollès | 5 |
| Forêt de Molló (90) ⚠️ | Molló › Ripollès | 5 |
| Forêt de Campelles (11) ⚠️ | Campelles › Ripollès | 5 |
| Forêt de Meranges (9) ⚠️ | Meranges › Cerdanya (Gérone) | 5 |
| Forêt de Meranges (22) ⚠️ | Meranges › Cerdanya (Gérone) | 5 |
| Forêt de Sant Joan de les Abadesses (28) ⚠️ | Sant Joan de les Abadesses › Ripollès | 5 |
| Forêt de Susqueda (5) ⚠️ | Susqueda › la Selva (Gérone) | 5 |
| Forêt de la Cellera de Ter (34) ⚠️ | la Cellera de Ter › la Selva (Gérone) | 5 |
| Forêt de Olot (17) ⚠️ | Olot › Garrotxa | 5 |
| Forêt de Santa Coloma de Farners (24) ⚠️ | Santa Coloma de Farners › la Selva (Gérone) | 5 |
| Forêt de Osor (28) ⚠️ | Osor › la Selva (Gérone) | 5 |
| Forêt de Isòvol (12) ⚠️ | Isòvol › Cerdanya (Gérone) | 5 |
| Forêt de el Port de la Selva (37) ⚠️ | el Port de la Selva › Alt Empordà | 5 |
| Forêt de Peralada (8) ⚠️ | Peralada › Alt Empordà | 5 |
| Forêt de Cabanes (10) ⚠️ | Cabanes › Alt Empordà | 5 |
| Forêt de Castelló d'Empúries (10) ⚠️ | Castelló d'Empúries › Alt Empordà | 5 |
| Forêt de Sant Pere Pescador (5) ⚠️ | Sant Pere Pescador › Alt Empordà | 5 |
| Forêt de Vila-sacra (2) ⚠️ | Peralada › Alt Empordà | 5 |
| Forêt de Das (27) ⚠️ | Das › Cerdanya (Gérone) | 5 |
| Forêt de Toses (51) ⚠️ | Toses › Ripollès | 5 |
| Forêt de Toses (56) ⚠️ | Toses › Ripollès | 5 |
| Forêt de Sant Julià de Ramis (14) ⚠️ | Sant Julià de Ramis › Gironès | 5 |
| Forêt de Celrà (9) ⚠️ | Celrà › Gironès | 5 |
| Forêt de Queralbs (39) ⚠️ | Queralbs › Ripollès | 5 |
| Forêt de Sant Hilari Sacalm (40) ⚠️ | Sant Hilari Sacalm › la Selva (Gérone) | 5 |
| Forêt de Susqueda (12) ⚠️ | Susqueda › la Selva (Gérone) | 5 |
| Forêt de Massanes (23) ⚠️ | Massanes › la Selva (Gérone) | 5 |
| Forêt de Sant Feliu de Buixalleu (27) ⚠️ | Sant Feliu de Buixalleu › la Selva (Gérone) | 5 |
| Forêt de Riells i Viabrea (24) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 5 |
| Forêt de la Vall d'en Bas (60) ⚠️ | la Vall d'en Bas › Garrotxa | 5 |
| Forêt de la Vall d'en Bas (63) ⚠️ | la Vall d'en Bas › Garrotxa | 5 |
| Forêt de la Vall d'en Bas (64) ⚠️ | la Vall d'en Bas › Garrotxa | 5 |
| Forêt de la Vall d'en Bas (68) ⚠️ | la Vall d'en Bas › Garrotxa | 5 |
| Forêt de Camprodon (63) ⚠️ | Camprodon › Ripollès | 5 |
| Forêt de Riudaura (2) ⚠️ | Riudaura › Garrotxa | 5 |
| Forêt de Tossa de Mar (45) ⚠️ | Tossa de Mar › la Selva (Gérone) | 5 |
| Bois de Pau (20) ⚠️ | Pau › Alt Empordà | 5 |
| Forêt de Esponellà (4) ⚠️ | Crespià › Pla de l'Estany | 5 |
| Forêt de Esponellà (10) ⚠️ | Esponellà › Pla de l'Estany | 5 |
| Forêt de Cabanelles (11) ⚠️ | Cabanelles › Alt Empordà | 5 |
| Forêt de Besalú (16) ⚠️ | Sant Ferriol › Garrotxa | 5 |
| Forêt de Ventalló (22) ⚠️ | Ventalló › Alt Empordà | 5 |
| Forêt de Torroella de Fluvià (20) ⚠️ | Torroella de Fluvià › Alt Empordà | 5 |
| Forêt de Llagostera ⚠️ | Llagostera › Gironès | 4 |
| Forêt de Llagostera (4) ⚠️ | Llagostera › Gironès | 4 |
| Forêt de Vilobí d'Onyar (3) ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 4 |
| Forêt de Vilobí d'Onyar (8) ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 4 |
| Forêt de Avinyonet de Puigventós (2) ⚠️ | Avinyonet de Puigventós › Alt Empordà | 4 |
| Forêt de Riudellots de la Selva (3) ⚠️ | Riudellots de la Selva › la Selva (Gérone) | 4 |
| Forêt de Arbúcies (3) ⚠️ | Arbúcies › la Selva (Gérone) | 4 |
| Forêt de Garrigàs (5) ⚠️ | Garrigàs › Alt Empordà | 4 |
| Forêt de Girona (7) ⚠️ | Girona › Gironès | 4 |
| Forêt de Forallac (10) ⚠️ | Forallac › Baix Empordà | 4 |
| Forêt de Forallac (16) ⚠️ | Forallac › Baix Empordà | 4 |
| Forêt de Caldes de Malavella (13) ⚠️ | Caldes de Malavella › la Selva (Gérone) | 4 |
| Forêt de Fornells de la Selva (11) ⚠️ | Fornells de la Selva › Gironès | 4 |
| Forêt de Begur (5) ⚠️ | Begur › Baix Empordà | 4 |
| Bosc d'en Puig ⚠️ | Vidreres › la Selva (Gérone) | 4 |
| Forêt de Riudellots de la Selva (15) ⚠️ | Riudellots de la Selva › la Selva (Gérone) | 4 |
| Forêt de Castell d'Aro, Platja d'Aro i s'Agaró (6) ⚠️ | Castell d'Aro, Platja d'Aro i s'Agaró › Baix Empordà | 4 |
| Turó d'en Buc ⚠️ | Lloret de Mar › la Selva (Gérone) | 4 |
| Forêt de Sarrià de Ter (2) ⚠️ | Sarrià de Ter › Gironès | 4 |
| Forêt de Cervià de Ter (23) ⚠️ | Cervià de Ter › Gironès | 4 |
| Forêt de Cervià de Ter (34) ⚠️ | Cervià de Ter › Gironès | 4 |
| Forêt de Massanes (3) ⚠️ | Massanes › la Selva (Gérone) | 4 |
| Forêt de la Vajol (25) ⚠️ | la Vajol › Alt Empordà | 4 |
| Forêt de la Vajol (42) ⚠️ | la Vajol › Alt Empordà | 4 |
| Forêt de l'Escala (2) ⚠️ | l'Escala › Alt Empordà | 4 |
| Forêt de Santa Cristina d'Aro (7) ⚠️ | Santa Cristina d'Aro › Baix Empordà | 4 |
| Forêt de Cornellà del Terri (3) ⚠️ | Cornellà del Terri › Pla de l'Estany | 4 |
| Forêt de Cornellà del Terri (10) ⚠️ | Cornellà del Terri › Pla de l'Estany | 4 |
| Forêt de Vila-sacra ⚠️ | Vila-sacra › Alt Empordà | 4 |
| Forêt de Sils (5) ⚠️ | Sils › la Selva (Gérone) | 4 |
| Forêt de Santa Coloma de Farners (6) ⚠️ | Santa Coloma de Farners › la Selva (Gérone) | 4 |
| Forêt de Alp (61) ⚠️ | Alp › Cerdanya (Gérone) | 4 |
| Forêt de Das (20) ⚠️ | Das › Cerdanya (Gérone) | 4 |
| Forêt de Alp (81) ⚠️ | Alp › Cerdanya (Gérone) | 4 |
| Forêt de Sils (9) ⚠️ | Sils › la Selva (Gérone) | 4 |
| Bois de Vilanant (4) ⚠️ | Vilanant › Alt Empordà | 4 |
| Bois de Sant Jordi Desvalls (6) ⚠️ | Sant Jordi Desvalls › Gironès | 4 |
| Forêt de Sils (11) ⚠️ | Sils › la Selva (Gérone) | 4 |
| Forêt de Torroella de Montgrí (37) ⚠️ | Torroella de Montgrí › Baix Empordà | 4 |
| Forêt de la Vajol (46) ⚠️ | la Vajol › Alt Empordà | 4 |
| Forêt de Ger (3) ⚠️ | Ger › Cerdanya (Gérone) | 4 |
| Forêt de el Port de la Selva (7) ⚠️ | el Port de la Selva › Alt Empordà | 4 |
| Bois de Mont-ras (9) ⚠️ | Mont-ras › Baix Empordà | 4 |
| Forêt de Torroella de Montgrí (59) ⚠️ | Torroella de Montgrí › Baix Empordà | 4 |
| les Vidales ⚠️ | Brunyola i Sant Martí Sapresa › la Selva (Gérone) | 4 |
| Bois de Sant Gregori (4) ⚠️ | Sant Gregori › Gironès | 4 |
| Forêt de Saus, Camallera i Llampaies (4) ⚠️ | Saus, Camallera i Llampaies › Alt Empordà | 4 |
| Bois de Ullastret (2) ⚠️ | Ullastret › Baix Empordà | 4 |
| Bois de Madremanya (3) ⚠️ | Madremanya › Gironès | 4 |
| Forêt de Sils (16) ⚠️ | Sils › la Selva (Gérone) | 4 |
| Forêt de Mont-ras (10) ⚠️ | Mont-ras › Baix Empordà | 4 |
| Bois de Vilallonga de Ter ⚠️ | Vilallonga de Ter › Ripollès | 4 |
| Forêt de Riudarenes (9) ⚠️ | Riudarenes › la Selva (Gérone) | 4 |
| Forêt de Llançà (9) ⚠️ | Llançà › Alt Empordà | 4 |
| Parc dels Estanys ⚠️ | Castell d'Aro, Platja d'Aro i s'Agaró › Baix Empordà | 4 |
| Forêt de Castell d'Aro, Platja d'Aro i s'Agaró (21) ⚠️ | Castell d'Aro, Platja d'Aro i s'Agaró › Baix Empordà | 4 |
| Forêt de Vilademuls (13) ⚠️ | Vilademuls › Pla de l'Estany | 4 |
| Forêt de Ripoll (8) ⚠️ | Ripoll › Ripollès | 4 |
| Bois de la Cellera de Ter (7) ⚠️ | la Cellera de Ter › la Selva (Gérone) | 4 |
| Forêt de Viladrau (21) ⚠️ | Viladrau › Osona (Gérone) | 4 |
| Forêt de Viladrau (22) ⚠️ | Viladrau › Osona (Gérone) | 4 |
| Forêt de Sant Julià de Ramis (7) ⚠️ | Sant Julià de Ramis › Gironès | 4 |
| Forêt de la Cellera de Ter (26) ⚠️ | la Cellera de Ter › la Selva (Gérone) | 4 |
| Forêt de Sant Andreu Salou (8) ⚠️ | Sant Andreu Salou › Gironès | 4 |
| Forêt de Llagostera (44) ⚠️ | Llagostera › Gironès | 4 |
| Forêt de Cornellà del Terri (16) ⚠️ | Cornellà del Terri › Pla de l'Estany | 4 |
| Bois de Porqueres (6) ⚠️ | Porqueres › Pla de l'Estany | 4 |
| Forêt de Camós (5) ⚠️ | Cornellà del Terri › Pla de l'Estany | 4 |
| Bois de Vilademuls (20) ⚠️ | Vilademuls › Pla de l'Estany | 4 |
| Forêt de Flaçà (5) ⚠️ | Flaçà › Gironès | 4 |
| Forêt de la Vajol (48) ⚠️ | la Vajol › Alt Empordà | 4 |
| Forêt de Aiguaviva (34) ⚠️ | Aiguaviva › Gironès | 4 |
| Forêt de Palafrugell (121) ⚠️ | Palafrugell › Baix Empordà | 4 |
| Forêt de Lloret de Mar (23) ⚠️ | Lloret de Mar › la Selva (Gérone) | 4 |
| Forêt de Tossa de Mar (28) ⚠️ | Tossa de Mar › la Selva (Gérone) | 4 |
| Forêt de Torroella de Montgrí (66) ⚠️ | Torroella de Montgrí › Baix Empordà | 4 |
| Forêt de Roses (22) ⚠️ | Roses › Alt Empordà | 4 |
| Forêt de Colera (3) ⚠️ | Colera › Alt Empordà | 4 |
| Forêt de el Port de la Selva (20) ⚠️ | el Port de la Selva › Alt Empordà | 4 |
| Forêt de Setcases (38) ⚠️ | Setcases › Ripollès | 4 |
| Forêt de Campdevànol (6) ⚠️ | Campdevànol › Ripollès | 4 |
| Forêt de Campdevànol (7) ⚠️ | Campdevànol › Ripollès | 4 |
| Forêt de Ripoll (30) ⚠️ | Ripoll › Ripollès | 4 |
| Forêt de Bolvir (3) ⚠️ | Bolvir › Cerdanya (Gérone) | 4 |
| Forêt de Guils de Cerdanya ⚠️ | Guils de Cerdanya › Cerdanya (Gérone) | 4 |
| Forêt de Ger (7) ⚠️ | Ger › Cerdanya (Gérone) | 4 |
| Forêt de Palamós (19) ⚠️ | Palamós › Baix Empordà | 4 |
| Forêt de Blanes (18) ⚠️ | Blanes › la Selva (Gérone) | 4 |
| Forêt de Sant Martí de Llémena (3) ⚠️ | Sant Martí de Llémena › Gironès | 4 |
| Forêt de Anglès (9) ⚠️ | Anglès › la Selva (Gérone) | 4 |
| Forêt de Puigcerdà (7) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 4 |
| Forêt de Pals (64) ⚠️ | Pals › Baix Empordà | 4 |
| Forêt de Sant Feliu de Guíxols (32) ⚠️ | Sant Feliu de Guíxols › Baix Empordà | 4 |
| Forêt de les Llosses (79) ⚠️ | les Llosses › Ripollès | 4 |
| Forêt de Olot (15) ⚠️ | Olot › Garrotxa | 4 |
| Forêt de Susqueda (3) ⚠️ | Susqueda › la Selva (Gérone) | 4 |
| Forêt de les Planes d'Hostoles (10) ⚠️ | les Planes d'Hostoles › Garrotxa | 4 |
| Forêt de Viladrau (48) ⚠️ | Viladrau › Osona (Gérone) | 4 |
| Forêt de Urús (3) ⚠️ | Urús › Cerdanya (Gérone) | 4 |
| Forêt de les Llosses (87) ⚠️ | les Llosses › Ripollès | 4 |
| Forêt de Campdevànol (25) ⚠️ | Campdevànol › Ripollès | 4 |
| Forêt de Campdevànol (43) ⚠️ | Campdevànol › Ripollès | 4 |
| Forêt de Campdevànol (45) ⚠️ | Campdevànol › Ripollès | 4 |
| Forêt de les Llosses (100) ⚠️ | les Llosses › Ripollès | 4 |
| Forêt de les Llosses (102) ⚠️ | les Llosses › Ripollès | 4 |
| Forêt de Ogassa (10) ⚠️ | Campdevànol › Ripollès | 4 |
| Forêt de Ribes de Freser (29) ⚠️ | Ribes de Freser › Ripollès | 4 |
| Forêt de Vallfogona de Ripollès (14) ⚠️ | Vallfogona de Ripollès › Ripollès | 4 |
| Forêt de Ripoll (71) ⚠️ | Ripoll › Ripollès | 4 |
| Bois de Bescanó (7) ⚠️ | Bescanó › Gironès | 4 |
| Forêt de Sales de Llierca (4) ⚠️ | Sales de Llierca › Garrotxa | 4 |
| Forêt de Montagut i Oix (30) ⚠️ | Montagut i Oix › Garrotxa | 4 |
| Forêt de Montagut i Oix (46) ⚠️ | Montagut i Oix › Garrotxa | 4 |
| Forêt de Montagut i Oix (51) ⚠️ | Montagut i Oix › Garrotxa | 4 |
| Forêt de Montagut i Oix (63) ⚠️ | Montagut i Oix › Garrotxa | 4 |
| Forêt de Argelaguer (3) ⚠️ | Argelaguer › Garrotxa | 4 |
| Forêt de Tortellà (6) ⚠️ | Tortellà › Garrotxa | 4 |
| Forêt de Albanyà (13) ⚠️ | Albanyà › Alt Empordà | 4 |
| Forêt de Albanyà (27) ⚠️ | Albanyà › Alt Empordà | 4 |
| Forêt de Camprodon (41) ⚠️ | Molló › Ripollès | 4 |
| Forêt de Setcases (102) ⚠️ | Setcases › Ripollès | 4 |
| Forêt de Toses (39) ⚠️ | Toses › Ripollès | 4 |
| Forêt de Toses (46) ⚠️ | Toses › Ripollès | 4 |
| Forêt de Meranges (17) ⚠️ | Meranges › Cerdanya (Gérone) | 4 |
| Forêt de Meranges (19) ⚠️ | Meranges › Cerdanya (Gérone) | 4 |
| Forêt de Meranges (26) ⚠️ | Meranges › Cerdanya (Gérone) | 4 |
| Forêt de la Vall de Bianya (21) ⚠️ | la Vall de Bianya › Garrotxa | 4 |
| Forêt de Sant Pau de Segúries (5) ⚠️ | Sant Pau de Segúries › Ripollès | 4 |
| Forêt de Sant Joan de les Abadesses (19) ⚠️ | Sant Joan de les Abadesses › Ripollès | 4 |
| Forêt de Sant Joan de les Abadesses (25) ⚠️ | Sant Joan de les Abadesses › Ripollès | 4 |
| Forêt de la Vall de Bianya (27) ⚠️ | la Vall de Bianya › Garrotxa | 4 |
| Forêt de la Vall de Bianya (29) ⚠️ | la Vall de Bianya › Garrotxa | 4 |
| Forêt de Ripoll (81) ⚠️ | Ripoll › Ripollès | 4 |
| Forêt de Olot (23) ⚠️ | Olot › Garrotxa | 4 |
| Forêt de Santa Coloma de Farners (28) ⚠️ | Santa Coloma de Farners › la Selva (Gérone) | 4 |
| Forêt de Arbúcies (30) ⚠️ | Arbúcies › la Selva (Gérone) | 4 |
| Forêt de Arbúcies (37) ⚠️ | Arbúcies › la Selva (Gérone) | 4 |
| Forêt de el Port de la Selva (28) ⚠️ | el Port de la Selva › Alt Empordà | 4 |
| Forêt de el Port de la Selva (36) ⚠️ | el Port de la Selva › Alt Empordà | 4 |
| Forêt de Peralada (6) ⚠️ | Peralada › Alt Empordà | 4 |
| Forêt de Peralada (10) ⚠️ | Peralada › Alt Empordà | 4 |
| Forêt de Cabanes (7) ⚠️ | Cabanes › Alt Empordà | 4 |
| Forêt de Castelló d'Empúries (11) ⚠️ | Castelló d'Empúries › Alt Empordà | 4 |
| Forêt de Castelló d'Empúries (15) ⚠️ | Castelló d'Empúries › Alt Empordà | 4 |
| Forêt de Gombrèn (78) ⚠️ | Gombrèn › Ripollès | 4 |
| Forêt de Toses (55) ⚠️ | Toses › Ripollès | 4 |
| Forêt de les Preses ⚠️ | les Preses › Garrotxa | 4 |
| Forêt de Sant Julià de Ramis (18) ⚠️ | Sant Julià de Ramis › Gironès | 4 |
| Forêt de la Vall d'en Bas (61) ⚠️ | la Vall d'en Bas › Garrotxa | 4 |
| Forêt de la Vall de Bianya (35) ⚠️ | la Vall de Bianya › Garrotxa | 4 |
| Forêt de Juià (3) ⚠️ | Juià › Gironès | 4 |
| Forêt de Viladrau (63) ⚠️ | Viladrau › Osona (Gérone) | 4 |
| Forêt de Vilallonga de Ter (26) ⚠️ | Vilallonga de Ter › Ripollès | 4 |
| Forêt de Ribes de Freser (47) ⚠️ | Ribes de Freser › Ripollès | 4 |
| Forêt de Esponellà (6) ⚠️ | Esponellà › Pla de l'Estany | 4 |
| Forêt de Cabanelles (7) ⚠️ | Cabanelles › Alt Empordà | 4 |
| Forêt de Vilademuls (29) ⚠️ | Vilademuls › Pla de l'Estany | 4 |
| Forêt de Argelaguer (10) ⚠️ | Argelaguer › Garrotxa | 4 |
| Forêt de Ventalló (21) ⚠️ | Ventalló › Alt Empordà | 4 |
| Forêt de Torroella de Fluvià (15) ⚠️ | Ventalló › Alt Empordà | 4 |
| Forêt de Torroella de Fluvià (17) ⚠️ | Torroella de Fluvià › Alt Empordà | 4 |
| Forêt de Sant Hilari Sacalm (7) ⚠️ | Sant Hilari Sacalm › la Selva (Gérone) | 3 |
| Forêt de la Vall d'en Bas ⚠️ | la Vall d'en Bas › Garrotxa | 3 |
| Forêt de Sant Hilari Sacalm (10) ⚠️ | Sant Hilari Sacalm › la Selva (Gérone) | 3 |
| Forêt de Viladrau (11) ⚠️ | Viladrau › Osona (Gérone) | 3 |
| Forêt de Sant Feliu de Buixalleu (6) ⚠️ | Sant Feliu de Buixalleu › la Selva (Gérone) | 3 |
| Forêt de Canet d'Adri (3) ⚠️ | Canet d'Adri › Gironès | 3 |
| Forêt de Canet d'Adri (5) ⚠️ | Canet d'Adri › Gironès | 3 |
| Forêt de Avinyonet de Puigventós ⚠️ | Avinyonet de Puigventós › Alt Empordà | 3 |
| Bosc d'en Ros ⚠️ | Aiguaviva › Gironès | 3 |
| Forêt de Riudellots de la Selva (5) ⚠️ | Riudellots de la Selva › la Selva (Gérone) | 3 |
| Forêt de Siurana ⚠️ | Siurana › Alt Empordà | 3 |
| Forêt de Avinyonet de Puigventós (5) ⚠️ | Avinyonet de Puigventós › Alt Empordà | 3 |
| Forêt de Llers (3) ⚠️ | Llers › Alt Empordà | 3 |
| Forêt de Llers (4) ⚠️ | Llers › Alt Empordà | 3 |
| Forêt de Garrigàs (4) ⚠️ | Garrigàs › Alt Empordà | 3 |
| Forêt de Cruïlles, Monells i Sant Sadurní de l'Heura (7) ⚠️ | Cruïlles, Monells i Sant Sadurní de l'Heura › Baix Empordà | 3 |
| Forêt de Cruïlles, Monells i Sant Sadurní de l'Heura (8) ⚠️ | Cruïlles, Monells i Sant Sadurní de l'Heura › Baix Empordà | 3 |
| Forêt de Forallac (9) ⚠️ | Forallac › Baix Empordà | 3 |
| Forêt de Celrà (6) ⚠️ | Celrà › Gironès | 3 |
| Pins d'en Ros ⚠️ | Celrà › Gironès | 3 |
| Forêt de Vilobí d'Onyar (28) ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 3 |
| Forêt de Llagostera (16) ⚠️ | Llagostera › Gironès | 3 |
| Forêt de Llagostera (17) ⚠️ | Llagostera › Gironès | 3 |
| Forêt de Llagostera (20) ⚠️ | Llagostera › Gironès | 3 |
| Forêt de Llagostera (24) ⚠️ | Llagostera › Gironès | 3 |
| Forêt de Cassà de la Selva (10) ⚠️ | Cassà de la Selva › Gironès | 3 |
| Forêt de Cassà de la Selva (22) ⚠️ | Cassà de la Selva › Gironès | 3 |
| Forêt de Caldes de Malavella (7) ⚠️ | Caldes de Malavella › la Selva (Gérone) | 3 |
| Forêt de Caldes de Malavella (12) ⚠️ | Caldes de Malavella › la Selva (Gérone) | 3 |
| Forêt de Caldes de Malavella (14) ⚠️ | Caldes de Malavella › la Selva (Gérone) | 3 |
| Forêt de Palafrugell ⚠️ | Palafrugell › Baix Empordà | 3 |
| Forêt de Sant Feliu de Guíxols (13) ⚠️ | Sant Feliu de Guíxols › Baix Empordà | 3 |
| Parc de Can Santaló ⚠️ | Tortellà › Garrotxa | 3 |
| Illa del Ter ⚠️ | Girona › Gironès | 3 |
| Forêt de Cervià de Ter (14) ⚠️ | Cervià de Ter › Gironès | 3 |
| Forêt de la Vajol (43) ⚠️ | Darnius › Alt Empordà | 3 |
| Forêt de Mont-ras (7) ⚠️ | Mont-ras › Baix Empordà | 3 |
| Forêt de Aiguaviva (21) ⚠️ | Aiguaviva › Gironès | 3 |
| Forêt de Fornells de la Selva (15) ⚠️ | Fornells de la Selva › Gironès | 3 |
| Forêt de Sant Julià de Ramis (3) ⚠️ | Sant Julià de Ramis › Gironès | 3 |
| Forêt de Camós (2) ⚠️ | Camós › Pla de l'Estany | 3 |
| Parc de Llívia ⚠️ | Llívia › Cerdanya (Gérone) | 3 |
| Forêt de Quart (9) ⚠️ | Quart › Gironès | 3 |
| Forêt de Banyoles (4) ⚠️ | Banyoles › Pla de l'Estany | 3 |
| Forêt de Girona (18) ⚠️ | Girona › Gironès | 3 |
| Forêt de Das (16) ⚠️ | Das › Cerdanya (Gérone) | 3 |
| Forêt de Das (17) ⚠️ | Das › Cerdanya (Gérone) | 3 |
| Forêt de Alp (48) ⚠️ | Alp › Cerdanya (Gérone) | 3 |
| Forêt de Alp (58) ⚠️ | Alp › Cerdanya (Gérone) | 3 |
| Forêt de Alp (65) ⚠️ | Alp › Cerdanya (Gérone) | 3 |
| Forêt de Llagostera (33) ⚠️ | Llagostera › Gironès | 3 |
| Forêt de Vilanant (2) ⚠️ | Vilanant › Alt Empordà | 3 |
| Bois de Vilademuls (9) ⚠️ | Vilademuls › Pla de l'Estany | 3 |
| Bois de Vilademuls (12) ⚠️ | Vilademuls › Pla de l'Estany | 3 |
| Bois de Vilanant (3) ⚠️ | Vilanant › Alt Empordà | 3 |
| Forêt de Ventalló (2) ⚠️ | Ventalló › Alt Empordà | 3 |
| Forêt de Garrigoles (3) ⚠️ | Garrigoles › Baix Empordà | 3 |
| Bois de la Pera ⚠️ | la Pera › Baix Empordà | 3 |
| Bois de Sant Jordi Desvalls (2) ⚠️ | Sant Jordi Desvalls › Gironès | 3 |
| Bois de Sant Jordi Desvalls (3) ⚠️ | Sant Jordi Desvalls › Gironès | 3 |
| Bois de Sant Jordi Desvalls (13) ⚠️ | Sant Jordi Desvalls › Gironès | 3 |
| Forêt de Bescanó (9) ⚠️ | Bescanó › Gironès | 3 |
| Forêt de Blanes (6) ⚠️ | Blanes › la Selva (Gérone) | 3 |
| Forêt de Palafrugell (101) ⚠️ | Palafrugell › Baix Empordà | 3 |
| Bois de Maçanet de la Selva (2) ⚠️ | Maçanet de la Selva › la Selva (Gérone) | 3 |
| Forêt de Borrassà (3) ⚠️ | Borrassà › Alt Empordà | 3 |
| Forêt de el Port de la Selva (2) ⚠️ | el Port de la Selva › Alt Empordà | 3 |
| Forêt de la Bisbal d'Empordà (5) ⚠️ | la Bisbal d'Empordà › Baix Empordà | 3 |
| Forêt de Setcases (5) ⚠️ | Setcases › Ripollès | 3 |
| Forêt de Massanes (6) ⚠️ | Massanes › la Selva (Gérone) | 3 |
| Bois de Sant Martí Vell ⚠️ | Sant Martí Vell › Gironès | 3 |
| Forêt de Blanes (8) ⚠️ | Blanes › la Selva (Gérone) | 3 |
| Forêt de Sils (12) ⚠️ | Sils › la Selva (Gérone) | 3 |
| Forêt de Sant Feliu de Guíxols (22) ⚠️ | Sant Feliu de Guíxols › Baix Empordà | 3 |
| Forêt de Girona (51) ⚠️ | Girona › Gironès | 3 |
| Forêt de Girona (52) ⚠️ | Girona › Gironès | 3 |
| Forêt de Girona (54) ⚠️ | Girona › Gironès | 3 |
| Forêt de Esponellà ⚠️ | Esponellà › Pla de l'Estany | 3 |
| Bois de Salt ⚠️ | Salt › Gironès | 3 |
| Bois de Salt (5) ⚠️ | Salt › Gironès | 3 |
| Forêt de Corçà (12) ⚠️ | Corçà › Baix Empordà | 3 |
| Bois de la Bisbal d'Empordà (3) ⚠️ | la Bisbal d'Empordà › Baix Empordà | 3 |
| Bois de Ullastret (6) ⚠️ | Ullastret › Baix Empordà | 3 |
| Bois de la Vall d'en Bas ⚠️ | la Vall d'en Bas › Garrotxa | 3 |
| Forêt de Llagostera (38) ⚠️ | Llagostera › Gironès | 3 |
| Bois de Cistella ⚠️ | Cistella › Alt Empordà | 3 |
| Forêt de Cornellà del Terri (12) ⚠️ | Cornellà del Terri › Pla de l'Estany | 3 |
| Forêt de Setcases (31) ⚠️ | Setcases › Ripollès | 3 |
| Bois de Anglès (4) ⚠️ | Anglès › la Selva (Gérone) | 3 |
| Forêt de Llagostera (40) ⚠️ | Llagostera › Gironès | 3 |
| Forêt de la Jonquera (11) ⚠️ | la Jonquera › Alt Empordà | 3 |
| Forêt de Puigcerdà (3) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 3 |
| Forêt de Avinyonet de Puigventós (6) ⚠️ | Avinyonet de Puigventós › Alt Empordà | 3 |
| Forêt de Viladrau (20) ⚠️ | Viladrau › Osona (Gérone) | 3 |
| Forêt de Viladrau (23) ⚠️ | Viladrau › Osona (Gérone) | 3 |
| Forêt de Fontanilles (2) ⚠️ | Fontanilles › Baix Empordà | 3 |
| Forêt de Cruïlles, Monells i Sant Sadurní de l'Heura (29) ⚠️ | Cruïlles, Monells i Sant Sadurní de l'Heura › Baix Empordà | 3 |
| Forêt de Mont-ras (12) ⚠️ | Mont-ras › Baix Empordà | 3 |
| Bois de Banyoles (3) ⚠️ | Banyoles › Pla de l'Estany | 3 |
| Forêt de Aiguaviva (30) ⚠️ | Aiguaviva › Gironès | 3 |
| Forêt de Girona (72) ⚠️ | Girona › Gironès | 3 |
| Forêt de la Cellera de Ter (30) ⚠️ | la Cellera de Ter › la Selva (Gérone) | 3 |
| Forêt de Anglès (8) ⚠️ | Anglès › la Selva (Gérone) | 3 |
| Bois de Fontcoberta (3) ⚠️ | Fontcoberta › Pla de l'Estany | 3 |
| Forêt de Queralbs (26) ⚠️ | Queralbs › Ripollès | 3 |
| Forêt de Begur (17) ⚠️ | Begur › Baix Empordà | 3 |
| Forêt de Begur (36) ⚠️ | Begur › Baix Empordà | 3 |
| Forêt de Sant Feliu de Guíxols (25) ⚠️ | Sant Feliu de Guíxols › Baix Empordà | 3 |
| Forêt de Tossa de Mar (11) ⚠️ | Tossa de Mar › la Selva (Gérone) | 3 |
| Forêt de Tossa de Mar (12) ⚠️ | Tossa de Mar › la Selva (Gérone) | 3 |
| Forêt de Tossa de Mar (19) ⚠️ | Tossa de Mar › la Selva (Gérone) | 3 |
| Forêt de Lloret de Mar (22) ⚠️ | Lloret de Mar › la Selva (Gérone) | 3 |
| Forêt de Lloret de Mar (25) ⚠️ | Lloret de Mar › la Selva (Gérone) | 3 |
| Forêt de Palamós (17) ⚠️ | Palamós › Baix Empordà | 3 |
| Forêt de l'Escala (30) ⚠️ | l'Escala › Alt Empordà | 3 |
| Forêt de l'Escala (32) ⚠️ | l'Escala › Alt Empordà | 3 |
| Forêt de l'Escala (33) ⚠️ | l'Escala › Alt Empordà | 3 |
| Forêt de Roses (16) ⚠️ | Roses › Alt Empordà | 3 |
| Forêt de Cadaqués (7) ⚠️ | Cadaqués › Alt Empordà | 3 |
| Forêt de el Port de la Selva (15) ⚠️ | el Port de la Selva › Alt Empordà | 3 |
| Forêt de el Port de la Selva (21) ⚠️ | el Port de la Selva › Alt Empordà | 3 |
| Forêt de Colera (10) ⚠️ | Colera › Alt Empordà | 3 |
| Forêt de Colera (13) ⚠️ | Colera › Alt Empordà | 3 |
| Forêt de Roses (24) ⚠️ | Roses › Alt Empordà | 3 |
| Forêt de Setcases (35) ⚠️ | Setcases › Ripollès | 3 |
| Forêt de Setcases (47) ⚠️ | Setcases › Ripollès | 3 |
| Forêt de Setcases (52) ⚠️ | Setcases › Ripollès | 3 |
| Forêt de Ripoll (23) ⚠️ | Ripoll › Ripollès | 3 |
| Forêt de Camprodon (8) ⚠️ | Llanars › Ripollès | 3 |
| Forêt de Roses (27) ⚠️ | Roses › Alt Empordà | 3 |
| Forêt de Calonge i Sant Antoni (33) ⚠️ | Calonge i Sant Antoni › Baix Empordà | 3 |
| Forêt de Pals (11) ⚠️ | Pals › Baix Empordà | 3 |
| Forêt de Torroella de Montgrí (79) ⚠️ | Torroella de Montgrí › Baix Empordà | 3 |
| Forêt de Tossa de Mar (29) ⚠️ | Tossa de Mar › la Selva (Gérone) | 3 |
| Forêt de Llagostera (46) ⚠️ | Llagostera › Gironès | 3 |
| Forêt de Vidreres (14) ⚠️ | Vidreres › la Selva (Gérone) | 3 |
| Forêt de Vidreres (16) ⚠️ | Vidreres › la Selva (Gérone) | 3 |
| Forêt de Blanes (17) ⚠️ | Blanes › la Selva (Gérone) | 3 |
| Forêt de Toses (9) ⚠️ | Toses › Ripollès | 3 |
| Forêt de les Llosses (45) ⚠️ | les Llosses › Ripollès | 3 |
| Forêt de les Llosses (52) ⚠️ | les Llosses › Ripollès | 3 |
| Forêt de Sarrià de Ter (15) ⚠️ | Sarrià de Ter › Gironès | 3 |
| Forêt de Torroella de Montgrí (80) ⚠️ | Torroella de Montgrí › Baix Empordà | 3 |
| Mota dels Oms ⚠️ | Torroella de Montgrí › Baix Empordà | 3 |
| Forêt de Torroella de Montgrí (88) ⚠️ | Torroella de Montgrí › Baix Empordà | 3 |
| Forêt de Pals (35) ⚠️ | Pals › Baix Empordà | 3 |
| Forêt de Pals (38) ⚠️ | Pals › Baix Empordà | 3 |
| Forêt de Pals (54) ⚠️ | Pals › Baix Empordà | 3 |
| Bois de Vilallonga de Ter (8) ⚠️ | Vilallonga de Ter › Ripollès | 3 |
| Bois de Vilallonga de Ter (9) ⚠️ | Vilallonga de Ter › Ripollès | 3 |
| Bois de Fontanals de Cerdanya (2) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 3 |
| Bois de Fontanals de Cerdanya (3) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 3 |
| Forêt de les Llosses (64) ⚠️ | les Llosses › Ripollès | 3 |
| Forêt de Vallfogona de Ripollès (8) ⚠️ | Vallfogona de Ripollès › Ripollès | 3 |
| Forêt de la Vall d'en Bas (16) ⚠️ | la Vall d'en Bas › Garrotxa | 3 |
| Forêt de Pals (71) ⚠️ | Pals › Baix Empordà | 3 |
| Forêt de Santa Coloma de Farners (19) ⚠️ | Santa Coloma de Farners › la Selva (Gérone) | 3 |
| Forêt de Puigcerdà (26) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 3 |
| Forêt de Puigcerdà (32) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 3 |
| Forêt de Puigcerdà (110) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 3 |
| Forêt de Puigcerdà (122) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 3 |
| Forêt de Alp (101) ⚠️ | Alp › Cerdanya (Gérone) | 3 |
| Forêt de Alp (105) ⚠️ | Alp › Cerdanya (Gérone) | 3 |
| Forêt de Urús (4) ⚠️ | Urús › Cerdanya (Gérone) | 3 |
| Forêt de Gombrèn (12) ⚠️ | Gombrèn › Ripollès | 3 |
| Forêt de Gombrèn (25) ⚠️ | Gombrèn › Ripollès | 3 |
| Forêt de Gombrèn (40) ⚠️ | Gombrèn › Ripollès | 3 |
| Forêt de Gombrèn (45) ⚠️ | Gombrèn › Ripollès | 3 |
| Forêt de Gombrèn (46) ⚠️ | Gombrèn › Ripollès | 3 |
| Forêt de Gombrèn (51) ⚠️ | Gombrèn › Ripollès | 3 |
| Forêt de Campdevànol (33) ⚠️ | Campdevànol › Ripollès | 3 |
| Forêt de Gombrèn (61) ⚠️ | Gombrèn › Ripollès | 3 |
| Forêt de Gombrèn (64) ⚠️ | Gombrèn › Ripollès | 3 |
| Forêt de Campdevànol (53) ⚠️ | Campdevànol › Ripollès | 3 |
| Forêt de Campdevànol (54) ⚠️ | Campdevànol › Ripollès | 3 |
| Forêt de Ripoll (53) ⚠️ | Ripoll › Ripollès | 3 |
| Forêt de Campdevànol (73) ⚠️ | Ogassa › Ripollès | 3 |
| Forêt de Ribes de Freser (34) ⚠️ | Ribes de Freser › Ripollès | 3 |
| Forêt de Vallfogona de Ripollès (22) ⚠️ | Vallfogona de Ripollès › Ripollès | 3 |
| Forêt de Montagut i Oix (11) ⚠️ | Montagut i Oix › Garrotxa | 3 |
| Forêt de Montagut i Oix (61) ⚠️ | Montagut i Oix › Garrotxa | 3 |
| Forêt de Montagut i Oix (62) ⚠️ | Montagut i Oix › Garrotxa | 3 |
| Forêt de Montagut i Oix (65) ⚠️ | Montagut i Oix › Garrotxa | 3 |
| Forêt de Montagut i Oix (72) ⚠️ | Montagut i Oix › Garrotxa | 3 |
| Forêt de Montagut i Oix (74) ⚠️ | Montagut i Oix › Garrotxa | 3 |
| Forêt de Albanyà (29) ⚠️ | Albanyà › Alt Empordà | 3 |
| Forêt de Albanyà (30) ⚠️ | Albanyà › Alt Empordà | 3 |
| Forêt de Espolla (10) ⚠️ | Espolla › Alt Empordà | 3 |
| Forêt de la Jonquera (26) ⚠️ | la Jonquera › Alt Empordà | 3 |
| Forêt de Rabós (12) ⚠️ | Rabós › Alt Empordà | 3 |
| Forêt de Molló (20) ⚠️ | Molló › Ripollès | 3 |
| Forêt de Molló (39) ⚠️ | Molló › Ripollès | 3 |
| Forêt de Molló (45) ⚠️ | Molló › Ripollès | 3 |
| Forêt de Molló (55) ⚠️ | Molló › Ripollès | 3 |
| Forêt de Molló (62) ⚠️ | Molló › Ripollès | 3 |
| Forêt de Setcases (69) ⚠️ | Setcases › Ripollès | 3 |
| Forêt de Setcases (71) ⚠️ | Setcases › Ripollès | 3 |
| Forêt de Llanars (7) ⚠️ | Llanars › Ripollès | 3 |
| Forêt de Setcases (76) ⚠️ | Setcases › Ripollès | 3 |
| Forêt de Llanars (8) ⚠️ | Llanars › Ripollès | 3 |
| Forêt de Setcases (93) ⚠️ | Setcases › Ripollès | 3 |
| Forêt de Molló (75) ⚠️ | Molló › Ripollès | 3 |
| Forêt de Molló (81) ⚠️ | Molló › Ripollès | 3 |
| Forêt de Molló (85) ⚠️ | Molló › Ripollès | 3 |
| Forêt de Toses (24) ⚠️ | Toses › Ripollès | 3 |
| Forêt de Toses (28) ⚠️ | Toses › Ripollès | 3 |
| Forêt de Toses (34) ⚠️ | Toses › Ripollès | 3 |
| Forêt de Planoles (9) ⚠️ | Planoles › Ripollès | 3 |
| Forêt de Planoles (13) ⚠️ | Planoles › Ripollès | 3 |
| Forêt de Planoles (14) ⚠️ | Planoles › Ripollès | 3 |
| Forêt de Meranges (13) ⚠️ | Meranges › Cerdanya (Gérone) | 3 |
| Forêt de Meranges (21) ⚠️ | Meranges › Cerdanya (Gérone) | 3 |
| Forêt de Sant Pau de Segúries (3) ⚠️ | Sant Pau de Segúries › Ripollès | 3 |
| Forêt de Sant Joan de les Abadesses (14) ⚠️ | Sant Joan de les Abadesses › Ripollès | 3 |
| Forêt de Sant Joan de les Abadesses (17) ⚠️ | Sant Joan de les Abadesses › Ripollès | 3 |
| Forêt de Sant Joan de les Abadesses (18) ⚠️ | Sant Joan de les Abadesses › Ripollès | 3 |
| Forêt de Ripoll (74) ⚠️ | Ripoll › Ripollès | 3 |
| Forêt de la Vall de Bianya (28) ⚠️ | la Vall de Bianya › Garrotxa | 3 |
| Forêt de la Vall de Bianya (31) ⚠️ | la Vall de Bianya › Garrotxa | 3 |
| Forêt de la Vall de Bianya (32) ⚠️ | la Vall de Bianya › Garrotxa | 3 |
| Forêt de la Vall de Bianya (33) ⚠️ | la Vall de Bianya › Garrotxa | 3 |
| Forêt de Ripoll (87) ⚠️ | Ripoll › Ripollès | 3 |
| Forêt de les Llosses (120) ⚠️ | les Llosses › Ripollès | 3 |
| Forêt de Vidrà (6) ⚠️ | Vidrà › Osona (Gérone) | 3 |
| Forêt de Ripoll (91) ⚠️ | Ripoll › Ripollès | 3 |
| Forêt de Olot (18) ⚠️ | Olot › Garrotxa | 3 |
| Forêt de Olot (20) ⚠️ | Olot › Garrotxa | 3 |
| Forêt de Montagut i Oix (78) ⚠️ | Montagut i Oix › Garrotxa | 3 |
| Parc de Sant Salvador ⚠️ | Santa Coloma de Farners › la Selva (Gérone) | 3 |
| Forêt de Arbúcies (21) ⚠️ | Arbúcies › la Selva (Gérone) | 3 |
| Forêt de Osor (30) ⚠️ | Osor › la Selva (Gérone) | 3 |
| Forêt de les Llosses (124) ⚠️ | les Llosses › Ripollès | 3 |
| Forêt de Roses (29) ⚠️ | Roses › Alt Empordà | 3 |
| Forêt de Roses (30) ⚠️ | Roses › Alt Empordà | 3 |
| Forêt de Roses (36) ⚠️ | Roses › Alt Empordà | 3 |
| Forêt de Llançà (30) ⚠️ | Llançà › Alt Empordà | 3 |
| Forêt de Vilamaniscle (4) ⚠️ | Vilamaniscle › Alt Empordà | 3 |
| Forêt de Castelló d'Empúries (12) ⚠️ | Castelló d'Empúries › Alt Empordà | 3 |
| Forêt de Figueres (10) ⚠️ | Figueres › Alt Empordà | 3 |
| Bois de Anglès (5) ⚠️ | Anglès › la Selva (Gérone) | 3 |
| Forêt de Riudarenes (24) ⚠️ | Riudarenes › la Selva (Gérone) | 3 |
| Forêt de Gombrèn (69) ⚠️ | Gombrèn › Ripollès | 3 |
| Forêt de Toses (53) ⚠️ | Toses › Ripollès | 3 |
| Forêt de Toses (58) ⚠️ | Toses › Ripollès | 3 |
| Forêt de Santa Pau (26) ⚠️ | Santa Pau › Garrotxa | 3 |
| Forêt de Tossa de Mar (37) ⚠️ | Tossa de Mar › la Selva (Gérone) | 3 |
| Forêt de Torroella de Montgrí (93) ⚠️ | Torroella de Montgrí › Baix Empordà | 3 |
| Forêt de Sant Julià de Ramis (15) ⚠️ | Sant Julià de Ramis › Gironès | 3 |
| Forêt de la Vall d'en Bas (25) ⚠️ | la Vall d'en Bas › Garrotxa | 3 |
| Forêt de la Vall d'en Bas (26) ⚠️ | la Vall d'en Bas › Garrotxa | 3 |
| Forêt de Sant Hilari Sacalm (39) ⚠️ | Sant Hilari Sacalm › la Selva (Gérone) | 3 |
| Forêt de les Llosses (132) ⚠️ | les Llosses › Ripollès | 3 |
| Forêt de Sant Feliu de Buixalleu (32) ⚠️ | Sant Feliu de Buixalleu › la Selva (Gérone) | 3 |
| Forêt de Hostalric (11) ⚠️ | Hostalric › la Selva (Gérone) | 3 |
| Forêt de Riells i Viabrea (35) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 3 |
| Forêt de Riells i Viabrea (36) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 3 |
| Forêt de Riells i Viabrea (39) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 3 |
| Forêt de Camprodon (59) ⚠️ | Camprodon › Ripollès | 3 |
| Forêt de Camprodon (60) ⚠️ | Camprodon › Ripollès | 3 |
| Forêt de la Vall d'en Bas (44) ⚠️ | la Vall d'en Bas › Garrotxa | 3 |
| Forêt de la Vall d'en Bas (45) ⚠️ | la Vall d'en Bas › Garrotxa | 3 |
| Forêt de la Vall d'en Bas (62) ⚠️ | la Vall d'en Bas › Garrotxa | 3 |
| Forêt de la Vall d'en Bas (65) ⚠️ | la Vall d'en Bas › Garrotxa | 3 |
| Forêt de Castellfollit de la Roca (5) ⚠️ | Castellfollit de la Roca › Garrotxa | 3 |
| Forêt de Sant Feliu de Guíxols (33) ⚠️ | Sant Feliu de Guíxols › Baix Empordà | 3 |
| Forêt de Sant Ferriol (13) ⚠️ | Sant Ferriol › Garrotxa | 3 |
| Forêt de Vilallonga de Ter (27) ⚠️ | Vilallonga de Ter › Ripollès | 3 |
| Forêt de Queralbs (43) ⚠️ | Queralbs › Ripollès | 3 |
| Forêt de Queralbs (45) ⚠️ | Queralbs › Ripollès | 3 |
| Forêt de Queralbs (49) ⚠️ | Queralbs › Ripollès | 3 |
| Forêt de Esponellà (7) ⚠️ | Esponellà › Pla de l'Estany | 3 |
| Forêt de Esponellà (8) ⚠️ | Esponellà › Pla de l'Estany | 3 |
| Forêt de Esponellà (9) ⚠️ | Esponellà › Pla de l'Estany | 3 |
| Forêt de Cabanelles (14) ⚠️ | Cabanelles › Alt Empordà | 3 |
| Forêt de Vilademuls (25) ⚠️ | Vilademuls › Pla de l'Estany | 3 |
| Forêt de Vilademuls (34) ⚠️ | Vilademuls › Pla de l'Estany | 3 |
| Forêt de Garrigàs (16) ⚠️ | Garrigàs › Alt Empordà | 3 |
| Forêt de Garrigàs (18) ⚠️ | Garrigàs › Alt Empordà | 3 |
| Forêt de Vilademuls (38) ⚠️ | Vilademuls › Pla de l'Estany | 3 |
| Forêt de Sant Mori (4) ⚠️ | Sant Mori › Alt Empordà | 3 |
| Forêt de Sant Mori (5) ⚠️ | Sant Mori › Alt Empordà | 3 |
| Forêt de Palau de Santa Eulàlia (3) ⚠️ | Palau de Santa Eulàlia › Alt Empordà | 3 |
| Forêt de Torroella de Fluvià (19) ⚠️ | Torroella de Fluvià › Alt Empordà | 3 |
| Forêt de Sant Pere Pescador (12) ⚠️ | Sant Pere Pescador › Alt Empordà | 3 |
| Forêt de l'Armentera (3) ⚠️ | l'Armentera › Alt Empordà | 3 |
| Forêt de Ventalló (24) ⚠️ | Ventalló › Alt Empordà | 3 |
| Forêt de Sant Mori (6) ⚠️ | Sant Mori › Alt Empordà | 3 |
| Forêt de Ripoll (98) ⚠️ | Ripoll › Ripollès | 3 |
| Parc de les Ribes del Ter ⚠️ | Girona › Gironès | 2 |
| Forêt de Vilobí d'Onyar ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 2 |
| Forêt de Vilobí d'Onyar (2) ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 2 |
| Parc Bosc ⚠️ | Figueres › Alt Empordà | 2 |
| Bois de Bescanó (2) ⚠️ | Bescanó › Gironès | 2 |
| Bois de Vilablareix ⚠️ | Vilablareix › Gironès | 2 |
| Forêt de Llagostera (5) ⚠️ | Llagostera › Gironès | 2 |
| Forêt de Sant Hilari Sacalm (4) ⚠️ | Sant Hilari Sacalm › la Selva (Gérone) | 2 |
| Forêt de les Llosses (6) ⚠️ | les Llosses › Ripollès | 2 |
| Forêt de Maçanet de la Selva (2) ⚠️ | Maçanet de la Selva › la Selva (Gérone) | 2 |
| Forêt de Girona (4) ⚠️ | Girona › Gironès | 2 |
| Forêt de Vidrà ⚠️ | Vidrà › Osona (Gérone) | 2 |
| Forêt de Sant Hilari Sacalm (12) ⚠️ | Sant Hilari Sacalm › la Selva (Gérone) | 2 |
| Forêt de les Llosses (31) ⚠️ | les Llosses › Ripollès | 2 |
| Forêt de Vilobí d'Onyar (12) ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 2 |
| Forêt de Vilobí d'Onyar (14) ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 2 |
| Forêt de Aiguaviva (3) ⚠️ | Aiguaviva › Gironès | 2 |
| Forêt de Aiguaviva (4) ⚠️ | Aiguaviva › Gironès | 2 |
| Forêt de Aiguaviva (5) ⚠️ | Aiguaviva › Gironès | 2 |
| Bosc de Can Gros ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 2 |
| Forêt de Aiguaviva (12) ⚠️ | Aiguaviva › Gironès | 2 |
| Forêt de Aiguaviva (14) ⚠️ | Aiguaviva › Gironès | 2 |
| Forêt de Aiguaviva (15) ⚠️ | Aiguaviva › Gironès | 2 |
| Forêt de Riudellots de la Selva (4) ⚠️ | Riudellots de la Selva › la Selva (Gérone) | 2 |
| Forêt de Fornells de la Selva (3) ⚠️ | Fornells de la Selva › Gironès | 2 |
| Forêt de Torroella de Fluvià (3) ⚠️ | Torroella de Fluvià › Alt Empordà | 2 |
| Forêt de l'Escala ⚠️ | l'Escala › Alt Empordà | 2 |
| Forêt de Vilafant (2) ⚠️ | Santa Llogaia d'Àlguema › Alt Empordà | 2 |
| Forêt de Vilamalla ⚠️ | Vilamalla › Alt Empordà | 2 |
| Parc Schierbeck ⚠️ | Puigcerdà › Cerdanya (Gérone) | 2 |
| Forêt de Lladó (3) ⚠️ | Lladó › Alt Empordà | 2 |
| Forêt de Cruïlles, Monells i Sant Sadurní de l'Heura (5) ⚠️ | Cruïlles, Monells i Sant Sadurní de l'Heura › Baix Empordà | 2 |
| Forêt de Forallac (8) ⚠️ | Forallac › Baix Empordà | 2 |
| Forêt de Palau-sator (2) ⚠️ | Palau-sator › Baix Empordà | 2 |
| Forêt de Llambilles ⚠️ | Llambilles › Gironès | 2 |
| Forêt de Llambilles (4) ⚠️ | Llambilles › Gironès | 2 |
| Forêt de Llambilles (5) ⚠️ | Llambilles › Gironès | 2 |
| Parc Temàtic del Pirineu ⚠️ | Ripoll › Ripollès | 2 |
| Forêt de Celrà (5) ⚠️ | Celrà › Gironès | 2 |
| Forêt de Campllong (12) ⚠️ | Campllong › Gironès | 2 |
| Forêt de Llagostera (13) ⚠️ | Llagostera › Gironès | 2 |
| Forêt de Llagostera (15) ⚠️ | Llagostera › Gironès | 2 |
| Forêt de Llagostera (21) ⚠️ | Llagostera › Gironès | 2 |
| Forêt de Cassà de la Selva (11) ⚠️ | Cassà de la Selva › Gironès | 2 |
| Forêt de Cassà de la Selva (12) ⚠️ | Cassà de la Selva › Gironès | 2 |
| Forêt de Sant Andreu Salou (2) ⚠️ | Sant Andreu Salou › Gironès | 2 |
| Forêt de Caldes de Malavella (4) ⚠️ | Caldes de Malavella › la Selva (Gérone) | 2 |
| Forêt de Caldes de Malavella (5) ⚠️ | Caldes de Malavella › la Selva (Gérone) | 2 |
| Forêt de Caldes de Malavella (15) ⚠️ | Caldes de Malavella › la Selva (Gérone) | 2 |
| Forêt de Riudellots de la Selva (8) ⚠️ | Riudellots de la Selva › la Selva (Gérone) | 2 |
| Forêt de Fornells de la Selva (9) ⚠️ | Fornells de la Selva › Gironès | 2 |
| Forêt de Fornells de la Selva (10) ⚠️ | Fornells de la Selva › Gironès | 2 |
| Forêt de Palafrugell (23) ⚠️ | Palafrugell › Baix Empordà | 2 |
| Forêt de Garrigàs (10) ⚠️ | Pontós › Alt Empordà | 2 |
| Forêt de Palafrugell (79) ⚠️ | Palafrugell › Baix Empordà | 2 |
| Forêt de Calonge i Sant Antoni (7) ⚠️ | Calonge i Sant Antoni › Baix Empordà | 2 |
| Forêt de Palafrugell (87) ⚠️ | Palafrugell › Baix Empordà | 2 |
| Forêt de Palafrugell (89) ⚠️ | Palafrugell › Baix Empordà | 2 |
| Bosc de la Coma ⚠️ | Olot › Garrotxa | 2 |
| Forêt de Santa Coloma de Farners (4) ⚠️ | Santa Coloma de Farners › la Selva (Gérone) | 2 |
| Forêt de Vilobí d'Onyar (34) ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 2 |
| Forêt de Aiguaviva (20) ⚠️ | Aiguaviva › Gironès | 2 |
| Forêt de Riudellots de la Selva (13) ⚠️ | Riudellots de la Selva › la Selva (Gérone) | 2 |
| Forêt de Castell d'Aro, Platja d'Aro i s'Agaró (3) ⚠️ | Castell d'Aro, Platja d'Aro i s'Agaró › Baix Empordà | 2 |
| Forêt de Castell d'Aro, Platja d'Aro i s'Agaró (4) ⚠️ | Castell d'Aro, Platja d'Aro i s'Agaró › Baix Empordà | 2 |
| Forêt de Pardines (7) ⚠️ | Pardines › Ripollès | 2 |
| Forêt de Pardines (8) ⚠️ | Pardines › Ripollès | 2 |
| Forêt de Castell d'Aro, Platja d'Aro i s'Agaró (8) ⚠️ | Castell d'Aro, Platja d'Aro i s'Agaró › Baix Empordà | 2 |
| Forêt de Ribes de Freser (3) ⚠️ | Ribes de Freser › Ripollès | 2 |
| Forêt de Vall-llobrega ⚠️ | Vall-llobrega › Baix Empordà | 2 |
| Forêt de Palamós (4) ⚠️ | Palamós › Baix Empordà | 2 |
| Jardí botànic del Cap Roig ⚠️ | Mont-ras › Baix Empordà | 2 |
| Forêt de Quart (5) ⚠️ | Quart › Gironès | 2 |
| Forêt de Tossa de Mar (2) ⚠️ | Tossa de Mar › la Selva (Gérone) | 2 |
| Forêt de Girona (12) ⚠️ | Girona › Gironès | 2 |
| Forêt de Sant Hilari Sacalm (17) ⚠️ | Sant Hilari Sacalm › la Selva (Gérone) | 2 |
| Forêt de Cervià de Ter (2) ⚠️ | Cervià de Ter › Gironès | 2 |
| Forêt de Cervià de Ter (12) ⚠️ | Cervià de Ter › Gironès | 2 |
| Forêt de Cervià de Ter (20) ⚠️ | Cervià de Ter › Gironès | 2 |
| Forêt de la Vajol (35) ⚠️ | la Vajol › Alt Empordà | 2 |
| Forêt de la Vajol (36) ⚠️ | la Vajol › Alt Empordà | 2 |
| Bois de la Vajol ⚠️ | la Vajol › Alt Empordà | 2 |
| Forêt de la Vajol (44) ⚠️ | la Vajol › Alt Empordà | 2 |
| Forêt de Tortellà ⚠️ | Tortellà › Garrotxa | 2 |
| Forêt de Mont-ras (4) ⚠️ | Mont-ras › Baix Empordà | 2 |
| Bois de Mont-ras (4) ⚠️ | Mont-ras › Baix Empordà | 2 |
| Forêt de Cornellà del Terri (2) ⚠️ | Cornellà del Terri › Pla de l'Estany | 2 |
| Forêt de Fontcoberta ⚠️ | Fontcoberta › Pla de l'Estany | 2 |
| Bois de Sils (3) ⚠️ | Sils › la Selva (Gérone) | 2 |
| Forêt de Sils (4) ⚠️ | Sils › la Selva (Gérone) | 2 |
| Forêt de Sant Gregori (5) ⚠️ | Sant Gregori › Gironès | 2 |
| Forêt de Sant Jaume de Llierca ⚠️ | Sant Jaume de Llierca › Garrotxa | 2 |
| Forêt de Sant Jaume de Llierca (2) ⚠️ | Sant Jaume de Llierca › Garrotxa | 2 |
| Forêt de Alp (4) ⚠️ | Alp › Cerdanya (Gérone) | 2 |
| Forêt de Das (9) ⚠️ | Das › Cerdanya (Gérone) | 2 |
| Forêt de Das (10) ⚠️ | Das › Cerdanya (Gérone) | 2 |
| Forêt de Alp (19) ⚠️ | Alp › Cerdanya (Gérone) | 2 |
| Forêt de Alp (42) ⚠️ | Alp › Cerdanya (Gérone) | 2 |
| Forêt de Alp (44) ⚠️ | Alp › Cerdanya (Gérone) | 2 |
| Forêt de Alp (46) ⚠️ | Alp › Cerdanya (Gérone) | 2 |
| Forêt de Alp (47) ⚠️ | Alp › Cerdanya (Gérone) | 2 |
| Forêt de Alp (50) ⚠️ | Alp › Cerdanya (Gérone) | 2 |
| Forêt de Alp (55) ⚠️ | Alp › Cerdanya (Gérone) | 2 |
| Forêt de Alp (59) ⚠️ | Alp › Cerdanya (Gérone) | 2 |
| Forêt de Alp (68) ⚠️ | Alp › Cerdanya (Gérone) | 2 |
| Forêt de Alp (79) ⚠️ | Alp › Cerdanya (Gérone) | 2 |
| Forêt de Alp (80) ⚠️ | Alp › Cerdanya (Gérone) | 2 |
| Forêt de Alp (82) ⚠️ | Alp › Cerdanya (Gérone) | 2 |
| Forêt de Alp (83) ⚠️ | Alp › Cerdanya (Gérone) | 2 |
| Forêt de Queralbs (14) ⚠️ | Queralbs › Ripollès | 2 |
| Forêt de Girona (31) ⚠️ | Girona › Gironès | 2 |
| Forêt de Sarrià de Ter (10) ⚠️ | Sarrià de Ter › Gironès | 2 |
| Forêt de Sils (7) ⚠️ | Sils › la Selva (Gérone) | 2 |
| Forêt de Riudarenes (5) ⚠️ | Riudarenes › la Selva (Gérone) | 2 |
| Bois de Palafrugell (30) ⚠️ | Palafrugell › Baix Empordà | 2 |
| Bois de Forallac ⚠️ | Forallac › Baix Empordà | 2 |
| Bois de Lloret de Mar (2) ⚠️ | Lloret de Mar › la Selva (Gérone) | 2 |
| Forêt de Bescanó (8) ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 2 |
| Forêt de Amer (3) ⚠️ | Amer › la Selva (Gérone) | 2 |
| Bois de Cornellà del Terri ⚠️ | Cornellà del Terri › Pla de l'Estany | 2 |
| Forêt de Cistella (3) ⚠️ | Vilanant › Alt Empordà | 2 |
| Forêt de Cistella (4) ⚠️ | Cistella › Alt Empordà | 2 |
| Forêt de Vilanant (4) ⚠️ | Vilanant › Alt Empordà | 2 |
| Forêt de Cistella (5) ⚠️ | Cistella › Alt Empordà | 2 |
| Forêt de Cistella (6) ⚠️ | Cistella › Alt Empordà | 2 |
| Bois de Vilademuls (6) ⚠️ | Vilademuls › Pla de l'Estany | 2 |
| Bois de Vilademuls (7) ⚠️ | Vilademuls › Pla de l'Estany | 2 |
| Bois de Vilademuls (8) ⚠️ | Vilademuls › Pla de l'Estany | 2 |
| Bois de Sant Julià de Ramis (3) ⚠️ | Sant Julià de Ramis › Gironès | 2 |
| Bois de Torroella de Montgrí (2) ⚠️ | Torroella de Montgrí › Baix Empordà | 2 |
| Bois de Llers (5) ⚠️ | Llers › Alt Empordà | 2 |
| Forêt de Foixà (6) ⚠️ | Foixà › Baix Empordà | 2 |
| Bois de Vilopriu ⚠️ | Vilopriu › Baix Empordà | 2 |
| Forêt de Torroella de Montgrí (18) ⚠️ | Torroella de Montgrí › Baix Empordà | 2 |
| Forêt de Cantallops (2) ⚠️ | Cantallops › Alt Empordà | 2 |
| Forêt de Cantallops (5) ⚠️ | Cantallops › Alt Empordà | 2 |
| Forêt de Torroella de Montgrí (36) ⚠️ | Torroella de Montgrí › Baix Empordà | 2 |
| Forêt de l'Escala (7) ⚠️ | l'Escala › Alt Empordà | 2 |
| Forêt de Vilamacolum ⚠️ | Vilamacolum › Alt Empordà | 2 |
| Forêt de Santa Cristina d'Aro (9) ⚠️ | Santa Cristina d'Aro › Baix Empordà | 2 |
| Parc de Torroella de Montgrí (3) ⚠️ | Torroella de Montgrí › Baix Empordà | 2 |
| Forêt de Queralbs (17) ⚠️ | Queralbs › Ripollès | 2 |
| Forêt de Das (24) ⚠️ | Das › Cerdanya (Gérone) | 2 |
| Forêt de Riumors ⚠️ | Riumors › Alt Empordà | 2 |
| Camp de Mart ⚠️ | Girona › Gironès | 2 |
| Forêt de Siurana (5) ⚠️ | Siurana › Alt Empordà | 2 |
| Paratge El Vilar ⚠️ | Blanes › la Selva (Gérone) | 2 |
| Forêt de Pals ⚠️ | Pals › Baix Empordà | 2 |
| Forêt de Begur (8) ⚠️ | Begur › Baix Empordà | 2 |
| Forêt de Blanes (7) ⚠️ | Blanes › la Selva (Gérone) | 2 |
| Forêt de Ogassa (7) ⚠️ | Ogassa › Ripollès | 2 |
| Forêt de Setcases (17) ⚠️ | Setcases › Ripollès | 2 |
| Forêt de Setcases (19) ⚠️ | Setcases › Ripollès | 2 |
| Bois de Rupià (2) ⚠️ | Rupià › Baix Empordà | 2 |
| Parc de Cassà de la Selva (2) ⚠️ | Cassà de la Selva › Gironès | 2 |
| el riai ⚠️ | Olot › Garrotxa | 2 |
| Forêt de Massanes (13) ⚠️ | Massanes › la Selva (Gérone) | 2 |
| Forêt de Lloret de Mar (15) ⚠️ | Lloret de Mar › la Selva (Gérone) | 2 |
| Forêt de Vidreres (7) ⚠️ | Vidreres › la Selva (Gérone) | 2 |
| Forêt de Maçanet de la Selva (10) ⚠️ | Maçanet de la Selva › la Selva (Gérone) | 2 |
| Forêt de Maçanet de la Selva (11) ⚠️ | Maçanet de la Selva › la Selva (Gérone) | 2 |
| Bois de Mont-ras (7) ⚠️ | Mont-ras › Baix Empordà | 2 |
| Forêt de Brunyola i Sant Martí Sapresa (5) ⚠️ | Brunyola i Sant Martí Sapresa › la Selva (Gérone) | 2 |
| Forêt de Riudarenes (6) ⚠️ | Riudarenes › la Selva (Gérone) | 2 |
| Bois de Figueres ⚠️ | Figueres › Alt Empordà | 2 |
| Forêt de Sant Feliu de Guíxols (19) ⚠️ | Sant Feliu de Guíxols › Baix Empordà | 2 |
| Forêt de Girona (53) ⚠️ | Girona › Gironès | 2 |
| Bois de Quart (2) ⚠️ | Quart › Gironès | 2 |
| Forêt de Pont de Molins ⚠️ | Llers › Alt Empordà | 2 |
| Forêt de Fontanilles ⚠️ | Fontanilles › Baix Empordà | 2 |
| Forêt de Vidreres (8) ⚠️ | Vidreres › la Selva (Gérone) | 2 |
| Forêt de Vidreres (10) ⚠️ | Vidreres › la Selva (Gérone) | 2 |
| Forêt de Vidreres (11) ⚠️ | Vidreres › la Selva (Gérone) | 2 |
| Bois de Vidreres (10) ⚠️ | Vidreres › la Selva (Gérone) | 2 |
| Bois de Ribes de Freser ⚠️ | Ribes de Freser › Ripollès | 2 |
| Bois de Salt (6) ⚠️ | Salt › Gironès | 2 |
| Bois de Sant Gregori (10) ⚠️ | Sant Gregori › Gironès | 2 |
| Forêt de Canet d'Adri (7) ⚠️ | Sant Gregori › Gironès | 2 |
| Forêt de Forallac (27) ⚠️ | Forallac › Baix Empordà | 2 |
| Bois de Ullastret (5) ⚠️ | Ullastret › Baix Empordà | 2 |
| Bois de Regencós ⚠️ | Regencós › Baix Empordà | 2 |
| Bois de Sils (6) ⚠️ | Sils › la Selva (Gérone) | 2 |
| Forêt de Sils (23) ⚠️ | Sils › la Selva (Gérone) | 2 |
| Parc del Malatosquer ⚠️ | Olot › Garrotxa | 2 |
| Forêt de Ventalló (11) ⚠️ | Ventalló › Alt Empordà | 2 |
| Forêt de Garrigàs (13) ⚠️ | Garrigàs › Alt Empordà | 2 |
| Forêt de Molló (4) ⚠️ | Molló › Ripollès | 2 |
| Forêt de Olot (11) ⚠️ | Olot › Garrotxa | 2 |
| Forêt de Molló (6) ⚠️ | Molló › Ripollès | 2 |
| Forêt de Llagostera (41) ⚠️ | Llagostera › Gironès | 2 |
| Forêt de Bàscara (4) ⚠️ | Bàscara › Alt Empordà | 2 |
| Bois de Riudarenes (3) ⚠️ | Riudarenes › la Selva (Gérone) | 2 |
| Forêt de Santa Pau (9) ⚠️ | Santa Pau › Garrotxa | 2 |
| Forêt de Santa Pau (12) ⚠️ | Santa Pau › Garrotxa | 2 |
| Forêt de Llívia (3) ⚠️ | Llívia › Cerdanya (Gérone) | 2 |
| Forêt de Riells i Viabrea (5) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 2 |
| Forêt de Riells i Viabrea (12) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 2 |
| Forêt de Riells i Viabrea (13) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 2 |
| Bois de Santa Coloma de Farners (10) ⚠️ | Santa Coloma de Farners › la Selva (Gérone) | 2 |
| Bois de Vilobí d'Onyar (3) ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 2 |
| Bois de Palau-saverdera (6) ⚠️ | Palau-saverdera › Alt Empordà | 2 |
| Bois de Palau-saverdera (91) ⚠️ | Palau-saverdera › Alt Empordà | 2 |
| Bois de Pardines (5) ⚠️ | Pardines › Ripollès | 2 |
| Forêt de Vilademuls (12) ⚠️ | Vilademuls › Pla de l'Estany | 2 |
| Forêt de Ripoll (7) ⚠️ | Ripoll › Ripollès | 2 |
| Forêt de Sant Miquel de Fluvià (2) ⚠️ | Sant Miquel de Fluvià › Alt Empordà | 2 |
| Forêt de Sant Julià del Llor i Bonmatí (2) ⚠️ | Sant Julià del Llor i Bonmatí › la Selva (Gérone) | 2 |
| Forêt de Bescanó (14) ⚠️ | Bescanó › Gironès | 2 |
| Forêt de Ultramort ⚠️ | Ultramort › Baix Empordà | 2 |
| Forêt de Sant Gregori (22) ⚠️ | Sant Gregori › Gironès | 2 |
| Bois de Sant Julià del Llor i Bonmatí (3) ⚠️ | Sant Julià del Llor i Bonmatí › la Selva (Gérone) | 2 |
| Forêt de Sant Andreu Salou (10) ⚠️ | Sant Andreu Salou › Gironès | 2 |
| Forêt de Cassà de la Selva (33) ⚠️ | Cassà de la Selva › Gironès | 2 |
| Bois de Olot (19) ⚠️ | Olot › Garrotxa | 2 |
| Forêt de Bàscara (13) ⚠️ | Bàscara › Alt Empordà | 2 |
| Forêt de Bescanó (18) ⚠️ | Bescanó › Gironès | 2 |
| Forêt de Santa Cristina d'Aro (24) ⚠️ | Santa Cristina d'Aro › Baix Empordà | 2 |
| Bosc dels Casalots ⚠️ | Banyoles › Pla de l'Estany | 2 |
| Parc Monar ⚠️ | Salt › Gironès | 2 |
| Parc de Banyoles (25) ⚠️ | Banyoles › Pla de l'Estany | 2 |
| Forêt de Fornells de la Selva (19) ⚠️ | Fornells de la Selva › Gironès | 2 |
| Forêt de Aiguaviva (27) ⚠️ | Aiguaviva › Gironès | 2 |
| Forêt de Vilablareix (4) ⚠️ | Vilablareix › Gironès | 2 |
| Bosc de Ca n'Arbres ⚠️ | Aiguaviva › Gironès | 2 |
| Forêt de Girona (70) ⚠️ | Girona › Gironès | 2 |
| Forêt de Camós (8) ⚠️ | Camós › Pla de l'Estany | 2 |
| Forêt de Porqueres (10) ⚠️ | Porqueres › Pla de l'Estany | 2 |
| Forêt de Campllong (20) ⚠️ | Campllong › Gironès | 2 |
| Forêt de Girona (73) ⚠️ | Girona › Gironès | 2 |
| Forêt de Vilobí d'Onyar (45) ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 2 |
| Parc de Castelló d'Empúries (8) ⚠️ | Castelló d'Empúries › Alt Empordà | 2 |
| Forêt de Sant Julià de Ramis (11) ⚠️ | Sant Julià de Ramis › Gironès | 2 |
| Forêt de Sant Julià de Ramis (12) ⚠️ | Sant Julià de Ramis › Gironès | 2 |
| Bois de la Cellera de Ter (10) ⚠️ | la Cellera de Ter › la Selva (Gérone) | 2 |
| Bois de Amer (3) ⚠️ | Amer › la Selva (Gérone) | 2 |
| Bois de la Cellera de Ter (12) ⚠️ | la Cellera de Ter › la Selva (Gérone) | 2 |
| Forêt de la Cellera de Ter (32) ⚠️ | la Cellera de Ter › la Selva (Gérone) | 2 |
| Bois de Vilademuls (19) ⚠️ | Vilademuls › Pla de l'Estany | 2 |
| Forêt de Vidrà (4) ⚠️ | Vidrà › Osona (Gérone) | 2 |
| Forêt de Bescanó (25) ⚠️ | Bescanó › Gironès | 2 |
| Forêt de Figueres (5) ⚠️ | Figueres › Alt Empordà | 2 |
| Forêt de Sant Julià de Ramis (13) ⚠️ | Sant Julià de Ramis › Gironès | 2 |
| Forêt de Mieres (5) ⚠️ | Mieres › Garrotxa | 2 |
| Forêt de Porqueres (17) ⚠️ | Porqueres › Pla de l'Estany | 2 |
| Forêt de Porqueres (18) ⚠️ | Porqueres › Pla de l'Estany | 2 |
| Forêt de la Jonquera (19) ⚠️ | la Jonquera › Alt Empordà | 2 |
| Forêt de Begur (33) ⚠️ | Begur › Baix Empordà | 2 |
| Forêt de Palafrugell (120) ⚠️ | Palafrugell › Baix Empordà | 2 |
| Càmping Caravaning Pinell ⚠️ | Castell d'Aro, Platja d'Aro i s'Agaró › Baix Empordà | 2 |
| Forêt de Sant Feliu de Guíxols (24) ⚠️ | Sant Feliu de Guíxols › Baix Empordà | 2 |
| Forêt de Tossa de Mar (15) ⚠️ | Tossa de Mar › la Selva (Gérone) | 2 |
| Forêt de Lloret de Mar (29) ⚠️ | Lloret de Mar › la Selva (Gérone) | 2 |
| Forêt de Lloret de Mar (33) ⚠️ | Lloret de Mar › la Selva (Gérone) | 2 |
| Forêt de Roses (15) ⚠️ | Roses › Alt Empordà | 2 |
| Forêt de el Port de la Selva (16) ⚠️ | el Port de la Selva › Alt Empordà | 2 |
| Forêt de el Port de la Selva (17) ⚠️ | el Port de la Selva › Alt Empordà | 2 |
| Forêt de Llançà (20) ⚠️ | Llançà › Alt Empordà | 2 |
| Forêt de Llançà (21) ⚠️ | Llançà › Alt Empordà | 2 |
| Forêt de Colera (9) ⚠️ | Colera › Alt Empordà | 2 |
| Forêt de Roses (26) ⚠️ | Roses › Alt Empordà | 2 |
| Forêt de Setcases (53) ⚠️ | Setcases › Ripollès | 2 |
| Forêt de Ripoll (17) ⚠️ | Ripoll › Ripollès | 2 |
| Forêt de Ripoll (18) ⚠️ | Ripoll › Ripollès | 2 |
| Forêt de Ripoll (24) ⚠️ | Ripoll › Ripollès | 2 |
| Forêt de Ripoll (33) ⚠️ | Ripoll › Ripollès | 2 |
| Forêt de Camprodon (18) ⚠️ | Camprodon › Ripollès | 2 |
| Forêt de la Vall de Bianya (8) ⚠️ | la Vall de Bianya › Garrotxa | 2 |
| Forêt de Sant Joan les Fonts (6) ⚠️ | Sant Joan les Fonts › Garrotxa | 2 |
| Forêt de Sant Joan les Fonts (8) ⚠️ | Sant Joan les Fonts › Garrotxa | 2 |
| Forêt de Sant Joan les Fonts (9) ⚠️ | Sant Joan les Fonts › Garrotxa | 2 |
| Forêt de Sant Joan les Fonts (10) ⚠️ | Sant Joan les Fonts › Garrotxa | 2 |
| Forêt de Besalú (10) ⚠️ | Besalú › Garrotxa | 2 |
| Forêt de Besalú (11) ⚠️ | Besalú › Garrotxa | 2 |
| Forêt de Besalú (12) ⚠️ | Besalú › Garrotxa | 2 |
| Forêt de Alp (97) ⚠️ | Alp › Cerdanya (Gérone) | 2 |
| Forêt de Castell d'Aro, Platja d'Aro i s'Agaró (31) ⚠️ | Castell d'Aro, Platja d'Aro i s'Agaró › Baix Empordà | 2 |
| Forêt de Castell d'Aro, Platja d'Aro i s'Agaró (34) ⚠️ | Castell d'Aro, Platja d'Aro i s'Agaró › Baix Empordà | 2 |
| Forêt de Calonge i Sant Antoni (34) ⚠️ | Calonge i Sant Antoni › Baix Empordà | 2 |
| Forêt de Torroella de Montgrí (76) ⚠️ | Torroella de Montgrí › Baix Empordà | 2 |
| Forêt de Tossa de Mar (30) ⚠️ | Tossa de Mar › la Selva (Gérone) | 2 |
| Forêt de Lloret de Mar (48) ⚠️ | Lloret de Mar › la Selva (Gérone) | 2 |
| Forêt de Maçanet de la Selva (17) ⚠️ | Maçanet de la Selva › la Selva (Gérone) | 2 |
| Forêt de Toses (16) ⚠️ | Toses › Ripollès | 2 |
| Forêt de Toses (17) ⚠️ | Toses › Ripollès | 2 |
| Forêt de Toses (21) ⚠️ | Toses › Ripollès | 2 |
| Forêt de Ribes de Freser (12) ⚠️ | Ribes de Freser › Ripollès | 2 |
| Forêt de Ribes de Freser (15) ⚠️ | Ribes de Freser › Ripollès | 2 |
| Forêt de Ribes de Freser (19) ⚠️ | Ribes de Freser › Ripollès | 2 |
| Forêt de Palamós (21) ⚠️ | Palamós › Baix Empordà | 2 |
| Forêt de Pals (14) ⚠️ | Pals › Baix Empordà | 2 |
| Forêt de Girona (74) ⚠️ | Girona › Gironès | 2 |
| Forêt de Pals (18) ⚠️ | Pals › Baix Empordà | 2 |
| Bois de Torroella de Montgrí (14) ⚠️ | Torroella de Montgrí › Baix Empordà | 2 |
| Forêt de Torroella de Montgrí (87) ⚠️ | Torroella de Montgrí › Baix Empordà | 2 |
| Forêt de Pals (30) ⚠️ | Pals › Baix Empordà | 2 |
| Forêt de Pals (32) ⚠️ | Pals › Baix Empordà | 2 |
| Forêt de Pals (49) ⚠️ | Pals › Baix Empordà | 2 |
| Forêt de Torrent (4) ⚠️ | Torrent › Baix Empordà | 2 |
| Bois de Vilallonga de Ter (6) ⚠️ | Vilallonga de Ter › Ripollès | 2 |
| Bois de Fontanals de Cerdanya ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 2 |
| Forêt de les Llosses (70) ⚠️ | les Llosses › Ripollès | 2 |
| Forêt de Palafrugell (126) ⚠️ | Palafrugell › Baix Empordà | 2 |
| Forêt de Sant Feliu de Pallerols (5) ⚠️ | Sant Feliu de Pallerols › Garrotxa | 2 |
| Forêt de les Planes d'Hostoles (6) ⚠️ | les Planes d'Hostoles › Garrotxa | 2 |
| Forêt de les Planes d'Hostoles (7) ⚠️ | les Planes d'Hostoles › Garrotxa | 2 |
| Forêt de les Planes d'Hostoles (8) ⚠️ | les Planes d'Hostoles › Garrotxa | 2 |
| Forêt de les Planes d'Hostoles (9) ⚠️ | les Planes d'Hostoles › Garrotxa | 2 |
| Forêt de Pals (70) ⚠️ | Pals › Baix Empordà | 2 |
| Forêt de Pals (79) ⚠️ | Pals › Baix Empordà | 2 |
| Forêt de Fontanals de Cerdanya (8) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 2 |
| Forêt de Fontanals de Cerdanya (9) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 2 |
| Forêt de Puigcerdà (8) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 2 |
| Forêt de Puigcerdà (13) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 2 |
| Forêt de Bolvir (5) ⚠️ | Bolvir › Cerdanya (Gérone) | 2 |
| Forêt de Bolvir (14) ⚠️ | Bolvir › Cerdanya (Gérone) | 2 |
| Forêt de Bolvir (15) ⚠️ | Bolvir › Cerdanya (Gérone) | 2 |
| Forêt de Puigcerdà (36) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 2 |
| Forêt de Puigcerdà (53) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 2 |
| Forêt de Puigcerdà (63) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 2 |
| Forêt de Puigcerdà (67) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 2 |
| Forêt de Puigcerdà (69) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 2 |
| Forêt de Puigcerdà (70) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 2 |
| Forêt de Puigcerdà (89) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 2 |
| Forêt de Puigcerdà (100) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 2 |
| Forêt de Puigcerdà (105) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 2 |
| Forêt de Puigcerdà (108) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 2 |
| Forêt de Fontanals de Cerdanya (14) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 2 |
| Forêt de Guils de Cerdanya (11) ⚠️ | Guils de Cerdanya › Cerdanya (Gérone) | 2 |
| Forêt de Guils de Cerdanya (15) ⚠️ | Guils de Cerdanya › Cerdanya (Gérone) | 2 |
| Forêt de Guils de Cerdanya (28) ⚠️ | Guils de Cerdanya › Cerdanya (Gérone) | 2 |
| Forêt de Ger (11) ⚠️ | Ger › Cerdanya (Gérone) | 2 |
| Forêt de Ger (19) ⚠️ | Isòvol › Cerdanya (Gérone) | 2 |
| Forêt de Guils de Cerdanya (38) ⚠️ | Guils de Cerdanya › Cerdanya (Gérone) | 2 |
| Forêt de Fontanals de Cerdanya (21) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 2 |
| Forêt de Fontanals de Cerdanya (54) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 2 |
| Forêt de Fontanals de Cerdanya (55) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 2 |
| Forêt de Alp (103) ⚠️ | Alp › Cerdanya (Gérone) | 2 |
| Forêt de Alp (104) ⚠️ | Alp › Cerdanya (Gérone) | 2 |
| Forêt de Alp (106) ⚠️ | Alp › Cerdanya (Gérone) | 2 |
| Forêt de Urús (6) ⚠️ | Urús › Cerdanya (Gérone) | 2 |
| Forêt de les Llosses (93) ⚠️ | les Llosses › Ripollès | 2 |
| Forêt de Campelles (6) ⚠️ | Campelles › Ripollès | 2 |
| Forêt de Campdevànol (29) ⚠️ | Campdevànol › Ripollès | 2 |
| Forêt de Gombrèn (49) ⚠️ | Gombrèn › Ripollès | 2 |
| Forêt de Campdevànol (31) ⚠️ | Campdevànol › Ripollès | 2 |
| Forêt de Campdevànol (34) ⚠️ | Campdevànol › Ripollès | 2 |
| Forêt de Gombrèn (60) ⚠️ | Gombrèn › Ripollès | 2 |
| Forêt de Campdevànol (50) ⚠️ | Campdevànol › Ripollès | 2 |
| Forêt de Ribes de Freser (26) ⚠️ | Ribes de Freser › Ripollès | 2 |
| Forêt de Ripoll (45) ⚠️ | Ripoll › Ripollès | 2 |
| Forêt de Ripoll (46) ⚠️ | Ripoll › Ripollès | 2 |
| Forêt de Campdevànol (70) ⚠️ | Ripoll › Ripollès | 2 |
| Forêt de Ripoll (48) ⚠️ | Ripoll › Ripollès | 2 |
| Forêt de Ogassa (13) ⚠️ | Ogassa › Ripollès | 2 |
| Forêt de Campelles (8) ⚠️ | Campelles › Ripollès | 2 |
| Forêt de Ripoll (59) ⚠️ | Ripoll › Ripollès | 2 |
| Forêt de Ripoll (65) ⚠️ | Ripoll › Ripollès | 2 |
| Forêt de Ripoll (66) ⚠️ | Ripoll › Ripollès | 2 |
| Forêt de Ripoll (68) ⚠️ | Ripoll › Ripollès | 2 |
| Forêt de Vallfogona de Ripollès (18) ⚠️ | Vallfogona de Ripollès › Ripollès | 2 |
| Forêt de Vallfogona de Ripollès (19) ⚠️ | Vallfogona de Ripollès › Ripollès | 2 |
| Forêt de Sales de Llierca (7) ⚠️ | Sales de Llierca › Garrotxa | 2 |
| Forêt de Montagut i Oix (10) ⚠️ | Montagut i Oix › Garrotxa | 2 |
| Forêt de Montagut i Oix (34) ⚠️ | Montagut i Oix › Garrotxa | 2 |
| Forêt de Montagut i Oix (37) ⚠️ | Montagut i Oix › Garrotxa | 2 |
| Forêt de Montagut i Oix (39) ⚠️ | Montagut i Oix › Garrotxa | 2 |
| Forêt de Montagut i Oix (66) ⚠️ | Montagut i Oix › Garrotxa | 2 |
| Forêt de Montagut i Oix (67) ⚠️ | Montagut i Oix › Garrotxa | 2 |
| Forêt de Montagut i Oix (69) ⚠️ | Montagut i Oix › Garrotxa | 2 |
| Forêt de Albanyà (14) ⚠️ | Albanyà › Alt Empordà | 2 |
| Forêt de Sant Llorenç de la Muga (20) ⚠️ | Sant Llorenç de la Muga › Alt Empordà | 2 |
| Forêt de Sant Llorenç de la Muga (21) ⚠️ | Sant Llorenç de la Muga › Alt Empordà | 2 |
| Forêt de la Vajol (49) ⚠️ | la Vajol › Alt Empordà | 2 |
| Forêt de la Vajol (51) ⚠️ | la Vajol › Alt Empordà | 2 |
| Forêt de la Vajol (52) ⚠️ | la Vajol › Alt Empordà | 2 |
| Forêt de Albanyà (26) ⚠️ | Albanyà › Alt Empordà | 2 |
| Forêt de Albanyà (31) ⚠️ | Albanyà › Alt Empordà | 2 |
| Forêt de Espolla (11) ⚠️ | Espolla › Alt Empordà | 2 |
| Forêt de la Jonquera (27) ⚠️ | la Jonquera › Alt Empordà | 2 |
| Forêt de Espolla (16) ⚠️ | Espolla › Alt Empordà | 2 |
| Forêt de Camprodon (28) ⚠️ | Camprodon › Ripollès | 2 |
| Forêt de Molló (10) ⚠️ | Molló › Ripollès | 2 |
| Forêt de Molló (13) ⚠️ | Molló › Ripollès | 2 |
| Forêt de Molló (17) ⚠️ | Molló › Ripollès | 2 |
| Forêt de Molló (31) ⚠️ | Molló › Ripollès | 2 |
| Forêt de Molló (41) ⚠️ | Molló › Ripollès | 2 |
| Forêt de Molló (42) ⚠️ | Molló › Ripollès | 2 |
| Forêt de Molló (44) ⚠️ | Molló › Ripollès | 2 |
| Forêt de Molló (61) ⚠️ | Molló › Ripollès | 2 |
| Forêt de Molló (63) ⚠️ | Molló › Ripollès | 2 |
| Forêt de Setcases (75) ⚠️ | Setcases › Ripollès | 2 |
| Forêt de Molló (68) ⚠️ | Molló › Ripollès | 2 |
| Forêt de Setcases (79) ⚠️ | Setcases › Ripollès | 2 |
| Forêt de Setcases (80) ⚠️ | Setcases › Ripollès | 2 |
| Forêt de Setcases (84) ⚠️ | Setcases › Ripollès | 2 |
| Forêt de Setcases (92) ⚠️ | Setcases › Ripollès | 2 |
| Forêt de Setcases (99) ⚠️ | Setcases › Ripollès | 2 |
| Forêt de Molló (78) ⚠️ | Molló › Ripollès | 2 |
| Forêt de Camprodon (43) ⚠️ | Camprodon › Ripollès | 2 |
| Forêt de Llanars (15) ⚠️ | Llanars › Ripollès | 2 |
| Forêt de Vilallonga de Ter (9) ⚠️ | Vilallonga de Ter › Ripollès | 2 |
| Forêt de Vilallonga de Ter (16) ⚠️ | Vilallonga de Ter › Ripollès | 2 |
| Forêt de Vilallonga de Ter (19) ⚠️ | Vilallonga de Ter › Ripollès | 2 |
| Forêt de Vilallonga de Ter (20) ⚠️ | Vilallonga de Ter › Ripollès | 2 |
| Forêt de Setcases (106) ⚠️ | Setcases › Ripollès | 2 |
| Forêt de Planoles (8) ⚠️ | Planoles › Ripollès | 2 |
| Forêt de Planoles (11) ⚠️ | Planoles › Ripollès | 2 |
| Forêt de Ribes de Freser (43) ⚠️ | Ribes de Freser › Ripollès | 2 |
| Forêt de Guils de Cerdanya (46) ⚠️ | Guils de Cerdanya › Cerdanya (Gérone) | 2 |
| Forêt de Meranges (18) ⚠️ | Meranges › Cerdanya (Gérone) | 2 |
| Forêt de Meranges (25) ⚠️ | Meranges › Cerdanya (Gérone) | 2 |
| Forêt de Camprodon (48) ⚠️ | Camprodon › Ripollès | 2 |
| Forêt de Camprodon (50) ⚠️ | Camprodon › Ripollès | 2 |
| Forêt de Sant Pau de Segúries (4) ⚠️ | Sant Pau de Segúries › Ripollès | 2 |
| Forêt de Sant Pau de Segúries (7) ⚠️ | Sant Pau de Segúries › Ripollès | 2 |
| Forêt de Sant Joan de les Abadesses (15) ⚠️ | Sant Joan de les Abadesses › Ripollès | 2 |
| Forêt de Sant Joan de les Abadesses (23) ⚠️ | Sant Joan de les Abadesses › Ripollès | 2 |
| Forêt de Sant Joan de les Abadesses (27) ⚠️ | Sant Joan de les Abadesses › Ripollès | 2 |
| Forêt de Sant Joan de les Abadesses (29) ⚠️ | Sant Joan de les Abadesses › Ripollès | 2 |
| Forêt de Sant Joan de les Abadesses (32) ⚠️ | Sant Joan de les Abadesses › Ripollès | 2 |
| Forêt de Sant Joan de les Abadesses (33) ⚠️ | Sant Joan de les Abadesses › Ripollès | 2 |
| Forêt de Sant Joan de les Abadesses (36) ⚠️ | Sant Joan de les Abadesses › Ripollès | 2 |
| Forêt de la Vall de Bianya (23) ⚠️ | la Vall de Bianya › Garrotxa | 2 |
| Forêt de la Vall de Bianya (24) ⚠️ | la Vall de Bianya › Garrotxa | 2 |
| Forêt de la Vall de Bianya (30) ⚠️ | la Vall de Bianya › Garrotxa | 2 |
| Forêt de Camprodon (53) ⚠️ | Camprodon › Ripollès | 2 |
| Forêt de Camprodon (56) ⚠️ | Camprodon › Ripollès | 2 |
| Forêt de Ripoll (89) ⚠️ | Ripoll › Ripollès | 2 |
| Forêt de Vidrà (8) ⚠️ | Vidrà › Osona (Gérone) | 2 |
| Forêt de la Cellera de Ter (33) ⚠️ | la Cellera de Ter › la Selva (Gérone) | 2 |
| Parc de les Mores ⚠️ | Olot › Garrotxa | 2 |
| Forêt de Olot (21) ⚠️ | Olot › Garrotxa | 2 |
| Forêt de Olot (22) ⚠️ | Olot › Garrotxa | 2 |
| Forêt de Sant Joan les Fonts (15) ⚠️ | Sant Joan les Fonts › Garrotxa | 2 |
| Forêt de Camprodon (57) ⚠️ | Camprodon › Ripollès | 2 |
| Forêt de Montagut i Oix (79) ⚠️ | Montagut i Oix › Garrotxa | 2 |
| Forêt de Santa Coloma de Farners (20) ⚠️ | Santa Coloma de Farners › la Selva (Gérone) | 2 |
| Forêt de Santa Coloma de Farners (21) ⚠️ | Santa Coloma de Farners › la Selva (Gérone) | 2 |
| Forêt de Sant Hilari Sacalm (30) ⚠️ | Sant Hilari Sacalm › la Selva (Gérone) | 2 |
| Forêt de Sant Hilari Sacalm (31) ⚠️ | Sant Hilari Sacalm › la Selva (Gérone) | 2 |
| Forêt de Sant Hilari Sacalm (32) ⚠️ | Sant Hilari Sacalm › la Selva (Gérone) | 2 |
| Forêt de Arbúcies (25) ⚠️ | Arbúcies › la Selva (Gérone) | 2 |
| Forêt de Arbúcies (26) ⚠️ | Arbúcies › la Selva (Gérone) | 2 |
| Forêt de Arbúcies (38) ⚠️ | Arbúcies › la Selva (Gérone) | 2 |
| Forêt de Osor (24) ⚠️ | Osor › la Selva (Gérone) | 2 |
| Forêt de el Port de la Selva (33) ⚠️ | el Port de la Selva › Alt Empordà | 2 |
| Forêt de Palau-saverdera (4) ⚠️ | Palau-saverdera › Alt Empordà | 2 |
| Forêt de la Selva de Mar (7) ⚠️ | la Selva de Mar › Alt Empordà | 2 |
| Forêt de el Port de la Selva (38) ⚠️ | el Port de la Selva › Alt Empordà | 2 |
| Forêt de la Selva de Mar (11) ⚠️ | la Selva de Mar › Alt Empordà | 2 |
| Forêt de Palau-saverdera (9) ⚠️ | Palau-saverdera › Alt Empordà | 2 |
| Forêt de Roses (35) ⚠️ | Roses › Alt Empordà | 2 |
| Forêt de Roses (38) ⚠️ | Roses › Alt Empordà | 2 |
| Forêt de Vilajuïga ⚠️ | Vilajuïga › Alt Empordà | 2 |
| Forêt de Vilamaniscle ⚠️ | Vilamaniscle › Alt Empordà | 2 |
| Forêt de Vilamaniscle (3) ⚠️ | Vilamaniscle › Alt Empordà | 2 |
| Forêt de Peralada (11) ⚠️ | Peralada › Alt Empordà | 2 |
| Forêt de Cabanes (6) ⚠️ | Cabanes › Alt Empordà | 2 |
| Forêt de Cabanes (8) ⚠️ | Cabanes › Alt Empordà | 2 |
| Forêt de Pont de Molins (6) ⚠️ | Pont de Molins › Alt Empordà | 2 |
| Forêt de Pont de Molins (9) ⚠️ | Pont de Molins › Alt Empordà | 2 |
| Forêt de Castelló d'Empúries (14) ⚠️ | Castelló d'Empúries › Alt Empordà | 2 |
| Forêt de Castelló d'Empúries (17) ⚠️ | Castelló d'Empúries › Alt Empordà | 2 |
| Forêt de Sant Pere Pescador (3) ⚠️ | Sant Pere Pescador › Alt Empordà | 2 |
| Forêt de el Far d'Empordà (3) ⚠️ | el Far d'Empordà › Alt Empordà | 2 |
| Forêt de Bescanó (28) ⚠️ | Bescanó › Gironès | 2 |
| Forêt de Bescanó (29) ⚠️ | Anglès › la Selva (Gérone) | 2 |
| Forêt de Sant Gregori (27) ⚠️ | Sant Gregori › Gironès | 2 |
| Forêt de Amer (5) ⚠️ | Amer › la Selva (Gérone) | 2 |
| Forêt de Toses (52) ⚠️ | Toses › Ripollès | 2 |
| Forêt de Toses (54) ⚠️ | Toses › Ripollès | 2 |
| Forêt de Toses (59) ⚠️ | Toses › Ripollès | 2 |
| Forêt de Santa Pau (23) ⚠️ | Santa Pau › Garrotxa | 2 |
| Forêt de Santa Pau (24) ⚠️ | Santa Pau › Garrotxa | 2 |
| Forêt de Ullà ⚠️ | Gualta › Baix Empordà | 2 |
| Forêt de Sant Julià de Ramis (20) ⚠️ | Sant Julià de Ramis › Gironès | 2 |
| Forêt de Sant Julià de Ramis (21) ⚠️ | Sant Julià de Ramis › Gironès | 2 |
| Forêt de la Vall d'en Bas (24) ⚠️ | la Vall d'en Bas › Garrotxa | 2 |
| Forêt de la Vall d'en Bas (27) ⚠️ | les Preses › Garrotxa | 2 |
| Forêt de Queralbs (37) ⚠️ | Queralbs › Ripollès | 2 |
| Forêt de Susqueda (8) ⚠️ | Susqueda › la Selva (Gérone) | 2 |
| Forêt de Sant Joan de les Abadesses (38) ⚠️ | Sant Joan de les Abadesses › Ripollès | 2 |
| Forêt de Sant Joan de les Abadesses (43) ⚠️ | Sant Joan de les Abadesses › Ripollès | 2 |
| Forêt de Sant Jordi Desvalls (10) ⚠️ | Sant Jordi Desvalls › Gironès | 2 |
| Forêt de Hostalric (3) ⚠️ | Hostalric › la Selva (Gérone) | 2 |
| Forêt de Hostalric (4) ⚠️ | Hostalric › la Selva (Gérone) | 2 |
| Forêt de Massanes (21) ⚠️ | Massanes › la Selva (Gérone) | 2 |
| Forêt de Massanes (24) ⚠️ | Massanes › la Selva (Gérone) | 2 |
| Forêt de Sant Feliu de Buixalleu (34) ⚠️ | Sant Feliu de Buixalleu › la Selva (Gérone) | 2 |
| Forêt de Sant Feliu de Buixalleu (35) ⚠️ | Sant Feliu de Buixalleu › la Selva (Gérone) | 2 |
| Forêt de Riells i Viabrea (28) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 2 |
| Forêt de Riells i Viabrea (31) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 2 |
| Forêt de Riells i Viabrea (37) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 2 |
| Forêt de Riells i Viabrea (40) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 2 |
| Forêt de Breda ⚠️ | Breda › la Selva (Gérone) | 2 |
| Forêt de la Vall d'en Bas (29) ⚠️ | la Vall d'en Bas › Garrotxa | 2 |
| Forêt de la Vall d'en Bas (33) ⚠️ | la Vall d'en Bas › Garrotxa | 2 |
| Forêt de la Vall d'en Bas (41) ⚠️ | la Vall d'en Bas › Garrotxa | 2 |
| Forêt de la Vall d'en Bas (42) ⚠️ | la Vall d'en Bas › Garrotxa | 2 |
| Forêt de la Vall d'en Bas (49) ⚠️ | la Vall d'en Bas › Garrotxa | 2 |
| Forêt de la Vall d'en Bas (54) ⚠️ | la Vall d'en Bas › Garrotxa | 2 |
| Forêt de la Vall d'en Bas (70) ⚠️ | la Vall d'en Bas › Garrotxa | 2 |
| Forêt de Viladrau (58) ⚠️ | Viladrau › Osona (Gérone) | 2 |
| Forêt de Viladrau (59) ⚠️ | Viladrau › Osona (Gérone) | 2 |
| Forêt de Olot (26) ⚠️ | Olot › Garrotxa | 2 |
| Forêt de Olot (27) ⚠️ | Olot › Garrotxa | 2 |
| Forêt de Sant Joan les Fonts (21) ⚠️ | Sant Joan les Fonts › Garrotxa | 2 |
| Bois de Ullastret (7) ⚠️ | Ullastret › Baix Empordà | 2 |
| Forêt de Sant Feliu de Guíxols (38) ⚠️ | Sant Feliu de Guíxols › Baix Empordà | 2 |
| Forêt de Sant Feliu de Guíxols (39) ⚠️ | Sant Feliu de Guíxols › Baix Empordà | 2 |
| Forêt de Sant Ferriol (12) ⚠️ | Sant Ferriol › Garrotxa | 2 |
| Forêt de Queralbs (46) ⚠️ | Queralbs › Ripollès | 2 |
| Forêt de Caldes de Malavella (32) ⚠️ | Caldes de Malavella › la Selva (Gérone) | 2 |
| Forêt de Peralada (21) ⚠️ | Peralada › Alt Empordà | 2 |
| Forêt de Cabanelles (8) ⚠️ | Cabanelles › Alt Empordà | 2 |
| Forêt de Cabanelles (13) ⚠️ | Cabanelles › Alt Empordà | 2 |
| Forêt de Crespià (6) ⚠️ | Crespià › Pla de l'Estany | 2 |
| Forêt de Vilademuls (31) ⚠️ | Vilademuls › Pla de l'Estany | 2 |
| Forêt de Vilademuls (35) ⚠️ | Vilademuls › Pla de l'Estany | 2 |
| Forêt de Sant Miquel de Fluvià (5) ⚠️ | Sant Miquel de Fluvià › Alt Empordà | 2 |
| Forêt de Argelaguer (12) ⚠️ | Argelaguer › Garrotxa | 2 |
| Forêt de Besalú (15) ⚠️ | Besalú › Garrotxa | 2 |
| Forêt de Montagut i Oix (85) ⚠️ | Montagut i Oix › Garrotxa | 2 |
| Forêt de Torroella de Fluvià (12) ⚠️ | Torroella de Fluvià › Alt Empordà | 2 |
| Forêt de Ventalló (15) ⚠️ | Ventalló › Alt Empordà | 2 |
| Forêt de Ventalló (20) ⚠️ | Ventalló › Alt Empordà | 2 |
| Forêt de Sant Miquel de Fluvià (7) ⚠️ | Sant Miquel de Fluvià › Alt Empordà | 2 |
| Forêt de Sant Pere Pescador (11) ⚠️ | Sant Pere Pescador › Alt Empordà | 2 |
| Forêt de Ripoll (95) ⚠️ | Ripoll › Ripollès | 2 |
| Forêt de Ripoll (102) ⚠️ | Ripoll › Ripollès | 2 |
| Forêt de Fontanals de Cerdanya (59) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 2 |
| Forêt de Fontanals de Cerdanya (60) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 2 |
| Forêt de Fontanals de Cerdanya (61) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 2 |
| Parc de Amer ⚠️ | Amer › la Selva (Gérone) | 1 |
| Parc de la Mina Cristal·lina ⚠️ | Blanes › la Selva (Gérone) | 1 |
| L'Era del Cigarro ⚠️ | Salt › Gironès | 1 |
| Forêt de Blanes (4) ⚠️ | Blanes › la Selva (Gérone) | 1 |
| Parc de Girona ⚠️ | Girona › Gironès | 1 |
| Parc de la Comtessa Ermessenda ⚠️ | Girona › Gironès | 1 |
| Plaça de Fra Ignasi Barnoya i Oms ⚠️ | Girona › Gironès | 1 |
| Parc de Francesc Sabaté i Llopart ⚠️ | Girona › Gironès | 1 |
| Parc de Vista Alegre ⚠️ | Girona › Gironès | 1 |
| Parc de Xon Ferrer ⚠️ | Blanes › la Selva (Gérone) | 1 |
| Bois de Anglès ⚠️ | Anglès › la Selva (Gérone) | 1 |
| Forêt de la Cellera de Ter (5) ⚠️ | la Cellera de Ter › la Selva (Gérone) | 1 |
| Forêt de Llagostera (2) ⚠️ | Llagostera › Gironès | 1 |
| Forêt de Llagostera (3) ⚠️ | Llagostera › Gironès | 1 |
| les Bòries ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 1 |
| Forêt de Aiguaviva ⚠️ | Aiguaviva › Gironès | 1 |
| Forêt de les Llosses ⚠️ | les Llosses › Ripollès | 1 |
| Forêt de Viladrau (3) ⚠️ | Viladrau › Osona (Gérone) | 1 |
| Forêt de les Llosses (3) ⚠️ | les Llosses › Ripollès | 1 |
| Forêt de les Llosses (5) ⚠️ | les Llosses › Ripollès | 1 |
| Forêt de Viladrau (4) ⚠️ | Viladrau › Osona (Gérone) | 1 |
| Bois de Amer ⚠️ | Amer › la Selva (Gérone) | 1 |
| Bois de Girona (4) ⚠️ | Girona › Gironès | 1 |
| Parc Artigues ⚠️ | Vilamalla › Alt Empordà | 1 |
| Forêt de les Llosses (10) ⚠️ | les Llosses › Ripollès | 1 |
| Forêt de Sant Hilari Sacalm (11) ⚠️ | Sant Hilari Sacalm › la Selva (Gérone) | 1 |
| Forêt de Vilademuls (4) ⚠️ | Vilademuls › Pla de l'Estany | 1 |
| Forêt de Quart ⚠️ | Quart › Gironès | 1 |
| Forêt de Alp ⚠️ | Alp › Cerdanya (Gérone) | 1 |
| Forêt de la Jonquera (5) ⚠️ | la Jonquera › Alt Empordà | 1 |
| Forêt de Espinelves (5) ⚠️ | Espinelves › Osona (Gérone) | 1 |
| Forêt de Canet d'Adri (2) ⚠️ | Canet d'Adri › Gironès | 1 |
| Forêt de Vilobí d'Onyar (5) ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 1 |
| Forêt de Vilobí d'Onyar (6) ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 1 |
| Forêt de Vilobí d'Onyar (7) ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 1 |
| Forêt de Vilobí d'Onyar (10) ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 1 |
| Forêt de Vilobí d'Onyar (11) ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 1 |
| Forêt de Vilobí d'Onyar (13) ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 1 |
| Forêt de Sant Hilari Sacalm (16) ⚠️ | Sant Hilari Sacalm › la Selva (Gérone) | 1 |
| Forêt de Vilobí d'Onyar (16) ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 1 |
| Forêt de Aiguaviva (7) ⚠️ | Aiguaviva › Gironès | 1 |
| Forêt de Aiguaviva (8) ⚠️ | Aiguaviva › Gironès | 1 |
| Forêt de Vilobí d'Onyar (17) ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 1 |
| Forêt de Vilobí d'Onyar (18) ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 1 |
| Forêt de Aiguaviva (10) ⚠️ | Aiguaviva › Gironès | 1 |
| Forêt de Vilobí d'Onyar (20) ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 1 |
| Forêt de Vilobí d'Onyar (22) ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 1 |
| Forêt de Aiguaviva (17) ⚠️ | Aiguaviva › Gironès | 1 |
| Forêt de Riudellots de la Selva (7) ⚠️ | Riudellots de la Selva › la Selva (Gérone) | 1 |
| Forêt de Siurana (2) ⚠️ | Siurana › Alt Empordà | 1 |
| Forêt de Fornells de la Selva (5) ⚠️ | Fornells de la Selva › Gironès | 1 |
| Forêt de Fornells de la Selva (7) ⚠️ | Fornells de la Selva › Gironès | 1 |
| Forêt de Aiguaviva (18) ⚠️ | Aiguaviva › Gironès | 1 |
| Forêt de Aiguaviva (19) ⚠️ | Aiguaviva › Gironès | 1 |
| Forêt de Torroella de Fluvià ⚠️ | Torroella de Fluvià › Alt Empordà | 1 |
| Forêt de Siurana (3) ⚠️ | Siurana › Alt Empordà | 1 |
| Forêt de Torroella de Fluvià (4) ⚠️ | Torroella de Fluvià › Alt Empordà | 1 |
| Bois de Anglès (2) ⚠️ | Anglès › la Selva (Gérone) | 1 |
| Forêt de Figueres (2) ⚠️ | Figueres › Alt Empordà | 1 |
| Parc de Sant Feliu de Guíxols (2) ⚠️ | Sant Feliu de Guíxols › Baix Empordà | 1 |
| Forêt de Viladasens (2) ⚠️ | Viladasens › Gironès | 1 |
| Forêt de Navata (2) ⚠️ | Navata › Alt Empordà | 1 |
| Forêt de Navata (3) ⚠️ | Navata › Alt Empordà | 1 |
| Forêt de Llers (5) ⚠️ | Llers › Alt Empordà | 1 |
| Forêt de Llers (7) ⚠️ | Llers › Alt Empordà | 1 |
| Parc de l'Estació ⚠️ | Sant Joan de les Abadesses › Ripollès | 1 |
| Forêt de Foixà (4) ⚠️ | Foixà › Baix Empordà | 1 |
| Forêt de Bescanó (4) ⚠️ | Bescanó › Gironès | 1 |
| Camp del Toro ⚠️ | Llanars › Ripollès | 1 |
| Parc de Blanes (7) ⚠️ | Blanes › la Selva (Gérone) | 1 |
| Parc de Sant Feliu de Guíxols (3) ⚠️ | Sant Feliu de Guíxols › Baix Empordà | 1 |
| Forêt de la Cellera de Ter (13) ⚠️ | la Cellera de Ter › la Selva (Gérone) | 1 |
| Forêt de Girona (8) ⚠️ | Girona › Gironès | 1 |
| Parc de Susqueda (2) ⚠️ | Susqueda › la Selva (Gérone) | 1 |
| Forêt de Cruïlles, Monells i Sant Sadurní de l'Heura (3) ⚠️ | Cruïlles, Monells i Sant Sadurní de l'Heura › Baix Empordà | 1 |
| Forêt de Cruïlles, Monells i Sant Sadurní de l'Heura (4) ⚠️ | Cruïlles, Monells i Sant Sadurní de l'Heura › Baix Empordà | 1 |
| Forêt de Cruïlles, Monells i Sant Sadurní de l'Heura (6) ⚠️ | Cruïlles, Monells i Sant Sadurní de l'Heura › Baix Empordà | 1 |
| Forêt de Cruïlles, Monells i Sant Sadurní de l'Heura (9) ⚠️ | Cruïlles, Monells i Sant Sadurní de l'Heura › Baix Empordà | 1 |
| Forêt de la Bisbal d'Empordà (2) ⚠️ | la Bisbal d'Empordà › Baix Empordà | 1 |
| Forêt de la Bisbal d'Empordà (3) ⚠️ | la Bisbal d'Empordà › Baix Empordà | 1 |
| Forêt de Cruïlles, Monells i Sant Sadurní de l'Heura (15) ⚠️ | Cruïlles, Monells i Sant Sadurní de l'Heura › Baix Empordà | 1 |
| Forêt de Cruïlles, Monells i Sant Sadurní de l'Heura (19) ⚠️ | Cruïlles, Monells i Sant Sadurní de l'Heura › Baix Empordà | 1 |
| Forêt de Cruïlles, Monells i Sant Sadurní de l'Heura (20) ⚠️ | Cruïlles, Monells i Sant Sadurní de l'Heura › Baix Empordà | 1 |
| Forêt de Cruïlles, Monells i Sant Sadurní de l'Heura (22) ⚠️ | Cruïlles, Monells i Sant Sadurní de l'Heura › Baix Empordà | 1 |
| Forêt de Cruïlles, Monells i Sant Sadurní de l'Heura (23) ⚠️ | Cruïlles, Monells i Sant Sadurní de l'Heura › Baix Empordà | 1 |
| Forêt de Cruïlles, Monells i Sant Sadurní de l'Heura (24) ⚠️ | Cruïlles, Monells i Sant Sadurní de l'Heura › Baix Empordà | 1 |
| Forêt de la Pera (3) ⚠️ | la Pera › Baix Empordà | 1 |
| Forêt de la Pera (4) ⚠️ | la Pera › Baix Empordà | 1 |
| Forêt de Forallac (2) ⚠️ | Forallac › Baix Empordà | 1 |
| Forêt de Forallac (4) ⚠️ | Forallac › Baix Empordà | 1 |
| Forêt de Forallac (5) ⚠️ | Forallac › Baix Empordà | 1 |
| Forêt de Forallac (6) ⚠️ | Forallac › Baix Empordà | 1 |
| Forêt de Forallac (7) ⚠️ | Forallac › Baix Empordà | 1 |
| Forêt de Forallac (11) ⚠️ | Forallac › Baix Empordà | 1 |
| Forêt de Forallac (12) ⚠️ | Forallac › Baix Empordà | 1 |
| Forêt de Forallac (18) ⚠️ | Forallac › Baix Empordà | 1 |
| Forêt de Forallac (19) ⚠️ | Forallac › Baix Empordà | 1 |
| Forêt de Forallac (22) ⚠️ | Forallac › Baix Empordà | 1 |
| Parc de Ripoll (4) ⚠️ | Ripoll › Ripollès | 1 |
| Parc de Campdevànol ⚠️ | Campdevànol › Ripollès | 1 |
| Parc de Campdevànol (5) ⚠️ | Campdevànol › Ripollès | 1 |
| Forêt de Sant Feliu de Guíxols (3) ⚠️ | Sant Feliu de Guíxols › Baix Empordà | 1 |
| Forêt de Campllong (2) ⚠️ | Campllong › Gironès | 1 |
| Forêt de Campllong (4) ⚠️ | Campllong › Gironès | 1 |
| Forêt de Campllong (7) ⚠️ | Campllong › Gironès | 1 |
| Forêt de Campllong (8) ⚠️ | Campllong › Gironès | 1 |
| Forêt de Campllong (9) ⚠️ | Campllong › Gironès | 1 |
| Parc de Ripoll (14) ⚠️ | Ripoll › Ripollès | 1 |
| Forêt de Celrà (3) ⚠️ | Celrà › Gironès | 1 |
| Forêt de Sant Feliu de Guíxols (5) ⚠️ | Sant Feliu de Guíxols › Baix Empordà | 1 |
| Forêt de Olot (2) ⚠️ | Olot › Garrotxa | 1 |
| Forêt de la Bisbal d'Empordà (4) ⚠️ | la Bisbal d'Empordà › Baix Empordà | 1 |
| Forêt de Sant Gregori (2) ⚠️ | Sant Gregori › Gironès | 1 |
| Forêt de Sant Gregori (3) ⚠️ | Sant Gregori › Gironès | 1 |
| Forêt de Sant Feliu de Guíxols (6) ⚠️ | Sant Feliu de Guíxols › Baix Empordà | 1 |
| Forêt de Sant Feliu de Guíxols (7) ⚠️ | Sant Feliu de Guíxols › Baix Empordà | 1 |
| Forêt de Campllong (13) ⚠️ | Campllong › Gironès | 1 |
| Forêt de Cassà de la Selva (2) ⚠️ | Cassà de la Selva › Gironès | 1 |
| Forêt de Campllong (15) ⚠️ | Campllong › Gironès | 1 |
| Forêt de Sant Feliu de Guíxols (9) ⚠️ | Sant Feliu de Guíxols › Baix Empordà | 1 |
| Forêt de Brunyola i Sant Martí Sapresa ⚠️ | Brunyola i Sant Martí Sapresa › la Selva (Gérone) | 1 |
| Bosc d'en Peric ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 1 |
| Forêt de Vilobí d'Onyar (25) ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 1 |
| Forêt de Vilobí d'Onyar (26) ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 1 |
| Forêt de Llagostera (8) ⚠️ | Llagostera › Gironès | 1 |
| Forêt de Cassà de la Selva (5) ⚠️ | Cassà de la Selva › Gironès | 1 |
| Forêt de Llagostera (14) ⚠️ | Cassà de la Selva › Gironès | 1 |
| Forêt de Llagostera (18) ⚠️ | Cassà de la Selva › Gironès | 1 |
| Forêt de Cassà de la Selva (6) ⚠️ | Cassà de la Selva › Gironès | 1 |
| Forêt de Cassà de la Selva (8) ⚠️ | Cassà de la Selva › Gironès | 1 |
| Forêt de Llagostera (29) ⚠️ | Llagostera › Gironès | 1 |
| Forêt de Sant Andreu Salou ⚠️ | Sant Andreu Salou › Gironès | 1 |
| Forêt de Cassà de la Selva (15) ⚠️ | Cassà de la Selva › Gironès | 1 |
| Forêt de Cassà de la Selva (19) ⚠️ | Cassà de la Selva › Gironès | 1 |
| Forêt de Cassà de la Selva (20) ⚠️ | Cassà de la Selva › Gironès | 1 |
| Forêt de Sant Andreu Salou (3) ⚠️ | Sant Andreu Salou › Gironès | 1 |
| Forêt de Cassà de la Selva (26) ⚠️ | Cassà de la Selva › Gironès | 1 |
| Forêt de Cassà de la Selva (27) ⚠️ | Cassà de la Selva › Gironès | 1 |
| Forêt de Sant Andreu Salou (5) ⚠️ | Sant Andreu Salou › Gironès | 1 |
| Forêt de Cassà de la Selva (29) ⚠️ | Cassà de la Selva › Gironès | 1 |
| Forêt de Caldes de Malavella (8) ⚠️ | Caldes de Malavella › la Selva (Gérone) | 1 |
| Forêt de Caldes de Malavella (17) ⚠️ | Caldes de Malavella › la Selva (Gérone) | 1 |
| Forêt de Sant Andreu Salou (6) ⚠️ | Sant Andreu Salou › Gironès | 1 |
| Forêt de Sant Andreu Salou (7) ⚠️ | Sant Andreu Salou › Gironès | 1 |
| Forêt de Fornells de la Selva (8) ⚠️ | Fornells de la Selva › Gironès | 1 |
| Forêt de Brunyola i Sant Martí Sapresa (2) ⚠️ | Brunyola i Sant Martí Sapresa › la Selva (Gérone) | 1 |
| Forêt de Llagostera (32) ⚠️ | Llagostera › Gironès | 1 |
| Forêt de Palamós ⚠️ | Palamós › Baix Empordà | 1 |
| Forêt de Calonge i Sant Antoni (4) ⚠️ | Calonge i Sant Antoni › Baix Empordà | 1 |
| Parc de Vila-Seca ⚠️ | Palafrugell › Baix Empordà | 1 |
| Forêt de Palafrugell (2) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Forêt de Palafrugell (4) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Forêt de Palafrugell (5) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Forêt de Palafrugell (7) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Forêt de Palafrugell (8) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Forêt de Palafrugell (9) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Parc de Calonge i Sant Antoni (2) ⚠️ | Calonge i Sant Antoni › Baix Empordà | 1 |
| Forêt de Palafrugell (13) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Forêt de Palafrugell (14) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Bois de Palafrugell (2) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Bois de Palafrugell (4) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Forêt de Palafrugell (17) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Forêt de Palafrugell (22) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Forêt de Palafrugell (24) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Forêt de Begur ⚠️ | Begur › Baix Empordà | 1 |
| Forêt de Begur (2) ⚠️ | Begur › Baix Empordà | 1 |
| Bois de Begur ⚠️ | Begur › Baix Empordà | 1 |
| Plaça 11 de Març de 2004 ⚠️ | Palafrugell › Baix Empordà | 1 |
| Forêt de Palafrugell (32) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Forêt de Palafrugell (35) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Parc de Torrent ⚠️ | Torrent › Baix Empordà | 1 |
| Bois de Palafrugell (9) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Forêt de Palafrugell (41) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Forêt de Palafrugell (44) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Forêt de Pontós (2) ⚠️ | Pontós › Alt Empordà | 1 |
| Forêt de Palafrugell (51) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Forêt de Palafrugell (52) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Forêt de Palafrugell (58) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Forêt de Palafrugell (69) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Forêt de Palafrugell (71) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Forêt de Vidreres (3) ⚠️ | Vidreres › la Selva (Gérone) | 1 |
| Forêt de Vidreres (4) ⚠️ | Vidreres › la Selva (Gérone) | 1 |
| Forêt de Palafrugell (88) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Forêt de Torrent (2) ⚠️ | Torrent › Baix Empordà | 1 |
| Forêt de Olot (3) ⚠️ | Olot › Garrotxa | 1 |
| Bois de Olot (4) ⚠️ | Olot › Garrotxa | 1 |
| Bois de Olot (12) ⚠️ | Olot › Garrotxa | 1 |
| Forêt de Brunyola i Sant Martí Sapresa (3) ⚠️ | Brunyola i Sant Martí Sapresa › la Selva (Gérone) | 1 |
| Forêt de Santa Coloma de Farners (2) ⚠️ | Santa Coloma de Farners › la Selva (Gérone) | 1 |
| Forêt de Vilobí d'Onyar (33) ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 1 |
| Forêt de Riudellots de la Selva (14) ⚠️ | Riudellots de la Selva › la Selva (Gérone) | 1 |
| Plaça de Sebastià Salellas i Magret ⚠️ | Girona › Gironès | 1 |
| Forêt de Calonge i Sant Antoni (8) ⚠️ | Calonge i Sant Antoni › Baix Empordà | 1 |
| Forêt de Girona (10) ⚠️ | Girona › Gironès | 1 |
| Forêt de Calonge i Sant Antoni (10) ⚠️ | Calonge i Sant Antoni › Baix Empordà | 1 |
| Forêt de Calonge i Sant Antoni (11) ⚠️ | Calonge i Sant Antoni › Baix Empordà | 1 |
| Forêt de Calonge i Sant Antoni (15) ⚠️ | Calonge i Sant Antoni › Baix Empordà | 1 |
| Forêt de Lladó (4) ⚠️ | Lladó › Alt Empordà | 1 |
| Parc de Sils (3) ⚠️ | Sils › la Selva (Gérone) | 1 |
| Forêt de Lladó (5) ⚠️ | Lladó › Alt Empordà | 1 |
| Forêt de Castell d'Aro, Platja d'Aro i s'Agaró (9) ⚠️ | Castell d'Aro, Platja d'Aro i s'Agaró › Baix Empordà | 1 |
| Forêt de Calonge i Sant Antoni (17) ⚠️ | Calonge i Sant Antoni › Baix Empordà | 1 |
| Parc de Palamós (7) ⚠️ | Palamós › Baix Empordà | 1 |
| Forêt de Lloret de Mar (2) ⚠️ | Lloret de Mar › la Selva (Gérone) | 1 |
| Bois de Girona (5) ⚠️ | Girona › Gironès | 1 |
| Bois de Girona (6) ⚠️ | Girona › Gironès | 1 |
| Bois de Girona (7) ⚠️ | Girona › Gironès | 1 |
| Bois de Girona (8) ⚠️ | Girona › Gironès | 1 |
| Bois de Girona (10) ⚠️ | Girona › Gironès | 1 |
| Plaça de Joaquim Llucià i Olivet ⚠️ | Vidreres › la Selva (Gérone) | 1 |
| Parc de Maçanet de la Selva ⚠️ | Maçanet de la Selva › la Selva (Gérone) | 1 |
| Forêt de Cervià de Ter (3) ⚠️ | Cervià de Ter › Gironès | 1 |
| Forêt de Cervià de Ter (4) ⚠️ | Cervià de Ter › Gironès | 1 |
| Forêt de Cervià de Ter (5) ⚠️ | Cervià de Ter › Gironès | 1 |
| Forêt de Cervià de Ter (7) ⚠️ | Cervià de Ter › Gironès | 1 |
| Forêt de Cervià de Ter (8) ⚠️ | Cervià de Ter › Gironès | 1 |
| Forêt de Cervià de Ter (11) ⚠️ | Cervià de Ter › Gironès | 1 |
| Forêt de Sant Jordi Desvalls (2) ⚠️ | Cervià de Ter › Gironès | 1 |
| Forêt de Cervià de Ter (15) ⚠️ | Cervià de Ter › Gironès | 1 |
| Forêt de Cervià de Ter (16) ⚠️ | Cervià de Ter › Gironès | 1 |
| Forêt de Cervià de Ter (18) ⚠️ | Cervià de Ter › Gironès | 1 |
| Forêt de Cervià de Ter (19) ⚠️ | Cervià de Ter › Gironès | 1 |
| Forêt de Cervià de Ter (25) ⚠️ | Cervià de Ter › Gironès | 1 |
| Bois de Cervià de Ter ⚠️ | Cervià de Ter › Gironès | 1 |
| Forêt de Cervià de Ter (31) ⚠️ | Cervià de Ter › Gironès | 1 |
| Forêt de Cervià de Ter (32) ⚠️ | Cervià de Ter › Gironès | 1 |
| Bois de Viladasens ⚠️ | Viladasens › Gironès | 1 |
| Bois de Cervià de Ter (3) ⚠️ | Cervià de Ter › Gironès | 1 |
| Forêt de la Vajol (11) ⚠️ | la Vajol › Alt Empordà | 1 |
| Forêt de la Vajol (14) ⚠️ | la Vajol › Alt Empordà | 1 |
| Forêt de la Vajol (26) ⚠️ | Agullana › Alt Empordà | 1 |
| Forêt de la Vajol (30) ⚠️ | la Vajol › Alt Empordà | 1 |
| Forêt de la Vajol (32) ⚠️ | la Vajol › Alt Empordà | 1 |
| Forêt de la Tallada d'Empordà (3) ⚠️ | la Tallada d'Empordà › Baix Empordà | 1 |
| Parc de Palamós (9) ⚠️ | Palamós › Baix Empordà | 1 |
| Forêt de Mont-ras (5) ⚠️ | Mont-ras › Baix Empordà | 1 |
| Parc de Vilablareix (2) ⚠️ | Vilablareix › Gironès | 1 |
| Parc de Vilablareix (3) ⚠️ | Vilablareix › Gironès | 1 |
| Forêt de Calonge i Sant Antoni (18) ⚠️ | Calonge i Sant Antoni › Baix Empordà | 1 |
| Parc de Blanes (8) ⚠️ | Blanes › la Selva (Gérone) | 1 |
| Forêt de Santa Cristina d'Aro ⚠️ | Santa Cristina d'Aro › Baix Empordà | 1 |
| Forêt de Camós ⚠️ | Camós › Pla de l'Estany | 1 |
| Forêt de Cornellà del Terri (8) ⚠️ | Cornellà del Terri › Pla de l'Estany | 1 |
| Forêt de Cornellà del Terri (9) ⚠️ | Cornellà del Terri › Pla de l'Estany | 1 |
| Forêt de Darnius ⚠️ | Darnius › Alt Empordà | 1 |
| Font de la Vaca ⚠️ | Caldes de Malavella › la Selva (Gérone) | 1 |
| Forêt de Quart (8) ⚠️ | Quart › Gironès | 1 |
| Parc de Besalú (2) ⚠️ | Besalú › Garrotxa | 1 |
| Forêt de Fontcoberta (3) ⚠️ | Fontcoberta › Pla de l'Estany | 1 |
| Forêt de Sarrià de Ter (3) ⚠️ | Sarrià de Ter › Gironès | 1 |
| Parc de la Maçana ⚠️ | Salt › Gironès | 1 |
| Bois de Sils (2) ⚠️ | Sils › la Selva (Gérone) | 1 |
| Parc de Isòvol ⚠️ | Isòvol › Cerdanya (Gérone) | 1 |
| Forêt de Calonge i Sant Antoni (19) ⚠️ | Calonge i Sant Antoni › Baix Empordà | 1 |
| Plaça John Lennon ⚠️ | Torroella de Montgrí › Baix Empordà | 1 |
| Clota d'en Font ⚠️ | Bescanó › Gironès | 1 |
| Forêt de Castell d'Aro, Platja d'Aro i s'Agaró (11) ⚠️ | Castell d'Aro, Platja d'Aro i s'Agaró › Baix Empordà | 1 |
| Parc de L'Arbreda ⚠️ | Begur › Baix Empordà | 1 |
| Forêt de Caldes de Malavella (18) ⚠️ | Caldes de Malavella › la Selva (Gérone) | 1 |
| Parc de Bolvir (3) ⚠️ | Bolvir › Cerdanya (Gérone) | 1 |
| Parc de Girona (17) ⚠️ | Girona › Gironès | 1 |
| Forêt de Castell d'Aro, Platja d'Aro i s'Agaró (12) ⚠️ | Castell d'Aro, Platja d'Aro i s'Agaró › Baix Empordà | 1 |
| Forêt de Bescanó (5) ⚠️ | Bescanó › Gironès | 1 |
| Forêt de Santa Coloma de Farners (7) ⚠️ | Santa Coloma de Farners › la Selva (Gérone) | 1 |
| Bosquet Municipal ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Castell d'Aro, Platja d'Aro i s'Agaró (14) ⚠️ | Castell d'Aro, Platja d'Aro i s'Agaró › Baix Empordà | 1 |
| Bois de Porqueres (4) ⚠️ | Porqueres › Pla de l'Estany | 1 |
| Jardins de John Lennon ⚠️ | Girona › Gironès | 1 |
| Forêt de Viladrau (17) ⚠️ | Viladrau › Osona (Gérone) | 1 |
| Parc Central ⚠️ | Girona › Gironès | 1 |
| Forêt de Das (2) ⚠️ | Alp › Cerdanya (Gérone) | 1 |
| Forêt de Das (3) ⚠️ | Das › Cerdanya (Gérone) | 1 |
| Forêt de Das (6) ⚠️ | Das › Cerdanya (Gérone) | 1 |
| Forêt de Das (11) ⚠️ | Das › Cerdanya (Gérone) | 1 |
| Forêt de Das (14) ⚠️ | Das › Cerdanya (Gérone) | 1 |
| Forêt de Das (15) ⚠️ | Das › Cerdanya (Gérone) | 1 |
| Forêt de Alp (18) ⚠️ | Alp › Cerdanya (Gérone) | 1 |
| Forêt de Alp (41) ⚠️ | Alp › Cerdanya (Gérone) | 1 |
| Forêt de Alp (49) ⚠️ | Alp › Cerdanya (Gérone) | 1 |
| Forêt de Alp (51) ⚠️ | Alp › Cerdanya (Gérone) | 1 |
| Forêt de Alp (52) ⚠️ | Alp › Cerdanya (Gérone) | 1 |
| Forêt de Alp (60) ⚠️ | Alp › Cerdanya (Gérone) | 1 |
| Forêt de Alp (76) ⚠️ | Alp › Cerdanya (Gérone) | 1 |
| Forêt de Alp (77) ⚠️ | Alp › Cerdanya (Gérone) | 1 |
| Forêt de Queralbs (2) ⚠️ | Queralbs › Ripollès | 1 |
| Forêt de Queralbs (6) ⚠️ | Queralbs › Ripollès | 1 |
| Forêt de Queralbs (8) ⚠️ | Queralbs › Ripollès | 1 |
| Forêt de Queralbs (11) ⚠️ | Queralbs › Ripollès | 1 |
| Forêt de Queralbs (12) ⚠️ | Queralbs › Ripollès | 1 |
| Forêt de Girona (23) ⚠️ | Girona › Gironès | 1 |
| Jardins d'Esperança Bru i Oller ⚠️ | Girona › Gironès | 1 |
| Forêt de Girona (28) ⚠️ | Girona › Gironès | 1 |
| Forêt de Girona (29) ⚠️ | Girona › Gironès | 1 |
| Forêt de Girona (30) ⚠️ | Girona › Gironès | 1 |
| Forêt de Girona (32) ⚠️ | Girona › Gironès | 1 |
| Forêt de Girona (33) ⚠️ | Girona › Gironès | 1 |
| Forêt de Girona (35) ⚠️ | Girona › Gironès | 1 |
| Forêt de Sarrià de Ter (11) ⚠️ | Sarrià de Ter › Gironès | 1 |
| Forêt de Sarrià de Ter (12) ⚠️ | Sarrià de Ter › Gironès | 1 |
| Forêt de Girona (39) ⚠️ | Girona › Gironès | 1 |
| Forêt de Begur (7) ⚠️ | Begur › Baix Empordà | 1 |
| Forêt de Aiguaviva (22) ⚠️ | Aiguaviva › Gironès | 1 |
| Forêt de Sils (10) ⚠️ | Sils › la Selva (Gérone) | 1 |
| Forêt de Riudarenes (4) ⚠️ | Riudarenes › la Selva (Gérone) | 1 |
| Espai Firal ⚠️ | Palafrugell › Baix Empordà | 1 |
| Forêt de Palafrugell (97) ⚠️ | Begur › Baix Empordà | 1 |
| Bois de Palafrugell (27) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Forêt de Mont-ras (8) ⚠️ | Mont-ras › Baix Empordà | 1 |
| Plaça Catalunya (4) ⚠️ | Llagostera › Gironès | 1 |
| Forêt de Torroella de Montgrí (2) ⚠️ | Torroella de Montgrí › Baix Empordà | 1 |
| Forêt de Torroella de Montgrí (3) ⚠️ | Torroella de Montgrí › Baix Empordà | 1 |
| Forêt de Cassà de la Selva (30) ⚠️ | Cassà de la Selva › Gironès | 1 |
| Forêt de Corçà (10) ⚠️ | Corçà › Baix Empordà | 1 |
| Bois de la Bisbal d'Empordà ⚠️ | la Bisbal d'Empordà › Baix Empordà | 1 |
| Forêt de Bescanó (7) ⚠️ | Bescanó › Gironès | 1 |
| Forêt de Vilobí d'Onyar (37) ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 1 |
| Parc de Banyoles (13) ⚠️ | Banyoles › Pla de l'Estany | 1 |
| Forêt de Llançà ⚠️ | Llançà › Alt Empordà | 1 |
| Forêt de el Port de la Selva ⚠️ | el Port de la Selva › Alt Empordà | 1 |
| Bois de Agullana ⚠️ | Agullana › Alt Empordà | 1 |
| Bois de Pontós (4) ⚠️ | Pontós › Alt Empordà | 1 |
| Bois de Pontós (5) ⚠️ | Pontós › Alt Empordà | 1 |
| Forêt de Fontcoberta (7) ⚠️ | Fontcoberta › Pla de l'Estany | 1 |
| Forêt de Vilanant (3) ⚠️ | Vilanant › Alt Empordà | 1 |
| Bois de Vilademuls (2) ⚠️ | Vilademuls › Pla de l'Estany | 1 |
| Bois de Vilademuls (5) ⚠️ | Vilademuls › Pla de l'Estany | 1 |
| Forêt de Vilademuls (8) ⚠️ | Vilademuls › Pla de l'Estany | 1 |
| Bois de Vilademuls (15) ⚠️ | Vilademuls › Pla de l'Estany | 1 |
| Bois de Vilademuls (16) ⚠️ | Vilademuls › Pla de l'Estany | 1 |
| Bois de Sant Julià de Ramis ⚠️ | Sant Julià de Ramis › Gironès | 1 |
| Bois de Cornellà del Terri (3) ⚠️ | Cornellà del Terri › Pla de l'Estany | 1 |
| Bois de Cornellà del Terri (4) ⚠️ | Cornellà del Terri › Pla de l'Estany | 1 |
| Bois de Cornellà del Terri (5) ⚠️ | Cornellà del Terri › Pla de l'Estany | 1 |
| Bois de Camós (2) ⚠️ | Cornellà del Terri › Pla de l'Estany | 1 |
| Bois de Cornellà del Terri (6) ⚠️ | Cornellà del Terri › Pla de l'Estany | 1 |
| Bois de Camós (3) ⚠️ | Camós › Pla de l'Estany | 1 |
| Bois de Torroella de Montgrí (3) ⚠️ | Torroella de Montgrí › Baix Empordà | 1 |
| Bois de Ullà ⚠️ | Ullà › Baix Empordà | 1 |
| Bois de Terrades ⚠️ | Terrades › Alt Empordà | 1 |
| Bois de Llers (3) ⚠️ | Llers › Alt Empordà | 1 |
| Bois de Llers (4) ⚠️ | Llers › Alt Empordà | 1 |
| Forêt de Lloret de Mar (6) ⚠️ | Lloret de Mar › la Selva (Gérone) | 1 |
| Forêt de Garrigoles (9) ⚠️ | Garrigoles › Baix Empordà | 1 |
| Forêt de Viladamat ⚠️ | Viladamat › Alt Empordà | 1 |
| Bois de Foixà ⚠️ | Foixà › Baix Empordà | 1 |
| Forêt de Foixà (5) ⚠️ | Foixà › Baix Empordà | 1 |
| Bois de Sant Jordi Desvalls ⚠️ | Sant Jordi Desvalls › Gironès | 1 |
| Bois de Sant Jordi Desvalls (5) ⚠️ | Sant Jordi Desvalls › Gironès | 1 |
| Bois de Sant Jordi Desvalls (7) ⚠️ | Sant Jordi Desvalls › Gironès | 1 |
| Parc de Girona (39) ⚠️ | Girona › Gironès | 1 |
| Forêt de l'Escala (4) ⚠️ | l'Escala › Alt Empordà | 1 |
| Forêt de Torroella de Montgrí (14) ⚠️ | Torroella de Montgrí › Baix Empordà | 1 |
| Forêt de Torroella de Montgrí (16) ⚠️ | Torroella de Montgrí › Baix Empordà | 1 |
| Forêt de Torroella de Montgrí (19) ⚠️ | Torroella de Montgrí › Baix Empordà | 1 |
| Forêt de Torroella de Montgrí (22) ⚠️ | Torroella de Montgrí › Baix Empordà | 1 |
| Forêt de Torroella de Montgrí (26) ⚠️ | Torroella de Montgrí › Baix Empordà | 1 |
| Parc de Peralada ⚠️ | Peralada › Alt Empordà | 1 |
| Forêt de Castelló d'Empúries (6) ⚠️ | Castelló d'Empúries › Alt Empordà | 1 |
| Forêt de Ventalló (7) ⚠️ | Ventalló › Alt Empordà | 1 |
| Forêt de Cantallops ⚠️ | Cantallops › Alt Empordà | 1 |
| Forêt de Cantallops (3) ⚠️ | Cantallops › Alt Empordà | 1 |
| Forêt de Cantallops (6) ⚠️ | Cantallops › Alt Empordà | 1 |
| Forêt de Mollet de Peralada (2) ⚠️ | Mollet de Peralada › Alt Empordà | 1 |
| Forêt de Torroella de Montgrí (40) ⚠️ | Torroella de Montgrí › Baix Empordà | 1 |
| Forêt de Torroella de Montgrí (41) ⚠️ | Torroella de Montgrí › Baix Empordà | 1 |
| Forêt de l'Escala (8) ⚠️ | l'Escala › Alt Empordà | 1 |
| Forêt de l'Escala (9) ⚠️ | l'Escala › Alt Empordà | 1 |
| Forêt de l'Escala (10) ⚠️ | l'Escala › Alt Empordà | 1 |
| Forêt de l'Escala (11) ⚠️ | l'Escala › Alt Empordà | 1 |
| Forêt de l'Escala (12) ⚠️ | l'Escala › Alt Empordà | 1 |
| Forêt de Ullastret ⚠️ | Ullastret › Baix Empordà | 1 |
| Forêt de Jafre (3) ⚠️ | Jafre › Baix Empordà | 1 |
| Parc de Santa Coloma de Farners (9) ⚠️ | Santa Coloma de Farners › la Selva (Gérone) | 1 |
| Forêt de Alp (84) ⚠️ | Alp › Cerdanya (Gérone) | 1 |
| Forêt de Figueres (4) ⚠️ | Figueres › Alt Empordà | 1 |
| Forêt de l'Escala (24) ⚠️ | l'Escala › Alt Empordà | 1 |
| Parc de Castell d'Aro, Platja d'Aro i s'Agaró (30) ⚠️ | Castell d'Aro, Platja d'Aro i s'Agaró › Baix Empordà | 1 |
| Parc de Castell d'Aro, Platja d'Aro i s'Agaró (34) ⚠️ | Castell d'Aro, Platja d'Aro i s'Agaró › Baix Empordà | 1 |
| Forêt de Girona (48) ⚠️ | Girona › Gironès | 1 |
| Forêt de Palafrugell (100) ⚠️ | Palafrugell › Baix Empordà | 1 |
| parc la devesa ⚠️ | Girona › Gironès | 1 |
| Camp de Mart - antic estadi del GEiEG ⚠️ | Girona › Gironès | 1 |
| Forêt de Serinyà (2) ⚠️ | Serinyà › Pla de l'Estany | 1 |
| Parc de Torroella de Montgrí (4) ⚠️ | Torroella de Montgrí › Baix Empordà | 1 |
| Parc de Torroella de Montgrí (5) ⚠️ | Torroella de Montgrí › Baix Empordà | 1 |
| Forêt de Ger (4) ⚠️ | Ger › Cerdanya (Gérone) | 1 |
| Parc de Girona (46) ⚠️ | Girona › Gironès | 1 |
| Forêt de Queralbs (15) ⚠️ | Queralbs › Ripollès | 1 |
| Forêt de Queralbs (18) ⚠️ | Queralbs › Ripollès | 1 |
| Forêt de Das (23) ⚠️ | Das › Cerdanya (Gérone) | 1 |
| Bois de Maçanet de la Selva ⚠️ | Maçanet de la Selva › la Selva (Gérone) | 1 |
| Bois de Sant Joan de Mollet ⚠️ | Sant Joan de Mollet › Gironès | 1 |
| Forêt de Olot (7) ⚠️ | Olot › Garrotxa | 1 |
| Forêt de Olot (9) ⚠️ | Olot › Garrotxa | 1 |
| Parc de Maçanet de Cabrenys ⚠️ | Maçanet de Cabrenys › Alt Empordà | 1 |
| Parc del Ter ⚠️ | Colomers › Baix Empordà | 1 |
| puig mari zona de joc ⚠️ | Maçanet de la Selva › la Selva (Gérone) | 1 |
| Parc de Sils (8) ⚠️ | Sils › la Selva (Gérone) | 1 |
| Forêt de Sarrià de Ter (14) ⚠️ | Sarrià de Ter › Gironès | 1 |
| Forêt de Girona (49) ⚠️ | Girona › Gironès | 1 |
| Forêt de Palafrugell (104) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Forêt de Sant Feliu de Guíxols (14) ⚠️ | Sant Feliu de Guíxols › Baix Empordà | 1 |
| Forêt de Sant Feliu de Guíxols (16) ⚠️ | Sant Feliu de Guíxols › Baix Empordà | 1 |
| Forêt de Lloret de Mar (8) ⚠️ | Lloret de Mar › la Selva (Gérone) | 1 |
| Forêt de Lloret de Mar (10) ⚠️ | Lloret de Mar › la Selva (Gérone) | 1 |
| Forêt de Torroella de Montgrí (50) ⚠️ | Torroella de Montgrí › Baix Empordà | 1 |
| Forêt de l'Escala (29) ⚠️ | l'Escala › Alt Empordà | 1 |
| Forêt de Roses (7) ⚠️ | Roses › Alt Empordà | 1 |
| Forêt de el Port de la Selva (3) ⚠️ | el Port de la Selva › Alt Empordà | 1 |
| Forêt de Colera (2) ⚠️ | Colera › Alt Empordà | 1 |
| Forêt de la Bisbal d'Empordà (6) ⚠️ | la Bisbal d'Empordà › Baix Empordà | 1 |
| Forêt de Ullastret (5) ⚠️ | Ullastret › Baix Empordà | 1 |
| Forêt de Cabanes ⚠️ | Cabanes › Alt Empordà | 1 |
| Forêt de Setcases (3) ⚠️ | Setcases › Ripollès | 1 |
| Forêt de Setcases (7) ⚠️ | Setcases › Ripollès | 1 |
| Forêt de Setcases (9) ⚠️ | Setcases › Ripollès | 1 |
| Forêt de Setcases (13) ⚠️ | Setcases › Ripollès | 1 |
| Forêt de Setcases (16) ⚠️ | Setcases › Ripollès | 1 |
| Forêt de Setcases (20) ⚠️ | Setcases › Ripollès | 1 |
| Forêt de Ripoll (4) ⚠️ | Ripoll › Ripollès | 1 |
| Forêt de Flaçà (4) ⚠️ | Flaçà › Gironès | 1 |
| Forêt de Besalú (2) ⚠️ | Besalú › Garrotxa | 1 |
| Forêt de Palau-saverdera ⚠️ | Palau-saverdera › Alt Empordà | 1 |
| Parc de l'estació ⚠️ | Llagostera › Gironès | 1 |
| Parc de la Torre ⚠️ | Llagostera › Gironès | 1 |
| Parc de Riudellots de la Selva ⚠️ | Riudellots de la Selva › la Selva (Gérone) | 1 |
| Parc de Riudellots de la Selva (2) ⚠️ | Riudellots de la Selva › la Selva (Gérone) | 1 |
| Forêt de Vilaür (3) ⚠️ | Vilaür › Alt Empordà | 1 |
| Bois de Sant Feliu de Buixalleu ⚠️ | Sant Feliu de Buixalleu › la Selva (Gérone) | 1 |
| Bois de Sant Feliu de Buixalleu (2) ⚠️ | Sant Feliu de Buixalleu › la Selva (Gérone) | 1 |
| Bois de Sant Feliu de Buixalleu (3) ⚠️ | Sant Feliu de Buixalleu › la Selva (Gérone) | 1 |
| Forêt de Sant Feliu de Buixalleu (14) ⚠️ | Sant Feliu de Buixalleu › la Selva (Gérone) | 1 |
| Forêt de Torroella de Montgrí (53) ⚠️ | Torroella de Montgrí › Baix Empordà | 1 |
| Forêt de Massanes (8) ⚠️ | Massanes › la Selva (Gérone) | 1 |
| Forêt de Massanes (9) ⚠️ | Massanes › la Selva (Gérone) | 1 |
| Forêt de Massanes (10) ⚠️ | Massanes › la Selva (Gérone) | 1 |
| Forêt de Massanes (11) ⚠️ | Massanes › la Selva (Gérone) | 1 |
| Forêt de Massanes (15) ⚠️ | Massanes › la Selva (Gérone) | 1 |
| Forêt de Hostalric (2) ⚠️ | Hostalric › la Selva (Gérone) | 1 |
| Forêt de Osor (4) ⚠️ | Osor › la Selva (Gérone) | 1 |
| Forêt de Osor (8) ⚠️ | Osor › la Selva (Gérone) | 1 |
| Forêt de Osor (9) ⚠️ | Osor › la Selva (Gérone) | 1 |
| Forêt de Castell d'Aro, Platja d'Aro i s'Agaró (17) ⚠️ | Castell d'Aro, Platja d'Aro i s'Agaró › Baix Empordà | 1 |
| Forêt de Santa Cristina d'Aro (18) ⚠️ | Santa Cristina d'Aro › Baix Empordà | 1 |
| Forêt de Palau-sator (5) ⚠️ | Palau-sator › Baix Empordà | 1 |
| Forêt de Palau-sator (6) ⚠️ | Palau-sator › Baix Empordà | 1 |
| Forêt de Palau-sator (10) ⚠️ | Palau-sator › Baix Empordà | 1 |
| Bois de Palau-sator (3) ⚠️ | Palau-sator › Baix Empordà | 1 |
| Bois de Sant Pere Pescador ⚠️ | Sant Pere Pescador › Alt Empordà | 1 |
| Bois de Forallac (3) ⚠️ | Forallac › Baix Empordà | 1 |
| Bois de Sant Julià del Llor i Bonmatí (2) ⚠️ | Sant Julià del Llor i Bonmatí › la Selva (Gérone) | 1 |
| Forêt de Calonge i Sant Antoni (21) ⚠️ | Calonge i Sant Antoni › Baix Empordà | 1 |
| Forêt de Llagostera (36) ⚠️ | Llagostera › Gironès | 1 |
| Forêt de Lloret de Mar (11) ⚠️ | Lloret de Mar › la Selva (Gérone) | 1 |
| Forêt de Lloret de Mar (14) ⚠️ | Lloret de Mar › la Selva (Gérone) | 1 |
| Forêt de Vidreres (5) ⚠️ | Vidreres › la Selva (Gérone) | 1 |
| Forêt de Maçanet de la Selva (12) ⚠️ | Maçanet de la Selva › la Selva (Gérone) | 1 |
| Forêt de Blanes (9) ⚠️ | Blanes › la Selva (Gérone) | 1 |
| Plaça del Puig Sec ⚠️ | l'Escala › Alt Empordà | 1 |
| Bois de Caldes de Malavella ⚠️ | Caldes de Malavella › la Selva (Gérone) | 1 |
| Forêt de Maçanet de Cabrenys (3) ⚠️ | Maçanet de Cabrenys › Alt Empordà | 1 |
| Forêt de Vilobí d'Onyar (38) ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 1 |
| Bois de Mont-ras (8) ⚠️ | Mont-ras › Baix Empordà | 1 |
| Forêt de Vilobí d'Onyar (39) ⚠️ | Vilobí d'Onyar › la Selva (Gérone) | 1 |
| Parc de la Rectoria ⚠️ | Aiguaviva › Gironès | 1 |
| Forêt de Caldes de Malavella (21) ⚠️ | Caldes de Malavella › la Selva (Gérone) | 1 |
| Forêt de Brunyola i Sant Martí Sapresa (4) ⚠️ | Brunyola i Sant Martí Sapresa › la Selva (Gérone) | 1 |
| Parc de Girona (53) ⚠️ | Girona › Gironès | 1 |
| Forêt de Torroella de Montgrí (58) ⚠️ | Torroella de Montgrí › Baix Empordà | 1 |
| Bois de Palafrugell (31) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Parc de Calonge i Sant Antoni (18) ⚠️ | Calonge i Sant Antoni › Baix Empordà | 1 |
| Forêt de Celrà (7) ⚠️ | Celrà › Gironès | 1 |
| Forêt de Girona (57) ⚠️ | Girona › Gironès | 1 |
| Forêt de Girona (58) ⚠️ | Girona › Gironès | 1 |
| Forêt de Begur (15) ⚠️ | Begur › Baix Empordà | 1 |
| Forêt de Pals (2) ⚠️ | Pals › Baix Empordà | 1 |
| Forêt de Cruïlles, Monells i Sant Sadurní de l'Heura (26) ⚠️ | Cruïlles, Monells i Sant Sadurní de l'Heura › Baix Empordà | 1 |
| Forêt de Palau-sator (14) ⚠️ | Palau-sator › Baix Empordà | 1 |
| Forêt de Sant Jaume de Llierca (3) ⚠️ | Sant Jaume de Llierca › Garrotxa | 1 |
| Parc de Forallac ⚠️ | Forallac › Baix Empordà | 1 |
| Parc ⚠️ | Forallac › Baix Empordà | 1 |
| Bois de Vidreres ⚠️ | Vidreres › la Selva (Gérone) | 1 |
| Bois de Vidreres (3) ⚠️ | Vidreres › la Selva (Gérone) | 1 |
| Bois de Vidreres (4) ⚠️ | Vidreres › la Selva (Gérone) | 1 |
| Bois de Sils (5) ⚠️ | Sils › la Selva (Gérone) | 1 |
| Forêt de Vidreres (12) ⚠️ | Vidreres › la Selva (Gérone) | 1 |
| Parc de Fornells de la Selva (3) ⚠️ | Fornells de la Selva › Gironès | 1 |
| Bois de Sant Miquel de Campmajor ⚠️ | Sant Miquel de Campmajor › Pla de l'Estany | 1 |
| Bois de Salt (2) ⚠️ | Salt › Gironès | 1 |
| Bois de Salt (3) ⚠️ | Salt › Gironès | 1 |
| Bois de Sant Gregori (3) ⚠️ | Sant Gregori › Gironès | 1 |
| Bois de Sant Gregori (5) ⚠️ | Sant Gregori › Gironès | 1 |
| Bois de Serinyà ⚠️ | Serinyà › Pla de l'Estany | 1 |
| Bois de Navata (2) ⚠️ | Navata › Alt Empordà | 1 |
| Bois de Navata (4) ⚠️ | Navata › Alt Empordà | 1 |
| Bois de Navata (5) ⚠️ | Navata › Alt Empordà | 1 |
| Forêt de Riudarenes (7) ⚠️ | Riudarenes › la Selva (Gérone) | 1 |
| Parc de Blanes (17) ⚠️ | Blanes › la Selva (Gérone) | 1 |
| Plaça Onze de Setembre ⚠️ | Porqueres › Pla de l'Estany | 1 |
| Forêt de Saus, Camallera i Llampaies (3) ⚠️ | Saus, Camallera i Llampaies › Alt Empordà | 1 |
| Forêt de Garrigàs (12) ⚠️ | Garrigàs › Alt Empordà | 1 |
| Forêt de Sant Gregori (16) ⚠️ | Sant Gregori › Gironès | 1 |
| Forêt de Sant Gregori (19) ⚠️ | Sant Gregori › Gironès | 1 |
| Forêt de Viladasens (4) ⚠️ | Viladasens › Gironès | 1 |
| Parc de la Guingueta de Fontajau ⚠️ | Girona › Gironès | 1 |
| Bois de Corçà (2) ⚠️ | Corçà › Baix Empordà | 1 |
| Forêt de Cruïlles, Monells i Sant Sadurní de l'Heura (27) ⚠️ | Cruïlles, Monells i Sant Sadurní de l'Heura › Baix Empordà | 1 |
| Forêt de Forallac (31) ⚠️ | Forallac › Baix Empordà | 1 |
| Forêt de Forallac (32) ⚠️ | Forallac › Baix Empordà | 1 |
| Forêt de Forallac (34) ⚠️ | Forallac › Baix Empordà | 1 |
| Bois de Madremanya ⚠️ | Madremanya › Gironès | 1 |
| Bois de Madremanya (2) ⚠️ | Madremanya › Gironès | 1 |
| Bois de Madremanya (4) ⚠️ | Madremanya › Gironès | 1 |
| Bois de Canet d'Adri (4) ⚠️ | Canet d'Adri › Gironès | 1 |
| Forêt de Peralada (2) ⚠️ | Peralada › Alt Empordà | 1 |
| Forêt de Peralada (3) ⚠️ | Peralada › Alt Empordà | 1 |
| Forêt de Peralada (4) ⚠️ | Peralada › Alt Empordà | 1 |
| Forêt de Sils (15) ⚠️ | Sils › la Selva (Gérone) | 1 |
| Forêt de Sils (17) ⚠️ | Sils › la Selva (Gérone) | 1 |
| Forêt de Sils (18) ⚠️ | Sils › la Selva (Gérone) | 1 |
| Forêt de Sils (19) ⚠️ | Sils › la Selva (Gérone) | 1 |
| Forêt de Sils (21) ⚠️ | Sils › la Selva (Gérone) | 1 |
| Forêt de Sils (24) ⚠️ | Sils › la Selva (Gérone) | 1 |
| Forêt de Cabanes (2) ⚠️ | Cabanes › Alt Empordà | 1 |
| Forêt de Cabanes (3) ⚠️ | Cabanes › Alt Empordà | 1 |
| Forêt de Cabanes (4) ⚠️ | Cabanes › Alt Empordà | 1 |
| Forêt de Vilabertran (4) ⚠️ | Vilabertran › Alt Empordà | 1 |
| Bois de Canet d'Adri (5) ⚠️ | Canet d'Adri › Gironès | 1 |
| Zona pícnic el Castanyer ⚠️ | Sant Joan les Fonts › Garrotxa | 1 |
| Forêt de la Vall d'en Bas (4) ⚠️ | la Vall d'en Bas › Garrotxa | 1 |
| Forêt de Riells i Viabrea ⚠️ | Riells i Viabrea › la Selva (Gérone) | 1 |
| Forêt de Viladrau (18) ⚠️ | Viladrau › Osona (Gérone) | 1 |
| Bois de Corçà (3) ⚠️ | Corçà › Baix Empordà | 1 |
| Forêt de la Vall d'en Bas (6) ⚠️ | la Vall d'en Bas › Garrotxa | 1 |
| Forêt de la Vall d'en Bas (9) ⚠️ | la Vall d'en Bas › Garrotxa | 1 |
| Forêt de Maià de Montcal (5) ⚠️ | Maià de Montcal › Garrotxa | 1 |
| Forêt de Ventalló (8) ⚠️ | Ventalló › Alt Empordà | 1 |
| Forêt de Ventalló (10) ⚠️ | Ventalló › Alt Empordà | 1 |
| Plaça Miquel Coll i Alentorn ⚠️ | Girona › Gironès | 1 |
| Parc de Hostalric (10) ⚠️ | Hostalric › la Selva (Gérone) | 1 |
| Forêt de Girona (59) ⚠️ | Girona › Gironès | 1 |
| Bois de Sant Pere Pescador (3) ⚠️ | Sant Pere Pescador › Alt Empordà | 1 |
| Bois de Castelló d'Empúries (10) ⚠️ | Castelló d'Empúries › Alt Empordà | 1 |
| Forêt de Llanars (2) ⚠️ | Llanars › Ripollès | 1 |
| Forêt de Setcases (24) ⚠️ | Setcases › Ripollès | 1 |
| Forêt de Llanars (3) ⚠️ | Llanars › Ripollès | 1 |
| Forêt de Vilallonga de Ter (3) ⚠️ | Vilallonga de Ter › Ripollès | 1 |
| Forêt de Riudellots de la Selva (18) ⚠️ | Riudellots de la Selva › la Selva (Gérone) | 1 |
| Bois de Vilallonga de Ter (2) ⚠️ | Vilallonga de Ter › Ripollès | 1 |
| Parc de Castell d'Aro, Platja d'Aro i s'Agaró (40) ⚠️ | Castell d'Aro, Platja d'Aro i s'Agaró › Baix Empordà | 1 |
| Forêt de Sant Pau de Segúries ⚠️ | Sant Pau de Segúries › Ripollès | 1 |
| Forêt de Sant Pau de Segúries (2) ⚠️ | Sant Pau de Segúries › Ripollès | 1 |
| Forêt de Blanes (10) ⚠️ | Blanes › la Selva (Gérone) | 1 |
| Parc de l'Escala (8) ⚠️ | l'Escala › Alt Empordà | 1 |
| Forêt de el Port de la Selva (8) ⚠️ | el Port de la Selva › Alt Empordà | 1 |
| Forêt de el Port de la Selva (11) ⚠️ | el Port de la Selva › Alt Empordà | 1 |
| Forêt de Llançà (6) ⚠️ | Llançà › Alt Empordà | 1 |
| Forêt de Palau-saverdera (2) ⚠️ | Palau-saverdera › Alt Empordà | 1 |
| Camp dels caçadors ⚠️ | Rabós › Alt Empordà | 1 |
| Bois de Pardines (2) ⚠️ | Pardines › Ripollès | 1 |
| Bois de Pardines (4) ⚠️ | Pardines › Ripollès | 1 |
| Bois de Quart (4) ⚠️ | Quart › Gironès | 1 |
| Bois de Quart (5) ⚠️ | Quart › Gironès | 1 |
| Forêt de Celrà (8) ⚠️ | Celrà › Gironès | 1 |
| Turonet del Pla de Dalt ⚠️ | Olot › Garrotxa | 1 |
| Forêt de Toses (4) ⚠️ | Toses › Ripollès | 1 |
| Forêt de Gombrèn (2) ⚠️ | Gombrèn › Ripollès | 1 |
| Forêt de Bàscara (7) ⚠️ | Bàscara › Alt Empordà | 1 |
| Forêt de Bàscara (9) ⚠️ | Bàscara › Alt Empordà | 1 |
| Forêt de Bàscara (11) ⚠️ | Bàscara › Alt Empordà | 1 |
| Pícnic Pavelló ⚠️ | Bescanó › Gironès | 1 |
| Bois de Riudarenes (2) ⚠️ | Riudarenes › la Selva (Gérone) | 1 |
| Parc de Sant Ramon ⚠️ | Castell d'Aro, Platja d'Aro i s'Agaró › Baix Empordà | 1 |
| Forêt de Santa Pau (5) ⚠️ | Santa Pau › Garrotxa | 1 |
| Forêt de Santa Pau (7) ⚠️ | Santa Pau › Garrotxa | 1 |
| Forêt de Santa Pau (11) ⚠️ | Santa Pau › Garrotxa | 1 |
| Forêt de Santa Coloma de Farners (9) ⚠️ | Santa Coloma de Farners › la Selva (Gérone) | 1 |
| Forêt de Santa Coloma de Farners (10) ⚠️ | Santa Coloma de Farners › la Selva (Gérone) | 1 |
| Bois de Cassà de la Selva (2) ⚠️ | Cassà de la Selva › Gironès | 1 |
| Parc de Riells i Viabrea (4) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 1 |
| Forêt de Llívia (4) ⚠️ | Llívia › Cerdanya (Gérone) | 1 |
| Forêt de Llívia (6) ⚠️ | Llívia › Cerdanya (Gérone) | 1 |
| Forêt de Sant Jordi Desvalls (3) ⚠️ | Sant Jordi Desvalls › Gironès | 1 |
| Parc del Vuit de Març ⚠️ | la Bisbal d'Empordà › Baix Empordà | 1 |
| Plaça Narcís de Carreras ⚠️ | la Bisbal d'Empordà › Baix Empordà | 1 |
| Forêt de Riells i Viabrea (3) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 1 |
| Forêt de Riells i Viabrea (7) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 1 |
| Forêt de Riells i Viabrea (9) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 1 |
| Forêt de Riells i Viabrea (11) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 1 |
| Bois de Llançà (3) ⚠️ | Llançà › Alt Empordà | 1 |
| Parc Xingurri ⚠️ | les Preses › Garrotxa | 1 |
| Forêt de Espinelves (7) ⚠️ | Espinelves › Osona (Gérone) | 1 |
| Bois de Bescanó (3) ⚠️ | Bescanó › Gironès | 1 |
| Bois de Bescanó (5) ⚠️ | Bescanó › Gironès | 1 |
| Forêt de Meranges (2) ⚠️ | Meranges › Cerdanya (Gérone) | 1 |
| Forêt de la Tallada d'Empordà (5) ⚠️ | la Tallada d'Empordà › Baix Empordà | 1 |
| Rost d'en Thió ⚠️ | Bescanó › Gironès | 1 |
| Forêt de Santa Coloma de Farners (12) ⚠️ | Santa Coloma de Farners › la Selva (Gérone) | 1 |
| Parc de Viladrau ⚠️ | Viladrau › Osona (Gérone) | 1 |
| Bois de Santa Coloma de Farners (14) ⚠️ | Santa Coloma de Farners › la Selva (Gérone) | 1 |
| Bois de Santa Coloma de Farners (17) ⚠️ | Santa Coloma de Farners › la Selva (Gérone) | 1 |
| Bois de Santa Coloma de Farners (18) ⚠️ | Santa Coloma de Farners › la Selva (Gérone) | 1 |
| Bois de Santa Coloma de Farners (19) ⚠️ | Santa Coloma de Farners › la Selva (Gérone) | 1 |
| Bois de Santa Coloma de Farners (20) ⚠️ | Santa Coloma de Farners › la Selva (Gérone) | 1 |
| Bois de Santa Coloma de Farners (24) ⚠️ | Santa Coloma de Farners › la Selva (Gérone) | 1 |
| Forêt de Setcases (33) ⚠️ | Setcases › Ripollès | 1 |
| Bois de Llagostera (4) ⚠️ | Llagostera › Gironès | 1 |
| Bois de Llagostera (11) ⚠️ | Llagostera › Gironès | 1 |
| Bois de Llagostera (15) ⚠️ | Llagostera › Gironès | 1 |
| Bois de Llagostera (17) ⚠️ | Llagostera › Gironès | 1 |
| Bois de Roses (4) ⚠️ | Roses › Alt Empordà | 1 |
| Bois de Roses (11) ⚠️ | Roses › Alt Empordà | 1 |
| Bois de Roses (26) ⚠️ | Roses › Alt Empordà | 1 |
| Bois de Roses (32) ⚠️ | Roses › Alt Empordà | 1 |
| Bois de Roses (50) ⚠️ | Roses › Alt Empordà | 1 |
| Bois de Palau-saverdera (3) ⚠️ | Roses › Alt Empordà | 1 |
| Bois de Palau-saverdera (5) ⚠️ | Palau-saverdera › Alt Empordà | 1 |
| Bois de Palau-saverdera (10) ⚠️ | Palau-saverdera › Alt Empordà | 1 |
| Bois de Roses (63) ⚠️ | Roses › Alt Empordà | 1 |
| Parc de Palamós (26) ⚠️ | Palamós › Baix Empordà | 1 |
| Bois de Palau-saverdera (13) ⚠️ | Palau-saverdera › Alt Empordà | 1 |
| Bois de Roses (77) ⚠️ | Roses › Alt Empordà | 1 |
| Bois de Palau-saverdera (18) ⚠️ | Palau-saverdera › Alt Empordà | 1 |
| Bois de Palau-saverdera (43) ⚠️ | Palau-saverdera › Alt Empordà | 1 |
| Bois de Palau-saverdera (44) ⚠️ | Palau-saverdera › Alt Empordà | 1 |
| Bois de Palau-saverdera (66) ⚠️ | Palau-saverdera › Alt Empordà | 1 |
| Bois de Castelló d'Empúries (12) ⚠️ | Castelló d'Empúries › Alt Empordà | 1 |
| Bois de Palau-saverdera (70) ⚠️ | Palau-saverdera › Alt Empordà | 1 |
| Bois de Roses (90) ⚠️ | Roses › Alt Empordà | 1 |
| Bois de Roses (91) ⚠️ | Roses › Alt Empordà | 1 |
| Bois de Palau-saverdera (79) ⚠️ | Palau-saverdera › Alt Empordà | 1 |
| Bois de Palau-saverdera (83) ⚠️ | Palau-saverdera › Alt Empordà | 1 |
| Bois de Palau-saverdera (87) ⚠️ | Palau-saverdera › Alt Empordà | 1 |
| Bois de Pau ⚠️ | Pau › Alt Empordà | 1 |
| Parc de Riudellots de la Selva (8) ⚠️ | Riudellots de la Selva › la Selva (Gérone) | 1 |
| Bois de Palau-saverdera (97) ⚠️ | Palau-saverdera › Alt Empordà | 1 |
| Bois de Pau (14) ⚠️ | Pau › Alt Empordà | 1 |
| Bois de Roses (101) ⚠️ | Roses › Alt Empordà | 1 |
| Parc del barri de l'Est ⚠️ | Quart › Gironès | 1 |
| Forêt de Santa Cristina d'Aro (20) ⚠️ | Santa Cristina d'Aro › Baix Empordà | 1 |
| Parc de Palamós (28) ⚠️ | Palamós › Baix Empordà | 1 |
| Forêt de Esponellà (3) ⚠️ | Esponellà › Pla de l'Estany | 1 |
| Parc del Riu ⚠️ | Sant Pere Pescador › Alt Empordà | 1 |
| Parc de Girona (65) ⚠️ | Girona › Gironès | 1 |
| Parc del Migdia ⚠️ | Girona › Gironès | 1 |
| La Parada del Jonquer ⚠️ | les Planes d'Hostoles › Garrotxa | 1 |
| Forêt de la Cellera de Ter (18) ⚠️ | la Cellera de Ter › la Selva (Gérone) | 1 |
| Bois de la Cellera de Ter (5) ⚠️ | la Cellera de Ter › la Selva (Gérone) | 1 |
| Bois de la Cellera de Ter (6) ⚠️ | la Cellera de Ter › la Selva (Gérone) | 1 |
| Forêt de la Cellera de Ter (19) ⚠️ | la Cellera de Ter › la Selva (Gérone) | 1 |
| Forêt de la Cellera de Ter (20) ⚠️ | la Cellera de Ter › la Selva (Gérone) | 1 |
| Forêt de Bescanó (15) ⚠️ | Bescanó › Gironès | 1 |
| Bois de Bescanó (6) ⚠️ | Bescanó › Gironès | 1 |
| Forêt de Foixà (9) ⚠️ | Foixà › Baix Empordà | 1 |
| Forêt de Foixà (11) ⚠️ | Foixà › Baix Empordà | 1 |
| Forêt de Cruïlles, Monells i Sant Sadurní de l'Heura (30) ⚠️ | Cruïlles, Monells i Sant Sadurní de l'Heura › Baix Empordà | 1 |
| Jardins de Santa Clotilde ⚠️ | Lloret de Mar › la Selva (Gérone) | 1 |
| Forêt de Sant Gregori (23) ⚠️ | Sant Gregori › Gironès | 1 |
| Forêt de Anglès (7) ⚠️ | Anglès › la Selva (Gérone) | 1 |
| Forêt de Palafrugell (114) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Forêt de Palafrugell (115) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Forêt de Sant Llorenç de la Muga (4) ⚠️ | Sant Llorenç de la Muga › Alt Empordà | 1 |
| Forêt de Bescanó (17) ⚠️ | Bescanó › Gironès | 1 |
| Forêt de Girona (64) ⚠️ | Girona › Gironès | 1 |
| Bois de Porqueres (8) ⚠️ | Porqueres › Pla de l'Estany | 1 |
| Bois de Porqueres (10) ⚠️ | Porqueres › Pla de l'Estany | 1 |
| Bois de Porqueres (11) ⚠️ | Porqueres › Pla de l'Estany | 1 |
| Parc de Banyoles (18) ⚠️ | Banyoles › Pla de l'Estany | 1 |
| Plaça de la Diputació ⚠️ | Salt › Gironès | 1 |
| Bois de Salt (7) ⚠️ | Salt › Gironès | 1 |
| Forêt de Salt (3) ⚠️ | Salt › Gironès | 1 |
| Forêt de Girona (67) ⚠️ | Salt › Gironès | 1 |
| Forêt de Porqueres (4) ⚠️ | Porqueres › Pla de l'Estany | 1 |
| Bois de Porqueres (12) ⚠️ | Porqueres › Pla de l'Estany | 1 |
| Forêt de Banyoles (9) ⚠️ | Banyoles › Pla de l'Estany | 1 |
| Forêt de Banyoles (10) ⚠️ | Banyoles › Pla de l'Estany | 1 |
| Parc de l'U d'Octubre ⚠️ | Banyoles › Pla de l'Estany | 1 |
| Parc de Banyoles (29) ⚠️ | Banyoles › Pla de l'Estany | 1 |
| Parc de Banyoles (32) ⚠️ | Banyoles › Pla de l'Estany | 1 |
| Forêt de Banyoles (11) ⚠️ | Banyoles › Pla de l'Estany | 1 |
| Parc de Figueres (11) ⚠️ | Figueres › Alt Empordà | 1 |
| Parc de Girona (71) ⚠️ | Girona › Gironès | 1 |
| Forêt de Fornells de la Selva (20) ⚠️ | Fornells de la Selva › Gironès | 1 |
| Forêt de Fornells de la Selva (22) ⚠️ | Fornells de la Selva › Gironès | 1 |
| Forêt de Aiguaviva (25) ⚠️ | Aiguaviva › Gironès | 1 |
| Plaça de Palau ⚠️ | Girona › Gironès | 1 |
| Parc de Girona (73) ⚠️ | Girona › Gironès | 1 |
| Parc de Girona (74) ⚠️ | Girona › Gironès | 1 |
| Bois de Porqueres (14) ⚠️ | Porqueres › Pla de l'Estany | 1 |
| Forêt de Camós (7) ⚠️ | Camós › Pla de l'Estany | 1 |
| Forêt de Cornellà del Terri (21) ⚠️ | Cornellà del Terri › Pla de l'Estany | 1 |
| Forêt de Sant Gregori (26) ⚠️ | Sant Gregori › Gironès | 1 |
| Parc de Cornellà del Terri (2) ⚠️ | Cornellà del Terri › Pla de l'Estany | 1 |
| Forêt de el Port de la Selva (12) ⚠️ | el Port de la Selva › Alt Empordà | 1 |
| Parc de Cornellà del Terri (9) ⚠️ | Cornellà del Terri › Pla de l'Estany | 1 |
| Bois de la Cellera de Ter (8) ⚠️ | Amer › la Selva (Gérone) | 1 |
| Bois de la Cellera de Ter (9) ⚠️ | la Cellera de Ter › la Selva (Gérone) | 1 |
| Forêt de la Cellera de Ter (29) ⚠️ | la Cellera de Ter › la Selva (Gérone) | 1 |
| Forêt de Sant Julià del Llor i Bonmatí (3) ⚠️ | Sant Julià del Llor i Bonmatí › la Selva (Gérone) | 1 |
| Forêt de Bescanó (22) ⚠️ | Bescanó › Gironès | 1 |
| Parc de Girona (75) ⚠️ | Girona › Gironès | 1 |
| Forêt de Bescanó (24) ⚠️ | Bescanó › Gironès | 1 |
| Forêt de Alp (91) ⚠️ | Alp › Cerdanya (Gérone) | 1 |
| Forêt de Calonge i Sant Antoni (26) ⚠️ | Calonge i Sant Antoni › Baix Empordà | 1 |
| Parc de Sant Miquel de Campmajor ⚠️ | Sant Miquel de Campmajor › Pla de l'Estany | 1 |
| Forêt de Castellfollit de la Roca ⚠️ | Castellfollit de la Roca › Garrotxa | 1 |
| Forêt de Castellfollit de la Roca (2) ⚠️ | Castellfollit de la Roca › Garrotxa | 1 |
| Parc de Sant Jaume de Llierca ⚠️ | Sant Jaume de Llierca › Garrotxa | 1 |
| Forêt de Fornells de la Selva (24) ⚠️ | Fornells de la Selva › Gironès | 1 |
| Forêt de Aiguaviva (33) ⚠️ | Aiguaviva › Gironès | 1 |
| Forêt de Besalú (7) ⚠️ | Besalú › Garrotxa | 1 |
| Forêt de Besalú (8) ⚠️ | Besalú › Garrotxa | 1 |
| Forêt de Palol de Revardit (6) ⚠️ | Palol de Revardit › Pla de l'Estany | 1 |
| Bois de Mieres (2) ⚠️ | Mieres › Garrotxa | 1 |
| Forêt de Ger (6) ⚠️ | Ger › Cerdanya (Gérone) | 1 |
| Forêt de Porqueres (13) ⚠️ | Porqueres › Pla de l'Estany | 1 |
| Forêt de Banyoles (15) ⚠️ | Banyoles › Pla de l'Estany | 1 |
| Parc de Banyoles (36) ⚠️ | Banyoles › Pla de l'Estany | 1 |
| Forêt de Queralbs (27) ⚠️ | Queralbs › Ripollès | 1 |
| Forêt de Banyoles (19) ⚠️ | Banyoles › Pla de l'Estany | 1 |
| Forêt de Isòvol (7) ⚠️ | Isòvol › Cerdanya (Gérone) | 1 |
| Jardins de les Pedreres ⚠️ | Girona › Gironès | 1 |
| Forêt de Begur (21) ⚠️ | Begur › Baix Empordà | 1 |
| Forêt de Begur (30) ⚠️ | Begur › Baix Empordà | 1 |
| Forêt de Begur (32) ⚠️ | Begur › Baix Empordà | 1 |
| Forêt de Palafrugell (119) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Forêt de Begur (34) ⚠️ | Begur › Baix Empordà | 1 |
| Forêt de Palafrugell (124) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Bois de Calonge i Sant Antoni (6) ⚠️ | Calonge i Sant Antoni › Baix Empordà | 1 |
| Aparcament Club Nàutic Port d'Aro ⚠️ | Castell d'Aro, Platja d'Aro i s'Agaró › Baix Empordà | 1 |
| Forêt de Castell d'Aro, Platja d'Aro i s'Agaró (26) ⚠️ | Castell d'Aro, Platja d'Aro i s'Agaró › Baix Empordà | 1 |
| Forêt de Calonge i Sant Antoni (29) ⚠️ | Calonge i Sant Antoni › Baix Empordà | 1 |
| Forêt de Sant Feliu de Guíxols (26) ⚠️ | Sant Feliu de Guíxols › Baix Empordà | 1 |
| Forêt de Tossa de Mar (18) ⚠️ | Tossa de Mar › la Selva (Gérone) | 1 |
| Forêt de Tossa de Mar (21) ⚠️ | Tossa de Mar › la Selva (Gérone) | 1 |
| Forêt de Santa Cristina d'Aro (26) ⚠️ | Santa Cristina d'Aro › Baix Empordà | 1 |
| Forêt de Lloret de Mar (30) ⚠️ | Lloret de Mar › la Selva (Gérone) | 1 |
| Forêt de Begur (41) ⚠️ | Begur › Baix Empordà | 1 |
| Forêt de Begur (42) ⚠️ | Begur › Baix Empordà | 1 |
| Forêt de Roses (12) ⚠️ | Roses › Alt Empordà | 1 |
| Forêt de Roses (14) ⚠️ | Roses › Alt Empordà | 1 |
| Forêt de Roses (18) ⚠️ | Roses › Alt Empordà | 1 |
| Forêt de Cadaqués (5) ⚠️ | Cadaqués › Alt Empordà | 1 |
| Forêt de Cadaqués (6) ⚠️ | Cadaqués › Alt Empordà | 1 |
| Forêt de Cadaqués (9) ⚠️ | Cadaqués › Alt Empordà | 1 |
| Forêt de el Port de la Selva (14) ⚠️ | el Port de la Selva › Alt Empordà | 1 |
| Forêt de Colera (7) ⚠️ | Colera › Alt Empordà | 1 |
| Forêt de Llançà (15) ⚠️ | Llançà › Alt Empordà | 1 |
| Forêt de el Port de la Selva (19) ⚠️ | el Port de la Selva › Alt Empordà | 1 |
| Forêt de Llançà (24) ⚠️ | Llançà › Alt Empordà | 1 |
| Forêt de Colera (12) ⚠️ | Colera › Alt Empordà | 1 |
| Forêt de Cadaqués (14) ⚠️ | Cadaqués › Alt Empordà | 1 |
| Forêt de Cadaqués (16) ⚠️ | Cadaqués › Alt Empordà | 1 |
| Forêt de Setcases (36) ⚠️ | Setcases › Ripollès | 1 |
| Forêt de Setcases (40) ⚠️ | Setcases › Ripollès | 1 |
| Forêt de Setcases (42) ⚠️ | Setcases › Ripollès | 1 |
| Forêt de Setcases (45) ⚠️ | Setcases › Ripollès | 1 |
| Forêt de Setcases (48) ⚠️ | Setcases › Ripollès | 1 |
| Forêt de Setcases (56) ⚠️ | Setcases › Ripollès | 1 |
| Forêt de Setcases (58) ⚠️ | Setcases › Ripollès | 1 |
| Forêt de Setcases (59) ⚠️ | Setcases › Ripollès | 1 |
| Forêt de Setcases (60) ⚠️ | Setcases › Ripollès | 1 |
| Forêt de Setcases (61) ⚠️ | Setcases › Ripollès | 1 |
| Forêt de Ripoll (15) ⚠️ | Ripoll › Ripollès | 1 |
| Forêt de Ripoll (22) ⚠️ | Ripoll › Ripollès | 1 |
| Forêt de Ripoll (28) ⚠️ | Ripoll › Ripollès | 1 |
| Forêt de Ripoll (31) ⚠️ | Ripoll › Ripollès | 1 |
| Parc de Camprodon (3) ⚠️ | Camprodon › Ripollès | 1 |
| Forêt de Camprodon (15) ⚠️ | Camprodon › Ripollès | 1 |
| Forêt de Camprodon (16) ⚠️ | Camprodon › Ripollès | 1 |
| Forêt de Santa Pau (16) ⚠️ | Santa Pau › Garrotxa | 1 |
| Forêt de Sant Joan les Fonts (4) ⚠️ | Sant Joan les Fonts › Garrotxa | 1 |
| Forêt de la Vall de Bianya (7) ⚠️ | la Vall de Bianya › Garrotxa | 1 |
| Forêt de Sant Joan les Fonts (7) ⚠️ | Sant Joan les Fonts › Garrotxa | 1 |
| Forêt de Alp (93) ⚠️ | Alp › Cerdanya (Gérone) | 1 |
| Forêt de Alp (96) ⚠️ | Alp › Cerdanya (Gérone) | 1 |
| Forêt de Alp (98) ⚠️ | Alp › Cerdanya (Gérone) | 1 |
| Forêt de Osor (19) ⚠️ | Osor › la Selva (Gérone) | 1 |
| Forêt de Llançà (26) ⚠️ | Llançà › Alt Empordà | 1 |
| Forêt de Calonge i Sant Antoni (35) ⚠️ | Calonge i Sant Antoni › Baix Empordà | 1 |
| Forêt de Calonge i Sant Antoni (38) ⚠️ | Calonge i Sant Antoni › Baix Empordà | 1 |
| Forêt de Pals (10) ⚠️ | Pals › Baix Empordà | 1 |
| Parc dels Vinyers ⚠️ | Calonge i Sant Antoni › Baix Empordà | 1 |
| Forêt de Vall-llobrega (4) ⚠️ | Vall-llobrega › Baix Empordà | 1 |
| Forêt de Lloret de Mar (39) ⚠️ | Lloret de Mar › la Selva (Gérone) | 1 |
| Forêt de Lloret de Mar (45) ⚠️ | Lloret de Mar › la Selva (Gérone) | 1 |
| Forêt de l'Escala (35) ⚠️ | l'Escala › Alt Empordà | 1 |
| Forêt de Toses (19) ⚠️ | Toses › Ripollès | 1 |
| Forêt de Ribes de Freser (16) ⚠️ | Ribes de Freser › Ripollès | 1 |
| Parc de la Sardana ⚠️ | Caldes de Malavella › la Selva (Gérone) | 1 |
| Forêt de les Llosses (46) ⚠️ | les Llosses › Ripollès | 1 |
| Forêt de Ripoll (41) ⚠️ | Ripoll › Ripollès | 1 |
| Forêt de Pals (15) ⚠️ | Pals › Baix Empordà | 1 |
| Forêt de Pals (16) ⚠️ | Pals › Baix Empordà | 1 |
| Parc de Sarrià de Ter (9) ⚠️ | Sarrià de Ter › Gironès | 1 |
| Forêt de Pals (19) ⚠️ | Pals › Baix Empordà | 1 |
| Forêt de Pals (20) ⚠️ | Pals › Baix Empordà | 1 |
| Forêt de Pals (21) ⚠️ | Pals › Baix Empordà | 1 |
| Forêt de Pals (22) ⚠️ | Pals › Baix Empordà | 1 |
| Forêt de Torroella de Montgrí (81) ⚠️ | Torroella de Montgrí › Baix Empordà | 1 |
| Forêt de Torroella de Montgrí (82) ⚠️ | Torroella de Montgrí › Baix Empordà | 1 |
| Forêt de Torroella de Montgrí (83) ⚠️ | Torroella de Montgrí › Baix Empordà | 1 |
| Forêt de Pals (23) ⚠️ | Pals › Baix Empordà | 1 |
| Forêt de Pals (24) ⚠️ | Pals › Baix Empordà | 1 |
| Forêt de Pals (25) ⚠️ | Pals › Baix Empordà | 1 |
| Pineda d'en Negre ⚠️ | Torroella de Montgrí › Baix Empordà | 1 |
| Forêt de Torroella de Montgrí (90) ⚠️ | Torroella de Montgrí › Baix Empordà | 1 |
| Forêt de Pals (27) ⚠️ | Pals › Baix Empordà | 1 |
| Forêt de Pals (31) ⚠️ | Pals › Baix Empordà | 1 |
| Forêt de les Llosses (53) ⚠️ | les Llosses › Ripollès | 1 |
| Forêt de les Llosses (54) ⚠️ | les Llosses › Ripollès | 1 |
| Forêt de Puigcerdà (4) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Puigcerdà (5) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Guils de Cerdanya (2) ⚠️ | Guils de Cerdanya › Cerdanya (Gérone) | 1 |
| Forêt de Pals (36) ⚠️ | Pals › Baix Empordà | 1 |
| Forêt de Pals (44) ⚠️ | Pals › Baix Empordà | 1 |
| Forêt de Pals (47) ⚠️ | Pals › Baix Empordà | 1 |
| Forêt de Pals (51) ⚠️ | Pals › Baix Empordà | 1 |
| Forêt de Pals (52) ⚠️ | Pals › Baix Empordà | 1 |
| Forêt de Pals (53) ⚠️ | Pals › Baix Empordà | 1 |
| Forêt de Palau-sator (15) ⚠️ | Palau-sator › Baix Empordà | 1 |
| Forêt de Torrent (6) ⚠️ | Torrent › Baix Empordà | 1 |
| Forêt de Pals (57) ⚠️ | Pals › Baix Empordà | 1 |
| Forêt de Pals (60) ⚠️ | Pals › Baix Empordà | 1 |
| Forêt de Palau-sator (16) ⚠️ | Palau-sator › Baix Empordà | 1 |
| Forêt de Torrent (9) ⚠️ | Torrent › Baix Empordà | 1 |
| Forêt de la Bisbal d'Empordà (9) ⚠️ | la Bisbal d'Empordà › Baix Empordà | 1 |
| Forêt de la Bisbal d'Empordà (13) ⚠️ | la Bisbal d'Empordà › Baix Empordà | 1 |
| Forêt de la Bisbal d'Empordà (17) ⚠️ | la Bisbal d'Empordà › Baix Empordà | 1 |
| Bois de Vilallonga de Ter (4) ⚠️ | Vilallonga de Ter › Ripollès | 1 |
| Bois de Vilallonga de Ter (7) ⚠️ | Vilallonga de Ter › Ripollès | 1 |
| Bois de Vilallonga de Ter (10) ⚠️ | Vilallonga de Ter › Ripollès | 1 |
| Forêt de les Llosses (77) ⚠️ | les Llosses › Ripollès | 1 |
| Forêt de Olot (16) ⚠️ | Olot › Garrotxa | 1 |
| Forêt de les Planes d'Hostoles (5) ⚠️ | les Planes d'Hostoles › Garrotxa | 1 |
| Forêt de Sant Feliu de Pallerols (9) ⚠️ | Sant Feliu de Pallerols › Garrotxa | 1 |
| Forêt de la Vall d'en Bas (17) ⚠️ | la Vall d'en Bas › Garrotxa | 1 |
| Forêt de les Llosses (82) ⚠️ | les Llosses › Ripollès | 1 |
| Forêt de Riudarenes (20) ⚠️ | Riudarenes › la Selva (Gérone) | 1 |
| Forêt de Pals (68) ⚠️ | Pals › Baix Empordà | 1 |
| Forêt de Pals (72) ⚠️ | Pals › Baix Empordà | 1 |
| Forêt de Pals (74) ⚠️ | Pals › Baix Empordà | 1 |
| Forêt de Pals (76) ⚠️ | Pals › Baix Empordà | 1 |
| Forêt de Pals (78) ⚠️ | Pals › Baix Empordà | 1 |
| Forêt de Pals (83) ⚠️ | Pals › Baix Empordà | 1 |
| Forêt de Viladrau (39) ⚠️ | Viladrau › Osona (Gérone) | 1 |
| Forêt de Viladrau (44) ⚠️ | Viladrau › Osona (Gérone) | 1 |
| Forêt de Viladrau (45) ⚠️ | Viladrau › Osona (Gérone) | 1 |
| Forêt de Riells i Viabrea (16) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 1 |
| Bois de Sant Joan de les Abadesses ⚠️ | Sant Joan de les Abadesses › Ripollès | 1 |
| Parc de Figueres (12) ⚠️ | Figueres › Alt Empordà | 1 |
| Passeig de Santa Caterina ⚠️ | Ribes de Freser › Ripollès | 1 |
| Parc de l'Armentera ⚠️ | l'Armentera › Alt Empordà | 1 |
| Parc de Torroella de Fluvià ⚠️ | Torroella de Fluvià › Alt Empordà | 1 |
| Forêt de Fontanals de Cerdanya (4) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 1 |
| Forêt de Fontanals de Cerdanya (6) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 1 |
| Forêt de Fontanals de Cerdanya (10) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 1 |
| Forêt de Puigcerdà (9) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Puigcerdà (11) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Puigcerdà (12) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Fontanals de Cerdanya (13) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 1 |
| Forêt de Puigcerdà (16) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Puigcerdà (22) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Bolvir (7) ⚠️ | Bolvir › Cerdanya (Gérone) | 1 |
| Forêt de Bolvir (16) ⚠️ | Bolvir › Cerdanya (Gérone) | 1 |
| Forêt de Guils de Cerdanya (4) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Puigcerdà (37) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Puigcerdà (39) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Puigcerdà (46) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Puigcerdà (48) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Puigcerdà (55) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Puigcerdà (56) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Parc Cordomí ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Puigcerdà (61) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Puigcerdà (62) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Puigcerdà (65) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Puigcerdà (66) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Puigcerdà (71) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Puigcerdà (80) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Puigcerdà (82) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Puigcerdà (83) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Puigcerdà (86) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Puigcerdà (90) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Puigcerdà (92) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Puigcerdà (99) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Puigcerdà (101) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Puigcerdà (103) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Puigcerdà (111) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Guils de Cerdanya (7) ⚠️ | Guils de Cerdanya › Cerdanya (Gérone) | 1 |
| Forêt de Guils de Cerdanya (9) ⚠️ | Guils de Cerdanya › Cerdanya (Gérone) | 1 |
| Forêt de Guils de Cerdanya (10) ⚠️ | Guils de Cerdanya › Cerdanya (Gérone) | 1 |
| Forêt de Guils de Cerdanya (18) ⚠️ | Guils de Cerdanya › Cerdanya (Gérone) | 1 |
| Forêt de Guils de Cerdanya (21) ⚠️ | Guils de Cerdanya › Cerdanya (Gérone) | 1 |
| Forêt de Guils de Cerdanya (27) ⚠️ | Guils de Cerdanya › Cerdanya (Gérone) | 1 |
| Forêt de Ger (10) ⚠️ | Ger › Cerdanya (Gérone) | 1 |
| Forêt de Bolvir (17) ⚠️ | Bolvir › Cerdanya (Gérone) | 1 |
| Forêt de Ger (14) ⚠️ | Ger › Cerdanya (Gérone) | 1 |
| Forêt de Ger (15) ⚠️ | Ger › Cerdanya (Gérone) | 1 |
| Forêt de Ger (18) ⚠️ | Ger › Cerdanya (Gérone) | 1 |
| Forêt de Guils de Cerdanya (36) ⚠️ | Guils de Cerdanya › Cerdanya (Gérone) | 1 |
| Forêt de Guils de Cerdanya (44) ⚠️ | Guils de Cerdanya › Cerdanya (Gérone) | 1 |
| Forêt de Fontanals de Cerdanya (19) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 1 |
| Forêt de Fontanals de Cerdanya (20) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 1 |
| Forêt de Fontanals de Cerdanya (23) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 1 |
| Forêt de Fontanals de Cerdanya (27) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 1 |
| Forêt de Fontanals de Cerdanya (28) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 1 |
| Forêt de Fontanals de Cerdanya (33) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 1 |
| Forêt de Fontanals de Cerdanya (36) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 1 |
| Forêt de Fontanals de Cerdanya (39) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 1 |
| Forêt de Fontanals de Cerdanya (41) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 1 |
| Parc de Fontanals de Cerdanya (4) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 1 |
| Forêt de Fontanals de Cerdanya (43) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 1 |
| Forêt de Fontanals de Cerdanya (52) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 1 |
| Forêt de Fontanals de Cerdanya (53) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 1 |
| Forêt de Alp (102) ⚠️ | Alp › Cerdanya (Gérone) | 1 |
| Parc de Fontanals de Cerdanya (5) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 1 |
| Forêt de Fontanals de Cerdanya (56) ⚠️ | Fontanals de Cerdanya › Cerdanya (Gérone) | 1 |
| Forêt de Urús (5) ⚠️ | Urús › Cerdanya (Gérone) | 1 |
| Forêt de Urús (12) ⚠️ | Urús › Cerdanya (Gérone) | 1 |
| Forêt de les Llosses (83) ⚠️ | les Llosses › Ripollès | 1 |
| Forêt de les Llosses (86) ⚠️ | les Llosses › Ripollès | 1 |
| Forêt de les Llosses (97) ⚠️ | les Llosses › Ripollès | 1 |
| Forêt de Campdevànol (19) ⚠️ | Campdevànol › Ripollès | 1 |
| Forêt de Gombrèn (30) ⚠️ | Gombrèn › Ripollès | 1 |
| Forêt de Gombrèn (44) ⚠️ | Gombrèn › Ripollès | 1 |
| Forêt de Gombrèn (50) ⚠️ | Gombrèn › Ripollès | 1 |
| Forêt de Campdevànol (32) ⚠️ | Campdevànol › Ripollès | 1 |
| Forêt de Campdevànol (36) ⚠️ | Campdevànol › Ripollès | 1 |
| Forêt de Campdevànol (37) ⚠️ | Campdevànol › Ripollès | 1 |
| Forêt de Gombrèn (66) ⚠️ | Gombrèn › Ripollès | 1 |
| Forêt de Campdevànol (51) ⚠️ | Campdevànol › Ripollès | 1 |
| Forêt de Campdevànol (52) ⚠️ | Campdevànol › Ripollès | 1 |
| Forêt de Campdevànol (55) ⚠️ | Campdevànol › Ripollès | 1 |
| Forêt de Campdevànol (56) ⚠️ | Campdevànol › Ripollès | 1 |
| Forêt de Campdevànol (65) ⚠️ | Campdevànol › Ripollès | 1 |
| Forêt de Campdevànol (66) ⚠️ | Campdevànol › Ripollès | 1 |
| Forêt de Campdevànol (68) ⚠️ | Campdevànol › Ripollès | 1 |
| Forêt de Ripoll (50) ⚠️ | Ripoll › Ripollès | 1 |
| Forêt de Ripoll (51) ⚠️ | Ripoll › Ripollès | 1 |
| Forêt de Ripoll (52) ⚠️ | Ripoll › Ripollès | 1 |
| Forêt de Ribes de Freser (28) ⚠️ | Ribes de Freser › Ripollès | 1 |
| Forêt de Ripoll (55) ⚠️ | Ripoll › Ripollès | 1 |
| Forêt de Campdevànol (76) ⚠️ | Campdevànol › Ripollès | 1 |
| Forêt de Vallfogona de Ripollès (11) ⚠️ | Vallfogona de Ripollès › Ripollès | 1 |
| Forêt de Vallfogona de Ripollès (12) ⚠️ | Vallfogona de Ripollès › Ripollès | 1 |
| Forêt de Ripoll (57) ⚠️ | Ripoll › Ripollès | 1 |
| Forêt de Ripoll (63) ⚠️ | Ripoll › Ripollès | 1 |
| Forêt de Ripoll (64) ⚠️ | Ripoll › Ripollès | 1 |
| Forêt de Ripoll (69) ⚠️ | Ripoll › Ripollès | 1 |
| Forêt de Ripoll (70) ⚠️ | Ripoll › Ripollès | 1 |
| Forêt de Ripoll (72) ⚠️ | Ripoll › Ripollès | 1 |
| Forêt de Vallfogona de Ripollès (17) ⚠️ | Vallfogona de Ripollès › Ripollès | 1 |
| Forêt de Vallfogona de Ripollès (21) ⚠️ | Vallfogona de Ripollès › Ripollès | 1 |
| Forêt de Sales de Llierca (3) ⚠️ | Sales de Llierca › Garrotxa | 1 |
| Forêt de Montagut i Oix (3) ⚠️ | Montagut i Oix › Garrotxa | 1 |
| Forêt de Sales de Llierca (11) ⚠️ | Sales de Llierca › Garrotxa | 1 |
| Forêt de Sales de Llierca (12) ⚠️ | Sales de Llierca › Garrotxa | 1 |
| Forêt de Sales de Llierca (13) ⚠️ | Sales de Llierca › Garrotxa | 1 |
| Forêt de Montagut i Oix (14) ⚠️ | Montagut i Oix › Garrotxa | 1 |
| Forêt de Montagut i Oix (22) ⚠️ | Montagut i Oix › Garrotxa | 1 |
| Forêt de Montagut i Oix (32) ⚠️ | Montagut i Oix › Garrotxa | 1 |
| Forêt de Montagut i Oix (41) ⚠️ | Montagut i Oix › Garrotxa | 1 |
| Forêt de Montagut i Oix (48) ⚠️ | Montagut i Oix › Garrotxa | 1 |
| Forêt de Montagut i Oix (58) ⚠️ | Montagut i Oix › Garrotxa | 1 |
| Forêt de Montagut i Oix (60) ⚠️ | Montagut i Oix › Garrotxa | 1 |
| Forêt de Argelaguer (7) ⚠️ | Argelaguer › Garrotxa | 1 |
| Parc (3) ⚠️ | Montagut i Oix › Garrotxa | 1 |
| Forêt de Albanyà (17) ⚠️ | Albanyà › Alt Empordà | 1 |
| Forêt de Sant Llorenç de la Muga (9) ⚠️ | Sant Llorenç de la Muga › Alt Empordà | 1 |
| Forêt de Sant Llorenç de la Muga (10) ⚠️ | Sant Llorenç de la Muga › Alt Empordà | 1 |
| Forêt de Sant Llorenç de la Muga (15) ⚠️ | Sant Llorenç de la Muga › Alt Empordà | 1 |
| Forêt de Sant Llorenç de la Muga (18) ⚠️ | Sant Llorenç de la Muga › Alt Empordà | 1 |
| Forêt de Sant Llorenç de la Muga (19) ⚠️ | Sant Llorenç de la Muga › Alt Empordà | 1 |
| Forêt de Maçanet de Cabrenys (21) ⚠️ | Maçanet de Cabrenys › Alt Empordà | 1 |
| Forêt de Albanyà (28) ⚠️ | Albanyà › Alt Empordà | 1 |
| Forêt de Espolla (9) ⚠️ | Espolla › Alt Empordà | 1 |
| Forêt de Espolla (12) ⚠️ | Espolla › Alt Empordà | 1 |
| Forêt de Rabós (4) ⚠️ | Rabós › Alt Empordà | 1 |
| Forêt de Rabós (6) ⚠️ | Rabós › Alt Empordà | 1 |
| Forêt de Rabós (9) ⚠️ | Rabós › Alt Empordà | 1 |
| Forêt de Espolla (13) ⚠️ | Espolla › Alt Empordà | 1 |
| Forêt de Camprodon (30) ⚠️ | Camprodon › Ripollès | 1 |
| Forêt de Molló (12) ⚠️ | Molló › Ripollès | 1 |
| Forêt de Molló (29) ⚠️ | Molló › Ripollès | 1 |
| Forêt de Molló (32) ⚠️ | Molló › Ripollès | 1 |
| Forêt de Molló (33) ⚠️ | Molló › Ripollès | 1 |
| Forêt de Molló (43) ⚠️ | Molló › Ripollès | 1 |
| Forêt de Molló (50) ⚠️ | Molló › Ripollès | 1 |
| Forêt de Setcases (85) ⚠️ | Setcases › Ripollès | 1 |
| Forêt de Setcases (86) ⚠️ | Setcases › Ripollès | 1 |
| Forêt de Setcases (87) ⚠️ | Setcases › Ripollès | 1 |
| Forêt de Setcases (96) ⚠️ | Setcases › Ripollès | 1 |
| Forêt de Setcases (97) ⚠️ | Setcases › Ripollès | 1 |
| Forêt de Molló (79) ⚠️ | Molló › Ripollès | 1 |
| Forêt de Molló (87) ⚠️ | Molló › Ripollès | 1 |
| Forêt de Camprodon (45) ⚠️ | Camprodon › Ripollès | 1 |
| Forêt de Setcases (101) ⚠️ | Setcases › Ripollès | 1 |
| Forêt de Setcases (103) ⚠️ | Setcases › Ripollès | 1 |
| Forêt de Toses (27) ⚠️ | Toses › Ripollès | 1 |
| Forêt de Toses (37) ⚠️ | Toses › Ripollès | 1 |
| Forêt de Toses (41) ⚠️ | Toses › Ripollès | 1 |
| Forêt de Toses (42) ⚠️ | Toses › Ripollès | 1 |
| Forêt de Toses (47) ⚠️ | Toses › Ripollès | 1 |
| Forêt de Planoles (12) ⚠️ | Planoles › Ripollès | 1 |
| Forêt de Planoles (15) ⚠️ | Planoles › Ripollès | 1 |
| Forêt de Ger (23) ⚠️ | Ger › Cerdanya (Gérone) | 1 |
| Forêt de Meranges (20) ⚠️ | Meranges › Cerdanya (Gérone) | 1 |
| Bois de Vilallonga de Ter (11) ⚠️ | Vilallonga de Ter › Ripollès | 1 |
| Forêt de Camprodon (49) ⚠️ | Camprodon › Ripollès | 1 |
| Forêt de Sant Joan de les Abadesses (11) ⚠️ | Sant Joan de les Abadesses › Ripollès | 1 |
| Forêt de Sant Joan de les Abadesses (12) ⚠️ | Sant Joan de les Abadesses › Ripollès | 1 |
| Forêt de Ripoll (75) ⚠️ | Ripoll › Ripollès | 1 |
| Forêt de Sant Joan de les Abadesses (30) ⚠️ | Sant Joan de les Abadesses › Ripollès | 1 |
| Forêt de Sant Joan de les Abadesses (31) ⚠️ | Sant Joan de les Abadesses › Ripollès | 1 |
| Forêt de la Vall de Bianya (26) ⚠️ | la Vall de Bianya › Garrotxa | 1 |
| Forêt de Camprodon (54) ⚠️ | Camprodon › Ripollès | 1 |
| Forêt de Camprodon (55) ⚠️ | Camprodon › Ripollès | 1 |
| Forêt de Ripoll (76) ⚠️ | Ripoll › Ripollès | 1 |
| Forêt de Ripoll (84) ⚠️ | Ripoll › Ripollès | 1 |
| Forêt de les Llosses (113) ⚠️ | les Llosses › Ripollès | 1 |
| Forêt de Montagut i Oix (80) ⚠️ | Montagut i Oix › Garrotxa | 1 |
| Parc de Santa Coloma de Farners (13) ⚠️ | Santa Coloma de Farners › la Selva (Gérone) | 1 |
| Forêt de Sant Hilari Sacalm (29) ⚠️ | Sant Hilari Sacalm › la Selva (Gérone) | 1 |
| Forêt de Arbúcies (20) ⚠️ | Arbúcies › la Selva (Gérone) | 1 |
| Forêt de Arbúcies (31) ⚠️ | Arbúcies › la Selva (Gérone) | 1 |
| Forêt de Palafrugell (130) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Forêt de Palafrugell (131) ⚠️ | Palafrugell › Baix Empordà | 1 |
| Forêt de Isòvol (13) ⚠️ | Isòvol › Cerdanya (Gérone) | 1 |
| Forêt de el Port de la Selva (30) ⚠️ | el Port de la Selva › Alt Empordà | 1 |
| Forêt de el Port de la Selva (32) ⚠️ | el Port de la Selva › Alt Empordà | 1 |
| Forêt de la Selva de Mar (6) ⚠️ | la Selva de Mar › Alt Empordà | 1 |
| Forêt de el Port de la Selva (34) ⚠️ | el Port de la Selva › Alt Empordà | 1 |
| Forêt de la Selva de Mar (9) ⚠️ | la Selva de Mar › Alt Empordà | 1 |
| Forêt de el Port de la Selva (35) ⚠️ | el Port de la Selva › Alt Empordà | 1 |
| Forêt de Cadaqués (23) ⚠️ | Cadaqués › Alt Empordà | 1 |
| Forêt de la Selva de Mar (10) ⚠️ | la Selva de Mar › Alt Empordà | 1 |
| Forêt de Pau ⚠️ | Pau › Alt Empordà | 1 |
| Forêt de Palau-saverdera (6) ⚠️ | Palau-saverdera › Alt Empordà | 1 |
| Forêt de Palau-saverdera (7) ⚠️ | Palau-saverdera › Alt Empordà | 1 |
| Forêt de Palau-saverdera (8) ⚠️ | Palau-saverdera › Alt Empordà | 1 |
| Forêt de Roses (31) ⚠️ | Roses › Alt Empordà | 1 |
| Forêt de Roses (32) ⚠️ | Roses › Alt Empordà | 1 |
| Forêt de Roses (41) ⚠️ | Roses › Alt Empordà | 1 |
| Forêt de Roses (42) ⚠️ | Roses › Alt Empordà | 1 |
| Forêt de Llançà (28) ⚠️ | Llançà › Alt Empordà | 1 |
| Forêt de Llançà (29) ⚠️ | Llançà › Alt Empordà | 1 |
| Forêt de Llançà (34) ⚠️ | Llançà › Alt Empordà | 1 |
| Forêt de Llançà (39) ⚠️ | Llançà › Alt Empordà | 1 |
| Forêt de Peralada (5) ⚠️ | Peralada › Alt Empordà | 1 |
| Forêt de Peralada (12) ⚠️ | Peralada › Alt Empordà | 1 |
| Forêt de Pont de Molins (4) ⚠️ | Pont de Molins › Alt Empordà | 1 |
| Forêt de Pont de Molins (8) ⚠️ | Pont de Molins › Alt Empordà | 1 |
| Forêt de Pont de Molins (10) ⚠️ | Pont de Molins › Alt Empordà | 1 |
| Forêt de Pont de Molins (11) ⚠️ | Pont de Molins › Alt Empordà | 1 |
| Forêt de Castelló d'Empúries (18) ⚠️ | Castelló d'Empúries › Alt Empordà | 1 |
| Forêt de Sant Pere Pescador (4) ⚠️ | Sant Pere Pescador › Alt Empordà | 1 |
| Forêt de Sant Pere Pescador (6) ⚠️ | Sant Pere Pescador › Alt Empordà | 1 |
| Forêt de Vila-sacra (3) ⚠️ | Vila-sacra › Alt Empordà | 1 |
| Forêt de Peralada (18) ⚠️ | Peralada › Alt Empordà | 1 |
| Forêt de Figueres (11) ⚠️ | Figueres › Alt Empordà | 1 |
| Forêt de Roses (43) ⚠️ | Roses › Alt Empordà | 1 |
| Forêt de Urús (16) ⚠️ | Urús › Cerdanya (Gérone) | 1 |
| Bois de Sant Gregori (13) ⚠️ | Sant Gregori › Gironès | 1 |
| Forêt de Bescanó (27) ⚠️ | Bescanó › Gironès | 1 |
| Forêt de la Cellera de Ter (39) ⚠️ | la Cellera de Ter › la Selva (Gérone) | 1 |
| Forêt de Sant Julià del Llor i Bonmatí (4) ⚠️ | Sant Julià del Llor i Bonmatí › la Selva (Gérone) | 1 |
| Bois de Amer (5) ⚠️ | Amer › la Selva (Gérone) | 1 |
| Bois de Amer (6) ⚠️ | Amer › la Selva (Gérone) | 1 |
| Bois de Peralada (3) ⚠️ | Peralada › Alt Empordà | 1 |
| Forêt de Gombrèn (73) ⚠️ | Gombrèn › Ripollès | 1 |
| Forêt de Gombrèn (74) ⚠️ | Gombrèn › Ripollès | 1 |
| Forêt de Gombrèn (75) ⚠️ | Gombrèn › Ripollès | 1 |
| Forêt de Toses (57) ⚠️ | Toses › Ripollès | 1 |
| Forêt de Santa Pau (20) ⚠️ | Santa Pau › Garrotxa | 1 |
| Forêt de Santa Pau (22) ⚠️ | Santa Pau › Garrotxa | 1 |
| Forêt de Tossa de Mar (36) ⚠️ | Tossa de Mar › la Selva (Gérone) | 1 |
| Forêt de Siurana (9) ⚠️ | Siurana › Alt Empordà | 1 |
| Forêt de Siurana (10) ⚠️ | Siurana › Alt Empordà | 1 |
| Forêt de Gualta (2) ⚠️ | Gualta › Baix Empordà | 1 |
| Forêt de Gualta (3) ⚠️ | Gualta › Baix Empordà | 1 |
| Forêt de Torroella de Montgrí (92) ⚠️ | Torroella de Montgrí › Baix Empordà | 1 |
| Forêt de Torroella de Montgrí (94) ⚠️ | Torroella de Montgrí › Baix Empordà | 1 |
| Forêt de Torroella de Montgrí (95) ⚠️ | Torroella de Montgrí › Baix Empordà | 1 |
| Forêt de Gualta (5) ⚠️ | Gualta › Baix Empordà | 1 |
| Forêt de Sant Julià de Ramis (16) ⚠️ | Sant Julià de Ramis › Gironès | 1 |
| Forêt de Bordils ⚠️ | Celrà › Gironès | 1 |
| Forêt de Sant Julià de Ramis (19) ⚠️ | Sant Julià de Ramis › Gironès | 1 |
| Forêt de Cervià de Ter (42) ⚠️ | Cervià de Ter › Gironès | 1 |
| Forêt de la Vall d'en Bas (23) ⚠️ | la Vall d'en Bas › Garrotxa | 1 |
| Forêt de Sant Hilari Sacalm (36) ⚠️ | Sant Hilari Sacalm › la Selva (Gérone) | 1 |
| Forêt de Susqueda (9) ⚠️ | Susqueda › la Selva (Gérone) | 1 |
| Forêt de Sant Hilari Sacalm (41) ⚠️ | Sant Hilari Sacalm › la Selva (Gérone) | 1 |
| Forêt de Sant Joan de les Abadesses (40) ⚠️ | Sant Joan de les Abadesses › Ripollès | 1 |
| Forêt de Sant Joan de les Abadesses (41) ⚠️ | Sant Joan de les Abadesses › Ripollès | 1 |
| Forêt de Sant Jordi Desvalls (5) ⚠️ | Cervià de Ter › Gironès | 1 |
| Forêt de Sant Jordi Desvalls (6) ⚠️ | Sant Jordi Desvalls › Gironès | 1 |
| Forêt de Sant Jordi Desvalls (7) ⚠️ | Sant Jordi Desvalls › Gironès | 1 |
| Forêt de Viladasens (8) ⚠️ | Viladasens › Gironès | 1 |
| Forêt de Sant Jordi Desvalls (13) ⚠️ | Sant Jordi Desvalls › Gironès | 1 |
| Forêt de Hostalric (7) ⚠️ | Hostalric › la Selva (Gérone) | 1 |
| Forêt de Massanes (25) ⚠️ | Massanes › la Selva (Gérone) | 1 |
| Forêt de Hostalric (9) ⚠️ | Hostalric › la Selva (Gérone) | 1 |
| Forêt de Sant Feliu de Buixalleu (25) ⚠️ | Sant Feliu de Buixalleu › la Selva (Gérone) | 1 |
| Forêt de Sant Feliu de Buixalleu (29) ⚠️ | Sant Feliu de Buixalleu › la Selva (Gérone) | 1 |
| Forêt de Hostalric (10) ⚠️ | Sant Feliu de Buixalleu › la Selva (Gérone) | 1 |
| Forêt de Riells i Viabrea (20) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 1 |
| Forêt de Riells i Viabrea (23) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 1 |
| Forêt de Riells i Viabrea (25) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 1 |
| Forêt de Riells i Viabrea (27) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 1 |
| Forêt de Riells i Viabrea (32) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 1 |
| Forêt de Riells i Viabrea (38) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 1 |
| Forêt de Riells i Viabrea (41) ⚠️ | Riells i Viabrea › la Selva (Gérone) | 1 |
| Forêt de Camprodon (58) ⚠️ | Camprodon › Ripollès | 1 |
| Forêt de Camprodon (61) ⚠️ | Camprodon › Ripollès | 1 |
| Forêt de Sant Joan de les Abadesses (44) ⚠️ | Sant Joan de les Abadesses › Ripollès | 1 |
| Forêt de la Vall d'en Bas (32) ⚠️ | la Vall d'en Bas › Garrotxa | 1 |
| Forêt de la Vall d'en Bas (39) ⚠️ | la Vall d'en Bas › Garrotxa | 1 |
| Forêt de la Vall d'en Bas (43) ⚠️ | la Vall d'en Bas › Garrotxa | 1 |
| Forêt de la Vall d'en Bas (46) ⚠️ | la Vall d'en Bas › Garrotxa | 1 |
| Forêt de la Vall d'en Bas (50) ⚠️ | la Vall d'en Bas › Garrotxa | 1 |
| Forêt de la Vall d'en Bas (55) ⚠️ | la Vall d'en Bas › Garrotxa | 1 |
| Forêt de la Vall d'en Bas (57) ⚠️ | la Vall d'en Bas › Garrotxa | 1 |
| Forêt de la Vall d'en Bas (58) ⚠️ | la Vall d'en Bas › Garrotxa | 1 |
| Forêt de la Vall d'en Bas (66) ⚠️ | la Vall d'en Bas › Garrotxa | 1 |
| Forêt de la Vall d'en Bas (67) ⚠️ | la Vall d'en Bas › Garrotxa | 1 |
| Forêt de Viladrau (53) ⚠️ | Viladrau › Osona (Gérone) | 1 |
| Forêt de Riudaura ⚠️ | Riudaura › Garrotxa | 1 |
| Forêt de Olot (25) ⚠️ | Olot › Garrotxa | 1 |
| Forêt de Riudaura (5) ⚠️ | Riudaura › Garrotxa | 1 |
| Forêt de Sant Joan les Fonts (17) ⚠️ | Sant Joan les Fonts › Garrotxa | 1 |
| Forêt de Sant Joan les Fonts (18) ⚠️ | Sant Joan les Fonts › Garrotxa | 1 |
| Forêt de Sant Joan les Fonts (19) ⚠️ | Sant Joan les Fonts › Garrotxa | 1 |
| Forêt de Sant Joan les Fonts (20) ⚠️ | Sant Joan les Fonts › Garrotxa | 1 |
| Forêt de Sant Joan les Fonts (25) ⚠️ | Castellfollit de la Roca › Garrotxa | 1 |
| Forêt de Tossa de Mar (39) ⚠️ | Tossa de Mar › la Selva (Gérone) | 1 |
| Forêt de Tossa de Mar (43) ⚠️ | Tossa de Mar › la Selva (Gérone) | 1 |
| Forêt de Sant Joan de les Abadesses (45) ⚠️ | Sant Joan de les Abadesses › Ripollès | 1 |
| Forêt de Camprodon (67) ⚠️ | Camprodon › Ripollès | 1 |
| Forêt de Camprodon (68) ⚠️ | Camprodon › Ripollès | 1 |
| Forêt de Viladrau (65) ⚠️ | Viladrau › Osona (Gérone) | 1 |
| Forêt de Vilallonga de Ter (22) ⚠️ | Vilallonga de Ter › Ripollès | 1 |
| Forêt de Vilallonga de Ter (24) ⚠️ | Vilallonga de Ter › Ripollès | 1 |
| Forêt de Vilallonga de Ter (28) ⚠️ | Vilallonga de Ter › Ripollès | 1 |
| Forêt de Llanars (22) ⚠️ | Llanars › Ripollès | 1 |
| Forêt de Vilallonga de Ter (31) ⚠️ | Vilallonga de Ter › Ripollès | 1 |
| Forêt de Setcases (110) ⚠️ | Setcases › Ripollès | 1 |
| Forêt de Queralbs (42) ⚠️ | Queralbs › Ripollès | 1 |
| Forêt de Alp (107) ⚠️ | Alp › Cerdanya (Gérone) | 1 |
| Forêt de Castell d'Aro, Platja d'Aro i s'Agaró (35) ⚠️ | Castell d'Aro, Platja d'Aro i s'Agaró › Baix Empordà | 1 |
| Forêt de Esponellà (5) ⚠️ | Esponellà › Pla de l'Estany | 1 |
| Forêt de Vilademuls (30) ⚠️ | Vilademuls › Pla de l'Estany | 1 |
| Forêt de Vilademuls (32) ⚠️ | Vilademuls › Pla de l'Estany | 1 |
| Forêt de Sant Mori (3) ⚠️ | Sant Mori › Alt Empordà | 1 |
| Forêt de Sant Miquel de Fluvià (4) ⚠️ | Sant Miquel de Fluvià › Alt Empordà | 1 |
| Forêt de Torroella de Fluvià (9) ⚠️ | Torroella de Fluvià › Alt Empordà | 1 |
| Forêt de Sant Miquel de Fluvià (6) ⚠️ | Sant Miquel de Fluvià › Alt Empordà | 1 |
| Forêt de Ventalló (14) ⚠️ | Ventalló › Alt Empordà | 1 |
| Forêt de Argelaguer (11) ⚠️ | Argelaguer › Garrotxa | 1 |
| Forêt de Besalú (17) ⚠️ | Besalú › Garrotxa | 1 |
| Forêt de Sant Jaume de Llierca (4) ⚠️ | Sant Jaume de Llierca › Garrotxa | 1 |
| Forêt de Sant Jaume de Llierca (5) ⚠️ | Sant Jaume de Llierca › Garrotxa | 1 |
| Forêt de Montagut i Oix (86) ⚠️ | Montagut i Oix › Garrotxa | 1 |
| Forêt de Torroella de Fluvià (11) ⚠️ | Torroella de Fluvià › Alt Empordà | 1 |
| Forêt de Torroella de Fluvià (13) ⚠️ | Torroella de Fluvià › Alt Empordà | 1 |
| Forêt de Ventalló (16) ⚠️ | Ventalló › Alt Empordà | 1 |
| Forêt de Torroella de Fluvià (14) ⚠️ | Torroella de Fluvià › Alt Empordà | 1 |
| Forêt de Sant Miquel de Fluvià (8) ⚠️ | Sant Miquel de Fluvià › Alt Empordà | 1 |
| Forêt de l'Armentera (4) ⚠️ | l'Armentera › Alt Empordà | 1 |
| Forêt de Sant Pere Pescador (13) ⚠️ | Sant Pere Pescador › Alt Empordà | 1 |
| Forêt de Ventalló (25) ⚠️ | Ventalló › Alt Empordà | 1 |
| Forêt de Ventalló (27) ⚠️ | Ventalló › Alt Empordà | 1 |
| Forêt de Ventalló (29) ⚠️ | Ventalló › Alt Empordà | 1 |
| Forêt de Ripoll (93) ⚠️ | Ripoll › Ripollès | 1 |
| Forêt de Ripoll (96) ⚠️ | Ripoll › Ripollès | 1 |
| Forêt de Ripoll (97) ⚠️ | Ripoll › Ripollès | 1 |
| Forêt de Ripoll (99) ⚠️ | Ripoll › Ripollès | 1 |
| Forêt de Ripoll (100) ⚠️ | Ripoll › Ripollès | 1 |
| Forêt de Ripoll (101) ⚠️ | Ripoll › Ripollès | 1 |
| Forêt de Puigcerdà (125) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Puigcerdà (129) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |
| Forêt de Puigcerdà (130) ⚠️ | Puigcerdà › Cerdanya (Gérone) | 1 |

3 135 parc(s) plus petits qu'une cellule ne sont pas listés : la carte les dessine, mais ils n'offrent aucune cellule.

⚠️ 5908 parc(s) hors de la fenêtre 10–125 cellules (5711 trop petit(s), 197 trop grand(s)) : affichés sur la carte, mais ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| military | 792 |
| airport | 92 |
| prison | 7 |
| **Total déclaré** | **891** |
| dont dans une zone de ce territoire | 889 |

Le jeu de données couvre plus large que le territoire — il est produit à une échelle supérieure. Seules les cellules tombant dans une zone d'ici pèsent sur un pourcentage.

### Zones concernées

| Zone | Cellules exclues |
|---|---:|
| Sant Climent Sescebes | 624 |
| Espolla | 156 |
| Vilobí d'Onyar | 48 |
| Das | 14 |
| Aiguaviva | 13 |
| Castelló d'Empúries | 8 |
| Figueres | 7 |
| Roses | 6 |
| Fontanals de Cerdanya | 5 |
| Viladamat | 4 |
| Cantallops | 4 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
