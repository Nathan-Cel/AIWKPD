
# De quoi on parle

Quand on parle ici d’**analyse de la variance**, il s’agit d’examiner comment la variabilité totale des données peut être décomposée entre ce que le modèle **explique** et ce qu’il **n’explique pas**.  
Contrairement à la **[[Mean Squared Error]]**, qui mesure le **niveau d’erreur global**, les formules qui suivent cherchent à **analyser l’origine et la répartition** de cette erreur.

## Décomposition

Comme mentionné précédemment, la variation des valeurs observées est en partie explicable par le modèle (ESS). Il reste cependant une partie non-expliquée par le modèle (RSS) et ceci se modélise par la formule :  
$$TSS=ESS+RSS$$

# Total Sum of Squares (TSS)

Cette mesure est faite sans introduire le modèle pour comprendre à quel point la variable y "s'éparpille". Plus cette mesure est grande plus il y a "à expliquer" et plus un modèle est intéressant. 
Pour prendre un exemple, prenons les notes de la classe d'un contrôle au hasard. Si toutes les notes sont entre 14 et 16, la variation totale sera très basse. Si on veut maintenant prédire la note d'un nouvel élève, un modèle n'apportera pas plus d'information qu'une simple estimation de base telle que prendre la moyenne. Mais si les notes varient entre 4 et 20 alors là la variation totale sera bien plus importante et un modèle sera bien plus intéressant.
La TSS se calcule comme suit : 
$$TSS=\sum_{i=1}^{n}(y_{i}-\bar{y}_{i})^{2}$$
Formule en français : 
Somme des différences entre les **valeurs observées** et leur **moyenne** au carré.

# Explained Sum of Squares (ESS)

On aborde d'abord la partie des variations "expliquée" par le modèle. Ici quand on dit "expliquée" on peut faire une simplification et parler de la partie des variations que le modèle "comprend". Donc plus cette partie est grande, plus le modèle est bon car s'il "comprend" les mouvements de la valeur observée, alors il peut mieux la prédire. 
Par exemple, si l'on arrivait à avoir un modèle où ESS = TSS, cela voudrait dire que les prédictions de ce modèle serait exacte à la virgule près à chaque fois (bien sûr c'est irréaliste mais c'est pour l'exemple).
L'ESS se calcule avec la formule suivante : 

$$ESS=\sum_{i=1}^{n}(\hat{y}_{i}-\bar{y}_{i})^2$$
Formule en français :
Somme des différences entre les **valeurs prédites par le modèle** et la **moyenne des valeurs observées** au carré.

# Residual Sum of Squares (RSS)

En opposition direct à l'ESS, la RSS est la partie des variations totales que le modèle ne "comprend" pas, donc plus la RSS est grande moins les prédictions du modèle seront précises.
Elle se calcule avec la formule suivante :

$$RSS=\sum_{i=1}^{n}(y_{i}-\hat{y}_{i})^{2}$$
Formule en français :
Somme des différences entre les **valeurs prédites par le modèle** et la **moyenne des valeurs observées** au carré

# R²

Enfin maintenant que nous avons ces mesures, nous pouvons déterminer la proportion de TSS qui est expliquée en utilisant soit ESS soi RSS :

$$R²=\frac{ESS}{TSS}=1-\frac{RSS}{TSS}$$

Et avec cette valeur on peut déterminer si:
#### R² tend vers 1
 Si R² est proche de 1 alors le modèle explique très bien les données et les prédit aussi très bien.

#### R² tend vers 0
Si R² est proche de 0 alors le modèle n’explique rien et les prédictions seront mauvaises


# Bonus R²

Maintenant qu'on a notre mesure de fiabilité du modèle, quel taux veut-on atteindre avec celui-ci? 
50% ?
80% ?
95% ?

Eh bien pour le coup ce n'est pas une question de math, ça a tout à voir avec le business understanding.





