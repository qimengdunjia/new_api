<!--
  文件功能：说明 NewAPI 首页内容项目的用途与使用方式。
  用途：作为 GitHub 仓库首页文档，帮助快速复制并维护首页片段。
-->

# NewAPI 首页 Codex 使用教学

这个项目用于维护 NewAPI 首页中的 Codex 使用教学内容。

## 文件说明

- `home_page/newapi_home_page_content.html`：可直接复制到 NewAPI 首页内容配置中的 HTML 片段。
- `AGENTS.md`：后续维护约束，记录 NewAPI Markdown/HTML 混合渲染的注意事项。

## 使用方式

1. 打开 `home_page/newapi_home_page_content.html`。
2. 复制文件全部内容。
3. 粘贴到 NewAPI 后台的首页内容配置中。
4. 保存后访问首页检查渲染效果。

## 注意事项

- 不要把完整 HTML 文档粘贴到 NewAPI 首页。
- 示例 API Key 必须保持占位符，不要提交真实密钥。
- `config.toml` 展示区已经适配 NewAPI 的 Markdown 解析器，不要轻易改回普通 `<pre><code>`。
