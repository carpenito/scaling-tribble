---
title: 自定义图标
deprecated: false
hidden: false
metadata:
  robots: index
---
## Font Awesome

ReadMe 加载了 Font Awesome 6 的 [Regular](https://fontawesome.com/search?s=regular\&f=classic\&o=r) 和 [Duotone](https://fontawesome.com/search?s=solid\&f=duotone\&o=r) 图标库，您可以在文档中使用它们！

<HTMLBlock>{`
<div class="Flex">
  <i class="fa-duotone fa-solid fa-house"></i>
  <i class="fa-duotone fa-solid fa-copyright"></i>
  <i class="fa-duotone fa-solid fa-bomb"></i>
  <i class="fa-duotone fa-solid fa-umbrella"></i>
  <i class="fa-duotone fa-solid fa-paper-plane"></i>
  <i class="fa-duotone fa-solid fa-computer-classic"></i>
  <i class="fa-duotone fa-solid fa-crab"></i>
  <i class="fa-duotone fa-solid fa-bullseye-pointer"></i>
  <i class="fa-duotone fa-solid fa-wheelchair-move"></i>
  <i class="fa-duotone fa-solid fa-table-tennis-paddle-ball"></i>
</div>
`}</HTMLBlock>

```
<i class="fa-duotone fa-solid fa-house"></i>
<i class="fa-duotone fa-solid fa-copyright"></i>
<i class="fa-duotone fa-solid fa-bomb"></i>
<i class="fa-duotone fa-solid fa-umbrella"></i>
<i class="fa-duotone fa-solid fa-paper-plane"></i>
<i class="fa-duotone fa-solid fa-computer-classic"></i>
<i class="fa-duotone fa-solid fa-crab"></i>
<i class="fa-duotone fa-solid fa-bullseye-pointer"></i>
<i class="fa-duotone fa-solid fa-wheelchair-move"></i>
<i class="fa-duotone fa-solid fa-table-tennis-paddle-ball"></i>
```

***

### 无障碍访问

如果图标仅用于装饰目的，可以将其标记为隐藏。例如，将其与适当的文字标签一起使用时：

```html
<button>
  <i aria-hidden="true" class="fa-duotone fa-solid fa-computer-classic"></i>
  Download to Floppy
</button>
```

如果您的图标需要具有语义含义，请使用 `aria-label` 属性：

```html
<i aria-label="Download to Floppy" class="fa-duotone fa-solid fa-computer-classic"></i>
```

您可以参阅 Font Awesome 的[无障碍访问文档](https://docs.fontawesome.com/web/dig-deeper/accessibility)以获取更多信息。