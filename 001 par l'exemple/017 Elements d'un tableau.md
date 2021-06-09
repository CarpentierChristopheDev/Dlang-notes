# Elements d'un tableau

On doit régulièrement réaliser une opération pour tous les éléments d'un tableau.

On peut réaliser cette opération avec un boucle, mais de nombreux opérateurs 
(`+ - / % ^^`, `++ --` ...) permettent de travailler directement sur chaque élément du tableau.

```D
import std;

void main()
{

    // Réaliser une opération sur chaque élément d'un tableau 
    // Avec une boucle
    int[] tabChiffres = [1, 2, 3];
    int[] tabResultats;
    for (int i = 0; i < tabChiffres.length; i++)
    {
        tabResultats ~= tabChiffres[i] + 4;
    }
    writeln(tabResultats);

    // Réaliser une opération sur chaque élément d'un tableau 
    int[] tabResultats2;
    tabResultats2[] = tabChiffres[] + 4;
    writeln(tabResultats);

    // On peut appliquer l'opérateur de type +=, -= ... sur le tableau lui-même
    tabChiffres[] += 4;
    writeln(tabChiffres);

}
```

`tabResultats2[] = tabChiffres[] + 4;`  Cette seule ligne :
- lit chaque élément **tabChiffres**
- lui ajoute 4
- mémorise le résultat dans le tableau **tabResultats2** 

 `tabChiffres[] += 4;` fait de même, mais stoke le résultat dans le tableau lui-même.

