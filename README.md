# Smart Execution V1

Author: Kevin KE  
GitHub: [https://github.com/KevinKE93](https://github.com/KevinKE93)

## English

Smart Execution V1 is a lightweight execution skill for AI agents. It is for tasks where guessing is not good enough.

When a request is vague, multi-step, tied to existing files, quality-sensitive, or risky to change, an agent should slow down before acting. It should inspect the real context, decide what success means, take the smallest useful path, and verify the result.

Smart Execution V1 gives the agent that working rhythm.

### What It Improves

- Fewer guesses before checking the actual context
- Clearer success criteria for subjective or quality-sensitive work
- Smaller, more focused changes
- Less unnecessary refactoring or scope drift
- Better verification before reporting completion
- Clearer final reports: what changed, what was checked, and what risk remains

The goal is not to add ceremony. The goal is to make the agent more careful when mistakes are costly.

### When To Use

Use it for tasks that are:

- ambiguous or underspecified
- multi-step
- dependent on existing project context
- quality-sensitive
- risky to change or expensive to undo
- likely to need testing, verification, or iteration

Do not use it for simple facts, tiny rewrites, one-command tasks, or cases where a more specific skill already gives the right workflow.

### How It Works

The skill uses a compact loop:

1. Understand the goal and constraints.
2. Inspect real context before making claims.
3. Define success criteria when quality matters.
4. Choose the smallest path that can solve the task.
5. Act in focused steps.
6. Verify with practical evidence.
7. Report clearly.
8. Save reusable learning only when it is genuinely useful.

### Install

For Codex, copy this folder into:

```text
~/.codex/skills/smart-execution-v1/
```

For other agent hosts, load `SKILL.md` as the canonical instruction file. Optional adapters are included for Claude and Gemini:

```text
.claude/commands/smart-execution-v1.md
.gemini/commands/smart-execution-v1.toml
```

### Usage

Codex-style:

```text
[$Smart Execution V1](/Users/kevinke/.codex/skills/smart-execution-v1/SKILL.md)
```

Natural language:

```text
Use Smart Execution V1 for this task.
```

### License

MIT License. See [LICENSE](LICENSE).

## 中文

Smart Execution V1 是一个轻量级的 AI agent 执行 skill，适合那些不能靠猜的任务。

当需求不够清楚、步骤较多、依赖已有文件、对质量有要求，或者改错了会比较麻烦时，agent 不应该急着下结论或直接改文件。它应该先看真实上下文，想清楚什么算完成，再用最小有效路径推进，并验证结果。

Smart Execution V1 提供的就是这种工作节奏。

### 它改善什么

- 少凭感觉猜，多先看真实上下文
- 质量敏感的任务先说清楚成功标准
- 改动更小、更集中
- 减少不必要的重构和跑偏
- 完成前做更可靠的验证
- 汇报更清楚：改了什么、检查了什么、还剩什么风险

它的目标不是增加流程，而是在容易出错、改错成本高的时候，让 agent 更稳。

### 适合什么时候用

适合用于这些任务：

- 需求含糊或信息不足
- 需要多个步骤完成
- 依赖已有项目上下文
- 对质量、风格或判断标准敏感
- 修改有风险，或回滚成本较高
- 需要测试、验证或迭代

不建议用于简单事实回答、很小的文字改写、单条命令即可完成的任务，或已有更专业 skill 能覆盖完整流程的场景。

### 它怎么工作

这个 skill 使用一个紧凑的执行闭环：

1. 理解目标和约束。
2. 先检查真实上下文，再做判断。
3. 质量敏感时，先定义成功标准。
4. 选择最小但能解决问题的路径。
5. 用集中的步骤推进。
6. 用实际证据验证。
7. 清楚汇报结果。
8. 只有在经验确实可复用时，才沉淀记录。

### 安装

在 Codex 中，将本文件夹复制到：

```text
~/.codex/skills/smart-execution-v1/
```

在其他 agent host 中，可将 `SKILL.md` 作为核心指令文件加载。本仓库也提供 Claude 和 Gemini 的可选适配文件：

```text
.claude/commands/smart-execution-v1.md
.gemini/commands/smart-execution-v1.toml
```

### 使用

Codex 风格调用：

```text
[$Smart Execution V1](/Users/kevinke/.codex/skills/smart-execution-v1/SKILL.md)
```

自然语言调用：

```text
Use Smart Execution V1 for this task.
```

### 许可证

MIT 许可证。详见 [LICENSE](LICENSE)。
