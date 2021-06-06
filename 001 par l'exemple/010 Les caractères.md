# Les caractères

Les caractères sont délimités par des `'`

```D
import std.stdio;

void main()
{
    char a = 'a';
    char excla = '\x21';
    dchar web = '\u20a9';
    dchar euro = '\&euro;';

    writeln(a, excla, web, euro);
}
```

On peut définir un caractère en :
- tapant le caractère, 
- en indiquant son code 
- en précisant sa référence d'entité HTML

D support 3 types de caractère pour travailler avec Unicode : 

|  type | taille en bits |
|---|---|
| char  | 8 |
| dchar  | 16 |
| wchar  | 32 |




