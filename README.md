# 🧠♟️ IA Échecs Évolutive - Apprentissage par Renforcement

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-yellow.svg)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Chess.js](https://img.shields.io/badge/Chess.js-v0.10.3-blue.svg)](https://github.com/jhlywa/chess.js)

> Un moteur d'échecs intelligent qui **apprend de ses victoires et défaites** en temps réel, utilisant une combinaison d'algorithmes classiques (Minimax, Alpha-Beta) et d'apprentissage par renforcement.

![Demo](https://img.shields.io/badge/Status-Fonctionnel-success)

## 🎯 Caractéristiques Principales

### Intelligence Artificielle Évolutive
- 🧠 **Apprentissage adaptatif** : L'IA ajuste ses poids après chaque partie
- 🌲 **Algorithme Minimax avec Alpha-Beta Pruning** : Recherche optimisée dans l'arbre de jeu
- 📊 **Tables de position** : Utilise des stratégies d'échecs classiques (70%) + apprentissage (30%)
- 🎯 **Move Ordering** : Priorise les captures, échecs et promotions pour une recherche plus efficace
- 🔄 **Profondeur ajustable** : Choisissez entre 2 (rapide), 3 (normal) ou 4 (expert)

### Visualisation en Temps Réel
- 🌲 **Arbre d'analyse** : Visualisez les coups évalués par l'IA en temps réel
- 🗺️ **Carte des poids** : Observez quelles positions l'IA préfère pour chaque pièce
- 📈 **Graphique d'évolution** : Suivez le taux de victoire sur 20 parties
- 📊 **Statistiques détaillées** : Victoires, défaites, nuls, taux de réussite
- ⚡ **Compteur de performance** : Positions évaluées et temps de calcul

### Interface Moderne
- 🎨 **Design sombre élégant** avec animations fluides
- 🖼️ **Pièces haute qualité** provenant de Chess.com
- 📱 **Responsive** : S'adapte à tous les écrans
- 💾 **Sauvegarde automatique** : La mémoire de l'IA persiste entre les sessions

## 🚀 Installation & Utilisation

### Option 1 : Utilisation directe (Recommandé)
1. Téléchargez le fichier `chess_ai.html`
2. Ouvrez-le dans votre navigateur web moderne (Chrome, Firefox, Safari, Edge)
3. Commencez à jouer ! 🎮

### Option 2 : Serveur local
```bash
# Cloner le repository
git clone https://github.com/votre-username/chess-ai-evolutif.git
cd chess-ai-evolutif

# Ouvrir avec un serveur local (Python 3)
python -m http.server 8000

# Ou avec Node.js (npx http-server)
npx http-server

# Accéder à http://localhost:8000
```

## 🎮 Comment Jouer

1. **Vous jouez les Blancs** (pièces en bas)
2. **L'IA joue les Noirs** (pièces en haut)
3. Déplacez vos pièces en **glissant-déposant**
4. L'IA réfléchit et joue automatiquement
5. Observez son analyse dans le panneau de droite

### Contrôles
- 🔄 **Nouvelle Partie** : Recommencer une partie
- 🗑️ **Reset Mémoire** : Effacer l'apprentissage de l'IA
- 🎛️ **Profondeur** : Ajuster la difficulté (2-4)
- 🗺️ **Boutons de pièces** : Voir la carte d'apprentissage de chaque type

## 🧪 Technologies Utilisées

- **JavaScript ES6+** : Logique principale
- **[Chess.js](https://github.com/jhlywa/chess.js)** : Règles d'échecs et validation des coups
- **[Chessboard.js](https://chessboardjs.com/)** : Interface graphique de l'échiquier
- **jQuery** : Manipulation DOM simplifiée
- **LocalStorage** : Persistance de la mémoire de l'IA
- **SVG** : Graphiques de performance

## 📊 Architecture de l'IA

### Évaluation de Position
```javascript
Score = Matériel + (PositionStandard × 0.7) + (PoidsAppris × 0.3) + Mobilité
```

### Composants Principaux
1. **Fonction d'évaluation** (`evaluateBoard`)
   - Valeur matérielle des pièces
   - Tables de position standard (Piece-Square Tables)
   - Poids appris par renforcement
   - Bonus de mobilité

2. **Algorithme Minimax** (`minimax`)
   - Recherche en profondeur (2-4 coups)
   - Alpha-Beta Pruning pour optimisation
   - Move Ordering pour efficacité

3. **Apprentissage** (`learnFromGame`)
   - +20 points pour les positions gagnantes
   - -25 points pour les positions perdantes
   - Limitation des poids (-500 à +500)

## 📈 Performance

| Profondeur | Positions évaluées | Temps moyen | Niveau |
|------------|-------------------|-------------|---------|
| 2          | ~1,000            | < 1s        | Débutant |
| 3          | ~5,000            | 1-3s        | Intermédiaire |
| 4          | ~25,000           | 3-10s       | Avancé |

## 🎯 Roadmap

### Version Actuelle (v2.0)
- ✅ Apprentissage par renforcement
- ✅ Visualisation de l'arbre d'analyse
- ✅ Tables de position standard
- ✅ Alpha-Beta Pruning

### Améliorations Futures
- [ ] Ouvertures préenregistrées
- [ ] Fin de partie optimisée
- [ ] Apprentissage par base de données de parties
- [ ] Mode multijoueur en ligne
- [ ] Analyse de parties PGN
- [ ] Suggestions de coups pour le joueur
- [ ] Niveaux de difficulté prédéfinis

## 🤝 Contribution

Les contributions sont les bienvenues ! Voici comment participer :

1. Fork le projet
2. Créez une branche (`git checkout -b feature/AmeliorationIncroyable`)
3. Committez vos changements (`git commit -m 'Ajout d'une amélioration'`)
4. Push vers la branche (`git push origin feature/AmeliorationIncroyable`)
5. Ouvrez une Pull Request

### Idées de contribution
- 🐛 Correction de bugs
- ✨ Nouvelles fonctionnalités
- 📝 Amélioration de la documentation
- 🎨 Améliorations visuelles
- ⚡ Optimisations de performance

## 📝 License

Ce projet est sous licence MIT. Voir le fichier [LICENSE](LICENSE) pour plus de détails.

## 🙏 Remerciements

- **Chess.js** - Pour la logique d'échecs robuste
- **Chessboard.js** - Pour l'interface graphique élégante
- **Chess.com** - Pour les magnifiques images de pièces
- **Communauté Chess Programming** - Pour les algorithmes classiques

## 📞 Contact & Support

- 🐛 **Bug Reports** : Ouvrez une [issue](https://github.com/votre-username/chess-ai-evolutif/issues)
- 💬 **Discussions** : Utilisez les [discussions GitHub](https://github.com/votre-username/chess-ai-evolutif/discussions)
- ⭐ **Star le projet** si vous l'aimez !

## 📚 Ressources & Apprentissage

Pour en savoir plus sur la programmation d'échecs :
- [Chess Programming Wiki](https://www.chessprogramming.org/)
- [Minimax Algorithm](https://en.wikipedia.org/wiki/Minimax)
- [Alpha-Beta Pruning](https://en.wikipedia.org/wiki/Alpha%E2%80%93beta_pruning)
- [Piece-Square Tables](https://www.chessprogramming.org/Piece-Square_Tables)

---

<div align="center">

**Développé avec ❤️ et ♟️**

[⬆ Retour en haut](#-ia-échecs-évolutive---apprentissage-par-renforcement)

</div>
