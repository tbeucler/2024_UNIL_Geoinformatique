# Tutoriel 11 - Analyse spatiale I (B)

Dans cette section, nous aborderons les points suivants:

- Calculatrice raster = Reclasser les valeurs d’un raster??
- Automatisaton (model builder) 

# Calculatrice raster

Un outil très puissant, qui peut réaliser en une seule formule l’équivalent de plusieurs traitements successifs.
Toujours un raster en sortie, un ou plusieurs raster(s) en entrée. Important : la formule est appliquée sur chaque pixel pour en changer la valeur.
![](assets/)

Les opérateurs
![](assets/)

Possible de combiner plusieurs raster, avec des opérateurs mathématiques ou logiques (ici : AND)
![](assets/)
Possible d’utiliser une clause conditionnelle :
Cons( « expression à vérifier », « valeur si vrai », « valeur si faux »)
et d’en imbriquer plusieurs.
![](assets/)

# Automatisation

POUR BOUCLER LA BOUCLE... Géomatique = Géographie + Informatique
«La géomatique regroupe l'ensemble des outils et méthodes permettant d'acquérir, de représenter, d'analyser et d'intégrer des données géographiques. La géomatique consiste donc en au moins trois activités distinctes : collecte, traitement et diffusion des données géographiques».
L’informatique permet non seulement d’appliquer des géotraitements, mais également de le faire automatiquement.

## Pourquoi automatiser ?
-> **Reproductibilité** des analyses 
-> **Mise à jour** des données
-> **Réduction** du nombre **d’opérations manuelles** (donc diminution du risque d’erreur et gain de temps)

L’automatisation se base sur une **programmation des géotraitements** qui peut prendre plusieurs formes :
- Partielle (répétition d’un unique traitement) : exécution par lots (batch)
- Via des lignes de code : langage Python 
- Via une interface visuelle : ModelBuilder
![](assets/)

Des données toujours à jour ! - données officielles, base de décision 
*Exemple public : le cadastre des restrictions de droit public à la propriété foncière (RDPPF), plus de 700’000 requêtes par an.*
![](assets/)
Des rapports réguliers,
permettant comparaison et
monitoring.
*Exemple public : l’annuaire hydrologique Suisse. Données annuelles sur le débit, la température, et la qualité des eaux.*
![](assets/)
source : https://www.bafu.admin.ch/bafu/fr/home/themes/eaux/publications/publications-eaux/ annuaire-hydrologique.html
 
## Concevoir une chaîne de traitement --> même qu'avant??

Que veut-on obtenir en sortie ?
- Définir l’objet d’étude (les individus) et leur géométrie
- Combien de couches en sortie portent l’information, vecteur ou raster, quelle géométrie, quelle emprise (zone d’étude)

Quelles sont les données nécessaires ?
- Format, système de coordonnées de référence, géométrie
- Attributs/valeurs, structure des données, relations (un à un, un à plusieurs...)
Quels outils doivent être utilisés et dans quel ordre ?

### Batch/Lots : L'option partielle
La plupart des outils peuvent être exécutés par lots (batch processing), c’est-à-dire une seule exécution appliquée à plusieurs couches.
![](assets/)

### Python : L'option code
L’interface graphique permet de faire du SIG sans voir le code caché derrière.
MAIS créer un script permet :
- De répéter un traitement à intervalle régulier ;
- De rééditer la même analyse sur des jeux de données différents ;
- De publier ou transmettre tout le détail des traitements effectués.

Python fait partie intégrante des logiciels de SIG.
Des librairies Python dédiées à la géomatique (ex :
GDAL/OGR).

*Exemple avec OGR :*
*geometry = feature.GetGeometryRef()*
*x = geometry.GetX()*
*y = geometry.GetY()*

Les outils utilisent nativement Python, donc il est facile de récupérer le code (clic droit ou passer par l’historique).
Un langage «facile» car possède une syntaxe lisible et abordable, bien documenté.

APPRENDRE À PARLER PYTHON
Il existe énormément de ressources en ligne sur le langage python.
Les références : https://wiki.python.org/moin/BeginnersGuide https://www.w3schools.com/python/
Complet, en français :
https://python.developpez.com/tutoriels/apprendre-programmation-python/les-bases/?page=le-langage-p ython
Pour QGIS: https://docs.qgis.org/3.22/en/docs/pyqgis_developer_cookbook/index.html 
Pour ArcGIS: https://learn.arcgis.com/fr/paths/learn-python-in-arcgis-pro/

### Model Builder : L'option visuelle
- Le modeleur est un outil qui permet, via une interface graphique, de créer un modèle = chaîne de traitements.
- Le modeleur permet de connecter et paramétrer un ou plusieurs processus = séquence d’outils.
- Chaque processus modifie les données en entrée et/ou génère de nouvelles données.
- Permet de présenter visuellement son workflow. 
- Peut être transmis dans un projet empaqueté.
![](assets/)