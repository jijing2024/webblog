---
title: "GitHub Blog 发布流程测试"
date: "2026-09-29"
product: "docusign"
subject: "publishing-test"
category: "集成实践"
summary: "验证文章从 GitHub 内容目录读取、构建并展示到 FreeLink 官网的完整流程。"
author: "FreeLink 技术团队"
status: "published"
featured: true
---

这是一篇用于验证新 Blog 发布流程的测试文章。文章不再从官网后台直接发布，而是先提交到受权限保护的 GitHub 内容仓库。

## 一篇文章一个文件夹

文章正文固定使用 `index.md`，文章使用的图片也放在同一个文件夹中。这样移动、审核和归档时不会出现图片与正文分离的问题。

## 发布状态控制

- `draft` 表示仍在撰写。
- `review` 表示等待审核。
- `published` 表示允许官网构建和展示。

## 官网如何读取

构建程序读取 `content/blog` 目录，检查文件名和文章字段，只将状态为 `published` 的文章生成到网站中，并按照日期倒序排列。

> 这篇文章用于链路测试，确认成功后可以删除或改成正式内容。

