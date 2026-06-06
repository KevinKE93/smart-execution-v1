---
name: Smart Execution V1
description: Use Smart Execution V1 when a task is ambiguous, multi-step, quality-sensitive, context-dependent, risky to change, or likely to require trade-offs, verification, iteration, or reusable learning. Helps Codex inspect real context, define success criteria, choose the smallest effective path, execute, verify, report clearly, and capture durable learning only when appropriate. Do not use for simple direct answers, trivial one-command tasks, or when a narrower specialist skill fully covers the work.
---

# Smart Execution V1

Use this skill as a lightweight execution discipline for non-trivial work. It should improve judgment and follow-through without turning ordinary tasks into ceremony.

This skill does not replace system, developer, user, safety, repository, or specialist-skill instructions. When a narrower skill applies, use that skill for domain-specific procedure and use Smart Execution V1 only to coordinate scope, criteria, verification, and reporting.

## Trigger Boundary

Use this skill when at least one condition is true:

- The request is ambiguous, multi-step, or depends on unstated assumptions.
- The result is subjective or quality-sensitive, such as UI, writing, architecture, product judgment, prioritization, review, or evaluation.
- The task depends on existing code, docs, tools, skills, agents, configs, environment state, or project conventions.
- The work has meaningful trade-offs, rollback cost, user-facing impact, or high chance of scope drift.
- The task should produce durable learning, a reusable workflow, or a repeatable verification path.

Do not use this skill when:

- The user asks for a simple fact, translation, rewrite, command output, or tiny local edit.
- A direct answer is clearly enough.
- A specialist skill provides a complete workflow and no extra coordination is needed.
- The user explicitly asks to skip planning or only wants a quick answer.

## Operating Posture

For simple tasks, answer or act directly.

For non-trivial tasks, avoid both extremes: do not act blindly, and do not over-plan. Build only enough understanding to choose the next useful action, then execute in small verifiable steps.

If the user clearly asks for implementation, default to implementing after the necessary inspection. Do not stop at a plan unless the user requested a plan, approval, or decision point.

## Execution Loop

1. Understand
   Identify the goal, deliverable, constraints, known facts, unknowns, and assumptions. Ask a question only when the missing answer would materially change the result, waste substantial work, or create irreversible risk.

2. Inspect
   Check the real sources before making project-specific claims: relevant files, docs, configs, scripts, tests, prior conventions, installed skills, tool availability, runtime state, and user-provided artifacts.

3. Define
   For subjective or quality-sensitive work, define success criteria before creating or judging. Keep criteria contextual and observable, not taste-based.

4. Prioritize
   Separate must-have, should-have, and nice-to-have work. Execute must-haves first and defer optional improvements unless they are cheap and clearly increase quality.

5. Plan
   Create the shortest useful plan. Include the next concrete actions, the main risk, and the intended deliverable. Skip visible planning when it would not help the user.

6. Act
   Make small, coherent changes. Prefer existing project patterns and specialist tools over new abstractions. Keep scope tied to the user's goal.

7. Check
   Verify against the goal and criteria using the strongest practical evidence: tests, builds, screenshots, rendered artifacts, command output, source inspection, or reasoned comparison. State any gap that remains.

8. Report
   Summarize what changed, what was verified, and any residual risk. Keep the final answer shorter than the work log.

9. Capture
   Record reusable knowledge only when appropriate. Update durable docs, memory, or workflow notes only when the user asked for it, the project already expects it, or the finding is clearly useful for future similar work.

## Subjective Quality

When the user asks for something better, cleaner, more professional, more beautiful, more usable, or similarly subjective, define quality in context before evaluating or producing the result.

Useful criteria often include:

- Supports the user's primary task.
- Has clear hierarchy and reduces cognitive load.
- Fits the product, audience, and existing design or writing style.
- Uses consistent structure, spacing, typography, naming, or tone.
- Handles important states, edge cases, and constraints.
- Is feasible to implement and maintain.
- Can be checked with concrete evidence.

Do not claim subjective quality as fact without criteria and evidence.

## Calibration

Stay evidence-backed:

- Do not claim certainty without evidence.
- Do not invent files, tools, skills, agents, configs, or project conventions.
- Do not claim a project uses a pattern before inspecting the project.
- Do not treat one passing check as proof of broader correctness.
- When uncertain, say what the answer depends on and how you checked.

Useful phrasing:

- "Based on the current context..."
- "Assuming the goal is..."
- "The main trade-off is..."
- "I found no existing convention for this, so I used the smallest compatible approach..."
- "I verified X; Y remains unverified because..."

## Scope Control

Keep work focused:

- Prefer the smallest deliverable that genuinely satisfies the goal.
- Do not explore many weak alternatives when one strong path is enough.
- Do not introduce architecture, files, dependencies, or abstractions unless they directly serve the goal.
- Do not optimize nice-to-have details before must-have requirements are done.
- If the task grows too broad, reduce it to the smallest useful slice and make the trade-off explicit.

## Documentation And Memory

Capture reusable learning when it will likely help future work:

- New project conventions.
- Recurring commands, workflows, or verification paths.
- Architecture, product, or design decisions.
- Environment constraints or tool usage notes.
- Pitfalls future agents are likely to hit again.

Avoid capturing:

- Temporary observations.
- Obvious facts.
- Failed guesses.
- One-off implementation details.
- Information outside the user's requested scope.

When updating durable records, add concise notes, correct misleading instructions, and avoid destructive deletion unless the user asked for it or the change is clearly safe.

## Cross-Agent Adapters

This package includes lightweight adapters for other agent hosts:

- `.claude/commands/smart-execution-v1.md` for Claude Code slash-command use.
- `.gemini/commands/smart-execution-v1.toml` for Gemini command use.

The adapters should point back to this `SKILL.md` as the canonical source. Keep this file authoritative to avoid drift across hosts.

## User-Facing Output

Expose only the process that helps the user decide or trust the result.

For complex tasks, a concise shape can be:

```text
Goal: ...
Criteria: ...
Plan: ...
Result: ...
Check: ...
```

Use that structure only when helpful. For ordinary tasks, answer naturally and keep the reasoning internal.

## Anti-Patterns

Avoid:

- Acting before understanding the goal enough to proceed.
- Asking clarification questions when a reasonable assumption allows progress.
- Treating personal taste as objective quality.
- Producing long plans that do not improve execution.
- Expanding beyond the user's actual goal.
- Inventing conventions instead of checking the real context.
- Stopping at analysis when the user clearly asked for implementation.
- Over-documenting trivial or temporary information.
- Letting this skill override a more specific skill or explicit user instruction.
