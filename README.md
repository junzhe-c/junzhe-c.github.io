# Junzhe Chen — Academic Homepage

面向 GitHub Pages 的纯静态学术主页，不依赖 Node.js、构建工具、后端或外部 CDN。原有 `CNAME`（`junzhec.top`）保持不变。

仓库：<https://github.com/junzhe-c/junzhe-c.github.io>。个人资料：<https://github.com/junzhe-c>。

## 本地预览

在本目录运行：

```sh
python3 -m http.server 4173 --bind 127.0.0.1
```

然后打开 <http://127.0.0.1:4173>。修改文件后刷新浏览器即可。

## 文件说明

- `index.html`：个人介绍、导师、新闻、两篇研究图文摘要、教育与经历。完整静态 HTML，不依赖 JavaScript。
- `publications.html`：完整论文列表，包含每篇的简短介绍、原始论文图、资源链接和独立锚点。
- `assets/styles.css`：桌面、平板、手机和打印样式。
- `assets/citations/*.bib`：各篇论文的 BibTeX；`assets/publications.bib` 为完整合集。
- `assets/papers/`：三篇论文的原始图、首页缩略图和显示副本，完整图片可单独打开。
- `assets/icons/`：本地 Lucide SVG 图标及授权文件。
- `assets/fonts/`：保留旧版字体与授权文件；当前使用系统字体。
- `docs/content-sources.md`：核对来源、日期和仍需本人确认的履历信息。

2026-10-15 的样式参考 <https://simolark.com/>：白底、侧栏个人信息和简单章节标题。按用户后续要求补充少量青绿色线条图标，并将论文展示扩展到独立页面。首页保留两篇图文摘要；手机自动改为单栏。论文配图采用真实论文原图，不使用示意封面代替实验内容。

## 更新论文

在 `publications.html` 对应的 `.publication-section` 中新增 `article.publication-detail`，填写标题、完整作者、年份、发表状态、简短介绍和真实链接。需要首页展示时，在 `index.html` 的 `.research-previews` 中补充摘要。图片引用使用相对路径，保留有意义的 alt 文本，并在 `docs/content-sources.md` 记录来源。预印本与正式发表的论文分开列出，自己的论文署名用 `strong` 标注；同步维护独立及合并的 BibTeX 文件。不要将预印本写成已录用论文。

## 发布到原 GitHub Pages

将本目录的修改提交、推送并合并到原仓库配置的发布分支即可；保留根目录 `index.html`、`CNAME`、`.nojekyll` 与 `assets/`。当前没有添加 GitHub Actions，也没有修改远程 Pages 设置。2026-08-31 已通过 GitHub API 确认当前发布源为 `main` 分支根目录 `/`（legacy build）。

主页面不收集访客数据、不加载第三方脚本或外部字体，也不展示原页面的个人电话号码。
