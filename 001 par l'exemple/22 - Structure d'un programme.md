# Structure d'un programme

Le point d'entrée d'un programme D est la méthode main

```D
import std.stdio;  
import std.getopt;  
import std.random;  

void main(string[] args)  
{  
    int nombre;  
 	int minimum;  
 	int maximum;  
	getopt(args,
	       "nombre", &nombre, 
		   "minimum", &minimum, 
		   "maximum", &maximum); 
	writefln("tirage de %s nombres entre %s et %s", nombre, minimum, maximum);
	foreach(i; 0 .. nombre) {  
		write( uniform( minimum, maximum + 1), ' ');  
	}  
    writeln();  
}
```

La forme entier de la méthode est `void main(string[] args)`. Généralement, lorsque l'on a pas besoin des arguments, on omettre ce paramétre.

Le module `std.getopt` permet de découper le tableau **args** pour récupérer les valeurs qui nous interessent et de les stocker dans des variables.

Le module `std.random` permet de tirer des nombres au hasard.

Pour demander à mon executable de tirer au hasard 3 nombres entre 10 et 20, je l'appele de la façon suivante : 
```Batch
solHello1.exe --nombre 3 --minimum 10 --maximum 20
```

La syntaxe | dans la chaine permet de définir les raccourcis pour les paramétres

```D
import std.stdio;  
import std.getopt;  
import std.random;  


void main(string[] args)  
{  
    int nombre;  
 	int minimum;  
 	int maximum;  
	getopt(args,
		   "nombre|n", &nombre, 
		   "minimum|m", &minimum, 
		   "maximum|x", &maximum); 
	writefln("tirage de %s nombres entre %s et %s", nombre, minimum, maximum);
	foreach(i; 0 .. nombre) {  
		write( uniform( minimum, maximum + 1), ' ');  
	}  
    writeln();  
}
```

Cela me permet d'appeler mon programme avec la syntaxe "courte" des paramètres : 

```Batch
solHello1.exe -n3 -m10 -x20
```
