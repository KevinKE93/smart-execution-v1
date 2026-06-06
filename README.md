# Smart Execution V1

Author: Kevin KE  
GitHub: [https://github.com/KevinKE93](https://github.com/KevinKE93)

## English

Smart Execution V1 is a lightweight Codex skill for tasks where guessing is not good enough.

Some requests are simple. Others are vague, multi-step, tied to an existing codebase, sensitive to quality, or risky to change. In those cases, an agent should not jump straight into an answer or edit files based on assumptions. It should pause, inspect the real context, decide what success looks like, make the smallest useful move, and verify the result.

That is what Smart Execution V1 is for.

### Why It Helps

Smart Execution V1 gives Codex a practical working rhythm:

- understand the actual goal before acting
- check real files, tools, docs, errors, or runtime state before making claims
- define success criteria when quality or judgment matters
- avoid unnecessary refactors and side quests
- make focused changes in small steps
- verify with real evidence
- report clearly what was done, what was checked, and what risk remains

The value is not more process. The value is better judgment at the moments where mistakes are expensive.

It is especially useful when a task has hidden assumptions, project conventions, uncertain requirements, side effects, or rollback cost. It helps the agent stay useful without becoming reckless.

### When To Use It

Use Smart Execution V1 for tasks that are:

- ambiguous or underspecified
- multi-step
- quality-sensitive
- dependent on existing project context
- risky to change or expensive to undo
- likely to need testing, verification, or iteration

Do not use it for simple facts, tiny rewrites, one-command tasks, or cases where a more specific skill already has the right workflow.

### How It Works

Smart Execution V1 guides the agent through a compact loop:

1. Understand the goal, constraints, assumptions, and unknowns.
2. Inspect the real context before making project-specific claims.
3. Define success criteria when the result is subjective or quality-sensitive.
4. Prioritize what must be done before optional improvements.
5. Choose the smallest path that can actually solve the task.
6. Act in small, coherent steps.
7. Verify with the strongest practical evidence available.
8. Report the outcome clearly.
9. Capture reusable learning only when it is genuinely useful.

This skill is intentionally lightweight. It does not include a runtime, schemas, or external tool integration. It is a behavioral guide for agents that already have access to local files, shell commands, tests, browser tools, or other host capabilities.

### Install

Copy this folder into your Codex skills directory:

```text
~/.codex/skills/smart-execution-v1/
```

The required file is:

```text
SKILL.md
```

Optional host adapters are included for Claude and Gemini command-style usage:

```text
.claude/commands/smart-execution-v1.md
.gemini/commands/smart-execution-v1.toml
```

Restart Codex after installation so the skill list refreshes.

### Usage

In Codex-style skill syntax:

```text
[$Smart Execution V1](/Users/kevinke/.codex/skills/smart-execution-v1/SKILL.md)
```

Or ask naturally:

```text
Use Smart Execution V1 for this task.
```

### License

MIT License. See [LICENSE](LICENSE).

## 中文

Smart Execution V1 是一个轻量级 Codex skill，适合那些“不能靠猜”的任务。

有些请求很简单，直接回答就行。但有些任务不一样：需求还不够清楚、步骤比较多、依赖现有代码或文件、对质量有要求，或者改错了会比较麻烦。遇到这种情况，agent 不应该上来就给结论，也不应该凭感觉直接改文件。它应该先停一下，看清楚真实上下文，想清楚什么算完成，再用最小有效步骤推进，并且做完后验证。

Smart Execution V1 解决的就是这个问题。

### 它的价值

Smart Execution V1 给 Codex 一个更稳的工作节奏：

- 先弄清楚用户真正要什么，再开始动手
- 先看真实文件、工具、文档、报错或运行状态，再做判断
- 遇到质量敏感或主观判断时，先定义成功标准
- 避免不必要的重构、扩展和跑偏
- 用小而集中的步骤推进
- 用真实证据验证结果
- 最后说清楚做了什么、检查了什么、还剩什么风险

它的价值不是增加流程，而是在容易出错、改错成本高的时候，让 agent 更有判断力。

当任务里有隐藏假设、项目约定、不确定需求、潜在副作用，或者回滚成本时，这个 skill 会特别有用。它能让 agent 保持行动力，但不鲁莽。

### 适合什么时候用

适合用于这些任务：

- 需求含糊或信息不足
- 需要多个步骤完成
- 对质量、风格或判断标准敏感
- 依赖已有项目上下文
- 修改有风险，或回滚成本较高
- 需要测试、验证或迭代

不建议用于简单事实回答、很小的文字改写、单条命令即可完成的任务，或已有更专业 skill 能覆盖完整流程的场景。

### 它怎么工作

Smart Execution V1 会引导 agent 走一个紧凑的执行闭环：

1. 理解目标、约束、假设和未知点。
2. 在做项目相关判断前，先检查真实上下文。
3. 当结果带有主观性或质量敏感时，先定义成功标准。
4. 先处理必须完成的事项，再考虑可选优化。
5. 选择最小但真正能解决问题的路径。
6. 以小而连贯的步骤执行。
7. 使用当前最强、最实际的证据进行验证。
8. 清楚汇报结果。
9. 只有在经验确实可复用时，才沉淀为长期记录。

这个 skill 有意保持轻量。它不包含 runtime、schema 或外部工具集成，而是一份行为指南，适合已经能使用本地文件、命令行、测试、浏览器工具或其他宿主能力的 agent。

### 安装

将本文件夹复制到 Codex skills 目录：

```text
~/.codex/skills/smart-execution-v1/
```

必需文件是：

```text
SKILL.md
```

可选提供 Claude 和 Gemini 的命令式适配文件：

```text
.claude/commands/smart-execution-v1.md
.gemini/commands/smart-execution-v1.toml
```

安装后重启 Codex，让 skill 列表刷新。

### 使用

使用 Codex 风格的 skill 调用语法：

```text
[$Smart Execution V1](/Users/kevinke/.codex/skills/smart-execution-v1/SKILL.md)
```

也可以自然语言调用：

```text
Use Smart Execution V1 for this task.
```

### 许可证

MIT 许可证。详见 [LICENSE](LICENSE)。
