# Composables

Le [dossier composables](https://nuxt.com/docs/guide/directory-structure/composables) contient les composants de l'application :
- auto importés

Ex:

```html
| components/
--| useProducts.ts
```

```html
<script setup lang="ts">
const products = useProducts()
</script>

```

*Nb : en cas d'export par défaut, le nom du composable est [déduit du nom du fichier](https://nuxt.com/docs/guide/directory-structure/composables#usage)*