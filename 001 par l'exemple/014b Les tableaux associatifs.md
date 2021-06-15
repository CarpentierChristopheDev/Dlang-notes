Un tableau associatif, ou dictionnaire, permet d'associer une valeur à chaque clée. 

```D
import std;

void main()
{

    // Tableau associatif
    int[string] joursCode = ["lun": 0, "mar": 1, "mer": 2];
    joursCode["jeu"] = 3; // Ajout d'élément
    joursCode["ven"] = 4;
    joursCode.remove("lun"); // Retrait d'élément
    writeln(joursCode);

    // Propriétés d'un tableau associatif 
    writeln("taille : ", joursCode.length);
    writeln("clées : ", joursCode.keys);
    writeln("valeurs : ", joursCode.values);
    
    // Parcours
    foreach (string s, int i; joursCode)
    {
        writefln("joursCode['%s'] = %d", s, i);
    }

}
```

`int[string] joursCode` déclare un tableau associatif dont les clées sont de type chaines et qui va contenir des valeurs entières.

La boucle `foreach` possède une syntaxe qui permet de balayer les clées et les valeurs associées.

```D
import std;

void main()
{

    // Tableau associatif
    int[string] joursCode = ["lun": 0, "mar": 1, "mer": 2];

    /+ Recherche d'une clée dans le tableau
       Retourne : 
       - null si la clée est non trouvée
       - un pointeur sur l'élément si la clée est trouvée +/
    writeln("sam." in joursCode); // Teste existance de la clée

    int* pMer = "mer" in joursCode;
    if (pMer !is null)
    {
        writeln(*pMer);
    }

}
```

La recherche d'une clée dans un tableau associatif se fait avec l'opérateur `in` et retourne **null** ou l'adresse mémoire de l'élément.



