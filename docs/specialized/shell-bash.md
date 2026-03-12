# Shell / Bash 专用版

这份文档适合 Shell、Bash、Linux 命令行脚本、批处理任务、cron、运维脚本和 CLI 封装场景。

---

## 1. 安全脚本实现版
**用途**：让 AI 写 Shell 时不再只顾能跑，要兼顾健壮性和可维护性。  
**适合**：新脚本、部署脚本、日常自动化任务。

```text
Write this shell script like a senior engineer, not like a quick command dump.

Prioritize:
- correctness,
- idempotency,
- safe defaults,
- quoting and escaping,
- error handling,
- input validation,
- logging,
- maintainability.

Do not rely on fragile one-liners if a clearer multi-step script is safer.
```

## 2. Shell 排障根因版
**用途**：脚本报错、变量不对、管道结果异常时很好用。  
**适合**：bash 报错、set -e 行为异常、环境变量问题。

```text
Debug this shell script systematically.

Do not patch around the visible failure.
Check quoting, word splitting, subshell behavior, exit-code propagation, pipeline semantics, environment assumptions, file permissions, and shell compatibility.

Explain the likely root cause first, then implement the cleanest fix.
```

## 3. 可移植性与兼容性版
**用途**：需要兼顾不同 Linux 发行版、不同 shell 环境。  
**适合**：CI 脚本、服务器脚本、跨环境脚本。

```text
Review this script from a portability and compatibility perspective.

Check whether it depends on:
- Bash-only features,
- GNU-specific flags,
- locale assumptions,
- filesystem layout assumptions,
- interactive shell behavior,
- environment-specific commands.

Prefer a robust and predictable approach that behaves well across target environments.
```

## 4. 批处理与目录操作版
**用途**：文件批量处理、日志归档、重命名、打包、清理任务。  
**适合**：日常自动化、运维巡检、批量操作。

```text
Design this shell automation for batch processing safely.

Do not optimize only for fewer lines.
Consider:
- spaces and special characters in file names,
- partial failure handling,
- resumability,
- dry-run support,
- logging,
- destructive-action safeguards.

Prefer a script that is safe to run repeatedly in real environments.
```

## 5. Cron / 定时任务版
**用途**：让 AI 设计周期任务时考虑环境差异、日志和失败恢复。  
**适合**：cron、systemd timer、定时清理、定时报表。

```text
Treat this as a production scheduled-job design task.

Do not assume cron will run with the same environment as an interactive shell.
Check path assumptions, environment variables, locking, overlapping runs, logging, alerting, and retry behavior.

Design a scheduled execution flow that is observable, safe, and repeatable.
```

## 6. Shell 重构版
**用途**：旧脚本越来越乱时，要求 AI 按函数化和职责拆分思路重构。  
**适合**：历史脚本、长脚本、多人维护脚本。

```text
Refactor this shell script like a maintainability-focused engineer.

Evaluate whether the current structure is readable, testable, and safe to modify.
If the script is becoming a pile of commands, reorganize it into clear functions, explicit variables, and well-defined execution steps.

Do not preserve a fragile structure just to minimize edits.
```

## 7. Shell 代码评审版
**用途**：审脚本风险点、删除危险操作、发现隐患。  
**适合**：上线前 review、生产脚本 review。

```text
Review this shell script critically for production risk.

Focus on:
- destructive operations,
- unquoted variables,
- hidden assumptions,
- race conditions,
- missing validation,
- unsafe temp file handling,
- privilege and permission risks,
- rollback limitations.

For each important issue, explain why it matters and propose a safer implementation.
```
