# Skills 技能库总览(含 Codex 部署标注)

- 生成日期:2026-10-05
- 数据来源:skills-manager 中央库 `C:\Users\VIOLET\.skills-manager\skills`
- 元数据:`.skills-manager\skills\*.json`(每个受管技能一个文件)
- Codex 部署目录:`C:\Users\VIOLET\.codex\skills`(均为指向中央库的软链接)
- 规模:库内 118 个技能目录 → 受管 49 个 → **Codex 已启用 49 个**

## 标注说明

| 标记 | 含义 |
| --- | --- |
| `[Codex]` | 已通过 skills-manager 部署到 `~/.codex/skills`,Codex 可直接调用 |
| `[库中]` | 存在于中央库,但当前未部署给 Codex |

> 结论:当前中央库里**所有受管(registered)技能都做了 Codex 部署**,即 Codex 的可用集 = 受管集合,共 49 个。
>
> 库里另有 69 个目录未纳入 skills-manager 元数据,因此没有部署到 Codex(详见第三节)。

---

## 一、Codex 已启用的技能(49 个)

### 1. 工程流程与协作(26)

| 技能 | 用途 | 来源 |
| --- | --- | --- |
| code-review | 对某分支/PR/工作区改动按「规范 + 需求」双轴并行评审 | import |
| codebase-design | 深层模块设计词汇:接口、接缝、可测试性 | import |
| diagnosing-bugs | 难查 bug 与性能回归的诊断循环 | import |
| improve-codebase-architecture | 扫描代码库找架构深化点,出 HTML 报告并逐项推敲 | import |
| implement | 依据 spec/工单实现一块工作 | import |
| resolving-merge-conflicts | 解决进行中的 git merge/rebase 冲突 | import |
| tdd | 测试驱动开发(红-绿-重构、集成测试) | import |
| triage | 按状态机对 issue/外部 PR 分流、分类、验证、写 brief | import |
| to-spec | 把当前对话整理成 spec 并发布到 issue tracker | import |
| to-tickets | 把计划/spec 拆成带依赖关系的 tracer-bullet 工单 | import |
| to-questionnaire | 把答不了的决定转成给别人填的问卷 | import |
| wayfinder | 把超大会话尺度的工作规划成决策工单地图并逐个解决 | import |
| handoff | 把当前会话压缩成交接文档给另一个 agent | import |
| grill-me | 对计划/设计做不留情面的追问 | import |
| grill-with-docs | 追问的同时产出 ADR 与术语表 | import |
| grilling | 就计划、决定、想法做高强度质询 | import |
| wait-what | 上一条没讲清时让对方重新讲一遍 | import |
| teach | 在当前工作区内给你讲一个新技能或概念 | import |
| research | 面向高可信一手来源调研并产出 Markdown 报告 | import |
| prototype | 做一个一次性原型回答设计问题 | import |
| setup-matt-pocock-skills | 为工程类技能初始化仓库(issue tracker、标签、文档结构) | import |
| writing-for-agents | 写给 agent 看的文档,编写技能 / AGENTS.md / CLAUDE.md | import |
| skill-creator | 创建、改进、评估 skill | local |
| manage-skills | 用 skills-manager-cli 管理技能库、按 agent 部署/撤下 | git |
| find-skills | 发现并安装可用技能 | skillssh |
| mcp-builder | 构建高质量 MCP server(Python/TS) | local |

### 2. 前端与界面设计(8)

| 技能 | 用途 | 来源 |
| --- | --- | --- |
| frontend-design | 新建/重塑 UI 时的视觉方向与排版取舍 | import |
| design-taste-frontend | 落地页/作品集/改版的「反模板感」设计流程 | local |
| impeccable | 前端的评审、重设计、打磨、可访问性、响应式等全套 | import |
| industrial-brutalist-ui | 工业/军事终端风界面规范 | local |
| minimalist-ui | 干净编辑风的极简界面规范 | local |
| web-artifacts-builder | 用 React/Tailwind/shadcn 构建复杂 HTML artifact | local |
| webapp-testing | 用 Playwright 交互测试本地 Web 应用 | import |
| theme-factory | 给 artifact 套用/生成主题(配色字体) | local |

