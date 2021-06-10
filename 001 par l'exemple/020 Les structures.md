# Les structures 

Elle permettent de créer ses propres types. 

```D
import std;

void main()
{
    struct Pirate
    {
        string nom;
        string role;
        int age;
    }

    Pirate cptRackam = Pirate ("Rackam le rouge", "Capitaine", 56);
    Pirate sdMorty = Pirate ("Mortimer", "Second", 43);
    Pirate cnTiti = Pirate ("Titi la teingne", "Canonier", 30);
    
    // Affichage
    writeln(cptRackam);
    
    // Lecture des membres
    writefln("PIRATE => Nom: %s, ROLE : %s, AGE : %d", sdMorty.nom, sdMorty.role, sdMorty.age);
    
    // Modification
    cnTiti.Canonier = "Timonier"
    writeln(cnTiti);
    
}
```

Pas default, la structure est crée dans la pile.

On accède aux  données de la structure à travers leurs membres. `sdMorty.nom` permet d'accèder au membre **nom** de la variable  **sdMorty** de type **Pirate**.