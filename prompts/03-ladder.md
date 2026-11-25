# Prompt 3: One prompt for each rung

Start at the bottom. Move up only when the rung below is not enough. Higher rungs spend more quota. Boost and Teamwork need a paid plan.

```
1 Just Ask: Rewrite this email to sound confident and half as long: [text]
2 Sub-agents: While you work on [main task], send a helper to check [side job] and report back.
3 Orchestrator: (pick Orchestrator in the model menu) Plan and build [one bigger job]. Show me the plan before you start.
4 Workflows: /run-workflow For every file in [folder], [check/extract X] and give me one table. Show me the script before it runs.
5 Swarm: /swarm [see prompt 4]
6 Boost: /boost Find the root cause of [bug] and fix it. Prove the fix with a failing test that now passes.
7 Teamwork: /teamwork-preview Build [big project]. Interview me first, including what the team must not do. Write a done checklist and wait for my yes. Don't make anything up, check real sources.
```

## When not to use a rung

| Rung | Skip it when |
| --- | --- |
| Just Ask | The job has many different parts. |
| Sub-agents | The side job is the whole project. |
| Orchestrator | It is a quick question. |
| Workflows | One item, or each item needs different work. Show the script, cap the first run near 20, let a failed script fix itself and ask again, then save it for next week's folder. |
| Swarm | The work cannot be split, or it is a two-minute task. |
| Boost | The job is broad, or you are not fixing code. |
| Teamwork | You need the result today, or the job is small. |
