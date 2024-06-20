# Question 2: calculs de superficie

<link rel="stylesheet" href="assets/q2/style.css" />

Cette question porte sur le pays suivant: <b><span id="pays">...</span></b>.

La géometrie du pays est disponible dans la couche **"ne_10m_admin_0_countries"** du fichier suivant:
<a href="assets/q2/natural_earth_vector_10m.gpkg"><i class="far fa-file"></i> natural_earth_vector_10m.gpkg</a> [GeoPackage, 9.5 Mo]

Faites une extraction du pays à l'aide de QGIS. Le nom de pays indiqué ci-dessus correspond au contenu de l'attribut `SOVEREIGNT`. Ainsi, vous pourrez utiliser ce champ pour l'extraction du pays.

Projetez ensuite le pays dans deux systèmes de coordonnées:

<ul>
  <li>World Robinson (code ESRI:54030)</li>
  <li>UTM, dans la zone correspondante au pays. En cas de doute, prenez la localisation de la capitale du pays comme référence. Assurez-vous que vous prenez le SRS avec SCG WGS84; il s'agit des SRS avec code EPSG entre 32600 et 32760.</li>
</ul>

Calculez ensuite pour votre pays en entier (si composé de plusieurs parties, considérez la somme totale) la superficie à la fois géodésique (considérant la courbature de la Terre) et la superficie planimétrique. Le résultat doit être en km².

---

<div id="q1wrapper" style="">
  <form id="q2" onsubmit="event.preventDefault(); Q.submit()">
    <div class="form-group">
      <label>Pays:</label>
      <input readonly id="pays_fld" name="pays" class="form-control" style="width: 300px; display: inline-block;" />
    </div>
    <div class="form-group">
      <label for="robinsonGeodesique">World Robinson, superficie géodésique:</label>
      <input id="robinsonGeodesique" name="robinsonGeodesique" style="width: 150px; display: inline-block;" class="form-control" onchange="Q.save()" />&nbsp;km<sup>2</sup>
    </div>
    <div class="form-group">
      <label for="robinsonPlani">World Robinson, superficie planimétrique:</label>
      <input id="robinsonPlani" name="robinsonPlani" style="width: 150px; display: inline-block;" class="form-control" onchange="Q.save()" />&nbsp;km<sup>2</sup>
    </div>
    <div class="form-group">
      <label for="utmGeodesique">UTM, superficie géodésique:</label>
      <input id="utmGeodesique" name="utmGeodesique" style="width: 150px; display: inline-block;" class="form-control" onchange="Q.save()" />&nbsp;km<sup>2</sup>
    </div>
    <div class="form-group">
      <label for="utmPlani">UTM, superficie planimétrique:</label>
      <input id="utmPlani" name="utmPlani" style="width: 150px; display: inline-block;" class="form-control" onchange="Q.save()" />&nbsp;km<sup>2</sup>
    </div>
    <div class="form-group">
      <label for="utmCode">Notez également le code EPSG du SRS UTM utilisé:</label>
      <input id="utmCode" name="utmCode" style="width: 150px; display: inline-block;" class="form-control" onchange="Q.save()" />
    </div>
    <button class="btn btn-sm btn-success">Enregistrer</button>
  </form>
</div>
<script src="assets/q2/script.js"></script>
