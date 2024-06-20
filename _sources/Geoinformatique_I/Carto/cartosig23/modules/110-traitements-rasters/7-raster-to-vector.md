# Interroger une couche raster aux points d'une couche vectorielle

Il est possible d'interroger une couche raster à l'aide d'une couche vectorielle et de transférer les valeurs pixels d'une couche raster dans la table d'attributs d'une couche vectorielle. Ceci est par exemple utile pour déterminer l'altitude d'un point à l'aide du MNA.

Pour illustrer ce principe, nous allons ici extraire l'altitude de chaque bâtiment.

Pour cet exemple, nous aurons besoin d'une couche vectorielle des bâtiments et d'un Modèle Numérique d'Altitude (MNA, aussi appelé Modèle Numérique du Terrain MNT). Le MNA est une couche raster.

Nous pouvons par exemple utiliser le [MNT25 de Swisstopo](https://www.swisstopo.admin.ch/fr/geodata/height/dhm25.html) pour faire cet exercice. Ce jeu de données contient les courbes de niveau mais aussi une couche raster (le modèle matriciel) où chaque pixel a une taille de 25 mètres et contient l'altitude du pixel. Vous pouvez obtenir le fichier directement chez Swisstopo par le lien suivant: [https://cms.geo.admin.ch/ogd/topography/DHM25_MM_ASCII_GRID.zip](https://cms.geo.admin.ch/ogd/topography/DHM25_MM_ASCII_GRID.zip).

Pour les bâtiments, vous pouvez utiliser p.ex. le jeu [Swiss Map Vector 25](https://www.swisstopo.admin.ch/fr/geodata/maps/smv/smv25.html), ou encore [swissTLMRegio](https://www.swisstopo.admin.ch/fr/geodata/landscape/tlmregio.html) qui est plus généralisé.

Pour ajouter l'altitude du bâtiment, nous allons d'abord déterminer un point à l'intérieur du bâtiment pour lequel nous allons ensuite extraire l'altitude du pixel correspondant du MNA. Concrètement, nous allons utiliser deux fonctions dans la calculatrice des champs:

- la fonction `raster_value` qui permet d'obtenir la valeur raster d'une couche à indiquer à une localisation précise

- la fonction `pole_of_inaccessibility` pour extraire un point représentatif du polygone du bâtiment

Vous pouvez obtenir l'aide pour chacune des fonction dans la calculatrice des champs (il faut suivant comment cliquer sur le bouton «Show Help» en haut de la liste des fonction).

Concrètement, l'expression ressemblera à quelque chose comme ça:

```php
raster_value(
   'mnt25_ch_c48d408f_4ce2_48c7_800f_114e1b3becac',
   1,
   pole_of_inaccessibility(  $geometry, 1 )
)
```

La fonction `raster_value` nécessite d'indiquer le nom interne à QGIS de la couche raster (on le trouve dans la section «Map Layers» dans la liste des fonctions, le numéro de la bande (un MNT n'a qu'une seule bande, on indique donc 1), et le point pour lequel on veut obtenir la valeur pixel. Cette valeur est calculée à l'aide de la fonction `pole_of_inaccessibility` qui prend le polygone du bâtiment et la tolérance permise (1 mètre dans l'exemple ci-dessus). La géométrie du feature peut être obtenue avec la variable intégrée `$geometry`.

Voici à quoi ça ressemble:

![](assets/alti-batiments.webp)

Vérifiez le résultat. Il se peut que toutes les valeurs sont `NULL` et vous ne comprenez pas pourquoi. C'est très probablement un problème de projection. En effet, beaucoup des fonctions QGIS demandent à ce que toutes les couches impliquées dans un calcul ont le même système de coordonnées. Il faut donc suivant comment projeter certaines couches avant de faire l'opération de calcul.
