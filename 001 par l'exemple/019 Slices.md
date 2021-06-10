# Les slices 

Les slices permettent de créer des vues sur une partie d'un tableau. 

Cela ne crée pas un nouveau tableau, toute modification apportée au tableau est visible dans la slice et réciproquement.

```D
import std;

void main()
{
    
    char[] lettres = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h'];

    writeln(lettres);

    char[] g1 = lettres[0 .. 3];
    char[] g2 = lettres[3 .. 7];
    char[] g3 = lettres[5 .. 8];

    afficheGroupes(g1,g2,g3);

    lettres[1] = '0';
    lettres[7] = '1';

    afficheGroupes(g1,g2,g3);
    
    g2[1] = 'X'; // Elément d'index 1 du second groupe 
    
    afficheGroupes(g1,g2,g3);
    
    writeln('\n', lettres);
    
}

void afficheGroupes(char[] g1,char[] g2,char[] g3)
{
    writeln('\n', g1);
    writeln(g2);
    writeln(g3);
}
```

Dans l'exemple, nous définisons le tableau et les slices suivante : 

|index|0|1|2|3|4|5|6|7
|---|---|---|---|---|---|---|---|---|
|caractère|a|b|c|d|e|f|g|h|
|g1|0|1|2||||||
|g2||||0|1|2|3||
|g3||||||0|1|2|

On peut définir plusieurs slices sur un même tableau qui se chevauchent.

On modifie : 
- Les caractères du tableau à l'index 1 et 7 
- Le caractère à l'index **1** de la slice **g2** -->  qui correspond à l'index 4 du tableau d'origine



