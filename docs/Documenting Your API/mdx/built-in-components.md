---
title: Composants intégrés
deprecated: false
hidden: false
metadata:
  robots: index
---
ReadMe fournit plusieurs puissants composants MDX prêts à l'emploi, accessibles directement depuis le menu slash. Pour les composants créés par la communauté, consultez notre [Marketplace](https://docs.readme.com/main/docs/building-custom-mdx-components?isFramePreview=true#marketplace) dans la page **Paramètres > Composants personnalisés**.

### Onglets

<Image align="center" border={false} src="https://files.readme.io/336b9b02322ea3f7e522edd2cac1328f65179ecab4c7124dadaa012d1453e8eb-Editing_Tab_MDX_Component_1.gif" />

Organisez le contenu associé en sections facilement navigables :

**Exemple d'onglets**

<Tabs>
  <Tab title="Premier onglet">
    Bienvenue dans le contenu que vous ne pouvez voir qu'à l'intérieur du premier onglet.
  </Tab>

  <Tab title="Deuxième onglet">
    Voici le contenu qui se trouve uniquement dans le deuxième onglet.
  </Tab>

  <Tab title="Troisième onglet">
    Voici le contenu qui se trouve uniquement dans le troisième onglet.
  </Tab>
</Tabs>

***

### Accordéon

<Image align="center" border={false} src="https://files.readme.io/a29c8744b62ec4b51e366e91a012533f9c6e21638db2c425358cec92a7058d7d-CleanShot_2024-11-08_at_20.10.29.gif" />

Présentez les informations dans des sections réductibles :

**Exemple d'accordéon**

<Accordion title="Titre de mon accordéon" icon="fa-info-circle">
  Lorem ipsum dolor sit amet, **consectetur adipiscing elit.** Ut enim
  ad minim veniam, quis nostrud exercitation ullamco. Excepteur sint
  occaecat cupidatat non proident!
</Accordion>

***

### Cartes

<Image align="center" border={false} src="https://files.readme.io/8702f98924ba19d8c0f1041e999fb6c3dc0dce5e15ead63e5e07f846fc4a28a8-CleanShot_2024-11-09_at_13.12.09.gif" />

Affichez le contenu dans un format propre et en grille :

**Exemple de cartes**

<Cards columns={3}>
  <Card title="Première carte" href="https://readme.com" icon="fa-home" target="_blank">
    Neque porro quisquam est qui dolorem ipsum quia
  </Card>

  <Card title="Deuxième carte" icon="fa-user">
    *Lorem ipsum dolor sit amet, consectetur adipiscing elit*
  </Card>

  <Card title="Troisième carte" icon="fa-star">
    > Ut enim ad minim veniam, quis nostrud ullamco
  </Card>
</Cards>

***

### Colonnes

Crée une mise en page multi-colonnes où le contenu est affiché côte à côte plutôt qu'empilé verticalement.

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