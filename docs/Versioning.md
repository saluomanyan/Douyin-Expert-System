# Versioning

> 版本号策略

---

## 语义化版本

采用 [Semantic Versioning](https://semver.org/)：`MAJOR.MINOR.PATCH`

- **MAJOR**：架构重构、核心原则变更、不兼容的改动
- **MINOR**：新增 Memory/Skill/Framework/Checklist，向后兼容
- **PATCH**：修正错误、优化措辞、更新元数据

---

## 当前版本

**v0.1.0** — 工程骨架

---

## Memory 版本独立管理

每条 Memory 内部有自己的版本号（如 `v1.2`），独立于项目版本：

```markdown
---
memory_id: M-001
version: 1.2
last_updated: 2026-06-27
---
```

- `1.x`：内容质量迭代（措辞优化、补充案例）
- `2.0+`：认知升级（推翻重写）
- L1 级别 Memory 版本升级需要特别审批

---

## 版本对应阶段

| 版本 | 阶段 | 内容 |
|------|------|------|
| v0.1.x | Phase 1 | 工程骨架 |
| v0.2.x | Phase 2 | 首批 Memory (L1+L2) |
| v0.3.x | Phase 2 | Memory 扩充 (L3) |
| v0.4.x | Phase 3+4 | Framework + Checklist |
| v0.5.x | Phase 5 | Skills |
| v1.0.0 | Phase 6 | Agent 适配器 + 正式发布 |
