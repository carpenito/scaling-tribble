---
title: 内置组件
deprecated: false
hidden: false
metadata:
  robots: index
---
ReadMe 提供了多个强大的 MDX 组件，开箱即用，可直接通过斜杠菜单访问。如需社区构建的组件，请在 **设置 > 自定义组件** 页面查看我们的 [Marketplace](https://docs.readme.com/main/docs/building-custom-mdx-components?isFramePreview=true#marketplace)。

### 标签页（Tabs）

<Image align="center" border={false} src="https://files.readme.io/336b9b02322ea3f7e522edd2cac1328f65179ecab4c7124dadaa012d1453e8eb-Editing_Tab_MDX_Component_1.gif" />

将相关内容整理成易于导航的分区：

**标签页示例**

<Tabs>
  <Tab title="第一个标签页">
    欢迎查看仅在第一个标签页中显示的内容。
  </Tab>

  <Tab title="第二个标签页">
    这是仅在第二个标签页中显示的内容。
  </Tab>

  <Tab title="第三个标签页">
    这是仅在第三个标签页中显示的内容。
  </Tab>
</Tabs>

***

### 折叠面板（Accordion）

<Image align="center" border={false} src="https://files.readme.io/a29c8744b62ec4b51e366e91a012533f9c6e21638db2c425358cec92a7058d7d-CleanShot_2024-11-08_at_20.10.29.gif" />

以可折叠的方式呈现信息：

**折叠面板示例**

<Accordion title="我的折叠面板标题" icon="fa-info-circle">
  Lorem ipsum dolor sit amet，**consectetur adipiscing elit。** Ut enim
  ad minim veniam，quis nostrud exercitation ullamco。Excepteur sint
  occaecat cupidatat non proident！
</Accordion>

***

### 卡片（Cards）

<Image align="center" border={false} src="https://files.readme.io/8702f98924ba19d8c0f1041e999fb6c3dc0dce5e15ead63e5e07f846fc4a28a8-CleanShot_2024-11-09_at_13.12.09.gif" />

以简洁的网格格式展示内容：

**卡片示例**

<Cards columns={3}>
  <Card title="第一张卡片" href="https://readme.com" icon="fa-home" target="_blank">
    Neque porro quisquam est qui dolorem ipsum quia
  </Card>

  <Card title="第二张卡片" icon="fa-user">
    *Lorem ipsum dolor sit amet, consectetur adipiscing elit*
  </Card>

  <Card title="第三张卡片" icon="fa-star">
    > Ut enim ad minim veniam, quis nostrud ullamco
  </Card>
</Cards>

***

### 多列布局（Columns）

创建多列布局，使内容并排显示而非垂直堆叠。

<Columns layout="auto">
  <Column>
    Neque porro quisquam est qui dolorem ipsum quia
  </Column>

  <Column>
    *Lorem ipsum dolor sit amet, consectetur adipiscing elit*
  </Column>

  <Column>
    > Ut enim ad minim veniam, quis nostrud ullamco
  </Column>
</Columns>