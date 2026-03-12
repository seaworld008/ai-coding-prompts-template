# CI/CD / GitHub Actions 专用版

这份文档适合 CI/CD 流水线、GitHub Actions、构建发布、测试门禁、制品流转、密钥管理和发布回滚场景。

---

## 1. 流水线方案设计版
**用途**：让 AI 先把 pipeline 设计清楚，而不是上来就拼 YAML。  
**适合**：新建流水线、重构现有 CI/CD、发布流程设计。

```text
Design this CI/CD pipeline like an engineer responsible for real software delivery.

Before writing workflow files, think through:
- validation stages,
- build artifacts,
- deployment boundaries,
- approval gates,
- rollback strategy,
- secret handling,
- environment separation,
- observability.

Do not jump straight to YAML.
Prefer a pipeline design that is reliable, maintainable, and operationally safe.
```

## 2. GitHub Actions YAML 审视版
**用途**：专门看 workflow 结构、job 依赖、触发条件和可维护性。  
**适合**：Actions workflow review、触发逻辑优化、矩阵任务设计。

```text
Treat this as a GitHub Actions workflow design review, not as a simple YAML edit.

Evaluate:
- trigger correctness,
- job dependencies,
- matrix strategy,
- caching,
- artifact passing,
- secret usage,
- concurrency control,
- reusability,
- maintainability.

If the workflow structure is flawed, redesign the workflow logic rather than patching a broken job graph.
```

## 3. 失败流水线排障版
**用途**：CI 反复失败、某一步骤抖动、环境不一致时很好用。  
**适合**：构建失败、测试失败、部署失败、偶发 flaky workflow。

```text
Debug this CI/CD failure systematically.

Do not treat the final failed step as the only problem.
Check:
- dependency installation,
- cache correctness,
- environment drift,
- secret and permission issues,
- artifact availability,
- path assumptions,
- shell behavior,
- external service dependencies,
- flaky test or runner conditions.

Identify the root cause first, then propose the most reliable fix.
```

## 4. 发布安全与回滚版
**用途**：让 AI 设计发布步骤时考虑制品一致性、审批门禁和回滚。  
**适合**：生产发布、preview deployment、多环境部署。

```text
Review this deployment workflow from a release safety perspective.

Focus on:
- artifact immutability,
- environment promotion,
- approval gates,
- rollback strategy,
- failure isolation,
- partial deployment risk,
- secret exposure,
- post-deploy verification.

Prefer a deployment process that is reversible, observable, and safe under failure.
```

## 5. Secrets / 权限治理版
**用途**：GitHub Actions 里最容易出坑的就是 secrets、token scopes 和权限过大。  
**适合**：workflow 权限 review、OIDC、部署密钥、组织级安全治理。

```text
Review this CI/CD setup from a secrets and permissions perspective.

Check:
- token scopes,
- secrets exposure,
- reusable workflow boundaries,
- environment protection rules,
- OIDC usage,
- third-party action trust,
- permission minimization,
- auditability.

Challenge convenience-based insecure defaults and recommend secure professional defaults.
```

## 6. 构建效率与稳定性优化版
**用途**：让 AI 不只会修失败，还能优化慢、重复、抖动的流水线。  
**适合**：慢构建、重复 job、缓存效率差。

```text
Analyze this CI/CD workflow from an efficiency and reliability perspective.

Do not optimize only for a green run.
Consider:
- cache hit rate,
- duplicated work,
- parallelization opportunities,
- artifact reuse,
- matrix explosion,
- retry boundaries,
- flaky step isolation,
- maintenance cost.

Recommend improvements that reduce pipeline time without making the workflow fragile.
```

## 7. CI/CD Runbook 版
**用途**：写发布操作手册、回滚说明、流水线维护文档。  
**适合**：值班手册、平台文档、交接资料。

```text
Write this as a CI/CD operational runbook.

Include:
- purpose and scope,
- trigger conditions,
- step-by-step execution flow,
- required approvals,
- expected outputs,
- verification steps,
- rollback or recovery procedure,
- warnings for risky operations such as production deploys.
```
