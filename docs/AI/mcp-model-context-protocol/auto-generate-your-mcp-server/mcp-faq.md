---
title: FAQ MCP
deprecated: false
hidden: false
metadata:
  robots: index
---
<br />

Cette FAQ répond aux questions fréquentes sur l'utilisation du [Model Context Protocol (MCP)](https://modelcontextprotocol.io/introduction) avec les projets ReadMe.

## Général

### Qu'est-ce que le Model Context Protocol (MCP) ?

Le Model Context Protocol (MCP) est un standard définissant la façon dont les assistants IA interagissent avec les API. Dans ReadMe, MCP transforme votre documentation API et votre définition OpenAPI en une ressource structurée que les outils IA peuvent comprendre, rechercher et appeler de manière programmatique.

### Comment MCP fonctionne-t-il avec mon projet ReadMe ?

ReadMe crée un serveur MCP dédié à votre projet. Ce serveur se connecte à votre spécification OpenAPI et à votre fonctionnalité [Ask AI](/docs/ask-ai), afin que les assistants IA puissent :

* Lire et comprendre votre spécification OpenAPI
* Exécuter des appels API
* Rechercher dans votre documentation
* Récupérer les détails des endpoints, les corps de requête, les schémas de réponse et des exemples de code

### Que peuvent faire les assistants IA via le serveur MCP ?

Une fois connectés à votre serveur MCP, les assistants IA peuvent :

* Parcourir et lister les endpoints API disponibles
* Inspecter les schémas de sécurité et les exigences d'authentification
* Récupérer la documentation détaillée des endpoints
* Obtenir des schémas de requête et de réponse structurés
* Générer des exemples de code pour appeler votre API
* Rechercher dans votre documentation générale des contextes et des guides

## Activation et utilisation de MCP

### Comment activer mon serveur MCP dans ReadMe ?

En mode Édition, dans le coin supérieur droit, cliquez sur **:sparkles:AI** pour ouvrir le panneau latéral. Sélectionnez **MCP** et activez le bouton **Serveur MCP** pour démarrer votre serveur MCP. Une fois activé, votre URL MCP sera :

`https://your-project.readme.com/mcp`

Vous pouvez partager cette URL avec vos développeurs afin qu'ils puissent connecter des outils IA compatibles (comme Cursor) directement à votre API et à votre documentation.

### Comment tester que mon serveur MCP fonctionne ?

Une fois MCP activé :

1. Ouvrez votre éditeur IA (Cursor, VS Code, etc.).
2. Démarrez une nouvelle conversation avec l'assistant IA.
3. Posez des questions telles que :
   * « Comment faire [cas d'usage courant] ? »
   * « Montre-moi un exemple de [fonctionnalité API]. »
   * « Crée une [type d'intégration] en utilisant [votre API]. »

Si la configuration est correcte, l'assistant devrait être en mesure de découvrir vos endpoints, de lire votre documentation et de générer des exemples fonctionnels.

### Puis-je contrôler quels endpoints sont exposés via MCP ?

Oui. Vous pouvez désactiver les endpoints que vous ne souhaitez pas rendre accessibles depuis votre serveur MCP sous **Routes MCP activées**. Seules les routes activées seront disponibles pour les assistants IA via les outils MCP.

## Outils et capacités

### Quels outils OpenAPI sont disponibles via MCP ?

Le serveur MCP expose plusieurs outils axés sur OpenAPI, notamment :

* `execute-request` – Effectuez des appels API directement depuis votre spécification.
* `get-endpoint` – Récupérez des informations détaillées sur un endpoint.
* `get-request-body` – Accédez aux paramètres de requête structurés.
* `get-response-schema` – Consultez ce que retourne votre API.
* `list-endpoints` – Parcourez tous les endpoints API disponibles.
* `list-security-schemes` – Inspectez les exigences d'authentification.
* `search-schema` – Effectuez des recherches dans votre schéma OpenAPI.
* `get-code-snippet` – Générez des exemples de code dans le langage de votre choix.

### Quels outils de documentation sont disponibles ?

Les outils de documentation se concentrent sur votre base de connaissances générale :

* `search` – Recherchez dans l'ensemble de votre documentation du contenu pertinent.
* `fetch` – Retournez une page de guide spécifique.

<Callout icon="📘" theme="info">
  Les outils de documentation nécessitent la mise à niveau de votre plan actuel avec le <Anchor label="AI Booster Pack" target="_blank" href="https://readme.com/pricing">AI Booster Pack</Anchor>.

  Pour les clients Enterprise, veuillez contacter votre CSM.

  Pour les clients Startup et Business, veuillez mettre à niveau votre plan avec l'AI Booster Pack depuis votre page **Gérer le plan** dans les Paramètres.
</Callout>

## Configuration et accès

### Comment les branches fonctionnent-elles avec MCP ?

Par défaut, le serveur MCP se connecte à la dernière version stable de votre projet. Pour cibler une branche différente, ajoutez `?branch=<name>` à l'URL MCP. Lors de l'utilisation d'un serveur MCP spécifique à une branche, la fonctionnalité `search-documentation` ne sera pas disponible.

### Comment autoriser MCP à accéder aux projets privés ?

Pour les projets privés ou protégés, vous devrez configurer votre client MCP pour envoyer un en-tête `x-readme-auth` :

* **Protégé par mot de passe** : `x-readme-auth` doit être le mot de passe du site.
* **Coéquipiers uniquement & Connexion personnalisée** : `x-readme-auth` doit être une clé API de la forme `bearer <api_key>`.

### Comment générer des instructions de connexion pour mes utilisateurs ?

Après avoir activé votre serveur MCP, cliquez sur **Générer un modèle MCP** dans votre projet. Cela crée un nouveau guide **MCP** non publié dans les Guides ou la Référence API de votre projet, sous une nouvelle catégorie appelée **SERVEUR MCP**. Le guide inclut des instructions prêtes à l'emploi pour se connecter à votre serveur MCP depuis des outils comme Cursor et Claude Desktop.

## Plans, tarification et prérequis

### Ai-je besoin d'un plan spécifique ou d'un module complémentaire pour utiliser MCP ?

Tous les projets ReadMe peuvent générer automatiquement un serveur MCP une fois MCP activé. Cependant, certaines fonctionnalités (comme les outils de documentation) nécessitent le module complémentaire **AI Booster Pack**. Les clients Enterprise doivent contacter leur CSM, et les clients Startup/Business peuvent effectuer la mise à niveau depuis leur page **Gérer le plan** dans les Paramètres.