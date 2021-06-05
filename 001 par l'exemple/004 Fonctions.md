# Fonctions

```D
void main()
{
    import std.stdio : writeln;

    int add(int x, int y)
    {
        int sum = x + y;
        return sum;
    }

    writeln(add(4, 5));
}
```

La déclaration **import** est ici interne à la fonction main et importe uniquement la fonction **writeln()**

On déclare une fonction prenant deux paramétres de type entier et retournant un entier. 