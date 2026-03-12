# AI 编程高频增强提示词清单（最新版）

这份清单按你的要求整理：

- **提示词全部英文**
- **说明全部中文**
- **你在后面直接加自己的需求就能用**
- **分成 7 大类**
- **每条都尽量偏工程化、通用、能直接复制粘贴**

---

## 使用方式

最简单的用法：

```text
[增强提示词]

Now here is my actual task:
[你的具体需求]
```

或者：

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

# 1）Bug 修复

## 1. 根因修复版
**用途**：让 AI 不要看到报错就乱补丁，而是先找根因，再系统修复。  
**适合**：代码报错、服务异常、逻辑 bug、线上问题排查。

```text
Act like a senior engineer debugging a production issue.

Before changing anything, verify whether the current implementation is conceptually correct and whether the recent changes are based on a sound approach.

Do not patch around symptoms.
Identify the root cause first, then implement a proper fix systematically.

If the current direction or recent change is flawed, discard it rather than layering more fixes on top of it.

Prefer a clean, maintainable, production-safe solution over a quick workaround.
```

## 2. 强力纠偏版
**用途**：当 AI 已经开始乱改、越修越歪时，用这条把它拉回来。  
**适合**：连续改错、补丁越来越多、逻辑开始失控。

```text
Stop patching around.

Discard what you've just changed if it is based on a flawed approach.
Do not continue building on a wrong foundation.

First determine whether the solution is reasonable and aligned with industry conventions.
Then identify the root cause and implement a proper fix systematically.

Give me the corrected final solution, not a temporary workaround unless I explicitly ask for one.
```

## 3. 先诊断后动手版
**用途**：要求 AI 先分析问题，再改代码。  
**适合**：你怕它上来就改，结果改偏。

```text
Do not start editing immediately.

First:
1. explain the likely root cause,
2. point out any flawed assumptions in the current implementation,
3. state whether the current approach is reasonable and aligned with common engineering practice.

Only then propose and implement the fix.
Do not patch around symptoms; fix the problem systematically from the root cause.
```

---

# 2）重构

## 4. 标准重构版
**用途**：让 AI 用更专业的方式重构，而不是只改表面。  
**适合**：代码太乱、可维护性差、职责混乱。

```text
Act like a senior engineer performing a refactor.

Evaluate whether the current design is reasonable, maintainable, and aligned with industry conventions.
Use professional judgment to simplify structure, improve separation of concerns, and remove fragile patterns.

Do not preserve a bad structure just to minimize edits.
If parts of the implementation are fundamentally flawed, replace them properly instead of patching around them.

Prefer clarity, maintainability, and correctness over minimal change.
```

## 5. 第一性原理重构版
**用途**：让 AI 不受原来烂结构束缚，从更合理的角度重新设计。  
**适合**：老代码、历史包袱、设计本身就不对。

```text
Re-evaluate this implementation from first principles.

Do not assume the current structure is worth preserving.
Assess whether the design is actually sound, whether responsibilities are properly separated, and whether the implementation matches common engineering conventions.

If the current design is flawed, redesign the relevant parts properly rather than applying incremental patches.
Refactor systematically toward a cleaner, more robust, and more maintainable architecture.
```

## 6. 小改动但不妥协版
**用途**：希望改动尽量控制范围，但不接受在坏设计上硬凑。  
**适合**：项目已有约束，不能大改，但也不能瞎修。

```text
Keep the scope of change reasonable, but do not compromise engineering quality.

Evaluate whether the current implementation is sound.
If a small change is sufficient, apply it cleanly.
If the current design is flawed, say so clearly and fix the underlying issue rather than forcing a superficial minimal patch.

Use professional judgment to balance change scope, maintainability, and correctness.
```

---

# 3）功能实现 / 最佳方案设计

## 7. 标准方案设计版
**用途**：让 AI 不只是“把功能做出来”，而是先从设计层面给出更合理的实现方案。  
**适合**：新功能开发、模块设计、系统能力扩展、业务需求落地。

```text
Act like a senior engineer designing the best implementation approach for a new feature.

Before proposing code, evaluate the problem from a design perspective:
- what is the actual requirement,
- what constraints matter,
- what interfaces, data flow, and responsibilities are involved,
- what trade-offs exist.

Do not jump straight to coding.
First propose the most reasonable implementation approach based on industry conventions, maintainability, extensibility, and production safety.

Use professional judgment to reject weak or shortsighted designs.
Prefer a clean, scalable, and maintainable solution over a quick but fragile implementation.
```

