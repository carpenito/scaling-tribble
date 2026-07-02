---
title: 主题
deprecated: false
hidden: false
metadata:
  robots: index
---
所有方案均可在 **主题** 设置中进行自定义。在管理界面左上角打开 **设置**，然后在侧边栏中选择 **主题**。

* 布局
* 品牌形象（Logo、网站图标和颜色）
* 页眉样式

<PlanTable currentPlan="Free" />

<Callout icon="💁‍♂️" theme="default">
  **注意：** 商业版和企业版方案提供更多自定义选项和服务。
</Callout>

***

## 布局

<Image align="center" border={false} width="400px" src="https://files.readme.io/3d30b1d7f55cd7e37def92bb05c5c4799bc0e1294169209626ff9a24181733cc-Launch_Week-20250628-1026262x.webp" />

您可以从 3 种布局选项中进行选择：经典、紧凑和现代。此外，还有一个选项可以为较大屏幕拉伸布局。保存前您可以预览布局效果。

<Callout icon="🚧" theme="warn">
  仅侧边栏选项即将推出！
</Callout>

***

## 品牌形象

### Logo

当某些主题和页眉颜色设置需要替代方案时，可选择上传白色 Logo。

**格式**

* 建议使用 SVG 以获得最佳质量。
* 如果您的 Logo 过于复杂而无法使用 SVG，WEBP 是一个不错的替代方案——使用所需 Logo 尺寸的 2 倍，以在高分辨率显示器上保持清晰度。
* 不支持 GIF 格式。

**尺寸**

* 默认高度为 24px。在经典和现代主题中，您可以选择更大的 40px 高度 Logo。

**进一步自定义**

* 拥有自定义 CSS 访问权限的客户可以使用我们的全局类和 CSS 变量进一步调整其 Logo 显示效果：

```css
.rm-Logo-img {
  --Header-logo-height: YOUR_CUSTOM_HEIGHT
}
```

***

## 页眉

<Image align="center" border={false} width="400px" src="https://files.readme.io/9c14d52d69809626037d9cb483cd2fb0619734f6ccc3c3428fd6380936a44b43-Launch_Week-20250628-1043112x.webp" />

您可以从 4 种布局选项中进行选择：线条、纯色、渐变和叠加。

<Callout icon="💁‍♂️" theme="default">
  线条页眉选项现在默认以标签页形式显示链接。使用旧版按钮显示的用户可以进行切换。一旦切换，将无法恢复。
</Callout>

**进一步自定义**

* 拥有自定义 CSS 访问权限的客户可以使用我们的全局类和 CSS 变量进一步调整其页眉：

```css
.rm-Header {
  --Header-background: YOUR_CUSTOM_VALUE /* defaults to your brand color */
  --Header-border-color: YOUR_CUSTOM_VALUE /* default: rgba(0, 0, 0, 0.1) */
  --Header-button-padding: YOUR_CUSTOM_VALUE /* default: 10px */

  /* Line theme only */
  --Header-tab-underline: YOUR_CUSTOM_VALUE /* defaults to your brand color */
}
```