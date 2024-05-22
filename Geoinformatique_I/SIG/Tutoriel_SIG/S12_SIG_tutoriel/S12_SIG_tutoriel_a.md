# Tutoriel 12 - Analyse spatiale II (A)

Dans cette section, nous aborderons les points suivants:

- Analyse de proximité et analyses de réseau (auto-corrélation??)
- Analyse de l’intensité (lissage spatial)
- Analyses multicritères – avec contraintes et facteurs

# Analyse de distance
Avec les analyses de distances, on répond à des questions du type :
- Comment un service (ponctuel) structure l’espace → aire d’influence, bassin de clientèle, aire de chalandise...
- Quels sont les caractéristiques de ces zones ?
- Quelle zone / quels objets se trouvent à une distance X d’un lieu donné ? 
- Quel est le plus court chemin entre A et B ?

On l’a vu, il existe différentes manière de mesurer des distances. Il y a donc diverses analyses de distance :
- En ligne droite, à une distance donnée : zone tampon (buffer)
- En ligne droite, sans recouvrement ni vides : polygones de Thiessen ou de Voronoï 
- Si la ligne droite se révèle trop grossière : distance au réseau

## Aires d'influence ou de chalandise

Polygones de Thiessen ou de Voronoï : un moyen simple et rapide de définir des «zones d’égale concurrence» autour de points (souvent des services). La surface des polygones varie selon la densité des points.
Par exemple : Quel est le profil socio-économique des habitants de l’aire de chalandise des hôpitaux romands ? Comparer les impacts de différentes usines de traitement des déchets en comparant les valeurs moyennes de pollution dans leur aire d’influence respective.
*cf. interpolation par proches voisins, pondérés en fonction de l’intersection entre la surface de leur zone d’influence et le périmètre de calcul.*
![](assets/)
OUTIL Créer des polygones de Thiessen

## Mesures sur des réseaux

Si l’on a besoin d’une distance (ou d’un temps) réaliste, il faut faire une analyse de réseau.
Etape 1 : **construire un réseau.**
Etape 2 : faire l’analyse

Conseil : utiliser les données OSM si besoin d’infos sur la circulation (tronçons accessibles aux vélos, limite de vitesse, sens uniques, ...), les données Swisstopo sinon.
![](assets/)
OUTIL Créer un jeu de données réseau

**Types d’analyses** : // linkhttps://pro.arcgis.com/fr/pro-app/latest/help/analysis/networks/network-analyst-solver-types.htm  
- Meilleur itinéraire
![](assets/)

- Ressource la plus proche
![](assets/)

- Zone de desserte
![](assets/)

- Emplacement-allocation
![](assets/)

SOLVEURS de Network Analyst

# Analyse de l'intensité (Lissage)

But du lissage spatial : pouvoir analyser des densités d’objets (sans être contraint par les limites administrative) et/ou fusionner des informations trop précises (confidentialité).
Par exemple : connaître la densité des arrêts de bus ou l’impact du réseau routier (en pondérant plus fortement une autoroute qu’une route de campagne).
Paramètres importants de la densité de noyau : le type de noyau, la population (pondération en fonction d’un attribut des objets), taille du voisinage prise en compte.
![](assets/)
OUTIL Densité de noyau

![](assets/) 

Possible d’ajouter des obstacle, pour limiter l’analyse aux zones pertinentes (= traitement des effets de bord). On peut utiliser des lignes ou des polygones.
![](assets/) 

La densité de point (ou de ligne) compte le nombre d’objets dans une surface autour chaque point (ou ligne). Le croisement des surfaces crée l’information recherchée.
Au contraire l’analyse de noyau calcule une valeur pour chaque pixel du raster.
![](assets/) 
OUTIL Densité de point

# Analyse Multicritère
Quelles sont les zones idéales pour implanter un toboggan aquatique alpin ?
Facteurs +
- Arrêt de TP à moins de 500m (zone tampon)
- Faible densité de piscines existantes (densité de noyau ou de points)
- Forte déclivité (pente)
- Ensoleillement (exposition) Contraintes -
- Hors réserves naturelles
Intersect (facteurs 1, 2, 3, 4) puis Erase (contrainte 1)
→ zones idéales
![](assets/) 

A quel niveau de risque de pénurie sont soumis les barrages du Valais ?
Facteurs +
- Grand bassin versant
- Grande proportion de glaciers dans le bassin versant 
Facteurs - = l’inverse
→ calculer un indice sur la base d’attributs avec la Calculatrice de champs.
![](assets/) 
![](assets/) or make the table!!