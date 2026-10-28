---
title: Temas
deprecated: false
hidden: false
metadata:
  robots: index
---
Todos los planes tienen acceso para personalizar en la configuración de **Tema**. Abre **Configuración** en la parte superior izquierda de la interfaz de administración y, a continuación, selecciona **Tema** en la barra lateral.

- Diseño
- Marca (logotipo, favicon y colores)
- Estilo del encabezado

<PlanTable currentPlan="Free" />

<Callout icon="💁‍♂️" theme="default">
  **Nota:** Hay disponibles opciones y servicios de personalización adicionales en los planes Business y Enterprise.
</Callout>

***

## Diseño {#layout}

<Image align="center" border={false} width="400px" src="https://files.readme.io/3d30b1d7f55cd7e37def92bb05c5c4799bc0e1294169209626ff9a24181733cc-Launch_Week-20250628-1026262x.webp" />

Puedes elegir entre 3 opciones de diseño: Clásico, Compacto y Moderno. Y también hay una opción para expandir el diseño en pantallas más grandes. Podrás previsualizar el diseño antes de guardar.

<Callout icon="🚧" theme="warn">
  ¡Pronto estará disponible una opción de solo barra lateral!
</Callout>

***

## Marca {#branding}

### Logotipo {#logo}

Existe la opción de subir un logotipo blanco cuando se necesita una alternativa para determinados temas y ajustes de color del encabezado.

**Formato**

- Se recomienda SVG para obtener la mejor calidad.
- Si tu logotipo es demasiado complejo para un SVG, WEBP es una buena alternativa—usa el doble del tamaño deseado para tu logotipo para mayor nitidez en pantallas de alta resolución.
- No se admiten archivos GIF.

**Dimensiones**

- 24px de altura de forma predeterminada. En los temas Clásico y Moderno puedes seleccionar un logotipo más grande de 40px de altura.

**Personalización adicional**

- Los clientes con acceso a Custom CSS pueden usar nuestras clases globales y variables CSS para ajustar aún más la visualización de su logotipo:

```css
.rm-Logo-img {
  --Header-logo-height: YOUR_CUSTOM_HEIGHT
}
```

***

## Encabezado {#header}

<Image align="center" border={false} width="400px" src="https://files.readme.io/9c14d52d69809626037d9cb483cd2fb0619734f6ccc3c3428fd6380936a44b43-Launch_Week-20250628-1043112x.webp" />

Puedes elegir entre 4 opciones de diseño: Línea, Color sólido, Degradado y Superposición.

<Callout icon="💁‍♂️" theme="default">
  La opción de encabezado Línea ahora muestra enlaces en pestañas de forma predeterminada. Los usuarios con la visualización anterior de botones pueden cambiar. Una vez que cambies, no podrás volver atrás.
</Callout>

**Personalización adicional**

- Los clientes con acceso a Custom CSS pueden usar nuestras clases globales y variables CSS para ajustar aún más su encabezado:

```css
.rm-Header {
  --Header-background: YOUR_CUSTOM_VALUE /* defaults to your brand color */
  --Header-border-color: YOUR_CUSTOM_VALUE /* default: rgba(0, 0, 0, 0.1) */
  --Header-button-padding: YOUR_CUSTOM_VALUE /* default: 10px */

  /* Line theme only */
  --Header-tab-underline: YOUR_CUSTOM_VALUE /* defaults to your brand color */
}
```
