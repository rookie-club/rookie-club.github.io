# Session du 15 décembre 2020

Nous avons fait un kata bowling en JavaScript

## Personnes présentent

- Élodie
- Yannick

## Le code

```javascript=
function bowling(scores){
    let result = 0;

    for(let i = 0; i < scores.length; i++){
        let frame = scores[i];
        result += frame[0];
        result += frame[1];
        if (i > 0){
            let previous_frame = scores[i - 1];
            if(previous_frame[0] + previous_frame[1] == 10){
                result +=  frame[0];
            }
        }
    }
    return result;
}
```

Les tests de la soirées
```javascript
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
    it("Should return a simply spare", function(){
        const scorePartyBowling = [[0, 8], [2, 1]];
        assert.strictEqual(bowling(scorePartyBowling), 11);
    })
});
```


## Ce que nous appris



Je visite totale de bowling car ma demande été comment sortir des methodes avec les conditions existantes.

> Le code est l'expression du métier compris par la personne qui développe.
> -- Yannick


J'ai constatée que je n'avais pas _le métier_ en tête. Je code d'une manière technique et non fonctionnelle. Et pourtant, j'ais les termes métiers : Fame , Spare, Srike.

En cherchant à exprimer le métier, le mon code à une tête totalement différente.

> Ça semble plus facile d'écrire du code à partir d'une bonne compréhension du métier, que d'écrire du code sans forcement réfléchir au métier.
> -- Yannick

Je souhaite garder cette matière première pour pouvoir m'exercer à faire des extractions de méthtodes.  




