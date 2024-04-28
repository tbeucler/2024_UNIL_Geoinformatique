# Exercice

Les systèmes de coordonnées sont un sujet qui est souvent considéré comme étant un peu compliqué par les utilisateurs SIG. Il est donc important de faire les bonnes manipulations et surtout de comprendre ce qu'on est en train de faire (ce n'est pas si évident...).

Le but de l'exercice qui suit est relativement simple: arriver à une carte où chaque couche a le même système de coordonnées, c'est-à-dire le nouveau système de coordonnées projeté suisse (CH1903+/LV95).

Sur la carte, il faudra avoir les données suivantes:

- Le modèle numérique d'altitude (couche raster avec l'altitude par pixel)
- Les lacs et les limites des communes (de 2012)
- L'inventaire fédéral des paysages, sites et monuments naturels d'importance nationale (IFP)
- Les stations MétéoSuisse de mesure de la température pour le canton de Berne

**Défi supplémentaire**: Ajoutez également la localisation du trésor caché de votre amie Clémentine qui travaille au service des géodonnées de la ville de Brest, en Bretagne. Elle a caché le trésor lors d'un voyage en Suisse il y a environ 20 ans. Malheureusement elle n'a plus de souvenirs où c'était à part qu'il avait une combe avec des arbres. Par contre, elle a encore trouvé un fichier Shape avec la localisation du trésor, sauf que le système de coordonnées utilisé n'est malheureusement plus connu. Elle vous dit que ça pourrait être du Mercator transverse puisqu'elle ne connaissait pas le système de référence suisse. Est-ce que vous arrivez à localiser le trésor?

<a href="assets/exercice-crs-projections.zip"><i class="far fa-file-pdf"></i> Géodonnées pour l'exercice</a>

Ensuite, essayez de répondre aux questions suivantes:

- Dans quelle commune se trouve le trésor?

- Quel était le système de coordonnées du modèle numérique d'altitude dans le jeu de données initial ?
