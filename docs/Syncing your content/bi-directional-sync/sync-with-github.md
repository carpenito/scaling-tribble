---
title: 与 GitHub 同步
deprecated: false
hidden: false
metadata:
  robots: index
---
## 如何设置与 GitHub 的双向同步

### 前提条件

* 您需要一个 GitHub 账户。
* 在同步到组织内的仓库时，您需要有权限创建一个**空仓库**。

### 设置步骤

1. 导航至 **Settings** > **Git Connection** 页面。
2. 选择 GitHub。
3. 如果尚未创建，请在 [GitHub](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository) 中创建一个空仓库——请确保取消勾选创建 README 的选项。
4. 与您的提供商进行 **Sync** 并完成身份验证。授予对您希望同步的仓库的访问权限，并在下一个页面确认您的仓库。

***

## 更换仓库

1. 在 ReadMe 中，通过垃圾桶图标断开项目连接。
2. 在 GitHub 中，创建新仓库（必须为空仓库）。
3. 导航至 **Applications > Installed GitHub Apps**。
4. 找到 **ReadMe Sync** 并点击 **Configure**。
5. 在 _Repository access_ 下，选择您希望同步到的新仓库。
6. 返回 ReadMe 并连接到您的新仓库。

***

## 编辑您的文档

**[分支](https://docs.readme.com/main/docs/branches#/)**

* ReadMe 的初始提交是为了与 GitHub 建立分支同步
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

***

### GitHub Enterprise Server

如果您使用的是自托管的 **[GitHub Enterprise Server (GHES)](https://docs.readme.com/ent/docs/connecting-github-enterprise-server)**，您可以在群组仪表板的 **Git Connection** 下设置同步。同步需要一个全新的空仓库，且每个子项目只能同步到一个仓库。

<Image align="center" border={false} src="https://files.readme.io/bd2640dae70270e20b0a71ae98adf56bd4e3a59b275b1609e86bbc4fc8ad81cd-GHES.png" />

如果您的项目无法使用 GHES，请联系您的客户成功经理。

### GitHub 分支保护

如果您的 GitHub 仓库使用了分支保护规则，您需要对其进行配置，以允许 ReadMe Sync 应用推送更改。以下是根据您的 GitHub 配置进行设置的方法：

#### 适用于 GitHub Rulesets（新版本）

1. 导航至您仓库的分支保护设置。
2. 在 _Bypass list_ 部分，点击 **+ Add bypass**。
3. 搜索 _ReadMe Sync_（App • readmeio），并将权限设置为 **Always allow**。

<Image align="center" alt="Adding ReadMe Sync to the GitHub Rulesets bypass list for direct push access." border={false} caption="Adding ReadMe Sync to the GitHub Rulesets bypass list for direct push access." src="https://files.readme.io/0e52415eb4dede062a4d9df4a2d3f06dda62500c26caae7f000e4ecd50f4521d-Screenshot_2024-11-22_at_11.12.14_AM.png" width="600px" />

#### 适用于旧版分支保护

1. 前往您仓库的分支保护规则。
2. 找到 _Allow specified actors to bypass required pull requests_ 部分。
3. 将 _readme-sync_（ReadMe Sync）添加到允许的操作者列表中。

<Image align="center" alt="Configuring ReadMe Sync in legacy branch protection settings to bypass pull request requirements." border={false} caption="Configuring ReadMe Sync in legacy branch protection settings to bypass pull request requirements." src="https://files.readme.io/8f3765d6ebbe96f5a93e4c6f915e52392ad6ba1512d0af4d4113ca8ff6ef8077-Screenshot_2024-11-22_at_11.12.07_AM.png" />

此配置可确保在 ReadMe 编辑器中所做的更改能够同步到您 GitHub 仓库中受保护的分支。

***

<br />

## 常见问题

<Accordion title="ReadMe 如何与 GitHub 集成，需要哪些权限？" icon="fa-question-circle">
  ReadMe 使用具有仓库级别访问权限的 GitHub App：元数据为只读（必需），内容同步为读/写。Webhook 负责处理同步、变更检测和冲突解决。
</Accordion>

<Accordion title="Why don't my branches show on GitHub?" icon="fa-question-circle">
  启用双向同步后新创建的分支会自动在 GitHub 上创建对应的分支，但已有分支在 ReadMe 端保存任何更改（无论多小）之前，不会在 GitHub 上创建对应的分支。
</Accordion>