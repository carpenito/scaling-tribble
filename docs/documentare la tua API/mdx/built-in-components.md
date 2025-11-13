---
title: Componenti Integrati
excerpt: >-
  ReadMe fornisce diversi potenti componenti MDX pronti all'uso e accessibili
  direttamente dal menu slash.
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  robots: index
---
ReadMe fornisce diversi potenti componenti MDX pronti all'uso e accessibili direttamente dal menu slash. Per componenti creati dalla community, consulta il nostro [Marketplace](https://docs.readme.com/main/docs/building-custom-mdx-components?isFramePreview=true#marketplace) nella pagina **Impostazioni > Componenti Personalizzati**.

### Schede

<Image align="center" border={false} src="https://files.readme.io/336b9b02322ea3f7e522edd2cac1328f65179ecab4c7124dadaa012d1453e8eb-Editing_Tab_MDX_Component_1.gif" />

Organizza contenuti correlati in sezioni facilmente navigabili:

**Esempio di Schede**

<Tabs>
  <Tab title="Prima Scheda">
    Benvenuto nel contenuto che puoi vedere solo all'interno della prima Scheda.
  </Tab>

  <Tab title="Seconda Scheda">
    Ecco il contenuto che si trova solo all'interno della seconda Scheda.
  </Tab>

  <Tab title="Terza Scheda">
    Ecco il contenuto che si trova solo all'interno della terza Scheda.
  </Tab>
</Tabs>

***

### Accordion

<Image align="center" border={false} src="https://files.readme.io/a29c8744b62ec4b51e366e91a012533f9c6e21638db2c425358cec92a7058d7d-CleanShot_2024-11-08_at_20.10.29.gif" />

Presenta informazioni in sezioni richiudibili:

**Esempio di Accordion**

<Accordion title="Il Mio Titolo Accordion" icon="fa-info-circle">
  Lorem ipsum dolor sit amet, **consectetur adipiscing elit.** Ut enim
  ad minim veniam, quis nostrud exercitation ullamco. Excepteur sint
  occaecat cupidatat non proident!
</Accordion>

***

### Carte

<Image align="center" border={false} src="https://files.readme.io/8702f98924ba19d8c0f1041e999fb6c3dc0dce5e15ead63e5e07f846fc4a28a8-CleanShot_2024-11-09_at_13.12.09.gif" />

Visualizza contenuti in un formato pulito, simile a una griglia:

**Esempio di Carte**

<Cards columns={3}>
  <Card title="Prima Carta" href="https://readme.com" icon="fa-home" target="_blank">
    Neque porro quisquam est qui dolorem ipsum quia
  </Card>

  <Card title="Seconda Carta" icon="fa-user">
    *Lorem ipsum dolor sit amet, consectetur adipiscing elit*
  </Card>

  <Card title="Terza Carta" icon="fa-star">
    > Ut enim ad minim veniam, quis nostrud ullamco
  </Card>
</Cards>

***

### Colonne

Crea un layout multi-colonna dove il contenuto viene visualizzato affiancato piuttosto che impilato verticalmente.

<Columns layout="auto">
  <Column>
    Neque porro quisquam est qui dolorem ipsum quia
  </Column>

  <Column>
    *Lorem ipsum dolor sit amet, consectetur adipiscing elit*
  </Column>

  <Column>
    > Ut enim ad minim veniam, quis nostrud ullamco
  </Column>
</Columns>