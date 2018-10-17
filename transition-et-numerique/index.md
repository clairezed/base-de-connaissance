# Transition et numérique - quelle compatibilité ?

Un peu par hasard, je me suis trouvée à fréquenter pas mal les milieux écolo, les gens de la transition. Dans un contexte d'effondrement, réfléchir aux effets qu'ont nos pratiques professionnelles toutes tournées vers le numérique ne me semble pas débile.

Transition écologique et numérique... On peut concilier les deux ou c'est de la pure mauvaise foi ?

## Quelques chiffres

- selon [#Greenpeace](https://www.greenpeace.fr/il-est-temps-de-renouveler-internet/) le numérique représente 7% de la consommation d'électricité mondiale
- d'autres infos sur [consoglobe](https://www.consoglobe.com/internet-pollution-reelle-cg)

## Transition écologique

3 expressions-clés :
- User sobrement des ressources.
- Avoir des impacts limités, voire régénérant, sur les écosystèmes.
- Construire des communautés humaines résilientes.

## Rapport Lean ICT (Shift) pour une sobriété numérique (mars 2018)

> Le Numérique peut servir à repenser les usages et modifier les modes de fonctionnement et de production pour aboutir à une réduction des émissions de GES, voire à une réduction de la consommation énergétique : réseaux électriques  intelligents  (smart  grids),  mobilité  et  transports  intelligents,  monitoring  environnemental  et  urbain, dématérialisation, télétravail et visioconférence, bâtiments intelligents et écoconception logicielle.
>
> **Mais ceci ne se produira qu’à la condition de maîtriser les « effets rebond
»**. Or, jusqu’ici, les effets rebond se sont montrés plus importants que les gains apportés par l’innovation technologique (Magee et Devezas, 2017). Ainsi les bénéfices du télétravail sont-ils largement inférieurs à ceux intuitivement escomptés, en tout cas lorsqu’il n’est pas combiné à d’autres changements de l’écosystème social.

Il faut donc progresser notamment sur les points suivants :
- **Accélérer  la  prise  de  conscience des  impacts  environnementaux  du  Numérique**  dans  les  entreprises  et organisations publiques (via les DSI et les DDD), au sein du grand public (étiquetage) et dans la communauté de la Recherche.
- Réduire l’empreinte énergétique et environnementale du Numérique
passe par un **retour à une capacité individuelle  et  collective  à  interroger  l’utilité  sociale  et  économique  de  nos  comportements  d’achat  et  de consommation** d’objets et de services numériques, et à les adapter en conséquence
- Faire  en  sorte que  les  **organismes  publics intègrent  ces  impacts  comme  critères  de  décision  dans  leurs politiques d’achat** et d’utilisation des équipements numériques, ceci dans les pays développés comme dans les pays en développement.
- Faire  en  sorte  que  les  entreprises et  les  organismes  publics disposent de **références et d’outils leur permettant de prendre en compte l’impact environnemental** de la composante numérique des choix qu’elles envisagent

> A titre de conclusions provisoires, nous constatons tout d’abord que la Transition Numérique en cours résulte en une augmentation  forte  de l’empreinte  énergétique  directe  du  Numérique.
> 
> [...]
> consommer un euro de Numérique en 2018 induit une consommation d’énergie directe supérieure de 35% à ce qu’elle était en 2010.
> 
> **L’accélération de la croissance du Numérique n’ayant pas aujourd’hui l’effet espéré ni sur la croissance mondiale** (ni celle de l’OCDE) **ni sur la productivité** (Byrne et Corrado, 2017), il est donc d’autant plus important d’évaluer l’apport effectif de la Transition Numérique à la capacité des secteurs les plus énergivores (Electricité, Transports, Batiments) à le devenir moins


-> [Rapport "Lean ICT" - pdf](https://theshiftproject.org/wp-content/uploads/2018/05/2018-05-17_Rapport-interm%C3%A9diaire_Lean-ICT-Pour-une-sobri%C3%A9t%C3%A9-num%C3%A9rique.pdf) - Pour une sobriété numérique  - Rapport intermédiaire du groupe de travail dirigé par Hugues Ferreboeuf, pour le think tank The Shift Project - Mars 2018

## Etre développeur.se et transitionneur.se ?

cf [fil mastodon](https://mastodon.xyz/@FdC/100632791427437788)

> Vous semblez nombreux à vous préoccuper d' #Environnement, du #RéchauffementClimatique, de l'#Effondrement mais vous êtes aussi nombreux à bosser dans l'informatique... Comment vous faites pour rester en accord avec vos convictions ? Non, parce qu'on est quand même un grosse part du problème non ??

Quelques réponses : 

- Perso, en plus de me former en qualité web et accessibilité, je regarde du côté de l'éco-conception / greenIT, et je vois ce que je peux appliquer au web, aux sites que je fais. (d'ailleurs j'aimerais migrer de Mastodon à Pleroma, histoire que l'impact énergétique soit moins gros)
- Si les sites que je fais peuvent marcher sur des vieux ordinateurs, un utilisateur de mes sites auront moins l'envie d'en acheter un neuf. Si je fais attention aux ressources (JS à gogo), la batterie d'une utilisatrice sur mobile s'usera moins rapidement. Si je peux pousser une solution "site statique" à un client, c'est moins de servers qui tournent, pour les BDD, etc
- [Éco-conception : mon site web au régime](https://www.paris-web.fr/2016/conferences/eco-conception-mon-site-web-au-regime.php), Frédéric Bordage, 2016
- [Internet et les TIC, pas très écologiques ?](https://www.paris-web.fr/2014/conferences/internet-et-les-tic-pas-tres-ecologique.php), Luc Poupard, 2014
- [Le Green IT : facteur incontournable pour laver plus vert le web responsable](https://www.paris-web.fr/2017/conferences/le-green-it-facteur-incontournable-pour-laver-plus-vert-le-web-responsable.php), Christophe Clouzeau, 2017
- rien n'interdit de concevoir des internetz responsables et économes en matière rare et énergie, conçus et maintenus localement par un réseau distribué de corps de métier redevenu artisanal et intégré à la communauté locale. 
-  on peut alléger les pages web, réduire les vidéos, favoriser le cache des sites pour pas générer les pages a chaque fois. Je ne cherche pas à capter mes usagers mais plutôt proposer un service sincère sans pièges, en réduisant le service a l'essentiel. Pas de pub, pas de référencement (que du naturel et éventuellement des articles)... 
-  à titre personnel j'ai fait des recherches sur le #greenit et le #greencomputing en recyclant au maximum le matériel, achetant d'occasion, usant jusqu'à la moelle les machines, gardant les pièces, tri de ce qui ne peut être utilisé, augmentation de la durée de vie de la machine, achat de batteries pour faire durer plus longtemps, utilisation de raspberry-pi comme mini-serveurs parfois etc ...
-  si on héberge soi-même, limitant l'usage des datacenter, utilisant les bookmarks une fois que le site a été trouvé, décentralisant et utilisant ce dont on a besoin des pas des machines overshoot, en poussant la durée de vie au maximum est-ce plus écologique de lire la presse en ligne ou d'acheter du papier fait à partir d'arbres ?

## Éco-conception : mon site web au régime

[Vidéo Éco-conception : mon site web au régime](https://www.paris-web.fr/2016/conferences/eco-conception-mon-site-web-au-regime.php), paris web 2016

Aspects fondamentaux dans la démarche d'éco-conception :
- Allonger la durée de vie des terminaux des internautes (60%)
- Réduire le nb de serveur nécessaires (20%)
- Réduire la quantité de bande passante consommée (20%)

Principaux leviers :
- conception fonctionnelle et conception technique : 60%
- Développement : 15%
- Hébergement : 25%

Critères à observer :
- poids de la page
- nombre de requêtes HTTP
- DOM
- délai pour l'affichage complet
-> cf score EcoIndex.fr

### Bonnes pratiques clés :

Conception fonctionnelle :
- Eliminer les fonctionnalités non indispensables (frugalité)
- Quantifier précisément le besoin (sobriété)

Conception graphique et ergonomie :
- Préférer l’approche « mobile first »
- Epurer l’interface (sobriété)
- Préférer la saisie assistée à l’autocompletion

Conception technique :
- Adapter la technologie à l’usage
- Eviter les plugins de type Flash
- Supprimer tous les traitements inutiles (animations, etc.)
- Eviter les allers-retours avec le serveur

Templating général
- Valider le code (W3C, linteurs, etc.)
- Eviter les images et les optimiser (compression, choix de format, regroupement via sprite, etc.)
- Factoriser, modulariser, et externaliser les librairies (CSS, JS, etc.)
- Epurer, minifier, compresser les fichiers avant de passer en prod.

Code client :
- Réduire les accès au DOM et éviter de le manipuler
- Optimiser le code Javascript / CSS
- S’appuyer sur l’architecture AJAX pour ne pas mettre à jour toute la page
- Attention aux boucles

Code serveur :
- Favoriser les pages statiques
- Optimiser le code serveur
- Attention aux boucles (dont SQL)

Hébergement
- Ne livrer que du contenu optimisé, si possible statiquement (compression manuelle des fichiers plutôt que gzip à la volée par le serveur web)
- S’assurer que le cache (navigateur et front web) est utilisé au maximum
- Optimiser l’infrastructure logiciel (paramétrage)
- Optimiser l’infrastructure matérielle (choix du matériel, etc.)
- Choisir un hébergeur engagé