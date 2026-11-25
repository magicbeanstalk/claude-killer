---
name: software-factory
description: Splits work across factory-line subagents with read-only reviewers and a person in the manager seat. Use when the user wants a software factory, custom sub-agents, parallel reviewers, or intake-check-fix-report lines.
---

# Software factory

Each line is its own context window so the main chat stays small. You sit in the manager seat: open any worker, read its chat, message it, stop it if it drifts.

## Lines

| Line | Writes code? | Job |
| --- | --- | --- |
| Lead | Yes | The only agent the user talks to. Routes with if/then rules. |
| Builder | Yes | One module. Does not touch another builder's files. |
| Reviewer | No | `.agents/agents/reviewer.md`. Bugs, security, data loss, broken UI. |
| Checker | No | `.agents/agents/checker.md`. Browser proof before done. |

Reviewers and checkers stay read-only. Give them `view_file`, `grep_search`, and `run_command` only. A misspelled tool name can hang the subagent, so do not invent tool ids.

## When to add a line

A new subagent needs a single job, a done checklist, and a handoff. Put reusable procedure in `.agents/skills/<name>/SKILL.md` and point the agent's `skills` field at `skills/<name>`.

Parallel lines only when they do not need each other's output. If they do, the Lead sequences them.

## Close

Tell the user the file you created and how to call that agent (`invoke_subagent`, or by name from `/agents`).
