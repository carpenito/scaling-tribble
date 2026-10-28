---
title: Componentes integrados
deprecated: false
hidden: false
metadata:
  robots: index
---
ReadMe ofrece varios componentes MDX potentes listos para usar y accesibles directamente desde el menú de barra diagonal. Para componentes creados por la comunidad, consulta nuestro [Marketplace](https://docs.readme.com/main/docs/building-custom-mdx-components?isFramePreview=true#marketplace) en la página **Configuración > Componentes personalizados**.

### Pestañas {#tabs}

<Image align="center" border={false} src="https://files.readme.io/336b9b02322ea3f7e522edd2cac1328f65179ecab4c7124dadaa012d1453e8eb-Editing_Tab_MDX_Component_1.gif" />

Organiza el contenido relacionado en secciones fácilmente navegables:

**Ejemplo de pestañas**

<Tabs>
  <Tab title="Primera pestaña">
    Te damos la bienvenida al contenido que solo puedes ver dentro de la primera pestaña.
  </Tab>

  <Tab title="Segunda pestaña">
    Aquí tienes contenido que solo está dentro de la segunda pestaña.
  </Tab>

  <Tab title="Tercera pestaña">
    Aquí tienes contenido que solo está dentro de la tercera pestaña.
  </Tab>
</Tabs>

***

### Acordeón {#accordion}

<Image align="center" border={false} src="https://files.readme.io/a29c8744b62ec4b51e366e91a012533f9c6e21638db2c425358cec92a7058d7d-CleanShot_2024-11-08_at_20.10.29.gif" />

Presenta información en secciones desplegables:

**Ejemplo de acordeón**

<Accordion title="Título de mi acordeón" icon="fa-info-circle">
  Lorem ipsum dolor sit amet, **consectetur adipiscing elit.** Ut enim
  ad minim veniam, quis nostrud exercitation ullamco. Excepteur sint
  occaecat cupidatat non proident!
</Accordion>

***

### Tarjetas {#cards}

<Image align="center" border={false} src="https://files.readme.io/8702f98924ba19d8c0f1041e999fb6c3dc0dce5e15ead63e5e07f846fc4a28a8-CleanShot_2024-11-09_at_13.12.09.gif" />

Muestra el contenido en un formato limpio en forma de cuadrícula:

**Ejemplo de tarjetas**

<Cards columns={3}>
  <Card title="Primera tarjeta" href="https://readme.com" icon="fa-home" target="_blank">
    Neque porro quisquam est qui dolorem ipsum quia
  </Card>

  <Card title="Segunda tarjeta" icon="fa-user">
    _Lorem ipsum dolor sit amet, consectetur adipiscing elit_
  </Card>

  <Card title="Tercera tarjeta" icon="fa-star">
    > Ut enim ad minim veniam, quis nostrud ullamco
  </Card>
</Cards>

***

### Columnas {#columns}

Crea un diseño de varias columnas donde el contenido se muestra lado a lado en lugar de apilarse verticalmente.

<Columns layout="auto">
  <Column>
    Neque porro quisquam est qui dolorem ipsum quia
  </Column>

  <Column>
    _Lorem ipsum dolor sit amet, consectetur adipiscing elit_
  </Column>

  <Column>
    > Ut enim ad minim veniam, quis nostrud ullamco
  </Column>
</Columns>
