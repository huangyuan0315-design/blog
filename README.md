# Huang Yuan Blog

基于 [Astro](https://astro.build) 构建的个人博客，托管于 [Cloudflare Pages](https://pages.cloudflare.com)。

## 本地开发

```bash
# 安装依赖
npm install

# 启动开发服务器
npm run dev

# 构建生产版本
npm run build
```

## 部署到 Cloudflare Pages

### 1. 将代码推送到 GitHub

```bash
git add .
git commit -m "Initialize blog"
git push origin main
```

### 2. 在 Cloudflare Pages 中连接仓库

1. 登录 [Cloudflare Dashboard](https://dash.cloudflare.com)
2. 进入 **Workers & Pages** → **Pages**
3. 点击 **连接到 Git**
4. 选择 GitHub 中的 `blog` 仓库
5. 配置构建设置：

| 设置项 | 值 |
|--------|-----|
| 生产分支 | `main` |
| 构建命令 | `npm run build` |
| 构建输出目录 | `dist` |
| Node.js 版本 | `22.x` |

6. 点击 **保存并部署**

首次部署完成后，Cloudflare 会分配一个 `*.pages.dev` 域名。后续每次推送到 `main` 分支都会自动触发部署。

### 3. 更新站点 URL

部署完成后，将 `astro.config.mjs` 中的 `site` 字段更新为实际的 Cloudflare Pages 域名：

```js
site: 'https://your-blog.pages.dev',
```

## 写作指南

### 创建新文章

在 `src/content/blog/` 目录下创建 `.md` 或 `.mdx` 文件：

```markdown
---
title: '文章标题'
description: '文章摘要描述'
pubDate: '2025-06-07'
heroImage: '../../assets/blog-placeholder-1.jpg'
---

文章内容...
```

### 添加图片

将图片放入 `src/assets/` 目录，在文章 frontmatter 中通过 `heroImage` 引用。Astro 会自动优化图片（生成 WebP、调整尺寸）。

文章内部的图片可以放在 `public/images/` 目录，通过 Markdown 语法引用：

```markdown
![图片描述](/images/photo.jpg)
```

## 技术栈

- **框架**: Astro 6.x
- **内容**: Markdown + MDX
- **部署**: Cloudflare Pages
- **图片优化**: Sharp (内置)
- **RSS**: @astrojs/rss
- **站点地图**: @astrojs/sitemap
