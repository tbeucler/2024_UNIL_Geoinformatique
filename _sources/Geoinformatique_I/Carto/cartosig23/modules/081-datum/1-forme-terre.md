# La forme de la Terre

La forme réelle de la terre est une sorte de **patatoïde**. Elle est très irrégulière, allant du fond des océans aux sommets des montagnes.

La formée *idéalisée, lissée* de ce patatoïde correspond à un ***géoïde***. Sa forme reste relativement irrégulière.

<img src="assets/geoide_transp.png" style="display: block; margin: 0 auto;">

Afin de mieux calculer les objets sur la surface terrestre, il faut donc un modèle encore plus simple : **l'ellipsoïde**

Le **géoïde** (en vert sur la figure ci-dessous) ne prend pas en compte toutes les hétérogénéités de la surface terrestre mais est essentiel pour reproduire la forme réelle de la Terre. On peut se représenter le géoïde comme étant le niveau moyen de la mer prolongé sous les continents ([Swisstopo](https://www.swisstopo.admin.ch/fr/connaissances-faits/mensuration-geodesie/geoide.html "Géoïde d'après Swisstopo")). Il correspond à *la surface équipotentielle particulière du champ de pesanteur terrestre.* En d'autres termes, en tout point à la surface du géoïde, la force de gravité est la même.

![](assets/geo_ellip.png)

L'**altitude** (*H* sur la figure ci-dessus) est la hauteur d'un point sur le relief par rapport au **géoïde**.

Un **GCS**, que nous avons vu précédemment, est basé sur un *ellipsoïde* (traitillé noir) (une ellipse en 3D) et non sur un géoïde. Le but est donc de trouver un *ellipsoïde* ou une *sphère* qui représente au mieux le géoïde pour une surface (sur une échelle globale ou locale) donnée.

## La forme d'un ellipsoïde

La forme d'une ellipse (2D), et donc d'une ellipsoïde (3D), est définie par deux rayons :

1. Le rayon le plus long est appelé **demi-grand axe (semi-major axis)**
2. Le rayon le plus court est appelé **demi-petit axe (semi-minor axis)**

![Demi-grand axe et demi-petit axe](assets/minor.gif)


## Paramètres de l'ellipsoïde de la Terre

Plusieurs paramètres sont à prendre en compte pour l'ellipsoïde :

1. Le diamètre polaire (d'un pôle à un autre) est d'environ **12'714 km**

2. Le diamètre équatorial est d'environ **12'758 km**

3. L'*aplatissement* de l'ellipsoïde est définie comme
        $f = \frac{(a - b)}{a}$

    Avec :
    - $a$, longueur du demi-grand axe
    - $b$</span>, longueur du demi-petit axe

Par exemple, pour le modèle géodésique mondial 1984 (WGS 84), largement utilisé, notamment par les systèmes GPS :

$a$ = 6 378 137 mètres  
$\frac{1}{f}$ = 298.257223563

Plusieurs ellipsoïdes de référence ont été élaborés comme approximation (locale ou globale) du géoïde.

Un ellipsoïde est sélectionné pour s'adapter et représenter au mieux un pays ou une zone spécifique.

<span style="font-size:1em; color:red">ATTENTION :</span> ***le meilleur ellipsoïde pour une région donnée n'est pas le meilleur ellipsoïde global, et vice versa !***

![](assets/illpisode.png)

Voici quelques ellipsoïdes communément utilisés (non exhaustif)

|Ellipsoid Name|EPSG#|Semi Major Axis (a)|Inverse Flattening (f)|
|-------------|-------------|---------------|---------------|
|Airy 1830|7001|6377563.396|299.3249646|
|Airy Modified 1849|7002|6377340.189|299.3249646|
|Australian National Spheroid|7003|6378160|298.25|
|Average Terrestrial System 1977|7041|6378135|298.257|
|Bessel 1841|7004|6377397.155|299.1528128|
|Bessel Modified|7005|6377492.018|299.1528128|
|Bessel Namibia|7006|6377483.865|299.1528128|
|Bessel Namibia (GLM)|7046|6377397.155|299.1528128|
|CGCS2000|1024|6378137|298.257222101|
|Clarke 1858|7007|6378293.64520876|294.260676369261|

