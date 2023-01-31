---
title: Expérimentation - Nuxt.js & Vue.js
type: page
description: Création d'un portfolio avec Nuxt.js et Vue.js. Expérimentation et découverte.
topic: experimentation, nuxt
---

# Expérimentation

Dans le cadre de mes études à la HEIG-VD, j'ai eu l'occasion de développer mon [portfolio](https://portfolio-plk6.onrender.com/about) en ligne. Au lieu de choisir un CMS classique comme Wordpress, j'ai décidé de me lancer dans l'utilisation de Nuxt.JS et Vue.JS. Bien que j'aie déjà rencontré Vue.js dans mes cours, Nuxt.JS était une nouvelle technologie pour moi.

## Nuxt.js

Nuxt.js est un framework JavaScript basé sur Vue.js qui vise à faciliter le développement d'applications web et d'applications de rendu côté serveur (SSR, Server-side Rendering). Il offre une structure claire et une organisation efficace pour les développeurs, ce qui en fait un choix populaire pour les projets de grande envergure.

## Mise en place de Nuxt.js

Le démarrage avec Nuxt.js a présenté certaines difficultés, notamment avec la version de nodejs installée sur mon ordinateur. Pour remédier à ce problème, j'ai installé [nvm](https://www.freecodecamp.org/news/node-version-manager-nvm-install-guide/) pour gérer plusieurs versions de node. Une fois la bonne version en place, j'ai commencé la création de mes composants pour le portfolio.

Cependant, le manque de temps a rapidement posé problème. Pour gagner du temps, j'ai décidé d'utiliser un template déjà existant (https://github.com/realstoman/nuxtjs-tailwindcss-portfolio) pour construire mon portfolio.

Je n'ai pas compris tout de suite le fonctionnement du projet. Je ne savais pas où se trouvaient les fichiers et les données. 

Puis, après quelques recherches et réflexions, j'ai pu enfin m'y retrouver 

### Les données
Les données où se trouvent toutes les informations (textes, liens vers images, etc.) se trouvent dans le fichier "store/index.js". 
Il s'agit d'un fichier Vuex. Ce fichier n'est pas obligatoire mais est une manière de faire. 

Selon [la documentation](https://nuxtjs.org/docs/directory-structure/store/), si le répertoire store existe avec un fichier dedans, il va importer Vuex et ajouter les options de store dans l'instance racine de Vue.

Ce qui fait que tous les fichier js dans le répertoire "store" sera transformé en "namespaced module".
J'ai donc dans ce fichier index.js plusieurs propriétés, dont les projets, les textes de la page "About me", etc. 

### Components
Il y a ensuite les composants, dans le répertoire "Components". Ce sont tous les éléments réutilisables, ou affichables dans des modals. 
On y retrouve notamment:
- La page about avec les différentes sections. Les textes sont d'ailleurs récupérés depuis le fichier "store/index.js".
- La page "Contact me" avec le formulaire en composant séparé
- Les projets
- Les éléments réutilisables (boutons)
- Les éléments partagés comme le footer et le header qui se trouvent sur chaque page. 

### Layout
Le portfolio est donc basé sur un layout (se trouvant dans "layouts/default.vue"). Celui-ci importe l'en-tête et le footer et définit les transitions entre les pages.
A chaque changement de page, ce n'est que le composant central qui change, ce qui donne une meilleur expérience utilisateur (à mon avis).

### Pages

Nous avons ensuite le répertoires "pages". Il s'agit de toutes les pages existantes. Chacune d'elle va ensuite récupérer les composants dans le répertoire "components", et les données se situant dans le store. 


# Conclusion

En conclusion, la mise en place de Nuxt.js pour le développement de mon portfolio était intéressant. Bien que j'aie rencontré des obstacles, j'ai appris énormément sur ce framework JavaScript et sur la manière de travailler avec Vue.js.
La prise en main est plutôt facile. Ce qui prend du temps est la mise en place de chacune des parties (store, components, layout...). Mais dans des projets, ce temps pris au début fera gagner énormément de temps par la suite.

Non seulement il permettra d'éviter de la redondance de données, mais donnera également une structure beaucoup plus précise et une cohérence dans l'identité visuelle. 



# Sources
[Portfolio template](https://github.com/realstoman/nuxtjs-tailwindcss-portfolio)

[Mon portfolio](https://portfolio-plk6.onrender.com/contact)

[Nuxt.js](https://nuxt.com/)