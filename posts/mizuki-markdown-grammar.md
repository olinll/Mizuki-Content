---
title: Mizuki Markdown 语法说明
published: 2026-01-20
pinned: true
description: 对于Mizuki的文章语法进行一些记录，方便翻阅
tags: [Markdown]
category: '碎碎念'

draft: false
date: 2026-01-01
image: "https://pic1.acofork.com/ri/h/556.webp"
---

# Markdown常用语法

可以参考 Mizuki Next Theme里面写的，很详细：[Markdown基础 - Mizuki Next Theme](https://docs.mizuki.mysqil.com/press/Markdown/Markdown/)

或者使用：[菜鸟教程 - Markdown教程](https://www.runoob.com/markdown/md-tutorial.html)

# Mizuki 扩展语法

## GitHub仓库卡片（GitHub Repository Cards）

支持添加动态 GitHub 仓库卡片，页面加载时会通过 GitHub API 拉取仓库实时信息（如星标数、分支数等）。

### 使用示例

::github{repo="olinll/Mizuki"}

### 语法格式

```markdown
::github{repo="用户名/仓库名"}
```

- `repo` 参数：必填，格式为「GitHub 用户名/仓库名称」（如 `matsuzaka-yuki/Mizuki`）

## 提示框（Admonitions）

支持 5 种预设类型的提示框，用于突出显示不同重要程度的信息，适配多种使用场景。

### 支持类型及示例

| 类型         | 语法标识    | 效果示例 |
| ------------ | ----------- | -------- |
| 说明         | `note`      | ::       |
| 技巧         | `tip`       | ::       |
| 重要         | `important` | ::       |
| 警告         | `warning`   | ::       |
| 注意（谨慎） | `caution`   | ::       |

### 基础语法

```markdown
:::类型标识
提示框内容（支持换行）
:::
```

### 自定义标题

可修改提示框默认标题，语法如下：

```markdown
:::note[我的自定义标题]
这是一个带有自定义标题的说明提示框。
:::
```

:::note[我的自定义标题]
这是一个带有自定义标题的说明提示框。
:::

### GitHub 兼容语法

同时支持 GitHub 官方提示框语法（无缝适配 GitHub 文档风格）：

```markdown
> [!NOTE]
> GitHub 语法的说明提示框。
> 支持多行内容。

> [!TIP]
> GitHub 语法的技巧提示框。
```

效果

> [!NOTE]
> GitHub 语法的说明提示框。
> 支持多行内容。

> [!TIP]
> GitHub 语法的技巧提示框。

## 折叠剧透（Spoiler）

支持添加折叠式剧透内容，默认隐藏，hover 或点击时显示，内容支持 Markdown 格式。

### 使用示例

```markdown
这是普通文本，剧透内容：:spoiler[被隐藏的**剧透内容**（支持粗体等 Markdown 语法）]！
```

效果：这是普通文本，剧透内容：:spoiler[被隐藏的**剧透内容**（支持粗体等 Markdown 语法）]！

### 语法格式

```markdown
:spoiler[剧透内容（可包含 Markdown 语法）]
```

