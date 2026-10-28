---
title: Personalización de la documentación mediante variables CSS
deprecated: false
hidden: false
metadata:
  robots: index
---
## Opciones de personalización {#customization-options}

Hay dos formas de personalizar tu documentación. Recomendamos usar variables CSS; es la manera más fácil y segura de añadir personalizaciones a tu documentación.

Si deseas cambiar el fondo de tu encabezado, puedes configurar la variable CSS de la siguiente manera:

```css
.App {
  --Header-background: #fff;
}
```

La otra opción es escribir CSS personalizado. Expondremos nombres de clases globales para que los utilices como selectores (con el prefijo `rm`):

```css
.rm-Header {
  background: #fff;
}
```

<Callout icon="📘" theme="info">
  ### :root frente a body {#root-vs-body}

  Nuestras variables CSS están dirigidas al selector `:root` y se cargan después de las tuyas, ¡así que usa el selector `body` para asegurarte de que tus variables tengan prioridad!
</Callout>

***

## Cambiar la tipografía {#changing-your-typeface}

Puedes cambiar la tipografía en toda tu documentación mediante la variable `--font-family`.

```css Custom CSS
.App {
  --font-family: 'Your Typeface';
}

```

Si estás utilizando un servicio como Google Fonts, deberás incluir los elementos `<link />` en tu HTML personalizado.

***

## Encabezado {#header}

Algunas variables varían según el color principal del fondo de tu encabezado (configurado en la página de Apariencia, según sea claro u oscuro). Puedes basar la anulación de tus variables CSS en claro u oscuro haciendo lo siguiente:

```cs
.ThemeContext_dark {
  --Header-button-color: #fff;
}
```

### Variables CSS {#css-variables}

| Nombre                       | Valor predeterminado           | Descripción                                                                                                         |
| :--------------------------- | :----------------------------- | :------------------------------------------------------------------------------------------------------------------ |
| `--Header-background`        | `var(--color-primary)`         | `--color-primary` es el fondo de tu encabezado de la página de Apariencia del panel de control.                     |
| `--Header-border-color`      | `rgba(0, 0, 0, 0.1)`           |                                                                                                                     |
| `--Header-border-width`      | `1px`                          |                                                                                                                     |
| `--Header-button-color`      |                                | Color del texto del botón en el encabezado.                                                                         |
| `--Header-button-hover`      |                                | Color del texto del botón al pasar el cursor sobre él.                                                              |
| `--Header-button-active`     |                                | Color del texto del botón cuando está seleccionado.                                                                 |
| `--Header-button-focus`      |                                |                                                                                                                     |
| `--Header-jumpTo-background` | `var(--color-primary-inverse)` |                                                                                                                     |
| `--Header-jumpTo-color`      | `var(--color-primary)`         |                                                                                                                     |
| `--Header-tab-padding`       | `5px 2px`                      | Cantidad de relleno dentro de cada pestaña de navegación (disponible con la opción de encabezado Line).             |
| `--Header-tab-underline`     | `var(--color-primary)`         | Color del subrayado de la pestaña al usar la navegación por pestañas (disponible con la opción de encabezado Line). |

### Clases globales {#global-classes}

<Image border={false} src="https://files.readme.io/fd2d896-An_Introduction_to_ReadMe-20220323-115038.png" />

1. `.rm-Header`
2. `.rm-Logo`
3. `.rm-Header-top-link`
4. `.rm-Header-bottom-link`
5. `.rm-SearchToggle`
6. `.rm-Header-top-link_login`

No aparece en la imagen:

- `.rm-JumpTo`
- `.rm-Logo-img`

***

## Barra lateral {#sidebar}

### Clases globales {#global-classes-1}

<Image border={false} src="https://files.readme.io/861a758-Safari_-_An_Introduction_to_ReadMe_-_2021-10-27_at_09.55_AM.png" title="Safari - Introducción a ReadMe - 2021-10-27 a las 09.55 AM.png" />

1. `.rm-Sidebar`
2. `.rm-Sidebar-link `
3. `.rm-Sidebar-wrapper` (contiene tanto el encabezado como la lista)
4. `.rm-Sidebar-heading` (solo el encabezado)
5. `.rm-Sidebar-list` (solo la lista)

### Variables CSS {#css-variables-1}

| Nombre                     | Valor predeterminado | Descripción                                           |
| :------------------------- | :------------------- | :---------------------------------------------------- |
| `--Sidebar-border-color`   | `rgba(0, 0, 0, 0.1)` |                                                       |
| `--Sidebar-indent`         | `15px`               | Espacio de sangría de las subpáginas                  |
| `--Sidebar-link-padding-y` | `5px`                | Relleno vertical de cada elemento en la barra lateral |

***

## Artículo {#article}

