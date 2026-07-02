---
title: MCP（模型上下文协议）
deprecated: false
hidden: false
metadata:
  robots: index
---
[Model Context Protocol (MCP)](https://modelcontextprotocol.io/introduction) 是 AI 助手与 API 交互方式的标准化规范，ReadMe 正将这一能力引入您的开发者中心。借助 MCP 服务器，您可以将 API 文档转换为结构化资源，使 AI 助手能够以编程方式理解并与之交互。

## 主要功能

* **自定义工具**：定义自定义工作流和端点组合。<Badge label="New" bgColor="var(--purple)" textColor="var(--purple100)" cornerRadius="30px" />
* **启用路由**：禁用您不希望在 MCP 服务器中访问的端点 <Badge label="New" bgColor="var(--purple)" textColor="var(--purple100)" cornerRadius="30px" />
* **OpenAPI 集成**：从现有的 OpenAPI 规范生成 MCP 服务器。
* **AI 助手可连接到您的 MCP 服务器以**：
  * 读取并理解您的 OpenAPI 规范。
  * 执行 API 调用。
  * 使用 [Ask AI](/docs/ask-ai) 搜索文档。
* **MCP 工具**：
  * **OpenAPI 工具**：
    * `execute-request` - 直接从您的规范发起 API 调用
    * `get-endpoint` - 按需获取详细的端点信息
    * `get-request-body` - 访问结构化的请求参数
    * `get-response-schema` - 了解您的 API 返回内容
    * `list-endpoints` - 浏览所有可用的 API 端点
    * `list-security-schemes` - 访问身份验证要求
    * `search-schema` - 在您的 API 规范中精确查找所需内容
    * `get-code-snippet` - 以您偏好的语言获取与端点交互的示例代码片段。
  * **文档工具**：
    * `search` - 在整个知识库中搜索相关信息
    * `fetch` - 返回指南页面

<Callout icon="📘" theme="info">
  文档工具需要通过 <Anchor label="AI Booster Pack" target="_blank" href="https://readme.com/pricing">AI Booster Pack</Anchor> 升级您当前的套餐。

  企业客户请联系您的客户成功经理（CSM）。

  初创版和商业版客户，请在设置中的**管理套餐**页面通过 AI Booster Pack 升级您的套餐。
</Callout>

## 工作原理

我们创建一个专用的 MCP 服务器，将其连接到您的 OpenAPI 规范和 [Ask AI](/docs/ask-ai) 功能。这在您的 API 文档与 AI 助手之间建立了一座桥梁，使您的 API 对 AI 工具而言更易访问、更易理解。

## 额外功能

* **分支** 默认情况下，MCP 服务器连接到最新的稳定版本。若要选择其他分支，请在 MCP URL 后附加 `?branch=<name>`。注意：当您处于某个分支时，`search-documentation` 将不可用。
* **私有项目** 若要访问受保护的项目，您需要配置 MCP 客户端以发送 `x-readme-auth` 请求头
  * 密码保护：`x-readme-auth` 应为站点密码
  * 仅限团队成员 & 自定义登录：`x-readme-auth` 应为格式为 `bearer <api_key>` 的 API 密钥

## MCP 入门指南

选择您希望开始使用 MCP 的方式：

1. <Anchor label="Auto-Generate Your Own MCP Server" target="_blank" href="doc:generate-your-own-mcp-server">自动生成您自己的 MCP 服务器</Anchor>：每个 ReadMe 项目都自动包含一个完整配置的 MCP 服务器。只需启用 MCP，即可将您的 API 文档连接到 AI 工具。
2. <Anchor label="Use ReadMe’s MCP Server" target="_blank" href="doc:readmes-mcp-server">使用 ReadMe 的 MCP 服务器</Anchor>：借助 ReadMe 的 MCP 服务器，您可以通过我们的 API 直接完成在 ReadMe 中通常会做的一切操作，例如添加和编辑页面。