# reimu-template

<img alt="主题版本" src="https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2FD-Sketon%2Freimu-template%2Frefs%2Fheads%2Fmain%2Fpackage.json&query=%24.dependencies.hexo-theme-reimu&label=主题版本">


[hexo-theme-reimu](https://github.com/D-Sketon/hexo-theme-reimu) 的模板

## 使用方法

```bash
git clone https://github.com/D-Sketon/reimu-template
cd reimu-template
npm install
hexo server
```

## 特性

已预支持以下特性：

- 支持 LaTeX (@reimujs/hexo-renderer-markdown-it-plus)
- 支持 mermaid (hexo-filter-mermaid-diagrams)
- 支持 git (hexo-deployer-git)
- 支持 rss (hexo-generator-feed)
- 支持 Algolia 搜索 (@reimujs/hexo-algoliasearch)

## 使用说明

Hexo 的配置在 `_config.yml` 中  
Reimu 的配置在 `_config.reimu.yml` 中  
您可以根据需要修改配置