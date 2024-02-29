# Question 1: calculs d'altitude

<link rel="stylesheet" href="assets/q1/style.css" />

Sur la base des fichiers fournis ci-dessous, déterminez l'altitude minimale, maximale et moyenne
de la commune suisse suivante: <b<span id="commune">...</span> (Numéro OFS: <span id="no_bfs">...</span>)</b>.

Les fichiers à utiliser pour l'analyse:

<ul>
  <li><a href="assets/q1/mnt25_ch.tif.zip"><i class="far fa-file"></i> Modèle numérique d'altitude MNT25</a> [Archive ZIP, 204 Mo]</li>
  <li><a href="assets/q1/swissboundaries3d_1_5_lv95.gpkg"><i class="far fa-file"></i> Communes suisses (fichier GeoPackage, 35 Mo)</a></li>
</ul>

Avant l'analyse, il faut extraire les fichiers ZIP. Le numéro OFS correspond à la colonne `bfs_nummer` de la couche des communes suisses.

---

<div id="q1wrapper" style="">
  <form id="q1" onsubmit="event.preventDefault(); Q.submit()">
    <div class="form-group">
      <label>Commune:</label>
      <input readonly id="commune_fld" name="commune" class="form-control" />
    </div>
    <div class="form-group">
      <label for="minAltitude">Altitude minimale:</label>
      <input id="minAltitude" name="minAltitude" class="form-control" onchange="Q.save()" />
    </div>
    <div class="form-group">
      <label for="maxAltitude">Altitude maximale:</label>
      <input id="maxAltitude" name="maxAltitude" class="form-control" onchange="Q.save()" />
    </div>
    <div class="form-group">
      <label for="avgAltitude">Altitude moyenne:</label>
      <input id="avgAltitude" name="avgAltitude" class="form-control" onchange="Q.save()" />
    </div>
    <button class="btn btn-sm btn-success">Enregistrer</button>
  </form>
</div>
<script src="assets/q1/script.js"></script>
