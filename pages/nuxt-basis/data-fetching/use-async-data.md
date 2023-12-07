# Data fetching

On peut utiliser avec Nuxt n'importe quelle solution de data-fetching : fetch, axios, ky...

Mais Nuxt propose sa propre solution, qui a en particulier l'intérêt de :
- proposer une gestion de l'état serveur
- $etre optimisée pour le SSR (on en parlera après). 

Voir le poids de cette solution (pour comparaison)

La solution : un composable, `use-async-data` qui est basé sur ohmyfetch (à vérifier), solution JS optimisées pour SSR.

