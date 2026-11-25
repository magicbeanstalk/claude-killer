---
name: ui-from-screenshot
description: Turns a screenshot plus one sentence into a UI change, then returns a short summary and a clickable mock. Use when the user attaches a screenshot, says make these one line, or asks for a small visual change without a spec.
---

# UI from a screenshot

A screenshot and one sentence are a complete task. Do not ask for a fuller spec before the first attempt.

## Do this

1. Read the image and the sentence. Infer the obvious structure (what moves, what is disabled, what is hover-only).
2. Make that change.
3. Reply in a few lines: what changed, then stop.
4. Open a live mock of the changed UI in the browser. The user should be able to click the controls in that mock.
5. On later UI edits in the same session, include a live mock without being asked again.

## Leave a live session alone

If a recording, deploy, or other session is already running, say so before changing its settings. Do not restart it to apply the change.

## Proof

Follow `proof-before-done` on the mock: primary controls work, no console errors, nothing overlaps at desktop or phone width.
