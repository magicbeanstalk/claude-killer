# Antigravity skills and prompts

A workspace library for [Google Antigravity](https://antigravity.google/), taken from codila's course [Google Antigravity + Gemini 4 Neon](https://x.com/0xCodila/status/2125623560689369440). Open this folder as an Antigravity project. The app loads `AGENTS.md`, `.agents/rules/`, `.agents/skills/`, and `.agents/agents/` on its own.

Neon needs a paid Google AI Pro or Ultra plan on the account you sign in with.

## Five-minute setup

1. Download Antigravity from [antigravity.google](https://antigravity.google/) and sign in.
2. Settings: Permission preset → Auto, Queued messages → Send immediately, Prevent sleep → On, Remote control → On.
3. New project → this folder. Model: Gemini 4 Neon on High.
4. In chat, type `/setup-check`.

Non-coders: Settings → General → Interface layout → Knowledge work.

## Skills

Type `/` plus the name, or describe the job and let the agent pick.

| Skill | What it does |
| --- | --- |
| `/setup-check` | Neon on High, git, Node, Python, rules, browser |
| `/first-app` | One polished app, launched, then proven |
| `/agent-ladder` | Just Ask through Teamwork, including when to skip a rung |
| `/swarm-with-verifier` | Parallel modules plus a verifier for UI and real constraints |
| `/proof-before-done` | Open it, click it, check the constraints, then say done |
| `/ui-from-screenshot` | A screenshot and one sentence, then a clickable mock |
| `/readonly-reviewer` | Bugs and risk only. No file edits |
| `/software-factory` | Lead, builders, read-only reviewer and checker |
| `/sleep-staff` | Remote agents, `/automation`, phone control |
| `/three-model-swarm` | Neon builds, Claude verifies, GPT checks risk |
| `/model-council` | Three models, anonymous ranking, one recommendation |
| `/neon-team-architect` | Grill, graph, quality loop, weekly improvement |

Subagents already in the repo: `reviewer` and `checker`.

## Prompts

The same course, as copy-paste text, is in [prompts/](prompts/README.md). Prompts 8 and 9 are for Claude Code. The rest are for Antigravity.

## One evening

1. `/setup-check` (10 min)
2. `/first-app` on something you would actually use (20 min)
3. `/swarm-with-verifier` on a real task (30 min)
4. `/learn` so the corrections become a rule (2 min)
5. `/sleep-staff` for one Monday automation (5 min)

Add a second model the next day with `/three-model-swarm`.

## How the pieces map to the course

- **7 rungs, including when to skip one,** live in `agent-ladder` and [prompts/03-ladder.md](prompts/03-ladder.md).
- **Constraint checks** (dates, budget, eligibility) sit on the `checker` subagent, `swarm-with-verifier`, and `proof-before-done`.
- **Screenshot plus one sentence** is `ui-from-screenshot`.
- **Project rules** from prompt 1 are already in [AGENTS.md](AGENTS.md), so they apply to every chat.
- **Model choice** (Hydrogen, Neon, Carbon, Orchestrator) is in [.agents/rules/model-routing.md](.agents/rules/model-routing.md). The agent reads it when a task is about picking a model.
- **`/learn`** is Antigravity's own command. Use it at the end of a session. It proposes a new skill or rule. You approve it before anything is saved.
