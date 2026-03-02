# 写文章工作流（Hexo + Butterfly）

> 仓库：`ruiranyan.github.io`
> 目录：`/Users/bytedance/Documents/trae_projects/myopenclaw/openclaw_workspace/ruiranyan.github.io`

下面假设你已经在这个目录下：

```bash
cd /Users/bytedance/Documents/trae_projects/myopenclaw/openclaw_workspace/ruiranyan.github.io
```

---

## 1. 初始化（第一次或换电脑时）

```bash
npm install
```

只需要在新环境跑一次，安装 Hexo 和主题依赖。

---

## 2. 本地预览网站

```bash
npm run server
```

然后在浏览器打开：

```text
http://localhost:4000
```

写文章的时候可以一直开着，保存后刷新页面就能看到效果。

---

## 3. 新建一篇文章

Hexo 默认会在 `source/_posts` 下保存文章；目前你的 repo 里还没有 `_posts` 目录，第一次新建时会自动创建。

```bash
npx hexo new post "你的文章标题"
```

例子：

```bash
npx hexo new post "2026 的一些想法"
```

执行后会在 `source/_posts/` 里生成一个类似：

```text
source/_posts/2026-de-yi-xie-xiang-fa.md
```

文件头部会有类似的 Front-matter：

```yaml
---
title: 2026 的一些想法
date: 2026-03-02 19:20:00
tags:
  - life
categories:
  - notes
---

正文从这里开始写……
```

你可以在编辑器里调整：

- `tags`: 标签（可以多个）
- `categories`: 分类（可以嵌套）

---

## 4. 写作与预览

1. 用你喜欢的编辑器打开新生成的 `.md` 文件
2. 启动本地预览：
   ```bash
   npm run server
   ```
3. 在浏览器里刷新 `http://localhost:4000` 看到效果

写作时注意：

- 图片可以放在 `source` 目录下合适的位置，然后用相对路径引用
- Markdown 支持公式（项目依赖了 `markdown-it-katex`）

---

## 5. 构建静态文件

写完准备发布时：

```bash
npm run clean   # 可选，清理旧的构建
npm run build   # 实际命令是：hexo generate
```

生成结果会在 `public/` 目录下，这是最终会部署到 GitHub Pages 的静态网站内容。

---

## 6. 部署到 GitHub Pages

确保 `_config.yml` 里的 `deploy` 配置已经设置好了（一般是 `hexo-deployer-git` 推到 GitHub 仓库的某个分支）。

然后执行：

```bash
npm run deploy
```

这会：

1. 根据 `deploy` 配置，把 `public/` 内容推到 GitHub
2. 触发 GitHub Pages 更新你的网站

通常几十秒到几分钟后，就能在 `https://ruiranyan.github.io/` 上看到最新内容。

---

## 7. 常用命令速查

在项目根目录：

```bash
# 安装依赖（首次 / 依赖更新）
npm install

# 本地预览
npm run server

# 生成静态文件
npm run build

# 清理旧构建
npm run clean

# 部署到 GitHub Pages
npm run deploy

# 新建文章
npx hexo new post "文章标题"
```

---

如果以后你想用更短的命令（比如 `npm run dev`），可以在 `package.json` 里新增 script，然后把这里的说明同步更新。
