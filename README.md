# tyangjn.github.io

田阳（Yang Tian）的个人学术主页，纯静态 HTML，无需构建工具。

## 目录结构

```
github_page/
├── index.html        # 主页（全部内容和样式都在这一个文件里）
├── images/           # 照片和论文配图
└── .nojekyll         # 告诉 GitHub Pages 不要用 Jekyll 处理
```

## 部署步骤

1. 在 GitHub 上创建一个新的**公开**仓库，名字必须是 `TyangJN.github.io`（用户名 + `.github.io`）。
2. 在本目录执行：

   ```bash
   cd "/Users/yangtian/Desktop/田阳工作/个人材料/github_page"
   git init
   git add .
   git commit -m "Initial homepage"
   git branch -M main
   git remote add origin git@github.com:TyangJN/TyangJN.github.io.git
   git push -u origin main
   ```

3. 打开仓库 Settings → Pages，确认 Source 为 `Deploy from a branch`，分支 `main`、目录 `/ (root)`。
4. 一两分钟后访问 <https://tyangjn.github.io/>。

## 日常维护

- 改内容：直接编辑 `index.html`（新增论文就复制一个 `<article class="pub">…</article>` 块改内容）。
- 换图：把新图放进 `images/`（建议压缩到 200KB 以内），改 `index.html` 里对应的 `src`。
- 提交更新：`git add . && git commit -m "update" && git push`，推送后页面自动更新。
