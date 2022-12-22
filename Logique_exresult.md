- [<span style="color: #1a02d6"><ins>**Exercices ch6**</ins>](#span-stylecolor-1a02d6insexercices-ch6ins)
  - [<span style="color: #1a02d6"><ins>**Exercice 6.1**</ins></span>](#insexercice-61ins)
  - [<span style="color: #1a02d6"><ins>**Exercice 6.2**</ins></span>](#insexercice-62ins)
  - [<span style="color: #1a02d6"><ins>**Exercice 6.3**</ins></span>](#insexercice-63ins)
  - [<span style="color: #1a02d6"><ins>**Exercice 6.4**</ins></span>](#insexercice-64ins)
  - [<span style="color: #1a02d6"><ins>**Exercice 6.5**</ins></span>](#insexercice-65ins)
  - [<span style="color: #1a02d6"><ins>**Exercice 6.6**</ins></span>](#insexercice-66ins)
  - [<span style="color: #1a02d6"><ins>**Exercice 6.7**</ins></span>](#insexercice-67ins)
  - [<span style="color: #1a02d6"><ins>**Exercice 6.8**</ins></span>](#insexercice-68ins)
  - [<span style="color: #1a02d6"><ins>**Exercice 6.9**</ins></span>](#insexercice-69ins)

# <span style="color: #1a02d6"><ins>**Exercices ch6**</ins>

## <span style="color: #1a02d6"><ins>**Exercice 6.1**</ins></span>

Formulez un algorithme équivalent à l’algorithme suivant :
```
Si Tutu > Toto + 4 OU Tata = "OK" Alors
    Tutu ← Tutu + 1
Sinon
    Tutu ← Tutu – 1
Finsi
```
<span style="color: #26B260"> il suffit d’appliquer la règle de la transformation du OU en ET vue en cours (loi de Morgan) : </span>
```
Si Tutu <= Toto + 4 ET Tata différent de "OK" Alors
  Tutu ← Tutu - 1
Sinon
  Tutu ← Tutu + 1
Finsi
```


## <span style="color: #1a02d6"><ins>**Exercice 6.2**</ins></span>

Cet algorithme est destiné à prédire l'avenir, et il doit être infaillible !

Il lira au clavier l’heure et les minutes, et il affichera l’heure qu’il sera une minute plus tard. Par exemple, si l'utilisateur tape 21 puis 32, l'algorithme doit répondre :

"Dans une minute, il sera 21 heure(s) 33".

<ins>**NB**</ins> : on suppose que l'utilisateur entre une heure valide. Pas besoin donc de la vérifier.

Ecrire 2 versions :

- une sans utiliser modulo
- une autre en utilisant modulo

<span style="color: #26B260">**Première Version sans utiliser modulo**</span>

```
Variables 
H, M en Numérique

Début
    Ecrire "Entrez les Heures, puis les Minutes : "
    Lire H, M
    M ← M + 1
    Si M = 60 Alors
        M <- 0
        H <- H + 1
    FinSi
    Si H = 24 Alors
        H <- 0
    FinSi
    Ecrire "Dans une minute, il sera ", H, "heure(s) ", M, "minute(s)"
Fin
```
<span style="color: #26B260">**Deuxième version en utilisant modulo**</span>

```
Variables
Heu, Min en Numérique

Début
    Ecrire "Entrez les Heures, puis les Minutes : "
    lire Heu, Min
    Min <- Min + 1
    Si Min % 60 = 0 Alors
        H <- H + 1
    FinSi
    si H % 24 =0 Alors
        H <- 0
    FinSi
    Ecrire "Dans une minute, il sera", Heu, "heure(s) ", Min, "Minute(s)"
Fin
```

## <span style="color: #1a02d6"><ins>**Exercice 6.3**</ins></span>

De même que le précédent, cet algorithme doit demander une heure et en afficher une autre. Mais cette fois, il doit gérer également les secondes, et afficher l'heure qu'il sera une seconde plus tard.

Par exemple, si l'utilisateur tape 21, puis 32, puis 8, l'algorithme doit répondre : "Dans une seconde, il sera 21 heure(s), 32 minute(s) et 9 seconde(s)".

<ins>**NB**</ins> : là encore, on suppose que l'utilisateur entre une date valide.

```
Variables 
Heur, Min, Sec en Numérique

Début
    Ecrire "Entrez les Heures, puis les Minutes, puis les Secondes : "
    Lire Heur, Min, Sec
    Sec <- Sec + 1
    Si Sec = 60 Alors
        Sec <- 0
        Min <- Min + 1
    FinSi
    Si Min = 60 Alors
        Min <- 0
        Heur <- Heur + 1
    FinSi
    Si Heur = 24 Alors
        Heur <- 0
    FinSi
    Ecrire "Dans une Seconde il sera ", Heur, "H", Min, "M et ", Sec, "S"
Fin
```

## <span style="color: #1a02d6"><ins>**Exercice 6.4**</ins></span>

Un magasin de reprographie facture 0,10 € les dix premières photocopies, 0,09 E les vingt suivantes et 0,08 E au-delà.

Ecrivez un algorithme qui demande à l’utilisateur le nombre de photocopies effectuées et qui affiche la facture correspondante.

```
Variables 
Nb, PRIX en Numérique
Début
    Ecrire "Quel est le Nombre de photocopies que vous désirez ?  "
    Lire Nb
    Si Nb <= 10 Alors
        PRIX <- Nb * 0,1
    SinonSi Nb <= 30 Alors
        PRIX <- 10 * 0,1 + (Nb – 10) * 0,09
    Sinon
        PRIX <- 10 * 0,1 + 20 * 0,09 + (Nb – 30) * 0,08
    FinSi
    Ecrire "Le Prix à payer pour vos photocopies est de : ", PRIX
Fin
```

## <span style="color: #1a02d6"><ins>**Exercice 6.5**</ins></span>

Les habitants de Zorglub paient l’impôt selon les règles suivantes :
- les hommes de plus de 20 ans paient l’impôt
- les femmes paient l’impôt si elles ont entre 18 et 35 ans
- les autres ne paient pas d’impôt
  
Le programme demandera donc l’âge et le sexe du Zorglubien, et se prononcera donc ensuite sur le fait que l’habitant est imposable.

```
Variables 
Sexe en Caractère
Age en Numérique
Cas1, Cas2 en Booléen

Début
    Ecrire "Entrez le sexe de la personne (H/F) : "
    Lire sex
    Ecrire "Entrez l’âge: "
    Lire Age
    Cas1 <- Sexe = "H" ET Age > 20
    Cas2 <- Sexe = "F" ET (Age > 18 ET Age < 35)
    Si Cas1 OU Cas2 Alors
        Ecrire "Imposable"
    Sinon
        Ecrire "Non Imposable"
FinSi
Fin
```



## <span style="color: #1a02d6"><ins>**Exercice 6.6**</ins></span>

Les élections législatives, en Guignolerie Septentrionale, obéissent à la règle suivante :
- lorsque l'un des candidats obtient plus de 50% des suffrages, il est élu dès le premier tour.
- en cas de deuxième tour, peuvent participer uniquement les candidats ayant obtenu au moins 12,5% des voix au premier tour.
  
Vous devez écrire un algorithme qui permette la saisie des scores de quatre candidats au premier tour. Cet algorithme traitera ensuite le candidat numéro 1 (et **uniquement** lui) : il dira s'il est élu, battu, s'il se trouve en ballottage favorable (il participe au second tour en étant arrivé en tête à l'issue du premier tour) ou défavorable (il participe au second tour sans avoir été en tête au premier tour).

```
Variables 
Cand1, Cand2, Cand3, Cand4 en Numérique
Cas1, Cas2, Cas3, Cas4 en Booléen

Début
    Ecrire "Entrez les scores des quatre candidats :"
    Lire Cand1, Cand2, Cand3, Cand4
    Cas1 <- Cand1 > 50
    Cas2 <- Cand2 > 50 ou Cand3 > 50 ou Cand4 > 50
    Cas3 <- Cand1 >= Cand2 et Cand1 >= Cand3 et Cand1 >= Cand4
    Cas4 <- Cand1 >= 12,5
    Si Cas1 Alors
        Ecrire “Le Candidat 1 est élu au premier tour, félicitations !"
    Sinonsi Cas2 OU Non Cas4 Alors
        Ecrire “Le Candidat 1 est battu, éliminé, au-revoir !!!”
    SinonSi Cas3 Alors
        Ecrire "Le Candidat 1 est en ballotage favorable."
    Sinon
        Ecrire "Le Candidat 1 est en ballotage, mais défavorable, dur dur !!"
    FinSi
Fin
```

## <span style="color: #1a02d6"><ins>**Exercice 6.7**</ins></span>

Une compagnie d'assurance automobile propose à ses clients quatre familles de tarifs identifiables par une couleur, du moins au plus onéreux : tarifs bleu, vert, orange et rouge. Le tarif dépend de la situation du conducteur :

- un **conducteur de moins de 25 ans et titulaire du permis depuis moins de deux ans**, se voit attribuer le **tarif rouge**, si toutefois **il n'a jamais été responsable d'accident. Sinon, la compagnie refuse de l'assurer**.
- un **conducteur de moins de 25 ans et titulaire du permis depuis plus de deux ans**, ou de **plus de 25 ans mais titulaire du permis depuis moins de deux ans** a le droit au **tarif orange** s'il n'a **jamais provoqué d'accident, au tarif rouge** pour **un accident, sinon il est refusé**.
- un **conducteur de plus de 25 ans titulaire du permis depuis plus de deux ans** bénéficie du **tarif vert** s'il n'est à l'origine d'**aucun accident** et du **tarif orange** pour **un accident**, du **tarif rouge** pour **deux accidents**, et **refusé** au-delà
- De plus, **pour encourager la fidélité des clients acceptés**, la compagnie propose un contrat de la couleur immédiatement la plus avantageuse s'il est entré dans la maison depuis **plus de cinq ans**. Ainsi, s'il satisfait à cette exigence, un client normalement **"vert" devient "bleu"**, un client normalement **"orange" devient "vert"**, et le **"rouge" devient orange**.
  
Ecrire l'algorithme permettant de saisir les données nécessaires (sans contrôle de saisie) et de traiter ce problème. Avant de se lancer à corps perdu dans cet exercice, on pourra réfléchir un peu et s'apercevoir qu'il est plus simple qu'il n'en a l'air (cela s'appelle faire une analyse !)

```
Variables 
Age, PERMIS, Acci, Assuran en Numérique
Cas1, Cas2, Cas3 en Booléen
Sit en Caractère

Début
    Ecrire "Quel âge à la personne ? "
    Lire Age
    Ecrire "Combien a-t-elle d'années de permis ? "
    Lire PERMIS
    Ecrire "Combien a-t-elle eu d'accident(s) ? "
    Lire Acci
    Ecrire "Depuis combien d'années est elle assurée ?(Nombre d'années) "
    Lire Assuran
    Cas1 <- Age >= 25
    Cas2 <- PERMIS >= 2
    Cas3 <- Assuran > 5
    Si Non Cas1 et Non Cas2 Alors
        Si Acci = 0 Alors
            Sit <- "Rouge"
        Sinon
            Sit <- "Refusé"
        FinSi
    Sinonsi (Non Cas1 ET Cas2) OU (Cas1 ET Non Cas2) Alors
        Si Acci = 0 Alors
            Sit <- "Orange"
        SinonSi Acci = 1 Alors
            Sit <- "Rouge"
        Sinon
            Sit <- "Refusé"
        FinSi
    Sinon
        Si Acci = 0 Alors
            Sit <- "Vert"
        SinonSi Acci = 1 Alors
            Sit <- "Orange"
        SinonSi Acci = 2 Alors
            Sit <- "Rouge"
        Sinon
            Sit <- "Refusé"
        FinSi
    FinSi
    Si Cas3 Alors
        Si Sit = "Rouge" Alors
            Sit <- "Orange"
        SinonSi Sit = "Orange" Alors
            Sit <- "Vert"
        SinonSi Sit = "Vert" Alors
            Sit <- "Bleu"
        FinSi
    FinSi
    Ecrire "La personne sera dans la situation suivante : ", Sit
Fin
```
<span style="color: #26B260">Le raisonnement de cet algorithme  resemble à un système de points :</span>

<span style="color: #26B260">- Conducteur moins de 25 ans **+ 1 point**</span>

<span style="color: #26B260">- Titulaire du permis de conduire depuis moins de 2 ans **+ 1point**</span>

<span style="color: #26B260">- 1 Accident : **+ 1 Point**</span>

<span style="color: #26B260">- Plus de 5 ans d'assurance  **- 1 point**</span>
  
<span style="color: #26B260">Ainsi la situation de la personne peut etre établie suivent la barème suivant :</span>

<span style="color: #26B260">- Rouge : 2 points</span>

<span style="color: #26B260">- Orange : 1 point</span>

<span style="color: #26B260">- Vert : 0 point</span>

<span style="color: #26B260">- Bleu : -1 point</span>


```
Variables 
Age, PERMIS, Acci, Assuran, Point en Numérique
Cas1, Cas2, Cas3 en Booléen
Sit en Caractère

Début
    Ecrire "Quel âge à la personne ? "
    Lire Age
    Ecrire "Combien a-t-elle d'années de permis ? "
    Lire PERMIS
    Ecrire "Combien a-t-elle eu d'accident(s) ? "
    Lire Acci
    Ecrire "Depuis combien d'années est elle assurée ?(Nombre d'années) "
    Lire Assuran
    Cas1 <- Age >= 25
    Cas2 <- PERMIS >= 2
    Cas3 <- Assuran > 5
    Point <- 0
    Si Non Cas1 Alors
        Point <- Point + 1
    FinSi
    Si Non Cas2 Alors
        Point <- Point + 1
    FinSi
    Point <- Point + Acci
    Si Point < 3 ET Cas3 Alors
        Point <- Point – 1
    FinSi
    Si Point = -1 Alors
        Sit <- "Bleu"
    SinonSi Point = 0 Alors
        Sit <- "Vert"
    SinonSi Point = 1 Alors
        Sit <- "Orange"
    SinonSi Point = 2 Alors
        Sit <- "Rouge"
    Sinon
        Sit <- "Refusé"
    FinSi
    Ecrire "La personne sera dans la situation suivante : ", Sit
Fin
```


## <span style="color: #1a02d6"><ins>**Exercice 6.8**</ins></span>

Ecrivez un algorithme qui a près avoir **demandé un numéro de jour, de mois et d'année à l'utilisateur, renvoie s'il s'agit ou non d'une date valide**.

Cet exercice est certes d’un manque d’originalité affligeant, mais après tout, en algorithmique comme ailleurs, il faut connaître ses classiques ! Et quand on a fait cela une fois dans sa vie, on apprécie pleinement l’existence d’un type numérique « date » dans certains langages…).

Il n'est sans doute pas inutile de rappeler rapidement que **le mois de février compte 28 jours, sauf si l’année est bissextile, auquel cas il en compte 29. L’année est bissextile si elle est divisible par quatre**. Toutefois, **les années divisibles par 100 ne sont pas bissextiles, mais les années divisibles par 400 le sont**. Ouf !

Un dernier petit détail : vous ne savez pas, pour l’instant, exprimer correctement en pseudo-code l’idée qu’un nombre A est divisible par un nombre B. Aussi, vous vous contenterez d’écrire en bons télégraphistes que A divisible par B se dit « A dp B ».

```
Variables 
Jour, Mois, Annee, JourMax en Numérique
ValidJ, ValidM, Bissex en Booleen

Début
    Ecrire "Entrez le numéro du jour"
    Lire Jour
    Ecrire "Entrez le numéro du mois"
    Lire Mois
    Ecrire "Entrez l'année"
    Lire Annee 
    Bissex ← Annee dp 400 OU (non(Annee dp 100) ET Annee dp 4)
    JourMax ← 0
    ValidM ← Mois >= 1 ET Mois =< 12
    Si ValidM Alors
        Si Mois = 2 ET Bissex Alors
            JourMax ← 29
        SinonSi Mois = 2 Alors
            JourMax ← 28
        SinonSi Mois = 4 OU Mois = 6 OU Mois = 9 OU Mois = 11 Alors
            JourMax ← 30
<<<<<<< HEAD
        finSi
        Sinon
=======
    Sinon
>>>>>>> b42b7710af13e3ea3a774493e7194d5262b685b2
        JourMax ← 31
    FinSi
    ValidJ ← Jour >= 1 ET Jour =< JourMax
    Si ValidJ ET ValidM alors
        Ecrire "La date est valide"
    Sinon
        Ecrire "La date n'est pas valide"
    FinSi
FinSi
```
<span style="color: #26B260">Alternative :</span>

```
Variables 
Jour, Mois, Annee, en Numérique
Cas1, Cas2, Cas3, Cas4, Bissex en Booleen

Début
    Ecrire "Entrez le numéro du jour"
    Lire Jour
    Ecrire "Entrez le numéro du mois"
    Lire Mois
    Ecrire "Entrez l'année"
    Lire Annee
    Bissex ← (Annee dp 4 et Non(Annee dp 100)) OU Annee dp 400
    Cas1 <- (Mois=1 OU Mois=3 OU Mois=5 OU Mois=7 OU Mois=8 OU Mois=10 OU Mois=12) ET (Jour >= 1 ET Jour =< 31)
    Cas2 <- (Mois=4 OU Mois=6 OU Mois=9 OU Mois=11) ET (Jour>=1 ET Jour=<30)
    Cas3 <- Mois=2 ET Bissex ET Jour>=1 ET Jour=<29
    Cas4 <- Mois=2 ET Jour>=1 ET Jour=<28
    Si Cas1 OU Cas2 OU Cas3 OU Cas4 Alors
        Ecrire "Date valide"
    Sinon
        Ecrire "Date non valide"
    FinSi
Fin
```


## <span style="color: #1a02d6"><ins>**Exercice 6.9**</ins></span>

Soit une équation de droite `3x + 4y + 1 = 0`. Écrire un algorithme qui lit au clavier les coordonnées d’un point et étudie l’appartenance du point à la droite.

```
Variables
x, y, f type Numérique

Début
    Ecrire "Soit l'équation de la droite 3x+4y+1 = 0. Pour déterminer si un point de coordonnées (x,y) appartient à cette droite . Donnez sa coordonnée x :"
    Lire x
    Afficher "Donner donnez sa coordonnée y :"
    Lire y
    Donner à f la valeur 3x+4y+1
    Si f == 0 alors
        Afficher "Le point " x "," y " appartient à la droite."
    sinon
        Afficher "Le point " x "," y " n'appartient pas à la droite."
    fin si
fin
```