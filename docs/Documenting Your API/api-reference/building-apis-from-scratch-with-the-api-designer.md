---
title: Créer des API de zéro avec l'API Designer
deprecated: false
hidden: false
metadata:
  robots: index
---
# Vue d'ensemble

Pas de spécification OpenAPI ? Pas de problème ! L'API Designer de ReadMe vous permet de créer votre référence API directement dans la plateforme grâce à une interface visuelle intuitive – sans YAML ni JSON.

Dans ce guide, nous allons créer une API de réseau social avec des endpoints pour lister et créer des publications. Vous verrez à quel point il est facile de documenter votre API même en partant de zéro.

## Créer votre définition d'API

Commençons par mettre en place la structure de base de votre API :

1. Accédez à **API Reference** dans votre projet ReadMe
2. Cliquez sur le bouton **+ Add**
3. Sélectionnez **Start Building** sous « Build an API definition from scratch »

<Image align="center" border={false} src="https://files.readme.io/f9e241f98e3e8ad91e999561f4e3b4dfe260a8e6a18662e23da840887977b6c7-CleanShot_2025-03-11_at_11.18.13.gif" />

4. Saisissez les détails de votre définition d'API :
   * **API Title** : Entrez un nom descriptif (ex. : « Social Media API »)
   * **Target Host URL** : L'URL de base de votre API (ex. : « [http://api.example.com](http://api.example.com) »)
   * **Authentication Type** : Sélectionnez votre méthode d'authentification (None, API Key, Basic ou Bearer)

<Image align="center" border={false} src="https://files.readme.io/7a81519f9faf96f4af361d26c405792fe78488558a9c8e972d084d102dda098e-CleanShot_2025-03-11_at_11.21.07.gif" />

5. Cliquez sur **Save** pour créer votre définition d'API

Votre nouvelle définition d'API apparaîtra dans le panneau de navigation de gauche, prête à recevoir vos endpoints.

## Créer votre premier endpoint (Lister les publications du réseau social)

Créons un endpoint pour récupérer une liste de publications de réseau social :

1. Dans la navigation de gauche, vous verrez un endpoint par défaut intitulé `/new-endpoint`
2. Renommez-le pour mieux refléter la structure de votre API – appelons-le « Posts »
3. Vous verrez maintenant cette catégorie dans votre navigation de gauche

<Image align="center" border={false} src="https://files.readme.io/fc908c66586d12aa0327f1bc17d60a045a23e550e82161ae4818a37eb91b3931-CleanShot_2025-03-11_at_11.29.12.gif" />

4. Créez votre endpoint GET pour lister les publications :
   * Cliquez sur l'endpoint pour le modifier
   * Changez le titre en « List Social Media Posts »
   * Sélectionnez la méthode **GET** dans le menu déroulant
   * Définissez le chemin sur `/posts`
   * Ajoutez une description expliquant ce que fait l'endpoint (ex. : « Returns a paginated list of social media posts »)

<Image align="center" border={false} src="https://files.readme.io/72e65717ef6534caa7b0d2a187deb7125b1466bc72a95a8fdcd7459267ae8b35-CleanShot_2025-03-11_at_11.31.27.gif" />

### Ajouter des paramètres de requête

La plupart des endpoints de liste prennent en charge la pagination ou le filtrage. Ajoutons quelques paramètres de requête :

1. Repérez la section **Query Parameters** et cliquez sur le bouton **+**
2. Ajoutez des paramètres pour la pagination :
   * Ajoutez un paramètre `page` de type `integer`
   * Ajoutez un paramètre `limit` de type `integer`
   * Ajoutez d'autres paramètres de filtrage si nécessaire (ex. : `category` en tant que `string`)
3. Pour chaque paramètre :
   * Ajoutez une description
   * Indiquez s'il est obligatoire
   * Fournissez une valeur par défaut si applicable

<Image align="center" border={false} src="https://files.readme.io/c596d7f09014adbfb1166f81b10936c0427f6b0e4a4c1cc9f2983a51c55aaa55-CleanShot_2025-03-11_at_11.35.30.gif" />

<br />

## Créer votre deuxième endpoint (Créer une publication sur le réseau social)

Ajoutons maintenant un endpoint pour créer de nouvelles publications :

1. Dans la navigation de gauche, cliquez sur le bouton **+ New Category** si vous avez besoin d'une nouvelle catégorie, ou utilisez votre catégorie « Posts » existante
2. Cliquez sur l'icône + pour ajouter un nouvel endpoint
3. Configurez votre endpoint POST :
   * Titre : « Create New Post »
   * Méthode : Sélectionnez **POST** dans le menu déroulant
   * Chemin : `/posts`
   * Description : « Allows authenticated users to create new posts »

<Image align="center" border={false} src="https://files.readme.io/fa7c7a03010f8fdbc0bee4ff32db7a11e34f723f3640ed6e3f311234e93dd2bd-CleanShot_2025-03-11_at_11.52.25.gif" />

### Ajouter des paramètres au corps de la requête

Pour un endpoint POST, vous devez définir le corps de la requête :

1. Repérez la section **Request Body** et cliquez pour la développer
2. Définissez le type de contenu sur `object`
3. Ajoutez les champs obligatoires :
   * Ajoutez un champ `content` de type `string` et marquez-le comme obligatoire
   * Ajoutez tout champ supplémentaire accepté par votre API (ex. : `image_url`, `tags`)
4. Pour chaque champ :
   * Ajoutez une description claire
   * Indiquez s'il est obligatoire
   * Précisez les contraintes éventuelles (longueur min/max, pattern, etc.)

