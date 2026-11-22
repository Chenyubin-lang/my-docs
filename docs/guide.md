# 使用指南

## 文档更新流程

1. 修改 docs 目录下的 Markdown 文件。
2. 在本地预览文档网站。
3. 使用 Git 提交修改。
4. 推送代码到 GitHub。
5. GitHub Actions 自动构建并部署网站。

## 常用命令

启动本地预览：

    python -m mkdocs serve

构建静态网站：

    python -m mkdocs build --strict

## 自动部署原理

当代码推送到 main 分支时，GitHub Actions 会执行自动构建任务，并通过 GitHub Pages 发布网站。