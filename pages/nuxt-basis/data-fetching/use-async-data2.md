# $fetch vs useFetch

`$fetch` : 

```html
<script>
const data = ref()
const pending = ref(false)
const error = ref()

pending.value = true;
try {
    data.value = await fetch('xxx')
}
</script>

<template>
<LoaderComponent v-if="pending" />
<ErrorComponent v-else-if="error" :error="error" />
<div v-else>{{ data }}</div>
```