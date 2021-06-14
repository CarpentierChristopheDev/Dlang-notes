# Constructeur de structure

Chaque structure à un constructeur par défault, cela permet de déclarer et d'initialiser la variable. `Point p2 = Point(13,14);`

```D
import std;

void main()
{
    
	struct Point
    {
        int x = 10;
        int y = 10;
    }

    // Initialisation avec les valeurs par défault
  	Point p1;
    writeln("P1 => ", p1);
        
    // Initialisation avec le constructeur par défaut
    Point p2 = Point(13,14);
    writeln("P2 => ", p2);
    
    // Initialisation avec les valeurs nommées
    Point p3 = {x:13, y:14};
    writeln("P3 => ", p3);
    
}
```

La structure possède aussi un initialiseur par défault : `Point p3 = {x:13, y:14}`

Les membres d'une structures peuvent avoir une valeur par défault.

```D
import std;

void main()
{
   
   struct Point
    {
        int x = 10;
        int y = 10;
        this(int z) {
            this.x = z;
            this.y = z;
        }
    }

    // Initialisation avec les valeurs par défault
  	Point p1;
    writeln("P1 => ", p1);
        
    // Initialisation avec le constructeur personnalisé
    Point p4 = Point(20);
    writeln("P4 => ",p4);    
    
}
```

`this(int z)` permet de créer un constructeur personnalisé. 

`this.x` permet d'accéder au membre **x** de la structure.
