# Opérateurs sur les géométries

Dans les SIG on trouve un nombre relativement important d'opérateurs qui s'appliquent sur les géométries d'une couche vectorielle. Nous regardons ici les opérateurs les plus importants.


## La zone tampon

Un opérateur très connu est la *zone tampon*, ou *buffer*. Cette opérateur ajoute (ou enlève) une certaine distance aux géométries d'une couche. Ainsi, on peut par exemple trouver tous les endroits qui se trouvent à moins de 10 mètres d'une route. Comme résultat, on obtient une nouvelle couche que l'on pourra utiliser pour d'autres opérations, ou encore pour des sélection.

Dans la vidéo ci-dessous le principe de la zone tampon est illustré et la manipulation est montrée à l'aide d'un exemple où on souhaite sélectionner tous les bâtiments qui se trouvent à moins de 10 mètres d'une route. Évidemment, on pourrait d'abord faire une sélection d'une partie des routes pour ainsi trouver p.ex. tous les bâtiments qui sont à moins de 100 mètres d'une autoroute.

```content
type: video
id: buffer
src: assets/buffer.m4v
```

### Exercice: zone tampon

Téléchargez ci-dessous le jeu de données d'exemple de swissTLM3D (le jeu de données complet peut être obtenu sur le site Web de Swisstopo).

Chargez la couche des bâtiments (`swissTLM3D_TLM_GEBAEUDE_FOOTPRINT`) ainsi que les cours d'eau (`swissTLM3D_TLM_FLIESSGEWAESSER`). Calculez une zone tampon de 100 mètres autour des cours d'eau et sélectionnez tous les bâtiments qui se trouvent au moins en partie à moins de 100 mètres d'un cours d'eau.

Ouvrez la table d'attribut de la couche des bâtiments et regardez combien de bâtiments sont sélectionnés. Le nombre est marqué dans le titre de la fenêtre:

![](assets/feature-count-qgis.png)

---

<a href="assets/swissTLM3D_1.9_shp_LV95.zip"><i class="far fa-file-pdf"></i> Échantillon du jeu de données swissTLM3D</a>

---

**Question:** Dans le jeu de données fourni ci-dessus, combien de bâtiments se trouvent au moins en partie à moins de 100 mètres d'une rivière?

```comment
[quiz]
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
          "answertext": "11682"
        },
        {
          "correct": true,
          "answertext": "3407"
        },
        {
          "correct": false,
          "answertext": "3704"
        },
        {
          "correct": false,
          "answertext": "0"
        },
        {
          "correct": false,
          "answertext": "6112"
        }
      ],
      "question": "Dans le jeu de données fourni ci-dessus, combien de bâtiments se trouvent au moins en partie à moins de 100 mètres d'une rivière?"
    }
  ]
}
```


## Opérateurs de l'analyse combinatoire

Un SIG est en mesure de faire des analyses sur la base de 2 couches vectorielles et de créer une nouvelle couche en sortie en fonction des relations géométriques entre les entités des 2 couches d'entrée.

Pour illustrer ce principe, prenons l'exemple de l'opérateur ***intersection*** qui est un de ces opérateurs. Nous avons p.ex. deux couches de polygones en entrée, et l'opérateur de l'intersection permet de garder uniquement les parties des polygones qui se trouvent dans les deux couches. Les géométries sont coupées si nécessaires. Voici une illustration de ce principe:

![](assets/intersect.png)

Donc si on voudrait par exemple non pas seulement savoir quels bâtiments se trouvent à une distance donnée d'une route, mais quelle partie du bâtiment, on pourrait combiner une zone tampon avec une intersection. Voici une vidéo qui illustre cette opération:

```content
type: video
id: intersect
src: assets/intersect.m4v
```

Voici les opérateurs d'analyse combinatoire disponibles dans QGIS:

![](assets/overlay-operations.png)


## Clip

Un autre opérateur utile est le **«clip»** ou «découpage» en français (ou simplement «couper»). Au niveau des géométries, cet opérateur est identique à l'opérateur d'intersection. Par contre, l'opérateur de découpage ne reprend pas les attributs de la couche de recouvrement.

Une autre variante de l'opérateur «clip» est le «clip by extent» (découpage par étendue) où l'on doit spécifier une région rectangulaire qui sera utilisée pour découper les géométries de la couche d'entrée.


## Dissolve

Une opération de nature un peu différente est le *dissolve*. Cette opération travaille sur les géométries d'une seule couche. Elle regroupe ensemble dans une seule géométrie (qui peut être complexe et/ou multiple) toutes les géométries qui partagent les mêmes valeurs pour un ou plusieurs attributs. Ainsi, si nous avons par exemple une couche vectorielles avec toutes les communes de Suisse, et qu'un attribut contient l'information sur l'appartenance de la commune à un canton, nous pouvons obtenir une couche des limites cantonales à partir de la couche des communes:

```content
type: video
id: dissolve
src: assets/dissolve.m4v
```

### Exercice: l'opérateur Dissolve

Téléchargez le jeu de données swissBOUNDARIES3D, chargez la couche `swissBOUNDARIES3D_1_3_TLM_HOHEITSGEBIET` (c'est la couche des communes suisses), et appliquez un «dissolve» sur l'attribut `BEZIRKSNUM`.

---

<a href="assets/swissBOUNDARIES3D_shp_LV95.zip"><i class="far fa-file-pdf"></i> swissBOUNDARIES3D_shp_LV95.zip</a>

---

**Question:** Combien d'entités obtenez-vous après l'opération dissolve dans la couche de sortie ?


```comment
[quiz]
{
  "intro": "",
  "title": "",
  "questions": [
    {
      "id": "q02",
      "type": "singlechoice",
      "answers": [
        {
          "correct": false,
          "answertext": "1"
        },
        {
          "correct": true,
          "answertext": "135"
        },
        {
          "correct": false,
          "answertext": "153"
        },
        {
          "correct": false,
          "answertext": "158"
        },
        {
          "correct": false,
          "answertext": "2289"
        }
      ],
      "question": "Combien d'entités obtenez-vous après l'opération dissolve dans la couche de sortie ?"
    }
  ]
}
```