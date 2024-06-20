# Instructions

Le deuxième travail pratique consiste en l'élaboration d'une carte thématique pour un indicateur précis et une région d'étude déterminée. 

La carte contiendra en plus un certain nombre de découpages géographiques ainsi que des informations statistiques. Ces éléments seront précisés plus loin.

Voici la région d'étude et l'indicateur pour votre TP:

```content
type: random_assignment
id: tp2-region
text: Votre région pour le TP2 sera:
options: Région de Zurich, Région de Berne, Région de Bâle, Région de Genève, Région de Lausanne, Région de Winterthour, Région de Thoune
```

```content
type: random_assignment
id: tp2-thematique
text: Votre indicateur pour le TP2 (pour la description de l'indicateur veuillez voir le fichier avec la liste des indicateurs):
options: P1, P2, P3, M1, E1, E2
```


## Données

L'ensemble des données nécessaires pour le TP sont disponibles dans le fichier ZIP suivant:

[tp2_data.zip](assets/tp2_data.zip) (version du 19.11.2023; 94 Mo)


## La région d'étude

La région d'étude se base sur un certain nombre de régions de mobilité spatiale (régions MS). Ces régions sont des anciennes régions d'analyse. Pour plus d'informations, consultez le site Web de l'OFS:

- [les informations générales sur les niveaux géographiques](https://www.bfs.admin.ch/bfs/fr/home/statistiques/themes-transversaux/analyses-spatiales/niveaux-geographiques.html)

- [les informations sur les différentes régions d'analyse](https://www.bfs.admin.ch/bfs/fr/home/statistiques/themes-transversaux/analyses-spatiales/niveaux-geographiques/regions-analyse.html)

- [les informations sur les régions MS](https://www.bfs.admin.ch/bfs/fr/home/statistiques/espace-environnement/nomenclatures/msreg.html)

La définition des régions d'étude du TP se trouve dans le fichier `definition_regions.ods` dans le fichier `tp2_data.zip`.

Les géométries des régions MS se trouvent dans le dossier `2023_GEOM_TK`. Il s'agit ici des [géométries de base de la section ThemaKart de l'OFS](https://www.bfs.admin.ch/bfs/fr/home/statistiques/statistique-regions/fonds-cartes/geometries-base.html). Le fichier `THK-Geometriedebase_CH_K4_f_2023.pdf` à l'intérieur du dossier `DOKU` décrit le contenu complet de ce jeu de données.


## Le maillage spatial

La carte thématique sera faite sur la base du découpage communale, sauf pour les grandes villes où le découpage se fait par quartier.

Les données SIG avec les géométries se trouvent toutes dans le fichier ZIP des données du TP2.

Les limites communales avec quartiers pour les villes se trouvent dans le dossier `2023_GEOM_TK`. Le fichier `THK-Geometriedebase_CH_K4_f_2023.pdf` à l'intérieur du dossier `DOKU` décrit le contenu complet de ce jeu de données.


## L'indicateur

Les indicateurs du TP sont décrites dans le fichier `definition_indicateurs.ods` dans le fichier ZIP des données du TP.

Les données de l'indicateur se trouvent soit dans le dossier `statpop2022` (indicateurs P1, P2, P3 et M1) ou `statent2021` (indicateurs E1 et E2).

Chacun de ces dossiers contient un fichier `README.md` qui précise le contenu.

Les données statistiques ne contiennent pas directement votre indicateur, mais toutes les variables nécessaires au calcul.


## La carte thématique

Vous devez faire la carte thématique avec le logiciel QGIS. La mise en page finale de la carte se fera à nouveau dans Adobe Illustrator.

La carte thématique devra contenir les éléments suivant:

- Les unités spatiales (communes et quartiers).

- L'indicateur représenté de manière appropriée.

- Il faut pouvoir distinguer les limites des communes et celle des quartiers. Autrement dit, il faut voir les limites des villes.

- Il faut également voir les régions MS de votre région d'étude, ainsi que les limites cantonales et le cas échéant nationales.

- Il faudra également voir la zone bâtie la plus grande de votre région d'étude. La zone bâtie est définie par la zone tampon de 200 mètres autour des bâtiments.

Par ailleurs, à côté de la carte, il faudra avoir les éléments habituels comme titre ou légende. Il doit être très clair ce que votre carte montre, vous devez donc faire tout le nécessaire pour que la thématique soit facile à comprendre.

En plus, vous devez ajouter une indication sur le nombre et la proportion d'habitants (indicateurs P1, P2 et P3), de ménages (indicateur M1) ou emplois équivalents temps plein (E1 et E2) qui se trouvent à l'intérieur respectivement à l'extérieur de la zone bâtie définie par la zone tampon des 200 mètres autour des bâtiments.


## La zone bâtie

Comme déjà mentionné ci-dessus, vous devez représenter la zone bâtie. Elle est définie par une zone tampon de 200 mètres autour des bâtiments. Les données des bâtiments sont fournies dans le fichier `swissTLMRegio_2023_4326_buildings.gpkg`. C'est à vous de calculer la zone tampon. Vous devez agréger les zones tampons qui se chevauchent.

Vous devez garder uniquement la zone tampon la plus grande de votre région. Pour déterminer la taille de la zone tampon, vous devez calculer la superficie de chacune des zones tampons de votre région.

Si la zone tampon la plus grande dépasse votre région d'étude, vous la devez représenter sur la carte dans son intégralité (donc aussi les parties en dehors de la région d'étude).

Vous devez également calculer le nombre total et la proportion d'habitants, ménages ou emplois pour cette zone bâtie. Cependant, pour cela, vous devez considérer uniquement la partie à l'intérieur de votre région d'étude. Les données nécessaires pour le calcul sont les données à l'hectare à l'intérieur du fichier GeoPackage dans `statpop2022` ou `statent2021`.

Les calculs de la zone tampon et du nombre total resp. de la proportion seront couverts plus tard, lors des traitements spatiaux des données vectorielles.
