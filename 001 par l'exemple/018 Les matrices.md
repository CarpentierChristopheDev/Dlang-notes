# Les matrices

Les matrices sont des tableaux de tableaux. 

```D
import std;

void main()
{

    // Tableau dynamique à deux dimension 
    int[][] matNombres = [[1, 2, 3], [11, 12, 13], [21, 22, 23]];
    writeln(matNombres);

    // Ajout d'un nouveau tableau au tableau initial
    matNombres ~= [31, 32];
    writeln(matNombres);

    // Ajout d'éléments dans le premier tableau (d'index 0)
    matNombres[0] ~= 4;
    writeln(matNombres);

    //Parcours des éléments à l'aide de deux boucles foreach imbriquées
    foreach (ligne; matNombres)
    {
        foreach (element; ligne)
        {
            write(element," ");
        }
        writeln();
    }

}
```

On peut créer des matrices avec des tableaux fixes.

```D
	double [6][3] matrix = 0;
```

Crée une matrice de  3 lignes de 6 éléments chacuns de type double initialisés à 0. 