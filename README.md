# 黄镇 · Zhen Huang

同济大学工程智能研究院助理教授个人主页。

- 网站：https://yellowtownhz.github.io/
- 仓库：https://github.com/yellowtownhz/yellowtownhz.github.io
- 默认分支：`master`

## 项目结构

- `dist/index.html`：个人介绍、研究方向、论文、经历与招生内容。
- `dist/assets/style.css`：排版与移动端适配。
- `dist/assets/portrait.png`：个人照片。
- `.github/workflows/pages.yml`：GitHub Pages 自动发布。

纯静态 HTML/CSS，无需安装依赖或构建，实际发布目录为 `dist/`。

## 本地预览

```sh
python3 -m http.server 8000 --bind 127.0.0.1 --directory dist
```

访问 http://127.0.0.1:8000 。

## 更新与发布

直接在本项目目录修改、提交和推送，不再使用临时发布目录。

```sh
git pull --ff-only
# 修改页面后检查差异
git diff --check
git diff
git add dist/index.html
git commit -m "Update homepage"
git push origin master
```

推送后 GitHub Actions 自动发布；在仓库 Actions 页面确认部署结果。
终端连接超时时，可为单次 Git 命令设置自己的 HTTP_PROXY 和 HTTPS_PROXY。

本地打包文件、缓存和内容来源笔记由 `.gitignore` 排除。
