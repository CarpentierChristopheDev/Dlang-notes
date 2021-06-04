# Propriétés de types 

```D
import std;
void main()
{
    // Taille et valeurs adminisible du type int 
    writefln("Un entier occupe %s octects en mémoire", int.sizeof);
    writefln("Un entier peut représenter une valeur comprise entre %d et %d", int.min, int.max);
    
}
```

Les types ont des propriétés 
- .stringof retourne une représentation du type ou de la variable
- .sizeof retourne la taille en octect 
- .min .max
- .init retourne la valeur utilisé à l'initialisation 
