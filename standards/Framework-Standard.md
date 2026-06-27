# Framework Standard

> Hermes 分析框架设计规范

---

## 一、Framework 是什么

Framework 是**结构化的分析方法论**。

它定义了分析某个问题时的固定思考路径。不是让 AI 自由发挥，而是按既定框架推演。

---

## 二、Framework 模板

```markdown
---
framework_id: {领域-分析类型}
name: {中文名称}
version: 1.0
category: {Account | Positioning | Topic | Script | Director | Editing | Review | Data | IP}
description: {一句话描述}
referenced_memory:
  - M-XXX
  - M-YYY
created: YYYY-MM-DD
last_updated: YYYY-MM-DD
---

# {框架名称}

## 适用场景

{什么时候用这个框架}

## 分析步骤

### Step 1：{步骤名称}

{具体分析的问题和方法}

### Step 2：{步骤名称}

...

## 输出格式

{定义分析结果的结构}
```

---

## 三、计划的 Framework 列表

| ID | 名称 | 说明 |
|----|------|------|
| account-diagnosis | 账号诊断框架 | 系统评估账号健康状况 |
| positioning | 定位分析框架 | 验证和优化账号定位 |
| topic-validation | 选题决策框架 | 判断选题是否值得拍 |
| hook-design | 钩子设计框架 | 黄金三秒钩子设计方法 |
| script-structure | 脚本结构框架 | 视频脚本的标准结构 |
| director-planning | 导演规划框架 | 镜头设计与节奏规划 |
| editing-review | 剪辑审核框架 | 剪辑质量评估标准 |
| data-review | 数据复盘框架 | 视频发布后数据回顾 |
| ip-growth | IP 成长框架 | 长期 IP 建设路径评估 |
| commercial-fit | 商业适配框架 | 变现方式与账号匹配度 |
