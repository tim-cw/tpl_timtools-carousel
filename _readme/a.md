# Semaine 03 - Ma première composante

## `ÉTAPE 1` - La classe Carousel

La première étape est de se créer une classe Carousel et d'y ajouter le code nécessaire pour qu'elle fonctionne

### Avant de commencer

1. Est-ce que Swiper est installé dans votre projet?
1. Assurez-vous que les styles de `Swiper` soient importé dans le `main.scss`

Tous les modules de Swiper ont des styles propres à eux à importer. Vérifiez la documentation.

### Création de la classe Carousel

1. Dans un nouveau fichier nommé `Carousel.js` ajouter le code nécessaire pour avoir une classe fonctionnelle (constructor et init)
1. Il ne faut pas se créer de nouvelle instance à ce stade-ci
1. Mettre un `console.log` dans le init : "Initialisation de ma composange Carousel"

Le `console.log` ne fonctionne pas pour l'instant, nous allons maintenant nous créer une nouvelle instance dans notre Main

Pour respecter l'approche par composante, nous allons utiliser les attributs data pour sélectionner nos composantes. En appliquant un data-component sur tous les éléments qui doivent s'activer dans notre Javascript, notre code sera facilement réutilisable. La valeur de notre data-component sera la composante qu'on veut qui s'active.

### Ajout de la boucle pour créer les nouveaux carousels

1. Ajouter l'attribut `data-component="Carousel"` sur tout les éléments HTML qui représentent vos carousels `('.swiper')`
1. Dans le init de votre classe `Main` ajouter une variable local `components`
1. Votre variable `components` doit selectionner tous les éléments HTML qui ont l'arribut `data-component="carousel"`
1. Faire une boucle `for` qui boucle dans tous les éléments HTML que contient votre variable `components`
   1. Assigner l'élément du tableau à la position `[i]` , à une variable locale nommé `component`;
   1. Faire une nouvelle instance de votre carousel (`new`)
1. Votre `console.log` du `Carousel` devrait maintenant s'afficher.

Si ce n'est pas le cas faite des `console.log` dans de votre init pour voir si tout fonctionne comme vous le désirez.
<br><br><hr>

[Passer à l'étape suivante ▶](b.md)

<hr>

[◀ Retourner à l'intro](../readme.md)
