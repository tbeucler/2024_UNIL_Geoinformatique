# Étapes de travail

Vous trouvez ci-dessous l'ensemble des étapes de travail du TP2. Ces différentes étapes seront expliquées de manière plus ou moins détaillée dans les différents modules du cours. Certaines instructions seront données de manière générale et devront être appliquées au TP, d'autres seront assez précises. 


## 1. Familarisez-vous avez les données

La première chose à faire est d'inspecter toutes les données, étudier les méta-données (la description des données), et de charger les fichiers essentiels dans le logiciel correspondant (QGIS ou LibreOffice Calc / Excel).


## 2. Sélectionner les régions MS de votre région

Votre région d'étude est définie en termes de régions MS. Ouvrez la couche des régions MS dans QGIS et regardez où se trouve votre région. Faites une sélection de toutes vos régions MS et exportez-les vers une nouvelle couche.

Ensuite, ouvrez la couche des communes et quartiers (prenez la version la plus récente). Pour la trouver, il faudra inspecter la documentation des géométries de base ThemaKart. Sélectionnez les unités spatiales qui font partie de votre région d'étude et exportez-les dans une nouvelle couche vectorielles.

Même si vous allez avoir des géométries qui dépassent votre région d'étude, vous allez avoir besoin de ces couches découpées pour la représentation de votre thématique.


## 3. Jointure des données

Les données statistiques se trouvent dans un fichier LibreOffice Calc, tandis que les géométries des communes et quartiers se trouvent dans une couche vectorielle (p.ex. un fichier Shape ou un fichier GeoPackage). Il faut faire une jointure de ces deux informations dans QGIS afin d'obtenir une nouvelle couche vectorielles qui contient tous les attributs nécessaires.

Le fait que vous avez délimiter les communes et quartiers de votre région d'étude fera que vous importez uniquement les attributs de votre région lors de la jointure.


## 4. Calcul de l'indicateur

Une fois que vous avez une couche vectorielles avec les géométries nécessaires et les attributs qui permettent de calculer l'indicateur, procédez au calcul. Le calcul se fera avec la calculatrice des champs dans QGIS.


## 5. Cartographie de l'indicateur

Vous pouvez ensuite procéder à la cartographie de l'indicateur. Le cas échéant, choisissez une méthode de mise en classe appropriée et faites la mise en classe. Sélectionnez une palette de couleur adaptée.


## 6. Calcul de la zone bâtie

Vous pouvez maintenant procéder au calcul de la zone bâtie sur la base de la couche des bâtiments. La zone bâtie est définie avec la zone tampon de 200 mètres autour des bâtiments. Assurez-vous que les zones tampons qui se superposent sont fusionnées, sans pour autant fusionner l'ensemble des zones tampons.

Ensuite, calculez la superficie de chaque zone tampon à l'aide de la calculatrice des champs. Sélectionnez ensuite la zone tampon la plus grande de votre région d'étude. Cette zone bâtie devra être rajoutée à la carte thématique.


## 7. Calcul du nombre et de la proportion d'habitants, ménages ou emplois dans la zone bâtie

Calculez le nombre d'habitants (indicateurs P1, P2 et P3), ménages (indicateur M1) et emplois équivalent temps plein (indicateurs E1 et E2) qui se trouvent à l'intérieur de votre région d'étude.

Faites de même pour le même nombre, mais uniquement ceux qui sont à l'intérieur de la zone bâtie la plus grande et votre région d'étude.

Calculez la proportion de ce nombre qui se trouve à l'intérieur de la zone bâtie.

Cette information devra être rajoutée sur la carte sous forme textuelle. Il faut qu'il est clair ce que cette information signifie.


## 8. Finalisation de la carte

Assurez-vous qu'on voit sur votre carte les limites communales (surtout celles des villes), les régions MS de votre région d'étude ainsi que les limites cantonales et le cas échéant nationales.

Exportez la carte en format PDF et importez-la dans Adobe Illustrator. Faites attention à la taille et au format de la carte.

Finalement, faites la mise en page entière en ajoutant la titraille, légende et tous les autres éléments de votre carte. La carte devra avoir un format A4 en paysage ou portrait (ce qui est plus approprié pour votre région).
