# SQL 数据库专用版

这份文档适合关系型数据库场景，比如 PostgreSQL、MySQL、MariaDB、SQL Server 等。

重点覆盖：

- 表结构设计
- SQL 查询
- 索引优化
- 事务与一致性
- 迁移与变更
- 慢查询与生产排障

---

## 1. 表结构设计版
**用途**：让 AI 在设计表结构时，不只是“能存数据”，而是考虑规范化、扩展性和查询模式。  
**适合**：新建表、重构 schema、核心业务模型设计。

```text
Design this relational schema like a senior database engineer.

Before proposing tables, think through:
- access patterns,
- normalization vs pragmatic denormalization,
- primary and foreign keys,
- data integrity,
- indexing implications,
- growth patterns,
- migration safety,
- long-term maintainability.

Do not optimize only for getting the first version working.
Prefer a schema that remains understandable and stable as the system grows.
```

## 2. SQL 查询设计版
**用途**：让 AI 写 SQL 时兼顾正确性、可读性和未来维护成本。  
**适合**：报表查询、业务查询、复杂 join、聚合场景。

```text
Write this SQL like an engineer who cares about correctness, clarity, and maintainability.

Before finalizing the query, validate:
- whether the logic matches the actual business requirement,
- join correctness,
- null handling,
- duplicate-row risk,
- grouping behavior,
- filter selectivity,
- readability for future maintenance.

Do not produce a query that is merely syntactically valid.
Prefer a query that is correct, explicit, and reviewable.
```

## 3. 索引与执行计划优化版
**用途**：让 AI 从执行计划和访问路径角度分析性能，而不是机械“加索引”。  
**适合**：慢查询、扫描过大、排序过重、查询延迟高。

```text
Analyze this SQL performance issue from an execution-plan perspective.

Do not suggest indexes mechanically.
Evaluate:
- actual access patterns,
- filter selectivity,
- join order,
- sort and aggregation costs,
- covering opportunities,
- write overhead,
- index maintenance trade-offs.

Identify the likely bottleneck first, then recommend the most practical optimization.
```

## 4. 事务与一致性版
**用途**：涉及并发写入、余额扣减、库存锁定、订单状态流转时非常重要。  
**适合**：高一致性业务、竞态问题、并发更新。

```text
Review this database logic from a transaction and consistency perspective.

Focus on:
- isolation assumptions,
- race conditions,
- locking behavior,
- lost updates,
- retry semantics,
- idempotency,
- rollback boundaries,
- correctness under concurrent load.

Do not assume the happy path proves correctness.
Prefer a design that remains correct under real concurrency.
```

## 5. 数据迁移与变更安全版
**用途**：让 AI 设计 schema 变更时兼顾兼容性、回滚和停机风险。  
**适合**：加列、改列、拆表、回填、数据迁移。

```text
Design this database change like an engineer responsible for production safety.

Consider:
- backward compatibility,
- lock risk,
- migration ordering,
- data backfill strategy,
- application compatibility during rollout,
- rollback feasibility,
- verification steps,
- blast radius.

Do not optimize only for getting the migration script accepted.
Prefer a change plan that is staged, reversible, and production-safe.
```

## 6. 慢查询与线上排障版
**用途**：线上查询变慢、CPU 飙升、锁等待、连接堆积时很好用。  
**适合**：生产数据库排障、性能问题定位、容量压力分析。

```text
Debug this SQL database issue systematically.

Do not assume the slow query text alone is the root cause.
Check:
- query plan behavior,
- locking and blocking,
- missing or inefficient indexes,
- stale statistics,
- parameter sensitivity,
- connection pool behavior,
- workload spikes,
- schema or data distribution changes.

Explain the most likely root cause first, then propose the safest fix.
```

## 7. SQL Runbook / 文档版
**用途**：输出可以交付给工程团队执行的数据库操作说明。  
**适合**：迁移 SOP、排障手册、值班文档、执行步骤说明。

```text
Write this as a practical SQL database runbook for engineers.

Include:
- purpose and scope,
- prerequisites,
- exact steps,
- validation queries,
- expected results,
- rollback or recovery guidance,
- warnings for risky operations such as schema changes or large updates.
```
