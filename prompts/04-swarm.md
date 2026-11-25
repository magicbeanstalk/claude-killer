# Prompt 4: Swarm with verifier rules

Use when the job splits into 3 or 4 parts that do not depend on each other. One module per worker. Type `/swarm` and the task.

```
/swarm Build [project name]: [one-line description].

Workers, one module each, no one touches another's files:
- @shell: shared layout and design system, done first
- @[module-1]: [what it does]
- @[module-2]: [what it does]
- @[module-3]: [what it does]

Verifier rules (reject anything that fails):
- Open the app in a real browser and click every button
- Zero console errors
- No overlapping elements at 1280x720 and on a phone screen
- Data survives a page reload
- Stated constraints hold: dates fit, totals stay inside the budget, ineligible options are rejected. Quote both values on a fail

Send failures back to the worker who wrote it. Report to me only when every check passes, with the number of checks run
```
