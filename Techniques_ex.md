- [Exercices ch9](#exercices-ch9)
  - [Exercice 9.1](#exercice-91)
  - [Exercice 9.2](#exercice-92)
  - [Exercice 9.3](#exercice-93)
  - [Exercice 9.4](#exercice-94)
  - [Exercice 9.5](#exercice-95)
  - [Exercice 9.6](#exercice-96)
  - [Exercice 9.7](#exercice-97)

# Exercices ch9

## Exercice 9.1

Ecrivez un algorithme qui permette de saisir un nombre quelconque de valeurs, et qui les range au fur et à mesure dans un tableau. Le programme, une fois la saisie terminée, doit dire si les éléments du tableau sont tous consécutifs ou non.
Par exemple, si le tableau est :

|12|13|14|15|16|17|18|
|--|--|--|--|--|--|--|

ses éléments sont tous consécutifs. En revanche, si le tableau est :

|9|10|11|15|16|17|18|
|--|--|--|--|--|--|--|

ses éléments ne sont pas tous consécutifs.

## Exercice 9.2

Ecrivez un algorithme qui trie un tableau dans l’ordre décroissant.
Vous écrirez bien entendu deux versions de cet algorithme, l'une employant le tri par sélection, l'autre le tri à bulles.

## Exercice 9.3

Ecrivez un algorithme qui inverse l’ordre des éléments d’un tableau dont on suppose qu'il a été préalablement saisi (« les premiers seront les derniers… »)

## Exercice 9.4

Ecrivez un algorithme qui permette à l’utilisateur de supprimer une valeur d’un tableau préalablement saisi. L’utilisateur donnera l’indice de la valeur qu’il souhaite supprimer. Attention, il ne s’agit pas de remettre une valeur à zéro, mais bel et bien de la supprimer du tableau lui-même ! Si le tableau de départ était :

|12|8|4|45|64|9|2|
|--|--|--|--|--|--|--|

Et que l’utilisateur souhaite supprimer la valeur d’indice 4, le nouveau tableau sera :

|12|8|4|45|9|2|
|--|--|--|--|--|--|

## Exercice 9.5

Ecrivez l'algorithme qui recherche un mot saisi au clavier dans un dictionnaire. Le dictionnaire est supposé être codé dans un tableau préalablement rempli et trié.

## Exercice 9.6

Écrivez un algorithme qui fusionne deux tableaux (déjà existants) dans un troisième, qui devra être trié.
Attention ! On présume que les deux tableaux de départ sont préalablement triés : il est donc irrationnel de faire une simple concaténation des deux tableaux de départ, puis d'opérer un tri : comme quand on se trouve face à deux tas de papiers déjà triés et qu'on veut les réunir, il existe une méthode bien plus économique (et donc, bien plus rationnelle...)
(on considère qu'il n'y a pas de valeurs communes au deux tableaux)

## Exercice 9.7

La fonction f(x) = x² + x − 1 est strictement croissante sur l'intervalle [0; 2]. et que
pour x=0, f(x) est négatif
pour x=2, f(x) est positif

La dichotomie consiste à évaluer la valeur de f(x) au milieu de l'intervalle [a,b]

- si f($\frac{a + b}{2}$) $\leq$ 0 alors on sait qu'il y a une solution à `f(x)=0` dans l'intervale [$\frac{a + b}{2}$, b]
- sinon f($\frac{a + b}{2}$) > 0 alors on sait qu'il y a une solution à `f(x)=0` dans l'intervale [a, $\frac{a + b}{2}$]

Ainsi, dans les deux cas, on a trouvé un intervalle de longueur moitié dans lequel est située une racine de l'équation `f(x)=0`. On recommence alors avec cet intervalle, et ainsi de suite jusqu'à ce qu'on trouve une approximation qui nous convienne.

Écrire un algorithme qui recherche une solution approchée de l’équation y = 0  sur l’intervalle [0; 2] par dichotomie, avec une précision de 10<sup>-3</sup> cad jusqu'à ce que l'intervalle contenant une solution à `f(x)=0` ait une largeur inférieur à 10<sup>-3<sup>.
