# Calcul d'indicateur dans Excel ou LibreOffice Calc

Cette module explique comment calculer les différents indicateurs que vous pouvez utiliser pour le TP1. Les explications sont données avec un jeu de données sur une autre région, mais le principe est strictement identique.

Pour le TP1, vous allez choisir librement un indicateur qui est listé dans le fichier Excel des données du TP.


## Indicateur: une courte définition

Un indicateur permet de quantifier et puis analyser et visualiser un phénomène localisé dans l'espace, à travers des mesures directes ou indirectes. Nous avons à disposition des données démographiques et économiques. L'indicateur permet de mettre en relation deux valeurs, d'où sa nature relative. Un indicateur peut être aussi simple qu'un pourcentage, par exemple la part de population très âgée. Ou il peut être un peu plus élaboré, comme les indices de localisation qui comparent un ratio d'une région avec une région de référence (généralement la totalité de la région étudiée).

Étant une valeur relative, ces indicateurs se prêtent à une carte choroplèthe, éventuellement en combinaison avec des symboles proportionnels.


## Exemples d'indicateurs

Ci-dessous il y a quelques indicateurs démographiques typiques. Pour le TP1, vous allez calculer un indicateur identique ou au moins similaire sur la base des données disponibles. Consultez également l'onglet «indicateurs» du fichier Excel du TP1 ainsi que les vidéos d'explications ci-dessous.

**Indicateur 1: Croissance moyenne annuelle de la population 2011 – 2014, en %**

$$( (\frac{P_{t1}}{P_{t0}})^\frac{1}{N} - 1) \cdot 100$$

où $P_{t1}$ est la population en 2014, $P_{t0}$ la population en 2010, et $N$ le nombre d'année entre 2014 et 2011 (donc 3).

Il s'agit ici de la croissance annuelle moyenne de la population, en pourcentages. La croissance annuelle est normalisée pour pouvoir comparer des périodes de temps de longueurs différentes.

Si la croissance de la population est très faible, on peut aussi changer les unités en pour-milles (donc multiplier la valeur en pourcentage par 10).


**Indicateur 2: Rapport de dépendance**

$$100 \cdot \frac{\text{Population 0-15ans} + \text{Population 65 ans et plus}}{\text{Population 15-64 ans}}$$

Le rapport de dépendance mesure combien de personnes dans une tranche d'âge avant ou après une activité professionnelle potentielle. Le rapport de dépendance n'a pas d'unité (ce ne sont pas des pourcentages). Une valeur de 50 veut p.ex. dire qu'il y 2 personnes potentiellement active pour 1 personne en dehors de la tranche d'âge des actifs.

Attention: le rapport de dépendance n'a pas d'unité. Les valeurs ne sont donc pas des pourcentages, malgré la multiplication par 100. Ceci parce que la *Popluation 0-15 ans* et la *Population 65 ans et plus* ne sont pas contenues dans *Population 15-64 ans* (qui serait la population de référence si c'était un pourcentage).


**Indicateur 3: Part de la population très âgée**

$$\frac{\text{Population 85+}}{\text{Population totale}} \cdot 100$$

Ce sont bel et bien des pourcentages ici, car la *population 85+* est contenue dans la *population totale*.

Suivant comment, l'indication *très âgée* n'est pas la même selon le pays. Typiquement, dans un pays en développement, l'espérance de vie est moins élevée et la notion de *personne âgée* un peu différente.


**Indicateur 4: Ratio jeunes / vieux**

$$\frac{\text{Population 0-14}}{\text{Population 65+}} \cdot 100$$

Comme le rapport de dépendance, ce ratio n'a pas d'unité, il n'est donc pas en pourcentages. Une valeur de 100 indique parité entre jeunes et vieux. Une valeur de plus de 100 indique qu'il y a plus de jeunes que de vieux.



## Vidéos d'explication pour le calcul d'indicateurs.

Les vidéos ci-dessous expliquent le calcul de différents indicateurs, en vue du TP1.

**Explications générales:**  

+++
type: video
id: explications-generales
src: assets/calcul-indicateurs-1-explications.mp4
+++

---

**Exemple 1: Calcul du pourcentage de catholiques:**

+++
type: video
id: propcath
src: assets/calcul-indicateurs-2-ex1-catholiques.mp4
+++

---

**Exemple 2: Calcul du rapport de dépendance:**

+++
type: video
id: rapdep
src: assets/calcul-indicateurs-3-ex2-rapdep.mp4
+++

---

**Exemple 3: Calcul de la croissance annuelle moyenne de la population:**

+++
type: video
id: tcam
src: assets/calcul-indicateurs-4-ex3-tcam-pop.mp4
+++

---

**_Important:_ calcul de la moyenne sur toute la région d'étude:**

+++
type: video
id: moyenne-region
src: assets/calcul-indicateurs-5-moyenne-region.m4v
+++
