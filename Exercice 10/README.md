# Labo C++ : Exercice 10

## Énoncé :

- Écrire un programme permettant d'entrer un nombre donné de personnes et de les afficher.

La structure personne est : 
```cpp
struct Personne
{
	std::string nom, prenom;
	int age;
};
```

La fonction devra prendre en paramètre un `const size_t&` pour le nombre de personnes.