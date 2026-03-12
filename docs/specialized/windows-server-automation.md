# Windows Server 自动化专用版

这份文档适合 Windows Server、PowerShell、IIS、任务计划程序、服务管理、文件分发和常见运维自动化任务。

---

## 1. PowerShell 生产脚本版
**用途**：让 AI 写 PowerShell 时兼顾错误处理、幂等性和可维护性。  
**适合**：自动化脚本、巡检脚本、部署脚本。

```text
Write this PowerShell automation like a production engineer.

Prioritize:
- correctness,
- idempotency,
- explicit error handling,
- parameter validation,
- logging,
- maintainability,
- safe execution defaults.

Do not produce a brittle admin-only quick script unless explicitly requested.
```

## 2. Windows 服务 / IIS 配置版
**用途**：IIS、Windows Service、应用池、站点部署和配置变更。  
**适合**：站点发布、服务重启、应用池调整。

```text
Treat this as a Windows Server production operations task.

Before making changes, assess whether the requested approach is safe, maintainable, and aligned with common Windows administration conventions.

Focus on:
- service lifecycle,
- IIS site and app pool behavior,
- permissions,
- configuration consistency,
- restart impact,
- rollback feasibility,
- logging and diagnostics.
```

## 3. 任务计划程序设计版
**用途**：定时执行 PowerShell、批处理、备份和清理任务时很好用。  
**适合**：Task Scheduler、定时脚本、夜间任务。

```text
Design this Windows scheduled task for reliable unattended execution.

Do not assume the interactive user context will exist.
Evaluate:
- execution identity,
- permissions,
- working directory,
- environment assumptions,
- overlap prevention,
- logging,
- retry and failure visibility.

Prefer a scheduled task setup that is explicit, observable, and safe to maintain.
```

## 4. Windows 排障根因版
**用途**：脚本不生效、任务失败、服务异常、权限问题时。  
**适合**：PowerShell 报错、服务起不来、IIS 行为异常。

```text
Debug this Windows Server issue systematically.

Do not patch around symptoms.
Determine whether the root cause is related to permissions, service state, execution policy, path assumptions, environment context, scheduled-task identity, IIS configuration, or dependency failure.

Explain the most likely root cause first, then propose the cleanest corrective action.
```

## 5. 权限与安全版
**用途**：脚本权限、服务账号、共享目录访问、安全基线检查。  
**适合**：生产服务器治理、安全 review。

```text
Review this Windows Server automation from a security and least-privilege perspective.

Focus on:
- service accounts,
- local and domain permissions,
- credential handling,
- script signing or execution policy assumptions,
- SMB/share exposure,
- registry and filesystem access,
- auditability.

Challenge insecure convenience shortcuts and recommend secure professional defaults.
```

## 6. Runbook / 运维手册版
**用途**：写 Windows 运维操作步骤、发布 SOP 和故障手册。  
**适合**：值班手册、交接文档、标准操作流程。

```text
Write this as a Windows Server operational runbook.

Include:
- purpose and scope,
- prerequisites,
- exact PowerShell or GUI-equivalent steps where relevant,
- expected results,
- validation steps,
- rollback or recovery guidance,
- warnings for risky operations such as service restarts or IIS binding changes.
```
