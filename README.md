# 部署到 Vercel

本项目为单文件静态网页（`ggd.html`）。已添加 `vercel.json` 和 `index.html`，确保在 Vercel 上默认域名可直接访问。

## 部署方式一：Vercel Dashboard（推荐）
- 将此项目推送到 Git 仓库（如 GitHub/GitLab/Bitbucket）。
- 访问 https://vercel.com/new ，选择你的仓库进行导入。
- 框架选择：`Other`（静态网站），构建命令留空，输出目录留空（默认根目录）。
- 导入后，Vercel 会自动部署。部署成功后，访问默认域名即可跳转到 `ggd.html`。

## 部署方式二：Vercel CLI
- 安装 CLI：`npm i -g vercel`
- 登录：`vercel login`
- 在项目根目录执行：`vercel`
- 首次部署按提示选择团队、项目名称，后续使用：`vercel --prod`

## 说明
- `vercel.json` 配置了 `rewrites`，将根路径 `/` 重写到 `/ggd.html`，并开启 `cleanUrls`。
- 额外提供了 `index.html`，通过 `meta refresh` 与 JS 双重跳转到 `ggd.html`，提高兼容性。
- 无需构建步骤，Vercel 直接作为静态站点托管即可。

## 目录结构
```
.
├─ ggd.html
├─ index.html
└─ vercel.json
```

## 访问
- 部署完成后，访问 Vercel 分配的域名，如 `https://your-project.vercel.app/`。
- 首页会自动跳转到 `ggd.html`，也可直接访问 `https://your-project.vercel.app/ggd.html`。
