# Semaine 03 - Ma première composante

## `ÉTAPE 5` - Pagination et navigation en option

### Voici ce qu'on cherche à faire avec cette étape:

Tout élément interactif doit posséder des _indices visuels_ fort qui incite à l'interaction. Un carousel sans pagination ni navigation où on ne voit qu'une image complète n'incite pas à tenter d'interragit avec.

Cependant, parfois on veut la navigation et d'autres fois, uniquement que la pagination. Vous pourriez être tenté de faire d'autres options à la pièce dans votre composante.

### N'en faites rien

Swiper fait déjà des vérifications afin d'éviter des erreurs JavaScript si certains éléments spécifiés dans les options n'existent pas. Dans nos options par défaut, nous spécifions toujours vouloir une pagination et une navigation. Cependant, si les sélecteurs (`el`) ne trouvent pas d'éléments, la fonctionnalité sera désactivée.

### Donc.. pour avoir une pagination

Pour ajouter une pagination, vous devez simplement :

1. Inclure le code HTML avec la classe exigée par Swiper, soit `.swiper-pagination` au bon endroit.

### Et pour une navigation ?

Exactement la même chose :

1. Inclure le code HTML avec la classe exigée par Swiper, soit `.swiper-button-prev` et `.swiper-button-next` au bon endroit.

Et si vous ne les voulez pas? Enlevez le HTML non désiré de votre code.

### Un bonus pour terminer
Un carousel plein écran peut-être visuellement intéressant. Parfois, vous pouvez désirer également un carousel qui entre à l'intérieur d'un wrapper et qui ne dépasse pas ni d'un côté, ni de l'autre.

Plusieurs d'entre-vous avez remarqué que l'élément `.swiper` a un `overflow: hidden;` par défaut et c'est cette propriété qui empêche les diapositives d'être visibles à l'extérieur.

Un autre effet visuellement intéressant avec le carousel reprend un mélange des 2 scénarios ci-haut et est très simple à effectuer. Suivez ces quelques étapes pour voir le résulat où le carousel commence contraint par le wrapper du côté gauche, mais sort à l'extérieur de ce dernier jusqu'à l'extrémité de votre fenêtre de navigateur pour un bris de grille qui rend votre site encore plus dynamique.

1. Dupliquez le code HTML de la dernière section contenant un carousel.
2. Ajoutez une deuxième classe css à l'élément HTML `.swiper`. Nommons-la `.swiper-full`.
3. Allez dans votre `carousel.scss` et ajoutez un nouveau sélecteur pour cette classe qui ne fait que modifier la propriété `overflow` à `visible`.
4. Jouez maintenant avec le carousel d'une extrémité à l'autre afin de voir le résultat.

Vous verrez cependant apparaître une barre de défilement horizontale au bas de votre site. On ne veut surtout pas celà.

Il ne suffit que de mettre un overflow: hidden; sur un parent du `.swiper` qui est pleine largeur (dont PAS le .wrapper).

1. Nous avons créé un `components` scss nommé `section` qui gère l'espacement vertical entre les grandes section. Allez-y ajouté à la règle un `overflow: hidden`. Tada!

<br><br>

# Bravo! Vous avez complétez le lab ! 💪

[◀ Retourner au début](../README.md)

<hr>

[◀ Retourner à l'étape précédente](d.md)
