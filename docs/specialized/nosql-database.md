# NoSQL 数据库专用版

这份文档适合 Redis、MongoDB、Cassandra、DynamoDB、Elasticsearch 等偏 NoSQL 场景。

重点覆盖：

- 数据模型设计
- 分区与副本
- 访问模式
- 一致性与吞吐
- 热点与容量问题
- 备份、恢复与生产排障

---

## 1. 数据模型设计版
**用途**：让 AI 在设计 NoSQL 模型时，先围绕访问模式来想，而不是照搬关系型设计。  
**适合**：新建集合、Key 设计、文档模型、事件数据、缓存模型。

```text
Design this NoSQL data model around real access patterns, not around relational habits.

Before proposing the model, think through:
- read and write patterns,
- partitioning needs,
- document or key shape,
- denormalization trade-offs,
- update frequency,
- query constraints,
- retention behavior,
- operational simplicity.

Prefer a data model that matches the workload instead of forcing relational structure into a NoSQL system.
```

## 2. 分区 / 分片 / 热点版
**用途**：NoSQL 最容易踩的坑之一就是热点 key、分片不均和写入倾斜。  
**适合**：吞吐不稳、热点 key、分片负载不均、容量扩展。

```text
Analyze this NoSQL design from a partitioning and hotspot perspective.

Do not assume the current key or shard strategy is acceptable.
Evaluate:
- partition key distribution,
- write skew,
- read hotspots,
- replication fan-out,
- resharding implications,
- time-based concentration,
- high-cardinality vs low-cardinality trade-offs.

Recommend a data distribution strategy that remains stable under scale.
```

## 3. 一致性与正确性版
**用途**：让 AI 在 NoSQL 场景下明确一致性模型，而不是默认“最终一致性就行”。  
**适合**：缓存一致性、读写顺序要求、事件处理、幂等写入。

```text
Review this NoSQL workflow from a consistency and correctness perspective.

Clarify:
- what consistency level is actually required,
- whether stale reads are acceptable,
- write visibility assumptions,
- idempotency,
- retry safety,
- duplicate event handling,
- ordering guarantees,
- reconciliation strategy.

Do not hide correctness trade-offs behind vague eventual consistency language.
```

## 4. 吞吐与容量优化版
**用途**：面向高吞吐、低延迟、容量评估和成本控制。  
**适合**：Redis / DynamoDB / Cassandra / Elasticsearch 容量与性能问题。

```text
Review this NoSQL workload from a throughput, latency, and capacity perspective.

Do not suggest random scaling changes.
Evaluate:
- read vs write profile,
- working set size,
- memory pressure,
- storage growth,
- replication overhead,
- compaction or indexing costs,
- request amplification,
- operational cost.

Recommend an optimization strategy that is realistic, scalable, and operationally safe.
```

## 5. 线上排障根因版
**用途**：缓存击穿、集群抖动、查询变慢、节点不均衡时很好用。  
**适合**：生产故障、性能劣化、节点异常、数据延迟。

```text
Debug this NoSQL production issue systematically.

Do not assume the symptom points directly to the root cause.
Check:
- data distribution,
- replication lag,
- node imbalance,
- memory or disk pressure,
- compaction behavior,
- index usage,
- query pattern drift,
- timeout and retry amplification,
- client-side connection behavior.

Identify the most likely root cause first, then propose the safest corrective action.
```

## 6. 备份 / 恢复 / 运维安全版
**用途**：让 AI 在 NoSQL 运维操作上兼顾备份一致性、恢复步骤和风险边界。  
**适合**：备份策略、灾备、节点替换、集群维护。

```text
Review this NoSQL operational plan from a backup, recovery, and safety perspective.

Consider:
- snapshot consistency,
- restore objectives,
- replica behavior,
- failover implications,
- maintenance sequencing,
- data-loss windows,
- verification after recovery,
- rollback practicality.

Prefer an operational plan that is explicit, testable, and safe under failure.
```

## 7. NoSQL Runbook / 文档版
**用途**：输出可执行的 NoSQL 运维与排障文档。  
**适合**：值班手册、恢复手册、交接文档、平台文档。

```text
Write this as a practical NoSQL database runbook.

Include:
- purpose,
- scope,
- prerequisites,
- exact steps,
- expected observations,
- verification checks,
- backup or recovery notes,
- warnings for risky operations such as rebalancing, failover, or large data movement.
```
