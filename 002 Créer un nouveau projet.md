# Créer le projet 

En mode console, l'utilitaire DUB permet de démarrer un nouveau projet : 

```BATCH
dub init
```

Cela génère le fichier dub.json qui décrit votre module : 

```Json
{
  "authors" : [
    "Chris"
  ],
  "copyright" : "Copyright © 2020, Chris",
  "description" : "Exemple Dlang",
  "license" : "GPLv3 or later",
  "name" : "example1",
  "targetType": "executable"
}
```

```D
import std.stdio;

void main()
{
	writeln("Edit source/app.d to start your project.");
}
```

## Lancer le projet

```BATCH
dub run
```

## Créer l'executable 

```BATCH
dub build
```

... et pour créer la version optimisée pour la production : 

```BATCH
dub build -b release
```

Les plugins pour les environnements de développement intégrent ces fonctionnalités.