# Notes :

- `useAsyncData` et `useFetch` ne peuvent être appelés que dans des setup function, plugin, ou middlewares
- avec du SSR, `useAsyncData` et `useFetch` permettent d'éviter de fetch les données deux fois (côté client et serveur)