## 8. 多方案对比版
**用途**：让 AI 先给多个实现方案，并比较利弊后再推荐最佳方案。  
**适合**：不确定技术路线、需要选型、功能实现方式有多种可能时。

```text
Think like a senior engineer doing solution design.

Do not provide only one implementation path immediately.
First propose 2 to 4 reasonable approaches for implementing this feature.

For each approach, compare:
- complexity,
- maintainability,
- scalability,
- performance,
- delivery speed,
- operational risk,
- alignment with industry conventions.

Then recommend the best option with clear reasoning, and only after that provide the implementation plan or code.
```

## 9. 面向可扩展性的方案设计版
**用途**：要求 AI 在设计功能时，把后续扩展、复用和演进也考虑进去。  
**适合**：平台能力、公共组件、中后台系统、长期维护模块。

```text
Design this feature with long-term maintainability and extensibility in mind.

Do not optimize only for the immediate requirement.
Evaluate whether the design will remain clean as the feature grows, whether responsibilities are properly separated, and whether future extensions can be added without creating technical debt.

Use professional judgment and follow common industry design conventions.
Prefer a modular, extensible, and production-grade solution over a narrow short-term implementation.
```

## 10. 先设计后实现版
**用途**：让 AI 先把方案、模块划分、接口和数据流想清楚，再开始写代码。  
**适合**：复杂功能、跨模块改动、多人协作开发。

```text
Do not start with code.

First design the implementation properly:
1. clarify the requirement and constraints,
2. define the architecture or module boundaries,
3. identify the main data flow and interfaces,
4. point out risks, trade-offs, and edge cases,
5. choose the best implementation approach.

Only then write the final implementation.
Avoid ad hoc coding and prefer a systematic design.
```

## 11. 工程落地版
**用途**：不只是讲概念，还要求 AI 给出可以直接推进开发的落地方案。  
**适合**：你希望 AI 输出开发步骤、模块拆分、接口建议、实施顺序。

```text
Design this feature as an engineer responsible for actual delivery.

Do not stay at the conceptual level.
Provide a practical implementation plan that can be executed by a real team.

Include:
- the recommended design,
- module or component breakdown,
- key interfaces or contracts,
- data flow,
- important edge cases,
- migration or rollout considerations if relevant,
- the recommended implementation order.

Prefer a solution that is clear, practical, maintainable, and ready for engineering execution.
```

---

# 4）代码评审

## 12. 严格代码评审版
**用途**：让 AI 像高级工程师做 code review。  
**适合**：审 PR、审脚本、审配置生成代码。

```text
Review this like a strict senior engineer.

Do not just look for syntax issues.
Evaluate correctness, maintainability, readability, failure modes, edge cases, and alignment with industry conventions.

Call out bad assumptions, fragile logic, hidden risks, and unnecessary complexity.
Use professional judgment and be direct.

Where appropriate, suggest a cleaner and more robust implementation.
```

## 13. 风险导向评审版
**用途**：专门看隐患、风险、线上事故点。  
**适合**：生产代码、关键路径、运维脚本、部署流程。

```text
Review this from a production-risk perspective.

Focus on:
- correctness,
- operational safety,
- maintainability,
- edge cases,
- failure handling,
- rollback and recovery concerns,
- security and configuration risks where relevant.

Do not assume the current implementation is acceptable.
Challenge weak design choices and point out anything that could cause production issues.
```

## 14. 带修改建议的评审版
**用途**：不是只挑毛病，还要求给出更好的实现建议。  
**适合**：你想直接拿去改。

```text
Review this critically and propose improvements.

For each important issue you find:
1. explain why it is a problem,
2. state whether it violates common engineering conventions or best practices,
3. propose a better implementation approach.

Prefer practical, maintainable, production-grade recommendations over theoretical comments.
```

---

# 5）配置修改

## 15. 生产安全配置版
**用途**：改配置时，要求 AI 按生产环境标准来考虑。  
**适合**：Nginx、Kubernetes、Docker、CI/CD、Vector、Prometheus、Redis、MySQL 等。

```text
Treat this as a production engineering task.

Before changing the configuration, verify whether the requested approach is operationally sound, aligned with common industry conventions, and safe for production use.

Do not apply mechanical edits.
Use professional judgment to identify flawed assumptions, hidden risks, and configuration drift.

If the current configuration or recent change is flawed, discard it and fix the root cause systematically.
Prefer a clean, explicit, maintainable, production-safe configuration.
```

