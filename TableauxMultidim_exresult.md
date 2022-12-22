# <span style="color: #1a02d6"><ins>**Exercices ch10**</ins></span>

## <span style="color: #1a02d6"><ins>**Exercice 10.1**</ins></span>

Écrivez un algorithme remplissant un tableau de 6 sur 13, avec des zéros.

Réponse :

```
Tableau 
Tab[5, 12] en Entier

Début
    Pour i <- 0 à 5
        Pour j <- 0 à 12
            Tab[i, j] <- 0
        j++
    i++
Fin
```

## <span style="color: #1a02d6"><ins>**Exercice 10.2**</ins></span>
Quel résultat produira cet algorithme ?

```
Tableau 
X[1, 2] en Entier
Variables
i, j, val en Entier
    
Début
    Val <- 1
    Pour i <- 0 à 1
        Pour j <- 0 à 2
            X[i, j] <- Val
            Val <- Val + 1
        j++
    i++
    Pour i <- 0 à 1
        Pour j <- 0 à 2
            Ecrire X[i, j]
        j++
    i++
Fin
```

<span style="color: #26B260">Cet algorithme produit un tableau comme ceci:</span>



<span style="color: #26B260">**X[0, 0] = 1**</span>

<span style="color: #26B260">**X[0, 1] = 2**</span>

<span style="color: #26B260">**X[0, 2] = 3**</span>

<span style="color: #26B260">**X[1, 0] = 4**</span>

<span style="color: #26B260">**X[1, 1] = 5**</span>

<span style="color: #26B260">**X[1, 2] = 6**</span>

<span style="color: #26B260">On peut le simplifier en supprimant une boucle comme ceci :</span>

```
Tableau 
X[1, 2] en Entier
Variables
i, j, val en Entier

Début
    Val <- 1
    Pour i <- 0 à 1
        Pour j <- 0 à 2
            X[i, j] <- Val
            Val <- Val + 1
            Ecrire X[i, j]
        j++
    i++
fin
```

## <span style="color: #1a02d6"><ins>**Exercice 10.3**</ins></span>

Quel résultat produira cet algorithme ?
```
Tableau 
X[1, 2] en Entier
Variables 
i, j, val en Entier

Début
    Val <- 1
    Pour i <- 0 à 1
        Pour j <- 0 à 2
            X[i, j] <- Val
            Val <- Val + 1
        j++
    i++
    Pour j <- 0 à 2
        Pour i <- 0 à 1
            Ecrire X[i, j]
        i++
    j++
Fin
```
<span style="color: #26B260">Cet algorithme produit un tableau comme ceci et écris dans cet ordre:</span>

<span style="color: #26B260">**X[0, 0] = 1**</span>

<span style="color: #26B260">**X[1, 0] = 4**</span>

<span style="color: #26B260">**X[0, 1] = 2**</span>

<span style="color: #26B260">**X[1, 1] = 5**</span>

<span style="color: #26B260">**X[0, 2] = 3**</span>

<span style="color: #26B260">**X[1, 2] = 6**</span>


## <span style="color: #1a02d6"><ins>**Exercice 10.4**</ins></span>

Quel résultat produira cet algorithme ?
```
Tableau 
T[3, 1] en Entier
Variables 
k, m, en Entier

Début
    Pour k <- 0 à 3
        Pour m <- 0 à 1
            T[k, m] <- k + m
        m++
    k++
    Pour k <- 0 à 3
        Pour m <- 0 à 1
            Ecrire T[k, m]
        m++
    k++
Fin
```
<span style="color: #26B260">Cet algorithme produit un tableau comme ceci et affiche ses valeurs à l’écran, dans cet ordre:</span>

<span style="color: #26B260">**T[0, 0] = 0**</span>

<span style="color: #26B260">**T[0, 1] = 1**</span>

<span style="color: #26B260">**T[1, 0] = 1**</span>

<span style="color: #26B260">**T[1, 1] = 2**</span>

<span style="color: #26B260">**T[2, 0] = 2**</span>

<span style="color: #26B260">**T[2, 1] = 3**</span>

<span style="color: #26B260">**T[3, 0] = 3**</span>

<span style="color: #26B260">**T[3, 1] = 4**</span>

## <span style="color: #1a02d6"><ins>**Exercice 10.5**</ins></span>

Mêmes questions, en remplaçant la ligne :
```
T[k, m] ← k + m
```

par
```
T[k, m] ← 2 *k + [m + 1]
```
puis par :
```
T[k, m] ← [k + 1] + 4* m
```
En remplaçant la ligne par la première proposition, l'algorithme produit un tableau comme ceci et les affiche dans cet ordre :

<span style="color: #26B260">**T[0, 0] = 1**</span>

<span style="color: #26B260">**T[0, 1] = 2**</span>

<span style="color: #26B260">**T[1, 0] = 3**</span>

<span style="color: #26B260">**T[1, 1] = 4**</span>

<span style="color: #26B260">**T[2, 0] = 5**</span>

<span style="color: #26B260">**T[2, 1] = 6**</span>

<span style="color: #26B260">**T[3, 0] = 7**</span>

<span style="color: #26B260">**T[3, 1] = 8**</span>

 
<span style="color: #26B260">En remplaçant la ligne par la deuxième proposition, l'algorithme produit un tableau comme ceci et les affiche dans cet ordre :</span>

<span style="color: #26B260">**T[0, 0] = 1**</span>

<span style="color: #26B260">**T[0, 1] = 5**</span>

<span style="color: #26B260">**T[1, 0] = 2**</span>

<span style="color: #26B260">**T[1, 1] = 6**</span>

<span style="color: #26B260">**T[2, 0] = 3**</span>

