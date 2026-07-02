---
title: 自定义 CSS 和 JavaScript
deprecated: false
hidden: false
metadata:
  robots: index
---
在本节中，您可以添加 CSS 和 Javascript 来进一步自定义文档站点的外观。

<Image align="center" border={true} src="https://files.readme.io/ca07f17-CleanShot_2022-09-25_at_09.57.452x.png" className="border" />

> 🚧 选择器
>
> 请使用 `.rm-` 前缀的选择器。哈希选择器会不断变化，**不应**将其作为选择器使用（例如 `Header-bottom2eLKOFXMEmh5`）。

## 自定义样式表

<Callout icon="📘" theme="info">
  您应将更改限制在细微调整范围内。此外，样式表不受版本控制；所有版本使用同一个样式表。
</Callout>

## 自定义 Javascript

您的 Javascript 将被包含在页面底部。

<details>
  <summary><b>全局变量</b></summary>

  ReadMe 提供了某些全局变量，以帮助您自定义 hub 的用户体验：

  * **`RM_ReferenceSidebarScrollTopOffset`**\
    在连续 <Glossary>参考</Glossary> 章节中，滚动到活动项目侧边栏逻辑的像素偏移量。
</details>

## 自定义包含标签

**Header HTML**

此处的任何 HTML 都将包含在 head 标签中，适用于 meta 标签以及加载外部 CSS 或 JS 等场景。

**Footer HTML**  
​  
这将放置在 `</body>` 标签之前。适用于分析和跟踪等场景。

## 切换自定义 Javascript 和 CSS

在任意 URL 末尾添加 `?disableCustomCss=true&disableCustomJs=true` 查询参数。