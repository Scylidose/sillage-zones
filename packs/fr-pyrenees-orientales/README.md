# Pyrénées-Orientales

Pack `fr-pyrenees-orientales` · version 1.0.0 · grille 200 m · France › Occitanie

> Généré par `scripts/build_pack_readme.py`. Ne pas éditer à la main : les nombres sont recalculés depuis les frontières du pack.

## Résumé

| | |
|---|---:|
| Cellules du territoire | 187 842 |
| dont restreintes (aéroport, militaire, prison) | 1 615 |
| Cellules retirées par le masque d'eau | 3 132 |
| Villes | 226 |
| Arrondissements et quartiers | 0 |
| Îles | 12 |
| Parcs | 3 448 |

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

## Îles

| Île | Cellules | Composition |
|---|---:|---|
| Agly Fenouillèdes | 17 135 | somme de 24 villes |
| Conflent-Canigó | 36 014 | somme de 45 villes |
| Corbières Salanque Méditerranée | 4 817 | somme de 3 villes |
| Pyrénées Cerdagne | 20 086 | somme de 19 villes |
| Pyrénées catalanes | 16 218 | somme de 19 villes |
| Roussillon Conflent | 10 251 | somme de 15 villes |
| Sud-Roussillon | 1 884 | somme de 6 villes |
| Albères – Côte Vermeille – Illibéris | 13 349 | somme de 15 villes |
| Aspres | 10 651 | somme de 19 villes |
| Haut-Vallespir | 20 199 | somme de 14 villes |
| Vallespir | 8 409 | somme de 10 villes |
| Perpignan Méditerranée Métropole | 28 839 | somme de 37 villes |

Une île *composite* n'a pas de cellules à elle : sa progression est la somme de ses villes, et ses cellules ne lui sont jamais rattachées directement — elles compteraient deux fois.

## Villes (226)

| Zone | Brut | Eau | Sans eau | Restr. | Comptées | Parcs |
|---|---:|---:|---:|---:|---:|---:|
| Prats-de-Mollo-la-Preste | 5 494 | 0 | 5 494 | 0 | **5 494** | 34 |
| Angoustrine-Villeneuve-des-Escaldes | 3 959 | 166 | 3 793 | 0 | **3 793** | 493 |
| Salses-le-Château | 3 836 | 506 | 3 330 | 286 | **3 044** | 17 |
| Mosset | 3 275 | 0 | 3 275 | 0 | **3 275** | 23 |
| Perpignan | 3 150 | 35 | 3 115 | 61 | **3 054** | 109 |
| Porta | 2 985 | 3 | 2 982 | 0 | **2 982** | 30 |
| Fontpédrouse | 2 959 | 6 | 2 953 | 0 | **2 953** | 20 |
| Argelès-sur-Mer | 2 719 | 68 | 2 651 | 0 | **2 651** | 39 |
| Tautavel | 2 473 | 0 | 2 473 | 184 | **2 289** | 6 |
| Porté-Puymorens | 2 330 | 7 | 2 323 | 0 | **2 323** | 98 |
| Py | 2 298 | 0 | 2 298 | 0 | **2 298** | 9 |
| Opoul-Périllos | 2 261 | 0 | 2 261 | 128 | **2 133** | 21 |
| Corsavy | 2 193 | 0 | 2 193 | 0 | **2 193** | 9 |
| Formiguères | 2 189 | 26 | 2 163 | 0 | **2 163** | 380 |
| Saint-Paul-de-Fenouillet | 2 054 | 0 | 2 054 | 0 | **2 054** | 22 |
| Saint-Laurent-de-Cerdans | 2 053 | 0 | 2 053 | 0 | **2 053** | 8 |
| Banyuls-sur-Mer | 1 975 | 5 | 1 970 | 0 | **1 970** | 48 |
| Maureillas-las-Illas | 1 947 | 1 | 1 946 | 0 | **1 946** | 14 |
| Les Angles | 2 001 | 56 | 1 945 | 0 | **1 945** | 201 |
| Caudiès-de-Fenouillèdes | 1 742 | 0 | 1 742 | 0 | **1 742** | 34 |
| Céret | 1 745 | 9 | 1 736 | 0 | **1 736** | 17 |
| Nyer | 1 677 | 0 | 1 677 | 0 | **1 677** | 15 |
| Maury | 1 618 | 0 | 1 618 | 0 | **1 618** | 3 |
| Sorède | 1 582 | 1 | 1 581 | 0 | **1 581** | 15 |
| Mantet | 1 493 | 0 | 1 493 | 0 | **1 493** | 11 |
| Vingrau | 1 472 | 0 | 1 472 | 141 | **1 331** | 10 |
| Ille-sur-Têt | 1 465 | 15 | 1 450 | 0 | **1 450** | 7 |
| Sournia | 1 405 | 0 | 1 405 | 0 | **1 405** | 8 |
| Enveitg | 1 395 | 2 | 1 393 | 0 | **1 393** | 38 |
| Ayguatébia-Talau | 1 384 | 0 | 1 384 | 230 | **1 154** | 16 |
| Font-Romeu-Odeillo-Via | 1 365 | 0 | 1 365 | 0 | **1 365** | 223 |
| Casteil | 1 364 | 0 | 1 364 | 0 | **1 364** | 6 |
| Olette | 1 350 | 2 | 1 348 | 0 | **1 348** | 4 |
| Amélie-les-Bains-Palalda | 1 347 | 3 | 1 344 | 0 | **1 344** | 7 |
| Arles-sur-Tech | 1 330 | 4 | 1 326 | 0 | **1 326** | 6 |
| Nohèdes | 1 330 | 4 | 1 326 | 0 | **1 326** | 7 |
| Rivesaltes | 1 335 | 18 | 1 317 | 111 | **1 206** | 24 |
| Llo | 1 312 | 0 | 1 312 | 0 | **1 312** | 3 |
| Reynès | 1 276 | 2 | 1 274 | 0 | **1 274** | 2 |
| Caixas | 1 276 | 7 | 1 269 | 0 | **1 269** | 3 |
| Valmanya | 1 264 | 0 | 1 264 | 0 | **1 264** | 10 |
| Espira-de-l'Agly | 1 258 | 20 | 1 238 | 186 | **1 052** | 11 |
| Estoher | 1 210 | 0 | 1 210 | 0 | **1 210** | 2 |
| Le Tech | 1 199 | 0 | 1 199 | 0 | **1 199** | 3 |
| Valcebollère | 1 199 | 0 | 1 199 | 0 | **1 199** | 2 |
| Err | 1 197 | 1 | 1 196 | 0 | **1 196** | 29 |
| Dorres | 1 155 | 0 | 1 155 | 0 | **1 155** | 2 |
| Calce | 1 114 | 6 | 1 108 | 0 | **1 108** | 2 |
| Canet-en-Roussillon | 1 410 | 311 | 1 099 | 0 | **1 099** | 23 |
| Lamanère | 1 083 | 0 | 1 083 | 0 | **1 083** | 4 |
| Boule-d'Amont | 1 074 | 0 | 1 074 | 0 | **1 074** | 2 |
| La Llagonne | 1 064 | 1 | 1 063 | 22 | **1 041** | 86 |
| Sansa | 1 049 | 0 | 1 049 | 0 | **1 049** | 4 |
| Serralongue | 1 048 | 0 | 1 048 | 0 | **1 048** | 1 |
| Montbolo | 1 009 | 0 | 1 009 | 0 | **1 009** | 4 |
| Prunet-et-Belpuig | 1 008 | 0 | 1 008 | 0 | **1 008** |  |
| Montferrer | 990 | 0 | 990 | 0 | **990** | 1 |
| Elne | 1 003 | 15 | 988 | 0 | **988** | 19 |
| Laroque-des-Albères | 951 | 0 | 951 | 0 | **951** | 6 |
| Bélesta | 946 | 0 | 946 | 0 | **946** | 12 |
| Eyne | 946 | 0 | 946 | 0 | **946** | 25 |
| Estagel | 961 | 17 | 944 | 0 | **944** | 11 |
| Eus | 939 | 4 | 935 | 0 | **935** | 9 |
| Thuir | 928 | 0 | 928 | 0 | **928** | 14 |
| Thuès-Entre-Valls | 920 | 0 | 920 | 0 | **920** | 6 |
| Rabouillet | 900 | 0 | 900 | 0 | **900** | 5 |
| Puyvalador | 899 | 6 | 893 | 0 | **893** | 100 |
| Castelnou | 891 | 5 | 886 | 0 | **886** | 3 |
| Conat | 884 | 0 | 884 | 0 | **884** | 5 |
| Millas | 891 | 10 | 881 | 0 | **881** | 10 |
| Fenouillet | 880 | 0 | 880 | 0 | **880** | 33 |
| Baixas | 881 | 3 | 878 | 0 | **878** | 1 |
| Claira | 898 | 23 | 875 | 0 | **875** | 1 |
| Glorianes | 873 | 0 | 873 | 0 | **873** | 1 |
| Oms | 865 | 0 | 865 | 0 | **865** | 46 |
| Rodès | 862 | 7 | 855 | 0 | **855** | 7 |
| Bolquère | 828 | 7 | 821 | 0 | **821** | 21 |
| Baillestavy | 818 | 0 | 818 | 0 | **818** | 3 |
| Trévillach | 815 | 0 | 815 | 0 | **815** | 1 |
| Matemale | 891 | 77 | 814 | 0 | **814** | 39 |
| Serdinya | 798 | 0 | 798 | 0 | **798** | 4 |
| Campoussy | 792 | 0 | 792 | 0 | **792** | 3 |
| Osséja | 784 | 0 | 784 | 0 | **784** |  |
| Montesquieu-des-Albères | 790 | 9 | 781 | 0 | **781** | 7 |
| Torreilles | 807 | 29 | 778 | 4 | **774** | 11 |
| Trouillas | 788 | 14 | 774 | 0 | **774** | 10 |
| Vernet-les-Bains | 773 | 4 | 769 | 0 | **769** | 16 |
| Coustouges | 767 | 0 | 767 | 0 | **767** | 5 |
| Oreilla | 760 | 0 | 760 | 0 | **760** |  |
| Pézilla-la-Rivière | 763 | 4 | 759 | 0 | **759** | 8 |
| L'Albère | 748 | 0 | 748 | 0 | **748** | 4 |
| Montalba-le-Château | 740 | 0 | 740 | 0 | **740** | 2 |
| Lesquerde | 730 | 0 | 730 | 0 | **730** | 2 |
| Saint-Cyprien | 747 | 18 | 729 | 0 | **729** | 17 |
| Fontrabiouse | 713 | 1 | 712 | 0 | **712** | 11 |
| La Bastide | 710 | 0 | 710 | 0 | **710** | 1 |
| Saint-Marsal | 705 | 0 | 705 | 0 | **705** |  |
| Escaro | 700 | 0 | 700 | 0 | **700** | 6 |
| Cassagnes | 709 | 11 | 698 | 0 | **698** | 10 |
| Sahorre | 691 | 0 | 691 | 0 | **691** | 14 |
| Saint-Hippolyte | 1 173 | 503 | 670 | 0 | **670** | 2 |
| Planès | 665 | 0 | 665 | 0 | **665** | 3 |
| Port-Vendres | 664 | 0 | 664 | 0 | **664** | 24 |
| Urbanya | 652 | 0 | 652 | 0 | **652** | 5 |
| Latour-de-France | 652 | 3 | 649 | 0 | **649** | 7 |
| Le Boulou | 670 | 24 | 646 | 0 | **646** | 7 |
| Arboussols | 647 | 4 | 643 | 0 | **643** | 4 |
| Prugnanes | 640 | 0 | 640 | 0 | **640** | 7 |
| Rasiguères | 634 | 0 | 634 | 0 | **634** | 4 |
| Ponteilla | 638 | 5 | 633 | 0 | **633** | 7 |
| Taurinya | 628 | 0 | 628 | 0 | **628** | 13 |
| Pia | 618 | 6 | 612 | 0 | **612** | 10 |
| Calmeilles | 618 | 7 | 611 | 0 | **611** | 8 |
| Passa | 621 | 11 | 610 | 0 | **610** |  |
| Cases-de-Pène | 629 | 25 | 604 | 98 | **506** | 7 |
| Caramany | 662 | 59 | 603 | 0 | **603** | 14 |
| Le Vivier | 600 | 0 | 600 | 0 | **600** | 4 |
| Molitg-les-Bains | 600 | 0 | 600 | 0 | **600** | 2 |
| Vira | 597 | 0 | 597 | 0 | **597** | 2 |
| Camélas | 601 | 6 | 595 | 0 | **595** | 11 |
| Latour-de-Carol | 601 | 8 | 593 | 0 | **593** | 3 |
| Ria-Sirach | 595 | 2 | 593 | 0 | **593** | 12 |
| Saint-Pierre-dels-Forcats | 592 | 0 | 592 | 0 | **592** | 53 |
| Corneilla-la-Rivière | 590 | 1 | 589 | 0 | **589** | 3 |
| Collioure | 555 | 1 | 554 | 4 | **550** | 14 |
| Saint-Laurent-de-la-Salanque | 813 | 264 | 549 | 52 | **497** | 5 |
| Bages | 550 | 2 | 548 | 0 | **548** | 4 |
| Saint-Estève | 540 | 5 | 535 | 0 | **535** | 14 |
| Villelongue-dels-Monts | 537 | 10 | 527 | 0 | **527** | 2 |
| Vivès | 521 | 0 | 521 | 0 | **521** | 6 |
| Montauriol | 522 | 2 | 520 | 0 | **520** | 1 |
| Palau-de-Cerdagne | 520 | 0 | 520 | 0 | **520** | 6 |
| Saillagouse | 520 | 0 | 520 | 0 | **520** | 8 |
| Canaveilles | 513 | 0 | 513 | 12 | **501** |  |
| Corneilla-de-Conflent | 512 | 0 | 512 | 0 | **512** | 21 |
| Le Barcarès | 737 | 225 | 512 | 0 | **512** | 23 |
| Montner | 512 | 0 | 512 | 0 | **512** | 6 |
| Tresserre | 517 | 11 | 506 | 0 | **506** | 1 |
| Prades | 507 | 2 | 505 | 0 | **505** | 21 |
| Bouleternère | 500 | 0 | 500 | 0 | **500** | 3 |
| Cabestany | 493 | 5 | 488 | 0 | **488** | 16 |
| Banyuls-dels-Aspres | 492 | 6 | 486 | 0 | **486** | 2 |
| Saint-Féliu-d'Avall | 483 | 4 | 479 | 0 | **479** | 2 |
| Railleu | 476 | 0 | 476 | 0 | **476** | 9 |
| Réal | 490 | 14 | 476 | 0 | **476** | 17 |
| Saint-Jean-Pla-de-Corts | 491 | 15 | 476 | 0 | **476** | 10 |
| Palau-del-Vidre | 478 | 7 | 471 | 0 | **471** | 2 |
| Le Soler | 481 | 11 | 470 | 0 | **470** | 21 |
| Sainte-Marie-la-Mer | 480 | 11 | 469 | 0 | **469** | 3 |
| Tordères | 466 | 0 | 466 | 0 | **466** | 2 |
| Jujols | 464 | 0 | 464 | 0 | **464** | 2 |
| Taillet | 463 | 0 | 463 | 0 | **463** | 1 |
| Saint-Génis-des-Fontaines | 456 | 2 | 454 | 0 | **454** | 3 |
| Saint-Nazaire | 479 | 29 | 450 | 0 | **450** | 6 |
| Fuilla | 448 | 0 | 448 | 0 | **448** | 16 |
| Villeneuve-de-la-Raho | 530 | 84 | 446 | 0 | **446** | 5 |
| Saint-Martin-de-Fenouillet | 443 | 0 | 443 | 0 | **443** | 4 |
| Saint-André | 453 | 15 | 438 | 0 | **438** | 6 |
| Fourques | 441 | 7 | 434 | 0 | **434** | 1 |
| Estavar | 426 | 3 | 423 | 0 | **423** | 3 |
| Sainte-Léocadie | 413 | 0 | 413 | 15 | **398** | 1 |
| Trilla | 417 | 4 | 413 | 0 | **413** | 1 |
| Saint-Michel-de-Llotes | 410 | 0 | 410 | 0 | **410** | 2 |
| Les Cluses | 404 | 0 | 404 | 0 | **404** |  |
| Clara-Villerach | 403 | 0 | 403 | 0 | **403** | 4 |
| Fillols | 401 | 0 | 401 | 0 | **401** | 5 |
| Néfiach | 408 | 7 | 401 | 0 | **401** | 10 |
| Canohès | 400 | 0 | 400 | 0 | **400** | 5 |
| Finestret | 394 | 2 | 392 | 0 | **392** | 2 |
| Tarerach | 389 | 0 | 389 | 0 | **389** |  |
| Ortaffa | 398 | 10 | 388 | 0 | **388** | 2 |
| Sauto | 386 | 0 | 386 | 62 | **324** | 10 |
| Cerbère | 383 | 0 | 383 | 0 | **383** | 8 |
| Prats-de-Sournia | 381 | 0 | 381 | 0 | **381** | 1 |
| Llauro | 381 | 1 | 380 | 0 | **380** |  |
| Peyrestortes | 377 | 0 | 377 | 6 | **371** | 13 |
| Pollestres | 387 | 10 | 377 | 0 | **377** | 6 |
| Catllar | 373 | 2 | 371 | 0 | **371** | 7 |
| Toulouges | 372 | 1 | 371 | 0 | **371** | 5 |
| Ansignan | 373 | 9 | 364 | 0 | **364** | 2 |
| Targasonne | 357 | 0 | 357 | 0 | **357** | 5 |
| Baho | 361 | 6 | 355 | 0 | **355** | 1 |
| Brouilla | 366 | 13 | 353 | 0 | **353** | 4 |
| Bourg-Madame | 351 | 1 | 350 | 0 | **350** | 7 |
| Terrats | 350 | 4 | 346 | 0 | **346** | 2 |
| Corbère | 344 | 0 | 344 | 0 | **344** | 1 |
| Villelongue-de-la-Salanque | 337 | 1 | 336 | 0 | **336** | 3 |
| Llupia | 326 | 0 | 326 | 0 | **326** | 3 |
| Casefabre | 322 | 0 | 322 | 0 | **322** | 2 |
| Saint-Arnac | 319 | 0 | 319 | 0 | **319** | 2 |
| Pézilla-de-Conflent | 316 | 0 | 316 | 0 | **316** | 1 |
| Feilluns | 307 | 0 | 307 | 0 | **307** | 1 |
| Ur | 308 | 1 | 307 | 0 | **307** | 9 |
| Caudiès-de-Conflent | 304 | 0 | 304 | 0 | **304** | 3 |
| Planèzes | 296 | 0 | 296 | 0 | **296** | 1 |
| Vinça | 357 | 67 | 290 | 0 | **290** | 10 |
| Saleilles | 286 | 3 | 283 | 0 | **283** | 4 |
| Taulis | 278 | 0 | 278 | 0 | **278** |  |
| Espira-de-Conflent | 277 | 0 | 277 | 0 | **277** | 3 |
| Villemolaque | 281 | 6 | 275 | 0 | **275** | 2 |
| Montescot | 287 | 21 | 266 | 0 | **266** | 1 |
| Bompas | 267 | 2 | 265 | 0 | **265** | 10 |
| Los Masos | 262 | 0 | 262 | 0 | **262** | 8 |
| Alénya | 264 | 3 | 261 | 0 | **261** | 3 |
| Nahuja | 258 | 0 | 258 | 0 | **258** | 2 |
| Saint-Féliu-d'Amont | 256 | 3 | 253 | 0 | **253** | 1 |
| Corneilla-del-Vercol | 252 | 1 | 251 | 0 | **251** | 7 |
| Campôme | 247 | 0 | 247 | 0 | **247** | 1 |
| Lansac | 245 | 0 | 245 | 0 | **245** |  |
| Souanyas | 229 | 0 | 229 | 0 | **229** | 2 |
| Théza | 223 | 0 | 223 | 0 | **223** | 2 |
| Marquixanes | 226 | 4 | 222 | 0 | **222** | 2 |
| Sainte-Colombe-de-la-Commanderie | 217 | 0 | 217 | 0 | **217** |  |
| Villefranche-de-Conflent | 210 | 0 | 210 | 0 | **210** | 3 |
| Égat | 208 | 0 | 208 | 0 | **208** | 2 |
| Fosse | 207 | 0 | 207 | 0 | **207** | 1 |
| Villeneuve-la-Rivière | 204 | 1 | 203 | 0 | **203** | 2 |
| Le Perthus | 195 | 0 | 195 | 0 | **195** | 5 |
| Corbère-les-Cabanes | 194 | 0 | 194 | 0 | **194** | 2 |
| Rigarda | 168 | 0 | 168 | 0 | **168** | 2 |
| Joch | 165 | 0 | 165 | 0 | **165** | 2 |
| Latour-Bas-Elne | 155 | 1 | 154 | 0 | **154** | 6 |
| La Cabanasse | 147 | 0 | 147 | 0 | **147** | 5 |
| Codalet | 132 | 0 | 132 | 0 | **132** | 1 |
| Saint-Jean-Lasseille | 130 | 0 | 130 | 0 | **130** | 1 |
| Mont-Louis | 17 | 0 | 17 | 13 | **4** |  |

