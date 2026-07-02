---
title: 双向同步
deprecated: false
hidden: false
metadata:
  robots: index
---
双向同步在您的 ReadMe 项目与 GitHub 或 GitLab 仓库之间建立双向连接。这一可选工作流可保持两个平台上的内容一致：

* 在您偏好的环境中编写内容，无论是 ReadMe 还是本地开发环境。
* 开发人员、工程师和技术写作者可以使用各自偏好的工具进行协作。
* 更改会在 ReadMe 和 Git 之间自动同步，形成单一可信来源。

<PlanTable currentPlan="Startup" />

***

## 设置双向同步

ReadMe 支持与 <Anchor label="GitHub" target="_blank" href="https://docs.readme.com/main/docs/sync-with-github">GitHub</Anchor> 和 <Anchor label="GitLab" target="_blank" href="https://docs.readme.com/main/docs/sync-with-gitlab">GitLab</Anchor> 进行双向同步。

如需与 GitHub 同步，您可以连接到 GitHub Cloud。如果您使用的是 Enterprise 计划，ReadMe 支持与 <Anchor label="GitHub Enterprise Server" target="_blank" href="https://docs.readme.com/ent/docs/connecting-github-enterprise-server">GitHub Enterprise Server</Anchor> 进行双向同步。

<Image align="center" border={true} src="https://files.readme.io/6335bcb6aa344d9d1f23d11b3cf420cbe94493872630760fb04d2cce9df10189-Screenshot_2025-10-27_at_12.29.28_PM.png" className="border" />

<Callout icon="❗️" theme="error">
  您要同步的仓库在连接到 ReadMe 之前必须为空——不含任何提交或文件（例如 README.md）。设置完成后，您可以添加或删除文件。
</Callout>

***

## 文档版本管理

如果您的 ReadMe 项目使用了多个[版本](doc:versions)，首次启用双向同步时，只有主版本会被同步。成功启用双向同步后，其他版本的任何更改都将同步到您的 Git 仓库。

***

## 编辑文档

设置好 Git 连接后，在 ReadMe 编辑器中所做的所有更改都会自动同步到您的 Git 仓库，反之亦然。在 Git 中编辑文档时，您可以使用偏好的代码编辑器或 Git 工具。

为确保从 _Git 到 ReadMe_ 的同步成功，请遵循以下结构规范：

**Markdown 文件：**

* 文件必须包含必要的 frontmatter：`title` 和 `summary`
* 内容应以标准 Markdown 格式编写
* 文件名必须与预期的 URL slug 匹配，以确保正确路由

**导航：**

* 页面顺序通过 `_order.yaml` 文件定义
* 每个分类文件夹可以有其自己的 `order.yaml`
* Git 中的[导航结构](https://docs.readme.com/main/docs/documentation-structure#/)与您的 ReadMe 项目层级结构相对应

**[分支](https://docs.readme.com/main/docs/branches#/)**

* ReadMe 的初始提交用于建立与 GitHub 的分支同步
* 分支名称必须与 ReadMe 中定义的版本名称完全匹配
* 任何不匹配的版本和名称将存在于 GitHub 中，但不会与 ReadMe 同步。

<HTMLBlock>{`
<div class="migrating-column">
  <section>
    <header>
      <i class="fa-duotone fa-solid fa-hexagon-exclamation"></i> 未同步
    </header>
    <pre>ReadMe: v2.0_new-branch
GitHub: v2-new-branch
		</pre>
  </section>
  <section>
    <header>
      <i class="fa-duotone fa-solid fa-circle-check"></i> 已同步
    </header>
    <pre>ReadMe: v2.0_new-branch
GitHub: v2.0_new-branch
		</pre>
  </section>
</div>
`}</HTMLBlock>

<HTMLBlock>{`
<!-- style guide CSS -->
<style>
  .migrating-column {
    border: 1px solid var(--color-border-default);
    border-radius: var(--border-radius);
    display: flex;
    justify-content: center;
    
    + .migrating-column {
      margin-top: 1em;
    }
    
    section {
      flex: 1 1 50%;
      overflow: hidden;
      
      + section {
        border-left: 1px solid var(--color-border-default);
      }
    }
    
    pre {
      background: transparent;
      border: 0;
      border-radius: 0;
      font-size: 0.8em;
      margin: 0;
      overflow: auto;
      padding: 15px;
      
      + pre {
        border-top: 1px solid var(--color-border-default);
      }
    }
    
    header {
      align-items: center;
      border-bottom: 1px solid var(--color-border-default);
      display: flex;
      font-size: 15px;
      font-weight: var(--font-weight-bold);
      gap: 0.5em;
      padding: 1em;
    }

    .fa-circle-check {
      color: var(--green);
    }

    .fa-hexagon-exclamation {
      color: var(--red);
    }
  }
</style>
`}</HTMLBlock>

### 处理冲突

在 ReadMe 中保存时检测到冲突，系统将立即提示您选择覆盖 Git 更改或取消保存并继续编辑。在 ReadMe 中保存的更改将始终与线上内容保持一致。

从 GitHub 合并时，用户可以通过 GitHub 编辑器或在本地使用自己偏好的合并工具解决冲突后再推送。

***

## 常见问题

<Accordion title="ReadMe 如何与 GitHub 集成，需要哪些权限？" icon="fa-question-circle">
  ReadMe 使用具有仓库级别访问权限的 GitHub App：元数据为只读（必需），内容同步为读/写权限。Webhook 负责处理同步、变更检测和冲突解决。
</Accordion>

<Accordion title="Why aren't my branches showing up in GitHub or GitLab?" icon="fa-question-circle">
  启用双向同步后新建的分支会自动在 Git 工具中创建对应分支，但已有分支在您于 ReadMe 中保存该分支的更改之前，不会在 Git 工具中创建对应分支。
</Accordion>

<Accordion title="与 GitLab 同步时需要哪些权限？" icon="fa-question-circle">
  ReadMe 请求访问以下权限：

  * `read_api` 用于列出项目
  * `read_user` 和 `read_profile` 用于显示用户信息
  * `read_repository` 用于将 GitLab 中的内容同步到 ReadMe
  * `write_repository` 用于将 ReadMe 中的内容同步到 GitLab
</Accordion>