# Clean Code



## chapitre 6 « Objects and data structures »

- Dans ce chapitre, on parle d'objet, ça rappel les `struc` en C.
- Objet vs Structure; méthode exposé vs attributs exposé ?
- La malediction de l'expert; discours critique sur le procédural, l'objet apporte des solutions à ces problèmes...
- Le livre à été écrit dans un contexte, ce contexte est visible dans ce chapitre.
- La structure est un premier saut d'abstraction (vis à vis des variables simple).
- Loi de Demeter « La méthode ne doit pas invoquer les méthodes sur les objets qui sont retournés par les fonctions autorisées. Autrement dit, il ne faut pas parler aux inconnus, uniquement aux amis. ».
- [Les principes SOLID dans la vie de tout les jours](http://www.arolla.fr/blog/2017/02/principes-solid-vie-de-jours/) (ils ont ajouté la loi de Demeter dedans).


## Chapitre 7 «Exceptions »

- L'auteur évoque le fait que c'est mieux d'utiliser des exceptions plutôt que des code de retour.
- Difficile à aborder (encore) si on a pas déjà un peu de d'historique (pourquoi gérer les erreurs ?).
- Est-ce que ce livre s'adresse à des débutant ?
- Qu'est que c'est une exception ? C'est quoi les `try`/`catch` ?
- Lien avec l'électronique (par rapport aux codes retour) ?
- Une compétence à développer : **apprendre à comprendre les messages d'erreurs**.
- [Rust](https://www.rust-lang.org/fr-FR/) à une gestion d'erreur remarquable il parait.


## chapitre 8 « Boundaries »

* C'est important de laisser les limites d'un système propre.
* Est-ce que les « boundaries » (limites), ne sont pas en fait ce qu'on appel API également ?
* Contraindre la zone où on utilise un élément extérieur pour limiter l'impact d'un changement subit.
* On peut travailler sur un truc qui n'existe pas encore en le simulant, dans un objet tampon.
* Il y a une ambiguité sur le terme « generics »
* C'est mieux de bien typer les éléments qui sont utilisé dans les interfaces
* On peut écrire des tests pour vérifier et apprendre à utliser une librairie externe, une api.
* Pas beaucoup de code example sur ce chapitre, c'est dommage.
* Il faudrait faire un clean code pour les langages dynamiques


On parle d'un stop ou encore... 
Parce que ce livre est un peu vieux, il évoque des éléments de contexte difficilement accessible pour des personnes arrivé plus recement à la programmation.
Parce que certains article comme [Forget about Clean Code, let’s embrace Compassionate Code](http://johannesbrodwall.com/2018/06/24/forget-about-clean-code-lets-embrace-compassionate-code/) et [Developers Should Abandon Agile](https://ronjeffries.com/articles/018-01ff/abandon-1/) font un peu réfléchir autour de ce genre de contenu.

Ce livre reste intéressant, mais il faut faire attention de ne pas le brandir en étendard.
On a décidé de continuer, en gardant une regard critique.


## chapitre 9 « Tests »

* Très important d’écrire des tests propres. Exemple d’une entreprise où le fait d’écrire les tests de façon pas maintenable a coulé le projet
* Des tests propres, c’est des codes lisibles.
* Marine : « Dans un test, il vaut mieux privilégier la lisibilité à la réduction de duplication » cf 99 bottles.
* Un test doit être construit selon la structure ‘Given, when, then’, équivalent à ‘acteur, action, assertion’
* Un test doit tester une seule chose. En tout cas un seul concept
* Un test doit renvoyer un booléen
* Un test doit utiliser assert_equal plutot que assert true ou false, pour la lisibilité
* Il évoque la possibilité de refactorer la partie assertion dans une fonction à part. Possibilité de refactorer en conservant la lisibilité.
* Elodie : « Le refactoring peut-il exister en dehors de la pratique du TDD ? »

Les 3 lois du TDD :
* commencer par écrire un test d’échec
* le test  écrit doit être le plus petit possible
* écrire uniquement le code de production suffisant pour faire passer le test

F.I.R.S.T
* Fast : les tests doivent être rapides
* Independant : les tests doivent pouvoir être lancés dans n’importe quel ordre, ne pas dépendre les uns des autres
* Repeatable :  les tests doivent pouvoir être lancés dans n’importe quel environnement
* Self-validating : les tests doivent renvoyés un booléen
* Timely : écrire le test en premier, juste avant d’écrire le code de production

Une deuxième lecture nous permet de dire :

- C'est important de garder le code de test lisible.
- Pour garder une bonne lisibilité des tests, il ne faut pas hésiter à créer des fonctions spécifiques dans les tests pour simplifier.
- La complexité des tests peut devenir un signal que quelque chose pourrait être amélioré.
- Il faut essayer de tester les concepts, un par test, plutôt que de tester l'implémentation. C'est peut-être avec l'expérience qu'on y arrive...


## chapitre 10 « Classes »

* On parle surtout de SRP(Single Responsability Principle)
* Une classe doit rester petite
* Garder une cohésion dans une classe amène à en créer beaucoup de plus petite
* La cohésion peut être divers selon le contexte


## Chapitre 11 « System »

@will.i.am, @camille, @Yannick, @PetitPandaRoux parle du chapitre 11 « System » du livre clean code.

- On y parle d'architecture et de systèmes complexes, et de comment on les organisent.
- C'est une bonne idée de séparer la construction d'un objet de son utilisation.
- C'est une notion a explorer; est-ce que c'est un chapitre un peu popre à Java ?
- Le chapitre parle ensuite d'injection de dépendance.
- Concept un peu flou et/ou compliqué ?
- Est-ce que les exemples en Java sont perturbant ?
- On parle de scaling, de `cross-cuting concerns`, de Aspect Oriented Progamming, ... on comprend pas tout.
- Il y a un rappel sur le fait que c'est plus important d'avoir **une application qui fonctionne** que de mettre en place un design patterm.
- Repousser les decisions de design le plus tard possible, et garder un design le plus simple possible pour pouvoir le modifier facilement. On parle aussi de garder les options ouvertes le plus longtemps possible.
- Ici on parle de design de code, pas de la partie visible.
- C'est une bonne chose d'utiliser un langage métier pour être compréhensible.
- Fabriquer un DSL semble un truc vraiment bien, mais c'est pas facile à envisager.
- Chapitre un peu trop gros ?

Les DSL :

![](/uploads/default/original/1X/b681d9159073f58e5b2417973699b4847ad81c6b.gif)


## chapitre 12 "Emergence"

Le chapitre décrit quatres règles pour garder le code simple. L'idée n'est pas de tout designer dès le début, mais qu'en respectant les principes, cela émergera au fur et à mesure.
Dans l'ordre d'importance, les règles du système:
- elle réussit tout les tests.
- elle ne contient aucune redondance.
- elle exprime les intentions du programmeur.
- elle réduit le nombre de classe et de méthodes.

Dans la phase de refactoring, il est important de prendre du recul par rapport à son code. Pratique qui n'est pas forcément enseigné pendant les études et qui n'est pas forcément courante chez les développeurs.
Il existe un juste milieu entre la réflexion sur le design et la mise en action. Le danger avec la réflexion peut-être une fuite vers un design du grand tout chronophage.

Il ne faut pas écrire du code pour soit, mais surtout pour les autres. D'autant plus que les autre sera probablement le programmeur dans le futur. Il ne faut donc pas égoïste lors de l'écriture.
Le coût d'un projet étant principalement de la maintenance, réduire la complexité et améliorer l'intelligibilité du code diminue ce code à long terme.
cf. [egoless programming](https://blog.codinghorror.com/the-ten-commandments-of-egoless-programming/)


## chapite 13 « Concurrency »

- Encore un chapitre qui est difficile sans expérience. Comment aborder ce genre de notions sans les manipuler
- Pourquoi résoudre des problèmes qu'on a pas rencontré ?
- Le multithreading semble un truc intéressant, mais il faut avoir des connaissances bas niveau apparement (comprendre le processeur) ?

## chapite 14 « Successive refinement »

Beaucoup de code dans ce chapitre, pas mal survolé pour la plupart des participants.

Il s'agit d'assister aux étapes de refactoring d'une bibliothèque et la réflexion associé.

- Titre surprenant au regard du contenu.
- "timeline vers un code le plus propre possible" -> idée de brouillon puis de code "raffiné"
- comparaison de l'enseignement du code et l'enseignement de math vs l'enseignement de l'écriture pertinente
- le sujet n'aborde pas la manière de juger d'un raffinement "good-enough" - quand, alors, arrêter de raffiner ?
- baby-steps & TDD, c'est conseillé aussi pour les refactos

Finalement, l'objectif du code propre, "keep it simple" est d'avoir un refactoring le moins couteux possible et ainsi, de garantir l'évolutivité du programme.

refactoring lisibilité vs. refactoring perfomance. Ces notions sont-elles exclusives ?

"[Make It Work Make It Right Make It Fast](http://c2.com/cgi/fullSearch?search=MakeItWorkMakeItRightMakeItFast)" -- Kent Beck


##  chapite 17 « Smells and Heuristics »

- Chapitre long, c'est une suite de règles.
- Clean Code en un chapitre avec une suite de règle.
- Rangé par catégorie, mais il y a une grosse catégorie général.
- C'est une grille de lecture pour développer un esprit critique sur son code.
- On parle un peu de la règle g5 autour de la duplication.
- On peut savoir détecter une mauvaise odeur dans le code (smells), mais comment le résoudre ?
- Pour apprendre à coder proprement, il faut coder à plusieurs, histoire de pouvoir débattre des idées.
- Certaines de ces règles sont difficilement abordable sur un kata, la base de code est trop petite. C'est important d'alterner avec un projet libre.


## Clean Code appliqué à

[Clean code appliqué au JavaScript](https://github.com/ryanmcdermott/clean-code-javascript)


[Clean Code en Ruby](https://github.com/uohzxela/clean-code-ruby)
C'est une synthèse des notions de Clean Code avec des exemples de bonnes et de mauvaises pratiques en Ruby.

