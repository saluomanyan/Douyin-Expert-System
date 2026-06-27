# Framework Standard · 分析框架规范

> 定义 Hermes-Douyin-Expert-System 中每个分析框架的标准格式。

---

## Framework 是什么

Framework 是**结构化的分析/决策模型**。

它告诉 Agent：当面对一个问题时，应该按什么逻辑去推演。

---

## Framework 标准格式

```yaml
---
id: fw-001
name: "选题决策树"
description: "拿到一个选题后的 9 步推演流程"
category: "Topic"
version: 1
last_updated: 2026-06-27
---
```

### 内容结构

1. **触发条件** — 什么情况下使用这个 Framework
2. **输入** — 需要什么信息
3. **推演步骤** — 逐步决策流程（决策树格式）
4. **输出** — 最终给出什么结论
5. **关联** — 引用哪些 Memory / Checklist

---

## Framework 示例结构

```markdown
# 选题决策树

## 触发条件
用户提出一个内容选题时。

## 输入
- 选题描述
- 目标人群
- 账号定位

## 推演步骤

### Q1: 这个东西有人搜吗？
→ 没有人搜 → 不建议（除非你有极强的制造需求能力）
→ 有人搜 → 继续

### Q2: 用户为什么看？
→ 没有明确理由 → 不建议
→ 有明确利益/情绪价值 → 继续

### Q3: 为什么现在看？
→ 没有时效性/紧迫性 → 降低优先级
→ 有 → 继续

（继续 Q4-Q9……）

## 输出
- 结论：建议做 / 不建议做 / 可以做但需修改
- 理由：逐条说明
- 建议方向：如果不做这个，做什么
```

---

## Framework 分类

| 类别 | 目录 | 示例 |
|------|------|------|
| Account | framework/Account/ | 账号诊断框架 |
| Positioning | framework/Positioning/ | 定位验证框架 |
| Topic | framework/Topic/ | 选题决策树 |
| Script | framework/Script/ | 脚本评估框架 |
| Director | framework/Director/ | 导演审查框架 |
| Editing | framework/Editing/ | 剪辑质检框架 |
| Review | framework/Review/ | 内容复盘框架 |
| Data | framework/Data/ | 数据分析框架 |
| IP | framework/IP/ | IP 架构框架 |

---

## 设计原则

- 必须是**决策树/流程图**式的推演，不是散文
- 每一步都是**二选一或多选一的判断**
- **必须有明确结论**，不能以"视情况而定"结束
