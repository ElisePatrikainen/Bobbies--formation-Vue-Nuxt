# L'instance Vue

Comme nous l'avons vu précédemment, une application Vue sera constituée de l'encapsulation d'instances de Vue, chacune correspondant à un **composant**.

```html {all|8-10,16}
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