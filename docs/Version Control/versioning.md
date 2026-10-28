---
title: Versionado
excerpt: hola mundo
deprecated: false
hidden: false
metadata:
  robots: index
---
Mantener múltiples versiones de tu documentación es fundamental para muchos productos técnicos diferentes. Esta página profundiza en los detalles de cómo funciona el control de versiones en ReadMe, así como en varios casos de uso.

<Callout icon="🚧" theme="warn">
  **Secciones afectadas:** Solo se versionan las secciones Guías, Recetas y Referencia. El contenido de Página de destino, Discusiones y Registro de cambios persistirá entre versiones.
</Callout>

## Crear una nueva versión {#making-a-new-version}

Para crear una nueva versión, abre el menú Versiones y ramas seleccionando el **nombre de la versión** (es decir, v3.0) en la navegación de administración. A continuación, haz clic en el botón **+ Nueva versión** en la esquina superior derecha. Elige desde qué versión bifurcar y asigna un nombre a tu nueva versión. Esto creará una copia de esta versión; no podrás incorporar los cambios de vuelta a la versión que se bifurcó.

<Image align="center" border={false} src="https://files.readme.io/c543cc3ff266bd3b210d720cfb7c5e09d7750c78dcb5ccfd60f669eae003ca39-versions.png" />

### Semver (o similar) {#semver-ish}

Nuestro control de versiones se basa en <Anchor label="Semver" target="_blank" href="http://semver.org/">Semver</Anchor>, pero es mucho más flexible que Semver en cuanto a las entradas aceptables. Esto significa que tus versiones pueden ser tan simples como `v1.0`, pero tan complejas como `v1.0-hello-this-is-a-version`.

***

## Opciones de versión {#version-options}

<Image align="center" border={false} width="500px" src="https://files.readme.io/159f0425970c8c5849bc6b6e7b684f51fdab23a656f6488139337adaa75e9d60-version_options.png" />

### Predeterminada {#default}

Esta es la versión a la que se dirigirá tu dominio. Los usuarios pueden cambiar a una versión diferente haciendo clic en el selector desplegable de versiones.

<Callout icon="🙅‍♂️" theme="default">
  No es posible fusionar dos versiones. Si quieres realizar cambios en ambas, ¡tendrás que hacerlo manualmente!
</Callout>

### Pública {#public}

Al seleccionar esto, estará disponible en el selector desplegable de versiones y para cualquier persona que pueda ver tu documentación. Si no se selecciona, esta versión se marcará como **Oculta** y solo será visible para los administradores del proyecto.

### Beta {#beta}

Indicar que una versión es beta añadirá una insignia junto a la versión en el selector desplegable de versiones. No crea un cuadro de aviso en la página ni ningún otro cambio visible.

### Obsoleta {#deprecated}

Selecciona esto para marcar versiones anteriores. Además de ver una insignia de "obsoleta" junto a la versión en el selector desplegable de versiones, los usuarios también verán un gran banner rojo encima de la documentación al visitar esta versión obsoleta. Así es como se ve:

<Image align="center" border={true} width="smart" src="https://files.readme.io/RhO7iWuhSMGsBrHSrFMt_Screen%20Shot%202015-12-16%20at%2012.17.04%20PM.png" className="border" />

***

## Mostrar el menú desplegable de versiones {#displaying-version-dropdown}

<Image align="center" border={false} caption="Vista de administrador: Oculta y Obsoleta no son visibles para los usuarios finales" src="https://files.readme.io/5f0ac4bab3338c5e1cceee0368a02363bb6c2eca6f40324725d6d43593e564ab-version_drop.png" />

De forma predeterminada, mostramos el selector desplegable de versiones mencionado anteriormente en la barra de subnavegación. Puedes activar o desactivar su visualización en **Configuración > Encabezado y pie de página > Subnavegación**.

<Image align="center" border={false} src="https://files.readme.io/1a975ae96b399662d42cee67ca226a8fd49bfb9188da95ccfd00a2125f0347d7-version_picker.png" />

***

## Contenido reutilizable {#reusable-content}

Cualquier [contenido reutilizable](doc:reusable-content) creado dentro de una versión solo se puede utilizar dentro de la documentación de esa versión; no es posible definir bloques de contenido reutilizable que se puedan usar entre versiones dentro de un mismo proyecto.

Si se crea una nueva versión al bifurcarla a partir de una versión existente, la nueva versión hereda todos los bloques de contenido reutilizable definidos en la versión existente. Sin embargo, los bloques de contenido reutilizable de la nueva versión son completamente independientes de la versión anterior.

<Callout icon="📘" theme="info">
  ### Contenido reutilizable global {#global-reusable-content}

  Los proyectos con un plan Enterprise tienen la posibilidad de definir **Contenido reutilizable global** que _sí_ se puede usar en diferentes proyectos y versiones. ¡Consulta nuestra [documentación sobre contenido reutilizable para grupos Enterprise](https://docs.readme.com/ent/docs/reusable-content-enterprise) para obtener más información!
</Callout>

***

## Casos de uso {#use-cases}

Hay muchos escenarios diferentes en los que el control de versiones de la documentación puede resultar útil — algunos son más evidentes que otros. El caso de uso más evidente es cuando la versión de tu documentación necesita coincidir con el versionado de tu API u otro producto técnico, y necesitas mantener copias de tus documentos para cada versión respectiva.

Otro caso de uso es para reestructuraciones de contenido o migraciones más grandes, especialmente cuando estos cambios son más complejos que simplemente actualizar unas pocas páginas (en cuyo caso recomendamos <Anchor label="Ediciones sugeridas" target="_blank" href="doc:suggested-edits">Ediciones sugeridas</Anchor>). Puedes bifurcar una nueva versión de tu documentación, realizar una reestructuración importante (por ejemplo, reorganizar categorías de páginas, combinar páginas, eliminar contenido desactualizado, etc.) y seguir teniendo tu documentación anterior visible para el público. Y cuando estés listo para hacer el cambio, ¡es tan fácil como cambiar el nombre de las versiones y modificar un par de ajustes de versión!

***

## Preguntas frecuentes {#faq}

<Accordion title="¿Cuántas versiones puedo crear?" icon="fa-tags">
  Los usuarios del plan gratuito pueden crear hasta 3 versiones. Actualiza al plan Startup o superior para desbloquear versiones ilimitadas.
</Accordion>
