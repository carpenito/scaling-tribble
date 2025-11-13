---
title: Auto-Generate Your MCP Server
deprecated: false
hidden: false
metadata:
  robots: index
---
With ReadMe, every project automatically includes a fully configured MCP server. Simply enable MCP to connect your API documentation to AI tools.

## How to Generate Your Own MCP Server

In Edit Mode, in the top right-hand corner, click **:sparkles:AI** to open up the side panel. Select **MCP** and toggle MCP Server to activate your MCP server. Your MCP URL will be: `https://your-project.readme.com/mcp`. You can share your MCP URL with your developers, and they can connect their AI assistants and tools directly to your API. Endpoints you don't want accessible in your MCP server can be disabled under Enabled MCP Routes.

The AI should now have access to your ReadMe account data and documentation through the MCP server.

<Image align="center" border={false} width="35% " src="https://files.readme.io/f4981199e6757d7c7a64ff259c4c592ab97b8b91f91255804a6a5a8d696fbd9b-mcp_advanced.png" />

### Custom Tools

<br />

## Testing Your MCP Setup

Once configured, you can test your MCP server connection:

1. Open your AI editor (Cursor, VS Code, etc.)
2. Start a new chat with the AI assistant
3. Ask about your API & docs. Try these questions:
   * "How do I [common use case]?"
   * "Show me an example of [API functionality]"
   * "Create a [integration type] using [your API]

## How to Generate Access Instructions For Your Users

Once you have activated your MCP server, can automatically generate access instructions for your end-users by clicking the "Generate MCP Template" button. This creates a new unpublished doc called "MCP" in your Guides showing how to connect to your MCP server in tools such as Cursor and Claude Desktop. You can find the doc at the bottom of your Guides or API Reference in a new category called "MCP SERVER."
