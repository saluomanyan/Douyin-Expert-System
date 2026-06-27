# Citation Standard · 引用规范

> 定义 Hermes-Douyin-Expert-System 中的引用和来源标注标准。

---

## 来源类型

| 类型 | 代码 | 可信度基准 | 示例 |
|------|------|-----------|------|
| 官方文档 | `official` | 高 | 抖音创作者学院、抖音规则中心 |
| 行业报告 | `report` | 高 | 艾瑞、QuestMobile、飞瓜 |
| 书籍 | `book` | 中-高 | 出版书籍 |
| 课程 | `course` | 中 | 混沌、得到、三节课 |
| 访谈 | `interview` | 中 | 播客、视频访谈 |
| 文章 | `article` | 中-低 | 公众号、知乎、即刻 |
| 社区 | `community` | 低 | 生财有术、知识星球 |
| MCN内部 | `mcn_internal` | 高 | MCN 培训手册（需脱敏） |
| 个人经验 | `personal` | 低 | 操盘手个人分享 |

---

## 来源标注格式

每条 Memory / Knowledge 中的来源标注：

```yaml
sources:
  - name: "抖音创作者学院 — 起号入门指南"
    type: official
    url: "https://..."
    access_date: 2026-06-27
    note: "第3章：账号定位篇"
    confidence_contribution: high
```

---

## 交叉验证记录

当一条 Memory 通过交叉验证后，在 Memory 文件中记录：

```markdown
## 交叉验证

| 来源 | 类型 | 观点一致性 |
|------|------|-----------|
| 抖音创作者学院 | official | ✅ 一致 |
| 《抖音运营实战》第4章 | book | ✅ 一致 |
| 某MCN培训手册 | mcn_internal | ✅ 一致 |
| 某操盘手播客 | interview | ⚠️ 部分一致（强调侧重不同） |

验证结论：**3/4 来源一致，可信度高。** 分歧点为侧重点差异，不影响核心认知。
```

---

## 不可引用来源

- 匿名来源（无法追溯）
- 已被官方辟谣的信息
- 明显过时的信息（抖音规则变动频繁，超过 2 年的非底层原则类信息需标注时效性风险）
