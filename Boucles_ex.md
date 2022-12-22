- [Exercices ch7](#exercices-ch7)
  - [Exercice 7.1](#exercice-71)
  - [Exercice 7.2](#exercice-72)
  - [Exercice 7.3](#exercice-73)
  - [Exercice 7.4](#exercice-74)
  - [Exercice 7.5](#exercice-75)
  - [Exercice 7.6](#exercice-76)
  - [Exercice 7.7](#exercice-77)
  - [Exercice 7.8](#exercice-78)
  - [Exercice 7.9](#exercice-79)
  - [Exercice 7.10](#exercice-710)
  - [Exercice 7.11](#exercice-711)
  - [Exercice 7.12](#exercice-712)
  - [Exercice 7.13](#exercice-713)
  - [Exercice 7.14](#exercice-714)
  - [Exercice 7.15](#exercice-715)
  - [Exercice 7.16](#exercice-716)
  - [Exercice 7.17](#exercice-717)
  - [Exercice 7.18](#exercice-718)
  - [Exercice 7.19](#exercice-719)
  - [Exercice 7.20](#exercice-720)
  - [Exercice 7.21](#exercice-721)
  - [Exercice 7.22](#exercice-722)

# Exercices ch7

## Exercice 7.1

Ecrire un algorithme qui demande à l’utilisateur un nombre compris entre 1 et 3 jusqu’à ce que la réponse convienne.

## Exercice 7.2

Ecrire un algorithme qui demande un nombre compris entre 10 et 20, jusqu’à ce que la réponse convienne. En cas de réponse supérieure à 20, on fera apparaître un message : « Plus petit ! », et inversement, « Plus grand ! » si le nombre est inférieur à 10.

## Exercice 7.3

Ecrire un algorithme qui demande un nombre de départ, et qui ensuite affiche les dix nombres suivants. Par exemple, si l'utilisateur entre le nombre 17, le programme affichera les nombres de 18 à 27.

## Exercice 7.4

Réécrire l'algorithme précédent, en utilisant cette fois l'instruction Pour

## Exercice 7.5

Ecrire un algorithme qui demande un nombre de départ, et qui ensuite écrit la table de multiplication de ce nombre, présentée comme suit (cas où l'utilisateur entre le nombre 7) :

    Table de 7 :
    7 x 1 = 7
    7 x 2 = 14
    7 x 3 = 21
    …
    7 x 10 = 70

## Exercice 7.6

Ecrire un algorithme qui demande un nombre de départ, et qui calcule la somme des entiers jusqu’à ce nombre. Par exemple, si l’on entre 5, le programme doit calculer :
1 + 2 + 3 + 4 + 5 = 15
NB : on souhaite afficher uniquement le résultat, pas la décomposition du calcul.

## Exercice 7.7

Ecrire un algorithme qui demande un nombre de départ, et qui calcule sa factorielle.
NB : la factorielle de 8, notée 8 !, vaut
1 x 2 x 3 x 4 x 5 x 6 x 7 x 8

## Exercice 7.8

Ecrire un algorithme qui demande successivement 20 nombres à l’utilisateur, et qui lui dise ensuite quel était le plus grand parmi ces 20 nombres :

    Entrez le nombre numéro 1 : 12
    Entrez le nombre numéro 2 : 14
    etc.
    Entrez le nombre numéro 20 : 6
    Le plus grand de ces nombres est  : 14

Modifiez ensuite l’algorithme pour que le programme affiche de surcroît en quelle position avait été saisie ce nombre :

    C’était le nombre numéro 2

## Exercice 7.9

Réécrire l’algorithme précédent, mais cette fois-ci on ne connaît pas d’avance combien l’utilisateur souhaite saisir de nombres. La saisie des nombres s’arrête lorsque l’utilisateur entre un zéro.

## Exercice 7.10

Lire la suite des prix (en euros entiers et terminée par zéro) des achats d’un client. Calculer la somme qu’il doit, lire la somme qu’il paye, et simuler la remise de la monnaie en affichant les textes "10 Euros", "5 Euros" et "1 Euro" autant de fois qu’il y a de coupures de chaque sorte à rendre.

Exemple :

    Saisie de : 20 puis 4 puis de 0 (pour indiquer la fin de saisie des prix)
    Affiche la somme due : 24
    Saisie de la somme payée : 50
    Affiche :
        Rendu de la monnaie (26 €)
            Billets de 10 € : 2
            Billets de 5 € : 1
            Pièces de 1 € : 1

## Exercice 7.11

Écrire un algorithme qui permette de connaître ses chances de gagner au tiercé, quarté, quinté et autres.
On demande à l’utilisateur le nombre de chevaux partants, et le nombre de chevaux joués.
Les deux messages affichés devront être :

    Dans l’ordre : une chance sur X de gagner
    Dans le désordre : une chance sur Y de gagner

X et Y nous sont donnés par la formule suivante, si n est le nombre de chevaux partants et p le
nombre de chevaux joués (on rappelle que le signe ! signifie "factorielle") :

    X = n ! / (n - p) !
    Y = n ! / (p ! * (n – p) !)

NB : cet algorithme peut être écrit d’une manière simple, mais relativement peu performante. Ses performances peuvent être singulièrement augmentées par une petite astuce. Vous commencerez par écrire la manière la plus simple, puis vous identifierez le problème, et écrirez une deuxième version permettant de le résoudre.
(ce n'est pas grave si vous n'arrivez pas à effectuer la partie simplification)

## Exercice 7.12

Que fait cet algorithme :

    Variables nb, somme, d, tir en Entier
    début
        nb <- 1000
        somme <- 0
        répéter nb fois
            tir <- 1
            d  <- une valeur entière aléatoire entre 1 et 6
            répéter jusqu’à d = 6
                tir <- tir + 1
                d <- valeur entière aléatoire entre 1 et 6
            fin
            somme <- somme + tir
        fin
        Ecrire somme/nb
    fin

## Exercice 7.13

Ecrire un algorithme qui lise un nombre entier positif inférieur à 20 et qui affiche le décompte jusqu'à zéro.

## Exercice 7.14

L’algorithme ci-dessous calcule 10!
Quelle est l'erreur ?

    Variable res, i en Entier
    début
        res <- 1
        i <- 1
        tant que i ≤ 10 faire
            Donner à res la valeur res ∗ i
        fin
        Afficher res
    fin

## Exercice 7.15

L’algorithme ci-dessous calcule 10!
Quelle est l'erreur ?

    début
        Donner à res la valeur 1
        tant que i ≤ 10 faire
            Donner à res la valeur res ∗ i
            Donner à i la valeur i + 1
        fin
        Afficher res
    fin

## Exercice 7.16

L’algorithme ci-dessous calcule 10!
Quelle est l'erreur ?

    début
        Donner à res la valeur 1
        Donner à i la valeur 1
        tant que i ≤ 10 faire
            Donner à i la valeur 1
            Donner à res la valeur res ∗ i
            Donner à i la valeur i + 1
        fin
        Afficher res
    fin

## Exercice 7.17

L’algorithme ci-dessous calcule 10!
Quelle est l'erreur ?

    début
        Donner à res la valeur 1
        Donner à i la valeur 11
        tant que i ≤ 10 faire
            Donner à res la valeur res ∗ i
            Donner à i la valeur i + 1
        fin
        Afficher res
    fin

## Exercice 7.18

Que fait l’algorithme ci-dessous ?

    début
        Donner à a la valeur 0 
        Donner à b la valeur 10
        Donner à N la valeur 50 
        Donner à pas la valeur (b − a)/N
        Donner à x la valeur a 
        Donner à max la valeur 2x² − 5x + 3
        pour i de 1 à N faire
            Donner à x la valeur x + pas
            Donner à y la valeur 2x² − 5x + 3
            si max < y alors
                Donner à max la valeur y
            fin
        fin
        Afficher max
    fin

## Exercice 7.19

Que fait l’algorithme ci-dessous ?

    début
        Lire la valeur de N
        Donner à i la valeur 0
        Donner à n la valeur 1
        tant que n ≤ N faire
            Donner à n la valeur 2 ∗ n
            Donner à i la valeur i + 1
        fin
        Afficher i − 1
    fin

## Exercice 7.20

Que se passe-t-il si dans l'exercice précédent on choisit N = 0 ?
Comment réparer le problème ?

## Exercice 7.21

Écrire un algorithme qui détermine si un nombre lu au clavier est un nombre premier.

Un nombre entier naturel (supérieur ou égal à 2) est un nombre premier s'il admet exactement 2 diviseurs : 1 et lui-même.
Exemple : 2, 3, 5, 7, 11, 13, 17, 19 … sont des nombres premiers. Il en existe une infinité.

## Exercice 7.22

Pour déterminer si un nombre entier naturel n supérieur ou égal 2 est un nombre premier, on doit chercher un diviseur de n parmi les nombres premiers successifs (2, 3, 5, 7, 11 …) jusqu'à la valeur $\sqrt{n}$.
En effet, si n n'admet aucun diviseur parmi les nombres premiers successifs jusqu'à la valeur $\sqrt{n}$, il n'en admettra pas non plus entre $\sqrt{n}$ et n car les diviseurs d'un nombre vont par paires : l'un compris entre 2 et $\sqrt{n}$, et l'autre compris entre $\sqrt{n}$ et n.
Si n n'admet aucun diviseur parmi les nombres premiers successifs jusqu'à la valeur $\sqrt{n}$, c'est donc un nombre premier.

Améliorer l'exercice précédent en conséquence.

