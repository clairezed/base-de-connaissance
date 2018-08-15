# Jamstack

## Ressources générales

- [Jekyll tips](http://jekyll.tips/) : tutoriaux, plugins et services s'intégrant à Jekyll
- [The new dynamic](https://www.thenewdynamic.org/) : plein d'articles sur les sites statiques, serverless, etc
- Snipcart [blog post](https://snipcart.com/blog/jamstack-clients-static-site-cms) about jamstack : plein d'exemple de service + argumentaire client
- [Awesome Static Hosting and CMS](https://github.com/b-long/awesome-static-hosting-and-cms)

## Exemples de workflows

### Utilisateurs

- MadeMistakes :
	- [How I’m Using Jekyll in 2016](https://mademistakes.com/articles/using-jekyll-2016/) : plugin jekyll-tagging-related_posts for related articles, improve build time : --incremental regeneration || Liquid Profiler, bundler, rsync task to deploy on own server, task to notify pingomatic, bing, google of changes, Jekyll-Assets plugin : cache busting and inlining assets + autoprefixer
	- [Repos github](https://github.com/mmistakes?tab=repositories)
	- [Repo github principal](https://github.com/mmistakes/made-mistakes-jekyll)
- Andrew Banchich :
	- [gitlab repo](https://gitlab.com/users/andrewbanchich/projects)
	- cf [political revolution repo](https://gitlab.com/political-revolution/political-revolution.gitlab.io/tree/master) : Jekyll, Sass, React, and Webpack.
- Boris Schapira :
	- [Un blog avec Jekyll et Codeship](https://borisschapira.com/2016/02/jekyll-codeship/), février 2016 : gemfile, i18n, vitesse lecture, moteur rendu markdown, précédent/suivant dans une meme categorie, node, gulp, browsersync, hooks github interfacé à caodeship (ac rspec), html-proofer, accessibilité : 2 chargements fonts, abrr-touch, algolia, instantClick pour impression vitesse, content security policy avec log des infractions
	- [Repo github](https://github.com/borisschapira/borisschapira.com)

## CMS

### Headless CMS - API driven

API driven : Stockage des données en cloud, cms pour éditer, accès aux données via API.

- [Contentful](https://www.contentful.com/)
- [Cockpit](https://getcockpit.com/) : open source version of the above solutions ?
- Strapi (open source)
- [Prismic.io](https://prismic.io)
- [GatherContent](https://gathercontent.com)

### Headless CMS - Git-backed

- [Netlify CMS](https://github.com/netlify/netlify-cms) -  open source, Git-backed
- [Forestry.io](https://forestry.io/) - Git-backed


### Headless CMS - A classer

- GraphCMS
- [Prose.io](http://prose.io/)
- [Cloud Cannon](http://cloudcannon.com/), a minima 25$/mois
- [Siteleaf](https://www.siteleaf.com/), with basic free plan
- [DatoCMS](www.datocms.com), really basic free plan

Alternatives : "ma meilleur expérience à ce jour c'est Nuxt.js. Donc c'est lui que je conseillerai, car il fait le SSR et peut générer aussi du statique"

### Flat File CMS

- [kirby](https://getkirby.com/) : env 20 €
- [statamic](https://statamic.com/) : 200$ !
- [lektor](https://www.getlektor.com)

## Par thématiques

### Performance

- [Optimiser les performances et la sécurité avec Cloudflare](https://medium.com/@JeremyRaffin/site-web-statique-optimis%C3%A9-avec-github-pages-partie-3-optimiser-les-performances-et-la-s%C3%A9curit-2be5413b7b17#.i1p2gx6nw)
- [Optimizing jekyll with gulp](http://savaslabs.com/2016/10/19/optimizing-jekyll-with-gulp.html), oct 2016
- [Performant Websites with Jekyll, Grunt, GitHub Pages, and CloudFlare](http://davidensinger.com/2015/01/performant-websites-with-jekyll-grunt-github-pages-and-cloudflare/), janv 2015
- [13 STEPS TO A FASTER JEKYLL WEBSITE](https://wiredcraft.com/blog/make-jekyll-fast/), mai 2016

### images

[jekyll-srcset](https://github.com/netlify/jekyll-srcset) plugin : Dead simple responsive images for jekyll

### Hosting

#### Github pages

- [deploy a directory as a git branch](https://github.com/X1011/git-directory-deploy), dec 2015
- [How To Use Any Jekyll Plugins on GitHub Pages with CircleCI](http://tongueroo.com/articles/how-to-use-any-jekyll-plugins-on-github-pages-with-circleci/), aout 2015
- [Jekyll on Github Pages with Plugins](http://sarahcassady.com/2015/07/17/jekyll-on-github-pages/), juill 2015
- [A simple way to use jekyll plugins on GitHub Pages](https://shitao.github.io/use-jekyll-plugin-on-gitpage/), juill 2015
- [How I moved my websites to Dropbox and GitHub](http://alexcican.com/post/guide-hosting-website-dropbox-github/)
- [Jekyll Plugins on GitHub](https://www.sitepoint.com/jekyll-plugins-github/), 2014
- [How to use Jekyll, Plugins and Sass on GitHub Pages](https://gist.github.com/WouterJ/4945964), 2013

#### Other host

- [5apps.com](https://5apps.com/deploy/home) : free for open source
- [Netlify](https://www.netlify.com/) : free for proto & experiment, pro plan free for open source
- [codeship](https://codeship.com) : *"A hosted Continuous Integration service that fits your needs"*.
- [alwaysdata](https://www.alwaysdata.com/fr/) (utilisé par Schapira)


## Plugins et services

- [Awesome Static Website Services](https://github.com/aharris88/awesome-static-website-services)

- [Staticman](https://staticman.net/) : système de commentaires statiques

> Want comments on your website? Add Disqus, Isso or Facebook comments. Want social integration? Add Twitter or Facebook’s JavaScript widget to your website. Want real-time data updating live on your website? Add a squirt of Firebase. Want search? Add Swiftype. Want to add live chat support? Olark is there. Heck, you can even add an entire store to a static website with Snipcart.

[Why Static Website Generators Are The Next Big Thing](https://www.smashingmagazine.com/2015/11/modern-static-website-generators-next-big-thing/)

- [Fork n go](http://jlord.us/forkngo/) : exemples (avec repo forkable) de sites statiques intéragissant avec des services tiers (google spreadsheet, mapbox, [sheetsee.js](http://jlord.us/sheetsee.js/), iftt...)

## Templating

### Templates

- [andrew banchich](https://github.com/andrewbanchich?tab=repositories) : portage jekyll de themes [html5up](https://html5up.net/)
	- [gems](https://rubygems.org/profiles/andrewbanchich)
	- [github repo](https://github.com/andrewbanchich?tab=repositories)
- [writer theme](http://preview.themeforest.net/item/writer-a-minimal-blog-for-jekyll/full_screen_preview/10562560) (Theme Forest)
- MadeMistakes : fait ses propres thèmes.
	- [Repos github](https://github.com/mmistakes?tab=repositories)
- [jekyll tips, templates](http://jekyll.tips/templates/)
- [liste templates cloudcannon](http://cloudcannon.com/announcements/2016/12/05/free-jekyll-templates/)

### Front-end framework integration

- Repo mêlant jekyll + webpack + vue : https://github.com/teleyinex/teleyinex.github.com

## Conference Bertrand Keller - Paris web

Nuxt : générateur à la jekyll / hugo, mais en view ? à regarder

Hugo : pas de plugin

théorie et idéologie : site statique en intégration continue. Si vous voulez passer à d'autres process, je vous laisse tout le dépôt, pas besoin de me recontacter.


**plugins jekyll à zieuter**
- plugin markdown développé par Ben Marker ?
- optionnal-front-matter : pas besoin de `---` pour créer du markdownify
- readme-index : le readme devient un index, qui peut pointer sur des resources, et voilà
- jekyll-title-from-heading : si on a pas de front-matter, le `#` devient la balise <title>
