# CHANGELOG

> 所有值得记录的变更

---

## [v0.2.0] — 2026-06-27

### Changed
- `standards/Memory-Standard.md` — 升级到 v0.2，合并 ChatGPT 第二阶段讨论的所有新增字段
  - 编号格式统一为 M0001（去掉横杠）
  - 新增字段：Priority、Status、Author、Summary、Decision、Anti-pattern、Conflict、Checklist、Update Log
  - 新增来源分级 A-E 制度
  - 新增 3 问测试（为什么/什么时候/为什么不是其它方法）
  - 新增废弃规范（Status: Deprecated，不删除）
  - 新增编号段分配（L1: M0001-M0099, L2: M0100-M0199, L3: M0200-M0999, L4: M1000-M1999）
- `templates/Memory.md` — 匹配 v0.2 新规范，含全部新字段
- `docs/Architecture.md` — 反映 MA→M→F→S 四层知识粒度
- `config/memory-index.md` — 增加 MA 索引段 + 编号段

### Added
- `standards/Memory-Atom-Standard.md` — 记忆原子（MA）设计规范（v0.1）
- `templates/Memory-Atom.md` — MA 文件模板
- `memory/atoms/` — MA 存放目录 + INDEX.md
- `docs/Second-Chat-Summary.md` — 与 ChatGPT 第二阶段讨论摘要

---

## [v0.1.0] — 2026-06-27

### Added
- 项目初始化：`Hermes-Douyin-Expert-System`
- 完整目录结构（memory/skills/framework/checklist/repository/knowledge/standards/templates/config/adapter）
- `README.md` — 项目概述
- `ROADMAP.md` — 版本路线图
- `INSTALL.md` — 安装指南
- `CHANGELOG.md` — 本文
- `CONTRIBUTING.md` — 贡献指南
- `LICENSE` — MIT
- `docs/` — 项目文档（架构、设计原则、命名规范、版本策略、FAQ）
- `standards/` — 全部规范（Memory/Skill/Framework/Checklist/Knowledge/Citation）
- `templates/` — 全部文件模板
- `config/` — 索引文件
- `prompts/` — AI 辅助 Prompt
- `docs/Chat-Summary.md` — 与 ChatGPT 讨论摘要
