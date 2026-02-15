# 个人学术主页（Jekyll + al-folio）

本项目是基于 **Jekyll** 与 **al-folio** 主题构建的个人网站仓库，适用于学术主页、项目展示与论文展示。

---

## 1. 项目整体结构（按职责）

### 1.1 配置与构建

- `_config.yml`：全站核心配置（站点信息、导航、插件、主题开关、学术展示规则等）
- `Gemfile`：Jekyll/Ruby 插件依赖
- `package.json`：前端格式化工具依赖（Prettier + Liquid）
- `Dockerfile`、`docker-compose.yml`、`docker-compose-slim.yml`：容器化运行与调试
- `bin/`：构建/部署辅助脚本
- `.github/workflows/`：CI/CD（部署、检查、格式化、性能检测等）

### 1.2 模板与渲染层

- `_layouts/`：页面布局骨架（默认页、文章页、出版物页等）
- `_includes/`：可复用组件（头部、底部、新闻、项目卡片、脚本引入等）
- `_plugins/`：自定义 Jekyll 插件（如学术引用增强、缓存、外部内容等）

### 1.3 内容层（你最常编辑）

- `_pages/`：主要页面（About、Projects、Publications、CV、Contact 等）
- `_news/`：新闻条目
- `_projects/`：项目条目
- `_bibliography/papers.bib`：论文 BibTeX 数据源
- `_data/`：结构化数据（coauthors、venues、cv、repositories）

### 1.4 资源与交互

- `assets/css/`：样式入口与第三方样式
- `assets/js/`：前端交互逻辑（主题切换、搜索等）
- `assets/img/`、`assets/pdf/`、`assets/audio/`、`assets/video/`：静态资源
- `assets/json/`：JSON 数据（如 `resume.json`）
- `assets/jupyter/`、`assets/html/`：Notebook 与嵌入式 HTML 资源

### 1.5 生成产物与文档

- `_site/`：Jekyll 生成后的静态网站（构建产物，不建议直接手改）
- `CUSTOMIZE.md`、`INSTALL.md`、`FAQ.md`：使用与定制说明
- `lighthouse_results/`：性能测试报告

---

## 2. 控制网页“风格”的关键文件

按影响范围从大到小：

1. **全站风格开关与参数**
   - `_config.yml`

2. **全站样式入口与主题变量**
   - `assets/css/main.scss`
   - `_sass/_themes.scss`
   - `_sass/_variables.scss`
   - `_sass/_base.scss`
   - `_sass/_layout.scss`
   - `_sass/_cv.scss`
   - `_sass/_distill.scss`
   - `_sass/_tabs.scss`

3. **页面结构与组件（决定视觉骨架）**
   - `_layouts/default.liquid`
   - `_includes/head.liquid`
   - `_includes/header.liquid`
   - `_includes/footer.liquid`

4. **交互体验（动态表现）**
   - `assets/js/theme.js`
   - `assets/js/common.js`
   - `assets/js/search/` 下相关脚本

---

## 3. 控制网页“内容”的关键文件

1. **页面正文内容**
   - `_pages/about.md`
   - `_pages/projects.md`
   - `_pages/publications.md`
   - `_pages/cv.md`
   - 以及 `_pages/` 中其他页面

2. **列表型内容源**
   - `_news/`（新闻）
   - `_projects/`（项目）
   - `_bibliography/papers.bib`（论文）

3. **结构化数据**
   - `_data/coauthors.yml`
   - `_data/venues.yml`
   - `_data/repositories.yml`
   - `_data/cv.yml`

4. **附件与媒体**
   - `assets/img/`、`assets/pdf/`、`assets/video/`、`assets/audio/`

---

## 4. 常见修改场景（速查）

- 改首页自我介绍：`_pages/about.md`
- 改导航显示顺序：对应页面 front matter 的 `nav` / `nav_order`，以及 `_config.yml`
- 加一篇论文：`_bibliography/papers.bib`
- 给论文加 PDF/预览图：`assets/pdf/`、`assets/img/publication_preview/`，并在 bib 条目中填写字段
- 新增项目卡片：`_projects/*.md`
- 改主题色：`_sass/_themes.scss`
- 改整体字体/间距：`_sass/_base.scss`

---

## 5. 本地运行（Docker）

### 5.1 启动

```bash
docker compose pull
docker compose up
```

访问：<http://localhost:8080>

### 5.2 精简镜像（可选）

```bash
docker compose -f docker-compose-slim.yml up
```

### 5.3 需要重建时

```bash
docker compose up --build
```

强制重建：

```bash
docker compose up --build --force-recreate
```

### 5.4 排查问题

查看日志：

```bash
docker compose logs
```

进入容器：

```bash
docker compose exec -it jekyll /bin/bash
```

容器内可执行：

```bash
./bin/entry_point.sh
bundle install
./bin/entry_point.sh
```

---

## 6. 说明

- 本 README 已改为面向当前仓库的“结构与维护指南”。
- 若你后续新增页面/集合（collections），建议同步更新此 README 的“结构”和“速查”两节。
