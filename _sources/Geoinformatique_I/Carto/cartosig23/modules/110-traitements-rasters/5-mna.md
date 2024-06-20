# Modèle numérique d'altitude (MNA)

Dans cette étape nous regardons quelques opérations de base que nous pouvons faire avec un modèle numérique d’altitude. Afin de mettre en pratique ces opérations nous utiliserons les données suivantes :

<ul>
<li><a href="assets/mnt25_ch.zip"><i class="far fa-file"></i> MNT25 - Modèle numérique de terrain de Swisstopo avec une résolution de 25 mètres</a></li>

<li><a href="assets/region-etude-TI-Nord.zip"><i class="far fa-file"></i> Région d'étude: Nord-Est du Tessin</a></li>
</ul>

La couche raster du MNT25 est en format ESRI GRID. La couche correspond au dossier entier mnt25_ch. Pour ajouter la couche au projet QGIS, vous devez charger le fichier `hdr.adf` qui se trouve à l’intérieur de ce dossier. Mais conservez dans tous les cas toujours le dossier entier, sinon la couche raster sera corrompue. Et ensuite, il faudra encore spécifier le système de coordonnées dans les propriétés de la couche (le MNT25 est en CH1903/LV03).

Avant de passer aux opérations sur la base d’un modèle numérique d’altitude, découpez la couche raster selon la région d'étude pour réduire son étendue.

## Inspecter le modèle numérique d'altitude

Le modèle numérique d'altitude (MNA), aussi appelé modèle numérique de terrain (MNT) contient pour chaque pixel l'altitude moyenne de la région sous le pixel. Ainsi, nous pouvons obtenir l'altitude approximative de chaque point en utilisant les outils d'inspection dans le SIG :

![](assets/altitude-mnt.webp)

En l’occurrence, l’endroit du curseur a donc une altitude de 4268.1 mètres. Il s'agit de **l'altitude du terrain sans couverture**, c'est-à-dire sans des objets comme les bâtiments ou les arbres. Un modèle numérique où les bâtiments, arbres, etc. sont présents est appelé **« modèle numérique de surface »**.


## Calcul du relief à partir du MNA

Le modèle numérique d'altitude permet de calculer plusieurs choses, dont une image du relief. Il y a d'un côté le relief ombré, et de l'autre côté une représentation en couleurs du relief qui peuvent être calculées.

L’outil **Hillshade** (ombrage) permet de calculer un relief ombré en niveaux de gris qui est parfait comme fond pour la cartographie d’une région de montagne :

![](assets/hillshade.webp)

Le relief ombré peut être calculé avec l’outil «Hillshade» de QGIS, accessible dans la boîte d’outil de géotraitement. Dans ArcGIS, la fonction est accessible dans ArcToolbox, sous «Spatial Analyst Tools > Surface > Hillshade».

Un autre outil **«Relief»** permet de calculer une image en couleurs du relief :

![](assets/relief.webp)

Bien évidemment, ces couches ne seront utiles que pour une représentation cartographique et non pas pour des analyses.


## Calcul de la pente et l'orientation

Il est possible de déterminer la pente (en degrés) à partir du MNA, à l'aide de l'outil **Slope**.

L’orientation de chaque endroit peut être déterminé avec l’outil **Aspect**. Il calcule l’orientation de chaque endroit en fonction du Nord, en degrés. Le Nord correspondant à la valeur 0 degré, Est à la valeur 90°, le Sud est représenté par la valeur 180°, etc.
