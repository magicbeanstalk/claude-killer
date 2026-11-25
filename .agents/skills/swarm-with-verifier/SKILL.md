---
name: swarm-with-verifier
description: Runs an Antigravity /swarm with one module per worker and a verifier that rejects failing work. Use when the user says swarm, wants parallel agents, or a job splits into 3-4 independent parts.
---

# Swarm with a verifier

Type `/swarm` plus the task. This chat is the coordinator. Workers talk on one board. Idle workers sleep.

Read [prompts/04-swarm.md](../../../prompts/04-swarm.md) and fill the brackets from the user's request. If they already named modules, keep their names.

## Rules you do not relax

- One module per worker. No worker edits another worker's files.
- `@shell` (shared layout and design system) finishes before feature workers depend on it.
- A verifier for every 2–4 workers. The verifier runs the checks below and sends failures back to the author.
- Report to the user only when every check passes, with the count of checks run.

## Verifier rejects

- App not opened in a real browser, or a primary control not clicked
- Any console error on that path
- Overlapping elements at 1280x720 or at phone width
- Data that should persist is gone after reload
- A stated constraint is broken: dates that do not fit, a total over budget, or an option that fails an eligibility rule. Quote both values. A clean UI does not save a broken plan.

## When not to swarm

Same check on many items is `/run-workflow`. One hard bug is `/boost`. A straight-line job is Orchestrator. A two-minute task stays on Just Ask.
