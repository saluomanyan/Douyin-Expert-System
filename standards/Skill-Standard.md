# Skill Standard

> Hermes Skills 设计规范

---

## 一、Skill 是什么

Skill 是 Hermes Agent 的**执行能力**。

一个 Skill 定义了一个具体任务的工作流程：它知道该读取哪些 Memory、应用哪个 Framework、对照哪份 Checklist，最后让 LLM 组织语言输出。

**Skill 不做决策。决策依据全部来自 Memory。**

---

## 二、Skill 与 Memory 的关系

```
Memory = 知道什么是对的（决策认知）
Skill  = 会做什么事（执行能力）
```

Skill 的工作流程：

```
用户请求
    ↓
Skill 匹配（判断任务类型）
    ↓
读取相关 Memory（获取专家认知）
    ↓
应用 Framework（结构化分析）
    ↓
对照 Checklist（逐项审核）
    ↓
LLM 组织语言输出
```

---

## 三、Skill 文件格式

### 文件名

```
{领域}_{功能}.skill.md

示例：
Account_Diagnosis.skill.md
Script_Generate.skill.md
```

### 文件内容模板

```markdown
---
skill_id: {领域-功能}
name: {中文名称}
version: 1.0
category: {Account | Content | Script | Director | Shooting | Editing | Algorithm | Growth | Commercial}
trigger: {触发条件描述}
required_memory:
  - M-XXX  # 必须读取的 Memory
  - M-YYY
required_framework:
  - {Framework 名称}
required_checklist:
  - {Checklist 名称}
created: YYYY-MM-DD
last_updated: YYYY-MM-DD
---

# {技能名称}

## 触发条件

{当用户说什么时触发此 Skill}

## 能力描述

{这个 Skill 能做什么}

## 工作流程

### Step 1：读取 Memory

读取以下 Memory 获取专家认知：
- M-XXX（说明用途）
- M-YYY（说明用途）

### Step 2：应用 Framework

使用 [Framework 名称](../framework/{路径}.md) 进行结构化分析。

### Step 3：对照 Checklist

参照 [Checklist 名称](../checklist/{路径}.md) 逐项检查。

### Step 4：输出

基于 Memory 认知 + Framework 结构 + Checklist 审核，由 LLM 组织最终输出。

## 输出格式

{定义输出的结构}

## 约束

- {这个 Skill 的底线，如"不得建议损害 IP 的操作"}
- {如"如果 Memory 没有覆盖，直接说不知道，不要瞎编"}

## 示例

### 输入示例

```
{用户可能的输入}
```

### 输出示例

```
{预期输出格式}
```
```

---

## 四、Skill 设计原则

1. **不做决策**：决策依据来自 Memory，Skill 只负责执行流程
2. **必须引用**：每个 Skill 必须明确列出依赖的 Memory / Framework / Checklist
3. **有底线**：当 Memory 没有覆盖时，说"不知道"，不瞎编
4. **创作者哲学优先**：任何 Skill 都必须遵守创作哲学约束

---

## 五、计划的 Skill 列表

| Skill ID | 名称 | 领域 |
|----------|------|------|
| account-diagnosis | 账号诊断 | Account |
| account-setup | 账号搭建 | Account |
| topic-selection | 选题分析 | Content |
| script-generate | 脚本生成 | Script |
| title-optimize | 标题优化 | Script |
| cover-design | 封面设计 | Content |
| hook-design | 黄金三秒设计 | Script |
| director-plan | 导演规划 | Director |
| editing-review | 剪辑审核 | Editing |
| data-analysis | 数据分析 | Algorithm |
| competitor-analysis | 竞品分析 | Growth |
| commercial-plan | 商业规划 | Commercial |