## 16. YAML / IaC 专用版
**用途**：适合 Kubernetes YAML、Helm values、Terraform、Ansible 这类内容。  
**适合**：声明式配置、基础设施即代码。

```text
Treat this as infrastructure-as-code, not as a text editing task.

Validate whether the requested change is semantically correct, operationally safe, and consistent with common conventions for maintainable IaC.

Do not patch around broken structure or drift.
If the current configuration pattern is flawed, correct the pattern itself.

Prefer explicit, predictable, and production-safe configuration over clever but fragile shortcuts.
```

## 17. 配置排障版
**用途**：配置明明写了但就是不生效，让 AI 用排障思路看。  
**适合**：服务启动失败、配置冲突、行为异常。

```text
Debug this configuration systematically.

Do not assume the current configuration is valid just because it looks syntactically correct.
Check whether the behavior actually matches the intended effect, whether there are conflicting settings, precedence issues, environment-specific pitfalls, or hidden defaults.

Identify the root cause and produce a proper fix rather than adding more config on top of a broken setup.
```

---

# 6）文档编写

## 18. 工程文档标准版
**用途**：让 AI 写出来的文档不是空话，而是工程上能交付。  
**适合**：技术方案、部署文档、运维手册、README。

```text
Write this like an experienced engineer writing for real delivery.

Do not produce vague or generic documentation.
Make it concrete, structured, accurate, and operationally useful.

Follow common engineering documentation conventions:
- clear purpose,
- assumptions and prerequisites,
- step-by-step instructions where needed,
- risks and caveats,
- validation steps,
- troubleshooting guidance if relevant.

Prefer practical clarity over polished but empty wording.
```

## 19. README / 使用说明版
**用途**：写 README、安装说明、项目说明时很好用。  
**适合**：GitHub 仓库、工具说明、内部项目文档。

```text
Write this as a high-quality engineering README.

Make it clear, concise, and practical.
Include the information a real user or maintainer would need:
- what this is,
- why it exists,
- how to install or run it,
- configuration and prerequisites,
- common usage examples,
- limitations or caveats where relevant.

Do not write generic filler.
Use professional judgment to keep it useful and grounded.
```

## 20. 运维 Runbook 版
**用途**：写值班手册、故障处理 SOP、操作手册。  
**适合**：线上排障、重启、巡检、应急操作文档。

```text
Write this as an operational runbook for engineers.

Assume the reader may need to execute it under pressure.
Make it explicit, ordered, and action-oriented.

Include:
- purpose and scope,
- prerequisites,
- exact steps,
- expected results,
- verification steps,
- rollback or recovery guidance where relevant,
- warnings for risky actions.

Do not make assumptions silently.
Document critical details clearly.
```

---

# 7）测试补全

## 21. 有效测试补全版
**用途**：让 AI 补测试时不是为了覆盖率而覆盖率，而是真测关键行为。  
**适合**：单元测试、集成测试、接口测试。

```text
Add meaningful tests like a senior engineer.

Do not add superficial tests just to increase coverage.
Focus on behavior, correctness, edge cases, failure cases, regression protection, and important assumptions.

Use professional judgment to determine what is actually worth testing.
Prefer tests that would catch real bugs and future regressions.
```

## 22. 回归保护测试版
**用途**：修 bug 后，要求 AI 顺手补一组能防止以后再犯的测试。  
**适合**：bugfix 后补测试。

```text
After fixing the bug, add regression tests that would have caught this issue earlier.

Do not write shallow happy-path-only tests.
Cover the failing scenario, important edge cases, and the expected behavior after the fix.

Make sure the tests validate the real root-cause correction, not just the visible symptom.
```

## 23. 测试设计思维版
**用途**：先让 AI 想清楚测试策略，再开始写测试。  
**适合**：复杂模块、逻辑较多、你怕它乱测。

```text
Before writing tests, think through the test strategy.

Identify:
- the critical behaviors,
- the main failure modes,
- the edge cases,
- the assumptions that must hold,
- the scenarios most likely to regress in the future.

Then implement a focused, maintainable test suite.
Do not generate noisy or redundant tests.
```

---

# 万能通用前缀

## 24. 万能工程增强版
**用途**：你懒得分场景时，直接用这一条。  
**适合**：写代码、改配置、修 bug、写文档、补测试，几乎都能套。

