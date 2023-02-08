# Semaine 03 - Ma première composante

## `ÉTAPE 3` - Optimiser notre instance de carousel

Lors de l'instanciation de `Swiper` (new Swiper), le premier paramètre est un sélecteur d'élément HTML et la documentation indique de prendre `.swiper` ou `document.querySelector('.swiper)`.
Swiper ne connait pas nos instances de Carousel ainsi que l'élément HTML désiré `data-component="Carousel"`. Il n'y a aucun lien entre la boucle `for` du `Main` et l'instance qu'on a créée. Pour cette raison, nous allons plutôt passer l'élément HTML en référence lors de la création de l'instance.

1. Dans la classe `Main` passez en paramètre de l'instanciation de votre `Carousel` (new Carousel) l'élément HTML (const `component`)

1. Dans la classe Carousel, ajouter en paramètre du constructor l'élément HTML passé ci-haut. (`constructor(element)`)

1. Assignez-le à une variable globale nommée `element`.

Dans votre navigateur, faites défiler la page afin de pouvoir voir le bas du tout premier carousel et sa pagination ainsi que le deuxième AVEC les flèches de navigation.

1. Cliquez sur une flèche de navigation du deuxième carousel et observez le premier en même temps. Les deux carousels se déplaceront en même temps alors que vous n'avez interragit avec la navigation du deuxième.

Tous les paramètres de `Swiper` contenant un sélecteur HTML doivent être modifier pour éviter ce problème et s'assurer que chaque éléments (pagination, navigation, etc.) d'un carousel ne contrôle que l'instance en question. Afin d'éviter ce problème :

1. Pour la pagination, changer la valeur de `el` pour `this.element.querySelector('.swiper-pagination')`

1. Pour la navigation, changer la valeur de `nextEl` et `prevEl` pour `this.element.querySelector('.swiper-button-next|.swiper-button-prev')`

<br><br><hr>

[Passer à l'étape suivante ▶](d.md)

<hr>

[◀ Retourner à l'étape précédente](b.md)
