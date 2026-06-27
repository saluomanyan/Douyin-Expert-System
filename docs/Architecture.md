# Architecture · 系统架构

> Hermes-Douyin-Expert-System 的整体架构设计说明。

---

## 核心理念

本系统是一个 **知识工程 (Knowledge Engineering)**，而非 Prompt 工程。

核心架构遵循：**知识分层 · 独立于 Agent · 人工最终审核**。

---

## 整体架构

```
┌─────────────────────────────────────────────────┐
│                  Agent 框架层                      │
│  Hermes / LangGraph / Claude Code / OpenManus     │
│  （通过 adapter/ 适配接入）                        │
├─────────────────────────────────────────────────┤
│                  Skills 执行层                     │
│  调用 Memory + Framework + Checklist 完成工作     │
├──────────┬──────────┬──────────┬────────────────┤
│  Memory  │Framework │Checklist │  Knowledge     │
│  长期认知 │ 分析框架  │ 检查清单  │  知识提炼      │
├──────────┴──────────┴──────────┴────────────────┤
│                  Repository 原始资料层             │
│  课程/文章/案例/官方文档/行业报告                   │
└─────────────────────────────────────────────────┘
```

---

## 四层知识流向

```
Repository（原始资料）
    ↓  搜集 · 存档 · 去重
Knowledge（知识提炼）
    ↓  整理 · 交叉验证 · 结构化
Memory（专家记忆）
    ↓  蒸馏 · 精简 · 编号 · 分级
Skills（执行能力）
    ↓  调用 Memory → Framework → Checklist
Agent 输出
```

---

## 各层职责

| 层 | 职责 | 产出物格式 | 谁维护 |
|----|------|-----------|--------|
| Repository | 原始资料存档 | 原文/笔记/链接 | AI 搜集 + 人归档 |
| Knowledge | 去噪提炼 | 结构化摘要 | AI 提炼 + 人审核 |
| Memory | 专家认知 | M编号 .md | AI 蒸馏 + 人修改 |
| Skills | 执行能力 | Skill .md | 人定义 + AI 调用 |

---

## 关键设计决策

1. **Memory 不绑定 LLM** — 知识独立于模型，换模型不影响认知质量
2. **Skills 不直接依赖 LLM** — Skills 优先调用 Memory/Framework/Checklist，LLM 只组织最终语言
3. **Adapter 作为薄层** — 本系统对任何 Agent 框架的接入只通过 adapter/ 目录，不修改核心知识内容
4. **人工最终审核** — 所有进入 Memory 的知识必须经过人工阅读、修改、确认
