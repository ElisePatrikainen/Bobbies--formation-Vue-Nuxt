# Props

Une prop est une propriété passée à un composant par son parent :

```html
<ImageComponent src="an/image/url" />
```

Elle peut être réactive, auquel cas la réactivité sera propagée au composant enfant.

```html
<ImageComponent :src="imageUrl" />
```

Elle doit aussi déclarée dans le composant enfant et peut ensuite être utilisée comme n'importe quelle propriété du composant.

```js
export default {
  props: ['src'],
  computed: {
    fullUrl() {
      return `${this.baseUrl}/${this.src}`
    }
  }
}
```

*Nb: on peut [typer nos props](https://vuejs.org/guide/typescript/options-api.html#typing-component-props) via Typescript*