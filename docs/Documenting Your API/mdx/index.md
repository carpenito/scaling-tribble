---
title: MDX
deprecated: false
hidden: false
metadata:
  robots: index
---
La redacción de documentos en ReadMe se realiza en [Markdown eXtended](https://mdxjs.com) (MDX), que se basa en la [especificación CommonMark](https://commonmark.org). A diferencia de Markdown puro, MDX utiliza una sintaxis ligeramente diferente llamada [Javascript XML](https://react.dev/learn/writing-markup-with-jsx) (JSX). Hay algunas pequeñas diferencias al escribir MDX en comparación con Markdown si intentas escribir HTML.

## Markdown frente a MDX {#markdown-vs-mdx}

Todas las páginas de ReadMe utilizan MDX para ofrecerte la posibilidad de escribir componentes reutilizables e interactivos. Por lo general, no debería haber ninguna diferencia al escribir Markdown, a menos que estés escribiendo HTML. Se _parece_ a HTML, pero es más estricto. El problema más común es que no puedes tener etiquetas de cierre automático en JSX:

<Columns layout="auto">
  <Column>
    <i className="fa-duotone fa-solid fa-square-x"></i> No válido

    ```
    <br>
    <img>
    <hr>
    ```
  </Column>

  <Column>
    <i className="fa-duotone fa-solid fa-circle-check"></i> Válido

    ```
    <br />
    <img />
    <hr />
    ```
  </Column>
</Columns>

Todas las etiquetas de estilo JSX deben cerrarse explícitamente, incluidas las etiquetas de cierre automático.

<Columns layout="auto">
  <Column>
    <i className="fa-duotone fa-solid fa-square-x"></i> No válido

    ```
    <p>Content
    <ul>
      <li>1
      <li>2
      <li>3
    </ul>
    ```
  </Column>

  <Column>
    <i className="fa-duotone fa-solid fa-circle-check"></i> Válido

    ```
    <p>Content</p>
    <ul>
      <li>1</li>
      <li>2</li>
      <li>3</li>
    </ul>
    ```
  </Column>
</Columns>

La mayoría de los atributos deberán estar en camelCase, excepto `data-` y `aria-`. Los estilos en línea deberán ser un objeto `{}` y esas propiedades también deben estar en camelCase cuando se escriben en JSX (no se aplica si estás escribiendo CSS en una etiqueta `<style />`.

<Columns layout="auto">
  <Column>
    <i className="fa-duotone fa-solid fa-square-x"></i> No válido

    ```
    <img 
      aria-label="my label" 
      class="my-class" 
      style="
        margin-left: auto; 
        margin-right: auto;
      "
    >
    ```
  </Column>

  <Column>
    <i className="fa-duotone fa-solid fa-circle-check"></i> Válido

    ```
    <img 
      aria-label="my label" 
      className="my-class" 
      style={{ 
        marginLeft: 'auto', 
        marginRight: 'auto' 
      }}
    />
    ```
  </Column>
</Columns>

<HTMLBlock>{`
<style>
  .fa-square-x {
    color: var(--red);
  }

  .fa-circle-check {
    color: var(--green);
  }
</style>
`}</HTMLBlock>

<Callout icon="📘" theme="info">
  **Consejo:** si te encuentras con otras peculiaridades o errores al trabajar con MDX, consulta [Solucionar errores de MDX](https://docs.readme.com/main/docs/rendering-errors-invalid-mdx) para ver más problemas comunes.
</Callout>

## Escribir JSX {#writing-jsx}

<Image align="center" border={false} src="https://files.readme.io/a29c8744b62ec4b51e366e91a012533f9c6e21638db2c425358cec92a7058d7d-CleanShot_2024-11-08_at_20.10.29.gif" />

Al editar tus documentos, puedes escribir componentes dinámicos en JSX de varias formas:

1. **En la página:** escribe tu JSX en texto plano. El editor analizará automáticamente la sintaxis y resaltará tu JSX.

2. **[Reutilización de componentes](https://docs.readme.com/main/v3.0_move-rdme/docs/building-custom-mdx-components/):** Para escribir un componente que puedas reutilizar en cualquier página, abre tu **Configuración** y navega a la página **Componentes personalizados**. Una vez que escribas tu primer componente, podrás reutilizarlo en cualquier página: `<ExampleComponent />`

3. **[Listos para usar](https://docs.readme.com/main/v3.0_move-rdme/docs/built-in-components/):** Nuestro editor facilita el uso de componentes que hemos integrado en ReadMe. Puedes encontrarlos abriendo el menú de comandos al escribir `/` en el editor. En la sección **Componente**, puedes elegir los componentes `Tabs`, `Accordion`, `Columns` o `Cards`.

4. **Componentes públicos:** También mantenemos un [mercado de componentes](https://github.com/readmeio/marketplace) donde cualquiera puede enviar un componente.
