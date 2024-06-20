# Tutoriel 9 - Géotraitement (A)

Dans cette section, nous aborderons les points suivants:

- Chaîne de traitements
- Agréger et délimiter des zones

# Chaîne de traitements
La chaîne de (géo)traitements ou workflow est l’ensemble des opérations de géotraitement successives qui mènent à la résolution d’un problème spatial.
On peut distinguer

- les géotraitements (ou traitements spatiaux) : méthode intégrées aux logiciels SIG pour agréger, extraire, combiner et transformer les géodonnées (basés sur la localisation et la géométrie des entités)
- Les méthodes d’analyse spatiale : méthodes qu’on retrouve aussi en dehors des SIG pour comprendre les règles d’organisation de l’espace (analyse de réseau, densité, autocorrélation spatiale, concentration, interpolation, analyses de surface (pente, exposition, etc.), analyse de visibilité, outils
![](assets/)

## Géotraitements
*Définition*
Opérations réalisées sur un jeu de données spatiales afin de créer de nouvelles géodonnées.

Exemples:
![](assets/)

## Agréger et délimiter des zones

## Agréger des entités
Les opérations d’agrégation regroupent des entités géographiques à une résolution plus faible → perte d’information.
On peut agréger des entités sur la base de leurs attributs (ex : toutes les parcelles de type « forêt ») ou de leur localisation (ex : toutes les communes à l’intérieur du PNR Gruyère – Pays d’Enhaut).
![](assets/)

## Agréger les couches
![](assets/)

## Délimiter des zones
Les opérations de délimitation sont essentielles pour créer des zones d’étude pertinentes et limiter l’information à traiter.
![](assets/)

donnée. Il est possible de les imbriquer (ex : impact fort → 25m et moyen → 50m)
![](assets/)

## Combiner des géométries

Les opérations de combinaison (superposition) sont en quelque sorte la transposition géométrique des opérateurs logiques : OR, AND, NOT
![](assets/)

![](assets/)

## Equivalents raster
![](assets/)

![](assets/)

## Récupérer des données raster
Il est parfois très pratique de travailler avec des rasters puis de revenir au vecteur pour la cartographie ou pour des calculs de champs.

**OUTIL Extraire de valeurs vers des points**
Permet de récupérer dans la table attributaire d’une couche de points (vos objets d’étude ou le centroïde de ceux-ci) la valeur de la cellule raster à la même position. Une simple **Jointure spatiale** permet ensuite de reprendre la valeur du point dans la table de la couche polygones.
*Couche polygones → Centroïdes → Extraire du raster vers points → Jointure spatiale entre points et polygones → Couche polygones avec nouvelles valeurs.*

**OUTIL Statistiques zonales**
Permet de calculer des statistiques descriptives (moyenne, somme, maximum, etc.) sur des groupes de cellules raster, donc des zones. Ces zones sont définies soit par un autre raster (de type Entier, où chaque zone possède son code 0, 1, 2 etc.), soit par une couche de polygones (l’outil va automatiquement rasteriser la couche pour réaliser l’opération ; il faut un attribut pour identifier les différentes zones).

![](assets/)