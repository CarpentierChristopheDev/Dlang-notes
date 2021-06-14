# les unions

L' union peut accueillir une valeur de n’importe lequel de ses membres, mais un seul à la fois.

Elle prends en mémoire moins de place qu'une structure équivalente, qui elle réserve la mémoire pour tous les champs déclarés, même si vous ne les utilisez pas.

```D

import std;

void main()
{

    struct NomStructuré
    {
        string prenom;
        string nom;
    }

    union Nom
    {
        NomStructuré nomClient;
        string raisonSociale;
    }

    // Le client est une personne 
    Nom monClient;
    monClient.nomClient = NomStructuré("Marie", "Berine");
    writeln(monClient.nomClient.prenom, " ", monClient.nomClient.nom);

    // Le client est une entreprise 
    monClient.raisonSociale = "Entreprise SixTaudisReconstruits";
    writeln(monClient.raisonSociale);

}

```

**monClient** peut être une personne ou une entreprise, mais pas les deux à la fois.
