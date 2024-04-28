# Statistiques zonales

Sur la base d’une couche polygones et d’une couche raster, il est possible de faire des statistiques par polygone. Pour chaque polygone, les pixels d’une couche raster dont le centre se trouve à l'intérieur sont considérées et ensuite des statistiques calculées sur les valeurs des pixels concernés. Ce principe est illustré dans la figure suivante :

![](assets/zonal-stats.png)

Ainsi, les pixels avec centre rouge sont associés au polygone rouge, et la même chose pour les pixels de couleur bleue ou verte.

Évidemment, plusieurs calculs sont possibles à partir des valeurs des pixels par polygones, dont typiquement le calcul de la moyenne, du minimum, maximum, etc.

Pour illustrer les possibilités, nous allons faire deux exemples. Nous allons utiliser les données suivantes:

<ul>
  <li><a href="assets/mnt25_ch.zip"><i class="far fa-file"></i> MNT25 - Modèle numérique de terrain de Swisstopo avec une résolution de 25 mètres (probablement vous l'avez déjà téléchargé dans un exercice précédent)</a></li>

  <li><a href="assets/swissBoundaries3D-202107.zip"><i class="far fa-file"></i> swissBoundaries3D (limites de communes de Swisstopo)</a></li>

  <li><a href="assets/utilisation-du-sol-8classes.zip"><i class="far fa-file"></i> Utilisation du sol en 8 classes pour le Tessin</a></li>
</ul>

## Exemple 1 : l’altitude par commune

À partir de la couche vectorielle des communes suisses et du modèle numérique d’altitude, nous pouvons déterminer l’altitude moyenne, minimum et maximum.

Nous pouvons aussi déterminer la commune qui a la différence d’altitude la plus grande de Suisse.

Utilisez la couche raster du MNT et des communes suisses. Le MNT n'a pas de système de coordonnées, il s'agit du système CH1903/LV03 (EPSG: 21781). Il faut projeter la couche dans le même système de coordonnées que celui des communes (CH1903/LV95).

Attention : il peut y avoir des problèmes de projection du MNT de CH1903/LV03. Dans ce cas, projetez la couche d’abord de CH1903/LV03 vers WGS84 (EPSG : 4326), et dans un deuxième temps de WGS84 vers CH1903/LV95.

Pour le calcul des statistiques zonales, il faut utiliser l'outil «Zonal statistics». Voici le dialogue dans QGIS :

![](assets/zonal-stats-dialog.png)

```comment
TODO: make quiz
{
  "intro": "",
  "title": "",
  "questions": [
    {
      "id": "q1",
      "type": "singlechoice",
      "answers": [
        {
          "correct": false,
          "answertext": "Zermatt"
        },
        {
          "correct": true,
          "answertext": "Anniviers"
        },
        {
          "correct": false,
          "answertext": "Val de Bagnes"
        },
        {
          "correct": false,
          "answertext": "Lauterbrunnen"
        },
        {
          "correct": false,
          "answertext": "Saint-Barthélemy (VD)"
        }
      ],
      "question": "Quelle est la commune suisse avec la plus grande différence d'altitude ?"
    },
    {
      "id": "q2",
      "type": "singlechoice",
      "answers": [
        {
          "correct": false,
          "answertext": "Zermatt"
        },
        {
          "correct": false,
          "answertext": "Fieschertal"
        },
        {
          "correct": false,
          "answertext": "Bâle"
        },
        {
          "correct": false,
          "answertext": "Locarno"
        },
        {
          "correct": true,
          "answertext": "Brissago"
        }
      ],
      "question": "Quelle est la commune suisse avec la plus faible altitude moyenne ?"
    }
  ]
}
```

Essayez de répondre aux questions suivantes:

- Quelle est la commune suisse avec la plus grande différence d'altitude ?

- Quelle est la commune suisse avec la plus faible altitude moyenne ?


## Exemple 2 : classes d’utilisation du sol

Déterminez pour une commune tessinoise de votre choix la classe d’utilisation du sol la plus répandue. Utilisez pour ça la couche raster de l’utilisation du sol pour le Tessin.

La valeur statistique à calculer est dans ce cas la «majority», donc la valeur la plus fréquente.
