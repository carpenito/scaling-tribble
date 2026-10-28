---
title: Creación de una receta
deprecated: false
hidden: false
metadata:
  robots: index
---
# Descripción general {#overview}

¿Listo para transformar tus ejemplos de código en experiencias de aprendizaje intuitivas para los desarrolladores? Esta guía te muestra cómo crear tu primera Recipe de principio a fin. Aprenderás a desglosar código complejo en pasos fáciles de asimilar, añadir anotaciones útiles y personalizar la experiencia visual para que coincida con tu marca.

<br />

<Image align="center" border={false} src="https://files.readme.io/05e72a5519ad6e9421775f6688bbee366623e93528abf9df93dd5ae1973b81dd-Screenshot_2025-05-22_at_2.16.36_PM.png" />

<br />

## Antes de comenzar {#before-you-start}

- Ten a mano tu ejemplo de código (o ten claro qué endpoint de API deseas utilizar como punto de partida)
- Asegúrate de que la sección Recipes esté accesible en tu proyecto de ReadMe
- Considera qué lenguajes de programación utilizan más tus desarrolladores
- Piensa en los objetivos de aprendizaje clave para este tutorial paso a paso del código

## Crear una Recipe {#creating-a-recipe}

<Image border={false} src="https://files.readme.io/4482047-Screen_Shot_2020-12-01_at_3.42.35_PM.png" />

### 1. Accede al editor de Recipes {#1-access-the-recipe-editor}

Ve a tu proyecto de ReadMe y haz clic en **Edit** para entrar en la interfaz de edición. En el menú de navegación principal, selecciona **Recipes** para acceder al área de gestión de Recipes. Haz clic en el botón **Create New Recipe** para abrir el creador de Recipes.

<Image align="center" border={false} src="https://files.readme.io/139f1a2224d1add344a0071284be7614929b7cac5be5babf7cb0860b16b9f81e-Screenshot_2025-05-22_at_12.47.08_PM.png" />

### 2. Configura tu ejemplo de código {#2-configure-your-code-sample}

1. En el panel superior derecho, selecciona tu lenguaje de programación en el menú desplegable.
2. Añade tu ejemplo de código y asegúrate de que tenga el formato adecuado con resaltado de sintaxis. Esta será la base a la que harán referencia tus anotaciones paso a paso.

<Image align="center" border={false} src="https://files.readme.io/91f78f372bffaf5521f48ba6972275b5d3fa1b74cf4b4f917a5d7284a6d51c11-Screenshot_2025-05-22_at_2.09.51_PM.png" />

**Nota:** Cada Recipe puede admitir varios lenguajes de programación, por lo que puedes añadir versiones en otros lenguajes después de configurar la primera.

### 3. Crea tus anotaciones paso a paso {#3-build-your-step-by-step-annotations}

En la barra lateral izquierda, crea los pasos resaltados que guiarán a los desarrolladores a través de tu código. Para cada paso:

- Escribe un título claro y descriptivo que explique qué logra esta parte del código
- Añade explicaciones detalladas que ayuden a los desarrolladores a entender el "porqué" detrás de cada sección
- Especifica los números de línea que deben resaltarse en este paso
- Utiliza un lenguaje conversacional que haga accesibles los conceptos complejos

Cada paso debe centrarse en un concepto o una acción específicos dentro de tu ejemplo de código, desarrollando la comprensión de forma progresiva.

<Image border={false} src="https://files.readme.io/cece453-Screen_Shot_2020-12-01_at_3.49.54_PM.png" />

### **4. Añade ejemplos de respuesta** {#4-add-response-examples}

En el panel inferior derecho, incluye la respuesta esperada de la API cuando tu código se ejecute con éxito. Esto muestra a los desarrolladores exactamente cómo es una respuesta correcta y les ayuda a verificar su implementación.

Si tu código no genera una respuesta (o si mostrarla no es relevante), puedes dejar esta sección vacía; se ocultará automáticamente en la Recipe final.

**Nota:** ¡Las variables de datos de usuario también funcionan en las Recipes! Si tienes configurada la documentación personalizada, puedes incluir contenido dinámico en tus respuestas.

<Callout icon="👍" theme="okay">
  ### ¡Las variables de datos de usuario funcionan en las Recipes! {#user-data-variables-work-in-recipes}

  Si tienes [variables](doc:personalized-docs) en tu documentación, por ejemplo pasadas a través del webhook de Personalized Docs, ¡también funcionarán en las Recipes!
</Callout>

### 5. Personaliza la apariencia visual {#5-customize-visual-appearance}

Cambia a la pestaña **Appearance** para hacer que tu Recipe sea única:

