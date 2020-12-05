---
layout: default
title: Grosse revue de code sur la désectorisation
---

## Personnes présentent

- Élodie
- Yannick

## Ce que nous avons fait

_Session ayant lieu le 27 novembre 2020_

https://github.com/betagouv/rdv-solidarites.fr/pull/976

En deux temps sur la journée nous avons : 
- testé le contenue de la PR sur la feature App
- Relue le code source, par commits


## Ce que nous avons appris

Elo : j'ai pu revoir qu'il y avait deux sortes de PR dans la vie d'une application :
 - Les petites PR qui apportent un petit changement significatif pour l'utilisateur ;
 - Les grosses PR qui elles apportent un changement plus grand dans l'application. 

Je me suis aussi rappeler que les grosses PR sont souvent des "features" souhaitées par le client et parfois pas "sèche".

> La notion de sec, de prêt à être développé est un élément souvent flou, propre à chaque personne. Il convient a une équipe de le préciser. 
> -- Yannick. 


Je constate que mon niveau de code n'est pas suffisant pour _surivre_ à cette taille de revue de code (je ne peux pas faire une session de code après).

Je n'ai pas appris de chose de concrète dans le faite de s'orienté dans le code source d'un produit. (c'est pas grave.)

> C'est peut-être lié à la façon dont le code est présenté dans les outils de revue de code, github ou gitlab sont assez similaire là dessus. Le code est vue de façon linéaire : fichier après fichier. Il n'y a pas ou peu de présence de l'arborescence et la navigation d'un fichier à l'autre se faire selon l'ordre défini pas git-hub-lab.
> -- Yannick
 
Je note une certaine désoriantation de ma part vis-à-vis des tests qui sont écrit d'une manière totalement différentes à la mienne.
Ce qui m'apporte un doute quant aux test ecris : est qu'ils y en a assez ? Sont-ils bons ? Et poussent-ils la feature qu'il a développé à son maximum ?

Je ne suis pas confiante quant au testes qui sont présents, si jamais je devais travaillé sur cette feature, je faire des tests unitaires pour m'assurée que tout et j'ai bien dit tout fonctionne correctement.


Dans un deuxième temps : Ce que l'on a fait ce matin

J'aime beaucoup le fait de pouvoir tester l'application dans une review app _en semi-live_. Je trouve que cela permet de mieux comprendre comment l'application fonctionne. Ça me permet également de mettre en perspective le code et son organisation sur le résultat produit. C'est quelque chose que je n'ai pas trop eu l'occasion de faire dans mes missions précédentes.



 
