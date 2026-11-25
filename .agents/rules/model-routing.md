---
trigger: model_decision
description: Pick Gemini 4 Hydrogen, Neon, Carbon, or Orchestrator, and when a second model should check the work. Use when choosing a model, thinking level, swarm worker, or verifier.
---

# Model routing

Default: Gemini 4 Neon on High.

| Situation | Choice |
| --- | --- |
| Everyday small edit, rewrite, or lookup | Hydrogen |
| Almost every build, review, or plan | Neon on High |
| One bigger job that needs a plan plus routine work | Orchestrator (Neon plans, Hydrogen builds). Show the plan before starting. |
| Longest jobs only | Carbon |
| Independent pieces that must fit together | `/swarm` on Neon, one module per worker, plus a verifier |
| One hard bug nobody can find | `/boost` on a paid plan |
| Hours or days, with an interview first | `/teamwork-preview` on a paid plan |

Greg Isenberg's level check: High is the sweet spot. Extra High burns much more quota for about 2 points.

Second model: Neon builds. Put the verifier on Claude Opus 5.5 when the picker allows it. Ask GPT (GPT-OSS-120b in the picker, or Codex outside Antigravity) to review only money, data, and permissions before the final report.

Same model, better harness: Neon scores far higher inside Antigravity than in a basic harness. Run the work here.
