# Prompt 8: GPT + Claude + Gemini as one team

Paste into Claude Code when Claude Code is home base. Antigravity users who stay in this app should use Prompt 7 instead.

Claude plans and writes. Gemini gives an independent second plan and makes images, video, music, and voice-over. GPT does heavy backend work in a sandbox and reviews before merge.

```
Set up an AI team on this computer. You (Claude Code) are the lead. Gemini 4 Neon is your advisor and media team. GPT is your builder and reviewer. I only talk to you; you call the other two yourself.

1. CHECK: detect my OS and what is already installed (Node.js, Codex CLI, gemini-api CLI).
2. INSTALL: OpenAI's Codex CLI (github.com/openai/codex) and Google's Gemini API CLI (github.com/google-gemini/gemini-api-cli). Use only the install steps from their official READMEs.
3. SIGN IN: tell me exactly what to type in a separate terminal window: run "codex" and choose "Sign in with ChatGPT", then set up gemini-api with my Google AI Studio key the way its README says. Never ask me to paste a key or password into this chat.
4. MODELS: run "gemini-api models list --all" and check the Codex model list. Use the exact IDs for Gemini 4 Neon and the strongest GPT my plan offers. If one is missing, tell me and use the closest.
5. HELPERS: create two scripts in ~/.ai-team/bin and add them to PATH:
- ask-gemini "task" [files]: sends the task and files to Gemini 4 Neon. Read-only. With --image, --video, --music or --voice it calls the matching gemini-api command and saves the file to ./assets.
- ask-gpt "task": runs Codex in that folder in the workspace-write sandbox, never full access. For reviews, read-only.
6. RULES: add an "AI team" section to ~/.claude/CLAUDE.md:
- Small edits: do them yourself.
- Big plans: write yours, and at the same time send my original words (not your draft) to ask-gemini. Check every claim before you trust it, merge both plans, and tell me what you took from each.
- Backend and data work with a fixed interface: send it to ask-gpt with the interface and acceptance tests. Read its diff and run the tests yourself.
- Images, video, music and voice-over for the project: ask-gemini with the matching flag.
- Before every merge, ask-gpt reviews the diff. Only money, data loss, permissions, messages to other people and broken releases block it. Max 2 rounds, then ask me.
- Report in plain words: what's done and what I'll see.
7. TEST: run one small task through the whole team (plan a simple to-do app and make its icon) and show me who did what.

Done means: both tools work, the scripts run, the rules are in CLAUDE.md and the test passed. Stop and ask only when you need my sign-in or before anything that costs money beyond my plans
```
