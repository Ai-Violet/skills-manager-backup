# Skills 技能库总览(含 Codex 部署标注)

- 生成日期:2026-10-05(清理后更新)
- 数据来源:skills-manager 中央库 `C:\Users\VIOLET\.skills-manager\skills`
- 元数据:`.skills-manager\skills\*.json`(每个受管技能一个文件)
- Codex 部署目录:`C:\Users\VIOLET\.codex\skills`(均是指向中央库的软链接)
- 规模:库内 **90** 个技能目录 → 受管 49 → **Codex 已启用 49**
- 本次清理:移除 **28** 个(12 个空/无效 + 16 个同名副本)

## 标注说明

| 标记 | 含义 |
| --- | --- |
| `[Codex]` | 已通过 skills-manager 部署到 `~/.codex/skills`,Codex 可直接调用 |
| `[库中]` | 存在于中央库、结构有效,但当前未部署给 Codex |

> 结论:中央库里**所有受管技能都做了 Codex 部署**,Codex 可用集 = 受管集合,共 49 个。
> 清理后剩余的 41 个未部署技能结构均有效(含 SKILL.md),可按需再纳管。

---

## 一、Codex 已启用的技能(49)

### 1. 工程流程与协作(26)

| 技能 | 用途 | 来源 |
| --- | --- | --- |
| code-review | 按「规范 + 需求」双轴并行评审分支/PR/改动 | import |
| codebase-design | 深层模块设计词汇:接口、接缝、可测试性 | import |
| diagnosing-bugs | 难查 bug 与性能回归的诊断循环 | import |
| improve-codebase-architecture | 扫描架构深化点,出 HTML 报告并逐项推敲 | import |
| implement | 依据 spec/工单实现一块工作 | import |
| resolving-merge-conflicts | 解决进行中的 git merge/rebase 冲突 | import |
| tdd | 测试驱动开发(红-绿-重构) | import |
| triage | 对 issue/外部 PR 分流、分类、验证、写 brief | import |
| to-spec | 把当前对话整理成 spec 并发布到 issue tracker | import |
| to-tickets | 把计划/spec 拆成带依赖的 tracer-bullet 工单 | import |
| to-questionnaire | 把答不了的决定转成问卷 | import |
| wayfinder | 把超大会话尺度的工作规划成决策工单地图 | import |
| handoff | 把会话压缩成交接文档给另一个 agent | import |
| grill-me | 对计划/设计做不留情面的追问 | import |
| grill-with-docs | 追问的同时产出 ADR 与术语表 | import |
| grilling | 就计划、决定、想法做高强度质询 | import |
| wait-what | 上一条没讲清时让对方重讲 | import |
| teach | 在当前工作区内讲一个新技能或概念 | import |
| research | 面向高可信一手来源调研并产出 Markdown | import |
| prototype | 做一次性原型回答设计问题 | import |
| setup-matt-pocock-skills | 为工程类技能初始化仓库 | import |
| writing-for-agents | 编写技能 / AGENTS.md / CLAUDE.md | import |
| skill-creator | 创建、改进、评估 skill | local |
| manage-skills | 用 skills-manager-cli 管理/部署技能库 | git |
| find-skills | 发现并安装可用技能 | skillssh |
| mcp-builder | 构建高质量 MCP server | local |

### 2. 前端与界面设计(8)

| 技能 | 用途 | 来源 |
| --- | --- | --- |
| frontend-design | 新建/重塑 UI 时的视觉方向与排版取舍 | import |
| design-taste-frontend | 落地页/作品集/改版的「反模板感」流程 | local |
| impeccable | 前端评审、重设计、打磨、可访问性 | import |
| industrial-brutalist-ui | 工业/军事终端风界面规范 | local |
| minimalist-ui | 干净编辑风极简界面规范 | local |
| web-artifacts-builder | 用 React/Tailwind/shadcn 构建复杂 HTML artifact | local |
| webapp-testing | 用 Playwright 测试本地 Web 应用 | import |
| theme-factory | 给 artifact 套用/生成主题 | local |

### 3. 文档与办公文件(4)

| 技能 | 用途 | 来源 |
| --- | --- | --- |
| docx | 创建/读取/编辑 Word 文档与模板 | local |
| xlsx | 创建/读取/编辑/分析电子表格 | local |
| pptx | 创建/读取/编辑幻灯片 | local |
| pdf | PDF 读取、合并拆分、水印、表单、OCR | local |

### 4. 图像与视觉(3)

| 技能 | 用途 | 来源 |
| --- | --- | --- |
| algorithmic-art | 用 p5.js 做生成式/算法艺术 | local |
| canvas-design | 用设计理念产出 .png/.pdf 视觉作品 | local |
| brand-guidelines | 套用 Anthropic 官方品牌色与字体 | local |

### 5. 游戏开发(7)

| 技能 | 用途 | 来源 |
| --- | --- | --- |
| threejs-game-director | Three.js 浏览器游戏总入口 | skillssh |
| threejs-gameplay-systems | 玩法系统:脚手架、核心循环、关卡、物理、手感 | skillssh |
| threejs-game-ui-designer | 游戏内 HUD、菜单、覆盖层 UI | skillssh |
| threejs-qa-release | 游戏 QA、自动 playtest、构建发布 | skillssh |
| threejs-3d-generator | 经 Tripo API 生成/绑定/动画 3D 资产 | skillssh |
| threejs-audio-generator | 经 ElevenLabs 生成并集成音频 | skillssh |
| game-developer | Unity/Unreal 游戏系统、ECS、物理、网络、优化 | skillssh |

### 6. 工具(1)

