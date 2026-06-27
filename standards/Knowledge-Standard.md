# Knowledge Standard

> 提炼后的知识设计规范

---

## 一、Knowledge 是什么

Knowledge 是**经过整理和摘要的知识**——介于原始资料（Repository）和专家记忆（Memory）之间。

它已经去除了噪音、提取了要点，但**尚未通过 6 条铁律的全面审核**，还不能进入 Memory。

---

## 二、Knowledge 的生命周期

```
Repository（原始资料）
    ↓ 阅读 + 提炼
Knowledge（经过摘要）
    ↓ 多源验证 + 人工审核
Memory（专家认知）
```

---

## 三、Knowledge 模板

```markdown
---
knowledge_id: K-XXX
title: {标题}
source_type: {Official | Report | Book | Course | Interview | Podcast | Community | Case-Study}
source_url: {原文链接}
source_author: {作者/机构}
source_date: YYYY-MM-DD
extracted_by: {提取人}
extracted_date: YYYY-MM-DD
tags: [tag1, tag2]
---

# {标题}

## 来源

{原始出处信息}

## 核心要点

{提取的关键知识点}

## 潜在 Memory 候选

{哪些点可能值得进一步验证并进入 Memory？}

## 待验证

{哪些点需要更多来源验证？}
```

---

## 四、Knowledge 目录结构

```
knowledge/
├── Official/         ← 官方资料（抖音创作者学院等）
├── Reports/          ← 行业报告
├── Books/            ← 书籍笔记
├── Courses/          ← 课程笔记
├── Interviews/       ← 操盘手访谈
├── Podcasts/         ← 播客笔记
├── Community/        ← 社区精华（即刻/生财有术等）
└── Case-Studies/     ← 案例分析
```
