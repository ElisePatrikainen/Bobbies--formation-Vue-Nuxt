# Application 2

Implémenter les spécifications suivantes :
- gérer le chargement côté client de la page home (sans bloquer la navigation), optimiser la payload, ajouter un bouton permettant de reactualiser la liste des produits
- n'afficher la page produit que lorsqu'elle est chargée (afficher un loader pendant le temps de chargement) 
- ajouter un appel sur cette page (note : cet appel, qui a un faible interet SEO et dont le display se trouve en bas de page, n'est pas utile au premier rendu)
- ajouter au panier l'information du montant de la livraison en se servant d'un endpoint créé avec l'API Nuxt 
- ajouter un cache à l'appel Home, qui sera revalidé dans le cas où il date de plus de 10 minutes
- conserver temporairement l'utilisateur dans le cache, et faire une 'optimistic update' dessus avec le POST qu'on a fait precedemment