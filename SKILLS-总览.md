# Skills 技能库总览（整理版）

- 更新日期：2026-10-05
- 库目录：`C:\Users\VIOLET\.skills-manager\skills`
- 管理工具：`C:\Users\VIOLET\.skills-manager\bin\skills-manager-cli.exe`
- 规模：**90** 个技能，全部已注册 + 已打标签
- Codex 已部署：**49**

## 标注说明

| 标记 | 含义 |
| --- | --- |
| ✅ | 已部署到 Codex（`~/.codex/skills` 软链接），可直接调用 |
| ⬜ | 在库中已注册、已打标签，但当前未部署给 Codex |

---

## 一、本次「整理」做了什么

1. **纳管 41 个孤儿技能**：库里原有 41 个目录有 `SKILL.md` 却未注册进 skills-manager。通过「移出暂存 → `skills adopt` 导入」的方式全部纳管，库从 49 → **90**，Codex 可用/可管理范围随之完整。
2. **建立标签体系**：给全部 90 个技能打上 9 类标签（见第三节），可用 `skills list --tag <标签>` 过滤。
3. **建立预设体系**：把 4 个空预设按类别填满，并新建 3 个预设；现在共 8 个预设（见第四节），可在 skills-manager 里一键切换部署给某类 agent。
4. **（上一轮）清理 28 个**：12 个空/无效目录 + 16 个同名副本（`anthro-*`、`taste-*`）。

---

## 二、Codex 部署状态

Codex 当前部署 **49** 个（`~/.codex/skills` 下全部为有效软链接）。

如果想让 Codex 增/减某类技能，推荐用 CLI 按预设或按技能操作：

```powershell
# 查看某技能在各 agent 的部署状态
& 'C:\Users\VIOLET\.skills-manager\bin\skills-manager-cli.exe' skills status code-review

# 把某个预设的技能部署到 Codex（可加 --dry-run 预览）
& 'C:\Users\VIOLET\.skills-manager\bin\skills-manager-cli.exe' presets deploy 前端设计 --agent codex --dry-run

# 部署单个技能到 Codex
& 'C:\Users\VIOLET\.skills-manager\bin\skills-manager-cli.exe' skills deploy animate --agent codex

# 从 Codex 撤下
& 'C:\Users\VIOLET\.skills-manager\bin\skills-manager-cli.exe' skills undeploy animate --agent codex
```

---

## 三、标签体系（9 类）

| 标签 | 数量 | 说明 |
| --- | --- | --- |
| workflow | 26 | 软件工程流程：评审、规格、工单、调试、TDD |
| game | 16 | 游戏开发（Unity/Three.js/Phaser/PixiJS） |
| frontend | 14 | 前端与界面设计 |
| docker | 11 | 容器、Compose、Docker Agent、Sandboxes |
| meta | 8 | 技能库/MCP/向导等元能力 |
| motion | 8 | 动效动画 |
| docs | 8 | 文档与办公文件 |
| art | 3 | 插画与视觉 |
| lang | 1 | 语言专项（Swift） |

> 有重叠：`apple-design`、`emil-design-eng` 同属 frontend+motion；`handoff`、`teach` 同属 workflow+docs；`writing-for-agents` 同属 docs+meta。

---

## 四、预设体系（8 个）

| 预设 | 成员数 | 覆盖范围 |
| --- | --- | --- |
| 全开默认 | 90 | 全部技能 |
| 工程流程 | 34 | workflow + meta |
| 游戏开发 | 16 | game |
| 前端设计 | 14 | frontend |
| 容器与部署 | 11 | docker |
| 动效动画 | 8 | motion |
| 文档编写 | 8 | docs |
| 插画图片 | 3 | art |

> 当前激活预设是「游戏开发」（仅标记，不等于部署集合）。

---

## 五、全库技能目录（按标签分组，90 个）

### 工程流程 (workflow)

