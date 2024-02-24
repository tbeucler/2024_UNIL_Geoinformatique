# C'est la première fois que vous codez en Python ?
Cette section vous aidera à comprendre comment exécuter des scripts avec Python. Comme vous le savez peut-être déjà, Python est un langage _interprété_. Cela signifie que vous n'avez pas besoin de compiler le code avant de l'exécuter, mais cela a un inconvénient : vous devez avoir un environnement qui répond à toutes les exigences de votre script avant de pouvoir exécuter le code.

## Qu'est-ce que j'entends par environnement ?
Dans ce contexte, l'environnement fait référence à l'interpréteur Python de base, qui traduit le code que vous écrivez en Python en commandes que les ordinateurs peuvent comprendre et exécuter, ainsi qu'à toutes les autres bibliothèques et modules nécessaires (c'est-à-dire le code écrit par d'autres qui a été commodément partagé avec vous et qui rend généralement le codage plus simple). Ces bibliothèques vous permettent, par exemple, d'effectuer efficacement des opérations numériques (Numpy), de traiter efficacement les structures de données et les tâches d'analyse de données (Pandas), et même de mettre en œuvre des solutions d'apprentissage automatique de pointe (SciKit Learn, Tensorflow, PyTorch).

Aujourd'hui, nous allons examiner trois options pour exécuter du code Python :
1. Google Colaboratory (souvent abrégé en Colab)
> Colab est un service géré par Google, et vous donne un accès (limité) à leurs CPUs, GPUs, et même TPUs ! Colab est basé sur les carnets Jupyter, et est destiné à vous permettre d'écrire et d'exécuter du code Python à partir de votre navigateur gratuitement. De nombreuses bibliothèques d'apprentissage automatique sont installées et des API permettent d'interagir avec les services Google (par exemple, Drive). Colab exige toutefois que vous vous connectiez à l'aide d'un compte Google, ce que vous ne possédez peut-être pas ou ne souhaitez pas faire.
>> *Plusses* : Gratuit, Intégration avec les services Google, Intégration avec GitHub, *Nécessite aucune installation de votre part pour la plupart des tâches*.
>> *Minus* : Votre code sera stocké et exécuté sur les serveurs de Google, Nécessite l'utilisation d'un compte Google, Ressources limitées, Limité aux scripts interactifs
2. Binder
> Comme Colab, Binder est une plateforme en ligne qui vous permet d'écrire et d'exécuter du code Python à partir de votre navigateur. Contrairement à Colab, le projet Binder est une initiative *open-source* qui permet la création d'environnements informatiques personnalisés pour la science des données et le calcul scientifique interactifs et reproductibles. Grâce à lui, vous pouvez transformer des dépôts GitHub contenant des carnets Jupyter ou d'autres codes de science des données en environnements exécutables que d'autres peuvent lancer et avec lesquels ils peuvent interagir en ligne, sans qu'il soit nécessaire d'installer quoi que ce soit localement.
>> *Plusses* : Gratuit, Open Source, S'intègre à GitHub, *Ne nécessite aucune installation de votre part pour la plupart des tâches*, Prise en charge d'environnements complexes (y compris Docker)
*Minus* : Ressources limitées, complexité de l'installation pour les nouveaux utilisateurs, le temps de construction peut être long, votre code sera stocké et exécuté sur des serveurs externes, *vous ne pouvez pas sauvegarder les modifications apportées aux fichiers sur le serveur ; vous devez télécharger les fichiers*.
3. Conda (en utilisant Miniconda)  
> Conda est un gestionnaire de paquets qui vous permet de créer et de gérer des environnements pour Python et d'autres langages. C'est un outil très puissant, et c'est le moyen recommandé pour gérer vos environnements Python. Conda est disponible en deux versions : Anaconda et Miniconda. Anaconda est une distribution complète de Python, et est livré avec de nombreux paquets préinstallés. Miniconda, en revanche, est une version minimale d'Anaconda, et n'est livrée qu'avec le strict minimum pour vous permettre de démarrer. Nous utiliserons Miniconda aujourd'hui, car il est beaucoup plus léger et plus facile à installer. De plus, nous pouvons utiliser Conda avec une variété d'IDE (Integrated Development Environments), qui nous permettent d'écrire et d'exécuter du code Python à partir de nos ordinateurs.
>> *Plusses* : Gratuit, Open Source et Cross-Platform, *Permet de créer et de gérer vos propres environnements*, *Gère la compatibilité des dépendances des bibliothèques pour vos environnements*, Votre code sera stocké et exécuté sur l'ordinateur où Conda est installé (*Vous pouvez exécuter le code hors ligne*)
>> *Minus* : Complexité d'installation pour les nouveaux utilisateurs, *Nécessite l'installation de logiciels sur votre ordinateur*, *Nécessite la gestion de vos environnements*.

Voyons comment utiliser chacune de ces options.


