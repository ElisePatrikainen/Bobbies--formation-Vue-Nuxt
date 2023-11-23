# Data

Représente le data-model du composant.

// Revoir pourquoi c'est une fonction.

// TODO: mettre les composants en Camel/Kebab Case (voir la différence)

On l'a déjà vue.

```html
<script lang="ts">
export default {
    data() {
        return {
            msg: 'Hello Vue'
        }
    }
}
</script>

<template>
    {{ msg }}
</template>
```