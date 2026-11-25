---
name: readonly-reviewer
description: Reviews a diff for bugs, security risks, data loss, and broken UI without editing files. Use before merge, when the user asks for a review, or when invoking the reviewer subagent.
---

# Read-only reviewer

The subagent is `.agents/agents/reviewer.md`. Invoke it, or follow this yourself if you are that agent. Do not edit files.

Source prompt: [prompts/05-reviewer.md](../../../prompts/05-reviewer.md).

## Review

1. Read the diff. Run the tests.
2. Report real problems only: bugs, security risks, data loss, broken UI. Skip style.
3. Each problem: file, line, why it breaks, the fix in one line.
4. End with `PASS` or `FAIL`.

A clean review is a short PASS, not a list of compliments.
