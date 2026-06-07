---
title: 'Git 工作流最佳实践'
description: '介绍日常开发中常用的 Git 工作流，帮助你更高效地进行版本控制。'
pubDate: '2025-06-03'
heroImage: '../../assets/blog-placeholder-2.jpg'
---

一个好的 Git 工作流能提升团队协作效率，减少合并冲突。

## 分支策略

推荐使用以下分支模型：

- `main` — 生产就绪代码
- `develop` — 集成分支
- `feature/*` — 功能开发
- `fix/*` — Bug 修复
- `release/*` — 发布准备

## 提交信息规范

使用约定式提交（Conventional Commits）格式：

```
<type>(<scope>): <description>

[optional body]
```

常用类型：

| 类型 | 说明 |
|------|------|
| `feat` | 新功能 |
| `fix` | Bug 修复 |
| `docs` | 文档更新 |
| `refactor` | 代码重构 |
| `style` | 代码格式 |

## 合并策略

优先使用 `rebase` 保持提交历史的整洁：

```bash
git checkout feature/my-feature
git rebase develop
```

对于已完成的功能分支，使用 `squash merge` 保持主分支整洁。

> 良好的提交记录是最好的代码文档。
