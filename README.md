# 🚀 GOBAN JS — Application Web de Jeu de Go

## 📝 Description

GOBAN JS est une application web haute performance dédiée au jeu de Go, développée intégralement en JavaScript natif (Vanilla JS) pour son moteur de règles, tout en intégrant le framework Bootstrap pour une interface utilisateur moderne et réactive.
Le projet traduit les règles millénaires du Go en un système informatique déterministe absolu, reposant sur une architecture modulaire et une gestion stricte de la topologie de graphes.

Le jeu propose une expérience fluide et adaptative mêlant :
- Modélisation dynamique du Goban (tailles 9x9, 13x13 et 19x19)
- Interface utilisateur responsive conçue avec Bootstrap
- Gestion algorithmique des groupes de pierres et décompte des libertés
- Moteur de règles déterministe (captures, détection du suicide, règle du Ko)
- Phase de fin de partie avec calcul dynamique du territoire (Flood-fill)
- Horloges asynchrones et algorithme décisionnel stochastique
- Intégration de supports médias (logo dynamique et vidéo d'ambiance)

## 🎮 Gameplay

### Objectif

Encercler un maximum de territoire sur le plateau et capturer les pierres adverses en :
- Occupant les intersections clés de la grille
- Étouffant les libertés (points de respiration) des groupes ennemis
- Évitant les coups illégaux (suicide et répétition d'état de plateau)

### Mécaniques principales

- ⚪⚫ **Placement libre de pierres** sur la grille
- 🔗 **Chaînage automatique** des pierres adjacentes en "Groupes"
- 🫁 **Calcul en temps réel** des "Libertés" orthogonales
- 💥 **Système de capture** et purge automatique de la matrice
- ⛔ **Invalidation et rollback** automatique des coups interdits (Suicide & Ko)
- 🧹 **Phase interactive** de nettoyage des pierres mortes en fin de partie
- 📐 **Décompte automatique** du territoire avec application du Komi (7.5 points)
- ⏱️ **Chronomètres asynchrones** gérés par joueur

## ⌨️ Contrôles & Interactions

| Mode / Action | Interaction Utilisateur |
| :--- | :--- |
| **Poser une pierre** | Clic gauche sur une intersection libre du Goban |
| **Passer son tour** | Clic sur le bouton "Passer" |
| **Purger pierre morte** | Clic sur un groupe mort lors de la phase de scoring |
| **Changer de taille** | Menu de sélection d'interface (9x9, 13x13, 19x19) |
| **Réinitialiser** | Clic sur le bouton de réinitialisation |

## 🧠 Fonctionnalités techniques

### 🎨 Rendu Web & UI Responsive
- Intégration du framework Bootstrap pour la mise en page (grille, composants UI et réactivité multi-écran)
- Feuille de style personnalisée (`style.css`) pour l'habillage spécifique du plateau
- Support d'éléments multimédias (`Img_logo.png` et `img_logo_live.mp4`)

### 🔄 Algorithmique & Logique JavaScript (`Idx_script.JS`)
- Structuration du plateau sous forme de matrice 2D à accès direct O(1)
- Parcours de graphe (DFS / Flood-fill) pour le calcul des libertés et du territoire
- Détection des composants connexes (Groupes de pierres)
- Sérialisation d'état (JSON) pour le respect strict de la règle du Ko
- Algorithme décisionnel gérant le tirage de coups légaux par mélange stochastique (Fisher-Yates)
- Gestion de l'asynchronisme via `setInterval` pour les horloges de jeu

## 📁 Structure du projet

```text
📦 Projet dev_web
 ┣ 📂 Img/
 ┃ ┣ 🖼️ Img_logo.png         # Logo principal de l'application
 ┃ ┗ 🎥 img_logo_live.mp4    # Vidéo / Animation de présentation
 ┣ 📂 Js/
 ┃ ┗ 📜 Idx_script.JS        # Moteur de règles, logique du jeu et algorithmes
 ┣ 📂 css/
 ┃ ┗ 🎨 style.css            # Styles personnalisés et habillage du Goban
 ┣ 📄 Index.html             # Structure HTML5 avec composants Bootstrap
 ┗ 📄 README.md              # Documentation du projet
```

## ⚙️ Installation & Lancement

### Prérequis

- Un navigateur web moderne (Chrome, Firefox, Edge, Safari) compatible ES6+.

### Lancement

1. Cloner le dépôt GitHub :
   ```bash
   git clone [https://github.com/Dembolton/Projet-Dev_web.git](https://github.com/Dembolton/Projet-Dev_web.git)
   ```

2. Exécuter l'application :
   Ouvrir directement le fichier `Index.html` dans votre navigateur web.

## 📊 Système de score

Formule du score final (Standard Français) :
`Score = Territoire + Captures adverses - Pénalités - Pierres Mortes (+ Komi de 7.5 pour Blanc)`

- Komi de 7.5 points accordé au joueur Blanc pour compenser le désavantage du premier coup.
- Le demi-point (0.5) rend l'égalité mathématiquement impossible.

## ⚠️ Conditions de fin de partie

- 🛑 Deux abandons de tour consécutifs (passes)
- ⏱️ Dépassement du temps imparti au chrono
- 🏳️ Abandon manuel d'un des joueurs

## 🎓 Cadre du projet

Ce projet a été réalisé dans un cadre académique d'expérimentation en ingénierie logicielle et développement web (Université Toulouse Capitole — L3 MIAGE).
Il fait la démonstration de l'implémentation de structures de données complexes et d'algorithmes de théorie des graphes associés à une interface utilisateur moderne sous Bootstrap.

## ✨ Améliorations possibles

- Implémentation d'un Hash de Zobrist pour optimiser la vérification de la règle du Ko
- Intégration d'une Intelligence Artificielle avancée (Minimax ou Search MCTS)
- Support du protocole GTP (Go Text Protocol)
- Module multijoueur en temps réel via WebSockets

## 👤 Auteurs

- **Joël-Élisée Dembele**  
  📧 joeleliseefac@gmail.com  
  🔗 [LinkedIn](https://www.linkedin.com/in/joel-elisi%C3%A9e-dembele-423a3b293)

- **Abderahim Abba Adji**  
  🔗 [LinkedIn](https://www.linkedin.com/in/abderahim-abba-adji-b76b96354/)
