# Question 8: abstraction cartographique

<link rel="stylesheet" href="assets/q8/style.css" />

Consultez la carte à l'URL suivante: <span id="map_url_z8">...</span> (<b>Extrait A</b>).

Et comparez cet extrait avec la carte à l'URL suivante: <span id="map_url_z6">...</span> (<b>Extrait B</b>).

Pendant votre analyse, assurez-vous de ne pas zoomer la carte et de la laisser centrer au même endroit que lors de l'ouverture (carte centrée sur &laquo;<span id="name_lbl">...</span>&raquo;).

La différence entre les deux extrait est l'échelle, celle de l'extrait A est plus grande que pour l'extrait B. L'extrait A est contenu entièrement à l'intérieur de l'extrait B.

Identifiez 5 endroits sur l'extrait A où vous pouvez constater l'utilisation d'un opérateur d'abstraction cartographique par rapport à l'extrait B. Les 5 opérateurs de généralisation doivent être différents.

Pour chaque endroit, obtenez les coordonnées (clic droit avec la souris à l'endroit identifié sur l'extrait A). Considérez les coordonnées en CH1903+/LV95.

Notez ci-dessous l'opérateur de généralisation identifié ainsi que les coordonnées X et Y où vous l'avez observé. Vous pouvez également y ajouter un commentaire si vous souhaitez.

<form id="q8" onsubmit="event.preventDefault(); Q.submit()">
  <input type="hidden" id="coords" name="coords" />
  <input type="hidden" id="name" name="name" />

  <hr />
  <div style="margin-top: 15px;">
    <b>Opérateur 1:</b>
    <p>
      <label>Opérateur d'abstraction: </label><input onchange="Q.save()" id="op1_txt" name="op1_txt" style="min-width: 300px; width: calc(100% - 210px)"/><br>
      <label>Coordonnée X: </label><input onchange="Q.save()" style="width: 150px;" id="op1_x" name="op1_x" /><br>
      <label>Coordonnée Y: </label><input onchange="Q.save()" style="width: 150px;" id="op1_y" name="op1_y" />
    </p>
    <p>Commentaire (optionnel):<br />
      <textarea style="width: 100%" id="op1_comment" name="op1_comment" onchange="Q.save()"></textarea>
    </p>
  </div>

  <hr />
  <div style="margin-top: 15px;">
    <b>Opérateur 2:</b>
    <p>
      <label>Opérateur d'abstraction: </label><input onchange="Q.save()" id="op2_txt" name="op2_txt" style="min-width: 300px; width: calc(100% - 210px)"/><br>
      <label>Coordonnée X: </label><input onchange="Q.save()" style="width: 150px;" id="op2_x" name="op2_x" /><br>
      <label>Coordonnée Y: </label><input onchange="Q.save()" style="width: 150px;" id="op2_y" name="op2_y" />
    </p>
    <p>Commentaire (optionnel):<br />
      <textarea style="width: 100%" id="op2_comment" name="op2_comment" onchange="Q.save()"></textarea>
    </p>
  </div>

  <hr />
  <div style="margin-top: 15px;">
    <b>Opérateur 3:</b>
    <p>
      <label>Opérateur d'abstraction: </label><input onchange="Q.save()" id="op3_txt" name="op3_txt" style="min-width: 300px; width: calc(100% - 210px)"/><br>
      <label>Coordonnée X: </label><input onchange="Q.save()" style="width: 150px;" id="op3_x" name="op3_x" /><br>
      <label>Coordonnée Y: </label><input onchange="Q.save()" style="width: 150px;" id="op3_y" name="op3_y" />
    </p>
    <p>Commentaire (optionnel):<br />
      <textarea style="width: 100%" id="op3_comment" name="op3_comment" onchange="Q.save()"></textarea>
    </p>
  </div>

  <hr />
  <div style="margin-top: 15px;">
    <b>Opérateur 4:</b>
    <p>
      <label>Opérateur d'abstraction: </label><input onchange="Q.save()" id="op4_txt" name="op4_txt" style="min-width: 300px; width: calc(100% - 210px)"/><br>
      <label>Coordonnée X: </label><input onchange="Q.save()" style="width: 150px;" id="op4_x" name="op4_x" /><br>
      <label>Coordonnée Y: </label><input onchange="Q.save()" style="width: 150px;" id="op4_y" name="op4_y" />
    </p>
    <p>Commentaire (optionnel):<br />
      <textarea style="width: 100%" id="op4_comment" name="op4_comment" onchange="Q.save()"></textarea>
    </p>
  </div>

  <hr />
  <div style="margin-top: 15px;">
    <b>Opérateur 5:</b>
    <p>
      <label>Opérateur d'abstraction: </label><input onchange="Q.save()" id="op5_txt" name="op5_txt" style="min-width: 300px; width: calc(100% - 210px)"/><br>
      <label>Coordonnée X: </label><input onchange="Q.save()" style="width: 150px;" id="op5_x" name="op5_x" /><br>
      <label>Coordonnée Y: </label><input onchange="Q.save()" style="width: 150px;" id="op5_y" name="op5_y" />
    </p>
    <p>Commentaire (optionnel):<br />
      <textarea style="width: 100%" id="op5_comment" name="op5_comment" onchange="Q.save()"></textarea>
    </p>
  </div>

  <hr />
  <button class="btn btn-sm btn-success">Enregistrer</button>
</form>

<script src="assets/q8/script.js"></script>
