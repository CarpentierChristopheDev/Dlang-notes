# Booléens et branchements conditionnels

Un booléen ne peut avoir que deux valeur : **true** ou **false**.
Les opérateur de comparaisons `==, !=, <, >, <=, >=` retournent une valeur booléenne.

```D
import std;
void main()
{
	bool flag = true;
	
    // Branchement conditionnel 
    if (flag) {
       	writeln("choix 1");
    } else {
        writeln("choix 2");
    }
    
    // Opérateur ternaire 
    int n = flag ? 1 : 2;
    writeln("choix " ~ to!string(n));
}
```

Le type **bool** permet de déclarer une variable booléenne.

la forme compléte du `if` est 
```D
if (condition1) { 
   ... traitement à réaliser si la condition 1 est vrai ... 
} else if (condition2) { 
	... traitement à réaliser si la condition 2 est vrai ...
} else { 
	... traitement à réaliser les conditions au dessus sont fausses ...
}
```

`if` peut déclarer autant de bloc `else if` que nécessaire.

l'opérateur `p ? a : b` retourne *a* si la condition *p* est vrai, ou *b* dans le cas contraire. 

