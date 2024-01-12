# Application de synthèse

Implémenter la structure d'une authentification :
- créer une page de sign-in/login, depuis laquelle on récupère un token (depuis [fakeStoreApi](https://fakestoreapi.com/docs))
- stocker les informations utilisateur (ici le token) au runtime ou, si possible, en cookie ([hint](https://nuxt.com/docs/api/composables/use-cookied))
- indiquer dans le header que l'on est loggé
- créer une page "profil" à laquelle on n'accède seulement en étant authentifié, ajouter un lien dans le header
- permettre l'édition du profil de l'utilisateur à partir de cette page (vers [fakeStoreApi](https://fakestoreapi.com/docs)). L'appel devra :
    - avoir le token passé en header `authorisation`
    - déconnecter l'utilisateur et le rediriger vers la page de login si l'API retourne une erreur 401 (non autorisé)