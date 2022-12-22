- [**Exercices ch13**](#exercices-ch13)
  - [**Exercice 13.1**](#exercice-131)
  - [**Exercice 13.2**](#exercice-132)
  - [**Exercice 13.3**](#exercice-133)
  - [**Exercice 13.4**](#exercice-134)
  - [**Exercice 13.5**](#exercice-135)
  - [**Exercice 13.6**](#exercice-136)
  - [**Exercice 13.7**](#exercice-137)
  - [**Exercice 13.8**](#exercice-138)
  - [**Exercice 13.9**](#exercice-139)
  - [**Exercice 13.10**](#exercice-1310)
  - [**Exercice 13.11**](#exercice-1311)
    - [**a. Ecrire la fonction TousDifferents**](#a-ecrire-la-fonction-tousdifferents)
    - [**b. Ecrire la procédure RemplitGrille**](#b-ecrire-la-procédure-remplitgrille)
    - [**c. Ecrire la fonction Veriflignes**](#c-ecrire-la-fonction-veriflignes)
    - [**d. Ecrire la fonction Verifcolonnes**](#d-ecrire-la-fonction-verifcolonnes)
    - [**e. Ecrire la fonction VerifSousGrilles**](#e-ecrire-la-fonction-verifsousgrilles)
    - [**f. Ecrire la procédure principale de l'application**](#f-ecrire-la-procédure-principale-de-lapplication)

# <span style="color: #1a02d6"><ins>**Exercices ch13**</ins></span>

## <span style="color: #1a02d6"><ins>**Exercice 13.1**</ins></span>

Ecrire un algorithme permenttant de calculer la factorielle d'un nombre en utilisant une fonction récursive.


```
Fonction Facto (Nbr) de Type Numérique

VARIABLES
Result, Nbr de Type Numérique

Début
    Si Nbr < 0 Alors
        Result <- 0
    Sinon
        Si Nbr = 1 OU Nbr = 0 Alors
            Result <- 1
        Sinon
            Result <- Nbr * Facto (Nbr - 1)
        FinSI
    FinSi
    Retourner Result
FinFonction
```


## <span style="color: #1a02d6"><ins>**Exercice 13.2**</ins></spans>

Écrivez une fonction qui renvoie la somme de cinq nombres fournis en argument.

```
Fonction Somme(A, B, C, D, E) Par valeur de Type Numérique

VARIABLES
Result de Type Numérique

DébutFonction
    Result <- A + B + C + D
    Renvoyer Result
FinFonction
```
<span style="color: #26B260">Ou alors en une seule ligne </span>

```
Fonction Somme(A, B, C, D, E) Par valeur de Type Numérique

DébutFonction
    Renvoyer A + B + C + D
FinFonction
```

## <span style="color: #1a02d6"><ins>**Exercice 13.3**</ins></span>

Écrivez une fonction qui renvoie le nombre de voyelles contenues dans une chaîne de caractères passée en argument. Au passage, notez qu'une fonction a tout à fait le droit d'appeler une autre fonction.

```
Fonction NbVoyelles (Phra de Type Caractère en Argument) Type Numérique

VARIABLES
Nb, i, en Entier

DébutFonction
    Ecrire "Tapez votre phrase : "
    Lire Phra
    Nb <- 0
    Pour i <- 1 à Len(Phra)          % Len(Phra)  : renvoie le nombre de caractères de la phrase tapée %
        Si Mid(Phra, i, 1) = "a" OU Mid(Phra, i, 1) = "e" OU Mid(Phra, i, 1) = "i" OU Mid(Phra, i, 1) = "o" OU Mid(Phra, i, 1) = "u" OU Mid(Phra, i, 1) = "y" Alors
            Nb ← Nb + 1
        FinSi
    i++
    Renvoyer Nb
FinFonction
```

Ou avec moins de code :

```
Fonction NbVoyelles( Phra de Type Caractère en Argument)

VARIABLES
Nb, i de Type Entier

DébutFonction
    Pour i <- 1 à Len(Phra)
      Si Trouve("aeiouy", Mid(Phra,i,1)) <> 0 Alors
        Nb <- Nb + 1
      FinSi
    i++
    Renvoyer Nb
FinFontion
```

## <span style="color: #1a02d6"><ins>**Exercice 13.4**</ins></span>

Réécrivez **la fonction Trouve**, vue précédemment, à l’aide des **fonctions Mid** et **Len** (comme quoi, Trouve, à la différence de Mid et Len, n’est pas une fonction indispensable dans un langage).

<span style="color: #26B260"><ins>**Rappel :**</ins></span>

<span style="color: #26B260"><ins>**MID:**</ins> Retourne une chaîne contenant un nombre spécifié de caractères d'une chaîne.</span>

<span style="color: #26B260"><ins>**LEN:**</ins> Retourne un entier contenant le nombre de caractères contenus dans une chaîne.</span>

<span style="color: #26B260"><ins>**Trouve(chaine1,chaine2)**</ins> renvoie un nombre correspondant à la position de chaine2 dans chaine1 et 0 si chaine2 n'est pas dans chaine1.</span>

```
Fonction Trouve (Phra1 de type caractère, Phra2 de type caractère) de Type Numérique

VARIABLES
Trouv de Type Booléen
i, j de Type Numérique

Début

    Tant que Phra2 <> Mid(Phra1, i, Len(Phra2)) ET i < Len(Phra1) - Len(Phra2)      % Tant qu'on ne trouve pas de caractère de Phra2 dans Phra1 et on a pas atteint le dernier rang possible %
    i++                       % On fait avancer i %
    FinTantque

    Si Phra2 <> Mid(Phra1,i, Len(Phra2)) Alors    % Si on ne trouve pas de caractère de Phra2 dans Phra1 %
        Renvoyer 0
    Sinon
        Renvoyer 1
    FinSi
FinFonction
```


## <span style="color: #1a02d6"><ins>**Exercice 13.5**</ins></span>

Ecrivez une fonction qui purge une chaîne d'un caractère, la chaîne comme le caractère étant passés en argument. Si le caractère spécifié ne fait pas partie de la chaîne, celle-ci devra être retournée intacte. Par exemple :

- Purge("Bonjour","o") renverra "Bnjur"
- Purge("J'ai horreur des espaces"," ") renverra "J'aihorreurdesespaces"
- Purge("Moi, je m'en fous", "y") renverra "Moi, je m'en fous"

```
Fonction Purge  (Phra1 de Type caractère en Argument, Car de Type caractère par valeur) 

VARIABLES 
Phra2 de type Caractère 
i de Type Entier

Début 
    Phra2 <-  "" 
    Pour i <- 0 à Len(Phra1) faire 
        si Mid(Phra1, i, 1) <> Car alors       % Si tout les caractère renvoyé dans Phra1 sont différent de Car %
            Phra2 <- Phra2 & Mid(Phra1, i, car) % On reproduit chaques caractères et on l'insère dans Phra2   %
        finsi
    i++ 
    FinPour
    retourner Phra2
FinFonction
```

## <span style="color: #1a02d6"><ins>**Exercice 13.6**</ins></span>

Même question que précédement, mais cette fois, on doit pouvoir fournir un nombre quelconque de caractères à supprimer en argument.

```
Fonction PurgeBis(Phra1 de Type Caractère, Car de Type Caractère) de Type Caractère

VARIABLES
Phra2 de Type Caractère
i de Type Numérique

Début
   Phra2 <- ""
    Pour i <- 1 à Len(Phra1)
        Si Trouve(Car, Mid(Phra1, i, 1)) = 0 Alors  % Si on ne trouve pas le caractère à supprimer donné en argument %
          Phra2 <- Phra2 & Mid(Phra1, i, 1)     % On reproduit chaques caractères et on l'insère dans Phra2   %
        FinSi
    i++
    Renvoyer Phra2
FinFonction
```

## <span style="color: #1a02d6"><ins>**Exercice 13.7**</ins></span>

Ecrire un traitement qui effectue le tri d'un tableau envoyé en argument (on considère que le code appelant devra également fournir le nombre d'éléments du tableau).

```
Fonction TriTableau (Tab de Type Numérique par Référence, Nb de Type Numérique par Valeur)

VARIABLES
i, PosMin, Tmp de Type Numérique

Début
    Pour i <- 0 à Nb - 2
        PosMin <- i
        Pour j <- i + 1 à Nb - 1 
            Si Tab[j] < Tab[PosMin] Alors
            PosMin <- j
            Finsi
        j++
        FinPour
        Tmp <- Tab[PosMin]
        Tab[PosMin] <- Tab[i]
        Tab[i] <- Tmp
    i++
    FinPour
    Renvoyer Tab
FinFonction
```
________
```
Fonction TriTableauBulle (Tab de Type Numérique par Référence , Taille de Type Numérique par valeur)

VARIABLES
i, Borne de Type Numérique
Tri de Type Booléen

Début
    Tri <- Faux
    Borne <- Taille
    Tant que Tri <- Faux Faire
        Tri <- Vrai
        Pour i <- 0 à Borne -2 Faire
            Si Tab[i] > Tab[i+1] Alors
                Tmp <- Tab[i+1]
                Tab[i+1] <- Tab[i]
                Tab[i] <- Tmp
                Tri <- Faux
            FinSi
        FinPour
        Borne <- Borne - 1
    FinTantque
Fin

```


## <span style="color: #1a02d6"><ins>**Exercice 13.8**</ins></span>

Ecrire un traitement qui informe si un un tableau envoyé en argument est formé ou non d'éléments tous rangés en ordre croissant.

```
Fonction TableauCroissant (Tab de Type Numérique, Taille de Type Numérique)

VARIABLES
i, de Type Numérique
Tri de Type Booléen

Début
    Tri <- Vrai
    i <- 0
    Tant Que Tri ET i < Taille - 1 
        Tri <- Tab[i] < Tab[i+1] 
        i <- i + 1
    FinTantQue
    Renvoyer Tri 
FinFonction
```


## <span style="color: #1a02d6"><ins>**Exercice 13.9**</ins></span>

Ecrire un traitement qui inverse le contenu de deux valeurs passées en argument.

```
PROCEDURE Invers(Val1 de type Numérique par Référence, Val2 de Type Numérique par Référence)

VARIABLE
Tmp en Numérique

Début
    Temp <- Val1
    Val1 <- Val2
    Val2 <- Tmp
FinProcédure
```

## <span style="color: #1a02d6"><ins>**Exercice 13.10**</ins></span>

Reprendre l'exercice 13.6, mais cette fois la procédure comprendra un troisième paramètre, de type booléen. VRAI, celui-ci indiquera que le tri devra être effectué dans l'ordre croissant, FAUX dans l'ordre décroissant.

```
PROCEDURE TriTableau(T[] de Type Numérique par Référence, Nb de Type Numérique par Valeur, Croissant de Type Booléen par valeur)

VARIABLES
i, Pos, Tmp de Type Numérique

Début
    Pour i <- 0 à Nb-2
    Pos <- i
    Pour j <- (i + 1) à (Nb - 1)
        Si Croissant Alors
            Si T[j] < T[Pos] Alors
                Pos <- j
            FinSi
        Sinon
            Si T[j] > T[Pos] Alors
                Pos <- j
            FinSi
        FinSi
    j++
    FinPour
    Tmp <- T[Pos]
    T[Pos] <- T[i]
    T[i] <- Tmp
    i++
FinProcédure
```


## <span style="color: #1a02d6"><ins>**Exercice 13.11**</ins></span>

On va à présent réaliser une application complète, en utilisant une architecture sous forme de sous-procédures et de fonction. Cette application a pour tâche de générer des grilles de Sudoku. Une telle grille est formée de 81 cases (9 x 9), contenant un chiffre entre 1 et 9, et dans laquelle aucune ligne, aucune colonne et aucune "sous-grille" de 3x3, ne contient deux fois le même chiffre.
Pour parvenir à nos fins, on va utiliser une méthode particulièrement barbare et inefficace : la génération aléatoire des 81 valeurs de la grille. On vérifiera alors que la grille satisfait aux critères ; si tel n'est pas le cas... on recommence la génération jusqu'à ce que la grille convienne. En pratique, la probabilité de générer une grille adéquate est si faible que cette méthode prendra sans doute beaucoup de temps, mais passons.
Tout le truc est de piger que vérifier que les neuf cases d'une ligne, d'une colonne, ou d'une sous-grille, sont toutes différentes, c'est en réalité du pareil au même. On va donc factoriser le code procédant à cette vérification sous la forme d'une fonction booléenne TousDifférents, à qui on passera un tableau de 9 valeurs en argument. La fonction renverra donc VRAI si les 9 valeurs du tableau sont toutes différentes, et FAUX sinon.

### <span style="color: #1a02d6"><ins>**a. Ecrire la fonction TousDifferents**</ins></span>

```
Fonction TousDifférents(T[8] de Type Numérique) de Type Booléen
    Pour i <- 0 à 7
        Pour j <- (i + 1) à 8
            Si T[i] = T[j] Alors
                Renvoyer Faux
            FinSi
        j++
        FinPour
    i++
    FinPour
    Renvoyer Vrai 
FinFonction
```


Maintenant, bien que ce ne soit pas indispensable (car ce code n'est pas spécialement répété), on choisit également par pure commodité de confier la génération au hasard de la grille de 81 cases à un module dédié, RemplitGrille. (ce module, à qui on passera notre tableau de 81 cases en argument, est forcément une procédure, puisqu'il a pour tâche d'en modifier les 81 valeurs).

### <span style="color: #1a02d6"><ins>**b. Ecrire la procédure RemplitGrille**</ins></span>

```
Procédure RemplitGrille(T[8, 8] de Type Numérique par Référence)
    Pour i <- 0 à 8
        Pour j <- 0 à 8
            T[i, j] <- Ent(Alea()*9) + 1
        j++
        FinPour
    i++
    FinPour
FinProcédure
```

Il faut à présent vérifier que l'ensemble des lignes correspond à la condition voulue, à savoir qu'il n'y existe pas de doublons. On réalise donc une fonction, VerifLignes, qui va vérifier les neuf lignes de notre grille une par une (en utilisant bien sûr la fonction TousDifférents, déjà écrite) et renvoyer VRAI si toutes les lignes sont correctes, FAUX dans le cas contraire.

### <span style="color: #1a02d6"><ins>**c. Ecrire la fonction Veriflignes**</ins></span>

```
Fonction VerifLignes(Grille[8, 8] de Type Numérique) de Type Booléen

Tableau Ligne[8] de Type Numérique

    Pour i <- 0 à 8
        Pour j <- 0 à 8
            Ligne[j] <- Grille[i, j]
        j++
        FinPour
        Si Non TousDifferents(Ligne[]) Alors
            Renvoyer Faux
        FinSi
    i++
    FinPour
    Renvoyer Vrai
FinFonction
```

On procède alors de même avec une fonction chargée de vérifir les colonnes, VérifColonnes.

### <span style="color: #1a02d6"><ins>**d. Ecrire la fonction Verifcolonnes**</ins></span>

```
Fonction VerifColonnes(Grille[8, 8] de Type Numérique) de Type Booléen

Tableau Colonne[8] de Type Numérique

    Pour j <- 0 à 8
        Pour i <- 0 à 8
            Colonne[i] <- Grille[i, j]
        i++
        FinPour
        Si Non TousDifferents(Colonne[]) Alors
            Renvoyer Faux
        FinSi
    j++
    FinPour
Renvoyer Vrai
FinFonction
```

...et encore à nouveau, avec cette fois la vrification des neuf "sous-grilles" 3x3.

### <span style="color: #1a02d6"><ins>**e. Ecrire la fonction VerifSousGrilles**</ins></span>

```
Fonction VerifSousGrilles(Grille[8, 8] en Num) en Booléen
Tableau SousGrille[8] en Num
Pour ancrei ← 0 à 6 pas 3
   Pour ancrej ← 0 à 6 pas 3
      Pour decali ← 0 à 2
         Pour decalj ← 0 à 2
            SousGrille[decali*3 + decalj] ← Grille[ancrei + decali, ancrej + decalj]
         decalj suivant
      decali suivant
      Si Non TousDifferents(SousGrille[]) Alors
         Renvoyer Faux
      FinSi
   ancrej suivant
ancrei suivant
Renvoyer Vrai
FinFonction
```


Il ne reste plus qu'à écrire la procédure principale, et l'affaire est dans le sac !

### <span style="color: #1a02d6"><ins>**f. Ecrire la procédure principale de l'application**</ins></span>

```
Procédure principale()
Tableau Sudok[8, 8] en Num
Appeler RemplitGrille(Sudok[])
Tant Que Non VerifLignes(Sudok[]) ou Non VerifColonnes(Sudok[]) ou Non VerifSousGrilles(Sudok[])
   Appeler RemplitGrille(Sudok[])
FinTantQue>
FinProcédure
```

