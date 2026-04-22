# SJTU BCI Lab Static Site

## 项目结构

- `main.html`：主页面文件（GitHub Pages 默认入口）
- `team_members.csv`：成员信息数据表
- `*.jpg`：页面引用的本地图片资源
- `.nojekyll`：禁用 Jekyll 处理，避免静态资源路径被干扰

## 本地维护建议

1. 更新成员信息时，优先修改 `team_members.csv`。
2. 图片文件名保持与页面/CSV引用一致。
3. 每次修改后直接打开 `main.html` 做快速检查。

## 发布到 GitHub Pages（推荐）

### 1. 新建仓库

在 GitHub 新建一个仓库（例如：`bci-lab-site`）。

### 2. 上传文件

把当前目录下这些文件全部上传到仓库根目录：

- `main.html`
- `team_members.csv`
- 所有 `*.jpg`
- `.nojekyll`
- `README.md`

### 3. 开启 Pages

仓库页面进入：

`Settings` -> `Pages`

设置：

- Source: `Deploy from a branch`
- Branch: `main`
- Folder: `/ (root)`

保存后等待 1-3 分钟，GitHub 会生成一个网址：

`https://<你的用户名>.github.io/<仓库名>/`

### 4. 验证上线

检查以下内容：

- 首页可正常加载
- 图库图片可打开
- 成员区能显示数据
- 中英切换和明暗模式可用

## 可选：命令行一次性推送

如果你本地已经安装了 Git：

```powershell
git init
git add .
git commit -m "Initial static site deployment"
git branch -M main
git remote add origin https://github.com/<你的用户名>/<仓库名>.git
git push -u origin main
```

## 常见问题

1. 页面空白：确认 `main.html` 在仓库根目录。
2. 图片不显示：确认文件名（含中文和空格）与引用完全一致。
3. 访问 404：确认 GitHub Pages 已开启并等待几分钟生效。
