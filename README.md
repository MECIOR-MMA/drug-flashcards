# 药物结构背诵应用

基于**艾宾浩斯遗忘曲线 (SM-2算法)** 的药物化合物结构闪卡背诵应用。

## 功能

- 📖 **学习 + 复习** — 看结构猜药名 / 看药名想结构，SM-2 间隔重复
- 📊 **学习分析** — 分类掌握度、14天学习量图表、薄弱环节定位
- 💡 **背诵技巧** — 联想记忆、骨架识别、SAR联想、对比记忆
- 🔍 **快速浏览** — 网格展示 + 分类筛选 + 搜索
- ⚙️ **药品管理** — 编辑、新增、删除、上传自定义图片
- 💾 **数据备份** — JSON 导出/导入，多端手动同步
- 🌙 **深色模式** — 护眼暗色主题
- 📱 **PWA** — 可添加到手机主屏幕，离线使用

---

## 🚀 部署到 GitHub Pages（iPhone 使用）

### 第一步：安装 Git

1. 去 https://git-scm.com/download/win 下载 Git for Windows
2. 安装时一路默认选项即可
3. 安装完成后，在项目文件夹右键 → "Git Bash Here"

### 第二步：创建 GitHub 仓库

1. 打开 https://github.com 注册/登录账号
2. 点击右上角 **+** → **New repository**
3. Repository name 填写：`drug-flashcards`（或任意名字）
4. 选择 **Public**（公开）
5. **不要**勾选 "Add a README file"
6. 点击 **Create repository**

### 第三步：推送代码

在项目文件夹中打开 Git Bash（或终端），逐行执行：

```bash
# 初始化 git
git init

# 添加所有文件
git add .

# 提交
git commit -m "药物结构背诵应用 v1.0"

# 关联远程仓库（替换成你的用户名和仓库名）
git remote add origin https://github.com/你的用户名/drug-flashcards.git

# 推送
git branch -M main
git push -u origin main
```

### 第四步：开启 GitHub Pages

1. 刷新你的 GitHub 仓库页面
2. 点击 **Settings** → 左侧 **Pages**
3. **Branch** 选择 `main`，点击 **Save**
4. 等待 1-2 分钟，页面会显示：
   > Your site is published at `https://你的用户名.github.io/drug-flashcards/`

### 第五步：在 iPhone 上使用

1. 用 Safari 打开 `https://你的用户名.github.io/drug-flashcards/`
2. 点击底部的 **分享按钮**（方框+箭头图标）
3. 向下滚动，点击 **添加到主屏幕**
4. 名称改为"药物背诵"，点击 **添加**
5. 桌面会出现 💊 图标，点击即可像 App 一样使用！

> 🔄 **更新数据**：在手机上学习后，回到电脑 → 手机导出 JSON → 发送到电脑 → 电脑导入。或者反过来。

---

## 💻 本地使用

### 桌面端
直接用浏览器打开 `index.html` 即可。

### 本地服务器（手机连电脑WiFi访问）
```bash
cd 项目目录
python -m http.server 8080
# 浏览器打开 http://localhost:8080
# 手机连同一WiFi访问 http://你电脑的IP:8080
```

## 📝 背诵流程

1. 在**仪表盘**点击"学习新卡片"或"开始复习"
2. 选择模式：**看图识名** 或 **看名识图**
3. 看到结构图（或药名）→ 心中默想 → 点击屏幕显示答案
4. 点击 **✗ 不认识** 或 **✓ 认识**
5. 系统自动安排下次复习时间

## 💡 学习分析

点击底部"学习"栏可以查看：
- 总体进度和分类掌握度
- 近14天学习量柱状图
- 错误最多的薄弱环节
- 药学背诵技巧（点击切换）

## 🔧 技术栈

- 纯原生 HTML/CSS/JS，零依赖
- IndexedDB 本地持久化
- SM-2 间隔重复算法
- PWA Service Worker 离线缓存
