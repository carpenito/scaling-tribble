---
title: Contenido reutilizable
deprecated: false
hidden: false
metadata:
  robots: index
---
# ¡Simplifica el flujo de trabajo de mantenimiento de tu documentación con contenido reutilizable! {#simplify-your-docs-maintenance-workflow-with-reusable-content}

**Edita una vez, actualiza en todas partes**. Los bloques de contenido reutilizable te ayudan a minimizar los errores manuales y a garantizar que los cambios en tu centro para desarrolladores se apliquen en todos los lugares donde sean necesarios. 😉

<Image align="center" border={true} src="https://files.readme.io/05b4408-RC_gif_long.gif" className="border" />

## Cómo funciona el contenido reutilizable {#how-reusable-content-works}

El contenido reutilizable, como su nombre indica, permite a los administradores de ReadMe crear bloques de contenido Markdown que se pueden usar repetidamente en varias páginas de la documentación de sus proyectos. Cuando cualquier persona de tu proyecto con acceso de administrador edita y actualiza un bloque de contenido reutilizable, este se actualiza automáticamente en cada instancia en la que se utiliza, ¡lo que supone un enorme ahorro de tiempo!

El contenido reutilizable funciona como un bloque y se encuentra en el menú de barra diagonal del editor. Crear un bloque de contenido reutilizable no es solo para texto; ¡es compatible con todo Markdown! Esto significa que puedes tener bloques de contenido reutilizable que incluyan imágenes, fragmentos de código, notas destacadas ¡y mucho más!

<Image align="center" border={true} src="https://files.readme.io/88eaaa9-Docs_adding_RC_block_with_image.gif" className="border" />

### Beneficios de usar bloques de contenido reutilizable {#benefits-of-using-reusable-content-blocks}

1️⃣ **Creación de documentación más eficiente** - para nuestros administradores de ReadMe que son responsables de producir y gestionar una amplia documentación de API, la capacidad de realizar cambios en varias páginas de tu documentación actualizando un bloque de contenido reutilizable (en lugar de tener que buscar cada instancia y actualizarla manualmente) agiliza significativamente el flujo de trabajo de edición y mantenimiento de la documentación.

2️⃣ **Mayor precisión y menos errores** - Menos ediciones manuales y más cambios automatizados significan menos margen de error. Ya sea para incluir contenido específico de una versión, añadir notas destacadas relevantes para tipos de planes específicos o garantizar que todas las páginas relacionadas se vinculen entre sí, los bloques de contenido reutilizable permiten a tu equipo escalar la producción de documentación y garantizar un mayor control de calidad en todos los aspectos.

3️⃣ **Mayor claridad en toda tu documentación = una mejor experiencia de usuario para los desarrolladores que visitan tu centro** - Los bloques de contenido reutilizable permiten a los administradores de proyectos optimizar y unificar la forma en que comunican conceptos que se repiten en todo tu centro para desarrolladores. Los desarrolladores confían en tu documentación para comprender cómo integrar y utilizar con éxito tu API o producto, y cuando esa documentación es clara y coherente, ayuda a que los desarrolladores disfruten de una mejor experiencia en tu centro y al utilizar tu API o producto en general.

<Callout icon="📘" theme="info">
  ### ¡El contenido reutilizable está disponible en los planes Business y Enterprise de ReadMe! {#reusable-content-is-available-on-readme-business-and-enterprise-plans}

  Si estás en nuestros planes Business o Enterprise, podrás crear bloques de contenido reutilizable desde el menú de barra diagonal del editor (o usando la sintaxis \<). Los grupos Enterprise también tendrán acceso a la página de contenido reutilizable en el panel de su grupo Enterprise. Si estás en nuestros planes Free, Startup u Open Source, deberás mejorar tu plan para acceder a esta función. ¡Puedes hacerlo en la página Mejorar plan del panel de control de tu proyecto!
</Callout>

