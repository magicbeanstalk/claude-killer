---
name: setup-check
description: Checks an Antigravity workspace for Gemini 4 Neon on High, git, Node.js, Python, project rules, and browser testing. Use when setting up Antigravity, starting a new project, or when the user asks for a setup check.
---

# Setup check

Read [prompts/01-setup-check.md](../../../prompts/01-setup-check.md) and run that checklist. Do not reinstall tools that already work.

## Steps

1. Report the model and thinking level in this chat. The target is Gemini 4 Neon on High. If this chat is on something else, say exactly where to switch it. Do not pretend you switched it.
2. Check `git`, `node`, and `python` (or `python3`) with version commands. If one is missing, name it and ask before installing.
3. Confirm `AGENTS.md` at the workspace root already contains the four project rules (visual quality, no em dashes, ask before destructive actions, 3-line close). If a rule is missing, add only the missing line.
4. Open one local or public web page with the browser tools. If the browser needs an extension or a setting, give the click path. Do not skip the check.
5. Close with three lines: what is ready, what the user must do, what to try first (usually `/first-app`).

## Hand settings

Tell the user once if you cannot verify them from the chat:

- Permission preset: Auto
- Queued messages: Send immediately
- Prevent sleep: On
- Remote control: On
- Neon needs Google AI Pro or Ultra on the signed-in account
