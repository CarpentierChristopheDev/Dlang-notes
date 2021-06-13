# Writefln et les tableaux

`writefln` possède une syntaxe de formatage spécifique pour les tableaux qui permet d'afficher les éléments d'une tableau sans avoir a coder de boucle. 

```D
import std;
void main()
{
    
    // Affichage des éléments d'un tableau 
    string[] fruits = ["cerise", "mange", "banane", "fraise"];
    writeln("\nFruits :");
    writefln("%( %s %|- %)", fruits);    

    // Affichage des éléments d'un tableau associatifs
    string[string] cpVilles = ["43390" : "Azérat", "43370" : "Bains" , "43340" : "Barges", "43210" : "Bas en Basset"];
    writeln("\nCP - Villes :");
    writefln("%-( %s (%s) %|\n%)", cpVilles); 
    
}
```

la chaine `%( %s %|- %)` permet de formater les éléments du tableau **fruits** : 
- `%( ... %)` Pour tous les éléments du tableau
- `%s` affichage de l'élément
- `|%-`  séparateur **-** entre les éléments

pour le tableau associatif **cpVilles** :
- `%-( ... %)` Pour tous les éléments du tableau, remarquer le **-** qui indique qu'il ne faut pas afficher les guillements autours des chaines de caractères
- `%s %s`  affichage de l'élément clé et de la valeur
- `|%-`  séparateur **\n** (retour à la ligne) entre les éléments




