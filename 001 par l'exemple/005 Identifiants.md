# Identifiants

```D
import std;

void main()
{

    void welcome(string lastname) {
    	writeln("Welcome" ~ lastname);
    }
    
    void bienvenueàvous(string prénom) {
        writeln("Bienvenue" ~ prénom);
    }
    
    void ยินดีต้อนรับ(string ชื่อจริง) {
       writeln("ยินดีต้อนรับ" ~ ชื่อจริง);
    }

    welcome("Bob");
    bienvenueàvous("Rodolphe");            
    ยินดีต้อนรับ("ආයුබෝවන්");
 
}
```

Ici, les fonctions de salutations sont déclarées dans la portée de la fonction **main()**

D supporte l'unicode dans les chaines de caractères, mais aussi dan les identifiants. Le compilateur utilise nativement des fichiers au format UTF8. 