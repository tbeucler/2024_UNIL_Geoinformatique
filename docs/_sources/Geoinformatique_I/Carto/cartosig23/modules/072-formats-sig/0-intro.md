# Introduction et logiciels de conversion

Il y a beaucoup de formats SIG différents. Certains de ces formats sont très vieux, ou viennent des logiciels de dessin, d'autres des bases de données. Au final, seulement un nombre relativement restreint de formats de données est couramment utilisé.

Parmi ces formats très utilisés, il y en a certains qui sont très vieux et même propriétaires. C'est le cas du format Shape qui reste un standard important pour les données vectorielles.

Pour palier au problème des nombreux formats et pour éviter des dépendances envers une seule entreprise, l'Open Geospatial Consortium (OGC, [www.ogc.org](https://www.ogc.org/)) a comme objectif de définir des standards et formats ouverts qui permettent l'interopérabilité entre plusieurs logiciels SIG.

De manière générale, nous distinguons les formats pour données vectorielles et les formats raster. Parmi ces formats nous avons notamment:

<table>
<thead><tr><th>Formats vectoriels</th><th>Formats raster</th></tr></thead>
<tbody>
<tr><td>ESRI Shape</td>                   <td>GeoTIFF</td></tr>
<tr><td>ESRI Geodatabase</td>             <td>ESRI Grid</td></tr>
<tr><td>GeoPackage</td>                   <td>ERDAS Imagine</td></tr>
<tr><td>INTERLIS</td>                     <td>ASCII Grid (XYZ)</td></tr>
<tr><td>Bases de données spatiales</td>   <td>...</td></tr>
<tr><td>OpenStreetMap</td>                <td></td></tr>
<tr><td>...</td>                          <td></td></tr>
</tbody>
</table>

## Logiciels de conversion

Généralement, les logiciels SIG sont en mesure de lire et écrire beaucoup de
format différents. Deux logiciels majeurs de conversion de formats SIG existent:

- **[OGR / GDAL](https://gdal.org/)**: OGR est pour les données vectorielles, GDAL pour les données raster. Il s'agit d'une librairie open-source qui est intégré dans beaucoup de logiciels, dont p.ex. QGIS. La liste des formats est impressionnante: plus de 150 formats raster et pas loin de 100 formats vectoriels... OGR/GDAL peut également être utilisé en mode Terminal avec le logiciel `ogr2ogr` pour les format vectoriels, et `gdal_translate` pour les données raster. D'autres utilitaires existent aussi et peuvent être utilisées en mode Terminal ou depuis la boîte GeoProcessing dans QGIS.

- **[FME](https://www.safe.com/fme/)** est un logiciel commercial pour automatiser les conversions de formats SIG et d'autres processus de géo-traitement.

Le premier logiciel est généralement intégré directement dans le logiciel SIG. Une utilisation directe est possible à l'aide de quelques outils en mode terminal. OGR / GDAL n'a pas d'interface graphique. QGIS utilise ce logiciel pour la lecture et l'écriture des données, et ArcGIS en utilise au moins une partie.

FME par contre est un logiciel qui vient avec un environnement complet (et complexe) et il est souvent utilisé dans les administration et grandes entreprises, souvent conjointement avec ArcGIS et QGIS.

---

Par la suite, nous regardons d'abord les principaux formats de données vectorielles, et ensuite les formats raster pour finalement regarder les aspects pratiques de la conversion des formats dans le logiciel SIG.
