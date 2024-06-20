# Types de systèmes de coordonnées

Comme déjà rapidement vu, il existe deux types de systèmes de coordonnées que nous allons voir plus en détail dans les prochaines sections:

<img style="display: block; margin: 0 auto;" src="assets/grid2.png">

1. Système de coordonnées **géographiques** (SCG)
    * en anglais : Geographic coordinate systeme (GCS)
    * Ce système convient bien aux représentations globales et en 3D (c-à-d sphérique et sans déformation) de la terre
    * Appelé aussi Système de coordonnées globales, sphériques ou universelles
    * Les coordonnées sont lues en **latitude** et **longitude**, exprimées en **degré**
    * Exemple : 
        * Coordonnées géographiques (lat/long): 46°31′35.605″N 6°34′45.834″E

2. Système de coordonnées **projetées** (SCP)
    * en anglais : Projected coordinate systeme (PCS)
    * Aussi appelé Système de coordonnées planes ou cartgraphiques
    * Unité de mesure **X** et **Y**, représenté donc sur un plan en 2D avec deux axes (présence parfois de l'altitude exprimée avec un troisième axe **Z**)
    * Coordonnées exprimées en **unité** linéaires (mètres, miles, ...)
    * Exemple :
        * Coordonnées projetées (mètres): 2'534'073.5, 1'153'168.5

Les deux types de systèmes sont des systèmes de référence spatiale (SRS; Spatial Reference System), aussi connus sous le nom de «Coordinate Reference System» (CRS).

La différence entre ces deux types de systèmes de coordonnées est fondamentale. En principe, on ne pourra pas utiliser un GCS pour faire une carte sur un support plat; il faudra toujours utiliser un PCS pour cela.

Dans la pratique, un logiciel SIG vous permettra de faire une carte en utilisant un GCS. Il fera ça tout simplement en prenant les angles de latitude pour l'axe Y de l'écran, et les angles de longitude pour l'axe X de l'écran...