## Uso de contenido reutilizable en todo tu proyecto {#using-reusable-content-across-your-project}

Los paneles de proyectos del plan Business y los proyectos secundarios de Enterprise tienen una página de **Contenido reutilizable** en la sección Documentación de sus paneles de proyectos. Esta página proporciona un lugar centralizado para ver y gestionar todos los bloques de contenido reutilizable utilizados en un proyecto. Dentro de esta página, los administradores pueden crear nuevos bloques de contenido reutilizable, editar los existentes y eliminar bloques (solo si no se están utilizando en ninguna página).

<Image align="center" border={true} src="https://files.readme.io/cef3109-Docs_RC_Menu_in_self_serve_and_child_proj_dashboards.png" className="border" />

### Creación de un nuevo bloque de contenido reutilizable en una página de Guías o Referencia de API {#creating-a-new-reusable-content-block-on-a-guides-or-api-reference-page}

Hay **dos formas** de crear un nuevo bloque de contenido reutilizable en una página de Guías o Referencia de API en el panel de control de tu proyecto.

**Opción 1: Resalta un bloque existente y selecciona “Hacer\[lo] reutilizable”**

Si tienes un bloque de Markdown existente que te gustaría hacer reutilizable, usa el menú Acciones de bloque para seleccionar el texto y elige la opción Hacer reutilizable. Desde allí, podrás realizar modificaciones adicionales en la ventana de edición de contenido reutilizable antes de guardar el bloque.

<Image align="center" border={true} src="https://files.readme.io/ba2a818-Docs_Make_Text_into_RC_block.png" className="border" />

**Opción 2: Crear un nuevo bloque de contenido reutilizable desde el menú de barra diagonal del editor**

De forma similar a como crearías cualquier bloque de Markdown, escribe / para abrir el menú de barra diagonal y navega hasta la sección Contenido reutilizable. Hay dos opciones: **Crear nuevo** y **Reutilizar contenido**.

<Image align="center" border={true} src="https://files.readme.io/3e4f3eb-Docs_Creating_New_RC_Block_from_Slash_Menu.gif" className="border" />

Tanto si resaltas un bloque existente para hacerlo reutilizable como si seleccionas “Crear nuevo” en la sección Contenido reutilizable del menú de barra diagonal, aparecerá esta ventana de contenido reutilizable. Aquí es donde nombrarás el bloque de contenido reutilizable (esto solo se usa internamente), podrás crearlo y realizar modificaciones en él, y guardarlo para que sea reutilizable.

<Image align="center" border={true} src="https://files.readme.io/726d3c2-Docs_RC_editing_menu_blank.png" className="border" />

<Callout icon="🚧" theme="warn">
  ### No puedes editar el nombre de un bloque de contenido reutilizable una vez creado {#you-cannot-edit-the-name-of-a-reusable-content-block-once-its-been-created}

  Una vez que asignas un nombre a tu bloque de contenido reutilizable, no puedes cambiar ni editar el nombre. Solo puedes editar el contenido del cuerpo del bloque.
</Callout>

### Cómo añadir un bloque de contenido reutilizable a una página {#adding-a-reusable-content-block-to-a-page}

Así como hay dos formas de crear un nuevo bloque de contenido reutilizable, también hay dos formas de insertar un bloque de contenido reutilizable existente en una página de Guías o Referencia de API.

De forma similar a como insertas una variable o un término del glosario, al escribir “\<” en una página se abrirá un menú con los bloques de contenido reutilizable de tu proyecto, además de los términos del glosario y las variables. Selecciona de la lista el bloque de contenido reutilizable que deseas usar para insertarlo en la página.

<Image align="center" border={true} src="https://files.readme.io/0b9fbf2-Docs_Using__to_Bring_Up_RC_Menu.png" className="border" />