## Google Colaboratory 🥼
Pour utiliser Colab, vous devez disposer d'un compte Google. Si vous n'en avez pas, vous pouvez en créer un [ici](https://accounts.google.com/signup/v2/webcreateaccount?flowName=GlifWebSignIn&flowEntry=SignUp). Une fois que vous avez un compte, vous pouvez accéder à Colab [ici](https://colab.research.google.com/). Vous devriez voir un écran comme celui-ci :  
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Colab_Screens/Opening_Colab.png?raw=true' width=50%>

À partir de cette page, vous pouvez ouvrir un nouveau carnet en cliquant sur "Nouveau carnet" ou en cliquant sur "Fichier" puis sur "Nouveau carnet". Vous devriez alors voir un écran comme celui-ci :  
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Colab_Screens/Colab_New_Notebook.png?raw=true' width=50%>

Vous pouvez maintenant écrire et exécuter du code Python dans ce carnet.Pour exécuter une cellule, vous pouvez soit cliquer sur le bouton 'play' à gauche de la cellule, soit appuyer sur 'Shift+Enter' sur votre clavier. Essayez-le en copiant le texte suivant dans une cellule et en exécutant le code :  
```python
print('Voici la liste de tous les paquets installés dans cet environnement:')
!pip list
```

C'est bien, mais ce qui nous intéresse le plus aujourd'hui, c'est de pouvoir exécuter des tutoriels hébergés sur GitHub. Il y a plusieurs façons de le faire,
1. Si le notebook jupyter est hébergé sur GitHub et a été téléchargé via l'interface Colab, vous pouvez simplement cliquer sur le bouton "Open in Colab" en haut de la page.
><img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Colab_Screens/open_in_colab.png?raw=true' width=10%> <br>
>Cela ouvrira le carnet dans Colab, et vous pourrez alors exécuter le code comme vous le feriez normalement. Vous pouvez trouver un exemple de ceci [ici] (https://github.com/msgomez06/ML_pedagogical_materials/blob/main/Labs/S2_1_Classification.ipynb). Ce notebook fait partie d'une série de documents développés pour un cours sur l'apprentissage automatique donné à l'UNIL, et est hébergé sur GitHub.

2. Si le notebook est hébergé sur GitHub, mais n'a pas été téléchargé via l'interface Colab, vous pouvez utiliser le motif URL afin de l'ouvrir sur Colab.  
À titre d'exemple, nous utiliserons les carnets développés par Jesper Dramsch pour le tutoriel EuroSciPy 2022 [Machine Learning for Science Reproducibility] (https://github.com/JesperDramsch/ml-for-science-reproducibility-tutorial/tree/main). Bien que les documents aient été préparés pour être ouverts avec Colab et Binder (comme en témoignent les widgets _open on_ dans le Readme.md principal), faisons comme s'ils ne l'étaient pas et [visualisons le premier carnet sur GitHub](https://github.com/JesperDramsch/ml-for-science-reproducibility-tutorial/blob/main/book/notebooks/0-basic-data-prep-and-model.ipynb). Lorsque vous visualisez le carnet hébergé dans votre navigateur, vous devriez voir que l'URL est
`https://github.com/JesperDramsch/ml-for-science-reproducibility-tutorial/blob/main/book/notebooks/0-basic-data-prep-and-model.ipynb`. 
Pour ouvrir ce carnet dans Colab, vous devez remplacer `github.com` par `colab.research.google.com/github`.
L'URL résultante doit être  
`https://colab.research.google.com/github/JesperDramsch/ml-for-science-reproducibility-tutorial/blob/main/book/notebooks/0-basic-data-prep-and-model.ipynb`  
Si vous ouvrez cette URL, vous devriez voir le notebook ouvert dans Colab, et vous pouvez exécuter le code comme vous le feriez normalement.
Essayez-le par vous-même avec le carnet de notes suivant :
`https://github.com/JesperDramsch/ml-for-science-reproducibility-tutorial/blob/main/book/notebooks/1-model-evaluation.ipynb`

3. Vous pouvez également utiliser la commande `Open Notebook` de Colab dans le menu fichier, qui vous permettra de rechercher des dépôts GitHub par utilisateur, comme le montre la capture d'écran ci-dessous.  
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Colab_Screens/open_from_github.png?raw=true' width=50%> <br>



## Binder 📒
Binder est un peu plus compliqué à utiliser que Colab, mais il est aussi plus puissant. Nous n'entrerons pas dans les détails de la création d'un environnement Binder, mais nous verrons comment l'utiliser.

Commençons par ouvrir l'environnement Binder pour le tutoriel EuroSciPy 2022 [Machine Learning for Science Reproducibility] (https://mybinder.org/v2/gh/JesperDramsch/ml-for-science-reproducibility-tutorial/HEAD). Vous devriez voir un écran comme celui-ci :
<img src='Binder_screens\binder_loading.png?raw=true' width=50%> <br>
Cet écran indique que Binder est en train de construire l'environnement pour vous.  
Cela peut prendre un certain temps, alors soyez patient.  
Une fois l'environnement construit, vous devriez voir un écran comme celui-ci :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Binder_screens\binder_jplab.png?raw=true' width=50%> <br>
Contrairement à Colab, Binder lance une instance complète de JupyterLab et pas seulement l'interface du carnet de notes. Cela vous permet d'ouvrir et d'éditer plusieurs carnets en même temps, et même d'ouvrir d'autres fichiers (par exemple, des images, des fichiers texte, etc.) ! Vous pouvez utiliser l'explorateur de fichiers sur le plan gauche pour parcourir le contenu du référentiel, et vous pouvez ouvrir un carnet en double-cliquant dessus. Voici le premier cahier du référentiel, `0-basic-data-prep-and-model.ipynb` :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Binder_screens\binder_notebook.png?raw=true' width=50%> <br>
Notez que si vous voulez exécuter ce bloc-notes, au moment de l'écriture, vous devez changer la ligne  
`DATA_FOLDER = Path("...") / "data"`  
en  
`DATA_FOLDER = Path("../...") / "data"`

<br><br>

## Conda (en utilisant Miniconda) 🐍

Conda est une solution beaucoup plus flexible pour exécuter du code Python, mais elle nécessite l'installation d'un logiciel sur votre ordinateur. Dans ce tutoriel, nous allons voir comment installer Miniconda sur Windows et Linux (toutes mes excuses à ceux qui utilisent OSX - je n'ai pas accès à un Mac, je ne peux donc pas vous fournir le même niveau d'instructions - cela devrait cependant être assez similaire).

Avant d'entamer l'installation, passons en revue quelques termes de base :

### Terminologie
- **Package** : Un paquet est une collection de code qui peut être installée et utilisée en Python. Les paquets peuvent être installés à partir d'une variété de sources, y compris le Python Package Index (PyPI), Anaconda Cloud, et Conda-Forge. Les paquets peuvent être installés en utilisant la commande `conda`, ou en utilisant `pip` (l'installateur de paquets Python). Nous nous appuierons sur `conda`, car il s'assure que toutes les dépendances d'un paquet sont également installées (et vérifie les conflits entre les paquets)
- **Environnement virtuel** : Comme nous l'avons mentionné précédemment, un environnement est un ensemble de paquets installés à un endroit spécifique. Les environnements Python contiennent tous les logiciels nécessaires à l'interprétation du code et à l'exécution des scripts Python. Les environnements virtuels sont utiles car ils vous permettent d'avoir différentes versions de paquets installées dans différents environnements, et ils vous permettent de partager facilement votre environnement avec d'autres. Les environnements peuvent être créés à l'aide de la commande `conda`, ou à l'aide de `pipenv` (l'environnement d'installation des paquets Python).
- **Canal** : Un canal est une source de paquets. Le canal par défaut est le canal Anaconda, qui contient les paquets testés par l'équipe Anaconda. Les autres canaux incluent Conda-Forge, qui contient les paquets qui ont été testés par l'équipe Conda-Forge, et PyPI, qui contient les paquets qui ont été téléchargés par la communauté. Les canaux peuvent être spécifiés lors de l'installation de paquets en utilisant la commande `conda`.

### Installation de Miniconda
Pour installer Miniconda, vous devez télécharger le programme d'installation correspondant à votre système d'exploitation à partir d'[ici] (https://docs.conda.io/en/latest/miniconda.html). Une fois que vous avez téléchargé le programme d'installation, vous pouvez l'exécuter pour installer Miniconda. Pour passer aux instructions pour Linux, cliquez [ici] (#linux-🐧). Pour passer aux instructions pour Windows. Les instructions pour Windows se trouvent juste en dessous.
<br>

#### Windows 🗔
Une fois que vous avez téléchargé le programme d'installation, exécutez-le et suivez les instructions avec les paramètres par défaut. Vous devriez maintenant avoir un programme appelé `Anaconda Prompt` et `Anaconda Powershell Primpt` installé sur votre ordinateur. Ces programmes vous permettent d'exécuter des commandes dans un terminal avec l'environnement correct activé - commençons par ouvrir 'Anaconda Powershell Prompt'. Vous devriez voir un écran comme celui-ci :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Conda_screens/anaconda_powershell_prompt.png?raw=true' width=50%> <br>
Remarquez le `(base)` au début de la ligne - cela indique que l'environnement `base` est actuellement actif. Créons un nouvel environnement appelé `test_env` en exécutant la commande suivante :
```bash
conda create -n test_env
```
On vous demandera de confirmer l'installation du nouvel environnement en tapant `y` et en appuyant sur `Enter`. Une fois l'environnement créé, vous devriez voir un écran comme celui-ci :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Conda_screens/create_env.png?raw=true' width=50%> <br>
Si vous lancez la commande `conda env list`, vous devriez maintenant voir les environnements `base` et `test_env` listés. Allons-y et activons l'environnement `test_env` en lançant la commande suivante :
```bash
conda activate test_env
```
Si vous lancez `conda list`, vous obtiendrez une liste des paquets installés sur l'environnement virtuel. Pour le moment, cette liste est vide ! (Après tout, nous venons de créer un environnement virtuel vierge).
Installons ipython, abréviation de interactive python, qui nous permettra d'exécuter du code Python de manière interactive. Pour ce faire, nous allons exécuter la commande suivante :
```bash
conda install ipython
```
Conda va générer une liste de paquets qui seront installés, et vous demandera de confirmer l'installation en tapant `y` et en appuyant sur `Enter`. Une fois l'installation terminée, vous devriez voir un écran comme celui-ci :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Conda_screens/ipython_install.png?raw=true' width=50%> <br>
Tapez maintenant `ipython` et appuyez sur `Enter`. Vous devriez voir un écran comme celui-ci :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Conda_screens/ipython.png?raw=true' width=50%> <br>
Essayez d'exécuter un petit programme qui imprime les nombres de 0 à 9 :
```python	
[print(number) for number in range(10)]
```
L'écran suivant devrait s'afficher :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Conda_screens/ipython_example.png?raw=true' width=50%> <br>
Une fois que vous avez terminé avec ipython, tapez simplement `exit()` et appuyez sur `Enter` pour quitter le programme.
Installons maintenant quelques paquets couramment utilisés. Pour ce faire, nous allons utiliser un canal différent de celui par défaut. Ajoutez simplement `-c conda-forge` comme option à la commande install, comme montré ci-dessous :  
```bash
conda install -c conda-forge numpy pandas matplotlib
```
Félicitations, vous avez un environnement Python fonctionnel ! Nous verrons comment installer les IDE dans la section suivante ; sautez la section Linux pour l'instant.

<br><br>

#### Linux 🐧
Après avoir téléchargé le programme d'installation, ouvrez un terminal et naviguez jusqu'au répertoire où vous avez téléchargé le programme d'installation. En supposant que vous avez utilisé Firefox, la commande par défaut pour vous emmener dans le répertoire où se trouve l'installateur est :
```bash
cd ~/Downloads
```
Une fois que vous êtes dans le bon répertoire, exécutez la commande suivante pour rendre le programme d'installation exécutable :
```bash
chmod +x Miniconda3-latest-Linux-x86_64.sh
```
Ensuite, exécutez le programme d'installation :
```bash
bash Miniconda3-latest-Linux-x86_64.sh
```
Vous serez invité à accepter le contrat de licence. Appuyez sur `Space` pour faire défiler le contrat de licence, puis tapez `oui` et appuyez sur `Enter` pour accepter le contrat de licence. Il vous sera ensuite demandé de confirmer l'emplacement d'installation. Appuyez sur `Enter` pour accepter l'emplacement par défaut. On vous demandera alors si vous voulez initialiser Miniconda3 en lançant `conda init`. Tapez `oui` et appuyez sur `Enter` pour accepter. Redémarrez votre terminal, et vous devriez maintenant voir `(base)` à côté du prompt. Cela indique que l'environnement `base` est actuellement actif :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Conda_screens/linux_conda_init.png?raw=true' width=50%> <br>
Créons un nouvel environnement appelé `test_env` en exécutant la commande suivante :
```bash
conda create -n test_env
```
On vous demandera de confirmer l'installation du nouvel environnement en tapant `y` et en appuyant sur `Enter`. Une fois l'environnement créé, vous devriez voir un écran comme celui-ci :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Conda_screens/linux_create_env.png?raw=true' width=50%> <br>
Si vous lancez la commande `conda env list`, vous devriez maintenant voir les environnements `base` et `test_env` listés. Allons-y et activons l'environnement `test_env` en lançant la commande suivante :
```bash
conda activate test_env
```
Si vous lancez `conda list`, vous obtiendrez une liste des paquets installés sur l'environnement virtuel. Pour le moment, cette liste est vide ! (Après tout, nous venons de créer un environnement virtuel vierge).
Installons ipython, abréviation de interactive python, qui nous permettra d'exécuter du code Python de manière interactive. Pour ce faire, nous allons lancer la commande suivante :
```bash
conda install ipython
```
Conda va générer une liste de paquets qui seront installés, et vous demandera de confirmer l'installation en tapant `y` et en appuyant sur `Enter`. Une fois l'installation terminée, vous devriez voir un écran comme celui-ci :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Conda_screens/linux_ipython_install.png?raw=true' width=50%> <br>
Tapez maintenant `ipython` et appuyez sur `Enter`. Vous devriez voir un écran comme celui-ci :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Conda_screens/linux_ipython.png?raw=true' width=50%> <br>
Essayez d'exécuter un petit programme qui imprime les nombres de 0 à 9 :
```python	
[print(number) for number in range(10)]
```
L'écran suivant devrait s'afficher :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Conda_screens/linux_ipython_example.png?raw=true' width=50%> <br>
Une fois que vous avez terminé avec ipython, tapez simplement `exit()` et appuyez sur `Enter` pour quitter le programme.
Installons maintenant quelques paquets couramment utilisés. Pour ce faire, nous allons utiliser un canal différent de celui par défaut. Ajoutez simplement `-c conda-forge` comme option à la commande install, comme montré ci-dessous :  
```bash
conda install -c conda-forge numpy pandas matplotlib
```
Félicitations, vous avez un environnement Python fonctionnel ! Nous verrons comment installer les IDE dans la section suivante.
<br>


### Integrated Development Environments (IDEs)
-----

Les IDE sont des logiciels qui vous fournissent des outils pour écrire du code. S'il est vrai que vous pouvez écrire vos programmes dans n'importe quel éditeur de texte, vous rencontrerez rapidement des problèmes - avez-vous tout écrit correctement ? Quels arguments la fonction "my_function" a-t-elle pris à nouveau ? Quelle partie de votre code a fait échouer votre script ? Quelle est la valeur actuelle de `ma_variable` ? Les IDE peuvent aider à répondre à ces questions et à bien d'autres.

Aujourd'hui, nous allons examiner trois IDE : Jupyter, Spyder et Visual Studio Code (VScode). Jupyter est un IDE basé sur le web qui vous permet d'écrire et d'exécuter du code dans un navigateur web. Spyder est un IDE de bureau qui vous permet d'écrire et d'exécuter du code dans une seule fenêtre. VScode est un IDE de bureau qui vous permet d'écrire et d'exécuter du code dans une seule fenêtre, et qui vous fournit également une variété d'outils pour déboguer et gérer votre code (y compris des plugins pour GitHub Copilot - un assistant d'intelligence artificielle qui est gratuit pour les étudiants - au moment de la rédaction, du moins).
<br><br>

#### Jupyter Notebook 📓
Nous utiliserons Jupyter Notebook pour ce tutoriel, mais il existe également une interface JupyterLab qui est plus similaire à Spyder et VScode. Pour installer Jupyter, il suffit de lancer la commande suivante :
```bash
conda install -c conda-forge jupyter
```

*C'EST ÇA !*
Vous avez maintenant un environnement Python fonctionnel avec Jupyter installé ! Pour lancer Jupyter, il suffit de lancer la commande suivante :
```bash
jupyter notebook
```
L'écran suivant devrait s'afficher :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Conda_screens/jupyter.png?raw=true' width=50%> <br>
Vous pouvez maintenant naviguer jusqu'à l'endroit où vous avez stocké vos carnets et les ouvrir. Vous pouvez également créer de nouveaux carnets en cliquant sur le bouton "Nouveau" dans le coin supérieur droit de l'écran.
Pour la documentation sur Jupyter Notebook, veuillez vous référer à la [documentation officielle](https://jupyter-notebook.readthedocs.io/en/stable/).
<br><br>

#### Jupyter Lab 🧪
Si vous préférez l'interface JupyterLab, vous pouvez l'installer en exécutant la commande suivante :
```bash
conda install -c conda-forge jupyterlab
```
Vous pouvez ensuite lancer JupyterLab en exécutant la commande suivante :
```bash
jupyter lab
```
L'écran suivant devrait s'afficher :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Conda_screens/jupyterlab.png?raw=true' width=50%> <br>
Vous pouvez maintenant naviguer jusqu'à l'endroit où vous avez stocké vos carnets de notes et les ouvrir. À partir du lanceur, vous pouvez créer un nouveau carnet Jupyter (et vous pouvez ouvrir d'autres lancements en cliquant sur le bouton + dans le coin supérieur gauche de l'écran).
Pour la documentation sur JupyterLab, veuillez vous référer à la [documentation officielle] (https://jupyterlab.readthedocs.io/en/stable/).
<br><br>

#### Spyder 🕷️
Spyder est un IDE de bureau qui vous permet d'écrire et d'exécuter du code dans une seule fenêtre. (Si vous êtes curieux, c'est l'abréviation de **S**cientific **Py**thon **De**velopment Envi**R**onment) Pour installer Spyder, exécutez simplement la commande suivante :
```bash
conda install -c conda-forge spyder
```
Cependant, Spyder n'est pas configuré par défaut pour exécuter les Notebooks Jupyter, nous devrons donc installer quelques paquets supplémentaires. Après tout, nous travaillerons principalement avec des carnets Jupyter. (Bien que vous puissiez faire tout ce qui est fait dans le cours avec des scripts à la place !) Pour installer les paquets nécessaires, exécutez la commande suivante :
```bash
conda install -c conda-forge spyder-notebook
```
Démarrons Spyder en exécutant la commande suivante :
```bash
spyder
```
L'écran suivant devrait s'afficher :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Conda_screens/spyder.png?raw=true' width=50%> <br>
Spyder ouvrira un fichier script temporaire au lancement (`temp.py`). Vous remarquerez qu'il y a deux onglets en bas de l'écran : `Editeur` et `Notebook`. Cliquez sur l'onglet `Notebook` pour ouvrir l'interface du notebook. Vous devriez voir un écran comme celui-ci :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Conda_screens/spyder-notebook.png?raw=true' width=50%> <br>
À partir de cet écran, vous pouvez créer des Notebooks Jupyter et ouvrir ceux qui existent déjà. Félicitations, vous avez maintenant un environnement Python fonctionnel avec Spyder installé ! 😃
Pour la documentation sur Spyder, veuillez vous référer à la [documentation officielle] (https://docs.spyder-ide.org/). Pour la documentation sur Spyder-Notebook, veuillez vous référer à la [documentation officielle](https://docs.spyder-ide.org/current/plugins/notebook.html).
<br><br>

#### Visual Studio Code (VScode) 🆚
VScode est un puissant environnement de développement intégré (IDE) de bureau qui vous permet d'écrire et d'exécuter du code dans une seule fenêtre. Il vous offre également une variété d'outils pour le débogage et la gestion de votre code (y compris des plugins pour GitHub Copilot - un assistant IA gratuit pour les étudiants - au moment de la rédaction, du moins). Pour installer VScode, vous devrez télécharger l'installateur depuis [the VScode website](https://code.visualstudio.com/download) et l'exécuter.

Sur Windows, lancez simplement l'installateur. Sur Linux, accédez au répertoire où vous avez téléchargé l'installateur et exécutez la commande suivante :
```bash
sudo dpkg -i code_1.60.2-1632313585_amd64.deb
```

Une fois que vous avez installé VScode, lancez-le (en cliquant sur l'icône appropriée sur Windows ou en exécutant `code` dans un terminal sur Linux). Vous devriez voir un écran comme celui-ci :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Conda_screens/vscode_start.png?raw=true' width=50%> <br>

À gauche, vous verrez une icône qui ressemble à un ensemble de 3 blocs sur le point d'être rejoints par un quatrième bloc. Cliquez dessus pour ouvrir le menu des extensions. Recherchez `Python` et installez le premier résultat. Vous devriez voir un écran comme celui-ci :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Conda_screens/vscode_python.png?raw=true' width=50%> <br>

Allez-y et installez l'extension Jupyter par vous-même 😃.

Maintenant que vous avez installé les deux, cliquez sur l'icône `Explorer` à gauche - elle ressemble à deux fichiers empilés l'un sur l'autre. Vous devriez voir un écran comme celui-ci :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Conda_screens/vscode_explorer.png?raw=true' width=50%> <br>

Cliquez sur le bouton `Ouvrir un dossier`, puis naviguez jusqu'au dossier où vous avez stocké vos notebooks. Sélectionnez le dossier et cliquez sur `Ouvrir`. Vous devriez voir un écran comme celui-ci :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Conda_screens/vscode_folder.png?raw=true' width=50%> <br>

Allons-y et commençons un nouveau notebook. Cliquez sur le bouton `Nouveau fichier` en haut à gauche de l'écran, et saisissez `test.ipynb`. Vous devriez voir un écran comme celui-ci :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Conda_screens/new_jupyter_notebook.png?raw=true' width=50%> <br>

Vous devriez voir 'sélectionner le noyau' en haut à droite de l'écran - cliquez dessus, choisissez Python Environment dans la fenêtre contextuelle, et sélectionnez votre environnement virtuel (par exemple, test_env) dans la liste.
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Conda_screens/vscode_select_kernel.png?raw=true' width=50%> <br>
Essayez d'importer une bibliothèque (vous pourriez être invité par VScode à installer certains fichiers requis pour l'exécution interactive des notebooks Jupyter - allez-y et acceptez cette invitation).
Félicitations - vous pouvez maintenant exécuter des notebooks Jupyter depuis VScode ! 😃

Pour la documentation sur VScode, veuillez vous référer à la [documentation officielle](https://code.visualstudio.com/docs).

<br><br>

### Utilisation de Git et GitHub
-----

Git est un système de contrôle de version qui vous permet de suivre les modifications apportées à votre code. GitHub est un service qui vous permet de stocker votre code en ligne et qui vous offre une variété d'outils pour collaborer avec d'autres personnes. Nous n'aborderons pas l'utilisation de Git et GitHub dans ce tutoriel, mais nous verrons comment installer Git et comment cloner un dépôt depuis GitHub. De plus, nous examinerons comment utiliser les outils Git intégrés dans VScode. Enfin, nous discuterons de la configuration de Github Copilot dans VScode 🤖.

<br>

#### Installation de Git sur Windows
Pour installer Git sur Windows, vous devrez télécharger l'installateur depuis [le site web de Git](https://git-scm.com/download/win) et l'exécuter - laissez toutes les options par défaut cochées. Une fois Git installé, vous pouvez ouvrir un terminal (par exemple, Powershell) et exécuter la commande suivante pour vérifier qu'il est correctement installé :
```bash
git --version
```
 <br>

 #### Installation de Git sur Linux
Pour installer Git sur Linux, exécutez simplement les commandes suivantes :
```bash
sudo apt-get update
sudo apt install git
```
Répondez par `y` lorsque vous êtes invité à confirmer l'installation. Une fois Git installé, vous pouvez ouvrir un terminal et exécuter la commande suivante pour vérifier qu'il est correctement installé :
```bash
git --version
```

<br><br>

#### Configurer votre compte GitHub
Vous n'avez pas besoin de créer un compte sur GitHub pour cloner un dépôt, mais vous en aurez besoin si vous souhaitez pousser des modifications vers un dépôt. Pour créer un compte, rendez-vous sur [la section d'inscription du site web de GitHub](https://github.com/signup). On vous demandera d'entrer votre adresse e-mail (RAPPELEZ-VOUS D'UTILISER VOTRE ADRESSE E-MAIL ACADÉMIQUE SI VOUS PRÉVOYEZ DE DEMANDER DES AVANTAGES ÉTUDIANTS/ENSEIGNANTS) sur l'écran suivant :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Git/github_signup.png?raw=true' width=50%> <br>
Suivez les invitations pour créer votre compte, puis vérifiez votre adresse e-mail. Vous serez ensuite invité à indiquer vos préférences - si vous êtes étudiant ou enseignant, vous pouvez demander des avantages associés à votre statut dans ce processus.
Une fois cela fait, passons à la configuration d'une clé SSH. Les clés SSH sont une manière d'identifier les ordinateurs de confiance, sans utiliser de mots de passe. Vous devrez configurer cela pour téléverser des modifications vers GitHub - *l'authentification par mot de passe n'est plus prise en charge* 🙅.

##### Configuration d'une clé SSH sur Linux
Pour configurer une clé SSH sur Linux, vous devrez
1. Ouvrir un terminal et exécuter la commande suivante :
```bash
ssh-keygen -t ed25519
```
On vous demandera d'entrer un fichier dans lequel sauvegarder la clé. Appuyez sur `Enter` pour accepter l'emplacement par défaut. On vous demandera ensuite d'entrer une phrase secrète. Vous pouvez entrer une phrase secrète ou laisser le champ vide. Si vous le laissez vide, on vous demandera de confirmer que vous souhaitez le laisser vide - dans notre cas, nous le laisserons vide (*NOTEZ QUE CECI EST MOINS SÉCURISÉ*). Une fois cela fait, vous devriez voir un écran comme celui-ci :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Git/linux_ssh_keygen.png?raw=true' width=50%> <br>

2. Vous pouvez maintenant afficher votre clé SSH en exécutant la commande suivante, après quoi vous devriez copier la clé dans votre presse-papiers :
```bash
cat ~/.ssh/id_ed25519.pub
```

3. Maintenant, allez dans [vos paramètres GitHub](https://github.com/settings/profile)
4. Cliquez sur `SSH and GPG keys` du côté gauche de l'écran
5. Cliquez sur `New SSH key`
6. Donnez un titre à votre clé (par exemple: `My SSH Key`)
7. Collez votre clé dans le champ `Key``
8. Cliquez sur `Add SSH key`


>>Votre clé SSH devrait maintenant apparaître dans la liste des clés SSH (SSH-keys) de vos paramètres GitHub, similaire à la capture d'écran ci-dessous :
><img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Git/linux_github_ssh_key.png?raw=true' width=50%> <br>
<br><br>

##### Configuration d'une clé SSH sur Windows
Pour configurer une clé SSH sur Windows, **après avoir installé Git*, vous devrez :
1. Ouvrez le menu Démarrer et recherchez `Powershell`. Faites un clic droit sur l'icône et sélectionnez `Run as administrator`.
2. Activez le ssh-agent en exécutant la commande suivante :
```bash
Get-Service ssh-agent | Set-Service -StartupType Automatic -PassThru | Start-Service
```
3. Exécutez la commande suivante pour démarrer le ssh-agent sans redémarrer votre ordinateur :
```bash
start-ssh-agent.cmd
```
4. Exécutez la commande suivante pour générer une clé SSH :
```bash
ssh-keygen -t ed25519
```
>On vous demandera d'entrer un fichier dans lequel sauvegarder la clé. Appuyez sur `Enter` pour accepter l'emplacement par défaut. On vous demandera ensuite d'entrer une phrase secrète. Vous pouvez entrer une phrase secrète ou laisser le champ vide. Si vous le laissez vide, on vous demandera de confirmer que vous souhaitez le laisser vide - dans notre cas, nous le laisserons vide (*NOTEZ QUE CECI EST MOINS SÉCURISÉ*). Une fois cela fait, vous devriez voir un écran comme celui-ci :
><img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Git/windows_ssh_keygen.png?raw=true' width=50%> <br>
5. Naviguez vers le répertoire où vous avez enregistré votre clé SSH (par exemple, `C:\Users\nom_utilisateur\.ssh\id_ed25519.pub`) et ouvrez le fichier dans un éditeur de texte (par exemple, Notepad). Copiez le contenu du fichier dans votre presse-papiers. Vous devriez voir quelque chose comme ceci :
><img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Git/windows_ssh_key.png?raw=true' width=50%> <br>
6. Allez dans [vos paramètres GitHub](https://github.com/settings/profile)
7. Cliquez sur `SSH and GPG keys` du côté gauche de l'écran
8. Cliquez sur `New SSH key`
9. Donnez un titre à votre clé (par exemple, `My SSH Windows Key`)
10. Collez votre clé dans le champ `Key`
11. Cliquez sur `Add SSH key`

>Votre clé SSH devrait maintenant apparaître dans la liste des clés SSH de vos paramètres GitHub, similaire à la capture d'écran ci-dessous : 
><img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Git/windows_ssh_github.png?raw=true' width=50%> <br>

<br><br>

#### Cloner un dépôt GitHub
Vous devriez maintenant être en mesure de cloner des dépôts depuis GitHub ! Allons-y et clonons le dépôt pour le tutoriel EuroSciPy 2022 [Machine Learning for Science Reproducibility](https://github.com/JesperDramsch/ml-for-science-reproducibility-tutorial/tree/main). Ouvrez le dépôt dans votre navigateur, cliquez sur le bouton `Code`, puis sur l'onglet SSH. Vous devriez voir un écran comme celui-ci :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Git/clone_code.png?raw=true' width=50%> <br>

Ouvrez un terminal et naviguez vers le répertoire où vous souhaitez cloner le dépôt. Ensuite, exécutez la commande suivante :
```bash
git clone git@github.com:JesperDramsch/ml-for-science-reproducibility-tutorial.git
```
Si c'est la première fois que vous clonez un dépôt, on vous demandera de confirmer que vous souhaitez vous connecter à l'hôte. Tapez `yes` et appuyez sur `Enter` pour confirmer. Vous devriez voir un écran comme celui-ci :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Git/win_repo_clone.png?raw=true' width=50%> <br>
Et si vous naviguez vers le répertoire où vous avez cloné le dépôt, vous devriez voir un dossier avec le nom du dépôt, comme indiqué ci-dessous :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Git/win_after_cloning.png?raw=true' width=50%> <br>

Vous pouvez maintenant ouvrir le dépôt dans votre IDE préféré et commencer à travailler dessus ! 😃

<br><br>

#### Utilisation de Git dans VScode
VScode dispose d'une interface Git intégrée qui vous permet de gérer vos dépôts. Allons-y et ouvrons le dépôt que nous venons de cloner dans VScode. Ouvrez VScode, et cliquez sur l'icône `Explorer` à gauche - elle ressemble à deux fichiers empilés l'un sur l'autre. Vous devriez voir un écran comme celui-ci :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Git/vscode_with_cloned.png?raw=true' width=50%> <br>
Si vous cliquez maintenant sur l'icône Contrôle de source (celle qui ressemble à un ensemble de cercles reliés par des fils), vous devriez voir un écran comme celui-ci (notez que vous devrez peut-être cliquer sur le bouton "Trust the authors" (Gérer les dépôts non sécurisés) et sélectionner "Faire confiance aux auteurs" pour gérer le dépôt - après tout, il s'agit d'un dépôt que vous avez cloné depuis Internet à partir d'un utilisateur que vous ne connaissez pas) :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Git/vscode_source_control.png?raw=true' width=50%> <br>
Chaque fois que vous apportez des modifications à votre dépôt, vous pourrez pousser et tirer les modifications en utilisant les boutons en haut de l'écran. Vous pouvez également utiliser les boutons `+` et `...` pour mettre en scène et valider les modifications.

NOUS N'ABORDERONS PAS L'UTILISATION DE GIT DANS CE TUTORIEL, mais vous pouvez trouver la documentation [ici](https://code.visualstudio.com/docs/editor/versioncontrol).
De plus, veuillez ne pas essayer de pousser des modifications vers le dépôt que nous avons cloné - il ne vous appartient pas et vous n'avez pas l'autorisation de le faire. J'aimerais aussi éviter de charger le propriétaire du dépôt avec une multitude de demandes de fusion de personnes qui essaient simplement d'apprendre à utiliser Git 😅.
<br><br>

#### Configuration de GitHub Copilot dans VScode

Tout d'abord, ouvrez les paramètres de votre compte GitHub - vous devriez voir un écran comme celui-ci :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Git/github_settings.png?raw=true' width=50%> <br>
Dans la colonne de gauche, vous devriez voir un lien vers `Copilot` sous la catégorie `Code`, `Planning`, and `Automation`. Si vous avez un compte étudiant, vous devriez pouvoir l'activer gratuitement tant que vous vous êtes abonné à _Github Global Campus_ lors de la configuration de votre compte. (Alternativement, vous pouvez vous y abonner maintenant en [suivant ce lien](https://education.github.com/discount_requests/application)) Si vous n'êtes pas étudiant, vous pouvez toujours l'essayer gratuitement avec un essai, et au moment de la rédaction, l'abonnement coûte 10 $ par mois.

Une fois votre licence de Copilot activée, ouvrez VSCode et accédez à l'onglet des extensions. Recherchez `Copilot` et installez le premier résultat. Vous devriez voir un écran comme celui-ci :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Git/vscode_copilot_signin.png?raw=true' width=50%> <br>
À gauche, vous devriez voir une icône d'utilisateur avec un point vert à côté. Cliquez dessus et sélectionnez l'option `sign in Github to use Github Copilot`. Cela vous redirigera vers un écran d'autorisation qui ressemblera à ceci :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Git/authorize_vscode.png?raw=true' width=50%> <br>

Acceptez toutes les invitations qui apparaissent, et vous devriez être prêt ! 😃
Maintenant, chaque fois que vous tapez dans un document dans VSCode, vous devriez voir des suggestions de Copilot apparaître. Vous pouvez accepter ces suggestions en appuyant sur `Tab`.

Enfin, vous pouvez vous inscrire à la bêta de GitHub Copilot Chat ici(https://github.com/github-copilot/chat_waitlist_signup/join) si cela vous intéresse. L'interface de chat vous offre un moyen pratique d'interagir avec Copilot - par exemple, voici une brève conversation demandant à Copilot de créer un modèle LDA (analyse discriminante linéaire) qui s'adapte à 5 caractéristiques générées de manière aléatoire :
<img src='https://github.com/tbeucler/2023_MLEES_JB/blob/5ed5b4cd553f414f01f4207ffb0523bfa1a93afc/ML_EES/Milton/Git/5-feature_LDA.png?raw=true' width=50%> <br>
Notez que Copilot peut gérer des demandes en langage naturel, même avec des fautes d'orthographe ! 😝 
Le texte complet du code est :
```python
from sklearn.datasets import make_classification
from sklearn.discriminant_analysis import LinearDiscriminantAnalysis

# Générer un ensemble de données aléatoires avec 5 features (caractéristiques)
X, y = make_classification(n_samples=100, n_features=5, n_informative=3, n_redundant=0, n_classes=2, random_state=42)

# Fit (ajuster) le modèle LDA au jeu de données
lda = LinearDiscriminantAnalysis()
lda.fit(X, y)
```