### Clases globales {#global-classes-2}

<Image border={false} src="https://files.readme.io/93ce267-Safari_-_Get_changelogs_-_2021-05-25_at_01.42_PM.png" title="Safari - Obtener changelogs - 2021-05-25 a las 01.42 PM.png" />

1. `.rm-APISectionHeader` (este selector se usa en el Playground y también afectará a esos elementos)
2. `.rm-APILogInfo`
3. `.rm-APILogsTable`
4. `.rm-ParamContainer `
5. `.rm-ParamInput` o `.rm-ParamSelect`
6. `.rm-APIResponseSchemaPicker`

No aparece en la imagen:

- `.rm-Pagination` (el contenedor para los botones de navegación de Página anterior / Página siguiente ubicados en la parte inferior de la página)

## Playground {#playground}

### Variables CSS {#css-variables-2}

| Nombre                        | Valor predeterminado                                   | Descripción                                                                                                                      |
| :---------------------------- | :----------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------- |
| `--tryit-background`          | `var(--color-primary, #118cfd)`                        | Color de fondo del botón Try It. `--color-primary` es el fondo de tu encabezado de la página de Apariencia del panel de control. |
| `--tryit-background-hover`    | `var(--color-primary-darken-10, #0272d9)`              |                                                                                                                                  |
| `--tryit-background-active`   | `var(--color-primary-darken-20, #0158a7)`              |                                                                                                                                  |
| `--tryit-background-focus`    | `var(--color-primary-alpha-25, rgba(17,140,253,0.25))` |                                                                                                                                  |
| `--tryit-background-disabled` | `var(--color-primary-darken-20, #0158a7)`              |                                                                                                                                  |
| `--tryit-border-radius`       | `var(--border-radius-lg)`                              | `--border-radius-lg` tiene un valor predeterminado de 7.5px.                                                                     |
| `--tryit-color`               | `var(--color-primary-inverse)`                         |                                                                                                                                  |
| `--tryit-spinner-color`       | `var(--color-primary-inverse)`                         |                                                                                                                                  |

### Clases globales {#global-classes-3}

<Image border={false} src="https://files.readme.io/561e588-Safari_-_Get_metadata_-_2021-05-25_at_01.15_PM.png" title="Safari - Obtener metadatos - 2021-05-25 a las 01.15 PM.png" />

Selector de idioma:

1. `.rm-LanguageButton`
2. `.rm-LanguageButton-more`
3. `.rm-APISectionHeader` (este selector se usa en el Artículo y también afectará a esos elementos)
4. `.rm-PlaygroundRequest`
5. `.rm-TryIt`
6. `.rm-PlaygroundResponse`

***

## Variables globales {#global-variables}

| Nombre                    | Valor predeterminado                                                                                                                |
| :------------------------ | :---------------------------------------------------------------------------------------------------------------------------------- |
| `--border-radius`         | `5px`                                                                                                                               |
| `--border-radius-lg`      | `calc(var(--border-radius) * 1.5)`                                                                                                  |
| `--box-shadow-menu-light` | `0 5px 10px rgba(0,0,0,.05), 0 2px 6px rgba(0,0,0,.025), 0 1px 3px rgba(0,0,0,.025)`                                                |
| `--box-shadow-pill`       | `inset 0 1px 1px 0 rgba(255,255,255,.2), inset 0 -1px 2px 0 rgba(0,0,0,.2), 0 1px 2px 0 rgba(0,0,0,0.05)`                           |
| `--box-shadow-tooltip`    | `0 1px 2px rgba(0,0,0,.05), inset 0 -1px 2px rgba(0,0,0,.2), inset 0 1px 1px rgba(255,255,255,.2)`                                  |
| `--font-family`           | `-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Oxygen, Ubuntu, Cantarell, Fira Sans, Droid Sans, Helvetica Neue, sans-serif` |
| `--font-family-mono`      | `"SF Mono", SFMono-Regular, ui-monospace, "DejaVu Sans Mono", Menlo, Consolas, monospace`                                           |
| `--font-weight`           | `500`                                                                                                                               |
| `--font-weight-bold`      | `600`                                                                                                                               |
| `--transition-fast`       | `.15s`                                                                                                                              |
| `--transition-slow`       | `.3s`                                                                                                                               |
| `--transition-timing`     | `cubic-bezier(.16,1,.3,1)`                                                                                                          |

## ReadMe Markdown {#readme-markdown}

También disponemos de varias variables específicas para [ReadMe Markdown (RDMD)](https://rdmd.readme.io), que es el motor de Markdown que procesa todo el contenido Markdown de ReadMe. Puedes obtener más información sobre estas variables y otros consejos para [personalizar RDMD](https://rdmd.readme.io/docs/custom-css).
