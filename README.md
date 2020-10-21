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

<strong>v-show</strong> peut sembler très similaire à la directive  v-if  ; pourtant, les deux ne sont pas interchangeables.  v-show  est généralement utilisée dans le but de contrôler la visibilité d'un élément faisant l'objet d'une permutation (toggle, en anglais) fréquente. La principale différence entre les deux directives est que  v-show  permute la visibilité de l'élément HTML grâce au CSS, alors que v-if supprime complètement l'élément du DOM.

### Définissez des attributs HTML de façon dynamique

Vous serez très souvent tenté d'utiliser une propriété  data  pour définir l'attribut d'un élément, plutôt que de le coder en dur. Il y a justement une directive faite exprès : la directive  <strong>v-bind</strong>. C'est le cas, par exemple, lorsque vous effectuez une requête pour récupérer des données auprès d'une API et que vous avez besoin de renvoyer des données en fonction de ce qui est retourné. 
```vue.js
<div id="app">
    <ul>
        <li v-for="item in apiResponse">
            <a v-bind:href="item.url">{{ item.name }}</a>
        </li>
    </ul>
</div>

<script>
    const app = new Vue({
        el: '#app',
        data: {
            apiResponse: [
                { name: 'GitHub', url: '<https://www.github.com>' },
                { name: 'Twitter', url: '<https://www.twitter.com>' },
                { name: 'Netlify', url: '<https://www.netlify.com>' }
            ]
        }
    })
</script>
```


<i>La directive  v-bind  est couramment utilisée via son abréviation «   :  ». En d'autres termes, au lieu d'écrire  v-bind:href="item.url", on écrit généralement plutôt  :href="item.url".</i>


### Ecoutez des événements

Lorsque on souhaite écouter certains événements sur un élément, Vue nous facilite la tâche avec la directive   v-on.
```vue.js
<div id="app">
    <button v-on:click="alert('Bonjour')">Cliquez ici !</button>
</div>```

Attention : 
<i>La directive  <b>v-on</b>  est couramment utilisée via son abréviation «  @  ». Au lieu d'écrire  v-on:click="alert('Bonjour')", on écrit généralement plutôt   @click="alert('Bonjour')".</i>





