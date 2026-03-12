# Docker / Compose 专用版

这份文档适合 Dockerfile、Docker Compose、镜像构建、容器运行、环境变量、网络、卷挂载和交付流程相关任务。

---

## 1. Dockerfile 生产设计版
**用途**：让 AI 写 Dockerfile 时不只是“能 build”，而是兼顾体积、安全、缓存和可维护性。  
**适合**：新服务容器化、镜像优化、多阶段构建。

```text
Treat this as a production containerization task, not just a Dockerfile generation request.

Before writing the Dockerfile, assess:
- runtime requirements,
- build dependencies,
- image size,
- layer caching,
- security posture,
- startup behavior,
- configuration injection,
- maintainability.

Prefer a clean, minimal, reproducible, production-safe image over a quick image that merely builds.
```

## 2. Compose 架构与本地开发版
**用途**：让 AI 设计 Compose 时兼顾本地开发体验和未来扩展，而不是把所有服务乱堆在一起。  
**适合**：本地联调、开发环境编排、服务依赖搭建。

```text
Design this Docker Compose setup like an engineer maintaining a real local development environment.

Do not just stack services into one file.
Think through:
- service boundaries,
- dependency order,
- health assumptions,
- volumes,
- ports,
- environment variables,
- local developer ergonomics,
- maintainability as the stack grows.

Prefer a clear and predictable Compose setup over a fragile one-shot configuration.
```

## 3. 容器排障根因版
**用途**：容器起不来、瞬间退出、网络不通、卷挂载异常时很好用。  
**适合**：Crash、启动失败、配置未生效、端口暴露问题。

```text
Debug this container issue systematically.

Do not assume the visible startup error is the root cause.
Check:
- entrypoint and command behavior,
- environment variable injection,
- filesystem paths,
- permissions,
- exposed and published ports,
- network assumptions,
- bind mounts and volumes,
- dependency readiness.

Explain the likely root cause first, then propose the cleanest fix.
```

## 4. 镜像安全与最小化版
**用途**：让 AI 从镜像基底、用户权限、秘密信息和攻击面角度 review。  
**适合**：生产镜像、安全 review、镜像基线。

```text
Review this container setup from a security and minimization perspective.

Focus on:
- base image choice,
- unnecessary packages,
- root vs non-root execution,
- secret handling,
- build-time leakage,
- filesystem permissions,
- network exposure,
- attack surface.

Prefer a secure, minimal, production-grade container design.
```

## 5. 构建与发布流程版
**用途**：让 AI 设计镜像构建、tag、缓存和发布策略。  
**适合**：CI 构建、镜像仓库发布、多环境镜像流转。

```text
Design this Docker build and release flow like an engineer responsible for reliable delivery.

Consider:
- image tagging strategy,
- cache usage,
- reproducibility,
- artifact traceability,
- environment promotion,
- rollback practicality,
- registry behavior,
- build-time secret safety.

Do not optimize only for a successful build.
Prefer a release process that is traceable, maintainable, and production-safe.
```

## 6. 资源与运行时行为版
**用途**：容器内应用运行稳定性、内存限制、信号处理、日志输出。  
**适合**：OOM、优雅退出、容器行为不稳定。

```text
Review this container runtime behavior like a production engineer.

Evaluate:
- signal handling,
- graceful shutdown,
- stdout/stderr logging,
- memory behavior,
- CPU expectations,
- health assumptions,
- startup sequencing,
- process model inside the container.

Recommend a runtime setup that behaves predictably in real environments.
```

## 7. Docker 文档 / Runbook 版
**用途**：输出可执行的容器构建、运行、排障、回滚文档。  
**适合**：README、运行手册、交接文档。

```text
Write this as a practical Docker runbook for engineers.

Include:
- purpose,
- prerequisites,
- build steps,
- run steps,
- environment variables,
- validation steps,
- troubleshooting guidance,
- rollback or recovery notes if relevant.
```
