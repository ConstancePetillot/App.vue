# App.vue

## S'entrainer avec Vue.js en créant une application pour un coffee shop.

### Les données réactives
En cas de modification de l'une de ces valeurs, la liste s'adaptera en conséquence. En d'autres termes, le data store a fait en sorte que tout soit réactif pour qu'on n'ait plus à intervenir !                                                     
![enter image description here](https://zupimages.net/up/20/43/yjb9.png)

### Les propriétés calculées
Les propriétés calculées (computed properties) nous permettent de définir une valeur réutilisable qui est mise à jour en fonction d'autres propriétés  data. Comme pour la propriété  data, nous commençons par ajouter une propriété  calculée  qui utilise un objet pour définir les propriétés que nous voulons. Cependant, contrairement à la propriété  data, chaque propriété calculée doit être une fonction retournant une valeur. En effet, elle effectue des calculs et retourne le résultat souhaité.
![enter image description here](https://zupimages.net/up/20/43/23v7.png)

### Les directives
Les directives nous fournissent un moyen standard pour résoudre les problèmes courants. Elles sont particulièrement puissantes et écrites de manière sémantique, afin que le code soit facile à comprendre. Les directives ressemblent à des attributs HTML avec une différence principale : elles disposent toutes du préfixe  v-. Voici quelques directives courantes que vous rencontrerez dans les applications Vue : 

- v-if, v-else-if, v-else
- v-show
- v-for
- v-bind
- v-on
- v-model
