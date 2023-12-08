# $fetch vs useAsyncData vs useFetch

On recommande donc d'utiliser :
- useFetch (ou `useAsyncData`) pour le fetchd es données nécessaires au rendu d'un composant
- `$fetch` pour le fetch de données suite à des intéractions utilisateur (ex: click sur un bouton)
