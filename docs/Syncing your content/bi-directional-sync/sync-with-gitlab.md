---
title: 与 GitLab 同步
deprecated: false
hidden: false
metadata:
  robots: index
---
## 如何设置与 GitLab 的双向同步

### 前提条件

* 您需要一个 GitLab 账户。
* 在与组织中的仓库同步时，您需要具有创建**空仓库**的权限。

<Image align="center" border={false} src="https://files.readme.io/d2a12db436be321b972fd817432f3754a13d61c0ecb915202862e58fb2252cc1-Screenshot_2025-10-31_at_1.43.41_PM.png" />

### 设置步骤

1. 导航至 **Settings** > **Git Connection** 页面。
2. 选择 GitLab。
3. 如果尚未创建，请在 [GitLab](https://docs.gitlab.com/user/project/) 中创建一个空仓库——请确保取消勾选创建 README 的选项。
4. 与您的提供商进行 **Sync**（同步）并完成身份验证。
5. 创建一个具有 `api` 权限范围的个人访问令牌。完成设置后可删除此令牌。ReadMe 仅在设置过程中使用该令牌在您的仓库中创建 webhook，且不会存储该令牌。
   1. 对于项目访问令牌，您需要具备 Maintainer 角色。但不建议使用此方式，因为根据 GitLab 的定价方案，可创建的项目访问令牌数量存在上限。

<Image border={false} src="https://files.readme.io/b350ddb7403c7d0ffbaa7d4f8e4c5fc6ca0d92308c4c81bde90b2c2b146a1ed3-image.png" />

6. 将访问令牌添加到 ReadMe，然后点击 webhook 图标以创建所需的 webhook，从而保持您的内容与 GitLab 同步。

***

## 更换仓库

如果您需要将 ReadMe 项目连接到其他仓库，必须先使用垃圾桶图标断开与原仓库的连接。

1. 在 ReadMe 中，通过垃圾桶图标断开项目连接。
2. 在 GitLab 中，创建一个新的空项目。
3. 返回 ReadMe，选择您希望同步的项目。

***

## 受保护分支

所有分支规则应允许（从 ReadMe 同步到 GitLab 的）用户进行推送操作。

<Image border={false} src="https://files.readme.io/5ab0dbdd08ca7f9fc31d8a6895ebb9a970819ea4f2c352c92307ab5886b14541-image.png" />

## 常见问题

<Accordion title="与 GitLab 同步时需要哪些权限？" icon="fa-question-circle">
  ReadMe 请求访问以下权限：

  * `read_api` 用于列出项目
  * `read_user` 和 `read_profile` 用于显示用户信息
  * `read_repository` 用于将 GitLab 中的内容同步到 ReadMe
  * `write_repository` 用于将 ReadMe 中的内容同步到 GitLab
</Accordion>

<br />