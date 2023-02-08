# Semaine 03 - Ma première composante

## `ÉTAPE 4` - Personnaliser nos carousels

Vous avez maintenant une base de carousel fonctionelle. Cependant, tous vos carousels seront identiques au niveau des paramètres et fonctionnalités.

Nous allons créer une `variante` qui changera visuellement le rendu du carousel. Nous vérifierons aussi la présence de certains attributs data qui modifieront plutôt que quelques paramètres.

### Variantes

1. Sur le deuxième et troisième carousel, ajouter un attribut data `data-variant` sur le même élément HTML que la componsante avec la valeur split.
1. Créer une méthode `setOptions`
1. Dans le `init`, avant la création du `Swiper`, appeller la méthode `setOptions()`
1. On retourne dans `setOptions`

   1. Créer une variable globale `variant` qui récupère le data-attribut variant
   1. Ajouter une condition qui regarde si la valeur égale `"split"`
      - Ajouter une options breakpoints(768) pour avoir `2.5` diapositives par vue (`this.options.breakpoints = {}`)

### Propriétés à la pièce

Après avoir fait une variante, nous aimerions faire bouger le carousel automatiquement lorsque notre élément HTML contient l'attribut `data-autoplay`

1. Ajouter l'attribut `data-autoplay`, sans aucune valeur, sur le premier carousel
   1. Faire une condition qui valide la présence de `autoplay` dans le dataset (voir aide-mémoire)
      - Si l'attribut existe, modifiez la valeur de `this.options.autoplay` en lui assignant un object qui tient compte des paramètres `Swiper` suivants :
        - délai de 5000
        - une pause lors du survol
        - Enlever l'option de desactivation lors d'intéraction

Ajoutons une deuxième propriété modifiable à la pièce, soit `data-loop`

1. Ajouter l'attribut `data-loop`, avec la valeur `true`, sur le premier carousel
1. Faire une condition qui valide la présence de `loop` dans le dataset (voir aide-mémoire)
   - Si l'attribut existe, modifiez la valeur de `this.options.loop` pour `true`
     <br><br><hr>

[Passer à l'étape suivante ▶](e.md)

<hr>

[◀ Retourner à l'étape précédente](c.md)
