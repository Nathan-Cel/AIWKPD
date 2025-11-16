
Le modèle de régression linéaire multiple postule une relation linéaire entre une variable cible `Y` et plusieurs variables explicatives `X₁, X₂, ..., Xₚ`.

### 1. Écriture Vectorielle
Pour une seule observation, le modèle s'écrit :
$$
\hat{Y} = β_0 + β_1 X_1 + β_2 X_2 + ... + β_p X_p
$$
- `Ŷ` est la valeur prédite.
- `β` sont les [[Coefficients du modèle (β)|coefficients]] (ou paramètres) que l'on cherche. `β₀` est l'ordonnée à l'origine (l'intercept).

### 2. Écriture Matricielle
Pour l'ensemble du jeu de données, on utilise une écriture plus compacte :
$$
\hat{Y} = Xβ
$$
Où :
- `Ŷ` est le vecteur de toutes les prédictions.
- `X` est la **matrice de design**, qui contient les données des variables `X` avec une première colonne de `1` pour l'intercept `β₀`.
- `β` est le vecteur contenant tous les coefficients du modèle.

---
*Source : [[Modèle Mathématique d'apprentissage]]*
