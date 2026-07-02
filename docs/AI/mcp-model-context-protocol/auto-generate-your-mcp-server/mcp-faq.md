---
title: MCP 常见问题
deprecated: false
hidden: false
metadata:
  robots: index
---
<br />

本 FAQ 解答了在 ReadMe 项目中使用 [Model Context Protocol (MCP)](https://modelcontextprotocol.io/introduction) 的常见问题。

## 常规问题

### 什么是 Model Context Protocol (MCP)？

Model Context Protocol (MCP) 是一种规范 AI 助手与 API 交互方式的标准。在 ReadMe 中，MCP 将您的 API 文档和 OpenAPI 定义转化为结构化资源，使 AI 工具能够理解、搜索并以编程方式调用它们。

### MCP 如何与我的 ReadMe 项目配合使用？

ReadMe 会为您的项目创建一个专属的 MCP 服务器。该服务器连接到您的 OpenAPI 规范和 [Ask AI](/docs/ask-ai) 功能，使 AI 助手能够：

* 读取并理解您的 OpenAPI 规范
* 执行 API 调用
* 搜索您的文档
* 获取端点详情、请求体、响应 schema 及示例代码片段

### AI 助手通过 MCP 服务器可以做什么？

连接到您的 MCP 服务器后，AI 助手可以：

* 浏览并列出可用的 API 端点
* 检查安全方案和身份验证要求
* 获取详细的端点文档
* 获取结构化的请求和响应 schema
* 生成调用您 API 的示例代码片段
* 在更广泛的文档中搜索上下文和指南

## 启用与使用 MCP

### 如何在 ReadMe 中启用我的 MCP 服务器？

在编辑模式下，点击右上角的 **:sparkles:AI** 打开侧边面板。选择 **MCP**，然后开启 **MCP Server** 开关以激活您的 MCP 服务器。启用后，您的 MCP URL 将为：

`https://your-project.readme.com/mcp`

您可以将此 URL 分享给您的开发者，让他们将兼容的 AI 工具（如 Cursor）直接连接到您的 API 和文档。

### 如何测试我的 MCP 服务器是否正常工作？

启用 MCP 后：

1. 打开您的 AI 编辑器（Cursor、VS Code 等）。
2. 与 AI 助手开启一个新对话。
3. 提出如下问题：
   * "如何实现 [常见用例]？"
   * "给我展示一个 [API 功能] 的示例。"
   * "使用 [您的 API] 创建一个 [集成类型]。"

如果配置正确，助手应能发现您的端点、读取您的文档并生成可用的示例。

### 我可以控制哪些端点通过 MCP 暴露吗？

可以。您可以在 **Enabled MCP Routes** 下禁用不希望通过 MCP 服务器访问的端点。只有已启用的路由才能通过 MCP 工具供 AI 助手使用。

## 工具与功能

### MCP 提供哪些 OpenAPI 工具？

MCP 服务器提供多种以 OpenAPI 为核心的工具，包括：

* `execute-request` – 直接根据您的规范发起 API 调用。
* `get-endpoint` – 获取详细的端点信息。
* `get-request-body` – 访问结构化的请求参数。
* `get-response-schema` – 查看您的 API 返回内容。
* `list-endpoints` – 浏览所有可用的 API 端点。
* `list-security-schemes` – 检查身份验证要求。
* `search-schema` – 在您的 OpenAPI schema 中搜索。
* `get-code-snippet` – 以您偏好的语言生成示例代码。

### 有哪些文档工具可用？

文档工具专注于您更广泛的知识库：

* `search` – 在您的整个文档集中搜索相关内容。
* `fetch` – 返回特定的指南页面。

<Callout icon="📘" theme="info">
  文档工具需要通过 <Anchor label="AI Booster Pack" target="_blank" href="https://readme.com/pricing">AI Booster Pack</Anchor> 升级您当前的套餐。

  Enterprise 客户请联系您的 CSM。

  Startup 和 Business 客户请在设置中的 **Manage Plan** 页面使用 AI Booster Pack 升级您的套餐。
</Callout>

## 配置与访问

### 分支如何与 MCP 配合使用？

默认情况下，MCP 服务器连接到您项目的最新稳定版本。若要指定不同的分支，请在 MCP URL 后附加 `?branch=<name>`。使用特定分支的 MCP 服务器时，`search-documentation` 功能将不可用。

### 如何允许 MCP 访问私有项目？

对于私有或受保护的项目，您需要配置 MCP 客户端以发送 `x-readme-auth` 请求头：

* **密码保护**：`x-readme-auth` 应为站点密码。
* **仅限团队成员 & 自定义登录**：`x-readme-auth` 应为格式为 `bearer <api_key>` 的 API 密钥。

### 如何为我的用户生成连接说明？

激活 MCP 服务器后，在您的项目中点击 **Generate MCP Template**。这将在您项目的指南或 API 参考中，在名为 **MCP SERVER** 的新分类下创建一个新的、未发布的 **MCP** 指南。该指南包含从 Cursor 和 Claude Desktop 等工具连接到您的 MCP 服务器的现成说明。

## 套餐、定价与要求

### 使用 MCP 是否需要特定套餐或附加组件？

所有 ReadMe 项目在启用 MCP 后均可自动生成 MCP 服务器。但某些功能（如文档工具）需要 **AI Booster Pack** 附加组件。Enterprise 客户请联系其 CSM，Startup/Business 客户可在设置中的 **Manage Plan** 页面进行升级。