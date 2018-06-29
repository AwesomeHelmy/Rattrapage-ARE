# Rattrapage-ARE

# Projet Feu de Foret:

![Alt Text](https://wallpapercave.com/wp/cvoz2gS.jpg)
# Présentation  du Sujet:

Les incendies ont toujours constitué une menace pour les forêts. Aujourd'hui, avec le changement climatique en cours, le risque s'aggrave. Pour qu'un feu se déclenche, il est indispensable de réunir trois ingrédients : un combustible, un comburant et aussi une énergie d'activation, soit une source de chaleur. Dans le cas des feux de forêt, la végétation est le combustible, l'air et l'oxygène le comburant et la moindre étincelle peut alors suffire à apporter une énergie d'activation suffisante. 

Notre but est alors de simuler la propagation d'un feu de foret afin d'observer son comportement en fonction de differents parametres comme la chaleur, la distance entre les arbres,...

# Règles de la modélisation :

Nous simulons notre modélisation dans une matrice. Les cellules de cette matrice peuvent prendre les valeurs suivantes :

0: vide(blanc) __  1: arbre(vert) __  2: végétation(gris) __   3: feu(rouge)  __  4: cendre(noir)

![](https://www.researchgate.net/profile/Maoteng_Zheng/publication/318869365/figure/fig3/AS:552848645267456@1508820796878/8-directions-in-the-neighborhood-of-a-pixel.png)

Initialement, le modélisation se lance avec une seule cellule en feu choisi aléatoirement.
Le feu ensuite se propage au fur et à mesure que le temps passe dans 8 directions différentes selon les paramètres suivants: La chaleur dans la foret, la presence de végétation, la direction de soufflement du vent et enfin un facteur de "chance" représentant les différents facteurs qu'on a pas pris en considération. 

![code](https://user-images.githubusercontent.com/36737929/42052757-fdf6d9d0-7b0f-11e8-987b-c4d2f4a6df30.png)

Cette partie du code nous présente justement comment le feu se propage d'une cellule déja en feu aux cellules d'en bas {i-1} pour un vent nul après avoir pris en considération plusieurs facteurs et leur probabilités pour pouvoir calculer une probabilité générale qui devra dépasser un certain seuil pour que la cellule soit en feu. 


# Paramètres: 

On a donc plusieurs paramètres:
la chaleur, la chance aléatoire, la probabilite de feu selon le type de cellule (veg a veg ou veg a arbre,..) , mais le plus important de tout c'etait le paramètre du vent. 

![chart](https://user-images.githubusercontent.com/36737929/42071977-86b23fdc-7b5e-11e8-9782-5749c486622f.png)

On observe sur excel que le feu de foret qui brule le plus rapidement et s'etteind ainsi le plus rapidement est le feu ou le vent est present puisque le nombre de pas necessaire pour bruler la foret plus inferieure. 
De meme, on observe que les effets de la chaleur sont les plus insignifiant du point de vue que ca change peut a rapidite a laquelle plus les arbres.
Donc le paramètre clef de cette modélisation est le vent soit l'oxyegene qui est justement le comburant dans notre feu de foret et ce qui apparait donc logique.

![untitled10](https://user-images.githubusercontent.com/36737929/42072647-e8ebf50a-7b61-11e8-8b34-3d4e3ee2848a.png)

# Problèmes:

On a eu beaucoup de difficultés avec l'animation qui ne fonctionne pas. On a eu aussi certains resultats qui posent problemes ou le feu va se propager dans 2 directions et pas les deux autres comme par exemple dans le cas vu précédemment, ou le feu se propage au Nord et a l'Ouest mais pas au sud et l'Est alors que selon la modélisation, le feu devrait se répendre dans toutes les directions ensuite s'étteindre potentiellement dans les endroits ou la probabilité de feu est plus bas que le seuil.
