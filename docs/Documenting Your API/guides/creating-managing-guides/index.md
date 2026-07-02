---
title: Créer et gérer des guides
deprecated: false
hidden: false
metadata:
  robots: index
---
# Vue d'ensemble

Plongeons dans les détails de l'organisation de votre documentation dans ReadMe. De la création de nouveaux guides à la gestion du contenu au fil du temps, ce guide vous montrera comment construire et maintenir une base de connaissances bien structurée qui aide les développeurs à trouver exactement ce dont ils ont besoin, au moment où ils en ont besoin.

### Pourquoi les guides sont importants

Les guides constituent l'épine dorsale de votre documentation développeur. Tandis que votre référence API indique aux développeurs ce qui est possible, les guides leur montrent comment réussir. De bons guides :

* Accompagnent les développeurs du niveau débutant à expert
* Fournissent un contexte que les références API ne peuvent pas capturer
* Répondent au « pourquoi » en même temps qu'au « comment »
* Résolvent les problèmes concrets rencontrés par les développeurs

## Créer votre premier guide

### Créer des catégories 📂

Les catégories vous aident à organiser votre documentation en sections logiques, fonctionnant comme des chapitres dans l'histoire de votre API. Chaque catégorie crée une rupture naturelle dans le récit de votre documentation, facilitant ainsi le suivi pour les développeurs.

1. Accédez à votre hub de documentation et basculez en **Mode Édition**.
2. Cliquez sur le bouton **+ NOUVELLE CATÉGORIE** dans la navigation latérale.
3. Saisissez un nom pour votre catégorie (par ex., « Démarrage » ou « Sujets avancés »)
4. Cliquez sur **Entrée** pour enregistrer.

> 📘 Expérience utilisateur
>
> Pensez au parcours de votre développeur lors de la dénomination des catégories. Qu'est-ce qui aurait le plus de sens pour quelqu'un qui explore votre API pour la première fois ? Envisagez d'organiser les catégories par niveau de compétence (débutant à avancé) ou par cas d'utilisation.

### Créer une page de guide 📝

Maintenant que vos catégories sont configurées, ajoutons quelques pages :

1. En mode **Édition**, survolez une catégorie et cliquez sur le bouton **+**
2. Remplissez les détails essentiels :
   * **Titre** : Rendez-le clair et descriptif
   * **Slug** : Ce sera le chemin URL (généré automatiquement, mais vous pouvez le personnaliser)
   * **Masqué** : Activez cette option si vous souhaitez travailler sur le guide avant de le rendre public
3. Cliquez sur **Enregistrer** pour créer votre nouveau guide

### Utiliser l'interface d'édition ✏️

<Image align="left" border={false} width="50% " src="https://files.readme.io/53c229bb50f36b2a6398894e5de72e9909397911c2deba6c77e629733e714a99-Editing_UI_-_view_to_edit_toggle.gif" />

<br />

<br />

<br />

<br />

<br />

<br />

Avec l'interface d'édition de ReadMe, vous créez et modifiez du contenu directement sur votre hub. Cela signifie que ce que vous voyez est exactement ce que vos développeurs verront.

1. Après avoir créé votre page, vous serez automatiquement dans l'éditeur
2. Utilisez la barre d'outils de mise en forme pour le style de texte de base
3. Tapez `/` pour accéder au menu de commandes permettant d'insérer :
   * Des blocs de code
   * Des encadrés
   * Des images
   * Et bien plus encore !
4. Basculez entre les modes **Édition** et **Aperçu** pour voir exactement comment votre contenu apparaîtra aux développeurs

<Image align="center" border={false} src="https://files.readme.io/a106664539184b9eebb366fd2c51ed5ba10ca5c1224c0ce52a209dd8c08ac143-CleanShot_2024-11-08_at_20.24.59.gif" />

> 📘 Contrôle total de votre Markdown
>
> Le mode Raw de ReadMe vous permet d'ajouter du nouveau contenu et de modifier le contenu existant directement en Markdown. Ouvrez simplement le menu à trois points à côté des paramètres de visibilité et choisissez **Mode Raw**.

## Structurer des guides efficaces

### L'anatomie d'un excellent guide

Les guides réussis suivent une structure cohérente qui aide les développeurs à comprendre et à appliquer rapidement les informations :

1. **Introduction claire** : Quel problème ce guide résout-il ?
2. **Prérequis** : Que doivent savoir ou avoir les développeurs avant de commencer ?
3. **Instructions étape par étape** : Décomposez les processus complexes en étapes gérables
4. **Exemples de code** : Montrez, ne vous contentez pas de dire
5. **Dépannage** : Traitez les problèmes courants et leurs solutions
6. **Prochaines étapes** : Où les développeurs doivent-ils aller après avoir terminé ce guide ?

### Écrire pour les développeurs

Lorsque vous rédigez des guides, rappelez-vous que les développeurs veulent résoudre les problèmes rapidement :

* **Soyez concis** : Allez droit au but et évitez les explications inutiles
* **Utilisez abondamment des exemples de code** : Les développeurs comprennent souvent le code plus vite que la prose
* **Mettez en évidence les informations importantes** : Utilisez des encadrés pour les avertissements, conseils et notes importantes
* **Aérez le texte** : Utilisez des titres, des listes et des paragraphes courts pour améliorer la lisibilité
* **Utilisez des exemples concrets** : Montrez du code qui résout de vrais problèmes

