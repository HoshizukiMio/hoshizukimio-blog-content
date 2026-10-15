# 星月澪の幻想笔记 · 内容仓库

网站：https://blog.hoshizukimio.com/

主题代码独立存放在 `HoshizukiMio/hoshizukimio-blog`。本仓库只管理内容，旧文章没有迁入。

| 目录 | 内容 |
| --- | --- |
| `posts/` | Markdown / MDX 文章 |
| `spec/` | 关于、友链等页面正文 |
| `data/` | 日记、友链、项目等结构化内容 |
| `images/` | 头像、背景和文章图片，以 `/images/…` 引用 |

新建 `posts/hello.md` 即可发布文章：

```markdown
---
title: 我的第一篇文章
published: 2026-10-15
description: 文章摘要
tags: [日常]
category: 随笔
draft: false
---

在这里写正文。
```

推送到 `main` 后，GitHub Actions 会调用 Vercel Deploy Hook，自动重新构建主题仓库并同步最新内容。Hook 地址作为 `VERCEL_DEPLOY_HOOK` 仓库 Secret 保存，不写进源码。

本地预览时编辑主题目录中的 `content/` 独立仓库，再在主题根目录运行 `pnpm dev`。同步脚本会保留未提交的本地内容修改；提交并推送内容仓库即可发布。
