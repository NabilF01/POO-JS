## Exercice 1 : Classes et Objets

**Objectif :** Comprendre la création de classes et d'objets.

### Consignes

1. Créez une classe `Voiture` avec les attributs `marque`, `modele`, `annee`, et `couleur`.
2. Ajoutez une méthode `afficherDetails` permettant d'afficher les caractéristiques de la `Voiture`. 
3. Créez une instance de cette classe et initialisez ses attributs.
4. Affichez les détails de la voiture.

```js

class Voiture {
    constructor(marque, modele, annee, couleur) {
        this.marque = marque;
        this.modele = modele;
        this.annee = annee;
        this.couleur = couleur;
    }
    afficherDetails() {
        return `La voiture est une ${this.marque} qui a pour modèle ${this.modele} sortie en année ${this.annee} de couleur ${this.couleur}.`;
    }
}

const voiture1 = new Voiture('BMW', 'X4', '2024', 'bleue');

console.log(voiture1.afficherDetails());

```