# Semaine 03 - Ma première composante

## `ÉTAPE 1` - La classe Carousel

La première étape est de se créer une classe Carousel et d'y ajouter le code nécessaire pour qu'elle fonctionne.

### À faire avant de commencer

1. Est-ce que Swiper est installé dans votre projet?
1. Assurez-vous également que les styles de `Swiper` soient importé dans le `main.scss`. On veut charger le `swiper-bundle` seulement qui contient tout ce dont nous avons besoin.

### Création de la classe Carousel

1. Dans un nouveau fichier nommé `Carousel.js` ajouter le code nécessaire pour avoir une classe fonctionnelle  (constructor et init)
1. **Il ne faut pas** se créer de nouvelle instance à ce stade-ci. 
1. Mettre un `console.log` dans le init : "Initialisation de ma composante Carousel"

Le `console.log` ne fonctionne pas pour l'instant, c'est normal. Nous allons maintenant nous créer une nouvelle instance dans notre `Main`.

Pour respecter l'approche par composante dans TimTools, nous utiliserons les attributs data pour sélectionner nos composantes. En appliquant un `data-component` sur tous les éléments qui doivent s'activer dans notre JavaScript, le code sera facilement réutilisable. La valeur de cet attribut `data-component` sera celui de la composante qu'on voudra activer. Ici, ça sera `Carousel`.

### Ajout de la boucle pour créer les nouveaux carousels

1. Ajouter l'attribut `data-component="Carousel"` sur tout les éléments HTML qui représentent vos carousels `('.swiper')`
1. Construisez la même structure que d'habitude de votre classe Main (incluant son instanciation comme il s'agit de la classe principale).1. Dans le init de votre classe `Main` ajouter une variable locale `components`
1. Votre variable `components` devra contenir une référence à tous les éléments HTML qui ont l'arribut `data-component="Carousel"`
1. Faire une boucle `for` qui boucle dans tous les éléments HTML que contient votre variable `components`
   1. Assigner l'élément du tableau à la position `[i]` , à une variable locale nommé `element`. Si vous utilisez le snippet, c'est possiblement partiellement fait 😎;
   1. Faire une nouvelle instance de votre carousel (`new`)
1. Votre `console.log` du `Carousel` devrait maintenant s'afficher 3 fois (parce que vous en avez fait 3).

Si ce n'est pas le cas faite des `console.log` dans de votre init pour identifier et régler le problème.
<br><br><hr>

[Passer à l'étape suivante ▶](b.md)

<hr>

[◀ Retourner à l'intro](../readme.md)
