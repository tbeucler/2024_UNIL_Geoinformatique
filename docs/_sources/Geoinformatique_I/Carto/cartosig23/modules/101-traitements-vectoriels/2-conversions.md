# Conversions entre types de géométries

Les SIG proposent plusieurs façon de passer d'un type de géométrie à un autre type. Quelques exemples:

- composer une couche de polygones à partir d'une couche de lignes
- extraire une couche de points à partir de polygones, p.ex. pour placer des symboles dans les polygones
- extraire une couche de points à partir de lignes (p.ex. tous les points de la ligne, ou un point par ligne)
- composer une ligne à partir d'une série de points
- créer une couche de polygones à partir d'une série de points de sorte à ce que chaque polygone contient exactement un point

Un autre problème fréquent est aussi de convertir un fichier CSV (ou similaire) qui contient des coordonnées en couche points. Ou de convertir un fichier d'adresses en coordonnées géographiques.

La plupart de ces fonctions peuvent simplement être accédées dans la boîte à outils («Processing Toolbox» dans QGIS, ArcToolbox dans ArcGIS).

Nous regardons ici par la suite quelques cas qui méritent une attention particulière au niveau théorique.


## Extraire un point par polygone

Il y a en gros 3 algorithmes à disposition:

1. calcul des centroïdes
2. «point on surface»
3. «pôle d’inaccessibilité»

Les différences sont expliquées ici:

```content
type: folder_presentation
id: poly2pt
directory: assets/poly2pt
```

<a href="assets/poly2pt.pdf"><i class="far fa-file-pdf"></i> poly2pt.pdf</a>

Avec QGIS ces différents algorithmes sont accessibles directement dans la Processing Toolbox sous la rubrique «Vector geometry». Il suffit de chercher un des termes «centroids», «point on surface» ou «pole of inaccessibility».

```comment
[FIXME: Problem with several folder presentations on the same page]
## Généralisation

Un autre problème fréquent est la généralisation des géométries.

La présentation ci-dessous montre ce qu'il faut faire et pas faire:

!!!
type: folder_presentation
id: generalisation
directory: assets/generalisation
!!!

<a href="assets/generalisation.pdf"><i class="far fa-file-pdf"></i> generalisation.pdf</a>
```
