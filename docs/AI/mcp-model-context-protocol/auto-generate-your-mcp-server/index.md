---
title: Genereer automatisch uw MCP-server
deprecated: false
hidden: false
metadata:
  robots: index
---
Met ReadMe bevat elk project automatisch een volledig geconfigureerde MCP-server. Schakel MCP eenvoudig in om uw API-documentatie te verbinden met AI-tools.

## Hoe u uw eigen MCP-server genereert

Klik in de bewerkingsmodus, in de rechterbovenhoek, op **:sparkles:AI** om het zijpaneel te openen. Selecteer **MCP** en zet de MCP-server aan om uw MCP-server te activeren. Uw MCP-URL wordt: `https://your-project.readme.com/mcp`. U kunt uw MCP-URL delen met uw ontwikkelaars, zodat zij hun AI-assistenten en tools rechtstreeks op uw API kunnen aansluiten. Endpoints die u niet toegankelijk wilt maken via uw MCP-server, kunnen worden uitgeschakeld onder Ingeschakelde MCP-routes.

De AI heeft nu toegang tot uw ReadMe-accountgegevens en documentatie via de MCP-server.

<Image align="center" border={false} width="35% " src="https://files.readme.io/f4981199e6757d7c7a64ff259c4c592ab97b8b91f91255804a6a5a8d696fbd9b-mcp_advanced.png" />

### Aangepaste tools

<br />

## Uw MCP-configuratie testen

Na de configuratie kunt u de verbinding met uw MCP-server testen:

1. Open uw AI-editor (Cursor, VS Code, enz.)
2. Start een nieuw gesprek met de AI-assistent
3. Stel vragen over uw API en documentatie. Probeer deze vragen:
   * "Hoe doe ik [veelvoorkomend gebruik]?"
   * "Laat me een voorbeeld zien van [API-functionaliteit]"
   * "Maak een [integratietype] met behulp van [uw API]"

## Hoe u toegangsinstructies genereert voor uw gebruikers

Zodra u uw MCP-server heeft geactiveerd, kunt u automatisch toegangsinstructies genereren voor uw eindgebruikers door op de knop "Generate MCP Template" te klikken. Dit maakt een nieuw niet-gepubliceerd document aan met de naam "MCP" in uw Handleidingen, waarin wordt uitgelegd hoe u verbinding maakt met uw MCP-server in tools zoals Cursor en Claude Desktop. U vindt het document onderaan uw Handleidingen of API-referentie in een nieuwe categorie genaamd "MCP SERVER".