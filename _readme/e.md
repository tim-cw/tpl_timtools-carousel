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
2. Chargez les styles du module `pagination` dans votre `Main.scss`

### Et pour une navigation ?

Exactement la même chose :

1. Inclure le code HTML avec la classe exigée par Swiper, soit `.swiper-button-prev` et `.swiper-button-next` au bon endroit.
2. Chargez les styles du module `navigation` dans votre `Main.scss`

Et si vous ne les voulez pas? Enlevez le HTML non désiré de votre code.

<br><br>

# Bravo! Vous avez complétez le lab ! 💪

[◀ Retourner au début](../README.md)

<hr>

[◀ Retourner à l'étape précédente](d.md)
