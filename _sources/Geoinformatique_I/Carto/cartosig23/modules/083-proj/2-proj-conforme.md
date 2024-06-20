# Projection conforme

<style>
.center {
  display: block;
  margin-left: auto;
  margin-right: auto;
  height: auto;
}
.surf {
    float: right;
}
</style>

La ***projection conforme*** permet de conserver le rapport local des **angles** et des **formes** des figures. Elle est notamment utilisée en *géodésie*, en topographie pour la *navigation*, dans les *applications militaires* et pour les *cartes à grandes échelles* pour permettre d'appliquer la trigonométrie plane dans les opérations courantes de topométrie.

Voici quelques exemples de ***projections conformes***:

* ***Mercator, Mercator transverses***
* ***Stéréographique***
* ***Projection conique conforme de Lambert***


## Quelques projection

### La projection de Mercator

La ***projection de Mercator*** est une des plus répandue. Nous allons nous y intéresser de plus près.

C'est une projection cylindrique en *trois variantes* selon l'orientation du cylindre :

* ***Mercator "normal"*** : le cylindre touche l’équateur (cylindre "debout")
* ***Mercator transverse*** : le cylindre touche un des méridiens (cylindre "couché")
* ***Mercator oblique*** : le cylindre touche un *grand cercle* (cercle tracé à la surface d'une sphère) qui n'est ni un méridien, ni l’équateur.

<img src="assets/cylindrique.gif" width="60%" class="center">

#### Caractéristiques de la projection Mercator "normale"

<img src="assets/mercator.gif" width="45%" class="center">

<br>
<br>

- Cette projection cylindrique touche l’équateur
<img src="assets/merca_surf.png" width="25%" class="surf">

- A cause de la reprojection d'une sphère à un cylindre, il y a une grande exagération des pôles, ce qui rend quasiment impossible leur représentation

- Elle est idéale pour les cartes locales proches de l’équateur (∓ 15°) car il y a peu ou pas de déformation des surfaces

- Elle est idéale pour la navigation avec la boussole car cette projection conforme garde les angles entre le Méridien et le Nord

- A éviter pour la plupart des cartes à petite échelle


#### Projection Mercator transverse ou oblique

Comme nous l'avons vu, la projection Mercator "normale" est idéale pour les régions proches de l’équateur car elle y déforme peu les surfaces.
Vient alors l'utilité d'utiliser une projection **Mercator transverse ou oblique** pour les régions qui s'éloignent de l’équateur. Ces projections permettent d'orienter le cylindre conformément à la région que nous voulons cartographier.

<img src="assets/trans.png" width="45%" class="center">

### Projection conique conforme de Lambert

Elle est utilisée notamment en France ou pour des cartes d'Europe à petites échelles

<img src="assets/lambert.png" width="55%" class="center">
<img src="assets/lambert2.png" width="45%" class="center">
