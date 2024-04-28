# Question 4: modèles du territoire

<link rel="stylesheet" href="assets/q4/style.css" />

Attribuez le type de modèle et, le cas échéant, la géométrie de base utilisée aux images suivantes. Expliquez aussi les caractéristiques des modèles identifiés ainsi que de la notion de résolution.

<form id="q4" onsubmit="event.preventDefault(); Q.submit()">

<div id="q41wrapper" style="display: none;">
  <h2 id="h2_q41">Exemple 1</h2>
  <img src="assets/q4/mod1.png" />
  <div style="margin-top: 15px;">
    <b>Modèle de territoire:</b>
    <div class="form-group">
      <label><input onchange="Q.save()" type="radio" id="m1_raster" name="m1_mod"> Modèle raster</label><br/>
      <label><input onchange="Q.save()" type="radio" id="m1_vector" name="m1_mod"> Modèle vectoriel</label>
    </div>
    <div style="margin-top: 10px;">
      <b>Géométrie de base.</b> Cochez toutes les options possibles. Si nécessaire, ajoutez un commentaire.</b>
    </div>
    <div class="form-group">
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m1_Point" name="m1_Point"> Point</label>&nbsp;
        <input onchange="Q.save()" id="m1_Point_cmt" name="m1_Point_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m1_LineString" name="m1_LineString"> LineString</label>&nbsp;
        <input onchange="Q.save()" id="m1_LineString_cmt" name="m1_LineString_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m1_LinearRing" name="m1_LinearRing"> LinearRing</label>&nbsp;
        <input onchange="Q.save()" id="m1_LinearRing_cmt" name="m1_LinearRing_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m1_Polygon" name="m1_Polygon"> Polygon</label>&nbsp;
        <input onchange="Q.save()" id="m1_Polygon_cmt" name="m1_Polygon_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m1_MultiPoint" name="m1_MultiPoint"> MultiPoint</label>&nbsp;
        <input onchange="Q.save()" id="m1_MultiPoint_cmt" name="m1_MultiPoint_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m1_MultiLineString" name="m1_MultiLineString"> MultiLineString</label>&nbsp;
        <input onchange="Q.save()" id="m1_MultiLineString_cmt" name="m1_MultiLineString_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m1_MultiPolygon" name="m1_MultiPolygon"> MultiPolygon</label>&nbsp;
        <input onchange="Q.save()" id="m1_MultiPolygon_cmt" name="m1_MultiPolygon_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
    </div>
  </div>
</div>



<div id="q42wrapper" style="display: none;">
  <h2 id="h2_q42">Exemple 2</h2>
  <img src="assets/q4/mod2.png" />
  <div style="margin-top: 15px;">
    <b>Modèle de territoire:</b>
    <div class="form-group">
      <label><input onchange="Q.save()" type="radio" id="m2_raster" name="m2_mod"> Modèle raster</label><br/>
      <label><input onchange="Q.save()" type="radio" id="m2_vector" name="m2_mod"> Modèle vectoriel</label>
    </div>
    <div style="margin-top: 10px;">
      <b>Géométrie de base.</b> Cochez toutes les options possibles. Si nécessaire, ajoutez un commentaire.</b>
    </div>
    <div class="form-group">
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m2_Point" name="m2_Point"> Point</label>&nbsp;
        <input onchange="Q.save()" id="m2_Point_cmt" name="m2_Point_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m2_LineString" name="m2_LineString"> LineString</label>&nbsp;
        <input onchange="Q.save()" id="m2_LineString_cmt" name="m2_LineString_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m2_LinearRing" name="m2_LinearRing"> LinearRing</label>&nbsp;
        <input onchange="Q.save()" id="m2_LinearRing_cmt" name="m2_LinearRing_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m2_Polygon" name="m2_Polygon"> Polygon</label>&nbsp;
        <input onchange="Q.save()" id="m2_Polygon_cmt" name="m2_Polygon_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m2_MultiPoint" name="m2_MultiPoint"> MultiPoint</label>&nbsp;
        <input onchange="Q.save()" id="m2_MultiPoint_cmt" name="m2_MultiPoint_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m2_MultiLineString" name="m2_MultiLineString"> MultiLineString</label>&nbsp;
        <input onchange="Q.save()" id="m2_MultiLineString_cmt" name="m2_MultiLineString_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m2_MultiPolygon" name="m2_MultiPolygon"> MultiPolygon</label>&nbsp;
        <input onchange="Q.save()" id="m2_MultiPolygon_cmt" name="m2_MultiPolygon_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
    </div>
  </div>
</div>




