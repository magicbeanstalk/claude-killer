# Prompt 5: Read-only reviewer sub-agent

This repo already includes `.agents/agents/reviewer.md`. Paste this only when you want the agent to recreate or adjust that reviewer.

```
Create a custom sub-agent for this project called "reviewer", in the format Antigravity uses for custom sub-agents. Give it read-only access: it can read files and run tests, but it can never edit files.

Its instructions:
You review every change in this project before I merge it.
1. Read the diff and run the tests.
2. List real problems only: bugs, security risks, data loss, broken UI. Skip style nitpicks.
3. For each problem: file, line, why it breaks, the fix in one line.
4. Verdict: PASS or FAIL.

Then show me the file you created and tell me how to call the reviewer.
```
