- [**Exercices ch8**](#exercices-ch8)
  - [**Exercice 8.1**](#exercice-81)
  - [**Exercice 8.2**](#exercice-82)
  - [**Exercice 8.3**](#exercice-83)
  - [**Exercice 8.4**](#exercice-84)
  - [**Exercice 8.5**](#exercice-85)
  - [**Exercice 8.6**](#exercice-86)
  - [**Exercice 8.7**](#exercice-87)
  - [**Exercice 8.8**](#exercice-88)
  - [**Exercice 8.9**](#exercice-89)
  - [**Exercice 8.10**](#exercice-810)
  - [**Exercice 8.11**](#exercice-811)
  - [**Exercice 8.12**](#exercice-812)
  - [**Exercice 8.13**](#exercice-813)
  - [**Exercice 8.14**](#exercice-814)
  - [**Exercice 8.15**](#exercice-815)
  - [**Exercice 8.16**](#exercice-816)
  - [**Exercice 8.17**](#exercice-817)
  - [**Exercice 8.18**](#exercice-818)
  - [**Exercice 8.19**](#exercice-819)
  - [**Exercice 8.20**](#exercice-820)
  - [**Exercice 8.21**](#exercice-821)
  - [**Exercice 8.22**](#exercice-822)

# <span style="color: #1a02d6"><ins>**Exercices ch8**</ins></span>

## <span style="color: #1a02d6"><ins>**Exercice 8.1**</ins></span>

Ecrire un algorithme qui déclare et remplisse un tableau de 7 valeurs numériques en les mettant toutes à zéro.

```
Tableau 
ValNum[6] en Numérique
Variable 
i en Numérique

Début
    Pour i <- 0 à 6
        ValNum[i] <- 0
    i++
Fin
```



## <span style="color: #1a02d6"><ins>**Exercice 8.2**</ins></span>

Ecrire un algorithme qui déclare et remplisse un tableau contenant les six voyelles de l’alphabet latin.

```
Tableau 
Voyel[5] en Caractère

Début
    Voyel[0] <- "a"
    Voyel[1] <- "e"
    Voyel[2] <- "i"
    Voyel[3] <- "o"
    Voyel[4] <- "u"
    Voyel[5] <- "y"
Fin
```


## <span style="color: #1a02d6"><ins>**Exercice 8.3**</ins></span>

Ecrire un algorithme qui déclare un tableau de 9 notes, dont on fait ensuite saisir les valeurs par l’utilisateur.

```
Tableau 
Notes[8] en Numérique
Variable 
i en Numérique

Début
    Pour i <- 0 à 8
        Ecrire "Veuillez saisir la note numéro ", i + 1
        Lire Notes[i]
    i++
Fin
```

## <span style="color: #1a02d6"><ins>**Exercice 8.4**</ins></span>

Que produit l’algorithme suivant ?
```
Tableau 
Nb[5] en Entier
Variable 
i en Entier

Début
    Pour i ← 0 à 5
        Nb[i] ← i * i
    i suivant
    Pour i ← 0 à 5
        Ecrire Nb[i]
    i suivant
    Fin
```
<span style="color: #26B260">L'algorithme suivant rempli un tableau de  6 valeurs d'entiers par le carré de chaque indice, 0 , 1, 4, 9, 16, 25 et l'affiche à l'écran.</span>

| 0 | 1 | 2 | 3 | 4 | 5 |
| :----: |  :----: |  :----: |  :----: |  :----: |  :----: | 
| 0 | 1<sup>1</sup> | 2<sup>2</sup> | 3<sup>2</sup> | 4<sup>2</sup> | 5<sup>2</sup>

Peut-on simplifier cet algorithme avec le même résultat ?

<span style="color: #26B260">On peut éviter de faire deux boucles pour la même itération en regroupant dans une seule boucle pour :</span>

```
Tableau 
Nb[5] en Entier
Variable 
i en Entier

Début
    Pour i ← 0 à 5
        Nb[i] ← i * i
        Ecrire Nb[i]
    i Suivant
Fin
```

## <span style="color: #1a02d6"><ins>**Exercice 8.5**</ins></span>

Que produit l’algorithme suivant ?
```
Tableau 
N[6] en Entier
Variables 
i, k en Entier

Début
    N[0] ← 1
    Pour k ← 1 à 6
        N[k] ← N[k-1] + 2
    k Suivant
    Pour i ← 0 à 6
        Ecrire N[i]
    i suivant
Fin
```
<span style="color: #26B260">Cet algorithme remplit un tableau avec 7 valeurs d'Entier : 1, 3, 5, 7, 9, 11, 13. Il les écrit ensuite à l’écran.</span>

| 0 | 1 | 2 | 3 | 4 | 5 | 6 |
| :----: |  :----: |  :----: |  :----: |  :----: | :----: | :----: |
| 1 | 3 | 5 | 7 | 9 | 11 | 13


Peut-on simplifier cet algorithme avec le même résultat ?

<span style="color: #26B260">De la même manière que l'exercice précédent, on peut éviter de faire deux boucles pour la même itération en regroupant dans une seule boucle pour :</span>

```
Tableau 
N[6] en Entier
Variables 
k en Entier
Début
    N[0] <- 1
    Ecrire N[0]
    Pour k <- 1 à 6
        N[k] <- N[k-1] + 2
        Ecrire N[k]
    k Suivant
Fin
```


## <span style="color: #1a02d6"><ins>**Exercice 8.6**</ins></span>

Que produit l’algorithme suivant ?

```
Tableau 
Suite[7] en Entier
Variable 
i en Entier

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
```
<span style="color: #26B260">Cet algorithme remplit un tableau avec 8 valeurs d'Entier : 1, 1, 2, 3, 5, 8, 13, 21. Il les écrit ensuite à l’écran.</span>

| 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 
| :----: |  :----: |  :----: |  :----: |  :----: | :----: | :----: | :----: |
| 1 | 1 | 2 | 3 | 5 | 8 | 13 | 21 |


## <span style="color: #1a02d6"><ins>**Exercice 8.7**</ins></span>

Ecrivez la fin de l’algorithme 8.3 afin que le calcul de la moyenne des notes soit effectué et affiché à l’écran.
```
Tableau 
Notes[8] en Numérique
Variable 
i, Som en Numérique

Début
    Som <- 0
    Pour i <- 0 à 8
        Ecrire "Veuillez saisir la note numéro ", i + 1
        Lire Notes[i]
        Som <- Som + Notes[i]
    i++
    Ecrire "La Moyenne des Notes saisies est de : ", Som/9
Fin
```


## <span style="color: #1a02d6"><ins>**Exercice 8.8**</ins></span>

Ecrivez un algorithme permettant à l’utilisateur de saisir un nombre quelconque de valeurs, qui devront être stockées dans un tableau. L’utilisateur doit donc commencer par entrer le nombre de valeurs qu’il compte saisir. Il effectuera ensuite cette saisie. Enfin, une fois la saisie terminée, le programme affichera le nombre de valeurs négatives et le nombre de valeurs positives.

```
Tableau 
Tab[] en Numérique
Variables 
Nb, Posi, i, Nega en Numérique

Début
    Ecrire "Veuillez entrer le nombre de valeurs que vous souhaitez : "
    Lire Nb
    Redim Tab[Nb-1]
    Posi <- 0
    Nega <- 0
    Pour i <- 0 à Nb-1
        Ecrire "Veuillez saisir le nombre numéro : ", i + 1
        Lire Tab[i]
    fin Pour
    Si Tab[i] > 0 alors
        Posi <-  Posi + 1
    Sinon
        Nega <- Nega + 1
    finSi
    i++
    Ecrire "Il y a ", Posi , "valeurs Positives."
    Ecrire "Il y a ", Nega , "valeurs Négatives."
fin
```

## <span style="color: #1a02d6"><ins>**Exercice 8.9**</ins></span>

Ecrivez un algorithme calculant la somme des valeurs d’un tableau (on suppose que le tableau a été préalablement saisi)

<span style="color: #26B260">On part avec comme hypothèse que le tableau à N éléments</span>

```
Tableau 
Tab[N] en Numérique
Variables 
S, en Numérique

Début
    S <- 0
    Pour i <- 0 à N - 1 faire
        Lire Tab[i]
        S <- S + Tab[i]
    i++
    finPour
    Ecrire "La somme des éléments du tableau préalablement saisi : ", S
Fin

```


## <span style="color: #1a02d6"><ins>**Exercice 8.10**</ins></span>

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

```
Tableaux 
Tab1[N], Tab2[N], Tab3[N] en Numérique
Variables 
i, N en Numérique

% On part de la supposition que Tab1 et Tab2 ont N éléments %

Début
    Redim Tab3[N-1]
    Pour i <- 0 à N - 1
        Tab3[i] <- Tab1[i] + Tab2[i]
    i++
Fin
```

## <span style="color: #1a02d6"><ins>**Exercice 8.11**</ins></span>

Toujours à partir de deux tableaux précédemment saisis, écrivez un algorithme qui calcule le schtroumpf des deux tableaux. Pour calculer le schtroumpf, il faut multiplier chaque élément du tableau 1 par chaque élément du tableau 2, et additionner le tout. Par exemple si l'on a :
Tableau 1 :
|4| 8| 7| 12|
|-|-|-|-|

Tableau 2 :
|3| 6|
|-|-|

Le Schtroumpf sera :
3 *4 + 3* 8 + 3 *7 + 3* 12 + 6 *4 + 6* 8 + 6 *7 + 6* 12 = 279


```
Tableaux 
Tab1[Nb1], T2[Nb2] en Numérique
Variables 
i, j, Nb1, Nb2, S en Numérique

Début
    S <- 0
    Pour i <- 0 à (N1 – 1)
        Pour j <- 0 à (N2 – 1)
            S <- S + Tab1(i) * Tab2(j)
        j++
    i++
    Ecrire "Le schtroumpf sera : ", S
Fin
```

## <span style="color: #1a02d6"><ins>**Exercice 8.12**</span>

Ecrivez un algorithme permettant à l’utilisateur de saisir un nombre quelconque de valeurs, qui devront être stockées dans un tableau. L’utilisateur doit donc commencer par entrer le nombre de valeurs qu’il compte saisir. Il effectuera ensuite cette saisie. Enfin, une fois la saisie terminée, appliquer ensuite le traitement suivant sur le tableau :

- la première valeur du tableau est augmentée de 1
- la deuxième valeur du tableau est diminuée de 1
- la 3eme valeur du tableau est augmentée de 2
- la 4eme valeur du tableau est diminuée de 2
- la 5eme valeur du tableau est augmentée de 3
- la 6eme valeur du tableau est diminuée de 3
- etc

Le nouveau tableau sera affiché à l’écran.


```
Tableau 
Tab[], TabTrait[] en Numérique
Variables
Nb, i en Numérique
Début
    Ecrire "Veuillez saisir le nombre de valeurs du Tableau :"
    Lire Nb
    Redim Tab[Nb-1]
    Pour i <- 0 à Nb - 1
        Ecrire "Saisissez le nombre numéro :", i + 1
        Lire Tab[i]
    i++
    Tant que i =< Nb-1 Faire
        Pour i <- 0 à  Nb + 1 pas 1 faire
            Si i % 2 = 0 alors
                TabTrait[i] <-Tab[i] + 1
            Sinon        
            TabTrait[i] < -Tab[i]
            finSi
        FinPour
    FinTantque
    Ecrire TabTrait[i]
fin
```


## <span style="color: #1a02d6"><ins>**Exercice 8.13**</span>

Ecrivez un algorithme permettant, toujours sur le même principe, à l’utilisateur de **saisir un nombre déterminé de valeurs**. Le programme, une fois la saisie terminée, **renvoie la plus petite valeur en précisant quelle position elle occupe dans le tableau**. On prendra soin d’effectuer **la saisie dans un premier temps**, et **la recherche de la plus petite valeur du tableau dans un second temps**.

```
Tableau 
Tab[] en Entier
Variables 
Nb, i, PosMin en Entier

Début
    Ecrire "Veuillez saisir le nombre de valeur que nous souhaitez entrer :"
    Lire Nb
    Redim Tab[Nb-1]
    Pour i <- 0 à nb - 1 faire
        Ecrire "Veuillez saisir le nombre numéro :", i+1
        Lire Tab[i]
    finPour
    PosMin <- 0
    Pour i de 1 à Nb - 1 faire
        Si Tab[i] < T[Posmin] alors
            PosMin <- i
        finSi
    finpour
    Ecrire "La plus petite valeur est : ", T[PosMin]
    Ecrire "La position de cette plus petite valeur est : ", PosMin
fin
```


## <span style="color: #1a02d6"><ins>**Exercice 8.14**</ins></span>

Toujours et encore sur le même principe, écrivez un algorithme permettant, à l’utilisateur de saisir les notes d'une classe. Le programme, une fois la saisie terminée, renvoie le nombre de ces notes supérieures à la moyenne **de la classe** ainsi que le plus grand écart (**l'écart est la valeur absolue de la différence de deux éléments : une note et la moyenne de la classe**)

```
Tableau
Tab[] en Entier
Variables
Notes, i, Som, Moy, NbnoteSup, NoteMin, NoteMax en Entier

Début
    Ecrire "Veuillez saisir le nombres de notes à saisir :"
    Lire Notes
    Redim Tab[Notes-1]
    Som <- 0
    Pour i <- 0 à Notes-1 faire
        Ecrire "Veuillez saisir la Note numéro ", i + 1
        Lire Tab[i]
        Som <- Som + Tab[i]
    finPour
    Moy <- Som / Notes
    NoteSup <- 0
    Pour i <- 0 à Notes-1 faire
        Si Tab[i] > Moy Alors
            NbnoteSup <- NbnoteSup + 1
        finSi
    finpour
    Ecrire NbnoteSup, " élèves dépassent la moyenne de la classe"
    NoteMin <- Tab[1]
    NoteMax <- Tab1]
    Pour i <- 0 à Notes-1 faire
        Si Tab[i] > NoteMax Alors
            NoteMax <- Tab[i]
        finSi
        Si Tab[i] < NoteMin Alors
            NoteMin <- Tab[i]
        finSi
    finPour
    Si NoteMax - Moy > Moy - NoteMin Alors
        Ecrire "Le plus grand écart entre une note de la classe et la Moyenne est : ", NoteMax - Moy
    Sinon
        Ecrire "Le plus grand écart entre une note de la classe et la Moyenne est : ", Moy-NoteMin
fin
```

## <span style="color: #1a02d6"><ins>**Exercice 8.15**</ins></span>

Écrire un algorithme de machine à voter : on fait voter des électeurs tant qu’il y en a entre un candidat A et un candidat B. À la fin, on affiche le nom du vainqueur (s’il y en a un). L’algorithme doit être fiable à 100% et ne doit pas permettre d’erreur de saisie.
L'algorithme demandera le nombre de votant puis proposera 4 votes possibles pour chacun des votants :

- A
- B
- blanc```
- nul

```
Tableau
Tab[] en Caractère
Variables
Electeur, CandidatA, CandidatB, Blanc, Nul en Entier

Début
    CandidatA <- 0
    CandidatB <- 0
    Blanc <- 0
    Nul <- 0

    Ecrire "Veuillez saisir le nombre d'électeur :"
    Lire Electeur
    Redim Tab[Electeur-1]
    Pour i <- 0 à Electeur - 1 Faire
        Ecrire "Vote de l'électeur numéro :", i+1
        Ecrire "Effectuez votre vote :"
        Ecrire "****************************************"
        Ecrire "Pressez A pour voter pour le Candidat A."
        Ecrire "Pressez B pour voter pour le Candidat B."
        Ecrire "Pressez C pour le vote Blanc."
        Ecrire "****************************************"
        Ecrire "Quel est votre choix ?"
        Lire Tab[i]
    fin Pour

    Pour i <- 0 à Electeur - 1 pas 1 Faire
        Si A = Tab[i] Alors
            CandidatA <- CandidatA + 1
        SinonSi B = Tab[i] Alors
            CandidatB <- Candidat B + 1
        SinonSi C = Tab[i] Alors
            Blanc <- Blanc + 1
        Sinon
            Nul <- Nul + 1
        FinSi
    finPour

    Si CandidatA > CandidatB Alors
        Ecrire "le Candidat A est élu."
    SinonSi
        Candidat B > Candidat A Alors
            Ecrire "Le candidat B est élu."
    Sinon
        Ecrire "A et B sont à égalité."
    FinSi

    Ecrire "Voici le partage des voix :"
    Ecrire "Le nombre de voix pour le Candidat A est :", CompteA
    Ecrire "Le nombre de voix pour le Candidat B est :", CompteB
    Ecrire "Le nombre de vote Blanc est :", CompteBlanc
    Ecrire "Le nombre de Vote Nul est :", CompteNul
fin
```


## <span style="color: #1a02d6"><ins>**Exercice 8.16**</ins></span>

Ecrire un algorithme permettant le calcul du nombre d'occurences d'un élément donné dans un tableau

```
Tableau
Tab[N]
Variables
i, n, x en Numérique       % i éléments à rentrer dans le tableau , n Le nombre cherché, x le nombre d'occurence %

Début
    Ecrire "Veuillez saisir le nombre d'éléments :"
    Lire N
    Redim Tab[N - 1]

    Pour i <- 0 à N - 1 Faire
        Ecrire "Saisir les éléments dans le tableau ", i+1 , ":"
        Lire T[i]
    FinPour

    Ecrire "Donner la valeur recherché dans la tableau : "
    Lire n
    x <-  0

    Pour i <- 0 à Elem-1 pas 1 Faire
        Si n = T[i] alors
            x <- x + 1
        FinSi
    FinPour

    Ecrire "Le nombre d'Occurence de " , n ,  " dans le Tableau est : " , x
fin
```


## <span style="color: #1a02d6"><ins>**Exercice 8.17**</ins></span>

Ecrire un algorithme permettant le calcul de la moyenne, du minimum et du maximim des éléments d'un tableau.

```
Tableau
Tab[] en Entier
Variables
Elems, i, Somme, Moy, ElemMax, ElemMin en Entier

Début
    Ecrire "Veuillez saisir le nombres d'éléments' à saisir :"
    Lire Elems
    Redim Tab[Elems-1]
    Somme <- 0
    Pour i <- 0 à Elems-1 faire
        Ecrire "Veuillez saisir l'élément numéro ", i + 1
        Lire Tab[i]
        Somme <- Somme + Tab[i]
    finPour

    Moy <- Somme / Elems
    
    ElemMin <- Tab[0]
    ElemMax <- Tab[0]
    Pour i <- 0 à Elems - 1 faire
        Si Tab[i] > ElemMax Alors
            ElemMax <- Tab[i]
        finSi
        Si Tab[i] < ElemMin Alors
            ElemMin <- Tab[i]
        finSi
    finPour

    Ecrire "La moyenne des éléments du tableau est :", Moy
    Ecrire "L'élément minimum du tableau est :", ElemMin
    Ecrire " L'élément maximum du tableau est :", ElemMax
fin
```


## <span style="color: #1a02d6"><ins>**Exercice 8.18**</ins></span>

Ecrire un algorithme permettant de tester si un tableau est trié dans l'ordre décroissant (on ne demande pas de trier)


```
Tableau
Tab[N] en Entier
Variables
i en Entier
Tri en Booléen

Début
    Tri <- VRAI
    i <- 0
    Tant que (Tri = VRAI) ET i < N - 1 faire
        Tri <- Tab[i] =< Tab[i + 1]
        i <- i + 1
    finTant que
    Afficher "Le Tableau est-il trié ? :", Tri
fin
```
## <span style="color: #1a02d6"><ins>**Exercice 8.19**</ins></span>

Ecrire l'algorithme effectuant le décalage des éléments d'un tableau.

Exemple :
• Tableau initial :
|D|E|C|A|L|A|G|E|
|-|-|-|-|-|-|-|-|

• Tableau modifié (décalage à gauche)

|E|C|A|L|A|G|E|D|
|-|-|-|-|-|-|-|-|


```
Tableau
TabCar[7] de type Caractères
Variables
Tmp de type caractère 
i de type Entier 

Début 
    Tmp <- TabCar[1] 
    Pour i <- 0 à 6 Faire 
        TabCar[i] <- TabCar[i+1] 
    FinPour 
    TabCar[7] <- Tmp 
Fin
```

## <span style="color: #1a02d6"><ins>**Exercice 8.20**</ins></span>

Ecrire un algorithme qui calcule le plus grand écart dans un tableau (l'écart est la valeur absolue de la différence de deux éléments). Le tableau ne contiendra que des nombre strictement positifs.

Exemple :
|4|8|1|16|
|-|-|-|-|

Le plus grand écart est de : 15

```
Tableau
Tab[] en Entier
Variables
Nb, i, NbMax,NbMin en Entier
Début
    Ecrire "Veuillez saisir le nombre de valeur que nous souhaitez entrer :"
    Lire Nb
    Redim Tab[Nb-1]
    
    Pour i <- 0 à Nb - 1 faire
        Ecrire "Veuillez saisir le nombre numéro :", i+1
        Lire Tab[i]
        NbMin <- Tab[0]
        NbMax <- Tab[1]
        Si Tab[i] > NbMax Alors
            NbMax <- Tab[i]
        finSi
        Si Tab[i] < NbMin Alors
            NbMin <- Tab[i]
        finSi
    finPour

    Ecrire "Le plus grand écart entre deux éléments du tableau est : ",NbMax - NbMin
fin
```



## <span style="color: #1a02d6"><ins>**Exercice 8.21**</ins></span>

Écrire un algorithme qui remplit une liste de 10 nombres entiers entre 0 et 9 au hasard, puis calcule la somme des éléments de la liste et la moyenne.

```
Tableau
Tab[9] en Entier

Variables
Nb, i, Somme, Moy en Entier

Début
    Somme <- 0
    Pour i <- 0 à 9 Faire
        T[i] <- valeur aléatoire entre 0 et 9
        Lire T[i]
        Somme <- Somme + Tab[i]
    finpour

    Moy <- Somme / 10

    Ecrire "La somme des éléments de la liste est :", Somme, "et la moyenne est :", Moy
fin
```


## <span style="color: #1a02d6"><ins>**Exercice 8.22**</ins></span>

Le code de César consiste à crypter un message en remplaçant chaque lettre par celle qui se trouve 3 rangs à droite dans l’alphabet (et bien sûr "x","y" et "z" deviennent respectivement "a", "b" et "c").
Par exemple "exemple" devient "hahpsoh".
Écrire un algorithme qui crypte un mot entré au clavier (le mot sera en bas de casse) en utilisant le code de César.
Ne pas utiliser le code ASCII, utiliser un simple tableau de longueur 26.

```
Tableau
TabAlpha[25] en Caractère
Variables
Decalage, RangCher, en Entier
Mess , MessCod, Car  en String (Chaîne de Caractère)

Début
    TabAlpha[0] = "a"
    TabAlpha[1] = "b"
    TabAlpha[2] = "c"
    TabAlpha[3] = "d"
    TabAlpha[4] = "e"
    TabAlpha[5] = "f"
    TabAlpha[6] = "g"
    TabAlpha[7] = "h"
    TabAlpha[8] = "i"
    TabAlpha[9] = "j"
    TabAlpha[10] = "k"
    TabAlpha[11] = "l"
    TabAlpha[12] = "m"
    TabAlpha[13] = "n"
    TabAlpha[14] = "o"
    TabAlpha[15] = "p"
    TabAlpha[16] = "q"
    TabAlpha[17] = "r"
    TabAlpha[18] = "s"
    TabAlpha[19] = "t"
    TabAlpha[20] = "u"
    TabAlpha[21] = "v"
    TabAlpha[22] = "w"
    TabAlpha[23] = "x"
    TabAlpha[24] = "y"
    TabAlpha[25] = "z"

    Afficher "Entrez un message à chiffrer :"
    Lire Mess
    MessCod = " "                  % MessCod est vide %
    long_Mess <- Mess.length
    Decalage <- 3
    Pour i <- 0 à long_Mess pas 1 Faire
        Car <- Mess[i]
        Si Car == " "              % car est vide %
            MessCod <- " "
        sinon
            RangCher <- (rang de car dans TabAlpha + decalage) % 26
            MessCod <- TabAlpha[RangCher]
        finSi
    finPour

    Ecrire "Le message chiffré est : ", MessCod
fin
```


