# Découper une image raster

Dans la section sur les orthophotos, nous avons rencontré l'outil **merge** qui permet de fusionner différentes images raster en une seule couche. Un autre outil important est l'outil de **découpage** d'une image raster. Il permet de limiter l'étendue spatiale de la couche et ainsi réduire le volume des données à traiter. Étant donné que les images raster sont souvent très grandes, il est fortement recommandé de faire une analyse uniquement sur la portion du territoire qu'il nous faut.

L'outil de découpage est disponible dans la Processing Toolbox de QGIS sous «GDAL > Raster extraction > Clip raster by extent». Dans le dialogue qui suit, il faut spécifier les paramètres suivants:

- la couche d'entrée

- l'étendue («Clipping extent»). Si vous avez déjà une couche avec l'étendue ça peut se faire grace au menu caché sous le bouton à droite et l'option «Calculate from layer».

- le fichier de sortie

![](assets/clip-raster.png)