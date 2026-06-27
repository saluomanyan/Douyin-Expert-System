# ROADMAP

> Hermes-Douyin-Expert-System 版本路线图

---

## 总体原则

- 每个版本对应一个可交付的里程碑
- 以 Git Commit 为单位推进，不是以"模块"为单位
- **宁缺毋滥**：不追求数量，追求每条知识都经过严格审核

---

## v0.1 — 工程骨架 🚧

**目标**：建立完整的知识工程目录结构和所有规范文件。**不写任何具体知识。**

### 交付物

- [ ] `README.md` — 项目概述
- [ ] `ROADMAP.md` — 本文
- [ ] `INSTALL.md` — 安装指南
- [ ] `CHANGELOG.md` — 变更日志
- [ ] `CONTRIBUTING.md` — 贡献指南
- [ ] `LICENSE` — MIT
- [ ] `docs/` — 架构、设计原则、命名规范、版本策略、FAQ
- [ ] `standards/` — Memory/Skill/Framework/Checklist/Knowledge/Citation 规范
- [ ] `templates/` — 所有文件模板
- [ ] `config/` — 索引文件
- [ ] `prompts/` — AI 辅助 Prompt
- [ ] 所有空目录 + `.gitkeep`

---

## v0.2 — 首批 Memory（L1 世界观 + L2 战略）

**目标**：填充 10-20 条核心 Memory，建立知识质量标杆。

### 计划 Memory 列表

| 编号 | 标题 | 等级 |
|------|------|------|
| M-001 | 创作者哲学 | L1 |
| M-002 | 抖音平台底层逻辑 | L1 |
| M-003 | 推荐算法机制 | L2 |
| M-004 | 用户行为动机（停留/点赞/评论/关注/分享/收藏） | L2 |
| M-005 | 账号增长底层逻辑 | L2 |
| M-006 | IP 长期建设原则 | L2 |
| M-007 | 起号核心策略 | L2 |
| M-008 | 风景类内容创作原则 | L1 |

---

## v0.3 — Memory 扩充（L3 战术层）

**目标**：填充 30-50 条战术层 Memory。

### 计划主题

- 账号搭建（昵称、头像、简介、主页装修）
- 封面设计（锚点、信息密度、颜色、文字、人物摆放）
- 标题设计（CTR、信息结构、避坑）
- 黄金三秒（钩子类型、适用场景）
- 视频节奏（情绪曲线、信息密度、转折）
- 脚本结构（开头-中段-结尾、CTA）
- 导演知识（第一镜、镜头节奏、空镜、B-roll）
- 摄影（构图、光线、焦段、移动镜头）
- 剪辑（切点、留白、字幕、音乐）

---

## v0.4 — Framework + Checklist

**目标**：建立所有分析框架和操作检查清单。

---

## v0.5 — Skills

**目标**：建立第一批可执行 Skill。Skill 调用 Memory → Framework → Checklist，LLM 仅组织语言。

---

## v1.0 — Agent 适配器

**目标**：将知识工程接入 Hermes Agent，形成完整工作流。

---

## 远期愿景

- 800+ 条高质量 Memory
- 覆盖账号全生命周期（起号→增长→变现→维护）
- 支持多 Agent 框架（Hermes / LangGraph / ClaudeCode / OpenManus）
- 社区贡献机制
- 知识版本管理与 A/B 测试
