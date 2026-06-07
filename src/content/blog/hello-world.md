---
title: '欢迎来到我的博客'
description: '第一篇博客文章，聊聊搭建这个博客的初衷和计划。'
pubDate: '2025-06-01'
updatedDate: '2025-06-07'
heroImage: '../../assets/blog-placeholder-1.jpg'
---

## 关于这个博客

这是一篇示例博客文章，用来演示 Astro 博客模板的功能。这个博客会用来记录以下内容：

- **技术学习笔记**：编程、框架、工具链等
- **读书笔记**：阅读过程中的思考和摘录
- **生活记录**：旅行、日常、摄影

## 为什么选择 Astro？

Astro 是一个现代的静态站点生成器，具有以下优点：

1. 默认输出纯静态 HTML，性能极佳
2. 支持 Markdown 和 MDX 写作
3. 内置图片优化
4. 可以按需引入交互组件

## 代码示例

以下是一段 TypeScript 代码示例：

```typescript
interface Post {
  title: string;
  description: string;
  pubDate: Date;
  heroImage?: string;
}

async function getPosts(): Promise<Post[]> {
  const posts = await getCollection('blog');
  return posts.sort((a, b) => 
    b.data.pubDate.valueOf() - a.data.pubDate.valueOf()
  );
}
```

## 展望

接下来会陆续更新内容，希望这个博客能坚持写下去。
