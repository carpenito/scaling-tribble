---
title: Composants personnalisés
deprecated: false
hidden: false
metadata:
  robots: index
---
Créez et gérez des composants MDX personnalisés depuis la page **Composants personnalisés** dans **Paramètres**. Au fur et à mesure que vous construisez, vous écrirez du code JSX et verrez un aperçu en direct de votre composant en temps réel. Une fois enregistrés, vous pouvez accéder à vos composants depuis le menu `<` et les réutiliser dans toute votre documentation.

### Principaux avantages

* Transformez les modèles courants en composants réutilisables pour garantir la cohérence, simplifier la maintenance et créer une interface utilisateur unifiée dans vos docs.
* Personnalisez le contenu en fonction du public, du cas d'utilisation ou du niveau d'accès _sans_ dupliquer les pages.
* Adaptez les composants à votre produit et faites ressortir votre documentation.
* Ajoutez de l'interactivité à vos docs avec des composants qui font bien plus qu'afficher du contenu.

## Marketplace

Parcourez le Marketplace pour explorer des composants open source développés par la communauté. Chaque composant est examiné par ReadMe pour en vérifier la qualité et la conformité. Sélectionnez simplement un composant, apportez les modifications nécessaires ou utilisez-le tel quel — puis enregistrez-le pour commencer à l'intégrer dans votre documentation.

<Image align="center" border={false} src="https://files.readme.io/4878ee5ee5a98ad931898ff6a4638d3f79ea3f57c90296bcc65b0623d58c5219-Screenshot_2025-09-04_at_4.29.16_PM.png" />

<Callout icon="💡" theme="default">
  **Vous vous sentez créatif ?** Contribuez le vôtre ! Ouvrez une pull request dans le [dépôt GitHub](https://github.com/readmeio/marketplace). Une fois fusionné, voyez votre composant en direct dans le Marketplace et contribuez à enrichir la bibliothèque pour tout le monde.
</Callout>

***

## Créez votre premier composant

Voyons comment créer un composant personnalisé simple mais utile. Nous allons construire un composant « Note » qui met en valeur les informations importantes dans vos docs.

```jsx
export const ExampleComponent = props => {
  return (
    <div className="flex items-center h-full w-full">
      <div className="bg-gray-800 rounded-md p-6 m-4">
        {props.children}
      </div>
    </div>
  );
};

<ExampleComponent>
  Here's a very simple example component rather than an empty state. This should help you figure out what's happening quicker and see what's possible with custom components!
</ExampleComponent>
```

### Comprendre le code

<Image align="center" border={false} src="https://files.readme.io/e6e6aa810d1cd0f55f001261284d475c244902bd3bd14b46e98a6b15ac2680e4-CleanShot_2025-02-24_at_12.57.54.gif" />

**Ligne 1 :** `export const ExampleComponent = props => {`

* Ici, nous définissons un nouveau composant appelé `ExampleComponent`
* Le mot-clé `export` est requis pour définir toute variable ou composant en MDX
* Nous pouvons accéder aux `props` React pour afficher les attributs ou le contenu ajoutés à la balise du composant

**Lignes 2-8 :** La structure du composant

* `return (...)` définit ce que le composant affichera lors de son utilisation
* Le `<div>` externe utilise les [classes Tailwind](https://tailwindcss.com/docs/styling-with-utility-classes) pour centrer son contenu (`flex items-center`) et occuper toute la largeur et la hauteur (`h-full w-full`)
* Le `<div>` interne crée une boîte gris foncé (`bg-gray-800`) avec des coins arrondis (`rounded-md`) et des espacements (`p-6 m-4`)
* `{props.children}` est l'ingrédient magique — il affiche le contenu que vous placez entre les balises de votre composant

<Callout icon="💁" theme="default">
  ### Une remarque rapide sur Tailwind CSS

  Ne vous inquiétez pas si ces classes vous semblent inconnues ! Vous pouvez consulter la [documentation officielle de Tailwind CSS](https://tailwindcss.com/docs/styling-with-utility-classes) pour un guide complet sur le style avec les classes utilitaires
</Callout>

**Lignes 10-14 :** Pour afficher le composant par défaut dans l'aperçu et dans vos docs

* Nous exigeons que les composants soient ajoutés APRÈS tous les exports pour afficher le composant dans l'aperçu et l'utiliser dans l'éditeur
* La syntaxe MDX nécessite la création d'une nouvelle ligne avant le composant d'aperçu, sinon une erreur se produira
* `<ExampleComponent>` ouvre le composant
* Le texte entre les balises devient la prop `children`
* `</ExampleComponent>` ferme le composant

Cet exemple simple crée un conteneur stylisé réutilisable que vous pouvez utiliser dans toute votre documentation. Il suffit d'envelopper n'importe quel contenu avec les balises `<ExampleComponent>`, et il apparaîtra dans une belle boîte gris foncé avec un espacement approprié et des coins arrondis !

### Consultez la recette ci-dessous pour parcourir le code !

<Recipe slug="create-a-custom-component" title="Créer un composant personnalisé" />

Qu'est-ce qui rend cela si puissant ? Vous pouvez désormais utiliser ce composant n'importe où dans votre documentation lorsque vous avez besoin de mettre en valeur du contenu de manière cohérente. Vous souhaitez modifier l'apparence du contenu mis en évidence dans toute votre documentation ? Il vous suffit de mettre à jour le composant une seule fois, et les modifications s'appliquent partout où vous l'avez utilisé !