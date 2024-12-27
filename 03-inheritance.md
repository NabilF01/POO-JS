## Exercice 3 : Héritage

**Objectif :** Comprendre l'héritage entre classes.

### Consignes

1. Créez une classe `Vehicule` avec les attributs `marque`, `modele`, et `annee`.
2. Faites en sorte que la classe `Voiture` hérite de la classe `Vehicule` et possède l'attribut `couleur` (non présent dans la classe `Vehicule`).

### Solution


```js
class Vehicule {
    marque;
    modele;
    annee;
    constructor(marque, modele, annee) {
        this.marque = marque;
        this.modele = modele;
        this.annee = annee;
    }
    afficherDetails() {
        return `Le véhicule est un(e) ${this.marque} qui a pour modèle ${this.modele} sorti(e) en année ${this.annee}.`;
    }
}

class Voiture extends Vehicule {
    couleur;
    constructor(marque, modele, annee, couleur) {
        super(marque, modele, annee);
        this.couleur = couleur;
    }
    afficherDetails() {
        return `La voiture est un(e) ${this.marque} qui a pour modèle ${this.modele} sorti(e) en année ${this.annee} de couleur ${this.couleur}.`;
    }
}

const monVehicule = new Vehicule('Mercedes', 'Classe A', '2024');
const maVoiture = new Voiture('Renault', 'Clio III', '2010', 'blanche');

console.log(monVehicule.afficherDetails());
console.log(maVoiture.afficherDetails());
```