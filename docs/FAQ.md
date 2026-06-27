# FAQ · 常见问题

---

### Q: 这个项目和普通的"抖音运营教程"有什么区别？

A: 这不是教程。这是**可以被 AI Agent 加载为长期记忆的专家认知库**。

- 教程告诉你怎么做
- 认知系统告诉 Agent 为什么这样做，并进行逻辑推演

---

### Q: 为什么叫 Hermes-Douyin-Expert-System 而不是 Douyin-Prompts？

A: 因为目标是建立一个**知识系统**，不只是 Prompt 合集。

Hermes 是默认适配的 Agent 框架，但整个知识工程独立于任何特定 Agent。

---

### Q: 我现在就能用吗？

A: Phase 1 是项目骨架，还没有具体知识内容。Memory 将从 Phase 2 开始建设。

你现在可以：
- 阅读 [README.md](../README.md) 了解项目愿景
- 阅读 [ROADMAP.md](../ROADMAP.md) 了解建设计划
- 按照 [INSTALL.md](../INSTALL.md) 准备接入环境

---

### Q: 如何贡献？

A: 见 [CONTRIBUTING.md](../CONTRIBUTING.md)。

---

### Q: 知识来源是什么？

A: 抖音官方文档、行业报告、顶级操盘手的公开分享、MCN 培训资料、案例研究等。

所有进入 Memory 的知识都经过交叉验证（至少 3 个来源）和人工审核。

---

### Q: 支持哪些 Agent 框架？

A: 本系统不绑定任何框架。通过 `adapter/` 目录适配：

- Hermes Agent（默认）
- LangGraph
- Claude Code
- OpenManus
- 未来更多……
