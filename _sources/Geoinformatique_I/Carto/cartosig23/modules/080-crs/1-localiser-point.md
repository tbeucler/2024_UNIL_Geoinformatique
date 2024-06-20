# Localiser un point sur la Terre

La Terre est ronde. Elle a approximativement une forme d'un ellipsoïde. Approximativement, c'est important. Si on exagère un peu les déviations par rapport à la forme idéalisée d'un ellipsoïde, on obtient une forme (exagérée) qui ressemble plutôt à ça:

![Forme exagérée du Géoïde](assets/geoide_transp.png)

La forme de la Terre est donc plutôt une sorte de *pataoïde*. Cette forme est logiquement appelée **«géoïde»**.

Le problème de la localisation d'un point sur la Terre peut donc être formulée de manière suivante:

<div style="border: 1px solid #ddd; padding: 1rem; margin-top: .25rem; background-color: #f0f0f0;">Comment localiser un point de manière précise sur une patate qui est en rotation autour d'un axe (en faisant un tour par jour) et qui en plus vole avec une vitesse de 110'000 km/h autour d'une étoile ?</div>

De manière pratique, ce que nous faisons est:

1. Nous définissons un **ellipsoïde** qui ressemble le plus possible au géoïde. Cet ellipsoïde est presque une sphère, sauf qu'il est aplati aux extrémités de l'axe de rotation (les pôles).

2. Nous définissons une surface plane qui est perpendiculaire à l'axe de rotation, à mi-distance entre les deux pôles. Ceci définit notamment le cercle de l'équateur.

3. Ainsi, nous avons défini le centre de l'ellipsoïde (qui n'est pas nécessairement identique au «centre» du géoïde!). Ceci nous permet de définir une droite entre le centre et le point à localiser. Ensuite, nous pouvons mesurer l'angle entre le surface plane de l'équateur et cette ligne (on appelle cet angle **«latitude»**).

4. Nous définissons un cercle (ou plus formellement une ellipse) qui passe par les deux pôles, de manière totalement arbitraire. On appellera ce cercle «grand cercle» et nous choisissons le grand cercle qui passe par l'observatoire de Greenwich à Londres. Nous pouvons maintenant mesurer l'angle entre ce grand cercle et la droite entre le centre et le point à localiser. Cet angle s'appelle **«longitude»**.

Ainsi, nous avons défini un système de coordonnées qui permet de localiser un point sur la **surface** de la Terre. Nous appelons ce genre de système de coordonnées **«système de coordonnées géographique»** (SCG, ou en anglais Geographic Coordinate System GCS).

Cependant, un tel système de coordonnées géographique n'est pas très pratique, car il nous permet pas une représentation en 2 dimensions sur un support papier ou un écran. Le calcul des distances est aussi assez compliqué (quelle est la distance entre le point à 47°N / 6.9°E et le point à 46.6°N / 10.2°E ?). En plus, la définition de l'ellipsoïde n'est pas forcément la même (il y a en effet des dizaines voire centaines d'ellipsoïdes), et ces ellipsoïdes ne sont pas tout à fait positionnés au même endroit par rapport au géoïde (on appellera ça le *«datum»*).

Il faut donc procéder à une **projection** qui permet de passer du système de coordonnées géographique (qui est en fait en 3D vu que c'est sur un ellipsoïde) à des coordonnées planes en 2D. On pourra ainsi faire une carte en 2 dimensions et mesurer si possible les distances en kilomètres et plus sur des lignes 3D en courbe.
