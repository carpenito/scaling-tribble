---
title: MCP (Model Context Protocol)
deprecated: false
hidden: false
metadata:
  robots: index
---
[Model Context Protocol (MCP)](https://modelcontextprotocol.io/introduction) is a standardization of how AI assistants interact with APIs, and ReadMe is bringing this capability to your developer hub. With MCP servers, you can convert your API documentation into a structured, resource that AI assistants can understand and interact with programmatically.

## Key Features

* **Custom Tooling**: Define custom workflow and endpoint combinations. <Badge label="New" bgColor="var(--purple)" textColor="var(--purple100)" cornerRadius="30px" />
* **Enabled Routes**: Disable endpoints you don’t want accessible in your MCP server <Badge label="New" bgColor="var(--purple)" textColor="var(--purple100)" cornerRadius="30px" />
* **OpenAPI Integration**: Generate an MCP server from your existing OpenAPI specification.
* **AI assistants can connect to your MCP server to**:
  * Read and understand your OpenAPI spec.
  * Execute API calls.
  * Search docs with [Ask AI](/docs/ask-ai).
* **MCP Tools**:
  * **OpenAPI Tools**:
    * `execute-request` - Make API calls directly from your specification
    * `get-endpoint` - Pull in detailed endpoint information on demand
    * `get-request-body` - Access structured request parameters
    * `get-response-schema` - Understand what your API returns
    * `list-endpoints` - Browse all available API endpoints
    * `list-security-schemes` - Access authentication requirements
    * `search-schema` - Find exactly what you need in your API spec
    * `get-code-snippet` - Example code snippets in your preferred language to interact with your endpoint.
  * **Documentation Tools**:
    * `search` - Search your entire knowledge base for relevant information
    * `fetch` - Return a guides page

<Callout icon="📘" theme="info">
  Documentation Tools require upgrading your current plan with the <Anchor label="AI Booster Pack" target="_blank" href="https://readme.com/pricing">AI Booster Pack</Anchor>.

  For Enterprise customers, please reach out to your CSM.

  For Startup and Business customers, please upgrade your plan with the AI Booster Pack from your **Manage Plan** page under Settings.
</Callout>

## How It Works

We create a dedicated MCP server that connects to your OpenAPI specification and [Ask AI](/docs/ask-ai) functionality. This creates a bridge between your API documentation and AI assistants, making your API instantly more accessible and understandable to AI tools.

## Extra Features

* **Branches** By default, the MCP server is connected to the latest stable version. To chose a different branch append `?branch=<name>` to the MCP url. NOTE: When you are on a branch `search-documentation` will not be available.
* **Private Projects** To access protected projects, you will need to configure your MCP client to send a `x-readme-auth` header
  * Password protected: `x-readme-auth` should be the site password
  * Teammates only & Custom login: `x-readme-auth` should be an api key in the form `bearer <api_key>`

## Getting Started with MCP

Choose how you’d like to start working with MCP:

1. <Anchor label="Auto-Generate Your Own MCP Server" target="_blank" href="doc:generate-your-own-mcp-server">Auto-Generate Your Own MCP Server</Anchor>: Every ReadMe project automatically includes a fully configured MCP server. Simply enable MCP to connect your API documentation to AI tools.
2. <Anchor label="Use ReadMe’s MCP Server" target="_blank" href="doc:readmes-mcp-server">Use ReadMe’s MCP Server</Anchor>: With ReadMe’s MCP server, you can do everything you normally would in ReadMe, like adding and editing pages, directly through our API.
