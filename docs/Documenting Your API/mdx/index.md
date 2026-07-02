---
title: MDX
deprecated: false
hidden: false
metadata:
  robots: index
---
La rédaction de documentation dans ReadMe se fait en [Markdown eXtended](https://mdxjs.com) (MDX), basé sur la [spécification CommonMark](https://commonmark.org). Contrairement au Markdown pur, MDX utilise une syntaxe légèrement différente appelée [Javascript XML](https://react.dev/learn/writing-markup-with-jsx) (JSX). Il existe quelques différences lors de l'écriture en MDX par rapport au Markdown si vous tentez d'écrire du HTML.

## Markdown vs MDX

Toutes les pages de ReadMe utilisent MDX pour vous offrir la possibilité d'écrire des composants réutilisables et interactifs. En général, cela ne devrait pas faire de différence lors de l'écriture en Markdown — sauf si vous écrivez du HTML. Cela _ressemble_ à du HTML, mais est plus strict. Le problème le plus courant est que vous ne pouvez pas avoir de balises auto-fermantes en JSX :

<Columns layout="auto">
  <Column>
    <i className="fa-duotone fa-solid fa-square-x" /> Invalide

    ```
    <br>
    <img>
    <hr>
    ```
  </Column>

  <Column>
    <i className="fa-duotone fa-solid fa-circle-check" /> Valide

    ```
    <br />
    <img />
    <hr />
    ```
  </Column>
</Columns>

Toutes les balises de style JSX doivent être explicitement fermées, y compris les balises auto-fermantes.

<Columns layout="auto">
  <Column>
    <i className="fa-duotone fa-solid fa-square-x" /> Invalide

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
    <i className="fa-duotone fa-solid fa-circle-check" /> Valide

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

La plupart des attributs devront être en camelCase — à l'exception de `data-` et `aria-`. Les styles en ligne devront être un objet `{}` et ces propriétés doivent également être en camelCase lorsqu'elles sont écrites en JSX (cela ne s'applique pas si vous écrivez du CSS dans une balise `<style />`.

<Columns layout="auto">
  <Column>
    <i className="fa-duotone fa-solid fa-square-x" /> Invalide

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
    <i className="fa-duotone fa-solid fa-circle-check" /> Valide

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
  **Conseil :** Si vous rencontrez d'autres problèmes ou erreurs lors de l'utilisation de MDX, consultez [Résoudre les erreurs MDX](https://docs.readme.com/main/docs/rendering-errors-invalid-mdx) pour les problèmes les plus courants.
</Callout>

## Écrire en JSX

<Image align="center" border={false} src="https://files.readme.io/a29c8744b62ec4b51e366e91a012533f9c6e21638db2c425358cec92a7058d7d-CleanShot_2024-11-08_at_20.10.29.gif" />

Lors de l'édition de votre documentation, vous pouvez écrire des composants dynamiques en JSX, de plusieurs façons :

1. **Sur la page :** Écrivez votre JSX en texte brut. L'éditeur analysera automatiquement votre syntaxe et mettra en évidence votre JSX.

2. **[Réutiliser des composants](https://docs.readme.com/main/v3.0_move-rdme/docs/building-custom-mdx-components/) :** Pour écrire un composant réutilisable sur n'importe quelle page, ouvrez vos **Paramètres** et accédez à la page **Composants personnalisés**. Une fois votre premier composant écrit, vous pouvez le réutiliser sur n'importe quelle page : `<ExampleComponent />`

3. **[Prêts à l'emploi](https://docs.readme.com/main/v3.0_move-rdme/docs/built-in-components/) :** Notre éditeur facilite l'utilisation des composants intégrés à ReadMe. Vous pouvez les trouver en ouvrant le menu de commandes en tapant `/` dans l'éditeur. Dans la section **Composant**, vous pouvez choisir les composants `Tabs`, `Accordion`, `Columns` ou `Cards`.

4. **Composants publics :** Nous maintenons également un [marché de composants](https://github.com/readmeio/marketplace) où tout le monde peut soumettre un composant.