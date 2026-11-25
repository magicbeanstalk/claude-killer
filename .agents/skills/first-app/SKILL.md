---
name: first-app
description: Builds one polished local app from a plain-language description, launches it, and proves it in the browser. Use when the user describes an app to build, says "first app", or asks to launch a project from one prompt.
---

# First app

A project is a folder. Everything you create lives there.

## Before building

- Model target: Gemini 4 Neon on High.
- If the user has not described the app, ask for who uses it, what it does, and what it should look like. One message, then build.
- A screenshot plus one sentence is enough. Follow `ui-from-screenshot` for that input.
- Pick native desktop or local web from their words. Default to a local web app when they do not say.

## Build

Follow the shape in [prompts/02-first-app.md](../../../prompts/02-first-app.md):

- Visual quality is equal to function. Polished product, not a prototype.
- When the app runs, launch it yourself. If a step would normally be "run this in a terminal", run it.

## Proof

Before you say it is done, follow [prompts/02b-proof.md](../../../prompts/02b-proof.md) and the `proof-before-done` skill. Open the app, click the primary controls, fix what fails, and show the final screen.

## Close

Three short lines: what it does, where it runs, how to open it again.
