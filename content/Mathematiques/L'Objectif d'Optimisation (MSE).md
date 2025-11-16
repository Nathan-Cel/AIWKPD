****

Pour trouver les meilleurs [[Coefficients du modèle (β)|coefficients]] pour notre [[Le Modèle de Régression Multiple|modèle de régression]], nous devons définir ce que "meilleur" signifie.

L'approche standard est de **minimiser l'erreur** entre les valeurs réelles `Y` et les valeurs prédites `Ŷ`.

### La Fonction de Coût : MSE
La fonction de coût (ou "perte") la plus utilisée en régression est l'**Erreur Quadratique Moyenne** (MSE - Mean Squared Error).

Elle se calcule comme la moyenne des carrés des erreurs pour chaque observation :
$$
\epsilon = MSE = \frac{1}{n} \sum_{i=1}^{n} (Y_i - \hat{Y}_i)^2
$$
- `n` est le nombre d'observations.
- `(Yᵢ - Ŷᵢ)` est l'erreur (ou résidu) pour la i-ème observation.

L'objectif de l'entraînement du modèle est donc de trouver le vecteur `β` qui minimise cette valeur `ε`. C'est un problème d'optimisation.

---
*Source : [[Hub : Modèles Mathématiques d'Apprentissage]]*
