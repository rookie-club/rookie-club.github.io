---
layout: default
title: Session du 18 décembre 2020
---

Nous avons repris le kata bowling en JavaScript de la dernière fois

## Personnes présentent

- Élodie
- Yannick

## Le code

```javascript=
var assert = require("assert");
const bowling = require("../bowling");

describe("test function bowling", function(){
    it("Should return empty party.", function(){
        const scorePartyBowling = [[0, 0], [0, 0]];
        assert.strictEqual(bowling(scorePartyBowling), 0);
    })
    it("Should return simply addtion", function(){
        const scorePartyBowling = [[1, 2], [0, 0]];
        assert.strictEqual(bowling(scorePartyBowling), 3);
    })
    it("Should return a simply spare", function(){
        const scorePartyBowling = [[8, 2], [1, 0]];
        assert.strictEqual(bowling(scorePartyBowling), 12);
    })
    it("Should return a simply addtion without sapre", function(){
        const scorePartyBowling = [[0, 8], [2, 1]];
        assert.strictEqual(bowling(scorePartyBowling), 11);
    })
    it("Should return strike", function(){
        const scorePartyBowling = [[10], [2, 1]];
        assert.strictEqual(bowling(scorePartyBowling), 16);
    })
    it("Should count skrike", function(){
        const scorePartyBowling = [[1, 3], [10], [2, 1]];
        assert.strictEqual(bowling(scorePartyBowling), (1 + 3) + (10 + 2 + 1) + ( 2 + 1 ));
    })
    it("10 quiles tombé au deuxième lancé compte pour un spare", function(){
        const scorePartyBowling = [[0, 10], [2, 1]];
        assert.strictEqual(bowling(scorePartyBowling), (0 + 10 + 2) + ( 2 + 1 ));
    }) 
});
```

```javascript
function bowling(scores){
    let result = 0;

    for(let i = 0; i < scores.length; i++){
        let frame = scores[i];
        let previous_frame = scores[i - 1];
        let premier_lance = frame[0];
        let deuxième_lance = frame[1];

        result += premier_lance;
        if (deuxième_lance) {
            result += deuxième_lance;
        }
        
        if(i > 0)
            result += calculBonus(previous_frame, frame);
    }
    return result;
}


function calculBonus(previous_frame, frame){
    if (previous_frame[0] == 10) {
        return frame[0] + frame[1];
    }
    if (previous_frame[0] + previous_frame[1] == 10) {
        return frame[0];
    }
    return 0;
}

module.exports = bowling;
```

## Ce que nous appris

> Nous essayons un format cuisine à code. Une pause de débrief tout les deux commits.
> -- Yannick

### Debrief de 1er round

Pas facile de regarder une autre personne coder, sans parler et sans interenir sur le code. J'avais envie d'explorer _ma_ piste, celle que j'avais en tête.

Sur le premier commit, je suis heureuse de l'avoir refait parce que j'avais compris.

Sur le deuxième mouvement, j'ai refait de mémoire, c'est pas confortable. Je n'ai pas compris pourquoi nous avons ajouté un `if` autour du `result += frame[1]`.

> Sur le deuxième commit, nous avons fait 3 mouvements, c'est sans doute un peu trop. Deux sont lié au TDD, nous avions posé deux faux bout de code. L'autre est lié à une nouvelle situation.
> -- Yannick

### Debrief de 2eme round

En reprennant nous avons refait l'exploration du mouvement autour de
```javascript
if (frame[1]) {
    result += frame[1];
}
```
Là j'ai compris pourquoi nous avons fait ça.

J'avais oublié le format de donnée d'entrée. Je pense que si nous avions autre chose qu'un strike d'entrée, nous n'aurions pas eu le problème à résoudre (poser le `if`).

Pas facile de faire le bowling quand on traite les lancer les uns après les autres plutôt que tout le tableau.

### Debrief de 3eme round

Je constate que ma première intuition n'était pas la bonne.

Je ne me sent pas encore à l'aise à manipuler des tableaux de tableau. Ce qui ne fonctionnait pas, c'était que, dans le cas d'un strike, il n'y a pas de deuxième lancé.

> Nous avons extrait deux variables pour rendre explicite les deux lancés d'une frame.
> Pas d'autre remaniement. Par contre nous avons ajouté un élément de complexité en ajoutant le test sur la présence du deuxième lancé.
> -- Yannick

## Debrief général

> Nous pouvons encore pousser le remaniement. Deux axes de travail compatible
> - l'extraction de méthode, permettant de reduire drastiquement le nombre de ligne par méthode, et d'apporter plus de clareté sur le code (avec des nom explicite à ces méthdoes)
> - la structure de données. Élodie à évoqué une diffculté à la manipuler en tableau. Ça serait un exercice intéressant.
> -- Yannick


Avant de démarrer, peur de tomber dans le copier coller avec le format cuisine à code. Mais finalement, je constate que j'arrive à re-écrire le code que j'ai compris, alors que ça va être plus dur de recopier du code de mémoire si je ne l'ai pas compris.

C'est chouette d'être aiguillé pour en pas rester bloquer, quitte à ne pas comprendre ce qu'il se passe sur le moment.

> Les debriefs régulié sont très important, surtout pour la personne sachante. Elle peut ainsi reprendre les parties non comprise.
> -- Yannick


> Petite note sur le refactoring plus à jour que le livre, le catalogue en ligne des remaniements de code https://www.refactoring.com/catalog/
> -- Yannick


Nous avons utilisé VSCode avec LiveShare pour l'exercice. Ça a plutôt bien fonctionné.

> Le soucis avec VSCodium, c'est qu'on ne peux pas s'identifié (nous n'avons pas réussi), et donc pas être en écriture sur LiveShare
> -- Yannick