## Parcs (3448)

Cellules réellement offertes : dans le parc, hors eau et hors zone restreinte — ce que l'app énumère pour un défi. Le pack livre tous les parcs, la zone les affiche tous ; seuls ceux de 10 à 125 cellules peuvent servir de cible à un défi « parc ».

« Zone » est celle qui contient le plus de cellules du parc : un parc à cheval sur deux villes n'est rattaché qu'à une seule.

| Parc | Zone | Cellules |
|---|---|---:|
| Forêt de Saint-Laurent-de-Cerdans (3) ⚠️ | Saint-Laurent-de-Cerdans › Haut-Vallespir | 9 086 |
| Forêt de Sorède (4) ⚠️ | Sorède › Albères – Côte Vermeille – Illibéris | 2 528 |
| Forêt de Oms (12) ⚠️ | Oms › Aspres | 2 192 |
| Forêt de Corsavy (7) ⚠️ | Corsavy › Haut-Vallespir | 1 820 |
| Forêt de Matemale (39) ⚠️ | Matemale › Pyrénées catalanes | 1 668 |
| Forêt de La Llagonne (85) ⚠️ | La Llagonne › Pyrénées catalanes | 1 549 |
| Forêt de Baillestavy (2) ⚠️ | Baillestavy › Conflent-Canigó | 1 277 |
| Forêt de Olette (3) ⚠️ | Olette › Conflent-Canigó | 1 107 |
| Forêt des Angles (182) ⚠️ | Les Angles › Pyrénées catalanes | 1 073 |
| Forêt de l'Albère ⚠️ | L'Albère › Vallespir | 1 022 |
| Forêt de Casteil (4) ⚠️ | Casteil › Conflent-Canigó | 1 000 |
| Forêt de Err (29) ⚠️ | Err › Pyrénées Cerdagne | 995 |
| Forêt de Valcebollère (2) ⚠️ | Valcebollère › Pyrénées Cerdagne | 980 |
| Forêt de Boule-d'Amont ⚠️ | Boule-d'Amont › Roussillon Conflent | 959 |
| Forêt de Prats-de-Mollo-la-Preste (23) ⚠️ | Prats-de-Mollo-la-Preste › Haut-Vallespir | 919 |
| Forêt de Calmeilles ⚠️ | Calmeilles › Aspres | 868 |
| Forêt de Montbolo (3) ⚠️ | Montbolo › Haut-Vallespir | 850 |
| Forêt de Caixas (2) ⚠️ | Caixas › Roussillon Conflent | 834 |
| Forêt de Ayguatébia-Talau (16) ⚠️ | Ayguatébia-Talau › Pyrénées catalanes | 700 |
| Forêt de Fontpédrouse ⚠️ | Fontpédrouse › Conflent-Canigó | 696 |
| Forêt de Escaro (6) ⚠️ | Escaro › Conflent-Canigó | 678 |
| Forêt de Boule-d'Amont (2) ⚠️ | Boule-d'Amont › Roussillon Conflent | 572 |
| Bois de Planès ⚠️ | Planès › Pyrénées catalanes | 561 |
| Forêt de Py ⚠️ | Py › Conflent-Canigó | 540 |
| Forêt de Caixas (3) ⚠️ | Caixas › Roussillon Conflent | 527 |
| Forêt du Tech (2) ⚠️ | Le Tech › Haut-Vallespir | 506 |
| Forêt de Trilla ⚠️ | Trilla › Agly Fenouillèdes | 499 |
| Forêt du Vivier (3) ⚠️ | Le Vivier › Agly Fenouillèdes | 496 |
| Forêt de Bouleternère ⚠️ | Bouleternère › Roussillon Conflent | 441 |
| Forêt de Thuès-Entre-Valls ⚠️ | Thuès-Entre-Valls › Conflent-Canigó | 440 |
| Bois de Saint-Paul-de-Fenouillet (3) ⚠️ | Saint-Paul-de-Fenouillet › Agly Fenouillèdes | 440 |
| Forêt de Mosset (21) ⚠️ | Mosset › Conflent-Canigó | 410 |
| Forêt de Corsavy ⚠️ | Corsavy › Haut-Vallespir | 409 |
| Forêt de Fenouillet (24) ⚠️ | Fenouillet › Agly Fenouillèdes | 384 |
| Forêt de Prats-de-Mollo-la-Preste (24) ⚠️ | Prats-de-Mollo-la-Preste › Haut-Vallespir | 383 |
| Forêt de Rabouillet (4) ⚠️ | Rabouillet › Agly Fenouillèdes | 365 |
| Forêt de Finestret (2) ⚠️ | Finestret › Conflent-Canigó | 348 |
| Forêt de Mosset ⚠️ | Mosset › Conflent-Canigó | 338 |
| Forêt de Taurinya (5) ⚠️ | Taurinya › Conflent-Canigó | 337 |
| Forêt de Fontrabiouse (11) ⚠️ | Fontrabiouse › Pyrénées catalanes | 337 |
| Forêt de Pézilla-de-Conflent ⚠️ | Pézilla-de-Conflent › Agly Fenouillèdes | 336 |
| Forêt de Thuès-Entre-Valls (3) ⚠️ | Thuès-Entre-Valls › Conflent-Canigó | 334 |
| Forêt de Font-Romeu-Odeillo-Via (216) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 304 |
| Forêt de Caixas ⚠️ | Caixas › Roussillon Conflent | 300 |
| Forêt de Vivès (5) ⚠️ | Vivès › Vallespir | 291 |
| Forêt de Valmanya (6) ⚠️ | Valmanya › Conflent-Canigó | 287 |
| Forêt de Nyer (5) ⚠️ | Nyer › Conflent-Canigó | 284 |
| Forêt de Mosset (7) ⚠️ | Mosset › Conflent-Canigó | 273 |
| Forêt de Ansignan (2) ⚠️ | Ansignan › Agly Fenouillèdes | 272 |
| Forêt de Prugnanes (2) ⚠️ | Prugnanes › Agly Fenouillèdes | 270 |
| Forêt de Mantet (3) ⚠️ | Mantet › Conflent-Canigó | 264 |
| Forêt de Prugnanes (5) ⚠️ | Prugnanes › Agly Fenouillèdes | 263 |
| Forêt de Clara-Villerach (3) ⚠️ | Clara-Villerach › Conflent-Canigó | 254 |
| Forêt de Eyne ⚠️ | Eyne › Pyrénées catalanes | 249 |
| Forêt de Prats-de-Mollo-la-Preste (9) ⚠️ | Prats-de-Mollo-la-Preste › Haut-Vallespir | 245 |
| Forêt de Caudiès-de-Fenouillèdes (17) ⚠️ | Caudiès-de-Fenouillèdes › Agly Fenouillèdes | 225 |
| Forêt de Prats-de-Mollo-la-Preste (10) ⚠️ | Prats-de-Mollo-la-Preste › Haut-Vallespir | 222 |
| Forêt de Porta (4) ⚠️ | Porta › Pyrénées Cerdagne | 221 |
| Forêt de Vira ⚠️ | Vira › Agly Fenouillèdes | 214 |
| Forêt de Matemale (38) ⚠️ | Matemale › Pyrénées catalanes | 210 |
| Forêt de Ayguatébia-Talau ⚠️ | Ayguatébia-Talau › Pyrénées catalanes | 208 |
| Forêt de Bélesta (8) ⚠️ | Bélesta › Roussillon Conflent | 207 |
| Forêt de Formiguères ⚠️ | Formiguères › Pyrénées catalanes | 199 |
| Forêt de Vira (2) ⚠️ | Vira › Agly Fenouillèdes | 197 |
| Forêt de Prats-de-Mollo-la-Preste (13) ⚠️ | Prats-de-Mollo-la-Preste › Haut-Vallespir | 194 |
| Forêt de Fontpédrouse (2) ⚠️ | Fontpédrouse › Conflent-Canigó | 190 |
| Forêt de Saint-Martin-de-Fenouillet (4) ⚠️ | Saint-Martin-de-Fenouillet › Agly Fenouillèdes | 189 |
| Forêt de Rabouillet (5) ⚠️ | Rabouillet › Agly Fenouillèdes | 184 |
| Forêt de Maureillas-las-Illas (4) ⚠️ | Maureillas-las-Illas › Vallespir | 181 |
| Forêt de Prugnanes (6) ⚠️ | Prugnanes › Agly Fenouillèdes | 180 |
| Forêt de Casteil (5) ⚠️ | Casteil › Conflent-Canigó | 174 |
| Forêt de Thuès-Entre-Valls (4) ⚠️ | Thuès-Entre-Valls › Conflent-Canigó | 172 |
| Forêt de Puyvalador (97) ⚠️ | Puyvalador › Pyrénées catalanes | 165 |
| Forêt du Perthus (3) ⚠️ | Le Perthus › Vallespir | 165 |
| Forêt de Py (3) ⚠️ | Py › Conflent-Canigó | 164 |
| Forêt de Porté-Puymorens (4) ⚠️ | Porté-Puymorens › Pyrénées Cerdagne | 154 |
| Bois de Vingrau (4) ⚠️ | Vingrau › Perpignan Méditerranée Métropole | 154 |
| Forêt de Prats-de-Mollo-la-Preste (11) ⚠️ | Prats-de-Mollo-la-Preste › Haut-Vallespir | 153 |
| Forêt de Valmanya (3) ⚠️ | Valmanya › Conflent-Canigó | 153 |
| Forêt de Py (5) ⚠️ | Py › Conflent-Canigó | 152 |
| Forêt de Estoher (2) ⚠️ | Estoher › Conflent-Canigó | 152 |
| Forêt de Casteil ⚠️ | Casteil › Conflent-Canigó | 146 |
| Forêt de Mantet (4) ⚠️ | Mantet › Conflent-Canigó | 143 |
| Forêt de Font-Romeu-Odeillo-Via (217) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 142 |
| Forêt de Campoussy (3) ⚠️ | Campoussy › Agly Fenouillèdes | 141 |
| Forêt de Molitg-les-Bains ⚠️ | Molitg-les-Bains › Conflent-Canigó | 139 |
| Forêt de Corneilla-de-Conflent (19) ⚠️ | Corneilla-de-Conflent › Conflent-Canigó | 130 |
| Forêt de Feilluns ⚠️ | Feilluns › Agly Fenouillèdes | 128 |
| Forêt de Prats-de-Sournia ⚠️ | Prats-de-Sournia › Agly Fenouillèdes | 127 |
| Forêt de Bélesta (7) ⚠️ | Bélesta › Roussillon Conflent | 126 |
| Forêt de Oreilla | Olette › Conflent-Canigó | 124 |
| Forêt de la Matte | Les Angles › Pyrénées catalanes | 123 |
| Forêt de Py (7) | Py › Conflent-Canigó | 122 |
| Forêt de Nyer (6) | Nyer › Conflent-Canigó | 121 |
| Forêt de Taurinya | Taurinya › Conflent-Canigó | 118 |
| Forêt de Latour-de-Carol (3) | Latour-de-Carol › Pyrénées Cerdagne | 118 |
| Forêt de Souanyas (2) | Souanyas › Conflent-Canigó | 117 |
| Forêt de Nohèdes (3) | Nohèdes › Conflent-Canigó | 116 |
| Forêt de Porta (6) | Porta › Pyrénées Cerdagne | 114 |
| Forêt de Nohèdes (6) | Nohèdes › Conflent-Canigó | 113 |
| Forêt de Vivès | Vivès › Vallespir | 111 |
| Bois de Angoustrine-Villeneuve-des-Escaldes | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 111 |
| Forêt de Rasiguères | Rasiguères › Agly Fenouillèdes | 111 |
| Forêt de Rasiguères (2) | Rasiguères › Agly Fenouillèdes | 111 |
| Forêt de Mosset (3) | Mosset › Conflent-Canigó | 109 |
| Forêt de Céret | Céret › Vallespir | 108 |
| Forêt de Puyvalador (99) | Puyvalador › Pyrénées catalanes | 108 |
| Forêt de Dorres | Dorres › Pyrénées Cerdagne | 105 |
| Forêt de Vernet-les-Bains (10) | Vernet-les-Bains › Conflent-Canigó | 103 |
| Forêt de Bélesta (6) | Bélesta › Roussillon Conflent | 100 |
| Forêt de Mosset (6) | Mosset › Conflent-Canigó | 98 |
| Forêt de Serdinya (2) | Serdinya › Conflent-Canigó | 97 |
| Forêt de Py (2) | Py › Conflent-Canigó | 96 |
| Forêt de Coustouges | Coustouges › Haut-Vallespir | 94 |
| Forêt de Saint-Paul-de-Fenouillet (15) | Saint-Paul-de-Fenouillet › Agly Fenouillèdes | 94 |
| Forêt de Bélesta (5) | Bélesta › Roussillon Conflent | 94 |
| Forêt de Camélas (2) | Camélas › Aspres | 93 |
| Forêt de Porta (2) | Porta › Pyrénées Cerdagne | 92 |
| Forêt de Fontpédrouse (6) | Fontpédrouse › Conflent-Canigó | 92 |
| Forêt de Prats-de-Mollo-la-Preste (12) | Prats-de-Mollo-la-Preste › Haut-Vallespir | 92 |
| Forêt de Prats-de-Mollo-la-Preste (8) | Prats-de-Mollo-la-Preste › Haut-Vallespir | 87 |
| Forêt de Eus (2) | Eus › Conflent-Canigó | 87 |
| Forêt de Montalba-le-Château | Montalba-le-Château › Roussillon Conflent | 84 |
| Forêt de Camélas (11) | Camélas › Aspres | 84 |
| Forêt de Prats-de-Mollo-la-Preste (3) | Prats-de-Mollo-la-Preste › Haut-Vallespir | 83 |
| Forêt de Urbanya (3) | Urbanya › Conflent-Canigó | 82 |
| Forêt de Urbanya | Urbanya › Conflent-Canigó | 81 |
| Forêt de Souanyas | Souanyas › Conflent-Canigó | 80 |
| Forêt de Urbanya (2) | Urbanya › Conflent-Canigó | 79 |
| Forêt de Nohèdes (2) | Nohèdes › Conflent-Canigó | 79 |
| Forêt de Prats-de-Mollo-la-Preste (14) | Prats-de-Mollo-la-Preste › Haut-Vallespir | 79 |
| Forêt de Conat | Conat › Conflent-Canigó | 78 |
| Forêt de Montesquieu-des-Albères (3) | Montesquieu-des-Albères › Albères – Côte Vermeille – Illibéris | 78 |
| Forêt de Tautavel | Tautavel › Perpignan Méditerranée Métropole | 77 |
| Forêt de Sournia (5) | Sournia › Agly Fenouillèdes | 77 |
| Forêt de Sournia (6) | Sournia › Agly Fenouillèdes | 77 |
| Forêt de Mosset (22) | Mosset › Conflent-Canigó | 77 |
| Forêt de Maureillas-las-Illas (3) | Maureillas-las-Illas › Vallespir | 75 |
| Forêt de Banyuls-sur-Mer (39) | Banyuls-sur-Mer › Albères – Côte Vermeille – Illibéris | 75 |
| Forêt de Arboussols (2) | Arboussols › Conflent-Canigó | 73 |
| Forêt de Marquixanes | Marquixanes › Conflent-Canigó | 73 |
| Forêt de Fenouillet (30) | Fenouillet › Agly Fenouillèdes | 72 |
| Forêt de Porté-Puymorens (3) | Porté-Puymorens › Pyrénées Cerdagne | 71 |
| Forêt domaniale de Fontpédrouse | Planès › Pyrénées catalanes | 70 |
| Forêt de Py (4) | Py › Conflent-Canigó | 70 |
| Forêt de Py (6) | Py › Conflent-Canigó | 70 |
| Forêt de Eus | Eus › Conflent-Canigó | 69 |
| Forêt de Caramany | Caramany › Agly Fenouillèdes | 68 |
| Forêt de Corneilla-de-Conflent (2) | Corneilla-de-Conflent › Conflent-Canigó | 68 |
| Forêt de Angoustrine-Villeneuve-des-Escaldes | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 67 |
| Forêt de La Bastide | La Bastide › Haut-Vallespir | 67 |
| Forêt de Sournia (8) | Sournia › Agly Fenouillèdes | 67 |
| Forêt de Sournia (3) | Sournia › Agly Fenouillèdes | 66 |
| Bois de Opoul-Périllos (2) | Opoul-Périllos › Perpignan Méditerranée Métropole | 66 |
| Forêt de Finestret | Finestret › Conflent-Canigó | 66 |
| Forêt de Sansa (2) | Sansa › Pyrénées catalanes | 65 |
| Forêt de Puyvalador | Puyvalador › Pyrénées catalanes | 64 |
| Forêt de Salses-le-Château (2) | Salses-le-Château › Corbières Salanque Méditerranée | 64 |
| Forêt de Maury (2) | Maury › Agly Fenouillèdes | 64 |
| Forêt de Nohèdes (4) | Nohèdes › Conflent-Canigó | 62 |
| Forêt de Valmanya (2) | Valmanya › Conflent-Canigó | 61 |
| Forêt de Sahorre (5) | Sahorre › Conflent-Canigó | 61 |
| Forêt de Maureillas-las-Illas (2) | Maureillas-las-Illas › Vallespir | 61 |
| Forêt de Caudiès-de-Fenouillèdes (31) | Caudiès-de-Fenouillèdes › Agly Fenouillèdes | 60 |
| Forêt de Fenouillet (28) | Fenouillet › Agly Fenouillèdes | 60 |
| Forêt de Trévillach | Trévillach › Conflent-Canigó | 60 |
| Forêt de Fillols (3) | Fillols › Conflent-Canigó | 59 |
| Forêt de Sahorre (14) | Sahorre › Conflent-Canigó | 59 |
| Forêt de Ria-Sirach (2) | Ria-Sirach › Conflent-Canigó | 57 |
| Forêt de Espira-de-l'Agly (2) | Espira-de-l'Agly › Perpignan Méditerranée Métropole | 56 |
| Forêt de Font-Romeu-Odeillo-Via (3) | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 56 |
| Forêt de Fenouillet (19) | Fenouillet › Agly Fenouillèdes | 56 |
| Forêt de Tautavel (2) | Tautavel › Perpignan Méditerranée Métropole | 55 |
| Forêt de Valmanya (5) | Valmanya › Conflent-Canigó | 55 |
| Forêt de Lesquerde (2) | Lesquerde › Agly Fenouillèdes | 55 |
| Forêt de Taurinya (2) | Taurinya › Conflent-Canigó | 53 |
| Forêt de Fontpédrouse (5) | Fontpédrouse › Conflent-Canigó | 52 |
| Forêt de Escaro (4) | Escaro › Conflent-Canigó | 52 |
| Forêt de Cerbère | Cerbère › Albères – Côte Vermeille – Illibéris | 52 |
| Forêt de Caudiès-de-Fenouillèdes (28) | Caudiès-de-Fenouillèdes › Agly Fenouillèdes | 52 |
| Forêt de Fenouillet | Fenouillet › Agly Fenouillèdes | 51 |
| Forêt de Mosset (4) | Mosset › Conflent-Canigó | 51 |
| Forêt de Escaro (2) | Escaro › Conflent-Canigó | 51 |
| Forêt de Bélesta | Bélesta › Roussillon Conflent | 51 |
| Forêt de Sournia (4) | Sournia › Agly Fenouillèdes | 51 |
| Forêt de Sahorre (6) | Sahorre › Conflent-Canigó | 51 |
| Forêt de Cassagnes (5) | Cassagnes › Perpignan Méditerranée Métropole | 51 |
| Forêt de Saint-Pierre-dels-Forcats (45) | Saint-Pierre-dels-Forcats › Pyrénées catalanes | 51 |
| Forêt de Prats-de-Mollo-la-Preste (4) | Prats-de-Mollo-la-Preste › Haut-Vallespir | 50 |
| Bois de Opoul-Périllos | Opoul-Périllos › Perpignan Méditerranée Métropole | 50 |
| Forêt de Caudiès-de-Fenouillèdes (24) | Caudiès-de-Fenouillèdes › Agly Fenouillèdes | 50 |
| Forêt de Saint-Martin-de-Fenouillet (2) | Saint-Martin-de-Fenouillet › Agly Fenouillèdes | 50 |
| Forêt de Campoussy | Campoussy › Agly Fenouillèdes | 49 |
| Forêt de Mosset (9) | Mosset › Conflent-Canigó | 48 |
| Forêt de Mosset (14) | Mosset › Conflent-Canigó | 48 |
| Forêt de Prades | Prades › Conflent-Canigó | 48 |
| Forêt de Sahorre (2) | Sahorre › Conflent-Canigó | 47 |
| Forêt de Rabouillet (2) | Rabouillet › Agly Fenouillèdes | 45 |
| Forêt de Saint-Paul-de-Fenouillet (10) | Saint-Paul-de-Fenouillet › Agly Fenouillèdes | 45 |
| Forêt de Los Masos | Los Masos › Conflent-Canigó | 44 |
| Forêt de Caudiès-de-Fenouillèdes (2) | Caudiès-de-Fenouillèdes › Agly Fenouillèdes | 44 |
| Forêt de Urbanya (4) | Urbanya › Conflent-Canigó | 44 |
| Forêt de Fuilla (17) | Fuilla › Conflent-Canigó | 44 |
| Forêt de Mosset (2) | Mosset › Conflent-Canigó | 43 |
| Forêt de Vernet-les-Bains | Vernet-les-Bains › Conflent-Canigó | 43 |
| Forêt de Escaro | Escaro › Conflent-Canigó | 43 |
| Forêt de Eyne (5) | Eyne › Pyrénées catalanes | 43 |
| Bois de Néfiach (5) | Néfiach › Roussillon Conflent | 43 |
| Forêt de Prats-de-Mollo-la-Preste (2) | Prats-de-Mollo-la-Preste › Haut-Vallespir | 42 |
| Forêt de Opoul-Périllos | Opoul-Périllos › Perpignan Méditerranée Métropole | 41 |
| Forêt de Sournia (2) | Sournia › Agly Fenouillèdes | 41 |
| Forêt de Font-Romeu-Odeillo-Via | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 41 |
| Forêt de Jujols | Jujols › Conflent-Canigó | 41 |
| Forêt de Railleu | Railleu › Pyrénées catalanes | 40 |
| Forêt de Tordères | Tordères › Aspres | 40 |
| Forêt de Rasiguères (3) | Rasiguères › Agly Fenouillèdes | 40 |
| Forêt de Dorres (2) | Dorres › Pyrénées Cerdagne | 39 |
| Forêt de Nyer (3) | Nyer › Conflent-Canigó | 38 |
| Forêt de Cases-de-Pène | Cases-de-Pène › Perpignan Méditerranée Métropole | 38 |
| Forêt de Mosset (12) | Mosset › Conflent-Canigó | 38 |
| Forêt de Mosset (13) | Mosset › Conflent-Canigó | 38 |
| Forêt de Font-Romeu-Odeillo-Via (4) | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 38 |
| Forêt de Escaro (5) | Escaro › Conflent-Canigó | 38 |
| Forêt de Prades (16) | Prades › Conflent-Canigó | 38 |
| Forêt de Espira-de-Conflent (2) | Espira-de-Conflent › Conflent-Canigó | 37 |
| Forêt de Eyne (2) | Eyne › Pyrénées catalanes | 37 |
| Forêt de Caudiès-de-Fenouillèdes (12) | Caudiès-de-Fenouillèdes › Agly Fenouillèdes | 37 |
| Forêt de Fosse | Fosse › Agly Fenouillèdes | 37 |
| Forêt de Lesquerde | Lesquerde › Agly Fenouillèdes | 37 |
| Forêt de Palau-de-Cerdagne (6) | Palau-de-Cerdagne › Pyrénées Cerdagne | 37 |
| Forêt de Estoher | Estoher › Conflent-Canigó | 36 |
| Forêt de Maureillas-las-Illas (7) | Maureillas-las-Illas › Vallespir | 36 |
| Forêt de Camélas | Camélas › Aspres | 35 |
| Forêt de Valmanya | Valmanya › Conflent-Canigó | 35 |
| Forêt de Thuès-Entre-Valls (2) | Thuès-Entre-Valls › Conflent-Canigó | 35 |
| Forêt de Glorianes | Glorianes › Roussillon Conflent | 35 |
| Forêt de Porté-Puymorens (5) | Porté-Puymorens › Pyrénées Cerdagne | 35 |
| Forêt de Casefabre (2) | Casefabre › Roussillon Conflent | 35 |
| Forêt de Cassagnes (3) | Cassagnes › Perpignan Méditerranée Métropole | 35 |
| Forêt de Vernet-les-Bains (9) | Vernet-les-Bains › Conflent-Canigó | 35 |
| Forêt de Saint-Laurent-de-Cerdans (5) | Saint-Laurent-de-Cerdans › Haut-Vallespir | 35 |
| Forêt de Sansa | Sansa › Pyrénées catalanes | 34 |
| Forêt de Salses-le-Château (4) | Salses-le-Château › Corbières Salanque Méditerranée | 34 |
| Forêt de Espira-de-Conflent | Espira-de-Conflent › Conflent-Canigó | 34 |
| Forêt de Villefranche-de-Conflent (2) | Villefranche-de-Conflent › Conflent-Canigó | 34 |
| Forêt de Porté-Puymorens (2) | Porté-Puymorens › Pyrénées Cerdagne | 34 |
| Forêt de Montauriol | Montauriol › Aspres | 33 |
| Forêt de Olette (2) | Olette › Conflent-Canigó | 33 |
| Forêt de Saint-Arnac | Saint-Arnac › Agly Fenouillèdes | 33 |
| Forêt de Caudiès-de-Fenouillèdes (20) | Caudiès-de-Fenouillèdes › Agly Fenouillèdes | 33 |
| Forêt de Reynès | Reynès › Vallespir | 33 |
| Forêt de Jujols (2) | Jujols › Conflent-Canigó | 32 |
| Forêt de Saint-Martin-de-Fenouillet (3) | Saint-Martin-de-Fenouillet › Agly Fenouillèdes | 32 |
| Forêt de Cassagnes | Cassagnes › Perpignan Méditerranée Métropole | 31 |
| Forêt de Opoul-Périllos (2) | Opoul-Périllos › Perpignan Méditerranée Métropole | 31 |
| Forêt de Serdinya (4) | Serdinya › Conflent-Canigó | 31 |
| Forêt de Mosset (19) | Mosset › Conflent-Canigó | 31 |
| Forêt de Targasonne (5) | Targasonne › Pyrénées Cerdagne | 31 |
| Forêt de Serdinya | Serdinya › Conflent-Canigó | 30 |
| Forêt de Escaro (3) | Escaro › Conflent-Canigó | 30 |
| Forêt de Enveitg (2) | Enveitg › Pyrénées Cerdagne | 30 |
| Forêt de Prats-de-Mollo-la-Preste (6) | Prats-de-Mollo-la-Preste › Haut-Vallespir | 30 |
| Bois de Oms | Oms › Aspres | 30 |
| Forêt de Espira-de-l'Agly | Espira-de-l'Agly › Perpignan Méditerranée Métropole | 29 |
| Forêt de Sahorre | Sahorre › Conflent-Canigó | 29 |
| Forêt de Enveitg (3) | Enveitg › Pyrénées Cerdagne | 29 |
| Forêt de Enveitg (4) | Enveitg › Pyrénées Cerdagne | 29 |
| Forêt de Py (8) | Py › Conflent-Canigó | 29 |
| Forêt de Sournia (7) | Sournia › Agly Fenouillèdes | 29 |
| Forêt de Ille-sur-Têt | Ille-sur-Têt › Roussillon Conflent | 29 |
| Forêt de Casteil (3) | Casteil › Conflent-Canigó | 29 |
| Forêt de Nyer (2) | Nyer › Conflent-Canigó | 28 |
| Forêt de Montesquieu-des-Albères | Montesquieu-des-Albères › Albères – Côte Vermeille – Illibéris | 28 |
| Forêt du Vivier | Le Vivier › Agly Fenouillèdes | 28 |
| Forêt de Puyvalador (96) | Puyvalador › Pyrénées catalanes | 28 |
| Forêt du Perthus | Le Perthus › Vallespir | 27 |
| Forêt de Nohèdes | Nohèdes › Conflent-Canigó | 27 |
| Forêt de Sansa (3) | Sansa › Pyrénées catalanes | 27 |
| Forêt de Sahorre (4) | Sahorre › Conflent-Canigó | 27 |
| Forêt de Taurinya (3) | Taurinya › Conflent-Canigó | 27 |
| Forêt des Angles (177) | Les Angles › Pyrénées catalanes | 27 |
| Forêt de Rabouillet | Rabouillet › Agly Fenouillèdes | 26 |
| Forêt de Fontpédrouse (3) | Fontpédrouse › Conflent-Canigó | 26 |
| Forêt de Corsavy (6) | Corsavy › Haut-Vallespir | 26 |
| Forêt de Ria-Sirach (7) | Ria-Sirach › Conflent-Canigó | 26 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (148) | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 26 |
| Chemin de l'Église Saint-Étienne | Sahorre › Conflent-Canigó | 26 |
| Forêt de Baillestavy | Baillestavy › Conflent-Canigó | 26 |
| Bois de Caramany (6) | Caramany › Agly Fenouillèdes | 26 |
| Forêt de Villefranche-de-Conflent | Villefranche-de-Conflent › Conflent-Canigó | 25 |
| Forêt de Campôme | Campôme › Conflent-Canigó | 25 |
| Forêt de Fillols | Fillols › Conflent-Canigó | 25 |
| Forêt de Corneilla-de-Conflent (4) | Corneilla-de-Conflent › Conflent-Canigó | 25 |
| Forêt de Prats-de-Mollo-la-Preste (17) | Prats-de-Mollo-la-Preste › Haut-Vallespir | 25 |
| Forêt de Saint-Laurent-de-Cerdans | Saint-Laurent-de-Cerdans › Haut-Vallespir | 25 |
| Bois de Latour-de-France | Latour-de-France › Agly Fenouillèdes | 25 |
| Forêt de Égat | Égat › Pyrénées Cerdagne | 25 |
| Forêt de Eyne (15) | Eyne › Pyrénées catalanes | 25 |
| Forêt de Rabouillet (3) | Rabouillet › Agly Fenouillèdes | 25 |
| Forêt de Corneilla-de-Conflent (22) | Corneilla-de-Conflent › Conflent-Canigó | 25 |
| Forêt de Porta | Porta › Pyrénées Cerdagne | 24 |
| Forêt de Nyer (7) | Nyer › Conflent-Canigó | 24 |
| Forêt de Porta (5) | Porta › Pyrénées Cerdagne | 24 |
| Forêt de Saint-Martin-de-Fenouillet | Saint-Martin-de-Fenouillet › Agly Fenouillèdes | 24 |
| Forêt de Maury (3) | Maury › Agly Fenouillèdes | 24 |
| Forêt de Puyvalador (98) | Puyvalador › Pyrénées catalanes | 24 |
| Forêt de Arboussols | Arboussols › Conflent-Canigó | 23 |
| Forêt de Prats-de-Mollo-la-Preste | Prats-de-Mollo-la-Preste › Haut-Vallespir | 23 |
| Forêt de Valmanya (4) | Valmanya › Conflent-Canigó | 23 |
| Forêt de Clara-Villerach | Clara-Villerach › Conflent-Canigó | 23 |
| Forêt de Clara-Villerach (2) | Clara-Villerach › Conflent-Canigó | 23 |
| Forêt de Maury | Maury › Agly Fenouillèdes | 23 |
| Forêt de Maureillas-las-Illas (6) | Maureillas-las-Illas › Vallespir | 23 |
| Forêt de Saint-Laurent-de-Cerdans (7) | Saint-Laurent-de-Cerdans › Haut-Vallespir | 23 |
| Forêt de Vernet-les-Bains (13) | Vernet-les-Bains › Conflent-Canigó | 23 |
| Forêt de Puyvalador (2) | Puyvalador › Pyrénées catalanes | 22 |
| Forêt de Serdinya (3) | Serdinya › Conflent-Canigó | 22 |
| Forêt de Fillols (2) | Fillols › Conflent-Canigó | 22 |
| Forêt de Mantet | Mantet › Conflent-Canigó | 22 |
| Forêt de Laroque-des-Albères (2) | Laroque-des-Albères › Albères – Côte Vermeille – Illibéris | 22 |
| Forêt de Nohèdes (5) | Nohèdes › Conflent-Canigó | 22 |
| Forêt de Catllar (5) | Catllar › Conflent-Canigó | 22 |
| Forêt de Corneilla-de-Conflent (14) | Corneilla-de-Conflent › Conflent-Canigó | 22 |
| Forêt de Cases-de-Pène (3) | Cases-de-Pène › Perpignan Méditerranée Métropole | 22 |
| Bois de Montalba-le-Château | Montalba-le-Château › Roussillon Conflent | 22 |
| Forêt de Montbolo | Montbolo › Haut-Vallespir | 21 |
| Forêt de Maureillas-las-Illas | Maureillas-las-Illas › Vallespir | 21 |
| Forêt de Prats-de-Mollo-la-Preste (5) | Prats-de-Mollo-la-Preste › Haut-Vallespir | 21 |
| Forêt de Enveitg (5) | Enveitg › Pyrénées Cerdagne | 21 |
| Forêt de Espira-de-l'Agly (4) | Espira-de-l'Agly › Perpignan Méditerranée Métropole | 21 |
| Forêt de Castelnou (3) | Castelnou › Aspres | 21 |
| Forêt de Maureillas-las-Illas (8) | Maureillas-las-Illas › Vallespir | 21 |
| Forêt de Olette | Olette › Conflent-Canigó | 20 |
| Forêt de Nyer | Nyer › Conflent-Canigó | 20 |
| Forêt de Mosset (10) | Mosset › Conflent-Canigó | 20 |
| Forêt de Conat (2) | Conat › Conflent-Canigó | 20 |
| Forêt de Conat (3) | Conat › Conflent-Canigó | 20 |
| Forêt de Nyer (8) | Nyer › Conflent-Canigó | 20 |
| Forêt de Fontpédrouse (7) | Fontpédrouse › Conflent-Canigó | 20 |
| Forêt de Mosset (16) | Mosset › Conflent-Canigó | 20 |
| Forêt de Eus (6) | Eus › Conflent-Canigó | 20 |
| Forêt de Bélesta (2) | Bélesta › Roussillon Conflent | 20 |
| Forêt de Palau-de-Cerdagne (2) | Palau-de-Cerdagne › Pyrénées Cerdagne | 20 |
| Forêt de Amélie-les-Bains-Palalda | Amélie-les-Bains-Palalda › Haut-Vallespir | 20 |
| Forêt de Corsavy (3) | Corsavy › Haut-Vallespir | 19 |
| Forêt de Prats-de-Mollo-la-Preste (21) | Prats-de-Mollo-la-Preste › Haut-Vallespir | 19 |
| Bois de Montesquieu-des-Albères | Montesquieu-des-Albères › Albères – Côte Vermeille – Illibéris | 19 |
| Bois de Calmeilles | Calmeilles › Aspres | 19 |
| Forêt de Saint-Paul-de-Fenouillet (16) | Saint-Paul-de-Fenouillet › Agly Fenouillèdes | 19 |
| Forêt de Cassagnes (7) | Cassagnes › Perpignan Méditerranée Métropole | 19 |
| Forêt de Mosset (5) | Mosset › Conflent-Canigó | 18 |
| Forêt de Vivès (2) | Vivès › Vallespir | 18 |
| Forêt de Fillols (4) | Fillols › Conflent-Canigó | 18 |
| Forêt des Angles (6) | Les Angles › Pyrénées catalanes | 18 |
| Bois de Porta | Porta › Pyrénées Cerdagne | 18 |
| Forêt de Saillagouse (6) | Saillagouse › Pyrénées Cerdagne | 18 |
| Forêt de Corneilla-de-Conflent | Corneilla-de-Conflent › Conflent-Canigó | 17 |
| Forêt de Fuilla | Fuilla › Conflent-Canigó | 17 |
| Forêt de Estavar | Estavar › Pyrénées Cerdagne | 17 |
| Forêt de Montbolo (2) | Montbolo › Haut-Vallespir | 17 |
| Forêt de Corsavy (5) | Corsavy › Haut-Vallespir | 17 |
| Forêt de Salses-le-Château (5) | Salses-le-Château › Corbières Salanque Méditerranée | 17 |
| Forêt de Tordères (2) | Tordères › Aspres | 17 |
| Forêt de Sorède | Sorède › Albères – Côte Vermeille – Illibéris | 17 |
| Forêt de Estavar (2) | Estavar › Pyrénées Cerdagne | 17 |
| Bois de Mantet (6) | Mantet › Conflent-Canigó | 17 |
| Forêt de Enveitg | Enveitg › Pyrénées Cerdagne | 16 |
| Forêt de Sournia | Sournia › Agly Fenouillèdes | 16 |
| Forêt de Mantet (2) | Mantet › Conflent-Canigó | 16 |
| Forêt de Serralongue | Serralongue › Haut-Vallespir | 16 |
| Forêt de Collioure | Collioure › Albères – Côte Vermeille – Illibéris | 16 |
| Forêt de Arboussols (3) | Arboussols › Conflent-Canigó | 16 |
| Forêt de Py (9) | Py › Conflent-Canigó | 16 |
| Forêt de Catllar (4) | Catllar › Conflent-Canigó | 16 |
| Forêt de Cassagnes (4) | Cassagnes › Perpignan Méditerranée Métropole | 16 |
| Forêt de Prugnanes | Prugnanes › Agly Fenouillèdes | 15 |
| Forêt de Urbanya (5) | Urbanya › Conflent-Canigó | 15 |
| Forêt de Montferrer | Montferrer › Haut-Vallespir | 15 |
| Forêt de Prats-de-Mollo-la-Preste (16) | Prats-de-Mollo-la-Preste › Haut-Vallespir | 15 |
| Forêt de Prats-de-Mollo-la-Preste (22) | Prats-de-Mollo-la-Preste › Haut-Vallespir | 15 |
| Forêt de Argelès-sur-Mer (2) | Argelès-sur-Mer › Albères – Côte Vermeille – Illibéris | 15 |
| Bois de Banyuls-sur-Mer | Banyuls-sur-Mer › Albères – Côte Vermeille – Illibéris | 15 |
| Forêt de Ortaffa | Ortaffa › Albères – Côte Vermeille – Illibéris | 15 |
| Forêt de Ria-Sirach (3) | Ria-Sirach › Conflent-Canigó | 15 |
| Forêt de Fuilla (11) | Fuilla › Conflent-Canigó | 15 |
| Forêt de Err (24) | Err › Pyrénées Cerdagne | 15 |
| Forêt de Saint-Paul-de-Fenouillet | Saint-Paul-de-Fenouillet › Agly Fenouillèdes | 15 |
| Forêt de Cases-de-Pène (4) | Cases-de-Pène › Perpignan Méditerranée Métropole | 15 |
| Forêt de Banyuls-sur-Mer (2) | Banyuls-sur-Mer › Albères – Côte Vermeille – Illibéris | 15 |
| Forêt de Fenouillet (31) | Fenouillet › Agly Fenouillèdes | 15 |
| Forêt de Banyuls-sur-Mer (37) | Banyuls-sur-Mer › Albères – Côte Vermeille – Illibéris | 15 |
| Forêt de Caramany (10) | Caramany › Agly Fenouillèdes | 15 |
| Pinède Mas de l'Isle | Le Barcarès › Perpignan Méditerranée Métropole | 14 |
| Forêt de Brouilla | Brouilla › Aspres | 14 |
| Forêt de Corsavy (4) | Corsavy › Haut-Vallespir | 14 |
| Forêt de Laroque-des-Albères | Laroque-des-Albères › Albères – Côte Vermeille – Illibéris | 14 |
| Forêt de Prats-de-Mollo-la-Preste (7) | Prats-de-Mollo-la-Preste › Haut-Vallespir | 14 |
| Forêt de Font-Romeu-Odeillo-Via (2) | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 14 |
| Forêt de Corbère-les-Cabanes (2) | Corbère-les-Cabanes › Roussillon Conflent | 14 |
| Forêt de Ria-Sirach | Ria-Sirach › Conflent-Canigó | 14 |
| Forêt de Nyer (9) | Nyer › Conflent-Canigó | 14 |
| Forêt de Corneilla-de-Conflent (13) | Corneilla-de-Conflent › Conflent-Canigó | 14 |
| Bois de Pézilla-la-Rivière | Pézilla-la-Rivière › Perpignan Méditerranée Métropole | 14 |
| Forêt de Montesquieu-des-Albères (2) | Montesquieu-des-Albères › Albères – Côte Vermeille – Illibéris | 14 |
| Forêt de Camélas (3) | Camélas › Aspres | 14 |
| Forêt de Fontpédrouse (4) | Fontpédrouse › Conflent-Canigó | 13 |
| Forêt de Nyer (4) | Nyer › Conflent-Canigó | 13 |
| Forêt de Llo | Llo › Pyrénées Cerdagne | 13 |
| Forêt de Mosset (11) | Mosset › Conflent-Canigó | 13 |
| Forêt de Mantet (5) | Mantet › Conflent-Canigó | 13 |
| Forêt de Prats-de-Mollo-la-Preste (15) | Prats-de-Mollo-la-Preste › Haut-Vallespir | 13 |
| Forêt de Prats-de-Mollo-la-Preste (18) | Prats-de-Mollo-la-Preste › Haut-Vallespir | 13 |
| Forêt de Cassagnes (2) | Cassagnes › Perpignan Méditerranée Métropole | 13 |
| Forêt de Espira-de-l'Agly (5) | Espira-de-l'Agly › Perpignan Méditerranée Métropole | 13 |
| Forêt de Saint-Pierre-dels-Forcats (16) | Saint-Pierre-dels-Forcats › Pyrénées catalanes | 13 |
| Forêt de Caudiès-de-Fenouillèdes (6) | Caudiès-de-Fenouillèdes › Agly Fenouillèdes | 13 |
| Forêt de Coustouges (3) | Coustouges › Haut-Vallespir | 13 |
| Forêt de Coustouges (5) | Coustouges › Haut-Vallespir | 13 |
| Forêt de Corsavy (2) | Corsavy › Haut-Vallespir | 12 |
| Forêt de La Cabanasse | La Cabanasse › Pyrénées catalanes | 12 |
| Forêt de Valcebollère | Valcebollère › Pyrénées Cerdagne | 12 |
| Forêt du Tech | Le Tech › Haut-Vallespir | 12 |
| Forêt de Llo (2) | Llo › Pyrénées Cerdagne | 12 |
| Forêt de Prats-de-Mollo-la-Preste (20) | Prats-de-Mollo-la-Preste › Haut-Vallespir | 12 |
| Forêt de Espira-de-l'Agly (3) | Espira-de-l'Agly › Perpignan Méditerranée Métropole | 12 |
| Forêt de Ria-Sirach (5) | Ria-Sirach › Conflent-Canigó | 12 |
| Forêt de Formiguères (27) | Formiguères › Pyrénées catalanes | 12 |
| Forêt de Fenouillet (9) | Fenouillet › Agly Fenouillèdes | 12 |
| Forêt de Peyrestortes | Peyrestortes › Perpignan Méditerranée Métropole | 12 |
| Bois de Saint-Jean-Pla-de-Corts | Saint-Jean-Pla-de-Corts › Vallespir | 12 |
| Forêt de Caudiès-de-Fenouillèdes (29) | Caudiès-de-Fenouillèdes › Agly Fenouillèdes | 12 |
| Bois de Mantet (3) | Mantet › Conflent-Canigó | 12 |
| Bois de Caramany (5) | Caramany › Agly Fenouillèdes | 12 |
| Forêt de l'Albère (3) | L'Albère › Vallespir | 12 |
| Forêt de Prats-de-Mollo-la-Preste (19) | Prats-de-Mollo-la-Preste › Haut-Vallespir | 11 |
| Forêt de Argelès-sur-Mer | Argelès-sur-Mer › Albères – Côte Vermeille – Illibéris | 11 |
| Forêt des Angles (18) | Les Angles › Pyrénées catalanes | 11 |
| Forêt de Oms (7) | Oms › Aspres | 11 |
| Forêt de Corneilla-de-Conflent (20) | Vernet-les-Bains › Conflent-Canigó | 11 |
| Forêt de Caudiès-de-Fenouillèdes | Caudiès-de-Fenouillèdes › Agly Fenouillèdes | 10 |
| Forêt de Porta (3) | Porta › Pyrénées Cerdagne | 10 |
| Forêt de Puyvalador (3) | Puyvalador › Pyrénées catalanes | 10 |
| Forêt de Sansa (4) | Sansa › Pyrénées catalanes | 10 |
| Forêt de Saint-Laurent-de-Cerdans (2) | Saint-Laurent-de-Cerdans › Haut-Vallespir | 10 |
| Bois de Estagel | Latour-de-France › Agly Fenouillèdes | 10 |
| Espace Sportif de la Prade | Saint-Cyprien › Sud-Roussillon | 10 |
| Forêt de Arboussols (4) | Arboussols › Conflent-Canigó | 10 |
| Forêt de Réal (4) | Réal › Pyrénées catalanes | 10 |
| Forêt de Céret (2) | Céret › Vallespir | 10 |
| Bois de Vingrau (5) | Vingrau › Perpignan Méditerranée Métropole | 10 |
| Forêt de Cases-de-Pène (2) | Cases-de-Pène › Perpignan Méditerranée Métropole | 10 |
| Bois de Argelès-sur-Mer (7) | Argelès-sur-Mer › Albères – Côte Vermeille – Illibéris | 10 |
| Forêt des Angles (183) | Les Angles › Pyrénées catalanes | 10 |
| Bois de Prats-de-Mollo-la-Preste | Prats-de-Mollo-la-Preste › Haut-Vallespir | 10 |
| Forêt de Canet-en-Roussillon ⚠️ | Sainte-Marie-la-Mer › Perpignan Méditerranée Métropole | 9 |
| Forêt de Corneilla-de-Conflent (9) ⚠️ | Corneilla-de-Conflent › Conflent-Canigó | 9 |
| Forêt de Montesquieu-des-Albères (4) ⚠️ | Montesquieu-des-Albères › Albères – Côte Vermeille – Illibéris | 9 |
| Forêt de Montesquieu-des-Albères (5) ⚠️ | Montesquieu-des-Albères › Albères – Côte Vermeille – Illibéris | 9 |
| Forêt de Camélas (9) ⚠️ | Camélas › Aspres | 9 |
| Forêt de Prugnanes (3) ⚠️ | Prugnanes › Agly Fenouillèdes | 9 |
| Forêt de Tautavel (3) ⚠️ | Tautavel › Perpignan Méditerranée Métropole | 9 |
| Forêt de Formiguères (338) ⚠️ | Formiguères › Pyrénées catalanes | 9 |
| Bois de Porté-Puymorens (49) ⚠️ | Porté-Puymorens › Pyrénées Cerdagne | 9 |
| Forêt de Prades (15) ⚠️ | Prades › Conflent-Canigó | 9 |
| Forêt de Tautavel (4) ⚠️ | Tautavel › Perpignan Méditerranée Métropole | 9 |
| Forêt de Eus (4) ⚠️ | Eus › Conflent-Canigó | 8 |
| Forêt de Argelès-sur-Mer (4) ⚠️ | Argelès-sur-Mer › Albères – Côte Vermeille – Illibéris | 8 |
| Forêt Noire ⚠️ | Caudiès-de-Fenouillèdes › Agly Fenouillèdes | 8 |
| Forêt de Caudiès-de-Fenouillèdes (10) ⚠️ | Caudiès-de-Fenouillèdes › Agly Fenouillèdes | 8 |
| Forêt de Caudiès-de-Fenouillèdes (16) ⚠️ | Caudiès-de-Fenouillèdes › Agly Fenouillèdes | 8 |
| Forêt du Vivier (4) ⚠️ | Le Vivier › Agly Fenouillèdes | 8 |
| Bois de Porté-Puymorens ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 8 |
| Bois de Porté-Puymorens (2) ⚠️ | Porté-Puymorens › Pyrénées Cerdagne | 8 |
| Bois de Formiguères (3) ⚠️ | Formiguères › Pyrénées catalanes | 8 |
| Forêt de Marquixanes (2) ⚠️ | Marquixanes › Conflent-Canigó | 8 |
| Forêt des Angles (178) ⚠️ | Les Angles › Pyrénées catalanes | 8 |
| Forêt de Porté-Puymorens ⚠️ | Porté-Puymorens › Pyrénées Cerdagne | 7 |
| Forêt de Corneilla-de-Conflent (5) ⚠️ | Corneilla-de-Conflent › Conflent-Canigó | 7 |
| Forêt de Font-Romeu-Odeillo-Via (68) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 7 |
| Forêt de Err (15) ⚠️ | Err › Pyrénées Cerdagne | 7 |
| Forêt de Err (20) ⚠️ | Err › Pyrénées Cerdagne | 7 |
| Forêt de Porté-Puymorens (20) ⚠️ | Porté-Puymorens › Pyrénées Cerdagne | 7 |
| La Pinède (3) ⚠️ | Saint-Estève › Perpignan Méditerranée Métropole | 7 |
| Forêt de Argelès-sur-Mer (6) ⚠️ | Argelès-sur-Mer › Albères – Côte Vermeille – Illibéris | 7 |
| Forêt de Laroque-des-Albères (6) ⚠️ | Laroque-des-Albères › Albères – Côte Vermeille – Illibéris | 7 |
| Bois de Oms (30) ⚠️ | Oms › Aspres | 7 |
| Forêt de Castelnou ⚠️ | Castelnou › Aspres | 7 |
| Forêt de Saint-Paul-de-Fenouillet (5) ⚠️ | Saint-Paul-de-Fenouillet › Agly Fenouillèdes | 7 |
| Forêt d'Aiguebonnes ⚠️ | Fenouillet › Agly Fenouillèdes | 7 |
| Forêt de Fenouillet (25) ⚠️ | Fenouillet › Agly Fenouillèdes | 7 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (205) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 7 |
| Bois de Caramany ⚠️ | Caramany › Agly Fenouillèdes | 7 |
| Forêt de Bourg-Madame (3) ⚠️ | Bourg-Madame › Pyrénées Cerdagne | 7 |
| Bois de Argelès-sur-Mer (8) ⚠️ | Argelès-sur-Mer › Albères – Côte Vermeille – Illibéris | 7 |
| Forêt de Cases-de-Pène (5) ⚠️ | Cases-de-Pène › Perpignan Méditerranée Métropole | 7 |
| Forêt de Eus (8) ⚠️ | Eus › Conflent-Canigó | 7 |
| Forêt de Vernet-les-Bains (12) ⚠️ | Vernet-les-Bains › Conflent-Canigó | 7 |
| Forêt de Rodès (6) ⚠️ | Rodès › Roussillon Conflent | 7 |
| Parc des Sports et Loisirs Gabriel Sola ⚠️ | Bompas › Perpignan Méditerranée Métropole | 6 |
| Forêt de Corneilla-de-Conflent (3) ⚠️ | Corneilla-de-Conflent › Conflent-Canigó | 6 |
| Forêt de Mosset (17) ⚠️ | Mosset › Conflent-Canigó | 6 |
| Forêt de Font-Romeu-Odeillo-Via (132) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 6 |
| Forêt de Saint-Pierre-dels-Forcats (32) ⚠️ | Saint-Pierre-dels-Forcats › Pyrénées catalanes | 6 |
| Forêt de Formiguères (22) ⚠️ | Formiguères › Pyrénées catalanes | 6 |
| Forêt de Porta (15) ⚠️ | Porta › Pyrénées Cerdagne | 6 |
| Bois de Saint-Jean-Pla-de-Corts (6) ⚠️ | Saint-Jean-Pla-de-Corts › Vallespir | 6 |
| Bois de Céret (8) ⚠️ | Céret › Vallespir | 6 |
| Bois de Oms (21) ⚠️ | Oms › Aspres | 6 |
| Bois de Calmeilles (6) ⚠️ | Calmeilles › Aspres | 6 |
| Forêt de Camélas (6) ⚠️ | Camélas › Aspres | 6 |
| Bois de Néfiach ⚠️ | Néfiach › Roussillon Conflent | 6 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (150) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 6 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (199) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 6 |
| Bois de Palau-del-Vidre ⚠️ | Palau-del-Vidre › Albères – Côte Vermeille – Illibéris | 6 |
| Forêt de Bélesta (4) ⚠️ | Bélesta › Roussillon Conflent | 6 |
| Bois de Bélesta (3) ⚠️ | Bélesta › Roussillon Conflent | 6 |
| Forêt de Font-Romeu-Odeillo-Via (218) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 6 |
| Forêt de Rigarda (2) ⚠️ | Rigarda › Conflent-Canigó | 6 |
| Forêt de Matemale (37) ⚠️ | Matemale › Pyrénées catalanes | 6 |
| Forêt du Perthus (4) ⚠️ | Le Perthus › Vallespir | 6 |
| Forêt de Latour-de-Carol (2) ⚠️ | Latour-de-Carol › Pyrénées Cerdagne | 6 |
| Forêt de Sahorre (3) ⚠️ | Fuilla › Conflent-Canigó | 5 |
| Parcours Sportif Paysager de Sainte-Camille ⚠️ | Cabestany › Perpignan Méditerranée Métropole | 5 |
| Forêt de Ria-Sirach (4) ⚠️ | Ria-Sirach › Conflent-Canigó | 5 |
| Forêt de Fuilla (9) ⚠️ | Fuilla › Conflent-Canigó | 5 |
| Bois de Mont-Louis ⚠️ | Sauto › Pyrénées catalanes | 5 |
| Forêt de Bolquère (14) ⚠️ | Bolquère › Pyrénées catalanes | 5 |
| Forêt de Font-Romeu-Odeillo-Via (202) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 5 |
| Forêt de Puyvalador (4) ⚠️ | Puyvalador › Pyrénées catalanes | 5 |
| Forêt de Puyvalador (18) ⚠️ | Puyvalador › Pyrénées catalanes | 5 |
| Forêt de Puyvalador (32) ⚠️ | Puyvalador › Pyrénées catalanes | 5 |
| arboretum ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 5 |
| Forêt de Argelès-sur-Mer (5) ⚠️ | Argelès-sur-Mer › Albères – Côte Vermeille – Illibéris | 5 |
| Forêt de Fenouillet (13) ⚠️ | Fenouillet › Agly Fenouillèdes | 5 |
| Parc de Port-Vendres ⚠️ | Port-Vendres › Albères – Côte Vermeille – Illibéris | 5 |
| Bois de Céret ⚠️ | Céret › Vallespir | 5 |
| Forêt de Taurinya (4) ⚠️ | Taurinya › Conflent-Canigó | 5 |
| Bois de Calmeilles (4) ⚠️ | Calmeilles › Aspres | 5 |
| Forêt de Casefabre ⚠️ | Casefabre › Roussillon Conflent | 5 |
| Bois du Soler (2) ⚠️ | Le Soler › Perpignan Méditerranée Métropole | 5 |
| Forêt du Soler (9) ⚠️ | Le Soler › Perpignan Méditerranée Métropole | 5 |
| Forêt de Saint-Paul-de-Fenouillet (4) ⚠️ | Saint-Paul-de-Fenouillet › Agly Fenouillèdes | 5 |
| Forêt de Fenouillet (21) ⚠️ | Fenouillet › Agly Fenouillèdes | 5 |
| Forêt de Fenouillet (22) ⚠️ | Fenouillet › Agly Fenouillèdes | 5 |
| Forêt de Fenouillet (27) ⚠️ | Fenouillet › Agly Fenouillèdes | 5 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (183) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 5 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (189) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 5 |
| Bois de Fontpédrouse ⚠️ | Fontpédrouse › Conflent-Canigó | 5 |
| Forêt de Font-Romeu-Odeillo-Via (215) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 5 |
| Bois de Argelès-sur-Mer (9) ⚠️ | Argelès-sur-Mer › Albères – Côte Vermeille – Illibéris | 5 |
| Forêt de Ria-Sirach (11) ⚠️ | Ria-Sirach › Conflent-Canigó | 5 |
| Forêt de Corneilla-de-Conflent (21) ⚠️ | Corneilla-de-Conflent › Conflent-Canigó | 5 |
| Forêt de Corbère-les-Cabanes ⚠️ | Corbère-les-Cabanes › Roussillon Conflent | 4 |
| Forêt de Salses-le-Château (3) ⚠️ | Salses-le-Château › Corbières Salanque Méditerranée | 4 |
| Forêt de Mosset (8) ⚠️ | Mosset › Conflent-Canigó | 4 |
| Forêt des Angles ⚠️ | Les Angles › Pyrénées catalanes | 4 |
| Bois des chênes ⚠️ | Perpignan › Perpignan Méditerranée Métropole | 4 |
| Le Bois des Pins ⚠️ | Argelès-sur-Mer › Albères – Côte Vermeille – Illibéris | 4 |
| Forêt de Trouillas ⚠️ | Trouillas › Aspres | 4 |
| Forêt de Vinça ⚠️ | Vinça › Conflent-Canigó | 4 |
| Forêt de La Llagonne (67) ⚠️ | La Llagonne › Pyrénées catalanes | 4 |
| Forêt des Angles (28) ⚠️ | Les Angles › Pyrénées catalanes | 4 |
| Forêt de Font-Romeu-Odeillo-Via (56) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 4 |
| Forêt de Saint-Pierre-dels-Forcats (25) ⚠️ | Saint-Pierre-dels-Forcats › Pyrénées catalanes | 4 |
| Forêt de Saint-Pierre-dels-Forcats (26) ⚠️ | Saint-Pierre-dels-Forcats › Pyrénées catalanes | 4 |
| Forêt de Puyvalador (34) ⚠️ | Puyvalador › Pyrénées catalanes | 4 |
| Forêt de Formiguères (56) ⚠️ | Formiguères › Pyrénées catalanes | 4 |
| Parc Municipal de Valmy et circuit botanique ⚠️ | Argelès-sur-Mer › Albères – Côte Vermeille – Illibéris | 4 |
| Forêt de Ria-Sirach (9) ⚠️ | Ria-Sirach › Conflent-Canigó | 4 |
| Forêt de Opoul-Périllos (14) ⚠️ | Opoul-Périllos › Perpignan Méditerranée Métropole | 4 |
| Bois de Salses-le-Château (2) ⚠️ | Salses-le-Château › Corbières Salanque Méditerranée | 4 |
| Bois de Argelès-sur-Mer ⚠️ | Argelès-sur-Mer › Albères – Côte Vermeille – Illibéris | 4 |
| Forêt de Espira-de-Conflent (3) ⚠️ | Espira-de-Conflent › Conflent-Canigó | 4 |
| Forêt de Matemale (31) ⚠️ | Matemale › Pyrénées catalanes | 4 |
| Forêt de Puyvalador (74) ⚠️ | Puyvalador › Pyrénées catalanes | 4 |
| Forêt de Fenouillet (3) ⚠️ | Fenouillet › Agly Fenouillèdes | 4 |
| Bois de Céret (3) ⚠️ | Céret › Vallespir | 4 |
| Bois de Oms (4) ⚠️ | Oms › Aspres | 4 |
| Bois de Oms (25) ⚠️ | Oms › Aspres | 4 |
| Bois de Calmeilles (2) ⚠️ | Calmeilles › Aspres | 4 |
| Forêt de Camélas (8) ⚠️ | Camélas › Aspres | 4 |
| Forêt de Millas (6) ⚠️ | Millas › Roussillon Conflent | 4 |
| Forêt de Néfiach ⚠️ | Néfiach › Roussillon Conflent | 4 |
| Forêt du Soler (3) ⚠️ | Le Soler › Perpignan Méditerranée Métropole | 4 |
| Forêt de Caudiès-de-Fenouillèdes (14) ⚠️ | Caudiès-de-Fenouillèdes › Agly Fenouillèdes | 4 |
| Forêt de Caudiès-de-Fenouillèdes (25) ⚠️ | Caudiès-de-Fenouillèdes › Agly Fenouillèdes | 4 |
| Forêt de Caudiès-de-Fenouillèdes (27) ⚠️ | Caudiès-de-Fenouillèdes › Agly Fenouillèdes | 4 |
| Forêt de Saint-Paul-de-Fenouillet (7) ⚠️ | Saint-Paul-de-Fenouillet › Agly Fenouillèdes | 4 |
| Forêt de Fenouillet (26) ⚠️ | Fenouillet › Agly Fenouillèdes | 4 |
| Forêt du Vivier (2) ⚠️ | Le Vivier › Agly Fenouillèdes | 4 |
| Bois de Canet-en-Roussillon (4) ⚠️ | Canet-en-Roussillon › Perpignan Méditerranée Métropole | 4 |
| Forêt de Casteil (2) ⚠️ | Casteil › Conflent-Canigó | 4 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (201) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 4 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (376) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 4 |
| Bois de Taurinya (2) ⚠️ | Taurinya › Conflent-Canigó | 4 |
| Parc de Néfiach (2) ⚠️ | Néfiach › Roussillon Conflent | 4 |
| Bois de Enveitg ⚠️ | Enveitg › Pyrénées Cerdagne | 4 |
| Bois de Porta (3) ⚠️ | Porta › Pyrénées Cerdagne | 4 |
| Forêt de Rodès (7) ⚠️ | Rodès › Roussillon Conflent | 4 |
| Forêt de Vivès (6) ⚠️ | Vivès › Vallespir | 4 |
| Bois du Barcarès ⚠️ | Le Barcarès › Perpignan Méditerranée Métropole | 3 |
| Parc Sant Vicens ⚠️ | Perpignan › Perpignan Méditerranée Métropole | 3 |
| Parc Palauda ⚠️ | Thuir › Aspres | 3 |
| La Pinède ⚠️ | Saint-Estève › Perpignan Méditerranée Métropole | 3 |
| Forêt de Prades (3) ⚠️ | Prades › Conflent-Canigó | 3 |
| Parc de Clairfont ⚠️ | Toulouges › Perpignan Méditerranée Métropole | 3 |
| La motte de l’Agly ⚠️ | Saint-Laurent-de-la-Salanque › Perpignan Méditerranée Métropole | 3 |
| Forêt communale de Saleilles "La Mainada" ⚠️ | Saleilles › Perpignan Méditerranée Métropole | 3 |
| Forêt de Sauto (7) ⚠️ | Sauto › Pyrénées catalanes | 3 |
| Forêt des Angles (10) ⚠️ | Les Angles › Pyrénées catalanes | 3 |
| Forêt de Font-Romeu-Odeillo-Via (44) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 3 |
| Forêt de Font-Romeu-Odeillo-Via (49) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 3 |
| Forêt de Font-Romeu-Odeillo-Via (122) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 3 |
| Forêt de Font-Romeu-Odeillo-Via (129) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 3 |
| Forêt de Font-Romeu-Odeillo-Via (203) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 3 |
| Forêt de Saint-Pierre-dels-Forcats (15) ⚠️ | Saint-Pierre-dels-Forcats › Pyrénées catalanes | 3 |
| Forêt de Saint-Pierre-dels-Forcats (21) ⚠️ | Saint-Pierre-dels-Forcats › Pyrénées catalanes | 3 |
| Forêt de Saint-Pierre-dels-Forcats (28) ⚠️ | Saint-Pierre-dels-Forcats › Pyrénées catalanes | 3 |
| Forêt de Eyne (18) ⚠️ | Eyne › Pyrénées catalanes | 3 |
| Forêt de Puyvalador (8) ⚠️ | Puyvalador › Pyrénées catalanes | 3 |
| Forêt de Err (12) ⚠️ | Err › Pyrénées Cerdagne | 3 |
| Forêt de Porta (16) ⚠️ | Porta › Pyrénées Cerdagne | 3 |
| Forêt de Porté-Puymorens (46) ⚠️ | Porté-Puymorens › Pyrénées Cerdagne | 3 |
| Forêt de Corneilla-de-Conflent (12) ⚠️ | Corneilla-de-Conflent › Conflent-Canigó | 3 |
| Forêt de Fuilla (16) ⚠️ | Fuilla › Conflent-Canigó | 3 |
| Forêt de Ria-Sirach (6) ⚠️ | Ria-Sirach › Conflent-Canigó | 3 |
| La Pinède (2) ⚠️ | Saint-Estève › Perpignan Méditerranée Métropole | 3 |
| Forêt de Llo (3) ⚠️ | Saillagouse › Pyrénées Cerdagne | 3 |
| Forêt de Angoustrine-Villeneuve-des-Escaldes (3) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 3 |
| Parc du Moulin ⚠️ | Le Soler › Perpignan Méditerranée Métropole | 3 |
| Parc du château d'Aubiry ⚠️ | Céret › Vallespir | 3 |
| Bassin Albert Vila ⚠️ | Perpignan › Perpignan Méditerranée Métropole | 3 |
| Forêt de Rodès (2) ⚠️ | Rodès › Roussillon Conflent | 3 |
| Forêt de Rodès (3) ⚠️ | Rodès › Roussillon Conflent | 3 |
| Forêt de Rodès (4) ⚠️ | Rodès › Roussillon Conflent | 3 |
| Forêt de Formiguères (113) ⚠️ | Formiguères › Pyrénées catalanes | 3 |
| Forêt de Réal (7) ⚠️ | Réal › Pyrénées catalanes | 3 |
| Forêt de Réal (11) ⚠️ | Réal › Pyrénées catalanes | 3 |
| Bois de Saint-Paul-de-Fenouillet ⚠️ | Saint-Paul-de-Fenouillet › Agly Fenouillèdes | 3 |
| Forêt de Saint-André (3) ⚠️ | Saint-André › Albères – Côte Vermeille – Illibéris | 3 |
| Forêt de Sorède (3) ⚠️ | Sorède › Albères – Côte Vermeille – Illibéris | 3 |
| Forêt de Catllar (8) ⚠️ | Catllar › Conflent-Canigó | 3 |
| Forêt de Banyuls-dels-Aspres ⚠️ | Banyuls-dels-Aspres › Aspres | 3 |
| Forêt de Vivès (3) ⚠️ | Vivès › Vallespir | 3 |
| Bois de Vinça ⚠️ | Vinça › Conflent-Canigó | 3 |
| Bois de Vinça (4) ⚠️ | Vinça › Conflent-Canigó | 3 |
| Bois de Saint-Jean-Pla-de-Corts (2) ⚠️ | Saint-Jean-Pla-de-Corts › Vallespir | 3 |
| Bois de Céret (4) ⚠️ | Céret › Vallespir | 3 |
| Forêt de Llupia ⚠️ | Llupia › Perpignan Méditerranée Métropole | 3 |
| Bois de Eyne (3) ⚠️ | Eyne › Pyrénées catalanes | 3 |
| Bois de Opoul-Périllos (3) ⚠️ | Opoul-Périllos › Perpignan Méditerranée Métropole | 3 |
| Forêt de Camélas (4) ⚠️ | Camélas › Aspres | 3 |
| Forêt de Camélas (7) ⚠️ | Camélas › Aspres | 3 |
| Forêt de Millas (3) ⚠️ | Millas › Roussillon Conflent | 3 |
| Forêt du Soler (10) ⚠️ | Le Soler › Perpignan Méditerranée Métropole | 3 |
| Forêt de Caudiès-de-Fenouillèdes (11) ⚠️ | Caudiès-de-Fenouillèdes › Agly Fenouillèdes | 3 |
| Forêt de Saint-Paul-de-Fenouillet (3) ⚠️ | Saint-Paul-de-Fenouillet › Agly Fenouillèdes | 3 |
| Forêt de Caudiès-de-Fenouillèdes (22) ⚠️ | Caudiès-de-Fenouillèdes › Agly Fenouillèdes | 3 |
| Parc de Caudiès-de-Fenouillèdes ⚠️ | Caudiès-de-Fenouillèdes › Agly Fenouillèdes | 3 |
| Forêt de Saint-Paul-de-Fenouillet (12) ⚠️ | Saint-Paul-de-Fenouillet › Agly Fenouillèdes | 3 |
| Forêt de Saint-Pierre-dels-Forcats (43) ⚠️ | Saint-Pierre-dels-Forcats › Pyrénées catalanes | 3 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (21) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 3 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (94) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 3 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (100) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 3 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (113) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 3 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (134) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 3 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (137) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 3 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (154) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 3 |
| Bois de Porté-Puymorens (4) ⚠️ | Porté-Puymorens › Pyrénées Cerdagne | 3 |
| Bois de Porté-Puymorens (16) ⚠️ | Porté-Puymorens › Pyrénées Cerdagne | 3 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (206) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 3 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (229) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 3 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (233) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 3 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (257) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 3 |
| Bois de Formiguères (2) ⚠️ | Formiguères › Pyrénées catalanes | 3 |
| Bois de Mantet ⚠️ | Mantet › Conflent-Canigó | 3 |
| Bois de Nyer ⚠️ | Nyer › Conflent-Canigó | 3 |
| Bois de Latour-de-France (2) ⚠️ | Latour-de-France › Agly Fenouillèdes | 3 |
| Bois de Argelès-sur-Mer (5) ⚠️ | Argelès-sur-Mer › Albères – Côte Vermeille – Illibéris | 3 |
| Forêt de Vinça (3) ⚠️ | Vinça › Conflent-Canigó | 3 |
| Bois de Cassagnes (3) ⚠️ | Cassagnes › Perpignan Méditerranée Métropole | 3 |
| Bois de Porta (2) ⚠️ | Porta › Pyrénées Cerdagne | 3 |
| Forêt de Millas (9) ⚠️ | Millas › Roussillon Conflent | 3 |
| Bois de Cases-de-Pène (2) ⚠️ | Cases-de-Pène › Perpignan Méditerranée Métropole | 3 |
| Forêt de Caramany (9) ⚠️ | Bélesta › Roussillon Conflent | 3 |
| Forêt de Porté-Puymorens (51) ⚠️ | Porté-Puymorens › Pyrénées Cerdagne | 3 |
| Bois de Trouillas (7) ⚠️ | Trouillas › Aspres | 3 |
| Forêt de Saint-Laurent-de-Cerdans (4) ⚠️ | Saint-Laurent-de-Cerdans › Haut-Vallespir | 3 |
| Forêt de Maureillas-las-Illas (11) ⚠️ | Maureillas-las-Illas › Vallespir | 3 |
| Forêt de l'Albère (4) ⚠️ | L'Albère › Vallespir | 3 |
| Parc de Saint-Estève ⚠️ | Saint-Estève › Perpignan Méditerranée Métropole | 2 |
| Forêt de Salses-le-Château (7) ⚠️ | Salses-le-Château › Corbières Salanque Méditerranée | 2 |
| Bois de Ille-sur-Têt ⚠️ | Ille-sur-Têt › Roussillon Conflent | 2 |
| Forêt de Conat (4) ⚠️ | Conat › Conflent-Canigó | 2 |
| Arboretum du Mas Roussillon ⚠️ | Canet-en-Roussillon › Perpignan Méditerranée Métropole | 2 |
| Fort du Serrat d'En Vaquer ⚠️ | Perpignan › Perpignan Méditerranée Métropole | 2 |
| Parc de Saleilles ⚠️ | Saleilles › Perpignan Méditerranée Métropole | 2 |
| Forêt de Railleu (5) ⚠️ | Railleu › Pyrénées catalanes | 2 |
| Forêt de Prades (12) ⚠️ | Prades › Conflent-Canigó | 2 |
| El Moli ⚠️ | Eus › Conflent-Canigó | 2 |
| Forêt de Fuilla (2) ⚠️ | Fuilla › Conflent-Canigó | 2 |
| Forêt de Corneilla-de-Conflent (8) ⚠️ | Corneilla-de-Conflent › Conflent-Canigó | 2 |
| Parc Maillol ⚠️ | Perpignan › Perpignan Méditerranée Métropole | 2 |
| Forêt des Angles (24) ⚠️ | Les Angles › Pyrénées catalanes | 2 |
| Forêt des Angles (26) ⚠️ | Les Angles › Pyrénées catalanes | 2 |
| Forêt des Angles (35) ⚠️ | Les Angles › Pyrénées catalanes | 2 |
| Forêt des Angles (44) ⚠️ | Les Angles › Pyrénées catalanes | 2 |
| Forêt des Angles (68) ⚠️ | Les Angles › Pyrénées catalanes | 2 |
| Forêt des Angles (88) ⚠️ | Les Angles › Pyrénées catalanes | 2 |
| Forêt des Angles (112) ⚠️ | Les Angles › Pyrénées catalanes | 2 |
| Forêt des Angles (118) ⚠️ | Les Angles › Pyrénées catalanes | 2 |
| Forêt des Angles (136) ⚠️ | Les Angles › Pyrénées catalanes | 2 |
| Forêt des Angles (141) ⚠️ | Les Angles › Pyrénées catalanes | 2 |
| Forêt des Angles (143) ⚠️ | Les Angles › Pyrénées catalanes | 2 |
| Forêt de Font-Romeu-Odeillo-Via (34) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 2 |
| Forêt de Font-Romeu-Odeillo-Via (35) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 2 |
| Forêt de Font-Romeu-Odeillo-Via (36) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 2 |
| Forêt de Bolquère (11) ⚠️ | Bolquère › Pyrénées catalanes | 2 |
| Forêt de Bolquère (12) ⚠️ | Bolquère › Pyrénées catalanes | 2 |
| Forêt de Bolquère (16) ⚠️ | Bolquère › Pyrénées catalanes | 2 |
| Forêt de Font-Romeu-Odeillo-Via (60) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 2 |
| Forêt de Font-Romeu-Odeillo-Via (115) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 2 |
| Forêt de Font-Romeu-Odeillo-Via (118) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 2 |
| Forêt de Font-Romeu-Odeillo-Via (159) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 2 |
| Forêt de Eyne (10) ⚠️ | Eyne › Pyrénées catalanes | 2 |
| Forêt de Saint-Pierre-dels-Forcats ⚠️ | Saint-Pierre-dels-Forcats › Pyrénées catalanes | 2 |
| Forêt de Saint-Pierre-dels-Forcats (18) ⚠️ | Saint-Pierre-dels-Forcats › Pyrénées catalanes | 2 |
| Forêt de Saint-Pierre-dels-Forcats (22) ⚠️ | Saint-Pierre-dels-Forcats › Pyrénées catalanes | 2 |
| Forêt de Saint-Pierre-dels-Forcats (23) ⚠️ | Saint-Pierre-dels-Forcats › Pyrénées catalanes | 2 |
| Forêt de Puyvalador (10) ⚠️ | Puyvalador › Pyrénées catalanes | 2 |
| Forêt de Puyvalador (12) ⚠️ | Puyvalador › Pyrénées catalanes | 2 |
| Forêt de Puyvalador (14) ⚠️ | Puyvalador › Pyrénées catalanes | 2 |
| Forêt de Puyvalador (24) ⚠️ | Puyvalador › Pyrénées catalanes | 2 |
| Forêt de Puyvalador (26) ⚠️ | Puyvalador › Pyrénées catalanes | 2 |
| Forêt de Puyvalador (30) ⚠️ | Puyvalador › Pyrénées catalanes | 2 |
| Forêt de Puyvalador (31) ⚠️ | Puyvalador › Pyrénées catalanes | 2 |
| Forêt de Formiguères (2) ⚠️ | Formiguères › Pyrénées catalanes | 2 |
| Forêt de Formiguères (13) ⚠️ | Formiguères › Pyrénées catalanes | 2 |
| Forêt de Formiguères (17) ⚠️ | Formiguères › Pyrénées catalanes | 2 |
| Forêt de Formiguères (18) ⚠️ | Formiguères › Pyrénées catalanes | 2 |
| Forêt de Formiguères (20) ⚠️ | Formiguères › Pyrénées catalanes | 2 |
| Forêt de Formiguères (23) ⚠️ | Formiguères › Pyrénées catalanes | 2 |
| Forêt de Formiguères (55) ⚠️ | Formiguères › Pyrénées catalanes | 2 |
| Forêt de Err (7) ⚠️ | Err › Pyrénées Cerdagne | 2 |
| Forêt de Err (10) ⚠️ | Err › Pyrénées Cerdagne | 2 |
| Forêt de Err (11) ⚠️ | Err › Pyrénées Cerdagne | 2 |
| Forêt de Porta (11) ⚠️ | Porta › Pyrénées Cerdagne | 2 |
| Forêt de Porté-Puymorens (8) ⚠️ | Porta › Pyrénées Cerdagne | 2 |
| Forêt de Porta (23) ⚠️ | Porta › Pyrénées Cerdagne | 2 |
| Forêt de Porté-Puymorens (19) ⚠️ | Porté-Puymorens › Pyrénées Cerdagne | 2 |
| Forêt de Porté-Puymorens (42) ⚠️ | Porté-Puymorens › Pyrénées Cerdagne | 2 |
| Forêt de Corneilla-de-Conflent (11) ⚠️ | Corneilla-de-Conflent › Conflent-Canigó | 2 |
| Forêt de Ayguatébia-Talau (7) ⚠️ | Ayguatébia-Talau › Pyrénées catalanes | 2 |
| Forêt de Caudiès-de-Conflent (3) ⚠️ | Caudiès-de-Conflent › Pyrénées catalanes | 2 |
| Forêt de Opoul-Périllos (9) ⚠️ | Opoul-Périllos › Perpignan Méditerranée Métropole | 2 |
| Jardin Pams ⚠️ | Collioure › Albères – Côte Vermeille – Illibéris | 2 |
| Forêt de Llo (4) ⚠️ | Llo › Pyrénées Cerdagne | 2 |
| Forêt de Rodès ⚠️ | Rodès › Roussillon Conflent | 2 |
| Aire de Loisirs du Prat de la Farga ⚠️ | Maureillas-las-Illas › Vallespir | 2 |
| Forêt de Formiguères (79) ⚠️ | Formiguères › Pyrénées catalanes | 2 |
| Forêt de Formiguères (109) ⚠️ | Formiguères › Pyrénées catalanes | 2 |
| Forêt de Réal (9) ⚠️ | Réal › Pyrénées catalanes | 2 |
| Forêt de Torreilles (2) ⚠️ | Torreilles › Perpignan Méditerranée Métropole | 2 |
| Forêt de Saint-André (2) ⚠️ | Saint-André › Albères – Côte Vermeille – Illibéris | 2 |
| Forêt de Argelès-sur-Mer (9) ⚠️ | Argelès-sur-Mer › Albères – Côte Vermeille – Illibéris | 2 |
| Forêt de Fenouillet (6) ⚠️ | Fenouillet › Agly Fenouillèdes | 2 |
| Forêt de Peyrestortes (2) ⚠️ | Peyrestortes › Perpignan Méditerranée Métropole | 2 |
| Bois de Vinça (5) ⚠️ | Vinça › Conflent-Canigó | 2 |
| Forêt de Fillols (5) ⚠️ | Fillols › Conflent-Canigó | 2 |
| Forêt de Pollestres ⚠️ | Pollestres › Perpignan Méditerranée Métropole | 2 |
| Bois de Saint-Jean-Pla-de-Corts (3) ⚠️ | Saint-Jean-Pla-de-Corts › Vallespir | 2 |
| Bois de Céret (2) ⚠️ | Céret › Vallespir | 2 |
| Forêt de Formiguères (148) ⚠️ | Formiguères › Pyrénées catalanes | 2 |
| Forêt urbaine du Prat de Cavall ⚠️ | Théza › Sud-Roussillon | 2 |
| Bois de Maureillas-las-Illas ⚠️ | Maureillas-las-Illas › Vallespir | 2 |
| Forêt de Cabestany (2) ⚠️ | Cabestany › Perpignan Méditerranée Métropole | 2 |
| Bois de Perpignan (2) ⚠️ | Perpignan › Perpignan Méditerranée Métropole | 2 |
| Bois de Oms (2) ⚠️ | Oms › Aspres | 2 |
| Bois de Oms (12) ⚠️ | Oms › Aspres | 2 |
| Bois de Oms (22) ⚠️ | Oms › Aspres | 2 |
| Bois de Oms (26) ⚠️ | Oms › Aspres | 2 |
| Bois de Saint-Estève (3) ⚠️ | Saint-Estève › Perpignan Méditerranée Métropole | 2 |
| Forêt de Pollestres (2) ⚠️ | Pollestres › Perpignan Méditerranée Métropole | 2 |
| Bois de Peyrestortes ⚠️ | Peyrestortes › Perpignan Méditerranée Métropole | 2 |
| Bois de Saint-Féliu-d'Avall ⚠️ | Saint-Féliu-d'Avall › Perpignan Méditerranée Métropole | 2 |
| Forêt de Saint-Paul-de-Fenouillet (8) ⚠️ | Saint-Paul-de-Fenouillet › Agly Fenouillèdes | 2 |
| Forêt de Prugnanes (4) ⚠️ | Prugnanes › Agly Fenouillèdes | 2 |
| Forêt de Saint-Paul-de-Fenouillet (9) ⚠️ | Saint-Paul-de-Fenouillet › Agly Fenouillèdes | 2 |
| Forêt de Saint-Paul-de-Fenouillet (14) ⚠️ | Saint-Paul-de-Fenouillet › Agly Fenouillèdes | 2 |
| Forêt de Fenouillet (20) ⚠️ | Fenouillet › Agly Fenouillèdes | 2 |
| Forêt de Fenouillet (23) ⚠️ | Fenouillet › Agly Fenouillèdes | 2 |
| Bois de Canet-en-Roussillon (3) ⚠️ | Canet-en-Roussillon › Perpignan Méditerranée Métropole | 2 |
| Parc de Amélie-les-Bains-Palalda ⚠️ | Amélie-les-Bains-Palalda › Haut-Vallespir | 2 |
| Bois de Arles-sur-Tech ⚠️ | Arles-sur-Tech › Haut-Vallespir | 2 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (76) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 2 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (95) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 2 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (115) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 2 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (126) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 2 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (151) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 2 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (156) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 2 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (167) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 2 |
| Bois de Porté-Puymorens (17) ⚠️ | Porté-Puymorens › Pyrénées Cerdagne | 2 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (224) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 2 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (256) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 2 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (274) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 2 |
| Bois de Porté-Puymorens (33) ⚠️ | Porté-Puymorens › Pyrénées Cerdagne | 2 |
| Bois de Mantet (4) ⚠️ | Mantet › Conflent-Canigó | 2 |
| Bois de Fontpédrouse (3) ⚠️ | Fontpédrouse › Conflent-Canigó | 2 |
| Bois de Ille-sur-Têt (3) ⚠️ | Ille-sur-Têt › Roussillon Conflent | 2 |
| Bois de Millas ⚠️ | Néfiach › Roussillon Conflent | 2 |
| Bois de Nyer (4) ⚠️ | Nyer › Conflent-Canigó | 2 |
| Forêt de Cabestany (5) ⚠️ | Cabestany › Perpignan Méditerranée Métropole | 2 |
| Bois du Tamariguer ⚠️ | Argelès-sur-Mer › Albères – Côte Vermeille – Illibéris | 2 |
| Forêt de Corneilla-de-Conflent (17) ⚠️ | Corneilla-de-Conflent › Conflent-Canigó | 2 |
| Forêt de Rivesaltes (6) ⚠️ | Pia › Corbières Salanque Méditerranée | 2 |
| Bois de Argelès-sur-Mer (3) ⚠️ | Argelès-sur-Mer › Albères – Côte Vermeille – Illibéris | 2 |
| Forêt de Bourg-Madame (4) ⚠️ | Bourg-Madame › Pyrénées Cerdagne | 2 |
| Forêt de Angoustrine-Villeneuve-des-Escaldes (4) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 2 |
| Bois de Argelès-sur-Mer (10) ⚠️ | Argelès-sur-Mer › Albères – Côte Vermeille – Illibéris | 2 |
| Bois de Latour-de-France (4) ⚠️ | Latour-de-France › Agly Fenouillèdes | 2 |
| Jardin de la Butte ⚠️ | Perpignan › Perpignan Méditerranée Métropole | 2 |
| Bois de Thuir (10) ⚠️ | Thuir › Aspres | 2 |
| Forêt de Caramany (2) ⚠️ | Caramany › Agly Fenouillèdes | 2 |
| Forêt de Caramany (5) ⚠️ | Caramany › Agly Fenouillèdes | 2 |
| Forêt de Eus (7) ⚠️ | Eus › Conflent-Canigó | 2 |
| Forêt de Vernet-les-Bains (11) ⚠️ | Vernet-les-Bains › Conflent-Canigó | 2 |
| Forêt des Angles (180) ⚠️ | Les Angles › Pyrénées catalanes | 2 |
| Forêt de Vinça (5) ⚠️ | Vinça › Conflent-Canigó | 2 |
| Forêt de Réal (17) ⚠️ | Réal › Pyrénées catalanes | 2 |
| Forêt de Fenouillet (32) ⚠️ | Fenouillet › Agly Fenouillèdes | 2 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (475) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 2 |
| Forêt de Ur (2) ⚠️ | Ur › Pyrénées Cerdagne | 2 |
| Bois de Argelès-sur-Mer (14) ⚠️ | Argelès-sur-Mer › Albères – Côte Vermeille – Illibéris | 2 |
| Forêt de Banyuls-sur-Mer (40) ⚠️ | Banyuls-sur-Mer › Albères – Côte Vermeille – Illibéris | 2 |
| Square Bir Hakeim ⚠️ | Perpignan › Perpignan Méditerranée Métropole | 1 |
| Espace Sportif Pierre Jonquères d'Oriola et Christian d'Oriola ⚠️ | Perpignan › Perpignan Méditerranée Métropole | 1 |
| Parc de Perpignan ⚠️ | Perpignan › Perpignan Méditerranée Métropole | 1 |
| Parc Jeanne De Guardia ⚠️ | Baho › Perpignan Méditerranée Métropole | 1 |
| Bois du Barcarès (2) ⚠️ | Le Barcarès › Perpignan Méditerranée Métropole | 1 |
| Forêt de Salses-le-Château (6) ⚠️ | Salses-le-Château › Corbières Salanque Méditerranée | 1 |
| Forêt de Mosset (15) ⚠️ | Mosset › Conflent-Canigó | 1 |
| Forêt de Prades (2) ⚠️ | Prades › Conflent-Canigó | 1 |
| Forêt de Millas ⚠️ | Millas › Roussillon Conflent | 1 |
| Forêt de Conat (5) ⚠️ | Conat › Conflent-Canigó | 1 |
| Parc du Château Pams ⚠️ | Prades › Conflent-Canigó | 1 |
| Parc des Quatre Chemins ⚠️ | Saint-Hippolyte › Perpignan Méditerranée Métropole | 1 |
| Forêt de Saillagouse ⚠️ | Saillagouse › Pyrénées Cerdagne | 1 |
| Forêt de Mosset (20) ⚠️ | Mosset › Conflent-Canigó | 1 |
| Espace Jeanbrau Bardou Job ⚠️ | Prades › Conflent-Canigó | 1 |
| Forêt de Vernet-les-Bains (2) ⚠️ | Vernet-les-Bains › Conflent-Canigó | 1 |
| Forêt de Eus (5) ⚠️ | Eus › Conflent-Canigó | 1 |
| Forêt de Los Masos (2) ⚠️ | Los Masos › Conflent-Canigó | 1 |
| Forêt de Los Masos (5) ⚠️ | Los Masos › Conflent-Canigó | 1 |
| Forêt de Prades (5) ⚠️ | Prades › Conflent-Canigó | 1 |
| Forêt de Prades (7) ⚠️ | Prades › Conflent-Canigó | 1 |
| Forêt de Prades (8) ⚠️ | Prades › Conflent-Canigó | 1 |
| Forêt de Railleu (3) ⚠️ | Railleu › Pyrénées catalanes | 1 |
| Forêt de Railleu (4) ⚠️ | Railleu › Pyrénées catalanes | 1 |
| Maternité Suisse d'Elne ⚠️ | Elne › Albères – Côte Vermeille – Illibéris | 1 |
| Square Bir-Hakeim ⚠️ | Perpignan › Perpignan Méditerranée Métropole | 1 |
| Jardin des Plantes Les Capellans ⚠️ | Saint-Cyprien › Sud-Roussillon | 1 |
| Forêt de Rivesaltes (2) ⚠️ | Rivesaltes › Perpignan Méditerranée Métropole | 1 |
| Parc de Villelongue-de-la-Salanque ⚠️ | Villelongue-de-la-Salanque › Perpignan Méditerranée Métropole | 1 |
| Parc de la Pépinière ⚠️ | Perpignan › Perpignan Méditerranée Métropole | 1 |
| Forêt de Fuilla (4) ⚠️ | Fuilla › Conflent-Canigó | 1 |
| Forêt de Sahorre (7) ⚠️ | Sahorre › Conflent-Canigó | 1 |
| Forêt de Fuilla (8) ⚠️ | Fuilla › Conflent-Canigó | 1 |
| Forêt de Sahorre (12) ⚠️ | Sahorre › Conflent-Canigó | 1 |
| Forêt de Vernet-les-Bains (3) ⚠️ | Vernet-les-Bains › Conflent-Canigó | 1 |
| Forêt de Vernet-les-Bains (4) ⚠️ | Vernet-les-Bains › Conflent-Canigó | 1 |
| Forêt de Vernet-les-Bains (6) ⚠️ | Vernet-les-Bains › Conflent-Canigó | 1 |
| Forêt de Vernet-les-Bains (7) ⚠️ | Vernet-les-Bains › Conflent-Canigó | 1 |
| Forêt de Corneilla-de-Conflent (6) ⚠️ | Corneilla-de-Conflent › Conflent-Canigó | 1 |
| Bois de Vingrau (2) ⚠️ | Vingrau › Perpignan Méditerranée Métropole | 1 |
| Bois de Vingrau (3) ⚠️ | Vingrau › Perpignan Méditerranée Métropole | 1 |
| Forêt de Codalet ⚠️ | Codalet › Conflent-Canigó | 1 |
| Forêt de La Llagonne (2) ⚠️ | La Llagonne › Pyrénées catalanes | 1 |
| Forêt de La Llagonne (9) ⚠️ | La Llagonne › Pyrénées catalanes | 1 |
| Forêt de La Llagonne (20) ⚠️ | La Llagonne › Pyrénées catalanes | 1 |
| Forêt de La Llagonne (21) ⚠️ | La Llagonne › Pyrénées catalanes | 1 |
| Forêt de La Llagonne (22) ⚠️ | La Llagonne › Pyrénées catalanes | 1 |
| Forêt de La Llagonne (23) ⚠️ | La Llagonne › Pyrénées catalanes | 1 |
| Forêt de La Llagonne (29) ⚠️ | La Llagonne › Pyrénées catalanes | 1 |
| Forêt de La Llagonne (40) ⚠️ | La Llagonne › Pyrénées catalanes | 1 |
| Forêt de La Llagonne (46) ⚠️ | La Llagonne › Pyrénées catalanes | 1 |
| Forêt de La Llagonne (47) ⚠️ | La Llagonne › Pyrénées catalanes | 1 |
| Forêt de La Llagonne (52) ⚠️ | La Llagonne › Pyrénées catalanes | 1 |
| Forêt de La Llagonne (61) ⚠️ | La Llagonne › Pyrénées catalanes | 1 |
| Forêt de La Llagonne (64) ⚠️ | La Llagonne › Pyrénées catalanes | 1 |
| Forêt de La Llagonne (65) ⚠️ | La Llagonne › Pyrénées catalanes | 1 |
| Forêt de La Llagonne (66) ⚠️ | La Llagonne › Pyrénées catalanes | 1 |
| Forêt de Sauto (3) ⚠️ | Sauto › Pyrénées catalanes | 1 |
| Forêt de La Llagonne (77) ⚠️ | La Llagonne › Pyrénées catalanes | 1 |
| Forêt des Angles (9) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (11) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (22) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (29) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (34) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (36) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (38) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (42) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (43) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (51) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (53) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (74) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (75) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (78) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (86) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (91) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (93) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (98) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (100) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (101) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (102) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (104) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (108) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (119) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (120) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (132) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (135) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (142) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (144) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (8) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (10) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (19) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Bolquère (2) ⚠️ | Bolquère › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (20) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (24) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Bolquère (6) ⚠️ | Bolquère › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (27) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Bolquère (8) ⚠️ | Bolquère › Pyrénées catalanes | 1 |
| Forêt de Bolquère (9) ⚠️ | Bolquère › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (29) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (31) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (32) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Bolquère (10) ⚠️ | Bolquère › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (38) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (43) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (45) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (52) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (69) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (73) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (75) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (76) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (79) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (89) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (106) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (120) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (124) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (131) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (134) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (135) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (138) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (139) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (145) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (152) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (153) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (174) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (178) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (184) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (186) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (194) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (204) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (208) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Eyne (7) ⚠️ | Eyne › Pyrénées catalanes | 1 |
| Forêt de Eyne (8) ⚠️ | Eyne › Pyrénées catalanes | 1 |
| Forêt de Saint-Pierre-dels-Forcats (6) ⚠️ | Saint-Pierre-dels-Forcats › Pyrénées catalanes | 1 |
| Forêt de Saint-Pierre-dels-Forcats (8) ⚠️ | Saint-Pierre-dels-Forcats › Pyrénées catalanes | 1 |
| Forêt de Eyne (17) ⚠️ | Eyne › Pyrénées catalanes | 1 |
| Forêt de Saint-Pierre-dels-Forcats (13) ⚠️ | Saint-Pierre-dels-Forcats › Pyrénées catalanes | 1 |
| Forêt de Saint-Pierre-dels-Forcats (17) ⚠️ | Saint-Pierre-dels-Forcats › Pyrénées catalanes | 1 |
| Forêt de Saint-Pierre-dels-Forcats (19) ⚠️ | Saint-Pierre-dels-Forcats › Pyrénées catalanes | 1 |
| Forêt de Saint-Pierre-dels-Forcats (24) ⚠️ | Saint-Pierre-dels-Forcats › Pyrénées catalanes | 1 |
| Forêt de Saint-Pierre-dels-Forcats (29) ⚠️ | Saint-Pierre-dels-Forcats › Pyrénées catalanes | 1 |
| Forêt de Saint-Pierre-dels-Forcats (39) ⚠️ | Saint-Pierre-dels-Forcats › Pyrénées catalanes | 1 |
| Forêt de Puyvalador (11) ⚠️ | Puyvalador › Pyrénées catalanes | 1 |
| Forêt de Puyvalador (25) ⚠️ | Puyvalador › Pyrénées catalanes | 1 |
| Forêt de Puyvalador (27) ⚠️ | Puyvalador › Pyrénées catalanes | 1 |
| Forêt de Puyvalador (37) ⚠️ | Puyvalador › Pyrénées catalanes | 1 |
| Forêt de Puyvalador (38) ⚠️ | Puyvalador › Pyrénées catalanes | 1 |
| Forêt de Puyvalador (44) ⚠️ | Puyvalador › Pyrénées catalanes | 1 |
| Forêt de Puyvalador (46) ⚠️ | Puyvalador › Pyrénées catalanes | 1 |
| Forêt de Fontrabiouse ⚠️ | Fontrabiouse › Pyrénées catalanes | 1 |
| Forêt de Formiguères (3) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (5) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (7) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (8) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (9) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (19) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (43) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (47) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (53) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (58) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (63) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Bolquère (17) ⚠️ | Bolquère › Pyrénées catalanes | 1 |
| Forêt de Err (4) ⚠️ | Err › Pyrénées Cerdagne | 1 |
| Forêt de Err (8) ⚠️ | Err › Pyrénées Cerdagne | 1 |
| Forêt de Err (9) ⚠️ | Err › Pyrénées Cerdagne | 1 |
| Forêt de Err (26) ⚠️ | Err › Pyrénées Cerdagne | 1 |
| Forêt de Porta (8) ⚠️ | Porta › Pyrénées Cerdagne | 1 |
| Forêt de Porta (9) ⚠️ | Porta › Pyrénées Cerdagne | 1 |
| Forêt de Porta (10) ⚠️ | Porta › Pyrénées Cerdagne | 1 |
| Forêt de Porté-Puymorens (9) ⚠️ | Porté-Puymorens › Pyrénées Cerdagne | 1 |
| Forêt de Porta (18) ⚠️ | Porta › Pyrénées Cerdagne | 1 |
| Forêt de Porta (20) ⚠️ | Porta › Pyrénées Cerdagne | 1 |
| Forêt de Porta (25) ⚠️ | Porta › Pyrénées Cerdagne | 1 |
| Forêt de Porté-Puymorens (25) ⚠️ | Porté-Puymorens › Pyrénées Cerdagne | 1 |
| Forêt de Porté-Puymorens (39) ⚠️ | Porté-Puymorens › Pyrénées Cerdagne | 1 |
| Forêt de Porté-Puymorens (40) ⚠️ | Porté-Puymorens › Pyrénées Cerdagne | 1 |
| Forêt de Porté-Puymorens (41) ⚠️ | Porté-Puymorens › Pyrénées Cerdagne | 1 |
| Forêt de Porté-Puymorens (48) ⚠️ | Porté-Puymorens › Pyrénées Cerdagne | 1 |
| Forêt de Corneilla-de-Conflent (10) ⚠️ | Corneilla-de-Conflent › Conflent-Canigó | 1 |
| Forêt de Fuilla (13) ⚠️ | Fuilla › Conflent-Canigó | 1 |
| Forêt de Fuilla (14) ⚠️ | Fuilla › Conflent-Canigó | 1 |
| Forêt de Fuilla (15) ⚠️ | Conflent-Canigó | 1 |
| Forêt de Ayguatébia-Talau (4) ⚠️ | Ayguatébia-Talau › Pyrénées catalanes | 1 |
| Forêt de Caudiès-de-Conflent ⚠️ | Caudiès-de-Conflent › Pyrénées catalanes | 1 |
| Forêt de Caudiès-de-Conflent (2) ⚠️ | Caudiès-de-Conflent › Pyrénées catalanes | 1 |
| Forêt de Ayguatébia-Talau (8) ⚠️ | Ayguatébia-Talau › Pyrénées catalanes | 1 |
| Forêt de Ayguatébia-Talau (9) ⚠️ | Ayguatébia-Talau › Pyrénées catalanes | 1 |
| Forêt de Ria-Sirach (8) ⚠️ | Ria-Sirach › Conflent-Canigó | 1 |
| Forêt de Opoul-Périllos (4) ⚠️ | Opoul-Périllos › Perpignan Méditerranée Métropole | 1 |
| Forêt de Opoul-Périllos (11) ⚠️ | Opoul-Périllos › Perpignan Méditerranée Métropole | 1 |
| Forêt de Opoul-Périllos (13) ⚠️ | Opoul-Périllos › Perpignan Méditerranée Métropole | 1 |
| Square des Herbiers ⚠️ | Perpignan › Perpignan Méditerranée Métropole | 1 |
| Parc de Vernet-les-Bains ⚠️ | Vernet-les-Bains › Conflent-Canigó | 1 |
| Parc Bartholdi ⚠️ | Perpignan › Perpignan Méditerranée Métropole | 1 |
| Forêt de Argelès-sur-Mer (3) ⚠️ | Argelès-sur-Mer › Albères – Côte Vermeille – Illibéris | 1 |
| Bois de Collioure ⚠️ | Collioure › Albères – Côte Vermeille – Illibéris | 1 |
| Jardin de la Baixarada ⚠️ | Torreilles › Perpignan Méditerranée Métropole | 1 |
| Forêt de Matemale (4) ⚠️ | Matemale › Pyrénées catalanes | 1 |
| Forêt de Matemale (5) ⚠️ | Matemale › Pyrénées catalanes | 1 |
| Bois de Saillagouse ⚠️ | Saillagouse › Pyrénées Cerdagne | 1 |
| Forêt de Font-Romeu-Odeillo-Via (209) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Argelès-sur-Mer (7) ⚠️ | Argelès-sur-Mer › Albères – Côte Vermeille – Illibéris | 1 |
| Ancienne cité du Réart ⚠️ | Rivesaltes › Perpignan Méditerranée Métropole | 1 |
| Forêt de Rigarda ⚠️ | Rigarda › Conflent-Canigó | 1 |
| Forêt de Sainte-Léocadie ⚠️ | Sainte-Léocadie › Pyrénées Cerdagne | 1 |
| Forêt de Saint-Pierre-dels-Forcats (40) ⚠️ | Saint-Pierre-dels-Forcats › Pyrénées catalanes | 1 |
| Forêt de Saint-Pierre-dels-Forcats (41) ⚠️ | Saint-Pierre-dels-Forcats › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (210) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Font-Romeu-Odeillo-Via (211) ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Square Aragon ⚠️ | Perpignan › Perpignan Méditerranée Métropole | 1 |
| Jardin Jésus Pret ⚠️ | Perpignan › Perpignan Méditerranée Métropole | 1 |
| Forêt des Angles (147) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (160) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (161) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Parc des Vergers ⚠️ | Bages › Albères – Côte Vermeille – Illibéris | 1 |
| Forêt de Matemale (17) ⚠️ | Matemale › Pyrénées catalanes | 1 |
| Forêt de Matemale (35) ⚠️ | Matemale › Pyrénées catalanes | 1 |
| Forêt de Formiguères (69) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Matemale (36) ⚠️ | Matemale › Pyrénées catalanes | 1 |
| Forêt de Formiguères (72) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (73) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (75) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (77) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (98) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (101) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (108) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Fontrabiouse (7) ⚠️ | Fontrabiouse › Pyrénées catalanes | 1 |
| Forêt de Fontrabiouse (8) ⚠️ | Fontrabiouse › Pyrénées catalanes | 1 |
| Forêt de Puyvalador (58) ⚠️ | Puyvalador › Pyrénées catalanes | 1 |
| Forêt de Puyvalador (67) ⚠️ | Puyvalador › Pyrénées catalanes | 1 |
| Forêt de Puyvalador (68) ⚠️ | Puyvalador › Pyrénées catalanes | 1 |
| Forêt de Puyvalador (69) ⚠️ | Puyvalador › Pyrénées catalanes | 1 |
| Forêt de Puyvalador (88) ⚠️ | Puyvalador › Pyrénées catalanes | 1 |
| Forêt de Réal (2) ⚠️ | Réal › Pyrénées catalanes | 1 |
| Forêt de Réal (8) ⚠️ | Réal › Pyrénées catalanes | 1 |
| Forêt de Réal (13) ⚠️ | Réal › Pyrénées catalanes | 1 |
| Forêt de Réal (15) ⚠️ | Réal › Pyrénées catalanes | 1 |
| Forêt de Formiguères (115) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (119) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (121) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (123) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt du Barcarès (5) ⚠️ | Le Barcarès › Perpignan Méditerranée Métropole | 1 |
| Forêt de Fenouillet (2) ⚠️ | Fenouillet › Agly Fenouillèdes | 1 |
| Forêt de Sorède (2) ⚠️ | Sorède › Albères – Côte Vermeille – Illibéris | 1 |
| Forêt de Saint-André ⚠️ | Saint-André › Albères – Côte Vermeille – Illibéris | 1 |
| Forêt de Laroque-des-Albères (5) ⚠️ | Laroque-des-Albères › Albères – Côte Vermeille – Illibéris | 1 |
| Bois de Corsavy ⚠️ | Corsavy › Haut-Vallespir | 1 |
| Parc de Arles-sur-Tech ⚠️ | Amélie-les-Bains-Palalda › Haut-Vallespir | 1 |
| Parc de Arles-sur-Tech (2) ⚠️ | Arles-sur-Tech › Haut-Vallespir | 1 |
| Bois de Valmanya ⚠️ | Valmanya › Conflent-Canigó | 1 |
| Parc de Perpignan (13) ⚠️ | Perpignan › Perpignan Méditerranée Métropole | 1 |
| Forêt de Fenouillet (5) ⚠️ | Fenouillet › Agly Fenouillèdes | 1 |
| Forêt de Argelès-sur-Mer (11) ⚠️ | Argelès-sur-Mer › Albères – Côte Vermeille – Illibéris | 1 |
| Forêt de Fenouillet (12) ⚠️ | Fenouillet › Agly Fenouillèdes | 1 |
| Forêt de Fenouillet (14) ⚠️ | Fenouillet › Agly Fenouillèdes | 1 |
| Forêt de Fenouillet (17) ⚠️ | Fenouillet › Agly Fenouillèdes | 1 |
| Forêt de Caudiès-de-Fenouillèdes (7) ⚠️ | Caudiès-de-Fenouillèdes › Agly Fenouillèdes | 1 |
| Parc de Canet-en-Roussillon (7) ⚠️ | Canet-en-Roussillon › Perpignan Méditerranée Métropole | 1 |
| Parc de la Guinguette ⚠️ | Rivesaltes › Perpignan Méditerranée Métropole | 1 |
| Jardin des rêves ⚠️ | Rivesaltes › Perpignan Méditerranée Métropole | 1 |
| Forêt de Peyrestortes (4) ⚠️ | Peyrestortes › Perpignan Méditerranée Métropole | 1 |
| Forêt de Peyrestortes (8) ⚠️ | Peyrestortes › Perpignan Méditerranée Métropole | 1 |
| Square Raoul Casenove ⚠️ | Latour-de-France › Agly Fenouillèdes | 1 |
| Bois de Saint-Paul-de-Fenouillet (2) ⚠️ | Saint-Paul-de-Fenouillet › Agly Fenouillèdes | 1 |
| Parc de Perpignan (15) ⚠️ | Perpignan › Perpignan Méditerranée Métropole | 1 |
| Parc de Perpignan (16) ⚠️ | Perpignan › Perpignan Méditerranée Métropole | 1 |
| Bois de Perpignan ⚠️ | Perpignan › Perpignan Méditerranée Métropole | 1 |
| Bois de Vinça (3) ⚠️ | Vinça › Conflent-Canigó | 1 |
| Forêt de Bages ⚠️ | Bages › Albères – Côte Vermeille – Illibéris | 1 |
| Forêt de Corneilla-de-Conflent (15) ⚠️ | Corneilla-de-Conflent › Conflent-Canigó | 1 |
| Forêt de Bages (2) ⚠️ | Bages › Albères – Côte Vermeille – Illibéris | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (10) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Pézilla-la-Rivière (2) ⚠️ | Pézilla-la-Rivière › Perpignan Méditerranée Métropole | 1 |
| Bois de Saint-Jean-Pla-de-Corts (4) ⚠️ | Saint-Jean-Pla-de-Corts › Vallespir | 1 |
| Bois de Saint-Jean-Pla-de-Corts (5) ⚠️ | Céret › Vallespir | 1 |
| Bois de Saint-Jean-Pla-de-Corts (7) ⚠️ | Saint-Jean-Pla-de-Corts › Vallespir | 1 |
| Bois de Céret (5) ⚠️ | Céret › Vallespir | 1 |
| Bois de Céret (6) ⚠️ | Céret › Vallespir | 1 |
| Bois de Céret (7) ⚠️ | Céret › Vallespir | 1 |
| Parc de Torreilles (3) ⚠️ | Torreilles › Perpignan Méditerranée Métropole | 1 |
| Forêt de Formiguères (140) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (155) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (158) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (163) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (170) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (174) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (187) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (191) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (230) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (231) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (233) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (234) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (235) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (267) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (278) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (293) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (300) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (314) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (324) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Vivès (4) ⚠️ | Vivès › Vallespir | 1 |
| Forêt de Brouilla (2) ⚠️ | Brouilla › Aspres | 1 |
| Parc d'activités Le Clos d'en Cante ⚠️ | Espira-de-l'Agly › Perpignan Méditerranée Métropole | 1 |
| Bois de Valmanya (2) ⚠️ | Valmanya › Conflent-Canigó | 1 |
| Bois de Valmanya (3) ⚠️ | Valmanya › Conflent-Canigó | 1 |
| Bois des Angles ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (15) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Le Jardin des Feuillages ⚠️ | Perpignan › Perpignan Méditerranée Métropole | 1 |
| Forêt de Cabestany ⚠️ | Cabestany › Perpignan Méditerranée Métropole | 1 |
| Parc de Canet-en-Roussillon (8) ⚠️ | Canet-en-Roussillon › Perpignan Méditerranée Métropole | 1 |
| Bois de Canet-en-Roussillon (2) ⚠️ | Canet-en-Roussillon › Perpignan Méditerranée Métropole | 1 |
| Espace de détente Las Palades ⚠️ | Bompas › Perpignan Méditerranée Métropole | 1 |
| Parc du Barcarès (5) ⚠️ | Le Barcarès › Perpignan Méditerranée Métropole | 1 |
| Parc du Barcarès (6) ⚠️ | Le Barcarès › Perpignan Méditerranée Métropole | 1 |
| Forêt de Cabestany (3) ⚠️ | Cabestany › Perpignan Méditerranée Métropole | 1 |
| Parc de Rivesaltes (2) ⚠️ | Rivesaltes › Perpignan Méditerranée Métropole | 1 |
| Forêt de Cabestany (4) ⚠️ | Cabestany › Perpignan Méditerranée Métropole | 1 |
| Forêt de Saint-Cyprien (2) ⚠️ | Saint-Cyprien › Sud-Roussillon | 1 |
| Bois de Oms (3) ⚠️ | Oms › Aspres | 1 |
| Bois de Oms (8) ⚠️ | Oms › Aspres | 1 |
| Bois de Oms (9) ⚠️ | Oms › Aspres | 1 |
| Bois de Oms (11) ⚠️ | Oms › Aspres | 1 |
| Bois de Oms (29) ⚠️ | Oms › Aspres | 1 |
| Bois de Calmeilles (3) ⚠️ | Calmeilles › Aspres | 1 |
| Forêt de Bompas (3) ⚠️ | Bompas › Perpignan Méditerranée Métropole | 1 |
| Forêt de Bompas (4) ⚠️ | Bompas › Perpignan Méditerranée Métropole | 1 |
| Bois de Saint-Cyprien (3) ⚠️ | Saint-Cyprien › Sud-Roussillon | 1 |
| Bois de Saint-Estève (4) ⚠️ | Saint-Estève › Perpignan Méditerranée Métropole | 1 |
| Espace Marcel et Serge Padrines ⚠️ | Pézilla-la-Rivière › Perpignan Méditerranée Métropole | 1 |
| Parc de la Mairie (2) ⚠️ | Ponteilla › Perpignan Méditerranée Métropole | 1 |
| Forêt de Camélas (10) ⚠️ | Camélas › Aspres | 1 |
| Bois de Néfiach (2) ⚠️ | Néfiach › Roussillon Conflent | 1 |
| Forêt de Millas (2) ⚠️ | Millas › Roussillon Conflent | 1 |
| Bois de Perpignan (3) ⚠️ | Perpignan › Perpignan Méditerranée Métropole | 1 |
| Forêt de Toulouges ⚠️ | Toulouges › Perpignan Méditerranée Métropole | 1 |
| Forêt du Soler (4) ⚠️ | Le Soler › Perpignan Méditerranée Métropole | 1 |
| Forêt du Soler (11) ⚠️ | Le Soler › Perpignan Méditerranée Métropole | 1 |
| Forêt du Soler (12) ⚠️ | Le Soler › Perpignan Méditerranée Métropole | 1 |
| Forêt du Soler (14) ⚠️ | Le Soler › Perpignan Méditerranée Métropole | 1 |
| Bois de Thuir ⚠️ | Thuir › Aspres | 1 |
| Parc du Bicentenaire ⚠️ | Saint-Nazaire › Perpignan Méditerranée Métropole | 1 |
| Forêt de Caudiès-de-Fenouillèdes (18) ⚠️ | Caudiès-de-Fenouillèdes › Agly Fenouillèdes | 1 |
| Forêt de Caudiès-de-Fenouillèdes (26) ⚠️ | Caudiès-de-Fenouillèdes › Agly Fenouillèdes | 1 |
| Forêt de Saint-Paul-de-Fenouillet (6) ⚠️ | Saint-Paul-de-Fenouillet › Agly Fenouillèdes | 1 |
| Parc de Prugnanes ⚠️ | Prugnanes › Agly Fenouillèdes | 1 |
| Forêt de Saint-Paul-de-Fenouillet (13) ⚠️ | Saint-Paul-de-Fenouillet › Agly Fenouillèdes | 1 |
| Forêt de Campoussy (2) ⚠️ | Campoussy › Agly Fenouillèdes | 1 |
| Jardin Taulera ⚠️ | Alénya › Sud-Roussillon | 1 |
| Parc de Canohès ⚠️ | Canohès › Perpignan Méditerranée Métropole | 1 |
| Jardin des Métiers d'Art ⚠️ | Elne › Albères – Côte Vermeille – Illibéris | 1 |
| Parc-en-ciel ⚠️ | Amélie-les-Bains-Palalda › Haut-Vallespir | 1 |
| Forêt de Argelès-sur-Mer (12) ⚠️ | Argelès-sur-Mer › Albères – Côte Vermeille – Illibéris | 1 |
| Espace Patrick Bourrat ⚠️ | Perpignan › Perpignan Méditerranée Métropole | 1 |
| Parc de Vernet-les-Bains (2) ⚠️ | Vernet-les-Bains › Conflent-Canigó | 1 |
| Bois de Ille-sur-Têt (2) ⚠️ | Bouleternère › Roussillon Conflent | 1 |
| Forêt de Saint-Pierre-dels-Forcats (44) ⚠️ | Saint-Pierre-dels-Forcats › Pyrénées catalanes | 1 |
| Espace Étienne Maso ⚠️ | Terrats › Aspres | 1 |
| Le Viaduc ⚠️ | Brouilla › Aspres | 1 |
| Forêt de Puyvalador (94) ⚠️ | Puyvalador › Pyrénées catalanes | 1 |
| Forêt de Castelnou (2) ⚠️ | Castelnou › Aspres | 1 |
| Bois de la Ciurède ⚠️ | Saint-Génis-des-Fontaines › Albères – Côte Vermeille – Illibéris | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (25) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Saint-Pierre-dels-Forcats (5) ⚠️ | Saint-Pierre-dels-Forcats › Pyrénées catalanes | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (39) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (40) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (57) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (78) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (81) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (84) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (122) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (123) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (129) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (136) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (139) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (143) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (149) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (153) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (155) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (158) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (160) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (162) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (164) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (166) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (169) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (174) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (175) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (176) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (177) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (178) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (180) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (185) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (188) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Porté-Puymorens (5) ⚠️ | Porté-Puymorens › Pyrénées Cerdagne | 1 |
| Bois de Porté-Puymorens (7) ⚠️ | Porté-Puymorens › Pyrénées Cerdagne | 1 |
| Bois de Porté-Puymorens (10) ⚠️ | Porté-Puymorens › Pyrénées Cerdagne | 1 |
| Bois de Porté-Puymorens (11) ⚠️ | Porté-Puymorens › Pyrénées Cerdagne | 1 |
| Bois de Porté-Puymorens (14) ⚠️ | Porté-Puymorens › Pyrénées Cerdagne | 1 |
| Bois de Porté-Puymorens (15) ⚠️ | Porté-Puymorens › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (200) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (202) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (203) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (213) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (214) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (216) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (220) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (228) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (246) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (272) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (289) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (293) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (301) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (349) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (365) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois des Angles (8) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (375) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (379) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (380) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (390) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Formiguères (5) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (399) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (415) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (458) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Porté-Puymorens (38) ⚠️ | Porté-Puymorens › Pyrénées Cerdagne | 1 |
| Bois de Porté-Puymorens (40) ⚠️ | Porté-Puymorens › Pyrénées Cerdagne | 1 |
| Bois de Planès (2) ⚠️ | Planès › Pyrénées catalanes | 1 |
| Bois de Taurinya (5) ⚠️ | Taurinya › Conflent-Canigó | 1 |
| Bois de Néfiach (6) ⚠️ | Néfiach › Roussillon Conflent | 1 |
| Bois de Bélesta ⚠️ | Bélesta › Roussillon Conflent | 1 |
| Forêt de Latour-Bas-Elne ⚠️ | Latour-Bas-Elne › Sud-Roussillon | 1 |
| Bois de Fontpédrouse (4) ⚠️ | Fontpédrouse › Conflent-Canigó | 1 |
| Bois de Fontpédrouse (6) ⚠️ | Fontpédrouse › Conflent-Canigó | 1 |
| Bois de Fontpédrouse (11) ⚠️ | Fontpédrouse › Conflent-Canigó | 1 |
| Forêt de Cabestany (6) ⚠️ | Cabestany › Perpignan Méditerranée Métropole | 1 |
| Mas Pams ⚠️ | Bompas › Perpignan Méditerranée Métropole | 1 |
| Forêt de Elne (2) ⚠️ | Elne › Albères – Côte Vermeille – Illibéris | 1 |
| Bois de Caramany (2) ⚠️ | Caramany › Agly Fenouillèdes | 1 |
| Bois de Cassagnes (2) ⚠️ | Cassagnes › Perpignan Méditerranée Métropole | 1 |
| Forêt de Estagel ⚠️ | Estagel › Perpignan Méditerranée Métropole | 1 |
| Forêt de Pia (3) ⚠️ | Pia › Corbières Salanque Méditerranée | 1 |
| Forêt de Pia (6) ⚠️ | Pia › Corbières Salanque Méditerranée | 1 |
| Bois de Caramany (3) ⚠️ | Caramany › Agly Fenouillèdes | 1 |
| Bois de Argelès-sur-Mer (4) ⚠️ | Argelès-sur-Mer › Albères – Côte Vermeille – Illibéris | 1 |
| Bois de Argelès-sur-Mer (6) ⚠️ | Argelès-sur-Mer › Albères – Côte Vermeille – Illibéris | 1 |
| Forêt de Nahuja ⚠️ | Nahuja › Pyrénées Cerdagne | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (473) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Enveitg (15) ⚠️ | Enveitg › Pyrénées Cerdagne | 1 |
| Bois de Enveitg (26) ⚠️ | Enveitg › Pyrénées Cerdagne | 1 |
| Bois de Ur (6) ⚠️ | Ur › Pyrénées Cerdagne | 1 |
| Bois de Villelongue-dels-Monts ⚠️ | Villelongue-dels-Monts › Albères – Côte Vermeille – Illibéris | 1 |
| Forêt du Barcarès (7) ⚠️ | Le Barcarès › Perpignan Méditerranée Métropole | 1 |
| Forêt du Barcarès (12) ⚠️ | Le Barcarès › Perpignan Méditerranée Métropole | 1 |
| Forêt de Formiguères (339) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (343) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (345) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (346) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (350) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (358) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (362) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Formiguères (368) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Forêt de Angoustrine-Villeneuve-des-Escaldes (6) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Forêt des Angles (163) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (166) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt des Angles (175) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Bois de Saint-André ⚠️ | Saint-André › Albères – Côte Vermeille – Illibéris | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (474) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Forêt de Corneilla-la-Rivière ⚠️ | Corneilla-la-Rivière › Perpignan Méditerranée Métropole | 1 |
| Bois de Pézilla-la-Rivière (5) ⚠️ | Pézilla-la-Rivière › Perpignan Méditerranée Métropole | 1 |
| Bois de Pézilla-la-Rivière (6) ⚠️ | Pézilla-la-Rivière › Perpignan Méditerranée Métropole | 1 |
| Bois de Corneilla-la-Rivière ⚠️ | Corneilla-la-Rivière › Perpignan Méditerranée Métropole | 1 |
| Forêt de Pézilla-la-Rivière ⚠️ | Pézilla-la-Rivière › Perpignan Méditerranée Métropole | 1 |
| Forêt de Montner (2) ⚠️ | Montner › Perpignan Méditerranée Métropole | 1 |
| Bois de Montner (2) ⚠️ | Montner › Perpignan Méditerranée Métropole | 1 |
| Forêt de Peyrestortes (10) ⚠️ | Peyrestortes › Perpignan Méditerranée Métropole | 1 |
| Bois de Estagel (5) ⚠️ | Estagel › Perpignan Méditerranée Métropole | 1 |
| Bois de Estagel (7) ⚠️ | Estagel › Perpignan Méditerranée Métropole | 1 |
| Bois de Calce (2) ⚠️ | Calce › Perpignan Méditerranée Métropole | 1 |
| Bois de Latour-Bas-Elne ⚠️ | Latour-Bas-Elne › Sud-Roussillon | 1 |
| Bois de Trouillas (4) ⚠️ | Trouillas › Aspres | 1 |
| Bois de Trouillas (5) ⚠️ | Trouillas › Aspres | 1 |
| Parc Chocolat ⚠️ | Font-Romeu-Odeillo-Via › Pyrénées catalanes | 1 |
| Forêt de Port-Vendres ⚠️ | Port-Vendres › Albères – Côte Vermeille – Illibéris | 1 |
| Forêt de Port-Vendres (3) ⚠️ | Port-Vendres › Albères – Côte Vermeille – Illibéris | 1 |
| Forêt de Banyuls-sur-Mer (5) ⚠️ | Banyuls-sur-Mer › Albères – Côte Vermeille – Illibéris | 1 |
| Forêt de Banyuls-sur-Mer (6) ⚠️ | Banyuls-sur-Mer › Albères – Côte Vermeille – Illibéris | 1 |
| Forêt de Rivesaltes (8) ⚠️ | Rivesaltes › Perpignan Méditerranée Métropole | 1 |
| Bois de Baillestavy ⚠️ | Baillestavy › Conflent-Canigó | 1 |
| Cœur de vie ⚠️ | Torreilles › Perpignan Méditerranée Métropole | 1 |
| Parc Ducup ⚠️ | Perpignan › Perpignan Méditerranée Métropole | 1 |
| Forêt de Banyuls-sur-Mer (7) ⚠️ | Banyuls-sur-Mer › Albères – Côte Vermeille – Illibéris | 1 |
| Jardins de la Basse ⚠️ | Perpignan › Perpignan Méditerranée Métropole | 1 |
| Forêt de Collioure (5) ⚠️ | Collioure › Albères – Côte Vermeille – Illibéris | 1 |
| Forêt de Collioure (6) ⚠️ | Collioure › Albères – Côte Vermeille – Illibéris | 1 |
| Forêt de Banyuls-sur-Mer (8) ⚠️ | Banyuls-sur-Mer › Albères – Côte Vermeille – Illibéris | 1 |
| Forêt de Banyuls-sur-Mer (20) ⚠️ | Banyuls-sur-Mer › Albères – Côte Vermeille – Illibéris | 1 |
| Parc de Elne (6) ⚠️ | Elne › Albères – Côte Vermeille – Illibéris | 1 |
| Forêt de Banyuls-sur-Mer (30) ⚠️ | Banyuls-sur-Mer › Albères – Côte Vermeille – Illibéris | 1 |
| La forêt nourricière Suzanne Noël ⚠️ | Elne › Albères – Côte Vermeille – Illibéris | 1 |
| Forêt de Caramany (4) ⚠️ | Caramany › Agly Fenouillèdes | 1 |
| Bois de la Rivière ⚠️ | Saint-Féliu-d'Amont › Roussillon Conflent | 1 |
| Forêt de Targasonne (4) ⚠️ | Targasonne › Pyrénées Cerdagne | 1 |
| Forêt de Los Masos (8) ⚠️ | Los Masos › Conflent-Canigó | 1 |
| Forêt des Angles (181) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Bois de Vingrau (6) ⚠️ | Vingrau › Perpignan Méditerranée Métropole | 1 |
| Bois des Angles (17) ⚠️ | Les Angles › Pyrénées catalanes | 1 |
| Forêt de Formiguères (376) ⚠️ | Formiguères › Pyrénées catalanes | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (476) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Eyne (7) ⚠️ | Eyne › Pyrénées catalanes | 1 |
| Forêt de Lamanère (3) ⚠️ | Lamanère › Haut-Vallespir | 1 |
| Forêt de Coustouges (4) ⚠️ | Coustouges › Haut-Vallespir | 1 |
| Forêt de Prats-de-Mollo-la-Preste (25) ⚠️ | Prats-de-Mollo-la-Preste › Haut-Vallespir | 1 |
| Parc de Elne (7) ⚠️ | Elne › Albères – Côte Vermeille – Illibéris | 1 |
| Bois de Angoustrine-Villeneuve-des-Escaldes (478) ⚠️ | Angoustrine-Villeneuve-des-Escaldes › Pyrénées Cerdagne | 1 |
| Bois de Enveitg (29) ⚠️ | Enveitg › Pyrénées Cerdagne | 1 |
| Forêt de Port-Vendres (12) ⚠️ | Port-Vendres › Albères – Côte Vermeille – Illibéris | 1 |
| Forêt de Banyuls-sur-Mer (41) ⚠️ | Banyuls-sur-Mer › Albères – Côte Vermeille – Illibéris | 1 |
| Forêt de Port-Vendres (17) ⚠️ | Port-Vendres › Albères – Côte Vermeille – Illibéris | 1 |
| Forêt de Port-Vendres (18) ⚠️ | Port-Vendres › Albères – Côte Vermeille – Illibéris | 1 |

