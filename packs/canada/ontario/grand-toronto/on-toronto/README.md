# Toronto

Pack `on-toronto` · version 1.0.1 · grille 200 m · Canada › Ontario › Grand Toronto

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 30 303 |
| dont restreintes (aéroport, militaire, prison) | 75 |
| dont sans chemin (aucune voie à moins de 60 m) | 44 |
| dont en forêt, sans chemin non plus | 106 |
| dont traversées par un cours d'eau, sans chemin non plus | 8 |
| Cellules retirées par le masque d'eau | 1 590 |
| Villes | 1 |
| Arrondissements et quartiers | 25 |
| Îles | 0 |
| Parcs | 1 743 |

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

## Villes (1)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Sans chemin | Parcs |
|---|---:|---:|---:|---:|---:|---:|---:|
| Toronto | 31 891 | 1 590 | 30 301 | 75 | **30 226** | 44 (0 %) | 1738 |

## Arrondissements et quartiers (25)

| Zone | Ville | Brut | Eau | Sans eau | Restr. | Comptées | Sans chemin | Parcs |
|---|---|---:|---:|---:|---:|---:|---:|---:|
| Scarborough—Rouge Park | toronto | 2 694 | 129 | 2 565 | 0 | **2 565** | 4 (0 %) | 69 |
| Etobicoke North | toronto | 2 324 | 24 | 2 300 | 15 | **2 285** | 15 (1 %) | 66 |
| Etobicoke—Lakeshore | toronto | 2 098 | 187 | 1 911 | 5 | **1 906** | 2 (0 %) | 112 |
| Etobicoke Centre | toronto | 1 781 | 14 | 1 767 | 0 | **1 767** | 1 (0 %) | 83 |
| York Centre | toronto | 1 691 | 13 | 1 678 | 14 | **1 664** | 7 (0 %) | 63 |
| Humber River—Black Creek | toronto | 1 474 | 7 | 1 467 | 0 | **1 467** |  | 55 |
| Scarborough North | toronto | 1 463 | 1 | 1 462 | 0 | **1 462** | 5 (0 %) | 42 |
| Don Valley West | toronto | 1 452 | 3 | 1 449 | 0 | **1 449** |  | 74 |
| Scarborough Southwest | toronto | 1 465 | 115 | 1 350 | 0 | **1 350** |  | 75 |
| Scarborough Centre | toronto | 1 351 | 3 | 1 348 | 0 | **1 348** |  | 49 |
| Scarborough—Guildwood | toronto | 1 287 | 33 | 1 254 | 0 | **1 254** | 1 (0 %) | 58 |
| York South—Weston | toronto | 1 203 | 17 | 1 186 | 0 | **1 186** |  | 72 |
| Don Valley North | toronto | 1 174 | 4 | 1 170 | 0 | **1 170** |  | 90 |
| Don Valley East | toronto | 1 100 | 14 | 1 086 | 0 | **1 086** |  | 54 |
| Eglinton—Lawrence | toronto | 1 086 | 1 | 1 085 | 0 | **1 085** |  | 73 |
| Scarborough—Agincourt | toronto | 1 029 | 5 | 1 024 | 0 | **1 024** | 1 (0 %) | 43 |
| Toronto—Danforth | toronto | 1 305 | 303 | 1 002 | 0 | **1 002** | 8 (1 %) | 74 |
| Willowdale | toronto | 948 | 0 | 948 | 0 | **948** |  | 80 |
| Beaches—East York | toronto | 887 | 84 | 803 | 0 | **803** |  | 52 |
| Parkdale—High Park | toronto | 769 | 61 | 708 | 0 | **708** |  | 77 |
| University—Rosedale | toronto | 652 | 1 | 651 | 0 | **651** |  | 102 |
| Toronto—St. Paul's | toronto | 626 | 1 | 625 | 0 | **625** |  | 67 |
| Spadina—Fort York | toronto | 1 175 | 569 | 606 | 41 | **565** |  | 92 |
| Davenport | toronto | 578 | 0 | 578 | 0 | **578** |  | 55 |
| Toronto Centre | toronto | 282 | 1 | 281 | 0 | **281** |  | 61 |

