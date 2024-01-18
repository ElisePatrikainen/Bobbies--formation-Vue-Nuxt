# useLazyAsyncData, useLazyFetch

Nb 2 : l'option `lazy` n'a aucun impact sur le comportement de `useAsyncData` et `useFetch` dans le cas d'un rendu côté serveur.

Si on souhaite ne pas effectuer le fetch côté serveur, il faut utiliser l'option `{ server : false }`.
