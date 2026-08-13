# VideoExpress Viral Relay Automation

A paste-ready Codex system prompt for producing a six-person relay video in
VideoExpress.ai from only two user inputs:

- a topic
- an aspect ratio (`16:9` or `9:16`)

This repository contains no website or interface. Codex controls the visible
VideoExpress browser, generates six distinct human-speaker clips, reviews them,
places accepted clips on the timeline in script order, and saves the project.

## Use

1. Open [`SYSTEM_PROMPT.md`](SYSTEM_PROMPT.md).
2. Copy its complete contents into the system-instructions field of a new Codex
   task or reusable agent configuration.
3. Make sure the Codex account has the Browser capability and can display the
   in-app browser side screen.
4. Sign in to VideoExpress.ai in that visible browser.
5. Send a request in this form:

```text
Topic: Why eclipse shadows become crescents
Aspect ratio: 16:9
```

Codex should begin immediately when both values are present.

## Fixed production format

- Six short Lipsync HD clips
- Six visibly different human speakers
- One continuous script relayed across all six speakers
- Five organic, topic-motivated match-action transitions
- Text to Video -> Advanced with Advanced Mode enabled
- Automatic prompt enhancement disabled for every generation
- Manual clip length set to approximately six seconds
- Direct path only: New -> Create with AI -> Text to Video -> Advanced
- Visual action and exact quoted dialogue in each Video Prompt
- Mandatory one-scene lip-sync calibration before batch generation
- Private generation
- Full audio and visual review before timeline placement
- Project saved but not exported unless the user asks

## Repository structure

```text
.
|-- AGENTS.md
|-- SYSTEM_PROMPT.md
|-- examples/
|   `-- requests.md
`-- evals/
    `-- acceptance-checklist.md
```

## Important quality decision

Generator prompts deliberately avoid mentioning overlay-related negative terms.
VideoExpress training demonstrates that explicitly asking the model to omit such
elements can cause it to generate them. Cleanup requirements remain in the
system workflow, outside the text sent to the video model.
