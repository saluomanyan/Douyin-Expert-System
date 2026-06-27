# Knowledge Standard · 知识提炼规范

> 定义 Hermes-Douyin-Expert-System 中每条 Knowledge 条目的标准格式。

---

## Knowledge 是什么

Knowledge 是**从原始资料中提炼的结构化知识**。

它是 Memory 的上游——原始资料经过整理、去噪、结构化后形成 Knowledge，再进一步蒸馏为 Memory。

---

## Knowledge 条目标准格式

```yaml
---
id: kn-001
title: "抖音创作者学院 2024 核心要点"
source_type: "official"
source_name: "抖音创作者学院"
source_url: "https://..."
date_collected: 2026-06-27
extracted_by: "AI"
reviewed_by: "待审核"
status: draft
tags: [官方, 创作者学院, 2024]
---
```

---

## 内容结构

1. **来源信息** — 出处、日期、作者、可信度
2. **核心摘要** — 500 字以内，提取最核心的观点
3. **关键引用** — 原文中最重要的 3-5 句直接引用
4. **潜在 Memory 候选** — 哪些观点有潜力蒸馏为 Memory
5. **相关条目** — 关联的其他 Knowledge 条目

---

## 与 Memory 的区别

| | Knowledge | Memory |
|---|----------|--------|
| 定位 | 知识提炼 | 专家认知 |
| 密度 | 中（保留上下文） | 高（只留核心） |
| 长度 | 500-2000 字 | 300-500 字 |
| 来源标注 | 单源 | 多源交叉验证 |
| 可操作性 | 中等 | 极高 |
| 谁维护 | AI 提炼 + 人审核 | AI 蒸馏 + 人修改 |

---

## Knowledge 分类

| 类别 | 目录 | 来源类型 |
|------|------|----------|
| Official | knowledge/Official/ | 抖音官方文档/公告 |
| Reports | knowledge/Reports/ | 行业报告/白皮书 |
| Books | knowledge/Books/ | 书籍 |
| Courses | knowledge/Courses/ | 课程/培训 |
| Interviews | knowledge/Interviews/ | 访谈/播客 |
| Community | knowledge/Community/ | 社区精华帖 |
| Case-Studies | knowledge/Case-Studies/ | 案例分析 |
