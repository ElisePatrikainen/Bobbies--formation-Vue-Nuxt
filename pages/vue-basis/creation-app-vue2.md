# L'instance Vue

C'est aussi la première instance qui initie l'application la "monte" sur le DOM.

```html {all|3,12,17,19}
<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>

<div id="app"></div>

<script>
  const { createApp } = Vue

  const helloComponent = Vue.defineComponent({
    template: `<span>Hello Vue from a component !</span>`
  })

  const app = createApp({
    components: {
      helloComponent
    },
    template: `<hello-component />`
  })

  app.mount('#app')
  </script>

```