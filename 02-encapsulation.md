## Exercice 2 : Encapsulation

**Objectif :** Appliquer le concept d'encapsulation.

### Consignes

1. Modifiez la classe `Voiture` pour que ses attributs soient privés.
2. Ajoutez des `getters` et des `setters` pour chaques attributs.
3. Créer une instance de `Voiture` et modifiez en la couleur.

### Solution


```js

class Voiture {
    #marque = 'Renault';
    #modele = 'Clio III';
    #annee = '2010';
    #couleur = 'blanche';

    get Marque() {
        return this.#marque;
    }
    get Modele() {
        return this.#modele;
    }
    get Annee() {
        return this.#annee;
    }
    get Couleur() {
        return this.#couleur;
    }

    set Marque(marque) {
        this.#marque = marque;
    }
    set Modele(modele) {
        this.#modele = modele;
    }
    set Annee(annee) {
        this.#annee = annee;
    }
    set Couleur(couleur) {
        this.#couleur = couleur;
    }

    afficherDetails() {
        return `La voiture est une ${this.#marque} qui a pour modèle ${this.#modele} sortie en année ${this.#annee} de couleur ${this.#couleur}.`;
    }

}

const maVoiture = new Voiture();
maVoiture.Couleur = 'rouge';

console.log(maVoiture.afficherDetails());
console.log(maVoiture.Couleur);



```