También puedes insertar un bloque de contenido reutilizable desde el menú de barra diagonal del editor. Selecciona la opción “Reutilizar contenido” del menú para ver una lista de todos los bloques de contenido reutilizable disponibles. Desplázate por las opciones, selecciona la que deseas utilizar ¡y se insertará en la página!

<Image align="center" border={true} src="https://files.readme.io/1171888-Docs_Adding_Existing_RC_block_from_slash_menu.gif" className="border" />

### Cómo identificar un bloque de contenido reutilizable en uso {#identifying-a-reusable-content-block-in-use}

Los bloques de contenido reutilizable tienen un borde verde y están etiquetados como **REUTILIZABLE** en el editor.

<Image align="center" border={true} src="https://files.readme.io/bac17d4-docs_page_-_RC_block_menu.png" className="border" />

Características:

1. La etiqueta izquierda identifica el bloque como reutilizable y muestra el nombre del bloque
2. Si haces clic en el menú desplegable izquierdo, tendrás la opción de **editar** o **desvincular** el bloque
3. La etiqueta derecha indica en cuántas páginas se utiliza este bloque en particular
4. Si haces clic en el menú desplegable derecho, se muestran las páginas específicas donde se está utilizando el bloque de contenido reutilizable

### Edición de un bloque de contenido reutilizable {#editing-a-reusable-content-block}

