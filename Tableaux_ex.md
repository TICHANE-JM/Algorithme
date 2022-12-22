- [Exercices ch8](#exercices-ch8)
  - [Exercice 8.1](#exercice-81)
  - [Exercice 8.2](#exercice-82)
  - [Exercice 8.3](#exercice-83)
  - [Exercice 8.4](#exercice-84)
  - [Exercice 8.5](#exercice-85)
  - [Exercice 8.6](#exercice-86)
  - [Exercice 8.7](#exercice-87)
  - [Exercice 8.8](#exercice-88)
  - [Exercice 8.9](#exercice-89)
  - [Exercice 8.10](#exercice-810)
  - [Exercice 8.11](#exercice-811)
  - [Exercice 8.12](#exercice-812)
  - [Exercice 8.13](#exercice-813)
  - [Exercice 8.14](#exercice-814)
  - [Exercice 8.15](#exercice-815)
  - [Exercice 8.16](#exercice-816)
  - [Exercice 8.17](#exercice-817)
  - [Exercice 8.18](#exercice-818)
  - [Exercice 8.19](#exercice-819)
  - [Exercice 8.20](#exercice-820)
  - [Exercice 8.21](#exercice-821)
  - [Exercice 8.22](#exercice-822)

# Exercices ch8

## Exercice 8.1

Ecrire un algorithme qui déclare et remplisse un tableau de 7 valeurs numériques en les mettant toutes à zéro.


## Exercice 8.2

Ecrire un algorithme qui déclare et remplisse un tableau contenant les six voyelles de l’alphabet latin.

## Exercice 8.3

Ecrire un algorithme qui déclare un tableau de 9 notes, dont on fait ensuite saisir les valeurs par l’utilisateur.

## Exercice 8.4

Que produit l’algorithme suivant ?

    Tableau Nb[5] en Entier
    Variable i en Entier
    Début
        Pour i ← 0 à 5
            Nb[i] ← i * i
        i suivant
        Pour i ← 0 à 5
            Ecrire Nb[i]
        i suivant
    Fin

Peut-on simplifier cet algorithme avec le même résultat ?

## Exercice 8.5

Que produit l’algorithme suivant ?

    Tableau N[6] en Entier
    Variables i, k en Entier
    Début
        N[0] ← 1
        Pour k ← 1 à 6
            N[k] ← N[k-1] + 2
        k Suivant
        Pour i ← 0 à 6
            Ecrire N[i]
        i suivant
    Fin

Peut-on simplifier cet algorithme avec le même résultat ?


## Exercice 8.6

Que produit l’algorithme suivant ?

    Tableau Suite[7] en Entier
    Variable i en Entier
    Début
        Suite[0] ← 1
        Suite[1] ← 1
        Pour i ← 2 à 7
            Suite[i] ← Suite[i-1] + Suite[i-2]
        i suivant
        Pour i ← 0 à 7
            Ecrire Suite[i]
        i suivant
    Fin

## Exercice 8.7

Ecrivez la fin de l’algorithme 8.3 afin que le calcul de la moyenne des notes soit effectué et affiché à l’écran.

## Exercice 8.8

Ecrivez un algorithme permettant à l’utilisateur de saisir un nombre quelconque de valeurs, qui devront être stockées dans un tableau. L’utilisateur doit donc commencer par entrer le nombre de valeurs qu’il compte saisir. Il effectuera ensuite cette saisie. Enfin, une fois la saisie terminée, le programme affichera le nombre de valeurs négatives et le nombre de valeurs positives.

## Exercice 8.9

Ecrivez un algorithme calculant la somme des valeurs d’un tableau (on suppose que le tableau a été préalablement saisi)

## Exercice 8.10

Ecrivez un algorithme constituant un tableau, à partir de deux tableaux de même longueur préalablement saisis. Le nouveau tableau sera la somme des éléments des deux tableaux de départ.

Tableau 1 :
| 4 | 8 | 7 | 9 | 1 | 5 | 4 | 6 |
|-|-|-|-|-|-|-|-|

Tableau 2 :
|7| 6| 5| 2| 1| 3| 7 |4|
|-|-|-|-|-|-|-|-|

Tableau à constituer :
|11| 14| 12| 11| 2 |8| 11| 10|
|-|-|-|-|-|-|-|-|

## Exercice 8.11

Toujours à partir de deux tableaux précédemment saisis, écrivez un algorithme qui calcule le schtroumpf des deux tableaux. Pour calculer le schtroumpf, il faut multiplier chaque élément du tableau 1 par chaque élément du tableau 2, et additionner le tout. Par exemple si l'on a :
Tableau 1 :
|4| 8| 7| 12|
|-|-|-|-|

Tableau 2 :
|3| 6|
|-|-|

Le Schtroumpf sera :
3 *4 + 3* 8 + 3 *7 + 3* 12 + 6 *4 + 6* 8 + 6 *7 + 6* 12 = 279

## Exercice 8.12

Ecrivez un algorithme qui permette la saisie d’un nombre quelconque de valeurs, sur le principe de l’exercice 8.8. Toutes les valeurs doivent être ensuite augmentées de 1, et le nouveau tableau sera affiché à l’écran.

## Exercice 8.13

Ecrivez un algorithme permettant, toujours sur le même principe, à l’utilisateur de saisir un nombre déterminé de valeurs. Le programme, une fois la saisie terminée, renvoie la plus grande valeur en précisant quelle position elle occupe dans le tableau. On prendra soin d’effectuer la saisie dans un premier temps, et la recherche de la plus grande valeur du tableau dans un second temps.

## Exercice 8.14

Toujours et encore sur le même principe, écrivez un algorithme permettant, à l’utilisateur de saisir les notes d'une classe. Le programme, une fois la saisie terminée, renvoie le nombre de ces notes supérieures à la moyenne **de la classe**.

## Exercice 8.15

Écrire un algorithme de machine à voter : on fait voter des électeurs tant qu’il y en a entre un candidat A et un candidat B. À la fin, on affiche le nom du vainqueur (s’il y en a un). L’algorithme doit être fiable à 100% et ne doit pas permettre d’erreur de saisie.

## Exercice 8.16

Ecrire un algorithme permettant le calcul du nombre d'occurences d'un élément donné dans un tableau

## Exercice 8.17

Ecrire un algorithme permettant le calcul de la moyenne et du minimum des éléments d'un tableau.

## Exercice 8.18

Ecrire un algorithme permettant de tester si un tableau est trié (on ne demande pas de trier)

## Exercice 8.19

Ecrire l'algorithme effectuant le décalage des éléments d'un tableau.

Exemple :
• Tableau initial :
|D|E|C|A|L|A|G|E|
|-|-|-|-|-|-|-|-|

• Tableau modifié (décalage à gauche)

|E|C|A|L|A|G|E|D|
|-|-|-|-|-|-|-|-|

## Exercice 8.20

Ecrire un algorithme qui calcule le plus grand écart dans un tableau (l'écart est la valeur absolue de la différence de deux éléments). Le tableau ne contiendra que des nombre strictement positifs.

Exemple :
|4|8|1|16|
|-|-|-|-|

Le plus grand écart est de : 15

## Exercice 8.21

Écrire un algorithme qui remplit une liste de 10 nombres entiers entre 0 et 9 au hasard, puis calcule la somme des éléments de la liste

## Exercice 8.22

Le code de César consiste à crypter un message en remplaçant chaque lettre par celle qui se trouve 3 rangs à droite dans l’alphabet (et bien sûr "x","y" et "z" deviennent respectivement "a", "b" et "c").
Par exemple "exemple" devient "hahpsoh".
Écrire un algorithme qui crypte un mot entré au clavier (le mot sera en bas de casse) en utilisant le code de César.
Ne pas utiliser le code ASCII, utiliser un simple tableau de longueur 26.
