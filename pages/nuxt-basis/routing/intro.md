# Routing

*Nb: les fonctionalités de routing dans Nuxt sont basées sur le [Vue Router](https://router.vuejs.org/)*

- [File based routing](https://nuxt.com/docs/getting-started/routing) : syntaxe  `[param]` dans le nom du fichier
- Liens : built-in component [`<NuxtLink>`](https://nuxt.com/docs/api/components/nuxt-link)
- Accès au router via les composables [`useRoute`](https://nuxt.com/docs/api/composables/use-route) (informations sur la route courante) et [`useRouter`](https://nuxt.com/docs/api/composables/use-router) (navigation programmatique, récupération des paramètres...), ainsi que via les propriétés `$route` et `$router` [dans les templates](https://router.vuejs.org/guide/advanced/composition-api.html#Accessing-the-Router-and-current-Route-inside-setup)