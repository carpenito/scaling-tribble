---
title: Maak een aangepaste component
description: >-
  Recept BeschrijvingDit recept legt uit hoe je een eenvoudige herbruikbare
  gestijlde container maakt die je door je documentatie heen kunt gebruiken.


  Omsluit gewoon inhoud met ExampleComponent-tags en het verschijnt in een mooi
  donkergrijs vak!n
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

# Maak een ExampleComponent

<!-- java@1 -->

We maken een React-component genaamd ExampleComponent.

Het sleutelwoord export maakt dit component beschikbaar voor import elders

({ children }) gebruikt destructuring om toegang te krijgen tot inhoud die tussen de openings- en sluitingstags van het component is geplaatst.

# De component structureren

<!-- java@2-8 -->

return (...) definieert wat het component zal renderen, terwijl de buitenste <div> Tailwind CSS-klassen gebruikt om de inhoud te centreren en de volledige breedte en hoogte in te nemen.

De binnenste <div> maakt een donkergrijs vak met afgeronde hoeken en opvulling

{children} is waar de magie gebeurt—dit rendert welke inhoud je ook tussen je component-tags plaatst.

# Het component gebruiken

<!-- java@11-13 -->

De <ExampleComponent> opent het component.

De tekst tussen de tags wordt de children-prop

Ten slotte sluit de </ExampleComponent> het component.