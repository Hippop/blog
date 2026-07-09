# Subagent 与 Skill 建设路线

本系统按五批逐步补充 Subagent 与 Skill。

## 基本边界

- Subagent：稳定角色，负责独立上下文中的分析或执行。
- Skill：可复用的方法、规范、检查清单与执行步骤。
- Harness：负责调度、状态、权限、输入产物、验证和失败路由。

## 第一批：需求形成循环

### Subagent

1. `requirement-analyst`：抽取目标、范围、角色、规则、歧义和验收候选。
2. `domain-modeler`：生成统一语言、限界上下文、聚合、实体、值对象和不变量。
3. `domain-critic`：独立审查领域模型和边界。
4. `human-decision-preparer`：把未决问题整理为结构化人工决策请求。

### Skill

1. `requirement-clarification`
2. `domain-modeling`
3. `domain-model-review`
4. `human-decision-request`
5. `loop-contract-authoring`

## 第二批：架构与行为

Subagent：`architecture-option-analyst`、`adr-author`、`behavior-designer`、`behavior-critic`。

Skill：`architecture-option-analysis`、`adr-writing`、`bdd-scenario-design`、`acceptance-coverage-review`。

## 第三批：契约与测试设计

Subagent：`contract-designer`、`contract-reviewer`、`unit-test-designer`、`api-test-designer`。

Skill：`openapi-contract-design`、`consumer-contract-design`、`unit-test-matrix`、`api-test-matrix`。

## 第四批：实现与验证

Subagent：`code-implementer`、`test-implementer`、`failure-analyzer`、`minimal-fix-agent`、`code-reviewer`。

Skill：`minimal-change-implementation`、`failure-classification`、`test-integrity-guard`、`architecture-compliance-review`。

## 第五批：构建、部署与经验沉淀

Subagent：`build-diagnoser`、`deploy-coordinator`、`runtime-verifier`、`episode-summarizer`、`skill-miner`。

Skill：`build-verification`、`safe-test-deployment`、`runtime-health-check`、`episode-reporting`、`skill-promotion-review`。

## 设计规则

1. Subagent 名称表达角色，Skill 名称表达可复用能力。
2. Reviewer 默认只读，不直接修复自己发现的问题。
3. 单次需求事实进入 Artifact，稳定方法才进入 Skill。
4. 每个 Subagent 默认只预加载少量必要 Skill。
5. Subagent 只能声明本阶段候选完成，不能声明全局完成。

下一步先完善 `requirement-analyst` 和 `requirement-clarification`。
