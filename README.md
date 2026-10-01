# Panda Blog 🐼

基于 [Hugo](https://gohugo.io/) 的纯静态博客，托管于 GitHub Pages。

**在线地址**：https://pandaq1.github.io/pandablog/

## 如何写文章

在 `content/posts/` 下新建 Markdown 文件即可，例如 `content/posts/my-first-post.md`：

```markdown
+++
title = '我的文章标题'
date = 2026-10-02T12:00:00+08:00
tags = ['随笔']
draft = false
+++

正文内容，支持所有 Markdown 语法。
```

写完提交并推送到 GitHub：

```bash
git add .
git commit -m "新增文章：我的文章标题"
git push
```

推送后 GitHub Actions 会自动构建并发布，约 1 分钟后刷新网页即可看到新文章。

## 发布说说

编辑 `data/shuoshuo.toml`，在文件顶部添加一条即可：

```toml
[[shuoshuo]]
date = 2026-10-02T18:00:00+08:00
content = "今天想说的话……"
```

## 添加友情链接

编辑 `data/friends.toml`：

```toml
[[friends]]
name = "站点名"
url  = "https://example.com"
desc = "一句话介绍"
```

## 本地预览（可选）

```bash
hugo server
```

浏览器打开 http://localhost:1313/pandablog/ 实时预览。

## 目录结构

```
├── assets/css/main.css    # 全站样式
├── content/
│   ├── posts/             # 👈 文章放这里
│   ├── about.md           # 关于页
│   ├── archives.md        # 归档页
│   ├── shuoshuo.md        # 说说页
│   ├── guestbook.md       # 留言板
│   ├── friends.md         # 友情链接
│   └── search.md          # 搜索页
├── data/
│   ├── shuoshuo.toml      # 👈 说说内容
│   └── friends.toml       # 👈 友情链接
├── static/images/         # 背景图 bg.png、头像 avatar.png
├── layouts/               # 页面模板
└── .github/workflows/     # 自动部署配置
```

## 开启评论（可选）

本站预留了 [giscus](https://giscus.app) 评论支持（评论数据存在 GitHub Discussions 中）：

1. 确保本仓库已开启 Discussions（仓库 Settings → General → Features）
2. 打开 https://giscus.app ，填入仓库信息生成参数
3. 取消 `hugo.toml` 中 `[params.giscus]` 段的注释，填入你的 `repoId` 和 `categoryId`

## 首次部署注意

推送后需在仓库 **Settings → Pages** 中，将 Source 设置为 **GitHub Actions**（仅需一次）。
