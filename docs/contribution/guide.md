# 贡献指引

## 参与协作

!!! note "提示"

    > 不要害怕编辑，勇于更新页面！
    
    —— [维基百科](https://zh.wikipedia.org/wiki/Wikipedia:%E6%96%B0%E6%89%8B%E5%85%A5%E9%96%80/%E7%B7%A8%E8%BC%AF)

### 找到你想要编辑的页面

在开始贡献之前，你需要先知道你需要编辑什么。

- 如果你在一个页面上发现了错误或希望进行改进，则你已经知道了你需要编辑的页面：

    !!! note "提示"
        请在开始贡献之前打开一个新的 [Issue](https://github.com/OpenCubikFoundation/theopensourceway-guidebook-zh/issues/new) 让维护者/其他贡献者知道你在做的事情，避免重复工作。

- 否则，前往 [TODO-List](https://github.com/OpenCubikFoundation/theopensourceway-guidebook-zh/issues/1) 查看需要进行翻译的内容。如果你想要向其中的某个页面贡献，请在该页面的 Issue 下方留言并 `@` 我 (`@Cubik65536`) 告知你想要贡献的页面。我会开启另外一个 issue 并将其分配给你，对该页面的内容的工作将在新 issue 内跟踪。

前往 [GitHub 仓库](https://github.com/OpenCubikFoundation/theopensourceway-guidebook-zh) 中的 `docs` 目录，你将可以看到所有页面的 Markdown 源文件，根据路径找到你想要编辑的文件。

### 编辑页面

#### 在 GitHub 上编辑

参与本仓库中的翻译工作 **需要** 一个 GitHub 账号（可以前往 [GitHub 的账号注册页面](https://github.com/signup) 页面注册），但 **不需要** 高超的 GitHub 技巧，即使你是一名新手，只要按照下面所述的步骤操作，也能够 **非常出色** 地完成编辑。

???+ tip "提示"
    在你的更改被合并到 `theopensourceway-guidebook-zh` 的主仓库之前，你对 `theopensourceway-guidebook-zh` 的内容所作出的修改均不会出现在网站或 pdf 上，所以无需担心你的修改会破坏网站上正在显示的内容。
    如果还是不放心，可以查看 [GitHub 的官方教程](https://skills.github.com/)。

1. 打开 [GitHub 仓库](https://github.com/OpenCubikFoundation/theopensourceway-guidebook-zh) 仓库，点击键盘上的 <kbd>.</kbd> 按钮（或者将 URL 中的 `github.com` 更改为 `github.dev`）[^ref1]，进入 GitHub 的网页版 VS Code 编辑器；
2. 在编辑器中作出对页面源文件的更改，可以使用页面右上方的预览按钮（或按下 <kbd>Ctrl+K</kbd> <kbd>V</kbd> 快捷键）在右侧打开预览界面；
3. 修改完成后使用左侧的 Source Control 选项卡，并按照本文中 [commit 信息格式规范](#commit-信息格式规范) 填写 commit 信息并提交，提交时会提示是否创建此仓库的分支，点击绿色的 **Fork Repository** 按钮即可。
4. 提交后会在网页上方的中央弹出一个提示框，在第一次的提示框内填写标题，第二次的提示框内填写此提交要提交到的仓库内分支名称，之后右下角会弹出一个提示框，内容类似于 `Created Pull Request #1 for OpenCubikFoundation/theopensourceway-guidebook-zh.`，点击蓝字链接即可查看该 Pull Request。

##### 向 Pull Request 追加更改

1. 打开 [Pull Request 列表](https://github.com/OpenCubikFoundation/theopensourceway-guidebook-zh/pulls)，找到您提交的 Pull Request 并点击。
2. Pull Request 页面的标题下方将会有一段例如 `<您的ID> wants to merge x commits into OpenCubikFoundation:main from <您的ID>:patch-1` 的文字，点击 `<您的ID>:patch-1` 部分。
3. 您应该会被重定向到您的分支仓库中，而且文件列表左上角的分支名称是你提交 Pull Request 的分支名称（在本示例中应为 `patch-1`）。
4. 进行您需要的更改。
    - 如果您需要编辑单个文件或多个互相无关联的页面的内容，请直接找到你要的文件并进行更改，更改完成后滚动到页面下方，按照本文中 [commit 信息格式规范](#commit-信息格式规范) 填写 commit 信息，之后点击 **Commit changes** 按钮提交修改。
    - 如果您需要编辑多个文件，点击键盘上的 <kbd>.</kbd> 按钮（或者将 URL 中的 `github.com` 更改为 `github.dev`）[^ref1]，进入 GitHub 的网页版 VS Code 编辑器并作出更改。然后使用左侧的 Source Control 选项卡，并按照本文中 [commit 信息格式规范](#commit-信息格式规范) 填写 commit 信息并提交修改。
5. 这时你的更改会被自动追加在您的 Pull Request 中。

#### 使用 Git 在本地进行编辑

虽然大多数情况下您可以直接在 GitHub 上进行编辑，但对于一些较为特殊的情况（如需要使用 GPG 签名），我们更推荐使用 Git 在本地进行编辑。

大致流程如下：

1. 将主仓库 Fork 到自己的仓库中；
2. 将 Fork 后的分支仓库克隆（clone）到本地；
3. 在本地新建一个分支（branch）并切换到这个分支；
4. 在本地进行修改后提交（commit）这些更改；
5. 将这些更改推送（push）到你克隆的分支仓库；
6. 提交 Pull Request 至主仓库。

##### 在本地预览编辑效果

在本地进行编辑时，您可以使用 `mkdocs serve` 命令在本地运行预览服务器。

##### 向 Pull Request 追加更改

在 clone 下来的本地分支仓库中继续进行修改，并提交（commit）以及推送（push）这些更改即可。你的更改会被自动追加在 Pull Request 中。

## 贡献规范

不遵循此处的内容可能会导致您的 Pull Request 被直接关闭。

!!! warning "注意"
    您可能会因为多次提交低质量/不符合要求的内容被封禁。

### 格式规范

请遵循本站的 [格式规范](/docs/contribution/format-guide.md)。

### 分支规范

我们 **非常** 建议您在增加与提交新内容时使用新的分支！分支命名可以是 `patch-1`、`patch-2` 等等，也可以使用描述具体更改内容性质的名称，例如 `translate-xxx`、`fix-xxx` 等等。

### Commit 信息格式规范

对于提交时需要填写的 commit 信息，请遵守以下几点基本要求：

1. commit 摘要请简要描述这一次 commit 改动的内容。注意 commit 摘要的长度不要超过 50 字符，超出的部分会自动置于正文中。
2. 如果需要进一步描述本次 commit 内容，请在正文中详细说明。

对于 commit 摘要，推荐按照如下格式书写：

``` text
<修改类型>(<文件名>): <修改的内容>
```

修改类型分为如下几类：

- `feat`：用于添加内容的情况。
- `fix`：用于修正现有内容错误的情况。
- `refactor`：用于对一个页面进行重构（较大规模的更改）的情况。
- `revert`：用于回退之前更改的情况。

#### Pull Request 信息格式规范

对于 Pull Request，请遵守以下几点要求：

1. 标题请写明本次 PR 的目的（做了 **什么** 工作，修复了 **什么** 问题）。
2. 内容请简要叙述修改的内容。如果修复了一个 issue 的问题，请在结尾增加 `(#xxxx)` 字段，其中 `xxxx` 代表 issue 的编号。

对于 Pull Request 的标题，推荐使用如下格式书写：

``` text
<修改类型>(<文件名>): <修改的内容> (<对应 issue 的编号>)
```

修改类型分为如下几类：

- `feat`：用于添加内容的情况。
- `fix`：用于修正现有内容错误的情况。
- `refactor`：用于对一个页面进行重构（较大规模的更改）的情况。
- `revert`：用于回退之前更改的情况。

## 协作流程

1. 在收到一个新的 Pull Request 之后，GitHub 会给 reviewer 发送邮件；
2. reviewer 可能会发现问题，并提出 `review` 或 `suggested changes`（建议更改，显示为灰色图标）/`requested changes`（强制更改，显示为红色图标，只会在 reviewer 拥有 repo 写权限时出现）。一般来说，reviewer 也会附上建议和需要进行的更改，在这时，您将会需要继续向 Pull Request 追加其他更改。更改的方法可以参考 `在 GitHub 上编辑` 或者 `使用 Git 在本地进行编辑` 部分的 `向 Pull Request 追加更改` 部分。
3. 在 reviewer 批准一个 PR 之后，这个 PR 才可以合并到 `main` 分支中；
4. 在合并到 `main` 分支之后，GitHub Actions 会构建一遍网页内容，并更新到 gh-pages 分支；
5. 这时服务器才会拉取 gh-pages 分支的更新，并重新部署最新版本的内容。
6. 在提交高质量的 PR 之后，您将会被邀请成为仓库的协作者，多次提交高质量的 PR 之后，您将会被邀请成为 GitHub 组织的成员。

## 参考资料与注释

[如何参与 - OI-Wiki](https://oi.wiki/intro/htc/)

[^ref1]: [Web-based editor - GitHub Codespaces - GitHub Docs](https://docs.github.com/en/codespaces/developing-in-codespaces/web-based-editor)
