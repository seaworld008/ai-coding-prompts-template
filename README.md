# AI 编程高频增强提示词仓库模板

一个适合直接开源到 GitHub 的 AI 编程提示词样板仓库。

Open-source AI coding prompt template repo with Chinese explanations, English prompts, and specialized engineering playbooks.

这个仓库延续你当前这份清单的写法：

- 提示词全部英文
- 说明全部中文
- 结构尽量工程化、可直接复制
- Markdown 风格保持简洁，不引入额外站点工具

---

## 仓库亮点

- 适合直接作为 GitHub 开源模板仓库使用
- 保留“中文说明 + 英文提示词”的高可复制结构
- 同时提供通用版和专用版，便于按场景快速取用
- 内容面向真实工程交付，而不是泛泛提示词堆砌

---

## 快速开始

如果你是第一次进入这个仓库，最推荐这样使用：

1. 从 [通用版总览](./docs/general/core-prompt-list.md) 里挑一条最接近你的任务
2. 如果任务属于明确技术域，再叠加一个 [专用版](./docs/specialized/)
3. 把你的真实上下文直接接在提示词后面发给 AI

最短可直接复制的使用方式：

```text
[增强提示词]

Now here is my actual task:
[你的具体需求]
```

---

## 快速跳转

### 通用版

- [通用版总览](./docs/general/core-prompt-list.md)
- [原始主清单快照](./AI编程高频增强提示词清单_2026-03-10.md)

### 专用版

- [Kubernetes 专用版](./docs/specialized/kubernetes.md)
- [Nginx 专用版](./docs/specialized/nginx.md)
- [Shell / Bash 专用版](./docs/specialized/shell-bash.md)
- [Python 自动化专用版](./docs/specialized/python-automation.md)
- [Windows Server 自动化专用版](./docs/specialized/windows-server-automation.md)
- [OpenClaw / Codex / Claude Code 专用版](./docs/specialized/agent-coding-clients.md)

### 设计与规划

- [仓库设计文档](./docs/plans/2026-03-12-ai-prompt-repo-design.md)
- [仓库实施计划](./docs/plans/2026-03-12-ai-prompt-repo-plan.md)

---

## 这个仓库适合做什么

适合把高频使用的 AI 编程增强提示词整理成一个长期维护、可分享、可协作、可继续扩展的开源仓库。

你可以把它当作：

- 个人提示词资产库
- 团队内部 AI 编程协作基线
- GitHub 开源示例仓库
- 后续继续扩充专题版的母仓库

---

## 使用方式

如果你需要把上下文提供得更完整，可以用这个结构：

```text
[增强提示词]

Context:
[背景信息]

Task:
[你的具体任务]

Code / Config / File:
[你的代码、配置、文档内容]
```

---

## 推荐阅读顺序

1. 先看 [通用版总览](./docs/general/core-prompt-list.md)
2. 再按场景进入对应 [专用版](./docs/specialized/)
3. 如果你想保留最初整理版本，再看 [原始主清单快照](./AI编程高频增强提示词清单_2026-03-10.md)

---

## 当前包含的内容

### 通用能力

- Bug 修复
- 重构
- 功能实现 / 最佳方案设计
- 代码评审
- 配置修改
- 文档编写
- 测试补全
- 万能通用前缀
- 高频补刀句
- 可直接套用模板

### 专题能力

- Kubernetes
- Nginx
- Shell / Bash
- Python 自动化
- Windows Server 自动化
- OpenClaw / Codex / Claude Code

---

## 维护约定

- 新增内容尽量继续使用“中文说明 + 英文提示词”
- 一个文档尽量只覆盖一个明确主题
- 先追求可直接使用，再追求华丽表达
- 优先保留工程交付感，而不是空泛措辞

---

## 贡献方式

欢迎补充新的高频场景、专用版清单和更稳的模板写法。

提交内容时，建议保持以下原则：

- 说明写中文，提示词写英文
- 尽量给出明确适用场景
- 提示词要能直接复制，不要过度依赖上下文解释
- 避免与现有条目高重复

更多细节见 [CONTRIBUTING.md](./CONTRIBUTING.md)。

---

## 开源说明

当前仓库默认附带 MIT License，后续如果你更想把它调整为偏文档内容友好的许可证，也可以再切换。
