---
name: model-council
description: Runs an anonymous three-model council before a stack, design, or ship decision, then merges agreements and disagreements. Use when the user says council, second opinion, which stack, or whether a plan is safe to ship.
---

# Model council

Do this before a big decision. Do not change project files during the council.

Inside Antigravity, ask three available models separately (Neon, Claude Opus 5.5, GPT). Give them the same context. None sees the others' answers.

If this chat is Claude Code with `ask-gemini` and `ask-gpt` already installed, follow [prompts/09-model-council.md](../../../prompts/09-model-council.md) exactly. Prompt 8 in [prompts/08-claude-code-team.md](../../../prompts/08-claude-code-team.md) is the install path for that home base. Do not install those CLIs from an Antigravity session unless the user asks.

## Steps

1. Ask the question once per model. Same wording, same files.
2. Strip the names. Label answers A, B, and C.
3. Send all three back to each model. Each one ranks them and names the weakest claim in each.
4. As chairman, write where they agree, where they disagree and why, and a 3-line recommendation.
5. Show the three original answers under that summary.
6. If a claim is a price, a command, or a version, check it before it enters the final answer.

Say which models actually ran.
