# GitHub Pages 部署指南

## 第一步：在 GitHub 创建仓库

1. 打开浏览器，访问 https://github.com/new
2. 填写仓库信息：
   - Repository name: `academic-homepage`
   - Description: `My Academic Homepage`
   - 选择 **Public**（必须是公开仓库才能使用免费的 GitHub Pages）
   - **不要勾选** "Add a README file"
3. 点击 **Create repository** 按钮

---

## 第二步：本地 Git 配置（首次使用需要）

打开命令行（在当前文件夹按住 Shift + 右键，选择"在此处打开命令窗口"或"在此处打开 PowerShell 窗口"），依次执行：

```bash
git config --global user.name "Stonezzh"
git config --global user.email "你的GitHub邮箱"
```

**注意：** 把 `你的GitHub邮箱` 替换为你注册 GitHub 时使用的邮箱地址。

---

## 第三步：初始化本地仓库并推送

在 `F:\Desktop\MySelf` 文件夹下打开命令行，依次执行以下命令：

### 3.1 初始化 Git 仓库
```bash
git init
```

### 3.2 添加所有文件
```bash
git add .
```

### 3.3 提交文件
```bash
git commit -m "Initial commit: Academic homepage"
```

### 3.4 关联远程仓库
```bash
git remote add origin https://github.com/Stonezzh/academic-homepage.git
```

### 3.5 推送到 GitHub
```bash
git push -u origin main
```

**如果推送失败，提示需要认证：**

方法A（推荐）：使用 Personal Access Token
1. 访问 https://github.com/settings/tokens
2. 点击 **Generate new token** → **Generate new token (classic)**
3. Note 填写：`academic-homepage`
4. 勾选 `repo` 权限
5. 点击 **Generate token**
6. **复制生成的 token**（只显示一次，务必保存）
7. 重新执行推送命令，用户名输入 `Stonezzh`，密码输入刚才复制的 token

方法B：使用 GitHub Desktop（图形界面工具）
1. 下载安装 GitHub Desktop: https://desktop.github.com/
2. 登录你的 GitHub 账号
3. 在软件中打开 `F:\Desktop\MySelf` 文件夹
4. 点击 Publish repository

---

## 第四步：开启 GitHub Pages

1. 访问 https://github.com/Stonezzh/academic-homepage
2. 点击仓库顶部的 **Settings**（设置）
3. 在左侧菜单找到 **Pages**
4. 在 **Source** 下拉菜单中选择 **main** 分支
5. 点击 **Save**
6. 等待 1-2 分钟，页面会显示：
   ```
   Your site is live at https://stonezzh.github.io/academic-homepage/
   ```

---

## 第五步：访问你的网站

打开浏览器访问：**https://stonezzh.github.io/academic-homepage/**

用手机浏览器访问同样的网址，即可看到移动端适配效果。

---

## 后续更新内容

每次修改 `index.html` 后，在命令行执行：

```bash
git add .
git commit -m "更新内容描述"
git push
```

等待 1-2 分钟后，网站会自动更新。

---

## 常见问题

**Q: 推送时提示 "failed to push some refs"**  
A: 执行 `git pull origin main --rebase` 后再推送

**Q: 网站显示 404**  
A: 检查 GitHub Pages 设置中分支是否选择正确，等待几分钟后刷新

**Q: 图片不显示**  
A: 确保 `images/mine.png` 文件也一起推送到了 GitHub

**Q: 如何分享给别人？**  
A: 直接把网址 `https://stonezzh.github.io/academic-homepage/` 发给对方即可

---

## 微信分享测试

1. 用手机微信扫码或直接在微信中打开网址
2. 点击右上角 "..." → 发送给朋友
3. 对方点击后会直接在微信内置浏览器中打开
