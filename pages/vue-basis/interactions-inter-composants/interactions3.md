# Events

Vue permet de déclarer et émettre des événements dans nos composants.

```js
export default {
  emits: ['submit'],
  methods: {
    submitForm(email, password) {
      this.$emit('submit', { email, password })
    }
  }
}
```

Ils peuvent être écoutés par le composant parent de la même manière que les événements natifs.

```html
<FormComponent @submit="saveForm" />
```

*Nb: on peut [typer nos évènement](https://vuejs.org/guide/typescript/composition-api.html#typing-component-emits) mais on le verra plus en détail avec l'API de composition.*