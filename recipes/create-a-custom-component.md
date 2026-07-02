---
title: 创建自定义组件
description: |-
  食谱描述：本食谱将引导您创建一个简单的可复用样式容器，您可以在整个文档中使用它。

  只需用 ExampleComponent 标签包裹任意内容，它就会显示在一个漂亮的深灰色框中！
hidden: false
recipe:
  color: '#018FF4'
  icon: 🔧
---
```java Java
export const ExampleComponent = ({ children }) => {
  return (
    <div className="flex items-center h-full w-full">
      <div className="bg-gray-800 rounded-md p-6 m-4">
        {children}
      </div>
    </div>
  );
};

<ExampleComponent>
  Here's a very simple example component rather than an empty state. This should help you figure out what's happening quicker and see what's possible with custom components!
</ExampleComponent>
```

```json Response Example
{"success":true}
```

# 创建 ExampleComponent

<!-- java@1 -->

我们正在创建一个名为 ExampleComponent 的 React 组件。

export 关键字使该组件可以在其他地方被导入使用。

({ children }) 使用解构来访问放置在组件开闭标签之间的任何内容。

# 构建组件结构

<!-- java@2-8 -->

return (...) 定义了组件将渲染的内容，外层 <div> 使用 Tailwind CSS 类来使其内容居中，并占据完整的宽度和高度。

内层 <div> 创建一个带有圆角和内边距的深灰色框。

{children} 是魔法发生的地方——它将渲染您放置在组件标签之间的任何内容。

# 使用组件

<!-- java@11-13 -->

<ExampleComponent> 用于打开组件。

标签之间的文本将成为 children 属性的值。

最后，</ExampleComponent> 用于关闭组件。