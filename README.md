# Smart Execution V1

Smart Execution V1 is a lightweight Codex skill for handling work that should not be answered blindly: ambiguous requests, multi-step changes, quality-sensitive judgment, context-dependent implementation, or tasks that are risky to change.

Smart Execution V1 是一个轻量级 Codex skill，适合处理不应该直接猜测完成的任务：需求含糊、多步骤变更、质量敏感判断、依赖上下文的实现，或修改成本较高、存在风险的工作。

Author: Kevin KE  
GitHub: [https://github.com/KevinKE93](https://github.com/KevinKE93)

## Value / 价值

Smart Execution V1 gives an agent a practical execution discipline without turning every task into a heavy process. It helps the agent slow down at the right moments, inspect real context before making project-specific claims, define success criteria when quality matters, choose the smallest useful path, verify the result, and report what was actually checked.

Smart Execution V1 为 agent 提供一套务实的执行纪律，但不会把每个任务都变成沉重流程。它帮助 agent 在关键时刻放慢速度：先检查真实上下文，再做项目相关判断；在质量敏感时定义成功标准；选择最小有效路径；完成后验证结果，并清楚说明实际检查过什么。

This is most useful when a task has hidden assumptions, existing project conventions, possible side effects, or a meaningful cost if the agent guesses wrong.

当任务存在隐藏假设、既有项目约定、潜在副作用，或猜错会带来明显成本时，这个 skill 最有价值。

## When To Use / 适用场景

Use this skill when the task is:

适合在以下任务中使用：

- ambiguous or underspecified
- multi-step
- quality-sensitive
- dependent on existing files, tools, repository conventions, or runtime state
- risky to change or expensive to undo
- likely to require verification, iteration, or reusable learning

中文对应为：

- 需求含糊或信息不足
- 需要多个步骤完成
- 对质量、风格、判断标准敏感
- 依赖已有文件、工具、仓库约定或运行状态
- 修改有风险，或回滚成本较高
- 需要验证、迭代，或沉淀可复用经验

Do not use it for simple facts, tiny rewrites, trivial one-command tasks, or cases where a narrower specialist skill already provides the right workflow.

不建议用于简单事实回答、很小的文字改写、单条命令即可完成的任务，或已有更专业 skill 能覆盖完整流程的场景。

## How It Works / 工作方式

Smart Execution V1 guides the agent through a compact loop:

Smart Execution V1 会引导 agent 走一个紧凑的执行闭环：

1. Understand the goal, constraints, assumptions, and unknowns. / 理解目标、约束、假设和未知点。
2. Inspect real context before making project-specific claims. / 在做项目相关判断前，先检查真实上下文。
3. Define success criteria when the result is subjective or quality-sensitive. / 当结果带有主观性或质量敏感时，先定义成功标准。
4. Prioritize must-have work before optional improvements. / 先处理必须完成的事项，再考虑可选优化。
5. Plan the shortest useful path. / 制定最短但有效的执行路径。
6. Act in small, coherent steps. / 以小而连贯的步骤执行。
7. Verify with the strongest practical evidence. / 使用当前最强、最实际的证据进行验证。
8. Report what changed, what was checked, and what risk remains. / 汇报改了什么、验证了什么、还剩什么风险。
9. Capture durable learning only when it is clearly reusable. / 只有在经验明显可复用时，才沉淀为长期记录。

The skill is intentionally lightweight. It does not include a runtime, schemas, or external tool integration. It is a behavioral guide for agents that already have access to local files, shell commands, tests, browser tools, or other host capabilities.

这个 skill 有意保持轻量。它不包含 runtime、schema 或外部工具集成，而是一份行为指南，适合已经能使用本地文件、命令行、测试、浏览器工具或其他宿主能力的 agent。

## Install / 安装

Copy this folder into your Codex skills directory:

将本文件夹复制到 Codex skills 目录：

```text
~/.codex/skills/smart-execution-v1/
```

The required file is:

必需文件是：

```text
SKILL.md
```

Optional host adapters are included for Claude and Gemini command-style usage:

可选提供 Claude 和 Gemini 的命令式适配文件：

```text
.claude/commands/smart-execution-v1.md
.gemini/commands/smart-execution-v1.toml
```

Restart Codex after installation so the skill list refreshes.

安装后重启 Codex，让 skill 列表刷新。

## Usage / 使用

In Codex-style skill syntax:

使用 Codex 风格的 skill 调用语法：

```text
[$Smart Execution V1](/Users/kevinke/.codex/skills/smart-execution-v1/SKILL.md)
```

Or ask naturally:

也可以自然语言调用：

```text
Use Smart Execution V1 for this task.
```

## License / 许可证

MIT License. See [LICENSE](LICENSE).

MIT 许可证。详见 [LICENSE](LICENSE)。
