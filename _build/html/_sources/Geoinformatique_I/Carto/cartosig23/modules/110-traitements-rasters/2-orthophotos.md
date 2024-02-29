# Orthophotos (et fusion de couches raster)

Une orthophoto est une image aérienne qui a été géométriquement rectifiée pour pouvoir être utilisée dans un SIG. Le principe de l'orthophoto est montrée dans cette figure:

![](assets/principe-orthophoto.png)

Une photo aérienne est prise par un appareil photo p.ex. depuis un avion. Comme tout appareil photo, la photo prise a naturellement une perspective et représente la vue depuis le point précis où la photo a été prise. Les objets qui ne se trouvent pas directement en dessous de l'appareil photo seront prises légèrement de côté. Ainsi, la façade d'un grand bâtiment pourra suivant comment être vue.

Dans une orthophoto on souhaite avoir une vue du haut pour n'importe quel endroit de la photo. Une orthophoto est donc compatible avec une carte qui représente le territoire également strictement du haut et ceci à n'importe quel endroit. En conséquence, pour transformer une photo aérienne en orthophoto, une correction géométrique est nécessaire. Cette opération est généralement faite à partir d'une série de photos aériennes et à l'aide de logiciels spécialisés. En plus, cette opération sera généralement faite de manière approximative et on pourra toujours voir p.ex. certaines façades de bâtiments.

Maintenant, nous explorons les orthophotos dans un SIG. Pour commencer, téléchargez les orthophotos suivantes qui proviennent de Swisstopo (attention, environ 250 Mo):

<a href="assets/swissimage-greina.zip"><i class="far fa-file"></i> Orthophotos Swisstopo à 10 cm d'une partie de la Greina (Tessin/Grisons)</a>

Ensuite, décompressez l'archive ZIP et ajoutez les couches à un nouveau projet SIG. Inspectez une des couches et regardez notamment les caractéristiques de l'image raster dans les propriétés.

Au total, il y a 6 couches raster avec à chaque fois 10'000 x 10'000 pixels et 3 bandes. Il n'est pas très pratique de devoir cocher et décocher chacune des 6 couches manuellement pour simplement afficher ou cacher les orthophotos. Pour cette raison, nous pouvons grouper les images:

![](assets/group-layers.png)

Ces orthophotos sont des couches raster avec 3 bandes, une par couleur primaire (rouge, vert et bleu). Par contre, on peut modifier l'**affichage** de chaque couche raster séparément dans la symbologie de la couche. Voici comment ça se présente dans QGIS:

![](assets/raster-symbology-qgis.png)

Nous pouvons notamment voir en haut le type d'affichage ("Render type") qui est une représentation multi-bandes en 3 couleurs. L'affichage de la couche raster sera nécessairement en 3 canaux rouge, vert et bleu, puisque ça correspond aux couleurs de l'écran. Nous affectons une bande de la couche raster à chaque canal pour afficher l'orthophoto comme nous en avons l'habitude.

Nous pouvons aussi modifier beaucoup de paramètres que vous connaissez peut-être de Photoshop. Dans l'exemple ci-dessus, notez que le contraste a été changé à une valeur de 50 (la valeur normale est 0).

Explorez les différentes options de symbologie et regardez l'effet sur l'affichage de l'image.

Évidemment, uniquement une des 6 couches raster sera affecté par vos changements. Ce n'est pas très pratique. Il serait plus pratique de disposer d'une seule couche raster pour toute la zone. Un logiciel SIG avancé comme QGIS est capable de fusionner plusieurs couches raster en une seule à condition qu'il y a le même système de coordonnées pour toutes les couches. Cette opération de fusion s'appelle **merge** dans QGIS. Elle est disponible dans les outils "GDAL" de la Processing Toolbox dans QGIS:

![](assets/merge-tool.png)

Procédez à l'opération de fusion des 6 images et enregistrez le résultat dans un nouveau fichier GeoTIFF.


```comment
TODO: make quiz
{
  "intro": "",
  "title": "",
  "questions": [
    {
      "id": "q01",
      "type": "singlechoice",
      "answers": [
        {
          "correct": false,
          "answertext": "20'000 pixels de large et 30'000 pixels de haut"
        },
        {
          "correct": true,
          "answertext": "20'000 pixels de haut et 30'000 pixels de large"
        },
        {
          "correct": false,
          "answertext": "1.68 Go"
        },
        {
          "correct": false,
          "answertext": "1.8 Go"
        }
      ],
      "question": "Quelle est la taille de la couche raster de sortie?"
    },
    {
      "id": "q02",
      "type": "singlechoice",
      "answers": [
        {
          "correct": false,
          "answertext": "10 mètres"
        },
        {
          "correct": true,
          "answertext": "10 cm"
        },
        {
          "correct": false,
          "answertext": "25 mètres"
        },
        {
          "correct": false,
          "answertext": "25 cm"
        }
      ],
      "question": "Quelle est la résolution?"
    }
  ]
}
```


- Quelle est la taille de la couche raster de sortie?

- Quelle est la résolution?
