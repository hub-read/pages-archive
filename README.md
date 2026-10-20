# hubgork.github.io

由 GitHub Actions 部署（`.github/workflows/pages.yml`）。

用法：新建一个顶层子文件夹，放入 `index.html`，push 到 main 即可。根目录 `index.html` 由 `scripts/build-index.py` 在构建时自动生成（不提交到仓库），按最近提交时间倒序列出所有含 `index.html` 的子文件夹。

- 标题取自页面的 `<title>`；可选 `meta.json`：`{"title": "...", "description": "..."}` 覆盖。
- 只放非机密内容；大型项目用独立仓库；很小的文件可放 Release 资产。
- 推送约 1 分钟后生效；浏览器缓存 max-age=600，可用 `?v=` 绕过。
