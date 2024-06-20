# Rendu et calendrier

Vous trouvez ici le détails des éléments à rendre. Notez surtout le contenu du fichier GeoPackage à créer, c'est quelque chose qui peut être fait dès le départ.

Le calendrier donne les informations sur l'avancement du TP. À chaque étape de travail, les informations sur comment accomplir la partie correspondante du TP sera rendue accessible.


## Éléments à rendre

Le rendu doit se faire dans le module du TP2 à la dernière étape. Les éléments suivants devront être rendus:

- Un fichier Adobe Illustrator (format .ai) avec la carte finale. Assurez-vous que votre carte est bien organisée en calquesl.

- Un fichier PDF (.pdf) avec le même contenu que le fichier Illustrator

- Un fichier GeoPackage qui contient les couches suivantes:

    - La couche des communes et quartiers de votre région. Cette couche doit contenir dans les attributs votre indicateur ainsi que tous les attributs qui ont permis de le calculer. Cette couche doit s'appeler `communes_quartiers`.
    
    - La couche de la zone tampon des 200 mètres autour des bâtiments, avec dans les attributs une colonne qui contient la superficie de chaque zone. Cette couche doit s'appeler `zones_tampons_200m`.

    - La couche de la zone bâtie (la zone tampon la plus grande). Cette couche doit s'appeler `zone_batie`.

    - Toutes les autres couches qui figurent sur la carte. Toutes ces couches doivent avoir un nom logique qui ne contient uniquement des caractères en minuscules, sans accents ou autres caractères spéciaux. Le nom de la couche peut toutefois contenir des tirets bas (`_`) et des nombres. Donc un nom `Zone bâtie` n'est pas permis, il doit être `zone_batie`.

- Votre projet QGIS qui permet d'afficher votre carte produite dans QGIS.


## Calendrier

Le calendrier ci-dessous définit les différentes étapes du travail telles que discutées dans le cadre des exercices. Il doit permettre d’assurer l’avancement du travail. Par ailleurs, le calendrier correspond exactement aux exercices du cours.

<table>
  <thead>
    <tr><th>Date</th><th>Étape de travail</th></tr>
  </thead>
  <tbody>
    <tr><td>13.11.</td><td>Début du travail pratique 2<br> 1 - Familiarisation avec les données<br />2 - Sélectionner et découper votre région</td></tr>
    <tr><td>20.11.</td><td>3 - Jointure des données<br />4 - Calcul de l'indicateur</td></tr>
    <tr><td>27.11.</td><td>5 - Cartographie de l'indicateur</td></tr>
    <tr><td>4.12.</td><td>6 - Calcul de la zone bâtie<br />7-  Calcul de la proportion d'habitants, ménages ou emplois<br />
    8 - Finalisation de la carte</td></tr>
    <tr><td>11.12.</td><td>Délai de rendu du travail pratique 2 (à 23h59 au plus tard)</td></tr>
  </tbody>
</table>