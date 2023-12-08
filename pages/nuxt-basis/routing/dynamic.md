# Dynamic routing


- [File based routing](https://nuxt.com/docs/getting-started/routing) : syntaxe  `[param]` dans le nom du fichier
- Récupération des paramètres de la route courante (segments, query params...) : via le composable [`useRoute`](https://nuxt.com/docs/api/composables/use-route)
```js
const { params, query } = useRoute()
```