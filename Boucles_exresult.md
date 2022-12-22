- [**Exercices ch7**](#exercices-ch7)
  - [**Exercice 7.1**](#exercice-71)
  - [**Exercice 7.2**](#exercice-72)
  - [**Exercice 7.3**](#exercice-73)
  - [**Exercice 7.4**](#exercice-74)
  - [**Exercice 7.5**](#exercice-75)
  - [**Exercice 7.6**](#exercice-76)
  - [**Exercice 7.7**](#exercice-77)
  - [**Exercice 7.8**](#exercice-78)
  - [**Exercice 7.9**](#exercice-79)
  - [**Exercice 7.10**](#exercice-710)
  - [**Exercice 7.11**](#exercice-711)
  - [**Exercice 7.12**](#exercice-712)
  - [**Exercice 7.13**](#exercice-713)
  - [**Exercice 7.14**](#exercice-714)
  - [**Exercice 7.15**](#exercice-715)
  - [**Exercice 7.16**](#exercice-716)
  - [**Exercice 7.17**](#exercice-717)
  - [**Exercice 7.18**](#exercice-718)
  - [**Exercice 7.19**](#exercice-719)
  - [**Exercice 7.20**](#exercice-720)
  - [**Exercice 7.21**](#exercice-721)
  - [**Exercice 7.22**](#exercice-722)

# <span style="color: #1a02d6"><ins>**Exercices ch7**</ins></span>

## <span style="color: #1a02d6"><ins>**Exercice 7.1**</ins></span>

Ecrire un algorithme qui demande à l’utilisateur un nombre compris entre 1 et 3 jusqu’à ce que la réponse convienne.

```
Variable 
Nb en Entier

Début
    Nb <- 0
    Ecrire "Veuillez saisir un nombre entre 1 et 3"
    TantQue Nb < 1 ou Nb > 3
        Lire Nb
        Si Nb < 1 ou Nb > 3 Alors
            Ecrire "Erreur dans la saisie. Veuillez recommencer”
        FinSi
    FinTantQue
Fin
```

## <span style="color: #1a02d6"><ins>**Exercice 7.2**</ins></span>

Ecrire un algorithme qui demande un nombre compris entre 10 et 20, jusqu’à ce que la réponse convienne. En cas de réponse supérieure à 20, on fera apparaître un message : « Plus petit ! », et inversement, « Plus grand ! » si le nombre est inférieur à 10.

```
Variables
Nb en Entier

Début
    Nb <- 0
    Ecrire "Entrez un nombre entre 10 et 20"
    TantQue Nb < 10 ou Nb> 20
        Lire Nb
        Si Nb < 10 Alors
            Ecrire "Plus grand !"
        SinonSi Nb > 20 Alors
            Ecrire "Plus petit !"
        FinSi
    FinTantQue
Fin
```


## <span style="color: #1a02d6"><ins>**Exercice 7.3**</ins></span>

Ecrire un algorithme qui demande un nombre de départ, et qui ensuite affiche les dix nombres suivants. Par exemple, si l'utilisateur entre le nombre 17, le programme affichera les nombres de 18 à 27.

```
Variables 
Nb, i en Entier

Début
    Ecrire "Veuillez saisir un nombre : "
    Lire Nb
    i <- 0
    Ecrire "Les Dix nombres suivants le nombre saisi sont : "
    TantQue i < 10
        i <- i + 1
        Ecrire N + i
    FinTantQue
Fin
```

## <span style="color: #1a02d6"><ins>**Exercice 7.4**</ins></span>

Réécrire l'algorithme précédent, en utilisant cette fois l'instruction Pour

```
Variables
Nb, i en Entier

Début
    Ecrire "Veuillez saisir un nombre : "
    Lire Nb
    Ecrire "Les Dix nombres suivants le nombre saisi sont : "
    Pour i <- 1 à 10 pas 1 Faire
        Ecrire Nb + i
    finPour
Fin
```


## <span style="color: #1a02d6"><ins>**Exercice 7.5**</ins></span>

Ecrire un algorithme qui demande un nombre de départ, et qui ensuite écrit la table de multiplication de ce nombre, présentée comme suit (cas où l'utilisateur entre le nombre 7) :
```
Table de 7 :
7 x 1 = 7
7 x 2 = 14
7 x 3 = 21
…
7 x 10 = 70
```
<span style="color: #26B260">**Réponse :**</span>

```
Variables 
Nb, i en Entier

Début
    Ecrire "Veuillez saisir un nombre : "
    Lire Nb
    Ecrire "La table de multiplication de ce nombre est : "
    Pour i <- 1 à 10 pas 1 Faire
        Ecrire Nb, " x ", i, " = ", Nb*i
    FinPour
Fin
```


## <span style="color: #1a02d6"><ins>**Exercice 7.6**</ins></span>

Ecrire un algorithme qui demande un nombre de départ, et qui calcule la somme des entiers jusqu’à ce nombre. Par exemple, si l’on entre 5, le programme doit calculer :
1 + 2 + 3 + 4 + 5 = 15

<ins>NB </ins>: on souhaite afficher uniquement le résultat, pas la décomposition du calcul.

```
Variables 
Nb, i, Somme en Entier

Début
    Ecrire "Veuillez saisir un nombre : "
    Lire Nb
    Somme <- 0
    Pour i <- 1 à Nb pas 1 Faire
        Somme <- Somme + i
    FinPour
    Ecrire "La somme des entiers jusqu'au nombre saisi est : ", Somme
Fin
```

## <span style="color: #1a02d6"><ins>**Exercice 7.7**</ins></span>

Ecrire un algorithme qui demande un nombre de départ, et qui calcule sa factorielle.

<ins>NB </ins>: la factorielle de 8, notée 8 !, vaut
1 x 2 x 3 x 4 x 5 x 6 x 7 x 8

```
Variables 
Nb, i, Facto en Entier

Début
    Ecrire "Veuillez saisir un nombre : "
    Lire Nb
    Facto <- 1
    Pour i <- 2 à Nb
        Facto ← Facto * i
    i++
    Ecrire "La factorielle du nombre saisi est : ", Facto
Fin
```


## <span style="color: #1a02d6"><ins>**Exercice 7.8**</ins></span>

Ecrire un algorithme qui demande successivement 20 nombres à l’utilisateur, et qui lui dise ensuite quel était le plus grand parmi ces 20 nombres :
```
Entrez le nombre numéro 1 : 12
Entrez le nombre numéro 2 : 14
etc...
Entrez le nombre numéro 20 : 6
Le plus grand de ces nombres est  : 14
```

Modifiez ensuite l’algorithme pour que le programme affiche de surcroît en quelle position avait été saisie ce nombre :
```
C’était le nombre numéro 2
```
**Réponse :**


```
Variables 
Nb, i, PlusG en Entier

Début
    PlusG ← 0
    Pour i <- 1 à 20 pas  1 Faire
        Ecrire "Veuillez saisir un nombre : "
        Lire Nb
        Si i = 1 ou Nb > PlusG Alors
            PlusG <- N
        FinSi
    FinPour
    Ecrire "Le plus grand parmi ces 20 nombres était : ", PlusG
Fin
```
<span style="color: #26B260">**Rajout de la position du chiffre :**</span>
```
Variables 
Nb, i, PlusG, PosPlusG en Entier

Début
    PlusG <- 0
    Pour i <- 1 à 20 pas 1 Faire
        Ecrire "Veuillez saisir un nombre : "
        Lire Nb
        Si i = 1 ou Nb > PlusG Alors
            PlusG <- Nb
            PosPlusG <- i
        FinSi
    FinPour
    Ecrire "Le plus grand parmi ces 20 nombres était : ", PlusG
    Ecrire "C'était le nombre numéro ", PosPlusG
Fin
```

## <span style="color: #1a02d6"><ins>**Exercice 7.9**</ins></span>

Réécrire l’algorithme précédent, mais cette fois-ci on ne connaît pas d’avance combien l’utilisateur souhaite saisir de nombres. La saisie des nombres s’arrête lorsque l’utilisateur entre un zéro.

```
Variables 
Nb, i, PlusG, PosPlusG en Entier

Début
    Nb <- 1
    i <- 0
    PlusG <- 0
    TantQue Nb <> 0
        Ecrire "Veuillez saisir un nombre : "
        Lire Nb
        i <- i + 1
        Si i = 1 ou Nb > PlusG Alors
            PlusG <- Nb
            PosPlusG <- i
        FinSi
    FinTantQue
    Ecrire "Le plus grand parmi ces nombres était : ", PlusG
    Ecrire "Il a été saisi en  ", PosPlusG ,"ème position"
Fin
```


## <span style="color: #1a02d6"><ins>**Exercice 7.10**</ins></span>

Lire la suite des prix (en euros entiers et terminée par zéro) des achats d’un client. Calculer la somme qu’il doit, lire la somme qu’il paye, et simuler la remise de la monnaie en affichant les textes "**10 Euros**", "**5 Euros**", "**1 Euro**", "**50 centimes**", "**10 centimes**", "**5 centimes**" et "**1 centime**" autant de fois qu’il y a de coupures de chaque sorte à rendre.

<ins>**Exemple**:</ins>
```
Saisie de : 20.11 puis 4 puis de 0 (pour indiquer la fin de saisie des prix)
Affiche la somme due : 24.11
Saisie de la somme payée : 50
Affiche :
    Rendu de la monnaie (25.89 €)
        Billets de 10 € : 2
        Billets de 5 € : 1
        Pièces de 1 € : 0
        Pièces de 0,50 € : 1
        Pièces de 0,10 € : 3
        Pièces de 0,05 € : 1
        Pièces de 0,01 € : 4

```
<span style="color: #26B260">**Réponse :**</span>

```
Variables
Mont, MontVer, Rend, Cpt en réels

Début
    Ecrire "Entrez le montant à payer : "
    Lire Mont
    Ecrire "Entrez le montant donné par l'acheteur : "
    Lire MontVer
    Rend <- MontVer - Mont
    Cpt <- 0

    Tant que MontVer >= 10
        Rend <- Rend - 10
        Cpt <- Cpt + 1
        Ecrire "Billets de 10 € : ", Cpt
    fin Tantque

    Rend <- Rend-(Cpt * 10)
    Cpt <- 0
 
    Tant que Rend >= 5
        Rend <- Rend - 5
        Cpt <- Cpt + 1
        Ecrire "billets de 5 euros" , Cpt
    fin Tantque
 
    Rend <- Rend - (Cpt * 5)
    Cpt <-0
 
    Tant que Rend >= 1
        Rend <- Rend - 1
        Cpt <- Cpt + 1
        Ecrire "pièces de 1 euros" , Cpt
    fin Tantque
 
    Rend <- Rend -(Cpt * 1)
    Cpt <- 0
 
    Tant que Rend >= 0.50
        Rend <- Rend - 0.50
        Cpt <- Cpt + 1
        Ecrire "pièces de 50 centimes" , Cpt
    fin Tantque
 
    Rend <- Rend-(Cpt * 0.50)
    Cpt <- 0
 
   Tant que  Rend >= 0.10
        Rend <- Rend - 0.10
        Cpt <- Cpt + 1
        Ecrire "pièces de 10 centimes" , Cpt
    fin Tant que
     
    Rend <- Rend - (Cpt * 0.10)
    Cpt <- 0
 
    Tant que Rend >= 0.05
        Rend = Rend - 0.05
        Cpt = Cpt + 1
        Ecrire "pièces de 5 centimes" , Cpt
    fin Tantque
 
    Rend <- Rend -(Cpt * 0.05)
    Cpt <- 0
 
    Tant que Rend >= 0.01
        Rend <- Rend - 0.01
        Cpt <- Cpt + 1
        Ecrire "pièces de 1 centimes" , Cpt
    fin Tant que
fin
```

## <span style="color: #1a02d6"><ins>**Exercice 7.11**</ins></span>

Écrire un algorithme qui permette de connaître ses chances de gagner au tiercé, quarté, quinté et autres.
On demande à l’utilisateur le nombre de chevaux partants, et le nombre de chevaux joués.
Les deux messages affichés devront être :
```
Dans l’ordre : une chance sur X de gagner
Dans le désordre : une chance sur Y de gagner
```

**X** et **Y** nous sont donnés par la formule suivante, si **n** est le **nombre de chevaux partants** et 
**p** le
**nombre de chevaux joués** (on rappelle que le signe ! signifie "factorielle") :
```
X = n ! / (n -p) !
Y = n ! / (p ! * (n – p) !)
```

<ins>**NB :**</ins> cet algorithme peut être écrit d’une manière simple, mais relativement peu performante. Ses performances peuvent être singulièrement augmentées par une petite astuce. Vous commencerez par écrire la manière la plus simple, puis vous identifierez le problème, et écrirez une deuxième version permettant de le résoudre.
(ce n'est pas grave si vous n'arrivez pas à effectuer la partie simplification)

```
Variables 
ChevPart, ChevJoue, i, XYNumé, XDéno, YDéno en Entier

Début 
    Ecrire "Entrez le nombre de chevaux partants : "
    Lire ChevPart
    Ecrire "Entrez le nombre de chevaux joués : "
    Lire ChevJoue
    XYNumé <- 1
    Pour i <- 2 à ChevPart pas 1 Faire             % Boucle 1 %
        XYNumé <- XYNumé * i
    FinPour
    XDéno <- 1
    Pour i <- 2 à ChevPart-ChevJoue pas 1 Faire     % Boucle 2 %
        XDéno ← XDéno * i
    FinPour
    YDéno <- 1
    Pour i <- 2 à ChevJoue pas 1 Faire             % Boucle 3 %
        YDéno <- YDéno * i
    FinPour
    Ecrire "Dans l’ordre, une chance sur ", XYNumé / XDéno
    Ecrire "Dans le désordre, une sur ", XYNumé / (XDéno * YDéno)
Fin
```
<span style="color: #26B260">**simplification :**</span> 

```
Variables 


Début



Fin
```

## <span style="color: #1a02d6"><ins>**Exercice 7.12**</ins></span>

Que fait cet algorithme :
```
Variables 
nb, somme, d, tir en Entier

Début
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
```
<span style="color: #26B260">Cet algorithme détermne en 1000 tentative, combien de fois il faut lancer les dés par tentative pour obtenir 6.</span>

```
Variables nb, i, somme, tir en Entier

Début
    nb <- 1000
    somme <- 0
    Pour i <- 1 à nb pas  1 Faire
        tir <- 1
        d <- valeur aléatoire entre 1 et 6
        Si d = 6 Alors
            tir <- tir + 1
        FinSi
        somme <- somme + tir
    FinPour
    Ecrire somme/nb
fin
```
<span style="color: #26B260">Celui-ci calcule la fréquence de la face 6 obtenue sur une série de 1000 lancers du dé.</span>

## <span style="color: #1a02d6"><ins>**Exercice 7.13**</ins></span>

Ecrire un algorithme qui lit un nombre entier positif inférieur à 20 et qui affiche le décompte jusqu'à zéro.

```
Variables
Nb en Entier

Début
    Nb <- 21
    Ecrire "Veuillez saisir un Nombre entier positif inférieur à 20 :"
    Tant que Nb < 0 ET Nb > 20
        Lire Nb
        Si Nb < 0 ET Nb > 20
            Ecrire "Ce nombre n'est pas dans l'intervalle, veuillez ressaisir :"
        Sinon
            Tant que n >= 0
                Ecrire n
                n <- n - 1
            finTantque
            Ecrire Nb
        FinSi
    fin Tantque
fin
```
## <span style="color: #1a02d6"><ins>**Exercice 7.14**</ins></span>

L’algorithme ci-dessous calcule 10!
Quelle est l'erreur ?
```
Variable 
res, i en Entier
    
Début
    res <- 1
    i <- 1
    Tant que i ≤ 10 faire
        Donner à res la valeur res ∗ i
    fin
    Afficher res
fin
```
<span style="color: #26B260">Non l'algorithme ne donne pas le résultat 10!, il manque l'incrémentation de i dans le tant que</span>


## <span style="color: #1a02d6"><ins>**Exercice 7.15**</ins></span>

L’algorithme ci-dessous calcule 10!
Quelle est l'erreur ?
```
début
    Donner à res la valeur 1
    Tant que i ≤ 10 faire
        Donner à res la valeur res ∗ i
        Donner à i la valeur i + 1
    fin
    Afficher res
fin
```

<span style="color: #26B260"><ins>Première erreur :</ins> Oubli de la déclaration des variables.</span>

<span style="color: #26B260"><Ins>Deuxième erreur :</ins> La condition pour entrer dans la boucle ne peut pas être vérifiée car i n'a pas de valeur avant l'entrée dans le Tant que.</span>

## <span style="color: #1a02d6"><ins>**Exercice 7.16**</ins></span>

L’algorithme ci-dessous calcule 10!
Quelle est l'erreur ?
```
Début
    Donner à res la valeur 1
    Donner à i la valeur 1
    tant que i ≤ 10 faire
        Donner à i la valeur 1
        Donner à res la valeur res ∗ i
        Donner à i la valeur i + 1
    fin
    Afficher res
fin
```
<span style="color: #26B260">Quand on développe l'algorithme on voit :</span>

<span style="color: #26B260">res = 1</span>

<span style="color: #26B260">i = 1 ; res = 1</span>

<span style="color: #26B260">Tant que i est inférieur ou égal à 10 (condition vérifiée et VRAI), on donne à i la valeur 1 et on lui ajoute 1 donc i = 2, et on recommence, on donne i = 1 et on lui ajoute 1;  i = 2 et ainsi de suite. **C'est une boucle infinie**.</span>

## <span style="color: #1a02d6"><ins>**Exercice 7.17**</ins></span>

L’algorithme ci-dessous calcule 10!
Quelle est l'erreur ?
```
Début
    Donner à res la valeur 1
    Donner à i la valeur 11
    tant que i ≤ 10 faire
        Donner à res la valeur res ∗ i
        Donner à i la valeur i + 1
    fin
    Afficher res
fin
```
<span style="color: #26B260">Cet algorithme ne calcule pas 10!, car la valeur de i ne rentre pas dans la condition d'entrée dans la boucle.</span>


## <span style="color: #1a02d6"><ins>**Exercice 7.18**</ins></span>

Que fait l’algorithme ci-dessous ?
```
Début
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
        finSi
    finPour
    Afficher max
fin
```

<span style="color: #26B260">Cet algorithme est un algorithme de calcul d'intégrale pour une fonction qu'on considère définie et continue sur un intervalle [0 ; 10 ] .</span>

<span style="color: #26B260">Sur chaque intervalle [xi, xi+1] est représenté un rectangle de largeur xi+1 - xi et de hauteur : f((xi + xi+1)/2) pour rectangles du point milieu . La méthode des rectangles consiste à remplacer “ l'aire sous la courbe ” par la somme des aires des rectangles obtenus. Mais là l'algorithme demande uniquement la valeur Maximale de la courbe.</span>

Max = 153

## <span style="color: #1a02d6"><ins>**Exercice 7.19**</ins></span>

Que fait l’algorithme ci-dessous ?
```
Début
    Lire la valeur de N
    Donner à i la valeur 0
    Donner à n la valeur 1
    Tant que n ≤ N faire
        Donner à n la valeur 2 ∗ n
        Donner à i la valeur i + 1
    fin
    Afficher i − 1
fin
```

<span style="color: #26B260">Cet algorithme la plus grande puissance de 2 du chiffre entré , exemple :</span>

<span style="color: #26B260">N = 18 , une fois la bouche exécuté on obtient 4 on a bien 18 = 2<sup>4</sup> + 2</span> 

<span style="color: #26B260">N  = 32 , une fois la boucle exécuté on obtient 5 On a bien 32 = 2<sup>5</sup></span>


## <span style="color: #1a02d6"><ins>**Exercice 7.20**</ins></span>

Que se passe-t-il si dans l'exercice précédent on choisit N = 0 ?
Comment réparer le problème ?

<span style="color: #26B260">La condition n'est pas respectée on ne rentre pas dans la boucle donc le résultat est -1.</span>

<span style="color: #26B260">Pour réparer le problème on va utiliser : </span>

```
Début
    Lire la valeur de N
    Donner à i la valeur 0
    Si N = 0
        Ecrire "Ce chiffre n'a pas de puissance de 2 , Veuillez en saisir un autre."
    finSi
    Tant que 2^i =< N Faire 
        Donner à i la valeur i+1
    Fin de Tant que
    Ecrire i-1
fin
```

## <span style="color: #1a02d6"><ins>**Exercice 7.21**</span>

Écrire un algorithme qui détermine si un nombre lu au clavier est un nombre premier.

Un nombre entier naturel (supérieur ou égal à 2) est un nombre premier s'il admet exactement 2 diviseurs : 1 et lui-même.
Exemple : 2, 3, 5, 7, 11, 13, 17, 19 … sont des nombres premiers. Il en existe une infinité.

<span style="color: #26B260">Faut bien retenir ce qu'il y a dans l'énoncé à savoir Un nombre est premier que s'il admet exactement **2 Diviseurs : 1 et lui-même**</span>

```
Variables
Nombre, i, Div de type Entier  % Div va nous permettre de calculer le Nombre de Diviseurs %

Début
    Afficher "Veuillez saisir un nombre pour déterminer s'il est un nombre premier : "
    Lire Nombre
    Div <- 0

    Pour i <- 1 à Nombre
        Si (Nombre % i = 0) Alors
            Div <- Div + 1
        FinSi
    FinPour

    Si Div = 2 Alors
        Ecrire "Le nombre saisi est premier."
    Sinon
        Ecrire "Le nombre saisi n'est pas premier."
    FinSi
fin
```

## <span style="color: #1a02d6"><ins>**Exercice 7.22**</ins></span>

Pour déterminer si un nombre entier naturel n supérieur ou égal 2 est un nombre premier, on doit chercher un diviseur de n parmi les nombres premiers successifs (2, 3, 5, 7, 11 …) jusqu'à la valeur $\sqrt{n}$.
En effet, si n n'admet aucun diviseur parmi les nombres premiers successifs jusqu'à la valeur $\sqrt{n}$, il n'en admettra pas non plus entre $\sqrt{n}$ et n car les diviseurs d'un nombre vont par paires : l'un compris entre 2 et $\sqrt{n}$, et l'autre compris entre $\sqrt{n}$ et n.
Si n n'admet aucun diviseur parmi les nombres premiers successifs jusqu'à la valeur $\sqrt{n}$, c'est donc un nombre premier.

Améliorer l'exercice précédent en conséquence.

```
Variables
Nb, Diviseur, Rac de type Numérique

Début
    Afficher " Veuillez saisir un nombre pour déterminer s'il est un nombre premier : "
    Lire Nb
    Rac <- RacineCarré(N)
    Diviseur <- 2
    Tant que ((N % Diviseur <> 0) et (Diviseur =< Rac)) faire
        Diviseur <- Diviseur+1
    fin Tant que
    Si Diviseur > Rac Alors 
        Affichier "Le nombre que vous avez saisi est premier"
    Sinon
        Afficher "Le nombre que vous avez saisi n'est pas premier"
    fin Si
fin
```