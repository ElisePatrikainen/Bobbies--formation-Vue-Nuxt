# Computed

Une propriété `computed` est une propriété dérivée depuis les propriétés Data.

```html
<script lang="ts">
export default {
    data() {
        return {
            msg: 'Hello Vue'
        }
    },
    computed: {
        reversedMsg() {
            return this.msg.split('').reverse().join('')
        }
    }
}
</script>

<template>
    {{ msg }} || {{ reversedMsg }}
</template>
```

Exercice : 

A partir d'un model de données d'un produit : 

afficher en interval de 1 seconde chaque produit
// peut etre ne pas mettre le setTimeout dans la premiere slide
afficher le nombre total de produits
// peut-être faire un gif et le mettre dans les slides ?