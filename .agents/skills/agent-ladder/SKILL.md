---
name: agent-ladder
description: Picks the cheapest Antigravity agent mode that can finish the job, and says when to skip a rung. Covers Just Ask, sub-agents, Orchestrator, workflows, swarm, boost, and teamwork. Use when the user asks which mode, /swarm, /boost, /run-workflow, /teamwork, or how to run agents.
---

# Agent ladder

Start at the bottom. Move up only when the rung below cannot do the job. Higher rungs spend more quota. Paste-ready lines are in [prompts/03-ladder.md](../../../prompts/03-ladder.md).

| Rung | Command | Use when | Skip it when |
| --- | --- | --- | --- |
| 1. Just Ask | none | One agent, one chat. Rewrite, small fix, short answer. | The job has many different parts. |
| 2. Sub-agents | invoke a helper | One side job while the main task continues. Often happens on its own. | The helper would be doing the whole project. |
| 3. Orchestrator | model menu | One bigger job that needs a plan. Neon plans, Hydrogen does routine work. Show the plan first. | It is a quick question. Planning only adds delay. |
| 4. Workflows | `/run-workflow` | The same check on many items, now and again next week. | There is one item, or each item needs a different kind of work. |
| 5. Swarm | `/swarm` | Different jobs that must fit together. Use `swarm-with-verifier`. | The work cannot be split, or it takes a couple of minutes. Quota heavy. |
| 6. Boost | `/boost` | One hard problem, usually a bug. Paid plan. Prove it with a test that failed and now passes. | The job is broad. Many parts belong on swarm. Skip it if you are not fixing code. |
| 7. Teamwork | `/teamwork-preview` | Hours or days. Paid plan, preview. | You need the result today, or the job is small. |

## Workflows

Show the script and wait for a yes before it runs. Cap the first run at about 20 items. If the last step fails, let the agent fix its own script and ask again. Save the workflow so the next batch is a rerun on a new folder.

## Teamwork

The user says what they want. The interview includes what the team must not do. Write a done checklist and wait for a yes before any work starts. Check real sources. Do not invent facts.

## Decide

1. Name the rung you picked and the rung you skipped, using the skip column.
2. Same check on many items is a workflow. Different jobs that must fit together are a swarm.
3. If two steps do not pass data to each other, run them side by side.

## Side thread

`/btw` asks a side question while the main agent keeps working. It only appears while the agent is busy. If the side thread is useful, promote it back into the main work. Do not use it as the verifier.

## After

End a session that taught you something with `/learn`. Approve the proposed rule or skill before it is saved. `/grill-me` plus `/plan` before a large build. `/goal` when the job should continue until a check passes.
