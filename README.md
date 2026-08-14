# VideoExpress Viral Relay Automation

A short, paste-ready Codex system prompt that creates a complete six-person
relay video from only:

- a topic
- an aspect ratio (`16:9` or `9:16`)

Copy [`SYSTEM_PROMPT.md`](SYSTEM_PROMPT.md) into Codex, sign in at
[https://app.videoexpress.ai/](https://app.videoexpress.ai/), then send:

```text
Topic: Three habits that improve morning focus
Aspect ratio: 9:16
```

The automation directly generates six Advanced videos, uses 6 seconds normally
or 8 seconds for longer dialogue, adds them to the timeline in scene order, and
saves the project. It does not perform post-generation playback, quality review,
repair, regeneration, trimming, or transition inspection.

## Fixed settings

- Visible in-app browser side screen
- Text to Video -> Advanced
- Advanced Mode enabled
- Automatic prompt enhancement disabled
- Requested aspect ratio selected for every scene
- Six different human speakers
- Exact continuous dialogue relay
- Private generation
- No export unless requested
