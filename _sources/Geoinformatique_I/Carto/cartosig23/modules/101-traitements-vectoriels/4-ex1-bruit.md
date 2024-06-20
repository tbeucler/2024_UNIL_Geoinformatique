# Exemple 1: traitements pour une analyse de bruit

Dans cette exemple, vous devez déterminer dans le cadre d'une analyse de bruit tous les bâtiments qui se trouvent à moins de 100 mètres d'une route principale ou d'une autoroute. Et ensuite, il faudra déterminer les parties de routes qui affectent ces bâtiments.

Cette analyse permettra par la suite de déterminer les mesures possibles pour diminuer le bruit dans les bâtiments. Il peut s'agit de mesures d'amélioration au niveau du bâtiment, ou au niveau de la route.

Les données nécessaires pour cette analyse sont une couche des routes et une couche des bâtiments. Un exemple de jeu de données possible est [Swiss Map Vector 25](https://www.swisstopo.admin.ch/fr/geodata/maps/smv.html). Vous pouvez télécharger une partie de ce jeu de données pour la région d'Interlaken-Grindelwald directement ici:

<a href="assets/swissMapVector25_254_CHLV95LN02.zip"><i class="far fa-file-pdf"></i> Swiss Map Vector 25 (feuille 254, région Interlaken-Grindelwald, fichier ZIP, 65 Mo)</a>

```content
type: video
id: analyseBruit
src: assets/analyse-de-bruit.m4v
```

<div style="border: 1px solid #999; padding: 15px; background-color: #dee;">
De manière générale, il est vivement conseillé de bien documenter les étapes de traitement en prenant des notes à côté, p.ex. dans un fichier texte. Chaque étape d'analyse est rapidement notée dans ce fichier, y compris les noms des couches. Ceci permet d'un côté d'avoir une bonne traçabilité de l'analyse faite, et en même temps, vous pouvez revoir vos notes plus tard quand vous devrez refaire un traitement similaire.
</div>
