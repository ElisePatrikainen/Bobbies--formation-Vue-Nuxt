# Option API

Nb : on l'a déjà un peu vue (avec `data`).

<div class="max-h-[80%] overflow-auto">
```html {all|3-10|11-21|22-33}
<script lang="ts">
export default defineComponent({
  // interface du composant
  props: {
    book: {
      type: Object as PropType<Book>,
      required: true
    },
  },
  emits : ['update:book'],
  // local state
  data() {
    return {
      msg: 'Hello Vue'
    }
  },
  computed: {
    reversedMsg() {
      return this.msg.split('').reverse().join('')
    }
  },
  // events
  mounted() {
    console.log("component mounted")
  },
  watch: {
    book: {
      handler(newValue, oldValue) {
        console.log("book changed", newValue, oldValue)
      },
      deep: true
    }
  },
})

</script>
```
</div>