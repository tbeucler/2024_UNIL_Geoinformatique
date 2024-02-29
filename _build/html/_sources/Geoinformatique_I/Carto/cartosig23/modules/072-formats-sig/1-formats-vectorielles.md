# Formats de données vectorielles

Ci-dessous vous trouvez une description rapide des principaux formats vectoriels que nous rencontrons dans le travail quotidien avec les SIG. Certains des formats supportent également des formats raster; dans ce cas c'est mentionné sous le format concerné. C'est le cas notamment des File Geodatabases et GeoPackages, deux formats très importants dans le monde ESRI pour le premier, et dans le monde des SIG libres pour le deuxième.

Évidemment le but n'est pas d'apprendre par coeur ces formats, mais de venir consulter ces informations au besoin.

## ESRI Shape

Le fichier Shape est un vieux format introduit par ESRI en 1998. Ce format binaire est propriétaire mais bien connu. C'est probablement le format le plus utilisé pour échanger des données vectorielles, malgré quelques limitations.

Une caractéristique des format Shape est qu'il ne s'agit pas d'un seul fichier, mais d'une série de fichiers qui partagent le même nome mais une extension différente. Malgré cela, on va parler d'«un fichier Shape» même si en réalité il s'agit de plusieurs fichiers:

- Le fichier avec l'extension `.shp` contient les géométries
- Le fichier `.dbf` contient les attributs
- Le fichier `.shx` permet de lier les géométries aux attributs
- Le fichier `.prj` est en principe optionnel. Il contient la référence spatial et du coup il est tout de même très utile.

Dans un fichier Shape, on peut avoir un seul type de géométrie par couche.

Les noms des attributs sont limités à 11 caractères.

Seulement un nombre limité de types d'attributs est possible: les textes, les nombres (avec ou sans décimales) et les dates (sans l'heure).

Le nombre d'attributs (donc de colonnes) est limité aussi.

Le format Shape ne permet pas d'enregistrer ce qu'on appelle la topologie. Du coup, si on a par exemple les limites administratives, la frontière partagée entre deux entités sera représentée deux fois dans le fichier, avec le risque qu'elles ne se superposent pas parfaitement bien.


## ESRI Geodatabase

Format propriétaire d’ESRI pour ArcGIS.

3 versions:

- **File Geodatabase**: utilise des fichiers pour stocker les données.

- **Personal Geodatabase**: utilise une base de données Microsoft Access pour stocker les données

- **Enterprise Geodatabase**: utilise un serveur Microsoft SQL Server pour stocker les données de manière centrale

- File Geodatabase peut être lu et écrit par beaucoup de logiciels SIG (grâce à OGR).
- Personal Geodatabase est limité à 2 Go et Windows
- File Geodatabase est devenu le format le plus fréquent dans le monde ArcGIS
- Plusieurs couches et autres informations dans le même jeu de données


## GeoPackage

- Standard ouvert et indépendant pour stocker des données géographiques
- Supporte données vectorielles et raster
- Plusieurs couches sont stockées dans le même fichier
- Utilise un fichier de base de données SQLite standard avec un format de stockage particulier
- Possibilité d’utiliser le langage SQL
- Possibilité de stocker des styles avec les couches dans QGIS
- Supporté par OGR/GDAL, QGIS et beaucoup d’autres
- Supporté entièrement depuis ArcGIS Pro 2.6 (avec édition)
- Remplacement pratique et performant pour le format Shape


## INTERLIS

- Format standardisé pour décrire, stocker et échanger des données géographiques
- Langage permettant de **modéliser les objets** décrits, donnant un modèle de données sémantique
- Standard utilisé notamment par les autorités suisses (dont Swisstopo) et ancré dans la loi sur la géoinformation
- Supporté par OGR/GDAL, QGIS et FME
-  Logiciels de conversion pour GeoPackage, ESRI Geodatabase et PostGIS


## Bases de données spatiales

- Souvent, les données SIG sont gérées dans des bases de données relationnelles (bases de données SQL) avec extension spatiale

- Une BD relationnelle contient une série de tables. Les colonnes ont un type précis (p.ex. texte, nombre entier, etc.)

- Colonne de type «géométrie»

- Traitements possibles, p.ex. projections, calculs de distance, intersection de géométries, zones tampon etc.

- Les bases de données spatiales les plus connues:
    - PostgreSQL / [PostGIS](http://postgis.org/)
    - SQLite Spatial
    - Oracle Spatial

- Bases de données très efficaces pour les requêtes et beaucoup de calculs

- SIG sans la partie affichage...


## OpenStreetMap

[OpenStreetMap](https://www.openstreetmap.org/) n'est en principe pas un format de données, mais il s'agit d'une source de données cartographiques mondiales qui sont libres. En même temps, les données OpenStreetMap viennent dans un format qui leur est spécifique.

- Format de données très différent des formats SIG habituels
- Format topologique
- Tous les objets sont dans «une seule couche» (car le principe des couches n’y existe pas)
- Fichiers .osm.pbf
- Utilisé essentiellement pour importer les données OSM dans les SIG
- Supporté par OGR/GDAL et QGIS
- Nécessite un traitement (typiquement un filtrage) pour être utile dans un SIG

Des données extraites par pays ou région et utilisables directement dans les SIG sont disponibles pour téléchargement à l'adresse [https://download.geofabrik.de](https://download.geofabrik.de/). Certaines des données sont également disponibles en format Shape, format qui est plus répandu dans les SIG...

