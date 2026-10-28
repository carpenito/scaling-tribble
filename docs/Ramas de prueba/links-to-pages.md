---
title: Enlaces a páginas
deprecated: false
hidden: false
icon: fad fa-rocket-launch
metadata:
  robots: index
---
## Enlaces internos {#internal-links}

Para crear un enlace entre páginas, empieza escribiendo `[` y aparecerá un menú desplazable con las páginas disponibles a las que puedes enlazar. A medida que continúes escribiendo más caracteres, aparecerán opciones relevantes de enlaces a páginas internas.

<Image align="center" border={true} src="https://files.readme.io/cff6bf4-link_to_pages.gif" className="border" />

El Markdown resultante se verá así:

<Image align="center" border={true} src="https://files.readme.io/9b34336-CleanShot_2022-10-18_at_11.19.16.gif" className="border" />

¡Y para los usuarios terminará viéndose como el enlace de arriba!

<Callout icon="📘" theme="info">
  ### Los enlaces internos solo funcionan dentro de un solo proyecto. {#internal-links-only-work-within-one-project}

  Si enlazas entre varios proyectos, debes usar hipervínculos estándar.
</Callout>

 

## Enlaces de anclaje {#anchor-links}

Todos los encabezados de sección incluyen un enlace de anclaje. El formato es `#header-name`. Por ejemplo, este [enlace](doc:linking-to-pages#anchor-links) te llevará de vuelta a esta sección:

```
[link](doc:linking-to-pages#anchor-links)
```

 

## Enlaces externos {#external-links}

### Enlaces en línea {#inline-linking}

Para enlazar en línea, escribe el texto que deseas enlazar entre corchetes, `[x]`, seguido directamente de la URL del enlace entre paréntesis, `(y)`.

Los enlaces se ven así en el editor de Markdown:

```
[ReadMe](readme.com)
```

Y dan como resultado un enlace que se ve así: [ReadMe](https://readme.com/)

 

### Enlaces de estilo referencia {#reference-style-linking}

Los enlaces de estilo referencia te permiten asignarle a un enlace un número o "nombre" y hacer referencia a él varias veces.

Por ejemplo, si escribes lo siguiente en tu panel:

```
When I first research something I look at [Wikipedia][1] then at [Google][2] then [Wookiepedia][3].

[1]: https://wikipedia.org            "Wikipedia"
[2]: https://google.com               "Google"
[3]: https://starwars.fandom.com      "Wookiepedia"
```

...los enlaces se verán así en tu Hub:

Cuando investigo algo por primera vez, consulto \[Wikipedia]\[1], luego \[Google]\[2] y después \[Wookiepedia]\[3].

[1]: https://wikipedia.org "Wikipedia"

[2]: https://google.com "Google"

[3]: https://starwars.fandom.com "Wookiepedia"

 

## Abrir enlaces en una nueva pestaña {#open-links-in-new-tab}

Actualmente, Markdown y [RDMD](https://docs.readme.com/rdmd/docs/) no tienen una forma de definir el destino de un enlace. En su lugar, se deberá usar HTML estándar para abrir enlaces en una nueva pestaña.

La sintaxis HTML es `target="_blank"`, que se utiliza de esta manera dentro de la etiqueta `<a>`:

```html
<a href="https://readme.com/" target="_blank">ReadMe</a>
```

Esto se puede combinar con nuestra sintaxis `doc:page` para abrir [enlaces a páginas dentro del mismo proyecto](doc:linking-to-pages#internal-links) de esta manera:

```html
<a href="doc:intro-to-readme" target="_blank">Introduction</a>
```

 

## Validación de enlaces {#validating-links}

ReadMe admite varias herramientas de terceros para encontrar automáticamente enlaces rotos en un proyecto de documentación. Un servicio que sugerimos es el [W3C Validator](https://validator.w3.org/checklink). No se requiere iniciar sesión. Para el campo **URL**, introduce el dominio personalizado de tu documentación. Selecciona **Ocultar redirecciones** y selecciona **Comprobar documentos enlazados de forma recursiva**. Deja en blanco la profundidad de recursión.

Los resultados solo mostrarán los enlaces que estén rotos, no en **qué** páginas aparecen esos enlaces ni cuántas veces aparecen los enlaces rotos,

 

## Próximos pasos {#whats-next}

Puedes usar la sección **Próximos pasos** en la parte inferior de la página para enlazar a páginas relevantes dentro de tu proyecto y/o a enlaces externos relevantes. También puedes añadir una descripción para proporcionar más contexto.

<Image align="center" border={true} src="https://files.readme.io/1ae72b6-New_Whats_Next.gif" className="border" />
