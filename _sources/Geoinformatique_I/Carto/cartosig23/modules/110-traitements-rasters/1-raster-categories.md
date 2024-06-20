# Raster avec données catégorielles

La première image raster que nous regardons contient des classes (catégories) d'utilisation du sol. Les données proviennent de la [Statistique suisse de la superficie](https://www.bfs.admin.ch/bfs/fr/home/services/geostat/geodonnees-statistique-federale/sol-utilisation-couverture/statistique-suisse-superficie.html) qui sont produites par [l'Office fédéral de la statistique (OFS)](https://www.bfs.admin.ch/bfs/fr/home.html).

Les données peuvent être téléchargées librement depuis le site Web de l'OFS. Une partie déjà prête à être utilisée avec un SIG peut être téléchargée directement ici:

<a href="assets/usol.zip"><i class="far fa-file"></i> Utilisation du sol par la classification de 27 catégories pour la Suisse entière</a>

Ce fichier contient une image raster en format GeoTIFF. Le fichier Excel contient une description des catégories utilisées. Dans l'onglet «Codes AS\_27» vous trouvez les valeurs et une description de la catégorie d'utilisation du sol correspondante.

Nous pouvons ajouter le fichier GeoTIFF dans un nouveau projet SIG. Voici comment la couche raster pourrait se présenter:

![](assets/qgis-usol.png)

Chaque catégorie possède une valeur sous forme d'un nombre entier. Nous avons donc une couche raster de type "Integer". Plus exactement, il s'agit d'un type "unsigned byte" ce qui correspond à des nombres entiers entre 0 et 255.

Pour chaque valeur il y a un ton de gris ou une couleur associé. Ces couleurs sont complètement arbitraires et peuvent être définies par l'utilisateur du SIG. Il n'y a pas de palette de couleur enregistrée dans ce fichier GeoTIFF.

Essayez de trouver les caractéristiques de la couche raster.

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
          "answertext": "3484 x 2207 pixels"
        },
        {
          "correct": true,
          "answertext": "100 mètres"
        },
        {
          "correct": false,
          "answertext": "1"
        },
        {
          "correct": false,
          "answertext": "GeoTIFF"
        }
      ],
      "question": "Quelle est la résolution de cette couche raster?"
    },
    {
      "id": "q02",
      "type": "singlechoice",
      "answers": [
        {
          "correct": false,
          "answertext": "3484"
        },
        {
          "correct": false,
          "answertext": "2207"
        },
        {
          "correct": false,
          "answertext": "10'000"
        },
        {
          "correct": true,
          "answertext": "7'689'188"
        },
        {
          "correct": false,
          "answertext": "2'485'500"
        }
      ]
    },
    {
      "id": "q03",
      "type": "singlechoice",
      "answers": [
        {
          "correct": false,
          "answertext": "Aire d'habitation"
        },
        {
          "correct": false,
          "answertext": "Surface d'infrastructure spéciale"
        },
        {
          "correct": true,
          "answertext": "Aérodrome"
        },
        {
          "correct": false,
          "answertext": "Horticulture"
        },
        {
          "correct": false,
          "answertext": "Lac"
        },
        {
          "correct": false,
          "answertext": "Glacier, névé"
        }
      ],
      "question": "Téléchargez la couche Shape <a href=\"/_assets/sirs/22/raster/sample-point.zip\">sample-point.zip</a> et ajoutez-la à votre projet QGIS. Quelle est la catégorie d'utilisation du sol à l'endroit du seul point du fichier Shape?"
    }
  ]
}
```


- Quelle est la résolution de cette couche raster?

- Combien de pixels il y a dans cette couche?

- Téléchargez la couche Shape [sample-point.zip](assets/sample-point.zip) et ajoutez-la à votre projet QGIS. Quelle est la catégorie d'utilisation du sol à l'endroit du seul point du fichier Shape?

Ensuite, essayez de changer la représentation pour obtenir une représentation en couleurs. Vous pouvez aussi donner pour chaque valeur le nom de la catégorie. Voici comment ça pourrait se présenter:

![](assets/usol-qgis-col.jpg)
