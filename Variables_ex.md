- [Exercices ch3](#exercices-ch3)
  - [Exercice 3.1](#exercice-31)
  - [Exercice 3.2](#exercice-32)
  - [Exercice 3.3](#exercice-33)
  - [Exercice 3.4](#exercice-34)
  - [Exercice 3.5](#exercice-35)
  - [Exercice 3.6](#exercice-36)
  - [Exercice 3.7](#exercice-37)
  - [Exercice 3.8](#exercice-38)
  - [Exercice 3.9](#exercice-39)
  - [Exercice 3.10](#exercice-310)

# Exercices ch3

## Exercice 3.1

Quelles seront les valeurs des variables A et B après exécution des instructions suivantes ?

    Variables A, B en Entier
    Début
        A ← 1
        B ← A + 3
        A ← 3
    Fin

## Exercice 3.2

Quelles sont les valeurs des variables de a, b et c après exécution des instructions suivantes ?

    Variables a, b, c
    Début
        a <- 1
        b <- 2
        c <- 3
        c <- a
        a <- b
        b <- c
    Fin

## Exercice 3.3

Quelles seront les valeurs des variables A, B et C après exécution des instructions suivantes ?

    Variables A, B, C en Entier
    Début
        A ← 5
        B ← 3
        C ← A + B
        A ← 2
        C ← B – A
    Fin

## Exercice 3.4
Quelles seront les valeurs des variables A et B après exécution des instructions suivantes ?

    Variables A, B en Entier
    Début
        A ← 5
        B ← A + 4
        A ← A + 1
        B ← A – 4
    Fin

## Exercice 3.5

Quelles seront les valeurs des variables A, B et C après exécution des instructions suivantes ?

    Variables A, B, C en Entier
    Début
        A ← 3
        B ← 10
        C ← A + B
        B ← A + B
        A ← C
    Fin

## Exercice 3.6

Quelles seront les valeurs des variables A et B après exécution des instructions suivantes ?

    Variables A, B en Entier
    Début
        A ← 5
        B ← 2
        A ← B
        B ← A
    Fin

Moralité : les deux dernières instructions permettent-elles d’échanger les deux valeurs de B et A ? Si l’on inverse les deux dernières instructions, cela change-t-il quelque chose ?


## Exercice 3.7

Plus difficile, mais c’est un classique absolu, qu’il faut absolument maîtriser : écrire un algorithme permettant d’échanger les valeurs de deux variables A et B, et ce quel que soit leur contenu préalable. 


## Exercice 3.8

Une variante du précédent : on dispose de trois variables A, B et C. Ecrivez un algorithme transférant à B la valeur de A, à C la valeur de B et à A la valeur de C (toujours quels que soient les contenus préalables de ces variables).

## Exercice 3.9

Que produit l’algorithme suivant ?

    Variables A, B, C en Caractères
    Début
        A ← "423"
        B ← "12"
        C ← A + B
    Fin

## Exercice 3.10

Que produit l’algorithme suivant ?

    Variables A, B, C en Caractères
    Début
        A ← "423"
        B ← "12"
        C ← A & B
    Fin
