
# A quoi ça sert

Tout simplement à savoir à quel point les prédictions diffèrent des valeurs observées. La bonne chose avec la MSE est que sa formule est littéralement dans le nom :
	- Mean : moyenne
	- Squared : au carré
	- Error : erreur


## Mean 

La formule de la moyenne c'est toujours la même, la somme des éléments divisée par le nombre d'éléments : 

$$moyenne=\frac{1}{n}\sum_{i=1}^{n}(formule)$$

## Squared

Le tout au carré

## Error
Ici l'erreur c'est la différence entre prédiction et val observée. Et comme on parle de différence, on note le taux d'erreur : 

$$ \epsilon_{i}=y_{i}- \hat{y}_{i}$$

# MSE

Tout ensemble donne donc : 

$$ MSE=\frac{1}{n}\sum_{i=1}^{n}(y_{i}-\hat{y}_{i})^2$$