<div id="q43wrapper" style="display: none;">
    <h2 id="h2_q43">Exemple 3</h2>
  <img src="assets/q4/mod3.png" />
  <div style="margin-top: 15px;">
    <b>Modèle de territoire:</b>
    <div class="form-group">
      <label><input onchange="Q.save()" type="radio" id="m3_raster" name="m3_mod"> Modèle raster</label><br/>
      <label><input onchange="Q.save()" type="radio" id="m3_vector" name="m3_mod"> Modèle vectoriel</label>
    </div>
    <div style="margin-top: 10px;">
      <b>Géométrie de base.</b> Cochez toutes les options possibles. Si nécessaire, ajoutez un commentaire.</b>
    </div>
    <div class="form-group">
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m3_Point" name="m3_Point"> Point</label>&nbsp;
        <input onchange="Q.save()" id="m3_Point_cmt" name="m3_Point_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m3_LineString" name="m3_LineString"> LineString</label>&nbsp;
        <input onchange="Q.save()" id="m3_LineString_cmt" name="m3_LineString_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m3_LinearRing" name="m3_LinearRing"> LinearRing</label>&nbsp;
        <input onchange="Q.save()" id="m3_LinearRing_cmt" name="m3_LinearRing_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m3_Polygon" name="m3_Polygon"> Polygon</label>&nbsp;
        <input onchange="Q.save()" id="m3_Polygon_cmt" name="m3_Polygon_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m3_MultiPoint" name="m3_MultiPoint"> MultiPoint</label>&nbsp;
        <input onchange="Q.save()" id="m3_MultiPoint_cmt" name="m3_MultiPoint_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m3_MultiLineString" name="m3_MultiLineString"> MultiLineString</label>&nbsp;
        <input onchange="Q.save()" id="m3_MultiLineString_cmt" name="m3_MultiLineString_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m3_MultiPolygon" name="m3_MultiPolygon"> MultiPolygon</label>&nbsp;
        <input onchange="Q.save()" id="m3_MultiPolygon_cmt" name="m3_MultiPolygon_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
    </div>
  </div>
</div>



<div id="q44wrapper" style="display: none;">
  <h2 id="h2_q44">Exemple 4</h2>
  <img src="assets/q4/mod4.png" />
  <div style="margin-top: 15px;">
    <b>Modèle de territoire:</b>
    <div class="form-group">
      <label><input onchange="Q.save()" type="radio" id="m4_raster" name="m4_mod"> Modèle raster</label><br/>
      <label><input onchange="Q.save()" type="radio" id="m4_vector" name="m4_mod"> Modèle vectoriel</label>
    </div>
    <div style="margin-top: 10px;">
      <b>Géométrie de base.</b> Cochez toutes les options possibles. Si nécessaire, ajoutez un commentaire.</b>
    </div>
    <div class="form-group">
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m4_Point" name="m4_Point"> Point</label>&nbsp;
        <input onchange="Q.save()" id="m4_Point_cmt" name="m4_Point_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m4_LineString" name="m4_LineString"> LineString</label>&nbsp;
        <input onchange="Q.save()" id="m4_LineString_cmt" name="m4_LineString_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m4_LinearRing" name="m4_LinearRing"> LinearRing</label>&nbsp;
        <input onchange="Q.save()" id="m4_LinearRing_cmt" name="m4_LinearRing_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m4_Polygon" name="m4_Polygon"> Polygon</label>&nbsp;
        <input onchange="Q.save()" id="m4_Polygon_cmt" name="m4_Polygon_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m4_MultiPoint" name="m4_MultiPoint"> MultiPoint</label>&nbsp;
        <input onchange="Q.save()" id="m4_MultiPoint_cmt" name="m4_MultiPoint_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m4_MultiLineString" name="m4_MultiLineString"> MultiLineString</label>&nbsp;
        <input onchange="Q.save()" id="m4_MultiLineString_cmt" name="m4_MultiLineString_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m4_MultiPolygon" name="m4_MultiPolygon"> MultiPolygon</label>&nbsp;
        <input onchange="Q.save()" id="m4_MultiPolygon_cmt" name="m4_MultiPolygon_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
    </div>
  </div>
</div>




