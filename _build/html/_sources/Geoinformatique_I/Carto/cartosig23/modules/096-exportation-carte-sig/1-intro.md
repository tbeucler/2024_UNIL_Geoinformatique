# Exportation de la carte SIG vers le logiciel de graphisme

L'exportation d'une carte SIG vers un logiciel de graphisme comme Adobe Illustrator se fait généralement en plusieurs fois. Tous les éléments sauf la carte elle-même sont construits dans Illustrator. Cependant, nous allons inclure dans l'exportation une échelle et généralement une légende. Ces éléments seront reconstruits dans le logiciel de graphisme.

L'exportation de la carte SIG se fait depuis le gestionnaire d'impression sous forme de fichier PDF, en cliquant sur le bouton correspondant:

![](assets/pdf-export-1.webp)

Dans le dialogue des options d'export, il faut sélectionner impérativement l'option «Always export as vectors». On peut aussi cocher l'option «Simplify geometries to reduce output file size», au moins si on ne constate pas de problèmes topologiques dans le résultat final. Sinon, il faut suivant comment désactiver cette option.

Souvent on exportera quelques toponymes. Souvent, il faudra refaire les toponymes dans le logiciel de graphisme manuellement. Si on veut éditer les toponymes facilement, il faudra sélectionner dans le menu «Text export» l'option «Always Export Text as Text Objects» sans quoi le texte ne pourra pas être édité.

Les autres options peuvent être laissées désactivées:

![](assets/pdf-export-2.webp)

Les couches doivent souvent être exportées une par une. Pour cela, il est important de bloquer l'étendu géographique dans le composeur d'impression (utiliser l'option de calcul de l'étendu). Ceci se produit notamment dans les cas suivants:

- Nous avons des images raster dans notre projet QGIS. Il est conseillé de les exporter à part.

- Nous utilisons des transparences. Il est conseillé de ne pas utiliser les transparences dans QGIS, mais de les appliquer dans le logiciel de graphisme.

- Nous voulons ajouter plus tard une couche que nous avons oublié. Dans ce cas, il est important d'avoir enregistré le projet QGIS et d'avoir une structure de fichiers et dossiers correcte.


## Le problème de la légende des symboles proportionnels

Pour obtenir des symboles proportionnels dans QGIS, nous utilisons une formule pour calculer la taille manuellement. Cette façon de faire est très flexible et permet de créer des cartes correctes. Cependant, le désavantage est que QGIS ne va pas pouvoir produire une légende correcte. Pour palier à ce problème, nous procédons de la manière suivante:

- Nous créons une nouvelle couche vectorielle de points. La couche aura un attribut numérique qui contiendra la valeur des symboles de la légende.

- Nous ajoutons un point par symbole de la légende, et donnons la valeur correspondante à l'attribut. Généralement, le point sera localisé un peu à côté de la carte (p.ex. là où on placera la légende).

- Nous appliquons la formule de la couche des symboles proportionnels aussi à cette couche.

- Nous exportons cette couche lors de l'export de la carte (attention que l'échelle est identique). Ceci nous permettra de reconstruire la légende avec les bonnes tailles des symboles.
