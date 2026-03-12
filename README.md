# AI 编程高频增强提示词仓库模板

Open-source AI coding prompt template repo with Chinese explanations, English prompts, and specialized engineering playbooks.

一个面向真实工程场景的 AI 编程提示词模板仓库，适合直接开源、团队共用，或作为你自己的提示词资产库继续扩展。

---

## 仓库概览

| 你想知道什么 | 简短答案 |
|---|---|
| 这是什么 | 一个面向真实工程场景的 AI 编程提示词模板仓库，采用“中文说明 + 英文提示词”结构。 |
| 为什么存在 | 为了让提示词更贴近真实开发、交付和运维任务，而不是停留在泛化或营销化表达。 |
| 适合谁用 | 适合个人沉淀提示词、团队建立协作基线，或继续扩展成公开的 GitHub 模板仓库。 |
| 内容结构 | 分为通用版和专用版两层，既能覆盖大多数任务，也能按技术域快速进入。 |

---

## 按任务选择指南

如果你不确定先看哪篇，可以按下面这个表快速进入：

| 你的任务 | 推荐入口 |
|---|---|
| 通用开发、Bug 修复、重构、测试补全 | [通用版总览](./docs/general/core-prompt-list.md) |
| Kubernetes、Helm、Ingress、Pod 排障 | [Kubernetes 专用版](./docs/specialized/kubernetes.md) |
| 反向代理、TLS、缓存、location / rewrite | [Nginx 专用版](./docs/specialized/nginx.md) |
| Shell 脚本、cron、批处理、命令链 | [Shell / Bash 专用版](./docs/specialized/shell-bash.md) |
| Python 脚本自动化、API 批处理、定时任务 | [Python 自动化专用版](./docs/specialized/python-automation.md) |
| Windows Server、PowerShell、IIS、任务计划 | [Windows Server 自动化专用版](./docs/specialized/windows-server-automation.md) |
| Codex、Claude Code、OpenClaw 协作 | [OpenClaw / Codex / Claude Code 专用版](./docs/specialized/agent-coding-clients.md) |
| Dockerfile、Compose、镜像构建、容器排障 | [Docker / Compose 专用版](./docs/specialized/docker-compose.md) |
| GitHub Actions、发布门禁、流水线失败排障 | [CI/CD / GitHub Actions 专用版](./docs/specialized/cicd-github-actions.md) |
| Terraform、Ansible、IaC 变更与漂移治理 | [Terraform / Ansible 专用版](./docs/specialized/terraform-ansible.md) |
| 表结构、SQL、索引、事务、慢查询 | [SQL 数据库专用版](./docs/specialized/sql-database.md) |
| Redis、MongoDB、DynamoDB、热点与容量问题 | [NoSQL 数据库专用版](./docs/specialized/nosql-database.md) |

---

## 快速开始

如果你第一次使用这个仓库，最推荐走这条路径：

1. 先看上面的“按任务选择指南”，找到最接近当前任务的入口
2. 打开对应的通用版或专用版文档
3. 复制提示词，并把你的真实上下文拼接进去
4. 如果 AI 输出涉及生产环境，再做人工审查和实际验证

---

## 如何使用

最常见的使用方式是：

1. 从 [通用版总览](./docs/general/core-prompt-list.md) 里选一条最接近当前任务的提示词
2. 如果任务属于明确技术域，再叠加一个对应的 [专用版](./docs/specialized/)
3. 把真实上下文接在提示词后面交给 AI

最短用法：

```text
[增强提示词]

Now here is my actual task:
[你的具体需求]
```

更完整的用法：

```text
[增强提示词]

Context:
[背景信息]

Task:
[你的具体任务]

Code / Config / File:
[你的代码、配置、日志、文档内容]
```

---

## 常见使用示例

### 示例 1：修一个线上 Bug

```text
[Bug 修复类增强提示词]

Context:
This is a production issue in our payment service.

Task:
Find the root cause and propose a proper fix.

Code / Config / File:
[错误日志 + 相关代码]
```

### 示例 2：改 Kubernetes 配置

```text
[通用增强提示词]

[Kubernetes 专用版提示词]

Task:
Review this Deployment and Ingress change for production safety.

Code / Config / File:
[YAML 内容]
```

### 示例 3：设计一条 GitHub Actions 流水线

```text
[通用增强提示词]

[CI/CD / GitHub Actions 专用版提示词]

Task:
Design a CI pipeline for build, test, and release.

Code / Config / File:
[仓库背景、技术栈、现有 workflow]
```

### 示例 4：分析 SQL 慢查询

```text
[SQL 数据库专用版提示词]

Task:
Analyze this slow query and recommend practical improvements.

Code / Config / File:
[SQL 语句 + 执行计划 + 表结构]
```

---

## 内容导航

### 通用入口

- [通用版总览](./docs/general/core-prompt-list.md)
- [原始主清单快照](./docs/archive/2026-03-10-original-prompt-list.md)

### 专题入口

