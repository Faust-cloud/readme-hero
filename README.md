# 🦸 ReadmeHero

> 一键生成好看的 GitHub 项目封面图 —— 纯浏览器运行，零安装、零后端、不上传任何数据。
>
> _A tiny in-browser tool to generate beautiful banner images for your GitHub README. No install, no backend, 100% local._

![ReadmeHero banner](./banner.png)

<p align="center">
  <a href="#-功能特性">功能</a> ·
  <a href="#-在线使用">在线使用</a> ·
  <a href="#-本地运行">本地运行</a> ·
  <a href="#-部署到-github-pages">部署</a> ·
  <a href="#-技术栈">技术栈</a>
</p>

<p align="center">
  <img alt="License: MIT" src="https://img.shields.io/badge/License-MIT-ff5a36.svg" />
  <img alt="PRs Welcome" src="https://img.shields.io/badge/PRs-welcome-6366f1.svg" />
  <img alt="No build step" src="https://img.shields.io/badge/build-none%20needed-22c55e.svg" />
</p>

---

## 这是什么？

好的 GitHub 项目，README 顶部往往有一张漂亮的**横幅封面图**（项目名 + 一句话简介 + 配色），一眼就显得专业。但做这张图很烦——得开 Figma / PS 自己拼。

**ReadmeHero** 把这件事变成 30 秒的事：打开网页 → 填项目名和简介 → 选个风格和颜色 → 一键下载 PNG，直接放进你的 README。

整个工具就是**一个 HTML 文件**，在你浏览器里本地出图，不联网、不上传、不收费。

## ✨ 功能特性

- 🎨 **5 套精致模板**：极简白、科技深、活力渐变、极客终端、杂志感
- 🌈 **自由配色**：8 个预设主色 + 任意自定义颜色
- 😀 **Emoji 点缀**：预设常用 emoji，也可输入任意一个
- 👀 **实时预览**：改任何内容，右侧封面图立刻更新
- 📐 **标准尺寸**：输出 1280 × 640 px（GitHub 社交预览图官方尺寸），2 倍分辨率不糊
- 💾 **一键导出**：下载 PNG，或直接复制到剪贴板
- 🔒 **完全本地**：所有渲染在浏览器完成，不上传任何数据
- 🪶 **零依赖**：单个 HTML 文件，无需安装、无需构建

## 🚀 在线使用

👉 **https://faust-cloud.github.io/readme-hero/**

## 💻 本地运行

不需要安装任何东西，两种方式随便选：

**方式一（最简单）**：直接双击 `index.html`，用浏览器打开即可。

**方式二**：如果你本机装了 Python，可以起一个本地服务（可选）：

```bash
# 在项目目录下执行，然后浏览器打开 http://localhost:8000
python3 -m http.server 8000
```

## 🌐 部署到 GitHub Pages

想让别人也能在线用，免费挂到 GitHub Pages：

1. 把本项目上传到你的一个 GitHub 仓库（本仓库 `readme-hero`）。
2. 进入仓库的 **Settings → Pages**。
3. 在 **Source** 选择 `Deploy from a branch`，分支选 `main`、目录选 `/ (root)`，保存。
4. 等一两分钟，页面会给出 `https://faust-cloud.github.io/readme-hero/` 地址，打开就能用。

## 🧩 技术栈

- 原生 **HTML / CSS / JavaScript**，无框架、无构建步骤
- 使用浏览器原生 **Canvas API** 绘制与导出图片
- 使用 **Clipboard API** 实现「复制到剪贴板」
- 所有代码在单个 `index.html` 内，便于阅读、fork 和二次开发

## 🛠️ 想加新模板？

模板都定义在 `index.html` 里的 `TEMPLATES` 对象中。每个模板是一个 `draw(o)` 函数，`o` 里有 `name / subtitle / author / accent / emoji`。照着现有的模板复制一个、改改画法，就能加一套新风格。欢迎 PR！

## 🤝 贡献

欢迎提 Issue 和 PR——新模板、新配色、bug 修复都欢迎。保持「零依赖、单文件」的简单风格即可。

## 📄 License

[MIT](./LICENSE) © Faust-cloud
