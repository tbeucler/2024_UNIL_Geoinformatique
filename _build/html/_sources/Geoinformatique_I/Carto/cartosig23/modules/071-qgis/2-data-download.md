# Téléchargement d'un jeu de données SIG

Afin de pouvoir travailler avec un SIG, nous allons avoir besoin de quelques données. Nous allons expliquer un peu plus tard dans le cours les différents formats de données SIG et comment créer, gérer et convertir des données. Pour le moment, il nous suffit de disposer d'un jeu de données qui nous permet de faire les premiers pas avec le logiciel.

Nous allons utiliser ici un jeu de données assez varié sur une région de la Caroline du Nord, aux États-Unis. Ce jeu de données qui peut être diffusé librement (avec une licence CC) a été développé spécifiquement pour apprendre les SIG. Il a été préparé par Markus Neteler et Helena Mitasova pour leur livre de 2008 *«Open Source GIS: A GRASS GIS Approach»*. Vous pouvez consulter la page d'explication du jeu de données ici: [https://grassbook.org/datasets/datasets-3rd-edition/](https://grassbook.org/datasets/datasets-3rd-edition/). Il y a également une description détaillé ici: [https://wiki.osgeo.org/wiki/Edu_Data_Package_North_Carolina](https://wiki.osgeo.org/wiki/Edu_Data_Package_North_Carolina)

Même si nous n'allons pas utiliser GRASS GIS, le jeu de données peut être utilisé avec n'importe quel logiciel SIG. Vous pouvez le télécharger directement ici:

<a href="assets/nc.zip"><i class="far fa-file-pdf"></i> Jeu de données Caroline du Nord (fichier ZIP)</a>

Le jeu de données vient sous forme de fichier ZIP. Avant de l'utiliser il faut le décompresser. Sur Windows, il ne suffit pas de double-cliquer sur le fichier, ça ne fait que d'afficher le contenu, ça ne décompresse pas le contenu de l'archive ZIP.


## Organiser les données pour travailler avec un logiciel SIG

Dans le logiciel SIG nous allons créer un *document de projet*. Dans QGIS, il s'agit d'un fichier avec extension .qgs ou .qgz. Il est important à savoir que ces **fichiers de projet ne contiennent pas les données SIG,** car sinon il deviendraient extrêmement gros. Les fichiers de projet contiennent uniquement une **référence** vers le jeu de données SIG, c'est-à-dire le *chemin d'accès* des données (donc sur Windows quelque chose comme `C:\geodata\...`).

L'avantage de ce système est que les fichiers de projet restent gérables, et que nous pouvons utiliser le même jeu de données dans plusieurs fichiers de projet SIG.

L’inconvénient est que nous devons avoir une organisation rigoureuse et bien réfléchie des données et projets. Il est important de ne pas déplacer les données SIG, sinon le chemin d'accès des données change et le logiciel SIG ne trouvera plus les données à charger lors de l'ouverture du fichier de projet.

De manière pratique, il y a plusieurs façon d'organiser les données et les projets. Cependant, afin de simplifier les choses surtout au début, nous proposons de suivre les conseils suivants:

1. Créer un dossier `gis` dans notre dossier d'utilisateur. Sur Windows, c'est typiquement `C:\Users\xx\gis` où `xx` est votre nom d'utilisateur. Sur macOS, ce serait plutôt le chemin `/Users/xx/gis`, et sur Linux `/home/xx/gis`. Important: n'utilisez uniquement des noms en minuscules, sans caractères spéciaux comme des accents etc., et sans espaces. Si votre nom d'utilisateur contient un accent ou un espace, vous pouvez toujours créer votre dossier directement à la racine `C:\`, ou vous créer un nouvel utilisateur. Un nom d'utilisateur est idéalement très simple; il peut consister uniquement de vos initiales (en minuscules, donc p.ex. `ae` pour Albert Einstein).

2. À l'intérieur du dossier `gis`, vous créez un dossier `data`. Pour chaque jeu de données SIG que vous avez, vous allez créer un sous-dossier à l'intérieur de ce dossier. Donc pour le jeu de données de la Caroline du Nord, vous créez un dossier `nc` à l'intérieur de `data`. Ce sont les données que vous allez utiliser pour l'ensemble de vos projets SIG.

3. Pour chaque projet SIG que vous faites, vous créez un dossier dans `gis` (vous pouvez aussi faire un sous-dossier `projets` et créer un dossier par projet à l'intérieur si vous préférez). Dans chaque dossier de projet, vous créez à nouveau un dossier `data` avec les données spécifiques du projet, ensemble avec votre fichier de projet.

Ceci donne une structure qui ressemble à ça:

<img alt="Structure de dossiers et fichiers pour les SIG" src="assets/structure-projets-sig.png" style="border: 1px solid #aaa;" />

**Il est important de ne plus modifier cette structure une fois qu'elle a été mise en place!**
