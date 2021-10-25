# Labo C++ : Exercice 4

## Énoncé :
Ecrire un programme qui demande à l’utilisateur de taper un nombre d'entiers de votre choix qui seront stockés dans un tableau et une chaine de caractère "croissant" ou "deccroissant".
Le programme doit trier le tableau par ordre croissant ou décroissant selon le choix de l'utilisateur et doit afficher le tableau.

Voila le code pour générer un nombre aléatoire pour remplir votre tableau  :
``` cpp
#include<random>
#include<limits>
[...]
    std::default_random_engine generator;
    std::uniform_int_distribution<int> distribution(0, std::numeric_limits<int>::max());
    int unNombreAleatoire = distribution(generator);
[...]
```