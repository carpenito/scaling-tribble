---
title: Creare un componente personalizzato
description: >-
  Questa ricetta illustra come creare un semplice contenitore riutilizzabile che
  potrai utilizzare in tutta la tua documentazione.


  Basta racchiudere qualsiasi contenuto tra i tag ExampleComponent e apparirà in
  un elegante riquadro grigio scuro!
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

# Crea un ExampleComponent

<!-- java@1 -->

Stiamo creando un componente React chiamato ExampleComponent.

La parola chiave export rende questo componente disponibile per l'importazione altrove.

({ children }) utilizza la destrutturazione per accedere a qualsiasi contenuto inserito tra i tag di apertura e chiusura del componente.

# Strutturazione del componente

<!-- java@2-8 -->

return (...) definisce ciò che il componente renderà, mentre il <div> esterno utilizza le classi CSS Tailwind per centrare il suo contenuto e occupare l'intera larghezza e altezza.

The inner <div> creates a dark gray box with rounded corners and padding

{children} is where the magic happens—this will render whatever content you place between your component tags.

# Utilizzo del componente

<!-- java@11-13 -->

Il tag <ExampleComponent> apre il componente.

Il testo tra i tag diventa la proprietà children.

Infine, il tag </ExampleComponent> chiude il componente.