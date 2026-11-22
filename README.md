# MkDocs 文档自动部署实践

本项目是 Git 工具与软件开发课程的个人实践作业，使用 Markdown 和 MkDocs Material 编写四页技术文档，并通过 GitHub Actions 自动构建、发布到 GitHub Pages。

- GitHub 登录名：Chenyubin-lang
- [公开网站](https://chenyubin-lang.github.io/my-docs/)
- [个人实验报告](report/README.md)
- [部署工作流](.github/workflows/deploy.yml)

## 本地预览

需要 Python 3.12，在项目根目录执行：

```powershell
python -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
.\.venv\Scripts\python.exe -m mkdocs build --strict
.\.venv\Scripts\python.exe -m mkdocs serve
```

浏览器访问终端给出的地址，通常为 http://127.0.0.1:8000/；按 Ctrl+C 停止预览。直接使用虚拟环境中的 Python，无需修改 PowerShell 执行策略。

## 项目结构

- `docs/`：首页、关于、使用指南和 API 示例的 Markdown 源码。
- `mkdocs.yml`：主题、网站地址和导航配置。
- `.github/workflows/deploy.yml`：构建和发布工作流。
- `report/`：实验说明及实际过程截图。
- `site/`：自动生成的构建产物，已忽略，不提交到 main。

## 自动发布

指定文档或配置文件推送到 main 后，工作流构建并上传 site/ 产物，再部署到 Pages。仅修改 README 或实验报告不会触发部署。
