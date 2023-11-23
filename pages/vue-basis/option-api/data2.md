# Data

Les Data sont réactives : si on les change, le DOM est automatiquement mis à jour.

// Toto : plutot mettre un exemple ou la data est mutee dans le composant
```html
<script lang="ts">
export default {
    data() {
        return {
            msg: 'Hello Vue'
        }
    },
    mounted() {
        setTimeout(() => {
            this.msg = '[Updated message] How are you?'
        }, 2000)
    }
}
</script>

<template>
    {{ msg }}
</template>
```

Nb: `mounted` est un hook qui est appelé quand le composant est monté dans le DOM, on le verra d'ici quelques minutes.