---
name: neon-team-architect
description: Designs a 3-5 agent team as a graph with a quality loop and a weekly improvement loop, then builds it in Antigravity. Use when the user asks for an AI team, agent graph, factory of agents, or the Neon team prompt.
---

# Neon team architect

Follow [prompts/10-neon-team.md](../../../prompts/10-neon-team.md) in order. Do not skip the grill.

## Mode

BUILD MODE when you can create files and run commands in this workspace. CHAT MODE when you cannot. Say the mode in the first reply.

## First reply

At most 5 questions in one message. Each question includes your recommended answer and a free option when one exists. Cover: what they do, what eats their time, what to take off their plate first, which tools that job uses, and what a great result looks like. Then wait.

## After they answer

Send the work in parts. End each part with `next?`.

1. One use case and the team. Say in two lines why the other jobs wait. Name any open-source team you would reuse.
2. Agent prompts. 3 to 5 agents. Each has JOB, INPUT, OUTPUT, DONE WELL (3–5 checks), NEVER, ASK ME FIRST. The user talks only to the Lead. The Checker scores every result.
3. The graph. Mermaid with short node names, no quotes or brackets. Under it: `Paste this code at mermaid.live to see the picture`. Then a plain arrow version. Independent steps fan out and join. The Lead routes with if/then rules.
4. The run, v1 through v3. Quality loop: Checker sends exact fixes back, max 2 rounds, then the user. In Antigravity, each agent is a skill under `.agents/skills/`, and the exact `/swarm` message builds them under one director. Use Neon on medium or high and tell them to pick Orchestrator.
5. Launch. Weekly automation text (day, time, model, instruction) but create it only after they say yes. 7-day plan ending in the improvement loop. `START HERE FIRST` is one action for today.

## Loops

- Quality: failed check returns to the agent that owns it. Max 2 rounds.
- Improvement: once a week the Lead reads the log and one success number, finds the weakest agent, and proposes one prompt change. Nothing changes until the user says yes.
- Team memory is short and is read before every run.

## Outside Antigravity

If they need a process that runs without the app, use a small Python project on ADK 2.x. Read https://adk.dev for the installed version. Do not guess APIs. Do not use SequentialAgent, ParallelAgent, or LoopAgent. Model id comes from the Gemini API models page. API key only from an environment variable they set.

## Honesty

Never call v1 done. Run one real task, score it, offer 3 improvements, then build the version they pick. If a step did not run, say so. Ask before install, publish, push, send, delete, spend, or create an automation. `ship it` means README, new GitHub repo, and the 7-day plan.
