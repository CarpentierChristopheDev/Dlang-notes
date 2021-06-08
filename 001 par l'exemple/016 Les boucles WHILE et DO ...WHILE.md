# Les boucles WHILE et DO ... WHILE

Elle permettent de répéter du code tant qu'un prédicat est vrai.

```D
import std;

void main()
{
    // Boucle 9 -> 0 
    int n = 9;
    while (n >= 0)
    {
        writeln(n);
        n--;
    }

    writeln(n); // ici n = -1 

    // Boucle 0 -> 9
    do
    {
        n++;
        writeln(n);
    }
    while (n < 9);
}
```

Dans le cas de la boucle `do ... while` sera executer avant de vérifier le prédicat. Le code sera donc toujours executer au moins une fois. 

