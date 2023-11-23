# Vue

Plus concrètement, voici à quoi ressemblerait une application Vue minimaliste :

```html
<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>

<div id="app">{{ message }}</div>

<script>
  const { createApp, ref } = Vue

  createApp({
    setup() {
      const message = ref('Hello vue!')
      return {
        message
      }
    }
  }).mount('#app')
</script>
```

*Nb : On utilisera bien-sûr quelque chose de plus pratique pour construire nos applications (un bundler, Vite, et une syntaxe adaptée avec les SFC, Single File Components).*