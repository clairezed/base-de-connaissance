# Kiwi party 2018

## Manifeste pour un web éthique - Arnaud Malon (groupe crédit mutuel)

  www.6x8.org

  Ce que nous travailleurs du web pouvons faire à notre niveau pour que le web :
  - reste accessible (respectueux des gens) ->
    - accessibilité,
    - qualité web (+ facile à promouvoir en entreprise ?) : approche globale et multidisciplinaire (visibilité, perception, technique, contenus, services)
  - reste universel
   - qqsoit navigateur, systeme d'exploitation, matériel
   - Google AMP, facebook instant article... que de grandes régies présélectionnés, des formats standardisés...
  - soit antirouille
    - certains sites vieillissent mal. Des sites qui rouillent, c'est des info qui se perdent
    - et quand les navigateurs refuseront d'afficher flash, etc -> vieux sites sont perdus ?
  - soit respectueux de la vie privée (coucou Mark)

  - restreindre les fonctionnalité -> frugalité
  - conception graphique
  - techno adapté
  - developpement, avec optimisation (15%)
  - hébergement (cdn, etc) (25%)

  Ecoconception : opqast, green-it

  Aller vers amélioration continu et implication de tous les acteurs (kaizen - bon changement)

## Embarquement Agile : comment transmettre sa culture à une nouvelle personne en 5 semaines ? - Florian Ferbach (Marmelab)

  Spécialisé sur projet à fort risque, avec beaucoup d'inconnu. Démarre les projets chez les clients (lean startup, scrum master...)

  On parle d'embarquement agile, "onboarding".

  C'est quoi le problème ?

  Embarquement = **intégrer** une nouvelle recrue ("en harmonie avec les autres éléments")
  Problème (choix en fait) : les équipes sur les projets changent tout le temps. (pour garder les dev + longtemps) -> faut le même niveau de service qqsoit l'équipe. Donc tous les humains doivent être au top.
  -> open source, veille, budget conférence, hackday 2j/mois... Ca marche pour les maintenir eu top.
  Mais pour les amener ?

  Pour l'onboarding :
  - documentation : lire 1200 pages en vrac le premier jour ?
  - tour d'entreprise : aucune colalboration, on travaille pas avec les gens
  - organigramme ?
  -
  - camp d'entrainement : on envoie les devs ailleurs pour se former. Ils reviennent bons techniquement, mais savent pas taffer avec leurs collègues
  - pairing -> là, c'est mieux. Mais un seul point de vue, et souvent c'est le dernier recruté qui forme (donc le + junior)

  Manque un point essentiel : mise en situation réelle

  Embarquement agile :
  - connaitre la cible, définir c'est quoi le collaborateur idéal, faire une checklist pour l'orienter (soft skills, programming, project management, collaboration...) Chez Marmelab, 143 points pour décrire le collaborateur idéal.
  - Ce sont les membres de l'équipe qui définissent cette liste

  Exemple de Julien :
  - quarto comme sujet d'intégration, pour casser le stress, décrocher de son expérience passée. Faire comprendre que là, le but n'est pas de travailler mais d'apprendre (et le jeu fait parti de la culture d'entreprise)

  Puis itération d'une semaine avec chacune un challenge.
  - Qui ? le nouveau, un tuteur (svt dev senior), un facilitateur (accompagne sur processus et méthodes agiles), et tout le monde
  - 1/ phase de planning : le planning doit être sur mesure, pour convenir à un humain spécifique. Graphe 'important x acquis', puis on voit ce qu'il reste à acquérir, et on pose le planning des challenge en fonction
    - challenge centré utilisateur : faire le jeu du quarto en console
    - challenge collaboration : travailler avec qqn à distance
  - 2/ daily : le tuteur aide le tutoré à échouer rapidement. Il accompagne, donne pas de solution toute cuite
  - 3/ démo engagée devant toute la boite, pour désamorcer la peur de parler en public, et consolider l'apprentissage
  - 4/ rétro, juste après la démo. Comment il a senti sa semaine ? Qu'est-ce qu'il a appris ? Est-ce qu'il aurait fait des choses différement (identifier vecteurs d'amélioration). Il faut être honnête, savoir avouer ses échec
  - 5/ évaluation, fournir un feedback au nouveau

  C'est aussi une période d'essai, ça peut s'arrêter à un moment

  La réussite, c'est différent de l'apprentissage, et la cible doit être l'apprentissage

