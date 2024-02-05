# Semaine 03 - Ma première composante

## `ÉTAPE 4` - Personnaliser nos carousels

Vous avez maintenant une base de carousel fonctionelle. Cependant, tous vos carousels sont actuellement identiques au niveau des paramètres et fonctionnalités.

Nous allons utiliser les attributs data que nous mettrons sur nos composantes (ceux qui ont le data-component) afin d'ajouter des variations en tout genre.

### Modifications

1. Sur les deuxième et troisième carousels, ajouter un attribut data `data-split` sur le même élément HTML que la composante.

Avec la présence de cet attribut, sur un grand écran, nous aurons 2 diapositive de visible à la fois alors que lorsque la largeur de l'écran sera égal ou inférieur à 768px, nous passerons à une seule diapositive visible.

1. Créer une méthode `setOptions`
1. Dans le `init`, avant la création du `Swiper`, appeller la méthode `setOptions()`. Cette dernière sera appellée et modifiera l'**objet global options** pour chaque instance de `Carousel`.
1. On retourne dans `setOptions`

   1. Vérifiez la présence de l'attribut `data-split` sur la composante (rappel, `this.element`représente l'élément HTML pour chacune des instances. (voir aide-mémoire)
      - Ajouter à votre variable globale option une propriété `breakpoints` pour qu'à 768px et plus, il y ait `2.5` diapositives par vue (`this.options.breakpoints = {}`)

### Propriétés à la pièce

Après avoir fait une variante, nous aimerions faire bouger le carousel automatiquement lorsque notre élément HTML contient l'attribut `data-autoplay`.

1. Ajouter l'attribut `data-autoplay`, sans aucune valeur, sur le premier carousel
   1. Faire une condition qui valide la présence de `autoplay` dans le dataset.
      - Si l'attribut existe, modifiez la valeur de `this.options.autoplay` en lui assignant un object qui tient compte des paramètres `Swiper` suivants :
        - délai de 5000
        - une pause lors du survol
        - Enlever l'option de désactivation lors d'interaction

Ajoutons une autre propriété modifiable à la pièce, soit `data-loop`

1. Ajouter l'attribut `data-loop`, avec la valeur `true`, sur le premier carousel
1. Faire une condition qui valide la présence de `loop` dans le dataset.
   - Si l'attribut existe, modifiez la valeur de `this.options.loop` pour `true`

Terminons les propriétés à la pièce avec une dernière. Le nom de l'attribut doit être `data-slides`. Voici ce que la propriété devrait changer.

- Elle devra permettre de modifier le paramètre `slidesPerView` de Swiper.
- On doit lui passer une valeur pour qu'elle fonctionne. Selon la doc. de Swiper :
   - soit on lui passe `'auto'` (chaîne de caractère)
   - soit on lui passe un nombre entier ou décimal
1. Si l'attribut est présent, on s'assure qu'il contienne une valeur afin de modifier `this.options.slidesPerView` sinon, on utilise la technique du " OR " `||` afin d'assigner à ce paramètre la valeur par défaut que nous avions dans les options. ` = this.options.slidesPerView`.
2. Testez plusieurs valeurs de nombres entiers et à décimale (3, 2.5, etc.) Terminez le tout sur ce qui est demandé dans le fichier .html!
     <br><br><hr>

[Passer à l'étape suivante ▶](e.md)

<hr>

[◀ Retourner à l'étape précédente](c.md)
