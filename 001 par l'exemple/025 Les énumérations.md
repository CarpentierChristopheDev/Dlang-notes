# Les énumérations

Elle permettent de déclarer un type comme ayant une valeur restrainte à une liste finie de valeurs.

```D
import std;

void main()
{

    // Enumération 
    enum jours {lundi, mardi, mercredi, jeudi, vendredi, samedi, dimanche}
    jours j = jours.mercredi;
    writeln("valeur de j: ", j);
    
    // propriétés de jours 
    writeln("valeur minimale de jours: ", jours.min);
    writeln("valeur maximale de jours: ", jours.max);
    writeln("taille de jours: ", jours.sizeof); // Jours est un int donc 4 octets
	writeln();
        
    // Enumération 
    enum couleurs {rouge=0xFF0000, vert=0x00FF00, bleu=0x0000FF}
    couleurs c = couleurs.vert;
   
    // Affichage de  la valeur de la variable
    writefln("valeur enumérée : %s ", c);
    writefln("valeur hexadecimal : %x ", c);
    
}
```

D affiche nativement le nom d'une variable énumérée et non sa valeur. 

Les valeurs énumérés sont par défault de type **int** donc stocké sur 4 octects.

Si la valeur n'est pas précisée, D attribue la valeur 0 au premier élément puis incrémente la valeur. 

