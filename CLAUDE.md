# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 项目概述

这是一个小米商城首页的静态页面练习项目，纯 HTML + CSS 实现，无 JavaScript、无构建工具、无包管理器。

## 项目结构

项目按"天"递进式构建，每个目录是当天的完整成果，从 `03/` 到 `07滑动门效果/`。根目录的 `index.html` + `css/` + `images/` 是早期阶段（第1-2天）。**最新最完整的版本在 `07滑动门效果/`**。

每个目录自包含 `css/`、`images/` 和 `index.html`。CSS 文件结构统一为：
- `reset.css` — 基础样式重置
- `iconfont/iconfont.css` — 图标字体（购物车、箭头、放大镜图标）
- `mi.css` — 主样式文件

## 如何运行

这是纯静态页面，无需构建。直接在浏览器中打开任意目录的 `index.html` 即可查看效果。

```
# Windows 下快速预览
start 07滑动门效果/index.html
```

## 各阶段内容

| 目录 | 内容 |
|------|------|
| 根目录 (`index.html`) | 顶部广告区域居中 + 黑色导航栏 |
| `04/` | （第4天） |
| `05白色导航滑动门/` | 白色主导航栏 + 下拉菜单（滑动门效果） |
| `06新建Banner/` | Banner 区域 + 左侧分类侧边栏 |
| `07滑动门效果/` | 侧边栏二级弹出菜单（滑动门效果） |

## 关键 CSS 模式

- **布局方式**: 基于 `float` 的传统布局（非 Flexbox/Grid）
- **内容区**: `.warp { width: 1226px; margin: 0 auto; }` 居中固定宽度
- **下拉菜单**: 通过 `:hover` 触发 `display: none/block` + `height` 过渡动画实现
- **CSS 三角形**: 用 border 技巧绘制下拉菜单小箭头（`.stri`）
- **小米品牌色**: `#ff6700`（橙色），用于 hover 高亮和 logo 背景
- **黑色导航**: 背景 `#333`，文字 `#b0b0b0`，高度 40px
- **白色导航**: 高度 100px，logo 区域 55×55px

## Git 分支

- `demo` — 当前开发分支
- `master` — 主分支
