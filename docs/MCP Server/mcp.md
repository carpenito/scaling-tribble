---
title: MCP
hidden: false
---
Kirb_TranslationsQA_Nov2025 模型上下文协议（MCP）服务器使 Cursor 和 Windsurf 等 AI 代码编辑器，以及 Claude Desktop 等通用工具，能够直接与您的 Kirb_TranslationsQA_Nov2025 API 和文档进行交互。

## 什么是 MCP？

模型上下文协议（MCP）是一种开放标准，允许 AI 应用程序安全地访问外部数据源和工具。Kirb_TranslationsQA_Nov2025 MCP 服务器为 AI 代理提供：

* **直接 API 访问** Kirb_TranslationsQA_Nov2025 功能
* **文档搜索**能力
* **实时数据**来自您的 Kirb_TranslationsQA_Nov2025 账户
* **代码生成**辅助，用于 Kirb_TranslationsQA_Nov2025 集成

## Kirb_TranslationsQA_Nov2025 MCP 服务器设置

Kirb_TranslationsQA_Nov2025 在 `https://kirbtranslationsqanov2025.readme.io/mcp` 托管了一个远程 MCP 服务器。请配置您的 AI 开发工具以连接到此服务器。如果您的 API 需要身份验证，您可以通过查询参数或 MCP 客户端中配置请求头的方式传入请求头。

<Tabs>
  <Tab title="Cursor">
    **添加到 `~/.cursor/mcp.json`：**

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
    **添加到 `~/.codeium/windsurf/mcp_config.json`：**

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
    **添加到 `claude_desktop_config.json`：**

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

## 测试您的 MCP 设置

配置完成后，您可以测试 MCP 服务器连接：

1. **打开您的 AI 编辑器**（Cursor、Windsurf 等）
2. **开启一个新对话**与 AI 助手
3. **询问有关 Kirb_TranslationsQA_Nov2025 的问题** - 尝试以下问题：
   * "我如何[常见用例]？"
   * "给我展示一个[API 功能]的示例"
   * "使用 Kirb_TranslationsQA_Nov2025 创建一个[集成类型]"

AI 现在应该可以通过 MCP 服务器访问您的 Kirb_TranslationsQA_Nov2025 账户数据和文档。