# Lecture sur l'entrée standard

```D
import std;

void main()
{

    writeln("Quel est ton nom ?");
    string nom = readln.strip;
    writef("Salut %s", nom);

    writeln(" quel est ton age ?");
    ushort age = readln.strip.to!ushort;
    writef("%d. Super ! ", age);

    writeln("Ton chiffre préféré ?");
    uint chiffre;
	readf(" %d", &chiffre);
    writef("%d. Ok ! ", chiffre); 

}
```

La fonction **readln()** permet de récupérer une ligne sur l'entrée standard.

La chaine récupérée contient tout ce qui a été saisie, y compris les caractères de contrôles. Il convient donc de la nettoyer avant utilisation, c'est le rôle de la fonction **strip()**.

On utilise `to!` pour réaliser la conversion de la ligne reçut en un entier non signé.

La fonction **readf()** permet de formater le chaine lue. 

L'esperluette (`&`) devant le nom de la variable `chiffre` dans l'utilisation de la fonction **readf()**, indique que l'on passe l'adresse de la variable et non son contenu. 

La fonction **readf()**,  va remplacer le contenu de la variable avec la valeur qui sera lue sur l'entrée standard.




