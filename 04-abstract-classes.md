## Exercice 4 : Polymorphisme

**Objectif :** Utiliser le polymorphisme.

### Consignes

1. Créez une classe `Animal` avec une méthode `faireDuBruit`.
2. Créez des classes `Chien` et `Chat` qui héritent de `Animal` et redéfinissent la méthode `faireDuBruit`.
3. Utilisez le polymorphisme pour afficher que `Le chien aboie` et que `Le chat miaule` lors de l'appel de la méthode `faireDuBruit`.

### Solution


```js
class Animal {
    faireDuBruit() {
        return "L'animal fait du bruit.";
    }
}

class Chat extends Animal {
    faireDuBruit() {
        return "Le chat miaule.";
    }
}

class Chien extends Animal {
    faireDuBruit() {
        return "Le chien aboie.";
    }
}

const monChat = new Chat();
const monChien = new Chien();
const monAnimal = new Animal();

console.log(monChat.faireDuBruit());
console.log(monChien.faireDuBruit());
console.log(monAnimal.faireDuBruit());
```