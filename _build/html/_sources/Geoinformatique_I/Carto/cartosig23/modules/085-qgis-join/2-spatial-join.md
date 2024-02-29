# Jointure spatiale

La jointure que nous avons vu à l'étape précédente nécessite d'avoir un attribut dans les deux tables contenant la même information. Cependant, dans un SIG, nous avons également la position géographique qui peut permettre de faire des liens entre couches. Nous pouvons par exemple nous imaginer que nous avons une couche avec des bâtiments, et une autre couche avec les communes. Maintenant nous souhaitons d'exploiter la localisation géographique pour joindre les attributs de la couche des communes à la table d'attributs des bâtiments. Ainsi, on pourra p.ex. avoir le nom de la commune pour chaque bâtiment. Ce concept est appelée une **jointure spatiale**.

Dans une jointure spatiale il peut y avoir plusieurs types de relations géométriques, comme des intersections, appartenances etc. Lors d'une jointure spatiale, il faut spécifier quel type de relation on souhaite considérer.

Une jointure spatiale peut avoir une relation 1:1 (comme pour la jointure par attribut), où chaque entité de la couche A correspond exactement à une entité de la couche B. Cependant, ce n'est évidemment pas toujours le cas. Lors d'une relation 1:N, selon la direction de la jointure, il faudra décider comment on veut traiter plusieurs entités qui doivent être jointes à une seule entité. Plusieurs stratégies existent, dont notamment le calcul d'une somme ou de la moyenne pour un attribut, ou la duplication de l'information, etc.

Pour voir comment effectuer une jointure spatiale dans QGIS, nous considérons le cas suivant: nous avons une couche vectorielle des communes, et une autre couche vectorielle des bâtiments. Nous voulons ajouter quelques attributs de la couche des communes à celle des bâtiment. Ainsi, nous pourrons p.ex. savoir dans quelle commune se trouve chaque bâtiment sans recourir à la couche des communes.

Pour faire la jointure spatiale, nous devons d'abord charger les deux couches dans QGIS. Ensuite il faut ouvrir le panneau de GeoProcessing pour ensuite chercher l'outil de jointure par localisation:

![](assets/spatial-join.webp)

On note qu'il y a deux fonctions de jointure spatiale, une pour effectuer des jointures normalement, et une autre pour faire des calculs statistiques. Cette dernière variante pourrait par exemple être utilisée pour calculer la somme des superficies de tous les bâtiments par commune. Les deux variantes se ressemblent fortement. Dans notre exemple, nous utilisons la première version de la jointure spatiale simple car nous pouvons admettre que pour chaque bâtiment nous n'aurons qu'une seule commune.

Dans le dialogue qui s'affiche, nous devons d'abord sélectionner les deux couches:

![](assets/spatial-join-dialog.webp)

La couche de base est celle qui va accueillir les attributs de la couche de jointure.

Nous devons aussi définir la relation géométrique souhaitée. La relation d'intersection peut être considérée si une partie de la géométrie de la couche de base s'intersecte avec une géométrie de la couche de jointure. Pour le cas des bâtiments et communes, nous pouvons rester avec ce choix, ou opter pour la relation *«within»* (à l'intérieur de). Les deux doivent en principe donner le même résultat sauf si un bâtiment devait être sur plusieurs communes (ce qui peut arriver, il y a même des bâtiments sur deux pays).

Ensuite, il faut encore définir le type de jointure (en gros relation 1:1 ou 1:N).

Finalement, le résultat de la jointure se trouvera dans une nouvelle couche. Par défaut, QGIS crée une couche temporaire qui devra être exportée pour devenir pérenne. Mais il est possible de directement spécifier la couche de sortie.

Suivant la complexité des deux couches impliquées, une jointure spatiale peut prendre un petit moment pour le calcul.
