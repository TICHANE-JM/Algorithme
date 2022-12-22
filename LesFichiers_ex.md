- [Exercices ch12](#exercices-ch12)
  - [Exercice 12.1](#exercice-121)
  - [Exercice 12.2](#exercice-122)
  - [Exercice 12.3](#exercice-123)
  - [Exercice 12.4](#exercice-124)
  - [Exercice 12.5](#exercice-125)
  - [Exercice 12.6](#exercice-126)
  - [Exercice 12.7](#exercice-127)
  - [Exercice 12.8](#exercice-128)
  - [Exercice 12.9](#exercice-129)

# Exercices ch12

## Exercice 12.1

Quel résultat cet algorithme produit-il ?

    Variable Truc en Caractère
    Début
        Ouvrir "Exemple.txt" sur 5 en Lecture
        Tantque Non EOF(5)
            LireFichier 5, Truc
            Ecrire Truc
        FinTantQue
        Fermer 5
    Fin

## Exercice 12.2

Ecrivez l’algorithme qui produit un résultat similaire au précédent, mais le fichier texte "Exemple.txt" est cette fois de type délimité (caractère de délimitation : /). On produira à l'écran un affichage où pour des raisons esthétiques, ce caractère sera remplacé avec des espaces.

## Exercice 12.3

On travaille avec le fichier du carnet d’adresses en champs de largeur fixe.

Ecrivez un algorithme qui permet à l’utilisateur de saisir au clavier un nouvel individu qui sera ajouté à ce carnet d’adresses.

## Exercice 12.4

Même question, mais cette fois le carnet est supposé être trié par ordre alphabétique. L’individu doit donc être inséré au bon endroit dans le fichier.

## Exercice 12.5

Ecrivez un algorithme qui permette de modifier un renseignement (pour simplifier, disons uniquement le nom de famille) d’un membre du carnet d’adresses. Il faut donc demander à l’utilisateur quel est le nom à modifier, puis quel est le nouveau nom, et mettre à jour le fichier. Si le nom recherché n'existe pas, le programme devra le signaler.

## Exercice 12.6

Ecrivez un algorithme qui trie les individus du carnet d’adresses par ordre alphabétique.

## Exercice 12.7

Soient Toto.txt et Tata.txt deux fichiers dont les enregistrements ont la même structure. Ecrire un algorithme qui recopie tout le fichier Toto dans le fichier Tutu, puis à sa suite, tout le fichier Tata (concaténation de fichiers).

## Exercice 12.8

Ecrire un algorithme qui supprime dans notre carnet d'adresses tous les individus dont le mail est invalide (pour employer un critère simple, on considèrera que sont invalides les mails ne comportant aucune arobase, ou plus d'une arobase).

## Exercice 12.9

Les enregistrements d’un fichier contiennent les deux champs Nom (chaîne de caractères) et Montant (Entier). Chaque enregistrement correspond à une vente conclue par un commercial d’une société.
On veut mémoriser dans un tableau, puis afficher à l'écran, le total de ventes par vendeur. Pour simplifier, on suppose que le fichier de départ est déjà trié alphabétiquement par vendeur.

