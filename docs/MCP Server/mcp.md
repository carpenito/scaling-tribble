---
title: MCP
hidden: false
---
Le serveur Model Context Protocol (MCP) de Kirb_TranslationsQA_Nov2025 permet aux éditeurs de code alimentés par l'IA, comme Cursor et Windsurf, ainsi qu'aux outils polyvalents comme Claude Desktop, d'interagir directement avec votre API et votre documentation Kirb_TranslationsQA_Nov2025.

## Qu'est-ce que MCP ?

Model Context Protocol (MCP) est un standard ouvert qui permet aux applications d'IA d'accéder de manière sécurisée à des sources de données et des outils externes. Le serveur MCP de Kirb_TranslationsQA_Nov2025 fournit aux agents IA :

* **Un accès direct à l'API** des fonctionnalités de Kirb_TranslationsQA_Nov2025
* Des capacités de **recherche dans la documentation**
* Des **données en temps réel** depuis votre compte Kirb_TranslationsQA_Nov2025
* Une assistance à la **génération de code** pour les intégrations Kirb_TranslationsQA_Nov2025

## Configuration du serveur MCP de Kirb_TranslationsQA_Nov2025

Kirb_TranslationsQA_Nov2025 héberge un serveur MCP distant à l'adresse `https://kirbtranslationsqanov2025.readme.io/mcp`. Configurez vos outils de développement IA pour vous connecter à ce serveur. Si vos API nécessitent une authentification, vous pouvez transmettre des en-têtes via des paramètres de requête ou selon la méthode de configuration des en-têtes dans votre client MCP.

<Tabs>
  <Tab title="Cursor">
    **Ajoutez à `~/.cursor/mcp.json` :**

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
    **Ajoutez à `~/.codeium/windsurf/mcp_config.json` :**

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
    **Ajoutez à `claude_desktop_config.json` :**

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

## Tester votre configuration MCP

Une fois configuré, vous pouvez tester la connexion à votre serveur MCP :

1. **Ouvrez votre éditeur IA** (Cursor, Windsurf, etc.)
2. **Démarrez une nouvelle conversation** avec l'assistant IA
3. **Posez des questions sur Kirb_TranslationsQA_Nov2025** - essayez des questions comme :
   * « Comment puis-je [cas d'utilisation courant] ? »
   * « Montrez-moi un exemple de [fonctionnalité API] »
   * « Créez une [type d'intégration] en utilisant Kirb_TranslationsQA_Nov2025 »

L'IA devrait désormais avoir accès aux données de votre compte Kirb_TranslationsQA_Nov2025 et à la documentation via le serveur MCP.