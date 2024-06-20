# Question 3: calcul de coordonnées

<link rel="stylesheet" href="assets/q3/style.css" />

Dans la couche vectorielle **swiss_names_pkg** disponible ci-dessous, vous trouverez un nombre important de points avec des noms des cartes topographiques suisses. Le jeu de données provient de [Swisstopo](https://www.swisstopo.admin.ch/fr/geodata/landscape/names3d.html).

<p><a href="assets/q3/swiss_names_pkt.zip"><i class="far fa-file"></i> swiss_names_pkt.zip (archive ZIP, 26 Mo)</a></p>

Dans cette couche vectorielle à ouvrir sur QGIS, il y a notamment les sommets alpins. On arrive à identifier les sommets grâce à l'attribut `OBJEKTART` qui contient la valeur `Alpiner Gipfel` pour cette catégorie de points.

Déterminez les coordonnées x, y et z pour le sommet suivant: <b><span id="sommet_lbl">...</span></b>

Déterminez aussi le nom et le code EPSG du SRS de la couche.

---

<div id="q3wrapper" style="">
  <form id="q3" onsubmit="event.preventDefault(); Q.submit()">
    <div class="form-group">
      <label>Sommet:</label>
      <input readonly id="sommet" name="commune" class="form-control" />
    </div>
    <div class="form-group">
      <label for="coordX">Coordonnées X:</label>
      <input id="coordX" name="coordX" class="form-control" onchange="Q.save()" style="width: 150px; display: inline-block;"/>
    </div>
    <div class="form-group">
      <label for="coordY">Coordonnées Y:</label>
      <input id="coordY" name="coordY" class="form-control" onchange="Q.save()" style="width: 150px; display: inline-block;"/>
    </div>
    <div class="form-group">
      <label for="coordZ">Coordonnées Z:</label>
      <input id="coordZ" name="coordZ" class="form-control" onchange="Q.save()" style="width: 150px; display: inline-block;"/>
    </div>
    <hr />
    <div class="form-group">
      <label for="epsg">Code EPSG du SRS:</label>
      <input id="epsg" name="epsg" class="form-control" onchange="Q.save()" style="width: 150px; display: inline-block;"/>
    </div>
    <div class="form-group">
      <label for="srs">Nom complet du SRS:</label>
      <input id="srs" name="srs" class="form-control" onchange="Q.save()" style="width: 150px; display: inline-block;"/>
    </div>
    <button class="btn btn-sm btn-success">Enregistrer</button>
  </form>
</div>
<script src="assets/q3/script.js"></script>
