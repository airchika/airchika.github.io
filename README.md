# Air Chika

Astro 静态个人站。首版定位是柔和二次元气质的个人博客，包含首页、关于页、文章列表、文章详情、标签入口、站点运行天数和 GitHub Pages 部署工作流。

## 本地开发

```sh
npm install
npm run dev
```

## 构建

```sh
npm run build
npm run preview
```

## 写文章

文章放在 `content/blog`。每篇 Markdown 需要 frontmatter：

```md
---
title: 文章标题
description: 简短描述
pubDate: 2026-06-22
tags: [随笔, 视觉小说]
draft: false
---
```

## GitHub Pages

这个项目按“用户站”配置，不设置 `base`。仓库名应为 `<你的 GitHub 用户名>.github.io`。

部署前建议在仓库 `Settings > Secrets and variables > Actions > Variables` 里添加：

```txt
SITE_URL=https://<你的 GitHub 用户名>.github.io
```

然后到 `Settings > Pages` 把 Source 设为 `GitHub Actions`。推送到 `main` 后，`.github/workflows/deploy.yml` 会自动构建并发布。

如果使用自定义域名，把 `SITE_URL` 设置为自定义域，并同步修改 `public/robots.txt` 里的 sitemap 地址。