| 技能 | Codex | 用途 |
| --- | :---: | --- |
| `code-review` | ✅ | 对分支/PR/改动做「规范+需求」双轴评审 |
| `codebase-design` | ✅ | 深层模块设计词汇（接口/接缝/可测试性） |
| `diagnosing-bugs` | ✅ | 难查 bug 与性能回归的诊断循环 |
| `improve-codebase-architecture` | ✅ | 扫描架构深化点并出 HTML 报告 |
| `implement` | ✅ | 依据 spec/工单实现一块工作 |
| `implement-spec` | ⬜ | 实现 /to-spec + /to-tickets 的产出 |
| `resolving-merge-conflicts` | ✅ | 解决进行中的 git merge/rebase 冲突 |
| `tdd` | ✅ | 测试驱动开发（红-绿-重构） |
| `triage` | ✅ | issue/外部 PR 分流、分类、写 brief |
| `to-spec` | ✅ | 把当前对话整理成 spec 并发布 |
| `to-tickets` | ✅ | 把计划/spec 拆成带依赖的工单 |
| `to-questionnaire` | ✅ | 把答不了的决定转成问卷 |
| `wayfinder` | ✅ | 超大会话尺度的工作规划成决策地图 |
| `handoff` | ✅ | 会话压缩成交接文档 |
| `grill-me` | ✅ | 对计划/设计做不留情面的追问 |
| `grill-with-docs` | ✅ | 追问并产出 ADR 与术语表 |
| `grilling` | ✅ | 高强度质询计划/决定 |
| `wait-what` | ✅ | 上一条没讲清时让对方重讲 |
| `teach` | ✅ | 讲一个新技能或概念 |
| `prototype` | ✅ | 做一次性原型回答设计问题 |
| `domain-modeling` | ⬜ | 领域模型 / GLOSSARY / ADR |
| `setup-matt-pocock-skills` | ✅ | 初始化工程技能仓库 |
| `setup-pre-commit` | ⬜ | 配置 Husky pre-commit 钩子 |
| `pr` | ⬜ | 写 PR 说明 |
| `retro` | ⬜ | 对一次编码会话做复盘 |
| `scaffold-exercises` | ⬜ | 脚手架练习目录结构 |

### 前端设计 (frontend)

| 技能 | Codex | 用途 |
| --- | :---: | --- |
| `frontend-design` | ✅ | 新建/重塑 UI 的视觉方向与排版 |
| `design-taste-frontend` | ✅ | 落地页/作品集/改版的反模板感流程 |
| `impeccable` | ✅ | 前端评审、重设计、打磨、可访问性 |
| `industrial-brutalist-ui` | ✅ | 工业/军事终端风界面规范 |
| `minimalist-ui` | ✅ | 干净编辑风极简界面规范 |
| `theme-factory` | ✅ | 给 artifact 套用/生成主题 |
| `web-artifacts-builder` | ✅ | 用 React/Tailwind/shadcn 构建 HTML artifact |
| `webapp-testing` | ✅ | 用 Playwright 测试本地 Web 应用 |
| `mobile-native` | ⬜ | 让 Web 应用更像原生 App |
| `ask-sonner` | ⬜ | React toast 库 Sonner 使用与排错 |
| `pick-ui-library` | ⬜ | 按任务挑前端库 |
| `migrate-to-shoehorn` | ⬜ | 测试断言迁移到 shoehorn |
| `apple-design` | ⬜ | Apple 式界面与物理感动效（Web） |
| `emil-design-eng` | ⬜ | UI 打磨与组件设计哲学 |

### 动效动画 (motion)

| 技能 | Codex | 用途 |
| --- | :---: | --- |
| `animate` | ⬜ | 从零构建 Web 动画 |
| `animate-expo` | ⬜ | React Native/Expo 动画 |
| `animation-vocabulary` | ⬜ | 动效术语反查词典 |
| `find-animation-opportunities` | ⬜ | 只读地找该动没动的地方 |
| `improve-animations` | ⬜ | 审计全库动效并出改进计划 |
| `review-animations` | ⬜ | 按高标准评审动效代码 |
| `apple-design` | ⬜ | （同前端）Apple 式动效 |
| `emil-design-eng` | ⬜ | （同前端）设计工程哲学 |

### 文档办公 (docs)

| 技能 | Codex | 用途 |
| --- | :---: | --- |
| `docx` | ✅ | 创建/读取/编辑 Word 文档与模板 |
| `xlsx` | ✅ | 创建/读取/编辑/分析电子表格 |
| `pptx` | ✅ | 创建/读取/编辑幻灯片 |
| `pdf` | ✅ | PDF 读取、合并拆分、水印、表单、OCR |
| `research` | ✅ | 面向一手来源调研并产出 Markdown |
| `writing-for-agents` | ✅ | 编写技能 / AGENTS.md / CLAUDE.md |
| `handoff` | ✅ | （同工程流程）会话交接文档 |
| `teach` | ✅ | （同工程流程）讲解概念 |

### 插画视觉 (art)

| 技能 | Codex | 用途 |
| --- | :---: | --- |
| `algorithmic-art` | ✅ | 用 p5.js 做生成式/算法艺术 |
| `canvas-design` | ✅ | 用设计理念产出 .png/.pdf 视觉作品 |
| `brand-guidelines` | ✅ | 套用 Anthropic 官方品牌色与字体 |

