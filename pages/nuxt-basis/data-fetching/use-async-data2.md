# Data fetching

Fonctionnement : 

```html
<script>
const { data, pending, error } = useAsyncData('xxx')
// TODO: voir pour le typage
</script>

<template>
<LoaderComponent v-if="pending" />
<ErrorComponent v-else-if="error" :error="error" />
<div v-else>{{ data }}</div>
```


Sans gestion d'etat, ce serait equivalent, sur la partie script, a :


```html
<script>
const data = ref()
const pending = ref(false)
const error = ref()

// todo: a tester
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