# Glossaire

## TDD, Le développement piloté par les tests

Le « Test Driven Development » (ou développement piloté par les tests) est une pratique de création logiciel. C'est une «façon» de construire un programme qui permet de s'appuier sur des tests, et de pouvoir construire par petit bout un programme plus complexe.


[Wikipedia](https://fr.wikipedia.org/wiki/Test_driven_development)


## cUrl, c'est quoi ?

Outil de requête HTTP (et autre) dans le Terminal.

[command line tool and library for transferring data with URLs](https://curl.haxx.se/)
[Wikipedia](https://fr.wikipedia.org/wiki/CURL)


## C'est quoi un thread?

Un vidéo intéressante pour parler de ce qu'est un thread (et d'autre aspect prérequis pour l'explication).

Dans la vidéo, on parle de programme complié, mais ça fonctionne pareil avec un langage interprété. La différence, c'est que pour le langage interprété, le code source est « compilé » à la volé...

https://schneems.com/2017/10/23/wtf-is-a-thread/

## Bourne Again SHell, ou Bash, un langage interprété

* [Site officiel](https://www.gnu.org/software/bash/)
* [Exemple syntaxe learnXinYminutes](https://learnxinyminutes.com/docs/bash/)
* Paradigme: Impératif
* Typage: Dynamique
* Documentation: Voir man page intégré au terminal
* Execution: interprété, démarrage d’un OS unix, puis sh mon_programme, ou ./mon_programme s’il est executable.
* Librairie externe: Les programmes executable présent dans les repertoires listé dans la variable PATH ?

Il reste à apprendre à lire les erreurs, comprendre la documentation, et lire l’histoire du langage.

## Manpage, c'est quoi ?

Les _manpages_ sont des pages accéssible dans la console lire de la documentation sur l'usage d'une commande.

Executer `man man` pour ne savoir plus. Certain système propose une commande `help` qui propose de faire `man man` puis de regarder une commande en fonction de ce qu'on cherche à faire.

## Snippet, C'est quoi ? ça sert à quoi ?

Une (ou un ?) snippet est un bout de code que l'on va re-utiliser.

Beaucoup d'éditeur propose une gestion de snippet permettant d'insérer facilement tout un block de code (la snippet) dans le programme en court d'écriture.

Si certaines personnes par ici souhaite en partager quelques une, ou montrer comment ça fonctionne dans leur éditeur, n'hésitez pas ! :slight_smile:

Dans Visual Studio Code : File->Preferences->User Snippets et après il faut choisir le langage pour le snippet.
Il s'écrit en JSON très facilement.

https://code.visualstudio.com/docs/editor/userdefinedsnippets

## C le plus utilisé des langages

Langage de programmation très répandu, de bas niveau, que l’on retrouve à coup sur dans tout les appareils électronique, même les plus petit.

Quand tu dis “bas niveau” cela veut-il dire : “bas niveau” donc proche de la machine ou “bas niveau” facile d’accès pour un rookie ?

Je me permet de répondre pour @Yannick : "bas-niveau" signifie bien "proche de la machine". On pourrait aussi dire "langage au niveau d'abstraction bas" :thinking: . ça éviterait de faire l'amalgame facile/bas-niveau ;)

et là c'est vraiment moi :

Après est-ce que pour autant le C est difficile à apprendre pour un rookie ? Pour ma part, non, pas plus que du Javascript. Le tout c'est de savoir ce qu'on apprend et pourquoi.

Déjà, le C étant "proche de la machine", il demande un minimum de savoir sur comment fonctionne la machine et en disant ça, je pense directement à l'architecture de la mémoire (stack et heap). En effet, les transactions en mémoire étant complètement à la charge du développeur, il faut les connaîtres pour s'en servir dans le langage. C'est à peu-près le même topo pour faire du réseau ou écrire/lire dans des fichiers, etc. Mais c'est pas non plus vrai à 100% puisque certaines abstractions existent malgré tout.

L'avantage du C et pour moi, le principal intérêt de son apprentissage, c'est qu'on sait vraiment comment fonctionne plein de mécanismes sur sa machine. Et aussi, on peut potentiellement comprendre le code source de plein de projets (y compris de langage de programmation :D).

Je pense que chaque langage est accessible pour apprendre la programmation. Et pourquoi pas le C. Il y a des aspects pas forcement éviendent au premier abord (je pense aux pointeurs), mais la boucle d'execution asynchrone en JavaScript est un peu spécial aussi (pour prendre un exemple d'en langage beaucoup plus courant dans les bootcamps et autres sessions d'apprentissage rapide de la programmation).

Quand je dis bas niveau, c'est vraiment pour l'aspect proche de la machine. @tho a très bien évoqué ce que j'avais en tête :-) Merci.

## Git, C'est quoi ?

C’est un gestionnaire de version, un outil indispensable en développement logiciel. Cela permet de prendre une «photo» de l’état du code à un instant donnée.

[Git-scm.org](https://git-scm.com/)

Il y a un très bon cours gratuit sur Udacity : https://eu.udacity.com/course/how-to-use-git-and-github--ud775
C’est assez long mais très complet et vous pouvez passer ce qui ne vous intéresse pas :wink:

Github propose également pas mal de ressources (en anglais) pour apprendre Git try.github.io

Pour ceux qui préfèreraient vraiment une ressource en français il y a un cours d'openclassrooms sur git et github (format vidéo et/ou texte) :
https://openclassrooms.com/courses/2342361-gerez-votre-code-avec-git-et-github

Particulièrement recommandé si on n'est pas très à l'aise avec la programmation encore car il ne se base pas du tout sur des exemples techniques de code dans mon souvenir ! Mais il permet de bien comprendre l'intérêt du versioning, le concept de commit, branche, etc. tout en pratiquant les commandes simples (et le prof est friendly avec les newbies du terminal aussi :slight_smile: )

J’ajoute aussi le lien https://learngitbranching.js.org/ 2 qui était passé il y a quelque temps sur la mailing list (il me semble). C’est une application web conçue pour aider les débutants à bien comprendre le concepts de branche dans git.

Learngitbranching.org 2 est listé (parmi d’autres) dans try.github.io 1 :slight_smile:

