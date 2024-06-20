# Tutoriel 7 - Introduction SIG & Projection (A)

Dans cette section, nous aborderons les points suivants:

- Introduction SIG
- Modèle vecteur vs modèle raster
- Système géodésique (datum)
- Principe de projection

# Introduction SIG
## Petite définition 

Géomatique = Géographie + informatique
- «La géomatique regroupe l'ensemble des outils et méthodes permettant
d'acquérir, de représenter, d'analyser et d'intégrer des données
géographiques. La géomatique consiste donc en au moins trois activités
distinctes : collecte, traitement et diffusion des données géographiques». 

- «L'information géographique est la représentation d'un objet ou d'un
phénomène réel ou imaginaire, présent, passé ou futur, localisé dans l'espace
à un moment donné et quelles qu'en soient la dimension et l'échelle de
représentation.»                
(Wikipedia: /Géomatique, /Information_géographique)

## Système d'information géographique

Un SIG est composé de :
• Matériel (ordinateur...)
• Logiciel de traitement (ArcGIS, QGIS, FME, R, suite Autodesk…)
• Données géographiques (géométries à référence spatiale)
• Données descriptives / attributaires (table, base de données)
• Fonctions
• … et vous ! (utilisateurs, administrations, clients)

## Logiciel à l'UNIL: ARCGIS ou QGIS

![](assets/Arcgis_logo.png)

- Depuis 1999
- Propriétaire (ESRI) > $$$
- Windows + Linux
- Très bien documenté
- Ecosystème produits ESRI
- Largement utilisé entreprises/admin
https://www.arcgis.com

![](assets/QGIS_logo.png)

- Depuis 2002
- Libre
- Multi-plateforme
- Grande communauté d’utilisateurs
- ++ dans administration,associations, formation...
https://qgis.org

## Système d'information géographique : fonctions

Un (logiciel) SIG est conçu pour réaliser les fonctions :
- d’enregistrement : acquisition et saisie
- de gestion des données : édition et construction
- de traitement : analyse et modélisation
- de visualisation ou représentation de l’information géographique.

![](assets/fonctions.png)

## SIG vs Carto Traditionnelle
SIG:
- Gestion, traitement et affichage de base de données (géométries et attributs)
- Géoréférencement intégré
- Facilité du géotraitement (surtout répété)
- Mise à jour aisée
![](assets/)

Cartographie traditionnelle:
- Echelle fixe Information limitée
- Pas d’interrogation dynamique des objets
- Mise à jour difficile
![](assets/)

## Information discrète ou continue
Localisation de station météo
![](assets/)

Champ spatiale de température.
![](assets/)
*(source: European Environment Agency, eart.nullschool.net)*

# Modèle vecteur vs modèle raster
![](assets/)
*(source: Raoof Naushad (Medium), Marc Spiller (adapter from blogspot.com))*

## Primitves Géographiques
![](assets/)

# Couche thématiques
Une carte se compose de 
- Géométries
- Données attributaires

Le SIG permet de relier géométries et données attributaires --> géodonnées

Dans une carte thématique, on distingue les couches de fond de carte (essentiellement des géométries) de la -ou des- couche(s) thématique(s) (des données statistiques).

## Pas de bonne carte sans contexte
![](assets/)

Eléments d'habillage obligatoires:
- Titre, sous-titre (simple, accrocheur, descriptif)
- Légende(s) (titre clair, hiérachie, équilibre)
- Echelle (graphique de préférence)
- Sources (fond de carte, données, doit respecter les licences)
- Auteur.e (qui l'a crée, dans quel institut/bureau)
- Dates (données, fond et de création)

# Système géodésique (datum)

## Géoïde, ellispoïde et système géodésique
### Géoïde
![](assets/)

### Ellispoïde
![](assets/)
*(schéma : Messer Woland)*

### Système géodésique
![](assets/)

# Principe de projection

La terre est en 3D, mais nos visualisations (cartes) en 2D --> nous avons besoin d'une projection
![](assets/)
*Earth Peel (ESRI)*

Liste des projections les plus courantes avec les propriétés:
https://pro.arcgis.com/en/pro-app/latest/he lp/mapping/properties/list-of-supported-ma p-projections.htm

1. Surface de projection: Azimutale, Conique, Cylindrique
![](assets/)

2. Propriétés de conservation:
- Conforme = Angles (donc les formes)
- Équivalentes = Surfaces
- Équidistantes = Distances 
- Aphylactiques ≈ Angles/surf.
![](assets/)


## Projections : Exemples

Projection équivalente (Peters)
![](assets/)
![](assets/)

Projection équidistante
![](assets/)

Projection aphylactique (Robinson)
![](assets/)

## Projection de Mercator
cylindrique et conforme
![](assets/)
![](assets/)

## Projection de Mercator - En Suisse
En Suisse, le système géodésique local CH1903+ est basé sur l’ellispsoïde local de Bessel 1841.
La projection suisse (Swiss Grid) est une projection de Mercator oblique, donc cylindrique et conforme.
![](assets/)

## Localiser un point
Les coordonnées géographiques sont exprimées en latitude et longitude.

Par exemple dans le système WGS84 (EPSG:4326), Berne se trouve à 46°56′53 N et 7°26′50 E ou en degrés décimaux : 46.94, 7.44
![](assets/)

Après projection (globe → carte) on peut utiliser des coordonnées projetées (cartésiennes).
Le système de référence spatiale (SRS) dans lequel on se trouve est désigné par un code EPSG.
Exemple : dans le système UTM (Universal Transverse Mercator), la Suisse se trouve dans le fuseau T32 avec un méridien central à la longitude 9°Est. EPSG:32632
Dans ce sytème, Berne est à la coordonnées 381’500 / 5’200’800.

![](assets/)
(swisstopo)

Central meridian : 9 
False easting : 500’000 
False northing : 0

Le système de coordonnées suisses est basé aujourd’hui sur le cadre de référence MN95.

**EPSG:2056**

Dans ce système, Berne se trouve aux coordonnées
2’600’000 (Est) / 1’200’000 (Nord)
! inversion des coordonnées

![](assets/)
False easting : 2’600’000
False northing : 1’200’000
+ 3 translations depuis WGS84