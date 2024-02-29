# Question 7: échelle et calculs de distance

<link rel="stylesheet" href="assets/q7/style.css" />

Sur une carte avec échelle <span id="echelle_lbl">...</span>, vous mesurez la distance entre le sommet de l'Acongagua en Argentine, montagne la plus haute d'Amérique du Sud avec une altitude de <span id="alti1_lbl">...</span> mètres, et Los Andes, ville en Chilie, situé sur une altitude de <span id="alti2_lbl">...</span> mètres. Vous mesurez une distance de <span id="dist_cm_lbl">...</span> cm.

---

<form id="q7" onsubmit="event.preventDefault(); Q.submit()">
  <input type="hidden" id="echelle" name="echelle" />
  <input type="hidden" id="dist_cm" name="dist_cm" />
  <input type="hidden" id="alti1" name="alti1" />
  <input type="hidden" id="alti2" name="alti2" />

  <div style="margin-top: 15px;">
    <p>A. Quelle est la <b>distance à vol d'oiseau</b> (sur le plan, en 2 dimensions, donc sans tenir compte du relief) entre les 2 endroits ?</p>
    <p><input onchange="Q.save()" id="dist_2d" name="dist_2d" style="width: 150px;"/>&nbsp;km<br>
      <span style="font-size: 85%">(précision requise: 3 décimales après la virgule)</span>
    </p>
  </div>
  <hr />
  <div style="margin-top: 15px;">
    <p>B. Et quelle est la <b>distance réelle en 3D</b>, en tenant compte des différences d'altitude ? <span style="font-size: 85%">(donc la distance qu'un oiseau devrait voler en ligne droite sous l'hypothèse qu'il n'y a pas d'obstacle)</span></p>
    <p><input onchange="Q.save()" id="dist_3d" name="dist_3d" style="width: 150px;"/>&nbsp;km<br>
      <span style="font-size: 85%">(précision requise: 3 décimales après la virgule)</span>
    </p>
  </div>

  <hr />

  <div style="margin-top: 15px;">
    C. Faites une brève <b>réflexion sur la précision</b> des distances calculés:
    <textarea onchange="Q.save()" id="reflexion" name="reflexion" style="width: 100%; height: 120px;"></textarea>
  </div>

  <hr />
  <button class="btn btn-sm btn-success">Enregistrer</button>
</form>


<script src="assets/q7/script.js"></script>

