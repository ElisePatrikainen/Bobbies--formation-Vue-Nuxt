# DefineProps et EmitEvents

Différences :
- ce sont des fonctions avec un retour
```js
const props = defineProps({
  product: Product
})
console.log(props.product)
// Nb: 'product' dans le template
```
```
```js
const emit = defineEmits(['add-product'])
emit('add-product', product)
```

- on peut les [typer](https://vuejs.org/guide/typescript/composition-api.html#typing-component-props) avec des notations raccourcies (=> usage facilité d'interfaces)
- il existe aussi le macro [`withDefaults`](https://vuejs.org/api/sfc-script-setup.html#default-props-values-when-using-type-declaration) pour définir les valeurs des props par défaut 