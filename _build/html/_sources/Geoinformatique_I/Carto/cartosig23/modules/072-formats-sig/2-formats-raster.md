# Formats de données raster

## GeoTIFF

- Il s’agit d’un fichier TIFF
- C’est donc un format pour images, un peu comme JPEG mais sans perte
- Possibilité de stocker la référence géographique de deux manières:
    - dans les métadonnées à l’intérieur du fichier TIFF
    - dans un fichier à part appelé «world file» (même nom, mais extension .tfw)

## Les «world files»

- Possibilité d’ajouter un référence géographique à n’importe quelle image

- Le nom de fichier est le même, mais l’extension diffère:
    - .tif + .tfw
    - .jpg + .jgw
    - .png + .pgw

- Ne contient pas d’indication sur le système de référence spatial utilisé
- Le world file est dans le fond un fichier texte avec un contenu ressemblant à:

![](assets/world-file.png)


## Erdas Imagine

- Erdas est un logiciel de traitement d’images satellites et photos aériennes
- Fichiers avec extension .img
- Format propriétaire mais connu en grande partie
- Compatible avec OGR/GDAL et QGIS ainsi qu'ArcGIS


## ASCII Grid (XYZ)

- Format texte avec valeurs de pixels sous forme de texte
- Plusieurs variantes existent, p.ex. pour ESRI Arc/info et GRASS GIS
- Avantage: possibilité d’inspecter les fichiers avec un éditeur de texte
- Désavantage: taille des fichiers importante
- Utile notamment pour transférer des données
- Compatible avec à peu près tous les logiciels SIG supportant des données raster
- À ne pas confondre avec d’autres formats XYZ, p.ex. Lidar XYZ