### 3. 文档与办公文件(4)

| 技能 | 用途 | 来源 |
| --- | --- | --- |
| docx | 创建/读取/编辑 Word 文档与模板 | local |
| xlsx | 创建/读取/编辑/分析电子表格 | local |
| pptx | 创建/读取/编辑幻灯片 | local |
| pdf | PDF 读取、合并拆分、水印、表单、OCR 等 | local |

### 4. 图像与视觉(3)

| 技能 | 用途 | 来源 |
| --- | --- | --- |
| algorithmic-art | 用 p5.js 做生成式/算法艺术 | local |
| canvas-design | 用设计理念产出 .png/.pdf 视觉作品 | local |
| brand-guidelines | 套用 Anthropic 官方品牌色与字体 | local |

### 5. 游戏开发(7)

| 技能 | 用途 | 来源 |
| --- | --- | --- |
| threejs-game-director | Three.js 浏览器游戏的总入口,路由到各子技能 | skillssh |
| threejs-gameplay-systems | 玩法系统:脚手架、核心循环、关卡、物理、手感 | skillssh |
| threejs-game-ui-designer | 游戏内 HUD、菜单、覆盖层的 UI 设计 | skillssh |
| threejs-qa-release | 游戏 QA、自动 playtest、构建与发布 | skillssh |
| threejs-3d-generator | 经 Tripo API 生成/绑定/动画 3D 资产 | skillssh |
| threejs-audio-generator | 经 ElevenLabs 生成并集成音效/音乐/配音 | skillssh |
| game-developer | Unity/Unreal 游戏系统、ECS、物理、网络、优化 | skillssh |

### 6. 工具(1)

| 技能 | 用途 | 来源 |
| --- | --- | --- |
| wizard | 生成引导人一步步操作基础设施/凭据的交互式 bash 向导 | import |

---

## 二、库中未部署到 Codex 的技能(69 个)

这些目录在中央库里,但没有 skills-manager 元数据,因此 Codex 未启用。

### 动画与动效(7)
- **animate** — 从零构建 Web 动画(是否动、动什么、曲线、时长)
- **animate-expo** — React Native/Expo 动画(Reanimated、手势、触感)
- **animation-vocabulary** — 动效术语反查词典(「弹出时那下弹跳」→ Pop in)
- **find-animation-opportunities** — 只读地找「该动没动」的地方并给精确参数
- **improve-animations** — 审计全库动效并给出可执行改进计划
- **review-animations** — 按 Emil Kowalski 的高标准评审动效代码
- **apple-design** — Apple 式界面与物理感动效的 Web 化

### 前端 UI 与组件(6)
- **emil-design-eng** — Emil Kowalski 的 UI 打磨与组件设计哲学
- **mobile-native** — 让 Web 应用在手机上更像原生的小修小补
- **ask-sonner** — React toast 库 Sonner 的使用与排错
- **pick-ui-library** — 按前端任务从精选清单里挑库(数字输入、图表、拖拽等)
- **migrate-to-shoehorn** — 测试里把 as 断言迁移到 @total-typescript/shoehorn
- **domain-modeling** — 建立并打磨项目领域模型(GLOSSARY、ADR)

### 游戏开发扩展(12)
- **gamedev-router** — 游戏开发技能路由入口
- **game-feel** — 手感调校
- **game-ui-ux** — 游戏 UI/UX
- **create-game-assets** — 生成游戏美术资产
- **camera-systems** — 相机系统
- **input-systems** — 输入系统
- **platformer** — 平台跳跃类玩法
- **roguelike** — Roguelike 玩法
- **card-game** — 卡牌游戏玩法
- **save-systems** — 存档系统
- **itch-publish** — 发布到 itch.io
- **audio-design** — 音频设计(无 SKILL.md)

### Phaser / PixiJS / Three.js 细分(6)
- **phaser-core**、**phaser-arcade-physics** — Phaser 核心与 Arcade 物理
- **pixijs-rendering** — PixiJS 渲染
- **threejs-scene-setup**、**threejs-gltf-loading**、**threejs-materials-lighting** — Three.js 场景、模型加载、材质与灯光

