# 🚀 网页修改和发布备忘录

## 📋 快速发布流程（推荐）

每次修改网页后，只需要执行以下3个命令：

```bash
# 1. 添加所有更改
git add .

# 2. 提交更改（记得写有意义的提交信息）
git commit -m "你的更改描述"

# 3. 推送到GitHub（会自动触发部署）
git push origin main
```

**完成！** GitHub Actions会自动构建并部署你的网站，通常2-3分钟后就能看到更新。

---

## 🔧 详细操作步骤

### 1. 修改网页内容
- 编辑 `docs/` 目录下的 `.md` 文件
- 修改 `mkdocs.yml` 配置文件
- 添加图片到 `docs/assets/` 目录

### 2. 本地预览（可选）
```bash
# 启动本地服务器预览
mkdocs serve

# 在浏览器中访问 http://127.0.0.1:8000
```

### 3. 发布到GitHub Pages
```bash
# 检查更改状态
git status

# 添加更改
git add .

# 提交更改
git commit -m "更新描述：具体做了什么修改"

# 推送到GitHub
git push origin main
```

### 4. 检查部署状态
- 去GitHub仓库的 **Actions** 标签页
- 查看 "Deploy to GitHub Pages" 工作流是否成功
- 等待2-3分钟，访问你的网站：`https://lixicheng01.github.io/Xicheng-Li/`

---

## 📝 常见修改场景

### 修改首页内容
```bash
# 编辑首页
vim docs/index.md

# 发布
git add docs/index.md
git commit -m "更新首页内容"
git push origin main
```

### 添加新页面
```bash
# 1. 创建新文件
touch docs/research/new-paper.md

# 2. 编辑内容
vim docs/research/new-paper.md

# 3. 更新导航配置
vim mkdocs.yml  # 在nav部分添加新页面

# 4. 发布
git add .
git commit -m "添加新研究论文页面"
git push origin main
```

### 修改网站配置
```bash
# 编辑配置文件
vim mkdocs.yml

# 发布
git add mkdocs.yml
git commit -m "更新网站主题配置"
git push origin main
```

### 添加图片
```bash
# 1. 复制图片到assets目录
cp your-image.png docs/assets/

# 2. 在markdown中引用
# ![图片描述](assets/your-image.png)

# 3. 发布
git add docs/assets/your-image.png
git commit -m "添加新图片"
git push origin main
```

---

## ⚠️ 注意事项

1. **提交信息要清晰**：用中文或英文描述你做了什么修改
2. **检查Actions状态**：推送后去Actions标签页确认部署成功
3. **等待部署完成**：通常需要2-3分钟才能看到更新
4. **浏览器缓存**：如果看不到更新，试试强制刷新（Ctrl+Shift+R）

---

## 🆘 故障排除

### 如果Actions失败
1. 去 **Actions** 标签页查看错误信息
2. 检查 `mkdocs.yml` 语法是否正确
3. 确认所有引用的文件都存在

### 如果网站没有更新
1. 等待3-5分钟
2. 强制刷新浏览器（Ctrl+Shift+R）
3. 检查GitHub Pages设置是否正确

### 如果需要回滚
```bash
# 查看提交历史
git log --oneline

# 回滚到指定版本
git reset --hard <commit-id>
git push origin main --force
```

---

## 🛠️ 快速命令参考

```bash
# 查看状态
git status

# 查看更改
git diff

# 查看提交历史
git log --oneline

# 本地预览
mkdocs serve

# 构建网站
mkdocs build
```

---

## 📚 有用的链接

- **网站地址**：https://lixicheng01.github.io/Xicheng-Li/
- **GitHub仓库**：https://github.com/LiXicheng01/Xicheng-Li
- **MkDocs文档**：https://www.mkdocs.org/
- **Material主题**：https://squidfunk.github.io/mkdocs-material/

---

**记住：每次修改后只需要 `git add .` → `git commit -m "描述"` → `git push origin main` 三步即可！** 🎉 