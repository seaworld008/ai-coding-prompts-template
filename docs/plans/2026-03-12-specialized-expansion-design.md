# Specialized Expansion Design

## 背景

当前仓库已经覆盖：

- Kubernetes
- Nginx
- Shell / Bash
- Python 自动化
- Windows Server 自动化
- OpenClaw / Codex / Claude Code

这些内容已经形成了一个不错的基础，但从真实工程使用频率来看，还缺少三个非常高价值的基础设施与交付主题：

- Docker / Compose
- CI/CD / GitHub Actions
- Terraform / Ansible

## 目标

继续扩充仓库的专用版专题，让它更像一个真正可长期维护的“工程场景提示词库”，而不是只停留在首批常见主题。

## 方案对比

### 方案一：继续补运维基础设施专题

补：

- Docker / Compose
- CI/CD / GitHub Actions
- Terraform / Ansible

优点：

- 与现有 Kubernetes、Nginx、Shell 内容形成天然闭环
- 搜索价值高
- 对真实工程团队更有吸引力

缺点：

- 内容量会继续增加

### 方案二：补语言生态专题

补：

- Java
- Go
- Node.js

优点：

- 更贴近开发者语言栈

缺点：

- 与当前已成型的运维 / 平台方向衔接没那么强

### 方案三：补协作流程专题

补：

- Code Review
- PR 流程
- 发布流程

优点：

- 治理层内容更完整

缺点：

- 当前仓库已经有较多通用工程方法内容，这一方向短期收益不如基础设施专题明显

## 推荐方案

采用方案一。

## 设计原则

- 每个专题仍然独立成篇
- 不和通用版重复堆内容
- 更强调该技术域里的典型坑位、排障路径、生产安全和工程落地
- README 和总览文档同步增加入口

## 预期结果

本轮完成后，仓库会新增 3 篇专题文档：

- `docs/specialized/docker-compose.md`
- `docs/specialized/cicd-github-actions.md`
- `docs/specialized/terraform-ansible.md`

并同步更新：

- `README.md`
- `docs/general/core-prompt-list.md`

如有必要，再补充 GitHub repository topics。
