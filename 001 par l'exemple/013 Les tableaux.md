Un tableau est une séquence d'éléments de même type indexés à partir de 0.

## Tableau fixe

La taille du tableau est fixée à la déclaration et ne peut pas être modifiée. 

```D
import std;

void main()
{

    // Crée un tableau fixe de 10 entiers
    int[10] tabEntiers = [21, 3, 25, 10, 100, 155, 45, 85, 15, 8];
    writeln(tabEntiers);

    writeln("Nombre d'élément dans le tableau : ", tabEntiers.length);

    writeln("Premier élément du tableau : ", tabEntiers[0]);
    writeln("5eme élément du tableau : ", tabEntiers[4]);
    writeln("8eme élément du tableau : ", tabEntiers[7]);
    writeln("Dernier élément du tableau : ", tabEntiers[$ - 1]);
    writeln("8eme élément du tableau : ", tabEntiers[$ - 3]); // 3ene en partant de la fin

    // Modification d'elements
    tabEntiers[4] = 200; // Fixe la valeur du 5eme élément à 200
    tabEntiers[7] += 100; // Augmente la valeur du 8eme élément de 100

    writeln(tabEntiers);

}
```

 `int[10]` réserve 10 emplacements mémoire pour contenir 10 entiers contaigus (de 32 bits chacuns)
 
 La propriété **Length** retourne le nombre le nombre d'éléments contenu dans le tableau. 
 
 dans l'expression tabEntiers `tabEntiers[$ - 1]`, qui désigne le dernier élément du table (le premier en partant de la fin),  le symbole `$` fait référence à la propriété **Length**
 
 C'est une forme allégée de  `tabEntiers[tabEntiers.length - 1]`
 
 On peut créer des tableau d'entier, de chaines, de booléens ... 