# Représentation des coordonnées latitude / longitude

Les coordonnées latitude / longitude (lat/long, lat/lng) peuvent être représentées et écrites de différentes manières.

Afin d'illustrer les différentes possibilités d'écriture, nous prendront ici les coordonnées géographiques du bâtiment de Géopolis à Lausanne.

1. Représentation **DMS** (degrés minutes secondes) par quadrant :
    * C'est la représentation qu'on l'habitude de voir
    * Coordonnées du bâtiment Géopolis : 46°31′35.605″N / 6°34′45.834″E

    * Avec :
        * ° : degré
        * ′ : minute
        * ″ : seconde

    * 1 minute est égale à 60 secondes
    * 1 degré est égal à 1 heure (60 minutes ou 3600 secondes)

2. Représentation **DMS** sans quadrant :
    * Comme vu précédemment, *N, S, W ou E* sont remplacés par des valeurs positives ou négatives
    * Coordonnées du bâtiment Géopolis : 46°31′35.605″ / 6°34′45.834″
    * Puisque nous nous trouvons dans le quadrant NE, les deux coordonnées ont des valeurs positives

3. Représentation **DD** (decimal degree)
    * Elle est très employée dans les logiciels de SIG
    * Une coordonnée **DMS** est convertie en coordonnée **DD** avec la formule :
       $D_{dec} = D + \frac{M}{60} + \frac{S}{3600}$
    * Donc pour convertir les coordonnées **DMS** du bâtiment Géopolis en coordonnées **DD** nous faisons :
        * Coordonnée latitude :
           $D_{dec} = 46 + \frac{31}{60} + \frac{35.605}{3600}$
        * Coordonnée longitude :
           $D_{dec} = 6 + \frac{34}{60} + \frac{45.834}{3600}$

    Ce qui nous donne (en arondissant) :
    * Latitude :
       $46 + 0.51\overline{6} + 0.00989 = 46.52656$
    * Longitude : 
       $6 + 0.5\overline{6} + 0.00127 = 6.57940$
        
Et donc les coordonnées **DD** du bâtiment Géopolis : ***46.52656, 6.57940***

## Conversion DMS en DD

Tentez de convertir les coordonnées DMS suivantes en coordonnées DD:

40° 41' 21.296″ N 74° 2' 40.2″ W"

Rendez-vous sur [Google Maps](https://www.google.ch/maps) et entrez les coordonnées DD que vous avez obtenu. A quel monument correspondent ces coordonnées ?
