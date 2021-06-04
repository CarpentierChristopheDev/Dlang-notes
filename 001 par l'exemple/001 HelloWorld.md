# Hello world

```D
import std.stdio;

void main()
{
    writeln("Hello world");
}
```

La fonction **main()** est le point d'entrée du programme. 

La déclaration **import** permet de charger le module *stdio* de la bibliothéque *std* (standard)

le module std.stdio donne accès aux fonctions de lecture et d'écriture sur la console : 
- **write()** pour écrire sur la console   
- **writeln()** pour écrire une ligne et passer à la ligne suivante
- **readln()** pour capter une ligne saisie par l'utilisateur sur la console ...