# Tutoriel 8 - Données spatiales (B)

Dans cette section, nous aborderons les points suivants:

- Sélections, requêtes et jointures
- Geopandas

# Sélections
Les sélections interviennent à toutes les étapes d’une chaîne de géotraitement : pour préparer les données en entrée, pour trier des données intermédiaire, pour analyse des données en sortie.
Sélectionner permet de répondre aux questions de type combien d’objets ou quels objets ont telle ou telle caractéristique (spatiale ou attributaire).

Trois types de sélection
- Sélection manuelle
- Requête spatiale (basée sur les opérateurs topologiques)
- Requête attributaire (utilisant le langage SQL pour interroger la table attributaire)

## Sélection manuelle
Permise par le logiciel SIG, mais n’est pas de la géomatique : ne peut pas être intégrée à une chaîne de géotraitements.

# Requête 

## Requête spatiales (par localisation)

Interroger les géodonnées sur la base de leurs relations topologiques (en utilisant les opérateurs topologiques → relationship).
![](assets/)


Par exemple : communes qui se situent dans le canton de Vaud.
*sélectionner le canton de Vaud puis sélectionner les polygones des communes within polygone Vaud précédemment sélectionné*
OUTIL Select layer by location (Data Management Tools)

Utiliser selection type pour combiner des sélections successives.
![](assets/)

## Requêtes attributaires
Interroger les données sur la base de leur table attributaire, sur un champ ou une combinaison de champs, en utilisant des opérateurs logiques et mathématiques.
Outil très puissant, exploitant la structure en base de données des SIG pour répondre rapidement à des questions.
Basé sur le langage SQL.

Voir référence pour ArcGIS :
https://pro.arcgis.com/fr/pro-app/latest/help/mappin g/navigation/sql-reference-for-elements-used-in-q uery-expressions.htm

Une requête SQL de sélection a la syntaxe suivante : SELECT champs FROM couche de données WHERE condition. Dans ArcGIS, on n’écrit que la condition.
![](assets/)

Par exemple : combien y a-t-il de communes de plus de 10’000 habitants ?
*sélectionner les communes répondant à la condition EINWOHNERZAHL>10000 (attribut EINWOHNERZAHL ayant une valeur plus grande que 10000)*

OUTIL Select layer by attribute (Data Management Tools)
![](assets/)

## Imbriquer les requêtes

Imbriquer plusieurs requêtes avec des opérateurs logiques.
![](assets/)
NOT = exclusion (SAUF)
S’écrit aussi AND NOT
Attention au sens : A NOT B ←→ B NOT A

Par exemple :
Sélectionner les communes vaudoises de 5000 à 10’000 habitants.
Parmi celles-ci, quelle(s) commune(s) a une densité de plus de 50 habitants / hectare?
Imbriquer les lusieurs requêtes imbriquées avec opérateurs logiques (AND, OR...):
*EINWOHNERZAHL >= 5000 AND EINWOHNERZAHL <= 10000 AND KANTONSNUMMER = 22 AND EINWOHNERZAHL/GEM_FLAECHE > 50*

# Jointures
Un moyen de lier temporairement (outils Add... Join) ou durablement deux tables.

Comme pour les sélections, il existe des jointures attributaires (Join Field) et spatiales (Spatial Join)

Référence :
https://pro.arcgis.com/fr/p ro-app/latest/tool-referen ce/geoanalytics-desktop/jo in-features.htm
![](assets/)

## JOINTURES ATTRIBUTAIRES
OUTILS Add Join et Join Field

Les deux tables jointes doivent avoir un attribut commun (idéalement, un UID). La table attributaire résultante contient les attributs des 2 tables.
![](assets/)

## Jointure spatiales
OUTILS Spatial Join et Add Spatial Join
Permet de joindre deux tables sur la base de leur relations spatiales (opérateurs topologiques → match option).
Attention au type de jointure : une à une ou une à plusieurs.
![](assets/)




