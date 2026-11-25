---
name: three-model-swarm
description: Runs one Antigravity swarm where Gemini 4 Neon builds, Claude Opus 5.5 verifies, and GPT reviews money, data, and permissions. Use when the user wants a second model, a council inside Antigravity, Claude checking Neon, or Prompt 7.
---

# Three models, one swarm

Nothing to install. Needs a paid plan whose picker includes Claude and GPT. Prompt: [prompts/07-three-model-swarm.md](../../../prompts/07-three-model-swarm.md).

## Assignment

- Workers: Gemini 4 Neon. One module each when the work splits. See `swarm-with-verifier`.
- Verifier: Claude Opus 5.5. It runs the done checks and sends failures back.
- Second verifier, only at the end: GPT-OSS-120b, or the strongest GPT in the picker. Scope is money, data, and permissions. It does not restyle the work.

## Report

Say what each model caught. If a model is missing from the picker, name the closest available model and use that. Do not invent a run.

`/btw` is a side thread while the main agent keeps going. Use it for a spot check, not for the verifier. If the side thread is worth keeping, promote it back into the main work.
