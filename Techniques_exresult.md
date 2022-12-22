- [**Exercices ch9**](#exercices-ch9)
  - [**Exercice 9.1**](#exercice-91)
  - [**Exercice 9.2**](#exercice-92)
  - [**Exercice 9.3**](#exercice-93)
  - [**Exercice 9.4**](#exercice-94)
  - [**Exercice 9.5**](#exercice-95)
  - [**Exercice 9.6**](#exercice-96)
  - [**Exercice 9.7**](#exercice-97)
  - [**Exercice 9.8**](#exercice-98)

# <span style="color: #1a02d6"><ins>**Exercices ch9**</ins></spam>

## <span style="color: #1a02d6"><ins>**Exercice 9.1**</ins></span>

Ecrivez un algorithme qui permette de saisir **un nombre quelconque de valeurs, et qui les range au fur et à mesure dans un tableau**. Le programme, <ins>une fois la saisie terminée</ins>, doit dire **si les éléments du tableau sont tous consécutifs ou non**.
Par exemple, si le tableau est :

|12|13|14|15|16|17|18|
|--|--|--|--|--|--|--|

ses éléments sont tous consécutifs. En revanche, si le tableau est :

|9|10|11|15|16|17|18|
|--|--|--|--|--|--|--|

ses éléments ne sont pas tous consécutifs.

```
Tableau 
TabVal[] en Entier
Variables 
Nb, i en Entier
Flag en Booleen

Début
    Ecrire "Veuillez saisir le nombre de valeurs désirés :"
    Lire Nb
    Redim TabVal[Nb-1]
    
    Pour i <- 0 à Nb - 1
        Ecrire "Saisissez le nombre numéro ", i + 1
        Lire TabVal[i]
    i++
    FinPour

    Flag ← Vrai

    Pour i ← 1 à Nb - 1
        Si T[i] <> T[i – 1] + 1 Alors
            Flag ← Faux
        FinSi
    i++
    FinPour
    Si Flag Alors
        Ecrire "Les nombres saisis sont consécutifs."
    Sinon
        Ecrire "Les nombres saisis ne sont pas consécutifs."
    FinSi
Fin
```

Sans utiliser flag, car si le tableau est plus grand l'algorithme est plus long car il faut examiner la totalité du tableau, alors que si on trouve deux éléments non consécutifs on fait sortir de la Boucle :

```
Tableau 
TabVal[] en Entier
Variables 
Nb, i en Entier
Flag en Booleen

Début
    Ecrire "Veuillez saisir le nombre de valeurs désirés :"
    Lire Nb
    Redim TabVal[Nb-1]
    
    Pour i <- 0 à Nb - 1
        Ecrire "Saisissez le nombre numéro ", i + 1
        Lire TabVal[i]
    i++
    FinPour
    i <- 1
    Tant que TabVal[i] = TabVal[i - 1] + 1 ET i < Nb - 1     % Tant qu'on trouve  deux éléments consécutifs On reste dans la boucle %
        i <- i + 1
    FinTantque

    Si TabVal[i] = TabVal[i - 1] + 1 Alors
        Ecrire "Les nombres saisis sont consécutifs "
    Sinon
        Ecrire "Les nombres saisis ne sont pas consécutifs."
    FinSi

```

## <span style="color: #1a02d6"><ins>**Exercice 9.2**</ins></span>

Ecrivez un algorithme qui trie un tableau dans l’ordre décroissant.
Vous écrirez bien entendu deux versions de cet algorithme, l'une employant le tri par sélection, l'autre le tri à bulles.

<span style="color: #26B260">En employant le tri par sélection :</span>

```
Tableau
Tab[] en Numérique
Variables
i, j, PosMax, Tmp, N en Entier

Début

% boucle principale : le point de départ se décale à chaque tour %
    Pour i <- 0 à N - 2 pas 1 Faire

% on considère provisoirement que t[i] est le plus grand élément %
        PosMax <- i

% on examine tous les éléments suivants %
        Pour j <- i + 1 à N - 1 pas 1 Faire
            Si t[j] > t[PosMax] alors
                PosMax <- j
            Finsi
        FinPour

% A cet endroit, on sait maintenant où est le plus petit élément. Il ne reste plus qu'à effectuer la permutation. On a placé correctement l'élément numéro i, on passe à présent au suivant.%
        Tmp <- t[PosMax]
        t[PosMax] <- t[i]
        t[i] <- Tmp
    FinPour
Fin
```

<span style="color: #26B260">En employant le Tri à Bulles :</span>

```
Tableau
Tab[] en Numérique
Variables
i, j, Tmp, N en Entier

% le flag Permute booléenne nous indique si nous avons ou non procédé à une permutation au cours du dernier balayage du tableau (dans le cas contraire, c’est signe que le tableau est trié, et donc qu’on peut arrêter la machine à bulles) %

Permut en Booléen

Début
    Permut <- Vrai                              % lui attribuer la valeur Vrai dès qu’une seule permutation a été faite %
    TantQue Permut Faire
        Permut <- Faux                          % la remettre à Faux à chaque tour de la boucle principale %
        Pour i <- 0 à N - 2 pas 1 Faire         % On prend les éléments du tableau, du premier jusqu'à l'avant dernier et on procède à l'échange si nécessaire %
            Si Tab[i] < Tab[i + 1] Alors
                Tmp <- Tab[i]
                Tab[i] <- Tab[i + 1]
                Tab[i + 1] <- Tmp
                Permut <- Vrai                  % Pour lancer la boucle principale redonner la valeur Permut à Vrai %
            Finsi
        FinPour
    FinTantQue
Fin
```

## <span style="color: #1a02d6"><ins>**Exercice 9.3**</ins></span>

Ecrivez un algorithme qui inverse l’ordre des éléments d’un tableau dont on suppose qu'il a été préalablement saisi (« les premiers seront les derniers… »)

```
Tableau
Tab[Nb] en Numérique
Variables
i, , Tmp, Nb en Entier

Début
    % On suppose que Tab a Nb éléments préalablement saisis. %
    
    Pour i <- 0 à (Nb-1)/2 
        Tmp <- Tab[i]
        Tab[i] <- Tab[(Nb-1)-i] 
        Tab[(Nb-1)-i] <- Tmp 
    i++
    Finpour
Fin
```



## <span style="color: #1a02d6"><ins>**Exercice 9.4**</ins></span>

Ecrivez un algorithme qui permette à l’utilisateur de supprimer une valeur d’un tableau préalablement saisi. L’utilisateur donnera l’indice de la valeur qu’il souhaite supprimer. Attention, il ne s’agit pas de remettre une valeur à zéro, mais bel et bien de la supprimer du tableau lui-même ! Si le tableau de départ était :

|12|8|4|45|64|9|2|
|--|--|--|--|--|--|--|

Et que l’utilisateur souhaite supprimer la valeur d’indice 4, le nouveau tableau sera :

|12|8|4|45|9|2|
|--|--|--|--|--|--|



```
Tableau 
Tab[N] en numérique
Variable
i, Rg, N en Numérique

Début
    Ecrire "Rang de la valeur à supprimer ?"
    Lire Rg
    Pour i <- Rg à N-2
        Tab[i] <- Tab[i+1]
    i++
    FinPour
    Redim Tab[N–1]
Fin
```

## <span style="color: #1a02d6"><ins>**Exercice 9.5**</ins></span>

Ecrivez l'algorithme qui recherche un mot saisi au clavier dans un dictionnaire. Le dictionnaire est supposé être codé dans un tableau préalablement rempli et trié. L'algo renverra la position dans le tableau si trouvé, sinon renverra 0.

```
Tableau
Dico[] en Caractère                   % Contiens les mots du dictionnaire préalablement remplis %
Variables 
BorSup, BorInf, Icomp, Elem en Entier           % Elem est le nombre d'éléments du tableau Dico[] %
Flag en Booléen

Début
    Ecrire "Entrez le mot à vérifier"
    Lire Mot
    BorSup <- Elem - 1                       % On définit les bornes BorSup & BorInf de la partie du tableau à traiter %
    BorInf <- 0
    Flag <- Faux
    TantQue Non Flag
        Icomp <- [BorSup + BorInf]/2          % Icomp -> indice de l'élément à comparer.%
        Si Mot < Dico[Icomp] Alors    % Si mot se situe avant point comparaison, alors BorSup change, BorInf bouge pas.%
            BorSup <- Icomp - 1
        Sinon
            BorInf <- Icomp + 1
        FinSi
        Flag <- Mot = Dico[Icomp] ou BorSup < BorInf
    FinTantQue
    Si Mot = Dico[Icomp] Alors
        Ecrire "le mot entré existe dans le dictionnaire et occupe la position :", Icomp
    Sinon
        Ecrire "le mot entré n'existe pas dans le dictionnaire : 0"
    Finsi
Fin
```



## <span style="color: #1a02d6"><ins>**Exercice 9.6**</ins></span>

Écrivez un algorithme qui fusionne deux tableaux (déjà existants) dans un troisième, qui devra être trié.
Attention ! On présume que les deux tableaux de départ sont préalablement triés : il est donc irrationnel de faire une simple concaténation des deux tableaux de départ, puis d'opérer un tri : comme quand on se trouve face à deux tas de papiers déjà triés et qu'on veut les réunir, il existe une méthode bien plus économique (et donc, bien plus rationnelle...)
(on considère qu'il n'y a pas de valeurs communes au deux tableaux)

<span style="color: #26B260">T1 est un tableau trié et indexé de 1 à n.</span>

<span style="color: #26B260">T2 est un tableau trié et indexé de 1 à m.</span>

<span style="color: #26B260">T est un tableau trié indexé de 1 à n+m, fusion des tableaux T1 et T2.</span>

```
Tableau
T1[n] , T2[m], T[]
Variable
i, j, k de Type Numérique

Début
    i<- 1
    j <- 1
    k <- 1
    Tant que i =< n ET j =< m Faire
        Si T1[i] < T2[j] Alors
            T[k] <- T1[i]
            i <- i + 1
        Sinon
            T[k] <- T2[j]
            j <- j + 1
        FinSi
        k <- k + 1
    FinTantque
    Tant que i =< n Faire
        T[k]<- T1[i]
        k <- k + 1
        i <- i + 1
    FinTantque
    Tant que j =< m Faire
        T[k] <- T2[j]
        k <- k + 1
        j <- j + 1
    FinTant que
fin
```


## <span style="color: #1a02d6"><ins>**Exercice 9.7**</ins></span>

La fonction f(x) = x² + x − 1 est strictement croissante sur l'intervalle [0; 2]. et que
pour x=0, f(x) est négatif
pour x=2, f(x) est positif

La dichotomie consiste à évaluer la valeur de f(x) au milieu de l'intervalle [a,b]

- si f($\frac{a + b}{2}$) $\leq$ 0 alors on sait qu'il y a une solution à `f(x)=0` dans l'intervale [$\frac{a + b}{2}$, b]
- sinon f($\frac{a + b}{2}$) > 0 alors on sait qu'il y a une solution à `f(x)=0` dans l'intervale [a, $\frac{a + b}{2}$]

Ainsi, dans les deux cas, on a trouvé un intervalle de longueur moitié dans lequel est située une racine de l'équation `f(x)=0`. On recommence alors avec cet intervalle, et ainsi de suite jusqu'à ce qu'on trouve une approximation qui nous convienne.

Écrire un algorithme qui recherche une solution approchée de l’équation y = 0  sur l’intervalle [0; 2] par dichotomie, avec une précision de 10<sup>-3</sup> cad jusqu'à ce que l'intervalle contenant une solution à `f(x)=0` ait une largeur inférieur à 10<sup>-3</sup>.

```
Variables
m, a, b et f sont de type Réels

Début
    f <- x² + x − 1
    a <- 0
    b <- 2
    Tant que (b-a) > 10^-3
        m <- (a+b)/2
        Si f(m)>0 Alors
            b <- m
        Sinon
            a <- m
        fin Si
    FinTantque
    Ecrire "La solution approchée est dans l'intervalle [" a , b "]"
fin
```

<span style="color: #26B260">Autre solution :</span>

```
Variables
Precision , a , b, m , f En Numérique

Début
    Precision <- 0,001
    f <- x² + x − 1
    a <- 0
    b <- 2
    Tant que (b-a) > Precision Faire
        m <- (a+b) / 2                  % On calcule m le milieu de [a,b].%
        Si f(m) * f(b) > 0 Alors        % Si f(m) et f(b) sont de même signe, c'est que la solution se trouve dans [a,m]  %
            b <- m                      % : on affecte à b la valeur de m afin de pouvoir continuer le processus..%
        Sinon
            a <- m                      % Dans le cas contraire, la solution se trouve dans [m,b] : on affecte à a la valeur de m afin de pouvoir continuer le processus %
    FinTantque
    Ecrire a, " < solution < ", b
Fin
```
## <span style="color: #1a02d6"><ins>**Exercice 9.8**</ins></span>

Ecrire un algorithme de sélection de sous tableau et qui autorise la saisie d'index négatif (mais aussi positif).
Exemple :
soit le tableau
|12|8|4|45|9|2|
|--|--|--|--|--|--|

Si l'utilisateur saisit 2 puis -1 l'algorithme renverra le sous tableau qui début à l'indice 2 et termine à l'indice (taille total - 1) cad [2,4]

|4|45|9|
|--|--|--|

Si l'utilisateur saisit 1 puis -2 l'algorithme renverra le sous tableau [1,3]

|8|4|45|
|--|--|--|

Si l'utilisateur saisit 3 puis -4 l'algorithme affichera un message d'erreur car l'intervalle [3,1] n'est pas valide

Si l'utilisateur saisit 1 puis 2 l'algorithme renverra le sous tableau [1,2]

|8|4|
|--|--|

```
Tableau 
T1[N] de type Numérique

Variables
N, RgDeb , RgFin En Numérique

Début
    ...
    RgDeb <- N + 1
    Ecrire "Veuillez saisir le rang à partir duquel vous souhaitez conserver les données : "
    Tant que RgDeb >= N ET |RgDeb| >= N Faire
        Lire RgDeb
        Si RgDeb >= N ET |RgDeb| >= N Alors
            Ecrire "Veuillez Saisir un rang dans le tableau !"
        FinSi
    FinTantQue

    RgFin <- N + 1
    Ecrire "Veuillez saisir le redimensionnement du tableau ou le Rang maxi que vous souhaitez conserver :"
    Tant que RgFin >= N ET |RgFin| >= N Faire
        Lire RgFin
        Si RgFin >= N ET |RgFin| >= N Alors
            Ecrire "Veuillez Saisir un rang dans le tableau !"
        FinSi
    FinTantQue

    Si RgDeb >= 0 ET RgFin > 0 ET RgDeb < RgFin Alors
        Ecrire T1[RgDeb, RgFin]
    Sinon
        Si RgDeb >= 0 ET RgFin =< 0 ET RgDeb < N -|RgFin|  Alors
            Ecrire T1[RgDeb, N - |RgFin|]
        Sinon
            Ecrire "Intervalle non valable"
        FinSi
    FinSi
    
    Si RgDeb < 0 ET RgFin > 0 ET N - |RgDeb| < RgFin Faire
        Ecrire T1[N - |RgDeb| , RgFin]
    Sinon
        Si RgDeb < 0 ET RgFin =< 0 ET |RgDeb| > |RgFin| Alors
            Ecrire T1[N - |RgDeb| , N - |RgFin|]
        Sinon
            Ecrire "Intervalle non valable."
        FinSi
    FinSi

Fin
```
---------------------------

