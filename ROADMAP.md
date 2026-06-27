# ROADMAP · Hermes-Douyin-Expert-System

> 建设路线图。每个 Phase 对应一组 GitHub Commit，逐步构建完整的抖音专家知识系统。

---

## Phase 1 ✅ — 项目骨架（当前）

**目标**：建立整个知识工程的目录结构和规范体系。

| 文件/目录 | 状态 |
|-----------|------|
| README.md | ✅ |
| ROADMAP.md | ✅ |
| INSTALL.md | ✅ |
| CHANGELOG.md | ✅ |
| CONTRIBUTING.md | ✅ |
| LICENSE | ✅ |
| docs/ | ✅ |
| standards/ | ✅ |
| memory/INDEX.md | ✅ |
| skills/INDEX.md | ✅ |
| framework/INDEX.md | ✅ |
| checklist/INDEX.md | ✅ |
| knowledge/INDEX.md | ✅ |
| prompts/ | ✅ |
| templates/ | ✅ |
| config/ | ✅ |
| adapter/ | ✅ |
| archive/ | ✅ |

**不包含具体知识内容**。只建立规范和模板。

---

## Phase 2 — Memory 建设（专家长期认知）

**目标**：按 Memory-Standard 规范，逐条创建高质量专家记忆。

| 编号 | 主题 | 所属层级 | 优先级 |
|------|------|----------|--------|
| M0001 | 创作者哲学 | L1_Worldview | 🔴 高 |
| M0002 | 抖音底层逻辑 | L1_Worldview | 🔴 高 |
| M0003 | 账号定位 | L2_Strategy | 🔴 高 |
| M0004 | 账号主页 | L3_Tactics | 🟡 中 |
| M0005 | 封面设计 | L3_Tactics | 🟡 中 |
| M0006 | 标题设计 | L3_Tactics | 🟡 中 |
| M0007 | 黄金三秒 | L3_Tactics | 🔴 高 |
| M0008 | 视频导演 | L3_Tactics | 🟡 中 |
| M0009 | 拍摄方法论 | L3_Tactics | 🟢 低 |
| M0010 | 剪辑逻辑 | L3_Tactics | 🟢 低 |
| M0011 | 台词设计 | L3_Tactics | 🟡 中 |
| M0012 | 完播率 | L4_Platform | 🔴 高 |
| M0013 | 点赞机制 | L4_Platform | 🟡 中 |
| M0014 | 评论机制 | L4_Platform | 🔴 高 |
| M0015 | 关注机制 | L4_Platform | 🔴 高 |
| M0016 | IP人设 | L2_Strategy | 🟡 中 |
| M0017 | 内容系列化 | L2_Strategy | 🟢 低 |
| M0018 | 数据分析 | L4_Platform | 🟡 中 |
| M0019 | 直播逻辑 | L2_Strategy | 🟢 低 |
| M0020 | 小黄车成交 | L2_Strategy | 🟢 低 |

每一条 Memory 的标准参见 [standards/Memory-Standard.md](./standards/Memory-Standard.md)。

---

## Phase 3 — Framework 建设（分析框架）

**目标**：建立可复用的结构化分析框架。

| 框架 | 用途 |
|------|------|
| Account-Diagnosis | 账号诊断：7 维度评分卡 |
| Positioning-Validation | 定位验证：人群×痛点×差异化 |
| Topic-Decision-Tree | 选题决策树：9 问筛选 |
| Script-Evaluation | 脚本评估：钩子/信息密度/完播驱动 |
| Director-Review | 导演审查：视觉节奏/情绪曲线 |
| Editing-Quality | 剪辑质检：节奏/转场/信息效率 |
| Content-Retro | 内容复盘：数据→归因→优化 |
| Data-Dashboard | 数据看板：核心指标解读框架 |
| IP-Architecture | IP 架构：人格锚点体系 |
| Commercial-Model | 商业模型：变现路径推演 |

---

## Phase 4 — Checklist 建设（检查清单）

**目标**：将顶层认知转化为可逐项勾选的执行清单。

| Checklist | 触发时机 |
|-----------|----------|
| 拍摄前检查 | 每次拍摄前 |
| 剪辑前检查 | 开始剪辑前 |
| 发布前检查 | 点击发布前 |
| 主页检查 | 账号装修后 |
| 周复盘检查 | 每周日 |
| 月复盘检查 | 每月末 |

---

## Phase 5 — Skills 建设（执行能力）

**目标**：构建可被 Agent 调用的 Skill。

Skills 设计原则：
- 不直接依赖 LLM
- 优先调用 Memory → Framework → Checklist
- LLM 只负责组织最终语言

---

## Phase 6 — Adapter 接入

**目标**：将知识工程接入 Hermes / LangGraph / Claude Code / OpenManus 等 Agent 框架。

---

## 推进方式

每次推进以 **GitHub Commit** 为单位：
- Commit 1：项目骨架 ✅（当前）
- Commit 2：Memory Standard 规范
- Commit 3：Skills Standard 规范
- Commit 4：M0001 创作者哲学
- Commit 5：M0002 抖音底层逻辑
- ……

每完成一个 Commit，同步更新本文件。
