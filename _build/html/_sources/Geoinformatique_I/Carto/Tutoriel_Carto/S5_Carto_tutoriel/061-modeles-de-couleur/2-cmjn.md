# Le modèle CMJN

CMJN est l'abréviation de «Cyan Magenta Jaune Noir». En anglais, l'abréviation courante est CMYK ce qui signifie «Cyan Magenta Yellow Key» où «Key» est le noir.

Il s'agit ici d'un modèle de couleur qui est **basé sur la synthèse des couleurs sur papier** comme utilisé notamment pour peindre ou par les imprimantes. Sur le papier, la synthèse de la couleur est différente que celle de la lumière. En effet, si on combine les couleurs primaires sur le papier, on ne va obtenir du blanc. Le modèle CMJN utilise la **synthèse soustractive** par 3 autres couleurs primaires, et en plus le noir. Nous verrons plus loin pourquoi on ajoute le noir aux 3 couleurs primaires. Dans le modèle CMJN, les 3 couleurs primaires sont cyan, magenta et jaune, qui sont en fait les combinaisons des 3 couleurs primaires du modèle RVB.

Pour créer une couleur CMJN, nous allons également utiliser une valeur numérique pour chaque couleur, sauf que nous allons utiliser une valeur entre 0 et 100, valeur qui représente des pourcentages de couverture de chaque couleur. Ainsi, la couleur «cyan» est représentée par le code (100, 0, 0, 0). La dernière valeur représente le noir qui pour le moment sera toujours 0.

Voici les trois couleurs primaires du modèle CMJN ainsi que les combinaisons des couleurs:

<img src="assets/modele-cmyk.png" style="border: 1px solid #ddd;" />

Il y a un petit problème avec ces trois couleurs primaires du modèle CMJN. Les couleurs primaires utilisées pour l'impression ne sont jamais complètement pures. Et du coup, les combinaisons de couleurs ne seront pas parfaites. Ainsi, la combinaison de toutes les trois couleurs est censée donner du noir, mais en réalité, la couleur résultante ne sera pas tout à fait noire, mais plutôt une sorte de gris très foncé. Pour cette raison, le modèle CMJN ajoute le noir comme couleur primaire supplémentaire. Ainsi, nous aurons un modèle à 4 couleurs où le noir pur sera représenté par le code (0, 0, 0, 100) et non pas (100, 100, 100, 0).

Il faut encore noter que l'espace de toutes les couleurs que nous pouvons représenter avec le modèle CMJN ne correspond pas totalement à l'espace des couleurs RVB. Ainsi, un vert pur avec code RVB (0, 255, 0) de pourra pas être représenté dans le modèle CMJN. La couleur la plus proche en CMJN est la couleur (63, 0, 100, 0) qui en RVB correspond à peu près à la couleur avec le code (105, 190, 70) (en réalité, ceci dépend encore de l'imprimante que vous utilisez...). Ces différences dans les modèles de couleurs font d'ailleurs aussi qu'un document couleur imprimé ne sera jamais complètement identique au même document à l'écran. Et c'est la raison pourquoi nos photos sont souvent imprimées avec des couleurs un peu ternes même si elles ont l'air parfaites à l'écran.

Les logiciels de graphisme professionnels savent gérer ce genre de conversion entre modèles de couleurs et afficheront les couleurs aussi bien que possible. Par contre, ceci nécessite que si nous créons un document destiné à l'impression, nous devons donc utiliser le modèle CMJN pour définir les couleurs.
