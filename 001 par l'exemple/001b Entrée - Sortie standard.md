# Readf

Pour écrire sur la sortie standard, on utilise les fonctions write :
- **write()** pour écrire du texte 
- **writeln()** pour écrire du texte et retourner à la ligne
- **writefln()** pour mettre en forme une chaine, l'afficher et retourner à la ligne 
 
```D
import std.stdio;

int main()
{
	
	string name;
    int age;
	
	write("Bonjour, veuillez entrer votre nom : ");
    readf(" %s\n", &name);
    write("Bonjour ", name, ". Quel est votre age ? ");
    readf(" %d\n", &age);
	writefln("Ok vous avez %d ans.", age);
    writeln("Au plaisir de vous revoir.");

    return 0;

}
```

Pour lire sur l'entrée standard, on utilise les fontion read : 
- **readf()** permet de préciser le type de variable dans lequels va être stocké le flux récupéré.