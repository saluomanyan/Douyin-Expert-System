# INSTALL · Hermes-Douyin-Expert-System

> 如何将本知识工程接入 Hermes Agent（或其他 AI Agent 框架）。

---

## 前置条件

- 已安装 [Hermes Agent](https://hermes-agent.nousresearch.com/)（或其他 Agent 框架）
- Git

---

## 方式一：克隆到本地

```bash
git clone https://github.com/saluomanyan/Douyin-Expert-System.git
cd Douyin-Expert-System
```

---

## 方式二：作为 Hermes Skill 加载

### 2.1 直接加载 Skill

将本项目的 `skills/` 目录下的 Skill 文件复制到 Hermes 的 skills 目录：

```bash
# 复制到 Hermes skills 目录
cp -r skills/* ~/.hermes/skills/douyin-expert/
```

然后在 Hermes 会话中加载：

```
/skill douyin-expert/<skill-name>
```

### 2.2 加载 Memory 为 Hermes Memory

Hermes 支持通过 Memory 工具加载外部知识。将 `memory/` 目录下的 `.md` 文件作为知识源导入：

```bash
# 查看 Hermes 当前 memory 配置
hermes memory status

# 将 memory 文件作为上下文注入
# 具体方式取决于 Hermes 版本，参见：
# https://hermes-agent.nousresearch.com/docs/user-guide/features/memory
```

---

## 方式三：作为独立知识库使用

本知识工程**不绑定任何 Agent 框架**。你可以：

1. **直接阅读**：所有 `.md` 文件都是人类可读的
2. **接入 LangGraph**：将 Memory 条目作为 system prompt 注入
3. **接入 Claude Code**：将 Memory 文件放到 CLAUDE.md 引用的路径
4. **接入 RAG 系统**：将 `memory/` 目录作为向量化素材

---

## 目录说明

| 目录 | 用途 | 接入方式 |
|------|------|----------|
| `memory/` | 专家长期认知 | System Prompt 注入 / RAG 向量化 |
| `skills/` | 执行技能 | Agent Skill 加载 |
| `framework/` | 分析框架 | 决策时引用 |
| `checklist/` | 检查清单 | 执行前逐项核对 |
| `knowledge/` | 知识提炼 | 参考阅读 |
| `repository/` | 原始资料 | 溯源用 |
| `adapter/` | Agent 适配器 | 各框架的加载脚本/配置 |

---

## V0.1 阶段说明

当前为 **Phase 1**（项目骨架阶段），仅建立了目录结构和规范体系，**尚未包含具体知识内容**。

Memory 内容将从 Phase 2 开始按 [ROADMAP.md](./ROADMAP.md) 逐步建设。
