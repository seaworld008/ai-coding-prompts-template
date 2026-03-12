# README And Repository Metadata Design

## 背景

当前仓库已经具备基础开源结构，但首页展示还偏“文档入口页”，缺少更强的开源仓库首页感。同时，GitHub 仓库描述和 topics 还未设置，不利于搜索和传播。

## 目标

本次补强聚焦两件事：

- 优化 `README.md` 顶部展示，让仓库首页更像公开项目首页
- 为 GitHub 仓库补上中英文描述对应的话术和搜索友好的 topics

## 方案对比

### 方案一：只补一句描述

优点：

- 改动最少
- 风险最低

缺点：

- 首页仍然偏平
- 对 GitHub 首屏吸引力提升有限

### 方案二：增强 README 顶部首屏

优点：

- 不改变整体文档结构
- 可以强化定位、适用人群、快速入口和仓库亮点
- 仍然保持当前 Markdown 风格

缺点：

- 需要重排 README 前半部分

### 方案三：重做整份 README

优点：

- 展示最强

缺点：

- 改动过大
- 容易偏离当前已成型的结构

## 推荐方案

采用方案二：

- 保留现有 README 主体结构
- 强化标题、副标题、亮点和快速开始
- 不大改正文内容顺序

## README 顶部设计

新增或强化以下内容：

- 更清晰的副标题
- 仓库亮点摘要
- 更醒目的快速开始
- 更自然的“通用版 + 专用版”导读

## GitHub 元信息设计

### 推荐英文短描述

`Open-source AI coding prompt template repo with Chinese explanations, English prompts, and specialized engineering playbooks.`

### 推荐 topics

- `ai`
- `prompts`
- `ai-coding`
- `prompt-engineering`
- `developer-tools`
- `software-engineering`
- `devops`
- `kubernetes`
- `nginx`
- `automation`

## 风格约束

- 不引入花哨模板
- 不加无意义徽章
- 保持当前中文主叙事风格
- 首页要让首次访问者 10 秒内知道仓库是什么、怎么用、去哪里看
