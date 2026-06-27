# CONTRIBUTING

> 欢迎贡献！本项目的目标是建立一套**高质量、可演化的抖音专家知识系统**。

---

## 核心原则

1. **知识质量优先于数量** — 一条经过交叉验证的认知 > 十条来路不明的技巧
2. **写"为什么"而非"怎么做"** — 解释底层机制，而非复述操作步骤
3. **可复用、跨赛道** — 每条知识应能迁移到不同内容领域
4. **人工审核** — AI 辅助搜集和提炼，最终由人工审核入库

---

## 如何贡献

### 贡献 Memory 条目

1. 阅读 [standards/Memory-Standard.md](./standards/Memory-Standard.md)
2. 使用 [templates/Memory.md](./templates/Memory.md) 模板
3. 确保至少有 3 个独立来源交叉验证
4. 提交 PR 到对应的 `memory/L1-L4/` 目录

### 贡献 Skill

1. 阅读 [standards/Skill-Standard.md](./standards/Skill-Standard.md)
2. 使用 [templates/Skill.md](./templates/Skill.md) 模板
3. 确保 Skill 优先调用 Memory，而非依赖 LLM 自由发挥

### 贡献 Framework / Checklist

类似流程，参见对应的 Standard 和 Template。

---

## Commit 规范

```
<type>: <描述>

# 示例
feat: 添加 M0001 创作者哲学
fix: 修正 M0007 黄金三秒的算法描述
docs: 更新 ROADMAP Phase 2 计划
chore: 补充 repository/ 原始资料索引
```

---

## 审核标准

所有 PR 必须满足：

- [ ] 内容符合对应的 Standard 规范
- [ ] 至少 3 个独立来源交叉验证（Memory 条目）
- [ ] 使用了正确的模板
- [ ] 更新了对应的 INDEX.md 索引
