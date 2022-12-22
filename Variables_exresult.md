- [**Exercices ch3**](#exercices-ch3)
  - [**Exercice 3.1**](#exercice-31)
  - [**Exercice 3.2**](#exercice-32)
  - [**Exercice 3.3**](#exercice-33)
  - [**Exercice 3.4**](#exercice-34)
  - [**Exercice 3.5**](#exercice-35)
  - [**Exercice 3.6**](#exercice-36)
  - [**Exercice 3.7**](#exercice-37)
  - [**Exercice 3.8**](#exercice-38)
  - [**Exercice 3.9**](#exercice-39)
  - [**Exercice 3.10**](#exercice-310)

# <span style="color: #1a02d6"><ins>**Exercices ch3**</span>

## <span style="color: #1a02d6"><ins>**Exercice 3.1**</span>

Quelles seront les valeurs des variables A et B après exécution des instructions suivantes ?

```
Variables A, B en Entier
    
Début
    A ← 1           % A = 1  %
    B ← A + 3       % A = 1 ; B = A + 3 soit B = 1 + 3 = 4 %
    A ← 3           % A = 3 ; B = 4 %
Fin
```

<span style="color: #26B260">Les Variables A et B après exécution des instructions suivantes sont :</span>

<span style="color: #26B260"> - A ← 1    : On attribue à **A la valeur 1**</span>

<span style="color: #26B260"> - B ← A + 3 : On attribue à **B la valeur de A + 3** soit **1 + 3** donc **On attribue à B la valeur 4** Et **A garde son attribution inchangée de la ligne précédente soit 1** .</span>

<span style="color: #26B260"> - A ← 3 :On attribue à **A la valeur 3** ; **B garde son attribution inchangée de la ligne précédente soit 4**

## <span style="color: #1a02d6"><ins>**Exercice 3.2**</span>

Quelles sont les valeurs des variables de a, b et c après exécution des instructions suivantes ?
```
Variables a, b, c

Début
    a <- 1          % a = 1 %
    b <- 2          % a = 1 ; b = 2 %
    c <- 3          % a = 1 ; b = 2 ; c = 3 %
    c <- a          % a = 1 ; b = 2 ; c = 1 %
    a <- b          % a = 2 ; b = 2 ; c = 1 %
    b <- c          % a = 2 ; b = 1 ; c = 1 %
    Fin
```
<span style="color: #26B260">Les valeurs des variables de a, b et c après exécution des instructions suivantes sont </span>

<span style="color: #26B260"> - a <- 1    : On attribue à **a la valeur 1**</span>

<span style="color: #26B260"> - b <- 2 : On attribue à **b la valeur 2** ; **a garde son attribution inchangée de la ligne précédente soit 1** .</span>

<span style="color: #26B260"> - c <- 3 : On attribue à **c la valeur 3** ; **a garde son attribution inchangée soit 1** ; **b garde son attribution inchangée soit 2**.</span>

<span style="color: #26B260"> - c <- a : On attribue à **c la valeur de a soit 1** ; **a garde son attribution inchangée soit 1** ; **b garde son attribution inchangée soit 2**.</span>

<span style="color: #26B260"> - a <- b : On attribue à **a la valeur de b soit 2** ; **b garde son attribution inchangée soit 2** ; **c garde son attribution inchangée soit 1**.</span>

<span style="color: #26B260"> - b <- c : On attribue à **b la valeur de c soit 1** ; **a garde son attribution inchangée soit 2** ; **c garde son attribution inchangée soit 1**.</span>

## <span style="color: #1a02d6"><ins>**Exercice 3.3**</span>

Quelles seront les valeurs des variables A, B et C après exécution des instructions suivantes ?
```
Variables A, B, C en Entier

Début
    A ← 5           % A = 5 %
    B ← 3           % A = 5 ; B = 3 %
    C ← A + B       % A = 5 ; B = 3 ; C = 5 + 3 = 8 %
    A ← 2           % A = 2 ; B = 3 ; C = 8 %
    C ← B – A       % A = 2 ; B = 3 ; C = 3 - 2 = 1 %
Fin
```
<span style="color: #26B260">Les valeurs des variables A, B et C après exécution des instructions sont :</span>

<span style="color: #26B260"> - A ← 5    : On attribue à **A la valeur 5**</span>

<span style="color: #26B260"> - B ← 3 : On attribue à **B la valeur 3** ; **A garde son attribution inchangée de la ligne précédente soit 5** .</span>

<span style="color: #26B260"> - C ← A + B : On attribue à **C la valeur de A + B soit 5 + 3 = 8** ; **A garde son attribution inchangée soit 5** ; **B garde son attribution inchangée soit 3**.</span>

<span style="color: #26B260"> - A ← 2 : On attribue à **A la valeur de 2** ; **B garde son attribution inchangée soit 3** ; **C garde son attribution inchangée soit 8**.</span>

<span style="color: #26B260"> - C ← B – A : On attribue à **C la valeur de B – A soit 3 - 2 = 1** ; **A garde son attribution inchangée soit 2** ; **B garde son attribution inchangée soit 3**.</span>


## <span style="color: #1a02d6"><ins>**Exercice 3.4**</span>

Quelles seront les valeurs des variables A et B après exécution des instructions suivantes ?
```
Variables A, B en Entier

Début
    A ← 5               % A = 5 %
    B ← A + 4           % A = 5 ; B = 5 + 4 = 9 %
    A ← A + 1           % A = 5 + 1 = 6 ; B = 9 %
    B ← A – 4           % A = 6 ; B = 6 - 4 = 2 %
Fin
```
<span style="color: #26B260">Les valeurs des variables A et B après exécution des instructions sont :</span>

<span style="color: #26B260"> - A ← 5    : On attribue à **A la valeur 5**</span>

<span style="color: #26B260"> - B ← A + 4    : On attribue à **B la valeur de A + 4 soit 5 + 4 = 9 ; A garde son attribution inchangée soit 5**</span>

<span style="color: #26B260"> - A ← A + 1    : On attribue à **A la valeur de A + 1 soit 5 + 1 = 6 ; B garde son attribution inchangée soit 9 **</span>

<span style="color: #26B260"> - B ← A – 4    : On attribue à **B la valeur de A - 4 soit 6 - 4 = 2 ; A garde son attribution inchangée soit 6**</span>

## <span style="color: #1a02d6"><ins>**Exercice 3.5**</span>

Quelles seront les valeurs des variables A, B et C après exécution des instructions suivantes ?
```
Variables A, B, C en Entier

Début
    A ← 3           % A = 3  %
    B ← 10          % A = 3 ; B = 10 %
    C ← A + B       % A = 3 ; B = 10 ; C = 3 + 10 = 13 %
    B ← A + B       % A = 3 ; B = 3 + 10 = 13 ; C = 13 %
    A ← C           % A = C = 13 ; B = 13 ; C = 13 %
Fin
```
<span style="color: #26B260">Les valeurs des variables A, B et C après exécution des instructions</span>

<span style="color: #26B260"> - A ← 3    : On attribue à **A la valeur 3**</span>

<span style="color: #26B260"> - B ← 10    : On attribue à **B la valeur de 10 ; A garde son attribution inchangée soit 3**</span>

<span style="color: #26B260"> - C ← A + B    : On attribue à **C la valeur de A + B soit 3 + 10 = 13 ; A garde son attribution inchangée soit 3 ; B garde son attribution inchangée soit 10**</span>

<span style="color: #26B260"> - B ← A + B    : On attribue à **B la valeur de A + B soit 3 + 10 = 13 ; A garde son attribution inchangée soit 3 ; C garde son attribution inchangée soit 13**</span>

<span style="color: #26B260"> - A ← C    : On attribue à **A la valeur de C soit 13 ; B garde son attribution inchangée soit 13 ; C garde son attribution inchangée soit 13**</span>



## <span style="color: #1a02d6"><ins>**Exercice 3.6**</span>

Quelles seront les valeurs des variables A et B après exécution des instructions suivantes ?
```
Variables A, B en Entier

Début
    A ← 5       % A = 5   %
    B ← 2       % A = 5 ; B = 2 %
    A ← B       % A = B = 2 ; B = 2 %
    B ← A       % A = 2 ; B = A = 2 %
Fin
```
<span style="color: #26B260">Les valeurs des variables A et B après exécution des instructions sont :</span>

<span style="color: #26B260"> - A ← 5    : On attribue à **A la valeur 5**</span>

<span style="color: #26B260"> - B ← 2    : On attribue à **B la valeur de 2 ; A garde son attribution inchangée soit 5**</span>

<span style="color: #26B260"> - A ← B    : On attribue à **A la valeur de B soit 2 ; B garde son attribution inchangée soit 2**</span>

<span style="color: #26B260"> - B ← A    : On attribue à **B la valeur de A soit 2 ; A garde son attribution inchangée soit 2**</span>


<ins>Moralité :</ins> les deux dernières instructions permettent-elles d’échanger les deux valeurs de B et A ? Si l’on inverse les deux dernières instructions, cela change-t-il quelque chose ?

<span style="color: #26B260"> Les deux dernières instructions ne permettent donc pas d’échanger les deux valeurs de B et A, puisque l’une des deux valeurs (celle de A) est ici écrasée..</span>

<span style="color: #26B260"> Si par contre on inverse les deux dernières instructions soit :</span>

```
Variables A, B en Entier

Début
    A ← 5       % A = 5   %
    B ← 2       % A = 5 ; B = 2 %
    B ← A       % A = 5 ; B = A = 5 %
    A ← B       % A = B = 5 ; B = 5 %
Fin
```
<span style="color: #26B260"> **Le résultat n'est pas du tout le même A et B ont comme valeur attribuées 5 et non 2 comme avant l'inversion des deux dernères instructions.C’est la valeur de B qui sera écrasée. Rien ne change , ça ne permute toujours pas.**.</span>


## <span style="color: #1a02d6"><ins>**Exercice 3.7**</span>

Plus difficile, mais c’est un classique absolu, qu’il faut absolument maîtriser : écrire un algorithme permettant d’échanger les valeurs de deux variables A et B, et ce quel que soit leur contenu préalable. 

<span style="color: #26B260"> On utilise une variable intermédiaire ou temporaire pour faire l'échange</span>

```
VARIABLES
A, B, tmp 

Début
    tmp <- A 
    A <- B 
    B <- tmp 
fin
```
<span style="color: #26B260">On attribue à **C la valeur de A**, puis à la ligne suivante on attribue à **A la valeur de B**; et enfin à la dernière ligne **on récupère par la valeur de C qui a eu comme attribution à la première ligne de la valeur de A qu'on attribue à B**.</span>


## <span style="color: #1a02d6"><ins>**Exercice 3.8**</span>

Une variante du précédent : on dispose de trois variables A, B et C. Ecrivez un algorithme transférant à B la valeur de A, à C la valeur de B et à A la valeur de C (toujours quels que soient les contenus préalables de ces variables).

<span style="color: #26B260">On utilise une variable tampon qu'on appelle **tmp**. On attribue à cette variable **tmp la valeur de C**. Puis on attribue à **C la valeur de B** et on attribue à **B la valeur de A** , enfin on attribue à **A la valeur de tmp** (a qui ont a attribué la valeur de C à la première ligne)</span>

```
VARIABLES
A , B , C et tmp

Début
   tmp ← C
   C ← B
   B ← A
   A ← tmp
Fin 
```

## <span style="color: #1a02d6"><ins>**Exercice 3.9**</span>

Que produit l’algorithme suivant ?

```
Variables A, B, C en Caractères

Début
    A ← "423"
    B ← "12"
    C ← A + B
Fin
```

<span style="color: #26B260">Procédons ligne par ligne pour voir ce que cet algorithme produit :
Dans la déclaration de variables nous avons des caractères.</span>

<span style="color: #26B260">Dejà nous remarquons les guillemets dans l'affection de la valeur des variables.</SPAN>

<span style="color: #26B260">Ensuite on détaille les affectations  :</span>

<span style="color: #26B260">- pour la variable A on  la suite de caractères 4 – 2 – 3,</span>

<span style="color: #26B260">- puis à B la suite de caractères 1 - 2.</span>

<span style="color: #26B260">- puis à C la la somme de caractères attribué à A et B soit "423" et  "12".</span>

<span style="color: #26B260">Il ne peut produire **qu’une erreur d’exécution**, puisqu’on ne peut pas additionner des caractères. </span>


## <span style="color: #1a02d6"><ins>**Exercice 3.10**</span>

Que produit l’algorithme suivant ?
```
Variables A, B, C en Caractères

Début
    A ← "423"
    B ← "12"
    C ← A & B
Fin
```
<span style="color: #26B260">Procédons ligne par ligne pour voir ce que cet algorithme produit :
Dans la déclaration de variables nous avons des caractères.</span>

<span style="color: #26B260">Dejà nous remarquons les guillemets dans l'affection de la valeur des variables.</SPAN>

<span style="color: #26B260">Ensuite on détaille les affectations  :</span>

<span style="color: #26B260">- pour la variable A on  la suite de caractères 4 – 2 – 3,</span>

<span style="color: #26B260">- puis à B la suite de caractères 1 - 2.</span>

<span style="color: #26B260">- puis à B on concatène avec l'opérateur alphanumérique & lescaractères attribué à A et B soit "423" et  "12".</span>

<span style="color: #26B260">Le résultat de l'algorithme est "42312"</span>