Al hacer clic en el menú desplegable de la etiqueta izquierda en un bloque de contenido reutilizable y seleccionar **Editar**, aparecerá la ventana de edición. Si tienes un plan Business (o estás creando un bloque para un único proyecto secundario de Enterprise), puedes editar el bloque de contenido reutilizable y hacer clic en **Actualizar**, lo que actualizará la información del bloque de contenido reutilizable en todas las instancias donde se esté utilizando. Si estás en un proyecto Enterprise, dirígete a [esta página](https://docs.readme.com/ent/docs/reusable-content-enterprise#/) de nuestras Guías de Enterprise para obtener más información sobre el proceso.

En esta ventana de edición también hay una opción para **Eliminar**, que elimina el bloque por completo. Para poder eliminar un bloque de contenido reutilizable, primero debes quitar (ya sea eliminando o desvinculando) todas sus instancias en todo tu proyecto.

<Image align="center" border={true} src="https://files.readme.io/1e3f201-Docs_Deleting_an_RC_Block.png" className="border" />

### Desvinculación de un bloque de contenido reutilizable {#detaching-a-reusable-content-block}

Si deseas eliminar la instancia de un bloque de contenido reutilizable o deseas realizar una edición en un bloque de una página que no quieres que se refleje en todas las instancias, considera **desvincular** el bloque.

Puedes hacer esto mediante el menú desplegable izquierdo en la parte superior del bloque de contenido reutilizable. Selecciona **Desvincular** y el bloque volverá inmediatamente a su estado original de Markdown.

<Image align="center" border={true} src="https://files.readme.io/7b61371-Detaching_an_RC_block.gif" className="border" />

<Callout icon="⏭️" theme="default">
  ### ¿Buscas más información sobre el contenido reutilizable para tu grupo Enterprise? {#looking-for-more-information-about-reusable-content-for-your-enterprise-group}

  ¡Tenemos una página dedicada para eso! Si eres un cliente Enterprise que busca obtener más información sobre cómo gestionar el contenido reutilizable para tu grupo Enterprise, ¡dirígete a [esta página](https://docs.readme.com/ent/docs/reusable-content-enterprise#/)!
</Callout>

## Preguntas frecuentes sobre el contenido reutilizable {#reusable-content-faqs}

**¿Cómo se encuentran los bloques de contenido reutilizable que ya existen en tu proyecto?**

Actualmente existen dos formas de localizar los bloques de contenido reutilizable que se han creado para tu proyecto del plan Business (o proyecto secundario de Enterprise): (1) puedes localizarlos a través del menú de barra diagonal del editor (Reutilizable -> Reutilizar contenido -> genera una lista de todos los bloques de contenido reutilizable) o (2) usar la sintaxis \< para abrir el menú de todos los bloques de contenido reutilizable (además de los términos del glosario y las variables de tu proyecto).

**¿Qué aspectos se deben tener en cuenta al utilizar bloques de contenido reutilizable?**

- No puedes anidar un bloque de contenido reutilizable dentro de otro bloque de contenido reutilizable
- Un bloque de contenido reutilizable se guarda por separado de la página en la que se utiliza. Para actualizar un bloque, guarda el cambio en la ventana de edición de contenido reutilizable y, a continuación, guarda la página en la que estás trabajando
- Cuando creas y guardas inicialmente un bloque de contenido reutilizable, el bloque dirá “usado en 0 páginas”. Tendrás que guardar la página para que el recuento del bloque se actualice a “usado en 1 página”
- Si exportas un proyecto a archivos .md y luego vuelves a importar ese archivo a ReadMe, los bloques de contenido reutilizable creados previamente que se hayan exportado ya no se reconocerán como bloques de contenido reutilizable en el nuevo proyecto. Si el nuevo proyecto está en un plan Business o Enterprise, podrás crear nuevos bloques de contenido reutilizable

**¿Cómo funciona el control de versiones con los bloques de contenido reutilizable?**

- Cada versión de tu proyecto de ReadMe tiene su propio subconjunto de bloques reutilizables
- No puedes usar bloques reutilizables entre diferentes versiones, a menos que los clones manualmente y los agregues a una nueva versión. Aun así, una vez que los actualices en una versión, no se actualizarán automáticamente en otras versiones
  - Por ejemplo, si creas una nueva versión de tu proyecto, v2.0, que se bifurca de v1.0, la nueva versión incluirá cualquier bloque de contenido reutilizable que se haya creado y utilizado en v1.0. Sin embargo, los bloques de contenido reutilizable que ahora están en v2.0 son diferentes y, aunque siguen siendo reutilizables y se sincronizan automáticamente, no se sincronizan con los bloques de contenido reutilizable de v1.0 (a pesar de que los bloques tengan el mismo nombre). El recuento de cuántas veces se utiliza un bloque de contenido reutilizable está vinculado al nivel de versión.

**¿Cómo funcionan las ediciones sugeridas con los bloques de contenido reutilizable?**

- No puedes sugerir una edición en un bloque de contenido reutilizable; esto se aplica tanto a los usuarios conectados como a los administradores que ven tu proyecto desde el centro
- Los usuarios conectados pueden sugerir mover un bloque de contenido reutilizable, eliminarlo del contenido de la página y desvincularlo
- Para sugerir una edición en el contenido de un bloque de contenido reutilizable, el usuario final primero deberá desvincular el bloque y luego editar ese contenido
- Cuando esto suceda, los administradores de proyectos tendrán la opción de fusionar la sugerencia desde el panel del proyecto, como ocurre con todas las ediciones sugeridas

**¿Qué sucede si mejoras o reduces tu plan?**

- Actualmente, el contenido reutilizable solo está disponible en los planes Business y Enterprise
- El contenido reutilizable también está incluido en la prueba gratuita de ReadMe
- Si cambias a un plan inferior en el que tenías acceso a bloques de contenido reutilizable y los habías creado previamente, sucederá lo siguiente:
  - Los bloques de contenido reutilizable seguirán existiendo en las páginas de tu proyecto
  - Estos bloques estarán en modo de ‘solo lectura’; no podrás editarlos a menos que los desvincules
  - También perderás el menú “Usado en” y no podrás ver dónde se utilizan los bloques en todo el proyecto
- Si luego vuelves a mejorar a Business o Enterprise, entonces:
  - Recuperarás el acceso a cualquier bloque de contenido reutilizable existente y tendrás la capacidad de crear, actualizar, desvincular y/o eliminar bloques de contenido reutilizable existentes y nuevos
