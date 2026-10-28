---
title: Páginas personalizadas
deprecated: false
hidden: false
metadata:
  robots: index
---
<br />

<Callout icon="👍" theme="okay">
  Ver este artículo como [una página personalizada](https://docs.readme.com/page/custom-page)
</Callout>

Las páginas personalizadas son ideales cuando deseas mantener la navegación superior de tu proyecto de ReadMe, pero también buscas un aspecto personalizado debajo de la barra de búsqueda.

# ¿Qué es diferente? {#whats-different}

1. Sin navegación en la barra lateral izquierda
2. Sin tabla de contenido a la derecha, incluso cuando se usan encabezados
3. Ruta de URL diferente (la subcarpeta es /page en lugar de /docs)
4. Sin ediciones sugeridas
5. Sin votación de páginas
6. Sin "actualizado hace x días"

<Callout icon="🚧" theme="warn">
  Las páginas personalizadas no se ven afectadas por el versionado y son compartidas. Si eliminas una página personalizada, se eliminará de todas partes.
</Callout>

# ¿Qué sigue igual? {#whats-the-same}

Con un [diseño de subencabezado desplegable](/main/docs/subheader-layout), el título de la página aparece en la navegación de migas de pan.

<Image align="center" border={true} width="smart" src="https://files.readme.io/14c46d5-Screen_Shot_2021-05-19_at_3.28.30_PM.png" className="border" />

<Callout icon="📘" theme="info">
  ### Nota {#note}

  El título de la página personalizada ocupa el espacio de una sección en la navegación de migas de pan, pero **no** crea una sección permanente en el menú desplegable.
</Callout>

## Modos {#modes}

Las páginas personalizadas tienen dos modos:

1. **Markdown:** el modo estándar utilizado en la sección de documentación

<Image border={true} src="https://files.readme.io/5300f08-CleanShot_2022-10-15_at_08.56.122x.png" className="border" />

2. **HTML:** el código se [sanitiza](https://en.wikipedia.org/wiki/HTML_sanitization). Si quieres incluir CSS o JavaScript, hazlo en Apariencia > Javascript/hoja de estilo personalizada.
