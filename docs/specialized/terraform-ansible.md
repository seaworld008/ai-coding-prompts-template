# Terraform / Ansible 专用版

这份文档适合 Terraform、Ansible、模块设计、状态管理、环境分层、基础设施变更和配置编排任务。

---

## 1. IaC 结构设计版
**用途**：让 AI 从结构、职责和环境边界设计 IaC，而不是直接堆资源块。  
**适合**：新建 Terraform 项目、整理 Ansible 目录、模块拆分。

```text
Treat this as an infrastructure-as-code architecture task, not as a text-editing request.

Before writing or changing code, assess:
- module boundaries,
- environment separation,
- variable design,
- reuse strategy,
- state implications,
- secret handling,
- maintainability,
- operational safety.

Prefer a clean, explicit, long-term maintainable IaC structure over a quick configuration dump.
```

## 2. Terraform plan 审核版
**用途**：专门让 AI 帮你看 plan 是否安全、语义是否正确。  
**适合**：资源变更 review、上线前审查、风险评估。

```text
Review this Terraform change like an engineer responsible for production infrastructure.

Do not stop at syntax validity.
Evaluate whether the plan is semantically correct, safe to apply, and aligned with good Terraform practices.

Focus on:
- destructive changes,
- state implications,
- dependency ordering,
- variable correctness,
- drift indicators,
- module assumptions,
- rollback practicality.
```

## 3. Terraform 状态与漂移排障版
**用途**：state 混乱、drift、import、资源替换异常时很有用。  
**适合**：plan 不符合预期、重复创建、漂移治理。

```text
Debug this Terraform issue systematically.

Do not assume the visible diff is the true root cause.
Check:
- state correctness,
- drift,
- imports,
- lifecycle rules,
- provider behavior,
- environment-specific inputs,
- implicit dependencies,
- unintended replacements.

Explain the likely root cause first, then propose the safest corrective action.
```

## 4. Ansible Playbook 设计版
**用途**：让 AI 写 playbook 时考虑幂等性、角色拆分和可维护性。  
**适合**：配置编排、批量部署、主机初始化、运维自动化。

```text
Design this Ansible automation like an engineer responsible for repeatable operations.

Prioritize:
- idempotency,
- role structure,
- variable hygiene,
- host targeting,
- privilege boundaries,
- error handling,
- maintainability,
- operational clarity.

Do not write a playbook that only works once in a perfect environment.
```

## 5. Ansible 排障与执行安全版
**用途**：playbook 执行失败、变量覆盖异常、权限或 inventory 问题。  
**适合**：运行报错、行为异常、部分主机失败。

```text
Debug this Ansible issue systematically.

Check:
- inventory targeting,
- variable precedence,
- privilege escalation,
- module assumptions,
- idempotency behavior,
- host-specific drift,
- task ordering,
- rollback practicality.

Do not patch around failing tasks without understanding the real execution model.
```

## 6. 基础设施变更安全版
**用途**：让 AI 在设计 IaC 变更时兼顾执行窗口、影响范围和回滚策略。  
**适合**：生产变更、平台重构、大规模配置调整。

```text
Review this infrastructure change from a change-management and operational safety perspective.

Consider:
- blast radius,
- sequencing,
- rollback feasibility,
- dependency coupling,
- state or inventory consistency,
- environment isolation,
- approval requirements,
- post-change verification.

Prefer a rollout plan that is explicit, reversible, and production-safe.
```

## 7. IaC 文档 / Runbook 版
**用途**：输出可执行的 IaC 使用说明、变更 SOP 和排障手册。  
**适合**：内部平台文档、交付文档、团队手册。

```text
Write this as a practical infrastructure-as-code runbook.

Include:
- purpose,
- prerequisites,
- environment assumptions,
- plan or dry-run steps,
- apply steps,
- verification guidance,
- rollback or recovery considerations,
- common troubleshooting notes.
```
