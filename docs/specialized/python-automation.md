# Python 自动化专用版

这份文档适合 Python 脚本自动化、文件处理、API 调用、批量任务、数据清洗、定时任务和内部工具开发。

---

## 1. 自动化方案设计版
**用途**：在动手写脚本之前，先让 AI 把任务边界、输入输出和失败恢复设计清楚。  
**适合**：新自动化任务、内部工具、批处理流水线。

```text
Design this Python automation like an engineer responsible for real-world delivery.

Before writing code, clarify:
- inputs and outputs,
- failure modes,
- retry boundaries,
- idempotency requirements,
- logging needs,
- configuration model,
- execution environment,
- operational safety.

Prefer a practical, maintainable automation design over a quick script that only works once.
```

## 2. 稳健脚本实现版
**用途**：让 AI 写出来的 Python 自动化脚本更像可维护工具，而不是一次性 demo。  
**适合**：批处理脚本、目录扫描、接口同步、巡检脚本。

```text
Implement this Python automation as a maintainable engineering tool.

Do not write a throwaway script.
Include clean structure, clear function boundaries, explicit configuration, error handling, logging, and directly usable execution flow.

Prefer readable, robust code that can be run repeatedly in production-like environments.
```

## 3. API 自动化与重试版
**用途**：调用第三方 API、内部服务、Webhook 时很有用。  
**适合**：同步脚本、拉取接口数据、批量写入。

```text
Design this Python automation for reliable API interaction.

Consider:
- timeout strategy,
- retry policy,
- rate limiting,
- pagination,
- partial failure handling,
- backoff behavior,
- idempotent writes,
- observability.

Do not assume happy-path networking.
Build for realistic API failure conditions.
```

## 4. 批量文件处理版
**用途**：目录扫描、批量重命名、格式转换、报表生成。  
**适合**：文件自动化、办公自动化、运维辅助工具。

```text
Implement this Python file-processing workflow safely and systematically.

Do not optimize only for short code.
Consider:
- encoding,
- large-file behavior,
- partial writes,
- temp-file strategy,
- duplicate handling,
- resumability,
- dry-run support,
- validation of outputs.

Prefer a workflow that is safe for repeated real-world use.
```

## 5. 定时任务与后台运行版
**用途**：长期跑的自动化、定时同步、夜间任务、守护式脚本。  
**适合**：scheduled jobs、cron、Windows Task Scheduler、服务化脚本。

```text
Treat this as a production scheduled automation task.

Do not assume the script will always run interactively.
Design for:
- non-interactive execution,
- configuration injection,
- locking or overlap prevention,
- structured logging,
- alerting hooks,
- restart safety,
- data consistency after interruptions.
```

## 6. 自动化代码评审版
**用途**：不确定脚本质量时，用它让 AI 按工程标准 review。  
**适合**：上线前 review、团队共用脚本 review。

```text
Review this Python automation code like a strict senior engineer.

Focus on:
- correctness,
- maintainability,
- failure handling,
- data integrity,
- retry safety,
- logging quality,
- configuration hygiene,
- testability.

Call out any design that is too fragile for real operational use.
```

## 7. 回归与验证版
**用途**：自动化任务改完后，让 AI 帮你设计验证和回归保护。  
**适合**：脚本升级、批处理逻辑变更、接口切换。

```text
After implementing the automation change, design meaningful verification and regression protection.

Do not stop at "the script runs".
Check:
- expected outputs,
- edge cases,
- failure recovery behavior,
- idempotent reruns,
- bad-input handling,
- logging and metrics visibility.

Prefer validation that would catch real operational regressions.
```
