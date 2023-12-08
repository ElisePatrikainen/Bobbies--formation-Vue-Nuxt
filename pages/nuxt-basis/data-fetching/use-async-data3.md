# $fetch vs useFetch

`useFetch` : 

```html
<script>
const { data, pending, error } = useFetch('xxx')
</script>

<template>
<LoaderComponent v-if="pending" />
<ErrorComponent v-else-if="error" :error="error" />
<div v-else>{{ data }}</div>
```
