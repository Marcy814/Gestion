# Gestion d'une Bibliothèque

## Description
Ce projet consiste en la création d'une application Python pour gérer une bibliothèque. L'application permet de gérer les livres, les auteurs et les emprunteurs, ainsi que les actions courantes telles que l'ajout de livres, la recherche de livres, l'emprunt et le retour de livres. Des tests unitaires ont été écrits pour valider le bon fonctionnement des différentes fonctionnalités.

## Structure du Projet

- `livre.py` : Contient la classe `Livre` représentant un livre de la bibliothèque.
- `auteur.py` : Contient la classe `Auteur` représentant un auteur.
- `emprunteur.py` : Contient la classe `Emprunteur` représentant un emprunteur de livres.
- `bibliotheque.py` : Contient la classe `Bibliothèque` qui gère les livres, les auteurs et les emprunteurs ainsi que les actions comme ajouter, emprunter et retourner des livres.
- `tests/` : Dossier contenant les tests unitaires pour chaque méthode de la classe `Bibliothèque`.

## Classes Principales

### `Livre`
- `id` : Identifiant du livre.
- `titre` : Titre du livre.
- `auteur` : Auteur du livre.
- `disponible` : Indique si le livre est disponible ou emprunté.

### `Auteur`
- `nom` : Nom de l'auteur.
- `nationalité` : Nationalité de l'auteur.
- `oeuvres` : Liste des œuvres écrites par l'auteur.

### `Emprunteur`
- `id` : Identifiant de l'emprunteur.
- `nom` : Nom de l'emprunteur.
- `livres_empruntés` : Liste des livres empruntés par l'emprunteur.

### `Bibliothèque`
- `livres` : Liste des livres dans la bibliothèque.
- `auteurs` : Liste des auteurs disponibles.
- `emprunteurs` : Liste des emprunteurs.
- Méthodes :
  - `ajouter_livre(id, titre, auteur)`
  - `rechercher_livre(recherche)`
  - `emprunter_livre(id_livre, id_emprunteur)`
  - `retourner_livre(id_livre, id_emprunteur)`

## Fonctionnalités

- **Ajouter un livre** : Permet d'ajouter un nouveau livre dans la bibliothèque.
- **Rechercher un livre** : Permet de rechercher un livre par son titre ou son auteur.
- **Emprunter un livre** : Permet à un emprunteur d'emprunter un livre disponible.
- **Retourner un livre** : Permet à un emprunteur de retourner un livre qu'il a emprunté.

## Tests Unitaires
Les tests unitaires ont été écrits pour vérifier le bon fonctionnement des méthodes suivantes :

- Ajouter un livre.
- Rechercher un livre.
- Emprunter un livre.
- Retourner un livre.

Les tests couvrent aussi bien les cas positifs que négatifs (par exemple, emprunter un livre non disponible ou retourner un livre non emprunté).

### Exemple de Test

```python
import unittest
from bibliotheque import Bibliothèque
from livre import Livre
from auteur import Auteur
from emprunteur import Emprunteur

class TestBibliotheque(unittest.TestCase):
    
    def test_ajouter_livre(self):
        # Tester l'ajout d'un livre
        pass
        
    def test_rechercher_livre(self):
        # Tester la recherche d'un livre
        pass

    def test_emprunter_livre(self):
        # Tester l'emprunt d'un livre
        pass

    def test_retourner_livre(self):
        # Tester le retour d'un livre
        pass

if __name__ == '__main__':
    unittest.main()
