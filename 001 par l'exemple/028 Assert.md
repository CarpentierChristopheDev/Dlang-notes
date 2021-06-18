# assert

assert permet de vérifier une hypothèse de travail.

```D
import std;

void main()
{
    int x = 3;
    int y = 4;

    int z = x + y;

    // Hypothése : a ce stade du traitement, z vaut 10
    assert(z == 10);

    writeln(z);
}
```

Lorsque l ' assertion `z == 10` est fausse, le traitement s'arrête : 

```Error
core.exception.AssertError@onlineapp.d(11): Assertion failure
----------------
??:? \_d\_assertp \[0x555e907ecb59\]
onlineapp.d:11 \_Dmain \[0x555e907eb2e7\]
```