<span style="color: #26B260">**T[2, 1] = 7**</span>

<span style="color: #26B260">**T[3, 0] = 4**</span>

<span style="color: #26B260">**T[3, 1] = 8**</span>


## <span style="color: #1a02d6"><ins>**Exercice 10.6**</ins></span>

Ecrire un algorithme qui trouve la plus grande valeur positive dans ce tableau multidimensionnel.

nbres = [[0, 18], [1, 45], [45, 48], [-49, 2]]

```
Tableau
nbres [3,1] en Numérique
Variables
ValGr, i, j en Numérique

Début
    nbres <- [[0, 18], [1, 45], [45, 48], [[-49, 2]]
    ValGr <- 0
    Pour i <- 0 à 3 Faire
        Si nbres [i][0] > ValGr Alors
            ValGr <- nbres [i][0]
        Sinon
            Si  nbres[i][1] > ValGr Alors
                ValGr <- nbres [i][1]
            FinSi
        FinSi
    FinPour
    Ecrire "La plus grande valeur de ce tableau multidimensionnel est : ", ValGr
FIN
```
```
Tableau
nbres [3,1] en Numérique
Variables
ValGr, i, compare en Numérique

Début
    nbres <- [[0, 18], [1, 45], [45, 48], [-49, 2]]
    ValGr <- 0
    compare <- 0
    POUR i <- 0 à 3 Faire
        Si nbres[i][0] > nbres[i][1] Alors
            compare <- nbres[i][0]
        Sinon
            compare <- nbres[i][1]
        FinSi
        Si compare > ValGr Alors
            ValGr <- compare
        FinSi
    FinPour
    Ecrire "La plus grande valeur de ce tableau multidimensionnel est : ", ValGr
Fin
```

```
Tableau
Nbres [3,1]
en Numérique
Variables
ValGr, i, j en Numérique

Début
    Nbres <- [[0, 18], [1, 45], [45, 48], [-49, 2]]
    ValGr <- 0
    Pour i <- 0 à 3 Faire
        Pour j <- 0 à 1 Faire
            Si Nbres[i][j] > ValGr Alors
                ValGr <- Nbres [i][j]
            FinSi
        FinPour
    FinPour
    Ecrire "La plus grande valeur de ce tableau multidimensionnel est : ", ValGr
Fin
```
## <span style="color: #1a02d6"><ins>**Exercice 10.7**</ins></span>

Écrire un **algorithme de jeu de dames** très simplifié avec **seulement un pion**.

L’ordinateur demande à l’utilisateur **dans quelle case se trouve son pion (quelle ligne, quelle colonne)**. On met en place **un contrôle de saisie afin de vérifier la validité des valeurs entrées**.
Ensuite, on demande à l’utilisateur quel mouvement il veut effectuer : 0 (en haut à gauche), 1 (en haut à droite), 2 (en bas à gauche), 3 (en bas à droite).
Si le mouvement est impossible (i.e. on sort du damier ), on le signale à l’utilisateur et on s’arrête là . Sinon, on déplace le pion et on affiche le damier résultant, en affichant un « O » pour une case vide et un « X » pour la case où se trouve le pion.

```
Tableau 
Tab[10,10]

Variables
i, j, xLigne, yColonne , xLigne2, yColonne2, Mouv En Numérique
MouvOk en Booléen


Début
    xLigne <- 12
    Ecrire "Sur quelle ligne se trouve votre pion ? "
    Tant que xLigne > 9 ET xLigne < 0 
        Lire xLigne
        Si xLigne > 9 OU xligne < 0
            Ecrire "Veuillez saisir une Ligne sur le Damier"
        FinSi
    FinTantque
    yColonne <- 18
    Ecrire "Sur quelle colonne se trouve votre pion ?"
    Tant que yColonne > 9 ET yColonne < 0 Faire
        Lire yColonne
        Si yColonne > 9 OU yColonne < 0
            Ecrire "Veuillez saisir une Colonne sur le Damier"
        FinSi
    FinTantque

    Mouv <- "18"                                       
    Ecrire : "Quel mouvement voulez vous faire ?"
    Ecrire : "0 (en haut a gauche), 1(en haut a droite) 2 (en bas a gauche), 3 (en bas a droite)"
    Tant que Mouv <> 0 ET Mouv <> 1 ET Mouv <> 2 ET Mouv <> 3 Faire           % Contrôle de Mouv %
        Lire Mouv
        Si Mouv <> 0 ET Mouv <> 1 ET Mouv <> 2 ET Mouv <> 3 Alors
            Ecrire "Mouvement impossible recommencez !!"
        FinSi
    FinTantque

    Si Mouv = 0 Alors
        xLigne2 <- xLigne - 1
        yColonne2 <- yColonne + 1
    Sinon
        Si Mouv = 1 Alors
            xLigne2 <- xLigne + 1
            yColonne2 <- yColonne + 1
        Sinon
            Si Mouv = 2 Alors
                xLigne2 <- xLigne - 1
                yColonne2 <- yColonne - 1
            Sinon
                Si Mouv =3 Alors
                    xLigne2 <- xLigne + 1
                    yColonne2 <- yColonne - 1
                FinSi
            FinSI
        FinSi
    FinSi

    MouvOK <- i2 >= 0 et i2 =< 9 et j2 >= 0 et j2 =< 9
    Si mouvOK Alors
        Pour i <- 0 à 9 
            Pour j <- 0 à 9
                Si i <> xLigne2 ET j <> yColonne2
                    Ecrire "O"
                Sinon
                    Ecrire "X"
            j++
            FinPour
        i++
        FinPour
    Sinon
        Ecrire "Vous faite sortir votre pion du damier mouvement impossible !!"
    FinSi
Fin
```
