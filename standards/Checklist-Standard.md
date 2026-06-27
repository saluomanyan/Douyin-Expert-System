# Checklist Standard

> Hermes 操作检查清单设计规范

---

## 一、Checklist 是什么

Checklist 是**可执行的操作审核标准**——不是"建议"，而是"在 XX 之前必须逐项打勾"的清单。

每条 Checklist 条目必须：
- 是/否 可判断
- 有明确的检查点
- 引用相关 Memory（说明为什么）

---

## 二、Checklist 模板

```markdown
---
checklist_id: {阶段-检查类型}
name: {中文名称}
version: 1.0
stage: {Before-Shooting | Before-Editing | Before-Publishing | Homepage | Weekly-Review | Monthly-Review}
description: {一句话描述}
created: YYYY-MM-DD
---

# {检查清单名称}

## 使用时机

{什么时候执行这个清单}

## 检查项

### 一、{类别}

- [ ] **{检查点}** — 引用：[M-XXX](...)
- [ ] **{检查点}** — 引用：[M-YYY](...)

### 二、{类别}

- [ ] **{检查点}**
...
```

---

## 三、计划的 Checklist 列表

| ID | 名称 | 阶段 |
|----|------|------|
| before-shooting | 拍摄前检查 | Before-Shooting |
| before-editing | 剪辑前检查 | Before-Editing |
| before-publishing | 发布前检查 | Before-Publishing |
| homepage-review | 主页审查 | Homepage |
| cover-review | 封面审查 | Before-Publishing |
| title-review | 标题审查 | Before-Publishing |
| weekly-content | 周度内容复盘 | Weekly-Review |
| monthly-growth | 月度增长复盘 | Monthly-Review |
