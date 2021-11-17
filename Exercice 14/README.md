# Labo C++ : Exercice 14

## Énoncé :

Convertir des coordonées polaires en coordonées cartésiennes :

Coordonées cartésiennes : avec absisse et ordonnée (ex : A(4;2))
Coordonées polaires : avec une distance (r) et un angle en radians (θ) (ex : A(2, 7π/6))

Pour convertir ces corodonées, on utilise les formules : 
	x = r*cos(θ)
	y = r*sin(θ)
	r = 2*cos(θ)
	r² = x² + y²
	tan(θ) = y/x

Ecrivez un programme qui convertit des coordones polaires en coordonées cartésiennes, puis inversement, en stockant l'entrée et la sortie dans des structures. Vous devrez passer ces structures par références à la fonction de convertion. Celle qui ne sera pas modifiée doit etre constante.