# Calculatrice raster

La calculatrice raster permet d’effectuer n’importe quelle opération arithmétique sur des images raster (ou pour les images multi-bandes sur toutes les bandes). Ainsi, nous pouvons p.ex.

- Sortir les zones avec pentes supérieures à 25° d'une couche raster de la pente (nous allons voir un peu plus tard comment créer une telle couche)

- Calculer un indice comme le NDVI (Normalized Difference Vegetation Index) qui permet de quantifier la végétation. Le NDVI se calcule sur la base d'images satellites Landsat ou Sentinel-2 avec la formule suivante:

    $$NDVI = \frac{NIR - Red}{NIR + Red}$$

La calculatrice raster se cache sous l’outil QGIS **Raster calculator**:

![](assets/raster-calc.png)

Elle permet de faire des opérations sur les pixels de différentes couches raster. La calculatrice raster ne permet pas de travailler avec des couches vectorielles.

Nous pouvons évidemment faire beaucoup d'autres calculs avec la calculatrice raster. Le concept est finalement très facile à comprendre. Par contre, assurez-vous de prendre toujours des couches raster qui ont le même système de coordonnées, autrement les calculs ne seront souvent pas justes.
