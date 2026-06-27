# INSTALL

> 将 Douyin-Expert-System 安装到 Hermes Agent

---

## 前置条件

- [Hermes Agent](https://hermes-agent.nousresearch.com/docs) 已安装
- Git

---

## 安装步骤

### 1. 克隆仓库

```bash
git clone https://github.com/saluomanyan/Douyin-Expert-System.git
cd Douyin-Expert-System
```

### 2. 链接到 Hermes

> ⚠️ 此步骤将在 Phase 6（v1.0）时完善。
> 当前项目处于 **v0.1 工程骨架**阶段，Memory/Skills 尚未建设完成。

预期安装方式（待验证）：

```bash
# 将 Memory 安装为 Hermes 的长期记忆
hermes memory import ./memory/

# 将 Skills 安装为 Hermes 的技能
hermes skills install ./skills/
```

---

## 目录说明

| 目录 | 用途 | 当前状态 |
|------|------|----------|
| `memory/` | 专家长期记忆（核心资产） | 🚧 建设准备中 |
| `skills/` | Hermes 可加载的执行能力 | ⬜ 待 Phase 5 |
| `framework/` | 分析框架 | ⬜ 待 Phase 3 |
| `checklist/` | 操作检查清单 | ⬜ 待 Phase 4 |
| `standards/` | 各类规范文档 | ✅ v0.1 |
| `templates/` | 文件模板 | ✅ v0.1 |

---

## 更新

```bash
git pull origin main
```
