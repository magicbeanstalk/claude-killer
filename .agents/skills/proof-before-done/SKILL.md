---
name: proof-before-done
description: Proves a build by opening it, clicking through it, and fixing failures before calling it done. Use after building an app, fixing a UI bug, finishing a swarm, or when the user asks to verify, screenshot, or try to break it.
---

# Proof before done

Never accept "done" without a check the agent can run. The user-facing line is in [prompts/02b-proof.md](../../../prompts/02b-proof.md).

## Do this

1. Launch the app if it is not already running.
2. Open it in a real browser.
3. Click every primary button and try one bad input.
4. Read the console. Zero errors on the path you exercised.
5. Look at 1280x720 and a phone-width viewport. Nothing overlaps.
6. Reload. Data that should persist is still there.
7. Check every constraint the user stated. Dates must fit, totals must stay inside the budget, and ineligible options must be rejected. Quote the conflicting values when one fails.
8. Fix failures yourself, then re-run the failed checks.
9. Show the final screen and the number of checks that passed.

If a live recording, deploy, or other session is in progress, say so before changing its settings, and do not restart it.

If a check cannot run, say which one. Do not mark it passed.
