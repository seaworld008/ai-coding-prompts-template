# Database Split Design

## 背景

仓库当前已经有较完整的基础设施与交付类专题，但“数据库”仍然缺位。

数据库方向如果只写成一篇泛泛总览，容易把 SQL 和 NoSQL 两类完全不同的问题混在一起：

- SQL 更偏表结构、索引、事务、查询计划、迁移和一致性
- NoSQL 更偏数据模型、分区、副本、吞吐、TTL、热点与最终一致性

## 目标

新增数据库相关专题，并保持仓库内容对真实工程场景的针对性。

## 方案对比

### 方案一：单篇数据库总览

优点：

- 入口简单
- 文件更少

缺点：

- SQL 与 NoSQL 场景容易混淆
- 内容会变得过宽、泛化

### 方案二：SQL 一篇

优点：

- 聚焦最常见数据库场景

缺点：

- 无法覆盖大量 NoSQL 实践问题

### 方案三：拆成 SQL / NoSQL 两篇

优点：

- 结构最清晰
- 更贴近真实工程差异
- 便于未来继续细分到 PostgreSQL、MySQL、Redis、MongoDB 等方向

缺点：

- 需要多维护一篇文档

## 推荐方案

采用方案三。

## 设计原则

- 两篇都保持“中文说明 + 英文提示词”
- 不把产品选型百科硬塞进文档
- 重点覆盖数据库工程中最常见的设计、排障、性能与变更场景
- README 和通用总览同步增加入口

## 预期结果

本轮新增：

- `docs/specialized/sql-database.md`
- `docs/specialized/nosql-database.md`

并同步更新：

- `README.md`
- `docs/general/core-prompt-list.md`

如有必要，再补充 GitHub repository topics，例如 `database`、`sql`、`nosql`。
