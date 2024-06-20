# Tutoriel 11 - Analyse spatiale I (A)

Dans cette section, nous aborderons les points suivants:

- Analyse de terrain/surface - sur base de MNT
- Interpolation spatiale

# Analyse Spatiale 
L’analyse spatiale sert à faire apparaître la structure spatiale d’un phénomène et à observer/quantifier les relations entre objets géographiques.

Une analyse spatiale consiste en une chaîne de géotraitements, transformant par calcul, modélisation ou combinaison des géodonnées sources en nouvelles informations géographiques et statistiques.

![](assets/)
Source : ESRI

On peut regrouper les processus d’analyse spatiale en fonction du type d’opérations et/ou sur le type de données en entrée.

# Analyse de surface

## Que peut-on faire avec un MNT ?

Récupérer la valeur d’altitude d’un objet (ponctuelle ou moyenne)
- Ponctuelle : OUTIL Extraire des valeurs vers points
- Moyenne : OUTIL Statistiques de zones

Identifier des tranches des d’altitude (ex : zone montagne > 800m)
- OUTIL Reclassifier ou Calculatrice Raster

Le transformer en:
- Couche d'ombrage (raster) : OUTIL Ombrage
- Couche de courbes de niveau : OUTIL 

Isoligne (! pas que pour les altitudes!)
![](assets/)

Calculer en chaque pixel, en fonction de ceux qui l’entourent :
- La pente : OUTIL Pente et, pour l’hydro, OUTIL Direction de flux
- L’orientation : OUTIL Exposition
![](assets/)
![](assets/)
![](assets/)

Calculer en chaque pixel, en fonction de ceux qui l’entourent :
- La rugosité du terrain : OUTIL (Paramètres de) Courbure
- La visibilité d'un ou plusieurs objets : OUTIL Champ de vision
![](assets/)
![](assets/)

L’utiliser comme couche de surface d’élévation prédéfinie «ground» d’une scène 3D (modifie la position Z des autres couches)
![](assets/)
![](assets/)

# Interpolation Spatiale
L’interpolation permet de prédire la valeurs de chaque pixel d’un raster (continu) sur la base de points d’échantillonage (discrets).
Il existe deux grandes familles de méthodes d’interpolation, selon qu’elles sont basées sur une fonction mathématique ou un modèle (géo)statistique.
Méthodes mathématiques (déterministes) : Spline, Tendance et...
- Voisins naturels (pondération selon la surface)
![](assets/)
- IDW
(pondération selon la distance)

Méthodes statistiques (probabilistes) :
- Kriegeage
![](assets/)
Etape 1 : l’outil analyse l’autocorrélation spatiale pour chaque paire d’emplacements et ajuste ainsi un modèle statistique empirique de base où la variance augmente simplement avec la distance.
Etape 2 : grâce à ce modèle ajusté, l’outil peut ensuite calculer les valeurs manquantes probables.