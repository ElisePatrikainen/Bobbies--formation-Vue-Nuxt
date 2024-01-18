# SSR

Idée : 
- générer le HTML relatif à la première requête côté serveur, et envoyer ce HTML au client (ainsi on a une première réponse rapide)
- envoyer parallèlement le JS de la SPA au client, qui l'exécute
- une fois le JS prêt à être exécuté, on "connecte" ce JS avec le HTML préalablement envoyé : c'est l'hydratation
- l'application fonctionne ensuite comme une SPA standard