2 099 parc(s) plus petits qu'une cellule ne sont pas listés : la carte les dessine, mais ils n'offrent aucune cellule.

⚠️ 3084 parc(s) hors de la fenêtre 10–125 cellules (2994 trop petit(s), 90 trop grand(s)) : affichés sur la carte, mais ils ne peuvent pas servir de cible à un défi.

## Zones restreintes

Cellules soustraites du dénominateur de leur zone : on ne peut pas demander à quelqu'un de marcher sur une piste d'atterrissage.

| Catégorie | Cellules déclarées |
|---|---:|
| military | 1 456 |
| airport | 158 |
| prison | 3 |
| **Total déclaré** | **1 617** |
| dont dans une zone de ce territoire | 1 615 |

Le jeu de données couvre plus large que le territoire — il est produit à une échelle supérieure. Seules les cellules tombant dans une zone d'ici pèsent sur un pourcentage.

### Zones concernées

| Zone | Cellules exclues |
|---|---:|
| Salses-le-Château | 286 |
| Ayguatébia-Talau | 230 |
| Espira-de-l'Agly | 186 |
| Tautavel | 184 |
| Vingrau | 141 |
| Opoul-Périllos | 128 |
| Rivesaltes | 111 |
| Cases-de-Pène | 98 |
| Sauto | 62 |
| Perpignan | 61 |
| Saint-Laurent-de-la-Salanque | 52 |
| La Llagonne | 22 |
| Sainte-Léocadie | 15 |
| Mont-Louis | 13 |
| Canaveilles | 12 |
| Peyrestortes | 6 |
| Collioure | 4 |
| Torreilles | 4 |

---

Données dérivées d'OpenStreetMap et de données ouvertes publiques, sous licence **ODbL**.
