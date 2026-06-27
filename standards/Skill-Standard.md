# Skill Standard · 技能规范

> 定义 Hermes-Douyin-Expert-System 中每个 Skill 的标准格式。

---

## Skill 是什么

Skill 是**可以被 Agent 加载和执行的模块化能力**。

它不同于 Memory：
- Memory 回答"知道什么"
- Skill 回答"会做什么"

---

## Skill 组成结构

每个 Skill 文件包含：

```yaml
---
id: skill-001
name: "账号诊断"
description: "对抖音账号进行7维度诊断，输出问题和优化建议"
category: "Account"
inputs:
  - name: account_url
    type: string
    required: true
    description: "抖音账号链接或ID"
outputs:
  - name: diagnosis_report
    type: markdown
    description: "诊断报告"
references:
  memory: [M0003, M0004, M0016]    # 引用的 Memory
  framework: ["Account-Diagnosis"]  # 引用的 Framework
  checklist: ["Homepage-Check"]     # 引用的 Checklist
---
```

---

## Skill 设计原则

1. **不直接依赖 LLM** — Skill 优先调用 Memory → Framework → Checklist，LLM 只组织最终语言
2. **输入输出明确** — 每个 Skill 必须有明确定义的输入参数和输出格式
3. **可独立执行** — 一个 Skill 对应一个明确的任务
4. **引用而非内嵌** — Skill 引用 Memory/Framework/Checklist，不重复写知识

---

## Skill 执行流程

```
用户输入
    ↓
Skill 加载 → 读取引用的 Memory
    ↓
调用 Framework 进行分析/判断
    ↓
调用 Checklist 逐项核对
    ↓
LLM 组织自然语言输出
    ↓
返回结果
```

---

## Skill 分类

| 类别 | 目录 | 示例 |
|------|------|------|
| Account | skills/Account/ | 账号诊断、主页优化 |
| Content | skills/Content/ | 内容策划、选题建议 |
| Script | skills/Script/ | 脚本生成、台词优化 |
| Director | skills/Director/ | 导演规划、镜头建议 |
| Shooting | skills/Shooting/ | 拍摄指导 |
| Editing | skills/Editing/ | 剪辑建议 |
| Algorithm | skills/Algorithm/ | 算法分析、流量诊断 |
| Growth | skills/Growth/ | 增长策略、起号方案 |
| Commercial | skills/Commercial/ | 变现分析、小黄车策略 |

---

## Skill 生命周期

```
Draft → Review → Published → Deprecated
```
