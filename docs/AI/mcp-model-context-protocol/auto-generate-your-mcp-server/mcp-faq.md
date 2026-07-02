---
title: MCP FAQ
deprecated: false
hidden: false
metadata:
  robots: index
---
<br />

Deze FAQ beantwoordt veelgestelde vragen over het gebruik van [Model Context Protocol (MCP)](https://modelcontextprotocol.io/introduction) met ReadMe-projecten.

## Algemeen

### Wat is het Model Context Protocol (MCP)?

Model Context Protocol (MCP) is een standaard voor de manier waarop AI-assistenten met API's communiceren. In ReadMe zet MCP uw API-documentatie en OpenAPI-definitie om in een gestructureerde resource die AI-tools kunnen begrijpen, doorzoeken en programmatisch aanroepen.

### Hoe werkt MCP met mijn ReadMe-project?

ReadMe maakt een speciale MCP-server aan voor uw project. Deze server verbindt met uw OpenAPI-specificatie en uw [Ask AI](/docs/ask-ai)-functionaliteit, zodat AI-assistenten het volgende kunnen doen:

* Uw OpenAPI-spec lezen en begrijpen
* API-aanroepen uitvoeren
* Uw documentatie doorzoeken
* Endpoint-details, request bodies, response-schema's en voorbeeldcodefragmenten ophalen

### Wat kunnen AI-assistenten doen via de MCP-server?

Nadat ze verbonden zijn met uw MCP-server, kunnen AI-assistenten:

* Beschikbare API-endpoints bekijken en weergeven
* Beveiligingsschema's en authenticatievereisten inspecteren
* Gedetailleerde endpoint-documentatie ophalen
* Gestructureerde request- en response-schema's opvragen
* Voorbeeldcodefragmenten genereren om uw API aan te roepen
* Uw bredere documentatie doorzoeken voor context en handleidingen

## MCP inschakelen & gebruiken

### Hoe schakel ik mijn MCP-server in ReadMe in?

Klik in de bewerkingsmodus in de rechterbovenhoek op **:sparkles:AI** om het zijpaneel te openen. Selecteer **MCP** en zet **MCP Server** aan om uw MCP-server te activeren. Zodra ingeschakeld, is uw MCP-URL:

`https://your-project.readme.com/mcp`

U kunt deze URL delen met uw ontwikkelaars zodat zij compatibele AI-tools (zoals Cursor) rechtstreeks kunnen verbinden met uw API en documentatie.

### Hoe test ik of mijn MCP-server werkt?

Nadat u MCP hebt ingeschakeld:

1. Open uw AI-editor (Cursor, VS Code, enz.).
2. Start een nieuw gesprek met de AI-assistent.
3. Stel vragen zoals:
   * "Hoe doe ik [veelvoorkomend gebruik]?"
   * "Laat me een voorbeeld zien van [API-functionaliteit]."
   * "Maak een [integratietype] met behulp van [uw API]."

Als alles correct is geconfigureerd, zou de assistent uw endpoints moeten kunnen ontdekken, uw documentatie kunnen lezen en werkende voorbeelden kunnen genereren.

### Kan ik bepalen welke endpoints beschikbaar zijn via MCP?

Ja. U kunt endpoints die u niet toegankelijk wilt maken via uw MCP-server uitschakelen onder **Ingeschakelde MCP-routes**. Alleen ingeschakelde routes zijn beschikbaar voor AI-assistenten via de MCP-tools.

## Tools & mogelijkheden

### Welke OpenAPI-tools zijn beschikbaar via MCP?

De MCP-server biedt verschillende OpenAPI-gerichte tools, waaronder:

* `execute-request` – Voer API-aanroepen rechtstreeks uit vanuit uw specificatie.
* `get-endpoint` – Haal gedetailleerde endpoint-informatie op.
* `get-request-body` – Toegang tot gestructureerde request-parameters.
* `get-response-schema` – Bekijk wat uw API retourneert.
* `list-endpoints` – Blader door alle beschikbare API-endpoints.
* `list-security-schemes` – Inspecteer authenticatievereisten.
* `search-schema` – Zoek door uw OpenAPI-schema.
* `get-code-snippet` – Genereer voorbeeldcode in uw voorkeurstaal.

### Welke documentatietools zijn beschikbaar?

Documentatietools richten zich op uw bredere kennisbank:

* `search` – Doorzoek uw volledige documentatieset op relevante inhoud.
* `fetch` – Geef een specifieke handleidingspagina terug.

<Callout icon="📘" theme="info">
  Voor documentatietools moet u uw huidige abonnement upgraden met het <Anchor label="AI Booster Pack" target="_blank" href="https://readme.com/pricing">AI Booster Pack</Anchor>.

  Voor Enterprise-klanten kunt u contact opnemen met uw CSM.

  Voor Startup- en Business-klanten kunt u uw abonnement upgraden met het AI Booster Pack via uw **Abonnement beheren**-pagina onder Instellingen.
</Callout>

## Configuratie & toegang

### Hoe werken branches met MCP?

Standaard verbindt de MCP-server met de nieuwste stabiele versie van uw project. Om een andere branch te gebruiken, voegt u `?branch=<name>` toe aan de MCP-URL. Wanneer u een branch-specifieke MCP-server gebruikt, is de `search-documentation`-functionaliteit niet beschikbaar.

### Hoe geef ik MCP toegang tot privéprojecten?

Voor privé- of beveiligde projecten moet u uw MCP-client configureren om een `x-readme-auth`-header te verzenden:

* **Wachtwoordbeveiligd**: `x-readme-auth` moet het sitewachtwoord zijn.
* **Alleen teamleden & Aangepaste login**: `x-readme-auth` moet een API-sleutel zijn in de vorm `bearer <api_key>`.

### Hoe kan ik verbindingsinstructies genereren voor mijn gebruikers?

Na het activeren van uw MCP-server klikt u op **MCP-sjabloon genereren** in uw project. Dit maakt een nieuwe, niet-gepubliceerde **MCP**-handleiding aan in de Handleidingen of API-referentie van uw project, onder een nieuwe categorie genaamd **MCP SERVER**. De handleiding bevat kant-en-klare instructies voor het verbinden met uw MCP-server vanuit tools zoals Cursor en Claude Desktop.

## Abonnementen, prijzen & vereisten

### Heb ik een specifiek abonnement of add-on nodig om MCP te gebruiken?

Alle ReadMe-projecten kunnen automatisch een MCP-server genereren zodra MCP is ingeschakeld. Sommige mogelijkheden (zoals Documentatietools) vereisen echter de **AI Booster Pack**-add-on. Enterprise-klanten kunnen contact opnemen met hun CSM, en Startup/Business-klanten kunnen upgraden via hun **Abonnement beheren**-pagina onder Instellingen.