# Agent 工作说明

本文件记录 agent 在本仓库中的协作要求、项目结构理解与日常维护入口。后续 agent 进入项目后，应先阅读本文件，再阅读 `README.md`、`_config.yml` 和当天 `project_archive/` 中的记录。

## 用户要求

- 进入或创建 Python、Arduino 或硬件编程项目时，如果项目根目录尚未被 git 跟踪，应先初始化 git。
- 安装 Python、Arduino 或硬件编程项目依赖时，应创建并使用独立 conda 环境，不安装到 base 环境。
- 对每个项目，所有通过网络下载的内容都必须记录到项目进度 Markdown 文件中，包含来源 URL、许可证或访问策略、本地保存路径。
- 本仓库根目录维护 `project_archive/` 文件夹。
- 每个发生 agent 改动的日期，在 `project_archive/` 下创建或更新一个 `YYYY-MM-DD.md` 文件，记录当日 agent 执行的改动、涉及文件、验证结果，以及网络下载内容。
- 每次推送到 GitHub 远程仓库后，在本文件的“推送记录”中追加一条记录，格式为 `YYYYMMDD 主要改动关键词总结`。

## 归档规范

- 文件命名：`project_archive/YYYY-MM-DD.md`。
- 同一天多次改动时，追加到同一个日期文件。
- 每次记录建议包含：
  - 日期与任务摘要
  - 修改文件
  - 改动说明
  - 验证方式与结果
  - 网络下载内容记录；如无下载，写明“本次无网络下载”
- 不要把归档写入 `_site/`，因为 `_site/` 是 Jekyll 构建产物。

## 项目概览

这是一个基于 Jekyll 与 al-folio 主题的个人学术主页仓库，用于展示 Ziqi Liu 刘子琦的个人简介、研究兴趣、项目、论文、CV、新闻与摄影画廊。

站点主要信息在 `_config.yml` 中：

- 站点地址：`https://ziqidennisliu.github.io`
- 站点身份：`Ziqi Liu 刘子琦`
- 主要技术栈：Jekyll、Liquid、Sass、Bootstrap、Ruby gems、少量前端 JavaScript
- 内容类型：学术主页、项目集、论文列表、个人 CV、新闻、图片画廊

## 主要目录

- `_config.yml`：全站核心配置，包含站点身份、导航行为、collections、插件、图片处理、第三方库配置等。
- `_pages/`：页面内容入口。当前主要导航页面包括 `ABOUT`、`PROJECTS`、`PUBLICATIONS`、`CV`、`GALLERY`、`CONTACT`。
- `_projects/`：项目集合，每个 Markdown 文件是一项项目详情页。
- `_bibliography/papers.bib`：论文 BibTeX 数据源，由 Jekyll Scholar 渲染到 publications 页面。
- `_news/`：新闻公告条目，首页 News 模块会引用。
- `_data/`：结构化数据，包括 coauthors、venues、repositories、cv 等。
- `_layouts/`：页面布局骨架，例如 `default.liquid`、`about.liquid`、`page.liquid`、`bib.liquid`。
- `_includes/`：可复用 Liquid 组件，例如 header、footer、projects、research_interests、news、scripts 等。
- `_sass/` 与 `assets/css/main.scss`：样式入口、主题变量、布局、基础样式、CV、tabs、distill 等。
- `assets/`：静态资源，包括图片、PDF、视频、音频、JS、CSS、字体、JSON、HTML、Jupyter notebook。
- `.github/workflows/`：GitHub Actions，包含部署、链接检查、Prettier、Lighthouse、Axe accessibility 等。
- `bin/`：Jekyll/Docker 构建和部署辅助脚本。
- `_site/`：Jekyll 生成后的静态网站输出，不建议直接编辑。
- `project_archive/`：agent 日志与每日改动归档。

## 内容入口速查

- 首页个人介绍：`_pages/about.md`
- 首页头像与社交链接：`_pages/about.md` 的 `profile` 配置
- 首页研究兴趣：`_pages/about.md` 的 `research_interests`
- 项目列表页：`_pages/projects.md`
- 项目详情：`_projects/*.md`
- 论文列表页：`_pages/publications.md`
- 论文数据：`_bibliography/papers.bib`
- 新闻：`_news/*.md`
- CV 页面：`_pages/cv.md`
- CV PDF：`assets/pdf/CV_ziqi_liu.pdf`
- 摄影画廊：`_pages/gallery.md` 与 `assets/img/gallery/`
- 联系页面：`_pages/contact.md`

## 当前内容理解

研究方向集中在 ubiquitous computing、human-computer interaction、AI-driven sensing、adaptive intervention、pervasive sensing、personalized state inference、just-in-time intervention。

研究项目包括：

- `PreTap`：面向单手移动交互的隐式可达性分析与点击预测，提交至 ACM IMWUT 2026。
- `COMETIC`：基于 cursor interaction 的智能手机眼动追踪隐式校准，CHI 2025。
- `AroMR`：面向混合现实的环境分布式嗅觉显示，CHI EA 2025。

设计与交互项目包括：

- `Cognitive Pen`
- `Embroidery of Light`
- `Laser Battle Chess`
- `Guidance System Design`
- `TagMagnet`
- `CanvaSphere`

论文数据目前至少包含 COMETIC 与 AroMR，两者都设置了 publication preview，并标记为 selected。

## 构建与验证

常用本地运行方式见 `README.md`：

```bash
docker compose pull
docker compose up
```

访问：

```text
http://localhost:8080
```

常见验证方式：

- 只改文档：检查 Markdown 内容和 git diff 即可。
- 改 Liquid、Sass、配置或内容页面：建议运行 Jekyll 构建或 Docker 本地预览。
- 改前端视觉：建议用浏览器检查桌面与移动视口。
- 改格式相关文件：可运行 `npx prettier . --check`，但注意这会依赖 Node 环境与本地依赖安装状态。

## 维护注意事项

- 优先修改源文件，不直接修改 `_site/`。
- 新增图片、PDF、视频等资源时，放入 `assets/` 对应子目录，并在内容文件中使用相对站点路径。
- 新增项目时，在 `_projects/` 中创建 Markdown，设置 `layout`、`title`、`description`、`tag`、`img`、`importance`、`category`。
- 新增论文时，更新 `_bibliography/papers.bib`；预览图放在 `assets/img/publication_preview/`。
- 修改导航显示时，检查 `_pages/*.md` 的 front matter：`nav`、`nav_order`、`permalink`、`title`。
- `_data/cv.yml` 和 `_pages/profiles.md` 仍保留较多 al-folio 示例内容，若需要启用这些页面，应先替换为真实内容。
- `_config.yml` 中 `scholar.last_name` / `scholar.first_name` 仍是 Einstein 示例值；如果需要在论文作者列表中高亮 Ziqi Liu，应更新此配置。
- `_news/announcement.md` 是未发布示例长公告，`published: false`。

## 网络下载记录

本文件创建时未下载任何网络内容。

## 推送记录

- 20260618 gallery-blur-agent-archive-about-cv-news
- 20260626 research-interest-icons-gallery-news
- 20260708 publication-project-orcid-step
