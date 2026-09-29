# Blog 发布规范

每篇文章使用一个独立文件夹：

```text
YYYY-MM-DD-product-subject/
├── index.md
├── cover.jpg        # 可选
└── article-image.png
```

## 文件夹命名

- 日期使用 `YYYY-MM-DD`。
- 产品只能使用：`docusign`、`okta`、`sentinelone`、`jamf`、`yubikey`、`abnormal`、`company`。
- Subject 使用小写英文，单词之间使用 `-`。
- 正文文件固定命名为 `index.md`。
- 图片与文章放在同一个文件夹中；封面统一使用 `cover.jpg` 或 `cover.png`。

## 文章头部字段

```yaml
---
title: "文章标题"
date: "2026-09-29"
product: "docusign"
subject: "api-integration"
category: "集成实践"
summary: "用于列表和搜索引擎的文章摘要。"
cover: "./cover.jpg"
author: "FreeLink 技术团队"
status: "draft"
featured: false
---
```

`status` 允许三个值：

- `draft`：草稿，不在官网展示。
- `review`：待审核，不在官网展示。
- `published`：正式发布。

发布前，将 `status` 改为 `published`。网站构建程序只读取正式发布的文章，并按 `date` 从新到旧排序。

