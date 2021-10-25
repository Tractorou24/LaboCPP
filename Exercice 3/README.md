# Labo C++ : Exercice 3

## Énoncé :
Écrire un programme qui demande à l'utilisateur de saisir 10 entiers stockés dans un tableau ainsi qu'un entier V. Le programme doit rechercher si V se trouve dans le tableau et afficher "V se trouve dans le tableau" ou "V ne se trouve pas dans le tableau".

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