## MJML, le nouveau standard pour écrire nos mails ? - Thomas Deneulin (Weglot, Delipress, WP God, blogueur sur Essential Developer Skills)

  Email : `table`, `tr`, `td`, c'est l'horreur
  Faut penser aussi
  - au responsive, etc. Demande bcp de compétence,
  - à tous les clients mail (gmail, yahoo, outlook...) qui peuvent se comporter différemment selon navigateur
  Y'en a qui veulent dans les mails des carousels, un accordion...

  MJML : markup language développé en js, open source et gratuit. Développé par Passport (qui a été absorbé par mailjet)
  v3 : en react
  v4 : on enlève react, passage en vanilla.js (perf x10 ou 15 sur la compilation)

  Comment ça marche ?
  - Structure de base comme HTML, avec head et body
  - une approche section / column (comme bootstrap)
  - dans le head, on peut définir des attributs par défaut (`mj-attributes`), des classes.
  - si besoin de spécificité, sur mobile par ex : `mj-style`

  Constructeur email :
  - topol
  - Delipress
  - grapeJS
  Sont basés sur `mjml2html`, à qui on envoie une structure en json, et voilà

  Pour les dev : une ligne de commande pour compiler
  Y'a aussi une API, mais + compliquée à gérer

  Tests sous litmus (???) ?

  Poids moyen d'un email ? ne sais pas. Garder les bonnes pratiques, optimisez les images, etc

  En termes d'accessibilité ? Pas la priorité au départ, mais ça évolue (même si pas encore totalement accessible)

  Les constructeurs permettent déjà de faire beaucoup de choses, passer au langage mjml pour cas complexe

## CSS3+, une plongée dans le futur - Jonathan Giamporcaro

  Ce qui existe déjà :
  - Grid layout
  - `repeat` pour les column, par ex
  - `fr` : fraction d'espace
  - variables css (plus besoin de preprocessors ?)
  - `@supports` : pour tester si le client supporte une certaine feature (grid, par ex)
  - sélecteur d'attribut i : toutes les capitalisations fonctionneront

  Dans les draft :
  - `filter()`, qui va permettre d'appliquer des filtres aussi aux background-images
  - scroll snap points : définir des points d'accroche, si on scroll on arrive au prochain point d'accroche
  - pseudo-class de niveau 4
    - `:has` : cible un élément si au moins un des sélecteurs passé en param a cet élément
    - `:dir` : en fonction de la direction du texte (cool pour sites multilangues)
    - `:any-link` : cible a, area ou link avec href (= ceux qui sont vraiment des liens)
    - `:default` : par ex, un attribut checked non checké.
    - `:in-range` et `out-of-range` : si demande de saisie entre 0 et 10, permet de styler différemment si on entre 11.
    - `:placeholder-shown`
    - `:past`, `:current`, `:futur` : pr lecteur d'écran ou sous-titres...
    - `:nth-child` : renforcé, pour ciblé des éléments children suivant une condition (:nthè-child(event of :not([hidden]))). Parmet de pas casser les zébrures alternées de ligne de tableau si une ligne est cachée, par ex

  Projet Houdini
  - groupe de travail Mozilla, Apple, Opera, Microsoft, HP, intel, Google
  - `Layout API` : permet aux dev de créer leurs propres algo de mise en page (comme `display: grid`)

