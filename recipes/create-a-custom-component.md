---
title: Crear un componente personalizado
description: >-
  Descripción de la receta: esta receta explica cómo crear un contenedor con
  estilos, simple y reutilizable, que puedes usar en toda tu documentación.


  ¡Simplemente envuelve cualquier contenido con etiquetas ExampleComponent y
  aparecerá en una atractiva caja gris oscura!
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

# Crear un ExampleComponent

<!-- java@1 -->

Estamos creando un componente de React llamado ExampleComponent.

La palabra clave export hace que este componente esté disponible para su importación en otros lugares

({ children }) utiliza la desestructuración para acceder a cualquier contenido ubicado entre las etiquetas de apertura y cierre del componente.

# Estructurar el componente

<!-- java@2-8 -->

return (...) define lo que renderizará el componente, mientras que el <div> exterior utiliza clases de Tailwind CSS para centrar su contenido y ocupar todo el ancho y alto.

El <div> interior crea una caja gris oscura con esquinas redondeadas y espaciado interno

{children} es donde ocurre la magia: esto renderizará cualquier contenido que coloques entre las etiquetas de tu componente.

# Usar el componente

<!-- java@11-13 -->

El <ExampleComponent> abre el componente.

El texto entre las etiquetas se convierte en la prop children

Por último, el </ExampleComponent> cierra el componente.