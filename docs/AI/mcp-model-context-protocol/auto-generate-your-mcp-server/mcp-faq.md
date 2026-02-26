---
title: MCP FAQ
deprecated: false
hidden: false
metadata:
  robots: index
---
<br />

This FAQ answers common questions about using [Model Context Protocol (MCP)](https://modelcontextprotocol.io/introduction) with ReadMe projects.

## General

### What is the Model Context Protocol (MCP)?

Model Context Protocol (MCP) is a standard for how AI assistants interact with APIs. In ReadMe, MCP turns your API documentation and OpenAPI definition into a structured resource that AI tools can understand, search, and call programmatically.

### How does MCP work with my ReadMe project?

ReadMe creates a dedicated MCP server for your project. This server connects to your OpenAPI specification and your [Ask AI](/docs/ask-ai) functionality, so AI assistants can:

* Read and understand your OpenAPI spec
* Execute API calls
* Search your docs
* Pull in endpoint details, request bodies, response schemas, and example code snippets

### What can AI assistants do through the MCP server?

Once connected to your MCP server, AI assistants can:

* Browse and list available API endpoints
* Inspect security schemes and authentication requirements
* Fetch detailed endpoint documentation
* Get structured request and response schemas
* Generate example code snippets to call your API
* Search your broader documentation for context and guides

## Enabling & Using MCP

### How do I enable my MCP server in ReadMe?

In Edit Mode, in the top right-hand corner, click **:sparkles:AI** to open the side panel. Select **MCP** and toggle **MCP Server** on to activate your MCP server. Once enabled, your MCP URL will be:

`https://your-project.readme.com/mcp`

You can share this URL with your developers so they can connect compatible AI tools (like Cursor) directly to your API and docs.

### How do I test that my MCP server is working?

Once you’ve enabled MCP:

1. Open your AI editor (Cursor, VS Code, etc.).
2. Start a new chat with the AI assistant.
3. Ask questions like:
   * "How do I [common use case]?"
   * "Show me an example of [API functionality]."
   * "Create a [integration type] using [your API]."

If configured correctly, the assistant should be able to discover your endpoints, read your docs, and generate working examples.

### Can I control which endpoints are exposed via MCP?

Yes. You can disable endpoints you don’t want accessible from your MCP server under **Enabled MCP Routes**. Only enabled routes will be available to AI assistants through the MCP tools.

## Tools & Capabilities

### What OpenAPI tools are available through MCP?

The MCP server exposes several OpenAPI-focused tools, including:

* `execute-request` – Make API calls directly from your specification.
* `get-endpoint` – Retrieve detailed endpoint information.
* `get-request-body` – Access structured request parameters.
* `get-response-schema` – View what your API returns.
* `list-endpoints` – Browse all available API endpoints.
* `list-security-schemes` – Inspect authentication requirements.
* `search-schema` – Search across your OpenAPI schema.
* `get-code-snippet` – Generate example code in your preferred language.

### What documentation tools are available?

Documentation tools focus on your broader knowledge base:

* `search` – Search your entire documentation set for relevant content.
* `fetch` – Return a specific guides page.

<Callout icon="📘" theme="info">
  Documentation tools require upgrading your current plan with the <Anchor label="AI Booster Pack" target="_blank" href="https://readme.com/pricing">AI Booster Pack</Anchor>.

  For Enterprise customers, please reach out to your CSM.

  For Startup and Business customers, please upgrade your plan with the AI Booster Pack from your **Manage Plan** page under Settings.
</Callout>

## Configuration & Access

### How do branches work with MCP?

By default, the MCP server connects to the latest stable version of your project. To target a different branch, append `?branch=<name>` to the MCP URL. When using a branch-specific MCP server, the `search-documentation` functionality will not be available.

### How do I allow MCP to access private projects?

For private or protected projects, you’ll need to configure your MCP client to send an `x-readme-auth` header:

* **Password protected**: `x-readme-auth` should be the site password.
* **Teammates only & Custom login**: `x-readme-auth` should be an API key in the form `bearer <api_key>`.

### How can I generate connection instructions for my users?

After activating your MCP server, click **Generate MCP Template** in your project. This creates a new, unpublished **MCP** guide in your project’s Guides or API Reference, under a new category called **MCP SERVER**. The guide includes ready-made instructions for connecting to your MCP server from tools like Cursor and Claude Desktop.

## Plans, Pricing & Requirements

### Do I need a specific plan or add-on to use MCP?

All ReadMe projects can auto-generate an MCP server once MCP is enabled. However, some capabilities (like Documentation Tools) require the **AI Booster Pack** add-on. Enterprise customers should contact their CSM, and Startup/Business customers can upgrade from their **Manage Plan** page under Settings.
