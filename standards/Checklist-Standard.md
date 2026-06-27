# Checklist Standard · 检查清单规范

> 定义 Hermes-Douyin-Expert-System 中每条 Checklist 的标准格式。

---

## Checklist 是什么

Checklist 是**可逐项勾选的执行审核标准**。

它把 Memory 中的认知和 Framework 中的推演，转化为"发布前/拍摄前/复盘时"逐项核对的清单。

---

## Checklist 标准格式

```yaml
---
id: cl-001
name: "发布前检查"
description: "视频发布前必须逐项核对的清单"
category: "Before-Publishing"
trigger: "每次点击发布按钮前"
version: 1
last_updated: 2026-06-27
references:
  memory: [M0005, M0006, M0007]
  framework: ["Script-Evaluation"]
---
```

### 内容结构

1. **触发时机** — 什么时候用这条 Checklist
2. **检查项** — 每条一个可勾选的 `[ ]`
3. **每项的"为什么"** — 简要说明为什么这一项重要（引用 Memory）
4. **严重程度** — 🔴 致命 / 🟡 重要 / 🟢 建议

---

## Checklist 示例结构

```markdown
# 发布前检查清单

> 触发时机：每次点击"发布"按钮前

## 封面

- [ ] 🔴 封面有明确的视觉锚点？（用户 0.5 秒内能看见什么）— M0005
- [ ] 🟡 封面文字不超过 6 个字？
- [ ] 🟡 封面和标题不重复信息？

## 标题

- [ ] 🔴 标题制造了点击理由？（而非介绍内容）— M0006
- [ ] 🟡 标题包含具体数字或结果？（提升 CTR）

## 前三秒

- [ ] 🔴 前三秒没有自我介绍/寒暄/铺垫？— M0007
- [ ] 🔴 前三秒制造了冲突/利益/反差/结果？
```

---

## Checklist 分类

| 类别 | 目录 | 触发时机 |
|------|------|----------|
| Before-Shooting | checklist/Before-Shooting/ | 每次拍摄前 |
| Before-Editing | checklist/Before-Editing/ | 开始剪辑前 |
| Before-Publishing | checklist/Before-Publishing/ | 点击发布前 |
| Homepage | checklist/Homepage/ | 账号装修后 |
| Weekly-Review | checklist/Weekly-Review/ | 每周日 |
| Monthly-Review | checklist/Monthly-Review/ | 每月末 |

---

## 设计原则

- 每一项必须**可明确判断是/否**，不允许模糊项
- 每一项必须标注**严重程度**（🔴🟡🟢）
- 每一项必须**引用来源 Memory**
- 清单不宜过长，控制在 **15-25 项**
