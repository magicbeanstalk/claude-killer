# Prompt 9: Model council before a big decision

Paste into Claude Code after Prompt 8. Inside Antigravity, use the `model-council` skill, which runs the same council with the model picker and does not change files.

```
Before we decide, run a council. The question: [your question, e.g. "Which stack should I use for this app?" or "Is this plan safe to ship?"]

1. Ask three models the same question separately, so none sees the others: you (Claude), Gemini 4 Neon through ask-gemini, and GPT through ask-gpt in read-only mode. Give all three the same context files.
2. Remove the names, label the answers A, B and C, and send all three back to each model. Ask each one to rank them and point out the weakest claim in each.
3. As chairman, write the final answer: where all three agree, where they disagree and why, and your recommendation in 3 lines.
4. Show me the three original answers under the summary.

Don't change any files. If a claim can be checked (a price, a command, a version), check it before it goes into the final answer.
```
