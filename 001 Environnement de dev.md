# Les compilateurs D 
Comparatif des compilateurs : https://wiki.dlang.org/Compilers


## DMD le compilateur de référence 
Sous Licence Boost, DMD est le compilateur de référence D, il est disponible sur les plateformes Windows, Linux, OS X, FreeBSD. 

DMD privilégie la vitesse de compilation. C'est un excellent choix pour débuter. 
Des packages "DMD" Chocolatey, Homebrown, MacPorts et Nix sont aussi disponibles.

https://dlang.org/download.html#dmd


## GCD le frontend pour GCC
Sous licence GPL, GCD est un frontend pour utiliser le compilateur GCC, ce portage est principalement destiné à être utilisé sous Linux. 

GCD/GCC privilégie la vitesse de l'executable généré. 

https://gdcproject.org/downloads


## LCD le frontend pour LLVM
Publié sous la 3-Clause BSD License, LDC est un frontend pour LLVM. Disponible sous Windows, Linux, Os X, FreeBSD , il propose aussi un support pour utiliser le compilateur Android natif.

LCD propose en plus des blocs assembleurs au format DMD/GCC, le support de l'assembleur LLVM (ir). 

Des packages Homebrown, Nix et GNU Guix sont aussi disponibles.

Sous Windows, LCD est disponible depuis l'installateur du plugin VisualD 

https://github.com/ldc-developers/ldc/releases

# Les IDE et Editeur de texte 

Il existe de nombreux plugins pour les IDE et les éditeurs de texte 

## VSCode 
- https://marketplace.visualstudio.com/items?itemName=webfreak.code-d

## Atom
- https://atom.io/packages/ide-dlang

## Emacs 
- https://github.com/Emacs-D-Mode-Maintainers/Emacs-D-Mode

## VI
- https://github.com/VundleVim/Vundle.vim

## Sublime Text
- https://github.com/Pure-D/sublime-d

## IntelliJ
- https://intellij-dlanguage.github.io/

## Visual Studio
- http://rainers.github.io/visuald/visuald/StartPage.html

L'installateur de VisualD est disponible avec (ou sans) les compilateurs DMD (compilateur de référence) et  LCD (pour compiler du D via LLVM).

L'installateur intégre aussi Mago, un serveur pour le debugage.

https://wiki.dlang.org/IDEs
https://wiki.dlang.org/Editors

## Dexed 

Un éditeur de code entièrement dédié au D. 
Pour Linux : https://gitlab.com/basile.b/dexed/-/tree/master

Il existe une version pour Windows, mais je n'ai pas réussi à mettre la main sur les binaires : https://ci.appveyor.com/project/BBasile/dexed/builds/38765898/artifacts




