---
title: MCP (Model Context Protocol)
deprecated: false
hidden: false
metadata:
  robots: index
---
[Model Context Protocol (MCP)](https://modelcontextprotocol.io/introduction) est une standardisation de la façon dont les assistants IA interagissent avec les API, et ReadMe apporte cette capacité à votre hub développeur. Grâce aux serveurs MCP, vous pouvez convertir votre documentation API en une ressource structurée que les assistants IA peuvent comprendre et avec laquelle ils peuvent interagir de manière programmatique.

## Fonctionnalités principales

* **Outils personnalisés** : Définissez des combinaisons de workflows et d'endpoints personnalisés. <Badge label="New" bgColor="var(--purple)" textColor="var(--purple100)" cornerRadius="30px" />
* **Routes activées** : Désactivez les endpoints que vous ne souhaitez pas rendre accessibles dans votre serveur MCP <Badge label="New" bgColor="var(--purple)" textColor="var(--purple100)" cornerRadius="30px" />
* **Intégration OpenAPI** : Générez un serveur MCP à partir de votre spécification OpenAPI existante.
* **Les assistants IA peuvent se connecter à votre serveur MCP pour** :
  * Lire et comprendre votre spécification OpenAPI.
  * Exécuter des appels API.
  * Rechercher dans la documentation avec [Ask AI](/docs/ask-ai).
* **Outils MCP** :
  * **Outils OpenAPI** :
    * `execute-request` - Effectuer des appels API directement depuis votre spécification
    * `get-endpoint` - Récupérer des informations détaillées sur les endpoints à la demande
    * `get-request-body` - Accéder aux paramètres de requête structurés
    * `get-response-schema` - Comprendre ce que retourne votre API
    * `list-endpoints` - Parcourir tous les endpoints API disponibles
    * `list-security-schemes` - Accéder aux exigences d'authentification
    * `search-schema` - Trouver exactement ce dont vous avez besoin dans votre spécification API
    * `get-code-snippet` - Exemples de code dans le langage de votre choix pour interagir avec votre endpoint.
  * **Outils de documentation** :
    * `search` - Rechercher dans l'ensemble de votre base de connaissances les informations pertinentes
    * `fetch` - Retourner une page de guides

<Callout icon="📘" theme="info">
  Les outils de documentation nécessitent la mise à niveau de votre plan actuel avec le <Anchor label="AI Booster Pack" target="_blank" href="https://readme.com/pricing">AI Booster Pack</Anchor>.

  Pour les clients Enterprise, veuillez contacter votre CSM.

  Pour les clients Startup et Business, veuillez mettre à niveau votre plan avec l'AI Booster Pack depuis votre page **Gérer le plan** dans les Paramètres.
</Callout>

## Comment ça fonctionne

Nous créons un serveur MCP dédié qui se connecte à votre spécification OpenAPI et à la fonctionnalité [Ask AI](/docs/ask-ai). Cela crée un pont entre votre documentation API et les assistants IA, rendant votre API instantanément plus accessible et compréhensible pour les outils IA.

## Fonctionnalités supplémentaires

* **Branches** Par défaut, le serveur MCP est connecté à la dernière version stable. Pour choisir une branche différente, ajoutez `?branch=<name>` à l'URL MCP. REMARQUE : Lorsque vous êtes sur une branche, `search-documentation` ne sera pas disponible.
* **Projets privés** Pour accéder aux projets protégés, vous devrez configurer votre client MCP pour envoyer un en-tête `x-readme-auth`
  * Protégé par mot de passe : `x-readme-auth` doit être le mot de passe du site
  * Coéquipiers uniquement & Connexion personnalisée : `x-readme-auth` doit être une clé API sous la forme `bearer <api_key>`

## Démarrer avec MCP

Choisissez comment vous souhaitez commencer à utiliser MCP :

1. <Anchor label="Auto-Generate Your Own MCP Server" target="_blank" href="doc:generate-your-own-mcp-server">Générez automatiquement votre propre serveur MCP</Anchor> : Chaque projet ReadMe inclut automatiquement un serveur MCP entièrement configuré. Activez simplement MCP pour connecter votre documentation API aux outils IA.
2. <Anchor label="Use ReadMe’s MCP Server" target="_blank" href="doc:readmes-mcp-server">Utilisez le serveur MCP de ReadMe</Anchor> : Avec le serveur MCP de ReadMe, vous pouvez faire tout ce que vous faites habituellement dans ReadMe, comme ajouter et modifier des pages, directement via notre API.