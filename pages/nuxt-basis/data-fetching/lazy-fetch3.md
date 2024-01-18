# useLazyAsyncData, useLazyFetch

Nb : `useLazy...` est un alias de `use...` avec l'option `{ lazy: true }`.

```ts
const { pending, data: count } = await useLazyAsyncData('count', () => $fetch('/api/count'))
```
équivaut à :
```ts
const { pending, data: count } = await useAsyncData('count', () => $fetch('/api/count'), { lazy: true })
```