# Le datum

Le **datum** définit :

- Les *paramètres* de l'ellipsoïde de référence
- La *position* de l'ellipsoïde par rapport au centre de masse de la terre (ou une autre référence, comme les points tangents au géoïde)
- L'*orientation* des axes de l'ellipsoïde

Les **datums globaux** permettent d'avoir une assez bonne précision, d'une manière générale, sur l'entier de la surface terrestre.
Les **datums locaux** visent à aligner le sphéroïde aussi précisément que possible pour une région plus petite.

![](assets/datum.png)

Dans l'exemple ci-contre, le *datum local* ***NAD27 (North American Datum)*** s'aligne mieux à la surface réelle de la Terre pour l'Amérique du Nord que le *datum global* ***WGS 84***

Chaque région possède donc un ***datum*** qui représente au mieux sa surface par rapport à la surface de la Terre, pour éviter au maximum les déformations.

Voici quelques *datums* que vous retrouverez souvent durant vos études :

- **Datum suisse :** ***CH1903 / CHTRS95***
- **Datum européen:** ***ETRS89***
- **Datum GPS :** ***WGS 84***
- **Datum Amérique du Nord :** ***NAD27, NAD83***

Lorsque l'on passe d'un *datum* à un autre, les coordonnées de **latitude** et de **longitude** d'un endroit peuvent changer. Il existe des **logiciels de conversion** généralement directement intégrés dans les logiciels SIG.
