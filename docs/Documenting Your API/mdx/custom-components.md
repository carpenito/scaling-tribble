---
title: Aangepaste Componenten
deprecated: false
hidden: false
metadata:
  robots: index
---
Maak en beheer aangepaste MDX-componenten via de pagina **Aangepaste Componenten** in **Instellingen**. Terwijl je bouwt, schrijf je JSX-code en zie je een live voorbeeld van je component in realtime. Eenmaal opgeslagen, kun je je componenten openen via het `<`-menu en ze hergebruiken in je documentatie.

### Belangrijkste voordelen

* Zet veelvoorkomende patronen om in herbruikbare componenten voor consistentie, eenvoudiger onderhoud en een uniforme UI in je documentatie.
* Personaliseer inhoud op basis van doelgroep, gebruiksscenario of toegangsniveau _zonder_ pagina's te dupliceren.
* Pas componenten aan zodat ze bij je product passen en je documentatie opvalt.
* Voeg interactiviteit toe aan je documentatie met componenten die meer doen dan alleen inhoud weergeven.

## Marketplace

Blader door de Marketplace om open-source componenten te verkennen die door de community zijn ontwikkeld. Elke component wordt door ReadMe beoordeeld op kwaliteit en naleving. Selecteer eenvoudig een component, breng eventuele aanpassingen aan of gebruik hem zoals hij is — sla hem vervolgens op om hem in je documentatie te integreren.

<Image align="center" border={false} src="https://files.readme.io/4878ee5ee5a98ad931898ff6a4638d3f79ea3f57c90296bcc65b0623d58c5219-Screenshot_2025-09-04_at_4.29.16_PM.png" />

<Callout icon="💡" theme="default">
  **Creatief ingesteld?** Draag je eigen component bij! Open een pull request in de [GitHub-repo](https://github.com/readmeio/marketplace). Zodra het is samengevoegd, zie je je component live in de Marketplace en help je de bibliotheek voor iedereen te laten groeien.
</Callout>

***

## Maak je eerste component

Laten we stap voor stap bekijken hoe je een eenvoudige maar nuttige aangepaste component maakt. We bouwen een "Note"-component die belangrijke informatie laat opvallen in je documentatie.

```jsx
export const ExampleComponent = props => {
  return (
    <div className="flex items-center h-full w-full">
      <div className="bg-gray-800 rounded-md p-6 m-4">
        {props.children}
      </div>
    </div>
  );
};

<ExampleComponent>
  Here's a very simple example component rather than an empty state. This should help you figure out what's happening quicker and see what's possible with custom components!
</ExampleComponent>
```

### De code begrijpen

<Image align="center" border={false} src="https://files.readme.io/e6e6aa810d1cd0f55f001261284d475c244902bd3bd14b46e98a6b15ac2680e4-CleanShot_2025-02-24_at_12.57.54.gif" />

**Regel 1:** `export const ExampleComponent = props => {`

* Hier definiëren we een nieuwe component genaamd `ExampleComponent`
* Het sleutelwoord `export` is vereist om een variabele of component in MDX te definiëren
* We kunnen de React `props` gebruiken om attributen of inhoud die aan de componenttag zijn toegevoegd te renderen

**Regels 2-8:** De structuur van de component

* `return (...)` definieert wat de component rendert wanneer hij wordt gebruikt
* De buitenste `<div>` gebruikt [Tailwind-klassen](https://tailwindcss.com/docs/styling-with-utility-classes) om de inhoud te centreren (`flex items-center`) en de volledige breedte en hoogte in te nemen (`h-full w-full`)
* De binnenste `<div>` maakt een donkergrijze box (`bg-gray-800`) met afgeronde hoeken (`rounded-md`) en opvulling (`p-6 m-4`)
* `{props.children}` is het geheime ingrediënt — het rendert alle inhoud die je tussen je componenttags plaatst

<Callout icon="💁" theme="default">
  ### Een korte opmerking over Tailwind CSS

  Maak je geen zorgen als deze klassen onbekend lijken! Je kunt de officiële [Tailwind CSS-documentatie](https://tailwindcss.com/docs/styling-with-utility-classes) raadplegen voor een uitgebreide handleiding over stijlen met utility-klassen
</Callout>

**Regels 10-14:** Om de standaardcomponent in de preview en in je documentatie te renderen

* Componenten moeten NA alle exports worden toegevoegd om de component in de preview te renderen en in de editor te gebruiken
* MDX-syntaxis vereist het aanmaken van een nieuwe regel vóór de previewcomponent, anders treedt er een fout op
* `<ExampleComponent>` opent de component
* De tekst tussen de tags wordt de `children`-prop
* `</ExampleComponent>` sluit de component

Dit eenvoudige voorbeeld maakt een herbruikbare gestijlde container die je overal in je documentatie kunt gebruiken. Wikkel gewoon inhoud in `<ExampleComponent>`-tags en het verschijnt in een mooie donkergrijze box met de juiste opvulling en afgeronde hoeken!

### Bekijk het recept hieronder om de code stap voor stap te doorlopen!

<Recipe slug="create-a-custom-component" title="Een aangepaste component maken" />

Wat maakt dit zo krachtig? Je kunt deze component nu overal in je documentatie gebruiken waar je inhoud op een consistente manier wilt benadrukken. Wil je de weergave van gemarkeerde inhoud in je volledige documentatie aanpassen? Werk de component eenmalig bij en de wijzigingen worden overal toegepast waar je hem hebt gebruikt!