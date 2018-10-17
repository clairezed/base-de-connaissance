# Jamstack - outils

- [Jamstack - outils](#jamstack---outils)
  - [Gatsby](#gatsby)
    - [Avis](#avis)
    - [Avantages](#avantages)
  - [Nuxt](#nuxt)
  - [Grav](#grav)
  - [Phenomic](#phenomic)

## Gatsby

Gatsby + Contentful + Netlify et Algolia

### Avis

> Bon, j'ai essayé Gatsby ce week-end
Mon premier verdict: c'est hardcore
C'est pas standard du tout: je peux pas écrire mon `<head>` comme je veux, faut un plugin pour ça. Je peux pas insérer une feuille de style externe, faut l'importer. Je peux pas intégrer un tag d'image vers une image statique, faut un plugin pour générer des thumbnails à coup de GraphQL.
Ok, c'est super puissant, mais c'est clairement pas easy à prendre en main

> tout est composant React et tout passe par GraphQL si j’ai bien suivi

Les avantages compensent les inconvénients pour le moment, donc je continue et j'aime assez mais OMG comment la courbe d'apprentissage est velue

oui après ça booste et t’as une PWA qui va bien

### Avantages

- C'est du React. C'est un avantage parce que l'écosystème des composants React est énorme, donc il y a plein de trucs qui existent déjà que tu peux juste plugguer. Mais ça fait aussi parti de la courbe d'apprentissage compliqué
- Le live-reload est super réactif et marche très très bien
- Le système de cache incrémental semble plutot bien marcher, les temps de builds me semblent bons pour le moment (mais j'ai qu'un mini site pour le moment)
- Le plugin gatsby-image est assez impressionannt: il génère des thumbnails et adapte automatiquement avec `srcset` en fonction du device. il peut aussi générer des placeholder blurry et loader que quand ça rentre dans le viewport. En terme d'optimisation des images, tout les trucs super compliqués semblent déjà intégrés
- J'ai toujours trouvé la gestion de data complexe avec Jekyll et Middleman (tu store des yaml quelque part et ensuite tu loope dessus pour trouver ce que tu veux). Ici, tu as du graphQL pour selectionner uniquement ce que tu veux avec plein de filtres sympas. Encore une fois: courbe d'apprentissage costaud, faut comprendre graphQL. C'est pas super bien documenté, mais y a un live-editor qui permet de tester ses queries et d'explorer les data à la main qui est chouette

## Nuxt

très bonne solution pour de l’application avec rendu SSR

## Grav

https://getgrav.org/

## Phenomic

Phenomic is different from other SSG by allowing you to pick the technologies, libraries, frameworks of your choice and build your website with it. You can decide the renderer you want to use (like React), your bundler (like Webpack) and so on.

https://phenomic.io/