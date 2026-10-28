---
title: CSS y JavaScript personalizados
deprecated: false
hidden: false
metadata:
  robots: index
---
En esta sección puedes añadir CSS y Javascript para personalizar aún más la apariencia de tu sitio de documentación.

<Image align="center" border={true} src="https://files.readme.io/ca07f17-CleanShot_2022-09-25_at_09.57.452x.png" className="border" />

<Callout icon="🚧" theme="warn">
  ### Selectores {#selectors}

  Utiliza selectores con el prefijo `.rm-`. Los selectores con hash cambian constantemente y **no se debe** confiar en ellos como selectores (p. ej., `Header-bottom2eLKOFXMEmh5`).
</Callout>

## Hoja de estilo personalizada {#custom-stylesheet}

<Callout icon="📘" theme="info">
  Debes limitar tus cambios a pequeños ajustes. Además, las hojas de estilo no tienen versiones; todas las versiones utilizan la misma hoja de estilo.
</Callout>

## Javascript personalizado {#custom-javascript}

Tu Javascript se incluirá en la parte inferior de la página.

<details>
  <summary><b>Variables globales</b></summary>

ReadMe expone ciertas variables globales para ayudarte a personalizar la experiencia de usuario de tu hub:

- **`RM_ReferenceSidebarScrollTopOffset`**<br />Desplazamiento en píxeles para la lógica de la barra lateral de desplazamiento al elemento activo en secciones continuas de <Glossary>Reference</Glossary>.

</details>

## Etiquetas de inclusión personalizadas {#custom-include-tags}

**HTML de encabezado**

Cualquier HTML aquí se incluirá en la etiqueta head, lo que resulta útil para cosas como metaetiquetas y para cargar CSS o JS externos.

**HTML de pie de página**<br />​<br />Esto irá justo antes de la etiqueta `</body>`. Útil para cosas como analítica y seguimiento.

## Alternar Javascript y CSS personalizados {#toggling-custom-javascript-and-css}

Añade los parámetros de consulta `?disableCustomCss=true&disableCustomJs=true` al final de cualquier URL.
