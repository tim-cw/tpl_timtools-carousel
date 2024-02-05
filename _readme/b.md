# Semaine 03 - Ma première composante

## `ÉTAPE 2` - Construire notre classe Carousel

Dans cette prochaine étape nous ferons créerons une instance de `Swiper` avec des options par défaut qui se répéterons pour tous nos carousel.

### Dans votre classe Carousel

Souvenez-nous que le `this.init()` être positionné à un endroit particulier par rapport aux déclarations de variables qui se trouve dans le `constructor`.

1. Créez une variable globale nommée `options` de type objet {} et assignez les valeurs désirées qui s'appliqueront à toutes nos instances de la composante Carousel.

   - le nombre de diapositives par vue à 1
   - la marge entre les diapositives à 20
   - la pagination (sur le bon élément)
   - la navigation (sur le bon élément)

Voir la documentation de [swiper](https://swiperjs.com/swiper-api)

**Pour la pagination et la navigation, il ne faut PLUS utiliser le querySelector tel que vu en conception web 3 mais simplement une chaîne de caractères avec le bon sélecteur à l'intérieur comme dans la documentation.**

1. Dans la méthode `init`, créer une instance de `Swiper` en ciblant l'élément HTML désiré et en deuxième paramètre, en lui passant littéralement la variable globale d'options que nous venons de configurer (En utilisant les mêmes noms que la librairie Swiper, pas besoin de rien récrire).

`Avez-vous testé les trois carousels pour voir s'ils fonctionnaient tous? N'oubliez pas d'importer la librairie dans votre classe Carousel.`

<br><br><hr>

[Passer à l'étape suivante ▶](c.md)

<hr>

[◀ Retourner à l'étape précédente](a.md)
