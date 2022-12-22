- [**Exercices ch12**](#exercices-ch12)
  - [**Exercice 12.1**](#exercice-121)
  - [**Exercice 12.2**](#exercice-122)
  - [**Exercice 12.3**](#exercice-123)
  - [**Exercice 12.4**](#exercice-124)
  - [**Exercice 12.5**](#exercice-125)
  - [**Exercice 12.6**](#exercice-126)
  - [**Exercice 12.7**](#exercice-127)
  - [**Exercice 12.8**](#exercice-128)
  - [**Exercice 12.9**](#exercice-129)

#  <span style="color: #1a02d6"><ins>**Exercices ch12**</ins></span>

##  <span style="color: #1a02d6"><ins>**Exercice 12.1**</ins></span>

Quel résultat cet algorithme produit-il ?

```
Variable
Truc en Caractère

Début
    Ouvrir "Exemple.txt" sur 5 en Lecture
    Tantque Non EOF(5)
        LireFichier 5, Truc
        Ecrire Truc
    FinTantQue
    Fermer 5
Fin
```

<span style="color: #26B260">Cet algorithme  ouvre le fichier, puis avec la boucle "tant que" le fichier n'est pas fini il le lit et l'affiche à l'écran. Une fois arrivé à la fin il s'arrête et ferme.</span>


## <span style="color: #1a02d6"><ins>**Exercice 12.2**</ins></span>

Ecrivez l’algorithme qui produit un résultat similaire au précédent, mais le fichier texte "Exemple.txt" est cette fois de type délimité (caractère de délimitation : /). On produira à l'écran un affichage où pour des raisons esthétiques, ce caractère sera remplacé avec des espaces.

```
Variable 
Line de Type Caractère
i de Type Entier

Début
    Ouvrir "Exemple.txt" sur 5 en Lecture            % Ouverture du fichier en lecture %
        Tantque Non EOF(5)
            LireFichier 5, Line
            Pour i <- 1 à Len(File)
                Si Mid(Line, i, 1) = "/" Alors        % A chaque fois qu'i détecte le délimiteur "/" %
                    Ecrire " "                      % Il remplace le délimiteur par un espace %
                Sinon
                    Ecrire Mid(Line, i, 1)           % Si il rencontre aucun délimiteur il reproduit le contenu du fichier caractère par caractère %
                FinSi
            i++
            FinPour
        FinTantQue
    Fermer 5                                        % Fermeture du fichier %
Fin
```


## <span style="color: #1a02d6"><ins>**Exercice 12.3**</ins></span>

On travaille avec le fichier du carnet d’adresses en champs de largeur fixe.

Ecrivez un algorithme qui permet à l’utilisateur de saisir au clavier un nouvel individu qui sera ajouté à ce carnet d’adresses.

```
Variables 
Nom * 20, Prenom * 17, Tel * 10, Mail * 20, Ligne de Type Caractères

Début
    Ecrire "Saisissez le nom du nouveau contact : "
    Lire Nom
    Ecrire "Saisissez le prénom du nouveau contact : "
    Lire Prenom
    Ecrire "Saisissez le numéro de téléphone du nouveau contact : "
    Lire Tel
    Ecrire "Saisissez l'adresse mail du nouveau contact : "
    Lire Mail
    Ligne <- Nom & Prenom & Tel & Mail
    Ouvrir "Adresses.txt" sur 1 pour Ajout
        EcrireFichier 1, Ligne
    Fermer 1
Fin
```




## <span style="color: #1a02d6"><ins>**Exercice 12.4**</ins></span>

Même question, mais cette fois le carnet est supposé être trié par ordre alphabétique. L’individu doit donc être inséré au bon endroit dans le fichier.

```
Structure Carnet
    Nom de Type Caractère * 20
    Prenom de Type Caractère * 15
    Tel de Type Caractère * 10
    Mail de Type Caractère * 20
FinStructure

Tableau 
MesContacts[] en Carnet

Variables 
Contact, Nouv en Carnet
i, j de Type Numérique
Insert de Type Booléen

Début
    Ecrire "Saisissez le nom du nouveau contact : "
    Lire Nouv.Nom
    Ecrire "Saisissez le prénom du nouveau contact : "
    Lire Nouv.Prenom
    Ecrire "Saisissez le numéro de téléphone du nouveau contact : "
    Lire Nouv.Tel
    Ecrire "Saisissez l'adresse mail du nouveau contact :"
    Lire Nouv.Mail

    Ouvrir "Adresses.txt" sur 1 pour Lecture
        i <- -1
        Insert <- Faux
        Tantque Non EOF(1)                  % ON copie Adresses dans MesContacts[]  %
            i <- i + 1
            Redim MesContacts[i]
            LireFichier 1, Contact
            Si Contact.Nom > Nouv.Nom ET NON Insert Alors      % Si on trouve le bon endroit à l'insérer on l'insère %
                MesContacts[i] <- Nouv
                Insert <- Vrai
                i <- i + 1
                Redim MesContacts[i]
            FinSi
            MesContacts[i] <- Contact
        FinTantQue
    Fermer 1

    Ouvrir "Adresses.txt" sur 1 pour Ecriture       % On insère le contenu du tableau dans le fichier %
        Pour j <- 0 à i
            EcrireFichier 1, MesContacts[j]
        j++
        FinPour
    Fermer 1
Fin
```

## <span style="color: #1a02d6"><ins>**Exercice 12.5**</ins></span>

Ecrivez un algorithme qui permette de modifier un renseignement (pour simplifier, disons uniquement le nom de famille) d’un membre du carnet d’adresses. Il faut donc demander à l’utilisateur quel est le nom à modifier, puis quel est le nouveau nom, et mettre à jour le fichier. Si le nom recherché n'existe pas, le programme devra le signaler.


```
Structure Carnet
    Nom de Type Caractère * 20
    Prenom de Type Caractère * 15
    Tel de Type Caractère * 10
    Mail de Type Caractère * 20
FinStructure

Tableau
MesContacts[] en Carnet

Variables
Contact en Carnet
Ancien, Nouv de Type Caractère * 20
i, j de Type Numérique
Trouv de Type Booléen

Début
    Ecrire "Saisissez le nom du contact à modifier :"
    Lire Ancien
    Ecrire "Saisissez le nouveau nom du contact à modifier :
    Lire Nouv

    Ouvrir "Adresses.txt" sur 1 pour Lecture         % Ouverture du fichier %
        i <- -1
        Trouv <- Faux
        Tant que NON EOF(1)                     % Copie du contenu d'"Adresses" dans le tableau MesContacts[]  %
            i <- i + 1
            Redim MesContacts[i]
            LireFichier 1, Contact            % Recherche du Contact  %
            Si Contact.Nom = Ancien.Nom Alors     % Si on le trouve on le modifie  %
                Trouv <- Vrai
                Contact.Nom <- Nouv
            FinSi
            MesContacts[i] <- Contact        % On remet le résultat dans le tableau MesContacts[]   %
        FinTantque
    Fermer 1

    Si Trouv Alors                           % On informe l'utilisateur de la modification ou non %
        Ecrire "La Modification de vos contacts a été effectuée !"
    Sinon
        Ecrire "Contact inconnu. Aucune modification n'a été effectuée !!"
    FinSi

    Ouvrir "Adresses.ext" sur 1 pour Ecriture         % On copie l'intégralité du tableau dans le fichiers "Adresses"
        Pour j <- 0 à i
            EcrireFichier 1, MesContacts[j]
        j++
        FinPour
    Fermer 1                                     % Et on le ferme  %
Fin
```

## <span style="color: #1a02d6"><ins>**Exercice 12.6**</ins></span>

Ecrivez un algorithme qui trie les individus du carnet d’adresses par ordre alphabétique.

```
Structure Carnet
    Nom de Type Caractère * 20
    Prenom de Type Caractère * 15
    Tel de Type Caractère * 10
    Mail de Type Caractère * 20
FinStructure

Tableau 
MesContacts[] en Carnet

Variables 
Min en Carnet
i, j , k, PosMin de Type Numérique

Début
    Ouvrir "Adresses.txt" sur 1 pour Lecture        % On Ouvre le Fichier %
        i <- -1
        Tant que Non EOF(1)                             % On recopie le contenue d'"Adresses" Dans un Tableau MesContacts[] %
            i <- i + 1
            Redim MesContacts[i]
            LireFichier 1, MesContacts[i]
        FinTantQue
    Fermer 1

    Pour j <- 0 à i - 1                             % On effectue le tri  %
        Min <- MesContacts[j]
        PosMin <- j
        Pour k <- j + 1 à i
            Si MesContacts[k].Nom < Min.Nom Alors
                Min <- MesContacts[k]
                PosMin <- k
            Finsi
        k++
        FinPour
        MesContacts[PosMin] <- MesContacts[j]
        MesContacts[j] <- Min
    j++
    FinPour

    Ouvrir "Adresses.txt" sur 1 pour Ecriture   % On Copie ensuite le tableau dans "Adresses"
    Pour j <- 0 à i
        EcrireFichier 1, MesContacts[j]
    j++
    FinPour
    Fermer 1
Fin
```

## <span style="color: #1a02d6"><ins>**Exercice 12.7**</ins></span>

Soient Toto.txt et Tata.txt deux fichiers dont les enregistrements ont la même structure. Ecrire un algorithme qui recopie tout le fichier Toto dans le fichier Tutu, puis à sa suite, tout le fichier Tata (concaténation de fichiers).

```
Variable
Line de Type Caractère

Début
    Ouvrir "Tutu.txt sur 1 pour Ajout
        Ouvrir "Toto.txt" sur 2 Pour Lecture
            Tant que NON EOF(2)
                LireFichier 2, Line
                EcrireFichier 1, Line
            FinTantque
        Fermer 2

        Ouvrir "Tata.txt sur 3 Pour Lecture
            Tant que NON EOF(3)
                LireFichier 3, Line
                EcrireFichier 1, Line
            FinTantque
        Fermer 3
    Fermer 1
Fin
```


## <span style="color: #1a02d6"><ins>**Exercice 12.8**</ins></span>

Ecrire un algorithme qui supprime dans notre carnet d'adresses tous les individus dont le mail est invalide (pour employer un critère simple, on considèrera que sont invalides les mails ne comportant aucune arobase, ou plus d'une arobase).

```
Structure Carnet
    Nom de Type Caractère * 20
    Prénom de Type Caractère * 15
    Tel de Type Caractère * 10
    Mail de Type Caractère * 20
FinStructure

Tableau 
MesContacts[] en Carnet

Variables 
Contact, Nouv en Carnet
Nb, i, j de Type Numérique

Début
    Ouvrir "Adresses.txt" sur 1 pour Lecture                        % On ouvre le fichier en Lecture  %
        i <- -1
        Tantque Non EOF(1)
            LireFichier 1, Contact
            Nb <- 0
            Pour i <- 1 à Len(Contact.Mail)
                Si Mid(Contact.Mail, i, 1) = "@" Alors             % On recherche à chaque fois qu'il y a un @ %
                    Nb <- Nb + 1
                FinSi
            i++
            FinPour
            Si Nb = 1 Alors
                i <- i + 1
                Redim MesContacts[i]
                MesContacts[i] <- Contact                           % On recopie dans MesContacts les adresses mails testé au dessus %
            FinSi
        FinTantQue
    Fermer 1

    Ouvrir "Adresses.txt" sur 1 pour Ecriture                     % On ouvre le fichier Adresses.txt pour recopier le tableau MesContacts dedans %
        Pour j <- 0 à i
            EcrireFichier 1, MesContacts[j]
        j++
        FinPour
    Fermer 1
Fin
```

## <span style="color: #1a02d6"><ins>**Exercice 12.9**</ins></span>

Les enregistrements d’un fichier contiennent les deux champs Nom (chaîne de caractères) et Montant (Entier). Chaque enregistrement correspond à une vente conclue par un commercial d’une société.
On veut mémoriser dans un tableau, puis afficher à l'écran, le total de ventes par vendeur. Pour simplifier, on suppose que le fichier de départ est déjà trié alphabétiquement par vendeur.

```
Structure Commerciaux
    Nom en Caractère * 20
    Montant en Numérique
FinStructure

Tableau 
MesCommerciaux[] en Commerciaux

Variables 
NomCom * 20, Ligne, Nom de Type caractère
Somme, Vente de Type Numérique


Début
    Ouvrir "Ventes.txt” sur 1 pour Lecture
        i <- -1
        Somme <- 0
        NomCom <- ""                                % Vide %
        Tantque Non EOF(1)
            LireFichier 1, Ligne
            Nom <- Mid(Ligne, 1, 20)
            Vente <- CNum(Mid(Ligne, 21, 10))          % On utilise la fonction de conversion String to Numérique vu au chapitre 11 %
            Si Nom = NomCom Alors
                Somme <- Somme + Vente
            Sinon
                i <- i + 1
                Redim MesCommerciaux(i)
                MesCommerciaux[i].Nom <- NomCom
                MesCommerciaux[i].Montant <- Somme
                Somme <- 0
                NomCom <- Nom
            FinSi
        FinTantQue
        i <- i + 1
        Redim MesCommerciaux[i]
        MesCommerciaux[i].Nom <- NomCom
        MesCommerciaux[i].Montant <- Somme
    Fermer 1

    Pour j <- 0 à i
        Ecrire MesCommerciaux[j]
    j++
    FinPour
Fin

```

