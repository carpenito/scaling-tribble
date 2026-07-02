---
title: Ingebouwde componenten
deprecated: false
hidden: false
metadata:
  robots: index
---
ReadMe biedt verschillende krachtige MDX-componenten standaard aan, direct toegankelijk via het slash-menu. Voor door de community gebouwde componenten kun je onze [Marketplace](https://docs.readme.com/main/docs/building-custom-mdx-components?isFramePreview=true#marketplace) bekijken op de pagina **Instellingen > Aangepaste componenten**.

### Tabbladen

<Image align="center" border={false} src="https://files.readme.io/336b9b02322ea3f7e522edd2cac1328f65179ecab4c7124dadaa012d1453e8eb-Editing_Tab_MDX_Component_1.gif" />

Organiseer gerelateerde inhoud in eenvoudig navigeerbare secties:

**Voorbeeld van tabbladen**

<Tabs>
  <Tab title="Eerste tabblad">
    Welkom bij de inhoud die je alleen kunt zien in het eerste tabblad.
  </Tab>

  <Tab title="Tweede tabblad">
    Dit is de inhoud die alleen in het tweede tabblad staat.
  </Tab>

  <Tab title="Derde tabblad">
    Dit is de inhoud die alleen in het derde tabblad staat.
  </Tab>
</Tabs>

***

### Accordeon

<Image align="center" border={false} src="https://files.readme.io/a29c8744b62ec4b51e366e91a012533f9c6e21638db2c425358cec92a7058d7d-CleanShot_2024-11-08_at_20.10.29.gif" />

Presenteer informatie in inklapbare secties:

**Voorbeeld van accordeon**

<Accordion title="Mijn accordeontitel" icon="fa-info-circle">
  Lorem ipsum dolor sit amet, **consectetur adipiscing elit.** Ut enim
  ad minim veniam, quis nostrud exercitation ullamco. Excepteur sint
  occaecat cupidatat non proident!
</Accordion>

***

### Kaarten

<Image align="center" border={false} src="https://files.readme.io/8702f98924ba19d8c0f1041e999fb6c3dc0dce5e15ead63e5e07f846fc4a28a8-CleanShot_2024-11-09_at_13.12.09.gif" />

Toon inhoud in een overzichtelijk rasterformaat:

**Voorbeeld van kaarten**

<Cards columns={3}>
  <Card title="Eerste kaart" href="https://readme.com" icon="fa-home" target="_blank">
    Neque porro quisquam est qui dolorem ipsum quia
  </Card>

  <Card title="Tweede kaart" icon="fa-user">
    *Lorem ipsum dolor sit amet, consectetur adipiscing elit*
  </Card>

  <Card title="Derde kaart" icon="fa-star">
    > Ut enim ad minim veniam, quis nostrud ullamco
  </Card>
</Cards>

***

### Kolommen

Maakt een meerkolomsindeling waarbij inhoud naast elkaar wordt weergegeven in plaats van verticaal gestapeld.

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