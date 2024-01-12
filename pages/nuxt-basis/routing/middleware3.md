# Middleware

3 types de middleware :
- global : `middleware-name.global.ts`
- nommé : `middleware-name.ts` =/ appelé dans la page
- inline : défini dans la page

```js
<script setup lang="ts">
definePageMeta({
  middleware: [
    function (to, from) {
      // Custom inline middleware
    },
    'auth',
  ],
});
</script>
```