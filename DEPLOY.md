# 部署到 GitHub Pages 指南

由于您的系统未安装 GitHub CLI (gh)，请按照以下步骤手动创建 GitHub 仓库并部署：

## 步骤 1: 创建 GitHub 仓库

1. 访问 https://github.com/new
2. 仓库名称输入: `portfolio`
3. 选择 **Public**（公开）
4. 不要初始化 README、.gitignore 或 license
5. 点击 **Create repository**

## 步骤 2: 推送代码到 GitHub

在终端运行以下命令：

```bash
cd /Users/yesimin/Documents/portfolio
git branch -M main
git remote add origin https://github.com/你的用户名/portfolio.git
git push -u origin main
```

*注意：将 `你的用户名` 替换为你的 GitHub 用户名*

## 步骤 3: 启用 GitHub Pages

1. 访问你创建的 GitHub 仓库: https://github.com/你的用户名/portfolio
2. 点击 **Settings** 标签
3. 在左侧菜单中找到 **Pages**
4. 在 **Build and deployment** 部分:
   - Source: 选择 **Deploy from a branch**
   - Branch: 选择 **main** / **root** (默认)
5. 点击 **Save**

## 步骤 4: 等待部署

等待 1-2 分钟，GitHub 会自动构建你的网站。你会在 GitHub Pages 页面看到部署状态。

## 步骤 5: 访问你的网站

部署成功后，你的网站可以通过以下地址访问：

```
https://你的用户名.github.io/portfolio/
```

## 自定义域名（可选）

如果你想使用自己的域名：

1. 在 GitHub Pages 设置中点击 **Add domain**
2. 输入你的域名（如 `www.yourdomain.com`）
3. 按照提示配置 DNS 记录

## 更新网站

当你修改代码后，只需运行：

```bash
git add .
git commit -m "Update website"
git push
```

GitHub Pages 会自动重新部署。
