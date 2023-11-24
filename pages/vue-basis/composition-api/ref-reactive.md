# Ref et reactive

Ces deux fonctions permettent de rendre une variable (primitive ou objet) réactive.

Différence : 
- ref() : rend une variable réactive en la 'wrappant' dans un objet 
    - nécessaire pour les variables primitives
    - permet d'accéder à la valeur de la variable via `.value`
- reactive() : rend un objet réactif
    - ne fonctionne que pour les objets
    - permet d'accéder à la valeur de la variable directement

Nb: on peut aussi n'utiliser que ref() pour rendre un objet réactif :
    - meilleure lisibilité (on sait, grâce au `.value`, que la variable est réactive)
    - une seule guideline
