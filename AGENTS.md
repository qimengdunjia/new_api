<!--
  文件功能：记录 new_api 工作区的协作与实现约束。
  用途：指导后续代理维护 NewAPI 首页内容片段，避免重复踩 Markdown/HTML 渲染问题。
-->

# new_api 工作区说明

## NewAPI 首页内容

- 当前首页内容维护文件是 `home_page/newapi_home_page_content.html`。
- NewAPI 首页内容会先经过 Markdown 解析，再通过 HTML 注入页面。
- 不要把完整 HTML 文档粘进 NewAPI 首页，例如 `<!doctype html>`、`<html>`、`<head>`、`<body>` 都不要使用。
- 首页内容应使用可嵌入片段：一个外层容器、局部 CSS、正文 HTML。
- CSS 必须限定在 `.codex-guide` 或相关 `cg-` 类名下，避免污染 NewAPI 自身样式。

## 代码块与配置展示

- NewAPI 的 Markdown 解析器会把代码块里的 `# 中文注释` 误解析成标题。
- 展示 `~/.codex/config.toml` 时，不要使用普通 `<pre><code>` 承载带 `#` 的多行配置。
- 对 `config.toml` 推荐使用 `.cg-code-box` 加逐行 `<span>` 的方式展示。
- 注释符号 `#` 应写成 `&#35;`，避免被 Markdown 当成标题语法。
- `.cg-code-box` 容器不要使用 `white-space: pre`，否则 HTML 结构换行会变成多余空白行。
- 若需要保留单行文本格式，只在 `.cg-code-box span` 上使用 `white-space: pre`。

## 线上检查流程

- 每次改完 `home_page/newapi_home_page_content.html` 后，先停下让用户复制到 NewAPI。
- 未收到用户明确说明“已复制 / 请访问页面”前，不要主动访问线上站点。
- 用户确认复制后，再访问 `https://new-api-latest-xhh3.onrender.com` 检查最终渲染效果。
