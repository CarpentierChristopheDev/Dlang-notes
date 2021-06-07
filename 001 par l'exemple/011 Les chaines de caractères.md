# Les chaines de caractères

Les chaines de caractères sont des séquences immutables de caractères. 

```D
import std;

void main()
{
   
   string poignéeDeMain = "🤝";
    string salutation = "\&Bfr;onjour" ~ " " ~ poignéeDeMain;
    writeln(salutation);

    writeln("ceci est une chaine 
qui s'étend sur 
plusieurs lignes");

}
```

Les caractères dans les chaines peuvent être représenté : 
- à partir de leur lettre
- avec le code unicode `\u....`
- depuis l'entité HTML `\&...;`

L'opérateur `~` permet la concaténation.

D support 3 types de chaines de caractères pour travailler avec Unicode : 

|  type | Format |
|---|---|
| string  | UTF-8 |
| dstring  | UTF-16 |
| wstring  | UTF-32 |

```D
import std;

void main()
{

    writeln(q"MON_DELIMITEUR
ceci est une chaine qui 
s'étend sur plusieurs lignes
MON_DELIMITEUR");
            
    writeln(q"<Encore une chaine qui 
s'étend sur plusieurs lignes
>");

    writeln(q"(Enfin dernière chaine qui 
s'étend sur plusieurs lignes)");
             
}
```

La syntaxe `q"` dite "heredoc" permet de définir son propre délimiteur de chaine.

Vous pouvez utilisez les caractères ouvrant/fermant : `(…)`  `<…>` ...