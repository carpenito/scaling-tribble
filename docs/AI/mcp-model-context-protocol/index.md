---
title: MCP (Model Context Protocol)
deprecated: false
hidden: false
metadata:
  robots: index
---
[Model Context Protocol (MCP)](https://modelcontextprotocol.io/introduction) is een standaardisatie van hoe AI-assistenten omgaan met API's, en ReadMe brengt deze mogelijkheid naar jouw ontwikkelaarshub. Met MCP-servers kun je jouw API-documentatie omzetten in een gestructureerde resource die AI-assistenten kunnen begrijpen en programmatisch mee kunnen werken.

## Belangrijkste functies

* **Aangepaste tooling**: Definieer aangepaste workflow- en endpointcombinaties. <Badge label="New" bgColor="var(--purple)" textColor="var(--purple100)" cornerRadius="30px" />
* **Ingeschakelde routes**: Schakel endpoints uit die je niet toegankelijk wilt maken in jouw MCP-server <Badge label="New" bgColor="var(--purple)" textColor="var(--purple100)" cornerRadius="30px" />
* **OpenAPI-integratie**: Genereer een MCP-server vanuit jouw bestaande OpenAPI-specificatie.
* **AI-assistenten kunnen verbinding maken met jouw MCP-server om**:
  * Jouw OpenAPI-specificatie te lezen en te begrijpen.
  * API-aanroepen uit te voeren.
  * Documentatie te doorzoeken met [Ask AI](/docs/ask-ai).
* **MCP-tools**:
  * **OpenAPI-tools**:
    * `execute-request` - Maak API-aanroepen rechtstreeks vanuit jouw specificatie
    * `get-endpoint` - Haal gedetailleerde endpointinformatie op aanvraag op
    * `get-request-body` - Toegang tot gestructureerde aanvraagparameters
    * `get-response-schema` - Begrijp wat jouw API retourneert
    * `list-endpoints` - Blader door alle beschikbare API-endpoints
    * `list-security-schemes` - Toegang tot authenticatievereisten
    * `search-schema` - Vind precies wat je nodig hebt in jouw API-specificatie
    * `get-code-snippet` - Voorbeeldcodefragmenten in jouw voorkeurstaal om met jouw endpoint te werken.
  * **Documentatietools**:
    * `search` - Doorzoek jouw volledige kennisbank naar relevante informatie
    * `fetch` - Geeft een handleidingspagina terug

<Callout icon="📘" theme="info">
  Documentatietools vereisen een upgrade van jouw huidige abonnement met het <Anchor label="AI Booster Pack" target="_blank" href="https://readme.com/pricing">AI Booster Pack</Anchor>.

  Voor Enterprise-klanten: neem contact op met jouw CSM.

  Voor Startup- en Business-klanten: upgrade jouw abonnement met het AI Booster Pack via jouw **Abonnement beheren**-pagina onder Instellingen.
</Callout>

## Hoe het werkt

We maken een speciale MCP-server die verbinding maakt met jouw OpenAPI-specificatie en [Ask AI](/docs/ask-ai)-functionaliteit. Dit creëert een brug tussen jouw API-documentatie en AI-assistenten, waardoor jouw API direct toegankelijker en begrijpelijker wordt voor AI-tools.

## Extra functies

* **Branches** Standaard is de MCP-server verbonden met de nieuwste stabiele versie. Om een andere branch te kiezen, voeg je `?branch=<name>` toe aan de MCP-url. LET OP: Wanneer je op een branch zit, is `search-documentation` niet beschikbaar.
* **Privéprojecten** Om toegang te krijgen tot beveiligde projecten, moet je jouw MCP-client configureren om een `x-readme-auth`-header te sturen
  * Wachtwoordbeveiliging: `x-readme-auth` moet het sitewachtwoord zijn
  * Alleen teamleden & Aangepaste login: `x-readme-auth` moet een API-sleutel zijn in de vorm `bearer <api_key>`

## Aan de slag met MCP

Kies hoe je wilt beginnen met MCP:

1. <Anchor label="Auto-Generate Your Own MCP Server" target="_blank" href="doc:generate-your-own-mcp-server">Genereer automatisch jouw eigen MCP-server</Anchor>: Elk ReadMe-project bevat automatisch een volledig geconfigureerde MCP-server. Schakel MCP eenvoudig in om jouw API-documentatie te verbinden met AI-tools.
2. <Anchor label="Use ReadMe’s MCP Server" target="_blank" href="doc:readmes-mcp-server">Gebruik de MCP-server van ReadMe</Anchor>: Met de MCP-server van ReadMe kun je alles doen wat je normaal in ReadMe zou doen, zoals pagina's toevoegen en bewerken, rechtstreeks via onze API.