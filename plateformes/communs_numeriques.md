# Construire des communs numériques - Matti Schneider

[communs.mattischneider.fr](https://communs.mattischneider.fr)

<!-- TOC depthFrom:2 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Constituants](#constituants)
	- [Code source](#code-source)
	- [Usage](#usage)
	- [Données](#donnes)
	- [Communauté](#communaut)
	- [Marque](#marque)
- [Gouvernance](#gouvernance)
	- [Défendre les intérêts communs](#dfendre-les-intrts-communs)
	- [Définir les investissements](#dfinir-les-investissements)
	- [Faire évoluer le commun](#faire-voluer-le-commun)

<!-- /TOC -->

## Constituants

### Code source

- mise à disposition du code source sous une **licence libre**
  - a minima licence MIT
- mise à disposition du code source avec une **clause de repartage**
  - AGPL v3 et assimilés
- moyen de solliciter l’**intégration de modifications effectuées par un usager** dans la base de code originelle
  - github, gitlab
- engagement sur le **délai de traitement des sollicitations** d’intégration de modifications, **charte de communication** avec les contributeurs potentiels

### Usage

Le service doit fournir une garantie de liberté d’usage

- **conditions générales d’utilisation** qui permettent l’usage sans conditions autres que celles strictement nécessaires à l’opération du service et à la prévention des actes visant à réduire la capacité d’autres usage
  - cgu lisible avec garanties juridiques fortes (exemple de [mes-aides.gouv](https://mes-aides.gouv.fr/cgu))
- engagement sur un **taux de disponibilité du service** pour ses usagers (SLA). Pour ne pas freiner l’évolution du service, ce SLA doit évoluer dans le temps et être interprété comme un « budget de contribution »

### Données

- **mise à disposition des données manipulées** sous une licence qui en permet la réutilisation
  - exporter à intervalles réguliers (et a minima hebdomadairement) sur data.gouv.fr la base de données du service en rendant impossible la réidentification de ses utilisateurs18, sous a minima [Licence ouverte 2](https://www.etalab.gouv.fr/wp-content/uploads/2017/04/ETALAB-Licence-Ouverte-v2.0.pdf) voire mieux [licence ODbL](https://fr.wikipedia.org/wiki/Open_Database_License)
- mise à disposition des **statistiques de fréquentation de chaque fonctionnalité** du service sous une licence qui en permet la réutilisation.
  -  exposer une instance publique du service de suivi Piwik (ou Xiti), configurée en [conformité avec la règlementation CNIL](https://www.cnil.fr/fr/solutions-pour-les-cookies-de-mesure-daudience) afin d’être exempté de consentement en anonymisant tout le suivi à la source et de récolter le maximum d’informations. Préciser que les données offertes par cette instance sont à disposition sous Licence ouverte.
- mise à disposition des données produites par les usagers sous une **licence de repartage**
  - [licence ODbL](https://fr.wikipedia.org/wiki/Open_Database_License)

### Communauté

Par exemple solliciter la communauté pour contribuer ponctuellement aux communs numériques dont ils forment la communauté, pour les promouvoir ou encore pour procéder à un arbitrage référendaire.

- mise à disposition de tous les contributeurs des **moyens de contacter la communauté**, tout en garantissant un volume limité de sollicitations afin de maximiser la valeur potentielle.
  - liste de diffusion compatible avec le droit européen (mailjet, framaliste) + engagement sur une fréquence maximale d'envoi.
  - mise à disposition d'un pad collaboratif pour préparer les envois.
- mise à disposition de tous les contributeurs de **moyens de contacter le public**, tout en garantissant une forte pertinence des messages diffusés
  - charte rédactionnelle (exemple de [mes-aides-ui](https://github.com/betagouv/mes-aides-ui/wiki/Notre-ton))
  - système de délégation de compte pour chaque média social utilisé par le service (TweetDeck pour Twitter, Business Manager pour Facebook…)
  - et faire certifier le compte social par l’opérateur du réseau.

### Marque

Les marques représentent le capital réputationnel des communs numériques. Pour être compatibles avec ce statut, leur bénéfice doit donc être mis en partage et défendu sans réappropriation, comme les autres formes de capital.

- **protection juridique des éléments constitutifs de la marque et leur mise à libre disposition** sous condition du respect d’une charte .
  - fournir tous les éléments de marque sur un page web,
  - les déposer à [l’INPI](https://www.inpi.fr/fr/services-et-prestations/depot-de-marque-en-ligne)
  - adapter la [Politique de marque de Wikipédia](https://meta.wikimedia.org/wiki/Trademark_policy/fr#policy) pour définir les cas d’usage recommandés et ceux défendus. Les cas défendus sont justifiés par l’explicitation du danger qu’il ferait peser sur le capital réputationnel.


## Gouvernance

Gouvernance pensée sur le principes de **rôles à définir**.

### Défendre les intérêts communs

- **garant d’application du commun**, avec une liste claire des sanctions applicables en cas de non-respect des règles qu’il décrit
- **responsable opérationnel du commun**, avec des moyens de gestion d’accès et de rationnement temporaire pour garantir un accès à tous les membres de la communauté.
- **représentation du commun** pour répondre aux critiques
- **représentation juridique du commun**, pour gérer la répartition de la responsabilité juridique, les actions à mettre en oeuvre en cas d'infraction (ex : contenu mis à disposition en infraction avec le droit)

### Définir les investissements

- **responsabilité de produit (product ownership)**, avec un droit d’arbitrage entre la mise en œuvre de fonctionnalités incompatibles dans leurs effets ou dans leur consommation de ressources.
- **garant financier**, avec la responsabilité de vérifier la proportionnalité des prélèvements sur les ressources communes avec les objectifs déterminés collectivement.

### Faire évoluer le commun

Un **espace de réflexivité sur les règles en place, leur application et leur évolution** doit être aménagé. Les modalités de cette évolution sont elles-mêmes des règles soumises au processus d’évolution.
