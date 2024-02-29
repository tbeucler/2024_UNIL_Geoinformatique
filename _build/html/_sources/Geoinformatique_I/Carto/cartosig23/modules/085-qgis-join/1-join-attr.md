# Jointure par attribut

Souvent il est nécessaire de combiner deux tables d'attributs, respectivement une table d'attribut et un tableau Excel (ou LibreOffice Calc). Nous pouvons considérer le cas suivant:

![](assets/join-orig-data.png)

Dans ce cas nous avons un tableau LibreOffice Calc avec une colonne qui contient l’abréviation du canton et une deuxième colonne avec la population résidente en 2020.

Pour combiner ces deux tableaux, nous pouvons **joindre le tableau LibreOffice à la table d'attributs**. Pour cela, nous devons avoir dans chaque tableau une colonne qui contient des valeurs correspondantes. Le principe de la jointure dans un SIG suit donc une logique de colonne identique. On parle alors d'une **jointure par attribut**. Une telle jointure nous permet de compléter une table d'attribut avec d'autres attributs. La jointure dans un SIG fait surtout du sens si nous avons les mêmes entités dans la couche comme dans le tableau. Les données pour lesquelles il n'y a pas de correspondance seront écartées. **Il s'agit en fait d'une relation 1:1**.

Lors d'une jointure dans un SIG, les attributs de la couche liée sont ajoutées à la table d'attribut tant que le jointure existe. Les deux sources de données impliquées ne sont pour ça pas modifiées. Pour rendre une jointure pérenne, il faut exporter la couche vectorielle comportant la jointure pour ainsi créer une nouvelle couche vectorielle.

Pour montrer le principe de la jointure par attribut dans QGIS, nous considérons à nouveau le cas des deux tables ci-dessus. Dans ce cas nous avons un tableau LibreOffice Calc avec une colonne qui contient l’abréviation du canton et une deuxième colonne avec la population résidente en 2020.

Il faut faire attention au formatage du tableau LibreOffice Calc. Sur la première ligne il doit y avoir les noms des colonnes, et il ne doit pas y avoir d'autres informations que les noms des colonnes et les données elles-mêmes. Dans beaucoup de situations, il faudra donc créer un nouveau fichier LibreOffice Calc et le formater au plus simple possible.

Pour combiner ces deux tableaux, nous allons **joindre le tableau LibreOffice à la table d'attributs**. Dans ce cas, la colonne «canton» du tableau LibreOffice contient les mêmes valeurs que l'attribut «abbr» de la table d'attributs. Nous allons donc utiliser ces deux champs pour faire correspondre les lignes du tableau avec les entités géographiques de la couche vectorielle.

Pour effectuer la jointure, nous devons d'abord ajouter la couche vectorielle ainsi que le tableau au projet QGIS. La façon de le faire est un peu surprenante: QGIS considère un fichier Excel ou LibreOffice comme une couche vectorielle sans géométrie. Il faut donc aller dans le dialogue pour ajouter une couche vectorielle et ensuite on sélectionne simplement le fichier Excel ou LibreOffice et non pas un fichier Shape:

![](assets/add-ods-file.png)

QGIS ajoute le tableau dans la liste des couches et nous pouvons en consulter la table d'attributs:

![](assets/ods-layer.png)

Une fois que la couche vectorielle et le tableau sont chargés dans QGIS, nous pouvons procéder à la jointure. Pour cela, nous allons dans les propriétés de la couche vectorielle et ensuite dans l'onglet «Joins». À l'aide du bouton avec le plus vert en bas de la page, nous pouvons ajouter une nouvelle jointure:

![](assets/join-dialog.webp)

Ensuite, nous pouvons sélectionner le tableau duquel les attributs doivent être ajoutés à la table d'attributs de la couche de destination. Il faut également spécifier les deux champs de correspondance pour permettre la jointure.

Finalement, il est conseillé de supprimer le préfixe que QGIS va ajouter au nom de l'attribut en activant la section *«Custom field name prefix»* et en supprimant le contenu. Ceci est particulièrement important avec les fichiers Shape, car les noms des attributs avec ce format de fichier sont limités à 11 caractères.

Une fois que la jointure a été spécifiée, nous pouvons ouvrir la table d'attributs de la couche vectorielle. Les attributs joints apparaissent à la fin de la table:

![](assets/join-result.webp)

Pour les valeurs pour lesquelles aucune correspondance n'a été trouvée, l'attribut obtient la valeur `NULL`.

**Il est important à noter que la jointure n'a pas modifié la table d'attributs de la couche vectorielle. Il s'agit juste d'un lien temporaire.** Il est fortement recommandé de pérenniser la jointure pour avoir une copie des attributs joints dans la couche vectorielle. Pour faire cela, nous devons **exporter la couche vectorielle avec le tableau joint dans une nouvelle couche vectorielle** en cliquant avec le bouton droit de la souris sur la couche vectorielle et en choisissant «Export > Save Features As...»:

![](assets/export-save-as.webp)

Une fois que l'export a été effectué et que la nouvelle couche est chargée dans QGIS, nous pouvons enlever les deux couches utilisées pour la jointure.

Il faut encore noter que même si nous avons fait ici la jointure entre une couche vectorielle et un tableau LibreOffice, il est évidemment possible de faire une jointure entre deux couches vectorielles.

Encore une fois: lors d'une jointure avec un tableau Excel ou LibreOffice, il faut faire très **attention à la structure des données dans le tableau**. Idéalement, il faut avoir un fichier avec une seule feuille. Ensuite, la première ligne doit contenir tous les noms de colonnes. Pour le nom il est une bonne idée de respecter les conventions de la couche de destination (p.ex. dans un fichier Shape uniquement 11 caractères). La première colonne du tableau doit être dans la colonne A. Et à partir de la ligne 2, il faut ajouter les données. Il ne faut pas laisser de colonne ou ligne vide.
