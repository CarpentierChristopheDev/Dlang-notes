# Les entiers

Les entiers supportent les opérateurs `+ - / % ^^` et `++ --`

```D
import std;
void main()
{

    int m = 100_000_000;
    int n = 0xFFFF; // Base hexadécimale
    n += m;

    writeln(n);
    
    // La conversion au type le plus grand est implicite
    writeln((n + 9_595L));
    writeln((n + 9_595L).stringof);
	
}
```

l'underscore permet de rendre plus lisible les chiffres long, il n'a aucune incidence sur le comportement du programme.

Un entier long peut être déclaré en utilisant la lettre 'L'; Un entier non signé avec 'U'.

la propriété **stringof** permet de renvoyer une représentation textuelle de l'expression.

## Les types entiers

Les types d'entiers signés peuvent représenter un entier négatif ou positif :  

|  type signé | taille en bits  |  Valeurs min | Valeur max  | Valeur initiale  |
|---|---|---|---|---|
| byte  |  8 | -128  | 127  | 0 |
| short  | 16   | -32768  | 32767  | 0 |
| int  | 32  | -2147483648  |  2147483647  | 0 |
| long  | 64  |  -9223372036854775808  |  9223372036854775807  | 0L |

Les types d'entiers non signés ne peuvent représenter qu'un entier positif :

|  type non signé | taille en bits  |  Valeurs min | Valeur max  | Valeur initiale  |
|---|---|---|---|---|
| ubyte  |  8 | 0  | 255  | 0U |
| ushort  | 16   | 0  | 65535  | 0U |
| uint  | 32  | 0  |  4294967295  | 0U |
| ulong  | 64  |  0  |  18446744073709551615  | 0UL |

En cas de doute, vous pouvez toujours utiliser les propriétés des types :

```D
import std;
void main()
{
	writeln("Entiers signés : ");
    writefln("%d et %d", byte.min, byte.max);
    writefln("%d et %d", short.min, short.max);
    writefln("%d et %d", int.min, int.max);
    writefln("%d et %d", long.min, long.max);
    
    writeln("\nEntiers non signés : ");
    writefln("%d et %d", ubyte.min, ubyte.max);
    writefln("%d et %d", ushort.min, ushort.max);
    writefln("%d et %d", uint.min, uint.max);
    writefln("%d et %d", ulong.min, ulong.max);
}
```