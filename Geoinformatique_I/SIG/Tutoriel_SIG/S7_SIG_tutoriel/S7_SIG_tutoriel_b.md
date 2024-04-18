# Tutoriel 7 - Introduction SIG & Projection (B)

Dans cette section, nous aborderons les points suivants:

- Modéisation Numérique de terrain (MNT)
- Opérateur topologique

# Modéisation Numérique de terrain (MNT)
## Représenter la 3ème dimension
- Les modèles numériques de terrain (MNT)
- Les modèles numériques de surface (MNS)
![](assets/)


Visualiser le relief à partir d’un MNT : appliquer un traitement Ombrage / Hillshade sur le modèle de terrain. Attention : les pixels n’ont plus de valeur d’altitude, mais d’ombrage.
![](assets/)

Chez Swisstopo :

MNT = SwissALTI3D 
![](assets/)

MNS = SwissSURFACE3D
![](assets/)

Modèle 3D d’objets = SwissBUILDINGS3D
![](assets/)

# Opérateur topologique
## Relation 
Les objets géographiques peuvent être en relation topologique : inclusion, adjacence (segment en commun), intersection (point en commun). Dans un réseau, on considère également la connectivité.

Exemples :
![](assets/)

## Opérateurs
Les opérateurs topologiques permettent de traiter les géodonnées en tenant compte de leurs relations pour vérifier leur qualité, sélectionner et/ou joindre des entités, analyser les répartitions spatiales.
- Pour l’inclusion : est égal, se trouve dans, contient 
- Pour l’adjacence : touche
- Pour l’intersection : croise (géométries différentes), chevauche (mêmes géométries), intersecte, est disjoint (aucune relation)

## Calcul de distances
Deux types de distances à distinguer :

- ligne droite sur la carte projetée : distance loxodromique (Mercator : le navire suit un cap constant)
- ligne droite sur le globe terrestre : distance orthodromique (chemin réellement le plus court, en arc de cercle ; nécessite de continuellement changer de cap)

Dans un petit espace géographique (ex : la Suisse), la différence est minime.
https://www.edumedia-sciences.com/fr/media/924-orthodromie-et-loxodromie

![](assets/)

Les distances peuvent être calculées à partir de données vectorielles ou de données raster.
Il existe plusieurs manière de calculer une distance. Par exemple :
- Distance euclidienne (à vol d’oiseau)
- Distance rectilinéaire ou «de Manhattan», «City block» ou «de Gower».
![](assets/)

