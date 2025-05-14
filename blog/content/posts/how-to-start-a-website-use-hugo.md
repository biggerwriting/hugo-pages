+++
date = '2025-05-13T12:38:11+08:00'
draft = false
title = 'How to Start a Website Use Hugo'
tags = ['hugo']
+++

## 建站步骤
### 环境准备
安装好 go, hugo, git, node, npm

### 运行命令

```bash
# 初始化项目
hugo new site quickstart
cd quickstart

# 下载主题, 不限于以下方式，只要themes/ananke 目录存在即可
git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke

# 配置主题
echo "theme = 'ananke'" >> hugo.toml

# 启动服务, 支持看草稿
hugo server -D

# 添加文件内容
hugo new content content/posts/my-first-post.md

```

### 拓展
- 页面支持标签配置
- 文章目录分级



> 参考网站：https://gohugo.io/getting-started/quick-start/

