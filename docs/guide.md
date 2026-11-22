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

当 docs/、mkdocs.yml、requirements.txt 或部署工作流的修改推送到 main 分支时，GitHub Actions 会自动构建并发布网站。只修改报告或根目录 README 不触发部署；也可以在 Actions 页面手动运行工作流。