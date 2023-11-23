# Vue

Vue est aussi component based, permettant d'encapsuler la logique et le template.


```html
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

*Nb : les SFC nous permettrons évidemment de diviser nos composants en fichiers.*