## Slow UX, de l'art de la lenteur dans les processus de conseption centrés sur l'usage - Raphaël Yharrassarry (@iergo)

  Mythe : 'on peut faire des tests utilisateurs vite fait dans des starbucks et ça va être top'
  Il faut comprendre à quoi on s'engage quand on fait du guerrilla ux.

  Méthodes guerilla (l'atelier UX le plus rapide du monde) :
  - 2 min : quels sont ses besoins ? (photos d'une fille qui essaye d'atteindre un livre en hauteur -> un tabouret ? accéder au savoir ?)
  - 4 x 2 minutes, (observation, interpretation, expression des besoin, solutions) sur une autre photo (étudiants assis dans le couloir qui bossent, lisent...) (atelier proposé comme démo dans le cadre d'un appel d'offre) (difficile de casser el cadre d'un appel d'offre en UX)

  Design sprint
  - En 5 jours : objectif, esquisser des solutions, décider, prototyper, tester.
  - On vend 5 jours, mais faut 3 semaines de préparation + 1 semaine de restitution. Et la phas ede prototypage + test est souvent bâclée. On n'a le temps de prototyper qu'un cas réduit, etc.
  - On voit apparaitre des design sprint de 5 semaines -> design marathon ?
  - Ou bien utilisé de façon ponctuelle pour relancer un projet
  - Le design sprint a un peu vécu ? Bientôt une nouvelle méthode révolutionnaire ?

  UX
  - p < 0.01 : probabilité que le résultat soit dû au hasard, et pas aux conditions mises en place.
  - p < .05 : 5% de chance que ce qu'on mesure soit dû au hasard (seuil de référence, en gros). Donne la validité de l'expérience.
  - + on augmente le nb d'expérimentateur, plus l'expérience est valide, robuste. Donc, la validité est liée au temps qu'on y passe.

  Des méthodes quick, mais pas dirty ? Comment contourner le lien entre validité et temps apssé ?
  - sondes culturelles : on donne aux utilisateurs des objets, parfois improbable, pour retracer une activité. A la fin, les utilisateurs la redonne (APN, carte, carnet, cartes postales à envoyer...). Si possible improbable et stimulant, pour permettre l'expression des attentes et usages
  - tri par cartes, à faire en ligne (http://ows.io/os/4268zk12)
  - tests utilisateur en ligne. Pas besoin de suivre en direct.
  L'idée est qu'on les fait à distance, donc moins de temps passé tout en améliorant la validité. Mais au niveau planning, c'est toujours long.

  Utilisateurs et temps :
  - cf A/B testing (une référence / un test, en prod, avec orientation aléatoire des visiteurs). Comment savoir si mon test est valide ? cf https://measuringru.com/ab-cal/ -> + de monde, sur + de temps. Si on est sur un service que les gens utilise régulièrement (ex meetic, avec 2 ou 3 passage par semaine) -> faut laisser le temps aux gens d'appréhender l'interface. Il y a 3 phases : 1 à 2 semaines d'apprentissage d'abord, le pivot (ou pas), et le vrai calcul. Faut laisser le temps aux utilisateurs de s'habituer aux changements.

  Co-conception
  - l'équipe d'UX doit bosser avec un ou deux temps d'avance sur l'équipe dev; les devs ont besoin de la conception pour commencer leur cycle.
  - Le cycle UX 0, de recherche, prend pas mal de temps (ateliers, entretiens, sondes culturelles...). Ce temps est incompressible.
  - idem, les tests utilisateurs sont à prévoir 2-3 semaines en amont (et que les dev soient prévenus pour que l'interface soit prête)

  La première idée / solution est probablement médiocre, même si suffisante pour le client ? Laisser le temps des discussions informelles pour que de meilleures idées arrivent ?

  Envie d'être un designer holistique : faire des choses qui paraissent incohérentes vu de l'ext mais finalement rtouver la bonne solution

## Gérer le mode hors-ligne grâce aux services workers  - Corinne Schillinger

  Services workers : utilisables en prod, oui oui !
  Sorte de proxy, fichier js, associé à un domaine, qui intercepte les requetes serveur et modifie les réponses retournées.
  Avec unservice worker, la requete est direct intercepté. Le SW peut dire : va pas taper sur le serveur, sers-toi du cache -> hyper rapide du coup.

  SW est téléchargé et exécuté parallèlement, en background. Donc pas accès au DOM. Mais pas bloquant.

  Les contraintes :
  - https obligatoire (pour des questions de sécu). Permet d'utiliser des API fonctionnant QUE en https. Mais on peut l'installer en localhost (seule exception autorisée).
  - le SW peut uniquement controler un site de meme origine (protocole, port et hote identique)

## Arrêtez de nous demander combien coûte une ligne de code ! - Aurélie Guillaume (CREADS)

  Nous même on le fait "Rajouter ça de telle manière, ça te prendra pas + de temps".
  Pourquoi on pose cette question ? Réflexe de l'ancien temps. Sauf que derrière le code il y a beaucoup de coûts cachés.

  Un code peu s'écrire de plein de façons différentes, déjà.

  Coûts cachés :
  - cout de conception : gestion de projet, graphisme, ux, pour produire des lignes de code les plus adaptées au projet.
  - après la ligne de code : tests, etc (process qualité, guidelines, code review...)
  - coût de mise en place de l'infrastructure (serveur, nom domaine..)
  - coût du code legacy et des évolutions
  - chaque techno a son coût d'exploitation (.NET : faut serveur spécifique, etc)

  Wordpress : déjà 1,5 millions de lignes de code produites :)

  Cf openhub ?

## Préprocesseurs vs CSS natif : le match ! - Jonathan Levaillant (JoliCode)

  Préprocesseur : outil qui permet de générer dynamiquement du css
  1. sass : 65%
  2. postCss
  3. Less
  4. Stylus

  Mais y'a des dérives et problèmes lors de la compilation.

  Problème de l'imbrication de css :
  - copie du code html. Si le html change, ls css est cassé
  - spécificité des sélecteurs (on fini avec du !important partout)
  -> se limiter aux pseudo-class et pseudo-éléments (gni ?)

  Pb @extend :
  - peu ruiner l'ordre d'insertion des sélecteurs
  - accepte pas d'argument
  - pas possible dans une media-query
  -> utiliser des mixins plutôt qu'extend

  Battle !

  1/ Fonction calc()
  - il est possible de réaliser des calculs avec des unités des différents
  - permet de garder le contexte de l'opération (`calc(100%/7)` plutot que `14,7656%`)

  2/ Custom properties (propriété personnalisées)
  - `var(--)`
  - peut être manipulé en js
  - comparaison avec les variables Préprocesseur.
  - supporté sauf IE...

  3/ matches()
  - link:matches(hover, active)
  - comaptibilité  : 90%. Dans 6 mois / 1 an ça devrait être bon.

  Pour les fonctionnalité structurelle : css va prendre le dessus ?
  Pour les fonctionnalités programmatiques (fonctions, boucles...) : utiliser les pré-processeurs

  http://jonathanlevaillant.fr/2018/kiwiparty.pdf

## Privacy by design - m4dz

  Les éditeurs d'application font tout pour nous donner l'illusion d'une grande puissance, car ils sont tous en compétition pour choper notre attention. Les vrais clients des services, c'est la pub, les régies. Nous, notre attention, c'est juste le carburant.

  On a
  - des grosses boites qui pompent des données
  - des petites boites qui pompent des données (sans forcément s'en rendre compte (Prestashop demande à votre client sa date de naissance))
  - des startups qui pompent de la donnée pour faire comme les grands

  Cf logo de Cambridge Analytica

  Donner trop de permeissions donne l'illusion qu'on contrôle. Donner trop de pouvoir rend les choses trop complexe
  - illusionner sur une protection trop parfaite.
  - c'est à nous, dev, designer, de prendre la responsabilité de la vie privée.

  On a lâcher les derniers lambeau de notre vie privée pour le luxe de l'hyperconnexion.

  Privacy by Design : 1995, par les équivalents de CNIL d'autres pays.

  7 lois, dont :
  - il faut partir du principe que les données vont fuiter, et anticiper sur ce qu'on fera

  **PETS** - Privacy E? Technology : chiffrement, gérer méta-données et permissions, quelle ligne de code permet de couvrir tel aspect de la loi, gérer finement les identités...

  Pseudonomyser : substituer ce qui est de l'ordre de la donnée perso pour qu'on puisse pas reconnaitre l'utilisateur.
  Pour faire du vrai pseudonymat : differentail privacy, introduire du bruit controllées dans les données.

  Dans l'iéal :
  - OpenId plutôt que facebookId
  - hasher, chiffrer
  - faire passer des cron pour supprimer des données

  **OWASP** : top 10 privacy risks

## L'index mobile first de Google : révolution ou encore une prise de tête pour les concepteurs de sites web ? - Dan Bernier

## Le Cloud pour les petits - Rodolphe Rimelé (alsacréation)

  1er fournisseur cloud : Amazon, puis Alibaba

  Force des petites equipes : + réactifs que les + gros (avantage d'utiliser le cloud pour ça)

  Grands principes : scalabité et élasticité (échelonnable, extansible, redistribuable...)

  Cloud encourage les bonnes pratiques, oblige à économiser stockage et puissance, faire des backups, etc

  Faas : function as a service. Serverless (lambda + gateway API chez AWS)

  Question philosophique : est-ce qu'on soutient ça ? AWS ?

  Cas pratiques :
  - 1/ youtube, boncoin, fb pour 5000€ ? Niet
  - 2/ petit CMS, avec video d'apprentissage : on peut utiliser un service cloud pour l'hébergement des videos
  - 3/ Site vitrine avec un formulaire de contact : hébergement statique (0.5$/mois), une fonction serverless pour le contact...

  http://kiwi.gg/partycloud

## Arrêtez de vendre des prestas d'UX dans vos projets web ! - Pierre Fritsch

... ou bien faites-le vraiment et vendez-le.

UX = U + X
- Utillisateur : faut les intégrer ! (les rencontrer, utiliser leurs données...)
- Expérimentation

- interview et focus group
- shadowing
- storyboard sur post-it
- co-conception : design studio (ou 6-to-1) : faire dessiner les utilisateurs !
- @pierrefritsch

# Checks
- faire des grilles
Creer les outils, adaptés à votre activité, qui vous feront gagner du temps
