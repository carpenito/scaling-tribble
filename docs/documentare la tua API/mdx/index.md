---
title: MDX
excerpt: >-
  Guida per scrivere documentazione in ReadMe utilizzando MDX (Markdown
  eXtended) con sintassi JSX
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  robots: index
---
Scrivere documentazione in ReadMe viene fatto in [Markdown eXtended](https://mdxjs.com) (MDX), che è basato sulla [specifica CommonMark](https://commonmark.org). A differenza del Markdown puro, MDX utilizza una sintassi leggermente diversa chiamata [Javascript XML](https://react.dev/learn/writing-markup-with-jsx) (JSX). Ci sono alcune piccole differenze quando si scrive MDX rispetto a Markdown se stai tentando di scrivere HTML.

## Markdown vs MDX

Tutte le pagine in ReadMe utilizzano MDX per offrirti la possibilità di scrivere componenti riutilizzabili e interattivi. Generalmente, non dovrebbe fare differenza quando scrivi Markdown—a meno che tu non stia scrivendo HTML. _Sembra_ HTML, ma è più rigoroso. Il problema più comune è che non puoi avere tag auto-chiudenti in JSX:

<Columns layout="auto">
  <Column>
    <i className="fa-duotone fa-solid fa-square-x" /> Non valido

    ```
    <br>
    <img>
    <hr>
    ```
  </Column>

  <Column>
    <i className="fa-duotone fa-solid fa-circle-check" /> Valido

    ```
    <br />
    <img />
    <hr />
    ```
  </Column>
</Columns>

Tutti i tag in stile JSX devono essere esplicitamente chiusi, inclusi i tag auto-chiudenti.

<Columns layout="auto">
  <Column>
    <i className="fa-duotone fa-solid fa-square-x" /> Non valido

    ```
    <p>Contenuto
    <ul>
      <li>1
      <li>2
      <li>3
    </ul>
    ```
  </Column>

  <Column>
    <i className="fa-duotone fa-solid fa-circle-check" /> Valido

    ```
    <p>Contenuto</p>
    <ul>
      <li>1</li>
      <li>2</li>
      <li>3</li>
    </ul>
    ```
  </Column>
</Columns>

La maggior parte degli attributi dovranno essere camelCase—eccetto `data-` e `aria-`. Gli stili inline dovranno essere un oggetto `{}` e quelle proprietà devono anche essere camelCase quando scritte in JSX (non si applica se stai scrivendo CSS in un tag `<style />`).

<Columns layout="auto">
  <Column>
    <i className="fa-duotone fa-solid fa-square-x" /> Non valido

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
    <i className="fa-duotone fa-solid fa-circle-check" /> Valido

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
  **Suggerimento:** Se stai riscontrando altri problemi o errori quando lavori con MDX, consulta [Risoluzione Problemi Errori MDX](https://docs.readme.com/main/docs/rendering-errors-invalid-mdx) per altri problemi comuni.
</Callout>

## Scrivere JSX

<Image align="center" border={false} src="https://files.readme.io/a29c8744b62ec4b51e366e91a012533f9c6e21638db2c425358cec92a7058d7d-CleanShot_2024-11-08_at_20.10.29.gif" />

Quando modifichi la tua documentazione, puoi scrivere componenti dinamici in JSX, in alcuni modi:

1. **Sulla pagina:** Scrivi il tuo JSX in testo semplice. L'editor analizzerà automaticamente la tua sintassi e evidenzierà il tuo JSX.

2. **[Riutilizzo Componenti](https://docs.readme.com/main/v3.0_move-rdme/docs/building-custom-mdx-components/):** Per scrivere un componente che puoi riutilizzare in qualsiasi pagina, apri le tue **Impostazioni** e naviga alla pagina **Componenti Personalizzati**. Una volta scritto il tuo primo componente, puoi riutilizzarli in qualsiasi pagina: `<ExampleComponent />`

3. **[Già disponibili](https://docs.readme.com/main/v3.0_move-rdme/docs/built-in-components/):** Il nostro editor rende facile utilizzare componenti che abbiamo integrato in ReadMe. Puoi trovarli aprendo il menu comandi digitando `/` nell'editor. Sotto la sezione **Componente**, puoi scegliere i componenti `Tabs`, `Accordion`, `Columns`, o `Cards`.

4. **Componenti Pubblici:** Manteniamo anche un [marketplace dei componenti](https://github.com/readmeio/marketplace) dove chiunque può inviare un componente.