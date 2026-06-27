# Hermes-Douyin-Expert-System

> Build an AI-native Douyin Expert Knowledge System.
>
> 目标不是 Prompt，而是建立一个可以持续进化的「抖音专家认知系统」。

---

## 这是什么？

一套**独立于 LLM 的抖音运营专家知识工程**，包含：

- **Memory（长期认知）**：顶级抖音操盘手"大脑中默认知道"的知识。不是教程，是 CPU 指令集。
- **Skills（执行能力）**：调用 Memory 完成账号诊断、脚本设计、导演规划、数据分析等任务。
- **Framework（分析框架）**：选题判断、定位验证、商业化推演等决策模型。
- **Checklist（检查清单）**：发布前、拍摄前、数据复盘等可执行的审核标准。
- **Knowledge（知识提炼）**：从原始资料中提取、整理、交叉验证后的结构化知识。

---

## 设计原则

1. **先知识工程，再 Agent 工程** — 不绑定 Hermes，任何 Agent 框架（LangGraph、Claude Code、OpenManus……）都能加载
2. **知识独立于 LLM** — 换模型不影响认知质量
3. **交叉验证** — 每条核心认知需多源验证
4. **人工最终审核** — AI 搜集提炼，人做最终入库决策
5. **以 Commit 为推进单位** — 每次迭代对应一次可追踪的知识沉淀

---

## 项目结构

