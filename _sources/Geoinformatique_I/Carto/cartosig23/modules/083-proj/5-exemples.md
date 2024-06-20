# Quelques exemples de PCS

<style>
.center {
  display: block;
  margin-left: auto;
  margin-right: auto;
  height: auto;
}
</style>

Maintenant que nous avons compris comment les projections fonctionnent, il est plus aisé de comprendre les Systèmes de coordonnées projetées. Il s'agit donc simplement de coordonnées géographiques (exprimés en degrés) que nous avons transformer selon une projection qui nous convenait, pour finalement exprimer ces coordonnées sur un plan en 2D (avec un axe X et Y) avec des unités linéaires (mètres, etc ...)

## Deux exemples de Système de Coordonnées Projetées

Nous allons ici nous intéresser à deux PCS largement utilisés :

- Le premier à l'échelle internationale : ***Système UTM***
- Le deuxième à l'échelle nationale (Suisse) : ***LV03 et LV95***

### Système UTM (Universal Transverse Mercator)

<img src="assets/utm2.png" width="65%" class="center">

Ce système utilise donc, comme son nom l'indique, une ***projection transverse de Mercator***.

Il divise le monde en **60 fuseaux** (n'a rien à voir avec les fuseaux horaires) : 

* Chaque fuseau couvre **6° de longitude**
* Chaque fuseau définit donc un méridien touchant le cylindre de projection.
* Ainsi, chaque fuseau correspond à un système de coordonnées projeté et permet une bonne représentation des différentes régions

Le système est donc **rectangulaire** et les coordonnées sont exprimées en **mètres**.

* L'origine de la coordonnée x est définie par le fuseau choisi (le méridien central se trouve à 500 000m)
* L'origine de la coordonnée y est définie :
    * Par l’équateur pour l'hémisphère nord (N)
    * Par le pôle sud pour l'hémisphère sud (S)

Les coordonnées sont ainsi toujours positives.
Une indication complète du SRS nécessite donc l'indication du **fuseau** ***ET*** **de l'hémisphère**. Par exemple, pour la Suisse, nous devrions utiliser ***UTM 32N***, car la Suisse se trouve (quasiment) entièrement dans le fuseau 32 et dans l'hémisphère Nord.

## Projections utilisées en Suisse

Précédemment, la projection la plus utilisée en Suisse s’appelait ***Swiss Grid CH1903/LV03*** (pour **L**andes**v**ermessung 1903).

C'est une ***projection double cylindrique conforme à axe oblique*** :

- On projette l'*ellipsoïde* sur une *sphère*, puis on projette cette *sphère* sur un *cylindre* (Mercator oblique)
- Le cylindre est **tangent** à la sphère le long du *grand cercle* qui passe par Berne, et **perpendiculaire** au méridien de Berne.
- Il est défini sur l'**ellipsoïde de Bessel 1841**
- Les coordonnées sont exprimées en ***mètres***, avec pour référence un ancien observatoire de Berne (origine à 600 000 / 200 000 m)
- L'origine du système des axes (0, 0) se trouve à St-Emilion, près de Bordeaux, pour s'assurer d'avoir des coordonnées x et y positives et non ambiguës sur l'ensemble du territoire suisse

<img src="assets/swiss_grid.png" width="70%" class="center">

---

<img src="assets/1903.png" width="70%" class="center">

***Depuis 2017***, l'Office fédéral de la topographie a mis en place une [mensuration nationale](https://www.swisstopo.admin.ch/fr/connaissances-faits/mensuration-geodesie/cadres-de-reference/local/mn95.html "LV95") fondée sur la mensuration satellite, qui a remplacé progressivement l'ancien système de mesure fondé sur la triangulation nationale. Ce nouveau système de référence se nomme ***CH1903+/LV95***

- Il utilise le même ellipsoïde de référence que l'ancien système
- Afin de distinguer les coordonnées ***CH1903+*** des coordonnées ***CH1903***, un septième chiffre précède les anciennes coordonnées à 6 chiffres :
    - On ajoute un **1** pour les coordonnées dans la direction Ouest-Est
    - On ajout un **2** pour les coordonnées dans la direction Sud-Nord

## Base de données des systèmes de coordonnées

Tous les systèmes de coordonnées (géographiques et projetés) courant sont répertoriés dans une base de données par l'*Association Internationale de Prodcteurs de Pétrole et de Gaz (OGP)*. Cette base de données attribue un ***code EPSG*** à chaque système de coordonnées. Ces codes sont très utiles lorsqu'on recherche un système de coordonnées dans un logiciel type **SIG**.

Quelques exemples de ***codes EPSG*** :

- CH1903 / LV03 -> ***EPSG 21781***
- CH1903+ / LV95 -> ***EPSG 2056***
- WGS84 -> ***EPSG 4326***