<div id="q45wrapper" style="display: none;">
  <h2 id="h2_q45">Exemple 5</h2>
  <img src="assets/q4/mod5.png" />
  <div style="margin-top: 15px;">
    <b>Modèle de territoire:</b>
    <div class="form-group">
      <label><input onchange="Q.save()" type="radio" id="m5_raster" name="m5_mod"> Modèle raster</label><br/>
      <label><input onchange="Q.save()" type="radio" id="m5_vector" name="m5_mod"> Modèle vectoriel</label>
    </div>
    <div style="margin-top: 10px;">
      <b>Géométrie de base.</b> Cochez toutes les options possibles. Si nécessaire, ajoutez un commentaire.</b>
    </div>
    <div class="form-group">
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m5_Point" name="m5_Point"> Point</label>&nbsp;
        <input onchange="Q.save()" id="m5_Point_cmt" name="m5_Point_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m5_LineString" name="m5_LineString"> LineString</label>&nbsp;
        <input onchange="Q.save()" id="m5_LineString_cmt" name="m5_LineString_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m5_LinearRing" name="m5_LinearRing"> LinearRing</label>&nbsp;
        <input onchange="Q.save()" id="m5_LinearRing_cmt" name="m5_LinearRing_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m5_Polygon" name="m5_Polygon"> Polygon</label>&nbsp;
        <input onchange="Q.save()" id="m5_Polygon_cmt" name="m5_Polygon_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m5_MultiPoint" name="m5_MultiPoint"> MultiPoint</label>&nbsp;
        <input onchange="Q.save()" id="m5_MultiPoint_cmt" name="m5_MultiPoint_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m5_MultiLineString" name="m5_MultiLineString"> MultiLineString</label>&nbsp;
        <input onchange="Q.save()" id="m5_MultiLineString_cmt" name="m5_MultiLineString_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m5_MultiPolygon" name="m5_MultiPolygon"> MultiPolygon</label>&nbsp;
        <input onchange="Q.save()" id="m5_MultiPolygon_cmt" name="m5_MultiPolygon_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
    </div>
  </div>
</div>




<div id="q46wrapper" style="display: none;">
  <h2 id="h2_q46">Exemple 6</h2>
  <img src="assets/q4/mod6.png" />
  <div style="margin-top: 15px;">
    <b>Modèle de territoire:</b>
    <div class="form-group">
      <label><input onchange="Q.save()" type="radio" id="m6_raster" name="m6_mod"> Modèle raster</label><br/>
      <label><input onchange="Q.save()" type="radio" id="m6_vector" name="m6_mod"> Modèle vectoriel</label>
    </div>
    <div style="margin-top: 10px;">
      <b>Géométrie de base.</b> Cochez toutes les options possibles. Si nécessaire, ajoutez un commentaire.</b>
    </div>
    <div class="form-group">
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m6_Point" name="m6_Point"> Point</label>&nbsp;
        <input onchange="Q.save()" id="m6_Point_cmt" name="m6_Point_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m6_LineString" name="m6_LineString"> LineString</label>&nbsp;
        <input onchange="Q.save()" id="m6_LineString_cmt" name="m6_LineString_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m6_LinearRing" name="m6_LinearRing"> LinearRing</label>&nbsp;
        <input onchange="Q.save()" id="m6_LinearRing_cmt" name="m6_LinearRing_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m6_Polygon" name="m6_Polygon"> Polygon</label>&nbsp;
        <input onchange="Q.save()" id="m6_Polygon_cmt" name="m6_Polygon_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m6_MultiPoint" name="m6_MultiPoint"> MultiPoint</label>&nbsp;
        <input onchange="Q.save()" id="m6_MultiPoint_cmt" name="m6_MultiPoint_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m6_MultiLineString" name="m6_MultiLineString"> MultiLineString</label>&nbsp;
        <input onchange="Q.save()" id="m6_MultiLineString_cmt" name="m6_MultiLineString_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
      <div class="chk" style="margin-bottom: 7px;">
        <label style="display: inline-block; min-width: 130px;"><input onchange="Q.save()" type="checkbox" id="m6_MultiPolygon" name="m6_MultiPolygon"> MultiPolygon</label>&nbsp;
        <input onchange="Q.save()" id="m6_MultiPolygon_cmt" name="m6_MultiPolygon_cmt" type="text" placeholder="Si nécessaire: commentaire" style="width: calc(100% - 160px);" />
      </div>
    </div>
  </div>
</div>


<h2>Caractéristiques des modèles du territoire</h2>

<p>Expliquez brièvement les caractéristiques principales des modèles du territoire rencontrés:</p>

<textarea onchange="Q.save()" id="expl_modterr" name="expl_modterr" style="width: 100%; height: 160px;"></textarea>

<p style="font-size: 85%"><i>Notice: N'oubliez pas de citer vos sources.</i></p>


<h2>Notion de résolution</h2>

<p>Expliquez la notion de <b>résolution</b> dans le cadre des modèles du territoire en cartographie et SIG:</p>

<textarea onchange="Q.save()" id="expl_res" name="expl_res" style="width: 100%; height: 160px;"></textarea>

<p style="font-size: 85%"><i>Notice: N'oubliez pas de citer vos sources.</i></p>

<hr />

<button class="btn btn-sm btn-success">Enregistrer</button>

</form>

<script src="assets/q4/script.js"></script>