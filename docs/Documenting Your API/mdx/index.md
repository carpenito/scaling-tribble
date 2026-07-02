---
title: MDX
deprecated: false
hidden: false
metadata:
  robots: index
---
在 ReadMe 中编写文档使用的是 [Markdown eXtended](https://mdxjs.com)（MDX），它基于 [CommonMark 规范](https://commonmark.org)。与纯 Markdown 不同，MDX 使用一种略有不同的语法，称为 [Javascript XML](https://react.dev/learn/writing-markup-with-jsx)（JSX）。如果你尝试编写 HTML，MDX 与 Markdown 在写法上存在一些细微差异。

## Markdown 与 MDX

ReadMe 中的所有页面均使用 MDX，以便你能够编写可复用的交互式组件。通常情况下，编写 Markdown 时不会有太大区别——除非你在编写 HTML。它_看起来_像 HTML，但语法更为严格。最常见的问题是 JSX 中不能使用自闭合标签：

<Columns layout="auto">
  <Column>
    <i className="fa-duotone fa-solid fa-square-x" /> 无效

    ```
    <br>
    <img>
    <hr>
    ```
  </Column>

  <Column>
    <i className="fa-duotone fa-solid fa-circle-check" /> 有效

    ```
    <br />
    <img />
    <hr />
    ```
  </Column>
</Columns>

所有 JSX 风格的标签必须显式关闭，包括自闭合标签。

<Columns layout="auto">
  <Column>
    <i className="fa-duotone fa-solid fa-square-x" /> 无效

    ```
    <p>Content
    <ul>
      <li>1
      <li>2
      <li>3
    </ul>
    ```
  </Column>

  <Column>
    <i className="fa-duotone fa-solid fa-circle-check" /> 有效

    ```
    <p>Content</p>
    <ul>
      <li>1</li>
      <li>2</li>
      <li>3</li>
    </ul>
    ```
  </Column>
</Columns>

大多数属性需要使用驼峰命名法——除了 `data-` 和 `aria-`。内联样式需要以对象形式 `{}` 书写，且在 JSX 中编写时这些属性也必须使用驼峰命名法（如果你在 `<style />` 标签中编写 CSS 则不适用）。

<Columns layout="auto">
  <Column>
    <i className="fa-duotone fa-solid fa-square-x" /> 无效

    ```
    <img 
      aria-label="my label" 
      class="my-class" 
      style="
        margin-left: auto; 
        margin-right: auto;
      "
    >
    ```
  </Column>

  <Column>
    <i className="fa-duotone fa-solid fa-circle-check" /> 有效

    ```
    <img 
      aria-label="my label" 
      className="my-class" 
      style={{ 
        marginLeft: 'auto', 
        marginRight: 'auto' 
      }}
    />
    ```
  </Column>
</Columns>

<HTMLBlock>{`
<style>
  .fa-square-x {
    color: var(--red);
  }

  .fa-circle-check {
    color: var(--green);
  }
</style>
`}</HTMLBlock>

<Callout icon="📘" theme="info">
  **提示：** 如果你在使用 MDX 时遇到其他问题或错误，请查看 [MDX 错误排查](https://docs.readme.com/main/docs/rendering-errors-invalid-mdx) 了解更多常见问题。
</Callout>

## 编写 JSX

<Image align="center" border={false} src="https://files.readme.io/a29c8744b62ec4b51e366e91a012533f9c6e21638db2c425358cec92a7058d7d-CleanShot_2024-11-08_at_20.10.29.gif" />

在编辑文档时，你可以通过以下几种方式编写动态 JSX 组件：

1. **在页面中：** 直接以纯文本形式编写 JSX。编辑器会自动解析你的语法并高亮显示 JSX 内容。

2. **[复用组件](https://docs.readme.com/main/v3.0_move-rdme/docs/building-custom-mdx-components/)：** 若要编写可在任意页面复用的组件，请打开 **设置**，导航至 **自定义组件** 页面。编写好第一个组件后，即可在任意页面复用：`<ExampleComponent />`

3. **[开箱即用](https://docs.readme.com/main/v3.0_move-rdme/docs/built-in-components/)：** 我们的编辑器让你可以轻松使用我们内置于 ReadMe 的组件。你可以在编辑器中输入 `/` 打开命令菜单来查找它们。在 **组件** 部分，你可以选择 `Tabs`、`Accordion`、`Columns` 或 `Cards` 组件。

4. **公共组件：** 我们还维护了一个[组件市场](https://github.com/readmeio/marketplace)，任何人都可以在其中提交组件。