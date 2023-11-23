




§§§ component based architecture :::





La solution : le SSR (Server Side Rendering) d'une SPA



Nuxt est donc initialement connu pour proposer une implémentation du SSR pour Vue.

Nb : on peut aussi faire du SSR sur Vue sans Nuxt (mais c'est beaucoup plus compliqué).


Nuxt propose donc plusieurs modes de rendu, déclinés à partir de ce concept de SSR : 
- SSR (Server Side Rendering) : le mode de rendu initial de Nuxt
- SSG (Static Site Generation) : permet de générer des pages statiques (HTML, CSS, JS) à l'avance, et de les servir depuis un CDN
- SWR (Stale While Revalidating) / ISR (Incremental Static Regeneration) : permet de servir une version cachée sur un CDN d'une page statique, et de la mettre à jour sur le CDN en arrière plan
- ESR (Edge Side Rendering) :  TODO : voir

Et une fonctionnalité expérimentale : Nuxt Islands, qui permet de rendre et mettre à jour un composant en SSR (donc sans charger de JS).

Nb : on peut aussi faire du CSR (Client Side Rendering, le mode de rendu standard des SPA) avec Nuxt.


Autres exemples de fonctionnalités d'optimisation des performances :
- Code splitting : découpage du code en un chunks par qui sera ensuite lazy-loadé
- Prefetching : préchargement des pages liées à la page courante
- Tree-shaking : suppression des dépendances inutilisées // TODO : voir plus en détails

Et de nombreuses fonctionnalités offertes par les modules : 
- Optimisation des images (Nuxt Image)
- Optimisation des fonts (Nuxt Font Loader)
- Optimisation du CSS (Nuxt Purge CSS / Nuxt Critters)



















Concernant la performance, Nuxt est initialement connu pour fournir une solution de SSR natif (Server Side Rendering) pour Vue, ce qui permet de générer le HTML côté serveur, et donc d'améliorer la performance de l'application (temps de chargement, SEO, etc).

Ce mode de rendu a été étoffé en pleinsd de categories : SSR, islands, rtc

// VITE ne pas oublier
Framewok JS : construire 
// Est-il possible


Vue.js, commonly referred to as Vue, is an open-source JavaScript framework for building user interfaces (UIs) and single-page applications (SPAs). It was created by Evan You and first released in 2014. Vue is designed to be incrementally adoptable, meaning you can use as much or as little of it as you need in your project, making it versatile and suitable for a wide range of applications.

Key features and concepts of Vue.js include:

    Declarative Rendering: Vue allows you to build your UI using a declarative approach, where you describe the desired state of your UI, and Vue takes care of updating the actual DOM to match that state. This simplifies UI development and makes it more predictable.

    Component-Based Architecture: Vue encourages the use of reusable components to build complex user interfaces. Each component encapsulates its own logic, template, and styles, making it easier to manage and maintain code.

    Vue Templates: Vue uses templates to define the structure of your UI, similar to HTML, but with additional features like directives (e.g., v-for, v-if) that enable data binding and dynamic updates.

    Two-Way Data Binding: Vue provides two-way data binding, which means that changes to the data (the model) automatically update the UI, and vice versa, simplifying the synchronization of data and UI elements.

    Directives: Vue's custom directives (e.g., v-bind, v-on) allow you to add special behavior to your templates, such as binding data to attributes or listening to events.

    Computed Properties: Vue allows you to define computed properties that are derived from your data, providing a way to perform complex calculations or transformations on your data in a more organized manner.

    Vue Router: Vue comes with its official routing library called Vue Router, which helps you build SPAs with client-side routing capabilities.

    Vuex: Vuex is Vue's official state management library, designed to manage application-level state and provide a centralized data store for your Vue components.

    Lifecycle Hooks: Vue provides a set of lifecycle hooks that allow you to execute code at specific points in the lifecycle of a Vue component, such as when it is created, mounted, updated, or destroyed.

    Community and Ecosystem: Vue has a vibrant and growing community, with a rich ecosystem of plugins and extensions that can extend its functionality and make it suitable for various use cases.

Vue.js has gained popularity for its simplicity, performance, and flexibility, making it a popular choice among developers for building interactive and dynamic web applications. It can be used in conjunction with other technologies and libraries to create robust web solutions.



Nuxt and performance : 

Nuxt.js is a popular JavaScript framework built on top of Vue.js that is designed to simplify the development of server-side-rendered (SSR) or statically generated web applications. When it comes to performance, Nuxt offers several features and optimizations to help improve the overall performance of your web applications:

1. Server-Side Rendering (SSR): SSR is a core feature of Nuxt.js. It enables your application to render pages on the server and send a fully-rendered HTML response to the client, which can significantly improve initial page load times and SEO.

2. Automatic Code Splitting: Nuxt automatically splits your JavaScript code into smaller chunks, also known as code splitting. This ensures that only the necessary JavaScript is loaded for each page, reducing the initial load time.

3. Async Data Fetching: Nuxt provides a `asyncData` method that allows you to fetch data asynchronously on the server side before rendering the page. This can help reduce client-side rendering time and improve perceived performance.

4. Static Site Generation (SSG): Nuxt supports static site generation, which allows you to generate static HTML files for your website. This can dramatically improve performance by serving pre-rendered pages directly from a CDN.

5. Lazy Loading: Nuxt has built-in support for lazy-loading images and components, which can help reduce the initial page load time by deferring the loading of non-essential assets.

6. Minification and Compression: Nuxt can automatically minify and compress your CSS and JavaScript files to reduce their size, improving load times.

7. Asset Optimization: Nuxt includes features for optimizing and loading assets like images and fonts efficiently.

8. Caching: Nuxt can be configured to enable caching at various levels, including server-side caching, client-side caching, and CDN caching, to further improve performance.

9. Critical CSS: Nuxt allows you to extract and inline critical CSS, which can help with the first paint and overall rendering speed.

10. PWA Support: Nuxt can be configured as a Progressive Web App (PWA), enabling offline access and improved performance for returning users.

11. Webpack Bundling: Nuxt uses Webpack under the hood, and you can customize the webpack configuration to fine-tune your application's performance optimizations.

12. Automatic Prefetching: Nuxt automatically adds `<link>` tags for prefetching linked pages, enhancing navigation speed.

To ensure optimal performance with Nuxt, it's essential to follow best practices in web development, such as optimizing images, using proper cache strategies, and keeping your JavaScript bundle sizes small. Additionally, you can use performance monitoring tools and techniques to identify and address specific performance bottlenecks in your application.