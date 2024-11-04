# blog-ncuscc

这是我们俱乐部的官网博客。

## 简介

使用 Hexo 框架与 Butterfly 主题搭建，目前通过 GitHub Actions 自动构建，并部署在 GitHub Pages 上。未来计划将网站迁移到腾讯云服务器，并使用腾讯云的自定义域名（当前使用 GitHub 分配的域名）。

Hexo 框架的核心功能是将 Markdown 文档转化为静态 HTML、CSS 和 JS 文件，适合用于生成静态网站。Butterfly 主题则是我们选择的一款美化主题，用于提升网站的视觉效果。

## 贡献

### 1. Fork 仓库并克隆到本地

首先，将此仓库**fork**到您的 GitHub 账户。这一步让您可以在自己的账号下进行修改，而不影响原始项目。接着，将 fork 后的仓库**克隆**到本地，方便在本地环境中进行开发和测试。

```bash
git clone <your_forked_repo_url>
```

### 2. 安装依赖

进入本地仓库的根目录，运行以下命令安装项目所需的依赖包：

```bash
npm install
```

这一步确保您有所有项目运行所需的库和工具，保证开发环境的完整性。

### 3. 下载主题

在完成依赖安装后，运行以下命令下载 Hexo 主题到指定目录：

```bash
git clone -b master https://github.com/jerryc127/hexo-theme-butterfly.git themes/butterfly
```

建议您也可以尝试使用 SSH 方式下载，这样可以简化后续的权限管理：

```bash
git clone -b master git@github.com:jerryc127/hexo-theme-butterfly.git themes/butterfly
```

### 4. 本地开发与修改

在完成下载和安装后，您可以使用以下命令清理缓存、生成静态文件并启动本地服务器，以便预览您的更改：

```bash
hexo clean && hexo generate && hexo server
```

您还可以使用以下命令新建文章：

```bash
hexo new post "你的文章标题"
```

### 5. 测试和预览

本地服务器启动后，您可以在浏览器中访问生成的网站，查看您的修改效果。这一步很重要，以确保所有内容正常显示，没有错误。

### 6. 提交修改并创建 PR

测试无误后，将修改推送到您 fork 的仓库中：

```bash
git push origin master
```

然后在 GitHub 上访问您的仓库，创建一个**Pull Request (PR)**，以便提交审核。审核通过后，您的修改将合并到主仓库中。

## 常见问题

您可能会在安装依赖时遇见部分依赖版本过老和网络连接失败等报错，此时可以进行如下尝试(进行操作前请先确认关闭网络加速器或VPN服务)：

1.强制删除原来的不完整依赖模块

```bash
rm -rf node_modules
```

2.强制安装所需依赖

```bash
npm install --force
```

3.检查hexo安装情况

```bash
hexo -v
```

