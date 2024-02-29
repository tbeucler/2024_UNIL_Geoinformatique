# Coordonnées planes et les projections

La majorité des systèmes de coordonnées font référence à **un plan** alors que les phénomènes réels se localisent à **surface de la Terre** (donc sur le géoïde, représenté, comme vu précédemment, par un ellipsoïde ou une sphère).

On utilise alors les ***projections*** pour représenter les coordonnées géographiques dans un espace à deux dimensions.

Les **projections** traduisent en **unités linéaires** (par exemple en mètres) les coordonnées géographiques (exprimés en degrés).

Un tel système de coordonnées d'un plan est alors dit **Système de coordonnées projetées (PCS)**

<style>
.center {
  display: block;
  margin-left: auto;
  margin-right: auto;
  height: auto;
}
</style>

## Projection cartographique


La **projection cartographique** est donc un ensemble de techniques qui permet de représenter une **surface non plane** (la surface de la Terre) sur une surface plane. Elle est donc *une fonction mathématique destiné à projeter point par point une partie de l'ellipsoïde sur un plan*

Avantage : L'avantage principal de passer d'une forme ellipsoïdale (en 3D) à une surface plane est qu'il est alors possible de représenter la surface terrestre sur un support papier (ou un écran).

Désavantage : toutes les surfaces et les lignes subissent des **distorsions** lors de leur aplatissement en terme de **formes, surface, distance** et **direction**.

## Caractéristiques de la surface de projection

Nous allons maintenant nous intéresser un peu plus aux différentes caractéristiques qui permettent d'obtenir une projection optimale pour une région donnée :

* ***Géométrie de la surface*** : elle définit quelle forme possède la surface que nous allons projeter. Elle peut être :
    * **Conique (a)**
    * **Cylindrique (b)**
    * **Azymutale (c)**

<img src="assets/3.png" class="center">

* ***Position de la surface*** : elle définit si et comment la géométrie choisie coupe la surface de la Terre. Elle peut être :
    * **Tangente (ne coupe pas la surface)**
    * **Sécante (coupe la surface)**

Tangente :
<img src="assets/conique_tangente.gif" width="60%" class="center">
Sécante:
<img src="assets/conique_secante.gif" width="60%" class="center">

* ***L'aspect de la surface*** : elle définit l'angle de positionnement de la géométrie choisie.
    * Pour une géométrie cylindrique, l'aspect peut être :
        * ***Normal***
        * ***Transverse***
        * ***Oblique***

<img src="assets/cylindrique.gif" width="60%" class="center">

*   
    * Pour une géométrie planaire, il peut être :
        * ***Polaire***
        * ***Equatorial***
        * ***Oblique***

<img src="assets/planaire.gif" width="60%" class="center">

## Types de projections

Une projection cartographique est donc une *fonction mathématique destinée à projeter point par point une partie de l'ellipsoïde sur un plan.*

Comme vu précédemment, lorsque l'on passe d'un ellipsoïde à une surface plane, de nombreuses déformations sont impliquées. Il existe plusieurs types de projection qui permettent de conserver telle ou telle autre géométrie. En revanche, il faut souvent faire un compromis entre quelle(s) géométrie(s) nous voulons conserver au mieux.

1. ***Conforme*** : permet de conserver les angles
2. ***Equivalente*** : permet de conserver les surfaces
3. ***Equidistante*** : permet de conserver les distances (sur les méridiens)

Autre : ***Aphylactique*** : permet de faire un compromis entre les différentes déformations (ne conserve donc rien du tout)
