---
title: Créer un composant personnalisé
description: >-
  Description de la recetteCette recette explique comment créer un conteneur
  stylisé simple et réutilisable que vous pouvez utiliser dans toute votre
  documentation.


  Il suffit d'envelopper n'importe quel contenu avec les balises
  ExampleComponent, et il apparaîtra dans une belle boîte gris foncé !
hidden: false
recipe:
  color: '#018FF4'
  icon: 🔧
---
```java Java
export const ExampleComponent = ({ children }) => {
  return (
    <div className="flex items-center h-full w-full">
      <div className="bg-gray-800 rounded-md p-6 m-4">
        {children}
      </div>
    </div>
  );
};

<ExampleComponent>
  Here's a very simple example component rather than an empty state. This should help you figure out what's happening quicker and see what's possible with custom components!
</ExampleComponent>
```

```json Response Example
{"success":true}
```

# Créer un ExampleComponent

<!-- java@1 -->

Nous créons un composant React appelé ExampleComponent.

Le mot-clé export rend ce composant disponible pour être importé ailleurs

({ children }) utilise la déstructuration pour accéder à tout contenu placé entre les balises d'ouverture et de fermeture du composant.

# Structurer le composant

<!-- java@2-8 -->

return (...) définit ce que le composant va afficher, tandis que le <div> externe utilise les classes Tailwind CSS pour centrer son contenu et occuper toute la largeur et la hauteur.

Le <div> interne crée une boîte gris foncé avec des coins arrondis et un rembourrage

{children} est là où la magie opère — cela affichera le contenu que vous placez entre les balises de votre composant.

# Utiliser le composant

<!-- java@11-13 -->

Le <ExampleComponent> ouvre le composant.

Le texte entre les balises devient la prop children

Enfin, le </ExampleComponent> ferme le composant.