> 📘 Restez concret
>
> Utilisez des exemples de code authentiques qui illustrent des implémentations réalistes. Si vous montrez l'authentification, utilisez un exemple complet avec gestion des erreurs. Si vous démontrez la récupération de données, montrez comment traiter et utiliser ces données de manière pratique. Les exemples concrets aident les développeurs à combler le fossé entre la documentation et l'implémentation.

```javascript
// Good example - with meaningful comments and clear variable names
const apiKey = 'your_api_key_here';

// Initialize the client with your API key
const client = new ReadMeAPI(apiKey);

// Fetch user data and handle potential errors
try {
  const userData = await client.getUser(userId);
  console.log(`Found user: ${userData.name}`);
} catch (error) {
  console.error(`Error fetching user: ${error.message}`);
}
```

## Enrichir les guides avec MDX

ReadMe prend désormais en charge MDX (Markdown + JSX), vous donnant le pouvoir de créer une documentation interactive avec des composants réutilisables.

### Composants MDX de base

Voici un exemple de nos composants MDX d'onglets intégrés que vous pouvez utiliser pour enrichir vos guides :

<Tabs>
  <Tab title="Node.js">
    ```javascript
    const client = new ReadMeAPI(apiKey);
    ```
  </Tab>

  <Tab title="Python">
    ```python
    client = ReadMeAPI(api_key)
    ```
  </Tab>

  <Tab title="Ruby">
    ```ruby
    client = ReadMeAPI.new(api_key)
    ```
  </Tab>
</Tabs>

### Créer du contenu réutilisable

Pour le contenu que vous utiliserez dans plusieurs guides, [créez des blocs de contenu réutilisables](doc:reusable-content)

1. Accédez aux **Paramètres de contenu** dans l'interface d'édition
2. Sélectionnez **Contenu réutilisable**
3. Créez des blocs pour les éléments courants tels que :
   * Les étapes d'authentification API
   * Les instructions de configuration de l'environnement
   * Les modèles de code standard
4. Insérez-les dans n'importe quel guide avec la commande `/`

## Organiser votre documentation

### Créer une stratégie de documentation

Avant de vous lancer dans des guides individuels, réfléchissez à la structure globale de votre documentation :

1. **Cartographiez le parcours développeur** : Quel chemin les développeurs empruntent-ils de la première inscription à l'utilisation avancée ?
2. **Identifiez les lacunes de connaissances** : Où les développeurs se retrouvent-ils généralement bloqués ?
3. **Créez des parcours d'apprentissage progressifs** : Comment chaque guide peut-il s'appuyer sur les connaissances précédentes ?

### Types de guides à envisager

Différents guides servent différents objectifs :

* **Démarrage** : Intégration des nouveaux développeurs
* **Tutoriels** : Instructions étape par étape pour des tâches spécifiques
* **Guides conceptuels** : Explication d'idées complexes ou d'architectures
* **Guides pratiques** : Instructions ciblées pour des fonctionnalités spécifiques
* **Dépannage** : Solutions aux problèmes courants

## Maintenir les guides dans le temps

### Garder le contenu à jour

La documentation nécessite une maintenance régulière :

1. Planifiez des cycles de révision réguliers (trimestriels, c'est bien)
2. Mettez à jour les guides, et votre journal des modifications, lorsque les fonctionnalités changent
3. Surveillez les retours des utilisateurs qui indiquent une confusion
4. Analysez les statistiques pour voir quels guides nécessitent des améliorations

### Considérations sur le versionnage

Si votre API comporte plusieurs versions :

1. Utilisez la fonctionnalité de versionnage de ReadMe pour maintenir des ensembles de documentation séparés
2. Indiquez clairement les informations spécifiques à chaque version
3. Envisagez d'utiliser des encadrés pour mettre en évidence les différences entre les versions

## Collaborer avec l'intégration Git

Avec la [synchronisation Git bidirectionnelle](doc:bi-directional-sync) de ReadMe, vous pouvez désormais collaborer sur la documentation en utilisant les workflows Git familiers :

1. Connectez votre projet ReadMe à GitHub/GitLab
2. Modifiez les fichiers de documentation directement dans votre dépôt
3. Les modifications se synchronisent automatiquement avec votre projet ReadMe
4. Utilisez les pull requests et les révisions pour les modifications de documentation

## Mesurer le succès

### Utiliser les analyses

ReadMe fournit des informations sur la façon dont les développeurs utilisent votre documentation :

1. Surveillez les pages vues pour identifier les guides populaires
2. Suivez les requêtes de recherche pour trouver les informations manquantes
3. Utilisez ces données pour prioriser les améliorations de la documentation

### Recueillir des retours

Créez des boucles de rétroaction pour vous améliorer continuellement :

1. Activez les discussions sur les guides
2. Examinez régulièrement les questions et commentaires
3. Mettez à jour les guides en fonction des questions fréquentes

## Prochaines étapes

Maintenant que vous savez comment créer et gérer des guides dans ReadMe, essayez :

* Créer votre première catégorie et votre premier guide
* Expérimenter avec les composants MDX
* Mettre en place un processus de révision de la documentation
* Connecter votre documentation à GitHub pour une édition collaborative

Besoin d'aide supplémentaire ? Consultez nos autres ressources :

* [Documentation MDX](doc:mdx)
* [Configuration de la synchronisation bidirectionnelle](doc:bi-directional-sync)