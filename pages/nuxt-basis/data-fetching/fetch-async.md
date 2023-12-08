# useAsyncData vs useFetch

` useFetch` est basé sur `$fetch` et `useAsyncData` : 

```ts
const { data, pending, error, refresh } = await useAsyncData(
  'products',
  () => $fetch('api/products')
)
```

```ts
const { data, pending, error, refresh } = await useFetch(`api/products`)
```