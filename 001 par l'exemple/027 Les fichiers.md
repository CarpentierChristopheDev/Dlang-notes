# Les fichiers

Le module **std.file*** contient les fonctions pour travailler avec les fichiers et les dossiers à haut niveau.

```D
import std.conv;
import std.stdio : writeln;
import std.file;

void main()
{

    // Ecriture d'une ligne dans un fichier
    write("test.txt", "Hello Marie-Françoise Bouchérà\n");

    // Ajout de ligne dans le fichier 
    foreach (i; 2 .. 6)
    {
        append("test.txt", "Hello ligne " ~ to!string(i) ~ "\n");
    }

    // Lecture du fichier 
    string content = readText("test.txt");
    writeln(content);

    // Si le fichier existe le supprimer
    if (exists("test.txt"))
    {
        remove("test.txt");
    }

}
```

Pour travailler à plus bas niveau sur le fichier, on utilise la structure `File` définie dans le module **stdio**

```D
import std.conv;
import std.stdio;

void main()
{

    auto testFile = File();
         
    // Création d'un fichier 
    testFile.open("test.txt", "w");
    testFile.writeln("Hello");
    testFile.close();
    
    // Lecture d'une ligne fichier
    testFile.open("test.txt", "r");
    writeln("une ligne du fichier texte : \n", testFile.readln());
    testFile.close();

    // Ajout de plusieurs lignes dans une fichier 
    testFile.open("test.txt", "a");
    foreach (i; 2 .. 6)
    {
        testFile.writefln("Hello ligne %s", i);
    }
    testFile.close();

    // Travailler avec un fichier texte Ligne à Ligne
    testFile.open("test.txt", "r");
    foreach (line; testFile.byLine())
    {
        writeln(line);
    }
    testFile.close();

}
```

Cette structure comporte les fonctions pour travailler avec les handle de fichiers : 
- open : pour ouvrir un fichier. 
	- en écriture (suppression et création du fichier) mode "w"
	- en lecture mode "r"
	- en ajout de donnée dans un fichier existant, mode "a"
- close : pour ferme le fichier
- write, writeln, writef, writefln ... pour écrire dans le fichier
- read, readln : pour lire dans le fichier
- byLine :  qui retourne un tableau de chaine des lignes du fichiers.
