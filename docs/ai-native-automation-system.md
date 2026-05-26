# AI 原生个人事业收束自动化系统

本文档用于把“个人事业收束系统”进一步自动化，让长期主线、每周复盘、选题、作品沉淀、Demo 路线和 GitHub 公开资产形成闭环。

---

## 1. 自动化目标

核心目标不是替代思考，而是减少启动成本，让系统自动推动自己运转。

最终形成以下飞轮：

```text
观察输入
  ↓
自动生成每周复盘 Issue
  ↓
人工补充观察与想法
  ↓
AI 辅助收束为选题 / Demo / 架构图
  ↓
沉淀到 docs / projects / roadmap
  ↓
公开积累
  ↓
形成长期个人标签
```

---

## 2. 推荐工具栈

### 2.1 GitHub Repository

用途：长期公开资产中心。

承载内容：

- 长期主线文档
- 每周复盘 Issue
- 项目 Roadmap
- Agent 设计文档
- Demo 原型
- 架构图
- 公开文章

---

### 2.2 GitHub Issues

用途：把“想法”变成可追踪任务。

建议 Issue 类型：

- `weekly-review`：每周复盘
- `idea`：灵感池
- `article`：文章选题
- `demo`：Demo 原型
- `architecture`：架构图
- `roadmap`：季度路线

---

### 2.3 GitHub Actions

用途：自动创建周期性任务。

第一阶段先实现：

- 每周自动创建复盘 Issue
- 每月自动创建路线检查 Issue

后续可扩展：

- 自动汇总未完成 Issue
- 自动生成周报草稿
- 自动检查 docs 是否更新
- 自动生成 Roadmap 看板

---

### 2.4 AGENTS.md

用途：给 AI Coding Agent 提供仓库级上下文。

它告诉未来的 Codex / Claude Code / Cursor / Copilot Agent：

- 这个仓库的长期目标是什么
- 文档应该怎么写
- Issue 应该如何分类
- 不应该偏离哪些主线
- 每次改动应该如何服务长期身份

---

### 2.5 AI Coding Agent

推荐使用方式：

- 用 Codex / Claude Code / Cursor 处理文档整理、脚本生成、Issue 总结
- 用 GitHub Copilot 辅助日常编辑
- 用本仓库的 AGENTS.md 约束 Agent 行为

Agent 不负责替你决定人生方向，只负责降低执行成本。

---

## 3. 当前已实现的最小系统

本仓库将包含：

```text
AGENTS.md
.github/
  ISSUE_TEMPLATE/
    weekly-review.md
    idea.md
    article.md
  workflows/
    weekly-review.yml
    monthly-roadmap.yml
docs/
  ai-native-career-system.md
  ai-native-automation-system.md
roadmap/
  2026-roadmap.md
```

---

## 4. 每周自动化流程

### 每周一：自动创建 Weekly Review Issue

Issue 会提示你填写：

- 本周观察到的 AI / Agent / 研发趋势
- 本周最值得收束的一个主题
- 本周要产出的作品
- 本周最小行动
- 是否需要生成文章 / Demo / 架构图

### 每周中：人工补充输入

你只需要把碎片想法丢进 Issue。

### 每周末：AI 辅助整理

让 AI 基于 Issue 内容输出：

- 一篇文章草稿
- 一个 Demo 任务拆解
- 一个架构图说明
- 一个下周计划

---

## 5. 每月自动化流程

### 每月 1 日：自动创建 Roadmap Review Issue

检查：

- 本月是否围绕主线
- 是否有公开作品
- 是否有 Demo 进展
- 是否有偏离主题
- 下月主攻方向是什么

---

## 6. 标签体系

建议使用以下标签：

```text
weekly-review
idea
article
demo
architecture
roadmap
agent
ai-native-dev
```

---

## 7. 后续增强方向

### 阶段 1：自动建任务

已实现：

- Weekly Review Issue
- Monthly Roadmap Issue
- Issue 模板
- Agent 仓库说明

### 阶段 2：自动生成内容

可继续加入：

- scripts/generate-weekly-summary.py
- 从 Issue 自动生成周报 Markdown
- 从 idea Issue 自动生成文章草稿

### 阶段 3：自动维护作品集

可继续加入：

- 自动更新 README
- 自动汇总文章列表
- 自动汇总 Demo 进展
- 自动生成季度复盘

### 阶段 4：Agent 化

可继续加入：

- Terminal Agent
- API Debug Agent
- Fault Diagnosis Agent
- Personal Strategy Agent

---

## 8. 使用原则

1. 所有想法都进入 Issue。
2. 所有 Issue 最终必须导向文章、架构图或 Demo。
3. 每周只收束一个主主题。
4. 公开输出服务于长期身份：AI × 软件研发 × Agent × 工具链。
5. 自动化只负责推动流程，不替代判断。
