# Components

Le [dossier components](https://nuxt.com/docs/guide/directory-structure/components) contient les composants de l'application :
- auto importés
- peuvent être lazy loaded (préfixe `Lazy`)

Ex:

```html
| components/
--| ProductList.vue
```

```html
<template>
  <div>
    <ProductList />
    <LazyProductList />
  </div>
</template>

```