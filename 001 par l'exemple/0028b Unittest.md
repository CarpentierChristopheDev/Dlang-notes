# Unittest

les blocs `unittest { ... }` ne sont compilés et executés que si le compilateur est lancé avec l'argument **-unitest**

Ils ne sont pas générés dans la version de production (release).

Ces blocs font parties intégrante du langage, ils simplifient la vérification de tests de non régression et favorisent l'utilisation de méthode comme TDD qui consiste à écrire les tests avant de développer le code de la fonctionnalité.

```D
import std;

unittest
{
    assert(fizzBuzz(1) == "1");
    assert(fizzBuzz(2) == "2");
    assert(fizzBuzz(3) == "Fizz");
    assert(fizzBuzz(5) == "Buzz");
    assert(fizzBuzz(15) == "FizzBuzz");
}

void main()
{
    foreach(nombre;1..21) {
        writefln("%s ==> %s",nombre, fizzBuzz(nombre)); 
    }
}

string fizzBuzz(int nombre)
{
	string result = "";
    if ((nombre % 3 == 0) && (nombre % 5 == 0)) {
       result = "FizzBuzz";  
    } else if (nombre % 5 == 0) {
        result = "Buzz";
    } else if (nombre % 3 == 0) {
        result = "Fizz";
    } else {
        result = to!string(nombre);
    }
    return(result);
}
```

FizzBuzz :  Pour les nombres entre 1 et 20 :
-    si le nombre est divisible par 3 : on écrit Fizz
-    si le nombre est divisible par 5 : on écrit Buzz
-    si le nombre est divisible par 3 et par 5 : on écrit Fizzbuzz
-    sinon : on écrit le nombre
  