```
Hermes-Douyin-Expert-System/
│
├── README.md                  ← 你在这
├── ROADMAP.md                 ← 建设路线图
├── INSTALL.md                 ← 如何接入 Hermes / 其他 Agent
├── CHANGELOG.md               ← 变更记录
├── CONTRIBUTING.md            ← 贡献指南
├── LICENSE                    ← MIT
│
├── docs/                      ← 项目文档
│   ├── Architecture.md        ← 系统架构说明
│   ├── Design-Principles.md   ← 设计原则详解
│   ├── Naming-Convention.md   ← 命名规范
│   ├── Versioning.md          ← 版本管理策略
│   └── FAQ.md                 ← 常见问题
│
├── standards/                 ← 规范定义
│   ├── Memory-Standard.md     ← Memory 的编号/分类/字段/可信度规范
│   ├── Skill-Standard.md      ← Skill 的组成/调用/输入输出规范
│   ├── Framework-Standard.md  ← Framework 的统一格式
│   ├── Checklist-Standard.md  ← Checklist 的统一格式
│   ├── Knowledge-Standard.md  ← Knowledge 条目规范
│   └── Citation-Standard.md   ← 引用/来源标注规范
│
├── memory/                    ← 专家长期记忆
│   ├── L1_Worldview/          ← 世界观层：创作者哲学、抖音底层逻辑
│   ├── L2_Strategy/           ← 策略层：账号定位、IP打造、商业化
│   ├── L3_Tactics/            ← 战术层：标题、封面、黄金三秒、完播率
│   ├── L4_Platform/           ← 平台层：算法机制、推荐逻辑、流量池
│   └── INDEX.md               ← Memory 索引
│
├── skills/                    ← 执行技能
│   ├── Account/               ← 账号诊断、主页优化
│   ├── Content/               ← 内容策划
│   ├── Script/                ← 脚本生成
│   ├── Director/              ← 导演规划
│   ├── Shooting/              ← 拍摄指导
│   ├── Editing/               ← 剪辑建议
│   ├── Algorithm/             ← 算法分析
│   ├── Growth/                ← 增长策略
│   ├── Commercial/            ← 商业变现
│   └── INDEX.md
│
├── framework/                 ← 分析框架
│   ├── Account/               ← 账号诊断框架
│   ├── Positioning/           ← 定位验证框架
│   ├── Topic/                 ← 选题判断框架
│   ├── Script/                ← 脚本评估框架
│   ├── Director/              ← 导演审查框架
│   ├── Editing/               ← 剪辑审查框架
│   ├── Review/                ← 内容复盘框架
│   ├── Data/                  ← 数据分析框架
│   ├── IP/                    ← IP打造框架
│   └── INDEX.md
│
├── checklist/                 ← 检查清单
│   ├── Before-Shooting/       ← 拍摄前检查
│   ├── Before-Editing/        ← 剪辑前检查
│   ├── Before-Publishing/     ← 发布前检查
│   ├── Homepage/              ← 主页检查
│   ├── Weekly-Review/         ← 周复盘
│   ├── Monthly-Review/        ← 月复盘
│   └── INDEX.md
│
├── knowledge/                 ← 知识提炼
│   ├── Official/              ← 抖音官方资料提炼
│   ├── Reports/               ← 行业报告提炼
│   ├── Books/                 ← 书籍提炼
│   ├── Courses/               ← 课程提炼
│   ├── Interviews/            ← 访谈/播客提炼
│   ├── Podcasts/
│   ├── Community/             ← 社区精华提炼
│   ├── Case-Studies/          ← 案例研究
│   └── INDEX.md
│
├── repository/                ← 原始资料库（未经加工）
│   ├── Official-Docs/
│   ├── Douyin-Docs/
│   ├── Creator-Academy/
│   ├── MCN-Internal/
│   ├── Course-Notes/
│   ├── Articles/
│   ├── Videos/
│   ├── Case-Library/
│   └── Research/
│
├── assets/                    ← 静态资源
│   ├── Images/
│   ├── Diagrams/
│   ├── Templates/
│   └── Examples/
│
├── prompts/                   ← 知识工程辅助 Prompt
│   ├── Knowledge-Extraction.md
│   ├── Memory-Review.md
│   ├── Skill-Build.md
│   ├── Framework-Build.md
│   └── QA.md
│
├── templates/                 ← 文件模板
│   ├── Memory.md              ← 新建 Memory 条目的模板
│   ├── Skill.md               ← 新建 Skill 的模板
│   ├── Framework.md           ← 新建 Framework 的模板
│   ├── Checklist.md           ← 新建 Checklist 的模板
│   ├── Knowledge.md           ← 新建 Knowledge 条目的模板
│   └── Case.md                ← 案例研究模板
│
├── config/                    ← 配置文件
│   ├── memory-index.md        ← Memory 索引配置
│   ├── skill-index.md         ← Skill 索引配置
│   ├── framework-index.md     ← Framework 索引配置
│   ├── checklist-index.md     ← Checklist 索引配置
│   └── tags.md                ← 标签体系
│
├── adapter/                   ← Agent 框架适配器
│   ├── Hermes/                ← Hermes Agent 适配
│   ├── LangGraph/
│   ├── OpenManus/
│   ├── ClaudeCode/
│   └── Future/
│
└── archive/                   ← 归档区
    ├── Deprecated/
    ├── Draft/
    └── Experiments/
```

---

## 四层知识流向

```
原始资料（repository/）
       ↓  搜集、存档
知识提炼（knowledge/）
       ↓  整理、交叉验证、去噪
专家记忆（memory/）
       ↓  蒸馏为可被 Agent 加载的长期认知
执行能力（skills/）
       ↓  调用 Memory + Framework + Checklist 完成工作
```

---

## 建设路线图

| Phase | 内容 | 说明 |
|-------|------|------|
| **Phase 1** ✅ | 项目骨架 | README、ROADMAP、Standards、Templates |
| **Phase 2** | Memory 建设 | 按 M0001→M00xx 逐条构建专家记忆 |
| **Phase 3** | Framework 建设 | 账号定位、选题、脚本等分析框架 |
| **Phase 4** | Checklist 建设 | 发布前检查、拍摄检查、数据复盘等 |
| **Phase 5** | Skills 建设 | Skills 优先调用 Memory→Framework→Checklist |
| **Phase 6** | Adapter 接入 | 将知识工程接入 Hermes 等 Agent 框架 |

详细路线见 [ROADMAP.md](./ROADMAP.md)。

---

## 许可证

MIT License — 详见 [LICENSE](./LICENSE)
