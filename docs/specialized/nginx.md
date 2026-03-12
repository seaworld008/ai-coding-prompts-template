# Nginx 专用版

这份文档适合 Nginx 反向代理、静态资源分发、负载均衡、TLS、缓存、日志和高并发场景。

---

## 1. 生产配置审查版
**用途**：让 AI 按生产标准看 Nginx 配置，而不是只看语法是否能过。  
**适合**：`nginx.conf`、server 块、upstream、反向代理配置。

```text
Treat this as a production Nginx configuration review.

Do not stop at syntax correctness.
Evaluate whether the configuration is operationally sound, maintainable, and aligned with common Nginx conventions.

Focus on:
- request routing,
- timeout behavior,
- buffer settings,
- header forwarding,
- upstream health assumptions,
- TLS and redirect behavior,
- logging and observability,
- failure modes under load.
```

## 2. location / rewrite 排障版
**用途**：URI 匹配、rewrite、try_files、反向代理路径问题非常适合。  
**适合**：404、路径错乱、代理后路径不对。

```text
Debug this Nginx routing issue systematically.

Do not assume the visible 404 or 502 is the real problem.
Analyze request matching order, location precedence, rewrite behavior, try_files logic, proxy_pass path semantics, and upstream expectations.

Explain the exact request flow first.
Then propose the cleanest fix.
Do not stack extra rewrite rules onto a broken routing design.
```

## 3. TLS / HTTPS 安全版
**用途**：证书、HTTPS 跳转、TLS 配置、HSTS、安全头审查。  
**适合**：对外服务、生产站点、网关层。

```text
Review this Nginx setup from a TLS and edge-security perspective.

Check:
- certificate handling,
- protocol and cipher posture,
- HTTP to HTTPS redirects,
- HSTS suitability,
- proxy header trust,
- security headers,
- mixed-content and origin assumptions.

Use professional judgment.
Prefer a secure, maintainable, production-grade edge configuration over a quick patch.
```

## 4. 性能与并发优化版
**用途**：高并发、慢响应、静态资源分发、连接数问题。  
**适合**：性能优化、容量评估、参数调优。

```text
Analyze this Nginx configuration from a performance and concurrency perspective.

Do not suggest tuning values blindly.
Relate recommendations to workload shape, connection behavior, upstream latency, static asset patterns, keepalive usage, buffering, compression, and file serving strategy.

Recommend changes that improve throughput and stability without creating fragile tuning debt.
```

## 5. upstream 与故障隔离版
**用途**：多后端服务、负载均衡、容错策略、超时和重试。  
**适合**：502、504、单节点抖动、后端切换。

```text
Review this Nginx upstream and proxy design like an engineer responsible for production availability.

Focus on:
- load-balancing behavior,
- upstream failure handling,
- timeout and retry semantics,
- keepalive reuse,
- connection exhaustion risk,
- request amplification,
- rollback safety.

If the upstream strategy is flawed, redesign it cleanly instead of adding one more directive as a patch.
```

## 6. 日志与可观测性版
**用途**：希望 AI 不只是改配置，还能把定位问题的日志策略一起设计出来。  
**适合**：线上排障、边缘流量诊断、审计。

```text
Design the Nginx logging and observability setup for real operations.

Do not keep only the default access log if it is insufficient for diagnosing issues.
Evaluate what should be logged for routing, latency, upstream behavior, request identity, TLS termination, and failure analysis.

Recommend a logging strategy that is practical, debuggable, and production-safe.
```

## 7. Nginx Runbook 版
**用途**：生成可执行的配置变更、重载、验证和回滚手册。  
**适合**：交接文档、SRE 手册、上线 SOP。

```text
Write this as an Nginx operational runbook.

Include:
- purpose and scope,
- configuration change steps,
- validation commands,
- reload sequence,
- expected results,
- rollback procedure,
- warnings for risky changes such as TLS or routing updates.

Assume the reader may need to execute it under production pressure.
```
