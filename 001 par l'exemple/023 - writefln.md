# Writefln

Pour formatter une chaine et l'écrire sur la console on utilise **writefln** (write format line). 

```D
import std;
void main()
{
    string nom = "Rackam Le Rouge";
    int age = 54;
    double taille = 1.8425;
    
    // Affichage de chaine "%s" et de décimale "%d"
    writefln("nom: %s, age: %d", nom, age);
    
    // Affichage de la taille en différente précision
    writefln("taille: %f", taille);
    writefln("taille: %.02f", taille);
    
    // Affichage de l'age dans différentes bases 
    writeln();
    writefln("age (%d) en binaire %b ", age, age);
    writefln("age (%d) en octal %o ", age, age);
    writefln("age (%d) en hexadecimal %x ", age, age);
    
    // Aligne les informations a droite ou a gauche 
    writeln();
    writefln("|%5s|%-5s|", "*","*"); 
    writefln("|%5s|%-5s|", "**","**");
    writefln("|%5s|%-5s|", "***","***");
    
}
```

## Chaines de formatage standard
Les caractères permettent de mettre en forme le contenu de la variable a interpoller.

|chaine||
|---|---|
|%s| pour l'interpollation de chaine|
|%d| pour de l'entier |
|%f| pour un nombre a virgule flottante |
|%.02f| permet de préciser que l'on veut 2 chiffres après la virgule |