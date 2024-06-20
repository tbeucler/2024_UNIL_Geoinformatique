# Tutoriel 8 - Données spatiales (A)

Dans cette section, nous aborderons les points suivants:

- Principe et intérêt de l'OpenData
- Métadonnées
- Géodatabase

# OpenData

Les données publiques ouvertes (Open Government Data) sont les données du secteur public que l’État et l’administration mettent à disposition dans l’intérêt général. Elles peuvent être exploitées, redistribuées et réutilisées gratuitement.

Exemple des conditions d'utilisation des géodonnées et géoservices gratuits (OGD) de swisstopo : Les géodonnées et les géoservices gratuits de swisstopo peuvent être utilisés, distribués et rendus accessibles. En outre, ils peuvent être enrichis et transformés et être également utilisés à des fins commerciales.

![](assets/)
* https://opendefinition.org/licenses/ 
* http://ggim.un.org/ggim_20171012/docs/meetings/GGIM7/Agenda%208%20-%20Compendium%20on%20Licensing%20of%20Geospatial%20Information.pdf 

## Licences et sources

Une indication de la source est obligatoire sur toutes les représentations graphiques et publications, numériques ou analogiques, ainsi qu’en cas de transmission.
L’info sur la manière de citer les sources de données est toujours disponible via un lien sur la page de téléchargement, directement sur celle-ci ou dans les métadonnées.

**Responsabilité individuelle**

Pour swisstopo, choix entre:
- Office fédéral de topographie swisstopo
- ©swisstopo

Pour Open Street Map, il faut indiquer : 
- OpenStreetMap + lien ou url écrite openstreetmap.org/copyright

## Sources de données

**Portail et guichet cartographique / métadonnées**
• OFS https://www.bfs.admin.ch/bfs/fr/home/statistiques/statistique-regions/atlas/atlas-stati
stique-interactif-suisse.html
• Swisstopo (suit les principes de l’OGD depuis le 1er mars 2021) https://shop.swisstopo.admin.ch/fr/products/free/free_geodata
• VD https://www.asitvd.ch/chercher/guichets-cartographiques.html
• OSM https://www.openstreetmap.org
• Opendata.swiss https://opendata.swiss/fr/
• Geodienste.ch https://www.geodienste.ch/
• Geocat.ch (catalogue de métadonnées pour l'ensemble des géodonnées suisses) https://www.geocat.ch/geonetwork/srv/fre/catalog.search#/home
•... 
**UNIL**
• https://www.unil.ch/gis/fr/home.html
• /!\ demande d’accès aux géodonnées de l’UNIL via le formulaire

# Métadonnées

**Les métadonnées sont un mode d’emploi des données.**
Informations...
... d’identification : titre, description, mots-clefs
... de contact : créateur, éditeur, distributeur des données
... de qualité et validité : précision, date, mise à jour, complétude ... géographiques : système de référence, étendue, maillage
... de contenu : géométries, attributs
... légales : accès, licence, distribution, usage

Standards : ISO19115 (international) et GM03 (Suisse)

Exemple
https://viageo.ch/catalogue/donnee/200712

## Les principes fair
Principes à appliquer à vos projets universitaires (yc rapport personnel SIG!).
Un cadre pour la production, la publication et le partage de données publiques (open data), scientifiques (open sciences), etc. Aussi valable pour des données «fermées».

**Autodiagnostic**
![](assets/)

![](assets/)

## Format de données
![](assets/)
**Vecteur**
Le format SHP (ESRI Shapefile) est devenu standard de fait.
Attention, ce format se traduit matériellement par plusieurs fichiers portant le même nom, mais avec diverses extensions : .shp, .shx, .dbf, .prj, .cpg, etc. (les 3 premiers sont obligatoires).
Les données ponctuelles sont parfois fournies comme une simple table CSV, avec deux attributs stockant les coordonnées de chaque point.
Autres formats courants : GeoJSON (ouvert), DXF (AutoCad), KML (GoogleMaps).

**Raster**
Une immense variété de formats : .
On recommande le (Geo)TIFF pour favoriser l’interopérabilité. Le format ESRI Grid n’est pas un standard.

## Base de données géographiques

Permet de stocker ensemble, de manière structurée, toute une arborescence de données. Facilite le transfert de données et les requêtes, aussi depuis l’extérieur du SIG (par exemple, serveur web).

**Format interopérable**
OCG Geopackage (.gpkg), basé sur le SGBD SQLite
Format bientôt standard sur QGIS (à la place du shapefile), mais probablement jamais sur ArcGIS

**Format propriétaire ESRI ArcGIS**
File Geodatabase (et aussi Personnal Geodatabae et Entreprise Geodatabase)
→ la File Geodatabase se concrétise comme un ensemble de fichiers et de dossiers sur l’ordinateur, quel que soit le système d’exploitation.

# Géodatabase

La base de données géographique peut contenir :
Des géodonnées vectorielle (table attributaire + géométrie)
Des données (table attributaire seule) Des géodonnées raster
![](assets/)

## Structure
Pour les données vectorielle, l’unité de base est la **Feature class**, une table regroupant des objets avec la même primitive géographique (points, lignes ou polygones).
Plusieurs Feature classes peuvent être regroupées dans un **Feature dataset** si elles partagent le même système de coordonnées.
On peut organiser nos données thématiquement dans plusieurs Feature datasets.

**Attention à la logique de vos données de base, en fonction de ce que vous allez en faire :**
**tous les points dans une même table, différenciés par un attribut TYPE ou une table différente pour chaque type, le tout dans un Feature dataset?**
![](assets/)

**Bonnes pratiques à adopter**
Nommer logiquement vos tables (Feature class) :
- sans espaces, lettres accentuées ou autres
- en mentionnant la primitive géographique _pnt _lin _pol 
- avec un nom explicite mais court, p.ex. BAT_ZE_2020_po

Utiliser la structure en jeux de données (Datasets) pour séparer :
- les données sources (intactes)
- les couches temporaires, de travail
- les données de résultats, définitives

Réfléchir à une arborescence logique et thématique, avec des sous-datasets