## Parcs (1743)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Rouge National Urban Park ⚠️ | Toronto › Scarborough—Rouge Park | 868 |
| West Humber Parkland | Toronto › Etobicoke North | 110 |
| Morningside Park | Toronto › Scarborough—Guildwood | 110 |
| Sunnybrook Park | Toronto › Don Valley West | 95 |
| Tommy Thompson Park | Toronto › Toronto—Danforth | 91 |
| Parc de Toronto (104) | Toronto › Don Valley East | 88 |
| High Park | Toronto › Parkdale—High Park | 70 |
| Toronto Island Park | Toronto › Spadina—Fort York | 67 |
| Highland Creek Ravine | Toronto › Scarborough—Rouge Park | 64 |
| Taylor Creek Park | Toronto › Beaches—East York | 61 |
| G. Ross Lord Park | Toronto › York Centre | 60 |
| Centennial Park | Toronto › Etobicoke Centre | 60 |
| Earl Bales Park | Toronto › York Centre | 60 |
| E. T. Seton Park | Toronto › Don Valley West | 58 |
| East Don Parkland (2) | Toronto › Don Valley North | 58 |
| Humber Arboretum | Toronto › Etobicoke North | 56 |
| Parc de Toronto (127) | Toronto › Scarborough—Rouge Park | 51 |
| Rowntree Mills Park | Toronto › Humber River—Black Creek | 47 |
| Downsview Dells Park | Toronto › York Centre | 38 |
| East Point Park | Toronto › Scarborough—Rouge Park | 36 |
| Beare Hill Park | Toronto › Scarborough—Rouge Park | 32 |
| Downsview Park | Toronto › York Centre | 32 |
| Bluffer's Park | Toronto › Scarborough Southwest | 32 |
| Derrydowns Park | Toronto › Humber River—Black Creek | 29 |
| Parc de Toronto (268) | Toronto › York Centre | 27 |
| Parc de Toronto (18) | Toronto › York South—Weston | 26 |
| Colonel Samuel Smith Park | Toronto › Etobicoke—Lakeshore | 24 |
| West Deane Park | Toronto › Etobicoke Centre | 24 |
| Parc de Toronto (19) | Toronto › Etobicoke Centre | 23 |
| Guild Park and Gardens | Toronto › Scarborough—Guildwood | 22 |
| Parc de Toronto (5) | Toronto › University—Rosedale | 21 |
| Moatfield Farm Park | Toronto › Don Valley East | 20 |
| Warden Woods Park | Toronto › Scarborough Southwest | 19 |
| Hinder Area | Toronto › Willowdale | 19 |
| Parc de Toronto (37) | Toronto › Scarborough Centre | 19 |
| Pine Point Park | Toronto › Etobicoke North | 18 |
| Parc de Toronto (33) | Toronto › Don Valley West | 18 |
| Highland Creek | Toronto › Scarborough—Guildwood | 16 |
| L'Amoreaux Sports Complex | Toronto › Scarborough—Agincourt | 15 |
| Cherry Beach Clarke Beach Park | Toronto › Toronto—Danforth | 15 |
| Todmorden Mills Park | Toronto › Toronto—Danforth | 14 |
| Don Valley Brick Works Park | Toronto › University—Rosedale | 14 |
| Milliken Park | Toronto › Scarborough North | 14 |
| Woodbine Beach Park | Toronto › Beaches—East York | 14 |
| Étienne Brûlé Park | Toronto › Parkdale—High Park | 14 |
| King's Mill Park | Toronto › Etobicoke—Lakeshore | 14 |
| Humber Marshes | Toronto › Parkdale—High Park | 14 |
| Thomson Memorial Park | Toronto › Scarborough Centre | 13 |
| South Marine Park | Toronto › Scarborough—Guildwood | 13 |
| Marie Curtis Park | Toronto › Etobicoke—Lakeshore | 13 |
| Edwards Gardens | Toronto › Don Valley West | 13 |
| Biidaasige Park | Toronto › Toronto—Danforth | 13 |
| Home Smith Park | Toronto › Etobicoke—Lakeshore | 13 |
| Cedarvale Park | Toronto › Toronto—St. Paul's | 13 |
| David A. Balfour Park | Toronto › University—Rosedale | 12 |
| Humber Bay Park East | Toronto › Etobicoke—Lakeshore | 11 |
| L'Amoreaux Park | Toronto › Scarborough—Agincourt | 10 |
| Parc de Toronto (54) | Toronto › Scarborough—Guildwood | 10 |
| Etobicoke Valley Park | Toronto › Etobicoke—Lakeshore | 10 |
| South Humber Park | Toronto › Etobicoke—Lakeshore | 10 |
| Black Creek Parkland (2) | Toronto › Humber River—Black Creek | 10 |
| Summerlea Park | Toronto › Etobicoke North | 10 |
| Claireville Conservation Area (2) | Toronto › Etobicoke North | 10 |
| Riverdale Park East ⚠️ | Toronto › Toronto—Danforth | 9 |
| Leslie Greenbelt ⚠️ | Toronto › Don Valley North | 9 |
| Mallaby Park ⚠️ | Toronto › Etobicoke North | 9 |
| Moore Park Ravine ⚠️ | Toronto › University—Rosedale | 9 |
| Brookbanks Park (4) ⚠️ | Toronto › Don Valley East | 9 |
| Parc de Toronto (4) ⚠️ | Toronto › University—Rosedale | 8 |
| Westview Greenbelt ⚠️ | Toronto › York South—Weston | 8 |
| Fergy Brown Park ⚠️ | Toronto › York South—Weston | 8 |
| Eglinton Flats (2) ⚠️ | Toronto › York South—Weston | 8 |
| Sherwood Park ⚠️ | Toronto › Don Valley West | 8 |
| Ellesmere Greenspace ⚠️ | Toronto › Scarborough—Guildwood | 8 |
| Adams Park ⚠️ | Toronto › Scarborough—Rouge Park | 8 |
| Ashbridges Bay Park ⚠️ | Toronto › Beaches—East York | 8 |
| Birkdale Ravine ⚠️ | Toronto › Scarborough Centre | 8 |
| Cudia Park ⚠️ | Toronto › Scarborough Southwest | 8 |
| Cedarbrook Park ⚠️ | Toronto › Scarborough—Guildwood | 7 |
| Woodbine Park ⚠️ | Toronto › Beaches—East York | 7 |
| Eglinton Flats ⚠️ | Toronto › York South—Weston | 7 |
| Chalkfarm Park ⚠️ | Toronto › Humber River—Black Creek | 7 |
| Parc de Toronto (21) ⚠️ | Toronto › York Centre | 7 |
| North Park ⚠️ | Toronto › York South—Weston | 7 |
| Humber Bay Park West ⚠️ | Toronto › Etobicoke—Lakeshore | 7 |
| Bob Hunter Greenspace ⚠️ | Toronto › Scarborough—Rouge Park | 7 |
| Thackeray Park ⚠️ | Toronto › Etobicoke North | 7 |
| North York Civic Soccer Fields ⚠️ | Toronto › York Centre | 7 |
| Trinity Bellwoods Park ⚠️ | Toronto › Spadina—Fort York | 7 |
| Tom Riley Park ⚠️ | Toronto › Etobicoke—Lakeshore | 7 |
| Lower Don Parklands ⚠️ | Toronto › Toronto—Danforth | 6 |
| East Don Parkland ⚠️ | Toronto › Don Valley North | 6 |
| Parc de Toronto (7) ⚠️ | Toronto › Scarborough North | 6 |
| Beaches Park ⚠️ | Toronto › Beaches—East York | 6 |
| Earlscourt Park ⚠️ | Toronto › Davenport | 6 |
| Smythe Park ⚠️ | Toronto › York South—Weston | 6 |
| Parc de Toronto (23) ⚠️ | Toronto › York South—Weston | 6 |
| Palace Pier Park ⚠️ | Toronto › Etobicoke—Lakeshore | 6 |
| Richview Park ⚠️ | Toronto › Etobicoke Centre | 6 |
| Alex Marchetti Park ⚠️ | Toronto › Etobicoke Centre | 6 |
| Amesbury Park ⚠️ | Toronto › York South—Weston | 6 |
| Birchmount Park ⚠️ | Toronto › Scarborough Southwest | 6 |
| Lambton Park (2) ⚠️ | Toronto › Parkdale—High Park | 6 |
| Christie Pits Park ⚠️ | Toronto › University—Rosedale | 5 |
| Sir Winston Churchill Park ⚠️ | Toronto › Toronto—St. Paul's | 5 |
| Riverdale Park West ⚠️ | Toronto › Toronto Centre | 5 |
| Stan Wadlow Park ⚠️ | Toronto › Beaches—East York | 5 |
| Fairglen Park ⚠️ | Toronto › Scarborough—Agincourt | 5 |
| Eglinton Park ⚠️ | Toronto › Eglinton—Lawrence | 5 |
| Parc de Toronto (14) ⚠️ | Toronto › Scarborough—Rouge Park | 5 |
| Caledonia Park ⚠️ | Toronto › Eglinton—Lawrence | 5 |
| Parc de Toronto (29) ⚠️ | Toronto › York South—Weston | 5 |
| Sir Casimir Gzowski Park ⚠️ | Toronto › Parkdale—High Park | 5 |
| Huntsmill Park ⚠️ | Toronto › Scarborough—Agincourt | 5 |
| Alexander Muir Memorial Gardens ⚠️ | Toronto › Don Valley West | 5 |
| Confederation Park ⚠️ | Toronto › Scarborough—Guildwood | 5 |
| Hampshire Heights Park ⚠️ | Toronto › Etobicoke Centre | 5 |
| Coronation Park (2) ⚠️ | Toronto › Spadina—Fort York | 5 |
| Ashtonbee Reservoir Park ⚠️ | Toronto › Scarborough Centre | 5 |
| Baycrest Park ⚠️ | Toronto › Eglinton—Lawrence | 5 |
| Brookbanks Park (3) ⚠️ | Toronto › Don Valley East | 5 |
| Parc de Toronto (291) ⚠️ | Toronto › Etobicoke—Lakeshore | 5 |
| Ward's Island Park ⚠️ | Toronto › Spadina—Fort York | 5 |
| Coronation Park (3) ⚠️ | Toronto › York South—Weston | 5 |
| Humber Gate Park ⚠️ | Toronto › Etobicoke North | 5 |
| Ramsden Park ⚠️ | Toronto › University—Rosedale | 4 |
| Dufferin Grove Park ⚠️ | Toronto › Davenport | 4 |
| Withrow Park ⚠️ | Toronto › Toronto—Danforth | 4 |
| Kew Gardens ⚠️ | Toronto › Beaches—East York | 4 |
| Cummer Park ⚠️ | Toronto › Don Valley North | 4 |
| Queens GreenBelt Park ⚠️ | Toronto › York South—Weston | 4 |
| Cruickshank Park ⚠️ | Toronto › Etobicoke Centre | 4 |
| Parc de Toronto (20) ⚠️ | Toronto › York Centre | 4 |
| Parc de Toronto (24) ⚠️ | Toronto › York South—Weston | 4 |
| Parc de Toronto (30) ⚠️ | Toronto › Etobicoke North | 4 |
| Flemingdon Park (2) ⚠️ | Toronto › Don Valley East | 4 |
| Parc de Toronto (32) ⚠️ | Toronto › Don Valley West | 4 |
| Remberto Navia Sports Field ⚠️ | Toronto › Humber River—Black Creek | 4 |
| Rennie Park ⚠️ | Toronto › Parkdale—High Park | 4 |
| Marilyn Bell Park ⚠️ | Toronto › Parkdale—High Park | 4 |
| Neilson Park ⚠️ | Toronto › Scarborough—Rouge Park | 4 |
| Littles Park ⚠️ | Toronto › Scarborough—Rouge Park | 4 |
| Neilson Park (2) ⚠️ | Toronto › Etobicoke Centre | 4 |
| Parc de Toronto (49) ⚠️ | Toronto › Scarborough—Rouge Park | 4 |
| Major Abbas Ali Park ⚠️ | Toronto › Scarborough North | 4 |
| Duncairn Park ⚠️ | Toronto › Don Valley East | 4 |
| Parc de Toronto (121) ⚠️ | Toronto › Scarborough Centre | 4 |
| White Haven Park ⚠️ | Toronto › Scarborough North | 4 |
| Parkway Forest Park ⚠️ | Toronto › Don Valley North | 4 |
| Howard Talbot Park ⚠️ | Toronto › Don Valley West | 4 |
| Black Creek Parkland ⚠️ | Toronto › Humber River—Black Creek | 4 |
| Black Creek Park West ⚠️ | Toronto › York South—Weston | 4 |
| Broadlands Park ⚠️ | Toronto › Don Valley East | 4 |
| McCowan District Park ⚠️ | Toronto › Scarborough Southwest | 4 |
| Humber Sheppard Park ⚠️ | Toronto › Humber River—Black Creek | 4 |
| Toronto Azzurri Youth Sport Village ⚠️ | Toronto › York Centre | 4 |
| Curran Hall Ravine ⚠️ | Toronto › Scarborough—Guildwood | 3 |
| Wanita Park ⚠️ | Toronto › Scarborough—Rouge Park | 3 |
| Charlottetown Park ⚠️ | Toronto › Scarborough—Rouge Park | 3 |
| Hullmar Park ⚠️ | Toronto › Humber River—Black Creek | 3 |
| Elm Park ⚠️ | Toronto › Humber River—Black Creek | 3 |
| Wishing Well Park ⚠️ | Toronto › Scarborough—Agincourt | 3 |
| Greenwood Park ⚠️ | Toronto › Toronto—Danforth | 3 |
| Clairlea Park ⚠️ | Toronto › Scarborough Southwest | 3 |
| Chorley Park ⚠️ | Toronto › University—Rosedale | 3 |
| Linus Park ⚠️ | Toronto › Don Valley North | 3 |
| St. Clair Ravine ⚠️ | Toronto › Scarborough Southwest | 3 |
| Rockford Park ⚠️ | Toronto › York Centre | 3 |
| Elie Wiesel Park ⚠️ | Toronto › York Centre | 3 |
| Finch-Islington Park ⚠️ | Toronto › Etobicoke North | 3 |
| Roding Park ⚠️ | Toronto › York Centre | 3 |
| Fountainhead Park ⚠️ | Toronto › Humber River—Black Creek | 3 |
| Parc de Toronto (25) ⚠️ | Toronto › York South—Weston | 3 |
| Echo Valley Park ⚠️ | Toronto › Etobicoke Centre | 3 |
| L'Amoreaux Hydro ⚠️ | Toronto › Scarborough—Agincourt | 3 |
| Flemingdon Park ⚠️ | Toronto › Don Valley East | 3 |
| York Mills Valley Park ⚠️ | Toronto › Don Valley West | 3 |
| Parc de Toronto (35) ⚠️ | Toronto › Etobicoke—Lakeshore | 3 |
| Iroquois Park ⚠️ | Toronto › Scarborough North | 3 |
| Edgeley Park ⚠️ | Toronto › Humber River—Black Creek | 3 |
| Blythwood Ravine Park ⚠️ | Toronto › Don Valley West | 3 |
| Parc de Toronto (52) ⚠️ | Toronto › Humber River—Black Creek | 3 |
| Jack Goodlad Park ⚠️ | Toronto › Scarborough Centre | 3 |
| Parc de Toronto (66) ⚠️ | Toronto › Scarborough Centre | 3 |
| North Bendale Park ⚠️ | Toronto › Scarborough—Guildwood | 3 |
| Parc de Toronto (85) ⚠️ | Toronto › Scarborough North | 3 |
| Parc de Toronto (108) ⚠️ | Toronto › Willowdale | 3 |
| Pelmo Park ⚠️ | Toronto › York South—Weston | 3 |
| Masseygrove Park ⚠️ | Toronto › Etobicoke North | 3 |
| Parc de Toronto (133) ⚠️ | Toronto › Etobicoke—Lakeshore | 3 |
| Smithfield Park ⚠️ | Toronto › Etobicoke North | 3 |
| Parc de Toronto (154) ⚠️ | Toronto › Scarborough—Rouge Park | 3 |
| Ron Watson Park ⚠️ | Toronto › Scarborough—Agincourt | 3 |
| St. Lucie Park ⚠️ | Toronto › Humber River—Black Creek | 3 |
| Bloordale Park (2) ⚠️ | Toronto › Etobicoke Centre | 3 |
| Brimley Woods ⚠️ | Toronto › Scarborough North | 3 |
| Broadacres Park ⚠️ | Toronto › Etobicoke Centre | 3 |
| Brookbanks Park (2) ⚠️ | Toronto › Don Valley East | 3 |
| Buttonwood Park ⚠️ | Toronto › Etobicoke Centre | 3 |
| Sunnyside Park ⚠️ | Toronto › Parkdale—High Park | 3 |
| Woodsworth Park ⚠️ | Toronto › Scarborough—Guildwood | 3 |
| Parc de Toronto (258) ⚠️ | Toronto › Humber River—Black Creek | 3 |
| Memorial Park - North York ⚠️ | Toronto › Eglinton—Lawrence | 3 |
| North Keelesdale Park ⚠️ | Toronto › York South—Weston | 3 |
| The Elms Park ⚠️ | Toronto › Etobicoke North | 3 |
| James Gardens ⚠️ | Toronto › Etobicoke Centre | 3 |
| Wexford Park ⚠️ | Toronto › Scarborough Centre | 2 |
| Vermont Square Park ⚠️ | Toronto › University—Rosedale | 2 |
| Megan Park ⚠️ | Toronto › Scarborough—Rouge Park | 2 |
| Parc de Toronto (2) ⚠️ | Toronto › Willowdale | 2 |
| Harry W. Arthurs Common ⚠️ | Toronto › Humber River—Black Creek | 2 |
| Nordheimer Ravine ⚠️ | Toronto › Toronto—St. Paul's | 2 |
| Willowdale Park ⚠️ | Toronto › Willowdale | 2 |
| Sorauren Avenue Park ⚠️ | Toronto › Parkdale—High Park | 2 |
| Ashbridge's Bay Sports Club ⚠️ | Toronto › Toronto—Danforth | 2 |
| Dieppe Park ⚠️ | Toronto › Toronto—Danforth | 2 |
| Dentonia Park ⚠️ | Toronto › Beaches—East York | 2 |
| Inglewood Heights Park ⚠️ | Toronto › Scarborough—Agincourt | 2 |
| Collingsbrook Parkette ⚠️ | Toronto › Scarborough—Agincourt | 2 |
| Grey Abbey Park ⚠️ | Toronto › Scarborough—Rouge Park | 2 |
| Rosedale Park ⚠️ | Toronto › University—Rosedale | 2 |
| Terry Fox Park ⚠️ | Toronto › Scarborough—Agincourt | 2 |
| Cresthaven Park ⚠️ | Toronto › Don Valley North | 2 |
| Skymark Park ⚠️ | Toronto › Don Valley North | 2 |
| McDairmid Woods Park ⚠️ | Toronto › Scarborough North | 2 |
| Mossgrove Park ⚠️ | Toronto › Don Valley West | 2 |
| Hobart Park ⚠️ | Toronto › Don Valley North | 2 |
| Monarch Park ⚠️ | Toronto › Toronto—Danforth | 2 |
| Felstead Park ⚠️ | Toronto › Toronto—Danforth | 2 |
| Wigmore Park ⚠️ | Toronto › Don Valley East | 2 |
| Flagstaff Park ⚠️ | Toronto › Etobicoke North | 2 |
| Scarden Park ⚠️ | Toronto › Scarborough—Agincourt | 2 |
| Parc de Toronto (16) ⚠️ | Toronto › Scarborough Centre | 2 |
| Fairbank Memorial Park ⚠️ | Toronto › Toronto—St. Paul's | 2 |
| Irving W Chapley Park ⚠️ | Toronto › York Centre | 2 |
| Hendon Park ⚠️ | Toronto › Willowdale | 2 |
| Edithvale Park ⚠️ | Toronto › Willowdale | 2 |
| Sunnydale Acres Park ⚠️ | Toronto › Etobicoke North | 2 |
| Parc de Toronto (22) ⚠️ | Toronto › Scarborough Centre | 2 |
| Densgrove Park ⚠️ | Toronto › Scarborough—Guildwood | 2 |
| Parc de Toronto (27) ⚠️ | Toronto › York South—Weston | 2 |
| Wadsworth Park ⚠️ | Toronto › Davenport | 2 |
| Cataraqui Park ⚠️ | Toronto › Scarborough Southwest | 2 |
| Parc de Toronto (31) ⚠️ | Toronto › Don Valley West | 2 |
| Ethennonnhawahstihnen' Park ⚠️ | Toronto › Don Valley North | 2 |
| Parc de Toronto (36) ⚠️ | Toronto › Etobicoke—Lakeshore | 2 |
| East Mall Park ⚠️ | Toronto › Etobicoke Centre | 2 |
| Connorvale Park ⚠️ | Toronto › Etobicoke—Lakeshore | 2 |
| Cedargrove Park ⚠️ | Toronto › Scarborough—Guildwood | 2 |
| St. Andrew’s Park ⚠️ | Toronto › Don Valley West | 2 |
| St. Andrew’s Park (2) ⚠️ | Toronto › Don Valley West | 2 |
| Laburnham Park ⚠️ | Toronto › Etobicoke—Lakeshore | 2 |
| Clarinda Park ⚠️ | Toronto › Don Valley North | 2 |
| Fundy Bay Park ⚠️ | Toronto › Scarborough—Agincourt | 2 |
| Parc de Toronto (46) ⚠️ | Toronto › Scarborough—Rouge Park | 2 |
| Harvest Moon Park ⚠️ | Toronto › Scarborough—Rouge Park | 2 |
| Driftwood Park ⚠️ | Toronto › Humber River—Black Creek | 2 |
| Parc de Toronto (48) ⚠️ | Toronto › Scarborough—Rouge Park | 2 |
| Chatsworth Ravine ⚠️ | Toronto › Eglinton—Lawrence | 2 |
| Elmcrest Park ⚠️ | Toronto › Etobicoke Centre | 2 |
| Sentinel Park ⚠️ | Toronto › Humber River—Black Creek | 2 |
| Parc de Toronto (53) ⚠️ | Toronto › York Centre | 2 |
| Seven Oaks Park ⚠️ | Toronto › Scarborough—Guildwood | 2 |
| Lissom Park ⚠️ | Toronto › Willowdale | 2 |
| Parc de Toronto (56) ⚠️ | Toronto › Etobicoke North | 2 |
| Lindy Lou Park ⚠️ | Toronto › Humber River—Black Creek | 2 |
| Millwood Park ⚠️ | Toronto › Etobicoke Centre | 2 |
| Viewmount Park ⚠️ | Toronto › Eglinton—Lawrence | 2 |
| Guild Park ⚠️ | Toronto › Scarborough—Guildwood | 2 |
| Highland Creek Community Park ⚠️ | Toronto › Scarborough—Rouge Park | 2 |
| Hupfield Park ⚠️ | Toronto › Scarborough—Rouge Park | 2 |
| Scarborough Village Park ⚠️ | Toronto › Scarborough—Guildwood | 2 |
| Laurentide Park ⚠️ | Toronto › Don Valley East | 2 |
| Dr. Daniel Hill Park ⚠️ | Toronto › Don Valley East | 2 |
| Parc de Toronto (67) ⚠️ | Toronto › Beaches—East York | 2 |
| Terraview Park ⚠️ | Toronto › Scarborough Centre | 2 |
| Parc de Toronto (78) ⚠️ | Toronto › Humber River—Black Creek | 2 |
| Spenvalley Park ⚠️ | Toronto › Humber River—Black Creek | 2 |
| Silver Creek Park ⚠️ | Toronto › Etobicoke Centre | 2 |
| Queensway Park ⚠️ | Toronto › Etobicoke—Lakeshore | 2 |
| Grand Avenue Park ⚠️ | Toronto › Etobicoke—Lakeshore | 2 |
| Manchester Park ⚠️ | Toronto › Etobicoke—Lakeshore | 2 |
| Eringate Park ⚠️ | Toronto › Etobicoke Centre | 2 |
| Martingrove Gardens Park ⚠️ | Toronto › Etobicoke Centre | 2 |
| Maidavale Park ⚠️ | Toronto › Scarborough Centre | 2 |
| Cynthia Lai Park ⚠️ | Toronto › Scarborough North | 2 |
| Duncairn Park (2) ⚠️ | Toronto › Don Valley East | 2 |
| Heather Heights Park ⚠️ | Toronto › Scarborough—Guildwood | 2 |
| Dallington Park ⚠️ | Toronto › Don Valley North | 2 |
| Lescon Park ⚠️ | Toronto › Don Valley North | 2 |
| Muirlands Park ⚠️ | Toronto › Scarborough North | 2 |
| Princess Anne Park ⚠️ | Toronto › Etobicoke Centre | 2 |
| Cedar Ridge Park ⚠️ | Toronto › Scarborough—Guildwood | 2 |
| Highview Park ⚠️ | Toronto › Scarborough Southwest | 2 |
| Scarborough Heights Park ⚠️ | Toronto › Scarborough Southwest | 2 |
| Seneca Hill Park ⚠️ | Toronto › Don Valley North | 2 |
| Parc de Toronto (93) ⚠️ | Toronto › Scarborough—Rouge Park | 2 |
| Warden Park ⚠️ | Toronto › Scarborough—Agincourt | 2 |
| Parc de Toronto (97) ⚠️ | Toronto › York Centre | 2 |
| Parc de Toronto (98) ⚠️ | Toronto › Scarborough North | 2 |
| Highland Heights Park ⚠️ | Toronto › Scarborough—Agincourt | 2 |
| Princess Margaret Park ⚠️ | Toronto › Etobicoke Centre | 2 |
| Gihon Spring Park ⚠️ | Toronto › Etobicoke North | 2 |
| Parc de Toronto (102) ⚠️ | Toronto › Scarborough—Rouge Park | 2 |
| Graydon Hall Park ⚠️ | Toronto › Don Valley East | 2 |
| Parc de Toronto (105) ⚠️ | Toronto › Don Valley East | 2 |
| Richmond Park ⚠️ | Toronto › Scarborough North | 2 |
| Blue Ridge Park ⚠️ | Toronto › Don Valley North | 2 |
| Pinto Park ⚠️ | Toronto › Don Valley North | 2 |
| Stephen Leacock Park ⚠️ | Toronto › Scarborough—Agincourt | 2 |
| Wickson Trail Park ⚠️ | Toronto › Scarborough—Rouge Park | 2 |
| Woburn Park (4) ⚠️ | Toronto › Scarborough—Guildwood | 2 |
| Horseley Hill Park ⚠️ | Toronto › Scarborough North | 2 |
| Ourland Park ⚠️ | Toronto › Etobicoke—Lakeshore | 2 |
| Humber Valley Park ⚠️ | Toronto › Etobicoke Centre | 2 |
| Parc de Toronto (132) ⚠️ | Toronto › Humber River—Black Creek | 2 |
| Woodborough Park ⚠️ | Toronto › York South—Weston | 2 |
| Mason Road Park ⚠️ | Toronto › Scarborough Southwest | 2 |
| Parc de Toronto (143) ⚠️ | Toronto › Etobicoke North | 2 |
| Havenbrook Park ⚠️ | Toronto › Don Valley North | 2 |
| Goulding Park ⚠️ | Toronto › Willowdale | 2 |
| Parc de Toronto (152) ⚠️ | Toronto › Scarborough Centre | 2 |
| Glen Long Park ⚠️ | Toronto › Eglinton—Lawrence | 2 |
| Marie Baldwin Park ⚠️ | Toronto › York South—Weston | 2 |
| Ravenscrest Park ⚠️ | Toronto › Etobicoke Centre | 2 |
| Algonquin Island Park ⚠️ | Toronto › Spadina—Fort York | 2 |
| Guildwood Village Park ⚠️ | Toronto › Scarborough—Guildwood | 2 |
| Melody Park ⚠️ | Toronto › Etobicoke North | 2 |
| Roundhouse Park ⚠️ | Toronto › Spadina—Fort York | 2 |
| Westgrove Park ⚠️ | Toronto › Etobicoke North | 2 |
| Don Russell Memorial Park ⚠️ | Toronto › Etobicoke—Lakeshore | 2 |
| North Mimico Valley Park ⚠️ | Toronto › Etobicoke North | 2 |
| Cherry Beach Sports Fields ⚠️ | Toronto › Toronto—Danforth | 2 |
| Agincourt Park ⚠️ | Toronto › Scarborough North | 2 |
| Oriole Park (2) ⚠️ | Toronto › Toronto—St. Paul's | 2 |
| Moorevale Park ⚠️ | Toronto › University—Rosedale | 2 |
| Albion Gardens Park ⚠️ | Toronto › Etobicoke North | 2 |
| Alexmuir Park ⚠️ | Toronto › Scarborough North | 2 |
| Allan Gardens ⚠️ | Toronto › Toronto Centre | 2 |
| Balmy Beach Park ⚠️ | Toronto › Beaches—East York | 2 |
| Bayview Village Park ⚠️ | Toronto › Don Valley North | 2 |
| Beaumonde Heights Park (2) ⚠️ | Toronto › Etobicoke North | 2 |
| Beechgrove Ravine ⚠️ | Toronto › Scarborough—Rouge Park | 2 |
| Bellbury Park (2) ⚠️ | Toronto › Don Valley North | 2 |
| Berner Trail Park ⚠️ | Toronto › Scarborough North | 2 |
| Berry Road Park ⚠️ | Toronto › Etobicoke—Lakeshore | 2 |
| Bert Robinson Park ⚠️ | Toronto › Davenport | 2 |
| Bestview Park ⚠️ | Toronto › Don Valley North | 2 |
| Bickford Park ⚠️ | Toronto › University—Rosedale | 2 |
| Birch Park ⚠️ | Toronto › Etobicoke—Lakeshore | 2 |
| Birunthan Park ⚠️ | Toronto › Scarborough—Rouge Park | 2 |
| Black Creek Site East ⚠️ | Toronto › York South—Weston | 2 |
| Bloordale Park ⚠️ | Toronto › Etobicoke Centre | 2 |
| Bond Park ⚠️ | Toronto › Don Valley East | 2 |
| Briarcrest Park ⚠️ | Toronto › Etobicoke Centre | 2 |
| Bridletowne Park ⚠️ | Toronto › Scarborough—Agincourt | 2 |
| Bridlewood Park (2) ⚠️ | Toronto › Scarborough—Agincourt | 2 |
| Brookbanks Park ⚠️ | Toronto › Don Valley East | 2 |
| Byng Park ⚠️ | Toronto › Scarborough Southwest | 2 |
| Corktown Common ⚠️ | Toronto › Toronto Centre | 2 |
| Claireville Conservation Area ⚠️ | Toronto › Etobicoke North | 2 |
| Seneca Hill Outdoor Field ⚠️ | Toronto › Don Valley East | 2 |
| Trillium Park ⚠️ | Toronto › Spadina—Fort York | 2 |
| Corvette Park ⚠️ | Toronto › Scarborough Southwest | 2 |
| Parc de Toronto (266) ⚠️ | Toronto › Humber River—Black Creek | 2 |
| Parc de Toronto (275) ⚠️ | Toronto › Scarborough—Guildwood | 2 |
| Parc de Toronto (277) ⚠️ | Toronto › Scarborough—Guildwood | 2 |
| Parc de Toronto (287) ⚠️ | Toronto › Scarborough—Rouge Park | 2 |
| Thistletown Park ⚠️ | Toronto › Etobicoke North | 2 |
| Botany Hill Park ⚠️ | Toronto › Scarborough—Guildwood | 2 |
| Lawrence Park Ravine ⚠️ | Toronto › Don Valley West | 2 |
| Pinetree Park ⚠️ | Toronto › Scarborough North | 2 |
| Kay Gardner Beltline Park ⚠️ | Toronto › Toronto—St. Paul's | 2 |
| Parc de Toronto (345) ⚠️ | Toronto › University—Rosedale | 2 |
| Grange Park ⚠️ | Toronto › Spadina—Fort York | 1 |
| Clarence Square ⚠️ | Toronto › Spadina—Fort York | 1 |
| St. Alban's Square ⚠️ | Toronto › University—Rosedale | 1 |
| Jesse Ketchum Park ⚠️ | Toronto › University—Rosedale | 1 |
| Dovercourt Park ⚠️ | Toronto › Davenport | 1 |
| Wenderly Park ⚠️ | Toronto › Eglinton—Lawrence | 1 |
| June Rowlands Park ⚠️ | Toronto › Toronto—St. Paul's | 1 |
| St. Margaret's Parkette ⚠️ | Toronto › Scarborough—Guildwood | 1 |
| Huron & Washington Parkette ⚠️ | Toronto › University—Rosedale | 1 |
| Marian Engel Park ⚠️ | Toronto › Toronto—St. Paul's | 1 |
| Hillcrest Park ⚠️ | Toronto › Toronto—St. Paul's | 1 |
| Parkview Park ⚠️ | Toronto › Willowdale | 1 |
| Glendora Park ⚠️ | Toronto › Willowdale | 1 |
| Silverview Park ⚠️ | Toronto › Willowdale | 1 |
| St. Andrew's Playground ⚠️ | Toronto › Spadina—Fort York | 1 |
| Poplar Plains Parkette ⚠️ | Toronto › Toronto—St. Paul's | 1 |
| Pricefield Road Playground ⚠️ | Toronto › University—Rosedale | 1 |
| Graham Park ⚠️ | Toronto › Toronto—St. Paul's | 1 |
| Little Norway Park ⚠️ | Toronto › Spadina—Fort York | 1 |
| Moss Park ⚠️ | Toronto › Toronto Centre | 1 |
| St. James Park ⚠️ | Toronto › Toronto Centre | 1 |
| MacGregor Playground ⚠️ | Toronto › Davenport | 1 |
| McCormick Park ⚠️ | Toronto › Davenport | 1 |
| Robert Hicks Park ⚠️ | Toronto › York Centre | 1 |
| Hunters Glen Park ⚠️ | Toronto › Scarborough Centre | 1 |
| Erwin Krickhahn Park ⚠️ | Toronto › Davenport | 1 |
| Campbell Avenue Park ⚠️ | Toronto › Davenport | 1 |
| Wellesley Park ⚠️ | Toronto › Toronto Centre | 1 |
| East Toronto Athletic Field ⚠️ | Toronto › Beaches—East York | 1 |
| East Lynn Park ⚠️ | Toronto › Beaches—East York | 1 |
| Kitchener Park ⚠️ | Toronto › Scarborough Southwest | 1 |
| Canada Square ⚠️ | Toronto › Spadina—Fort York | 1 |
| HTO Park West ⚠️ | Toronto › Spadina—Fort York | 1 |
| Westlake Park ⚠️ | Toronto › York South—Weston | 1 |
| Clydesdale Park ⚠️ | Toronto › Don Valley North | 1 |
| R.V. Burgess Park ⚠️ | Toronto › Don Valley West | 1 |
| Coleman Park ⚠️ | Toronto › Beaches—East York | 1 |
| Wanless Park ⚠️ | Toronto › Don Valley West | 1 |
| Topham Park ⚠️ | Toronto › Beaches—East York | 1 |
| Jay Robinson Park ⚠️ | Toronto › Don Valley West | 1 |
| Jaye Robinson Park ⚠️ | Toronto › Don Valley West | 1 |
| Wallace Emerson Park ⚠️ | Toronto › Davenport | 1 |
| Oakridge Park ⚠️ | Toronto › Scarborough Southwest | 1 |
| Prairie Drive Park ⚠️ | Toronto › Scarborough Southwest | 1 |
| Mike Bela Park ⚠️ | Toronto › Don Valley West | 1 |
| Parc de Toronto (6) ⚠️ | Toronto › Don Valley West | 1 |
| Rippleton Park ⚠️ | Toronto › Don Valley West | 1 |
| Kirkwood Park ⚠️ | Toronto › Don Valley West | 1 |
| Oriole Park ⚠️ | Toronto › Don Valley North | 1 |
| Shaughnessy Public School Park ⚠️ | Toronto › Don Valley North | 1 |
| Village of Yorkville Park ⚠️ | Toronto › University—Rosedale | 1 |
| Willesden Park ⚠️ | Toronto › Don Valley North | 1 |
| Pineway Park ⚠️ | Toronto › Don Valley North | 1 |
| Stafford Park ⚠️ | Toronto › Willowdale | 1 |
| Maple Leaf Park ⚠️ | Toronto › York South—Weston | 1 |
| Gwendolen Park ⚠️ | Toronto › Willowdale | 1 |
| Cheltenham Park ⚠️ | Toronto › Don Valley West | 1 |
| Oakvale Green ⚠️ | Toronto › Toronto—Danforth | 1 |
| Sandy Bruce Park ⚠️ | Toronto › Don Valley West | 1 |
| Lambton - Kingsway Park ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Pantry Park ⚠️ | Toronto › Beaches—East York | 1 |
| Phin Park ⚠️ | Toronto › Toronto—Danforth | 1 |
| Phil Givens Park ⚠️ | Toronto › Eglinton—Lawrence | 1 |
| Prince Charles Park ⚠️ | Toronto › Eglinton—Lawrence | 1 |
| Sweeney Drive ⚠️ | Toronto › Don Valley East | 1 |
| Parc de Toronto (11) ⚠️ | Toronto › York Centre | 1 |
| Vradenberg Park ⚠️ | Toronto › Scarborough—Agincourt | 1 |
| Snowhill Park ⚠️ | Toronto › Scarborough North | 1 |
| Dorset Park ⚠️ | Toronto › Scarborough Centre | 1 |
| Parc de Toronto (15) ⚠️ | Toronto › Scarborough Centre | 1 |
| Parc de Toronto (17) ⚠️ | Toronto › Scarborough Centre | 1 |
| Turpin Avenue Park ⚠️ | Toronto › Etobicoke North | 1 |
| Westway Park ⚠️ | Toronto › Etobicoke Centre | 1 |
| Seeley Greenbelt ⚠️ | Toronto › York Centre | 1 |
| Heathrow Park ⚠️ | Toronto › York Centre | 1 |
| North Humber Park ⚠️ | Toronto › Etobicoke North | 1 |
| Lusted Park ⚠️ | Toronto › Scarborough—Guildwood | 1 |
| Harding Park ⚠️ | Toronto › York South—Weston | 1 |
| Gulliver Park ⚠️ | Toronto › York South—Weston | 1 |
| Parc de Toronto (26) ⚠️ | Toronto › York South—Weston | 1 |
| Parc de Toronto (28) ⚠️ | Toronto › York South—Weston | 1 |
| Holley Park ⚠️ | Toronto › York South—Weston | 1 |
| Windwood Park ⚠️ | Toronto › Etobicoke North | 1 |
| Chandos Park North ⚠️ | Toronto › Davenport | 1 |
| Lloyd Manor Park ⚠️ | Toronto › Etobicoke Centre | 1 |
| Neil McLellan Park ⚠️ | Toronto › Parkdale—High Park | 1 |
| Dunlop Park ⚠️ | Toronto › Scarborough Southwest | 1 |
| Rean Park ⚠️ | Toronto › Don Valley North | 1 |
| Parc de Toronto (34) ⚠️ | Toronto › Willowdale | 1 |
| Maywood Tot Lot ⚠️ | Toronto › Scarborough Southwest | 1 |
| Heathercrest Park ⚠️ | Toronto › Etobicoke Centre | 1 |
| Joyce Parkette ⚠️ | Toronto › Eglinton—Lawrence | 1 |
| Capri Park ⚠️ | Toronto › Etobicoke Centre | 1 |
| Silverhill Park ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Cloverdale Park ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Greenfield Park ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Queensland Park ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Rotary Peace Park ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Lochleven Park ⚠️ | Toronto › Scarborough Southwest | 1 |
| Wellesworth Park ⚠️ | Toronto › Etobicoke Centre | 1 |
| Dennis Flynn Park ⚠️ | Toronto › Etobicoke Centre | 1 |
| Douglas Park ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Port Union Village Common ⚠️ | Toronto › Scarborough—Rouge Park | 1 |
| Parc de Toronto (41) ⚠️ | Toronto › Don Valley West | 1 |
| Parc de Toronto (42) ⚠️ | Toronto › Don Valley West | 1 |
| Lakeshore Boulevard Parklands ⚠️ | Toronto › Parkdale—High Park | 1 |
| Leaside Park ⚠️ | Toronto › Don Valley West | 1 |
| Hawksbury Park ⚠️ | Toronto › Don Valley North | 1 |
| Robertson Parkette ⚠️ | Toronto › Toronto—Danforth | 1 |
| Stratford Park ⚠️ | Toronto › Don Valley West | 1 |
| Parc de Toronto (45) ⚠️ | Toronto › Scarborough—Agincourt | 1 |
| Port Royal Park ⚠️ | Toronto › Scarborough North | 1 |
| Lytton Park ⚠️ | Toronto › Eglinton—Lawrence | 1 |
| St. Clair Gardens Parkette ⚠️ | Toronto › Davenport | 1 |
| Jonathan Ashbridge Park ⚠️ | Toronto › Toronto—Danforth | 1 |
| Severn Creek Park ⚠️ | Toronto › University—Rosedale | 1 |
| Inukshuk Park ⚠️ | Toronto › Spadina—Fort York | 1 |
| Maple Claire Park ⚠️ | Toronto › York South—Weston | 1 |
| Harwood Park ⚠️ | Toronto › York South—Weston | 1 |
| Harbour Square Park ⚠️ | Toronto › Spadina—Fort York | 1 |
| Warner Park ⚠️ | Toronto › Don Valley East | 1 |
| Gord and Irene Risk Park ⚠️ | Toronto › Humber River—Black Creek | 1 |
| Prince of Wales Park ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Norris Crescent Parkette ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Dunlace Park ⚠️ | Toronto › Don Valley West | 1 |
| Former Baycrest Public School grounds ⚠️ | Toronto › Eglinton—Lawrence | 1 |
| Sandown Park ⚠️ | Toronto › Scarborough Southwest | 1 |
| Muir Park ⚠️ | Toronto › Scarborough Southwest | 1 |
| Centennial Park (2) ⚠️ | Toronto › Scarborough—Rouge Park | 1 |
| Shawn Blu Rose Park ⚠️ | Toronto › Scarborough—Rouge Park | 1 |
| Parc de Toronto (63) ⚠️ | Toronto › Don Valley West | 1 |
| Ranchdale Park ⚠️ | Toronto › Don Valley East | 1 |
| Natal Park ⚠️ | Toronto › Scarborough Southwest | 1 |
| Eglinton Ravine Park ⚠️ | Toronto › Scarborough Southwest | 1 |
| Farlinger Ravine ⚠️ | Toronto › Scarborough Southwest | 1 |
| Dalrymple Park ⚠️ | Toronto › York South—Weston | 1 |
| Runnymede Park ⚠️ | Toronto › York South—Weston | 1 |
| Elmbrook Park ⚠️ | Toronto › Etobicoke Centre | 1 |
| Lynedock Park ⚠️ | Toronto › Don Valley East | 1 |
| Rowena Park ⚠️ | Toronto › Don Valley East | 1 |
| Parc de Toronto (68) ⚠️ | Toronto › Scarborough Centre | 1 |
| Parc de Toronto (72) ⚠️ | Toronto › Willowdale | 1 |
| Murison Park ⚠️ | Toronto › Scarborough—Rouge Park | 1 |
| Lillian Park ⚠️ | Toronto › Willowdale | 1 |
| Lord Roberts Woods ⚠️ | Toronto › Scarborough Centre | 1 |
| Shawnee Park ⚠️ | Toronto › Don Valley North | 1 |
| Giltspur Park ⚠️ | Toronto › York Centre | 1 |
| Parc de Toronto (80) ⚠️ | Toronto › York Centre | 1 |
| Eden Valley Park ⚠️ | Toronto › Etobicoke Centre | 1 |
| Green Meadows Park ⚠️ | Toronto › Etobicoke Centre | 1 |
| Woburn Park (3) ⚠️ | Toronto › Eglinton—Lawrence | 1 |
| Talwood Park ⚠️ | Toronto › Don Valley East | 1 |
| Ben Nobleman Park ⚠️ | Toronto › Toronto—St. Paul's | 1 |
| Heather Heights Woods ⚠️ | Toronto › Scarborough—Guildwood | 1 |
| Strathburn Park ⚠️ | Toronto › Humber River—Black Creek | 1 |
| Loring-Wyle Parkette ⚠️ | Toronto › University—Rosedale | 1 |
| Parc de Toronto (86) ⚠️ | Toronto › Scarborough North | 1 |
| Secor Memorial Park ⚠️ | Toronto › Scarborough—Guildwood | 1 |
| Plowshare Park ⚠️ | Toronto › Etobicoke North | 1 |
| Harrison Properties ⚠️ | Toronto › Scarborough Southwest | 1 |
| Lynndale Park ⚠️ | Toronto › Scarborough Southwest | 1 |
| McNicoll Park ⚠️ | Toronto › Don Valley North | 1 |
| Parc de Toronto (91) ⚠️ | Toronto › Don Valley West | 1 |
| Parc de Toronto (92) ⚠️ | Toronto › Scarborough—Rouge Park | 1 |
| Collingwood Park ⚠️ | Toronto › Scarborough—Agincourt | 1 |
| Parc de Toronto (94) ⚠️ | Toronto › Scarborough—Agincourt | 1 |
| Parc de Toronto (95) ⚠️ | Toronto › Scarborough—Agincourt | 1 |
| Muirhead Park ⚠️ | Toronto › Don Valley North | 1 |
| Parc de Toronto (96) ⚠️ | Toronto › Scarborough—Guildwood | 1 |
| West Birkdale Park ⚠️ | Toronto › Scarborough Centre | 1 |
| Kempton Howard Park ⚠️ | Toronto › Toronto—Danforth | 1 |
| Moccasin Trail Park ⚠️ | Toronto › Don Valley East | 1 |
| Ernie Lustig - Rainbow Park ⚠️ | Toronto › York South—Weston | 1 |
| Timberbank Park ⚠️ | Toronto › Scarborough—Agincourt | 1 |
| Treverton Park ⚠️ | Toronto › Scarborough Centre | 1 |
| Walter Saunders Memorial Park ⚠️ | Toronto › Eglinton—Lawrence | 1 |
| Parc de Toronto (100) ⚠️ | Toronto › Etobicoke North | 1 |
| Parc de Toronto (101) ⚠️ | Toronto › Scarborough—Agincourt | 1 |
| Parc de Toronto (103) ⚠️ | Toronto › Etobicoke Centre | 1 |
| Duncan Creek Park ⚠️ | Toronto › Don Valley North | 1 |
| Silvio Collela Park ⚠️ | Toronto › Humber River—Black Creek | 1 |
| Plunkett park ⚠️ | Toronto › Humber River—Black Creek | 1 |
| Godstone Park ⚠️ | Toronto › Don Valley North | 1 |
| Hideaway Park ⚠️ | Toronto › Toronto—Danforth | 1 |
| Van Horne Park ⚠️ | Toronto › Don Valley North | 1 |
| Parc de Toronto (119) ⚠️ | Toronto › York Centre | 1 |
| Parc de Toronto (120) ⚠️ | Toronto › Eglinton—Lawrence | 1 |
| Parc de Toronto (122) ⚠️ | Toronto › Scarborough Southwest | 1 |
| Fir Valley Woods Park ⚠️ | Toronto › Scarborough Southwest | 1 |
| McCleary Park ⚠️ | Toronto › Toronto—Danforth | 1 |
| Morse Street Playground ⚠️ | Toronto › Toronto—Danforth | 1 |
| Churchill Heights Park ⚠️ | Toronto › Scarborough—Guildwood | 1 |
| Parc de Toronto (123) ⚠️ | Toronto › Scarborough—Guildwood | 1 |
| John Tabor Park ⚠️ | Toronto › Scarborough—Rouge Park | 1 |
| Tall Pines Park ⚠️ | Toronto › Scarborough—Rouge Park | 1 |
| Parc de Toronto (125) ⚠️ | Toronto › Scarborough—Rouge Park | 1 |
| Dean Park ⚠️ | Toronto › Scarborough—Rouge Park | 1 |
| Parc de Toronto (126) ⚠️ | Toronto › Scarborough—Rouge Park | 1 |
| Indian Line Park ⚠️ | Toronto › Etobicoke North | 1 |
| Allan A. Lamport Stadium Park ⚠️ | Toronto › Spadina—Fort York | 1 |
| Norseman Heights Park ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Fairfield Park ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Sunnylea Park ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Humbertown Park ⚠️ | Toronto › Etobicoke Centre | 1 |
| Valecrest Park ⚠️ | Toronto › Etobicoke Centre | 1 |
| Rosethorn Park ⚠️ | Toronto › Etobicoke Centre | 1 |
| Mill Valley Park ⚠️ | Toronto › Etobicoke Centre | 1 |
| Parc de Toronto (129) ⚠️ | Toronto › York South—Weston | 1 |
| Rexlington Park ⚠️ | Toronto › Etobicoke North | 1 |
| Valley Field Park ⚠️ | Toronto › Etobicoke Centre | 1 |
| Tamarisk Park ⚠️ | Toronto › Etobicoke North | 1 |
| Halbert Park ⚠️ | Toronto › Scarborough Southwest | 1 |
| Garrison Common ⚠️ | Toronto › Spadina—Fort York | 1 |
| Parc de Toronto (140) ⚠️ | Toronto › Scarborough—Guildwood | 1 |
| Parc de Toronto (142) ⚠️ | Toronto › York South—Weston | 1 |
| Seasons Park ⚠️ | Toronto › Scarborough North | 1 |
| Parc de Toronto (144) ⚠️ | Toronto › Scarborough North | 1 |
| Stonehouse Park ⚠️ | Toronto › Etobicoke Centre | 1 |
| Highfield Park ⚠️ | Toronto › Etobicoke North | 1 |
| Parc de Toronto (145) ⚠️ | Toronto › Scarborough—Guildwood | 1 |
| Canoe Landing Park ⚠️ | Toronto › Spadina—Fort York | 1 |
| Florence Gell Park ⚠️ | Toronto › Parkdale—High Park | 1 |
| Parc de Toronto (148) ⚠️ | Toronto › Don Valley West | 1 |
| Hillside Park ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Coronation Park ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Rotary Park ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Saddletree Park ⚠️ | Toronto › Don Valley North | 1 |
| Roywood Park ⚠️ | Toronto › Don Valley East | 1 |
| Fenside Park ⚠️ | Toronto › Don Valley East | 1 |
| Cliffwood Park ⚠️ | Toronto › Don Valley North | 1 |
| Parc de Toronto (158) ⚠️ | Toronto › Willowdale | 1 |
| Longmore Park ⚠️ | Toronto › Willowdale | 1 |
| Ann Tindal Park ⚠️ | Toronto › Spadina—Fort York | 1 |
| Spadina Quay Wetland ⚠️ | Toronto › Spadina—Fort York | 1 |
| Humber Valley Park (2) ⚠️ | Toronto › Etobicoke Centre | 1 |
| Wedgewood Park (2) ⚠️ | Toronto › Willowdale | 1 |
| Jean Augustine Park ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Rowatson Park ⚠️ | Toronto › Scarborough—Guildwood | 1 |
| Parc de Toronto (174) ⚠️ | Toronto › Scarborough—Agincourt | 1 |
| Elm Park (2) ⚠️ | Toronto › York South—Weston | 1 |
| Geary Avenue Parkette ⚠️ | Toronto › Davenport | 1 |
| Brown's Line Lake Shore Parkette ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Parc de Toronto (179) ⚠️ | Toronto › Scarborough North | 1 |
| Long Branch Park ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Len Ford Park ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Parc de Toronto (184) ⚠️ | Toronto › Scarborough Centre | 1 |
| Parc de Toronto (186) ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Drumoak Road Parkette ⚠️ | Toronto › Etobicoke Centre | 1 |
| La Rose Park ⚠️ | Toronto › Etobicoke Centre | 1 |
| Lorraine Drive Park ⚠️ | Toronto › Willowdale | 1 |
| Glen Agar Park ⚠️ | Toronto › Etobicoke Centre | 1 |
| Kerr Hall Quad ⚠️ | Toronto › Toronto Centre | 1 |
| Abbotsford Park ⚠️ | Toronto › Willowdale | 1 |
| Adanac Park ⚠️ | Toronto › Scarborough Southwest | 1 |
| Maryland Park ⚠️ | Toronto › Beaches—East York | 1 |
| Charlton Park ⚠️ | Toronto › Willowdale | 1 |
| Glen Ravine Park ⚠️ | Toronto › Scarborough Centre | 1 |
| Michael Power Park ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Trace Manes Park ⚠️ | Toronto › Don Valley West | 1 |
| Ruddington Park ⚠️ | Toronto › Don Valley North | 1 |
| Dempsey Park ⚠️ | Toronto › Willowdale | 1 |
| Albion Arena ⚠️ | Toronto › Etobicoke North | 1 |
| Alexandra Park ⚠️ | Toronto › Spadina—Fort York | 1 |
| Alotment Garden Parkette ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Amberdale Ravine ⚠️ | Toronto › Scarborough Centre | 1 |
| Ames Park ⚠️ | Toronto › Don Valley West | 1 |
| Ancaster Park ⚠️ | Toronto › York Centre | 1 |
| Ancona Park ⚠️ | Toronto › Willowdale | 1 |
| Anewan Greenbelt ⚠️ | Toronto › Don Valley East | 1 |
| Ravina Gardens Park ⚠️ | Toronto › Parkdale—High Park | 1 |
| Anson Park ⚠️ | Toronto › Scarborough Southwest | 1 |
| Anthony Road School Park ⚠️ | Toronto › York Centre | 1 |
| Antibes Park ⚠️ | Toronto › York Centre | 1 |
| Apted Park ⚠️ | Toronto › Humber River—Black Creek | 1 |
| Baird Park ⚠️ | Toronto › Parkdale—High Park | 1 |
| Michael Mostyn Balmoral Park ⚠️ | Toronto › York Centre | 1 |
| Bamburgh Park ⚠️ | Toronto › Scarborough—Agincourt | 1 |
| Banbury Community Centre ⚠️ | Toronto › Don Valley West | 1 |
| Banting Park ⚠️ | Toronto › York Centre | 1 |
| Barkdene Park ⚠️ | Toronto › Scarborough Southwest | 1 |
| Bayview Arena Park ⚠️ | Toronto › Willowdale | 1 |
| Bayview/York Mills Parkette ⚠️ | Toronto › Don Valley West | 1 |
| Budapest Park ⚠️ | Toronto › Parkdale—High Park | 1 |
| Beaver Lightbourn Parkette ⚠️ | Toronto › Davenport | 1 |
| Bedford Parkette ⚠️ | Toronto › Eglinton—Lawrence | 1 |
| Brookdale Park (2) ⚠️ | Toronto › Eglinton—Lawrence | 1 |
| Bell Manor Park ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Bellamy Park ⚠️ | Toronto › Scarborough Southwest | 1 |
| Bendale Park ⚠️ | Toronto › Scarborough—Guildwood | 1 |
| Benjamin Boake Greenbelt ⚠️ | Toronto › York Centre | 1 |
| Benner Park ⚠️ | Toronto › Eglinton—Lawrence | 1 |
| Bethune Park ⚠️ | Toronto › Scarborough—Guildwood | 1 |
| Beverly Glen Park ⚠️ | Toronto › Scarborough—Agincourt | 1 |
| Birchcrest Park ⚠️ | Toronto › Scarborough—Agincourt | 1 |
| Chester Le Park ⚠️ | Toronto › Scarborough—Agincourt | 1 |
| Bill Hancox Park ⚠️ | Toronto › Scarborough—Rouge Park | 1 |
| Bill Johnston Park ⚠️ | Toronto › Spadina—Fort York | 1 |
| Birkdale Community Centre ⚠️ | Toronto › Scarborough Centre | 1 |
| Blantyre Park ⚠️ | Toronto › Scarborough Southwest | 1 |
| Bowan Court Parkette ⚠️ | Toronto › Don Valley North | 1 |
| Bramber Woods Park ⚠️ | Toronto › Scarborough—Rouge Park | 1 |
| Bratty Park ⚠️ | Toronto › Humber River—Black Creek | 1 |
| Bridlewood Park ⚠️ | Toronto › Scarborough—Agincourt | 1 |
| Brooks Road Park ⚠️ | Toronto › Scarborough—Guildwood | 1 |
| Bruce Mackey Park ⚠️ | Toronto › Toronto—Danforth | 1 |
| Burnett Park ⚠️ | Toronto › Willowdale | 1 |
| Burrows Hall Park ⚠️ | Toronto › Scarborough North | 1 |
| Burrows Hall Park (2) ⚠️ | Toronto › Scarborough North | 1 |
| Burrows Hall Park (3) ⚠️ | Toronto › Scarborough North | 1 |
| Dixon Park ⚠️ | Toronto › Etobicoke North | 1 |
| Willowridge Park ⚠️ | Toronto › Etobicoke North | 1 |
| Metrogate Park ⚠️ | Toronto › Scarborough—Agincourt | 1 |
| Joel Weeks Park ⚠️ | Toronto › Toronto—Danforth | 1 |
| Lawrence-Kennedy Parkette ⚠️ | Toronto › Scarborough Centre | 1 |
| Park Lawn Park ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Park Lawn Park (2) ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Olympia Park ⚠️ | Toronto › York South—Weston | 1 |
| Parc de Toronto (205) ⚠️ | Toronto › Scarborough—Rouge Park | 1 |
| Regent Park ⚠️ | Toronto › Toronto Centre | 1 |
| Bonspiel Park ⚠️ | Toronto › Scarborough—Guildwood | 1 |
| Wellesley - Magill Park ⚠️ | Toronto › Toronto Centre | 1 |
| Davenport Village Park ⚠️ | Toronto › Davenport | 1 |
| Senator Marian Maloney Park ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Islington Place Park ⚠️ | Toronto › Etobicoke North | 1 |
| Parc de Toronto (215) ⚠️ | Toronto › Scarborough—Rouge Park | 1 |
| Habitant Park ⚠️ | Toronto › Humber River—Black Creek | 1 |
| Glen Sheppard Park ⚠️ | Toronto › Scarborough Southwest | 1 |
| Woolner Park ⚠️ | Toronto › York South—Weston | 1 |
| Fairford Avenue Parkette ⚠️ | Toronto › Toronto—Danforth | 1 |
| Parc de Toronto (223) ⚠️ | Toronto › Scarborough Centre | 1 |
| Van Horne Park (2) ⚠️ | Toronto › Don Valley North | 1 |
| Hillsborough Park ⚠️ | Toronto › Scarborough—Guildwood | 1 |
| Fred Young Park ⚠️ | Toronto › Humber River—Black Creek | 1 |
| Whitehall Parkette ⚠️ | Toronto › University—Rosedale | 1 |
| Parc de Toronto (226) ⚠️ | Toronto › Scarborough Southwest | 1 |
| Morningside Church Park Area ⚠️ | Toronto › Parkdale—High Park | 1 |
| Colonel Danforth Park ⚠️ | Toronto › Scarborough—Rouge Park | 1 |
| Oak Street Park ⚠️ | Toronto › Toronto Centre | 1 |
| Port Union Waterfront Park ⚠️ | Toronto › Scarborough—Rouge Park | 1 |
| Duncan Creek Park (2) ⚠️ | Toronto › Don Valley North | 1 |
| Parc de Toronto (246) ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Craigleigh Gardens ⚠️ | Toronto › University—Rosedale | 1 |
| Toronto Botanical Garden ⚠️ | Toronto › Don Valley West | 1 |
| Joyce Trimmer Park ⚠️ | Toronto › Scarborough—Rouge Park | 1 |
| Parc de Toronto (255) ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Sir Adam Beck Park ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Parc de Toronto (256) ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Mimico Waterfront Park ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Parc de Toronto (257) ⚠️ | Toronto › Etobicoke North | 1 |
| Oakdale Village Park ⚠️ | Toronto › Humber River—Black Creek | 1 |
| Parc de Toronto (260) ⚠️ | Toronto › Humber River—Black Creek | 1 |
| Parc de Toronto (267) ⚠️ | Toronto › York South—Weston | 1 |
| Cy Townsend Park ⚠️ | Toronto › Toronto—St. Paul's | 1 |
| John Chang Neighbourhood Park ⚠️ | Toronto › Toronto—Danforth | 1 |
| Syd Cole Park ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| West Mall Outdoor Artifical Ice Rink ⚠️ | Toronto › Etobicoke Centre | 1 |
| Centennial Park (3) ⚠️ | Toronto › Spadina—Fort York | 1 |
| Parc de Toronto (276) ⚠️ | Toronto › Scarborough—Guildwood | 1 |
| Parc de Toronto (278) ⚠️ | Toronto › Scarborough Centre | 1 |
| Parc de Toronto (280) ⚠️ | Toronto › Scarborough Southwest | 1 |
| Parc de Toronto (281) ⚠️ | Toronto › Scarborough—Agincourt | 1 |
| Parc de Toronto (283) ⚠️ | Toronto › Scarborough—Agincourt | 1 |
| Sanwood Park ⚠️ | Toronto › Scarborough—Agincourt | 1 |
| Parc de Toronto (284) ⚠️ | Toronto › Scarborough Centre | 1 |
| Parc de Toronto (286) ⚠️ | Toronto › Scarborough Southwest | 1 |
| Hummingbird Park ⚠️ | Toronto › Scarborough North | 1 |
| McCleary Playground ⚠️ | Toronto › Toronto—Danforth | 1 |
| Langford Parkette ⚠️ | Toronto › Toronto—Danforth | 1 |
| Denfield Park ⚠️ | Toronto › Etobicoke Centre | 1 |
| Parc de Toronto (293) ⚠️ | Toronto › Humber River—Black Creek | 1 |
| Spadina Road Park ⚠️ | Toronto › Toronto—St. Paul's | 1 |
| Kilgour Parkette ⚠️ | Toronto › Don Valley West | 1 |
| Honey & Barry Community Park ⚠️ | Toronto › York Centre | 1 |
| Lower Field ⚠️ | Toronto › Eglinton—Lawrence | 1 |
| Parc de Toronto (319) ⚠️ | Toronto › Eglinton—Lawrence | 1 |
| Parc de Toronto (320) ⚠️ | Toronto › Eglinton—Lawrence | 1 |
| Parc de Toronto (324) ⚠️ | Toronto › Don Valley North | 1 |
| Allenbury Park ⚠️ | Toronto › Don Valley North | 1 |
| Garnier Park ⚠️ | Toronto › Don Valley North | 1 |
| Islington Parkette ⚠️ | Toronto › Etobicoke—Lakeshore | 1 |
| Spadina Park ⚠️ | Toronto › Toronto—St. Paul's | 1 |
| Linkwood Lane Park ⚠️ | Toronto › Don Valley East | 1 |
| Parc de Toronto (327) ⚠️ | Toronto › Scarborough Southwest | 1 |
| Leslie Barns Park ⚠️ | Toronto › Toronto—Danforth | 1 |
| Frankel Lambert Park ⚠️ | Toronto › Toronto—St. Paul's | 1 |
| 175 The Pond Road Park ⚠️ | Toronto › Humber River—Black Creek | 1 |
| Ledbury Park ⚠️ | Toronto › Eglinton—Lawrence | 1 |
| Glengarry Park ⚠️ | Toronto › Eglinton—Lawrence | 1 |
| Manhattan Park ⚠️ | Toronto › Scarborough Centre | 1 |
| Isaac Devins Park ⚠️ | Toronto › Humber River—Black Creek | 1 |
| Roycroft Park Lands ⚠️ | Toronto › Toronto—St. Paul's | 1 |
| Bluehaven Park ⚠️ | Toronto › Humber River—Black Creek | 1 |
| Louise Russo Park ⚠️ | Toronto › Humber River—Black Creek | 1 |
| Esther Lorrie Park ⚠️ | Toronto › Etobicoke North | 1 |
| Sunnydene Park ⚠️ | Toronto › Don Valley West | 1 |
| Irma Burman Greenbelt ⚠️ | Toronto › Scarborough—Rouge Park | 1 |
| The Park at CIBC Square ⚠️ | Toronto › Spadina—Fort York | 1 |
| Portland Street Parkette ⚠️ | Toronto › Spadina—Fort York | 1 |
| Horsham Parquette ⚠️ | Toronto › Willowdale | 1 |
| Diana Park ⚠️ | Toronto › York Centre | 1 |
| Front Campus ⚠️ | Toronto › University—Rosedale | 1 |
| Suydam Park ⚠️ | Toronto › Toronto—St. Paul's | 1 |
| Don-Leslie Park ⚠️ | Toronto › Don Valley East | 1 |
| Secord Park ⚠️ | Toronto › Beaches—East York | 1 |
| J.A. Leslie Tot Lot ⚠️ | Toronto › Scarborough Southwest | 1 |
| Joshua Cronkwright Parkette ⚠️ | Toronto › Beaches—East York | 1 |
| Sadler Parkette ⚠️ | Toronto › Scarborough Southwest | 1 |
| Edgewood Park ⚠️ | Toronto › Scarborough Centre | 1 |
| Maxome Park ⚠️ | Toronto › Willowdale | 1 |
| North Agincourt Park ⚠️ | Toronto › Scarborough North | 1 |
| Woodsworth Greenbelt ⚠️ | Toronto › Don Valley West | 1 |
| Mary Harker Park ⚠️ | Toronto › Etobicoke North | 1 |
| Blackfriar Park ⚠️ | Toronto › Etobicoke North | 1 |
| Underpass Park ⚠️ | Toronto › Toronto Centre | 1 |
| West Toronto Railpath ⚠️ | Toronto › Davenport | 1 |
| Wincott Park ⚠️ | Toronto › Etobicoke Centre | 1 |
| Evergreen Gardens Park ⚠️ | Toronto › Don Valley West | 1 |
| Bob Acton Park ⚠️ | Toronto › Beaches—East York | 1 |
| Queen's Park ⚠️ | Toronto › University—Rosedale | 1 |

950 parc(s) plus petits qu'une cellule ne sont pas listés : la carte les dessine, mais ils n'offrent aucune cellule.

⚠️ 1681 parc(s) hors de la fenêtre 10–125 cellules (1680 trop petit(s), 1 trop grand(s)) : affichés sur la carte, mais ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| airport | 56 |
| military | 14 |
| prison | 5 |
| **Total déclaré** | **75** |
| dont dans une zone de ce territoire | 75 |


### Zones concernées

| Zone | Cellules exclues |
|---|---:|
| Toronto | 75 |
| Spadina—Fort York | 41 |
| Etobicoke North | 15 |
| York Centre | 14 |
| Etobicoke—Lakeshore | 5 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
