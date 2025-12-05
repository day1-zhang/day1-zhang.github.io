# 个人博客（GitHub Pages + Jekyll）

本项目是一个最小可用的 Jekyll 博客，用于部署到 `your-username.github.io`。

## 快速开始
- 将 `_config.yml` 中的 `title`、`author`、`github_username`、`url` 替换为你的信息。
- 在 GitHub 创建仓库：`your-username.github.io`。
- 将本目录全部文件推送到该仓库的 `main` 分支。
- 启用 GitHub Pages：默认从 `main` 分支根目录构建，稍等片刻即可访问。

## 写作指南
- 新文章放在 `_posts` 目录，文件名格式：`YYYY-MM-DD-标题.md`。
- 文章头部示例：

```
---
layout: post
title: 标题
date: 2025-01-01 10:00:00 +0800
categories: [分类]
tags: [标签1,标签2]
---
```

- 首页自动展示文章列表；`about.md` 可编辑为你的个人简介。

## 本地预览（可选）
- 如果需要本地预览，安装 Ruby 与 Bundler，然后在仓库根目录执行：

```
bundle install
bundle exec jekyll serve
```

- 访问 `http://localhost:4000` 查看效果。

## 常用自定义
- 更换主题：在 `_config.yml` 中调整 `theme`（默认为 `minima`）。
- 添加导航与页脚：参考主题文档，在 `_includes` 与 `_layouts` 中扩展。
- 订阅源：已启用 `jekyll-feed` 插件，可为读者提供 RSS。

## 目录结构
- `_config.yml`：站点配置
- `index.md`：首页，展示文章列表
- `about.md`：关于页面
- `_posts/`：文章目录
- `.gitignore`：忽略构建产物

## 常见问题
- 无法访问页面：确认仓库名为 `your-username.github.io`，并且 Pages 已成功构建。
- 文章未显示：确认文件名与头部信息格式正确，时间不在未来。