# Définir le système de coordonnées

Dans un SIG, il faut définir le système de coordonnées à deux endroits très différents:

1. Pour la carte que nous voulons faire
2. Pour chaque couche que nous chargeons dans notre projet SIG

Si le système de coordonnées de la carte n'est pas le même que celui des couches, le SIG va devoir faire une projection. Cette projection peut être automatique (avec parfois des limites au niveau de la précision), ou on peut l'ajuster manuellement en projetant toutes les couches dans le système de coordonnées de la carte.

Évidemment, il peut arriver que certaines couches n'ont pas le même système de coordonnées que d'autres. Du coup, le SIG doit aussi faire une projection, ou vous procédez à une projection manuelle d'une ou plusieurs couches.

Il peut aussi arriver que pour certaines couches, le système de coordonnées est soit inconnu pour le SIG, soit il est carrément faux. Dans ce cas, il faudra indiquer au SIG le bon système de coordonnées pour la couche.

Passons en revue comment régler les différents cas liés aux systèmes de coordonnées.

## Définir le système de coordonnées pour la carte

Le système de coordonnées pour la carte est définie dans QGIS dans les propriétés du projet.

Généralement, QGIS va définir le système de coordonnées du projet selon la première couche qui est ajoutée. Mais nous pouvons aussi le définir manuellement en faisant un clic droit sur le boutons des systèmes de coordonnées en bas à droite, ou en allant dans le menu «Project > Properties». Ensuite il faut choisir l'onglet «CRS» et sélectionner le bon système de coordonnées.

En principe, étant donné que nous faisons une carte en deux dimensions, nous choisirons un système de coordonnées dans «Projected Coordinate Systems». Les systèmes de coordonnées dans «Geographic Coordinate Systems» utilisent tous les coordonnées latitude/longitude, ce qui n'est pas idéal pour une carte 2D.

Souvent, nous allons utiliser le système de coordonnées local, en l'occurrence le nouveau système de coordonnées suisse CH1903+/LV95, ou peut être encore l'ancien CH1903/LV03. Il suffit de chercher dans le filtre en haut «CH1903» pour avoir une liste relativement courte des systèmes de coordonnées suisses. Faites attention de choisir le bon système de coordonnées. Vérifiez toujours l'identifiant du système de coordonnées à droite dans la liste. Le code EPSG pour CH1903+/LV95 est 2056, et celui de l'ancien système de coordonnées est le 21781.

Voici le dialogue qui permet de définir le système de coordonnées:

![](assets/project-crs.png)


## Définir le système de coordonnées pour une couche

Si une couche a un système de coordonnées inconnu, ou le mauvais système de coordonnées est défini, nous devons **définir le système de coordonnées**. Dans ce cas, nous changeons uniquement l'indication quel système de coordonnées doit être utilisé pour représenter les coordonnées. Les coordonnées en tant que tel ne seront pas affectés.

Pour illustrer cela, imaginons que nous avons un fichier avec une coordonnées 600'000/200'000, et le système de coordonnées défini est EPSG:2056 (le nouveau système de coordonnées suisse). Or, nous savons que les coordonnées de CH1903+/LV95 devraient avoir 7 chiffres et non pas 6, au moins pour les points localisés en Suisse. Nous avons donc le soupçon que ces coordonnées sont en réalité des coordonnées dans l'ancien système de coordonnées. Nous allons donc indiquer à QGIS que le bon système de coordonnées est le EPSG:21781.

Regardons comment nous pouvons définir le système de coordonnées d'une **couche**. Pour cela, nous faisons un clic droit sur la couche et choisissons ensuite «Properties...». Ensuite nous allons dans l'onglet «Source». Nous pouvons choisir le bon système de coordonnées à l'aide du menu déroulant dans «Assigned Coordinate Reference System (CRS)», respectivement en cliquant sur le petit bouton à droite du menu:

![](assets/layer-crs.png)



## Projeter une couche

Si on a une couche avec un système de coordonnées correctement défini, nous pouvons le *projeter* dans un autre système de coordonnées. Il s'agit ici d'une **transformation des coordonnées**. Donc les valeurs des coordonnées changent dans le fichier.

La projection est donc fondamentalement différente de la définition simple du système de coordonnées. Ici, nous allons vraiment changer les géométries de la couche. Une image raster devra être recalculée et pourra éventuellement être déformée (car un rectangle n'est pas nécessairement un rectangle dans un autre système de coordonnées).

Pour projeter une couche dans QGIS, on va simplement l'exporter et changer le système de coordonnées dans le dialogue d'enregistrement. Pour exporter une couche, on peut faire un clic droit sur la couche et ensuite dans le menu contextuel choisir «Export > Save As...». La même option est accessible dans le menu «Layer > Save As...».

Dans la fenêtre qui s'ouvre, on devra choisir un nouveau nom (cliquer sur le boutons avec les trois petits points à droite du champ de texte), et surtout définir le nouveau système de coordonnées de destination:

![](assets/projection.png)


## Les fichiers de transformation

Parfois, QGIS va se plaindre qu'il n'a pas trouvé le fichier de transformation qu'il lui faut pour projeter d'un système de coordonnées vers un autre. Probablement le cas le plus fréquent que nous allons rencontrer est la transformation de l'ancien système de coordonnées suisse CH1903/LV03 vers le nouveau CH1903+/LV95.

QGIS vous donnera en principe un lien de téléchargement vers le fichier nécessaire. Pour le cas de la projection entre les deux systèmes de coordonnées suisses, il vous faudra un fichier qui pèse 3 Mo environ. Le fichier proposé par QGIS pèse environ 180 Mo puisqu'il contient plein d'autres fichiers de transformation. Pour simplifier un peu les choses, vous pouvez télécharger les fichiers relatives à la Suisse directement ici:
