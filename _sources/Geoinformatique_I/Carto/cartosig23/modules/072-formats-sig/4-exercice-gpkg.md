# Exercice: créer une base de données GeoPackage

Comme nous avons vu, un «GeoPackage» est une base de données qui permet d'enregistrer plusieurs couches dans un seul fichier. Les objectifs de cet exercices sont:

- de reconnaître les différents formats de fichiers
- savoir manipuler ces formats
- créer une base de données de type GeoPackage
- sauvegarder des couches existantes dans un fichier GeoPackage


## Données de l'exercice

Dans le cadre de cet exercice, nous utilisons des données de Salzbourg, en Autriche. Vous pouvez télécharger les données ici:

<a href="assets/salzburg.zip"><i class="far fa-file-pdf"></i> Géodonnées de Salzbourg (fichier ZIP, 135 Mo)</a>

Créez à l'intérieur de votre dossier des projets SIG un nouveau dossier «Salzbourg». Décompressez l'archive ZIP à l'intérieur de ce dossier. Si vous voulez, vous pouvez le renommer en `data`.

Ensuite, explorez le contenu de ce dossier, et chargez quelques couches dans un nouveau projet SIG. Essayez de trouver une réponse aux questions suivantes:

1. Chargez la couche `MunicipalBoundaries` qui se trouve dans le dossier `City_of_Salzburg` dans votre projet SIG. Quel est le système de coordonnées de cette couche?

2. Parmi les **formats de fichiers** suivants, lesquels vous trouvez dans le jeu de données sur Salzbourg?

3. Chargez la couche `OSM_Salzburg_BuildingFootprints` dans votre projet SIG. Combien de «features» contient cette couche?

4. Chargez la couche `Hillshade_DGM10m` dans votre projet SIG. Il s'agit d'une couche raster avec le relief ombré. Quelle est la résolution en X de cette couche?


## Créer une base de données GeoPackage

La création d'un fichier GeoPackage se fait le plus simplement en exportant une couche existante:

+++
type: video
id: create-bd-gpkg
src: assets/create-geopackage.m4v
+++


## Ajouter une couche vectorielle à un GeoPackage existant

Un fichier GeoPackage est une base de données qui permet d'accueillir plusieurs couches en même temps dans un seul fichier. Pour ajouter une couche vectorielle existante à un GeoPackage, on va exporter la couche et donner comme destination un fichier GeoPackage existant, mais avec un nom de couche qui unique:

+++
type: video
id: add-vector-to-gpkg
src: assets/add-vector-to-gpkg.mp4
+++


## Ajouter une couche raster à un GeoPackage

Un fichier GeoPackage peut également accueillir des couches raster.

Cependant attention avec les couches raster: ces fichiers peuvent très vite être très gros! Pour des raisons pratiques, il est souvent plus simple de garder les couches raster à part dans des fichier GeoTIFF individuels. La gestion d'un GeoPackage qui a une taille de plusieurs To n'est pas évident...

Mais dans beaucoup de situations où la couche raster n'est pas trop grosse, cette option d'ajouter une couche raster au GeoPackage reste très intéressante:

+++
type: video
id: add-raster-to-gpkg
src: assets/add-raster-to-gpkg.mp4
+++

