# Les Single File Components

`hello-component.vue`

```html {all|1-9|2-8|11-13|12|15-19|15}
<script>
export default {
  data() {
    return {
      message: 'Hello Vue from SFC!'
    }
  }
}
</script>

<template>
  <h1>{{ message }}</h1>
</template>

<style scoped>
h1 {
  color: pink;
}
</style>
```