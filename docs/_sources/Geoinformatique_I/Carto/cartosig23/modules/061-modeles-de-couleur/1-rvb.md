# Le modèle RVB

RVB est l'abréviation de «Rouge Vert Bleu», en anglais RGB signifie «Red Green Blue». Il s'agit d'un modèle de couleur qui est **basé sur la lumière** et il est utilisé notamment par tous les **écrans**. Un écran constitue la couleur par **synthèse additive** à partir des trois **couleurs primaires** qui sont le rouge, le vert et le bleu. En combinant ces trois couleurs primaires, il est possible d'obtenir n'importe quelle couleur qui est représentable dans le modèle RVB.

De manière concrète, une valeur numérique entre 0 (pour absence) et 255 est donnée à chacune des 3 couleurs primaires (255 est la valeur numérique la plus grande qui peut être représentée avec 1 octet, c'est-à-dire 8 bits). Ainsi, on peut régler la quantité de lumière rouge, vert et bleu.

Dans un modèle RVB, nous allons donc représenter une couleur à l'aide de 3 valeurs numériques, p.ex. (255, 0, 0) pour la couleur rouge. La première valeur représente la quantité de rouge, la deuxième la quantité de vert, et la troisième valeur la quantité de bleu.

L'absence de toutes les couleurs, la couleur (0, 0, 0), donne du noir, car nous avons absence de lumière. Si au contraire, nous mélangeons toutes les couleurs ensemble, nous obtenons la couleur avec le code (255, 255, 255) ce qui représente le blanc.

La figure ci-dessous montre les trois couleurs primaires ainsi que les combinaisons des couleurs, ensemble avec les codes couleurs:

![](assets/modele-rgb.png)

À l'aide de différentes valeurs pour les 3 couleurs primaires, nous pouvons définir toutes les couleurs qui peuvent être représentées à l'écran. Ci-dessous vous pouvez essayer plusieurs combinaisons des couleurs primaires. Essayez p.ex. de trouver la couleur orange:


<table id="colors">
<tr style="background-color: #f0f0f0;">
  <td rowspan="3"><div id="col" style="width: 200px; height: 200px; background-color: #f00">&nbsp;</div></td>
  <td>Rouge:</td><td id="rval" style="width: 50px">255</td>
  <td><input oninput="renderColor()" type="range" id="r" min="0" max="255" step="1" value="255" /></td>
</tr>
<tr style="background-color: #f0f0f0;">
  <td>Vert:</td><td id="vval" style="width: 50px">0</td>
  <td><input oninput="renderColor()" type="range" id="v" min="0" max="255" step="1" value="0" /></td>
</tr>
<tr style="background-color: #f0f0f0;">
  <td>Bleu:</td><td id="bval" style="width: 50px">0</td>
  <td><input oninput="renderColor()" type="range" id="b" min="0" max="255" step="1" value="0" /></td>
</tr>
</table>
<script>
function renderColor () {
  const r = document.getElementById('r').value
  const v = document.getElementById('v').value
  const b = document.getElementById('b').value
  document.getElementById('col').style.backgroundColor = `rgb(${r}, ${v}, ${b})`
  document.getElementById('rval').innerHTML = r
  document.getElementById('vval').innerHTML = v
  document.getElementById('bval').innerHTML = b
}
renderColor()
</script>
