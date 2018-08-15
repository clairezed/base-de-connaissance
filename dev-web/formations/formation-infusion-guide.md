# Formation infusion

-> Notes à la volée prise durant une formation-infusion avec David, débutée le 7 juin 2018.

[Repo du projet](https://github.com/clairezed/guide-conso)

## Faire du web côté client ?

1/ SPA sans body

- 3 allers-retours (charger le html, puis le js, puis les data)
- latence de 1 à 10 secondes (en moyenne 2 à 3)

2/ SPA avec body

- dès le premier AR, on donne à voir du html, puis ensuite js et data sont chargés (et viennent se rajouter au html déjà produit)
- duplication de code entre client et serveur

3/ Langages de templating

- à la [mustache](https://mustache.github.io/), etc
- vise à réutiliser les mêmes briques côté client et côté serveur, mais sous forme de `string UI`
- amène à ré-injecter des données dans le html (souvent sous forme de plein de `data-attributes`), pour réussir à recoupler l'ui avec les données

4/ Framework à la react

Ressources complémentaires :

- [Client-side Web Application Engineering](https://github.com/DavidBruant/contenu-formations-web/blob/master/client-side%20web%20application%20engineering.md), contenu formation David


## Head et inclusion de fichiers

- [Better defaults](https://github.com/DavidBruant/better-defaults)
- [Spec balise script](https://html.spec.whatwg.org/multipage/scripting.html#the-script-element)
- Liens vers des CDN : `crossorigin="anonymous"` + `<meta name="referrer" content="same-origin">` (les sites externes ne reçoivent pas `referer` dans le `head`) -> comme ça, les CDN peuvent pas pister
- utiliser `defer` de preference
- `async` possible quand on charge qqch qui touche pas le dom

## Serveur web express

```
npm init
npm install serve --save-dev
```
Permet d'installer la dépendance dans les `devDependencies` (les packages installés sont installés sans leurs devDependencies)

(keywords : permet de trouver package sur npm, aide à la recherche)

Pour lancer le serveur :

```
./node_modules/.bin/serve
```

Pour enregistrer une commande plus simple à lancer, éditer `package.json` :
```json
"scripts": {
    "start": "serve",
    "test": "echo \"Error: no test specified\" && exit 1"
  },
```

Cf [Dataviz finances gironde pakage.json](https://github.com/DavidBruant/dataviz-finances-gironde/blob/master/package.json)


## Vrac

word2vec

## Doc AppScript
- [Le script](https://script.google.com/macros/d/1n2Wr960_wShq9aiPWtgYCRG64Yfts6bhV-33NKUJkYeM3Y_4LC2uH7UO/edit?uiv=2&mid=ACjPJvFE2j4M-qwvBQVKm_yLz0uvn-0vFefOAASdDDmXolMbkdq9-szJg4dEcj_lVuE89hiftEdFeFpQhYdIuNu1nf85P4ukmldekQm-OR_RM5I0oJFd7zuBNpqqX7Ci6Q1Os8-3Txb4n_JO7yEOq5PHfSH-HBDQ4cvoAB5_XoL51lHJ3b8zMIRU5aYXFg&splash=yes)
- [La console](https://console.cloud.google.com/logs/viewer?pli=1&project=project-id-9886081328049514054&resource=app_script_function&minLogLevel=0&expandAll=false&timestamp=2018-06-08T14:10:35.123000000Z&customFacets=&limitCustomFacetWidth=true&interval=PT1H&dateRangeUnbound=both&scrollTimestamp=2018-06-08T14:27:56.900000000Z)

Attention à plein d'ajout de triggers (Edit - current project triggers)

- [Reference - spreadsheet ](https://developers.google.com/apps-script/reference/spreadsheet/)
- [Guides - triggers ](https://developers.google.com/apps-script/guides/triggers/)
- [Guides - triggers events ](https://developers.google.com/apps-script/guides/triggers/events)
  - [Reference - url-fetch ](https://developers.google.com/apps-script/reference/url-fetch/url-fetch-app)
- [Reference - spreadsheet trigger builder ](https://developers.google.com/apps-script/reference/script/spreadsheet-trigger-builder)
- [Reference - mail app ](https://developers.google.com/apps-script/reference/mail/mail-app#sendEmail(Object))
- [API base adresse nationale](https://adresse.data.gouv.fr/api)
- Pour pouvoir versionner les appscripts : https://github.com/google/clasp


## CSV

- parser csv : [d3-fetch csv function](https://github.com/d3/d3-fetch#csv)
-

## WebGL

- limitation :
  - vieux navigateurs supportent mal
  - se base sur la carte graphique
  - bouffe plus de ressource même si trop bien car vecteurs, etc

- Comment protéger le gh token ? -> project data pour stocker des infos à l'échelle du projet (file data) -> + documenter qu'il faut créer un gh token et le rentrer dans le projet

## EsLint
- yaml?
- eslint recommended ?
- eslint --fix : pratique pour le style
- chercher comment l'appliquer sur un dossier et pas sur l'autre (https://github.com/DavidBruant/bouture/blob/master/.eslintrc.yml)
