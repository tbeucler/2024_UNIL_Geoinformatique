# Question 5: sémiologie graphique

<link rel="stylesheet" href="assets/q5/style.css" />

Analysez la carte ci-dessous qui provient de l'Office fédéral de la statistique:

<div id="carte"></div>

<p style="font-size: 85%;">Source: <span id="source"></span></p>

<p style="font-size: 85%; font-style: italic;">Cliquez sur l'image pour ouvrir une version plus grande ou rendez-vous à la source du document où une version PDF est aussi disponible.</p>

---

<form id="q5" onsubmit="event.preventDefault(); Q.submit()">
  <input type="hidden" id="asset_id" name="asset_id" />
  <div style="margin-top: 15px;">
    <p style="font-weight: 700;">A. Quel est le type de cette carte ?</p>
    <textarea onchange="Q.save()" id="type_carte" name="type_carte" style="width: 100%; height: 80px;"></textarea>
  </div>
  <hr />
  <div style="margin-top: 15px;">
    <p><b>B. Quelles sont les informations figurant sur la carte, de quelle nature sont-elles et comment elles ont été représentées? Jugez également la qualité de la représentation (l'efficacité).</b></p>
    <p>Identifiez séparément chaque information (variable, indicateur), et ajoutez la nature de l'information (type de variable) et comment elle est représentée (par quelle variable visuelle).</p>
    <p>Exemple pour une carte thématique montrant le nombre d'habitants (p.ex. par district) représenté par des symboles proportionnels:</p>
    <table>
      <thead>
        <tr>
          <th>Information</th>
          <th>Échelle de mesure</th>
          <th>Type de donnée cartographique</th>
          <th>Variable visuelle utilisée</th>
          <th>Efficacité</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Nombre d'habitants</td>
          <td>Intervalle</td>
          <td>Variable absolue</td>
          <td>Taille</td>
          <td>Bonne</td>
        </tr>
      </tbody>
    </table>
    <p>Dans le tableau ci-dessous, remplissez une ligne pour chaque information identifiée sur la carte.</p>
    <p style="font-size: 85%; font-style: italic;">Ci-dessous, vous pouvez remplir les information pour un total de 8 variables représentées au maximum. À priori, c'est bien plus que nécessaire. Laissez simplement vide les parties dont vous n'avez pas besoin. Vous pouvez aussi ajouter un commentaire (optionnel) pour chaque information identifiée. Finalement, vous avez la possibilité d'ajouter un commentaire général à la fin (aussi optionnel).</p>
    <table style="border: 1px solid #e0e0e0;">
      <thead>
        <tr>
          <th colspan="2">Information 1</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Information (p.ex. nom de la variable):</td>
          <td><input id="r01_informa" name="r01_informa" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Échelle de mesure:</td>
          <td><input id="r01_echMesu" name="r01_echMesu" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Type de donnée cartographique:</td>
          <td><input id="r01_typeVar" name="r01_typeVar" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Variable visuelle:</td>
          <td><input id="r01_varVisu" name="r01_varVisu" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Efficacité de représentation:</td>
          <td>
            <select id="r01_efficac" name="r01_efficac" onchange="Q.save()">
              <option value="-"></option>
              <option value="bonne">Bonne</option>
              <option value="mediocre">Médiocre</option>
              <option value="marginale">Marginale</option>
            </select>
          </td>
        </tr>
        <tr>
          <td>Commentaire facultatif:</td>
          <td><input id="r01_comment" name="r01_comment" onchange="Q.save()" /></td>
        </tr>
      </tbody>
    </table>
    <table style="border: 1px solid #e0e0e0;">
      <thead>
        <tr>
          <th colspan="2">Information 2</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Information (p.ex. nom de la variable):</td>
          <td><input id="r02_informa" name="r02_informa" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Échelle de mesure:</td>
          <td><input id="r02_echMesu" name="r02_echMesu" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Type de donnée cartographique:</td>
          <td><input id="r02_typeVar" name="r02_typeVar" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Variable visuelle:</td>
          <td><input id="r02_varVisu" name="r02_varVisu" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Efficacité de représentation:</td>
          <td>
            <select id="r02_efficac" name="r02_efficac" onchange="Q.save()">
              <option value="-"></option>
              <option value="bonne">Bonne</option>
              <option value="mediocre">Médiocre</option>
              <option value="marginale">Marginale</option>
            </select>
          </td>
        </tr>
        <tr>
          <td>Commentaire facultatif:</td>
          <td><input id="r02_comment" name="r02_comment" onchange="Q.save()" /></td>
        </tr>
      </tbody>
    </table>
    <table style="border: 1px solid #e0e0e0;">
      <thead>
        <tr>
          <th colspan="2">Information 3</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Information (p.ex. nom de la variable):</td>
          <td><input id="r03_informa" name="r03_informa" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Échelle de mesure:</td>
          <td><input id="r03_echMesu" name="r03_echMesu" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Type de donnée cartographique:</td>
          <td><input id="r03_typeVar" name="r03_typeVar" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Variable visuelle:</td>
          <td><input id="r03_varVisu" name="r03_varVisu" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Efficacité de représentation:</td>
          <td>
            <select id="r03_efficac" name="r03_efficac" onchange="Q.save()">
              <option value="-"></option>
              <option value="bonne">Bonne</option>
              <option value="mediocre">Médiocre</option>
              <option value="marginale">Marginale</option>
            </select>
          </td>
        </tr>
        <tr>
          <td>Commentaire facultatif:</td>
          <td><input id="r03_comment" name="r03_comment" onchange="Q.save()" /></td>
        </tr>
      </tbody>
    </table>
    <table style="border: 1px solid #e0e0e0;">
      <thead>
        <tr>
          <th colspan="2">Information 4</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Information (p.ex. nom de la variable):</td>
          <td><input id="r04_informa" name="r04_informa" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Échelle de mesure:</td>
          <td><input id="r04_echMesu" name="r04_echMesu" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Type de donnée cartographique:</td>
          <td><input id="r04_typeVar" name="r04_typeVar" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Variable visuelle:</td>
          <td><input id="r04_varVisu" name="r04_varVisu" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Efficacité de représentation:</td>
          <td>
            <select id="r04_efficac" name="r04_efficac" onchange="Q.save()">
              <option value="-"></option>
              <option value="bonne">Bonne</option>
              <option value="mediocre">Médiocre</option>
              <option value="marginale">Marginale</option>
            </select>
          </td>
        </tr>
        <tr>
          <td>Commentaire facultatif:</td>
          <td><input id="r04_comment" name="r04_comment" onchange="Q.save()" /></td>
        </tr>
      </tbody>
    </table>
    <table style="border: 1px solid #e0e0e0;">
      <thead>
        <tr>
          <th colspan="2">Information 5</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Information (p.ex. nom de la variable):</td>
          <td><input id="r05_informa" name="r05_informa" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Échelle de mesure:</td>
          <td><input id="r05_echMesu" name="r05_echMesu" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Type de donnée cartographique:</td>
          <td><input id="r05_typeVar" name="r05_typeVar" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Variable visuelle:</td>
          <td><input id="r05_varVisu" name="r05_varVisu" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Efficacité de représentation:</td>
          <td>
            <select id="r05_efficac" name="r05_efficac" onchange="Q.save()">
              <option value="-"></option>
              <option value="bonne">Bonne</option>
              <option value="mediocre">Médiocre</option>
              <option value="marginale">Marginale</option>
            </select>
          </td>
        </tr>
        <tr>
          <td>Commentaire facultatif:</td>
          <td><input id="r05_comment" name="r05_comment" onchange="Q.save()" /></td>
        </tr>
      </tbody>
    </table>
    <table style="border: 1px solid #e0e0e0;">
      <thead>
        <tr>
          <th colspan="2">Information 5</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Information (p.ex. nom de la variable):</td>
          <td><input id="r06_informa" name="r06_informa" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Échelle de mesure:</td>
          <td><input id="r06_echMesu" name="r06_echMesu" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Type de donnée cartographique:</td>
          <td><input id="r06_typeVar" name="r06_typeVar" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Variable visuelle:</td>
          <td><input id="r06_varVisu" name="r06_varVisu" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Efficacité de représentation:</td>
          <td>
            <select id="r06_efficac" name="r06_efficac" onchange="Q.save()">
              <option value="-"></option>
              <option value="bonne">Bonne</option>
              <option value="mediocre">Médiocre</option>
              <option value="marginale">Marginale</option>
            </select>
          </td>
        </tr>
        <tr>
          <td>Commentaire facultatif:</td>
          <td><input id="r06_comment" name="r06_comment" onchange="Q.save()" /></td>
        </tr>
      </tbody>
    </table>
    <table style="border: 1px solid #e0e0e0;">
      <thead>
        <tr>
          <th colspan="2">Information 7</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Information (p.ex. nom de la variable):</td>
          <td><input id="r07_informa" name="r07_informa" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Échelle de mesure:</td>
          <td><input id="r07_echMesu" name="r07_echMesu" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Type de donnée cartographique:</td>
          <td><input id="r07_typeVar" name="r07_typeVar" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Variable visuelle:</td>
          <td><input id="r07_varVisu" name="r07_varVisu" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Efficacité de représentation:</td>
          <td>
            <select id="r07_efficac" name="r07_efficac" onchange="Q.save()">
              <option value="-"></option>
              <option value="bonne">Bonne</option>
              <option value="mediocre">Médiocre</option>
              <option value="marginale">Marginale</option>
            </select>
          </td>
        </tr>
        <tr>
          <td>Commentaire facultatif:</td>
          <td><input id="r07_comment" name="r07_comment" onchange="Q.save()" /></td>
        </tr>
      </tbody>
    </table>
    <table style="border: 1px solid #e0e0e0;">
      <thead>
        <tr>
          <th colspan="2">Information 8</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Information (p.ex. nom de la variable):</td>
          <td><input id="r08_informa" name="r08_informa" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Échelle de mesure:</td>
          <td><input id="r08_echMesu" name="r08_echMesu" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Type de donnée cartographique:</td>
          <td><input id="r08_typeVar" name="r08_typeVar" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Variable visuelle:</td>
          <td><input id="r08_varVisu" name="r08_varVisu" onchange="Q.save()" /></td>
        </tr>
        <tr>
          <td>Efficacité de représentation:</td>
          <td>
            <select id="r08_efficac" name="r08_efficac" onchange="Q.save()">
              <option value="-"></option>
              <option value="bonne">Bonne</option>
              <option value="mediocre">Médiocre</option>
              <option value="marginale">Marginale</option>
            </select>
          </td>
        </tr>
        <tr>
          <td>Commentaire facultatif:</td>
          <td><input id="r08_comment" name="r08_comment" onchange="Q.save()" /></td>
        </tr>
      </tbody>
    </table>
  </div>
  <hr />
  <div style="margin-top: 15px;">
    <p style="font-weight: 700;">Commentaire général (optionnel):</p>
    <textarea onchange="Q.save()" id="commentaire" name="commentaire" style="width: 100%; height: 80px;"></textarea>
  </div>
  <hr />
  <button class="btn btn-sm btn-success">Enregistrer</button>
</form>

<script src="assets/q5/script.js"></script>
