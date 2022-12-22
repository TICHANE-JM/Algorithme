
# <span style="color: #1a02d6"><ins>**Exercices ch11**</ins></span>

## <span style="color: #1a02d6"><ins>**Exercice 11.1**</ins></span>

Parmi ces affectations (considérées indépendamment les unes des autres), lesquelles provoqueront des erreurs, et pourquoi ?
```
Variables A, B, C en Numérique
Variable D en Caractère
A ← Sin(B)
A ← Sin(A + B * C)
B ← Sin(A) – Sin(D)
C ← Sin(A / B)
C ← Cos(Sin(A)
```
```
A ← Sin(B)              Aucune erreur

A ← Sin(A + B * C)      Aucune erreur

B ← Sin(A) – Sin(D)     Erreur ! D est une Variable en caractère.

C ← Sin(A / B)          Aucune erreur à condition que B soit différent de zéro.

C ← Cos(Sin(A)          Erreur ! pas de parenthèse fermante
```


## <span style="color: #1a02d6"><ins>**Exercice 11.2**</ins></span>

Ecrivez un algorithme qui demande un mot à l’utilisateur et qui affiche à l’écran le nombre de lettres de ce mot (c'est vraiment tout bête).

```
Variables 
Mot en Caractère
Nb en Entier

Début
    Ecrire "Veuillez saisir un mot : "
    Lire Mot
    Nb <- Len(Mot)            % Len(chaîne) : renvoie le nombre de caractères d’une chaîne %
    Ecrire "Le mot saisi contient ", Nb, " lettres"
Fin
```

## <span style="color: #1a02d6"><ins>**Exercice 11.3**</ins></span>

Ecrivez un algorithme qui demande une phrase à l’utilisateur et qui affiche à l’écran le nombre de mots de cette phrase. On suppose que les mots ne sont séparés que par des espaces (et c'est déjà un petit peu moins bête).


```
Variables 
Phra en Caractère
Nb, i en Entier

Début
    Ecrire "Tapez votre phrase : "
    Lire Phra
    Nb <- 0
    Pour i <- 1 à Len(Phra)                      % Len(Phra)  : renvoie le nombre de caractères de la phrase tapée %
        Si Mid(Phra, i , 1) = " " Alors          % Mid(Phra,i,1) :** renvoie un extrait de la phrase, commençant au caractère i (1) et faisant 1 caractère de long %
            Nb <- Nb + 1
        FinSi
    i++
    Ecrire "La phrase tapée comporte ", Nb + 1, " mots"
Fin
```


## <span style="color: #1a02d6"><ins>**Exercice 11.4**</ins></span>

Ecrivez un algorithme qui demande une phrase à l’utilisateur et qui affiche à l’écran le nombre de voyelles contenues dans cette phrase.

On pourra écrire deux solutions. La première déploie une condition composée bien fastidieuse. La deuxième, en utilisant la fonction Trouve, allège considérablement l'algorithme.

**<ins>Solution 1 :</ins>**

```
Variables
Phra en Caractère
Nb, i, j en Entier

Début
    Ecrire "Tapez votre phrase : "
    Lire Phra
    Nb <- 0
    Pour i <- 1 à Len(Phra)          % Len(Phra)  : renvoie le nombre de caractères de la phrase tapée %
        Si Mid(Phra, i, 1) = "a" OU Mid(Phra, i, 1) = "e" OU Mid(Phra, i, 1) = "i" OU Mid(Phra, i, 1) = "o" OU Mid(Phra, i, 1) = "u" OU Mid(Phra, i, 1) = "y" Alors
            Nb ← Nb + 1
        FinSi
    i++
    Ecrire "La phrase tapée comporte ", Nb, " voyelles"
Fin
```
**<ins>Solution 2 :</ins>** On stocke toutes les voyelles dans une variable de type chaîne. Avec la fonction Trouve, on detecte si le caractère examiné est une voyelle ou non.

```
Variables 
Phra , Voy en Caractère
Nb, i, j en Entier

Début
    Ecrire "Tapez votre phrase : "
    Lire Phra
    Nb <- 0
    Voy <- "aeiouy"
    Pour i <- 1 à Len(Phra)
        Si Trouve(Voy, Mid(Phra, i, 1)) <> 0 Alors             % Trouve(Voy,Mid(Phra, i, 1)) : renvoie le nombre de Voyelle dans la Phrase entrée. %
            Nb <- Nb + 1
        FinSi
    i++
    Ecrire "La phrase tapée comporte ", Nb, " voyelles"
Fin
```

## <span style="color: #1a02d6"><ins>**Exercice 11.5**</ins></span>

Ecrivez un algorithme qui demande une phrase à l’utilisateur. Celui-ci entrera ensuite le rang d’un caractère à supprimer, et la nouvelle phrase doit être affichée (on doit réellement supprimer le caractère dans la variable qui stocke la phrase, et pas uniquement à l’écran).


```
Variables 
Phra en Caractère
Nb, i, j en Entier

Début
    Ecrire "Tapez votre phrase : "
    Lire Phra
    L <- Len(Phra)
    Ecrire "Entrez le rang du caractère à supprimer : "
    Lire Nb

    Phra <- Mid(Phra, 1, Nb – 1) & Mid(Phra, Nb + 1, L – Nb)         % On concatène ce qui se trouve à gauche du caractère à supprimer avec ce qui se trouve à sa droite. %

    Ecrire "La nouvelle phrase est : ", Phra
Fin
```

## <span style="color: #1a02d6"><ins>**Exercice 11.6 - Cryptographie 1**</ins></span>

Un des plus anciens systèmes de cryptographie (aisément déchiffrable) consiste à décaler les lettres d’un message pour le rendre illisible. Ainsi, les A deviennent des B, les B des C, etc. Ecrivez un algorithme qui demande une phrase à l’utilisateur et qui la code selon ce principe. Comme dans le cas précédent, le codage doit s’effectuer au niveau de la variable stockant la phrase, et pas seulement à l’écran.



```
Variables 
Phra, Codee, Alpha, Tmp en Caractère
i, Pos en Entier

Début
    Alpha <- "ABCDEFGHIJKLMNOPQRSTUVWXYZ"
    Codee <- ""                               % Vide %
    Ecrire "Entrez la phrase à coder : "
    Lire Phra

    Pour i <- 1 à Len(Phra)
        Tmp <- Mid(Phra, i, 1)                        % Mid(Phra,i,1) renvoie les caractères de la Phrase, commençant du 1er caractère i et faisant 1 caractère de long dans Tmp %

        Si Tmp <> "Z" Alors                            % Cas particulier de la 26ème lettre %
            Pos <- Trouve(Alpha, Tmp)                   % Trouve(Alpha,Tmp) Donne la position de chaque caractère de Tmp dans Alpha  %
            Codee <- Codee & Mid(Alpha, Pos + 1, 1)     % Mid(Alpha,Pos + 1,1)  Renvoi les nouveaux caractères et les concatènes avec Codee vide initialisé au départ. %
        Sinon
            Codee <- Codee & "A"
        FinSi
    i++
    Phra <- Codee
    Ecrire "La phrase codée est : ", Phra
Fin
```

## <span style="color: #1a02d6"><ins>**Exercice 11.7 - Cryptographie 2 - le chiffre de César**</ins></span>

Une amélioration (relative) du principe précédent consiste à opérer avec un décalage non de 1, mais d’un nombre quelconque de lettres. Ainsi, par exemple, si l’on choisit un décalage de 12, les A deviennent des M, les B des N, etc.
Réalisez un algorithme sur le même principe que le précédent, mais qui demande en plus quel est le décalage à utiliser. Votre sens proverbial de l'élégance vous interdira bien sûr une série de vingt-six "Si...Alors"

```
Variables 
Phra, Codee, Alpha ,Tmp en Caractère
i, Pos,  Décal en Entier

Début
    Alpha <- "ABCDEFGHIJKLMNOPQRSTUVWXYZ"
    Codee <- ""                               % Liste Vide %
    Ecrire "Entrez la phrase à coder : "
    Lire Phra
    Ecrire "Entrez le décalage à appliquer : "
    Lire Décal

    Pour i <- 1 à Len(Phra)                  % Pour chaque lettre dans la Phrase %
        Tmp <- Mid(Phra, i, 1)               % Mid(Phra,i,1) renvoie les caractères de la Phrase, commençant du 1er caractère i et faisant 1 caractère de long dans une liste tampon Tmp %

        Pos <- Trouve(Alpha, Tmp)            % Trouve(Alpha,Tmp) Détecte la position de chaque carac dans Tmp dans Alpha , la lettre de Phrase devient un chiffre (la Position) %

        NouvPos <- (Pos + Décal) % 26      % On effectue le chiffrement, on donne la nouvelle position %

        Si NouvPos = 0 Alors
            NouvPos <- 26
        FinSi

        Codee <- Codee & Mid(Alpha, NouvPos, 1)       % Retour aux lettres : Mid(Alpha,NouvPos,1) renvoie les caractères d'Alpha, commençant du 1er caractère de NouvPos et faisant 1 caractère de long et le concatène avec la chaine vide qu'on a initialisé au départ. %
    i++

    Phra <- Codee
Ecrire "La phrase codée est : ", Phra
Fin
```

## <span style="color: #1a02d6"><ins>**Exercice 11.8 - Cryptographie 3**</ins></span>

Une technique ultérieure de cryptographie consista à opérer non avec un décalage systématique, mais par une substitution aléatoire. Pour cela, on utilise un alphabet-clé, dans lequel les lettres se succèdent de manière désordonnée, par exemple :
```
HYLUJPVREAKBNDOFSQZCWMGITX
```
C’est cette clé qui va servir ensuite à coder le message. Selon notre exemple, les A deviendront des H, les B des Y, les C des L, etc.

Ecrire un algorithme qui effectue ce cryptage (l’alphabet-clé sera saisi par l’utilisateur, et on suppose qu'il effectue une saisie correcte).

```
Variables 
Phra, Codee, Alpha, AlphaCle, Tmp en Caractère
i, Pos, en Entier

Début
    Alpha <- "ABCDEFGHIJKLMNOPQRSTUVWXYZ"
    Codee <- ""                                 % Liste Vide  %

    Ecrire "Entrez l’alphabet-clé qui servira à crypter la phrase : "
    Lire AlphaCle

    Ecrire "Entrez la phrase à crypter : "
    Lire Phra

    Pour i <- 1 à Len(Phra)                 % Pour chaque lettre dans la Phrase %
        Tmp <- Mid(Phra, i, 1)              % Mid(Phra,i,1)renvoie les caractères de la Phrase, commençant du 1er caractère i et faisant 1 caractère de long dans la liste Tampon Tmp %
        Pos <- Trouve(Phra, Tmp)            % Trouve(Phra,Tmp) Donne la position de chaque caractère de Tmp dans Phra et l'assigne à Pos, la lettre deviens un nombre %
        Codee <- Codee & Mid(AlphaCle, Pos, 1)    % Mid(AlphaCle, Pos, 1) Retour du Nombre à la lettre et le concatène avec la liste vide qu'on a initialisé au départ %
    i++
    Phra <- Codee
    Ecrire "La phrase codée est : ", Phra
Fin
```


## <span style="color: #1a02d6"><ins>**Exercice 11.9 - Cryptographie 4 - le chiffre de Vigenère**</ins></span>

Un système de cryptographie beaucoup plus difficile à briser que les précédents fut inventé au XVIe siècle par le français Vigenère. Il consistait en une combinaison de différents chiffres de César.

On peut en effet écrire **25 alphabets décalés par rapport à l’alphabet normal** :
- l’alphabet qui commence par **B** et finit par **…YZA**
- l’alphabet qui commence par **C** et finit par **…ZAB**
- etc.
  
Le codage va s’effectuer sur **le principe du chiffre de César :** on remplace la lettre d’origine par la lettre occupant la même place dans l’alphabet décalé.

Mais à la différence du chiffre de César, un même message va utiliser non un, mais plusieurs alphabets décalés. Pour savoir quels alphabets doivent être utilisés, et dans quel ordre, on utilise une clé.

Si cette clé est **"VIGENERE"** et le message "Il faut coder cette phrase", on procèdera comme suit :

- La première lettre du message, I, est la 9e lettre de l’alphabet normal. Elle doit être codée en utilisant l’alphabet commençant par la première lettre de la clé, V. Dans cet alphabet, la 9e lettre est le D. I devient donc D.
- La deuxième lettre du message, L, est la 12e lettre de l’alphabet normal. Elle doit être codée en utilisant l’alphabet commençant par la deuxième lettre de la clé, I. Dans cet alphabet, la 12e lettre est le T. L devient donc T, etc.
- Quand on arrive à la dernière lettre de la clé, on recommence à la première.
  
Ecrire l’algorithme qui effectue un cryptage de Vigenère, en demandant bien sûr au départ la clé à l’utilisateur.


```
Variables 
Alpha, Phra, Crypt, Key, Tmp, TmpKey en Caractère
i, Pos, PosKey, PosTmpKey, NouvPos en Entier

Début
    Alpha <- "ABCDEFGHIJKLMNOPQRSTUVWXYZ"
    Crypt <- ""
    PosKey <- 0
    Ecrire "Entrez la clé de cryptage que vous souhaitez utiliser : "
    Lire Key
    Ecrire "Saisissez le message à Crypter : "
    Lire Phra
    
    Pour i <- 1 à Len(Phra)                     % Pour chaque lettre dans la Phrase %

        PosKey <- (PosKey + 1) % Len(Phra)      % On Progresse dans la clé %
    
        TmpKey <- Mid(Key, PosKey, 1)           % renvoie les caractères de la Clé, commençant du 1er caractère de PosKey et faisant 1 caractère de long dans la liste Tampon Tmp %

        PosTmpKey <- Trouve(Alpha, TmpKey)      % On détermine la lettre clé et sa position dans la liste Alpha et on l'assigne à PosTmpKey la Lettre devient un nombre %

        Tmp <- Mid(Phra, i, 1)                 % renvoie les caractères de la Phrase, commençant du 1er caractère i et faisant 1 caractère de long dans la liste Tampon Tmp %

        Pos <- Trouve(Alpha, Tmp)              % Donne la position de chaque caractère de Tmp dans Phra et l'assigne à Pos, la lettre devient un nombre %

        NouvPos <- (Pos + PosTmpKey) % 26      % On effectue le chiffrement, on donne la nouvelle position %

        Crypt <- Crypt & Mid(Alpha, NouvPos, 1) % Le nombre redevient Lettre %
    i++
    FinPour
    Ecrire "Le message crypté est : ", Crypt
Fin
```

## <span style="color: #1a02d6"><ins>**Exercice 11.10**</ins></span>

Ecrivez un algorithme qui demande un nombre entier à l’utilisateur. L’ordinateur affiche ensuite le message "Ce nombre est pair" ou "Ce nombre est impair" selon le cas.
*
```
Variable 
Nb en Entier

Début
    Ecrire "Saisissez votre nombre : "
    Lire Nb
    Si Nb % 2 = 0 Alors
        Ecrire "Ce nombre est pair"
    Sinon
        Ecrire "Ce nombre est impair"
    FinSi
Fin
```

```
Variable 
Nb en Entier

Début
    Ecrire "Saisissez votre nombre : "
    Lire Nb
    Si Nb/2 = Ent(Nb/2) Alors           % Si Nb / 2 est un entier %
        Ecrire "Ce nombre est pair"
    Sinon
        Ecrire "Ce nombre est impair"
    FinSi
Fin

```

## <span style="color: #1a02d6"><ins>**Exercice 11.11**</ins></span>

Ecrivez les algorithmes qui génèrent un nombre Glup aléatoire tel que …
- 0 =< Glup < 2
- –1 =< Glup < 1
- 1,35 =< Glup < 1,65
- Glup émule un dé à six faces
- –10,5 =< Glup < +6,5
- Glup émule la somme du jet simultané de deux dés à six faces


```
Variables
Glup En numérique

Début
    Glup <- Alea() * 2            %  0 =< Glup < 2 %
    Glup <- Alea() * 2 + (-1)     %   –1 =< Glup < 1  %
    Glup <- Alea() * 0,30 + 1,35  %   1,35 =< Glup < 1,65 %
    Glup <- Ent(Alea() * 6) + 1   %  Glup émule un dé à six faces équivalent à 1=< Glup < 6 (voir plus bas) %
    Glup <- Alea() * 17 + (- 10,5)  %   –10,5 =< Glup < +6,5
    Glup <- (Ent(Alea() * 6) + 1) + (Ent(Alea() * 6) + 1)    %  Glup émule la somme du jet simultané de deux dés à six faces. On additionne l'émulation de chaque dés. %
fin 
```
<span style="color: #26B260">Alea() fournit un nombre décimal de l'intervalle [0 ; 1 [ , Alea() * 6 fournit un nombre décimal de l'intervalle [0 ; 6 [ . En prenant la partie entière Ent(Alea() * 6) on obtient alors un nombre entier d'élément de l'ensemble {0 ; 1 ; 2 ; 3 ; 4 ; 5} En y ajoutant 1 soit Ent(Alea() * 6) + 1 On obtient bien les  6 faces du dé soit : {1 ; 2 ; 3 ; 4 ; 5 ; 6}