- [<span style="color: #1a02d6"><ins>**Exercices ch5**</ins></span>](#insexercices-ch5ins)
  - [<span style="color: #1a02d6"><ins>**Exercice 5.1**</ins></span>](#insexercice-51ins)
  - [<span style="color: #1a02d6"><ins>**Exercice 5.2**</ins></span>](#insexercice-52ins)
  - [<span style="color: #1a02d6"><ins>**Exercice 5.3**</ins></span>](#insexercice-53ins)
  - [<span style="color: #1a02d6"><ins>**Exercice 5.4**</ins></span>](#insexercice-54ins)
  - [<span style="color: #1a02d6"><ins>**Exercice 5.5**</ins></span>](#insexercice-55ins)
  - [<span style="color: #1a02d6"><ins>**Exercice 5.6**</ins></span>](#insexercice-56ins)
  - [<span style="color: #1a02d6"><ins>**Exercice 5.7**</ins></span>](#insexercice-57ins)

# <span style="color: #1a02d6"><ins>**Exercices ch5**</ins></span>

## <span style="color: #1a02d6"><ins>**Exercice 5.1**</ins></span>

Ecrire un algorithme qui demande un nombre à l’utilisateur, et l’informe ensuite si ce nombre est positif ou négatif (on laisse de côté le cas où le nombre vaut zéro).

```
Variable 
Nb en Entier

Début
    Ecrire "Veuillez saisir un nombre : "
    Lire Nb
    Si Nb > 0 Alors
        Ecrire "Le nombre saisi est positif”
    Sinon
        Ecrire "Le nombre saisi est négatif"
    Finsi
Fin
```



## <span style="color: #1a02d6"><ins>**Exercice 5.2**</ins></span>

Écrire un algorithme qui lit trois valeurs au clavier et affiche le maximum des trois.

```
Variables
a, b, c, Max `     % pas de typage définit dans l'énoncé %

Début
    Ecrire "Entrez successivement trois valeurs :"
    Lire a, b, c

    Max <- 0
    Si (a>b) alors
        Max = a
    sinon

    Max = a
    Si (b > Max) alors

        Max = b
    fin Si
    Si (c > Max) alors
        Max = c
    fin si
    Afficher "La valeur maximale des trois valeurs est :" , Max
fin
```

## <span style="color: #1a02d6"><ins>**Exercice 5.3**</ins></span>

Ecrire un algorithme qui demande deux nombres à l’utilisateur et l’informe ensuite si leur produit est négatif ou positif (on laisse de côté le cas où le produit est nul). Attention toutefois : on ne doit pas calculer le produit des deux nombres.

```
Variables 
Nb1, Nb2 en Entier

Début
    Ecrire "Entrez deux nombres : "
    Lire Nb1, Nb2
    Si (Nb1 < 0 ET Nb2 < 0) OU (Nb1 > 0 ET Nb2 > 0) Alors
        Ecrire "Le produit est positif"
    Sinon

    Ecrire "Le produit est négatif"

        Ecrire "Le produit est négatif"

    Finsi
Fin
```

## <span style="color: #1a02d6"><ins>**Exercice 5.4**</ins></span>

Ecrire un algorithme qui demande trois noms à l’utilisateur et l’informe ensuite s’ils sont rangés ou non dans l’ordre alphabétique.

```
Variables 
Nom1, Nom2, Nom3 en Caractère

Début
    Ecrire "Entrez trois noms : "
    Lire Nom1, Nom2, Nom3
    Si Nom1 < Nom2 ET Nom2 < Nom3 Alors
        Ecrire "Ces noms sont classés alphabétiquement"
    Sinon
        Ecrire "Ces noms ne sont pas classés dans l'ordre alphabétique"
    Finsi
Fin
```


## <span style="color: #1a02d6"><ins>**Exercice 5.5**</ins></span>

Ecrire un algorithme qui demande un nombre à l’utilisateur, et l’informe ensuite si ce nombre est positif ou négatif (on inclut cette fois le traitement du cas où le nombre vaut zéro).

```
Variables
Nb en Entier

Début
    Ecrire "Veuillez entrer un nombre : "
    Lire Nb
    Si Nb > 0 Alors
        Ecrire "Le nombre saisi est positif."
    SinonSi Nb = 0 Alors
        Ecrire "Le nombre saisi est nul
    Sinon
        Ecrire "Le nombre saisi est négatif
    finSi
fin
```

## <span style="color: #1a02d6"><ins>**Exercice 5.6**</ins></span>

Ecrire un algorithme qui demande deux nombres à l’utilisateur et l’informe ensuite si le produit est négatif ou positif (on inclut cette fois le traitement du cas où le produit peut être nul). Attention toutefois, on ne doit pas calculer le produit !

```
Variables
Nb1, Nb2 en entier 

Début 

    Ecrire (“Veuillez saisir le premier nombre”) 
    Lire (Nb1)
    Ecrire (“Veuillez saisir le second nombre”)
    Lire (Nb2) 
    Si (Nb1 = 0 OU Nb2 = 0) Alors 
        Ecrire (“Le produit de ces nombres est nul”) 
    SinonSi (Nb1 < 0 ET Nb2 < 0) OU (Nb1 > 0 ET Nb2 > 0) Alors
        Ecrire (“Le produit de ces nombres est positif”) 
    Sinon 
        Ecrire (“Le produit de ces nombres est négatif”) 

    Ecrire “Veuillez saisir le premier nombre” 
    Lire Nb1
    Ecrire “Veuillez saisir le second nombre”
    Lire Nb2 
    Si Nb1 = 0 OU Nb2 = 0 Alors 
        Ecrire “Le produit de ces nombres est nul” 
    SinonSi Nb1 < 0 ET Nb2 < 0 OU Nb1 > 0 ET Nb2 > 0 Alors
        Ecrire “Le produit de ces nombres est positif” 
    Sinon 
        Ecrire “Le produit de ces nombres est négatif” 
    Fin Si 
Fin
```

## <span style="color: #1a02d6"><ins>**Exercice 5.7**</ins></span>

Ecrire un algorithme qui demande l’âge d’un enfant à l’utilisateur. Ensuite, il l’informe de sa catégorie :

- "Poussin" de 6 à 7 ans
- "Pupille" de 8 à 9 ans
- "Minime" de 10 à 11 ans
- "Cadet" après 12 ans

Peut-on concevoir plusieurs algorithmes équivalents menant à ce résultat ?

```
Variables
Age en entier

Début
    Ecrire "Afin de connaître la catégorie de votre enfant , entrez son âge : "
    Lire Age
    Si Age >= 12 Alors
        Ecrire "Votre enfant est dans la catégorie Cadet."
    SinonSi Age >= 10 Alors
        Ecrire "Votre enfant est dans la catégorie Minime"
    SinonSi Age >= 8 Alors
        Ecrire "Votre enfant est dans la catégorie Pupille"
    SinonSi Age >= 6 Alors
        Ecrire "Votre enfant est dans la catégorie Poussin"
    Finsi
Fin
```

<span style="color: #26B260">On peut concevoir plusieurs algorithmes équivalents par exemple en commençant par tester l'âge la plus petite par exemple :</span>
=======
<span style="color: #26B260">Alternative :</span>

```
Variables
Age en entier

Début
    Ecrire "Afin de connaître la catégorie de votre enfant , entrez son âge : "
    Lire Age
    Si Age >= 6 Alors 
        Ecrire "Votre enfant est dans la catégorie Poussin"
    SinonSi Age >= 8 Alors
        Ecrire "Votre enfant est dans la catégorie Pupille"
    SinonSi Age >= 10 Alors
    Si Age >= 6 ET Age <= 7 Alors 
        Ecrire "Votre enfant est dans la catégorie Poussin"
    SinonSi Age >= 8 ET Age <= 9 Alors
        Ecrire "Votre enfant est dans la catégorie Pupille"
    SinonSi Age >= 10 ET Age <= 11 Alors
        Ecrire "Votre enfant est dans la catégorie Minime"
    SinonSi Age >= 12 Alors
        Ecrire "Votre enfant est dans la catégorie Cadet."
    Finsi
Fin
```
<span style="color: #26B260">Ou en commençant par une autre catégorie, par exemple tester l'âge pour la catégorie Pupille.</span>

```
Variables
Age en entier

Début
    Ecrire "Afin de connaître la catégorie de votre enfant , entrez son âge : "
    Lire Age
    Si Age >= 8 Alors 
        Ecrire "Votre enfant est dans la catégorie Pupille"
    SinonSi Age >= 6 Alors
        Ecrire "Votre enfant est dans la catégorie Poussin"
    SinonSi Age >= 10 Alors
        Ecrire "Votre enfant est dans la catégorie Minime"
    SinonSi Age >= 12 Alors
        Ecrire "Votre enfant est dans la catégorie Cadet."
    Finsi
Fin
```
<span style="color: #26B260">On peut inverser les tests comme on désire.</span>

