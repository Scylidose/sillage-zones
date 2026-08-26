# Province de Barcelone

Pack `es-barcelona` · version 1.0.0 · grille 200 m · Espagne › Catalogne

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 346 352 |
| dont restreintes (aéroport, militaire, prison) | 448 |
| dont sans chemin (aucune voie à moins de 60 m) | 10 498 |
| dont en forêt, sans chemin non plus | 22 855 |
| dont traversées par un cours d'eau, sans chemin non plus | 3 207 |
| Cellules retirées par le masque d'eau | 1 196 |
| Villes | 311 |
| Arrondissements et quartiers | 0 |
| Îles | 14 |
| Parcs | 19 021 |

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
| Alt Penedès | 26 302 | somme de 27 villes |
| Anoia | 38 818 | somme de 33 villes |
| Bages | 49 072 | somme de 30 villes |
| Baix Llobregat | 21 530 | somme de 30 villes |
| Barcelonès | 6 509 | somme de 5 villes |
| Berguedà | 51 146 | somme de 30 villes |
| Garraf | 8 219 | somme de 6 villes |
| Lluçanès | 10 238 | somme de 8 villes |
| Maresme | 17 819 | somme de 30 villes |
| Moianès | 15 178 | somme de 10 villes |
| Osona (Barcelone) | 41 513 | somme de 40 villes |
| Vallès Occidental | 25 976 | somme de 23 villes |
| Vallès Oriental | 32 595 | somme de 38 villes |
| la Selva (Barcelone) | 1 443 | somme de 1 villes |

Une île *composite* n'a pas de cellules à elle : sa progression est la somme de ses villes, et ses cellules ne lui sont jamais rattachées directement — elles compteraient deux fois.

## Villes (311)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Sans chemin | Parcs |
|---|---:|---:|---:|---:|---:|---:|---:|
| Sant Mateu de Bages | 4 615 | 4 | 4 611 | 0 | **4 611** | 179 (4 %) | 170 |
| Barcelona | 4 515 | 10 | 4 505 | 0 | **4 505** | 3 (0 %) | 758 |
| Tordera | 3 803 | 10 | 3 793 | 0 | **3 793** | 61 (2 %) | 139 |
| Navàs | 3 648 | 5 | 3 643 | 0 | **3 643** | 80 (2 %) | 164 |
| Montmajor | 3 445 | 1 | 3 444 | 0 | **3 444** | 148 (4 %) | 135 |
| Moià | 3 423 | 1 | 3 422 | 7 | **3 415** | 161 (5 %) | 87 |
| Terrassa | 3 144 | 18 | 3 126 | 0 | **3 126** | 22 (1 %) | 200 |
| Oristà | 3 104 | 0 | 3 104 | 0 | **3 104** | 153 (5 %) | 175 |
| Saldes | 3 056 | 0 | 3 056 | 0 | **3 056** | 272 (9 %) | 137 |
| Viver i Serrateix | 3 021 | 1 | 3 020 | 0 | **3 020** | 104 (3 %) | 124 |
| Cardona | 2 999 | 5 | 2 994 | 0 | **2 994** | 149 (5 %) | 124 |
| Santa Maria d'Oló | 2 989 | 1 | 2 988 | 0 | **2 988** | 50 (2 %) | 92 |
| Sallent | 2 949 | 15 | 2 934 | 0 | **2 934** | 74 (3 %) | 149 |
| Sant Celoni | 2 935 | 4 | 2 931 | 0 | **2 931** | 2 (0 %) | 123 |
| Avinyó | 2 860 | 1 | 2 859 | 0 | **2 859** | 44 (2 %) | 124 |
| Guardiola de Berguedà | 2 821 | 7 | 2 814 | 0 | **2 814** | 168 (6 %) | 145 |
| l'Esquirol | 2 835 | 25 | 2 810 | 0 | **2 810** | 128 (5 %) | 125 |
| Castellfollit del Boix | 2 659 | 0 | 2 659 | 0 | **2 659** | 124 (5 %) | 44 |
| Piera | 2 549 | 1 | 2 548 | 0 | **2 548** | 74 (3 %) | 106 |
| Vilanova de Sau | 2 663 | 163 | 2 500 | 0 | **2 500** | 10 (0 %) | 66 |
| Sant Pere de Torelló | 2 501 | 6 | 2 495 | 0 | **2 495** | 46 (2 %) | 26 |
| Subirats | 2 482 | 0 | 2 482 | 0 | **2 482** | 42 (2 %) | 100 |
| Lluçà | 2 422 | 1 | 2 421 | 0 | **2 421** | 79 (3 %) | 91 |
| la Pobla de Lillet | 2 355 | 7 | 2 348 | 0 | **2 348** | 23 (1 %) | 72 |
| Fonollosa | 2 341 | 0 | 2 341 | 0 | **2 341** | 87 (4 %) | 180 |
| Òdena | 2 341 | 0 | 2 341 | 7 | **2 334** | 124 (5 %) | 140 |
| la Llacuna | 2 336 | 0 | 2 336 | 0 | **2 336** | 115 (5 %) | 28 |
| Santa Maria de Merlès | 2 327 | 2 | 2 325 | 0 | **2 325** | 59 (3 %) | 139 |
| Gurb | 2 317 | 2 | 2 315 | 0 | **2 315** | 137 (6 %) | 127 |
| Begues | 2 230 | 0 | 2 230 | 0 | **2 230** | 184 (8 %) | 86 |
| Rupit i Pruit | 2 183 | 0 | 2 183 | 0 | **2 183** | 49 (2 %) | 41 |
| Castellar de n'Hug | 2 149 | 0 | 2 149 | 0 | **2 149** | 212 (10 %) | 55 |
| Mura | 2 147 | 0 | 2 147 | 0 | **2 147** | 2 (0 %) | 60 |
| Mediona | 2 146 | 0 | 2 146 | 0 | **2 146** | 62 (3 %) | 95 |
| Sant Cugat del Vallès | 2 144 | 5 | 2 139 | 0 | **2 139** | 2 (0 %) | 369 |
| el Bruc | 2 124 | 0 | 2 124 | 4 | **2 120** | 42 (2 %) | 53 |
| Argençola | 2 117 | 0 | 2 117 | 0 | **2 117** | 145 (7 %) | 61 |
| Puig-reig | 2 086 | 11 | 2 075 | 0 | **2 075** | 39 (2 %) | 102 |
| Castellet i la Gornal | 2 087 | 30 | 2 057 | 0 | **2 057** | 70 (3 %) | 116 |
| Rajadell | 2 044 | 0 | 2 044 | 0 | **2 044** | 58 (3 %) | 74 |
| Sagàs | 2 044 | 0 | 2 044 | 0 | **2 044** | 146 (7 %) | 58 |
| Castellar del Vallès | 2 027 | 1 | 2 026 | 0 | **2 026** | 11 (1 %) | 34 |
| Cercs | 2 145 | 128 | 2 017 | 0 | **2 017** | 45 (2 %) | 72 |
| Borredà | 1 979 | 5 | 1 974 | 0 | **1 974** | 46 (2 %) | 129 |
| Bagà | 1 965 | 1 | 1 964 | 0 | **1 964** | 169 (9 %) | 93 |
| Sitges | 1 959 | 4 | 1 955 | 0 | **1 955** | 276 (14 %) | 132 |
| Tagamanent | 1 944 | 0 | 1 944 | 0 | **1 944** | 2 (0 %) | 38 |
| Aguilar de Segarra | 1 935 | 0 | 1 935 | 0 | **1 935** | 123 (6 %) | 55 |
| Manresa | 1 864 | 8 | 1 856 | 0 | **1 856** | 14 (1 %) | 249 |
| el Brull | 1 855 | 3 | 1 852 | 0 | **1 852** | 38 (2 %) | 43 |
| Sant Llorenç Savall | 1 847 | 0 | 1 847 | 0 | **1 847** | 2 (0 %) | 33 |
| Muntanyola | 1 837 | 1 | 1 836 | 0 | **1 836** | 78 (4 %) | 36 |
| Dosrius | 1 824 | 0 | 1 824 | 0 | **1 824** | 5 (0 %) | 54 |
| Vacarisses | 1 821 | 0 | 1 821 | 0 | **1 821** | 9 (0 %) | 74 |
| Sant Pere de Ribes | 1 811 | 0 | 1 811 | 0 | **1 811** | 38 (2 %) | 130 |
| Fogars de Montclús | 1 791 | 4 | 1 787 | 0 | **1 787** | 14 (1 %) | 28 |
| Gaià | 1 781 | 3 | 1 778 | 0 | **1 778** | 23 (1 %) | 74 |
| Veciana | 1 740 | 0 | 1 740 | 0 | **1 740** | 228 (13 %) | 21 |
| Sant Martí de Tous | 1 743 | 5 | 1 738 | 0 | **1 738** | 72 (4 %) | 51 |
| Rubió | 1 737 | 0 | 1 737 | 0 | **1 737** | 57 (3 %) | 9 |
| Olivella | 1 727 | 0 | 1 727 | 0 | **1 727** | 125 (7 %) | 133 |
| la Quar | 1 726 | 2 | 1 724 | 0 | **1 724** | 10 (1 %) | 53 |
| Sabadell | 1 688 | 1 | 1 687 | 27 | **1 660** | 10 (1 %) | 290 |
| Caldes de Montbui | 1 687 | 3 | 1 684 | 0 | **1 684** | 20 (1 %) | 46 |
| Gisclareny | 1 671 | 0 | 1 671 | 0 | **1 671** | 118 (7 %) | 74 |
| Sant Salvador de Guardiola | 1 663 | 0 | 1 663 | 0 | **1 663** | 14 (1 %) | 131 |
| Calonge de Segarra | 1 661 | 0 | 1 661 | 0 | **1 661** | 214 (13 %) | 19 |
| Font-rubí | 1 655 | 0 | 1 655 | 0 | **1 655** | 45 (3 %) | 36 |
| Balsareny | 1 656 | 8 | 1 648 | 0 | **1 648** | 12 (1 %) | 103 |
| Torrelles de Foix | 1 644 | 0 | 1 644 | 0 | **1 644** | 32 (2 %) | 35 |
| la Roca del Vallès | 1 642 | 12 | 1 630 | 9 | **1 621** | 23 (1 %) | 88 |
| Olvan | 1 613 | 5 | 1 608 | 0 | **1 608** | 25 (2 %) | 46 |
| l'Espunyola | 1 594 | 0 | 1 594 | 0 | **1 594** | 66 (4 %) | 79 |
| Sant Bartomeu del Grau | 1 572 | 2 | 1 570 | 0 | **1 570** | 122 (8 %) | 19 |
| Sant Martí Sarroca | 1 564 | 0 | 1 564 | 0 | **1 564** | 59 (4 %) | 43 |
| Capolat | 1 562 | 0 | 1 562 | 0 | **1 562** | 26 (2 %) | 49 |
| Sant Pere de Vilamajor | 1 535 | 1 | 1 534 | 0 | **1 534** | 7 (0 %) | 106 |
| Castellcir | 1 529 | 1 | 1 528 | 0 | **1 528** | 59 (4 %) | 13 |
| Vilanova i la Geltrú | 1 504 | 1 | 1 503 | 0 | **1 503** | 12 (1 %) | 99 |
| els Hostalets de Pierola | 1 496 | 1 | 1 495 | 0 | **1 495** | 59 (4 %) | 45 |
| Castellar del Riu | 1 490 | 0 | 1 490 | 0 | **1 490** | 7 (0 %) | 76 |
| Calders | 1 489 | 9 | 1 480 | 0 | **1 480** | 15 (1 %) | 89 |
| els Prats de Rei | 1 463 | 0 | 1 463 | 0 | **1 463** | 248 (17 %) | 31 |
| Fogars de la Selva | 1 444 | 1 | 1 443 | 0 | **1 443** | 24 (2 %) | 50 |
| Tavertet | 1 459 | 16 | 1 443 | 0 | **1 443** | 11 (1 %) | 83 |
| Rubí | 1 441 | 5 | 1 436 | 0 | **1 436** | 13 (1 %) | 169 |
| el Prat de Llobregat | 1 496 | 63 | 1 433 | 350 | **1 083** | 44 (4 %) | 359 |
| Sora | 1 421 | 0 | 1 421 | 0 | **1 421** | 59 (4 %) | 27 |
| Castellterçol | 1 420 | 0 | 1 420 | 0 | **1 420** | 13 (1 %) | 98 |
| Pujalt | 1 411 | 0 | 1 411 | 0 | **1 411** | 229 (16 %) | 12 |
| Sant Sadurní d'Osormort | 1 392 | 0 | 1 392 | 0 | **1 392** | 18 (1 %) | 50 |
| Bellprat | 1 390 | 0 | 1 390 | 0 | **1 390** | 184 (13 %) | 10 |
| Vic | 1 390 | 0 | 1 390 | 0 | **1 390** | 50 (4 %) | 140 |
| Jorba | 1 387 | 0 | 1 387 | 0 | **1 387** | 110 (8 %) | 65 |
| Seva | 1 375 | 3 | 1 372 | 0 | **1 372** | 43 (3 %) | 42 |
| Olesa de Bonesvalls | 1 371 | 0 | 1 371 | 0 | **1 371** | 19 (1 %) | 52 |
| Gavà | 1 377 | 7 | 1 370 | 0 | **1 370** | 30 (2 %) | 108 |
| Cerdanyola del Vallès | 1 368 | 0 | 1 368 | 0 | **1 368** | 7 (1 %) | 195 |
| Fígols | 1 361 | 0 | 1 361 | 0 | **1 361** | 49 (4 %) | 47 |
| Castellbisbal | 1 383 | 24 | 1 359 | 0 | **1 359** | 26 (2 %) | 72 |
| Castellnou de Bages | 1 337 | 0 | 1 337 | 0 | **1 337** | 9 (1 %) | 94 |
| Olèrdola | 1 336 | 0 | 1 336 | 0 | **1 336** | 17 (1 %) | 71 |
| les Franqueses del Vallès | 1 334 | 3 | 1 331 | 0 | **1 331** | 40 (3 %) | 116 |
| Casserres | 1 331 | 1 | 1 330 | 0 | **1 330** | 38 (3 %) | 43 |
| Olost | 1 314 | 3 | 1 311 | 0 | **1 311** | 193 (15 %) | 24 |
| Bigues i Riells del Fai | 1 306 | 0 | 1 306 | 0 | **1 306** | 5 (0 %) | 56 |
| Talamanca | 1 310 | 4 | 1 306 | 0 | **1 306** | 3 (0 %) | 47 |
| Avinyonet del Penedès | 1 296 | 0 | 1 296 | 4 | **1 292** | 46 (4 %) | 71 |
| Cànoves i Samalús | 1 290 | 5 | 1 285 | 0 | **1 285** | 8 (1 %) | 66 |
| Castellví de la Marca | 1 271 | 0 | 1 271 | 0 | **1 271** | 29 (2 %) | 60 |
| Vallcebre | 1 269 | 1 | 1 268 | 0 | **1 268** | 40 (3 %) | 78 |
| Castellbell i el Vilar | 1 283 | 16 | 1 267 | 0 | **1 267** | 5 (0 %) | 79 |
| Sentmenat | 1 262 | 0 | 1 262 | 0 | **1 262** | 25 (2 %) | 39 |
| Santa Margarida de Montbui | 1 239 | 1 | 1 238 | 0 | **1 238** | 41 (3 %) | 80 |
| Llinars del Vallès | 1 237 | 0 | 1 237 | 0 | **1 237** | 14 (1 %) | 133 |
| el Pont de Vilomara i Rocafort | 1 238 | 6 | 1 232 | 0 | **1 232** | 1 (0 %) | 66 |
| Avià | 1 234 | 7 | 1 227 | 0 | **1 227** | 62 (5 %) | 70 |
| Orís | 1 230 | 14 | 1 216 | 0 | **1 216** | 69 (6 %) | 31 |
| Montseny | 1 214 | 0 | 1 214 | 0 | **1 214** | 19 (2 %) | 24 |
| Esparreguera | 1 214 | 9 | 1 205 | 0 | **1 205** | 21 (2 %) | 74 |
| Gelida | 1 189 | 0 | 1 189 | 0 | **1 189** | 40 (3 %) | 40 |
| Taradell | 1 194 | 6 | 1 188 | 0 | **1 188** | 52 (4 %) | 60 |
| Castellfollit de Riubregós | 1 180 | 0 | 1 180 | 0 | **1 180** | 74 (6 %) | 10 |
| Sant Martí de Centelles | 1 160 | 0 | 1 160 | 0 | **1 160** | 37 (3 %) | 80 |
| Sant Quirze Safaja | 1 150 | 0 | 1 150 | 0 | **1 150** | 10 (1 %) | 57 |
| Castellolí | 1 137 | 0 | 1 137 | 0 | **1 137** | 5 (0 %) | 45 |
| la Nou de Berguedà | 1 135 | 1 | 1 134 | 0 | **1 134** | 33 (3 %) | 19 |
| Argentona | 1 133 | 0 | 1 133 | 0 | **1 133** | 3 (0 %) | 123 |
| Matadepera | 1 135 | 4 | 1 131 | 0 | **1 131** |  | 241 |
| Santa Maria de Miralles | 1 131 | 0 | 1 131 | 0 | **1 131** | 77 (7 %) | 5 |
| Pontons | 1 129 | 0 | 1 129 | 0 | **1 129** | 48 (4 %) | 19 |
| Santa Maria de Besora | 1 132 | 3 | 1 129 | 0 | **1 129** | 16 (1 %) | 21 |
| Castell de l'Areny | 1 128 | 0 | 1 128 | 0 | **1 128** | 14 (1 %) | 30 |
| Cervelló | 1 078 | 0 | 1 078 | 0 | **1 078** | 9 (1 %) | 28 |
| Granera | 1 065 | 0 | 1 065 | 0 | **1 065** |  | 38 |
| Súria | 1 061 | 2 | 1 059 | 0 | **1 059** | 6 (1 %) | 62 |
| Vallirana | 1 057 | 1 | 1 056 | 0 | **1 056** | 4 (0 %) | 41 |
| Torrelavit | 1 054 | 0 | 1 054 | 0 | **1 054** | 27 (3 %) | 85 |
| Sant Feliu Sasserra | 1 040 | 1 | 1 039 | 0 | **1 039** | 13 (1 %) | 42 |
| Gualba | 1 038 | 0 | 1 038 | 0 | **1 038** | 2 (0 %) | 33 |
| Montcada i Reixac | 1 047 | 11 | 1 036 | 0 | **1 036** | 4 (0 %) | 100 |
| Berga | 1 023 | 3 | 1 020 | 0 | **1 020** | 9 (1 %) | 77 |
| Montclar | 1 019 | 0 | 1 019 | 0 | **1 019** | 66 (6 %) | 38 |
| Lliçà d'Amunt | 1 002 | 0 | 1 002 | 0 | **1 002** | 19 (2 %) | 72 |
| Mataró | 999 | 1 | 998 | 0 | **998** | 2 (0 %) | 164 |
| Copons | 996 | 0 | 996 | 0 | **996** | 58 (6 %) | 12 |
| Vallgorguina | 995 | 0 | 995 | 0 | **995** |  | 25 |
| Monistrol de Calders | 993 | 3 | 990 | 0 | **990** | 2 (0 %) | 48 |
| les Masies de Voltregà | 1 006 | 20 | 986 | 0 | **986** | 54 (5 %) | 30 |
| Sant Fruitós de Bages | 986 | 4 | 982 | 0 | **982** | 36 (4 %) | 134 |
| Sant Pere Sallavinera | 982 | 0 | 982 | 0 | **982** | 69 (7 %) | 65 |
| Sant Jaume de Frontanyà | 974 | 0 | 974 | 0 | **974** | 5 (1 %) | 26 |
| Vilada | 1 018 | 44 | 974 | 0 | **974** | 36 (4 %) | 18 |
| Sant Boi de Llobregat | 950 | 5 | 945 | 13 | **932** |  | 125 |
| Arenys de Munt | 933 | 0 | 933 | 0 | **933** | 17 (2 %) | 34 |
| Badalona | 935 | 2 | 933 | 0 | **933** | 3 (0 %) | 63 |
| Sant Boi de Lluçanès | 895 | 0 | 895 | 0 | **895** | 70 (8 %) | 7 |
| Viladecavalls | 894 | 0 | 894 | 0 | **894** |  | 51 |
| Abrera | 895 | 8 | 887 | 0 | **887** | 31 (3 %) | 55 |
| Vilafranca del Penedès | 887 | 0 | 887 | 0 | **887** | 21 (2 %) | 58 |
| Viladecans | 899 | 16 | 883 | 3 | **880** | 11 (1 %) | 177 |
| Perafita | 884 | 2 | 882 | 0 | **882** | 83 (9 %) | 5 |
| Sant Llorenç d'Hortons | 861 | 0 | 861 | 0 | **861** | 69 (8 %) | 33 |
| la Garriga | 860 | 1 | 859 | 0 | **859** | 10 (1 %) | 81 |
| Tavèrnoles | 855 | 7 | 848 | 0 | **848** | 13 (2 %) | 12 |
| Sant Sadurní d'Anoia | 840 | 3 | 837 | 0 | **837** | 44 (5 %) | 53 |
| la Pobla de Claramunt | 832 | 3 | 829 | 0 | **829** | 3 (0 %) | 46 |
| Sant Esteve Sesrovires | 826 | 1 | 825 | 15 | **810** | 38 (5 %) | 37 |
| Corbera de Llobregat | 813 | 0 | 813 | 0 | **813** |  | 42 |
| Collbató | 808 | 4 | 804 | 0 | **804** | 6 (1 %) | 33 |
| Artés | 803 | 1 | 802 | 0 | **802** | 11 (1 %) | 40 |
| Sant Iscle de Vallalta | 792 | 0 | 792 | 0 | **792** | 4 (1 %) | 9 |
| Rellinars | 790 | 0 | 790 | 0 | **790** | 1 (0 %) | 10 |
| Masquefa | 780 | 0 | 780 | 0 | **780** | 40 (5 %) | 24 |
| Balenyà | 780 | 1 | 779 | 0 | **779** | 17 (2 %) | 45 |
| Sant Vicenç de Castellet | 780 | 5 | 775 | 0 | **775** | 2 (0 %) | 69 |
| Santa Margarida i els Monjos | 770 | 0 | 770 | 0 | **770** | 25 (3 %) | 63 |
| Santa Maria de Palautordera | 768 | 0 | 768 | 0 | **768** | 9 (1 %) | 65 |
| Cabrera d'Anoia | 772 | 7 | 765 | 0 | **765** | 4 (1 %) | 53 |
| Castellgalí | 777 | 13 | 764 | 0 | **764** | 4 (1 %) | 80 |
| Manlleu | 782 | 20 | 762 | 0 | **762** | 36 (5 %) | 56 |
| Santpedor | 759 | 1 | 758 | 0 | **758** | 20 (3 %) | 106 |
| Sant Joan de Vilatorrada | 744 | 2 | 742 | 5 | **737** | 30 (4 %) | 116 |
| Tona | 741 | 0 | 741 | 0 | **741** | 29 (4 %) | 70 |
| Olesa de Montserrat | 745 | 10 | 735 | 0 | **735** | 6 (1 %) | 68 |
| Palafolls | 735 | 2 | 733 | 0 | **733** | 5 (1 %) | 56 |
| Gallifa | 729 | 0 | 729 | 0 | **729** |  | 8 |
| Sant Julià de Vilatorta | 729 | 0 | 729 | 0 | **729** | 28 (4 %) | 27 |
| Castellví de Rosanes | 727 | 0 | 727 | 0 | **727** | 7 (1 %) | 13 |
| Molins de Rei | 707 | 10 | 697 | 0 | **697** |  | 47 |
| Sant Cebrià de Vallalta | 696 | 0 | 696 | 0 | **696** | 9 (1 %) | 23 |
| Santa Perpètua de Mogoda | 695 | 0 | 695 | 0 | **695** | 21 (3 %) | 74 |
| Vilanova del Vallès | 693 | 0 | 693 | 0 | **693** | 9 (1 %) | 50 |
| Centelles | 692 | 0 | 692 | 0 | **692** | 13 (2 %) | 39 |
| Collsuspina | 679 | 0 | 679 | 0 | **679** | 31 (5 %) | 14 |
| Orpí | 680 | 1 | 679 | 0 | **679** | 28 (4 %) | 4 |
| Sant Feliu de Codines | 677 | 1 | 676 | 0 | **676** | 4 (1 %) | 26 |
| Palau-solità i Plegamans | 673 | 1 | 672 | 3 | **669** | 14 (2 %) | 63 |
| Figaró-Montmany | 669 | 0 | 669 | 0 | **669** | 3 (0 %) | 10 |
| Sant Martí d'Albars | 665 | 0 | 665 | 0 | **665** | 66 (10 %) | 6 |
| Granollers | 666 | 4 | 662 | 1 | **661** | 6 (1 %) | 79 |
| la Torre de Claramunt | 660 | 0 | 660 | 0 | **660** | 6 (1 %) | 30 |
| les Masies de Roda | 722 | 81 | 641 | 0 | **641** | 26 (4 %) | 11 |
| Sant Quirze del Vallès | 634 | 1 | 633 | 0 | **633** |  | 58 |
| Santa Eulàlia de Ronçana | 633 | 0 | 633 | 0 | **633** | 13 (2 %) | 18 |
| Santa Eulàlia de Riuprimer | 627 | 1 | 626 | 0 | **626** | 15 (2 %) | 29 |
| Sobremunt | 626 | 0 | 626 | 0 | **626** | 20 (3 %) | 3 |
| Sant Antoni de Vilamajor | 625 | 0 | 625 | 0 | **625** | 19 (3 %) | 69 |
| l'Ametlla del Vallès | 624 | 0 | 624 | 0 | **624** | 11 (2 %) | 38 |
| Sant Agustí de Lluçanès | 623 | 0 | 623 | 0 | **623** | 44 (7 %) | 6 |
| Canyelles | 622 | 0 | 622 | 0 | **622** | 5 (1 %) | 24 |
| Alpens | 622 | 1 | 621 | 0 | **621** | 15 (2 %) | 27 |
| Sant Quintí de Mediona | 616 | 0 | 616 | 0 | **616** | 18 (3 %) | 21 |
| Prats de Lluçanès | 608 | 0 | 608 | 0 | **608** | 5 (1 %) | 43 |
| Montmaneu | 606 | 0 | 606 | 0 | **606** | 88 (15 %) | 43 |
| Torrelles de Llobregat | 603 | 0 | 603 | 0 | **603** | 1 (0 %) | 268 |
| Cubelles | 608 | 7 | 601 | 0 | **601** | 4 (1 %) | 76 |
| Marganell | 594 | 0 | 594 | 0 | **594** | 2 (0 %) | 31 |
| Torelló | 604 | 15 | 589 | 0 | **589** | 38 (6 %) | 32 |
| Sant Fost de Campsentelles | 589 | 3 | 586 | 0 | **586** | 8 (1 %) | 30 |
| l'Hospitalet de Llobregat | 585 | 1 | 584 | 0 | **584** |  | 138 |
| Martorell | 569 | 5 | 564 | 0 | **564** | 3 (1 %) | 72 |
| Santa Susanna | 559 | 0 | 559 | 0 | **559** |  | 35 |
| Castelldefels | 562 | 6 | 556 | 0 | **556** | 5 (1 %) | 42 |
| Cardedeu | 548 | 1 | 547 | 0 | **547** | 9 (2 %) | 95 |
| Callús | 546 | 6 | 540 | 0 | **540** | 11 (2 %) | 65 |
| Sant Andreu de Llavaneres | 534 | 0 | 534 | 0 | **534** |  | 17 |
| Sant Julià de Cerdanyola | 529 | 0 | 529 | 0 | **529** | 8 (2 %) | 21 |
| Sant Feliu de Llobregat | 531 | 4 | 527 | 0 | **527** | 4 (1 %) | 32 |
| Monistrol de Montserrat | 532 | 8 | 524 | 0 | **524** | 23 (4 %) | 49 |
| Carme | 510 | 0 | 510 | 0 | **510** | 18 (4 %) | 11 |
| Malla | 499 | 0 | 499 | 0 | **499** | 43 (9 %) | 14 |
| Folgueroles | 496 | 0 | 496 | 0 | **496** | 15 (3 %) | 13 |
| Mollet del Vallès | 485 | 4 | 481 | 0 | **481** | 20 (4 %) | 59 |
| Sant Esteve de Palautordera | 479 | 0 | 479 | 0 | **479** | 1 (0 %) | 23 |
| Sant Climent de Llobregat | 478 | 0 | 478 | 0 | **478** | 5 (1 %) | 21 |
| Lliçà de Vall | 477 | 1 | 476 | 0 | **476** | 3 (1 %) | 40 |
| Pineda de Mar | 476 | 0 | 476 | 0 | **476** | 1 (0 %) | 90 |
| Vallromanes | 472 | 0 | 472 | 0 | **472** | 1 (0 %) | 43 |
| Vilanova del Camí | 464 | 3 | 461 | 0 | **461** | 1 (0 %) | 43 |
| l'Estany | 456 | 0 | 456 | 0 | **456** | 12 (3 %) | 9 |
| Montornès del Vallès | 455 | 2 | 453 | 0 | **453** | 4 (1 %) | 53 |
| Alella | 429 | 0 | 429 | 0 | **429** | 2 (0 %) | 18 |
| el Pla del Penedès | 420 | 0 | 420 | 0 | **420** | 6 (1 %) | 11 |
| Calaf | 417 | 0 | 417 | 0 | **417** | 62 (15 %) | 18 |
| Vilobí del Penedès | 415 | 2 | 413 | 0 | **413** | 14 (3 %) | 9 |
| Sant Vicenç dels Horts | 404 | 2 | 402 | 0 | **402** | 1 (0 %) | 32 |
| Parets del Vallès | 405 | 4 | 401 | 0 | **401** | 1 (0 %) | 50 |
| Cabrera de Mar | 400 | 0 | 400 | 0 | **400** | 8 (2 %) | 21 |
| Vilassar de Dalt | 396 | 0 | 396 | 0 | **396** | 2 (1 %) | 42 |
| Malgrat de Mar | 395 | 0 | 395 | 0 | **395** | 3 (1 %) | 42 |
| Polinyà | 394 | 0 | 394 | 0 | **394** | 8 (2 %) | 37 |
| Santa Cecília de Voltregà | 393 | 0 | 393 | 0 | **393** | 26 (7 %) |  |
| el Papiol | 389 | 2 | 387 | 0 | **387** | 13 (3 %) | 14 |
| Pallejà | 380 | 6 | 374 | 0 | **374** |  | 26 |
| Igualada | 370 | 1 | 369 | 0 | **369** | 1 (0 %) | 81 |
| Barberà del Vallès | 366 | 1 | 365 | 0 | **365** | 2 (1 %) | 33 |
| Aiguafreda | 360 | 0 | 360 | 0 | **360** |  | 17 |
| Sant Quirze de Besora | 359 | 3 | 356 | 0 | **356** | 15 (4 %) | 12 |
| Sant Vicenç de Montalt | 356 | 0 | 356 | 0 | **356** | 1 (0 %) | 18 |
| Calella | 350 | 0 | 350 | 0 | **350** | 1 (0 %) | 32 |
| Sant Just Desvern | 350 | 0 | 350 | 0 | **350** |  | 38 |
| Tiana | 348 | 1 | 347 | 0 | **347** |  | 32 |
| Sant Pol de Mar | 342 | 0 | 342 | 0 | **342** |  | 26 |
| Campins | 336 | 0 | 336 | 0 | **336** |  | 8 |
| Ullastrell | 330 | 0 | 330 | 0 | **330** | 9 (3 %) | 12 |
| Santa Coloma de Cervelló | 331 | 3 | 328 | 0 | **328** | 3 (1 %) | 93 |
| Santa Eugènia de Berga | 317 | 0 | 317 | 0 | **317** | 23 (7 %) | 26 |
| Cabrils | 311 | 0 | 311 | 0 | **311** |  | 27 |
| Canovelles | 308 | 0 | 308 | 0 | **308** | 3 (1 %) | 49 |
| Santa Coloma de Gramenet | 315 | 7 | 308 | 0 | **308** |  | 36 |
| Cornellà de Llobregat | 304 | 0 | 304 | 0 | **304** |  | 65 |
| Gironella | 307 | 4 | 303 | 0 | **303** | 5 (2 %) | 40 |
| Sant Vicenç de Torelló | 304 | 6 | 298 | 0 | **298** | 4 (1 %) | 16 |
| Teià | 296 | 0 | 296 | 0 | **296** |  | 10 |
| Premià de Dalt | 293 | 0 | 293 | 0 | **293** |  | 19 |
| Arenys de Mar | 289 | 1 | 288 | 0 | **288** | 4 (1 %) | 29 |
| Vallbona d'Anoia | 288 | 0 | 288 | 0 | **288** | 5 (2 %) | 14 |
| Canet de Mar | 285 | 0 | 285 | 0 | **285** | 3 (1 %) | 17 |
| la Granada | 285 | 0 | 285 | 0 | **285** | 12 (4 %) | 11 |
| Sant Cugat Sesgarrigues | 281 | 0 | 281 | 0 | **281** | 18 (6 %) | 10 |
| Sant Joan Despí | 278 | 2 | 276 | 0 | **276** |  | 24 |
| Pacs del Penedès | 270 | 0 | 270 | 0 | **270** | 5 (2 %) | 11 |
| Vilalba Sasserra | 267 | 0 | 267 | 0 | **267** |  | 8 |
| Calldetenes | 257 | 0 | 257 | 0 | **257** | 13 (5 %) | 6 |
| Òrrius | 254 | 0 | 254 | 0 | **254** |  | 26 |
| Sant Andreu de la Barca | 254 | 1 | 253 | 0 | **253** |  | 41 |
| la Palma de Cervelló | 240 | 0 | 240 | 0 | **240** | 1 (0 %) | 5 |
| Navarcles | 248 | 9 | 239 | 0 | **239** |  | 38 |
| Sant Pere de Riudebitlles | 236 | 1 | 235 | 0 | **235** | 1 (0 %) | 13 |
| Montesquiu | 217 | 6 | 211 | 0 | **211** |  | 20 |
| Esplugues de Llobregat | 200 | 0 | 200 | 0 | **200** |  | 68 |
| Santa Maria de Martorelles | 199 | 0 | 199 | 0 | **199** |  | 5 |
| Ripollet | 198 | 1 | 197 | 0 | **197** |  | 75 |
| Vilassar de Mar | 180 | 0 | 180 | 0 | **180** | 2 (1 %) | 25 |
| Sant Adrià de Besòs | 182 | 3 | 179 | 0 | **179** |  | 20 |
| Sant Martí Sesgueioles | 172 | 0 | 172 | 0 | **172** | 29 (17 %) | 1 |
| Montmeló | 174 | 6 | 168 | 0 | **168** |  | 29 |
| Martorelles | 163 | 1 | 162 | 0 | **162** |  | 7 |
| el Masnou | 157 | 0 | 157 | 0 | **157** |  | 37 |
| Santa Fe del Penedès | 148 | 0 | 148 | 0 | **148** | 10 (7 %) | 4 |
| la Llagosta | 134 | 1 | 133 | 0 | **133** | 1 (1 %) | 16 |
| Capellades | 132 | 2 | 130 | 0 | **130** |  | 6 |
| Montgat | 130 | 0 | 130 | 0 | **130** |  | 14 |
| Premià de Mar | 102 | 0 | 102 | 0 | **102** | 3 (3 %) | 25 |
| Roda de Ter | 103 | 1 | 102 | 0 | **102** |  | 1 |
| les Cabanyes | 54 | 0 | 54 | 0 | **54** | 1 (2 %) | 1 |
| Sant Hipòlit de Voltregà | 41 | 0 | 41 | 0 | **41** |  | 15 |
| Badia del Vallès | 39 | 0 | 39 | 0 | **39** |  | 15 |
| Caldes d'Estrac | 37 | 0 | 37 | 0 | **37** |  | 14 |
| Puigdàlber | 31 | 0 | 31 | 0 | **31** |  |  |

## Parcs (19021)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Forêt de Vacarisses (11) ⚠️ | Vacarisses › Vallès Occidental | 1 555 |
| Forêt de Gelida (20) ⚠️ | Gelida › Alt Penedès | 1 422 |
| Forêt de Castellolí (6) ⚠️ | Castellolí › Anoia | 1 326 |
| Forêt de Caldes de Montbui (9) ⚠️ | Caldes de Montbui › Vallès Oriental | 1 222 |
| Forêt de Rupit i Pruit (15) ⚠️ | Rupit i Pruit › Osona (Barcelone) | 1 188 |
| Forêt de Sobremunt (2) ⚠️ | Sobremunt › Osona (Barcelone) | 1 133 |
| Forêt de Mura (14) ⚠️ | Mura › Bages | 1 075 |
| Forêt de Castellar del Vallès (16) ⚠️ | Castellar del Vallès › Vallès Occidental | 1 010 |
| Forêt de Tagamanent (4) ⚠️ | Tagamanent › Vallès Oriental | 953 |
| Forêt de Castellterçol (16) ⚠️ | Castellterçol › Moianès | 911 |
| Forêt de Collbató (4) ⚠️ | Collbató › Baix Llobregat | 860 |
| Bois de Cerdanyola del Vallès (14) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 837 |
| Forêt de Monistrol de Calders (6) ⚠️ | Monistrol de Calders › Moianès | 824 |
| Forêt de Fogars de Montclús (25) ⚠️ | Fogars de Montclús › Vallès Oriental | 755 |
| Forêt de Oristà (108) ⚠️ | Oristà › Moianès | 743 |
| Forêt de Sallent (25) ⚠️ | Sallent › Bages | 732 |
| Forêt de Tagamanent (9) ⚠️ | Tagamanent › Vallès Oriental | 722 |
| Forêt de la Llacuna (8) ⚠️ | la Llacuna › Anoia | 695 |
| Forêt de Olvan (5) ⚠️ | Olvan › Berguedà | 692 |
| Forêt de Gallifa (3) ⚠️ | Gallifa › Vallès Occidental | 638 |
| Forêt de Gaià (11) ⚠️ | Gaià › Bages | 620 |
| Forêt de Orpí (2) ⚠️ | Orpí › Anoia | 606 |
| Forêt de Fígols (4) ⚠️ | Fígols › Berguedà | 597 |
| Forêt de Sant Pere de Torelló (14) ⚠️ | Sant Pere de Torelló › Osona (Barcelone) | 557 |
| Forêt de Terrassa (65) ⚠️ | Terrassa › Vallès Occidental | 555 |
| Forêt de Sant Mateu de Bages (27) ⚠️ | Sant Mateu de Bages › Bages | 553 |
| Forêt de Santa Maria de Miralles (4) ⚠️ | Santa Maria de Miralles › Anoia | 538 |
| Bois de Castellbisbal (3) ⚠️ | Castellbisbal › Vallès Occidental | 534 |
| Forêt de la Pobla de Lillet (10) ⚠️ | la Pobla de Lillet › Berguedà | 530 |
| Forêt de Vallirana (25) ⚠️ | Vallirana › Alt Penedès | 508 |
| Forêt de Santa Maria d'Oló (38) ⚠️ | Santa Maria d'Oló › Moianès | 506 |
| Forêt de Tordera (100) ⚠️ | Tordera › Maresme | 504 |
| Forêt de Mediona (78) ⚠️ | Mediona › Alt Penedès | 502 |
| Forêt de la Nou de Berguedà (6) ⚠️ | la Nou de Berguedà › Berguedà | 500 |
| Forêt de Subirats (93) ⚠️ | Subirats › Alt Penedès | 488 |
| Forêt de Sant Llorenç Savall (16) ⚠️ | Sant Llorenç Savall › Vallès Occidental | 479 |
| Forêt de Rellinars (10) ⚠️ | Rellinars › Bages | 479 |
| Forêt de Saldes (14) ⚠️ | Saldes › Berguedà | 472 |
| Forêt de Sant Iscle de Vallalta (5) ⚠️ | Sant Iscle de Vallalta › Maresme | 468 |
| Forêt de el Brull (9) ⚠️ | el Brull › Osona (Barcelone) | 467 |
| Forêt de Fogars de Montclús (26) ⚠️ | Fogars de Montclús › Vallès Oriental | 449 |
| Forêt de Dosrius (5) ⚠️ | Dosrius › Maresme | 445 |
| Forêt de Vilada (2) ⚠️ | Vilada › Berguedà | 442 |
| Forêt de Sant Pere de Torelló (10) ⚠️ | Sant Pere de Torelló › Osona (Barcelone) | 438 |
| Forêt de Sant Celoni (25) ⚠️ | Sant Celoni › Vallès Oriental | 437 |
| Forêt de Sant Martí Sarroca (28) ⚠️ | Sant Martí Sarroca › Alt Penedès | 436 |
| Forêt de Sant Mateu de Bages (28) ⚠️ | Sant Mateu de Bages › Bages | 433 |
| Forêt de Tavèrnoles ⚠️ | Tavèrnoles › Osona (Barcelone) | 429 |
| Forêt de Begues (30) ⚠️ | Begues › Baix Llobregat | 428 |
| Forêt de Saldes (9) ⚠️ | Saldes › Berguedà | 426 |
| Forêt de Santa Maria d'Oló (34) ⚠️ | Santa Maria d'Oló › Moianès | 423 |
| Forêt de Rajadell (11) ⚠️ | Rajadell › Bages | 419 |
| Forêt de la Pobla de Lillet (7) ⚠️ | la Pobla de Lillet › Berguedà | 418 |
| Forêt de la Garriga (44) ⚠️ | la Garriga › Vallès Oriental | 415 |
| Forêt de Tordera (54) ⚠️ | Tordera › Maresme | 412 |
| Forêt de Castellnou de Bages (38) ⚠️ | Castellnou de Bages › Bages | 410 |
| Forêt de Sant Bartomeu del Grau (10) ⚠️ | Sant Bartomeu del Grau › Osona (Barcelone) | 400 |
| Forêt de Sant Pere de Vilamajor (78) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 397 |
| Forêt de Avinyó (89) ⚠️ | Avinyó › Bages | 395 |
| Forêt de Capolat (8) ⚠️ | Capolat › Berguedà | 386 |
| Forêt de Vallgorguina (2) ⚠️ | Vallgorguina › Vallès Oriental | 385 |
| Forêt de Castellgalí (10) ⚠️ | Castellgalí › Bages | 380 |
| Forêt de Sentmenat ⚠️ | Sentmenat › Vallès Occidental | 375 |
| Forêt de Vilanova del Camí ⚠️ | Vilanova del Camí › Anoia | 361 |
| Forêt de Dosrius (9) ⚠️ | Dosrius › Maresme | 359 |
| Forêt de Sant Llorenç Savall (14) ⚠️ | Sant Llorenç Savall › Vallès Occidental | 351 |
| Forêt de Sant Sadurní d'Osormort (22) ⚠️ | Sant Sadurní d'Osormort › Osona (Barcelone) | 350 |
| Forêt de Avinyó (36) ⚠️ | Avinyó › Bages | 350 |
| Forêt de Vilada (3) ⚠️ | Vilada › Berguedà | 348 |
| Forêt de Castellar del Riu (9) ⚠️ | Castellar del Riu › Berguedà | 346 |
| Forêt de Cercs (24) ⚠️ | Cercs › Berguedà | 344 |
| Forêt de Cervelló (7) ⚠️ | Cervelló › Baix Llobregat | 343 |
| Forêt de Castellcir (2) ⚠️ | Castellcir › Moianès | 339 |
| Forêt de Vallirana (31) ⚠️ | Vallirana › Baix Llobregat | 338 |
| Bois de el Papiol ⚠️ | el Papiol › Baix Llobregat | 336 |
| Forêt de Vacarisses (10) ⚠️ | Vacarisses › Vallès Occidental | 335 |
| Forêt de la Pobla de Lillet (5) ⚠️ | la Pobla de Lillet › Berguedà | 330 |
| Forêt de Cervelló (8) ⚠️ | Cervelló › Baix Llobregat | 329 |
| Forêt de Sant Bartomeu del Grau (15) ⚠️ | Sant Bartomeu del Grau › Osona (Barcelone) | 329 |
| Forêt de Cardona (33) ⚠️ | Cardona › Bages | 323 |
| Forêt de Piera (24) ⚠️ | Piera › Anoia | 318 |
| Forêt de Moià (3) ⚠️ | Moià › Moianès | 314 |
| Forêt de Guardiola de Berguedà (34) ⚠️ | Guardiola de Berguedà › Berguedà | 311 |
| Forêt de Tavertet (30) ⚠️ | Tavertet › Osona (Barcelone) | 309 |
| Forêt de Vallcebre (29) ⚠️ | Vallcebre › Berguedà | 304 |
| Forêt de el Brull (4) ⚠️ | el Brull › Osona (Barcelone) | 302 |
| Forêt de el Pont de Vilomara i Rocafort (21) ⚠️ | el Pont de Vilomara i Rocafort › Bages | 300 |
| Forêt de Moià (38) ⚠️ | Moià › Moianès | 297 |
| Forêt de Vilanova de Sau (10) ⚠️ | Vilanova de Sau › Osona (Barcelone) | 292 |
| Forêt de Granera (18) ⚠️ | Granera › Moianès | 292 |
| Forêt de Montcada i Reixac (27) ⚠️ | Montcada i Reixac › Vallès Occidental | 292 |
| Forêt de el Brull (15) ⚠️ | el Brull › Osona (Barcelone) | 289 |
| Bois de Lliçà d'Amunt (29) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 286 |
| Forêt de Sant Pere de Torelló (7) ⚠️ | Sant Pere de Torelló › Osona (Barcelone) | 285 |
| Forêt de els Hostalets de Pierola (11) ⚠️ | els Hostalets de Pierola › Anoia | 285 |
| Forêt de Cercs (7) ⚠️ | Cercs › Berguedà | 281 |
| Forêt de la Torre de Claramunt ⚠️ | la Torre de Claramunt › Anoia | 280 |
| Forêt de Castellnou de Bages (94) ⚠️ | Castellnou de Bages › Bages | 280 |
| Forêt de Fígols (5) ⚠️ | Fígols › Berguedà | 279 |
| Forêt de Montclar (9) ⚠️ | Montclar › Berguedà | 279 |
| Forêt de Viver i Serrateix (24) ⚠️ | Viver i Serrateix › Berguedà | 279 |
| Forêt de Perafita ⚠️ | Perafita › Lluçanès | 271 |
| Forêt de Castellet i la Gornal (65) ⚠️ | Castellet i la Gornal › Alt Penedès | 269 |
| Forêt de Montseny (2) ⚠️ | Montseny › Vallès Oriental | 268 |
| Forêt de Castellfollit del Boix (15) ⚠️ | Castellfollit del Boix › Bages | 266 |
| Forêt de Sant Feliu de Codines (7) ⚠️ | Sant Feliu de Codines › Vallès Oriental | 266 |
| Forêt de Sant Pere de Vilamajor (77) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 264 |
| Forêt de Sant Mateu de Bages (29) ⚠️ | Sant Mateu de Bages › Bages | 264 |
| Forêt de Sant Jaume de Frontanyà (9) ⚠️ | Sant Jaume de Frontanyà › Berguedà | 263 |
| Forêt de Montmajor (47) ⚠️ | Montmajor › Berguedà | 259 |
| Forêt de Castellfollit del Boix (20) ⚠️ | Castellfollit del Boix › Bages | 259 |
| Forêt de Sant Jaume de Frontanyà (6) ⚠️ | Sant Jaume de Frontanyà › Berguedà | 258 |
| Forêt de la Quar (6) ⚠️ | la Quar › Berguedà | 254 |
| Forêt de Argençola (13) ⚠️ | Argençola › Anoia | 251 |
| Forêt de la Nou de Berguedà (3) ⚠️ | la Nou de Berguedà › Berguedà | 250 |
| Forêt de Capolat (7) ⚠️ | Capolat › Berguedà | 248 |
| Forêt de Moià (29) ⚠️ | Moià › Moianès | 248 |
| Forêt de Argençola (15) ⚠️ | Argençola › Anoia | 246 |
| Forêt de Sagàs (8) ⚠️ | Sagàs › Berguedà | 244 |
| Forêt de Castellcir (10) ⚠️ | Castellcir › Moianès | 243 |
| Forêt de Gualba (5) ⚠️ | Gualba › Vallès Oriental | 243 |
| Forêt de Tordera (46) ⚠️ | Tordera › Maresme | 242 |
| Forêt de Taradell (24) ⚠️ | Taradell › Osona (Barcelone) | 239 |
| Forêt de Seva (9) ⚠️ | Seva › Osona (Barcelone) | 237 |
| Forêt de Castellfollit del Boix (19) ⚠️ | Castellfollit del Boix › Bages | 237 |
| Forêt de Santa Maria de Merlès (28) ⚠️ | Santa Maria de Merlès › Berguedà | 236 |
| Forêt de Matadepera (208) ⚠️ | Matadepera › Vallès Occidental | 235 |
| Forêt de Gualba (3) ⚠️ | Gualba › Vallès Oriental | 235 |
| Forêt de Vilanova de Sau (12) ⚠️ | Vilanova de Sau › Osona (Barcelone) | 233 |
| Forêt de Sant Mateu de Bages (26) ⚠️ | Sant Mateu de Bages › Bages | 233 |
| Forêt de Rubió (8) ⚠️ | Rubió › Anoia | 230 |
| Forêt de Rubió (3) ⚠️ | Rubió › Anoia | 229 |
| Forêt de Bigues i Riells del Fai (13) ⚠️ | Bigues i Riells del Fai › Vallès Oriental | 229 |
| Forêt de Vallgorguina (6) ⚠️ | Vallgorguina › Vallès Oriental | 229 |
| Forêt de Puig-reig (24) ⚠️ | Puig-reig › Berguedà | 228 |
| Forêt de Òdena (8) ⚠️ | Òdena › Anoia | 227 |
| Forêt de Cardona (34) ⚠️ | Cardona › Bages | 227 |
| Forêt de Sant Pere Sallavinera (6) ⚠️ | Sant Pere Sallavinera › Anoia | 226 |
| Forêt de Balsareny (17) ⚠️ | Balsareny › Bages | 225 |
| Forêt de Sallent (26) ⚠️ | Sallent › Bages | 222 |
| Forêt de Vilanova de Sau (32) ⚠️ | Vilanova de Sau › Osona (Barcelone) | 220 |
| Forêt de Sagàs (9) ⚠️ | Sagàs › Berguedà | 220 |
| Forêt de Talamanca (8) ⚠️ | Talamanca › Bages | 220 |
| Forêt de Santa Maria de Besora (2) ⚠️ | Santa Maria de Besora › Osona (Barcelone) | 219 |
| Forêt de Rubió (7) ⚠️ | Rubió › Anoia | 218 |
| Forêt de Gisclareny (14) ⚠️ | Gisclareny › Berguedà | 217 |
| Forêt de Castellar del Vallès (15) ⚠️ | Castellar del Vallès › Vallès Occidental | 216 |
| Forêt de Sant Mateu de Bages (34) ⚠️ | Sant Mateu de Bages › Bages | 216 |
| Forêt de Perafita (3) ⚠️ | Perafita › Lluçanès | 215 |
| Forêt de Castellar del Vallès (12) ⚠️ | Castellar del Vallès › Vallès Occidental | 215 |
| Forêt de Avinyó (61) ⚠️ | Avinyó › Bages | 211 |
| Forêt de Muntanyola (26) ⚠️ | Muntanyola › Osona (Barcelone) | 210 |
| Forêt de la Quar (5) ⚠️ | la Quar › Berguedà | 209 |
| Forêt de Sitges (29) ⚠️ | Sitges › Garraf | 208 |
| Forêt de Esparreguera (6) ⚠️ | Esparreguera › Baix Llobregat | 207 |
| Forêt de Santa Maria d'Oló (37) ⚠️ | Santa Maria d'Oló › Moianès | 206 |
| Forêt de Fogars de la Selva (26) ⚠️ | Fogars de la Selva › la Selva (Barcelone) | 204 |
| Forêt de Aguilar de Segarra (4) ⚠️ | Aguilar de Segarra › Bages | 203 |
| Bois de Molins de Rei (3) ⚠️ | Molins de Rei › Baix Llobregat | 202 |
| Forêt de Castellbell i el Vilar ⚠️ | Castellbell i el Vilar › Bages | 201 |
| Forêt de Collsuspina (7) ⚠️ | Collsuspina › Moianès | 200 |
| Forêt de Sant Quirze Safaja (10) ⚠️ | Sant Quirze Safaja › Moianès | 199 |
| Forêt de la Nou de Berguedà (7) ⚠️ | la Nou de Berguedà › Berguedà | 198 |
| Forêt de Vilanova de Sau (34) ⚠️ | Vilanova de Sau › Osona (Barcelone) | 195 |
| Forêt de Corbera de Llobregat (12) ⚠️ | Corbera de Llobregat › Baix Llobregat | 194 |
| Forêt de Sant Feliu Sasserra (7) ⚠️ | Santa Maria d'Oló › Bages | 191 |
| Forêt de la Llacuna (2) ⚠️ | la Llacuna › Anoia | 190 |
| Forêt de Sant Celoni (29) ⚠️ | Sant Celoni › Vallès Oriental | 190 |
| Forêt de l'Esquirol (116) ⚠️ | l'Esquirol › Osona (Barcelone) | 189 |
| Forêt de l'Espunyola (34) ⚠️ | l'Espunyola › Berguedà | 188 |
| Forêt de la Nou de Berguedà (2) ⚠️ | la Nou de Berguedà › Berguedà | 185 |
| Forêt de Bigues i Riells del Fai (38) ⚠️ | Bigues i Riells del Fai › Vallès Oriental | 185 |
| Forêt de Puig-reig (5) ⚠️ | Puig-reig › Berguedà | 184 |
| Forêt de Gavà (71) ⚠️ | Gavà › Baix Llobregat | 184 |
| Forêt de Fogars de Montclús (11) ⚠️ | Fogars de Montclús › Vallès Oriental | 183 |
| Parc de Montjuïc ⚠️ | Barcelona › Barcelonès | 182 |
| Forêt de Olvan (7) ⚠️ | Olvan › Berguedà | 182 |
| Forêt de Santa Maria de Palautordera (27) ⚠️ | Santa Maria de Palautordera › Vallès Oriental | 182 |
| Forêt de Sant Salvador de Guardiola (57) ⚠️ | Sant Salvador de Guardiola › Bages | 181 |
| Forêt de Sant Quirze del Vallès (18) ⚠️ | Sant Quirze del Vallès › Vallès Occidental | 181 |
| Forêt de Santa Susanna ⚠️ | Santa Susanna › Maresme | 180 |
| Forêt de Guardiola de Berguedà (14) ⚠️ | Guardiola de Berguedà › Berguedà | 179 |
| Forêt de Calders (6) ⚠️ | Calders › Moianès | 178 |
| Forêt de Castell de l'Areny (21) ⚠️ | Castell de l'Areny › Berguedà | 177 |
| Forêt de Navàs (83) ⚠️ | Navàs › Bages | 177 |
| Forêt de Moià (17) ⚠️ | Moià › Moianès | 176 |
| Bois de la Palma de Cervelló ⚠️ | la Palma de Cervelló › Baix Llobregat | 175 |
| Forêt de Argençola (25) ⚠️ | Argençola › Anoia | 175 |
| Forêt de Sant Esteve de Palautordera (4) ⚠️ | Sant Esteve de Palautordera › Vallès Oriental | 175 |
| Forêt de Viver i Serrateix (63) ⚠️ | Viver i Serrateix › Berguedà | 175 |
| Forêt de Viver i Serrateix (45) ⚠️ | Viver i Serrateix › Berguedà | 174 |
| Forêt de Súria (5) ⚠️ | Súria › Bages | 173 |
| Forêt de Castellfollit del Boix (16) ⚠️ | Castellfollit del Boix › Bages | 171 |
| Forêt de Santa Maria de Martorelles (3) ⚠️ | Santa Maria de Martorelles › Vallès Oriental | 171 |
| Forêt de Rubió (5) ⚠️ | Rubió › Anoia | 168 |
| Forêt de Tordera (52) ⚠️ | Tordera › Maresme | 168 |
| Forêt de Sant Iscle de Vallalta (6) ⚠️ | Sant Iscle de Vallalta › Maresme | 168 |
| Forêt de Capolat (6) ⚠️ | Capolat › Berguedà | 167 |
| Forêt de Sant Quirze del Vallès (15) ⚠️ | Sant Quirze del Vallès › Vallès Occidental | 167 |
| Forêt de Sant Pere de Torelló (2) ⚠️ | Sant Pere de Torelló › Osona (Barcelone) | 166 |
| Forêt de Sora (18) ⚠️ | Sora › Osona (Barcelone) | 166 |
| Forêt de Castellfollit del Boix (14) ⚠️ | Castellfollit del Boix › Bages | 166 |
| Forêt de Castellbisbal (12) ⚠️ | Castellbisbal › Vallès Occidental | 166 |
| Forêt de Tordera (36) ⚠️ | Tordera › Maresme | 165 |
| Forêt de Vallgorguina (7) ⚠️ | Vallgorguina › Vallès Oriental | 165 |
| Forêt de el Brull (12) ⚠️ | el Brull › Osona (Barcelone) | 164 |
| Forêt de Montmajor (128) ⚠️ | Montmajor › Berguedà | 164 |
| Forêt de Sant Martí de Tous (11) ⚠️ | Sant Martí de Tous › Anoia | 164 |
| Bois de Barcelona (96) ⚠️ | Barcelona › Barcelonès | 162 |
| Forêt de Navàs (154) ⚠️ | Navàs › Bages | 162 |
| Forêt de Navàs (132) ⚠️ | Navàs › Bages | 161 |
| Bois de Montornès del Vallès (3) ⚠️ | Montornès del Vallès › Vallès Oriental | 161 |
| Forêt de Sant Agustí de Lluçanès (2) ⚠️ | Sant Agustí de Lluçanès › Osona (Barcelone) | 160 |
| Forêt de Santa Coloma de Cervelló (7) ⚠️ | Santa Coloma de Cervelló › Baix Llobregat | 160 |
| Forêt de Castellnou de Bages (36) ⚠️ | Castellnou de Bages › Bages | 160 |
| Forêt de Navàs (131) ⚠️ | Navàs › Bages | 160 |
| Forêt de Figaró-Montmany (3) ⚠️ | Figaró-Montmany › Vallès Oriental | 160 |
| Forêt de Sant Vicenç dels Horts (6) ⚠️ | Sant Vicenç dels Horts › Baix Llobregat | 157 |
| Bois de Llinars del Vallès (32) ⚠️ | Llinars del Vallès › Vallès Oriental | 157 |
| Forêt de Saldes (81) ⚠️ | Saldes › Berguedà | 157 |
| Forêt de Saldes (43) ⚠️ | Saldes › Berguedà | 156 |
| Forêt de Montseny ⚠️ | Montseny › Vallès Oriental | 155 |
| Forêt de Santa Margarida de Montbui (12) ⚠️ | Santa Margarida de Montbui › Anoia | 155 |
| Forêt de Santa Maria de Besora (13) ⚠️ | Santa Maria de Besora › Osona (Barcelone) | 155 |
| Forêt de Castell de l'Areny ⚠️ | Castell de l'Areny › Berguedà | 154 |
| Forêt de Santa Maria d'Oló (33) ⚠️ | Santa Maria d'Oló › Moianès | 154 |
| Forêt de Fonollosa (82) ⚠️ | Fonollosa › Bages | 152 |
| Forêt de Sant Pere de Torelló (9) ⚠️ | Sant Pere de Torelló › Osona (Barcelone) | 151 |
| Forêt de Castellar del Vallès (13) ⚠️ | Castellar del Vallès › Vallès Occidental | 151 |
| Forêt de Avinyó (60) ⚠️ | Avinyó › Bages | 151 |
| Forêt de Castell de l'Areny (9) ⚠️ | Castell de l'Areny › Berguedà | 151 |
| Forêt de Navàs (70) ⚠️ | Navàs › Bages | 151 |
| Bois de Sant Cugat del Vallès (120) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 151 |
| Forêt de Cànoves i Samalús (28) ⚠️ | Cànoves i Samalús › Vallès Oriental | 150 |
| Forêt de Avinyonet del Penedès (55) ⚠️ | Avinyonet del Penedès › Alt Penedès | 150 |
| Forêt de Balsareny (16) ⚠️ | Balsareny › Bages | 149 |
| Forêt de el Bruc (6) ⚠️ | el Bruc › Anoia | 149 |
| Forêt de Castellfollit de Riubregós (5) ⚠️ | Castellfollit de Riubregós › Anoia | 149 |
| Forêt de Argençola (12) ⚠️ | Argençola › Anoia | 148 |
| Forêt de Tordera (49) ⚠️ | Tordera › Maresme | 147 |
| Forêt de Vallbona d'Anoia ⚠️ | Vallbona d'Anoia › Anoia | 147 |
| Forêt de Sallent (44) ⚠️ | Sallent › Bages | 147 |
| Forêt de Bagà (4) ⚠️ | Bagà › Berguedà | 146 |
| Forêt de Mura (20) ⚠️ | Mura › Bages | 146 |
| Forêt de Tordera (53) ⚠️ | Tordera › Maresme | 145 |
| Forêt de Montseny (3) ⚠️ | Montseny › Vallès Oriental | 144 |
| Forêt de Santa Maria d'Oló (15) ⚠️ | Santa Maria d'Oló › Moianès | 144 |
| Forêt de Pallejà (3) ⚠️ | Pallejà › Baix Llobregat | 144 |
| Forêt de Vacarisses (9) ⚠️ | Vacarisses › Vallès Occidental | 143 |
| Forêt de Viver i Serrateix (50) ⚠️ | Viver i Serrateix › Berguedà | 143 |
| Forêt de Balsareny (18) ⚠️ | Balsareny › Bages | 142 |
| Forêt de Viver i Serrateix (88) ⚠️ | Viver i Serrateix › Berguedà | 142 |
| Forêt de Bellprat (7) ⚠️ | Bellprat › Anoia | 141 |
| Forêt de Cardona (103) ⚠️ | Cardona › Bages | 141 |
| Forêt de Sant Sadurní d'Osormort (39) ⚠️ | Sant Sadurní d'Osormort › Osona (Barcelone) | 140 |
| Forêt de la Llacuna (5) ⚠️ | la Llacuna › Anoia | 139 |
| Forêt de Sant Martí de Centelles (48) ⚠️ | Sant Martí de Centelles › Osona (Barcelone) | 139 |
| Forêt de Oristà (85) ⚠️ | Oristà › Lluçanès | 139 |
| Forêt de Mediona (9) ⚠️ | Mediona › Alt Penedès | 139 |
| Bois de Barcelona (104) ⚠️ | Barcelona › Barcelonès | 139 |
| Forêt de Dosrius (6) ⚠️ | Dosrius › Vallès Oriental | 139 |
| Forêt de Sant Martí de Tous (6) ⚠️ | Sant Martí de Tous › Anoia | 138 |
| Forêt de Moià (26) ⚠️ | Moià › Moianès | 138 |
| Forêt de Gisclareny (11) ⚠️ | Gisclareny › Berguedà | 138 |
| Forêt de Sant Celoni (72) ⚠️ | Sant Celoni › Vallès Oriental | 138 |
| Forêt de Lluçà (3) ⚠️ | Lluçà › Lluçanès | 137 |
| Forêt de Capolat (16) ⚠️ | Capolat › Berguedà | 137 |
| Forêt de Casserres (13) ⚠️ | Casserres › Berguedà | 136 |
| Forêt de Santa Maria de Palautordera (16) ⚠️ | Santa Maria de Palautordera › Vallès Oriental | 135 |
| Forêt de Terrassa (72) ⚠️ | Terrassa › Vallès Occidental | 134 |
| Forêt de Castellnou de Bages (37) ⚠️ | Castellnou de Bages › Bages | 133 |
| Forêt de Sant Mateu de Bages (37) ⚠️ | Sant Mateu de Bages › Bages | 133 |
| Forêt de Viver i Serrateix (67) ⚠️ | Viver i Serrateix › Berguedà | 133 |
| Forêt de Sant Celoni (27) ⚠️ | Sant Celoni › Vallès Oriental | 132 |
| Forêt de Sant Iscle de Vallalta (2) ⚠️ | Sant Iscle de Vallalta › Maresme | 131 |
| Forêt de Castellet i la Gornal (72) ⚠️ | Castellet i la Gornal › Alt Penedès | 131 |
| Forêt de Lluçà (5) ⚠️ | Lluçà › Lluçanès | 130 |
| Forêt de Bagà (7) ⚠️ | Bagà › Berguedà | 129 |
| Forêt de Sant Llorenç Savall (19) ⚠️ | Sant Llorenç Savall › Vallès Occidental | 129 |
| Forêt de Castellar de n'Hug (9) ⚠️ | Castellar de n'Hug › Berguedà | 128 |
| Forêt de Vallcebre (14) ⚠️ | Vallcebre › Berguedà | 127 |
| Forêt de Sant Pere de Vilamajor (80) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 127 |
| Forêt de Berga (18) ⚠️ | Berga › Berguedà | 127 |
| Forêt de Tavertet (34) ⚠️ | Tavertet › Osona (Barcelone) | 127 |
| Forêt de Montseny (10) | Montseny › Vallès Oriental | 125 |
| Forêt de la Pobla de Lillet (59) | la Pobla de Lillet › Berguedà | 125 |
| Forêt de Fogars de la Selva (24) | Fogars de la Selva › la Selva (Barcelone) | 125 |
| Forêt de Bellprat (3) | Bellprat › Anoia | 124 |
| Forêt de Sant Celoni (24) | Sant Celoni › Vallès Oriental | 124 |
| Forêt de Fogars de Montclús (10) | Fogars de Montclús › Vallès Oriental | 122 |
| Forêt de els Hostalets de Pierola (3) | els Hostalets de Pierola › Anoia | 121 |
| Forêt de Rajadell (9) | Rajadell › Bages | 121 |
| Forêt de Castellgalí (11) | Castellgalí › Bages | 121 |
| Forêt de Súria (23) | Súria › Bages | 121 |
| Forêt de la Pobla de Claramunt (4) | la Pobla de Claramunt › Anoia | 120 |
| Forêt de Cercs (37) | Cercs › Berguedà | 120 |
| Forêt de Sant Bartomeu del Grau (2) | Sant Bartomeu del Grau › Osona (Barcelone) | 119 |
| Forêt de Vilanova de Sau (30) | Vilanova de Sau › Osona (Barcelone) | 119 |
| Forêt de Sant Pere de Vilamajor (86) | Sant Pere de Vilamajor › Vallès Oriental | 119 |
| Forêt de Tordera (102) | Tordera › Maresme | 118 |
| Forêt de Jorba (5) | Jorba › Anoia | 117 |
| Forêt de Prats de Lluçanès (3) | Prats de Lluçanès › Lluçanès | 117 |
| Forêt de Sant Pere de Ribes (107) | Sant Pere de Ribes › Garraf | 117 |
| Forêt de Rajadell (27) | Rajadell › Bages | 116 |
| Forêt de Gallifa (2) | Gallifa › Vallès Occidental | 115 |
| Forêt de Saldes (6) | Saldes › Berguedà | 115 |
| Forêt de Mura (13) | Mura › Bages | 115 |
| Forêt de Viladecavalls (5) | Viladecavalls › Vallès Occidental | 115 |
| Forêt de Olivella (124) | Olivella › Garraf | 115 |
| Forêt de Puig-reig (83) | Puig-reig › Berguedà | 114 |
| Forêt de Sant Julià de Vilatorta (3) | Sant Julià de Vilatorta › Osona (Barcelone) | 114 |
| Forêt de Vilanova de Sau (5) | Vilanova de Sau › Osona (Barcelone) | 113 |
| Forêt de Marganell (2) | Marganell › Bages | 113 |
| Forêt de Montmajor (65) | Montmajor › Berguedà | 113 |
| Forêt de Bagà (10) | Bagà › Berguedà | 113 |
| Forêt de Moià (36) | Moià › Moianès | 113 |
| Forêt de Santa Maria de Merlès (42) | Santa Maria de Merlès › Berguedà | 113 |
| Forêt de Tordera (107) | Tordera › Maresme | 113 |
| Forêt de Gavà (70) | Gavà › Baix Llobregat | 112 |
| Forêt de Montmajor (93) | Montmajor › Berguedà | 112 |
| Forêt de la Quar (31) | la Quar › Berguedà | 112 |
| Forêt de Sant Pere de Ribes (113) | Sant Pere de Ribes › Garraf | 112 |
| Forêt de Lluçà (61) | Lluçà › Lluçanès | 112 |
| Forêt de Sant Julià de Cerdanyola (2) | Sant Julià de Cerdanyola › Berguedà | 111 |
| Forêt de Castellolí (27) | Castellolí › Anoia | 111 |
| Forêt de Fogars de la Selva (31) | Fogars de la Selva › la Selva (Barcelone) | 111 |
| Forêt de Sant Bartomeu del Grau (3) | Sant Bartomeu del Grau › Osona (Barcelone) | 110 |
| Forêt de Borredà (19) | Borredà › Berguedà | 110 |
| Forêt de Gualba (19) | Gualba › Vallès Oriental | 110 |
| Forêt de Sobremunt (3) | Sobremunt › Lluçanès | 110 |
| Forêt de Masquefa (2) | Masquefa › Anoia | 109 |
| Forêt de Bellprat (8) | Bellprat › Anoia | 109 |
| Forêt de Castellfollit del Boix (18) | Castellfollit del Boix › Bages | 109 |
| Forêt de Rubí (64) | Rubí › Vallès Occidental | 109 |
| Forêt de Rajadell (50) | Rajadell › Bages | 109 |
| Forêt de Sant Feliu Sasserra (14) | Sant Feliu Sasserra › Bages | 109 |
| Forêt de Cerdanyola del Vallès (62) | Cerdanyola del Vallès › Vallès Occidental | 109 |
| Forêt de Castellar de n'Hug (6) | Castellar de n'Hug › Berguedà | 108 |
| Forêt de Calders (63) | Calders › Moianès | 108 |
| Forêt de Sora (11) | Sora › Osona (Barcelone) | 107 |
| Forêt de Balsareny (64) | Balsareny › Bages | 107 |
| Forêt de Montesquiu | Montesquiu › Osona (Barcelone) | 107 |
| Forêt de Muntanyola (15) | Muntanyola › Osona (Barcelone) | 107 |
| Forêt de Seva (16) | Seva › Osona (Barcelone) | 106 |
| Forêt de Gaià (49) | Gaià › Bages | 106 |
| Forêt de Castellfollit del Boix (23) | Castellfollit del Boix › Bages | 106 |
| Forêt de Castellolí (26) | Castellolí › Anoia | 106 |
| Forêt de Santa Maria de Merlès (51) | Santa Maria de Merlès › Berguedà | 106 |
| Forêt de Borredà (24) | Borredà › Berguedà | 106 |
| Forêt de Gisclareny (22) | Gisclareny › Berguedà | 106 |
| Forêt de Esparreguera (9) | Esparreguera › Baix Llobregat | 105 |
| Forêt de Vilanova de Sau (58) | Vilanova de Sau › Osona (Barcelone) | 105 |
| Forêt de Montmajor (26) | Montmajor › Berguedà | 104 |
| Forêt de Avinyó (16) | Avinyó › Bages | 104 |
| Forêt de Sant Vicenç de Castellet (9) | Sant Vicenç de Castellet › Bages | 104 |
| Forêt de la Roca del Vallès (10) | la Roca del Vallès › Vallès Oriental | 104 |
| Forêt de Santa Maria de Besora (17) | Santa Maria de Besora › Osona (Barcelone) | 104 |
| Forêt de Fogars de la Selva (11) | Fogars de la Selva › la Selva (Barcelone) | 104 |
| Forêt de l'Esquirol (45) | l'Esquirol › Osona (Barcelone) | 103 |
| Forêt de Canet de Mar | Canet de Mar › Maresme | 103 |
| Forêt de Guardiola de Berguedà (33) | Guardiola de Berguedà › Berguedà | 103 |
| Forêt de Vilassar de Dalt (3) | Vilassar de Dalt › Maresme | 103 |
| Forêt de Mediona (10) | Mediona › Alt Penedès | 103 |
| Forêt de Castellet i la Gornal (81) | Castellet i la Gornal › Alt Penedès | 102 |
| Forêt de Sant Sadurní d'Osormort (29) | Sant Sadurní d'Osormort › Osona (Barcelone) | 102 |
| Forêt de Gisclareny (17) | Gisclareny › Berguedà | 101 |
| Forêt de Campins (7) | Campins › Vallès Oriental | 101 |
| Forêt de Cercs (11) | Cercs › Berguedà | 100 |
| Forêt de Fonollosa (81) | Fonollosa › Bages | 99 |
| Forêt de Tordera (50) | Tordera › Maresme | 99 |
| Forêt de Mediona (93) | Mediona › Alt Penedès | 99 |
| Forêt de Sant Celoni (30) | Sant Celoni › Vallès Oriental | 99 |
| Forêt de Sant Agustí de Lluçanès (3) | Sant Agustí de Lluçanès › Osona (Barcelone) | 98 |
| Forêt de Folgueroles | Folgueroles › Osona (Barcelone) | 98 |
| Forêt de Matadepera (210) | Matadepera › Vallès Occidental | 98 |
| Forêt de Casserres (17) | Casserres › Berguedà | 98 |
| Forêt de Navàs (59) | Navàs › Bages | 98 |
| Forêt de Montclar (30) | Montclar › Berguedà | 98 |
| Forêt de l'Esquirol (119) | l'Esquirol › Osona (Barcelone) | 98 |
| Forêt de Sant Sadurní d'Osormort (28) | Sant Sadurní d'Osormort › Osona (Barcelone) | 98 |
| Forêt de Argentona (13) | Argentona › Maresme | 98 |
| Forêt de Oristà (101) | Oristà › Lluçanès | 97 |
| Forêt de Cardona (70) | Cardona › Bages | 97 |
| Forêt de l'Esquirol (117) | l'Esquirol › Osona (Barcelone) | 97 |
| Forêt de Sora (20) | Sora › Osona (Barcelone) | 96 |
| Forêt de Òdena (7) | Òdena › Anoia | 96 |
| Forêt de Santa Maria de Besora (6) | Santa Maria de Besora › Osona (Barcelone) | 96 |
| Forêt de Borredà (58) | Borredà › Berguedà | 96 |
| Forêt de Muntanyola (24) | Muntanyola › Osona (Barcelone) | 96 |
| Forêt de Tordera (112) | Tordera › Maresme | 96 |
| Forêt de Matadepera (206) | Matadepera › Vallès Occidental | 95 |
| Forêt de Tagamanent (5) | Tagamanent › Vallès Oriental | 95 |
| Forêt de Sant Feliu de Codines (8) | Sant Feliu de Codines › Vallès Oriental | 95 |
| Forêt de Santa Margarida de Montbui (14) | Santa Margarida de Montbui › Anoia | 95 |
| Forêt de Gaià (60) | Gaià › Bages | 95 |
| Forêt de Santa Maria de Merlès (61) | Santa Maria de Merlès › Berguedà | 95 |
| Forêt de Muntanyola (32) | Muntanyola › Osona (Barcelone) | 95 |
| Forêt de Òdena (6) | Òdena › Anoia | 94 |
| Forêt de la Quar (7) | la Quar › Berguedà | 94 |
| Forêt de Navàs (38) | Navàs › Bages | 94 |
| Forêt de Fígols (11) | Fígols › Berguedà | 94 |
| Forêt de la Quar (23) | la Quar › Berguedà | 94 |
| Forêt de els Hostalets de Pierola (15) | els Hostalets de Pierola › Anoia | 94 |
| Forêt de Vilanova de Sau | Vilanova de Sau › Osona (Barcelone) | 93 |
| Forêt de Capolat (19) | Capolat › Berguedà | 93 |
| Forêt de Vilanova de Sau (37) | Vilanova de Sau › Osona (Barcelone) | 93 |
| Forêt de Montmajor (110) | Montmajor › Berguedà | 93 |
| Forêt de Castellet i la Gornal (67) | Castellet i la Gornal › Alt Penedès | 93 |
| Forêt de Cardona (95) | Cardona › Bages | 93 |
| Forêt de Vallgorguina (3) | Vallgorguina › Vallès Oriental | 93 |
| Forêt de Pontons (8) | Pontons › Alt Penedès | 93 |
| Forêt de Gaià (25) | Gaià › Bages | 92 |
| Forêt de Santa Maria de Merlès (52) | Santa Maria de Merlès › Berguedà | 92 |
| Forêt de Santa Margarida i els Monjos | Santa Margarida i els Monjos › Alt Penedès | 91 |
| Forêt de Marganell (3) | Marganell › Bages | 91 |
| Forêt de Sant Mateu de Bages (33) | Sant Mateu de Bages › Bages | 91 |
| Forêt de Cervelló (10) | Cervelló › Baix Llobregat | 91 |
| Forêt de Talamanca (18) | Talamanca › Bages | 91 |
| Bois de Molins de Rei (4) | Molins de Rei › Baix Llobregat | 91 |
| Forêt de Cabrera d'Anoia (8) | Cabrera d'Anoia › Anoia | 91 |
| Forêt de Vilanova de Sau (63) | Vilanova de Sau › Osona (Barcelone) | 91 |
| Forêt de Balsareny (23) | Balsareny › Bages | 90 |
| Forêt de Castellar de n'Hug (16) | Castellar de n'Hug › Berguedà | 90 |
| Forêt de Navàs (53) | Navàs › Bages | 90 |
| Forêt de Cardona (61) | Cardona › Bages | 90 |
| Bois de Sant Just Desvern (4) | Sant Just Desvern › Baix Llobregat | 90 |
| Forêt de Sora (4) | Sora › Osona (Barcelone) | 89 |
| Forêt de Sant Pere de Ribes | Sant Pere de Ribes › Garraf | 89 |
| Forêt de Gurb (3) | Gurb › Osona (Barcelone) | 89 |
| Forêt de Corbera de Llobregat (11) | Corbera de Llobregat › Baix Llobregat | 89 |
| Forêt de la Pobla de Lillet (32) | la Pobla de Lillet › Berguedà | 89 |
| Forêt de Castellar de n'Hug (18) | Castellar de n'Hug › Berguedà | 89 |
| Forêt de Arenys de Munt (5) | Arenys de Munt › Maresme | 89 |
| Bois de la Roca del Vallès (4) | la Roca del Vallès › Vallès Oriental | 88 |
| Forêt de Súria (4) | Súria › Bages | 88 |
| Forêt de Castellfollit de Riubregós (8) | Castellfollit de Riubregós › Anoia | 88 |
| Bois de Sant Feliu de Llobregat (2) | Sant Feliu de Llobregat › Baix Llobregat | 88 |
| Bois de Sant Feliu de Llobregat (4) | Sant Feliu de Llobregat › Baix Llobregat | 88 |
| Forêt de Sant Celoni (38) | Sant Celoni › Vallès Oriental | 88 |
| Forêt de Sant Celoni (4) | Sant Celoni › Vallès Oriental | 87 |
| Forêt de la Nou de Berguedà (10) | la Nou de Berguedà › Berguedà | 87 |
| Forêt de Navàs (60) | Navàs › Bages | 87 |
| Forêt de Cabrera d'Anoia (33) | Cabrera d'Anoia › Anoia | 87 |
| Forêt de Mediona (85) | Mediona › Alt Penedès | 87 |
| Forêt de Lluçà (63) | Lluçà › Lluçanès | 87 |
| Forêt de Sant Cebrià de Vallalta (7) | Sant Cebrià de Vallalta › Maresme | 87 |
| Forêt de Sant Andreu de Llavaneres (2) | Sant Andreu de Llavaneres › Maresme | 86 |
| Forêt de Montmajor (3) | Montmajor › Berguedà | 86 |
| Forêt de Fonollosa (79) | Fonollosa › Bages | 86 |
| Forêt de Aguilar de Segarra (19) | Aguilar de Segarra › Bages | 86 |
| Forêt de Òdena (9) | Òdena › Anoia | 85 |
| Forêt de Sant Mateu de Bages (32) | Sant Mateu de Bages › Bages | 85 |
| Forêt de Sant Martí de Centelles (68) | Sant Martí de Centelles › Osona (Barcelone) | 85 |
| Forêt de Oristà (128) | Oristà › Lluçanès | 85 |
| Forêt de Bigues i Riells del Fai (6) | Bigues i Riells del Fai › Vallès Oriental | 84 |
| Forêt de el Bruc (12) | el Bruc › Anoia | 84 |
| Forêt de Berga (36) | Berga › Berguedà | 84 |
| Forêt de Borredà (11) | Borredà › Berguedà | 84 |
| Forêt de Castellar del Riu (19) | Castellar del Riu › Berguedà | 84 |
| Forêt de Bagà (19) | Bagà › Berguedà | 84 |
| Forêt de Santa Maria de Merlès (132) | Santa Maria de Merlès › Berguedà | 84 |
| Forêt de Lluçà (37) | Lluçà › Lluçanès | 84 |
| Forêt de Copons (5) | Copons › Anoia | 83 |
| Forêt de Castellterçol (21) | Castellterçol › Moianès | 83 |
| Forêt de Puig-reig (61) | Puig-reig › Berguedà | 83 |
| Forêt de Olivella (123) | Olivella › Garraf | 83 |
| Forêt de Oristà (156) | Oristà › Lluçanès | 83 |
| Forêt de Aguilar de Segarra (2) | Aguilar de Segarra › Bages | 82 |
| Forêt de Aguilar de Segarra (21) | Aguilar de Segarra › Bages | 82 |
| Forêt de Castellar del Riu (12) | Castellar del Riu › Berguedà | 82 |
| Forêt de Guardiola de Berguedà (43) | Guardiola de Berguedà › Berguedà | 82 |
| Forêt de Viver i Serrateix (38) | Viver i Serrateix › Berguedà | 82 |
| Forêt de Olesa de Bonesvalls (44) | Olesa de Bonesvalls › Alt Penedès | 82 |
| Forêt de Gallifa (8) | Gallifa › Vallès Occidental | 82 |
| Forêt de Font-rubí (2) | Font-rubí › Alt Penedès | 81 |
| Forêt de Tavèrnoles (2) | Tavèrnoles › Osona (Barcelone) | 81 |
| Forêt de el Brull (17) | el Brull › Osona (Barcelone) | 81 |
| Forêt de Cercs (20) | Cercs › Berguedà | 81 |
| Forêt de Santa Maria de Merlès (39) | Santa Maria de Merlès › Berguedà | 81 |
| Forêt de Vic (33) | Vic › Osona (Barcelone) | 81 |
| Forêt de Gisclareny (26) | Gisclareny › Berguedà | 81 |
| Forêt de Guardiola de Berguedà (13) | Guardiola de Berguedà › Berguedà | 80 |
| Forêt de Sant Salvador de Guardiola (37) | Sant Salvador de Guardiola › Bages | 80 |
| Forêt de Castellar de n'Hug (13) | Castellar de n'Hug › Berguedà | 80 |
| Forêt de Santa Maria d'Oló (77) | Santa Maria d'Oló › Moianès | 80 |
| Forêt de Santa Eulàlia de Riuprimer (10) | Santa Eulàlia de Riuprimer › Osona (Barcelone) | 80 |
| Forêt de Fonollosa (155) | Fonollosa › Bages | 80 |
| Forêt de Olivella (51) | Olivella › Garraf | 79 |
| Forêt de Sant Llorenç Savall (15) | Sant Llorenç Savall › Vallès Occidental | 79 |
| Forêt de Sant Mateu de Bages (35) | Sant Mateu de Bages › Bages | 79 |
| Forêt de Cercs (21) | Cercs › Berguedà | 79 |
| Forêt de Montmajor (64) | Montmajor › Berguedà | 79 |
| Forêt de Puig-reig (35) | Puig-reig › Berguedà | 79 |
| Forêt de Centelles (13) | Centelles › Osona (Barcelone) | 79 |
| Forêt de Lluçà (15) | Lluçà › Lluçanès | 79 |
| Forêt de Bagà (62) | Bagà › Berguedà | 79 |
| Forêt de Tavertet | Tavertet › Osona (Barcelone) | 78 |
| Forêt de Tagamanent (11) | Tagamanent › Vallès Oriental | 78 |
| Forêt de Sant Joan de Vilatorrada (19) | Sant Joan de Vilatorrada › Bages | 78 |
| Forêt de Castellfollit del Boix (17) | Castellfollit del Boix › Bages | 78 |
| Forêt de Cardona (62) | Cardona › Bages | 78 |
| Forêt de Torrelles de Foix (5) | Torrelles de Foix › Alt Penedès | 78 |
| Forêt de Fogars de la Selva (6) | Fogars de la Selva › la Selva (Barcelone) | 77 |
| Forêt de Gurb (8) | Gurb › Osona (Barcelone) | 77 |
| Forêt de Capolat (10) | Capolat › Berguedà | 77 |
| Forêt de Castellar de n'Hug (19) | Castellar de n'Hug › Berguedà | 77 |
| Forêt de Sant Vicenç de Montalt (3) | Sant Vicenç de Montalt › Maresme | 77 |
| Bois de els Hostalets de Pierola (3) | els Hostalets de Pierola › Anoia | 77 |
| Forêt de Argençola (14) | Argençola › Anoia | 76 |
| Forêt de Vilanova de Sau (29) | Vilanova de Sau › Osona (Barcelone) | 76 |
| Forêt de Aguilar de Segarra (27) | Aguilar de Segarra › Bages | 76 |
| Forêt de Santa Maria de Merlès (12) | Santa Maria de Merlès › Berguedà | 76 |
| Forêt de Vallgorguina (4) | Vallgorguina › Vallès Oriental | 76 |
| Forêt de Fonollosa (80) | Fonollosa › Bages | 75 |
| Forêt de Saldes (63) | Saldes › Berguedà | 75 |
| Forêt de Font-rubí (24) | Font-rubí › Alt Penedès | 75 |
| Forêt de Sant Cebrià de Vallalta (14) | Sant Cebrià de Vallalta › Maresme | 75 |
| Forêt de Fogars de la Selva (32) | Fogars de la Selva › la Selva (Barcelone) | 75 |
| Forêt de Sant Martí de Tous (5) | Sant Martí de Tous › Anoia | 74 |
| Forêt de Cànoves i Samalús (29) | Cànoves i Samalús › Vallès Oriental | 74 |
| Forêt de Puig-reig (45) | Puig-reig › Berguedà | 74 |
| Forêt de Fogars de la Selva (49) | Fogars de la Selva › la Selva (Barcelone) | 74 |
| Forêt de Argençola (10) | Argençola › Anoia | 73 |
| Forêt de Pallejà (5) | Pallejà › Baix Llobregat | 73 |
| Forêt de Santa Maria de Besora (12) | Santa Maria de Besora › Osona (Barcelone) | 73 |
| Forêt de Navàs (144) | Navàs › Bages | 73 |
| Forêt de Castellar del Riu (36) | Castellar del Riu › Berguedà | 73 |
| Forêt de Lluçà (42) | Lluçà › Lluçanès | 73 |
| Forêt de Malgrat de Mar (5) | Malgrat de Mar › Maresme | 73 |
| Forêt de Olèrdola | Olèrdola › Alt Penedès | 72 |
| Forêt de Vilanova de Sau (13) | Vilanova de Sau › Osona (Barcelone) | 72 |
| Forêt de Montclar | Montclar › Berguedà | 72 |
| Forêt de Sabadell (79) | Sabadell › Vallès Occidental | 72 |
| Forêt de Sant Esteve Sesrovires (25) | Sant Esteve Sesrovires › Baix Llobregat | 72 |
| Forêt de Guardiola de Berguedà (30) | Guardiola de Berguedà › Berguedà | 72 |
| Forêt de Argençola (27) | Argençola › Anoia | 72 |
| Forêt de Sant Fost de Campsentelles (15) | Sant Fost de Campsentelles › Vallès Oriental | 72 |
| Forêt de Orís (27) | Orís › Osona (Barcelone) | 72 |
| Forêt de Sant Climent de Llobregat (3) | Sant Climent de Llobregat › Baix Llobregat | 71 |
| Forêt de Torrelles de Llobregat (2) | Torrelles de Llobregat › Baix Llobregat | 71 |
| Forêt de Torrelavit (2) | Torrelavit › Alt Penedès | 71 |
| Forêt de Rubió (4) | Rubió › Anoia | 71 |
| Forêt de Lluçà (6) | Lluçà › Lluçanès | 71 |
| Forêt de Sallent (40) | Sallent › Bages | 71 |
| Forêt de Sant Julià de Cerdanyola (3) | Sant Julià de Cerdanyola › Berguedà | 71 |
| Forêt de Sant Quirze Safaja (14) | Sant Quirze Safaja › Moianès | 71 |
| Forêt de Fogars de la Selva (14) | Fogars de la Selva › la Selva (Barcelone) | 71 |
| Forêt de Sant Martí de Tous (27) | Sant Martí de Tous › Anoia | 71 |
| Forêt de Sant Julià de Vilatorta (8) | Sant Julià de Vilatorta › Osona (Barcelone) | 71 |
| Forêt de Casserres | Casserres › Berguedà | 70 |
| Forêt de Sant Mateu de Bages (30) | Sant Mateu de Bages › Bages | 70 |
| Forêt de Castellar de n'Hug (5) | Castellar de n'Hug › Berguedà | 70 |
| Forêt de Sant Vicenç de Torelló (3) | Sant Vicenç de Torelló › Osona (Barcelone) | 70 |
| Forêt de Rupit i Pruit (17) | Rupit i Pruit › Osona (Barcelone) | 70 |
| Forêt de Bagà (12) | Bagà › Berguedà | 70 |
| Forêt de el Pont de Vilomara i Rocafort (10) | el Pont de Vilomara i Rocafort › Bages | 70 |
| Forêt de Cercs (40) | Cercs › Berguedà | 70 |
| Forêt de la Quar (46) | la Quar › Berguedà | 70 |
| Forêt de Sant Sadurní d'Osormort (48) | Sant Sadurní d'Osormort › Osona (Barcelone) | 70 |
| Forêt de Moià (2) | Moià › Moianès | 69 |
| Forêt de Castellcir | Castellcir › Moianès | 69 |
| Forêt de Sant Sadurní d'Osormort (9) | Sant Sadurní d'Osormort › Osona (Barcelone) | 69 |
| Forêt de el Brull (7) | el Brull › Osona (Barcelone) | 69 |
| Forêt de Castellar de n'Hug (7) | Castellar de n'Hug › Berguedà | 69 |
| Forêt de Oristà (109) | Oristà › Lluçanès | 69 |
| Forêt de Borredà (17) | Borredà › Berguedà | 69 |
| Forêt de Olèrdola (68) | Olèrdola › Alt Penedès | 69 |
| Forêt de Bigues i Riells del Fai (14) | Bigues i Riells del Fai › Vallès Oriental | 69 |
| Forêt de Sant Martí de Centelles (76) | Sant Martí de Centelles › Osona (Barcelone) | 69 |
| Forêt de Lluçà (89) | Lluçà › Lluçanès | 69 |
| Forêt de Taradell (22) | Taradell › Osona (Barcelone) | 69 |
| Forêt de Sant Bartomeu del Grau | Sant Bartomeu del Grau › Osona (Barcelone) | 68 |
| Forêt de Jorba (2) | Jorba › Anoia | 68 |
| Forêt de Òdena (12) | Òdena › Anoia | 68 |
| Forêt de el Brull (6) | el Brull › Osona (Barcelone) | 68 |
| Forêt de Seva (10) | Seva › Osona (Barcelone) | 68 |
| Forêt de Bagà (16) | Bagà › Berguedà | 68 |
| Forêt de Santa Maria de Merlès (16) | Santa Maria de Merlès › Berguedà | 68 |
| Forêt de Fogars de la Selva (29) | Fogars de la Selva › la Selva (Barcelone) | 68 |
| Forêt de Vilanova de Sau (33) | Vilanova de Sau › Osona (Barcelone) | 67 |
| Forêt de Avinyó (62) | Avinyó › Bages | 67 |
| Forêt de Rubió | Rubió › Anoia | 66 |
| Forêt de Avinyonet del Penedès (54) | Avinyonet del Penedès › Alt Penedès | 66 |
| Forêt de Cercs (4) | Cercs › Berguedà | 66 |
| Forêt de Súria (6) | Súria › Bages | 66 |
| Forêt de Sora (24) | Sora › Osona (Barcelone) | 66 |
| Forêt de Orís (8) | Orís › Osona (Barcelone) | 66 |
| Forêt de Sant Pere Sallavinera (24) | Sant Pere Sallavinera › Anoia | 66 |
| Forêt de Tona (2) | Tona › Osona (Barcelone) | 66 |
| Forêt de Sant Martí Sarroca (37) | Castellví de la Marca › Alt Penedès | 66 |
| Forêt de Cabrera d'Anoia (11) | Cabrera d'Anoia › Anoia | 66 |
| Forêt de Lluçà (86) | Lluçà › Lluçanès | 66 |
| Forêt de Sant Celoni (40) | Sant Celoni › Vallès Oriental | 66 |
| Forêt de Calders (77) | Calders › Moianès | 66 |
| Forêt de Sant Iscle de Vallalta (3) | Sant Iscle de Vallalta › Maresme | 65 |
| Forêt de Sant Celoni (6) | Sant Celoni › Vallès Oriental | 65 |
| Forêt de l'Esquirol (44) | l'Esquirol › Osona (Barcelone) | 65 |
| Forêt de Tagamanent (8) | Tagamanent › Vallès Oriental | 65 |
| Forêt de Guardiola de Berguedà (15) | Guardiola de Berguedà › Berguedà | 65 |
| Forêt de Santa Maria de Besora (11) | Santa Maria de Besora › Osona (Barcelone) | 65 |
| Bois de Molins de Rei (6) | Molins de Rei › Baix Llobregat | 65 |
| Forêt de Olivella (125) | Olivella › Garraf | 65 |
| Forêt de Santa Maria d'Oló (58) | Santa Maria d'Oló › Moianès | 65 |
| Forêt de Montmajor (137) | Montmajor › Berguedà | 65 |
| Forêt de Vilanova de Sau (57) | Vilanova de Sau › Osona (Barcelone) | 65 |
| Forêt de Tavertet (2) | Tavertet › Osona (Barcelone) | 64 |
| Forêt de Tavertet (5) | Tavertet › Osona (Barcelone) | 64 |
| Forêt de el Brull (14) | el Brull › Osona (Barcelone) | 64 |
| Forêt de Santa Maria de Miralles (3) | Santa Maria de Miralles › Anoia | 64 |
| Forêt de el Bruc (26) | el Bruc › Anoia | 64 |
| Forêt de Avià (43) | Avià › Berguedà | 64 |
| Forêt de Santa Maria d'Oló (61) | Santa Maria d'Oló › Moianès | 64 |
| Forêt de Viver i Serrateix (121) | Viver i Serrateix › Berguedà | 64 |
| Forêt de Sant Martí de Tous (3) | Sant Martí de Tous › Anoia | 63 |
| Forêt de Sant Pere de Torelló (5) | Sant Pere de Torelló › Osona (Barcelone) | 63 |
| Forêt de el Bruc (5) | el Bruc › Anoia | 63 |
| Forêt de Fígols (7) | Fígols › Berguedà | 63 |
| Forêt de Rajadell (49) | Rajadell › Bages | 63 |
| Forêt de Cardona (59) | Cardona › Bages | 63 |
| Forêt de les Franqueses del Vallès (50) | les Franqueses del Vallès › Vallès Oriental | 63 |
| Forêt de Borredà (60) | Borredà › Berguedà | 63 |
| Forêt de Sant Celoni (47) | Sant Celoni › Vallès Oriental | 63 |
| Forêt de Orís (4) | Orís › Osona (Barcelone) | 62 |
| Forêt de Alpens (12) | Alpens › Lluçanès | 62 |
| Forêt de el Bruc (8) | el Bruc › Anoia | 62 |
| Forêt de Rajadell (16) | Rajadell › Bages | 62 |
| Forêt de Terrassa (67) | Terrassa › Vallès Occidental | 62 |
| Forêt de Avinyó (46) | Avinyó › Bages | 62 |
| Forêt de Viver i Serrateix (39) | Viver i Serrateix › Berguedà | 62 |
| Forêt de Santa Maria de Merlès (13) | Santa Maria de Merlès › Berguedà | 62 |
| Forêt de Navàs (146) | Navàs › Bages | 62 |
| Forêt de Santa Maria de Merlès (102) | Santa Maria de Merlès › Berguedà | 62 |
| Forêt de Taradell (12) | Taradell › Osona (Barcelone) | 62 |
| Forêt de Balenyà (8) | Balenyà › Osona (Barcelone) | 62 |
| Forêt de Pineda de Mar | Pineda de Mar › Maresme | 62 |
| Forêt de Sant Julià de Vilatorta (2) | Sant Julià de Vilatorta › Osona (Barcelone) | 62 |
| Bois de Argentona (55) | Argentona › Maresme | 62 |
| Forêt de Olèrdola (3) | Olèrdola › Alt Penedès | 61 |
| Forêt de Rubió (2) | Rubió › Anoia | 61 |
| Forêt de Rubí (59) | Rubí › Vallès Occidental | 61 |
| Forêt de Gavà (62) | Castelldefels › Baix Llobregat | 61 |
| Forêt de Talamanca (19) | Talamanca › Bages | 61 |
| Forêt de l'Espunyola (74) | l'Espunyola › Berguedà | 61 |
| Forêt de Montmajor (119) | Montmajor › Berguedà | 61 |
| Forêt de Dosrius (18) | Dosrius › Maresme | 61 |
| Forêt de Sant Sadurní d'Osormort (24) | Sant Sadurní d'Osormort › Osona (Barcelone) | 61 |
| Forêt de Pontons (19) | Pontons › Alt Penedès | 61 |
| Forêt de Tavertet (36) | Tavertet › Osona (Barcelone) | 61 |
| Forêt de Vilanova de Sau (2) | Vilanova de Sau › Osona (Barcelone) | 60 |
| Forêt de Sant Fost de Campsentelles (2) | Sant Fost de Campsentelles › Vallès Oriental | 60 |
| Forêt de les Masies de Roda (2) | les Masies de Roda › Osona (Barcelone) | 60 |
| Forêt de la Nou de Berguedà (4) | la Nou de Berguedà › Berguedà | 60 |
| Forêt de la Pobla de Lillet (9) | la Pobla de Lillet › Berguedà | 60 |
| Forêt de Moià (22) | Moià › Moianès | 60 |
| Forêt de el Bruc (38) | el Bruc › Anoia | 60 |
| Forêt de l'Espunyola (57) | l'Espunyola › Berguedà | 60 |
| Bois de Sant Just Desvern (3) | Sant Just Desvern › Baix Llobregat | 60 |
| Forêt de Torrelles de Foix (6) | Torrelles de Foix › Alt Penedès | 60 |
| Forêt de Aguilar de Segarra (3) | Aguilar de Segarra › Bages | 59 |
| Forêt de Begues (29) | Begues › Baix Llobregat | 59 |
| Forêt de Sitges (17) | Sitges › Garraf | 59 |
| Forêt de Rajadell (30) | Rajadell › Bages | 59 |
| Forêt de Moià (33) | Moià › Moianès | 59 |
| Forêt de Rajadell (43) | Rajadell › Bages | 59 |
| Forêt de Viver i Serrateix (48) | Viver i Serrateix › Berguedà | 59 |
| Forêt de Moià (40) | Moià › Moianès | 59 |
| Forêt de Sant Pere de Vilamajor (88) | Sant Pere de Vilamajor › Vallès Oriental | 59 |
| Forêt de Cardona (104) | Cardona › Bages | 59 |
| Forêt de Sallent (121) | Sallent › Bages | 59 |
| Forêt de l'Esquirol (12) | l'Esquirol › Osona (Barcelone) | 58 |
| Forêt de Rupit i Pruit (14) | Rupit i Pruit › Osona (Barcelone) | 58 |
| Forêt de Montmajor (37) | Montmajor › Berguedà | 58 |
| Forêt de Sallent (57) | Sallent › Bages | 58 |
| Forêt de Sant Salvador de Guardiola (61) | Sant Salvador de Guardiola › Bages | 58 |
| Forêt de Navàs (74) | Navàs › Bages | 58 |
| Forêt de Gurb (19) | Gurb › Osona (Barcelone) | 58 |
| Forêt de Jorba (23) | Jorba › Anoia | 58 |
| Forêt de Vilanova de Sau (40) | Vilanova de Sau › Osona (Barcelone) | 58 |
| Forêt de Fogars de la Selva (25) | Fogars de la Selva › la Selva (Barcelone) | 58 |
| Bois de Argentona (53) | Argentona › Maresme | 58 |
| Forêt de Caldes de Montbui (23) | Caldes de Montbui › Vallès Oriental | 58 |
| Forêt de Palafolls | Palafolls › Maresme | 57 |
| Forêt de Sant Llorenç d'Hortons (3) | Sant Llorenç d'Hortons › Alt Penedès | 57 |
| Forêt de la Nou de Berguedà (11) | la Nou de Berguedà › Berguedà | 57 |
| Forêt de Casserres (18) | Casserres › Berguedà | 57 |
| Bois de Sant Cugat del Vallès (114) | Sant Cugat del Vallès › Vallès Occidental | 57 |
| Forêt de Muntanyola (16) | Muntanyola › Osona (Barcelone) | 57 |
| Forêt de Bigues i Riells del Fai (17) | Bigues i Riells del Fai › Vallès Oriental | 57 |
| Forêt de Castellfollit de Riubregós | Castellfollit de Riubregós › Anoia | 56 |
| Forêt de Montmajor (123) | Montmajor › Berguedà | 56 |
| Forêt de Tordera (110) | Tordera › Maresme | 56 |
| Forêt de Sant Sadurní d'Osormort (52) | Sant Sadurní d'Osormort › Osona (Barcelone) | 56 |
| Forêt de Calonge de Segarra (5) | Calonge de Segarra › Anoia | 55 |
| Forêt de Copons (3) | Copons › Anoia | 55 |
| Forêt de Aguilar de Segarra (20) | Aguilar de Segarra › Bages | 55 |
| Forêt de Castellterçol (15) | Castellterçol › Moianès | 55 |
| Forêt de Fonollosa (98) | Fonollosa › Bages | 55 |
| Forêt de Rajadell (51) | Rajadell › Bages | 55 |
| Forêt de Santa Maria de Merlès (14) | Santa Maria de Merlès › Berguedà | 55 |
| Forêt de Begues (76) | Begues › Baix Llobregat | 55 |
| Forêt de Gisclareny (16) | Gisclareny › Berguedà | 55 |
| Forêt de les Franqueses del Vallès (51) | les Franqueses del Vallès › Vallès Oriental | 55 |
| Forêt de Tagamanent (14) | Tagamanent › Vallès Oriental | 55 |
| Forêt de Muntanyola (25) | Muntanyola › Osona (Barcelone) | 55 |
| Forêt de Lluçà (43) | Lluçà › Lluçanès | 55 |
| Forêt de Pontons (9) | Pontons › Alt Penedès | 55 |
| Forêt de Guardiola de Berguedà (132) | Guardiola de Berguedà › Berguedà | 55 |
| Forêt de Sora | Sora › Osona (Barcelone) | 54 |
| Forêt de Perafita (2) | Perafita › Lluçanès | 54 |
| Forêt de Calonge de Segarra (7) | Calonge de Segarra › Anoia | 54 |
| Forêt de Font-rubí (7) | Font-rubí › Alt Penedès | 54 |
| Forêt de Santa Maria d'Oló (28) | Santa Maria d'Oló › Moianès | 54 |
| Forêt de Castellbell i el Vilar (34) | Castellbell i el Vilar › Bages | 54 |
| Forêt de Santa Maria de Besora (8) | Santa Maria de Besora › Osona (Barcelone) | 54 |
| Forêt de Aguilar de Segarra (33) | Aguilar de Segarra › Bages | 54 |
| Forêt de Vilanova i la Geltrú (39) | Vilanova i la Geltrú › Garraf | 54 |
| Bosc de Can Bosquerons | Martorelles › Vallès Oriental | 54 |
| Forêt de Piera (65) | Piera › Anoia | 54 |
| Forêt de Muntanyola (4) | Muntanyola › Osona (Barcelone) | 53 |
| Forêt de Tagamanent (12) | Tagamanent › Vallès Oriental | 53 |
| Forêt de Vilanova de Sau (36) | Vilanova de Sau › Osona (Barcelone) | 53 |
| Forêt de les Masies de Roda (6) | les Masies de Roda › Osona (Barcelone) | 53 |
| Forêt de Sagàs (7) | Sagàs › Berguedà | 53 |
| Forêt de Sant Pere de Ribes (95) | Sant Pere de Ribes › Garraf | 53 |
| Forêt de Sant Sadurní d'Osormort (19) | Sant Sadurní d'Osormort › Osona (Barcelone) | 52 |
| Forêt de Matadepera (2) | Terrassa › Vallès Occidental | 52 |
| Bois de Argentona (7) | Argentona › Maresme | 52 |
| Bois de Copons (2) | Copons › Anoia | 52 |
| Forêt de Avià (16) | Avià › Berguedà | 52 |
| Forêt de Montmajor (59) | Montmajor › Berguedà | 52 |
| Forêt de Sallent (77) | Sallent › Bages | 52 |
| Forêt de el Pont de Vilomara i Rocafort (15) | el Pont de Vilomara i Rocafort › Bages | 52 |
| Forêt de Gavà (74) | Gavà › Baix Llobregat | 52 |
| Forêt de Avinyó (86) | Avinyó › Bages | 52 |
| Forêt de l'Espunyola (54) | l'Espunyola › Berguedà | 52 |
| Bois de Sant Cugat del Vallès (118) | Sant Cugat del Vallès › Vallès Occidental | 52 |
| Bois de Barcelona (106) | Barcelona › Barcelonès | 52 |
| Forêt de Muntanyola (22) | Muntanyola › Osona (Barcelone) | 52 |
| Forêt de Dosrius (15) | Dosrius › Maresme | 52 |
| Forêt de Dosrius (20) | Dosrius › Maresme | 52 |
| Forêt de Collsuspina (8) | Collsuspina › Moianès | 52 |
| El bosc Encantat | la Roca del Vallès › Vallès Oriental | 52 |
| Forêt de Tavertet (48) | Tavertet › Osona (Barcelone) | 52 |
| Forêt de Arenys de Munt (14) | Arenys de Munt › Maresme | 52 |
| Forêt de Fogars de la Selva (37) | Fogars de la Selva › la Selva (Barcelone) | 52 |
| Forêt de Fogars de la Selva | Fogars de la Selva › la Selva (Barcelone) | 51 |
| Forêt de Sora (6) | Sora › Osona (Barcelone) | 51 |
| Forêt de Sant Pere de Torelló (8) | Sant Pere de Torelló › Osona (Barcelone) | 51 |
| Bois de Vallromanes | Vallromanes › Maresme | 51 |
| Forêt de Casserres (4) | Casserres › Berguedà | 51 |
| Forêt de Aiguafreda (6) | Aiguafreda › Osona (Barcelone) | 51 |
| Forêt de Cànoves i Samalús (25) | Cànoves i Samalús › Vallès Oriental | 51 |
| Forêt de Olvan (4) | Olvan › Berguedà | 51 |
| Forêt de Sallent (42) | Sallent › Bages | 51 |
| Forêt de Sant Salvador de Guardiola (62) | Sant Salvador de Guardiola › Bages | 51 |
| Forêt de els Hostalets de Pierola (26) | els Hostalets de Pierola › Anoia | 51 |
| Forêt de Montseny (9) | Montseny › Vallès Oriental | 51 |
| Forêt de Sant Mateu de Bages (56) | Sant Mateu de Bages › Bages | 51 |
| Forêt de Bigues i Riells del Fai (39) | Bigues i Riells del Fai › Vallès Oriental | 51 |
| Forêt de Castellar de n'Hug (23) | Castellar de n'Hug › Berguedà | 51 |
| Forêt de Montmajor (136) | Montmajor › Berguedà | 51 |
| Forêt de Olesa de Bonesvalls | Olesa de Bonesvalls › Alt Penedès | 50 |
| Forêt de els Prats de Rei (3) | els Prats de Rei › Anoia | 50 |
| Forêt de Olvan (3) | Olvan › Berguedà | 50 |
| Forêt de Balsareny (28) | Balsareny › Bages | 50 |
| Forêt de Fígols (6) | Fígols › Berguedà | 50 |
| Forêt de Vallirana (24) | Vallirana › Baix Llobregat | 50 |
| Forêt de l'Espunyola (32) | l'Espunyola › Berguedà | 50 |
| Forêt de Corbera de Llobregat (26) | Corbera de Llobregat › Baix Llobregat | 50 |
| Forêt de el Bruc (25) | el Bruc › Anoia | 50 |
| Forêt de la Garriga (40) | la Garriga › Vallès Oriental | 50 |
| Forêt de Cercs (51) | Cercs › Berguedà | 50 |
| Forêt de Sant Mateu de Bages (41) | Sant Mateu de Bages › Bages | 50 |
| Forêt de Begues (60) | Begues › Baix Llobregat | 50 |
| Forêt de Navàs (143) | Navàs › Bages | 50 |
| Forêt de Tordera (72) | Tordera › Maresme | 50 |
| Bois de Vilanova del Vallès (16) | Vilanova del Vallès › Vallès Oriental | 50 |
| Forêt de Carme (10) | Carme › Anoia | 50 |
| Forêt de Sant Cugat del Vallès (160) | Sant Cugat del Vallès › Vallès Occidental | 50 |
| Forêt de l'Esquirol | l'Esquirol › Osona (Barcelone) | 49 |
| Forêt de Sant Llorenç d'Hortons (2) | Sant Llorenç d'Hortons › Alt Penedès | 49 |
| Forêt de Casserres (11) | Casserres › Berguedà | 49 |
| Forêt de Santa Maria de Merlès (18) | Santa Maria de Merlès › Berguedà | 49 |
| Forêt de Seva (20) | Seva › Osona (Barcelone) | 49 |
| Forêt de Sant Sadurní d'Osormort (27) | Sant Sadurní d'Osormort › Osona (Barcelone) | 49 |
| Forêt de Bellprat (6) | Bellprat › Anoia | 48 |
| Forêt de Sant Pere de Vilamajor (71) | Sant Pere de Vilamajor › Vallès Oriental | 48 |
| Forêt de Montseny (4) | Montseny › Vallès Oriental | 48 |
| Forêt de Berga (28) | Berga › Berguedà | 48 |
| Forêt de Olesa de Montserrat (14) | Olesa de Montserrat › Baix Llobregat | 48 |
| Forêt de Sant Climent de Llobregat (16) | Sant Climent de Llobregat › Baix Llobregat | 48 |
| Forêt de Navàs (94) | Navàs › Bages | 48 |
| Forêt de Montclar (27) | Montclar › Berguedà | 48 |
| Forêt de Sant Martí de Centelles (62) | Sant Martí de Centelles › Osona (Barcelone) | 48 |
| Forêt de Bigues i Riells del Fai (15) | Bigues i Riells del Fai › Vallès Oriental | 48 |
| Forêt de Torrelles de Foix (7) | Torrelles de Foix › Alt Penedès | 48 |
| Forêt de Lluçà (66) | Lluçà › Lluçanès | 48 |
| Forêt de Palafolls (27) | Palafolls › Maresme | 48 |
| Forêt de Sant Celoni (69) | Sant Celoni › Vallès Oriental | 48 |
| Forêt de Sant Mateu de Bages (140) | Sant Mateu de Bages › Bages | 48 |
| Forêt de Alpens (6) | Alpens › Lluçanès | 47 |
| Forêt de Tordera (12) | Tordera › Maresme | 47 |
| Bois de Dosrius | Dosrius › Maresme | 47 |
| Forêt de els Prats de Rei | els Prats de Rei › Anoia | 47 |
| Forêt de Copons (2) | els Prats de Rei › Anoia | 47 |
| Forêt de Berga (17) | Berga › Berguedà | 47 |
| Forêt de Navàs (46) | Navàs › Bages | 47 |
| Forêt de Monistrol de Calders (25) | Monistrol de Calders › Moianès | 47 |
| Forêt de Bagà (30) | Bagà › Berguedà | 47 |
| Forêt de els Hostalets de Pierola (20) | els Hostalets de Pierola › Anoia | 47 |
| Forêt de Cabrera d'Anoia (6) | Cabrera d'Anoia › Anoia | 47 |
| Forêt de Malgrat de Mar (4) | Malgrat de Mar › Maresme | 47 |
| Forêt de Gurb (60) | Gurb › Osona (Barcelone) | 47 |
| Forêt de Oristà (171) | Oristà › Lluçanès | 47 |
| Forêt de Gurb (2) | Gurb › Osona (Barcelone) | 46 |
| Forêt de els Hostalets de Pierola (8) | els Hostalets de Pierola › Anoia | 46 |
| Forêt de Copons (4) | Copons › Anoia | 46 |
| Bosc dels Giberts | Torrelles de Foix › Alt Penedès | 46 |
| Forêt de Sant Bartomeu del Grau (9) | Sant Bartomeu del Grau › Osona (Barcelone) | 46 |
| Forêt de Fonollosa (78) | Fonollosa › Bages | 46 |
| Forêt de Masquefa (12) | Masquefa › Anoia | 46 |
| Forêt de Berga (19) | Berga › Berguedà | 46 |
| Forêt de Viver i Serrateix (62) | Viver i Serrateix › Berguedà | 46 |
| Forêt de Castellet i la Gornal (82) | Castellet i la Gornal › Alt Penedès | 46 |
| Forêt de Santa Eulàlia de Riuprimer (7) | Muntanyola › Osona (Barcelone) | 46 |
| Forêt de Sant Martí de Centelles (66) | Sant Martí de Centelles › Osona (Barcelone) | 46 |
| Forêt de Borredà (73) | Borredà › Berguedà | 46 |
| Forêt de la Quar (43) | la Quar › Berguedà | 46 |
| Forêt de Gisclareny (55) | Gisclareny › Berguedà | 46 |
| Forêt de Pontons (10) | Pontons › Alt Penedès | 46 |
| Forêt de Lluçà (60) | Lluçà › Lluçanès | 46 |
| Forêt de Arenys de Munt (11) | Arenys de Munt › Maresme | 46 |
| Bois de Palau-solità i Plegamans | Palau-solità i Plegamans › Vallès Occidental | 45 |
| Bois de Vilanova del Vallès | Vilanova del Vallès › Vallès Oriental | 45 |
| Forêt de Gurb (12) | Gurb › Osona (Barcelone) | 45 |
| Forêt de Calders (45) | Calders › Moianès | 45 |
| Forêt de Viver i Serrateix (40) | Viver i Serrateix › Berguedà | 45 |
| Forêt de Avià (39) | Avià › Berguedà | 45 |
| Forêt de Castellfollit de Riubregós (9) | Castellfollit de Riubregós › Anoia | 45 |
| Forêt de la Pobla de Lillet (49) | la Pobla de Lillet › Berguedà | 45 |
| Bois de Llinars del Vallès (37) | Llinars del Vallès › Vallès Oriental | 45 |
| Forêt de Òdena (73) | Òdena › Anoia | 45 |
| Forêt de Castellbisbal (49) | Castellbisbal › Vallès Occidental | 45 |
| Forêt de Gualba (10) | Gualba › Vallès Oriental | 45 |
| Forêt de Sant Pol de Mar | Sant Pol de Mar › Maresme | 44 |
| Forêt de Torrelavit | Torrelavit › Alt Penedès | 44 |
| Forêt de Rupit i Pruit (13) | Rupit i Pruit › Osona (Barcelone) | 44 |
| Bois de Dosrius (13) | Dosrius › Maresme | 44 |
| Forêt de Viladecavalls (6) | Viladecavalls › Vallès Occidental | 44 |
| Forêt de Seva (17) | Seva › Osona (Barcelone) | 44 |
| Forêt de Capolat (13) | Capolat › Berguedà | 44 |
| Forêt de Artés (17) | Artés › Bages | 44 |
| Forêt de Santa Maria de Palautordera (17) | Santa Maria de Palautordera › Vallès Oriental | 44 |
| Forêt de Montmajor (92) | Montmajor › Berguedà | 44 |
| Forêt de Santa Eulàlia de Ronçana (7) | Santa Eulàlia de Ronçana › Vallès Oriental | 44 |
| Forêt de Santa Maria de Merlès (71) | Santa Maria de Merlès › Berguedà | 44 |
| Forêt de Sagàs (38) | Sagàs › Berguedà | 44 |
| Forêt de Sant Feliu de Codines (9) | Sant Feliu de Codines › Vallès Oriental | 44 |
| Forêt de Vic (32) | Vic › Osona (Barcelone) | 44 |
| Forêt de Oristà (144) | Oristà › Lluçanès | 44 |
| Forêt de Castellar del Riu (27) | Castellar del Riu › Berguedà | 44 |
| Bois de Cerdanyola del Vallès (15) | Cerdanyola del Vallès › Vallès Occidental | 44 |
| Forêt de Lluçà (57) | Lluçà › Lluçanès | 44 |
| Forêt de Sant Sadurní d'Osormort (35) | Sant Sadurní d'Osormort › Osona (Barcelone) | 44 |
| Forêt de Sant Andreu de Llavaneres (3) | Sant Andreu de Llavaneres › Maresme | 43 |
| Forêt de Gurb | Gurb › Osona (Barcelone) | 43 |
| Forêt de Santa Maria de Besora (4) | Santa Maria de Besora › Osona (Barcelone) | 43 |
| Forêt de Guardiola de Berguedà (12) | Guardiola de Berguedà › Berguedà | 43 |
| Forêt de Cercs (23) | Cercs › Berguedà | 43 |
| Forêt de Corbera de Llobregat (16) | Corbera de Llobregat › Baix Llobregat | 43 |
| Forêt de Sant Esteve de Palautordera (6) | Sant Esteve de Palautordera › Vallès Oriental | 43 |
| Forêt de Granera (19) | Granera › Moianès | 43 |
| Forêt de Borredà (21) | Borredà › Berguedà | 43 |
| Forêt de Sant Quirze Safaja (13) | Sant Quirze Safaja › Moianès | 43 |
| Forêt de Sant Mateu de Bages (89) | Sant Mateu de Bages › Bages | 43 |
| Forêt de la Quar (29) | la Quar › Berguedà | 43 |
| Forêt de Gisclareny (32) | Gisclareny › Berguedà | 43 |
| Forêt de Pontons (17) | Pontons › Alt Penedès | 43 |
| Forêt de Cabrera d'Anoia (10) | Cabrera d'Anoia › Anoia | 43 |
| Forêt de Sora (9) | Sora › Osona (Barcelone) | 42 |
| Forêt de Calonge de Segarra (6) | Calonge de Segarra › Anoia | 42 |
| Forêt de Sagàs (6) | Sagàs › Berguedà | 42 |
| Forêt de Castellcir (3) | Castellcir › Moianès | 42 |
| Forêt de Fonollosa (92) | Fonollosa › Bages | 42 |
| Forêt de el Bruc (24) | el Bruc › Anoia | 42 |
| Forêt de les Franqueses del Vallès (48) | les Franqueses del Vallès › Vallès Oriental | 42 |
| Forêt de Talamanca (9) | Talamanca › Bages | 42 |
| Forêt de Navàs (93) | Navàs › Bages | 42 |
| Forêt de Puig-reig (76) | Puig-reig › Berguedà | 42 |
| Forêt de l'Espunyola (70) | l'Espunyola › Berguedà | 42 |
| Forêt de Viver i Serrateix (72) | Viver i Serrateix › Berguedà | 42 |
| Forêt de Borredà (52) | Borredà › Berguedà | 42 |
| Forêt de l'Estany (4) | l'Estany › Moianès | 42 |
| Forêt de Sant Antoni de Vilamajor (43) | Sant Antoni de Vilamajor › Vallès Oriental | 42 |
| Forêt de la Pobla de Lillet (42) | la Pobla de Lillet › Berguedà | 42 |
| Forêt de Torrelles de Foix (12) | Torrelles de Foix › Alt Penedès | 42 |
| Forêt de Rajadell (7) | Rajadell › Bages | 41 |
| Forêt de Fonollosa (85) | Fonollosa › Bages | 41 |
| Forêt de Seva (14) | Seva › Osona (Barcelone) | 41 |
| Forêt de Moià (31) | Moià › Moianès | 41 |
| Forêt de Sitges (61) | Sitges › Garraf | 41 |
| Forêt de Moià (37) | Moià › Moianès | 41 |
| Forêt de Santa Maria de Palautordera (18) | Santa Maria de Palautordera › Vallès Oriental | 41 |
| Forêt de Sant Jaume de Frontanyà (13) | Sant Jaume de Frontanyà › Berguedà | 41 |
| Forêt de l'Espunyola (60) | l'Espunyola › Berguedà | 41 |
| Forêt de Navàs (102) | Navàs › Bages | 41 |
| Forêt de Canyelles (22) | Canyelles › Garraf | 41 |
| Forêt de Castellar del Vallès (20) | Castellar del Vallès › Vallès Occidental | 41 |
| Forêt de els Hostalets de Pierola (25) | els Hostalets de Pierola › Anoia | 41 |
| Forêt de Vallgorguina (5) | Vallgorguina › Vallès Oriental | 41 |
| Forêt de Gallifa (4) | Gallifa › Vallès Occidental | 41 |
| Forêt de Castellar del Riu (37) | Castellar del Riu › Berguedà | 41 |
| Forêt de Borredà (120) | Borredà › Berguedà | 41 |
| Forêt de Santa Maria de Besora (22) | Santa Maria de Besora › Osona (Barcelone) | 41 |
| Forêt de Sant Bartomeu del Grau (18) | Sant Bartomeu del Grau › Osona (Barcelone) | 41 |
| Forêt de Borredà (131) | Borredà › Berguedà | 41 |
| Forêt de Castellcir (12) | Castellcir › Moianès | 41 |
| Forêt de Pujalt (2) | Pujalt › Anoia | 40 |
| Forêt de Santa Maria d'Oló (4) | Santa Maria d'Oló › Moianès | 40 |
| Forêt de Muntanyola (8) | Muntanyola › Osona (Barcelone) | 40 |
| Forêt de Fonollosa (86) | Fonollosa › Bages | 40 |
| Forêt de Orís (6) | Orís › Osona (Barcelone) | 40 |
| Forêt de Avinyó (48) | Avinyó › Bages | 40 |
| Forêt de Sant Feliu Sasserra (8) | Sant Feliu Sasserra › Bages | 40 |
| Forêt de Premià de Dalt (6) | Premià de Dalt › Maresme | 40 |
| Forêt de Castellar del Riu (16) | Castellar del Riu › Berguedà | 40 |
| Forêt de Castellolí (28) | Castellolí › Anoia | 40 |
| Forêt de Olesa de Bonesvalls (36) | Olesa de Bonesvalls › Alt Penedès | 40 |
| Forêt de Sant Bartomeu del Grau (12) | Sant Bartomeu del Grau › Osona (Barcelone) | 40 |
| Camps de la Vall | Sant Martí de Centelles › Osona (Barcelone) | 40 |
| Forêt de l'Estany (8) | l'Estany › Moianès | 40 |
| Forêt de Sant Mateu de Bages (90) | Sant Mateu de Bages › Bages | 40 |
| Forêt de Dosrius (13) | Dosrius › Maresme | 40 |
| Forêt de Gualba (6) | Gualba › Vallès Oriental | 40 |
| Forêt de Pontons (11) | Pontons › Alt Penedès | 40 |
| Forêt de Cardona (107) | Cardona › Bages | 40 |
| Forêt de Mediona (94) | Mediona › Alt Penedès | 40 |
| Forêt de Torrelles de Foix (11) | Torrelles de Foix › Alt Penedès | 40 |
| Forêt de Tordera (101) | Tordera › Maresme | 40 |
| Forêt de Calella (8) | Calella › Maresme | 40 |
| Forêt de Pineda de Mar (3) | Pineda de Mar › Maresme | 40 |
| Forêt de Sallent (118) | Sallent › Bages | 40 |
| Forêt de Sant Sadurní d'Osormort (43) | Sant Sadurní d'Osormort › Osona (Barcelone) | 40 |
| Forêt de Santa Maria de Besora | Santa Maria de Besora › Osona (Barcelone) | 39 |
| Forêt de Oristà (2) | Oristà › Lluçanès | 39 |
| Forêt de l'Esquirol (13) | l'Esquirol › Osona (Barcelone) | 39 |
| Forêt de Sant Martí de Tous (9) | Sant Martí de Tous › Anoia | 39 |
| Forêt de Rajadell (6) | Rajadell › Bages | 39 |
| Forêt de Fonollosa (84) | Rajadell › Bages | 39 |
| Forêt de Vilanova de Sau (28) | Vilanova de Sau › Osona (Barcelone) | 39 |
| Forêt de Vilanova de Sau (31) | Vilanova de Sau › Osona (Barcelone) | 39 |
| Forêt de les Masies de Roda (4) | les Masies de Roda › Osona (Barcelone) | 39 |
| Forêt de Bagà (3) | Bagà › Berguedà | 39 |
| Forêt de Monistrol de Montserrat (6) | Monistrol de Montserrat › Bages | 39 |
| Forêt de Aguilar de Segarra (22) | Aguilar de Segarra › Bages | 39 |
| Forêt de Manresa (96) | Manresa › Bages | 39 |
| Forêt de Montmajor (56) | Montmajor › Berguedà | 39 |
| Forêt de Oristà (106) | Oristà › Lluçanès | 39 |
| Bois de Abrera | Abrera › Baix Llobregat | 39 |
| Forêt de Castell de l'Areny (12) | Castell de l'Areny › Berguedà | 39 |
| Forêt de Montmajor (100) | Montmajor › Berguedà | 39 |
| Forêt de Sentmenat (10) | Sentmenat › Vallès Occidental | 39 |
| Forêt de Navàs (149) | Navàs › Bages | 39 |
| Forêt de Santa Maria d'Oló (46) | Santa Maria d'Oló › Moianès | 39 |
| Forêt de Borredà (50) | Borredà › Berguedà | 39 |
| Forêt de Balenyà (9) | Balenyà › Osona (Barcelone) | 39 |
| Forêt de Saldes (52) | Saldes › Berguedà | 39 |
| Forêt de Guardiola de Berguedà (75) | Bagà › Berguedà | 39 |
| Forêt de Guardiola de Berguedà (98) | Guardiola de Berguedà › Berguedà | 39 |
| Forêt de Gisclareny (57) | Gisclareny › Berguedà | 39 |
| Forêt de Sora (29) | Sora › Osona (Barcelone) | 39 |
| Forêt de Sant Feliu Sasserra (38) | Sant Feliu Sasserra › Bages | 39 |
| Forêt de Sant Quirze Safaja (53) | Sant Quirze Safaja › Moianès | 39 |
| Forêt de Talamanca (42) | Navarcles › Bages | 39 |
| Forêt de Montmajor (2) | Montmajor › Berguedà | 38 |
| Forêt de Marganell (4) | Marganell › Bages | 38 |
| Forêt de Berga (32) | Berga › Berguedà | 38 |
| Forêt de Calders (31) | Calders › Moianès | 38 |
| Forêt de Talamanca (17) | Talamanca › Bages | 38 |
| Forêt de Castellbisbal (19) | Castellbisbal › Vallès Occidental | 38 |
| Forêt de Navàs (57) | Navàs › Bages | 38 |
| Forêt de Montmajor (121) | Montmajor › Berguedà | 38 |
| Forêt de Gallifa (5) | Gallifa › Vallès Occidental | 38 |
| Forêt de Borredà (86) | Borredà › Berguedà | 38 |
| Forêt de la Quar (44) | Sagàs › Berguedà | 38 |
| Forêt de Borredà (104) | Borredà › Berguedà | 38 |
| Forêt de Sant Fost de Campsentelles (11) | Sant Fost de Campsentelles › Vallès Oriental | 38 |
| Forêt de Cabrera d'Anoia (36) | Cabrera d'Anoia › Anoia | 38 |
| Forêt de Tordera (106) | Tordera › Maresme | 38 |
| Forêt de Sallent (120) | Sallent › Bages | 38 |
| Forêt de Sant Mateu de Bages (139) | Sant Mateu de Bages › Bages | 38 |
| Forêt de Sant Climent de Llobregat (2) | Sant Climent de Llobregat › Baix Llobregat | 37 |
| Forêt de Sant Climent de Llobregat (5) | Sant Climent de Llobregat › Baix Llobregat | 37 |
| Forêt de Sant Sadurní d'Anoia (8) | Sant Sadurní d'Anoia › Alt Penedès | 37 |
| Forêt de Cabrera de Mar (2) | Cabrera de Mar › Maresme | 37 |
| Forêt de Guardiola de Berguedà (11) | Guardiola de Berguedà › Berguedà | 37 |
| Forêt de la Pobla de Claramunt (5) | la Pobla de Claramunt › Anoia | 37 |
| Forêt de Avinyó (17) | Avinyó › Bages | 37 |
| Forêt de Casserres (10) | Casserres › Berguedà | 37 |
| Forêt de l'Espunyola (46) | l'Espunyola › Berguedà | 37 |
| Forêt de Vallromanes (10) | Vallromanes › Vallès Oriental | 37 |
| Forêt de Mura (17) | Mura › Bages | 37 |
| Forêt de Calonge de Segarra (10) | Calonge de Segarra › Anoia | 37 |
| Forêt de Castellet i la Gornal (70) | Castellet i la Gornal › Alt Penedès | 37 |
| Forêt de Avinyonet del Penedès (57) | Avinyonet del Penedès › Alt Penedès | 37 |
| Forêt de Sant Jaume de Frontanyà (14) | Sant Jaume de Frontanyà › Berguedà | 37 |
| Forêt de Llinars del Vallès (74) | Llinars del Vallès › Vallès Oriental | 37 |
| Forêt de Guardiola de Berguedà (115) | Guardiola de Berguedà › Berguedà | 37 |
| Forêt de la Pobla de Lillet (41) | la Pobla de Lillet › Berguedà | 37 |
| Forêt de Sant Julià de Vilatorta | Sant Julià de Vilatorta › Osona (Barcelone) | 37 |
| Forêt de Pontons (14) | Pontons › Alt Penedès | 37 |
| Forêt de Torrelles de Llobregat (180) | Torrelles de Llobregat › Baix Llobregat | 37 |
| Forêt de Orís (2) | Orís › Osona (Barcelone) | 36 |
| Forêt de Alella | Alella › Maresme | 36 |
| Bois de Argentona (32) | Argentona › Maresme | 36 |
| Forêt de Aguilar de Segarra (14) | Aguilar de Segarra › Bages | 36 |
| Forêt de Castellar del Riu (11) | Castellar del Riu › Berguedà | 36 |
| Forêt de Balsareny (49) | Balsareny › Bages | 36 |
| Forêt de Monistrol de Montserrat (16) | Monistrol de Montserrat › Bages | 36 |
| Forêt de Rellinars (3) | Rellinars › Vallès Occidental | 36 |
| Forêt de Guardiola de Berguedà (36) | Guardiola de Berguedà › Berguedà | 36 |
| Forêt de Sant Salvador de Guardiola (46) | Sant Salvador de Guardiola › Bages | 36 |
| Forêt de Avinyó (88) | Avinyó › Bages | 36 |
| Forêt de Olesa de Montserrat (24) | Olesa de Montserrat › Baix Llobregat | 36 |
| Bois de Barcelona (107) | Barcelona › Barcelonès | 36 |
| Bois de Dosrius (14) | Dosrius › Maresme | 36 |
| Forêt de Sant Pere de Ribes (112) | Sant Pere de Ribes › Garraf | 36 |
| Forêt de Sant Jaume de Frontanyà (16) | Sant Jaume de Frontanyà › Berguedà | 36 |
| Forêt de Sant Mateu de Bages (81) | Sant Mateu de Bages › Bages | 36 |
| Forêt de Mataró (5) | Mataró › Maresme | 36 |
| Forêt de Tona (13) | Tona › Osona (Barcelone) | 36 |
| Forêt de Castellar del Riu (31) | Castellar del Riu › Berguedà | 36 |
| Forêt de Castellar del Riu (44) | Castellar del Riu › Berguedà | 36 |
| Forêt de Font-rubí (19) | Font-rubí › Alt Penedès | 36 |
| Forêt de Rupit i Pruit (38) | Rupit i Pruit › Osona (Barcelone) | 36 |
| Forêt de Sant Cebrià de Vallalta (5) | Sant Cebrià de Vallalta › Maresme | 36 |
| Forêt de Sant Vicenç de Montalt (4) | Sant Vicenç de Montalt › Maresme | 36 |
| Forêt de Tavèrnoles (7) | Tavèrnoles › Osona (Barcelone) | 36 |
| Forêt de el Pont de Vilomara i Rocafort (33) | el Pont de Vilomara i Rocafort › Bages | 36 |
| Forêt de Moià (4) | Moià › Moianès | 35 |
| Forêt de Campins (4) | Campins › Vallès Oriental | 35 |
| Forêt de Piera (5) | Piera › Anoia | 35 |
| Forêt de Arenys de Munt (4) | Arenys de Munt › Maresme | 35 |
| Forêt de la Garriga (37) | la Garriga › Vallès Oriental | 35 |
| Forêt de Talamanca (3) | Talamanca › Bages | 35 |
| Forêt de Sallent (31) | Sallent › Bages | 35 |
| Forêt de Santa Maria d'Oló (26) | Santa Maria d'Oló › Moianès | 35 |
| Forêt de l'Espunyola (49) | l'Espunyola › Berguedà | 35 |
| Forêt de Esparreguera (20) | Esparreguera › Baix Llobregat | 35 |
| Forêt de Santa Maria de Merlès (50) | Santa Maria de Merlès › Berguedà | 35 |
| Bois de Sant Feliu de Llobregat (3) | Sant Feliu de Llobregat › Baix Llobregat | 35 |
| Forêt de Sant Martí de Centelles (61) | Sant Martí de Centelles › Osona (Barcelone) | 35 |
| Forêt de Lluçà (11) | Lluçà › Lluçanès | 35 |
| Forêt de Gisclareny (25) | Gisclareny › Berguedà | 35 |
| Forêt de Cercs (52) | Cercs › Berguedà | 35 |
| Forêt de Borredà (103) | Borredà › Berguedà | 35 |
| Forêt de Torrelles de Llobregat (172) | Torrelles de Llobregat › Baix Llobregat | 35 |
| Forêt de la Llacuna (9) | la Llacuna › Anoia | 35 |
| Forêt de Piera (78) | Piera › Anoia | 35 |
| Forêt de Torrelles de Foix (3) | Torrelles de Foix › Alt Penedès | 35 |
| Forêt de Dosrius (37) | Dosrius › Maresme | 35 |
| Forêt de Castellnou de Bages (51) | Castellnou de Bages › Bages | 35 |
| Forêt de Bigues i Riells del Fai (40) | Bigues i Riells del Fai › Vallès Oriental | 35 |
| Forêt de Sant Quirze Safaja (56) | Sant Quirze Safaja › Moianès | 35 |
| Forêt de Olost | Olost › Lluçanès | 34 |
| Forêt de Santa Eulàlia de Ronçana | Santa Eulàlia de Ronçana › Vallès Oriental | 34 |
| Bois de Llinars del Vallès (17) | Llinars del Vallès › Vallès Oriental | 34 |
| Bois de Dosrius (8) | Dosrius › Maresme | 34 |
| Bois de Copons | Copons › Anoia | 34 |
| Bois de Copons (4) | Copons › Anoia | 34 |
| Forêt de Castellterçol (18) | Castellterçol › Moianès | 34 |
| Forêt de la Pobla de Lillet (6) | la Pobla de Lillet › Berguedà | 34 |
| Forêt de Gaià (38) | Gaià › Bages | 34 |
| Forêt de Olesa de Montserrat (22) | Olesa de Montserrat › Baix Llobregat | 34 |
| Forêt de Navàs (66) | Navàs › Bages | 34 |
| Forêt de Viver i Serrateix (28) | Viver i Serrateix › Berguedà | 34 |
| Forêt de Santa Maria de Merlès (62) | Santa Maria de Merlès › Berguedà | 34 |
| Forêt de Sant Antoni de Vilamajor (40) | Sant Antoni de Vilamajor › Vallès Oriental | 34 |
| Forêt de Muntanyola (18) | Muntanyola › Osona (Barcelone) | 34 |
| Forêt de Sant Martí de Centelles (57) | Sant Martí de Centelles › Osona (Barcelone) | 34 |
| Forêt de Aiguafreda (14) | Aiguafreda › Osona (Barcelone) | 34 |
| Forêt de Lluçà (8) | Lluçà › Lluçanès | 34 |
| Forêt de Santa Maria de Martorelles (2) | Santa Maria de Martorelles › Vallès Oriental | 34 |
| Forêt de Guardiola de Berguedà (120) | Guardiola de Berguedà › Berguedà | 34 |
| Forêt de Sant Cebrià de Vallalta (10) | Sant Cebrià de Vallalta › Maresme | 34 |
| Forêt de Arenys de Munt (23) | Arenys de Munt › Maresme | 34 |
| Forêt de Guardiola de Berguedà (144) | Guardiola de Berguedà › Berguedà | 34 |
| Forêt de Sant Sadurní d'Osormort (44) | Sant Sadurní d'Osormort › Osona (Barcelone) | 34 |
| Forêt de Gurb (61) | Gurb › Osona (Barcelone) | 34 |
| Forêt de Sant Quirze Safaja (55) | Sant Quirze Safaja › Moianès | 34 |
| Forêt de Sant Llorenç d'Hortons | Sant Llorenç d'Hortons › Alt Penedès | 33 |
| Forêt de Fogars de Montclús | Fogars de Montclús › Vallès Oriental | 33 |
| Forêt de Guardiola de Berguedà | Guardiola de Berguedà › Berguedà | 33 |
| Forêt de Seva (2) | Seva › Osona (Barcelone) | 33 |
| Bosc de Can Sabater | Canovelles › Vallès Oriental | 33 |
| Forêt de Olesa de Bonesvalls (32) | Olesa de Bonesvalls › Alt Penedès | 33 |
| Forêt de Moià (16) | Moià › Moianès | 33 |
| Forêt de Olvan (10) | Olvan › Berguedà | 33 |
| Forêt de Montclar (18) | Montclar › Berguedà | 33 |
| Forêt de Capolat (18) | Capolat › Berguedà | 33 |
| Forêt de Avinyó (93) | Avinyó › Bages | 33 |
| Forêt de Santa Maria de Besora (15) | Santa Maria de Besora › Osona (Barcelone) | 33 |
| Forêt de Talamanca (5) | Talamanca › Bages | 33 |
| Forêt de Mura (34) | Mura › Bages | 33 |
| Forêt de Castellfollit del Boix (30) | Castellfollit del Boix › Bages | 33 |
| Forêt de Navàs (124) | Navàs › Bages | 33 |
| Forêt de Viver i Serrateix (90) | Viver i Serrateix › Berguedà | 33 |
| Forêt de Vic (29) | Vic › Osona (Barcelone) | 33 |
| Forêt de Jorba (17) | Jorba › Anoia | 33 |
| Forêt de Cubelles (21) | Cubelles › Garraf | 33 |
| Forêt de Santa Maria de Merlès (79) | Santa Maria de Merlès › Berguedà | 33 |
| Forêt de la Quar (18) | la Quar › Berguedà | 33 |
| Forêt de Sant Martí de Centelles (49) | Sant Martí de Centelles › Osona (Barcelone) | 33 |
| Forêt de Sant Martí de Centelles (64) | Sant Martí de Centelles › Osona (Barcelone) | 33 |
| Forêt de Sant Martí de Centelles (65) | Sant Martí de Centelles › Osona (Barcelone) | 33 |
| Forêt de Dosrius (24) | Dosrius › Maresme | 33 |
| Forêt de Castellfollit del Boix (38) | Castellfollit del Boix › Bages | 33 |
| Forêt de Saldes (41) | Saldes › Berguedà | 33 |
| Forêt de Guardiola de Berguedà (97) | Guardiola de Berguedà › Berguedà | 33 |
| Forêt de la Pobla de Lillet (36) | la Pobla de Lillet › Berguedà | 33 |
| Forêt de Balenyà (31) | Balenyà › Osona (Barcelone) | 33 |
| Forêt de Sora (28) | Sora › Osona (Barcelone) | 33 |
| Forêt de Tavèrnoles (5) | Tavèrnoles › Osona (Barcelone) | 33 |
| Forêt de Alella (4) | Alella › Maresme | 33 |
| Forêt de Carme (9) | Carme › Anoia | 33 |
| Forêt de la Llacuna (18) | la Llacuna › Anoia | 33 |
| Forêt de Alpens (26) | Alpens › Lluçanès | 33 |
| Forêt de Sant Cugat del Vallès (162) | Sant Cugat del Vallès › Vallès Occidental | 33 |
| Forêt de Sallent (122) | Sallent › Bages | 33 |
| Forêt de Alpens (5) | Alpens › Lluçanès | 32 |
| Forêt de Sora (14) | Sora › Osona (Barcelone) | 32 |
| Forêt de Granera | Granera › Moianès | 32 |
| Forêt de Veciana (3) | Veciana › Anoia | 32 |
| Forêt de Argençola (18) | Argençola › Anoia | 32 |
| Forêt de Santa Margarida i els Monjos (19) | Santa Margarida i els Monjos › Alt Penedès | 32 |
| Bois de Dosrius (9) | Dosrius › Maresme | 32 |
| Forêt de Viver i Serrateix (13) | Viver i Serrateix › Berguedà | 32 |
| Bois de Argençola (22) | Argençola › Anoia | 32 |
| Forêt de Figaró-Montmany | Figaró-Montmany › Vallès Oriental | 32 |
| Forêt de Sant Joan de Vilatorrada (20) | Sant Joan de Vilatorrada › Bages | 32 |
| Forêt de Sant Pere de Torelló (15) | Sant Pere de Torelló › Osona (Barcelone) | 32 |
| Forêt de Sant Mateu de Bages (36) | Sant Mateu de Bages › Bages | 32 |
| Forêt de Rubí (56) | Rubí › Vallès Occidental | 32 |
| Forêt de Puig-reig (47) | Puig-reig › Berguedà | 32 |
| Forêt de Vacarisses (18) | Vacarisses › Vallès Occidental | 32 |
| Forêt de Vacarisses (48) | Vacarisses › Vallès Occidental | 32 |
| Forêt de Castellbell i el Vilar (14) | Castellbell i el Vilar › Bages | 32 |
| Forêt de Vallromanes (13) | Vallromanes › Vallès Oriental | 32 |
| Forêt de Gaià (53) | Gaià › Bages | 32 |
| Forêt de Viver i Serrateix (33) | Viver i Serrateix › Berguedà | 32 |
| Forêt de Casserres (23) | Casserres › Berguedà | 32 |
| Forêt de Avià (34) | Avià › Berguedà | 32 |
| Forêt de Jorba (27) | Jorba › Anoia | 32 |
| Forêt de Borredà (46) | Borredà › Berguedà | 32 |
| Forêt de Sagàs (26) | Sagàs › Berguedà | 32 |
| Forêt de Sagàs (33) | Sagàs › Berguedà | 32 |
| Forêt de Oristà (111) | Oristà › Lluçanès | 32 |
| Forêt de Sant Mateu de Bages (102) | Sant Mateu de Bages › Bages | 32 |
| Forêt de Guardiola de Berguedà (80) | Guardiola de Berguedà › Berguedà | 32 |
| Forêt de Guardiola de Berguedà (109) | Guardiola de Berguedà › Berguedà | 32 |
| Forêt de Lluçà (32) | Lluçà › Lluçanès | 32 |
| Forêt de Vallcebre (30) | Vallcebre › Berguedà | 32 |
| Forêt de Pontons (18) | Pontons › Alt Penedès | 32 |
| Forêt de Alpens (16) | Alpens › Lluçanès | 32 |
| Forêt de Sant Cebrià de Vallalta (3) | Sant Cebrià de Vallalta › Maresme | 32 |
| Forêt de Tordera (103) | Tordera › Maresme | 32 |
| Forêt de Tordera (109) | Tordera › Maresme | 32 |
| Forêt de Santpedor (58) | Santpedor › Bages | 32 |
| Forêt de Sant Mateu de Bages (110) | Sant Mateu de Bages › Bages | 32 |
| Forêt de Tavèrnoles (8) | Tavèrnoles › Osona (Barcelone) | 32 |
| Forêt de Sant Quintí de Mediona (21) | Sant Quintí de Mediona › Alt Penedès | 32 |
| Forêt de Muntanyola | Muntanyola › Osona (Barcelone) | 31 |
| Forêt de Sora (7) | Sora › Osona (Barcelone) | 31 |
| Forêt de Alpens (10) | Alpens › Lluçanès | 31 |
| Bois de Dosrius (7) | Dosrius › Maresme | 31 |
| Forêt de Seva (12) | Seva › Osona (Barcelone) | 31 |
| Forêt de Aguilar de Segarra (15) | Aguilar de Segarra › Bages | 31 |
| Forêt de Tordera (48) | Tordera › Maresme | 31 |
| Forêt de l'Espunyola (31) | l'Espunyola › Berguedà | 31 |
| Forêt de el Pont de Vilomara i Rocafort (11) | el Pont de Vilomara i Rocafort › Bages | 31 |
| Forêt de Sant Vicenç de Castellet (18) | Sant Vicenç de Castellet › Bages | 31 |
| Forêt de Gavà (72) | Gavà › Baix Llobregat | 31 |
| Forêt de Cànoves i Samalús (34) | Cànoves i Samalús › Vallès Oriental | 31 |
| Forêt de Monistrol de Calders (10) | Monistrol de Calders › Moianès | 31 |
| Forêt de Aguilar de Segarra (31) | Aguilar de Segarra › Bages | 31 |
| Forêt de Navàs (73) | Navàs › Bages | 31 |
| Forêt de Dosrius (4) | Dosrius › Maresme | 31 |
| Forêt de Sant Jaume de Frontanyà (17) | Sant Jaume de Frontanyà › Berguedà | 31 |
| Forêt de Santa Maria d'Oló (56) | Santa Maria d'Oló › Moianès | 31 |
| Forêt de l'Estany (6) | l'Estany › Moianès | 31 |
| Forêt de Santa Eulàlia de Riuprimer (9) | Santa Eulàlia de Riuprimer › Osona (Barcelone) | 31 |
| Forêt de Balenyà (26) | Balenyà › Osona (Barcelone) | 31 |
| Forêt de Sant Martí d'Albars (2) | Sant Martí d'Albars › Lluçanès | 31 |
| Forêt de Pontons (12) | Pontons › Alt Penedès | 31 |
| Forêt de Lluçà (68) | Lluçà › Lluçanès | 31 |
| Forêt de Santa Susanna (2) | Santa Susanna › Maresme | 31 |
| Forêt de Santa Susanna (7) | Santa Susanna › Maresme | 31 |
| Forêt de Tordera (111) | Tordera › Maresme | 31 |
| Forêt de Sant Julià de Vilatorta (7) | Sant Julià de Vilatorta › Osona (Barcelone) | 31 |
| Forêt de Talamanca (41) | Talamanca › Bages | 31 |
| Forêt de Subirats | Subirats › Alt Penedès | 30 |
| Forêt de Font-rubí | Font-rubí › Alt Penedès | 30 |
| Forêt de Olost (2) | Olost › Lluçanès | 30 |
| Forêt de la Quar (3) | la Quar › Berguedà | 30 |
| Forêt de Sant Celoni (5) | Sant Celoni › Vallès Oriental | 30 |
| Forêt de Sant Pere de Ribes (3) | Sant Pere de Ribes › Garraf | 30 |
| Bois de Dosrius (2) | Dosrius › Maresme | 30 |
| Forêt de Santa Margarida i els Monjos (31) | Santa Margarida i els Monjos › Alt Penedès | 30 |
| Forêt de Sant Sadurní d'Osormort (20) | Sant Sadurní d'Osormort › Osona (Barcelone) | 30 |
| Forêt de Montseny (5) | Montseny › Vallès Oriental | 30 |
| Forêt de Olvan (6) | Olvan › Berguedà | 30 |
| Forêt de Abrera (6) | Abrera › Baix Llobregat | 30 |
| Forêt de Castellbell i el Vilar (2) | Castellbell i el Vilar › Bages | 30 |
| Forêt de Manresa (17) | Manresa › Bages | 30 |
| Forêt de Cercs (10) | Cercs › Berguedà | 30 |
| Forêt de Avinyó (52) | Avinyó › Bages | 30 |
| Forêt de Sant Pol de Mar (15) | Sant Pol de Mar › Maresme | 30 |
| Forêt de Corbera de Llobregat (25) | Corbera de Llobregat › Baix Llobregat | 30 |
| Forêt de Vacarisses (37) | Vacarisses › Vallès Occidental | 30 |
| Forêt de Marganell (13) | Marganell › Bages | 30 |
| Forêt de Talamanca (13) | Talamanca › Bages | 30 |
| Forêt de Aguilar de Segarra (25) | Aguilar de Segarra › Bages | 30 |
| Forêt de Viver i Serrateix (43) | Viver i Serrateix › Berguedà | 30 |
| Forêt de Gisclareny (15) | Gisclareny › Berguedà | 30 |
| Forêt de Sagàs (35) | Sagàs › Berguedà | 30 |
| Forêt de Figaró-Montmany (4) | Sant Martí de Centelles › Vallès Oriental | 30 |
| Forêt de Sant Feliu de Codines (10) | Sant Feliu de Codines › Vallès Oriental | 30 |
| Forêt de Sant Martí de Centelles (75) | Sant Martí de Centelles › Osona (Barcelone) | 30 |
| Forêt de Cànoves i Samalús (47) | Cànoves i Samalús › Vallès Oriental | 30 |
| Forêt de Gisclareny (35) | Gisclareny › Berguedà | 30 |
| Forêt de Pontons (16) | Pontons › Alt Penedès | 30 |
| Forêt de Cerdanyola del Vallès (60) | Cerdanyola del Vallès › Vallès Occidental | 30 |
| Forêt de Guardiola de Berguedà (130) | Guardiola de Berguedà › Berguedà | 30 |
| Forêt de Mediona (83) | Mediona › Alt Penedès | 30 |
| Forêt de Tordera (104) | Tordera › Maresme | 30 |
| Forêt de Calella (7) | Calella › Maresme | 30 |
| Forêt de Sant Andreu de Llavaneres (5) | Sant Andreu de Llavaneres › Maresme | 30 |
| Forêt de Taradell (40) | Taradell › Osona (Barcelone) | 30 |
| Forêt de Orís | Orís › Osona (Barcelone) | 29 |
| Forêt de Lluçà (2) | Lluçà › Lluçanès | 29 |
| Bois de Vilassar de Dalt (4) | Vilassar de Dalt › Maresme | 29 |
| Forêt de Calella | Calella › Maresme | 29 |
| Forêt de Olesa de Bonesvalls (31) | Olesa de Bonesvalls › Alt Penedès | 29 |
| Forêt de Esparreguera (7) | Esparreguera › Baix Llobregat | 29 |
| Forêt de Sallent (51) | Sallent › Bages | 29 |
| Forêt de Vacarisses (20) | Vacarisses › Vallès Occidental | 29 |
| Forêt de Sitges (53) | Sitges › Garraf | 29 |
| Forêt de Gaià (39) | Gaià › Bages | 29 |
| Forêt de Castell de l'Areny (25) | Castell de l'Areny › Berguedà | 29 |
| Forêt de Vallcebre (19) | Vallcebre › Berguedà | 29 |
| Forêt de Calders (60) | Calders › Moianès | 29 |
| Forêt de Puig-reig (55) | Puig-reig › Berguedà | 29 |
| Forêt de Capolat (22) | Capolat › Berguedà | 29 |
| Forêt de Navàs (96) | Navàs › Bages | 29 |
| Forêt de Navàs (100) | Navàs › Bages | 29 |
| Forêt de Navàs (118) | Navàs › Bages | 29 |
| Forêt de Begues (50) | Begues › Baix Llobregat | 29 |
| Forêt de Sant Quirze Safaja (51) | Sant Quirze Safaja › Moianès | 29 |
| Forêt de Santa Eulàlia de Riuprimer (14) | Santa Eulàlia de Riuprimer › Osona (Barcelone) | 29 |
| Forêt de Muntanyola (31) | Muntanyola › Osona (Barcelone) | 29 |
| Forêt de Dosrius (8) | Dosrius › Maresme | 29 |
| Forêt de Arenys de Munt (6) | Vallgorguina › Vallès Oriental | 29 |
| Forêt de Saldes (62) | Saldes › Berguedà | 29 |
| Forêt de Saldes (65) | Saldes › Berguedà | 29 |
| Forêt de Bagà (42) | Bagà › Berguedà | 29 |
| Forêt de Lluçà (54) | Borredà › Berguedà | 29 |
| Forêt de Borredà (95) | Borredà › Berguedà | 29 |
| Forêt de Vallcebre (38) | Vallcebre › Berguedà | 29 |
| Forêt de Montcada i Reixac (29) | Montcada i Reixac › Vallès Occidental | 29 |
| Forêt de Palafolls (28) | Palafolls › Maresme | 29 |
| Forêt de Sant Celoni (37) | Sant Celoni › Vallès Oriental | 29 |
| Forêt de Callús (35) | Callús › Bages | 29 |
| Forêt de Sora (19) | Sora › Osona (Barcelone) | 28 |
| Forêt de Argençola (17) | Argençola › Anoia | 28 |
| Forêt de Montmajor (24) | Montmajor › Berguedà | 28 |
| Forêt de les Franqueses del Vallès (14) | les Franqueses del Vallès › Vallès Oriental | 28 |
| Forêt de Rajadell (8) | Rajadell › Bages | 28 |
| Forêt de Vilanova de Sau (35) | Vilanova de Sau › Osona (Barcelone) | 28 |
| Forêt de Viladecavalls (8) | Viladecavalls › Vallès Occidental | 28 |
| Forêt de Cardona (57) | Cardona › Bages | 28 |
| Forêt de l'Espunyola (13) | l'Espunyola › Berguedà | 28 |
| Forêt de Santa Margarida de Montbui (15) | Santa Margarida de Montbui › Anoia | 28 |
| Forêt de Vacarisses (15) | Vacarisses › Vallès Occidental | 28 |
| Forêt de Avinyó (84) | Avinyó › Bages | 28 |
| Forêt de la Pobla de Lillet (19) | la Pobla de Lillet › Berguedà | 28 |
| Forêt de Capolat (20) | Capolat › Berguedà | 28 |
| Forêt de Súria (28) | Súria › Bages | 28 |
| Forêt de Viver i Serrateix (84) | Viver i Serrateix › Berguedà | 28 |
| Forêt de Sant Fost de Campsentelles (9) | Sant Fost de Campsentelles › Vallès Oriental | 28 |
| Forêt de Avinyonet del Penedès (64) | Avinyonet del Penedès › Alt Penedès | 28 |
| Forêt de Viver i Serrateix (96) | Viver i Serrateix › Berguedà | 28 |
| Forêt de els Hostalets de Pierola (22) | els Hostalets de Pierola › Anoia | 28 |
| Forêt de Esparreguera (40) | Esparreguera › Baix Llobregat | 28 |
| Forêt de Tagamanent (15) | Tagamanent › Vallès Oriental | 28 |
| Forêt de les Franqueses del Vallès (55) | les Franqueses del Vallès › Vallès Oriental | 28 |
| Forêt de Tona (29) | Tona › Osona (Barcelone) | 28 |
| Forêt de Vallcebre (22) | Vallcebre › Berguedà | 28 |
| Forêt de Bagà (53) | Bagà › Berguedà | 28 |
| Forêt de Guardiola de Berguedà (99) | Guardiola de Berguedà › Berguedà | 28 |
| Forêt de la Roca del Vallès (13) | la Roca del Vallès › Vallès Oriental | 28 |
| Forêt de Pontons (15) | Pontons › Alt Penedès | 28 |
| Forêt de Guardiola de Berguedà (131) | Guardiola de Berguedà › Berguedà | 28 |
| Forêt de Piera (61) | Piera › Anoia | 28 |
| Forêt de Piera (70) | Piera › Anoia | 28 |
| Forêt de la Llacuna (16) | la Llacuna › Anoia | 28 |
| Forêt de Tavertet (41) | Tavertet › Osona (Barcelone) | 28 |
| Forêt de Sallent (116) | Sallent › Bages | 28 |
| Forêt de Sant Mateu de Bages (134) | Sant Mateu de Bages › Bages | 28 |
| Forêt de Gurb (57) | Gurb › Osona (Barcelone) | 28 |
| Forêt de Granera (38) | Granera › Moianès | 28 |
| Forêt de Moià (66) | Moià › Moianès | 28 |
| Forêt de el Pont de Vilomara i Rocafort (38) | el Pont de Vilomara i Rocafort › Bages | 28 |
| Forêt de la Quar | la Quar › Berguedà | 27 |
| Forêt de Borredà | Borredà › Berguedà | 27 |
| Forêt de Sant Pere de Torelló | Sant Pere de Torelló › Osona (Barcelone) | 27 |
| Forêt de Sant Feliu de Codines | Sant Feliu de Codines › Vallès Oriental | 27 |
| Forêt de Olèrdola (50) | Olèrdola › Alt Penedès | 27 |
| Forêt de Sant Esteve Sesrovires (8) | Sant Esteve Sesrovires › Baix Llobregat | 27 |
| Forêt de Cànoves i Samalús (24) | Cànoves i Samalús › Vallès Oriental | 27 |
| Forêt de Callús (9) | Callús › Bages | 27 |
| Forêt de les Masies de Roda | les Masies de Roda › Osona (Barcelone) | 27 |
| Forêt de Castellar del Vallès (11) | Castellar del Vallès › Vallès Occidental | 27 |
| Forêt de Vallcebre (12) | Vallcebre › Berguedà | 27 |
| Bois de Viladecavalls (8) | Viladecavalls › Vallès Occidental | 27 |
| Forêt de Cardona (39) | Cardona › Bages | 27 |
| Forêt de Gaià (15) | Gaià › Bages | 27 |
| Forêt de Capolat (17) | Capolat › Berguedà | 27 |
| Forêt de Gavà (64) | Gavà › Baix Llobregat | 27 |
| Forêt de la Pobla de Lillet (24) | la Pobla de Lillet › Berguedà | 27 |
| Forêt de Talamanca (4) | Mura › Bages | 27 |
| Forêt de Talamanca (16) | Talamanca › Bages | 27 |
| Forêt de Navàs (75) | Navàs › Bages | 27 |
| Forêt de Santa Maria de Merlès (19) | Santa Maria de Merlès › Berguedà | 27 |
| Forêt de Casserres (24) | Casserres › Berguedà | 27 |
| Forêt de Navàs (98) | Navàs › Bages | 27 |
| Forêt de Navàs (126) | Navàs › Bages | 27 |
| Forêt de Viver i Serrateix (89) | Viver i Serrateix › Berguedà | 27 |
| Forêt de Gaià (63) | Gaià › Bages | 27 |
| Forêt de Saldes (19) | Saldes › Berguedà | 27 |
| Bois de Llinars del Vallès (30) | Llinars del Vallès › Vallès Oriental | 27 |
| Forêt de Argençola (29) | Argençola › Anoia | 27 |
| Forêt de Olivella (114) | Olivella › Garraf | 27 |
| Forêt de Canyelles (27) | Canyelles › Garraf | 27 |
| Bois de Ullastrell (2) | Ullastrell › Vallès Occidental | 27 |
| Forêt de Navàs (145) | Navàs › Bages | 27 |
| Forêt de Monistrol de Calders (37) | Monistrol de Calders › Moianès | 27 |
| Forêt de Montseny (11) | Montseny › Vallès Oriental | 27 |
| Forêt de Sant Celoni (28) | Sant Celoni › Vallès Oriental | 27 |
| Forêt de Castellar del Riu (45) | Castellar del Riu › Berguedà | 27 |
| Forêt de Vallcebre (31) | Vallcebre › Berguedà | 27 |
| Forêt de Tordera (65) | Tordera › Maresme | 27 |
| Forêt de Castellar de n'Hug (33) | Castellar de n'Hug › Berguedà | 27 |
| Forêt de Mediona (95) | Mediona › Alt Penedès | 27 |
| Forêt de Olvan (36) | Olvan › Berguedà | 27 |
| Forêt de Sant Sadurní d'Osormort (31) | Sant Sadurní d'Osormort › Osona (Barcelone) | 27 |
| Forêt de Vilanova de Sau (65) | Vilanova de Sau › Osona (Barcelone) | 27 |
| Forêt de el Pont de Vilomara i Rocafort (34) | el Pont de Vilomara i Rocafort › Bages | 27 |
| Forêt de Sora (13) | Sora › Osona (Barcelone) | 26 |
| Forêt de Sant Boi de Llobregat | Sant Boi de Llobregat › Baix Llobregat | 26 |
| Forêt de Sant Llorenç d'Hortons (17) | Sant Llorenç d'Hortons › Alt Penedès | 26 |
| Forêt de Sant Martí Sarroca (13) | Sant Martí Sarroca › Alt Penedès | 26 |
| Bois de Argentona (9) | Argentona › Maresme | 26 |
| Forêt de Sagàs (4) | Sagàs › Berguedà | 26 |
| Forêt de Cànoves i Samalús (26) | Cànoves i Samalús › Vallès Oriental | 26 |
| Forêt de Manresa (16) | Manresa › Bages | 26 |
| Forêt de Sant Joan de Vilatorrada (21) | Sant Joan de Vilatorrada › Bages | 26 |
| Forêt de Avinyó (20) | Avinyó › Bages | 26 |
| Forêt de Balsareny (22) | Balsareny › Bages | 26 |
| Forêt de Rajadell (36) | Rajadell › Bages | 26 |
| Forêt de Castell de l'Areny (4) | Castell de l'Areny › Berguedà | 26 |
| Forêt de Esparreguera (8) | Esparreguera › Baix Llobregat | 26 |
| Forêt de Manresa (97) | Manresa › Bages | 26 |
| Forêt de Montmajor (57) | Montmajor › Berguedà | 26 |
| Forêt de l'Espunyola (33) | l'Espunyola › Berguedà | 26 |
| Forêt de Vacarisses (47) | Vacarisses › Vallès Occidental | 26 |
| Forêt de el Bruc (15) | el Bruc › Anoia | 26 |
| Forêt de Castellbell i el Vilar (54) | Castellbell i el Vilar › Bages | 26 |
| Forêt de Borredà (12) | Borredà › Berguedà | 26 |
| Forêt de Guardiola de Berguedà (46) | Guardiola de Berguedà › Berguedà | 26 |
| Forêt de el Bruc (39) | el Bruc › Anoia | 26 |
| Forêt de Viver i Serrateix (91) | Viver i Serrateix › Berguedà | 26 |
| Forêt de Santa Maria de Merlès (56) | Santa Maria de Merlès › Berguedà | 26 |
| Forêt de Gurb (20) | Gurb › Osona (Barcelone) | 26 |
| Forêt de Vilada (16) | Vilada › Berguedà | 26 |
| Forêt de la Quar (8) | la Quar › Berguedà | 26 |
| Forêt de Jorba (11) | Santa Margarida de Montbui › Anoia | 26 |
| Forêt de Jorba (30) | Jorba › Anoia | 26 |
| Forêt de Avinyonet del Penedès (56) | Avinyonet del Penedès › Alt Penedès | 26 |
| Forêt de Aguilar de Segarra (51) | Aguilar de Segarra › Bages | 26 |
| Forêt de Sant Bartomeu del Grau (14) | Sant Bartomeu del Grau › Osona (Barcelone) | 26 |
| Forêt de Sant Martí de Centelles (59) | Sant Martí de Centelles › Osona (Barcelone) | 26 |
| Forêt de Sant Martí de Centelles (67) | Sant Martí de Centelles › Osona (Barcelone) | 26 |
| Forêt de Sant Feliu Sasserra (20) | Sant Feliu Sasserra › Bages | 26 |
| Bosc de Can Montells | Cardedeu › Vallès Oriental | 26 |
| Forêt de Sagàs (40) | Sagàs › Berguedà | 26 |
| Forêt de Dosrius (23) | Dosrius › Maresme | 26 |
| Forêt de Balenyà (19) | Balenyà › Osona (Barcelone) | 26 |
| Forêt de Gisclareny (24) | Gisclareny › Berguedà | 26 |
| Forêt de Lluçà (27) | Lluçà › Lluçanès | 26 |
| Forêt de la Quar (34) | la Quar › Berguedà | 26 |
| Forêt de Sagàs (49) | Sagàs › Berguedà | 26 |
| Forêt de Borredà (102) | Borredà › Berguedà | 26 |
| Forêt de Borredà (117) | Borredà › Berguedà | 26 |
| Forêt de la Pobla de Lillet (51) | la Pobla de Lillet › Berguedà | 26 |
| Forêt de Balenyà (29) | Balenyà › Osona (Barcelone) | 26 |
| Forêt de Sant Martí de Tous (30) | Sant Martí de Tous › Anoia | 26 |
| Forêt de Castellar de n'Hug (45) | Castellar de n'Hug › Berguedà | 26 |
| Forêt de Vallirana (39) | Vallirana › Baix Llobregat | 26 |
| Forêt de Torrelles de Foix (2) | Torrelles de Foix › Alt Penedès | 26 |
| Forêt de Lluçà (85) | Lluçà › Lluçanès | 26 |
| Forêt de Sant Celoni (39) | Sant Celoni › Vallès Oriental | 26 |
| Forêt de Vilanova de Sau (64) | Vilanova de Sau › Osona (Barcelone) | 26 |
| Forêt de Sant Agustí de Lluçanès | Sant Agustí de Lluçanès › Osona (Barcelone) | 25 |
| Forêt de Avinyonet del Penedès | Avinyonet del Penedès › Alt Penedès | 25 |
| Forêt de Sant Mateu de Bages (4) | Sant Mateu de Bages › Bages | 25 |
| Forêt de Sora (8) | Sora › Osona (Barcelone) | 25 |
| Forêt de Santa Eulàlia de Ronçana (2) | Santa Eulàlia de Ronçana › Vallès Oriental | 25 |
| Forêt de Calonge de Segarra (9) | Calonge de Segarra › Anoia | 25 |
| Forêt de la Garriga (36) | la Garriga › Vallès Oriental | 25 |
| Forêt de el Brull (11) | el Brull › Osona (Barcelone) | 25 |
| Forêt de Balsareny (21) | Balsareny › Bages | 25 |
| Forêt de Vallcebre (18) | Vallcebre › Berguedà | 25 |
| Forêt de Lliçà de Vall (5) | Lliçà de Vall › Vallès Oriental | 25 |
| Forêt de Saldes (15) | Saldes › Berguedà | 25 |
| Forêt de Pallejà (4) | Pallejà › Baix Llobregat | 25 |
| Forêt de Castellví de Rosanes (5) | Castellví de Rosanes › Baix Llobregat | 25 |
| Forêt de Corbera de Llobregat (17) | Corbera de Llobregat › Baix Llobregat | 25 |
| Forêt de Guardiola de Berguedà (37) | Guardiola de Berguedà › Berguedà | 25 |
| Forêt de Sant Vicenç de Castellet (21) | Sant Vicenç de Castellet › Bages | 25 |
| Forêt de Begues (38) | Begues › Baix Llobregat | 25 |
| Forêt de Santa Maria d'Oló (32) | Santa Maria d'Oló › Moianès | 25 |
| Forêt de Sant Celoni (23) | Sant Celoni › Vallès Oriental | 25 |
| Forêt de la Pobla de Lillet (13) | la Pobla de Lillet › Berguedà | 25 |
| Forêt de Cercs (48) | Cercs › Berguedà | 25 |
| Forêt de la Pobla de Lillet (31) | la Pobla de Lillet › Berguedà | 25 |
| Forêt de Mura (31) | Mura › Bages | 25 |
| Forêt de Calders (61) | Calders › Moianès | 25 |
| Forêt de el Bruc (44) | el Bruc › Anoia | 25 |
| Forêt de Navàs (79) | Navàs › Bages | 25 |
| Forêt de Navàs (135) | Navàs › Bages | 25 |
| Forêt de Gaià (59) | Gaià › Bages | 25 |
| Forêt de Canyelles (6) | Canyelles › Garraf | 25 |
| Forêt de Sant Antoni de Vilamajor (41) | Sant Antoni de Vilamajor › Vallès Oriental | 25 |
| Forêt de Vallcebre (21) | Vallcebre › Berguedà | 25 |
| Forêt de Borredà (90) | Borredà › Berguedà | 25 |
| Forêt de la Pobla de Lillet (57) | la Pobla de Lillet › Berguedà | 25 |
| Forêt de Vallromanes (14) | Vallromanes › Vallès Oriental | 25 |
| Forêt de Carme (6) | Carme › Anoia | 25 |
| Forêt de Sant Cebrià de Vallalta (4) | Sant Cebrià de Vallalta › Maresme | 25 |
| Forêt de Tordera (108) | Tordera › Maresme | 25 |
| Forêt de Castellnou de Bages (54) | Castellnou de Bages › Bages | 25 |
| Forêt de Sant Sadurní d'Osormort (45) | Sant Sadurní d'Osormort › Osona (Barcelone) | 25 |
| Bois de Cabrils (14) | Cabrils › Maresme | 25 |
| Forêt de Torrelles de Llobregat | Torrelles de Llobregat › Baix Llobregat | 24 |
| Forêt de Sant Jaume de Frontanyà (3) | Sant Jaume de Frontanyà › Berguedà | 24 |
| Forêt de Pontons (5) | Pontons › Alt Penedès | 24 |
| Forêt de Sant Boi de Lluçanès | Sant Boi de Lluçanès › Osona (Barcelone) | 24 |
| Forêt de la Roca del Vallès | la Roca del Vallès › Vallès Oriental | 24 |
| Forêt de Molins de Rei (3) | Molins de Rei › Baix Llobregat | 24 |
| Forêt de Rubí (16) | Rubí › Vallès Occidental | 24 |
| Forêt de Cercs (3) | Cercs › Berguedà | 24 |
| Forêt de Sant Joan de Vilatorrada (61) | Fonollosa › Bages | 24 |
| Forêt de Sant Feliu Sasserra (10) | Sant Feliu Sasserra › Bages | 24 |
| Forêt de Navàs (25) | Navàs › Bages | 24 |
| Forêt de Vacarisses (16) | Vacarisses › Vallès Occidental | 24 |
| Forêt de Vacarisses (46) | Vacarisses › Vallès Occidental | 24 |
| Forêt de Cercs (31) | Cercs › Berguedà | 24 |
| Forêt de Santa Maria de Besora (14) | Santa Maria de Besora › Osona (Barcelone) | 24 |
| Forêt de Guardiola de Berguedà (44) | Guardiola de Berguedà › Berguedà | 24 |
| Forêt de Casserres (26) | Casserres › Berguedà | 24 |
| Forêt de Gurb (21) | Gurb › Osona (Barcelone) | 24 |
| Forêt de Castellet i la Gornal (71) | Castellet i la Gornal › Alt Penedès | 24 |
| Forêt de Ullastrell (3) | Ullastrell › Vallès Occidental | 24 |
| Forêt de Sant Antoni de Vilamajor (39) | Sant Antoni de Vilamajor › Vallès Oriental | 24 |
| Forêt de Tagamanent (19) | Tagamanent › Vallès Oriental | 24 |
| Forêt de Sant Martí de Centelles (53) | Sant Martí de Centelles › Osona (Barcelone) | 24 |
| Forêt de Figaró-Montmany (6) | Figaró-Montmany › Vallès Oriental | 24 |
| Forêt de Seva (22) | Seva › Osona (Barcelone) | 24 |
| Forêt de Sant Feliu Sasserra (19) | Sant Feliu Sasserra › Bages | 24 |
| Forêt de Sant Iscle de Vallalta (4) | Sant Iscle de Vallalta › Maresme | 24 |
| Forêt de Muntanyola (34) | Muntanyola › Osona (Barcelone) | 24 |
| Forêt de Gisclareny (43) | Gisclareny › Berguedà | 24 |
| Forêt de la Quar (30) | la Quar › Berguedà | 24 |
| Forêt de Montmajor (135) | Montmajor › Berguedà | 24 |
| Forêt de Sant Fost de Campsentelles (13) | Sant Fost de Campsentelles › Vallès Oriental | 24 |
| Forêt de Castellar de n'Hug (31) | Castellar de n'Hug › Berguedà | 24 |
| Forêt de Castellar de n'Hug (36) | Castellar de n'Hug › Berguedà | 24 |
| Bois de Piera (7) | Piera › Anoia | 24 |
| Forêt de Piera (66) | Piera › Anoia | 24 |
| Forêt de la Llacuna (21) | la Llacuna › Anoia | 24 |
| Forêt de Lluçà (69) | Lluçà › Lluçanès | 24 |
| Forêt de Sant Iscle de Vallalta (7) | Sant Iscle de Vallalta › Maresme | 24 |
| Forêt de Sant Celoni (32) | Sant Celoni › Vallès Oriental | 24 |
| Forêt de Tordera (113) | Tordera › Maresme | 24 |
| Forêt de Castellnou de Bages (56) | Castellnou de Bages › Bages | 24 |
| Forêt de Callús (38) | Callús › Bages | 24 |
| Forêt de Vallcebre (67) | Vallcebre › Berguedà | 24 |
| Forêt de Gurb (63) | Gurb › Osona (Barcelone) | 24 |
| Forêt de Sant Quirze Safaja (54) | Sant Quirze Safaja › Moianès | 24 |
| Forêt de la Llacuna (4) | la Llacuna › Anoia | 23 |
| Forêt de Òdena | Òdena › Anoia | 23 |
| Forêt de Sant Pere de Ribes (2) | Sant Pere de Ribes › Garraf | 23 |
| Forêt de Vilanova de Sau (11) | Vilanova de Sau › Osona (Barcelone) | 23 |
| Forêt de Olèrdola (4) | Olèrdola › Alt Penedès | 23 |
| Forêt de Òdena (10) | Òdena › Anoia | 23 |
| Bois de Òrrius (23) | Òrrius › Maresme | 23 |
| Bois de Cabrils (11) | Cabrils › Maresme | 23 |
| Forêt de l'Espunyola (7) | l'Espunyola › Berguedà | 23 |
| Forêt de Sallent (47) | Sallent › Bages | 23 |
| Forêt de Manresa (22) | Manresa › Bages | 23 |
| Forêt de Cerdanyola del Vallès (56) | Cerdanyola del Vallès › Vallès Occidental | 23 |
| Forêt de Oristà (100) | Oristà › Lluçanès | 23 |
| Forêt de Sant Vicenç de Castellet (12) | Sant Vicenç de Castellet › Bages | 23 |
| Forêt de Sant Salvador de Guardiola (53) | Sant Salvador de Guardiola › Bages | 23 |
| Forêt de Gaià (50) | Gaià › Bages | 23 |
| Forêt de Sant Pere de Vilamajor (85) | Sant Pere de Vilamajor › Vallès Oriental | 23 |
| Forêt de Castell de l'Areny (27) | Castell de l'Areny › Berguedà | 23 |
| Forêt de Sant Jaume de Frontanyà (7) | Sant Jaume de Frontanyà › Berguedà | 23 |
| Forêt de Talamanca (23) | Talamanca › Bages | 23 |
| Forêt de Aguilar de Segarra (40) | Aguilar de Segarra › Bages | 23 |
| Forêt de Rajadell (42) | Rajadell › Bages | 23 |
| Forêt de Viver i Serrateix (41) | Viver i Serrateix › Berguedà | 23 |
| Forêt de Montclar (28) | Montclar › Berguedà | 23 |
| Forêt de Sant Fost de Campsentelles (8) | Sant Fost de Campsentelles › Vallès Oriental | 23 |
| Forêt de Sant Pere de Ribes (94) | Sant Pere de Ribes › Garraf | 23 |
| Forêt de Castellet i la Gornal (84) | Castellet i la Gornal › Alt Penedès | 23 |
| Forêt de Viver i Serrateix (95) | Viver i Serrateix › Berguedà | 23 |
| Forêt de Súria (36) | Súria › Bages | 23 |
| Forêt de Sagàs (32) | Sagàs › Berguedà | 23 |
| Forêt de Collbató (20) | Collbató › Baix Llobregat | 23 |
| Forêt de Santa Eulàlia de Riuprimer (8) | Santa Eulàlia de Riuprimer › Osona (Barcelone) | 23 |
| Forêt de Guardiola de Berguedà (73) | Guardiola de Berguedà › Berguedà | 23 |
| Forêt de Guardiola de Berguedà (100) | Guardiola de Berguedà › Berguedà | 23 |
| Forêt de Borredà (96) | Borredà › Berguedà | 23 |
| Forêt de Mediona (58) | Mediona › Alt Penedès | 23 |
| Forêt de Piera (79) | Piera › Anoia | 23 |
| Forêt de Sant Quintí de Mediona (14) | Sant Quintí de Mediona › Alt Penedès | 23 |
| Forêt de Tavertet (54) | Tavertet › Osona (Barcelone) | 23 |
| Forêt de Tavertet (78) | Tavertet › Osona (Barcelone) | 23 |
| Forêt de Lluçà (56) | Lluçà › Lluçanès | 23 |
| Forêt de Tordera (116) | Tordera › Maresme | 23 |
| Forêt de Callús (52) | Callús › Bages | 23 |
| Forêt de Sant Mateu de Bages (113) | Sant Mateu de Bages › Bages | 23 |
| Bois de Cabrils (15) | Cabrils › Maresme | 23 |
| Forêt de Viladecans (2) | Viladecans › Baix Llobregat | 22 |
| Forêt de Sora (3) | Sora › Osona (Barcelone) | 22 |
| Forêt de Gallifa | Gallifa › Vallès Occidental | 22 |
| Forêt de Sant Iscle de Vallalta | Sant Iscle de Vallalta › Maresme | 22 |
| Forêt de Tordera (4) | Tordera › Maresme | 22 |
| Forêt de Vilanova de Sau (14) | Vilanova de Sau › Osona (Barcelone) | 22 |
| Forêt de Pujalt (5) | Pujalt › Anoia | 22 |
| Bois de Argentona (3) | Argentona › Maresme | 22 |
| Bois de Sant Just Desvern (2) | Sant Just Desvern › Baix Llobregat | 22 |
| Forêt de Piera (21) | Piera › Anoia | 22 |
| Forêt de Sant Celoni (16) | Sant Celoni › Vallès Oriental | 22 |
| Forêt de Matadepera (213) | Matadepera › Vallès Occidental | 22 |
| Forêt de Monistrol de Montserrat (7) | Monistrol de Montserrat › Bages | 22 |
| Forêt de Castellterçol (12) | Castellterçol › Moianès | 22 |
| Forêt de Sallent (33) | Sallent › Bages | 22 |
| Forêt de Rupit i Pruit (16) | Rupit i Pruit › Osona (Barcelone) | 22 |
| Forêt de Avinyó (58) | Avinyó › Bages | 22 |
| Forêt de Capolat (15) | Capolat › Berguedà | 22 |
| Forêt de Montmajor (69) | l'Espunyola › Berguedà | 22 |
| Forêt de Martorell (3) | Martorell › Baix Llobregat | 22 |
| Forêt de Santa Maria d'Oló (36) | Santa Maria d'Oló › Moianès | 22 |
| Forêt de Cercs (39) | Cercs › Berguedà | 22 |
| Forêt de la Pobla de Lillet (18) | la Pobla de Lillet › Berguedà | 22 |
| Forêt de Talamanca (29) | Talamanca › Bages | 22 |
| Forêt de Sant Salvador de Guardiola (71) | Sant Salvador de Guardiola › Bages | 22 |
| Forêt de Viver i Serrateix (32) | Viver i Serrateix › Berguedà | 22 |
| Forêt de Puig-reig (60) | Puig-reig › Berguedà | 22 |
| Forêt de Gaià (68) | Gaià › Bages | 22 |
| Forêt de Sant Feliu Sasserra (13) | Sant Feliu Sasserra › Bages | 22 |
| Forêt de Saldes (21) | Saldes › Berguedà | 22 |
| Forêt de Castellet i la Gornal (78) | Castellet i la Gornal › Alt Penedès | 22 |
| Forêt de Olèrdola (61) | Olèrdola › Alt Penedès | 22 |
| Forêt de Sant Cebrià de Vallalta (2) | Sant Cebrià de Vallalta › Maresme | 22 |
| Forêt de Sant Quirze Safaja (52) | Sant Quirze Safaja › Moianès | 22 |
| Forêt de Dosrius (26) | Dosrius › Maresme | 22 |
| Forêt de Guardiola de Berguedà (114) | Guardiola de Berguedà › Berguedà | 22 |
| Forêt de Prats de Lluçanès (24) | Prats de Lluçanès › Lluçanès | 22 |
| Forêt de Sant Jaume de Frontanyà (24) | Sant Jaume de Frontanyà › Berguedà | 22 |
| Forêt de Orís (22) | Orís › Osona (Barcelone) | 22 |
| Forêt de Pontons (13) | Pontons › Alt Penedès | 22 |
| Forêt de Badalona (30) | Badalona › Barcelonès | 22 |
| Forêt de Tiana (14) | Tiana › Maresme | 22 |
| Forêt de Alella (3) | Alella › Maresme | 22 |
| Forêt de Montmajor (141) | Montmajor › Berguedà | 22 |
| Forêt de la Pobla de Claramunt (21) | la Pobla de Claramunt › Anoia | 22 |
| Forêt de Sant Pere de Riudebitlles (2) | Sant Pere de Riudebitlles › Alt Penedès | 22 |
| Forêt de Font-rubí (23) | Font-rubí › Alt Penedès | 22 |
| Forêt de Puig-reig (87) | Puig-reig › Berguedà | 22 |
| Forêt de Tavertet (74) | Tavertet › Osona (Barcelone) | 22 |
| Forêt de Castellnou de Bages (55) | Castellnou de Bages › Bages | 22 |
| Forêt de Sant Julià de Vilatorta (9) | Sant Julià de Vilatorta › Osona (Barcelone) | 22 |
| Forêt de Sant Sadurní d'Osormort (49) | Sant Sadurní d'Osormort › Osona (Barcelone) | 22 |
| Forêt de Sant Climent de Llobregat | Sant Climent de Llobregat › Baix Llobregat | 21 |
| Forêt de Alpens | Alpens › Lluçanès | 21 |
| Forêt de Sant Celoni (3) | Sant Celoni › Vallès Oriental | 21 |
| Forêt de Vilanova de Sau (6) | Vilanova de Sau › Osona (Barcelone) | 21 |
| Forêt de Castellfollit de Riubregós (2) | Castellfollit de Riubregós › Anoia | 21 |
| Forêt de Jorba | Jorba › Anoia | 21 |
| Forêt de Castellfollit de Riubregós (3) | Castellfollit de Riubregós › Anoia | 21 |
| Forêt de Castellfollit del Boix (4) | Castellfollit del Boix › Bages | 21 |
| Forêt de Sant Climent de Llobregat (4) | Sant Climent de Llobregat › Baix Llobregat | 21 |
| Bois de Vilassar de Dalt (2) | Vilassar de Dalt › Maresme | 21 |
| Bois de Òrrius (10) | Òrrius › Maresme | 21 |
| Bois de la Roca del Vallès (5) | la Roca del Vallès › Vallès Oriental | 21 |
| Bois de Òrrius (18) | Òrrius › Maresme | 21 |
| Bois de Argentona (8) | Argentona › Maresme | 21 |
| Forêt de Rubió (6) | Rubió › Anoia | 21 |
| Forêt de Seva (8) | Seva › Osona (Barcelone) | 21 |
| Forêt de Sant Pere de Vilamajor (73) | Sant Pere de Vilamajor › Vallès Oriental | 21 |
| Forêt de Rajadell (10) | Rajadell › Bages | 21 |
| Forêt de les Masies de Roda (3) | les Masies de Roda › Osona (Barcelone) | 21 |
| Forêt de les Masies de Roda (5) | les Masies de Roda › Osona (Barcelone) | 21 |
| Forêt de Manresa (71) | Manresa › Bages | 21 |
| Forêt de Aiguafreda (11) | Aiguafreda › Osona (Barcelone) | 21 |
| Forêt de Rajadell (37) | Rajadell › Bages | 21 |
| Forêt de Sabadell (81) | Sabadell › Vallès Occidental | 21 |
| Forêt de Castellbell i el Vilar (4) | Castellbell i el Vilar › Bages | 21 |
| Bosc de Ca n'Enrani | les Franqueses del Vallès › Vallès Oriental | 21 |
| Forêt de Sitges (49) | Sitges › Garraf | 21 |
| Forêt de Manresa (121) | Manresa › Bages | 21 |
| Forêt de Sant Esteve de Palautordera (11) | Sant Esteve de Palautordera › Vallès Oriental | 21 |
| Forêt de Castellar de n'Hug (15) | Castellar de n'Hug › Berguedà | 21 |
| Forêt de Navàs (54) | Navàs › Bages | 21 |
| Forêt de Montmajor (118) | Montmajor › Berguedà | 21 |
| Forêt de Santa Maria de Merlès (57) | Santa Maria de Merlès › Berguedà | 21 |
| Forêt de Borredà (31) | Borredà › Berguedà | 21 |
| Forêt de Sant Pere de Ribes (91) | Sant Pere de Ribes › Garraf | 21 |
| Forêt de Castellet i la Gornal (77) | Castellet i la Gornal › Alt Penedès | 21 |
| Forêt de Guardiola de Berguedà (64) | Guardiola de Berguedà › Berguedà | 21 |
| Forêt de Taradell (10) | Taradell › Osona (Barcelone) | 21 |
| Forêt de Muntanyola (21) | Muntanyola › Osona (Barcelone) | 21 |
| Forêt de Sant Quirze Safaja (11) | Sant Quirze Safaja › Moianès | 21 |
| Forêt de Fogars de Montclús (14) | Fogars de Montclús › Vallès Oriental | 21 |
| Forêt de Mataró (6) | Mataró › Maresme | 21 |
| Forêt de Dosrius (21) | Dosrius › Maresme | 21 |
| Forêt de Saldes (44) | Saldes › Berguedà | 21 |
| Forêt de Borredà (101) | Borredà › Berguedà | 21 |
| Forêt de Gisclareny (59) | Gisclareny › Berguedà | 21 |
| Forêt de Fogars de la Selva (20) | Fogars de la Selva › la Selva (Barcelone) | 21 |
| Forêt de Piera (29) | Piera › Anoia | 21 |
| Bois de Torrelles de Foix (6) | Torrelles de Foix › Alt Penedès | 21 |
| Forêt de Castellar de n'Hug (30) | Castellar de n'Hug › Berguedà | 21 |
| Forêt de Castellar de n'Hug (44) | Castellar de n'Hug › Berguedà | 21 |
| Forêt de Vallirana (36) | Vallirana › Baix Llobregat | 21 |
| Forêt de la Llacuna (12) | la Llacuna › Anoia | 21 |
| Forêt de Piera (54) | Piera › Anoia | 21 |
| Forêt de Mediona (86) | Mediona › Alt Penedès | 21 |
| Forêt de Lluçà (67) | Lluçà › Lluçanès | 21 |
| Forêt de Sant Cebrià de Vallalta (8) | Sant Cebrià de Vallalta › Maresme | 21 |
| Forêt de Sant Vicenç de Montalt (12) | Sant Vicenç de Montalt › Maresme | 21 |
| Forêt de Sant Celoni (36) | Sant Celoni › Vallès Oriental | 21 |
| Forêt de Sant Celoni (43) | Sant Celoni › Vallès Oriental | 21 |
| Forêt de Fogars de la Selva (28) | Fogars de la Selva › la Selva (Barcelone) | 21 |
| Forêt de Gualba (15) | Gualba › Vallès Oriental | 21 |
| Forêt de Santpedor (30) | Santpedor › Bages | 21 |
| Forêt de Fonollosa (153) | Fonollosa › Bages | 21 |
| Forêt de Talamanca (40) | Talamanca › Bages | 21 |
| Forêt de Bigues i Riells del Fai | Bigues i Riells del Fai › Vallès Oriental | 20 |
| Forêt de les Masies de Voltregà | les Masies de Voltregà › Osona (Barcelone) | 20 |
| Forêt de Terrassa (2) | Terrassa › Vallès Occidental | 20 |
| Forêt de Calonge de Segarra (3) | Calonge de Segarra › Anoia | 20 |
| Forêt de Pujalt (4) | Pujalt › Anoia | 20 |
| Forêt de Torrelavit (23) | Torrelavit › Alt Penedès | 20 |
| Forêt de el Brull (10) | el Brull › Osona (Barcelone) | 20 |
| Bois de la Roca del Vallès (38) | la Roca del Vallès › Vallès Oriental | 20 |
| Forêt de Tavèrnoles (3) | Tavèrnoles › Osona (Barcelone) | 20 |
| Forêt de Balsareny (29) | Balsareny › Bages | 20 |
| Forêt de Manresa (29) | Manresa › Bages | 20 |
| Forêt de Olvan (8) | Olvan › Berguedà | 20 |
| Forêt de Berga (8) | Berga › Berguedà | 20 |
| Forêt de Abrera (11) | Abrera › Baix Llobregat | 20 |
| Forêt de Sant Salvador de Guardiola (41) | Sant Salvador de Guardiola › Bages | 20 |
| Forêt de Castellbell i el Vilar (35) | Castellbell i el Vilar › Bages | 20 |
| Forêt de Avinyó (79) | Avinyó › Bages | 20 |
| Forêt de Puig-reig (52) | Puig-reig › Berguedà | 20 |
| Forêt de Gaià (36) | Gaià › Bages | 20 |
| Forêt de Castell de l'Areny (26) | Castell de l'Areny › Berguedà | 20 |
| Forêt de Castellar del Riu (21) | Castellar del Riu › Berguedà | 20 |
| Forêt de Montesquiu (3) | Montesquiu › Osona (Barcelone) | 20 |
| Forêt de Guardiola de Berguedà (45) | Guardiola de Berguedà › Berguedà | 20 |
| Forêt de Mura (30) | Mura › Bages | 20 |
| Forêt de Sant Salvador de Guardiola (115) | Sant Salvador de Guardiola › Bages | 20 |
| Forêt de Olvan (20) | Olvan › Berguedà | 20 |
| Forêt de Avià (19) | Avià › Berguedà | 20 |
| Forêt de Avià (38) | Avià › Berguedà | 20 |
| Forêt de Gaià (57) | Gaià › Bages | 20 |
| Bois de Òrrius (25) | Òrrius › Maresme | 20 |
| Forêt de Borredà (25) | Borredà › Berguedà | 20 |
| Bois de Castellar del Vallès | Castellar del Vallès › Vallès Occidental | 20 |
| Forêt de Olivella (102) | Olivella › Garraf | 20 |
| Forêt de Monistrol de Calders (26) | Monistrol de Calders › Moianès | 20 |
| Forêt de Castellar de n'Hug (17) | Castellar de n'Hug › Berguedà | 20 |
| Forêt de Muntanyola (19) | Muntanyola › Osona (Barcelone) | 20 |
| Forêt de Centelles (6) | Centelles › Osona (Barcelone) | 20 |
| Forêt de Sant Martí de Centelles (63) | Sant Martí de Centelles › Osona (Barcelone) | 20 |
| Forêt de Sant Quirze Safaja (37) | Sant Quirze Safaja › Moianès | 20 |
| Forêt de Oristà (113) | Oristà › Lluçanès | 20 |
| Forêt de Dosrius (31) | Dosrius › Maresme | 20 |
| Forêt de Saldes (29) | Saldes › Berguedà | 20 |
| Forêt de Fígols (24) | Fígols › Berguedà | 20 |
| Forêt de la Pobla de Lillet (39) | la Pobla de Lillet › Berguedà | 20 |
| Forêt de Barcelona (60) | Barcelona › Barcelonès | 20 |
| Forêt de Sant Fost de Campsentelles (14) | Sant Fost de Campsentelles › Vallès Oriental | 20 |
| Forêt de Begues (82) | Begues › Baix Llobregat | 20 |
| Forêt de Mediona (11) | Mediona › Alt Penedès | 20 |
| Forêt de Sant Sadurní d'Anoia (26) | Sant Sadurní d'Anoia › Alt Penedès | 20 |
| Forêt de Sant Cugat del Vallès (159) | Sant Cugat del Vallès › Vallès Occidental | 20 |
| Forêt de Sant Andreu de Llavaneres (8) | Sant Andreu de Llavaneres › Maresme | 20 |
| Forêt de Sant Cugat del Vallès (163) | Sant Cugat del Vallès › Vallès Occidental | 20 |
| Forêt de Callús (25) | Callús › Bages | 20 |
| Forêt de Sant Joan de Vilatorrada (75) | Sant Joan de Vilatorrada › Bages | 20 |
| Forêt de Vallcebre (72) | Vallcebre › Berguedà | 20 |
| Forêt de Sant Sadurní d'Osormort (51) | Sant Sadurní d'Osormort › Osona (Barcelone) | 20 |
| Forêt de Malla | Malla › Osona (Barcelone) | 19 |
| Forêt de Copons | Copons › Anoia | 19 |
| Forêt de Castellar del Vallès | Castellar del Vallès › Vallès Occidental | 19 |
| Forêt de Balenyà | Balenyà › Osona (Barcelone) | 19 |
| Forêt de Sant Pere de Torelló (4) | Sant Pere de Torelló › Osona (Barcelone) | 19 |
| Forêt de Santa Maria de Miralles | Santa Maria de Miralles › Anoia | 19 |
| Forêt de Argençola (16) | Argençola › Anoia | 19 |
| Bois de Premià de Dalt (2) | Premià de Dalt › Maresme | 19 |
| Bois de Llinars del Vallès (23) | Llinars del Vallès › Vallès Oriental | 19 |
| Forêt de Tavertet (4) | Tavertet › Osona (Barcelone) | 19 |
| Forêt de Sant Pere de Ribes (72) | Sant Pere de Ribes › Garraf | 19 |
| Forêt de Sant Esteve de Palautordera (2) | Sant Esteve de Palautordera › Vallès Oriental | 19 |
| Forêt de Cànoves i Samalús (27) | Cànoves i Samalús › Vallès Oriental | 19 |
| Forêt de Matadepera (207) | Matadepera › Vallès Occidental | 19 |
| Forêt de Balsareny (39) | Balsareny › Bages | 19 |
| Forêt de Montmajor (30) | Montmajor › Berguedà | 19 |
| Forêt de Viladecavalls (3) | Viladecavalls › Vallès Occidental | 19 |
| Forêt de la Torre de Claramunt (4) | la Torre de Claramunt › Anoia | 19 |
| Forêt de Navàs (26) | Navàs › Bages | 19 |
| Forêt de Montmajor (73) | Montmajor › Berguedà | 19 |
| Forêt de Guardiola de Berguedà (35) | Guardiola de Berguedà › Berguedà | 19 |
| Forêt de Castellbell i el Vilar (43) | Castellbell i el Vilar › Bages | 19 |
| Forêt de Sant Vicenç de Castellet (17) | Sant Vicenç de Castellet › Bages | 19 |
| Forêt de Sant Salvador de Guardiola (47) | Sant Salvador de Guardiola › Bages | 19 |
| Forêt de Avinyó (78) | Avinyó › Bages | 19 |
| Forêt de el Pont de Vilomara i Rocafort (25) | el Pont de Vilomara i Rocafort › Bages | 19 |
| Forêt de el Pont de Vilomara i Rocafort (26) | el Pont de Vilomara i Rocafort › Bages | 19 |
| Forêt de Talamanca (15) | Talamanca › Bages | 19 |
| Forêt de Sant Salvador de Guardiola (113) | Sant Salvador de Guardiola › Bages | 19 |
| Forêt de Olesa de Montserrat (23) | Olesa de Montserrat › Baix Llobregat | 19 |
| Forêt de Navàs (58) | Navàs › Bages | 19 |
| Forêt de l'Espunyola (51) | l'Espunyola › Berguedà | 19 |
| Forêt de Viver i Serrateix (70) | Viver i Serrateix › Berguedà | 19 |
| Forêt de Viver i Serrateix (83) | Viver i Serrateix › Berguedà | 19 |
| Forêt de Copons (6) | Copons › Anoia | 19 |
| Forêt de Castellfollit del Boix (34) | Castellfollit del Boix › Bages | 19 |
| Forêt de Cubelles (20) | Cubelles › Garraf | 19 |
| Forêt de Olesa de Bonesvalls (42) | Olesa de Bonesvalls › Alt Penedès | 19 |
| Forêt de Bagà (27) | Bagà › Berguedà | 19 |
| Forêt de Tavertet (33) | Tavertet › Osona (Barcelone) | 19 |
| Forêt de Avià (48) | Avià › Berguedà | 19 |
| Forêt de la Quar (25) | la Quar › Berguedà | 19 |
| Forêt de els Hostalets de Pierola (24) | els Hostalets de Pierola › Anoia | 19 |
| Forêt de Tagamanent (16) | Tagamanent › Vallès Oriental | 19 |
| Forêt de Sant Martí de Centelles (60) | Sant Martí de Centelles › Osona (Barcelone) | 19 |
| Forêt de Montseny (7) | Montseny › Vallès Oriental | 19 |
| Forêt de Sant Quirze Safaja (16) | Sant Quirze Safaja › Moianès | 19 |
| Forêt de Santa Eulàlia de Riuprimer (26) | Santa Eulàlia de Riuprimer › Osona (Barcelone) | 19 |
| Forêt de Oristà (117) | Oristà › Lluçanès | 19 |
| Forêt de Santa Maria de Merlès (125) | Sant Feliu Sasserra › Bages | 19 |
| Forêt de Vallgorguina | Vilalba Sasserra › Vallès Oriental | 19 |
| Forêt de Vallgorguina (8) | Vallgorguina › Vallès Oriental | 19 |
| Forêt de Guardiola de Berguedà (68) | Guardiola de Berguedà › Berguedà | 19 |
| Forêt de Santa Maria de Palautordera (29) | Santa Maria de Palautordera › Vallès Oriental | 19 |
| Forêt de Gisclareny (29) | Gisclareny › Berguedà | 19 |
| Forêt de Olvan (35) | Olvan › Berguedà | 19 |
| Forêt de Gisclareny (33) | Gisclareny › Berguedà | 19 |
| Forêt de Bagà (64) | Bagà › Berguedà | 19 |
| Forêt de la Quar (39) | la Quar › Berguedà | 19 |
| Forêt de Barcelona (61) | Barcelona › Barcelonès | 19 |
| Forêt de Sant Martí de Tous (46) | Sant Martí de Tous › Anoia | 19 |
| Forêt de Sant Martí de Tous (47) | Sant Martí de Tous › Anoia | 19 |
| Forêt de Castellar de n'Hug (40) | Castellar de n'Hug › Berguedà | 19 |
| Forêt de Oristà (157) | Oristà › Lluçanès | 19 |
| Forêt de Abrera (35) | Abrera › Baix Llobregat | 19 |
| Forêt de Mediona (88) | Mediona › Alt Penedès | 19 |
| Forêt de Òdena (102) | Òdena › Anoia | 19 |
| Forêt de Lluçà (55) | Borredà › Berguedà | 19 |
| Forêt de Lluçà (80) | Lluçà › Lluçanès | 19 |
| Forêt de Pineda de Mar (2) | Pineda de Mar › Maresme | 19 |
| Forêt de Sant Andreu de Llavaneres (6) | Sant Andreu de Llavaneres › Maresme | 19 |
| Forêt de Sant Vicenç de Montalt (6) | Sant Vicenç de Montalt › Maresme | 19 |
| Forêt de Sant Celoni (42) | Sant Celoni › Vallès Oriental | 19 |
| Forêt de Fogars de la Selva (27) | Fogars de la Selva › la Selva (Barcelone) | 19 |
| Forêt de Gualba (24) | Gualba › Vallès Oriental | 19 |
| Forêt de Sant Celoni (71) | Sant Celoni › Vallès Oriental | 19 |
| Forêt de Castellnou de Bages (53) | Castellnou de Bages › Bages | 19 |
| Forêt de Folgueroles (9) | Folgueroles › Osona (Barcelone) | 19 |
| Bois de els Hostalets de Pierola (4) | els Hostalets de Pierola › Anoia | 19 |
| Forêt de Gurb (33) | Gurb › Osona (Barcelone) | 19 |
| Forêt de Sant Quirze Safaja (57) | Sant Quirze Safaja › Moianès | 19 |
| Forêt de el Pont de Vilomara i Rocafort (50) | el Pont de Vilomara i Rocafort › Bages | 19 |
| Forêt de Moià | Moià › Moianès | 18 |
| Forêt de Sant Celoni (2) | Sant Celoni › Vallès Oriental | 18 |
| Forêt de els Hostalets de Pierola (4) | els Hostalets de Pierola › Anoia | 18 |
| Forêt de Rupit i Pruit (8) | Rupit i Pruit › Osona (Barcelone) | 18 |
| Forêt de els Hostalets de Pierola (7) | els Hostalets de Pierola › Anoia | 18 |
| Forêt de Sant Climent de Llobregat (9) | Sant Climent de Llobregat › Baix Llobregat | 18 |
| Forêt de Subirats (82) | Subirats › Alt Penedès | 18 |
| Bois de Cabrils (3) | Cabrils › Maresme | 18 |
| Bois de Cabrils (7) | Cabrils › Maresme | 18 |
| Bois de Vallromanes (6) | Vallromanes › Vallès Oriental | 18 |
| Forêt de Viver i Serrateix (11) | Viver i Serrateix › Berguedà | 18 |
| Forêt de Sant Martí de Tous (8) | Sant Martí de Tous › Anoia | 18 |
| Bois de Veciana (3) | Veciana › Anoia | 18 |
| Forêt de Font-rubí (15) | Font-rubí › Alt Penedès | 18 |
| Forêt de Palafolls (25) | Palafolls › Maresme | 18 |
| Forêt de Sant Pere de Vilamajor (72) | Sant Pere de Vilamajor › Vallès Oriental | 18 |
| Forêt de Fogars de Montclús (12) | Fogars de Montclús › Vallès Oriental | 18 |
| Forêt de Fogars de Montclús (13) | Fogars de Montclús › Vallès Oriental | 18 |
| Forêt de Callús (10) | Callús › Bages | 18 |
| Forêt de Castellar del Vallès (14) | Castellar del Vallès › Vallès Occidental | 18 |
| Bois de Viladecavalls (5) | Viladecavalls › Vallès Occidental | 18 |
| Forêt de Balsareny (51) | Balsareny › Bages | 18 |
| Forêt de Balsareny (58) | Balsareny › Bages | 18 |
| Forêt de Capolat (9) | Capolat › Berguedà | 18 |
| Forêt de Puig-reig (19) | Puig-reig › Berguedà | 18 |
| Forêt de Guardiola de Berguedà (21) | Guardiola de Berguedà › Berguedà | 18 |
| Forêt de Esparreguera (18) | Esparreguera › Baix Llobregat | 18 |
| Forêt de Marganell (11) | Marganell › Bages | 18 |
| Forêt de Sant Vicenç de Castellet (19) | Sant Vicenç de Castellet › Bages | 18 |
| Forêt de Castell de l'Areny (6) | Castell de l'Areny › Berguedà | 18 |
| Forêt de Castell de l'Areny (8) | Castell de l'Areny › Berguedà | 18 |
| Forêt de la Pobla de Lillet (22) | la Pobla de Lillet › Berguedà | 18 |
| Forêt de Mura (28) | Mura › Bages | 18 |
| Forêt de Talamanca (24) | Talamanca › Bages | 18 |
| Forêt de Sant Vicenç de Castellet (32) | Sant Vicenç de Castellet › Bages | 18 |
| Forêt de Rajadell (40) | Rajadell › Bages | 18 |
| Forêt de Castellbisbal (14) | Castellbisbal › Vallès Occidental | 18 |
| Forêt de Navàs (88) | Navàs › Bages | 18 |
| Forêt de Viver i Serrateix (30) | Viver i Serrateix › Berguedà | 18 |
| Forêt de Puig-reig (63) | Puig-reig › Berguedà | 18 |
| Forêt de Puig-reig (64) | Puig-reig › Berguedà | 18 |
| Forêt de Avià (25) | Avià › Berguedà | 18 |
| Forêt de Avià (28) | Avià › Berguedà | 18 |
| Forêt de Montclar (26) | Montclar › Berguedà | 18 |
| Forêt de Navàs (133) | Navàs › Bages | 18 |
| Forêt de Gaià (61) | Gaià › Bages | 18 |
| Forêt de Gaià (64) | Gaià › Bages | 18 |
| Forêt de Rajadell (57) | Rajadell › Bages | 18 |
| Forêt de Olivella (107) | Olivella › Garraf | 18 |
| Forêt de Olesa de Bonesvalls (46) | Olesa de Bonesvalls › Alt Penedès | 18 |
| Forêt de Olivella (115) | Olivella › Garraf | 18 |
| Forêt de Canyelles (14) | Canyelles › Garraf | 18 |
| Forêt de Bagà (31) | Bagà › Berguedà | 18 |
| Forêt de la Quar (14) | la Quar › Berguedà | 18 |
| Forêt de Muntanyola (17) | Muntanyola › Osona (Barcelone) | 18 |
| Forêt de el Brull (22) | el Brull › Osona (Barcelone) | 18 |
| Forêt de Sant Martí de Centelles (52) | Sant Martí de Centelles › Osona (Barcelone) | 18 |
| Forêt de Figaró-Montmany (9) | Figaró-Montmany › Vallès Oriental | 18 |
| Forêt de Sant Quirze Safaja (45) | Sant Quirze Safaja › Moianès | 18 |
| Forêt de Arenys de Munt (7) | Arenys de Munt › Maresme | 18 |
| Forêt de Saldes (37) | Saldes › Berguedà | 18 |
| Forêt de Saldes (99) | Saldes › Berguedà | 18 |
| Forêt de Centelles (34) | Centelles › Osona (Barcelone) | 18 |
| Forêt de Tordera (62) | Tordera › Maresme | 18 |
| Forêt de Castellar de n'Hug (55) | Castellar de n'Hug › Berguedà | 18 |
| Forêt de Begues (79) | Begues › Baix Llobregat | 18 |
| Forêt de Terrassa (88) | Terrassa › Vallès Occidental | 18 |
| Forêt de Sant Quintí de Mediona (11) | Sant Quintí de Mediona › Alt Penedès | 18 |
| Forêt de Mediona (84) | Mediona › Alt Penedès | 18 |
| Forêt de Torrelles de Foix | Torrelles de Foix › Alt Penedès | 18 |
| Forêt de Lluçà (71) | Lluçà › Lluçanès | 18 |
| Forêt de Lluçà (75) | Lluçà › Lluçanès | 18 |
| Forêt de Arenys de Munt (17) | Arenys de Munt › Maresme | 18 |
| Forêt de Sant Andreu de Llavaneres (7) | Sant Andreu de Llavaneres › Maresme | 18 |
| Forêt de Sallent (129) | Sallent › Bages | 18 |
| Muntanya de Sant Pau i Sant Jaume | Pacs del Penedès › Alt Penedès | 18 |
| Forêt de Sant Sadurní d'Osormort (36) | Sant Sadurní d'Osormort › Osona (Barcelone) | 18 |
| Forêt de Vilanova de Sau (67) | Vilanova de Sau › Osona (Barcelone) | 18 |
| Forêt de Seva (38) | Seva › Osona (Barcelone) | 18 |
| Forêt de Bellprat (4) | Bellprat › Anoia | 17 |
| Forêt de Santa Maria de Martorelles | Santa Maria de Martorelles › Vallès Oriental | 17 |
| Forêt de la Quar (2) | la Quar › Berguedà | 17 |
| Forêt de Sant Sadurní d'Osormort (6) | Sant Sadurní d'Osormort › Osona (Barcelone) | 17 |
| Forêt de Sant Fost de Campsentelles | Sant Fost de Campsentelles › Vallès Oriental | 17 |
| Forêt de Seva (3) | Seva › Osona (Barcelone) | 17 |
| Forêt de el Pla del Penedès | el Pla del Penedès › Alt Penedès | 17 |
| Forêt de Fogars de Montclús (5) | Fogars de Montclús › Vallès Oriental | 17 |
| Forêt de Sant Pere de Ribes (16) | Sant Pere de Ribes › Garraf | 17 |
| Bois de Argentona (10) | Argentona › Maresme | 17 |
| Forêt de Sant Llorenç Savall (10) | Sant Llorenç Savall › Vallès Occidental | 17 |
| Forêt de Viver i Serrateix (14) | Viver i Serrateix › Berguedà | 17 |
| Forêt de Olèrdola (57) | Olèrdola › Alt Penedès | 17 |
| Forêt de Tagamanent (7) | Tagamanent › Vallès Oriental | 17 |
| Forêt de Montseny (6) | Montseny › Vallès Oriental | 17 |
| Forêt de Calders (7) | Calders › Moianès | 17 |
| Forêt de Sallent (45) | Sallent › Bages | 17 |
| Forêt de Artés (10) | Artés › Bages | 17 |
| Forêt de Calders (26) | Calders › Moianès | 17 |
| Forêt de Tona | Tona › Osona (Barcelone) | 17 |
| Forêt de Masquefa (13) | Masquefa › Anoia | 17 |
| Forêt de Sallent (52) | Sallent › Bages | 17 |
| Forêt de Montmajor (74) | Montmajor › Berguedà | 17 |
| Forêt de Sant Vicenç de Castellet (5) | Sant Vicenç de Castellet › Bages | 17 |
| Forêt de Òdena (38) | Òdena › Anoia | 17 |
| Forêt de les Franqueses del Vallès (47) | les Franqueses del Vallès › Vallès Oriental | 17 |
| Bois de Vilanova del Vallès (12) | Vilanova del Vallès › Vallès Oriental | 17 |
| Forêt de Guardiola de Berguedà (50) | Guardiola de Berguedà › Berguedà | 17 |
| Forêt de Guardiola de Berguedà (55) | Guardiola de Berguedà › Berguedà | 17 |
| Forêt de Castellfollit del Boix (22) | Castellfollit del Boix › Bages | 17 |
| Forêt de Sant Salvador de Guardiola (101) | Sant Salvador de Guardiola › Bages | 17 |
| Forêt de Vacarisses (57) | Vacarisses › Vallès Occidental | 17 |
| Forêt de Viver i Serrateix (44) | Viver i Serrateix › Berguedà | 17 |
| Forêt de Puig-reig (72) | Puig-reig › Berguedà | 17 |
| Forêt de Navàs (130) | Navàs › Bages | 17 |
| Forêt de Montmajor (113) | Montmajor › Berguedà | 17 |
| Bois de Barcelona (108) | Barcelona › Barcelonès | 17 |
| Forêt de Tordera (51) | Tordera › Maresme | 17 |
| Forêt de Castellfollit del Boix (31) | Castellfollit del Boix › Bages | 17 |
| Forêt de Sant Pere de Ribes (89) | Sant Pere de Ribes › Garraf | 17 |
| Forêt de Sant Pere de Ribes (96) | Olivella › Garraf | 17 |
| Forêt de Canyelles (10) | Canyelles › Garraf | 17 |
| Forêt de Vilanova i la Geltrú (37) | Vilanova i la Geltrú › Garraf | 17 |
| Forêt de Vilanova i la Geltrú (40) | Vilanova i la Geltrú › Garraf | 17 |
| Forêt de Bagà (17) | Bagà › Berguedà | 17 |
| Forêt de Sant Jaume de Frontanyà (18) | Sant Jaume de Frontanyà › Berguedà | 17 |
| Forêt de Borredà (53) | Borredà › Berguedà | 17 |
| Forêt de Santa Maria de Merlès (81) | Santa Maria de Merlès › Berguedà | 17 |
| Forêt de la Quar (24) | la Quar › Berguedà | 17 |
| Forêt de Santa Maria d'Oló (52) | Santa Maria d'Oló › Moianès | 17 |
| Forêt de Fogars de Montclús (18) | Fogars de Montclús › Vallès Oriental | 17 |
| Forêt de Sant Quirze Safaja (35) | Sant Quirze Safaja › Moianès | 17 |
| Forêt de Santa Maria d'Oló (75) | Santa Maria d'Oló › Moianès | 17 |
| Forêt de Cardona (83) | Cardona › Bages | 17 |
| Forêt de Cardona (98) | Cardona › Bages | 17 |
| Bois de Argentona (52) | Argentona › Maresme | 17 |
| Forêt de Saldes (48) | Saldes › Berguedà | 17 |
| Forêt de Fígols (23) | Fígols › Berguedà | 17 |
| Forêt de la Pobla de Lillet (45) | la Pobla de Lillet › Berguedà | 17 |
| Forêt de Gisclareny (45) | Gisclareny › Berguedà | 17 |
| Forêt de Gisclareny (51) | Gisclareny › Berguedà | 17 |
| Forêt de Saldes (92) | Saldes › Berguedà | 17 |
| Forêt de Puig-reig (84) | Puig-reig › Berguedà | 17 |
| Forêt de Saldes (133) | Saldes › Berguedà | 17 |
| Forêt de Piera (25) | Piera › Anoia | 17 |
| Forêt de Piera (30) | Piera › Anoia | 17 |
| Forêt de Begues (80) | Begues › Baix Llobregat | 17 |
| Forêt de Torrelavit (25) | Torrelavit › Alt Penedès | 17 |
| Forêt de Mediona (87) | Mediona › Alt Penedès | 17 |
| Forêt de Lluçà (72) | Lluçà › Lluçanès | 17 |
| Forêt de Lluçà (81) | Lluçà › Lluçanès | 17 |
| Forêt de Santa Susanna (4) | Santa Susanna › Maresme | 17 |
| Forêt de Seva (37) | Seva › Osona (Barcelone) | 17 |
| Forêt de Sant Julià de Vilatorta (16) | Sant Julià de Vilatorta › Osona (Barcelone) | 17 |
| Forêt de Cabrera de Mar (3) | Cabrera de Mar › Maresme | 17 |
| Forêt de Orís (31) | Orís › Osona (Barcelone) | 17 |
| Forêt de Cabrera de Mar (5) | Cabrera de Mar › Maresme | 17 |
| Parc del Mirador del Migdia | Barcelona › Barcelonès | 16 |
| Forêt de Sobremunt | Sobremunt › Lluçanès | 16 |
| Forêt de Collsuspina (2) | Collsuspina › Moianès | 16 |
| Forêt de Borredà (2) | Borredà › Berguedà | 16 |
| Forêt de Muntanyola (2) | Muntanyola › Osona (Barcelone) | 16 |
| Forêt de Castellet i la Gornal (2) | Castellet i la Gornal › Alt Penedès | 16 |
| Forêt de Perafita (4) | Perafita › Lluçanès | 16 |
| Forêt de Òdena (2) | Òdena › Anoia | 16 |
| Forêt de Castellfollit del Boix (3) | Castellfollit del Boix › Bages | 16 |
| Forêt de Sant Agustí de Lluçanès (5) | Sant Agustí de Lluçanès › Osona (Barcelone) | 16 |
| Forêt de Tagamanent (2) | Tagamanent › Vallès Oriental | 16 |
| Bois de Argentona (21) | Argentona › Maresme | 16 |
| Bois de la Roca del Vallès (25) | la Roca del Vallès › Vallès Oriental | 16 |
| Bois de la Roca del Vallès (35) | la Roca del Vallès › Vallès Oriental | 16 |
| Bois de Argentona (44) | Argentona › Maresme | 16 |
| Forêt de Terrassa (35) | Terrassa › Vallès Occidental | 16 |
| Forêt de Terrassa (55) | Terrassa › Vallès Occidental | 16 |
| Bois de Veciana (10) | Veciana › Anoia | 16 |
| Forêt de el Brull (5) | el Brull › Osona (Barcelone) | 16 |
| Forêt de Sant Martí Sarroca (29) | Sant Martí Sarroca › Alt Penedès | 16 |
| Forêt de Fogars de la Selva (10) | Fogars de la Selva › la Selva (Barcelone) | 16 |
| Forêt de l'Espunyola (9) | l'Espunyola › Berguedà | 16 |
| Forêt de Monistrol de Calders (7) | Monistrol de Calders › Moianès | 16 |
| Forêt de Sant Fruitós de Bages (19) | Sant Fruitós de Bages › Bages | 16 |
| Forêt de Calders (14) | Calders › Moianès | 16 |
| Bois de Viladecavalls (6) | Viladecavalls › Vallès Occidental | 16 |
| Forêt de Bagà (5) | Bagà › Berguedà | 16 |
| Forêt de Aiguafreda (9) | Aiguafreda › Osona (Barcelone) | 16 |
| Forêt de Saldes (13) | Saldes › Berguedà | 16 |
| Bosc del Forn de Can Rovira | Lliçà d'Amunt › Vallès Oriental | 16 |
| Forêt de Montmajor (67) | Montmajor › Berguedà | 16 |
| Forêt de Oristà (94) | Oristà › Lluçanès | 16 |
| Forêt de Sant Feliu Sasserra (9) | Sant Feliu Sasserra › Bages | 16 |
| Forêt de Rubí (72) | Rubí › Vallès Occidental | 16 |
| Forêt de Vacarisses (49) | Vacarisses › Vallès Occidental | 16 |
| Forêt de Gavà (78) | Gavà › Baix Llobregat | 16 |
| Forêt de Llinars del Vallès (58) | Llinars del Vallès › Vallès Oriental | 16 |
| Forêt de Gaià (47) | Gaià › Bages | 16 |
| Forêt de Castell de l'Areny (7) | Castell de l'Areny › Berguedà | 16 |
| Forêt de Castellar del Riu (20) | Castellar del Riu › Berguedà | 16 |
| Forêt de la Pobla de Lillet (21) | la Pobla de Lillet › Berguedà | 16 |
| Forêt de Castellar de n'Hug (10) | Castellar de n'Hug › Berguedà | 16 |
| Forêt de la Pobla de Lillet (34) | la Pobla de Lillet › Berguedà | 16 |
| Forêt de Talamanca (30) | Talamanca › Bages | 16 |
| Forêt de Sant Pere Sallavinera (36) | Sant Pere Sallavinera › Anoia | 16 |
| Forêt de Sant Pere Sallavinera (37) | Sant Pere Sallavinera › Anoia | 16 |
| Forêt de Sant Salvador de Guardiola (108) | Sant Salvador de Guardiola › Bages | 16 |
| Forêt de Viver i Serrateix (31) | Viver i Serrateix › Berguedà | 16 |
| Forêt de Puig-reig (66) | Puig-reig › Berguedà | 16 |
| Forêt de Puig-reig (70) | Puig-reig › Berguedà | 16 |
| Forêt de Santa Maria de Merlès (15) | Santa Maria de Merlès › Berguedà | 16 |
| Forêt de Santa Maria de Merlès (24) | Santa Maria de Merlès › Berguedà | 16 |
| Forêt de Montmajor (114) | Montmajor › Berguedà | 16 |
| Forêt de Gaià (62) | Gaià › Bages | 16 |
| Forêt de Santa Maria de Merlès (25) | Santa Maria de Merlès › Berguedà | 16 |
| Forêt de Sant Fost de Campsentelles (7) | Sant Fost de Campsentelles › Vallès Oriental | 16 |
| Forêt de Cubelles (19) | Cubelles › Garraf | 16 |
| Forêt de Begues (64) | Begues › Baix Llobregat | 16 |
| Forêt de Avinyonet del Penedès (59) | Avinyonet del Penedès › Alt Penedès | 16 |
| Forêt de Olivella (120) | Olivella › Garraf | 16 |
| Forêt de Sant Julià de Cerdanyola (12) | Sant Julià de Cerdanyola › Berguedà | 16 |
| Forêt de Santa Maria de Merlès (83) | Santa Maria de Merlès › Berguedà | 16 |
| Forêt de la Quar (16) | la Quar › Berguedà | 16 |
| Forêt de Sant Bartomeu del Grau (13) | Sant Bartomeu del Grau › Osona (Barcelone) | 16 |
| Forêt de Centelles (7) | Centelles › Osona (Barcelone) | 16 |
| Forêt de Santa Maria d'Oló (67) | Santa Maria d'Oló › Moianès | 16 |
| Forêt de Saldes (34) | Saldes › Berguedà | 16 |
| Forêt de Saldes (64) | Saldes › Berguedà | 16 |
| Forêt de Bagà (52) | Bagà › Berguedà | 16 |
| Forêt de Guardiola de Berguedà (96) | Guardiola de Berguedà › Berguedà | 16 |
| Forêt de Fígols (34) | Fígols › Berguedà | 16 |
| Forêt de Sant Martí de Centelles (77) | Sant Martí de Centelles › Osona (Barcelone) | 16 |
| Forêt de Sant Feliu Sasserra (35) | Sant Feliu Sasserra › Bages | 16 |
| Forêt de Castellar de n'Hug (29) | Castellar de n'Hug › Berguedà | 16 |
| Forêt de Sant Agustí de Lluçanès (6) | Sant Agustí de Lluçanès › Osona (Barcelone) | 16 |
| Forêt de Vallirana (38) | Vallirana › Baix Llobregat | 16 |
| Forêt de Rupit i Pruit (37) | Rupit i Pruit › Osona (Barcelone) | 16 |
| Forêt de Borredà (129) | Borredà › Berguedà | 16 |
| Forêt de Alpens (15) | Alpens › Lluçanès | 16 |
| Forêt de Sallent (115) | Sallent › Bages | 16 |
| Forêt de Santpedor (19) | Santpedor › Bages | 16 |
| Forêt de Fonollosa (152) | Fonollosa › Bages | 16 |
| Forêt de Sant Mateu de Bages (142) | Sant Mateu de Bages › Bages | 16 |
| Forêt de Vallcebre (74) | Vallcebre › Berguedà | 16 |
| Forêt de Gurb (62) | Gurb › Osona (Barcelone) | 16 |
| Forêt de Polinyà | Polinyà › Vallès Occidental | 15 |
| Forêt de Sant Sadurní d'Osormort (3) | Sant Sadurní d'Osormort › Osona (Barcelone) | 15 |
| Forêt de Fogars de la Selva (2) | Fogars de la Selva › la Selva (Barcelone) | 15 |
| Forêt de Sagàs | Sagàs › Berguedà | 15 |
| Forêt de els Hostalets de Pierola | els Hostalets de Pierola › Anoia | 15 |
| Forêt de Castellet i la Gornal | Castellet i la Gornal › Alt Penedès | 15 |
| Forêt de Veciana (2) | Veciana › Anoia | 15 |
| Forêt de Vilanova de Sau (9) | Vilanova de Sau › Osona (Barcelone) | 15 |
| Forêt de Sora (12) | Sora › Osona (Barcelone) | 15 |
| Forêt de Sabadell (2) | Sabadell › Vallès Occidental | 15 |
| Bois de Vilassar de Dalt (15) | Vilassar de Dalt › Maresme | 15 |
| Bois de Llinars del Vallès (6) | Llinars del Vallès › Vallès Oriental | 15 |
| Forêt de els Prats de Rei (2) | els Prats de Rei › Anoia | 15 |
| Bois de Argentona (49) | Argentona › Maresme | 15 |
| Forêt de l'Ametlla del Vallès (6) | l'Ametlla del Vallès › Vallès Oriental | 15 |
| Bois de Veciana (12) | Veciana › Anoia | 15 |
| Forêt de Fogars de Montclús (9) | Fogars de Montclús › Vallès Oriental | 15 |
| Forêt de Tagamanent (13) | Tagamanent › Vallès Oriental | 15 |
| Forêt de Matadepera (209) | Matadepera › Vallès Occidental | 15 |
| Forêt de Avinyó (49) | Avinyó › Bages | 15 |
| Forêt de Castellbell i el Vilar (37) | Castellbell i el Vilar › Bages | 15 |
| Forêt de Rellinars (8) | Rellinars › Vallès Occidental | 15 |
| Forêt de Rellinars (9) | Rellinars › Vallès Occidental | 15 |
| Forêt de el Pont de Vilomara i Rocafort (9) | el Pont de Vilomara i Rocafort › Bages | 15 |
| Forêt de el Pont de Vilomara i Rocafort (17) | el Pont de Vilomara i Rocafort › Bages | 15 |
| Forêt de Moià (34) | Moià › Moianès | 15 |
| Forêt de Begues (35) | Begues › Baix Llobregat | 15 |
| Forêt de Manresa (122) | Manresa › Bages | 15 |
| Forêt de Gaià (46) | Gaià › Bages | 15 |
| Forêt de Santa Maria de Palautordera (26) | Santa Maria de Palautordera › Vallès Oriental | 15 |
| Forêt de Vilada (5) | Vilada › Berguedà | 15 |
| Forêt de Castell de l'Areny (11) | Castell de l'Areny › Berguedà | 15 |
| Forêt de Borredà (13) | Borredà › Berguedà | 15 |
| Forêt de Castell de l'Areny (23) | Castell de l'Areny › Berguedà | 15 |
| Forêt de Fígols (9) | Fígols › Berguedà | 15 |
| Forêt de Sant Vicenç de Castellet (31) | Sant Vicenç de Castellet › Bages | 15 |
| Forêt de Terrassa (75) | Terrassa › Vallès Occidental | 15 |
| Forêt de Súria (24) | Súria › Bages | 15 |
| Forêt de Navàs (80) | Navàs › Bages | 15 |
| Forêt de Viver i Serrateix (37) | Viver i Serrateix › Berguedà | 15 |
| Forêt de Avià (18) | Avià › Berguedà | 15 |
| Forêt de Avià (24) | Avià › Berguedà | 15 |
| Forêt de Casserres (25) | Casserres › Berguedà | 15 |
| Forêt de Viver i Serrateix (77) | Viver i Serrateix › Berguedà | 15 |
| Forêt de Montmajor (109) | Montmajor › Berguedà | 15 |
| Forêt de Santa Maria de Merlès (35) | Santa Maria de Merlès › Berguedà | 15 |
| Forêt de Sant Bartomeu del Grau (11) | Sant Bartomeu del Grau › Osona (Barcelone) | 15 |
| Forêt de Vic (30) | Santa Eulàlia de Riuprimer › Osona (Barcelone) | 15 |
| Forêt de Saldes (25) | Saldes › Berguedà | 15 |
| Forêt de Jorba (22) | Jorba › Anoia | 15 |
| Forêt de Olesa de Bonesvalls (35) | Olesa de Bonesvalls › Alt Penedès | 15 |
| Forêt de Castellet i la Gornal (83) | Castellet i la Gornal › Alt Penedès | 15 |
| Forêt de Guardiola de Berguedà (62) | Guardiola de Berguedà › Berguedà | 15 |
| Forêt de Guardiola de Berguedà (63) | Guardiola de Berguedà › Berguedà | 15 |
| Forêt de Figaró-Montmany (5) | Figaró-Montmany › Vallès Oriental | 15 |
| Forêt de Santa Maria d'Oló (59) | Santa Maria d'Oló › Moianès | 15 |
| Forêt de el Brull (38) | el Brull › Osona (Barcelone) | 15 |
| Forêt de Montseny (21) | Montseny › Vallès Oriental | 15 |
| Forêt de Sant Quirze Safaja (46) | Sant Quirze Safaja › Moianès | 15 |
| Forêt de Sant Pere de Vilamajor (96) | Sant Pere de Vilamajor › Vallès Oriental | 15 |
| Forêt de Argentona (4) | Argentona › Maresme | 15 |
| Forêt de Collsuspina (10) | Collsuspina › Moianès | 15 |
| Forêt de Saldes (36) | Saldes › Berguedà | 15 |
| Forêt de Bagà (65) | Bagà › Berguedà | 15 |
| Forêt de Olost (6) | Olost › Lluçanès | 15 |
| Forêt de Lluçà (40) | Lluçà › Lluçanès | 15 |
| Forêt de Gisclareny (54) | Gisclareny › Berguedà | 15 |
| Forêt de Vallcebre (39) | Vallcebre › Berguedà | 15 |
| Forêt de Vilanova del Vallès (21) | Vilanova del Vallès › Vallès Oriental | 15 |
| Bois de Llinars del Vallès (38) | Llinars del Vallès › Vallès Oriental | 15 |
| Parc Fluvial del Besòs | Santa Coloma de Gramenet › Barcelonès | 15 |
| Forêt de Torrelles de Llobregat (176) | Torrelles de Llobregat › Baix Llobregat | 15 |
| Forêt de Guardiola de Berguedà (126) | Guardiola de Berguedà › Berguedà | 15 |
| Forêt de Calders (69) | Calders › Moianès | 15 |
| Forêt de Castellar de n'Hug (35) | Castellar de n'Hug › Berguedà | 15 |
| Forêt de Castellar de n'Hug (41) | Castellar de n'Hug › Berguedà | 15 |
| Forêt de Oristà (164) | Oristà › Lluçanès | 15 |
| Forêt de Orpí (3) | Carme › Anoia | 15 |
| Forêt de Sant Esteve Sesrovires (29) | Sant Esteve Sesrovires › Baix Llobregat | 15 |
| Forêt de Piera (75) | Piera › Anoia | 15 |
| Forêt de Borredà (134) | Borredà › Berguedà | 15 |
| Forêt de Lluçà (78) | Lluçà › Lluçanès | 15 |
| Forêt de Castellnou de Bages (66) | Castellnou de Bages › Bages | 15 |
| Forêt de el Pont de Vilomara i Rocafort (47) | el Pont de Vilomara i Rocafort › Bages | 15 |
| Forêt de Sant Martí d'Albars (4) | Sant Martí d'Albars › Lluçanès | 15 |
| Parc del Guinardó | Barcelona › Barcelonès | 14 |
| Forêt de Collsuspina | Collsuspina › Moianès | 14 |
| Forêt de Castellfollit del Boix (2) | Castellfollit del Boix › Bages | 14 |
| Forêt de Fogars de Montclús (2) | Fogars de Montclús › Vallès Oriental | 14 |
| Forêt de Vilanova de Sau (7) | Vilanova de Sau › Osona (Barcelone) | 14 |
| Forêt de Sora (17) | Sora › Osona (Barcelone) | 14 |
| Forêt de la Quar (4) | la Quar › Berguedà | 14 |
| Forêt de Orpí | Orpí › Anoia | 14 |
| Forêt de Avinyonet del Penedès (30) | Avinyonet del Penedès › Alt Penedès | 14 |
| Forêt de Gelida | Gelida › Alt Penedès | 14 |
| Forêt de Subirats (81) | el Pla del Penedès › Alt Penedès | 14 |
| Forêt de Santa Fe del Penedès (2) | Santa Fe del Penedès › Alt Penedès | 14 |
| Forêt de Bigues i Riells del Fai (7) | Bigues i Riells del Fai › Vallès Oriental | 14 |
| Bois de la Roca del Vallès (7) | la Roca del Vallès › Vallès Oriental | 14 |
| Bois de la Roca del Vallès (13) | la Roca del Vallès › Vallès Oriental | 14 |
| Forêt de Sant Salvador de Guardiola (5) | Sant Salvador de Guardiola › Bages | 14 |
| Forêt de Cardona (12) | Cardona › Bages | 14 |
| Forêt de Cànoves i Samalús (22) | Cànoves i Samalús › Vallès Oriental | 14 |
| Forêt de Sant Pere de Vilamajor (75) | Sant Pere de Vilamajor › Vallès Oriental | 14 |
| Forêt de Tagamanent (6) | Tagamanent › Vallès Oriental | 14 |
| les Sorres de Pineda | Viladecans › Baix Llobregat | 14 |
| Forêt de Cercs (8) | Cercs › Berguedà | 14 |
| Forêt de Tordera (47) | Tordera › Maresme | 14 |
| Forêt de el Bruc (7) | el Bruc › Anoia | 14 |
| Forêt de Marganell (5) | Marganell › Bages | 14 |
| Forêt de Balsareny (43) | Balsareny › Bages | 14 |
| Forêt de Vallcebre (15) | Vallcebre › Berguedà | 14 |
| Forêt de Abrera (7) | Abrera › Baix Llobregat | 14 |
| Forêt de Sant Esteve Sesrovires (16) | Sant Esteve Sesrovires › Baix Llobregat | 14 |
| Forêt de Masquefa (15) | Masquefa › Anoia | 14 |
| Forêt de Montmajor (58) | Montmajor › Berguedà | 14 |
| Forêt de Oristà (92) | Oristà › Lluçanès | 14 |
| Forêt de Canyelles (5) | Canyelles › Garraf | 14 |
| Forêt de Oristà (105) | Oristà › Lluçanès | 14 |
| Forêt de Gelida (22) | Gelida › Alt Penedès | 14 |
| Forêt de la Palma de Cervelló (3) | la Palma de Cervelló › Baix Llobregat | 14 |
| Forêt de Collbató (6) | Collbató › Baix Llobregat | 14 |
| Forêt de Castellbell i el Vilar (36) | Castellbell i el Vilar › Bages | 14 |
| Forêt de Òdena (31) | Òdena › Anoia | 14 |
| Forêt de la Pobla de Claramunt (10) | la Pobla de Claramunt › Anoia | 14 |
| Forêt de Castellbell i el Vilar (57) | Castellbell i el Vilar › Bages | 14 |
| Forêt de Castellbell i el Vilar (66) | Castellbell i el Vilar › Bages | 14 |
| Forêt de el Pont de Vilomara i Rocafort (20) | el Pont de Vilomara i Rocafort › Bages | 14 |
| Forêt de Sitges (64) | Sitges › Garraf | 14 |
| Forêt de Cànoves i Samalús (38) | Cànoves i Samalús › Vallès Oriental | 14 |
| Forêt de la Pobla de Lillet (12) | la Pobla de Lillet › Berguedà | 14 |
| Forêt de Sant Quirze de Besora (2) | Sant Quirze de Besora › Osona (Barcelone) | 14 |
| Forêt de Monistrol de Calders (17) | Monistrol de Calders › Moianès | 14 |
| Forêt de Sant Llorenç Savall (17) | Sant Llorenç Savall › Vallès Occidental | 14 |
| Forêt de Sant Salvador de Guardiola (58) | Sant Salvador de Guardiola › Bages | 14 |
| Forêt de Sant Salvador de Guardiola (72) | Sant Salvador de Guardiola › Bages | 14 |
| Forêt de Castellbisbal (15) | Castellbisbal › Vallès Occidental | 14 |
| Forêt de Viver i Serrateix (57) | Viver i Serrateix › Berguedà | 14 |
| Forêt de Viver i Serrateix (60) | Viver i Serrateix › Berguedà | 14 |
| Forêt de Viver i Serrateix (61) | Viver i Serrateix › Berguedà | 14 |
| Forêt de Montmajor (102) | Montclar › Berguedà | 14 |
| Forêt de Súria (27) | Súria › Bages | 14 |
| Forêt de la Quar (9) | la Quar › Berguedà | 14 |
| Forêt de Jorba (29) | Jorba › Anoia | 14 |
| Forêt de Jorba (36) | Jorba › Anoia | 14 |
| Forêt de Òdena (46) | Òdena › Anoia | 14 |
| Forêt de Sant Pere de Ribes (103) | Sant Pere de Ribes › Garraf | 14 |
| Forêt de Fígols (12) | Fígols › Berguedà | 14 |
| Forêt de Canyelles (18) | Canyelles › Garraf | 14 |
| Forêt de Vilanova i la Geltrú (36) | Vilanova i la Geltrú › Garraf | 14 |
| Forêt de Gisclareny (19) | Gisclareny › Berguedà | 14 |
| Forêt de Fígols (13) | Fígols › Berguedà | 14 |
| Forêt de Sagàs (23) | Sagàs › Berguedà | 14 |
| Forêt de Avinyó (115) | Avinyó › Bages | 14 |
| Forêt de Santa Maria de Merlès (114) | Santa Maria de Merlès › Berguedà | 14 |
| Forêt de Balenyà (6) | Balenyà › Osona (Barcelone) | 14 |
| Forêt de el Brull (27) | el Brull › Osona (Barcelone) | 14 |
| Forêt de Tagamanent (34) | Tagamanent › Vallès Oriental | 14 |
| Forêt de Fogars de Montclús (20) | Fogars de Montclús › Vallès Oriental | 14 |
| Forêt de Montseny (13) | Montseny › Vallès Oriental | 14 |
| Forêt de Sant Quirze Safaja (28) | Sant Quirze Safaja › Moianès | 14 |
| Forêt de Sant Quirze Safaja (33) | Sant Quirze Safaja › Moianès | 14 |
| Forêt de Santa Maria d'Oló (76) | Santa Maria d'Oló › Moianès | 14 |
| Forêt de Santa Eulàlia de Riuprimer (15) | Santa Eulàlia de Riuprimer › Osona (Barcelone) | 14 |
| Forêt de Oristà (145) | Oristà › Lluçanès | 14 |
| Forêt de Sant Mateu de Bages (76) | Sant Mateu de Bages › Bages | 14 |
| Forêt de Perafita (5) | Perafita › Lluçanès | 14 |
| Forêt de Bagà (46) | Bagà › Berguedà | 14 |
| Forêt de Capolat (42) | Capolat › Berguedà | 14 |
| Forêt de Castellar del Riu (35) | Castellar del Riu › Berguedà | 14 |
| Forêt de Castellar del Riu (40) | Castellar del Riu › Berguedà | 14 |
| Forêt de Prats de Lluçanès (26) | Prats de Lluçanès › Lluçanès | 14 |
| Forêt de Lluçà (25) | Lluçà › Lluçanès | 14 |
| Forêt de la Quar (37) | la Quar › Berguedà | 14 |
| Forêt de Gisclareny (52) | Gisclareny › Berguedà | 14 |
| Forêt de Cercs (68) | Cercs › Berguedà | 14 |
| Forêt de Orís (17) | Orís › Osona (Barcelone) | 14 |
| Forêt de Sant Sadurní d'Osormort (26) | Sant Sadurní d'Osormort › Osona (Barcelone) | 14 |
| Bois de Vilanova del Vallès (13) | Vilanova del Vallès › Vallès Oriental | 14 |
| Forêt de Castellar de n'Hug (25) | Castellar de n'Hug › Berguedà | 14 |
| Forêt de Castellar de n'Hug (42) | Castellar de n'Hug › Berguedà | 14 |
| Forêt de Sant Feliu Sasserra (39) | Sant Feliu Sasserra › Bages | 14 |
| Forêt de Sant Quintí de Mediona (4) | Sant Quintí de Mediona › Alt Penedès | 14 |
| Forêt de Piera (82) | Piera › Anoia | 14 |
| Forêt de Piera (84) | Piera › Anoia | 14 |
| Forêt de la Llacuna (15) | la Llacuna › Anoia | 14 |
| Forêt de la Llacuna (22) | la Llacuna › Anoia | 14 |
| Forêt de la Llacuna (23) | la Llacuna › Anoia | 14 |
| Forêt de la Quar (49) | la Quar › Berguedà | 14 |
| Forêt de Sagàs (55) | Sagàs › Berguedà | 14 |
| Forêt de Sant Cebrià de Vallalta (11) | Sant Cebrià de Vallalta › Maresme | 14 |
| Forêt de Santa Susanna (3) | Santa Susanna › Maresme | 14 |
| Forêt de Sant Celoni (31) | Sant Celoni › Vallès Oriental | 14 |
| Forêt de Vallgorguina (10) | Vallgorguina › Vallès Oriental | 14 |
| Forêt de Sant Celoni (41) | Sant Celoni › Vallès Oriental | 14 |
| Forêt de Seva (36) | Seva › Osona (Barcelone) | 14 |
| Forêt de Arenys de Mar (14) | Arenys de Mar › Maresme | 14 |
| Turó de Cerdanyola | Mataró › Maresme | 14 |
| Bois de Argentona (54) | Argentona › Maresme | 14 |
| Forêt de Barberà del Vallès | Barberà del Vallès › Vallès Occidental | 13 |
| Forêt de Aguilar de Segarra | Aguilar de Segarra › Bages | 13 |
| Forêt de Castellar del Vallès (2) | Castellar del Vallès › Vallès Occidental | 13 |
| Forêt de Subirats (2) | Subirats › Alt Penedès | 13 |
| Forêt de Pujalt (3) | Pujalt › Anoia | 13 |
| Forêt de Mediona | Mediona › Alt Penedès | 13 |
| Forêt de Torrelavit (3) | Torrelavit › Alt Penedès | 13 |
| Forêt de Calonge de Segarra (4) | Calonge de Segarra › Anoia | 13 |
| Forêt de Lluçà (4) | Lluçà › Lluçanès | 13 |
| Forêt de Vilanova de Sau (25) | Vilanova de Sau › Osona (Barcelone) | 13 |
| Forêt de Tordera (13) | Tordera › Maresme | 13 |
| Forêt de Sant Climent de Llobregat (13) | Sant Climent de Llobregat › Baix Llobregat | 13 |
| la Serreta | Olèrdola › Alt Penedès | 13 |
| Forêt de Avinyonet del Penedès (43) | Avinyonet del Penedès › Alt Penedès | 13 |
| Bois de Argentona (11) | Argentona › Maresme | 13 |
| Bois de la Roca del Vallès (18) | la Roca del Vallès › Vallès Oriental | 13 |
| Bois de Dosrius (6) | Dosrius › Maresme | 13 |
| Parc del Turó de Can Mates | Sant Cugat del Vallès › Vallès Occidental | 13 |
| Bois de Argentona (36) | Argentona › Maresme | 13 |
| Bois de Argentona (45) | Argentona › Maresme | 13 |
| Bosc de Can Plandolit | l'Ametlla del Vallès › Vallès Oriental | 13 |
| Forêt de Sant Fost de Campsentelles (6) | Sant Fost de Campsentelles › Vallès Oriental | 13 |
| Forêt de les Masies de Voltregà (6) | les Masies de Voltregà › Osona (Barcelone) | 13 |
| Forêt de el Brull (13) | el Brull › Osona (Barcelone) | 13 |
| Forêt de Balsareny (42) | Balsareny › Bages | 13 |
| Forêt de Rubí (58) | Rubí › Vallès Occidental | 13 |
| Forêt de Rajadell (35) | Rajadell › Bages | 13 |
| Forêt de Olvan (9) | Olvan › Berguedà | 13 |
| Forêt de Lliçà de Vall (6) | Lliçà de Vall › Vallès Oriental | 13 |
| Forêt de Castellterçol (63) | Castellterçol › Moianès | 13 |
| Forêt de Berga (24) | Avià › Berguedà | 13 |
| Forêt de Sant Jaume de Frontanyà (5) | Sant Jaume de Frontanyà › Berguedà | 13 |
| Forêt de Berga (49) | Berga › Berguedà | 13 |
| Forêt de Castellnou de Bages (39) | Castellnou de Bages › Bages | 13 |
| Forêt de Viver i Serrateix (23) | Viver i Serrateix › Berguedà | 13 |
| Forêt de l'Espunyola (47) | l'Espunyola › Berguedà | 13 |
| Forêt de l'Espunyola (48) | l'Espunyola › Berguedà | 13 |
| Forêt de Gelida (23) | Gelida › Alt Penedès | 13 |
| Forêt de Corbera de Llobregat (20) | Corbera de Llobregat › Baix Llobregat | 13 |
| Forêt de Rubí (63) | Rubí › Vallès Occidental | 13 |
| Forêt de Vacarisses (19) | Vacarisses › Vallès Occidental | 13 |
| Forêt de Sant Vicenç de Castellet (6) | Sant Vicenç de Castellet › Bages | 13 |
| Forêt de Castelldefels (11) | Castelldefels › Baix Llobregat | 13 |
| Forêt de Begues (37) | Gavà › Baix Llobregat | 13 |
| Bois de Vilanova del Vallès (10) | Vilanova del Vallès › Vallès Oriental | 13 |
| Forêt de Gaià (52) | Gaià › Bages | 13 |
| Forêt de Sant Pere de Vilamajor (84) | Sant Pere de Vilamajor › Vallès Oriental | 13 |
| Forêt de Vilada (7) | Vilada › Berguedà | 13 |
| Forêt de Borredà (14) | Borredà › Berguedà | 13 |
| Bois de Castellar del Riu | Castellar del Riu › Berguedà | 13 |
| Forêt de Guardiola de Berguedà (56) | Guardiola de Berguedà › Berguedà | 13 |
| Forêt de el Pont de Vilomara i Rocafort (27) | el Pont de Vilomara i Rocafort › Bages | 13 |
| Forêt de Talamanca (31) | Talamanca › Bages | 13 |
| Forêt de Castellar del Vallès (19) | Castellar del Vallès › Vallès Occidental | 13 |
| Forêt de Sant Pere Sallavinera (20) | Sant Pere Sallavinera › Anoia | 13 |
| Forêt de Sant Salvador de Guardiola (67) | Sant Salvador de Guardiola › Bages | 13 |
| Forêt de Castellfollit del Boix (28) | Castellfollit del Boix › Bages | 13 |
| Forêt de Sant Salvador de Guardiola (114) | Sant Salvador de Guardiola › Bages | 13 |
| Forêt de Sant Salvador de Guardiola (119) | Sant Salvador de Guardiola › Bages | 13 |
| Forêt de Esparreguera (30) | Esparreguera › Baix Llobregat | 13 |
| Forêt de Castellbisbal (33) | Castellbisbal › Vallès Occidental | 13 |
| Forêt de Martorell (19) | Martorell › Baix Llobregat | 13 |
| Forêt de Navàs (63) | Navàs › Bages | 13 |
| Forêt de Puig-reig (56) | Puig-reig › Berguedà | 13 |
| Forêt de Puig-reig (62) | Puig-reig › Berguedà | 13 |
| Forêt de Viver i Serrateix (54) | Viver i Serrateix › Berguedà | 13 |
| Forêt de Puig-reig (74) | Puig-reig › Berguedà | 13 |
| Forêt de Santa Maria de Merlès (21) | Santa Maria de Merlès › Berguedà | 13 |
| Forêt de Gironella (11) | Gironella › Berguedà | 13 |
| Forêt de Montclar (32) | Montclar › Berguedà | 13 |
| Forêt de Capolat (21) | Capolat › Berguedà | 13 |
| Forêt de Sant Mateu de Bages (43) | Sant Mateu de Bages › Bages | 13 |
| Forêt de Navàs (109) | Navàs › Bages | 13 |
| Forêt de Navàs (137) | Navàs › Bages | 13 |
| Forêt de Gaià (67) | Gaià › Bages | 13 |
| Forêt de Avinyó (104) | Avinyó › Bages | 13 |
| Forêt de Jorba (13) | Jorba › Anoia | 13 |
| Forêt de Begues (69) | Begues › Baix Llobregat | 13 |
| Forêt de Vilanova i la Geltrú (33) | Vilanova i la Geltrú › Garraf | 13 |
| Forêt de Viver i Serrateix (106) | Viver i Serrateix › Berguedà | 13 |
| Forêt de Sant Feliu Sasserra (16) | Sant Feliu Sasserra › Bages | 13 |
| Forêt de la Quar (15) | la Quar › Berguedà | 13 |
| Forêt de les Franqueses del Vallès (52) | les Franqueses del Vallès › Vallès Oriental | 13 |
| Forêt de Collsuspina (6) | Collsuspina › Moianès | 13 |
| Forêt de Monistrol de Calders (41) | Monistrol de Calders › Moianès | 13 |
| Forêt de Santa Eulàlia de Riuprimer (17) | Santa Eulàlia de Riuprimer › Osona (Barcelone) | 13 |
| Forêt de Santa Eulàlia de Riuprimer (18) | Santa Eulàlia de Riuprimer › Osona (Barcelone) | 13 |
| Forêt de Santa Eulàlia de Riuprimer (21) | Santa Eulàlia de Riuprimer › Osona (Barcelone) | 13 |
| Forêt de Oristà (147) | Oristà › Lluçanès | 13 |
| Forêt de Santa Maria de Merlès (124) | Santa Maria de Merlès › Berguedà | 13 |
| Forêt de Gisclareny (27) | Gisclareny › Berguedà | 13 |
| Forêt de Bagà (49) | Bagà › Berguedà | 13 |
| Forêt de Fígols (17) | Fígols › Berguedà | 13 |
| Forêt de Lluçà (26) | Lluçà › Lluçanès | 13 |
| Forêt de Borredà (124) | Borredà › Berguedà | 13 |
| Forêt de la Pobla de Lillet (52) | la Pobla de Lillet › Berguedà | 13 |
| Forêt de Cercs (67) | Cercs › Berguedà | 13 |
| Forêt de Saldes (119) | Saldes › Berguedà | 13 |
| Forêt de Centelles (31) | Centelles › Osona (Barcelone) | 13 |
| Forêt de Castellet i la Gornal (93) | Castellet i la Gornal › Alt Penedès | 13 |
| Forêt de Barcelona (59) | Barcelona › Barcelonès | 13 |
| Forêt de Piera (27) | Piera › Anoia | 13 |
| Forêt de Sant Feliu Sasserra (34) | Sant Feliu Sasserra › Bages | 13 |
| Forêt de Cardona (105) | Cardona › Bages | 13 |
| Forêt de la Torre de Claramunt (6) | la Torre de Claramunt › Anoia | 13 |
| Parc de Catalunya (2) | Sabadell › Vallès Occidental | 13 |
| Forêt de Castellbisbal (47) | Castellbisbal › Vallès Occidental | 13 |
| Bois de Piera (8) | Piera › Anoia | 13 |
| Forêt de Torrelavit (26) | Torrelavit › Alt Penedès | 13 |
| Forêt de Torrelavit (41) | Torrelavit › Alt Penedès | 13 |
| Forêt de Sant Pere de Riudebitlles (5) | Sant Pere de Riudebitlles › Alt Penedès | 13 |
| Forêt de Piera (80) | Piera › Anoia | 13 |
| Forêt de Sant Quintí de Mediona (16) | Sant Quintí de Mediona › Alt Penedès | 13 |
| Forêt de Mediona (89) | Mediona › Alt Penedès | 13 |
| Forêt de la Llacuna (17) | la Llacuna › Anoia | 13 |
| Forêt de la Llacuna (19) | la Llacuna › Anoia | 13 |
| Forêt de Òdena (90) | Òdena › Anoia | 13 |
| Forêt de la Quar (50) | la Quar › Berguedà | 13 |
| Forêt de Arenys de Munt (24) | Arenys de Munt › Maresme | 13 |
| Forêt de Gualba (11) | Gualba › Vallès Oriental | 13 |
| Forêt de Sant Mateu de Bages (138) | Sant Mateu de Bages › Bages | 13 |
| Forêt de Sant Mateu de Bages (145) | Sant Mateu de Bages › Bages | 13 |
| Forêt de Sant Mateu de Bages (146) | Sant Mateu de Bages › Bages | 13 |
| Forêt de Gurb (32) | Gurb › Osona (Barcelone) | 13 |
| Forêt de Sant Quintí de Mediona (19) | Sant Quintí de Mediona › Alt Penedès | 13 |
| Forêt de Prats de Lluçanès (36) | Prats de Lluçanès › Lluçanès | 13 |
| Forêt de Olost (10) | Olost › Lluçanès | 13 |
| Forêt de Talamanca (43) | Talamanca › Bages | 13 |
| Parc de Vallparadís | Terrassa › Vallès Occidental | 12 |
| Forêt de la Garriga | la Garriga › Vallès Oriental | 12 |
| Forêt de Taradell | Taradell › Osona (Barcelone) | 12 |
| Forêt de Oristà (3) | Oristà › Lluçanès | 12 |
| Forêt de Montmaneu (4) | Montmaneu › Anoia | 12 |
| Forêt de Sant Cebrià de Vallalta | Sant Cebrià de Vallalta › Maresme | 12 |
| Forêt de Olèrdola (2) | Olèrdola › Alt Penedès | 12 |
| Forêt de Terrassa (4) | Terrassa › Vallès Occidental | 12 |
| Forêt de Sant Martí de Tous (7) | Sant Martí de Tous › Anoia | 12 |
| Forêt de Subirats (19) | Subirats › Alt Penedès | 12 |
| Forêt de Sitges (3) | Sitges › Garraf | 12 |
| Bois de Òrrius (20) | Òrrius › Maresme | 12 |
| Bois de la Roca del Vallès (16) | la Roca del Vallès › Vallès Oriental | 12 |
| Bois de la Roca del Vallès (17) | la Roca del Vallès › Vallès Oriental | 12 |
| Forêt de Navàs | Navàs › Bages | 12 |
| Bois de Gurb (5) | Gurb › Osona (Barcelone) | 12 |
| Forêt de Cardedeu | Cardedeu › Vallès Oriental | 12 |
| Forêt de Sant Jaume de Frontanyà (4) | Sant Jaume de Frontanyà › Berguedà | 12 |
| Forêt de Alpens (11) | Alpens › Lluçanès | 12 |
| Bosc de les Valls | Torrelles de Foix › Alt Penedès | 12 |
| Bois de Torrelles de Foix (4) | Torrelles de Foix › Alt Penedès | 12 |
| Forêt de Gaià (12) | Gaià › Bages | 12 |
| Forêt de Rajadell (13) | Rajadell › Bages | 12 |
| Forêt de Manresa (21) | Manresa › Bages | 12 |
| Forêt de Balsareny (34) | Balsareny › Bages | 12 |
| Forêt de Calders (27) | Calders › Moianès | 12 |
| Forêt de Rubí (57) | Rubí › Vallès Occidental | 12 |
| Forêt de Castellterçol (17) | Castellterçol › Moianès | 12 |
| Forêt de Castell de l'Areny (5) | Castell de l'Areny › Berguedà | 12 |
| Forêt de Aiguafreda (10) | Aiguafreda › Osona (Barcelone) | 12 |
| Forêt de Cardona (54) | Cardona › Bages | 12 |
| Forêt de l'Esquirol (115) | l'Esquirol › Osona (Barcelone) | 12 |
| Forêt de Montmajor (68) | Montmajor › Berguedà | 12 |
| Forêt de Sant Salvador de Guardiola (28) | Sant Salvador de Guardiola › Bages | 12 |
| Forêt de Gironella (7) | Gironella › Berguedà | 12 |
| Forêt de Oristà (104) | Oristà › Lluçanès | 12 |
| Forêt de Castellbell i el Vilar (6) | Castellbell i el Vilar › Bages | 12 |
| Forêt de l'Espunyola (38) | l'Espunyola › Berguedà | 12 |
| Forêt de Sant Julià de Cerdanyola | Sant Julià de Cerdanyola › Berguedà | 12 |
| Forêt de Santa Margarida de Montbui (10) | Santa Margarida de Montbui › Anoia | 12 |
| Forêt de Guardiola de Berguedà (38) | Guardiola de Berguedà › Berguedà | 12 |
| Forêt de Castellbell i el Vilar (17) | Castellbell i el Vilar › Bages | 12 |
| Forêt de Marganell (8) | Marganell › Bages | 12 |
| Forêt de el Bruc (13) | el Bruc › Anoia | 12 |
| Forêt de el Bruc (27) | el Bruc › Anoia | 12 |
| Forêt de Moià (35) | Moià › Moianès | 12 |
| Forêt de Sitges (60) | Sitges › Garraf | 12 |
| Forêt de Marganell (27) | Marganell › Bages | 12 |
| Forêt de Artés (22) | Artés › Bages | 12 |
| Forêt de Vic (26) | Vic › Osona (Barcelone) | 12 |
| Forêt de Cardedeu (26) | Cardedeu › Vallès Oriental | 12 |
| Forêt de Sallent (81) | Sallent › Bages | 12 |
| Forêt de Gaià (33) | Gaià › Bages | 12 |
| Forêt de Gaià (43) | Gaià › Bages | 12 |
| Forêt de Santa Maria de Palautordera (20) | Santa Maria de Palautordera › Vallès Oriental | 12 |
| Forêt de Vilada (6) | Vilada › Berguedà | 12 |
| Forêt de Castell de l'Areny (10) | Castell de l'Areny › Berguedà | 12 |
| Forêt de Castell de l'Areny (16) | Castell de l'Areny › Berguedà | 12 |
| Forêt de Castell de l'Areny (17) | Castell de l'Areny › Berguedà | 12 |
| Forêt de Castell de l'Areny (18) | Castell de l'Areny › Berguedà | 12 |
| Forêt de la Pobla de Lillet (33) | la Pobla de Lillet › Berguedà | 12 |
| Forêt de Guardiola de Berguedà (47) | Guardiola de Berguedà › Berguedà | 12 |
| Forêt de Guardiola de Berguedà (57) | Guardiola de Berguedà › Berguedà | 12 |
| Forêt de Talamanca (6) | Talamanca › Bages | 12 |
| Forêt de Talamanca (7) | Talamanca › Bages | 12 |
| Forêt de Talamanca (12) | Talamanca › Bages | 12 |
| Forêt de Castellfollit del Boix (29) | Castellfollit del Boix › Bages | 12 |
| Forêt de el Bruc (41) | el Bruc › Anoia | 12 |
| Forêt de Castellbisbal (13) | Castellbisbal › Vallès Occidental | 12 |
| Forêt de Castellbisbal (18) | Castellbisbal › Vallès Occidental | 12 |
| Forêt de Castellbisbal (24) | Castellbisbal › Vallès Occidental | 12 |
| Forêt de Viver i Serrateix (47) | Viver i Serrateix › Berguedà | 12 |
| Forêt de Sagàs (15) | Sagàs › Berguedà | 12 |
| Forêt de Montmajor (97) | Montmajor › Berguedà | 12 |
| Forêt de Navàs (127) | Navàs › Bages | 12 |
| Forêt de Súria (30) | Súria › Bages | 12 |
| Forêt de Súria (31) | Súria › Bages | 12 |
| Forêt de Montmajor (112) | Montmajor › Berguedà | 12 |
| Forêt de Argençola (26) | Argençola › Anoia | 12 |
| Forêt de Olivella (111) | Olivella › Garraf | 12 |
| Forêt de Olesa de Bonesvalls (49) | Olesa de Bonesvalls › Alt Penedès | 12 |
| Forêt de Sant Pere de Ribes (90) | Sant Pere de Ribes › Garraf | 12 |
| Forêt de Castellet i la Gornal (85) | Castellet i la Gornal › Alt Penedès | 12 |
| Forêt de Sant Pere de Ribes (108) | Sant Pere de Ribes › Garraf | 12 |
| Forêt de Gisclareny (23) | Gisclareny › Berguedà | 12 |
| Forêt de Sagàs (28) | Sagàs › Berguedà | 12 |
| Forêt de Muntanyola (20) | Muntanyola › Osona (Barcelone) | 12 |
| Parc dels Talls | Vilobí del Penedès › Alt Penedès | 12 |
| Forêt de Tagamanent (22) | Tagamanent › Vallès Oriental | 12 |
| Forêt de Tagamanent (36) | Tagamanent › Vallès Oriental | 12 |
| Forêt de el Brull (33) | el Brull › Osona (Barcelone) | 12 |
| Forêt de Oristà (115) | Oristà › Lluçanès | 12 |
| Forêt de Oristà (126) | Oristà › Lluçanès | 12 |
| Forêt de Sant Mateu de Bages (103) | Sant Mateu de Bages › Bages | 12 |
| Forêt de Mataró (7) | Mataró › Maresme | 12 |
| Forêt de l'Ametlla del Vallès (26) | l'Ametlla del Vallès › Vallès Oriental | 12 |
| Forêt de Seva (31) | Seva › Osona (Barcelone) | 12 |
| Forêt de Saldes (56) | Saldes › Berguedà | 12 |
| Forêt de Saldes (60) | Saldes › Berguedà | 12 |
| Forêt de Guardiola de Berguedà (76) | Guardiola de Berguedà › Berguedà | 12 |
| Forêt de Guardiola de Berguedà (101) | Guardiola de Berguedà › Berguedà | 12 |
| Forêt de Lluçà (38) | Lluçà › Lluçanès | 12 |
| Forêt de Borredà (82) | Borredà › Berguedà | 12 |
| Forêt de Borredà (87) | Borredà › Berguedà | 12 |
| Forêt de Borredà (88) | Borredà › Berguedà | 12 |
| Forêt de Borredà (125) | Borredà › Berguedà | 12 |
| Forêt de Castellar del Riu (52) | Castellar del Riu › Berguedà | 12 |
| Forêt de Castellar del Riu (54) | Castellar del Riu › Berguedà | 12 |
| Forêt de Saldes (90) | Saldes › Berguedà | 12 |
| Forêt de Balenyà (30) | Balenyà › Osona (Barcelone) | 12 |
| Forêt de Montesquiu (9) | Montesquiu › Osona (Barcelone) | 12 |
| Forêt de Montesquiu (12) | Montesquiu › Osona (Barcelone) | 12 |
| Forêt de Tavèrnoles (6) | Tavèrnoles › Osona (Barcelone) | 12 |
| Forêt de les Masies de Roda (9) | les Masies de Roda › Osona (Barcelone) | 12 |
| Forêt de Barcelona (62) | Barcelona › Barcelonès | 12 |
| Forêt de Castellar de n'Hug (51) | Castellar de n'Hug › Berguedà | 12 |
| Forêt de Mediona (43) | Mediona › Alt Penedès | 12 |
| Forêt de Torrelles de Foix (4) | Torrelles de Foix › Alt Penedès | 12 |
| Forêt de la Llacuna (24) | la Llacuna › Anoia | 12 |
| Forêt de Borredà (130) | Borredà › Berguedà | 12 |
| Forêt de Lluçà (58) | Lluçà › Lluçanès | 12 |
| Forêt de Lluçà (65) | Lluçà › Lluçanès | 12 |
| Forêt de Alpens (27) | Alpens › Lluçanès | 12 |
| Forêt de la Quar (51) | la Quar › Berguedà | 12 |
| Forêt de Sant Vicenç de Montalt (7) | Sant Vicenç de Montalt › Maresme | 12 |
| Forêt de Vallgorguina (9) | Vallgorguina › Vallès Oriental | 12 |
| Forêt de Vilalba Sasserra (3) | Vilalba Sasserra › Vallès Oriental | 12 |
| Forêt de Fogars de la Selva (30) | Fogars de la Selva › la Selva (Barcelone) | 12 |
| Forêt de Castellnou de Bages (68) | Castellnou de Bages › Bages | 12 |
| Forêt de Callús (36) | Callús › Bages | 12 |
| Forêt de Sant Mateu de Bages (137) | Sant Mateu de Bages › Bages | 12 |
| Forêt de Sant Mateu de Bages (148) | Sant Mateu de Bages › Bages | 12 |
| Forêt de Vallcebre (61) | Vallcebre › Berguedà | 12 |
| Forêt de Sant Sadurní d'Osormort (53) | Sant Sadurní d'Osormort › Osona (Barcelone) | 12 |
| Forêt de Sant Fruitós de Bages (44) | Sant Fruitós de Bages › Bages | 12 |
| Forêt de Sant Quintí de Mediona | Sant Quintí de Mediona › Alt Penedès | 11 |
| Forêt de Campins (2) | Campins › Vallès Oriental | 11 |
| Forêt de Sant Sadurní d'Osormort (5) | Sant Sadurní d'Osormort › Osona (Barcelone) | 11 |
| Forêt de Arenys de Mar | Arenys de Mar › Maresme | 11 |
| Forêt de Sant Pere de Torelló (11) | Sant Pere de Torelló › Osona (Barcelone) | 11 |
| Bosc de Can Valls | Lliçà de Vall › Vallès Oriental | 11 |
| Forêt de Subirats (33) | Subirats › Alt Penedès | 11 |
| Forêt de Olèrdola (21) | Olèrdola › Alt Penedès | 11 |
| Forêt de Sant Sadurní d'Anoia (6) | Sant Sadurní d'Anoia › Alt Penedès | 11 |
| Bois de Òrrius (3) | Òrrius › Maresme | 11 |
| Bois de la Roca del Vallès (2) | la Roca del Vallès › Vallès Oriental | 11 |
| Bois de la Roca del Vallès (22) | la Roca del Vallès › Vallès Oriental | 11 |
| Bois de la Roca del Vallès (32) | la Roca del Vallès › Vallès Oriental | 11 |
| Bois de Canovelles (3) | Canovelles › Vallès Oriental | 11 |
| Parc de la Muntanyeta | Sant Boi de Llobregat › Baix Llobregat | 11 |
| Forêt de Santa Maria d'Oló (5) | Santa Maria d'Oló › Moianès | 11 |
| Forêt de Sentmenat (4) | Sentmenat › Vallès Occidental | 11 |
| Bois de Torrelavit | Torrelavit › Alt Penedès | 11 |
| Bois de Jorba (4) | Jorba › Anoia | 11 |
| Forêt de Cànoves i Samalús (23) | Cànoves i Samalús › Vallès Oriental | 11 |
| Forêt de el Brull (16) | el Brull › Osona (Barcelone) | 11 |
| Pineda de Can Camins | el Prat de Llobregat › Baix Llobregat | 11 |
| Forêt de Montornès del Vallès (10) | Montornès del Vallès › Vallès Oriental | 11 |
| Forêt de Sallent (27) | Sallent › Bages | 11 |
| Bois de Argentona (51) | Argentona › Maresme | 11 |
| Forêt de Sant Joan de Vilatorrada (25) | Sant Joan de Vilatorrada › Bages | 11 |
| Forêt de Avinyó (19) | Avinyó › Bages | 11 |
| Forêt de Artés (12) | Artés › Bages | 11 |
| Forêt de Terrassa (66) | Terrassa › Vallès Occidental | 11 |
| Forêt de Viladecavalls (7) | Viladecavalls › Vallès Occidental | 11 |
| Forêt de Fonollosa (95) | Fonollosa › Bages | 11 |
| Forêt de Palau-solità i Plegamans (13) | Palau-solità i Plegamans › Vallès Occidental | 11 |
| Forêt de Avinyó (45) | Avinyó › Bages | 11 |
| Forêt de Balsareny (63) | Balsareny › Bages | 11 |
| Forêt de Sant Salvador de Guardiola (35) | Sant Salvador de Guardiola › Bages | 11 |
| Forêt de Santa Maria d'Oló (29) | Santa Maria d'Oló › Moianès | 11 |
| Forêt de Santa Maria d'Oló (30) | Santa Maria d'Oló › Moianès | 11 |
| Forêt de Sant Salvador de Guardiola (42) | Sant Salvador de Guardiola › Bages | 11 |
| Forêt de Premià de Dalt (5) | Premià de Dalt › Maresme | 11 |
| Forêt de l'Espunyola (36) | l'Espunyola › Berguedà | 11 |
| Forêt de Vallirana (29) | Vallirana › Baix Llobregat | 11 |
| Forêt de Vacarisses (29) | Vacarisses › Vallès Occidental | 11 |
| Forêt de Vacarisses (34) | Vacarisses › Vallès Occidental | 11 |
| Forêt de Castellbell i el Vilar (11) | Castellbell i el Vilar › Bages | 11 |
| Forêt de Vacarisses (38) | Vacarisses › Vallès Occidental | 11 |
| Forêt de Vacarisses (40) | Vacarisses › Vallès Occidental | 11 |
| Forêt de Vacarisses (41) | Vacarisses › Vallès Occidental | 11 |
| Forêt de el Bruc (18) | el Bruc › Anoia | 11 |
| Forêt de el Bruc (23) | el Bruc › Anoia | 11 |
| Forêt de Castelldefels (10) | Castelldefels › Baix Llobregat | 11 |
| Forêt de Gavà (75) | Gavà › Baix Llobregat | 11 |
| Forêt de Sant Salvador de Guardiola (54) | Sant Salvador de Guardiola › Bages | 11 |
| Forêt de Sant Salvador de Guardiola (56) | Sant Salvador de Guardiola › Bages | 11 |
| Forêt de Avinyó (77) | Avinyó › Bages | 11 |
| Bois de Òrrius (24) | Òrrius › Maresme | 11 |
| Forêt de Navàs (33) | Navàs › Bages | 11 |
| Forêt de Vilada (4) | Vilada › Berguedà | 11 |
| Forêt de la Pobla de Lillet (16) | la Pobla de Lillet › Berguedà | 11 |
| Forêt de Santa Maria de Besora (10) | Santa Maria de Besora › Osona (Barcelone) | 11 |
| Forêt de Sant Vicenç de Castellet (25) | Sant Vicenç de Castellet › Bages | 11 |
| Forêt de Sant Pere Sallavinera (10) | Sant Pere Sallavinera › Anoia | 11 |
| Forêt de Calonge de Segarra (11) | Calonge de Segarra › Anoia | 11 |
| Forêt de Sant Salvador de Guardiola (91) | Sant Salvador de Guardiola › Bages | 11 |
| Forêt de Navàs (71) | Navàs › Bages | 11 |
| Forêt de Viver i Serrateix (26) | Viver i Serrateix › Berguedà | 11 |
| Forêt de Puig-reig (69) | Puig-reig › Berguedà | 11 |
| Forêt de Santa Maria de Merlès (22) | Santa Maria de Merlès › Berguedà | 11 |
| Forêt de Capolat (26) | Capolat › Berguedà | 11 |
| Forêt de Montclar (35) | Montclar › Berguedà | 11 |
| Forêt de Montmajor (104) | Montmajor › Berguedà | 11 |
| Forêt de Montmajor (122) | Montmajor › Berguedà | 11 |
| Forêt de Montmajor (131) | Montmajor › Berguedà | 11 |
| Forêt de Santa Maria de Merlès (27) | Santa Maria de Merlès › Berguedà | 11 |
| Forêt de Santa Maria de Merlès (59) | Santa Maria de Merlès › Berguedà | 11 |
| Forêt de Sant Cugat del Vallès (118) | Sant Cugat del Vallès › Vallès Occidental | 11 |
| Forêt de Begues (58) | Begues › Baix Llobregat | 11 |
| Forêt de Begues (68) | Begues › Baix Llobregat | 11 |
| Forêt de Olèrdola (62) | Olèrdola › Alt Penedès | 11 |
| Forêt de Olèrdola (66) | Olèrdola › Alt Penedès | 11 |
| Forêt de Vilanova i la Geltrú (38) | Vilanova i la Geltrú › Garraf | 11 |
| Forêt de Bagà (20) | Bagà › Berguedà | 11 |
| Forêt de Navàs (151) | Navàs › Bages | 11 |
| Forêt de Santa Maria d'Oló (51) | Santa Maria d'Oló › Moianès | 11 |
| Forêt de Santa Maria de Merlès (93) | Santa Maria de Merlès › Berguedà | 11 |
| Forêt de Santa Maria de Merlès (106) | Santa Maria de Merlès › Berguedà | 11 |
| Forêt de Avià (50) | Avià › Berguedà | 11 |
| Forêt de Castellar de n'Hug (20) | Castellar de n'Hug › Berguedà | 11 |
| Forêt de els Hostalets de Pierola (17) | el Bruc › Anoia | 11 |
| Forêt de Esparreguera (38) | Esparreguera › Baix Llobregat | 11 |
| Forêt de Esparreguera (41) | Esparreguera › Baix Llobregat | 11 |
| Forêt de Monistrol de Calders (36) | Monistrol de Calders › Moianès | 11 |
| Forêt de Monistrol de Calders (38) | Monistrol de Calders › Moianès | 11 |
| Forêt de Tona (3) | Tona › Osona (Barcelone) | 11 |
| Forêt de l'Estany (3) | l'Estany › Moianès | 11 |
| Forêt de el Brull (35) | el Brull › Osona (Barcelone) | 11 |
| Forêt de Montseny (12) | Montseny › Vallès Oriental | 11 |
| Forêt de Montseny (19) | Montseny › Vallès Oriental | 11 |
| Forêt de Montseny (22) | Montseny › Vallès Oriental | 11 |
| Forêt de Sant Quirze Safaja (20) | Sant Quirze Safaja › Moianès | 11 |
| Forêt de Santa Eulàlia de Riuprimer (11) | Santa Eulàlia de Riuprimer › Osona (Barcelone) | 11 |
| Forêt de Muntanyola (30) | Muntanyola › Osona (Barcelone) | 11 |
| Forêt de Sant Mateu de Bages (72) | Sant Mateu de Bages › Bages | 11 |
| Forêt de Saldes (33) | Saldes › Berguedà | 11 |
| Forêt de Guardiola de Berguedà (82) | Guardiola de Berguedà › Berguedà | 11 |
| Forêt de Guardiola de Berguedà (110) | Guardiola de Berguedà › Berguedà | 11 |
| Forêt de Castellar del Riu (43) | Castellar del Riu › Berguedà | 11 |
| Forêt de Lluçà (19) | Lluçà › Lluçanès | 11 |
| Forêt de Lluçà (23) | Lluçà › Lluçanès | 11 |
| Forêt de Sant Jaume de Frontanyà (22) | Sant Jaume de Frontanyà › Berguedà | 11 |
| Forêt de Castellar del Riu (53) | Castellar del Riu › Berguedà | 11 |
| Forêt de Centelles (33) | Centelles › Osona (Barcelone) | 11 |
| Forêt de Orís (16) | Orís › Osona (Barcelone) | 11 |
| Forêt de Castell de l'Areny (29) | Castell de l'Areny › Berguedà | 11 |
| Forêt de Vilanova del Vallès (17) | Vilanova del Vallès › Vallès Oriental | 11 |
| Bois de Llinars del Vallès (35) | Llinars del Vallès › Vallès Oriental | 11 |
| Bois de Esparreguera (3) | Esparreguera › Baix Llobregat | 11 |
| Forêt de Sant Feliu Sasserra (36) | Sant Feliu Sasserra › Bages | 11 |
| Forêt de Oristà (163) | Oristà › Lluçanès | 11 |
| Forêt de Cabrera d'Anoia (16) | Cabrera d'Anoia › Anoia | 11 |
| Forêt de Sant Quintí de Mediona (5) | Sant Quintí de Mediona › Alt Penedès | 11 |
| Forêt de Sant Quintí de Mediona (13) | Sant Quintí de Mediona › Alt Penedès | 11 |
| Forêt de Òdena (117) | Òdena › Anoia | 11 |
| Forêt de Tavertet (40) | Tavertet › Osona (Barcelone) | 11 |
| Forêt de Tavertet (76) | Tavertet › Osona (Barcelone) | 11 |
| Forêt de Alpens (21) | Alpens › Lluçanès | 11 |
| Forêt de Arenys de Munt (22) | Arenys de Munt › Maresme | 11 |
| Forêt de Sant Celoni (48) | Sant Celoni › Vallès Oriental | 11 |
| Forêt de Fogars de la Selva (35) | Fogars de la Selva › la Selva (Barcelone) | 11 |
| Forêt de Fogars de la Selva (43) | Fogars de la Selva › la Selva (Barcelone) | 11 |
| Forêt de Fonollosa (156) | Fonollosa › Bages | 11 |
| Forêt de Fonollosa (158) | Fonollosa › Bages | 11 |
| Forêt de el Pont de Vilomara i Rocafort (31) | el Pont de Vilomara i Rocafort › Bages | 11 |
| Forêt de Sant Martí d'Albars (7) | Sant Martí d'Albars › Lluçanès | 11 |
| Forêt de Cardona (5) | Cardona › Bages | 10 |
| Forêt de Olesa de Bonesvalls (2) | Olesa de Bonesvalls › Alt Penedès | 10 |
| Forêt de Sant Sadurní d'Osormort (8) | Sant Sadurní d'Osormort › Osona (Barcelone) | 10 |
| Forêt de Torrelavit (4) | Torrelavit › Alt Penedès | 10 |
| Forêt de la Llacuna (6) | la Llacuna › Anoia | 10 |
| Bosc de Can Mulà | Mollet del Vallès › Vallès Oriental | 10 |
| Forêt de Olesa de Bonesvalls (8) | Olesa de Bonesvalls › Alt Penedès | 10 |
| Forêt de Sant Pere de Ribes (25) | Sant Pere de Ribes › Garraf | 10 |
| Forêt de Gelida (9) | Gelida › Alt Penedès | 10 |
| Forêt de Sant Llorenç d'Hortons (9) | Sant Llorenç d'Hortons › Alt Penedès | 10 |
| Bois de Vilanova del Vallès (2) | Vilanova del Vallès › Vallès Oriental | 10 |
| Bois de Vilanova del Vallès (4) | Vilanova del Vallès › Vallès Oriental | 10 |
| Bois de Vilassar de Dalt (7) | Vilassar de Dalt › Maresme | 10 |
| Bois de la Roca del Vallès (9) | la Roca del Vallès › Vallès Oriental | 10 |
| Bois de Teià (3) | Teià › Maresme | 10 |
| Bois de la Roca del Vallès (31) | la Roca del Vallès › Vallès Oriental | 10 |
| Bois de Llinars del Vallès (14) | Llinars del Vallès › Vallès Oriental | 10 |
| Forêt de Tiana (2) | Tiana › Maresme | 10 |
| Forêt de Cardona (10) | Cardona › Bages | 10 |
| Forêt de Oristà (31) | Oristà › Lluçanès | 10 |
| Forêt de Oristà (33) | Oristà › Lluçanès | 10 |
| Forêt de Arenys de Munt (2) | Arenys de Munt › Maresme | 10 |
| Forêt de la Pobla de Lillet (4) | la Pobla de Lillet › Berguedà | 10 |
| Forêt de Saldes (7) | Saldes › Berguedà | 10 |
| Forêt de Collbató (5) | Collbató › Baix Llobregat | 10 |
| Forêt de Rubí (52) | Rubí › Vallès Occidental | 10 |
| Forêt de Rubí (54) | Rubí › Vallès Occidental | 10 |
| Forêt de Cardona (46) | Cardona › Bages | 10 |
| Forêt de l'Esquirol (111) | l'Esquirol › Osona (Barcelone) | 10 |
| Forêt de l'Esquirol (114) | l'Esquirol › Osona (Barcelone) | 10 |
| Forêt de Castellterçol (65) | Castellterçol › Moianès | 10 |
| Forêt de Castellterçol (74) | Castellterçol › Moianès | 10 |
| Forêt de Berga (41) | Berga › Berguedà | 10 |
| Forêt de Montmajor (61) | Montmajor › Berguedà | 10 |
| Forêt de Gaià (21) | Gaià › Bages | 10 |
| Forêt de Santa Maria d'Oló (24) | Santa Maria d'Oló › Moianès | 10 |
| Forêt de Santa Maria d'Oló (31) | Santa Maria d'Oló › Moianès | 10 |
| Forêt de l'Espunyola (35) | l'Espunyola › Berguedà | 10 |
| Forêt de Taradell (4) | Taradell › Osona (Barcelone) | 10 |
| Forêt de Corbera de Llobregat (18) | Corbera de Llobregat › Baix Llobregat | 10 |
| Forêt de Gelida (24) | Gelida › Alt Penedès | 10 |
| Parc del Pi Gros | Sant Vicenç dels Horts › Baix Llobregat | 10 |
| Forêt de Rubí (61) | Rubí › Vallès Occidental | 10 |
| Forêt de Vacarisses (30) | Vacarisses › Vallès Occidental | 10 |
| Forêt de Sant Vicenç de Castellet (7) | Sant Vicenç de Castellet › Bages | 10 |
| Forêt de el Bruc (19) | el Bruc › Anoia | 10 |
| Forêt de Marganell (17) | Marganell › Bages | 10 |
| Forêt de el Pont de Vilomara i Rocafort (16) | el Pont de Vilomara i Rocafort › Bages | 10 |
| Forêt de Sitges (57) | Sitges › Garraf | 10 |
| Forêt de Gavà (67) | Gavà › Baix Llobregat | 10 |
| Forêt de Gavà (73) | Gavà › Baix Llobregat | 10 |
| Forêt de Sant Salvador de Guardiola (45) | Sant Salvador de Guardiola › Bages | 10 |
| Forêt de Avinyó (80) | Avinyó › Bages | 10 |
| Forêt de Calders (43) | Calders › Moianès | 10 |
| Forêt de Calders (49) | Calders › Moianès | 10 |
| Bois de Vic (3) | Vic › Osona (Barcelone) | 10 |
| Forêt de les Franqueses del Vallès (49) | les Franqueses del Vallès › Vallès Oriental | 10 |
| Bois de Vilanova del Vallès (11) | Vilanova del Vallès › Vallès Oriental | 10 |
| Forêt de Puig-reig (51) | Puig-reig › Berguedà | 10 |
| Forêt de Castellar del Riu (25) | Castellar del Riu › Berguedà | 10 |
| Forêt de Mura (19) | Mura › Bages | 10 |
| Forêt de el Pont de Vilomara i Rocafort (24) | el Pont de Vilomara i Rocafort › Bages | 10 |
| Forêt de Castellbell i el Vilar (68) | Castellbell i el Vilar › Bages | 10 |
| Forêt de Rajadell (41) | Rajadell › Bages | 10 |
| Forêt de Vacarisses (53) | Vacarisses › Vallès Occidental | 10 |
| Forêt de Olesa de Montserrat (25) | Olesa de Montserrat › Baix Llobregat | 10 |
| Forêt de Sant Vicenç de Castellet (41) | Sant Vicenç de Castellet › Bages | 10 |
| Bosc del Cadevall | Sant Vicenç de Castellet › Bages | 10 |
| Forêt de Sant Vicenç de Castellet (44) | Sant Vicenç de Castellet › Bages | 10 |
| Forêt de Viver i Serrateix (42) | Viver i Serrateix › Berguedà | 10 |
| Forêt de Puig-reig (65) | Puig-reig › Berguedà | 10 |
| Forêt de Santa Maria de Merlès (11) | Santa Maria de Merlès › Berguedà | 10 |
| Forêt de Montmajor (77) | Montmajor › Berguedà | 10 |
| Forêt de Navàs (114) | Navàs › Bages | 10 |
| Forêt de Viver i Serrateix (82) | Viver i Serrateix › Berguedà | 10 |
| Forêt de Sant Feliu Sasserra (15) | Sant Feliu Sasserra › Bages | 10 |
| Forêt de Prats de Lluçanès (5) | Prats de Lluçanès › Lluçanès | 10 |
| Forêt de Jorba (28) | Jorba › Anoia | 10 |
| Forêt de Castellfollit del Boix (35) | Castellfollit del Boix › Bages | 10 |
| Forêt de Olivella (56) | Olivella › Garraf | 10 |
| Forêt de Begues (47) | Begues › Baix Llobregat | 10 |
| Forêt de Avinyonet del Penedès (58) | Avinyonet del Penedès › Alt Penedès | 10 |
| Forêt de Sant Pere de Ribes (93) | Sant Pere de Ribes › Garraf | 10 |
| Forêt de Cubelles (27) | Cubelles › Garraf | 10 |
| Forêt de Vilanova i la Geltrú (32) | Vilanova i la Geltrú › Garraf | 10 |
| Forêt de Castellet i la Gornal (91) | Castellet i la Gornal › Alt Penedès | 10 |
| Forêt de Vilanova i la Geltrú (43) | Vilanova i la Geltrú › Garraf | 10 |
| Forêt de Santa Maria de Merlès (78) | Santa Maria de Merlès › Berguedà | 10 |
| Forêt de Navàs (152) | Navàs › Bages | 10 |
| Forêt de Santa Maria d'Oló (45) | Santa Maria d'Oló › Moianès | 10 |
| Forêt de Sagàs (37) | Sagàs › Berguedà | 10 |
| Bois de Lliçà de Vall (8) | Lliçà de Vall › Vallès Oriental | 10 |
| Forêt de la Quar (17) | la Quar › Berguedà | 10 |
| Forêt de la Quar (19) | la Quar › Berguedà | 10 |
| Forêt de els Hostalets de Pierola (19) | els Hostalets de Pierola › Anoia | 10 |
| Forêt de Monistrol de Calders (33) | Monistrol de Calders › Moianès | 10 |
| Forêt de Monistrol de Calders (34) | Monistrol de Calders › Moianès | 10 |
| Forêt de Moià (39) | Moià › Moianès | 10 |
| Forêt de Santa Maria d'Oló (54) | Santa Maria d'Oló › Moianès | 10 |
| Forêt de Tona (4) | Tona › Osona (Barcelone) | 10 |
| Forêt de Sant Quirze Safaja (12) | Sant Quirze Safaja › Moianès | 10 |
| Forêt de el Brull (28) | el Brull › Osona (Barcelone) | 10 |
| Forêt de Fogars de Montclús (24) | Fogars de Montclús › Vallès Oriental | 10 |
| Forêt de Figaró-Montmany (10) | Figaró-Montmany › Vallès Oriental | 10 |
| Forêt de Sant Quirze Safaja (31) | Sant Quirze Safaja › Moianès | 10 |
| Forêt de l'Ametlla del Vallès (23) | l'Ametlla del Vallès › Vallès Oriental | 10 |
| Forêt de Santa Maria d'Oló (62) | Santa Maria d'Oló › Moianès | 10 |
| Forêt de Santa Eulàlia de Riuprimer (19) | Santa Eulàlia de Riuprimer › Osona (Barcelone) | 10 |
| Forêt de Sant Mateu de Bages (64) | Sant Mateu de Bages › Bages | 10 |
| Forêt de Sant Mateu de Bages (65) | Sant Mateu de Bages › Bages | 10 |
| Forêt de Cardona (97) | Cardona › Bages | 10 |
| Forêt de Guardiola de Berguedà (67) | Guardiola de Berguedà › Berguedà | 10 |
| Forêt de Dosrius (10) | Dosrius › Maresme | 10 |
| Forêt de Sant Feliu de Codines (15) | Sant Feliu de Codines › Vallès Oriental | 10 |
| Forêt de Saldes (35) | Saldes › Berguedà | 10 |
| Forêt de Vallcebre (24) | Vallcebre › Berguedà | 10 |
| Forêt de Olvan (33) | Olvan › Berguedà | 10 |
| Forêt de Bagà (61) | Bagà › Berguedà | 10 |
| Forêt de Guardiola de Berguedà (113) | Guardiola de Berguedà › Berguedà | 10 |
| Forêt de Castellar del Riu (34) | Castellar del Riu › Berguedà | 10 |
| Forêt de Fígols (25) | Fígols › Berguedà | 10 |
| Forêt de la Quar (32) | la Quar › Berguedà | 10 |
| Forêt de la Quar (33) | la Quar › Berguedà | 10 |
| Forêt de la Quar (40) | la Quar › Berguedà | 10 |
| Forêt de la Quar (42) | Sagàs › Berguedà | 10 |
| Forêt de la Pobla de Lillet (50) | la Pobla de Lillet › Berguedà | 10 |
| Forêt de Gisclareny (53) | Gisclareny › Berguedà | 10 |
| Forêt de Fígols (35) | Fígols › Berguedà | 10 |
| Forêt de Castellar del Riu (64) | Castellar del Riu › Berguedà | 10 |
| Forêt de Castellar del Riu (72) | Castellar del Riu › Berguedà | 10 |
| Forêt de Cercs (66) | Cercs › Berguedà | 10 |
| Forêt de Saldes (96) | Saldes › Berguedà | 10 |
| Forêt de Vallcebre (41) | Vallcebre › Berguedà | 10 |
| Forêt de Vallcebre (45) | Vallcebre › Berguedà | 10 |
| Forêt de Sora (27) | Sora › Osona (Barcelone) | 10 |
| Forêt de Orís (12) | Orís › Osona (Barcelone) | 10 |
| Forêt de Tordera (61) | Tordera › Maresme | 10 |
| Forêt de Cerdanyola del Vallès (61) | Cerdanyola del Vallès › Vallès Occidental | 10 |
| Forêt de Santa Margarida de Montbui (28) | Santa Margarida de Montbui › Anoia | 10 |
| Forêt de Moià (47) | Moià › Moianès | 10 |
| Forêt de Castellar de n'Hug (27) | Castellar de n'Hug › Berguedà | 10 |
| Forêt de Castellar de n'Hug (50) | Castellar de n'Hug › Berguedà | 10 |
| Forêt de Castellar de n'Hug (53) | Castellar de n'Hug › Berguedà | 10 |
| Forêt de Òdena (75) | Òdena › Anoia | 10 |
| Forêt de Font-rubí (18) | Font-rubí › Alt Penedès | 10 |
| Forêt de Lluçà (70) | Lluçà › Lluçanès | 10 |
| Forêt de Lluçà (74) | Lluçà › Lluçanès | 10 |
| Forêt de Lluçà (84) | Lluçà › Lluçanès | 10 |
| Forêt de Sant Vicenç de Montalt (8) | Sant Vicenç de Montalt › Maresme | 10 |
| Forêt de Fogars de la Selva (33) | Fogars de la Selva › la Selva (Barcelone) | 10 |
| Forêt de Fogars de la Selva (50) | Fogars de la Selva › la Selva (Barcelone) | 10 |
| Forêt de Callús (14) | Callús › Bages | 10 |
| Forêt de Castellnou de Bages (65) | Castellnou de Bages › Bages | 10 |
| Forêt de Balsareny (91) | Balsareny › Bages | 10 |
| Forêt de Vallcebre (63) | Vallcebre › Berguedà | 10 |
| Forêt de Vallcebre (64) | Vallcebre › Berguedà | 10 |
| Forêt de Taradell (34) | Taradell › Osona (Barcelone) | 10 |
| Bois de Cabrils (13) | Cabrils › Maresme | 10 |
| Forêt de Caldes de Montbui (24) | Caldes de Montbui › Vallès Oriental | 10 |
| Forêt de Calders (76) | Calders › Moianès | 10 |
| Forêt de el Pont de Vilomara i Rocafort (32) | el Pont de Vilomara i Rocafort › Bages | 10 |
| Forêt de Ullastrell (5) | Ullastrell › Vallès Occidental | 10 |
| Forêt de Viladecavalls (22) | Viladecavalls › Vallès Occidental | 10 |
| Parc Güell ⚠️ | Barcelona › Barcelonès | 9 |
| Bois de Lliçà d'Amunt (2) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 9 |
| Forêt de Masquefa ⚠️ | Masquefa › Anoia | 9 |
| Forêt de Argençola (11) ⚠️ | Argençola › Anoia | 9 |
| Forêt de Palafolls (12) ⚠️ | Palafolls › Maresme | 9 |
| Forêt de Muntanyola (3) ⚠️ | Muntanyola › Osona (Barcelone) | 9 |
| Forêt de Vilanova i la Geltrú ⚠️ | Vilanova i la Geltrú › Garraf | 9 |
| Forêt de Subirats (32) ⚠️ | Subirats › Alt Penedès | 9 |
| Forêt de Avinyonet del Penedès (41) ⚠️ | Avinyonet del Penedès › Alt Penedès | 9 |
| Forêt de Olèrdola (19) ⚠️ | Olèrdola › Alt Penedès | 9 |
| El Pont de Ferro, Riera de Marmellar ⚠️ | Castellet i la Gornal › Alt Penedès | 9 |
| Forêt de Gelida (6) ⚠️ | Gelida › Alt Penedès | 9 |
| Forêt de Sant Llorenç d'Hortons (22) ⚠️ | Sant Llorenç d'Hortons › Alt Penedès | 9 |
| Bois de la Roca del Vallès (12) ⚠️ | la Roca del Vallès › Vallès Oriental | 9 |
| Bois de Premià de Dalt (3) ⚠️ | Premià de Dalt › Maresme | 9 |
| Bois de Argentona (26) ⚠️ | Argentona › Maresme | 9 |
| Bois de la Roca del Vallès (34) ⚠️ | la Roca del Vallès › Vallès Oriental | 9 |
| Forêt de Òdena (11) ⚠️ | Òdena › Anoia | 9 |
| Bois de Llinars del Vallès (27) ⚠️ | Llinars del Vallès › Vallès Oriental | 9 |
| Forêt de Santa Maria de Palautordera (7) ⚠️ | Santa Maria de Palautordera › Vallès Oriental | 9 |
| Forêt de Badalona (3) ⚠️ | Badalona › Barcelonès | 9 |
| Forêt de l'Ametlla del Vallès (9) ⚠️ | l'Ametlla del Vallès › Vallès Oriental | 9 |
| Forêt de Oristà (32) ⚠️ | Oristà › Lluçanès | 9 |
| Forêt de Terrassa (36) ⚠️ | Terrassa › Vallès Occidental | 9 |
| Forêt de Santa Coloma de Gramenet (6) ⚠️ | Santa Coloma de Gramenet › Barcelonès | 9 |
| Bois de Ullastrell ⚠️ | Ullastrell › Vallès Occidental | 9 |
| Forêt de l'Esquirol (21) ⚠️ | l'Esquirol › Osona (Barcelone) | 9 |
| Bois de Torrelavit (2) ⚠️ | Torrelavit › Alt Penedès | 9 |
| Forêt de Seva (11) ⚠️ | Seva › Osona (Barcelone) | 9 |
| Forêt de Abrera (5) ⚠️ | Sant Esteve Sesrovires › Baix Llobregat | 9 |
| Forêt de Sallent (28) ⚠️ | Sallent › Bages | 9 |
| Forêt de Balsareny (47) ⚠️ | Balsareny › Bages | 9 |
| Forêt de Navarcles (4) ⚠️ | Navarcles › Bages | 9 |
| Forêt de Sant Fruitós de Bages (23) ⚠️ | Sant Fruitós de Bages › Bages | 9 |
| Forêt de Cànoves i Samalús (30) ⚠️ | Cànoves i Samalús › Vallès Oriental | 9 |
| Forêt de Rubí (55) ⚠️ | Rubí › Vallès Occidental | 9 |
| Forêt de Ullastrell ⚠️ | Ullastrell › Vallès Occidental | 9 |
| Forêt de Avià (12) ⚠️ | Avià › Berguedà | 9 |
| Forêt de Sant Joan de Vilatorrada (35) ⚠️ | Sant Joan de Vilatorrada › Bages | 9 |
| Forêt de Cerdanyola del Vallès (58) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 9 |
| Forêt de Sant Pere de Torelló (16) ⚠️ | Sant Pere de Torelló › Osona (Barcelone) | 9 |
| Forêt de l'Esquirol (112) ⚠️ | l'Esquirol › Osona (Barcelone) | 9 |
| Forêt de Sant Esteve Sesrovires (17) ⚠️ | Sant Esteve Sesrovires › Baix Llobregat | 9 |
| Forêt de Montmajor (63) ⚠️ | Montmajor › Berguedà | 9 |
| Forêt de Avinyó (56) ⚠️ | Avinyó › Bages | 9 |
| Forêt de Avinyó (57) ⚠️ | Avinyó › Bages | 9 |
| Forêt de Santa Maria d'Oló (18) ⚠️ | Santa Maria d'Oló › Moianès | 9 |
| Forêt de Sant Salvador de Guardiola (27) ⚠️ | Sant Salvador de Guardiola › Bages | 9 |
| Forêt de Santa Maria d'Oló (21) ⚠️ | Santa Maria d'Oló › Moianès | 9 |
| Forêt de Puig-reig (20) ⚠️ | Puig-reig › Berguedà | 9 |
| Forêt de Puig-reig (21) ⚠️ | Puig-reig › Berguedà | 9 |
| Forêt de Puig-reig (26) ⚠️ | Puig-reig › Berguedà | 9 |
| Forêt de Oristà (103) ⚠️ | Oristà › Lluçanès | 9 |
| Forêt de Sant Pol de Mar (4) ⚠️ | Sant Pol de Mar › Maresme | 9 |
| Forêt de Sant Esteve Sesrovires (19) ⚠️ | Martorell › Baix Llobregat | 9 |
| Forêt de el Papiol (3) ⚠️ | el Papiol › Baix Llobregat | 9 |
| Forêt de Castellbell i el Vilar (10) ⚠️ | Castellbell i el Vilar › Bages | 9 |
| Forêt de Vacarisses (45) ⚠️ | Vacarisses › Vallès Occidental | 9 |
| Forêt de Vacarisses (50) ⚠️ | Vacarisses › Vallès Occidental | 9 |
| Forêt de Castellbell i el Vilar (32) ⚠️ | Castellbell i el Vilar › Bages | 9 |
| Forêt de el Bruc (14) ⚠️ | el Bruc › Anoia | 9 |
| Forêt de Esparreguera (25) ⚠️ | Esparreguera › Baix Llobregat | 9 |
| Forêt de Castellbell i el Vilar (44) ⚠️ | Castellbell i el Vilar › Bages | 9 |
| Forêt de Castellbell i el Vilar (50) ⚠️ | Castellbell i el Vilar › Bages | 9 |
| Forêt de Castellbell i el Vilar (59) ⚠️ | Castellbell i el Vilar › Bages | 9 |
| Forêt de Sant Pere de Ribes (86) ⚠️ | Sant Pere de Ribes › Garraf | 9 |
| Forêt de Sitges (22) ⚠️ | Sitges › Garraf | 9 |
| Forêt de Sitges (32) ⚠️ | Sitges › Garraf | 9 |
| Forêt de Sant Salvador de Guardiola (44) ⚠️ | Sant Salvador de Guardiola › Bages | 9 |
| Forêt de Marganell (25) ⚠️ | Marganell › Bages | 9 |
| Forêt de Sant Salvador de Guardiola (50) ⚠️ | Sant Salvador de Guardiola › Bages | 9 |
| Forêt de Sant Salvador de Guardiola (55) ⚠️ | Sant Salvador de Guardiola › Bages | 9 |
| Forêt de Artés (23) ⚠️ | Artés › Bages | 9 |
| Forêt de Cardedeu (27) ⚠️ | Cardedeu › Vallès Oriental | 9 |
| Forêt de Llinars del Vallès (70) ⚠️ | Llinars del Vallès › Vallès Oriental | 9 |
| Bosc Negre ⚠️ | Cardedeu › Vallès Oriental | 9 |
| Forêt de Vallromanes (9) ⚠️ | Vallromanes › Vallès Oriental | 9 |
| Forêt de Gaià (56) ⚠️ | Gaià › Bages | 9 |
| Forêt de Sant Jaume de Frontanyà (11) ⚠️ | Sant Jaume de Frontanyà › Berguedà | 9 |
| Forêt de Talamanca (22) ⚠️ | Talamanca › Bages | 9 |
| Forêt de Castellbell i el Vilar (67) ⚠️ | Castellbell i el Vilar › Bages | 9 |
| Forêt de Sant Pere Sallavinera (15) ⚠️ | Sant Pere Sallavinera › Anoia | 9 |
| Forêt de Rajadell (46) ⚠️ | Rajadell › Bages | 9 |
| Forêt de Sant Salvador de Guardiola (64) ⚠️ | Sant Salvador de Guardiola › Bages | 9 |
| Forêt de Sant Salvador de Guardiola (66) ⚠️ | Sant Salvador de Guardiola › Bages | 9 |
| Forêt de Castellfollit del Boix (26) ⚠️ | Castellfollit del Boix › Bages | 9 |
| Forêt de Sant Salvador de Guardiola (89) ⚠️ | Sant Salvador de Guardiola › Bages | 9 |
| Forêt de Sant Salvador de Guardiola (102) ⚠️ | Sant Salvador de Guardiola › Bages | 9 |
| Forêt de Sant Salvador de Guardiola (116) ⚠️ | Sant Salvador de Guardiola › Bages | 9 |
| Forêt de el Bruc (42) ⚠️ | el Bruc › Anoia | 9 |
| Forêt de Olesa de Montserrat (19) ⚠️ | Olesa de Montserrat › Baix Llobregat | 9 |
| Forêt de Abrera (24) ⚠️ | Abrera › Baix Llobregat | 9 |
| Forêt de Castellbisbal (20) ⚠️ | Castellbisbal › Vallès Occidental | 9 |
| Forêt de Martorell (27) ⚠️ | Martorell › Baix Llobregat | 9 |
| Forêt de Navàs (84) ⚠️ | Navàs › Bages | 9 |
| Forêt de Viver i Serrateix (27) ⚠️ | Viver i Serrateix › Berguedà | 9 |
| Forêt de Casserres (22) ⚠️ | Casserres › Berguedà | 9 |
| Forêt de Sant Mateu de Bages (51) ⚠️ | Sant Mateu de Bages › Bages | 9 |
| Forêt de Súria (29) ⚠️ | Súria › Bages | 9 |
| Forêt de Viver i Serrateix (71) ⚠️ | Viver i Serrateix › Berguedà | 9 |
| Forêt de Montmajor (127) ⚠️ | Montmajor › Berguedà | 9 |
| Forêt de Avinyó (111) ⚠️ | Avinyó › Bages | 9 |
| Forêt de Avinyó (112) ⚠️ | Avinyó › Bages | 9 |
| Forêt de Borredà (20) ⚠️ | Borredà › Berguedà | 9 |
| Forêt de Vilanova del Vallès (8) ⚠️ | Vilanova del Vallès › Vallès Oriental | 9 |
| Forêt de Taradell (6) ⚠️ | Taradell › Osona (Barcelone) | 9 |
| Forêt de Vilanova del Camí (12) ⚠️ | Vilanova del Camí › Anoia | 9 |
| Forêt de Begues (41) ⚠️ | Begues › Baix Llobregat | 9 |
| Forêt de Olivella (103) ⚠️ | Olivella › Garraf | 9 |
| Forêt de Olèrdola (63) ⚠️ | Olèrdola › Alt Penedès | 9 |
| Forêt de Vilanova i la Geltrú (58) ⚠️ | Vilanova i la Geltrú › Garraf | 9 |
| Forêt de Avinyonet del Penedès (67) ⚠️ | Avinyonet del Penedès › Alt Penedès | 9 |
| Forêt de Avinyonet del Penedès (70) ⚠️ | Avinyonet del Penedès › Alt Penedès | 9 |
| Forêt de Monistrol de Calders (23) ⚠️ | Monistrol de Calders › Moianès | 9 |
| Forêt de Monistrol de Calders (27) ⚠️ | Monistrol de Calders › Moianès | 9 |
| Forêt de Sant Julià de Cerdanyola (9) ⚠️ | Sant Julià de Cerdanyola › Berguedà | 9 |
| Forêt de Sallent (92) ⚠️ | Sallent › Bages | 9 |
| Forêt de Tavertet (32) ⚠️ | Tavertet › Osona (Barcelone) | 9 |
| Forêt de Viver i Serrateix (110) ⚠️ | Viver i Serrateix › Berguedà | 9 |
| Forêt de Viver i Serrateix (111) ⚠️ | Viver i Serrateix › Berguedà | 9 |
| Forêt de Viver i Serrateix (113) ⚠️ | Viver i Serrateix › Berguedà | 9 |
| Forêt de Sagàs (31) ⚠️ | Sagàs › Berguedà | 9 |
| Forêt de Santa Maria de Merlès (87) ⚠️ | Santa Maria de Merlès › Berguedà | 9 |
| Forêt de Santa Maria de Merlès (95) ⚠️ | Santa Maria de Merlès › Berguedà | 9 |
| Forêt de Santa Maria de Merlès (110) ⚠️ | Santa Maria de Merlès › Berguedà | 9 |
| Bois de Lliçà de Vall (6) ⚠️ | Lliçà de Vall › Vallès Oriental | 9 |
| Forêt de Avià (49) ⚠️ | Avià › Berguedà | 9 |
| Forêt de la Garriga (45) ⚠️ | la Garriga › Vallès Oriental | 9 |
| Forêt de Centelles (18) ⚠️ | Centelles › Osona (Barcelone) | 9 |
| Forêt de Tagamanent (31) ⚠️ | Tagamanent › Vallès Oriental | 9 |
| Forêt de Tagamanent (32) ⚠️ | Tagamanent › Vallès Oriental | 9 |
| Forêt de Tagamanent (35) ⚠️ | Tagamanent › Vallès Oriental | 9 |
| Forêt de Cànoves i Samalús (42) ⚠️ | Cànoves i Samalús › Vallès Oriental | 9 |
| Forêt de el Brull (36) ⚠️ | el Brull › Osona (Barcelone) | 9 |
| Forêt de Montseny (20) ⚠️ | Montseny › Vallès Oriental | 9 |
| Forêt de Gualba (4) ⚠️ | Gualba › Vallès Oriental | 9 |
| Forêt de Sant Quirze Safaja (21) ⚠️ | Sant Quirze Safaja › Moianès | 9 |
| Forêt de Castellterçol (78) ⚠️ | Castellterçol › Moianès | 9 |
| Forêt de Castellterçol (80) ⚠️ | Castellterçol › Moianès | 9 |
| Forêt de Oristà (114) ⚠️ | Oristà › Lluçanès | 9 |
| Forêt de Sant Mateu de Bages (59) ⚠️ | Sant Mateu de Bages › Bages | 9 |
| Forêt de Cardona (71) ⚠️ | Cardona › Bages | 9 |
| Forêt de Dosrius (7) ⚠️ | Dosrius › Maresme | 9 |
| Forêt de Sagàs (39) ⚠️ | Sagàs › Berguedà | 9 |
| Parc del Falgar i la Verneda ⚠️ | les Franqueses del Vallès › Vallès Oriental | 9 |
| Forêt de Tona (30) ⚠️ | Tona › Osona (Barcelone) | 9 |
| Forêt de Saldes (32) ⚠️ | Saldes › Berguedà | 9 |
| Forêt de Saldes (57) ⚠️ | Saldes › Berguedà | 9 |
| Forêt de Gisclareny (34) ⚠️ | Gisclareny › Berguedà | 9 |
| Forêt de Gisclareny (41) ⚠️ | Gisclareny › Berguedà | 9 |
| Forêt de Guardiola de Berguedà (118) ⚠️ | Guardiola de Berguedà › Berguedà | 9 |
| Forêt de Castellar del Riu (39) ⚠️ | Castellar del Riu › Berguedà | 9 |
| Forêt de Fígols (33) ⚠️ | Fígols › Berguedà | 9 |
| Forêt de la Quar (38) ⚠️ | la Quar › Berguedà | 9 |
| Forêt de Sagàs (52) ⚠️ | Sagàs › Berguedà | 9 |
| Forêt de la Pobla de Lillet (47) ⚠️ | la Pobla de Lillet › Berguedà | 9 |
| Forêt de Castellar del Riu (61) ⚠️ | Castellar del Riu › Berguedà | 9 |
| Forêt de Castellar del Riu (63) ⚠️ | Castellar del Riu › Berguedà | 9 |
| Forêt de Cercs (59) ⚠️ | Cercs › Berguedà | 9 |
| Forêt de Saldes (84) ⚠️ | Saldes › Berguedà | 9 |
| Forêt de Gisclareny (71) ⚠️ | Gisclareny › Berguedà | 9 |
| Forêt de Gisclareny (73) ⚠️ | Gisclareny › Berguedà | 9 |
| Forêt de Collsuspina (14) ⚠️ | Collsuspina › Moianès | 9 |
| Forêt de Alella (2) ⚠️ | Alella › Maresme | 9 |
| Forêt de Oristà (159) ⚠️ | Oristà › Lluçanès | 9 |
| Forêt de Òdena (56) ⚠️ | Òdena › Anoia | 9 |
| Forêt de Abrera (32) ⚠️ | Abrera › Baix Llobregat | 9 |
| Forêt de Mediona (53) ⚠️ | Mediona › Alt Penedès | 9 |
| Forêt de Torrelavit (27) ⚠️ | Torrelavit › Alt Penedès | 9 |
| Forêt de Torrelavit (49) ⚠️ | Torrelavit › Alt Penedès | 9 |
| Forêt de Mediona (72) ⚠️ | la Llacuna › Anoia | 9 |
| Forêt de Font-rubí (21) ⚠️ | Font-rubí › Alt Penedès | 9 |
| Forêt de Òdena (101) ⚠️ | Òdena › Anoia | 9 |
| Forêt de Tavertet (50) ⚠️ | Tavertet › Osona (Barcelone) | 9 |
| Forêt de Lluçà (77) ⚠️ | Lluçà › Lluçanès | 9 |
| Forêt de Alpens (29) ⚠️ | Alpens › Lluçanès | 9 |
| Forêt de Sant Cebrià de Vallalta (15) ⚠️ | Sant Cebrià de Vallalta › Maresme | 9 |
| Forêt de Arenys de Munt (12) ⚠️ | Arenys de Munt › Maresme | 9 |
| Forêt de Dosrius (36) ⚠️ | Sant Vicenç de Montalt › Maresme | 9 |
| Forêt de Arenys de Munt (20) ⚠️ | Arenys de Munt › Maresme | 9 |
| Forêt de Sant Vicenç de Montalt (5) ⚠️ | Sant Vicenç de Montalt › Maresme | 9 |
| Forêt de Arenys de Munt (27) ⚠️ | Arenys de Munt › Maresme | 9 |
| Forêt de Fogars de la Selva (45) ⚠️ | Fogars de la Selva › la Selva (Barcelone) | 9 |
| Forêt de Tordera (114) ⚠️ | Tordera › Maresme | 9 |
| Forêt de Gualba (12) ⚠️ | Gualba › Vallès Oriental | 9 |
| Forêt de Santpedor (18) ⚠️ | Santpedor › Bages | 9 |
| Forêt de Callús (24) ⚠️ | Callús › Bages | 9 |
| Forêt de Rupit i Pruit (39) ⚠️ | Rupit i Pruit › Osona (Barcelone) | 9 |
| Forêt de Vallcebre (70) ⚠️ | Vallcebre › Berguedà | 9 |
| Forêt de Vallcebre (75) ⚠️ | Vallcebre › Berguedà | 9 |
| Forêt de Castellterçol (81) ⚠️ | Castellterçol › Moianès | 9 |
| Forêt de Lliçà d'Amunt (19) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 9 |
| Forêt de Moià (67) ⚠️ | Moià › Moianès | 9 |
| Forêt de Sant Fruitós de Bages (45) ⚠️ | Sant Fruitós de Bages › Bages | 9 |
| Forêt de Terrassa (96) ⚠️ | Terrassa › Vallès Occidental | 9 |
| Forêt de el Brull (43) ⚠️ | el Brull › Osona (Barcelone) | 9 |
| Forêt de Gavà ⚠️ | Gavà › Baix Llobregat | 8 |
| Forêt de Lliçà d'Amunt ⚠️ | Lliçà d'Amunt › Vallès Oriental | 8 |
| Forêt de l'Esquirol (9) ⚠️ | l'Esquirol › Osona (Barcelone) | 8 |
| Forêt de Pujalt (6) ⚠️ | Pujalt › Anoia | 8 |
| Bosc de Can Baró ⚠️ | Sant Pere de Ribes › Garraf | 8 |
| Forêt de Terrassa (17) ⚠️ | Terrassa › Vallès Occidental | 8 |
| Forêt de Avinyonet del Penedès (14) ⚠️ | Avinyonet del Penedès › Alt Penedès | 8 |
| Forêt de Gavà (17) ⚠️ | Gavà › Baix Llobregat | 8 |
| Parc Central del Vallès ⚠️ | Barberà del Vallès › Vallès Occidental | 8 |
| Forêt de Caldes de Montbui (2) ⚠️ | Caldes de Montbui › Vallès Oriental | 8 |
| Bois de Vilassar de Dalt (10) ⚠️ | Vilassar de Dalt › Maresme | 8 |
| Bois de Vilassar de Dalt (11) ⚠️ | Vilassar de Dalt › Maresme | 8 |
| Bois de Argentona (17) ⚠️ | Argentona › Maresme | 8 |
| Bois de Argentona (28) ⚠️ | Argentona › Maresme | 8 |
| Bois de la Roca del Vallès (28) ⚠️ | la Roca del Vallès › Vallès Oriental | 8 |
| Forêt de Tiana (4) ⚠️ | Tiana › Maresme | 8 |
| Forêt de Sant Salvador de Guardiola (15) ⚠️ | Sant Salvador de Guardiola › Bages | 8 |
| Bois de Santa Margarida i els Monjos (2) ⚠️ | Santa Margarida i els Monjos › Alt Penedès | 8 |
| Forêt de Olivella (50) ⚠️ | Olivella › Garraf | 8 |
| Bois de Argençola (4) ⚠️ | Argençola › Anoia | 8 |
| Bois de Argençola (5) ⚠️ | Argençola › Anoia | 8 |
| Bois de Montmaneu (17) ⚠️ | Montmaneu › Anoia | 8 |
| Forêt de Sant Pere de Vilamajor (7) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 8 |
| Bois de Torrelles de Foix ⚠️ | Torrelles de Foix › Alt Penedès | 8 |
| Bois de Torrelles de Foix (3) ⚠️ | Torrelles de Foix › Alt Penedès | 8 |
| Bois de Veciana (7) ⚠️ | Veciana › Anoia | 8 |
| Forêt de Subirats (85) ⚠️ | Subirats › Alt Penedès | 8 |
| Parc de la Ciutadella ⚠️ | Barcelona › Barcelonès | 8 |
| Forêt de Sant Esteve de Palautordera (3) ⚠️ | Sant Esteve de Palautordera › Vallès Oriental | 8 |
| Forêt de Avinyó (21) ⚠️ | Avinyó › Bages | 8 |
| Forêt de Calders (24) ⚠️ | Calders › Moianès | 8 |
| Forêt de Manresa (37) ⚠️ | Manresa › Bages | 8 |
| Forêt de Rubí (60) ⚠️ | Rubí › Vallès Occidental | 8 |
| Forêt de Rajadell (28) ⚠️ | Rajadell › Bages | 8 |
| Forêt de Castellterçol (34) ⚠️ | Castellterçol › Moianès | 8 |
| Bois de Castellterçol (10) ⚠️ | Castellterçol › Moianès | 8 |
| Forêt de Castell de l'Areny (2) ⚠️ | Castell de l'Areny › Berguedà | 8 |
| Forêt de Sant Joan de Vilatorrada (39) ⚠️ | Sant Joan de Vilatorrada › Bages | 8 |
| Forêt de Fonollosa (116) ⚠️ | Fonollosa › Bages | 8 |
| Parc de l'Hostal del Fum ⚠️ | Palau-solità i Plegamans › Vallès Occidental | 8 |
| Forêt de Prats de Lluçanès (2) ⚠️ | Prats de Lluçanès › Lluçanès | 8 |
| Forêt de Berga (39) ⚠️ | Berga › Berguedà | 8 |
| Forêt de Montclar (10) ⚠️ | Montclar › Berguedà | 8 |
| Forêt de Montmajor (46) ⚠️ | Montmajor › Berguedà | 8 |
| Forêt de Montmajor (52) ⚠️ | Montmajor › Berguedà | 8 |
| Forêt de Masquefa (14) ⚠️ | Masquefa › Anoia | 8 |
| Forêt de Sallent (54) ⚠️ | Sallent › Bages | 8 |
| Forêt de Avinyó (55) ⚠️ | Avinyó › Bages | 8 |
| Forêt de Navàs (24) ⚠️ | Navàs › Bages | 8 |
| Forêt de Puig-reig (15) ⚠️ | Puig-reig › Berguedà | 8 |
| Forêt de Puig-reig (17) ⚠️ | Puig-reig › Berguedà | 8 |
| Forêt de Santa Maria d'Oló (27) ⚠️ | Santa Maria d'Oló › Moianès | 8 |
| Forêt de l'Espunyola (37) ⚠️ | l'Espunyola › Berguedà | 8 |
| Forêt de l'Espunyola (44) ⚠️ | l'Espunyola › Berguedà | 8 |
| Forêt de la Nou de Berguedà (8) ⚠️ | la Nou de Berguedà › Berguedà | 8 |
| Forêt de la Pobla de Claramunt (6) ⚠️ | la Pobla de Claramunt › Anoia | 8 |
| Forêt de Sant Pol de Mar (10) ⚠️ | Sant Pol de Mar › Maresme | 8 |
| Forêt de Cervelló (11) ⚠️ | Cervelló › Baix Llobregat | 8 |
| Forêt de Vacarisses (23) ⚠️ | Vacarisses › Vallès Occidental | 8 |
| Forêt de Esparreguera (19) ⚠️ | Esparreguera › Baix Llobregat | 8 |
| Forêt de Collbató (7) ⚠️ | Collbató › Baix Llobregat | 8 |
| Forêt de Marganell (12) ⚠️ | Marganell › Bages | 8 |
| Forêt de Marganell (16) ⚠️ | Marganell › Bages | 8 |
| Forêt de el Pont de Vilomara i Rocafort (14) ⚠️ | el Pont de Vilomara i Rocafort › Bages | 8 |
| Forêt de Sitges (56) ⚠️ | Sitges › Garraf | 8 |
| Forêt de Sitges (65) ⚠️ | Sitges › Garraf | 8 |
| Forêt de Begues (34) ⚠️ | Begues › Baix Llobregat | 8 |
| Forêt de Begues (36) ⚠️ | Begues › Baix Llobregat | 8 |
| Forêt de el Bruc (31) ⚠️ | el Bruc › Anoia | 8 |
| Forêt de Artés (18) ⚠️ | Artés › Bages | 8 |
| Forêt de Avinyó (85) ⚠️ | Avinyó › Bages | 8 |
| Forêt de Llinars del Vallès (57) ⚠️ | Llinars del Vallès › Vallès Oriental | 8 |
| Forêt de Súria (18) ⚠️ | Súria › Bages | 8 |
| Bosc de Vilalba ⚠️ | la Roca del Vallès › Vallès Oriental | 8 |
| Forêt de Vilanova del Vallès (4) ⚠️ | Vilanova del Vallès › Vallès Oriental | 8 |
| Bois de Vilanova del Vallès (9) ⚠️ | Vilanova del Vallès › Vallès Oriental | 8 |
| Forêt de Avinyó (90) ⚠️ | Avinyó › Bages | 8 |
| Forêt de Navàs (34) ⚠️ | Navàs › Bages | 8 |
| Forêt de Gaià (37) ⚠️ | Gaià › Bages | 8 |
| Forêt de Castell de l'Areny (15) ⚠️ | Castell de l'Areny › Berguedà | 8 |
| Forêt de Borredà (15) ⚠️ | Borredà › Berguedà | 8 |
| Forêt de la Pobla de Lillet (27) ⚠️ | la Pobla de Lillet › Berguedà | 8 |
| Forêt de Castellar de n'Hug (11) ⚠️ | Castellar de n'Hug › Berguedà | 8 |
| Forêt de Sant Jaume de Frontanyà (10) ⚠️ | Sant Jaume de Frontanyà › Berguedà | 8 |
| Forêt de Guardiola de Berguedà (58) ⚠️ | Guardiola de Berguedà › Berguedà | 8 |
| Forêt de Terrassa (74) ⚠️ | Terrassa › Vallès Occidental | 8 |
| Forêt de Castellbisbal (21) ⚠️ | Castellbisbal › Vallès Occidental | 8 |
| Forêt de Martorell (20) ⚠️ | Martorell › Baix Llobregat | 8 |
| Forêt de Martorell (21) ⚠️ | Martorell › Baix Llobregat | 8 |
| Forêt de Castellgalí (32) ⚠️ | Castellgalí › Bages | 8 |
| Forêt de Castellgalí (47) ⚠️ | Castellgalí › Bages | 8 |
| Forêt de Navàs (55) ⚠️ | Navàs › Bages | 8 |
| Forêt de Puig-reig (67) ⚠️ | Puig-reig › Berguedà | 8 |
| Forêt de Puig-reig (77) ⚠️ | Puig-reig › Berguedà | 8 |
| Forêt de Sagàs (14) ⚠️ | Sagàs › Berguedà | 8 |
| Forêt de Avià (17) ⚠️ | Avià › Berguedà | 8 |
| Forêt de Avià (22) ⚠️ | Avià › Berguedà | 8 |
| Forêt de Capolat (25) ⚠️ | Capolat › Berguedà | 8 |
| Forêt de Capolat (30) ⚠️ | Capolat › Berguedà | 8 |
| Forêt de Avià (45) ⚠️ | Avià › Berguedà | 8 |
| Forêt de Capolat (31) ⚠️ | Capolat › Berguedà | 8 |
| Forêt de Montmajor (88) ⚠️ | Montmajor › Berguedà | 8 |
| Forêt de Montmajor (98) ⚠️ | Montmajor › Berguedà | 8 |
| Forêt de Navàs (138) ⚠️ | Navàs › Bages | 8 |
| Forêt de Montmajor (126) ⚠️ | Montmajor › Berguedà | 8 |
| Forêt de Gaià (66) ⚠️ | Gaià › Bages | 8 |
| Forêt de Borredà (30) ⚠️ | Borredà › Berguedà | 8 |
| Forêt de Santa Margarida de Montbui (17) ⚠️ | Santa Margarida de Montbui › Anoia | 8 |
| Forêt de Òdena (44) ⚠️ | Òdena › Anoia | 8 |
| Forêt de Castellfollit del Boix (36) ⚠️ | Castellfollit del Boix › Bages | 8 |
| Forêt de Cubelles (17) ⚠️ | Cubelles › Garraf | 8 |
| Forêt de Cubelles (23) ⚠️ | Cubelles › Garraf | 8 |
| Forêt de Olivella (68) ⚠️ | Olivella › Garraf | 8 |
| Forêt de Begues (46) ⚠️ | Begues › Baix Llobregat | 8 |
| Forêt de Begues (55) ⚠️ | Begues › Baix Llobregat | 8 |
| Forêt de Begues (67) ⚠️ | Begues › Baix Llobregat | 8 |
| Forêt de Olesa de Bonesvalls (48) ⚠️ | Olesa de Bonesvalls › Alt Penedès | 8 |
| Forêt de Castellet i la Gornal (87) ⚠️ | Castellet i la Gornal › Alt Penedès | 8 |
| Forêt de Canyelles (11) ⚠️ | Canyelles › Garraf | 8 |
| Forêt de Canyelles (12) ⚠️ | Canyelles › Garraf | 8 |
| Forêt de Canyelles (15) ⚠️ | Canyelles › Garraf | 8 |
| Forêt de Canyelles (17) ⚠️ | Canyelles › Garraf | 8 |
| Forêt de Avinyonet del Penedès (63) ⚠️ | Avinyonet del Penedès › Alt Penedès | 8 |
| Forêt de Gisclareny (9) ⚠️ | Gisclareny › Berguedà | 8 |
| Forêt de Bagà (26) ⚠️ | Bagà › Berguedà | 8 |
| Forêt de Sant Jaume de Frontanyà (20) ⚠️ | Sant Jaume de Frontanyà › Berguedà | 8 |
| Forêt de Sagàs (27) ⚠️ | Sagàs › Berguedà | 8 |
| Forêt de Santa Maria de Merlès (91) ⚠️ | Santa Maria de Merlès › Berguedà | 8 |
| Forêt de Fogars de Montclús (19) ⚠️ | Fogars de Montclús › Vallès Oriental | 8 |
| Forêt de Montseny (18) ⚠️ | Montseny › Vallès Oriental | 8 |
| Forêt de Bigues i Riells del Fai (21) ⚠️ | Bigues i Riells del Fai › Vallès Oriental | 8 |
| Forêt de l'Estany (9) ⚠️ | l'Estany › Moianès | 8 |
| Forêt de Oristà (112) ⚠️ | Oristà › Lluçanès | 8 |
| Forêt de Oristà (150) ⚠️ | Oristà › Lluçanès | 8 |
| Forêt de Cardona (73) ⚠️ | Cardona › Bages | 8 |
| Forêt de Sant Mateu de Bages (101) ⚠️ | Sant Mateu de Bages › Bages | 8 |
| Forêt de Bagà (33) ⚠️ | Bagà › Berguedà | 8 |
| Forêt de Lluçà (10) ⚠️ | Lluçà › Lluçanès | 8 |
| Forêt de la Roca del Vallès (12) ⚠️ | la Roca del Vallès › Vallès Oriental | 8 |
| Forêt de Balenyà (11) ⚠️ | Balenyà › Osona (Barcelone) | 8 |
| Forêt de Vallcebre (23) ⚠️ | Vallcebre › Berguedà | 8 |
| Forêt de Saldes (51) ⚠️ | Saldes › Berguedà | 8 |
| Forêt de Saldes (69) ⚠️ | Saldes › Berguedà | 8 |
| Forêt de Bagà (35) ⚠️ | Bagà › Berguedà | 8 |
| Forêt de Bagà (59) ⚠️ | Bagà › Berguedà | 8 |
| Forêt de Guardiola de Berguedà (107) ⚠️ | Guardiola de Berguedà › Berguedà | 8 |
| Forêt de Capolat (37) ⚠️ | Capolat › Berguedà | 8 |
| Forêt de Lluçà (35) ⚠️ | Lluçà › Lluçanès | 8 |
| Forêt de Borredà (78) ⚠️ | Borredà › Berguedà | 8 |
| Forêt de Sagàs (51) ⚠️ | Sagàs › Berguedà | 8 |
| Forêt de Santa Maria de Merlès (143) ⚠️ | Santa Maria de Merlès › Berguedà | 8 |
| Forêt de Sagàs (53) ⚠️ | Sagàs › Berguedà | 8 |
| Forêt de Sagàs (54) ⚠️ | Sagàs › Berguedà | 8 |
| Forêt de la Pobla de Lillet (62) ⚠️ | la Pobla de Lillet › Berguedà | 8 |
| Forêt de Castellar del Riu (60) ⚠️ | Castellar del Riu › Berguedà | 8 |
| Forêt de Castellar del Riu (67) ⚠️ | Castellar del Riu › Berguedà | 8 |
| Forêt de Castellar del Riu (68) ⚠️ | Castellar del Riu › Berguedà | 8 |
| Forêt de Castellar del Riu (74) ⚠️ | Castellar del Riu › Berguedà | 8 |
| Forêt de Cercs (60) ⚠️ | Cercs › Berguedà | 8 |
| Forêt de Saldes (98) ⚠️ | Saldes › Berguedà | 8 |
| Forêt de Puig-reig (81) ⚠️ | Puig-reig › Berguedà | 8 |
| Forêt de Gisclareny (74) ⚠️ | Gisclareny › Berguedà | 8 |
| Forêt de Centelles (30) ⚠️ | Centelles › Osona (Barcelone) | 8 |
| Forêt de Orís (9) ⚠️ | Orís › Osona (Barcelone) | 8 |
| Forêt de la Pobla de Lillet (63) ⚠️ | la Pobla de Lillet › Berguedà | 8 |
| Forêt de la Pobla de Lillet (64) ⚠️ | la Pobla de Lillet › Berguedà | 8 |
| Forêt de Tordera (59) ⚠️ | Tordera › Maresme | 8 |
| Forêt de Badalona (31) ⚠️ | Badalona › Barcelonès | 8 |
| Forêt de Teià (2) ⚠️ | Teià › Maresme | 8 |
| Forêt de Saldes (134) ⚠️ | Saldes › Berguedà | 8 |
| Forêt de Castellar de n'Hug (52) ⚠️ | Castellar de n'Hug › Berguedà | 8 |
| Forêt de Òdena (76) ⚠️ | Òdena › Anoia | 8 |
| Forêt de Vallirana (35) ⚠️ | Vallirana › Baix Llobregat | 8 |
| Forêt de Mediona (57) ⚠️ | Mediona › Alt Penedès | 8 |
| Forêt de Puig-reig (92) ⚠️ | Viver i Serrateix › Berguedà | 8 |
| Forêt de Tavertet (51) ⚠️ | Tavertet › Osona (Barcelone) | 8 |
| Forêt de Tavertet (55) ⚠️ | Tavertet › Osona (Barcelone) | 8 |
| Forêt de Sant Cebrià de Vallalta (13) ⚠️ | Sant Cebrià de Vallalta › Maresme | 8 |
| Forêt de Arenys de Munt (25) ⚠️ | Arenys de Munt › Maresme | 8 |
| Forêt de Dosrius (39) ⚠️ | Dosrius › Maresme | 8 |
| Forêt de Sant Celoni (63) ⚠️ | Sant Celoni › Vallès Oriental | 8 |
| Forêt de Gualba (9) ⚠️ | Gualba › Vallès Oriental | 8 |
| Forêt de Gualba (23) ⚠️ | Gualba › Vallès Oriental | 8 |
| Forêt de Casserres (39) ⚠️ | Casserres › Berguedà | 8 |
| Forêt de Sant Mateu de Bages (111) ⚠️ | Sant Mateu de Bages › Bages | 8 |
| Forêt de Vallcebre (68) ⚠️ | Vallcebre › Berguedà | 8 |
| Forêt de Sant Sadurní d'Osormort (34) ⚠️ | Sant Sadurní d'Osormort › Osona (Barcelone) | 8 |
| Forêt de Tavèrnoles (10) ⚠️ | Tavèrnoles › Osona (Barcelone) | 8 |
| Forêt de Taradell (33) ⚠️ | Taradell › Osona (Barcelone) | 8 |
| Forêt de Castellterçol (82) ⚠️ | Castellterçol › Moianès | 8 |
| Forêt de Olost (12) ⚠️ | Olost › Lluçanès | 8 |
| Forêt de Olost (17) ⚠️ | Olost › Lluçanès | 8 |
| Forêt de Sant Martí d'Albars (6) ⚠️ | Sant Martí d'Albars › Lluçanès | 8 |
| Forêt de Tordera (3) ⚠️ | Tordera › Maresme | 7 |
| Forêt de Alpens (2) ⚠️ | Alpens › Lluçanès | 7 |
| Forêt de Montmajor ⚠️ | Montmajor › Berguedà | 7 |
| Forêt de Alpens (4) ⚠️ | Alpens › Lluçanès | 7 |
| Forêt de Castellar del Vallès (3) ⚠️ | Castellar del Vallès › Vallès Occidental | 7 |
| Forêt de Vilanova de Sau (8) ⚠️ | Vilanova de Sau › Osona (Barcelone) | 7 |
| Forêt de Bellprat (5) ⚠️ | Bellprat › Anoia | 7 |
| Forêt de l'Esquirol (11) ⚠️ | l'Esquirol › Osona (Barcelone) | 7 |
| Forêt de Sant Pere de Torelló (6) ⚠️ | Sant Pere de Torelló › Osona (Barcelone) | 7 |
| Forêt de la Garriga (3) ⚠️ | la Garriga › Vallès Oriental | 7 |
| Forêt de Torrelles de Llobregat (3) ⚠️ | Torrelles de Llobregat › Baix Llobregat | 7 |
| Forêt de Viladecans (3) ⚠️ | Viladecans › Baix Llobregat | 7 |
| Forêt de Sabadell (3) ⚠️ | Sabadell › Vallès Occidental | 7 |
| Forêt de Olivella ⚠️ | Olivella › Garraf | 7 |
| Forêt de Avinyonet del Penedès (37) ⚠️ | Avinyonet del Penedès › Alt Penedès | 7 |
| Forêt de Sant Pere de Ribes (13) ⚠️ | Sant Pere de Ribes › Garraf | 7 |
| Forêt de Piera (4) ⚠️ | Piera › Anoia | 7 |
| Forêt de Calders ⚠️ | Calders › Moianès | 7 |
| Forêt de Castellet i la Gornal (40) ⚠️ | Castellet i la Gornal › Alt Penedès | 7 |
| Forêt de Castellví de la Marca (8) ⚠️ | Castellví de la Marca › Alt Penedès | 7 |
| Forêt de Sant Llorenç d'Hortons (23) ⚠️ | Sant Llorenç d'Hortons › Alt Penedès | 7 |
| Forêt de Torrelavit (5) ⚠️ | Torrelavit › Alt Penedès | 7 |
| Forêt de el Pla del Penedès (2) ⚠️ | el Pla del Penedès › Alt Penedès | 7 |
| Forêt de el Pla del Penedès (5) ⚠️ | el Pla del Penedès › Alt Penedès | 7 |
| Forêt de Vilobí del Penedès (5) ⚠️ | Vilobí del Penedès › Alt Penedès | 7 |
| Bois de Òrrius (4) ⚠️ | Òrrius › Maresme | 7 |
| Bois de la Roca del Vallès (3) ⚠️ | la Roca del Vallès › Vallès Oriental | 7 |
| Bois de Òrrius (12) ⚠️ | Òrrius › Maresme | 7 |
| Bois de Òrrius (16) ⚠️ | Òrrius › Maresme | 7 |
| Bois de Argentona (27) ⚠️ | Argentona › Maresme | 7 |
| Bois de la Roca del Vallès (20) ⚠️ | la Roca del Vallès › Vallès Oriental | 7 |
| Forêt de l'Ametlla del Vallès (4) ⚠️ | l'Ametlla del Vallès › Vallès Oriental | 7 |
| Forêt de Santa Coloma de Gramenet ⚠️ | Santa Coloma de Gramenet › Barcelonès | 7 |
| Forêt de Sant Llorenç Savall (6) ⚠️ | Sant Llorenç Savall › Vallès Occidental | 7 |
| Forêt de Oristà (44) ⚠️ | Oristà › Lluçanès | 7 |
| Forêt de Esparreguera ⚠️ | Esparreguera › Baix Llobregat | 7 |
| Forêt de Viver i Serrateix (12) ⚠️ | Viver i Serrateix › Berguedà | 7 |
| Bois de Sant Cugat del Vallès (95) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 7 |
| Forêt de Canyelles (3) ⚠️ | Canyelles › Garraf | 7 |
| Forêt de Taradell (3) ⚠️ | Taradell › Osona (Barcelone) | 7 |
| Bois de Argençola (2) ⚠️ | Argençola › Anoia | 7 |
| Bois de Montmaneu (20) ⚠️ | Montmaneu › Anoia | 7 |
| Bois de Montmaneu (28) ⚠️ | Montmaneu › Anoia | 7 |
| Forêt de Muntanyola (14) ⚠️ | Muntanyola › Osona (Barcelone) | 7 |
| Forêt de Tordera (41) ⚠️ | Tordera › Maresme | 7 |
| Parc de Granollers (23) ⚠️ | Granollers › Vallès Oriental | 7 |
| Forêt de Montmajor (27) ⚠️ | Montmajor › Berguedà | 7 |
| Forêt de Cerdanyola del Vallès (52) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 7 |
| Forêt de Aguilar de Segarra (16) ⚠️ | Aguilar de Segarra › Bages | 7 |
| Forêt de Aguilar de Segarra (17) ⚠️ | Aguilar de Segarra › Bages | 7 |
| Forêt de Cercs (5) ⚠️ | Cercs › Berguedà | 7 |
| Forêt de Avinyó (23) ⚠️ | Avinyó › Bages | 7 |
| Forêt de Sallent (49) ⚠️ | Sallent › Bages | 7 |
| Forêt de Balsareny (32) ⚠️ | Balsareny › Bages | 7 |
| Forêt de Balsareny (45) ⚠️ | Balsareny › Bages | 7 |
| Forêt de Manresa (35) ⚠️ | Manresa › Bages | 7 |
| Forêt de Rubí (53) ⚠️ | Rubí › Vallès Occidental | 7 |
| Forêt de els Hostalets de Pierola (14) ⚠️ | els Hostalets de Pierola › Anoia | 7 |
| Forêt de Lliçà d'Amunt (17) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 7 |
| Forêt de Avià (13) ⚠️ | Avià › Berguedà | 7 |
| Forêt de Berga (34) ⚠️ | Berga › Berguedà | 7 |
| Bosc de l'Oller ⚠️ | Manresa › Bages | 7 |
| Forêt de Sant Sadurní d'Anoia (25) ⚠️ | Sant Sadurní d'Anoia › Alt Penedès | 7 |
| Forêt de Balsareny (52) ⚠️ | Balsareny › Bages | 7 |
| Forêt de Gaià (19) ⚠️ | Gaià › Bages | 7 |
| Forêt de Oristà (90) ⚠️ | Oristà › Lluçanès | 7 |
| Forêt de Santa Maria d'Oló (19) ⚠️ | Santa Maria d'Oló › Moianès | 7 |
| Forêt de Sant Salvador de Guardiola (32) ⚠️ | Sant Salvador de Guardiola › Bages | 7 |
| Forêt de Puig-reig (10) ⚠️ | Puig-reig › Berguedà | 7 |
| Forêt de Puig-reig (40) ⚠️ | Puig-reig › Berguedà | 7 |
| Bois de Barcelona (102) ⚠️ | Barcelona › Barcelonès | 7 |
| Parc de Diagonal Mar ⚠️ | Barcelona › Barcelonès | 7 |
| Forêt de Sant Esteve Sesrovires (24) ⚠️ | Sant Esteve Sesrovires › Baix Llobregat | 7 |
| Forêt de Malla (4) ⚠️ | Malla › Osona (Barcelone) | 7 |
| Forêt de Corbera de Llobregat (24) ⚠️ | Corbera de Llobregat › Baix Llobregat | 7 |
| Forêt de Rubí (71) ⚠️ | Rubí › Vallès Occidental | 7 |
| Forêt de Monistrol de Montserrat (11) ⚠️ | Monistrol de Montserrat › Bages | 7 |
| Forêt de Monistrol de Montserrat (40) ⚠️ | Monistrol de Montserrat › Bages | 7 |
| Forêt de Bagà (14) ⚠️ | Bagà › Berguedà | 7 |
| Forêt de Castellbell i el Vilar (21) ⚠️ | Castellbell i el Vilar › Bages | 7 |
| Forêt de el Bruc (17) ⚠️ | el Bruc › Anoia | 7 |
| Forêt de Marganell (23) ⚠️ | Marganell › Bages | 7 |
| Forêt de Castellolí (9) ⚠️ | Castellolí › Anoia | 7 |
| Forêt de Castellbell i el Vilar (52) ⚠️ | Castellbell i el Vilar › Bages | 7 |
| Forêt de Moià (23) ⚠️ | Moià › Moianès | 7 |
| Forêt de Sitges (35) ⚠️ | Sitges › Garraf | 7 |
| Forêt de Castelldefels (12) ⚠️ | Castelldefels › Baix Llobregat | 7 |
| Forêt de Sitges (63) ⚠️ | Sitges › Garraf | 7 |
| Forêt de Manresa (123) ⚠️ | Manresa › Bages | 7 |
| Forêt de Santa Maria d'Oló (35) ⚠️ | Santa Maria d'Oló › Moianès | 7 |
| Forêt de Llinars del Vallès (61) ⚠️ | Llinars del Vallès › Vallès Oriental | 7 |
| Forêt de les Franqueses del Vallès (45) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 7 |
| Forêt de Castell de l'Areny (22) ⚠️ | Castell de l'Areny › Berguedà | 7 |
| Forêt de la Pobla de Lillet (20) ⚠️ | la Pobla de Lillet › Berguedà | 7 |
| Forêt de Castellar de n'Hug (14) ⚠️ | Castellar de n'Hug › Berguedà | 7 |
| Forêt de Sant Jaume de Frontanyà (8) ⚠️ | Sant Jaume de Frontanyà › Berguedà | 7 |
| Forêt de la Nou de Berguedà (16) ⚠️ | la Nou de Berguedà › Berguedà | 7 |
| Forêt de Mura (27) ⚠️ | Mura › Bages | 7 |
| Forêt de Monistrol de Calders (22) ⚠️ | Monistrol de Calders › Moianès | 7 |
| Forêt de Aguilar de Segarra (29) ⚠️ | Aguilar de Segarra › Bages | 7 |
| Forêt de Aguilar de Segarra (37) ⚠️ | Aguilar de Segarra › Bages | 7 |
| Forêt de Sant Pere Sallavinera (8) ⚠️ | Sant Pere Sallavinera › Anoia | 7 |
| Forêt de Viladecavalls (11) ⚠️ | Viladecavalls › Vallès Occidental | 7 |
| Forêt de Rajadell (45) ⚠️ | Rajadell › Bages | 7 |
| Forêt de Sant Salvador de Guardiola (59) ⚠️ | Sant Salvador de Guardiola › Bages | 7 |
| Forêt de Sant Salvador de Guardiola (93) ⚠️ | Sant Salvador de Guardiola › Bages | 7 |
| Forêt de Sant Salvador de Guardiola (103) ⚠️ | Sant Salvador de Guardiola › Bages | 7 |
| Forêt de el Bruc (36) ⚠️ | el Bruc › Anoia | 7 |
| Forêt de Vacarisses (58) ⚠️ | Vacarisses › Vallès Occidental | 7 |
| Forêt de Olesa de Montserrat (20) ⚠️ | Olesa de Montserrat › Baix Llobregat | 7 |
| Forêt de Esparreguera (33) ⚠️ | Esparreguera › Baix Llobregat | 7 |
| Forêt de Castellbisbal (22) ⚠️ | Castellbisbal › Vallès Occidental | 7 |
| Forêt de Martorell (25) ⚠️ | Martorell › Baix Llobregat | 7 |
| Forêt de Martorell (26) ⚠️ | Martorell › Baix Llobregat | 7 |
| Forêt de Martorell (28) ⚠️ | Martorell › Baix Llobregat | 7 |
| Forêt de Navàs (86) ⚠️ | Navàs › Bages | 7 |
| Forêt de Viver i Serrateix (34) ⚠️ | Viver i Serrateix › Berguedà | 7 |
| Forêt de Navàs (92) ⚠️ | Navàs › Bages | 7 |
| Forêt de Santa Maria de Merlès (17) ⚠️ | Santa Maria de Merlès › Berguedà | 7 |
| Forêt de Olvan (16) ⚠️ | Olvan › Berguedà | 7 |
| Forêt de Avià (32) ⚠️ | Avià › Berguedà | 7 |
| Forêt de Avià (36) ⚠️ | Avià › Berguedà | 7 |
| Forêt de Capolat (27) ⚠️ | Capolat › Berguedà | 7 |
| Forêt de Navàs (97) ⚠️ | Navàs › Bages | 7 |
| Forêt de Navàs (123) ⚠️ | Navàs › Bages | 7 |
| Forêt de Súria (32) ⚠️ | Súria › Bages | 7 |
| Forêt de Viver i Serrateix (92) ⚠️ | Viver i Serrateix › Berguedà | 7 |
| Forêt de Santa Maria de Merlès (54) ⚠️ | Santa Maria de Merlès › Berguedà | 7 |
| Forêt de Santa Maria de Merlès (60) ⚠️ | Santa Maria de Merlès › Berguedà | 7 |
| Forêt de Santa Maria d'Oló (39) ⚠️ | Santa Maria d'Oló › Moianès | 7 |
| Bois de Sant Cugat del Vallès (117) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 7 |
| Forêt de Sant Cugat del Vallès (124) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 7 |
| Forêt de Barcelona (57) ⚠️ | Barcelona › Barcelonès | 7 |
| Forêt de Rubí (84) ⚠️ | Rubí › Vallès Occidental | 7 |
| Forêt de la Quar (12) ⚠️ | la Quar › Berguedà | 7 |
| Bois de els Hostalets de Pierola ⚠️ | els Hostalets de Pierola › Anoia | 7 |
| Forêt de Jorba (16) ⚠️ | Jorba › Anoia | 7 |
| Forêt de Igualada (9) ⚠️ | Igualada › Anoia | 7 |
| Forêt de Òdena (45) ⚠️ | Igualada › Anoia | 7 |
| Forêt de Igualada (13) ⚠️ | Òdena › Anoia | 7 |
| Forêt de la Pobla de Claramunt (17) ⚠️ | la Pobla de Claramunt › Anoia | 7 |
| Forêt de Castellet i la Gornal (66) ⚠️ | Castellet i la Gornal › Alt Penedès | 7 |
| Forêt de Avinyonet del Penedès (61) ⚠️ | Avinyonet del Penedès › Alt Penedès | 7 |
| Forêt de Sant Pere de Ribes (106) ⚠️ | Sant Pere de Ribes › Garraf | 7 |
| Forêt de Castellet i la Gornal (88) ⚠️ | Castellet i la Gornal › Alt Penedès | 7 |
| Forêt de Vilanova i la Geltrú (50) ⚠️ | Vilanova i la Geltrú › Garraf | 7 |
| Forêt de Vilanova i la Geltrú (54) ⚠️ | Vilanova i la Geltrú › Garraf | 7 |
| Forêt de Canyelles (25) ⚠️ | Canyelles › Garraf | 7 |
| Forêt de Avinyonet del Penedès (62) ⚠️ | Avinyonet del Penedès › Alt Penedès | 7 |
| Forêt de Olivella (126) ⚠️ | Olivella › Garraf | 7 |
| Forêt de Santa Maria de Merlès (70) ⚠️ | Santa Maria de Merlès › Berguedà | 7 |
| Forêt de Santa Maria de Merlès (80) ⚠️ | Santa Maria de Merlès › Berguedà | 7 |
| Forêt de Santa Maria de Merlès (98) ⚠️ | Santa Maria de Merlès › Berguedà | 7 |
| Forêt de Santa Maria de Merlès (99) ⚠️ | Santa Maria de Merlès › Berguedà | 7 |
| Forêt de Santa Maria de Merlès (120) ⚠️ | Santa Maria de Merlès › Berguedà | 7 |
| Forêt de Berga (62) ⚠️ | Berga › Berguedà | 7 |
| Forêt de els Hostalets de Pierola (27) ⚠️ | els Hostalets de Pierola › Anoia | 7 |
| Forêt de Monistrol de Calders (32) ⚠️ | Monistrol de Calders › Moianès | 7 |
| Forêt de Granera (28) ⚠️ | Granera › Moianès | 7 |
| Forêt de Bagà (32) ⚠️ | Bagà › Berguedà | 7 |
| Forêt de Fogars de Montclús (15) ⚠️ | Fogars de Montclús › Vallès Oriental | 7 |
| Forêt de Fogars de Montclús (17) ⚠️ | Fogars de Montclús › Vallès Oriental | 7 |
| Forêt de Montseny (14) ⚠️ | Montseny › Vallès Oriental | 7 |
| Forêt de Montseny (17) ⚠️ | Montseny › Vallès Oriental | 7 |
| Forêt de Sant Quirze Safaja (15) ⚠️ | Sant Quirze Safaja › Moianès | 7 |
| Forêt de l'Ametlla del Vallès (19) ⚠️ | l'Ametlla del Vallès › Vallès Oriental | 7 |
| Forêt de Sant Quirze Safaja (22) ⚠️ | Sant Quirze Safaja › Moianès | 7 |
| Forêt de Sant Quirze Safaja (34) ⚠️ | Sant Quirze Safaja › Moianès | 7 |
| Forêt de Sant Quirze Safaja (36) ⚠️ | Bigues i Riells del Fai › Vallès Oriental | 7 |
| Forêt de Sant Quirze Safaja (38) ⚠️ | Sant Quirze Safaja › Moianès | 7 |
| Forêt de Bigues i Riells del Fai (24) ⚠️ | Bigues i Riells del Fai › Vallès Oriental | 7 |
| Forêt de l'Ametlla del Vallès (20) ⚠️ | l'Ametlla del Vallès › Vallès Oriental | 7 |
| Forêt de Monistrol de Calders (43) ⚠️ | Monistrol de Calders › Moianès | 7 |
| Forêt de Santa Maria d'Oló (63) ⚠️ | Santa Maria d'Oló › Moianès | 7 |
| Forêt de Muntanyola (29) ⚠️ | Muntanyola › Osona (Barcelone) | 7 |
| Forêt de Oristà (142) ⚠️ | Oristà › Lluçanès | 7 |
| Forêt de Sant Mateu de Bages (57) ⚠️ | Sant Mateu de Bages › Bages | 7 |
| Forêt de Calonge de Segarra (14) ⚠️ | Calonge de Segarra › Anoia | 7 |
| Forêt de Dosrius (25) ⚠️ | Dosrius › Maresme | 7 |
| Forêt de Balenyà (10) ⚠️ | Balenyà › Osona (Barcelone) | 7 |
| Forêt de Tona (16) ⚠️ | Tona › Osona (Barcelone) | 7 |
| Forêt de Tona (23) ⚠️ | Tona › Osona (Barcelone) | 7 |
| Forêt de Saldes (49) ⚠️ | Saldes › Berguedà | 7 |
| Forêt de Saldes (50) ⚠️ | Saldes › Berguedà | 7 |
| Forêt de Olvan (22) ⚠️ | Olvan › Berguedà | 7 |
| Forêt de Bagà (45) ⚠️ | Bagà › Berguedà | 7 |
| Forêt de Guardiola de Berguedà (91) ⚠️ | Guardiola de Berguedà › Berguedà | 7 |
| Forêt de Guardiola de Berguedà (119) ⚠️ | Guardiola de Berguedà › Berguedà | 7 |
| Forêt de Capolat (38) ⚠️ | Capolat › Berguedà | 7 |
| Forêt de Capolat (39) ⚠️ | Capolat › Berguedà | 7 |
| Forêt de Castellar del Riu (41) ⚠️ | Castellar del Riu › Berguedà | 7 |
| Forêt de Prats de Lluçanès (22) ⚠️ | Prats de Lluçanès › Lluçanès | 7 |
| Forêt de Lluçà (24) ⚠️ | Lluçà › Lluçanès | 7 |
| Forêt de Sant Martí d'Albars ⚠️ | Prats de Lluçanès › Lluçanès | 7 |
| Forêt de Lluçà (36) ⚠️ | Lluçà › Lluçanès | 7 |
| Forêt de Lluçà (39) ⚠️ | Lluçà › Lluçanès | 7 |
| Forêt de Borredà (81) ⚠️ | Borredà › Berguedà | 7 |
| Forêt de la Pobla de Lillet (48) ⚠️ | la Pobla de Lillet › Berguedà | 7 |
| Forêt de Castellar del Riu (73) ⚠️ | Castellar del Riu › Berguedà | 7 |
| Forêt de Cercs (62) ⚠️ | Cercs › Berguedà | 7 |
| Forêt de Cercs (64) ⚠️ | Cercs › Berguedà | 7 |
| Forêt de Saldes (87) ⚠️ | Saldes › Berguedà | 7 |
| Forêt de Saldes (93) ⚠️ | Saldes › Berguedà | 7 |
| Forêt de Vallcebre (42) ⚠️ | Vallcebre › Berguedà | 7 |
| Forêt de Orís (21) ⚠️ | Orís › Osona (Barcelone) | 7 |
| Forêt de Tordera (64) ⚠️ | Tordera › Maresme | 7 |
| Forêt de Fogars de la Selva (21) ⚠️ | Fogars de la Selva › la Selva (Barcelone) | 7 |
| Forêt de Santa Coloma de Gramenet (9) ⚠️ | Santa Coloma de Gramenet › Barcelonès | 7 |
| Forêt de Vallromanes (20) ⚠️ | Vallromanes › Vallès Oriental | 7 |
| Forêt de Guardiola de Berguedà (125) ⚠️ | Guardiola de Berguedà › Berguedà | 7 |
| Forêt de Saldes (135) ⚠️ | Saldes › Berguedà | 7 |
| Forêt de Guardiola de Berguedà (138) ⚠️ | Guardiola de Berguedà › Berguedà | 7 |
| Forêt de Calders (70) ⚠️ | Calders › Moianès | 7 |
| Forêt de Castellar de n'Hug (43) ⚠️ | Castellar de n'Hug › Berguedà | 7 |
| Forêt de Castellar de n'Hug (54) ⚠️ | Castellar de n'Hug › Berguedà | 7 |
| Forêt de Oristà (160) ⚠️ | Oristà › Lluçanès | 7 |
| Forêt de Carme (4) ⚠️ | Carme › Anoia | 7 |
| Forêt de la Torre de Claramunt (5) ⚠️ | la Torre de Claramunt › Anoia | 7 |
| Forêt de la Torre de Claramunt (7) ⚠️ | la Torre de Claramunt › Anoia | 7 |
| Forêt de Piera (39) ⚠️ | Piera › Anoia | 7 |
| Forêt de Montmajor (140) ⚠️ | Montmajor › Berguedà | 7 |
| Forêt de Esparreguera (49) ⚠️ | Esparreguera › Baix Llobregat | 7 |
| Forêt de Vilanova del Camí (25) ⚠️ | Vilanova del Camí › Anoia | 7 |
| Forêt de Cabrera d'Anoia (15) ⚠️ | Cabrera d'Anoia › Anoia | 7 |
| Forêt de Cabrera d'Anoia (34) ⚠️ | Cabrera d'Anoia › Anoia | 7 |
| Forêt de Sant Pere de Riudebitlles (13) ⚠️ | Sant Pere de Riudebitlles › Alt Penedès | 7 |
| Forêt de Casserres (27) ⚠️ | Casserres › Berguedà | 7 |
| Forêt de Tavertet (47) ⚠️ | Tavertet › Osona (Barcelone) | 7 |
| Forêt de Tavertet (80) ⚠️ | Tavertet › Osona (Barcelone) | 7 |
| Forêt de Borredà (132) ⚠️ | Borredà › Berguedà | 7 |
| Forêt de Alpens (17) ⚠️ | Alpens › Lluçanès | 7 |
| Forêt de Alpens (20) ⚠️ | Alpens › Lluçanès | 7 |
| Forêt de Lluçà (64) ⚠️ | Lluçà › Lluçanès | 7 |
| Forêt de Lluçà (73) ⚠️ | Lluçà › Lluçanès | 7 |
| Forêt de Casserres (32) ⚠️ | Casserres › Berguedà | 7 |
| Forêt de Sallent (108) ⚠️ | Sallent › Bages | 7 |
| Forêt de Santpedor (12) ⚠️ | Santpedor › Bages | 7 |
| Forêt de Castellnou de Bages (64) ⚠️ | Castellnou de Bages › Bages | 7 |
| Forêt de Castellnou de Bages (79) ⚠️ | Castellnou de Bages › Bages | 7 |
| Forêt de Fonollosa (145) ⚠️ | Fonollosa › Bages | 7 |
| Forêt de Vallcebre (73) ⚠️ | Vallcebre › Berguedà | 7 |
| Forêt de Vallcebre (77) ⚠️ | Vallcebre › Berguedà | 7 |
| Forêt de Sant Julià de Vilatorta (5) ⚠️ | Sant Julià de Vilatorta › Osona (Barcelone) | 7 |
| Forêt de Sant Sadurní d'Osormort (40) ⚠️ | Sant Sadurní d'Osormort › Osona (Barcelone) | 7 |
| Forêt de Sant Sadurní d'Osormort (46) ⚠️ | Sant Sadurní d'Osormort › Osona (Barcelone) | 7 |
| Forêt de Taradell (32) ⚠️ | Taradell › Osona (Barcelone) | 7 |
| Forêt de Taradell (43) ⚠️ | Taradell › Osona (Barcelone) | 7 |
| Forêt de Santpedor (85) ⚠️ | Sant Fruitós de Bages › Bages | 7 |
| Forêt de el Pont de Vilomara i Rocafort (36) ⚠️ | el Pont de Vilomara i Rocafort › Bages | 7 |
| Forêt de el Pont de Vilomara i Rocafort (40) ⚠️ | el Pont de Vilomara i Rocafort › Bages | 7 |
| Forêt de Tordera ⚠️ | Tordera › Maresme | 6 |
| Parc del Carmel ⚠️ | Barcelona › Barcelonès | 6 |
| Bois de Lliçà d'Amunt (9) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 6 |
| Bois de Lliçà d'Amunt (10) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 6 |
| Bois de Lliçà de Vall ⚠️ | Lliçà de Vall › Vallès Oriental | 6 |
| Forêt de els Hostalets de Pierola (2) ⚠️ | els Hostalets de Pierola › Anoia | 6 |
| Bois de Cerdanyola del Vallès ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 6 |
| Forêt de Oristà (6) ⚠️ | Oristà › Lluçanès | 6 |
| Can Gambus ⚠️ | Sabadell › Vallès Occidental | 6 |
| Forêt de Santa Coloma de Cervelló ⚠️ | Santa Coloma de Cervelló › Baix Llobregat | 6 |
| Forêt de Viladecans (4) ⚠️ | Viladecans › Baix Llobregat | 6 |
| Forêt de Sant Pere de Ribes (5) ⚠️ | Sant Pere de Ribes › Garraf | 6 |
| Bosc de Solers ⚠️ | Sant Pere de Ribes › Garraf | 6 |
| Avetosa del Montseny ⚠️ | Fogars de Montclús › Vallès Oriental | 6 |
| Forêt de Avinyonet del Penedès (28) ⚠️ | Sant Cugat Sesgarrigues › Alt Penedès | 6 |
| Forêt de Olèrdola (17) ⚠️ | Olèrdola › Alt Penedès | 6 |
| Forêt de Terrassa (25) ⚠️ | Terrassa › Vallès Occidental | 6 |
| Parc Serra de Galliners ⚠️ | Terrassa › Vallès Occidental | 6 |
| Forêt de Subirats (69) ⚠️ | Subirats › Alt Penedès | 6 |
| Forêt de el Pla del Penedès (3) ⚠️ | el Pla del Penedès › Alt Penedès | 6 |
| Parc Nou ⚠️ | el Prat de Llobregat › Baix Llobregat | 6 |
| Bois de Argentona ⚠️ | Argentona › Maresme | 6 |
| Bois de la Roca del Vallès (8) ⚠️ | la Roca del Vallès › Vallès Oriental | 6 |
| Bois de Vilassar de Dalt (5) ⚠️ | Vilassar de Dalt › Maresme | 6 |
| Bois de la Roca del Vallès (15) ⚠️ | la Roca del Vallès › Vallès Oriental | 6 |
| Bois de Teià ⚠️ | Teià › Maresme | 6 |
| Bois de Vallromanes (9) ⚠️ | Vallromanes › Vallès Oriental | 6 |
| Bois de la Roca del Vallès (21) ⚠️ | la Roca del Vallès › Vallès Oriental | 6 |
| Bois de la Roca del Vallès (23) ⚠️ | la Roca del Vallès › Vallès Oriental | 6 |
| Bois de la Roca del Vallès (29) ⚠️ | la Roca del Vallès › Vallès Oriental | 6 |
| Bois de Llinars del Vallès (3) ⚠️ | Llinars del Vallès › Vallès Oriental | 6 |
| Bois de Llinars del Vallès (10) ⚠️ | Llinars del Vallès › Vallès Oriental | 6 |
| Bois de Llinars del Vallès (13) ⚠️ | Llinars del Vallès › Vallès Oriental | 6 |
| Forêt de Sant Pere de Torelló (12) ⚠️ | Sant Pere de Torelló › Osona (Barcelone) | 6 |
| Bois de Tiana (2) ⚠️ | Tiana › Maresme | 6 |
| Forêt de Palau-solità i Plegamans (7) ⚠️ | Palau-solità i Plegamans › Vallès Occidental | 6 |
| Forêt de Sant Boi de Llobregat (3) ⚠️ | Sant Boi de Llobregat › Baix Llobregat | 6 |
| Zona Verda Sector Sant Llàtzer ⚠️ | Vic › Osona (Barcelone) | 6 |
| Forêt de Sant Fost de Campsentelles (5) ⚠️ | Sant Fost de Campsentelles › Vallès Oriental | 6 |
| Parc de el Prat de Llobregat (14) ⚠️ | el Prat de Llobregat › Baix Llobregat | 6 |
| Forêt de Palafolls (23) ⚠️ | Palafolls › Maresme | 6 |
| Bois de Calldetenes ⚠️ | Calldetenes › Osona (Barcelone) | 6 |
| Finca de la Baronia de Viver ⚠️ | Argentona › Maresme | 6 |
| Forêt de Oristà (42) ⚠️ | Oristà › Lluçanès | 6 |
| Bois de Rubí (5) ⚠️ | Rubí › Vallès Occidental | 6 |
| Bois de Rubí (7) ⚠️ | Rubí › Vallès Occidental | 6 |
| Forêt de Rubí (6) ⚠️ | Rubí › Vallès Occidental | 6 |
| Forêt de la Llacuna (7) ⚠️ | la Llacuna › Anoia | 6 |
| Bois de les Franqueses del Vallès (2) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 6 |
| Forêt de Vic (2) ⚠️ | Vic › Osona (Barcelone) | 6 |
| Bois de Caldes de Montbui ⚠️ | Caldes de Montbui › Vallès Oriental | 6 |
| Bosc de Can Catafal ⚠️ | Vilanova del Vallès › Vallès Oriental | 6 |
| Bois de Cànoves i Samalús ⚠️ | Cànoves i Samalús › Vallès Oriental | 6 |
| Forêt de la Garriga (7) ⚠️ | la Garriga › Vallès Oriental | 6 |
| Bois de Montmaneu (24) ⚠️ | Montmaneu › Anoia | 6 |
| Forêt de l'Esquirol (83) ⚠️ | l'Esquirol › Osona (Barcelone) | 6 |
| Forêt de Tordera (24) ⚠️ | Tordera › Maresme | 6 |
| Bois de el Pla del Penedès ⚠️ | el Pla del Penedès › Alt Penedès | 6 |
| Forêt de Torrelavit (24) ⚠️ | Torrelavit › Alt Penedès | 6 |
| Bois de Jorba (5) ⚠️ | Jorba › Anoia | 6 |
| Bois de Copons (6) ⚠️ | Copons › Anoia | 6 |
| Bois de Santa Maria de Miralles (2) ⚠️ | Bellprat › Anoia | 6 |
| Forêt de el Brull (8) ⚠️ | el Brull › Osona (Barcelone) | 6 |
| Forêt de Aguilar de Segarra (18) ⚠️ | Aguilar de Segarra › Bages | 6 |
| Forêt de Fonollosa (89) ⚠️ | Fonollosa › Bages | 6 |
| Parc de Can Dragó ⚠️ | Barcelona › Barcelonès | 6 |
| Forêt de el Bruc (9) ⚠️ | el Bruc › Anoia | 6 |
| Forêt de Monistrol de Montserrat (8) ⚠️ | Monistrol de Montserrat › Bages | 6 |
| Forêt de Balsareny (19) ⚠️ | Balsareny › Bages | 6 |
| Forêt de Balsareny (31) ⚠️ | Balsareny › Bages | 6 |
| Forêt de Sallent (50) ⚠️ | Sallent › Bages | 6 |
| Forêt de Calders (11) ⚠️ | Calders › Moianès | 6 |
| Forêt de Manresa (27) ⚠️ | Manresa › Bages | 6 |
| Forêt de Manresa (28) ⚠️ | Manresa › Bages | 6 |
| Bois de Viladecavalls (7) ⚠️ | Viladecavalls › Vallès Occidental | 6 |
| Forêt de Rajadell (32) ⚠️ | Rajadell › Bages | 6 |
| Forêt de Castellterçol (37) ⚠️ | Castellterçol › Moianès | 6 |
| Forêt de Sant Joan de Vilatorrada (38) ⚠️ | Sant Joan de Vilatorrada › Bages | 6 |
| Forêt de Sant Joan de Vilatorrada (49) ⚠️ | Sant Joan de Vilatorrada › Bages | 6 |
| Forêt de Cardona (40) ⚠️ | Cardona › Bages | 6 |
| Forêt de Fonollosa (113) ⚠️ | Fonollosa › Bages | 6 |
| Forêt de Saldes (10) ⚠️ | Saldes › Berguedà | 6 |
| Forêt de Saldes (11) ⚠️ | Saldes › Berguedà | 6 |
| Bois de Palau-solità i Plegamans (13) ⚠️ | Palau-solità i Plegamans › Vallès Occidental | 6 |
| Forêt de Aiguafreda (12) ⚠️ | Aiguafreda › Osona (Barcelone) | 6 |
| Forêt de Castellterçol (55) ⚠️ | Castellterçol › Moianès | 6 |
| Forêt de Castellterçol (64) ⚠️ | Castellterçol › Moianès | 6 |
| Forêt de Avià (15) ⚠️ | Avià › Berguedà | 6 |
| Forêt de Berga (40) ⚠️ | Berga › Berguedà | 6 |
| Forêt de Berga (48) ⚠️ | Berga › Berguedà | 6 |
| Forêt de Berga (61) ⚠️ | Berga › Berguedà | 6 |
| Forêt de Saldes (16) ⚠️ | Saldes › Berguedà | 6 |
| Forêt de Puig-reig (9) ⚠️ | Puig-reig › Berguedà | 6 |
| Forêt de Gaià (17) ⚠️ | Gaià › Bages | 6 |
| Forêt de Avinyó (51) ⚠️ | Avinyó › Bages | 6 |
| Forêt de Sallent (55) ⚠️ | Sallent › Bages | 6 |
| Forêt de Sallent (69) ⚠️ | Sallent › Bages | 6 |
| Forêt de Capolat (12) ⚠️ | Capolat › Berguedà | 6 |
| Forêt de Puig-reig (38) ⚠️ | Puig-reig › Berguedà | 6 |
| Forêt de Oristà (102) ⚠️ | Oristà › Lluçanès | 6 |
| Forêt de Castellar del Riu (15) ⚠️ | Castellar del Riu › Berguedà | 6 |
| Forêt de Sant Salvador de Guardiola (38) ⚠️ | Sant Salvador de Guardiola › Bages | 6 |
| Forêt de Sant Salvador de Guardiola (40) ⚠️ | Sant Salvador de Guardiola › Bages | 6 |
| Forêt de Sant Salvador de Guardiola (43) ⚠️ | Sant Salvador de Guardiola › Bages | 6 |
| Forêt de Castellnou de Bages (47) ⚠️ | Castellnou de Bages › Bages | 6 |
| Bois de Palau-solità i Plegamans (14) ⚠️ | Palau-solità i Plegamans › Vallès Occidental | 6 |
| Forêt de Santa Margarida de Montbui (11) ⚠️ | Santa Margarida de Montbui › Anoia | 6 |
| Forêt de Calella (2) ⚠️ | Calella › Maresme | 6 |
| Forêt de Calella (6) ⚠️ | Calella › Maresme | 6 |
| Forêt de Corbera de Llobregat (13) ⚠️ | Corbera de Llobregat › Baix Llobregat | 6 |
| Parc de Sant Julià d'Auvèrnia ⚠️ | Vic › Osona (Barcelone) | 6 |
| Forêt de Vic (17) ⚠️ | Vic › Osona (Barcelone) | 6 |
| Forêt de Taradell (5) ⚠️ | Taradell › Osona (Barcelone) | 6 |
| Forêt de Rubí (62) ⚠️ | Rubí › Vallès Occidental | 6 |
| Forêt de Rubí (67) ⚠️ | Rubí › Vallès Occidental | 6 |
| Forêt de Castellbell i el Vilar (12) ⚠️ | Castellbell i el Vilar › Bages | 6 |
| Forêt de Castellbell i el Vilar (19) ⚠️ | Castellbell i el Vilar › Bages | 6 |
| Forêt de Sant Vicenç de Castellet (11) ⚠️ | Sant Vicenç de Castellet › Bages | 6 |
| Forêt de Esparreguera (22) ⚠️ | Esparreguera › Baix Llobregat | 6 |
| Forêt de Marganell (18) ⚠️ | Marganell › Bages | 6 |
| Forêt de Castellbell i el Vilar (39) ⚠️ | Castellbell i el Vilar › Bages | 6 |
| Forêt de Castellolí (11) ⚠️ | Castellolí › Anoia | 6 |
| Forêt de Castellbell i el Vilar (60) ⚠️ | Castellbell i el Vilar › Bages | 6 |
| Forêt de el Pont de Vilomara i Rocafort (18) ⚠️ | el Pont de Vilomara i Rocafort › Bages | 6 |
| Forêt de Moià (21) ⚠️ | Moià › Moianès | 6 |
| Forêt de Sitges (47) ⚠️ | Sitges › Garraf | 6 |
| Forêt de Gavà (68) ⚠️ | Gavà › Baix Llobregat | 6 |
| Forêt de Castellgalí (21) ⚠️ | Castellgalí › Bages | 6 |
| Forêt de Sant Salvador de Guardiola (48) ⚠️ | Sant Salvador de Guardiola › Bages | 6 |
| Forêt de el Bruc (33) ⚠️ | el Bruc › Anoia | 6 |
| Forêt de Artés (20) ⚠️ | Artés › Bages | 6 |
| Forêt de Artés (28) ⚠️ | Artés › Bages | 6 |
| Forêt de Avinyó (87) ⚠️ | Avinyó › Bages | 6 |
| Forêt de Cànoves i Samalús (35) ⚠️ | Cànoves i Samalús › Vallès Oriental | 6 |
| Forêt de Llinars del Vallès (63) ⚠️ | Llinars del Vallès › Vallès Oriental | 6 |
| Forêt de les Franqueses del Vallès (46) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 6 |
| Forêt de Cànoves i Samalús (36) ⚠️ | Cànoves i Samalús › Vallès Oriental | 6 |
| Forêt de Vilanova del Vallès (5) ⚠️ | Vilanova del Vallès › Vallès Oriental | 6 |
| Forêt de Vilanova del Vallès (6) ⚠️ | Vilanova del Vallès › Vallès Oriental | 6 |
| Forêt de Vilanova del Vallès (7) ⚠️ | Vilanova del Vallès › Vallès Oriental | 6 |
| Forêt de Sallent (82) ⚠️ | Sallent › Bages | 6 |
| Forêt de Sallent (85) ⚠️ | Sallent › Bages | 6 |
| Forêt de Avinyó (94) ⚠️ | Avinyó › Bages | 6 |
| Forêt de Avinyó (99) ⚠️ | Avinyó › Bages | 6 |
| Forêt de Avinyó (102) ⚠️ | Avinyó › Bages | 6 |
| Forêt de Gaià (41) ⚠️ | Gaià › Bages | 6 |
| Forêt de Sant Esteve de Palautordera (7) ⚠️ | Sant Esteve de Palautordera › Vallès Oriental | 6 |
| Forêt de Santa Maria de Palautordera (24) ⚠️ | Santa Maria de Palautordera › Vallès Oriental | 6 |
| Forêt de Sant Esteve de Palautordera (9) ⚠️ | Sant Esteve de Palautordera › Vallès Oriental | 6 |
| Forêt de Sant Esteve de Palautordera (14) ⚠️ | Sant Esteve de Palautordera › Vallès Oriental | 6 |
| Forêt de Sant Celoni (22) ⚠️ | Sant Celoni › Vallès Oriental | 6 |
| Forêt de la Nou de Berguedà (14) ⚠️ | la Nou de Berguedà › Berguedà | 6 |
| Forêt de Cercs (43) ⚠️ | Cercs › Berguedà | 6 |
| Forêt de Cercs (50) ⚠️ | Cercs › Berguedà | 6 |
| Forêt de Castellar del Riu (18) ⚠️ | Castellar del Riu › Berguedà | 6 |
| Forêt de la Pobla de Lillet (17) ⚠️ | la Pobla de Lillet › Berguedà | 6 |
| Forêt de Sant Quirze de Besora (4) ⚠️ | Sant Quirze de Besora › Osona (Barcelone) | 6 |
| Forêt de Talamanca (10) ⚠️ | Talamanca › Bages | 6 |
| Forêt de Talamanca (14) ⚠️ | Talamanca › Bages | 6 |
| Forêt de Talamanca (28) ⚠️ | Talamanca › Bages | 6 |
| Forêt de el Pont de Vilomara i Rocafort (28) ⚠️ | el Pont de Vilomara i Rocafort › Bages | 6 |
| Forêt de Talamanca (34) ⚠️ | Talamanca › Bages | 6 |
| Forêt de Castellar del Vallès (17) ⚠️ | Castellar del Vallès › Vallès Occidental | 6 |
| Forêt de Aguilar de Segarra (43) ⚠️ | Aguilar de Segarra › Bages | 6 |
| Forêt de Sant Pere Sallavinera (19) ⚠️ | Sant Pere Sallavinera › Anoia | 6 |
| Forêt de Sant Pere Sallavinera (23) ⚠️ | Sant Pere Sallavinera › Anoia | 6 |
| Forêt de Sant Pere Sallavinera (32) ⚠️ | Sant Pere Sallavinera › Anoia | 6 |
| Forêt de Sant Pere Sallavinera (39) ⚠️ | Sant Pere Sallavinera › Anoia | 6 |
| Forêt de Viladecavalls (10) ⚠️ | Viladecavalls › Vallès Occidental | 6 |
| Forêt de Sant Salvador de Guardiola (94) ⚠️ | Sant Salvador de Guardiola › Bages | 6 |
| Forêt de el Bruc (34) ⚠️ | el Bruc › Anoia | 6 |
| Forêt de Sant Salvador de Guardiola (120) ⚠️ | Sant Salvador de Guardiola › Bages | 6 |
| Forêt de el Bruc (43) ⚠️ | el Bruc › Anoia | 6 |
| Forêt de Olesa de Montserrat (31) ⚠️ | Olesa de Montserrat › Baix Llobregat | 6 |
| Forêt de Martorell (13) ⚠️ | Martorell › Baix Llobregat | 6 |
| Forêt de Castellgalí (34) ⚠️ | Castellgalí › Bages | 6 |
| Forêt de Sant Vicenç de Castellet (42) ⚠️ | Sant Vicenç de Castellet › Bages | 6 |
| Forêt de Navàs (62) ⚠️ | Navàs › Bages | 6 |
| Forêt de Navàs (76) ⚠️ | Navàs › Bages | 6 |
| Forêt de Viver i Serrateix (29) ⚠️ | Viver i Serrateix › Berguedà | 6 |
| Forêt de Puig-reig (68) ⚠️ | Puig-reig › Berguedà | 6 |
| Forêt de Sagàs (10) ⚠️ | Sagàs › Berguedà | 6 |
| Forêt de Casserres (20) ⚠️ | Casserres › Berguedà | 6 |
| Forêt de Casserres (21) ⚠️ | Casserres › Berguedà | 6 |
| Forêt de Montclar (33) ⚠️ | Montclar › Berguedà | 6 |
| Forêt de l'Espunyola (65) ⚠️ | l'Espunyola › Berguedà | 6 |
| Forêt de l'Espunyola (69) ⚠️ | l'Espunyola › Berguedà | 6 |
| Forêt de l'Espunyola (75) ⚠️ | l'Espunyola › Berguedà | 6 |
| Forêt de Montmajor (76) ⚠️ | Montmajor › Berguedà | 6 |
| Forêt de Sant Mateu de Bages (39) ⚠️ | Sant Mateu de Bages › Bages | 6 |
| Forêt de Navàs (122) ⚠️ | Navàs › Bages | 6 |
| Forêt de Súria (26) ⚠️ | Súria › Bages | 6 |
| Forêt de Navàs (128) ⚠️ | Navàs › Bages | 6 |
| Forêt de Viver i Serrateix (81) ⚠️ | Viver i Serrateix › Berguedà | 6 |
| Forêt de Viver i Serrateix (85) ⚠️ | Viver i Serrateix › Berguedà | 6 |
| Forêt de Montmajor (115) ⚠️ | Montmajor › Berguedà | 6 |
| Forêt de Montmajor (125) ⚠️ | Montmajor › Berguedà | 6 |
| Forêt de Santa Maria de Merlès (26) ⚠️ | Gaià › Bages | 6 |
| Forêt de Avinyó (107) ⚠️ | Avinyó › Bages | 6 |
| Forêt de Sant Cugat del Vallès (139) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 6 |
| Bois de Sant Cugat del Vallès (126) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 6 |
| Forêt de Borredà (18) ⚠️ | Borredà › Berguedà | 6 |
| Bois de Viladecavalls (10) ⚠️ | Viladecavalls › Vallès Occidental | 6 |
| Forêt de Jorba (7) ⚠️ | Jorba › Anoia | 6 |
| Forêt de Jorba (14) ⚠️ | Jorba › Anoia | 6 |
| Forêt de Jorba (31) ⚠️ | Jorba › Anoia | 6 |
| Forêt de Òdena (42) ⚠️ | Òdena › Anoia | 6 |
| Forêt de Rajadell (60) ⚠️ | Rajadell › Bages | 6 |
| Forêt de Olesa de Bonesvalls (39) ⚠️ | Olesa de Bonesvalls › Alt Penedès | 6 |
| Forêt de Olivella (53) ⚠️ | Olivella › Garraf | 6 |
| Forêt de Begues (74) ⚠️ | Begues › Baix Llobregat | 6 |
| Forêt de Olivella (112) ⚠️ | Olivella › Garraf | 6 |
| Forêt de Sant Pere de Ribes (102) ⚠️ | Sant Pere de Ribes › Garraf | 6 |
| Forêt de Canyelles (16) ⚠️ | Canyelles › Garraf | 6 |
| Forêt de Vilanova i la Geltrú (51) ⚠️ | Vilanova i la Geltrú › Garraf | 6 |
| Forêt de Vilanova i la Geltrú (66) ⚠️ | Vilanova i la Geltrú › Garraf | 6 |
| Forêt de Avinyonet del Penedès (71) ⚠️ | Avinyonet del Penedès › Alt Penedès | 6 |
| Forêt de Sant Julià de Cerdanyola (6) ⚠️ | Sant Julià de Cerdanyola › Berguedà | 6 |
| Forêt de Bagà (18) ⚠️ | Bagà › Berguedà | 6 |
| Forêt de Gisclareny (18) ⚠️ | Gisclareny › Berguedà | 6 |
| Forêt de Bagà (29) ⚠️ | Bagà › Berguedà | 6 |
| Forêt de Viver i Serrateix (114) ⚠️ | Viver i Serrateix › Berguedà | 6 |
| Forêt de Oristà (110) ⚠️ | Oristà › Lluçanès | 6 |
| Forêt de Viver i Serrateix (118) ⚠️ | Viver i Serrateix › Berguedà | 6 |
| Forêt de Santa Maria d'Oló (44) ⚠️ | Santa Maria d'Oló › Moianès | 6 |
| Forêt de Borredà (37) ⚠️ | Borredà › Berguedà | 6 |
| Forêt de Borredà (38) ⚠️ | Borredà › Berguedà | 6 |
| Forêt de Borredà (49) ⚠️ | Borredà › Berguedà | 6 |
| Forêt de Sagàs (22) ⚠️ | Sagàs › Berguedà | 6 |
| Forêt de Sagàs (29) ⚠️ | Sagàs › Berguedà | 6 |
| Forêt de Santa Maria de Merlès (100) ⚠️ | Santa Maria de Merlès › Berguedà | 6 |
| Forêt de Sagàs (34) ⚠️ | Sagàs › Berguedà | 6 |
| Bois de Sant Cebrià de Vallalta (5) ⚠️ | Sant Cebrià de Vallalta › Maresme | 6 |
| Forêt de Cardedeu (34) ⚠️ | Cardedeu › Vallès Oriental | 6 |
| Forêt de la Quar (13) ⚠️ | la Quar › Berguedà | 6 |
| Forêt de la Quar (27) ⚠️ | la Quar › Berguedà | 6 |
| Forêt de Collbató (19) ⚠️ | Collbató › Baix Llobregat | 6 |
| Forêt de Santa Maria d'Oló (55) ⚠️ | Santa Maria d'Oló › Moianès | 6 |
| Forêt de Seva (18) ⚠️ | Seva › Osona (Barcelone) | 6 |
| Forêt de Tagamanent (17) ⚠️ | Tagamanent › Vallès Oriental | 6 |
| Forêt de Sant Martí de Centelles (56) ⚠️ | Sant Martí de Centelles › Osona (Barcelone) | 6 |
| Forêt de Centelles (10) ⚠️ | Centelles › Osona (Barcelone) | 6 |
| Forêt de Centelles (11) ⚠️ | Centelles › Osona (Barcelone) | 6 |
| Forêt de Tagamanent (30) ⚠️ | Tagamanent › Vallès Oriental | 6 |
| Forêt de Tagamanent (33) ⚠️ | Tagamanent › Vallès Oriental | 6 |
| Forêt de Tagamanent (37) ⚠️ | Tagamanent › Vallès Oriental | 6 |
| Forêt de el Brull (30) ⚠️ | el Brull › Osona (Barcelone) | 6 |
| Forêt de el Brull (34) ⚠️ | el Brull › Osona (Barcelone) | 6 |
| Forêt de Montseny (15) ⚠️ | Montseny › Vallès Oriental | 6 |
| Forêt de Fogars de Montclús (23) ⚠️ | Fogars de Montclús › Vallès Oriental | 6 |
| Forêt de Sant Quirze Safaja (18) ⚠️ | Sant Quirze Safaja › Moianès | 6 |
| Forêt de Sant Quirze Safaja (19) ⚠️ | Sant Quirze Safaja › Moianès | 6 |
| Forêt de Sant Feliu de Codines (11) ⚠️ | Sant Feliu de Codines › Vallès Oriental | 6 |
| Forêt de Santa Maria d'Oló (65) ⚠️ | Santa Maria d'Oló › Moianès | 6 |
| Forêt de Oristà (121) ⚠️ | Oristà › Lluçanès | 6 |
| Forêt de Oristà (151) ⚠️ | Oristà › Lluçanès | 6 |
| Forêt de Oristà (153) ⚠️ | Oristà › Lluçanès | 6 |
| Forêt de Oristà (154) ⚠️ | Oristà › Lluçanès | 6 |
| Forêt de Sant Mateu de Bages (63) ⚠️ | Sant Mateu de Bages › Bages | 6 |
| Forêt de Sant Mateu de Bages (68) ⚠️ | Sant Mateu de Bages › Bages | 6 |
| Forêt de Calonge de Segarra (17) ⚠️ | Calonge de Segarra › Anoia | 6 |
| Forêt de les Franqueses del Vallès (53) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 6 |
| Forêt de l'Ametlla del Vallès (25) ⚠️ | l'Ametlla del Vallès › Vallès Oriental | 6 |
| Forêt de Balenyà (7) ⚠️ | Balenyà › Osona (Barcelone) | 6 |
| Forêt de Balenyà (20) ⚠️ | Balenyà › Osona (Barcelone) | 6 |
| Forêt de Saldes (61) ⚠️ | Saldes › Berguedà | 6 |
| Forêt de Saldes (67) ⚠️ | Saldes › Berguedà | 6 |
| Forêt de Olvan (34) ⚠️ | Olvan › Berguedà | 6 |
| Forêt de Bagà (57) ⚠️ | Bagà › Berguedà | 6 |
| Forêt de Guardiola de Berguedà (105) ⚠️ | Guardiola de Berguedà › Berguedà | 6 |
| Forêt de Guardiola de Berguedà (108) ⚠️ | Guardiola de Berguedà › Berguedà | 6 |
| Forêt de Guardiola de Berguedà (112) ⚠️ | Guardiola de Berguedà › Berguedà | 6 |
| Forêt de Castellar del Riu (42) ⚠️ | Castellar del Riu › Berguedà | 6 |
| Forêt de Prats de Lluçanès (18) ⚠️ | Prats de Lluçanès › Lluçanès | 6 |
| Forêt de Sant Martí d'Albars (3) ⚠️ | Sant Martí d'Albars › Lluçanès | 6 |
| Forêt de Olost (9) ⚠️ | Olost › Lluçanès | 6 |
| Forêt de Lluçà (34) ⚠️ | Lluçà › Lluçanès | 6 |
| Forêt de Borredà (61) ⚠️ | Borredà › Berguedà | 6 |
| Forêt de Lluçà (45) ⚠️ | Lluçà › Lluçanès | 6 |
| Forêt de Borredà (80) ⚠️ | Borredà › Berguedà | 6 |
| Forêt de Borredà (97) ⚠️ | Borredà › Berguedà | 6 |
| Forêt de Santa Maria de Merlès (142) ⚠️ | Santa Maria de Merlès › Berguedà | 6 |
| Forêt de Borredà (111) ⚠️ | Borredà › Berguedà | 6 |
| Forêt de la Pobla de Lillet (38) ⚠️ | la Pobla de Lillet › Berguedà | 6 |
| Forêt de la Pobla de Lillet (58) ⚠️ | la Pobla de Lillet › Berguedà | 6 |
| Forêt de Sant Jaume de Frontanyà (25) ⚠️ | Sant Jaume de Frontanyà › Berguedà | 6 |
| Forêt de Saldes (72) ⚠️ | Saldes › Berguedà | 6 |
| Forêt de Cercs (63) ⚠️ | Cercs › Berguedà | 6 |
| Forêt de Vallcebre (35) ⚠️ | Vallcebre › Berguedà | 6 |
| Forêt de Centelles (37) ⚠️ | Centelles › Osona (Barcelone) | 6 |
| Forêt de Orís (23) ⚠️ | Orís › Osona (Barcelone) | 6 |
| Forêt de Sant Jaume de Frontanyà (27) ⚠️ | Sant Jaume de Frontanyà › Berguedà | 6 |
| Forêt de Tordera (85) ⚠️ | Tordera › Maresme | 6 |
| Bois de Vilanova del Vallès (14) ⚠️ | Vilanova del Vallès › Vallès Oriental | 6 |
| Forêt de Montcada i Reixac (31) ⚠️ | Montcada i Reixac › Vallès Occidental | 6 |
| Forêt de Badalona (29) ⚠️ | Badalona › Barcelonès | 6 |
| Bois de Cubelles (2) ⚠️ | Cubelles › Garraf | 6 |
| Forêt de Guardiola de Berguedà (127) ⚠️ | Guardiola de Berguedà › Berguedà | 6 |
| Forêt de Guardiola de Berguedà (137) ⚠️ | Guardiola de Berguedà › Berguedà | 6 |
| Forêt de Castellolí (37) ⚠️ | Castellolí › Anoia | 6 |
| Forêt de Sant Martí de Tous (13) ⚠️ | Sant Martí de Tous › Anoia | 6 |
| Forêt de Santa Margarida de Montbui (23) ⚠️ | Santa Margarida de Montbui › Anoia | 6 |
| Forêt de Moià (60) ⚠️ | Moià › Moianès | 6 |
| Forêt de Sant Feliu Sasserra (23) ⚠️ | Sant Feliu Sasserra › Bages | 6 |
| Forêt de Sant Feliu Sasserra (27) ⚠️ | Sant Feliu Sasserra › Bages | 6 |
| Forêt de Castellar de n'Hug (38) ⚠️ | Castellar de n'Hug › Berguedà | 6 |
| Forêt de Castellar de n'Hug (48) ⚠️ | Castellar de n'Hug › Berguedà | 6 |
| Forêt de Oristà (168) ⚠️ | Oristà › Lluçanès | 6 |
| Forêt de Vallirana (37) ⚠️ | Vallirana › Baix Llobregat | 6 |
| Forêt de Cardona (108) ⚠️ | Cardona › Bages | 6 |
| Forêt de Terrassa (82) ⚠️ | Terrassa › Vallès Occidental | 6 |
| Forêt de Mediona (14) ⚠️ | Mediona › Alt Penedès | 6 |
| Forêt de Sant Quintí de Mediona (2) ⚠️ | Sant Quintí de Mediona › Alt Penedès | 6 |
| Forêt de Mediona (70) ⚠️ | Mediona › Alt Penedès | 6 |
| Forêt de Sant Pere de Riudebitlles (6) ⚠️ | Sant Pere de Riudebitlles › Alt Penedès | 6 |
| Forêt de Torrelles de Foix (10) ⚠️ | Torrelles de Foix › Alt Penedès | 6 |
| Forêt de Viver i Serrateix (122) ⚠️ | Viver i Serrateix › Berguedà | 6 |
| Forêt de Tavertet (73) ⚠️ | Tavertet › Osona (Barcelone) | 6 |
| Forêt de Tavertet (82) ⚠️ | Tavertet › Osona (Barcelone) | 6 |
| Forêt de Alpens (19) ⚠️ | Alpens › Lluçanès | 6 |
| Forêt de la Quar (48) ⚠️ | la Quar › Berguedà | 6 |
| Forêt de Casserres (31) ⚠️ | Casserres › Berguedà | 6 |
| Forêt de Santa Susanna (13) ⚠️ | Santa Susanna › Maresme | 6 |
| Forêt de Malgrat de Mar (6) ⚠️ | Malgrat de Mar › Maresme | 6 |
| Forêt de Sant Andreu de Llavaneres (4) ⚠️ | Sant Andreu de Llavaneres › Maresme | 6 |
| Forêt de Arenys de Munt (13) ⚠️ | Arenys de Munt › Maresme | 6 |
| Forêt de Sant Celoni (44) ⚠️ | Sant Celoni › Vallès Oriental | 6 |
| Forêt de Sant Celoni (45) ⚠️ | Sant Celoni › Vallès Oriental | 6 |
| Forêt de Fogars de la Selva (34) ⚠️ | Fogars de la Selva › la Selva (Barcelone) | 6 |
| Forêt de Fogars de la Selva (38) ⚠️ | Fogars de la Selva › la Selva (Barcelone) | 6 |
| Forêt de Fogars de la Selva (44) ⚠️ | Fogars de la Selva › la Selva (Barcelone) | 6 |
| Forêt de Fogars de la Selva (46) ⚠️ | Fogars de la Selva › la Selva (Barcelone) | 6 |
| Forêt de Sant Celoni (58) ⚠️ | Sant Celoni › Vallès Oriental | 6 |
| Forêt de Sallent (102) ⚠️ | Sallent › Bages | 6 |
| Forêt de Sallent (110) ⚠️ | Sallent › Bages | 6 |
| Forêt de Santpedor (24) ⚠️ | Santpedor › Bages | 6 |
| Forêt de Castellnou de Bages (57) ⚠️ | Castellnou de Bages › Bages | 6 |
| Forêt de Castellnou de Bages (71) ⚠️ | Castellnou de Bages › Bages | 6 |
| Forêt de Sant Joan de Vilatorrada (74) ⚠️ | Sant Joan de Vilatorrada › Bages | 6 |
| Forêt de Rupit i Pruit (40) ⚠️ | Rupit i Pruit › Osona (Barcelone) | 6 |
| Forêt de Vallcebre (62) ⚠️ | Vallcebre › Berguedà | 6 |
| Forêt de Vallcebre (71) ⚠️ | Vallcebre › Berguedà | 6 |
| Forêt de Sant Julià de Vilatorta (4) ⚠️ | Sant Julià de Vilatorta › Osona (Barcelone) | 6 |
| Forêt de Vilanova de Sau (66) ⚠️ | Vilanova de Sau › Osona (Barcelone) | 6 |
| Forêt de Taradell (31) ⚠️ | Taradell › Osona (Barcelone) | 6 |
| Forêt de Taradell (39) ⚠️ | Taradell › Osona (Barcelone) | 6 |
| Forêt de Mediona (96) ⚠️ | Mediona › Alt Penedès | 6 |
| Forêt de Sentmenat (17) ⚠️ | Sentmenat › Vallès Occidental | 6 |
| Forêt de Oristà (174) ⚠️ | Olost › Lluçanès | 6 |
| Forêt de Moià (68) ⚠️ | Moià › Moianès | 6 |
| Forêt de Moià (70) ⚠️ | Moià › Moianès | 6 |
| Forêt de Sant Fruitós de Bages (46) ⚠️ | Sant Fruitós de Bages › Bages | 6 |
| Forêt de Pujalt (12) ⚠️ | Pujalt › Anoia | 6 |
| Forêt de Olost (19) ⚠️ | Olost › Lluçanès | 6 |
| Forêt de Gavà (2) ⚠️ | Gavà › Baix Llobregat | 5 |
| Parc de Barcelona ⚠️ | Barcelona › Barcelonès | 5 |
| Parc de Can Mercader ⚠️ | Cornellà de Llobregat › Baix Llobregat | 5 |
| Parc de la Creueta del Coll ⚠️ | Barcelona › Barcelonès | 5 |
| Parc de Can Zam ⚠️ | Santa Coloma de Gramenet › Barcelonès | 5 |
| Bois de Lliçà d'Amunt (6) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 5 |
| Bois de Lliçà d'Amunt (20) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 5 |
| Bosc d'en Fonolleda ⚠️ | Lliçà de Vall › Vallès Oriental | 5 |
| Forêt de Viladecans ⚠️ | Viladecans › Baix Llobregat | 5 |
| Forêt de Calonge de Segarra (2) ⚠️ | Calonge de Segarra › Anoia | 5 |
| Forêt de Vilanova de Sau (15) ⚠️ | Vilanova de Sau › Osona (Barcelone) | 5 |
| Forêt de Sant Agustí de Lluçanès (4) ⚠️ | Sant Agustí de Lluçanès › Osona (Barcelone) | 5 |
| Forêt de Tordera (16) ⚠️ | Tordera › Maresme | 5 |
| Parc i Roserar de Cervantes ⚠️ | Barcelona › Barcelonès | 5 |
| Parc del Turonet (2) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 5 |
| Bois de Mataró (2) ⚠️ | Mataró › Maresme | 5 |
| Bois de Mataró (4) ⚠️ | Mataró › Maresme | 5 |
| Bosc de Can Veire ⚠️ | Mollet del Vallès › Vallès Oriental | 5 |
| Forêt de Gavà (10) ⚠️ | Gavà › Baix Llobregat | 5 |
| Forêt de Gavà (21) ⚠️ | Gavà › Baix Llobregat | 5 |
| Forêt de Avinyonet del Penedès (40) ⚠️ | Avinyonet del Penedès › Alt Penedès | 5 |
| Forêt de Olivella (4) ⚠️ | Olivella › Garraf | 5 |
| Forêt de Olivella (9) ⚠️ | Olivella › Garraf | 5 |
| Forêt de Olivella (35) ⚠️ | Olivella › Garraf | 5 |
| Forêt de Sant Sadurní d'Anoia (3) ⚠️ | Sant Sadurní d'Anoia › Alt Penedès | 5 |
| Forêt de Olesa de Bonesvalls (27) ⚠️ | Olesa de Bonesvalls › Alt Penedès | 5 |
| Forêt de Olèrdola (39) ⚠️ | Olèrdola › Alt Penedès | 5 |
| Forêt de Santa Margarida i els Monjos (7) ⚠️ | Santa Margarida i els Monjos › Alt Penedès | 5 |
| Forêt de Subirats (65) ⚠️ | Subirats › Alt Penedès | 5 |
| Forêt de Subirats (77) ⚠️ | Subirats › Alt Penedès | 5 |
| Forêt de Sant Esteve Sesrovires (2) ⚠️ | Sant Esteve Sesrovires › Baix Llobregat | 5 |
| Forêt de Santa Fe del Penedès ⚠️ | Santa Fe del Penedès › Alt Penedès | 5 |
| Forêt de Vallirana (20) ⚠️ | Vallirana › Baix Llobregat | 5 |
| Forêt de Caldes de Montbui (6) ⚠️ | Caldes de Montbui › Vallès Oriental | 5 |
| Parc de les Bateries ⚠️ | Montgat › Maresme | 5 |
| Parc de la Llacuna ⚠️ | Montcada i Reixac › Vallès Occidental | 5 |
| Bois de Cabrils (5) ⚠️ | Cabrils › Maresme | 5 |
| Bois de Òrrius (11) ⚠️ | Òrrius › Maresme | 5 |
| Bois de Premià de Dalt ⚠️ | Premià de Dalt › Maresme | 5 |
| Forêt de Manlleu (2) ⚠️ | Manlleu › Osona (Barcelone) | 5 |
| Bois de Vallromanes (8) ⚠️ | Vallromanes › Vallès Oriental | 5 |
| Bois de Vallromanes (11) ⚠️ | Vallromanes › Vallès Oriental | 5 |
| Forêt de Molins de Rei (2) ⚠️ | Molins de Rei › Baix Llobregat | 5 |
| Forêt de Veciana (9) ⚠️ | Veciana › Anoia | 5 |
| Forêt de Puig-reig ⚠️ | Puig-reig › Berguedà | 5 |
| Forêt de Casserres (2) ⚠️ | Casserres › Berguedà | 5 |
| Forêt de Caldes d'Estrac ⚠️ | Caldes d'Estrac › Maresme | 5 |
| Forêt de Vallirana (21) ⚠️ | Vallirana › Baix Llobregat | 5 |
| Bois de Argentona (40) ⚠️ | Argentona › Maresme | 5 |
| Forêt de les Franqueses del Vallès (2) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 5 |
| Forêt de l'Ametlla del Vallès (5) ⚠️ | l'Ametlla del Vallès › Vallès Oriental | 5 |
| Bois de Tiana ⚠️ | Tiana › Maresme | 5 |
| Forêt de Vacarisses ⚠️ | Vacarisses › Vallès Occidental | 5 |
| Forêt de Vacarisses (3) ⚠️ | Vacarisses › Vallès Occidental | 5 |
| Parc de Esplugues de Llobregat (3) ⚠️ | Esplugues de Llobregat › Baix Llobregat | 5 |
| Forêt de Malla (2) ⚠️ | Malla › Osona (Barcelone) | 5 |
| Forêt de Castellbisbal ⚠️ | Castellbisbal › Vallès Occidental | 5 |
| Forêt de Sant Salvador de Guardiola (12) ⚠️ | Sant Salvador de Guardiola › Bages | 5 |
| Bois de les Franqueses del Vallès (4) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 5 |
| Forêt de Sant Esteve Sesrovires (13) ⚠️ | Sant Esteve Sesrovires › Baix Llobregat | 5 |
| Forêt de Sant Llorenç Savall (8) ⚠️ | Sant Llorenç Savall › Vallès Occidental | 5 |
| Forêt de Cànoves i Samalús ⚠️ | Cànoves i Samalús › Vallès Oriental | 5 |
| Forêt de Talamanca (2) ⚠️ | Talamanca › Bages | 5 |
| Bois de Santa Coloma de Cervelló (57) ⚠️ | Santa Coloma de Cervelló › Baix Llobregat | 5 |
| Forêt de Montmaneu (6) ⚠️ | Montmaneu › Anoia | 5 |
| Forêt de Oristà (78) ⚠️ | Oristà › Lluçanès | 5 |
| Forêt de Guardiola de Berguedà (5) ⚠️ | Guardiola de Berguedà › Berguedà | 5 |
| Forêt de Gisclareny ⚠️ | Gisclareny › Berguedà | 5 |
| Bois de Torrelavit (17) ⚠️ | Torrelavit › Alt Penedès | 5 |
| Bosc de la Mata ⚠️ | Torrelles de Foix › Alt Penedès | 5 |
| les Planes ⚠️ | Torrelles de Foix › Alt Penedès | 5 |
| Bois de Òdena ⚠️ | Òdena › Anoia | 5 |
| Forêt de Torrelavit (22) ⚠️ | Torrelavit › Alt Penedès | 5 |
| Forêt de Subirats (88) ⚠️ | Subirats › Alt Penedès | 5 |
| Parc del Castell de l'Oreneta ⚠️ | Barcelona › Barcelonès | 5 |
| Parc dels Pinetons (4) ⚠️ | Ripollet › Vallès Occidental | 5 |
| Forêt de Cardona (37) ⚠️ | Cardona › Bages | 5 |
| Forêt de l'Espunyola (8) ⚠️ | l'Espunyola › Berguedà | 5 |
| Forêt de Castellterçol (14) ⚠️ | Castellterçol › Moianès | 5 |
| Forêt de Rajadell (15) ⚠️ | Rajadell › Bages | 5 |
| Forêt de Rajadell (17) ⚠️ | Rajadell › Bages | 5 |
| Forêt de Rajadell (20) ⚠️ | Rajadell › Bages | 5 |
| Forêt de Artés (11) ⚠️ | Artés › Bages | 5 |
| Bosc de Sant Martí ⚠️ | Sant Fruitós de Bages › Bages | 5 |
| Forêt de Manresa (23) ⚠️ | Manresa › Bages | 5 |
| Forêt de Calders (22) ⚠️ | Calders › Moianès | 5 |
| Forêt de Manresa (60) ⚠️ | Manresa › Bages | 5 |
| Parc de les Aigües (4) ⚠️ | Cornellà de Llobregat › Baix Llobregat | 5 |
| Forêt de Gironella (5) ⚠️ | Gironella › Berguedà | 5 |
| Bosc de la Torre del Moro ⚠️ | Sant Joan de Vilatorrada › Bages | 5 |
| Forêt de Cardona (42) ⚠️ | Cardona › Bages | 5 |
| Forêt de Cardona (50) ⚠️ | Cardona › Bages | 5 |
| Forêt de Cardona (53) ⚠️ | Cardona › Bages | 5 |
| Forêt de Torelló (2) ⚠️ | Torelló › Osona (Barcelone) | 5 |
| Forêt de Orís (5) ⚠️ | Orís › Osona (Barcelone) | 5 |
| Forêt de Malla (3) ⚠️ | Malla › Osona (Barcelone) | 5 |
| Forêt de Sant Pere de Torelló (17) ⚠️ | Sant Pere de Torelló › Osona (Barcelone) | 5 |
| Forêt de Castellar de n'Hug (8) ⚠️ | Castellar de n'Hug › Berguedà | 5 |
| Forêt de Castellterçol (56) ⚠️ | Castellterçol › Moianès | 5 |
| Nou Parc Central ⚠️ | Mataró › Maresme | 5 |
| Forêt de Castellterçol (77) ⚠️ | Castellterçol › Moianès | 5 |
| Forêt de Berga (20) ⚠️ | Berga › Berguedà | 5 |
| Forêt de Berga (35) ⚠️ | Berga › Berguedà | 5 |
| Forêt de Cercs (13) ⚠️ | Cercs › Berguedà | 5 |
| Forêt de Berga (44) ⚠️ | Berga › Berguedà | 5 |
| Forêt de Cercs (18) ⚠️ | Berga › Berguedà | 5 |
| Forêt de l'Espunyola (14) ⚠️ | l'Espunyola › Berguedà | 5 |
| Forêt de Montmajor (38) ⚠️ | Montmajor › Berguedà | 5 |
| Forêt de Manresa (119) ⚠️ | Manresa › Bages | 5 |
| Forêt de Sant Sadurní d'Anoia (24) ⚠️ | Sant Sadurní d'Anoia › Alt Penedès | 5 |
| Forêt de Esparreguera (11) ⚠️ | Esparreguera › Baix Llobregat | 5 |
| Forêt de Sant Esteve Sesrovires (18) ⚠️ | Sant Esteve Sesrovires › Baix Llobregat | 5 |
| Forêt de Montmajor (62) ⚠️ | Montmajor › Berguedà | 5 |
| Forêt de Gaià (16) ⚠️ | Gaià › Bages | 5 |
| Forêt de Avinyó (27) ⚠️ | Avinyó › Bages | 5 |
| Forêt de Santa Maria d'Oló (16) ⚠️ | Santa Maria d'Oló › Moianès | 5 |
| Forêt de Sallent (61) ⚠️ | Sallent › Bages | 5 |
| Forêt de Avinyó (53) ⚠️ | Avinyó › Bages | 5 |
| Forêt de Sallent (62) ⚠️ | Avinyó › Bages | 5 |
| Forêt de Sallent (64) ⚠️ | Sallent › Bages | 5 |
| Forêt de Sallent (70) ⚠️ | Sallent › Bages | 5 |
| Forêt de Oristà (91) ⚠️ | Oristà › Lluçanès | 5 |
| Forêt de Sant Salvador de Guardiola (30) ⚠️ | Sant Salvador de Guardiola › Bages | 5 |
| Forêt de Puig-reig (11) ⚠️ | Puig-reig › Berguedà | 5 |
| Forêt de Puig-reig (13) ⚠️ | Puig-reig › Berguedà | 5 |
| Forêt de Santa Maria d'Oló (25) ⚠️ | Santa Maria d'Oló › Moianès | 5 |
| Forêt de Puig-reig (36) ⚠️ | Puig-reig › Berguedà | 5 |
| Forêt de Sant Salvador de Guardiola (39) ⚠️ | Sant Salvador de Guardiola › Bages | 5 |
| Forêt de Balsareny (77) ⚠️ | Balsareny › Bages | 5 |
| Forêt de Castellnou de Bages (46) ⚠️ | Castellnou de Bages › Bages | 5 |
| Forêt de el Papiol (5) ⚠️ | el Papiol › Baix Llobregat | 5 |
| Forêt de Vic (20) ⚠️ | Vic › Osona (Barcelone) | 5 |
| Forêt de Corbera de Llobregat (28) ⚠️ | Corbera de Llobregat › Baix Llobregat | 5 |
| Forêt de Vallirana (33) ⚠️ | Vallirana › Baix Llobregat | 5 |
| Forêt de Rubí (65) ⚠️ | Rubí › Vallès Occidental | 5 |
| Bois de Rubí (13) ⚠️ | Rubí › Vallès Occidental | 5 |
| Forêt de Monistrol de Montserrat (25) ⚠️ | Monistrol de Montserrat › Bages | 5 |
| Forêt de Vacarisses (13) ⚠️ | Vacarisses › Vallès Occidental | 5 |
| Forêt de Vacarisses (17) ⚠️ | Vacarisses › Vallès Occidental | 5 |
| Forêt de Vacarisses (22) ⚠️ | Vacarisses › Vallès Occidental | 5 |
| Forêt de Vacarisses (33) ⚠️ | Vacarisses › Vallès Occidental | 5 |
| Forêt de Esparreguera (14) ⚠️ | Esparreguera › Baix Llobregat | 5 |
| Forêt de Vacarisses (51) ⚠️ | Vacarisses › Vallès Occidental | 5 |
| Forêt de Castellbell i el Vilar (15) ⚠️ | Castellbell i el Vilar › Bages | 5 |
| Forêt de Sant Vicenç de Castellet (16) ⚠️ | Sant Vicenç de Castellet › Bages | 5 |
| Forêt de Esparreguera (21) ⚠️ | Esparreguera › Baix Llobregat | 5 |
| Forêt de Marganell (10) ⚠️ | Marganell › Bages | 5 |
| Forêt de el Bruc (20) ⚠️ | el Bruc › Anoia | 5 |
| Forêt de Marganell (14) ⚠️ | Marganell › Bages | 5 |
| Forêt de Castellolí (12) ⚠️ | Castellolí › Anoia | 5 |
| Forêt de Òdena (32) ⚠️ | Òdena › Anoia | 5 |
| Forêt de Òdena (35) ⚠️ | Òdena › Anoia | 5 |
| Forêt de el Pont de Vilomara i Rocafort (8) ⚠️ | el Pont de Vilomara i Rocafort › Bages | 5 |
| Forêt de Sitges (42) ⚠️ | Sitges › Garraf | 5 |
| Forêt de Sitges (44) ⚠️ | Sitges › Garraf | 5 |
| Forêt de Sitges (59) ⚠️ | Sitges › Garraf | 5 |
| Forêt de Gavà (63) ⚠️ | Gavà › Baix Llobregat | 5 |
| Forêt de Gavà (69) ⚠️ | Gavà › Baix Llobregat | 5 |
| Forêt de Castellgalí (12) ⚠️ | Sant Salvador de Guardiola › Bages | 5 |
| Forêt de Castellgalí (13) ⚠️ | Castellgalí › Bages | 5 |
| Forêt de Castellgalí (16) ⚠️ | Castellgalí › Bages | 5 |
| Forêt de Avinyó (65) ⚠️ | Avinyó › Bages | 5 |
| Forêt de Avinyó (71) ⚠️ | Artés › Bages | 5 |
| Forêt de Vic (25) ⚠️ | Vic › Osona (Barcelone) | 5 |
| Forêt de Cardedeu (25) ⚠️ | Cardedeu › Vallès Oriental | 5 |
| Forêt de Súria (14) ⚠️ | Sant Mateu de Bages › Bages | 5 |
| Forêt de Súria (15) ⚠️ | Súria › Bages | 5 |
| Forêt de Sant Pere de Ribes (87) ⚠️ | Sant Pere de Ribes › Garraf | 5 |
| Forêt de Navàs (37) ⚠️ | Navàs › Bages | 5 |
| Forêt de Santa Maria de Palautordera (21) ⚠️ | Santa Maria de Palautordera › Vallès Oriental | 5 |
| Forêt de Cercs (30) ⚠️ | Cercs › Berguedà | 5 |
| Forêt de Cercs (36) ⚠️ | Cercs › Berguedà | 5 |
| Forêt de Cercs (44) ⚠️ | Cercs › Berguedà | 5 |
| Forêt de Santa Maria de Besora (9) ⚠️ | Santa Maria de Besora › Osona (Barcelone) | 5 |
| Forêt de Guardiola de Berguedà (40) ⚠️ | Guardiola de Berguedà › Berguedà | 5 |
| Forêt de Monistrol de Calders (9) ⚠️ | Monistrol de Calders › Moianès | 5 |
| Forêt de el Pont de Vilomara i Rocafort (22) ⚠️ | el Pont de Vilomara i Rocafort › Bages | 5 |
| Forêt de Talamanca (21) ⚠️ | Talamanca › Bages | 5 |
| Forêt de Mura (33) ⚠️ | Mura › Bages | 5 |
| Forêt de Navarcles (15) ⚠️ | Navarcles › Bages | 5 |
| Forêt de Calders (57) ⚠️ | Calders › Moianès | 5 |
| Forêt de Sant Vicenç de Castellet (24) ⚠️ | Sant Vicenç de Castellet › Bages | 5 |
| Forêt de Calders (64) ⚠️ | Calders › Moianès | 5 |
| Forêt de Rajadell (39) ⚠️ | Rajadell › Bages | 5 |
| Forêt de Sant Pere Sallavinera (22) ⚠️ | Sant Pere Sallavinera › Anoia | 5 |
| Forêt de Sant Pere Sallavinera (31) ⚠️ | Sant Pere Sallavinera › Anoia | 5 |
| Forêt de Sant Pere Sallavinera (42) ⚠️ | Sant Pere Sallavinera › Anoia | 5 |
| Forêt de Sant Pere Sallavinera (43) ⚠️ | Sant Pere Sallavinera › Anoia | 5 |
| Forêt de Terrassa (76) ⚠️ | Terrassa › Vallès Occidental | 5 |
| Forêt de Rajadell (52) ⚠️ | Rajadell › Bages | 5 |
| Forêt de Sant Salvador de Guardiola (81) ⚠️ | Sant Salvador de Guardiola › Bages | 5 |
| Forêt de Sant Salvador de Guardiola (83) ⚠️ | Sant Salvador de Guardiola › Bages | 5 |
| Forêt de Sant Salvador de Guardiola (92) ⚠️ | Sant Salvador de Guardiola › Bages | 5 |
| Forêt de Vacarisses (65) ⚠️ | Vacarisses › Vallès Occidental | 5 |
| Forêt de Olesa de Montserrat (18) ⚠️ | Olesa de Montserrat › Baix Llobregat | 5 |
| Forêt de Olesa de Montserrat (30) ⚠️ | Olesa de Montserrat › Baix Llobregat | 5 |
| Forêt de Olesa de Montserrat (40) ⚠️ | Olesa de Montserrat › Baix Llobregat | 5 |
| Forêt de Abrera (12) ⚠️ | Abrera › Baix Llobregat | 5 |
| Forêt de Abrera (20) ⚠️ | Martorell › Baix Llobregat | 5 |
| Forêt de Castellbisbal (23) ⚠️ | Castellbisbal › Vallès Occidental | 5 |
| Forêt de Castellví de Rosanes (8) ⚠️ | Castellví de Rosanes › Baix Llobregat | 5 |
| Forêt de Sant Vicenç de Castellet (40) ⚠️ | Sant Vicenç de Castellet › Bages | 5 |
| Forêt de Navàs (82) ⚠️ | Navàs › Bages | 5 |
| Forêt de Puig-reig (57) ⚠️ | Puig-reig › Berguedà | 5 |
| Forêt de Puig-reig (59) ⚠️ | Puig-reig › Berguedà | 5 |
| Forêt de Viver i Serrateix (46) ⚠️ | Viver i Serrateix › Berguedà | 5 |
| Forêt de Viver i Serrateix (49) ⚠️ | Viver i Serrateix › Berguedà | 5 |
| Forêt de Santa Maria de Merlès (20) ⚠️ | Santa Maria de Merlès › Berguedà | 5 |
| Forêt de Sagàs (13) ⚠️ | Sagàs › Berguedà | 5 |
| Forêt de Sagàs (19) ⚠️ | Sagàs › Berguedà | 5 |
| Forêt de l'Espunyola (58) ⚠️ | l'Espunyola › Berguedà | 5 |
| Forêt de l'Espunyola (71) ⚠️ | l'Espunyola › Berguedà | 5 |
| Forêt de l'Espunyola (73) ⚠️ | l'Espunyola › Berguedà | 5 |
| Forêt de Avià (41) ⚠️ | Avià › Berguedà | 5 |
| Forêt de Capolat (23) ⚠️ | Capolat › Berguedà | 5 |
| Forêt de Capolat (29) ⚠️ | Capolat › Berguedà | 5 |
| Forêt de Montmajor (96) ⚠️ | Montmajor › Berguedà | 5 |
| Forêt de Navàs (99) ⚠️ | Navàs › Bages | 5 |
| Forêt de Navàs (105) ⚠️ | Navàs › Bages | 5 |
| Forêt de Navàs (113) ⚠️ | Navàs › Bages | 5 |
| Forêt de Navàs (125) ⚠️ | Navàs › Bages | 5 |
| Forêt de Viver i Serrateix (76) ⚠️ | Viver i Serrateix › Berguedà | 5 |
| Forêt de Montmajor (116) ⚠️ | Montmajor › Berguedà | 5 |
| Forêt de Viver i Serrateix (93) ⚠️ | Viver i Serrateix › Berguedà | 5 |
| Forêt de Montmajor (130) ⚠️ | Montmajor › Berguedà | 5 |
| Forêt de Gaià (65) ⚠️ | Gaià › Bages | 5 |
| Forêt de Vic (31) ⚠️ | Vic › Osona (Barcelone) | 5 |
| Forêt de Barcelona (53) ⚠️ | Barcelona › Barcelonès | 5 |
| Forêt de la Quar (11) ⚠️ | la Quar › Berguedà | 5 |
| Forêt de Saldes (23) ⚠️ | Saldes › Berguedà | 5 |
| Forêt de Borredà (16) ⚠️ | Borredà › Berguedà | 5 |
| Forêt de Borredà (29) ⚠️ | Borredà › Berguedà | 5 |
| Forêt de Jorba (15) ⚠️ | Jorba › Anoia | 5 |
| Forêt de Òdena (47) ⚠️ | Òdena › Anoia | 5 |
| Forêt de Òdena (48) ⚠️ | Òdena › Anoia | 5 |
| Forêt de Castellet i la Gornal (75) ⚠️ | Castellet i la Gornal › Alt Penedès | 5 |
| Forêt de Olivella (57) ⚠️ | Olivella › Garraf | 5 |
| Forêt de Begues (52) ⚠️ | Begues › Baix Llobregat | 5 |
| Forêt de Olivella (113) ⚠️ | Olivella › Garraf | 5 |
| Forêt de Sant Pere de Ribes (101) ⚠️ | Sant Pere de Ribes › Garraf | 5 |
| Forêt de Sitges (86) ⚠️ | Sitges › Garraf | 5 |
| Forêt de Vilanova i la Geltrú (31) ⚠️ | Vilanova i la Geltrú › Garraf | 5 |
| Forêt de Santa Margarida i els Monjos (33) ⚠️ | Santa Margarida i els Monjos › Alt Penedès | 5 |
| Forêt de Castellet i la Gornal (89) ⚠️ | Castellet i la Gornal › Alt Penedès | 5 |
| Forêt de Castellet i la Gornal (92) ⚠️ | Castellet i la Gornal › Alt Penedès | 5 |
| Forêt de Canyelles (13) ⚠️ | Vilanova i la Geltrú › Garraf | 5 |
| Forêt de Sant Pere de Ribes (110) ⚠️ | Sant Pere de Ribes › Garraf | 5 |
| Forêt de Vilanova i la Geltrú (56) ⚠️ | Vilanova i la Geltrú › Garraf | 5 |
| Forêt de Vilanova i la Geltrú (62) ⚠️ | Vilanova i la Geltrú › Garraf | 5 |
| Forêt de Sant Julià de Cerdanyola (11) ⚠️ | Sant Julià de Cerdanyola › Berguedà | 5 |
| Forêt de Viladecavalls (12) ⚠️ | Viladecavalls › Vallès Occidental | 5 |
| Forêt de Guardiola de Berguedà (60) ⚠️ | Guardiola de Berguedà › Berguedà | 5 |
| Forêt de Bagà (25) ⚠️ | Bagà › Berguedà | 5 |
| Forêt de Gisclareny (21) ⚠️ | Gisclareny › Berguedà | 5 |
| Forêt de Viver i Serrateix (109) ⚠️ | Viver i Serrateix › Berguedà | 5 |
| Forêt de Santa Maria de Merlès (76) ⚠️ | Santa Maria de Merlès › Berguedà | 5 |
| Forêt de Viver i Serrateix (116) ⚠️ | Viver i Serrateix › Berguedà | 5 |
| Forêt de Vilada (18) ⚠️ | Vilada › Berguedà | 5 |
| Forêt de Borredà (39) ⚠️ | Borredà › Berguedà | 5 |
| Forêt de Santa Maria de Merlès (86) ⚠️ | Santa Maria de Merlès › Berguedà | 5 |
| Forêt de Santa Maria de Merlès (88) ⚠️ | Santa Maria de Merlès › Berguedà | 5 |
| Forêt de Santa Maria de Merlès (112) ⚠️ | Santa Maria de Merlès › Berguedà | 5 |
| Forêt de Santa Maria de Merlès (116) ⚠️ | Santa Maria de Merlès › Berguedà | 5 |
| Forêt de Santa Maria de Merlès (118) ⚠️ | Santa Maria de Merlès › Berguedà | 5 |
| Forêt de Aguilar de Segarra (48) ⚠️ | Aguilar de Segarra › Bages | 5 |
| Bois de Sant Cebrià de Vallalta (2) ⚠️ | Sant Cebrià de Vallalta › Maresme | 5 |
| Forêt de Rupit i Pruit (23) ⚠️ | Rupit i Pruit › Osona (Barcelone) | 5 |
| Forêt de la Quar (20) ⚠️ | la Quar › Berguedà | 5 |
| Forêt de Sant Pol de Mar (17) ⚠️ | Sant Pol de Mar › Maresme | 5 |
| Forêt de Sant Pere Sallavinera (65) ⚠️ | Sant Pere Sallavinera › Anoia | 5 |
| Forêt de els Hostalets de Pierola (23) ⚠️ | els Hostalets de Pierola › Anoia | 5 |
| Forêt de Monistrol de Calders (39) ⚠️ | Monistrol de Calders › Moianès | 5 |
| Forêt de Taradell (7) ⚠️ | Tona › Osona (Barcelone) | 5 |
| Forêt de Centelles (9) ⚠️ | Centelles › Osona (Barcelone) | 5 |
| Forêt de Montseny (8) ⚠️ | Montseny › Vallès Oriental | 5 |
| Forêt de Bigues i Riells del Fai (22) ⚠️ | Bigues i Riells del Fai › Vallès Oriental | 5 |
| Forêt de Sant Feliu de Codines (12) ⚠️ | Sant Feliu de Codines › Vallès Oriental | 5 |
| Forêt de Santa Maria d'Oló (68) ⚠️ | Santa Maria d'Oló › Moianès | 5 |
| Forêt de Oristà (130) ⚠️ | Oristà › Lluçanès | 5 |
| Forêt de Oristà (152) ⚠️ | Oristà › Lluçanès | 5 |
| Forêt de Sant Mateu de Bages (62) ⚠️ | Sant Mateu de Bages › Bages | 5 |
| Forêt de Sant Mateu de Bages (66) ⚠️ | Sant Mateu de Bages › Bages | 5 |
| Forêt de Sant Mateu de Bages (71) ⚠️ | Sant Mateu de Bages › Bages | 5 |
| Forêt de Sant Mateu de Bages (94) ⚠️ | Sant Mateu de Bages › Bages | 5 |
| Forêt de les Franqueses del Vallès (56) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 5 |
| Forêt de Tona (10) ⚠️ | Tona › Osona (Barcelone) | 5 |
| Forêt de Tona (12) ⚠️ | Balenyà › Osona (Barcelone) | 5 |
| Forêt de Tona (17) ⚠️ | Tona › Osona (Barcelone) | 5 |
| Forêt de Malla (5) ⚠️ | Muntanyola › Osona (Barcelone) | 5 |
| Forêt de Malla (7) ⚠️ | Taradell › Osona (Barcelone) | 5 |
| Forêt de Malla (12) ⚠️ | Malla › Osona (Barcelone) | 5 |
| Forêt de Saldes (47) ⚠️ | Saldes › Berguedà | 5 |
| Forêt de Saldes (70) ⚠️ | Saldes › Berguedà | 5 |
| Forêt de Sagàs (44) ⚠️ | Sagàs › Berguedà | 5 |
| Forêt de Sagàs (45) ⚠️ | Sagàs › Berguedà | 5 |
| Forêt de Bagà (36) ⚠️ | Bagà › Berguedà | 5 |
| Forêt de Bagà (41) ⚠️ | Bagà › Berguedà | 5 |
| Forêt de Bagà (51) ⚠️ | Bagà › Berguedà | 5 |
| Forêt de Gisclareny (42) ⚠️ | Gisclareny › Berguedà | 5 |
| Forêt de Fígols (15) ⚠️ | Fígols › Berguedà | 5 |
| Forêt de Castellar del Riu (29) ⚠️ | Castellar del Riu › Berguedà | 5 |
| Forêt de Capolat (40) ⚠️ | Capolat › Berguedà | 5 |
| Forêt de Fígols (16) ⚠️ | Fígols › Berguedà | 5 |
| Forêt de Fígols (26) ⚠️ | Fígols › Berguedà | 5 |
| Forêt de Prats de Lluçanès (17) ⚠️ | Prats de Lluçanès › Lluçanès | 5 |
| Forêt de Prats de Lluçanès (19) ⚠️ | Prats de Lluçanès › Lluçanès | 5 |
| Forêt de Olost (5) ⚠️ | Olost › Lluçanès | 5 |
| Forêt de Olost (7) ⚠️ | Olost › Lluçanès | 5 |
| Forêt de Lluçà (33) ⚠️ | Lluçà › Lluçanès | 5 |
| Forêt de Lluçà (44) ⚠️ | Lluçà › Lluçanès | 5 |
| Forêt de Lluçà (53) ⚠️ | Lluçà › Lluçanès | 5 |
| Forêt de les Franqueses del Vallès (68) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 5 |
| Forêt de Borredà (128) ⚠️ | Borredà › Berguedà | 5 |
| Forêt de Castellar de n'Hug (22) ⚠️ | Castellar de n'Hug › Berguedà | 5 |
| Forêt de la Pobla de Lillet (40) ⚠️ | la Pobla de Lillet › Berguedà | 5 |
| Forêt de Sant Jaume de Frontanyà (26) ⚠️ | Sant Jaume de Frontanyà › Berguedà | 5 |
| Forêt de Vallcebre (33) ⚠️ | Vallcebre › Berguedà | 5 |
| Forêt de Castellar del Riu (56) ⚠️ | Castellar del Riu › Berguedà | 5 |
| Forêt de Cercs (61) ⚠️ | Cercs › Berguedà | 5 |
| Forêt de Gisclareny (70) ⚠️ | Gisclareny › Berguedà | 5 |
| Forêt de Collsuspina (11) ⚠️ | Collsuspina › Moianès | 5 |
| Forêt de Orís (11) ⚠️ | Orís › Osona (Barcelone) | 5 |
| Forêt de Orís (20) ⚠️ | Orís › Osona (Barcelone) | 5 |
| Forêt de les Masies de Voltregà (12) ⚠️ | les Masies de Voltregà › Osona (Barcelone) | 5 |
| Forêt de Gurb (23) ⚠️ | Gurb › Osona (Barcelone) | 5 |
| Forêt de Tordera (75) ⚠️ | Tordera › Maresme | 5 |
| Forêt de Fogars de la Selva (13) ⚠️ | Fogars de la Selva › la Selva (Barcelone) | 5 |
| Forêt de Fogars de la Selva (18) ⚠️ | Fogars de la Selva › la Selva (Barcelone) | 5 |
| Forêt de Tordera (82) ⚠️ | Tordera › Maresme | 5 |
| Forêt de Vilanova del Vallès (13) ⚠️ | Vilanova del Vallès › Vallès Oriental | 5 |
| Bois de Santa Coloma de Gramenet ⚠️ | Santa Coloma de Gramenet › Barcelonès | 5 |
| Forêt de Alella (8) ⚠️ | Alella › Maresme | 5 |
| Forêt de Guardiola de Berguedà (135) ⚠️ | Guardiola de Berguedà › Berguedà | 5 |
| Forêt de Guardiola de Berguedà (136) ⚠️ | Guardiola de Berguedà › Berguedà | 5 |
| Forêt de Sant Martí de Tous (32) ⚠️ | Sant Martí de Tous › Anoia | 5 |
| Forêt de Sant Martí de Tous (37) ⚠️ | Jorba › Anoia | 5 |
| Forêt de Sant Martí de Tous (39) ⚠️ | Sant Martí de Tous › Anoia | 5 |
| Forêt de Sant Feliu Sasserra (26) ⚠️ | Sant Feliu Sasserra › Bages | 5 |
| Forêt de Castellar de n'Hug (37) ⚠️ | Castellar de n'Hug › Berguedà | 5 |
| Forêt de la Pobla de Claramunt (20) ⚠️ | la Pobla de Claramunt › Anoia | 5 |
| Forêt de Viladecavalls (16) ⚠️ | Viladecavalls › Vallès Occidental | 5 |
| Forêt de Gelida (33) ⚠️ | Gelida › Alt Penedès | 5 |
| Forêt de Gelida (34) ⚠️ | Gelida › Alt Penedès | 5 |
| Forêt de la Pobla de Claramunt (26) ⚠️ | la Pobla de Claramunt › Anoia | 5 |
| Forêt de la Torre de Claramunt (16) ⚠️ | la Torre de Claramunt › Anoia | 5 |
| Forêt de Piera (40) ⚠️ | Piera › Anoia | 5 |
| Forêt de Mediona (36) ⚠️ | Mediona › Alt Penedès | 5 |
| Forêt de Sant Quintí de Mediona (3) ⚠️ | Sant Quintí de Mediona › Alt Penedès | 5 |
| Forêt de Mediona (62) ⚠️ | Mediona › Alt Penedès | 5 |
| Forêt de Mediona (63) ⚠️ | Mediona › Alt Penedès | 5 |
| Forêt de Cabrera d'Anoia (38) ⚠️ | Cabrera d'Anoia › Anoia | 5 |
| Forêt de Cabrera d'Anoia (41) ⚠️ | Cabrera d'Anoia › Anoia | 5 |
| Forêt de Torrelavit (34) ⚠️ | Torrelavit › Alt Penedès | 5 |
| Forêt de Torrelavit (35) ⚠️ | Torrelavit › Alt Penedès | 5 |
| Forêt de Sant Quintí de Mediona (7) ⚠️ | Sant Pere de Riudebitlles › Alt Penedès | 5 |
| Forêt de Sant Sadurní d'Anoia (27) ⚠️ | Sant Sadurní d'Anoia › Alt Penedès | 5 |
| Forêt de Sant Quintí de Mediona (17) ⚠️ | Sant Quintí de Mediona › Alt Penedès | 5 |
| Forêt de Mediona (82) ⚠️ | Mediona › Alt Penedès | 5 |
| Forêt de Puig-reig (93) ⚠️ | Viver i Serrateix › Berguedà | 5 |
| Forêt de Òdena (91) ⚠️ | Òdena › Anoia | 5 |
| Forêt de Òdena (98) ⚠️ | Òdena › Anoia | 5 |
| Forêt de Òdena (105) ⚠️ | Òdena › Anoia | 5 |
| Forêt de Òdena (116) ⚠️ | Òdena › Anoia | 5 |
| Forêt de Òdena (118) ⚠️ | Òdena › Anoia | 5 |
| Forêt de Tavertet (52) ⚠️ | Tavertet › Osona (Barcelone) | 5 |
| Forêt de Tavertet (65) ⚠️ | Tavertet › Osona (Barcelone) | 5 |
| Forêt de Alpens (22) ⚠️ | Alpens › Lluçanès | 5 |
| Forêt de Alpens (24) ⚠️ | Alpens › Lluçanès | 5 |
| Forêt de Lluçà (79) ⚠️ | Lluçà › Lluçanès | 5 |
| Forêt de Palafolls (32) ⚠️ | Palafolls › Maresme | 5 |
| Forêt de Calella (9) ⚠️ | Calella › Maresme | 5 |
| Forêt de Arenys de Munt (8) ⚠️ | Arenys de Munt › Maresme | 5 |
| Forêt de Sant Celoni (46) ⚠️ | Sant Celoni › Vallès Oriental | 5 |
| Forêt de Sant Celoni (49) ⚠️ | Sant Celoni › Vallès Oriental | 5 |
| Forêt de Fogars de la Selva (39) ⚠️ | Fogars de la Selva › la Selva (Barcelone) | 5 |
| Forêt de Gualba (18) ⚠️ | Gualba › Vallès Oriental | 5 |
| Forêt de Gualba (20) ⚠️ | Gualba › Vallès Oriental | 5 |
| Forêt de Gualba (28) ⚠️ | Sant Celoni › Vallès Oriental | 5 |
| Forêt de Sant Celoni (73) ⚠️ | Sant Celoni › Vallès Oriental | 5 |
| Forêt de Sant Cugat del Vallès (161) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 5 |
| Forêt de Santpedor (49) ⚠️ | Santpedor › Bages | 5 |
| Forêt de Sallent (128) ⚠️ | Sallent › Bages | 5 |
| Forêt de Castellnou de Bages (61) ⚠️ | Castellnou de Bages › Bages | 5 |
| Forêt de Castellnou de Bages (80) ⚠️ | Castellnou de Bages › Bages | 5 |
| Forêt de Súria (48) ⚠️ | Súria › Bages | 5 |
| Forêt de Fonollosa (134) ⚠️ | Fonollosa › Bages | 5 |
| Forêt de Sant Mateu de Bages (112) ⚠️ | Sant Mateu de Bages › Bages | 5 |
| Forêt de Fonollosa (167) ⚠️ | Fonollosa › Bages | 5 |
| Forêt de Sant Sadurní d'Osormort (33) ⚠️ | Sant Sadurní d'Osormort › Osona (Barcelone) | 5 |
| Forêt de Folgueroles (5) ⚠️ | Folgueroles › Osona (Barcelone) | 5 |
| Forêt de Folgueroles (6) ⚠️ | Folgueroles › Osona (Barcelone) | 5 |
| Forêt de Taradell (28) ⚠️ | Taradell › Osona (Barcelone) | 5 |
| Forêt de Taradell (30) ⚠️ | Taradell › Osona (Barcelone) | 5 |
| Forêt de Sant Julià de Vilatorta (17) ⚠️ | Sant Julià de Vilatorta › Osona (Barcelone) | 5 |
| Forêt de el Brull (42) ⚠️ | el Brull › Osona (Barcelone) | 5 |
| Parc de Montigalà ⚠️ | Badalona › Barcelonès | 5 |
| Forêt de Cabrils (5) ⚠️ | Cabrils › Maresme | 5 |
| Bois de Cabrera de Mar (2) ⚠️ | Cabrera de Mar › Maresme | 5 |
| Serrat de Garrigons ⚠️ | Gurb › Osona (Barcelone) | 5 |
| Forêt de Palau-solità i Plegamans (19) ⚠️ | Palau-solità i Plegamans › Vallès Occidental | 5 |
| Forêt de Lliçà d'Amunt (22) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 5 |
| Parc de l'Agulla ⚠️ | Manresa › Bages | 5 |
| Forêt de la Pobla de Lillet (65) ⚠️ | la Pobla de Lillet › Berguedà | 5 |
| Forêt de Sant Andreu de Llavaneres ⚠️ | Sant Andreu de Llavaneres › Maresme | 4 |
| Parc de Can Bernet ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 4 |
| Parc de Torreblanca ⚠️ | Sant Joan Despí › Baix Llobregat | 4 |
| Parc de Can Solei i Ca l'Arnús ⚠️ | Badalona › Barcelonès | 4 |
| Parc del Turó de la Peira ⚠️ | Barcelona › Barcelonès | 4 |
| Parc del Mirador del Poble Sec ⚠️ | Barcelona › Barcelonès | 4 |
| Bois de Canovelles (2) ⚠️ | Canovelles › Vallès Oriental | 4 |
| Forêt de Sant Celoni ⚠️ | Sant Celoni › Vallès Oriental | 4 |
| Forêt de Molins de Rei ⚠️ | Molins de Rei › Baix Llobregat | 4 |
| Forêt de Lluçà ⚠️ | Lluçà › Lluçanès | 4 |
| Forêt de Sant Sadurní d'Osormort (4) ⚠️ | Sant Sadurní d'Osormort › Osona (Barcelone) | 4 |
| Forêt de l'Esquirol (4) ⚠️ | l'Esquirol › Osona (Barcelone) | 4 |
| Forêt de Campins (3) ⚠️ | Campins › Vallès Oriental | 4 |
| Forêt de Fogars de Montclús (3) ⚠️ | Fogars de Montclús › Vallès Oriental | 4 |
| Forêt de Oristà (4) ⚠️ | Oristà › Lluçanès | 4 |
| Forêt de Tordera (11) ⚠️ | Tordera › Maresme | 4 |
| Forêt de l'Estany (2) ⚠️ | l'Estany › Moianès | 4 |
| Forêt de Bellprat (9) ⚠️ | Bellprat › Anoia | 4 |
| Forêt de Sant Sadurní d'Anoia ⚠️ | Sant Sadurní d'Anoia › Alt Penedès | 4 |
| Forêt de Piera ⚠️ | Piera › Anoia | 4 |
| Parc de la Marina ⚠️ | Viladecans › Baix Llobregat | 4 |
| Parc de Gavà (2) ⚠️ | Gavà › Baix Llobregat | 4 |
| Bois de Sant Cugat del Vallès (30) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 4 |
| Parc de Sabadell ⚠️ | Sabadell › Vallès Occidental | 4 |
| Jardins de la Maternitat ⚠️ | Barcelona › Barcelonès | 4 |
| Forêt de Palau-solità i Plegamans ⚠️ | Palau-solità i Plegamans › Vallès Occidental | 4 |
| Forêt de Sant Pere de Ribes (8) ⚠️ | Sant Pere de Ribes › Garraf | 4 |
| Parc del Riu ⚠️ | el Prat de Llobregat › Baix Llobregat | 4 |
| Parc del Mil·leni ⚠️ | Gavà › Baix Llobregat | 4 |
| Parc de la Fontsanta ⚠️ | Sant Joan Despí › Baix Llobregat | 4 |
| Forêt de Sant Climent de Llobregat (11) ⚠️ | Sant Climent de Llobregat › Baix Llobregat | 4 |
| Forêt de Subirats (13) ⚠️ | Subirats › Alt Penedès | 4 |
| Forêt de Subirats (20) ⚠️ | Subirats › Alt Penedès | 4 |
| Parc del Turó d'en Caritg ⚠️ | Badalona › Barcelonès | 4 |
| Forêt de Vilanova i la Geltrú (2) ⚠️ | Vilanova i la Geltrú › Garraf | 4 |
| Forêt de Subirats (24) ⚠️ | Subirats › Alt Penedès | 4 |
| Forêt de Olivella (6) ⚠️ | Olivella › Garraf | 4 |
| Forêt de Subirats (49) ⚠️ | Subirats › Alt Penedès | 4 |
| Parc de la Creueta ⚠️ | Santa Perpètua de Mogoda › Vallès Occidental | 4 |
| els Pinetons ⚠️ | Mollet del Vallès › Vallès Oriental | 4 |
| Forêt de Castellet i la Gornal (37) ⚠️ | Castellet i la Gornal › Alt Penedès | 4 |
| Forêt de Castellet i la Gornal (39) ⚠️ | Castellet i la Gornal › Alt Penedès | 4 |
| Parc del Laberint d'Horta ⚠️ | Barcelona › Barcelonès | 4 |
| Forêt de Sant Llorenç d'Hortons (18) ⚠️ | Sant Llorenç d'Hortons › Alt Penedès | 4 |
| Forêt de Sant Llorenç d'Hortons (28) ⚠️ | Sant Llorenç d'Hortons › Alt Penedès | 4 |
| Forêt de Santa Maria de Palautordera (3) ⚠️ | Santa Maria de Palautordera › Vallès Oriental | 4 |
| Forêt de Santa Maria de Palautordera (4) ⚠️ | Santa Maria de Palautordera › Vallès Oriental | 4 |
| Forêt de Caldes de Montbui ⚠️ | Caldes de Montbui › Vallès Oriental | 4 |
| Bois de Òrrius ⚠️ | Òrrius › Maresme | 4 |
| Bois de Argentona (2) ⚠️ | Argentona › Maresme | 4 |
| Bois de Cabrils (4) ⚠️ | Cabrils › Maresme | 4 |
| Bois de Vilassar de Dalt ⚠️ | Vilassar de Dalt › Maresme | 4 |
| Bois de Vallromanes (3) ⚠️ | Vallromanes › Vallès Oriental | 4 |
| Bois de Vilassar de Dalt (16) ⚠️ | Vilassar de Dalt › Maresme | 4 |
| Bois de Òrrius (13) ⚠️ | Òrrius › Maresme | 4 |
| Bois de Vallromanes (7) ⚠️ | Vallromanes › Vallès Oriental | 4 |
| Bois de Argentona (19) ⚠️ | Argentona › Maresme | 4 |
| Bois de Teià (2) ⚠️ | Teià › Maresme | 4 |
| Bois de Teià (6) ⚠️ | Teià › Maresme | 4 |
| Bois de la Roca del Vallès (27) ⚠️ | la Roca del Vallès › Vallès Oriental | 4 |
| Bois de la Roca del Vallès (30) ⚠️ | la Roca del Vallès › Vallès Oriental | 4 |
| Bois de Llinars del Vallès (5) ⚠️ | Llinars del Vallès › Vallès Oriental | 4 |
| Bois de Llinars del Vallès (15) ⚠️ | Llinars del Vallès › Vallès Oriental | 4 |
| Parc de Can Buxeres ⚠️ | l'Hospitalet de Llobregat › Barcelonès | 4 |
| Forêt de Aguilar de Segarra (5) ⚠️ | Aguilar de Segarra › Bages | 4 |
| El Bosc Tancat - Natupark ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 4 |
| Forêt de Avià ⚠️ | Avià › Berguedà | 4 |
| Forêt de Sant Pere Sallavinera (2) ⚠️ | Sant Pere Sallavinera › Anoia | 4 |
| Bois de Cabrils (9) ⚠️ | Cabrils › Maresme | 4 |
| Forêt de Montcada i Reixac (6) ⚠️ | Montcada i Reixac › Vallès Occidental | 4 |
| Bois de Argentona (35) ⚠️ | Argentona › Maresme | 4 |
| Parc Forestal ⚠️ | Mataró › Maresme | 4 |
| Bois de Canovelles (4) ⚠️ | Canovelles › Vallès Oriental | 4 |
| Forêt de Barcelona (12) ⚠️ | Barcelona › Barcelonès | 4 |
| Bosc de Sant Nicolau ⚠️ | Granollers › Vallès Oriental | 4 |
| Forêt de Montcada i Reixac (18) ⚠️ | Montcada i Reixac › Vallès Occidental | 4 |
| Forêt de Castelldefels (4) ⚠️ | Castelldefels › Baix Llobregat | 4 |
| Forêt de Sabadell (13) ⚠️ | Sabadell › Vallès Occidental | 4 |
| Forêt de Sabadell (14) ⚠️ | Sabadell › Vallès Occidental | 4 |
| Forêt de Sabadell (27) ⚠️ | Sabadell › Vallès Occidental | 4 |
| Forêt de Terrassa (27) ⚠️ | Terrassa › Vallès Occidental | 4 |
| Forêt de Sant Boi de Llobregat (5) ⚠️ | Sant Boi de Llobregat › Baix Llobregat | 4 |
| Parc de les Planes ⚠️ | l'Hospitalet de Llobregat › Barcelonès | 4 |
| Parc de Can Jalpí ⚠️ | Arenys de Munt › Maresme | 4 |
| Forêt de Badalona (8) ⚠️ | Badalona › Barcelonès | 4 |
| Forêt de Castellbisbal (3) ⚠️ | Castellbisbal › Vallès Occidental | 4 |
| Forêt de Rubí (12) ⚠️ | Rubí › Vallès Occidental | 4 |
| Forêt de Rubí (24) ⚠️ | Rubí › Vallès Occidental | 4 |
| Forêt de Terrassa (63) ⚠️ | Terrassa › Vallès Occidental | 4 |
| Forêt de Sant Salvador de Guardiola (11) ⚠️ | Sant Salvador de Guardiola › Bages | 4 |
| Forêt de Sant Salvador de Guardiola (14) ⚠️ | Sant Salvador de Guardiola › Bages | 4 |
| Forêt de Badalona (16) ⚠️ | Badalona › Barcelonès | 4 |
| Forêt de Esparreguera (2) ⚠️ | Esparreguera › Baix Llobregat | 4 |
| Forêt de Sant Llorenç Savall (9) ⚠️ | Sant Llorenç Savall › Vallès Occidental | 4 |
| Forêt de Sentmenat (6) ⚠️ | Sentmenat › Vallès Occidental | 4 |
| Bois de Palau-solità i Plegamans (3) ⚠️ | Palau-solità i Plegamans › Vallès Occidental | 4 |
| Forêt de Sant Sadurní d'Anoia (23) ⚠️ | Sant Sadurní d'Anoia › Alt Penedès | 4 |
| Bois de Sant Cugat del Vallès (94) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 4 |
| Forêt de Santa Eulàlia de Ronçana (3) ⚠️ | Santa Eulàlia de Ronçana › Vallès Oriental | 4 |
| Forêt de Santa Eulàlia de Ronçana (4) ⚠️ | Santa Eulàlia de Ronçana › Vallès Oriental | 4 |
| Forêt de Vilanova del Vallès (2) ⚠️ | Vilanova del Vallès › Vallès Oriental | 4 |
| Bois de Sant Llorenç Savall (15) ⚠️ | Sant Llorenç Savall › Vallès Occidental | 4 |
| Bois de Balenyà ⚠️ | Balenyà › Osona (Barcelone) | 4 |
| Forêt de Cubelles (10) ⚠️ | Cubelles › Garraf | 4 |
| Bois de Font-rubí (2) ⚠️ | Font-rubí › Alt Penedès | 4 |
| Bois de Lliçà d'Amunt (25) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 4 |
| Forêt de la Garriga (6) ⚠️ | la Garriga › Vallès Oriental | 4 |
| Forêt de la Garriga (10) ⚠️ | la Garriga › Vallès Oriental | 4 |
| Forêt de Taradell (2) ⚠️ | Taradell › Osona (Barcelone) | 4 |
| Bosc d'en Codern ⚠️ | Lliçà de Vall › Vallès Oriental | 4 |
| Forêt de l'Esquirol (108) ⚠️ | l'Esquirol › Osona (Barcelone) | 4 |
| Forêt de Sant Pere de Vilamajor (63) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 4 |
| Forêt de les Franqueses del Vallès (41) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 4 |
| Forêt de la Pobla de Lillet (2) ⚠️ | la Pobla de Lillet › Berguedà | 4 |
| Forêt de Malgrat de Mar (2) ⚠️ | Malgrat de Mar › Maresme | 4 |
| Bois de Torrelles de Foix (5) ⚠️ | Torrelles de Foix › Alt Penedès | 4 |
| Forêt de Castellar de n'Hug (2) ⚠️ | Castellar de n'Hug › Berguedà | 4 |
| Forêt de Premià de Dalt (2) ⚠️ | Premià de Dalt › Maresme | 4 |
| Forêt de Teià ⚠️ | Teià › Maresme | 4 |
| Bois de Castellví de la Marca (2) ⚠️ | Castellví de la Marca › Alt Penedès | 4 |
| Forêt de Vallcebre (7) ⚠️ | Vallcebre › Berguedà | 4 |
| Forêt de Arenys de Mar (5) ⚠️ | Arenys de Mar › Maresme | 4 |
| Bois de Jorba (12) ⚠️ | Jorba › Anoia | 4 |
| Bois de Veciana (9) ⚠️ | Veciana › Anoia | 4 |
| Bois de Piera (6) ⚠️ | Piera › Anoia | 4 |
| Forêt de Borredà (10) ⚠️ | Borredà › Berguedà | 4 |
| Parc de Sant Adrià de Besòs (5) ⚠️ | Sant Adrià de Besòs › Barcelonès | 4 |
| Parc de la Pau (6) ⚠️ | Sant Adrià de Besòs › Barcelonès | 4 |
| Bois de Llinars del Vallès (28) ⚠️ | Llinars del Vallès › Vallès Oriental | 4 |
| Forêt de Vic (14) ⚠️ | Vic › Osona (Barcelone) | 4 |
| Forêt de Cercs (9) ⚠️ | Cercs › Berguedà | 4 |
| Forêt de Cardona (36) ⚠️ | Cardona › Bages | 4 |
| Forêt de Matadepera (211) ⚠️ | Matadepera › Vallès Occidental | 4 |
| Forêt de Rajadell (14) ⚠️ | Rajadell › Bages | 4 |
| Forêt de Sallent (41) ⚠️ | Sallent › Bages | 4 |
| Forêt de Sallent (43) ⚠️ | Sallent › Bages | 4 |
| Forêt de Avinyó (18) ⚠️ | Avinyó › Bages | 4 |
| Forêt de Avinyó (22) ⚠️ | Avinyó › Bages | 4 |
| Forêt de Balsareny (20) ⚠️ | Balsareny › Bages | 4 |
| Forêt de Balsareny (35) ⚠️ | Balsareny › Bages | 4 |
| Forêt de Balsareny (40) ⚠️ | Balsareny › Bages | 4 |
| Forêt de Artés (8) ⚠️ | Artés › Bages | 4 |
| Forêt de Sant Fruitós de Bages (10) ⚠️ | Sant Fruitós de Bages › Bages | 4 |
| Forêt de Sant Fruitós de Bages (21) ⚠️ | Sant Fruitós de Bages › Bages | 4 |
| Forêt de Montmajor (31) ⚠️ | Montmajor › Berguedà | 4 |
| Forêt de Manresa (51) ⚠️ | Manresa › Bages | 4 |
| Forêt de Terrassa (69) ⚠️ | Terrassa › Vallès Occidental | 4 |
| Forêt de Gisclareny (8) ⚠️ | Gisclareny › Berguedà | 4 |
| Forêt de Fonollosa (127) ⚠️ | Fonollosa › Bages | 4 |
| Forêt de Castellfollit de Riubregós (6) ⚠️ | Castellfollit de Riubregós › Anoia | 4 |
| Forêt de Lliçà d'Amunt (18) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 4 |
| Forêt de Manresa (94) ⚠️ | Manresa › Bages | 4 |
| Forêt de Oristà (87) ⚠️ | Oristà › Lluçanès | 4 |
| Forêt de Avià (14) ⚠️ | Avià › Berguedà | 4 |
| Forêt de Cercs (12) ⚠️ | Cercs › Berguedà | 4 |
| Forêt de Olvan (13) ⚠️ | Olvan › Berguedà | 4 |
| Forêt de Manresa (115) ⚠️ | Manresa › Bages | 4 |
| Forêt de Balsareny (57) ⚠️ | Balsareny › Bages | 4 |
| Forêt de Navàs (22) ⚠️ | Balsareny › Bages | 4 |
| Forêt de Puig-reig (7) ⚠️ | Puig-reig › Berguedà | 4 |
| Forêt de Avinyó (26) ⚠️ | Avinyó › Bages | 4 |
| Forêt de Avinyó (28) ⚠️ | Avinyó › Bages | 4 |
| Forêt de Sallent (74) ⚠️ | Sallent › Bages | 4 |
| Forêt de Balsareny (65) ⚠️ | Balsareny › Bages | 4 |
| Forêt de Montmajor (66) ⚠️ | Montmajor › Berguedà | 4 |
| Forêt de Oristà (93) ⚠️ | Oristà › Lluçanès | 4 |
| Forêt de Santa Maria d'Oló (20) ⚠️ | Santa Maria d'Oló › Moianès | 4 |
| Forêt de Sant Salvador de Guardiola (29) ⚠️ | Sant Salvador de Guardiola › Bages | 4 |
| Forêt de Sant Salvador de Guardiola (34) ⚠️ | Sant Salvador de Guardiola › Bages | 4 |
| Forêt de Sant Salvador de Guardiola (36) ⚠️ | Sant Salvador de Guardiola › Bages | 4 |
| Forêt de Puig-reig (12) ⚠️ | Puig-reig › Berguedà | 4 |
| Forêt de Puig-reig (16) ⚠️ | Puig-reig › Berguedà | 4 |
| Forêt de Puig-reig (22) ⚠️ | Puig-reig › Berguedà | 4 |
| Forêt de Puig-reig (28) ⚠️ | Puig-reig › Berguedà | 4 |
| Forêt de Gaià (22) ⚠️ | Gaià › Bages | 4 |
| Forêt de l'Espunyola (41) ⚠️ | l'Espunyola › Berguedà | 4 |
| Forêt de l'Espunyola (45) ⚠️ | l'Espunyola › Berguedà | 4 |
| Forêt de Montmajor (70) ⚠️ | Montmajor › Berguedà | 4 |
| Forêt de Santa Margarida de Montbui (13) ⚠️ | Santa Margarida de Montbui › Anoia | 4 |
| Forêt de Vilanova del Camí (2) ⚠️ | Vilanova del Camí › Anoia | 4 |
| Forêt de Sant Esteve Sesrovires (20) ⚠️ | Sant Esteve Sesrovires › Baix Llobregat | 4 |
| Forêt de Sant Andreu de la Barca (2) ⚠️ | Sant Andreu de la Barca › Baix Llobregat | 4 |
| Parc de Gurb (4) ⚠️ | Vic › Osona (Barcelone) | 4 |
| Forêt de Vic (19) ⚠️ | Vic › Osona (Barcelone) | 4 |
| Forêt de Vic (24) ⚠️ | Vic › Osona (Barcelone) | 4 |
| Forêt de Pallejà (6) ⚠️ | Pallejà › Baix Llobregat | 4 |
| Forêt de Cervelló (15) ⚠️ | Cervelló › Baix Llobregat | 4 |
| Forêt de Cervelló (19) ⚠️ | Sant Vicenç dels Horts › Baix Llobregat | 4 |
| Forêt de Cervelló (20) ⚠️ | Cervelló › Baix Llobregat | 4 |
| Forêt de Vacarisses (24) ⚠️ | Vacarisses › Vallès Occidental | 4 |
| Forêt de Vacarisses (27) ⚠️ | Vacarisses › Vallès Occidental | 4 |
| Forêt de Vacarisses (39) ⚠️ | Vacarisses › Vallès Occidental | 4 |
| Forêt de Esparreguera (17) ⚠️ | Esparreguera › Baix Llobregat | 4 |
| Forêt de Castellbell i el Vilar (16) ⚠️ | Castellbell i el Vilar › Bages | 4 |
| Forêt de Guardiola de Berguedà (29) ⚠️ | Guardiola de Berguedà › Berguedà | 4 |
| Forêt de el Bruc (21) ⚠️ | el Bruc › Anoia | 4 |
| Forêt de Castellbell i el Vilar (38) ⚠️ | Castellbell i el Vilar › Bages | 4 |
| Forêt de Castellbell i el Vilar (51) ⚠️ | Castellbell i el Vilar › Bages | 4 |
| Forêt de Castellbell i el Vilar (65) ⚠️ | Castellbell i el Vilar › Bages | 4 |
| Forêt de el Pont de Vilomara i Rocafort (7) ⚠️ | el Pont de Vilomara i Rocafort › Bages | 4 |
| Forêt de Moià (28) ⚠️ | Moià › Moianès | 4 |
| Forêt de Moià (30) ⚠️ | Moià › Moianès | 4 |
| Forêt de Vilanova i la Geltrú (22) ⚠️ | Vilanova i la Geltrú › Garraf | 4 |
| Forêt de Sitges (23) ⚠️ | Sitges › Garraf | 4 |
| Forêt de Sitges (41) ⚠️ | Sitges › Garraf | 4 |
| Forêt de Sitges (58) ⚠️ | Sitges › Garraf | 4 |
| Forêt de Sitges (66) ⚠️ | Sitges › Garraf | 4 |
| Forêt de Gavà (77) ⚠️ | Gavà › Baix Llobregat | 4 |
| Forêt de Manresa (125) ⚠️ | Manresa › Bages | 4 |
| Forêt de Sant Salvador de Guardiola (49) ⚠️ | Sant Salvador de Guardiola › Bages | 4 |
| Forêt de Artés (25) ⚠️ | Artés › Bages | 4 |
| Forêt de Artés (26) ⚠️ | Artés › Bages | 4 |
| Forêt de Calders (29) ⚠️ | Calders › Moianès | 4 |
| Forêt de Artés (30) ⚠️ | Artés › Bages | 4 |
| Forêt de Artés (32) ⚠️ | Artés › Bages | 4 |
| Forêt de Calders (36) ⚠️ | Calders › Moianès | 4 |
| Zona de la Font dels Oms ⚠️ | Cardedeu › Vallès Oriental | 4 |
| Forêt de Sant Antoni de Vilamajor (37) ⚠️ | Sant Antoni de Vilamajor › Vallès Oriental | 4 |
| Forêt de la Garriga (41) ⚠️ | la Garriga › Vallès Oriental | 4 |
| Forêt de Cànoves i Samalús (37) ⚠️ | Cànoves i Samalús › Vallès Oriental | 4 |
| Forêt de Cànoves i Samalús (40) ⚠️ | Cànoves i Samalús › Vallès Oriental | 4 |
| Forêt de la Garriga (43) ⚠️ | Cànoves i Samalús › Vallès Oriental | 4 |
| Forêt de Sallent (83) ⚠️ | Sallent › Bages | 4 |
| Forêt de Sallent (84) ⚠️ | Sallent › Bages | 4 |
| Forêt de Avinyó (96) ⚠️ | Avinyó › Bages | 4 |
| Forêt de Avinyó (97) ⚠️ | Avinyó › Bages | 4 |
| Forêt de Navàs (35) ⚠️ | Navàs › Bages | 4 |
| Forêt de Navàs (47) ⚠️ | Navàs › Bages | 4 |
| Forêt de Gaià (42) ⚠️ | Gaià › Bages | 4 |
| Forêt de Gaià (45) ⚠️ | Gaià › Bages | 4 |
| Forêt de Sant Esteve de Palautordera (12) ⚠️ | Sant Esteve de Palautordera › Vallès Oriental | 4 |
| Forêt de Vilada (14) ⚠️ | Vilada › Berguedà | 4 |
| Forêt de Castell de l'Areny (14) ⚠️ | Castell de l'Areny › Berguedà | 4 |
| Forêt de Castell de l'Areny (19) ⚠️ | Castell de l'Areny › Berguedà | 4 |
| Forêt de Cercs (27) ⚠️ | Cercs › Berguedà | 4 |
| Forêt de Cercs (32) ⚠️ | Cercs › Berguedà | 4 |
| Forêt de Cercs (33) ⚠️ | Cercs › Berguedà | 4 |
| Forêt de Cercs (46) ⚠️ | Cercs › Berguedà | 4 |
| Forêt de Cercs (47) ⚠️ | Cercs › Berguedà | 4 |
| Forêt de Castellar del Riu (22) ⚠️ | Castellar del Riu › Berguedà | 4 |
| Forêt de Castellar del Riu (23) ⚠️ | Castellar del Riu › Berguedà | 4 |
| Forêt de la Pobla de Lillet (14) ⚠️ | la Pobla de Lillet › Berguedà | 4 |
| Forêt de la Pobla de Lillet (26) ⚠️ | la Pobla de Lillet › Berguedà | 4 |
| Forêt de Santa Maria de Besora (16) ⚠️ | Santa Maria de Besora › Osona (Barcelone) | 4 |
| Forêt de Guardiola de Berguedà (51) ⚠️ | Guardiola de Berguedà › Berguedà | 4 |
| Forêt de Mura (25) ⚠️ | Mura › Bages | 4 |
| Forêt de Talamanca (25) ⚠️ | Talamanca › Bages | 4 |
| Forêt de Talamanca (27) ⚠️ | Talamanca › Bages | 4 |
| Forêt de Mura (32) ⚠️ | Mura › Bages | 4 |
| Forêt de Navarcles (9) ⚠️ | Navarcles › Bages | 4 |
| Forêt de Sant Vicenç de Castellet (28) ⚠️ | Sant Vicenç de Castellet › Bages | 4 |
| Forêt de Calders (65) ⚠️ | Calders › Moianès | 4 |
| Forêt de Aguilar de Segarra (30) ⚠️ | Aguilar de Segarra › Bages | 4 |
| Forêt de Aguilar de Segarra (42) ⚠️ | Aguilar de Segarra › Bages | 4 |
| Forêt de Sant Pere Sallavinera (11) ⚠️ | Sant Pere Sallavinera › Anoia | 4 |
| Forêt de Terrassa (73) ⚠️ | Terrassa › Vallès Occidental | 4 |
| Forêt de Terrassa (77) ⚠️ | Terrassa › Vallès Occidental | 4 |
| Forêt de Castellbell i el Vilar (70) ⚠️ | Castellbell i el Vilar › Bages | 4 |
| Forêt de els Prats de Rei (23) ⚠️ | els Prats de Rei › Anoia | 4 |
| Forêt de Rajadell (47) ⚠️ | Rajadell › Bages | 4 |
| Forêt de Rajadell (53) ⚠️ | Rajadell › Bages | 4 |
| Forêt de Sant Salvador de Guardiola (60) ⚠️ | Sant Salvador de Guardiola › Bages | 4 |
| Forêt de Sant Salvador de Guardiola (70) ⚠️ | Sant Salvador de Guardiola › Bages | 4 |
| Forêt de Castellfollit del Boix (21) ⚠️ | Castellfollit del Boix › Bages | 4 |
| Forêt de Sant Salvador de Guardiola (90) ⚠️ | Sant Salvador de Guardiola › Bages | 4 |
| Forêt de Sant Salvador de Guardiola (96) ⚠️ | Sant Salvador de Guardiola › Bages | 4 |
| Forêt de el Bruc (35) ⚠️ | el Bruc › Anoia | 4 |
| Forêt de Sant Salvador de Guardiola (117) ⚠️ | Sant Salvador de Guardiola › Bages | 4 |
| Forêt de Vacarisses (66) ⚠️ | Vacarisses › Vallès Occidental | 4 |
| Forêt de Esparreguera (27) ⚠️ | Esparreguera › Baix Llobregat | 4 |
| Forêt de Esparreguera (28) ⚠️ | Esparreguera › Baix Llobregat | 4 |
| Forêt de Esparreguera (29) ⚠️ | Esparreguera › Baix Llobregat | 4 |
| Forêt de Olesa de Montserrat (44) ⚠️ | Olesa de Montserrat › Baix Llobregat | 4 |
| Forêt de Abrera (13) ⚠️ | Abrera › Baix Llobregat | 4 |
| Bois de Abrera (4) ⚠️ | Abrera › Baix Llobregat | 4 |
| Bois de Abrera (5) ⚠️ | Abrera › Baix Llobregat | 4 |
| Forêt de Abrera (21) ⚠️ | Abrera › Baix Llobregat | 4 |
| Forêt de Abrera (29) ⚠️ | Abrera › Baix Llobregat | 4 |
| Forêt de Castellbisbal (38) ⚠️ | Castellbisbal › Vallès Occidental | 4 |
| Forêt de Navàs (68) ⚠️ | Navàs › Bages | 4 |
| Forêt de Puig-reig (73) ⚠️ | Puig-reig › Berguedà | 4 |
| Forêt de Sagàs (11) ⚠️ | Sagàs › Berguedà | 4 |
| Forêt de Olvan (17) ⚠️ | Olvan › Berguedà | 4 |
| Forêt de Olvan (21) ⚠️ | Olvan › Berguedà | 4 |
| Forêt de Avià (21) ⚠️ | Avià › Berguedà | 4 |
| Forêt de Avià (27) ⚠️ | Avià › Berguedà | 4 |
| Forêt de l'Espunyola (50) ⚠️ | l'Espunyola › Berguedà | 4 |
| Forêt de l'Espunyola (64) ⚠️ | l'Espunyola › Berguedà | 4 |
| Forêt de l'Espunyola (66) ⚠️ | l'Espunyola › Berguedà | 4 |
| Forêt de Montmajor (87) ⚠️ | Montmajor › Berguedà | 4 |
| Forêt de Montmajor (95) ⚠️ | Montmajor › Berguedà | 4 |
| Forêt de Navàs (110) ⚠️ | Navàs › Bages | 4 |
| Forêt de Súria (34) ⚠️ | Súria › Bages | 4 |
| Forêt de Navàs (139) ⚠️ | Navàs › Bages | 4 |
| Forêt de Navàs (141) ⚠️ | Navàs › Bages | 4 |
| Forêt de Viver i Serrateix (78) ⚠️ | Viver i Serrateix › Berguedà | 4 |
| Forêt de Gaià (69) ⚠️ | Gaià › Bages | 4 |
| Forêt de Avinyó (110) ⚠️ | Avinyó › Bages | 4 |
| Forêt de Santa Maria de Merlès (31) ⚠️ | Santa Maria de Merlès › Berguedà | 4 |
| Forêt de Santa Maria de Merlès (32) ⚠️ | Santa Maria de Merlès › Berguedà | 4 |
| Forêt de Santa Maria de Merlès (38) ⚠️ | Santa Maria de Merlès › Berguedà | 4 |
| Forêt de Prats de Lluçanès (4) ⚠️ | Prats de Lluçanès › Lluçanès | 4 |
| Forêt de Santa Eulàlia de Riuprimer (5) ⚠️ | Santa Eulàlia de Riuprimer › Osona (Barcelone) | 4 |
| Forêt de Santa Eulàlia de Riuprimer (6) ⚠️ | Santa Eulàlia de Riuprimer › Osona (Barcelone) | 4 |
| Forêt de Sant Cugat del Vallès (116) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 4 |
| Bois de Sant Cugat del Vallès (119) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 4 |
| Forêt de Sant Cugat del Vallès (122) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 4 |
| Forêt de Barcelona (54) ⚠️ | Barcelona › Barcelonès | 4 |
| Forêt de Barcelona (56) ⚠️ | Barcelona › Barcelonès | 4 |
| Forêt de Rubí (83) ⚠️ | Rubí › Vallès Occidental | 4 |
| Forêt de Castellbisbal (44) ⚠️ | Castellbisbal › Vallès Occidental | 4 |
| Forêt de la Quar (10) ⚠️ | la Quar › Berguedà | 4 |
| Forêt de Saldes (18) ⚠️ | Saldes › Berguedà | 4 |
| Forêt de Saldes (22) ⚠️ | Saldes › Berguedà | 4 |
| Forêt de Borredà (22) ⚠️ | Borredà › Berguedà | 4 |
| Forêt de Borredà (33) ⚠️ | Borredà › Berguedà | 4 |
| Forêt de Sant Fost de Campsentelles (10) ⚠️ | Sant Fost de Campsentelles › Vallès Oriental | 4 |
| Forêt de Jorba (8) ⚠️ | Jorba › Anoia | 4 |
| Forêt de Òdena (39) ⚠️ | Òdena › Anoia | 4 |
| Forêt de Òdena (43) ⚠️ | Òdena › Anoia | 4 |
| Forêt de Òdena (50) ⚠️ | Òdena › Anoia | 4 |
| Forêt de Vilanova del Camí (13) ⚠️ | Vilanova del Camí › Anoia | 4 |
| Forêt de Vilanova del Camí (14) ⚠️ | Vilanova del Camí › Anoia | 4 |
| Forêt de Santa Margarida de Montbui (21) ⚠️ | Santa Margarida de Montbui › Anoia | 4 |
| Forêt de Sitges (71) ⚠️ | Sitges › Garraf | 4 |
| Forêt de Olivella (67) ⚠️ | Olivella › Garraf | 4 |
| Forêt de Olivella (83) ⚠️ | Olivella › Garraf | 4 |
| Forêt de Begues (65) ⚠️ | Begues › Baix Llobregat | 4 |
| Forêt de Olivella (100) ⚠️ | Olivella › Garraf | 4 |
| Forêt de Olivella (101) ⚠️ | Olivella › Garraf | 4 |
| Forêt de Sant Pere de Ribes (98) ⚠️ | Sant Pere de Ribes › Garraf | 4 |
| Forêt de Sitges (83) ⚠️ | Sant Pere de Ribes › Garraf | 4 |
| Forêt de Castellet i la Gornal (80) ⚠️ | Castellet i la Gornal › Alt Penedès | 4 |
| Forêt de Vilanova i la Geltrú (45) ⚠️ | Vilanova i la Geltrú › Garraf | 4 |
| Forêt de Vilanova i la Geltrú (52) ⚠️ | Vilanova i la Geltrú › Garraf | 4 |
| Forêt de Vilanova i la Geltrú (55) ⚠️ | Vilanova i la Geltrú › Garraf | 4 |
| Forêt de Vilanova i la Geltrú (63) ⚠️ | Vilanova i la Geltrú › Garraf | 4 |
| Forêt de Canyelles (26) ⚠️ | Canyelles › Garraf | 4 |
| Forêt de Olivella (127) ⚠️ | Olivella › Garraf | 4 |
| Forêt de Olivella (133) ⚠️ | Olivella › Garraf | 4 |
| Forêt de Olivella (134) ⚠️ | Olivella › Garraf | 4 |
| Forêt de Sant Feliu de Llobregat (2) ⚠️ | Sant Feliu de Llobregat › Baix Llobregat | 4 |
| Forêt de Gisclareny (10) ⚠️ | Gisclareny › Berguedà | 4 |
| Forêt de Viver i Serrateix (107) ⚠️ | Viver i Serrateix › Berguedà | 4 |
| Forêt de Borredà (54) ⚠️ | Borredà › Berguedà | 4 |
| Forêt de Santa Maria de Merlès (82) ⚠️ | Santa Maria de Merlès › Berguedà | 4 |
| Forêt de Santa Maria de Merlès (103) ⚠️ | Santa Maria de Merlès › Berguedà | 4 |
| Forêt de Santa Maria de Merlès (107) ⚠️ | Santa Maria de Merlès › Berguedà | 4 |
| Forêt de Santa Maria de Merlès (113) ⚠️ | Santa Maria de Merlès › Berguedà | 4 |
| Forêt de el Papiol (7) ⚠️ | el Papiol › Baix Llobregat | 4 |
| Forêt de Sant Pere Sallavinera (62) ⚠️ | Sant Pere Sallavinera › Anoia | 4 |
| Bois de Sant Cebrià de Vallalta ⚠️ | Sant Cebrià de Vallalta › Maresme | 4 |
| Forêt de Rupit i Pruit (29) ⚠️ | Rupit i Pruit › Osona (Barcelone) | 4 |
| Forêt de Borredà (59) ⚠️ | Borredà › Berguedà | 4 |
| Forêt de la Garriga (46) ⚠️ | la Garriga › Vallès Oriental | 4 |
| Forêt de els Hostalets de Pierola (16) ⚠️ | els Hostalets de Pierola › Anoia | 4 |
| Forêt de Monistrol de Calders (35) ⚠️ | Monistrol de Calders › Moianès | 4 |
| Forêt de Granera (20) ⚠️ | Granera › Moianès | 4 |
| Forêt de Taradell (9) ⚠️ | Taradell › Osona (Barcelone) | 4 |
| Forêt de Tagamanent (18) ⚠️ | Tagamanent › Vallès Oriental | 4 |
| Forêt de Tagamanent (21) ⚠️ | Tagamanent › Vallès Oriental | 4 |
| Forêt de Centelles (12) ⚠️ | Centelles › Osona (Barcelone) | 4 |
| Forêt de Tagamanent (28) ⚠️ | Tagamanent › Vallès Oriental | 4 |
| Forêt de el Brull (37) ⚠️ | el Brull › Osona (Barcelone) | 4 |
| Forêt de Montseny (16) ⚠️ | Montseny › Vallès Oriental | 4 |
| Forêt de Figaró-Montmany (8) ⚠️ | Figaró-Montmany › Vallès Oriental | 4 |
| Forêt de Bigues i Riells del Fai (16) ⚠️ | Bigues i Riells del Fai › Vallès Oriental | 4 |
| Forêt de Sant Feliu de Codines (13) ⚠️ | Bigues i Riells del Fai › Vallès Oriental | 4 |
| Forêt de Bigues i Riells del Fai (32) ⚠️ | Bigues i Riells del Fai › Vallès Oriental | 4 |
| Forêt de Sant Quirze Safaja (47) ⚠️ | Sant Quirze Safaja › Moianès | 4 |
| Forêt de l'Ametlla del Vallès (21) ⚠️ | l'Ametlla del Vallès › Vallès Oriental | 4 |
| Forêt de l'Ametlla del Vallès (22) ⚠️ | l'Ametlla del Vallès › Vallès Oriental | 4 |
| Forêt de Santa Maria d'Oló (69) ⚠️ | Santa Maria d'Oló › Moianès | 4 |
| Forêt de Santa Maria d'Oló (73) ⚠️ | Santa Maria d'Oló › Moianès | 4 |
| Forêt de Santa Maria d'Oló (74) ⚠️ | Santa Maria d'Oló › Moianès | 4 |
| Forêt de Oristà (137) ⚠️ | Oristà › Lluçanès | 4 |
| Forêt de Oristà (143) ⚠️ | Oristà › Lluçanès | 4 |
| Forêt de Sant Mateu de Bages (73) ⚠️ | Sant Mateu de Bages › Bages | 4 |
| Forêt de Navàs (155) ⚠️ | Navàs › Bages | 4 |
| Forêt de Navàs (160) ⚠️ | Navàs › Bages | 4 |
| Forêt de Cardona (72) ⚠️ | Cardona › Bages | 4 |
| Forêt de Cardona (78) ⚠️ | Cardona › Bages | 4 |
| Forêt de Cardona (99) ⚠️ | Cardona › Bages | 4 |
| Forêt de Sant Mateu de Bages (85) ⚠️ | Sant Mateu de Bages › Bages | 4 |
| Forêt de Sant Mateu de Bages (100) ⚠️ | Sant Mateu de Bages › Bages | 4 |
| Forêt de Súria (40) ⚠️ | Súria › Bages | 4 |
| Forêt de l'Ametlla del Vallès (24) ⚠️ | l'Ametlla del Vallès › Vallès Oriental | 4 |
| Forêt de Vilanova i la Geltrú (73) ⚠️ | Vilanova i la Geltrú › Garraf | 4 |
| Forêt de Guardiola de Berguedà (71) ⚠️ | Guardiola de Berguedà › Berguedà | 4 |
| Forêt de Santa Maria de Merlès (126) ⚠️ | Santa Maria de Merlès › Berguedà | 4 |
| Forêt de Santa Maria de Merlès (128) ⚠️ | Santa Maria de Merlès › Berguedà | 4 |
| Forêt de Santa Maria de Merlès (129) ⚠️ | Santa Maria de Merlès › Berguedà | 4 |
| Forêt de Lluçà (14) ⚠️ | Lluçà › Lluçanès | 4 |
| Forêt de Sagàs (41) ⚠️ | Sagàs › Berguedà | 4 |
| Forêt de Sagàs (42) ⚠️ | Sagàs › Berguedà | 4 |
| Forêt de l'Esquirol (118) ⚠️ | l'Esquirol › Osona (Barcelone) | 4 |
| Forêt de Mataró (4) ⚠️ | Mataró › Maresme | 4 |
| Forêt de Dosrius (16) ⚠️ | Dosrius › Maresme | 4 |
| Forêt de Dosrius (22) ⚠️ | Dosrius › Maresme | 4 |
| Forêt de Dosrius (27) ⚠️ | Dosrius › Maresme | 4 |
| Forêt de Dosrius (28) ⚠️ | Dosrius › Maresme | 4 |
| Forêt de Balenyà (14) ⚠️ | Balenyà › Osona (Barcelone) | 4 |
| Forêt de Tona (9) ⚠️ | Tona › Osona (Barcelone) | 4 |
| Forêt de Balenyà (24) ⚠️ | Balenyà › Osona (Barcelone) | 4 |
| Forêt de Tona (27) ⚠️ | Tona › Osona (Barcelone) | 4 |
| Forêt de Muntanyola (35) ⚠️ | Muntanyola › Osona (Barcelone) | 4 |
| Forêt de Malla (13) ⚠️ | Malla › Osona (Barcelone) | 4 |
| Forêt de Saldes (46) ⚠️ | Saldes › Berguedà | 4 |
| Forêt de Saldes (53) ⚠️ | Saldes › Berguedà | 4 |
| Forêt de Bagà (38) ⚠️ | Bagà › Berguedà | 4 |
| Forêt de Guardiola de Berguedà (81) ⚠️ | Guardiola de Berguedà › Berguedà | 4 |
| Forêt de Castellar del Riu (47) ⚠️ | Castellar del Riu › Berguedà | 4 |
| Forêt de Fígols (21) ⚠️ | Fígols › Berguedà | 4 |
| Forêt de Fígols (31) ⚠️ | Fígols › Berguedà | 4 |
| Forêt de Lluçà (20) ⚠️ | Lluçà › Lluçanès | 4 |
| Forêt de Lluçà (30) ⚠️ | Lluçà › Lluçanès | 4 |
| Forêt de Olost (4) ⚠️ | Olost › Lluçanès | 4 |
| Forêt de Borredà (92) ⚠️ | Borredà › Berguedà | 4 |
| Forêt de Santa Maria de Merlès (141) ⚠️ | Santa Maria de Merlès › Berguedà | 4 |
| Forêt de Borredà (113) ⚠️ | Borredà › Berguedà | 4 |
| Forêt de la Pobla de Lillet (55) ⚠️ | la Pobla de Lillet › Berguedà | 4 |
| Forêt de la Pobla de Lillet (56) ⚠️ | la Pobla de Lillet › Berguedà | 4 |
| Forêt de les Franqueses del Vallès (71) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 4 |
| Forêt de Saldes (76) ⚠️ | Saldes › Berguedà | 4 |
| Forêt de Vallcebre (32) ⚠️ | Vallcebre › Berguedà | 4 |
| Forêt de Cercs (58) ⚠️ | Cercs › Berguedà | 4 |
| Forêt de Fígols (36) ⚠️ | Fígols › Berguedà | 4 |
| Forêt de Fígols (38) ⚠️ | Fígols › Berguedà | 4 |
| Forêt de Saldes (94) ⚠️ | Saldes › Berguedà | 4 |
| Forêt de Saldes (97) ⚠️ | Saldes › Berguedà | 4 |
| Forêt de Guardiola de Berguedà (124) ⚠️ | Guardiola de Berguedà › Berguedà | 4 |
| Forêt de Sant Antoni de Vilamajor (49) ⚠️ | Sant Antoni de Vilamajor › Vallès Oriental | 4 |
| Forêt de Sant Antoni de Vilamajor (52) ⚠️ | Sant Antoni de Vilamajor › Vallès Oriental | 4 |
| Forêt de Saldes (102) ⚠️ | Saldes › Berguedà | 4 |
| Forêt de Vallcebre (36) ⚠️ | Vallcebre › Berguedà | 4 |
| Forêt de Vallcebre (37) ⚠️ | Vallcebre › Berguedà | 4 |
| Forêt de Saldes (120) ⚠️ | Saldes › Berguedà | 4 |
| Forêt de Saldes (121) ⚠️ | Saldes › Berguedà | 4 |
| Forêt de Saldes (122) ⚠️ | Saldes › Berguedà | 4 |
| Forêt de Gisclareny (72) ⚠️ | Gisclareny › Berguedà | 4 |
| Forêt de les Franqueses del Vallès (83) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 4 |
| Forêt de Centelles (35) ⚠️ | Centelles › Osona (Barcelone) | 4 |
| Forêt de Sant Vicenç de Torelló (9) ⚠️ | Sant Vicenç de Torelló › Osona (Barcelone) | 4 |
| Forêt de Orís (25) ⚠️ | Orís › Osona (Barcelone) | 4 |
| Forêt de les Masies de Voltregà (11) ⚠️ | les Masies de Voltregà › Osona (Barcelone) | 4 |
| Forêt de Tavèrnoles (4) ⚠️ | Tavèrnoles › Osona (Barcelone) | 4 |
| Forêt de Vilanova de Sau (45) ⚠️ | Vilanova de Sau › Osona (Barcelone) | 4 |
| Forêt de Vilanova de Sau (50) ⚠️ | Vilanova de Sau › Osona (Barcelone) | 4 |
| Forêt de les Masies de Roda (10) ⚠️ | les Masies de Roda › Osona (Barcelone) | 4 |
| Forêt de Vilanova de Sau (54) ⚠️ | Vilanova de Sau › Osona (Barcelone) | 4 |
| Bois de Tordera ⚠️ | Tordera › Maresme | 4 |
| Parc de Martorelles ⚠️ | Martorelles › Vallès Oriental | 4 |
| Forêt de Vilanova del Vallès (11) ⚠️ | Vilanova del Vallès › Vallès Oriental | 4 |
| Forêt de Vallromanes (16) ⚠️ | Vallromanes › Vallès Oriental | 4 |
| Forêt de Vallromanes (18) ⚠️ | Vallromanes › Vallès Oriental | 4 |
| Forêt de Alella (5) ⚠️ | Alella › Maresme | 4 |
| Forêt de Cubelles (43) ⚠️ | Cubelles › Garraf | 4 |
| Forêt de Sant Vicenç dels Horts (8) ⚠️ | Sant Vicenç dels Horts › Baix Llobregat | 4 |
| Forêt de Piera (28) ⚠️ | Piera › Anoia | 4 |
| Forêt de els Hostalets de Pierola (28) ⚠️ | els Hostalets de Pierola › Anoia | 4 |
| Forêt de Castellfollit del Boix (41) ⚠️ | Castellolí › Anoia | 4 |
| Forêt de Sant Martí de Tous (18) ⚠️ | Sant Martí de Tous › Anoia | 4 |
| Forêt de Sant Martí de Tous (26) ⚠️ | Sant Martí de Tous › Anoia | 4 |
| Forêt de Santa Margarida de Montbui (29) ⚠️ | Santa Margarida de Montbui › Anoia | 4 |
| Forêt de Sant Martí de Tous (38) ⚠️ | Sant Martí de Tous › Anoia | 4 |
| Forêt de Moià (52) ⚠️ | Moià › Moianès | 4 |
| Forêt de Sant Feliu Sasserra (25) ⚠️ | Sant Feliu Sasserra › Bages | 4 |
| Forêt de Sant Feliu Sasserra (29) ⚠️ | Sant Feliu Sasserra › Bages | 4 |
| Forêt de Sant Feliu Sasserra (33) ⚠️ | Sant Feliu Sasserra › Bages | 4 |
| Forêt de Castellar de n'Hug (34) ⚠️ | Castellar de n'Hug › Berguedà | 4 |
| Forêt de Oristà (158) ⚠️ | Oristà › Lluçanès | 4 |
| Forêt de Santa Margarida de Montbui (49) ⚠️ | Santa Margarida de Montbui › Anoia | 4 |
| Forêt de Òdena (72) ⚠️ | Òdena › Anoia | 4 |
| Forêt de la Torre de Claramunt (8) ⚠️ | la Torre de Claramunt › Anoia | 4 |
| Forêt de Viladecavalls (15) ⚠️ | Viladecavalls › Vallès Occidental | 4 |
| Forêt de Cardona (112) ⚠️ | Cardona › Bages | 4 |
| Forêt de Rubí (96) ⚠️ | Rubí › Vallès Occidental | 4 |
| Forêt de Abrera (34) ⚠️ | Abrera › Baix Llobregat | 4 |
| Forêt de Vilanova del Camí (24) ⚠️ | Vilanova del Camí › Anoia | 4 |
| Forêt de la Torre de Claramunt (12) ⚠️ | la Torre de Claramunt › Anoia | 4 |
| Forêt de Vallbona d'Anoia (5) ⚠️ | Vallbona d'Anoia › Anoia | 4 |
| Forêt de Cabrera d'Anoia (9) ⚠️ | Cabrera d'Anoia › Anoia | 4 |
| Forêt de Cabrera d'Anoia (13) ⚠️ | Cabrera d'Anoia › Anoia | 4 |
| Forêt de Mediona (27) ⚠️ | Mediona › Alt Penedès | 4 |
| Forêt de Cabrera d'Anoia (14) ⚠️ | Cabrera d'Anoia › Anoia | 4 |
| Forêt de Piera (47) ⚠️ | Piera › Anoia | 4 |
| Forêt de Piera (48) ⚠️ | Piera › Anoia | 4 |
| Forêt de Mediona (37) ⚠️ | Mediona › Alt Penedès | 4 |
| Forêt de Mediona (42) ⚠️ | Mediona › Alt Penedès | 4 |
| Forêt de la Torre de Claramunt (19) ⚠️ | la Torre de Claramunt › Anoia | 4 |
| Forêt de la Torre de Claramunt (25) ⚠️ | la Torre de Claramunt › Anoia | 4 |
| Forêt de Mediona (47) ⚠️ | Mediona › Alt Penedès | 4 |
| Forêt de Piera (53) ⚠️ | Piera › Anoia | 4 |
| Forêt de Cabrera d'Anoia (45) ⚠️ | Cabrera d'Anoia › Anoia | 4 |
| Forêt de Piera (55) ⚠️ | Piera › Anoia | 4 |
| Forêt de Torrelavit (33) ⚠️ | Torrelavit › Alt Penedès | 4 |
| Forêt de Piera (81) ⚠️ | Piera › Anoia | 4 |
| Forêt de Torrelavit (51) ⚠️ | Torrelavit › Alt Penedès | 4 |
| Forêt de Mediona (90) ⚠️ | Mediona › Alt Penedès | 4 |
| Forêt de Font-rubí (20) ⚠️ | Font-rubí › Alt Penedès | 4 |
| Forêt de Pontons (20) ⚠️ | Pontons › Alt Penedès | 4 |
| Forêt de la Llacuna (20) ⚠️ | la Llacuna › Anoia | 4 |
| Forêt de Puig-reig (89) ⚠️ | Puig-reig › Berguedà | 4 |
| Forêt de Puig-reig (91) ⚠️ | Puig-reig › Berguedà | 4 |
| Forêt de Òdena (92) ⚠️ | Òdena › Anoia | 4 |
| Forêt de Òdena (103) ⚠️ | Òdena › Anoia | 4 |
| Forêt de Tavertet (45) ⚠️ | Tavertet › Osona (Barcelone) | 4 |
| Forêt de Tavertet (62) ⚠️ | Tavertet › Osona (Barcelone) | 4 |
| Forêt de Tavertet (68) ⚠️ | Tavertet › Osona (Barcelone) | 4 |
| Forêt de Tavertet (79) ⚠️ | Tavertet › Osona (Barcelone) | 4 |
| Parc del Poblenou (2) ⚠️ | Barcelona › Barcelonès | 4 |
| Forêt de Lluçà (62) ⚠️ | Lluçà › Lluçanès | 4 |
| Forêt de Alpens (18) ⚠️ | Alpens › Lluçanès | 4 |
| Forêt de Lluçà (87) ⚠️ | Lluçà › Lluçanès | 4 |
| Forêt de Lluçà (88) ⚠️ | Lluçà › Lluçanès | 4 |
| Forêt de la Quar (47) ⚠️ | la Quar › Berguedà | 4 |
| Forêt de Sant Cebrià de Vallalta (12) ⚠️ | Sant Cebrià de Vallalta › Maresme | 4 |
| Forêt de Palafolls (30) ⚠️ | Palafolls › Maresme | 4 |
| Parc Dalmau ⚠️ | Calella › Maresme | 4 |
| Forêt de Sant Vicenç de Montalt (10) ⚠️ | Sant Vicenç de Montalt › Maresme | 4 |
| Forêt de Vallgorguina (16) ⚠️ | Vallgorguina › Vallès Oriental | 4 |
| Forêt de Fogars de la Selva (40) ⚠️ | Fogars de la Selva › la Selva (Barcelone) | 4 |
| Forêt de Fogars de la Selva (41) ⚠️ | Fogars de la Selva › la Selva (Barcelone) | 4 |
| Forêt de Tordera (115) ⚠️ | Tordera › Maresme | 4 |
| Forêt de Sant Celoni (55) ⚠️ | Sant Celoni › Vallès Oriental | 4 |
| Forêt de Gualba (14) ⚠️ | Gualba › Vallès Oriental | 4 |
| Forêt de Gualba (17) ⚠️ | Gualba › Vallès Oriental | 4 |
| Forêt de Sant Celoni (67) ⚠️ | Sant Celoni › Vallès Oriental | 4 |
| Forêt de Sant Celoni (77) ⚠️ | Sant Celoni › Vallès Oriental | 4 |
| Forêt de Gironella (31) ⚠️ | Gironella › Berguedà | 4 |
| Forêt de Castellnou de Bages (59) ⚠️ | Castellnou de Bages › Bages | 4 |
| Forêt de Castellnou de Bages (67) ⚠️ | Castellnou de Bages › Bages | 4 |
| Forêt de Callús (26) ⚠️ | Callús › Bages | 4 |
| Forêt de Callús (34) ⚠️ | Callús › Bages | 4 |
| Forêt de Sant Mateu de Bages (109) ⚠️ | Sant Mateu de Bages › Bages | 4 |
| Forêt de Sant Mateu de Bages (144) ⚠️ | Sant Mateu de Bages › Bages | 4 |
| Forêt de Vallcebre (76) ⚠️ | Vallcebre › Berguedà | 4 |
| Forêt de Sant Sadurní d'Osormort (37) ⚠️ | Sant Sadurní d'Osormort › Osona (Barcelone) | 4 |
| Forêt de Folgueroles (3) ⚠️ | Folgueroles › Osona (Barcelone) | 4 |
| Forêt de Tavèrnoles (11) ⚠️ | Tavèrnoles › Osona (Barcelone) | 4 |
| Forêt de Santa Maria d'Oló (84) ⚠️ | Santa Maria d'Oló › Moianès | 4 |
| Forêt de Pallejà (10) ⚠️ | Pallejà › Baix Llobregat | 4 |
| Forêt de Manlleu (9) ⚠️ | Manlleu › Osona (Barcelone) | 4 |
| Forêt de Arenys de Mar (10) ⚠️ | Arenys de Mar › Maresme | 4 |
| Forêt de Cabrera de Mar (4) ⚠️ | Cabrera de Mar › Maresme | 4 |
| Forêt de Vic (49) ⚠️ | Vic › Osona (Barcelone) | 4 |
| Forêt de Vic (55) ⚠️ | Vic › Osona (Barcelone) | 4 |
| Forêt de Gurb (50) ⚠️ | Gurb › Osona (Barcelone) | 4 |
| Forêt de Vic (76) ⚠️ | Vic › Osona (Barcelone) | 4 |
| Espai natural de Can Cabanyes ⚠️ | Granollers › Vallès Oriental | 4 |
| Forêt de Parets del Vallès (8) ⚠️ | Parets del Vallès › Vallès Oriental | 4 |
| Forêt de Sant Pere de Ribes (116) ⚠️ | Sant Pere de Ribes › Garraf | 4 |
| Forêt de Sentmenat (18) ⚠️ | Sentmenat › Vallès Occidental | 4 |
| Forêt de Santa Perpètua de Mogoda (22) ⚠️ | Santa Perpètua de Mogoda › Vallès Occidental | 4 |
| Forêt de Lliçà d'Amunt (24) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 4 |
| Forêt de Prats de Lluçanès (35) ⚠️ | Prats de Lluçanès › Lluçanès | 4 |
| Forêt de Calders (84) ⚠️ | Calders › Moianès | 4 |
| Forêt de Castellterçol (84) ⚠️ | Castellterçol › Moianès | 4 |
| Forêt de Sant Fruitós de Bages (86) ⚠️ | Sant Fruitós de Bages › Bages | 4 |
| Forêt de Gavà (7) ⚠️ | Gavà › Baix Llobregat | 3 |
| Parc Europa ⚠️ | Santa Coloma de Gramenet › Barcelonès | 3 |
| Forêt de Palafolls (4) ⚠️ | Palafolls › Maresme | 3 |
| Bois de Barcelona (6) ⚠️ | Barcelona › Barcelonès | 3 |
| Bois de Lliçà d'Amunt (4) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 3 |
| Bois de Lliçà d'Amunt (14) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 3 |
| Bosc de Can Montcau ⚠️ | Lliçà d'Amunt › Vallès Oriental | 3 |
| Forêt de Vilanova de Sau (4) ⚠️ | Vilanova de Sau › Osona (Barcelone) | 3 |
| Forêt de Sant Jaume de Frontanyà ⚠️ | Sant Jaume de Frontanyà › Berguedà | 3 |
| Forêt de Sant Martí de Tous (4) ⚠️ | Sant Martí de Tous › Anoia | 3 |
| Forêt de Tordera (5) ⚠️ | Tordera › Maresme | 3 |
| Forêt de Tordera (6) ⚠️ | Tordera › Maresme | 3 |
| Forêt de l'Esquirol (5) ⚠️ | l'Esquirol › Osona (Barcelone) | 3 |
| Forêt de Borredà (3) ⚠️ | Borredà › Berguedà | 3 |
| Forêt de Sant Llorenç Savall (3) ⚠️ | Sant Llorenç Savall › Vallès Occidental | 3 |
| Forêt de Terrassa (3) ⚠️ | Terrassa › Vallès Occidental | 3 |
| Forêt de Sant Sadurní d'Osormort (15) ⚠️ | Sant Sadurní d'Osormort › Osona (Barcelone) | 3 |
| Parc de la Trinitat ⚠️ | Barcelona › Barcelonès | 3 |
| Forêt de Tordera (15) ⚠️ | Tordera › Maresme | 3 |
| Parc de Ribes Roges ⚠️ | Vilanova i la Geltrú › Garraf | 3 |
| Parc del Congost ⚠️ | Granollers › Vallès Oriental | 3 |
| Parc de l'Arborètum ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 3 |
| Parc del Lledoner ⚠️ | Granollers › Vallès Oriental | 3 |
| Forêt de Sant Climent de Llobregat (7) ⚠️ | Sant Climent de Llobregat › Baix Llobregat | 3 |
| Forêt de Torrelles de Llobregat (5) ⚠️ | Torrelles de Llobregat › Baix Llobregat | 3 |
| Parc de la Ribera ⚠️ | Santa Perpètua de Mogoda › Vallès Occidental | 3 |
| Forêt de Terrassa (18) ⚠️ | Terrassa › Vallès Occidental | 3 |
| Forêt de Palau-solità i Plegamans (2) ⚠️ | Palau-solità i Plegamans › Vallès Occidental | 3 |
| Forêt de Cerdanyola del Vallès (7) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 3 |
| Forêt de Sant Pere de Ribes (10) ⚠️ | Sant Pere de Ribes › Garraf | 3 |
| Turó d'Onofre Arnau ⚠️ | Mataró › Maresme | 3 |
| Forêt de Olivella (2) ⚠️ | Olivella › Garraf | 3 |
| Forêt de Gavà (12) ⚠️ | Gavà › Baix Llobregat | 3 |
| Forêt de Avinyonet del Penedès (4) ⚠️ | Avinyonet del Penedès › Alt Penedès | 3 |
| Forêt de Avinyonet del Penedès (5) ⚠️ | Avinyonet del Penedès › Alt Penedès | 3 |
| Forêt de Corbera de Llobregat ⚠️ | Corbera de Llobregat › Baix Llobregat | 3 |
| Parc del G4 ⚠️ | Badalona › Barcelonès | 3 |
| Forêt de Subirats (16) ⚠️ | Subirats › Alt Penedès | 3 |
| Forêt de Subirats (17) ⚠️ | Subirats › Alt Penedès | 3 |
| Forêt de Subirats (46) ⚠️ | Subirats › Alt Penedès | 3 |
| Parc Central (3) ⚠️ | Santa Perpètua de Mogoda › Vallès Occidental | 3 |
| Forêt de Sant Pere de Ribes (41) ⚠️ | Sant Pere de Ribes › Garraf | 3 |
| Forêt de Sant Pere de Ribes (52) ⚠️ | Sant Pere de Ribes › Garraf | 3 |
| Forêt de Olèrdola (31) ⚠️ | Olèrdola › Alt Penedès | 3 |
| Forêt de Olivella (34) ⚠️ | Olivella › Garraf | 3 |
| Forêt de Olivella (37) ⚠️ | Olivella › Garraf | 3 |
| Forêt de Sant Pere de Ribes (58) ⚠️ | Sant Pere de Ribes › Garraf | 3 |
| Forêt de Sant Pere de Ribes (62) ⚠️ | Sant Pere de Ribes › Garraf | 3 |
| Forêt de Vallirana (5) ⚠️ | Vallirana › Baix Llobregat | 3 |
| Forêt de Subirats (62) ⚠️ | Subirats › Alt Penedès | 3 |
| Forêt de Olesa de Bonesvalls (28) ⚠️ | Olesa de Bonesvalls › Alt Penedès | 3 |
| Forêt de Olèrdola (43) ⚠️ | Olèrdola › Alt Penedès | 3 |
| Forêt de Santa Margarida i els Monjos (2) ⚠️ | Santa Margarida i els Monjos › Alt Penedès | 3 |
| Forêt de Olèrdola (53) ⚠️ | Olèrdola › Alt Penedès | 3 |
| Forêt de Castellví de la Marca (4) ⚠️ | Castellví de la Marca › Alt Penedès | 3 |
| Forêt de Castellet i la Gornal (9) ⚠️ | Castellet i la Gornal › Alt Penedès | 3 |
| Forêt de Santa Margarida i els Monjos (15) ⚠️ | Santa Margarida i els Monjos › Alt Penedès | 3 |
| Forêt de Sant Pol de Mar (2) ⚠️ | Sant Pol de Mar › Maresme | 3 |
| Forêt de Castellví de la Marca (10) ⚠️ | Castellví de la Marca › Alt Penedès | 3 |
| Forêt de Castellví de la Marca (11) ⚠️ | Castellví de la Marca › Alt Penedès | 3 |
| Forêt de Subirats (73) ⚠️ | Subirats › Alt Penedès | 3 |
| Forêt de Sant Esteve Sesrovires (9) ⚠️ | Sant Esteve Sesrovires › Baix Llobregat | 3 |
| Forêt de Masquefa (3) ⚠️ | Masquefa › Anoia | 3 |
| Forêt de Sant Llorenç d'Hortons (19) ⚠️ | Sant Llorenç d'Hortons › Alt Penedès | 3 |
| Forêt de Sant Llorenç d'Hortons (24) ⚠️ | Sant Llorenç d'Hortons › Alt Penedès | 3 |
| Forêt de Bigues i Riells del Fai (5) ⚠️ | Bigues i Riells del Fai › Vallès Oriental | 3 |
| Forêt de Sant Sadurní d'Anoia (11) ⚠️ | Sant Sadurní d'Anoia › Alt Penedès | 3 |
| Forêt de Santa Fe del Penedès (3) ⚠️ | Santa Fe del Penedès › Alt Penedès | 3 |
| Forêt de Font-rubí (6) ⚠️ | Font-rubí › Alt Penedès | 3 |
| Parc Central de Nou Barris ⚠️ | Barcelona › Barcelonès | 3 |
| Forêt de Vilobí del Penedès (6) ⚠️ | Vilobí del Penedès › Alt Penedès | 3 |
| Forêt de Vallirana (19) ⚠️ | Vallirana › Baix Llobregat | 3 |
| Forêt de Castellví de la Marca (50) ⚠️ | Castellví de la Marca › Alt Penedès | 3 |
| Forêt de Fonollosa (2) ⚠️ | Fonollosa › Bages | 3 |
| Forêt de Fonollosa (5) ⚠️ | Fonollosa › Bages | 3 |
| Parc de Sant Pere de Ribes (2) ⚠️ | Sant Pere de Ribes › Garraf | 3 |
| Bois de Òrrius (2) ⚠️ | Òrrius › Maresme | 3 |
| Bois de Argentona (5) ⚠️ | Argentona › Maresme | 3 |
| Bois de Vilassar de Dalt (3) ⚠️ | Vilassar de Dalt › Maresme | 3 |
| Pineda de Cal Francès ⚠️ | Viladecans › Baix Llobregat | 3 |
| Bois de Vilanova del Vallès (3) ⚠️ | Vilanova del Vallès › Vallès Oriental | 3 |
| Bois de Vilanova del Vallès (5) ⚠️ | Vilanova del Vallès › Vallès Oriental | 3 |
| Bois de la Roca del Vallès (6) ⚠️ | la Roca del Vallès › Vallès Oriental | 3 |
| Bois de Vilassar de Dalt (14) ⚠️ | Vilassar de Dalt › Maresme | 3 |
| Bois de Vilassar de Dalt (18) ⚠️ | Vilassar de Dalt › Maresme | 3 |
| Forêt de Manlleu ⚠️ | Manlleu › Osona (Barcelone) | 3 |
| Bois de Argentona (12) ⚠️ | Argentona › Maresme | 3 |
| Bois de Argentona (13) ⚠️ | la Roca del Vallès › Vallès Oriental | 3 |
| Bois de Argentona (16) ⚠️ | Argentona › Maresme | 3 |
| Bois de Argentona (29) ⚠️ | Argentona › Maresme | 3 |
| Bois de Argentona (31) ⚠️ | Argentona › Maresme | 3 |
| Bois de Teià (4) ⚠️ | Teià › Maresme | 3 |
| Bois de Vallromanes (10) ⚠️ | Vallromanes › Vallès Oriental | 3 |
| Bois de Dosrius (5) ⚠️ | Dosrius › Maresme | 3 |
| Bois de la Roca del Vallès (24) ⚠️ | la Roca del Vallès › Vallès Oriental | 3 |
| Bois de la Roca del Vallès (26) ⚠️ | la Roca del Vallès › Vallès Oriental | 3 |
| Bois de Llinars del Vallès (4) ⚠️ | Llinars del Vallès › Vallès Oriental | 3 |
| Bois de la Roca del Vallès (36) ⚠️ | la Roca del Vallès › Vallès Oriental | 3 |
| Forêt de l'Espunyola ⚠️ | l'Espunyola › Berguedà | 3 |
| Forêt de Cardona (6) ⚠️ | Cardona › Bages | 3 |
| Forêt de els Prats de Rei (5) ⚠️ | els Prats de Rei › Anoia | 3 |
| Bois de Llinars del Vallès (26) ⚠️ | Llinars del Vallès › Vallès Oriental | 3 |
| Forêt de Balenyà (2) ⚠️ | Balenyà › Osona (Barcelone) | 3 |
| Forêt de Avià (3) ⚠️ | Avià › Berguedà | 3 |
| Forêt de Santa Margarida de Montbui ⚠️ | Santa Margarida de Montbui › Anoia | 3 |
| Forêt de Santa Perpètua de Mogoda (9) ⚠️ | Santa Perpètua de Mogoda › Vallès Occidental | 3 |
| Forêt de Sabadell (7) ⚠️ | Sabadell › Vallès Occidental | 3 |
| Forêt de Santa Perpètua de Mogoda (12) ⚠️ | Santa Perpètua de Mogoda › Vallès Occidental | 3 |
| Bois de l'Ametlla del Vallès ⚠️ | l'Ametlla del Vallès › Vallès Oriental | 3 |
| Bosc de la Font del Ràdium ⚠️ | Granollers › Vallès Oriental | 3 |
| Forêt de Barcelona (13) ⚠️ | Barcelona › Barcelonès | 3 |
| Parc de la Bastida ⚠️ | Santa Coloma de Gramenet › Barcelonès | 3 |
| Forêt de Badalona (6) ⚠️ | Badalona › Barcelonès | 3 |
| Forêt de Tiana (3) ⚠️ | Tiana › Maresme | 3 |
| Forêt de Rubí ⚠️ | Rubí › Vallès Occidental | 3 |
| Forêt de Sant Quirze del Vallès (3) ⚠️ | Sant Quirze del Vallès › Vallès Occidental | 3 |
| Forêt de Sabadell (20) ⚠️ | Sabadell › Vallès Occidental | 3 |
| Forêt de Polinyà (7) ⚠️ | Polinyà › Vallès Occidental | 3 |
| Forêt de Sabadell (26) ⚠️ | Sabadell › Vallès Occidental | 3 |
| Forêt de Sabadell (38) ⚠️ | Sabadell › Vallès Occidental | 3 |
| Forêt de Sabadell (40) ⚠️ | Sabadell › Vallès Occidental | 3 |
| Bois de Gurb ⚠️ | Gurb › Osona (Barcelone) | 3 |
| Forêt de les Masies de Voltregà (5) ⚠️ | les Masies de Voltregà › Osona (Barcelone) | 3 |
| Forêt de Sant Boi de Llobregat (7) ⚠️ | Sant Boi de Llobregat › Baix Llobregat | 3 |
| Parc del Tramvia ⚠️ | Montgat › Maresme | 3 |
| Forêt de Cercs ⚠️ | Cercs › Berguedà | 3 |
| Parc de les Glòries ⚠️ | Barcelona › Barcelonès | 3 |
| Forêt de Avià (7) ⚠️ | Avià › Berguedà | 3 |
| Parc de Argentona (11) ⚠️ | Argentona › Maresme | 3 |
| Forêt de Oristà (55) ⚠️ | Oristà › Lluçanès | 3 |
| Forêt de Oristà (74) ⚠️ | Oristà › Lluçanès | 3 |
| Parc d'en Serentill ⚠️ | Badalona › Barcelonès | 3 |
| Bois de Sant Fost de Campsentelles (4) ⚠️ | Sant Fost de Campsentelles › Vallès Oriental | 3 |
| Bois de Alella ⚠️ | Alella › Maresme | 3 |
| Bois de Montornès del Vallès ⚠️ | Montornès del Vallès › Vallès Oriental | 3 |
| Bois de Terrassa (3) ⚠️ | Terrassa › Vallès Occidental | 3 |
| Bois de Terrassa (4) ⚠️ | Terrassa › Vallès Occidental | 3 |
| Forêt de Terrassa (32) ⚠️ | Terrassa › Vallès Occidental | 3 |
| Forêt de Rubí (4) ⚠️ | Rubí › Vallès Occidental | 3 |
| Forêt de Rubí (8) ⚠️ | Rubí › Vallès Occidental | 3 |
| Forêt de Rubí (10) ⚠️ | Rubí › Vallès Occidental | 3 |
| Forêt de Castellbisbal (2) ⚠️ | Castellbisbal › Vallès Occidental | 3 |
| Forêt de Rubí (14) ⚠️ | Rubí › Vallès Occidental | 3 |
| Forêt de Terrassa (56) ⚠️ | Terrassa › Vallès Occidental | 3 |
| Forêt de Rubí (19) ⚠️ | Rubí › Vallès Occidental | 3 |
| Forêt de Sabadell (49) ⚠️ | Sabadell › Vallès Occidental | 3 |
| Forêt de Abrera (3) ⚠️ | Abrera › Baix Llobregat | 3 |
| Forêt de Sant Salvador de Guardiola (7) ⚠️ | Sant Salvador de Guardiola › Bages | 3 |
| Parc del Cerdanet ⚠️ | Sant Feliu de Llobregat › Baix Llobregat | 3 |
| Forêt de Corbera de Llobregat (4) ⚠️ | Corbera de Llobregat › Baix Llobregat | 3 |
| Forêt de Moià (7) ⚠️ | Moià › Moianès | 3 |
| Forêt de Sitges (12) ⚠️ | Sitges › Garraf | 3 |
| Forêt de Vic ⚠️ | Vic › Osona (Barcelone) | 3 |
| Forêt de Molins de Rei (6) ⚠️ | Molins de Rei › Baix Llobregat | 3 |
| Bois de Sant Cugat del Vallès (92) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 3 |
| Bois de Sant Cugat del Vallès (107) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 3 |
| Bois de Barcelona (65) ⚠️ | Barcelona › Barcelonès | 3 |
| Bois de Sentmenat (5) ⚠️ | Sentmenat › Vallès Occidental | 3 |
| Forêt de Santa Eulàlia de Ronçana (5) ⚠️ | Santa Eulàlia de Ronçana › Vallès Oriental | 3 |
| Bosc d'en Prat ⚠️ | Vilanova del Vallès › Vallès Oriental | 3 |
| Forêt de Olivella (41) ⚠️ | Olivella › Garraf | 3 |
| Bois de Balenyà (2) ⚠️ | Balenyà › Osona (Barcelone) | 3 |
| Forêt de Vilanova i la Geltrú (17) ⚠️ | Vilanova i la Geltrú › Garraf | 3 |
| Forêt de Fígols (2) ⚠️ | Fígols › Berguedà | 3 |
| Forêt de Balenyà (4) ⚠️ | Balenyà › Osona (Barcelone) | 3 |
| Bois de Montmaneu (5) ⚠️ | Montmaneu › Anoia | 3 |
| Forêt de el Brull (3) ⚠️ | el Brull › Osona (Barcelone) | 3 |
| Bois de Argençola (8) ⚠️ | Argençola › Anoia | 3 |
| Forêt de Cànoves i Samalús (7) ⚠️ | Cànoves i Samalús › Vallès Oriental | 3 |
| Forêt de Sant Pere de Vilamajor (37) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 3 |
| Forêt de l'Esquirol (16) ⚠️ | l'Esquirol › Osona (Barcelone) | 3 |
| Forêt de l'Esquirol (65) ⚠️ | l'Esquirol › Osona (Barcelone) | 3 |
| Forêt de Dosrius (2) ⚠️ | Dosrius › Maresme | 3 |
| Forêt de Tordera (20) ⚠️ | Tordera › Maresme | 3 |
| Forêt de Llinars del Vallès (10) ⚠️ | Llinars del Vallès › Vallès Oriental | 3 |
| Forêt de Llinars del Vallès (35) ⚠️ | Llinars del Vallès › Vallès Oriental | 3 |
| Bois de Montmaneu (30) ⚠️ | Montmaneu › Anoia | 3 |
| Bois de Montmaneu (32) ⚠️ | Montmaneu › Anoia | 3 |
| Bois de Torrelavit (9) ⚠️ | Torrelavit › Alt Penedès | 3 |
| Bois de Torrelavit (22) ⚠️ | Torrelavit › Alt Penedès | 3 |
| Parc Puig dels Jueus ⚠️ | Vic › Osona (Barcelone) | 3 |
| Forêt de Sant Feliu Sasserra (5) ⚠️ | Sant Feliu Sasserra › Bages | 3 |
| Forêt de Castellar de n'Hug (4) ⚠️ | Castellar de n'Hug › Berguedà | 3 |
| Forêt de Premià de Dalt ⚠️ | Premià de Dalt › Maresme | 3 |
| Bois de Rubió ⚠️ | Rubió › Anoia | 3 |
| Bois de Jorba (2) ⚠️ | Jorba › Anoia | 3 |
| Forêt de Vallcebre (9) ⚠️ | Vallcebre › Berguedà | 3 |
| Bois de Sant Martí de Tous (3) ⚠️ | Sant Martí de Tous › Anoia | 3 |
| Bois de Jorba (6) ⚠️ | Argençola › Anoia | 3 |
| Bois de Veciana (8) ⚠️ | Veciana › Anoia | 3 |
| Forêt de Subirats (86) ⚠️ | Subirats › Alt Penedès | 3 |
| Forêt de Alpens (14) ⚠️ | Alpens › Lluçanès | 3 |
| Forêt de Sant Pere de Vilamajor (70) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 3 |
| Forêt de Caldes de Montbui (8) ⚠️ | Caldes de Montbui › Vallès Oriental | 3 |
| Forêt de Cercs (6) ⚠️ | Cercs › Berguedà | 3 |
| Forêt de Collbató (3) ⚠️ | Collbató › Baix Llobregat | 3 |
| Forêt de Saldes (8) ⚠️ | Saldes › Berguedà | 3 |
| Forêt de Matadepera (212) ⚠️ | Matadepera › Vallès Occidental | 3 |
| Forêt de Fonollosa (91) ⚠️ | Fonollosa › Bages | 3 |
| Forêt de Balsareny (30) ⚠️ | Balsareny › Bages | 3 |
| Forêt de Balsareny (44) ⚠️ | Balsareny › Bages | 3 |
| Forêt de Artés (6) ⚠️ | Artés › Bages | 3 |
| Forêt de Calders (18) ⚠️ | Calders › Moianès | 3 |
| Forêt de Artés (15) ⚠️ | Artés › Bages | 3 |
| Forêt de Sant Fruitós de Bages (28) ⚠️ | Sant Fruitós de Bages › Bages | 3 |
| Forêt de Vallcebre (16) ⚠️ | Vallcebre › Berguedà | 3 |
| Forêt de Olesa de Montserrat (13) ⚠️ | Olesa de Montserrat › Baix Llobregat | 3 |
| Forêt de Manresa (34) ⚠️ | Manresa › Bages | 3 |
| Parc fluvial del Pont Nou ⚠️ | Manresa › Bages | 3 |
| Parc del Cardener ⚠️ | Manresa › Bages | 3 |
| Forêt de Manresa (44) ⚠️ | Manresa › Bages | 3 |
| Forêt de Manresa (45) ⚠️ | Manresa › Bages | 3 |
| Forêt de Sant Joan de Vilatorrada (30) ⚠️ | Sant Joan de Vilatorrada › Bages | 3 |
| Forêt de Manresa (50) ⚠️ | Manresa › Bages | 3 |
| Forêt de Rajadell (33) ⚠️ | Rajadell › Bages | 3 |
| Forêt de Terrassa (68) ⚠️ | Terrassa › Vallès Occidental | 3 |
| Forêt de Castellterçol (29) ⚠️ | Castellterçol › Moianès | 3 |
| Forêt de Castellar del Riu (10) ⚠️ | Castellar del Riu › Berguedà | 3 |
| Forêt de Casserres (12) ⚠️ | Casserres › Berguedà | 3 |
| Forêt de Sant Joan de Vilatorrada (41) ⚠️ | Sant Joan de Vilatorrada › Bages | 3 |
| Forêt de Cardona (41) ⚠️ | Cardona › Bages | 3 |
| Forêt de Fonollosa (96) ⚠️ | Fonollosa › Bages | 3 |
| Forêt de Fonollosa (115) ⚠️ | Fonollosa › Bages | 3 |
| Forêt de Fonollosa (117) ⚠️ | Fonollosa › Bages | 3 |
| Forêt de Fonollosa (125) ⚠️ | Fonollosa › Bages | 3 |
| Forêt de Cerdanyola del Vallès (55) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 3 |
| Forêt de Saldes (12) ⚠️ | Saldes › Berguedà | 3 |
| Forêt de els Hostalets de Pierola (12) ⚠️ | els Hostalets de Pierola › Anoia | 3 |
| Forêt de Castellterçol (54) ⚠️ | Castellterçol › Moianès | 3 |
| Forêt de Castellterçol (68) ⚠️ | Castellterçol › Moianès | 3 |
| Forêt de Castellterçol (71) ⚠️ | Castellterçol › Moianès | 3 |
| Forêt de Berga (10) ⚠️ | Berga › Berguedà | 3 |
| Forêt de Berga (38) ⚠️ | Berga › Berguedà | 3 |
| Forêt de Cercs (14) ⚠️ | Cercs › Berguedà | 3 |
| Forêt de Cercs (15) ⚠️ | Cercs › Berguedà | 3 |
| Forêt de Cardona (58) ⚠️ | Cardona › Bages | 3 |
| Forêt de Cercs (22) ⚠️ | Cercs › Berguedà | 3 |
| Bois de Viladecavalls (9) ⚠️ | Viladecavalls › Vallès Occidental | 3 |
| Forêt de Abrera (8) ⚠️ | Abrera › Baix Llobregat | 3 |
| Forêt de Montmajor (35) ⚠️ | l'Espunyola › Berguedà | 3 |
| Forêt de l'Espunyola (18) ⚠️ | l'Espunyola › Berguedà | 3 |
| Forêt de l'Espunyola (23) ⚠️ | l'Espunyola › Berguedà | 3 |
| Forêt de Artés (16) ⚠️ | Artés › Bages | 3 |
| Forêt de Vilafranca del Penedès (7) ⚠️ | Vilafranca del Penedès › Alt Penedès | 3 |
| Forêt de Balsareny (54) ⚠️ | Balsareny › Bages | 3 |
| Forêt de Sallent (53) ⚠️ | Sallent › Bages | 3 |
| Forêt de Navàs (23) ⚠️ | Navàs › Bages | 3 |
| Forêt de Puig-reig (8) ⚠️ | Puig-reig › Berguedà | 3 |
| Forêt de Gaià (18) ⚠️ | Gaià › Bages | 3 |
| Forêt de Avinyó (32) ⚠️ | Avinyó › Bages | 3 |
| Forêt de Avinyó (37) ⚠️ | Avinyó › Bages | 3 |
| Forêt de Avinyó (39) ⚠️ | Avinyó › Bages | 3 |
| Forêt de Sallent (76) ⚠️ | Sallent › Bages | 3 |
| Forêt de Balsareny (66) ⚠️ | Balsareny › Bages | 3 |
| Forêt de Olèrdola (60) ⚠️ | Olèrdola › Alt Penedès | 3 |
| Forêt de Oristà (96) ⚠️ | Oristà › Lluçanès | 3 |
| Forêt de Sant Salvador de Guardiola (33) ⚠️ | Sant Salvador de Guardiola › Bages | 3 |
| Forêt de Monistrol de Montserrat (9) ⚠️ | Monistrol de Montserrat › Bages | 3 |
| Forêt de Monistrol de Montserrat (10) ⚠️ | Monistrol de Montserrat › Bages | 3 |
| Forêt de Puig-reig (23) ⚠️ | Puig-reig › Berguedà | 3 |
| Forêt de Gaià (24) ⚠️ | Gaià › Bages | 3 |
| Forêt de Puig-reig (42) ⚠️ | Puig-reig › Berguedà | 3 |
| Forêt de Casserres (14) ⚠️ | Casserres › Berguedà | 3 |
| Forêt de Casserres (16) ⚠️ | Casserres › Berguedà | 3 |
| Forêt de Gironella (9) ⚠️ | Gironella › Berguedà | 3 |
| Forêt de Gelida (21) ⚠️ | Gelida › Alt Penedès | 3 |
| Forêt de Castellbell i el Vilar (5) ⚠️ | Castellbell i el Vilar › Bages | 3 |
| Forêt de Castellnou de Bages (43) ⚠️ | Navàs › Bages | 3 |
| Forêt de Guardiola de Berguedà (16) ⚠️ | Guardiola de Berguedà › Berguedà | 3 |
| Forêt de l'Espunyola (40) ⚠️ | l'Espunyola › Berguedà | 3 |
| Forêt de l'Espunyola (43) ⚠️ | l'Espunyola › Berguedà | 3 |
| Forêt de Montmajor (75) ⚠️ | Montmajor › Berguedà | 3 |
| Forêt de Vilanova del Camí (3) ⚠️ | Vilanova del Camí › Anoia | 3 |
| Forêt de la Pobla de Claramunt (9) ⚠️ | la Pobla de Claramunt › Anoia | 3 |
| Forêt de Calella (5) ⚠️ | Calella › Maresme | 3 |
| Forêt de Sant Pol de Mar (7) ⚠️ | Sant Pol de Mar › Maresme | 3 |
| Forêt de Sant Esteve Sesrovires (22) ⚠️ | Sant Esteve Sesrovires › Baix Llobregat | 3 |
| Forêt de el Papiol (4) ⚠️ | el Papiol › Baix Llobregat | 3 |
| Forêt de Vic (18) ⚠️ | Vic › Osona (Barcelone) | 3 |
| Forêt de Vic (22) ⚠️ | Vic › Osona (Barcelone) | 3 |
| Forêt de Vic (23) ⚠️ | Vic › Osona (Barcelone) | 3 |
| Forêt de Vallirana (30) ⚠️ | Vallirana › Baix Llobregat | 3 |
| Forêt de Cervelló (16) ⚠️ | Cervelló › Baix Llobregat | 3 |
| Forêt de Cervelló (18) ⚠️ | Cervelló › Baix Llobregat | 3 |
| Forêt de Rubí (73) ⚠️ | Rubí › Vallès Occidental | 3 |
| Forêt de Monistrol de Montserrat (33) ⚠️ | Monistrol de Montserrat › Bages | 3 |
| Forêt de Monistrol de Montserrat (35) ⚠️ | Monistrol de Montserrat › Bages | 3 |
| Forêt de Vacarisses (25) ⚠️ | Vacarisses › Vallès Occidental | 3 |
| Forêt de Vacarisses (26) ⚠️ | Vacarisses › Vallès Occidental | 3 |
| Forêt de Vacarisses (35) ⚠️ | Vacarisses › Vallès Occidental | 3 |
| Forêt de Castellbell i el Vilar (13) ⚠️ | Castellbell i el Vilar › Bages | 3 |
| Forêt de Vacarisses (43) ⚠️ | Vacarisses › Vallès Occidental | 3 |
| Forêt de Vacarisses (44) ⚠️ | Vacarisses › Vallès Occidental | 3 |
| Forêt de Esparreguera (15) ⚠️ | Esparreguera › Baix Llobregat | 3 |
| Forêt de Esparreguera (16) ⚠️ | Esparreguera › Baix Llobregat | 3 |
| Bosc del Puig ⚠️ | Castellbell i el Vilar › Bages | 3 |
| Forêt de Castellbell i el Vilar (23) ⚠️ | Castellbell i el Vilar › Bages | 3 |
| Forêt de Castellbell i el Vilar (30) ⚠️ | Castellbell i el Vilar › Bages | 3 |
| Forêt de Olesa de Montserrat (16) ⚠️ | Olesa de Montserrat › Baix Llobregat | 3 |
| Forêt de Marganell (9) ⚠️ | Marganell › Bages | 3 |
| Forêt de Marganell (21) ⚠️ | Marganell › Bages | 3 |
| Forêt de Marganell (22) ⚠️ | Marganell › Bages | 3 |
| Forêt de Marganell (24) ⚠️ | Marganell › Bages | 3 |
| Forêt de Òdena (33) ⚠️ | Òdena › Anoia | 3 |
| Forêt de Òdena (34) ⚠️ | Òdena › Anoia | 3 |
| Forêt de Castellolí (23) ⚠️ | Castellolí › Anoia | 3 |
| Forêt de Òdena (36) ⚠️ | Òdena › Anoia | 3 |
| Forêt de Castellbell i el Vilar (53) ⚠️ | Castellbell i el Vilar › Bages | 3 |
| Forêt de el Pont de Vilomara i Rocafort (6) ⚠️ | el Pont de Vilomara i Rocafort › Bages | 3 |
| Forêt de el Pont de Vilomara i Rocafort (19) ⚠️ | el Pont de Vilomara i Rocafort › Bages | 3 |
| Forêt de Moià (25) ⚠️ | Moià › Moianès | 3 |
| Forêt de Moià (32) ⚠️ | Moià › Moianès | 3 |
| Forêt de Sitges (25) ⚠️ | Sitges › Garraf | 3 |
| Forêt de Sitges (27) ⚠️ | Sitges › Garraf | 3 |
| Forêt de Sitges (45) ⚠️ | Sitges › Garraf | 3 |
| Forêt de Sitges (62) ⚠️ | Sitges › Garraf | 3 |
| Forêt de Gavà (66) ⚠️ | Gavà › Baix Llobregat | 3 |
| Forêt de Sitges (68) ⚠️ | Sitges › Garraf | 3 |
| Forêt de Castellgalí (14) ⚠️ | Castellgalí › Bages | 3 |
| Forêt de Castellgalí (18) ⚠️ | Castellgalí › Bages | 3 |
| Forêt de Marganell (26) ⚠️ | Marganell › Bages | 3 |
| Forêt de el Bruc (32) ⚠️ | el Bruc › Anoia | 3 |
| Forêt de Sant Salvador de Guardiola (52) ⚠️ | Sant Salvador de Guardiola › Bages | 3 |
| Forêt de Artés (21) ⚠️ | Artés › Bages | 3 |
| Forêt de Calders (28) ⚠️ | Calders › Moianès | 3 |
| Forêt de Artés (29) ⚠️ | Artés › Bages | 3 |
| Forêt de Artés (31) ⚠️ | Artés › Bages | 3 |
| Forêt de Avinyó (63) ⚠️ | Avinyó › Bages | 3 |
| Forêt de Avinyó (69) ⚠️ | Avinyó › Bages | 3 |
| Forêt de Artés (33) ⚠️ | Artés › Bages | 3 |
| Forêt de Avinyó (81) ⚠️ | Avinyó › Bages | 3 |
| Forêt de Avinyó (83) ⚠️ | Avinyó › Bages | 3 |
| Forêt de Calders (30) ⚠️ | Calders › Moianès | 3 |
| Forêt de Calders (37) ⚠️ | Calders › Moianès | 3 |
| Forêt de Cardedeu (23) ⚠️ | Sant Antoni de Vilamajor › Vallès Oriental | 3 |
| Forêt de Cardedeu (29) ⚠️ | Cardedeu › Vallès Oriental | 3 |
| Forêt de Llinars del Vallès (67) ⚠️ | Llinars del Vallès › Vallès Oriental | 3 |
| Forêt de Súria (16) ⚠️ | Súria › Bages | 3 |
| Parc El Mirador ⚠️ | les Franqueses del Vallès › Vallès Oriental | 3 |
| Parc Firal ⚠️ | Granollers › Vallès Oriental | 3 |
| Forêt de Vallromanes (11) ⚠️ | Vallromanes › Vallès Oriental | 3 |
| Forêt de Sallent (87) ⚠️ | Sallent › Bages | 3 |
| Forêt de Avinyó (98) ⚠️ | Avinyó › Bages | 3 |
| Forêt de Navàs (39) ⚠️ | Navàs › Bages | 3 |
| Forêt de Navàs (48) ⚠️ | Navàs › Bages | 3 |
| Forêt de Gaià (54) ⚠️ | Gaià › Bages | 3 |
| Forêt de Sant Vicenç de Castellet (22) ⚠️ | Sant Vicenç de Castellet › Bages | 3 |
| Forêt de Sant Esteve de Palautordera (5) ⚠️ | Sant Esteve de Palautordera › Vallès Oriental | 3 |
| Forêt de Santa Maria de Palautordera (25) ⚠️ | Santa Maria de Palautordera › Vallès Oriental | 3 |
| Forêt de la Nou de Berguedà (12) ⚠️ | la Nou de Berguedà › Berguedà | 3 |
| Forêt de la Nou de Berguedà (13) ⚠️ | la Nou de Berguedà › Berguedà | 3 |
| Forêt de Vilada (12) ⚠️ | Vilada › Berguedà | 3 |
| Forêt de Cercs (26) ⚠️ | Cercs › Berguedà | 3 |
| Forêt de Cercs (49) ⚠️ | Cercs › Berguedà | 3 |
| Forêt de Orís (7) ⚠️ | Orís › Osona (Barcelone) | 3 |
| Forêt de Guardiola de Berguedà (52) ⚠️ | Guardiola de Berguedà › Berguedà | 3 |
| Forêt de Vallcebre (20) ⚠️ | Vallcebre › Berguedà | 3 |
| Forêt de Monistrol de Calders (8) ⚠️ | Monistrol de Calders › Moianès | 3 |
| Forêt de Monistrol de Calders (19) ⚠️ | Monistrol de Calders › Moianès | 3 |
| Forêt de Talamanca (11) ⚠️ | Talamanca › Bages | 3 |
| Forêt de Navarcles (11) ⚠️ | Navarcles › Bages | 3 |
| Forêt de Calders (51) ⚠️ | Calders › Moianès | 3 |
| Forêt de Calders (62) ⚠️ | Calders › Moianès | 3 |
| Forêt de Sant Vicenç de Castellet (23) ⚠️ | Sant Vicenç de Castellet › Bages | 3 |
| Forêt de Sant Vicenç de Castellet (26) ⚠️ | Sant Vicenç de Castellet › Bages | 3 |
| Forêt de Sant Vicenç de Castellet (30) ⚠️ | Sant Vicenç de Castellet › Bages | 3 |
| Forêt de Castellgalí (22) ⚠️ | Castellgalí › Bages | 3 |
| Forêt de Aguilar de Segarra (36) ⚠️ | Aguilar de Segarra › Bages | 3 |
| Forêt de Aguilar de Segarra (39) ⚠️ | Aguilar de Segarra › Bages | 3 |
| Forêt de Sant Pere Sallavinera (9) ⚠️ | Sant Pere Sallavinera › Anoia | 3 |
| Forêt de Aguilar de Segarra (44) ⚠️ | Aguilar de Segarra › Bages | 3 |
| Forêt de Sant Pere Sallavinera (14) ⚠️ | Sant Pere Sallavinera › Anoia | 3 |
| Forêt de Sant Pere Sallavinera (17) ⚠️ | Sant Pere Sallavinera › Anoia | 3 |
| Forêt de Sant Pere Sallavinera (21) ⚠️ | Sant Pere Sallavinera › Anoia | 3 |
| Forêt de Sant Pere Sallavinera (28) ⚠️ | Sant Pere Sallavinera › Anoia | 3 |
| Forêt de Sant Pere Sallavinera (45) ⚠️ | Sant Pere Sallavinera › Anoia | 3 |
| Forêt de Sant Pere Sallavinera (47) ⚠️ | Sant Pere Sallavinera › Anoia | 3 |
| Forêt de Sant Pere Sallavinera (53) ⚠️ | Calonge de Segarra › Anoia | 3 |
| Forêt de els Prats de Rei (30) ⚠️ | els Prats de Rei › Anoia | 3 |
| Forêt de Castellfollit del Boix (27) ⚠️ | Castellfollit del Boix › Bages | 3 |
| Forêt de Sant Salvador de Guardiola (95) ⚠️ | Sant Salvador de Guardiola › Bages | 3 |
| Forêt de Sant Salvador de Guardiola (104) ⚠️ | Sant Salvador de Guardiola › Bages | 3 |
| Forêt de Sant Salvador de Guardiola (111) ⚠️ | Sant Salvador de Guardiola › Bages | 3 |
| Forêt de el Bruc (37) ⚠️ | el Bruc › Anoia | 3 |
| Forêt de Marganell (28) ⚠️ | Marganell › Bages | 3 |
| Forêt de Castellgalí (25) ⚠️ | Castellgalí › Bages | 3 |
| Forêt de Castellgalí (28) ⚠️ | Castellgalí › Bages | 3 |
| Forêt de Vacarisses (55) ⚠️ | Vacarisses › Vallès Occidental | 3 |
| Forêt de Vacarisses (64) ⚠️ | Vacarisses › Vallès Occidental | 3 |
| Forêt de Vacarisses (69) ⚠️ | Esparreguera › Baix Llobregat | 3 |
| Forêt de Olesa de Montserrat (27) ⚠️ | Olesa de Montserrat › Baix Llobregat | 3 |
| Forêt de Olesa de Montserrat (33) ⚠️ | Olesa de Montserrat › Baix Llobregat | 3 |
| Forêt de Olesa de Montserrat (39) ⚠️ | Olesa de Montserrat › Baix Llobregat | 3 |
| Forêt de Abrera (14) ⚠️ | Abrera › Baix Llobregat | 3 |
| Forêt de Abrera (16) ⚠️ | Abrera › Baix Llobregat | 3 |
| Bois de Abrera (2) ⚠️ | Abrera › Baix Llobregat | 3 |
| Bois de Olesa de Montserrat (3) ⚠️ | Olesa de Montserrat › Baix Llobregat | 3 |
| Forêt de Abrera (18) ⚠️ | Abrera › Baix Llobregat | 3 |
| Forêt de Martorell (12) ⚠️ | Martorell › Baix Llobregat | 3 |
| Forêt de Castellbisbal (26) ⚠️ | Castellbisbal › Vallès Occidental | 3 |
| Forêt de Castellbisbal (27) ⚠️ | Castellbisbal › Vallès Occidental | 3 |
| Forêt de Martorell (18) ⚠️ | Martorell › Baix Llobregat | 3 |
| Parc del Riu Anoia ⚠️ | Martorell › Baix Llobregat | 3 |
| Forêt de Castellgalí (43) ⚠️ | Castellgalí › Bages | 3 |
| Forêt de Castellgalí (49) ⚠️ | Castellgalí › Bages | 3 |
| Forêt de Sant Vicenç de Castellet (52) ⚠️ | Sant Vicenç de Castellet › Bages | 3 |
| Forêt de Navàs (61) ⚠️ | Navàs › Bages | 3 |
| Forêt de Navàs (69) ⚠️ | Navàs › Bages | 3 |
| Forêt de Navàs (90) ⚠️ | Navàs › Bages | 3 |
| Forêt de Viver i Serrateix (51) ⚠️ | Viver i Serrateix › Berguedà | 3 |
| Forêt de Viver i Serrateix (55) ⚠️ | Viver i Serrateix › Berguedà | 3 |
| Forêt de Viver i Serrateix (56) ⚠️ | Viver i Serrateix › Berguedà | 3 |
| Forêt de Viver i Serrateix (59) ⚠️ | Viver i Serrateix › Berguedà | 3 |
| Forêt de Puig-reig (71) ⚠️ | Puig-reig › Berguedà | 3 |
| Forêt de Puig-reig (75) ⚠️ | Puig-reig › Berguedà | 3 |
| Forêt de Puig-reig (78) ⚠️ | Puig-reig › Berguedà | 3 |
| Forêt de Sagàs (12) ⚠️ | Sagàs › Berguedà | 3 |
| Forêt de Olvan (18) ⚠️ | Olvan › Berguedà | 3 |
| Forêt de Sagàs (17) ⚠️ | Sagàs › Berguedà | 3 |
| Forêt de Sagàs (18) ⚠️ | Sagàs › Berguedà | 3 |
| Forêt de Sagàs (20) ⚠️ | Sagàs › Berguedà | 3 |
| Forêt de Avià (30) ⚠️ | Avià › Berguedà | 3 |
| Forêt de l'Espunyola (55) ⚠️ | l'Espunyola › Berguedà | 3 |
| Forêt de l'Espunyola (61) ⚠️ | l'Espunyola › Berguedà | 3 |
| Forêt de Avià (40) ⚠️ | Avià › Berguedà | 3 |
| Forêt de Avià (42) ⚠️ | Avià › Berguedà | 3 |
| Forêt de Montmajor (79) ⚠️ | Montmajor › Berguedà | 3 |
| Forêt de Montmajor (82) ⚠️ | Montmajor › Berguedà | 3 |
| Forêt de Montmajor (94) ⚠️ | Montmajor › Berguedà | 3 |
| Forêt de Cardona (60) ⚠️ | Cardona › Bages | 3 |
| Forêt de Montmajor (103) ⚠️ | Montmajor › Berguedà | 3 |
| Forêt de Navàs (101) ⚠️ | Navàs › Bages | 3 |
| Forêt de Navàs (104) ⚠️ | Navàs › Bages | 3 |
| Forêt de Sant Mateu de Bages (42) ⚠️ | Sant Mateu de Bages › Bages | 3 |
| Forêt de Sant Mateu de Bages (50) ⚠️ | Sant Mateu de Bages › Bages | 3 |
| Forêt de Navàs (108) ⚠️ | Navàs › Bages | 3 |
| Forêt de Sant Mateu de Bages (53) ⚠️ | Sant Mateu de Bages › Bages | 3 |
| Forêt de Navàs (111) ⚠️ | Navàs › Bages | 3 |
| Forêt de Navàs (117) ⚠️ | Navàs › Bages | 3 |
| Forêt de Navàs (120) ⚠️ | Navàs › Bages | 3 |
| Forêt de Navàs (121) ⚠️ | Navàs › Bages | 3 |
| Forêt de Súria (25) ⚠️ | Súria › Bages | 3 |
| Forêt de Viver i Serrateix (65) ⚠️ | Viver i Serrateix › Berguedà | 3 |
| Forêt de Viver i Serrateix (79) ⚠️ | Viver i Serrateix › Berguedà | 3 |
| Forêt de Viver i Serrateix (87) ⚠️ | Viver i Serrateix › Berguedà | 3 |
| Forêt de Montmajor (120) ⚠️ | Montmajor › Berguedà | 3 |
| Forêt de Gaià (58) ⚠️ | Gaià › Bages | 3 |
| Forêt de Avinyó (108) ⚠️ | Avinyó › Bages | 3 |
| Forêt de Santa Maria de Merlès (34) ⚠️ | Santa Maria de Merlès › Berguedà | 3 |
| Forêt de Santa Maria de Merlès (45) ⚠️ | Santa Maria de Merlès › Berguedà | 3 |
| Forêt de Santa Maria de Merlès (47) ⚠️ | Santa Maria de Merlès › Berguedà | 3 |
| Forêt de Santa Maria de Merlès (49) ⚠️ | Santa Maria de Merlès › Berguedà | 3 |
| Forêt de Santa Maria de Merlès (55) ⚠️ | Santa Maria de Merlès › Berguedà | 3 |
| Forêt de Lluçà (7) ⚠️ | Lluçà › Lluçanès | 3 |
| Forêt de Vic (28) ⚠️ | Vic › Osona (Barcelone) | 3 |
| Forêt de Santa Eulàlia de Riuprimer (4) ⚠️ | Santa Eulàlia de Riuprimer › Osona (Barcelone) | 3 |
| Forêt de Sant Cugat del Vallès (123) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 3 |
| Bois de Barcelona (105) ⚠️ | Barcelona › Barcelonès | 3 |
| Bois de Barcelona (110) ⚠️ | Barcelona › Barcelonès | 3 |
| Bois de Barcelona (111) ⚠️ | Barcelona › Barcelonès | 3 |
| Forêt de Vilanova i la Geltrú (26) ⚠️ | Vilanova i la Geltrú › Garraf | 3 |
| Forêt de Castellgalí (64) ⚠️ | Castellgalí › Bages | 3 |
| Bois de Llinars del Vallès (34) ⚠️ | Llinars del Vallès › Vallès Oriental | 3 |
| Bosc de Can Pla ⚠️ | Vilanova del Vallès › Vallès Oriental | 3 |
| Bois de Viladecavalls (13) ⚠️ | Viladecavalls › Vallès Occidental | 3 |
| Forêt de Jorba (20) ⚠️ | Jorba › Anoia | 3 |
| Forêt de Jorba (25) ⚠️ | Jorba › Anoia | 3 |
| Forêt de Jorba (32) ⚠️ | Jorba › Anoia | 3 |
| Parc de Puigcornet ⚠️ | Igualada › Anoia | 3 |
| Forêt de la Pobla de Claramunt (14) ⚠️ | la Pobla de Claramunt › Anoia | 3 |
| Forêt de la Pobla de Claramunt (16) ⚠️ | la Pobla de Claramunt › Anoia | 3 |
| Forêt de Vilanova del Camí (8) ⚠️ | Vilanova del Camí › Anoia | 3 |
| Forêt de Santa Margarida de Montbui (19) ⚠️ | Santa Margarida de Montbui › Anoia | 3 |
| Forêt de Jorba (41) ⚠️ | Jorba › Anoia | 3 |
| Forêt de Cubelles (18) ⚠️ | Cubelles › Garraf | 3 |
| Forêt de Cubelles (22) ⚠️ | Cubelles › Garraf | 3 |
| Forêt de Cubelles (24) ⚠️ | Cubelles › Garraf | 3 |
| Forêt de Olivella (59) ⚠️ | Olivella › Garraf | 3 |
| Forêt de Olivella (86) ⚠️ | Begues › Baix Llobregat | 3 |
| Forêt de Begues (44) ⚠️ | Begues › Baix Llobregat | 3 |
| Forêt de Begues (53) ⚠️ | Begues › Baix Llobregat | 3 |
| Forêt de Begues (56) ⚠️ | Begues › Baix Llobregat | 3 |
| Forêt de Begues (57) ⚠️ | Begues › Baix Llobregat | 3 |
| Forêt de Begues (59) ⚠️ | Begues › Baix Llobregat | 3 |
| Forêt de Begues (70) ⚠️ | Begues › Baix Llobregat | 3 |
| Forêt de Begues (71) ⚠️ | Begues › Baix Llobregat | 3 |
| Forêt de Begues (75) ⚠️ | Begues › Baix Llobregat | 3 |
| Forêt de Begues (77) ⚠️ | Begues › Baix Llobregat | 3 |
| Forêt de Olesa de Bonesvalls (43) ⚠️ | Olesa de Bonesvalls › Alt Penedès | 3 |
| Forêt de Olivella (105) ⚠️ | Olivella › Garraf | 3 |
| Forêt de Avinyonet del Penedès (60) ⚠️ | Avinyonet del Penedès › Alt Penedès | 3 |
| Forêt de Sant Pere de Ribes (104) ⚠️ | Sant Pere de Ribes › Garraf | 3 |
| Forêt de Cubelles (28) ⚠️ | Cubelles › Garraf | 3 |
| Forêt de Cubelles (31) ⚠️ | Vilanova i la Geltrú › Garraf | 3 |
| Forêt de Castellet i la Gornal (86) ⚠️ | Castellet i la Gornal › Alt Penedès | 3 |
| Forêt de Canyelles (8) ⚠️ | Olèrdola › Alt Penedès | 3 |
| Forêt de Vilanova i la Geltrú (42) ⚠️ | Vilanova i la Geltrú › Garraf | 3 |
| Forêt de Vilanova i la Geltrú (61) ⚠️ | Vilanova i la Geltrú › Garraf | 3 |
| Forêt de Vilanova i la Geltrú (70) ⚠️ | Vilanova i la Geltrú › Garraf | 3 |
| Forêt de Avinyonet del Penedès (65) ⚠️ | Avinyonet del Penedès › Alt Penedès | 3 |
| Forêt de Pallejà (7) ⚠️ | Pallejà › Baix Llobregat | 3 |
| Forêt de Sant Julià de Cerdanyola (8) ⚠️ | Sant Julià de Cerdanyola › Berguedà | 3 |
| Bois de Viladecavalls (14) ⚠️ | Viladecavalls › Vallès Occidental | 3 |
| Forêt de Ullastrell (4) ⚠️ | Ullastrell › Vallès Occidental | 3 |
| Forêt de Guardiola de Berguedà (61) ⚠️ | Guardiola de Berguedà › Berguedà | 3 |
| Forêt de Gisclareny (20) ⚠️ | Gisclareny › Berguedà | 3 |
| Forêt de Fígols (14) ⚠️ | Fígols › Berguedà | 3 |
| Forêt de Saldes (28) ⚠️ | Saldes › Berguedà | 3 |
| Forêt de Navàs (142) ⚠️ | Navàs › Bages | 3 |
| Forêt de Santa Maria de Merlès (72) ⚠️ | Santa Maria de Merlès › Berguedà | 3 |
| Forêt de Santa Maria de Merlès (75) ⚠️ | Santa Maria de Merlès › Berguedà | 3 |
| Forêt de Vilada (17) ⚠️ | Vilada › Berguedà | 3 |
| Forêt de Sant Jaume de Frontanyà (19) ⚠️ | Sant Jaume de Frontanyà › Berguedà | 3 |
| Forêt de Borredà (44) ⚠️ | Borredà › Berguedà | 3 |
| Forêt de Borredà (48) ⚠️ | Borredà › Berguedà | 3 |
| Forêt de Borredà (56) ⚠️ | Borredà › Berguedà | 3 |
| Forêt de Sagàs (24) ⚠️ | Sagàs › Berguedà | 3 |
| Forêt de Avinyó (114) ⚠️ | Avinyó › Bages | 3 |
| Forêt de Santa Maria de Merlès (84) ⚠️ | Santa Maria de Merlès › Berguedà | 3 |
| Forêt de Santa Maria de Merlès (89) ⚠️ | Santa Maria de Merlès › Berguedà | 3 |
| Forêt de Santa Maria de Merlès (96) ⚠️ | Santa Maria de Merlès › Berguedà | 3 |
| Forêt de Santa Maria de Merlès (105) ⚠️ | Santa Maria de Merlès › Berguedà | 3 |
| Forêt de Santa Maria de Merlès (111) ⚠️ | Santa Maria de Merlès › Berguedà | 3 |
| Forêt de Santa Maria de Merlès (115) ⚠️ | Santa Maria de Merlès › Berguedà | 3 |
| Forêt de Santa Maria de Merlès (121) ⚠️ | Santa Maria de Merlès › Berguedà | 3 |
| Forêt de Aguilar de Segarra (49) ⚠️ | Aguilar de Segarra › Bages | 3 |
| Bois de Castellar del Vallès (2) ⚠️ | Castellar del Vallès › Vallès Occidental | 3 |
| Forêt de Rupit i Pruit (24) ⚠️ | Rupit i Pruit › Osona (Barcelone) | 3 |
| Forêt de Avià (56) ⚠️ | Avià › Berguedà | 3 |
| Forêt de la Quar (22) ⚠️ | la Quar › Berguedà | 3 |
| Forêt de Collbató (14) ⚠️ | Collbató › Baix Llobregat | 3 |
| Forêt de Monistrol de Calders (31) ⚠️ | Monistrol de Calders › Moianès | 3 |
| Forêt de Monistrol de Calders (40) ⚠️ | Monistrol de Calders › Moianès | 3 |
| Forêt de Santa Maria d'Oló (57) ⚠️ | Santa Maria d'Oló › Moianès | 3 |
| Forêt de Granera (22) ⚠️ | Granera › Moianès | 3 |
| Forêt de Abrera (30) ⚠️ | Abrera › Baix Llobregat | 3 |
| Forêt de Taradell (8) ⚠️ | Taradell › Osona (Barcelone) | 3 |
| Forêt de Taradell (11) ⚠️ | Tona › Osona (Barcelone) | 3 |
| Forêt de el Brull (23) ⚠️ | el Brull › Osona (Barcelone) | 3 |
| Forêt de Tagamanent (24) ⚠️ | Tagamanent › Vallès Oriental | 3 |
| Forêt de Sant Martí de Centelles (54) ⚠️ | Sant Martí de Centelles › Osona (Barcelone) | 3 |
| Forêt de Centelles (16) ⚠️ | Centelles › Osona (Barcelone) | 3 |
| Forêt de Centelles (25) ⚠️ | Centelles › Osona (Barcelone) | 3 |
| Forêt de Centelles (26) ⚠️ | Centelles › Osona (Barcelone) | 3 |
| Forêt de Centelles (28) ⚠️ | Centelles › Osona (Barcelone) | 3 |
| Forêt de l'Estany (7) ⚠️ | l'Estany › Moianès | 3 |
| Forêt de Cànoves i Samalús (41) ⚠️ | Cànoves i Samalús › Vallès Oriental | 3 |
| Forêt de Cànoves i Samalús (43) ⚠️ | Cànoves i Samalús › Vallès Oriental | 3 |
| Forêt de el Brull (29) ⚠️ | el Brull › Osona (Barcelone) | 3 |
| Forêt de el Brull (31) ⚠️ | el Brull › Osona (Barcelone) | 3 |
| Forêt de Sant Pere de Vilamajor (89) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 3 |
| Forêt de Fogars de Montclús (21) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 3 |
| Forêt de Figaró-Montmany (7) ⚠️ | Figaró-Montmany › Vallès Oriental | 3 |
| Forêt de Bigues i Riells del Fai (18) ⚠️ | Bigues i Riells del Fai › Vallès Oriental | 3 |
| Forêt de Sant Quirze Safaja (24) ⚠️ | Sant Quirze Safaja › Moianès | 3 |
| Forêt de Bigues i Riells del Fai (20) ⚠️ | Bigues i Riells del Fai › Vallès Oriental | 3 |
| Forêt de Bigues i Riells del Fai (23) ⚠️ | Bigues i Riells del Fai › Vallès Oriental | 3 |
| Forêt de Bigues i Riells del Fai (28) ⚠️ | Bigues i Riells del Fai › Vallès Oriental | 3 |
| Forêt de Bigues i Riells del Fai (31) ⚠️ | Sant Feliu de Codines › Vallès Oriental | 3 |
| Forêt de Bigues i Riells del Fai (34) ⚠️ | Bigues i Riells del Fai › Vallès Oriental | 3 |
| Forêt de Santa Maria d'Oló (79) ⚠️ | Santa Maria d'Oló › Moianès | 3 |
| Forêt de Santa Eulàlia de Riuprimer (16) ⚠️ | Santa Eulàlia de Riuprimer › Osona (Barcelone) | 3 |
| Forêt de Santa Eulàlia de Riuprimer (20) ⚠️ | Santa Eulàlia de Riuprimer › Osona (Barcelone) | 3 |
| Forêt de Santa Eulàlia de Riuprimer (22) ⚠️ | Santa Eulàlia de Riuprimer › Osona (Barcelone) | 3 |
| Forêt de Santa Eulàlia de Riuprimer (24) ⚠️ | Santa Eulàlia de Riuprimer › Osona (Barcelone) | 3 |
| Forêt de Muntanyola (27) ⚠️ | Muntanyola › Osona (Barcelone) | 3 |
| Forêt de Oristà (131) ⚠️ | Oristà › Lluçanès | 3 |
| Forêt de Oristà (134) ⚠️ | Oristà › Lluçanès | 3 |
| Forêt de Oristà (135) ⚠️ | Oristà › Lluçanès | 3 |
| Forêt de Oristà (136) ⚠️ | Oristà › Lluçanès | 3 |
| Forêt de Oristà (141) ⚠️ | Oristà › Lluçanès | 3 |
| Forêt de Sant Feliu Sasserra (17) ⚠️ | Sant Feliu Sasserra › Bages | 3 |
| Forêt de Sant Feliu Sasserra (18) ⚠️ | Sant Feliu Sasserra › Bages | 3 |
| Forêt de Sant Mateu de Bages (54) ⚠️ | Sant Mateu de Bages › Bages | 3 |
| Forêt de Sant Mateu de Bages (61) ⚠️ | Sant Mateu de Bages › Bages | 3 |
| Forêt de Navàs (158) ⚠️ | Navàs › Bages | 3 |
| Forêt de Navàs (159) ⚠️ | Navàs › Bages | 3 |
| Forêt de Cardona (69) ⚠️ | Cardona › Bages | 3 |
| Forêt de Cardona (74) ⚠️ | Cardona › Bages | 3 |
| Forêt de Cardona (75) ⚠️ | Cardona › Bages | 3 |
| Forêt de Cardona (89) ⚠️ | Cardona › Bages | 3 |
| Forêt de Cardona (96) ⚠️ | Cardona › Bages | 3 |
| Forêt de Sant Mateu de Bages (78) ⚠️ | Sant Mateu de Bages › Bages | 3 |
| Forêt de Sant Mateu de Bages (79) ⚠️ | Sant Mateu de Bages › Bages | 3 |
| Forêt de Sant Mateu de Bages (93) ⚠️ | Sant Mateu de Bages › Bages | 3 |
| Forêt de Sant Pere de Vilamajor (90) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 3 |
| Forêt de Sant Pere de Vilamajor (91) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 3 |
| Forêt de Guardiola de Berguedà (66) ⚠️ | Guardiola de Berguedà › Berguedà | 3 |
| Forêt de Santa Maria de Merlès (127) ⚠️ | Santa Maria de Merlès › Berguedà | 3 |
| Forêt de Santa Maria de Merlès (135) ⚠️ | Sagàs › Berguedà | 3 |
| Forêt de Santa Maria de Merlès (138) ⚠️ | Santa Maria de Merlès › Berguedà | 3 |
| Forêt de Mataró (3) ⚠️ | Mataró › Maresme | 3 |
| Forêt de Argentona (3) ⚠️ | Argentona › Maresme | 3 |
| Forêt de Dosrius (11) ⚠️ | Dosrius › Maresme | 3 |
| Forêt de Dosrius (17) ⚠️ | Dosrius › Maresme | 3 |
| Forêt de Dosrius (19) ⚠️ | Dosrius › Maresme | 3 |
| Forêt de Balenyà (15) ⚠️ | Balenyà › Osona (Barcelone) | 3 |
| Forêt de Tona (8) ⚠️ | Tona › Osona (Barcelone) | 3 |
| Forêt de Collsuspina (9) ⚠️ | Collsuspina › Moianès | 3 |
| Forêt de Balenyà (23) ⚠️ | Balenyà › Osona (Barcelone) | 3 |
| Forêt de Tona (24) ⚠️ | Tona › Osona (Barcelone) | 3 |
| Forêt de Taradell (13) ⚠️ | Taradell › Osona (Barcelone) | 3 |
| Forêt de Seva (24) ⚠️ | Seva › Osona (Barcelone) | 3 |
| Forêt de Malla (10) ⚠️ | Malla › Osona (Barcelone) | 3 |
| Forêt de Taradell (18) ⚠️ | Taradell › Osona (Barcelone) | 3 |
| Forêt de el Bruc (47) ⚠️ | el Bruc › Anoia | 3 |
| Forêt de Gallifa (6) ⚠️ | Gallifa › Vallès Occidental | 3 |
| Forêt de Saldes (42) ⚠️ | Saldes › Berguedà | 3 |
| Forêt de Sagàs (47) ⚠️ | Sagàs › Berguedà | 3 |
| Forêt de Gisclareny (36) ⚠️ | Gisclareny › Berguedà | 3 |
| Forêt de Bagà (48) ⚠️ | Bagà › Berguedà | 3 |
| Forêt de Guardiola de Berguedà (85) ⚠️ | Guardiola de Berguedà › Berguedà | 3 |
| Forêt de Guardiola de Berguedà (93) ⚠️ | Guardiola de Berguedà › Berguedà | 3 |
| Forêt de Bagà (58) ⚠️ | Bagà › Berguedà | 3 |
| Forêt de Guardiola de Berguedà (104) ⚠️ | Guardiola de Berguedà › Berguedà | 3 |
| Forêt de Guardiola de Berguedà (111) ⚠️ | Guardiola de Berguedà › Berguedà | 3 |
| Forêt de Bagà (68) ⚠️ | Bagà › Berguedà | 3 |
| Forêt de Vallcebre (28) ⚠️ | Vallcebre › Berguedà | 3 |
| Forêt de Capolat (36) ⚠️ | Capolat › Berguedà | 3 |
| Forêt de Castellar del Riu (28) ⚠️ | Castellar del Riu › Berguedà | 3 |
| Forêt de Capolat (45) ⚠️ | Capolat › Berguedà | 3 |
| Forêt de Fígols (19) ⚠️ | Fígols › Berguedà | 3 |
| Forêt de Prats de Lluçanès (14) ⚠️ | Prats de Lluçanès › Lluçanès | 3 |
| Forêt de Prats de Lluçanès (23) ⚠️ | Prats de Lluçanès › Lluçanès | 3 |
| Forêt de Prats de Lluçanès (27) ⚠️ | Prats de Lluçanès › Lluçanès | 3 |
| Forêt de la Quar (35) ⚠️ | la Quar › Berguedà | 3 |
| Forêt de la Quar (36) ⚠️ | la Quar › Berguedà | 3 |
| Forêt de Lluçà (46) ⚠️ | la Quar › Berguedà | 3 |
| Forêt de Lluçà (49) ⚠️ | Lluçà › Lluçanès | 3 |
| Forêt de Borredà (94) ⚠️ | Borredà › Berguedà | 3 |
| Forêt de Borredà (122) ⚠️ | Borredà › Berguedà | 3 |
| Forêt de la Pobla de Lillet (43) ⚠️ | la Pobla de Lillet › Berguedà | 3 |
| Forêt de la Pobla de Lillet (60) ⚠️ | la Pobla de Lillet › Berguedà | 3 |
| Forêt de la Pobla de Lillet (61) ⚠️ | la Pobla de Lillet › Berguedà | 3 |
| Forêt de Saldes (78) ⚠️ | Saldes › Berguedà | 3 |
| Forêt de Saldes (82) ⚠️ | Saldes › Berguedà | 3 |
| Forêt de Castellar del Riu (69) ⚠️ | Castellar del Riu › Berguedà | 3 |
| Forêt de Castellar del Riu (70) ⚠️ | Castellar del Riu › Berguedà | 3 |
| Forêt de Cercs (65) ⚠️ | Cercs › Berguedà | 3 |
| Forêt de Bagà (70) ⚠️ | Bagà › Berguedà | 3 |
| Forêt de Bagà (76) ⚠️ | Bagà › Berguedà | 3 |
| Forêt de Saldes (114) ⚠️ | Saldes › Berguedà | 3 |
| Forêt de Vallcebre (46) ⚠️ | Vallcebre › Berguedà | 3 |
| Forêt de Montesquiu (8) ⚠️ | Montesquiu › Osona (Barcelone) | 3 |
| Forêt de Orís (10) ⚠️ | Orís › Osona (Barcelone) | 3 |
| Forêt de Orís (14) ⚠️ | Orís › Osona (Barcelone) | 3 |
| Forêt de Sant Vicenç de Torelló (5) ⚠️ | Sant Vicenç de Torelló › Osona (Barcelone) | 3 |
| Forêt de Vilanova de Sau (46) ⚠️ | Vilanova de Sau › Osona (Barcelone) | 3 |
| Forêt de Vilanova de Sau (48) ⚠️ | Vilanova de Sau › Osona (Barcelone) | 3 |
| Forêt de Vilanova de Sau (53) ⚠️ | Vilanova de Sau › Osona (Barcelone) | 3 |
| Forêt de Gurb (22) ⚠️ | Gurb › Osona (Barcelone) | 3 |
| Forêt de Folgueroles (2) ⚠️ | Folgueroles › Osona (Barcelone) | 3 |
| Forêt de Sant Martí Sarroca (30) ⚠️ | Sant Martí Sarroca › Alt Penedès | 3 |
| Forêt de Vilanova de Sau (55) ⚠️ | Vilanova de Sau › Osona (Barcelone) | 3 |
| Forêt de Vilanova de Sau (56) ⚠️ | Vilanova de Sau › Osona (Barcelone) | 3 |
| Forêt de Castell de l'Areny (30) ⚠️ | Castell de l'Areny › Berguedà | 3 |
| Forêt de Tordera (55) ⚠️ | Tordera › Maresme | 3 |
| Forêt de Tordera (80) ⚠️ | Tordera › Maresme | 3 |
| Forêt de Tordera (81) ⚠️ | Tordera › Maresme | 3 |
| Forêt de Fogars de la Selva (23) ⚠️ | Fogars de la Selva › la Selva (Barcelone) | 3 |
| Forêt de Barcelona (63) ⚠️ | Barcelona › Barcelonès | 3 |
| Forêt de Sabadell (82) ⚠️ | Sabadell › Vallès Occidental | 3 |
| Forêt de Montornès del Vallès (14) ⚠️ | Montornès del Vallès › Vallès Oriental | 3 |
| Forêt de Martorelles ⚠️ | Martorelles › Vallès Oriental | 3 |
| Forêt de Vilanova del Vallès (18) ⚠️ | Vilanova del Vallès › Vallès Oriental | 3 |
| Forêt de Vilanova del Vallès (19) ⚠️ | Vilanova del Vallès › Vallès Oriental | 3 |
| Forêt de Vilanova del Vallès (20) ⚠️ | Vilanova del Vallès › Vallès Oriental | 3 |
| Forêt de la Roca del Vallès (17) ⚠️ | la Roca del Vallès › Vallès Oriental | 3 |
| Forêt de la Llagosta (3) ⚠️ | la Llagosta › Vallès Oriental | 3 |
| Forêt de Santa Coloma de Gramenet (8) ⚠️ | Santa Coloma de Gramenet › Barcelonès | 3 |
| Forêt de Santa Coloma de Gramenet (10) ⚠️ | Santa Coloma de Gramenet › Barcelonès | 3 |
| Forêt de Sant Fost de Campsentelles (12) ⚠️ | Sant Fost de Campsentelles › Vallès Oriental | 3 |
| Forêt de Vallromanes (17) ⚠️ | Vallromanes › Vallès Oriental | 3 |
| Forêt de Cubelles (35) ⚠️ | Cubelles › Garraf | 3 |
| Forêt de Saldes (132) ⚠️ | Saldes › Berguedà | 3 |
| Forêt de Piera (26) ⚠️ | Piera › Anoia | 3 |
| Forêt de Piera (31) ⚠️ | Piera › Anoia | 3 |
| Forêt de Piera (33) ⚠️ | Piera › Anoia | 3 |
| Forêt de el Bruc (48) ⚠️ | el Bruc › Anoia | 3 |
| Forêt de Castellolí (35) ⚠️ | Castellolí › Anoia | 3 |
| Forêt de Sant Martí de Tous (29) ⚠️ | Sant Martí de Tous › Anoia | 3 |
| Forêt de Santa Margarida de Montbui (25) ⚠️ | Santa Margarida de Montbui › Anoia | 3 |
| Forêt de Santa Margarida de Montbui (31) ⚠️ | Santa Margarida de Montbui › Anoia | 3 |
| Forêt de Santa Margarida de Montbui (39) ⚠️ | Santa Margarida de Montbui › Anoia | 3 |
| Forêt de Argençola (32) ⚠️ | Argençola › Anoia | 3 |
| Forêt de Sant Martí de Tous (36) ⚠️ | Sant Martí de Tous › Anoia | 3 |
| Forêt de Jorba (44) ⚠️ | Jorba › Anoia | 3 |
| Forêt de Sant Martí de Tous (43) ⚠️ | Sant Martí de Tous › Anoia | 3 |
| Forêt de Sitges (92) ⚠️ | Sitges › Garraf | 3 |
| Forêt de Moià (41) ⚠️ | Moià › Moianès | 3 |
| Forêt de Moià (42) ⚠️ | Moià › Moianès | 3 |
| Forêt de Moià (54) ⚠️ | Moià › Moianès | 3 |
| Forêt de Moià (61) ⚠️ | Moià › Moianès | 3 |
| Forêt de Sant Feliu Sasserra (28) ⚠️ | Sant Feliu Sasserra › Bages | 3 |
| Forêt de Sant Feliu Sasserra (37) ⚠️ | Sant Feliu Sasserra › Bages | 3 |
| Forêt de Castellar de n'Hug (26) ⚠️ | Castellar de n'Hug › Berguedà | 3 |
| Forêt de Oristà (167) ⚠️ | Oristà › Lluçanès | 3 |
| Forêt de Sant Feliu Sasserra (40) ⚠️ | Sant Feliu Sasserra › Bages | 3 |
| Forêt de Santa Margarida de Montbui (45) ⚠️ | Santa Margarida de Montbui › Anoia | 3 |
| Forêt de Jorba (51) ⚠️ | Jorba › Anoia | 3 |
| Forêt de Òdena (68) ⚠️ | Òdena › Anoia | 3 |
| Forêt de Òdena (74) ⚠️ | Òdena › Anoia | 3 |
| Forêt de Piera (38) ⚠️ | Piera › Anoia | 3 |
| Parc de Can Barra ⚠️ | Sant Quirze del Vallès › Vallès Occidental | 3 |
| Forêt de Viladecavalls (17) ⚠️ | Viladecavalls › Vallès Occidental | 3 |
| Forêt de Viladecavalls (19) ⚠️ | Viladecavalls › Vallès Occidental | 3 |
| Forêt de Martorell (36) ⚠️ | Martorell › Baix Llobregat | 3 |
| Forêt de Castellví de Rosanes (10) ⚠️ | Castellví de Rosanes › Baix Llobregat | 3 |
| Forêt de Terrassa (83) ⚠️ | Terrassa › Vallès Occidental | 3 |
| Forêt de Martorell (44) ⚠️ | Martorell › Baix Llobregat | 3 |
| Forêt de Martorell (48) ⚠️ | Martorell › Baix Llobregat | 3 |
| Forêt de Sant Esteve Sesrovires (27) ⚠️ | Sant Esteve Sesrovires › Baix Llobregat | 3 |
| Forêt de Esparreguera (46) ⚠️ | Esparreguera › Baix Llobregat | 3 |
| Forêt de Gelida (37) ⚠️ | Gelida › Alt Penedès | 3 |
| Forêt de la Pobla de Claramunt (24) ⚠️ | la Pobla de Claramunt › Anoia | 3 |
| Forêt de la Torre de Claramunt (10) ⚠️ | la Pobla de Claramunt › Anoia | 3 |
| Forêt de Mediona (21) ⚠️ | Mediona › Alt Penedès | 3 |
| Forêt de Mediona (29) ⚠️ | Mediona › Alt Penedès | 3 |
| Forêt de Mediona (30) ⚠️ | Mediona › Alt Penedès | 3 |
| Forêt de Piera (41) ⚠️ | Piera › Anoia | 3 |
| Forêt de Piera (43) ⚠️ | Piera › Anoia | 3 |
| Forêt de Piera (46) ⚠️ | Piera › Anoia | 3 |
| Forêt de Piera (49) ⚠️ | Piera › Anoia | 3 |
| Forêt de Mediona (35) ⚠️ | Mediona › Alt Penedès | 3 |
| Forêt de Mediona (38) ⚠️ | Mediona › Alt Penedès | 3 |
| Forêt de la Torre de Claramunt (23) ⚠️ | la Torre de Claramunt › Anoia | 3 |
| Forêt de Mediona (48) ⚠️ | Mediona › Alt Penedès | 3 |
| Forêt de Mediona (49) ⚠️ | Mediona › Alt Penedès | 3 |
| Forêt de la Llacuna (11) ⚠️ | la Llacuna › Anoia | 3 |
| Forêt de Cabrera d'Anoia (28) ⚠️ | Cabrera d'Anoia › Anoia | 3 |
| Forêt de Mediona (69) ⚠️ | Mediona › Alt Penedès | 3 |
| Forêt de Torrelavit (38) ⚠️ | Torrelavit › Alt Penedès | 3 |
| Forêt de Torrelavit (40) ⚠️ | Torrelavit › Alt Penedès | 3 |
| Forêt de Torrelavit (42) ⚠️ | Torrelavit › Alt Penedès | 3 |
| Forêt de Piera (64) ⚠️ | Piera › Anoia | 3 |
| Forêt de Piera (69) ⚠️ | Piera › Anoia | 3 |
| Forêt de Piera (77) ⚠️ | Piera › Anoia | 3 |
| Forêt de Sant Pere de Riudebitlles (8) ⚠️ | Sant Pere de Riudebitlles › Alt Penedès | 3 |
| Forêt de Torrelavit (50) ⚠️ | Torrelavit › Alt Penedès | 3 |
| Forêt de Sant Quintí de Mediona (12) ⚠️ | Sant Quintí de Mediona › Alt Penedès | 3 |
| Forêt de Mediona (81) ⚠️ | Mediona › Alt Penedès | 3 |
| Forêt de Puig-reig (88) ⚠️ | Puig-reig › Berguedà | 3 |
| Forêt de Puig-reig (94) ⚠️ | Puig-reig › Berguedà | 3 |
| Forêt de Òdena (96) ⚠️ | Òdena › Anoia | 3 |
| Forêt de Òdena (115) ⚠️ | Òdena › Anoia | 3 |
| Forêt de Òdena (120) ⚠️ | Òdena › Anoia | 3 |
| Forêt de Òdena (124) ⚠️ | Òdena › Anoia | 3 |
| Forêt de Rupit i Pruit (36) ⚠️ | Rupit i Pruit › Osona (Barcelone) | 3 |
| Forêt de Tavertet (42) ⚠️ | Tavertet › Osona (Barcelone) | 3 |
| Forêt de Tavertet (77) ⚠️ | Tavertet › Osona (Barcelone) | 3 |
| Forêt de Lluçà (59) ⚠️ | Lluçà › Lluçanès | 3 |
| Forêt de Borredà (133) ⚠️ | Borredà › Berguedà | 3 |
| Forêt de Sant Cugat del Vallès (158) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 3 |
| Forêt de Sant Cebrià de Vallalta (6) ⚠️ | Sant Cebrià de Vallalta › Maresme | 3 |
| Forêt de Santa Susanna (11) ⚠️ | Santa Susanna › Maresme | 3 |
| Forêt de Arenys de Munt (16) ⚠️ | Arenys de Munt › Maresme | 3 |
| Forêt de Arenys de Munt (18) ⚠️ | Arenys de Munt › Maresme | 3 |
| Forêt de Arenys de Munt (19) ⚠️ | Arenys de Munt › Maresme | 3 |
| Forêt de Arenys de Munt (26) ⚠️ | Arenys de Munt › Maresme | 3 |
| Forêt de Vallgorguina (17) ⚠️ | Vallgorguina › Vallès Oriental | 3 |
| Forêt de Sant Celoni (54) ⚠️ | Sant Celoni › Vallès Oriental | 3 |
| Forêt de Sant Celoni (61) ⚠️ | Sant Celoni › Vallès Oriental | 3 |
| Forêt de Sant Celoni (68) ⚠️ | Sant Celoni › Vallès Oriental | 3 |
| Forêt de Sant Celoni (70) ⚠️ | Sant Celoni › Vallès Oriental | 3 |
| Forêt de Gironella (28) ⚠️ | Gironella › Berguedà | 3 |
| Forêt de Casserres (36) ⚠️ | Casserres › Berguedà | 3 |
| Forêt de Sallent (105) ⚠️ | Sallent › Bages | 3 |
| Forêt de Santpedor (20) ⚠️ | Santpedor › Bages | 3 |
| Forêt de Santpedor (59) ⚠️ | Santpedor › Bages | 3 |
| Forêt de Sant Feliu de Codines (16) ⚠️ | Sant Feliu de Codines › Vallès Oriental | 3 |
| Forêt de Bigues i Riells del Fai (41) ⚠️ | Bigues i Riells del Fai › Vallès Oriental | 3 |
| Forêt de Sallent (130) ⚠️ | Sallent › Bages | 3 |
| Forêt de Balsareny (90) ⚠️ | Sallent › Bages | 3 |
| Forêt de Castellnou de Bages (86) ⚠️ | Castellnou de Bages › Bages | 3 |
| Forêt de Castellnou de Bages (88) ⚠️ | Castellnou de Bages › Bages | 3 |
| Forêt de Sant Joan de Vilatorrada (69) ⚠️ | Sant Joan de Vilatorrada › Bages | 3 |
| Forêt de Sant Mateu de Bages (141) ⚠️ | Sant Mateu de Bages › Bages | 3 |
| Forêt de Guardiola de Berguedà (145) ⚠️ | Guardiola de Berguedà › Berguedà | 3 |
| Forêt de Santa Eugènia de Berga (6) ⚠️ | Santa Eugènia de Berga › Osona (Barcelone) | 3 |
| Forêt de Sant Sadurní d'Osormort (50) ⚠️ | Sant Sadurní d'Osormort › Osona (Barcelone) | 3 |
| Forêt de Folgueroles (4) ⚠️ | Folgueroles › Osona (Barcelone) | 3 |
| Forêt de Taradell (26) ⚠️ | Taradell › Osona (Barcelone) | 3 |
| Forêt de Taradell (42) ⚠️ | Taradell › Osona (Barcelone) | 3 |
| Forêt de Sant Julià de Vilatorta (22) ⚠️ | Sant Julià de Vilatorta › Osona (Barcelone) | 3 |
| Forêt de Sant Julià de Vilatorta (24) ⚠️ | Sant Julià de Vilatorta › Osona (Barcelone) | 3 |
| Forêt de Cervelló (21) ⚠️ | Cervelló › Baix Llobregat | 3 |
| Forêt de les Masies de Voltregà (17) ⚠️ | les Masies de Voltregà › Osona (Barcelone) | 3 |
| Forêt de Mataró (11) ⚠️ | Mataró › Maresme | 3 |
| Forêt de Cabrera de Mar (6) ⚠️ | Cabrera de Mar › Maresme | 3 |
| Forêt de Santa Eulàlia de Riuprimer (28) ⚠️ | Santa Eulàlia de Riuprimer › Osona (Barcelone) | 3 |
| Forêt de Gurb (34) ⚠️ | Gurb › Osona (Barcelone) | 3 |
| Forêt de Gurb (68) ⚠️ | Gurb › Osona (Barcelone) | 3 |
| Forêt de Gurb (75) ⚠️ | Gurb › Osona (Barcelone) | 3 |
| Forêt de Montmeló (6) ⚠️ | Montmeló › Vallès Oriental | 3 |
| Bosc de Can Ferran ⚠️ | Granollers › Vallès Oriental | 3 |
| Forêt de Castellcir (11) ⚠️ | Sant Quirze Safaja › Moianès | 3 |
| Forêt de Sant Pere de Ribes (115) ⚠️ | Sant Pere de Ribes › Garraf | 3 |
| Forêt de Sentmenat (13) ⚠️ | Sentmenat › Vallès Occidental | 3 |
| Forêt de Palau-solità i Plegamans (17) ⚠️ | Palau-solità i Plegamans › Vallès Occidental | 3 |
| Parc de la Torre del Rector ⚠️ | Santa Perpètua de Mogoda › Vallès Occidental | 3 |
| Forêt de Prats de Lluçanès (34) ⚠️ | Prats de Lluçanès › Lluçanès | 3 |
| Forêt de Olost (18) ⚠️ | Olost › Lluçanès | 3 |
| Forêt de Calders (81) ⚠️ | Calders › Moianès | 3 |
| Forêt de Monistrol de Calders (45) ⚠️ | Monistrol de Calders › Moianès | 3 |
| Forêt de el Pont de Vilomara i Rocafort (30) ⚠️ | el Pont de Vilomara i Rocafort › Bages | 3 |
| Bois de Barcelona (114) ⚠️ | Barcelona › Barcelonès | 3 |
| Forêt de Gavà (5) ⚠️ | Gavà › Baix Llobregat | 2 |
| Parc de Terrassa (4) ⚠️ | Terrassa › Vallès Occidental | 2 |
| Parc de l'Estació del Nord ⚠️ | Barcelona › Barcelonès | 2 |
| Parc del Turó del Putxet ⚠️ | Barcelona › Barcelonès | 2 |
| Parc de Joan Miró ⚠️ | Barcelona › Barcelonès | 2 |
| Plaça del Pla de la Corneta ⚠️ | Terrassa › Vallès Occidental | 2 |
| Parc de Gernika ⚠️ | Terrassa › Vallès Occidental | 2 |
| Parc del Nord (2) ⚠️ | Terrassa › Vallès Occidental | 2 |
| Parc de Puigterrà ⚠️ | Manresa › Bages | 2 |
| Bosquet de Cal Pons ⚠️ | Puig-reig › Berguedà | 2 |
| Forêt de Palafolls (2) ⚠️ | Malgrat de Mar › Maresme | 2 |
| Forêt de Malgrat de Mar ⚠️ | Malgrat de Mar › Maresme | 2 |
| Forêt de Palafolls (7) ⚠️ | Palafolls › Maresme | 2 |
| Parc de Can Boada ⚠️ | Mataró › Maresme | 2 |
| Jardí de Terramar ⚠️ | Sitges › Garraf | 2 |
| Bosc dels Pinetons ⚠️ | Ripollet › Vallès Occidental | 2 |
| Parc del Puig de les Tres Forques ⚠️ | Granollers › Vallès Oriental | 2 |
| Parc dels Pinetons ⚠️ | Cardedeu › Vallès Oriental | 2 |
| Forêt de Vilassar de Mar ⚠️ | Vilassar de Mar › Maresme | 2 |
| Pinar de la Riera ⚠️ | Lliçà d'Amunt › Vallès Oriental | 2 |
| Parc de la Barceloneta ⚠️ | Barcelona › Barcelonès | 2 |
| Parc de la Cabana ⚠️ | l'Hospitalet de Llobregat › Barcelonès | 2 |
| Bois de Lliçà d'Amunt (3) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 2 |
| Bois de Lliçà d'Amunt (5) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 2 |
| Bois de Lliçà d'Amunt (15) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 2 |
| Forêt de Pontons (2) ⚠️ | Pontons › Alt Penedès | 2 |
| Forêt de Argençola (4) ⚠️ | Argençola › Anoia | 2 |
| Forêt de Bellprat ⚠️ | Bellprat › Anoia | 2 |
| Forêt de Oristà ⚠️ | Oristà › Lluçanès | 2 |
| Forêt de Montmaneu (3) ⚠️ | Montmaneu › Anoia | 2 |
| Forêt de Alpens (3) ⚠️ | Alpens › Lluçanès | 2 |
| Forêt de la Llacuna (3) ⚠️ | la Llacuna › Anoia | 2 |
| Forêt de Aiguafreda (2) ⚠️ | Aiguafreda › Osona (Barcelone) | 2 |
| Forêt de Fogars de la Selva (3) ⚠️ | Fogars de la Selva › la Selva (Barcelone) | 2 |
| Forêt de Sant Llorenç Savall (2) ⚠️ | Sant Llorenç Savall › Vallès Occidental | 2 |
| Forêt de els Hostalets de Pierola (6) ⚠️ | els Hostalets de Pierola › Anoia | 2 |
| Forêt de Begues ⚠️ | Begues › Baix Llobregat | 2 |
| Forêt de Sora (16) ⚠️ | Sora › Osona (Barcelone) | 2 |
| Forêt de Castellar del Vallès (6) ⚠️ | Castellar del Vallès › Vallès Occidental | 2 |
| Forêt de Sant Sadurní d'Osormort (10) ⚠️ | Sant Sadurní d'Osormort › Osona (Barcelone) | 2 |
| Bois de Matadepera ⚠️ | Matadepera › Vallès Occidental | 2 |
| Jardins de Vil·la Amèlia ⚠️ | Barcelona › Barcelonès | 2 |
| Forêt de Sant Pere de Ribes (4) ⚠️ | Sant Pere de Ribes › Garraf | 2 |
| Parc de la Quadra d'Enveja ⚠️ | Vilanova i la Geltrú › Garraf | 2 |
| Parc del Llobregat (2) ⚠️ | Sant Feliu de Llobregat › Baix Llobregat | 2 |
| Parc de Sant Cugat del Vallès (32) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 2 |
| Forêt de Sant Cugat del Vallès (63) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 2 |
| Forêt de Sant Cugat del Vallès (65) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 2 |
| Parc El Ramassar ⚠️ | Granollers › Vallès Oriental | 2 |
| Forêt de Sant Cugat del Vallès (94) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 2 |
| Forêt de Montornès del Vallès ⚠️ | Montornès del Vallès › Vallès Oriental | 2 |
| Parc del Nord (3) ⚠️ | Sabadell › Vallès Occidental | 2 |
| Bois de Sabadell (15) ⚠️ | Sabadell › Vallès Occidental | 2 |
| Parc de les Morisques ⚠️ | Sant Quirze del Vallès › Vallès Occidental | 2 |
| Bois de Sant Cugat del Vallès (63) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 2 |
| Parc de Sant Quirze del Vallès ⚠️ | Sant Quirze del Vallès › Vallès Occidental | 2 |
| Parc de Rubí (2) ⚠️ | Rubí › Vallès Occidental | 2 |
| Forêt de Terrassa (6) ⚠️ | Terrassa › Vallès Occidental | 2 |
| Forêt de Terrassa (9) ⚠️ | Terrassa › Vallès Occidental | 2 |
| Forêt de Terrassa (10) ⚠️ | Terrassa › Vallès Occidental | 2 |
| Forêt de Terrassa (11) ⚠️ | Terrassa › Vallès Occidental | 2 |
| Forêt de Terrassa (16) ⚠️ | Terrassa › Vallès Occidental | 2 |
| Forêt de Terrassa (19) ⚠️ | Terrassa › Vallès Occidental | 2 |
| Parc Pou d'en Fèlix ⚠️ | Esplugues de Llobregat › Baix Llobregat | 2 |
| Parc dels Torrents ⚠️ | Esplugues de Llobregat › Baix Llobregat | 2 |
| Parc del Rocar ⚠️ | Sitges › Garraf | 2 |
| Parc de Gurb (2) ⚠️ | Gurb › Osona (Barcelone) | 2 |
| Parc de Vic ⚠️ | Vic › Osona (Barcelone) | 2 |
| Parc de Pere Sallés ⚠️ | Sallent › Bages | 2 |
| Bois de Cerdanyola del Vallès (2) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 2 |
| Forêt de Cerdanyola del Vallès (23) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 2 |
| Forêt de Sant Climent de Llobregat (10) ⚠️ | Sant Climent de Llobregat › Baix Llobregat | 2 |
| Parc de Plana Lledó ⚠️ | Mollet del Vallès › Vallès Oriental | 2 |
| Parc de Ca l'Estrada ⚠️ | Mollet del Vallès › Vallès Oriental | 2 |
| Parc de Bellvitge ⚠️ | l'Hospitalet de Llobregat › Barcelonès | 2 |
| Bosc de Can Torres ⚠️ | Mollet del Vallès › Vallès Oriental | 2 |
| Forêt de Cerdanyola del Vallès (27) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 2 |
| Forêt de Olesa de Bonesvalls (3) ⚠️ | Olesa de Bonesvalls › Alt Penedès | 2 |
| Forêt de Gavà (11) ⚠️ | Gavà › Baix Llobregat | 2 |
| Forêt de Gavà (13) ⚠️ | Gavà › Baix Llobregat | 2 |
| Forêt de Sant Boi de Llobregat (2) ⚠️ | Sant Boi de Llobregat › Baix Llobregat | 2 |
| Forêt de Viladecans (6) ⚠️ | Viladecans › Baix Llobregat | 2 |
| Parc del G5 ⚠️ | Badalona › Barcelonès | 2 |
| Forêt de Olesa de Bonesvalls (7) ⚠️ | Olesa de Bonesvalls › Alt Penedès | 2 |
| Forêt de Avinyonet del Penedès (10) ⚠️ | Avinyonet del Penedès › Alt Penedès | 2 |
| Forêt de Vallirana (4) ⚠️ | Vallirana › Baix Llobregat | 2 |
| Forêt de Avinyonet del Penedès (13) ⚠️ | Avinyonet del Penedès › Alt Penedès | 2 |
| Forêt de Avinyonet del Penedès (19) ⚠️ | Avinyonet del Penedès › Alt Penedès | 2 |
| Forêt de Subirats (14) ⚠️ | Subirats › Alt Penedès | 2 |
| Forêt de Gavà (20) ⚠️ | Gavà › Baix Llobregat | 2 |
| Forêt de Avinyonet del Penedès (31) ⚠️ | Avinyonet del Penedès › Alt Penedès | 2 |
| Forêt de Avinyonet del Penedès (33) ⚠️ | Avinyonet del Penedès › Alt Penedès | 2 |
| Forêt de Gelida (4) ⚠️ | Gelida › Alt Penedès | 2 |
| Forêt de Subirats (29) ⚠️ | Subirats › Alt Penedès | 2 |
| Forêt de Subirats (34) ⚠️ | Subirats › Alt Penedès | 2 |
| Forêt de Sant Cugat Sesgarrigues (3) ⚠️ | Sant Cugat Sesgarrigues › Alt Penedès | 2 |
| Forêt de Sant Pere de Ribes (15) ⚠️ | Sant Pere de Ribes › Garraf | 2 |
| Forêt de Vilobí del Penedès (2) ⚠️ | Vilobí del Penedès › Alt Penedès | 2 |
| Forêt de Olèrdola (18) ⚠️ | Olèrdola › Alt Penedès | 2 |
| Forêt de Sant Martí Sarroca (2) ⚠️ | Sant Martí Sarroca › Alt Penedès | 2 |
| Forêt de Vilanova i la Geltrú (3) ⚠️ | Vilanova i la Geltrú › Garraf | 2 |
| Forêt de Subirats (47) ⚠️ | Subirats › Alt Penedès | 2 |
| Parc dels Ametllers ⚠️ | Santa Perpètua de Mogoda › Vallès Occidental | 2 |
| Forêt de Olèrdola (26) ⚠️ | Olèrdola › Alt Penedès | 2 |
| Forêt de Olèrdola (27) ⚠️ | Olèrdola › Alt Penedès | 2 |
| Forêt de Sant Pere de Ribes (21) ⚠️ | Sant Pere de Ribes › Garraf | 2 |
| Parc de l'Estany ⚠️ | Parets del Vallès › Vallès Oriental | 2 |
| Forêt de Sant Pere de Ribes (35) ⚠️ | Sant Pere de Ribes › Garraf | 2 |
| Forêt de Sant Pere de Ribes (36) ⚠️ | Sant Pere de Ribes › Garraf | 2 |
| Forêt de Sant Pere de Ribes (47) ⚠️ | Sant Pere de Ribes › Garraf | 2 |
| Forêt de Sant Pere de Ribes (51) ⚠️ | Sant Pere de Ribes › Garraf | 2 |
| Forêt de Olivella (12) ⚠️ | Olivella › Garraf | 2 |
| Forêt de Olivella (14) ⚠️ | Olivella › Garraf | 2 |
| Forêt de Olivella (16) ⚠️ | Olivella › Garraf | 2 |
| Forêt de Olivella (24) ⚠️ | Olivella › Garraf | 2 |
| Forêt de Sant Pere de Ribes (56) ⚠️ | Sant Pere de Ribes › Garraf | 2 |
| Forêt de Olivella (39) ⚠️ | Olivella › Garraf | 2 |
| Forêt de Sant Pere de Ribes (68) ⚠️ | Sant Pere de Ribes › Garraf | 2 |
| Parc de Terrassa (12) ⚠️ | Terrassa › Vallès Occidental | 2 |
| Forêt de Subirats (57) ⚠️ | Subirats › Alt Penedès | 2 |
| Forêt de Olesa de Bonesvalls (24) ⚠️ | Olesa de Bonesvalls › Alt Penedès | 2 |
| Forêt de Subirats (63) ⚠️ | Subirats › Alt Penedès | 2 |
| Forêt de Vallirana (6) ⚠️ | Vallirana › Baix Llobregat | 2 |
| Forêt de Vallirana (9) ⚠️ | Vallirana › Baix Llobregat | 2 |
| Forêt de Vallirana (10) ⚠️ | Vallirana › Baix Llobregat | 2 |
| Forêt de Olèrdola (37) ⚠️ | Olèrdola › Alt Penedès | 2 |
| Forêt de Vilafranca del Penedès ⚠️ | Vilafranca del Penedès › Alt Penedès | 2 |
| Forêt de Olèrdola (51) ⚠️ | Olèrdola › Alt Penedès | 2 |
| Forêt de Santa Margarida i els Monjos (9) ⚠️ | Santa Margarida i els Monjos › Alt Penedès | 2 |
| Parc de Barcelona (50) ⚠️ | Barcelona › Barcelonès | 2 |
| Forêt de Castellet i la Gornal (26) ⚠️ | Castellet i la Gornal › Alt Penedès | 2 |
| Forêt de Barcelona (4) ⚠️ | Barcelona › Barcelonès | 2 |
| Forêt de Castellet i la Gornal (33) ⚠️ | Castellet i la Gornal › Alt Penedès | 2 |
| Forêt de Terrassa (20) ⚠️ | Terrassa › Vallès Occidental | 2 |
| Forêt de Castellet i la Gornal (49) ⚠️ | Castellet i la Gornal › Alt Penedès | 2 |
| Parc de Manresa (11) ⚠️ | Manresa › Bages | 2 |
| Parc de Igualada ⚠️ | Igualada › Anoia | 2 |
| Parc del Castell (2) ⚠️ | Castelldefels › Baix Llobregat | 2 |
| Forêt de Castellet i la Gornal (55) ⚠️ | Castellet i la Gornal › Alt Penedès | 2 |
| Forêt de les Cabanyes ⚠️ | les Cabanyes › Alt Penedès | 2 |
| Forêt de Subirats (70) ⚠️ | Subirats › Alt Penedès | 2 |
| Forêt de Gelida (7) ⚠️ | Gelida › Alt Penedès | 2 |
| Forêt de Gelida (8) ⚠️ | Gelida › Alt Penedès | 2 |
| Forêt de Sant Esteve Sesrovires ⚠️ | Sant Esteve Sesrovires › Baix Llobregat | 2 |
| Forêt de Sant Llorenç d'Hortons (5) ⚠️ | Sant Llorenç d'Hortons › Alt Penedès | 2 |
| Forêt de Sant Llorenç d'Hortons (20) ⚠️ | Sant Llorenç d'Hortons › Alt Penedès | 2 |
| Forêt de Gelida (14) ⚠️ | Gelida › Alt Penedès | 2 |
| Forêt de Sant Llorenç d'Hortons (25) ⚠️ | Sant Llorenç d'Hortons › Alt Penedès | 2 |
| Forêt de Sant Sadurní d'Anoia (12) ⚠️ | Sant Sadurní d'Anoia › Alt Penedès | 2 |
| Forêt de Torrelavit (10) ⚠️ | Torrelavit › Alt Penedès | 2 |
| Forêt de Torrelavit (14) ⚠️ | Torrelavit › Alt Penedès | 2 |
| Forêt de Torrelavit (15) ⚠️ | Torrelavit › Alt Penedès | 2 |
| Forêt de Subirats (80) ⚠️ | Subirats › Alt Penedès | 2 |
| Forêt de el Pla del Penedès (6) ⚠️ | el Pla del Penedès › Alt Penedès | 2 |
| Forêt de Castellví de la Marca (27) ⚠️ | Castellví de la Marca › Alt Penedès | 2 |
| Forêt de Sant Martí Sarroca (12) ⚠️ | Sant Martí Sarroca › Alt Penedès | 2 |
| Forêt de Castellví de la Marca (37) ⚠️ | Castellví de la Marca › Alt Penedès | 2 |
| Forêt de Santa Maria de Palautordera (2) ⚠️ | Santa Maria de Palautordera › Vallès Oriental | 2 |
| Forêt de Sant Celoni (7) ⚠️ | Sant Celoni › Vallès Oriental | 2 |
| Forêt de Castellví de la Marca (48) ⚠️ | Castellví de la Marca › Alt Penedès | 2 |
| Bois de Bigues i Riells del Fai (2) ⚠️ | Bigues i Riells del Fai › Vallès Oriental | 2 |
| Forêt de Caldes de Montbui (3) ⚠️ | Caldes de Montbui › Vallès Oriental | 2 |
| Forêt de Caldes de Montbui (5) ⚠️ | Caldes de Montbui › Vallès Oriental | 2 |
| Forêt de Fonollosa (4) ⚠️ | Fonollosa › Bages | 2 |
| Forêt de Castellar del Vallès (7) ⚠️ | Castellar del Vallès › Vallès Occidental | 2 |
| Parc del Nord (4) ⚠️ | Sabadell › Vallès Occidental | 2 |
| Jardins del Dr. Ribalta ⚠️ | Esplugues de Llobregat › Baix Llobregat | 2 |
| Parc de les tres Esplugues ⚠️ | Esplugues de Llobregat › Baix Llobregat | 2 |
| Parc de Can Gorgs ⚠️ | Barberà del Vallès › Vallès Occidental | 2 |
| Bois de Bigues i Riells del Fai (3) ⚠️ | Bigues i Riells del Fai › Vallès Oriental | 2 |
| Forêt de Fonollosa (22) ⚠️ | Fonollosa › Bages | 2 |
| Masia Plallorens ⚠️ | Vilafranca del Penedès › Alt Penedès | 2 |
| Bois de Òrrius (8) ⚠️ | Òrrius › Maresme | 2 |
| Bois de Òrrius (9) ⚠️ | Argentona › Maresme | 2 |
| Bois de la Roca del Vallès (10) ⚠️ | la Roca del Vallès › Vallès Oriental | 2 |
| Bois de la Roca del Vallès (14) ⚠️ | Òrrius › Maresme | 2 |
| Bois de Òrrius (15) ⚠️ | Òrrius › Maresme | 2 |
| Bois de Vallromanes (4) ⚠️ | Vallromanes › Vallès Oriental | 2 |
| Bois de Vilassar de Dalt (20) ⚠️ | Vilassar de Dalt › Maresme | 2 |
| Bois de Premià de Dalt (4) ⚠️ | Premià de Dalt › Maresme | 2 |
| Bois de Vilanova del Vallès (6) ⚠️ | Vilanova del Vallès › Vallès Oriental | 2 |
| Bois de Argentona (14) ⚠️ | Argentona › Maresme | 2 |
| Bois de Argentona (20) ⚠️ | Argentona › Maresme | 2 |
| Bois de Teià (7) ⚠️ | Teià › Maresme | 2 |
| Bois de Vallromanes (12) ⚠️ | Vallromanes › Vallès Oriental | 2 |
| Bois de la Roca del Vallès (19) ⚠️ | la Roca del Vallès › Vallès Oriental | 2 |
| Bois de Llinars del Vallès (7) ⚠️ | Llinars del Vallès › Vallès Oriental | 2 |
| Forêt de els Prats de Rei (6) ⚠️ | els Prats de Rei › Anoia | 2 |
| Bois de Llinars del Vallès (22) ⚠️ | Llinars del Vallès › Vallès Oriental | 2 |
| Bois de Llinars del Vallès (24) ⚠️ | Llinars del Vallès › Vallès Oriental | 2 |
| Parc Forestal de l'Ermita del Pla de Sant Joan ⚠️ | la Palma de Cervelló › Baix Llobregat | 2 |
| Parc de Vic (9) ⚠️ | Vic › Osona (Barcelone) | 2 |
| Forêt de Balenyà (3) ⚠️ | Balenyà › Osona (Barcelone) | 2 |
| Forêt de Òdena (18) ⚠️ | Òdena › Anoia | 2 |
| Forêt de Piera (13) ⚠️ | Piera › Anoia | 2 |
| Parc de Mataró (12) ⚠️ | Mataró › Maresme | 2 |
| Plaça del Moviment Obrer ⚠️ | Barcelona › Barcelonès | 2 |
| Bois de Rubí (3) ⚠️ | Rubí › Vallès Occidental | 2 |
| Forêt de Cubelles (2) ⚠️ | Cubelles › Garraf | 2 |
| Parc de Badia del Vallès (8) ⚠️ | Badia del Vallès › Vallès Occidental | 2 |
| Forêt de Monistrol de Montserrat (4) ⚠️ | Monistrol de Montserrat › Bages | 2 |
| Forêt de Barberà del Vallès (4) ⚠️ | Barberà del Vallès › Vallès Occidental | 2 |
| Bois de Lliçà d'Amunt (23) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 2 |
| Parc dels Gorgs ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 2 |
| Forêt de Santa Margarida de Montbui (2) ⚠️ | Santa Margarida de Montbui › Anoia | 2 |
| Forêt de Montcada i Reixac (7) ⚠️ | Montcada i Reixac › Vallès Occidental | 2 |
| Forêt de Montcada i Reixac (9) ⚠️ | Montcada i Reixac › Vallès Occidental | 2 |
| Forêt de Montcada i Reixac (10) ⚠️ | Montcada i Reixac › Vallès Occidental | 2 |
| Forêt de Montcada i Reixac (11) ⚠️ | Montcada i Reixac › Vallès Occidental | 2 |
| Forêt de Santa Perpètua de Mogoda (10) ⚠️ | Santa Perpètua de Mogoda › Vallès Occidental | 2 |
| Bois de Argentona (34) ⚠️ | Argentona › Maresme | 2 |
| Bois de Argentona (43) ⚠️ | Argentona › Maresme | 2 |
| Forêt de Cerdanyola del Vallès (32) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 2 |
| Bois de Canovelles (14) ⚠️ | Canovelles › Vallès Oriental | 2 |
| Bosc del Molí dels Capellans ⚠️ | Granollers › Vallès Oriental | 2 |
| Forêt de Canovelles (2) ⚠️ | Canovelles › Vallès Oriental | 2 |
| Forêt de l'Ametlla del Vallès (3) ⚠️ | l'Ametlla del Vallès › Vallès Oriental | 2 |
| Forêt de Barcelona (14) ⚠️ | Barcelona › Barcelonès | 2 |
| Parc de la Riera de Canyadó ⚠️ | Badalona › Barcelonès | 2 |
| Parc de la Mediterrània (3) ⚠️ | Badalona › Barcelonès | 2 |
| Forêt de Sant Just Desvern (4) ⚠️ | Sant Just Desvern › Baix Llobregat | 2 |
| Parc de Cerdanyola del Vallès (15) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 2 |
| Forêt de Sabadell (16) ⚠️ | Sabadell › Vallès Occidental | 2 |
| Forêt de Sabadell (21) ⚠️ | Sabadell › Vallès Occidental | 2 |
| Forêt de Polinyà (2) ⚠️ | Polinyà › Vallès Occidental | 2 |
| Forêt de Sabadell (23) ⚠️ | Sabadell › Vallès Occidental | 2 |
| Forêt de Sabadell (30) ⚠️ | Sabadell › Vallès Occidental | 2 |
| Forêt de Sabadell (37) ⚠️ | Sabadell › Vallès Occidental | 2 |
| Forêt de Santa Perpètua de Mogoda (14) ⚠️ | Santa Perpètua de Mogoda › Vallès Occidental | 2 |
| Forêt de Polinyà (9) ⚠️ | Polinyà › Vallès Occidental | 2 |
| Forêt de Palau-solità i Plegamans (3) ⚠️ | Palau-solità i Plegamans › Vallès Occidental | 2 |
| Forêt de Palau-solità i Plegamans (4) ⚠️ | Palau-solità i Plegamans › Vallès Occidental | 2 |
| Forêt de Terrassa (29) ⚠️ | Terrassa › Vallès Occidental | 2 |
| Forêt de Terrassa (31) ⚠️ | Terrassa › Vallès Occidental | 2 |
| Parc de Montcada i Reixac (19) ⚠️ | Montcada i Reixac › Vallès Occidental | 2 |
| Forêt de Sant Boi de Llobregat (8) ⚠️ | Sant Boi de Llobregat › Baix Llobregat | 2 |
| Forêt de Caldes d'Estrac (3) ⚠️ | Caldes d'Estrac › Maresme | 2 |
| Parc de Barcelona (96) ⚠️ | Barcelona › Barcelonès | 2 |
| Parc de Can Corts ⚠️ | Cornellà de Llobregat › Baix Llobregat | 2 |
| Forêt de Vacarisses (2) ⚠️ | Vacarisses › Vallès Occidental | 2 |
| Forêt de Monistrol de Calders (3) ⚠️ | Monistrol de Calders › Moianès | 2 |
| Forêt de Monistrol de Calders (5) ⚠️ | Monistrol de Calders › Moianès | 2 |
| Parc del Prat de Cubelles ⚠️ | Cubelles › Garraf | 2 |
| Forêt de Fonollosa (29) ⚠️ | Fonollosa › Bages | 2 |
| Forêt de Fígols ⚠️ | Fígols › Berguedà | 2 |
| Forêt de Aiguafreda (4) ⚠️ | Aiguafreda › Osona (Barcelone) | 2 |
| Forêt de Cerdanyola del Vallès (36) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 2 |
| Bois de Lliçà de Vall (2) ⚠️ | Lliçà de Vall › Vallès Oriental | 2 |
| Bois de Lliçà de Vall (3) ⚠️ | Lliçà de Vall › Vallès Oriental | 2 |
| Parc de l'Arboretum ⚠️ | Manlleu › Osona (Barcelone) | 2 |
| Forêt de Vallromanes (5) ⚠️ | Vallromanes › Vallès Oriental | 2 |
| Bois de Gurb (32) ⚠️ | Gurb › Osona (Barcelone) | 2 |
| Turó de l'Enric ⚠️ | Badalona › Barcelonès | 2 |
| Forêt de Avià (6) ⚠️ | Avià › Berguedà | 2 |
| Forêt de Castellnou de Bages (4) ⚠️ | Castellnou de Bages › Bages | 2 |
| Parc de Caramar ⚠️ | el Masnou › Maresme | 2 |
| Forêt de Sant Celoni (8) ⚠️ | Sant Celoni › Vallès Oriental | 2 |
| Passeig del Ter (3) ⚠️ | Manlleu › Osona (Barcelone) | 2 |
| Finca de Cal Peix ⚠️ | Argentona › Maresme | 2 |
| Parc d'Aigües de Montcada ⚠️ | Barcelona › Barcelonès | 2 |
| Forêt de Oristà (16) ⚠️ | Oristà › Lluçanès | 2 |
| Forêt de Oristà (27) ⚠️ | Oristà › Lluçanès | 2 |
| Forêt de Oristà (47) ⚠️ | Oristà › Lluçanès | 2 |
| Forêt de Oristà (56) ⚠️ | Oristà › Lluçanès | 2 |
| Forêt de Santa Maria d'Oló (7) ⚠️ | Santa Maria d'Oló › Moianès | 2 |
| Bois de Sant Fost de Campsentelles (3) ⚠️ | Sant Fost de Campsentelles › Vallès Oriental | 2 |
| Bois de Martorelles ⚠️ | Martorelles › Vallès Oriental | 2 |
| Forêt de Vallromanes (6) ⚠️ | Vallromanes › Vallès Oriental | 2 |
| Forêt de Montornès del Vallès (3) ⚠️ | Montornès del Vallès › Vallès Oriental | 2 |
| Forêt de Montornès del Vallès (4) ⚠️ | Montornès del Vallès › Vallès Oriental | 2 |
| Bois de Tiana (5) ⚠️ | Tiana › Maresme | 2 |
| Bois de Terrassa (5) ⚠️ | Terrassa › Vallès Occidental | 2 |
| Bois de Terrassa (11) ⚠️ | Terrassa › Vallès Occidental | 2 |
| Bois de Sabadell (24) ⚠️ | Sabadell › Vallès Occidental | 2 |
| Forêt de Terrassa (33) ⚠️ | Terrassa › Vallès Occidental | 2 |
| Forêt de Terrassa (34) ⚠️ | Terrassa › Vallès Occidental | 2 |
| Forêt de Terrassa (38) ⚠️ | Terrassa › Vallès Occidental | 2 |
| Forêt de Sabadell (46) ⚠️ | Sabadell › Vallès Occidental | 2 |
| Bois de Rubí (6) ⚠️ | Rubí › Vallès Occidental | 2 |
| Forêt de Rubí (11) ⚠️ | Rubí › Vallès Occidental | 2 |
| Forêt de Sant Cugat del Vallès (101) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 2 |
| Forêt de Sant Cugat del Vallès (103) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 2 |
| Forêt de Rubí (13) ⚠️ | Rubí › Vallès Occidental | 2 |
| Forêt de Rubí (17) ⚠️ | Rubí › Vallès Occidental | 2 |
| Forêt de Rubí (27) ⚠️ | Rubí › Vallès Occidental | 2 |
| Forêt de Rubí (33) ⚠️ | Rubí › Vallès Occidental | 2 |
| Forêt de Rubí (34) ⚠️ | Rubí › Vallès Occidental | 2 |
| Forêt de Rubí (40) ⚠️ | Rubí › Vallès Occidental | 2 |
| Torrent de la romeua ⚠️ | Sabadell › Vallès Occidental | 2 |
| Forêt de Sant Salvador de Guardiola (6) ⚠️ | Sant Salvador de Guardiola › Bages | 2 |
| Forêt de Sant Salvador de Guardiola (8) ⚠️ | Sant Salvador de Guardiola › Bages | 2 |
| Forêt de Sant Salvador de Guardiola (10) ⚠️ | Sant Salvador de Guardiola › Bages | 2 |
| Forêt de Sant Salvador de Guardiola (13) ⚠️ | Sant Salvador de Guardiola › Bages | 2 |
| Bois de Premià de Dalt (8) ⚠️ | Premià de Dalt › Maresme | 2 |
| Bois de les Franqueses del Vallès (3) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 2 |
| Parc de Barcelona (121) ⚠️ | Barcelona › Barcelonès | 2 |
| Forêt de Corbera de Llobregat (6) ⚠️ | Corbera de Llobregat › Baix Llobregat | 2 |
| Forêt de Pallejà (2) ⚠️ | Pallejà › Baix Llobregat | 2 |
| Forêt de Corbera de Llobregat (10) ⚠️ | Corbera de Llobregat › Baix Llobregat | 2 |
| Forêt de Cervelló ⚠️ | Cervelló › Baix Llobregat | 2 |
| Forêt de Cervelló (2) ⚠️ | Cervelló › Baix Llobregat | 2 |
| la Devesa ⚠️ | Terrassa › Vallès Occidental | 2 |
| Forêt de Rubí (43) ⚠️ | Rubí › Vallès Occidental | 2 |
| Forêt de Sant Quirze del Vallès (12) ⚠️ | Sant Quirze del Vallès › Vallès Occidental | 2 |
| Forêt de Sant Llorenç Savall (11) ⚠️ | Castellar del Vallès › Vallès Occidental | 2 |
| Forêt de Sant Llorenç Savall (13) ⚠️ | Sant Llorenç Savall › Vallès Occidental | 2 |
| Forêt de Palau-solità i Plegamans (9) ⚠️ | Palau-solità i Plegamans › Vallès Occidental | 2 |
| Forêt de Sant Cugat del Vallès (106) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 2 |
| Bois de Castellet i la Gornal ⚠️ | Castellet i la Gornal › Alt Penedès | 2 |
| Bois de Sant Llorenç Savall (4) ⚠️ | Sant Llorenç Savall › Vallès Occidental | 2 |
| Bois de Santa Margarida i els Monjos ⚠️ | Santa Margarida i els Monjos › Alt Penedès | 2 |
| Forêt de Cànoves i Samalús (2) ⚠️ | Cànoves i Samalús › Vallès Oriental | 2 |
| Hortes dels Frares ⚠️ | Terrassa › Vallès Occidental | 2 |
| Bois de Castellet i la Gornal (2) ⚠️ | Castellet i la Gornal › Alt Penedès | 2 |
| Forêt de Gaià (4) ⚠️ | Gaià › Bages | 2 |
| Forêt de Sant Pere de Vilamajor (2) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 2 |
| Forêt de Sant Celoni (10) ⚠️ | Sant Celoni › Vallès Oriental | 2 |
| Forêt de Aguilar de Segarra (10) ⚠️ | Aguilar de Segarra › Bages | 2 |
| Parc dels Torrents (2) ⚠️ | Esplugues de Llobregat › Baix Llobregat | 2 |
| Forêt de Castellgalí (8) ⚠️ | Castellgalí › Bages | 2 |
| Forêt de Esparreguera (3) ⚠️ | Esparreguera › Baix Llobregat | 2 |
| Forêt de Avià (8) ⚠️ | Avià › Berguedà | 2 |
| Forêt de l'Espunyola (4) ⚠️ | l'Espunyola › Berguedà | 2 |
| Forêt de Cardona (11) ⚠️ | Cardona › Bages | 2 |
| Forêt de Molins de Rei (5) ⚠️ | Molins de Rei › Baix Llobregat | 2 |
| Bois de Sant Cugat del Vallès (87) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 2 |
| Forêt de Molins de Rei (8) ⚠️ | Molins de Rei › Baix Llobregat | 2 |
| Bois de Sant Cugat del Vallès (88) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 2 |
| Forêt de Sant Cugat del Vallès (107) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 2 |
| Bois de Sant Cugat del Vallès (99) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 2 |
| Forêt de Vilanova i la Geltrú (12) ⚠️ | Vilanova i la Geltrú › Garraf | 2 |
| Bois de Sentmenat (3) ⚠️ | Sentmenat › Vallès Occidental | 2 |
| Forêt de Santa Eulàlia de Ronçana (6) ⚠️ | Santa Eulàlia de Ronçana › Vallès Oriental | 2 |
| Bosc de Cal Ceballot ⚠️ | Granollers › Vallès Oriental | 2 |
| Forêt de Collsuspina (3) ⚠️ | Collsuspina › Moianès | 2 |
| Bois de Piera (4) ⚠️ | Piera › Anoia | 2 |
| Bois de Piera (5) ⚠️ | Piera › Anoia | 2 |
| Bois de Vilanova del Vallès (8) ⚠️ | Vilanova del Vallès › Vallès Oriental | 2 |
| Bosc de Ca la Joana ⚠️ | Vilanova del Vallès › Vallès Oriental | 2 |
| Forêt de Castellet i la Gornal (60) ⚠️ | Castellet i la Gornal › Alt Penedès | 2 |
| Forêt de Begues (12) ⚠️ | Begues › Baix Llobregat | 2 |
| Forêt de Begues (14) ⚠️ | Begues › Baix Llobregat | 2 |
| Forêt de Canyelles (2) ⚠️ | Canyelles › Garraf | 2 |
| Forêt de Vilanova i la Geltrú (14) ⚠️ | Vilanova i la Geltrú › Garraf | 2 |
| Forêt de Sant Martí Sarroca (26) ⚠️ | Sant Martí Sarroca › Alt Penedès | 2 |
| Forêt de Castellví de la Marca (56) ⚠️ | Castellví de la Marca › Alt Penedès | 2 |
| Bois de Sant Esteve Sesrovires ⚠️ | Sant Esteve Sesrovires › Baix Llobregat | 2 |
| Bois de Lliçà de Vall (4) ⚠️ | Lliçà de Vall › Vallès Oriental | 2 |
| Forêt de Castellar del Vallès (10) ⚠️ | Castellar del Vallès › Vallès Occidental | 2 |
| Forêt de la Garriga (8) ⚠️ | la Garriga › Vallès Oriental | 2 |
| Forêt de la Garriga (9) ⚠️ | la Garriga › Vallès Oriental | 2 |
| Forêt de Argentona ⚠️ | Argentona › Maresme | 2 |
| Forêt de Matadepera (31) ⚠️ | Matadepera › Vallès Occidental | 2 |
| Forêt de l'Ametlla del Vallès (10) ⚠️ | la Garriga › Vallès Oriental | 2 |
| Forêt de Campins (6) ⚠️ | Campins › Vallès Oriental | 2 |
| Bois de Montmaneu (7) ⚠️ | Montmaneu › Anoia | 2 |
| Bois de Argençola ⚠️ | Argençola › Anoia | 2 |
| Forêt de Lliçà de Vall (3) ⚠️ | Lliçà de Vall › Vallès Oriental | 2 |
| Forêt de Argençola (24) ⚠️ | Argençola › Anoia | 2 |
| Forêt de Muntanyola (11) ⚠️ | Muntanyola › Osona (Barcelone) | 2 |
| Forêt de l'Ametlla del Vallès (13) ⚠️ | l'Ametlla del Vallès › Vallès Oriental | 2 |
| Forêt de Sant Quirze Safaja ⚠️ | Sant Quirze Safaja › Moianès | 2 |
| Forêt de Sant Martí de Centelles (31) ⚠️ | Sant Martí de Centelles › Osona (Barcelone) | 2 |
| Forêt de Sant Martí de Centelles (34) ⚠️ | Sant Martí de Centelles › Osona (Barcelone) | 2 |
| Forêt de Sant Quirze Safaja (4) ⚠️ | Sant Quirze Safaja › Moianès | 2 |
| Forêt de Sant Martí de Centelles (42) ⚠️ | Sant Martí de Centelles › Osona (Barcelone) | 2 |
| Forêt de Sant Martí de Centelles (46) ⚠️ | Sant Martí de Centelles › Osona (Barcelone) | 2 |
| Forêt de Sant Pere de Vilamajor (9) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 2 |
| Forêt de Sant Pere de Vilamajor (22) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 2 |
| Forêt de Sant Pere de Vilamajor (29) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 2 |
| Forêt de Sant Pere de Vilamajor (40) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 2 |
| Forêt de Sant Antoni de Vilamajor (5) ⚠️ | Sant Antoni de Vilamajor › Vallès Oriental | 2 |
| Bois de l'Esquirol (5) ⚠️ | l'Esquirol › Osona (Barcelone) | 2 |
| Forêt de l'Esquirol (15) ⚠️ | l'Esquirol › Osona (Barcelone) | 2 |
| Forêt de l'Esquirol (18) ⚠️ | l'Esquirol › Osona (Barcelone) | 2 |
| Forêt de l'Esquirol (20) ⚠️ | l'Esquirol › Osona (Barcelone) | 2 |
| Forêt de l'Esquirol (48) ⚠️ | l'Esquirol › Osona (Barcelone) | 2 |
| Forêt de l'Esquirol (68) ⚠️ | l'Esquirol › Osona (Barcelone) | 2 |
| Forêt de l'Esquirol (80) ⚠️ | l'Esquirol › Osona (Barcelone) | 2 |
| Forêt de Manlleu (7) ⚠️ | Manlleu › Osona (Barcelone) | 2 |
| Forêt de l'Esquirol (109) ⚠️ | l'Esquirol › Osona (Barcelone) | 2 |
| Forêt de Olost (3) ⚠️ | Olost › Lluçanès | 2 |
| Forêt de Dosrius (3) ⚠️ | Dosrius › Maresme | 2 |
| Forêt de les Franqueses del Vallès (36) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 2 |
| Forêt de Tordera (26) ⚠️ | Tordera › Maresme | 2 |
| Forêt de Llinars del Vallès (2) ⚠️ | Llinars del Vallès › Vallès Oriental | 2 |
| Forêt de Llinars del Vallès (15) ⚠️ | Llinars del Vallès › Vallès Oriental | 2 |
| Bois de Montmaneu (34) ⚠️ | Montmaneu › Anoia | 2 |
| Forêt de Palafolls (24) ⚠️ | Palafolls › Maresme | 2 |
| Bois de Torrelavit (18) ⚠️ | Torrelavit › Alt Penedès | 2 |
| Bois de Font-rubí (3) ⚠️ | Font-rubí › Alt Penedès | 2 |
| Forêt de Gisclareny (4) ⚠️ | Gisclareny › Berguedà | 2 |
| Forêt de Gisclareny (7) ⚠️ | Gisclareny › Berguedà | 2 |
| Forêt de Sant Antoni de Vilamajor (29) ⚠️ | Sant Antoni de Vilamajor › Vallès Oriental | 2 |
| Forêt de Sant Antoni de Vilamajor (32) ⚠️ | Sant Antoni de Vilamajor › Vallès Oriental | 2 |
| Bois de Sabadell (28) ⚠️ | Sabadell › Vallès Occidental | 2 |
| Forêt de Tordera (32) ⚠️ | Tordera › Maresme | 2 |
| Parc dels Garrofers ⚠️ | Barcelona › Barcelonès | 2 |
| Forêt de Llinars del Vallès (56) ⚠️ | Llinars del Vallès › Vallès Oriental | 2 |
| Forêt de Guardiola de Berguedà (8) ⚠️ | Guardiola de Berguedà › Berguedà | 2 |
| Forêt de Santa Maria de Palautordera (15) ⚠️ | Santa Maria de Palautordera › Vallès Oriental | 2 |
| Bois de Sant Celoni (2) ⚠️ | Santa Maria de Palautordera › Vallès Oriental | 2 |
| Bosc de l'Arboçar ⚠️ | Torrelles de Foix › Alt Penedès | 2 |
| Forêt de Moià (12) ⚠️ | Moià › Moianès | 2 |
| Forêt de Castellar de n'Hug (3) ⚠️ | Castellar de n'Hug › Berguedà | 2 |
| Parc de les Comes ⚠️ | Igualada › Anoia | 2 |
| Bois de Seva (3) ⚠️ | Seva › Osona (Barcelone) | 2 |
| Parc de la Pollancreda ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 2 |
| Parc de Lourdes ⚠️ | Arenys de Munt › Maresme | 2 |
| Bois de el Pla del Penedès (2) ⚠️ | el Pla del Penedès › Alt Penedès | 2 |
| Bois de Argençola (16) ⚠️ | Argençola › Anoia | 2 |
| Forêt de Tordera (39) ⚠️ | Tordera › Maresme | 2 |
| Forêt de Sant Feliu Sasserra (6) ⚠️ | Sant Feliu Sasserra › Bages | 2 |
| Forêt de les Masies de Voltregà (8) ⚠️ | les Masies de Voltregà › Osona (Barcelone) | 2 |
| Forêt de Arenys de Mar (6) ⚠️ | Arenys de Mar › Maresme | 2 |
| Forêt de Argentona (2) ⚠️ | Argentona › Maresme | 2 |
| Forêt de Cabrils (4) ⚠️ | Cabrils › Maresme | 2 |
| Bois de la Llacuna ⚠️ | la Llacuna › Anoia | 2 |
| Forêt de Sant Boi de Llobregat (20) ⚠️ | Sant Boi de Llobregat › Baix Llobregat | 2 |
| Bois de Jorba (7) ⚠️ | Jorba › Anoia | 2 |
| Bois de Jorba (9) ⚠️ | Jorba › Anoia | 2 |
| Bois de Masquefa (4) ⚠️ | Masquefa › Anoia | 2 |
| Bois de la Llacuna (2) ⚠️ | la Llacuna › Anoia | 2 |
| Forêt de Subirats (87) ⚠️ | Subirats › Alt Penedès | 2 |
| Bosc de Can Feliuà ⚠️ | Granollers › Vallès Oriental | 2 |
| Forêt de Subirats (89) ⚠️ | Subirats › Alt Penedès | 2 |
| Forêt de Guardiola de Berguedà (10) ⚠️ | Guardiola de Berguedà › Berguedà | 2 |
| Forêt de Sant Pere de Vilamajor (74) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 2 |
| Forêt de Aiguafreda (7) ⚠️ | Seva › Osona (Barcelone) | 2 |
| Forêt de Fonollosa (83) ⚠️ | Fonollosa › Bages | 2 |
| Bois de el Prat de Llobregat (281) ⚠️ | el Prat de Llobregat › Baix Llobregat | 2 |
| Bois de el Prat de Llobregat (282) ⚠️ | el Prat de Llobregat › Baix Llobregat | 2 |
| Pineda del Remolar ⚠️ | Viladecans › Baix Llobregat | 2 |
| Forêt de Santpedor (11) ⚠️ | Santpedor › Bages | 2 |
| Forêt de Montmajor (29) ⚠️ | Montmajor › Berguedà | 2 |
| Forêt de Fonollosa (88) ⚠️ | Fonollosa › Bages | 2 |
| Forêt de Cardona (35) ⚠️ | Cardona › Bages | 2 |
| Forêt de les Masies de Voltregà (9) ⚠️ | les Masies de Voltregà › Osona (Barcelone) | 2 |
| Forêt de Castellterçol (13) ⚠️ | Castellterçol › Moianès | 2 |
| Forêt de Aguilar de Segarra (23) ⚠️ | Aguilar de Segarra › Bages | 2 |
| Forêt de Fonollosa (90) ⚠️ | Fonollosa › Bages | 2 |
| Forêt de Rajadell (12) ⚠️ | Rajadell › Bages | 2 |
| Forêt de Sant Joan de Vilatorrada (22) ⚠️ | Sant Joan de Vilatorrada › Bages | 2 |
| Forêt de Sant Joan de Vilatorrada (23) ⚠️ | Sant Joan de Vilatorrada › Bages | 2 |
| Forêt de Sant Joan de Vilatorrada (26) ⚠️ | Sant Joan de Vilatorrada › Bages | 2 |
| Forêt de Sallent (37) ⚠️ | Sallent › Bages | 2 |
| Forêt de Avinyó (25) ⚠️ | Avinyó › Bages | 2 |
| Forêt de Sallent (46) ⚠️ | Sallent › Bages | 2 |
| Forêt de Balsareny (37) ⚠️ | Balsareny › Bages | 2 |
| Forêt de Artés (7) ⚠️ | Artés › Bages | 2 |
| Forêt de Sant Fruitós de Bages (11) ⚠️ | Sant Fruitós de Bages › Bages | 2 |
| Forêt de Sant Fruitós de Bages (12) ⚠️ | Sant Fruitós de Bages › Bages | 2 |
| Forêt de Sant Fruitós de Bages (13) ⚠️ | Sant Fruitós de Bages › Bages | 2 |
| Forêt de Sant Fruitós de Bages (14) ⚠️ | Sant Fruitós de Bages › Bages | 2 |
| Forêt de Sant Fruitós de Bages (22) ⚠️ | Sant Fruitós de Bages › Bages | 2 |
| Forêt de Calders (8) ⚠️ | Calders › Moianès | 2 |
| Forêt de Calders (10) ⚠️ | Calders › Moianès | 2 |
| Forêt de Calders (13) ⚠️ | Calders › Moianès | 2 |
| Forêt de Calders (19) ⚠️ | Calders › Moianès | 2 |
| Forêt de Calders (20) ⚠️ | Calders › Moianès | 2 |
| Forêt de Navarcles (7) ⚠️ | Navarcles › Bages | 2 |
| Forêt de Vallcebre (13) ⚠️ | Vallcebre › Berguedà | 2 |
| Forêt de Cànoves i Samalús (31) ⚠️ | Cànoves i Samalús › Vallès Oriental | 2 |
| Forêt de Cànoves i Samalús (33) ⚠️ | Cànoves i Samalús › Vallès Oriental | 2 |
| Forêt de Sant Joan de Vilatorrada (29) ⚠️ | Sant Joan de Vilatorrada › Bages | 2 |
| Forêt de Manresa (48) ⚠️ | Manresa › Bages | 2 |
| Forêt de Manresa (55) ⚠️ | Manresa › Bages | 2 |
| Forêt de Manresa (57) ⚠️ | Manresa › Bages | 2 |
| Bois de Viladecavalls (4) ⚠️ | Viladecavalls › Vallès Occidental | 2 |
| Forêt de Castellterçol (25) ⚠️ | Castellterçol › Moianès | 2 |
| Parc del Canal de la Infanta ⚠️ | Cornellà de Llobregat › Baix Llobregat | 2 |
| Forêt de Gironella (4) ⚠️ | Gironella › Berguedà | 2 |
| Parc de Baix-A-Mar ⚠️ | Vilanova i la Geltrú › Garraf | 2 |
| Forêt de Sant Joan de Vilatorrada (34) ⚠️ | Sant Joan de Vilatorrada › Bages | 2 |
| Forêt de Sant Joan de Vilatorrada (42) ⚠️ | Sant Joan de Vilatorrada › Bages | 2 |
| Forêt de Sant Joan de Vilatorrada (45) ⚠️ | Sant Joan de Vilatorrada › Bages | 2 |
| Forêt de Sant Joan de Vilatorrada (50) ⚠️ | Callús › Bages | 2 |
| Forêt de Sant Joan de Vilatorrada (59) ⚠️ | Sant Fruitós de Bages › Bages | 2 |
| Forêt de Cardona (45) ⚠️ | Cardona › Bages | 2 |
| Forêt de Cardona (47) ⚠️ | Cardona › Bages | 2 |
| Forêt de Cardona (52) ⚠️ | Cardona › Bages | 2 |
| Forêt de Cardona (55) ⚠️ | Cardona › Bages | 2 |
| Forêt de Fonollosa (93) ⚠️ | Fonollosa › Bages | 2 |
| Forêt de Fonollosa (97) ⚠️ | Fonollosa › Bages | 2 |
| Forêt de Fonollosa (110) ⚠️ | Fonollosa › Bages | 2 |
| Forêt de Fonollosa (118) ⚠️ | Fonollosa › Bages | 2 |
| Forêt de Fonollosa (129) ⚠️ | Fonollosa › Bages | 2 |
| Forêt de Cerdanyola del Vallès (54) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 2 |
| Forêt de Cerdanyola del Vallès (59) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 2 |
| Parc de Polinyà (19) ⚠️ | Polinyà › Vallès Occidental | 2 |
| Forêt de Seva (13) ⚠️ | Seva › Osona (Barcelone) | 2 |
| Forêt de Seva (15) ⚠️ | Seva › Osona (Barcelone) | 2 |
| Forêt de l'Esquirol (113) ⚠️ | l'Esquirol › Osona (Barcelone) | 2 |
| Forêt de Manresa (100) ⚠️ | Castellgalí › Bages | 2 |
| Forêt de Castellterçol (43) ⚠️ | Castellterçol › Moianès | 2 |
| Forêt de Castellcir (4) ⚠️ | Castellcir › Moianès | 2 |
| Forêt de Castellterçol (47) ⚠️ | Castellcir › Moianès | 2 |
| Forêt de Castellterçol (48) ⚠️ | Castellterçol › Moianès | 2 |
| Forêt de Castellterçol (53) ⚠️ | Castellterçol › Moianès | 2 |
| Forêt de Castellterçol (73) ⚠️ | Castellterçol › Moianès | 2 |
| Forêt de Berga (14) ⚠️ | Berga › Berguedà | 2 |
| Forêt de Olvan (11) ⚠️ | Olvan › Berguedà | 2 |
| Forêt de Cercs (17) ⚠️ | Cercs › Berguedà | 2 |
| Forêt de Berga (53) ⚠️ | Berga › Berguedà | 2 |
| Forêt de Berga (57) ⚠️ | Berga › Berguedà | 2 |
| Forêt de Berga (58) ⚠️ | Berga › Berguedà | 2 |
| Forêt de Terrassa (71) ⚠️ | Terrassa › Vallès Occidental | 2 |
| Forêt de Montgat (3) ⚠️ | Montgat › Maresme | 2 |
| Forêt de Montmajor (33) ⚠️ | l'Espunyola › Berguedà | 2 |
| Forêt de Montmajor (34) ⚠️ | Montmajor › Berguedà | 2 |
| Forêt de l'Espunyola (20) ⚠️ | l'Espunyola › Berguedà | 2 |
| Forêt de Montmajor (39) ⚠️ | Montmajor › Berguedà | 2 |
| Forêt de Montclar (14) ⚠️ | Montclar › Berguedà | 2 |
| Forêt de l'Espunyola (30) ⚠️ | Montclar › Berguedà | 2 |
| Forêt de Montclar (22) ⚠️ | Montclar › Berguedà | 2 |
| Forêt de Montclar (23) ⚠️ | Montclar › Berguedà | 2 |
| Forêt de Manresa (114) ⚠️ | Manresa › Bages | 2 |
| Forêt de Abrera (10) ⚠️ | Sant Esteve Sesrovires › Baix Llobregat | 2 |
| Forêt de Sant Esteve Sesrovires (15) ⚠️ | Sant Esteve Sesrovires › Baix Llobregat | 2 |
| Parc de Sabadell (93) ⚠️ | Sabadell › Vallès Occidental | 2 |
| Forêt de Montmajor (54) ⚠️ | Montmajor › Berguedà | 2 |
| Forêt de Montmajor (55) ⚠️ | Montmajor › Berguedà | 2 |
| Forêt de Montmajor (60) ⚠️ | Montmajor › Berguedà | 2 |
| Forêt de Balsareny (53) ⚠️ | Balsareny › Bages | 2 |
| Forêt de Gaià (13) ⚠️ | Gaià › Bages | 2 |
| Forêt de Gaià (14) ⚠️ | Gaià › Bages | 2 |
| Forêt de Gaià (20) ⚠️ | Gaià › Bages | 2 |
| Forêt de Avinyó (47) ⚠️ | Avinyó › Bages | 2 |
| Forêt de Sallent (73) ⚠️ | Sallent › Bages | 2 |
| Forêt de Oristà (89) ⚠️ | Oristà › Lluçanès | 2 |
| Forêt de Olèrdola (59) ⚠️ | Olèrdola › Alt Penedès | 2 |
| Forêt de Oristà (98) ⚠️ | Oristà › Lluçanès | 2 |
| Forêt de Sant Salvador de Guardiola (26) ⚠️ | Sant Salvador de Guardiola › Bages | 2 |
| Forêt de Sant Salvador de Guardiola (31) ⚠️ | Sant Salvador de Guardiola › Bages | 2 |
| Forêt de Santa Maria d'Oló (23) ⚠️ | Santa Maria d'Oló › Moianès | 2 |
| Forêt de Puig-reig (14) ⚠️ | Puig-reig › Berguedà | 2 |
| Forêt de Puig-reig (18) ⚠️ | Puig-reig › Berguedà | 2 |
| Forêt de Puig-reig (25) ⚠️ | Puig-reig › Berguedà | 2 |
| Forêt de Puig-reig (29) ⚠️ | Puig-reig › Berguedà | 2 |
| Forêt de Puig-reig (34) ⚠️ | Puig-reig › Berguedà | 2 |
| Forêt de Puig-reig (41) ⚠️ | Puig-reig › Berguedà | 2 |
| Forêt de Puig-reig (46) ⚠️ | Puig-reig › Berguedà | 2 |
| Forêt de Oristà (107) ⚠️ | Oristà › Lluçanès | 2 |
| Forêt de Balsareny (72) ⚠️ | Balsareny › Bages | 2 |
| Forêt de Castellnou de Bages (44) ⚠️ | Castellnou de Bages › Bages | 2 |
| Forêt de Castellnou de Bages (45) ⚠️ | Castellnou de Bages › Bages | 2 |
| Forêt de Castellnou de Bages (48) ⚠️ | Castellnou de Bages › Bages | 2 |
| Forêt de Guardiola de Berguedà (20) ⚠️ | Guardiola de Berguedà › Berguedà | 2 |
| Forêt de Sant Pol de Mar (5) ⚠️ | Sant Pol de Mar › Maresme | 2 |
| Forêt de Sant Pol de Mar (12) ⚠️ | Sant Pol de Mar › Maresme | 2 |
| Forêt de Sant Esteve Sesrovires (23) ⚠️ | Sant Esteve Sesrovires › Baix Llobregat | 2 |
| Forêt de Corbera de Llobregat (19) ⚠️ | Corbera de Llobregat › Baix Llobregat | 2 |
| Forêt de Corbera de Llobregat (21) ⚠️ | Corbera de Llobregat › Baix Llobregat | 2 |
| Forêt de Rubí (66) ⚠️ | Rubí › Vallès Occidental | 2 |
| Forêt de Monistrol de Montserrat (14) ⚠️ | Monistrol de Montserrat › Bages | 2 |
| Forêt de Monistrol de Montserrat (15) ⚠️ | Monistrol de Montserrat › Bages | 2 |
| Forêt de Monistrol de Montserrat (18) ⚠️ | Monistrol de Montserrat › Bages | 2 |
| Forêt de Monistrol de Montserrat (23) ⚠️ | Monistrol de Montserrat › Bages | 2 |
| Forêt de Monistrol de Montserrat (26) ⚠️ | Monistrol de Montserrat › Bages | 2 |
| Forêt de Monistrol de Montserrat (27) ⚠️ | Monistrol de Montserrat › Bages | 2 |
| Forêt de Monistrol de Montserrat (34) ⚠️ | Monistrol de Montserrat › Bages | 2 |
| Forêt de Rellinars ⚠️ | Rellinars › Vallès Occidental | 2 |
| Forêt de Vacarisses (31) ⚠️ | Vacarisses › Vallès Occidental | 2 |
| Forêt de Vacarisses (32) ⚠️ | Vacarisses › Vallès Occidental | 2 |
| Forêt de Monistrol de Montserrat (39) ⚠️ | Monistrol de Montserrat › Bages | 2 |
| Forêt de Monistrol de Montserrat (41) ⚠️ | Monistrol de Montserrat › Bages | 2 |
| Forêt de Bagà (8) ⚠️ | Bagà › Berguedà | 2 |
| Forêt de Guardiola de Berguedà (31) ⚠️ | Guardiola de Berguedà › Berguedà | 2 |
| Forêt de Castellbell i el Vilar (18) ⚠️ | Castellbell i el Vilar › Bages | 2 |
| Forêt de Castellbell i el Vilar (26) ⚠️ | Castellbell i el Vilar › Bages | 2 |
| Forêt de Castellbell i el Vilar (27) ⚠️ | Castellbell i el Vilar › Bages | 2 |
| Forêt de Castellbell i el Vilar (28) ⚠️ | Castellbell i el Vilar › Bages | 2 |
| Forêt de Castellbell i el Vilar (29) ⚠️ | Castellbell i el Vilar › Bages | 2 |
| Forêt de Sant Vicenç de Castellet (14) ⚠️ | Sant Vicenç de Castellet › Bages | 2 |
| Forêt de Sant Vicenç de Castellet (15) ⚠️ | Sant Vicenç de Castellet › Bages | 2 |
| Forêt de el Bruc (16) ⚠️ | el Bruc › Anoia | 2 |
| Forêt de Castellbell i el Vilar (41) ⚠️ | Castellbell i el Vilar › Bages | 2 |
| Forêt de Castellbell i el Vilar (46) ⚠️ | Castellbell i el Vilar › Bages | 2 |
| Forêt de Castellbell i el Vilar (47) ⚠️ | Castellbell i el Vilar › Bages | 2 |
| Forêt de Castellolí (13) ⚠️ | Castellolí › Anoia | 2 |
| Forêt de Castellolí (17) ⚠️ | Castellolí › Anoia | 2 |
| Forêt de Castellolí (18) ⚠️ | Castellolí › Anoia | 2 |
| Forêt de Castellolí (22) ⚠️ | Castellolí › Anoia | 2 |
| Forêt de Òdena (37) ⚠️ | Òdena › Anoia | 2 |
| Forêt de Castellbell i el Vilar (48) ⚠️ | Castellbell i el Vilar › Bages | 2 |
| Forêt de Castellbell i el Vilar (49) ⚠️ | Monistrol de Montserrat › Bages | 2 |
| Forêt de Castellbell i el Vilar (58) ⚠️ | Castellbell i el Vilar › Bages | 2 |
| Forêt de Castellbell i el Vilar (61) ⚠️ | Castellbell i el Vilar › Bages | 2 |
| Forêt de Castellbell i el Vilar (64) ⚠️ | Castellbell i el Vilar › Bages | 2 |
| Forêt de Rellinars (6) ⚠️ | Rellinars › Vallès Occidental | 2 |
| Forêt de el Pont de Vilomara i Rocafort (13) ⚠️ | el Pont de Vilomara i Rocafort › Bages | 2 |
| Forêt de Vilanova i la Geltrú (20) ⚠️ | Vilanova i la Geltrú › Garraf | 2 |
| Forêt de Vilanova i la Geltrú (21) ⚠️ | Vilanova i la Geltrú › Garraf | 2 |
| Forêt de Sitges (31) ⚠️ | Sitges › Garraf | 2 |
| Forêt de Sitges (40) ⚠️ | Sitges › Garraf | 2 |
| Forêt de Sitges (43) ⚠️ | Sitges › Garraf | 2 |
| Forêt de Sitges (46) ⚠️ | Sitges › Garraf | 2 |
| Forêt de Gavà (65) ⚠️ | Gavà › Baix Llobregat | 2 |
| Forêt de Sitges (67) ⚠️ | Sitges › Garraf | 2 |
| Forêt de Manresa (130) ⚠️ | Manresa › Bages | 2 |
| Forêt de Castellgalí (19) ⚠️ | Castellgalí › Bages | 2 |
| Forêt de Artés (24) ⚠️ | Artés › Bages | 2 |
| Forêt de Avinyó (64) ⚠️ | Avinyó › Bages | 2 |
| Forêt de Avinyó (66) ⚠️ | Avinyó › Bages | 2 |
| Forêt de Calders (38) ⚠️ | Calders › Moianès | 2 |
| Forêt de Calders (40) ⚠️ | Calders › Moianès | 2 |
| Forêt de Calders (48) ⚠️ | Calders › Moianès | 2 |
| Forêt de Sant Pere de Vilamajor (83) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 2 |
| Forêt de Llinars del Vallès (68) ⚠️ | Llinars del Vallès › Vallès Oriental | 2 |
| Forêt de Sant Antoni de Vilamajor (36) ⚠️ | Sant Antoni de Vilamajor › Vallès Oriental | 2 |
| Forêt de Sant Antoni de Vilamajor (38) ⚠️ | Sant Antoni de Vilamajor › Vallès Oriental | 2 |
| Forêt de Súria (7) ⚠️ | Súria › Bages | 2 |
| Forêt de Súria (17) ⚠️ | Súria › Bages | 2 |
| Forêt de la Garriga (39) ⚠️ | la Garriga › Vallès Oriental | 2 |
| Forêt de la Garriga (42) ⚠️ | la Garriga › Vallès Oriental | 2 |
| Parc de Granollers (24) ⚠️ | Granollers › Vallès Oriental | 2 |
| Forêt de Vallromanes (12) ⚠️ | Vallromanes › Vallès Oriental | 2 |
| Forêt de Gaià (30) ⚠️ | Gaià › Bages | 2 |
| Forêt de Sallent (89) ⚠️ | Sallent › Bages | 2 |
| Forêt de Avinyó (95) ⚠️ | Avinyó › Bages | 2 |
| Forêt de Avinyó (100) ⚠️ | Avinyó › Bages | 2 |
| Forêt de Gaià (40) ⚠️ | Gaià › Bages | 2 |
| Forêt de Gaià (48) ⚠️ | Gaià › Bages | 2 |
| Forêt de Gaià (51) ⚠️ | Gaià › Bages | 2 |
| Forêt de Gaià (55) ⚠️ | Gaià › Bages | 2 |
| Forêt de Sant Esteve de Palautordera (13) ⚠️ | Sant Esteve de Palautordera › Vallès Oriental | 2 |
| Forêt de Vilada (11) ⚠️ | Vilada › Berguedà | 2 |
| Forêt de Castell de l'Areny (24) ⚠️ | Castell de l'Areny › Berguedà | 2 |
| Forêt de Cercs (38) ⚠️ | Cercs › Berguedà | 2 |
| Forêt de Cercs (45) ⚠️ | Cercs › Berguedà | 2 |
| Forêt de Castellar del Riu (17) ⚠️ | Castellar del Riu › Berguedà | 2 |
| Forêt de Sant Quirze de Besora (5) ⚠️ | Sant Quirze de Besora › Osona (Barcelone) | 2 |
| Forêt de Sant Quirze de Besora (6) ⚠️ | Sant Quirze de Besora › Osona (Barcelone) | 2 |
| Forêt de Sora (25) ⚠️ | Montesquiu › Osona (Barcelone) | 2 |
| Forêt de Sant Quirze de Besora (7) ⚠️ | Sant Quirze de Besora › Osona (Barcelone) | 2 |
| Forêt de Sant Quirze de Besora (8) ⚠️ | Sant Quirze de Besora › Osona (Barcelone) | 2 |
| Forêt de Santa Maria de Besora (7) ⚠️ | Santa Maria de Besora › Osona (Barcelone) | 2 |
| Forêt de Guardiola de Berguedà (54) ⚠️ | Guardiola de Berguedà › Berguedà | 2 |
| Forêt de Monistrol de Calders (11) ⚠️ | Monistrol de Calders › Moianès | 2 |
| Forêt de Monistrol de Calders (20) ⚠️ | Monistrol de Calders › Moianès | 2 |
| Forêt de Mura (16) ⚠️ | Mura › Bages | 2 |
| Forêt de Mura (18) ⚠️ | Mura › Bages | 2 |
| Forêt de el Pont de Vilomara i Rocafort (23) ⚠️ | el Pont de Vilomara i Rocafort › Bages | 2 |
| Forêt de Talamanca (20) ⚠️ | Talamanca › Bages | 2 |
| Forêt de Navarcles (16) ⚠️ | Navarcles › Bages | 2 |
| Forêt de Navarcles (17) ⚠️ | Navarcles › Bages | 2 |
| Forêt de Calders (50) ⚠️ | Calders › Moianès | 2 |
| Forêt de Calders (53) ⚠️ | Calders › Moianès | 2 |
| Forêt de Talamanca (36) ⚠️ | Talamanca › Bages | 2 |
| Forêt de Aguilar de Segarra (34) ⚠️ | Aguilar de Segarra › Bages | 2 |
| Forêt de Aguilar de Segarra (38) ⚠️ | Aguilar de Segarra › Bages | 2 |
| Forêt de Aguilar de Segarra (41) ⚠️ | Aguilar de Segarra › Bages | 2 |
| Forêt de Sant Pere Sallavinera (18) ⚠️ | Sant Pere Sallavinera › Anoia | 2 |
| Forêt de Sant Pere Sallavinera (30) ⚠️ | Sant Pere Sallavinera › Anoia | 2 |
| Forêt de Sant Pere Sallavinera (35) ⚠️ | Sant Pere Sallavinera › Anoia | 2 |
| Forêt de Sant Pere Sallavinera (46) ⚠️ | Sant Pere Sallavinera › Anoia | 2 |
| Forêt de Sant Pere Sallavinera (48) ⚠️ | Sant Pere Sallavinera › Anoia | 2 |
| Forêt de Castellbell i el Vilar (69) ⚠️ | Castellbell i el Vilar › Bages | 2 |
| Forêt de Castellbell i el Vilar (71) ⚠️ | Castellbell i el Vilar › Bages | 2 |
| Forêt de els Prats de Rei (19) ⚠️ | els Prats de Rei › Anoia | 2 |
| Forêt de Rajadell (48) ⚠️ | Rajadell › Bages | 2 |
| Forêt de Sant Salvador de Guardiola (65) ⚠️ | Sant Salvador de Guardiola › Bages | 2 |
| Forêt de Sant Salvador de Guardiola (68) ⚠️ | Sant Salvador de Guardiola › Bages | 2 |
| Forêt de Sant Salvador de Guardiola (73) ⚠️ | Sant Salvador de Guardiola › Bages | 2 |
| Forêt de Castellfollit del Boix (24) ⚠️ | Castellfollit del Boix › Bages | 2 |
| Forêt de Castellfollit del Boix (25) ⚠️ | Castellfollit del Boix › Bages | 2 |
| Forêt de Sant Salvador de Guardiola (86) ⚠️ | Sant Salvador de Guardiola › Bages | 2 |
| Forêt de Sant Vicenç de Castellet (35) ⚠️ | Sant Vicenç de Castellet › Bages | 2 |
| Forêt de Sant Salvador de Guardiola (97) ⚠️ | Sant Salvador de Guardiola › Bages | 2 |
| Forêt de Sant Salvador de Guardiola (107) ⚠️ | Sant Salvador de Guardiola › Bages | 2 |
| Forêt de Sant Salvador de Guardiola (109) ⚠️ | Sant Salvador de Guardiola › Bages | 2 |
| Forêt de Sant Salvador de Guardiola (110) ⚠️ | Sant Salvador de Guardiola › Bages | 2 |
| Forêt de Castellgalí (29) ⚠️ | Castellgalí › Bages | 2 |
| Forêt de Sant Vicenç de Castellet (36) ⚠️ | Sant Vicenç de Castellet › Bages | 2 |
| Forêt de Vacarisses (56) ⚠️ | Vacarisses › Vallès Occidental | 2 |
| Forêt de Vacarisses (62) ⚠️ | Vacarisses › Vallès Occidental | 2 |
| Forêt de Olesa de Montserrat (17) ⚠️ | Olesa de Montserrat › Baix Llobregat | 2 |
| Forêt de Olesa de Montserrat (21) ⚠️ | Olesa de Montserrat › Baix Llobregat | 2 |
| Forêt de Olesa de Montserrat (28) ⚠️ | Olesa de Montserrat › Baix Llobregat | 2 |
| Forêt de Olesa de Montserrat (29) ⚠️ | Olesa de Montserrat › Baix Llobregat | 2 |
| Forêt de Olesa de Montserrat (38) ⚠️ | Esparreguera › Baix Llobregat | 2 |
| Forêt de Esparreguera (31) ⚠️ | Esparreguera › Baix Llobregat | 2 |
| Bois de Abrera (3) ⚠️ | Abrera › Baix Llobregat | 2 |
| Forêt de Martorell (8) ⚠️ | Martorell › Baix Llobregat | 2 |
| Forêt de Castellbisbal (16) ⚠️ | Castellbisbal › Vallès Occidental | 2 |
| Forêt de Castellbisbal (17) ⚠️ | Castellbisbal › Vallès Occidental | 2 |
| Forêt de Sant Andreu de la Barca (3) ⚠️ | Sant Andreu de la Barca › Baix Llobregat | 2 |
| Forêt de Castellbisbal (31) ⚠️ | Castellbisbal › Vallès Occidental | 2 |
| Forêt de Castellbisbal (34) ⚠️ | Castellbisbal › Vallès Occidental | 2 |
| Forêt de Castellbisbal (35) ⚠️ | Castellbisbal › Vallès Occidental | 2 |
| Forêt de Castellbisbal (36) ⚠️ | Castellbisbal › Vallès Occidental | 2 |
| Forêt de Castellví de Rosanes (6) ⚠️ | Castellví de Rosanes › Baix Llobregat | 2 |
| Forêt de Castellví de Rosanes (9) ⚠️ | Castellví de Rosanes › Baix Llobregat | 2 |
| Forêt de Castellgalí (38) ⚠️ | Castellgalí › Bages | 2 |
| Forêt de Castellgalí (42) ⚠️ | Castellgalí › Bages | 2 |
| Forêt de Olvan (15) ⚠️ | Olvan › Berguedà | 2 |
| Forêt de Navàs (81) ⚠️ | Navàs › Bages | 2 |
| Forêt de Navàs (89) ⚠️ | Navàs › Bages | 2 |
| Forêt de Puig-reig (53) ⚠️ | Navàs › Bages | 2 |
| Forêt de Puig-reig (58) ⚠️ | Puig-reig › Berguedà | 2 |
| Forêt de Gironella (10) ⚠️ | Gironella › Berguedà | 2 |
| Forêt de Olvan (19) ⚠️ | Olvan › Berguedà | 2 |
| Forêt de Casserres (19) ⚠️ | Casserres › Berguedà | 2 |
| Forêt de Avià (20) ⚠️ | Avià › Berguedà | 2 |
| Forêt de Avià (29) ⚠️ | Avià › Berguedà | 2 |
| Forêt de Avià (31) ⚠️ | Avià › Berguedà | 2 |
| Forêt de Avià (35) ⚠️ | Avià › Berguedà | 2 |
| Forêt de l'Espunyola (52) ⚠️ | l'Espunyola › Berguedà | 2 |
| Forêt de l'Espunyola (56) ⚠️ | l'Espunyola › Berguedà | 2 |
| Forêt de l'Espunyola (59) ⚠️ | l'Espunyola › Berguedà | 2 |
| Forêt de l'Espunyola (62) ⚠️ | l'Espunyola › Berguedà | 2 |
| Forêt de l'Espunyola (76) ⚠️ | l'Espunyola › Berguedà | 2 |
| Forêt de Avià (44) ⚠️ | Avià › Berguedà | 2 |
| Forêt de Capolat (24) ⚠️ | Capolat › Berguedà | 2 |
| Forêt de Castellar del Riu (26) ⚠️ | Castellar del Riu › Berguedà | 2 |
| Forêt de Montmajor (81) ⚠️ | Montmajor › Berguedà | 2 |
| Forêt de Montmajor (91) ⚠️ | Montmajor › Berguedà | 2 |
| Forêt de Montmajor (101) ⚠️ | Montmajor › Berguedà | 2 |
| Forêt de Montmajor (106) ⚠️ | Montmajor › Berguedà | 2 |
| Forêt de Montmajor (108) ⚠️ | Montmajor › Berguedà | 2 |
| Forêt de Navàs (103) ⚠️ | Sant Mateu de Bages › Bages | 2 |
| Forêt de Navàs (116) ⚠️ | Navàs › Bages | 2 |
| Forêt de Navàs (119) ⚠️ | Navàs › Bages | 2 |
| Forêt de Súria (35) ⚠️ | Súria › Bages | 2 |
| Forêt de Cardona (67) ⚠️ | Cardona › Bages | 2 |
| Forêt de Viver i Serrateix (74) ⚠️ | Viver i Serrateix › Berguedà | 2 |
| Forêt de Montclar (36) ⚠️ | Montclar › Berguedà | 2 |
| Forêt de Montmajor (111) ⚠️ | Montmajor › Berguedà | 2 |
| Forêt de Viver i Serrateix (94) ⚠️ | Viver i Serrateix › Berguedà | 2 |
| Forêt de Cardona (68) ⚠️ | Cardona › Bages | 2 |
| Forêt de Montmajor (129) ⚠️ | Montmajor › Berguedà | 2 |
| Forêt de Montmajor (133) ⚠️ | Montmajor › Berguedà | 2 |
| Forêt de Avinyó (113) ⚠️ | Avinyó › Bages | 2 |
| Forêt de Santa Maria de Merlès (29) ⚠️ | Santa Maria de Merlès › Berguedà | 2 |
| Forêt de Santa Maria de Merlès (33) ⚠️ | Santa Maria de Merlès › Berguedà | 2 |
| Forêt de Santa Maria de Merlès (37) ⚠️ | Santa Maria de Merlès › Berguedà | 2 |
| Forêt de Santa Maria de Merlès (40) ⚠️ | Santa Maria de Merlès › Berguedà | 2 |
| Forêt de Santa Maria de Merlès (53) ⚠️ | Santa Maria de Merlès › Berguedà | 2 |
| Forêt de Prats de Lluçanès (6) ⚠️ | Prats de Lluçanès › Lluçanès | 2 |
| Forêt de Santa Maria de Merlès (66) ⚠️ | Santa Maria de Merlès › Berguedà | 2 |
| Forêt de Gurb (18) ⚠️ | Gurb › Osona (Barcelone) | 2 |
| Bois de Molins de Rei (5) ⚠️ | Molins de Rei › Baix Llobregat | 2 |
| Forêt de Sant Cugat del Vallès (138) ⚠️ | Rubí › Vallès Occidental | 2 |
| Forêt de Sant Andreu de la Barca (4) ⚠️ | Corbera de Llobregat › Baix Llobregat | 2 |
| Forêt de Saldes (24) ⚠️ | Saldes › Berguedà | 2 |
| Forêt de Saldes (27) ⚠️ | Saldes › Berguedà | 2 |
| Forêt de Borredà (28) ⚠️ | Borredà › Berguedà | 2 |
| Forêt de Borredà (32) ⚠️ | Borredà › Berguedà | 2 |
| Bois de Viladecavalls (11) ⚠️ | Viladecavalls › Vallès Occidental | 2 |
| Forêt de Jorba (12) ⚠️ | Jorba › Anoia | 2 |
| Forêt de Santa Margarida de Montbui (16) ⚠️ | Santa Margarida de Montbui › Anoia | 2 |
| Forêt de Igualada (6) ⚠️ | Igualada › Anoia | 2 |
| Forêt de Jorba (19) ⚠️ | Jorba › Anoia | 2 |
| Forêt de Jorba (26) ⚠️ | Jorba › Anoia | 2 |
| Forêt de Jorba (33) ⚠️ | Jorba › Anoia | 2 |
| Forêt de Jorba (34) ⚠️ | Jorba › Anoia | 2 |
| Forêt de Òdena (41) ⚠️ | Òdena › Anoia | 2 |
| Forêt de Igualada (14) ⚠️ | Òdena › Anoia | 2 |
| Forêt de la Pobla de Claramunt (15) ⚠️ | la Pobla de Claramunt › Anoia | 2 |
| Forêt de la Pobla de Claramunt (18) ⚠️ | la Pobla de Claramunt › Anoia | 2 |
| Forêt de Santa Margarida de Montbui (18) ⚠️ | Santa Margarida de Montbui › Anoia | 2 |
| Forêt de Vilanova del Camí (16) ⚠️ | Santa Margarida de Montbui › Anoia | 2 |
| Forêt de Jorba (38) ⚠️ | Jorba › Anoia | 2 |
| Forêt de Rajadell (61) ⚠️ | Rajadell › Bages | 2 |
| Forêt de Cubelles (12) ⚠️ | Cubelles › Garraf | 2 |
| Forêt de Cubelles (16) ⚠️ | Cubelles › Garraf | 2 |
| Forêt de Castellet i la Gornal (73) ⚠️ | Castellet i la Gornal › Alt Penedès | 2 |
| Forêt de Sitges (69) ⚠️ | Sitges › Garraf | 2 |
| Forêt de Sitges (72) ⚠️ | Sitges › Garraf | 2 |
| Forêt de Olivella (55) ⚠️ | Olivella › Garraf | 2 |
| Forêt de Olivella (62) ⚠️ | Olivella › Garraf | 2 |
| Forêt de Olivella (64) ⚠️ | Olivella › Garraf | 2 |
| Forêt de Olivella (71) ⚠️ | Olivella › Garraf | 2 |
| Forêt de Olivella (74) ⚠️ | Olivella › Garraf | 2 |
| Forêt de Olivella (80) ⚠️ | Olivella › Garraf | 2 |
| Forêt de Begues (45) ⚠️ | Begues › Baix Llobregat | 2 |
| Forêt de Begues (51) ⚠️ | Begues › Baix Llobregat | 2 |
| Forêt de Begues (63) ⚠️ | Begues › Baix Llobregat | 2 |
| Forêt de Begues (66) ⚠️ | Begues › Baix Llobregat | 2 |
| Forêt de Olivella (87) ⚠️ | Olivella › Garraf | 2 |
| Forêt de Olivella (88) ⚠️ | Olivella › Garraf | 2 |
| Forêt de Olivella (95) ⚠️ | Olivella › Garraf | 2 |
| Forêt de Olivella (104) ⚠️ | Olivella › Garraf | 2 |
| Forêt de Olesa de Bonesvalls (47) ⚠️ | Olesa de Bonesvalls › Alt Penedès | 2 |
| Forêt de Olivella (118) ⚠️ | Olivella › Garraf | 2 |
| Forêt de Sant Pere de Ribes (88) ⚠️ | Sant Pere de Ribes › Garraf | 2 |
| Forêt de Olivella (122) ⚠️ | Olivella › Garraf | 2 |
| Forêt de Sant Pere de Ribes (99) ⚠️ | Sant Pere de Ribes › Garraf | 2 |
| Forêt de Sitges (74) ⚠️ | Sitges › Garraf | 2 |
| Forêt de Sitges (80) ⚠️ | Sitges › Garraf | 2 |
| Forêt de Sitges (82) ⚠️ | Sitges › Garraf | 2 |
| Forêt de Sitges (84) ⚠️ | Sitges › Garraf | 2 |
| Forêt de Sitges (87) ⚠️ | Sitges › Garraf | 2 |
| Forêt de Vilanova i la Geltrú (34) ⚠️ | Vilanova i la Geltrú › Garraf | 2 |
| Forêt de Santa Margarida i els Monjos (32) ⚠️ | Santa Margarida i els Monjos › Alt Penedès | 2 |
| Forêt de Olèrdola (64) ⚠️ | Olèrdola › Alt Penedès | 2 |
| Forêt de Olèrdola (67) ⚠️ | Olèrdola › Alt Penedès | 2 |
| Forêt de Vilanova i la Geltrú (41) ⚠️ | Vilanova i la Geltrú › Garraf | 2 |
| Forêt de Sant Pere de Ribes (109) ⚠️ | Sant Pere de Ribes › Garraf | 2 |
| Forêt de Vilanova i la Geltrú (47) ⚠️ | Vilanova i la Geltrú › Garraf | 2 |
| Forêt de Vilanova i la Geltrú (48) ⚠️ | Vilanova i la Geltrú › Garraf | 2 |
| Forêt de Sant Pere de Ribes (111) ⚠️ | Sant Pere de Ribes › Garraf | 2 |
| Forêt de Vilanova i la Geltrú (57) ⚠️ | Vilanova i la Geltrú › Garraf | 2 |
| Forêt de Vilanova i la Geltrú (64) ⚠️ | Vilanova i la Geltrú › Garraf | 2 |
| Forêt de Canyelles (23) ⚠️ | Canyelles › Garraf | 2 |
| Forêt de Avinyonet del Penedès (68) ⚠️ | Avinyonet del Penedès › Alt Penedès | 2 |
| Forêt de Molins de Rei (10) ⚠️ | Molins de Rei › Baix Llobregat | 2 |
| Forêt de Sant Julià de Cerdanyola (4) ⚠️ | Sant Julià de Cerdanyola › Berguedà | 2 |
| Bois de Viladecavalls (15) ⚠️ | Viladecavalls › Vallès Occidental | 2 |
| Forêt de Viladecavalls (14) ⚠️ | Ullastrell › Vallès Occidental | 2 |
| Forêt de Bagà (28) ⚠️ | Bagà › Berguedà | 2 |
| Forêt de Tavertet (31) ⚠️ | Tavertet › Osona (Barcelone) | 2 |
| Forêt de Viver i Serrateix (98) ⚠️ | Viver i Serrateix › Berguedà | 2 |
| Forêt de Viver i Serrateix (103) ⚠️ | Viver i Serrateix › Berguedà | 2 |
| Forêt de Viver i Serrateix (104) ⚠️ | Viver i Serrateix › Berguedà | 2 |
| Forêt de Viver i Serrateix (108) ⚠️ | Viver i Serrateix › Berguedà | 2 |
| Forêt de Santa Maria de Merlès (73) ⚠️ | Santa Maria de Merlès › Berguedà | 2 |
| Forêt de Viver i Serrateix (117) ⚠️ | Viver i Serrateix › Berguedà | 2 |
| Forêt de Viver i Serrateix (119) ⚠️ | Viver i Serrateix › Berguedà | 2 |
| Forêt de Santa Maria d'Oló (42) ⚠️ | Santa Maria d'Oló › Moianès | 2 |
| Forêt de Santa Maria d'Oló (49) ⚠️ | Santa Maria d'Oló › Moianès | 2 |
| Forêt de Sant Jaume de Frontanyà (15) ⚠️ | Sant Jaume de Frontanyà › Berguedà | 2 |
| Forêt de Borredà (47) ⚠️ | Borredà › Berguedà | 2 |
| Forêt de Borredà (51) ⚠️ | Borredà › Berguedà | 2 |
| Forêt de Borredà (55) ⚠️ | Borredà › Berguedà | 2 |
| Forêt de Borredà (57) ⚠️ | Borredà › Berguedà | 2 |
| Forêt de Avinyó (116) ⚠️ | Avinyó › Bages | 2 |
| Forêt de Santa Maria de Merlès (97) ⚠️ | Santa Maria de Merlès › Berguedà | 2 |
| Forêt de Santa Maria de Merlès (101) ⚠️ | Santa Maria de Merlès › Berguedà | 2 |
| Forêt de Santa Maria de Merlès (123) ⚠️ | Santa Maria de Merlès › Berguedà | 2 |
| Forêt de el Papiol (9) ⚠️ | el Papiol › Baix Llobregat | 2 |
| Forêt de Aguilar de Segarra (50) ⚠️ | Aguilar de Segarra › Bages | 2 |
| Forêt de Sant Pere Sallavinera (63) ⚠️ | Sant Pere Sallavinera › Anoia | 2 |
| Forêt de Sant Pere Sallavinera (64) ⚠️ | Sant Pere Sallavinera › Anoia | 2 |
| Forêt de Aguilar de Segarra (54) ⚠️ | Aguilar de Segarra › Bages | 2 |
| Forêt de els Prats de Rei (31) ⚠️ | Aguilar de Segarra › Bages | 2 |
| Forêt de Rupit i Pruit (22) ⚠️ | Rupit i Pruit › Osona (Barcelone) | 2 |
| Forêt de Rupit i Pruit (25) ⚠️ | Rupit i Pruit › Osona (Barcelone) | 2 |
| Forêt de Avià (47) ⚠️ | Avià › Berguedà | 2 |
| Forêt de Avià (51) ⚠️ | Avià › Berguedà | 2 |
| Forêt de Avià (52) ⚠️ | Avià › Berguedà | 2 |
| Forêt de Avià (53) ⚠️ | Avià › Berguedà | 2 |
| Forêt de Avià (57) ⚠️ | Avià › Berguedà | 2 |
| Forêt de Collbató (15) ⚠️ | Collbató › Baix Llobregat | 2 |
| Forêt de Collbató (16) ⚠️ | Collbató › Baix Llobregat | 2 |
| Forêt de Esparreguera (35) ⚠️ | Esparreguera › Baix Llobregat | 2 |
| Forêt de Esparreguera (36) ⚠️ | Esparreguera › Baix Llobregat | 2 |
| Forêt de Collbató (17) ⚠️ | Collbató › Baix Llobregat | 2 |
| Parc de Sitges (28) ⚠️ | Sitges › Garraf | 2 |
| Forêt de Monistrol de Calders (30) ⚠️ | Monistrol de Calders › Moianès | 2 |
| Forêt de Granera (23) ⚠️ | Granera › Moianès | 2 |
| Forêt de Granera (26) ⚠️ | Granera › Moianès | 2 |
| Forêt de la Garriga (47) ⚠️ | la Garriga › Vallès Oriental | 2 |
| Forêt de la Garriga (49) ⚠️ | la Garriga › Vallès Oriental | 2 |
| Forêt de Aiguafreda (13) ⚠️ | Aiguafreda › Osona (Barcelone) | 2 |
| Forêt de Tagamanent (23) ⚠️ | Tagamanent › Vallès Oriental | 2 |
| Forêt de Centelles (14) ⚠️ | Centelles › Osona (Barcelone) | 2 |
| Forêt de Centelles (15) ⚠️ | Centelles › Osona (Barcelone) | 2 |
| Forêt de Centelles (23) ⚠️ | Centelles › Osona (Barcelone) | 2 |
| Forêt de l'Estany (5) ⚠️ | l'Estany › Moianès | 2 |
| Forêt de Tagamanent (25) ⚠️ | Tagamanent › Vallès Oriental | 2 |
| Forêt de Tagamanent (27) ⚠️ | Tagamanent › Vallès Oriental | 2 |
| Forêt de el Brull (26) ⚠️ | el Brull › Osona (Barcelone) | 2 |
| Forêt de Fogars de Montclús (16) ⚠️ | Fogars de Montclús › Vallès Oriental | 2 |
| Forêt de l'Ametlla del Vallès (18) ⚠️ | l'Ametlla del Vallès › Vallès Oriental | 2 |
| Forêt de el Brull (41) ⚠️ | el Brull › Osona (Barcelone) | 2 |
| Forêt de Castellcir (8) ⚠️ | Castellcir › Moianès | 2 |
| Forêt de Castellcir (9) ⚠️ | Castellcir › Moianès | 2 |
| Forêt de Sant Quirze Safaja (25) ⚠️ | Sant Quirze Safaja › Moianès | 2 |
| Forêt de Castellterçol (79) ⚠️ | Castellterçol › Moianès | 2 |
| Forêt de Sant Quirze Safaja (39) ⚠️ | Sant Quirze Safaja › Moianès | 2 |
| Forêt de Bigues i Riells del Fai (25) ⚠️ | Bigues i Riells del Fai › Vallès Oriental | 2 |
| Forêt de Sant Quirze Safaja (41) ⚠️ | Sant Quirze Safaja › Moianès | 2 |
| Forêt de Sant Quirze Safaja (48) ⚠️ | Sant Quirze Safaja › Moianès | 2 |
| Forêt de Monistrol de Calders (42) ⚠️ | Monistrol de Calders › Moianès | 2 |
| Forêt de Vic (34) ⚠️ | Vic › Osona (Barcelone) | 2 |
| Forêt de Santa Maria d'Oló (80) ⚠️ | Santa Maria d'Oló › Moianès | 2 |
| Forêt de Oristà (123) ⚠️ | Oristà › Lluçanès | 2 |
| Forêt de Oristà (127) ⚠️ | Oristà › Lluçanès | 2 |
| Forêt de Oristà (129) ⚠️ | Oristà › Lluçanès | 2 |
| Forêt de Oristà (132) ⚠️ | Oristà › Lluçanès | 2 |
| Forêt de Oristà (146) ⚠️ | Oristà › Lluçanès | 2 |
| Forêt de Sant Mateu de Bages (55) ⚠️ | Sant Mateu de Bages › Bages | 2 |
| Forêt de Sant Mateu de Bages (69) ⚠️ | Sant Mateu de Bages › Bages | 2 |
| Forêt de Sant Mateu de Bages (70) ⚠️ | Sant Mateu de Bages › Bages | 2 |
| Forêt de Sant Mateu de Bages (74) ⚠️ | Sant Mateu de Bages › Bages | 2 |
| Forêt de Sant Mateu de Bages (75) ⚠️ | Sant Mateu de Bages › Bages | 2 |
| Forêt de Navàs (157) ⚠️ | Navàs › Bages | 2 |
| Forêt de Cardona (77) ⚠️ | Cardona › Bages | 2 |
| Forêt de Cardona (82) ⚠️ | Cardona › Bages | 2 |
| Forêt de Cardona (87) ⚠️ | Cardona › Bages | 2 |
| Forêt de Cardona (92) ⚠️ | Cardona › Bages | 2 |
| Forêt de Sant Mateu de Bages (77) ⚠️ | Sant Mateu de Bages › Bages | 2 |
| Forêt de Cardona (101) ⚠️ | Cardona › Bages | 2 |
| Forêt de Sant Mateu de Bages (88) ⚠️ | Sant Mateu de Bages › Bages | 2 |
| Forêt de Sant Mateu de Bages (91) ⚠️ | Sant Mateu de Bages › Bages | 2 |
| Forêt de Sant Mateu de Bages (92) ⚠️ | Sant Mateu de Bages › Bages | 2 |
| Forêt de Sant Mateu de Bages (95) ⚠️ | Sant Mateu de Bages › Bages | 2 |
| Forêt de Sant Mateu de Bages (96) ⚠️ | Sant Mateu de Bages › Bages | 2 |
| Forêt de Sant Mateu de Bages (97) ⚠️ | Sant Mateu de Bages › Bages | 2 |
| Forêt de Calonge de Segarra (15) ⚠️ | Calonge de Segarra › Anoia | 2 |
| Forêt de Calonge de Segarra (16) ⚠️ | Calonge de Segarra › Anoia | 2 |
| Forêt de Sallent (98) ⚠️ | Sallent › Bages | 2 |
| Forêt de les Franqueses del Vallès (54) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 2 |
| Forêt de Sant Pere de Vilamajor (92) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 2 |
| Forêt de Sant Pere de Vilamajor (93) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 2 |
| Forêt de Sant Pere de Vilamajor (95) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 2 |
| Forêt de Guardiola de Berguedà (69) ⚠️ | Guardiola de Berguedà › Berguedà | 2 |
| Forêt de Lluçà (13) ⚠️ | Lluçà › Lluçanès | 2 |
| Forêt de la Garriga (56) ⚠️ | la Garriga › Vallès Oriental | 2 |
| Forêt de les Franqueses del Vallès (64) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 2 |
| Bois de les Franqueses del Vallès (6) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 2 |
| Parc de la Garriga (11) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 2 |
| Forêt de Dosrius (12) ⚠️ | Dosrius › Maresme | 2 |
| Forêt de Dosrius (14) ⚠️ | Dosrius › Maresme | 2 |
| Forêt de Dosrius (33) ⚠️ | Dosrius › Maresme | 2 |
| Bosc del torrent de Fangues ⚠️ | Canovelles › Vallès Oriental | 2 |
| Forêt de Balenyà (13) ⚠️ | Balenyà › Osona (Barcelone) | 2 |
| Forêt de Balenyà (16) ⚠️ | Balenyà › Osona (Barcelone) | 2 |
| Forêt de Tona (5) ⚠️ | Tona › Osona (Barcelone) | 2 |
| Forêt de Tona (11) ⚠️ | Tona › Osona (Barcelone) | 2 |
| Forêt de Balenyà (22) ⚠️ | Balenyà › Osona (Barcelone) | 2 |
| Forêt de Balenyà (25) ⚠️ | Balenyà › Osona (Barcelone) | 2 |
| Forêt de Tona (18) ⚠️ | Tona › Osona (Barcelone) | 2 |
| Forêt de Tona (19) ⚠️ | Tona › Osona (Barcelone) | 2 |
| Forêt de Tona (21) ⚠️ | Tona › Osona (Barcelone) | 2 |
| Forêt de Muntanyola (33) ⚠️ | Muntanyola › Osona (Barcelone) | 2 |
| Forêt de Tona (34) ⚠️ | Tona › Osona (Barcelone) | 2 |
| Forêt de Malla (6) ⚠️ | Malla › Osona (Barcelone) | 2 |
| Forêt de Malla (8) ⚠️ | Malla › Osona (Barcelone) | 2 |
| Forêt de Seva (25) ⚠️ | Seva › Osona (Barcelone) | 2 |
| Forêt de Malla (11) ⚠️ | Malla › Osona (Barcelone) | 2 |
| Forêt de Tona (40) ⚠️ | Tona › Osona (Barcelone) | 2 |
| Forêt de Sant Antoni de Vilamajor (45) ⚠️ | Sant Antoni de Vilamajor › Vallès Oriental | 2 |
| Forêt de Saldes (31) ⚠️ | Saldes › Berguedà | 2 |
| Forêt de Gisclareny (28) ⚠️ | Gisclareny › Berguedà | 2 |
| Forêt de Saldes (71) ⚠️ | Saldes › Berguedà | 2 |
| Forêt de Olvan (24) ⚠️ | Olvan › Berguedà | 2 |
| Forêt de Olvan (25) ⚠️ | Olvan › Berguedà | 2 |
| Forêt de Olvan (27) ⚠️ | Olvan › Berguedà | 2 |
| Forêt de Olvan (29) ⚠️ | Olvan › Berguedà | 2 |
| Forêt de Sagàs (46) ⚠️ | Sagàs › Berguedà | 2 |
| Forêt de Bagà (37) ⚠️ | Bagà › Berguedà | 2 |
| Forêt de Guardiola de Berguedà (74) ⚠️ | Guardiola de Berguedà › Berguedà | 2 |
| Forêt de Guardiola de Berguedà (78) ⚠️ | Guardiola de Berguedà › Berguedà | 2 |
| Forêt de Guardiola de Berguedà (84) ⚠️ | Guardiola de Berguedà › Berguedà | 2 |
| Forêt de Guardiola de Berguedà (87) ⚠️ | Guardiola de Berguedà › Berguedà | 2 |
| Forêt de Guardiola de Berguedà (95) ⚠️ | Guardiola de Berguedà › Berguedà | 2 |
| Forêt de Guardiola de Berguedà (103) ⚠️ | Guardiola de Berguedà › Berguedà | 2 |
| Forêt de Guardiola de Berguedà (106) ⚠️ | Guardiola de Berguedà › Berguedà | 2 |
| Forêt de Bagà (67) ⚠️ | Bagà › Berguedà | 2 |
| Forêt de Vallcebre (25) ⚠️ | Vallcebre › Berguedà | 2 |
| Forêt de Vallcebre (26) ⚠️ | Vallcebre › Berguedà | 2 |
| Forêt de Vallcebre (27) ⚠️ | Vallcebre › Berguedà | 2 |
| Forêt de Capolat (33) ⚠️ | Capolat › Berguedà | 2 |
| Forêt de Castellar del Riu (30) ⚠️ | Capolat › Berguedà | 2 |
| Forêt de Capolat (43) ⚠️ | Capolat › Berguedà | 2 |
| Forêt de Capolat (47) ⚠️ | Capolat › Berguedà | 2 |
| Forêt de Castellar del Riu (38) ⚠️ | Castellar del Riu › Berguedà | 2 |
| Forêt de Castellar del Riu (46) ⚠️ | Castellar del Riu › Berguedà | 2 |
| Forêt de Fígols (27) ⚠️ | Fígols › Berguedà | 2 |
| Forêt de Fígols (29) ⚠️ | Fígols › Berguedà | 2 |
| Forêt de Prats de Lluçanès (10) ⚠️ | Prats de Lluçanès › Lluçanès | 2 |
| Forêt de Prats de Lluçanès (13) ⚠️ | Prats de Lluçanès › Lluçanès | 2 |
| Forêt de Prats de Lluçanès (21) ⚠️ | Prats de Lluçanès › Lluçanès | 2 |
| Forêt de Prats de Lluçanès (25) ⚠️ | Prats de Lluçanès › Lluçanès | 2 |
| Forêt de Lluçà (18) ⚠️ | Lluçà › Lluçanès | 2 |
| Forêt de Lluçà (22) ⚠️ | Lluçà › Lluçanès | 2 |
| Forêt de Borredà (66) ⚠️ | Borredà › Berguedà | 2 |
| Forêt de Borredà (83) ⚠️ | Borredà › Berguedà | 2 |
| Forêt de Lluçà (48) ⚠️ | Lluçà › Lluçanès | 2 |
| Forêt de Lluçà (50) ⚠️ | Lluçà › Lluçanès | 2 |
| Forêt de Sagàs (50) ⚠️ | Sagàs › Berguedà | 2 |
| Forêt de la Quar (45) ⚠️ | la Quar › Berguedà | 2 |
| Forêt de Borredà (98) ⚠️ | Borredà › Berguedà | 2 |
| Forêt de Borredà (99) ⚠️ | Borredà › Berguedà | 2 |
| Forêt de Cardedeu (37) ⚠️ | Cardedeu › Vallès Oriental | 2 |
| Forêt de Borredà (112) ⚠️ | Borredà › Berguedà | 2 |
| Forêt de Borredà (116) ⚠️ | Borredà › Berguedà | 2 |
| Forêt de Borredà (127) ⚠️ | Borredà › Berguedà | 2 |
| Forêt de la Pobla de Lillet (37) ⚠️ | la Pobla de Lillet › Berguedà | 2 |
| Forêt de Saldes (74) ⚠️ | Saldes › Berguedà | 2 |
| Forêt de Saldes (75) ⚠️ | Saldes › Berguedà | 2 |
| Forêt de Gisclareny (60) ⚠️ | Gisclareny › Berguedà | 2 |
| Forêt de Castellar del Riu (58) ⚠️ | Castellar del Riu › Berguedà | 2 |
| Forêt de Castellar del Riu (59) ⚠️ | Castellar del Riu › Berguedà | 2 |
| Forêt de Castellar del Riu (71) ⚠️ | Castellar del Riu › Berguedà | 2 |
| Forêt de Castellar del Riu (75) ⚠️ | Castellar del Riu › Berguedà | 2 |
| Forêt de Cercs (57) ⚠️ | Cercs › Berguedà | 2 |
| Forêt de Castellar del Riu (76) ⚠️ | Castellar del Riu › Berguedà | 2 |
| Forêt de Fígols (37) ⚠️ | Fígols › Berguedà | 2 |
| Forêt de Saldes (89) ⚠️ | Saldes › Berguedà | 2 |
| Forêt de Saldes (91) ⚠️ | Saldes › Berguedà | 2 |
| Forêt de Sentmenat (12) ⚠️ | Sentmenat › Vallès Occidental | 2 |
| Forêt de les Franqueses del Vallès (78) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 2 |
| Forêt de Gisclareny (61) ⚠️ | Gisclareny › Berguedà | 2 |
| Forêt de Gisclareny (64) ⚠️ | Gisclareny › Berguedà | 2 |
| Forêt de Gisclareny (65) ⚠️ | Gisclareny › Berguedà | 2 |
| Forêt de Sant Antoni de Vilamajor (48) ⚠️ | Sant Antoni de Vilamajor › Vallès Oriental | 2 |
| Forêt de Saldes (103) ⚠️ | Saldes › Berguedà | 2 |
| Forêt de Saldes (107) ⚠️ | Saldes › Berguedà | 2 |
| Forêt de Saldes (108) ⚠️ | Saldes › Berguedà | 2 |
| Forêt de Puig-reig (82) ⚠️ | Puig-reig › Berguedà | 2 |
| Forêt de Puig-reig (86) ⚠️ | Puig-reig › Berguedà | 2 |
| Forêt de Saldes (111) ⚠️ | Saldes › Berguedà | 2 |
| Forêt de Saldes (115) ⚠️ | Saldes › Berguedà | 2 |
| Forêt de Vallcebre (43) ⚠️ | Vallcebre › Berguedà | 2 |
| Forêt de Saldes (124) ⚠️ | Saldes › Berguedà | 2 |
| Forêt de Collsuspina (13) ⚠️ | Collsuspina › Moianès | 2 |
| Forêt de Montesquiu (10) ⚠️ | Montesquiu › Osona (Barcelone) | 2 |
| Forêt de Montesquiu (11) ⚠️ | Montesquiu › Osona (Barcelone) | 2 |
| Forêt de Sant Vicenç de Torelló (4) ⚠️ | Sant Vicenç de Torelló › Osona (Barcelone) | 2 |
| Forêt de Orís (26) ⚠️ | Orís › Osona (Barcelone) | 2 |
| Forêt de Vilanova de Sau (39) ⚠️ | Vilanova de Sau › Osona (Barcelone) | 2 |
| Forêt de Sant Sadurní d'Osormort (23) ⚠️ | Sant Sadurní d'Osormort › Osona (Barcelone) | 2 |
| Forêt de Vilanova de Sau (43) ⚠️ | Vilanova de Sau › Osona (Barcelone) | 2 |
| Forêt de Vilanova de Sau (44) ⚠️ | Vilanova de Sau › Osona (Barcelone) | 2 |
| Forêt de Vilanova de Sau (49) ⚠️ | Vilanova de Sau › Osona (Barcelone) | 2 |
| Forêt de Vilanova de Sau (51) ⚠️ | Vilanova de Sau › Osona (Barcelone) | 2 |
| Forêt de Vilanova de Sau (52) ⚠️ | Vilanova de Sau › Osona (Barcelone) | 2 |
| Forêt de les Masies de Roda (7) ⚠️ | les Masies de Roda › Osona (Barcelone) | 2 |
| Forêt de les Masies de Roda (8) ⚠️ | les Masies de Roda › Osona (Barcelone) | 2 |
| Forêt de Sant Martí Sarroca (31) ⚠️ | Sant Martí Sarroca › Alt Penedès | 2 |
| Forêt de Sant Martí Sarroca (36) ⚠️ | Sant Martí Sarroca › Alt Penedès | 2 |
| Forêt de Pontons (6) ⚠️ | Pontons › Alt Penedès | 2 |
| Forêt de Tordera (60) ⚠️ | Tordera › Maresme | 2 |
| Forêt de Tordera (74) ⚠️ | Tordera › Maresme | 2 |
| Forêt de Fogars de la Selva (12) ⚠️ | Fogars de la Selva › la Selva (Barcelone) | 2 |
| Forêt de Fogars de la Selva (15) ⚠️ | Fogars de la Selva › la Selva (Barcelone) | 2 |
| Forêt de Tordera (84) ⚠️ | Tordera › Maresme | 2 |
| Forêt de Tordera (86) ⚠️ | Tordera › Maresme | 2 |
| Forêt de Tordera (95) ⚠️ | Tordera › Maresme | 2 |
| Forêt de Montornès del Vallès (11) ⚠️ | Montornès del Vallès › Vallès Oriental | 2 |
| Parc de Montornès del Vallès (5) ⚠️ | Montornès del Vallès › Vallès Oriental | 2 |
| Forêt de Martorelles (2) ⚠️ | Martorelles › Vallès Oriental | 2 |
| Forêt de Vilanova del Vallès (14) ⚠️ | Vilanova del Vallès › Vallès Oriental | 2 |
| Forêt de la Roca del Vallès (21) ⚠️ | la Roca del Vallès › Vallès Oriental | 2 |
| Forêt de la Roca del Vallès (27) ⚠️ | la Roca del Vallès › Vallès Oriental | 2 |
| Forêt de Llinars del Vallès (79) ⚠️ | Llinars del Vallès › Vallès Oriental | 2 |
| Forêt de Llinars del Vallès (82) ⚠️ | Llinars del Vallès › Vallès Oriental | 2 |
| Forêt de Llinars del Vallès (83) ⚠️ | Cardedeu › Vallès Oriental | 2 |
| Forêt de la Roca del Vallès (29) ⚠️ | la Roca del Vallès › Vallès Oriental | 2 |
| Forêt de la Llagosta ⚠️ | la Llagosta › Vallès Oriental | 2 |
| Forêt de Alella (7) ⚠️ | Alella › Maresme | 2 |
| Forêt de Vallcebre (49) ⚠️ | Vallcebre › Berguedà | 2 |
| Forêt de Vallcebre (52) ⚠️ | Vallcebre › Berguedà | 2 |
| Forêt de Vallcebre (53) ⚠️ | Vallcebre › Berguedà | 2 |
| Forêt de Vallcebre (57) ⚠️ | Vallcebre › Berguedà | 2 |
| Forêt de Vallcebre (59) ⚠️ | Vallcebre › Berguedà | 2 |
| Forêt de Torrelles de Llobregat (169) ⚠️ | Torrelles de Llobregat › Baix Llobregat | 2 |
| Forêt de Guardiola de Berguedà (128) ⚠️ | Guardiola de Berguedà › Berguedà | 2 |
| Forêt de Castellar de n'Hug (24) ⚠️ | Castellar de n'Hug › Berguedà | 2 |
| Forêt de Guardiola de Berguedà (133) ⚠️ | Guardiola de Berguedà › Berguedà | 2 |
| Forêt de Piera (32) ⚠️ | Piera › Anoia | 2 |
| Forêt de Castellolí (33) ⚠️ | Castellolí › Anoia | 2 |
| Forêt de Òdena (52) ⚠️ | Òdena › Anoia | 2 |
| Forêt de Òdena (54) ⚠️ | Òdena › Anoia | 2 |
| Forêt de Sant Martí de Tous (16) ⚠️ | Sant Martí de Tous › Anoia | 2 |
| Forêt de Sant Martí de Tous (20) ⚠️ | Sant Martí de Tous › Anoia | 2 |
| Forêt de Sant Martí de Tous (21) ⚠️ | Sant Martí de Tous › Anoia | 2 |
| Forêt de Sant Martí de Tous (23) ⚠️ | Sant Martí de Tous › Anoia | 2 |
| Forêt de Sant Martí de Tous (24) ⚠️ | Sant Martí de Tous › Anoia | 2 |
| Forêt de Sant Martí de Tous (25) ⚠️ | Sant Martí de Tous › Anoia | 2 |
| Forêt de Sant Martí de Tous (28) ⚠️ | Sant Martí de Tous › Anoia | 2 |
| Forêt de Sant Martí de Tous (31) ⚠️ | Sant Martí de Tous › Anoia | 2 |
| Forêt de Santa Margarida de Montbui (24) ⚠️ | Santa Margarida de Montbui › Anoia | 2 |
| Forêt de Santa Margarida de Montbui (32) ⚠️ | Santa Margarida de Montbui › Anoia | 2 |
| Forêt de Santa Margarida de Montbui (34) ⚠️ | Santa Margarida de Montbui › Anoia | 2 |
| Forêt de Santa Margarida de Montbui (36) ⚠️ | Santa Margarida de Montbui › Anoia | 2 |
| Forêt de Santa Margarida de Montbui (41) ⚠️ | Santa Margarida de Montbui › Anoia | 2 |
| Forêt de Sant Martí de Tous (34) ⚠️ | Sant Martí de Tous › Anoia | 2 |
| Forêt de Argençola (35) ⚠️ | Argençola › Anoia | 2 |
| Forêt de Jorba (45) ⚠️ | Jorba › Anoia | 2 |
| Forêt de Sant Martí de Tous (41) ⚠️ | Sant Martí de Tous › Anoia | 2 |
| Forêt de Sant Martí de Tous (42) ⚠️ | Sant Martí de Tous › Anoia | 2 |
| Forêt de Sant Martí de Tous (45) ⚠️ | Sant Martí de Tous › Anoia | 2 |
| Forêt de Moià (46) ⚠️ | Moià › Moianès | 2 |
| Forêt de Moià (48) ⚠️ | Moià › Moianès | 2 |
| Forêt de Moià (50) ⚠️ | Moià › Moianès | 2 |
| Forêt de Sant Feliu Sasserra (21) ⚠️ | Sant Feliu Sasserra › Bages | 2 |
| Forêt de Sant Feliu Sasserra (22) ⚠️ | Sant Feliu Sasserra › Bages | 2 |
| Forêt de Sant Feliu Sasserra (31) ⚠️ | Sant Feliu Sasserra › Bages | 2 |
| Forêt de Castellar de n'Hug (32) ⚠️ | Castellar de n'Hug › Berguedà | 2 |
| Forêt de Castellar de n'Hug (39) ⚠️ | Castellar de n'Hug › Berguedà | 2 |
| Forêt de Castellar de n'Hug (49) ⚠️ | Castellar de n'Hug › Berguedà | 2 |
| Forêt de Oristà (161) ⚠️ | Oristà › Lluçanès | 2 |
| Forêt de Oristà (165) ⚠️ | Oristà › Lluçanès | 2 |
| Forêt de Vilanova del Camí (22) ⚠️ | Vilanova del Camí › Anoia | 2 |
| Forêt de Òdena (69) ⚠️ | Òdena › Anoia | 2 |
| Forêt de Òdena (71) ⚠️ | Òdena › Anoia | 2 |
| Forêt de Òdena (79) ⚠️ | Òdena › Anoia | 2 |
| Forêt de Carme ⚠️ | Carme › Anoia | 2 |
| Forêt de Orpí (4) ⚠️ | Orpí › Anoia | 2 |
| Forêt de Carme (5) ⚠️ | Carme › Anoia | 2 |
| Forêt de Carme (8) ⚠️ | Carme › Anoia | 2 |
| Forêt de Piera (37) ⚠️ | Piera › Anoia | 2 |
| Forêt de Sant Quirze del Vallès (16) ⚠️ | Sant Quirze del Vallès › Vallès Occidental | 2 |
| Bois de Sant Quirze del Vallès (9) ⚠️ | Sant Quirze del Vallès › Vallès Occidental | 2 |
| Forêt de Begues (81) ⚠️ | Begues › Baix Llobregat | 2 |
| Forêt de Viladecavalls (18) ⚠️ | Viladecavalls › Vallès Occidental | 2 |
| Forêt de Montmajor (139) ⚠️ | Montmajor › Berguedà | 2 |
| Forêt de Cardona (114) ⚠️ | Cardona › Bages | 2 |
| Forêt de Saldes (136) ⚠️ | Saldes › Berguedà | 2 |
| Forêt de el Papiol (11) ⚠️ | el Papiol › Baix Llobregat | 2 |
| Bois de Sant Cugat del Vallès (128) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 2 |
| Forêt de Martorell (31) ⚠️ | Martorell › Baix Llobregat | 2 |
| Forêt de Martorell (38) ⚠️ | Martorell › Baix Llobregat | 2 |
| Forêt de Martorell (40) ⚠️ | Martorell › Baix Llobregat | 2 |
| Forêt de Terrassa (86) ⚠️ | Terrassa › Vallès Occidental | 2 |
| Forêt de Terrassa (87) ⚠️ | Terrassa › Vallès Occidental | 2 |
| Forêt de Terrassa (89) ⚠️ | Terrassa › Vallès Occidental | 2 |
| Forêt de Terrassa (91) ⚠️ | Terrassa › Vallès Occidental | 2 |
| Forêt de Martorell (43) ⚠️ | Martorell › Baix Llobregat | 2 |
| Forêt de Esparreguera (45) ⚠️ | Esparreguera › Baix Llobregat | 2 |
| Forêt de Gelida (29) ⚠️ | Gelida › Alt Penedès | 2 |
| Forêt de Sant Esteve Sesrovires (28) ⚠️ | Sant Esteve Sesrovires › Baix Llobregat | 2 |
| Forêt de Gelida (36) ⚠️ | Gelida › Alt Penedès | 2 |
| Forêt de Santa Margarida de Montbui (58) ⚠️ | Santa Margarida de Montbui › Anoia | 2 |
| Forêt de la Pobla de Claramunt (22) ⚠️ | la Pobla de Claramunt › Anoia | 2 |
| Forêt de la Pobla de Claramunt (25) ⚠️ | la Pobla de Claramunt › Anoia | 2 |
| Forêt de la Pobla de Claramunt (30) ⚠️ | la Pobla de Claramunt › Anoia | 2 |
| Forêt de la Pobla de Claramunt (36) ⚠️ | la Pobla de Claramunt › Anoia | 2 |
| Forêt de la Pobla de Claramunt (38) ⚠️ | la Pobla de Claramunt › Anoia | 2 |
| Forêt de la Torre de Claramunt (11) ⚠️ | la Torre de Claramunt › Anoia | 2 |
| Forêt de la Pobla de Claramunt (43) ⚠️ | la Pobla de Claramunt › Anoia | 2 |
| Forêt de la Torre de Claramunt (13) ⚠️ | la Torre de Claramunt › Anoia | 2 |
| Forêt de Vallbona d'Anoia (7) ⚠️ | Vallbona d'Anoia › Anoia | 2 |
| Forêt de Vallbona d'Anoia (8) ⚠️ | Vallbona d'Anoia › Anoia | 2 |
| Forêt de Mediona (15) ⚠️ | Mediona › Alt Penedès | 2 |
| Forêt de la Torre de Claramunt (15) ⚠️ | la Torre de Claramunt › Anoia | 2 |
| Forêt de Mediona (25) ⚠️ | Mediona › Alt Penedès | 2 |
| Forêt de Mediona (31) ⚠️ | Mediona › Alt Penedès | 2 |
| Forêt de Mediona (32) ⚠️ | Mediona › Alt Penedès | 2 |
| Forêt de Piera (42) ⚠️ | Piera › Anoia | 2 |
| Forêt de Piera (50) ⚠️ | Piera › Anoia | 2 |
| Forêt de Piera (52) ⚠️ | Piera › Anoia | 2 |
| Forêt de Mediona (44) ⚠️ | Mediona › Alt Penedès | 2 |
| Forêt de Mediona (51) ⚠️ | Mediona › Alt Penedès | 2 |
| Forêt de la Llacuna (10) ⚠️ | la Llacuna › Anoia | 2 |
| Forêt de Mediona (54) ⚠️ | Mediona › Alt Penedès | 2 |
| Forêt de Cabrera d'Anoia (25) ⚠️ | Cabrera d'Anoia › Anoia | 2 |
| Forêt de Cabrera d'Anoia (26) ⚠️ | Cabrera d'Anoia › Anoia | 2 |
| Forêt de Sant Pere de Riudebitlles (3) ⚠️ | Sant Pere de Riudebitlles › Alt Penedès | 2 |
| Forêt de Cabrera d'Anoia (35) ⚠️ | Cabrera d'Anoia › Anoia | 2 |
| Forêt de Cabrera d'Anoia (48) ⚠️ | Cabrera d'Anoia › Anoia | 2 |
| Forêt de Piera (60) ⚠️ | Piera › Anoia | 2 |
| Forêt de Torrelavit (36) ⚠️ | Torrelavit › Alt Penedès | 2 |
| Forêt de Torrelavit (37) ⚠️ | Torrelavit › Alt Penedès | 2 |
| Forêt de Torrelavit (39) ⚠️ | Torrelavit › Alt Penedès | 2 |
| Forêt de Sant Quintí de Mediona (6) ⚠️ | Sant Quintí de Mediona › Alt Penedès | 2 |
| Forêt de Piera (67) ⚠️ | Piera › Anoia | 2 |
| Forêt de Piera (68) ⚠️ | Piera › Anoia | 2 |
| Forêt de Piera (74) ⚠️ | Piera › Anoia | 2 |
| Forêt de Sant Pere de Riudebitlles (12) ⚠️ | Sant Pere de Riudebitlles › Alt Penedès | 2 |
| Forêt de Torrelavit (52) ⚠️ | Torrelavit › Alt Penedès | 2 |
| Forêt de la Llacuna (13) ⚠️ | la Llacuna › Anoia | 2 |
| Forêt de la Llacuna (14) ⚠️ | la Llacuna › Anoia | 2 |
| Forêt de Mediona (73) ⚠️ | Mediona › Alt Penedès | 2 |
| Forêt de Mediona (80) ⚠️ | Mediona › Alt Penedès | 2 |
| Forêt de la Llacuna (25) ⚠️ | la Llacuna › Anoia | 2 |
| Forêt de Òdena (119) ⚠️ | Òdena › Anoia | 2 |
| Forêt de Òdena (121) ⚠️ | Òdena › Anoia | 2 |
| Forêt de Òdena (122) ⚠️ | Òdena › Anoia | 2 |
| Forêt de Tavertet (35) ⚠️ | Tavertet › Osona (Barcelone) | 2 |
| Forêt de Tavertet (49) ⚠️ | Tavertet › Osona (Barcelone) | 2 |
| Forêt de Vilanova de Sau (60) ⚠️ | Vilanova de Sau › Osona (Barcelone) | 2 |
| Forêt de Tavertet (56) ⚠️ | Tavertet › Osona (Barcelone) | 2 |
| Forêt de Tavertet (61) ⚠️ | Tavertet › Osona (Barcelone) | 2 |
| Forêt de Granollers (8) ⚠️ | Montmeló › Vallès Oriental | 2 |
| Forêt de Alpens (25) ⚠️ | Alpens › Lluçanès | 2 |
| Forêt de Olvan (39) ⚠️ | Olvan › Berguedà | 2 |
| Forêt de Olvan (42) ⚠️ | Olvan › Berguedà | 2 |
| Forêt de Tordera (105) ⚠️ | Tordera › Maresme | 2 |
| Forêt de Palafolls (31) ⚠️ | Palafolls › Maresme | 2 |
| Forêt de Palafolls (33) ⚠️ | Palafolls › Maresme | 2 |
| Forêt de Santa Susanna (14) ⚠️ | Santa Susanna › Maresme | 2 |
| Forêt de Santa Susanna (15) ⚠️ | Santa Susanna › Maresme | 2 |
| Parc de Malgrat de Mar (13) ⚠️ | Malgrat de Mar › Maresme | 2 |
| Forêt de Arenys de Munt (9) ⚠️ | Arenys de Munt › Maresme | 2 |
| Forêt de Arenys de Munt (21) ⚠️ | Arenys de Munt › Maresme | 2 |
| Forêt de Vallgorguina (15) ⚠️ | Vallgorguina › Vallès Oriental | 2 |
| Forêt de Vallgorguina (18) ⚠️ | Vallgorguina › Vallès Oriental | 2 |
| Forêt de Vallgorguina (22) ⚠️ | Vallgorguina › Vallès Oriental | 2 |
| Forêt de Fogars de la Selva (42) ⚠️ | Fogars de la Selva › la Selva (Barcelone) | 2 |
| Forêt de Gualba (16) ⚠️ | Gualba › Vallès Oriental | 2 |
| Forêt de Gualba (21) ⚠️ | Gualba › Vallès Oriental | 2 |
| Forêt de Gualba (22) ⚠️ | Gualba › Vallès Oriental | 2 |
| Forêt de Gualba (27) ⚠️ | Gualba › Vallès Oriental | 2 |
| Forêt de Sant Celoni (66) ⚠️ | Sant Celoni › Vallès Oriental | 2 |
| Forêt de Sant Celoni (74) ⚠️ | Sant Celoni › Vallès Oriental | 2 |
| Forêt de Sant Celoni (76) ⚠️ | Sant Celoni › Vallès Oriental | 2 |
| Forêt de Gironella (22) ⚠️ | Gironella › Berguedà | 2 |
| Forêt de Gironella (27) ⚠️ | Gironella › Berguedà | 2 |
| Forêt de Gironella (29) ⚠️ | Gironella › Berguedà | 2 |
| Forêt de Sant Quirze del Vallès (17) ⚠️ | Sant Quirze del Vallès › Vallès Occidental | 2 |
| Forêt de Sallent (117) ⚠️ | Sallent › Bages | 2 |
| Forêt de Santpedor (13) ⚠️ | Santpedor › Bages | 2 |
| Forêt de Santpedor (15) ⚠️ | Santpedor › Bages | 2 |
| Forêt de Sallent (126) ⚠️ | Sallent › Bages | 2 |
| Forêt de Santpedor (17) ⚠️ | Santpedor › Bages | 2 |
| Forêt de Santpedor (28) ⚠️ | Santpedor › Bages | 2 |
| Forêt de Santpedor (31) ⚠️ | Castellnou de Bages › Bages | 2 |
| Forêt de Santpedor (57) ⚠️ | Santpedor › Bages | 2 |
| Forêt de Sant Feliu de Codines (17) ⚠️ | Sant Feliu de Codines › Vallès Oriental | 2 |
| Forêt de Castellnou de Bages (75) ⚠️ | Castellnou de Bages › Bages | 2 |
| Forêt de Castellnou de Bages (82) ⚠️ | Castellnou de Bages › Bages | 2 |
| Forêt de Castellnou de Bages (85) ⚠️ | Castellnou de Bages › Bages | 2 |
| Forêt de Callús (37) ⚠️ | Callús › Bages | 2 |
| Forêt de Callús (45) ⚠️ | Callús › Bages | 2 |
| Forêt de Santpedor (63) ⚠️ | Santpedor › Bages | 2 |
| Forêt de Sant Joan de Vilatorrada (71) ⚠️ | Sant Joan de Vilatorrada › Bages | 2 |
| Forêt de Sant Joan de Vilatorrada (78) ⚠️ | Sant Joan de Vilatorrada › Bages | 2 |
| Forêt de Callús (50) ⚠️ | Callús › Bages | 2 |
| Forêt de Sant Joan de Vilatorrada (84) ⚠️ | Sant Joan de Vilatorrada › Bages | 2 |
| Forêt de Callús (57) ⚠️ | Callús › Bages | 2 |
| Forêt de Fonollosa (149) ⚠️ | Fonollosa › Bages | 2 |
| Forêt de Fonollosa (150) ⚠️ | Fonollosa › Bages | 2 |
| Forêt de Fonollosa (151) ⚠️ | Fonollosa › Bages | 2 |
| Forêt de Fonollosa (160) ⚠️ | Fonollosa › Bages | 2 |
| Forêt de Fonollosa (163) ⚠️ | Fonollosa › Bages | 2 |
| Forêt de Fonollosa (165) ⚠️ | Fonollosa › Bages | 2 |
| Forêt de Sant Mateu de Bages (149) ⚠️ | Sant Mateu de Bages › Bages | 2 |
| Forêt de Sant Feliu Sasserra (41) ⚠️ | Sant Feliu Sasserra › Bages | 2 |
| Forêt de Vallcebre (65) ⚠️ | Vallcebre › Berguedà | 2 |
| Forêt de Vallcebre (66) ⚠️ | Vallcebre › Berguedà | 2 |
| Forêt de Vallcebre (69) ⚠️ | Vallcebre › Berguedà | 2 |
| Forêt de Santa Eugènia de Berga (3) ⚠️ | Santa Eugènia de Berga › Osona (Barcelone) | 2 |
| Forêt de Sant Julià de Vilatorta (11) ⚠️ | Sant Julià de Vilatorta › Osona (Barcelone) | 2 |
| Forêt de Sant Sadurní d'Osormort (42) ⚠️ | Sant Sadurní d'Osormort › Osona (Barcelone) | 2 |
| Forêt de Tavèrnoles (9) ⚠️ | Folgueroles › Osona (Barcelone) | 2 |
| Forêt de Sant Julià de Vilatorta (14) ⚠️ | Sant Julià de Vilatorta › Osona (Barcelone) | 2 |
| Forêt de Folgueroles (10) ⚠️ | Folgueroles › Osona (Barcelone) | 2 |
| Forêt de Sant Julià de Vilatorta (21) ⚠️ | Sant Julià de Vilatorta › Osona (Barcelone) | 2 |
| Forêt de Santa Maria d'Oló (86) ⚠️ | Santa Maria d'Oló › Moianès | 2 |
| Forêt de Manlleu (8) ⚠️ | Manlleu › Osona (Barcelone) | 2 |
| Parc de Rocaprevera ⚠️ | Torelló › Osona (Barcelone) | 2 |
| Forêt de les Masies de Voltregà (21) ⚠️ | les Masies de Voltregà › Osona (Barcelone) | 2 |
| Forêt de Arenys de Mar (15) ⚠️ | Arenys de Mar › Maresme | 2 |
| Forêt de Mataró (10) ⚠️ | Mataró › Maresme | 2 |
| Forêt de Argentona (10) ⚠️ | Argentona › Maresme | 2 |
| Forêt de Mataró (12) ⚠️ | Mataró › Maresme | 2 |
| Bois de Cabrera de Mar ⚠️ | Cabrera de Mar › Maresme | 2 |
| Forêt de Gurb (25) ⚠️ | Gurb › Osona (Barcelone) | 2 |
| Forêt de Vic (48) ⚠️ | Vic › Osona (Barcelone) | 2 |
| Forêt de Gurb (30) ⚠️ | Gurb › Osona (Barcelone) | 2 |
| Forêt de Vic (60) ⚠️ | Vic › Osona (Barcelone) | 2 |
| Forêt de Torelló (7) ⚠️ | Torelló › Osona (Barcelone) | 2 |
| Forêt de Gurb (39) ⚠️ | Gurb › Osona (Barcelone) | 2 |
| Forêt de Gurb (45) ⚠️ | Gurb › Osona (Barcelone) | 2 |
| Forêt de Gurb (47) ⚠️ | Gurb › Osona (Barcelone) | 2 |
| Forêt de Vic (79) ⚠️ | Vic › Osona (Barcelone) | 2 |
| Forêt de Gurb (76) ⚠️ | Gurb › Osona (Barcelone) | 2 |
| Forêt de Montmeló (5) ⚠️ | Montmeló › Vallès Oriental | 2 |
| Forêt de Montmeló (9) ⚠️ | Montmeló › Vallès Oriental | 2 |
| Bois de Parets del Vallès (2) ⚠️ | Parets del Vallès › Vallès Oriental | 2 |
| Bois de Vilanova del Vallès (18) ⚠️ | Montornès del Vallès › Vallès Oriental | 2 |
| Forêt de Caldes de Montbui (14) ⚠️ | Caldes de Montbui › Vallès Oriental | 2 |
| Forêt de Caldes de Montbui (16) ⚠️ | Caldes de Montbui › Vallès Oriental | 2 |
| Forêt de Caldes de Montbui (19) ⚠️ | Caldes de Montbui › Vallès Oriental | 2 |
| Forêt de Caldes de Montbui (20) ⚠️ | Caldes de Montbui › Vallès Oriental | 2 |
| Forêt de Caldes de Montbui (21) ⚠️ | Caldes de Montbui › Vallès Oriental | 2 |
| Forêt de Palau-solità i Plegamans (14) ⚠️ | Palau-solità i Plegamans › Vallès Occidental | 2 |
| Forêt de Palau-solità i Plegamans (18) ⚠️ | Palau-solità i Plegamans › Vallès Occidental | 2 |
| Parc de Lliçà d'Amunt (3) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 2 |
| Forêt de Lliçà de Vall (8) ⚠️ | Lliçà de Vall › Vallès Oriental | 2 |
| Forêt de Lluçà (90) ⚠️ | Prats de Lluçanès › Lluçanès | 2 |
| Forêt de Prats de Lluçanès (31) ⚠️ | Prats de Lluçanès › Lluçanès | 2 |
| Forêt de Olost (16) ⚠️ | Olost › Lluçanès | 2 |
| Forêt de Oristà (170) ⚠️ | Oristà › Lluçanès | 2 |
| Forêt de Oristà (172) ⚠️ | Oristà › Lluçanès | 2 |
| Forêt de Fígols (46) ⚠️ | Fígols › Berguedà | 2 |
| Forêt de Fígols (47) ⚠️ | Fígols › Berguedà | 2 |
| Forêt de Calders (75) ⚠️ | Calders › Moianès | 2 |
| Forêt de Calders (79) ⚠️ | Calders › Moianès | 2 |
| Forêt de Calders (80) ⚠️ | Calders › Moianès | 2 |
| Forêt de Moià (71) ⚠️ | Moià › Moianès | 2 |
| Forêt de Sant Fruitós de Bages (51) ⚠️ | Sant Fruitós de Bages › Bages | 2 |
| Forêt de Manresa (153) ⚠️ | Manresa › Bages | 2 |
| Forêt de Manresa (161) ⚠️ | Manresa › Bages | 2 |
| Forêt de Sant Fruitós de Bages (90) ⚠️ | Sant Fruitós de Bages › Bages | 2 |
| Forêt de el Pont de Vilomara i Rocafort (37) ⚠️ | el Pont de Vilomara i Rocafort › Bages | 2 |
| Forêt de el Pont de Vilomara i Rocafort (49) ⚠️ | el Pont de Vilomara i Rocafort › Bages | 2 |
| Forêt de Sant Salvador de Guardiola (123) ⚠️ | Sant Salvador de Guardiola › Bages | 2 |
| Forêt de Vacarisses (72) ⚠️ | Vacarisses › Vallès Occidental | 2 |
| Forêt de Seva (39) ⚠️ | Seva › Osona (Barcelone) | 2 |
| Forêt de Sant Martí d'Albars (5) ⚠️ | Sant Martí d'Albars › Lluçanès | 2 |
| Forêt de la Pobla de Lillet (66) ⚠️ | la Pobla de Lillet › Berguedà | 2 |
| Parc del Palau ⚠️ | Mataró › Maresme | 1 |
| Forêt de Barcelona ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de l'Espanya Industrial ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Gavà (3) ⚠️ | Gavà › Baix Llobregat | 1 |
| Parc de Can Guardiola ⚠️ | Viladecans › Baix Llobregat | 1 |
| Parc dels Xiprers ⚠️ | Castelldefels › Baix Llobregat | 1 |
| Plaça de la Sagrada Família ⚠️ | Barcelona › Barcelonès | 1 |
| Parc Municipal de la Torre Lluc ⚠️ | Gavà › Baix Llobregat | 1 |
| Parc dels Catalans ⚠️ | Terrassa › Vallès Occidental | 1 |
| Plaça de Can Tusell ⚠️ | Terrassa › Vallès Occidental | 1 |
| Parc de Sant Jordi ⚠️ | Terrassa › Vallès Occidental | 1 |
| Parc de Sant Cugat del Vallès (2) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Plaça de Can Roca ⚠️ | Terrassa › Vallès Occidental | 1 |
| Parc de la Pegaso ⚠️ | Barcelona › Barcelonès | 1 |
| Parc del Molinet ⚠️ | Santa Coloma de Gramenet › Barcelonès | 1 |
| Parc del Gran Sol ⚠️ | Badalona › Barcelonès | 1 |
| Plaça Francesc Macià ⚠️ | Montcada i Reixac › Vallès Occidental | 1 |
| Parc de Montcada i Reixac (3) ⚠️ | Montcada i Reixac › Vallès Occidental | 1 |
| Parc de la Vil·la Romana de Torre Llauder ⚠️ | Mataró › Maresme | 1 |
| Parc de Cerdanyola ⚠️ | Mataró › Maresme | 1 |
| Plaça de Rafael Casanova ⚠️ | Mataró › Maresme | 1 |
| Parc Central (2) ⚠️ | Mataró › Maresme | 1 |
| Parc de la Mariona ⚠️ | Molins de Rei › Baix Llobregat | 1 |
| Parc de Montcada i Reixac (7) ⚠️ | Montcada i Reixac › Vallès Occidental | 1 |
| Parc de Rafael Alberti ⚠️ | Mataró › Maresme | 1 |
| Parc de les Roques Albes ⚠️ | Mataró › Maresme | 1 |
| Parc de les Aigües ⚠️ | Barcelona › Barcelonès | 1 |
| Plaça de les Bruixes ⚠️ | Molins de Rei › Baix Llobregat | 1 |
| Parc de Josep Maria Serra Martí ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Terrassa ⚠️ | Terrassa › Vallès Occidental | 1 |
| Parc de Barcelona (2) ⚠️ | Barcelona › Barcelonès | 1 |
| Jardí dels Drets Humans ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de Terrassa (6) ⚠️ | Terrassa › Vallès Occidental | 1 |
| Parc de la Guineueta ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de Montcada i Reixac (8) ⚠️ | Montcada i Reixac › Vallès Occidental | 1 |
| Parc de les Aubes ⚠️ | Berga › Berguedà | 1 |
| Parc dels Pins ⚠️ | Santa Coloma de Gramenet › Barcelonès | 1 |
| Forêt de Tordera (2) ⚠️ | Tordera › Maresme | 1 |
| Plaça de Sants ⚠️ | Barcelona › Barcelonès | 1 |
| Jardins del Clot de la Mel ⚠️ | Barcelona › Barcelonès | 1 |
| Plaça de Dolors Vives ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de Sant Martí ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de Sant Martí (2) ⚠️ | Barcelona › Barcelonès | 1 |
| Jardins de Gandhi ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de Nova Icària ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Palafolls (3) ⚠️ | Palafolls › Maresme | 1 |
| Forêt de Palafolls (5) ⚠️ | Palafolls › Maresme | 1 |
| Forêt de Palafolls (6) ⚠️ | Palafolls › Maresme | 1 |
| Parc dels Tallinaires ⚠️ | Castelldefels › Baix Llobregat | 1 |
| Bois de Barcelona (4) ⚠️ | Barcelona › Barcelonès | 1 |
| Plaça del Dr. Pearson ⚠️ | Rubí › Vallès Occidental | 1 |
| Parc del Vinyet ⚠️ | Sitges › Garraf | 1 |
| Parc de la Font del Racó ⚠️ | Barcelona › Barcelonès | 1 |
| Parc del Litoral ⚠️ | Sant Adrià de Besòs › Barcelonès | 1 |
| Jardins del Baix Guinardó ⚠️ | Barcelona › Barcelonès | 1 |
| Jardins de Joan Vinyolí ⚠️ | Barcelona › Barcelonès | 1 |
| Plaça Vicenc Casanovas ⚠️ | Vilassar de Mar › Maresme | 1 |
| Parc de Torras Villà ⚠️ | Granollers › Vallès Oriental | 1 |
| Jardins Can Corts ⚠️ | Granollers › Vallès Oriental | 1 |
| Jardins Joan Vinyoli ⚠️ | Granollers › Vallès Oriental | 1 |
| Plaça de la Llacuna ⚠️ | Granollers › Vallès Oriental | 1 |
| Bois de Barcelona (5) ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de Ponent ⚠️ | Granollers › Vallès Oriental | 1 |
| Parc de Granollers ⚠️ | Granollers › Vallès Oriental | 1 |
| Jardins de Rita Gibernau Riera ⚠️ | Granollers › Vallès Oriental | 1 |
| Parc dels Pirineus ⚠️ | Lliçà d'Amunt › Vallès Oriental | 1 |
| Moll d'Espanya ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de Francisco Ibáñez ⚠️ | Lliçà d'Amunt › Vallès Oriental | 1 |
| Bois de Cabrils ⚠️ | Cabrils › Maresme | 1 |
| Plaça de Sóller ⚠️ | Barcelona › Barcelonès | 1 |
| Bois de Lliçà d'Amunt ⚠️ | Lliçà d'Amunt › Vallès Oriental | 1 |
| Plaça d'Ernest Lluch ⚠️ | l'Hospitalet de Llobregat › Barcelonès | 1 |
| Parc de Barcelona (12) ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de l'Hospitalet de Llobregat (2) ⚠️ | l'Hospitalet de Llobregat › Barcelonès | 1 |
| Plaça de Puig i Gairalt ⚠️ | l'Hospitalet de Llobregat › Barcelonès | 1 |
| Plaça de les Palmeres ⚠️ | l'Hospitalet de Llobregat › Barcelonès | 1 |
| Plaça de Lluís Companys i Jover ⚠️ | l'Hospitalet de Llobregat › Barcelonès | 1 |
| Parc de la Granvia de l'Hospitalet ⚠️ | l'Hospitalet de Llobregat › Barcelonès | 1 |
| Jardins de Maria Baldó ⚠️ | Barcelona › Barcelonès | 1 |
| Parc dels Pinetons (2) ⚠️ | la Garriga › Vallès Oriental | 1 |
| Forêt de Palafolls (8) ⚠️ | Palafolls › Maresme | 1 |
| Bosc de Can Roget ⚠️ | Lliçà d'Amunt › Vallès Oriental | 1 |
| Bois de Canovelles ⚠️ | Canovelles › Vallès Oriental | 1 |
| Forêt de Lliçà d'Amunt (7) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 1 |
| Bois de Lliçà d'Amunt (7) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 1 |
| Forêt de Lliçà d'Amunt (8) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 1 |
| Bois de Lliçà d'Amunt (11) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 1 |
| Bois de Lliçà d'Amunt (12) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 1 |
| Bois de Lliçà d'Amunt (13) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 1 |
| Bois de Lliçà d'Amunt (16) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 1 |
| Bois de Lliçà d'Amunt (18) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 1 |
| Bois de Lliçà d'Amunt (21) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 1 |
| Forêt de Cardona (2) ⚠️ | Cardona › Bages | 1 |
| Parc del Torrent Ballester ⚠️ | Viladecans › Baix Llobregat | 1 |
| Forêt de Sora (2) ⚠️ | Sora › Osona (Barcelone) | 1 |
| Forêt de Vilanova de Sau (3) ⚠️ | Vilanova de Sau › Osona (Barcelone) | 1 |
| Forêt de Gavà (8) ⚠️ | Gavà › Baix Llobregat | 1 |
| Forêt de Sant Jaume de Frontanyà (2) ⚠️ | Sant Jaume de Frontanyà › Berguedà | 1 |
| Forêt de Palafolls (11) ⚠️ | Palafolls › Maresme | 1 |
| Forêt de Cardona (3) ⚠️ | Cardona › Bages | 1 |
| Forêt de Sant Pere de Vilamajor ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 1 |
| Forêt de Santa Maria de Besora (3) ⚠️ | Santa Maria de Besora › Osona (Barcelone) | 1 |
| Forêt de Castellar del Vallès (5) ⚠️ | Castellar del Vallès › Vallès Occidental | 1 |
| Forêt de Seva ⚠️ | Seva › Osona (Barcelone) | 1 |
| Forêt de Sant Sadurní d'Osormort (7) ⚠️ | Sant Sadurní d'Osormort › Osona (Barcelone) | 1 |
| Forêt de Cerdanyola del Vallès (3) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Forêt de Alpens (7) ⚠️ | Alpens › Lluçanès | 1 |
| Forêt de Palafolls (19) ⚠️ | Palafolls › Maresme | 1 |
| Forêt de Vilanova de Sau (16) ⚠️ | Vilanova de Sau › Osona (Barcelone) | 1 |
| Forêt de Vilanova de Sau (18) ⚠️ | Vilanova de Sau › Osona (Barcelone) | 1 |
| Parc de Mataró (2) ⚠️ | Mataró › Maresme | 1 |
| Parc del Litoral (2) ⚠️ | Sant Pol de Mar › Maresme | 1 |
| Parc de Cornellà de Llobregat (2) ⚠️ | el Prat de Llobregat › Baix Llobregat | 1 |
| Plaça de Romuald Grané ⚠️ | Mataró › Maresme | 1 |
| Parc del Turonet ⚠️ | Montgat › Maresme | 1 |
| Plaça de la Sardana ⚠️ | Vilanova i la Geltrú › Garraf | 1 |
| Plaça de la Constitució ⚠️ | Terrassa › Vallès Occidental | 1 |
| Jardins de Piscines i esports ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de les Grases (2) ⚠️ | Sant Feliu de Llobregat › Baix Llobregat | 1 |
| Parc de Barcelona (27) ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de Barcelona (28) ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de Badia del Vallès (2) ⚠️ | Badia del Vallès › Vallès Occidental | 1 |
| Parc de Joan Oliver ⚠️ | Badia del Vallès › Vallès Occidental | 1 |
| Parc de Badia del Vallès (6) ⚠️ | Badia del Vallès › Vallès Occidental | 1 |
| Parc de Sant Cugat del Vallès (10) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Forêt de Sant Cugat del Vallès (13) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Parc de Sant Cugat del Vallès (21) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Parc de Sant Cugat del Vallès (22) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Parc de Sant Cugat del Vallès (28) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Parc de Sant Cugat del Vallès (30) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Forêt de Sant Cugat del Vallès (67) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Forêt de Sant Cugat del Vallès (71) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Forêt de Sant Cugat del Vallès (72) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Forêt de Sant Cugat del Vallès (79) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Forêt de Sant Cugat del Vallès (80) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Forêt de Sant Cugat del Vallès (81) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Forêt de Sant Cugat del Vallès (82) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Bois de Sant Cugat del Vallès (5) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Parc de Sant Cugat del Vallès (35) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Forêt de Begues (2) ⚠️ | Begues › Baix Llobregat | 1 |
| Parc de Sant Cugat del Vallès (36) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Bois de Sant Cugat del Vallès (20) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Bois de Sant Cugat del Vallès (23) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Bois de Sant Cugat del Vallès (28) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Bois de Sant Cugat del Vallès (35) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Bois de Sant Cugat del Vallès (46) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Plaça de Jeroni Gelpí ⚠️ | Vilassar de Mar › Maresme | 1 |
| Bois de Sant Cugat del Vallès (58) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Parc de Ca n'Oriol ⚠️ | Rubí › Vallès Occidental | 1 |
| Bois de Sant Cugat del Vallès (60) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Bois de Sant Cugat del Vallès (61) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Bois de Sant Cugat del Vallès (62) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Bois de Sabadell (13) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Parc de Sabadell (8) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Bois de Sant Quirze del Vallès ⚠️ | Sant Quirze del Vallès › Vallès Occidental | 1 |
| Bois de Sant Quirze del Vallès (3) ⚠️ | Sant Quirze del Vallès › Vallès Occidental | 1 |
| Parc d'Odessa ⚠️ | Sabadell › Vallès Occidental | 1 |
| Parc de Sabadell (11) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Parc de Barcelona (31) ⚠️ | Barcelona › Barcelonès | 1 |
| Bois de Barcelona (8) ⚠️ | Barcelona › Barcelonès | 1 |
| Bois de Barcelona (17) ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de Barcelona (32) ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Barcelona (3) ⚠️ | Barcelona › Barcelonès | 1 |
| Bois de Sant Quirze del Vallès (5) ⚠️ | Sant Quirze del Vallès › Vallès Occidental | 1 |
| Forêt de Sant Quirze del Vallès (2) ⚠️ | Sant Quirze del Vallès › Vallès Occidental | 1 |
| Forêt de Cerdanyola del Vallès (4) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Parc de Santa Perpètua de Mogoda ⚠️ | Santa Perpètua de Mogoda › Vallès Occidental | 1 |
| Parc de Santa Perpètua de Mogoda (2) ⚠️ | Santa Perpètua de Mogoda › Vallès Occidental | 1 |
| Parc d'Europa (2) ⚠️ | Santa Perpètua de Mogoda › Vallès Occidental | 1 |
| Forêt de Sant Climent de Llobregat (6) ⚠️ | Sant Climent de Llobregat › Baix Llobregat | 1 |
| Forêt de Terrassa (5) ⚠️ | Terrassa › Vallès Occidental | 1 |
| Forêt de Terrassa (7) ⚠️ | Terrassa › Vallès Occidental | 1 |
| Forêt de Terrassa (8) ⚠️ | Terrassa › Vallès Occidental | 1 |
| Forêt de Terrassa (12) ⚠️ | Terrassa › Vallès Occidental | 1 |
| Forêt de Terrassa (13) ⚠️ | Terrassa › Vallès Occidental | 1 |
| Parc de Catalunya ⚠️ | Santa Perpètua de Mogoda › Vallès Occidental | 1 |
| Parc de Pere Bufí i Pérez ⚠️ | Santa Perpètua de Mogoda › Vallès Occidental | 1 |
| Parc de Tísner ⚠️ | Santa Perpètua de Mogoda › Vallès Occidental | 1 |
| Parc de la Pau (2) ⚠️ | Santa Perpètua de Mogoda › Vallès Occidental | 1 |
| Parc de la Pesseta ⚠️ | Santa Perpètua de Mogoda › Vallès Occidental | 1 |
| Forêt de Viladecans (5) ⚠️ | Viladecans › Baix Llobregat | 1 |
| Parc de Sitges (4) ⚠️ | Sitges › Garraf | 1 |
| Jardins d'Ernest Lluch ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de la Bassa dels Germans Maristes ⚠️ | Vic › Osona (Barcelone) | 1 |
| Parc del Mil·lenari ⚠️ | Sant Joan Despí › Baix Llobregat | 1 |
| Parc del Cementiri ⚠️ | Vic › Osona (Barcelone) | 1 |
| Parc Catalunya ⚠️ | Sant Joan de Vilatorrada › Bages | 1 |
| Parc de Mataró (4) ⚠️ | Mataró › Maresme | 1 |
| Forêt de Sentmenat (2) ⚠️ | Sentmenat › Vallès Occidental | 1 |
| Parc Llobet ⚠️ | Sant Joan de Vilatorrada › Bages | 1 |
| Forêt de Cerdanyola del Vallès (6) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Forêt de Cerdanyola del Vallès (8) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Forêt de Cerdanyola del Vallès (9) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Forêt de Cerdanyola del Vallès (11) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Forêt de Cerdanyola del Vallès (13) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Forêt de Cerdanyola del Vallès (17) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Forêt de Cerdanyola del Vallès (19) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Parc de Cerdanyola del Vallès (6) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Forêt de Cerdanyola del Vallès (21) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Forêt de Sant Pere de Ribes (6) ⚠️ | Sant Pere de Ribes › Garraf | 1 |
| Forêt de Sant Pere de Ribes (7) ⚠️ | Sant Pere de Ribes › Garraf | 1 |
| Forêt de Sant Pere de Ribes (9) ⚠️ | Sant Pere de Ribes › Garraf | 1 |
| Forêt de Sant Joan de Vilatorrada ⚠️ | Sant Joan de Vilatorrada › Bages | 1 |
| Forêt de Cerdanyola del Vallès (22) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| el Bosquet ⚠️ | Sant Fruitós de Bages › Bages | 1 |
| Plaça de la Joventut ⚠️ | Canovelles › Vallès Oriental | 1 |
| Forêt de la Roca del Vallès (2) ⚠️ | la Roca del Vallès › Vallès Oriental | 1 |
| Bois de Cerdanyola del Vallès (3) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Parc de Pompeu Fabra ⚠️ | Sant Pere de Ribes › Garraf | 1 |
| Bois de Rubí (2) ⚠️ | Rubí › Vallès Occidental | 1 |
| Pati d'Escola Justo Domínguez ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Torrelles de Llobregat (7) ⚠️ | Torrelles de Llobregat › Baix Llobregat | 1 |
| Forêt de Torrelles de Llobregat (10) ⚠️ | Torrelles de Llobregat › Baix Llobregat | 1 |
| Forêt de Torrelles de Llobregat (11) ⚠️ | Torrelles de Llobregat › Baix Llobregat | 1 |
| Plaça de les Sibil·les ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de Barcelona (38) ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de Badia del Vallès (7) ⚠️ | Badia del Vallès › Vallès Occidental | 1 |
| Parc de Vic (2) ⚠️ | Vic › Osona (Barcelone) | 1 |
| Forêt de Esplugues de Llobregat (6) ⚠️ | Esplugues de Llobregat › Baix Llobregat | 1 |
| Parc de la Mar Xica ⚠️ | Vilassar de Mar › Maresme | 1 |
| Plaça dels Esposos Jaume Ribas i Francisca Asensio ⚠️ | Sant Vicenç dels Horts › Baix Llobregat | 1 |
| Parc de Santiñà ⚠️ | Canet de Mar › Maresme | 1 |
| Parc del Port Olímpic ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de Granollers (17) ⚠️ | Granollers › Vallès Oriental | 1 |
| Plaça dels Països Catalans (3) ⚠️ | Molins de Rei › Baix Llobregat | 1 |
| Plaça de les Tretze Roses ⚠️ | Gavà › Baix Llobregat | 1 |
| Parc de Solicrup ⚠️ | Vilanova i la Geltrú › Garraf | 1 |
| Bois de la Roca del Vallès ⚠️ | la Roca del Vallès › Vallès Oriental | 1 |
| Parc de Can Mulà ⚠️ | Mollet del Vallès › Vallès Oriental | 1 |
| Jardí de la Farinera ⚠️ | Mollet del Vallès › Vallès Oriental | 1 |
| Parc Europa (2) ⚠️ | Sant Feliu de Llobregat › Baix Llobregat | 1 |
| Parc Europa (4) ⚠️ | Sant Feliu de Llobregat › Baix Llobregat | 1 |
| Plaça Dicià ⚠️ | Sant Feliu de Llobregat › Baix Llobregat | 1 |
| Parc Europa (5) ⚠️ | Sant Just Desvern › Baix Llobregat | 1 |
| Plaça de l'Onze de Setembre (3) ⚠️ | Manresa › Bages | 1 |
| Jardins de Josep Trueta ⚠️ | Barcelona › Barcelonès | 1 |
| Plaça de les marmanyeres ⚠️ | Mollet del Vallès › Vallès Oriental | 1 |
| Plaça dels Mercaders ⚠️ | Mollet del Vallès › Vallès Oriental | 1 |
| Parc de Can Borrell ⚠️ | Mollet del Vallès › Vallès Oriental | 1 |
| Plaça dels Ferrers ⚠️ | Mollet del Vallès › Vallès Oriental | 1 |
| Forêt de Gurb (5) ⚠️ | Gurb › Osona (Barcelone) | 1 |
| Parc de Sant Pancraç ⚠️ | Sant Joan Despí › Baix Llobregat | 1 |
| Plaça del Consell d'Infants ⚠️ | Sant Joan Despí › Baix Llobregat | 1 |
| Parc de Manresa (4) ⚠️ | Manresa › Bages | 1 |
| Parc de Sant Ignasi ⚠️ | Manresa › Bages | 1 |
| Forêt de Cabrils (3) ⚠️ | Cabrils › Maresme | 1 |
| Parc de el Pont de Vilomara i Rocafort ⚠️ | el Pont de Vilomara i Rocafort › Bages | 1 |
| Bosc de Can Jornet ⚠️ | Mollet del Vallès › Vallès Oriental | 1 |
| Bosc de la Torre d'en Malla ⚠️ | Parets del Vallès › Vallès Oriental | 1 |
| Parc de Mollet del Vallès (2) ⚠️ | Mollet del Vallès › Vallès Oriental | 1 |
| Parc de Sabadell (15) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Forêt de Cerdanyola del Vallès (26) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Forêt de Cerdanyola del Vallès (28) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Bois de Mataró ⚠️ | Mataró › Maresme | 1 |
| Bois de Mataró (3) ⚠️ | Mataró › Maresme | 1 |
| Parc de les Ginestes ⚠️ | Caldes d'Estrac › Maresme | 1 |
| Parc de Gavà (3) ⚠️ | Gavà › Baix Llobregat | 1 |
| Parc dels Països Catalans ⚠️ | les Franqueses del Vallès › Vallès Oriental | 1 |
| Bois de Mataró (5) ⚠️ | Mataró › Maresme | 1 |
| Parc de la Via Europa ⚠️ | Mataró › Maresme | 1 |
| Parc de Barcelona (43) ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Begues (3) ⚠️ | Begues › Baix Llobregat | 1 |
| Jardins de Pons i Termes ⚠️ | Esplugues de Llobregat › Baix Llobregat | 1 |
| Parc de Cal Jardiner ⚠️ | Parets del Vallès › Vallès Oriental | 1 |
| Forêt de Gavà (14) ⚠️ | Gavà › Baix Llobregat | 1 |
| Forêt de Sitges ⚠️ | Sitges › Garraf | 1 |
| Forêt de Gavà (16) ⚠️ | Gavà › Baix Llobregat | 1 |
| Forêt de Subirats (3) ⚠️ | Subirats › Alt Penedès | 1 |
| Parc de Nova Lloreda ⚠️ | Badalona › Barcelonès | 1 |
| Forêt de Subirats (5) ⚠️ | Subirats › Alt Penedès | 1 |
| Parc de Nelson Mandela ⚠️ | Badalona › Barcelonès | 1 |
| Parc de Can Barriga ⚠️ | Badalona › Barcelonès | 1 |
| Forêt de Olesa de Bonesvalls (9) ⚠️ | Olesa de Bonesvalls › Alt Penedès | 1 |
| Forêt de Avinyonet del Penedès (9) ⚠️ | Avinyonet del Penedès › Alt Penedès | 1 |
| Forêt de Begues (9) ⚠️ | Begues › Baix Llobregat | 1 |
| Forêt de Mediona (5) ⚠️ | Mediona › Alt Penedès | 1 |
| Forêt de Mediona (6) ⚠️ | Mediona › Alt Penedès | 1 |
| Forêt de Avinyonet del Penedès (12) ⚠️ | Avinyonet del Penedès › Alt Penedès | 1 |
| Forêt de Subirats (8) ⚠️ | Subirats › Alt Penedès | 1 |
| Forêt de Avinyonet del Penedès (16) ⚠️ | Avinyonet del Penedès › Alt Penedès | 1 |
| Forêt de Olesa de Bonesvalls (14) ⚠️ | Olesa de Bonesvalls › Alt Penedès | 1 |
| Forêt de Avinyonet del Penedès (20) ⚠️ | Avinyonet del Penedès › Alt Penedès | 1 |
| Forêt de Avinyonet del Penedès (21) ⚠️ | Avinyonet del Penedès › Alt Penedès | 1 |
| Forêt de Subirats (11) ⚠️ | Subirats › Alt Penedès | 1 |
| Forêt de Subirats (12) ⚠️ | Subirats › Alt Penedès | 1 |
| Forêt de Subirats (15) ⚠️ | Subirats › Alt Penedès | 1 |
| Forêt de Gavà (19) ⚠️ | Gavà › Baix Llobregat | 1 |
| Forêt de Gavà (23) ⚠️ | Gavà › Baix Llobregat | 1 |
| Forêt de Olesa de Bonesvalls (17) ⚠️ | Olesa de Bonesvalls › Alt Penedès | 1 |
| Forêt de Avinyonet del Penedès (26) ⚠️ | Avinyonet del Penedès › Alt Penedès | 1 |
| Forêt de Avinyonet del Penedès (27) ⚠️ | Avinyonet del Penedès › Alt Penedès | 1 |
| Forêt de Olèrdola (6) ⚠️ | Olèrdola › Alt Penedès | 1 |
| Forêt de Subirats (18) ⚠️ | Subirats › Alt Penedès | 1 |
| Forêt de Avinyonet del Penedès (38) ⚠️ | Avinyonet del Penedès › Alt Penedès | 1 |
| Forêt de Gelida (3) ⚠️ | Gelida › Alt Penedès | 1 |
| Forêt de Subirats (23) ⚠️ | Subirats › Alt Penedès | 1 |
| Forêt de Subirats (25) ⚠️ | Subirats › Alt Penedès | 1 |
| Forêt de Subirats (26) ⚠️ | Subirats › Alt Penedès | 1 |
| Forêt de Subirats (28) ⚠️ | Subirats › Alt Penedès | 1 |
| Forêt de Olèrdola (7) ⚠️ | Olèrdola › Alt Penedès | 1 |
| Forêt de Olèrdola (8) ⚠️ | Olèrdola › Alt Penedès | 1 |
| Forêt de Subirats (37) ⚠️ | Subirats › Alt Penedès | 1 |
| Forêt de l'Esquirol (14) ⚠️ | l'Esquirol › Osona (Barcelone) | 1 |
| Forêt de Olèrdola (13) ⚠️ | Olèrdola › Alt Penedès | 1 |
| Parc de Sant Celoni (3) ⚠️ | Sant Celoni › Vallès Oriental | 1 |
| Forêt de Olèrdola (16) ⚠️ | Olèrdola › Alt Penedès | 1 |
| Forêt de Vilobí del Penedès (3) ⚠️ | Vilobí del Penedès › Alt Penedès | 1 |
| Parc de Francesc Macià ⚠️ | Malgrat de Mar › Maresme | 1 |
| Forêt de Subirats (40) ⚠️ | Subirats › Alt Penedès | 1 |
| Forêt de Subirats (41) ⚠️ | Subirats › Alt Penedès | 1 |
| Forêt de Subirats (42) ⚠️ | Subirats › Alt Penedès | 1 |
| Forêt de Olivella (8) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Sant Cugat Sesgarrigues (4) ⚠️ | Sant Cugat Sesgarrigues › Alt Penedès | 1 |
| Forêt de Sant Cugat Sesgarrigues (5) ⚠️ | Sant Cugat Sesgarrigues › Alt Penedès | 1 |
| Forêt de Olesa de Bonesvalls (21) ⚠️ | Olesa de Bonesvalls › Alt Penedès | 1 |
| Forêt de Avinyonet del Penedès (46) ⚠️ | Avinyonet del Penedès › Alt Penedès | 1 |
| Forêt de Subirats (48) ⚠️ | Subirats › Alt Penedès | 1 |
| Forêt de Avinyonet del Penedès (47) ⚠️ | Avinyonet del Penedès › Alt Penedès | 1 |
| Forêt de Avinyonet del Penedès (48) ⚠️ | Avinyonet del Penedès › Alt Penedès | 1 |
| Forêt de Olèrdola (23) ⚠️ | Olèrdola › Alt Penedès | 1 |
| Jardins de Ca l'Aranyó ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Olesa de Bonesvalls (22) ⚠️ | Olesa de Bonesvalls › Alt Penedès | 1 |
| Forêt de Sant Pere de Ribes (28) ⚠️ | Sant Pere de Ribes › Garraf | 1 |
| Forêt de Sant Pere de Ribes (29) ⚠️ | Sant Pere de Ribes › Garraf | 1 |
| Bosc de les Taules ⚠️ | Parets del Vallès › Vallès Oriental | 1 |
| Forêt de Sant Pere de Ribes (37) ⚠️ | Sant Pere de Ribes › Garraf | 1 |
| Forêt de Sant Pere de Ribes (40) ⚠️ | Sant Pere de Ribes › Garraf | 1 |
| Forêt de Sant Pere de Ribes (42) ⚠️ | Sant Pere de Ribes › Garraf | 1 |
| Forêt de Sant Pere de Ribes (43) ⚠️ | Sant Pere de Ribes › Garraf | 1 |
| Forêt de Sant Pere de Ribes (48) ⚠️ | Sant Pere de Ribes › Garraf | 1 |
| Parc del Molí d'en Rovira ⚠️ | Vilafranca del Penedès › Alt Penedès | 1 |
| Forêt de Sant Pere de Ribes (50) ⚠️ | Sant Pere de Ribes › Garraf | 1 |
| Parc de Sant Julià ⚠️ | Vilafranca del Penedès › Alt Penedès | 1 |
| Parc de Llevant ⚠️ | Vilafranca del Penedès › Alt Penedès | 1 |
| Forêt de Sant Pere de Ribes (53) ⚠️ | Sant Pere de Ribes › Garraf | 1 |
| Forêt de Olivella (15) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Olivella (20) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Olivella (21) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Olivella (23) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Olivella (27) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Olivella (31) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Olivella (33) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Olivella (38) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Sitges (5) ⚠️ | Sitges › Garraf | 1 |
| Forêt de Sant Pere de Ribes (59) ⚠️ | Sant Pere de Ribes › Garraf | 1 |
| Forêt de Sant Pere de Ribes (60) ⚠️ | Sant Pere de Ribes › Garraf | 1 |
| Forêt de Sant Pere de Ribes (61) ⚠️ | Sant Pere de Ribes › Garraf | 1 |
| Forêt de Sant Pere de Ribes (63) ⚠️ | Sant Pere de Ribes › Garraf | 1 |
| Forêt de Olesa de Bonesvalls (23) ⚠️ | Olesa de Bonesvalls › Alt Penedès | 1 |
| Forêt de Subirats (61) ⚠️ | Subirats › Alt Penedès | 1 |
| Zona verda Can Sabat ⚠️ | Sant Vicenç dels Horts › Baix Llobregat | 1 |
| Forêt de Vallirana (11) ⚠️ | Vallirana › Baix Llobregat | 1 |
| Forêt de Olesa de Bonesvalls (29) ⚠️ | Olesa de Bonesvalls › Alt Penedès | 1 |
| Forêt de Olèrdola (33) ⚠️ | Olèrdola › Alt Penedès | 1 |
| Forêt de Olèrdola (35) ⚠️ | Olèrdola › Alt Penedès | 1 |
| Forêt de Olèrdola (36) ⚠️ | Olèrdola › Alt Penedès | 1 |
| Forêt de Olèrdola (38) ⚠️ | Olèrdola › Alt Penedès | 1 |
| Forêt de Olèrdola (40) ⚠️ | Olèrdola › Alt Penedès | 1 |
| Forêt de Olèrdola (44) ⚠️ | Olèrdola › Alt Penedès | 1 |
| Forêt de Olèrdola (45) ⚠️ | Olèrdola › Alt Penedès | 1 |
| Forêt de Olèrdola (46) ⚠️ | Olèrdola › Alt Penedès | 1 |
| Forêt de Santa Margarida i els Monjos (3) ⚠️ | Santa Margarida i els Monjos › Alt Penedès | 1 |
| Forêt de Olèrdola (52) ⚠️ | Olèrdola › Alt Penedès | 1 |
| Forêt de Santa Margarida i els Monjos (5) ⚠️ | Santa Margarida i els Monjos › Alt Penedès | 1 |
| Forêt de Santa Margarida i els Monjos (6) ⚠️ | Santa Margarida i els Monjos › Alt Penedès | 1 |
| Forêt de Santa Margarida i els Monjos (8) ⚠️ | Santa Margarida i els Monjos › Alt Penedès | 1 |
| Forêt de Santa Margarida i els Monjos (12) ⚠️ | Santa Margarida i els Monjos › Alt Penedès | 1 |
| Forêt de Santa Margarida i els Monjos (13) ⚠️ | Santa Margarida i els Monjos › Alt Penedès | 1 |
| Bois de Sant Sadurní d'Anoia ⚠️ | Sant Sadurní d'Anoia › Alt Penedès | 1 |
| Forêt de Castellet i la Gornal (11) ⚠️ | Castellet i la Gornal › Alt Penedès | 1 |
| Forêt de Castellet i la Gornal (14) ⚠️ | Castellet i la Gornal › Alt Penedès | 1 |
| Forêt de Castellet i la Gornal (18) ⚠️ | Castellet i la Gornal › Alt Penedès | 1 |
| Forêt de Mollet del Vallès (2) ⚠️ | Mollet del Vallès › Vallès Oriental | 1 |
| Parc del Poblenou ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Castellet i la Gornal (24) ⚠️ | Castellet i la Gornal › Alt Penedès | 1 |
| Parc de L'Auditori ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de Can Sabaté ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de la Font Florida ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Santa Margarida i els Monjos (16) ⚠️ | Santa Margarida i els Monjos › Alt Penedès | 1 |
| Forêt de Castellet i la Gornal (29) ⚠️ | Castellet i la Gornal › Alt Penedès | 1 |
| Forêt de Castellet i la Gornal (31) ⚠️ | Castellet i la Gornal › Alt Penedès | 1 |
| Forêt de Castellet i la Gornal (35) ⚠️ | Castellet i la Gornal › Alt Penedès | 1 |
| Forêt de Castellet i la Gornal (38) ⚠️ | Castellet i la Gornal › Alt Penedès | 1 |
| Plaça del Mil·lenari de Barberà ⚠️ | Barberà del Vallès › Vallès Occidental | 1 |
| Forêt de Sabadell (6) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Forêt de Matadepera (3) ⚠️ | Matadepera › Vallès Occidental | 1 |
| Forêt de Castellet i la Gornal (44) ⚠️ | Castellet i la Gornal › Alt Penedès | 1 |
| Forêt de Manresa (4) ⚠️ | Manresa › Bages | 1 |
| Forêt de Castellet i la Gornal (46) ⚠️ | Castellet i la Gornal › Alt Penedès | 1 |
| Forêt de Castellet i la Gornal (47) ⚠️ | Castellet i la Gornal › Alt Penedès | 1 |
| Forêt de Vilanova i la Geltrú (7) ⚠️ | Vilanova i la Geltrú › Garraf | 1 |
| Forêt de Vallirana (14) ⚠️ | Vallirana › Baix Llobregat | 1 |
| Plaça del vuit de març ⚠️ | Manresa › Bages | 1 |
| Parc de Josep Vidal ⚠️ | Manresa › Bages | 1 |
| Parc de Manresa (13) ⚠️ | Manresa › Bages | 1 |
| Bosc de la Concòrdia ⚠️ | Sabadell › Vallès Occidental | 1 |
| El Camet de la Colònia Güell ⚠️ | Santa Coloma de Cervelló › Baix Llobregat | 1 |
| Parc de Vallbona ⚠️ | Igualada › Anoia | 1 |
| Parc de Valldaura ⚠️ | Igualada › Anoia | 1 |
| Plaça de Cal Gravat ⚠️ | Manresa › Bages | 1 |
| Parc d'Europa (3) ⚠️ | Martorell › Baix Llobregat | 1 |
| Parc de Manresa (16) ⚠️ | Manresa › Bages | 1 |
| Forêt de Castellet i la Gornal (54) ⚠️ | Castellet i la Gornal › Alt Penedès | 1 |
| Forêt de Castellet i la Gornal (56) ⚠️ | Castellet i la Gornal › Alt Penedès | 1 |
| Forêt de Castellet i la Gornal (57) ⚠️ | Castellet i la Gornal › Alt Penedès | 1 |
| Forêt de Castellví de la Marca (9) ⚠️ | Castellví de la Marca › Alt Penedès | 1 |
| Forêt de Castellví de la Marca (15) ⚠️ | Castellví de la Marca › Alt Penedès | 1 |
| Forêt de Castellví de la Marca (19) ⚠️ | Castellví de la Marca › Alt Penedès | 1 |
| Forêt de Castellví de la Marca (20) ⚠️ | Castellví de la Marca › Alt Penedès | 1 |
| Forêt de Castellví de la Marca (21) ⚠️ | Castellví de la Marca › Alt Penedès | 1 |
| Forêt de Castellví de la Marca (23) ⚠️ | Castellví de la Marca › Alt Penedès | 1 |
| Forêt de Castellví de la Marca (25) ⚠️ | Castellví de la Marca › Alt Penedès | 1 |
| Forêt de Castellví de la Marca (26) ⚠️ | Castellví de la Marca › Alt Penedès | 1 |
| Parc de les Rieres d'Horta ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de la Granada ⚠️ | la Granada › Alt Penedès | 1 |
| Forêt de la Granada (2) ⚠️ | la Granada › Alt Penedès | 1 |
| Forêt de Subirats (67) ⚠️ | Subirats › Alt Penedès | 1 |
| Forêt de Subirats (71) ⚠️ | Subirats › Alt Penedès | 1 |
| Forêt de Sant Sadurní d'Anoia (5) ⚠️ | Sant Sadurní d'Anoia › Alt Penedès | 1 |
| Forêt de Subirats (75) ⚠️ | Subirats › Alt Penedès | 1 |
| Forêt de Sant Esteve Sesrovires (3) ⚠️ | Sant Esteve Sesrovires › Baix Llobregat | 1 |
| Forêt de Sant Esteve Sesrovires (4) ⚠️ | Sant Esteve Sesrovires › Baix Llobregat | 1 |
| Forêt de Castellví de Rosanes (2) ⚠️ | Castellví de Rosanes › Baix Llobregat | 1 |
| Forêt de Castellví de Rosanes (3) ⚠️ | Castellví de Rosanes › Baix Llobregat | 1 |
| Forêt de Sant Esteve Sesrovires (7) ⚠️ | Sant Esteve Sesrovires › Baix Llobregat | 1 |
| Forêt de Sant Esteve Sesrovires (10) ⚠️ | Sant Esteve Sesrovires › Baix Llobregat | 1 |
| Forêt de Sant Esteve Sesrovires (11) ⚠️ | Sant Esteve Sesrovires › Baix Llobregat | 1 |
| Forêt de Sant Llorenç d'Hortons (12) ⚠️ | Sant Llorenç d'Hortons › Alt Penedès | 1 |
| Forêt de Masquefa (4) ⚠️ | Masquefa › Anoia | 1 |
| Forêt de Bigues i Riells del Fai (3) ⚠️ | Bigues i Riells del Fai › Vallès Oriental | 1 |
| Forêt de Gelida (11) ⚠️ | Gelida › Alt Penedès | 1 |
| Forêt de Gelida (12) ⚠️ | Gelida › Alt Penedès | 1 |
| Forêt de Gelida (13) ⚠️ | Gelida › Alt Penedès | 1 |
| Forêt de Gelida (15) ⚠️ | Gelida › Alt Penedès | 1 |
| Forêt de Gelida (16) ⚠️ | Gelida › Alt Penedès | 1 |
| Forêt de Sant Llorenç d'Hortons (27) ⚠️ | Sant Llorenç d'Hortons › Alt Penedès | 1 |
| Forêt de Sant Llorenç d'Hortons (29) ⚠️ | Sant Llorenç d'Hortons › Alt Penedès | 1 |
| Forêt de Sant Llorenç d'Hortons (30) ⚠️ | Sant Llorenç d'Hortons › Alt Penedès | 1 |
| Forêt de Sant Llorenç d'Hortons (31) ⚠️ | Sant Sadurní d'Anoia › Alt Penedès | 1 |
| Forêt de Sant Llorenç d'Hortons (32) ⚠️ | Sant Llorenç d'Hortons › Alt Penedès | 1 |
| Forêt de Masquefa (6) ⚠️ | Masquefa › Anoia | 1 |
| Forêt de Masquefa (8) ⚠️ | Masquefa › Anoia | 1 |
| Forêt de Sant Llorenç d'Hortons (33) ⚠️ | Sant Llorenç d'Hortons › Alt Penedès | 1 |
| Forêt de Sant Sadurní d'Anoia (7) ⚠️ | Sant Sadurní d'Anoia › Alt Penedès | 1 |
| Forêt de Sant Sadurní d'Anoia (10) ⚠️ | Sant Sadurní d'Anoia › Alt Penedès | 1 |
| Forêt de Sant Sadurní d'Anoia (13) ⚠️ | Sant Sadurní d'Anoia › Alt Penedès | 1 |
| Forêt de Sant Sadurní d'Anoia (15) ⚠️ | Sant Sadurní d'Anoia › Alt Penedès | 1 |
| Forêt de Sant Sadurní d'Anoia (17) ⚠️ | Sant Sadurní d'Anoia › Alt Penedès | 1 |
| Forêt de Sant Sadurní d'Anoia (18) ⚠️ | Sant Sadurní d'Anoia › Alt Penedès | 1 |
| Forêt de Torrelavit (8) ⚠️ | Torrelavit › Alt Penedès | 1 |
| Forêt de Torrelavit (9) ⚠️ | Torrelavit › Alt Penedès | 1 |
| Forêt de Torrelavit (11) ⚠️ | Torrelavit › Alt Penedès | 1 |
| Forêt de Sant Sadurní d'Anoia (21) ⚠️ | Sant Sadurní d'Anoia › Alt Penedès | 1 |
| Forêt de Torrelavit (12) ⚠️ | Torrelavit › Alt Penedès | 1 |
| Jardins de Lola Anglada ⚠️ | Cardedeu › Vallès Oriental | 1 |
| Plaça de Miquel Martí i Pol ⚠️ | Cardedeu › Vallès Oriental | 1 |
| els Pujols ⚠️ | la Granada › Alt Penedès | 1 |
| Parc de les Cascades ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Font-rubí (12) ⚠️ | Font-rubí › Alt Penedès | 1 |
| Forêt de Sant Martí Sarroca (5) ⚠️ | Sant Martí Sarroca › Alt Penedès | 1 |
| Forêt de Pacs del Penedès (7) ⚠️ | Pacs del Penedès › Alt Penedès | 1 |
| Forêt de Sant Martí Sarroca (8) ⚠️ | Sant Martí Sarroca › Alt Penedès | 1 |
| Forêt de Torrelles de Llobregat (13) ⚠️ | Torrelles de Llobregat › Baix Llobregat | 1 |
| Forêt de Sant Martí Sarroca (16) ⚠️ | Sant Martí Sarroca › Alt Penedès | 1 |
| Forêt de Castellví de la Marca (29) ⚠️ | Castellví de la Marca › Alt Penedès | 1 |
| Forêt de Castellví de la Marca (31) ⚠️ | Castellví de la Marca › Alt Penedès | 1 |
| Forêt de Castellví de la Marca (32) ⚠️ | Castellví de la Marca › Alt Penedès | 1 |
| Zona de barbacoes del polígon ⚠️ | els Hostalets de Pierola › Anoia | 1 |
| Parc de la Bòbila ⚠️ | Sant Sadurní d'Anoia › Alt Penedès | 1 |
| Plaça del Pont Romà ⚠️ | Sant Sadurní d'Anoia › Alt Penedès | 1 |
| Parc de Josep Pla ⚠️ | Sant Andreu de la Barca › Baix Llobregat | 1 |
| Parc urbà de la Vila ⚠️ | Esparreguera › Baix Llobregat | 1 |
| Parc de Joan Cluselles i Teixé ⚠️ | Cardedeu › Vallès Oriental | 1 |
| Parc de Cardedeu (11) ⚠️ | Cardedeu › Vallès Oriental | 1 |
| Parc dels Enamorats ⚠️ | Santa Maria de Palautordera › Vallès Oriental | 1 |
| Parc de Santa Maria de Palautordera ⚠️ | Santa Maria de Palautordera › Vallès Oriental | 1 |
| Forêt de Sant Martí Sarroca (23) ⚠️ | Sant Martí Sarroca › Alt Penedès | 1 |
| Parc dels Auditoris - El Parc del Fòrum ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Castellví de la Marca (44) ⚠️ | Castellví de la Marca › Alt Penedès | 1 |
| Forêt de Castellví de la Marca (46) ⚠️ | Castellví de la Marca › Alt Penedès | 1 |
| Forêt de Castellví de la Marca (52) ⚠️ | Castellví de la Marca › Alt Penedès | 1 |
| Forêt de Castellví de la Marca (53) ⚠️ | Castellví de la Marca › Alt Penedès | 1 |
| Forêt de Caldes de Montbui (4) ⚠️ | Caldes de Montbui › Vallès Oriental | 1 |
| Forêt de Bigues i Riells del Fai (10) ⚠️ | Caldes de Montbui › Vallès Oriental | 1 |
| Jardins de Blanca Selva i Henry ⚠️ | Barcelona › Barcelonès | 1 |
| Jardins de Sant Joan de Déu ⚠️ | Barcelona › Barcelonès | 1 |
| Jardins del Doctor Samuel Hahnemann ⚠️ | Barcelona › Barcelonès | 1 |
| Jardins d'Emma de Barcelona ⚠️ | Barcelona › Barcelonès | 1 |
| Plaça de Margarita Rivière Martí ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de les Corts ⚠️ | Barcelona › Barcelonès | 1 |
| Jardins de Can Cuiàs ⚠️ | Barcelona › Barcelonès | 1 |
| Jardins de Magalí ⚠️ | Barcelona › Barcelonès | 1 |
| Plaça del Doctor Letamendi ⚠️ | Barcelona › Barcelonès | 1 |
| Turó Parc ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Fonollosa (3) ⚠️ | Fonollosa › Bages | 1 |
| Parc de Manresa (21) ⚠️ | Manresa › Bages | 1 |
| Parc de el Pont de Vilomara i Rocafort (9) ⚠️ | el Pont de Vilomara i Rocafort › Bages | 1 |
| Parc de les Set Fonts ⚠️ | Sant Julià de Vilatorta › Osona (Barcelone) | 1 |
| Parc de Barcelona (66) ⚠️ | Barcelona › Barcelonès | 1 |
| Plaça del Nen de la Rutlla ⚠️ | Barcelona › Barcelonès | 1 |
| Plaça de Catalunya (5) ⚠️ | Cornellà de Llobregat › Baix Llobregat | 1 |
| Plaça Verda de la Prosperitat ⚠️ | Barcelona › Barcelonès | 1 |
| Plaça de Nou Barris ⚠️ | Barcelona › Barcelonès | 1 |
| Jardins de la Tamarita ⚠️ | Barcelona › Barcelonès | 1 |
| Jardins de les Basses de Sant Pere ⚠️ | Sant Just Desvern › Baix Llobregat | 1 |
| Forêt de Castellgalí (5) ⚠️ | Castellgalí › Bages | 1 |
| Parc de Xavier Montsalvatge ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de Barcelona (72) ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Fonollosa (10) ⚠️ | Fonollosa › Bages | 1 |
| Forêt de Fonollosa (12) ⚠️ | Fonollosa › Bages | 1 |
| Forêt de Fonollosa (14) ⚠️ | Fonollosa › Bages | 1 |
| Forêt de Fonollosa (15) ⚠️ | Fonollosa › Bages | 1 |
| Forêt de Fonollosa (16) ⚠️ | Fonollosa › Bages | 1 |
| Forêt de Fonollosa (18) ⚠️ | Fonollosa › Bages | 1 |
| Bois de Sant Feliu de Codines ⚠️ | Sant Feliu de Codines › Vallès Oriental | 1 |
| Forêt de Sant Mateu de Bages (5) ⚠️ | Sant Mateu de Bages › Bages | 1 |
| Jardins de l'Estany de Sant Maurici ⚠️ | el Prat de Llobregat › Baix Llobregat | 1 |
| Boscos de Can Ferrer ⚠️ | Piera › Anoia | 1 |
| Boscos Can Ferrer ⚠️ | Piera › Anoia | 1 |
| Bois de Piera ⚠️ | Piera › Anoia | 1 |
| Jardins de Sant Cristòfol ⚠️ | Barcelona › Barcelonès | 1 |
| Plaça de l'1 d'Octubre (2) ⚠️ | Vilanova i la Geltrú › Garraf | 1 |
| Parc de Sant Just Desvern ⚠️ | Sant Just Desvern › Baix Llobregat | 1 |
| Bois de Piera (3) ⚠️ | Piera › Anoia | 1 |
| Parc de Sabadell (19) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Plaça dels Franciscans ⚠️ | Vilanova i la Geltrú › Garraf | 1 |
| Bois de Sabadell (19) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Bois de Sabadell (20) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Parc de Sabadell (24) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Jardins d'Andalusia ⚠️ | el Prat de Llobregat › Baix Llobregat | 1 |
| Parc de el Prat de Llobregat (3) ⚠️ | el Prat de Llobregat › Baix Llobregat | 1 |
| Jardins de la Pau ⚠️ | el Prat de Llobregat › Baix Llobregat | 1 |
| Bois de el Prat de Llobregat (63) ⚠️ | el Prat de Llobregat › Baix Llobregat | 1 |
| Bois de Cabrils (2) ⚠️ | Cabrils › Maresme | 1 |
| Parc dels Tortosins ⚠️ | Vic › Osona (Barcelone) | 1 |
| Bois de Òrrius (7) ⚠️ | Òrrius › Maresme | 1 |
| Parc de l'Església ⚠️ | Abrera › Baix Llobregat | 1 |
| Plaça de l'Endalet ⚠️ | Premià de Mar › Maresme | 1 |
| Plaça de Francesc Macià (2) ⚠️ | Premià de Mar › Maresme | 1 |
| Parc del Blat ⚠️ | Vic › Osona (Barcelone) | 1 |
| Plaça de Carmen Tórtola Valencia ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de Can Cassany ⚠️ | Vic › Osona (Barcelone) | 1 |
| Parc de l'Ordi ⚠️ | Vic › Osona (Barcelone) | 1 |
| Parc dels Estudis ⚠️ | Vic › Osona (Barcelone) | 1 |
| Parc de l'Horta de la Sínia ⚠️ | Vic › Osona (Barcelone) | 1 |
| Plaça de les Vinyes ⚠️ | Santa Coloma de Cervelló › Baix Llobregat | 1 |
| Parc de Gurb (3) ⚠️ | Gurb › Osona (Barcelone) | 1 |
| Parc de Jaume Balmes ⚠️ | Vic › Osona (Barcelone) | 1 |
| Bois de el Prat de Llobregat (191) ⚠️ | el Prat de Llobregat › Baix Llobregat | 1 |
| Bois de el Prat de Llobregat (192) ⚠️ | el Prat de Llobregat › Baix Llobregat | 1 |
| Bois de el Prat de Llobregat (193) ⚠️ | el Prat de Llobregat › Baix Llobregat | 1 |
| Bois de el Prat de Llobregat (194) ⚠️ | el Prat de Llobregat › Baix Llobregat | 1 |
| Bois de el Prat de Llobregat (195) ⚠️ | el Prat de Llobregat › Baix Llobregat | 1 |
| Bois de Viladecans (15) ⚠️ | Viladecans › Baix Llobregat | 1 |
| Bois de Viladecans (53) ⚠️ | Viladecans › Baix Llobregat | 1 |
| Bois de Santa Coloma de Cervelló (9) ⚠️ | Santa Coloma de Cervelló › Baix Llobregat | 1 |
| Bois de Santa Coloma de Cervelló (13) ⚠️ | Santa Coloma de Cervelló › Baix Llobregat | 1 |
| Parc de la Sardana ⚠️ | Tordera › Maresme | 1 |
| Forêt de Palafolls (20) ⚠️ | Palafolls › Maresme | 1 |
| Bois de Vilassar de Dalt (6) ⚠️ | Vilassar de Dalt › Maresme | 1 |
| Bois de Vilassar de Dalt (8) ⚠️ | Vilassar de Dalt › Maresme | 1 |
| Bois de la Roca del Vallès (11) ⚠️ | la Roca del Vallès › Vallès Oriental | 1 |
| Bois de Argentona (6) ⚠️ | la Roca del Vallès › Vallès Oriental | 1 |
| Bois de Òrrius (17) ⚠️ | Òrrius › Maresme | 1 |
| Bois de Vilassar de Dalt (19) ⚠️ | Vilassar de Dalt › Maresme | 1 |
| Bois de Santa Coloma de Cervelló (29) ⚠️ | Santa Coloma de Cervelló › Baix Llobregat | 1 |
| Bois de Santa Coloma de Cervelló (43) ⚠️ | Santa Coloma de Cervelló › Baix Llobregat | 1 |
| Bois de Argentona (15) ⚠️ | Argentona › Maresme | 1 |
| Bois de Argentona (18) ⚠️ | Argentona › Maresme | 1 |
| Bois de Argentona (22) ⚠️ | Argentona › Maresme | 1 |
| Bois de Argentona (24) ⚠️ | Argentona › Maresme | 1 |
| Bois de Argentona (30) ⚠️ | Argentona › Maresme | 1 |
| Bois de Santa Coloma de Cervelló (55) ⚠️ | Santa Coloma de Cervelló › Baix Llobregat | 1 |
| Bois de Dosrius (3) ⚠️ | Dosrius › Maresme | 1 |
| Bois de la Roca del Vallès (33) ⚠️ | la Roca del Vallès › Vallès Oriental | 1 |
| Bois de Llinars del Vallès (2) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Bois de Llinars del Vallès (8) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Forêt de Montmajor (7) ⚠️ | Montmajor › Berguedà | 1 |
| Forêt de Castellar del Riu (5) ⚠️ | Castellar del Riu › Berguedà | 1 |
| Forêt de Òdena (3) ⚠️ | Òdena › Anoia | 1 |
| Forêt de Òdena (5) ⚠️ | Òdena › Anoia | 1 |
| Bois de Llinars del Vallès (11) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Bois de Llinars del Vallès (12) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Bois de Llinars del Vallès (16) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Bois de Llinars del Vallès (18) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Bois de Llinars del Vallès (20) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Laberint d'Horta ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de Barberà del Vallès ⚠️ | Barberà del Vallès › Vallès Occidental | 1 |
| Parc de Can Lluc ⚠️ | Santa Coloma de Cervelló › Baix Llobregat | 1 |
| Parc de Sant Celoni (13) ⚠️ | Sant Celoni › Vallès Oriental | 1 |
| Forêt de la Roca del Vallès (3) ⚠️ | la Roca del Vallès › Vallès Oriental | 1 |
| Forêt de Granollers ⚠️ | Granollers › Vallès Oriental | 1 |
| Jardins de Miquel Martí i Pol ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Parc de Sant Celoni (17) ⚠️ | Sant Celoni › Vallès Oriental | 1 |
| Forêt de Mura ⚠️ | Mura › Bages | 1 |
| Forêt de Sant Llorenç Savall (4) ⚠️ | Sant Llorenç Savall › Vallès Occidental | 1 |
| Forêt de Santa Maria de Palautordera (6) ⚠️ | Santa Maria de Palautordera › Vallès Oriental | 1 |
| Parc de la Bòbila (2) ⚠️ | Badalona › Barcelonès | 1 |
| Parc de Cerdanyola del Vallès (11) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Forêt de Cerdanyola del Vallès (30) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Parc de Gassó Vargas ⚠️ | Ripollet › Vallès Occidental | 1 |
| Parc Primer de Maig ⚠️ | Ripollet › Vallès Occidental | 1 |
| Parc Massot ⚠️ | Ripollet › Vallès Occidental | 1 |
| Parc de Rizal ⚠️ | Ripollet › Vallès Occidental | 1 |
| Parc Carles Ferré ⚠️ | Ripollet › Vallès Occidental | 1 |
| Forêt de Ripollet ⚠️ | Ripollet › Vallès Occidental | 1 |
| Forêt de Avià (2) ⚠️ | Avià › Berguedà | 1 |
| Parc del Lledó ⚠️ | Berga › Berguedà | 1 |
| Plaça del Mil·lenari ⚠️ | Montmeló › Vallès Oriental | 1 |
| Forêt de Òdena (16) ⚠️ | Òdena › Anoia | 1 |
| Forêt de Òdena (17) ⚠️ | Òdena › Anoia | 1 |
| Parc de les Aigües (2) ⚠️ | Montcada i Reixac › Vallès Occidental | 1 |
| Jardins de Rodrigo Caro ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Piera (8) ⚠️ | Piera › Anoia | 1 |
| Forêt de Piera (9) ⚠️ | Piera › Anoia | 1 |
| Forêt de Piera (12) ⚠️ | Piera › Anoia | 1 |
| Forêt de Masquefa (11) ⚠️ | Masquefa › Anoia | 1 |
| Forêt de Veciana (4) ⚠️ | Veciana › Anoia | 1 |
| Forêt de Piera (14) ⚠️ | Piera › Anoia | 1 |
| Parc del Gall Mullat ⚠️ | Piera › Anoia | 1 |
| Parc de Mataró (13) ⚠️ | Mataró › Maresme | 1 |
| Parc de Milpins ⚠️ | les Franqueses del Vallès › Vallès Oriental | 1 |
| Plaça Onze de Setembre (3) ⚠️ | Sant Salvador de Guardiola › Bages | 1 |
| Forêt de Sant Salvador de Guardiola (2) ⚠️ | Sant Salvador de Guardiola › Bages | 1 |
| Forêt de Sant Salvador de Guardiola (3) ⚠️ | Sant Salvador de Guardiola › Bages | 1 |
| Forêt de Castellví de la Marca (54) ⚠️ | Castellví de la Marca › Alt Penedès | 1 |
| Bosc de les Saleres ⚠️ | Sant Martí Sarroca › Alt Penedès | 1 |
| Forêt de Castellfollit del Boix (5) ⚠️ | Castellfollit del Boix › Bages | 1 |
| Forêt de Sant Martí Sarroca (24) ⚠️ | Sant Martí Sarroca › Alt Penedès | 1 |
| Bois de Terrassa ⚠️ | Sant Quirze del Vallès › Vallès Occidental | 1 |
| Parc de les Franqueses del Vallès ⚠️ | les Franqueses del Vallès › Vallès Oriental | 1 |
| Plaça de Buenaventura Durruti ⚠️ | Barcelona › Barcelonès | 1 |
| Plaça del Vaixell "Maria Assumpta" ⚠️ | Badalona › Barcelonès | 1 |
| Parc de Barcelona (78) ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Cubelles (7) ⚠️ | Cubelles › Garraf | 1 |
| Forêt de Cubelles (8) ⚠️ | Cubelles › Garraf | 1 |
| Parc de les Muntanyetes ⚠️ | Badalona › Barcelonès | 1 |
| Forêt de Montcada i Reixac (2) ⚠️ | Montcada i Reixac › Vallès Occidental | 1 |
| Forêt de Montcada i Reixac (3) ⚠️ | Montcada i Reixac › Vallès Occidental | 1 |
| Forêt de Veciana (8) ⚠️ | Veciana › Anoia | 1 |
| Forêt de Pujalt (8) ⚠️ | Pujalt › Anoia | 1 |
| Forêt de Pujalt (9) ⚠️ | Pujalt › Anoia | 1 |
| Forêt de Montcada i Reixac (4) ⚠️ | Montcada i Reixac › Vallès Occidental | 1 |
| Parc de Sant Vicenç de Castellet ⚠️ | Sant Vicenç de Castellet › Bages | 1 |
| Parc de les Quatre Estacions (2) ⚠️ | Cànoves i Samalús › Vallès Oriental | 1 |
| Plaça de Sara Llorens ⚠️ | Pineda de Mar › Maresme | 1 |
| Parc de Cerdanyola del Vallès (12) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Parc de Sant Celoni (20) ⚠️ | Sant Celoni › Vallès Oriental | 1 |
| Forêt de Castellolí (3) ⚠️ | Castellolí › Anoia | 1 |
| Parc de la Solidaritat (4) ⚠️ | Esplugues de Llobregat › Baix Llobregat | 1 |
| Forêt de Santa Margarida de Montbui (3) ⚠️ | Santa Margarida de Montbui › Anoia | 1 |
| Forêt de Santa Margarida de Montbui (4) ⚠️ | Santa Margarida de Montbui › Anoia | 1 |
| Forêt de Santa Margarida de Montbui (5) ⚠️ | Santa Margarida de Montbui › Anoia | 1 |
| Parc del Clot ⚠️ | Barcelona › Barcelonès | 1 |
| Bois de Barcelona (43) ⚠️ | Barcelona › Barcelonès | 1 |
| Bois de Barcelona (45) ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de Cerdanyola del Vallès (13) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Forêt de Cerdanyola del Vallès (31) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Forêt de Montcada i Reixac (5) ⚠️ | Montcada i Reixac › Vallès Occidental | 1 |
| Can Xarau ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Forêt de Montcada i Reixac (12) ⚠️ | Montcada i Reixac › Vallès Occidental | 1 |
| Forêt de Sabadell (8) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Forêt de Sabadell (10) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Forêt de Santa Perpètua de Mogoda (11) ⚠️ | Santa Perpètua de Mogoda › Vallès Occidental | 1 |
| Bosc de Can Trabau ⚠️ | Santa Perpètua de Mogoda › Vallès Occidental | 1 |
| Bois de Argentona (37) ⚠️ | Argentona › Maresme | 1 |
| Bois de Argentona (38) ⚠️ | Argentona › Maresme | 1 |
| Bois de Argentona (39) ⚠️ | Argentona › Maresme | 1 |
| Bois de Argentona (42) ⚠️ | Argentona › Maresme | 1 |
| Bois de Argentona (46) ⚠️ | Argentona › Maresme | 1 |
| Bois de Argentona (48) ⚠️ | Argentona › Maresme | 1 |
| Bois de Mataró (6) ⚠️ | Mataró › Maresme | 1 |
| Plaça de la Pau (4) ⚠️ | Vilafranca del Penedès › Alt Penedès | 1 |
| Plaça Vilanova ⚠️ | Vilafranca del Penedès › Alt Penedès | 1 |
| Parc de Moià (2) ⚠️ | Moià › Moianès | 1 |
| Jardins de la Rambla de Sants ⚠️ | Barcelona › Barcelonès | 1 |
| Plaça de Pau Casals (6) ⚠️ | Canovelles › Vallès Oriental | 1 |
| Bois de Canovelles (9) ⚠️ | Canovelles › Vallès Oriental | 1 |
| Bois de Lliçà d'Amunt (24) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 1 |
| Bois de Canovelles (10) ⚠️ | Canovelles › Vallès Oriental | 1 |
| Bois de Canovelles (13) ⚠️ | Canovelles › Vallès Oriental | 1 |
| Parc de Canovelles (3) ⚠️ | Canovelles › Vallès Oriental | 1 |
| Bosc de Can Many ⚠️ | Granollers › Vallès Oriental | 1 |
| Forêt de Lliçà d'Amunt (13) ⚠️ | Granollers › Vallès Oriental | 1 |
| Forêt de Lliçà d'Amunt (14) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 1 |
| Forêt de Canovelles (6) ⚠️ | Canovelles › Vallès Oriental | 1 |
| Forêt de Canovelles (11) ⚠️ | Canovelles › Vallès Oriental | 1 |
| Bosc de Can Pagès Nou ⚠️ | l'Ametlla del Vallès › Vallès Oriental | 1 |
| Forêt de l'Ametlla del Vallès ⚠️ | l'Ametlla del Vallès › Vallès Oriental | 1 |
| Forêt de l'Ametlla del Vallès (2) ⚠️ | l'Ametlla del Vallès › Vallès Oriental | 1 |
| Forêt de les Franqueses del Vallès (4) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 1 |
| Forêt de Barcelona (15) ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Badalona ⚠️ | Badalona › Barcelonès | 1 |
| Forêt de Barcelona (18) ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Barcelona (21) ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Barcelona (22) ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Montcada i Reixac (19) ⚠️ | Montcada i Reixac › Vallès Occidental | 1 |
| Forêt de Montcada i Reixac (21) ⚠️ | Montcada i Reixac › Vallès Occidental | 1 |
| Forêt de Montcada i Reixac (22) ⚠️ | Montcada i Reixac › Vallès Occidental | 1 |
| Bois de Sant Just Desvern ⚠️ | Sant Just Desvern › Baix Llobregat | 1 |
| Alzines de les Torres ⚠️ | Lliçà de Vall › Vallès Oriental | 1 |
| Forêt de l'Ametlla del Vallès (7) ⚠️ | l'Ametlla del Vallès › Vallès Oriental | 1 |
| Can Ramir ⚠️ | l'Ametlla del Vallès › Vallès Oriental | 1 |
| Parc de Badalona (3) ⚠️ | Badalona › Barcelonès | 1 |
| Forêt de Barcelona (28) ⚠️ | Barcelona › Barcelonès | 1 |
| Parc dels Cirerers ⚠️ | Santa Coloma de Cervelló › Baix Llobregat | 1 |
| Forêt de Barcelona (29) ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Badalona (7) ⚠️ | Badalona › Barcelonès | 1 |
| Forêt de Tiana ⚠️ | Tiana › Maresme | 1 |
| Forêt de Rubí (2) ⚠️ | Rubí › Vallès Occidental | 1 |
| Parc de Cerdanyola del Vallès (16) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Forêt de Sabadell (15) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Forêt de Sabadell (18) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Forêt de Polinyà (3) ⚠️ | Polinyà › Vallès Occidental | 1 |
| Forêt de Polinyà (4) ⚠️ | Polinyà › Vallès Occidental | 1 |
| Forêt de Polinyà (6) ⚠️ | Polinyà › Vallès Occidental | 1 |
| Forêt de Polinyà (8) ⚠️ | Polinyà › Vallès Occidental | 1 |
| Forêt de Sabadell (22) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Forêt de Sabadell (24) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Forêt de Sabadell (28) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Forêt de Sabadell (29) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Forêt de Sabadell (31) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Forêt de Sabadell (34) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Forêt de Sabadell (36) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Forêt de Santa Perpètua de Mogoda (13) ⚠️ | Santa Perpètua de Mogoda › Vallès Occidental | 1 |
| Forêt de Sabadell (39) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Forêt de Palau-solità i Plegamans (5) ⚠️ | Palau-solità i Plegamans › Vallès Occidental | 1 |
| Forêt de Palau-solità i Plegamans (6) ⚠️ | Palau-solità i Plegamans › Vallès Occidental | 1 |
| Forêt de Sant Quirze del Vallès (5) ⚠️ | Sant Quirze del Vallès › Vallès Occidental | 1 |
| Forêt de Terrassa (28) ⚠️ | Terrassa › Vallès Occidental | 1 |
| Parc de Sabadell (26) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Parc de Sant Quirze del Vallès (2) ⚠️ | Sant Quirze del Vallès › Vallès Occidental | 1 |
| Bois de Montcada i Reixac (2) ⚠️ | Montcada i Reixac › Vallès Occidental | 1 |
| Bosc de Can Maiol ⚠️ | Palau-solità i Plegamans › Vallès Occidental | 1 |
| Parc de Polinyà (5) ⚠️ | Polinyà › Vallès Occidental | 1 |
| Forêt de Polinyà (10) ⚠️ | Palau-solità i Plegamans › Vallès Occidental | 1 |
| Parc de Santa Perpètua de Mogoda (7) ⚠️ | Santa Perpètua de Mogoda › Vallès Occidental | 1 |
| Parc de Sabadell (27) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Forêt de Polinyà (13) ⚠️ | Polinyà › Vallès Occidental | 1 |
| Forêt de Polinyà (15) ⚠️ | Polinyà › Vallès Occidental | 1 |
| Parc de Polinyà (11) ⚠️ | Polinyà › Vallès Occidental | 1 |
| Forêt de Lliçà de Vall ⚠️ | Lliçà de Vall › Vallès Oriental | 1 |
| Parc de Parets del Vallès (6) ⚠️ | Parets del Vallès › Vallès Oriental | 1 |
| Parc Neus Català ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de Montcada i Reixac (20) ⚠️ | Montcada i Reixac › Vallès Occidental | 1 |
| la Roureda ⚠️ | Gurb › Osona (Barcelone) | 1 |
| Forêt de les Masies de Voltregà (4) ⚠️ | les Masies de Voltregà › Osona (Barcelone) | 1 |
| Bois de Gurb (6) ⚠️ | Gurb › Osona (Barcelone) | 1 |
| Bois de Gurb (8) ⚠️ | Gurb › Osona (Barcelone) | 1 |
| Bois de Gurb (9) ⚠️ | Gurb › Osona (Barcelone) | 1 |
| Bois de Gurb (10) ⚠️ | Gurb › Osona (Barcelone) | 1 |
| Bois de Manlleu ⚠️ | Manlleu › Osona (Barcelone) | 1 |
| Bois de Gurb (11) ⚠️ | Manlleu › Osona (Barcelone) | 1 |
| Parc de Olesa de Montserrat ⚠️ | Olesa de Montserrat › Baix Llobregat | 1 |
| Turó del Drac ⚠️ | Canet de Mar › Maresme | 1 |
| Plaça Gabriel Pujol ⚠️ | Sabadell › Vallès Occidental | 1 |
| Plaça d'Antoni Llonch ⚠️ | Sabadell › Vallès Occidental | 1 |
| Plaça de l'Abat Oliba ⚠️ | Torelló › Osona (Barcelone) | 1 |
| Parc de Cubelles (3) ⚠️ | Cubelles › Garraf | 1 |
| Parc Torre del Sol ⚠️ | Sant Boi de Llobregat › Baix Llobregat | 1 |
| Parc de Can Carreras ⚠️ | Sant Boi de Llobregat › Baix Llobregat | 1 |
| Forêt de Sant Boi de Llobregat (6) ⚠️ | Sant Boi de Llobregat › Baix Llobregat | 1 |
| Bois de Gurb (17) ⚠️ | Gurb › Osona (Barcelone) | 1 |
| Forêt de Caldes d'Estrac (2) ⚠️ | Caldes d'Estrac › Maresme | 1 |
| Forêt de Caldes d'Estrac (4) ⚠️ | Caldes d'Estrac › Maresme | 1 |
| Parc de Cornellà de Llobregat (15) ⚠️ | Cornellà de Llobregat › Baix Llobregat | 1 |
| Parc de Cornellà de Llobregat (16) ⚠️ | Cornellà de Llobregat › Baix Llobregat | 1 |
| Forêt de Caldes d'Estrac (5) ⚠️ | Caldes d'Estrac › Maresme | 1 |
| Parc de Molins de Rei (2) ⚠️ | Molins de Rei › Baix Llobregat | 1 |
| Parc de Sant Boi de Llobregat (9) ⚠️ | Sant Boi de Llobregat › Baix Llobregat | 1 |
| Parc de Sant Celoni (26) ⚠️ | Sant Celoni › Vallès Oriental | 1 |
| Parc de Sant Celoni (28) ⚠️ | Sant Celoni › Vallès Oriental | 1 |
| Parc de Monterols ⚠️ | Barcelona › Barcelonès | 1 |
| Jardí Ferran Soldevila ⚠️ | Barcelona › Barcelonès | 1 |
| Jardins del Palau de les Heures ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de Fibracolor ⚠️ | Tordera › Maresme | 1 |
| Prudenci Bertrana ⚠️ | Tordera › Maresme | 1 |
| Parc de Sant Adrià de Besòs ⚠️ | Sant Adrià de Besòs › Barcelonès | 1 |
| Parc de la Ribera (2) ⚠️ | Cornellà de Llobregat › Baix Llobregat | 1 |
| Forêt de Cabrera d'Anoia ⚠️ | Cabrera d'Anoia › Anoia | 1 |
| Forêt de Cabrera d'Anoia (3) ⚠️ | Cabrera d'Anoia › Anoia | 1 |
| Forêt de Castellar del Vallès (8) ⚠️ | Castellar del Vallès › Vallès Occidental | 1 |
| Forêt de Monistrol de Calders (2) ⚠️ | Monistrol de Calders › Moianès | 1 |
| Bois de Sabadell (21) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Plaça de la Vila (3) ⚠️ | Lliçà de Vall › Vallès Oriental | 1 |
| Forêt de Castellterçol ⚠️ | Castellterçol › Moianès | 1 |
| Parc de Viladecavalls (8) ⚠️ | Viladecavalls › Vallès Occidental | 1 |
| Parc de Sant Boi de Llobregat (10) ⚠️ | Sant Boi de Llobregat › Baix Llobregat | 1 |
| Parc de Vic (13) ⚠️ | Vic › Osona (Barcelone) | 1 |
| Parc de Vic (14) ⚠️ | Vic › Osona (Barcelone) | 1 |
| Forêt de Barcelona (31) ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Rajadell (3) ⚠️ | Rajadell › Bages | 1 |
| Forêt de Avinyó ⚠️ | Avinyó › Bages | 1 |
| Forêt de Balsareny (3) ⚠️ | Balsareny › Bages | 1 |
| Forêt de Calders (3) ⚠️ | Calders › Moianès | 1 |
| Parc d'Antoni Santiburcio ⚠️ | Barcelona › Barcelonès | 1 |
| Parc Fèlix Cucurull ⚠️ | Arenys de Mar › Maresme | 1 |
| Forêt de Llinars del Vallès ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Plaça d'Hostafrancs ⚠️ | Sabadell › Vallès Occidental | 1 |
| Bois de Cardedeu ⚠️ | Cardedeu › Vallès Oriental | 1 |
| Forêt de Sant Pere de Torelló (13) ⚠️ | Sant Pere de Torelló › Osona (Barcelone) | 1 |
| Parc Gassó Vargas (3) ⚠️ | Ripollet › Vallès Occidental | 1 |
| Parc de Ripollet (16) ⚠️ | Ripollet › Vallès Occidental | 1 |
| Forêt de Castellterçol (9) ⚠️ | Castellterçol › Moianès | 1 |
| Parc de Ripollet (19) ⚠️ | Ripollet › Vallès Occidental | 1 |
| Bois de Vilanova del Vallès (7) ⚠️ | Vilanova del Vallès › Vallès Oriental | 1 |
| Parc de Mataró (16) ⚠️ | Mataró › Maresme | 1 |
| Parc de Santa Coloma de Gramenet (3) ⚠️ | Santa Coloma de Gramenet › Barcelonès | 1 |
| Parc de Santa Coloma de Gramenet (5) ⚠️ | Santa Coloma de Gramenet › Barcelonès | 1 |
| Parc Sandino ⚠️ | Santa Coloma de Gramenet › Barcelonès | 1 |
| Parc de Josep Moragas ⚠️ | Santa Coloma de Gramenet › Barcelonès | 1 |
| Forêt de Aiguafreda (3) ⚠️ | Aiguafreda › Osona (Barcelone) | 1 |
| Bois de Viladecavalls (3) ⚠️ | Viladecavalls › Vallès Occidental | 1 |
| Parc de Sant Boi de Llobregat (36) ⚠️ | Sant Boi de Llobregat › Baix Llobregat | 1 |
| Forêt de Oristà (8) ⚠️ | Oristà › Lluçanès | 1 |
| Parc de Sabadell (35) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Bois de Sabadell (22) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Parc de Parets del Vallès (8) ⚠️ | Parets del Vallès › Vallès Oriental | 1 |
| Parc de Can Boada (2) ⚠️ | Mataró › Maresme | 1 |
| Plaça de l'Onze de Setembre (5) ⚠️ | Mataró › Maresme | 1 |
| Parc de Mataró (21) ⚠️ | Mataró › Maresme | 1 |
| Parc de Terrassa (19) ⚠️ | Terrassa › Vallès Occidental | 1 |
| Parc de Can Llobera ⚠️ | Sant Feliu de Llobregat › Baix Llobregat | 1 |
| Parc Mare Paula ⚠️ | Arenys de Mar › Maresme | 1 |
| Parc de la Romeua ⚠️ | Sabadell › Vallès Occidental | 1 |
| Bois de l'Hospitalet de Llobregat ⚠️ | l'Hospitalet de Llobregat › Barcelonès | 1 |
| Bois de l'Hospitalet de Llobregat (2) ⚠️ | l'Hospitalet de Llobregat › Barcelonès | 1 |
| Plaça de la República (3) ⚠️ | Rubí › Vallès Occidental | 1 |
| Plaça de Pau Picasso ⚠️ | Montornès del Vallès › Vallès Oriental | 1 |
| Plaça dels Remences ⚠️ | Montornès del Vallès › Vallès Oriental | 1 |
| Parc de Barcelona (109) ⚠️ | Barcelona › Barcelonès | 1 |
| Parc del Migdia ⚠️ | Manresa › Bages | 1 |
| Jardins Maria Mercè Marçal ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de Santpedor (6) ⚠️ | Santpedor › Bages | 1 |
| Parc de Santa Susanna (2) ⚠️ | Santa Susanna › Maresme | 1 |
| Parc de les destreses, o dels Arenys ⚠️ | Castellbisbal › Vallès Occidental | 1 |
| Parc de la Riera de Viladecans ⚠️ | Viladecans › Baix Llobregat | 1 |
| Parc de Can Ginestar ⚠️ | Viladecans › Baix Llobregat | 1 |
| Parc de Viladecans ⚠️ | Viladecans › Baix Llobregat | 1 |
| Forêt de Olesa de Montserrat (11) ⚠️ | Olesa de Montserrat › Baix Llobregat | 1 |
| Park Mas Colomer ⚠️ | les Franqueses del Vallès › Vallès Oriental | 1 |
| Plaça Can Monic ⚠️ | Granollers › Vallès Oriental | 1 |
| Parc (2) ⚠️ | Sant Fost de Campsentelles › Vallès Oriental | 1 |
| Forêt de Seva (4) ⚠️ | Seva › Osona (Barcelone) | 1 |
| Forêt de Seva (5) ⚠️ | Seva › Osona (Barcelone) | 1 |
| Parc de Parets del Vallès (15) ⚠️ | Parets del Vallès › Vallès Oriental | 1 |
| Parc de la Pau (3) ⚠️ | Viladecans › Baix Llobregat | 1 |
| Parc de la Torre-Roja ⚠️ | Viladecans › Baix Llobregat | 1 |
| Parc de la Sínia ⚠️ | Viladecans › Baix Llobregat | 1 |
| Parc dels Països Catalans (2) ⚠️ | Santa Perpètua de Mogoda › Vallès Occidental | 1 |
| Bosc Soldevilla ⚠️ | Santa Perpètua de Mogoda › Vallès Occidental | 1 |
| Parc de Can Folguera ⚠️ | Santa Perpètua de Mogoda › Vallès Occidental | 1 |
| Parc de Santa Perpètua de Mogoda (9) ⚠️ | Santa Perpètua de Mogoda › Vallès Occidental | 1 |
| Plaça del Repòs ⚠️ | l'Hospitalet de Llobregat › Barcelonès | 1 |
| Parc de Montornès del Vallès ⚠️ | Montornès del Vallès › Vallès Oriental | 1 |
| Parc de Montmeló ⚠️ | Montmeló › Vallès Oriental | 1 |
| Parc de Montmeló (2) ⚠️ | Montmeló › Vallès Oriental | 1 |
| Bois de Sant Quirze del Vallès (6) ⚠️ | Sant Quirze del Vallès › Vallès Occidental | 1 |
| Plaça d'Europa (3) ⚠️ | Viladecans › Baix Llobregat | 1 |
| Parc de Can Xic ⚠️ | Viladecans › Baix Llobregat | 1 |
| Parc de Can Sucre (2) ⚠️ | Viladecans › Baix Llobregat | 1 |
| Parc de la Riera de Viladecans (8) ⚠️ | Viladecans › Baix Llobregat | 1 |
| Jardins de Màlaga ⚠️ | Barcelona › Barcelonès | 1 |
| Ágora de Juan Andrés Benítez ⚠️ | Barcelona › Barcelonès | 1 |
| Plaça de Frederica Montseny (3) ⚠️ | Terrassa › Vallès Occidental | 1 |
| Plaça de Catalunya (12) ⚠️ | Castellar del Vallès › Vallès Occidental | 1 |
| parc de Can Muntanyà ⚠️ | Caldes d'Estrac › Maresme | 1 |
| Parc de les Franqueses del Vallès (5) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 1 |
| Parc de Canet de Mar (5) ⚠️ | Canet de Mar › Maresme | 1 |
| Parc de Vilafranca del Penedès (6) ⚠️ | Vilafranca del Penedès › Alt Penedès | 1 |
| Plaça de Can Moré ⚠️ | Pineda de Mar › Maresme | 1 |
| Plaça de Joan Miró (3) ⚠️ | Santa Susanna › Maresme | 1 |
| Parc de Can Boada (3) ⚠️ | Sant Vicenç de Montalt › Maresme | 1 |
| Forêt de Vallromanes ⚠️ | Vallromanes › Vallès Oriental | 1 |
| Forêt de Vallromanes (4) ⚠️ | Vallromanes › Vallès Oriental | 1 |
| parc de Can Werboom ⚠️ | Premià de Dalt › Maresme | 1 |
| Parc de Ripollet (32) ⚠️ | Ripollet › Vallès Occidental | 1 |
| Parc de Sitges (19) ⚠️ | Sitges › Garraf | 1 |
| Forêt de Sant Antoni de Vilamajor ⚠️ | Sant Antoni de Vilamajor › Vallès Oriental | 1 |
| Bois de Gurb (19) ⚠️ | Gurb › Osona (Barcelone) | 1 |
| Bois de Gurb (20) ⚠️ | Gurb › Osona (Barcelone) | 1 |
| Bois de Gurb (23) ⚠️ | Gurb › Osona (Barcelone) | 1 |
| Bois de Gurb (26) ⚠️ | Gurb › Osona (Barcelone) | 1 |
| Bois de Gurb (27) ⚠️ | Gurb › Osona (Barcelone) | 1 |
| Bois de Gurb (28) ⚠️ | Gurb › Osona (Barcelone) | 1 |
| Jardins del Pelut ⚠️ | Orís › Osona (Barcelone) | 1 |
| Parc del Colomer ⚠️ | Santa Susanna › Maresme | 1 |
| Plaça de la Germana Campos ⚠️ | Malgrat de Mar › Maresme | 1 |
| Parc de Rosa Sensat i Vila ⚠️ | Cornellà de Llobregat › Baix Llobregat | 1 |
| Forêt de Avià (5) ⚠️ | Avià › Berguedà | 1 |
| Parc de Lliçà de Vall (8) ⚠️ | Lliçà de Vall › Vallès Oriental | 1 |
| Parc d'Europa (4) ⚠️ | Barberà del Vallès › Vallès Occidental | 1 |
| Plaça d'Europa (4) ⚠️ | Barberà del Vallès › Vallès Occidental | 1 |
| Parc de Colobrers ⚠️ | Castellar del Vallès › Vallès Occidental | 1 |
| Plaça de la Miranda ⚠️ | Castellar del Vallès › Vallès Occidental | 1 |
| Forêt de Montgat ⚠️ | Montgat › Maresme | 1 |
| Forêt de Castellnou de Bages (5) ⚠️ | Castellnou de Bages › Bages | 1 |
| Forêt de Castellnou de Bages (10) ⚠️ | Castellnou de Bages › Bages | 1 |
| Parc de el Masnou ⚠️ | el Masnou › Maresme | 1 |
| Jardins del Maremar ⚠️ | el Masnou › Maresme | 1 |
| Parc de l'Hospitalet de Llobregat (21) ⚠️ | l'Hospitalet de Llobregat › Barcelonès | 1 |
| Parc de Olesa de Montserrat (5) ⚠️ | Olesa de Montserrat › Baix Llobregat | 1 |
| Parc de Mas Reixac ⚠️ | Palafolls › Maresme | 1 |
| Parc de Viladecans (3) ⚠️ | Viladecans › Baix Llobregat | 1 |
| Passeig del Ter (4) ⚠️ | Manlleu › Osona (Barcelone) | 1 |
| Parc de l'Arboretum (2) ⚠️ | Manlleu › Osona (Barcelone) | 1 |
| Forêt de Tordera (17) ⚠️ | Tordera › Maresme | 1 |
| Parc de Collbató (4) ⚠️ | Collbató › Baix Llobregat | 1 |
| Parc de Vallmora ⚠️ | el Masnou › Maresme | 1 |
| Parc de can Quatrecases ⚠️ | Argentona › Maresme | 1 |
| Plana de l'Espinal ⚠️ | Argentona › Maresme | 1 |
| Parc de Argentona (18) ⚠️ | Argentona › Maresme | 1 |
| Plaça d'Alfons Comín ⚠️ | Sant Feliu de Llobregat › Baix Llobregat | 1 |
| Parc de Sant Salvador de Guardiola (2) ⚠️ | Sant Salvador de Guardiola › Bages | 1 |
| Parc de la Muntanyeta (2) ⚠️ | Castelldefels › Baix Llobregat | 1 |
| Parc de Mataró (24) ⚠️ | Mataró › Maresme | 1 |
| Jardí de Pilar Espuña i Domènech ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Montcada i Reixac (25) ⚠️ | Montcada i Reixac › Vallès Occidental | 1 |
| Parc de Molins de Rei (9) ⚠️ | Molins de Rei › Baix Llobregat | 1 |
| Parc (4) ⚠️ | Sant Fost de Campsentelles › Vallès Oriental | 1 |
| Parc de Neus Català i Pallejà ⚠️ | Viladecans › Baix Llobregat | 1 |
| Placeta de Josep M. Jaén ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Sallent (4) ⚠️ | Sallent › Bages | 1 |
| Parc de Sant Quirze del Vallès (14) ⚠️ | Sant Quirze del Vallès › Vallès Occidental | 1 |
| Forêt de Sallent (5) ⚠️ | Sallent › Bages | 1 |
| Parc de l'Aqüeducte ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Oristà (11) ⚠️ | Oristà › Lluçanès | 1 |
| Forêt de Oristà (15) ⚠️ | Oristà › Lluçanès | 1 |
| Parc de Santa Maria de Palautordera (4) ⚠️ | Santa Maria de Palautordera › Vallès Oriental | 1 |
| Forêt de Oristà (36) ⚠️ | Oristà › Lluçanès | 1 |
| Forêt de Oristà (37) ⚠️ | Oristà › Lluçanès | 1 |
| Forêt de Oristà (39) ⚠️ | Oristà › Lluçanès | 1 |
| Forêt de Oristà (40) ⚠️ | Oristà › Lluçanès | 1 |
| Forêt de Oristà (45) ⚠️ | Oristà › Lluçanès | 1 |
| Forêt de Oristà (53) ⚠️ | Oristà › Lluçanès | 1 |
| Forêt de Navàs (4) ⚠️ | Navàs › Bages | 1 |
| Forêt de Oristà (60) ⚠️ | Oristà › Lluçanès | 1 |
| Forêt de Oristà (61) ⚠️ | Oristà › Lluçanès | 1 |
| Forêt de Oristà (62) ⚠️ | Oristà › Lluçanès | 1 |
| Skate Park (3) ⚠️ | Castellar del Vallès › Vallès Occidental | 1 |
| Forêt de Oristà (63) ⚠️ | Oristà › Lluçanès | 1 |
| Forêt de Oristà (64) ⚠️ | Oristà › Lluçanès | 1 |
| Forêt de Oristà (67) ⚠️ | Oristà › Lluçanès | 1 |
| Forêt de Oristà (68) ⚠️ | Oristà › Lluçanès | 1 |
| Forêt de Oristà (70) ⚠️ | Oristà › Lluçanès | 1 |
| Forêt de Oristà (71) ⚠️ | Oristà › Lluçanès | 1 |
| Forêt de Oristà (72) ⚠️ | Oristà › Lluçanès | 1 |
| Gran Clariana ⚠️ | Barcelona › Barcelonès | 1 |
| Plaça de la II República ⚠️ | Montcada i Reixac › Vallès Occidental | 1 |
| parc de les Quatre Hores ⚠️ | Badalona › Barcelonès | 1 |
| Forêt de Sabadell (41) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Forêt de Sabadell (43) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Forêt de Santa Perpètua de Mogoda (18) ⚠️ | Santa Perpètua de Mogoda › Vallès Occidental | 1 |
| Bois de Sant Fost de Campsentelles (2) ⚠️ | Sant Fost de Campsentelles › Vallès Oriental | 1 |
| Bois de Sant Fost de Campsentelles (5) ⚠️ | Sant Fost de Campsentelles › Vallès Oriental | 1 |
| Bois de Sant Fost de Campsentelles (6) ⚠️ | Sant Fost de Campsentelles › Vallès Oriental | 1 |
| Bois de Santa Maria de Martorelles ⚠️ | Santa Maria de Martorelles › Vallès Oriental | 1 |
| Forêt de Vallromanes (7) ⚠️ | Vallromanes › Vallès Oriental | 1 |
| Forêt de Montornès del Vallès (5) ⚠️ | Montornès del Vallès › Vallès Oriental | 1 |
| Bois de Tiana (3) ⚠️ | Tiana › Maresme | 1 |
| Bois de Tiana (6) ⚠️ | Tiana › Maresme | 1 |
| Bois de Tiana (7) ⚠️ | Tiana › Maresme | 1 |
| La Llosa ⚠️ | Montmeló › Vallès Oriental | 1 |
| Bois de Barcelona (52) ⚠️ | Barcelona › Barcelonès | 1 |
| Bois de Barcelona (53) ⚠️ | Barcelona › Barcelonès | 1 |
| Bois de Barcelona (54) ⚠️ | Barcelona › Barcelonès | 1 |
| Bois de Terrassa (2) ⚠️ | Terrassa › Vallès Occidental | 1 |
| Parc de Sant Quirze del Vallès (15) ⚠️ | Sant Quirze del Vallès › Vallès Occidental | 1 |
| Parc de Sant Quirze del Vallès (16) ⚠️ | Sant Quirze del Vallès › Vallès Occidental | 1 |
| Bois de Terrassa (7) ⚠️ | Terrassa › Vallès Occidental | 1 |
| Bois de Terrassa (9) ⚠️ | Terrassa › Vallès Occidental | 1 |
| Forêt de Terrassa (37) ⚠️ | Terrassa › Vallès Occidental | 1 |
| Forêt de Terrassa (43) ⚠️ | Terrassa › Vallès Occidental | 1 |
| Forêt de Terrassa (47) ⚠️ | Terrassa › Vallès Occidental | 1 |
| Forêt de Sabadell (45) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Forêt de Terrassa (50) ⚠️ | Terrassa › Vallès Occidental | 1 |
| Forêt de Rubí (5) ⚠️ | Rubí › Vallès Occidental | 1 |
| Forêt de Rubí (7) ⚠️ | Rubí › Vallès Occidental | 1 |
| Forêt de Rubí (9) ⚠️ | Rubí › Vallès Occidental | 1 |
| Forêt de Castellbisbal (4) ⚠️ | Castellbisbal › Vallès Occidental | 1 |
| Bois de Castellbisbal (2) ⚠️ | Castellbisbal › Vallès Occidental | 1 |
| Forêt de Castellbisbal (5) ⚠️ | Castellbisbal › Vallès Occidental | 1 |
| Bois de Rubí (8) ⚠️ | Rubí › Vallès Occidental | 1 |
| Bois de Rubí (9) ⚠️ | Rubí › Vallès Occidental | 1 |
| Bois de Sant Cugat del Vallès (85) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Forêt de Sant Cugat del Vallès (102) ⚠️ | Rubí › Vallès Occidental | 1 |
| Forêt de Sant Cugat del Vallès (104) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Forêt de Sant Cugat del Vallès (105) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Forêt de Rubí (15) ⚠️ | Rubí › Vallès Occidental | 1 |
| Forêt de Rubí (18) ⚠️ | Rubí › Vallès Occidental | 1 |
| Forêt de Rubí (20) ⚠️ | Rubí › Vallès Occidental | 1 |
| Forêt de Rubí (21) ⚠️ | Rubí › Vallès Occidental | 1 |
| Forêt de Rubí (22) ⚠️ | Rubí › Vallès Occidental | 1 |
| Forêt de Rubí (25) ⚠️ | Rubí › Vallès Occidental | 1 |
| Forêt de Rubí (26) ⚠️ | Rubí › Vallès Occidental | 1 |
| Forêt de Rubí (29) ⚠️ | Rubí › Vallès Occidental | 1 |
| Forêt de Rubí (32) ⚠️ | Rubí › Vallès Occidental | 1 |
| Forêt de Rubí (36) ⚠️ | Rubí › Vallès Occidental | 1 |
| Forêt de Terrassa (57) ⚠️ | Terrassa › Vallès Occidental | 1 |
| Forêt de Terrassa (62) ⚠️ | Terrassa › Vallès Occidental | 1 |
| Forêt de Terrassa (64) ⚠️ | Terrassa › Vallès Occidental | 1 |
| Forêt de Sabadell (48) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Forêt de Sant Salvador de Guardiola (9) ⚠️ | Sant Salvador de Guardiola › Bages | 1 |
| Forêt de Castellbisbal (8) ⚠️ | Castellbisbal › Vallès Occidental | 1 |
| Jardins de Josep Pous i Pagès (2) ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Guardiola de Berguedà (2) ⚠️ | Guardiola de Berguedà › Berguedà | 1 |
| Plataneda ⚠️ | Sant Just Desvern › Baix Llobregat | 1 |
| Bois de les Franqueses del Vallès ⚠️ | les Franqueses del Vallès › Vallès Oriental | 1 |
| Forêt de Cerdanyola del Vallès (37) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Forêt de Montmajor (19) ⚠️ | Montmajor › Berguedà | 1 |
| Parc de Sant Feliu de Llobregat (2) ⚠️ | Sant Feliu de Llobregat › Baix Llobregat | 1 |
| Parc de Cal Ramons ⚠️ | Gironella › Berguedà | 1 |
| Forêt de Bigues i Riells del Fai (11) ⚠️ | Bigues i Riells del Fai › Vallès Oriental | 1 |
| Bois de Sentmenat (2) ⚠️ | Sentmenat › Vallès Occidental | 1 |
| Forêt de Sentmenat (3) ⚠️ | Sentmenat › Vallès Occidental | 1 |
| Parc de Sant Pol de Mar ⚠️ | Sant Pol de Mar › Maresme | 1 |
| Parc de la Clota ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Forêt de Badalona (13) ⚠️ | Badalona › Barcelonès | 1 |
| Forêt de Santa Coloma de Gramenet (7) ⚠️ | Santa Coloma de Gramenet › Barcelonès | 1 |
| Plaça de les Comunitats ⚠️ | l'Hospitalet de Llobregat › Barcelonès | 1 |
| Forêt de l'Hospitalet de Llobregat (6) ⚠️ | l'Hospitalet de Llobregat › Barcelonès | 1 |
| Parc de Cerdanyola del Vallès (26) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Forêt de Castellbisbal (9) ⚠️ | Castellbisbal › Vallès Occidental | 1 |
| Forêt de Castellví de Rosanes (4) ⚠️ | Castellví de Rosanes › Baix Llobregat | 1 |
| Forêt de Corbera de Llobregat (5) ⚠️ | Corbera de Llobregat › Baix Llobregat | 1 |
| Forêt de Corbera de Llobregat (8) ⚠️ | Corbera de Llobregat › Baix Llobregat | 1 |
| Forêt de Cervelló (3) ⚠️ | Cervelló › Baix Llobregat | 1 |
| Forêt de Sant Vicenç dels Horts (5) ⚠️ | Sant Vicenç dels Horts › Baix Llobregat | 1 |
| Forêt de Sant Boi de Llobregat (11) ⚠️ | Sant Boi de Llobregat › Baix Llobregat | 1 |
| Parc Pla del Castell ⚠️ | Terrassa › Vallès Occidental | 1 |
| Parc de Manresa (29) ⚠️ | Manresa › Bages | 1 |
| Forêt de Vacarisses (5) ⚠️ | Vacarisses › Vallès Occidental | 1 |
| Forêt de Vacarisses (6) ⚠️ | Vacarisses › Vallès Occidental | 1 |
| Forêt de Vacarisses (8) ⚠️ | Vacarisses › Vallès Occidental | 1 |
| Parc de la Granota ⚠️ | Castelldefels › Baix Llobregat | 1 |
| Parc de Castelldefels (10) ⚠️ | Castelldefels › Baix Llobregat | 1 |
| Parc de la Pineda de la Salut ⚠️ | Sant Feliu de Llobregat › Baix Llobregat | 1 |
| Forêt de Moià (6) ⚠️ | Moià › Moianès | 1 |
| Forêt de Moià (8) ⚠️ | Moià › Moianès | 1 |
| Parc de Calldetenes ⚠️ | Calldetenes › Osona (Barcelone) | 1 |
| Forêt de Sitges (7) ⚠️ | Sitges › Garraf | 1 |
| Forêt de Castelldefels (5) ⚠️ | Castelldefels › Baix Llobregat | 1 |
| Forêt de Castelldefels (6) ⚠️ | Castelldefels › Baix Llobregat | 1 |
| Forêt de Sitges (8) ⚠️ | Sitges › Garraf | 1 |
| Jardins de Matilde Ucelay ⚠️ | l'Hospitalet de Llobregat › Barcelonès | 1 |
| Parc de Rubí (18) ⚠️ | Rubí › Vallès Occidental | 1 |
| Forêt de Rubí (42) ⚠️ | Rubí › Vallès Occidental | 1 |
| Bois de Rubí (10) ⚠️ | Rubí › Vallès Occidental | 1 |
| Parc de Cerdanyola del Vallès (55) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Parc de Cerdanyola del Vallès (57) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Forêt de Sant Salvador de Guardiola (16) ⚠️ | Sant Salvador de Guardiola › Bages | 1 |
| Forêt de Artés (5) ⚠️ | Artés › Bages | 1 |
| Forêt de Calders (5) ⚠️ | Calders › Moianès | 1 |
| Plaça Joan Sangenís ⚠️ | Sant Cugat Sesgarrigues › Alt Penedès | 1 |
| Forêt de Sant Quirze del Vallès (14) ⚠️ | Sant Quirze del Vallès › Vallès Occidental | 1 |
| Forêt de Cerdanyola del Vallès (38) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Forêt de Cerdanyola del Vallès (39) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Forêt de Cerdanyola del Vallès (40) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Plaça de la Sardana (6) ⚠️ | Rubí › Vallès Occidental | 1 |
| Forêt de Sant Llorenç Savall (7) ⚠️ | Sant Llorenç Savall › Vallès Occidental | 1 |
| Forêt de Sant Llorenç Savall (12) ⚠️ | Sant Llorenç Savall › Vallès Occidental | 1 |
| Forêt de Sentmenat (5) ⚠️ | Sentmenat › Vallès Occidental | 1 |
| Forêt de Palau-solità i Plegamans (8) ⚠️ | Palau-solità i Plegamans › Vallès Occidental | 1 |
| Bois de Palau-solità i Plegamans (2) ⚠️ | Palau-solità i Plegamans › Vallès Occidental | 1 |
| Parc de Rubí (22) ⚠️ | Rubí › Vallès Occidental | 1 |
| Parc de Cerdanyola del Vallès (60) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Parc de Cerdanyola del Vallès (63) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Parc de Barcelona (125) ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de Santa Margarida i els Monjos ⚠️ | Santa Margarida i els Monjos › Alt Penedès | 1 |
| Parc de Santa Margarida i els Monjos (2) ⚠️ | Santa Margarida i els Monjos › Alt Penedès | 1 |
| Bois de Sant Llorenç Savall ⚠️ | Sant Llorenç Savall › Vallès Occidental | 1 |
| Bois de Sant Llorenç Savall (2) ⚠️ | Sant Llorenç Savall › Vallès Occidental | 1 |
| Bois de Sant Llorenç Savall (3) ⚠️ | Sant Llorenç Savall › Vallès Occidental | 1 |
| Bois de Mura (2) ⚠️ | Mura › Bages | 1 |
| Bois de Mura (5) ⚠️ | Mura › Bages | 1 |
| Bois de Sant Llorenç Savall (8) ⚠️ | Sant Llorenç Savall › Vallès Occidental | 1 |
| Bois de Sant Llorenç Savall (11) ⚠️ | Sant Llorenç Savall › Vallès Occidental | 1 |
| Bois de Sant Llorenç Savall (13) ⚠️ | Sant Llorenç Savall › Vallès Occidental | 1 |
| Bois de Terrassa (13) ⚠️ | Terrassa › Vallès Occidental | 1 |
| Bois de Mura (14) ⚠️ | Mura › Bages | 1 |
| Bois de Mura (18) ⚠️ | Mura › Bages | 1 |
| Bois de Mura (19) ⚠️ | Mura › Bages | 1 |
| Bois de Mura (22) ⚠️ | Mura › Bages | 1 |
| Bois de Mura (23) ⚠️ | Mura › Bages | 1 |
| Forêt de Matadepera (13) ⚠️ | Matadepera › Vallès Occidental | 1 |
| Forêt de Matadepera (15) ⚠️ | Matadepera › Vallès Occidental | 1 |
| Forêt de Matadepera (18) ⚠️ | Matadepera › Vallès Occidental | 1 |
| Forêt de Matadepera (20) ⚠️ | Matadepera › Vallès Occidental | 1 |
| Bois de Terrassa (15) ⚠️ | Terrassa › Vallès Occidental | 1 |
| Forêt de Òrrius ⚠️ | Òrrius › Maresme | 1 |
| Bois de l'Hospitalet de Llobregat (5) ⚠️ | l'Hospitalet de Llobregat › Barcelonès | 1 |
| Parc de Rubí (25) ⚠️ | Rubí › Vallès Occidental | 1 |
| Bois de Castellet i la Gornal (8) ⚠️ | Castellet i la Gornal › Alt Penedès | 1 |
| Bois de Santa Margarida i els Monjos (5) ⚠️ | Santa Margarida i els Monjos › Alt Penedès | 1 |
| Forêt de Santa Margarida i els Monjos (28) ⚠️ | Santa Margarida i els Monjos › Alt Penedès | 1 |
| Forêt de Santa Margarida i els Monjos (29) ⚠️ | Santa Margarida i els Monjos › Alt Penedès | 1 |
| Forêt de Santa Margarida i els Monjos (30) ⚠️ | Santa Margarida i els Monjos › Alt Penedès | 1 |
| Forêt de Sant Boi de Llobregat (12) ⚠️ | Sant Boi de Llobregat › Baix Llobregat | 1 |
| Plaça de les Mallorquines ⚠️ | Montgat › Maresme | 1 |
| Forêt de Gavà (25) ⚠️ | Gavà › Baix Llobregat | 1 |
| Parc de Santa Margarida i els Monjos (14) ⚠️ | Santa Margarida i els Monjos › Alt Penedès | 1 |
| Bois de Sant Sadurní d'Anoia (2) ⚠️ | Sant Sadurní d'Anoia › Alt Penedès | 1 |
| Plaça de la Generalitat de Catalunya ⚠️ | Montgat › Maresme | 1 |
| Forêt de Piera (20) ⚠️ | Piera › Anoia | 1 |
| Forêt de Torrelavit (20) ⚠️ | Torrelavit › Alt Penedès | 1 |
| Forêt de Sant Celoni (14) ⚠️ | Sant Celoni › Vallès Oriental | 1 |
| Bois de el Prat de Llobregat (278) ⚠️ | el Prat de Llobregat › Baix Llobregat | 1 |
| Bois de el Prat de Llobregat (279) ⚠️ | el Prat de Llobregat › Baix Llobregat | 1 |
| Forêt de Aguilar de Segarra (8) ⚠️ | Aguilar de Segarra › Bages | 1 |
| Forêt de Sant Salvador de Guardiola (19) ⚠️ | Sant Salvador de Guardiola › Bages | 1 |
| Plaça d'Ausias March ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Plaça d'Almeda la Vella ⚠️ | Cornellà de Llobregat › Baix Llobregat | 1 |
| Parc de la Planota ⚠️ | Navarcles › Bages | 1 |
| Forêt de Viver i Serrateix (9) ⚠️ | Viver i Serrateix › Berguedà | 1 |
| Forêt de Sagàs (2) ⚠️ | Sagàs › Berguedà | 1 |
| Forêt de Avià (9) ⚠️ | Avià › Berguedà | 1 |
| Forêt de Avià (10) ⚠️ | Avià › Berguedà | 1 |
| Forêt de Casserres (6) ⚠️ | Casserres › Berguedà | 1 |
| Forêt de Casserres (7) ⚠️ | Casserres › Berguedà | 1 |
| Forêt de Capolat ⚠️ | Capolat › Berguedà | 1 |
| Forêt de Montclar (7) ⚠️ | Montclar › Berguedà | 1 |
| Forêt de Santa Maria de Merlès (2) ⚠️ | Santa Maria de Merlès › Berguedà | 1 |
| Plaça de Francesc Macià (4) ⚠️ | Cornellà de Llobregat › Baix Llobregat | 1 |
| Parc de Barcelona (131) ⚠️ | Barcelona › Barcelonès | 1 |
| Plaça Primer de Maig (2) ⚠️ | Barcelona › Barcelonès | 1 |
| Bois de Sant Cugat del Vallès (89) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Bois de Sant Cugat del Vallès (91) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Bois de Sant Cugat del Vallès (93) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Bois de Sant Cugat del Vallès (100) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Forêt de Sant Cugat del Vallès (108) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Parc de Sant Cugat del Vallès (55) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Bois de Sant Cugat del Vallès (101) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Bois de Sant Cugat del Vallès (106) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Bois de Barcelona (64) ⚠️ | Barcelona › Barcelonès | 1 |
| Bois de Barcelona (67) ⚠️ | Barcelona › Barcelonès | 1 |
| Bois de Barcelona (68) ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Barcelona (38) ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Sant Cugat del Vallès (112) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Forêt de Badalona (28) ⚠️ | Badalona › Barcelonès | 1 |
| Forêt de Vilanova i la Geltrú (10) ⚠️ | Vilanova i la Geltrú › Garraf | 1 |
| Bois de Sentmenat (4) ⚠️ | Sentmenat › Vallès Occidental | 1 |
| Forêt de Sant Vicenç de Montalt (2) ⚠️ | Sant Vicenç de Montalt › Maresme | 1 |
| Forêt de Collsuspina (5) ⚠️ | Collsuspina › Moianès | 1 |
| Plaça Verda del Carme ⚠️ | Esplugues de Llobregat › Baix Llobregat | 1 |
| Parc Fatjò ⚠️ | Sant Joan Despí › Baix Llobregat | 1 |
| Parc de Mataró (27) ⚠️ | Mataró › Maresme | 1 |
| Parc mediambiental de Gualba ⚠️ | Gualba › Vallès Oriental | 1 |
| Parc de la Plana Padrosa ⚠️ | Sant Just Desvern › Baix Llobregat | 1 |
| Parc del Gall ⚠️ | Esplugues de Llobregat › Baix Llobregat | 1 |
| el Pont Reixat ⚠️ | Sant Just Desvern › Baix Llobregat | 1 |
| Bois de Vic (2) ⚠️ | Vic › Osona (Barcelone) | 1 |
| Parc de Sant Adrià de Besòs (3) ⚠️ | Sant Adrià de Besòs › Barcelonès | 1 |
| Parc de Cal Sant Just ⚠️ | Sant Llorenç d'Hortons › Alt Penedès | 1 |
| Forêt de Castellfollit del Boix (10) ⚠️ | Castellfollit del Boix › Bages | 1 |
| Forêt de Cubelles (9) ⚠️ | Cubelles › Garraf | 1 |
| Forêt de Olivella (42) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Begues (15) ⚠️ | Begues › Baix Llobregat | 1 |
| Forêt de Begues (16) ⚠️ | Begues › Baix Llobregat | 1 |
| Bois de Tavertet ⚠️ | Tavertet › Osona (Barcelone) | 1 |
| Forêt de Olivella (45) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Begues (18) ⚠️ | Begues › Baix Llobregat | 1 |
| Forêt de Begues (19) ⚠️ | Begues › Baix Llobregat | 1 |
| Forêt de Olivella (48) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Sant Pere de Ribes (75) ⚠️ | Sant Pere de Ribes › Garraf | 1 |
| Forêt de Sant Pere de Ribes (78) ⚠️ | Sant Pere de Ribes › Garraf | 1 |
| Forêt de Sant Pere de Ribes (82) ⚠️ | Sant Pere de Ribes › Garraf | 1 |
| Forêt de Sant Pere de Ribes (83) ⚠️ | Sant Pere de Ribes › Garraf | 1 |
| Forêt de Sitges (13) ⚠️ | Sitges › Garraf | 1 |
| Bois de Montmaneu (2) ⚠️ | Montmaneu › Anoia | 1 |
| Forêt de Castellet i la Gornal (62) ⚠️ | Castellet i la Gornal › Alt Penedès | 1 |
| Forêt de Castellet i la Gornal (63) ⚠️ | Castellet i la Gornal › Alt Penedès | 1 |
| Forêt de Sant Pere de Ribes (85) ⚠️ | Sant Pere de Ribes › Garraf | 1 |
| Forêt de Vilanova i la Geltrú (15) ⚠️ | Vilanova i la Geltrú › Garraf | 1 |
| Forêt de Vilanova i la Geltrú (16) ⚠️ | Vilanova i la Geltrú › Garraf | 1 |
| Jardins de Frederica Montseny ⚠️ | Barcelona › Barcelonès | 1 |
| Bois de Gurb (33) ⚠️ | Gurb › Osona (Barcelone) | 1 |
| Bois de Sant Antoni de Vilamajor ⚠️ | Sant Antoni de Vilamajor › Vallès Oriental | 1 |
| Bois de Sant Antoni de Vilamajor (2) ⚠️ | Sant Antoni de Vilamajor › Vallès Oriental | 1 |
| Bois de Bigues i Riells del Fai (4) ⚠️ | Bigues i Riells del Fai › Vallès Oriental | 1 |
| Forêt de Montornès del Vallès (6) ⚠️ | Montornès del Vallès › Vallès Oriental | 1 |
| Bois de Bigues i Riells del Fai (6) ⚠️ | Bigues i Riells del Fai › Vallès Oriental | 1 |
| Forêt de Viver i Serrateix (15) ⚠️ | Viver i Serrateix › Berguedà | 1 |
| Forêt de Viver i Serrateix (18) ⚠️ | Viver i Serrateix › Berguedà | 1 |
| Forêt de Santa Maria de Merlès (4) ⚠️ | Santa Maria de Merlès › Berguedà | 1 |
| Parc de Sitges (24) ⚠️ | Sitges › Garraf | 1 |
| Plaça d'Andalusia (3) ⚠️ | Rubí › Vallès Occidental | 1 |
| Forêt de Tiana (8) ⚠️ | Tiana › Maresme | 1 |
| Forêt de Cànoves i Samalús (3) ⚠️ | Cànoves i Samalús › Vallès Oriental | 1 |
| Forêt de Sant Bartomeu del Grau (7) ⚠️ | Sant Bartomeu del Grau › Osona (Barcelone) | 1 |
| Forêt de Sitges (16) ⚠️ | Sitges › Garraf | 1 |
| Forêt de la Garriga (13) ⚠️ | la Garriga › Vallès Oriental | 1 |
| Forêt de Cànoves i Samalús (6) ⚠️ | Cànoves i Samalús › Vallès Oriental | 1 |
| Forêt de les Franqueses del Vallès (9) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 1 |
| Forêt de les Franqueses del Vallès (10) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 1 |
| Forêt de les Franqueses del Vallès (11) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 1 |
| Forêt de les Franqueses del Vallès (12) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 1 |
| Forêt de les Franqueses del Vallès (13) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 1 |
| Forêt de les Franqueses del Vallès (15) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 1 |
| Forêt de les Franqueses del Vallès (16) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 1 |
| Forêt de les Franqueses del Vallès (18) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 1 |
| Forêt de les Franqueses del Vallès (22) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 1 |
| Forêt de les Franqueses del Vallès (24) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 1 |
| Forêt de Sant Antoni de Vilamajor (2) ⚠️ | Sant Antoni de Vilamajor › Vallès Oriental | 1 |
| Forêt de Granera (2) ⚠️ | Granera › Moianès | 1 |
| Forêt de Granera (6) ⚠️ | Granera › Moianès | 1 |
| Forêt de Granera (7) ⚠️ | Granera › Moianès | 1 |
| Forêt de el Bruc (2) ⚠️ | el Bruc › Anoia | 1 |
| Forêt de Sant Feliu de Codines (6) ⚠️ | Sant Feliu de Codines › Vallès Oriental | 1 |
| Forêt de Matadepera (29) ⚠️ | Matadepera › Vallès Occidental | 1 |
| Forêt de Muntanyola (6) ⚠️ | Muntanyola › Osona (Barcelone) | 1 |
| Forêt de Matadepera (35) ⚠️ | Matadepera › Vallès Occidental | 1 |
| Forêt de Matadepera (38) ⚠️ | Matadepera › Vallès Occidental | 1 |
| Forêt de Matadepera (43) ⚠️ | Matadepera › Vallès Occidental | 1 |
| Forêt de Matadepera (45) ⚠️ | Matadepera › Vallès Occidental | 1 |
| Forêt de Matadepera (48) ⚠️ | Matadepera › Vallès Occidental | 1 |
| Bois de Montmaneu (8) ⚠️ | Montmaneu › Anoia | 1 |
| Bois de Montmaneu (9) ⚠️ | Montmaneu › Anoia | 1 |
| Bois de Montmaneu (10) ⚠️ | Montmaneu › Anoia | 1 |
| Bois de Argençola (3) ⚠️ | Argençola › Anoia | 1 |
| Forêt de Lliçà de Vall (4) ⚠️ | Lliçà de Vall › Vallès Oriental | 1 |
| Bois de Montmaneu (15) ⚠️ | Montmaneu › Anoia | 1 |
| Forêt de Argençola (23) ⚠️ | Argençola › Anoia | 1 |
| Bois de Montmaneu (19) ⚠️ | Montmaneu › Anoia | 1 |
| Bois de Montmaneu (21) ⚠️ | Montmaneu › Anoia | 1 |
| Bois de Montmaneu (27) ⚠️ | Montmaneu › Anoia | 1 |
| Forêt de Vic (3) ⚠️ | Vic › Osona (Barcelone) | 1 |
| Forêt de Vic (7) ⚠️ | Vic › Osona (Barcelone) | 1 |
| Forêt de Muntanyola (7) ⚠️ | Muntanyola › Osona (Barcelone) | 1 |
| Forêt de Sant Martí de Centelles ⚠️ | Sant Martí de Centelles › Osona (Barcelone) | 1 |
| Forêt de Muntanyola (9) ⚠️ | Malla › Osona (Barcelone) | 1 |
| Forêt de Muntanyola (12) ⚠️ | Muntanyola › Osona (Barcelone) | 1 |
| Forêt de Tagamanent (3) ⚠️ | Tagamanent › Vallès Oriental | 1 |
| Forêt de Fogars de Montclús (7) ⚠️ | Fogars de Montclús › Vallès Oriental | 1 |
| Forêt de Sant Martí de Centelles (2) ⚠️ | Sant Martí de Centelles › Osona (Barcelone) | 1 |
| Forêt de la Garriga (29) ⚠️ | la Garriga › Vallès Oriental | 1 |
| Forêt de Sant Martí de Centelles (4) ⚠️ | Sant Martí de Centelles › Osona (Barcelone) | 1 |
| Forêt de Sant Martí de Centelles (6) ⚠️ | Sant Martí de Centelles › Osona (Barcelone) | 1 |
| Forêt de Sant Martí de Centelles (9) ⚠️ | Sant Martí de Centelles › Osona (Barcelone) | 1 |
| Forêt de Sant Martí de Centelles (13) ⚠️ | Sant Martí de Centelles › Osona (Barcelone) | 1 |
| Forêt de Sant Martí de Centelles (14) ⚠️ | Sant Martí de Centelles › Osona (Barcelone) | 1 |
| Forêt de Sant Martí de Centelles (17) ⚠️ | Sant Martí de Centelles › Osona (Barcelone) | 1 |
| Forêt de Sant Martí de Centelles (18) ⚠️ | Sant Martí de Centelles › Osona (Barcelone) | 1 |
| Forêt de Sant Martí de Centelles (19) ⚠️ | Sant Martí de Centelles › Osona (Barcelone) | 1 |
| Forêt de Sant Martí de Centelles (20) ⚠️ | Sant Martí de Centelles › Osona (Barcelone) | 1 |
| Forêt de Centelles ⚠️ | Centelles › Osona (Barcelone) | 1 |
| Forêt de l'Ametlla del Vallès (12) ⚠️ | l'Ametlla del Vallès › Vallès Oriental | 1 |
| Forêt de l'Ametlla del Vallès (14) ⚠️ | l'Ametlla del Vallès › Vallès Oriental | 1 |
| Forêt de Sant Martí de Centelles (28) ⚠️ | Sant Martí de Centelles › Osona (Barcelone) | 1 |
| Forêt de Sant Martí de Centelles (37) ⚠️ | Sant Martí de Centelles › Osona (Barcelone) | 1 |
| Forêt de Sant Martí de Centelles (41) ⚠️ | Sant Martí de Centelles › Osona (Barcelone) | 1 |
| Forêt de Oristà (82) ⚠️ | Oristà › Lluçanès | 1 |
| Forêt de Navàs (17) ⚠️ | Navàs › Bages | 1 |
| Forêt de Navàs (18) ⚠️ | Navàs › Bages | 1 |
| Forêt de Sant Mateu de Bages (7) ⚠️ | Sant Mateu de Bages › Bages | 1 |
| Forêt de Sant Mateu de Bages (8) ⚠️ | Sant Mateu de Bages › Bages | 1 |
| Bois de Montmaneu (29) ⚠️ | Montmaneu › Anoia | 1 |
| Bois de Argençola (6) ⚠️ | Argençola › Anoia | 1 |
| Bois de Argençola (7) ⚠️ | Argençola › Anoia | 1 |
| Forêt de la Garriga (30) ⚠️ | la Garriga › Vallès Oriental | 1 |
| Forêt de les Franqueses del Vallès (28) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 1 |
| Forêt de Cardedeu (5) ⚠️ | Cardedeu › Vallès Oriental | 1 |
| Forêt de Sant Pere de Vilamajor (4) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 1 |
| Forêt de les Franqueses del Vallès (31) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 1 |
| Forêt de Sant Pere de Vilamajor (8) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 1 |
| Forêt de Sant Pere de Vilamajor (10) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 1 |
| Forêt de Sant Pere de Vilamajor (24) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 1 |
| Forêt de Sant Pere de Vilamajor (26) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 1 |
| Forêt de Sant Pere de Vilamajor (28) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 1 |
| Forêt de Sant Pere de Vilamajor (30) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 1 |
| Forêt de Sant Pere de Vilamajor (43) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 1 |
| Forêt de l'Esquirol (17) ⚠️ | l'Esquirol › Osona (Barcelone) | 1 |
| Forêt de l'Esquirol (19) ⚠️ | l'Esquirol › Osona (Barcelone) | 1 |
| Parc dels Camps de la Riera ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 1 |
| Parc de Cerdanyola del Vallès (78) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Forêt de l'Esquirol (24) ⚠️ | l'Esquirol › Osona (Barcelone) | 1 |
| Forêt de l'Esquirol (29) ⚠️ | l'Esquirol › Osona (Barcelone) | 1 |
| Forêt de l'Esquirol (32) ⚠️ | l'Esquirol › Osona (Barcelone) | 1 |
| Forêt de l'Esquirol (35) ⚠️ | l'Esquirol › Osona (Barcelone) | 1 |
| Forêt de l'Esquirol (41) ⚠️ | l'Esquirol › Osona (Barcelone) | 1 |
| Pati del Safareig ⚠️ | Santa Perpètua de Mogoda › Vallès Occidental | 1 |
| Forêt de Sant Pere de Vilamajor (44) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 1 |
| Forêt de Sant Pere de Vilamajor (49) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 1 |
| Forêt de Sant Pere de Vilamajor (58) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 1 |
| Forêt de Rupit i Pruit (11) ⚠️ | Rupit i Pruit › Osona (Barcelone) | 1 |
| Forêt de l'Esquirol (67) ⚠️ | l'Esquirol › Osona (Barcelone) | 1 |
| Forêt de l'Esquirol (81) ⚠️ | l'Esquirol › Osona (Barcelone) | 1 |
| Forêt de Rupit i Pruit (12) ⚠️ | Rupit i Pruit › Osona (Barcelone) | 1 |
| Forêt de les Franqueses del Vallès (35) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 1 |
| Forêt de l'Esquirol (102) ⚠️ | l'Esquirol › Osona (Barcelone) | 1 |
| Forêt de l'Esquirol (104) ⚠️ | l'Esquirol › Osona (Barcelone) | 1 |
| Parc de Cornellà de Llobregat (32) ⚠️ | Cornellà de Llobregat › Baix Llobregat | 1 |
| Forêt de Dosrius ⚠️ | Dosrius › Maresme | 1 |
| el Bosquet (2) ⚠️ | Alella › Maresme | 1 |
| Segon bosquet ⚠️ | Alella › Maresme | 1 |
| Plaça de Dolors Renau ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Tordera (27) ⚠️ | Tordera › Maresme | 1 |
| Forêt de Tordera (28) ⚠️ | Tordera › Maresme | 1 |
| Forêt de Sant Antoni de Vilamajor (10) ⚠️ | Sant Antoni de Vilamajor › Vallès Oriental | 1 |
| Forêt de Llinars del Vallès (4) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Parc de Sabadell (76) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Forêt de Sant Antoni de Vilamajor (12) ⚠️ | Sant Antoni de Vilamajor › Vallès Oriental | 1 |
| Forêt de Sant Antoni de Vilamajor (13) ⚠️ | Sant Antoni de Vilamajor › Vallès Oriental | 1 |
| Forêt de la Garriga (31) ⚠️ | la Garriga › Vallès Oriental | 1 |
| Forêt de Sant Antoni de Vilamajor (15) ⚠️ | Sant Antoni de Vilamajor › Vallès Oriental | 1 |
| Forêt de Sant Antoni de Vilamajor (21) ⚠️ | Sant Antoni de Vilamajor › Vallès Oriental | 1 |
| Forêt de Llinars del Vallès (9) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Forêt de Llinars del Vallès (12) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Forêt de Llinars del Vallès (14) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Forêt de Llinars del Vallès (16) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Forêt de Llinars del Vallès (21) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Forêt de Llinars del Vallès (24) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Forêt de Llinars del Vallès (31) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Forêt de Llinars del Vallès (34) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Forêt de Llinars del Vallès (36) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Parc de Sant Esteve de Palautordera (4) ⚠️ | Sant Esteve de Palautordera › Vallès Oriental | 1 |
| Parc de Llinars del Vallès (3) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Forêt de Llinars del Vallès (42) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Forêt de Sant Antoni de Vilamajor (24) ⚠️ | Sant Antoni de Vilamajor › Vallès Oriental | 1 |
| Forêt de Cardedeu (17) ⚠️ | Cardedeu › Vallès Oriental | 1 |
| Forêt de les Franqueses del Vallès (42) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 1 |
| Forêt de Llinars del Vallès (49) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Bois de Montmaneu (33) ⚠️ | Montmaneu › Anoia | 1 |
| Bois de Montmaneu (36) ⚠️ | Montmaneu › Anoia | 1 |
| Bois de Montmaneu (37) ⚠️ | Montmaneu › Anoia | 1 |
| Forêt de Gaià (8) ⚠️ | Gaià › Bages | 1 |
| Forêt de Gaià (9) ⚠️ | Gaià › Bages | 1 |
| Parc de Sant Simplici ⚠️ | Santa Eulàlia de Ronçana › Vallès Oriental | 1 |
| Forêt de Fígols (3) ⚠️ | Fígols › Berguedà | 1 |
| Bois de Torrelavit (19) ⚠️ | Torrelavit › Alt Penedès | 1 |
| Bois de Torrelavit (21) ⚠️ | Torrelavit › Alt Penedès | 1 |
| Jardins de Rosa Sensat ⚠️ | l'Hospitalet de Llobregat › Barcelonès | 1 |
| Bois de Torrelavit (23) ⚠️ | Torrelavit › Alt Penedès | 1 |
| Bois de Torrelavit (24) ⚠️ | Torrelavit › Alt Penedès | 1 |
| Bois de Torrelavit (26) ⚠️ | Torrelavit › Alt Penedès | 1 |
| Forêt de Gisclareny (5) ⚠️ | Gisclareny › Berguedà | 1 |
| Forêt de Gisclareny (6) ⚠️ | Gisclareny › Berguedà | 1 |
| Forêt de Bagà (2) ⚠️ | Bagà › Berguedà | 1 |
| Bois de Barcelona (82) ⚠️ | Barcelona › Barcelonès | 1 |
| Bois de Torrelavit (28) ⚠️ | Torrelavit › Alt Penedès | 1 |
| Forêt de Puig-reig (3) ⚠️ | Puig-reig › Berguedà | 1 |
| Forêt de Torrelles de Llobregat (51) ⚠️ | Torrelles de Llobregat › Baix Llobregat | 1 |
| Parc de Can Font ⚠️ | Santa Eulàlia de Ronçana › Vallès Oriental | 1 |
| Parc del Llac ⚠️ | el Masnou › Maresme | 1 |
| Bois de Sabadell (26) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Bois de Sabadell (29) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Forêt de Sabadell (60) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Plaça de Gernika (2) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Parc de les Tretze Roses ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Tordera (30) ⚠️ | Tordera › Maresme | 1 |
| Forêt de Tordera (33) ⚠️ | Tordera › Maresme | 1 |
| Forêt de Malgrat de Mar (3) ⚠️ | Malgrat de Mar › Maresme | 1 |
| Forêt de la Roca del Vallès (9) ⚠️ | la Roca del Vallès › Vallès Oriental | 1 |
| Forêt de Torrelles de Llobregat (75) ⚠️ | Torrelles de Llobregat › Baix Llobregat | 1 |
| Forêt de Torrelles de Llobregat (79) ⚠️ | Torrelles de Llobregat › Baix Llobregat | 1 |
| Forêt de Torrelles de Llobregat (80) ⚠️ | Torrelles de Llobregat › Baix Llobregat | 1 |
| Forêt de Torrelles de Llobregat (89) ⚠️ | Torrelles de Llobregat › Baix Llobregat | 1 |
| Bois de Torrelles de Llobregat (8) ⚠️ | Torrelles de Llobregat › Baix Llobregat | 1 |
| Bois de Torrelles de Llobregat (18) ⚠️ | Torrelles de Llobregat › Baix Llobregat | 1 |
| Forêt de Torrelles de Llobregat (114) ⚠️ | Torrelles de Llobregat › Baix Llobregat | 1 |
| Bois de Torrelles de Llobregat (62) ⚠️ | Torrelles de Llobregat › Baix Llobregat | 1 |
| Forêt de Montornès del Vallès (7) ⚠️ | Montornès del Vallès › Vallès Oriental | 1 |
| Forêt de Vilanova del Vallès (3) ⚠️ | Vilanova del Vallès › Vallès Oriental | 1 |
| Forêt de Torrelles de Llobregat (135) ⚠️ | Torrelles de Llobregat › Baix Llobregat | 1 |
| Forêt de Vallcebre (4) ⚠️ | Vallcebre › Berguedà | 1 |
| Forêt de Vallcebre (5) ⚠️ | Vallcebre › Berguedà | 1 |
| Parc del Prat de Cubelles (2) ⚠️ | Cubelles › Garraf | 1 |
| Bois de Barcelona (85) ⚠️ | Barcelona › Barcelonès | 1 |
| Bois de Granollers (2) ⚠️ | Granollers › Vallès Oriental | 1 |
| Bois de Montmeló (4) ⚠️ | Montmeló › Vallès Oriental | 1 |
| Plaça de la Lluita per les Llibertats ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Santa Coloma de Cervelló (2) ⚠️ | Santa Coloma de Cervelló › Baix Llobregat | 1 |
| Garrofers del PP-10 (Ceratonia siliqua L.) ⚠️ | el Masnou › Maresme | 1 |
| Bois de Cabrils (10) ⚠️ | Cabrils › Maresme | 1 |
| Plaça de Salvador Espriu (2) ⚠️ | Tiana › Maresme | 1 |
| Alzinaret de la Berna ⚠️ | Torrelles de Foix › Alt Penedès | 1 |
| Bosc de Cal Parraco ⚠️ | Torrelles de Foix › Alt Penedès | 1 |
| Bois de Torrelles de Foix (2) ⚠️ | Torrelles de Foix › Alt Penedès | 1 |
| Forêt de Moià (14) ⚠️ | Moià › Moianès | 1 |
| Forêt de Castellar de n'Hug ⚠️ | Castellar de n'Hug › Berguedà | 1 |
| Forêt de el Masnou ⚠️ | el Masnou › Maresme | 1 |
| Firal dels Reis ⚠️ | Montclar › Berguedà | 1 |
| Plaça de Luisa Alba ⚠️ | Barcelona › Barcelonès | 1 |
| Plaça de les Treballadores i Treballadors de Macosa ⚠️ | Barcelona › Barcelonès | 1 |
| Parc (10) ⚠️ | Igualada › Anoia | 1 |
| Forêt de Igualada ⚠️ | Igualada › Anoia | 1 |
| Plaça de Montserrat (3) ⚠️ | Igualada › Anoia | 1 |
| Parc del Mil·lenari (4) ⚠️ | Igualada › Anoia | 1 |
| Parc (14) ⚠️ | Igualada › Anoia | 1 |
| Parc de Santa Margarida de Montbui (3) ⚠️ | Santa Margarida de Montbui › Anoia | 1 |
| Parc de Sant Hilari (2) ⚠️ | Vilanova del Camí › Anoia | 1 |
| Parc (21) ⚠️ | Igualada › Anoia | 1 |
| Forêt de Santa Margarida de Montbui (9) ⚠️ | Santa Margarida de Montbui › Anoia | 1 |
| Bosc de Can Mercader ⚠️ | Òdena › Anoia | 1 |
| Forêt de Òdena (23) ⚠️ | Òdena › Anoia | 1 |
| Forêt de Òdena (24) ⚠️ | Òdena › Anoia | 1 |
| Plaça de Lluís Gallart ⚠️ | Calella › Maresme | 1 |
| Parc dels Estricadors ⚠️ | Olesa de Montserrat › Baix Llobregat | 1 |
| Parc del Doctor Ferràndiz ⚠️ | Tiana › Maresme | 1 |
| Forêt de Barcelona (45) ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Begues (20) ⚠️ | Begues › Baix Llobregat | 1 |
| Bois de el Pla del Penedès (3) ⚠️ | el Pla del Penedès › Alt Penedès | 1 |
| Parc de Can Batlló ⚠️ | Barcelona › Barcelonès | 1 |
| Bois de Argençola (17) ⚠️ | Argençola › Anoia | 1 |
| Bois de Argençola (18) ⚠️ | Argençola › Anoia | 1 |
| Bois de Argençola (20) ⚠️ | Argençola › Anoia | 1 |
| Bois de Argençola (21) ⚠️ | Argençola › Anoia | 1 |
| Bois de Veciana ⚠️ | Veciana › Anoia | 1 |
| Forêt de Montmajor (25) ⚠️ | Montmajor › Berguedà | 1 |
| Forêt de el Papiol (2) ⚠️ | el Papiol › Baix Llobregat | 1 |
| Parc (24) ⚠️ | Martorell › Baix Llobregat | 1 |
| Forêt de la Pobla de Claramunt ⚠️ | la Pobla de Claramunt › Anoia | 1 |
| Forêt de la Pobla de Claramunt (2) ⚠️ | la Pobla de Claramunt › Anoia | 1 |
| Forêt de la Pobla de Claramunt (3) ⚠️ | la Pobla de Claramunt › Anoia | 1 |
| Parc de Sabadell (87) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Parc Central (7) ⚠️ | Igualada › Anoia | 1 |
| Forêt de Òdena (28) ⚠️ | Òdena › Anoia | 1 |
| Forêt de Òdena (29) ⚠️ | Òdena › Anoia | 1 |
| Forêt de Vilanova de Sau (26) ⚠️ | Vilanova de Sau › Osona (Barcelone) | 1 |
| Forêt de Tavertet (12) ⚠️ | Tavertet › Osona (Barcelone) | 1 |
| Forêt de Tavertet (17) ⚠️ | Tavertet › Osona (Barcelone) | 1 |
| Forêt de Tavertet (18) ⚠️ | Tavertet › Osona (Barcelone) | 1 |
| Forêt de Tavertet (19) ⚠️ | Tavertet › Osona (Barcelone) | 1 |
| Forêt de Tavertet (27) ⚠️ | Tavertet › Osona (Barcelone) | 1 |
| Bois de Veciana (6) ⚠️ | Veciana › Anoia | 1 |
| Bois de Òdena (2) ⚠️ | Òdena › Anoia | 1 |
| Bois de Òdena (3) ⚠️ | Òdena › Anoia | 1 |
| Forêt de Cerdanyola del Vallès (50) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Parc de la Primavera ⚠️ | Barcelona › Barcelonès | 1 |
| Parc (25) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Parc de Cornellà de Llobregat (40) ⚠️ | Cornellà de Llobregat › Baix Llobregat | 1 |
| Parc de Santa Susanna (8) ⚠️ | Santa Susanna › Maresme | 1 |
| Forêt de Arenys de Munt (3) ⚠️ | Arenys de Munt › Maresme | 1 |
| Forêt de Tordera (37) ⚠️ | Tordera › Maresme | 1 |
| Forêt de Tordera (42) ⚠️ | Tordera › Maresme | 1 |
| Forêt de Tordera (44) ⚠️ | Tordera › Maresme | 1 |
| Forêt de Tordera (45) ⚠️ | Fogars de la Selva › la Selva (Barcelone) | 1 |
| Forêt de Sant Celoni (20) ⚠️ | Sant Celoni › Vallès Oriental | 1 |
| Parc de Cubelles (19) ⚠️ | Cubelles › Garraf | 1 |
| Forêt de Castellnou de Bages (24) ⚠️ | Castellnou de Bages › Bages | 1 |
| Forêt de Castellnou de Bages (27) ⚠️ | Castellnou de Bages › Bages | 1 |
| Forêt de Súria (2) ⚠️ | Súria › Bages | 1 |
| Forêt de Santpedor (7) ⚠️ | Santpedor › Bages | 1 |
| Forêt de Fonollosa (63) ⚠️ | Fonollosa › Bages | 1 |
| Forêt de Fonollosa (72) ⚠️ | Fonollosa › Bages | 1 |
| Bois de Lliçà d'Amunt (28) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 1 |
| Forêt de Tiana (9) ⚠️ | Tiana › Maresme | 1 |
| Forêt de Tiana (11) ⚠️ | Tiana › Maresme | 1 |
| Parc de Puig-reig (6) ⚠️ | Puig-reig › Berguedà | 1 |
| Parc de la Sardana (2) ⚠️ | Vilafranca del Penedès › Alt Penedès | 1 |
| Bois de Palau-solità i Plegamans (12) ⚠️ | Palau-solità i Plegamans › Vallès Occidental | 1 |
| Forêt de Vallcebre (6) ⚠️ | Vallcebre › Berguedà | 1 |
| Forêt de Vallcebre (8) ⚠️ | Vallcebre › Berguedà | 1 |
| Plaça 11 deSetembre ⚠️ | Calldetenes › Osona (Barcelone) | 1 |
| Parc de Cercs (3) ⚠️ | Cercs › Berguedà | 1 |
| Parc del Tren de la Potassa ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de Barcelona (158) ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de Oristà ⚠️ | Oristà › Lluçanès | 1 |
| Parc de Olost (2) ⚠️ | Olost › Lluçanès | 1 |
| Forêt de Matadepera (61) ⚠️ | Matadepera › Vallès Occidental | 1 |
| Forêt de Matadepera (64) ⚠️ | Matadepera › Vallès Occidental | 1 |
| Forêt de Matadepera (88) ⚠️ | Matadepera › Vallès Occidental | 1 |
| Forêt de Matadepera (101) ⚠️ | Matadepera › Vallès Occidental | 1 |
| Forêt de Matadepera (109) ⚠️ | Matadepera › Vallès Occidental | 1 |
| Forêt de Matadepera (130) ⚠️ | Matadepera › Vallès Occidental | 1 |
| Forêt de Matadepera (143) ⚠️ | Matadepera › Vallès Occidental | 1 |
| Forêt de Matadepera (144) ⚠️ | Matadepera › Vallès Occidental | 1 |
| Forêt de Matadepera (145) ⚠️ | Matadepera › Vallès Occidental | 1 |
| Forêt de Matadepera (149) ⚠️ | Matadepera › Vallès Occidental | 1 |
| Forêt de Matadepera (158) ⚠️ | Matadepera › Vallès Occidental | 1 |
| Forêt de Matadepera (162) ⚠️ | Matadepera › Vallès Occidental | 1 |
| Forêt de Matadepera (166) ⚠️ | Matadepera › Vallès Occidental | 1 |
| Forêt de Matadepera (176) ⚠️ | Matadepera › Vallès Occidental | 1 |
| Forêt de Matadepera (195) ⚠️ | Matadepera › Vallès Occidental | 1 |
| Forêt de Matadepera (196) ⚠️ | Matadepera › Vallès Occidental | 1 |
| Forêt de Santa Coloma de Cervelló (4) ⚠️ | Santa Coloma de Cervelló › Baix Llobregat | 1 |
| Jardins de Pepita Pardell Terrade ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de Can Coll ⚠️ | Torrelles de Llobregat › Baix Llobregat | 1 |
| Forêt de Torrelles de Llobregat (159) ⚠️ | Torrelles de Llobregat › Baix Llobregat | 1 |
| Forêt de Torrelles de Llobregat (166) ⚠️ | Torrelles de Llobregat › Baix Llobregat | 1 |
| Forêt de Cabrera de Mar ⚠️ | Cabrera de Mar › Maresme | 1 |
| Forêt de Gurb (7) ⚠️ | Gurb › Osona (Barcelone) | 1 |
| Parc de Vic (20) ⚠️ | Vic › Osona (Barcelone) | 1 |
| Forêt de Gurb (15) ⚠️ | Gurb › Osona (Barcelone) | 1 |
| Parc de Granollers (22) ⚠️ | Granollers › Vallès Oriental | 1 |
| Forêt de Caldes de Montbui (7) ⚠️ | Caldes de Montbui › Vallès Oriental | 1 |
| Forêt de Sant Boi de Llobregat (24) ⚠️ | Sant Boi de Llobregat › Baix Llobregat | 1 |
| Forêt de Sant Boi de Llobregat (25) ⚠️ | Sant Boi de Llobregat › Baix Llobregat | 1 |
| Forêt de Sant Boi de Llobregat (27) ⚠️ | Sant Boi de Llobregat › Baix Llobregat | 1 |
| Parc de Barcelona (173) ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de Sant Fruitós de Bages (17) ⚠️ | Sant Fruitós de Bages › Bages | 1 |
| Forêt de Sant Fruitós de Bages (6) ⚠️ | Sant Fruitós de Bages › Bages | 1 |
| Bois de Argentona (50) ⚠️ | Argentona › Maresme | 1 |
| Bois de Jorba (10) ⚠️ | Jorba › Anoia | 1 |
| Bois de Copons (5) ⚠️ | Copons › Anoia | 1 |
| Bois de Argençola (26) ⚠️ | Argençola › Anoia | 1 |
| El Pati de l'Esbarjo ⚠️ | Castellbisbal › Vallès Occidental | 1 |
| Parc de el Prat de Llobregat (17) ⚠️ | el Prat de Llobregat › Baix Llobregat | 1 |
| Forêt de Manresa (13) ⚠️ | Manresa › Bages | 1 |
| Parc de Sant Fruitós de Bages (21) ⚠️ | Sant Fruitós de Bages › Bages | 1 |
| Plaça de l'Assemblea de Catalunya (2) ⚠️ | Navarcles › Bages | 1 |
| Forêt de Monistrol de Montserrat (5) ⚠️ | Monistrol de Montserrat › Bages | 1 |
| Parc Marta Mata (3) ⚠️ | Castelldefels › Baix Llobregat | 1 |
| Parc de les Palmeres (2) ⚠️ | el Prat de Llobregat › Baix Llobregat | 1 |
| Parc de Barcelona (178) ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Subirats (92) ⚠️ | Subirats › Alt Penedès | 1 |
| Parc de el Prat de Llobregat (35) ⚠️ | el Prat de Llobregat › Baix Llobregat | 1 |
| Forêt de la Pobla de Lillet (3) ⚠️ | la Pobla de Lillet › Berguedà | 1 |
| Bois de Barcelona (92) ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de Cornellà de Llobregat (42) ⚠️ | Cornellà de Llobregat › Baix Llobregat | 1 |
| Parc de Jansana ⚠️ | l'Hospitalet de Llobregat › Barcelonès | 1 |
| La Selva ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Aiguafreda (5) ⚠️ | Aiguafreda › Osona (Barcelone) | 1 |
| Forêt de Figaró-Montmany (2) ⚠️ | Figaró-Montmany › Vallès Oriental | 1 |
| Parc de Can Sauleda ⚠️ | Sant Antoni de Vilamajor › Vallès Oriental | 1 |
| Forêt de Capolat (5) ⚠️ | Capolat › Berguedà | 1 |
| Parc de Mar ⚠️ | Mataró › Maresme | 1 |
| Parc de Pallejà (13) ⚠️ | Pallejà › Baix Llobregat | 1 |
| Parc de Barcelona (180) ⚠️ | Barcelona › Barcelonès | 1 |
| Parc de Can Vidalet ⚠️ | Esplugues de Llobregat › Baix Llobregat | 1 |
| Parc del Xipreret ⚠️ | Igualada › Anoia | 1 |
| Forêt de Montmajor (28) ⚠️ | Montmajor › Berguedà | 1 |
| Parc de Sabadell (92) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Forêt de Sant Mateu de Bages (31) ⚠️ | Sant Mateu de Bages › Bages | 1 |
| Forêt de Callús (11) ⚠️ | Callús › Bages | 1 |
| Passeig de Lluís Companys ⚠️ | Canovelles › Vallès Oriental | 1 |
| Forêt de la Torre de Claramunt (2) ⚠️ | la Torre de Claramunt › Anoia | 1 |
| Forêt de la Torre de Claramunt (3) ⚠️ | la Torre de Claramunt › Anoia | 1 |
| Forêt de Rajadell (18) ⚠️ | Rajadell › Bages | 1 |
| Forêt de Manresa (18) ⚠️ | Manresa › Bages | 1 |
| Forêt de Rajadell (21) ⚠️ | Rajadell › Bages | 1 |
| Forêt de Manresa (20) ⚠️ | Manresa › Bages | 1 |
| Forêt de Sant Joan de Vilatorrada (24) ⚠️ | Sant Joan de Vilatorrada › Bages | 1 |
| Forêt de Sallent (29) ⚠️ | Sallent › Bages | 1 |
| Forêt de Sallent (30) ⚠️ | Sallent › Bages | 1 |
| Forêt de Sallent (32) ⚠️ | Sallent › Bages | 1 |
| Forêt de Sallent (34) ⚠️ | Sallent › Bages | 1 |
| Forêt de Sallent (39) ⚠️ | Sallent › Bages | 1 |
| Forêt de Sallent (48) ⚠️ | Sallent › Bages | 1 |
| Forêt de Balsareny (25) ⚠️ | Balsareny › Bages | 1 |
| Forêt de Balsareny (27) ⚠️ | Balsareny › Bages | 1 |
| Forêt de Balsareny (46) ⚠️ | Balsareny › Bages | 1 |
| Forêt de Sant Fruitós de Bages (15) ⚠️ | Sant Fruitós de Bages › Bages | 1 |
| Bosc de les Costes ⚠️ | Sant Fruitós de Bages › Bages | 1 |
| Forêt de Sant Fruitós de Bages (24) ⚠️ | Sant Fruitós de Bages › Bages | 1 |
| Forêt de Sant Fruitós de Bages (25) ⚠️ | Manresa › Bages | 1 |
| Bosc de les Marcetes ⚠️ | Manresa › Bages | 1 |
| Forêt de Calders (16) ⚠️ | Calders › Moianès | 1 |
| Forêt de Calders (21) ⚠️ | Calders › Moianès | 1 |
| Forêt de Navarcles (5) ⚠️ | Navarcles › Bages | 1 |
| Forêt de Navarcles (6) ⚠️ | Navarcles › Bages | 1 |
| Forêt de Manresa (24) ⚠️ | Manresa › Bages | 1 |
| Forêt de Manresa (25) ⚠️ | Manresa › Bages | 1 |
| Forêt de Manresa (26) ⚠️ | Manresa › Bages | 1 |
| Forêt de Vallcebre (11) ⚠️ | Vallcebre › Berguedà | 1 |
| Forêt de Cànoves i Samalús (32) ⚠️ | Cànoves i Samalús › Vallès Oriental | 1 |
| Forêt de Manresa (36) ⚠️ | Manresa › Bages | 1 |
| Forêt de Manresa (42) ⚠️ | Manresa › Bages | 1 |
| Forêt de Manresa (47) ⚠️ | Manresa › Bages | 1 |
| Forêt de Manresa (54) ⚠️ | Manresa › Bages | 1 |
| Forêt de Manresa (56) ⚠️ | Manresa › Bages | 1 |
| Forêt de Manresa (58) ⚠️ | Manresa › Bages | 1 |
| Forêt de Manresa (62) ⚠️ | Manresa › Bages | 1 |
| Forêt de Manresa (66) ⚠️ | Manresa › Bages | 1 |
| Forêt de Manresa (69) ⚠️ | Manresa › Bages | 1 |
| Forêt de Manresa (70) ⚠️ | Manresa › Bages | 1 |
| Forêt de Barcelona (51) ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Rajadell (25) ⚠️ | Rajadell › Bages | 1 |
| Forêt de Rajadell (26) ⚠️ | Rajadell › Bages | 1 |
| Forêt de Rajadell (34) ⚠️ | Rajadell › Bages | 1 |
| Forêt de Manresa (73) ⚠️ | Manresa › Bages | 1 |
| Forêt de Sant Joan de Vilatorrada (32) ⚠️ | Sant Joan de Vilatorrada › Bages | 1 |
| Forêt de Castellterçol (19) ⚠️ | Castellterçol › Moianès | 1 |
| Forêt de Castellterçol (20) ⚠️ | Castellterçol › Moianès | 1 |
| Forêt de Castellterçol (22) ⚠️ | Castellterçol › Moianès | 1 |
| Forêt de Castellterçol (23) ⚠️ | Castellterçol › Moianès | 1 |
| Forêt de Castellterçol (26) ⚠️ | Castellterçol › Moianès | 1 |
| Forêt de Castellterçol (27) ⚠️ | Castellterçol › Moianès | 1 |
| Forêt de Castellterçol (28) ⚠️ | Castellterçol › Moianès | 1 |
| Forêt de Castellterçol (32) ⚠️ | Castellterçol › Moianès | 1 |
| Forêt de Castellterçol (36) ⚠️ | Castellterçol › Moianès | 1 |
| Bois de Castellterçol (11) ⚠️ | Castellterçol › Moianès | 1 |
| Forêt de Gironella (2) ⚠️ | Gironella › Berguedà | 1 |
| Forêt de Gironella (3) ⚠️ | Gironella › Berguedà | 1 |
| Forêt de Viladecavalls (4) ⚠️ | Viladecavalls › Vallès Occidental | 1 |
| Forêt de Sant Joan de Vilatorrada (36) ⚠️ | Sant Joan de Vilatorrada › Bages | 1 |
| Forêt de Sant Joan de Vilatorrada (37) ⚠️ | Sant Joan de Vilatorrada › Bages | 1 |
| Forêt de Sant Joan de Vilatorrada (47) ⚠️ | Sant Joan de Vilatorrada › Bages | 1 |
| Forêt de Callús (12) ⚠️ | Callús › Bages | 1 |
| Forêt de Manresa (79) ⚠️ | Manresa › Bages | 1 |
| Forêt de Sant Joan de Vilatorrada (52) ⚠️ | Sant Joan de Vilatorrada › Bages | 1 |
| Forêt de Sant Joan de Vilatorrada (53) ⚠️ | Sant Joan de Vilatorrada › Bages | 1 |
| Forêt de Manresa (81) ⚠️ | Manresa › Bages | 1 |
| Forêt de Sant Joan de Vilatorrada (57) ⚠️ | Sant Joan de Vilatorrada › Bages | 1 |
| Forêt de Sant Joan de Vilatorrada (58) ⚠️ | Sant Joan de Vilatorrada › Bages | 1 |
| Forêt de Manresa (86) ⚠️ | Manresa › Bages | 1 |
| Forêt de l'Espunyola (10) ⚠️ | l'Espunyola › Berguedà | 1 |
| Forêt de Cardona (38) ⚠️ | Cardona › Bages | 1 |
| Forêt de Cardona (43) ⚠️ | Cardona › Bages | 1 |
| Forêt de Cardona (49) ⚠️ | Cardona › Bages | 1 |
| Forêt de Fonollosa (100) ⚠️ | Fonollosa › Bages | 1 |
| Forêt de Fonollosa (108) ⚠️ | Fonollosa › Bages | 1 |
| Forêt de Rajadell (38) ⚠️ | Rajadell › Bages | 1 |
| Forêt de Fonollosa (120) ⚠️ | Fonollosa › Bages | 1 |
| Forêt de Fonollosa (121) ⚠️ | Fonollosa › Bages | 1 |
| Forêt de Fonollosa (126) ⚠️ | Fonollosa › Bages | 1 |
| Forêt de Fonollosa (130) ⚠️ | Fonollosa › Bages | 1 |
| Jardins de les sufragistes catalanes ⚠️ | Barcelona › Barcelonès | 1 |
| Plaça de Puigcerdà ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Cerdanyola del Vallès (57) ⚠️ | Cerdanyola del Vallès › Vallès Occidental | 1 |
| Forêt de Castellfollit de Riubregós (7) ⚠️ | Castellfollit de Riubregós › Anoia | 1 |
| Bois de Barcelona (100) ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de els Hostalets de Pierola (13) ⚠️ | els Hostalets de Pierola › Anoia | 1 |
| Forêt de l'Esquirol (110) ⚠️ | l'Esquirol › Osona (Barcelone) | 1 |
| Forêt de Palau-solità i Plegamans (11) ⚠️ | Palau-solità i Plegamans › Vallès Occidental | 1 |
| Plaça de la Maternitat d'Elna ⚠️ | Palau-solità i Plegamans › Vallès Occidental | 1 |
| Parc del Pla de l'Alzina ⚠️ | Palau-solità i Plegamans › Vallès Occidental | 1 |
| Forêt de Palau-solità i Plegamans (12) ⚠️ | Palau-solità i Plegamans › Vallès Occidental | 1 |
| Forêt de Sant Vicenç de Torelló ⚠️ | Sant Vicenç de Torelló › Osona (Barcelone) | 1 |
| Forêt de Sant Vicenç de Torelló (2) ⚠️ | Sant Vicenç de Torelló › Osona (Barcelone) | 1 |
| Forêt de Manresa (90) ⚠️ | Manresa › Bages | 1 |
| Forêt de Manresa (91) ⚠️ | Manresa › Bages | 1 |
| Forêt de Manresa (92) ⚠️ | Manresa › Bages | 1 |
| Forêt de Manresa (93) ⚠️ | Manresa › Bages | 1 |
| Forêt de Manresa (95) ⚠️ | Manresa › Bages | 1 |
| Jardins d'Elisava ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Castellterçol (39) ⚠️ | Castellterçol › Moianès | 1 |
| Forêt de Castellterçol (42) ⚠️ | Castellterçol › Moianès | 1 |
| Forêt de Castellterçol (45) ⚠️ | Castellterçol › Moianès | 1 |
| Bois de Castellterçol (13) ⚠️ | Castellterçol › Moianès | 1 |
| Forêt de Castellterçol (61) ⚠️ | Castellterçol › Moianès | 1 |
| Forêt de Castellterçol (67) ⚠️ | Castellterçol › Moianès | 1 |
| Forêt de Castellterçol (76) ⚠️ | Castellterçol › Moianès | 1 |
| Forêt de Berga (2) ⚠️ | Berga › Berguedà | 1 |
| Forêt de Berga (7) ⚠️ | Berga › Berguedà | 1 |
| Forêt de Berga (11) ⚠️ | Berga › Berguedà | 1 |
| Forêt de Berga (13) ⚠️ | Berga › Berguedà | 1 |
| Forêt de Berga (15) ⚠️ | Berga › Berguedà | 1 |
| Forêt de Berga (21) ⚠️ | Berga › Berguedà | 1 |
| Forêt de Berga (23) ⚠️ | Berga › Berguedà | 1 |
| Bois de Barcelona (101) ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Berga (33) ⚠️ | Berga › Berguedà | 1 |
| Forêt de Berga (37) ⚠️ | Berga › Berguedà | 1 |
| Forêt de Berga (45) ⚠️ | Berga › Berguedà | 1 |
| Forêt de Berga (46) ⚠️ | Berga › Berguedà | 1 |
| Forêt de Berga (51) ⚠️ | Berga › Berguedà | 1 |
| Forêt de Berga (54) ⚠️ | Berga › Berguedà | 1 |
| Forêt de Berga (55) ⚠️ | Berga › Berguedà | 1 |
| Forêt de Berga (56) ⚠️ | Berga › Berguedà | 1 |
| Forêt de Terrassa (70) ⚠️ | Terrassa › Vallès Occidental | 1 |
| Forêt de Abrera (9) ⚠️ | Abrera › Baix Llobregat | 1 |
| Forêt de Montgat (2) ⚠️ | Montgat › Maresme | 1 |
| Forêt de el Masnou (2) ⚠️ | el Masnou › Maresme | 1 |
| Forêt de l'Espunyola (11) ⚠️ | l'Espunyola › Berguedà | 1 |
| Forêt de l'Espunyola (12) ⚠️ | l'Espunyola › Berguedà | 1 |
| Forêt de Montmajor (32) ⚠️ | Montmajor › Berguedà | 1 |
| Forêt de Montmajor (36) ⚠️ | Montmajor › Berguedà | 1 |
| Forêt de Montmajor (41) ⚠️ | Montmajor › Berguedà | 1 |
| Forêt de l'Espunyola (27) ⚠️ | l'Espunyola › Berguedà | 1 |
| Forêt de Montclar (11) ⚠️ | l'Espunyola › Berguedà | 1 |
| Forêt de Montclar (13) ⚠️ | Montclar › Berguedà | 1 |
| Forêt de Montclar (16) ⚠️ | Montclar › Berguedà | 1 |
| Forêt de l'Espunyola (29) ⚠️ | l'Espunyola › Berguedà | 1 |
| Forêt de Montmajor (48) ⚠️ | Montmajor › Berguedà | 1 |
| Forêt de Montmajor (49) ⚠️ | Montmajor › Berguedà | 1 |
| Forêt de Montmajor (51) ⚠️ | Montmajor › Berguedà | 1 |
| Parc del Cementiri (3) ⚠️ | Manlleu › Osona (Barcelone) | 1 |
| Forêt de Manresa (101) ⚠️ | Manresa › Bages | 1 |
| Forêt de Manresa (102) ⚠️ | Manresa › Bages | 1 |
| Forêt de Manresa (105) ⚠️ | Manresa › Bages | 1 |
| Forêt de Manresa (106) ⚠️ | Manresa › Bages | 1 |
| Forêt de Sant Salvador de Guardiola (23) ⚠️ | Sant Salvador de Guardiola › Bages | 1 |
| Forêt de Manresa (109) ⚠️ | Sant Salvador de Guardiola › Bages | 1 |
| Forêt de Manresa (110) ⚠️ | Manresa › Bages | 1 |
| Forêt de Manresa (116) ⚠️ | Manresa › Bages | 1 |
| Forêt de Manresa (117) ⚠️ | Manresa › Bages | 1 |
| Forêt de Olèrdola (58) ⚠️ | Olèrdola › Alt Penedès | 1 |
| Forêt de Vilafranca del Penedès (5) ⚠️ | Vilafranca del Penedès › Alt Penedès | 1 |
| Forêt de Vilafranca del Penedès (6) ⚠️ | Vilafranca del Penedès › Alt Penedès | 1 |
| Parc de la Tria ⚠️ | Vilafranca del Penedès › Alt Penedès | 1 |
| Forêt de Esparreguera (12) ⚠️ | Esparreguera › Baix Llobregat | 1 |
| Parc del Centre del Poblenou ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Balsareny (50) ⚠️ | Balsareny › Bages | 1 |
| Forêt de Balsareny (56) ⚠️ | Balsareny › Bages | 1 |
| Forêt de Avinyó (29) ⚠️ | Avinyó › Bages | 1 |
| Forêt de Avinyó (33) ⚠️ | Avinyó › Bages | 1 |
| Forêt de Avinyó (34) ⚠️ | Avinyó › Bages | 1 |
| Forêt de Avinyó (35) ⚠️ | Avinyó › Bages | 1 |
| Forêt de Avinyó (38) ⚠️ | Avinyó › Bages | 1 |
| Forêt de Avinyó (42) ⚠️ | Avinyó › Bages | 1 |
| Forêt de Avinyó (50) ⚠️ | Avinyó › Bages | 1 |
| Forêt de Sallent (59) ⚠️ | Sallent › Bages | 1 |
| Forêt de Avinyó (54) ⚠️ | Avinyó › Bages | 1 |
| Forêt de Avinyó (59) ⚠️ | Avinyó › Bages | 1 |
| Forêt de Sallent (65) ⚠️ | Sallent › Bages | 1 |
| Forêt de Sallent (67) ⚠️ | Sallent › Bages | 1 |
| Forêt de Sallent (72) ⚠️ | Sallent › Bages | 1 |
| Forêt de Sallent (75) ⚠️ | Sallent › Bages | 1 |
| Forêt de Balsareny (67) ⚠️ | Balsareny › Bages | 1 |
| Forêt de Capolat (14) ⚠️ | Capolat › Berguedà | 1 |
| Jardins d'Ignacio Urenda ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Canyelles (4) ⚠️ | Olèrdola › Alt Penedès | 1 |
| Forêt de Oristà (97) ⚠️ | Oristà › Lluçanès | 1 |
| Forêt de Esparreguera (13) ⚠️ | Esparreguera › Baix Llobregat | 1 |
| Forêt de Puig-reig (27) ⚠️ | Puig-reig › Berguedà | 1 |
| Forêt de Puig-reig (31) ⚠️ | Puig-reig › Berguedà | 1 |
| Forêt de Puig-reig (32) ⚠️ | Puig-reig › Berguedà | 1 |
| Forêt de Puig-reig (33) ⚠️ | Puig-reig › Berguedà | 1 |
| Forêt de Puig-reig (37) ⚠️ | Puig-reig › Berguedà | 1 |
| Forêt de Puig-reig (39) ⚠️ | Puig-reig › Berguedà | 1 |
| Forêt de Puig-reig (44) ⚠️ | Puig-reig › Berguedà | 1 |
| Forêt de Puig-reig (49) ⚠️ | Casserres › Berguedà | 1 |
| Forêt de Casserres (15) ⚠️ | Casserres › Berguedà | 1 |
| Forêt de Gironella (8) ⚠️ | Gironella › Berguedà | 1 |
| Forêt de Calaf (5) ⚠️ | Calaf › Anoia | 1 |
| Forêt de Calaf (6) ⚠️ | Calaf › Anoia | 1 |
| Forêt de Castellbell i el Vilar (3) ⚠️ | Castellbell i el Vilar › Bages | 1 |
| Forêt de Castellbell i el Vilar (7) ⚠️ | Castellbell i el Vilar › Bages | 1 |
| Forêt de Premià de Dalt (3) ⚠️ | Premià de Dalt › Maresme | 1 |
| Forêt de Premià de Dalt (4) ⚠️ | Premià de Dalt › Maresme | 1 |
| Forêt de Balsareny (68) ⚠️ | Balsareny › Bages | 1 |
| Forêt de Balsareny (69) ⚠️ | Balsareny › Bages | 1 |
| Forêt de Navàs (27) ⚠️ | Navàs › Bages | 1 |
| Forêt de Sallent (78) ⚠️ | Sallent › Bages | 1 |
| Forêt de Balsareny (79) ⚠️ | Balsareny › Bages | 1 |
| Forêt de Balsareny (84) ⚠️ | Balsareny › Bages | 1 |
| Forêt de Navàs (29) ⚠️ | Navàs › Bages | 1 |
| Forêt de Guardiola de Berguedà (17) ⚠️ | Guardiola de Berguedà › Berguedà | 1 |
| Forêt de Guardiola de Berguedà (18) ⚠️ | Guardiola de Berguedà › Berguedà | 1 |
| Forêt de Navàs (30) ⚠️ | Navàs › Bages | 1 |
| Forêt de Montmajor (72) ⚠️ | Montmajor › Berguedà | 1 |
| Forêt de Vilanova del Camí (6) ⚠️ | Vilanova del Camí › Anoia | 1 |
| Forêt de la Pobla de Claramunt (7) ⚠️ | la Pobla de Claramunt › Anoia | 1 |
| Forêt de la Pobla de Claramunt (8) ⚠️ | la Pobla de Claramunt › Anoia | 1 |
| Forêt de Calella (3) ⚠️ | Calella › Maresme | 1 |
| Forêt de Sant Pol de Mar (8) ⚠️ | Sant Pol de Mar › Maresme | 1 |
| Forêt de Sant Pol de Mar (13) ⚠️ | Sant Pol de Mar › Maresme | 1 |
| Forêt de Sant Pol de Mar (14) ⚠️ | Sant Pol de Mar › Maresme | 1 |
| Parc de Can Preses ⚠️ | Sant Andreu de la Barca › Baix Llobregat | 1 |
| Forêt de Corbera de Llobregat (14) ⚠️ | Corbera de Llobregat › Baix Llobregat | 1 |
| Forêt de Vic (15) ⚠️ | Vic › Osona (Barcelone) | 1 |
| Forêt de Calldetenes ⚠️ | Calldetenes › Osona (Barcelone) | 1 |
| Forêt de Santa Eugènia de Berga ⚠️ | Santa Eugènia de Berga › Osona (Barcelone) | 1 |
| Forêt de Corbera de Llobregat (15) ⚠️ | Corbera de Llobregat › Baix Llobregat | 1 |
| Forêt de la Palma de Cervelló (2) ⚠️ | la Palma de Cervelló › Baix Llobregat | 1 |
| Forêt de Corbera de Llobregat (22) ⚠️ | Corbera de Llobregat › Baix Llobregat | 1 |
| Forêt de Corbera de Llobregat (23) ⚠️ | Cervelló › Baix Llobregat | 1 |
| Forêt de Cervelló (9) ⚠️ | Cervelló › Baix Llobregat | 1 |
| Forêt de Vallirana (26) ⚠️ | Vallirana › Baix Llobregat | 1 |
| Forêt de Vallirana (27) ⚠️ | Vallirana › Baix Llobregat | 1 |
| Forêt de Vallirana (28) ⚠️ | Vallirana › Baix Llobregat | 1 |
| Forêt de Vallirana (32) ⚠️ | Vallirana › Baix Llobregat | 1 |
| Forêt de Cervelló (17) ⚠️ | Cervelló › Baix Llobregat | 1 |
| Forêt de Rubí (69) ⚠️ | Rubí › Vallès Occidental | 1 |
| Forêt de Rubí (70) ⚠️ | Ullastrell › Vallès Occidental | 1 |
| Forêt de Rubí (74) ⚠️ | Rubí › Vallès Occidental | 1 |
| Forêt de Rubí (77) ⚠️ | Rubí › Vallès Occidental | 1 |
| Forêt de Monistrol de Montserrat (13) ⚠️ | Monistrol de Montserrat › Bages | 1 |
| Forêt de Marganell (6) ⚠️ | Marganell › Bages | 1 |
| Forêt de Marganell (7) ⚠️ | Marganell › Bages | 1 |
| Forêt de Monistrol de Montserrat (19) ⚠️ | Monistrol de Montserrat › Bages | 1 |
| Forêt de Monistrol de Montserrat (20) ⚠️ | Monistrol de Montserrat › Bages | 1 |
| Forêt de Monistrol de Montserrat (21) ⚠️ | Monistrol de Montserrat › Bages | 1 |
| Forêt de Monistrol de Montserrat (29) ⚠️ | Monistrol de Montserrat › Bages | 1 |
| Forêt de Monistrol de Montserrat (30) ⚠️ | Monistrol de Montserrat › Bages | 1 |
| Forêt de Monistrol de Montserrat (31) ⚠️ | Monistrol de Montserrat › Bages | 1 |
| Forêt de Vacarisses (14) ⚠️ | Vacarisses › Vallès Occidental | 1 |
| Forêt de Vacarisses (21) ⚠️ | Vacarisses › Vallès Occidental | 1 |
| Forêt de Vacarisses (28) ⚠️ | Vacarisses › Vallès Occidental | 1 |
| Forêt de Vacarisses (36) ⚠️ | Vacarisses › Vallès Occidental | 1 |
| Forêt de Monistrol de Montserrat (37) ⚠️ | Monistrol de Montserrat › Bages | 1 |
| Forêt de Rellinars (2) ⚠️ | Rellinars › Vallès Occidental | 1 |
| Forêt de Bagà (11) ⚠️ | Bagà › Berguedà | 1 |
| Forêt de Bagà (13) ⚠️ | Bagà › Berguedà | 1 |
| Forêt de Guardiola de Berguedà (23) ⚠️ | Guardiola de Berguedà › Berguedà | 1 |
| Forêt de Guardiola de Berguedà (25) ⚠️ | Guardiola de Berguedà › Berguedà | 1 |
| Forêt de Guardiola de Berguedà (26) ⚠️ | Guardiola de Berguedà › Berguedà | 1 |
| Forêt de la Pobla de Lillet (8) ⚠️ | la Pobla de Lillet › Berguedà | 1 |
| Forêt de Castellbell i el Vilar (25) ⚠️ | Castellbell i el Vilar › Bages | 1 |
| Forêt de Sant Vicenç de Castellet (8) ⚠️ | Sant Vicenç de Castellet › Bages | 1 |
| Forêt de Sant Vicenç de Castellet (10) ⚠️ | Sant Vicenç de Castellet › Bages | 1 |
| Forêt de Castellbell i el Vilar (31) ⚠️ | Sant Vicenç de Castellet › Bages | 1 |
| Forêt de Sant Vicenç de Castellet (13) ⚠️ | Sant Vicenç de Castellet › Bages | 1 |
| Forêt de Castellgalí (9) ⚠️ | Castellgalí › Bages | 1 |
| Forêt de Olesa de Montserrat (15) ⚠️ | Olesa de Montserrat › Baix Llobregat | 1 |
| Forêt de Esparreguera (24) ⚠️ | Esparreguera › Baix Llobregat | 1 |
| Forêt de el Bruc (22) ⚠️ | el Bruc › Anoia | 1 |
| Forêt de el Bruc (28) ⚠️ | el Bruc › Anoia | 1 |
| Forêt de el Bruc (29) ⚠️ | el Bruc › Anoia | 1 |
| Forêt de Marganell (15) ⚠️ | Marganell › Bages | 1 |
| Forêt de Marganell (19) ⚠️ | Marganell › Bages | 1 |
| Forêt de Marganell (20) ⚠️ | Castellbell i el Vilar › Bages | 1 |
| Forêt de Castellbell i el Vilar (42) ⚠️ | Castellbell i el Vilar › Bages | 1 |
| Forêt de Castellbell i el Vilar (45) ⚠️ | Castellbell i el Vilar › Bages | 1 |
| Forêt de Castellolí (7) ⚠️ | Castellolí › Anoia | 1 |
| Forêt de la Pobla de Claramunt (11) ⚠️ | la Pobla de Claramunt › Anoia | 1 |
| Forêt de Vilanova del Camí (7) ⚠️ | Vilanova del Camí › Anoia | 1 |
| Forêt de Castellolí (21) ⚠️ | Castellolí › Anoia | 1 |
| Forêt de Castellolí (24) ⚠️ | Castellolí › Anoia | 1 |
| Forêt de Monistrol de Montserrat (42) ⚠️ | Monistrol de Montserrat › Bages | 1 |
| Forêt de Castellbell i el Vilar (55) ⚠️ | Castellbell i el Vilar › Bages | 1 |
| Forêt de Castellbell i el Vilar (62) ⚠️ | Castellbell i el Vilar › Bages | 1 |
| Forêt de Rellinars (5) ⚠️ | Rellinars › Vallès Occidental | 1 |
| Forêt de Rellinars (7) ⚠️ | Rellinars › Vallès Occidental | 1 |
| Forêt de el Pont de Vilomara i Rocafort (5) ⚠️ | el Pont de Vilomara i Rocafort › Bages | 1 |
| Forêt de el Pont de Vilomara i Rocafort (12) ⚠️ | el Pont de Vilomara i Rocafort › Bages | 1 |
| Forêt de Moià (19) ⚠️ | Moià › Moianès | 1 |
| Forêt de Moià (20) ⚠️ | Moià › Moianès | 1 |
| Forêt de Moià (27) ⚠️ | Moià › Moianès | 1 |
| Forêt de Vilanova i la Geltrú (18) ⚠️ | Vilanova i la Geltrú › Garraf | 1 |
| Forêt de Sitges (18) ⚠️ | Sitges › Garraf | 1 |
| Forêt de Sitges (21) ⚠️ | Sitges › Garraf | 1 |
| Forêt de Vilanova i la Geltrú (23) ⚠️ | Vilanova i la Geltrú › Garraf | 1 |
| Forêt de Vilanova i la Geltrú (24) ⚠️ | Vilanova i la Geltrú › Garraf | 1 |
| Parc de Sitges (27) ⚠️ | Sitges › Garraf | 1 |
| Forêt de Sitges (37) ⚠️ | Sitges › Garraf | 1 |
| Forêt de Sitges (38) ⚠️ | Sitges › Garraf | 1 |
| Forêt de Sitges (39) ⚠️ | Sitges › Garraf | 1 |
| Forêt de Castelldefels (8) ⚠️ | Castelldefels › Baix Llobregat | 1 |
| Forêt de Castelldefels (9) ⚠️ | Castelldefels › Baix Llobregat | 1 |
| Forêt de Sitges (48) ⚠️ | Sitges › Garraf | 1 |
| Forêt de Sitges (50) ⚠️ | Sitges › Garraf | 1 |
| Forêt de Sitges (54) ⚠️ | Sitges › Garraf | 1 |
| Forêt de Sitges (55) ⚠️ | Sitges › Garraf | 1 |
| Forêt de Begues (32) ⚠️ | Gavà › Baix Llobregat | 1 |
| Forêt de Gavà (76) ⚠️ | Gavà › Baix Llobregat | 1 |
| Forêt de Gavà (79) ⚠️ | Gavà › Baix Llobregat | 1 |
| Forêt de Gavà (80) ⚠️ | Begues › Baix Llobregat | 1 |
| Forêt de Manresa (124) ⚠️ | Manresa › Bages | 1 |
| Forêt de Castellgalí (15) ⚠️ | Castellgalí › Bages | 1 |
| Forêt de Manresa (127) ⚠️ | Manresa › Bages | 1 |
| Forêt de Manresa (128) ⚠️ | Manresa › Bages | 1 |
| Forêt de Manresa (132) ⚠️ | Manresa › Bages | 1 |
| Forêt de Artés (27) ⚠️ | Artés › Bages | 1 |
| Forêt de Avinyó (67) ⚠️ | Avinyó › Bages | 1 |
| Forêt de Avinyó (75) ⚠️ | Avinyó › Bages | 1 |
| Forêt de Avinyó (82) ⚠️ | Avinyó › Bages | 1 |
| Forêt de Calders (35) ⚠️ | Calders › Moianès | 1 |
| Forêt de Calders (39) ⚠️ | Calders › Moianès | 1 |
| Forêt de Calders (46) ⚠️ | Calders › Moianès | 1 |
| Forêt de Calders (47) ⚠️ | Calders › Moianès | 1 |
| Forêt de Cardedeu (28) ⚠️ | la Roca del Vallès › Vallès Oriental | 1 |
| Forêt de Llinars del Vallès (59) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Bois de Llinars del Vallès (29) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Forêt de Cardedeu (31) ⚠️ | Cardedeu › Vallès Oriental | 1 |
| Parc de Pompeu Fabra (2) ⚠️ | Cardedeu › Vallès Oriental | 1 |
| Forêt de Sant Antoni de Vilamajor (35) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 1 |
| Forêt de Sant Celoni (21) ⚠️ | Sant Celoni › Vallès Oriental | 1 |
| Forêt de Santa Maria de Palautordera (19) ⚠️ | Santa Maria de Palautordera › Vallès Oriental | 1 |
| Forêt de Llinars del Vallès (65) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Forêt de Súria (9) ⚠️ | Súria › Bages | 1 |
| Forêt de Súria (12) ⚠️ | Súria › Bages | 1 |
| Forêt de Súria (13) ⚠️ | Súria › Bages | 1 |
| Forêt de Sant Mateu de Bages (38) ⚠️ | Sant Mateu de Bages › Bages | 1 |
| Forêt de Súria (19) ⚠️ | Súria › Bages | 1 |
| Forêt de Súria (20) ⚠️ | Súria › Bages | 1 |
| Forêt de Súria (22) ⚠️ | Súria › Bages | 1 |
| Forêt de Cànoves i Samalús (39) ⚠️ | Cànoves i Samalús › Vallès Oriental | 1 |
| Bois de Cabrils (12) ⚠️ | Cabrils › Maresme | 1 |
| Forêt de Vallromanes (8) ⚠️ | Vallromanes › Vallès Oriental | 1 |
| Forêt de Sallent (79) ⚠️ | Sallent › Bages | 1 |
| Forêt de Sallent (80) ⚠️ | Sallent › Bages | 1 |
| Forêt de Avinyó (91) ⚠️ | Avinyó › Bages | 1 |
| Forêt de Avinyó (92) ⚠️ | Avinyó › Bages | 1 |
| Forêt de Navàs (36) ⚠️ | Navàs › Bages | 1 |
| Forêt de Navàs (42) ⚠️ | Navàs › Bages | 1 |
| Forêt de Navàs (43) ⚠️ | Navàs › Bages | 1 |
| Forêt de Gaià (44) ⚠️ | Gaià › Bages | 1 |
| Arborètum ⚠️ | Santa Maria de Palautordera › Vallès Oriental | 1 |
| Forêt de Santa Maria de Palautordera (22) ⚠️ | Santa Maria de Palautordera › Vallès Oriental | 1 |
| Forêt de Santa Maria de Palautordera (23) ⚠️ | Santa Maria de Palautordera › Vallès Oriental | 1 |
| Forêt de Santa Maria de Palautordera (28) ⚠️ | Santa Maria de Palautordera › Vallès Oriental | 1 |
| Forêt de Sant Esteve de Palautordera (10) ⚠️ | Sant Esteve de Palautordera › Vallès Oriental | 1 |
| Forêt de Vilada (8) ⚠️ | Vilada › Berguedà | 1 |
| Forêt de Castell de l'Areny (20) ⚠️ | Castell de l'Areny › Berguedà | 1 |
| Forêt de Cercs (34) ⚠️ | Cercs › Berguedà | 1 |
| Forêt de Cercs (35) ⚠️ | Cercs › Berguedà | 1 |
| Forêt de Cercs (41) ⚠️ | Cercs › Berguedà | 1 |
| Forêt de Fígols (8) ⚠️ | Fígols › Berguedà | 1 |
| Forêt de Fígols (10) ⚠️ | Fígols › Berguedà | 1 |
| Forêt de la Pobla de Lillet (28) ⚠️ | la Pobla de Lillet › Berguedà | 1 |
| Forêt de Vilada (15) ⚠️ | Vilada › Berguedà | 1 |
| Forêt de Sant Quirze de Besora ⚠️ | Sant Quirze de Besora › Osona (Barcelone) | 1 |
| Forêt de Sant Quirze de Besora (3) ⚠️ | Sant Quirze de Besora › Osona (Barcelone) | 1 |
| Forêt de Montesquiu (2) ⚠️ | Montesquiu › Osona (Barcelone) | 1 |
| Forêt de Guardiola de Berguedà (41) ⚠️ | Guardiola de Berguedà › Berguedà | 1 |
| Forêt de Guardiola de Berguedà (42) ⚠️ | Guardiola de Berguedà › Berguedà | 1 |
| Forêt de Guardiola de Berguedà (53) ⚠️ | Guardiola de Berguedà › Berguedà | 1 |
| Forêt de Monistrol de Calders (14) ⚠️ | Monistrol de Calders › Moianès | 1 |
| Forêt de Monistrol de Calders (15) ⚠️ | Monistrol de Calders › Moianès | 1 |
| Forêt de Monistrol de Calders (18) ⚠️ | Monistrol de Calders › Moianès | 1 |
| Forêt de Monistrol de Calders (21) ⚠️ | Monistrol de Calders › Moianès | 1 |
| Forêt de Mura (15) ⚠️ | Mura › Bages | 1 |
| Forêt de Mura (29) ⚠️ | Mura › Bages | 1 |
| Forêt de Talamanca (26) ⚠️ | Talamanca › Bages | 1 |
| Forêt de Sant Llorenç Savall (18) ⚠️ | Sant Llorenç Savall › Vallès Occidental | 1 |
| Forêt de Talamanca (32) ⚠️ | Talamanca › Bages | 1 |
| Forêt de Navarcles (10) ⚠️ | Navarcles › Bages | 1 |
| Forêt de Navarcles (12) ⚠️ | Navarcles › Bages | 1 |
| Forêt de Calders (52) ⚠️ | Calders › Moianès | 1 |
| Forêt de Calders (54) ⚠️ | Calders › Moianès | 1 |
| Forêt de Talamanca (35) ⚠️ | Talamanca › Bages | 1 |
| Forêt de Calders (59) ⚠️ | Calders › Moianès | 1 |
| Forêt de Sant Vicenç de Castellet (27) ⚠️ | Sant Vicenç de Castellet › Bages | 1 |
| Forêt de Sant Vicenç de Castellet (33) ⚠️ | Sant Vicenç de Castellet › Bages | 1 |
| Forêt de Sant Pere Sallavinera (12) ⚠️ | Sant Pere Sallavinera › Anoia | 1 |
| Forêt de Aguilar de Segarra (46) ⚠️ | Aguilar de Segarra › Bages | 1 |
| Forêt de Sant Pere Sallavinera (13) ⚠️ | Sant Pere Sallavinera › Anoia | 1 |
| Forêt de Sant Pere Sallavinera (16) ⚠️ | Sant Pere Sallavinera › Anoia | 1 |
| Forêt de Aguilar de Segarra (47) ⚠️ | Aguilar de Segarra › Bages | 1 |
| Forêt de Sant Pere Sallavinera (33) ⚠️ | Sant Pere Sallavinera › Anoia | 1 |
| Forêt de Sant Pere Sallavinera (34) ⚠️ | Sant Pere Sallavinera › Anoia | 1 |
| Forêt de Sant Pere Sallavinera (38) ⚠️ | Sant Pere Sallavinera › Anoia | 1 |
| Forêt de Sant Pere Sallavinera (40) ⚠️ | Sant Pere Sallavinera › Anoia | 1 |
| Forêt de Sant Pere Sallavinera (41) ⚠️ | Sant Pere Sallavinera › Anoia | 1 |
| Forêt de Sant Pere Sallavinera (49) ⚠️ | Sant Pere Sallavinera › Anoia | 1 |
| Forêt de Sant Pere Sallavinera (52) ⚠️ | Sant Pere Sallavinera › Anoia | 1 |
| Forêt de Sant Pere Sallavinera (54) ⚠️ | Sant Pere Sallavinera › Anoia | 1 |
| Forêt de Calonge de Segarra (12) ⚠️ | Calonge de Segarra › Anoia | 1 |
| Forêt de Matadepera (216) ⚠️ | Matadepera › Vallès Occidental | 1 |
| Forêt de Sant Vicenç de Castellet (34) ⚠️ | Sant Vicenç de Castellet › Bages | 1 |
| Forêt de Monistrol de Montserrat (43) ⚠️ | Monistrol de Montserrat › Bages | 1 |
| Forêt de Castellgalí (24) ⚠️ | Castellgalí › Bages | 1 |
| Forêt de els Prats de Rei (10) ⚠️ | els Prats de Rei › Anoia | 1 |
| Forêt de els Prats de Rei (11) ⚠️ | els Prats de Rei › Anoia | 1 |
| Forêt de els Prats de Rei (16) ⚠️ | els Prats de Rei › Anoia | 1 |
| Forêt de els Prats de Rei (17) ⚠️ | els Prats de Rei › Anoia | 1 |
| Forêt de els Prats de Rei (18) ⚠️ | els Prats de Rei › Anoia | 1 |
| Forêt de els Prats de Rei (21) ⚠️ | els Prats de Rei › Anoia | 1 |
| Forêt de els Prats de Rei (22) ⚠️ | els Prats de Rei › Anoia | 1 |
| Forêt de els Prats de Rei (27) ⚠️ | els Prats de Rei › Anoia | 1 |
| Forêt de els Prats de Rei (28) ⚠️ | els Prats de Rei › Anoia | 1 |
| Forêt de els Prats de Rei (29) ⚠️ | els Prats de Rei › Anoia | 1 |
| Forêt de Rajadell (44) ⚠️ | Rajadell › Bages | 1 |
| Forêt de Sant Salvador de Guardiola (63) ⚠️ | Sant Salvador de Guardiola › Bages | 1 |
| Forêt de Sant Salvador de Guardiola (69) ⚠️ | Sant Salvador de Guardiola › Bages | 1 |
| Forêt de Sant Salvador de Guardiola (75) ⚠️ | Sant Salvador de Guardiola › Bages | 1 |
| Forêt de Sant Salvador de Guardiola (76) ⚠️ | Sant Salvador de Guardiola › Bages | 1 |
| Forêt de Sant Salvador de Guardiola (77) ⚠️ | Sant Salvador de Guardiola › Bages | 1 |
| Forêt de Sant Salvador de Guardiola (78) ⚠️ | Sant Salvador de Guardiola › Bages | 1 |
| Forêt de Sant Salvador de Guardiola (79) ⚠️ | Sant Salvador de Guardiola › Bages | 1 |
| Forêt de Sant Salvador de Guardiola (82) ⚠️ | Sant Salvador de Guardiola › Bages | 1 |
| Forêt de Sant Salvador de Guardiola (84) ⚠️ | Sant Salvador de Guardiola › Bages | 1 |
| Forêt de Sant Salvador de Guardiola (85) ⚠️ | Sant Salvador de Guardiola › Bages | 1 |
| Forêt de Sant Salvador de Guardiola (98) ⚠️ | Sant Salvador de Guardiola › Bages | 1 |
| Forêt de Sant Salvador de Guardiola (99) ⚠️ | Sant Salvador de Guardiola › Bages | 1 |
| Forêt de Sant Salvador de Guardiola (100) ⚠️ | Sant Salvador de Guardiola › Bages | 1 |
| Forêt de Sant Salvador de Guardiola (105) ⚠️ | Sant Salvador de Guardiola › Bages | 1 |
| Forêt de Sant Salvador de Guardiola (106) ⚠️ | Sant Salvador de Guardiola › Bages | 1 |
| Forêt de Sant Salvador de Guardiola (112) ⚠️ | Sant Salvador de Guardiola › Bages | 1 |
| Forêt de Sant Salvador de Guardiola (118) ⚠️ | Sant Salvador de Guardiola › Bages | 1 |
| Forêt de el Bruc (40) ⚠️ | el Bruc › Anoia | 1 |
| Forêt de Castellolí (29) ⚠️ | Castellolí › Anoia | 1 |
| Forêt de Castellolí (31) ⚠️ | Castellolí › Anoia | 1 |
| Forêt de Castellgalí (26) ⚠️ | Castellgalí › Bages | 1 |
| Forêt de Sant Vicenç de Castellet (38) ⚠️ | Sant Vicenç de Castellet › Bages | 1 |
| Forêt de Castellgalí (31) ⚠️ | Castellgalí › Bages | 1 |
| Forêt de Vacarisses (59) ⚠️ | Vacarisses › Vallès Occidental | 1 |
| Forêt de Vacarisses (61) ⚠️ | Vacarisses › Vallès Occidental | 1 |
| Forêt de Olesa de Montserrat (32) ⚠️ | Olesa de Montserrat › Baix Llobregat | 1 |
| Forêt de Olesa de Montserrat (35) ⚠️ | Olesa de Montserrat › Baix Llobregat | 1 |
| Forêt de Olesa de Montserrat (41) ⚠️ | Olesa de Montserrat › Baix Llobregat | 1 |
| Forêt de Olesa de Montserrat (43) ⚠️ | Olesa de Montserrat › Baix Llobregat | 1 |
| Forêt de Olesa de Montserrat (45) ⚠️ | Olesa de Montserrat › Baix Llobregat | 1 |
| Forêt de Abrera (15) ⚠️ | Abrera › Baix Llobregat | 1 |
| Forêt de Esparreguera (34) ⚠️ | Esparreguera › Baix Llobregat | 1 |
| Bois de Abrera (6) ⚠️ | Abrera › Baix Llobregat | 1 |
| Bois de Esparreguera (2) ⚠️ | Esparreguera › Baix Llobregat | 1 |
| Parc (32) ⚠️ | Abrera › Baix Llobregat | 1 |
| Forêt de Abrera (19) ⚠️ | Abrera › Baix Llobregat | 1 |
| Forêt de Abrera (22) ⚠️ | Abrera › Baix Llobregat | 1 |
| Forêt de Abrera (23) ⚠️ | Abrera › Baix Llobregat | 1 |
| Forêt de Abrera (27) ⚠️ | Abrera › Baix Llobregat | 1 |
| Forêt de Martorell (14) ⚠️ | Martorell › Baix Llobregat | 1 |
| Forêt de Martorell (16) ⚠️ | Martorell › Baix Llobregat | 1 |
| Forêt de Martorell (17) ⚠️ | Martorell › Baix Llobregat | 1 |
| Forêt de Castellbisbal (25) ⚠️ | Castellbisbal › Vallès Occidental | 1 |
| Forêt de Castellbisbal (32) ⚠️ | Castellbisbal › Vallès Occidental | 1 |
| Forêt de Castellbisbal (37) ⚠️ | Castellbisbal › Vallès Occidental | 1 |
| Forêt de Castellbisbal (42) ⚠️ | Castellbisbal › Vallès Occidental | 1 |
| Forêt de Castellbisbal (43) ⚠️ | Castellbisbal › Vallès Occidental | 1 |
| Forêt de Castellgalí (36) ⚠️ | Castellgalí › Bages | 1 |
| Forêt de Castellgalí (37) ⚠️ | Castellgalí › Bages | 1 |
| Forêt de Castellgalí (39) ⚠️ | Castellgalí › Bages | 1 |
| Forêt de Castellgalí (46) ⚠️ | Castellgalí › Bages | 1 |
| Forêt de Castellgalí (48) ⚠️ | Castellgalí › Bages | 1 |
| Forêt de Castellgalí (55) ⚠️ | Castellgalí › Bages | 1 |
| Forêt de Sant Vicenç de Castellet (39) ⚠️ | Sant Vicenç de Castellet › Bages | 1 |
| Forêt de Sant Vicenç de Castellet (46) ⚠️ | Sant Vicenç de Castellet › Bages | 1 |
| Forêt de Castellbell i el Vilar (73) ⚠️ | Castellbell i el Vilar › Bages | 1 |
| Forêt de Navàs (56) ⚠️ | Navàs › Bages | 1 |
| Forêt de Navàs (64) ⚠️ | Navàs › Bages | 1 |
| Forêt de Navàs (78) ⚠️ | Navàs › Bages | 1 |
| Forêt de Viver i Serrateix (36) ⚠️ | Viver i Serrateix › Berguedà | 1 |
| Forêt de Viver i Serrateix (52) ⚠️ | Viver i Serrateix › Berguedà | 1 |
| Forêt de Viver i Serrateix (53) ⚠️ | Viver i Serrateix › Berguedà | 1 |
| Forêt de Santa Maria de Merlès (23) ⚠️ | Santa Maria de Merlès › Berguedà | 1 |
| Forêt de Gironella (12) ⚠️ | Gironella › Berguedà | 1 |
| Forêt de Gironella (13) ⚠️ | Gironella › Berguedà | 1 |
| Forêt de Sagàs (21) ⚠️ | Sagàs › Berguedà | 1 |
| Forêt de Avià (23) ⚠️ | Avià › Berguedà | 1 |
| Forêt de Avià (26) ⚠️ | Avià › Berguedà | 1 |
| Forêt de Montclar (29) ⚠️ | Montclar › Berguedà | 1 |
| Forêt de l'Espunyola (53) ⚠️ | l'Espunyola › Berguedà | 1 |
| Forêt de l'Espunyola (63) ⚠️ | l'Espunyola › Berguedà | 1 |
| Forêt de l'Espunyola (67) ⚠️ | l'Espunyola › Berguedà | 1 |
| Forêt de l'Espunyola (72) ⚠️ | l'Espunyola › Berguedà | 1 |
| Forêt de Capolat (28) ⚠️ | Capolat › Berguedà | 1 |
| Forêt de Montmajor (80) ⚠️ | Montmajor › Berguedà | 1 |
| Forêt de Montmajor (86) ⚠️ | Montmajor › Berguedà | 1 |
| Forêt de Montmajor (89) ⚠️ | Montmajor › Berguedà | 1 |
| Forêt de Montmajor (105) ⚠️ | Montmajor › Berguedà | 1 |
| Forêt de Montmajor (107) ⚠️ | Montmajor › Berguedà | 1 |
| Forêt de Navàs (95) ⚠️ | Navàs › Bages | 1 |
| Forêt de Sant Mateu de Bages (40) ⚠️ | Sant Mateu de Bages › Bages | 1 |
| Forêt de Sant Mateu de Bages (44) ⚠️ | Sant Mateu de Bages › Bages | 1 |
| Forêt de Sant Mateu de Bages (47) ⚠️ | Sant Mateu de Bages › Bages | 1 |
| Forêt de Sant Mateu de Bages (48) ⚠️ | Sant Mateu de Bages › Bages | 1 |
| Forêt de Sant Mateu de Bages (49) ⚠️ | Sant Mateu de Bages › Bages | 1 |
| Forêt de Sant Mateu de Bages (52) ⚠️ | Sant Mateu de Bages › Bages | 1 |
| Forêt de Navàs (106) ⚠️ | Sant Mateu de Bages › Bages | 1 |
| Forêt de Navàs (107) ⚠️ | Navàs › Bages | 1 |
| Forêt de Navàs (112) ⚠️ | Navàs › Bages | 1 |
| Forêt de Navàs (115) ⚠️ | Navàs › Bages | 1 |
| Forêt de Navàs (129) ⚠️ | Navàs › Bages | 1 |
| Forêt de Navàs (134) ⚠️ | Navàs › Bages | 1 |
| Forêt de Navàs (136) ⚠️ | Navàs › Bages | 1 |
| Forêt de Cardona (64) ⚠️ | Cardona › Bages | 1 |
| Forêt de Cardona (66) ⚠️ | Cardona › Bages | 1 |
| Forêt de Navàs (140) ⚠️ | Navàs › Bages | 1 |
| Forêt de Viver i Serrateix (64) ⚠️ | Viver i Serrateix › Berguedà | 1 |
| Forêt de Viver i Serrateix (68) ⚠️ | Viver i Serrateix › Berguedà | 1 |
| Forêt de Viver i Serrateix (69) ⚠️ | Viver i Serrateix › Berguedà | 1 |
| Forêt de Viver i Serrateix (80) ⚠️ | Viver i Serrateix › Berguedà | 1 |
| Forêt de Montmajor (124) ⚠️ | Montmajor › Berguedà | 1 |
| Forêt de Montmajor (132) ⚠️ | Montmajor › Berguedà | 1 |
| Forêt de Avinyó (105) ⚠️ | Avinyó › Bages | 1 |
| Forêt de Avinyó (106) ⚠️ | Avinyó › Bages | 1 |
| Forêt de Sant Feliu Sasserra (12) ⚠️ | Sant Feliu Sasserra › Bages | 1 |
| Forêt de Santa Maria de Merlès (36) ⚠️ | Santa Maria de Merlès › Berguedà | 1 |
| Forêt de Santa Maria de Merlès (41) ⚠️ | Santa Maria de Merlès › Berguedà | 1 |
| Forêt de Santa Maria de Merlès (43) ⚠️ | Santa Maria de Merlès › Berguedà | 1 |
| Forêt de Santa Maria de Merlès (44) ⚠️ | Santa Maria de Merlès › Berguedà | 1 |
| Forêt de Santa Maria de Merlès (48) ⚠️ | Santa Maria de Merlès › Berguedà | 1 |
| Forêt de Prats de Lluçanès (8) ⚠️ | Prats de Lluçanès › Lluçanès | 1 |
| Forêt de Santa Maria de Merlès (63) ⚠️ | Santa Maria de Merlès › Berguedà | 1 |
| Forêt de Santa Maria de Merlès (64) ⚠️ | Santa Maria de Merlès › Berguedà | 1 |
| Forêt de Santa Maria de Merlès (65) ⚠️ | Santa Maria de Merlès › Berguedà | 1 |
| Forêt de Santa Maria de Merlès (67) ⚠️ | Santa Maria de Merlès › Berguedà | 1 |
| Forêt de Santa Eulàlia de Riuprimer (3) ⚠️ | Santa Eulàlia de Riuprimer › Osona (Barcelone) | 1 |
| Bois de Sant Cugat del Vallès (116) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Forêt de Sant Cugat del Vallès (119) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Forêt de Sant Cugat del Vallès (125) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Bois de Barcelona (109) ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Sant Just Desvern (5) ⚠️ | Sant Just Desvern › Baix Llobregat | 1 |
| Forêt de Sant Cugat del Vallès (136) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Bois de Sant Cugat del Vallès (123) ⚠️ | Rubí › Vallès Occidental | 1 |
| Forêt de Rubí (79) ⚠️ | Rubí › Vallès Occidental | 1 |
| Forêt de Rubí (81) ⚠️ | Rubí › Vallès Occidental | 1 |
| Forêt de Rubí (86) ⚠️ | Rubí › Vallès Occidental | 1 |
| Forêt de Rubí (88) ⚠️ | Rubí › Vallès Occidental | 1 |
| Parc de Rubí (29) ⚠️ | Rubí › Vallès Occidental | 1 |
| Forêt de Rubí (90) ⚠️ | Rubí › Vallès Occidental | 1 |
| Forêt de Sant Cugat del Vallès (140) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Forêt de Sant Cugat del Vallès (141) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Forêt de Sant Cugat del Vallès (145) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Forêt de Sant Cugat del Vallès (151) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Forêt de Santa Maria d'Oló (40) ⚠️ | Santa Maria d'Oló › Moianès | 1 |
| Forêt de Castellgalí (63) ⚠️ | Castellgalí › Bages | 1 |
| Forêt de Matadepera (218) ⚠️ | Matadepera › Vallès Occidental | 1 |
| Forêt de Saldes (26) ⚠️ | Saldes › Berguedà | 1 |
| Forêt de Borredà (34) ⚠️ | Borredà › Berguedà | 1 |
| Forêt de Borredà (35) ⚠️ | Borredà › Berguedà | 1 |
| Bois de Llinars del Vallès (31) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Bois de Llinars del Vallès (33) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Plaça de les Tereses ⚠️ | Mataró › Maresme | 1 |
| Forêt de Jorba (6) ⚠️ | Jorba › Anoia | 1 |
| Forêt de Jorba (9) ⚠️ | Jorba › Anoia | 1 |
| Forêt de Jorba (10) ⚠️ | Jorba › Anoia | 1 |
| Forêt de Igualada (4) ⚠️ | Igualada › Anoia | 1 |
| Forêt de Jorba (21) ⚠️ | Jorba › Anoia | 1 |
| Forêt de Argençola (28) ⚠️ | Argençola › Anoia | 1 |
| Forêt de Òdena (40) ⚠️ | Òdena › Anoia | 1 |
| Forêt de Igualada (8) ⚠️ | Igualada › Anoia | 1 |
| Forêt de la Pobla de Claramunt (12) ⚠️ | la Pobla de Claramunt › Anoia | 1 |
| Forêt de Vilanova del Camí (9) ⚠️ | Vilanova del Camí › Anoia | 1 |
| Forêt de Vilanova del Camí (11) ⚠️ | Vilanova del Camí › Anoia | 1 |
| Forêt de Santa Margarida de Montbui (20) ⚠️ | Santa Margarida de Montbui › Anoia | 1 |
| Forêt de Jorba (37) ⚠️ | Jorba › Anoia | 1 |
| Forêt de Jorba (39) ⚠️ | Jorba › Anoia | 1 |
| Forêt de Jorba (40) ⚠️ | Jorba › Anoia | 1 |
| Forêt de Castellfollit del Boix (32) ⚠️ | Castellfollit del Boix › Bages | 1 |
| Forêt de Castellfollit del Boix (33) ⚠️ | Castellfollit del Boix › Bages | 1 |
| Bois de Sant Pere de Torelló (3) ⚠️ | Sant Pere de Torelló › Osona (Barcelone) | 1 |
| Forêt de Castellfollit del Boix (37) ⚠️ | Castellfollit del Boix › Bages | 1 |
| Forêt de Rajadell (56) ⚠️ | Rajadell › Bages | 1 |
| Forêt de Rajadell (58) ⚠️ | Rajadell › Bages | 1 |
| Forêt de Rajadell (59) ⚠️ | Rajadell › Bages | 1 |
| Forêt de Rajadell (63) ⚠️ | Rajadell › Bages | 1 |
| Forêt de Rajadell (64) ⚠️ | Rajadell › Bages | 1 |
| Forêt de Rajadell (65) ⚠️ | Rajadell › Bages | 1 |
| Forêt de Rajadell (66) ⚠️ | Rajadell › Bages | 1 |
| Forêt de Rajadell (70) ⚠️ | Rajadell › Bages | 1 |
| Forêt de Cubelles (14) ⚠️ | Cubelles › Garraf | 1 |
| Forêt de Cubelles (15) ⚠️ | Cubelles › Garraf | 1 |
| Forêt de Castellet i la Gornal (68) ⚠️ | Castellet i la Gornal › Alt Penedès | 1 |
| Forêt de Olesa de Bonesvalls (38) ⚠️ | Olesa de Bonesvalls › Alt Penedès | 1 |
| Forêt de Olesa de Bonesvalls (40) ⚠️ | Olesa de Bonesvalls › Alt Penedès | 1 |
| Forêt de Olivella (58) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Olivella (60) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Olivella (63) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Olivella (65) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Olivella (69) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Olivella (70) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Begues (40) ⚠️ | Begues › Baix Llobregat | 1 |
| Forêt de Begues (43) ⚠️ | Begues › Baix Llobregat | 1 |
| Forêt de Olivella (72) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Olivella (73) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Olivella (76) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Olivella (79) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Olivella (82) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Olivella (84) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Olivella (85) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Begues (54) ⚠️ | Begues › Baix Llobregat | 1 |
| Forêt de Begues (61) ⚠️ | Begues › Baix Llobregat | 1 |
| Forêt de Begues (62) ⚠️ | Begues › Baix Llobregat | 1 |
| Forêt de Olivella (89) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Olivella (93) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Olivella (96) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Olivella (99) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Begues (73) ⚠️ | Begues › Baix Llobregat | 1 |
| Forêt de Olivella (106) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Begues (78) ⚠️ | Begues › Baix Llobregat | 1 |
| Forêt de Olesa de Bonesvalls (45) ⚠️ | Olesa de Bonesvalls › Alt Penedès | 1 |
| Forêt de Olivella (109) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Olivella (117) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Sitges (73) ⚠️ | Sitges › Garraf | 1 |
| Forêt de Olivella (121) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Sant Pere de Ribes (92) ⚠️ | Sant Pere de Ribes › Garraf | 1 |
| Forêt de Sant Pere de Ribes (97) ⚠️ | Sant Pere de Ribes › Garraf | 1 |
| Forêt de Sant Pere de Ribes (100) ⚠️ | Sitges › Garraf | 1 |
| Forêt de Sitges (75) ⚠️ | Sitges › Garraf | 1 |
| Forêt de Sitges (76) ⚠️ | Sitges › Garraf | 1 |
| Forêt de Sitges (78) ⚠️ | Sitges › Garraf | 1 |
| Forêt de Sitges (79) ⚠️ | Sitges › Garraf | 1 |
| Forêt de Sant Pere de Ribes (105) ⚠️ | Sitges › Garraf | 1 |
| Forêt de Sitges (81) ⚠️ | Sitges › Garraf | 1 |
| Forêt de Sitges (89) ⚠️ | Sitges › Garraf | 1 |
| Forêt de Castellet i la Gornal (79) ⚠️ | Castellet i la Gornal › Alt Penedès | 1 |
| Forêt de Cubelles (30) ⚠️ | Cubelles › Garraf | 1 |
| Forêt de Canyelles (7) ⚠️ | Canyelles › Garraf | 1 |
| Forêt de Canyelles (9) ⚠️ | Canyelles › Garraf | 1 |
| Forêt de Castellet i la Gornal (90) ⚠️ | Castellet i la Gornal › Alt Penedès | 1 |
| Forêt de Canyelles (19) ⚠️ | Canyelles › Garraf | 1 |
| Forêt de Vilanova i la Geltrú (46) ⚠️ | Vilanova i la Geltrú › Garraf | 1 |
| Forêt de Vilanova i la Geltrú (53) ⚠️ | Vilanova i la Geltrú › Garraf | 1 |
| Forêt de Vilanova i la Geltrú (59) ⚠️ | Vilanova i la Geltrú › Garraf | 1 |
| Forêt de Vilanova i la Geltrú (65) ⚠️ | Vilanova i la Geltrú › Garraf | 1 |
| Forêt de Vilanova i la Geltrú (67) ⚠️ | Vilanova i la Geltrú › Garraf | 1 |
| Forêt de Vilanova i la Geltrú (68) ⚠️ | Vilanova i la Geltrú › Garraf | 1 |
| Forêt de Vilanova i la Geltrú (69) ⚠️ | Vilanova i la Geltrú › Garraf | 1 |
| Forêt de Canyelles (24) ⚠️ | Canyelles › Garraf | 1 |
| Forêt de Olivella (128) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Olivella (129) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Olivella (131) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Olivella (132) ⚠️ | Olivella › Garraf | 1 |
| Forêt de Avinyonet del Penedès (69) ⚠️ | Avinyonet del Penedès › Alt Penedès | 1 |
| Forêt de Sant Joan Despí (3) ⚠️ | Sant Joan Despí › Baix Llobregat | 1 |
| Forêt de Monistrol de Calders (28) ⚠️ | Monistrol de Calders › Moianès | 1 |
| Forêt de Sant Julià de Cerdanyola (5) ⚠️ | Sant Julià de Cerdanyola › Berguedà | 1 |
| Forêt de Sant Julià de Cerdanyola (10) ⚠️ | Sant Julià de Cerdanyola › Berguedà | 1 |
| Forêt de Viladecavalls (13) ⚠️ | Viladecavalls › Vallès Occidental | 1 |
| Forêt de Gaià (70) ⚠️ | Gaià › Bages | 1 |
| Forêt de Gisclareny (12) ⚠️ | Gisclareny › Berguedà | 1 |
| Forêt de Gisclareny (13) ⚠️ | Gisclareny › Berguedà | 1 |
| Forêt de Bagà (22) ⚠️ | Bagà › Berguedà | 1 |
| Forêt de Bagà (24) ⚠️ | Bagà › Berguedà | 1 |
| Forêt de Navàs (147) ⚠️ | Navàs › Bages | 1 |
| Forêt de Viver i Serrateix (97) ⚠️ | Viver i Serrateix › Berguedà | 1 |
| Forêt de Viver i Serrateix (99) ⚠️ | Viver i Serrateix › Berguedà | 1 |
| Forêt de Viver i Serrateix (101) ⚠️ | Viver i Serrateix › Berguedà | 1 |
| Forêt de Viver i Serrateix (102) ⚠️ | Viver i Serrateix › Berguedà | 1 |
| Forêt de Viver i Serrateix (105) ⚠️ | Viver i Serrateix › Berguedà | 1 |
| Forêt de Viver i Serrateix (112) ⚠️ | Viver i Serrateix › Berguedà | 1 |
| Forêt de Santa Maria de Merlès (74) ⚠️ | Santa Maria de Merlès › Berguedà | 1 |
| Forêt de Súria (38) ⚠️ | Súria › Bages | 1 |
| Forêt de Súria (39) ⚠️ | Súria › Bages | 1 |
| Forêt de Santa Maria d'Oló (43) ⚠️ | Santa Maria d'Oló › Moianès | 1 |
| Forêt de Santa Maria d'Oló (48) ⚠️ | Santa Maria d'Oló › Moianès | 1 |
| Forêt de Santa Maria d'Oló (50) ⚠️ | Santa Maria d'Oló › Moianès | 1 |
| Forêt de Borredà (40) ⚠️ | Borredà › Berguedà | 1 |
| Forêt de Borredà (45) ⚠️ | Borredà › Berguedà | 1 |
| Forêt de Sagàs (25) ⚠️ | Sagàs › Berguedà | 1 |
| Forêt de Sagàs (30) ⚠️ | Sagàs › Berguedà | 1 |
| Forêt de Santa Maria de Merlès (85) ⚠️ | Santa Maria de Merlès › Berguedà | 1 |
| Forêt de Santa Maria de Merlès (92) ⚠️ | Santa Maria de Merlès › Berguedà | 1 |
| Forêt de Santa Maria de Merlès (104) ⚠️ | Santa Maria de Merlès › Berguedà | 1 |
| Forêt de Santa Maria de Merlès (109) ⚠️ | Santa Maria de Merlès › Berguedà | 1 |
| Forêt de Santa Maria de Merlès (117) ⚠️ | Santa Maria de Merlès › Berguedà | 1 |
| Forêt de Santa Maria de Merlès (119) ⚠️ | Santa Maria de Merlès › Berguedà | 1 |
| Forêt de Santa Maria de Merlès (122) ⚠️ | Santa Maria de Merlès › Berguedà | 1 |
| Forêt de Sagàs (36) ⚠️ | Sagàs › Berguedà | 1 |
| Forêt de el Papiol (6) ⚠️ | el Papiol › Baix Llobregat | 1 |
| Forêt de el Papiol (8) ⚠️ | el Papiol › Baix Llobregat | 1 |
| Forêt de Aguilar de Segarra (52) ⚠️ | Aguilar de Segarra › Bages | 1 |
| Forêt de Aguilar de Segarra (53) ⚠️ | Aguilar de Segarra › Bages | 1 |
| Bois de Sant Cebrià de Vallalta (3) ⚠️ | Sant Cebrià de Vallalta › Maresme | 1 |
| Forêt de Rupit i Pruit (18) ⚠️ | Rupit i Pruit › Osona (Barcelone) | 1 |
| Forêt de Rupit i Pruit (20) ⚠️ | Rupit i Pruit › Osona (Barcelone) | 1 |
| Forêt de Rupit i Pruit (27) ⚠️ | Rupit i Pruit › Osona (Barcelone) | 1 |
| Forêt de Rupit i Pruit (28) ⚠️ | Rupit i Pruit › Osona (Barcelone) | 1 |
| Forêt de Rupit i Pruit (30) ⚠️ | Rupit i Pruit › Osona (Barcelone) | 1 |
| Forêt de Rupit i Pruit (31) ⚠️ | Rupit i Pruit › Osona (Barcelone) | 1 |
| Forêt de Avià (54) ⚠️ | Avià › Berguedà | 1 |
| Forêt de Avià (55) ⚠️ | Avià › Berguedà | 1 |
| Forêt de Cardedeu (33) ⚠️ | Cardedeu › Vallès Oriental | 1 |
| Forêt de Cardedeu (36) ⚠️ | Cardedeu › Vallès Oriental | 1 |
| Forêt de Navàs (153) ⚠️ | Navàs › Bages | 1 |
| Forêt de la Quar (21) ⚠️ | la Quar › Berguedà | 1 |
| Forêt de Sant Pol de Mar (19) ⚠️ | Sant Pol de Mar › Maresme | 1 |
| Parc Fluvial (2) ⚠️ | Vilanova del Vallès › Vallès Oriental | 1 |
| Forêt de Collbató (9) ⚠️ | Collbató › Baix Llobregat | 1 |
| Forêt de Collbató (10) ⚠️ | Collbató › Baix Llobregat | 1 |
| Forêt de Collbató (11) ⚠️ | Collbató › Baix Llobregat | 1 |
| Forêt de Collbató (12) ⚠️ | Collbató › Baix Llobregat | 1 |
| Forêt de Collbató (13) ⚠️ | Collbató › Baix Llobregat | 1 |
| Forêt de Collbató (18) ⚠️ | Esparreguera › Baix Llobregat | 1 |
| Forêt de els Hostalets de Pierola (18) ⚠️ | els Hostalets de Pierola › Anoia | 1 |
| Forêt de els Hostalets de Pierola (21) ⚠️ | els Hostalets de Pierola › Anoia | 1 |
| Forêt de el Bruc (45) ⚠️ | el Bruc › Anoia | 1 |
| Forêt de Esparreguera (39) ⚠️ | Esparreguera › Baix Llobregat | 1 |
| Forêt de Sitges (91) ⚠️ | Sitges › Garraf | 1 |
| Forêt de Granera (31) ⚠️ | Granera › Moianès | 1 |
| Forêt de Granera (33) ⚠️ | Granera › Moianès | 1 |
| Forêt de Granera (34) ⚠️ | Granera › Moianès | 1 |
| Forêt de Granera (37) ⚠️ | Granera › Moianès | 1 |
| Forêt de Seva (19) ⚠️ | Seva › Osona (Barcelone) | 1 |
| Forêt de Seva (21) ⚠️ | Seva › Osona (Barcelone) | 1 |
| Forêt de el Brull (24) ⚠️ | el Brull › Osona (Barcelone) | 1 |
| Forêt de Tagamanent (20) ⚠️ | Tagamanent › Vallès Oriental | 1 |
| Forêt de Sant Martí de Centelles (51) ⚠️ | Sant Martí de Centelles › Osona (Barcelone) | 1 |
| Forêt de Sant Martí de Centelles (55) ⚠️ | Sant Martí de Centelles › Osona (Barcelone) | 1 |
| Forêt de Centelles (17) ⚠️ | Centelles › Osona (Barcelone) | 1 |
| Forêt de Centelles (19) ⚠️ | Sant Martí de Centelles › Osona (Barcelone) | 1 |
| Forêt de Centelles (20) ⚠️ | Centelles › Osona (Barcelone) | 1 |
| Forêt de Centelles (24) ⚠️ | Centelles › Osona (Barcelone) | 1 |
| Forêt de Cànoves i Samalús (45) ⚠️ | Cànoves i Samalús › Vallès Oriental | 1 |
| Forêt de Cànoves i Samalús (46) ⚠️ | Cànoves i Samalús › Vallès Oriental | 1 |
| Forêt de el Brull (32) ⚠️ | el Brull › Osona (Barcelone) | 1 |
| Forêt de Fogars de Montclús (22) ⚠️ | Fogars de Montclús › Vallès Oriental | 1 |
| Forêt de Sant Quirze Safaja (17) ⚠️ | Sant Quirze Safaja › Moianès | 1 |
| Forêt de l'Ametlla del Vallès (16) ⚠️ | l'Ametlla del Vallès › Vallès Oriental | 1 |
| Forêt de Figaró-Montmany (11) ⚠️ | Figaró-Montmany › Vallès Oriental | 1 |
| Forêt de Sant Quirze Safaja (26) ⚠️ | Sant Quirze Safaja › Moianès | 1 |
| Forêt de Sant Quirze Safaja (29) ⚠️ | Sant Quirze Safaja › Moianès | 1 |
| Forêt de Sant Quirze Safaja (30) ⚠️ | Sant Quirze Safaja › Moianès | 1 |
| Forêt de Sant Quirze Safaja (32) ⚠️ | Sant Quirze Safaja › Moianès | 1 |
| Forêt de Bigues i Riells del Fai (26) ⚠️ | Bigues i Riells del Fai › Vallès Oriental | 1 |
| Forêt de Bigues i Riells del Fai (27) ⚠️ | Bigues i Riells del Fai › Vallès Oriental | 1 |
| Forêt de Sant Quirze Safaja (42) ⚠️ | Sant Quirze Safaja › Moianès | 1 |
| Forêt de Sant Quirze Safaja (49) ⚠️ | Sant Quirze Safaja › Moianès | 1 |
| Forêt de Sant Quirze Safaja (50) ⚠️ | Sant Quirze Safaja › Moianès | 1 |
| Forêt de Santa Maria d'Oló (64) ⚠️ | Santa Maria d'Oló › Moianès | 1 |
| Forêt de Santa Maria d'Oló (71) ⚠️ | Santa Maria d'Oló › Moianès | 1 |
| Forêt de Muntanyola (23) ⚠️ | Muntanyola › Osona (Barcelone) | 1 |
| Forêt de Santa Eulàlia de Riuprimer (13) ⚠️ | Santa Eulàlia de Riuprimer › Osona (Barcelone) | 1 |
| Forêt de Santa Eulàlia de Riuprimer (25) ⚠️ | Santa Eulàlia de Riuprimer › Osona (Barcelone) | 1 |
| Forêt de Muntanyola (28) ⚠️ | Muntanyola › Osona (Barcelone) | 1 |
| Forêt de Oristà (118) ⚠️ | Oristà › Lluçanès | 1 |
| Forêt de Oristà (119) ⚠️ | Oristà › Lluçanès | 1 |
| Forêt de Oristà (125) ⚠️ | Oristà › Lluçanès | 1 |
| Forêt de Oristà (133) ⚠️ | Oristà › Lluçanès | 1 |
| Forêt de Oristà (140) ⚠️ | Oristà › Lluçanès | 1 |
| Forêt de Oristà (148) ⚠️ | Oristà › Lluçanès | 1 |
| Forêt de Oristà (149) ⚠️ | Oristà › Lluçanès | 1 |
| Forêt de Oristà (155) ⚠️ | Oristà › Lluçanès | 1 |
| Forêt de Bigues i Riells del Fai (35) ⚠️ | Bigues i Riells del Fai › Vallès Oriental | 1 |
| Forêt de Bigues i Riells del Fai (36) ⚠️ | Bigues i Riells del Fai › Vallès Oriental | 1 |
| Forêt de Sant Mateu de Bages (60) ⚠️ | Sant Mateu de Bages › Bages | 1 |
| Forêt de Sant Mateu de Bages (67) ⚠️ | Sant Mateu de Bages › Bages | 1 |
| Forêt de Cardona (76) ⚠️ | Cardona › Bages | 1 |
| Forêt de Cardona (81) ⚠️ | Cardona › Bages | 1 |
| Forêt de Cardona (84) ⚠️ | Cardona › Bages | 1 |
| Forêt de Cardona (85) ⚠️ | Cardona › Bages | 1 |
| Forêt de Cardona (86) ⚠️ | Cardona › Bages | 1 |
| Forêt de Cardona (88) ⚠️ | Cardona › Bages | 1 |
| Forêt de Cardona (90) ⚠️ | Cardona › Bages | 1 |
| Forêt de Cardona (93) ⚠️ | Cardona › Bages | 1 |
| Forêt de Cardona (102) ⚠️ | Cardona › Bages | 1 |
| Forêt de Sant Mateu de Bages (84) ⚠️ | Sant Mateu de Bages › Bages | 1 |
| Forêt de Sant Mateu de Bages (87) ⚠️ | Sant Mateu de Bages › Bages | 1 |
| Forêt de Sant Mateu de Bages (105) ⚠️ | Sant Mateu de Bages › Bages | 1 |
| Forêt de Calonge de Segarra (19) ⚠️ | Calonge de Segarra › Anoia | 1 |
| Forêt de Sallent (93) ⚠️ | Sallent › Bages | 1 |
| Forêt de Sallent (94) ⚠️ | Sallent › Bages | 1 |
| Forêt de Sallent (95) ⚠️ | Sallent › Bages | 1 |
| Forêt de Sallent (96) ⚠️ | Sallent › Bages | 1 |
| Forêt de Sallent (100) ⚠️ | Sallent › Bages | 1 |
| Forêt de Sant Pere de Vilamajor (94) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 1 |
| Forêt de Vilanova i la Geltrú (71) ⚠️ | Vilanova i la Geltrú › Garraf | 1 |
| Forêt de Vilanova i la Geltrú (72) ⚠️ | Vilanova i la Geltrú › Garraf | 1 |
| Parc dels Colors ⚠️ | Mollet del Vallès › Vallès Oriental | 1 |
| Forêt de Bagà (34) ⚠️ | Bagà › Berguedà | 1 |
| Forêt de Santa Maria de Merlès (131) ⚠️ | Santa Maria de Merlès › Berguedà | 1 |
| Forêt de Santa Maria de Merlès (134) ⚠️ | Santa Maria de Merlès › Berguedà | 1 |
| Forêt de Santa Maria de Merlès (136) ⚠️ | Santa Maria de Merlès › Berguedà | 1 |
| Forêt de Lluçà (9) ⚠️ | Lluçà › Lluçanès | 1 |
| Forêt de la Garriga (52) ⚠️ | la Garriga › Vallès Oriental | 1 |
| Forêt de les Franqueses del Vallès (57) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 1 |
| Forêt de la Garriga (57) ⚠️ | la Garriga › Vallès Oriental | 1 |
| Forêt de les Franqueses del Vallès (63) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 1 |
| Parc de Canovelles (5) ⚠️ | Canovelles › Vallès Oriental | 1 |
| Forêt de les Franqueses del Vallès (65) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 1 |
| Forêt de la Roca del Vallès (11) ⚠️ | la Roca del Vallès › Vallès Oriental | 1 |
| Forêt de Argentona (5) ⚠️ | Argentona › Maresme | 1 |
| Forêt de Dosrius (32) ⚠️ | Dosrius › Maresme | 1 |
| Forêt de Dosrius (35) ⚠️ | Dosrius › Maresme | 1 |
| Forêt de la Garriga (59) ⚠️ | la Garriga › Vallès Oriental | 1 |
| Forêt de Balenyà (12) ⚠️ | Balenyà › Osona (Barcelone) | 1 |
| Forêt de Balenyà (17) ⚠️ | Balenyà › Osona (Barcelone) | 1 |
| Forêt de Balenyà (18) ⚠️ | Balenyà › Osona (Barcelone) | 1 |
| Forêt de Tona (6) ⚠️ | Tona › Osona (Barcelone) | 1 |
| Forêt de Tona (7) ⚠️ | Tona › Osona (Barcelone) | 1 |
| Forêt de Balenyà (21) ⚠️ | Balenyà › Osona (Barcelone) | 1 |
| Forêt de Tona (15) ⚠️ | Tona › Osona (Barcelone) | 1 |
| Forêt de Tona (20) ⚠️ | Tona › Osona (Barcelone) | 1 |
| Forêt de Tona (22) ⚠️ | Tona › Osona (Barcelone) | 1 |
| Forêt de Tona (28) ⚠️ | Tona › Osona (Barcelone) | 1 |
| Forêt de Tona (31) ⚠️ | Tona › Osona (Barcelone) | 1 |
| Forêt de Tona (33) ⚠️ | Tona › Osona (Barcelone) | 1 |
| Forêt de Tona (36) ⚠️ | Tona › Osona (Barcelone) | 1 |
| Forêt de Taradell (15) ⚠️ | Taradell › Osona (Barcelone) | 1 |
| Forêt de Seva (23) ⚠️ | Seva › Osona (Barcelone) | 1 |
| Forêt de Seva (28) ⚠️ | Seva › Osona (Barcelone) | 1 |
| Forêt de Seva (32) ⚠️ | Seva › Osona (Barcelone) | 1 |
| Forêt de Taradell (19) ⚠️ | Taradell › Osona (Barcelone) | 1 |
| Forêt de Tona (44) ⚠️ | Tona › Osona (Barcelone) | 1 |
| Forêt de Llinars del Vallès (72) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Forêt de Santa Maria de Palautordera (30) ⚠️ | Santa Maria de Palautordera › Vallès Oriental | 1 |
| Forêt de Navàs (161) ⚠️ | Navàs › Bages | 1 |
| Forêt de Berga (64) ⚠️ | Berga › Berguedà | 1 |
| Forêt de Avià (62) ⚠️ | Avià › Berguedà | 1 |
| Forêt de Cànoves i Samalús (50) ⚠️ | Cànoves i Samalús › Vallès Oriental | 1 |
| Forêt de el Bruc (46) ⚠️ | el Bruc › Anoia | 1 |
| Forêt de Gallifa (7) ⚠️ | Gallifa › Vallès Occidental | 1 |
| Forêt de Saldes (30) ⚠️ | Saldes › Berguedà | 1 |
| Forêt de Saldes (39) ⚠️ | Saldes › Berguedà | 1 |
| Forêt de Gisclareny (30) ⚠️ | Gisclareny › Berguedà | 1 |
| Forêt de Gisclareny (31) ⚠️ | Gisclareny › Berguedà | 1 |
| Forêt de Saldes (54) ⚠️ | Saldes › Berguedà | 1 |
| Forêt de Saldes (58) ⚠️ | Saldes › Berguedà | 1 |
| Forêt de Saldes (59) ⚠️ | Saldes › Berguedà | 1 |
| Forêt de Saldes (66) ⚠️ | Saldes › Berguedà | 1 |
| Forêt de Saldes (68) ⚠️ | Saldes › Berguedà | 1 |
| Forêt de Olvan (23) ⚠️ | Olvan › Berguedà | 1 |
| Forêt de Olvan (26) ⚠️ | Olvan › Berguedà | 1 |
| Forêt de Olvan (28) ⚠️ | Olvan › Berguedà | 1 |
| Forêt de Olvan (30) ⚠️ | Olvan › Berguedà | 1 |
| Forêt de Olvan (32) ⚠️ | Olvan › Berguedà | 1 |
| Forêt de Sant Pere de Vilamajor (98) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 1 |
| Forêt de Bagà (50) ⚠️ | Bagà › Berguedà | 1 |
| Forêt de Guardiola de Berguedà (77) ⚠️ | Guardiola de Berguedà › Berguedà | 1 |
| Forêt de Guardiola de Berguedà (83) ⚠️ | Guardiola de Berguedà › Berguedà | 1 |
| Forêt de Guardiola de Berguedà (89) ⚠️ | Guardiola de Berguedà › Berguedà | 1 |
| Forêt de Guardiola de Berguedà (90) ⚠️ | Guardiola de Berguedà › Berguedà | 1 |
| Forêt de Gisclareny (44) ⚠️ | Gisclareny › Berguedà | 1 |
| Forêt de Guardiola de Berguedà (94) ⚠️ | Guardiola de Berguedà › Berguedà | 1 |
| Forêt de Bagà (66) ⚠️ | Bagà › Berguedà | 1 |
| Forêt de Guardiola de Berguedà (116) ⚠️ | Guardiola de Berguedà › Berguedà | 1 |
| Forêt de Bagà (69) ⚠️ | Bagà › Berguedà | 1 |
| Forêt de Guardiola de Berguedà (117) ⚠️ | Guardiola de Berguedà › Berguedà | 1 |
| Forêt de Capolat (32) ⚠️ | Capolat › Berguedà | 1 |
| Forêt de Capolat (34) ⚠️ | Capolat › Berguedà | 1 |
| Forêt de Capolat (35) ⚠️ | Capolat › Berguedà | 1 |
| Forêt de Castellar del Riu (32) ⚠️ | Capolat › Berguedà | 1 |
| Forêt de Castellar del Riu (33) ⚠️ | Castellar del Riu › Berguedà | 1 |
| Forêt de Capolat (46) ⚠️ | Capolat › Berguedà | 1 |
| Forêt de Castellar del Riu (48) ⚠️ | Castellar del Riu › Berguedà | 1 |
| Forêt de Castellar del Riu (50) ⚠️ | Castellar del Riu › Berguedà | 1 |
| Forêt de Castellar del Riu (51) ⚠️ | Castellar del Riu › Berguedà | 1 |
| Forêt de Montmajor (134) ⚠️ | — | 1 |
| Forêt de Fígols (30) ⚠️ | Fígols › Berguedà | 1 |
| Forêt de Fígols (32) ⚠️ | Fígols › Berguedà | 1 |
| Forêt de Cercs (53) ⚠️ | Cercs › Berguedà | 1 |
| Forêt de Cercs (54) ⚠️ | Cercs › Berguedà | 1 |
| Forêt de la Garriga (60) ⚠️ | la Garriga › Vallès Oriental | 1 |
| Forêt de les Franqueses del Vallès (67) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 1 |
| Forêt de Cànoves i Samalús (52) ⚠️ | Cànoves i Samalús › Vallès Oriental | 1 |
| Forêt de Cànoves i Samalús (54) ⚠️ | Cànoves i Samalús › Vallès Oriental | 1 |
| Forêt de Prats de Lluçanès (9) ⚠️ | Prats de Lluçanès › Lluçanès | 1 |
| Forêt de Prats de Lluçanès (12) ⚠️ | Prats de Lluçanès › Lluçanès | 1 |
| Forêt de Prats de Lluçanès (15) ⚠️ | Prats de Lluçanès › Lluçanès | 1 |
| Forêt de Prats de Lluçanès (16) ⚠️ | Prats de Lluçanès › Lluçanès | 1 |
| Forêt de Prats de Lluçanès (20) ⚠️ | Prats de Lluçanès › Lluçanès | 1 |
| Forêt de Lluçà (21) ⚠️ | Lluçà › Lluçanès | 1 |
| Forêt de Lluçà (29) ⚠️ | Lluçà › Lluçanès | 1 |
| Forêt de Olost (8) ⚠️ | Olost › Lluçanès | 1 |
| Forêt de Lluçà (41) ⚠️ | Lluçà › Lluçanès | 1 |
| Forêt de Borredà (62) ⚠️ | la Quar › Berguedà | 1 |
| Forêt de Borredà (63) ⚠️ | Borredà › Berguedà | 1 |
| Forêt de Lluçà (47) ⚠️ | la Quar › Berguedà | 1 |
| Forêt de Borredà (67) ⚠️ | Borredà › Berguedà | 1 |
| Forêt de Borredà (68) ⚠️ | Borredà › Berguedà | 1 |
| Forêt de Borredà (71) ⚠️ | Borredà › Berguedà | 1 |
| Forêt de Borredà (76) ⚠️ | Borredà › Berguedà | 1 |
| Forêt de Borredà (85) ⚠️ | Borredà › Berguedà | 1 |
| Forêt de Sagàs (48) ⚠️ | Sagàs › Berguedà | 1 |
| Forêt de Borredà (106) ⚠️ | Borredà › Berguedà | 1 |
| Forêt de Borredà (109) ⚠️ | Borredà › Berguedà | 1 |
| Forêt de Borredà (114) ⚠️ | Borredà › Berguedà | 1 |
| Forêt de Borredà (121) ⚠️ | Borredà › Berguedà | 1 |
| Forêt de la Pobla de Lillet (35) ⚠️ | la Pobla de Lillet › Berguedà | 1 |
| Forêt de la Pobla de Lillet (46) ⚠️ | la Pobla de Lillet › Berguedà | 1 |
| Forêt de Sant Pere de Vilamajor (99) ⚠️ | Sant Pere de Vilamajor › Vallès Oriental | 1 |
| Forêt de la Pobla de Lillet (53) ⚠️ | la Pobla de Lillet › Berguedà | 1 |
| Forêt de la Pobla de Lillet (54) ⚠️ | la Pobla de Lillet › Berguedà | 1 |
| Forêt de les Franqueses del Vallès (73) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 1 |
| Forêt de Sant Julià de Cerdanyola (14) ⚠️ | Sant Julià de Cerdanyola › Berguedà | 1 |
| Forêt de Gisclareny (46) ⚠️ | Gisclareny › Berguedà | 1 |
| Forêt de Gisclareny (47) ⚠️ | Gisclareny › Berguedà | 1 |
| Forêt de Gisclareny (50) ⚠️ | Gisclareny › Berguedà | 1 |
| Forêt de Gisclareny (56) ⚠️ | Gisclareny › Berguedà | 1 |
| Forêt de Caldes de Montbui (10) ⚠️ | Caldes de Montbui › Vallès Oriental | 1 |
| Forêt de Saldes (79) ⚠️ | Saldes › Berguedà | 1 |
| Forêt de Castellar del Riu (57) ⚠️ | Castellar del Riu › Berguedà | 1 |
| Forêt de Castellar del Riu (62) ⚠️ | Castellar del Riu › Berguedà | 1 |
| Forêt de Castellar del Riu (65) ⚠️ | Castellar del Riu › Berguedà | 1 |
| Forêt de Castellar del Riu (66) ⚠️ | Castellar del Riu › Berguedà | 1 |
| Forêt de Fígols (39) ⚠️ | Fígols › Berguedà | 1 |
| Forêt de Saldes (85) ⚠️ | Saldes › Berguedà | 1 |
| Forêt de les Franqueses del Vallès (79) ⚠️ | les Franqueses del Vallès › Vallès Oriental | 1 |
| Forêt de Cardedeu (40) ⚠️ | Cardedeu › Vallès Oriental | 1 |
| Forêt de Cardedeu (41) ⚠️ | Cardedeu › Vallès Oriental | 1 |
| Forêt de Gisclareny (67) ⚠️ | Gisclareny › Berguedà | 1 |
| Forêt de Bagà (72) ⚠️ | Bagà › Berguedà | 1 |
| Forêt de Bagà (73) ⚠️ | Bagà › Berguedà | 1 |
| Forêt de Bagà (77) ⚠️ | Bagà › Berguedà | 1 |
| Forêt de Bagà (78) ⚠️ | Bagà › Berguedà | 1 |
| Forêt de Bagà (81) ⚠️ | Bagà › Berguedà | 1 |
| Forêt de Bagà (82) ⚠️ | Bagà › Berguedà | 1 |
| Bois de Barcelona (112) ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Sant Antoni de Vilamajor (46) ⚠️ | Sant Antoni de Vilamajor › Vallès Oriental | 1 |
| Forêt de Sant Antoni de Vilamajor (50) ⚠️ | Sant Antoni de Vilamajor › Vallès Oriental | 1 |
| Forêt de Sant Antoni de Vilamajor (54) ⚠️ | Sant Antoni de Vilamajor › Vallès Oriental | 1 |
| Forêt de Sant Antoni de Vilamajor (55) ⚠️ | Sant Antoni de Vilamajor › Vallès Oriental | 1 |
| Forêt de Saldes (101) ⚠️ | Saldes › Berguedà | 1 |
| Forêt de Saldes (109) ⚠️ | Saldes › Berguedà | 1 |
| Forêt de Saldes (116) ⚠️ | Saldes › Berguedà | 1 |
| Forêt de Vallcebre (34) ⚠️ | Vallcebre › Berguedà | 1 |
| Forêt de Vallcebre (40) ⚠️ | Vallcebre › Berguedà | 1 |
| Forêt de Saldes (123) ⚠️ | Saldes › Berguedà | 1 |
| Forêt de Saldes (125) ⚠️ | Saldes › Berguedà | 1 |
| Forêt de Gisclareny (69) ⚠️ | Gisclareny › Berguedà | 1 |
| Forêt de Vallcebre (48) ⚠️ | Vallcebre › Berguedà | 1 |
| Forêt de Centelles (36) ⚠️ | Centelles › Osona (Barcelone) | 1 |
| Forêt de Collsuspina (12) ⚠️ | Collsuspina › Moianès | 1 |
| Forêt de Santa Maria de Besora (20) ⚠️ | Santa Maria de Besora › Osona (Barcelone) | 1 |
| Forêt de Montesquiu (4) ⚠️ | Montesquiu › Osona (Barcelone) | 1 |
| Forêt de Montesquiu (5) ⚠️ | Montesquiu › Osona (Barcelone) | 1 |
| Forêt de Montesquiu (13) ⚠️ | Montesquiu › Osona (Barcelone) | 1 |
| Forêt de Montesquiu (16) ⚠️ | Montesquiu › Osona (Barcelone) | 1 |
| Forêt de Orís (13) ⚠️ | Orís › Osona (Barcelone) | 1 |
| Forêt de Orís (18) ⚠️ | Orís › Osona (Barcelone) | 1 |
| Forêt de Orís (19) ⚠️ | Orís › Osona (Barcelone) | 1 |
| Forêt de Sant Quirze de Besora (11) ⚠️ | Sant Quirze de Besora › Osona (Barcelone) | 1 |
| Forêt de Orís (24) ⚠️ | Sant Vicenç de Torelló › Osona (Barcelone) | 1 |
| Forêt de Sant Martí Sarroca (34) ⚠️ | Sant Martí Sarroca › Alt Penedès | 1 |
| Forêt de Sant Martí Sarroca (35) ⚠️ | Sant Martí Sarroca › Alt Penedès | 1 |
| Forêt de Pontons (7) ⚠️ | Pontons › Alt Penedès | 1 |
| Forêt de Bagà (84) ⚠️ | Bagà › Berguedà | 1 |
| Forêt de Tordera (56) ⚠️ | Tordera › Maresme | 1 |
| Forêt de Tordera (58) ⚠️ | Tordera › Maresme | 1 |
| Forêt de Tordera (67) ⚠️ | Tordera › Maresme | 1 |
| Forêt de Tordera (69) ⚠️ | Tordera › Maresme | 1 |
| Forêt de Tordera (70) ⚠️ | Tordera › Maresme | 1 |
| Forêt de Tordera (76) ⚠️ | Tordera › Maresme | 1 |
| Forêt de Tordera (77) ⚠️ | Tordera › Maresme | 1 |
| Forêt de Tordera (78) ⚠️ | Tordera › Maresme | 1 |
| Forêt de Fogars de la Selva (16) ⚠️ | Fogars de la Selva › la Selva (Barcelone) | 1 |
| Forêt de Fogars de la Selva (17) ⚠️ | Fogars de la Selva › la Selva (Barcelone) | 1 |
| Forêt de Fogars de la Selva (19) ⚠️ | Fogars de la Selva › la Selva (Barcelone) | 1 |
| Forêt de Palafolls (26) ⚠️ | Palafolls › Maresme | 1 |
| Forêt de Tordera (88) ⚠️ | Tordera › Maresme | 1 |
| Forêt de Tordera (89) ⚠️ | Tordera › Maresme | 1 |
| Forêt de Tordera (94) ⚠️ | Tordera › Maresme | 1 |
| Forêt de Tordera (96) ⚠️ | Tordera › Maresme | 1 |
| Forêt de Tordera (99) ⚠️ | Tordera › Maresme | 1 |
| Forêt de Castellet i la Gornal (94) ⚠️ | Castellet i la Gornal › Alt Penedès | 1 |
| Forêt de Barcelona (58) ⚠️ | Barcelona › Barcelonès | 1 |
| Bois de Molins de Rei (7) ⚠️ | Molins de Rei › Baix Llobregat | 1 |
| Forêt de Molins de Rei (13) ⚠️ | Molins de Rei › Baix Llobregat | 1 |
| Forêt de Sabadell (83) ⚠️ | Sabadell › Vallès Occidental | 1 |
| Forêt de Cercs (69) ⚠️ | Cercs › Berguedà | 1 |
| Forêt de Montornès del Vallès (13) ⚠️ | Montornès del Vallès › Vallès Oriental | 1 |
| Forêt de Montornès del Vallès (17) ⚠️ | Montornès del Vallès › Vallès Oriental | 1 |
| Forêt de Montornès del Vallès (18) ⚠️ | Montornès del Vallès › Vallès Oriental | 1 |
| Forêt de Vilanova del Vallès (10) ⚠️ | Vilanova del Vallès › Vallès Oriental | 1 |
| Forêt de Vilanova del Vallès (15) ⚠️ | Vilanova del Vallès › Vallès Oriental | 1 |
| Forêt de Vilanova del Vallès (16) ⚠️ | Vilanova del Vallès › Vallès Oriental | 1 |
| Bois de Vilanova del Vallès (15) ⚠️ | Vilanova del Vallès › Vallès Oriental | 1 |
| Forêt de la Roca del Vallès (19) ⚠️ | la Roca del Vallès › Vallès Oriental | 1 |
| Forêt de la Roca del Vallès (20) ⚠️ | la Roca del Vallès › Vallès Oriental | 1 |
| Forêt de la Roca del Vallès (22) ⚠️ | la Roca del Vallès › Vallès Oriental | 1 |
| Forêt de la Roca del Vallès (23) ⚠️ | la Roca del Vallès › Vallès Oriental | 1 |
| Forêt de la Roca del Vallès (28) ⚠️ | la Roca del Vallès › Vallès Oriental | 1 |
| Forêt de Llinars del Vallès (78) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Forêt de Llinars del Vallès (80) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Forêt de Llinars del Vallès (86) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Bois de Llinars del Vallès (36) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Forêt de Llinars del Vallès (87) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Forêt de la Llagosta (2) ⚠️ | la Llagosta › Vallès Oriental | 1 |
| Forêt de Montcada i Reixac (30) ⚠️ | Montcada i Reixac › Vallès Occidental | 1 |
| Forêt de Vallromanes (15) ⚠️ | Vallromanes › Vallès Oriental | 1 |
| Forêt de Vallromanes (19) ⚠️ | Vallromanes › Vallès Oriental | 1 |
| Forêt de Vilassar de Dalt (4) ⚠️ | Vilassar de Dalt › Maresme | 1 |
| Forêt de Vallcebre (50) ⚠️ | Vallcebre › Berguedà | 1 |
| Forêt de Fígols (40) ⚠️ | Fígols › Berguedà | 1 |
| Forêt de Fígols (43) ⚠️ | Fígols › Berguedà | 1 |
| Forêt de Cubelles (33) ⚠️ | Cubelles › Garraf | 1 |
| Forêt de Cubelles (36) ⚠️ | Cubelles › Garraf | 1 |
| Parc (34) ⚠️ | Cubelles › Garraf | 1 |
| Forêt de Cubelles (37) ⚠️ | Cubelles › Garraf | 1 |
| Forêt de Castellet i la Gornal (96) ⚠️ | Castellet i la Gornal › Alt Penedès | 1 |
| Forêt de Cubelles (44) ⚠️ | Cubelles › Garraf | 1 |
| Forêt de Cubelles (45) ⚠️ | Cubelles › Garraf | 1 |
| Forêt de Cubelles (48) ⚠️ | Cubelles › Garraf | 1 |
| Forêt de Vilanova i la Geltrú (76) ⚠️ | Vilanova i la Geltrú › Garraf | 1 |
| Forêt de Cubelles (49) ⚠️ | Cubelles › Garraf | 1 |
| Forêt de Torrelles de Llobregat (168) ⚠️ | Torrelles de Llobregat › Baix Llobregat | 1 |
| Forêt de Torrelles de Llobregat (170) ⚠️ | Torrelles de Llobregat › Baix Llobregat | 1 |
| Forêt de Torrelles de Llobregat (173) ⚠️ | Torrelles de Llobregat › Baix Llobregat | 1 |
| Forêt de Torrelles de Llobregat (174) ⚠️ | Torrelles de Llobregat › Baix Llobregat | 1 |
| Forêt de Torrelles de Llobregat (175) ⚠️ | Torrelles de Llobregat › Baix Llobregat | 1 |
| Forêt de Torrelles de Llobregat (177) ⚠️ | Torrelles de Llobregat › Baix Llobregat | 1 |
| Forêt de Torrelles de Llobregat (178) ⚠️ | Torrelles de Llobregat › Baix Llobregat | 1 |
| Forêt de Torrelles de Llobregat (179) ⚠️ | Torrelles de Llobregat › Baix Llobregat | 1 |
| Forêt de Santa Coloma de Cervelló (8) ⚠️ | Santa Coloma de Cervelló › Baix Llobregat | 1 |
| Forêt de Santa Coloma de Cervelló (9) ⚠️ | Santa Coloma de Cervelló › Baix Llobregat | 1 |
| Forêt de Sant Climent de Llobregat (17) ⚠️ | Sant Climent de Llobregat › Baix Llobregat | 1 |
| Forêt de Bagà (85) ⚠️ | Bagà › Berguedà | 1 |
| Forêt de Bagà (86) ⚠️ | Bagà › Berguedà | 1 |
| Forêt de Guardiola de Berguedà (134) ⚠️ | Guardiola de Berguedà › Berguedà | 1 |
| Forêt de Saldes (129) ⚠️ | Saldes › Berguedà | 1 |
| Forêt de Saldes (131) ⚠️ | Saldes › Berguedà | 1 |
| Forêt de Guardiola de Berguedà (139) ⚠️ | Guardiola de Berguedà › Berguedà | 1 |
| Forêt de Castellfollit del Boix (40) ⚠️ | Castellfollit del Boix › Bages | 1 |
| Forêt de Castellfollit del Boix (42) ⚠️ | Castellfollit del Boix › Bages | 1 |
| Forêt de Castellolí (34) ⚠️ | Castellolí › Anoia | 1 |
| Forêt de el Bruc (50) ⚠️ | el Bruc › Anoia | 1 |
| Forêt de Castellolí (38) ⚠️ | Castellolí › Anoia | 1 |
| Forêt de Marganell (31) ⚠️ | Marganell › Bages | 1 |
| Forêt de el Bruc (52) ⚠️ | el Bruc › Anoia | 1 |
| Forêt de Sant Julià de Cerdanyola (19) ⚠️ | Sant Julià de Cerdanyola › Berguedà | 1 |
| Forêt de Sant Martí de Tous (17) ⚠️ | Sant Martí de Tous › Anoia | 1 |
| Forêt de Sant Martí de Tous (22) ⚠️ | Sant Martí de Tous › Anoia | 1 |
| Forêt de Santa Margarida de Montbui (27) ⚠️ | Santa Margarida de Montbui › Anoia | 1 |
| Forêt de Santa Margarida de Montbui (30) ⚠️ | Santa Margarida de Montbui › Anoia | 1 |
| Forêt de Santa Margarida de Montbui (35) ⚠️ | Santa Margarida de Montbui › Anoia | 1 |
| Forêt de Santa Margarida de Montbui (37) ⚠️ | Santa Margarida de Montbui › Anoia | 1 |
| Forêt de Argençola (31) ⚠️ | Argençola › Anoia | 1 |
| Forêt de Argençola (37) ⚠️ | Argençola › Anoia | 1 |
| Forêt de Jorba (43) ⚠️ | Jorba › Anoia | 1 |
| Forêt de Sant Martí de Tous (35) ⚠️ | Sant Martí de Tous › Anoia | 1 |
| Forêt de Jorba (46) ⚠️ | Jorba › Anoia | 1 |
| Forêt de Jorba (47) ⚠️ | Jorba › Anoia | 1 |
| Forêt de Sant Martí de Tous (48) ⚠️ | Sant Martí de Tous › Anoia | 1 |
| Bois de Torrelles de Foix (7) ⚠️ | Torrelles de Foix › Alt Penedès | 1 |
| Bois de Torrelles de Foix (9) ⚠️ | Torrelles de Foix › Alt Penedès | 1 |
| Forêt de Artés (34) ⚠️ | Artés › Bages | 1 |
| Parc municipal el Serrat ⚠️ | Monistrol de Calders › Moianès | 1 |
| Forêt de Calders (66) ⚠️ | Calders › Moianès | 1 |
| Forêt de Calders (67) ⚠️ | Calders › Moianès | 1 |
| Forêt de Moià (43) ⚠️ | Moià › Moianès | 1 |
| Forêt de Moià (49) ⚠️ | Moià › Moianès | 1 |
| Forêt de Moià (56) ⚠️ | Moià › Moianès | 1 |
| Forêt de Moià (62) ⚠️ | Moià › Moianès | 1 |
| Forêt de Moià (63) ⚠️ | Moià › Moianès | 1 |
| Forêt de Sant Feliu Sasserra (24) ⚠️ | Sant Feliu Sasserra › Bages | 1 |
| Forêt de Sant Feliu Sasserra (32) ⚠️ | Sant Feliu Sasserra › Bages | 1 |
| Forêt de Castellar de n'Hug (28) ⚠️ | Castellar de n'Hug › Berguedà | 1 |
| Forêt de Castellar de n'Hug (46) ⚠️ | Castellar de n'Hug › Berguedà | 1 |
| Forêt de Guardiola de Berguedà (142) ⚠️ | Guardiola de Berguedà › Berguedà | 1 |
| Parc Central (8) ⚠️ | Sant Andreu de la Barca › Baix Llobregat | 1 |
| Forêt de Oristà (162) ⚠️ | Oristà › Lluçanès | 1 |
| Forêt de Oristà (166) ⚠️ | Oristà › Lluçanès | 1 |
| Forêt de Balsareny (89) ⚠️ | Balsareny › Bages | 1 |
| Parc de Òdena (3) ⚠️ | Òdena › Anoia | 1 |
| Forêt de Igualada (18) ⚠️ | Igualada › Anoia | 1 |
| Forêt de Òdena (59) ⚠️ | Òdena › Anoia | 1 |
| Forêt de Òdena (60) ⚠️ | Òdena › Anoia | 1 |
| Forêt de Jorba (50) ⚠️ | Jorba › Anoia | 1 |
| Forêt de Vilanova del Camí (18) ⚠️ | Vilanova del Camí › Anoia | 1 |
| Parc Fluvial (3) ⚠️ | Vilanova del Camí › Anoia | 1 |
| Forêt de Vilanova del Camí (23) ⚠️ | Vilanova del Camí › Anoia | 1 |
| Forêt de Santa Margarida de Montbui (44) ⚠️ | Santa Margarida de Montbui › Anoia | 1 |
| Forêt de Santa Margarida de Montbui (46) ⚠️ | Santa Margarida de Montbui › Anoia | 1 |
| Forêt de Santa Margarida de Montbui (47) ⚠️ | Santa Margarida de Montbui › Anoia | 1 |
| Forêt de Santa Margarida de Montbui (50) ⚠️ | Santa Margarida de Montbui › Anoia | 1 |
| Forêt de Santa Margarida de Montbui (53) ⚠️ | Santa Margarida de Montbui › Anoia | 1 |
| Forêt de Santa Margarida de Montbui (54) ⚠️ | Santa Margarida de Montbui › Anoia | 1 |
| Forêt de Òdena (64) ⚠️ | Òdena › Anoia | 1 |
| Forêt de Òdena (65) ⚠️ | Òdena › Anoia | 1 |
| Forêt de Jorba (52) ⚠️ | Jorba › Anoia | 1 |
| Forêt de Òdena (70) ⚠️ | Òdena › Anoia | 1 |
| Forêt de Òdena (77) ⚠️ | Òdena › Anoia | 1 |
| Forêt de Castellar del Riu (77) ⚠️ | Castellar del Riu › Berguedà | 1 |
| Forêt de la Pobla de Claramunt (19) ⚠️ | la Pobla de Claramunt › Anoia | 1 |
| Forêt de Carme (2) ⚠️ | Carme › Anoia | 1 |
| Forêt de Carme (3) ⚠️ | Carme › Anoia | 1 |
| Jardins d'Antonio Machado ⚠️ | Sant Andreu de la Barca › Baix Llobregat | 1 |
| Parc del Torrent de la Font del Pont ⚠️ | Sant Quirze del Vallès › Vallès Occidental | 1 |
| Forêt de Sant Cugat del Vallès (152) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Parc de la Marquesa ⚠️ | l'Hospitalet de Llobregat › Barcelonès | 1 |
| Bois de Viladecavalls (16) ⚠️ | Viladecavalls › Vallès Occidental | 1 |
| Forêt de Cardona (106) ⚠️ | Cardona › Bages | 1 |
| Verneda de Can Gili ⚠️ | Granollers › Vallès Oriental | 1 |
| Forêt de Cardona (113) ⚠️ | Cardona › Bages | 1 |
| Forêt de Cardona (116) ⚠️ | Cardona › Bages | 1 |
| Forêt de Cardona (117) ⚠️ | Cardona › Bages | 1 |
| Forêt de Castellbisbal (45) ⚠️ | Castellbisbal › Vallès Occidental | 1 |
| Forêt de Castellbisbal (46) ⚠️ | Castellbisbal › Vallès Occidental | 1 |
| Forêt de Castellbisbal (48) ⚠️ | Castellbisbal › Vallès Occidental | 1 |
| Forêt de el Papiol (10) ⚠️ | el Papiol › Baix Llobregat | 1 |
| Forêt de Rubí (97) ⚠️ | Rubí › Vallès Occidental | 1 |
| Forêt de Martorell (30) ⚠️ | Martorell › Baix Llobregat | 1 |
| Forêt de Martorell (37) ⚠️ | Martorell › Baix Llobregat | 1 |
| Forêt de Terrassa (80) ⚠️ | Terrassa › Vallès Occidental | 1 |
| Forêt de Terrassa (81) ⚠️ | Terrassa › Vallès Occidental | 1 |
| Forêt de Terrassa (84) ⚠️ | Terrassa › Vallès Occidental | 1 |
| Forêt de Terrassa (85) ⚠️ | Terrassa › Vallès Occidental | 1 |
| Forêt de Terrassa (90) ⚠️ | Terrassa › Vallès Occidental | 1 |
| Forêt de Terrassa (93) ⚠️ | Terrassa › Vallès Occidental | 1 |
| Parc de Ferran Bach-Esteve ⚠️ | Terrassa › Vallès Occidental | 1 |
| Forêt de Martorell (46) ⚠️ | Martorell › Baix Llobregat | 1 |
| Forêt de Martorell (47) ⚠️ | Martorell › Baix Llobregat | 1 |
| Forêt de Martorell (49) ⚠️ | Martorell › Baix Llobregat | 1 |
| Forêt de Esparreguera (42) ⚠️ | Esparreguera › Baix Llobregat | 1 |
| Forêt de Esparreguera (43) ⚠️ | Esparreguera › Baix Llobregat | 1 |
| Forêt de Esparreguera (44) ⚠️ | Esparreguera › Baix Llobregat | 1 |
| Forêt de Esparreguera (47) ⚠️ | Esparreguera › Baix Llobregat | 1 |
| Forêt de Esparreguera (48) ⚠️ | Esparreguera › Baix Llobregat | 1 |
| Forêt de Abrera (36) ⚠️ | Abrera › Baix Llobregat | 1 |
| Forêt de Esparreguera (51) ⚠️ | Esparreguera › Baix Llobregat | 1 |
| Forêt de Gelida (25) ⚠️ | Gelida › Alt Penedès | 1 |
| Forêt de Gelida (26) ⚠️ | Gelida › Alt Penedès | 1 |
| Forêt de Gelida (27) ⚠️ | Gelida › Alt Penedès | 1 |
| Forêt de Gelida (28) ⚠️ | Gelida › Alt Penedès | 1 |
| Forêt de Castellví de Rosanes (12) ⚠️ | Castellví de Rosanes › Baix Llobregat | 1 |
| Forêt de Gelida (32) ⚠️ | Gelida › Alt Penedès | 1 |
| Forêt de Santa Margarida de Montbui (64) ⚠️ | Santa Margarida de Montbui › Anoia | 1 |
| Forêt de la Pobla de Claramunt (23) ⚠️ | la Pobla de Claramunt › Anoia | 1 |
| Forêt de la Pobla de Claramunt (27) ⚠️ | la Pobla de Claramunt › Anoia | 1 |
| Forêt de la Pobla de Claramunt (31) ⚠️ | la Pobla de Claramunt › Anoia | 1 |
| Forêt de la Pobla de Claramunt (37) ⚠️ | la Pobla de Claramunt › Anoia | 1 |
| Forêt de la Pobla de Claramunt (39) ⚠️ | la Pobla de Claramunt › Anoia | 1 |
| Forêt de la Pobla de Claramunt (41) ⚠️ | la Pobla de Claramunt › Anoia | 1 |
| Forêt de la Pobla de Claramunt (44) ⚠️ | la Pobla de Claramunt › Anoia | 1 |
| Forêt de Capellades (2) ⚠️ | Capellades › Anoia | 1 |
| Forêt de Vallbona d'Anoia (2) ⚠️ | Vallbona d'Anoia › Anoia | 1 |
| Forêt de Cabrera d'Anoia (7) ⚠️ | Cabrera d'Anoia › Anoia | 1 |
| Forêt de Mediona (12) ⚠️ | Mediona › Alt Penedès | 1 |
| Forêt de Mediona (13) ⚠️ | Mediona › Alt Penedès | 1 |
| Forêt de Mediona (16) ⚠️ | Mediona › Alt Penedès | 1 |
| Forêt de Mediona (19) ⚠️ | Mediona › Alt Penedès | 1 |
| Forêt de Mediona (20) ⚠️ | Mediona › Alt Penedès | 1 |
| Forêt de la Torre de Claramunt (17) ⚠️ | la Torre de Claramunt › Anoia | 1 |
| Forêt de Mediona (24) ⚠️ | Mediona › Alt Penedès | 1 |
| Forêt de Mediona (26) ⚠️ | Mediona › Alt Penedès | 1 |
| Forêt de Piera (44) ⚠️ | Piera › Anoia | 1 |
| Forêt de Piera (51) ⚠️ | Piera › Anoia | 1 |
| Forêt de Mediona (33) ⚠️ | Mediona › Alt Penedès | 1 |
| Forêt de Cabrera d'Anoia (18) ⚠️ | Cabrera d'Anoia › Anoia | 1 |
| Forêt de Mediona (41) ⚠️ | Mediona › Alt Penedès | 1 |
| Forêt de la Torre de Claramunt (18) ⚠️ | la Torre de Claramunt › Anoia | 1 |
| Forêt de la Torre de Claramunt (20) ⚠️ | la Torre de Claramunt › Anoia | 1 |
| Forêt de la Torre de Claramunt (21) ⚠️ | la Torre de Claramunt › Anoia | 1 |
| Forêt de la Torre de Claramunt (26) ⚠️ | la Torre de Claramunt › Anoia | 1 |
| Forêt de la Torre de Claramunt (27) ⚠️ | la Torre de Claramunt › Anoia | 1 |
| Forêt de la Torre de Claramunt (28) ⚠️ | la Torre de Claramunt › Anoia | 1 |
| Forêt de la Torre de Claramunt (29) ⚠️ | la Torre de Claramunt › Anoia | 1 |
| Forêt de la Torre de Claramunt (30) ⚠️ | la Torre de Claramunt › Anoia | 1 |
| Forêt de Mediona (55) ⚠️ | Mediona › Alt Penedès | 1 |
| Forêt de Cabrera d'Anoia (19) ⚠️ | Cabrera d'Anoia › Anoia | 1 |
| Forêt de Cabrera d'Anoia (27) ⚠️ | Cabrera d'Anoia › Anoia | 1 |
| Forêt de Mediona (60) ⚠️ | Mediona › Alt Penedès | 1 |
| Forêt de Mediona (68) ⚠️ | Mediona › Alt Penedès | 1 |
| Forêt de Vallbona d'Anoia (9) ⚠️ | Vallbona d'Anoia › Anoia | 1 |
| Forêt de Cabrera d'Anoia (32) ⚠️ | Cabrera d'Anoia › Anoia | 1 |
| Forêt de Sant Pere de Riudebitlles (4) ⚠️ | Cabrera d'Anoia › Anoia | 1 |
| Forêt de Cabrera d'Anoia (37) ⚠️ | Cabrera d'Anoia › Anoia | 1 |
| Forêt de Cabrera d'Anoia (40) ⚠️ | Cabrera d'Anoia › Anoia | 1 |
| Forêt de Cabrera d'Anoia (46) ⚠️ | Cabrera d'Anoia › Anoia | 1 |
| Forêt de Piera (58) ⚠️ | Piera › Anoia | 1 |
| Forêt de Piera (59) ⚠️ | Piera › Anoia | 1 |
| Forêt de Torrelavit (28) ⚠️ | Torrelavit › Alt Penedès | 1 |
| Forêt de Torrelavit (30) ⚠️ | Torrelavit › Alt Penedès | 1 |
| Forêt de Torrelavit (31) ⚠️ | Torrelavit › Alt Penedès | 1 |
| Forêt de Torrelavit (43) ⚠️ | Torrelavit › Alt Penedès | 1 |
| Forêt de Torrelavit (44) ⚠️ | Torrelavit › Alt Penedès | 1 |
| Forêt de Torrelavit (45) ⚠️ | Torrelavit › Alt Penedès | 1 |
| Forêt de Mediona (71) ⚠️ | Mediona › Alt Penedès | 1 |
| Forêt de Sant Quintí de Mediona (8) ⚠️ | Sant Quintí de Mediona › Alt Penedès | 1 |
| Forêt de Piera (62) ⚠️ | Piera › Anoia | 1 |
| Forêt de Piera (63) ⚠️ | Piera › Anoia | 1 |
| Forêt de Piera (72) ⚠️ | Piera › Anoia | 1 |
| Forêt de Piera (76) ⚠️ | Piera › Anoia | 1 |
| Forêt de Piera (83) ⚠️ | Piera › Anoia | 1 |
| Forêt de Sant Pere de Riudebitlles (7) ⚠️ | Sant Pere de Riudebitlles › Alt Penedès | 1 |
| Forêt de Sant Pere de Riudebitlles (9) ⚠️ | Torrelavit › Alt Penedès | 1 |
| Forêt de Torrelavit (47) ⚠️ | Torrelavit › Alt Penedès | 1 |
| Forêt de Sant Pere de Riudebitlles (10) ⚠️ | Sant Pere de Riudebitlles › Alt Penedès | 1 |
| Forêt de Sant Quintí de Mediona (10) ⚠️ | Sant Quintí de Mediona › Alt Penedès | 1 |
| Forêt de Sant Quintí de Mediona (15) ⚠️ | Sant Quintí de Mediona › Alt Penedès | 1 |
| Forêt de Torrelavit (54) ⚠️ | Torrelavit › Alt Penedès | 1 |
| Forêt de Mediona (76) ⚠️ | Mediona › Alt Penedès | 1 |
| Forêt de Mediona (79) ⚠️ | Mediona › Alt Penedès | 1 |
| Forêt de Mediona (91) ⚠️ | Mediona › Alt Penedès | 1 |
| Forêt de Torrelles de Foix (8) ⚠️ | Torrelles de Foix › Alt Penedès | 1 |
| Forêt de Torrelles de Foix (9) ⚠️ | Torrelles de Foix › Alt Penedès | 1 |
| Forêt de Puig-reig (90) ⚠️ | Puig-reig › Berguedà | 1 |
| Forêt de Casserres (28) ⚠️ | Casserres › Berguedà | 1 |
| Forêt de Òdena (97) ⚠️ | Òdena › Anoia | 1 |
| Forêt de Òdena (99) ⚠️ | Òdena › Anoia | 1 |
| Forêt de Òdena (100) ⚠️ | Òdena › Anoia | 1 |
| Forêt de Òdena (104) ⚠️ | Òdena › Anoia | 1 |
| Forêt de Òdena (107) ⚠️ | Òdena › Anoia | 1 |
| Forêt de Òdena (112) ⚠️ | Òdena › Anoia | 1 |
| Forêt de Òdena (126) ⚠️ | Òdena › Anoia | 1 |
| Forêt de Tavertet (37) ⚠️ | Tavertet › Osona (Barcelone) | 1 |
| Forêt de Tavertet (43) ⚠️ | Tavertet › Osona (Barcelone) | 1 |
| Forêt de Tavertet (46) ⚠️ | Tavertet › Osona (Barcelone) | 1 |
| Forêt de Vilanova de Sau (59) ⚠️ | Vilanova de Sau › Osona (Barcelone) | 1 |
| Forêt de Tavertet (57) ⚠️ | Tavertet › Osona (Barcelone) | 1 |
| Forêt de Tavertet (58) ⚠️ | Vilanova de Sau › Osona (Barcelone) | 1 |
| Forêt de Tavertet (59) ⚠️ | Tavertet › Osona (Barcelone) | 1 |
| Forêt de Tavertet (67) ⚠️ | Tavertet › Osona (Barcelone) | 1 |
| Forêt de Vilanova de Sau (62) ⚠️ | Vilanova de Sau › Osona (Barcelone) | 1 |
| Forêt de Tavertet (72) ⚠️ | Tavertet › Osona (Barcelone) | 1 |
| Forêt de Tavertet (75) ⚠️ | Tavertet › Osona (Barcelone) | 1 |
| Plaça de l'Església (8) ⚠️ | Sant Andreu de la Barca › Baix Llobregat | 1 |
| Forêt de Alpens (23) ⚠️ | Alpens › Lluçanès | 1 |
| Forêt de Alpens (28) ⚠️ | Alpens › Lluçanès | 1 |
| Forêt de la Quar (53) ⚠️ | la Quar › Berguedà | 1 |
| Forêt de Olvan (40) ⚠️ | Olvan › Berguedà | 1 |
| Forêt de Gironella (16) ⚠️ | Gironella › Berguedà | 1 |
| Forêt de Gironella (17) ⚠️ | Gironella › Berguedà | 1 |
| Forêt de Sant Cugat del Vallès (155) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Forêt de Sant Cugat del Vallès (156) ⚠️ | Sant Cugat del Vallès › Vallès Occidental | 1 |
| Forêt de Santa Susanna (5) ⚠️ | Santa Susanna › Maresme | 1 |
| Forêt de Santa Susanna (8) ⚠️ | Santa Susanna › Maresme | 1 |
| Forêt de Santa Susanna (10) ⚠️ | Santa Susanna › Maresme | 1 |
| Forêt de Santa Susanna (12) ⚠️ | Santa Susanna › Maresme | 1 |
| Forêt de Santa Susanna (16) ⚠️ | Santa Susanna › Maresme | 1 |
| Forêt de Malgrat de Mar (7) ⚠️ | Malgrat de Mar › Maresme | 1 |
| Forêt de Arenys de Munt (10) ⚠️ | Arenys de Munt › Maresme | 1 |
| Forêt de Dosrius (38) ⚠️ | Dosrius › Maresme | 1 |
| Forêt de Sant Vicenç de Montalt (9) ⚠️ | Sant Vicenç de Montalt › Maresme | 1 |
| Forêt de Sant Vicenç de Montalt (11) ⚠️ | Sant Vicenç de Montalt › Maresme | 1 |
| Forêt de Llinars del Vallès (90) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Forêt de Vallgorguina (11) ⚠️ | Vallgorguina › Vallès Oriental | 1 |
| Forêt de Vallgorguina (12) ⚠️ | Vallgorguina › Vallès Oriental | 1 |
| Forêt de Vallgorguina (13) ⚠️ | Vilalba Sasserra › Vallès Oriental | 1 |
| Forêt de Llinars del Vallès (91) ⚠️ | Llinars del Vallès › Vallès Oriental | 1 |
| Forêt de Vallgorguina (21) ⚠️ | Vallgorguina › Vallès Oriental | 1 |
| Forêt de Sant Celoni (33) ⚠️ | Sant Celoni › Vallès Oriental | 1 |
| Forêt de Fogars de la Selva (36) ⚠️ | Fogars de la Selva › la Selva (Barcelone) | 1 |
| Forêt de Tordera (117) ⚠️ | Tordera › Maresme | 1 |
| Forêt de Sant Celoni (52) ⚠️ | Sant Celoni › Vallès Oriental | 1 |
| Forêt de Sant Celoni (53) ⚠️ | Sant Celoni › Vallès Oriental | 1 |
| Forêt de Gualba (7) ⚠️ | Gualba › Vallès Oriental | 1 |
| Forêt de Sant Celoni (59) ⚠️ | Sant Celoni › Vallès Oriental | 1 |
| Forêt de Sant Celoni (62) ⚠️ | Sant Celoni › Vallès Oriental | 1 |
| Forêt de Gualba (13) ⚠️ | Gualba › Vallès Oriental | 1 |
| Forêt de Gualba (25) ⚠️ | Gualba › Vallès Oriental | 1 |
| Forêt de Gualba (26) ⚠️ | Gualba › Vallès Oriental | 1 |
| Forêt de Sant Celoni (64) ⚠️ | Gualba › Vallès Oriental | 1 |
| Forêt de Sant Celoni (65) ⚠️ | Sant Celoni › Vallès Oriental | 1 |
| Forêt de Gualba (29) ⚠️ | Gualba › Vallès Oriental | 1 |
| Forêt de Sant Celoni (78) ⚠️ | Sant Celoni › Vallès Oriental | 1 |
| Forêt de Gironella (20) ⚠️ | Gironella › Berguedà | 1 |
| Forêt de Gironella (24) ⚠️ | Gironella › Berguedà | 1 |
| Forêt de Gironella (26) ⚠️ | Gironella › Berguedà | 1 |
| Forêt de Gironella (30) ⚠️ | Gironella › Berguedà | 1 |
| Forêt de Gironella (34) ⚠️ | Gironella › Berguedà | 1 |
| Forêt de Gironella (36) ⚠️ | Gironella › Berguedà | 1 |
| Forêt de Casserres (37) ⚠️ | Casserres › Berguedà | 1 |
| Forêt de Sallent (111) ⚠️ | Sallent › Bages | 1 |
| Forêt de Sant Fruitós de Bages (34) ⚠️ | Sant Fruitós de Bages › Bages | 1 |
| Forêt de Sant Fruitós de Bages (35) ⚠️ | Sant Fruitós de Bages › Bages | 1 |
| Forêt de Sallent (124) ⚠️ | Sallent › Bages | 1 |
| Forêt de Sallent (127) ⚠️ | Sallent › Bages | 1 |
| Forêt de Santpedor (16) ⚠️ | Santpedor › Bages | 1 |
| Forêt de Santpedor (21) ⚠️ | Santpedor › Bages | 1 |
| Forêt de Santpedor (22) ⚠️ | Santpedor › Bages | 1 |
| Forêt de Santpedor (27) ⚠️ | Santpedor › Bages | 1 |
| Forêt de Santpedor (34) ⚠️ | Santpedor › Bages | 1 |
| Forêt de Santpedor (39) ⚠️ | Santpedor › Bages | 1 |
| Forêt de Santpedor (40) ⚠️ | Santpedor › Bages | 1 |
| Forêt de Santpedor (42) ⚠️ | Santpedor › Bages | 1 |
| Forêt de Santpedor (44) ⚠️ | Santpedor › Bages | 1 |
| Forêt de Sant Joan de Vilatorrada (64) ⚠️ | Sant Joan de Vilatorrada › Bages | 1 |
| Forêt de Santpedor (53) ⚠️ | Santpedor › Bages | 1 |
| Forêt de Callús (16) ⚠️ | Callús › Bages | 1 |
| Forêt de Callús (22) ⚠️ | Callús › Bages | 1 |
| Forêt de Castellnou de Bages (60) ⚠️ | Castellnou de Bages › Bages | 1 |
| Forêt de Castellnou de Bages (62) ⚠️ | Castellnou de Bages › Bages | 1 |
| Forêt de Sant Feliu de Codines (18) ⚠️ | Sant Feliu de Codines › Vallès Oriental | 1 |
| Forêt de Castellnou de Bages (69) ⚠️ | Castellnou de Bages › Bages | 1 |
| Forêt de Sallent (132) ⚠️ | Sallent › Bages | 1 |
| Bois de Sant Feliu de Codines (2) ⚠️ | Sant Feliu de Codines › Vallès Oriental | 1 |
| Forêt de Castellnou de Bages (72) ⚠️ | Castellnou de Bages › Bages | 1 |
| Forêt de Castellnou de Bages (73) ⚠️ | Castellnou de Bages › Bages | 1 |
| Forêt de Castellnou de Bages (78) ⚠️ | Castellnou de Bages › Bages | 1 |
| Forêt de Castellnou de Bages (92) ⚠️ | Castellnou de Bages › Bages | 1 |
| Forêt de Callús (23) ⚠️ | Callús › Bages | 1 |
| Forêt de Callús (27) ⚠️ | Callús › Bages | 1 |
| Forêt de Callús (30) ⚠️ | Callús › Bages | 1 |
| Forêt de Súria (41) ⚠️ | Súria › Bages | 1 |
| Forêt de Callús (39) ⚠️ | Callús › Bages | 1 |
| Forêt de Callús (43) ⚠️ | Callús › Bages | 1 |
| Forêt de Callús (44) ⚠️ | Callús › Bages | 1 |
| Forêt de Callús (46) ⚠️ | Callús › Bages | 1 |
| Forêt de Súria (46) ⚠️ | Súria › Bages | 1 |
| Forêt de Súria (47) ⚠️ | Súria › Bages | 1 |
| Forêt de Callús (47) ⚠️ | Callús › Bages | 1 |
| Forêt de Súria (51) ⚠️ | Súria › Bages | 1 |
| Forêt de Súria (52) ⚠️ | Súria › Bages | 1 |
| Forêt de Súria (53) ⚠️ | Súria › Bages | 1 |
| Forêt de Súria (54) ⚠️ | Súria › Bages | 1 |
| Forêt de Santpedor (77) ⚠️ | Santpedor › Bages | 1 |
| Forêt de Sant Joan de Vilatorrada (77) ⚠️ | Sant Joan de Vilatorrada › Bages | 1 |
| Forêt de Callús (54) ⚠️ | Callús › Bages | 1 |
| Forêt de Callús (58) ⚠️ | Callús › Bages | 1 |
| Forêt de Callús (60) ⚠️ | Súria › Bages | 1 |
| Forêt de Sant Joan de Vilatorrada (91) ⚠️ | Sant Joan de Vilatorrada › Bages | 1 |
| Forêt de Sant Joan de Vilatorrada (92) ⚠️ | Sant Joan de Vilatorrada › Bages | 1 |
| Forêt de Sant Joan de Vilatorrada (93) ⚠️ | Sant Joan de Vilatorrada › Bages | 1 |
| Forêt de Sant Joan de Vilatorrada (94) ⚠️ | Sant Joan de Vilatorrada › Bages | 1 |
| Forêt de Sant Joan de Vilatorrada (101) ⚠️ | Sant Joan de Vilatorrada › Bages | 1 |
| Forêt de Fonollosa (133) ⚠️ | Fonollosa › Bages | 1 |
| Forêt de Fonollosa (135) ⚠️ | Fonollosa › Bages | 1 |
| Forêt de Fonollosa (137) ⚠️ | Fonollosa › Bages | 1 |
| Forêt de Fonollosa (138) ⚠️ | Fonollosa › Bages | 1 |
| Forêt de Fonollosa (142) ⚠️ | Fonollosa › Bages | 1 |
| Forêt de Sant Mateu de Bages (122) ⚠️ | Sant Mateu de Bages › Bages | 1 |
| Forêt de Sant Mateu de Bages (129) ⚠️ | Sant Mateu de Bages › Bages | 1 |
| Forêt de Sant Mateu de Bages (130) ⚠️ | Sant Mateu de Bages › Bages | 1 |
| Forêt de Sant Mateu de Bages (143) ⚠️ | Sant Mateu de Bages › Bages | 1 |
| Forêt de Sant Mateu de Bages (147) ⚠️ | Sant Mateu de Bages › Bages | 1 |
| Forêt de Fonollosa (157) ⚠️ | Fonollosa › Bages | 1 |
| Forêt de Fonollosa (159) ⚠️ | Fonollosa › Bages | 1 |
| Forêt de Fonollosa (162) ⚠️ | Fonollosa › Bages | 1 |
| Forêt de Fonollosa (164) ⚠️ | Fonollosa › Bages | 1 |
| Forêt de Fonollosa (166) ⚠️ | Fonollosa › Bages | 1 |
| Forêt de Fonollosa (170) ⚠️ | Fonollosa › Bages | 1 |
| Forêt de Sant Mateu de Bages (159) ⚠️ | Sant Mateu de Bages › Bages | 1 |
| Forêt de Sant Julià de Vilatorta (6) ⚠️ | Sant Julià de Vilatorta › Osona (Barcelone) | 1 |
| Forêt de Sant Sadurní d'Osormort (30) ⚠️ | Sant Sadurní d'Osormort › Osona (Barcelone) | 1 |
| Forêt de Sant Sadurní d'Osormort (32) ⚠️ | Sant Sadurní d'Osormort › Osona (Barcelone) | 1 |
| Forêt de Sant Sadurní d'Osormort (47) ⚠️ | Sant Sadurní d'Osormort › Osona (Barcelone) | 1 |
| Forêt de Tavèrnoles (12) ⚠️ | Tavèrnoles › Osona (Barcelone) | 1 |
| Forêt de Folgueroles (7) ⚠️ | Folgueroles › Osona (Barcelone) | 1 |
| Forêt de Taradell (25) ⚠️ | Taradell › Osona (Barcelone) | 1 |
| Forêt de Taradell (27) ⚠️ | Taradell › Osona (Barcelone) | 1 |
| Forêt de Taradell (29) ⚠️ | Taradell › Osona (Barcelone) | 1 |
| Forêt de Sant Julià de Vilatorta (18) ⚠️ | Sant Julià de Vilatorta › Osona (Barcelone) | 1 |
| Forêt de Sant Julià de Vilatorta (20) ⚠️ | Sant Julià de Vilatorta › Osona (Barcelone) | 1 |
| Forêt de Taradell (46) ⚠️ | Taradell › Osona (Barcelone) | 1 |
| Forêt de Taradell (49) ⚠️ | Taradell › Osona (Barcelone) | 1 |
| Forêt de Santa Eugènia de Berga (7) ⚠️ | Santa Eugènia de Berga › Osona (Barcelone) | 1 |
| Forêt de Santa Maria d'Oló (82) ⚠️ | Santa Maria d'Oló › Moianès | 1 |
| Forêt de Santa Maria d'Oló (83) ⚠️ | Santa Maria d'Oló › Moianès | 1 |
| Forêt de Santa Maria d'Oló (85) ⚠️ | Santa Maria d'Oló › Moianès | 1 |
| Forêt de els Hostalets de Pierola (31) ⚠️ | els Hostalets de Pierola › Anoia | 1 |
| Forêt de Cervelló (22) ⚠️ | Sant Vicenç dels Horts › Baix Llobregat | 1 |
| Forêt de Torelló (5) ⚠️ | Torelló › Osona (Barcelone) | 1 |
| Forêt de les Masies de Voltregà (16) ⚠️ | les Masies de Voltregà › Osona (Barcelone) | 1 |
| Jardins de Can Travé ⚠️ | Cubelles › Garraf | 1 |
| Forêt de Castellbell i el Vilar (74) ⚠️ | Castellbell i el Vilar › Bages | 1 |
| Forêt de Torelló (6) ⚠️ | Torelló › Osona (Barcelone) | 1 |
| Forêt de les Masies de Voltregà (18) ⚠️ | les Masies de Voltregà › Osona (Barcelone) | 1 |
| Forêt de les Masies de Voltregà (20) ⚠️ | les Masies de Voltregà › Osona (Barcelone) | 1 |
| Forêt de Arenys de Mar (11) ⚠️ | Arenys de Mar › Maresme | 1 |
| Parc del Turó de Cerdanyola ⚠️ | Mataró › Maresme | 1 |
| Forêt de Argentona (8) ⚠️ | Argentona › Maresme | 1 |
| Forêt de Argentona (9) ⚠️ | Argentona › Maresme | 1 |
| Forêt de Argentona (12) ⚠️ | Argentona › Maresme | 1 |
| Forêt de Cabrera de Mar (8) ⚠️ | Cabrera de Mar › Maresme | 1 |
| Bois de Gurb (38) ⚠️ | Gurb › Osona (Barcelone) | 1 |
| Forêt de Gurb (29) ⚠️ | Gurb › Osona (Barcelone) | 1 |
| Forêt de Vic (51) ⚠️ | Vic › Osona (Barcelone) | 1 |
| Forêt de Vic (57) ⚠️ | Vic › Osona (Barcelone) | 1 |
| Forêt de Vic (59) ⚠️ | Vic › Osona (Barcelone) | 1 |
| Forêt de Vic (65) ⚠️ | Vic › Osona (Barcelone) | 1 |
| Forêt de Vic (67) ⚠️ | Vic › Osona (Barcelone) | 1 |
| Forêt de Torelló (10) ⚠️ | Torelló › Osona (Barcelone) | 1 |
| Forêt de Torelló (13) ⚠️ | Torelló › Osona (Barcelone) | 1 |
| Forêt de Torelló (16) ⚠️ | Torelló › Osona (Barcelone) | 1 |
| La Bardissa ⚠️ | Torelló › Osona (Barcelone) | 1 |
| Forêt de Gavà (81) ⚠️ | Gavà › Baix Llobregat | 1 |
| Parc de Colita ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Castellbell i el Vilar (75) ⚠️ | Castellbell i el Vilar › Bages | 1 |
| Forêt de Castellbell i el Vilar (76) ⚠️ | Castellbell i el Vilar › Bages | 1 |
| Forêt de Gurb (31) ⚠️ | Gurb › Osona (Barcelone) | 1 |
| Forêt de Gurb (35) ⚠️ | Gurb › Osona (Barcelone) | 1 |
| Forêt de Gurb (36) ⚠️ | Gurb › Osona (Barcelone) | 1 |
| Forêt de Gurb (37) ⚠️ | Gurb › Osona (Barcelone) | 1 |
| Forêt de Gurb (42) ⚠️ | Gurb › Osona (Barcelone) | 1 |
| Forêt de Vic (69) ⚠️ | Vic › Osona (Barcelone) | 1 |
| Forêt de Gurb (48) ⚠️ | Gurb › Osona (Barcelone) | 1 |
| Forêt de Gurb (49) ⚠️ | Gurb › Osona (Barcelone) | 1 |
| Bois de Vic (4) ⚠️ | Vic › Osona (Barcelone) | 1 |
| Forêt de Vic (74) ⚠️ | Vic › Osona (Barcelone) | 1 |
| Forêt de Vic (75) ⚠️ | Vic › Osona (Barcelone) | 1 |
| Forêt de Vic (80) ⚠️ | Gurb › Osona (Barcelone) | 1 |
| Forêt de Gurb (59) ⚠️ | Gurb › Osona (Barcelone) | 1 |
| Parc d'Europa (6) ⚠️ | Sant Boi de Llobregat › Baix Llobregat | 1 |
| Forêt de Montmeló (4) ⚠️ | Montmeló › Vallès Oriental | 1 |
| Forêt de Granollers (10) ⚠️ | Granollers › Vallès Oriental | 1 |
| Forêt de Granollers (11) ⚠️ | Granollers › Vallès Oriental | 1 |
| Forêt de Parets del Vallès (3) ⚠️ | Parets del Vallès › Vallès Oriental | 1 |
| Forêt de Granollers (14) ⚠️ | Granollers › Vallès Oriental | 1 |
| Forêt de Granollers (16) ⚠️ | Granollers › Vallès Oriental | 1 |
| Forêt de Parets del Vallès (5) ⚠️ | Parets del Vallès › Vallès Oriental | 1 |
| Forêt de Montmeló (7) ⚠️ | Montmeló › Vallès Oriental | 1 |
| Forêt de Montmeló (11) ⚠️ | Montmeló › Vallès Oriental | 1 |
| Forêt de Montornès del Vallès (23) ⚠️ | Montornès del Vallès › Vallès Oriental | 1 |
| Jardins de Can Parrella ⚠️ | Torelló › Osona (Barcelone) | 1 |
| Forêt de Sant Quintí de Mediona (18) ⚠️ | Sant Quintí de Mediona › Alt Penedès | 1 |
| Forêt de Sant Pere de Ribes (114) ⚠️ | Sant Pere de Ribes › Garraf | 1 |
| Forêt de Sentmenat (14) ⚠️ | Sentmenat › Vallès Occidental | 1 |
| Forêt de Sentmenat (15) ⚠️ | Sentmenat › Vallès Occidental | 1 |
| Forêt de Sentmenat (16) ⚠️ | Sentmenat › Vallès Occidental | 1 |
| Forêt de Caldes de Montbui (12) ⚠️ | Caldes de Montbui › Vallès Oriental | 1 |
| Forêt de Caldes de Montbui (13) ⚠️ | Caldes de Montbui › Vallès Oriental | 1 |
| Forêt de Caldes de Montbui (17) ⚠️ | Caldes de Montbui › Vallès Oriental | 1 |
| Forêt de Caldes de Montbui (18) ⚠️ | Caldes de Montbui › Vallès Oriental | 1 |
| Forêt de Caldes de Montbui (22) ⚠️ | Caldes de Montbui › Vallès Oriental | 1 |
| Forêt de Palau-solità i Plegamans (15) ⚠️ | Palau-solità i Plegamans › Vallès Occidental | 1 |
| Forêt de Palau-solità i Plegamans (16) ⚠️ | Palau-solità i Plegamans › Vallès Occidental | 1 |
| Parc de Palau-solità i Plegamans (11) ⚠️ | Palau-solità i Plegamans › Vallès Occidental | 1 |
| Parc de Santa Perpètua de Mogoda (15) ⚠️ | Santa Perpètua de Mogoda › Vallès Occidental | 1 |
| Parc de Santa Perpètua de Mogoda (17) ⚠️ | Santa Perpètua de Mogoda › Vallès Occidental | 1 |
| Forêt de Lliçà d'Amunt (21) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 1 |
| Forêt de Lliçà d'Amunt (26) ⚠️ | Lliçà d'Amunt › Vallès Oriental | 1 |
| Forêt de Lliçà de Vall (9) ⚠️ | Lliçà de Vall › Vallès Oriental | 1 |
| Forêt de Lliçà de Vall (10) ⚠️ | Lliçà de Vall › Vallès Oriental | 1 |
| Forêt de Lliçà de Vall (11) ⚠️ | Lliçà de Vall › Vallès Oriental | 1 |
| Parc de Lliçà de Vall (12) ⚠️ | Lliçà de Vall › Vallès Oriental | 1 |
| Forêt de Lluçà (91) ⚠️ | Lluçà › Lluçanès | 1 |
| Forêt de Prats de Lluçanès (28) ⚠️ | Prats de Lluçanès › Lluçanès | 1 |
| Forêt de Olost (13) ⚠️ | Olost › Lluçanès | 1 |
| Forêt de Olost (15) ⚠️ | Olost › Lluçanès | 1 |
| Forêt de Oristà (169) ⚠️ | Oristà › Lluçanès | 1 |
| Forêt de Oristà (173) ⚠️ | Oristà › Lluçanès | 1 |
| Jardins del Camp de Sarrià ⚠️ | Barcelona › Barcelonès | 1 |
| Jardins d'Elisard Sala ⚠️ | Barcelona › Barcelonès | 1 |
| Forêt de Calders (74) ⚠️ | Calders › Moianès | 1 |
| Forêt de Calders (78) ⚠️ | Calders › Moianès | 1 |
| Forêt de Monistrol de Calders (44) ⚠️ | Monistrol de Calders › Moianès | 1 |
| Forêt de Monistrol de Calders (46) ⚠️ | Monistrol de Calders › Moianès | 1 |
| Forêt de Castellterçol (83) ⚠️ | Castellterçol › Moianès | 1 |
| Forêt de Calders (83) ⚠️ | Calders › Moianès | 1 |
| Forêt de Calders (85) ⚠️ | Calders › Moianès | 1 |
| Forêt de Moià (72) ⚠️ | Moià › Moianès | 1 |
| Forêt de Calders (86) ⚠️ | Calders › Moianès | 1 |
| Forêt de Moià (74) ⚠️ | Moià › Moianès | 1 |
| Forêt de Moià (76) ⚠️ | Moià › Moianès | 1 |
| Forêt de Sant Fruitós de Bages (43) ⚠️ | Sant Fruitós de Bages › Bages | 1 |
| Forêt de Sant Fruitós de Bages (47) ⚠️ | Sant Fruitós de Bages › Bages | 1 |
| Forêt de Sant Fruitós de Bages (49) ⚠️ | Sant Fruitós de Bages › Bages | 1 |
| Forêt de Sant Fruitós de Bages (50) ⚠️ | Sant Fruitós de Bages › Bages | 1 |
| Forêt de Sant Fruitós de Bages (56) ⚠️ | Sant Fruitós de Bages › Bages | 1 |
| Forêt de Sant Fruitós de Bages (57) ⚠️ | Sant Fruitós de Bages › Bages | 1 |
| Forêt de Cardona (121) ⚠️ | Cardona › Bages | 1 |
| Bosc del Reguer ⚠️ | Sant Fruitós de Bages › Bages | 1 |
| Forêt de Sant Fruitós de Bages (62) ⚠️ | Sant Fruitós de Bages › Bages | 1 |
| Forêt de Sant Fruitós de Bages (64) ⚠️ | Santpedor › Bages | 1 |
| Forêt de Sant Fruitós de Bages (70) ⚠️ | Sant Fruitós de Bages › Bages | 1 |
| Forêt de Sant Fruitós de Bages (80) ⚠️ | Sant Fruitós de Bages › Bages | 1 |
| Forêt de Sant Fruitós de Bages (83) ⚠️ | Sant Fruitós de Bages › Bages | 1 |
| Parc de Can Font (2) ⚠️ | Manresa › Bages | 1 |
| Forêt de Manresa (156) ⚠️ | Manresa › Bages | 1 |
| Forêt de Manresa (163) ⚠️ | Manresa › Bages | 1 |
| Forêt de Sant Fruitós de Bages (88) ⚠️ | Sant Fruitós de Bages › Bages | 1 |
| Parc de Sant Fruitós de Bages (29) ⚠️ | Sant Fruitós de Bages › Bages | 1 |
| Forêt de Talamanca (37) ⚠️ | Talamanca › Bages | 1 |
| Forêt de Talamanca (38) ⚠️ | Talamanca › Bages | 1 |
| Forêt de Talamanca (39) ⚠️ | Talamanca › Bages | 1 |
| Forêt de el Pont de Vilomara i Rocafort (41) ⚠️ | el Pont de Vilomara i Rocafort › Bages | 1 |
| Forêt de el Pont de Vilomara i Rocafort (42) ⚠️ | el Pont de Vilomara i Rocafort › Bages | 1 |
| Forêt de el Pont de Vilomara i Rocafort (43) ⚠️ | el Pont de Vilomara i Rocafort › Bages | 1 |
| Forêt de Talamanca (44) ⚠️ | Talamanca › Bages | 1 |
| Forêt de el Pont de Vilomara i Rocafort (48) ⚠️ | el Pont de Vilomara i Rocafort › Bages | 1 |
| Forêt de el Pont de Vilomara i Rocafort (52) ⚠️ | el Pont de Vilomara i Rocafort › Bages | 1 |
| Forêt de el Pont de Vilomara i Rocafort (53) ⚠️ | el Pont de Vilomara i Rocafort › Bages | 1 |
| Forêt de Manresa (169) ⚠️ | Manresa › Bages | 1 |
| Forêt de Manresa (172) ⚠️ | Manresa › Bages | 1 |
| Forêt de Manresa (173) ⚠️ | Manresa › Bages | 1 |
| Forêt de Manresa (176) ⚠️ | Castellgalí › Bages | 1 |
| Forêt de Sant Salvador de Guardiola (122) ⚠️ | Sant Salvador de Guardiola › Bages | 1 |
| Forêt de Castellgalí (74) ⚠️ | Castellgalí › Bages | 1 |
| Forêt de Castellgalí (76) ⚠️ | Castellgalí › Bages | 1 |
| Forêt de Castellgalí (78) ⚠️ | Castellgalí › Bages | 1 |
| Forêt de Santpedor (91) ⚠️ | Santpedor › Bages | 1 |
| Forêt de Viladecavalls (21) ⚠️ | Viladecavalls › Vallès Occidental | 1 |
| Forêt de Terrassa (95) ⚠️ | Terrassa › Vallès Occidental | 1 |
| Forêt de Terrassa (97) ⚠️ | Terrassa › Vallès Occidental | 1 |
| Parc de la Ruta Mediterrànea ⚠️ | Sant Andreu de la Barca › Baix Llobregat | 1 |
| Forêt de la Pobla de Lillet (67) ⚠️ | la Pobla de Lillet › Berguedà | 1 |

9 166 parc(s) plus petits qu'une cellule ne sont pas listés : la carte les dessine, mais ils n'offrent aucune cellule.

⚠️ 16507 parc(s) hors de la fenêtre 10–125 cellules (16223 trop petit(s), 284 trop grand(s)) : affichés sur la carte, mais ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| airport | 403 |
| prison | 33 |
| military | 16 |
| **Total déclaré** | **452** |
| dont dans une zone de ce territoire | 448 |

Le jeu de données couvre plus large que le territoire — il est produit à une échelle supérieure. Seules les cellules tombant dans une zone d'ici pèsent sur un pourcentage.

### Zones concernées

| Zone | Cellules exclues |
|---|---:|
| el Prat de Llobregat | 350 |
| Sabadell | 27 |
| Sant Esteve Sesrovires | 15 |
| Sant Boi de Llobregat | 13 |
| la Roca del Vallès | 9 |
| Òdena | 7 |
| Moià | 7 |
| Sant Joan de Vilatorrada | 5 |
| Avinyonet del Penedès | 4 |
| el Bruc | 4 |
| Viladecans | 3 |
| Palau-solità i Plegamans | 3 |
| Granollers | 1 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