- **Selecciona un emoji**: haz clic en el icono de emoji para elegir uno en el menú desplegable
- **Establece el color de fondo**: usa el selector de color para elegir un fondo que coincida con tu marca (admite valores RGB, HSL o HEX)
- **Escribe una descripción**: añade una descripción detallada que aparecerá en la tarjeta de Recipe más grande en tu sección de Recipes

El color del botón _Open Recipe_ se hereda automáticamente de la configuración del color de los enlaces de tu proyecto.

<Image border={false} src="https://files.readme.io/ea6500f-Screen_Shot_2020-10-19_at_12.41.19_PM.png" />

### **6. Elige las ubicaciones de inserción** {#6-choose-embedding-locations}

Decide dónde debe aparecer tu Recipe en toda tu documentación:

- **Inserción en API Reference**: selecciona endpoints específicos donde esta Recipe proporcione un contexto relevante
- **Sección Recipes**: tu Recipe aparecerá automáticamente en el área principal de Recipes una vez publicada
- **Inserción en guías**: puedes insertar manualmente la Recipe en las páginas de guías más adelante utilizando el widget de Recipe

Marca las casillas junto a los endpoints pertinentes para que tu Recipe esté accesible exactamente donde los desarrolladores más la necesitan.

La Recipe aparecerá como una tarjeta interactiva, tal como se muestra en el área de vista previa del paso de apariencia.

<Image border={false} src="https://files.readme.io/20cf1e2-Screen_Shot_2020-12-03_at_5.14.16_PM.png" />

<br />

<Image border={false} src="https://files.readme.io/e4619b5-Screen_Shot_2020-12-01_at_2.59.43_PM.png" />

<br />

<Callout icon="🚧" theme="warn">
  Los elementos insertados no aparecerán en la sección Reference [hasta que se habilite la sección Recipes](#enable-recipes-section).
</Callout>

<br />

### 7. Establece el estado de publicación {#7-set-publication-status}

Elige el nivel de visibilidad de tu Recipe:

- **Unpublished**: solo visible para los administradores del proyecto (predeterminado para las Recipes nuevas)
- **Published**: visible para todos los usuarios en tu colección de Recipes
- **Featured**: destacada de forma prominente en la parte superior de tu sección Recipes (solo se puede destacar una Recipe a la vez)

Comienza con "Published" para poner tu Recipe a disposición de los desarrolladores, o mantenla en "Unpublished" mientras sigues perfeccionando el contenido.

|                 |                                                                                                                                                                                  |
| :-------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Featured**    | Esta es la Recipe destacada en la parte superior de la sección de Recipes. Debe haber una Recipe destacada si tu página de Recipes es pública, y debe estar en estado publicado. |
| **Published**   | Visible para los usuarios en la cuadrícula de tarjetas debajo de la Recipe destacada                                                                                             |
| **Unpublished** | Los clientes no pueden verla. Las Recipes nuevas están en estado "unpublished" por defecto.                                                                                      |

<Image border={false} src="https://files.readme.io/445d0c8-Screen_Shot_2020-12-16_at_3.54.22_PM.png" />

<br />

## Preguntas frecuentes y resolución de problemas {#faq--troubleshooting}

**¿Puedo eliminar el icono de Recipe de la barra de navegación?**

Esta sección solo es visible para los administradores del proyecto. Tus clientes no verán esta sección a menos que la [habilites](#enabling-your-recipes-page) para que sea visible para ellos.

A medida que traslademos más funciones de edición al frontend de tu centro de documentación, continuaremos haciendo más evidente lo que ven los administradores del proyecto en comparación con lo que ven tus clientes.

**¿Cómo cambio el color del botón azul "Open Recipe"?**

El color de este botón se hereda del Link Color que hayas configurado en el [Theme Editor](/main/docs/design-themes) en la configuración de tu proyecto. Para cambiarlo, tendrás que modificar el Link Color para todo tu hub de ReadMe.

**¿Puedo cambiar el nombre de la sección Recipe al igual que con las otras secciones?**

¡Aún no, pero estamos trabajando en ello!

**¿El resaltado de mi código no funciona correctamente?** Comprueba que los números de línea sean precisos y que hayas seleccionado el lenguaje de programación correcto. Recuerda que los números de línea comienzan en 1, no en 0.

**¿El widget de Recipe no aparece en mis guías?** Asegúrate de que la sección Recipes esté habilitada en la configuración de navegación de tu sitio. El widget no estará disponible hasta que Recipes esté activado en tu proyecto.

**¿Mi Recipe insertada no aparece en las páginas de API Reference?** Las Recipes insertadas solo aparecen una vez que la sección Recipes esté habilitada públicamente. Comprueba la configuración de navegación de tu sitio y asegúrate de que al menos una Recipe esté publicada.

**¿La sección de respuesta ha desaparecido?** Si borras por completo el contenido de respuesta predeterminado, el panel de respuesta se ocultará automáticamente. Vuelve a añadir contenido para que sea visible de nuevo.
