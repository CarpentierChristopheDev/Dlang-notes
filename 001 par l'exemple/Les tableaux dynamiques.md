# Les tableaux dynamiques

Les tableaux dynamiques sont crées sans définir de taille. On ajoute les éléments avec l'opérateur `~=`

```D
import std.stdio, std.algorithm;

void main()
{
    string[] travail = ["lun.", "mar."];
    travail ~= "mer.";
    travail ~= ["jeu.", "ven."];

    string[] repos;
    repos ~= ["sam.", "dim."];

    auto semaine = travail ~ repos;
    writeln(semaine);

    // Renversement 
    semaine.reverse();
    writeln(semaine);

    // Tri alphabétique
    semaine.sort();
    writeln(semaine);

    // suppression
    semaine = semaine.remove(1); // .. du second élément
    writeln(semaine);
    semaine = semaine.remove!(e => e[0] == 'm'); // .. de tous les éléments commençant par la lettre m 
    writeln(semaine);

}
```

L'opérateur `~` permet la concaténation entre deux tableaux dynamiques.

Le module **std.algorithm** contient de nombreuses fonctions, dont : 
- reverse
- sort
- remove ...

`remove!` permet d'utiliser une fonction anonyme (lambda) pour parcourir chaque élément du tableau et supprimer ceux qui correspondent au prédicat. 

