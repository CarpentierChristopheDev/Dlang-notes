# Les types nullables

Par défault, un entier ou un décimal ne peut être Null, il est initialisé avec une valeur par défault : 0.

```D
import std.stdio, std.typecons;

void main()
{
    int i; // i ne peut être Null
    writeln("i = ", i);

    Nullable!int ni; // ni peut être Null
    //ni = 5;
    if (!ni.isNull)
    {
        writeln("ni = ", ni.get);
    }
    else
    {
        writeln("ni est null");
    }
}
```

Le module **std.typecons** contient les types Nullables. 

On les déclare avec la macro **Nullable!**

Une variable nullable peut être testé avec la propriété **isNull**
