---
name: sleep-staff
description: Sets up Antigravity work that continues after the laptop closes, using remote agents, /automation, and phone control. Use when the user wants a schedule, Monday report, overnight job, or agents that run while they are away.
---

# Work while you sleep

Three different tools. Pick one.

| Need | Tool |
| --- | --- |
| One long job from a GitHub repo or Drive folder. Close the laptop. | Remote agent |
| A repeating plain-English schedule | `/automation` |
| Steer, approve, or start work from the phone | Remote control (Settings, scan the QR code) |

## Automation rules

Each run starts blank. It does not remember the last run. Put every input path, comparison file, and output path in the instruction.

Template: [prompts/06-monday-automation.md](../../../prompts/06-monday-automation.md).

- Name the timezone.
- Point at last week's report if the job compares weeks.
- Write the new report to `reports/[date].md`.
- Ask only before reading a folder the instruction did not already name.
- Tell the user runs can start up to 15 minutes late.
- Ask before creating the automation.

Prevent sleep must be On for local runs. Remote agents are the path that survives a closed laptop.
