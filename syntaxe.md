
# Définir une variable

    Variable g en Numérique
    Variables PrixHT, TauxTVA, PrixTTC en Numérique

# Affecter une valeur à une variable

    Toto <- 24
    Tutu <- Tutu + 1
<br>

    Début
        Riri <- "Loulou"
        Fifi <- "Riri"
    Fin

# Concaténer 2 chaines

    Variables A, B, C en Caractère
    Début
        A ← "Gloubi"
        B ← "Boulga"
        C ← A & B
    Fin

# Lire / Ecrire

    Ecrire "Veuillez saisir xxxx"
    Lire Titi
    % ou %
    titi <- Lire

# SI ALORS SINONSI SINON

    Variable Temp en Entier
    Début
        Ecrire "Entrez la température de l'eau :"
        Lire Temp
        Si Temp =< 0 Alors
            Ecrire "C'est de la glace"
        SinonSi Temp < 100 Alors
            Ecrire "C'est du liquide"
        Sinon
            Ecrire "C'est de la vapeur"
        Finsi
    Fin

# Boucles tant que

    Variable Rep en Caractère
    Début
        Ecrire "Voulez vous un café ? (O/N)"
        TantQue Rep <> "O" et Rep <> "N"
            Lire Rep
        FinTantQue
    Fin

<br>

    Variables Truc, Trac en Entier
    Début
        Pour Truc ← 1 à 15
            Ecrire "Il est passé par ici"
            Pour Trac ← 1 à 6
               Ecrire "Il repassera par là"
            Trac Suivant
        Truc Suivant
    Fin

# Tableau

    Tableau Note[11] en Numérique %lors de la déclaration d'un tableau, on précise la plus grande valeur de l'indice, ici le tableau a donc une longeuru de 12%
    Variables Moy, Som en Numérique
    Début
        Pour i ← 0 à 11
            Ecrire "Entrez la note n°", i
            Lire Note[i]
        i Suivant
        Som ← 0
        Pour i ← 0 à 11
            Som ← Som + Note[i]
        i Suivant
        Moy ← Som / 12
    Fin

## Tableau redimensionnement

    Tableau Notes[] en Numérique
    Variable nb en Numérique
    Début
        Ecrire "Combien y a-t-il de notes à saisir ?"
        Lire nb
        Redim Notes[nb-1]
    …
    Fin

## Matrice 

    Tableau Cases[7, 7] en Numérique %tableau de 8 par 8%

## Divers

    % length, size %
    Len("Bonjour, ça va ?")                % vaut      16 %
    Len("")                                % vaut      0 %
<br>

    % substring %
    % Mid(chaine, position_debut_inclus, nombre_de_caracteres_a_partir_du_debut) %
    Mid("Zorro is back", 4, 7)             % vaut      "ro is b" %
    Mid("Zorro is back", 12, 1)            % vaut      "c" %
<br>

    % left %
    Left("Et pourtant…", 8)                % vaut      "Et pourt" %
<br>

    % right %
    Right("Et pourtant…", 4)               % vaut      "t…" %
<br>

    % renvoie l'index si la chaine existe %
    Trouve("Un pur bonheur", "pur")        % vaut       4 %
    Trouve("Un pur bonheur", "techno")     % vaut       0 %
<br>

    % code ascii d'un caractère %
    Asc("N")                               % vaut      78  (renvoie le code ASCII associé)%
<br>

    % partie entière d'un nombre %
    A ← Ent(3,228)                         % (partie entière) A vaut 3 %
<br>

    % modulo %
    A ← Mod(10,3)                          %  A vaut 1 car 10 = 3*3 + 1 %
    B ← Mod(12,2)                          %  B vaut 0 car 12 = 6*2 %
    C ← Mod(44,8)                          %  C vaut 4 car 44 = 5*8 + 4 %
<br>

    % aléatoire %
    Toto ← Alea()                          % On a :    0 =< Toto < 1 %
    Toto ← Alea()*0,30 + 1,35              % générer un nombre entre 1,35 et 1,65 %

# Ouvrir/lire un fichier

    Variables Truc, Nom, Prénom, Tel, Mail en Caractères
    Début
        Ouvrir "Exemple.txt" sur 4 en Lecture
        LireFichier 4, Truc
        Nom ← Mid(Truc, 1, 20)
        Prénom ← Mid(Truc, 21, 15)
        Tel ← Mid(Truc, 36, 10)
        Mail ← Mid(Truc, 46, 20)
    Fin
<br>

    Variable Truc en Caractère
    Début
        Ouvrir "Exemple.txt" sur 5 en Lecture
        Tantque Non EOF(5)
            LireFichier 5, Truc
            …
        FinTantQue
        Fermer 5
    Fin
