---
layout: default
title: Exercices
---

## HackInScience

https://hackinscience.org

En quelques mot : C'est des amis et moi qui avons pondu la chose, c'est une plateforme open source (http://framagit.org/hackinscience/), en Django, pour faire des exercices Python.

Le gros du boulot n'est *pas* la rédaction des exercices (je dis pas que ça se fait en un claquement de doigts non plus), plein de plateforme savent le faire (project euler ♥), ce qu'on a essayé d'apporter, et c'est le gros du boulot, c'est une moulinette de correction capable de dire clairement ce qui ne convient pas dans un rendu.

Donc oui c'est des tests unitaires écrits pour chaques exercices, mais en plus une phrase en "bon" anglais pour chaque test unitaire pour dire pourquoi ça ne marche pas, pour qu'un élève ne soit jamais bloqué.

Aucun projet n'était terminé ... celui ci ne l'est pas non plus, si vous trouez des exercices donc la correction est améliorable vous pouvez me le dire, ou si vous trouvez des bugs vous pouvez me les remonter sur le framagit.

Je peux aussi vous créer un compte prof, ça vous donne accès a un tableau qui montre la progression des élèves d'un groupe (en ligne les élèves, en colonne les exercices, au milieu des ✓ ou des ✗, simplement).

Pas de pubs, pas de limitations, pas de partie payante, #captainobvious

-- Julien Palard aka MDK

## Exercice de Bienvenue

@manu, @NerOcrO, @mac et @will.i.am font un exercice de bienvenue.
L'exercice consistant à obtenir exo([1,2,3,4..]) --> [1,4,3,8..]

- Il est fondamental d'apprendre à lire un message d'erreur.
- Reproduire l'erreur lorsqu'on a un message d'erreur permet de vérifier la compréhension de l'erreur. A un niveau plus global, reproduire une erreur permet d'identifier l'origine.
- `import librairie.fonction` vs. `from librairie import fonction`

- A compléter:
-- typages des variables (`NoneType` par exemple)

_est-ce que c'est en fait un morceau de journal du 14 décembre 2018 à 15h18 ?_

## Kata FizzBuzz

http://wiki.c2.com/?FizzBuzzTest

### Le 14 septembre 2018 à 13h09

@jibe-b, @NerOcrO, @camille, @PetitPandaRoux, @Yannick et @will.i.am font une session du kata fizzbuzz en python

- on s'est essayé aux [fonctions calisthenics](https://codurance.com/2017/10/12/functional-calisthenics/)
- on a voulu faire le kata sans `if` sans succès, mais la solution se trouve [ici](http://sametmax.com/fizzbuzz-en-python/)
- On a étudié les types de conteneurs en faisant la différence entre une liste et un array. Un array est typé alors que la liste est non typée.
- la formulation du nom du test est importante et doit révéler l'intention du test, mais pas l'implémentation attendue.
- On a découvert les katas avec contraintes.
- Découverte pour certains de l'operateur ternaire de la forme `a if condition else b`

### Le 19 octobre 2018 à 16h32

Session avec @jibe-b, @will.i.am, @NerOcrO et @Yannick

On utilise le kata fizzbuzz pour explorer Rust

- On reparle de la fiche de langage;
  - Rust est de paradigme impératif, fonctionnel et concurrent,
  - de typage statique fort, compilé (avec rustc) dans un binaire executable,
  - la [doc officielle](https://www.rust-lang.org/en-US/documentation.html) fait bien le boulot et il y a un mécanisme intéressant pour les messages d'erreurs avec `rustc --explain <CODE>`,
  - pour la gestion de lib externe, il y a l'outil [cargo](https://doc.rust-lang.org/stable/cargo/)
  - Rust est créé par Mozilla, dans un soucis de gestion plus efficace de la mémoire, il y a peut-être beaucoup de chose.
- La gestion des chaines de caractères est un peut surprenante pour quelqu'un qui viens d'un langage typé dynamiquement
- L'utilisation de module externe ne semble pas triviale
- typage i32 au lieu de int

### Le 26 octobre 2018 18h52

@NerOcrO, @camille, @Yannick, @PetitPandaRoux et @will.i.am explorent la mise en place d'un docker pour les tests.

- Avec haskell pour utiliser stack, il faut lancer `stack run`
- Si l'image n'est pas disponible publiquement il faut builder localement avant de pouvoir executer `run`
- @PetitPandaRoux n'est toujours pas convaincu par rapport de Docker vs Vagrant
- il est facile de lancer un conteneur Docker, pratique pour servir beaucoup de requêtes
- Il y a un ordre dans le Dockerfile pour la gestion du cache
- Il y a peut-être un intérêt limité à Docker en développant seul, mais peut avoir un intérêt pour le travail en équipe
- un autre intérêt est l'aspect documentation exécutable, ce qui évite la documentation obsolète

### Le 1er décembre 2018 à 21h43

Vi Hart recommande également FizzBuzz… mais 50 fois :

http://vihart.com/fifty-fizzbuzzes/

Et un notebook où exécuter ces FizzBuzz :

https://mybinder.org/v2/gh/quasiben/fiftyfizzbuzzes/master?filepath=Fifty%20Fizzbuzzes.ipynb

## Kata balancedParentheses

Le 31 août 2018 à 18h

@camille, @PetitPandaRoux et @will.i.am font un kata balancedParentheses

- On a mis en place un environnement virtuel  `python3.6 -m venv dossier`
- on a ajouté les requirements `pip freeze > requirements.txt`
- on a lancé l'environnement `source bin/activate`
- on a utilisé la librairie externe `pytest`
- on a utilisé `String.count(pattern)`
- @Yannick a appris qu'il n'y avait que `assert` dans [`pytest`](https://docs.pytest.org/en/latest/)
- on a vu qu'on est plus rapide à définir les tests de démarrage
- on a vu qu'il est toujours plus facile de faire des katas en groupe

## Refactoring jeu de la vie quadricolore

Le 24 août 2018 à 18h

@NerOcrO, @PetitPandaRoux et @will.i.am remanient un (meilleur) jeu de la vie

- tentative de création et application d'un patch `git diff` et `git apply`
 -- mais problème avec des dossiers qui sont renommés
- push sur un autre repository `git push [nouvelle adresse remote]`
- worlkflow d'une contribution à un projet :
--création d'un fork
--modification et `git commit`
--`git push`
--création d'une pull request sur github
--validation (éventuelle) de la pull request

## Projet Euler

Le 2 novembre 2018 à 13h12

@shirley, @jibe-b, @NerOcrO, @Yannick, @Syla

On fait la première exercise sur Project Euler en Go - https://projecteuler.net/problem=1

https://github.com/Rookie-Club/EulerProject/commit/2bc26d7d611193fece6e3526401387ad135eed2b

What we learned
- @NerOcrO, @Syla, and @jibe-b discover go
- Understand what is written before writing
- Parameters not required for main function in C
- TDD: Pass the tests as quickly and with as little code as possible


## Kata RegExp Parser

Kata pour apprendre à faire un moteur de regexp

L'idée d'une expression régulière est de retrouver un motif dans une chaîne de caractères

Pour commencer, nous pourrions avoir une fonction qui renvoie vrai ou faux selon si le motif recherché existe dans la chaine ou pas.

Les tests pourrait être :

```python
mafonction("une chaine de caractères totalement banale", "z")
# => False
mafonction("une chaine de caractères totalement banale", "[0-9]")
# => False
mafonction("une chaine de caractères totalement banale", "banale")
# => True
mafonction("une chaine de caractères totalement banale", "[a-zA-Z]")
# => True
```

https://github.com/Rookie-Club/katas/releases/tag/20180928-regexp-python

@will.i.am, @PetitPandaRoux, @NerOcrO, @Yannick et @camille créent et explorent en même temps un kata regexpparser

- @PetitPandaRoux : "c'est puissant python"
- on a vu la compréhension de liste
- @camille commence à comprendre ce qu'est une expression régulière
- le premier test en tdd peut souvent être un cas limite vide de l'API
- mais est ce que finalement ce n'est pas mieux un cas simple plutôt qu'un cas limite ? (dans notre cas chercher 'a' dans 'a' plutôt que '' dans '')
- regexr.com pour tester les regex

Le 28 septembre 2018 à 18h


## Kata Poker

http://codingdojo.org/kata/PokerHands/

[code](https://github.com/rookie-club/katas/tree/poker/java)

@will.i.am
@camille
@carole.g
@PetitPandaRoux
@Yannick
Kévin
@jibe-b
@NerOcrO
@tho

- concept dans les tests - faut-il tester toutes les combinaisons ?
- [happy path](https://en.wikipedia.org/wiki/Happy_path) vs sad path
- [top-bottom vs. bottom-up](https://en.wikipedia.org/wiki/Top-down_and_bottom-up_design)
- ide [intellij](https://www.jetbrains.com/idea/)
- Sémantique dans les tests
- "C'est bien de faire du Java quand même." @PetitPandaRoux
- @Yannick est content de refaire un langage typé statiquement
- Stack Java volumineuse

Le 21 septembre 2018 à 13h

## Kata Gilded Roses

[Kata Gilded Roses](https://github.com/codingdojo-org/codingdojo.org/blob/master/content/kata/GildedRose.md)


### Le 21 septembre 2018 à 18h

@Yannick, @jibe-b, @josetoujours, @camille, @carole.g, @NerOcrO font une session.

[code source](https://github.com/Rookie-Club/katas/releases/tag/20180921-kata-gildedroses-js-to-functionnal)

- La définition du paradigme fonctionnel n'est pas forcement très claire. On sait que :
  - les variables sont immuables (ou pas ?)
  - Un seul `if` par fonction, et il doit avoir un else
- Des livres pour apprendre le fonctionnel [Learn Haskell](http://learnyouahaskell.com/) et [Structure and Interpretation of Computer Programs](https://mitpress.mit.edu/sites/default/files/sicp/index.html), il y a aussi [JavaScript allongé](https://leanpub.com/javascriptallongesix)
- C'est sécurisant de commiter à certaines étapes.
- « j'ai pu participer à un remaniement de code pas écrit par nous » -- @jibe-b
- On a pas essayé de comprendre le code, on a juste lu la doc et la fixture proposé pour écrire les tests.
 - On c'est intéressé à ce que le code doit faire, doit rendre comme service.

### Le 16 novembre 2018 à 13h

Un kata de refactoring en python avec @Yuhiba @NerOcrO et @jibe-b

- Brew est en carafe depuis la dernière version de macOS (Mojave)
- difficultéS à installer pytest
- configuration de vim pour @jibe-b
- mybinder.org pour lancer un environnement python (ou autre si configuration) avec Docker and Jupyter lab (notebooks) (demander à @jibe-b )


## Kata Game of life javascript

### Le 10 août 2018 à 17h

@PetitPandaRoux @NerOcrO @will.i.am @camille et @bobby font le kata game of life en nodejs

* @PetitPandaRoux dit qu'il devrait écrire plus souvent en ES6 pour prendre l'habitude
* C'est bien de connaître l'historique des langages
* Révision de `JSON.stringify(tableau)` pour comparer des tableaux
* Révision de `module.exports = { truc, bidule }`
* A revoir : les opérations logiques
* Fabien fait du tdd pour la première fois
* On a exploré la piste de faire un tableau d'objets plutôt que de gérer une grille
* On a revu le principe de l'extract method
* On a fait le choix d'écrire tout en français

Le code source de la session sur https://github.com/Rookie-Club/katas/releases/tag/20180810-kata-game-of-life-nodejs

Je l'ai fini c'est trop beau ! Je suis trop content(et pas peu fier) ! Je l'ai mis sur un site ou je montre normalement les productions des adolescents. (Désolé, le graphisme a été fait par mon ancien stagiaire de 3ème :) ).

J'ai programmé avec mes pieds il y a plein de refacto a faire et de l'optmisation.
J'ai fait quelques test en plus mais pas grand chose, avec ce qu'on a fait c'était quasiment l'essentiel.

http://www.mo-lab.fr/experience.html

Le repos du fichier :
https://github.com/PetitPandaRoux/game-of-life

J'ai préféré ne pas le mettre dans le dossier kata mais j'ai mis un lien dans le readme qui point dessus.

Voici ma version https://github.com/NerOcrO/game-of-life (@NeroCro)
