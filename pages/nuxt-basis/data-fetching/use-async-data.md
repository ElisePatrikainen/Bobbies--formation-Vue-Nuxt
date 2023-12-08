# Data fetching

On peut utiliser avec Nuxt n'importe quelle solution de data-fetching : fetch, axios, ky...

Mais Nuxt propose sa propre solution, qui a en particulier l'intérêt de :
- proposer une gestion de l'état serveur
- être optimisée pour le SSR (on en parlera après). 

La solution : 
- [`$fetch`](https://nuxt.com/docs/api/utils/dollarfetch), un helper basé sur [`ofetch`](https://github.com/unjs/ofetch)
- deux composables, [`useAsyncData`](https://nuxt.com/docs/api/composables/use-async-data) et [`useFetch`](https://nuxt.com/docs/api/composables/use-fetch)

