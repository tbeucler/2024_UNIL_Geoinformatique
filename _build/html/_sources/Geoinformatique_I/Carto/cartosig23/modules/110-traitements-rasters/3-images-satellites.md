# Image satellite multi-bandes

Les images satellites sont similaires aux orthophotos issues des photos aériennes étant donné que les deux sont des images de la surface terrestre. Par contre, au niveau de l’acquisition, il y a des différences importantes. Les photos aériennes sont typiquement prises par avion avec une caméra numérique de bonne qualité, à une altitude de quelques centaines de mètres. Les images satellites quant à eux sont prises à une distance de plusieurs centaines de kilomètres, et le mode d’acquisition est différent. Les senseurs d’un satellite d’observation terrestre sont sensibles à une seule longueur d’onde du spectre électromagnétique. Les ondes électromagnétiques comprennent, avec une longueur d’onde croissante, les rayons gamma, rayons X, les ultra-violets, la lumière visible, l’infrarouge et les ondes radio :

![](assets/domaines_spectre_electromagnetique.png)

<div style="text-align: right; font-style: italic; font-size: 12px; margin-top: 10px; color: #666;">Source de l'illustration: Benjamin ABEL, CC BY-SA 3.0, <a href="https://commons.wikimedia.org/w/index.php?curid=22016632">Lien</a></div>

Ainsi, un satellite peut avoir p.ex. 3 senseurs dans le spectre lumineux correspondant en gros au rouge, vert et bleu, et plusieurs senseurs dans le spectre infrarouge. Chaque senseur balaye la surface terrestre au fur et à mesure que le satellite progresse.

Pour prendre un exemple concret, nous considérons ici une image du satellite américain Landsat. Téléchargez l'image suivante:

<a href="assets/Landsat4_1990.zip"><i class="far fa-file"></i> Image Landsat 4 de 1990 du Tessin</a> [archive ZIP, 175 Mo]

En réalité, Landsat n'est pas un satellite, mais une série de satellites en plusieurs générations. La première mission Landsat a prise les premières images en 1972. Actuellement, Landsat 9 est en opération, en parallèle à Landsat 8. Les images Landsat peuvent être obtenues gratuitement depuis [l’EarthExplorer](https://earthexplorer.usgs.gov/). Les images Landsat ont une résolution de 30 mètres pour la plupart des bandes (certaines bandes sont à 15 respectivement 60 mètres). Une image Landsat 4 ou 5 possède 7 bandes, une image Landsat 7 a 8 bandes, et Landsat 8 même 11 bandes. Trois bandes sont dans le spectre visible, et il y a toujours une ou plusieurs bandes dans le spectre infrarouge.

Décompressez l'archive ZIP avec l'image Landsat 4 que vous avez téléchargé. Vous y trouvez notamment 7 couches raster en format GeoTIFF. Chaque couche correspond à une bande du satellite. Nous pouvons afficher chaque couche séparément, mais ce sera nécessairement toujours en tons de gris. Nous devons associer une bande du satellite à une couleur d'affichage. Pour pouvoir faire cela, nous devons combiner les 7 bandes en une seule couche raster. Une possibilité est d’utiliser ce qu’on appelle un «virtual raster», donc une couche raster virtuelle. C’est le fichier `.vrt` qui se trouve également dans l’archive ZIP. Il ne contient aucune donnée d’image, mais uniquement des liens vers les 7 fichiers TIFF. Si vous chargez le fichier `.vrt` avec le SIG, vous aurez automatiquement une couche raster avec toutes les 7 bandes.

Ensuite, vous pouvez varier l'attribution des 7 bandes aux couleurs d'affichages, p.ex. en mettant la bande 6 dans le canal du rouge, la bande 5 dans le canal du vert, et la bande 3 dans le canal du bleu:

![](assets/qgis-landsat-653.png)

Pour augmenter la luminosité et le contraste, il est souvent nécessaire d'ajuster les valeurs minimales et maximales des bandes et d'activer la fonction d'amélioration du contraste dans le menu déroulant correspondant.

L'image résultante ressemble à quelque chose comme ça:

![](assets/landsat-653.png)

On parle ici d'une **image satellite fausses couleurs** étant donné que les vraies couleurs du territoire ne sont pas respectés. En l'occurence, on parle d'une image *&laquo;6-5-3&raquo;* car il s'agit d'une combinaison de ces trois bandes Landsat. Cette combinaison particulière fait très bien ressortir la neige et la glace (à gauche dans l'image on voit le glacier d'Aletsch en bleu foncé).

Il y a aussi d'autres combinaisons qui chacune fait ressortir des éléments différents. Essayez notamment les combinaisons suivantes:

- *4-3-2*
- *7-6-4*
- *3-2-1*

