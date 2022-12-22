# **<ins>Exercice 1. Lecture et affichage d’une liste</ins>**

Écrire un algorithme permettant de construire une liste d’entiers naturels strictement positifs à partir
d’une suite entrée au clavier et terminée par 0, puis de l’afficher une fois construite.

## Réponse.

On construit la liste à l’aide de la structure `tantque` (pour détecter la fin de saisie), et on
affiche son contenu en la parcourant à l’aide d’une boucle `pour`.

L'algorithme est le suivant :

```
Algorithme LectureEtAffichageListeEntiers

% Cet algorithme permet de construire une liste d'entiers naturels %
% strictement positifs à partir d'une suite entrée au clavier et   %
% terminée par 0, puis de l'afficher une fois construire           %

VARIABLES
Liste : liste d'entiers naturels
n, i de Type Entiers naturels

Début
    % initialisation %
    liste <- []
    
    % Boucle de lecture des valeurs et de création de la liste %
    liste <- liste + [n]
    
    % On lit la valeur suivante   %
    Entrer n
    
    Tant Que n <> 0
         % On rajoute l'entier n en fin de liste %
         liste <- liste + [n]
      
        % On lit la valeur suivante %
        Entrer n
     FinTantQue
     
     % Boucle de parcours pour affichage
     
     Pour i <- 0 à Len(liste) - 1 
          Afficher liste[i]
     FinPour
 Fin
 ```
 
 ___________________________________________________________________________________________________________________
 
