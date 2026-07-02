---
title: Référence API
deprecated: false
hidden: false
metadata:
  robots: index
---
# Qu'est-ce qu'une référence API ?

Une référence API est le guide technique de référence de votre API, documentant chaque endpoint, paramètre et code de réponse en détail. C'est votre source de vérité ultime à laquelle les développeurs se tournent lorsqu'ils ont besoin de savoir exactement comment interagir avec votre API.

Dans ReadMe, votre référence API est une expérience interactive où les développeurs peuvent explorer votre API, effectuer des appels de test directement depuis la documentation et voir de vraies réponses sans écrire une seule ligne de code.

## Pourquoi votre référence API est importante

Une référence API bien conçue peut :

* **Réduire les tickets de support** en répondant aux questions techniques avant même qu'elles ne soient posées
* **Accélérer l'intégration des développeurs** en fournissant des conseils d'implémentation clairs et précis
* **Renforcer la confiance des développeurs** en montrant que votre API est conçue et maintenue avec soin
* **Mettre en valeur toutes les capacités de votre API** afin que les développeurs découvrent des fonctionnalités qu'ils auraient pu manquer

## Premiers pas avec votre référence API

ReadMe propose plusieurs façons de créer et de maintenir votre référence API, que vous travailliez avec des spécifications OpenAPI (anciennement Swagger) ou que vous préfériez construire votre référence manuellement.

### Dans cette section

Vous apprendrez à :

* **Télécharger et gérer des spécifications OpenAPI** via plusieurs méthodes
* **Utiliser notre API Designer** si vous ne disposez pas d'une spécification OpenAPI
* **Personnaliser votre référence API** pour correspondre à votre marque et améliorer l'utilisabilité
* **Créer des exemples interactifs** que les développeurs peuvent essayer directement dans votre documentation
* **Maintenir votre référence synchronisée** avec votre API réelle au fur et à mesure de son évolution

## Téléchargement et gestion OpenAPI

ReadMe prend entièrement en charge les spécifications OpenAPI 3.0, OpenAPI 3.1 et Swagger 2.0. Vous pouvez ajouter votre spécification API à ReadMe de plusieurs façons :

* **Téléchargement de fichier** : Glissez-déposez votre fichier JSON ou YAML OpenAPI/Swagger
* **Import par URL** : Indiquez à ReadMe l'emplacement en ligne de votre spécification
* **Intégration GitHub** : Connectez-vous directement à votre dépôt GitHub
* **Ligne de commande (rdme)** : Utilisez notre outil CLI pour des workflows automatisés
* **API Sync** : Maintenez votre référence API automatiquement synchronisée avec votre base de code

Une fois téléchargée, ReadMe transforme votre spécification en une documentation interactive et magnifiquement formatée que les développeurs adoreront.

## API Designer

Vous n'avez pas de spécification OpenAPI ? Pas de problème ! L'[API Designer](doc:building-apis-from-scratch-with-the-api-designer) de ReadMe vous permet de construire votre référence API de zéro grâce à une interface intuitive. Documentez vos endpoints, paramètres, corps de requête et objets de réponse sans avoir à écrire une seule ligne de YAML ou de JSON.

## Personnalisation de votre référence API

Faites de votre référence API quelque chose qui vous ressemble vraiment grâce aux options de personnalisation :

* Ajoutez des détails d'authentification et des en-têtes personnalisés
* Incluez des exemples de code dans plusieurs langages de programmation
* Organisez les endpoints en groupes logiques
* Ajoutez une documentation personnalisée et des aperçus à chaque groupe d'endpoints

## Support GraphQL

Vous travaillez avec GraphQL ? ReadMe offre un support limité mais croissant pour les [APIs GraphQL](doc:graphql). Vous pouvez documenter vos schémas, requêtes et mutations pour aider les développeurs à naviguer dans votre API GraphQL.

## Bonnes pratiques pour les références API

Pour créer une référence API exceptionnelle :

* **Soyez exhaustif** : Documentez chaque endpoint, paramètre et réponse
* **Incluez des exemples** : Montrez de vraies paires requête/réponse pour les cas d'usage courants
* **Expliquez les erreurs** : Documentez tous les codes d'erreur et comment les résoudre
* **Restez à jour** : Mettez à jour la documentation à chaque modification de votre API
* **Testez vous-même** : Utilisez régulièrement votre propre documentation pour détecter les problèmes