# Question 6: évaluation d'une carte thématique

<link rel="stylesheet" href="assets/q6/style.css" />

Cette question porte sur la même carte que la question précédente:

<div id="carte"></div>

<p style="font-size: 85%;">Source: <span id="source"></span></p>

<p style="font-size: 85%; font-style: italic;">Cliquez sur l'image pour ouvrir une version plus grande ou rendez-vous à la source du document où une version PDF est aussi disponible.</p>

---

Évaluez la qualité de la carte ci-dessus et faites 7 propositions d'amélioration de la carte.
Justifiez vos propositions.

Si vous avez plus de 7 propositions d'amélioration à faire, indiquez les 7 qui contribuent le plus
à l'amélioration de la carte.

---

<form id="q6" onsubmit="event.preventDefault(); Q.submit()">
  <input type="hidden" id="asset_id" name="asset_id" />
  <div style="margin-top: 15px;">
    <table style="width: 100%">
      <thead>
        <tr>
          <th>N°</th>
          <th>Proposition d'amélioration</th>
          <th>Justification</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>1</td>
          <td style="width: calc(40% - 40px);"><input id="r1_prop" name="r1_prop" onchange="Q.save()" /></td>
          <td style="width: calc(60% - 40px);"><textarea id="r1_just" name="r1_just" onchange="Q.save()"></textarea></td>
        </tr>
        <tr>
          <td>2</td>
          <td><input id="r2_prop" name="r2_prop" onchange="Q.save()" /></td>
          <td><textarea id="r2_just" name="r2_just" onchange="Q.save()"></textarea></td>
        </tr>
        <tr>
          <td>3</td>
          <td><input id="r3_prop" name="r3_prop" onchange="Q.save()" /></td>
          <td><textarea id="r3_just" name="r3_just" onchange="Q.save()"></textarea></td>
        </tr>
        <tr>
          <td>4</td>
          <td><input id="r4_prop" name="r4_prop" onchange="Q.save()" /></td>
          <td><textarea id="r4_just" name="r4_just" onchange="Q.save()"></textarea></td>
        </tr>
        <tr>
          <td>5</td>
          <td><input id="r5_prop" name="r5_prop" onchange="Q.save()" /></td>
          <td><textarea id="r5_just" name="r5_just" onchange="Q.save()"></textarea></td>
        </tr>
        <tr>
          <td>6</td>
          <td><input id="r6_prop" name="r6_prop" onchange="Q.save()" /></td>
          <td><textarea id="r6_just" name="r6_just" onchange="Q.save()"></textarea></td>
        </tr>
        <tr>
          <td>7</td>
          <td><input id="r7_prop" name="r7_prop" onchange="Q.save()" /></td>
          <td><textarea id="r7_just" name="r7_just" onchange="Q.save()"></textarea></td>
        </tr>
      </tbody>
    </table>
  </div>
  <hr />
  <div style="margin-top: 15px;">
    <p style="font-weight: 700;">Si nécessaire, vous pouvez laisser un commentaire général (optionnel):</p>
    <textarea onchange="Q.save()" id="commentaire" name="commentaire" style="width: 100%; height: 80px;"></textarea>
  </div>
  <hr />
  <button class="btn btn-sm btn-success">Enregistrer</button>
</form>

<script src="assets/q6/script.js"></script>
