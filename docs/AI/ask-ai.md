---
title: Ask AI
deprecated: false
hidden: false
metadata:
  robots: index
---
您的用户可以通过 Ask AI 即时获取有关您产品的答案。该助手使用您选择的模型，基于您的文档进行训练，提供准确、具有上下文感知能力的回答。它还包含指向您文档的直接链接，让用户可以深入探索相关主题。

***

## 终端用户预览

当您的用户与 Ask AI 互动时，它将打开助手并显示您自定义的示例问题，并根据您在管理面板中的配置提供回答。回答仅会引用公开页面的内容。对于同时拥有公开和私有项目的企业群组，Ask AI 将根据用户对项目的查看权限提供相应信息。

<Image align="center" border={false} width="750px" src="https://files.readme.io/93bba5b92a2c954d7aa1b5847d3648837ac31668b9861e35479e7a906596b3ab-user_gif.gif" />

## 配置

自定义 AI 助手的语气、回答长度和禁用内容，以符合您的品牌风格。为终端用户设置示例问题，并选择适合您需求的可用模型。

<Image align="center" border={false} src="https://files.readme.io/afc7f66444d7c8186118082c46a34ed5a8af5bbdfdb65cc9af97f8fba3969724-Ask_AI.png" />

### 企业群组

上述所有配置均可在您的群组控制台中用于企业项目。在群组级别进行的自定义设置将应用于所有对应的子项目。

## 分析

深入了解用户问题、回答和反馈，以了解用户的需求以及助手的表现效果。您可以在**设置**下的 **Ask AI 控制台**中查看所有分析数据。如需与团队共享洞察，可按自定义日期范围将数据导出为 CSV 文件。导出过程可能需要一些时间，具体取决于数据量，但准备就绪后，下载将立即在您的浏览器中开始。

<Image align="center" border={false} width="650px" src="https://files.readme.io/27af66805d9c4eb18c468750023284c9682c2734dd2422bb650d7408b98a4787-analytics.png" />

<br />

## 常见问题

<Accordion title="我的数据会如何处理？" icon="fa-chart-simple">
  Ask AI 由 OpenAI 的 API 提供支持，Markdown 内容以及 API 定义会被发送给 OpenAI 以生成用户问题的答案。
  虽然 OpenAI 会将这些 API 请求的日志保留 30 天，但不会使用任何数据来训练其 AI 模型。
</Accordion>

<Accordion title="Ask AI 会引用隐藏页面吗？" icon="fa-user-ninja">
  不会，隐藏页面永远不会被 Ask AI 索引。
  对于企业群组，仅使用用户有权访问的项目内容来回答问题。
</Accordion>

<Accordion title="Ask AI 的模型多久更新一次新内容？" icon="fa-swap">
  目前，新内容每 2 小时更新一次，但随着我们持续开发 Ask AI，这一频率可能会有所变化。
</Accordion>

<Accordion title="提供哪些工具来监控回答？" icon="fa-monitor-waveform">
  每个问题和答案的日志均可在管理控制台中查看。请参阅上方的[分析](https://docs.readme.com/maindocs/ask-ai#analytics)部分。
</Accordion>

<Accordion title="如何试用 Ask AI？" icon="fa-sparkles">
  您可以在 ReadMe 的文档上或在您自己的文档上以试用方式测试 Ask AI。
</Accordion>

<Accordion title="我正在使用旧版 Ask AI 体验。在哪里可以找到这些设置？" icon="fa-robot">
  您可以从 Ask AI 面板中的配置面板升级到新体验。升级是永久性的，无法撤销。
</Accordion>