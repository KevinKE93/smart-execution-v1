# Smart Execution V1

Smart Execution V1 is a lightweight Codex skill for handling work that should not be answered blindly: ambiguous requests, multi-step changes, quality-sensitive judgment, context-dependent implementation, or tasks that are risky to change.

Author: Kevin KE  
GitHub: [https://github.com/KevinKE93](https://github.com/KevinKE93)

## Value

Smart Execution V1 gives an agent a practical execution discipline without turning every task into a heavy process. It helps the agent slow down at the right moments, inspect real context before making project-specific claims, define success criteria when quality matters, choose the smallest useful path, verify the result, and report what was actually checked.

This is most useful when a task has hidden assumptions, existing project conventions, possible side effects, or a meaningful cost if the agent guesses wrong.

## When To Use

Use this skill when the task is:

- ambiguous or underspecified
- multi-step
- quality-sensitive
- dependent on existing files, tools, repository conventions, or runtime state
- risky to change or expensive to undo
- likely to require verification, iteration, or reusable learning

Do not use it for simple facts, tiny rewrites, trivial one-command tasks, or cases where a narrower specialist skill already provides the right workflow.

## How It Works

Smart Execution V1 guides the agent through a compact loop:

1. Understand the goal, constraints, assumptions, and unknowns.
2. Inspect real context before making project-specific claims.
3. Define success criteria when the result is subjective or quality-sensitive.
4. Prioritize must-have work before optional improvements.
5. Plan the shortest useful path.
6. Act in small, coherent steps.
7. Verify with the strongest practical evidence.
8. Report what changed, what was checked, and what risk remains.
9. Capture durable learning only when it is clearly reusable.

The skill is intentionally lightweight. It does not include a runtime, schemas, or external tool integration. It is a behavioral guide for agents that already have access to local files, shell commands, tests, browser tools, or other host capabilities.

## Install

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

## Usage

In Codex-style skill syntax:

```text
[$Smart Execution V1](/Users/kevinke/.codex/skills/smart-execution-v1/SKILL.md)
```

Or ask naturally:

```text
Use Smart Execution V1 for this task.
```

## License

MIT License. See [LICENSE](LICENSE).
