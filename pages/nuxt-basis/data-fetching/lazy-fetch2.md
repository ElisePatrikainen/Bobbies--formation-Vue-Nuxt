# useLazyAsyncData, useLazyFetch

Intérêt de bloquer la navigation : 
- SEO dans le cas SSR
- UI dans le cas SPA

Si on souhaite ne pas bloquer la navigation pendant le chargement des données (exemple : données non essentielles), on peut utiliser `useLazyAsyncData` ou `useLazyFetch`.

```ts
const { pending, data: count } = await useLazyAsyncData('count', () => $fetch('/api/count'))
```
