
## 1. Concepts Généraux

- **[[Types de Modèles d'Apprentissage (ML)|🎓 Les 2 Types de Modèles d'Apprentissage]]**
  - Une introduction à la [[Régression]] (quantitative) et à la [[Classification]] (qualitative).

- **[[Le Processus d'un Projet de Machine Learning|⚙️ Les Étapes d'un Projet]]**
  - De l'Observation au déploiement via une [[API]].

- **[[Autres Modèles du Semestre 2|📚 Modèles du S2]]**
  - Mention de la **PCA** (Réduction de dimension) et du **Clustering** (K-means, dbscan).

---

## 2. La Régression Linéaire Multiple

C'est le cœur de l'analyse, décomposé en plusieurs parties.

- **[[Le Modèle de Régression Multiple|🧠 Le Modèle et ses Écritures]]**
  - Présentation du modèle `ŷ = β₀ + β₁X₁ + ...` et de ses écritures vectorielle et matricielle.

- **[[L'Objectif d'Optimisation (MSE)|🎯 L'Objectif : Minimiser l'Erreur Quadratique Moyenne]]**
  - Définition de l'erreur `MSE = 1/n * Σ(Yᵢ - ŷᵢ)²` comme la fonction à minimiser.

- **[[La Solution par l'Équation Normale|💡 La Solution Mathématique (Équation Normale)]]**
  - La dérivation complète qui mène à la formule `β = (XᵀX)⁻¹ XᵀY`.

---

## 3. Exercices et Évaluation

- **[[Exercice 1 - Prédiction simple|✏️ Exercice 1 : Calculer Y]]**
  - Le premier exercice où il fallait calculer Y pour X1=9, X2=3, X3=6.

- **[[Exercice 2 - Calcul manuel des coefficients|💪 Exercice 2 : Calcul Complet d'un Modèle]]**
  - L'application pas à pas de l'Équation Normale sur un jeu de données (PC, Logiciels, Pannes).

- **[[Évaluation de la Précision du Modèle (Tao)|📊 Évaluation du Modèle (TSS, ESS, RSS)]]**
  - Le calcul de la performance du modèle via la décomposition de la variance.
