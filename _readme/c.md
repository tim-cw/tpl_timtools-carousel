# Semaine 03 - Ma première composante

## `ÉTAPE 3` - Optimiser notre instance de carousel

Lors de l'instanciation de `Swiper` (new Swiper), le premier paramètre est un sélecteur d'élément HTML et la documentation indique de prendre `.swiper` ou `document.querySelector('.swiper)`.
Swiper ne connait pas nos instances de Carousel ainsi que l'élément HTML désiré `data-component="Carousel"`. Il n'y a aucun lien entre la boucle `for` du `Main` et l'instance qu'on a créé. Pour cette raison, nous allons plutôt passer l'élément HTML en référence (paramètre) lors de la création de l'instance.

1. Dans la classe `Main` passez en paramètre de l'instanciation de votre `Carousel` (new Carousel) l'élément HTML (const `element`)

1. Dans la classe Carousel, ajouter en paramètre du constructor l'élément HTML passé ci-haut. (`constructor(element)`)

1. Au **tout début** de votre constructeur, assignez ce paramètre à une variable globale nommée `element`.

1. Finalement, comme premier paramètre de l'instanciation de `Swiper`, au lieu de lui passer vous-même un sélecteur, utilisez plutôt votre variable globale `element` fraîchement créé.

Dans votre navigateur, faites défiler la page afin de pouvoir voir le bas du tout premier carousel et sa pagination ainsi que le deuxième AVEC les flèches de navigation.

1. Cliquez sur une flèche de navigation du deuxième carousel et observez le premier en même temps. Les deux carousels se déplaceront en même temps alors que vous n'avez interragit avec la navigation du deuxième. Ça se produit pour les carousels n'ayant PAS de navigation, ce qui peut être un problème car nous n'en voulons pas tout le temps.

Tous les paramètres de `Swiper` contenant un sélecteur HTML doivent être modifier pour éviter ce problème et s'assurer que chaque éléments (pagination, navigation, etc.) d'un carousel ne contrôle que l'instance en question. Afin d'éviter ce problème :

1. Pour la pagination, changer la valeur de `el` pour `this.element.querySelector('.swiper-pagination')`

1. Pour la navigation, changer la valeur de `nextEl` et `prevEl` pour `this.element.querySelector('.swiper-button-next|.swiper-button-prev')`

1. Testez! Le comportement ne devrait PLUS se reproduire. Si oui, vérifiez à nouveau vos sélecteur ou encore assurement d'avoir passé votre variable globale element comme premier paramètre à l'instanciation de `Swiper`.

Avez-vous remarqué ici qu'on ne va PAS chercher les éléments à l'aide du `document` mais plutôt de `this.element`? this.element représente l'élément HTML sur lequel nous venons d'instancier notre classe `Carousel`. On s'assure que le querySelector cherche la navigation et la pagination uniquement `qu'à l'intérieur` de cet élément et pas dans TOUT notre HTML (document).

<br><br><hr>

[Passer à l'étape suivante ▶](d.md)

<hr>

[◀ Retourner à l'étape précédente](b.md)
