# AI 编程高频增强提示词总览

这份文档是仓库里的通用版入口，负责把主清单和专用版之间的关系整理清楚。

如果你想直接看完整原始版本，请打开：

- [原始主清单快照](../../AI编程高频增强提示词清单_2026-03-10.md)

如果你想按专题快速使用，请直接跳到：

- [Kubernetes 专用版](../specialized/kubernetes.md)
- [Nginx 专用版](../specialized/nginx.md)
- [Shell / Bash 专用版](../specialized/shell-bash.md)
- [Python 自动化专用版](../specialized/python-automation.md)
- [Windows Server 自动化专用版](../specialized/windows-server-automation.md)
- [OpenClaw / Codex / Claude Code 专用版](../specialized/agent-coding-clients.md)
- [Docker / Compose 专用版](../specialized/docker-compose.md)
- [CI/CD / GitHub Actions 专用版](../specialized/cicd-github-actions.md)
- [Terraform / Ansible 专用版](../specialized/terraform-ansible.md)
- [SQL 数据库专用版](../specialized/sql-database.md)
- [NoSQL 数据库专用版](../specialized/nosql-database.md)

---

## 通用版包含什么

当前主清单已经覆盖了这些最常用场景：

- Bug 修复
- 重构
- 功能实现 / 最佳方案设计
- 代码评审
- 配置修改
- 文档编写
- 测试补全
- 万能通用前缀
- 高频补刀句
- 直接套用模板

这些内容已经足够解决大多数通用开发需求。

---

## 什么情况下该去看专用版

如果你的任务已经明显进入某个垂直技术域，推荐优先用专用版，而不是只靠通用版。

例如：

- 你在改 Deployment、Ingress、Helm values：去看 Kubernetes 专用版
- 你在改反向代理、TLS、location、缓存：去看 Nginx 专用版
- 你在写脚本、批处理、cron、命令链：去看 Shell / Bash 专用版
- 你在做批量文件处理、API 自动化、任务调度：去看 Python 自动化专用版
- 你在做 IIS、服务控制、任务计划、PowerShell：去看 Windows Server 自动化专用版
- 你在跟 OpenClaw / Codex / Claude Code 这类 coding agent 协作：去看 Agent 专用版
- 你在写 Dockerfile、Compose、镜像构建与容器排障：去看 Docker / Compose 专用版
- 你在改 GitHub Actions、流水线、发布门禁与回滚：去看 CI/CD / GitHub Actions 专用版
- 你在改 Terraform、Ansible、模块结构和基础设施变更：去看 Terraform / Ansible 专用版
- 你在做表结构、SQL 查询、索引、事务、迁移和慢查询优化：去看 SQL 数据库专用版
- 你在做 Redis、MongoDB、DynamoDB、Cassandra、Elasticsearch 这类模型、热点和容量问题：去看 NoSQL 数据库专用版

---

## 建议的使用方式

### 方式一：通用版 + 具体任务

```text
[通用增强提示词]

Now here is my actual task:
[你的具体需求]
```

### 方式二：通用版 + 专用版叠加

```text
[通用增强提示词]

[某个专用版提示词]

Now here is my actual task:
[你的具体需求]
```

### 方式三：通用版 + 专用版 + 真实上下文

```text
[通用增强提示词]

[某个专用版提示词]

Context:
[背景信息]

Task:
[具体任务]

Code / Config / File:
[代码、配置、日志、文档]
```

---

## 推荐组合思路

- 通用版负责给 AI 一个“像高级工程师一样工作”的总约束
- 专用版负责把技术域内的关键风险、惯例和排障思路补上
- 真实上下文负责让输出从“像样”变成“可直接落地”

---

## 后续扩展建议

这个仓库后面还可以继续往下加：

- 数据库排障专用版
- 前端工程专用版
- Java / Go / Node.js 语言专用版

但建议每次只补一个主题，并同步把 `README.md` 的导航补上。
