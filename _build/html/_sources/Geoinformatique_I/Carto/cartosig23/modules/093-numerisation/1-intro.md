# Numérisation de données vectorielles

Les SIG ont généralement des outils puissants d'édition de couches vectorielles, et QGIS n'en fait pas exception. Il y a évidemment la possibilité de créer des nouvelles couches, ou d'éditer des couches existantes.

Un concept important à comprendre dans ce contexte est le fait que pour pouvoir éditer une couche, il faut d'abord passer la couche en **mode édition**. Et une fois que l'édition de la couche est terminée, on va persister les changements dans la couche avant de sortir du mode édition. Ceci évite de faire des changements par erreur des géométries et/ou attributs d'une couche.

La documentation QGIS contient une bonne introduction à la numérisation de couches:  
[https://docs.qgis.org/3.28/fr/docs/training_manual/create_vector_data/create_new_vector.html](https://docs.qgis.org/3.28/fr/docs/training_manual/create_vector_data/create_new_vector.html)

Pour les outils d'édition plus complets on peut se référer au manuel QGIS:  
[https://docs.qgis.org/3.28/fr/docs/user_manual/working_with_vector/editing_geometry_attributes.html](https://docs.qgis.org/3.28/fr/docs/user_manual/working_with_vector/editing_geometry_attributes.html)
