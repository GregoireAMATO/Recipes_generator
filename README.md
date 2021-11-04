# Objectif du projet 
Construire un outil permettant d'aider une personne à planifier ses repas pour la semaine. 
# Exemple d'utilisation de la version finale 
## Pas de compte utilisateur 
L'utilisateur arrive sur la page d'accueil, sur laquelle lui est proposé un ensemble de repas pour une semaine, 14 repas. Ces repas sont sélectionnés selon un critère de disponibilité des ingrédients à un instant T (saison) et d'impact carbone. Afin d'affiner ces propositions, l'utilisateur peux également préciser son régime alimentaire ainsi que les aliments allergènes qu'il souhaite exclure. Il peut également exclure un repas (s'il a prévu de manger dehors par exemple) ou de préciser qu'il s'amène à manger au travail, l'application va alors lui proposer des repas adaptés, faciles et rapides à préparer, végétariens, et pouvant être préparés la veille.
Si besoin, l'utilisateur peut supprimer un plat qui ne lui plaît pas. L'application va donc lui proposer de nouveaux plats en fonction des conditions précédentes et en évitant au maximum la répétition dans la semaine. 
Lorsque l'utilisateur est satisfait de son menu de la semaine, il peut commencer à éditer sa liste de course, en décochant les aliments qu'il possède déjà, puis la télécharger ou l'éditer en ligne. 
Sans compte, toutes ces données ne seront pas conservées.

## Avec un compte utilisateur 
Toutes les fonctionnalités précédentes s'appliquent, mais l'utilisateur peut également indiquer qu'une recette lui plait ou non. Lors de sa première connexion, l'utilisateur est invité à remplir une fiche, permettant de spécifier ses allergies, ses contraintes récurrentes (travail, peu de temps pour manger...). De plus, chaque jour, une option se débloque, permettant à l'utilisateur d'indiquer que la recette qu'il a goûté lui plaît ou non. Il peut également indiquer une remarque, une modification des quantités indiquées afin qu'elle soit plus à son goût... 
Un algorithme sera ensuite chargé d'analyser toutes les données de l'utilisateur afin de lui proposer chaque semaine des plats adaptés à ses goûts et à ses besoins.
L'utilisateur aura également accès à beaucoup de statistiques concernant ses apports nutritionnels théoriques, l'impact de son alimentation sur ses émissions de CO2...
L'utilisateur peut également enregistrer sa liste de courses, et si besoin, stocker les aliments présents dans le frigo de l'utilisateur, afin de décocher automatiquement les aliments déjà présents. 
L'utilisateur peut également ajouter une photo, qu'il peut choisir de partager ou non avec les autres.

# Principales étapes 
## Version fonctionnelle la plus simple 
L'utilisateur arrive sur la page d'accueil, sur laquelle lui est proposé un ensemble de repas pour une semaine, 14 repas. Ces repas sont sélectionnés selon un critère de disponibilité des ingrédients et d'impact carbone. Afin d'affiner ces propositions, l'utilisateur peux également préciser son régime alimentaire ainsi que les aliments allergènes qu'il souhaite exclure. Il peut également exclure un repas (s'il a prévu de manger dehors par exemple) ou de préciser qu'il s'amène à manger au travail, l'application va alors lui proposer des repas adaptés, faciles et rapides à préparer, végétariens, et pouvant être préparés la veille.
Si besoin, l'utilisateur peut supprimer un plat qui ne lui plaît pas. L'application va donc lui proposer de nouveaux plats en fonction des conditions précédentes et en évitant au maximum la répétition dans la semaine. 
Lorsque l'utilisateur est satisfait de son menu de la semaine, une liste de course s'affiche en dessous

## Etapes du projet
1. Récupérer les données concernant les fruits et légumes de saison DONE
2. Créer une fonction qui prend en entrée un entier, pour le nombre de plats à renvoyer, et renvoie les plats ne comportant que des fruits et légumes de saison
3. Ajouter un filtre pour la provenance du plat (asiatique, français...)
4. Ajouter un filtre concernant le régime alimentaire
5. Adapter la fonction pour pouvoir exclure des plats directement (afin d'éviter d'avoir 2 fois la même chose la même semaine, lorsqu'on veut changer un plat)
6. Créer une fonction prenant en entrée une liste de plats et qui renvoie une liste de course
7. Créer une fonction permettant de dire si un plat est végétarien ou pas (variable dummy)


## Profils de repas 

### Le repas de midi en semaine :
Ici deux possibilités :
    - Au travail : Place limité, on cherche à privilégier les repas froids et également rapide à préparer, puisqu'en général on le prépare le soir 
    - En télétravail : Place illimitée, on privilégiera les plats rapides à préparer et on le fait la veille


### Le repas du soir en semaine : 
On peut se permettre de préparer des plats un peu plus longs, mais en général on va chercher à privilégier un plat qui peut se congeler facilement, cela peut permettre de prévoir les jours de rush



Liens utiles :
- https://www.data.gouv.fr/fr/datasets/agribalyse-r-synthese-1/ 
- https://github.com/datagir/mesfruitsetlegumesdesaison/blob/master/public/data/products.json
- https://www.greenpeace.fr/guetteur/calendrier/
