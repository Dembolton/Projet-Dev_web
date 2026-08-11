# GOBAN JS

Implémentation web du jeu de Go traditionnel en JavaScript vanilla, gérant l'intégralité des règles complexes du plateau sans framework externe.

[▶️ Tester la démo en ligne](https://dembolton.github.io/Projet-Dev_web/)

![Aperçu de GOBAN JS](Projetdev_web/Img/Game_Content)

## Fonctionnalités et Algorithmique

* **Capture et libertés (Flood-Fill)** : Algorithme d'exploration de graphe pour calculer les libertés des groupes de pierres et gérer les captures multiples.
* **Gestion du Ko** : Détection automatique des répétitions de positions du plateau pour empêcher les boucles infinies de capture.
* **Calcul des scores** : Évaluation du territoire et des pierres capturées en fin de partie.

## Lancement en local

Projet en Vanilla JS sans dépendance d'installation.

### Option 1 : Directe
Ouvrir directement le fichier `index.html` dans n'importe quel navigateur moderne.

### Option 2 : Serveur local
```bash
# 1. Cloner le dépôt
git clone [https://github.com/Dembolton/Projet-Dev_web](https://github.com/Dembolton/Projet-Dev_web)
cd Projet-Dev_web

# 2. Lancer un serveur local léger
npx serve .
```
