# CLAUDE.md

本文件为Claude Code (claude.ai/code) 在此代码库中工作时提供指导。

## 项目概述

这是一个使用Reimu主题的Hexo博客。Hexo是一个基于Node.js的快速、简洁且强大的博客框架。

## 常用命令

### 开发
- `npm install` - 安装依赖
- `hexo server` 或 `npm run server` - 启动本地开发服务器
- `hexo generate` 或 `npm run build` - 生成静态文件
- `hexo clean` 或 `npm run clean` - 清理缓存文件和生成的静态文件

### 部署
- `hexo deploy` 或 `npm run deploy` - 部署到GitHub Pages
- `hexo generate && hexo deploy` - 生成并部署到GitHub Pages

### 创建内容
- `hexo new "文章标题"` - 创建新文章
- `hexo new page "页面标题"` - 创建新页面

## 项目结构

- `_config.yml` - 主要的Hexo配置文件
- `_config.reimu.yml` - Reimu主题配置文件
- `source/` - 源内容目录
  - `source/_posts/` - Markdown格式的博客文章
  - `source/about/` - 关于页面
  - `source/friend/` - 友链页面
- `themes/reimu/` - Reimu主题文件
- `public/` - 生成的静态文件（请勿手动编辑）
- `scaffolds/` - 新文章/页面的模板文件

## 高层架构

1. **内容管理**: 博客文章以Markdown格式编写并存储在`source/_posts/`目录中。每篇文章都可以包含front-matter元数据。

2. **主题系统**: Reimu主题控制表现层。主题配置在`_config.reimu.yml`文件中。

3. **静态生成**: Hexo处理Markdown文件和主题模板，在`public/`目录中生成静态HTML文件。

4. **部署**: 静态文件通过git部署器部署到GitHub Pages。

5. **插件**: 各种插件提供额外功能，如：
   - 数学公式渲染 (KaTeX/MathJax)
   - Mermaid图表
   - RSS订阅生成
   - Algolia搜索
   - 评论系统 (Waline)
   - 代码高亮

## 关键配置文件

1. `_config.yml` - 站点配置（标题、URL、部署设置）
2. `_config.reimu.yml` - 主题特定配置（菜单、社交链接、小工具、动画）
3. `themes/reimu/_config.yml` - 默认主题配置（备用设置）

## 内容创建

文章应以Markdown文件形式创建在`source/_posts/`目录中。每篇文章应包含front-matter元数据，如标题、日期、标签和分类。

front-matter示例：
```
---
title: 文章标题
date: 2023-01-01 12:00:00
tags:
  - 标签1
  - 标签2
categories:
  - 分类1
---
```