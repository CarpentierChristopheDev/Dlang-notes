# Les boucles FOR et FOREACH

Elles permettent d'executer du code un certain nombre de fois, ou pour chaque élément d'un tableau.

```D
import std;

void main()
{
    // Boucle qui affiche les chiffres
    for (int i; i < 10; i++)
    {
        writeln(i);
    }

    // Affiche les chiffres par itération 
    foreach (i; 0 .. 10)
    {
        writeln(i);
    }

    // Affiche le contenu d'un tableau en utilisant l'index 
    string[] fruits = [
        "cerise", "mangue", "banane", "fraise", "pomme", "citron"
    ];
    for (int i; i < fruits.length; i++)
    {
        writeln(fruits[i]);
    }

    // Affiche le contenu d'un tableau par itération 
    foreach (fruit; fruits)
    {
        writeln(fruit);
    }

}
```

## La boucle FOR
`for (int i; i < 10; i++)` :
- Déclare une variable `i` (à 0)
- Execute le bloc de code tant que `i < 10`
- Incrémente la valeur de i après l'execution du bloc de code, donc **i** vaut 0, puis 1, puis 2, ... 

## La boucle FOREACH 
`foreach (i; 0 .. 10)` : 
- Pour chaque élément du tableau (`0 .. 10` correspond au tableau [0, 1, 2, 3, 4, 5, 6, 7, 8, 9])
- Recopie la valeur de l'élément en cours de lecture dans la variable `i`
- Execute le bloc de code

