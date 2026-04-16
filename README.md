# 个人博客（Hexo）

当前生效站点目录：`myBlog`

## 一次性准备
1. 安装 Node.js（建议 18+）。
2. 在仓库根目录安装依赖：`cmd /c npm install`
3. 在博客目录安装依赖：`cmd /c "cd myBlog && npm install"`

## 写文章
在仓库根目录执行：

```bash
cmd /c "cd myBlog && npm run new -- \"文章标题\""
```

文章会生成在：`myBlog/source/_posts/文章标题.md`

## 本地预览
在仓库根目录执行：

```bash
cmd /c "cd myBlog && npm run preview"
```

预览地址：`http://localhost:4000`

## 上传发布
在仓库根目录执行：

```bash
cmd /c "cd myBlog && npm run publish"
```

`publish` 会自动执行：`hexo clean` + `hexo generate` + `hexo deploy`

## 常见问题
- 如果 PowerShell 报错 `npm.ps1` 被禁止运行，继续使用 `cmd /c npm ...` 即可。
- 首次发布失败时，检查 GitHub 仓库推送权限（SSH Key 或登录状态）。
- 当前发布配置在 `myBlog/_config.yml`，目标仓库为 `straw66/straw66.github.io`，分支为 `main`。
