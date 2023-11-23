# Syntaxe du template

Affichage des données : 
- interpolation `{{ }}`
```html
<span>Bonjour {{ firstName }}</span>
```

- v-bind `:` pour les attributs HTML (et plus largement pour les props, mais on verra ça plus tard)
```html
<img :src="imageSrc" />
```

Réactions aux événements utilisateurs : 
- v-on `@` pour les événements HTML (et plus largement pour les événements customs, cf plus tard)
```html
<button @click="save">Enregistrer</button>
```