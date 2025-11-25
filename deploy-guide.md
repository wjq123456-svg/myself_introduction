# 🌐 网站部署指南

## 📋 部署前准备

### 1. 确保文件完整
确保以下文件都在项目根目录：
```
d:\Code\program\test_vscode\
├── personal-profile.html   # 主页面
├── profile-styles.css      # 样式文件
├── profile-script.js       # 脚本文件
├── images/                 # 图片文件夹
│   ├── profile.jpg
│   ├── avatar.jpg
│   ├── work1.jpg
│   ├── work2.jpg
│   ├── life1.jpg
│   ├── life2.jpg
│   ├── travel1.jpg
│   └── travel2.jpg
└── deploy-guide.md         # 本文件
```

### 2. 测试本地运行
在浏览器中打开 `personal-profile.html`，确保所有功能正常。

---

## 🚀 部署方法

### 方法一：CloudStudio 部署（推荐新手）

**优点：**
- 完全免费
- 操作简单
- 自动生成链接
- 支持自定义域名

**步骤：**
1. 在 CloudStudio 中创建新工作空间
2. 上传所有文件到工作空间
3. 点击"部署"按钮
4. 获得访问链接

### 方法二：GitHub Pages（推荐开发者）

**优点：**
- 免费
- 支持版本控制
- 稳定可靠
- 支持自定义域名

**步骤：**
1. 创建 GitHub 账号
2. 创建新仓库（仓库名：`username.github.io`）
3. 上传文件到仓库
4. 启用 GitHub Pages
5. 访问 `https://username.github.io`

**详细步骤：**
```bash
# 1. 初始化 Git 仓库
git init
git add .
git commit -m "Initial commit"

# 2. 连接到 GitHub
git branch -M main
git remote add origin https://github.com/你的用户名/你的用户名.github.io.git
git push -u origin main

# 3. 在 GitHub 仓库设置中启用 Pages
# Settings -> Pages -> Source: Deploy from a branch -> main
```

### 方法三：Netlify（推荐专业用户）

**优点：**
- 免费额度充足
- 自动部署
- 支持表单处理
- 全球 CDN

**步骤：**
1. 注册 Netlify 账号
2. 拖拽文件夹到部署区域
3. 获得随机域名
4. 可自定义域名

### 方法四：Vercel（推荐前端开发者）

**优点：**
- 专为前端优化
- 自动 HTTPS
- 全球 CDN
- 零配置部署

**步骤：**
1. 注册 Vercel 账号
2. 导入 GitHub 仓库或上传文件
3. 自动部署完成

### 方法五：传统虚拟主机

**优点：**
- 完全控制
- 支持后端语言
- 数据库支持

**步骤：**
1. 购买虚拟主机
2. 使用 FTP 上传文件
3. 绑定域名
4. 配置 DNS

---

## 🛠️ 部署优化建议

### 1. 文件优化
```bash
# 压缩 CSS
npx clean-css-cli -o profile-styles.min.css profile-styles.css

# 压缩 JS
npx terser profile-script.js -o profile-script.min.js

# 压缩图片（使用工具）
# 推荐使用：TinyPNG、ImageOptim
```

### 2. 添加 SEO 优化
在 `<head>` 中添加：
```html
<meta name="description" content="张三的个人简介 - 全栈开发工程师">
<meta name="keywords" content="个人简介,全栈开发,Web开发,张三">
<meta name="author" content="张三">

<!-- Open Graph 标签 -->
<meta property="og:title" content="张三的个人简介">
<meta property="og:description" content="全栈开发工程师的个人简介网站">
<meta property="og:image" content="https://你的域名/images/profile.jpg">
<meta property="og:url" content="https://你的域名">

<!-- Favicon -->
<link rel="icon" href="images/favicon.ico" type="image/x-icon">
```

### 3. 添加网站地图
创建 `sitemap.xml`：
```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
    <url>
        <loc>https://你的域名/</loc>
        <lastmod>2024-01-01</lastmod>
        <priority>1.0</priority>
    </url>
</urlset>
```

---

## 📊 部署后检查清单

### ✅ 基本检查
- [ ] 网站可以正常访问
- [ ] 所有页面链接正常
- [ ] 图片显示正常
- [ ] 移动端适配正常
- [ ] 表单功能正常

### ✅ 性能检查
- [ ] 页面加载速度（建议 < 3秒）
- [ ] 图片优化完成
- [ ] CSS/JS 文件压缩
- [ ] 启用 Gzip 压缩

### ✅ SEO 检查
- [ ] 标题标签设置
- [ ] Meta 描述设置
- [ ] 图片 Alt 属性
- [ ] 语义化 HTML 标签

---

## 🔧 常见问题解决

### Q1: 图片不显示？
**A:** 检查文件路径和大小写，确保图片文件确实存在。

### Q2: 样式丢失？
**A:** 检查 CSS 文件路径，确保相对路径正确。

### Q3: JavaScript 不工作？
**A:** 检查浏览器控制台错误信息，确保 JS 文件路径正确。

### Q4: 移动端显示异常？
**A:** 检查 viewport 设置和媒体查询。

---

## 📈 推广建议

### 1. 搜索引擎提交
- Google Search Console
- Bing Webmaster Tools
- 百度站长平台

### 2. 社交媒体分享
- LinkedIn 个人资料
- 微信朋友圈
- 微博分享

### 3. 名片和简历
- 在名片上添加网站链接
- 在简历中包含网站地址

---

## 🎯 下一步

1. **选择部署平台**（推荐 GitHub Pages 或 Netlify）
2. **完成部署**
3. **测试所有功能**
4. **分享给朋友**
5. **定期更新内容**

需要帮助选择部署平台或遇到问题，随时询问！