| 技能 | 用途 | 来源 |
| --- | --- | --- |
| wizard | 生成引导人操作基础设施/凭据的交互式向导 | import |

---

## 二、库中结构有效但未部署到 Codex 的技能(41)

这些技能有完整 SKILL.md,可随时纳管部署,只是当前没部署给 Codex。

### 动效与动画(7)
- animate — 从零构建 Web 动画
- animate-expo — React Native/Expo 动画
- animation-vocabulary — 动效术语反查词典
- find-animation-opportunities — 只读地找该动没动的地方
- improve-animations — 审计全库动效并出改进计划
- review-animations — 按高标准评审动效代码
- apple-design — Apple 式界面与物理感动效

### 前端 UI 与组件(5)
- emil-design-eng — UI 打磨与组件设计哲学
- mobile-native — 让 Web 应用在手机上更像原生
- ask-sonner — React toast 库 Sonner 的使用与排错
- pick-ui-library — 按前端任务从精选清单挑库
- migrate-to-shoehorn — 测试断言迁移到 shoehorn

### 游戏开发扩展(9)
- gamedev-router — 游戏开发技能路由入口
- game-feel — 手感调校
- game-ui-ux — 游戏 UI/UX
- phaser-core、phaser-arcade-physics — Phaser 核心与 Arcade 物理
- pixijs-rendering — PixiJS 渲染
- threejs-scene-setup、threejs-gltf-loading、threejs-materials-lighting — Three.js 场景/模型/材质灯光

### Docker 与 Agent(12)
- docker-project-foundations、docker-build-strategies、docker-compose-patterns — 容器化项目、镜像构建、Compose 编排
- docker-destructive-guardrails — 破坏性 Docker 命令护栏
- docker-agent-config、docker-agent-run、docker-agent-deploy — Docker Agent 配置/运行/部署
- docker-sandboxes-lifecycle、docker-sandboxes-env、docker-sandboxes-kits、docker-sandboxes-network-credentials — Docker Sandboxes 生命周期/环境/套件/网络凭据

### 其他工程与文档(8)
- domain-modeling — 领域模型(GLOSSARY、ADR)
- implement-spec — 实现 /to-spec + /to-tickets 的产出
- pr — 写 PR 说明;retro — 会话复盘
- scaffold-exercises — 脚手架练习;setup-pre-commit — Husky 提交钩子
- write-swift — Swift 写法;git-guardrails-claude-code — Claude Code 的 git 危险命令拦截钩子(偏 Claude)
- ask-matt — 帮你判断该用哪个技能/流程的路由器

---

## 三、本次已移除的技能(28)

移除标准:对 Codex 不可安装(无 SKILL.md / 空目录),或与已部署技能同名重复。基础版均保留且已部署,移除副本不影响现有能力。仓库有 git 自动备份,副本可按需从历史恢复。

### A. 空目录 / 无 SKILL.md,无法安装(12)
`audio-design`、`book-to-skill`(断链,目标缺失)、`camera-systems`、`card-game`、`create-game-assets`、`docker-skill-index`、`falsify-the-problem`、`input-systems`、`itch-publish`、`platformer`、`roguelike`、`save-systems`

### B. 与基础版同名的重复副本(16)
- `anthro-*` × 13:anthro-algorithmic-art、anthro-brand-guidelines、anthro-canvas-design、anthro-docx、anthro-frontend-design、anthro-mcp-builder、anthro-pdf、anthro-pptx、anthro-skill-creator、anthro-theme-factory、anthro-web-artifacts-builder、anthro-webapp-testing、anthro-xlsx
- `taste-*` × 3:taste-brutalist(= industrial-brutalist-ui)、taste-minimalist(= minimalist-ui)、taste-skill(= design-taste-frontend)

> 说明:这些副本的 SKILL.md `name` 与基础版完全相同,同时安装会在 Codex 中产生同名冲突,故一并清理。

---

## 四、其他 Agent 的部署情况

| Agent | 部署目录 | 数量 |
| --- | --- | --- |
| **Codex** | `C:\Users\VIOLET\.codex\skills` | 49(全部受管技能) |
| Claude Code | `C:\Users\VIOLET\.claude\skills` | 28(工程流程类子集) |
| Codex 内置系统技能 | `C:\Users\VIOLET\.codex\skills\.system` | imagegen、openai-docs、review-agent、skill-creator、skill-installer |

---

## 五、场景(Preset)现状

skills-manager 存有 5 个场景,目前只有「全开默认」挂了全部 49 个成员,其余 4 个为空:

| 场景 | 成员数 | 建议放哪些 |
| --- | --- | --- |
| 全开默认 | 49 | 保持全部 |
| 前端设计 | 0 | frontend-design、design-taste-frontend、impeccable、industrial-brutalist-ui、minimalist-ui、theme-factory、web-artifacts-builder、webapp-testing |
| 文档编写 | 0 | docx、xlsx、pptx、pdf |
| 游戏开发 | 0 | game-developer、threejs-game-director、threejs-gameplay-systems、threejs-game-ui-designer、threejs-qa-release、threejs-3d-generator、threejs-audio-generator |
| 插画图片 | 0 | algorithmic-art、canvas-design、brand-guidelines |

---

## 六、维护建议

1. 后续增删/部署统一走 `manage-skills`(skills-manager-cli),不要直接改 `~/.codex/skills` 软链接。
2. 想要按用途切换技能集,可在 skills-manager 里把上面第五节的分组填进对应场景。
3. 41 个未部署技能里,Docker(12)、Phaser/PixiJS/Three.js 细分(9)、动效(7)最有价值按需纳管。

