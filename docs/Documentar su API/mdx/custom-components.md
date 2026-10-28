---
title: Componentes personalizados
deprecated: false
hidden: false
metadata:
  robots: index
---
Crea y administra componentes MDX personalizados desde la página **Custom Components** en **Settings**. A medida que construyes, escribirás código JSX y verás una vista previa de tu componente en tiempo real. Una vez guardados, puedes acceder a tus componentes desde el menú `<` y reutilizarlos en toda tu documentación.

### Beneficios clave {#key-benefits}

- Convierte patrones comunes en componentes reutilizables para garantizar la coherencia, simplificar el mantenimiento y crear una interfaz de usuario unificada en toda tu documentación.
- Personaliza el contenido según la audiencia, el caso de uso o el nivel de acceso _sin_ duplicar páginas.
- Adapta los componentes para que se ajusten a tu producto y haz que tu documentación destaque.
- Añade interactividad a tus documentos con componentes que hacen más que solo mostrar contenido.

## Marketplace {#marketplace}

Explora el Marketplace para descubrir componentes de código abierto desarrollados por la comunidad. ReadMe revisa cada componente para garantizar su calidad y cumplimiento. Simplemente selecciona un componente, realiza las modificaciones necesarias o úsalo tal como está; luego, guárdalo para comenzar a integrarlo en tu documentación.

<Image align="center" border={false} src="https://files.readme.io/4878ee5ee5a98ad931898ff6a4638d3f79ea3f57c90296bcc65b0623d58c5219-Screenshot_2025-09-04_at_4.29.16_PM.png" />

<Callout icon="💡" theme="default">
  **¿Te sientes creativo?** ¡Contribuye con el tuyo! Abre una pull request en el [repositorio de GitHub](https://github.com/readmeio/marketplace). Una vez fusionada, podrás ver tu componente activo en el Marketplace y ayudar a ampliar la biblioteca para todos.
</Callout>

***

## Crea tu primer componente {#create-your-first-component}

Analicemos cómo crear un componente personalizado simple pero útil. Crearemos un componente "Note" que haga que la información importante destaque en tu documentación.

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

### Comprender el código {#understanding-the-code}

<Image align="center" border={false} src="https://files.readme.io/e6e6aa810d1cd0f55f001261284d475c244902bd3bd14b46e98a6b15ac2680e4-CleanShot_2025-02-24_at_12.57.54.gif" />

**Línea 1:** `export const ExampleComponent = props => {`

- Aquí estamos definiendo un nuevo componente llamado `ExampleComponent`
- La palabra clave `export` es obligatoria para definir cualquier variable o componente en MDX
- Podemos acceder a las `props` de React para renderizar cualquier atributo o contenido añadido a la etiqueta del componente

**Líneas 2-8:** La estructura del componente

- `return (...)` define lo que renderizará el componente cuando se use
- El `<div>` exterior utiliza [clases de Tailwind](https://tailwindcss.com/docs/styling-with-utility-classes) para centrar su contenido (`flex items-center`) y ocupar todo el ancho y alto (`h-full w-full`)
- El `<div>` interior crea una caja gris oscuro (`bg-gray-800`) con esquinas redondeadas (`rounded-md`) y espaciado (`p-6 m-4`)
- `{props.children}` es el ingrediente mágico: renderiza cualquier contenido que coloques entre las etiquetas de tu componente

<Callout icon="💁" theme="default">
  ### Una breve nota sobre Tailwind CSS {#a-quick-note-on-tailwind-css}

  ¡No te preocupes si estas clases no te resultan familiares! Puedes consultar la [documentación oficial de Tailwind CSS](https://tailwindcss.com/docs/styling-with-utility-classes) para obtener una guía completa sobre cómo aplicar estilos con clases de utilidad
</Callout>

**Líneas 10-14:** Para renderizar el componente predeterminado en la vista previa y en tu documentación

- Requerimos que los componentes se agreguen DESPUÉS de todas las exportaciones para renderizar el componente en la vista previa y usarlo en el editor
- La sintaxis de MDX requiere crear un salto de línea antes del componente de vista previa, o de lo contrario se producirá un error
- `<ExampleComponent>` abre el componente
- El texto entre las etiquetas se convierte en la prop `children`
- `</ExampleComponent>` cierra el componente

Este sencillo ejemplo crea un contenedor con estilo reutilizable que puedes usar en toda tu documentación. Simplemente envuelve cualquier contenido con las etiquetas `<ExampleComponent>`, ¡y aparecerá en una bonita caja gris oscuro con el espaciado adecuado y esquinas redondeadas!

### ¡Consulta la receta a continuación para revisar el código paso a paso! {#see-the-recipe-below-to-walk-through-the-code}

<Recipe slug="create-a-custom-component" title="Crear un componente personalizado" />

¿Qué hace que esto sea tan potente? Ahora puedes usar este componente en cualquier lugar de tu documentación donde necesites destacar contenido de manera coherente. ¿Necesitas cambiar la apariencia del contenido destacado en toda tu documentación? Solo actualiza el componente una vez, ¡y los cambios se aplicarán en todos los lugares donde lo hayas usado!
