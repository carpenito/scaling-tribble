---
title: MDX
deprecated: false
hidden: false
metadata:
  robots: index
---
Documentatie schrijven in ReadMe gebeurt in [Markdown eXtended](https://mdxjs.com) (MDX), dat gebaseerd is op de [CommonMark-specificatie](https://commonmark.org). In tegenstelling tot puur Markdown gebruikt MDX een iets andere syntaxis genaamd [Javascript XML](https://react.dev/learn/writing-markup-with-jsx) (JSX). Er zijn enkele kleine verschillen bij het schrijven van MDX ten opzichte van Markdown als je HTML probeert te schrijven.

## Markdown vs MDX

Alle pagina's in ReadMe gebruiken MDX om je de mogelijkheid te bieden herbruikbare en interactieve componenten te schrijven. Over het algemeen maakt dit geen verschil bij het schrijven van Markdown—tenzij je HTML schrijft. Het _lijkt_ op HTML, maar is strikter. Het meest voorkomende probleem is dat je geen zelfsluitende tags kunt gebruiken in JSX:

<Columns layout="auto">
  <Column>
    <i className="fa-duotone fa-solid fa-square-x" /> Ongeldig

    ```
    <br>
    <img>
    <hr>
    ```
  </Column>

  <Column>
    <i className="fa-duotone fa-solid fa-circle-check" /> Geldig

    ```
    <br />
    <img />
    <hr />
    ```
  </Column>
</Columns>

Alle JSX-stijl tags moeten expliciet worden gesloten, inclusief zelfsluitende tags.

<Columns layout="auto">
  <Column>
    <i className="fa-duotone fa-solid fa-square-x" /> Ongeldig

    ```
    <p>Inhoud
    <ul>
      <li>1
      <li>2
      <li>3
    </ul>
    ```
  </Column>

  <Column>
    <i className="fa-duotone fa-solid fa-circle-check" /> Geldig

    ```
    <p>Inhoud</p>
    <ul>
      <li>1</li>
      <li>2</li>
      <li>3</li>
    </ul>
    ```
  </Column>
</Columns>

De meeste attributen moeten camelCase zijn—behalve `data-` en `aria-`. Inline stijlen moeten een object zijn `{}` en die eigenschappen moeten ook camelCase zijn wanneer ze in JSX worden geschreven (dit geldt niet als je CSS schrijft in een `<style />` tag).

<Columns layout="auto">
  <Column>
    <i className="fa-duotone fa-solid fa-square-x" /> Ongeldig

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
    <i className="fa-duotone fa-solid fa-circle-check" /> Geldig

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
  **Tip:** Als je andere problemen of fouten tegenkomt bij het werken met MDX, bekijk dan [MDX-fouten oplossen](https://docs.readme.com/main/docs/rendering-errors-invalid-mdx) voor meer veelvoorkomende problemen.
</Callout>

## JSX schrijven

<Image align="center" border={false} src="https://files.readme.io/a29c8744b62ec4b51e366e91a012533f9c6e21638db2c425358cec92a7058d7d-CleanShot_2024-11-08_at_20.10.29.gif" />

Bij het bewerken van je documentatie kun je dynamische componenten in JSX schrijven, op een aantal manieren:

1. **Op de pagina:** Schrijf je JSX in platte tekst. De editor parseert automatisch je syntaxis en markeert je JSX.

2. **[Componenten hergebruiken](https://docs.readme.com/main/v3.0_move-rdme/docs/building-custom-mdx-components/):** Om een component te schrijven die je op elke pagina kunt hergebruiken, open je je **Instellingen** en navigeer je naar de pagina **Aangepaste componenten**. Zodra je je eerste component hebt geschreven, kun je deze op elke pagina hergebruiken: `<ExampleComponent />`

3. **[Kant-en-klaar](https://docs.readme.com/main/v3.0_move-rdme/docs/built-in-components/):** Onze editor maakt het eenvoudig om componenten te gebruiken die we in ReadMe hebben ingebouwd. Je kunt ze vinden door het opdrachtmenu te openen door `/` in de editor te typen. Onder de sectie **Component** kun je de componenten `Tabs`, `Accordion`, `Columns` of `Cards` kiezen.

4. **Publieke componenten:** We onderhouden ook een [componentenmarktplaats](https://github.com/readmeio/marketplace) waar iedereen een component kan indienen.