### 游戏开发 (game)

| 技能 | Codex | 用途 |
| --- | :---: | --- |
| `game-developer` | ✅ | Unity/Unreal 游戏系统、ECS、物理、网络、优化 |
| `threejs-game-director` | ✅ | Three.js 游戏总入口，路由到子技能 |
| `threejs-gameplay-systems` | ✅ | 玩法系统：脚手架、核心循环、关卡、物理 |
| `threejs-game-ui-designer` | ✅ | 游戏内 HUD、菜单、覆盖层 UI |
| `threejs-qa-release` | ✅ | 游戏 QA、自动 playtest、构建发布 |
| `threejs-3d-generator` | ✅ | 经 Tripo API 生成/绑定/动画 3D 资产 |
| `threejs-audio-generator` | ✅ | 经 ElevenLabs 生成并集成音频 |
| `threejs-scene-setup` | ⬜ | 搭 Three.js 场景（相机/渲染器/循环） |
| `threejs-gltf-loading` | ⬜ | 加载 glTF/GLB 与骨骼动画 |
| `threejs-materials-lighting` | ⬜ | 材质与灯光（PBR/阴影/IBL） |
| `game-feel` | ⬜ | 手感、juice、命中停顿 |
| `game-ui-ux` | ⬜ | 游戏 HUD/菜单/覆盖层设计 |
| `gamedev-router` | ⬜ | 游戏开发技能路由（识别引擎） |
| `phaser-core` | ⬜ | Phaser 4 核心（场景/加载/相机） |
| `phaser-arcade-physics` | ⬜ | Phaser Arcade 物理与碰撞 |
| `pixijs-rendering` | ⬜ | PixiJS v8 渲染层 |

### 容器与部署 (docker)

| 技能 | Codex | 用途 |
| --- | :---: | --- |
| `docker-project-foundations` | ⬜ | 容器化项目基础（Dockerfile/compose） |
| `docker-build-strategies` | ⬜ | Dockerfile 编写与镜像优化 |
| `docker-compose-patterns` | ⬜ | Compose 服务编排 |
| `docker-destructive-guardrails` | ⬜ | 破坏性 Docker 命令护栏 |
| `docker-agent-config` | ⬜ | Docker Agent 配置（agent.yaml） |
| `docker-agent-run` | ⬜ | 运行 Docker Agent（安全模式/沙箱） |
| `docker-agent-deploy` | ⬜ | 把 Agent 暴露为服务/发布 |
| `docker-sandboxes-lifecycle` | ⬜ | Docker Sandboxes 生命周期 |
| `docker-sandboxes-env` | ⬜ | Sandboxes 环境（sbxenv.yaml） |
| `docker-sandboxes-kits` | ⬜ | Sandboxes 套件（kit spec） |
| `docker-sandboxes-network-credentials` | ⬜ | Sandboxes 网络与凭据 |

### 元能力 (meta)

| 技能 | Codex | 用途 |
| --- | :---: | --- |
| `skill-creator` | ✅ | 创建、改进、评估 skill |
| `manage-skills` | ✅ | 用 skills-manager-cli 管理技能库 |
| `find-skills` | ✅ | 发现并安装可用技能 |
| `mcp-builder` | ✅ | 构建高质量 MCP server |
| `wizard` | ✅ | 生成交互式 bash 向导 |
| `ask-matt` | ⬜ | 判断该用哪个技能/流程 |
| `git-guardrails-claude-code` | ⬜ | Claude Code 的 git 危险命令拦截钩子 |
| `writing-for-agents` | ✅ | （同文档）写 agent 文档 |

### 语言 (lang)

| 技能 | Codex | 用途 |
| --- | :---: | --- |
| `write-swift` | ⬜ | 现代 Swift 写法与并发安全 |

---

## 六、已知遗留（不影响使用）

- **来源指针悬空**：55 个「本地」技能的 `source_ref` 指向已删除的路径（41 个指向纳管时的暂存目录 `.adopt-tmp\*`，14 个指向早先删掉的 `anthro-*`/`taste-*` 副本）。技能本体与 `SKILL.md` 完好，`list`/`status`/部署均正常；仅当对它们执行 `skills update` 时该来源无效。如需彻底清理，需要在 skills-manager 内重新指定来源。
- **未部署项**：库中 41 个已整理但未部署到 Codex 的技能，可按上面的预设/技能命令按需部署。

## 七、后续可选动作

1. 按用途把预设部署到 Codex（如 `presets deploy 前端设计 --agent codex`）。
2. 把「全开默认」改为只含有意部署的技能，避免误全量部署。
3. 修正 55 个悬空 `source_ref`。