- [Kubernetes 专用版](./docs/specialized/kubernetes.md)
- [Nginx 专用版](./docs/specialized/nginx.md)
- [Shell / Bash 专用版](./docs/specialized/shell-bash.md)
- [Python 自动化专用版](./docs/specialized/python-automation.md)
- [Windows Server 自动化专用版](./docs/specialized/windows-server-automation.md)
- [OpenClaw / Codex / Claude Code 专用版](./docs/specialized/agent-coding-clients.md)
- [Docker / Compose 专用版](./docs/specialized/docker-compose.md)
- [CI/CD / GitHub Actions 专用版](./docs/specialized/cicd-github-actions.md)
- [Terraform / Ansible 专用版](./docs/specialized/terraform-ansible.md)
- [SQL 数据库专用版](./docs/specialized/sql-database.md)
- [NoSQL 数据库专用版](./docs/specialized/nosql-database.md)

---

## 安装与获取

这个仓库是 Markdown 文档仓库，不需要编译或安装依赖。

你可以直接：

1. 在 GitHub 上浏览文档
2. 克隆到本地长期维护
3. 点击 “Use this template” 二次创建你自己的版本

克隆方式：

```bash
git clone git@github.com:seaworld008/ai-coding-prompts-template.git
cd ai-coding-prompts-template
```

---

## 前置条件

使用这个仓库前，通常只需要这些前提：

- 你有一个可用的 AI 工具或 coding assistant
- 你知道自己的任务大概属于什么场景
- 你能提供尽量真实的上下文，例如代码、日志、配置、需求或报错信息

推荐但不是必须：

- GitHub 账号，用于 fork、提交 issue 或 PR
- 一个顺手的 Markdown 编辑器
- 基本的工程判断能力，用来筛选 AI 输出是否适合你的环境

---

## 仓库结构

```text
.
├─ README.md
├─ CONTRIBUTING.md
├─ SECURITY.md
├─ CODE_OF_CONDUCT.md
├─ SUPPORT.md
├─ MAINTAINERS.md
├─ docs/
│  ├─ archive/
│  ├─ general/
│  ├─ specialized/
│  └─ plans/
```

关键目录说明：

- `README.md`：仓库首页与主要入口
- `docs/archive/`：历史版本与归档快照
- `docs/general/`：通用版总览
- `docs/specialized/`：按技术域划分的专用版文档
- `docs/plans/`：仓库演进设计与实施记录
- `SUPPORT.md` / `MAINTAINERS.md`：支持与维护说明

---

## 维护约定

如果你准备继续维护或二次改造这个仓库，建议保持这些约定：

- 提示词写英文，说明写中文
- 一个文件尽量只覆盖一个明确主题
- 优先写可直接复制使用的内容，而不是概念性空话
- 新增专题时，记得同步更新 README 和总览导航

相关文档：

- [CONTRIBUTING.md](./CONTRIBUTING.md)
- [SECURITY.md](./SECURITY.md)
- [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md)
- [SUPPORT.md](./SUPPORT.md)
- [MAINTAINERS.md](./MAINTAINERS.md)

---

## 限制与注意事项

- 这个仓库提供的是提示词模板，不保证 AI 输出天然正确
- 不同模型、不同上下文质量，输出差异会很大
- 专用版能提升命中率，但不能替代真实环境验证
- 涉及生产配置、数据库迁移、权限安全、发布流程时，仍然需要人工审查
- 这个仓库不是 SaaS 产品，也不提供运行时服务

换句话说，它更像一个工程化提示词工具箱，而不是自动保证正确结果的系统。

---

## 贡献与协作

欢迎补充新的高频场景、专用版清单和更稳的模板写法。

比较推荐的贡献方向：

- 补新的高价值专题
- 修正文档中的风险点或失效链接
- 优化 README 导航和内容结构
- 提交更贴近真实工程场景的提示词条目

你可以通过这些入口参与：

- [CONTRIBUTING.md](./CONTRIBUTING.md)
- [SUPPORT.md](./SUPPORT.md)
- [SECURITY.md](./SECURITY.md)

---

## 开源说明

当前仓库默认使用 [MIT License](./LICENSE)。

如果你更希望它偏向文档内容分发，也可以在后续切换为更适合文档仓库的许可证。

---

## 设计记录

如果你关心这个仓库是如何一步步搭出来的，可以看这些设计与计划文档：

- [仓库设计文档](./docs/plans/2026-03-12-ai-prompt-repo-design.md)
- [README 与元信息设计](./docs/plans/2026-03-12-readme-metadata-design.md)
- [开源增强设计](./docs/plans/2026-03-12-open-source-polish-design.md)
- [社区模板设计](./docs/plans/2026-03-12-community-templates-design.md)
- [专题扩展设计](./docs/plans/2026-03-12-specialized-expansion-design.md)
- [数据库拆分设计](./docs/plans/2026-03-12-database-split-design.md)
- [工程 README 设计](./docs/plans/2026-03-12-engineering-readme-design.md)
