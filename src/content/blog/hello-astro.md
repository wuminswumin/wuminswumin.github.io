---
title: 用 Astro 搭建我的个人博客
description: 记录这个博客的搭建过程：为什么选 Astro、项目结构长什么样、以后怎么发文章。
pubDate: 2026-11-01
tags: [Astro, 博客, 折腾记录]
---

这是这个博客的第一篇文章。

## 为什么选 Astro

我想要一个自己的地方，用来放学习笔记和项目复盘。对比了几种方案后，我选了 Astro：

- 生成的是静态页面，打开速度快
- 写文章就是写 Markdown，不需要数据库
- 以后想加交互，可以直接嵌入 Vue 组件

## 项目结构

```text
my-blog/
├── src/
│   ├── content/blog/    # 文章放这里
│   ├── layouts/         # 页面骨架
│   ├── pages/           # 路由
│   └── styles/          # 全局样式
└── astro.config.mjs
```

## 怎么发新文章

在 `src/content/blog/` 里新建一个 `.md` 文件，写上标题、描述、日期，然后保存：

```md
---
title: 文章标题
description: 一句话摘要
pubDate: 2026-11-01
---

正文从这里开始。
```

开发服务器会自动刷新，刷新浏览器就能看到。

> 本站由 Astro 驱动，部署方式还没定，先在本地跑起来。