<br>

    Tableaux Nom[], Prénom[], Tel[], Mail[] en Caractère
    Début
        Ouvrir "Exemple.txt" sur 5 en Lecture
        i ← -1
        Tantque Non EOF(5)
            LireFichier 5, Truc
            i ← i + 1
            Redim Nom[i]
            Redim Prénom[i]
            Redim Tel[i]
            Redim Mail[i]
            Nom[i] ← Mid(Truc, 1, 20)
            Prénom[i] ← Mid(Truc, 21, 15)
            Tel[i] ← Mid(Truc, 36, 10)
            Mail[i] ← Mid(Truc, 46, 20)
        FinTantQue
        Fermer 5
    Fin
<br>

    Ouvrir "Exemple.txt" sur 3 en Ajout
    Variable Truc en Caractère
    Variables Nom*20, Prénom*15, Tel*10, Mail*20 en Caractère

# Structure 

    Structure Bottin
        Nom en Caractère *20
        Prénom en Caractère* 15
        Tel en Caractère *10
        Mail en Caractère* 20
    Fin Structure
<br>

    Variable Individu en Bottin
<br>

    Individu ← "Joker", "Midnight", "0348946532", "allstars@rock.com"
<br>

    Individu.Nom ← "Joker"
    Individu.Prénom ← "Midnight"
    Individu.Tel ← "0348946532"
    Individu.Mail ← "allstars@rockandroll.com"

# Ecrire fichier

    EcrireFichier 3, Individu

# Manip fichier complet 

    Structure Bottin
        Nom en Caractère *20
        Prénom en Caractère* 15
        Tel en Caractère *10
        Mail en Caractère* 20
    Fin Structure

    Tableau mesPotes[] en Bottin

    Début
        Ouvrir "Exemple.txt" sur 3 en Lecture
        i ← -1
        Tantque Non EOF(3)
            i ← i + 1
            Redim mesPotes[i]
            LireFichier 3, mesPotes[i]
        FinTantQue
        Fermer 3

        Ecrire mesPotes[12].Mail
    Fin

# Fonction

    Fonction RepOuiNon() en caractère
        Truc ← ""
        TantQue Truc <> "Oui" et Truc <> "Non"
            Ecrire "Tapez Oui ou Non"
            Lire Truc
        FinTantQue
        Renvoyer Truc
    Fin

     ...
    Ecrire "Etes-vous marié ?"
    Rep1 ← RepOuiNon()
    ...
    Ecrire "Avez-vous des enfants ?"
    Rep2 ← RepOuiNon()
    ...
<br>

    Fonction RepOuiNon(Msg en Caractère) en Caractère
        Ecrire Msg
        Truc ← ""
        TantQue Truc <> "Oui" et Truc <> "Non"
            Ecrire "Tapez Oui ou Non"
            Lire Truc
        FinTantQue
        Renvoyer Truc
    Fin Fonction

    ...
    Rep1 ← RepOuiNon("Etes-vous marié ?")
    ...
    Rep2 ← RepOuiNon("Avez-vous des enfants ?")
    ...

# Procédure

    Procédure Bidule( ... )
        ...
    Fin Procédure

    Appeler Bidule(...)
<br>

    Procédure FirstLast(Msg en Caractère par Valeur, Prems ..., Dern ...)
        ...
        ??? Left(Msg, 1)
        ??? Right(Msg, 1)
        ...
    Fin Procédure

    Variables Amouliner, Alpha, Omega en Caractère
    Amouliner ← "Bonjour"
    Appeler FirstLast(Amouliner, Alpha, Omega)

# Variable globale

    Variable Globale Toto en Numérique

# Tableau associatif

    Tableau associatif REPERTOIRE
<br>

Exemple graphique :

|Index d'accès (clé) | Valeur|
|--|--|
|Alain|0123456789|
|Martin|0223456789|

    Ecrire REPERTOIRE[Alain] %affiche la valeur associée à la clé Alain%
<br>

    Début
        REPERTOIRE <- données                          %le tableau associatif est en mémoire centrale%
        Pour chaque clé INDEX de REPERTOIRE faire          %itération de parcours du tableau%
            Ecrire REPERTOIRE[INDEX]          %n° téléphone de la personne INDEX% 
        FinPour
    Fin
<br>

    %test contient clé%
    SI REPERTOIRE contient clé "Sylvain" ALORS
        ...
    FINSI
<br>

    %créer clé%
    REPERTOIRE["Sylvain"] <- "9876543210"
