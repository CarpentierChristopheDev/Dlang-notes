# Historique 

Le but de la programmation est de produire des logiciels de qualité. Cette qualité se travaille sur plusieurs axes : exactitude, robustesse, efficiance, maintenabilité, évolutivité, réutilisabilité ... 

La programmation procédurale, qui définit les structures de données et les procédures qui travaillent sur ces structures, ont permis d'apporter aux programmes la robustesse et l'efficiance escomptées. Dans la pratique, l'adaptation et l'évolutivité conduisent à remettre en cause  les structures de données au détriment de la maintenabilité et la réutilisabilité. 

C'est là qu'intervient la notion d'objets. L'objet encapsule les données et les fonctions qui travaillent sur ces données, on parle alors de méthodes. Les utilisateurs de l'objet ne sont alors plus dépendants des modifications de la structure ,cela améliore considérablement la robustesse et la maintenabilité. 

Les autres grands principes de la programmation orientée objets, comme l'héritage et le polymorphisme apportent l'évolutivité et la réutilisabilité. L'héritage permet de créer une classe à partir d'une classe existante pour la spécialiser. Le polymorphisme permet de traiter de la même manière des ensembles de classes différentes pour peu qu'elles dérivent d'une classe commune.

Si les langages objets émergents dans les années 60 : Simula, SmallTalk, Lisp c'est dans les années 1980 que l'on voit apparaitre C++, Objective-C, Common Lisp object System, Eiffel et bien d'autres qui ouvrent la voie à la Programmation Orientée Objet (POO) dans les différents secteurs du développement logiciel des années 90 (Java, JavaScript, Python, Ruby...)

Frustré de ne pas trouver, dans les années 80, un langage évolué capable de produire du code performant indépendant de l'architecture de la machine, Bjarne Stroustrup,   employé au centre de recherche Bell, après l'obtention de son doctorat sur les systèmes distribués, décide de créer un nouveau langage pour poursuivre ses recherches dans le développement de logiciels systèmes efficaces.

En rejoingnant les laboratoires de recherche Bell, Bjarne Stroustrup a l'opportunité de côtoyer directement Dennis Ritchie, Brian Kernighan, les inventeurs du C, Bob Morris, Steve Johnson, Doug McIlroy et d’autres contributeurs majeurs des systèmes Unix.

Au vu des ses besoins de portabilité et de programmation à bas niveau, Bjarne Stroustrup décide de créer son langage en adjoignant au langage C les spécificités de la P.O.O qui arrivent alors des pays du Nord avec la mouture de Simula67 du Norwegian Computing Centre d'Oslo.

# Et le D dans tout ça  ?

Walter Bright est l'auteur de plusieurs compilateurs pour Ecmascripts, Java (Visual Cafe), et du premier compilateur pour C++ qui ne passe pas par la création de code C intermédiaire (Symantec C++ qui deviendra Digital Mars C++ du nom de la petite société de Bright) 

Dans les années 2000, Walter Bright créent le langage D, un langage compilé se basant sur C++ ayant l'expressivité et les caractèristiques des langages modernes interprétés. 

Dans les années 2007, il est rejoint par Andrei Alexandrescu, considéré comme l'un des plus grands spécialistes du langage C++, on lui doit principalement les bibliothéques Loki et Mojo en c++ et de nombreux ouvrages dont "c++ modern design" et "the D Programming Language"

Ensemble, ils implémentent la version 2 du langage D. Qui a très peu bougé depuis. 

Le langage D posséde, à l'instar de C++, les classes, les closures, les fonctions anonymes, la compilation de fonction à l'execution, les intervalles, les itérateurs, l'inférence de types, la généricité, ... 

Des langages interprétés, il propose la programmation par contrat, des tests unitaires intégrés, un garbage collector, des tableaux dynamiques et associatifs, l'évaluation paresseuse, l'héritage simple, les interfaces, les mixins,  ... 

... et biens d'autres fonctionnalités : https://dlang.org/comparison.html

D se veut être un trait d'union entre la programmation système en facilitant l'interfaçage avec l'éco-systeme C/C++,  voire même à très bas niveau (directement la programmation Assembleur) et la programmation de haut niveau. En fait, la plupart des langages sont techniquement utilisables depuis D : Python, Lua, Objective-C, Fortran ... 

Outre la programmation structurée et la POO, D permet la programmation fonctionnelle,  le scripting, la métaprogrammation, la programmation par contrats et concurrente à travers le modèle d'acteurs.

D est donc un excellent langage pour commencer à apprendre la programmation, tant il permet d'en explorer toutes les facettes tout en conservant une grande lisibilité. Il vous apportera toutes les clés nécessaires pour évoluer vers les langages de votre choix. Essayer D en ligne : https://run.dlang.io/

En tant que programmeur averti, D vous permettra de créer des executables rapides, et vous apportera un environnement de production open source complet : Un langage  productif, à la syntaxe C accessible, complet et moderne, mais aussi les outils de packaging, de documentations, de tests, des plugins pour les IDE ... pour développer dans de nombreux domaines : https://dlang.org/areas-of-d-usage.html

Le compilateur de référence de D est DMD, mais il existe également les versions GDC et LDC qui utilisent respectivement les backends GCC et LLVM. DMD favorise la vitesse de compilation, GDC et LDC optimisent principalement la vitesse du code produit. De nombreuses plateformes sont disponibles : https://dlang.org/download.html

La communauté est petite, voir confidentielle, surtout de ce côté de l'atlantique, il est donc peu probable de trouver un emploi recherchant un programmeur D. Du moins, je n'ai encore jamais vu d'annonce citant le langage D ;) - Par contre la communauté  est active et vous trouverez des ressources pour vous aider à progresser en D. A commencer par le livre de Ali Çehreli "Programming in D" : https://ddili.org/ders/d.en/index.html

Un des atouts majeurs du D, c'est que le code est facile à comprendre par toute personne familiarisée avec les langages de programmation de type C. Cela permet d'engager des personnes sur le projet quelque soient leurs horizons et cela est essentiel pour assurer la maintenabilité du logiciel.



















