# Introduction

Chaque couche vectorielle possède une table d'attributs. Elle permet d'associer à chaque entité géographique une série d'attributs. La table d'attributs est généralement montrée comme un tableau avec les entités géographiques en lignes et les attributs en colonnes. Voici comment une table d'attribut peut se présenter dans QGIS:

![](assets/qgis-table-attributs.png)

Cette table d'attribut ressemble donc un peu à un tableau Excel. Mais en réalité, il s'agit d'une base de données ce qui donne un certain nombre de contraintes. Ainsi, les colonnes ont des **noms** bien précises qui ne peuvent pas être changés facilement. Souvent, on ne peut pas choisir n'importe quel nom, mais on est limité sur les caractères permis et/ou la longueur du nom. Par exemple dans le cas d'un fichier Shape, la longueur du nom d'une colonne est limitée à 11 caractères. Il est conseillé de n'utiliser que des caractères a-z (en minuscules, car certains systèmes d'opération font une différence entre majuscules et minuscules, d'autres non), des chiffres 0-9 mais pas comme premier caractère du nom, et des tirets bas (_). Même si d'autres caractères sont permis, évitez de les utiliser. L'expérience montre qu'en se limitant à ces quelques caractères, on minimise les problèmes ultérieurs qui semblent parfois bizarres (p.ex. un outil SIG qui ne fonctionne pas et on ne sait pas pourquoi...).

Chaque colonne possède aussi un **type** et ne permet pas d'enregistrer n'importe quel type de données. Les types exactes possibles dépendent du format de fichier utilisé. En général, une colonne peut prendre un des types suivants:

- **nombre entier** (en anglais: integer)
- **nombre à décimales** (en anglais: *real*, parfois *float* ou *double*)
- **texte** (parfois appelé *chaîne de caractères* ou en anglais *string*)
- **date**

Il ne sera pas possible par exemple d'enregistrer le nombre *7.5* dans un champ à nombres entiers. On pourra enregistrer le texte *7.5* dans un champ texte, mais on ne pourra pas faire de calculs (car pour le SIG il s'agit d'un texte et non pas d'un nombre!).

Un champ texte peut être limité sur la longueur. Dans ce cas il faut spécifier le nombre de caractères qui peuvent être enregistrés, avec souvent un maximum possible d'environ 250 caractères.

Un champ de type nombre à décimales peut aussi avoir des limites de longueur. Dans ce cas, il  faut généralement spécifier le nombre total de chiffres y compris le point décimal (donc le nombre 7.5 a une longueur de 3), ainsi que la précision qui correspond au nombre de décimales.

Le type de chaque attribut peut être trouvé dans les propriétés d'une couche, dans l'onglet «Fields». Voici un exemple d'une table d'attributs avec la définition des attributs (en bas):

![](assets/qgis-attribute-table-types.png)

On peut par exemple voir que l'attribut «ID0» est de type «string», donc un texte, même s'il contient uniquement des nombres. On ne pourra pas faire de calculs avec cet attribut.

## Éditer les attributs

La table d'attributs est par défaut en mode lecture seule, tout comme les géométries de la couche. Pour modifier les attributs, il faut passer en **«mode édition»** à l'aide du petit bouton avec le crayon en haut à gauche de la fenêtre de la table d'attributs.

Ensuite, il est possible d'éditer le contenu de chaque attribut. Une fois que les modifications ont été faites, il faut sortir du mode édition en cliquant à nouveau sur le bouton avec le crayon. Au plus tard à ce moment il faut **enregistrer les modifications** faites dans la table d'attributs.


## Supprimer des attributs

Il est possible de supprimer une ou plusieurs colonnes de la table d'attributs. Pour cela, il faut passer en mode édition, et ensuite l'icône pour supprimer des attributs devient active:

![](assets/delete-attribute.webp)


## Créer un nouvel attribut vide

Pour créer un nouvel attribut sans contenu, il faut passer en mode édition, et ensuite le bouton pour créer un nouvel attribut devient actif. Ensuite, il faut saisir le nom et le type:

![](assets/new-attribute.webp)

Notez que l'ordre des attributs n'est à priori pas défini. Il est possible de la modifier temporairement à l'aide du bouton «Organize Columns» (à droite du bouton de suppression d'attributs).

Dans l'étape suivante, on regarde comment on peut faire des calculs avec les valeurs des attributs et ainsi mettre à jour un contenu existant ou créer un attributs qui contient déjà des valeurs.
