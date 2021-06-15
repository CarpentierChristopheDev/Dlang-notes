# L'immutabilité 

Certaines données, n'ont pas vocation a être modifiées au cours de la vie du programme. Le qualificateur **immutable** permet de verrouiller ces variables.

```D
import std;

void main()
{

    immutable int z = 3;
    writeln(z);

    z = 4; // Provoque une erreur 

    immutable string[] noms = ["Bob", "Claude", "Marc"];

    writeln(noms);
    noms ~= "Françis"; // On ne peut pas ajouter d'élément à un tableau immutable

    noms[0] = "Mary"; // On ne peut pas modifier un élément d'un tableau immutable
    writeln(noms);

}
```

La tentative de modification de variable immutable soulève une erreur. 

Les chaines litérrales sont par défault immutable, 

```D
import std;

void main()
{

    // Une chaine litéralle est immutable
    auto s1 = "hello"; // immutable(char)[5]
	s[0] = 'H'; // Soulève une erreur
    writeln(s1);

    // .dup duplique les éléments du tableau et les rends mutable
    char[5] s2 = s1.dup;
    s2[0] = 'H';
    writeln(s2);

    // .idup duplique des éléments et les rends immutable
    auto s3 = s2.idup;
    s3[0] = 'H'; // Soulève une erreur
    writeln(s3);

}
``` 

La propriété 'dup' permet de dupliquer des éléments et de les rendre mutables.

La proriété 'idup' permet de dupliquer des éléments et de les rendre immutables.