---
title: Créer une Recette
deprecated: false
hidden: false
metadata:
  robots: index
---
# Aperçu

Prêt à transformer vos exemples de code en expériences d'apprentissage conviviales pour les développeurs ? Ce guide vous accompagne dans la création de votre première Recette, de A à Z. Vous apprendrez à décomposer du code complexe en étapes digestes, à ajouter des annotations utiles et à personnaliser l'expérience visuelle pour qu'elle corresponde à votre marque.

<br />

<Image align="center" border={false} src="https://files.readme.io/05e72a5519ad6e9421775f6688bbee366623e93528abf9df93dd5ae1973b81dd-Screenshot_2025-05-22_at_2.16.36_PM.png" />

<br />

## Avant de commencer

* Ayez votre exemple de code prêt (ou sachez quel endpoint d'API vous souhaitez utiliser comme point de départ)
* Assurez-vous que la section Recettes est accessible dans votre projet ReadMe
* Réfléchissez aux langages de programmation que vos développeurs utilisent le plus
* Pensez aux objectifs d'apprentissage clés de cette présentation de code

## Créer une Recette

<Image border={false} src="https://files.readme.io/4482047-Screen_Shot_2020-12-01_at_3.42.35_PM.png" />

### 1. Accéder à l'éditeur de Recettes

Accédez à votre projet ReadMe et cliquez sur **Modifier** pour entrer dans l'interface d'édition. Dans la navigation principale, sélectionnez **Recettes** pour accéder à la zone de gestion des Recettes. Cliquez sur le bouton **Créer une nouvelle Recette** pour lancer le générateur de Recettes.

<Image align="center" border={false} src="https://files.readme.io/139f1a2224d1add344a0071284be7614929b7cac5be5babf7cb0860b16b9f81e-Screenshot_2025-05-22_at_12.47.08_PM.png" />

### 2. Configurer votre exemple de code

1. Dans le panneau supérieur droit, sélectionnez votre langage de programmation dans le menu déroulant.
2. Ajoutez votre exemple de code et assurez-vous qu'il est correctement formaté avec la coloration syntaxique. Ce sera la base à laquelle vos annotations étape par étape feront référence.

<Image align="center" border={false} src="https://files.readme.io/91f78f372bffaf5521f48ba6972275b5d3fa1b74cf4b4f917a5d7284a6d51c11-Screenshot_2025-05-22_at_2.09.51_PM.png" />

**Remarque :** Chaque Recette peut prendre en charge plusieurs langages de programmation, vous pouvez donc ajouter des versions dans d'autres langages après avoir configuré la première.

### 3. Créer vos annotations étape par étape

Dans la barre latérale gauche, créez vos étapes mises en évidence qui guideront les développeurs à travers votre code. Pour chaque étape :

* Rédigez un titre clair et descriptif qui explique ce que cette partie du code accomplit
* Ajoutez des explications détaillées qui aident les développeurs à comprendre le « pourquoi » de chaque section
* Indiquez les numéros de ligne qui doivent être mis en évidence pour cette étape
* Utilisez un langage accessible qui rend les concepts complexes compréhensibles

Chaque étape doit se concentrer sur un concept ou une action spécifique dans votre exemple de code, en construisant la compréhension progressivement.

<Image border={false} src="https://files.readme.io/cece453-Screen_Shot_2020-12-01_at_3.49.54_PM.png" />

### **4. Ajouter des exemples de réponses**

Dans le panneau inférieur droit, incluez la réponse API attendue lorsque votre code s'exécute avec succès. Cela montre aux développeurs exactement à quoi ressemble le succès et les aide à vérifier leur implémentation.

Si votre code ne génère pas de réponse (ou si en afficher une n'est pas pertinent), vous pouvez laisser cette section vide — elle se masquera automatiquement dans la Recette finale.

**Remarque :** Les variables de données utilisateur fonctionnent aussi dans les Recettes ! Si vous avez configuré des docs personnalisées, vous pouvez inclure du contenu dynamique dans vos réponses.

> 👍 Les variables de données utilisateur fonctionnent dans les Recettes !
>
> Si vous avez des [variables](doc:personalized-docs) dans votre documentation, par exemple transmises via le Webhook de Docs Personnalisées, elles fonctionneront aussi dans les Recettes !

### 5. Personnaliser l'apparence visuelle

Passez à l'onglet **Apparence** pour rendre votre Recette unique :

* **Sélectionner un emoji** : Cliquez sur l'icône emoji pour choisir dans le menu déroulant
* **Définir la couleur d'arrière-plan** : Utilisez le sélecteur de couleur pour choisir un arrière-plan correspondant à votre marque (prend en charge les valeurs RGB, HSL ou HEX)
* **Rédiger une description** : Ajoutez une description détaillée qui apparaîtra sur la carte Recette dans votre section Recettes

La couleur du bouton _Ouvrir la Recette_ hérite automatiquement des paramètres de couleur de lien de votre projet.

<Image border={false} src="https://files.readme.io/ea6500f-Screen_Shot_2020-10-19_at_12.41.19_PM.png" />

### **6. Choisir les emplacements d'intégration**

Décidez où votre Recette doit apparaître dans votre documentation :

* **Intégration dans la référence API** : Sélectionnez les endpoints spécifiques où cette Recette fournit un contexte pertinent
* **Section Recettes** : Votre Recette apparaîtra automatiquement dans la zone principale des Recettes une fois publiée
* **Intégration dans les guides** : Vous pouvez intégrer manuellement la Recette dans des pages de guide ultérieurement à l'aide du widget Recette

Cochez les cases à côté des endpoints pertinents pour rendre votre Recette accessible exactement là où les développeurs en ont le plus besoin.

La Recette apparaîtra sous forme de carte cliquable comme indiqué dans la zone d'aperçu de l'étape Apparence.

<Image border={false} src="https://files.readme.io/20cf1e2-Screen_Shot_2020-12-03_at_5.14.16_PM.png" />

<br />

<Image border={false} src="https://files.readme.io/e4619b5-Screen_Shot_2020-12-01_at_2.59.43_PM.png" />

<br />

<Callout icon="🚧" theme="warn">
  Les intégrations n'apparaîtront pas dans la section Référence [tant que la section Recettes n'est pas activée](#enable-recipes-section).
</Callout>

<br />

### 7. Définir le statut de publication

Choisissez le niveau de visibilité de votre Recette :

* **Non publiée** : Visible uniquement par les administrateurs du projet (par défaut pour les nouvelles Recettes)
* **Publiée** : Visible par tous les utilisateurs dans votre collection de Recettes
* **En vedette** : Mise en avant en haut de votre section Recettes (une seule Recette peut être en vedette à la fois)

Commencez avec « Publiée » pour rendre votre Recette disponible aux développeurs, ou gardez-la « Non publiée » pendant que vous affinez encore le contenu.

|                 |                                                                                                                                                                                          |
| :-------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **En vedette**  | Il s'agit de la Recette mise en avant en haut de la section Recettes. Une Recette doit être en vedette si votre page Recettes est publique, et elle doit être dans un état publié.       |
| **Publiée**     | Visible par les utilisateurs dans la grille de cartes sous la Recette en vedette                                                                                                         |
| **Non publiée** | Ne peut pas être vue par les clients. Les nouvelles Recettes sont non publiées par défaut.                                                                                               |

<Image border={false} src="https://files.readme.io/445d0c8-Screen_Shot_2020-12-16_at_3.54.22_PM.png" />

<br />

## FAQ et dépannage

**Puis-je supprimer l'icône Recette dans la barre de navigation ?**

Cette section n'est visible que par les administrateurs du projet. Vos clients ne verront pas cette section à moins que vous ne l'[activiez](#enabling-your-recipes-page) pour la rendre visible.

À mesure que nous transférons davantage de fonctionnalités d'édition vers le frontend de votre hub de documentation, nous continuerons à clarifier ce que voient les administrateurs de projet par rapport à ce que voient vos clients.

**Comment changer la couleur du bouton bleu « Ouvrir la Recette » ?**

La couleur de ce bouton est héritée de la couleur de lien que vous avez définie dans l'[Éditeur de thème](/main/docs/design-themes) dans les paramètres de votre projet. Pour la modifier, vous devrez changer la couleur de lien pour l'ensemble de votre hub ReadMe.

**Puis-je renommer la section Recettes comme les autres sections ?**

Pas encore, mais nous y travaillons !

**La mise en évidence de mon code ne fonctionne pas correctement ?** Vérifiez que vos numéros de ligne sont exacts et que vous avez sélectionné le bon langage de programmation. N'oubliez pas que les numéros de ligne commencent à 1, pas à 0.

**Le widget Recette n'apparaît pas dans mes guides ?** Assurez-vous que la section Recettes est activée dans les paramètres de navigation de votre site. Le widget ne sera pas disponible tant que les Recettes ne sont pas activées pour votre projet.

**Ma Recette intégrée n'apparaît pas dans les pages de référence API ?** Les Recettes intégrées n'apparaissent qu'une fois que la section Recettes est publiquement activée. Vérifiez les paramètres de navigation de votre site et assurez-vous qu'au moins une Recette est publiée.

**La section de réponse a disparu ?** Si vous effacez complètement le contenu de réponse par défaut, le panneau de réponse se masquera automatiquement. Ajoutez du contenu pour le rendre à nouveau visible.