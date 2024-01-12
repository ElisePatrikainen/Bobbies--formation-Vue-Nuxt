# Middleware

Définition : Fonction exécutée avant la navigation vers une page (authentification, tracking...). Elle peut en particulier bloquer la navigation.

```js
// middleware/admin.js
export default defineNuxtRouteMiddleware((to, from) => {
  if (to.path.includes('admin')) {
    const user = useUser()
    if (!user) {
      return navigateTo('/login')
    } else if (!user.isAdmin) {
      const useNotification = useNotifications()
      useNotification.notifyError('You are not allowed to access this page')
      return abortNavigation()
    }
  }
})
```

Ils peuvent bloquer la navigation en retournant 