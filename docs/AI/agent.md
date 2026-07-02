---
title: Agent
deprecated: false
hidden: false
metadata:
  robots: index
---
L'Agent est un puissant assistant de documentation qui vous aide à créer, modifier et enrichir du contenu dans les Guides, les Références API et les Pages personnalisées, grâce à des capacités avancées de recherche et d'analyse.

## Ce qu'il peut faire

L'Agent offre une assistance complète pour la documentation :

* **Création et modification de contenu** : Rédiger, réécrire, traduire et corriger la grammaire avec une mise en forme markdown appropriée
* **Recherche et analyse** : Effectuer des recherches sur le web, analyser des URL et récupérer des informations depuis votre documentation
* **Composants intelligents** : Suggérer et implémenter les composants MDX intégrés de ReadMe
* **Flux de travail en plusieurs étapes** : Combiner recherche, analyse et création de contenu en une seule requête
* **Correction des erreurs de linter** : Résoudre les erreurs de syntaxe et les avertissements conformément à votre guide de style configuré

## Utilisation

L'Agent excelle dans les tâches de documentation complexes et en plusieurs étapes. Vous pouvez formuler des requêtes telles que :

* « Rechercher les dernières tendances en matière de conception d'API et créer un guide »
* « Analyser cette URL et ajouter les points clés à notre documentation »
* « Trouver les informations d'authentification dans nos docs et développer cette section »

Chaque session de chat conserve le contexte complet de votre page actuelle et des fichiers de spécification OpenAPI. Toutes les conversations sont privées et liées à votre compte. Utilisez le modèle sélectionné automatiquement ou choisissez votre propre modèle dans la liste préconfigurée.

<Image align="center" border={false} src="https://files.readme.io/f678000604c17fb27accb05314a554ec94cf776d81f91701f4ed479db7e6b551-agent_mini.png" />

### Poser des questions sur ReadMe

Posez à l'Agent des questions relatives à ReadMe pour naviguer rapidement sur notre plateforme pendant que vous travaillez sur votre documentation. Il s'appuie sur notre base de connaissances pour répondre à vos questions et vous guider à travers les fonctionnalités, les outils et les bonnes pratiques.

## Configurer

Aidez l'Agent à mieux travailler pour vous :

* Si certains modèles ne sont pas compatibles avec votre documentation, désactivez-les dans les paramètres du Chat IA (<i class="fa-regular fa-solid fa-gear" color="var(--gray80" />).
* Pour améliorer les réponses de l'Agent, indexez votre base de code pour fournir un contexte supplémentaire ou ajoutez du contenu personnalisé.

<Image align="center" border={false} width="350px" src="https://files.readme.io/5525b67a2ebb59fdfefbdc82f8c8b88f86f6cf3ba9b03c6c5b927d5acb8a499d-agent_settings_2.png" />

<br />

## FAQ

<Accordion title="Quel LLM alimente l'agent ?" icon="fa-robot">
  L'Agent est alimenté par des modèles de langage avancés, notamment Google Gemini Pro 2.5, Claude et les modèles OpenAI, offrant des capacités avancées de raisonnement et de recherche.
</Accordion>

<Accordion title="Mes données sont-elles partagées avec le LLM ?" icon="fa-shield-alt">
  Uniquement lorsque vous utilisez la fonctionnalité Agent. Si vous ne l'utilisez pas, aucune donnée n'est partagée. Lorsqu'elle est activée, la page que vous consultez actuellement et la documentation pertinente sont incluses dans le prompt envoyé au modèle de langage pour générer une réponse.
</Accordion>

<Accordion title="Peut-il accéder à des sites web externes ?" icon="fa-globe">
  Oui ! L'Agent peut effectuer des recherches sur le web et analyser des URL pour enrichir votre documentation.
</Accordion>

<Accordion title="Comment accède-t-il à mes docs existants ?" icon="fa-search">
  Il peut effectuer des recherches dans la documentation de votre projet et dans vos sources de connaissances pour trouver et intégrer les informations pertinentes.
</Accordion>