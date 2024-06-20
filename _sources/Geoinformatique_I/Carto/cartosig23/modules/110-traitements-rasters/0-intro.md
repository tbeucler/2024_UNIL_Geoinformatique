# Introduction

Nous avons vu tout au début du cours les deux principaux modèles du territoire utilisés dans les SIG: le modèle vectoriel et le modèle raster. Le **modèle raster** (ou modèle image / matriciel) que nous traitons ici couvre l'espace géographique par une grille régulière de cellules (pixels) ordonnées pour former une matrice.

Les cellules sont de taille régulière et correspondent aux unités d'observation régulière.

![](assets/grille.png)

Chaque «image raster» peut être caractérisée en fonction de plusieurs informations:

- **l'étendue spatiale** de l'image qui définit la localisation géographique (la *géoréférence*)

- la **largeur** et **hauteur** de l'image en pixels (p.ex. 600 pixels de large (Est-Ouest) et 400 pixels de haut (Nord-Sud)

- un **type de données**. Chaque pixel contient une seule valeur numérique. Cette valeur peut être un nombre entier ou un nombre à décimales. En cas de nombres entiers, on parle de type «Integer», et sinon «Float». Le nombre d'octets réservé pour chaque valeur définit les valeurs possibles. Ainsi, si on a une image de type «integer» avec 1 octet (= 8 bits) par pixel, nous pouvons représenter uniquement des nombres entiers entre -128 et +127. Le type de données de l'image raster est donc définit à la fois par le type de nombre («integer» ou «float») ainsi que le nombre d'octets (ou bits) utilisé par pixel. Parfois, on utilise le terme «double» pour un nombre décimal («float») avec une longueur de 8 octets (64 bits).

- la **résolution** de l'image raster correspond à la taille d'un pixel sur le territoire. Ainsi. une image où un pixel couvre une distance de 30 mètres sur le territoire aura une *«résolution de 30 mètres»*. Le terme de résolution avec une image raster est donc un peu différent de celui qu'on a l'habitude p.ex. avec les appareils photos ou les écrans.

- le **nombre de bandes**. Une image raster peut contenir plusieurs grilles superposées. Ces grilles sont identiques au niveau de la largeur, hauteur, type de données et la résolution. Une grille est dans ce cas appelée **«bande»**. Par exemple, une photo prise avec un appareil photo normal contient pour chaque pixel une valeur numérique pour la couleur rouge, bleu et verte (les 3 couleurs primaires); une telle photo aurait donc 3 bandes.

Voici une capture d'écran des informations d'une couche raster dans QGIS (disponibles dans les propriétés de la couche). Toutes les caractéristiques de l'image raster mentionnées ci-dessus peuvent être trouvées:

![](assets/raster-properties-annot.png)

Par la suite, nous explorons différents types d'images raster ainsi que des manipulations que nous pouvons effectuer sur ces images.
