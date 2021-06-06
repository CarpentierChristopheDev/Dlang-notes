# les nombres décimaux

Pour stocker les nombres décimaux en mémoire, on utilise des type "à virgule flottante".

```D
import std;

void main()
{
    float f = 0.2;
    writeln(f - 0.035f);
    writeln(f);
        
    writeln( 1 - 0.2); 
}
```

Ils sont conforment à la norme [IEEE-754](https://standards.ieee.org/standard/754-2019.html)

les types flottants supportent les mêmes opérateurs que les entiers. `+ - / % ^^` et `++ --`


|  type | taille en bits  |
|---|---|
| float  |  32 |
| double  | 64   |

En cas d'opération entre un entier et un flottant, la conversion de l'entier est implicite.

```D
import std.stdio;

void main()
{
    writeln(2e3);    // ➠ 2000
    writeln(3.4e5);  // ➠ 340000
    writeln(7.8e-3); // ➠ 0.0078
}
```

Les décimaux peuvent être décrit à l'aide de la notation scientifique.