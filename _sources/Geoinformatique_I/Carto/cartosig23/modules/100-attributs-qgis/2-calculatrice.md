# Calculatrice des champs

La calculatrice des champs est un outil très puissant qui permet de modifier le contenu d'un attribut sur la base de calcul, ou de créer un nouvel attribut avec le contenu défini par le calcul.

La calculatrice des champs peut en principe être accédée par différents biais, une des façon est depuis la table d'attribut en cliquant sur l'icône correspondant:

![](assets/icon-calculator.webp)

Dans la fenêtre de la calculatrice, il faut d'abord décider si on veut créer un nouvel attribut, ou si on veut mettre à jour un attribut existant:

![](assets/calculator-create-update.webp)

Si on crée un nouvel attribut, il faut évidemment choisir un nom et un type comme décrit dans la section sur la création d'un nouvel attribut.

Par ailleurs, il est important que **le type de l'attribut et le résultat du calcul sont compatibles**. Si on calcule par exemple un pourcentage, le type de champs devra être de type nombre à décimales (*real* avec suivant comment une précision appropriée).

Ensuite, nous pouvons saisir la formule pour le calcul. Pour le calcul, il est possible d'utiliser tous les attributs existants ainsi qu'un nombre de fonctions pour différents calculs. Il y a une liste avec toutes les fonctions disponibles. On y trouve également sous la rubrique *«Fields and Values»* la liste de tous les attributs existants. Il suffit de double cliquer sur une entrée pour qu'elle est copiée dans le champ d'édition de la formule à gauche.

Ainsi, nous pouvons par exemple calculer une valeur de pourcentage très facilement, p.ex.

![](assets/calculator-prop.png)

Si le calcul est juste, un exemple de résultat s'affiche en bas à gauche. Si la formule n'est pas correcte, vous allez trouver un message d'erreur à cet endroit.

Une fois que l'on clique sur le bouton «OK» le calcul est exécuté pour l'ensemble des entités géographiques.

Parmi toutes les fonctions disponibles dans QGIS, nous trouvons par exemple la possibilité de convertir un nombre entier qui est stocké dans un attribut texte (et qui ne peut donc pas être utilisé pour des calculs) en «vrai» nombre entier. Nous devons utiliser une fonction de conversion pour cela. Cette fonction se cache dans la section «Conversions» et s'appelle `to_int`. Voici un exemple d'utilisation:

![](assets/text2int.png)


## Appliquer le calcul pour une partie des entités géographiques seulement

Parfois, il est utile de faire un calcul uniquement pour une partie des entités géographiques. Dans ce cas, nous pouvons sélectionner avant d'entrer dans la calculatrice des champs les entités géographiques pour lesquelles nous souhaitons faire le calcul à l'aide des outils de sélections habituels.

Ensuite, une fois que l'on ouvre la calculatrice des champs, un bouton apparaît tout en haut de la fenêtre (facile à louper!) qui permet de restreindre le calcul sur les entités sélectionnées uniquement:

![](assets/calculatrice-selection.webp)

**Attention!** Si vous avez sélectionné des entités dans la carte, cette option est cochée par défaut. Donc si vous voulez faire le calcul pour toutes les entités, n'oublier pas de décocher cette option avant de faire le calcul.


## Conseil pratique

La formule saisie dans la calculatrice des champs n'est pas gardée en mémoire comme c'est par exemple le cas dans Excel. Le calcul est effectué au moment de cliquer le bouton «OK». Ensuite, QGIS va fermer la fenêtre de la calculatrice. Si vous voulez répéter le même calcul, vous devez saisir à nouveau la formule.

Il est donc une bonne idée de **copier-coller toutes les formules avant d'exécuter le calcul** et de les garder dans un fichier texte à côté. Ceci permet de facilement refaire le calcul (p.ex. si on a oublié de désélectionner l'option d'appliquer le calcul uniquement aux entités sélectionnées...), et en plus, nous avons une trace des calculs que nous avons fait.
