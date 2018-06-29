# Rattrapage-ARE

- une présentation rapide de votre projet : contexte, thématique et 
enjeux rapidement présentés, et votre modèle, si possible en utilisant 
une petite portion de code (20 lignes max) ;
- une démonstration de votre projet en action, par une simulation 
complète ou pas-à-pas ;
- une identification des paramètres clefs de votre simulation (par 
exemple la population initiale, son renouvellement à chaque étape…), et 
une étude de l'influence de ces paramètres sur votre modèle, avec une 
démonstration prête à l'emploi si nécessaire.

# Projet Feu de Foret:

![Alt Text](https://wallpapercave.com/wp/cvoz2gS.jpg)
# Présentation  du Sujet:

Les incendies ont toujours constitué une menace pour les forêts. Aujourd'hui, avec le changement climatique en cours, le risque s'aggrave. Pour qu'un feu se déclenche, il est indispensable de réunir trois ingrédients : un combustible, un comburant et aussi une énergie d'activation, une source de chaleur. Dans le cas des feux de forêt, la végétation est le combustible, l'air et l'oxygène le comburant et la moindre étincelle peut alors suffire à apporter une énergie d'activation suffisante. 

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

Après avoir comis 
