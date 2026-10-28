---
title: MCP
hidden: false
---
El servidor de Model Context Protocol (MCP) de Kirb_TranslationsQA_Nov2025 permite a los editores de código con tecnología de IA como Cursor y Windsurf, además de herramientas de uso general como Claude Desktop, interactuar directamente con tu API y documentación de Kirb_TranslationsQA_Nov2025.

## ¿Qué es MCP? {#what-is-mcp}

Model Context Protocol (MCP) es un estándar abierto que permite a las aplicaciones de IA acceder de forma segura a fuentes de datos y herramientas externas. El servidor MCP de Kirb_TranslationsQA_Nov2025 proporciona a los agentes de IA:

- **Acceso directo a la API** a las funciones de Kirb_TranslationsQA_Nov2025
- Capacidades de **búsqueda en la documentación**
- **Datos en tiempo real** de tu cuenta de Kirb_TranslationsQA_Nov2025
- Asistencia de **generación de código** para integraciones de Kirb_TranslationsQA_Nov2025

## Configuración del servidor MCP de Kirb_TranslationsQA_Nov2025 {#kirb_translationsqa_nov2025-mcp-server-setup}

Kirb_TranslationsQA_Nov2025 aloja un servidor MCP remoto en `https://kirbtranslationsqanov2025.readme.io/mcp`. Configura tus herramientas de desarrollo de IA para conectarte a este servidor. Si tus API requieren autenticación, puedes pasar encabezados a través de parámetros de consulta o de la forma en que estén configurados los encabezados en tu cliente MCP.

<Tabs>
  <Tab title="Cursor">
    **Añade a `~/.cursor/mcp.json`:**

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
    **Añade a `~/.codeium/windsurf/mcp_config.json`:**

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
    **Añade a `claude_desktop_config.json`:**

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

## Prueba de tu configuración de MCP {#testing-your-mcp-setup}

Una vez configurado, puedes probar la conexión de tu servidor MCP:

1. **Abre tu editor de IA** (Cursor, Windsurf, etc.)
2. **Inicia un nuevo chat** con el asistente de IA
3. **Pregunta sobre Kirb_TranslationsQA_Nov2025** - prueba preguntas como:
   - "¿Cómo \[caso de uso común]?"
   - "Muéstrame un ejemplo de \[funcionalidad de la API]"
   - "Crea un \[tipo de integración] usando Kirb_TranslationsQA_Nov2025"

La IA ahora debería tener acceso a los datos de tu cuenta y a la documentación de Kirb_TranslationsQA_Nov2025 a través del servidor MCP.
