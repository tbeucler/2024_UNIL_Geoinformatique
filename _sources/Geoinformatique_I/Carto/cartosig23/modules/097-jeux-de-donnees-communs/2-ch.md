# Données pour la Suisse

De manière générale, il est utile de toujours vérifier les catalogues de métadonnées (géocatalogue). Le géocatalogue de la Confédération se trouve à l'URL [www.geocat.ch/](https://www.geocat.ch).

Il y a aussi la plupart des cantons qui ont des géocatalogues ainsi que certaines grandes villes.

## Données Swisstopo

Swisstopo est certainement le fournisseur de géodonnées le plus important pour la Suisse. Il vaut la peine d'aller consulter la section [Géodonnées et applications](https://www.swisstopo.admin.ch/fr/geodata.html) du site Web de Swisstopo. On y trouve l'ensemble des données qui nous sont utiles pour la cartographie. La plupart de ces données sont en plus gratuites.

Les jeux de données Swisstopo les plus importants sont:

- __Modèles du territoire__:
    - __swissTLM3D__: modèle topographique du paysage (__T__opographisches __L__andschafts__m__odell). _«Jeu de données vectorielles en 3D le plus précis et le plus complet de la Suisse.»_
    - __swissBUILDINGS3D__: bâtiments, y compris leur hauteur. Version 1.0: sans description du toit (toit plat), version 2.0: avec la forme complète du bâtimenet (simplifié).
    - __swissBOUNDARIES3D__: limites administratives (communes, cantons, etc.)
    - __swissNAMES3D__: noms géographiques (noms de lieux etc.), lié étroitement avec le TLM3D et les cartes nationales.
    - __swissTLMRegio__ (anciennement VECTOR200): modèle vectoriel (en 2D) pour les petites et moyennes échelles; à la base de la carte 1:200'000.

- __Modèles du terrain__:  
    modèle numérique de terrain (MNT), modèle numérique de surface (MNS)
    - swissALTI3D: MNT de grande précision
    - MNT25: MNT sur la base de la carte nationale 1:25'000 (CN25)
    - MNT25/200: MNT sur la base de CN25, mais résolution de 200 mètres
    - MNS: modèle numérique de surface: pas mis à jour!

- __Orthophotos__ (photos aériennes orthorectifiés, images satellites)
    - SWISSIMAGE: orthopothos mises à jour tous les 3 ans
    - SWISSIMAGE RS: orthophotos avec 4 canaux: rouge, vert, bleu et proche infrarouge
    - SWISSIMAGE FCIR: orthophotos infrarouge fausses couleurs
    - CITIMAGE: orthopothos de très haute résolution (25cm) pour quelques villes majeures
    - Spot: images du satellite européen Spot
    - Landsat: images du satellite américain Landsat

- __Cartes nationales__
    - __Swiss Map Raster__ (25, 50, 100, 200, 500, 1000): toutes les cartes nationales sous forme de couches raster. Également disponible en noir/blanc, avec ou sans relief.
        - Avantage: même représentation que les cartes imprimées.
        - Inconvénient: impossible de sélectionner uniquement une partie des informations.
    - __Swiss Map Vector__ (25, 500, 1000). Permet de construire la carte nationale à partir de couches vectorielles. Gratuit pour 500 et 1000. Dans certains cas, Swisstopo fournit un projet QGIS ou ArcGIS contenant le style de la carte nationale (très instructif!).


- __Cartes géologiques__
    - différents formats et variantes, dont aussi couches vectorielles


## Données de l'Office fédéral de la statistique

L'OFS propose essentiellement des données statistiques à des échelles différentes (surtout pour la Suisse entière, par cantons et par communes).

Parmi les recensement exhaustifs, il y a notamment les jeux de données suivants:
- STATPOP (statistiques de la population): pour la population, ménages et bâtiments; par communes
- STATENT (statistiques des entreprises); par communes

L'OFS conduit aussi de nombreux recensements partiels (micro-recensements), dont p.ex. le micro-recensement sur la mobilité. Ces jeux de données donnent un aperçu général et global sur une thématique précise, mais généralement il n'est pas possible de les utiliser pour la cartographie étant donné que la représentativité statistique à travers l'espace géographique n'est pas garantie. Il faut consulter la documentation du jeu de données pour le savoir.

L'OFS propose aussi des données spatiales avec le jeu de données [GEOSTAT](http://www.geostat.admin.ch/). Ce jeu de données propose notamment les recensements STATPOP et STATENT à l'échelle de l'hectare.

Pour obtenir les donneés de l'OFS, il suffit généralement de passer par le site Web, car la plupart des données s'y trouve en accès libre.

Pour certaines données, notamment à l'échelle des communes, on peut passer par l'__application interactive__ de recherche et d'extraction de données __STAT-TAB__ ([https://www.pxweb.bfs.admin.ch](https://www.pxweb.bfs.admin.ch))

L'OFS propose aussi des données géographiques: les données GEOSTAT. Il y a des données sur l'utilisation du sol et aussi des données sur la population et les entreprises à l'échelle de l'hectare.

## Les données cantonales

En règle générale, chaque canton possède un office pour les données géographiques. Souvent, il y a aussi un géoportail cantonal pour les données géographiques, parfois avec possibilité de téléchargement de données.

Souvent, surtout dans les grands cantons, il y a également un office pour les données statistiques.