### Docker 与 Agent(12)
- **docker-project-foundations**、**docker-build-strategies**、**docker-compose-patterns** — 容器化项目基础、镜像构建、Compose 编排
- **docker-destructive-guardrails** — 破坏性 Docker 命令护栏
- **docker-agent-config**、**docker-agent-run**、**docker-agent-deploy** — Docker Agent 配置、运行、部署
- **docker-sandboxes-lifecycle**、**docker-sandboxes-env**、**docker-sandboxes-kits**、**docker-sandboxes-network-credentials** — Docker Sandboxes 生命周期、环境、套件、网络与凭据
- **docker-skill-index** — Docker 技能索引

### 其他(6)
- **ask-matt** — 帮你判断该用哪个技能/流程的路由器
- **book-to-skill** — 把书转成技能(软链接到 `~/.cc-switch\skills`)
- **falsify-the-problem** — 证伪问题(无 SKILL.md)
- **git-guardrails-claude-code** — 给 Claude Code 装 git 危险命令拦截钩子
- **implement-spec** — 实现 /to-spec + /to-tickets 的产出
- **pr**、**retro**、**scaffold-exercises**、**setup-pre-commit**、**write-swift** — 写 PR 说明、会话复盘、脚手架练习、Husky 提交钩子、Swift 写法

### anthro-\* 前缀副本(13,内容与基础版重复)
- anthro-algorithmic-art、anthro-brand-guidelines、anthro-canvas-design、anthro-docx、anthro-frontend-design、anthro-mcp-builder、anthro-pdf、anthro-pptx、anthro-skill-creator、anthro-theme-factory、anthro-web-artifacts-builder、anthro-webapp-testing、anthro-xlsx

### taste-\* 前缀变体(3)
- taste-brutalist(= industrial-brutalist-ui)、taste-minimalist(= minimalist-ui)、taste-skill(= design-taste-frontend)

---

## 三、其他 Agent 的部署情况

| Agent | 部署目录 | 数量 |
| --- | --- | --- |
| **Codex** | `C:\Users\VIOLET\.codex\skills` | 49(全部受管技能) |
| Claude Code | `C:\Users\VIOLET\.claude\skills` | 28(工程流程类子集) |
| Codex 内置系统技能 | `C:\Users\VIOLET\.codex\skills\.system` | imagegen、openai-docs、review-agent、skill-creator、skill-installer |

Claude Code 比 Codex 多的没有;少的(未部署给 Claude)主要是:docx、xlsx、pptx、pdf、theme-factory、web-artifacts-builder、algorithmic-art、canvas-design、brand-guidelines、design-taste-frontend、industrial-brutalist-ui、minimalist-ui、game-developer、threejs-\*(6)、find-skills、mcp-builder、skill-creator。

---

## 四、场景(Preset)现状

skills-manager 里存有 5 个场景,但只有「全开默认」挂了技能成员(即上面 49 个全部),其余 4 个为空:

| 场景 | 成员数 |
| --- | --- |
| 全开默认 | 49 |
| 前端设计 | 0 |
| 文档编写 | 0 |
| 游戏开发 | 0 |
| 插画图片 | 0 |

---

## 五、维护建议

1. 若想让 Codex 更聚焦,可按场景把技能分组部署:「前端设计」放 frontend-design / design-taste-frontend / impeccable / 两个 ui 风格 + theme-factory;「文档编写」放 docx/xlsx/pptx/pdf;「游戏开发」放 game-developer + threejs-*;「插画图片」放 algorithmic-art / canvas-design / brand-guidelines。
2. 69 个未部署技能里,Docker、Phaser/PixiJS、游戏玩法细分、anthro-/taste- 副本最有可整理空间:副本可直接去重,游戏与 Docker 可按需纳管。
3. 建议用 `manage-skills` 或 skills-manager-cli 做后续的增删,避免直接改 `~/.codex/skills` 软链接。

