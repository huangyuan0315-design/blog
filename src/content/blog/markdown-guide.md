---
title: 'Markdown 写作完全指南'
description: '掌握 Markdown 基础语法，高效写作博客内容。包含文字、图片、代码等常用格式。'
pubDate: '2025-06-07'
heroImage: '../../assets/blog-placeholder-4.jpg'
---

Markdown 是一种轻量级标记语言，非常适合博客写作。

## 基本格式

**粗体**、*斜体*、~~删除线~~、`行内代码`

## 图片支持

在 Markdown 中插入图片非常简单：

```markdown
![图片描述](/images/photo.jpg)
```

> Astro 的 Content Collections 会自动优化 `src/assets/` 中的图片，生成不同尺寸的响应式版本。

## 列表

### 无序列表

- 项目一
- 项目二
- 项目三

### 有序列表

1. 第一步
2. 第二步
3. 第三步

## 引用

> 写作是最好的思考方式。
> — 佚名

## 代码块

```python
def greet(name: str) -> str:
    return f"Hello, {name}!"

print(greet("World"))
```

## 分隔线

---

以上就是 Markdown 的常用语法。掌握这些就能写出漂亮的博客文章了。
