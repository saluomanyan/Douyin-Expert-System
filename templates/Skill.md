---
id: skill-XXX
name: "模板：Skill 名称"
description: "这个 Skill 做什么"
category: "Account|Content|Script|Director|Shooting|Editing|Algorithm|Growth|Commercial"
inputs:
  - name: input1
    type: string
    required: true
    description: "输入参数说明"
outputs:
  - name: output1
    type: markdown
    description: "输出说明"
references:
  memory: [MXXXX, MXXXX]           # 引用的 Memory 编号
  framework: ["Framework-Name"]     # 引用的 Framework
  checklist: ["Checklist-Name"]     # 引用的 Checklist
version: 1
status: draft
last_updated: YYYY-MM-DD
---

# <Skill 名称>

## 功能描述

<一句话描述这个 Skill 完成什么任务>

## 执行流程

```
输入
  ↓
Step 1: <加载引用的 Memory>
  ↓
Step 2: <调用 Framework 分析>
  ↓
Step 3: <调用 Checklist 核对>
  ↓
Step 4: <LLM 组织语言>
  ↓
输出
```

## 输入

| 参数 | 类型 | 必填 | 说明 |
|------|------|------|------|
| input1 | string | ✅ | — |

## 输出格式

```markdown
## <输出标题>

- <输出内容>
```

## 引用说明

- **Memory**：<为什么引用这些 Memory>
- **Framework**：<为什么引用这些 Framework>
- **Checklist**：<为什么引用这些 Checklist>