```text
Act like a senior engineer, not a literal instruction executor.

Before making changes, evaluate whether the requested approach is actually reasonable.
Check it against industry conventions, best practices, maintainability, and production safety.

Use your professional judgment to challenge incorrect assumptions, weak designs, and fragile implementations.
If the current direction or recent changes are flawed, discard them rather than patching around them.

Identify the root cause first.
Then implement a proper fix systematically.
Prefer clear, robust, maintainable solutions over quick hacks or symptom-level patches.

If a trade-off is necessary, state it briefly and choose the most professional default.
```

---

# 6 句高频“补刀句”

## 25
```text
Do not follow the instruction literally if the instruction itself is flawed.
```
**作用**：防止 AI 机械执行错误需求。

## 26
```text
Challenge the premise if needed.
```
**作用**：允许 AI 质疑前提，不要太听话。

## 27
```text
Fix the root cause, not the visible symptom.
```
**作用**：防止表面修复。

## 28
```text
Do not preserve a broken design just to minimize edits.
```
**作用**：防止为了少改几行而保留坏结构。

## 29
```text
Choose the professional default unless I explicitly ask for a shortcut.
```
**作用**：默认走专业方案，不走投机方案。

## 30
```text
If the previous change was wrong, revert the idea, not just the code.
```
**作用**：不只是回滚字面改动，而是回滚错误思路。

---

# 你直接套用的模板

## 模板 A：最通用
```text
Act like a senior engineer, not a literal instruction executor.

Before making changes, evaluate whether the requested approach is actually reasonable.
Check it against industry conventions, best practices, maintainability, and production safety.

Use your professional judgment to challenge incorrect assumptions, weak designs, and fragile implementations.
If the current direction or recent changes are flawed, discard them rather than patching around them.

Identify the root cause first.
Then implement a proper fix systematically.
Prefer clear, robust, maintainable solutions over quick hacks or symptom-level patches.

Now here is my task:
[把你的需求写这里]
```

## 模板 B：修 Bug
```text
Act like a senior engineer debugging a production issue.

Before changing anything, verify whether the current implementation is conceptually correct and whether the recent changes are based on a sound approach.

Do not patch around symptoms.
Identify the root cause first, then implement a proper fix systematically.

If the current direction or recent change is flawed, discard it rather than layering more fixes on top of it.

Prefer a clean, maintainable, production-safe solution over a quick workaround.

Now here is the bug:
[把你的 bug 描述、报错、日志、代码贴这里]
```

## 模板 C：最佳方案设计 / 功能实现
```text
Act like a senior engineer designing the best implementation approach for a new feature.

Do not jump straight to coding.
First clarify the requirement, constraints, trade-offs, module boundaries, interfaces, and data flow.

Then propose the most reasonable implementation approach based on industry conventions, maintainability, extensibility, and production safety.

If there are multiple viable options, compare them briefly and recommend the best one.
Only after that provide the final implementation plan or code.

Now here is the feature request:
[把你的功能需求、背景、约束贴这里]
```

## 模板 D：改配置
```text
Treat this as a production engineering task.

Before changing the configuration, verify whether the requested approach is operationally sound, aligned with common industry conventions, and safe for production use.

Do not apply mechanical edits.
Use professional judgment to identify flawed assumptions, hidden risks, and configuration drift.

If the current configuration or recent change is flawed, discard it and fix the root cause systematically.
Prefer a clean, explicit, maintainable, production-safe configuration.

Now here is the configuration task:
[把你的配置需求和配置内容贴这里]
```

## 模板 E：补测试
```text
Add meaningful tests like a senior engineer.

Do not add superficial tests just to increase coverage.
Focus on behavior, correctness, edge cases, failure cases, regression protection, and important assumptions.

Use professional judgment to determine what is actually worth testing.
Prefer tests that would catch real bugs and future regressions.

Now here is the code to test:
[把代码和测试要求贴这里]
```

---

# 实战建议

平时实际用的时候，最好在增强提示词后面再补 1 句约束，效果会更稳。

例如：

```text
Show your reasoning briefly, then give the final implementation.
```

或者：

```text
Explain the root cause first, then provide the final corrected version.
```

或者：

```text
Return the final result in a directly usable form.
```

这三句很实用，因为它们能让 AI：

- 先解释，不要乱改
- 最后输出可直接使用的结果
- 少一点空话，多一点交付物

---

