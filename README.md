# Hermes-Douyin-Expert-System

> Build an AI-native Douyin Expert Knowledge System.
>
> 目标不是 Prompt，而是建立一个可以持续进化的「抖音专家认知系统」。

---

## 这是什么？

这是一个为 **Hermes Agent**（也兼容 LangGraph、ClaudeCode、OpenManus 等 Agent 框架）构建的**抖音运营专家知识工程**。

它不是：
- ❌ 一个 Prompt 合集
- ❌ 一个 AI 角色扮演
- ❌ 一个抖音运营教程
- ❌ 依赖 LLM 自带知识的聊天应用

它是：
- ✅ 一套经过**人工审核、多源验证、知识蒸馏**的专家认知资产
- ✅ 完全独立于 LLM 的私有记忆库（换模型不影响知识质量）
- ✅ 能够被 Agent Skills 调用的长期 Memory

---

## 项目架构

```
Hermes-Douyin-Expert-System/
├── README.md                     ← 本文
├── ROADMAP.md                    ← 路线图
├── INSTALL.md                    ← 安装指南
├── CHANGELOG.md                  ← 变更日志
├── CONTRIBUTING.md               ← 贡献指南
├── LICENSE
│
├── docs/                         ← 项目文档
│   ├── Architecture.md           ←   系统架构
│   ├── Design-Principles.md      ←   设计原则
│   ├── Naming-Convention.md      ←   命名规范
│   ├── Versioning.md             ←   版本策略
│   ├── Chat-Summary.md           ←   与 ChatGPT 讨论摘要
│   └── FAQ.md                    ←   常见问题
│
├── standards/                    ← 规范
│   ├── Memory-Standard.md        ←   Memory 设计规范
│   ├── Skill-Standard.md         ←   Skill 设计规范
│   ├── Framework-Standard.md     ←   Framework 设计规范
│   ├── Checklist-Standard.md     ←   Checklist 设计规范
│   ├── Knowledge-Standard.md     ←   Knowledge 设计规范
│   └── Citation-Standard.md      ←   引用规范
│
├── memory/                       ← 专家长期记忆（核心资产）
│   ├── INDEX.md
│   ├── L1_Worldview/             ←   世界观（几乎不改）
│   ├── L2_Strategy/              ←   战略（数年更新）
│   ├── L3_Tactics/               ←   战术（按需迭代）
│   └── L4_Platform/              ←   平台规则（变化最快）
│
├── skills/                       ← 执行能力
│   └── ... 按领域分目录
│
├── framework/                    ← 分析框架
│   └── ... 按领域分目录
│
├── checklist/                    ← 检查清单
│   └── ... 按阶段分目录
│
├── repository/                   ← 原始资料（未经加工）
├── knowledge/                    ← 提炼后的知识
│
├── assets/                       ← 图片、图示、模板、示例
├── prompts/                      ← AI 辅助 Prompt
├── templates/                    ← 各类文件模板
├── config/                       ← 索引、标签
├── adapter/                      ← Agent 适配器
└── archive/                      ← 废弃/草稿/实验
```

---

## 四层知识蒸馏

```
repository/     ← 原始资料（课程、文章、案例，永不直接喂给 Agent）
    ↓  人工 + AI 蒸馏
knowledge/      ← 提炼后的知识（经过整理和摘要）
    ↓  进一步蒸馏 + 多源交叉验证
memory/         ← 专家长期记忆（最终进入 Hermes 的认知核心）
    ↓  被调用
skills/         ← 执行能力（调用 Memory 完成实际工作）
```

---

## Memory 分级体系

| 等级 | 名称 | 内容示例 | 更新频率 |
|------|------|----------|----------|
| **L1** | 世界观 | 为什么做内容、为什么做人设、为什么做 IP | 几乎不改 |
| **L2** | 战略 | 为什么账号增长、为什么用户关注、为什么停留率决定一切 | 数年更新 |
| **L3** | 战术 | 昵称设计、简介三段论、封面锚点、黄金三秒、剪辑节奏 | 按需迭代 |
| **L4** | 平台规则 | 当前算法机制、流量池规则、平台政策 | 变化最快 |

---

## Memory 收录标准

只有通过以下**6 条铁律**的知识才能进入 Memory：

1. **必须具有明确操作锚点** — 能指导具体动作（"做好定位"❌）
2. **必须解释"为什么"** — 揭示底层机制，而非仅说"怎么做"
3. **尽量有多来源验证** — ≥3 个独立来源交叉验证
4. **能够跨赛道复用** — 优先底层规律，不收录短期技巧
5. **与抖音生态强相关** — 不是泛互联网运营理论
6. **不违背创作哲学** — 长期 IP > 短期流量

---

## 实施路线

| 阶段 | 内容 | 状态 |
|------|------|------|
| **Phase 1** | 建立工程骨架（本项目当前阶段） | 🚧 进行中 |
| Phase 2 | 建设 Memory（L1→L4 逐级填充） | ⬜ |
| Phase 3 | 建设 Framework（分析框架） | ⬜ |
| Phase 4 | 建设 Checklist（检查清单） | ⬜ |
| Phase 5 | 建设 Skills（执行能力） | ⬜ |
| Phase 6 | 接入 Agent（Hermes 适配器） | ⬜ |

---

## 创作者的账号方向

本项目专为以下定位服务：

| 主线 | 内容 | 重点 |
|------|------|------|
| 🏔️ 自然探索 | 山、湖、森林、海、日落、四季 | 视觉 |
| 🏙️ 人文探索 | 城市、街道、建筑、烟火气 | 故事 |
| 🧠 精神探索 | 旅行思考、孤独、成长、自由 | 思想 |

**创作哲学**：大道至简 · 真实比完美重要 · 尊重风景 · 长期 IP > 短期流量

---

## License

MIT
