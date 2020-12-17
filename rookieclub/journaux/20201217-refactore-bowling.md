# Session du 17 décembre 2020

Nous avons repris le kata bowling en JavaScript de la dernière fois

## Personnes présentent

- Élodie
- Yannick

## Le code

```javascript=
 function bowling(scores){
    let result = 0;

    for(let i = 0; i < scores.length; i++){
        let frame = scores[i];
        let previous_frame = scores[i - 1];
        result += frame[0];
        result += frame[1];
        if(i > 0)
            result += calculBonus(previous_frame, frame);
    }
    return result;
}


function calculBonus(previous_frame, frame){
    if (previous_frame[0] + previous_frame[1] == 10) {
        return frame[0];
    }
    return 0;
}

module.exports = bowling;
```

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
    it("Should return a simply addtion without sapre", function(){
        const scorePartyBowling = [[0, 8], [2, 1]];
        assert.strictEqual(bowling(scorePartyBowling), 11);
    })
});
```

## Ce que nous appris

Je remarque que je n'ai pas beaucoup d'entrainement sur le refacotring du code. Encore plus sur les extractions de méthode. 

Yannick m'a partager le livre [Refactoring](https://refactoring.com/) et un article qui parle [Object Calisthenics](https://williamdurand.fr/2013/06/03/object-calisthenics/).

Ce sont des pratiques qui permettent de faire du code plus simple à lire et à modifier. Toujours dans le principe où le métier est bien compris à la base (sinon ça n'a pas grand intérèt).

Je constate aussi qu'Antoine a raison : je suis capable de mettre en application les bases du code (sans objets ni classes). Mais pour le moment les _habitudes_ pour faire du code propre ne sont que des théories sur le papiers à mon niveau. 

> Nous avons parler des _Code Smells_. C'est important de les voirs, de les sentir. C'est à partir de là que l'on voudra remanier le code
> -- Yannick

Yannick a piloté l'extraction de la méthode `calculBonus`.

> Je me rends compte que ça pourrait être intéressant de faire le refactoring sujet par sujet, et de les nommer dans le message de commit. Un pattern d'apprentissage tiré de la cuisine à code.
> -- Yannick

En regardant le catalogue de refactoring, nous pouvons lister quelques mouvements que nous avons effectué

- Change Function Declaration
- Extract Function
- Extract Variable
- Return Modified Value

Je pense que ça mériterais de pendre le temps de le noté sur chaque commit, pour que ça puisse raconter une histoire. 
et aussi une aide mémoire pour que je puisse retrouver mes petits.

