# Community Templates Design

## 背景

当前仓库已经有：

- `README.md`
- `CONTRIBUTING.md`
- `SECURITY.md`
- `CODE_OF_CONDUCT.md`

但对于一个更完整的 GitHub 开源模板仓库来说，还缺少日常协作入口：

- Issue 模板
- Pull Request 模板
- Support 指引
- Maintainers 说明

## 目标

让仓库具备更完整的社区协作骨架，同时保持当前仓库“轻量、内容优先、Markdown 直给”的风格。

## 方案对比

### 方案一：只补 Bug 和 PR 模板

优点：

- 最少改动
- 上手最快

缺点：

- 对文档型仓库不够贴合
- 无法很好引导新增提示词内容的贡献

### 方案二：标准社区协作包

包含：

- Bug Issue 模板
- Feature Request 模板
- Prompt Submission 模板
- Issue 配置
- Pull Request 模板
- `SUPPORT.md`
- `MAINTAINERS.md`

优点：

- 更符合当前仓库类型
- 既支持内容补充，也支持问题反馈
- 不会引入过度复杂的治理结构

缺点：

- 文件数量会增加一些

### 方案三：社区自动化增强包

在方案二基础上增加 labels、workflow、自动分流等。

优点：

- 社区流程更完整

缺点：

- 超出当前必要范围

## 推荐方案

采用方案二。

## 设计原则

- 模板尽量短，不制造表单疲劳
- 内容贴合“提示词仓库”而不是“应用代码仓库”
- 中文为主，保留必要英文字段名以适应 GitHub 模板格式
- README 增加轻量入口，但不把首页变成流程说明墙