<Image align="center" border={false} src="https://files.readme.io/2a114a0bb8cfab72df455ea87638aa51d75a1ea3b931987fc18d1450f94cb08d-CleanShot_2025-03-11_at_11.57.21.gif" />

### Ajouter des exemples de code de requête

L'une des fonctionnalités puissantes de ReadMe est la génération automatique d'exemples de code :

1. Repérez la section **Request Code** sur la droite
2. ReadMe génère automatiquement des exemples de code dans plusieurs langages
3. Vous pouvez également cliquer sur « Write your own static samples » pour ajouter des exemples personnalisés

<Image align="center" border={false} src="https://files.readme.io/646ce4e3467087d3d7b8396632e29af646bf02be9113054d0c63e69c14561a6c-CleanShot_2025-03-11_at_12.03.35.gif" />

<br />

## Tester votre documentation API

Après avoir créé vos endpoints :

1. Enregistrez vos modifications
2. Basculez en mode « View » pour voir à quoi ressemble votre documentation pour les développeurs
3. Testez les fonctionnalités interactives pour vous assurer que vos exemples fonctionnent correctement

## Conseils pour une excellente documentation API

* **Soyez exhaustif dans vos descriptions** : Expliquez clairement ce que fait chaque endpoint et pourquoi
* **Fournissez des exemples réalistes** : Utilisez des données d'exemple qui ressemblent à une utilisation réelle
* **Documentez les états d'erreur** : Incluez des exemples de réponses d'erreur et la façon de les gérer
* **Utilisez une nomenclature cohérente** : Maintenez un style cohérent sur tous les endpoints et paramètres
* **Ajoutez une section « What's Next »** : Utilisez la section « What's Next » pour guider les utilisateurs vers les endpoints connexes dont ils pourraient avoir besoin

En suivant ce guide, vous avez créé une référence API bien documentée de zéro à l'aide de l'API Designer de ReadMe. Vos développeurs disposent désormais d'une documentation interactive et claire qui les aide à intégrer votre API rapidement et facilement.

N'oubliez pas que vous pouvez toujours revenir à l'API Designer pour ajouter des endpoints, mettre à jour des paramètres ou enrichir votre documentation au fur et à mesure que votre API évolue.

<br />

## Fonctionnalités OpenAPI actuellement non prises en charge dans l'API Designer

Nous ne prenons actuellement pas en charge toutes les fonctionnalités OpenAPI dans notre API Designer. Si vous utilisez l'une de ces fonctionnalités dans un endpoint, vous ne pourrez pas le modifier dans notre interface. Cependant, ces endpoints s'afficheront correctement dans la documentation et pourront toujours être mis à jour en modifiant directement le fichier OpenAPI.

<br />

| Fonctionnalité OpenAPI non prise en charge | Explication                                                                                                                                                                                                                                                    | Documentation OpenAPI                                                                                                                      |
| ------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| Additional Properties                      | Le mot-clé additionalProperties est utilisé dans un schéma pour définir si des propriétés non explicitement définies dans le schéma sont autorisées dans les objets, et si oui, quels doivent être leurs types.                                                | [Dictionaries, HashMaps and Associative Arrays](https://swagger.io/docs/specification/v3_0/data-models/dictionaries/)                      |
| Callbacks/Webhooks                         | OpenAPI dispose d'une fonctionnalité permettant de définir des endpoints qui effectueront un appel API une fois qu'un événement est terminé.                                                                                                                   | [Callbacks](https://swagger.io/docs/specification/v3_0/callbacks/)                                                                         |
| References                                 | Tout endpoint qui définit un objet à l'aide d'un $ref.                                                                                                                                                                                                         | [Using Ref](https://swagger.io/docs/specification/v3_0/using-ref/)                                                                         |
| Common Parameters                          | Endpoints dont les paramètres sont définis au niveau du chemin plutôt que de la méthode, de sorte que les paramètres sont partagés entre toutes les méthodes pour cette URL.                                                                                   | [Describing Parameters](https://swagger.io/docs/specification/v3_0/describing-parameters/#common-parameters)                               |
| Links                                      | Les liens sont une fonctionnalité OpenAPI qui décrit comment les réponses d'un endpoint peuvent être utilisées comme entrée pour d'autres opérations.                                                                                                          | [Links](https://swagger.io/docs/specification/v3_0/links/)                                                                                 |
| Polymorphism                               | Le polymorphisme vous permet de définir un schéma pouvant représenter plusieurs types ou modèles.                                                                                                                                                              | [Inheritance and Polymorphism](https://swagger.io/docs/specification/v3_0/data-models/inheritance-and-polymorphism/?sbsearch=Polymorphism) |
| Server Variables                           | Des variables peuvent être définies dans le chemin de base et peuvent avoir une liste prédéfinie de valeurs parmi lesquelles l'utilisateur peut choisir.                                                                                                       | [API Server and Base Path](https://swagger.io/docs/specification/v3_0/api-host-and-base-path/?sbsearch=server%20variables)                 |
| Style                                      | Le mot-clé Style permet de configurer la façon dont plusieurs valeurs doivent être transmises à un paramètre.                                                                                                                                                  | [Parameter Serialization](https://swagger.io/docs/specification/v3_0/serialization/?sbsearch=Styles)                                       |
| XML                                        | Endpoints qui acceptent ou répondent avec des données XML.                                                                                                                                                                                                     | [Representing XML](https://swagger.io/docs/specification/v3_0/data-models/representing-xml/?sbsearch=xml)                                  |