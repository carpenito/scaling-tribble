---
title: MCP
hidden: false
---
De Kirb_TranslationsQA_Nov2025 Model Context Protocol (MCP) server stelt AI-gestuurde code-editors zoals Cursor en Windsurf, en algemene tools zoals Claude Desktop, in staat om rechtstreeks te communiceren met je Kirb_TranslationsQA_Nov2025 API en documentatie.

## Wat is MCP?

Model Context Protocol (MCP) is een open standaard waarmee AI-applicaties veilig toegang kunnen krijgen tot externe gegevensbronnen en tools. De Kirb_TranslationsQA_Nov2025 MCP server biedt AI-agents:

* **Directe API-toegang** tot Kirb_TranslationsQA_Nov2025-functionaliteit
* **Documentatiezoek**mogelijkheden
* **Realtime gegevens** uit je Kirb_TranslationsQA_Nov2025-account
* **Codegeneratie**-ondersteuning voor Kirb_TranslationsQA_Nov2025-integraties

## Kirb_TranslationsQA_Nov2025 MCP Server Instellen

Kirb_TranslationsQA_Nov2025 host een externe MCP server op `https://kirbtranslationsqanov2025.readme.io/mcp`. Configureer je AI-ontwikkeltools om verbinding te maken met deze server. Als je API's authenticatie vereisen, kun je headers meegeven via queryparameters of op de manier waarop headers worden geconfigureerd in je MCP-client.

<Tabs>
  <Tab title="Cursor">
    **Voeg toe aan `~/.cursor/mcp.json`:**

    ```json
    {
      "mcpServers": {
        "kirbtranslationsqanov2025": {
          "url": "https://kirbtranslationsqanov2025.readme.io/mcp"
        }
      }
    }
    ```

    </Tab>
  <Tab title="Windsurf">
    **Voeg toe aan `~/.codeium/windsurf/mcp_config.json`:**

    ```json
    {
      "mcpServers": {
        "kirbtranslationsqanov2025": {
          "url": "https://kirbtranslationsqanov2025.readme.io/mcp"
        }
      }
    }
    ```

  </Tab>
  <Tab title="Claude Desktop">
    **Voeg toe aan `claude_desktop_config.json`:**

    ```json
    {
      "mcpServers": {
        "kirbtranslationsqanov2025": {
          "url": "https://kirbtranslationsqanov2025.readme.io/mcp"
        }
      }
    }
    ```

  </Tab>
</Tabs>

## Je MCP-instelling Testen

Na de configuratie kun je de verbinding met je MCP server testen:

1. **Open je AI-editor** (Cursor, Windsurf, enz.)
2. **Start een nieuw gesprek** met de AI-assistent
3. **Stel een vraag over Kirb_TranslationsQA_Nov2025** - probeer vragen zoals:
   * "Hoe doe ik [veelvoorkomend gebruik]?"
   * "Laat me een voorbeeld zien van [API-functionaliteit]"
   * "Maak een [integratietype] met Kirb_TranslationsQA_Nov2025"

De AI heeft nu toegang tot de gegevens van je Kirb_TranslationsQA_Nov2025-account en de documentatie via de MCP server.