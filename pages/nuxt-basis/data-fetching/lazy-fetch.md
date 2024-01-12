# useLazyAsyncData, useLazyFetch

Par défaut, `useFetch` bloque la navigation tant que la requête n'est pas terminée (basé sur `suspense`).

Utilisé avec `<NuxtLoadingIndicator />`, cela permet d'afficher un indicateur de chargement pendant la navigation.

```ts
const { data, pending, error, refresh } = await useFetch(`api/products`)
```

```html
<template>
  <NuxtLoadingIndicator />
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
</template>
```