# La cartographie et les SIG

Dans les SIG, la cartographie est essentiellement utilisée pour **visualiser rapidement les données et les résultats**. Après tout, il s'agit d'un Système d'Information, donc un système qui doit donner rapidement des renseignements, et non d'un outil d'édition de cartes. En même temps, il est clair qu'un SIG sera généralement en mesure de produire des cartes vu que c'est la méthode privilégié pour visualisation une information spatiale.

Par contre, en raison de l'héritage des systèmes d'information, les SIG ont quelques limitations au niveau de la cartographie et de la représentation graphique. Ainsi, le **modèle du territoire** utilisé avec notamment le **concept rigide des couches thématiques** amène quelques problèmes au niveau de la représentation. Les couches sont simplement dessinées dans l'ordre dans lequel elles sont définies dans la liste des couches du projet SIG. Ainsi, il sera par exemple difficile de représenter correctement les trains et les routes qui sont dans un SIG dans deux couches différentes. Est-ce que la couche des trains doit être par dessus ou en-dessous de la couche des routes? En réalité, il est clair que le train passe parfois par dessus la route, et parfois en-dessous.

Parfois, la situation est encore plus compliqué. Prenons l'exemple du viaduc de Brusio, dans les Grisons:

![](assets/viaduc-brusio.webp)

Ce viaduc est magnifique mais il pose la question comment le représenter dans une couche SIG avec les trains. L'ordre de dessin des entités dans un SIG n'est pas défini, et on ne pourra donc pas contrôler quelle ligne sera par dessus l'autre. Par ailleurs, un LineString simple comme défini dans la Simple Feature Specification n'est pas autorisé à se croiser lui-même...

On peut aussi considérer cet exemple:

![](assets/aerial-view-thusis.webp)

Ici, nous avons beaucoup de routes différentes, certaines dans un tunnel, d'autre qui passe par dessus ou par dessous, au niveau d'un tunnel ou sur des ponts. Et au milieu la ligne de train qui passe une fois par dessus la route, ensuite en-dessous pour passer par dessus une autre route qui se trouve dans un tunnel... Au niveau cartographique, ça doit ressembler à la fin à quelque chose comme ça:

![](assets/smr10-thusis.webp)


### Comment donc obtenir un résultat cartographique correct?

En gros, il y a deux solutions:

1. Faire du «bricolage» en multipliant les couches. En gros, il faut faire plusieurs couches avec les trains, les ponts, les routes etc. pour finalement arriver à un résultat convaincant. Vous trouvez plus bas une vidéo qui illustre comment Swisstopo organise les couches SIG pour produire une carte topographique.

2. On peut adapter le modèle du territoire et le principe des couches. Une solution est par exemple adopter un modèle dit topologique qui contient des informations sur la superposition des éléments dans les attributs. Un exemple de cette approche est le modèle de données utilisé pour [OpenStreetMap](https://osm.org). Cette adaptation va généralement de pair avec l'utilisation de logiciels de cartographie spécialisés (p.ex. [Mapnik](https://mapnik.org/)) même si les SIG ont commencé petit à petit à intégrer certaines des fonctionnalités comme la définition de l'ordre de rendu selon une valeur dans une colonne de la table d'attributs.


---

Voici une vidéo qui montre comment il est possible de gérer une carte topographique avec des couches vectorielles dans un SIG:

---

```content
type: video
id: construction-carte-topo
src: assets/carte-topo.m4v
```


## Autres limitations des SIG

La représentation graphique des couches SIG est toujours basée sur des règles. Ainsi, un contrôle graphique fin est difficile voire impossible. Prenons un exemple: nous avons une couche vectorielle avec les routes et une autre avec les bâtiments. Vous voulez faire une carte qui met en évidence certains bâtiments en les mettant en couleurs (p.ex. les bâtiments publics dans une ville). Pour cela, vous allez devoir ajouter un attribut dans la couche qui définit si un bâtiment est un bâtiment public ou non pour ensuite adapter le style de représentation dans le SIG.

En même temps, vous voulez mettre en évidence certaines routes qui se prêtent bien à la pratique du vélo, en les dessinant en plus épais et en couleur. Le fait que vous voulez faire les routes plus épaisses pose tout de suite un problème car la route couvre certains bâtiments. Il faudrait donc «pousser» les bâtiments (voir la partie sur la généralisation cartographique...), ce qui pose tout de suite des problèmes avec les éléments à côté des bâtiments à pousser. Vous vous retrouvez donc avec un problème qui nécessite l'adaptation manuelle du fond de carte pour une partie importante de la région à représenter, ce qui est une tâche très chronophage... Une alternative automatisée est au mieux insuffisante.

Un autre problème peut survenir avec certaines cartes thématiques. Les SIG offrent un choix pré-défini de représentations graphique d'une couche. Si la représentation souhaitée n'existe pas, on ne pourra que très difficilement faire la représentation souhaitée. Un exemple est la représentation en symboles proportionnels colorés avec le logiciel ArcGIS. Cette représentation n'est pas prévu, et du coup il faudra faire une couche séparée pour chaque classe avec des filtres correspondants. Si on a une carte avec 5 classes, on devra donc avoir 5 fois la même couche dans le projet SIG...


## Approche pragmatique utilisée souvent dans la pratique...

En raison de ces limitations mentionnées ci-dessus, l'approche suivante est souvent adoptée dans la pratique:

1. Tout d'abord, on prépare la carte dans un logiciel SIG

2. Ensuite, on exporte la carte en format PDF ou Illustrator. On peut même exporter couche par couche, à condition de fixer l'étendu géographique dans le SIG. Dans ce cas, on exporte chaque couche dans un fichier séparé et on les insère une par une dans un calque séparé dans Illustrator.

3. Les fichiers PDF ou Illustrator sont ensuite ouverts dans Adobe Illustrator, pour finaliser la carte dans le logiciel de graphisme.

Cette approche fait notamment du sens pour les documents destinés à l'impression, car les logiciels SIG ont souvent une gestion lacunaire des modèles de couleurs, notamment des couleurs CMYK.
